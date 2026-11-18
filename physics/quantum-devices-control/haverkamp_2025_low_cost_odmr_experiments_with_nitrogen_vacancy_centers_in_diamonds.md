Source: see manifest row of the PDF
PDF sha256: e4b967dbc2e47781b2a731249a569281c542f113644a3d158d78f6062917d36d
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of haverkamp_2025_low_cost_odmr_experiments_with_nitrogen_vacancy_centers_in_diamonds.pdf

Transcription of `haverkamp_2025_low_cost_odmr_experiments_with_nitrogen_vacancy_centers_in_diamonds.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-19 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Haverkamp et al. EPJ Quantum Technology
https://doi.org/10.1140/epjqt/s40507-025-00326-5

(2025) 12:27

RESEARCH

Open Access

Low-cost ODMR experiments with
nitrogen-vacancy centers in diamonds:
a didactical approach to theory and
experiment
Nils Haverkamp1 , Alexander Pusch1 , Markus Gregor2 and Stefan Heusler1*
*

Correspondence:
stefanheusler@uni-muenster.de
1
Institute of Physics Education
Research, Münster University,
Wilhelm Klemm Str. 10, 48149
Münster, Germany
Full list of author information is
available at the end of the article

Abstract
In recent years, nitrogen-vacancy centers in diamond have attracted much interest as
tools for magnetic ﬁeld sensing and imaging. Parallel to this progress in science, also
in science education, huge advancements are seen, which might even be called an
educational quantum revolution, which just has started to emerge.
In this article, we present an experimental setup for optically detectable magnetic
resonance (ODMR) in micro-diamonds with nitrogen-vacancy centers (NV centers)
which extends the recent work presented in Stegemann et al. (Eur J Phys.
44(3):035402, 2023) in view of better accessibility both from a technical perspective
and from an didactical perspective. We improved the mechanical setup, and in
particular the output of the measured values, which is now carried out by a
microcontroller and is directly accessible to digital devices instead of the need of an
oscilloscope. In this way, we increase the accessibility of the experimental setup for
learners. Concerning modeling of the theoretical foundations, we discuss the
importance of symmetries of the wave function for understanding quantum physics
and introduce visualizations for the spin and orbit part of the wave function.
Furthermore, we present ﬁrst empirical data (N = 53), indicating possible paths for
successful dissemination of the experiments to educators.
Keywords: ODMR; Nitrogen-vacancy center; Low-cost experiment

1 Introduction
In the educational context, there are comparatively few experiments on quantum physics.
At present, the transition from classical optics to quantum optics based on single photons
cannot be demonstrated directly in class. Typically, only experiments on the photoelectric
eﬀect and experiments on the interference of light (e.g. double slit with many photons) can
be carried out in class. Note that the photoelectric eﬀect can be explained with classical
electromagnetic ﬁelds and does not necessarily lead to the existence of photons (see Lamb
and Scully [8] or Rhode [11]). With the advent of the so-called second quantum revolution,
due to rapid progress in quantum computing, simulation, sensing, and communication,
© The Author(s) 2025. Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which
permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit
to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes were made. The
images or other third party material in this article are included in the article’s Creative Commons licence, unless indicated otherwise
in a credit line to the material. If material is not included in the article’s Creative Commons licence and your intended use is not
permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright
holder. To view a copy of this licence, visit http://creativecommons.org/licenses/by/4.0/.

## PDF page 2

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

the need for suitable, modern experiments for education and training arises also both in
high school and in industry.
In recent years, nitrogen-vacancy centers in diamond have attracted much interest as
√
tools for magnetic ﬁeld sensing and imaging reaching the pT/ Hz region at room temperature (Zhang et al. [15], Schirhagl et al. [12]). The spatial resolution for the detection of the
magnetic ﬁelds and other physical quantities reaches down to the nanoscale (Schirhagl et
al. [12]). As an explicit example from a broad range of possible applications, in medicine,
single NV centers at room temperature can resolve the magnetic ﬁeld caused by brain
activities. Brain-computer interfaces which might be able to restore some mobility to paralyzed people by controlling exoskeletons are an active ﬁeld of research (see for example
Q.ANT [10] and Fraunhofer [3]).
In the educational realm, several approaches to teach quantum sensing using NV centers
have been proposed in order to increase the accessibility of the experiments (Zhang et
al. [15]). Much progress is ongoing in this ﬁeld, which might be called an educational
quantum revolution, which just has started to emerge.
In this article, we present a beginner-friendly introduction to the theory behind nitrogen
vacancy center sensing (Sect. 2). After that, we showcase interesting experimental ﬁndings relevant for educational contexts (Sect. 3) and present an experimental setup for optically detectable magnetic resonance (ODMR) in micro-diamonds with nitrogen-vacancy
centers (NV centers) for teaching and learning (Sect. 4), which extends the recent work
presented in Stegemann et al. [13]. The mechanical setup was improved and expanded
based on technical and didactic considerations for easier use in learning and teaching. In
contrast to the work of Stegemann, et al. [13], the control and output of the measured
values (instead of an oscilloscope) is now carried out by a microcontroller (in this case an
ESP32) that can be controlled using the learners’ computers, tablets or smartphones.

2 What is the nitrogen-vacancy center (NV center)?
The NV center is one of many possible defects that can occur in diamond lattices. In a NV
center, a nitrogen atom is found at one site in the lattice instead of a carbon atom. Directly
next to the nitrogen atom, a second carbon atom is missing (Fig. 1). The imaginary line
connecting the nitrogen atom and the vacancy is called the NV axis. The theory of NV
centers in diamonds is described in detail in Doherty et al. [2].
2.1 What is the effect of the lattice defect?
Due to the lattice defect, there are ﬁve free bonding electrons at the NV vacancy center.
A sixth electron can be donated from, for instance, substitutional defects, like nitrogen, in
the surrounding lattice to form a negatively charged NV– center. When referring to NV
centers, the NV– center is usually meant in the literature and also below.
Numeric calculations indicate that there are four orbitals (Gali, Fyta and Kaxiras [4]). In
terms of energy, a′1 is the lowest orbital, followed by the orbital a1 . In the ground state |g⟩,
these orbitals are ﬁlled with two electrons each. The two following orbitals ex and ey are
energetically equally favorable and are occupied with one electron each. Thus, eﬀectively,
from the six electrons in the NV center, only two electrons are relevant, as only two orbitals
are ﬁlled partially. First, we consider the spin (s1 , s2 ) of this electron pair. There are four
diﬀerent possibilities for the spin conﬁguration (up/up, up/down, down/up, down/down).
According to standard quantum physics, these conﬁguration lead either to a symmetric

Page 2 of 19

## PDF page 3

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 1 Diamond lattice with a Nitrogen Vacancy
Center. Gold: Carbon, Red: Nitrogen, dashed line:
vacancy

Figure 2 The four possible basis states in the ground state of the NV center. Symmetric combinations lead to
the spin triplet states j = 1, antisymmetric combinations lead to the singlet state j = 0

spin wave function (“triplet state”), or an antisymmetric wave function (“singlet state”),
as these combined wave functions are eigenfunctions of the total angular momentum operator with j = 1 (triplet) and j = 0 (singlet). These conﬁgurations do not only emerge in
the ground state, but also in the excited state. The only diﬀerence lies in the fact that one
electron from the orbital a1 is lifted to either orbital ex or ey . The ground state is called
3
A (the index 3 indicating the triplet state), while the excited state is called 3 E. In total

Page 3 of 19

## PDF page 4

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

there are 2(3 + 1) = 6 + 2 conﬁgurations. The remaining two states are the singlet state 1 E
and 1 A, which cannot be reached from the excited state |e⟩ by radiative transitions due to
very fundamental principles of quantum physics, which we will explain next. All states are
shown in Fig. 2.

2.2 Symmetric and antisymmetric orbital wave functions
So far, we only considered the spin part of the wave function of the pair of electrons. The
total wave function of the two electrons can be written as a product of the orbital and
the spin wave function. For fermions, the total product must be antisymmetric under exchange of the two particles. Since the two electrons with spin 1/2 are fermions, two different types of wave functions emerge: either the spin wave function is symmetric (triplet
state) with antisymmetric orbital wave function, or the spin wave function is antisymmetric (singlet state) with symmetric orbital wave function under exchange of both electrons, see Fig. 3. Thus, the spectrum is decomposed into two parts, with either symmetric
(triplet) or antisymmetric (singlet) spin. No radiative process is possible which changes
the symmetry both of the spin part and the orbital of the wave function part just by a
single photon transition. Instead, a non-radiative process may emerge due to spin-orbit
coupling. This is the reason why the state |m⟩E is metastable (Fig. 3).
Historically, the ﬁrst application of a symmetry argument of that kind has been made by
Heisenberg [6] in order to explain the observations in the spectrum of helium: It turned
out that it must be divided into two independent sets such that no term of one set will
combine with a term of the other to produce spectral lines. Indeed, in the product of the
spin and orbital wave function of the two electrons in the atomic hull of helium, Heisenberg explained these two sets (called ortho- and para-helium) by noting that the spin wave
function can be either symmetric (triplet state) with antisymmetric orbital wave function,
or the spin wave function can be antisymmetric (singlet state) with symmetric orbital wave
function, leading to the two sets observed in experiment.
This type of argument can be applied in many diﬀerent applications, ranging from the
explanation of ferromagnetism to the discovery of the color degree of freedom in quantum

Figure 3 Term scheme of NV centers with relevant transitions (not in scale). The individual levels and
therefore also wavelengths are shown in simpliﬁed form. In reality, various grating eﬀects also result in further
absorptions and emissions in a locally extended frequency range

Page 4 of 19

## PDF page 5

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

chromodynamics and can be viewed as the advent of modern quantum physics about 100
years ago.
From this point of view, NV centers can not only be seen as a tool to explain modern
applications of quantum technology like quantum sensing, but also to grasp some fundamental ideas of quantum physics. While the symmetry argument itself is simple and
beautiful, the actual calculation of the energy spectrum as shown in Fig. 3 using density
functional theory is involved and highly non-trivial. Due to spin-orbit coupling, the energies for |ms = 1⟩ and |ms = –1⟩ diﬀer by a few nano-eV (Gali, Fyta and Kaxiras [4]). However, internal stress inside a microdiamond lattice can result in a much higher splitting.

2.3 How can the quantum states be inﬂuenced?
The antisymmetric singlet state 1 E plays a crucial role because there is no radiative decay
possible to the triplet ground state since in this transition, also the symmetry of the orbital
part of the wave function changes. In thermal equilibrium, as thermal energy is around
25 meV, which is about 2000 times of the energy diﬀerence between the ms = 0 and ms =
±1 state, all three states are populated with about equal probability, as the Boltzmannfactor is almost one. The non-radiative decay mostly leads to the ground state |g⟩ with
j = 0, ms = 0 (see Fig. 3). The transition between 3 A and 3 E is typically spin-conserving.
Note that the non-radiative decay via the 1 A and 1 E levels occurs mainly for ms = ±1.
Thus, by exciting the NV center with green laser light, on a time scale of microseconds,
the population of the ground state ms = 0 can reach about 95%, and only a small minority
remains in the ms = ±1 state (Breeze et al. [1]). While the radiative decay has 10 ns as
timescale, the non-radiative channel decays only after 200 ns. Although the probability
for the non-radiative decay channel is smaller than for the radiative channel, there are 100
“trials” to enter the non-radiative decay channel within one microsecond, which ﬁnally
leads to 95% population of the ms = 0 ground state.
Starting from this initial state at ms = 0, using a 2.87 GHz microwaves in resonance
with the transition from the ms = 0 to the ms = ±1 state, an increase of the ms = ±1 state
population can be induced. Since the non-radiative decay occurs mainly for ms = ±1 state,
the ﬂuorescence of NV centers decreases when the population of the |3 A, ms = ±1⟩ state
is high. This mechanism is called optically detected magnetic resonance (ODMR).
In an external magnetic ﬁeld, the Zeeman eﬀect manifests itself in the splitting of the
energy levels with ms ̸=0. The relevant parameter for the strength of the splitting is the
ﬁeld component that is parallel to the NV axis. The energy of |ms = +1⟩ increases in an
external magnetic ﬁeld, while the energy of |ms = –1⟩ states decreases. This results in an
(increasing) splitting of the energy levels. To a ﬁrst approximation, this splitting depends
linearly on the (parallel component) of the external magnetic ﬁeld.
If multiple NV centers are contained in a diamond lattice, these are typically not all
the same but are aligned in the four possible orientations of the NV axis (Fig. 4). Since
each of these directions interacts with a magnetic ﬁeld diﬀerently, a splitting into up to
eight energy levels (two per orientation of the NV axis) can typically be observed. For
more details on the full theory including this angle-dependence, we refer to the review of
Doherty et al. [2]. By deﬁning the “z-axis” parallel to one of these four possible orientations,
we obtain the projection Bz of the magnetic ﬁeld to this axis. Then, the spin part of the
Hamiltonian reads
H = DSz2 + ε(Sx2 – Sy2 ) + γ Bz Sz

Page 5 of 19

## PDF page 6

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 4 The four possible orientations of the NV axis in the diamond grid

Here, D and E are zero ﬁeld splitting parameters, and γ is the gyromagnetic ratio. In matrix
notation, for the triplet state, the reduced matrix notation (ignoring all angle-dependence)
reads
⎛
D+γB 0
⎜
H =⎝ 0
0
ϵ
0

⎞
ε
⎟
0 ⎠
D–γB

leading to the energy eigenvalues
⎛
⎜
E=⎝

D+

√︁

(γ B)2 + ε2
0
0

0
0
0

⎞
0
⎟
0
⎠
√︁
D – (γ B)2 + ε2

In experiment, we thus expect that for vanishing external magnetic ﬁeld a splitting in the
triplet ground state in (D + ε, D – ε) with D = 2.87 GHz and ε = 0.01 GHz, which is indeed
the case (see Fig. 8. Using a Taylor expansion, we ﬁnd for magnetic ﬁelds with γ B ≫ ε for

Page 6 of 19

## PDF page 7

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

the energy the approximation
1 ε 2
E± = D ± γ B(1 + (
) + ···)
2 γB
Since the zero ﬁeld splitting is given by ε = 10 MHz, this linear approximation of the Zeemann eﬀect is justiﬁed for magnetic ﬁelds larger than about 1.5 mT, as indeed, γ B ≫ ε is
valid in this regime (with γ = gμB/h ≈ 28 GHz/T the error is of order 3%, see also Stegemann et al. [13]).

2.4 What are the technical applications of diamonds with NV centers?
Two main approaches are relevant for the technical utilization of NV centers.
2.4.1 Spin state manipulation and readout
The spin states within the NV center can be manipulated and detected. This involves inducing the system into the |ms = ±1⟩ state using microwaves. Following excitation with
green light, the system returns mainly to the |ms = 0⟩ state. By measuring the ﬂuorescence
intensity as a function of the microwave frequency, it is possible to determine whether
the system is in the |ms = 0⟩ or the |ms = ±1⟩ state. This technique is known as optically
detected magnetic resonance (ODMR, see Sect. 3.2).
2.4.2 Magnetometry
The interaction between the spins and the external magnetic ﬁeld can be utilized to measure magnetic ﬁelds with high precision. When employing individual NV centers, very
ﬁne spatial resolution can be achieved. With multiple NV centers, the splitting into the
eight dips can be used to determine not only the strength but also the direction of the
magnetic ﬁeld (see Sect. 3.3).

3 Experiments and results
The previously described three-level system endows diamonds with NV centers with several intriguing properties. In this chapter, we will ﬁrst present experiments and results that
can be generally performed with NV centers, followed by the low-cost setup employed for
these experiments in Sect. 4. A more detailed description of the experimental results can
be found in Stegemann et al. [13].
3.1 Color and ﬂuorescence of diamonds
For the experimental setup presented here, microdiamonds with a diameter of about
0.15 mm are used (Fig. 5).
The diamonds can be examined more closely with a standard school microscope. Under
magniﬁcation, it can be seen that the diamond does not look colorless or transparent, as
might be expected, but glows a reddish-purple color (Fig. 6).
The color properties of the diamonds can be investigated more closely: To do this, one
of the diamonds is irradiated with a green laser (λ = 532 nm) and the light emitted by
the diamond is observed. If the laser light reﬂected from the diamond’s surroundings is
ﬁltered out with a red color ﬁlter, it can be observed that the diamonds glow red when
irradiated with green light. Thus, the ﬂuorescence described theoretically in Sect. 2 can
be observed (Fig. 7).

Page 7 of 19

## PDF page 8

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 5 Mirco stripline with glued-on microdiamonds and a 1-euro coin for size comparison (diameter of
the 1-euro coin = 23.25 mm)

Figure 6 Enlarged view of a microdiamond with NV
centers (diameter approx. 0.15 mm)

Figure 7 Emission of NV centers in a microdiamond: Left without and right with red ﬁlter foil. Photos taken
with setup in Fig. 11

Page 8 of 19

## PDF page 9

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 8 Intensity of the emitted light of an NV center as a function of microwave frequency for B ≈ 0. The
measurement was conducted using the setup presented in Sect. 4.2. Important: The intensity is given without
a unit, as the sensor used is not calibrated and the output intensity can vary depending on the positioning of
the diamond and laser, among other factors

3.2 Decrease in ﬂuorescence upon excitation with microwaves
As described in Sect. 2, a decrease in ﬂuorescence is expected when a spin ﬂip is induced
by microwave radiation. This can be demonstrated experimentally by measuring the ﬂuorescence light of the diamonds with a photodiode and recording the intensity change as
a function of the applied microwave frequency.
If microwaves are generated in a frequency range where the energy required for the spinﬂip is present (approximately 2.8 to 2.9 GHz), a dependence of the intensity of the emitted
light on the applied microwave frequency can be measured.
Figure 8 shows that the ﬂuorescence is clearly reduced by about 0.5% to 1% in the regions
around 2.86 GHz and 2.88 GHz. The two dips can be assigned to the spin ﬂips to |ms = –1⟩
and |ms = +1⟩. The contrast or strength of the decrease depends on the intensity of the
microwaves and the quality of the color ﬁlter, among other factors.
3.3 Dependence of the decrease in ﬂuorescence on the external magnetic ﬁeld
The speciﬁc energies (or resonance frequencies) of the |ms = ±1⟩ states depend on the external magnetic ﬁeld. This can be easily demonstrated experimentally by moving a magnet
to the microdiamond at diﬀerent distances.
An example measurement for 3 diﬀerent magnetic ﬁelds B1 –B3 can be seen in Fig. 9.
The magnetic ﬁeld was measured with an external hall sensor, that was positioned next to
the diamond. The measurement clearly shows that the dips in the ﬂuorescence split into
several diﬀerent dips as described in Sect. 2.3. Six of the dips can be clearly seen in each of
the measurement series. Two more dips in the middle might be easily overseen, because
of a weaker contrast. This is because the alignment of the microwave ﬁeld with respect to
the NV-axis inﬂuences how high the probability is for a transition from ms = 0 to ms = ±1
and thus impacts the contrast of the dip.

Page 9 of 19

## PDF page 10

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 9 a) Intensity of the emitted light of an NV center as a function of microwave frequency for diﬀerent
magnetic ﬁelds (B1 ≈ 1.6 mT; B2 ≈ 2 mT; B3 ≈ 2.3 mT) measured with the setup presented in Sect. 4.3.
b) Visualization of the splitting of the resonance frequencies for diﬀerent magnetic ﬁelds

4 Technical implementation and didactic revision for the teaching-learning
context
To implement the described experiments, a modular system for low-cost wave and quantum optics experiments is used, which has already been presented in Haverkamp et al. [5],
among others. The system is based on 3D-printed cube-shaped modules that can be positioned on a magnetic base plate. Additionally, the paper covers the general experimental
and didactical considerations and beneﬁts associated with this system in detail.
In Stegemann et al. [13], a ﬁrst version of this ODMR setup using the cube-shaped modules was presented, which we have technically and didactically revised for use in teaching
and learning contexts.
Technical, theoretical and didactic considerations are very closely linked in this work,
in order to increase the accessibility of the setup in a broad sense: both in realizing the
experiment itself, in understanding the physics behind, and in becoming aware of the importance of possible applications. In order to increase the accessibility of the pertinent
theory, we provide visualizations of the wave functions as shown in Fig. 2 and Fig. 3 in the
last section and stress the importance of symmetry arguments for the orbital and the spin
wave function. In order to increase the accessibility of the experimental setup itself, the
main goal was to further reduce the complexity of the system. The biggest change is the
replacement of the optical sensor and the oscilloscope, which is as a very complex measuring instrument that has to be coupled with a trigger signal. The control, measurement and
presentation of the results are now realized via an interface on any mobile device hosted
by a microcontroller in the control box (see Fig. 10, left). Also some of the main components where replaced with simpliﬁed versions: e.g. the sliding microscope objective was
replaced with a ﬁxed lens, the dichroic mirror was replaced with a beam splitter, which
makes it cheaper and the function easier to understand.
With these modiﬁcations, conducting experiments and preparing and presenting quantum mechanical phenomena becomes easier due to reduced requirements for specialized
knowledge in controlling and measuring processes. These simpliﬁcations could prove par-

Page 10 of 19

## PDF page 11

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 10 Revised and enhanced ODMR setup (with opened controller box)

ticularly valuable in educational settings where students or educators might not possess
advanced technical skills.
This variant of the system, with which the previously described phenomena and observations can be produced, is presented below (Fig. 10). The STL ﬁles, parts list, and program
code can be downloaded for free at www.o3q.de/odmr.

4.1 Fluorescence
Figure 11 shows a schematic diagram of a setup that can be used to observe the ﬂuorescence of the diamonds.
The green class 2 laser (λ = 532 nm) with radiated power of less than 1 mW, that can
usually be used in advanced educational settings, is mounted in an adjustable holder and
is directed onto one of the diamonds by a beam splitter. Although a dichroic mirror would
reﬂect more of the green laser light while transmitting more of the ﬂuorescing red light, an
ordinary beam splitter was intentionally used here. Besides being less expensive, its function is also easier to understand technically and familiar to learners who are accustomed
to other optical setups such as interferometers.
The diamonds are mounted on an XY stage, which can be used to adjust which diamond
is irradiated. We developed this specialized XY stage to provide accurate positioning and
leaving suﬃcient clearance for placing a magnet close to the probe whilst still allowing
to be easily 3D-printed. A (pivotable) red color ﬁlter is positioned in the transmission
direction of the beam splitter, which can ﬁlter out a large part of the green light from the
laser diode (which is reﬂected behind the diamonds). By tilting the ﬁlter, learners can easily
compare the ﬁltered and unﬁltered beams. The comparatively weak red ﬂuorescence of the
diamonds can be observed through the color ﬁlter. It should also be noted that the beam
splitter also transmits about half of the laser radiation. A screen can be used to ensure that
this does not pose a safety risk.
4.2 Decrease in ﬂuorescence under microwave excitation
Since the decrease in ﬂuorescence is only a few percent, it is not possible to perceive it
with the naked eye. For this reason, a digital photo sensor is added to the setup for mea-

Page 11 of 19

## PDF page 12

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 11 Schematic setup for observing the red ﬂuorescence

Figure 12 Schematic setup for measuring ﬂuorescence as a function of an applied microwave frequency

surement, as shown in Fig. 12. A lens between the diamonds and the beam splitter also
ensures that the green light from the laser is better focused on the diamond and that the
red light emitted by the diamond can also be better collected. Even though the diamond
could be precisely placed within the focal length of the lens with an adjustable lens mount,
it was decided to ﬁx the lens in place to reduce the complexity of aligning the setup for
learners, despite accepting a slight loss of intensity.
For our low budget photodetector, we use the TSL2591 model. Due to the integrated
analog-to-digital converter integrating over time, a good sensitivity and wide dynamic
range (600M:1) can be achieved when measuring at a rate of 10 Hz. Because of the rel-

Page 12 of 19

## PDF page 13

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 13 Schematic diagram of the 3D-printed XY stage. The
position of the diamonds on the board (green) can be adjusted
using the red knobs on the metric screws

atively long integration time and due to signals communicated digitally to the microcontroller, the inﬂuence of high-frequency noise is reduced. In addition, its sensitivity is
mainly in the infrared and red range, while green light is only weakly detected. This way,
an even better contrast between ﬂuorescence and reﬂected laser light can be generated.
The diamonds themselves are mounted on a circuit board, which is mounted on the XY
stage (Fig. 13). The board serves as a microwave antenna through which microwaves can
be guided to the diamonds.
An ESP32 microcontroller is connected to control the microwaves and read out the photosensor. Since the microcontroller itself is not capable of generating frequencies in this
frequency range, it is connected to a phase-locked loop frequency synthesizer (PLL) based
on an ADF 4351that can generate frequencies between 2200 MHz and 3600 MHz. The
generated microwave signals are then ampliﬁed and applied to the antenna behind the
diamonds.
The ESP32 opens a WIFI network and hosts a local website that can be accessed with
any mobile device with a browser. In addition to introductory information and a menu
for adjusting the experiment, there is a control section where the frequency range and
sampling rate can be set. The laser diode is also connected to the microcontroller via a
relay and can be switched on and oﬀ via the website. For learners without any experience
handling oscilloscopes, this provides a very accessible approach to operate and collect data
from the experiment.
The measurement results are displayed in an I-f diagram (Fig. 14). The intensity section
shown can be limited to the relevant range. Measurements that have been carried out are
cached and can be displayed again or downloaded, so that a comparison between the measurement series and a further analysis with other programs such as standard spreadsheet
applications is possible.

4.3 Dependence of the decrease in ﬂuorescence on the external magnetic ﬁeld
In order to visualize the splitting of the dips, as shown in Fig. 9, an external magnetic
ﬁeld must be introduced. For this purpose, a permanent magnet is added to the setup.

Page 13 of 19

## PDF page 14

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 14 HTML interface generated locally on the ESP32 to control the experiment and record and display
measurements

Figure 15 Permanent magnet (left) axially movable to the stage (right; Cubes without the Baseplate)

The magnet can be moved closer to or further away from the diamonds using a screw.
Alternatively, to the representation in Fig. 15, the magnet can also be brought to the setup
from the side to show that the orientation of the magnetic ﬁeld has an inﬂuence on the
shape of the splitting. The measurements shown in Fig. 9 were conducted using this setup.

5 First empirical results
While the setup is aﬀordable and thus of its components accessible for many educational
institutions, the challenge to get these experiments into school lies in the fact that wide-

Page 14 of 19

## PDF page 15

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Figure 16 Self-Assessment of n = 53 German high school teachers. (Items translated from German)

ranging technical skills are necessary to replicate the setup. To assess whether the required
competencies are present, a total of 53 educators (high school teachers and employees
from other educational institutions) were surveyed during a training session concerning
the usage and theory of this and similar setups using a self-assessment questionnaire. We
developed the questionnaire (see Appendices A and B) in collaboration with experts in the
ﬁeld of building modern low-cost experiments to accurately measure the skills needed to
replicate this and similar setups. To develop the questionnaire, we identiﬁed the main steps
in the replication and asked three experts to identify the technical skills needed for that
step. Then we condensed those technical skills into seven items. Those seven Items were
tested with three physics teaching students using the think aloud protocol.
After determining these seven Items, expected diﬃculties especially for the items concerning soldering and 3D-printing, because these are less needed in daily activities.
The educators answered these seven questions on a ﬁve-point Likert scale, where a
higher value means a higher self-assessment of the corresponding skill. The ﬁndings are
presented in Fig. 16. When examining these results, it is essential to consider that the
participants are a group specially interested in the topic, as they decided to participate in
a low-cost-experiments training program. Therefore, it could be hypothesized that they
initially possess on average superior technical abilities compared to the average of nonparticipating peers.
Our ﬁrst results suggest that teachers generally feel conﬁdent about most of the relevant
competencies. However, as we expected, educators rate their proﬁciency relatively low in
areas related to 3D printing and soldering, with higher than expected self-assesments for
soldering. In our opinion the diﬃculties concerning 3D-printing are not due to a bigger
complexity of the needed skills but due to the newness of the technology.

Page 15 of 19

## PDF page 16

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

To make the experimental material available, it is therefore not suﬃcient just to provide building instructions for replication. Rather, it is necessary to oﬀer training programs
where educators can acquire the necessary 3D-printing skills. Alternatively, oﬀers could
be created through which pre-printed and soldered components can be obtained and then
only need to be assembled.

6 Conclusion and application
An ODMR microscope can optically detect magnetic ﬁelds in the order of nanotesla with
high spatial resolution at room temperature. Current and future applications of NV centers in diamonds therefore include the investigation of biological processes, materials research, and process monitoring (Homrighausen et al. [7], Pogorzelski et al. [9], Schirhagl
[12]). These developments pave the way for the wide usage of quantum magnetometers
in non-laboratory environments and technical applications. These new technological applications point on the importance to teach quantum physics in a modern way with these
and other applications in mind. From our didactic point of view, the educational setup
presented here it is now particulary suitable for learners in school. It features a modular, easily understandable structure, the components of which may already be familiar to
learners from various wave and quantum optics experiments in previous learning units
(see Haverkamp et al. [5]). This makes it potentially suitable from a technical and experimental perspective. In contrast to the variant with an oscilloscope described in Stegemann
et al. [13], operation through the ESP32 web interface is signiﬁcantly simpler. Learners can
also access prepared supporting information on the function, structure, and experimental
procedure. The measurement results are displayed directly on the mobile devices. Multiple measurement series can be recorded and exported for further evaluation. This makes
it particularly easy and low-threshold for learners in higher education and industry to get
started with low-cost quantum physics experiments, which serve as the basis for the development of various ODMR application possibilities. Using this setup, for the ﬁrst time,
realistic and important experiments in the ﬁeld of quantum technology become accessible for high school and university in a low-cost version including simple control of the
experiment using a web interface.
We aim to conduct further research on what skills are required for constructing and
implementing these experiments in future, as well as determining eﬀective ways to teach
the relevant physics at various levels, ranging from high school to university.
Moreover, the setup presented here is signiﬁcantly more aﬀordable than commercial
ODMR experiments and can be realized for a low three-digit euro amount. In the Quantum Minilabs project (https://quantumminilabs.de/), funded by BMBF, we thus focus on
three paths for distribution of the low-cost experiments:
(1) Making all relevant materials available open source (https://o3q.de/) in combination
with workshops.
(2) Create a network of distributors for pre-printed components for self-assembly.
(3) Create a network of distributors for complete the NV center experiment.
In future, we aim to include coherent control into our setup by using a pulsed microwave
signal that can induce Rabi-oscillations in a controlled manner, to be realized e.g. Hahn
echo in a low-cost setup based on previous work (Stiegekötter et al. [14]). Thus, there are
many more future opportunities where the experiment presented in this contribution can
be used for education in the ﬁeld of quantum technologies.

Page 16 of 19

## PDF page 17

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Appendix A
Table A1 Original German version of the items of the questionnaire
1.
2.
3.
4.
5.

Ich traue mir zu, vorhandene 3D-Dateien (.stl) für den Druck vorzubereiten (slicen).
Ich traue mir zu, fertig geslicte 3D-Dateien(.gcode) am 3D-Drucker auszudrucken.
Ich weiß, wie man mit optischen Bauteilen (Linsen, Spiegel) umgeht, ohne diese zu beschädigen.
Ich kann Schraubendreher, Zange und ähnliche Werkzeuge verwenden.
Ich traue mir zu, ein Kabel an einen Kontakt des abgebildeten Batteriehalters zu löten.

6.

Ich traue mir zu, die Bauteile von der Teileliste (siehe Abbildung) zu bestellen.

7.

Ich kann ein vorgegebenes Bauteil mit Hilfe einer Explosionszeichnung (siehe Abbildung) zusammensetzen.

Page 17 of 19

## PDF page 18

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Appendix B
Table B1 Translated items of the questionnaire
1.
2.
3.
4.
5.

I am conﬁdent in my ability to prepare existing 3D ﬁles (.STL) for printing (slicing)
I am conﬁdent in my ability to print pre-sliced 3D ﬁles (.gcode) on a 3D printer.
I am aware of how to handle optical components (lenses, mirrors) without damaging them.
I am aware of how to handle optical components (lenses, mirrors) without damaging them.
I am conﬁdent that I can solder a cable to a contact on the pictured battery holder.

6.

I am conﬁdent that I can order the components from the parts list (see image).

7.

I can assemble a given component using an exploded view diagram (see image).

Abbreviations
NV center, Nitrogen-vacancy centers; ODMR, Optically detectable magnetic resonance; BMBF, Federal Ministry of
Education and Research.
Acknowledgements
In the frame of the Project O3Q, funded by BMBF (FKZ 13N15388), we wish to acknowledge cooperation with Rüdiger
Scholz, Kim-Alessandro Weber, Marina Peters, Jan Stegemann, Jonas Homrighausen and Nicole Langels.
In the Quantum Minilabs project, funded by BMBF (FKZ 13N16714), we wish to acknowledge cooperation with all groups
involved in the realization of low-cost experiments.
Author contributions
N.H. and S.H.and A.P. and M.G. wrote the main manuscript text and N.H. prepared all ﬁgures. All authors reviewed the
manuscript.
Funding
Open Access funding enabled and organized by Projekt DEAL.

Page 18 of 19

## PDF page 19

Haverkamp et al. EPJ Quantum Technology

(2025) 12:27

Data availability
Data is provided within the manuscript or supplementary information ﬁles.

Declarations
Ethics approval and consent to participate
Not applicable.
Consent for publication
Not applicable.
Competing interests
The authors declare no competing interests.
Author details
1
Institute of Physics Education Research, Münster University, Wilhelm Klemm Str. 10, 48149 Münster, Germany.
2
Department of Engineering Physics, Münster University of Applied Science, Stegerwaldstraße 39, 48565 Steinfurt,
Germany.
Received: 24 June 2024 Accepted: 5 February 2025
References
1. Breeze JD, Salvadori E, Sathian J, Alford NM, Kay CWM. Continuous-wave room-temperature diamond maser. Nature.
2018;555(7697):493–6. https://doi.org/10.1038/nature25970.
2. Doherty MW, Dolde F, Fedder H, Jelezko F, Wrachtrup J, Manson NB, Hollenberg LCL. Theory of the ground-state spin
of the NV-center in diamond. Phys Rev B. 2012;85(20):205203. https://doi.org/10.1103/physrevb.85.205203.
3. Fraunhofer Institute for Applied Solid State Physics IAF. Controlling neural exoskeletons more precisely with diamond
sensors. Fraunhofer Institute for Applied Solid State Physics IAF. 2023. https://www.iaf.fraunhofer.de/en/medialibrary/press-releases/project-launch-neuroq.html.
4. Gali A, Fyta M, Kaxiras E. Ab initiosupercell calculations on nitrogen-vacancy center in diamond: electronic structure
and hyperﬁne tensors. Phys Rev B. 2008;77(15):155206. https://doi.org/10.1103/physrevb.77.155206.
5. Haverkamp N, Pusch A, Heusler S, Gregor M. A simple modular kit for various wave optic experiments using 3D
printed cubes for education. Phys Educ. 2022;57(2):025019. https://doi.org/10.1088/1361-6552/ac4106.
6. Heisenberg W. Über den anschaulichen Inhalt der quantentheoretischen Kinematik und Mechanik. Eur Phys J A.
1927;43(3–4):172–98. https://doi.org/10.1007/bf01397280.
7. Homrighausen J, Hoﬀmann F, Pogorzelski J, Glösekötter P, Gregor M. Microscale ﬁber-integrated vector
magnetometer with on-tip ﬁeld biasing using N - V ensembles in diamond microcrystals. Phys Rev Appl.
2024;22(3):034029. https://doi.org/10.1103/physrevapplied.22.034029.
8. Lamb E, Scully MO. The photoelectric eﬀect without photons (Nr. 19680009569). Abgerufen am 11. Dezember 2024,
von https://ntrs.nasa.gov/api/citations/19680009569/downloads/19680009569.pdf.
9. Pogorzelski J, Horsthemke L, Homrighausen J, Stiegekötter D, Gregor M, Glösekötter P. Compact and fully integrated
LED quantum sensor based on NV centers in diamond. Sensors. 2024;24(3):743. https://doi.org/10.3390/s24030743.
10. Q.ANT GmbH. Quantum magnetometer: new deﬁnition of magnetic ﬁeld sensing. 2023. https://qant.com/wpcontent/uploads/2024/04/2404-Q.ANT-New-Deﬁnition-Magnetic-Sensing.pdf.
11. Rhode M. Falsche Freunde: Problematische Experimente und theoretische Überlegungen zur Quantenphysik.
Naturwissenschaft Im Unterricht Physik, Nr. 162. 2017.
12. Schirhagl R, Chang K, Loretz M, Degen CL. Nitrogen-vacancy centers in diamond: nanoscale sensors for physics and
biology. Annu Rev Phys Chem. 2014;65(1):83–105. https://doi.org/10.1146/annurev-physchem-040513-103659.
13. Stegemann J, Peters M, Horsthemke L, Langels N, Glösekötter P, Heusler S, Gregor M. Modular low-cost 3D printed
setup for experiments with NV centers in diamond. Eur J Phys. 2023;44(3):035402. https://doi.org/10.1088/13616404/acbe7c.
14. Stiegekötter D, Pogorzelski J, Horsthemke L, Hoﬀmann F, Gregor M, Glösekötter P. Microcontroller-optimized
measurement electronics for coherent control applications of NV centers. Sensors. 2024;24(10):3138. https://doi.org/
10.3390/s24103138.
15. Zhang H, Belvin C, Li W, Wang J, Wainwright J, Berg R, Bridger J. Little bits of diamond: optically detected magnetic
resonance of nitrogen-vacancy centers. Am J Phys. 2018;86(3):225–36. https://doi.org/10.1119/1.5023389.

Publisher’s Note
Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional aﬃliations.

Page 19 of 19
