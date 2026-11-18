Source: https://doi.org/10.3390/s24175537
PDF sha256: 522eaf7d8e393628b695f161dee3401e916d459caa8285c7f914d28098de55f8
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of viciana_2024_earth_field_nmr_spectrometer.pdf

Transcription of `viciana_2024_earth_field_nmr_spectrometer.pdf` in this directory, 23 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-23 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

sensors
Article

Development of an Earth-Field Nuclear Magnetic Resonance
Spectrometer: Paving the Way for AI-Enhanced Low-Field
Nuclear Magnetic Resonance Technology
Eduardo Viciana 1 , Juan Antonio Martínez-Lao 1 , Emilio López-Lao 1 , Ignacio Fernández 2, *
and Francisco Manuel Arrabal-Campos 1,2, *
1

2

*

Citation: Viciana, E.; Martínez-Lao,
J.A.; López-Lao, E.; Fernández, I.;
Arrabal-Campos, F.M. Development
of an Earth-Field Nuclear Magnetic
Resonance Spectrometer: Paving the
Way for AI-Enhanced Low-Field
Nuclear Magnetic Resonance

Department of Engineering, Research Centre CIMEDES, Escuela Superior de Ingeniería,
University of Almería, 04120 Almeria, Spain; evg010@ual.es (E.V.); ell658@inlumine.ual.es (E.L.-L.)
Department of Chemistry and Physics, Research Centre CIAIMBITAL, University of Almería,
04120 Almeria, Spain
Correspondence: ifernan@ual.es (I.F.); fmarrabal@ual.es (F.M.A.-C.)

Abstract: Today, it is difficult to have a high-field nuclear magnetic resonance (NMR) device due to
the high cost of its acquisition and maintenance. These high-end machines require significant space
and specialist personnel for operation and offer exceptional quality in the acquisition, processing, and
other advanced functions associated with detected signals. However, alternative devices are low-field
nuclear magnetic resonance devices. They benefit from the elimination of high-tech components
that generate static magnetic fields and advanced instruments. Instead, they used magnetic fields
induced by ordinary conductors. Another category of spectrometers uses the Earth’s magnetic field,
which is simple and economical but limited in use. These devices are called Earth-Field Nuclear
Magnetic Resonance (EFNMR) devices. This device is ideal for educational purposes, especially for
engineers and those who study nuclear magnetic resonance, such as chemistry or other experimental
sciences. Students can observe their internal workings and conduct experiments that complement
their education without worrying about damaging equipment. This article provides a detailed
explanation of the design and construction of electrical technology devices for the excitation of
atomic spin resonance using Earth’s magnetic fields. It covers all necessary stages, from research to
analysis, including simulation, assembly, construction of each component, and the development of
comprehensive software for spectrometer control.
Keywords: Earth’s field NMR; NMR spectrometer; EFNMR

Technology. Sensors 2024, 24, 5537.
https://doi.org/10.3390/s24175537
Academic Editors: Qing Yu, Ran Tu,
Ting Liu and Lina Li
Received: 19 July 2024
Revised: 20 August 2024
Accepted: 25 August 2024
Published: 27 August 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/
4.0/).

1. Introduction
The history of nuclear magnetic resonance (NMR) is deeply intertwined with advances
in multiple scientific disciplines, leading to its application in various fields such as chemistry,
biochemistry, and medicine [1]. The initial breakthroughs in NMR can be traced back to the
quantization of nuclear spin angular momentum observed by Stern and Gerlach in 1936
and the magnetic resonance method developed by Rabi and his team, which allowed for
the precise measurements of magnetic moments [2,3]. Despite early challenges, such as
Gorter’s unsuccessful attempts to detect NMR in solids due to long relaxation times, these
foundational experiments set the stage for further developments [1].
From the 1940s through the 1950s, significant strides in NMR technology were made.
Bloch and Purcell, working independently, were the first to detect NMR signals in bulk
matter, a discovery that earned them the Nobel Prize in Physics in 1952 [4,5]. Their work
revealed much shorter relaxation times than previously anticipated, marking a pivotal
moment in the understanding and application of NMR [6]. During this period, innovations
such as the use of short radiofrequency pulses to excite nuclear spins and the discovery
of spin echo by Hahn further refined NMR techniques, particularly in measuring the T1

Sensors 2024, 24, 5537. https://doi.org/10.3390/s24175537

https://www.mdpi.com/journal/sensors

## PDF page 2

Sensors 2024, 24, 5537

2 of 23

and T2 relaxation times [7–9]. These advances were crucial in developing a new theoretical
framework for NMR, including Bloch’s introduction of the relaxation times and the BPP
theory, which explained the effects of molecular motion on NMR signals [10,11].
The application of NMR has expanded rapidly with the discovery of chemical shifts
and scalar coupling. Early observations, such as the two distinct resonance signals in
14 N with NH NO and the identification of chemical shifts in various compounds, laid
3
4
the foundation for using NMR in the determination of chemical structures [12–15]. The
introduction of the term “chemical shift” by Herbert S. Gutowsky and the correlation of
shifts with structural features significantly impacted the utility of NMR in chemistry [16].
High-resolution NMR techniques revealed the multiplicity of chemically shifted signals,
further enhancing their application in structural analysis [17,18].
Dynamic nuclear polarization (DNP), discovered by Overhauser in 1953, and its
subsequent verification and application in the nuclear Overhauser effect (NOE) by Solomon,
provided new tools to enhance signal intensity in NMR, although these were not widely
recognized until later [19–21]. As NMR technology matured, commercial spectrometers,
such as those developed by Varian Associates, played a crucial role in making NMR more
accessible to the scientific community [22,23]. Advances such as the Fourier transform NMR
(FT-NMR) by Anderson and Ernst in the 1960s revolutionized data acquisition, allowing for
faster and more efficient analysis, which was recognized with a Nobel Prize in Chemistry
in 1991 [24].
NMR technology continued to advance through the 1970s and 1980s, with the development of two-dimensional (2D) NMR, proposed by Jean Jeener and advanced by
Richard Ernst [25,26]. These techniques allowed for more detailed structural analyses,
particularly in the study of biopolymers and complex molecules [27–29]. The integration of
computational methods and improvements in hardware and software further enhanced
the capabilities of NMR, making it a powerful tool for studying dynamic processes and the
structure of biological substances [30].
In the field of medicine, the application of NMR took a significant leap with the
introduction of magnetic resonance imaging (MRI) in the 1970s. The work of Lauterbur on
spatial encoding and Mansfield on echoplanar imaging (EPI) led to the development of
non-invasive diagnostic tools that revolutionized clinical medicine [31,32]. Solid-state NMR
(ssNMR) also advanced, enabling the study of complex solid materials such as biological
membranes and polymers [33,34].
The first Earth’s field NMR (EFNMR) was performed in 1954 [35,36]; it was a thing of
curiosity, and the main use was for geophysical magnetometry [37] or simply a low-cost
demonstration of magnetic resonance principles. Despite its low field, it continues to
attract the attention of researchers and engineers not only because of its rarity as a physical
phenomenon but also because of certain low-field results that are difficult to obtain in a high
field, such as the inflection obtained in the dependence of the inverse of T1 below 0.01 T of
the signal detected in some tissues [38], as well as other applications encountered [39,40].
The strength of the Earth’s magnetic field is very low. It is still possible to obtain narrow
NMR lines and a high signal-to-noise ratio with an acceptable spectral resolution. In the
1960s, Béné and colleagues demonstrated that EFNMR could measure the J-coupling of
nuclear elements [41]. Because high homogeneity and stability can be achieved successfully
in low fields, experiments have proven that many important spin multipliers can be studied
in low fields. Chemical shift differences have recently been demonstrated to be measured
even in inhomogeneous low magnetic fields [42].
This device presents several potential applications. One significant application is
the precise measurement of the chemical shift of hyperpolarized xenon-129 in the Earth’s
magnetic field, achieving a precision similar to high-field measurements [43]. Furthermore,
1 H and 19 F EFNMR spectra can be acquired with frequency resolutions nearly two orders of
magnitude better than those obtainable with high-field high-resolution NMR [44]. Another
application of the breakthrough was the observation of heteronuclear J-couplings using
the classic COSY experiment [45], and more recently, the first observation of homonuclear

## PDF page 3

Sensors 2024, 24, 5537

3 of 23

proton J-couplings in the Earth’s magnetic field, previously considered impossible [46].
In the realm of condensed matter physics, low-field NMR allows for high-resolution
spectra in solids by minimizing the line broadening caused by dipole–dipole interactions
in high fields [47]. Moreover, low magnetic fields allow for the observation of “forbidden
transitions”, providing unique information that is not detectable at high magnetic fields
Kohl et al. [48]. These applications highlight the versatility and potential of NMR in various
scientific fields.
2. Motivation and Objectives
NMR has proven to be an exceptionally valuable tool in a variety of disciplines, from
diagnostic medicine to chemical and biological research. However, most current NMR
spectrometers require intense magnetic fields, which limits their use to specialized laboratory environments. The development of an NMR spectrometer that can effectively operate
using the Earth’s magnetic field represents a significant pedagogical shift. This advancement could revolutionize the educational application of NMR, enabling its integration into
specialized NMR courses within the curriculum.
Current NMR equipment are prohibitively expensive for many institutions, especially
those in developing countries and organizations with limited budgets. Using the Earth’s
magnetic field, a more accessible NMR spectrometer can significantly reduce costs and
lower barriers to access, allowing for a much broader range of researchers to use this
valuable tool. However, its use is currently limited to educational purposes.
The potential applications of an Earth-field NMR spectrometer extend beyond traditional laboratories. There are numerous situations where access to conventional NMR
equipment is challenging or impossible, such as field research, low-resource environments,
or remote geographic regions. An Earth-field NMR spectrometer could enable on-site
analyses, provide real-time data, and eliminate the need for sample transportation. As
it can be transported, this has allowed us to carry out extensive research of diffusion in
explorations of Antartic ice and groundwater [49,50].
Research into an Earth-field NMR spectrometer also has the potential to deepen
our fundamental understanding of nuclear magnetic resonance. By working with much
lower magnetic field intensities than usual, we can gain new insights into the underlying
principles of NMR and uncover previously unobserved behaviors and properties. This
additional knowledge could open new avenues for research and application beyond the
purely educational purposes mentioned above.
The main objective of this paper is to design and construct an NMR spectrometer that
uses the Earth’s magnetic field as a constant magnetic field to operate. In addition, the aim
is to design systems that can generate acceptable and useful results under various operating
conditions. To evaluate the efficiency and effectiveness of the Earth-field NMR spectrometer,
its results are compared to those of conventional NMR spectrometers. One of the main
advantages of Earth-based NMR spectrometers is the ability to use NMR spectrometers
in situations where conventional NMR spectrometers cannot be used. Consequently,
spectrometers are designed and developed so that they are as portable, durable, and userfriendly as possible to be used in a wider range of environments. Data collected by Earth’s
field NMR spectrometers must be processed and analyzed. Herein, we developed robust
and user-friendly software systems to manage this process, simplify data interpretation,
and allow users to extract the maximum value from the results obtained.
3. Principle of Operation and General Aspects
Nuclear magnetic resonance (NMR) is a physical phenomenon in which atomic nuclei
in a magnetic field absorb and re-emit electromagnetic radiation. This process allows
for an investigation of the physical and chemical properties of the nucleus itself and its
surrounding environment.
Nuclear spin is a fundamental property of atomic nuclei related to the number of
protons and neutrons they contain. Some nuclei with specific properties, such as 1 H

## PDF page 4

Sensors 2024, 24, 5537

4 of 23

(protons), 13 C, 15 N, and 31 P, are NMR active, which means they have a nonzero spin
quantum number. This spin imparts a magnetic moment to them, turning them into tiny
magnetic bars.
In an NMR experiment, an external magnetic field, B0 , is applied. The magnetic moments of the nuclei align with the external field, but in quantum mechanics, this alignment
is quantized; Figure 1. This means that nuclear spins can align in specific orientations
dictated by their spin quantum number (ml ). For example, a nucleus with a spin quantum
number of 1/2 (such as 1 H or 13 C) has two possible spin states in an external magnetic
field: “spin-up” (ml = +1/2) or “spin-down” (ml = −1/2). These states have different
energies, with the spin-down state being the higher energy state.
B0

Figure 1. Energy levels considered before an external magnetic field B0 . Populations are generated
that are quantized with two energy levels.

The constant that relates the Larmor frequency to the applied magnetic field is called
the gyromagnetic constant, which, for 1 H, is 42.574 MHz/T. The energy levels produced
can be quantified as follows:
E I = hνI = hm I γ I B0

(1)

where E I is the energy level of the atom I, h is Planck’s constant, m I is the quantum spin
number, γ I is the gyromagnetic constant, and B0 is the external magnetic field. These
two energy levels are known as the alpha and beta states. For the hydrogen atom, the
energy levels (E I ) for a 600 MHz (14.1 T) spectrometer are around 2 × 10−25 J. The thermal
energy (ET ) that determines the population ratio of a partition distribution is around
4.1 × 10−21 J. Thus, the population associated with this energy state can be calculated
as follows:
1 (EI /ET )
1 m I hγ I B0
e
= e kb T
(2)
2
2
The population ratio for the different levels can be estimated by subtracting the energy
levels and dividing them by the sum of the two:
(

)

NI =

hγ I B0
−hγ I B0
)
(
N+1/2 − N−1/2
e kb T − e kb T
hγB0
hγB0
= hγ B
= tanh
≈
−hγ I B0
I 0
N+1/2 + N−1/2
2k
T
2k b T
b
e kb T + e kb T

(3)

## PDF page 5

Sensors 2024, 24, 5537

5 of 23

Equation (3) reveals that for a 600 MHz spectrometer at 288 K, the fraction of pop∆N±1/2
≈ 5 × 10−5 ; therefore, only a small fraction will have a net
ulations is around
N
magnetization M0 :
hγ
M0 = N
2

(

hγB0
2k b T

)

Cm VB0
=
T

( 2 2)
h γ
4R

(4)

where N is the total number of populations, Cm is the molar concentration of the nuclei
considered, V is the volume of the sample, B0 is the external magnetic field, and R is the
universal gas constant.
M0 is the projection on the Z-axis parallel to the external magnetic field, referred to as
the polarization in Mz of all spins, which defines the signal intensity in resonance. These
energy levels are called Zeeman energy levels and determine the magnetization parallel
to the external magnetic field (Figure 2). In NMR, a radiofrequency (RF) pulse is used to
perturb the nuclear spins from their equilibrium state. If this RF pulse matches the Larmor
frequency (a condition known as “on resonance”), the nuclear spins can absorb this energy
and “flip” from the lower-energy state to the higher one. Once the RF pulse is turned off,
the system will return to equilibrium, a process known as relaxation. During this process,
the nuclei will emit the absorbed energy in the form of an electromagnetic signal, which can
be detected and used to generate the NMR spectrum (Figure 2). The population difference
between the alpha and beta states is very small but sufficient to produce an observable
NMR signal, as explained previously. The system is in equilibrium when the ratio between
the populations of the alpha and beta states remains constant. In this state, there is no net
magnetization in the transverse plane (x-y). A short and intense burst of radiofrequency
(RF) radiation, called an RF pulse, is applied perpendicular to B0 . If this RF pulse matches
the Larmor frequency (the resonance frequency of the spins), the nuclear spins can absorb
this energy, causing a 90◦ flip of their alignment with B0 into the transverse plane (x-y).
This generates a net magnetization in the transverse plane, creating a non-equilibrium state
(Figure 2). It is a natural process based on the minimization of energy and maximization
of entropy; see Table 1. In NMR, this natural process is observed by minimizing the spin
energy and maximizing the nuclear spin phase.
Table 1. Model of equilibrium and non-equilibrium in the resonant process of nuclear spin.
Equilibrium
min(∆E − ∆ϕ)

Non-Equilibrium
max(∆E − ∆ϕ)

Mz = M0
Mx = 0
My = 0

Mz = M0 cos(ϕ p )
Mx = 0
My = M0 sin(ϕ p )

The variables involved in the spin perturbation process are the intensity of the radiofrequency pulse (BRF ), the phase value, and the duration of the pulse (τp ). The flip angle
of the Z-axis over the X-Y plane is determined as ϕ p = τp γBRF .
After turning off the RF pulse, the system does not remain in a non-equilibrium state.
The spins gradually return to their equilibrium alignment along the Z-axis, a process known
as relaxation. Relaxation occurs in two distinct processes: longitudinal relaxation (or T1 )
and transverse relaxation (or T2 ).
T1 relaxation is an enthalpic process where a net electromagnetic emission occurs,
producing a detectable signal as the system transitions from a non-equilibrium state to
equilibrium. Also known as spin-lattice relaxation, T1 relaxation is the process in which
the net magnetization vector in the transverse plane returns to the Z-axis. This process
is associated with the energy released by the spins as they return to equilibrium, causing
the nuclei to revert to their original energy states. The relaxation time T1 is a measure
of how quickly this process occurs. During this relaxation process, the detectable signal
mentioned earlier is observed as what is known as Free Induction Decay (FID). FID is

## PDF page 6

Sensors 2024, 24, 5537

6 of 23

the time-dependent signal generated by the precessing net magnetization vector in the
transverse plane immediately after the initial radiofrequency (RF) pulse is applied. As
the magnetization vector relaxes back to its equilibrium state along the Z-axis, the FID
signal decays exponentially, capturing the transition of the system back to equilibrium. The
physical model of relaxation can be mathematically expressed as follows:
Mz = Mz0 (1 − e−t/T1 )

(5)

Mx = Mx0 sin(tνH )e−t/T1

(6)

My = My0 cos(tνH )e−t/T1

(7)

Figure 2. (a) Spin population distribution before the application of an RF pulse or polarizing coil
in an external magnetic field Bo. Not all spins are aligned with Bo, leading to net magnetization.
(b) Spin population distribution after the application of the RF pulse or polarizing coil. The pulse
causes some spins to transition to a higher energy state, partially inverting the spin population, but
not all spins are fully inverted. This diagram reflects the Zeeman energy levels and the alignment
of nuclear spins with the external magnetic field. A radiofrequency (RF) pulse perturbs the nuclear
spins from their equilibrium state, which are “on resonance”.

Equation (5) shows what is called a coherent transition where photons are emitted,
resulting in a detectable signal. The relaxation T2 is an entropic process in which the
detectable signal has a phase among the different nuclear spins, producing relaxation in
the XY plane. Also known as spin–spin relaxation, T2 relaxation is the process by which
the spins in the XY plane dephase (i.e., lose their coherence). During this process, the
transverse magnetization decays to zero as a result of interactions between the spins. The
relaxation time T2 is a measure of the rate at which the transverse magnetization decays. A

## PDF page 7

Sensors 2024, 24, 5537

7 of 23

complete visualization of this relaxation process can be found in the following references
for different experiments [7,8,51,52].
Mz = Mz (1 − e−t/T1 )

(8)

Mx = Mx sin(tνH )e−t/T2

(9)

My = My cos(tνH )e−t/T2

(10)

This is the classical description of nuclear magnetization behavior developed by Bloch
in his vector model in the presence of an external magnetic field and following excitation
by an RF pulse. These equations, named after Felix Bloch, model nuclear spins as a bulk
magnetization vector and describe their precession and relaxation behaviors. Although
Bloch’s model is incredibly useful and has greatly contributed to our understanding of
NMR, it has several limitations.
•

•

•

•

•

•

Lack of quantum effects: Bloch equations are classical and do not account for quantum
mechanics effects. For example, they do not consider that the spin state of a nucleus
is quantized.
Assumption of a homogeneous magnetic field: The equations assume a perfectly
homogeneous external magnetic field. In reality, magnetic fields often exhibit inhomogeneities, which can lead to various effects not covered by Bloch equations.
Assumption of instantaneous excitation: The equations assume that the transition
from equilibrium to non-equilibrium (during the RF pulse) is instantaneous. In real
scenarios, the RF pulse has a finite duration, and its effect on the spin system might
not be as abrupt as assumed by Bloch equations.
Neglect of multiple spin interactions: Bloch’s model does not consider the interaction
of different spins with each other (spin–spin interactions), which can lead to more
complex phenomena such as relaxation and spin–spin coupling.
Assumption of large spin ensembles: Bloch equations consider the behavior of a spin
ensemble, thus providing average values. They do not provide information on the
behavior of individual spins within the ensemble.
Simplification of relaxation processes: The equations simplify relaxation processes (T1
and T2 ) to single exponential decays, whereas in reality these processes can involve
multiple components with different relaxation times.

Despite these limitations, the Bloch equations remain a fundamental tool in the understanding and interpretation of NMR, offering a simplified and efficient description of
many phenomena encountered in this field. However, for a more detailed understanding
of complex NMR phenomena, it is necessary to resort to quantum mechanical descriptions
or more advanced models.
Nuclear magnetic resonance in the geomagnetic field is known as Earth’s Field NMR
(EFNMR), a special case of low-field NMR. When a sample is placed in a uniform magnetic
field, nuclei with non-zero spin experience resonance at specific frequencies. This document
exclusively covers proton nuclear magnetic resonance (NMR), primarily involving the 1 H
isotope. Moreover, the experiments described in this study depend on the use of a polarizing coil to achieve the initial magnetization of the sample, which serves as an alternative
to the traditional RF excitation pulse commonly used in high-field NMR. This choice is
particularly important in the context of Earth-field NMR, where the magnetic field strength
is extremely low, and consequently, the thermal polarization of the spins is also weak. The
polarizing coil provides a stronger, more uniform magnetic field during the polarization
phase, effectively increasing the initial magnetization of the sample before signal detection.
This is very important in low-field conditions, where the natural magnetization would,
otherwise, be insufficient to produce a detectable signal. This device uses separate coils for
polarization and reception; each can be optimized independently for its specific function.
The polarizing coil is designed to generate a strong and uniform magnetic field, while
the receiving coil is optimized for maximum sensitivity and signal-to-noise ratio during

## PDF page 8

Sensors 2024, 24, 5537

8 of 23

detection. This approach enhances the overall performance of the NMR system. Utilizing
a dedicated polarizing coil helps to avoid potential artifacts or residual signals from the
excitation phase that could interfere with the detection phase. This results in cleaner and
more accurate signal acquisition, which is particularly important for reliable measurements
in an Earth-field NMR setup.
4. Materials and Methods
This document exclusively covers proton NMR, mainly involving the 1 H isotope. In
the Earth’s magnetic field, which is around 45,000 nT depending on the location, the 1 H
isotope has a Larmor frequency of approximately 2 kHz and generates a very weak signal
of a few microvolts.
Figure 3 shows the block diagram and the complete architecture of this EFNMR spectrometer. The polarizing coil assembly includes two receiver coils (Rx) that are connected in
an antiparallel configuration to cancel out environmental noise. The current flow through
the polarizing coil is managed by a regulated power supply, controlled by a polarizing
switch. The sample is placed inside one of the coils and the outputs of both Rx coils are fed
into a differential amplifier through a relay-controlled switch.

Polarization coil

Be

Reference coil

Receiver coil

Bp

S witch

Tunning

Differential
amplifier

S witch

Filters and Amplifiers

Amplifier

Bandpass
filter

Digitalization

Control

Figure 3. Block diagram of the electrotechnical device for nuclear spin excitation in the Earth’s
magnetic field. Bp and Be represent the polarization magnetic field and the Earth’s magnetic
field, respectively.

Given the small magnitude of the resonance signal, on the order of microvolts, signal
amplification is essential before further processing. Therefore, the signal is channeled
through a fixed-gain ultra-low noise differential amplifier and a low noise amplifier, and
then to a bandpass filter, with a cutoff frequency around the Larmor frequency, thus
eliminating unwanted noise and frequencies.
The filtered signal undergoes an additional amplification stage before being acquired
by the microcontroller Σ∆-ADC. Finally, signal processing is implemented on these data to
extrapolate and visualize the desired magnetic resonance information.

## PDF page 9

Sensors 2024, 24, 5537

9 of 23

4.1. CAD Design and 3D Printing

145.00

0
.0
90

80
.0
0

0
.0
32

28
.0
0

Three-dimensional printing is a very useful tool for prototyping. It allows for the
fabrication of parts designed using CAD programs. In this project, 3D printing has been
used to manufacture the cylinders on which the coils are wound and the base that holds
them, as well as other complementary parts that will be discussed below. To design the
parts used in this project, the CAD program was used. This software is a comprehensive 3D
design tool that combines parametric modeling, rendering, simulation, and computer-aided
manufacturing functions in a single integrated package.
The first part designed was the cylinder of the polarizing coil. This cylinder has a
height of 145 mm, an outer diameter of 90 mm, and an inner diameter of 80 mm. Two holes
with a diameter of 2 mm were made 20 mm from the base to allow the coil wire to pass
inside the cylinder. The second part designed was the cylinder of the receiving coils. This
cylinder has a height of 140 mm, an outer diameter of 32 mm, and an inner diameter of
28 mm. Similarly to the polarizing coil cylinder, this cylinder also has two holes made
20 mm from the base, but this time with a diameter of 1.5 mm to allow for the coil wires to
pass inside the cylinders. Figure 4 shows the CAD design of the polarizing coil and the
receiving coil cylinders.

145.00

Figure 4. CAD design of the polarizing and receiving coil cylinders.

The three coils are aligned by means of a base that has grooves 15 mm deep and a
width equivalent to the thickness of the walls of the cylinders where each of the coils is
fitted, and this same base aligns the wires of connection of the coils to match the connections
of the printed circuit.
In order to be able to modify the inclination of the coils, and to be able to align the
terrestrial magnetic field in an optimal way, a support was designed, which holds the
excitation coil and allows one to modify the angle with the base. The base of the equipment
has a curved surface where the support can slide and two fixing screws, which allow us to
secure the mounting in the desired position. The fixing screws used are plastic, so there is
no need for any metal component that could alter the magnetic field near the coil. Figure 5
shows the CAD design of the various parts and the assembled model.
Once the design of all parts in CAD is completed, the files are transferred to a G-code
translator. This kind of software is a sophisticated 3D model preparation software that
enables the configuration and optimization of printing parameters. This process is essential
before generating the G-code file required for 3D printing. The final result after the CAD
design and printing is shown in Figure 6.

## PDF page 10

Sensors 2024, 24, 5537

10 of 23

Figure 5. CAD design of the bases that support the coils and assembled model.

Figure 6. The 3D-printed parts with PETG and Nylon M10 threads

4.2. Polarizing Coil
The polarizing coil temporarily creates a polarizing magnetic field B p . This field
quickly turns off, leaving the magnetization instantly perpendicular to the Earth’s magnetic field around which precession begins [53,54]. The polarizing coil and its supporting

## PDF page 11

Sensors 2024, 24, 5537

11 of 23

structure must not contain any ferromagnetic material, see Figure 7 . Naturally, the Earth’s
field is very homogeneous, and if there is any ferromagnetic material near the coil, it will
change the uniformity of the field, causing magnetic field inhomogeneities. To properly use
the device during normal experiments, the entire system should be free of electromagnetic
interference due to the weakness of the detected signal. However, since the goal of this
project is to design a benchtop device, it has been designed to be robust under electromagnetic stress conditions. The purpose of the polarizing coil is to produce a magnetic
field much greater than the Earth’s magnetic field. To polarize the sample, a current of
approximately 10 A is passed through the coil for 10 s. Therefore, the wire for winding the
polarizing coil must have a large-enough cross-section to avoid heating while carrying this
current. The specifications chosen for the polarizing coil are given in Table 2.
Table 2. Specifications of the polarizing coil.
Coil

Specification

Enameled copper wire
Inner diameter of the coil
Outer diameter of the coil
Height of the coil
Number of wire layers
Number of turns per layer
Approximate inductance
Approximate resistance

1.7 mm or 14 AWG
80 mm
90 mm
145 mm
3
60
3.4 mH
0.8 Ω

The polarizing coil cylinder is wound on a commercial PVC (vinyl polychloride) tube.
The polarizing coil is placed in the center of the coil holder, which is provided with holes
for passing the connections to the PCB, placed under this holder. The base, inclination
part, and coil support are made of PETG, avoiding the use of metal. The tilt platform
should form an angle close to 50◦ relative to the base. The angle ensures that when B p is
turned off, the magnetization is perpendicular to the Earth’s field immediately prior to
signal detection. This geometrical arrangement maximizes the strength of the signal. The
Earth field in southern Spain (University of Almeria) has an inclination of 50.57◦ and a
declination of 0.59◦ .

Figure 7. Wounded polarizing coil.

## PDF page 12

Sensors 2024, 24, 5537

12 of 23

4.3. Receiver Coils (Antenna)
The receiving coils (R x ) are responsible for collecting the signal from the polarized
sample in precession. The signal is extremely low, requiring many iterations of the experiment to increase the signal-to-noise ratio (SNR). This process is known as signal averaging.
The main problem affecting this device is noise, which is why the coils have been designed
to minimize it. In addition to signal averaging, two nearly identical sensor coils are used to
address this issue and maximize the SNR.
The two coils are wound in series but in opposite directions and placed on the same
surface to cancel out noise (Figure 8). A real receiver coils built is shown in the Figure 9,
this receiver coil is designed according its test tube. To receive the signal, the sample is
placed in only one of the coils because if it is placed in both coils, the produced signals will
cancel each other out, resulting in no signal being received at the output.

Figure 8. Winding diagram of the receiver coils.

The most important requirement for correct winding is that both coils must be as
identical as possible to perfectly cancel out environmental noise. This is called commonmode rejection and can be achieved if the number of turns is equal for both coils and the
wire is not twisted at any point during winding. To verify the similarity of the coils, one
method is to weigh the coils before and after winding. As with the polarizing coil, the
material used for the cylinders on which the receiving coils are wound is a commercial
PVC pipe.

Figure 9. Wounded receiver coil and test tube.

## PDF page 13

Sensors 2024, 24, 5537

13 of 23

As mentioned earlier, the device was designed to operate using the Earth’s magnetic
field, so any nearby ferromagnetic material must be avoided. Metallic objects such as
copper, aluminum, and brass should also be kept away from the coil to avoid induced eddy
currents when B p is quickly turned off.
The wire’s cross-section is also an important parameter. With a thin wire, we have
more turns and √
a stronger signal, but it also has higher resistance and, therefore, more
Johnson noise ∝ R, which we do not want. On the other hand, with a thick wire, we have
fewer turns and a weaker signal compared to a thin wire, but the noise is lower and the
quality factor can be higher. The thermal noise follows the resistance relationship in volts:
VT =

√

4K B TR∆ f

(11)

where K B is Boltzmann’s constant (J/K), T is the temperature in K, R is the resistance, and
∆ f is the bandwidth. The specifications of the receiving coils are summarized in Table 3.
Table 3. Specifications of the receiver coil.
Coil

Specification

Enameled copper wire
Inner diameter of the coil
Outer diameter of the coil
Height of the coil
Number of wire layers
Number of turns per layer
Approximate inductance per coil
Approximate resistance per coil

0.812 mm or 21 AWG
25 mm
40 mm
100 mm
4
115
2.56 mH
2.5 Ω

To verify the proper functioning of the receiving coils, some preliminary tests were
conducted. The coils were placed inside the polarizing coil, and a sinusoidal signal was applied to the polarizing coil using a function generator (Figure 10). This induces a sinusoidal
wave in both receiving coils of the same amplitude and is approximately 180 degrees out of
phase with the excitation source. Both waves cancel each other out, resulting in an almost
null signal. All these signals were measured and analyzed in Matlab (Figure 11).

Figure 10. Testing of receiver coils in the electrotechnical laboratory .

## PDF page 14

Sensors 2024, 24, 5537

14 of 23

Figure 11. Test results give a good response of the avoiding signal between both coils. Only a little
180◦ dephased signal was measured, which ensures the cancelation of the signals.

4.4. Power Circuit
This circuit is responsible for turning the power supply of the polarizing coil on and
off with a signal from the microcontroller. This circuit had to be carefully designed because,
for the experiment to work correctly, the coil needs to discharge as quickly as possible, and
consequently, so does the magnetic field it generates. Therefore, no switch can be used to
turn off the polarizing coil. Mechanical relays could be used to turn the polarizing coil on
and off, but they are not the best option due to several disadvantages. The relay operates
like a basic switch and can produce an electric arc when it is turned off, as the coil has
high induced voltages. Relays also have a short lifespan and take a few milliseconds to
switch. In our case, the polarizing coil needs to be turned on and off within microseconds.
Therefore, the simplest solution to this problem is to use a power MOSFET with a shorter
switching time.
The MOSFET used is the IPD090N03L. The maximum allowed collector-emitter voltage is 30 V, and the base-emitter voltage is 20 V. The maximum current it can drain is 40 A.
The IPD090N03L has an extremely low internal on-resistance of 0.009 Ω. The positive power
supply of +12 V is connected to one terminal of the polarizing coil, while the other terminal
is connected to the MOSFET’s collector. The MOSFET emitter is connected to the ground.
The MOSFET is operated by the microcontroller through a specific driver that boosts the
voltage and current provided by the microcontroller to levels that ensure fast switching
with the least amount of losses possible. Because high voltages are induced during the
switching of the MOSFET, it is important to include a diode that absorbs these surges
without damaging the MOSFET. Given the low resistance of the MOSFET, the amount of
heat generated during switching can be dissipated by the PCB itself. The complete circuit
schematic can be seen in Figure 12.

Figure 12. Circuit schematic of excitation coil control.

## PDF page 15

Sensors 2024, 24, 5537

15 of 23

4.5. Receiver Circuit
The signal detected by the receiver coils is extremely small (on the order of microvolts).
This signal needs to be converted by the microcontroller ADC to be processed by a computer,
but it needs to be adapted; for this purpose, six different stages are designed as shown
in Figure 13.

Figure 13. Block diagram of the amplification and filtering circuit.

The first stage is a capacitor block. These capacitors act as tuners and are responsible
for enhancing the signal before it reaches the instrumentation amplifier. This is achieved by
placing these capacitors in parallel with the receiving coil. The value of the capacitor can
be found using the resonant frequency formula, Formula (12).
f =

1
√

2π LC

(12)

The frequency f is adjusted (adjusting C) to be as close as possible to the Larmor
frequency of the proton, which is approximately 2 KHz. Here, L is the combined inductance
of both coils, and its value is 5.12 mH. The optimal value of the tuning capacitor is 1.13 µF.
This value is approximated by 1 µF and two 56 nF.
The second stage is a double relay controlled through the microcontroller that connects
the output of the coils. The normal position of the relay switches is open. Each end of
the receiving coils is connected to one of the relay switches, while the common point of
the two coils is connected to the ground. When the microcontroller sends a signal to the
transistor, it connects the relays to the +5 V power supply, causing the relay switches to
activate, allowing the signal from the receiving coils to pass to the instrumentation amplifier.
The circuit is shown in Figure 14.

Figure 14. Switching amplification and filtering input stages circuit.

Third, there is an ultra-low-noise instrumentation preamplifier. An INA848 is used,
which is a high-precision instrumentation amplifier that requires no external components
for a fixed gain of 2000. Since the signal is in microvolts, only low-noise amplifiers can be
used. Both ends of the coils are connected to the input of the instrumentation amplifier,
while the sample is placed in only one of the coils, as mentioned earlier. When the signal
arrives, the signals from the two inputs of the instrumentation amplifier are subtracted,
and the signal emitted by the proton is obtained.

## PDF page 16

Sensors 2024, 24, 5537

16 of 23

The fourth stage is an amplifier stage, with a gain of 1000, built with one of the
four operational amplifiers available in the OPA4189. In the fifth stage, signal filtering
is performed, using the remaining three amplifiers to perform a band-pass filter of order
6, designed to attenuate the frequencies outside the range of interest for this application.
Specifically, 1.8 kHz center frequency and a width of 1.5 kHz have been chosen. The filter
response is shown in Figure 15.

Figure 15. Filter stage frequency response. Blue band shadow includes components’ tolerances.

The last stage transforms the signal to a differential mode and adapts the impedance
values to those expected by the 16-bit ADC incorporated in the microcontroller. In this stage,
the signal is shifted from referenced to GND to swing around Vre f /2, which is required to
meet the input ranges of the ADC. Both the reference voltage and Vre f /2 are supplied by a
precision voltage reference, in this case a REF2025.
The differential mode used significantly improves the conversion by increasing the
noise immunity. No gain is introduced at this stage, so the total system gain is 2,000,000.
The complete input schematic is shown in Figure 14.
4.6. Acquisition Sequence
The quality of the data obtained is strongly dependent on the precise timing of the
different stages involved in the process. By design, this device alternates between the
excitation stage, in which the polarizing coil is involved, and the relaxation stage, in
which the receiver coils are involved. In this case, the acquisition process is fixed, and the
timing parameters and the number of repetitions can be configured at the beginning of
each experiment.
At the beginning of each scan of the experiment, the microcontroller activates the
current conduction to the biasing coil. After the excitation time (τ1 ), the coil is turned
off. Once a preset time (τ2 ) has elapsed, which is necessary for the field of the biasing
coil to discharge, the relay closes and the receiver coils are connected to the amplifiers.
Digitization begins after a second period (τ2 ), which ensures complete closure of the relay,
the duration of which varies according to the number of samples required (τ3 ). At the
end of the sampling, the relay opens and waits for the relaxation time (τ4 ). This process is
repeated for the indicated number of times, improving the system’s ability to distinguish
signal from noise.
Figure 16 details the temporal sequence that the device follows during each operation
cycle. The time intervals associated with each phase of the sequence are detailed in Table 4.

## PDF page 17

Sensors 2024, 24, 5537

17 of 23

Figure 16. Sequence of pulses followed by the device as a function of time.
Table 4. Times for each stage of the sequence.
Stage

Symbol

Minimum

Maximum

Default

Polarizing coil activated
Pre-acquisition
Acquisition
Acquisition sample rate
Waiting between
experiments
Number of scans

τ1
τ2
τ3
-

1s
1000 samples
-

32 s
5,000,000 samples
-

10 s
100 ms
250,000 samples
50,000 SPS

τ4

1s

32 s

5s

N

1

5000

650

4.7. Control and Communications
The control tasks of the equipment, the digitalization of the amplified and adapted
signals in the previous section, and the communication with a computer are handled by
an ARM microcontroller (STM32F373). This microcontroller has the required features for
the correct operation of the unit, including a 16-bit-resolution analog–digital converter and
USB communication for sending the large number of samples that need to be acquired.
Of course, it has diverse input and output pins, timers, and SPI and I2C communication
ports, among others. To enable USB communication, it is required to use a 72 MHz clock
frequency obtained from an 8 MHz crystal and the internal PLL.
The required design is simple, having only the outputs corresponding to the activation
of the polarizing coil and the relay, the analog inputs for the signal, and a communication
port with the computer. The rest of the elements are auxiliary to achieve the correct
operation of the instrument. Figure 17 shows the microcontroller section as well as the rest
of the auxiliary elements of the circuit.
Since the coils need to be properly aligned with the terrestrial magnetic field, a 3-axis
magnetometer is also incorporated, which is accessed by the microcontroller via the I2C
bus. As the PCB is precisely aligned with the coils, it is convenient and practical to be able
to use this magnetometer to adjust the position before starting the measurements, ensuring
better results. The read values are visible from the program interface.

## PDF page 18

Sensors 2024, 24, 5537

18 of 23

Figure 17. Microcontroller schematic and auxiliary components.

4.8. Computer Software
To ensure proper use of the unit, we developed basic control software in C#. This
language for programming was chosen because it is driven by the extensive library support
and the language’s ease of use, facilitating the enhancement and swift implementation of
new experiments and functionalities. The main window (Figure 18) presents configurable
experimental parameters, enabling the user to adjust the settings as required.
•

•
•
•

The number of samples to capture; according to this number and taking into account
the fixed sampling frequency, the duration of this period is indicated, corresponding
to τ3 .
Number of scans or number of times the acquisition cycle will be repeated. Corresponds to the parameter N.
Recovery time, or time required after acquisition until a new cycle starts. Corresponds
to τ4 .
Pulse time or polarizing coil activation time. Corresponding to τ1 .

Figure 18. The main window of the computer software is divided into two parts. On the left side,
there is a control panel with textboxes and buttons for managing the acquisition process. On the
right side, there is a primary plot window that displays either the detected signal or its Fast Fourier
Transform (FFT) analysis.

## PDF page 19

Sensors 2024, 24, 5537

19 of 23

Although the software is intended to test the functionality of the machine, the ability
to model the noise is incorporated, saving the results and allowing one to improve the
behavior in subsequent experiments. This function is performed by running one or more
scans without introducing any sample. The frequency response (FFT) obtained is stored in a
file and used subsequently to suppress the background noise. The software also allows you
to switch between the Fast Fourier Transform view (FFT) and the free-induction decay view.
4.9. Cost Analysis
The cost of the manufactured device is minimized due to its basic design and the use
of readily available and inexpensive components. This approach ensures that the overall
cost remains low while fulfilling the necessary functionality and performance requirements.
The use of standard materials and simple manufacturing processes further enhances the
cost effectiveness of the machine (see Table 5).
Table 5. Cost breakdown of EFRMN device components.
Item
PETG Filament
PCB Fabrication
Components
Copper Wire 1.7 MM
Copper Wire 0.8 MM
Wiring
Power supply

Quantity

Cost

1 kg
70 m
120 m
1

24 €
10 €
100 €
30 €
25 €
10 €
30 €

Total

229 €

5. Results and Discussion
In this study, we successfully designed and built a complete assembly and electronic
component EFNMR spectrometer from scratch. All parts, including the spectrometer
framework, were manufactured with PETG material and 3D-printing technology with
CAD design and 3D printing to ensure the device’s robust and accurate structure.
The electronic system includes a custom coil to generate the required magnetic field
and a sensitive receiver coil to detect NMR signals. The STM32F373 microcontroller was
used to control pulse sequences and read Analog–Digital Converter (ADC) signals from
the receiver. This controller provides the computational power and flexibility necessary for
accurate timing and signal processing. In Figure 19 is shown the successfully assembled device, integrating all components into a fully functional and cohesive EFNMR spectrometer.

Figure 19. The final device was successfully assembled, integrating all components into a cohesive
and fully functional EFNMR spectrometer.

The control software has a user-friendly interface and is written in C#. This C# application can be visualized in Figures 18 and 20. This interface facilitates easy interaction with

## PDF page 20

Sensors 2024, 24, 5537

20 of 23

EFNMR spectrometers, allowing users to configure experimental parameters, begin measuring, and analyze the results. The software is designed to focus on simplicity and accessibility
and enable users of different levels of expertise to use the spectrometer effectively.

Figure 20. 1 H MR spectrum test was successfully conducted. The magnetometer detected a magnetic
field strength of 37.10 µT, resulting in a resonance frequency of 1579 Hz for the 1 H nuclei.

All aspects of the project, including electronic designs, coil specifications, and control
software, have been made available as open source resources on GitHub, https://github.
com/fmarrabal/Earth-Field-NMR (accessed on 18 July 2024). This ensures that other
researchers and enthusiasts can replicate, modify, and improve our work, fostering further
advancements in the field of EFNMR spectroscopy.
The system was tested using standard samples, and the results demonstrated the
capability of our EFNMR spectrometer to produce a 1 H NMR spectrum. The results indicate
that our EFNMR spectrometer can serve as a powerful tool for a wide range of applications,
including chemical analysis, geophysical exploration, and educational purposes. Figure 20
shows a clear signal peak at approximately 1579 Hz, which is an expected result for Earthfield NMR. However, the baseline noise is quite prominent, suggesting that the overall
SNR is low. The noise appears to be relatively high compared to the signal peak. In an ideal
NMR experiment, the signal should stand out distinctly above the noise floor. Here, the
noise level is only marginally lower than the intensity of the peak, which implies that the
SNR could be improved. In Earth-field NMR, the sensitivity is inherently lower than in
high-field NMR because of the significantly smaller magnetic field strength. This leads to a
reduced net magnetization, which directly impacts the strength of the detected signal. To
improve the sensitivity, it is possible to perform the following:
•
•
•

Increase the number of scans: averaging more scans can improve the SNR by reducing
random noise.
Optimize pulse parameters: adjusting pulse times and recovery times to ensure the
optimal alignment of the spins prior to detection can enhance the signal.
Signal averaging and background subtraction: techniques such as averaging multiple
acquisitions and subtracting background noise can also be helpful in enhancing the
detectable signal.

## PDF page 21

Sensors 2024, 24, 5537

21 of 23

•

Magnetization enhancement techniques: implementing techniques such as hyperpolarization or using stronger polarizing coils might also improve initial magnetization,
thus increasing the signal intensity.

This device and software are designed to optimize sensitivity through a variety of
advanced techniques. They are capable of setting the number of scans to improve the
signal-to-noise ratio (SNR) by averaging multiple acquisitions, thus reducing random noise.
The system can also fine-tune pulse times and recovery periods to ensure optimal spin
alignment before detection, which enhances the detected signal’s strength. In addition, the
software facilitates signal processing methods, such as background subtraction and realtime signal averaging, to further enhance the clarity of the detected peaks. Although these
capabilities significantly improve the sensitivity of the NMR measurements, it is important
to note that the system does not incorporate magnetization enhancement techniques, which
would require external interventions beyond the microcontroller and software scope.
In summary, the development of this EFNMR spectrometer demonstrates the feasibility
of constructing high-quality, low-cost NMR systems using readily available materials and
open-source technology. Our work lays the foundation for future innovations in portable
and accessible NMR spectroscopy oriented to AI-enhanced low-field NMR technology.
Author Contributions: F.M.A.-C. and I.F.; methodology, F.M.A.-C., E.V. and J.A.M.-L.; software,
F.M.A.-C. and E.V.; validation, I.F.; formal analysis, I.F.; investigation, E.L.-L.; resources, E.L.-L.; data
curation, E.L.-L.; writing—original draft preparation, F.M.A.-C. and I.F.; writing—review and editing,
F.M.A.-C. and I.F.; visualization, E.V. and E.L.-L.; supervision, J.A.M.-L.; project administration,
F.M.A.-C. and I.F.; funding acquisition, F.M.A.-C. and I.F. All authors have read and agreed to the
published version of the manuscript.
Funding: This research was funded by the State Research Agency of the Spanish Ministry of Science
and Innovation (PID2021-126445OB-I00), and by the Gobierno de España MCIN/AEI/10.13039
/501100011033 and Unión Europea “Next Generation EU”/PRTR (PDC2021-121248-I00, PLEC2021007774 and CPP2022-009967).
Institutional Review Board Statement: Not applicable.
Informed Consent Statement: Not applicable.
Data Availability Statement: The repository https://github.com/fmarrabal/Earth-Field-NMR
(accessed on 18 July 2024) provides complete device schematics, PCB design, microcontroller firmware,
and computer software for the device.
Conflicts of Interest: The authors declare no conflicts of interest.

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

Becker, E.D.; Fisk, C.L.; Khetrapal, C.L. The Development of NMR. In Encyclopaedia of Nuclear Magnetic Resonance; Grant, D.M.,
Harris, R.K., Eds.; Wiley: Chichester, NJ, USA, 1996; Volume 1, pp. 1–158. [CrossRef]
Gerlach, W.; Stern, O. Experimentelle Prüfung der Richtungsquantelung im Magnetfeld. Z. Phys. 1922, 9, 349–352. [CrossRef]
Rabi, I.I.; Zacharias, J.R.; Millman, S.; Kusch, P. A New Method of Measuring Nuclear Magnetic Moment. Phys. Rev. 1938, 53, 318. [CrossRef]
Purcell, E.M.; Torrey, H.C.; Pound, R.V. Resonance Absorption by Nuclear Magnetic Moments in a Solid. Phys. Rev. 1946, 69, 37. [CrossRef]
Bloch, F.; Hansen, W.W.; Packard, M.E. Nuclear Induction. Phys. Rev. 1946, 69, 127. [CrossRef]
Heitler, W.; Teller, E. Time effects in the magnetic cooling method. Proc. R. Soc. London. Ser. A 1936, 155, 62. [CrossRef]
Hahn, E.L. Spin Echoes. Phys. Rev. 1950, 80, 580–594. [CrossRef]
Carr, H.Y.; Purcell, E.M. Effects of Diffusion on Free Precession in Nuclear Magnetic Resonance Experiments. Phys. Rev. 1954,
94, 630. [CrossRef]
Meiboom, S.; Gill, D. Modified Spin-Echo Method for Measuring Nuclear Relaxation Times. Rev. Sci. Instruments 1958, 29, 688. [CrossRef]
Bloch, F. Nuclear Induction. Phys. Rev. 1946, 70, 460–474. [CrossRef]
Bloembergen, N.; Purcell, E.M.; Pound, R.V. Relaxation Effects in Nuclear Magnetic Resonance Absorption. Phys. Rev. 1948,
73, 679. [CrossRef]
Proctor, W.G.; Yu, F.C. The Dependence of a Nuclear Magnetic Resonance Frequency upon Chemical Compound. Phys. Rev. 1950,
77, 717. [CrossRef]
Dickinson, W.C. Dependence of the F19 Nuclear Resonance Position on Chemical Compound. Phys. Rev. 1950, 77, 736–737. [CrossRef]
Knight, W.D. Nuclear Magnetic Resonance Shift in Metals. Phys. Rev. 1949, 76, 1259–1260. [CrossRef]

## PDF page 22

Sensors 2024, 24, 5537

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

22 of 23

Arnold, J.T.; Dharmatti, S.S.; Packard, M.E. Chemical Effects on Nuclear Induction Signals from Organic Compounds. J. Chem.
Phys. 1951, 19, 507. [CrossRef]
Meyer, L.H.; Saika, A.; Gutowsky, H.S. Electron Distribution in Molecules. III. The Proton Magnetic Spectra of Simple Organic
Groups1. J. Am. Chem. Soc. 1953, 75, 4567. [CrossRef]
Proctor, W.G.; Yu, F.C. On the Nuclear Magnetic Moments of Several Stable Isotopes. Phys. Rev. 1951, 81, 20–30. [CrossRef]
Gutowsky, H.S.; McCall, D.W. Nuclear Magnetic Resonance Fine Structure in Liquids. Phys. Rev. 1951, 82, 748–749. [CrossRef]
Overhauser, A.W. Polarization of Nuclei in Metals. Phys. Rev. 1953, 92, 411–415. [CrossRef]
Carver, T.R.; Slichter, C.P. Polarization of Nuclear Spins in Metals. Phys. Rev. 1953, 92, 212–213. [CrossRef]
Solomon, I. Relaxation Processes in a System of Two Spins. Phys. Rev. 1955, 99, 559–565. [CrossRef]
Freeman, R.; Morris, G.A. The Varian story. J. Magn. Reson. 2015, 250, 80. [CrossRef]
Shoolery, J.N. The development of experimental and analytical high resolution NMR. Prog. Nucl. Magn. Reson. Spectrosc. 1995,
28, 37. [CrossRef]
Corey, E.J.; Burke, H.J.; Remers, W.A. Distinction between Cycloheptatriene and Bicycloheptadiene Structures by Nuclear
Magnetic Resonance. J. Am. Chem. Soc. 1955, 77, 4941. [CrossRef]
Müller, L.; Kumar, A.; Ernst, R.R. Two-Dimensional Carbon-13 NMR Spectroscopy. J. Chem. Phys. 1975, 63, 5490–5491. [CrossRef]
Aue, W.P.; Bartholdi, E.; Ernst, R.R. Two-dimensional Spectroscopy. Application to Nuclear Magnetic Resonance. J. Chem. Phys.
1976, 64, 2229. [CrossRef]
Andrew, E.R.; Szczesniak, E. A Historical Account of NMR in the Solid State. Prog. Nucl. Magn. Reson. Spectrosc. 1995, 28, 11–36. [CrossRef]
Bodenhausen, G.; Ruben, D.J. Natural Abundance Nitrogen-15 NMR by Enhanced Polarization Transfer. Chem. Phys. Lett. 1980,
69, 185. [CrossRef]
Bax, A.; Griffey, R.H.; Hawkins, B.L. Correlation of Proton and Nitrogen-15 Chemical Shifts by Multiple Quantum NMR. J. Magn.
Reson. 1983, 55, 301. [CrossRef]
Sugiki, T.; Kobayashi, N.; Fujiwara, T. Modern Technologies of Solution Nuclear Magnetic Resonance Spectroscopy for Three-dimensional
Structure Determination of Proteins Open Avenues for Life Scientists. Comput. Struct. Biotechnol. J. 2017, 15, 328. [CrossRef]
Lauterbur, P.C. Image Formation by Induced Local Interactions: Examples of Employing Nuclear Magnetic Resonance. Nature
1973, 242, 190–191. [CrossRef]
Mansfield, P. Multi-Planar Image Formation Using NMR Spin Echoes. J. Phys. C Solid State Phys. 1977, 10, L55. [CrossRef]
Alam, T.M.; Jenkins, J.E. HR-MAS NMR Spectroscopy in Material Science; IntechOpen, London, UK, 2012 ; pp. 279–306. [CrossRef]
Reimer, J.A. Development of NMR: Solid-State NMR and Materials Science, Post 1995. In Encyclopaedia of Nuclear Magnetic
Resonance; Grant, D.M., Harris, R.K., Eds.; Wiley: Chichester, UK, 2012; Volume 1, pp. 457–472. [CrossRef]
Packard, M.; Varian, R. Free Induction in the Earth’s Magnetic Field. In American Physical Society Minutes of the Stanford Meeting
December 28, 29, and 30, 1953; Kaplan, J., Ed.; American Chemical Society (ACS): Washington, DC, USA, 1954; Volume 93,
p. Abstract A7.
Waters, G.S. A Measurement of the Earth’s Magnetic Field by Nuclear Induction. Nature 1955, 176, 691. [CrossRef]
Courtillot, V.; Le Mouël, J. The study of Earth’s magnetism (1269–1950): A foundation by Peregrinus and subsequent development
of geomagnetism and paleomagnetism. Rev. Geophys. 2007, 45, 1–31. [CrossRef]
Koenig, S.H.; Brown, R.D.; Adams, D.; Emerson, D.; Harrison, C.G. Magnetic Field Dependence of 1/T1 of Protons in Tissue.
Investig. Radiol. 1984, 19, 76–81. [CrossRef]
Balcı, E.; Rameev, B.; Acar, H.; Mozzhukhin, G.V.; Aktaş, B.; Çolak, B.; Kupriyanov, P.A.; Ievlev, A.V.; Chernyshev, Y.S.; Chizhik,
V.I. Development of Earth’s Field Nuclear Magnetic Resonance (EFNMR) Technique for Applications in Security Scanning
Devices. Appl. Magn. Reson. 2016, 47, 87–99. [CrossRef]
Sato-Akaba, H.; Itozaki, H. Development of the Earth’s Field NMR Spectrometer for Liquid Screening. Appl. Magn. Reson. 2012,
43, 579–589. [CrossRef]
Duval, E.; Ranft, J.; Béné, G. Détermination des signes relatifs des constantes de couplage 31 P- 1 H dans le tripropyl phosphate
par R.M.N. dans le champ magnétique terrestre. Mol. Phys. 1965, 9, 427–431. [CrossRef]
Meriles, C.A.; Sakellariou, D.; Heise, H.; Moule, A.J.; Pines, A. Approach to High-Resolution ex Situ NMR Spectroscopy. Science
2001, 293, 82–85. [CrossRef] [PubMed]
Appelt, S.; Häsing, F.W.; Kühn, H.; Perlo, J.; Blümich, B. Mobile High Resolution Xenon Nuclear Magnetic Resonance Spectroscopy
in the Earth’s Magnetic Field. Phys. Rev. Lett. 2005, 94, 197602. [CrossRef]
Appelt, S.; Kühn, H.; Häsing, F.W.; Blümich, B. Chemical analysis by ultrahigh-resolution nuclear magnetic resonance in the
Earth’s magnetic field. Nat. Phys. 2006, 2, 105–109. [CrossRef]
Robinson, J.N.; Coy, A.; Dykstra, R.; Eccles, C.D.; Hunter, M.W.; Callaghan, P.T. Two-dimensional NMR spectroscopy in Earth’s
magnetic field. J. Magn. Reson. 2006, 182, 343–347. [CrossRef] [PubMed]
Appelt, S.; Häsing, F.W.; Kühn, H.; Sieling, U.; Blümich, B. Analysis of molecular structures by homo- and hetero-nuclear
J-coupled NMR in ultra-low field. Chem. Phys. Lett. 2007, 440, 308–312. [CrossRef]
Zax, D.B.; Bielecki, A.; Zilm, K.W.; Pines, A.; Weitekamp, D.P. Zero field NMR and NQR. J. Chem. Phys. 1985, 83, 4877–4905. [CrossRef]
Kohl, M.; Odehnal, M.; Petříěek, V.; Tichý, R.; Šafrata, S. Observation of higher order NMR larmor lines by SQUID in solids at
low magnetic field. J. Low Temp. Phys. 1988, 72, 319–343. [CrossRef]

## PDF page 23

Sensors 2024, 24, 5537

49.
50.
51.
52.
53.
54.

23 of 23

Hunter, M.W.; Dykstra, R.; Lim, M.H.; Haskell, T.G.; Callaghan, P.T. Using Earth’s Field NMR to Study Brine Content in Antarctic
Sea Ice: Comparison with Salinity and Temperature Estimates. Appl. Magn. Reson. 2009, 36, 1–8. [CrossRef]
Callaghan, P.; Eccles, C. NMR studies on Antarctic sea ice. Bull. Magn. Reson. 1996, 18, 62–64.
Anderson, A.G.; Garwin, R.L.; Hahn, E.L.; Horton, J.W.; Tucker, G.L.; Walker, R.M. Spin echo serial storage memory. J. Appl. Phys.
1955, 26, 1324–1338. [CrossRef]
Hahn, E.L. Nuclear induction due to free larmor precession. Phys. Rev. 1950, 77, 297–298. [CrossRef]
Melton, B.F.; Pollak, V.L.; Mayes, T.W.; Willis, B. Condition for Sudden Passage in the Earth’s-Field NMR Technique. J. Magn.
Reson. Ser. A 1995, 122, 164–170. [CrossRef]
NOAA National Centers for Environmental Information. Geomagnetic Calculators. 2023. Available online: https://www.ngdc.
noaa.gov/geomag/calculators/magcalc.shtml?useFullSite=true (accessed on 18 July 2024).

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
