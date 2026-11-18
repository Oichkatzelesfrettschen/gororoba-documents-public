Source: https://arxiv.org/abs/2505.00396v1
PDF sha256: bff27d8b1df3a3907f23aaa234a40d31e33013f4c18bb007b4b3c1c84adc48db
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of maksimov_2025_tcmt_symmetry_constraints_arxiv_2505_00396.pdf

Transcription of `maksimov_2025_tcmt_symmetry_constraints_arxiv_2505_00396.pdf` in this directory, 17 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-17 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Temporal coupled mode theory for high-Q resonances in dielectric metasurfaces
Dmitrii N. Maksimov,1, 2, 3 Pavel S. Pankin,1, 2, 4, ∗ Dong-Wook
Kim,1, 5 Mingzhao Song,1 Chao Peng,6 and Andrey A. Bogdanov1, 5, †
1 Qingdao Innovation and Development Center, Harbin Engineering University, Qingdao 266000, Shandong, China
2 Kirensky Institute of Physics, Federal Research Centre KSC SB RAS, 660036, Krasnoyarsk, Russia
3 IRC SQC, Siberian Federal University, 660041, Krasnoyarsk, Russia
4 School of Engineering Physics and Radio Electronics,

Siberian Federal University, 660041, Krasnoyarsk, Russia
Petersburg 197101, Russia
6 State Key Laboratory of Photonics and Communications, School of Electronics,
& Frontiers Science Center for Nano-optoelectronics, Peking University, Beijing 100871, China
(Dated: May 2, 2025)

arXiv:2505.00396v1 [physics.optics] 1 May 2025

5 School of Physics and Engineering, ITMO University, St.

In this work, we propose a coupled mode theory for resonant response from quasi-guided modes in periodic
dielectric metasurfaces. First, we derived a generic set of constraints imposed onto the parameters of the temporal coupled mode theory by energy conservation and time-reversal symmetry in an invariant form that allows for
asymmetry between the coupling and decoupling coefficients. The proposed approach is applied to the problem
of Fano resonances induced by isolated quasi-guided modes in the regime of specular reflection. Our central
result is a generic formula for the line-shape of the Fano resonance in transmittance for the lossless metasurfaces
in the framework of 2D electrodynamics. We consider all possible symmetries of the metasurface elementary
cell and uncover the effects that the symmetry incurs on the profile of the Fano resonance induced by an isolated high-Q mode. It is shown that the proposed approach correctly describes the presence of robust reflection
and transmission zeros in the spectra as well as the spectral signatures of bound states in the continuum. The
approach is applied to uniderictionally guided resonant modes in metasurfaces with an asymmetric elementary
cell. It is found that the existence of such modes and the transmittance in their spectral vicinity are consistent
with the theoretical predictions. Furthermore, the theory predicts that a uniderictionally guided resonant mode
is dual to a counter-propagating mode of a peculiar type which is coupled with the outgoing wave on both sides
of the metasurface but, nonetheless, exhibits only a single-sided coupling with incident waves.

I.

INTRODUCTION

In recent years dielectric metasurfaces have become an indispensable tool in the fields of photonics and radiophysics
since their application paves the way to shaping optical response induced by high-quality (high-Q) modes [1–5]. The
propagating modes in periodic dielectric metasurfaces are
Bloch waves traveling across the plane of the metasurface.
If the frequency of such waves at a given in-plane Bloch
wavenumber occurs above the line of light, the modes radiate electromagnetic energy into outer space. Thus, the modes
become leaky and, as such, can be termed quasi-guided or
radiative modes [6, 7]. On the other hand, leaky modes are
resonant, that is, can be coupled with incident light to induce a resonant response, which is accompanied by the enhancement of the electromagnetic field in the host structure
[8, 9]. This phenomenon has been instrumental in the design
of various devices that employ a strong light-matter interaction, even with low-loss dielectrics [10, 11]. Nowadays, such
devices include lasers [12–17], sensors [18–24], absorbers
[25–29], polaritonic devices [30–33], and nonlinear optical
components [34–38]. Formally, various types of resonances
in metasurfaces, including Wood anomalies [39, 40], lattice
resonances [41, 42], quasi-bound states in the continuum [43],
and high-Q Mie resonances [44] can be associated with quasi-

∗ pavel-s-pankin@iph.krasn.ru
† a.bogdanov@hrbeu.edu.cn

guided resonant modes also know as resonant states [45, 46]
or quasi-normal modes [47, 48].
In the far field the high-Q resonant modes manifest themselves as sharp Fano resonances in the transmittance spectrum
[2, 49–51]. The Fano resonances are typically understood as
the product of interference between waves following two optical paths. The above interpretation can be applied to dielectric
metasurfaces via decomposing the electromagnetic field into
a resonant field, which is induced by coupling to a resonant
eigenmode, and a background field, which is independent of
the incident frequency on the scale of the high-Q resonance
width [52]. The Fano resonances, therefore, are the primary
signature of the resonant modes in a dielectric metasurface.
The intricate behavior of Fano resonances makes it possible to
apply dielectric metasurfaces to shape the transmittance spectrum for filtering [53, 54], polarization conversion [55, 56],
and circular dichroism [57, 58].
One remarkable feature of the subwavelength dielectric
metasurfaces is the opportunity to control the life-time of the
resonant modes. In the ideal case of a lossless dielectric an
infinite life-time can be achieved even above the line of light
with non-radiating modes embedded in the continuum of scattering solutions. Such modes are known as bound states in the
continuum (BICs) and are representative of the utmost case of
light localization [59–62]. By definition, the BICs are not coupled with incident radiation, and therefore are seemingly useless in applications. However, BICs can be activated by breaking the system’s symmetry, either structurally [63], or by incident field [64]. As a consequence, the BIC can be transformed
into a quasi-BIC with extremely high quality factor (Q-factor)

## PDF page 2

2
which diverges to infinity as the symmetry is recovered under variation of a certain control parameter, e.g. the angle
of incidence. The Q-factor divergence manifests itself in the
transmittance spectrum as a collapsing Fano resonance with
the line-width vanishing on approach to the BIC point in the
parametric space [65–68]. The collapse of the Fano resonance
is complemented by the critical field enhancement [8, 69], the
latter effect being limited only by the material losses in the
host dielectric.
Another interesting type of high-Q resonant modes to have
recently attracted a lot of attention in the literature is a unidirectional guided resonant mode (UGR) [70]. This type of
resonant mode can be viewed as a semi-BIC since the UGRs
do not radiate only to a single direction, i.e., either to the
substrate or to the superstrate of the metasurface. In addition to intriguing topological properties [71–74], UGRs are
applicable to optical devices that utilize asymmetric coupling
between the resonant mode and the outgoing waves [75–80].
Theoretical description of the Fano resonances induced by
various types of quasi-guided modes in dielectric metasurfaces is hindered by the complexity of the host structures. The
aforementioned phenomena occur only in dielectric systems,
which are at least two-dimensional (2D) structures with the
permittivity modulated in one spatial dimension. This does
not allow for analytic solutions of Maxwell’s equations to be
written in a closed form. Nonetheless, it is possible to derive
a generic expression for the transmittance as a function of the
incident frequency by using temporal coupled mode theory
(TCMT). The TCMT is a phenomenological instrument that
relies on symmetries and conservation laws to establish constraints on the number of parameters that describe the Fano
line-shape [52, 81]. The TCMT approach has proved to be
efficient for analyzing the scattering and absorption spectra of
dielectric metasurfaces [82–89].
In this work, we revisit the TCMT in application to the Fano
response from dielectric metasurfaces hosting high-Q resonant modes. Our goal is to develop a TCMT approach that
both accommodates various kinds of high-Q resonances, including BICs and UGRs, and reflects the role of the symmetry
of the metasurface elementary cell. We derive a generic formula for the line-shape of the Fano resonance in transmittance
for the lossless metasurfaces in the framework of 2D electrodynamics. We discuss all possible symmetries of the metasruface elementary cell and uncover the effects that the symmetry
incurs on the profile of the Fano resonance induced by an isolated high-Q mode. The article is organized as follows. In
Sec. II we introduce the system under scrutiny and discuss the
generic properties of the scattering matrix (S-matrix) in the
regime of specular reflection. In Sec. III we overview and revisit the TCMT to derive the generic form of the constraints
imposed on the resonant mode coupling and decoupling coefficients by energy conservation and time-reversal symmetry.
In Sec. IV we apply the results of the previous section to dielectric metasurfaces and derive the generic TCMT solution
for the Fano resonance line-shape. In Sec. V we verify our
findings numerically in comparison with finite-difference frequency domain (FDFD) [90] simulations for all types of point
group symmetries of the elementary cell including in-plane

FIG. 1. Dielectric metasurface in the form of a ruled grating. (a) The
light blue bars show the ruled grating with refractive index n1 = 3.5.
The plane of incidence is shaded in gray. The magenta arrows shows
the wave vector k of the incident field. The y-component of the electric field and the x-component of k are shown as vectors. The refractive index of ambient medium n0 = 1.5. (b) Diagram of diffraction
orders. The colorbar on the right indicates the number of channels
open for diffraction on either side of the metasurface.

mirror symmetry, out-of-plane mirror symmetry, and inversion symmetry. In Sec. VI we apply our approach to UGRs.
It is shown for the asymmetric metasurfaces that the UGR is
dual to a counter-propagating mode of a peculiar type. Unlike the UGR which is not coupled with one of the outgoing channels whereas being coupled with both incident ones,
the dual mode, which we term unidirectional coupled resonant
mode (UCR), is not coupled with one of the incident channels
whereas is still coupled with both outgoing ones. Finally, we
summarize and conclude in Sec. VII.

II.

SYSTEM DESCRIPTION

The system to be considered is shown in Fig. 1. One can see
in Fig. 1 (a) that the system is a ruled grating that possesses
a translation symmetry in the x-direction with period Λ. The
body of the grating is made of lossless dielectric with permittivity n1 = 3.5. As it has been already mentioned before, here
we focus on 2D electrodynamics which means that all fields

## PDF page 3

3
are independent of y. This can be achieved by choosing the
x0z-plane as the plane of incidence. Further on we focus on
the transverse electric wave (s-waves) with the electric vector
perpendicular to the plane of incidence. Albeit the scattering of light is controlled by vectorial Maxwell’s equations the
problem can be reduced to a single scalar equation for the ycomponent of the electric field while the other components are
equal to zero
)
( 2
∂2
ω2
∂
+
Ey (x, z) + ε(x, z) 2 Ey (x, z) = 0,
(1)
2
2
∂x
∂z
c
where ε(x, z) is the dielectric function, ω is the angular frequency of the incident light, and c is the speed of light.
In the far-field the dielectric function is constant, thus, the
monochromatic solutions are plane waves
Ey (x, z) ∝ e±ikx x±ikz z ,

n20 ω 2
= kx2 + kz2 ,
c2

(2)

where n0 = 1.5 is the refractive index of the ambient medium,
and kx,z are the corresponding components of the wave vector.
Since the grating is periodic the solution has to comply with
the Bloch theorem
Ey (x, z) = Ey(0) (x, z)eiβ x , β Λ ∈ (−π, π],

(3)

where Ey(0) (x, z) is a periodic function of x with period Λ, and
β is the Bloch propagation constant. The conservation of
quasi-momentum requires kx = β + 2πm/Λ where index m
is known as the diffraction order. By setting kz = 0 one finds
the cut-off frequencies for the diffraction scattering channels
as follows
(
)
2πm
n0 ω = ±c β +
, m = −∞, . . . , −1, 0, 1, . . . , ∞. (4)
Λ

FIG. 2. Definition of the scattering channels for the structure shown
in Fig. 1 (a). θ is the angle of incidence.

open for incident/outgoing light. The scattering channels are
defined in Fig. 2, where the superscript (+) is used for the incident channels and (−) for the outgoing ones. We also assume
that the outgoing channels are linked to the incident ones via
the time-reversal operation. The 4×4 S-matrix is implicitly
defined through the following formula that relates the vectors
of incident and outgoing (scattered) amplitudes
s(−) = Ŝ4×4 s(+) ,

where the vectors of outgoing s(−) and incident s(+) amplitudes
are given by
 (±) 
s1
 s(±) 
2 
s(±) = 
 s(±)  .

The diagram of the diffraction channels is shown in Fig. 1 (b).
The specular reflection occurs when only the zeroth order
diffraction channel is open for propagation of light, i.e.
|kx | <

n0 ω
2π
<
− |kx |.
c
Λ

(5)

We assume that the metasurface supports an isolated rightgoing β > 0 resonant mode that does not overlap with the
other high-Q resonant modes on a frequency scale of its resonant width γ for any β . Since the mode is radiative it is
characterized by a complex eigenfrequency ω0 − iγ with ω0
being the resonance center-frequency. The resonant mode is
two-fold degenerate, so there is another resonant mode with
the same complex frequency but opposite Bloch wavenumber
−β . The amplitudes of these two counter-propagating modes
will be further denoted by a→ and a← with the index arrow
indicating the propagation direction.
We consider scattering of plane monochromatic waves in
the spectral domain where only specular reflection is possible, see Eq. (5). This assumption, together with the specified
incident frequency ω and the angle of incidence θ , drastically
simplify our analysis, since only four scattering channels are

(6)

(7)

3

s(±)
4
Note that in case θ ̸= 0 the time reversal changes the propagation direction of all waves with respect to the x-axis. Since
both the energy conservation s(−) † s(−) = s†(+) s(+) and the time
reversal s(±) = s∗(∓) are present with a lossless dielectric our
definition of scattering channels leads to the 4×4 scattering
matrix that is both symmetric
⊺
Ŝ4×4 = Ŝ4×4
,

(8)

†
−1
= Ŝ4×4
Ŝ4×4
.

(9)

and unitary

In addition the S-matrix must comply with the momentum
conservation which together with unitarity and symmetry of
the S-matrix yields
(
Ŝ4×4 =

0 Ŝ
Ŝ⊺ 0

)
,

(10)

## PDF page 4

4
where Ŝ is a 2×2 unitary matrix. Note that the matrix Ŝ does
not have to be symmetric. At this point we can only apply the
generic expression for the 2×2 unitary matrix
(
)
√
ρeiη iτeiξ
iψ
Ŝ = e
, τ ∈ [−1, 1], ρ = 1 − τ 2 , (11)
−iξ
−iη
iτe
ρe
where ψ, η, and ξ are real numbers. The matrix is dependent on four parameters but, as we shall see, three of them
can be removed by redefining the scattering channels. Care
is needed, though, since redefining the channels one should
preserve the time reversal symmetry of the channels. Let us
apply a diagonal transformation matrix
Û = diag(eiψ1 , eiψ2 , eiψ3 , eiψ4 )

(12)

to the incident channels so that
s̃(+) = Ûs(+) ,

(13)

then the outgoing channels have to be transformed as
s̃(−) = Û ∗ s(−) .

(14)

By substituting the unitary transformation into Eq. (10) one
finds that the choice
1
ψ1 = (ψ + η + ξ ),
2
1
ψ2 = (ψ − η − ξ ),
2
1
ψ3 = (ψ + η − ξ ),
2
1
ψ4 = (ψ − η + ξ )
2

(15)

leads to
(
Ŝ =

ρ iτ
iτ ρ

)
, τ ∈ [−1, 1], ρ =

√

1 − τ 2.

(16)

Thus, Ŝ can be written in the canonical form of a symmetric
unitary matrix. It is important to note that Ŝ4×4 is frequency
dependent. Therefore, albeit the structure of the matrix given
by Eq. (10) along with the unitarity of Ŝ is preserved in a frequency sweep, the transformation Û is also frequency dependent. More precisely, one can guaranty Eq. (16) only in a
single point in a frequency domain with a frequency independent Û. Note that Eq. (16) is identical to that proposed in [82]
up to an arbitrary phase factor.

modern TCMT formulation is to Fan, Suh, and Joannopoulos
who were the first to have put forward a number of important relationships for the system’s coefficients rendering the
TCMT tractable for describing Fano resonances in a single
mode approach [52]. Later, in [81] the TCMT was generalized
to the multi-modal case. Generalizations for arbitrary-shaped
objects with an infinite number of scattering channels are also
possible [91, 92]. More recently, the effects of the timereversal symmetry, energy conservation, and reciprocity on
the TCMT constraints were thoroughly investigated in [93].
The TCMT is akin to the plethora of resonant state expansion methods which have recently gained popularity in the
photonics community [94–96]. These methods also rely on series expansions into eigenmodes of Maxwell’s equation with
radiation boundary conditions. The difference is, though, that
the TCMT, being a phenomenological approach, does not utilize the explicit form of the eigenmodes, but rather establishes
the generic form of the optical response relying on physical
constraints such as symmetries and conservation laws. Practically, the TCMT solutions always contain unknown coefficients which are to be fitted to comply with exact full-wave
solutions obtained by numerically exact methods. In this work
we are going to apply the FDFD method [90]. Yet, the choice
of simulation method is, of course, always at the discretion of
the researcher, so other methods such as the increasingly popular finite-difference time-domain and finite-element methods
could have been equally applied. Finally, it is worth mentioning that recently some attempts have been made to put
the TCMT on more rigorous grounds by deriving the TCMT
equations from resonant mode expansions [83, 97, 98].
According to [81] the TCMT the relationship between s(+)
and s(−) can be written in the following form
da(t)
= [−iΩ̂ − Γ̂]a(t) + K̂ ⊺ s(+) (t),
dt
s(−) (t) = Ĉs(+) (t) + D̂a(t),

(17)

where a(t) is a column vector composed of the amplitudes of
the resonant eigenmodes supported by the photonic structure,
Ĉ – the matrix of direct (non-resonant) process, Ω̂ – the Hermitian matrix containing the natural frequencies of the resonant modes, Γ̂ – the Hermitian matrix of decay rates, K̂ is
the coupling matrix, and D̂ is the decoupling matrix. In the
frequency domain, i.e. for systems illuminated by monochromatic light, we apply a time-harmonic substitution for all
time-dependent quantities, e.g.
a(t) = ae−iωt ,

(18)

which leads to
III.

TCMT REVISITED

The key idea behind the TCMT is to cast the scattering
problem in the form of a system of coupled driven oscillators.
Each oscillator in the system represents an optical resonant
mode which can be excited by incident light. Mathematically,
in the TCMT framework the dynamics is controlled by a system of linear ordinary differential equations. The credit of the

[i(Ω̂ − ω Î) + Γ̂]a = K̂ ⊺ s(+) ,
s(−) = Ĉs(+) + D̂a.

(19)

Equation (19) are the basic equations to be used for finding
the S-matrix.
Now, for the sake of generality, assume that there are M
resonant modes coupled with N scattering channels. Then the

## PDF page 5

5
quantities in Eq. (17) are as follows. The vector a is a M×1
column vector, D̂ and K̂ are N×M matrices, and Ĉ is a N×N
matrix. In the same manner as in [81], by taking into account
the photon number conservation in radiation loss from an unpumped system one can show that Eq. (17) leads to
2Γ̂ = D̂† D̂.

(20)

At the same time the general solution for the S-matrix can be
obtained from Eq. (19) as follows
Ŝ(ω) = Ĉ + D̂

1
i(Ω̂ − ω Î) + Γ̂

K̂ ⊺ .

(21)

The following useful relationships can be derived from
Eq. (26) and Eq. (27)

i(Ω̂ − ω Î) + Γ̂

M

m=1

m=1

(22)

(28)

(29)

Now we are well equipped for analyzing Eq. (22). By plugging Eq. (28) into Eq. (22) one finds
i ∑ Ĉ∗ D̂
m=1
M

∑

m,m′ =1

1

D̂†Ĉ + Ĉ∗ D̂
K̂ ⊺
−i(Ω̂ − ω Î) + Γ̂
i(Ω̂ − ω Î) + Γ̂
1
1
Γ̂
+ 2K̂ ∗
K̂ ⊺ = 0.
−i(Ω̂ − ω Î) + Γ̂ i(Ω̂ − ω Î) + Γ̂

K̂ ∗

M

2Γ̂ = i ∑ (ωm − ω)am b⊺m − i ∑ (ωm∗ − ω)b∗m a†m .

2
1

1
am b⊺m ,
ω
−
ω
m
m=1

= −i ∑

and

M

The unitarity of the S-matrix given by Eq. (21) leads to a rather
awkward equation

M

1

M
am b⊺m ⊺
b∗ a†
K̂ − i ∑ K̂ ∗ ∗m m D̂†Ĉ =
ωm − ω
ωm − ω
m=1

K̂ ∗

am′ b⊺m′ ⊺
b∗m a†m
Γ̂
K̂ ,
ωm∗ − ω ωm′ − ω

(30)

Substituting Eq. (29) into Eq. (30) and collecting the terms
with the same poles in the ω-plane one obtains
K̂ ∗ b∗m a†m (D̂†Ĉ + K̂ ⊺ ) = 0.

(31)

To make use out of Eq. (22) we consider the eigenvalue problem

After summation over m and application of Eq. (26) we have

(iΩ̂ + Γ̂)am = iωm am .

In the same manner it can be shown that the symmetry of the
S-matrix leads to

(23)

In what follows we focus on the generic case when there exist M linearly independent, though not necessarily orthogonal,
eigenvectors. In the other words it is assumed that there are no
exceptional points [99] in the spectrum. The vectors am will
be termed the right eigenvectors of iΩ̂ + Γ̂. The right eigenvectors can be complemented with the left eigenvectors bm
which solve the eigenvalue problem
b⊺m (iΩ̂ + Γ̂) = iωm b⊺m .

(24)

It is possible to show that the right and left eigenvectors can be
normalized such that the following orthonormalization condition holds true
b⊺m am′ = δm,m′ .

(25)

Note that am are not orthogonal in terms of the skewsymmetric inner product a†m am′ ̸= δm,m′ . Thus, one would
rather say that am and bm form a bi-orthogonal basis [100].
Since the vector space dimensionality is finite one can show
that the biorthoganal vectors resolve the identity operator as
follows
M

Î = ∑

am b⊺m .

(26)

m=1

The matrix in the TCMT equations Eq. (19) can be written in
terms of the left and right eigenvectors

∑

D̂K̂ ⊺ = K̂ D̂⊺ .

(32)

(33)

It is worth mentioning that the above equation may also hold
for lossy systems, see the supplemental to [82], since it can be
derived solely relying on the Lorentz reciprocity.
Let us now analyze our findings. First of all we recall that
according to [81] the TMCT matching condition in the presence of energy conservation and time-reversal symmetry have
the following form
ĈD̂∗ + D̂ = 0,
D̂ = K̂.

(34)

One can easily see that if the matrices D̂ and K̂ satisfy Eq. (34)
then they also solve the new found Eq. (32) and Eq. (33). One
can argue, however, that there are solutions of Eq. (32) and
Eq. (33) not accommodated in Eq. (34). To see this, consider
a unitary transformation in space of the resonator eigenmodes
a → a′ , bearing in mind that unitarity is necessary for maintaining Eq. (20). This unitary transfromation can be written
as
a = Ûa′ ,

(35)

where Û is a unitary matrix. By plugging Eq. (35) into the
TCMT equations Eq. (17) we find that the matrix quantities
are transformed as follows
iΩ̂′ + Γ̂′ = Û † (iΩ̂ + Γ̂)Û,
D̂′ = D̂Û,

M

i(Ω̂ − ω Î) + Γ̂ = i
(ωm − ω)am b⊺m .
m=1

K̂ ∗ (D̂†Ĉ + K̂ ⊺ ) = 0.

(27)

K̂ ′ = K̂Û ∗ .

(36)

## PDF page 6

6
One can easily check that the TCMT matching conditions
given by Eq. (20), Eq. (32), and Eq. (33) are invariant to any
unitary transformation whereas Eq. (34) is not. This is a consequence of that the matrix K̂ is covariant with a while D̂ is
contra-variant. The U(M) invariant matching conditions that
we have derived in this section obviously lead to new solutions
not accommodated in Eq. (34) after some unitary transformations.
IV.

TCMT FOR A 2D METASURFACE

Let us now apply the results of the previous section to the
system introduced in Sec. II. The 4×4 S-matrix, which was
defined in Eq. (6) can be rewritten in a more convenient form
( (−) ) (
) ( (+) )
s←
0 Ŝ
s→
=
,
(37)
s(−)
s(+)
Ŝ⊺ 0
→
←
where
( (±) )
( (±) )
s1
s3
(−)
(+) (−)
s(+)
,
s
=
,
s
,
s
=
.
→
←
←
→
s(±)
s(±)
2
4

(38)

Note that the orientation of the subscript arrows in the above
equations corresponds to the wave propagation direction with
respect to the x-axis according to Fig. 2. Thus, taking into
account the momentum conservation [82] the coupling and
decoupling matrices can also be written in a simplified form
as follows
(
)
(
)
(
)
0 κ→
κ1
κ3
K̂ =
, κ→ =
, κ← =
, (39)
κ← 0
κ2
κ4
and
(
D̂ =

d← 0
0 d→

)

(
, d→ =

d3
d4

)

(
, d← =

d1
d2

)
,

(40)

where the subscript enumerates the scattering channels according to Fig. 2. The coupling and decoupling matrices are
of a block form in compliance with the momentum conservation. In accordance with our definition of D̂ and K̂ the time
domain TCMT equations (17) take the following form
(
) (
)(
)
( (+) )
d a←
−iω0 − γ
0
a←
s→
⊺
=
+ K̂
,
0
−iω0 − γ
a→
s(+)
dt a→
←
( (−) )
( (+) )
(
)
s←
s→
a←
= Ĉ4×4
+ D̂
.
(41)
a→
s(−)
s(+)
→
←
In the next step we apply the TCMT matching equations
Eq. (20), Eq. (32), and Eq. (33). Equation (33) yields
(
)
κ→ 0
D̂ = A
,
(42)
0 κ←
where A is an arbitrary complex number. Substituting the
above into D̂† D̂ = 2Γ̂ gives
√
2γ
iζ
A=e
,
(43)
κ2

where ζ ∈ [0, 2π) is a real number and
†
†
κ 2 = κ←
κ← = κ→
κ→

(44)

so the vectors κ← and κ→ are equal in the norm. Before applying Eq. (32) we recall that according to Eq. (10) and Eq. (16)
the 4×4 S-matrix can be written in a block form with a symmetric unitary matrix off the main diagonal at any given frequency. Here we apply this result to the matrix of the direct
process which, being independent of frequency, can be written
as follows
(
)
0 Ĉ
Ĉ4×4 =
,
(45)
Ĉ 0
where
(
Ĉ =

ρ iτ
iτ ρ

)
.

(46)

After using Eq. (32) and assuming in accordance with γ > 0
that both vectors κ← and κ→ have at least one non-zero element we arrive at
√
2γ
−iζ
e
Ĉκ ∗ + κ← = 0,
κ2 →
√
2γ
−iζ
e
Ĉκ ∗ + κ→ = 0.
(47)
κ2 ←
The solution of the above equation is any vector κ→ (κ← ) that
satisfies the normalization condition
κ 2 = 2γ.

(48)

Now, our goal is to write such a solution in a form symmetric with respect to both κ→ and κ← . To do this we introduce
matrix B̂ that is a symmetric unitary square root of −Ĉ so that
B̂B̂ = −Ĉ,
B̂⊺ = B̂,
B̂B̂† = Î.
Matrix B̂ can be explicitly written as
(
)
1
τ
−i(1 + ρ)
.
B̂ = √
τ
2(1 + ρ) −i(1 + ρ)

(49)

(50)

Having in mind Eq. (49) the solution of Eq. (47) can be written
as
√
κ→ = 2γe−iζ /2 B̂n∗ ,
√
κ← = 2γe−iζ /2 B̂n,
(51)
where n is any 2 × 1 vector such as n† n = 1. The S-matrix for
the right going waves is then written as
Ŝ = Ĉ +

2γ
B̂nn† B̂.
i(ω0 − ω) + γ

(52)

## PDF page 7

7
For the left-going waves the S-matrix is the transpose of
Eq. (52) according to Eq. (10). Using Eq. (49) it is possible to
demonstrate that Ŝ is a unitary matrix.
The unit vector n can be parametrized by three variables
(
)
cos α e+iδ /2
iχ
n=e
,
sin α e−iδ /2
χ ∈ [0, 2π), α ∈ [−π/2, π/2], δ ∈ [0, π),

(53)

which leads to the following solution for the transmittance
T=

[τ(ω0 − ω) + ργ sin(2α) cos δ ]2 + γ 2 sin2 (2α) sin2 δ
.
(ω0 − ω)2 + γ 2
(54)

Note that the above result is independent of the choice of the
incidence channel. In contrast, the analytic expressions for
the squared resonant mode amplitude are different depending
on the direction of incidence. When the metasurface is illuminated through channel s(+)
1 the solution reads
|a→ |2 =

γ[1 − ρ cos(2α) + τ sin(2α) sin δ ]
,
(ω0 − ω)2 + γ 2

(55)

FIG. 3. All possible symmetries of the elementary cell; A – fully
symmetric, B – out-of-plane mirror symmetry, C – in-plane mirror
symmetry, D – inversion symmetry, E – asymmetric.

whereas with channel s(+)
3 the solution is
|a← |2 =

γ[1 − ρ cos(2α) − τ sin(2α) sin δ ]
.
(ω0 − ω)2 + γ 2

(56)

The solution for the S-matrix Eq. (52) does not depend on the
phases χ and ζ . Further on we set χ = 0, ζ = 0, which gives
d← = κ→ , d→ = κ← .

(57)

The expression for the coupling vectors can be written as
(
)
√
γ
τ cos α e∓iδ /2 − i(1 + ρ) sin α e±iδ /2
κ→,← =
.
1 + ρ −i(1 + ρ) cos α e∓iδ /2 + τ sin α e±iδ /2
(58)
Since the Fano resonance is a product of interference between a resonant and a non-resonant pathways, the following
generic expression holds for the transmittance coefficients
∣
∣2
∣
A2 ei∆ ∣∣
∣
T = ∣A1 +
,
Ω+i∣

where p ∈ [0, 1] is the interaction coefficient [101]
p=

2F cos2 ∆
√
,
F + 2 sin ∆ + F 2 + 4F sin ∆ + 4

(64)

F = A2 /A1 is the relative intensity, and q is the Fano asymmetry parameter,
q=

F cos ∆
.
p

(65)

Thus, we have demonstred that Eq. (54) complies with the
generic theories of the Fano responce.

(59)

where A1 , A2 , ∆2 are real numbers, and Ω = (ω − ω0 )/γ.
Equation (59), besides Ω, depends on three real-valued parameters, same as Eq. (54). It is possible to show after some
algebra that the parameters in Eq. (54) and Eq. (59) are linked
by the following formulas
A1 = |τ|,
√
A2 = (τ + sin(2α) sin δ )2 + ρ 2 sin2 (2α) cos2 δ ,
(
)
ρ sin(2α) cos δ
π
∆ = − arctan
− sign (τ) .
τ + sin(2α) sin δ
2

Alternatively, according to [50], the Fano formula (59) can be
also expressed as
]
[
(q + Ω)2
p + (1 − p) A21 ,
(63)
T=
1 + Ω2

(60)
(61)
(62)

V.

SYMMETRIES AND NUMERICAL VALIDATION

In this section we present numerical results obtained by the
FDFD in support of our findings. All possible symmetries of
the metasurface elementary cell are considered according to
the scheme shown in Fig. 3 where we demonstrate the geometric shapes along with their group-theoretical notations [102].
The symmetry operations can be described with the use of the
first Pauli matrix
(
)
0 1
σ̂x =
(66)
1 0

## PDF page 8

8

FIG. 4. Transmission through fully symmetric metasurface. (a) The spectra of the high-Q leaky band calculated by FDFD with the mode
profiles shown on top. (b) Transmittance and the energy stored by the FDFD and the TCMT methods. (c) Transmittance against the incident
frequency; TCMT – dotted line, FDFD – solid line. The scattering solutions at ω = ω0 are shown on the right of each plot. The geometry is
described in the inset in subplot (a); w = 0.675Λ, h = 0.3Λ.

acting on the coupling vectors. Care is needed, though, as the
channel functions are in general not mapped onto each other
after the unitary transformation Eq. (12) that brings Ĉ4×4 to
the simplified form given by Eq. (45). This means that the
non-zero elements of all matrix representations of the symmetry operation will acquire phase factors in accordance with
Eq. (12). Therefore, the conditions imposed by the symmetries can only be expressed by equating the absolute values of
the elements of the coupling vectors.
In all simulations, a plane wave is incident from the halfspace z < 0. In accordance with Fig. 2, this means that the
(+)
incident channels are s(+)
1 if kx > 0, and s3 if kx < 0. For convenience in notation, we shall use the reciprocal lattice constant G, which is related to the lattice period Λ
G=

A.

2π
.
Λ

(67)

Fully symmetric case

We start from the case of full symmetry. The spectrum
of the real and imaginary parts of the leaky band resonant
eigenfrequencies calculated by the FDFD method is shown in
Fig. 4 (a). The profiles of the eigenmodes are shown on top of
the subplot. Notice that in the Γ-point β /G = 0 the imaginary
part of the complex eigenfrequency equals zero. This indicates the presence of a symmetry protected BIC. The BICs
of this type are omnipresent in dielectric gratings [103] due

to the Friedrich-Wintgen coupling [104] between two degenerate guided modes folded into the first Brillouin zone [105].
Since the system retains two mirror symmetries, the coupling
vector must simultaneously satisfy
|κ1 | = |κ2 |, |κ3 | = |κ4 |,
|κ1 | = |κ3 |, |κ2 | = |κ4 |.

(68)

After applying the above equations to Eq. (58) one finds that
α = ±π/4, δ = 0.

(69)

Since the eigenmode is symmetric with respect to inversion
of the z-axis, we choose α = π/4. Thus, we are left with a
single unknown parameter τ in applying the TCMT solutions
Eqs. (54–56). In general, the parameter τ can be dependent
on the angle of incidence. In order to fit the TCMT formulas
to the numerical spectra we interpolate α and τ in the range
kx /G ∈ [0, 0.1] by the following formulas
α=

π
,
4

τ = −0.790 − 0.113

kx
.
G

(70)

In the upper panel of Fig. 4 (b) we show the transmittance T
calculated by both the FDFD and the TCMT approaches. Note
that now the spectra are plotted against the x-component of the
wave vector kx in the surrounding medium. In full consistence
with Fig. 4 (a) we observe a narrow Fano feature which collapses at the Γ-point. In the bottom panel of Fig. 4 (b) we

## PDF page 9

9

FIG. 5. Transmission through metasurface with only out-of-plane mirror symmetry. (a) The spectra of the high-Q leaky band calculated by
FDFD with the mode profiles shown on top. (b) Transmittance and the energy stored by the FDFD and the TCMT methods. (c) Transmittance
against the incident frequency; TCMT – dotted line, FDFD – solid line. The geometry is described in the inset in subplot (a). The scattering
solutions at ω = ω0 are shown on the right of each plot. The in-plane mirror symmetry is broken by setting φ = 80◦ according to the scheme
shown in Fig. 3.

compare the energy stored in the dielectric grating E calculated by FDFD against the squared amplitude of the resonant
eigenmodes |a|2 = |a←,→ |2 calculated by Eq. (55) and Eq. (56).
In Fig. 4 (c) we demonstrate the profile of the Fano resonance
at three different values of kx together with the scattering solutions at ω = ω0 . Notice that in the case of normal incidence
kx /G = 0 the scattering field does not resemble the resonant
mode profile from Fig. 4 (a). The reason for this is that the
high-Q leaky mode becomes a BIC in the Γ-point and the scattering solution is given by the background. The background is
due to low-Q frequency modes [105], so one can clearly see
that there is a residual dependence on ω that leads to a discrepancy between the TCMT and the FDFD methods. Also,
notice that the transmittance reaches both zero and unity in the
vicinity of the resonant eigenfrequency. In fact, this result is
identical to the transmittance formula presented in [52].

symmetry protected BIC is destroyed and the imaginary part
of the resonant eigenfrequency does not equal zero in the Γpoint. The only condition that the coupling vector must satisfy
is
|κ1 | = |κ2 |, |κ3 | = |κ4 |.

Although we now have one less symmetry condition than in
the fully symmetric case, Eq. (58) results in the same solution
α = ±π/4, δ = 0.

Out-of-plane mirror symmetry

Now consider the situation when the in-plane mirror symmetry is broken whereas the out-of-plane mirror symmetry is
retained. The spectrum of the real and imaginary parts of the
leaky band resonant eigenfrequencies calculated by the FDFD
method is shown in Fig 5 (a). The profiles of the eigenmodes
are shown on top of the subplot. The symmetry is broken by
changing the angle φ as shown in the inset in Fig. 5 (a). Since
the system does not have the in-plane mirror symmetry the

(72)

As before, since the mode is symmetric we take α = π/4. The
parameters are interpolated in the range kx /G ∈ [0, 0.1] by the
following formula
α=

π
,
4

τ = −0.834 − 0.113
B.

(71)

kx
.
G

(73)

In the upper panel of Fig. 5 (b) we show the transmittance
T calculated by both the FDFD and the TCMT approaches.
As before we observe a narrow Fano feature which, however,
does not collapse in the Γ-point. The electromagnetic energy
stored in the dielectric grating E calculated by the FDFD is
compared with the squared amplitude of the resonant eigenmodes calculated by Eq. (55) and Eq. (56) in the lower panel
of Fig. 5 (b). In Fig. 5 (c) we demonstrate the profile of the
Fano resonance at three different values of kx together with

## PDF page 10

10

FIG. 6. Transmission through metasurface with only in-plane mirror symmetry. (a) The spectra of the high-Q leaky band calculated by FDFD
with the mode profiles shown on top. (b) Transmittance and the energy stored by the FDFD and the TCMT methods. (c) Transmittance against
the incident frequency; TCMT – dotted line, FDFD – solid line. The geometry is described in the inset in subplot (a). The scattering solutions
at ω = ω0 are shown on the right of each plot. The out-of-plane mirror symmetry is broken by setting φ = 70◦ according to the scheme shown
in Fig. 3.

the scattering solutions at ω = ω0 . Now in the case of normal
incidence kx /G = 0 the scattering field looks similar to the
resonant mode profile from Fig. 5 (a), since the high-Q mode
couples with incident light at all incident angles. In all other
aspects the results are identical to those obtained for the fully
symmetric structure. Thus, we conclude that the only effect
of breaking the in-plane mirror symmetry while the out-ofplane symmetry is preserved is destruction of the symmetry
protected BIC. We mention in passing that the interpolation
coefficients in Eq. (73) do not change significantly in comparison to the fully symmetric case, Eq. (70). The direct process
transmission amplitude τ is almost independent of the angle
of incidence.

C.

In-plane mirror symmetry

The in-plane mirror symmetry requires that
|κ1 | = |κ3 |, |κ2 | = |κ4 |,

(74)

which together with Eq. (58) leads to
δ = 0.

(75)

Notice that now we have two independent parameters τ and
α which have to be interpolated in the range kx /G ∈ [0, 0.1].
The results of our numerical simulations are shown in Fig. 6.
As before in subplot (a) we demonstrate the dispersion of the

high-Q eigenmode with the eigenmode profiles shown above
the dispersion curve. The two unknown parameters are interpolated by the formulas below
τ = −0.792 − 0.113

kx
,
G

π
α = 1.24 .
(76)
4
The comparison between the TCMT and FDFD solutions in
the whole interpolation range is shown in Fig. 6 (b). In
Fig. 6 (c) are shown the profiles of Fano resonances with
the corresponding scattering solutions at ω = ω0 presented
on the right of each plot. One can see that since the in-plane
mirror symmetry is present, the symmetry protected BIC is
preserved. On the other hand, one can see in Fig. 6 (c) that
the resonance does not reach unity at its peak. The analysis of Eq. (54) shows that a unity transmission at the peak of
the Fano resonance is only possible with α = ∓π/4 which
would indicate the (anti)symmetry of the coupling with the
scattering channels in the upper and lower half-spaces. This
asymmetry in the coupling is a direct consequence of broken
out-of-plane mirror symmetry. This case is important from
the application view-point since in realistic set-ups the out-ofplane mirror symmetry is broken by a substrate. It is worth
mentioning that α = ±π/4 is not strictly forbidden by broken
out-of-plane mirror symmetry. Yet, a robust reflection zero
is difficult to engineer, since it only occurs in two points out
of α ∈ [−π/2, π/2] while the symmetry breaking favors solutions with asymmetric coupling α ̸= ±π/4.

## PDF page 11

11

FIG. 7. Transmission thorough metasurface with only inversion symmetry. (a) The spectra of the high-Q leaky band calculated by FDFD with
the mode profiles shown on top. (b) Transmittance and the energy stored by the FDFD and the TCMT methods. (c) Transmittance against the
incident frequency; TCMT – dotted line, FDFD – solid line. The geometry is described in the inset in subplot (a). The scattering solutions at
ω = ω0 are shown on the right of each plot. The mirror symmetries are broken by setting φ = 70◦ according to the scheme shown in Fig. 3.

D.

Inversion symmetry

This symmetry can be prescribed by simultaneously flipping the coupling vector and changing the propagation direction to yield
|κ1 | = |κ4 |, |κ2 | = |κ3 |.

(77)

The above equation together with Eq. (58) results in
π
α =± .
4

(78)

The spectrum of the radiative mode together with the field
profiles is shown in Fig. 7 (a). One can see in Fig. 7 (a) that
because the in-plane mirror symmetry is broken there is no
symmetry protected BIC in the Γ-point. Since the eigenmode
is antisymmetric with respect to inversion, we take α = −π/4.
Thus, in the case of inversion symmetry we have two unknown
parameters, τ and δ , both dependent on the angle of incidence.
In addition, at normal incidence we have κ→ = κ← which dictates δ = 0 if kx /G = 0. Therefore, for applying the TCMT
formulas, we interpolate the parameters as follows
π
α =− ,
4
kx
,
G
( )2
kx
kx
δ = 49.61 − 258.5
.
G
G

In the upper panel Fig. 7 (b) we show the transmittance T
while the lower panel shows the energy E stored in the metasurface as functions of kx and ω. Notice that, unlike the
transmittance, the energy stored is asymmetric with respect
to kx → −kx . This is a consequence of δ ̸= 0 and n ̸= n∗ in
Eq. (53). Equivalently, one can state that κ→ ̸= κ← if kx ̸= 0.
According to Eq. (57) the coupling and decoupling vectors for
the guided mode are not equal to each other, κ←,(→) ̸= d←,(→) .
The asymmetry between the coupling and decoupling coefficients manifests itself in the absence of transmittance zeros,
see Fig. 7 (c), except at normal incidence where the couplingdecoupling symmetry is restored. It is also interesting to point
out that, unlike to the previous cases where we found that both
α and τ only slightly depend on the angle of incidence, in the
case of the inversion symmetry the parameter δ varies significantly within the interpolation range. One can see in Fig. 7 (c)
that the Fano resonance occurs in different shapes at different angles of incidence. Its profile can be flipped about the
center-frequency, as it can be seen by comparing kx /G = 0
and kx /G = 0.1. The resonance is found to be symmetric
(Lorentzian) at kx /G = 0.04 in which case δ = π/2.

E.

τ = −0.782 − 0.170

(79)

Asymmetric metasurface

For a metasurface with a fully asymmetric elementary cell
there are no extra constraints on parameters in Eq. (58) except
κ→ = κ← at normal incidence. Thus, we have to interpolate
all three parameters τ, α, and δ . The following formulas are

## PDF page 12

12

FIG. 8. Transmission through a fully asymmetric metasurfaces. (a) The spectra of the high-Q leaky band calculated by FDFD with the mode
profiles shown on top. (b) Transmittance and the energy stored by the FDFD and the TCMT methods. (c) Transmittance against the incident
frequency; TCMT – dotted line, FDFD – solid line. The geometry is described in the inset in subplot (a). The scattering solutions at ω = ω0
are shown on the right of each plot. The symmetries are broken by setting φ = 70◦ according to the scheme shown in Fig. 3.

used for interpolation in this subsection.
kx
,
G
kx
α = −0.877 − 0.032 ,
G
( )2
( )3
kx
kx
kx
δ = 104.2 − 1414
+ 6459
.
G
G
G

τ = −0.787 − 0.119

(80)

Notice that, as always, δ = 0 at normal incidence. The spectrum of the real and the imaginary parts of the resonant eigenfrequency is shown in Fig. 8 (a). There is no in-Γ symmetry protected BIC since the in-plane mirror symmetry is broken. The simulation results for the transmittance and the energy stored are shown in Fig. 8 (b). Similarly to the case of
the inversion symmetry the energy stored in the metasurface
is asymmetric with respect to kx → −kx because in general
δ ̸= 0. The profiles of Fano resonances are shown in Fig. 8 (c)
for three different values of kx . One can see in Fig. 8 (c) that,
in the case of the asymmetric metasurface neither reflectance
nor transmittance zeros are generally present in the spectra.
The transmittance zeros only occur at δ = 0, i.e. at the normal
incidence. The parameters α and δ vary considerably within
the interpolation range to result in a variation of the shape of
the Fano resonance. Accidental recovery of α = ±π/4, leading to reflectance zeros, as well as δ = 0, leading to transmittance zeros, is not forbidden by the absence of symmetry. Yet,
transmittance and reflectance zeros could only be obtained by
fine-tuning of parameters and, therefore, are not robust to fabrication inaccuracies. For example, in the case kz /G = 0.1

depicted in the lower panel of Fig. 8 (c) the transmittance almost reaches, but not exactly equal to, unity. As it has been
mentioned in the introduction, the asymmetric metasurfaces
have recently attracted attention as a platform for engineering
UGRs. It is evident that the key to UGRs is asymmetry of decoupling vector which can be obtained at δ ̸= 0. In the next
section we apply the TCMT approach to UGRs.
VI.

UNIGUIDED AND UNICOUPLED RESONANT MODES

By definition an UGR is decoupled from outgoing radiation in one of the two outgoing channels. Without a loss of
generality we consider the situation when there is no outgoing radiation in channel s(−)
3 , see Fig. 2. Then, according to the
definitions introduced in Eq. (40) for the right-going waves we
should have d3 = 0. By using Eq. (58) and Eq. (57) one finds
that d3 = 0 and γ ̸= 0 result in two possible sets of conditions
τ = 0, α = 0,

(81)

and
δ=

π
,
2

tan α =

τ
.
1+ρ

(82)

The first set of conditions, Eq. (81), can be satisfied only in
asymmetric metasurfaces and metasurfaces with in-plane mirror symmetry. The second set of conditions, Eq. (82), can be

## PDF page 13

13
satisfied in both asymmetric metasurfaces and metasurfaces
with inversion symmetry. Note that in metasurfaces with inplane mirror symmetry a UGR can only occur on the zerotransmittance background, τ = 0, which is consistent with
[76]. At the same time, since for metasurfaces with inversion symmetry α = ±π/4 the second line in Eq. (82) dictates that a UGR is only possible with zero-reflectance background, ρ = 0, which is again consistent with [76]. Either
of the two sets of conditions, Eq. (81) and Eq. (82), can be
met by varying two geometric parameters. It is obviously a
time-consuming computational task since two equations have
to be satisfied simultaneously or, in the other words, UGRs
are non-robust to variation of geometry.
In a metasruface with in-plane mirror symmetry d→ = κ→ ,
so κ1 = 0, which means that the UGR is not only decoupled
from outgoing light in a certain channel, but also can not be
excited by incident light on the same side. The same conclusion holds true for the mode counter-propagating to the UGR.
Thus, UGRs occur in pairs d3 = 0, κ1 = 0 and d1 = 0, κ3 = 0.
In the case of the inversion symmetry the situation is similar,
but, according to Eq. (58), the zero coupling occurs on the
other side of the metasurface κ2 = 0. The UGRs again emerge
in pairs but now the zero-coupling and the zero-decoupling directions are swapped between the counter-propagating modes,
i.e. we have d3 = 0, κ2 = 0 and d2 = 0, κ3 = 0. The picture becomes more interesting when all symmetries are lifted
and Eq. (82) is satisfied. One can easily see that if d3 = 0 and
α ̸= ±π/4, then κ1,2 ̸= 0. Thus, the UGR is coupled with incident waves on both sides of the metasurface. We, however, remember that the coupling and decoupling vectors are swapped
when the propagating direction is reversed. Therefore, we always have κ3 = d3 . Thus, in an asymmetric metasurface an
UGR is dual to a counter-propagating mode decoupled from
incident radiation from one of the sides of the metasurfaces.
We suggest to term this type of mode unidirectional coupled
resonant mode (UCR). Notice, that, unlike UGR, the UCR can
radiate into both half-spaces.
To verify our finding we applied the TCMT model to a
UGR in the asymmetric metasurface from the previous section. First, an UGR was found by varying the geometry of the
elementary cell in the point ω0 /Gc = 0.3939, kx /G = 0.0708.
Second, the numerical spectra were compared with the TCMT
predictions. The results are shown in Fig. 9. In Fig. 9 (a)
we show the scattering solutions in the points of the UGR
and UCR. In Fig. 9 (b) we demonstrated the UGR and UCR
mode shapes. Finally, in Fig. 9 (c) we compare the numerical results for the transmittance and the energy stored with
the TCMT model. One can see in Fig. 9 (b) that the UGR
is a right-going wave decoupled from the channel s(−)
3 . The
corresponding scattering solution is found by illuminating the
system through channel s(+)
1 . Note that in the case of UGR
the scattering solution is similar to the UGR eigenmode and
a resonant field enhancement is visible in the spectrum of the
energy stored. One the other hand, the UCR, i.e. the leftgoing mode counter-propagating to the UGR, radiates to both
sides of the metasurface, see Fig. 9 (b). The UCR is, however,
not excited by a plane wave incident in channel s(+)
3 indicating a unidirectional coupling to incident light, κ3 = 0. One

FIG. 9. Uniguided and unicoupled resonances in asymmetric metasurface. The symmetries are broken by setting φ = 33.42◦ according to Fig. 3. The spectral position of UGR (UCR) is given by
ω0 /Gc = 0.3939, kx /G = ±0.0708. (a) The scattering solution in
the points of the UGR and the UCR. (b) The field profiles of the
UGR and the UCR eigenmodes. (c) Comparison between the FDFD
simulation and the TCMT models for transmittance T and the energy
stored E . The position of the UGR is shown by a green star. The position of the UCR is shown by a red dot.

can also see in Fig. 9 (c) that the TCMT model reproduces the
spectra to a good accuracy. The parameters were interpolated
by the formulas
kx
,
G
kx
α = −0.487 + 0.345 ,
G
( )2
kx
kx
δ = 31.57 − 128.8
,
G
G

τ = −0.776 − 0.299

that satisfy Eq. (82) in the UGR point.

(83)

## PDF page 14

14
For the sake of completeness, it is worth writing down
the exact analytic expression for the S-matrix at the UGR
point according to Eq. (52). In doing so, one should remember that Eq. (52) is obtained after the unitary transformation
Eq. (12) that redefined the scattering channels. After returning
to the most generic expression for the S-matrix, Eq. (10) and
Eq. (11), one can write all non-zero elements of the S-matrix
as follows
]
[
i(ω0 − ω) − γ
,
S41 = S14 = iτei(ψ+ξ )
i(ω0 − ω) + γ
[
]
i(ω0 − ω) − γ
S42 = S24 = ρei(ψ−η)
,
i(ω0 − ω) + γ
S31 = S13 = ρei(ψ+η) ,
S32 = S23 = iτei(ψ−ξ ) .

(84)

Note that the absolute values of all matrix elements are independent of frequency. Thus, only the phase of the scattered
wave is frequency dependent if a UGR or a UCR is excited.
This phenomenon has been applied for engineering intensity
flattened phase shifting in [75–77].
VII.

SUMMARY AND CONCLUSIONS

We proposed a temporal coupled mode theory (TCMT) for
resonant response from quasi-guided modes in periodic dielectric metasurfaces. A generic set of constraints imposed
onto the parameters of the temporal coupled mode theory by
energy conservation and time-reversal symmetry is derived. It
is demonstrated that the proposed approach allows for asymmetry between the coupling and decoupling coefficients. In
particular, the TCMT approach is applied to the problem of
Fano resonances induced by isolated quasi-guided modes in
the regime of specular reflection. We derived a generic formula, Eq. (54), for the line-shape of the Fano resonance in
transmittance for the lossless metasurfaces in the framework
of 2D electrodynamics. An analytic expression for the Fano
asymmetry parameter, Eq. (65), is found. It is demonstrated
that our approach is applicable to all possible symmetries of
the metasurface elementary cell. In particular, the approach
explains the effects of the symmetry on the profile of the Fano
resonance induced by an isolated high-Q mode. It is shown
that the proposed approach correctly describes the presence
of robust reflection and transmission zeros in the spectra as
well as the spectral signatures of bound states in the continuum (BICs).
Thus far, there have been many attempts to derive the line
shapes of the Fano resonances relying on the spectra of radiative modes [65, 83, 88, 106–111] including systems with
reflectionless scattering modes [82, 112]. In particular, the
TCMT was applied for analyzing the fundamental bounds on
decay rates in asymmetric single-mode optical resonators with
two scattering channels in [109], where it was shown that full
reflection is always achievable at a Fano resonance, even for
structures lacking mirror symmetries, whereas full transmis-

sion can only be seen in a symmetric configuration where
the two decay rates are equal. In the context of the present
work, the above result corresponds to normal incidence at
which transmittance is always zero at the minimum of the resonant line if the high-Q mode is excited. At the same time reflectance zeros are only possible if either inversion or in-plane
mirror symmetries are preserved. Our approach also complies
with the earlier work on photonic crystal slabs [108] where
the authors reported that reflectivity peaks to unity near the
quasiguided mode resonance for normal light incidence in the
absence of diffraction, depolarisation, and absorptive losses,
while for the oblique incidence the full reflectivity is reached
only in symmetrical systems. Interestingly, only in-plane mirror symmetry does not guaranty the absence of reflectance zeros which can be obtained by fine-tuning the system’s parameters [111], such reflectance zeros are, however, non-robust.
For oblique incidence it was demonstrated many times
[106, 110, 113] that both reflectance and transmittance zeros simultaneously occur in symmetric metasurfaces. More
recently, Zhou and co-workers proposed a TCMT model that
can take into account all possible symmetries of the elementary cell [82]. Similarly to the model presented, their approach also implies asymmetry between the coupling and
the decoupling matrices that manifests itself in the relationship D̂ = K̂ σ̂x . Moreover, the authors came to the same
conclusion that the inversion symmetry only allows for robust reflectance zeros at oblique incidence, meanwhile the
in-plane mirror symmetry only permits robust zeros in transmittance. Nethertheless, the TCMT solution for reflectance
derived in [82], is not generic as it does not reproduce the
frequency independent transmittance/reflectance in the point
unidirectional guided resonance (UGR) [114]. The approach
presented here is found to be consistent with the existence of
UGRs. It is shown to correctly describe the transmittance and
resonant field enhancement in the spectral vicinity of an UGR
in metasurfaces with an asymmetric elementary cell. The analytic expression for the S-matrix in the UGR point is found
to be consistent with the previously reported effect of intensity flattened phase shifting [75–77]. Furthermore, in the case
of asymmetric metasurfaces the theory predicts that a UGR is
dual to a counter-propagating mode of a peculiar type which
is coupled with the outgoing wave on both sides of the metasurface but, nonetheless, exhibits only a single-sided coupling
with incident waves. This type of mode, which we termed a
unidirectional coupled resonance (UCR) is confirmed numerically.
The discussion is summarized in TABLE I. We believe that
the results presented can be of use in engineering Fano response from dielectric metasurfaces as well as pave a way for
application of TCMT in nanophotonics. In particular, generalizations for lossy systems are required for describing enhanced light-matter interaction in the critical coupling regime.
This work received financial support from the Ministry of
Science and Higher Education of Russian Federation (Project
No. FSRZ-2023-0006). DNM appreciates discussions with
Alexander E. Ershov.

## PDF page 15

15

Symmetry

Full symmetry

Out-of-plane mirror

In-plane mirror

Inversion

Asymmetric

Parameters in Eq. (54),
oblique incidence

τ ∈ [−1, 1],
δ = 0,
α = ±π/4

τ ∈ [−1, 1],
δ = 0,
α = ±π/4

τ ∈ [−1, 1],
δ = 0,
α ∈ [−π/2, π/2]

τ ∈ [−1, 1],
δ ∈ [0, π),
α = ±π/4

τ ∈ [−1, 1],
δ ∈ [0, π),
α ∈ [−π/2, π/2]

Parameters in Eq. (54),
normal incidence

τ ∈ [−1, 1],
δ = 0,
α = ±π/4

τ ∈ [−1, 1],
δ = 0,
α = ±π/4

τ ∈ [−1, 1],
δ = 0,
α ∈ [−π/2, π/2]

τ ∈ [−1, 1],
δ = 0,
α = ±π/4

τ ∈ [−1, 1],
δ = 0,
α ∈ [−π/2, π/2]

Symmetry protected BIC

+

−

+

−

−

Robust reflectance zeros

+

+

−

+

−

Robust transmittance zeros

+

+

+

only at normal incidence

only at normal incidence

Uniguided resonance, UGR

−

−

possible if τ = 0

possible if |τ| = 1

possible, see Eqs. (81), (82)

Unicoupled resonance, UCR

−

−

coincides with UGR

coincides with UGR

counter-propagating to UGR

TABLE I. Discussion summary.

[1] A. I. Kuznetsov, A. E. Miroshnichenko, M. L. Brongersma,
Y. S. Kivshar, and B. Lukyanchuk, Science 354, 2472 (2016).
[2] S. Campione, S. Liu, L. I. Basilio, L. K. Warne, W. L.
Langston, T. S. Luk, J. R. Wendt, J. L. Reno, G. A. Keeler,
I. Brener, and M. B. Sinclair, ACS Photonics 3, 2362 (2016).
[3] P. Genevet, F. Capasso, F. Aieta, M. Khorasaninejad, and
R. Devlin, Optica 4, 139 (2017).
[4] J. F. Algorri, D. C. Zografopoulos, A. Ferraro, B. GarciaCamara, R. Beccherelli, and J. M. Sanchez-Pena, Optics Express 27, 6320 (2019).
[5] K. Koshelev and Y. Kivshar, ACS Photonics 8, 102 (2020).
[6] S. G. Tikhodeev, A. Yablonskii, E. Muljarov, N. A. Gippius,
and T. Ishihara, Physical Review B 66, 045102 (2002).
[7] L. Huang, L. Xu, D. A. Powell, W. J. Padilla, and A. E.
Miroshnichenko, Physics Reports 1008, 1 (2023).
[8] V. Mocella and S. Romano, Physical Review B 92, 155117
(2015).
[9] S. Yuan, X. Qiu, C. Cui, L. Zhu, Y. Wang, Y. Li, J. Song,
Q. Huang, and J. Xia, ACS nano 11, 10704 (2017).
[10] D. G. Baranov, D. A. Zuev, S. I. Lepeshov, O. V. Kotov, A. E.
Krasnok, A. B. Evlyukhin, and B. N. Chichkov, Optica 4, 814
(2017).
[11] Y. Kivshar, National Science Review 5, 144 (2018).
[12] A. Kodigala, T. Lepetit, Q. Gu, B. Bahari, Y. Fainman, and
B. Kanté, Nature 541, 196 (2017).

[13] N. Shankhwar, R. K. Sinha, Y. Kalra, S. Makarov, A. Krasnok,
and P. Belov, Photonics and Nanostructures-Fundamentals and
Applications 24, 18 (2017).
[14] C. Huang, C. Zhang, S. Xiao, Y. Wang, Y. Fan, Y. Liu,
N. Zhang, G. Qu, H. Ji, J. Han, L. Ge, Y. Kivshar, and
Q. Song, Science 367, 1018 (2020).
[15] J.-H. Yang, Z.-T. Huang, D. N. Maksimov, P. S. Pankin, I. V.
Timofeev, K.-B. Hong, H. Li, J.-W. Chen, C.-Y. Hsu, Y.-Y.
Liu, T.-C. Lu, T.-R. Lin, C.-S. Yang, and C. Kuo-Ping, Laser
& Photonics Reviews 15, 2100118 (2021).
[16] S. I. Azzam, K. Chaudhuri, A. Lagutchev, Z. Jacob, Y. L. Kim,
V. M. Shalaev, A. Boltasseva, and A. V. Kildishev, Laser &
Photonics Reviews 15, 2000411 (2021).
[17] M.-S. Hwang, K.-Y. Jeong, J.-P. So, K.-H. Kim, and H.-G.
Park, Communications Physics 5, 106 (2022).
[18] S. Romano, G. Zito, S. Torino, G. Calafiore, E. Penzo, G. Coppola, S. Cabrini, I. Rendina, and V. Mocella, Photonics Research 6, 726 (2018).
[19] A. J. Ollanik, I. O. Oguntoye, G. Z. Hartfield, and M. D. Escarra, Advanced Materials Technologies 4, 1800567 (2018).
[20] F. Yesilkoy, E. R. Arvelo, Y. Jahani, M. Liu, A. Tittl,
V. Cevher, Y. Kivshar, and H. Altug, Nature Photonics 13,
390 (2019).
[21] M. L. Tseng, Y. Jahani, A. Leitis, and H. Altug, ACS Photonics 8, 47 (2020).

## PDF page 16

16
[22] J. Wang, J. Kühne, T. Karamanos, C. Rockstuhl, S. A. Maier,
and A. Tittl, Advanced Functional Materials 31, 2104652
(2021).
[23] D. Conteduca, I. Barth, G. Pitruzzello, C. P. Reardon, E. R.
Martins, and T. F. Krauss, Nature Communications 12, 3293
(2021).
[24] Z. Liu, T. Guo, Q. Tan, Z. Hu, Y. Sun, H. Fan, Z. Zhang, Y. Jin,
and S. He, Nano Letters 23, 10441 (2023).
[25] X. Liu, K. Fan, I. V. Shadrivov, and W. J. Padilla, Optics Express 25, 191 (2017).
[26] K. Fan, J. Y. Suen, X. Liu, and W. J. Padilla, Optica 4, 601
(2017).
[27] R. M. Saadabad, L. Huang, and A. E. Miroshnichenko, Physical Review B 104, 104 (2021).
[28] J. Tian, H. Luo, Q. Li, X. Pei, K. Du, and M. Qiu, Laser &
Photonics Reviews 12, 1800076 (2018).
[29] S. Chen, Z. Chen, J. Liu, J. Cheng, Y. Zhou, L. Xiao, and
K. Chen, Nanomaterials 9, 1350 (2019).
[30] I. A. M. Al-Ani, K. As’Ham, L. Huang, A. E. Miroshnichenko, W. Lei, and H. T. Hattori, Adv. Opt. Mater. 10,
2101120 (2022).
[31] X. Wu, S. Zhang, J. Song, X. Deng, W. Du, X. Zeng, Y. Zhang,
Z. Zhang, Y. Chen, Y. Wang, C. Jiang, Y. Zhong, B. Wu,
Z. Zhu, Y. Liang, Q. Zhang, Q. Xiong, and X. Liu, Nat. Commun. 15, 1 (2024).
[32] L. Sortino, J. Biechteler, L. Lafeta, L. Kühner, A. Hartschuh,
L. d. S. Menezes, S. A. Maier, and A. Tittl, arXiv (2024),
10.48550/arXiv.2407.16480, 2407.16480.
[33] M. A. Masharin, T. Oskolkova, F. Isik, H. Volkan Demir, A. K.
Samusev, and S. V. Makarov, ACS Nano 18, 3447 (2024).
[34] Y. Yang, W. Wang, A. Boulesbaa, I. I. Kravchenko, D. P.
Briggs, A. Puretzky, D. Geohegan, and J. Valentine, Nano
Letters 15, 7388 (2015).
[35] C. Schiattarella, S. Romano, L. Sirleto, V. Mocella, I. Rendina,
V. Lanzio, F. Riminucci, A. Schwartzberg, S. Cabrini, J. Chen,
L. Liang, X. Liu, and G. Zito, Nature 626, 765 (2024).
[36] Z. Liu, Y. Xu, Y. Lin, J. Xiang, T. Feng, Q. Cao, J. Li, S. Lan,
and J. Liu, Phys. Rev. Lett. 123, 253901 (2019).
[37] V. Kravtsov, E. Khestanova, F. A. Benimetskiy, T. Ivanova,
A. K. Samusev, I. S. Sinev, D. Pidgayko, A. M. Mozharov, I. S.
Mukhin, M. S. Lozhkin, Y. V. Kapitonov, A. S. Brichkin, V. D.
Kulakovskii, I. A. Shelykh, A. I. Tartakovskii, P. M. Walker,
M. S. Skolnick, D. N. Krizhanovskii, and I. V. Iorsh, Light
Sci. Appl. 9, 1 (2020).
[38] K. Koshelev, Y. Tang, K. Li, D.-Y. Choi, G. Li, and Y. Kivshar,
ACS Photonics 6, 1639 (2019).
[39] M. Sarrazin, J.-P. Vigneron, and J.-M. Vigoureux, Phys. Rev.
B 67, 085415 (2003).
[40] R. W. Wood, Phys. Rev. 48, 928 (1935).
[41] V. G. Kravets, A. V. Kabashin, W. L. Barnes, and A. N. Grigorenko, Chem. Rev. 118, 5912 (2018).
[42] G. W. Castellanos, P. Bai, and J. Gómez Rivas, J. Appl. Phys.
125 (2019), 10.1063/1.5094122.
[43] M. V. Rybin, K. L. Koshelev, Z. F. Sadrieva, K. B. Samusev,
A. A. Bogdanov, M. F. Limonov, and Y. S. Kivshar, Physical
Review Letters 119, 243901 (2017).
[44] V. E. Babicheva, A. B. Evlyukhin, A. B. Evlyukhin, and A. B.
Evlyukhin, Adv. Opt. Photonics 16, 539 (2024).
[45] M. B. Doost, W. Langbein, and E. A. Muljarov, Phys. Rev. A
90, 013834 (2014).
[46] S. Both and T. Weiss, Semicond. Sci. Technol. 37, 013002
(2021).
[47] P. Lalanne, W. Yan, K. Vynck, C. Sauvan, and J.-P. Hugonin,
Laser Photonics Rev. 12, 1700113 (2018).

[48] F. Alpeggiani, N. Parappurath, E. Verhagen, and L. Kuipers,
Phys. Rev. X 7, 021035 (2017).
[49] W. Zhou, D. Zhao, Y.-C. Shuai, H. Yang, S. Chuwongin,
A. Chadha, J.-H. Seo, K. X. Wang, V. Liu, Z. Ma, and S. Fan,
Progress in Quantum Electronics 38, 1 (2014).
[50] M. F. Limonov, M. V. Rybin, A. N. Poddubny, and Y. S.
Kivshar, Nature Photonics 11, 543 (2017).
[51] A. Krasnok, D. Baranov, H. Li, M.-A. Miri, F. Monticone, and
A. Alú, Advances in Optics and Photonics 11, 892 (2019).
[52] S. Fan, W. Suh, and J. D. Joannopoulos, Journal of the Optical
Society of America A 20, 569 (2003).
[53] J. M. Foley and J. D. Phillips, Optics Letters 40, 2637 (2015).
[54] A. Monti, A. Alù, A. Toscano, and F. Bilotti, IEEE Transactions on Antennas and Propagation 69, 5142 (2020).
[55] Y. Guo, M. Xiao, and S. Fan, Physical Review Letters 119,
167401 (2017).
[56] Y. Hu, X. Wang, X. Luo, X. Ou, L. Li, Y. Chen, P. Yang,
S. Wang, and H. Duan, Nanophotonics 9, 3755 (2020).
[57] M. V. Gorkunov, A. A. Antonov, and Y. S. Kivshar, Physical
Review Letters 125, 093903 (2020).
[58] I. Toftul, P. Tonkaev, K. Koshelev, F. Lai, Q. Song,
M. Gorkunov, and Y. Kivshar, Physical Review Letters 133,
216901 (2024).
[59] C. W. Hsu, B. Zhen, A. D. Stone, J. D. Joannopoulos, and
M. Soljačić, Nature Reviews Materials 1, 16048 (2016).
[60] K. Koshelev, A. Bogdanov, and Y. Kivshar, Science Bulletin
64, 836 (2019).
[61] S. Joseph, S. Pandey, S. Sarkar, and J. Joseph, Nanophotonics
10, 4175 (2021).
[62] M. Kang, T. Liu, C. T. Chan, and M. Xiao, Nature Reviews
Physics 5, 659 (2023).
[63] K. Koshelev, S. Lepeshov, M. Liu, A. Bogdanov, and
Y. Kivshar, Physical Review Letters 121, 193903 (2018).
[64] D. N. Maksimov, V. S. Gerasimov, S. Romano, and S. P.
Polyutov, Optics Express 28, 38907 (2020).
[65] C. Blanchard, J.-P. Hugonin, and C. Sauvan, Physical Review
B 94, 155303 (2016).
[66] A. A. Bogdanov, K. L. Koshelev, P. V. Kapitanova, M. V. Rybin, S. A. Gladyshev, Z. F. Sadrieva, K. B. Samusev, Y. S.
Kivshar, and M. F. Limonov, Advanced Photonics 1, 016001
(2019).
[67] P. S. Pankin, D. N. Maksimov, K.-P. Chen, and I. V. Timofeev,
Scientific Reports 10, 13691 (2020).
[68] E. N. Bulgakov and D. N. Maksimov, Journal of the Optical
Society of America B 35, 2443 (2018).
[69] J. W. Yoon, S. H. Song, and R. Magnusson, Sci. Rep. 5, 1
(2015).
[70] X. Yin, J. Jin, M. Soljačić, C. Peng, and B. Zhen, Nature 580,
467 (2020).
[71] Q. Jiang, P. Hu, J. Wang, D. Han, and J. Zi, Physical Review
Letters 131, 013801 (2023).
[72] X. Yin, T. Inoue, C. Peng, and S. Noda, Physical Review Letters 130, 056401 (2023).
[73] Z.-P. Zhuang, H.-L. Zeng, X.-D. Chen, X.-T. He, and J.-W.
Dong, Physical Review Letters 132, 113801 (2024).
[74] J. Wang, J. Liu, P. Hu, Q. Jiang, and D. Han, arXiv preprint
arXiv:2404.17281 (2024).
[75] Z. Zhang, X. Yin, Z. Chen, F. Wang, W. Hu, and C. Peng,
Nanophotonics 10, 4467 (2021).
[76] Z. Zhang, F. Wang, H. Wang, Y. Hu, X. Yin, W. Hu, and
C. Peng, Optics Letters 47, 2875 (2022).
[77] H. Li, W. Miao, Q. Du, P. Peng, and F. Liu, Applied Physics
Express 17, 014002 (2023).
[78] W. Xu, Q. Hong, P. Liu, J. Peng, B. Yang, J. Zhang, and

## PDF page 17

17
Z. Zhu, Optics Letters 48, 4761 (2023).
[79] W. Xu, Q. Hong, J. Peng, P. Liu, B. Yang, C. Guo, and Z. Zhu,
Optics Letters 48, 5963 (2023).
[80] H. Wang, Y. Zuo, X. Yin, Z. Chen, Z. Zhang, F. Wang, Y. Hu,
X. Zhang, and C. Peng, Science Advances 10, eadn4372
(2024).
[81] W. Suh, Z. Wang, and S. Fan, IEEE Journal of Quantum Electronics 40, 1511 (2004).
[82] H. Zhou, B. Zhen, C. W. Hsu, O. D. Miller, S. G. Johnson,
J. D. Joannopoulos, and M. Soljačić, Optica 3, 1079 (2016).
[83] F. Alpeggiani, N. Parappurath, E. Verhagen, and L. Kuipers,
Physical Review X 7, 021035 (2017).
[84] X. Ming, X. Liu, L. Sun, and W. J. Padilla, Optics Express 25,
24658 (2017).
[85] D. N. Maksimov, A. A. Bogdanov, and E. N. Bulgakov, Physical Review A 102, 033511 (2020).
[86] R. G. Bikbaev, D. N. Maksimov, P. S. Pankin, K.-P. Chen, and
I. V. Timofeev, Optics Express 29, 4672 (2021).
[87] J. Zhang, J. W. You, F. Feng, W. Na, Z. C. Lou, Q.-J. Zhang,
and T. J. Cui, IEEE Transactions on Microwave Theory and
Techniques 71, 2875 (2023).
[88] H. Wu, L. Yuan, and Y. Y. Lu, Physical Review A 105, 063510
(2022).
[89] Z. Huang, J. Wang, W. Jia, S. Zhang, and C. Zhou, Optics
Letters 50, 105 (2024).
[90] R. C. Rumpf, Electromagnetic and Photonic Simulation for
the Beginner: Finite-Difference Frequency-Domain in MATLAB® (Artech House, 2022).
[91] Z. Ruan and S. Fan, Physical Review A 85, 043828 (2012).
[92] E. N. Bulgakov, D. N. Maksimov, and A. E. Ershov, Physical
Review A 107, 043506 (2023).
[93] Z. Zhao, C. Guo, and S. Fan, Physical Review A 99, 033839
(2019).
[94] E. A. Muljarov and T. Weiss, Optics Letters 43, 1978 (2018).
[95] P. Lalanne, W. Yan, K. Vynck, C. Sauvan, and J.-P. Hugonin,
Laser & Photonics Reviews 12, 1700113 (2018).
[96] C. Sauvan, T. Wu, R. Zarouf, E. A. Muljarov, and P. Lalanne,
Optics Express 30, 6846 (2022).

[97] H. Zhang and O. D. Miller, arXiv preprint arXiv:2010.08650
(2020).
[98] T. Wu and P. Lalanne, Optics Express 32, 20904 (2024).
[99] Ş. K. Özdemir, S. Rotter, F. Nori, and L. Yang, Nature Materials 18, 783 (2019).
[100] I. Rotter, Journal of Physics A: Mathematical and Theoretical
42, 153001 (2009).
[101] M. V. Rybin, P. V. Kapitanova, D. S. Filonov, A. P.
Slobozhanyuk, P. A. Belov, Y. S. Kivshar, and M. F. Limonov,
Physical Review B 88, 205106 (2013).
[102] M. S. Dresselhaus, G. Dresselhaus, and A. Jorio, Group Theory (Springer Berlin, Germany, 2010).
[103] E. N. Bulgakov, D. N. Maksimov, P. N. Semina, and S. A.
Skorobogatov, Journal of the Optical Society of America B
35, 1218 (2018).
[104] H. Friedrich and D. Wintgen, Physical Review A 32, 3231
(1985).
[105] P. Hu, J. Wang, Q. Jiang, J. Wang, L. Shi, D. Han, Z. Q. Zhang,
C. T. Chan, and J. Zi, Optica 9, 1353 (2022).
[106] E. Popov, L. Mashev, and D. Maystre, Optica Acta: International Journal of Optics 33, 607 (1986).
[107] A.-L. Fehrembach, D. Maystre, and A. Sentenac, Journal of
the Optical Society of America A 19, 1136 (2002).
[108] N. A. Gippius, S. G. Tikhodeev, and T. Ishihara, Physical Review B 72, 045138 (2005).
[109] K. X. Wang, Z. Yu, S. Sandhu, and S. Fan, Optics Letters 38,
100 (2013).
[110] D. A. Bykov and L. L. Doskolovich, Physical Review A 92,
013845 (2015).
[111] L. Yuan, M. Zhang, and Y. Y. Lu, Physical Review A 106,
013505 (2022).
[112] W. R. Sweeney, C. W. Hsu, and A. D. Stone, Physical Review
A 102, 063511 (2020).
[113] S. P. Shipman and H. Tu, SIAM Journal on Applied Mathematics 72, 216 (2012).
[114] This can be easily seen by analizing Eq. (8) in [82]. Setting
1/τ1 = 0 corresponds to un UGR decoupled from channel 1.
Upon substitution to Eq. (8), 1/τ1 = 0 leads to complex valued
reflectance that depends on frequency.
