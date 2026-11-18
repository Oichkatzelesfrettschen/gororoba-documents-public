Source: see manifest row of the PDF
PDF sha256: 87272aab35c8ac51848f39f4a0a0212a8e8ecedd7b60cb45f012653794aea247
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of endrizzi_2023_physics_basis_for_the_wisconsin_hts_axisymmetric_mirror_wham.pdf

Transcription of `endrizzi_2023_physics_basis_for_the_wisconsin_hts_axisymmetric_mirror_wham.pdf` in this directory, 35 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-35 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

J. Plasma Phys. (2023), vol. 89, 975890501 © The Author(s), 2023.
Published by Cambridge University Press
This is an Open Access article, distributed under the terms of the Creative Commons Attribution
licence (http://creativecommons.org/licenses/by/4.0/), which permits unrestricted re-use, distribution
and reproduction, provided the original article is properly cited.
doi:10.1017/S0022377823000806

1

Physics basis for the Wisconsin HTS
Axisymmetric Mirror (WHAM)
D. Endrizzi 1 , J.K. Anderson 1 , M. Brown 2 , J. Egedal 1 , B. Geiger 1 ,
R.W. Harvey 3 , M. Ialovega 1 , J. Kirch1 , E. Peterson 4 , Yu.V. Petrov 3 ,
J. Pizzo 1 , T. Qian 1,5 , K. Sanwalka 1 , O. Schmitz 1 , J. Wallace 1 , D.
Yakovlev 1 , M. Yu 1 and C.B. Forest 1, †
1 University of Wisconsin-Madison
2 Swarthmore College
3 CompX
4 MIT
5 Princeton University

(Received 24 May 2023; revised 18 July 2023; accepted 21 July 2023)

The Wisconsin high-temperature superconductor axisymmetric mirror experiment
(WHAM) will be a high-field platform for prototyping technologies, validating
interchange stabilization techniques and benchmarking numerical code performance,
enabling the next step up to reactor parameters. A detailed overview of the experimental
apparatus and its various subsystems is presented. WHAM will use electron cyclotron
heating to ionize and build a dense target plasma for neutral beam injection of fast ions,
stabilized by edge-biased sheared flow. At 25 keV injection energies, charge exchange
dominates over impact ionization and limits the effectiveness of neutral beam injection
fuelling. This paper outlines an iterative technique for self-consistently predicting the
neutral beam driven anisotropic ion distribution and its role in the finite beta equilibrium.
Beginning with recent work by Egedal et al. (Nucl. Fusion, vol. 62, no. 12, 2022,
p. 126053) on the WHAM geometry, we detail how the FIDASIM code is used to model
the charge exchange sources and sinks in the distribution function, and both are combined
with an anisotropic magnetohydrodynamic equilibrium solver method to self-consistently
reach an equilibrium. We compare this with recent results using the CQL3D code adapted
for the mirror geometry, which includes the high-harmonic fast wave heating of fast ions.
Key words: fusion plasma, plasma devices

1. Introduction

The Wisconsin high-temperature superconductor axisymmetric mirror (WHAM) is
intended to operate in the weakly collisional or classical mirror (CM) regime in which
† Email address for correspondence: dendrizzi@wisc.edu

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 2

2

D. Endrizzi and others

F IGURE 1. The historical record of fast ion confinement time for beam driven simple mirrors
compared with (3.4) and for thermal ions in the tandem configuration.

particle confinement is governed by ion–ion pitch angle scattering rather than electron
drag on fast ions. While this was typical of the earlier non-axisymmetric experiments (see
figure 1), WHAM will extend recent advances from the gas dynamic regime, characterized
by strong sonic losses, to the CM regime, where ion pitch angle scattering controls the
particle confinement time.
Axisymmetric linear devices are unstable to magnetohydrodynamic (MHD) interchange
modes, with fast growth rates γMHD of the order of an inverse ion bounce time, τbounce =
Lp /vthi (Fowler 1981; Post 1987), the mirror half-length Lp over the ion thermal velocity.
However, experiments and simulations have shown that interchange modes with m ≥ 2 can
be stabilized by the ion’s finite Larmor radii (FLR) when the experiment is long enough,
and also that the m = 1 mode can be shear-flow stabilized at low amplitude when the
shearing rate exceeds the growth rate by roughly a factor of 2 (Beklemishev et al. 2010;
Bagryansky et al. 2011, 2015; Yakovlev et al. 2018; Soldatkina et al. 2020). A combination
of a high-mirror-ratio axisymmetric magnet system and electron cyclotron heating of
a sufficiently dense plasma has led to electron temperatures of 1 keV and dispelled
the myth that electrons are always ‘dead cold’ in mirrors. Separately, the development
of high-temperature superconductor (HTS) magnets appropriate for fusion applications
(Whyte et al. 2016; Whyte 2019) now allows for larger mirror ratios and better classical
confinement, while axisymmetry precludes neoclassical effects. Together, these significant
developments motivate this re-examination of fusion mirror devices.
WHAM will demonstrate several key technological milestones that show the viability
of fusion mirrors: retiring the engineering risks of constructing circa 20 T magnets; use
of electron cyclotron heating for breakdown, localized Te (r) control and temperatures
of Te ≥ 1 keV; extending MHD stabilization of axisymmetric plasmas to collisionless
environments; and demonstrating high-harmonic fast wave (HHFW) heating on injected
neutral beam ions. Perhaps most important, the proper modelling of the physics of these
features and benchmarking of computational methods against experimental results is
essential to its mission as a development platform for future linear devices. This paper lays

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 3

Physics basis for WHAM

3

out performance predictions for the WHAM experiment, and the methods in this paper will
be used in a concurrent paper designing a larger break-even axisymmetric mirror device.
We start with § 2 and give an overview of the engineering design of WHAM,
with summaries of the magnets and field geometry (§ 2.1), the vacuum vessel and
fuelling system (§ 2.2), the electron cyclotron heating (ECH) system (§ 2.3), the neutral
beam injection (NBI) system (§ 2.4), the radio-frequency (RH) HHFW heating system
(§ 2.5) and the biased limiter and end-ring system (§ 2.6). Then, in § 3, we discuss
the performance modelling of WHAM, beginning first with a general discussion of the
mirror physics. Section 3.1 addresses the most pressing issue for all axisymmetric mirror
experiments, MHD stability, and briefly discusses FLR effects and vortex stabilization.
Section 3.2 explains the several roles of the ECH system: first, in ionizing the target
plasma and in driving the transition to the collisionless mirror regime, and in localized
heating to produce sheared flow profiles. Section 3.3 looks at the feasibility of fuelling
via NBI on WHAM given its limited opacity, focusing on the outsize role of charge
exchange collisions in determining the ion distribution function. Section 3.4 discusses the
anisotropic equilibrium calculation method using the semi-analytic results from the fast
beam-ion solver code (FBIS) (see Egedal et al. 2022). Section 3.5 discusses the anticipated
role of kinetic instabilities, as well as enhanced radial transport from turbulence. Section
3.6 looks at the role of fast-ion adiabaticity in limiting device performance at low fields.
Finally, § 3.7 concludes by integrating §§ 3.1–3.6 into a holistic upper-limit prediction for
WHAM performance, presenting results from both the FBIS simulations, but also recent
results from the newly developed code CQL3D-mirror.
With the exception of §§ 3.5 and 3.6, all of these methods are purely classical in
nature. These results then represent an absolute best case scenario for a steady-state
plasma, one unperturbed by MHD and kinetic instabilities, uninhibited by gradient driven
turbulence and unbothered by impurities. Despite the many fewer mirror experiments as
compared with tokamaks, these issues have each individually been addressed theoretically
and managed experimentally. However, solving them simultaneously remains to be
demonstrated at reactor relevant scales. Modelling of each of these of substantial topics
will be presented in future papers.
2. Overview of WHAM and subsystems

Basic operation of the WHAM device works as follows: deuterium gas is puffed into the
central cell close to the ECH injection point. A total of 1 MW of 110 GHz crosses the 4 T
resonant surface with X-mode polarization to ionize a target plasma of radius a = 0.1 m
and density 1 − 3 × 1019 m−3 . This target is next struck with a 10 ms pulse of 25 keV,
40 A, 45◦ -inclined deuterium neutral beam producing a sloshing ion distribution. Biasing
of the limiters and rings in the expander region will impose a transverse electric field E
which interacts with the magnetic field B to produce an E × B drift in the edge, providing
the vortex confinement to saturate MHD instabilities at small amplitude. After a year of
operation, a 1 MW RF antenna will use second harmonic heating of the sloshing ions,
accelerating these particles above their injection energy. Figure 2 shows an engineering
schematic of the central region of WHAM for reference.

2.1. Magnets and Field Geometry
The 17 T, 2 kA steady state, 5.5 cm warm bore HTS mirror magnets, custom built by
Commonwealth Fusion Systems, are centred at z = ±98 cm. In addition, two pulsed
copper coils, repurposed from the Wendelstein-7A experiment, will be located near the
midplane at z = ±20 cm. They will be driven with Transrex power supplies with a 1 s
rise time to increase the central field from 0.32 T to a maximum of 0.86 T. At the highest

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 4

4

D. Endrizzi and others

F IGURE 2. Overhead section of WHAM with contours of field strength. The colour contours
represent the 4 T ECH resonance (yellow), the fast ion turning√point at 2B0 = 1.72 T (green)
and the expansion ratio for electron thermal confinement Bmir me /mi (blue). Numbered: (1)
ECH injection port, (2) NBI beam path, (3) HHFW antenna, (4) limiter.

fields, the compressive force between the HTS magnets will reach 60 tons, with three 304
stainless steel struts on the central cell bearing this load.
As seen in the Gas Dynamic Trap (GDT) experiment (see Bagryansky, Beklemishev
& Postupaev 2018),
√ a sufficiently large expansion ratio in the field outside of the mirrors,
Rexp ≡ Bmir /B ≥ mi /me , leads to increased electron thermal confinement (Yakovlev et al.
2018; Soldatkina et al. 2020) when compared with prior mirror experiments. This is due
to the parallel ambipolar potential that preserves quasineutrality, trapping the thermal
electron population (Boldyrev, Forest & Egedal 2020). In the less collisional WHAM case,
the parallel potential drop is predicted to happen in the central cell rather than the expander
region (Egedal et al. 2022). Still, the transition from gas dynamic to a CM will benefit from
the large expansion ratio by reducing thermal losses from the electrons to the end rings on
startup.

2.2. Vacuum Vessel and Fuelling System
The central cell vessel (manufactured by Nor-Cal) is bounded on either end by the
HTS mirror magnets, which are in turn bookended by large expansion tank end cells
(repurposed from the LANL CTX experiment). The strong stray magnetic fields require
turbopumps to be several metres from the HTS magnets: two turbos will be placed on
long pumping ducts leading to the central cell, and two on the end cells. Including the
cryopumps, the total centre cell pumping is 4800 l s−1 for 200 l, and the total end cell
pumping is 8400 l s−1 each for 3900 and 4400 l. This does not include the additional
pumping in the NBI source and titanium gettering in the beam dump, described later.
WHAM will be fuelled by piezoelectric gas valves placed close to the plasma inside the
central cell, with an actuation time of under 1 ms. A maximum of four injectors will be
available and each can be supplied with an arbitrary mixture of hydrogen, deuterium,
helium and argon gas for fuelling and diagnostic purposes. Two injectors on pivoting
mounts will supply gas fuelling at both ends of the central cell near the 4 T ECH
resonance surfaces, one injector on a telescopic mount will be available at the mid-plane
for diagnostics such as gas puff imaging and the remaining injector will be fixed on one

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 5

Physics basis for WHAM
(a)

5

(b)

F IGURE 3. Vacuum fields of WHAM at low field (a) and high field (b), not to scale. While the
ECH resonant surface stays nearly constant axially, the fast ion turning point at Rm ≡ B/B0 = 2
moves 20 cm and the radius decreases from 15 to 9 cm.

of the end cells. The Wisconsin in situ Penning gauge will provide fast measurements of
neutral gas pressure near the plasma edge (Kremeyer et al. 2020).
Successful plasma performance relies on the removal of neutral hydrogen atoms in
the plasma edge to reduce energy losses from charge exchange events. In WHAM, a
cold-sprayed tantalum coating on the inner surface of the central cell vacuum vessel will
be tested as a neutral pump. The high melting temperature, excellent room-temperature
ductility, outstanding corrosion resistance, low sputtering yield by hydrogen isotopes
and exothermic hydrogen absorption are beneficial properties of tantalum, alongside
the enhanced retention capacity of the engineered cold spray coatings. Our recent
experimental work (Ialovega et al. 2023) has shown that tantalum coatings sprayed on
SS 316L substrates maintain their mechanical integrity and physical properties upon high
dose (3 × 1025 D m−2 ) deuterium irradiation and subsequent thermal annealing up to
1100 K. The absorbing tantalum first wall interface can therefore be regenerated by heating
during wall conditioning to free up the trapping sites for hydrogen. This same technology
may later be used for coating the plasma-facing components in the expansion tank rings.

2.3. The ECH System
The ECH system is built around a Gycom gyrotron and various ancillary equipment
decommissioned from both the DIII-D and KSTAR tokamak experiments. The remainder
of the ECH system includes a modern field programmable gate array (FPGA) control
system, a General Atomics designed two-mirror aiming system that utilizes an electrically
biased split waveguide to cross through the cyclotron resonance to the high-field side
where it is launched and a full transmission line including two power monitor miter bends,
two polarization shift miter bends, a 5 kV DC voltage break, pumpout tee, waveguide
switch (to dummy load or machine), waveguide vacuum valve and all necessary straight
lengths and couplers. Figure 4 contains a rendering of the in-vessel section, including the
split waveguide.
The WHAM experiment plans to use fundamental high-field side X-mode ECH for two
purposes. The first is to breakdown plasma and build up target density prior to NBI heating,
similar to how the GDT device initiates discharges using ECH (Yakovlev et al. 2017). The
second is to provide additional heating to the electrons, beyond the collisional heating
from fast neutral beam ions, to transition from the gas dynamic regime to the CM regime
and improve overall confinement. Without ECH, the initially cold electrons will act as a
drag on the fast ions, preventing them from moving into the high ion temperature and good
confinement regime of the CM. The very large ECH power density (1 MW/40 l) should be

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 6

6

D. Endrizzi and others
(a)

(b)

(c)

F IGURE 4. Transmission line leading from low stray field area of the gyrotron to WHAM
device. (a) Shows the first section between the matching optics unit and the dummy load, (b)
shows the long waveguide run from the gyrotron cage to the vacuum vessel and (c) shows a CAD
rendering of the in-vessel transmission line.

enough to allow this transition. This configuration is optimal as high-field side injection
is strongly absorbed at low plasma density (see § 3.2) and is thus good for building up
density. And with the higher frequency (110 GHz, compared with 54.5 GHz on the GDT),
the waves can propagate without diffraction at four times higher density.
Accurately predicting the electron temperature achievable with our ECH system
involves a significant multi-factor analysis, which must include effects of collisions with
background neutrals, slowing down of fast ions on electrons, ion loss rate and bias
ring voltage profile among other factors. Until such an analysis is complete, we will
compare with the results of the GDT device to get a rough estimate of our target electron
temperature. GDT was able to achieve a stable electron temperature of 600 eV using ECH
with a power density of 0.4 MW/300 l. The ECH power density in WHAM is 1 MW/40 l,
therefore we predict we will be able to achieve an electron temperature of at least 1 keV.

2.4. The NBI System
The WHAM experiment will use a 25 keV, 40 A neutral beam originally built for TAE
Technologies by the Budker Institute of Nuclear Physics. The beam uses an inductively
driven RF plasma source, with characteristic primary-, half- and third-energy components
of 70 %, 20 % and 10 %, respectively. The neutralizer for the NBI is 80 cm long and will
operate at a pressure of 5.2 mTorr during a shot. In order to prevent this neutral gas
from entering the central cell, the NBI is equipped with 2 cryopumps, each capable of
a hydrogen pumping speed of 7 × 104 l s−1 . NBI injection is through the origin at a 45◦

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 7

Physics basis for WHAM

7

angle with respect to the machine axis (see figure 2). The 45◦ injection angle sets the
turning point for injected fast ions at the position where the magnetic field strength is
twice the central field B = 2B0 (see figure 3). The first phase of the experiment will begin
with power supplies capable of 10 ms of injection.
One NBI system acts as an unbalanced m = 1 perturbation on the plasma column. In
general, when the shear-flow stabilization is operational then the E × B drifts will rapidly
make symmetric the fast-ion content and this perturbation should be negligible. Although
one NBI system will be sufficient for full plasma performance in WHAM (see § 3.3), the
vessel has space for a second NBI system in case this assumption is not correct.
If injected beam particles slow without pitch angle scattering, they form a ‘sloshing
ion’ distribution with several important features. Such a distribution has an axial density
peak at the turning points and consequently forms a potential well that can trap a warm
thermal ion population. The trapped thermal ions provide kinetic stability against the
drift cyclotron loss cone instability (DCLC) by filling in the ambipolar hole in the ion
distribution function (Kesner 1973; Simonen et al. 1983). In addition, angled injection
decreases the pressure anisotropy compared with perpendicular injection, mitigating the
Alfvén ion cyclotron (AIC) instability (Smith 1984). The sloshing ion population will be
resolved with a proton detector array to measure the axial and radial intensity of 3.02 MeV
D-D fusion protons. The degree of peaking is sensitive to the collisionality, with cold Te
plasmas more strongly peaked as fast ions rapidly slow without diffusing in pitch angle.
These sloshing ions are also critical to the HHFW RF heating described below.

2.5. The RF Heating System
A primary physics mission of WHAM is to accelerate high-energy beam-born sloshing
ions by ion cyclotron absorption at the second to fourth harmonics of deuterium. With
the 0.86 T central field, the 2Ωci deuterium ion cyclotron frequency at the turning
point is 26 MHz. A well-suited 1 MW Thales transmitter has been transported from the
Archimedes device and is currently being commissioned pending substantial laboratory
infrastructure upgrades. A complete RF transmission line utilizing components from both
the LDX and C-Mod experiments at MIT is on site and ready for assembly. This includes
two long stub tuners, bi-directional couplers with detectors, suitable pre-amplifiers and
downstream electronics, several crates and cabinets full of miscellaneous elbows, straight
lengths, tee adaptors and vacuum windows.
For the first phase of the experiment, RF heating will be done via an m = 0 single
strap antenna collocated with the sloshing ions’ turning point, where their density and
residence times are maximized. As higher harmonic cyclotron damping is an FLR effect,
fast ions will be preferentially heated, further improving their confinement (Stix 1992).
The synergy between HHFW heating and neutral beam heating for enhancing the number
of high-energy ions has been robustly observed and demonstrated on tokamaks (Petty et al.
2001; Rosenberg et al. 2004) and also simulated by Fokker–Plank calculations (Harvey,
Petrov & Forest 2016).
A COMSOL Multiphysics finite-element model has been constructed using the RF
module in the frequency domain to simulate antenna performance. To model wave
propagation in the plasma, a fully anisotropic cold plasma dielectric tensor including
artificial collisional damping was used (Lau et al. 2019). Both two-dimensional (2-D)
axisymmetric and full 3-D simulations were run to inform the preliminary design of the
first antenna. The 3-D RF electric field magnitudes with moderate, uniform collisional
damping are shown in figure 5 together with a rendering of the antenna geometry. A single
strap antenna fed by parallel plate transmission lines has been shown to couple to a cavity
eigenmode in the limit of low single pass damping over a large range of core densities.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 8

8

D. Endrizzi and others

F IGURE 5. A three-dimensional COMSOL simulation of RF electric field strength (V m−1 )
with 100 kW incident power at 28 MHz, with artificial collision rate at 0.01ωci .

When collisional damping is increased, the loading impedance was found to be strongly
dependent on the edge density profile, but was of order 0.1–1 Ohm.
There is an ongoing effort to incorporate hot plasma effects such as higher harmonic
ion cyclotron damping in self-consistent, full-wave simulations. We are exploring the
possibility of coupling the KineticJ code to the cold plasma finite-element COMSOL
model via kinetic correction currents (Green et al. 2018), while the AORSA code is also
being adapted for the mirror geometry (Jaeger et al. 2001).

2.6. Biased limiter and end-ring system for controlling sheared flow
Magnetic mirrors have both radial and axial boundary conditions. In WHAM, the radial
boundary condition is set by a tungsten limiter positioned in the central cell, and
the axial boundary condition is set by an ensemble of concentric molybdenum end
rings installed in both end cells. Tungsten and molybdenum were chosen for their high
melting temperatures, resistance to sputtering by hydrogen isotopes and for manufacturing
considerations. Figure 6 shows a photograph of the end rings, and also the central cell
mounted limiter, which defines the potential on the outermost confined flux surface of the
plasma. Both the limiter and end rings are mounted on linear axial translation stages to
account for changes in the shape of the magnetic flux surface (see figure 2).
The limiter will be positioned to screen the HTS mirror coil cryostat from particle fluxes.
Each end-ring ensemble consists of 19 rings, 10 of which can be independently biased at
voltages up to 2.5 keV to create a radial electric field and hence a sheared rotation at the
radius of choice. The biased rings are spaced with 9 isolated (floating) rings to prevent
arcing. A set of programmable power supply modules has been modified to power the
biased rings. The expected bias potential is comparable to the electron temperature, Te ∼
1 keV, while the expected current draw of several hundred amps is set by ion saturation
current and is far below the 2 kA power supply rating.
A sub-goal of the WHAM experiment is to combine the expander bias end rings for
vortex confinement with a direct energy converter (DEC). This will have substantial
plasma–material interaction and engineering challenges. Single and multi-stage converters
have long since demonstrated more than 50 % efficiency on tandem mirror devices (Barr,

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 9

Physics basis for WHAM
(a)

9

(b)

F IGURE 6. Panel (a) (photo) shows one end-ring ensemble mounted in the end cells for radial
field control and panel (b) (rendering) a tungsten limiter to bias the outermost confined flux
surface. The limiter is electrically insulated from the rest of the assembly and is linearly
translatable.

F IGURE 7. An example FBIS histogram of the on-axis lost ion distribution at the segmented
end rings, after acceleration by the 5Te /e potential.

Moir & Hamilton 1982). The ambipolar accelerated distribution makes the use of a DEC
promising, as even a single stage DEC should be able to recapture 5Te /E0 of the injected
neutral beam energy. figure 7 shows the exhaust ion energy distribution for the same
dataset used later in § 3.7.
3. Performance Modelling of WHAM

Classical confinement in the simple mirror is governed by pitch angle scattering of
ions into a loss cone modified by the ambipolar field that limits the loss of electrons
(Bing & Roberts 1961; Fowler & Rankin 1962, 1966). The collisional relaxation of the
ion distribution function is governed by two time scales
3/2
Te,keV
μ
n20 τs = 5
ms,
2
Z
⟨Ei,keV ⟩3/2 μ
n20 τii =
ms,
8Z 2

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

(3.1)
(3.2)

## PDF page 10

10

D. Endrizzi and others

where τs represents slowing and energy loss to electrons, τii is the ion–ion pitch angle
scattering time, μ is the ion mass in units of proton masses and Z is the ion charge. It is
easy to see that these time scales are similar when Te = ⟨Ei ⟩/402/3 ∼ ⟨Ei ⟩/10.
Consider the idealized experiment that fuels plasma with a high-energy neutral beam:
when the electron temperature is low, Te ≤ ⟨Ei ⟩/10, the ions slow down before scattering
into the loss cone, and the confinement, which is still determined by the ion temperature
and pitch angle scattering rate, is essentially set by the electron slowing time. At higher
electron temperatures, the situation reverses and the confinement becomes independent
of the electrons, dependent only on the ion energy. This confinement gets very long
3/2
at high ion energies, as τii ∝ Ei . The fusion gain Q, however, does not continue
improving at higher temperatures due to increased radiative losses, as can be seen
in figure 1.
The much lighter electrons pitch angle scatter more rapidly, on a time scale associated
with electron–electron collisions
3/2

n20 τee = 5.8Te,keV µs.

(3.3)

These electrons would be lost very quickly (compared with the ions) were it not for
the development of a self-consistent ambipolar potential that retains the electrons and
increases ion losses. The result is that electrons essentially thermalize and only the
very high-energy electrons with energies above 5Te leave the system. The role of this
ambipolar potential is profound: it ensures the electron confinement and also leads to
plasma flows (both an outflow but also, as will be shown, rotation). However, this potential
also creates an ambipolar ‘hole’ in the ion distribution function that can lead to kinetic
instabilities.
For the simple case of NBI-only plasmas, a number of authors (see Killeen & Marx
1970; Killeen, Mirin & Rensink 1976; Egedal et al. 2022) have considered how the
classical confinement scales with beam injection energy by solving the Fokker–Planck
equation for the self-consistent ambipolar potential, electron temperature and ion
distribution function. The results are all generally in agreement with
3/2
n20 τp = 250Eb,100
keV log10 Rm ms,

(3.4)

although the exact coefficient depends on details, such as the shape the magnetic field,
the injection angle and the degree to which electrons are heated by alpha particles in a
deuterium-tritium (DT) device. Contrast this with the gas dynamic (GD) or collisional
confinement time of
Rm Lp
−1/2
τGDT =
= 5.2Rm Lp Te,keV µs,
(3.5)
cs
where Rm is the mirror ratio and Lp is again the plasma half-length (Ivanov & Prikhodko
2013). Mirrors might be expected to transition from the GD to CM regime as the
ions become less collisional. For this reason (among others), care must be taken to
self-consistently model the exact magnetic coil geometry, the ion distribution function
and also the resulting effect of the plasma currents on magnetic equilibrium. Equation
(3.4) is well supported by the historical record of fast ion confinement shown in figure 1 in
minimum-B mirrors (Coensgen et al. 1975; Post 1987; Wurzel & Hsu 2022). Historically,
the data collection ended when the US mirror program was cancelled in 1986. Perhaps
most relevant to this paper are the 2XIIB results at mirror ratio 2 that achieved the first
10 keV ion plasma (Coensgen et al. 1975). The GDT is not included here as its pulse length

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 11

Physics basis for WHAM

11

is shorter than the expected fast-ion confinement time, and because it is a two component
plasma with both warm and hot ions.
In the modelling that follows, our starting point is provided by the FBIS code (Egedal
et al. 2022), with the FBIS quasi-analytic solution for the fast ion distribution function and
electron temperature, the self-consistent ambipolar potential and density along a single
flux tube. In the FBIS solver, electron drag on the fast-ion population heats the electrons,
and the electrons do work sustaining the ambipolar potential which accelerates the exhaust
ions. An additional input heating term, paux. , is added to describe ECH heating, radiative
cooling or some other source of power to the electron species. To extend these results, we
combine a set of 1-D solutions from the FBIS code of Te , p∥ (B/B0 ), p⊥ (B/B0 ), n(B/B0 )
and φ(B/B0 ) to construct the 2-D equilibrium for a given magnetic geometry, where
again B0 is the midplane field. The solution includes both magnetic and electric equilibria
including the plasma flows.
As pressure and therefore β = 2μ0 p/B20 increases, plasma diamagnetism excavates the
magnetic field, increasing the mirror ratio and improving confinement
−1/2
Rm = Rvac
.
m (1 − β)

(3.6)

As has been noted by a number of authors, this improvement in confinement at high
pressures could lead to very high Q values, even in the simple mirror (Beklemishev 2016).
Hence, getting the equilibrium right (§ 3.4) is critical for assessing performance. However,
very high β values such as those observed in 2XIIB, would seem to be inconsistent with
mirror confinement due to adiabaticity issues, and so equilibria must be evaluated against
this constraint as well. Furthermore, (3.4) and (3.6) make clear that in going from β = 0
to β = 0.9, the gain in nτ is only 50 %.
With this background, we now address individual subtopics before integrating them in
§ 3.7.

3.1. MHD Stability
The principal challenge in developing the axisymmetric mirror is, and has always been,
stabilizing the flute or interchange mode that is universally unstable in non-cusped
axisymmetric systems (Rosenbluth & Longmire 1957). The strategy for WHAM will be
to use the known physics of FLR and vortex stabilization first, and later to test other
promising techniques that may extrapolate better to future fusion reactors. Many ideas
have been suggested and demonstrated to work over the past 50 years, (summarized well
by Ryutov et al. 2011), including the use of good curvature (Mirnov & Ryutov 1979;
Bagryansky et al. 2011), cusp boundaries (Prater 1971; Ferron et al. 1983; Kotelnikov
et al. 2019), ponderomotive effects (Ferron et al. 1987), rotating magnetic fields (Seemann,
Be’ery & Fisher 2018; Zhu et al. 2019), close fitting conducting shells (Kesner 1985;
Beklemishev 2016; Kotelnikov et al. 2022) and feedback (Prater 1971; Be’ery, Seemann
& Fisher 2014; Be’ery & Seemann 2015; Beklemishev 2017).
FLR stabilization of m > 1: hot temperatures and energetic ions in mirrors are
beneficial to MHD stability because FLR effects stabilize interchange for azimuthal mode
numbers m > 1. For this to occur, a magnetic mirror must be long enough to satisfy
(Ryutov et al. 2011)
a2
a/ρi
m>2
,
(3.7)
=2
Lp ρi
Lp /a
which sets a critical plasma half-length Lp , given ion gyroradius ρi and plasma radius a.
Ryutov’s scaling is derived from a dispersion relation of the form ω2 + mω(vTi ρi /a2 ) +

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 12

12

D. Endrizzi and others

Γ02 , where Γ0 ∼ vTi /Lp . For WHAM-0.86 with a/ρi = 4 and Lp /a = 10, all modes with
m ≥ 2 should be FLR stabilized.
Vortex flow stabilization of m = 1: the most successful technique for countering
m = 1 interchange thus far has been to use sheared flows (Cho et al. 2005, 2006) and vortex
stabilization (Sakai, Yasaka & Itatani 1993; Beklemishev et al. 2010; Bagryansky et al.
2011; Yakovlev et al. 2018). Vortex stabilization relies on an edge region rotating around
a stationary central plasma, while sheared flow refers to strong azimuthal flow shear not
necessarily localized to the edge. In both cases, growing instabilities are saturated at small
amplitude by a strong shearing rate. We focus on vortex stabilization here and sheared-flow
stabilization will be mentioned in § 3.2.
The ambipolar potential that maintains quasineutrality between the electron and ion
species in mirrors has long been recognized (Post 1961; Kelley 1967) theoretically
described (Fowler 1981) and experimentally measured (Post 1987). When paired with a
radial temperature gradient, this ambipolar potential naturally leads to positive Er and an
azimuthal E × B flow in the same direction as the ion diamagnetic drift (see § 3.4). This
is, in general, destabilizing for interchange (Severn et al. 1983). With external biasing,
both the HIEI and GDT experiments applied a positive bias to the limiter and edge, and a
negative or grounded potential to the low radius expander rings, producing a negative Er
in the edge and reversing the direction of the E × B drift (Sakai et al. 1993; Bagryansky
et al. 2018). Applying the opposite polarity to reinforce the natural Er was experimentally
challenging.
According to Beklemishev et al. (2010), this experimental technique works if, firstly,
the plasma has sufficient line-tying to the end plates to neutralize the polarization electric
field of the flute mode and ensure closed flow lines, and secondly, if the width of the flow
layer is smaller than the plasma radius. These two conditions ((20) and (22) in their text)
are
(
)(
)3/2
3 2
ρ
L
pi
eφ
∗
p
2
≥ 4Rm
+1
,
(3.8)
Te
a2 Lκ3
pe
(
( )2
)−1/2
a
L κ pi
Rm ≤ 0.7
+1
,
(3.9)
ρ∗
L p pe
√
where φ is the applied bias, ρ∗ ≡ cs /Ωi = mi Te /qe B is a length scale given by the sound
speed and ion cyclotron frequency, Lp the plasma half-length and Lκ is the field curvature
scale length. While having a large mirror ratio Rm is in general good for confinement,
it makes satisfying both of these conditions more difficult. An independent assessment
by the Budker team has estimated that vortex stabilization will likely be sufficient for
WHAM at high fields where Te , B ∼ 1 keV, 0.86 T, while it will likely not be for WHAM
at low fields where Te , B ∼ 0.5 keV, 0.32 T. However, their derivation uses gas dynamic
confinement to model the outflowing ion current and may not apply in the CM regime.

3.2. High-Density Target Formation through ECH Breakdown and Electron
Temperature Control
To ionize the plasma and achieve the high electron temperatures necessary for CM
performance, the WHAM ECH system will use fundamental X-mode heating launched
from the high-field side. Due to its high absorption at low densities, both the GDT
(Yakovlev et al. 2017) and GAMMA-10 (Shidara et al. 2011) experiments used similar
high-field launched X-mode ECH. Each observed that breakdown leads to an initial
low-density, high-energy electron population, which then causes rapid and near complete

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 13

Physics basis for WHAM

13

F IGURE 8. Absorbed ECH power vs plasma density in WHAM-0.32, using a centrally launched
ECH configuration at different electron temperatures, calculated using the GENRAY ray-tracing
code with ion temperature fixed at 10 eV.

ionization of neutral background gas on 1 ms time scales. Rapid ionization is important as
WHAM currently does not have power resources for longer than a 20 ms shot duration.
The GENRAY ray-tracing code from CompX (Smirnov, Harvey & Kupfer 1994)
predicts similar behaviour for ECH in WHAM. After an initial buildup of a low-density
plasma through neutral ionization (the physics of which is not properly captured in ray
tracing), ECH is calculated to be 20 % absorbed even at 2.5 × 1016 m−3 and over 99 %
absorbed above 3 × 1017 m−3 , as shown in figure 8. The electron temperature is also shown
to have a very minor effect on absorption. Thus, there should be no issues with the ECH
coupling to the low-temperature electrons produced though ionization of neutrals.
As ECH breakdown leaves relatively few background neutral particles compared with
a plasma gun discharge, it is less of a drain on the fast ion population through charge
exchange. However, with plasma radius of 0.1 m, WHAM will be a modest experiment
without a clear distinction between the edge and core plasma, and being so small it will
have substantial NBI shine-through. The question of whether a steady-state beam-only
operation can be achieved on WHAM is discussed in § 3.3.
After forming a seed plasma, the second role of the ECH system is to control the radial
electron temperature profile for both the transition to the weakly collisional CM regime
and for Er control. If a gradient in electron temperature is established though ECH, a radial
electric potential gradient will form and interact with the potential defined by the limiter
and bias rings. Both GAMMA-10 and the GDT have successfully used localized ECH to
create sheared flows and internal transport barriers (Cho et al. 2006; Yakovlev et al. 2018).
The WHAM experiment will control the beam direction with a rotatable mirror, which
allows for the ECH beam to be aimed at any radial position, see figure 9. By targeting
the beam at the plasma edge, the electron temperature will increase with radius and give
the desired ambipolar potential profile, assuming that the absorbed power is successfully
transferred to thermal electrons. While the beam diameter in waveguide is roughly 2 cm,
it will spread after exiting the launcher and the extent of control over the deposition profile
is not yet known. The effect of off-axis ECH injection on the radial density profile is also
yet to be seen, but data from GDT suggest that, despite the localized deposition profile

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 14

14

D. Endrizzi and others

(a)
(b)

F IGURE 9. (a) Location and absorption percentage of ECH power vs mirror angle in
WHAM-0.32. (b) The proposed in-vessel ECH beam path including a fixed mirror mounted
on the end of the waveguide run and a second, rotatable mirror mounted on the vessel.

at the ECR surface, the resulting seed plasma will have broad and uniform radial profile.
This means that, in most cases, the launching optics can be tuned for optimal ECH at later
stages of the discharge, without much regard for the initial breakdown stage.

3.3. NBI fuelling at CX dominated energies
An ideal neutral beam heated mirror experiment would begin with a target plasma dense
enough to fully attenuate the neutral beam, and the neutral beam alone would fuel and
heat the plasma. Unfortunately, WHAM, GDT, TAE and all previous mirror experiments
operate in a regime in which charge exchange (CX) collisions (which do not fuel the
plasma) dominate over impact ionization collisions (which do). The challenge is that
at 25 keV for deuterium, the CX cross-section σcx is roughly four times the combined
cross-sections for electron and ion impact ionization, σe+i . We represent this with the
variable χ ≡ σcx /(σcx + σe+i ), shown in figure 10. The consequence is that a 25 keV
neutral deuterium atom is more likely to CX, contributing nothing to the overall density,
but increasing the temperature while pumping out warm plasma.
To better understand these CX and fuelling challenges, NBI fuelling on WHAM
has been studied using FIDASIM. Specifically, we use the python-based pyFIDASIM
routines written by Geiger et al. (2020) to model neutral beam deposition. FIDASIM,
like TRANSP, calculates probabilities of all the atomic processes and uses a Monte Carlo
method to track the fuelling rates of both the incident neutral beam and the reionization
of halo neutrals generated by the CX process. In concert with the FBIS solution particle
confinement time, we use FIDASIM in an iterative scheme to calculate the evolution of the
density profile achieved by NBI fuelling. This assumes some pre-existing ECH produced
target plasma, but does not include additional fuelling that would come from cold neutrals
being ionized at the plasma edge.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 15

Physics basis for WHAM

15

F IGURE 10. Deuterium cross-sections for charge exchange and cumulative impact ionization,
including the resultant 1 − χ. Note that at beam energies of 25, 70 and 120 keV, the fraction of
impact ionization collisions 1 − χ is roughly 20, 50 and 80 %.

This iterative procedure begins with a simple differential equation
n
dn
= Sb − ,
dt
τp

(3.10)

where the density n is the average density along a field line, or equivalently the total
number of particles divided by the flux surface volume N/V(ψ). pyFIDASIM provides the
fuelling source rate Sb ≡ (1/V)dN/dt for each flux surface. The density is then iterated
as
]
[
nt
t+1
t
t
(3.11)
n = n + t S − t .
τp
The FBIS solution gives the steady-state particle confinement time τp∗ , as well as the
analytic result that nτp is constant, so that τpt ≡ τp∗ n∗ /nt and the above equation can be
solved. The results from this technique are plotted in figure 11, which predicts after 10 ms
a density of around 3 × 1019 /m3 with 65 % shine-through. Thus, despite the short path
length and unfavourable χ , WHAM should be able to achieve its target density solely via
neutral beam fuelling on a tenuous background plasma. It will not reach a steady state,
however, as the particle confinement time is much longer than the experiment duration.
Role of CX on fast-ion distribution: since CX processes will dominate over impact
ionization collisions, the ion distribution function is likely to be strongly modified due
to ‘pump out’ across the entire distribution. To reiterate, while CX still increases the total
plasma energy, it does not affect the fuelling. One conclusion from figure 10 is that, for
high efficiency fuelling, a beam energy above 100 keV is required.
Thus far, the FBIS Fokker–Planck solver presumes only losses through the trapped–
passing boundary. In principle, the CX process can be represented by a source term with
the energy and pitch angle of the NBI and an equal loss term that is distributed over the
entire distribution. Accurately including the effects of CX into FBIS requires weighting
the losses by the relative time t̃nbi that particles of a given pitch angle spend in the beam
path, with deeply trapped ions being most likely to be lost.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 16

16

D. Endrizzi and others

F IGURE 11. Density profile evolution including CX losses predicted from pyFIDASIM and
FBIS in an iterative method, for deuterium NBI with primary/secondary fractions of 0.6/0.4.

F IGURE 12. Relative time t̃ spent in the NBI beam path for particles as a function of η, the
bounce-averaged pitch angle variable. Beyond the trapped–passing boundary (red dashed line), t̃
is treated as 0.

For WHAM, the NBI beam path is defined by a region which extends to ±znbi around the
midplane. Particles with turning points inside of ±znbi spend all of their time in the beam
path. For all other particles, the fraction of time spent in the path t̃nbi can be calculated as
∫ znbi
dz/v∥ (z)
t̃nbi (Lbounce ) = ∫ 0Lbounce
.
(3.12)
dz/v∥ (z)
0

The result for WHAM 0.86 is plotted in figure 12.
Properly incorporating this weighting into the analytic FBIS solver for CX losses
requires a modification to the pitch angle eigenfunctions (and loss rate eigenvalues), which
is beyond the scope of this work. As an approximation, we assume the eigenfunctions are
unchanged and allow FBIS to solve for the ion distribution function normally. We then
incrementally remove density proportional to tnbi weightings until the losses through the
trapped–passing boundary equal (1 − χ ) of the injected current. In other words, we treat

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 17

Physics basis for WHAM

17

F IGURE 13. (a) The unmodified ion distribution function in (η, v) space, where η is a
bounce-averaged pitch angle variable (see Egedal et al. 2022). (b) The same distribution after
including pitch angle weighted CX losses for χ = 0.80. (c) The axial density profiles for the
two cases, including the ratio of total particle inventory. (d) The final velocity space distribution
function, showing the reduction in particles with large v⊥ /v∥ . The red dots represent the NBI
injection location, and the red dashed lines the trapped–passing boundaries.

all ionized particles as part of the injected current, but remove CX losses until the current
into the loss cone equals the impact ionization current.
There are several problems with this method. The first is that, if the CX replacement
rep.
CX
time constant τCX ≡ Ntot. /Inbi
, or the time to replace all the confined particles Ntot. via CX
CX
fuelling Inbi is substantially less than the particle confinement time, then the distribution
will be replaced by beam ions faster than it can slow or scatter. This ratio τp /τCX is simply
χ /(1 − χ ), which for χ = 0.8 is 4, so unfortunately larger than one. The second problem
is that FBIS will calculate the scattering as a result of both the CX and impact ionized
populations, when it should only include√the impact ionized part. Ignoring both concerns,
as a simple check we can use the n ∝ I dependence (Egedal
√ et al. 2022) and predict
that the total particle inventory should be reduced roughly as 1 − χ = 0.45 of its initial
value. This is very close to the 0.47 value observed in figure 13, and this approximation
improves at smaller values of χ . The initial and final distribution functions using this
method are plotted in figure 13.
Aside from the lower fuelling efficiency, two features illustrate the importance of
including this effect when evaluating the overall performance of WHAM. First, deeply
trapped particles are most effectively pumped, resulting in a ‘loss wedge’ feature at
v∥2 /v 2 < 1 − B0 /B(znbi ). Second, the distribution function is considerably more sloshing,
with a stronger density enhancement at the turning point. While we expect these results
will be an important feature of the experiment, we emphasize the approximate nature of
these estimates. Furthermore, the FBIS solver is still not configured to model the half and
third energy components of a real neutral beam.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 18

18

D. Endrizzi and others

3.4. Anisotropic MHD Equilibrium and Ambipolar Potential
The modelling of how the vacuum magnetic field is modified for high-β, anisotropic
plasmas with flow is done with an iterative Grad–Shafranov solver. First, the vacuum
flux function ψvac = ψ(r, z) and field B = B(r, z) is calculated from the coil and current
parameters using an internally developed, open-source Green’s function solver named
Pleiades.1 Next, the ion distribution function solution is calculated from the FBIS code,
giving a parallel and perpendicular pressure as a function of the normalized magnetic
field strength B̃ = B/B|z=0 . Extending the 1-D FBIS results to the 2-D domain requires a
radial pressure profile p(ψ̃), where ψ̃ ≡ ψ/ψlim is the flux function normalized to the flux
value at the limiter, and p(ψ̃ > 1) ≡ 0. This radial profile can either be chosen a priori
or a realistic paux profile representing increased cooling of the electrons at the edge can be
specified in FBIS .
The combined 2-D ion pressure profiles of p⊥ (B̃, ψ̃) and p∥ (B̃, ψ̃) are then interpolated
onto the RZ-grid and used to calculate the plasma currents from the diamagnetic (gradient
and curvature) drifts as derived in Appendix A
J⊥ = −

b × ∇p⊥
b×κ
b × r̂
− ( p ∥ − p⊥ )
− nmi ω2 r2
,
B
B
B

(3.13)

where b = B/|B| is the magnetic field unit vector, p is the pressure, B the magnetic field
strength and κ = b · ∇b the magnetic curvature. The last term, which is associated with
plasma rotation, is included here for completeness but is in general small for subsonic
rotation. Although not yet implemented in this code, biased limiters and end rings can be
used to modify both the rotation and centrifugal confinement from the boundary
n(ℓ)
eφ(ℓ, ψ) − eVbias (ψ)
= ln
,
Te
n(0)

(3.14)

where Vbias (ψ) is an applied potential.
The flux ψplas from the current in (3.13) is computed using the Pleiades Green’s function
method and is added to the vacuum magnetic flux solution ψ0 . From the sum ψ0 + ψplas ,
the magnetic field B is recalculated. With the updated field geometry, the pressure profiles
are again mapped to the RZ-grid and the process is repeated. A solution is reached after
the difference between iterations, summed over the entire domain, falls below specified
small threshold. A result for WHAM 0.86 at β = 0.2 with an imposed cos(ψ̃)2 pressure
profile is shown in figure 14. It is worth reiterating here that this axisymmetric solution
remains MHD unstable to perturbations as, unlike the minimum-B configurations of
earlier experiments, axisymmetric mirrors are always MHD unstable, though they may
be stabilized by FLR or sheared-flow effects.
Parallel force balance is controlled by
)
(
( 2 2)
p∥ −p⊥
ωr
b · ∇p⊥ + B · ∇
− nmi b · ∇
= 0,
(3.15)
B
2
where we recognize the second term as the mirror force and the third term as a centrifugal
confining force. The FBIS solution provides parallel force balance self-consistently as a
solution of the drift-kinetic solution that results in local values of p⊥ and p∥ . The resulting
density variation along the magnetic field is then used to compute the electric potential,
1 See https://github.com/eepeterson/pleiades.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 19

Physics basis for WHAM

19

F IGURE 14. Anisotropic equilibrium solution for WHAM at β = 0.2 corresponding to a density
of n = 0.3 × 1020 m−3 and an average ion energy of 10 keV at the midplane. The parallel and
perpendicular pressure profiles at left and the azimuthal plasma current at right. Colour contours
are identical to figure 3.

F IGURE 15. At left, the azimuthal E × B and diamagnetic flow speeds out to the limiter,
showing nearly solid body rotation (vφ ∝ R). Centre, the potential distribution after the
FBIS+Pleiades+pyFIDASIM iterative procedure described in § 3.7. At right, the axial
ambipolar, centrifugal and total potentials along the dashed flux surface.

since the electrons are electrostatically confined for many τee with a nearly Boltzmann
distribution. The centrifugal confining potential, shown on the right of figure 15, is
predicted to be small for NBI-only plasmas with shallow radial Te gradients.

3.5. Non-Classical Confinement
After § 3.1, we have been ignoring other non-ideal effects. In reality, once the problem of
MHD interchange has been solved, other limits may degrade the mirror performance. The
following are softer critical thresholds that generally increase velocity space diffusion,
but are not disruptive like interchange. The two principal kinetic instabilities are the
DCLC and the AIC (Baldwin 1977; Ferron & Wong 1984). A rigorous analysis of these
instabilities would evaluate stability from Particle-in-cell (PIC) or gyrokinetic simulations.
While substantial progress has been made addressing the computational challenges of
high-field mirrors (see Francisquez et al. 2023; Petrov et al. 2023), in the qualitative
analysis that follows, the fast-ion distributions’ outputs from the FBIS solver are used
to assess the severity of each kinetic instability. Drift waves and convective cells can
ruin the assumption that parallel transport losses dominate over radial losses, and these
are addressed below. Fast-ion adiabaticity matters at high energies or low magnetic field
strengths and will be addressed in § 3.6.
DCLC stabilization: the DCLC instability is the result of an ion-Bernstein-like mode
driven by the free energy associated with the non-thermal ambipolar hole coupling to
an electron drift wave associated with the density gradient. Following the work done by

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 20

20

D. Endrizzi and others

F IGURE 16. The change in the midplane ion distribution functions in the region of steep
edge gradients at Ψ = 0.5Ψlim. without (left) and with (right) the centrifugal effects. Note the
difference in the dashed pink line representing the loss cone at the midplane.

Kotelnikov, Chernoshtanov & Prikhodko (2017), DCLC is stabilized if the radial density
gradient scale length Lr ≡ n/∇n is much larger than the ion Larmor radius ρi . When Lr
is approximately the plasma radius a, then Nρ ≡ a/ρi must exceed approximately 100 for
stability (Ferron & Wong 1984), while in WHAM Nρ will be 3 or 4. An astute reader
may observe the apparent contradiction between FLR stabilization (which benefits from
small Nρ ), and DCLC (which is stabilized by large Nρ ). As a preventative strategy, one
could produce a pressure profile with a flat core and a steep edge: DCLC will be stable
in the core where the pressure gradient drive is zero, and in the edge the strong vortex
flow shear will saturate DCLC at small amplitudes. As noted in (Ferron & Wong 1984),
this localization of the DCLC will limit its effects to regions of strong gradients and also
saturate at manageable levels.
A different strategy involves the addition of low energy ions into the ambipolar hole,
which inhibits DCLC by reducing the positive gradient in the distribution function.
Kotelnikov provides a quantitative threshold
( )3/2
nc
μ
α≡
⪆ 4.22
,
nh
Nρ

(3.16)

where μ is the ion atomic mass number, and α represents the fraction of cold to hot ions.
In past experiments, nc has been introduced by cold plasma streams or by trapping in the
Yushmanov potential associated with sloshing ions (Yushmanov 1966; Kesner 1973). The
GDT, for example, is likely stabilized by the cold target plasma at first and then later by the
sloshing ions. When evaluated at values expected for WHAM, this constraint unfortunately
demands a cold ion population comparable with the fast-ion population.
A new mechanism for maintaining DCLC stability uses the centrifugal potential
associated with plasma rotation to trap low-energy ions. As described earlier, the radial
electron temperature profile and the axial ambipolar potential together produce an E × B
flow and consequently a centrifugal confining potential φcent shown in figure 15. To
enhance this potential, we assume a strong but realistic radial electron temperature gradient
of Te /ρi ∼ 300 eV cm−1 has been made in the edge with off-axis ECH. This potential
has been included self-consistently into the FBIS solution of the distribution function,
and the result is shown in figure 16. With this substantial radial potential gradient, the
combination of the trapping potential between fast-ion turning points and the centrifugal
potential increases the population of ‘cold’ ions by 4 %. This may not be sufficient in the
small Nρ of WHAM but could likely play a role in a larger next step device.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 21

Physics basis for WHAM

21

AIC stabilization: we can similarly make predictions of the degree of AIC instability
from FBIS distribution functions. The AIC is driven by the ion temperature anisotropy and
depends on the plasma β in a way similar to mirror and firehose instabilities. An absolute
instability threshold was identified by Smith (1984)
(
β⊥

T⊥
T∥

)2
> 3.5.

(3.17)

However, the threshold for convective instability can be much lower: GAMMA-10
observed AIC when β⊥ (T⊥ T∥ )2 exceeded only 0.3 (Katsumata et al. 1996). For
comparison, in the high β = 0.2 case of figure 14 this parameter approaches 0.4 at the
turning points. At present, we do not have a good estimate for the precise value of AIC
onset in WHAM, although this comparison indicates it will not be a problem until WHAM
exceeds the performance prediction of § 3.7.
We conclude our discussion of kinetic instabilities by noting that the GDT device has
seen no evidence of either DCLC and minimal evidence of AIC (Ivanov & Prikhodko
2013), and that our discussion here may be too pessimistic. Its likely that sloshing ion
distributions may have negligible kinetic instabilities (Post & Ryutov 1995). Regardless,
without a fully kinetic simulation test, understanding the extent of kinetic instabilities will
be left to the experiment.
Cross-field transport: drift waves, trapped particle modes, convective cells: the basic
assumption of the CM scaling is that parallel transport dominates over perpendicular
transport and that energy is lost via particle losses, i.e. the Lawson parameter nτ is set by
the particle confinement time τp . In addition to the kinetic instabilities described above, the
presence of traditional drift waves could mix plasma radially via turbulence, and thereby
allow energy to diffuse outward, just as in toroidal systems (including trapped electron
modes, electron temperature gradient modes and ion temperature gradient modes). The
lack of toroidal curvature removes an important driver of these modes from mirrors
(Simonen et al. 2008). Much less work has been carried out to evaluate which instabilities
(if any) will grow and be most problematic, but numerous authors have speculated that
trapped electron modes may be present in the long central cells of tandem mirrors (Horton
et al. 2010; Fowler, Moir & Simonen 2017). Radial transport associated with neoclassical
transport was inferred in TMX-U, trapped particle modes were observed in Tara and
convective cells measured directly in GAMMA-10. In a remarkable set of follow-on
papers, GAMMA-10 went on to document how sheared flow created by the natural
ambipolar potential fully stabilized these convective modes and restored the tandem to
having purely axially losses (Cho et al. 2005, 2006).
Beneficially, fast-ion FLR effects may mitigate turbulence as well as interchange
modes by averaging over small fluctuations (k⊥ ρ ≫ 1). An absence of turbulence was
observed by TAE that was attributed to fast ions(Schmitz et al. 2016). In tokamaks as
well, experimental measurements on the Tokamak Fusion Test Reactor (TFTR) show
that α-particles exhibit classical diffusion due to the FLR effect (Zweben et al. 1997).
Mirrors tend to optimize with Ti /Te ≫ 1 and this is known to stabilize ion temperature
gradient (ITG) driven turbulence in toroidal devices, e.g. TFTR supershots. On the other
hand, Ti /Te > 1 is known to destabilize electron temperature gradient (ETG) modes.
Sheared flow associated with differential rotation long wavelength streamer-like ion-scale
turbulence such as ITG and TEMs. Electron-scale ETG may not benefit from this effect
depending on the radial correlation lengths. Further evaluation of these instabilities is
warranted.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 22

22

D. Endrizzi and others

F IGURE 17. Numerical calculation of the adiabaticity parameter α ≡ LB /ρ∥ in velocity space
for the two WHAM configurations. Speeds are normalized to the 25 keV deuterium injection
energy, with the red dot locating the expected injected velocity.

3.6. Fast-Ion Adiabaticity
Non-adiabatic effects are always present as finite jumps μ in the magnetic moment
as trapped particles pass through the field minima (Hastie, Hobbs & Taylor 1969). As
discussed by Cohen, Rowlands & Foote (1978b), fast-ion adiabaticity is often a more
restrictive condition on β than the onset of the mirror mode. Conservation of the first
adiabatic invariant μ = mv⊥2 /2B fails if a particle experiences a large change in magnetic
field strength in one gyro-period. This is represented by the adiabaticity parameter α ≡
LB /ρ∥ , where ρ∥ ≡ v∥ /ωci and LB ≡ |B|/|∇B|, where large α means the magnetic field
gradient scale length is larger than the parallel distance travelled in one gyroperiod. The
size of the jumps scales as μ ∝ e−α (Cohen et al. 1978b). In general, particles are
well confined only if α ≫ 1, and we find non-adiabatic effects become significant when
α ≤ 10.
In WHAM, this adiabaticity condition is not satisfied everywhere. Figure 17 shows α
for the two magnetic configurations. In WHAM at low field (0.3 T), NBI deuterons are
born with α ≃ 10 and experience appreciable changes in μ each bounce. In contrast, for
the 0.8 T high-field case, α is much larger than 10 all the way to the loss cone. In short,
non-adiabatic effects may be present in WHAM at low field but are not expected at high
field.
To more carefully explore when adiabaticity fails in our specific geometries, we
implemented a standard Buneman–Boris algorithm for computing single particle
trajectories. As this algorithm is known to not conserve energy, simulations are run with
enough temporal resolution to keep the cumulative error in energy below 0.1 %. To model
fast-ion slowing behaviour without pitch angle scattering (the cold Te case), an electron
drag term is added so that at each timestep a scalar factor exp(−dt/τs ) is multiplied to the
particle velocity vector. This technique is appropriate in the limit that one bounce time is
less than the ion slowing down time, which is less than the ion pitch angle scattering time,
i.e. τb ≪ τs ≪ τi .
To understand some of the behaviour observed, we use conventions from early mirror
work to note that fast ions in WHAM will be ‘superadiabatic’, meaning that the gyrophase
angle at the midplane is well correlated between bounces (Cohen et al. 1978a). This is
largely due to the small ratio of bounce period to bounce-averaged gyroperiod, τb /τci ≤ 10
(Cohen et al. 1978a). In contrast, for longer or more collisional experiments, the gyrophase

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 23

Physics basis for WHAM

23

F IGURE 18. Numerical calculation of the ratio of bounce period to bounce-averaged gyroperiod
across velocity space. The pink line tracks the particles at each bounce as they slow over 1 ms
with τs = 2 ms.

is essentially random from bounce to bounce. Because of this, WHAM may encounter
gyro-bounce resonance effects. At low field in WHAM, the bounce period for 25 keV D
ions injected at 45◦ is six times the mean gyroperiod, allowing for a 6 : 1 resonance.
Figure 18 shows numerical calculations of the gyro-bounce ratio of injected NBI
deuterons into WHAM at 0.32 T and 0.86 T. For the high-field case, the particle slows
along the red line while preserving its initial pitch angle, as expected. In contrast, the
low field case shows the particle tracking the 6 : 1 gyro-bounce resonant surface. We
call these ‘resonant superadiabatic’ particles, as this resonance between bounce and
gyrofrequency can shift the pitch angle of the ion. The resonant condition breaks when
the bounce-to-bounce fluctuations in magnetic moment μ (which are proportional to α,
shown in figure 17) can no longer compensate for the decrease in μ due to the slowing.
This effect might be measured in a less peaked fusion proton axial intensity profile as
fast-ions are deflected towards larger v⊥ /v∥ .

3.7. Performance Predictions
The FBIS code can be combined with the methods in §§ 3.3 and 3.4 to produce
an upper-limit classical prediction for WHAM performance, with results displayed in
figure 19. The inputs to the model are shown in the top panel, with the mirror-ratio
profile calculated from the vacuum magnetic field, and an arbitrary auxiliary power profile
representing strong electron cooling at the edge. With that magnetic geometry and cooling
profile, results from the FBIS code are interpolated to each flux surface. pyFIDASIM
next calculates the deposition rate given an initial density profile, and uses the FBIS
particle confinement time to calculate the steady-state density. After this, the magnetic
equilibrium is recalculated using this new pressure profile and the process is iterated.
Finally, the bottom panel of figure 19 predicts the upper-limit Deuterium-Deuterium (DD)
fusion neutron rate for this configuration of 6 × 1013 s−1 .
As FBIS calculates the equilibrium solution, it does not provide information on the time
to reach this equilibrium state other than the particle confinement time. We know that, for
large χ > 0.5, CX will dominate over the fuelling and this method will not be accurate. It
will be more useful in calculating a next step experiment with high-energy neutral beams.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 24

24

D. Endrizzi and others

F IGURE 19. The FBIS, Pleides and pyFidasim performance predictions. Assumptions and
results for WHAM with B0 = 0.86 T, with 1 MW of 25 keV NBI onto an ECH target plasma.

3.7.1. CQL3D-mirror Results
In addition to not modelling temporal behaviour, the FBIS code also does not include
a model for the high-harmonic ion cyclotron heating. CQL3D-m (Harvey et al. 2016),
a special version of CQL3D (see Harvey & McCoy 1992) for mirror geometry, is
a bounce-averaged Fokker–Planck solver that, like FBIS, includes a self-consistent
calculation of E∥ (Petrov et al. 2023), but does not yet include the potential drop in
the expanders outside the mirror. Rather, a simple potential sheath drop to maintain
ambipolar losses is used. It has been used here to model a combined neutral beam and
second harmonic RF heating scenario, including subtleties like the half and third energy
components of the neutral beams. While the details of the implementation will be given

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 25

Physics basis for WHAM

25

F IGURE 20. CQL3D-m uses NFREYA to model NBI fuelling and GENRAY-C to track ray
trajectories. For clarity, only one ray is shown here, with reduced number of bounces. Labelled
are the first through fourth ion cyclotron harmonics.

in a subsequent publication, initial benchmarking has shown good agreement between the
semi-analytic FBIS and CQL3D-m for NBI only, predicting similar ion confinement times
and parallel electrostatic potential drops. CQL3D-m also has implemented an advanced
energy-dependent cross-section for CX such that the low-energy ions are pumped out of
plasma by CX with injected neutrals, while very fast ions (that are accelerated by RF above
injection energy) are less likely to CX with the neutrals. This is separate but similar to the
spatially dependent effect detailed in § 3.3. Important features of the simulation, including
the NBI deposition from NFREYA and ray tracing from GENRAY, are shown in figure 20
Preliminary simulations were initialized with a flat density profile at 6 × 1019 m−3 , and a
nominal 100 kW each of NBI and RF heating. The runs evolve with NBI fuelling balancing
the particles lost through the mirror loss cone and due to CX, resulting in a final density
of 2 × 1019 m−3 . The temporal evolution of the absorbed power, plasma β and DD fusion
neutron rate is shown in figure 21. Only a small fraction of the injected neutral beam
is captured, and the fast wave is mostly absorbed by Landau damping and transit time
magnetic pumping on the electrons, with only 10 %–20 % deposited into the fast-ions
(mostly at second harmonic resonance), although the RF power partition is gradually
shifting towards ions. As the accelerated fast-ions have long confinement times, vastly
reduced NBI and RF powers compared with experiment values help prevent the simulation
from rapidly becoming unrealistic. Indeed, by 200 ms, the plasma has already reached
β = 0.5.
As the second harmonic resonance condition is collocated with the turning points of
the 45◦ injected NBI ions, the RF preferentially increases the energy of the sloshing ion
distribution. The sloshing ions provide a confining potential in the central region, visible in
the axial plot of figure 22. The resultant midplane ion distribution functions are shown in
figure 23, demonstrating substantial diffusion to high energies at the 45◦ pitch angle of the
injected neutral beams, and the notable lack of an ambipolar hole. These electrostatically
trapped ions reduce the severity of the DCLC instability, although to what extent will be
addressed in future work.
These very promising initial results show that β = 0.5 can be reached in approximately
200 ms, but that further evolution would continue to even higher densities and pressures. It
should be noted that in these simulations the gyro-radius cutoff was implemented to reduce
the growth of high-energy tails, however, the effective ion temperature is still increasing
because of the tails getting wider (more populated). This suggests in an experiment that
the power might be feedback controlled and lowered to not exceed an effective β limit.
Unlike the combined results at the beginning of § 3.7, these results do not yet include the
diamagnetic modification to the equilibrium that will increase the mirror ratio and lead

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 26

26

D. Endrizzi and others

F IGURE 21. Time-dependent simulation of absorbed RF and NBI power, and DD neutron
yield. Central β corresponds to the right-hand axis. Note the magnetic equilibrium uses only
the vacuum field and is not self-consistently calculated, and so only results for small beta are
reasonable.

F IGURE 22. A snapshot of the spatial profiles from the CQL3D-m simulation at 200 ms. Radial
profiles (left) are taken at the midplane. Axial profiles (right) are shown for flux surface with
ρ/a = 0.17. In the right panel plot z/zmax = 0 corresponds to the midplane, while z/zmax = 1.0
is at the mirror coil position.

to even better confinement. Furthermore, the ray-tracing approximations may not be quite
valid as the rays fill up the plasma volume with no interference effects included. However,
by using the initial azimuthal spectrum, we were able to obtain reasonably wide profiles
of power deposition. A next step will be to use a full-wave code like AORSA3D (special
version for cylinder geometry) to couple to the Fokker–Planck solver and investigate if this
approximation is reasonable. Other next steps include modelling the electron cyclotron
resonance heating, including the role of CX halo particles and edge effects.

3.8. Concluding Remarks
MHD stability is paramount: forming a stable plasma is critical for assessing confinement
and establishing a platform for testing the viability of alternative stabilization concepts
like feedback or mantel line-tying. Stable plasmas will be a prerequisite for a number of
additional goals, such as demonstrating the HHFW acceleration of fast ions, and the direct

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 27

Physics basis for WHAM
(a)

(b)

(c)

(d)

27

F IGURE 23. Ion (a,b) and electron (c,d) distribution functions from a CQL3D-m simulation
after 20 ms (a,c) and 200 ms (b,d). Distributions are shown at ρ = 0, z = 0 midplane point.
Dashed black lines correspond to trapped–passing boundaries in the absence of the axial electric
potential, for reference. The solid black lines include the effect of φ(z). Note that the confining
region in the ion distribution formed by an increasing population of sloshing ions grows in time.
The fast ion birth energy 25 keV is at the top of the green region in fD (u∥ , u⊥ ) plots, at u/c ∼
0.005.

energy conversion of real exhaust distributions. Unfortunately, using biased limiters for
m = 1 stability in WHAM (duplicating the GDT method in the CM regime) does not fully
retire the MHD stability risk for a next step device when plasma confinement improves
even further. While the physics principle of sheared-flow stabilization has already been
shown to work experimentally, implementing it in the next step may require a different
set of techniques or actuators appropriate to larger, better confined plasmas. Because of
its increased size, such a device will have access to additional stabilization strategies
appropriate for a reactor grade plasma including: using a low-temperature mantel plasma
with good electrical connectivity to the ends to assist line-tying; the use of close fitting
shells theoretically expected to stabilize/ larger plasmas at high β; saddle feedback
stabilization or tail wagging; more precise control of Te and Er profiles, using steerable
ECH deposition as an actuator.
Scientific validation of the fast-ion confinement against models is not trivial: simply
measuring the total ion content and dividing by the neutral beam injection current is
not particularly informative because of the strong role that CX plays in the neutral
beam deposition and losses. Measurements of the ion distribution function with nuclear
product diagnostics, fast-ion D-α emission and CX neutrals will focus on observing
these effects. For these reasons, benchmarking WHAM results against hybrid-PIC
calculations and gyrofluid calculations that can include CX effects is essential. Validating
a CQL3D-mirror, FBIS, FIDASIM model will also require very careful measurements of
beam shine-through in order to accurately assess confinement.
In summary, the WHAM device is a prototype for a future Q ∼ 1 class simple
axisymmetric mirror. It will operate in the low collisionality ‘classical mirror’ limit in
which ion pitch angle scattering dominates over electron slowing. We have presented

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 28

28

D. Endrizzi and others

initial modelling predictions for the WHAM experiment that couples fast-ion modelling
from the FBIS package with anisotropic MHD equilibria from Pleiades and beam-ion
fuelling from pyFIDASIM to predict the upper limits of instability-free performance. We
have also included results from CQL3D-m showing the efficacy of second harmonic ICRF
heating.
Acknowledgements

For transparency of interests, the authors would like to state that J.K.A., C.B.F. and O.S.
are cofounders of Realta Fusion. The authors would like to thank P. Catto for their help
with the anisotropic equilibrium equations in Appendix A. The authors would also like to
thank D. Ryutov for their helpful comments during the review process.
Editor Per Helander thanks the referees for their advice in evaluating this article.
Declaration of interest

The authors report no conflict of interest.
Funding

The information, data or work presented herein was funded in part by the Advanced
Research Projects Agency-Energy (ARPA-E), U.S. Department of Energy under Award
Numbers DE-AR0001258, DE-AR0001261, and U.S. Department of Energy under Award
Number DE-FG02-ER54744. The views and opinions of authors expressed herein do not
necessarily state or reflect those of the United States Government or any agency thereof.
Appendix A. Equations for Anisotropic Equilibrium

For an anisotropic, low flow plasma in a magnetic field B = Bb, MHD pressure balance
J × B = ∇ · P can be rewritten
J × B = ∇ · [p∥ bb + p⊥ (1 − bb)]
]
[
B
= ∇ · p ⊥ 1 + ( p ∥ − p⊥ ) b
B
[
]
p∥ − p ⊥
b
= ∇p⊥ + B · ∇
B

)
p∥ − p⊥
= ∇p⊥ + ( p∥ − p⊥ )b · ∇b + bB · ∇
.
B
(

The parallel component of the right-hand side is
)
(
p ∥ − p⊥
= 0,
b · ∇p⊥ + B · ∇
B

(A1)

(A2)

while the perpendicular current density J ⊥ is
J⊥ =

B
× [∇p⊥ + ( p∥ − p⊥ )b · ∇b].
B2

(A3)

Using the following property of vector calculus:
(1 − bb) · ∇ × b = b × [(∇ × b) × b] = b × (b · ∇b),

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

(A4)

## PDF page 29

Physics basis for WHAM

29

and also this
1 − bb
· (∇ × B − ∇B × b)
B
μ0 J ⊥ b × ∇B
+
,
=
B
B

(1 − bb) · ∇ × b =

(A5)

both can be combined into
b × (b · ∇b) =

μ0 J ⊥ b × ∇B
+
.
B
B

As a result, J ⊥ can be rewritten as
[
[
]
]
μ0 ( p⊥ −p∥ )
B
∇B
( p∥ − p ⊥ ) .
J ⊥ = 2 × ∇p⊥ +
σ J ⊥≡ 1 +
B2
B
B

(A6)

(A7)

The perpendicular current density has ∇p⊥ and ∇B components. If you know p⊥ =
p⊥ (ψ, B), with the flux function ψ satisfying B · ∇ψ = 0, then J ⊥ can be written as
[
]
∂p⊥
∇B
B
∂p⊥
σJ⊥ = 2 ×
∇ψ +
∇B +
( p∥ − p⊥ ) ,
(A8)
B
∂ψ
∂B
B
which has separable ∇ψ and ∇B components
[
]
1 ∂p⊥ p∥ − p⊥
+
b · ∇B × ∇ψ,
σ J ⊥ · ∇ψ =
B ∂B
B
1 ∂p⊥
σ J ⊥ · ∇B =
b · ∇ψ × ∇B.
B ∂ψ
If you also know that p∥ = p∥ (ψ, B), then parallel pressure balance gives
[
]
∂ ( p∥ − p⊥ )
∂p∥ p∥ − p⊥
∂p⊥
+B
=0=
−
.
∂B
∂B
B
∂B
B

(A9)
(A10)

(A11)

The current, of course, ∇ · J = 0 with J = J ⊥ + J∥ b.

A.1. Rotation effects
To add the effects of E × B rotation into the MHD equilibrium, we assume axisymmetry
to allow the flow to be sonic. Sonic rotation adds a term to the right side of the MHD
pressure balance equation of the form ∇ · (mi ni vv) = ρi v · ∇v, with ni the ion density, mi
the ion mass, ρi the mass density and v the ion flow velocity. Using cylindrical r, θ , z,
coordinates and writing the magnetic field as
B = ∇ψ(r, θ ) × ∇θ =

1 ∂ψ
1 ∂ψ
∇z −
∇r,
r ∂r
r ∂z

(A12)

then the ion flow velocity is
v = ω(ψ, ℓ)r2 ∇θ.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

(A13)

## PDF page 30

30

D. Endrizzi and others

We now assume the rotation is a result of an electrostatic field
∂Φ(ψ, ℓ)
∂Φ(ψ, ℓ)
∇ψ −
b,
∂ψ
∂ℓ

(A14)

E ⊥ = −v × B = −ωr2 ∇θ × (∇ψ × ∇θ ) = −ω∇ψ,

(A15)

E = −∇Φ(ψ, ℓ) = −
where b ≡ B/|B|, thus

and the angular velocity becomes
ω=

∂Φ(ψ, ℓ)
.
∂ψ

(A16)

We note here that a ideal and resistive MHD do not hold since E∥ = −(Te /en)b · ∇n
Let us expand the v · ∇v term
v · ∇v = ω2 r2 ∇θ · ∇(r2 ∇θ )
= ω2 r3 ∇θ · [(∇r)(∇θ ) − (∇θ )(∇r)] = −ω2 r∇r.

(A17)

Now separate the rotation term into its parallel component
ρi ω 2 r
ρi v · ∇v · b = −
B · ∇r =
B

(

ρi ω 2
B

)(

∂ψ
∂z

)
,

(A18)

and its perpendicular component
b × [(ρi v · ∇v) × b] = −ρi ω2 r(1 − bb) · ∇r.

(A19)

Using the new term, parallel force balance becomes
[

( 2 2)
]
p∥ − p ⊥
ωr
2
= ρi ω rb · ∇r = ρi b · ∇
.
b · ∇p⊥ + B · ∇
B
2

(A20)

Substituting the new term in the expression for perpendicular current
ρi ω 2 r
B
× (ρi v · ∇v) = − 2 B × ∇r
2
B
B
(
)
ρi ω2 r ∂ψ
∇θ,
=− 2
B
∂r

(A21)

so that the perpendicular current becomes
J⊥ =

B
× [∇p⊥ + ( p∥ − p⊥ )b · ∇b − ρi ω2 r∇r].
B2

(A22)

Again using (A6)
b × (b · ∇b) =

μ0 J ⊥ b × ∇B
+
,
B
B

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

(A23)

## PDF page 31

Physics basis for WHAM

31

and substituting
[
]
μ0
σ J ⊥ ≡ 1 + 2 ( p⊥ −p∥ ) J ⊥
B
[
]
B
p∥ − p ⊥
∇B − ρi ω2 r∇r .
= 2 × ∇p⊥ +
B
B

(A24)

Using axisymmetry this becomes
σJ⊥ =

[
]
∇θ ∇ψ
p∥ − p⊥
2
∇B
−
ρ
·
∇p
+
ω
r∇r
.
⊥
i
B2
B

(A25)

Notice that because of axisymmetry, if p⊥ = p⊥ (ψ, B), then σ J ⊥ · ∇ψ = 0 = σ J ⊥ · ∇B.
Appendix B. Charge Exchange in Fast Beam-Ion Solver

At the NBI energy of Enbi = 25 keV, the CX cross-section is substantially larger than
the sum of the ion and electron impact ionization collisions. We parameterize this as χ ≡
σcx /(σcx + σi/e ), where at 25 keV χ ≃ 0.8. For each ion deposited by electron/ion impact
ionization, χ /(1 − χ ) ions are removed from elsewhere in the distribution function and
redeposited by charge exchange at the injection energy and pitch angle. (59) of Egedal
et al. (2022) can be rewritten as
[
]
1 ∂
vc3 g̃2 ∂fj
vc3 g̃1
3
3
−βλj 3 fj + 2
(v + vc h̃)fj +
v
v ∂v
2 ∂v
δ(v − v0 )
.
(B1)
−Cwj fj = −τs Sj
v2
The final term on the left-hand side reflects CX losses and is proportional to the
distribution function weighted by the normalized axial dependence of each eigenfunctions’
‘residence time’ within the NBI beam path. To solve for the constant C, we reason that the
sum over j of the integral of this term must add up to χ times the total number of injected
particles
∫
∑
∑ ∫
δ(v − v0 )
2
wj 4πv dv
dηfj = χ
τs Sj
.
(B2)
C
v2
j
j
The right-hand side can be rewritten
χ τs

∑
j

Sj

δ(v − v0 )
dN
I/e
= χ τs S0 = χ τs
= χ τs
.
2
v
dx dt
V

(B3)

The left-hand side can be integrated up into a weighted density n∗ and then using
τcx ≡

n∗ V
,
I/e

our constant C becomes

(B4)

τs
.
(B5)
τcx
This is calculated numerically in two steps: first solving the equation with the case where
τcx = τs , and then solving again once τcx is known. We use
C=χ

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 32

32

D. Endrizzi and others
∫
∫ 1
2
N = V 4πv dv
f (v, η) dη.

(B6)

0

It is worth noting that the effect here is precisely the concept conceived of to pump
out ions in thermal barrier plasmas (Carlson et al. 1981) that rely upon a sloshing ion
distribution and prevent buildup of plasma in the Yushmanov potential (Yushmanov 1966;
Kesner 1973) by pumping out the weakly confined particles.
REFERENCES

BAGRYANSKY, P.A., A NIKEEV, A.V., B EKLEMISHEV, A.D., D ONIN , A.S., I VANOV, A.A.,
KORZHAVINA , M.S., KOVALENKO , Y.V., K RUGLYAKOV, E.P., L IZUNOV, A.A., M AXIMOV,
V.V., M URAKHTIN , S.V., P RIKHODKO , V.V., P INZHENIN , E.I., P USHKAREVA , A.N., SAVKIN ,
V.Y. & Z AYTSEV, K.V. 2011 Confinement of hot ion plasma with β ≤ 0.6 in the gas dynamic trap.
Fusion Sci. Technol. 59 (1T), 31–35.
BAGRYANSKY, P.A., B EKLEMISHEV, A.D. & P OSTUPAEV, V.V. 2018 Encouraging results and new ideas
for fusion in linear traps. J. Fusion Energy 38 (1), 162–181.
BAGRYANSKY, P.A., S HALASHOV, A.G., G OSPODCHIKOV, E.D., L IZUNOV, A.A., M AXIMOV, V.V.,
P RIKHODKO , V.V., S OLDATKINA , E.I., S OLOMAKHIN , A.L. & YAKOVLEV, D.V. 2015 Threefold
increase of the bulk electron temperature of plasma discharges in a magnetic mirror device. Phys.
Rev. Lett. 114 (20), 205001.
BALDWIN , D.E. 1977 End-loss processes from mirror machines. Rev. Mod. Phys. 49 (2), 317–339.
BARR , W.L., M OIR , R.W. & H AMILTON , G.W. 1982 Experimental results from a beam direct converter
at 100 kV. J. Fusion Energy 2 (2), 131–143.
B E ’ ERY, I. & S EEMANN , O. 2015 Feedback effect on flute dynamics in a mirror machine. Plasma Phys.
Control. Fusion 57 (8), 085005.
B E ’ ERY, I., S EEMANN , O. & F ISHER , A. 2014 Active feedback stabilization of multimode flute instability
in a mirror trap. Plasma Phys. Control. Fusion 56 (7), 075002.
B EKLEMISHEV, A.D. 2016 Diamagnetic ‘bubble’ equilibria in linear traps. Phys. Plasmas 23 (8), 082506.
B EKLEMISHEV, A.D. 2017 Tail-waving system for active feedback stabilization of flute modes in open
traps. Fusion Sci. Technol. 59 (1T), 90–93.
B EKLEMISHEV, A.D., BAGRYANSKY, P.A., C HASCHIN , M.S. & S OLDATKINA , E.I. 2010 Vortex
confinement of plasmas in symmetric mirror traps. Fusion Sci. Technol. 57 (4), 351–360.
B ING , G.F. & ROBERTS , J.E. 1961 End-losses from mirror machines. Phys. Fluids 4 (8), 1039.
BOLDYREV, S., F OREST, C. & E GEDAL , J. 2020 Electron temperature of the solar wind. Proc. Natl Acad.
Sci. USA 117 (17).
C ARLSON , G.A., et al. 1981 Tandem mirror reactor with thermal barriers. Nucl. Engng Des. 63 (2),
233–250.
C HO , T., et al. 2005 Recent progress in the GAMMA 10 tandem mirror. Fusion Sci. Technol. 47 (1T), 9–16.
C HO , T., et al. 2006 Observation and control of transverse energy-transport barrier due to the formation of
an energetic-electron layer with sheared e × b flow. Phys. Rev. Lett. 97, 055001.
C OENSGEN , F.H., C UMMINS , W.F., L OGAN , B.G., M OLVIK , A.W., N EXSEN , W.E., S IMONEN ,
T.C., S TALLARD , B.W. & T URNER , W.C. 1975 Stabilization of a neutral-beam – sustained,
mirror-confined plasma. Phys. Rev. Lett. 35 (22), 1501–1503.
C OHEN , R.H., R ENSINK , M., C UTLER , T.A. & M IRIN , A.A. 1978a Collisional loss of electrostatically
confined species in a magnetic mirror. Nucl. Fusion 18, 1229.
C OHEN , R.H., ROWLANDS , G. & F OOTE , J.H. 1978b Nonadiabaticity in mirror machines. Phys. Fluids
21 (4), 627.
E GEDAL , J., E NDRIZZI , D., F OREST, C.B. & F OWLER , T.K. 2022 Fusion by beam ions in a low
collisionality, high mirror ratio magnetic mirror. Nucl. Fusion 62 (12), 126053.
F ERRON , J.R., G OULDING , R., N ELSON , B.A., I NTRATOR , T., WANG , E.Y., S EVERN , G.,
H ERSHKOWITZ , N., B ROUCHOUS , D., P EW, J., B REUN , R.A. & M AJESKI , R. 1987 Electrostatic
end plugging accompanied by a central-cell density increase in an axisymmetric tandem mirror.
Phys. Fluids 30 (9), 2855–2869.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 33

Physics basis for WHAM

33

F ERRON , J.R. & WONG , A.Y. 1984 The dependence of the drift cyclotron loss cone instability on the
radial density gradient. Phys. Fluids 27 (5), 1287.
F ERRON , J.R., WONG , A.Y., D IMONTE , G. & L EIKIND , B.J. 1983 Interchange stability of an
axisymmetric, average minimum-b magnetic mirror. Phys. Fluids 26 (8), 2227–2233.
F OWLER , T.K. 1981 Mirror theory. In Fusion, vol. 1, chap. 6, pp. 291–356. Academic Press.
F OWLER , T.K., M OIR , R.W. & S IMONEN , T.C. 2017 A new simpler way to obtain high fusion power gain
in tandem mirrors. Nucl. Fusion 57 (5), 056014.
F OWLER , T.K. & R ANKIN , M. 1962 Plasma potential and energy distributions in high-energy injection
machines. J. Nucl. Energy. C, Plasma Phys. Accel. Thermonucl. Res. 4 (5), 311–320.
F OWLER , T.K. & R ANKIN , M. 1966 Fusion energy balance in mirror machines. J. Nucl. Energy. C, Plasma
Phys. Accel. Thermonucl. Res. 8 (2), 121–128.
F RANCISQUEZ , M., ROSEN , M.H., M ANDELL , N.R., H AKIM , A., F OREST, C.B. & H AMMETT, G.W.
2023 Towards continuum gyrokinetic study of high-field mirrors. arXiv:2305.06372.
G EIGER , B., S TAGNER , L., H EIDBRINK , W.W., D UX , R., F ISCHER , R., F UJIWARA , Y., GARCIA ,
A.V., JACOBSEN , A.S., VAN V UUREN , A.J., K ARPUSHOV, A.N., L IU, D., S CHNEIDER , P.A.,
S FILIGOI , I., P OLOSKEI , P.Z. & W EILAND , M. 2020 Progress in modelling fast-ion d-alpha
spectra and neutral particle analyzer fluxes using fidasim. Plasma Phys. Control. Fusion 62 (10),
105008.
G REEN , D.L., B ERRY, L.A., S IMPSON , A.B. & YOUNKIN , T.R. 2018 Kinetic-j: a computational kernel
for solving the linearized vlasov equation applied to calculations of the kinetic, configuration space
plasma current for time harmonic wave electric fields. Comput. Phys. Commun. 225, 122–127.
H ARVEY, R.W. & M C C OY, M.G. 1992 The CQL3D code. In Proceedings of the IAEA TCM on Advances
in Simulation and Modeling of Thermonuclear Plasmas pp. 489–526 (see also CQL3D manual, with
corrections https://www.compxco.com/cql3d_manual.pdf).
H ARVEY, R.W., P ETROV, Y.V. & F OREST, C.B. 2016 3D distributions resulting from neutral beam,
ICRF and EC heating in an axisymmetric mirror. In AIP Conference Proceedings 1771, p. 040002.
https://doi.org/10.1063/1.4964187
H ASTIE , R.J., H OBBS , G.D. & TAYLOR , J.B. 1969 Non-adiabatic behavior of particles in inhomogeneous
magnetic fields. In Plasma Physics and Controlled Nuclear Fusion Research, vol. 1. IAEA.
H ORTON , W., F U, X.R., I VANOV, A. & B EKLEMISHEV, A. 2010 Parameter optimization studies for a
tandem mirror neutron source. J. Fusion Energy 29 (6), 521–526.
I ALOVEGA , M., et al. 2023 Initial study on thermal stability of cold spray tantalum coating irradiated with
deuterium. Phys. Scr. (in review).
I VANOV, A.A. & P RIKHODKO , V.V. 2013 Gas-dynamic trap: an overview of the concept and experimental
results. Plasma Phys. Control. Fusion 55 (6), 063001–32.
JAEGER , E.F., B ERRY, L.A., D’A ZEVEDO , E., BATCHELOR , D.B. & C ARTER , M.D. 2001 All-orders
spectral calculation of radio-frequency heating in two-dimensional toroidal plasmas. Phys. Plasmas
8 (5), 1573–1583.
K ATSUMATA , R., I CHIMURA , M., I NUTAKE , M., H OJO , H., M ASE , A. & TAMANO , T. 1996 Eigenmode
excitation of Alfvén ion cyclotron instability. Phys. Plasmas 3, 4489–4495.
K ELLEY, G.G. 1967 Elimination of ambipolar potential-enhanced loss in a magnetic trap. Plasma Phys. 9
(4), 503.
K ESNER , J. 1973 Inverse ambipolar potential in a magnetic mirror configuration. Plasma Phys. 15 (6), 577.
K ESNER , J. 1985 Axisymmetric, wall-stabilized tandem mirrors. Nucl. Fusion 25 (3), 275–282.
K ILLEEN , J. & M ARX , K.D. 1970 Solution of the Fokker-Planck equation for a mirror-confined plasma.
Meth. Comput. Phys. 9, 421.
K ILLEEN , J., M IRIN , A.A. & R ENSINK , M.E. 1976 The solution of the kinetic equations for a
multispecies plasma. Meth. Comput. Phys.: Adv. Res. Appl. 16, 389–431.
KOTELNIKOV, I.A., C HERNOSHTANOV, I.S. & P RIKHODKO , V.V. 2017 Electrostatic instabilities in a
mirror trap revisited. Phys. Plasmas 24 (12), 122512.
KOTELNIKOV, I.A., I VANOV, A.A., YAKOVLEV, D.V., C HEN , Z. & Z ENG , Q. 2019 Divertor for a
steady-state gas-dynamic trap. Nucl. Fusion 60 (1), 016008.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 34

34

D. Endrizzi and others

KOTELNIKOV, I., Z ENG , Q., P RIKHODKO , V., YAKOVLEV, D., Z HANG , K., C HEN , Z. & Y U, J. 2022
Wall stabilization of the rigid ballooning m = 1 mode in a long-thin mirror trap. Nucl. Fusion
62 (9), 096025.
K REMEYER , T., F LESCH , K., S CHMITZ , O., S CHLISIO , G. & W ENZEL , U. 2020 Wisconsin in situ
penning (wisp) gauge: a versatile neutral pressure gauge to measure partial pressures in strong
magnetic fields. Rev. Sci. Instrum. 91 (4), 043504.
L AU, C., B ERRY, L.A., JAEGER , E.F. & B ERTELLI , N. 2019 Cold plasma finite element wave model for
helicon waves. Plasma Phys. Control. Fusion 61 (4), 045008.
M IRNOV, V.V. & RYUTOV, D.D. 1979 Linear gasdynamic system for plasma confinement. Sov. Tech. Phys.
Lett. 5 (11), 678–682.
P ETROV, Y.V., H ARVEY, R.W., F OREST, C.B. & A NDERSON , J.K. 2023 Calculations of WHAM2 mirror
neutron rates and FI transport using the GENRAY/ CQL3D-M and MCGO-M codes. In Proceedings
of 49th European Conference on Plasma Physics, July 3–7 2023, Bordeaux, France.
P ETTY, C.C., BAITY, F.W., DE G RASSIE , J.S., M AU, T.K., P INSKER , R.I., P ORKOLAB , M. & P RATER ,
R. 2001 Fast wave current drive at high ion cyclotron harmonics on DIII-D. Plasma Phys. Control.
Fusion 43 (12), 1747–1758.
P OST, R.F. 1961 Equilibrium ambipolar potentials in a mirror machine. Phys. Fluids 4 (7), 902.
P OST, R.F. 1987 The magnetic mirror approach to fusion. Nucl. Fusion 27 (10), 1579–1739.
P OST, R.F. & RYUTOV, D.D. 1995 Mirror fusion research: update and prospects. Comm. Plasma Phys.
Control. Fusion 16 (6), 375–399.
P RATER , R. 1971 Feedback suppression of a large-growth-rate flute mode. Phys. Rev. Lett. 27 (3), 132–135.
ROSENBERG , A.L., M ENARD , J.E., W ILSON , J.R., M EDLEY, S.S., A NDRE , R., P HILLIPS , C.K.,
DARROW, D.S., L E B LANC , B.P., R EDI , M.H., F ISCH , N.J., T EAM , N.S.T.X., H ARVEY, R.W.,
M AU, T.K., JAEGER , E.F., RYAN , P.M., S WAIN , D.W., SABBAGH , S.A. & E GEDAL , J. 2004
Fast ion absorption of the high harmonic fast wave in the national spherical torus experiment. Phys.
Plasmas 11 (5), 2441–2452.
ROSENBLUTH , M.N. & L ONGMIRE , C.L. 1957 Stability of plasmas confined by magnetic fields. Ann.
Phys. (N.Y.) 1 (2), 120–140.
RYUTOV, D.D., B ERK , H.L., C OHEN , B.I., M OLVIK , A.W. & S IMONEN , T.C. 2011 Magnetohydrodynamically stable axisymmetric mirrors. Phys. Plasmas 18 (9), 092301.
SAKAI , O., YASAKA , Y. & I TATANI , R. 1993 High radial confinement mode induced by dc limiter biasing
in the HIEI tandem mirror. Phys. Rev. Lett. 70, 4071–4074.
S CHMITZ , L., et al. 2016 Suppressed ion-scale turbulence in a hot high-β plasma. Nat. Commun. 7, 13860.
S EEMANN , O., B E ’ ERY, I. & F ISHER , A. 2018 Stabilization of magnetic mirror machine using rotating
magnetic field. J. Plasma Phys. 84 (5), 905840502.
S EVERN , G., H ERSHKOWIT E, N., N ELSON , B. & P EW, J. 1983 Radial Potential Modification
Experiments in the Phaedrus Tandem Mirror Machine. Bulletin of the American Physical Society.
S HIDARA , H., NAKASHIMA , Y., I MAI , T., K ARIYA , T., M INAMI , R., I CHIMURA , M. & YOSHIKAWA ,
M. 2011 Ec wave plasma breakdown on gamma 10 device. Fusion Engng Des. 86 (6–8), 913–915.
S IMONEN , T., et al. 2008 The axisymmetric tandem mirror: a magnetic mirror concept game changer
magnet mirror status study group. LLNL Tech. Rep..
S IMONEN , T.C., et al. 1983 Operation of the tandem-mirror plasma experiment with skew neutral-beam
injection. Phys. Rev. Lett. 50, 1668–1671.
S MIRNOV, A.P., H ARVEY, R.W. & K UPFER , K. 1994 A general ray tracing code genray. Bull. Am. Phys.
Soc. 39 (7), 1626.
S MITH , G.R. 1984 Alfvén ion-cyclotron instability in tandem-mirror plasmas. I. Phys. Fluids 27 (6),
1499–1513.
S OLDATKINA , E.I., M AXIMOV, V.V., P RIKHODKO , V.V., SAVKIN , V.Y.A., S KOVORODIN , D.I.,
YAKOVLEV, D.V. & BAGRYANSKY, P.A. 2020 Measurements of axial energy loss from magnetic
mirror trap. Nucl. Fusion 60 (8), 086009.
S TIX , T.H. 1992 Waves in Plasmas. American Institute of Physics.
W HYTE , D. 2019 Small, modular and economically attractive fusion enabled by high temperature
superconductors. Phil. Trans. A. Math. Phys. Engng Sci. 377 (2141), 20180354.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press

## PDF page 35

Physics basis for WHAM

35

W HYTE , D.G., M INERVINI , J., L A BOMBARD , B., M ARMAR , E., B ROMBERG , L. & G REENWALD , M.
2016 Smaller and sooner: exploiting high magnetic fields from new superconductors for a more
attractive fusion energy development path. J. Fusion Energy 35, 41–53.
W URZEL , S.E. & H SU, S.C. 2022 Progress toward fusion energy breakeven and gain as measured against
the Lawson criterion. Phys. Plasmas 29 (6), 062103.
YAKOVLEV, D.V., S HALASHOV, A.G., G OSPODCHIKOV, E.D., M AXIMOV, V.V., P RIKHODKO , V.V.,
SAVKIN , V.Y.A., S OLDATKINA , E.I., S OLOMAKHIN , A.L. & BAGRYANSKY, P.A. 2018 Stable
confinement of high-electron-temperature plasmas in the GDT experiment. Nucl. Fusion 58 (9),
094001.
YAKOVLEV, D.V., S HALASHOV, A.G., G OSPODCHIKOV, E.D., S OLOMAKHIN , A.L., SAVKIN , V.Y.A.
& BAGRYANSKY, P.A. 2017 Electron cyclotron plasma startup in the GDT experiment. Nucl. Fusion
57 (1), 016033.
Y USHMANOV, P.P. 1966 Confinement of slow ions of plasma with positive potential in a mirror trap. Sov.
Phys. JETP 22, 409.
Z HU, G., S HI , P., YANG , Z., Z HENG , J., LUO , M., Y ING , J. & S UN , X. 2019 A new method to suppress
the Rayleigh-Taylor instability in a linear device. Phys. Plasmas 26 (4), 042107.
Z WEBEN , S.J., et al. 1997 Alpha-particle physics in the tokamak fusion test reactor DT experiment. Plasma
Phys. Control. Fusion 39 (5A), A275.

https://doi.org/10.1017/S0022377823000806 Published online by Cambridge University Press
