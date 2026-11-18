Source: see manifest row of the PDF
PDF sha256: 9980fd6c6d3879fde274637ad75e6dbb0d3e14afb42a97951541a3c24d6469e1
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of cros_2016_laser_driven_plasma_wakefield_propagation_effects.pdf

Transcription of `cros_2016_laser_driven_plasma_wakefield_propagation_effects.pdf` in this directory, 24 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-24 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published by CERN in the Proceedings of the CAS-CERN Accelerator School: Plasma Wake Acceleration, Geneva,
Switzerland, 23–29 November 2014, edited by B. Holzer, CERN-2016-001 (CERN, Geneva, 2016)

Laser-driven Plasma Wakefield: Propagation Effects
B. Cros
Laboratoire de Physique des Gaz et des Plasmas, CNRS-Université Paris Sud, Orsay, France
Abstract
In the frame of laser-driven wakefield acceleration, the main characteristics of
laser propagation and plasma wave excitation are described, with an emphasis
on the role of propagation distance for electron acceleration. To optimize interaction length and maximize energy gain, operation at low plasma density is
the most promising regime for achieving ultra-relativistic energies. Among
the possible methods of extending propagation length at low plasma density,
laser guiding by grazing incidence reflection at the wall of dielectric capillary
tubes has several assets. The properties of laser guiding and the measurement
of plasma waves over long distances are presented.
Keywords
Laser plasma acceleration; laser guiding; electron acceleration; plasma wave
diagnostic.
1

Introduction

Propagation effects play an important role in laser-driven plasma accelerators [1]. The mechanism of
plasma wave excitation relies on non-linear effects [2], linked to the presence of background electrons
in the medium, driven by short and intense laser pulses [3]. Plasma waves result from the action of the
ponderomotive force, which is proportional to the gradient of laser energy. This force expels electrons
from the regions of higher intensity. Depending on the laser intensity, the density perturbation, or wakefield, remaining behind the laser pulse may be a periodic plasma wave, e.g., a sinusoidal oscillation [4],
or cavities void of electrons, also known as bubbles [5]. Laser and plasma parameters need to be carefully
selected to take advantage of non-linear effects.
The high intensity value, typically in the range 1017 to 1019 W/cm2 , required to drive a wakefield
by laser is usually achieved by focusing the laser beam, within a small volume around the focus position,
over a length shorter than or of the order of 1 mm. The longitudinal fields associated with plasma waves
driven by laser can be as large as 100 GV/m, leading to accelerated electrons with energies of the order
of 100 MeV over a typical scale length of 1 mm [6–8]. Acceleration of electrons to ultra-high energies
requires that a high acceleration gradient be maintained over a longer distance [9].
Increasing the acceleration distance is one of the current challenges of laser plasma accelerators.
Ultra-intense laser beam interaction with matter gives rise to various kinds of non-linear effect [3], which
usually increase with propagation distance. Some intrinsic limitations of laser-driven wakefields, such
as dephasing of electrons during the acceleration process as they overrun the accelerating phase of the
field, or depletion of the laser beam over the propagation distance, can be less severe at low plasma
densities. Lowering the plasma density contributes to a reduction in non-linear effects and an increase
in acceleration distance, provided the laser intensity can be maintained at the required level over the
whole distance. This can be achieved by guiding the laser beam externally, by either a preformed plasma
structure or a capillary tube.
The first part of this paper outlines some of the main characteristics of laser-driven plasma wakefields, useful for describing laser propagation and plasma wave excitation. The main parameters governing electron acceleration are also described, with an emphasis on the role of propagation distance.
Among the different methods of optimizing interaction length to maximize energy gain, operation at low

0007–8328 – c
⃝ CERN, 2016. Published under the Creative Common Attribution CC BY 4.0 Licence.
http://dx.doi.org/10.5170/CERN-2016-001.207

207

## PDF page 2

B. C ROS
plasma density is the most promising regime towards achieving ultra-relativistic energies. Laser guiding
by grazing incidence reflection at the wall of dielectric capillary tubes is described in the second part of
this paper, from guiding properties to the measurement of plasma waves over long distances.
2

Laser plasma acceleration characteristics

2.1 Laser propagation in a vacuum
The electromagnetic field of a laser is described by Maxwell’s equations [10]. The laser pulse can be
modelled by Gaussian functions in space and time as a good approximation of experimental profiles. The
electric field E of a bi-Gaussian laser beam, propagating in vacuum along the z axis, is given by:
]
[
]
[
w0
(z − ct)2
r2
E(r, z, t) =EL
exp −2 ln(2) 2 2
exp − 2
w(z)
w (z)
c τ0
(1)
{
[
] }
2
r
× R exp iω0 t − ik0 z − ik0
+ iψg (z) e⊥ ,
2R(z)
where EL is the amplitude of the electric field, w0 is the waist or smallest laser transverse size in the
focal plane (z = 0), c denotes the speed of light in a vacuum, τ0 is the full width at half maximum of
the pulse duration, and k0 = 2π/λ0 and ω0 = ck0 represent, respectively, the wavenumber and angular
frequency of a laser beam with wavelength λ0 . The unit vector e⊥ indicates the polarization direction
of the laser electric field. For a laser
√ field linearly polarized in the x direction, e⊥ = ex , while for a
circularly polarized one, e⊥ = 1/ 2(ex ± iey ).
The propagation of the Gaussian laser pulse is fully characterized by the beam waist w(z), the
radius of curvature of the wavefront R(z), and the Gouy phase shift ψg (z). As illustrated in Fig. 1, these
parameters evolve along the z axis as
√
( )2
z
w(z) = w0 1 +
,
zR
[
( )2 ]
z
(2)
,
R(z) = z 1 +
zR
( )
z
,
ψg (z) = arctan
zR

where zR = πw02 /λ0 is the Rayleigh length, which represents the position at which the laser beam
transverse area is doubled, compared with the one in the focal plane, owing to diffraction. The beam
divergence far from the focal plane (z ≫ zR ) is given approximately by θL ≃ λ0 /πw0 .

The electromagnetic fields E and B can be expressed in terms of the scalar potential Φ and the
vector potential A,
E = −∇Φ −

∂A
,
∂t

(3)

B=∇×A,
with the Coulomb gauge ∇ · A = 0. In a vacuum Φ = 0, and both fields, E and B, depend only on the
vector potential A. It is useful to define a normalized peak vector potential, also called the laser strength,
a0 = eA0 /(mc) = eEL /(mcω0 ).
The quantities usually measured during experiments are the laser energy, EL , and its distribution
in space, and the pulse duration, τ0 ; they are used to evaluate the laser intensity, which is a key parameter
for laser plasma interaction. The laser intensity is defined as
cε0
IL = c2 ε0 ⟨E × B⟩ =
|E|2 ,
(4)
2
2
208

## PDF page 3

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 1: Electric field of a Gaussian beam in the (y, z) plane; the focal plane is located at z = 0

where ε0 = 8.85 × 10−12 F/m is the permittivity of free space. The laser power for a Gaussian pulse in
time is written as
√
ln(2) EL
EL
P =2
≃
,
(5)
π τ0
τ0
and the corresponding peak laser intensity in the focal plane is
I0 =

2P
2EL
≃
.
2
πw0
πτ0 w02

(6)

Equation (6) shows that the peak intensity can be calculated from the measurements of energy, duration,
and spot size, provided the shape of the laser beam is known. Substituting Eq. (4) into the expression
a0 = eEL /(mcω0 ), a0 can be expressed as a function of the intensity in practical units,
√
√
e2
a0 =
(7)
λ20 I0 ≃ 0.86λ0 [ µm] I0 [1018 W/cm2 ] .
2
2
5
2π ϵ0 me c
An example of energy distribution in the focal plane, measured at the Lund Laser Centre during
an experiment [11], is shown in Fig. 2. As is often the case, before focusing, the energy delivered by
the laser system exhibits a nearly flat-top cylindrically symmetrical distribution in the transverse plane.
Therefore, in the focal plane, the corresponding energy distribution is not purely Gaussian, and it can
be seen from the right of Fig. 2 that it exhibits a profile close to an Airy pattern. The radial profile
is obtained by averaging the energy distribution from the left-hand image over the azimuthal angle.
The focal spot shown in Fig. 2 was achieved after optimization of the symmetry of the distribution,
by tuning a deformable mirror placed after the compressor, to compensate for aberrations in the laser
wavefront. The average radius of the focal spot at first minimum can be determined from the radial
profile; in this example, it was measured as (19.7 ± 0.8) µm, which yields an on-axis peak intensity
of (5.4 ± 0.1) × 1018 W/cm2 and a normalized laser vector potential a0 = 1.6. The energy fraction
contained within the grey shaded area in Fig. 2 is estimated to equal 84% of the energy in the focal plane.
2.2

Electron motion in a laser field

For currently used laser systems, the maximum intensity usually exceeds 1018 W/cm2 , corresponding
to an electric field amplitude larger than 1012 V/m. As the laser field is transverse to the direction of
propagation, single electrons mainly wiggle in this field, and it cannot be used directly to accelerate
electrons in free space.

3
209

## PDF page 4

B. C ROS

Fig. 2: Left: energy distribution in the focal plane. Right: corresponding averaged radial profile of laser energy
in logarithmic scale; the grey shaded area, with a boundary at the first minimum of the focal spot, contains about
84% of laser energy in the focal plane.

The motion of a single electron with charge −e and mass me in the laser fields E and B is
described by the Lorentz equation,
dp
= −e(E + v × B) ,
(8)
dt
where p = γme v is the electron momentum, γ = (1 − β 2 )−1/2 is the relativistic factor, and β = v/c
denotes the normalized velocity. Approximating the laser field as a plane electromagnetic wave polarized along the x axis and propagating along the z axis, E(z) = EL cos(k0 z − ω0 t)ex , or in terms of
vector potential using Eq. (3): A(z) = A0 sin(k0 z − ω0 t)ex , with A0 = EL /ω0 . Taking into account
|B| = |E| /c, the second term in the right-hand side of Eq. (8) can be neglected in the non-relativistic
regime, when β ≪ 1. Then Eq. (8) becomes simply
dp
∂A
= −eE = e
.
dt
∂t

(9)

Therefore, an electron, initially at rest at z = 0, oscillates in the direction of the electric field with a
velocity
eA0
β=−
sin(ω0 t) ≜ −a0 sin(ω0 t) .
(10)
mc
It follows from Eq. (10) that an electron initially at rest will oscillate in the laser field with no net energy
gain.
For a0 ≳ 1, the electron oscillation velocity will approach c, and the v × B component in the
Lorentz equation must be taken into account. The solution of Eq. (8) in the relativistic regime can be
found, for example, in Ref. [12]. In the frame co-moving with the laser pulse, a(z) = a0 sin(k0 ξ)ex ,
where ξ = z − ct is the coordinate in the frame co-moving with the laser. The normalized momentum of
the electron can be written as
dx
= a = a0 sin(k0 ξ) ,
dξ
dz
a2
a2
uz = γβz =
=
= 0 sin2 (k0 ξ) .
dξ
2
2

ux = γβx =

4
210

(11)

## PDF page 5

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 3: Trajectory of an electron in the laser transverse field in the laboratory frame for two values of the laser
strength.

The electron velocity is always positive in the z direction, so that the v × B force pushes the electron
forward. Integrating Eq. (11) gives the electron coordinates along the trajectory:
x=−
z=

a0
cos(k0 ξ) ,
k0

a20
[2k0 ξ − sin(2k0 ξ)] .
8k0

(12)

The set of Eq. (12) indicates that the electron not only moves forward but also oscillates at twice
the laser frequency in the longitudinal z direction. Figure 3 shows the electron trajectories for two values
of a0 . The longitudinal momentum scales with the square of the laser strength as a20 , while the transverse
one linearly depends on the laser strength by a0 . Hence, for a0 ≫ 1, the longitudinal motion of the
electron dominates the transverse oscillation. The excursion distances along the x and z axis calculated
over one period become equal for a0 = 8/π ≃ 2.55. For a laser wavelength of 800 nm, a0 = 2.55
corresponds to I0 = 1.4 × 1019 W/cm2 .
This simple analysis shows the importance of operation in the relativistic regime, to achieve electron motion along the laser propagation direction. Nevertheless, as shown in Fig. 3, the electron is merely
pushed forward during each light cycle but does not gain energy from the laser. The overall net effect is
only to transfer the electron to a new longitudinal position. However, in this section, the laser beam was
assumed to be a uniform and infinite plane wave. This is generally not the case in experiments, where
laser pulses need to be tightly focused to achieve high intensity. The laser intensity is not uniform but
Gaussian-like in the transverse plane. As shown next, the ponderomotive force associated with the laser
intensity gradient excites a plasma wave, as the plasma plays the role of a transformer, to transfer laser
energy to electrons.
2.3

Electromagnetic waves in plasmas

In a plasma, electrons oscillate around an equilibrium position with a characteristic frequency defined as
the plasma frequency [2]
√
ωp =

ne e2
.
me ε0

5
211

(13)

## PDF page 6

B. C ROS
√
In the non-linear regime, the plasma frequency is modified by relativistic effects to ωpNL = ωp / γ. The
dispersion relation of an electromagnetic wave in a plasma can be written as
ω02 = ωp2 + c2 k 2 .

(14)

For ω0 > ωp , k is real and the wave can propagate in the plasma; k becomes imaginary for ω0 < ωp ,
and the wave is evanescent. The light is thus either transmitted, damped, or reflected in the plasma,
depending on the plasma density. The critical density, nc , is defined as the density for which ω0 = ωp ,
and can be written in practical units as
nc [1021 cm−3 ] =

ω02 me ε0
1.12
.
= 2
e2
λ0 [ µm]

(15)

The critical density corresponding to a laser wavelength of 0.8 µm is 1.75 × 1021 cm−3 . For ne < nc ,
the plasma is called underdense, and it is called overdense for ne > nc . The laser-driven wakefield relies
on the excitation of a plasma wave in the underdense regime.
The phase and group velocities of the electromagnetic field in the plasma are calculated from
Eq. (14):
√
ωp2
ω0
vph =
= c2 + 2 ,
k
k
(16)
2
dω0
c
c2
vg =
=
=√
.
dk
vph
c2 + ω 2 /k 2
p

If the evolution of the driving laser pulse in the plasma is not significant during propagation, the
phase velocity of the plasma wave is equal to the group velocity of the driving laser [13]. The normalized
phase velocity and relativistic factor of the plasma wave are then given by
√
vg
ne
βp =
= 1−
,
c
nc
√
(17)
1
nc
=
γp = √
.
ne
1 − βp2

It can be seen that a lower density leads to a higher phase velocity and a larger relativistic factor.
2.4 Plasma wave excitation

In a plasma, the action of the ponderomotive force leads to the excitation of a plasma wave. This force
is associated with the second-order electron motion [see Eq. (8)], averaged over a time-scale longer than
the laser period. The three-dimensional (3D) ponderomotive force [14] for an electron can be written as
⟨
⟩
Fp = −me c2 ∇ a2 /2 = −me c2 ∇a20 /2 .
(18)
The ponderomotive force can be viewed as the radiation pressure of laser intensity. This force expels
charged particles out of the region of high laser intensity, and does not depend on the sign of the charged
particle. Furthermore, it is inversely proportional to particle mass Fp ∝ 1/m. Hence, under the same
laser field, the acceleration exerted on a proton is only 10−6 times that exerted on an electron, so that ion
motion can be neglected for sufficiently low laser strength.
Figure 4 illustrates the excitation of a plasma wave (red solid curve) in the linear (top graph) and
non-linear (bottom graph) regimes, where the on-axis density exhibits localized spikes separated by a
6
212

## PDF page 7

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 4: Laser envelope (blue dashed line) and density perturbation (red solid line) along the axis of propagation in
(top) the linear and (bottom) non-linear regimes.

distance longer than the linear wavelength; the laser pulse envelope is indicated by a blue dashed line.
The longitudinal electric field associated with a plasma wave is thus a space charge field linked to the
periodic distribution of charges oscillating behind the laser pulse. The oscillation length is the plasma
wavelength linked to the electron density of the plasma, ne , by the relation
λp [µm] ≃ 33 × (ne [1018 cm−3 ])−1/2 .

(19)

This plasma wave is called a relativistic plasma wave because its phase velocity, given by Eq. (17), is of
the order of the laser group velocity in the medium when the plasma frequency ωp is much smaller than
the laser frequency ω0 . The amplitude of the longitudinal accelerating field can be written as:
Ep [ GV/m] ≃ 96(ne [1018 cm−3 ])1/2

δne
.
ne

(20)

The amplitude of this field is maximum for a density perturbation of 100%, at the upper limit of the
linear regime, where the plasma wave breaks.
2.5

Regimes of the laser wakefield

Among the parameters determining the characteristics of accelerated electrons in a plasma are the laser
characteristics (amplitude, transverse, and longitudinal sizes) and plasma properties, such as the electron
density and distribution. The laser strength a0 is mainly used to distinguish between linear (or quasilinear) and non-linear regimes of laser wakefield excitation. Nevertheless, as the non-linear evolution of
the laser includes a deformation of the spatial volume delimiting the most intense fraction of the laser
pulse, the initial transverse size of the laser, rL , is also a key parameter. In the quasi-linear regime,
a0 ≃ 1 and
kp2 rL2
a2
> 0 ,
(21)
2
γ⊥
with γ⊥ = (1 + a20 /2)1/2 . The bubble or blow-out regime occurs for a0 > 1 and is characterized by
√
kp rL ≤ 2 a0 .
(22)

Figure 5 illustrate the main features of these two different regimes with simulation results. The left panel
of Fig. 5 shows that the laser wakefield in the linear regime exhibits a regular oscillating behaviour [4].
7
213

## PDF page 8

B. C ROS

Fig. 5: Illustration of the two regimes of the laser wakefield. Left: Excitation of a plasma wave in the linear
regime; 3D view and projection in the horizontal plane of the normalized laser intensity, a0 , and wake potential,
ϕ. Right: Excitation of a plasma wave in the non-linear regime; map of density in the horizontal plane (grey scale,
white is zero) and superposition of laser amplitude (colour scale, red is a maximum).

The ponderomotive force varies as the laser energy gradient and creates a density distribution in the
longitudinal and transverse directions. The associated transverse and longitudinal fields can be controlled independently by adjusting the focal spot transverse size and the pulse duration. The accelerating
structure is shaped as a sine wave with wavelength λp , typically in the range 10–100 µm; its value is adjusted by tuning the plasma electron density. The accelerating field is typically in the range 1–10 GV/m,
this value is limited to the wavebreaking field for a non-relativistic cold plasma, E0 = me cωp /e, and is
of the order of 96 GV/m for a plasma electron density ne = 1018 cm−3 . Wavebreaking is characterized
by the fact that electron oscillations become so large that the electrons can escape the collective motion.
This may be at the origin of electron injection in the non-linear regime. In the linear regime, wavebreaking does not take place, and relativistic electrons need to be produced by an external source and
injected into the linear plasma wave to be accelerated.
The right panel of Fig. 5 illustrates the main features of the non-linear regime. As the laser propagates into the plasma, its front edge diffracts while the rest of the pulse self-focuses. Electrons are
expelled by the ponderomotive force from the high-intensity volume and a plasma cavity, the white area
in Fig. 5, which is void of electrons, is left behind the laser pulse. The expelled electrons travel along
the field lines and accumulate at the back of the cavity, where they can be injected and accelerated. The
cavity size is typically of the order of 10 µm, and produces accelerated electron bunches with a transverse
size of the order of a few micrometres, owing to the focusing field inside the cavity. This regime is also
called the blow-out or bubble regime [5, 15].
2.6

Laser modulation in plasma

The optical properties of the plasma are modified during the excitation of a plasma wave, and can, in
turn, modify the driving pulse. For the range of intensities of interest for a laser-driven wakefield, there
are two important effects, self-focusing and self-compression, corresponding to changes in the transverse
size and duration of the laser pulse during its propagation.
2.6.1

Self-focusing

The propagation of a laser pulse in a plasma can be investigated in terms of the spatial refractive index,
η(r) = c/vph . Recalling the definition of vph in Eq. (16), the refractive index for an underdense plasma,
8
214

## PDF page 9

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS
2 /γ)n (r)/n , is
with uniform density ne0 , and a large amplitude plasma wave, ωp2 (r) = (ωp0
e
e0

c
η(r) =
=
vph

(

ωp2 (r)
1−
ω02

)1/2

≃1−

1 ne (r)
.
2 γ(r)nc

(23)

Equation (23) shows that the spatial profile of the refractive index η(r) can be modified by the relativistic
factor γ(r) or the density distribution ne (r). In the weakly relativistic case, Eq. (23) can be expanded
as [3, 16]
(
)
ωp2
a2 ∆ne δne
η(r) = 1 − 2 1 −
+
,
(24)
+
2
n0
n0
2ω0

where ∆ne /n0 takes into account the contribution of a preformed plasma channel along the radius; the
δne /n0 term is responsible for plasma wave guiding, self-channelling, and the self-modulation of long
pulses; the a2 /2 term corresponds to the contribution of relativistic laser guiding.
For a Gaussian pulse, with intensity peaked on-axis, ∂a2 (r)/∂r < 0, which satisfies the condition
for refractive guiding, ∂η(r)/∂r < 0 or ∂vph (r)/∂r > 0. This implies that the on-axis phase velocity
is less than the off-axis velocity, making the laser wavefront curved. The plasma thus plays the role
of a convex lens, focusing the laser beam towards the propagation axis. This mechanism is known as
self-focusing, and is able to balance laser diffraction. As shown in Eq. (24), the modulation of the
refractive index leading to beam focusing scales with a2 . Therefore, for a given beam divergence, there
is a minimum threshold for laser intensity to balance diffraction. Self-focusing will occur when the laser
power P exceeds a critical power Pc , which can be written as [17–19]
Pc =

8πε0 m2e c5 ω02
ω02
≃
17
[ GW] .
e2 ωp2
ωp2

(25)

For example, the critical power for a λ = 0.8 µm laser at plasma density n0 = 7 × 1018 cm−3 is
Pc = 4.25 TW.
The radial ponderomotive force expels electrons from the axis, thus creating a radial density gradient ∂(δne (r))/∂r > 0, and a negative transverse gradient of the refractive index ∂η(r)/∂r < 0, acting to focus the laser beam, although for P ≪ Pc , the ponderomotive force is not sufficient to guide
the laser [13]. When the laser power approaches the critical power, relativistic self-guiding dominates
laser propagation, while ponderomotive channelling enhances self-guiding. The contribution of ponderomotive channelling slightly relaxes the critical power for self-guiding to Pc = 16.8(ω02 /ωp2 ) [ GW].
2.6.2 Self-compression
In addition to the beam size evolution in the transverse direction, the variation of plasma density along the
propagation axis modulates the laser pulse longitudinally. The density variation along the propagation
axis δne (ξ) during the laser pulse makes it experience different local refraction indices, and consequently
compress or stretch in the temporal domain.
Using Eq. (24), the local group velocity of the drive laser, or the phase velocity of the plasma
wave, can be examined, taking into account the longitudinal dependence of η:
ωp2
vg /c ≃ η ≃ 1 − 2
2ω0

(
)
a2 δne
1−
+
.
2
n0

(26)

δne = 0 gives the laser group velocity in the background plasma: vg0 . For positive density variation
δne > 0, the laser group velocity decreases vg − vg0 < 0, whereas δne < 0 corresponds to an increase
in laser group velocity: vg − vg0 > 0. As a result of plasma wave excitation (see Fig. 4), the rear of
the laser pulse moves faster than its front edge. The laser pulse is temporally compressed; this is also
9
215

## PDF page 10

B. C ROS
called pulse shortening. This effect plays an important role in laser-driven wakefields as it contributes to
matching the laser pulse duration and plasma wave period.
As a consequence of temporal compression, the spectral bandwidth of the short laser pulse will
increase. Most of the laser pulse can be redshifted, while strong blueshifts occur at the back of the pulse
for pulses longer than the plasma period [20]. As the spectral modulation of the driving laser is created
by the plasma modulation, this provides a good means of diagnosing the excited plasma wave [21].
2.7 Energy gain of an electron in a plasma wave
The energy gain, ∆W , of an electron accelerated in a plasma wave is proportional to the product of the
accelerating longitudinal field associated with the plasma wave, Ep , and the length, Lacc , over which the
electron is submitted to this field,
∆W = eEp Lacc .
(27)
The amplitude of the accelerating field and the length of acceleration depend on the regime of the laser
wakefield and can be optimized in different ways. Three main mechanisms may limit the acceleration
distance: laser diffraction typically limits acceleration to the Rayleigh length; pump depletion defines
the length over which half of the laser energy is transferred to the plasma wave; and dephasing, in
which accelerated electrons outrun the plasma wave and enter a decelerating phase, defines the dephasing
length. Diffraction is a limitation due to laser propagation in the medium and can be overcome in the
non-linear regime by self-focusing: in that case, the non-linearities imposed on the medium can shape
the transverse density profile to act as a transient focusing length. In the linear regime, where these
non-linear effects are negligible, external guiding has to be implemented; the use of capillary tubes for
this purpose will be described in Section 3. Electron dephasing and laser depletion are intrinsic to laser
plasma acceleration and depend on the electron density. Their dependences are described next.
2.7.1 Dephasing
As the phase of the plasma wave evolves at the group velocity of the laser in the plasma, a relativistic
electron accelerated in this wave can explore different phases of the accelerating field. The dephasing
length [13, 22], Ld , is defined as the length over which an electron can be accelerated before reaching a
decelerating period of the electric field.
In the one-dimensional (1D) linear regime, Ld is evaluated as follows: in the co-moving frame,
the maximum length over which the field is accelerating during one period is λp /2. Assuming that the
accelerated electron propagates at approximately c, and keeping in mind that the plasma wave phase
moves forward with velocity vg , L1D
d is estimated as
L1D
d =

λp
λp
nc
ω2
c=
≃ λp = 02 λp .
2(c − vg )
2(1 − βp )
ne
ωp

(28)

This expression can be generalized to two-dimensional (2D), by noting that for a 2D plasma wave, there
is only a quarter of the period (λp /4) in which the longitudinal electric field is accelerating and the radial
field is focusing. Therefore, the dephasing length becomes
1D
L2D
d = Ld /2 =

ω02
λp .
2ωp2

(29)

In the 3D bubble regime, the distance in the co-moving frame for dephasing becomes the bubble radius
Rb . The phase velocity of the plasma wave is modified to βp = 1 − 3ωp2 /(2ω02 ). Accordingly, the
dephasing length L3D
d is given by
√
Rb
2 ω02
4 ω02 a0
3D
Ld =
≃
Rb =
.
(30)
1 − βp
3 ωp2
3 ωp2 kp
10
216

## PDF page 11

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 6: 3D dephasing length and pump depletion length as functions of plasma electron density. The laser pulse
has a duration of 30 fs and a peak intensity corresponding to a0 = 4.

This expression shows that the 3D non-linear dephasing length depends on both the plasma electron
density and the laser intensity. A longer L3D
d can be achieved either decreasing the plasma density, as
illustrated in Fig. 6, or by increasing the laser intensity.
2.7.2

Pump depletion

Another underlying limit is the so-called pump depletion, associated with the length Lpd , over which
the driving laser becomes depleted. As the laser pulse travels in the plasma, it transfers its energy to the
plasma wave. The pump depletion length is defined as the distance
over which the energy contained in
∫
the plasma wave equals that of the driving laser, Ep2 Lpd = EL2 dξ. For a Gaussian driving laser pulse,
the linear pump depletion length is given by [23]
LLpd =

ω02 cτ0
.
ωp2 a20

(31)

In the non-linear regime, the pump depletion length is estimated via the etching velocity vetch ≃ cωp2 /ω02
[24]; this describes the erosion velocity of the laser front that excites the plasma wave, before the start of
self-focusing. The laser will be depleted over the depletion length given by
LNL
pd =

c
vetch

cτ0 =

ω02
cτ0 .
ωp2

(32)

Lu et al. [15] showed that this expression of non-linear pump depletion length LNL
pd is valid for 2D and
3D non-linear cases.
NL
Both the 3D dephasing length L3D
d and the pump depletion length Lpd are plotted as functions of
plasma density, for a0 = 4, in Fig. 6. Typically, the two lengths are of the order of a few millimetres in the
density range above ne = 3×1018 cm−3 , where dephasing dominates pump depletion. The most efficient
NL
18 cm−3 ,
use of laser energy is achieved around the density where L3D
d ≃ Lpd . Below ne = 2.5 × 10
pump depletion occurs over a shorter length than dephasing, and both lengths increase quickly when the
density becomes of the order of 1 × 1018 cm−3 .

2.7.3

Scaling laws

Scaling laws in the different regimes have been established from phenomenological considerations by Lu
et al. [15], and are summarized in Table 1. These scaling laws play an important role in understanding
11
217

## PDF page 12

B. C ROS
Table 1: Summary of scaling laws for linear and non-linear regimes [15], for the dephasing length Ld , the depletion
length, Lpd , the relativistic factor of the plasma wave γp , and ∆E, the energy gain of an electron accelerated over
the dephasing length.

Linear
1D non-linear
3D non-linear

a0

w0

Ld

Lpd

γp

∆E/me c2

<1

λp

ω02
λ
ωp2 p

ω02 cτ0
ωp2 a20

ω0
ωp

a20 ω02

λp

4a

2
2 ω0
0 ωp2

λp

2
1 ω0
3 ωp2

a0
π λp

2 √
4 ω0 a0
3 ωp2 kp

ω02
ωp2

>1
>2

√

ω2
p

cτ0

√

a0 ωωp0

4a20 ω02

cτ0

√1 ω0
3 ωp

ω02
2
3 a0 ωp2

ω2
p

laser plasma acceleration mechanisms, and have been verified in numerous experiments. Scaling laws
can be used, for example, to predict the energy gain in the non-linear regime. Using an average value
of the accelerating field in the bubble regime, and an average value for acceleration over the dephasing
length, the energy gain can be approximately written as
( 2 )1/3 ( )2/3
2 ω02
e P
nc
2
2
∆E ≃ a0 2 me c ≃ me c
,
(33)
2
5
3 ωp
me c
ne
which becomes, in practical units,
) (
)4/3 (
)2/3
(
0.8
1
P [TW] 1/3
.
∆E [ GeV] ≃ 1.7
100
λ0 [µm]
ne [1018 cm−3 ]

(34)

This expression shows that the plasma electron density is a key parameter for tuning the electron bunch
energy: a large energy gain over the dephasing length in the 3D non-linear regime can be achieved for low
electron density and large laser power. Figure 7 shows the electron energy gain as a function of plasma
density and laser power, calculated from Eq. (34). For a laser power of 100 TW, Eq. (34) predicts that
electrons can be accelerated up to 1.7 GeV at a plasma density of ne = 1 × 1018 cm−3 . The energy gain
displays a stronger dependence on plasma density than on laser power. Hence, to achieve higher electron
energy, a lower electron plasma density is desirable. Nevertheless, one must always remember the laser
√
√
size matching condition, which requires w0 = λp a0 /π, which is proportional to 1/ ne . When ne is
decreased, the laser power must be increased accordingly to meet the requirement for producing a larger
bubble, as P = I0 πw02 /2, which is proportional to 1/ne .
Numerous experimental results in the non-linear regime, where electrons from the plasma are selfinjected into the accelerating structure, follow the scaling law for energy gain ∝ 1/ne , as illustrated in
Fig. 8. Figure 8 shows that when the density is divided by a factor of 10, from ne = 8 × 1018 cm−3
to ne = 0.8 × 1018 cm−3 , the maximum energy of the electron bunch is multiplied by the same factor.
It should be noted that parameters other than the plasma density can change significantly between the
different cases plotted in this graph: in particular, the laser power has been increased over the years and
has contributed to the experimental observation of electrons in the gigaelectronvolt range for petawattclass laser systems. The length of the plasma was also increased: starting from millimetre-scale gas
jets at higher densities, gas cells of length between one and a few centimetres are used in intermediate
regimes; the largest energy gain to date was obtained using external guiding by a plasma channel [9].
In conclusion, experimental results are well understood regarding the maximum electron energy
dependence with electron plasma density and clearly indicate the way to increase the energy further.
Reducing the density significantly increases the dephasing length: the next challenge will be to achieve
metre-scale plasma lengths while preserving the laser intensity over the whole distance. Next, we examine some aspects of low-density operation of laser wakefield excitation over large distances.
12
218

## PDF page 13

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 7: Energy gain over the dephasing length as a function of plasma density and laser power, calculated using
Eq. (34).

Fig. 8: Energy gain measured in various experiments around the world, plotted with black squares and labels,
follow the dependence ∆W ∝ 1/n. Labels indicate institute acronyms and year of publication.

3
3.1

External guiding with capillary tubes
Choosing a guiding mechanism

Several methods have been developed to guide the focused laser over a distance longer than the Rayleigh
length. Among them, self-focusing is one of the most commonly employed, owing to the simplicity of
its implementation. Relying on this scheme, a powerful laser, PL > Pc , can be guided over the pump
depletion length, typically several millimetres long (see Fig. 6). To achieve self-focusing, the laser power
must be in excess of the critical power, given by Pc GW = 17ω02 /ωp2 , which increases rapidly when the
plasma density is decreased: for a plasma density ne = 1 × 1018 cm−3 , Pc equals 30 TW.
13
219

## PDF page 14

B. C ROS

Fig. 9: Guiding methods: left, plasma channel, characterized by varying plasma density along the radius; right,
capillary tube with glass wall, and laser reflection from the inner walls.

Self-focusing is the result of a modification of the plasma density by the front of the laser pulse,
acting to create a density structure able to compensate diffraction for the rear of the pulse. A density structure acting to compensate diffraction (see Eq. (24)) can be formed prior to the intense laser
interaction. A plasma channel can be created with the help of an external electrical discharge [25, 26]
or by a heating laser pulse [27, 28]: the hot on-axis plasma electrons move outward, owing to radial
hydrodynamic expansion, resulting in a density depletion on-axis and a nearly parabolic transverse density profile, as illustrated in the left panel of Fig. 9. A parabolic plasma channel can guide a Gaussian
beam with a constant spot size w0 = wm , where wm depends on the curvature of the channel. Under
the matching condition, lasers with intensity of the order of 1018 W/cm2 were successfully guided by
plasma waveguides over many Rayleigh lengths [27,29]. Good-quality guiding in plasma channels relies
on fine tuning of the incident laser parameters (spot size, duration, energy) with channel parameters. As
the guiding mechanism relies on plasma density and its spatial profile, this mechanism cannot be used
for applications requiring plasma parameters that are very different from those required for laser guiding
in the plasma channel.
When a capillary tube is used, as illustrated in the right panel of Fig. 9, the laser beam is guided
by reflections at the inner capillary wall [30], and laser guiding can thus be achieved in vacuum or at low
plasma density. This guiding scheme does not rely on laser power, or plasma density, and provides the
opportunity to explore a large domain of laser plasma parameters. Laser guiding can, in principle, be
achieved inside capillary tubes with total or partial reflection at the inner wall, depending on the material
of the tube wall, which may be either a conductor or a dielectric material. Metallic tubes could be used
to guide the laser beam without loss at the inner wall. In practice, their surface is usually not optically
smooth for the laser wavelength and tube diameters used for laser guiding at high intensities. Dielectric
capillaries, such as glass capillaries, are optically smooth and can be manufactured with a good reliability
for a large range of inner diameters, wall thicknesses and lengths.
3.2

Eigenmodes of capillary tubes

Solving Maxwell’s equations, with boundary conditions for dielectric surfaces at the capillary tube inner
wall, gives hybrid mode solutions, with quasi-transverse electromagnetic modes. Solving the wave equation in cylindrical geometry, with boundary conditions describing the continuity of the field components
at the boundary between the vacuum inside the tube and the dielectric wall, different families of eigenmodes of capillary tubes are obtained [30]. An incident linearly polarized Gaussian laser beam can
be efficiently coupled to the linearly polarized family of hybrid modes, namely the EH1m modes. The
transverse electric components of the EH1m modes at zero order can be found in Ref. [30]. For the EH1m
modes, the transverse electric field amplitude inside the capillary tube can be written as
l
E1m (r, z, t) = J0 (k⊥m r) exp(−km
z) cos(ω0 t − kzm z) ,

14
220

(35)

## PDF page 15

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 10: Field distribution in the transverse plane for the three first hybrid modes EH1m , plotted for Rcap = 50 µm;
bottom graphs show the corresponding distributions through y = 0.

2 )1/2 , and
where k⊥m is the transverse wavenumber of the mode with order m, defined as k⊥m = (k02 −kzm
is given by k⊥m = um /Rcap , Rcap is the capillary tube inner radius, um is the mth root of J0 (x) = 0,
and J0 is the Bessel function of integer order. Table 2 gives the first nine values of um . kzm is the
longitudinal wavenumber inside the tube, and k0 is the wavenumber of the laser beam in free space.
Figure 10 illustrates the electric field amplitude in the transverse plane for the three first modes. The
electric field of the EH1m modes is maximum at the tube axis; for m = 1, the field variation is close to
the field of a Gaussian beam.

The exponential decay term in Eq. (35) indicates that the electric field is damped along the direction of propagation, z: each reflection at the dielectric capillary wall is associated with a refracted
fraction of the laser beam inside the dielectric wall. This refracted fraction is minimum for the smallest
perpendicular wavenumber, corresponding to the grazing incidence. The characteristic damping col is given by [30]:
efficient km
u2
1 + εr
l
km
= 2 m3 √
,
(36)
2kz0 Rcap εr − 1
l strongly depends on the capillary
where εr is the dielectric constant of the wall. This shows that km
radius, Rcap , the wavelength of the incident laser beam, and the mode order, through um . Laser damping
is usually described by the attenuation length Llm , defined as

Llm =

2 R3 √
2kz0
1
εr − 1
cap
=
.
2
l
um
1 + εr
km

(37)

After a propagation distance of Llm , the field magnitude decreases by a factor 1/e and the beam energy by
a factor 1/e2 , owing to refraction losses. For example, the values of damping length Llm for a Ti:sapphire
laser (λ0 = 800 nm) guided inside a 50 µm radius capillary tube are given in Table 2 for the nine first
modes. Llm drops rapidly with increasing mode order, which means that higher-order modes are damped
over shorter distances. Therefore, the use of the fundamental mode is preferable, to achieve laser guiding
over a long propagation distance.
The group velocity is determined from the dispersion relation of an electromagnetic wave in a
2 ), for k 2
2
capillary tube, k02 = (kz2 + k⊥m
⊥m ≪ k0 , as
(
2 )1/2
k⊥m
.
vgm ≃ c 1 − 2
k0
15
221

(38)

## PDF page 16

B. C ROS

Table 2: Values of um , Llm , and vgm for the first nine modes of a capillary: radius, 50 µm; laser wavelength,
λ0 = 800 nm.

m
1
2
3
4
5
6
7
8
9

um
2.404826
5.520078
8.653728
11.79153
14.93092
18.07106
21.21164
24.35247
27.49348

Llm (cm)
91.7
17.4
7.1
3.8
2.4
1.6
1.2
0.9
0.7

vgm /c
0.99998
0.9999
0.9998
0.9995
0.9993
0.9989
0.9985
0.9981
0.9975

max (10−5 )
Fm
2.034
4.604
7.2011
9.8049
12.4113
15.0189
17.6272
20.2359
22.8449

The fourth column in Table 2 shows the values of vgm . It can be seen that the group velocity is close
to the velocity of light in free space, and decreases as the mode order increases. This again supports
the use a lower-order mode with higher group velocity, corresponding to a higher phase velocity for the
wakefield.
Another important issue associated with the use of a capillary tube is the threshold of material
damage at the inner wall where reflection occurs, which determines the ability of capillary tubes to guide
intense lasers. To examine this, we define the normalized flux at the capillary inner wall, Fm , as the ratio
of the radial component of the Poynting vector at r = Rcap to the longitudinal component of the on-axis
Poynting vector; it is given by [30]
Fm =

2
k⊥m
cos2 θ + εr sin2 θ
2
√
J
(k
R
)
.
cap
⊥m
1
k02
εr − 1

(39)

Fm depends on the azimuthal angle θ and mode order m. Fm is minimum for θ = 0, π and maximum
2 . Its
for θ = π/2, 3π/2. It also depends on the mode eigenvalue and capillary radius through k⊥m
maximum value should be below the threshold of material breakdown, to ensure laser guiding without
max increases by one order of magnitude
non-linear interaction at the wall. As shown in Table 2, Fm
from the fundamental mode to the ninth mode. Once again, it emphasizes the advantage of using the
fundamental mode. For a glass capillary, the ionization threshold is of the order of 1014 W/cm2 for an
800 nm laser pulse with duration shorter than or of the order of 100 fs [31]. The maximum intensity
on-axis guided by a capillary of 50 µm radius on the fundamental EH11 mode without wall ionization is
thus of the order of 1019 W/cm2 .
3.3

Mode coupling

When a laser beam is focused at the entrance of a capillary tube, its energy has to be coupled to the
capillary eigenmodes before propagation. In this section, we describe the conditions of coupling for
two kinds of laser energy distribution in the focal plane, located at the entrance of the capillary tube: a
Gaussian beam and an Airy beam, both of which can be good approximations to describe the beams used
in experiments. As shown in the previous section, monomode guiding with the fundamental EH11 mode
has interesting properties for laser wakefield excitation, so the condition for monomode coupling will be
particularly discussed.
3.3.1 Coupling of a Gaussian beam
Laser beams can be described as transverse electromagnetic modes with a transverse Gaussian envelope.
Assuming a linearly polarized Gaussian beam focused at the capillary entrance (z = 0), the amplitude of
16
222

## PDF page 17

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 11: Coupling coefficient of modes 1 to 4 for a Gaussian beam with waist w0 incident at the entrance of a
capillary with radius Rcap as a function of the ratio Rcap /w0 .

its electric field is written as EG (r) = EL exp(−r2 /w02 ), while the electric field inside a capillary tube
is a superposition of the EH1m eigenmodes given by Eq. (35). At the entrance (z = 0), the continuity of
fields reads
(
)
∞
∞
∑
∑
um r
EL exp(−r2 /w02 ) =
Am E1m =
Am J0
.
(40)
Rcap
m=1

m=1

The coefficient Am indicates the amplitude of the EH1m mode, which can be determined using the
orthogonality of Bessel functions,
∫1
2 /w 2 )J (u x)dx
x exp(−x2 Rcap
0 0 m
Am = 2EL 0
.
(41)
J12 (um )
The coupling coefficient, Cm , is defined as the fraction of incident energy coupled to the EH1m mode,
and can be written as
[
]
(
)2 ∫ 1 x exp(−x2 R2 /w2 )J (u x)dx 2
0
m
cap
0
0
Rcap
.
(42)
Cm = 8
2
w0
J1 (um )

Cm thus depends on the mode order m, the capillary radius Rcap , and the laser waist w0 . Figure 11 shows
the dependence of the coupling coefficient of an incident Gaussian beam on the first four eigenmodes, as
a function of the ratio of capillary radius to laser waist, Rcap /w0 . It shows that monomode coupling can
be achieved when Rcap /w0 ≃ 1.55 (or w0 /Rcap ≃ 0.65). In this case, almost 98% of the incident laser
energy is coupled to the fundamental EH11 mode, and only 1% of laser energy is coupled to higher-order
modes. The remaining 1% of laser energy is the energy contained in the wings of the Gaussian function
outside the capillary diameter, and it is lost into the material at the front surface of capillary tube.
For 1.2 ≤ Rcap /w0 ≤ 2, more than 90% of the incident laser energy can be coupled to the
first mode. When Rcap /w0 → 0, the laser size increases, and the fundamental mode is predominantly
excited, although coupling efficiency decreases quickly. This is because the laser energy is outside the
capillary diameter and hits the front surface of the capillary tube, as illustrated by the left-hand sketch
in Fig. 11. As Rcap /w0 increases, the laser waist becomes small compared with the optimal waist for
quasi-monomode coupling. In this case, the laser energy is nearly 100% coupled into the capillary tube,
17
223

## PDF page 18

B. C ROS

Fig. 12: Coupling coefficient of an Airy beam to the first five eigenmodes as a function Rcap /r0 . The grey area
indicates the range of Rcap /r0 where more than 80% of the incident laser energy is coupled to the EH11 mode.

as indicated by the sum. However, the energy coupled to the fundamental mode decreases at the benefit
of the excitation of higher-order modes, resulting in undesired mode beating and severe laser attenuation
during the propagation in the capillary tube.
3.3.2

Coupling of an Airy beam

Another case of interest is the coupling of a laser beam with an Airy-like distribution in the focal plane
[32]. The electric field amplitude for an Airy beam focused at the capillary entrance (z = 0) is written as
EA = EL

J1 (ν1 r/r0 )
,
r

(43)

where ν1 = 3.8317 is the first root of the equation J1 (x) = 0, and r0 is the radius corresponding to the
first zero. The continuity of the electric field at the capillary entrance gives
(
)
∞
∞
∑
∑
J1 (ν1 r/r0 )
um r
EL
=
Am E1m =
Am J0
,
(44)
r
Rcap
m=1

m=1

and the coupling coefficient, Cm , can be calculated from
[∫ 1 (
)
]2
ν1 Rcap
4
J1
x J0 (um x)dx .
Cm = 2
r0
J1 (um ) 0

(45)

The coupling coefficients for the first five eigenmodes are plotted as functions of Rcap /r0 in
Fig. 12. This shows that quasi-monomode guiding of an Airy beam can be achieved for Rcap /r0 ≃ 1.
However, even in this case, only 83% of the incident laser energy is coupled to the fundamental mode,
while the remaining 17% energy contained by the laser distribution for r > Rcap hits the capillary entrance wall. When Rcap /r0 increases, more laser energy can be coupled inside the capillary tube but
essentially to higher-order modes. It is thus less efficient to use an Airy beam than a Gaussian beam in
terms of laser coupling and monomode guiding. Another issue is capillary breakdown. The front surface
of the capillary tube is exposed to a greater energy for an Airy beam than for one with a Gaussian profile;
hence, the peak laser intensity has to be lowered to avoid capillary damage at the entrance.
To summarize, quasi-monomode guiding can be selected by coupling the input laser energy to the
fundamental EH11 mode: 98% of the energy of a Gaussian beam can be coupled to the fundamental
18
224

## PDF page 19

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 13: Example of guiding of a low-intensity laser in the absence of plasma

mode for a waist size w0 = 0.645Rcap . This mode is preferable for laser wakefield acceleration as its
group velocity is close to the velocity of light in free space, its damping factor is a minimum for a given
capillary radius and wavelength, and the transverse electric field exhibits a variation similar to a Gaussian
beam.
3.4

Experimental demonstration of laser guiding

Guiding in capillary tubes at low intensity has been measured and corresponds to theoretical predictions
in terms of coupling and transmission. Experimentally, the incident beam should be focused at the
entrance plane of the capillary tube, as illustrated in Fig. 13. In this case, a HeNe laser (λ0 = 632 nm)
was focused at the entrance of a capillary tube, of length 30 mm and inner diameter 127 µm. The focal
spot was measured to be Gaussian with a waist of about 43 µm, which corresponds to w0 = 0.68Rcap ,
close to the matching condition for monomode guiding. Figure 13 also shows the transmitted laser spot
at the output of the capillary, which is symmetrical and exhibits the pattern of the fundamental mode.
In this case, a transmission of 90 ± 2% was obtained experimentally, and can be compared with
the theoretical transmission. The transmission is defined as the ratio of incident and transmitted laser
energies at the capillary entrance and exit, respectively. The theoretical transmission of energy for the
fundamental mode is given by T1 = C1 exp(−2Lcap /Ll1 ) The theoretical value of the coupling coefficient C1 of a Gaussian beam for the EH11 mode is 97% for w0 = 0.68Rcap . The attenuation length
is calculated from Eq. (37) as L = 230 cm for λ0 = 632 nm and Rcap = 63 µm. Thus the theoretical
transmission is calculated as T1 = 94%, which is very close to the experimental value, suggesting that
excellent alignment and beam quality were achieved in the experiment, leading to quasi-monomode guiding. The sensitivity of the coupling and transmission to misalignments have been studied theoretically:
predictions are in excellent agreement with experimental results and are discussed in Ref. [33].
Monomode guiding has been demonstrated experimentally for laser intensities of the order of
I0 ≃ 1016 W/cm2 in a vacuum [34] and the transmission has been measured for different values of the
capillary tube radius. In agreement with theoretical predictions, the damping length was found to increase
with the cube of capillary radius, as illustrated in Fig. 14. The measured transmissions correspond to the
predicted values for quasi-monomode guiding, which was thus measured in a vacuum over a distance
of 100 Rayleigh lengths. Analytical predictions for coupling conditions and damping length have been
confirmed experimentally for tubes under vacuum.
3.5

Measurement of plasma waves in capillary tubes

The excitation of plasma waves over a length of up to 8 cm was, for the first time [21], demonstrated
using laser guiding of intense laser pulses through hydrogen-filled glass capillary tubes. Laser guiding at
input intensities up to 1018 W/cm2 was achieved with more than 90% energy transmission in evacuated
19
225

## PDF page 20

B. C ROS

Fig. 14: Measured transmission as a function of propagation distance for two values of the capillary tube radius,
Rcap = 35 µm (open circles and dotted line), and Rcap = 25 µm (filled circles and solid line).

Fig. 15: Spectrum of the laser beam at the output of a capillary tube in vacuum (black solid curve, the vertical line
indicates the centre of the spectrum in a vacuum through the capillary) and in 40 mbar of hydrogen (red line).

or hydrogen-filled gas tubes up to 8 cm long, with a radius of Rcap = 50 µm. To investigate the linear
and moderately non-linear regime, the input intensity was kept below 3 × 1017 W/cm2 , and the electron
density was varied in the range 0.05–5 × 1018 cm−3 . The plasma wave amplitude was diagnosed by
analyzing the spectrum of the transmitted laser radiation. Laser pulses transmitted through gas-filled
capillary tubes exhibit broadened spectra. In the range of parameters relevant to this experiment, spectral
modifications of the laser pulse driving the plasma wave, after propagating in the plasma over a large
distance, are mainly related to changes in the index of refraction of the plasma during the creation of the
plasma wave. The front of the laser pulse creates an increase in electron density, leading to a blueshift
at the front of the pulse, while the rear of the pulse creates a decrease of electron density with larger
amplitude, and thus a redshift of the spectrum.
The signature of plasma wave excitation is a redshift of the laser beam, i.e., a shift of the spectrum
towards longer wavelengths, as seen in Fig. 15. The spectrum at the output of a 7 cm long capillary was
measured in a vacuum and compared with the spectrum in the presence of 40 mbar of hydrogen filling
the tube.
The wavelength shift, ∆λ/λ can be shown [35] to be directly related to the energy of the plasma
wave with electric field, Ep , excited in the plasma volume, V ,
∫
∆λ
1
≃
E 2 dV ,
(46)
λ
16πEout V p

where Eout is the total energy of the transmitted laser pulse. For monomode propagation of a laser pulse
20
226

## PDF page 21

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

Fig. 16: Wavelength shifts as functions of the length of capillary filled with hydrogen at different pressure values,
as determined experimentally (symbols with error bars) and through modelling (curves).

with a Gaussian time envelope, generating a wakefield in the weakly non-linear regime, the wavelength
shift can be expressed analytically [21]. For small energy losses at the capillary wall, it is proportional to
the peak laser intensity on the capillary axis, and to the length of the capillary, and exhibits a resonant-like
dependence on gas pressure directly linked to plasma wave excitation. The dependence of the spectral
redshift was measured as a function of filling pressure, capillary tube length, and incident laser energy,
and was found to be in excellent agreement with results from modelling, as illustrated in Fig. 16. A
linear behaviour of the wavelength shift as a function of length is observed at 20 mbar. The fit of
experimental data by simulation results demonstrates that the plasma wave is excited over a length as
long as 8 cm. As the pressure is increased, the non-linear laser pulse evolution is amplified, with the
propagation length leading to a plasma wave amplitude larger than the linear prediction. The longitudinal
accelerating field, inferred from a detailed analysis of laser wakefield dynamics in capillary tubes and
numerical simulations [36], is in the range of 1–10 GV/m for an input laser intensity of the order of
I0 ≃ 1017 W/cm2 , as shown in Fig. 17. The average product of gradient and length achieved in this
experiment was thus of the order of 0.4 GV at a pressure of 50 mbar; it could be increased to several
gigavolts by increasing the length and diameter of the capillary tube with higher laser energy.
In conclusion, the outgoing spectra of driving laser pulses measured after propagation in gas-filled
capillaries supported by relevant modelling provide detailed information on laser pulse dynamics and on
the main characteristics of the accelerating fields excited in the wake of the laser pulses over the long
distances necessary for efficient acceleration of electrons to high energies.
4

Conclusion and perspectives

In summary, several features of laser-driven plasma wakefields linked to laser propagation in a plasma
were introduced and discussed. Numerous results from previous studies clearly indicate that reducing the
plasma density is the best method of increasing the energy of the accelerated electrons. At lower densities, such mechanisms as dephasing between the electron bunch and the plasma wave and the progressive
depletion of the driving laser pulse have to be taken into account, as they limit the maximum attainable
energy. Increased electron energy of the order of a few gigaelectronvolts is currently achieved at lower
plasma densities and higher laser peak powers, in non-linear regimes of laser plasma acceleration, where
21
227

## PDF page 22

B. C ROS

Fig. 17: Average amplitude of the plasma wave electric field measured at the output of a 8 cm long glass capillary
tube as a function of filling pressure.

extending the plasma length to the dephasing length is a challenge. Eventually, lowering the plasma
density will lead to a regime where self-injection of plasma electrons in the plasma wave does not take
place and injection of electrons from external sources has to be implemented.
Ongoing efforts of accelerator development tend to increase the energy of electrons, while improving the electron bunch properties, of which energy spread and transverse emittance are key parameters for beam transport and focusing, as well as subsequent applications. Separating electron injection
and acceleration processes, and relying on a number of purely accelerating stages [37], provide solutions
to the issues of dephasing and depletion, and make the acceleration process scalable to higher energies,
while preserving the bunch quality. Two crucial aspects of multistage laser-driven plasma acceleration
are laser guiding over metre-scale distances [38] and control of the properties of the electron bunch for
external injection into the plasma wave of the accelerating stage.
Future work will tackle the different issues of multistage laser-driven plasma acceleration. Laser
guiding and increased laser energy are expected to produce electron bunches in the 10 GeV range in
one stage (see, for example, the BELLA project [39] in the USA or the CILEX APOLLON project [40]
in France). Staging is the next milestone for the development of laser-driven plasma accelerators. The
APOLLON laser facility [41], under construction in France, will provide two beams in the 1–10 PW
range, and a shielded large experimental area built to host multistage experiments [40]. In those experiments, the first stage (i.e., the injector) will be used to generate electrons in the 50–200 MeV range,
which will then be transported [42] and focused into the accelerator stage. The quality of the accelerated
bunch will thus result from the combined intrinsic properties of the injector and the capability of the
transport line to accommodate them.
In the long term, the development of laser-driven accelerators will rely on improvements in the
performance of laser systems, in terms of beam quality, reliability, stability, and average power. Plasma
stages in the quasi-linear regime provide means to control transverse and longitudinal fields, and consequently the dynamics of accelerated bunches. Electron or positron beams can be accelerated in this
regime, and external injection schemes into metre-scale low-density plasma sources need to be developed.

22
228

## PDF page 23

L ASER - DRIVEN P LASMA WAKEFIELD : P ROPAGATION E FFECTS

References
[1] T. Tajima and J.M. Dawson, Phys. Rev. Lett. 43(4) (1979) 267.
http://dx.doi.org/10.1103/PhysRevLett.43.267
[2] F.F. Chen, Introduction to Plasma Physics and Controlled Fusion, 2nd ed. (Plenum, New York,
1983).
[3] E. Esarey et al., Rev. Mod. Phys. 81(3) (2009) 1229.
http://dx.doi.org/10.1103/RevModPhys.81.1229
[4] N.E. Andreev et al., JETP Lett. 55 (1992) 571.
[5] A. Pukhov and J. Meyer-ter-Vehn, Appl. Phys. B 74(4) (2002) 355.
http://dx.doi.org/10.1007/s003400200795
[6] S.P.D. Mangles et al., Nature 431 (2004) 535. http://dx.doi.org/10.1038/nature02939
[7] C.G.R. Geddes et al., Nature 431 (2004) 538. http://dx.doi.org/10.1038/nature02900
[8] J. Faure et al., Nature 431 (2004) 541. http://dx.doi.org/10.1038/nature02963
[9] W.P. Leemans et al., Phys. Rev. Lett. 113(24) (2014) 245002.
http://dx.doi.org/10.1103/PhysRevLett.113.245002
[10] B.E.A Saleh and M.C. Teich, Fundamentals of Photonics (John Wiley & Sons, Hoboken, NJ,
2007).
[11] J. Ju et al., Phys. Plasmas 20(8) (2013) 083106. http://dx.doi.org/10.1063/1.4817747
[12] P. Gibbon, Short Pulse Laser Interactions With Matter (Imperial College Press, London, 2005).
[13] E. Esarey et al., IEEE Trans. Plasma Science 24(2) (1996) 252.
http://dx.doi.org/10.1109/27.509991
[14] W.L. Kruer, The Physics of Laser Plasma Interactions (Westview Press, Boulder, CO, 2003).
[15] W. Lu et al., Phys. Rev. ST Accel. Beams 10(6) (2007) 061301.
http://dx.doi.org/10.1103/PhysRevSTAB.10.061301
[16] W.B. Mori, IEEE J. Quant. Elec. 33(11) (1997) 1942. http://dx.doi.org/10.1109/3.641309
[17] G.-Z. Sun et al., Phys. Fluids 30 (1987) 526. http://dx.doi.org/10.1063/1.866349
[18] P. Sprangle et al., Appl. Phys. Lett. 53(22) (1988) 2146. http://dx.doi.org/10.1063/1.100300
[19] E. Esarey et al., Phys. Fluids B 5(7) (1993) 2690. http://dx.doi.org/10.1063/1.860707
[20] J. Schreiber et al., Phys. Rev. Lett. 105(23) (2010) 235003.
http://dx.doi.org/10.1103/PhysRevLett.105.235003
[21] F. Wojda et al., Phys. Rev. E 80(6) (2009) 066403. http://dx.doi.org/10.1103/PhysRevE.80.066403
[22] C.G.R. Geddes et al., Phys. Plasmas 12(5) ( 2005) 056709. http://dx.doi.org/10.1063/1.1882352
[23] B.A. Shadwick et al., Phys. Plasmas 16(5) (2009) 056704. http://dx.doi.org/10.1063/1.3124185
[24] C.D. Decker et al., Phys. Plasmas 3(5) (1996) 2047. http://dx.doi.org/10.1063/1.872001
[25] D.J. Spence and S.M. Hooker, Phys. Rev. E 63(1) (2000) 015401(R).
http://dx.doi.org/10.1103/PhysRevE.63.015401
[26] D.J. Spence et al., J. Opt. Soc. Am. B 20(1) (2003) 138.
http://dx.doi.org/10.1364/JOSAB.20.000138
[27] C.G.R. Geddes et al., Phys. Rev. Lett. 95(14) (2005) 145002.
http://dx.doi.org/10.1103/PhysRevLett.95.145002
[28] W. Leemans et al., Philos. Trans. R. Soc. A 364(1840) (2006) 585.
http://dx.doi.org/10.1098/rsta.2005.1724
[29] A. Butler et al., Phys. Rev. Lett. 89(18) (2002) 185003.
http://dx.doi.org/10.1103/PhysRevLett.89.185003
[30] B. Cros et al., Phys. Rev. E 65(2) (2002) 026405. http://dx.doi.org/10.1103/PhysRevE.65.026405

23
229

## PDF page 24

B. C ROS
[31] D. Du et al., Appl. Phys. Lett. 64(23) (1994) 3071. http://dx.doi.org/10.1063/1.111350
[32] E. Hecht, Optics, 4th ed. (Addison Wesley, Reading, MA, 2002).
[33] M. Veysman et al., J. Opt. Soc. Am. B 27(7) (2010) 14008.
http://dx.doi.org/10.1364/JOSAB.27.001400
[34] F. Dorchies et al., Phys. Rev. Lett. 82(23) (1999) 4655.
http://dx.doi.org/10.1103/physrevlett.82.4655
[35] N.E. Andreev and M. Chegotov, JETP 101(1)(2005) 56. http://dx.doi.org/10.1134/1.2010661
[36] N.E. Andreev et al., New J. Phys. 12 (2010) 045024.
http://dx.doi.org/10.1088/1367-2630/12/4/045024
[37] W.P. Leemans and E. Esarey, Physics Today 62(3) (March 2009) 44.
http://dx.doi.org/10.1063/1.3099645
[38] B.S. Paradkar et al., Phys. Plasmas 20(8) (2013) 083120. http://dx.doi.org/10.1063/1.4819718
[39] BELLA: The Berkeley Lab Laser Accelerator. http://www.lbl.gov/community/bella/
[40] B. Cros et al., Nucl. Instrum. Meth. A 740(11) (2014) 27.
http://dx.doi.org/10.1016/j.nima.2013.10.090
[41] J.P. Zou et al., High Power Laser Sci. Eng. 3 (2015) e2. http://dx.doi.org/10.1017/hpl.2014.41
[42] A. Chancé et al., Nucl. Instrum. Meth. A 740(11) (2014) 158.
http://dx.doi.org/10.1016/j.nima.2013.10.036

24
230
