Source: https://doi.org/10.1109/TPS.2019.2942997
PDF sha256: 414ef4cd6e97b037003e464e276320ebb1568a751eaa46bc50f090d3d54695ef
License: public domain: 17 U.S.C. 105
Language: eng
Fidelity: machine (failed: characters)

# Transcription of pais_2019_plasma_compression_fusion_device.pdf

Transcription of `pais_2019_plasma_compression_fusion_device.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-6 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
IEEE TRANSACTIONS ON PLASMA SCIENCE

1

The Plasma Compression Fusion Device—Enabling
Nuclear Fusion Ignition
Salvatore Cezar Pais
Abstract— The plasma compression fusion device (PCFD) generates the energy gain by plasma compression-induced nuclear
fusion. This concept has the capability of maximizing the product
of plasma pressure and energy confinement time to maximize
the energy gain, and thus give rise to fusion ignition conditions.
The preferred embodiment of this original concept uses a hollow
cross-duct configuration of circular cross section in which the
concentrated magnetic energy flux from two pairs of opposing curved-headed counter-spinning conical structures (possibly
made from an alloy of tungsten with high capacitance) whose
outer surfaces are electrically charged compresses a gaseous
mixture of fusion fuel into a plasma, heated to extreme temperatures and pressures. The generated high-intensity electromagnetic
(EM) radiation heats the plasma and the produced magnetic fields
confine it in between the counter-spinning conical structures,
named the dynamic fusors (four of them—smoothly curved apex
sections opposing each other in pairs). The dynamic fusors can
be assemblies of electrified grids and toroidal magnetic coils,
arranged within a conical structure whose outer surface is
electrically charged. The cross-duct inner surface surrounding
the plasma core region is also electrically charged and vibrated
in an accelerated mode to minimize the flux of plasma particles
(including neutrals) from impacting the PCFD surfaces and
initiating a plasma quench. The fusion fuel (preferably deuterium
gas) is introduced into the plasma core through the counterspinning conical structures, namely, injected through orifices
in the dynamic fusor heads. There is envisioned another even
more compact version of this concept, which uses accelerated
vibration in a linear-duct configuration (using two counterspinning dynamic fusors only) and would best be suited for
fusion power generation on aircraft, or main battle tanks. The
concept uses controlled motion of electrically charged matter
through accelerated vibration and/or accelerated spin subjected
to smooth, yet rapid acceleration transients, to generate extremely
high-energy/high-intensity EM radiation (fields of high-energy
photons) which not only confines the plasma but also greatly
compresses it so as to produce a high power density plasma burn,
leading to ignition. The PCFD concept can produce power in the
gigawatt to terawatt range (and higher) with input power in the
kilowatt to megawatt range and can possibly lead to ignition (selfsustained) plasma burn. Several important practical engineering
and operational issues with operating a device such as the PCFD
are discussed.
Index Terms— Acceleration control, frequency control, fusion
power generation, fusion reactors, magnetic confinement,
Manuscript received April 11, 2018; revised February 1, 2019 and June 29,
2019; accepted July 11, 2019. This work was supported in part by the Naval
Innovative Science and Engineering (NISE)—Basic and Applied Research
(BAR) Section 219 Program, The High Energy Electromagnetic Field Generator (HEEMFG), under Project 219BAR-17-009. The review of this article
was arranged by Senior Editor E. Surrey.
The author was with NAVAIR/NAWCAD, NAS PAX, Patuxent River, MD
20670 USA. He is now with Navy SSP, Washington Navy Yard, Washington,
DC USA (e-mail: salvatore.pais@ssp.navy.mil).
Color versions of one or more of the figures in this article are available
online at http://ieeexplore.ieee.org.
Digital Object Identifier 10.1109/TPS.2019.2942997

magnetic fields, oscillators, piezoelectric devices, plasma confinement, plasma control.

I. I NTRODUCTION

T

HERMONUCLEAR fusion involves the forcing together
(unification) of light nuclei to form a heavier nucleus,
which due to the mass defect occurs with generation of energy,
as expressed in the ubiquitous (E = mc2 ) expression. Fusion
occurs at extremely high temperatures, exceeding the core
temperature of the Sun, which is approximately 10 million
degrees Celsius. For example, the deuterium–tritium fusion
reaction occurs at temperatures in excess of 175 million
degrees Celsius and that of deuterium–deuterium (D-D) at
approximately 232 million degrees Celsius.
At these extremely high temperatures and pressures, a gas
will ionize and form a plasma (the fourth state of matter) that is
an ensemble of an enormous number of electrons and positive
ions (≥1020/m3 ), which constantly interact with each other,
exchanging energy. The three primary methods of confining
plasma to make the ions fuse are gravitational confinement,
inertial confinement, and magnetic confinement. To have
fusion from gravitational confinement, stellar-sized masses are
required; thus, we are left with inertial and magnetic confinement, as well as possible hybrids of the two. Inertial confinement fusion is produced with laser-driven implosions or with
electric fields (electrostatic), whereas magnetic confinement
fusion is generated with extremely high magnetic induction in
configurations such as tokamaks, magnetic mirrors, magnetic
cusps, pinches, and magnetized targets [1].
All these methods of plasma confinement have grave issues,
ranging from extremely large size (commensurate to that of an
aircraft carrier) and plasma instabilities for tokamaks, to power
losses and short confinement times for magnetic mirror/cusp
machines. None of these confinement methods to date has
been able to achieve break-even fusion reactions (in a steadystate operational mode), namely, the condition for the fusion
power output to equal the power input, let alone achieve
the ignition condition whereby a fusion plasma burn is selfsustained, without the need for external power input. For a
fusion reaction to occur, in the case of the deuterium–tritium
reaction, we need to abide by the Lawson criterion, namely,
nTτ E ≥ 3 × 1021 KeV · /m3

(1)

where n is the plasma density, T is the plasma temperature,
and τ E is the energy confinement time. This expression drives
the point that the higher the product of plasma pressure with
plasma energy confinement time, the higher the energy gain
of the fusion reaction. The equal sign in (1) represents the

U.S. Government work not protected by U.S. copyright.

## PDF page 2

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
2

IEEE TRANSACTIONS ON PLASMA SCIENCE

break-even condition, in other words, an energy gain of one,
which is the condition under which the fusion power output
equals the reactor power input.
For the D-D reaction, which is the reaction of choice for the
present concept, the triple product, nTτ E ≥ 1023 KeV·s/m3 ,
since the temperatures required for fusion in the D-D reaction are far higher than those required for fusion in the
deuterium–tritium reaction.
An important fact for magnetic confinement-induced fusion
is that if the strength of the magnetic field is doubled
(i.e., double the magnetic induction B in units of tesla), the linear size of the reactor is reduced by half, given other fusion
parameters are held constant. Hence, being able to generate
high magnetic induction (magnetic flux density) is extremely
important in developing a compact fusion device [1].
There are two expressions that convey the importance of
having high magnetic field induction, when it comes to plasma
magnetic confinement for fusion, namely,
Energy Gain ∼ B

3

(2)

and
Fusion Power Density ∼ P 2 ∼ B 4

(3)

where P is the plasma pressure and B is the magnetic
induction or magnetic flux density, given the condition that
the ratio of plasma pressure and magnetic field pressure is on
the order of unity.
At present, there are few envisioned fusion reactors/devices
that come in a small, compact package (ranging from 0.3 to
2 m in diameter) and use different versions of plasma magnetic
confinement. Three such devices are the Lockheed Martin
(LM) Skunk Works compact fusion reactor (CFR), the EMC2
Polywell fusion concept, and the Princeton field-reversed
configuration (PFRC) machine [2]–[4].
The LM-CFR uses a magnetic mirror configuration in which
the toroidal magnetic coils featuring variable current generate
magnetic field oscillations which heat a confined plasma.
The Polywell device uses a hybrid plasma confinement and
heating scheme using both inertial electrostatic confinement
and magnetic confinement within a polyhedral biconic mirror
cusp geometry.
The PFRC uses a unique radio frequency (RF) heating
scheme to induce rotating magnetic fields to confine plasma.
These devices feature short plasma confinement times, possible plasma instabilities with scaling of size, and their ability
of achieving the break-even fusion condition, let alone a selfsustained plasma burn leading to ignition remains doubtful.
The key to fusion seems to rest with the achievement
of extremely high magnetic fields, possibly exceeding 30 T,
which are not even high-temperature REBCO-type superconducting magnets, which can be readily generated at present.
However, it is herein argued that extremely high B-fields
can be generated by controlled motion of electrically charged
matter, through accelerated spin and/or accelerated vibration,
subjected to rapid (yet smooth) acceleration transients.
II. E NABLEMENT OF C ONCEPT
As depicted in Fig. 1., the preferred embodiment of this
original concept [plasma compression fusion device (PCFD)]

Fig. 1.

PCFD cross-duct configuration (side view).

uses a hollow cross-duct configuration of circular cross section
in which the concentrated magnetic energy flux from two
pairs of opposing curved-headed counter-spinning conical
structures (possibly made from an alloy of tungsten with
high capacitance) whose outer surfaces are electrically charged
compresses a gaseous mixture of fusion fuel into a plasma,
heated to extreme temperatures and pressures.
The PCFD uses controlled motion of electrically charged
matter through accelerated vibration and/or accelerated spin
subjected to smooth, yet rapid acceleration–deceleration–
acceleration transients, to generate extremely highenergy/high-intensity electromagnetic (EM) fields which
not only confine the plasma but also greatly compress it
(by inducing a high-energy negative potential well) so as
to produce a high power density plasma burn, leading to
ignition.
The generated high-intensity EM radiation heats the plasma
and the produced magnetic fields confine it in between the
counter-spinning conical structures, named the dynamic fusors
(four of them—smoothly curved apex sections opposing each
other in pairs). It is important that the cross-duct inner surface
surrounding the plasma core region is electrically charged
and vibrated to prevent the plasma particles from impacting
the walls and initiating a plasma quench. Vibration can be
achieved by passing an electrical current through piezoelectric
films such as lead zirconate titanate (PZT) imbedded in the
PCFD duct inner walls. The PCFD device is housed in a
Faraday cage for reasons of personnel safety.
A 10–15-cm-thick boron carbide (or tungsten alloy) shielding which acts as the Faraday cage can also incorporate the
cooling channels for the thermal conversion cycle, as well as
provide the needed structural support and integrity to withstand
the fusion-induced neutron bombardment.
Plasma instabilities would be minimized and possibly suppressed by the shearing flows generated by the counterspinning dynamic fusors. The flow shearing would tear apart
the vortical eddies responsible for the onset of turbulence
within the plasma, which is regarded as the main source
of plasma instabilities in a fusion reaction [7]–[9]. Fig. 2
shows an even more compact version of the concept, which
uses vibration in a linear-duct configuration, featuring two

## PDF page 3

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
PAIS: PCFD—ENABLING NUCLEAR FUSION IGNITION

Fig. 2.

3

PCFD linear-duct configuration (side view).

counter-spinning dynamic fusors only, and would best be
suited for fusion power generation on aircraft, or main battle
tanks.
For both configurations, the fusion power output is extracted
through conformal heat exchangers (not shown) which are
flush with the PCFD outer walls and carry the neutronproduced heat to a thermoelectric generator through a cooling
fluid, such as water or poly-alpha olefin (PAO).
The fusion fuel (preferably deuterium gas) is introduced
into the plasma core through the counter-spinning conical
structures, namely, injected through orifices in the dynamic
fusor heads. Deuterium (heavy hydrogen) can be abundantly
extracted from sea-water, hence the “virtually limitless” fuel
source idea that makes this concept extremely beneficial.
The neutronic gaseous fusion fuel can be deuterium–tritium,
D-D, or possibly a deuterium–xenon mixture. This later reaction can produce Xenon-129 with the release of two fast
(highly energetic) neutrons which would greatly amplify the
power output; however, PCFD wall degradation and enhanced
radioactivity effects need to be considered from both an
operational and a safety perspective.
Aneutronic fuel can be proton–boron11 (for fusion at more
than 10× the fusion temperature of the neutronic fuel). In this
case, there will be no neutrons released, hence no radioactivity
dangers arise. For this hydrogen–boron fuel, there is a one in
one thousand chance of a Gamma-ray channel being formed,
which in case of full operational status of the device would
demand great caution. Direct energy conversion is used in
extracting fusion power from the PCFD, because the products
of this aneutronic fuel are three alpha particles (three helium4 particles), and hence a direct conversion of these charged
particles through a hi-tech transformer is made viable. The
main issue with the use of aneutronic fuel is that it demands a
fusion temperature of 2 billion degrees Celsius (and higher), an
almost 10× increase over neutronic fuel, such as the preferred
deuterium gas.
The PCFD will use deuterium (2 H) gas as the fusion fuel
of choice, yielding the reactions
2

H +2 H → 3 H(1.01 MeV) + p + (3.02 MeV)[50%]

2

H +2 H → 3 He(0.82 MeV) + n 0 (2.45 MeV)[50%]. (4)

Thus, it is feasible to use both direct (electrical) and indirect
(thermal) energy conversion using deuterium gas, which is
highly desirable from an operational viewpoint.

Fig. 3.

Alternative dynamic fusor (cross-sectional side view).

As shown in Fig. 3, the dynamic fusors can be assemblies of
electrified grids and toroidal magnetic coils, arranged within
a conical structure whose outer surface is electrically charged.
The electrical grids are used to ionize the deuterium gas (or
other fusion fuel in gaseous form) and are kept at different
oppositely charged voltages so as to electrostatically accelerate
either electrons or ions into the fusion plasma core, depending
on the desired physical effect, in a manner similar to ion
thrusters. The direction of the dynamic fusor spin is such that
the generated magnetic flux always points toward the plasma
core.
The dynamic fusors can act as particle accelerators for
electrons that are closely bound to the magnetic field lines
of the inner toroidal coil, as well as to the magnetic field
lines of the conical structure, once they exit the dynamic fusor.
These electrons are electrostatically accelerated through a set
of two grids exhibiting a potential difference into the plasma
core, forming a deep (high-energy) negative potential well.
This negative potential well greatly accelerates the positively
charged ions toward it, and as the ions keep recirculating
around the well, they undergo fusion. A high-temperature,
high-pressure plasma core results from the impingement of gas
dynamic vortical plumes, which exhibit high viscous heating,
as well as the intense collisions of electrons and positively
charged ions which make up these plumes. To heat the plasma
at the extreme temperatures that fusion requires, the electrically charged dynamic fusors (outer surfaces only) generate
high EM radiation by virtue of their accelerating spin. The
inner surfaces of the dynamic fusors are well-insulated against
electrical charge migration, possibly with silicon carbide (or
boron nitride, boron carbide) liners. An alloy of tungsten with
high capacitance, to hold an electric charge of a least 1 C,
is the material of choice for the dynamic fusors, which can
also be dome-like in geometry. The dynamic fusor is mounted
on a hollow shaft (deuterium gas conduit) which is coupled to
a variable power dc induction motor and can be accelerated–
decelerated–accelerated in spin, through a digital controller.
The PCFD must be vacuum-pumped for fusion power to be

## PDF page 4

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
4

IEEE TRANSACTIONS ON PLASMA SCIENCE

effectively produced. An ultrahigh vacuum on the order of
10−5 torr is desirable, yet a lower quality vacuum may be
used, given operational constraints on the device.
III. H IGH -E NERGY E LECTROMAGNETIC
F LUX G ENERATION
As discussed in two recent articles by the inventor [5], [6],
for conditions of accelerated vibration or accelerated spin of
an electrically charged object/system, we can write for the
maximum EM energy flux (time rate of change in EM energy
transfer per unit surface area)
Smax = f G (σ 2 /ε0 )[(Rv ν 2 )top ]

(5)

where f G is the charged system geometric shape factor (equal
to 1 for a disk configuration), σ is the surface charge density,
ε0 is the electrical permittivity of free space, Rv is the vibration
(harmonic oscillation) amplitude, ν is the angular frequency
of vibration in hertz, and, similarly in the case of axial spin,
Rv is the effective system radius, while ν represents the
angular frequency of spin, and top is the operational time for
which the electrically charged system is operated at maximum
acceleration (Rv ν 2 ). This closed-form formulation is the result
of the synthesis of classical EM field theory with the physics
of simple harmonic motion.
Furthermore, for the case of rapid time rates of change in
accelerated vibration/spin (rapid acceleration transients) of the
charged system, given that the time differential of acceleration
is nonzero, we obtain
]
[
2
Smax = f G (σ 2 /ε0 ) (Rv ν 3 )top
.
(6)
This formulation shows that even with moderate vibrational/spin frequencies in a rapidly accelerating mode, the EM
energy flux is greatly amplified (cubic frequency profile).
Moreover, this shows the extensive capabilities of a highenergy/high-frequency EM field generator, when used to heat
plasma within the confines of the PCFD.
If we consider adding to the equation representing simple
harmonic motion an “energy/momentum-pumping” (negative
damping) term (bv), endemic of system acceleration, where b
is a constant and v is (dx/dt), namely, the speed of a vibrating
mass (m), it can be shown that the maximum of the total
energy (E T ) of the vibrating system can be written as
E T ≈ m Rv2 2 [exp(2t)]

(7)

where  is the angular frequency of vibration, under the
condition [(b/2m) >> 0 (natural frequency of vibration)].
Because the EM energy flux is directly proportional to E T ,
we observe that there will be an exponential growth in energy
flux with accelerating vibration, especially under the condition
of rapid acceleration transients.
Considering a classical Newtonian second law expression
using the Lorentz (EM) force, we can relate the vibrating mass
(m) with its vibrating charge (Q), in that m becomes directly
proportional to the square of the ratio (Q/). Coupling this
relation with (7) yields
)
(
Smax ≈ (Q 2 /ε0 ) Rv2 /Rs5 [exp(2t)].
(8)

This equation represents the maximum EM flux that can be
achieved by accelerated vibration under the aforementioned
condition and applies to a spherical geometry (radius Rs ) for a
vibrating mass (m) of corresponding charge (Q). Note that the
vibration in the electrically charged PCFD device inner walls
must be monitored so that it does not greatly exceed the natural
vibration frequency of its component materials, because this
can generate an exponential growth in the EM flux and may
have deleterious effects on the plasma core, as well as on the
structural integrity and operational safety of the device.
Moreover, due to the conical geometry of the counterspinning dynamic fusors, the plasma fluid will assume the
shape of vortex structures. Considering the free force vortex
expression of (curl v = Av v), where v is the plasma fluid
velocity and Av is a constant, which under certain conditions
can be far greater than 1, we can write (B is directly proportional to v)
B/Rv ∼ curlB = Av B

(9)

where Rv is the effective vortex radius, so that as Rv goes
to zero, Av becomes a B-field amplification factor which
mathematically can go to infinity. Physically, this expresses
the great amplification of the magnetic induction B-fields of
the vortical plasma structures in the PCFD plasma core.
IV. P OSSIBLE O PERATIONAL I SSUES W ITH
THE PCFD D ESIGN
There are several important practical engineering and operating issues with operating a device such as the PCFD.
First, the deuterium–tritium triple product given in (1) will
be much higher, by at least two orders of magnitude, for
the D-D reaction envisioned as the PCFD fusion reaction of
choice. This is due to the fact that the plasma physics presented
herein is oversimplistic, with little if any consideration of
plasma transport or instabilities which degrade the achievable
triple product.
Further (future) theoretical research would have to be performed to give consideration to the impact of the extremely
high neutron flux anticipated in the D-D reaction (even though
this will peak at lower energy than for deuterium–tritium) and
even proton–boron fusion is not without neutron issues due to
the byproducts and B isotope production.
For the D-D reaction, which is the reaction of choice for our
present concept, the triple product, nTτ E ≥ 1023KeV s/m3 ,
because the temperatures required for fusion in the D-D
reaction are far higher than those required for fusion in the
deuterium–tritium reaction [10]. As far as the plasma instabilities (magnetohydronamic, interchange, kink, etc.) within
the PCFD device are concerned, it is possible that such
instabilities would be minimized and possibly suppressed by
the shearing flows generated by the counter-spinning dynamic
fusors. The induced flow shearing would tear apart the vortical
eddies responsible for the onset of turbulence within the
plasma, which is regarded as the main source of plasma
instabilities in a fusion reaction [7]–[9]. It is important to
note that this observation would have to be experimentally
verified in an actual working PCFD device, because plasma

## PDF page 5

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
PAIS: PCFD—ENABLING NUCLEAR FUSION IGNITION

instabilities represent phenomena of immense complexity, for
which theoretical expectations are insufficient with regard to
conclusive concept validation. Plasma heating would also play
an important role in the verification process, because this
drives plasma density and temperature gradients.
Moreover, the PCFD geometrical configuration can give rise
to high beta-factors, namely, the ratio of the plasma pressure
to the magnetic pressure can be high, possibly on the order
of unity. As discussed in [7], high beta can diminish the
possibility of the onset of plasma instabilities and in this
manner control their existence. The PCFD device can optimally control gradients in plasma densities and temperatures,
thereby controlling and minimizing plasma instabilities. This
theoretical argument must, however, be tested experimentally,
because plasma instabilities are highly complex entities, whose
optimal control proves to be a highly controversial subject.
Another possible issue with the PCFD is the extremely
high B-fields anticipated in operating it. Even though such
high-intensity EM fields have been shown to be theoretically
feasible [5], [6], experimental verification is necessary for
proof of concept.
If indeed the controlled motion of electrically charged
matter (from solid to plasma) under accelerated spin and/or
accelerated vibration and subjected to rapid acceleration transients can produce the theoretically anticipated high-energy
EM fields necessary for optimal PCFD operation, then another
major problem can arise, namely, possible structural failure of
the device due to the strength of material limits imposed by
the generated B-fields.
This is a problem of utmost importance for safety and
survivability of the device and its practical operation and
must be addressed at the highest levels, if the PCFD fusiongenerating abilities are to be realized. However, the ability of
the PCFD device to produce extremely high magnetic fields
can shape the plasma core in a configuration conducive to a
high possibility of self-sustained plasma burn fusion [11].
Furthermore, the PCFD device is operated in a transient, farfrom-equilibrium mode, which in the case of the D-D reaction
can give rise to fast neutrons and fast protons, a fact which
would optimally control fusion energy production [12]. The
impact of the high-speed neutrons with the walls of the enclosure which houses the dynamic fusors can be mitigated by the
high EM radiation generated by the accelerated vibration of
the electrified inner PCFD surfaces (enclosure), because fields
of photons carry both energy and momentum. This is not to
say that particle flux (including neutrals) will not impact the
PCFD surfaces; however, such interactions can be minimized,
as explained at the end of this section.
It is quite possible that to maintain the extremely high
temperatures (in excess of 232 million degree Celsius) for the
D-D fusion to occur, RF heating will be of great necessity to be
incorporated within the PCFD design. At the present time, only
EM heating of the plasma is provided by the dynamic fusors
and the vibrating electrified inner surfaces of the PCFD crossducts; however, RF heating may be necessary for establishing
and maintaining a burning plasma core.
Once a burning plasma state has been achieved, the PCFD
transient operation may become steady-state by the cou-

5

pling of additional RF heating with additional fuel injection
into the plasma core. The optimal RF heating method for
utilization would be electron cyclotron resonance heating
(ECRH), which uses RF waves of >100-GHz frequencies
for plasma heating. RF waves of this frequency can be
produced by gyrotrons (novel unconventional technology) and
couple optimally with the plasma from an absorption (of heat)
perspective. It may be possible to use 5-GHz radio waves,
produced by a klystron; however, these waves may not be
able to penetrate the plasma edge and thus offer optimal
heating.
One aspect of the PCFD reactor design that is critical for
future investigation is the large particle and heat flux to the
reactor wall, especially because the smaller the system is
made, the higher this impact will be. Moreover, the neutron
loading, even for a gigawatt and terawatt system (such as the
proposed PCFD reactor), will be extremely large on the reactor
walls, something that tokamaks and stellarators often have to
contend with.
Due to the highly complex state that is represented by
a burning plasma, the PCFD reactor would need a highly
sophisticated feedback control system, to sustain this fickle
state of matter. Therefore, because experiment trumps theory
every time, a phased approach based on careful experimental
studies needs to be considered in making the PCFD design
a viable reality for producing cost-effective fusion power,
especially at ignition conditions.
The generation of very high B-fields on the order of 1000 T
and above is amply discussed in [5] and [6]; these high
magnetic induction values can be obtained by the accelerated
spin and/or accelerated vibration of electrically charged matter subjected to rapid, yet smooth acceleration–deceleration–
acceleration transients. Indeed, in case this charged matter is
a plasma, it can be readily observed that the ν 2 term in (5) is
directly proportional to the plasma oscillation frequency and
thus directly proportional to the plasma density. Therefore,
high B-field values can be obtained by increasing both the
angular frequency of spin/vibration of the dynamic fusors and
the plasma density. The only limiting factor in the case of the
PCFD design and fabrication is that the structural integrity of
the fusion device can be compromised by B-fields exceeding
1000 T.
Of notable importance is also the fact that for optimal
operation of the PCFD system, we use the accelerated spin
of the dynamic fusors in conjunction with the accelerated
vibration of the PCFD electrically charged inner duct surface
(see Figs. 1 and 2). This greatly limits the loss cones of
particle flux out of the plasma core, because such PCFD
operation would produce high-intensity EM radiation, namely,
intense fields of high-energy photons oriented into the core
which would greatly minimize particle contact with the PCFD
surfaces, including high-energy neutral particles (photons are
uncharged). The only time that particle contact with the
PCFD surfaces may occur is during the deceleration mode of
the acceleration–deceleration–acceleration transient; however,
such adverse effects can be counteracted with enhanced reactor
shielding, as well as other safety precautions herein not
discussed.

## PDF page 6

This article has been accepted for inclusion in a future issue of this journal. Content is final as presented, with the exception of pagination.
6

IEEE TRANSACTIONS ON PLASMA SCIENCE

To properly understand the plasma physics of the PCFD
device (hence, properly judge its fusion ignition capabilities),
it is necessary to consider future studies involving the Monte
Carlo simulations of many-particle nonlinear dynamics which
is a necessary effort to be undertaken for PCFD validation
and verification in conjunction with experimental work. Such
studies would also result in preliminary B-field mappings of
the fusion plasma core and guide future experimental research
to be undertaken. No such unclassified data exist at this point
in time for the PCFD effort.
V. C ONCLUSION —F EASIBILITY OF PCFD C ONCEPT
Using physics explained in two recently published peerreviewed articles by Pias [5], [6], we can write the maximum
of magnetic field induction (B) for one of the dynamic fusors
as a function of the angular frequency of spin of the dynamic
fusor (ω) as
2
BMAX ≈ μ0 σ Rω ω3 top

(10)

where μ0 is the magnetic permeability of free space (on the
order of) O(10−6 ), σ is the surface charge density of the
dynamic fusor, Rω is the effective spin radius of the dynamic
fusor, and top is the operational time at maximum acceleration
of spin.
2 ∼ O(1), that is order of
For the condition of μ0 σ Rω top
unity, we obtain BMAX ∼ ω3 , in other words, the maximum
magnetic flux density scales with the cube of the angular spin
frequency of the dynamic fusor.
Because laboratory experiments (performed by the author’s
team—unpublished work) have taken disk-shaped objects of
(less than) 10 cm in diameter and spun them at 10 000 rad/s
(100 000 rpm), with no apparent failure resulting from centrifugal loading, we can safely conclude that given the
hardness of tungsten from which the dynamic fusor is
manufactured, it is possible to have values of ω on the
order of 104 rad/s. This means that a value for BMAX on the
order of 106 T (and much higher) is achievable by accelerated
spin of the surface-charged dynamic fusor, with a time differential of acceleration not equal to zero (smooth, yet rapid spin
acceleration—no abrupt/jerking motion required).
Taking into consideration (2), the energy gain of the fusion
reaction is on the order of 1018, meaning that the possibility
of fusion ignition, that is, self-sustained plasma burn, is highly
feasible, under the aforementioned conditions. As a result of
this simple analysis, it is important to note that the present
concept can produce power in the gigawatt to terawatt range
(and higher) with the input power in the kilowatt to megawatt
range and possibly lead to ignition plasma burn, that is, selfsustained plasma burn without need for external input power.

ACKNOWLEDGMENT
This article has no bearing at all on the author’s present
work with Navy SSP.
R EFERENCES
[1] K. Miyamoto, “Fundamentals of plasma physics and controlled fusion,”
Tech. Rep. NIFS-PROC-48, Oct. 2000.
[2] T. J. McGuire, “Magnetic field plasma confinement for compact fusion
power,” U.S. Patent 2014 0 301 518 A1, Oct. 9, 2014.
[3] R. W. Bussard, “Method and apparatus for controlling charged particles,”
U.S. Patent 2008 0 187 086 A1, Aug. 7, 2008.
[4] S. J. Thomas et al., “Fusion-enabled pluto orbiter and Lander,” in Proc.
AIAA SPACE Astronaut. Forum Expo., 2017, p. 5276.
[5] S. C. Pais, “High frequency gravitational waves-induced propulsion,”
SAE Tech. Paper 2017-01-2040, 2017.
[6] S. C. Pais, “A Hybrid craft using an inertial mass modification device,”
in Proc. AIAA SPACE Astronaut. Forum Expo., 2017, p. 5343.
[7] J. Park et al., “High-energy electron confinement in a magnetic cusp
configuration,” Phys. Rev. X, vol. 5, Jun. 2015, Art. no. 021024.
[8] E. Proano and B. Rollin, “Toward a better understanding of hydrodynamic instabilities in inertial fusion approaches,” in Proc. 53rd
AIAA/SAE/ASEE Joint Propuls. Conf., 2017, p. 4676.
[9] E. H. Matlis, A. J. Hoffman, and T. C. Corke, “Experiments on a
plasma-based metamaterial at microwave fequencies,” in Proc. 55th
AIAA Aerosp. Sci. Meeting, 2017, p. 1971.
[10] J. D. Lawson, “Some criteria for a useful thermonuclear reactor,” At.
Energy Res. Establishment, Harwell, U.K., Tech. Rep., Dec. 1955.
[11] L. Spitzer, Jr., “The stellarator concept,” Phys. Fluids, vol. 1, no. 4,
p. 253, 1958.
[12] R. Post, “Thoughts in fusion energy development,” in Proc. Fusion
Power Associates Annu. Meeting Symp., F. Post and J. H. Nuckolls,
Eds., Dec. 2008.

Salvatore Cezar Pais received the Ph.D. degree
in mechanical and aerospace engineering from
Case Western Reserve University, Cleveland, OH,
USA.
He was as a NASA Graduate Research Fellow with the NASA Glenn (Lewis) Research Center, Cleveland. He was with NAVAIR/NAWCAD,
NAS PAX, Patuxent River, MD, USA. He was a
General Engineer/Advanced Concepts Analyst with
Northrop Grumman Aerospace Systems, where he
was involved in defense-oriented work. He is currently with the Department of Defense, Department of the Navy, Strategic
Systems Programs (SSP), Washington, DC, USA, where he is involved in a
permanent civilian capacity. He has advanced knowledge of theory, analysis,
and modern experimental and computational methods in aerodynamics, along
with an understanding of air-vehicle and missile design, especially in the
domain of hypersonic power plant and vehicle design. Furthermore, he has
expertise in electrooptics and emerging quantum technologies, particularly the
laser power generation arena, and high-energy electromagnetic field generation, besides condensed matter physics, such as the emerging breakthrough
field of room temperature superconductivity, as related to advanced field
propulsion. As a relevant aside, it is important to stress the fact that his work
at SSP has absolutely no bearing on the subject of the paper at hand.
