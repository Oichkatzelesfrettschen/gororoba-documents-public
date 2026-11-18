Source: see manifest row of the PDF
PDF sha256: 6c132a6abb7f2cffd256b0b963a123e34144a7453f5c8f8baf9d9aeb54ea5d9b
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of yuen_2024_exact_quantum_electrodynamics_radiative_photonic_environments.pdf

Transcription of `yuen_2024_exact_quantum_electrodynamics_radiative_photonic_environments.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-6 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW LETTERS 133, 203604 (2024)

Exact Quantum Electrodynamics of Radiative Photonic Environments
Ben Yuen

*

and Angela Demetriadou

†

School of Physics and Astronomy, University of Birmingham, Edgbaston, Birmingham B15 2TT, United Kingdom
(Received 25 June 2024; accepted 20 September 2024; published 14 November 2024)
We present a comprehensive second quantization scheme for radiative photonic devices. We canonically
quantize the continuum of photonic eigenmodes by transforming them into a discrete set of pseudomodes
that provide a complete and exact description of quantum emitters interacting with electromagnetic
environments. This method avoids all reservoir approximations and offers new insights into quantum
correlations, accurately capturing all non-Markovian dynamics. This method overcomes challenges in
quantizing non-Hermitian systems and is applicable to diverse nanophotonic geometries.
DOI: 10.1103/PhysRevLett.133.203604

The geometry of the environment defines a photon’s
interaction with matter, bringing complexity to its radiative
behavior, from the Casimir force between an atom and
a surface, or the enhanced fluorescence of a molecule by a
nanoparticle, to the tapestry of colors scattered by stained
glass. Lately, quantum emitters (QEs), such as atoms,
fluorescent molecules, and quantum dots, have been
coupled to ever more geometrically complex photonic
devices [1–6], such as optical microcavities [7], nanobeams [4,8], plasmonic nanostructures [1–3,5] and hybrid
nanophotonic devices [9,10]. The interplay with multiple
photonic modes of varying radiative behavior leads to nonMarkovian quantum dynamics [11,12]. Such dynamics
significantly impact the future development of quantum
information processing [13,14], quantum transport [15–17],
photochemistry [18,19] and biological processes such as
light harvesting [20–22].
The interaction of QEs in photonic environments is
usually described by open quantum system coupled to a
reservoir that characterises radiative and material loss [11].
Such descriptions, typical of cavity quantum electrodynamics (cavity QED), simplify the continuous electromagnetic
spectrum via a simple phenomenological model of the local
density of states and were well suited to early high-finesse
micro resonators and Fabry-Perot cavities that radiate
weakly [23–25]. Lately however, focus has shifted toward
ever more intricate photonic devices where extreme subwavelength field confinement leads to extreme light-matter
interactions [1–5,8,26]. Such systems typically radiate
*

Contact author: b.yuen@bham.ac.uk
Contact author: a.demetriadou@bham.ac.uk

†

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI.

0031-9007=24=133(20)=203604(6)

efficiently to the far field, exhibit broadband overlapping
modes, and often have significant material losses. Classical
models for the local density of states have been phenomenologically quantised to form an open quantum system by
assuming Lorentzian photonic modes [27,28]. Alternatively,
classical quasi-normal modes [29,30] have been transformed and quantized “canonically” [31–33]. However,
such methods lack the generality of established quantum
optical theory, e.g. [34,35], and their disconnect between the
near and far-field precludes straightforward descriptions of
photon statistics, input and output field, squeezed light,
dressed states, etc. Furthermore, reservoir correlations—
from which complex non-Markovian dynamics arises—are
unaccounted for. Hence, there is need for an a priori method
that provides a global picture for open quantum nanophotonic systems.
In this Letter, we develop an a priori complete quantum
electrodynamic description of light-matter interactions for
radiative photonic devices by transforming the quantized
fields into pseudomodes [36,37]—originally used in an
elegant treatment of isolated Lorentzian resonances. We
show that our generalized pseudomode expansion gives a
complete and exact description of both near and far-field
without the need for a reservoir. The pseudomodes arise
naturally from the quantum dynamical equations of motion,
yet maintain a direct relationship to the resonant modes of
the photonic system. We derive the pseudomode’s quantum
equations of motion to obtain all the correlations and nonMarkovian dynamics of the field, and accurately described
the propagation of light. We give an example application of
a QE coupled to a microresonator that supports many
spectrally overlapping Mie resonances.
We start with the second quantization of the electromagnetic field, expanded in terms of its eigenmodes
uξ ðk; rÞ, labelled here by index ξ and wave number k.
For any nanophotonic system these are the solutions of the
Helmholtz equation

203604-1

Published by the American Physical Society

## PDF page 2

PHYSICAL REVIEW LETTERS 133, 203604 (2024)
½∇2 þ μðrÞϵðrÞk2 uξ ðk; rÞ ¼ 0;

Z ∞

ð1Þ

kdkρðkÞuξ ðk; rÞuξ ðk; r0 Þe−ickτ
X
¼
zξn vξn ðrÞvξn ðr0 ÞΘðτ − Δt ðr; r0 ÞÞe−iczξn τ ;
0

from which one constructs the corresponding electric
and magnetic fields Eðk; rÞ ¼ ickuξ ðk; rÞ, Hðk; rÞ ¼ ∇ ×
uξ ðk; rÞ. The nanostructure geometry is specified by the
relative electric permittivity ϵðrÞ–assuming non-magnetic
materials (μðrÞ ¼ 1). To canonically quantize the field via
this mode decomposition, the
R eigenmodes must satisfy
the orthogonality condition V drϵðrÞuξ ðk0 ; rÞuξ0 ðk0 ; rÞ ¼
δξξ0 δkk0 and the energy of each mode must be conserved in
time. For free space [ϵðrÞ ¼ 1] this is achieved using
periodic or zero Dirichlet boundary conditions within a
box of volume V, which is subsequently taken to infinity.
A similar approach is adopted here, but the shape of
the bounding volume V is chosen to match the geometry
of the nanophotonic device and the boundary condition
ðE × BÞ · dS ¼ 0 is applied on its surface. The solutions
uξ ðk; rÞ cover all of space, and the discrete spectrum
of k becomes continuous when we take the limit
V → ∞, which for convenience is performed after quantization. The quantum field operators are then expanded
over uξ ðk; rÞ, e.g.,
sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
ℏck
uξ ðk; rÞða†ξk þ aξk Þ;
2ϵ
ϵðrÞ
0
ξ;k

X
ÊðrÞ ¼ i

ð2Þ

where a†ξk and aξk are the usual bosonic creation and
annihiliation operators. We consider a two-level QE that
interacts via the dipole interaction d̂ · ÊðrÞ in the length
gauge where the system is described by the Hamiltonian
X
H=ℏ ¼ ω0 σ þ σ − þ
cka†ξk aξk
ξ;k

X
þ
gðrÞðaξk σ þ þ a†ξk σ − Þ:

ð3Þ

ξ;k

Each respective term corresponds to the QE with transition
frequency ω0, the field, and their interaction under the
dipole and rotating wave approximations, where σ  are the
dipole raising/lowering operators. The coupling strength
for a QE at position r is
gξ ðk; rÞ ¼

pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
ℏck=2ϵ0 ϵðrÞd · uξ ðk; rÞ;

evaluated by the residue theorem over poles zξn in the lower
half plane for τ > 0 [see Supplemental Material (SM) [39]].
The complex pseudomode frequencies czξn correspond to
the nth resonance of mode ξ. The integrand’s asymptotic
behavior determines the pole location and half plane the
contour integral encloses and leads to the Heaviside-step
function Θ½τ − Δt ðr; r0 Þ. Physically, this accounts for the
finite time delay for light to propagate from r0 to r via the
photonic structure.
The pseudomode transformation arises naturally from
the Schrödinger equations of motion with the QE initially
excited—we consider general initial conditions using the
Heisenberg equations elsewhere [40]. Here the state vector
is described by the amplitudes c0 ðtÞ and cξk ðtÞ of the QE
excited state j0; ei and singly excited field mode a†ξk j0; gi,
respectively. These obey the coupled equations c̃˙ 0 ðtÞ ¼
P
−i ξk gξk eiðω0 −ckÞt c̃ξk ðtÞ and c̃˙ ξk ðtÞ ¼ gξk e−iðω0 −ckÞt c̃0 ðtÞ,
derived from the Schrödinger equation in the interaction
picture. Formally integrating the latter with c̃ξk ð0Þ ¼ 0,
inserting into the
R and taking the continuum limit
Pformer,
V → ∞, where k → ρðkÞdk, gives
Z t XZ
d
0
dkρðkÞg2ξ ðkÞeiðω0 −ckÞðt−t Þ c̃0 ðt0 Þ:
c̃0 ðtÞ ¼ −
dt0
dt
0
ξ
ð6Þ
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
The first Markov approximation gξ ðkÞ ≈ γ=2π [41] is
often applied here to simplify the integral over k. Instead we
evaluate the k integral exactly using gξ ðk; rÞ of Eq. (4) and
the transformation of Eq. (5) to obtain
Z t X
d
0
c̃0 ðtÞ ¼ −
dt0 ḡ2ξn eiðω0 −czξn Þðt−t Þ c̃0 ðt0 Þ: ð7Þ
dt
0
ξ;n
This is equivalent to the discrete set of coupled pseudomode equations

ð4Þ

where d is the dipole moment. While here we only consider
two-level QEs, our approach can be generalized to complex
multilevel emitters starting from the minimal coupling
Hamiltonian, keeping terms linear in the field [38].
We transform the system into the “pseudomode picture”
to reveal the full range of quantum dynamics. The mode
functions are transformed from the continuous set of
Helmholtz solutions uξ ðk; rÞ to a discrete set of pseudomodes vξn ðrÞ, determined by the integral transformation

ð5Þ

n

X
d
c̃0 ðtÞ ¼
ḡξn eiðω0 −czξn Þt b̃ξn ðtÞ;
dt
ξn

ð8aÞ

d
b̃ ðtÞ ¼ ḡξn e−iðω0 −czξn Þt c̃0 ðtÞ:
dt ξn

ð8bÞ

i

i

with pseudomode-QE interaction strength

203604-2

sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
ℏczξn
d · vξn ðrÞ:
ḡξn ðrÞ ¼
2ϵ0 ϵðrÞ

ð9Þ

## PDF page 3

PHYSICAL REVIEW LETTERS 133, 203604 (2024)

FIG. 1. Schematic diagram of a spherical nanopartice (blue)
surrounded by vacuum and enclosed within a bounding volume
(dashed line) of radius R → ∞. A QE (red) interacts with the
mode’s electric field (purple). The interaction spectrum (right) is
shaped by the nanoparticle geometry.

By solving these equations for an initially excited QE one
obtains the full quantum dynamical evolution of the
system. These equations are non-Hermitian since zξn and
ḡξn are complex valued, which cause the pseudomode
amplitudes b̃ξn ðtÞ to decay in time as energy is radiated to
the far field.
The electromagnetic fields are expressed exactly by a
time-dependent superposition of pseudomodes vξn ðrÞ. The
intensity hE− ðr; tÞEþ ðr; tÞi is found from the field quadrature acting on jψðtÞi,
sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
X ℏczξn
Eþ jψðtÞi ¼ i
vξn ðrÞb̃ξn ðt − ΔtÞe−iczξn t ; ð10Þ
2ϵ
ϵðrÞ
0
ξ;n
which was derived using the pseudomode transformation (see SM [39]). Here, b̃ξn is taken at the retarded
time t − Δt ðr; r0 Þ. Expanding the exponential as
e−iczξn ðt−Δt Þ e−iczξn Δt highlights the decay by the factor
e−icImðzξn ÞΔt due to the propagation delay Δt ðr; r0 Þ.
This decay ensures the field remains regular even though
the pseudomodes themselves diverge as r → ∞, as
expected for a non-Hermitian theory [42]. Hence our
pseudomode approach overcomes the mode divergence
problem for radiating photonic systems [31,32] to give a
global description of the field.
To comprehensively demonstrate this new approach, we
apply it to a QE coupled to a spherical silicon resonator of
radius a ¼ 1μm and refractive index N ¼ 3.446 surrounded
by vacuum (see Fig. 1). We use dimensionless units ℏ ¼
c ¼ 1 hereafter. This geometry supports Mie resonances
with the near field enhanced due to the confinement of
modes by the dielectric interface at r ¼ a [43]. For microspheres with a ≫ λ the Mie modes interfere constructively,
forming high-finesse whispering gallery modes [44]. For
a ≲ 1μm, individual Mie modes form a spectrum of distinct
but overlapping resonances (e.g. Fig. 2). The eigenmodes
take the form of vector spherical Harmonics Mlm ðk; rÞ ¼
∇ × r̂ψ lm ðk; rÞ and Nlm ðk; rÞ ¼ ð1=kÞ∇ × Mlm ðk; rÞ,
where ψ lm ðk; rÞ ¼ eimϕ Pm
l ðcos θÞZl ðkrÞ. The angular

FIG. 2. Spectrum of a 1 μm Silicon sphere. (a) The enhancement of TM modes given by the mode normalization I M ðkÞ
(Eq. (12)), with the black line showing the sum over all modes
(total); (b) the scattering cross section.

distributions for different integers l ∈ N and jmj ≤ l are
orthogonal and Pm
l ðcos θÞ are the associated Legendre
polynomials (see SM [39]). The radial functions Zl ðkrÞ,
pﬃﬃ
1
Zl ð ϵkrÞ ¼ pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
I M ðkÞ



pﬃﬃ
ηl ðkÞjl ð ϵkrÞ

r<a

αl ðkÞjl ðkrÞ þ βl ðkÞyl ðkrÞ r > a;
ð11Þ

are piecewise continuous solutions of the spherical Bessel
equation that are regular at the origin, zero on the surface of
the bounding volume of radius R ≫ a, and produce a
continuous tangential field at the dielectric interface. The
interface conditions determine the coefficients αl ðkÞ; βl ðkÞ
and ηl ðkÞ (see SM [39]). These produce the resonances in
Fig. 2, determined by the normalization factor I M ðkÞ,
lim I M ðkÞ ¼

R→∞

R
½αl ðkÞ þ iβl ðkÞ½αl ðkÞ − iβl ðkÞ;
2k2

ð12Þ

analogous to the mode volume of the photonic system.
Resonances occur for real k adjacent to the complex roots
zln of Eq. (12) which are poles of Eq.P(11). Similarly, the
scattering cross-section σ s ðkÞ ¼ k−2 l ð2l þ 1Þjβl =ðαl þ
iβl Þj2 shown in Fig. 2(b) is resonant at the same poles,
which have long been identified as the natural modes [45].
Furthermore, the radial functions Zl ðkrÞ are orthogonal due
to the conditions at r ¼ 0; a and R, and therefore Mlm ðk; rÞ
and Nlm ðk; rÞ satisfy the orthonormality condition of
uξ ðk; rÞ with ξ ¼ ðl; m; nÞ. Finally, for finite R, the allowed
values of k for which Zl ðkRÞ ¼ 0 form a countably infinite
set, with asymptotic mode density ρðkÞ ¼ R=π. In the limit
R → ∞, k becomes continuous.
We now quantize these eigenmodes and subsequently
perform the pseudomode transformation. The second
quantized electric field operator Eq. (2) is now obtained
using these orthonormal modes, and the Hamiltonian is

203604-3

## PDF page 4

PHYSICAL REVIEW LETTERS 133, 203604 (2024)
given by Eq. (3) with coupling strengths given by Eq. (4).
For simplicity we choose a QE radially oriented d ¼ jdjr̂
which only couples to the TM modes, and therefore
ulm ðk; rÞ ¼ Nlm ðk; rÞ is sufficient henceforth. We now
transform the system into a discrete set of pseudomodes
vlmn ðrÞ that interact with the QE, by evaluating the integral
of Eq. (5) over Nlm ðk; rÞ. Separating out the k-dependent
terms, this becomes N lm ðrÞN Tlm ðr0 ÞI l ðr; r0 Þ, where
Z ∞
pﬃﬃ
pﬃﬃ
I l ðr; r0 Þ ¼
dkρðkÞk−1 Zl ð ϵkrÞZl ð ϵkr0 Þe−ickτ ð13Þ
0

and N lm ðrÞN Tlm ðr0 Þ is the outer product of the differential
pﬃﬃ
operators such that Nlm ðk; rÞ ¼ N lm ðrÞZl ð ϵkrÞ=k (see
SM [39]).
To evaluate Eq. (13), initially with lower limit k ¼ −∞,
we extend the integrand
pﬃﬃ fðkÞ into the complex plane
k → z. We expand Zl ð ϵzrÞ into its outgoing and incomð1 Þ

ing components proportional to hl 2 ¼ jl  iyl . This splits
fðzÞ into incoming f 1 ðzÞ, outgoing f 2 ðzÞ, and mixed
f 12 ðzÞ components that converge to zero as jzj → ∞ in the
lower half plane when cτ > ðr − aÞ for f 1, cτ < −ðr − aÞ
for f 2, and cτ < r for f 12, and the upper half plane
otherwise. After careful consideration of the poles and
contours (see SM [39]), we find
I
I l ¼ Θ½cτ − ðr − aÞ
f 1 ðzÞdz
LHP
I
þ Θ½cτ þ ðr − aÞ
f 2 ðzÞdz;
ð14Þ
UHP

which is evaluated using the residue theorem. To evaluate
Eq. (13) with lower limit k ¼ 0, we split fðkÞ further, into
symmetric f s ðkÞ and antisymmetric components f a ðkÞ,
then integrate f s ðkÞ or sgnðkÞf s ðkÞ as before, then divide
the result by two (see SM [39]). Consequently, for positive
times,
X
I l ðr; r0 Þ ¼ 2πi
Res½f 2 ðzÞΘ½cτ − ðr − aÞ; ð15Þ
zln ∈ Q4

where the sum is over the fourth quadrant of the complex
plane
2
3
sﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
αl ðzln Þ − iβl ðzln Þ
6
7
ð1Þ
vlmn ðrÞ ¼ N lm ðrÞ4π
hl ðzln rÞ5;
i½∂z ðαl ðzÞ þ iβl ðzÞÞzln
ð16Þ
where the term in brackets defines the pseudomodes radial
behavior. These pseudomodes differ from ulm ðk; rÞ in
their radial behavior, complex nature, and their discrete
spectrum over the roots of Eq. (12) in the fourth quadrant.
We show the distributions of two different pseudomodes,
ðl; m; nÞ equal to (5, 0, 4) and (8, 0, 3), in Fig. 3. These

FIG. 3. Intensity distribution for (a) the (5, 0, 4) and (b) the (8,
0, 3) pseudomodes plotted as function of 0 < r < 1.5 μm and θ.
The resonator surface is at r ¼ 1.

correspond to the two narrow overlapping resonances at
1.72 μm in Fig. 2(a).
The quantum dynamics of the system are found using
Eq. (8). Choosing the QE coordinate θ ¼ 0 simplifies
further calculations since Y m
l ð0; ϕÞ ≡ 0 for m ≠ 0, and
we label modes by ðl; nÞ henceforth. We set the QE’s
shifted transition frequency (ω0 þ Im½δω0 ) to be resonant
with the (8, 3) pseudomode, where
δω0 ¼

X

g2ln

off-res

ðω0 − ωln Þ − iγ ln
ðω0 − ωln Þ2 þ γ 2ln

ð17Þ

is the Lamb shift due to off-resonant modes (see SM [39])
[46]. The dynamical equations for the 613 pseudomodes in
the range l ≤ 30 and Rezln j < 20 μm−1 are solved rapidly
using diracpy [49] via a similarity transformation that
diagonalizes Eq. (8).
Figure 4 shows the time evolution of the QE excited state
(blue lines) and pseudomode populations. For d ¼ 10 D,
Rabi oscillations (inherently non-Markovian by nature)
occur between the QE and the strongly coupled (8, 3)
mode at frequency j2ḡ8;3 j, and their decay is primarily due to
the radiation of the (8, 3) mode. By contrast, the weakly
coupled (5, 4) mode dynamics are Markovian, oscillating in
phase with the QE six orders of magnitude lower. All other
modes are shown by the background (yellow-red lines) with
small populations ≲10−9 and are initially rapidly excited to
values ∼jg=ðω0 − czln Þj2 (see SM [39]). For d ¼ 100 D in
Fig. 4(b), the Rabi oscillations are 10 times faster, while the
decay rate remains largely unchanged. For d ¼ 104 D
(Fig. 4(c)) the dynamics are more complex. The (5, 4)
mode, on the cusp of strong coupling, now oscillates out of
phase with the QE and radiates energy more efficiently than
the (8, 3) mode, significantly accelerating the QE’s decay.
The remaining nonresonant mode’s behavior depends on the
ratio γ ln =Γ0 , where the rate Γ0 characterizes the QE decay:
strongly radiating pseudomodes (γ ln =Γ0 ≫ 1, red lines)
follow the QE amplitude with bln ðtÞ ≈ gln c0 ðtÞ=ðω0 −
czln Þ demonstrating Markovian behavior. High-Q pseudomodes (γ ln =Γ0 ≪ 1, yellow) are non-Markovian, evolving
as bln ðtÞ ≈ gln expð−iczln tÞ=ðω0 − czln Þ for long times
Γ−1
0 t ≫ 1.

203604-4

## PDF page 5

PHYSICAL REVIEW LETTERS 133, 203604 (2024)

FIG. 5. Expected field intensity hIðr; tÞi for a d ¼ 10D QE as a
function of radius r and time ct for (a) the (8, 3) pseudomode,
which is localized around the photonic resonator, (b) all other
modes showing radiative behavior, and (c) total intensity.

FIG. 4. Dynamical evolution of QE and pseudomodes state
populations calculated for dipole moments of (a) 10 D,
(b) 100 D, and (c) 104 D. The QE excited state (blue),
(8, 3) pseudomode (orange), and (5, 4) pseudomode (green)
populations. The lines in red-yellow hue show all other pseudomode populations where the hue indicates their decay rate
given by Imðzln Þ. The dashed lines show the approximate
results of Eq. (18).

We can approximate our system, dominated by the (8, 3)
and (5, 4) modes, by a two-mode model given by
i

X
d
c̃0 ðtÞ ¼ δω0 c̃0 ðtÞ þ
ḡln eiðω0 −czln Þt b̃ln ðtÞ
dt
ð5;4Þ;

ð18Þ

ð8;3Þ

and Eq. (9) for these two modes only, while δω0 is
calculated from Eq. (17) over all other modes. These
approximate solutions are plotted in Fig. 4 with dashed
lines and show remarkable accuracy provided jc0 j2 is larger
than the off-resonant mode populations.
Finally, we calculate the expected field intensity
hIðr; tÞi ¼ hE− ðr; tÞEþ ðr; tÞi using Eq. (10) for d ¼
10 D (see SM [39] for animations). Figure 5 shows
hIðr; tÞi plotted against distance from the sphere (r − a)
and time (ct) and clearly shows the light cone. The
contribution from the high-Q (8, 3) mode (Fig. 5(a)),
confined to the near field r − a ≲ 1 μm, shows decaying
Rabi oscillations with period cT ¼ 4.63 × 105 μ. All other
modes are shown in Fig. 5(b). A short pulse originates in the
region ðr ¼ a; ct ≲ 1μmÞ, due to transient excitation of the
field. Radiation from the weakly coupled (5,4) mode then
dominates in the region 1 μm < ct < 200 μm and interferes with more weakly excited modes. For ct > 200 μm,

the (5, 4) mode has radiatively decayed, revealing nonMarkovian dynamics in the near field due to high-finesse
off-resonant modes. Figure 5(c) shows the total intensity is
dominated at short times by the off-resonant modes and at
longer times by the coherent oscillations of the (8, 3) mode.
By transforming the continuum into a discrete set of
pseudomodes, we solve the dynamics without the need for
a reservoir, its accompanying approximations, and therefore we retain all the information about the continuum. Our
theory demonstrates that QE decay arises from the continuous nature of the quantized field: the system never
decays to the ground state j0; gi; its energy is merely
dispersed over the continuous spectrum of eigenmodes, for
which there is no inherent decay. The “decay” of the
pseudomode amplitudes b̃ξn ðτÞ describes the tail of the
photon wave packet as it propagates, when taken correctly
at the retarded time τ ¼ t − r=c. This arises naturally in
our infinite yet closed quantum system, which avoids
outgoing wave boundary conditions on the normal modes
uξ ðk; rÞ that necessitate nonstandard quantization of divergent modes for non-Hermitian systems [31].
In conclusion, we present a general theory that gives a
complete and exact description for the quantum electrodynamics of a QE strongly interacting with a radiating
photonic device. We quantize the continuous Helmholtz
eigenmodes, which we then transform with one-to-one
correspondence into a discrete set of non-Hermitian
pseudomodes. Thus, we solve common problems met
when quantizing non-Hermitian systems, such as mode
divergence, defining mode volumes, and identifying
canonical field variables. Furthermore, our approach precisely captures all quantum correlations of the field and
QE, avoiding common Markovian approximations, and
unlike other methods, accurately captures the light propagation to the far field. This new method can be further
extended for arbitrary photonic geometries through the
analytic continuation of the local density of states and can
reveal the non-Markovian behavior exhibited in experimentally realizable systems at the nanoscale.

203604-5

## PDF page 6

PHYSICAL REVIEW LETTERS 133, 203604 (2024)
Acknowledgments—A. D. gratefully acknowledges support from the Royal Society University Research
Fellowship URF/R1/180097 and URF/R/231024, and
funding from EPSRC EP/X012689/1, EP/Y008774/1 and
CDT in Topological Design EP/S02297X/1. A. D. and B.
Y. gratefully acknowledge support funding from Research
Fellows Enhancement Award RGF /EA/181038.

[1] G. Zengin, M. Wersäll, S. Nilsson, T. J. Antosiewicz, M.
Käll, and T. Shegai, Phys. Rev. Lett. 114, 157401 (2015).
[2] R. Chikkaraddy, B. De Nijs, F. Benz, S. J. Barrow, O. A.
Scherman, E. Rosta, A. Demetriadou, P. Fox, O. Hess, and
J. J. Baumberg, Nature (London) 535, 127 (2016).
[3] F. Benz, M. K. Schmidt, A. Dreismann, R. Chikkaraddy,
Y. Zhang, A. Demetriadou, C. Carnegie, H. Ohadi, B. De
Nijs, R. Esteban et al., Science 354, 726 (2016).
[4] A. Sipahigil, R. E. Evans, D. D. Sukachev, M. J. Burek,
J. Borregaard, M. K. Bhaskar, C. T. Nguyen, J. L. Pacheco,
H. A. Atikian, C. Meuwly et al., Science 354, 847 (2016).
[5] R. Chikkaraddy, R. Arul, L. A. Jakob, and J. J. Baumberg,
Nat. Photonics 17, 865 (2023).
[6] S. Sun, H. Kim, Z. Luo, G. S. Solomon, and E. Waks,
Science 361, 57 (2018).
[7] K. J. Vahala, Nature (London) 424, 839 (2003).
[8] Q. Quan and M. Loncar, Opt. Express 19, 18529 (2011).
[9] H. M. Doeleman and E. Verhagen, and A. F. Koenderink,
ACS Photonics 3, 1943 (2016).
[10] A. Barreda, L. Mercade, M. Zapata-Herrera, J. Aizpurua,
and A. Martínez, Phys. Rev. Appl. 18, 044066 (2022).
[11] I. De Vega and D. Alonso, Rev. Mod. Phys. 89, 015001
(2017).
[12] H.-P. Breuer and F. Petruccione, The Theory of Open
Quantum Systems (Oxford University Press, Oxford, 2002).
[13] F. Flamini, N. Spagnolo, and F. Sciarrino, Rep. Prog. Phys.
82, 016001 (2018).
[14] J. Wang, F. Sciarrino, A. Laing, and M. G. Thompson, Nat.
Photonics 14, 273 (2020).
[15] A. Bermúdez, M. Bruderer, and M. B. Plenio, Phys. Rev.
Lett. 111, 040601 (2013).
[16] S. Jezouin, F. Parmentier, A. Anthore, U. Gennser, A.
Cavanna, Y. Jin, and F. Pierre, Science 342, 601 (2013).
[17] J. P. Pekola, Nat. Phys. 11, 118 (2015).
[18] M. Mohseni, A. Shabani, S. Lloyd, Y. Omar, and H. Rabitz,
J. Chem. Phys. 138, 204309 (2013).
[19] G. D. Scholes, G. R. Fleming, L. X. Chen, A. AspuruGuzik, A. Buchleitner, D. F. Coker, G. S. Engel, R. Van
Grondelle, A. Ishizaki, D. M. Jonas et al., Nature (London)
543, 647 (2017).
[20] S. F. Huelga and M. B. Plenio, Contemp. Phys. 54, 181
(2013).
[21] R. Hildner, D. Brinks, J. B. Nieder, R. J. Cogdell, and N. F.
Van Hulst, Science 340, 1448 (2013).
[22] K. M. Pelzer, A. F. Fidler, G. B. Griffin, S. K. Gray, and
G. S. Engel, New J. Phys. 15, 095019 (2013).
[23] T. Yoshie, A. Scherer, J. Hendrickson, G. Khitrova, H.
Gibbs, G. Rupper, C. Ell, O. Shchekin, and D. Deppe,
Nature (London) 432, 200 (2004).

[24] J. P. Reithmaier and G. Sęk, A. Löffler, C. Hofmann,
S. Kuhn, S. Reitzenstein, L. Keldysh, V. Kulakovskii, T.
Reinecke, and A. Forchel, Nature (London) 432, 197 (2004).
[25] E. Peter, P. Senellart, D. Martrou, A. Lemaître, J. Hours,
J. M. Gérard, and J. Bloch, Phys. Rev. Lett. 95, 067401
(2005).
[26] M. S. Tame, K. McEnery, Ş. Özdemir, J. Lee, S. A. Maier,
and M. Kim, Nat. Phys. 9, 329 (2013).
[27] I. Medina, F. J. García-Vidal, A. I. Fernández-Domínguez,
and J. Feist, Phys. Rev. Lett. 126, 093601 (2021).
[28] M. Sánchez-Barquilla, F. J. García-Vidal, A. I. FernándezDomínguez, and J. Feist, Nanophotonics 11, 4363 (2022).
[29] R.-C. Ge, P. T. Kristensen, J. F. Young, and S. Hughes, New
J. Phys. 16, 113048 (2014).
[30] P. Lalanne, W. Yan, K. Vynck, C. Sauvan, and J.-P.
Hugonin, Laser Photonics Rev. 12, 1700113 (2018).
[31] S. Franke, S. Hughes, M. K. Dezfouli, P. T. Kristensen, K.
Busch, A. Knorr, and M. Richter, Phys. Rev. Lett. 122,
213901 (2019).
[32] C. Sauvan, J.-P. Hugonin, I. S. Maksymov, and P. Lalanne,
Phys. Rev. Lett. 110, 237401 (2013).
[33] K. Bedingfield, B. Yuen, and A. Demetriadou, arXiv:2310
.06462.
[34] S. Barnett and P. M. Radmore, Methods in Theoretical
Quantum Optics (Oxford University Press, Oxford, 2002),
Vol. 15.
[35] P. Lambropoulos, G. M. Nikolopoulos, T. R. Nielsen, and
S. Bay, Rep. Prog. Phys. 63, 455 (2000).
[36] B. M. Garraway, Phys. Rev. A 55, 2290 (1997).
[37] B. J. Dalton, S. M. Barnett, and B. M. Garraway, Phys. Rev.
A 64, 053813 (2001).
[38] G. Grynberg, A. Aspect, and C. Fabre, Introduction to
Quantum Optics: From the Semi-Classical Approach to
Quantized Light (Cambridge University Press, Cambridge,
England, 2010).
[39] See Supplemental Material at http://link.aps.org/
supplemental/10.1103/PhysRevLett.133.203604 for detailed derivation of the general pseudomode transformation
Eq. (5) and field operator Eq. (10), and their application to a
dielectric sphere.
[40] B. Yuen and A. Demetriadou (to be published).
[41] C. W. Gardiner and M. J. Collett, Phys. Rev. A 31, 3761
(1985).
[42] N. Moiseyev, Non-Hermitian Quantum Mechanics
(Cambridge University Press, Cambridge, England, 2011).
[43] C. F. Bohren and D. R. Huffman, Absorption and Scattering
of Light by Small Particles (John Wiley & Sons, New York,
2008).
[44] A. N. Oraevsky, Quantum Electron. 32, 377 (2002).
[45] J. A. Stratton, Electromagnetic Theory (John Wiley & Sons,
New York, 2007), Vol. 33.
[46] The effect of QED mass renormalization [47,48] on
this shift is considered in future work, where one must
also consider the resonator’s optical response at high
frequencies.
[47] S. Weinberg, The Quantum Theory of Fields (Cambridge
University Press, Cambridge, England, 1995), Vol. 2.
[48] B. Delamotte, Am. J. Phys. 72, 170 (2004).
[49] B. Yuen, Diracpy v1.0.0, https://github.com/b-yuen/diracpy
(2022).

203604-6
