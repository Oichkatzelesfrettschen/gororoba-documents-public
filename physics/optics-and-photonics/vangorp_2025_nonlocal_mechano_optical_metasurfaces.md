Source: https://doi.org/10.1021/acsphotonics.5c01385
PDF sha256: fa3db13186e1d18ea08bbf76c2fc96567010e5144ff658467d73a0516753eedd
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of vangorp_2025_nonlocal_mechano_optical_metasurfaces.pdf

Transcription of `vangorp_2025_nonlocal_mechano_optical_metasurfaces.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

UvA-DARE (Digital Academic Repository)

Nonlocal Mechano-Optical Metasurfaces
van Gorp, Freek; Liu, Wenfeng; Coulais, Corentin; van de Groep, Jorik
DOI
10.1021/acsphotonics.5c01385
Publication date
2025
Document Version
Final published version
Published in
ACS Photonics
License
CC BY
Link to publication
Citation for published version (APA):
van Gorp, F., Liu, W., Coulais, C., & van de Groep, J. (2025). Nonlocal Mechano-Optical
Metasurfaces. ACS Photonics, 12(11), 5978-5984.
https://doi.org/10.1021/acsphotonics.5c01385

General rights
It is not permitted to download or to forward/distribute the text or part of it without the consent of the author(s)
and/or copyright holder(s), other than for strictly personal, individual use, unless the work is under an open
content license (like Creative Commons).
Disclaimer/Complaints regulations
If you believe that digital publication of certain material infringes any of your rights or (privacy) interests, please
let the Library know, stating your reasons. In case of a legitimate complaint, the Library will make the material
inaccessible and/or remove it from the website. Please Ask the Library: https://uba.uva.nl/en/contact, or a letter
to: Library of the University of Amsterdam, Secretariat, P.O. Box 19185, 1000 GD Amsterdam, The Netherlands.
You will be contacted as soon as possible.
UvA-DARE is a service provided by the library of the University of Amsterdam (https://dare.uva.nl)
Download date:11 Mar 2026

## PDF page 2

This article is licensed under CC-BY 4.0

pubs.acs.org/journal/apchd5

Article

Nonlocal Mechano-Optical Metasurfaces
Freek van Gorp, Wenfeng Liu, Corentin Coulais, and Jorik van de Groep*
Cite This: ACS Photonics 2025, 12, 5978−5984

Downloaded via UNIV AMSTERDAM on March 4, 2026 at 16:05:35 (UTC).
See https://pubs.acs.org/sharingguidelines for options on how to legitimately share published articles.

ACCESS

Metrics & More

Read Online

Article Recommendations

* Supporting Information
sı

ABSTRACT: Tunable metasurfaces enable active and on-demand
control over optical wavefronts through the reconfigurable
scattering of resonant nanostructures. Here, we combine novel
insights inspired by mechanical metamaterials with the unique
sensitivity of nonlocal optical resonances to interparticle distances
to achieve giant tunability in mechano-optical metasurfaces where
the mechanical metamaterial and optical metasurfaces are
integrated in a single nanopatterned material. In a first design,
judiciously engineered cuts in a flexible substrate enable large,
strain-induced extension of the interparticle spacing, tuning a highquality-factor resonance in a silicon nanoparticle array across a very
broad spectral range. In a second design, we eliminate the substrate
and demonstrate a nanopatterned silicon membrane that
simultaneously functions as a mechanical metamaterial and an optical metasurface with large tunability. Our results highlight a
promising route toward active metasurfaces, with potential applications in tunable filters, reconfigurable lenses, and dynamic
wavefront shaping.
KEYWORDS: nonlocal metasurface, quasi-BIC, mechanical tuning, kirigami, multifunctional metamaterial

■

INTRODUCTION
Nanophotonic metasurfaces employ engineered arrangements
of interacting optical resonators to steer,1 filter,2 and shape
optical wavefronts3,4 in ultracompact optical coatings. The
optical function of such passive metasurfaces is imprinted in
the nanoscale geometry and, therefore, challenging to
manipulate postfabrication. Tunable metasurfaces enable active
and on-demand control over optical wavefronts through the
reconfigurable scattering of resonant nanostructures. This can
be achieved by active manipulation of the optical properties of
the resonant nanoparticles or its dielectric surrounding, for
example using phase-change materials,5−7 thermal effects,8,9
electrostatic doping of metal-oxides,10−13 or electrochemical
intercalation of electrochromic materials.14 Many of these
approaches exhibit considerable potential; however, such
tuning remains remarkably challenging in the visible spectral
range, as the refractive index of photonic materials is inherently
difficult to manipulate at optical frequencies.
A promising alternative approach is to employ mechanical
manipulation of the nanoparticles, where the far-field
interference of the locally scattered fields is effectively
manipulated through changes in the interparticle spacing.
Conventionally, such mechanical tuning of metasurfaces is
achieved through relatively simple methods, such as stretching
flexible substrates15−20 or employing out-of-plane deformations via MEMS technology.21−23 Although promising,
metasurface tunability remains limited by the rudimentary
mechanical manipulations of simple stretching and bending.
© 2025 The Authors. Published by
American Chemical Society

Recently, mechanical metamaterials have emerged as a novel
method to control a material’s mechanical properties through
their internal structure. Using the careful geometric design of
compliant hinges and rotating elements,24,25 these metamaterials can combine low density with high strength and energy
dissipation,26,27 perform computation,28,29 and exhibit advanced shape-morphing capabilities.25,30−37 Compared to
simple stretching and bending, these mechanical metamaterials
offer a distinct advantage for optical wavefront shaping by
providing unique degrees of freedom through the internal
rotations of their constituent building blocks, enabling more
intricate and precise control over the system’s geometry.38
While initial demonstrations of light manipulation with
metamaterial platforms have shown significant potential,39−42
and more recently at GHz frequencies using localized
resonances combined with Pancharatnam−Berry phase control,43 these have been restricted to macroscale unit cells and
operational frequencies in the GHz−THz regime, rely on
resonant particles supported by mechanically limited substrates, and employ only localized resonances.
Received: June 17, 2025
Revised: October 15, 2025
Accepted: October 15, 2025
Published: October 27, 2025

5978

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 3

ACS Photonics

pubs.acs.org/journal/apchd5

Article

Figure 1. Mechanical deformation and tunable optical response of an idealized kirigami metasurface. (a−c) Schematics of 3 × 3 unit cell sections of
the kirigami metasurface under increasing levels of strain: minimal strain (θ = 1°) (a), medium strain (θ = 15°) (b), and large strain (θ = 44°) (c).
Each elliptical nanoparticle is centered on a rectangular tile measuring 250 × 400 nm. (d) With increasing strain in the x-direction, the tiles�and
thus the particles�are rotated by an angle θ (solid, blue) and displaced, leading to changes in the interparticle spacing (dashed, orange). (e)
Reflectance spectra for the arrays shown in (a−c), illustrating the giant tunability of the high-quality-factor resonant peak across the visible
spectrum from green (∼500 nm) through yellow (∼580 nm) to red (∼650 nm), with zoomed-in sections near these wavelengths to highlight the
Fano line shape. (f) Strain dependence of the resonance wavelength (blue triangles) and quality factor Q (orange circles).

Here, we address these limitations by combining the unique
sensitivity of nonlocal metasurfaces44−46 to interparticle
spacing and orientation with the large internal rotations
offered by flexible mechanical metamaterials24,25,32,47−50 to
demonstrate a nanopatterned membrane that simultaneously
functions as an optical metasurface and a mechanical
metamaterial�a nonlocal mechano-optical metasurface. We
exploit these large internal rotations to change the distances
and angles between resonant nanoparticles on the fly, which in
turn allows us to dynamically tune the resonance condition and
associated optical filtering properties of the optical metasurface
and to showcase the synergy between mechanical and optical
functionalities in a single platform. Our approach augments the
toolbox of reconfigurable metasurfaces and opens avenues for
the synergistic design of mechanical and optical functionalities.

between the resonators can be obtained on demand by simply
stretching the kirigami Metasurface. In the corresponding
optical simulations, we treat the substrate as fictitious (i.e., n =
1) and use a constant, lossless refractive index for silicon.
Giant Tunability. To test whether stretching the kirigami
leads to notable changes in the optical response, we use finiteelement frequency-domain simulations with a normally
incident x-polarized plane wave to calculate the reflection
spectrum for varying metasurface geometries (see the Methods
in SI). The reflection spectrum of the kirigami metasurface
(Figure 1e) reveals a single resonant peak with three
remarkable features. First, as the kirigami metasurface is
stretched, the spectral position is tuned across the spectrum
from 500 to 650 nm (Figure 1f) due to the strong dependence
of the q-BIC mode on the interparticle spacing. This range
corresponds to 328× the resonant line width. This giant tuning
range is in stark contrast to the relatively small tunability of
most existing platforms for active metasurfaces.
Second, the resonance quality factor decreases from
theoretically arbitrarily large for infinitesimally small deformation to a minimum of Q = 1334 at θ = 24° (Figure 1f).
Interestingly, this decrease is less pronounced than the Q ∝
sin−2θ that is characteristic of the perturbation of q-BIC modal
symmetries.55 We attribute this to the changes in particle
spacing associated with the particle rotation within the kirigami
metasurface (See SI). Third, the maximum spectral shift is
achieved for θmax = 44°, which shows an unexpected
discrepancy with the 58° that provides the largest displacement
based on the kirigami design.
Quasi-Bound State in the Continuum. To elucidate the
interplay between internal rotations and nonlocal resonances,
we present in Figure 2 the electric field lines (arrows) and the
intensity enhancement (color) at resonance for three levels of
strain (ε; the unstretched metasurface (ε = 0, Figure 2a),
moderate strain (ε = 0.38 Figure 2b), and large strain (ε = 0.83

■

RESULTS
Idealized Kirigami Metasurface. We first introduce a
reconfigurable Metasurface made from resonant nanoparticles
on a kirigami substrate that exhibits a tunable quasi-bound
state in the continuum (q-BIC) with a high quality factor (Q)
by simple stretching (Figure 1). Unlike conventional
stretchable materials such as polydimethylsiloxane
(PDMS),51 judiciously placed cuts in the kirigami substrate
enable engineered mechanical deformations and thereby
unusually large strain and internal rotations (Figure 1a−c).52,53
The kirigami is decorated by an array of nanophotonic
resonators54,55�each elliptical resonator is placed in the
center of each rectangular tile. Crucially, the periodicity of the
Metasurface and the kirigami substrate must be commensurate.
When the kirigami is strained along its x-axis, the angle θ
(Figure 1c) varies from 0 to ∼58°. Importantly, the
interparticle distance (pitch) also increases linearly with
applied strain, reaching up to 89% elongation (Figure 1d).
As such, a wide range of relative spacings and orientations
5979

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 4

ACS Photonics

pubs.acs.org/journal/apchd5

Article

Resonant coupling to this q-BIC mode gives rise to strong field
enhancements in the plane of the metasurface (|E|2 ≫ |E0|2).
Interestingly, for large strain, the effective dipole orientation
within the individual resonant nanoparticles is no longer
aligned with the long axis of the ellipsoidal particle, but is
reoriented toward smaller θ (Figure 2c). This intuitively
explains why the maximum spectral shift does not align with
the maximum mechanical displacement. For θ = 90°, the
structure returns to a symmetry-protected BIC where the
dipoles align with the y-axis again (Figure S4), albeit at a lower
resonance wavelength than the original BIC (Figure 1f).
Further evidence for the collective, nonlocal nature of this
mode is provided in the Supporting Information, where we
show that the resonance wavelength follows a parabolic
dispersion as a function of k∥ (Figure S6) and that 1/Q scales
with (k∥/k0)2 (Figure S7), consistent with the behavior
expected for a q-BIC.
Beam-Linked Metasurface. So far, we have explored the
mechano-optical response of an “ideal” kirigami metasurface
where the substrate was fictitious (i.e., n = 1) and the refractive
index of the silicon was constant and lossless. In the following,
we aim to address these physical limitations in a second design:
we include the dispersive and lossy optical constants of realistic
silicon, and the particles are mechanically supported. Crucially,
our design is composed of a nanopatterned 50 nm-thick silicon
membrane that simultaneously functions as a mechanical
metamaterial and as an optical metasurface (Figure 3a−c). To
this end, the optically resonant nanoparticles are connected by
carefully designed 10 nm wide beams. We optimize the shape
of the beams such that (i) they bend to emulate the counterrotation mechanism of the rotating rectangle as closely as
possible (see SI for a detailed discussion); (ii) the stress
remains below the failure limit when the metasurface is
stretched to a maximum of 60° (Figure 3e). This is enabled by

Figure 2. Electric field intensity profiles, normalized to the source
intensity, for the idealized kirigami metasurface. Gray (arrow) lines
indicate the electric field lines in the plane. Overlaid white arrows
indicate the effective dipole moments. (a) The undeformed state (θ =
0°) displays a negligible field enhancement. (b) Small strain condition
(θ = 15°) and (c) large strain condition (θ = 44°) show enhanced
localized field intensities.

Figure 2c). The individual ellipsoidal particles support a strong
electric dipolar Mie resonance, with the dipole moment
(anti)parallel to the major axis. However, for the unstretched
situation, the modal symmetry of the unit cell inhibits incident
light from coupling to this pure BIC, and the dipolar field lines
are not observable (Figure 2a). The resulting field intensity in
the plane of the metasurface is not significantly enhanced
beyond the incident intensity: |E|2 < 10 |E0|2. For nonzero
stretch ratios, the unit cell expands, the particles rotate, and the
modal symmetry of the unit cell is perturbed. For small angles
(Figure 2b), the electric field lines of the dipolar Mie modes
are clearly observable in the individual particles, with strong
field intensities concentrated at the particle tips. Careful
evaluation of the field lines shows that within a four-particle
unit cell, neighboring dipole moments (white arrows guide the
eye) are oriented antiparallel with a relative angle close to θ.

Figure 3. Mechanical deformation and tunable optical response of the beam-linked metasurface (a−c) Schematics of 2 × 2 unit cell sections of the
kirigami-inspired metasurface: the initial undeformed state (a) shows no rotation of the elliptical nanoparticles, while moderate strain (θ = 10°)
(b), and large strain (θ = 38°) (c) show increasing rotation and interparticle spacing. (d) Particle rotation angle θ (solid, blue) and displacement
(dashed, orange) as functions of strain in the x-direction. (e) Simulated stress distribution for θ = 60°, showing strong localization of the stress at
the beams. (f) Reflectance spectra for the arrays shown in parts (a−c), illustrating the large tunability of the resonant peak across the visible
spectrum from yellow (∼580 nm) through orange (∼610 nm) to red (∼640 nm). (g) Strain-dependence of the resonance wavelength (blue
triangles) and quality factor Q (orange circles), with a notable overall decrease in comparison to Figure 1f.
5980

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 5

ACS Photonics

pubs.acs.org/journal/apchd5

Article

for θ = 0° (a), θ = 30° (b), and θ = 60° (c). Indeed, despite the
absence of particle rotation for θ = 0° (Figure 4a), the field
intensity is >200, the incident field as a result of the formation
of nanoscale hot spots at the contact points with the beams.
Also, for nonzero θ, the contact points of the beams with the
particles form sharp corners that perturb the modal field profile
and give rise to strongly localized hot spots due to the required
continuity of the displacement field D = ϵE.

the notable enhancement of the strength of silicon at the
nanoscale.56 In practice, the attainable fracture strength of
single-crystal silicon nanobeams depends on the morphology.
In particular, sidewall surface roughness reduces the nominal
fracture strength from 20 GPa to values in the 12−16 GPa
range.57,58 These values still exceed the maximum stresses
obtained in our simulations (<10 GPa at θ = 60°), and further
reduction of the operational strain would bring stresses well
below even the conservative strength estimates. (iii) they
minimally affect the optical resonance of the nanoparticles.
Analogous to the ideal design (Figure 1), applying in-plane
strain initiates a predesigned mechanical deformation of the
particle’s angle and interparticle spacing (Figure 3d). Just as for
the idealized kirigami metasurface, the beam-linked metasurface’s interparticle spacing is directly proportional to the
system strain. The particle rotation, however, is slightly
increased over the relevant strain range in the beam-linked
version. To assess the mechanical stability of the design, we
perform simulations of the structural deformation and map the
maximum stress throughout the unit cell (Figure 3e),
confirming the mechanical stability under strain.
The introduction of optical damping and constrained
mechanical deformations impacts the optical response in four
distinct manners: (i) The spectral tunability of the resonance is
reduced to 580−640 nm (Figure 3f,g). Despite being notably
smaller than for the idealized kirigami metasurface, this spectral
shift still corresponds to 4.7 times the largest resonance line
width. (ii) The peak reflection is now limited by optical
absorption and thus no longer reaches unity. (iii) The
associated resonance quality factor is reduced from Q =
1336−∞ to Q = 55−215 (Figure 3g). Although this may seem
as an undesired effect, a finite resonance bandwidth is a
prerequisite, e.g., reflective displays that employ structural
color to provide sufficient optical power within the reflection
peak. (iv) The introduction of the beams perturbs the unit cell
symmetry and already enables weak coupling to the q-BIC
mode for θ = 0°, i.e., the mode is no longer bound (Figure 3f).
This symmetry breaking also occurs for very small initial
rotations or due to imperfections in the array, and therefore
does not significantly affect the tunability. At the same time,
this symmetry breaking by the connecting beams is
unavoidable, as the design uses the internal rotations of the
unit cell to enable larger strain with reduced stress.
To further assess the impact of the nanobeams on the
optical response, Figure 4 shows the field profiles on resonance

■

DISCUSSION
Finite-Size Effects. Boundary conditions are also known to
play a crucial role in mechanical metamaterials and, in
particular, they are known to affect how internal rotations
permeate into the bulk.48 Our beam-linked metasurface does
not escape this rule, and indeed we observe bulging at the
edges, as a result of the nonslip boundary conditions (Figure
5a,b). This leads to a nonhomogeneous interparticle distance
throughout the material, where the unit cells close to the edges
do not stretch as much as the bulk of the metasurface (Figure
5b). The spatial extent of this inhomogeneous deformation is
further quantified by a characteristic length scale * = 1500
nm (3 unit cells) (Figure 5c), extracted from cross sections of
the local strain throughout the 20 unit cells. The inhomogeneous mechanical deformation impacts the overall optical
response of the metasurface. Averaged over the full metasurface, the reflection peak is slightly broader and exhibits a
reduced amplitude (Figure 5d). However, avoiding only the
regions within a distance * from the mechanical clamps will
already retain the optical response of the bulk material (Figure
5d). As such, the finite-size effects within the metasurface
become negligible for all practical purposes.

■

CONCLUSION AND OUTLOOK

In summary, we demonstrate how mechanical deformations in
mechano-optical metasurfaces can tune a nonlocal q-BIC
across the visible spectrum. The nanopatterned silicon
membrane proposed here combines the function of a
mechanical metamaterial and optical metasurfaces in a single
structure and alleviates the need for a supporting substrate.
Beyond resonance peak shifts that are characteristic of
elastomer-mounted/embedded photonic structures, our approach leverages internal rotations to dynamically reorient as
well as reposition scattering particles. This additional degree of
freedom enables not only resonance wavelength tuning but
also active control over the resonance quality factor, providing
a controllable coupling between Q and λ that is inaccessible to
simple stretching substrates. This highlights how mechanical
design can enrich the optical response and control of
metasurfaces. Moreover, this concept opens up opportunities
for multistable metasurfaces, mode switching with possible sign
changes in dispersion, switchable lensing, beam steering, and
polarization control, pointing to a broad class of functionalities
beyond reflective filtering.
Our results pave the way for controlling light fields using
designer mechanics with the prospect of more complex
mechanical deformations and tunable optical functions for
dynamic beam steering and wavefront manipulation beyond
reflective filtering. Looking forward, the experimental demonstration of this concept requires high nanofabrication precision,
typically enabled by electron-beam lithography (EBL),
combined with novel in-plane mechanical actuation mechanisms that ideally capitalize on established MEMS technology.

Figure 4. Electric field intensity (|E|2) profiles, normalized to the
source intensity, for the beam-linked metasurface. Gray (arrow) lines
indicate the electric field lines in the plane. Overlaid white arrows
indicate the effective dipole moments. (a) The undeformed state (θ =
0°) already displays significant field enhancement. (b) Moderate
strain condition (θ = 30°) and (c) high strain condition (θ = 60°)
also show field enhancement.
5981

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 6

ACS Photonics

pubs.acs.org/journal/apchd5

Article

Figure 5. Finite-size effects of the realistic kirigami metasurface. (a) A finite-size metasurface (20 × 20 unit cells) with rigid mechanical handholds
on either side, showing variations in local deformation. The color of the particles indicates deviation in the local strain with respect to the bulk
strain. (b) Zoomed-in view of the local strain distribution near the handholds, highlighting localized deformation. (c) Local strain distributions
across the structure for three strain values, each showing a strain plateau with roughly equal lateral size (between vertical dashed lines). (d)
Comparison of the reflectance spectra between the finite array (solid blue curves) and an infinite array (dashed orange curves), illustrating how
nonuniform stretching affects the overall optical properties, resulting in a reflectance peak with reduced amplitude and larger line width for the
finite array.

Author Contributions

While EBL is not scalable, substrate conformal imprint
lithography (SCIL) offers a scalable alternative with a
demonstrated 6 nm resolution.59 This approach opens up
new opportunities for translating advanced metasurface
concepts into practical large-scale applications.

■

C.C. and J.v.d.G. conceived the concept behind this research.
F.v.G. performed all simulations and associated data analysis
for Figures 1−4. W.L. performed the mechanical simulations
for Figure 5. FvG drafted the manuscript figures. All authors
contributed to the writing of the manuscript.

ASSOCIATED CONTENT

Funding

This work is funded by institutional funding from the Institute
of Physics at the University of Amsterdam. JvdG is also
supported by a Vidi grant (VI.Vidi.203.027) from The
Netherlands Organization for Scientific Research (NWO), as
well as an European Research Council Starting Grant under
grant agreement No. 101116984. C.C. also acknowledges
funding from the European Research Council under Grant
Agreement No. 852587 and from a NWO Vidi grant
(2131313.845).

Data Availability Statement

All data and analysis scripts underlying the figures presented in
this work are freely available in the form of a replication
package at 10.6084/m9.figshare.30350479.
sı Supporting Information
*

The Supporting Information is available free of charge at
https://pubs.acs.org/doi/10.1021/acsphotonics.5c01385.
Detailed simulation methods; BIC quality factor scaling
details; Design of the beam-linked metasurface;
Poisson’s ratio of the kirigami substrate; Y-polarization
BIC and dipole moment alignment with minor axis; qBIC dispersion; Actuation (PDF)

■

Notes

The authors declare no competing financial interest.

■

REFERENCES

(1) Berini, P. Optical beam steering using tunable metasurfaces. ACS
Photonics 2022, 9, 2204−2218.
(2) Wang, S.; Wen, S.; Deng, Z.-L.; Li, X.; Yang, Y. Metasurfacebased solid Poincaré sphere polarizer. Phys. Rev. Lett. 2023, 130,
No. 123801.
(3) Chen, H.-T.; Taylor, A. J.; Yu, N. A review of Metasurfaces:
Physics and Applications. Rep. Prog. Phys. 2016, 79, No. 076401.
(4) Kamali, S. M.; Arbabi, E.; Arbabi, A.; Faraon, A. A review of
dielectric optical metasurfaces for wavefront control. Nanophotonics
2018, 7, 1041−1068.
(5) Howes, A.; Zhu, Z.; Curie, D.; Avila, J. R.; Wheeler, V. D.;
Haglund, R. F.; Valentine, J. G. Optical limiting based on huygens’
metasurfaces. Nano Lett. 2020, 20, 4638−4644.
(6) Zhang, Y.; et al. Electrically reconfigurable non-volatile
metasurface using low-loss optical phase-change material. Nat.
Nanotechnol. 2021, 16, 661−666.
(7) Cotrufo, M.; Sulejman, S. B.; Wesemann, L.; Rahman, M. A.;
Bhaskaran, M.; Roberts, A.; Alù, A. Reconfigurable image processing
metasurfaces with phase-change materials. Nat. Commun. 2024, 15,
4483.

AUTHOR INFORMATION

Corresponding Author

Jorik van de Groep − Institute of Physics, Universiteit van
Amsterdam, 1098 XH Amsterdam, The Netherlands;
orcid.org/0000-0003-3033-8005; Email: j.vandegroep@
uva.nl
Authors

Freek van Gorp − Institute of Physics, Universiteit van
Amsterdam, 1098 XH Amsterdam, The Netherlands
Wenfeng Liu − Institute of Physics, Universiteit van
Amsterdam, 1098 XH Amsterdam, The Netherlands
Corentin Coulais − Institute of Physics, Universiteit van
Amsterdam, 1098 XH Amsterdam, The Netherlands
Complete contact information is available at:
https://pubs.acs.org/10.1021/acsphotonics.5c01385
5982

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 7

ACS Photonics

pubs.acs.org/journal/apchd5

Article

(30) Coulais, C.; Teomy, E.; de Reus, K.; Shokef, Y.; van Hecke, M.
Combinatorial design of textured mechanical metamaterials. Nature
2016, 535, 529−532.
(31) Coulais, C.; Sabbadini, A.; Vink, F.; van Hecke, M. Multi-step
self-guided pathways for shape-changing metamaterials. Nature 2018,
561, 512−515.
(32) Choi, G. P.; Dudte, L. H.; Mahadevan, L. Programming shape
using kirigami tessellations. Nat. Mater. 2019, 18, 999−1004.
(33) Gladman, A. S.; Matsumoto, E. A.; Nuzzo, R. G.; Mahadevan,
L.; Lewis, J. A. Biomimetic 4D printing. Nat. Mater. 2016, 15, 413−
418.
(34) Gao, T.; Bico, J.; Roman, B. Pneumatic cells toward absolute
gaussian morphing. Science 2023, 381, 862−867.
(35) Meeussen, A. S.; van Hecke, M. Multistable sheets with
rewritable patterns for switchable shape-morphing. Nature 2023, 621,
516−520.
(36) Melancon, D.; Gorissen, B.; García-Mora, C. J.; Hoberman, C.;
Bertoldi, K. Multistable inflatable origami structures at the metre
scale. Nature 2021, 592, 545−550.
(37) Smart, C. L.; Pearson, T. G.; Liang, Z.; Lim, M. X.;
Abdelrahman, M. I.; Monticone, F.; Cohen, I.; McEuen, P. L.
Magnetically programmed diffractive robotics. Science 2024, 386,
1031−1037.
(38) Liu, Z.; Du, H.; Li, J.; Lu, L.; Li, Z. Y.; Fang, N. X. Nanokirigami with giant optical chirality. Sci. Adv. 2018, 4, No. eaat4436.
(39) Wang, Y.; Shi, Y.; Li, L.; Zhu, Z.; Liu, M.; Jin, X.; Li, H.; Jiang,
G.; Cui, J.; Ma, S.; He, Q.; Zhou, L.; Sun, S. Electromagnetic
Wavefront Engineering by Switchable and Multifunctional kirigami
Metasurfaces. Nanomaterials 2025, 15, 61.
(40) Xu, L.; Wang, X.; Kim, Y.; Shyu, T. C.; Lyu, J.; Kotov, N. A.
kirigami nanocomposites as wide-angle diffraction gratings. ACS Nano
2016, 10, 6156−6162.
(41) Zheng, Y.; Chen, K.; Yang, W.; Wu, L.; Qu, K.; Zhao, J.; Jiang,
T.; Feng, Y. Kirigami reconfigurable gradient metasurface. Adv. Funct.
Mater. 2021, 32, No. 2107699.
(42) Phon, R.; Jeong, H.; Lim, S. Rotational kirigami tessellation
metasurface for tunable chirality. Adv. Mater. Technol. 2022, 7,
No. 2101706.
(43) Jiang, G.; Wang, Y.; Zhang, Z.; Pan, W.; Chen, Y.; Wang, Y.;
Chen, X.; Song, E.; Huang, G.; He, Q.; et al. Abnormal beam steering
with kirigami reconfigurable metasurfaces. Nat. Commun. 2025, 16,
1660.
(44) Lawrence, M.; Barton, D. R.; Dixon, J.; Song, J.-H.; van de
Groep, J.; Brongersma, M. L.; Dionne, J. A. High quality factor phase
gradient metasurfaces. Nat. Nanotechnol. 2020, 15, 956−961.
(45) Song, J.-H.; van de Groep, J.; Kim, S. J.; Brongersma, M. L.
Non-local metasurfaces for spectrally decoupled wavefront manipulation and eye tracking. Nat. Nanotechnol. 2021, 16, 1224−1230.
(46) Overvig, A.; Alù, A. Diffractive nonlocal metasurfaces. Laser
Photonics Rev. 2022, 16, No. 2100633.
(47) Zhai, Z.; Wu, L.; Jiang, H. Mechanical metamaterials based on
Origami and kirigami. Appl. Phys. Rev. 2021, 8, No. 041319.
(48) Coulais, C.; Kettenis, C.; van Hecke, M. A characteristic length
scale causes anomalous size effects and boundary programmability in
mechanical metamaterials. Nat. Phys. 2018, 14, 40−44.
(49) Lamoureux, A.; Lee, K.; Shlian, M.; Forrest, S. R.; Shtein, M.
Dynamic kirigami structures for integrated solar tracking. Nat.
Commun. 2015, 6, 8092.
(50) Rafsanjani, A.; Bertoldi, K. Buckling-induced kirigami. Phys.
Rev. Lett. 2017, 118, No. 084301.
(51) Akogwu, O.; Kwabi, D.; Midturi, S.; Eleruja, M.; Babatope, B.;
Soboyejo, W. Large strain deformation and cracking of nano-scale
gold films on PDMS substrate. Mater. Sci. Eng. B 2010, 170, 32−40.
(52) Grima, J. N.; Evans, K. E. Auxetic behavior from rotating
squares. Journal of materials science letters 2000, 19, 1563−1565.
(53) Florijn, B.; Coulais, C.; van Hecke, M. Programmable
Mechanical metamaterials. Phys. Rev. Lett. 2014, 113, No. 175503.

(8) Lewi, T.; Evans, H. A.; Butakov, N. A.; Schuller, J. A. Ultrawide
Thermo-optic Tuning of PbTe Meta-Atoms. Nano Lett. 2017, 17,
3940−3945.
(9) Wang, Y.; Landreman, P.; Schoen, D.; Okabe, K.; Marshall, A.;
Celano, U.; Wong, H.-S. P.; Park, J.; Brongersma, M. L. Electrical
tuning of phase-change antennas and metasurfaces. Nat. Nanotechnol.
2021, 16, 667−672.
(10) Li, Y.; van de Groep, J.; Talin, A. A.; Brongersma, M. L.
Dynamic tuning of gap plasmon resonances using a solid-state
electrochromic device. Nano Lett. 2019, 19, 7988−7995.
(11) Huang, Y.-W.; Lee, H. W.; Sokhoyan, R.; Pala, R. A.;
Thyagarajan, K.; Han, S.; Tsai, D. P.; Atwater, H. A. Gate-tunable
conducting oxide metasurfaces. Nano Lett. 2016, 16, 5319−5325.
(12) Siegel, J.; Kim, S.; Fortman, M.; Wan, C.; Kats, M. A.; Hon, P.
W.; Sweatlock, L.; Jang, M. S.; Brar, V. W. Electrostatic steering of
thermal emission with active metasurface control of delocalized
modes. Nat. Commun. 2024, 15, 3376.
(13) Park, J.; Kang, J.-H.; Kim, S. J.; Liu, X.; Brongersma, M. L.
Dynamic reflection phase and polarization control in metasurfaces.
Nano Lett. 2017, 17, 407−413.
(14) Kaissner, R.; Li, J.; Lu, W.; Li, X.; Neubrech, F.; Wang, J.; Liu,
N. Electrochemically controlled metasurfaces with high-contrast
switching at visible frequencies. Sci. Adv. 2021, 7, No. eabd9450.
(15) Ee, H.-S.; Agarwal, R. Tunable metasurface and flat optical
zoom lens on a stretchable substrate. Nano Lett. 2016, 16, 2818−
2823.
(16) Pryce, I. M.; Aydin, K.; Kelaita, Y. A.; Briggs, R. M.; Atwater, H.
A. Highly strained compliant optical metamaterials with large
frequency tunability. Nano Lett. 2010, 10, 4222−4227.
(17) Tseng, M. L.; Yang, J.; Semmlinger, M.; Zhang, C.; Nordlander,
P.; Halas, N. J. Two-dimensional active tuning of an aluminum
plasmonic array for full-spectrum response. Nano Lett. 2017, 17,
6034−6039.
(18) Zhang, C.; Jing, J.; Wu, Y.; Fan, Y.; Yang, W.; Wang, S.; Song,
Q.; Xiao, S. Stretchable all-dielectric metasurfaces with polarizationinsensitive and full-spectrum response. ACS Nano 2020, 14, 1418−
1426.
(19) Shen, Y.; Rinnerbauer, V.; Wang, I.; Stelmakh, V.;
Joannopoulos, J. D.; Soljačić, M. Structural colors from Fano
resonances. ACS Photonics 2015, 2, 27−32.
(20) Guan, X.; Xie, S.; Zhuo, J.; Sun, S. Tunable circular dichroism
supported by quasi-bound states in the continuum of a stretchable
metasurface. Physica B: Condensed Matter 2025, 699, No. 416867.
(21) Zheludev, N. I.; Plum, E. reconfigurable nanomechanical
photonic metamaterials. Nat. Nanotechnol. 2016, 11, 16−22.
(22) Holsteen, A. L.; Cihan, A. F.; Brongersma, M. L. Temporal
color mixing and dynamic beam shaping with silicon metasurfaces.
Science 2019, 365, 257−260.
(23) Afridi, A.; Gieseler, J.; Meyer, N.; Quidant, R. Ultrathin tunable
optomechanical metalens. Nano Lett. 2023, 23, 2496−2501.
(24) Bertoldi, K.; Vitelli, V.; Christensen, J.; van Hecke, M. Flexible
mechanical metamaterials. Nat. Rev. Mater. 2017, 2, 17066.
(25) Dudek, K. K.; Kadic, M.; Coulais, C.; Bertoldi, K. Shapemorphing metamaterials. Nature Reviews Materials 2025, 10, 783−
798.
(26) Schaedler, T. A.; Jacobsen, A. J.; Torrents, A.; Sorensen, A. E.;
Lian, J.; Greer, J. R.; Valdevit, L.; Carter, W. B. Ultralight Metallic
microlattices. Science 2011, 334, 962−965.
(27) Liu, W.; Janbaz, S.; Dykstra, D.; Ennis, B.; Coulais, C.
Harnessing plasticity in sequential metamaterials for ideal shock
absorption. Nature 2024, 634, 842−847.
(28) Yasuda, H.; Buskohl, P. R.; Gillman, A.; Murphey, T. D.;
Stepney, S.; Vaia, R. A.; Raney, J. R. Mechanical computing. Nature
2021, 598, 39−48.
(29) Bense, H.; van Hecke, M. Complex pathways and memory in
compressed corrugated sheets. Proc. Natl. Acad. Sci. U. S. A. 2021,
118, No. e2111436118.
5983

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984

## PDF page 8

ACS Photonics

pubs.acs.org/journal/apchd5

Article

(54) Tittl, A.; Leitis, A.; Liu, M.; Yesilkoy, F.; Choi, D.-Y.; Neshev,
D. N.; Kivshar, Y. S.; Altug, H. Imaging-based molecular barcoding
with pixelated dielectric metasurfaces. Science 2018, 360, 1105−1109.
(55) Koshelev, K.; Lepeshov, S.; Liu, M.; Bogdanov, A.; Kivshar, Y.
Asymmetric metasurfaces with high-Q resonances governed by bound
states in the Continuum. Phys. Rev. Lett. 2018, 121, No. 193903.
(56) Tsuchiya, T.; Hirata, Y.; Tanaka, S.; Kanda, Y. Evaluation of
Size Effect on Mechanical Properties of Single Crystal Silicon by
Nanoscale Bending Test Using AFM. J. Microelectromech. Syst. 2005,
14, 1178−1183.
(57) Alan, T.; Hines, M. A.; Zehnder, A. T. Effect of surface
morphology on the fracture strength of silicon nanobeams. Appl. Phys.
Lett. 2006, 89, No. 091901.
(58) DelRio, F. W.; Cook, R. F.; Boyce, B. L. Fracture strength of
micro- and nano-scale silicon components. Appl. Phys. Rev. 2015, 2,
No. 021303.
(59) Verschuuren, M. Substrate Conformal Imprint Lithography for
Nanophotonics; Ph.D. thesis, Utrecht University, 2010.

5984

https://doi.org/10.1021/acsphotonics.5c01385
ACS Photonics 2025, 12, 5978−5984
