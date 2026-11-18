Source: https://arxiv.org/abs/2601.03210v2
PDF sha256: 79148155cfb54d20b64c06b6826f0f4cc3bc79099d09beaf268db01c7815e56d
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of kaman_2026_emulating_2d_materials_with_magnons_arxiv_2601_03210v2.pdf

Transcription of `kaman_2026_emulating_2d_materials_with_magnons_arxiv_2601_03210v2.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Emulating 2D Materials with Magnons
Bobby Kaman,1, ∗ Jinho Lim,1 Yingkai Liu,2 and Axel Hoffmann1, †

arXiv:2601.03210v2 [cond-mat.mes-hall] 30 Jan 2026

1
Department of Materials Science and Engineering and Materials Research Laboratory,
The Grainger College of Engineering, University of Illinois Urbana-Champaign, Urbana, Illinois 61801, USA
2
Department of Physics and Institute for Condensed Matter Theory, The Grainger College of Engineering,
University of Illinois Urbana-Champaign, Urbana, Illinois 61801, USA
(Dated: February 3, 2026)

Spin waves (magnons) in 2D materials have received increasing interest due to their unique states
and potential for tunability. However, many interesting features of these systems, including Dirac
points and topological states, occur at high frequencies, where experimental probes are limited. Here,
we study a crystal formed by patterning a hexagonal array of holes in a perpendicularly magnetized
thin film. Through simulation, we find that the magnonic band structure imitates that of graphene,
but additionally has some kagome-like character and includes a few flat bands. Surprisingly, its
nature can be understood using a 9-band tight-binding Hamiltonian. This clear analogy to 2D
materials enables band-gap engineering in 2D, topological magnons along 1D phase boundaries, and
spectrally isolated modes at 0D point defects. Interestingly, the 1D phase boundaries allow access to
the valley degree of freedom through a magnonic analog of the quantum valley-Hall insulator. These
approaches can be extended to other magnonic systems, but are potentially more general due to the
simplicity of the model, which resembles existing results from electron, phonon, photon, and cold
atom systems. This finding brings the physics of spin waves in 2D materials to more experimentally
accessible scales, augments it, and outlines a few principles for controlling magnonic states.

I.

INTRODUCTION

The isolation of single layers of carbon in 2004
essentially gave birth to the experimental field of
two-dimensional (2D) materials [1], and immediately
prompted further study of the quasi-relativistic nature
of charge carriers in graphene [2–4]. The catalog of 2D
materials grew to include a zoo of electronic phases, including semiconductors [5] and insulators [6] at first, but
later more exotic interacting phases [7–9]. Among the
later species to join the zoo are 2D magnetic materials
[10–12]. For example, ferromagnetism resembling both
Ising-like and XY spins can be found within the family
of chromium halides [13, 14] and antiferromagnetism can
be found in nickel halides [15, 16]. However, much of this
research goes beyond the equilibrium states of 2D magnets, and focuses also on novel magnetization dynamics.
In magnetically ordered solids, including 2D materials, the low-energy spin excitations are usually wave-like
collective excitations called spin waves (whose quanta
are magnons – the terms will be used interchangably).
Magnons are promising as charge-free information carriers for low-power computing devices in a field of study
referred to as magnonics [17–19]. Unique applications
of magnons include signal guiding using broken timereversal symmetry and inference tasks that exploit their
inherent nonlinearities [20–23]. Magnons in 2D and layered magnets bear similarities to their electronic counterparts and can host, for example, Dirac points [24], topological gaps [25], and flat bands [26]. Although some

∗ Contact Author: kaman3@illinois.edu
† Contact Author: axelh@illinois.edu

properties of these states are attractive, their applications seem distant because of their high frequency (on
the order of THz) and limited number of experimentally
readily accessible probes.
One strategy of controlling magnons is given by
magnonic crystals, analogous to the more well-known
photonic crystals [27–29]. By patterning a magnetic material into an artificial lattice, one may modify dispersion relations and open band gaps at the Brillouin zone
(BZ) edges [30–32]. This is a powerful control scheme
for magnon transport that may find application in nextgeneration microwave and information technologies [33].
In this study, we outline a general strategy towards mapping between a few 2D materials and magnonic crystals
supported by magnetization dynamics simulations and
simple models. Understanding this mapping allows engineering of magnonic band structures using principles
from 2D electronics. This brings some of the physics
of 2D materials to more accessible frequency and length
scales in a system that allows the addition of tailored
defects and other spatial inhomogeneities. Therefore we
provide a simple experimentally feasible platform that allows to probe directly the emerging physics of 2D materials, while also providing a design strategy for functional
devices at microwave frequencies.

II.

SPIN DYNAMICS SIMULATIONS

Phenomenologically, classical magnetization dynamics
are described by the Landau-Lifshitz-Gilbert [LLG] equation [34, 35]:
∂t M = −γµ0 M × Heff +

α
(M × ∂t M) ,
MS

(1)

## PDF page 2

2
where M is the magnetization with magnitude MS , γ
is the gyromagnetic ratio, and Heff is an effective magnetic field having contributions from externally applied
fields, the exchange interaction, crystalline anisotropies,
the demagnetizing field, etc. This first term gives rise to
the well-known precessional motion of the magnetization
M. α, the contribution of Gilbert, is a phenomenological
damping parameter that weakens precession over time. A
magnetic material may be thought of as being composed
of many volume elements, known as macrospins, whose
internal magnetization profiles are roughly uniform and
who each individually follow this equation of motion. It
is possible to perform simulations based on this principle,
in which Heff is calculated for each macrospin and time
is evolved in steps. This approach to numerical simulations, referred to as ’micromagnetism,’ [36] is rich in phenomena and is particularly helpful in studying magnetization switching, complex geometries and ground states,
and nonlinear/soliton dynamics. Here, we use the GPUaccelerated micromagnetics program MuMax3 [37] to
study spin waves. [Fig. 1(a,b)]. We choose realistic
material parameters of the prototypical magnonics material yttrium-iron garnet (YIG), which is widely used in
magnonic devices due to its low dissipation. See SM sec.
I for details [38].

A.

Geometry

Any periodic magnetic structure can be considered a
magnonic crystal. However, geometries like arrays of
disks face a disadvantage in being coupled only by the
relatively weak magnetic dipole-dipole interaction. One
approach is to embed magnetic components in a different magnetic matrix so the components may be loosely
thought of as resonators coupled through spin waves in
the matrix [39–42]. Another approach uses the so-called
”anti-dot” lattice, in which a continuous thin film is patterned with an array of holes [43–47]. The anti-dot lattice
is different because it cannot generally be thought of as
a clear set of coupled resonators. For instance, a lattice
with vanishingly small holes should approach the behavior of a pristine film. Note that similar geometries have
been explored in the artificial spin ice community, mostly
for their interesting ground states [48, 49].
In general, a spin wave dispersion relation depends
upon the magnetic ground state. Even for pristine thin
films, the dispersion is anisotropic for an in-plane magnetization due to the dipole-dipole interaction [50]. To emulate the isotropic dispersion that is natural for electrons
in 2D, we choose an out-of-plane (OOP) ground state
by applying an external field Bext ||ẑ sufficient to saturate the thin film [Fig. 1(c)]. Alternatively, one could
also assume magnetic thin films that have perpendicular magnetic anisotropy. We choose anti-dot spacings of
100’s of nm to balance experimental feasibility with large
frequency band widths. Due to the rectangular shape
of micromagnetic cells, it is tremendously convenient to

Figure 1. Spin waves in (a) 1D and (b) 2D. Each arrow indicates a macrospin and its color indicates the direction of
the in-plane magnetization and hence the phase of the precession. System geometry: (c) The hexagonal anti-dot lattice
with a perpendicular field, leaving a film similar to a honeycomb lattice. (d) (shaded) our rectangular supercell, with
orthogonal lattice vectors 333 nm × 589 nm, and (dashed)
the typical unit cell of the hexagonal lattice. (e) Corresponding Brillouin zone (BZ) for the rectangular unit cell, with a
few special points X and Y marked. (f) relationship between
special points in the typical BZ (dashed, black letters), and
their placement in the rectangular BZ (shaded, colored letters).

work with a rectangular unit cell. We define a rectangular supercell containing two primitive cells [see Fig. 1(d)].
As a result, the BZ is halved and contains double the
number of bands [Fig. 1(e)]. Note that special points in
the hexagonal BZ (K and K′ , for instance) now fall inside the rectangular BZ, as shown in Fig. 1(f). These are
technically new points, but we will refer to them as K
and K′ for simplicity.
For numerical simulations, a rectangular unit cell tens
of micromagnetic cells in width is tiled tens of times;
these two sizes determine real-space and inverse-space
resolution, respectively. The simulation contains only
one micromagnetic cell in the ẑ-direction – this is a good
approximation for very thin films, in which the exchange
interaction penalizes ẑ-direction texturing and standing
waves (see supplemental Sec. I [38]). A film thickness
of 15 nm is chosen to ensure accuracy. After the structure is relaxed to its OOP equilibrium state with periodic
boundary conditions in the x and y directions, excitation
can be applied to probe the magnonic band structure.

B.

Excitation and analysis

An excitation meant to probe a band structure should
couple to many wavevectors and frequencies – in other
words, it should resemble a δ(r, t)-function. Therefore,

## PDF page 3

3
within a small region, a radio frequency (rf) pulse is ap(t−t0 )]
plied of the form Bx (t) = B0 sin[2πf
2πf (t−t0 ) , whose spectrum contains all frequencies between −f and +f . B0
is chosen to be small (≈ 0.1 mT or less) to make sure
we stay in the linear regime. We time-evolve the system
under the LLG equation and record the magnetization
state m(t, x, y, z) as a unit vector. Precession about ẑ is
assumed, so the complex field:
Ψ ≡ mx + imy

(2)

is a convenient representation that will be used frequently. This field can be interpreted as a wavefunction in some sense. Assuming circular precession and neglecting damping, eigenmodes (by definition) should keep
their shape |Ψ(r, t)|2 and time-evolve only by a phase:
∂t Ψ(r, t) = iωΨ(r, t) for a specific angular frequency
ω = 2πf . To give a relevant example, the linearized
Landau-Lifshitz equation, including an exchange interaction of strength Dex and an externally applied field Hz (r)
can be rewritten (see appendix XI A) in a Schrödingerlike form assuming a ẑ-polarized ground state[51–53]:
(
)
∂t Ψ(r, t) = iγµ0 H(r) − Dex ∇2 Ψ(r, t)
(3)
This equation is not used here except to provide an intuitive interpretation of mode profiles as wavefunctions.
In the simulations of this study, the dipole-dipole interaction is included, which, of course, deviates from this
form. The Ψ representation is not necesssary, but is convenient and will be enlightening in drawing parallels to
electrons in real 2D materials.
The time evolution of the magnetization after excitation is written in terms of Ψ(r, t). Because it is a result of the excitation, we will refer to it as a response.
Bloch’s theorem can be used to extract the magnonic
band structure from the response: the signal is folded
into Ψ(t, x, y, i, j) where (i, j) are unit cell indices and
(x, y) label positions within the unit cell. Then, the signal
is Fourier transformed along the t, i, and j axes, resulting in the complex amplitude Ψ(f, x, y, kx , ky ) associated
with frequency f and crystal momentum (kx , ky ). This
approach is similar to Ref. 54.
III.

MAGNONIC BAND STRUCTURES

Though our analysis methods are general, we focus
mainly on the YIG hexagonal anti-dot lattice. A few
magnonic band structures are plotted in Fig. 2. After summing over the unit cell (x, y), the magnitude
of the response |Ψ(f, kx , ky )| is a function of frequency
and wavevector, so it can displayed as a projection on
the f, kx plane or plotted in 3D as volumetric information. As expected, a continuous film [see Fig. 2(a)] has a
magnonic band structure equivalent to the zone-folded
representation of a free dispersion – the ”nearly-freemagnon.” Small holes [see Fig. 2(b)] significantly change
the dispersion but do not open spectral gaps. However,

Figure 2. The effect of hole diameter d on YIG films with
lattice parameter a = 333 nm, thickness t = 15 nm. Band
structures are plotted as projections in the (kx , f ) plane for:
(a) d/a = 0.0 (no holes; equivalent to the free spin wave spectrum), (b) d/a = 0.4, and (c) d/a = 0.8. Rectangular unit
cells appear as insets. Bext ||ẑ is varied to keep the lowestfrequency mode constant. (d) a 3D volumetric plot of the
projection in (c), more clearly showing the isotropic character of flat bands. The d/a = 0.8 geometry is the main subject
of this study. To be more precise, the plots are the magnitude of the response |Ψ(f, x, y, kx , ky )| to a δ-like excitation,
displayed as projections on to only a few axes: (kx , f ) for 2D,
or (kx , ky , f ) for 3D.

large holes open spectral gaps and bring about some
curious features [see Figs.2(c) and (d)]: near 1.5 GHz,
the band structure resembles that of graphene. Near
2.5 GHz, the band structure seems to have a second set
of Dirac points, and additionally has a few flat bands
that meet dispersive bands at the Γ point. The nature of
the transition between Fig. 2(b) and 2(c) is not obvious;
see supplemental Sec. II [38] for an expanded figure.
Because of its curious features, this third geometry appearing in Fig. 2(c) is the main subject of this study. Our
primary goals are to:
1. Point out and understand the curious features
which naturally occur in this anti-dot lattice
2. Propose potential uses of its unique properties
3. Use understanding from the field of 2D materials
to engineer these excitations in ways not possible
with natural van der Waals systems
The isotropic flat bands of this system are particularly
interesting. A truly flat band is one which has zero group
velocity everywhere; its excitations are immobile. Fig. 3
illustrates this immobility. A rectangular region is continuously excited at the first flat band frequency. In the

## PDF page 4

4

Figure 3. Under periodic boundary conditions, a rectangular
region (yellow) is continuously excited at the first flat band
frequency of 2.08 GHz. Scaled profiles of |Ψ|2 are plotted after
50 ns for the geometries corresponding to (a,b,c) in Fig. 2.
The strong localization in (c) demonstrates the exceptional
flatness of the band. Note the scale differences: the flat band
mode is excited to ≈ 1000× the density of its counterparts,
making it potentially useful in easily reaching the nonlinear
regime. (d) Zoomed-in plot of the mode in (c), with phase
encoded in color. (left) Key for color plots and (right) the
localized wavefunction of the kagome lattice, which this mode
closely resembles. This is an example of how Ψ can be useful
to interpret as a wavefunction.

non-flat cases [see Figs. 3(a) and (b)], the power radiates away as usual. However, the flat band state cannot
propagate and is instead excited to ≈ 1000× the density
of its counterparts [see Fig. 3(c)]. This is a rare feature, making this system potentially useful in nonlinear
magnonics experiments (magnon Bose-Einstein condensation, for instance, in which large magnon densities must
be achieved) [55, 56]. Outside magnonics, interactions in
flat bands on the kagome lattice is a popular topic [57] –
given the inherent nonlinearity of magnons, it is possible
that this may provide a platform for an analog of interacting phases when this localized state is excited to large
magnon number [58].
Interestingly, the reason behind localization here can
be understood from existing principles in 2D materials.
Figure 3(d) is a zoomed-in version of Fig. 3(c), plotted
using a phase-sensitive scheme. This reveals that the
excited mode closely resembles the famous localized electronic wavefunction of the kagome lattice, whose localization property can be understood as the result of destructive interference between neighboring sites [59–61].
This spin wave mode is also similar to localized spin excitations observed in the flat bands of layered kagome
magnets, which can be understood by the same means
[26, 62].
To understand the real nature of the excitations,
Ψ(x, y) can be examined at a few (f, kx , ky ) points. This
cell-periodic part of the response can be interpreted as

Figure 4. (a) Magnonic band structure for d/a = 0.8 and
Bext = 185 mT along a few paths in the rectangular BZ.
(b) A few examples of Bloch function-like responses at the Γ
point, and (c) their reconstructions using a small number of
basis ’orbitals,’ discussed in more detail in Sec. IV. (right)
Key for color plots of Ψ. The main finding is that the Bloch
functions are simple, suggesting a tight-binding model.

a Bloch function. The magnon band structure is plotted along a few paths in Fig. 4(a), and some Bloch-like
functions for Γ-point modes are plotted in Fig. 4(b).
One finding is that the lowest set of bands is indeed
graphene-like: this figure demonstrates the Dirac point
more clearly, but perhaps more incriminating is the fact
that Γ-point modes 1 and 2 in Fig. 4(b) are given by
acoustic and optical modes of the honeycomb lattice. Actually, there exists a tiny gap at the Dirac point due to
the dipole-dipole interaction, which is not easy to resolve
(see supplemental Sec. III [38]). This is interesting but
will be the primary subject of another study; here, we
focus on a simple picture of the band structure.
The most important finding demonstrated by Fig. 4
is that not just the graphene-like modes, but all the Γpoint modes may be understood with a simple set of basis
functions (or ”orbitals”). Figure 4(c) is an illustration of
reconstructions using this set of functions, which consists
of: (1) s-like spin wave modes on the honeycomb lattice,
(2) p-like modes on the honeycomb lattice, and (3) slike modes on the kagome lattice, for a total of 9 degrees
of freedom per primitive unit cell, or 18 per rectangular

## PDF page 5

5
cell. 1–2 GHz bands appear to be composed of s-like
modes and 2–3.5 GHz bands of p-like modes – we refer
to these as s-bands and p-bands, respectively. A natural
question is: If the Bloch functions can be reconstructed
using these basis orbitals, can the band structure also be
reproduced? The latter part of this study is dedicated to
this type of understanding and the engineering it enables.

the nonuniform mode operators can be thought of as superpositions of magnon operators on many macrospins,
with new hopping parameters that are simple to calculate from old parameters. In this picture, the hamiltonian
becomes:
) ∑
∑ ( †
H=
tij ai aj + ai a†j +
εi a†i ai
(8)
ij

IV.

TIGHT-BINDING-LIKE ANALYSIS

Taking a step back, a simple Heisenberg spin chain under an externally applied magnetic field has the hamiltonian [63]
gµB B0 ∑ z
J ∑
Si · Sj −
Si
H = −2 2
h̄
h̄ ⟨ij⟩
i

(4)

for an externally applied field B0 ||ẑ and ferromagnetic
exchange parameter J which couples neighboring spins
⟨ij⟩. This can be rewritten using spin raising and lowering operators S ± ≡ Sx ± iSy . The Holstein-Primakoff
(HP) transformation [64] can then be used to rewrite this
problem with magnon operators, assuming total spin s
parallel to ẑ and small magnon number:
√
Si+ ≈ h̄ 2sai
(5)
√
Si− ≈ h̄ 2sa†i
H = −2J s

i

in which i, j may now refer to different types of nonuniform modes.
Motivated by the observation that the Bloch functions
[see Fig. 4(b)] are made of s and p ’orbitals,’ we choose
this basis for a TB model. Using only nearest-neighbor
hoppings, we implement this model using the PythTB
package [67] and adjust parameters by hand. Fit parameters are listed in table I in units of frequency. Figure 5(a) is the same band structure appearing earlier,
and Fig. 5(b) is its corresponding model, displayed in a
manner similar to the simulations, using basis orbitals
shown in Fig. 5(c) and (d). More precisely, we plot the
spectrum of a supercell extended in the ŷ-direction with
semitransparent coloring, and only plot the kx extent of
the rectangular BZ.
It is remarkable that a TB model works well in an
anti-dot lattice. The orbitals emerge naturally from the
structure without any careful engineering. The fact that

)
∑( †
ai aj + ai a†j − a†i ai − a†j aj + s
⟨ij⟩

+gµB B0

∑(

s − a†i ai

)

(6)

i

Defining constants t = −2J s, ε = gµB B0 + 4J s, and
keeping only terms with magnon operators, this can be
rewritten as
)
∑( †
∑ †
H=t
ai aj + ai a†j + ε
ai ai
(7)
⟨ij⟩

i

This is the generic form of a tight-binding (TB) model
for a 1D atomic chain, except that operators refer to
magnons in the HP formalism. This suggests that TB
models with appropriate parameters can generically describe exchange-only systems with ferromagnetic ground
states. The interpretation is the same when these operators act on macrospins in nanostructures [65]. With
this TB picture in mind, it is not a large stretch to expect that nonuniform spin wave modes may also be represented by operators in this model, as long as the hopping parameters tij and energies εi are properly adjusted.
For example, an array of exchange-coupled elements may
be described by an effective TB model in which a†i creates a magnon in a nonuniform mode i, mainly confined
to a single magnetic element [66]. To be more precise,

Figure 5. (a) Simulated kx -projected band structure as plotted in Fig. 2(c), and (b) its 9-band tight-binding model using
fitting parameters listed in table I. (c) Basis orbitals for the
TB model (left to right): s, px , py orbitals on honeycomb sites,
and s orbitals on kagome sites. (d) Illustration of fitting parameters.

## PDF page 6

6
εs 1.69 GHz
εp 3.15 GHz
εk 3.17 GHz
tsk -0.38 GHz
tpk -0.63 GHz
Table I. Tight-binding parameters and their values as used in
Fig. 5. εi are ’on-site’ frequencies for orbital i and tij are hopping parameters between orbitals i and j. Subscripts s and
p denote s-like and px,y -like modes on the honeycomb lattice.
Subscripts k denote s-like modes on the kagome lattice.

a simple model works suggests that this is a general feature of the geometry that has nothing to do with spin
waves. Indeed, simply solving the Schrödinger equation
for a massive particle in a potential resembling this antidot lattice can yield a similar band structure (see supplemental Sec. IV [38]). This phenomenon can be understood from Eq. 3. In fact, as a representation of the simplicity of excitations in this system, similar band structures have been discussed and observed in electronic,
photon/polariton, acoustic, and cold-atom systems [68–
73].
Although the model appears to work, there are some
inconsistencies. At the Γ point of the lowest band, the
dispersion in the simulation is linear due to the dipoledipole interaction [50], which is explicitly ignored by the
TB model. Small mid-band gaps are also observable in
the simulations, but this is only an artifact of the imperfect reconstruction of the hexagonal lattice using pixels,
which breaks its C6 symmetry down to C2 . Such gaps
are not expected for real lattices. In addition, the model
is less accurate at high frequencies. This is because the
real wavelength of spin waves becomes small compared to
the lattice features. For larger hole sizes (smaller lattice
features), these high-frequency bands approach a more
TB-like form (see supplemental Sec. II [38]). Other subtle inconsistencies exist, in part due to the TB model’s
exclusion of the dipole-dipole interaction.
The fact that TB works well is curious but does not
teach us anything fundamentally new. However, understanding this band structure in terms of graphene-like
s and px,y excitations enables engineering using existing
principles from the field of 2D materials.

V.

SPIN WAVE ENGINEERING
A.

Inversion-broken crystals

In graphene, the masslessness of Dirac electrons is protected in part by inversion symmetry. Hexagonal boron
nitride (h-BN), another 2D compound, is isostructural
but with different atoms on each honeycomb sublattice.
This breaks the inversion symmetry of the unit cell, and
the Dirac points gap (for this reason, these symmetrybreaking terms are sometimes called mass terms). As a
result, h-BN is an insulator. This is shown schematically

Figure 6. The effect of inversion symmetry breaking on the s
and p bands. (a) Band structure for a unit cell with broken
symmetry, plotted in the same manner as before. The spectrum can still be modeled with TB. Symmetry breaking enters
the model as terms that discriminate between the honeycomb
sublattices, ∆εs and ∆εp , resulting in band gaps for both the
s- and p-bands. (b) Analogy to graphene and its symmetrybroken sister h-BN: a gap (highlighted in blue) opens at K
and K′ points. Fit parameters are listed in table II. (c)
The dependence of induced gaps and flat band frequencies
on externally applied field, extracted from simulations. This
tunability is one of the unique benefits of magnonic systems.

in Fig. 6(b). Even stacking graphene on h-BN has this result because of the small amount of symmetry breaking
[74, 75]. This principle is powerful because, unless the
system is fine-tuned, any method of breaking inversion
symmetry should result in a gap.
To mimic the relationship between graphene and h-BN,
we create new unit cells that break inversion symmetry
and perform simulations again. Figure 6(a) displays the
resulting band structures in the same manner as before.
As predicted, a gap is present in the inversion-broken
geometries. In analogy to h-BN, the symmetry breaking
can be described in TB by a difference ∆ε ≡ 12 (εB − εA )
in the energies of the two sublattices. For simplicity, this
is the only addition made to the model. Controllable
spin wave band gaps are desirable for rf applications;
it is interesting to note that this is an example of gaps
whose width is tunable using guidance from the analogy
to 2D materials. Furthermore, the frequency of these
gaps (along with all other features) can be tuned by an
externally applied magnetic field as shown in Figure 6(c).
This tunability is natural to magnonic crystals and, from
a functionality perspective, is a benefit compared to photonic and phononic crystals.
In graphene-like systems, these symmetry-breaking
mass terms do more than simply open a gap. For small
mass terms, opening such a gap generates sharply peaked
Berry curvature near the valleys K and K′ . Integrating
the Berry curvature over the vicinity of a single valley
yields an approximately quantized value, often referred

## PDF page 7

7
εs
1.93 GHz
εp
2.83 GHz
εk
3.28 GHz
∆εs 0.12 GHz
∆εp 0.35 GHz
tsk -0.45 GHz
tpk -0.49 GHz
Table II. Tight-binding parameters and their values as used
in Fig. 6, following the same labeling as in table I.

to as a valley Chern number (VCN) [76]. The two valleys
carry opposite VCNs, so the total Chern number over the
full Brillouin zone is zero. Nevertheless, a change in VCN
across a domain wall implies valley-polarized boundary
modes [77, 78], which remain robust as long as intervalley scattering remains weak [76]. TB calculations in this
s, px,y system show that symmetry breaking has this effect for both the s-band gaps and the p-band gaps. At
a single valley, the sign of the Berry curvature is opposite above and below the gap for both s and p bands,
but notably has a different sign in each (s, p) case. Upon
changing the sign of the symmetry-breaking terms ∆εs
and ∆εp , the sign of curvature flips (see supplemental
Sec. V [38]), schematically illustrated in Fig. 7(a).
This magnetic thin film geometry, unlike vdW systems,
is continuously tunable between distinct gapped phases.
Partially inspired by the Jackiw-Rebbi model [79], we investigate a boundary between these gapped phases. Figure 7(b) shows a gradual phase boundary in which the
unit cell changes shape over a few lattice spacings, making a smooth transition between the two phases. In the
corresponding TB model, we create a long supercell with
varying mass terms [Fig. 7(c)]. The band structure of the
TB model contains the essential features of the simulation, most notably the presence of states that bridge the
gap at each valley, highlighted in Fig. 7(d). These will
be referred to as boundary modes.
In our TB model, as we increase mass terms, Berry curvature is no longer localized to the valleys and the VCN
loses its quantization (supplemental Sec. V [38]). This
behavior is common in realistic systems [80–82], where
the absolute value of the VCN is smaller than its quantized value in the small-gap limit and varies smoothly
with system parameters. However, since the bulk gap
does not close as we vary mass parameters, the boundary modes we observe are adiabatically connected to
those in the small-gap limit. They remain (for example, in our simulations) visible well beyond the regime
where the VCN is sharply quantized. This phenomenon
of boundary-localized states has been seen before in many
other graphene-like systems [83–89], but occurs here for
both the s and p bands. Because the ∆ε terms affect the s
and p gaps in different ways, the corresponding magnon
boundary modes bridge the gaps with opposite chiralities: in the lower gap, K(K′ )-valley magnons propagate
to the left (right), while in the upper gap, K(K′ )-valley
magnons propagate to the left (right). The direction of

Figure 7. A boundary between different gapped phases. (a)
Two distinct gapped phases with different Berry curvature
at a given valley. (b) The simulated geometry, including a
boundary between the phases. (c) The corresponding TB
setup, in which the symmetry-breaking terms change sign
along the ŷ-direction. (d) Simulated and modeled band structures. In the simulation, the excitation is at the boundary.
To mimic this, the TB spectrum is plotted with opacity given
by amplitude at the boundary. Magnon states bridging the
gaps (highlighted in blue) indicates two instances of quantum
valley-Hall insulator behavior. However, the states bridging
the two gaps have opposite propagation: (e) s modes (in the
lower gap) have K′ -polarized waves moving to the right, while
p modes (in the upper gap) have K′ -polarized waves moving
to the left.

this valley-polarized magnon current can be reversed by
changing the sign of the symmetry-breaking terms (see
supplemental Sec. VI [38]). By calculating the VCNs of
the bulk bands in the small-gap limit, we thus identify
these boundary states as the magnonic analog of quantum valley Hall (QVH) edge states[76, 90], as illustrated
in Fig. 7(e). This is a more accessible realization of the
type of state proposed for 2D honeycomb magnets with
controllable staggered anisotropies [91]. For a more complete discussion including Berry curvature maps, see the
supplemental Sec. V [38].

B.

Topological Magnon Waveguiding

The QVH-like states that are localized to the boundary may be used as a frequency-selective waveguide for
valley-polarized magnons. In the same geometry as be-

## PDF page 8

8

Figure 8. Demonstration of spin wave transport along phase boundaries. (a) Simulation geometry, the same as that in Fig. 7.
(b) Spin wave profile 30 ns after the peak of a 2.7 GHz pulse (inside the p-band gap). Left- and right-moving modes are
valley polarized and move only along the boundary. The excitation (yellow) is tilted to match the phase profile of the spin
waves and allow efficient coupling. The boundary can be reduced in width and still allow directed transport, even along sharp
turns. Profiles are plotted after 500 ns of continuous excitation at (c) 1.55 GHz in the s-band gap, and (d) 2.55 GHz in the
p-band gap. Unlike the edge states of Chern insulators, because there exist co-localized left- and right- moving edge states,
inter-valley scattering is allowed. To demonstrate this, we show (e) Gaussian wavepackets scattering from a point defect formed
by removing a honeycomb site. Space-time plots of the spin wave profiles are shown for (f) the s-gap mode and (g) the p-gap
mode with the defect position marked in gray. Profiles are examined after the collision and give calculated reflections of ≈ 6%
and ≈ 22% respectively.

fore, shown again in Fig. 8(a), an excitation is applied
inside a localized region. At the in-gap frequency of
2.7 GHz, spin waves are launched only along the phase
boundary, as shown in Fig. 8(b). Because of the valleyspecific topological origin of these modes, left- and rightmoving modes are oppositely valley polarized – an interesting feature because valley polarization is occasionally
thought of as an information-carrying degree of freedom
in discussions of next-generation information technologies [92]. The transition between the insulating phases
can be reduced in width, and the states persist, even following sharp turns made by the phase boundary. This
phenomenon occurs for both s and p boundary modes [see
Figs. 8(c) and (d), respectively]. In both cases, magnon
transport remains completely localized to the boundary
after 500 ns of continuous excitation. It is worth noting
a few limitations here. Geometry does not only affect
the shape of the band structure; there can be a constant frequency offset as a result of the demagnetizing
field. This is the same reason Bext is varied for the different geometries in Fig. 2. When geometry is varied
over space, this varying frequency offset can result in a
spectral overlap of the localized mode with other bulk
modes. In this case, a large-area excitation like that in
Fig. 8(a) would excite both boundary and bulk modes.
In other words, the appealing boundary-specific transport demonstrated by Fig. 8 may not exist in all geometries with phase boundaries. Also note that these modes

are not protected against backscattering, making them
fundamentally different from more famous examples of
topological edge states in metamaterials, in [93, 94] for
example. Scattering between valley modes caused by a
point defect is demonstrated in Fig. 8(e-g) for both sgap and p-gap modes, returning differing reflection amplitudes for each case. This is discussed in more detail in
the supplemental Sec. VII [38].

C.

Isolated defect modes

The unique power of patterned crystals lies in the ability to control its properties in a spatially varying way.
In the previous section, this ability was used to exploit
valley band topology and waveguide magnons along a
one-dimensional boundary. It is also worth discussing
magnons that are confined to zero-dimensional point defects. Here we demonstrate a simple case of this: only
one honeycomb site is replaced with a disk similar to that
in the inversion-broken unit cells [see Fig. 9(a)], analogous to a substitutional defect in graphene (nitrogen or
boron, for example). In a phenomenon similar to spin
wave ”edge modes,” [95, 96] A single defect has a localized mode which lies below the bulk uniform precession
mode. Two such defect modes couple when placed in
adjacent sites. Using the TB interpretation, the level
should split into symmetric and antisymmetric superpo-

## PDF page 9

9

Figure 9. Level structure of point-defect modes under Bext =
200 mT ẑ. (a) Simulation geometry: A single defect resembling that used in the inversion-broken structures of section V A. (b) The localized modes of a single defect versus
two adjacent defects. When coupled, they split by 2∆ ≈
0.18 GHz, producing a two-level magnon spectrum that appears entirely below the continuum. These modes are plotted
in the same fashion as the Bloch-like functions of Fig. 4.

sitions of the original modes, separated in frequency by
twice the coupling parameter ∆. This is apparently a
good interpretation, as evidenced by the mode profiles
in Fig. 9(b). A single-defect mode at 1.47 GHz splits
into a symmetric mode at 1.38 GHz and an antisymmetric mode at 1.56 GHz (for details, see supplemental
Sec. VIII [38]). It happens that this whole level structure
appears below the continuum, which implies that these
defect-localized magnons may be interacted with separately from propagating waves, suggesting further application in magnonics. For the chosen Gilbert damping
parameter of α = 10−4 , these modes have quality factors
≈ 4100.

VI.

OTHER TB-LIKE SYSTEMS

In the previous sections, it was demonstrated that a
TB-like understanding can be used to engineer magnonic
band structures in analogy to a few popular 2D materials. It is worthwhile to show that this TB approach is
applicable in at least a few other cases. Fig. 10 shows
two such examples: a square anti-dot lattice and an artificial kagome lattice. The magnonic structure of the
perpendicularly magnetized square anti-dot lattice [see
Fig. 10(a)] happens to be analyzable using the same
approach. A TB model with s and p orbitals in the middle of the unit cell and s orbitals between these sites can
approximate the band structure with the right fitting parameters. Its spectrum is plotted in Fig. 10(b), using the
basis orbitals in Fig. 10(c). This square lattice is apparently another case of emergent ”atomic orbitals” (see
supplemental Sec. IX [38] for details). There is a simpler
(albeit less experimentally feasible) approach to engineer
magnonic band structures. Figure 10 also shows an artificial kagome lattice, where it is assumed that disks will
host s-like modes, so the disks are arranged to mimic the
kagome lattice [see Fig. 10(d)]. In this case, a simple
model of s-orbitals on the kagome lattice can approximate the band structure [see Fig. 10(e)]. This is similar

Figure 10. Other geometries which can be thought of as TBlike, using 15-nm YIG films with a lattice spacing a = 300 nm
and Bext ||ẑ = 185 mT. (a) The square anti-dot lattice, and
(b) its TB model, using (c) basis orbitals similar to those used
in the hexagonal anti-dot model. Some inconsistencies are
due to hybridization with higher-order modes like d-orbitals
(see supplemental Sec. IX [38]), which are not included for
simplicity. (d) Shows the artificial kagome lattice and (e) its
TB model using only s orbitals on kagome sites.

to results previously reported for magnetic rods embedded in a magnetic matrix [42, 97]. In this case, the relative decrease in momentum space resolution is due to the
fact that the unit cell must be simulated with greater resolution, so the whole simulation field has fewer unit cells
for computationally practical reasons.

VII.

EXPERIMENTAL FEASIBILITY

The YIG anti-dot lattices studied in this work may be
fabricated by standard electron beam lithography procedures including a hard mask and ion etch step, or by
focused ion beam (FIB) milling for the fabrication of single devices. There is already a significant amount of work
on these structures [43–47], albeit with somewhat different dimensions. Preliminary work indicates that FIB can
yield devices with sufficient scale and tolerances. In the
supplemental material Sec. X [38], we verify that lattices

## PDF page 10

10
with a thin magnetic dead layer caused by ion damage
are expected to yield similar physics. We also verify that
in the presence of edge roughness, flat modes, band gaps,
defect-localized modes, and QVH-like modes persist with
only moderate modification (Sec. XI [38]). All simulations are conducted for a Gilbert damping parameter
α = 10−4 and MS = 140 kA/m, which is realistic for YIG
[98, 99]. Overall, the anti-dot lattice is a more realistic
experimental route to these types of magnonic flat bands
compared to existing proposals, which mainly focus on
ferromagnetic rods embedded in a matrix[41, 42, 97].

VIII.

DISCUSSION AND CONCLUSION

Because the magnonic crystals discussed here demonstrate unique properties, it is worth discussing their potential applications.
First, the existence of isotropic flat bands of Fig. 3
is notable. In the TB picture, it is trivially easy to
achieve flat bands in one sense: an array of decoupled
resonators has no dispersion. However, here, the modes
are strongly coupled and flatness emerges from the symmetry of the basis orbitals and the geometry of the lattice. Bloch functions in this band contain singularities
at band touching points, a property which sometimes
awards it the title of ”topological flat band” in electronics
[59, 100]. Furthermore, these states may be of interest
for exploring magnon-magnon interactions, particularly
as analogs of interacting electronic phases on the kagome
lattice. The localization property of these magnons indicates that they could easily be excited to large magnon
numbers, potentially resulting in emergent modes which
already have some theoretical description in the hot research area of interacting kagome flat bands. The excitation enhancement due to flat band magnons has been
studied before, for example in [101].
Second, the topological magnons of Sec. V B are, of
course, attractive for precise control of magnon propagation. However, they are additionally interesting because
we can exercise control over the valley degree of freedom.
For example, in the setup of Fig. 8(a), any spin wave device to the right of the antenna should only ever receive
K-polarized spin waves at the frequency of 2.7 GHz. This
work may prove an important step in realistic magnonvalleytronics.
Third, additional control over the valley degree of freedom could reasonably be exercised here through an inhomogeneous pattern that mimics a strain field. Inhomogeneous strain fields can result in an effective gauge
field for Dirac point excitations, commonly called a
pseudo-magnetic field [102, 103]. The freedom associated
with patterning in this system might be used to realize
magnon valley filters, lenses, collimators, and (pseudo)Landau levels for magnons [104–106].
Fourth, point defects such as those in Fig. 9 may be
useful in magnonics because of their spatial localization
and spectral isolation. This implies that a carefully

placed waveguide could selectively excite these quasiuniform localized modes – making them potentially useful as a magnonic memory because spin waves will not
radiate away from the defect. Additionally, the fact that
a coupled two-mode structure of such defects still lies
below the continuum is interesting. We envision classical spin wave analogs of effects like induced transparency
and Rabi oscillation. If sufficiently long magnon lifetimes
can be achieved, possibly aided by the localization of the
modes[107], then this may also be an interesting perspective for designing quantum magnonic systems.
Fifth, these findings are generalizable in a few ways.
Sec. VI demonstrates that tight binding is somewhat accurate in a few other cases of perpendicularly magnetized YIG films, implying that the 2D-analog engineering done in the previous sections can be extended to
other magnon systems. However, in Sec. IV we mention that both tight-binding and the Schrödinger equation can reproduce band structures similar to the ones
observed here – implying that some of these engineering
strategies are applicable not only to magnonic systems,
but any system which can reasonably be described by a
simple Schrödinger equation.
Finally, because there exists similar physics in other
analog systems [68–73], it is worth noting a few novelties and benefits associated with this magnonic system.
The literature tends to focus on s-like modes, but we
show that it’s also possible to accomplish valley-specific
physics with p-like modes, and we show that it can be understood through the same TB lens. This amplifies the
potential for valley-tronics because there are two channels through which valley information may propagate.
There are also benefits that are unique to magnonic systems. Most importantly, the whole band structure is
tunable not just by geometry, but also by externally applied field, as was demonstrated in Fig. 6(c). This suggests that a constant microwave signal may be tuned on
the fly to be blocked by band gaps, waveguided, valleyor orbitally polarized, strongly localized in flat bands,
interacting with defect modes, etc. simply by varying
the external field. Spin waves also are associated with
a unique combination of small wavelengths and low frequencies; it is a significant result that a microwave signal
can be localized to these phase boundaries by some band
topology manipulation.
In conclusion, patterning a hexagonal array of holes
into perpendicularly magnetized YIG thin films is found
to lead to some unexpected features. Namely, the band
structure mimics a few unique properties of 2D systems,
and can be understood using a tight-binding model. This
new understanding allows the engineering of magnonic
states using existing principles from 2D materials to produce controllable band gaps, topological magnons along
1D channels, and spectrally isolated magnons at 0D point
defects. These design principles seem to be generalizable
to other geometries and even other excitations, but here
represent an important step in achieving and manipulating physical states that are usually reserved for van der

## PDF page 11

11
Waals systems.

XI.
A.

APPENDIX

Schrödinger-like form of the LL Equation

Beginning with the Landau-Lifshitz-Gilbert equation:
∂t M = −γµ0 M × Heff +

IX.

ACKNOWLEDGEMENTS

All aspects of this work were mainly supported by
the Illinois Materials Research Science and Engineering
Center (MRSEC) under grant no. DMR-2309037. Additional contributions to data analysis and manuscript
preparation were supported by the U.S. DOE, Office of
Science, Basic Energy Sciences, Materials Science and
Engineering Division under contract No. DE-SC0022060.
Other contributions to analysis were supported by the
U.S. Office of Naval Research (ONR) Multidisciplinary
University Research Initiative (MURI) Grant N00014-201-2325 on Robust Photonic Materials with High-Order
Topological Protection for support. We thank Taylor
Hughes for stimulating and fruitful discussions.

α
(M × ∂t M)
MS

for magnetization M of magnitude MS , gyromagnetic ratio γ and permeability of free space µ0 . Neglecting damping and rewriting in terms of the reduced magnetization
vector m ≡ M/MS ,
∂t m = −γµ0 m × Heff
Assuming Heff ||ẑ ≡ H, m ≈ ẑ, the linear limit,
∂t mx = −γµ0 Hmy
∂t my = γµ0 Hmx
∂t (mx + imy ) = γµ0 H(imx − my )
defining:

Ψ ≡ mx + imy
∂t Ψ = iγµ0 HΨ

Because we have introduced no Heff term which couples
spins over space, this should also be true for a set of
macrospins organized in space:

X.

SUPPELEMENTAL MATERIAL AND DATA
AVAILABILITY

See Supplemental Material [38] for a document containing items cited in the text. Codes used for simulation
and analysis are also openly available in Ref. [108].

[1] K. S. Novoselov, A. K. Geim, S. V. Morozov, D. Jiang,
Y. Zhang, S. V. Dubonos, I. V. Grigorieva, and A. A.
Firsov, Electric Field Effect in Atomically Thin Carbon
Films, Science 306, 666 (2004).
[2] M. I. Katsnelson, K. S. Novoselov, and A. K. Geim,
Chiral tunnelling and the Klein paradox in graphene,
Nat. Phys. 2, 620 (2006).
[3] G. Li and E. Y. Andrei, Observation of Landau levels
of Dirac fermions in graphite, Nat. Phys. 3, 623 (2007).
[4] F. Guinea, M. I. Katsnelson, and A. K. Geim, Energy
gaps and a zero-field quantum Hall effect in graphene
by strain engineering, Nat. Phys. 6, 30 (2010).

∂t Ψ(r) = iγµ0 H(r)Ψ(r)
Including the exchange interaction of strength Dex in the
effective field (and assuming its direction is +ẑ), this can
be written in a form [51–53]:
(
)
∂t Ψ(r) = iγµ0 H(r) − Dex ∇2 Ψ(r)
Which resembles a Schrödinger equation for a massive
particle in a potential γµ0 H(r). See ref. [53] for an
application of this idea to quantized spin waves modes in
finite-size systems.

[5] V. Podzorov, M. E. Gershenson, C. Kloc, R. Zeis, and
E. Bucher, High-mobility field-effect transistors based
on transition metal dichalcogenides, Appl. Phys Lett.
84, 3301 (2004).
[6] K. S. Novoselov, D. Jiang, F. Schedin, T. J. Booth,
V. V. Khotkevich, S. V. Morozov, and A. K. Geim,
Two-dimensional atomic crystals, Proc. Natl. Acad. Sci.
U.S.A. 102, 10451 (2005).
[7] M. M. Ugeda, A. J. Bradley, Y. Zhang, S. Onishi,
Y. Chen, W. Ruan, C. Ojeda-Aristizabal, H. Ryu,
M. T. Edmonds, H.-Z. Tsai, A. Riss, S.-K. Mo, D. Lee,
A. Zettl, Z. Hussain, Z.-X. Shen, and M. F. Crommie,
Characterization of collective ground states in single-

## PDF page 12

12
layer NbSe2 , Nat. Phys. 12, 92 (2016).
[8] Y. Cao, V. Fatemi, S. Fang, K. Watanabe, T. Taniguchi,
E. Kaxiras, and P. Jarillo-Herrero, Unconventional superconductivity in magic-angle graphene superlattices,
Nature 556, 43 (2018).
[9] Y. Zeng, Z. Xia, K. Kang, J. Zhu, P. Knüppel,
C. Vaswani, K. Watanabe, T. Taniguchi, K. F. Mak, and
J. Shan, Thermodynamic evidence of fractional Chern
insulator in moiré MoTe2 , Nature 622, 69 (2023).
[10] W. Han, R. K. Kawakami, M. Gmitra, and J. Fabian,
Graphene spintronics, Nat. Nanotechnol. 9, 794 (2014).
[11] B. Huang, G. Clark, E. Navarro-Moratalla, D. R. Klein,
R. Cheng, K. L. Seyler, D. Zhong, E. Schmidgall, M. A.
McGuire, D. H. Cobden, W. Yao, D. Xiao, P. JarilloHerrero, and X. Xu, Layer-dependent ferromagnetism
in a van der Waals crystal down to the monolayer limit,
Nature 546, 270 (2017).
[12] C. Gong, L. Li, Z. Li, H. Ji, A. Stern, Y. Xia, T. Cao,
W. Bao, C. Wang, Y. Wang, Z. Q. Qiu, R. J. Cava,
S. G. Louie, J. Xia, and X. Zhang, Discovery of intrinsic ferromagnetism in two-dimensional van der Waals
crystals, Nature 546, 265 (2017).
[13] Y. Liu, L. Wu, X. Tong, J. Li, J. Tao, Y. Zhu, and
C. Petrovic, Thickness-dependent magnetic order in
CrI3 single crystals, Sci. Rep. 9, 13599 (2019).
[14] A. Bedoya-Pinto, J.-R. Ji, A. K. Pandeya, P. Gargiani, M. Valvidares, P. Sessi, J. M. Taylor, F. Radu,
K. Chang, and S. S. P. Parkin, Intrinsic 2D-XY ferromagnetism in a van der Waals monolayer, Science 374,
616 (2021).
[15] H. Liu, X. Wang, J. Wu, Y. Chen, J. Wan, R. Wen,
J. Yang, Y. Liu, Z. Song, and L. Xie, Vapor Deposition
of Magnetic Van der Waals NiI2 Crystals, ACS Nano
14, 10544 (2020).
[16] D. Bikaljević, C. González-Orellana, M. Peña-Dı́az,
D. Steiner, J. Dreiser, P. Gargiani, M. Foerster, M. A.
Niño, L. Aballe, S. Ruiz-Gomez, N. Friedrich, J. Hieulle,
L. Jingcheng, M. Ilyn, C. Rogero, and J. I. Pascual, Noncollinear Magnetic Order in Two-Dimensional NiBr2
Films Grown on Au(111), ACS Nano 15, 14985 (2021).
[17] V. V. Kruglyak, S. O. Demokritov, and D. Grundler,
Magnonics, J. Phys. D: Appl. Phys. 43, 264001 (2010).
[18] A. A. Serga, A. V. Chumak, and B. Hillebrands, YIG
magnonics, J. Phys. D: Appl. Phys. 43, 264002 (2010).
[19] A. V. Chumak, V. I. Vasyuchka, A. A. Serga, and
B. Hillebrands, Magnon spintronics, Nat. Phys. 11, 453
(2015).
[20] Q. Wang, A. V. Chumak, and P. Pirro, Inverse-design
magnonic devices, Nat. Commun. 12, 2636 (2021).
[21] A. Papp, W. Porod, and G. Csaba, Nanoscale neural
network using non-linear spin-wave interference, Nat.
Commun. 12, 6422 (2021).
[22] N. Zenbaa, C. Abert, F. Majcen, M. Kerber, R. O.
Serha, S. Knauer, Q. Wang, T. Schrefl, D. Suess, and
A. V. Chumak, A universal inverse-design magnonic device, Nat. Electron. 8, 106 (2025).
[23] L. Körber, C. Heins, T. Hula, J.-V. Kim, S. Thlang,
H. Schultheiss, J. Fassbender, and K. Schultheiss, Pattern recognition in reciprocal space with a magnonscattering reservoir, Nat. Commun. 14, 3954 (2023).
[24] J. A. Schneeloch, Y. Tao, Y. Cheng, L. Daemen, G. Xu,
Q. Zhang, and D. Louca, Gapless Dirac magnons in
CrCl3 , npc Quantum Mater. 7, 1 (2022).

[25] L. Chen, J.-H. Chung, B. Gao, T. Chen, M. B. Stone,
A. I. Kolesnikov, Q. Huang, and P. Dai, Topological Spin Excitations in Honeycomb Ferromagnet CrI3 ,
Phys. Rev. X 8, 041028 (2018).
[26] S. X. M. Riberolles, T. J. Slade, T. Han, B. Li, D. L.
Abernathy, P. C. Canfield, B. G. Ueland, P. P. Orth,
L. Ke, and R. J. McQueeney, Chiral and flat-band
magnetic quasiparticles in ferromagnetic and metallic
kagome layers, Nat. Commun. 15, 1592 (2024).
[27] T. F. Krauss, R. M. D. L. Rue, and S. Brand, Twodimensional photonic-bandgap structures operating at
near-infrared wavelengths, Nature 383, 699 (1996).
[28] J. D. Joannopoulos, P. R. Villeneuve, and S. Fan, Photonic crystals, Solid State Commun. 102, 165 (1997).
[29] S. A. Nikitov, P. Tailhades, and C. S. Tsai, Spin waves
in periodic magnetic structures—magnonic crystals, J.
Magn. Magn. Mater. 236, 320 (2001).
[30] A. V. Chumak, T. Neumann, A. A. Serga, B. Hillebrands, and M. P. Kostylev, A current-controlled, dynamic magnonic crystal, J. Phys. D: Appl. Phys. 42,
205005 (2009).
[31] Z. K. Wang, V. L. Zhang, H. S. Lim, S. C. Ng, M. H.
Kuok, S. Jain, and A. O. Adeyeye, Nanostructured
Magnonic Crystals with Size-Tunable Bandgaps, ACS
Nano 4, 643 (2010).
[32] S. Tacchi, F. Montoncello, M. Madami, G. Gubbiotti,
G. Carlotti, L. Giovannini, R. Zivieri, F. Nizzoli, S. Jain,
A. O. Adeyeye, and N. Singh, Band Diagram of Spin
Waves in a Two-Dimensional Magnonic Crystal, Phys.
Rev. Lett. 107, 127204 (2011).
[33] A. V. Chumak, A. A. Serga, and B. Hillebrands,
Magnonic crystals for data processing, J. Phys. D: Appl.
Phys. 50, 244001 (2017).
[34] L. Landau and E. Lifshits, On the theory of the dispersion of magnetic permeability in ferromagnetic bodies,
Phys. Zeitsch. der Sow. 8, 153 (1935).
[35] T. Gilbert, A phenomenological theory of damping in
ferromagnetic materials, IEEE Trans. Magn. 40, 3443
(2004).
[36] W. F. Brown, Micromagnetics. (Interscience Publishers,
New York, 1963) open Library ID: OL5886173M.
[37] A. Vansteenkiste, J. Leliaert, M. Dvornik, M. Helsen,
F. Garcia-Sanchez, and B. Van Waeyenberge, The design and verification of MuMax3, AIP Adv. 4, 107133
(2014).
[38] See Supplemental Material at [URL] for extended calculations, details, justifications, and explanations.
[39] H. Puszkarski and M. Krawczyk, Magnonic Crystals —
the Magnetic Counterpart of Photonic Crystals, Solid
State Sci. 94, 125 (2003).
[40] M. Krawczyk, S. Mamica, M. Mruczkiewicz, J. W.
Klos, S. Tacchi, M. Madami, G. Gubbiotti, G. Duerr,
and D. Grundler, Magnonic band structures in twodimensional bi-component magnonic crystals with inplane magnetization, J. Phys. D: Appl. Phys. 46, 495003
(2013).
[41] G. Centala and J. W. Klos, Compact localized states in
magnonic Lieb lattices, Sci. Rep. 13, 12676 (2023).
[42] H. Yang, G. Yun, and Y. Cao, Flatbands of spin waves
in two-dimensional magnonic crystals with kagome lattices, J. Appl. Phys. 137, 113904 (2025).
[43] S. Neusser, G. Duerr, H. G. Bauer, S. Tacchi,
M. Madami, G. Woltersdorf, G. Gubbiotti, C. H. Back,
and D. Grundler, Anisotropic Propagation and Damp-

## PDF page 13

13
ing of Spin Waves in a Nanopatterned Antidot Lattice,
Phys. Rev. Lett. 105, 067208 (2010).
[44] H. Ulrichs, B. Lenk, and M. Münzenberg, Magnonic
spin-wave modes in CoFeB antidot lattices, Appl. Phys
Lett. 97, 092506 (2010).
[45] R. Bali, M. Kostylev, D. Tripathy, A. O. Adeyeye, and
S. Samarin, High-symmetry magnonic modes in antidot
lattices magnetized perpendicular to the lattice plane,
Phys. Rev. B 85, 104414 (2012).
[46] F. Groß, M. Zelent, A. Gangwar, S. Mamica,
P. Gruszecki, M. Werner, G. Schütz, M. Weigand, E. J.
Goering, C. H. Back, M. Krawczyk, and J. Gräfe, Phase
resolved observation of spin wave modes in antidot lattices, Appl. Phys Lett. 118, 232403 (2021).
[47] H. Wang, M. Madami, J. Chen, H. Jia, Y. Zhang,
R. Yuan, Y. Wang, W. He, L. Sheng, Y. Zhang, J. Wang,
S. Liu, K. Shen, G. Yu, X. Han, D. Yu, J.-P. Ansermet,
G. Gubbiotti, and H. Yu, Observation of Spin-Wave
Moiré Edge and Cavity Modes in Twisted Magnetic Lattices, Phys. Rev. X 13, 021016 (2023).
[48] Y. Qi, T. Brintlinger, and J. Cumings, Direct observation of the ice rule in an artificial kagome spin ice, Phys.
Rev. B 77, 094418 (2008).
[49] J. C. Gartside, D. M. Arroo, D. M. Burn, V. L. Bemmer,
A. Moskalenko, L. F. Cohen, and W. R. Branford, Realization of ground state in artificial kagome spin ice via
topological defect-driven magnetic writing, Nat. Nanotech. 13, 53 (2018).
[50] D. D. Stancil and A. Prabhakar, Magnetostatic Modes,
in Spin Waves: Theory and Applications (Springer US,
Boston, MA, 2009) pp. 139–168.
[51] L. Landau, E. Lifshits, and L. Pitaevskii, Magnetism,
in Statistical Physics Part 2, Course of Theoretical
Physics, Vol. 9 (Pergamon Press, 1958) p. 287.
[52] C. Herring and C. Kittel, On the Theory of Spin Waves
in Ferromagnetic Media, Phys. Rev. 81, 869 (1951).
[53] J. Lim, A. Garg, and J. B. Ketterson, Ferromagnetic
Resonance Modes in the Exchange-Dominated Limit in
Cylinders of Finite Length, Phys. Rev. Appl. 16, 064007
(2021).
[54] J. Feilhauer, M. Zelent, Z. Zhang, J. Christensen, and
M. Mruczkiewicz, Unidirectional spin-wave edge modes
in magnonic crystal, APL Mater. 11, 021104 (2023).
[55] S. O. Demokritov, V. E. Demidov, O. Dzyapko, G. A.
Melkov, A. A. Serga, B. Hillebrands, and A. N.
Slavin, Bose–Einstein condensation of quasi-equilibrium
magnons at room temperature under pumping, Nature
443, 430 (2006).
[56] V. Tiberkevich, I. V. Borisenko, P. Nowik-Boltyk, V. E.
Demidov, A. B. Rinkevich, S. O. Demokritov, and A. N.
Slavin, Excitation of coherent second sound waves in a
dense magnon gas, Sci. Rep. 9, 9063 (2019).
[57] Y. Wang, H. Wu, G. T. McCandless, J. Y. Chan, and
M. N. Ali, Quantum states and intertwining phases in
kagome materials, Nat. Rev. Phys. 5, 635 (2023).
[58] C. Wu, D. Bergman, L. Balents, and S. Das Sarma, Flat
Bands and Wigner Crystallization in the Honeycomb
Optical Lattice, Phys. Rev. Lett. 99, 070401 (2007).
[59] J.-W. Rhim, , and B.-J. Yang, Singular flat bands, Adv.
Phs. X 6, 1901606 (2021).
[60] C. Chen, J. Zheng, R. Yu, S. Sankar, K. T. Law, H. C.
Po, and B. Jäck, Visualizing the localized electrons of a
kagome flat band, Phys. Rev. Res. 5, 043269 (2023).

[61] D. Multer, J.-X. Yin, M. S. Hossain, X. Yang, B. C.
Sales, H. Miao, W. R. Meier, Y.-X. Jiang, Y. Xie,
P. Dai, J. Liu, H. Deng, H. Lei, B. Lian, and M. Zahid Hasan, Imaging real-space flat band localization in
kagome magnet FeSn, Commun. Mater. 4, 1 (2023).
[62] R. Chisnell, J. Helton, D. Freedman, D. Singh, R. Bewley, D. Nocera, and Y. Lee, Topological Magnon Bands
in a Kagome Lattice Ferromagnet, Phys. Rev. Lett. 115,
147201 (2015).
[63] D. D. Stancil and A. Prabhakar, Quantum Theory of
Spin Waves, in Spin Waves: Theory and Applications
(Springer US, Boston, MA, 2009) pp. 33–66.
[64] T. Holstein and H. Primakoff, Field Dependence of
the Intrinsic Domain Magnetization of a Ferromagnet,
Phys. Rev. 58, 1098 (1940).
[65] E. Iacocca, S. Gliga, R. L. Stamps, and O. Heinonen,
Reconfigurable wave band structure of an artificial
square ice, Phys. Rev. B 93, 134420 (2016).
[66] R. Shindou, J.-i. Ohe, R. Matsumoto, S. Murakami, and
E. Saitoh, Chiral spin-wave edge modes in dipolar magnetic thin films, Phys. Rev. B 87, 174402 (2013).
[67] S.
Coh
and
D.
Vanderbilt,
Python
Tight
Binding
(PythTB)
(2022),
zenodo:
https://doi.org/10.5281/zenodo.12721315.
[68] M. Milićević, G. Montambaux, T. Ozawa, O. Jamadi, B. Real, I. Sagnes, A. Lemaı̂tre, L. Le Gratiet,
A. Harouri, J. Bloch, and A. Amo, Type-III and Tilted
Dirac Cones Emerging from Flat Bands in Photonic Orbital Graphene, Phys. Rev. X 9, 031010 (2019).
[69] F. Gao, Y.-G. Peng, X. Xiang, Q.-L. Sun, C. Zheng,
B. Li, and X.-F. Zhu, Visualization of orbital twig edge
states in phononic graphene lattices, Phys. Rev. Appl.
21, 044005 (2024).
[70] C. Wu and S. Das Sarma, px,y -orbital counterpart of
graphene: Cold atoms in the honeycomb optical lattice,
Phys. Rev. B 77, 235107 (2008).
[71] M. Polini, F. Guinea, M. Lewenstein, H. C. Manoharan, and V. Pellegrini, Artificial honeycomb lattices for
electrons, atoms and photons, Nat. Nanotechnol. 8, 625
(2013).
[72] F. Mangussi, M. Milićević, I. Sagnes, L. L. Gratiet,
A. Harouri, A. Lemaı̂tre, J. Bloch, A. Amo, and G. Usaj,
Multi-orbital tight binding model for cavity-polariton
lattices, Journal of Physics: Condensed Matter 32,
315402 (2020).
[73] Y. Ding, Y. Peng, Y. Zhu, X. Fan, J. Yang, B. Liang,
X. Zhu, X. Wan, and J. Cheng, Experimental Demonstration of Acoustic Chern Insulators, Phys. Rev. Lett
122, 014302 (2019).
[74] G. Giovannetti, P. A. Khomyakov, G. Brocks, P. J.
Kelly, and J. van den Brink, Substrate-induced band
gap in graphene on hexagonal boron nitride: Ab initio
density functional calculations, Phys. Rev. B 76, 073103
(2007).
[75] J. Xue, J. Sanchez-Yamagishi, D. Bulmash, P. Jacquod,
A. Deshpande, K. Watanabe, T. Taniguchi, P. JarilloHerrero, and B. J. LeRoy, Scanning tunnelling microscopy and spectroscopy of ultra-flat graphene on
hexagonal boron nitride, Nat. Mater. 10, 282 (2011).
[76] F. Zhang, A. H. MacDonald, and E. J. Mele, Valley
Chern numbers and boundary modes in gapped bilayer
graphene, Proc. Natl. Acad. Sci. U.S.A. 110, 10546
(2013).

## PDF page 14

14
[77] G. W. Semenoff, V. Semenoff, and F. Zhou, Domain
Walls in Gapped Graphene, Phys. Rev. Lett 101,
087204 (2008).
[78] J. Jung, F. Zhang, Z. Qiao, and A. H. MacDonald,
Valley-Hall kink and edge states in multilayer graphene,
Phys. Rev. B 84, 075418 (2011).
[79] R. Jackiw and C. Rebbi, Solitons with fermion number
1
, Phys. Rev. D 13, 3398 (1976).
2
[80] K. W. Lee and C. E. Lee, Gapped edge states and quantum valley Hall effect in a planar honeycomb monolayer of group III–V binary compounds of the form BX
(X = N, P, and As), Journal of Physics and Chemistry
of Solids 170, 110946 (2022).
[81] H. Zhu, T.-W. Liu, and F. Semperlotti, Design and
experimental observation of valley-Hall edge states in
diatomic-graphene-like elastic waveguides, Phys. Rev.
B 97, 174301 (2018).
[82] K. W. Lee and C. E. Lee, Quantum valley Hall effect in
wide-gap semiconductor SiC monolayer, Scientific Reports 10, 5044 (2020).
[83] J. Lu, C. Qiu, L. Ye, X. Fan, M. Ke, F. Zhang, and
Z. Liu, Observation of topological valley transport of
sound in sonic crystals, Nat. Phys. 13, 369 (2017).
[84] Y. Yang, Z. Yang, and B. Zhang, Acoustic valley edge
states in a graphene-like resonator system, J. Appl.
Phys. 123, 091713 (2018).
[85] J.-Q. Wang, Z.-D. Zhang, S.-Y. Yu, H. Ge, K.-F. Liu,
T. Wu, X.-C. Sun, L. Liu, H.-Y. Chen, C. He, M.-H.
Lu, and Y.-F. Chen, Extended topological valley-locked
surface acoustic waves, Nat. Commun. 13, 1324 (2022).
[86] J. Noh, S. Huang, K. P. Chen, and M. C. Rechtsman,
Observation of Photonic Topological Valley Hall Edge
States, Phys. Rev. Lett. 120, 063902 (2018).
[87] Z. Zhang, Y. Cheng, and X. Liu, Achieving acoustic topological valley-Hall states by modulating the
subwavelength honeycomb lattice, Sci. Rep. 8, 16784
(2018).
[88] H. Wang, G. Tang, Y. He, Z. Wang, X. Li, L. Sun,
Y. Zhang, L. Yuan, J. Dong, and Y. Su, Ultracompact topological photonic switch based on valley-vortexenhanced high-efficiency phase shift, Light Sci. Appl.
11, 292 (2022).
[89] K. Funayama, K. Yatsugi, and H. Iizuka, Quantum valley Hall effect-based topological boundaries for
frequency-dependent and -independent mode energy
profiles, Commun. Phys. 7, 1 (2024).
[90] W. Yao, S. A. Yang, and Q. Niu, Edge States in
Graphene: From Gapped Flat-Band to Gapless Chiral
Modes, Phys. Rev. Lett. 102, 096801 (2009).
[91] R. Hidalgo-Sacoto, R. I. Gonzalez, E. E. Vogel, S. Allende, J. D. Mella, C. Cardenas, R. E. Troncoso, and
F. Munoz, Magnon valley Hall effect in CrI3 -based van
der Waals heterostructures, Phys. Rev. B 101, 205425
(2020).
[92] J. R. Schaibley, H. Yu, G. Clark, P. Rivera, J. S. Ross,
K. L. Seyler, W. Yao, and X. Xu, Valleytronics in 2D
materials, Nat. Rev. Mater. 1, 1 (2016).
[93] R. Shindou, R. Matsumoto, S. Murakami, and J.-i. Ohe,
Topological chiral magnonic edge mode in a magnonic
crystal, Phys. Rev. B 87, 174427 (2013).

[94] M. Hafezi, S. Mittal, J. Fan, A. Migdall, and J. M. Taylor, Imaging topological edge states in silicon photonics,
Nat. Photon. 7, 1001 (2013).
[95] B. B. Maranville, R. D. McMichael, S. A. Kim, W. L.
Johnson, C. A. Ross, and J. Y. Cheng, Characterization
of magnetic properties at edges by edge-mode dynamics,
J. Appl. Phys. 99, 08C703 (2006).
[96] R. D. McMichael and B. B. Maranville, Edge saturation
fields and dynamic edge modes in ideal and nonideal
magnetic film edges, Phys. Rev. B 74, 024424 (2006).
[97] Y. Liang, G. Yun, H. Yang, N. Bai, and Y. Cao, Dirac
points and flat bands in two-dimensional magnonic crystals with honeycomb–kagome structure, AIP Adv. 14,
035242 (2024).
[98] C. Dubs, O. Surzhenko, R. Thomas, J. Osten, T. Schneider, K. Lenz, J. Grenzer, R. Hübner, and E. Wendler,
Low damping and microstructural perfection of sub40nm-thin yttrium iron garnet films grown by liquid
phase epitaxy, Phys. Rev. Materials 4, 024416 (2020).
[99] S. Li, W. Zhang, J. Ding, J. E. Pearson, V. Novosad, and
A. Hoffmann, Epitaxial patterning of nanometer-thick
Y3 Fe5 O12 films with low magnetic damping, Nanoscale
8, 388 (2015).
[100] H. Liu, G. Sethi, S. Meng, and F. Liu, Orbital design of
flat bands in non-line-graph lattices via line-graph wave
functions, Phys. Rev. B 105, 085128 (2022).
[101] J. Wang, H. Wang, J. Chen, W. Legrand, P. Chen,
L. Sheng, J. Xia, G. Lan, Y. Zhang, R. Yuan, J. Dong,
X. Han, J.-P. Ansermet, and H. Yu, Broad-wave-vector
spin pumping of flat-band magnons, Phys. Rev. Appl.
21, 044024 (2024).
[102] V. M. Pereira and A. H. Castro Neto, Strain Engineering of Graphene’s Electronic Structure, Phys. Rev. Lett.
103, 046801 (2009).
[103] D.-H. Kang, H. Sun, M. Luo, K. Lu, M. Chen, Y. Kim,
Y. Jung, X. Gao, S. J. Parluhutan, J. Ge, S. W. Koh,
D. Giovanni, T. C. Sum, Q. J. Wang, H. Li, and D. Nam,
Pseudo-magnetic field-induced slow carrier dynamics in
periodically strained graphene, Nat. Commun. 12, 5087
(2021).
[104] J. Sun, H. Guo, and S. Feng, Magnon Landau levels in
the strained antiferromagnetic honeycomb nanoribbons,
Phys. Rev. Res. 3, 043223 (2021).
[105] B. Wei, J.-J. Zhu, Y. Song, and K. Chang, Strainengineered magnon states in two-dimensional ferromagnetic monolayers, Phys. Rev. Res. 6, 013210 (2024).
[106] O. Jamadi, E. Rozas, G. Salerno, M. Milićević,
T. Ozawa, I. Sagnes, A. Lemaı̂tre, L. Le Gratiet,
A. Harouri, I. Carusotto, J. Bloch, and A. Amo, Direct observation of photonic Landau levels and helical
edge states in strained honeycomb lattices, Light Sci.
Appl. 9, 144 (2020).
[107] R. O. Serha, K. H. McAllister, F. Majcen, S. Knauer,
T. Reimann, C. Dubs, G. A. Melkov, A. A. Serga,
V. S. Tyberkevych, A. V. Chumak, and D. A. Bozhko,
Ultra-long-living magnons in the quantum limit (2025),
arXiv:2505.22773 [cond-mat].
[108] B. Kaman, J. Lim, Y. Liu, and A. Hoffmann, Code for
’emulating 2d materials with magnons’, available at the
Illinois Databank.
