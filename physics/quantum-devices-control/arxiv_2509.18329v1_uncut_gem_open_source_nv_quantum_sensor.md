Source: https://arxiv.org/abs/2509.18329v1
PDF sha256: 8cbeeea48d34cc84a153f1ac6b0acec32a858a4e334d96712ac6a4873ae6ff35
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2509.18329v1_uncut_gem_open_source_nv_quantum_sensor.pdf

Transcription of `arxiv_2509.18329v1_uncut_gem_open_source_nv_quantum_sensor.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Uncut Gem An Open-Source Hackable Quantum Sensor

arXiv:2509.18329v1 [quant-ph] 22 Sep 2025

Mark Carney1[0000−0001−9372−9033] and Victoria Kumaran1
Quantum Village Inc., Delaware, USA and London, UK
{mark,victoria}@quantumvillage.org
https://quantumvillage.org/

Abstract. This work presents an overview of our fully open-source,
hackable quantum sensor platform based on nitrogen-vacancy (NV) center diamond magnetometry. This initiative aims to democratize access
to quantum sensing by providing a comprehensive, modular, and costeffective system. The design leverages consumer off-the-shelf (COTS)
components in a novel hardware configuration, complemented by opensource firmware written in the Arduino IDE, facilitating portability, ease
of customization, and future-proofing the design. By lowering the barriers to entry, our sensor serves as a compact platform for education,
research, and innovation in quantum technologies, embodying the ethos
of open science and community-driven development.
Keywords: Quantum sensing · Open Source

1

Introduction

Quantum technology needs an ‘Apple II’ moment. By this, we refer to the importance that the Apple II holds in the history of the desktop/personal computer.
From the first spreadsheet, VisiCalc, to the first graphical adventure game Mystery House, the Apple II was a consumer-grade platform that enabled much of
the modern technological world we are now so familiar with [16].
In a similar vein, the release of the Raspberry Pi was viewed as a key enabling
technology in the development of the Internet of Things, driving the decentralization of compute in society even further and giving prominence to the Single
Board Computer (SBC) [10]. Our work has taken inspiration from this concept
and applied this reasoning to Quantum Technologies, and sensing in particular. How can we push the boundary of what is conventionally considered to be
possible?
Open Source software has, in the first quarter of the 21st Century, formed the
bedrock of much of our technology stacks and infrastructure. Hoffman et al. [8]
determined that companies would spend around 3.5× more on software annually
if open-source options did not exist. With this, the importance of open sourcing
the key parts of the quantum technology stack become apparent - it drives
adoption upwards whilst driving costs down [8]. This sentiment of increasing

## PDF page 2

2

Carney & Kumaran

Fig. 1. Energy Level diagram for NV Centre Magnetometry, detailed in section 1.1.
NB - the intersystem crossing (ISC) shelf involving two singlet states with an infrared
(IR) transition occurring at 1042 nm, but this is not relevant to our magnetometry.

openness, interoperability, and institutional momentum is echoed by other open
source projects and studies in quantum technology, see [2, 19].
Stegemann et al. [20] managed to get the overall cost of an NV Centre diamond experimentation platform down to under €200, utilising COTS parts and
a 3D printer. This made our challenge apparent - could we reduce this cost down
even further? And could we fill in some of the gaps and create a full-stack device that is fully open-source, moving away from the optics table and towards a
hand-held form factor?
We first began designing and developing devices for quantum sensing and
magnetometry back in 2023, and this project has been the culmination of 2
years of work towards making at least part of the quantum technology space
truly open.
1.1

Brief Overview of NVC Magnetometry

The best surveys of the physics behind Nitrogen-Vacancy (NV) centre diamond
magnetometry are [18] for detailed theory, and [7] for a high-level overview.
A Nitrogen Vacancy Centre (NV Centre) is the replacement in a diamond
lattice of a single carbon (C) atom with a single Nitrogen (N) atom. In lab-grown
diamonds this replacement is typically done through electron bombardment [13].
The mismatch in atomic valencies (4 for C to 3 for N) means that a vacancy is
introduced. This defect essentially acts as a virtual atom contained within the
lattice structure that has a strong zero-phonon line at 1.945 eV (λZP L = 637nm)

## PDF page 3

Uncut Gem - An Open-Source Hackable Quantum Sensor

3

between the excited states 3 E and ground states 3 G. The hyperfine structures at
both these levels yield sub-levels that are split into a lower singlet state ms = 0
and two upper states ms = ±1 separated by a difference of D = 2.87GHz with
no magnetic field present [18]. The vacancy also has no Doppler shift relative
to any interacting photons, which is why its effects may be utilized at room
temperature.
The ground states Hamiltonian of this, ignoring the hyperfine interactions,
is given in [20] and [18] as:
H = hDSz2 + hE(Sy2 − Sx2 ) + gµB B · S

(1)

where z is the parallel axis to the NV centre, D and E are the Zero-Field Splitting
parameters, Sx2 , Sy2 , and Sz2 are the spin operators, g is the Landé g-factor, and
µB is the Bohr magneton. D arises via spin-spin interaction between the two
uncoupled electrons in the defect, and E is proportional to the internal strain
within the lattice. The resulting resonant frequency ν (see [20]) for the applied
microwave field at frequency D is given by
√
(2)
ν = D ± E 2 + (γ · B|| )2
with γ = gµB /h ≈ 28GHzT−1 [18]. The important takeaway here is that under this simplified regime, provided E is much less than B|| , the main variable
regarding the splitting is the magnetic field B|| and its orientation to the NV
centre axis.
The Energy-level scheme found in figure 1 summarizes the key physical concepts. We can excite these NV centres with green light λE ≈ 532nm. The NV
centres then relax into the upper excited states 3 E, and will become magnetosensitive under the application of microwaves. In practice, we sweep the microwave
spectrum surrounding 2.87GHz, utilizing a similar sweep to the sweep in [20] by
starting at 2.614GHz and sweeping up to 3.126GHz in discrete steps of 4MHz.

2

Gap Analysis

Many possible design options were reviewed, including the designs and build
characteristics from [4, 5, 9, 12, 17, 20, 21]. The most complete guide was from
Stegemann et al. [20], which provided a basis for our final design.
Upon analysis, however, we found a number of key things were missing from
the available designs; The firmware used in NV Center diamond experiments
is generally not available. Likewise, a reliable photodetector design schematic is
generally not available, with most examples in the literature not always accurate
to best electronic design principles. There are few easily configurable diamond
mounts, as most require specialist optical mounting apparatus. Lastly, none of
the solutions were designed to be ‘hackable’ for rapid deployment or prototyping,
with little to no reconfigurable electronics and software. Similarly, none of the
designs were geared to being ruggedized towards real world deployment.

## PDF page 4

4

Carney & Kumaran

3

Design Overview

In order to remediate these gaps, we came up with an initial design that made
the following key decisions:
1. Use off the shelf components - the only specialist part should be the
diamond material and any custom PCBs.
2. Make as many things ‘software problems’ as possible - by careful
hardware design we can relinquish most control to a single software source.
This massively improves debugging, maintenance, and updating a device.
3. Simplify the design as much as possible.
4. Make the device ‘hackable’ - by this we mean that the device should be
fundamentally and easily reconfigurable and/or extendable in both software
and hardware.
3.1

Microcontroller & Firmware

We wrote the source code for this device as Arduino IDE code - this taps into
a large user base, with lots of help and built-in support for 26 native Arduino
boards and hundreds of derivative boards [1]. This does two things; first, it
immediately makes the design much more accessible to more people who are
familiar with Arduino, over using an IDE or development tool-chain that is
manufacturer specific.
Second, it allows the design to be ported to other chips through Arduino’s
universal hardware abstraction layer. This future-proofs the design, as any issues
affecting the availability of one microcontroller means another more available one
may be substituted with ease.
To this end, we used an ESP32 microcontroller - this is very well supported by
Arduino IDE, has high quality 12-bit ADC inputs, is cheap and widely available,
and has built-in WiFi and Bluetooth Low Energy (BLE) for future connectivity.
The default software libraries for driving an ADF4351 chip (see below) use a
short calculation loop to generate the input values for the chip based off the input
of a desired frequency. However, the sensitivity of the electronics (see below)
means that this interferes with measurements significantly. To mitigate this, we
pre-computed all of the desired sweep values and store them in firmware. This
only consumes around 30 bytes per frequency at most, and practically eliminates
the noise from the microcontroller interfering with the measurement operations.
3.2

Electronics

We made use of off-the-shelf operational amplifiers that are in a standard transimpedence configuration. We use the BPW34 photodiode as the main detection
part as it has a large detection area - 3 × 3mm - and is widely available. This is
then amplified by a TL082 dual op-amp, a common low-noise dual operational
amplifier.

## PDF page 5

Uncut Gem - An Open-Source Hackable Quantum Sensor

5

To minimize the parts required and to only require one 5V power input, we
utilize a voltage divider formed from two 1,000 Ohm resistors in series from 5V to
Ground. This gives us a floating 2.5V which we utilize as a ‘fake ground’ to which
the non-inverting inputs (‘+’ pins) of the operational amplifiers are tied. This
achieves two things - firstly, it means we can do away with additional inverting
voltage regulators, and secondly means this guarantees that that output will be
below the 3V limit on the ESP32’s ADC input, without needing level shifting.
An ADF4351 PLL signal generator was chosen as a microwave generator as
it allows control via SPI bus with a range of 35MHz to 4.4GHz. The output of
this is then amplified by two monolithic microwave RF amplifiers, specifically
GALI-84+ (or compatible) amplifiers providing ≈ 16dB amplification each.
The PCBs were designed to use single-sided soldering and assembly of surface
mount components, reducing cost and complexity of production. The PCBs also
use top and bottom layer ground planes to reduce parasitics and noise.
Additionally, to make the device hackable beyond just giving full software
access, we also incorporated a small prototyping area. These generally consist
of 1.0mm copper (Cu) plated holes, spaced 2.54mm apart in a grid array. This
allows the incorporation of any device which has output pins with this standard
pitch, which is historically derived from the DIN 41612 standard, see [6].
3.3

Light Source

Canonically, 525-532nm light is sourced from a laboratory laser, however these
may sometimes prove to be problematic, especially where there is little to no
guarantee of adequate laser safety protocols.
One of the main advantages of lasers is the generation of phase coherent
photons. This is something we do not utilize for our magnetometry (see equation
1), so it suffices to use any source with the correct frequency output. ‘Superbrite’
LEDs were sourced that emit the correct frequency, and were found to perform
on par with laser sources. This significantly reduces cost and power consumption,
whilst also increasing the safety of the device.
3.4

Diamond and Photodiode Encapsulation

We make use of fast-UV curing epoxy to encase the photodetector, a microwave
aerial, and NV centre diamond samples. As pointed out in [20], we can omit
the need for a dichroic mirror and instead place a square of easily available red
lighting filter gel between the photodiode and diamond to act as our primary
optical filter.
The epoxy prism is created during a 3-step layering process, corresponding to
the diagram in figure 2; Layer 1 is a base layer of epoxy upon which the diamond
and microwave aerial are placed after it is cured. A second layer of epoxy is then
applied to fix the diamond and aerial in place. A third layer that fixes in place
the filter, photodiode, as well as any mechanical fixing parts.
The density of diamond means that it will naturally sink in most epoxies,
hence a layering approach is used. Even for fast UV curing epoxy, the excellent

## PDF page 6

6

Carney & Kumaran

Fig. 2. Left: A diagram depicting the constructions layers of the diamon epoxy prism
mount. Right: A mounted sample of diamond.

optical properties of clear epoxy are not compromised by the layering technique.
It is also easy to reconfigure, as most epoxies only need to be heated to ∼ 200C
in order to delaminate. The diamond is completely unaffeced by this heating,
and so can be retrieved for subsequent encapsulation. In particular, this move
away from the optics table towards very low cost epoxy mounting is a key part
of the fast iteration and innovation potential for this design.

4

Testing

Although full characterization of the quantum sensor is still yet to be performed,
we have managed to get some preliminary checks and estimates of sensitivity.
In figure 3 we can see the output from the sensor both with and without the
presence of a small magnet placed on top of the diamond prism. These are in line
with the measurement of the magnetism of a small bar magnet, ≈ 0.005 − 0.01
Teslas, found in figure 7 in [20] and figure 3 in [18], by rough approximation.

5

Conclusions and Future Work

On April 14th 2025 we released the full stack as open source on GitHub in [3]. To
this end, the schematics, PCBs, parts lists, software code, and build instructions
are all fully available, free and open source. We hope to build on this success
with future releases and updates to both the hardware and base software to
enable more people to learn about and practice with quantum sensing. Table 1
details the Bill of Materials (BoM) for the first release of the device, detailing a
total cost that should not exceed £120. In Aug 2025 we released a single-board
variant at DEF CON 33 [11, 15] with a lower total price of just under $100. With
our subsequent version releases we expect this cost to fall even further.
5.1

Future Work

Firstly, a full and accurate characterization should be performed on multiple
diamond samples in order to gather data for both assessing the direct measure-

## PDF page 7

Uncut Gem - An Open-Source Hackable Quantum Sensor

7

Fig. 3. Upper Left: Plotted readings in noise-adjusted millivolts from the ESP32 via
serial over USB. Each point is an average of 6 measurements, with the dashed orange
showing measurements with, and blue lines measurements without the presence of a
small magnet. The shift in the splitting can be observed both in the drop in levels and
in the shift of the valleys moving further apart. The frequency for each measurement
is given in MHz from the sample number n by (2838 + n). Upper Right: The device
during operation. Lower: Plotted readings in noise-adjusted millivolts with the sensor
in the presence of a large magnet (dashed orange) compared to no magnet (blue). Same
scale as other plot, but in a different noise environment, hence lower adjusted readings.

ment and further analysis. There is plenty of scope for improving the output
analysis and measurement estimation using edge machine learning and TinyML,
something that Homrighausen et al. demonstrated in [9], and which we think
would be an important step forward in improving the output of these devices.
We would like to see a space-ready version of the device prepared. This would
mean changing the form factor to that of a CubeSat, as well as ensuring that
all of the materials, soldering, conformal coating, and mechanical properties are
suitable for the stresses and strains of space.
There are many use cases that should also be further explored for their
suitability to this kind of low-cost quantum sensing setup, including; medical
technology use cases like magnetocardiography (MCG), industrial sensing applications, and low-cost magnetometry for Position, Navication and Timing (PNT)
use cases, building on work such as Muradoglu et al. [14].

## PDF page 8

8

Carney & Kumaran
Item
Number
Cost
Battery pack
1
Free to £5
OpAmp + electronics
1
up to £5
LED
1
∼£2-£5
ADF4350/1 MW Generator
1
£15-25
MW Gain (40dB) + BNC
1
£10
PCB (unit from run)
1
∼£5
OLED Screen
1
£5
ESP32 board
1
∼£10
NV Center Diamond
1
∼£10
Epoxy and Cu Wire
1 ea.
£10-15
TOTAL
∼£115
Table 1. Bill of Materials for the first release version sensor.

Acknowledgments. The authors are grateful to the following people for their help
during development of the device: Prof. Ben Varcoe, Max Shirokawa-Aalto, David
Benoit, Matthew Markham, Rick Altherr, David Bengtson, and Brian McDermott.
Disclosure of Interests. The authors have no competing interests to declare that
are relevant to the content of this article.

References
1. Banzi, M.: Getting started with arduino. Make: Projects, O’Reilly Media, 2 edn.
(Feb 2009)
2. Bülau,
A.,
Walter,
D.,
Fritz,
K.P.:
Components
for
an
inexpensive
cw-odmr
nv-based
magnetometer.
Magnetism
5(3),
18
(Aug
2025).
https://doi.org/10.3390/magnetism5030018,
http://dx.doi.org/10.3390/magnetism5030018
3. Carney, M., Kumaran, V.: Uncut Gem - A Fully Open-Source, Hackable Quantum
Sensor (Apr 2025), https://github.com/QuantumVillage/UncutGem
4. Chatzidrosos, G., Rebeirro, J.S., Zheng, H., Omar, M., Brenneis, A., Stürner, F.M.,
Fuchs, T., Buck, T., Rölver, R., Schneemann, T., Blümler, P., Budker, D., Wickenbrock, A.: Fiberized diamond-based vector magnetometers. Frontiers in Photonics
2 (Aug 2021). https://doi.org/10.3389/fphot.2021.732748
5. Dix, S., Lönard, D., Barbosa, I.C., Gutsche, J., Witzenrath, J., Widera, A.:
A miniaturized magnetic field sensor based on nitrogen-vacancy centers (2024).
https://doi.org/10.48550/ARXIV.2402.19372
6. Fletcher, A.: Connector industry: A profile of the European Connector Industry market prospects to 1999. Elsevier (Oct 2013)
7. Frellsen, L.F., Ahmadi, S.: Sensing magnetic fields with diamonds and green laser
light. Quantum Views 2, 10 (Jul 2018). https://doi.org/10.22331/qv-2018-07-1710
8. Hoffmann, M., Nagle, F., Zhou, Y.: The value of open source software. SSRN
Electronic Journal (2024). https://doi.org/10.2139/ssrn.4693148
9. Homrighausen, J., Horsthemke, L., Pogorzelski, J., Trinschek, S., Glösekötter,
P., Gregor, M.: Edge-machine-learning-assisted robust magnetometer based on

## PDF page 9

Uncut Gem - An Open-Source Hackable Quantum Sensor

9

randomly oriented nv-ensembles in diamond. Sensors 23(3), 1119 (Jan 2023).
https://doi.org/10.3390/s23031119
10. Johnston, S., Cox, S.: The raspberry pi: A technology disrupter,
and the enabler of dreams. Electronics 6(3),
51 (Jul 2017).
https://doi.org/10.3390/electronics6030051
11. Kumaran, V., Carney, M.: Diamonds are for hackers - building the first fully open
source and hackable quantum sensor. DEF CON 33 (August 2025)
12. Kuwahata, A., Kitaizumi, T., Saichi, K., Sato, T., Igarashi, R., Ohshima, T., Masuyama, Y., Iwasaki, T., Hatano, M., Jelezko, F., Kusakabe, M., Yatsui, T., Sekino,
M.: Magnetometer with nitrogen-vacancy center in a bulk diamond for detecting
magnetic nanoparticles in biomedical applications. Scientific Reports 10(1) (Feb
2020). https://doi.org/10.1038/s41598-020-59064-6
13. McLellan, C.A., Myers, B.A., Kraemer, S., Ohno, K., Awschalom, D.D., Bleszynski Jayich, A.C.: Patterned formation of highly coherent nitrogen-vacancy centers
using a focused electron irradiation technique. Nano Letters 16(4), 2450–2454 (Mar
2016). https://doi.org/10.1021/acs.nanolett.5b05304
14. Muradoglu, M., Johnsson, M.T., Wilson, N.M., Cohen, Y., Shin, D., Navickas, T.,
Pyragius, T., Thomas, D., Thompson, D., Moore, S.I., Rahman, M.T., Walker,
A., Dutta, I., Bijjahalli, S., Berlocher, J., Hush, M.R., Anderson, R.P., Szigeti,
S.S., Biercuk, M.J.: Quantum-assured magnetic navigation achieves positioning
accuracy better than a strategic-grade ins in airborne and ground-based field trials
(2025). https://doi.org/10.48550/ARXIV.2504.08167
15. Newman, L.H.: A special diamond is the key to a fully open source quantum sensor.
WIRED (Aug 2025), https://www.wired.com/story/fully-open-source-quantumsensor-uncut-gem/
16. Nooney, L.: The Apple II Age: How the Computer Became Personal. University of
Chicago Press (2023). https://doi.org/10.7208/chicago/9780226816531.001.0001
17. Opaluch, O.R., Oshnik, N., Nelz, R., Neu, E.: Optimized planar microwave antenna
for nitrogen vacancy center based sensing applications. Nanomaterials 11(8), 2108
(Aug 2021). https://doi.org/10.3390/nano11082108
18. Rondin, L., Tetienne, J.P., Hingant, T., Roch, J.F., Maletinsky, P., Jacques,
V.: Magnetometry with nitrogen-vacancy defects in diamond. Reports on
Progress in Physics 77(5), 056503 (May 2014). https://doi.org/10.1088/00344885/77/5/056503
19. Shammah, N., Saha Roy, A., Almudever, C.G., Bourdeauducq, S., Butko, A.,
Cancelo, G., Clark, S.M., Heinsoo, J., Henriet, L., Huang, G., Jurczak, C., Kotilahti, J., Landra, A., LaRose, R., Mari, A., Nowrouzi, K., Ockeloen-Korppi, C.,
Prawiroatmodjo, G., Siddiqi, I., Zeng, W.J.: Open hardware solutions in quantum
technology. APL Quantum 1(1) (Feb 2024). https://doi.org/10.1063/5.0180987,
http://dx.doi.org/10.1063/5.0180987
20. Stegemann, J., Peters, M., Horsthemke, L., Langels, N., Glösekötter, P., Heusler,
S., Gregor, M.: Modular low-cost 3d printed setup for experiments with nv
centers in diamond. European Journal of Physics 44(3), 035402 (Apr 2023).
https://doi.org/10.1088/1361-6404/acbe7c
21. Webb, J.L., Troise, L., Hansen, N.W., Achard, J., Brinza, O., Staacke, R.,
Kieschnick, M., Meijer, J., Perrier, J.F., Berg-Sørensen, K., Huck, A., Andersen, U.L.: Optimization of a diamond nitrogen vacancy centre magnetometer for sensing of biological signals. Frontiers in Physics 8 (Oct 2020).
https://doi.org/10.3389/fphy.2020.522536
