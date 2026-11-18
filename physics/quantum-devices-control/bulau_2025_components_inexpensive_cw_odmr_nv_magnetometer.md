Source: https://doi.org/10.3390/magnetism5030018
PDF sha256: 17a7456e67a4bc40915e6c094a3156378583743c7e3a0e45e9faac47eecdb01a
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of bulau_2025_components_inexpensive_cw_odmr_nv_magnetometer.pdf

Transcription of `bulau_2025_components_inexpensive_cw_odmr_nv_magnetometer.pdf` in this directory, 22 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-22 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

Components for an Inexpensive CW-ODMR NV-Based Magnetometer
André Bülau

, Daniela Walter *

and Karl-Peter Fritz

Hahn-Schickard, Allmandring 9b, 70569 Stuttgart, Germany; andre.buelau@hahn-schickard.de (A.B.);
karl-peter.fritz@hahn-schickard.de (K.-P.F.)
* Correspondence: daniela.walter@hahn-schickard.de; Tel.: +49-711-685-84722

Abstract
Quantum sensing based on NV-centers in diamonds has been demonstrated many times
in multiple publications. The majority of publications use lasers in free space or lasers
with fiber optics, expensive optical components such as dichroic mirrors, or beam splitters
with dichroic filters and expensive detectors, such as Avalanche photodiodes or single
photon detectors, overall, leading to custom and expensive setups. In order to provide
an inexpensive NV-based magnetometer setup for educational use in schools, to teach the
three topics, fluorescence, optically detected magnetic resonance, and Zeeman splitting,
inexpensive, miniaturized, off-the-shelf components with high reliability have to be used.
The cheaper such a setup, the more setups a school can afford. Hence, in this work, we
investigated LEDs as light sources, considered different diamonds for our setup, tested
different color filters, proposed an inexpensive microwave resonator, and used a cheap
photodiode with an appropriate transimpedance amplifier as the basis for our quantum
magnetometer. As a result, we identified cheap and functional components and present
a setup and show that it can demonstrate the three topics mentioned at a hardware cost
<EUR 100.
Keywords: quantum sensing; sensor; NV center; diamond; microwave resonator;
magnetometry; optically detected magnetic resonance; Zeeman splitting; LED; filter

1. Introduction
Received: 28 May 2025
Revised: 22 July 2025
Accepted: 30 July 2025
Published: 1 August 2025
Citation: Bülau, A.; Walter, D.; Fritz,
K.-P. Components for an Inexpensive
CW-ODMR NV-Based Magnetometer.
Magnetism 2025, 5, 18.
https://doi.org/10.3390/
magnetism5030018
Copyright: © 2025 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license
(https://creativecommons.org/
licenses/by/4.0/).

Magnetism 2025, 5, 18

The negatively charged nitrogen-vacancy (NV) color center in diamond for quantum
sensing has been studied for many years. Quantum sensors are of interest, as they are based
on fundamental constants of nature, which results in calibration-free sensing—in the case of
the NV center, that is Planck’s constant h. NVs in diamonds as quantum systems have the
advantage of working at room temperature, but can also be operated at cryogenic and even
high temperatures, which makes them very convenient to use compared to other quantum systems, such as Bose–Einstein condensates, Josephson junctions, superconductive
quantum interference devices (SQUIDs), ion traps, or vapor cells, like optically pumped
magnetometers (OPM) or Rydberg atoms. Quantum sensors based on NVs in diamonds are
especially sensitive to magnetic fields [1–5], but can also be used to sense temperature [6–8],
strain or pressure, and electric fields [9–11]. A comprehensive overview of the physical
working principle is given in [12] and many other papers, explaining the orientation of NV
axes in diamond, the energy level structure, optical excitation, fluorescence, optical detection, microwave excitation, optically detected magnetic resonance (ODMR), and Zeeman
splitting [1,2,13–16].
Multiple different groups have presented different setups and implementations over
the years, demonstrating quenching, continuous wave (CW) ODMR, Zeeman splitting,

https://doi.org/10.3390/magnetism5030018

## PDF page 2

Magnetism 2025, 5, 18

2 of 22

and pulse sequence protocols, such as the Hahn echo, spin echo, Rabi oscillation, and
others [17,18]. In general, such a setup consists of a green light source, which in most
cases is a 532 nm laser [1,4,19–25], a diamond containing the NV centers, a color filter
of some sort, such as a dichroic mirror or filter [2,4,17], and a photodetector, such as
photodiodes [2–5,14,17] or Avalanche photodetectors [26]. In rare cases, a light-emitting
diode (LED) is used for optical excitation [2,27,28]. Most of the setups are rather large, built
on optical tables, and use expensive optical components to demonstrate the physical effects.
Other sources use fiber optics and lasers [3,5,26,29–36], which can be very small, but are
expensive due to the expensive components used.
However, only a handful of implementations are known so far that have presented
setups for educational purposes [1,4,17] using cheap and off-the-shelf components that
schools can potentially afford. These setups have in common that they focus on replicating
the optical tables of the physics experiments with lower-cost components. This also means
that careful adjustment of each individual element in these setups is required, which
takes up most of the time of a typical physics lesson. In order to focus on teaching the
main underlying effects of an NV magnetometer in the duration of a physics lesson,
namely, fluorescence of the NV center in a diamond, quenching, ODMR, and Zeeman
splitting, a simpler setup is required, that in addition is free of adjustment, which was the
motivation of this work. On the other hand, such a setup has to be as cheap as possible,
without any concerns such as laser safety, to allow schools to acquire multiple kits so that
pupils can experiment in small groups instead of viewing a more advanced and expensive
experiment at the teacher’s desk. Hence, sensitivity is not the highest concern, as long
as the aforementioned effects can be demonstrated and the setup can be built easily in
out-of-school education, student labs, and makerspaces, with inexpensive and commercial
off-the-shelf components (COTS).
Therefore, components were evaluated and characterized and selected components
were combined to produce three miniaturized NV-magnetometers, which were then compared against each other. The components tested cover the light source to optically excite
NVs in a diamond, different diamonds, as well as color filters to block the excitation light.
Finally, we present a cheap and easy-to-build, exceptionally well-performing microwave
resonator, that, in turn, can be driven by a cheap and low-power microwave generator,
without the use of an additional gain block. Finally, CW-ODMR measurement results of
the NV-magnetometers are presented.

2. Materials and Methods
A CW-ODMR setup typically consists of a light source for optical excitation, a diamond,
a microwave structure with microwave generator, a color filter to block the excitation light,
and a photodetector with a transimpedance amplifier (TIA). For our ODMR setup, we
decided to evaluate LEDs instead of lasers as a light source because of their advantages,
such as large operating temperature range, low cost, absence of safety concerns, and high
reliability, but also their low noise and convenience of operation. We also tested various
inexpensive diamonds and various color filters. We proposed and presented a low cost, but
effective resonator for microwave excitation. Finally, we used a low-cost silicon photodiode
BPW34 (Vishay, Malvern, PA, USA) with a single stage TIA based on OPA140 (Texas
Instruments, Dallas, TX, USA) for our experimental setup.
2.1. LED
As demonstrated in [2,27], LEDs can serve as a light source to demonstrate fluorescence,
quenching, ODMR, and Zeeman splitting in quantum sensors. Since LEDs are widely used
as indicators, they show different viewing angles, luminous intensities (given in millicandela

## PDF page 3

Magnetism 2025, 5, 18

3 of 22

(mcd)), peak wavelengths, and dominant wavelengths, reflecting humans’ sensitivity to
green light, which peaks at 555 nm. As a first step, the specifications of the LEDs had to be
made comparable to that of lasers and to one another. Therefore, the viewing angle 2θ50% in
degrees was transferred into the solid angle Ω given in steradians (sr):
Ω = 2 × π × (1 − cos(2θ50% × π/180/2)).

(1)

Next, the luminous intensity IV given in mcd was transferred to luminous flux ΦV
given in lumens (lm):
ΦV = Ω × IV .
(2)
Applying the International Commission on Illumination (C.I.E.) Photopic Luminous
Efficiency Function [37] for the dominant wavelength λDom , the radiated power Φe in watts
can be calculated as:
Φe = ΦV /(683 × C.I.E. Photopic Luminous Efficiency Function).

(3)

With the values given for LED1 presented in Table 1 and compared to the values
calculated as presented in Table 2, we investigated several LEDs and found at least two
(LED2 and LED3) that seemed to exceed LED1, which was already used in [2], in terms of
these parameters.
Table 1. Comparison of three different green LEDs by their datasheet specifications.

Properties

LED1

LED2

LED3

Package
Continuous Forward Current [mA]
Operating Temperature [◦ C]
Peak Wavelength [nm]
Dominant Wavelength [nm]
Luminous Intensity [mcd]
Spectral Bandwidth [nm]
Viewing Angle Phi 0◦ [◦ ]

SMD *
30
−40 . . . +85
519 1
528 1
Typ. 1200 1
30 1
120 1

5 mm THT **
30
−40 . . . +95
527 1
Typ. 20,000 1
30 1

SMD *
70
−40 . . . +100
515 2
520 2
Typ. 30,000 2
40 2
30 2

1 Test condition 20 mA, 2 Test condition 50 mA., * Surface Mount Device (SMD), ** Through Hole Technology (THT).

Table 2. Comparison of three different green LEDs by their calculated properties.

Properties

LED1

LED2

LED3

Solid Angle [sr]
Luminous Flux [lm]
C.I.E. Photopic Luminous Efficiency Function
Optical Power [mW]

3.1416
3.77 1
0.8363
6.6 1

0.2141
4.28 1
0.82249
7.6 1

0.2141
6.42 2
0.71
13.2 2

1 Test condition 20 mA, 2 Test condition 50 mA.

It is worth noting that for LED2 only a dominant wavelength is given in the datasheet.
Since LED2 is a 5 mm LED with reflector and lens (viewing angle of 30◦ ), it provided
the opportunity to remove the 2.5 mm radius lens, which in the following is referred to as
“LED2 without lens”. In a second approach, the length of LED2 was reduced by another
1.3 mm, so in total by 3.8 mm (see Figure 1), leaving barely enough epoxy to secure the
bond wires and allowing the microdiamond to be placed as close as possible to the LED
chip. In the following, this LED is referred to as “LED2 shortened”.

## PDF page 4

Magnetism 2025, 5, 18

4 of 22

Figure 1. A photo of “LED2” before (left) and “LED2 shortened” after mechanical processing (right)
to reduce its length and to place the microdiamond as close as possible to the LED chip.

It is worth noting that the leads and the reflector of LED2 are made from a ferromagnetic material, most likely Kovar. It is also strongly attracted by a magnet. This, on the other
hand, can lead to an initial Zeeman splitting in the ODMR spectrum although no external
magnetic field is applied. LED3 however also showed a small attraction to a magnet, even
though the leads are made from plated copper and no indications of a magnetic material
being used are given.
2.2. Diamonds
Various diamonds containing NV centers are available at different price targets. We considered using high-pressure, high-temperature (HPHT) microdiamonds (MDNV150umHi30mg,
Adámas Nanotechnologies, Raleigh, NC, USA), large HPHT diamonds provided by Element
Six (London, UK) (bottom middle), large HPHT diamonds manufactured by Adámas (top
middle), but also a <100> chemical vapor deposition (CVD)-fabricated diamond slab (DNVB14)
manufactured by Elements Six (upper right), as shown in Figure 2.

Figure 2. A selection of various synthetic diamonds containing NV centers and covering different
price targets.

While the latter is rather expensive to begin with, laser cutting it into smaller pieces,
such as ~0.5 × 0.5 mm2 , using a green laser provides 36 pieces, each with a price of ~EUR
100. Cutting it into even smaller pieces will reduce the price per build even more, but it

## PDF page 5

Magnetism 2025, 5, 18

5 of 22

is worth noting that laser cutting can introduce strain at the edges. Sizes of components
down to 200 × 200 µm2 can be handled reliably by a pick-and-place machine these days,
which could lead to prices of about EUR 16 per diamond. Nevertheless, this approach was
not pursued for the time being.
2.3. Color Filter
In [38], dichroic color glass and gel filters were investigated for their use in medical
fluorescence applications. However, no comprehensive research into filters for quantum
sensor application has been published so far, as most of the experiments use either dichroic
mirrors to separate the excitation from the fluorescence light or filters without further
published information on their properties.
In order to characterize LEDs as light sources and various filters, a spectrometer
(CCS200/M, Thorlabs, Newton, NJ, USA, with a fiber patch cable) was used to measure the
following combinations:
1.
2.
3.

LED as light source,
LED as light source with various filters in front of it,
LED as light source with a microdiamond attached to it and various filters

The spectrometer is positioned at a fixed distance for all of the measurements to
prevent saturations of the CCD inside the spectrometer. Figure 3 gives an overview of the
expected spectral behavior of the individual components, that is, the spectral response of
the LEDs, the filter response of some selected filters, as well as the fluorescence response of
the NV0 and NV- in the diamonds. These curves were digitized from the available literature
and datasheets.

Figure 3. Fluorescence spectrum of NVs in diamond (digitized from [39]), relative intensity of several
different LEDs (digitized from datasheets), and transmission of several different color glass, gel, and
PET foil filters (digitized from datasheets).

2.4. Resonator
In order to excite the electrons to the ms = ±1 states of the NV center in the diamond for
ODMR, a microwave structure is needed. One way to build such a microwave structure is to
use a resonator of high quality factor Q with a resonance frequency at around f = 2.87 GHz,
and the electron spin resonance at zero magnetic field, by soldering two SMA connectors
back-to-back together, with a capacitor C between the two inner pins and a parallel wire
loop forming the inductance L, as shown in Figure 4a,b.

## PDF page 6

Magnetism 2025, 5, 18

6 of 22

(a)

(b)

Figure 4. A discrete resonator built from two SMA connectors, a 1 pF ceramic capacitor, and a 2 mm
loop of copper wire: (a) CAD model of the construction; (b) Real build with 50 Ω termination on the
left and 90◦ angled connector on the right to avoid any strain to the center pins and thus the capacitor.

The resonance frequency f of such an LC-circuit is calculated by the formula
f=

1
√ .
2π LC

(4)

According to (4), a capacitance of C = 1 pF and an inductance of L = 3 nH are needed,
resulting in a resonance frequency of f ≈ 2.9 GHz. By trimming the loop diameter, hence
the inductance, the resonance frequency can be tuned to f = 2.87 GHz. Coarse tuning was
achieved by starting with a slightly larger loop diameter, followed by a vector network
analyzer (VNA) measurement, to then decide if the loop diameter has to be increased or
decreased. Medium-trimming was achieved by slightly changing the solder point of the
copper wire at one pin of the SMA connecter, and fine-tuning was achieved by slightly
tweaking the loop shape with tweezers and a toothpick after soldering.
For the capacitor, a ceramic type like NP0 is sufficient. To achieve the desired 3 nH for
the wire loop inductance L, the formula
(
L ≈ µ0 µr

)( (
)
)
8·D
D
· ln
−2
2
d

(5)

was used to calculate the needed loop diameter D, that depends on the used wire diameter
d. According to (5), the inductance L can be formed by a loop of d = 0.2 mm copper wire
with a loop diameter of D = 2 mm resulting in the required inductance of L ≈ 3 nH.
One of the SMA connectors is terminated with a 50 Ω resistor. It is worth noting that
the SMA connectors are usually made from brass with nickel and gold plating. The nickel
plating can lead to an initial Zeeman splitting in the ODMR spectra at zero magnetic field.
The return loss S11 of the discrete resonator was measured by a VNA ZNLE6 (Rohde
& Schwarz, Munich, Germany) with a 10 MHz reference clock provided by a global
positioning system disciplined oscillator (GPSDO) Thunderbolt E (Trimble, Sunnyvale, CA,
USA). The results are shown below in Section 3.4.
2.5. Photodetector and TIA
To convert the photocurrent of the BPW34 photodiode into a voltage, a single-stage
TIA was used. The transimpedance was set in a way that the output voltage of the TIA
stayed below 3.3 V in order to digitize the signal with an analog-to-digital converter (ADC)
integrated in a standard microcontroller. The bandwidth of the TIA was limited to a
bandwidth of ~200 Hz, which seemed to be sufficiently fast, by choosing an appropriate
parallel capacitor. Thus, the values for the gain-setting passive components at the TIA
given in Table 3 were chosen for our builds.

## PDF page 7

Magnetism 2025, 5, 18

7 of 22

Table 3. Values for the gain-setting passive components at the transimpedance amplifier.

Build

Resistor (kΩ)

Capacitor (F)

LED3 + microdiamond
LED3 + large HPHT diamond
LED2 shortened + large HPHT diamond

620
56
82

120 p
12 n
8.2 n

2.6. CW-ODMR Setup and Measurement
To measure the CW-ODMR signals, a setup as shown in Figure 5 was arranged. The
LED of the inexpensive NV-magnetometer was fed by a programmable power supply
(Rohde & Schwarz HMPF 2030), either directly by setting the power supply into constant
current mode or indirectly by an LM317-based constant current source that can be placed
in between the LED and the power supply, with the power supply set to constant voltage
mode. The power supply also feeds the TIA of the inexpensive NV-magnetometer with
a bipolar voltage. The discrete resonator is driven by a cheap ADF4351 board (<EUR 30).
Therefore, some minor modifications were made to it. The first modification is related to
the loop filter, which was modified to match the datasheet and user manual of the ADF4351
evaluation board. The second modification is related to the output matching. As proposed
by the datasheet, the output was populated with an LC balun for the frequency range
of 1.6 to 3.6 GHz to convert the differential into a single-ended output, resulting in up
to +8 dBm of output power. This way, the microwave generator can drive a resonator
without an additional gain block. The ADF4351 board itself is controlled by an STM32
microcontroller (µC) via an SPI interface. The µC on the other hand is controlled via a
USB interface from a mathematical program (GNU Octave, version 9.3.0 (2024-12-12)) on
a personal computer (PC). The µC also provides a trigger signal, which is directly fed
into an oscilloscope (HDO6054-MS, Teledyne LeCroy, Chestnut Ridge, NY, USA). Signals
can be read in two ways. The first option is to capture and display the signals with the
oscilloscope and to store the acquired data. The second option is to capture the signals
with the µC itself, using its built-in ADC to digitize the signals and display them with the
mathematical program GNU Octave on the PC in real-time. In both cases, results are given
as the resulting photodiode voltage from the TIA and are called CW-ODMR signals in the
upcoming measurement results.
For the measurement with varying LED current and microwave power, a sweep ranging
from 2.67–3.07 GHz with 801 steps was performed and the photodiode voltage from the TIA
sampled with the oscilloscope at 1 MSps, which took about 1.6 s per sweep. In addition,
an average of 36 consecutive sweeps was taken to improve the signal-to-noise ratio (SNR),
resulting in a total time of ~1 min for each measurement. Afterwards, the averaged CW-ODMR
curve was decimated by a factor of 500, the data stored and analyzed offline.
For the measurements using the built-in ADC of the µC, the microwave power was
set to +8 dBm and a sweep from 2.67–3.07 GHz with 1500 steps was performed. The
µC accumulated 100 consecutive measurement values of the ADC at each frequency step
before the next frequency was applied, which resulted in a total sweep time of about 2.5 s.
Afterwards, the accumulated signals were divided by a factor of 100 using the PC software
(GNU Octave, version 9.3.0).

## PDF page 8

Magnetism 2025, 5, 18

8 of 22

Figure 5. Schematic drawing of the measurement setup with the inexpensive magnetometer on the
left, voltage source on the right, microwave generator and oscilloscope on the top, and microcontroller
with PC on the bottom.

3. Results
In the following, we present the results found for the spectral behavior of the LEDs
measured with a spectrometer, the spectral behavior of the various filters when excited
with LED2, measured with the spectrometer, as well as microscope images of the LEDs with
microdiamonds attached and two different color filters in front of them. Next, the results of
the discrete resonator measured with the VNA are presented. These results are followed by
three setups of inexpensive magnetometers resulting from the previous results regarding
the individual components. Afterwards, the presented magnetometers are characterized by
CW-ODMR measurements.
3.1. LEDs Measured with Spectrometer
In Figure 6, the spectral intensity of the tested LEDs is given as measured with
the spectrometer and the patch fiber cable directly attached to the LED’s surfaces. The
integration time of the CCD-based spectrometer was set to 20 µs for all these measurements.

Figure 6. Comparison of the LEDs by their measured spectral intensity.

As can be seen, LED1, LED2, and LED3 are comparable with each other, when a
current of 30 mA is flowing through them. As expected, the intensity significantly increases
for “LED2 without lens” and “LED2 shortened”, due to a smaller distance between the
LED chip and the optical fiber of the spectrometer. With a current of 70 mA through LED3,

## PDF page 9

Magnetism 2025, 5, 18

9 of 22

the intensity is comparable to that of “LED2 shortened”, but without any mechanical modification of the LED. Nevertheless, a significant improvement in intensity over LED1 [40]
used in [2] is achieved by using LED2 [41] after modification or LED3.
3.2. LED2 with Various Filters Measured with Spectrometer
As a next step, various long-pass filters, inexpensive gel filters, filters based on coated
PET foils, as well as color glass filters were tested for their ability to block the excitation
light of the LED. LED2 with a current of 30 mA was measured first and then the filters
were applied consecutively one after the other without changing the settings of the spectrometer. The results are presented in Figure 7, in which the diagram in Figure 7b is a
zoomed representation of the diagram in Figure 7a,d, which is a zoomed representation
of the diagram in Figure 7c. The diagrams show the inexpensive gel filters (Neewer filter,
Shenzhen Xing Ying Da Industry Co., Ltd., Shen Zhen, Guangdong, China), the coated
PET foils (FilterXXX, LEE Filters Worldwide, Hampshire, United Kindom), and the various
color glass filters (RGXXX, SCHOTT AG, Mainz, Germany). As can be seen, most of the
filters show a rather strong autofluorescence, like Filter106, the red Neewer filter or RG610.
Additionally, green light leaks through some of them, for example, for the red Neewer filter
or RG610, indicating an uneven distribution of the dye. For the inexpensive filters based
on coated PET foils, Filter787 showed the best results, followed by Filter789 and Filter027.
For the color glass filters, RG645 showed the best results, followed by R62.

(a)

(b)

(c)

(d)

Figure 7. The spectrum of the filter response during excitation with green light from LED2 is shown:
(a) with respect to the intensity of LED2 at 30 mA and (b) in a zoomed representation to better
visualize the filter behavior for the gel and coated PET foils; (c) with respect to the intensity of LED2
at 30 mA and (d) is a zoomed representation of (c) to better visualize the filter behavior for the color
glass filters.

In addition, yellow to orange autofluorescence was observed for all glass filters and
the Neewer filter when excited by a 532 nm laser (optical power <1 mW). In some cases,
laser light was leaking through the filter, visible as tiny spots, again indicating an uneven
distribution of the dye inside the glass filters. However, no autofluorescence for the filters

## PDF page 10

Magnetism 2025, 5, 18

10 of 22

based on coated PET foils was found but tiny spots of excitation laser light showed due to
leakage for all of them.
Excitation with a UV-LED (330 mW electrical power) again showed yellow to orange
autofluorescence for all glass filters, decreasing in intensity from 610 nm to 645 nm cutoff
wavelength. For the Neewer filter, autofluorescence was hidden by blue to UV light leaking
through the filter, due to a weak filter response at shorter wavelengths. However, no
autofluorescence was observed for the filters based on coated PET foils.
3.3. Microscope Images of LEDs with Microdiamond and Color Filters
The aforementioned LEDs with microdiamonds attached to them were used to take
images under a microscope at fixed exposure with two well-performing and inexpensive
filters based on coated PET foil (filter1: LEE FILTERS 027 MEDIUM RED (Filter027),
filter2: LEE FILTERS 787 MARIUS RED (Filter787)). This way, a qualitative analysis of the
fluorescence intensity was performed, while the green excitation was efficiently suppressed
at the same time. Figure 8 shows a series of images for the various LEDs and filters.

(a)

(b)

(c)

(d)

(e)

(f)

(g)

(h)

(i)

(j)

Figure 8. Various green LEDs with a microdiamond attached under a microscope and a color filter
in between: (a) LED1 with filter1; (b) LED1 with filter2; (c) LED2 with filter1; (d) LED2 with filter2;
(e) LED2 without lens and filter1; (f) LED2 without lens and filter2; (g) LED2 shortened with filter1;
(h) LED2 shortened with filter2; (i) LED3 with filter1; (j) LED3 with filter2.

## PDF page 11

Magnetism 2025, 5, 18

11 of 22

For all tests, a current of 30 mA through the LED, the very same magnification at
the microscope and an exposure time of 1 s of the camera was chosen, although LED3
could have been supplied with up to 70 mA. All LEDs were equipped with 150 µm sized
microdiamonds that were attached to the LEDs using optical adhesive (NOA61).
3.4. Resonator
Figure 9a shows the return loss S11, while Figure 9b depicts the corresponding Smith
chart of the discrete resonator, measured by the VNA. As can be seen, the bandwidth of
the resonator is broad, with a steep peak at resonance frequency. A resonance frequency of
f = 2.85976 GHz was measured, with a return loss of S11 = −50.8 dB.

(a)

(b)

Figure 9. VNA measurements of the discrete resonator: (a) Return loss S11; (b) Smith chart in the
frequency range 2.67 GHz to 3.07 GHz.

3.5. Inexpensive Magnetometer Setup
For the inexpensive magnetometer setups and to measure CW-ODMR, the components
from Sections 2.1–2.3 were used. This resulted in three different setups. As the basis, the
discrete resonator from Section 2.4. was taken. Additional components were arranged
around and in between the SMA connectors (EUR 10.60 per piece). The first setup uses
LED3 (EUR 0.87) and a microdiamond (~EUR 3). The second setup contains the same
LED3 and the large HPHT diamond from Element Six (EUR 10 . . . 15). The third setup
contains LED2 shortened (EUR 0.30) and another large HPHT diamond from Element Six.
All additional components are the same for every setup. A photodiode BPW34 (EUR <1.20)
was used to collect the fluorescence light. To filter the green excitation light, the color filter
LEE 027 MEDIUM RED (<EUR 0.01 per 4.5 × 4.0 mm2 piece) was directly attached to
the photodiode with optical adhesive (NOA61, Norland Products Incorporated, Cranbury,
NJ, USA). This filter was the cheapest to buy. The diamonds were arranged between the
LED and the color filter with as little distance between each component as possible. The
remaining gap was filled with optical adhesive (NOA61) to minimize optical losses along
the optical path. The diamonds were either positioned in the center or close to the center of
the loop, with one of their 111-surfaces oriented parallel to the photodiode’s surface.
Optionally, every LED can be driven by a constant current source (<EUR 1). The
photodiode signal is amplified by a simple one-stage TIA (<EUR 6 including all passives).
The amplification was chosen in such a way that the signal stayed below 3.3 V to feed the
built-in ADC of the µC (Table 3).
In Figure 10, the CAD models of the three different assemblies around the SMA cage
containing (a) LED3 with microdiamond, (b) LED3 and large HPHT diamond, (c) LED2

## PDF page 12

Magnetism 2025, 5, 18

12 of 22

and large HPHT diamond together with the discrete resonator, color filter, and photodiode
are shown. Figure 10d shows a real-world example of these builds.

Figure 10. CAD models of the three different assemblies for CW-ODMR measurement setups with
SMA connectors including (a) LED3 with microdiamond, (b) LED3 with large HPHT diamond, and
(c) LED2 shortened with large HPHT diamond. (d) Shows the real-world build.

3.6. CW-ODMR Signals
In a first test, the CW-ODMR signals with no external magnetic field were captured for
various LED currents. The LED current was directly set at the inexpensive magnetometer,
without the usage of the constant current source, by the programmable voltage source to
values ranging from 10 to 60 mA in steps of 10 mA for LED3 and up to 30 mA for LED2
shortened. The microwave sweep was performed from 2.67 GHz to 3.07 GHz in about
1.6 s. A Teledyne LeCroy HDO6054-MS oscilloscope captured the resulting signals. The
curves shown are averaged over 10 consequent sweeps. The sweep data were then saved
and post-processed using GNU Octave and a PC. Therefore, the offset from the signals was
removed to compare the height of the fluorescence dips at resonance. Figure 11 shows the
resulting CW-ODMR signals for the various LED currents for the previously introduced
magnetometer setups. The smallest dip heights were achieved with the microdiamond
in combination with LED3 (Figure 11a). The dip height is about 55 mV at the highest
current of 60 mA. It becomes smaller for lower LED currents. The large HPHT diamond in
combination with both LEDs showed much higher fluorescence dips. Therefore, at 60 mA,
the large HPHT diamond with LED3 (Figure 11b) showed about 300 mV dip height and
140 mV at 30 mA. In comparison, the large HPHT diamond in combination with LED2
shortened (Figure 11c) showed 150 mV dip height at its highest current of 30 mA, which is
slightly higher than for the large HPHT diamond with LED3, but could be related to the
diamonds sample size.
Furthermore, the ODMR dip height was measured for various currents of LED3 and
microwave power excitation for the microdiamond, with the results given in Figure 12. In
this measurement series, LED3 was tested up to a current of 70 mA.

## PDF page 13

Magnetism 2025, 5, 18

13 of 22

(a)

(b)

(c)

Figure 11. Resulting CW-ODMR signals for various LED currents from different CW-ODMR setups:
(a) LED3 with microdiamond, (b) LED3 with large HPHT diamond, and (c) LED2 shortened with
large HPHT diamond.

Figure 12. ODMR dip height for various currents of LED3 and microwave power excitation for the microdiamond.

## PDF page 14

Magnetism 2025, 5, 18

14 of 22

In a second test, the LEDs were driven with the constant current source at 30 mA for
the builds with large HPHT diamond and 60 mA for the build with microdiamond. This
time, the resulting CW-ODMR signals were captured with the ADC of the µC and read by
a PC. The position of a permanent magnet was varied on a linear stage in order to change
the resulting magnetic field in the diamond integrated into the different builds of the
inexpensive magnetometer. Every build was arranged in order to see all the NV-axes (four
dip pairs) at the highest magnetic field. This setup is shown in Figure 13. To determine the
size of the magnetic field, a 3D Hall sensor evaluation kit (TLE493D-P2B6 MS2GO, Infineon,
Neubiberg, Germany) was used as a reference. Therefore, the setup was rearranged such
that the inexpensive magnetometer was replaced by the reference sensor.

Figure 13. CW-ODMR measurement with varying magnetic field and a 3D reference Hall sensor to
determine the applied magnetic field.

The first measurement was performed without the presence of the permanent magnet.
Afterwards the permanent magnet was varied in its distance to the magnetometer in steps of
2.5 mm. The first position is the position where the reference sensor senses the first signals
in the direction of the permanent magnet. The distance was reduced until unusable signals
were measured due to dominating quenching effects. The left column of Figure 14 shows
diagrams with CW-ODMR curves at selected magnetic field values for the different builds,
which are Figure 14a LED3 with microdiamond, Figure 14c LED3 with large HPHT diamond,
and Figure 14e LED2 shortened with large HPHT diamond. The yellow-green curves show
the CW-ODMR signals without the permanent magnet. With higher magnetic fields, the
resonance peaks split, get smaller, and shift to both sides further away from 2.87 GHz as
the center frequency at no magnetic field. Though, for no magnetic field, the resonances of
ms = +1 and ms = −1 are already spread. This spreading is called zero-field-splitting (ZFS) and
is caused by the degeneration of the two states. Some minor spreading might also be caused
by surrounding magnetic fields and materials. The ZFS can be measured as the frequency
offset between the two resonances. For the build with LED3 and microdiamond, the ZFS
is about 31 MHz, whereas for the builds with large HPHT diamonds and LED3 and LED2
shortened, ZFS is 9 MHz and 11 MHz, respectively (Table 4).

## PDF page 15

Magnetism 2025, 5, 18

15 of 22

(a)

(b)

(c)

(d)

(e)

(f)

Figure 14. CW-ODMR signals as photodiode voltage for various selected magnetic field values
for all builds: (a) LED3 with microdiamond, (c) LED3 with large HPHT diamond, and (e) LED2
shortened with large HPHT diamond. The diagrams on the right side show colormaps of the achieved
CW-ODMR signals as photodiode voltage over frequency and magnetic field for all builds: (b) LED3
with microdiamond, (d) LED3 with large HPHT diamond, and (f) LED2 shortened with large HPHT
diamond. On top of each colormap, the smoothed photodiode voltage values at highest magnetic
field value are plotted over frequency.

## PDF page 16

Magnetism 2025, 5, 18

16 of 22

Table 4. ZFS determined from CW-ODMR signals with no external magnetic field and FWHM values
for different builds.

Build

ZFS (MHz)

FWHM (MHz)

LED3 + microdiamond
LED3 + large HPHT diamond
LED2 shortened + large HPHT diamond

31
9
11

13
15
23

For better visualization of the resonance shift in frequency with increasing magnetic field,
the diagrams in the right column of Figure 14 are provided. Therefore, the raw CW-ODMR
signals were first smoothed with a fastsmooth filter [42] and visualized with a colormap over
the frequency and magnetic field. All captured measurements are included in these figures.
On top of each colormap, the smoothed CW-ODMR signal at highest magnetic field is shown
to visualize the connection between the right and corresponding left figure in each row of
Figure 14. With higher magnetic field, the position of the dip pairs of every NV axis in the
spectrum changes in a different manner. The dips furthest away from the center frequency
correspond to the most addressed NV axis, which means this NV axis has the smallest angle
to the vector of the magnetic field. The magnetic field has most impact on an NV axis if its
vector is parallel to the NV axis. At no magnetic field, all dips for ms = +1 and ms = −1,
respectively, are superimposed in two dips with high dip heights. With increasing magnetic
field, the dips of each NV axis separate as the dip heights decrease. Finally, four dip pairs
(eight dips) can be seen in the colormaps of Figure 14. For the build with LED3 and large
HPHT diamond in Figure 14d, the eight dips are most distinctive, whereas for the build with
LED3 and microdiamond, the ms = −1 dip next to the center frequency of 2.87 GHz can hardly
be seen. Nevertheless, the other dips are distinctive. For the build with LED2 shortened and
large HPHT diamond in Figure 14f, the dips are broader and less distinctive. This broader
appearance of the dips can also be given as a characteristic number, which is called full width
at half maximum (FWHM). In the second column of Table 4, FWHM is given for all builds. It
is somewhat greater for LED2 shortened with large HPHT diamond than for the other two
builds that have quite similar FWHM values.

4. Discussion
Currently, LEDs specifically designed for NV-magnetometers do not exist and they are
designed for illumination purposes. However, we have shown that by selecting appropriate LEDs and/or by modifying their lenses, strong optical excitation of the NV centers in
diamonds can be achieved. Ideally, a high intensity LED chip would be placed inside a nonferromagnetic reflector, with a custom lens directly molded on the LED chip focusing as much
light as possible into the diamond. Combined with the overall advantages of LEDs, such as
their low price, their large operating temperature ranging from −40 ◦ C up to +90 ◦ C or even
100 ◦ C, their low noise due to missing speckle noise compared to lasers, their fast stabilization,
their easy control by a constant current source, and their potential of fast switching, they
are a perfect choice for low-cost CW-ODMR NV-magnetometers. Nevertheless, we have
proven that even currently available LEDs designed for illumination applications can be used,
although most of the emitted light is wasted.
As expected, the microdiamonds show a weaker fluorescence dip compared to the large
HPHT diamonds due to their physical size. Furthermore, the linewidth for both diamonds is
rather large, which is due to the huge internal strain of HPHT diamonds in general and their
large NV concentration. On the other hand, small additional lobes next to ZFS were observed,
which can be explained by carbon-13 (13 C) interaction. Nevertheless, for the purpose of
teaching the three topics of fluorescence, ODMR, and Zeeman splitting in schools, both

## PDF page 17

Magnetism 2025, 5, 18

17 of 22

diamonds are sufficient. However, future research will address using fluorescence waveguide
and excitation devices for the microdiamonds to improve the signal-to-noise ratio [3,43,44].
Care must be taken when selecting a proper color filter. One key aspect to be aware of,
despite the filter response itself, is autofluorescence, which most of the filters tested here
exhibited, showing up as yellow to orange light when excited with green light. This light
will create a large and constant photocurrent in the photodetector, resulting in a DC offset
at the output of the TIA.
Two inexpensive dye-coated PET foil filters, namely, LEE FILTERS 027 MEDIUM RED
and 787 MARIUS RED, were identified that both satisfied the technical requirements. Their
maximum operating temperature is specified as +180 ◦ C.
Autofluorescence is also important when selecting optical adhesives, which the chosen
NOA61 fulfilled and which was used in previous publications.
The discrete resonator is based on a parallel circuit of a capacitor and an inductor, built
around two SMA connectors and terminated with a 50 Ω resistor on one side. Off resonance,
the impedance of such a parallel LC circuit is low; hence, the termination resistor dominates
the overall impedance. Near and at resonance, the impedance of the resonator is high and only
a small current flows into the resonator. At the same time, the energy stored in the resonator
alternates between the electric field in the capacitor and the magnetic field in the inductor.
During the conversion of the magnetic field into the electric field, a huge current flows within
the resonator to maintain the magnetic field. Together with the skin effect, resulting in the
flow of current only in the surface of the wire loop, which at the same time provides a large
surface area, a strong microwave field is generated to excite the diamond.
With all of these tested components, three builds of inexpensive CW-ODMR NV-based
magnetometers were set up and the first measurements were successfully conducted. The
builds are rather simple and inexpensive (<EUR 100 in components, not including preferred
microcontroller platform and power supply) and therefore could be the basis for applied
research and educational kits, which was the goal of the project. An overview of all the
components used in our setup is given in Appendix A Table A1. The overall size is still big
and ongoing investigation to further miniaturize the setups is already in progress.
Figure 11 showed that the absolute negative dip height of the CW-ODMR signals increased with increasing LED current. What is not shown in the diagrams is that the offset
voltage also increases. The offset voltage increases due to increasing residual light of the green
LED passing the filter. The increased dip height can be explained by the higher optical power
with increasing LED current that leads to a higher number of excited electrons of the NVs and,
therefore, to a higher probability of the occurrence of intersystem crossing.
Figure 12 shows a measurement with varying microwave power excitation ranging
from −4 to +8 dBm for various currents of LED3 and microdiamond. Beyond +2 dBm, no
significant improvement in ODMR dip height was observed, which is related to the huge
quality factor of the discrete resonator. On the other hand, the ODMR dip height still does
not decrease at +8 dBm.
Figure 14 showed the CW-ODMR signals at various magnetic field values on the left and
a colormap of the CW-ODMR signals over frequency and magnetic field on the right. At no
magnetic field, ZFS can be determined. Due to internal strain of the HPHT diamonds, an initial
ZFS can be observed that is unique for each diamond sample. Some of this ZFS might also be
explained by magnetic fields present in the environment due to missing shielding, though
the environment was equal for all tested samples. Additionally, the used SMA connectors
as well as the Kovar material of the LED2 pins might contribute to ZFS too. For the large
HPHT diamonds, the ZFS of 9 and 11 MHz for both samples is about the same. The ZFS for
the microdiamond with 31 MHz, in contrast, is about three times larger. Stegemann et al. [4]
measured a ZFS of 20 MHz for a similar microdiamond, which is smaller but of the same

## PDF page 18

Magnetism 2025, 5, 18

18 of 22

order. Since ZFS can vary for each diamond sample, this is a valid result. For more statistics,
more samples need to be investigated, which could be part of a future study.
As can be seen in Figure 14a–f, the dip heights are not symmetrical to the center
frequency of 2.87 GHz. According to [17], an asymmetry might be a result of the MW
resonator that has a resonance frequency not exactly at the center frequency of 2.87 GHz
and, therefore, leads to the asymmetrical behavior of the CW-ODMR signals.
FWHM is a measure of the quality of the diamonds. Since we only used HPHT diamonds (microdiamond and large HPHT diamond), large values for FWHM were expected
for all builds. The higher value for LED2 shortened with the large HPHT diamond could
be the result of the natural variation in diamonds, since this diamond was of the same type
but not the identical diamond used with LED3 and the large HPHT diamond. To verify
this, more builds with the same type of diamond are necessary to measure FWHM and to
develop a corresponding statistic. For comparison, the ODMR spectrum shown in [2] was
digitized and FWHM was estimated to be ~20 MHz, which is in good agreement with the
FWHM found in this work.
For all experiments with a magnetic field, a permanent bar magnet was used. It is
known that magnetic field lines go from one pole to the other. This means that in this
setup, the magnetic field at the position of the diamond does not create a homogeneous
magnetic field. It is sufficient though to show the ability of our inexpensive magnetometers
to detect variations in magnetic fields and the magnitude of the characteristic values shown
(ZFS, FWHM). However, for a more precise characterization of these magnetometers,
homogeneous magnetic fields are needed, e.g., from a Helmholtz coil.
Compared to other existing low-cost solutions for education [1,4], the focus here
was not building an experimental setup, such as an optical table, requiring adjustment of
the individual components with respect to one another, but to use the sensor for simple
measurements, like detecting a nearby magnet or finding cabling in walls.
Currently, one of the limiting factors in making our solution more compact is the
resonator. Thus, work in progress is to produce an even more compact solution, containing
only the critical components, such as the arrangement of the optical components, including
the diamond, a novel easy-to-manufacture resonator design, the driver of the LED, and the
signal conditioning (TIA and such), in a volume of only π cm3 (Ø10 mm × 40 mm)—hence,
why we name it the π-Mk1 platform. In order to improve the signal-to-noise ratio for
microdiamonds, the use of fluorescence waveguide excitation and collection devices is
considered. The results of this work will be presented in another paper.
In parallel, a low-cost USB-based power supply is in development to provide the
necessary voltages for this platform, avoiding the need for expensive bench power supplies
and dealing with mains voltages. Additionally, real-time curve-fitting of the dips in the
ODMR spectrum is work in progress.
Both, the π-Mk1 platform as well as the USB power supply will be part of our QOOOL
Kit Magneto, which will become part of the senseBox (re:edu GmbH & Co. KG, Münster,
Germany) [45]. While we currently use our preferred STM32 microcontroller, a transfer
to the senseBox, an ESP32 microcontroller platform with various sensors, displays, and
wireless communication modules, is planned within our project QOOOL Sensing [46]. The
senseBox is already available at over 2000 schools, museums, and makerspaces in Germany
and the kit will extend the senseBox using a quantum sensor.

5. Conclusions
We have presented an inexpensive (<EUR 100) CW-ODMR NV-based magnetometer setup
for digital education based on thoroughly tested and selected components. Therefore, the datasheet
specifications of various LED light sources were made comparable and selected LEDs were success-

## PDF page 19

Magnetism 2025, 5, 18

19 of 22

fully tested. Color filters were characterized regarding their filter response and autofluorescence.
It turned out that coated PET foil color filters gave the best performance, while being extremely
cheap at the same time. A low-cost and exceptionally well-performing discrete built resonator
was presented that was eventually used for three CW-ODMR setups. Together with the testing
and selection of components, measurements of ODMR spectra at various LED currents were
performed in order to compare two different LEDs and two different types of HPHT diamonds.
In addition, microwave power was varied for the setup with microdiamond at various
LED currents and showed that beyond +2 dBm, no significant improvement in the fluorescence dips was observed, which is a result of the high-quality of the discrete resonator.
Furthermore, ODMR spectra with a magnet positioned at various distances to the
diamond demonstrated that the setup can serve as a magnetometer. The ZFS in the absence of
an external magnetic field, with no shielding of the setup, is rather large, which is due to strain
within the HPHT diamonds (and possibly also magnetic fields from nearby components). The
linewidth was calculated as FWHM and is in good agreement with other publications.
Future investigations will be conducted in order to further miniaturize the setup,
especially the MW resonator, and to fully characterize the setups and their limitations.
Author Contributions: Conceptualization, A.B. and D.W.; methodology, A.B. and D.W.; software,
A.B. and D.W.; validation, A.B. and D.W.; formal analysis, A.B. and D.W.; investigation, A.B. and
D.W.; data curation, A.B. and D.W.; writing—original draft preparation, A.B. and D.W.; writing—
review and editing, A.B., D.W. and K.-P.F.; visualization, A.B. and D.W.; supervision, A.B.; project
administration, A.B. and D.W.; funding acquisition, K.-P.F. All authors have read and agreed to the
published version of the manuscript.
Funding: This work was funded by Federal Ministry of Research, Technology and Space: FKZ 13N16730.
Data Availability Statement: The original contributions presented in this study are included in the
article. Further inquiries can be directed to the corresponding author.
Conflicts of Interest: The authors declare no conflicts of interest. The funders had no role in the design
of the study: in the collection, analyses or interpretation of data; in the writing of the manuscript; or
in the decision to publish the results.

Abbreviations
The following abbreviations are used in this manuscript:
ADC
COTS
CVD
CW
FWHM
GPSDO
HPHT
LED
MW
NV
ODMR
OPM
PC
SNR
SQUIDs
TIA
VNA
ZFS

Analog-to-digital converter
Commercial off-the-shelf
Chemical vapor deposition
Continuous wave
Full width at half maximum
Global positioning system disciplined oscillator
High pressure, high temperature
Light-emitting diode
Microwave
Nitrogen-vacancy
Optically detected magnetic resonance
Optically pumped magnetometers
Personal computer
Signal-to-noise ratio
Superconductive quantum interference devices
Transimpedance amplifier
Vector network analyzer
Zero-field splitting

## PDF page 20

Magnetism 2025, 5, 18

20 of 22

Appendix A
Table A1. Components used in this article.
Component

Description or Part Number

Supplier

Quantity

Price per Piece
[EUR]

Constant current source

LUMITRONIX
Micro-Konstantstromquelle

www.leds.de

1

0.99

LED

C503B-GCN-CY0C0792 or
C503B-GCN-CY0C0791

RS Components

1

0.30

Microdiamond

MDNV150umHi30mg

Adámas
Nanotechnologies

1

~3

578 (30 mg)

Color filter

LEE 027 MEDIUM RED

Thomann

1
(4.5 × 4.0 mm2 )

<0.01

5.50 (per role)

Photodiode

BPW34

RS Components

1

1.20

Optical adhesive

NOA61

Thorlabs

ADF435

ebay

1

~30

RS Components

2

10.60

RS Components

1
1
1
1
1

0.32
17.05
5.87
4.26

1

~74

Microwave generator
board
SMA connector
Capacitor 1 pF
Copper wire
Angled SMA connector
Termination resistor
Operational amplifier
Passives components
for TIA
NV-magnetometer

Amphenol RF
132289
VJ0603D1R0BXPAJ
Ø 0.2 mm
RS Pro
Amphenol RF 132360
OPA140

RS Components
RS Components
RS Components

Resistors, capacitors, connectors

RS Components

All listed components

Price per Sales
Unit [EUR]

40.75
(bottle with 1 oz.)

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

Zhang, H.; Belvin, C.; Li, W.; Wang, J.; Wainwright, J.; Berg, R.; Bridger, J. Little bits of diamond: Optically detected magnetic
resonance of nitrogen-vacancy centers. Am. J. Phys. 2018, 86, 225–236. [CrossRef]
Pogorzelski, J.; Horsthemke, L.; Homrighausen, J.; Stiegekötter, D.; Gregor, M.; Glösekötter, P. Compact and Fully Integrated LED
Quantum Sensor Based on NV Centers in Diamond. Sensors 2024, 24, 743. [CrossRef]
Zheng, D.; Ma, Z.; Guo, W.; Niu, L.; Wang, J.; Chai, X.; Li, Y.; Sugawara, Y.; Yu, C.; Shi, Y.; et al. A hand-held magnetometer based
on an ensemble of nitrogen-vacancy centers in diamond. J. Phys. D Appl. Phys. 2020, 53, 155004. [CrossRef]
Stegemann, J.; Peters, M.; Horsthemke, L.; Langels, N.; Glösekötter, P.; Heusler, S.; Gregor, M. Modular low-cost 3D printed setup
for experiments with NV centers in diamond. Eur. J. Phys. 2023, 44, 35402. [CrossRef]
Stürner, F.M.; Brenneis, A.; Buck, T.; Kassel, J.; Rölver, R.; Fuchs, T.; Savitsky, A.; Suter, D.; Grimmel, J.; Hengesbach, S.; et al.
Integrated and Portable Magnetometer Based on Nitrogen-Vacancy Ensembles in Diamond. Adv. Quantum Tech. 2021, 4, 2000111.
[CrossRef]
Acosta, V.M.; Bauch, E.; Ledbetter, M.P.; Waxman, A.; Bouchard, L.S.; Budker, D. Temperature dependence of the nitrogen-vacancy
magnetic resonance in diamond. Phys. Rev. Lett. 2010, 104, 070801. [CrossRef] [PubMed]
Fan, Z.; Xing, L.; Wu, F.; Feng, X.; Zhang, J. The Optimization of Microwave Field Characteristics for ODMR Measurement of
Nitrogen-Vacancy Centers in Diamond. Photonics 2024, 11, 436. [CrossRef]
Tabuchi, H.; Matsuzaki, Y.; Furuya, N.; Nakano, Y.; Watanabe, H.; Tokuda, N.; Mizuochi, N.; Ishi-Hayase, J. Temperature sensing
with RF-dressed states of nitrogen-vacancy centers in diamond. J. Appl. Phys. 2023, 133, 024401. [CrossRef]
Dolde, F.; Fedder, H.; Doherty, M.W.; Nöbauer, T.; Rempp, F.; Balasubramanian, G.; Wolf, T.; Reinhard, F.; Hollenberg, L.C.L.;
Jelezko, F.; et al. Electric-field sensing using single diamond spins. Nat. Phys. 2011, 7, 459–463. [CrossRef]
Michl, J.; Steiner, J.; Denisenko, A.; Bülau, A.; Zimmermann, A.; Nakamura, K.; Sumiya, H.; Onoda, S.; Neumann, P.; Isoya, J.;
et al. Robust and Accurate Electric Field Sensing with Solid State Spin Ensembles. Nano Lett. 2019, 19, 4904–4910. [CrossRef]
Yang, B.; Murooka, T.; Mizuno, K.; Kim, K.; Kato, H.; Makino, T.; Ogura, M.; Yamasaki, S.; Schmidt, M.E.; Mizuta, H.; et al. Vector
Electrometry in a Wide-Gap-Semiconductor Device Using a Spin-Ensemble Quantum Sensor. Phys. Rev. Appl. 2020, 14, 044049.
[CrossRef]
Doherty, M.W.; Manson, N.B.; Delaney, P.; Jelezko, F.; Wrachtrup, J.; Hollenberg, L.C. The nitrogen-vacancy colour centre in
diamond. Phys. Rep. 2013, 528, 1–45. [CrossRef]
Jelezko, F.; Wrachtrup, J. Single defect centres in diamond: A review. Phys. Status Solidi (A) 2006, 203, 3207–3225. [CrossRef]

## PDF page 21

Magnetism 2025, 5, 18

14.
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

21 of 22

Homrighausen, J.; Horsthemke, L.; Pogorzelski, J.; Trinschek, S.; Glösekötter, P.; Gregor, M. Edge-Machine-Learning-Assisted
Robust Magnetometer Based on Randomly Oriented NV-Ensembles in Diamond. Sensors 2023, 23, 1119. [CrossRef]
Abe, E.; Sasaki, K. Tutorial: Magnetic resonance with nitrogen-vacancy centers in diamond—Microwave engineering, materials
science, and magnetometry. J. Appl. Phys. 2018, 123, 161101. [CrossRef]
Sánchez Toural, J.L.; Marzoa, V.; Bernardo-Gavito, R.; Pau, J.L.; Granados, D. Hands-On Quantum Sensing with NV−Centers in
Diamonds. C 2023, 9, 16. [CrossRef]
Mariani, G.; Umemoto, A.; Nomura, S. A home-made portable device based on Arduino Uno for pulsed magnetic resonance of
NV centers in diamond. AIP Adv. 2022, 12, 065321. [CrossRef]
Soshenko, V.V.; Bolshedvorskii, S.V.; Rubinas, O.; Sorokin, V.N.; Smolyaninov, A.N.; Vorobyov, V.V.; Akimov, A.V. Nuclear Spin
Gyroscope based on the Nitrogen Vacancy Center in Diamond. Phys. Rev. Lett. 2021, 126, 197702. [CrossRef]
Chatzidrosos, G.; Wickenbrock, A.; Bougas, L.; Leefer, N.; Wu, T.; Jensen, K.; Dumeige, Y.; Budker, D. Miniature Cavity-Enhanced
Diamond Magnetometer. Phys. Rev. Appl. 2017, 8, 044019. [CrossRef]
Zhang, C.; Shagieva, F.; Widmann, M.; Kübler, M.; Vorobyov, V.; Kapitanova, P.; Nenasheva, E.; Corkill, R.; Rhrle, O.; Nakamura, K.;
et al. Diamond Magnetometry and Gradiometry Towards Subpicotesla dc Field Measurement. Phys. Rev. Appl. 2021, 15, 064075.
[CrossRef]
Wang, X.; Zheng, D.; Wang, X.; Liu, X.; Wang, Q.; Zhao, J.; Guo, H.; Qin, L.; Tang, J.; Ma, Z.; et al. Portable Diamond NV
Magnetometer Head Integrated With 520 nm Diode Laser. IEEE Sens. J. 2022, 22, 5580–5587. [CrossRef]
Sasaki, K.; Monnai, Y.; Saijo, S.; Fujita, R.; Watanabe, H.; Ishi-Hayase, J.; Itoh, K.M.; Abe, E. Broadband, large-area microwave
antenna for optically-detected magnetic resonance of nitrogen-vacancy centers in diamond. Rev. Sci. Instrum. 2016, 87, 134.
[CrossRef]
Herrmann, J.; Appleton, M.A.; Sasaki, K.; Monnai, Y.; Teraji, T.; Itoh, K.M.; Abe, E. Polarization- and frequency-tunable microwave
circuit for selective excitation of nitrogen-vacancy spins in diamond. Appl. Phys. Lett. 2016, 109, 134. [CrossRef]
Bayat, K.; Choy, J.; Baroughi, M.F.; Meesala, S.; Loncar, M. Efficient, uniform, and large area microwave magnetic coupling to NV
centers in diamond using double split-ring resonators. Nano Lett. 2014, 14, 1208–1213. [CrossRef] [PubMed]
Kuwahata, A.; Kitaizumi, T.; Saichi, K.; Sato, T.; Igarashi, R.; Ohshima, T.; Masuyama, Y.; Iwasaki, T.; Hatano, M.; Jelezko, F.; et al.
Magnetometer with nitrogen-vacancy center in a bulk diamond for detecting magnetic nanoparticles in biomedical applications.
Sci. Rep. 2020, 10, 2483. [CrossRef] [PubMed]
Johansson, S.; Lönard, D.; Barbosa, I.C.; Gutsche, J.; Witzenrath, J.; Widera, A. A miniaturized magnetic field sensor based on
nitrogen-vacancy centers. arXiv 2024, arXiv:2402.19372v3. [CrossRef]
Stürner, F.M.; Brenneis, A.; Kassel, J.; Wostradowski, U.; Rölver, R.; Fuchs, T.; Nakamura, K.; Sumiya, H.; Onoda, S.; Isoya, J.; et al.
Compact integrated magnetometer based on nitrogen-vacancy centres in diamond. Diam. Relat. Mater. 2019, 93, 59–65. [CrossRef]
Abrahams, G.J.; Ellul, E.; Robertson, I.O.; Khalid, A.; Greentree, A.D.; Gibson, B.C.; Tetienne, J.-P. Handheld device for non-contact
thermometry via optically detected magnetic resonance of proximate diamond sensors. Phys. Rev. Appl. 2023, 19, 054076.
[CrossRef]
Hu, Q.; Huang, K.; Mao, X.; Ran, G.; He, X.; Lin, Z.; Hu, T.; Ran, S. Design of high sensitivity magnetometer based on Diamond
Nitrogen-Vacancy Centers and Weak Signal Output Module. Diam. Relat. Mater. 2025, 151, 111858. [CrossRef]
Deguchi, H.; Hayashi, T.; Saito, H.; Nishibayashi, Y.; Teramoto, M.; Fujiwara, M.; Morishita, H.; Mizuochi, N.; Tatsumi, N.
Compact and portable quantum sensor module using diamond NV centers. Appl. Phys. Express 2023, 16, 62004. [CrossRef]
Webb, J.L.; Clement, J.D.; Troise, L.; Ahmadi, S.; Johansen, G.J.; Huck, A.; Andersen, U.L. Nanotesla sensitivity magnetic field
sensing using a compact diamond nitrogen-vacancy magnetometer. Appl. Phys. Lett. 2019, 114, 231103. [CrossRef]
Duan, D.; Du, G.X.; Kavatamane, V.K.; Arumugam, S.; Tzeng, Y.-K.; Chang, H.-C.; Balasubramanian, G. Efficient nitrogen-vacancy
centers’ fluorescence excitation and collection from micrometer-sized diamond by a tapered optical fiber in endoscope-type
configuration. Opt. Express 2019, 27, 6734–6745. [CrossRef]
Fedotov, I.V.; Doronina-Amitonova, L.V.; Voronin, A.A.; Levchenko, A.O.; Zibrov, S.A.; Sidorov-Biryukov, D.A.; Fedotov, A.B.;
Velichansky, V.L.; Zheltikov, A.M. Electron spin manipulation and readout through an optical fiber. Sci. Rep. 2014, 4, 5362.
[CrossRef] [PubMed]
Chen, F.L.; Huang, S.K.; Jiang, T.J.; Yan, F.S. Utilizing a homemade handheld magnetometer to sense nanotesla magnetic fields.
Res. Sq. 2023. [CrossRef]
Qin, L.; Fu, Y.; Zhang, S.; Zhao, J.; Gao, J.; Yuan, H.; Ma, Z.; Shi, Y.; Liu, J. Near-field microwave radiation function on spin assembly
of nitrogen vacancy centers in diamond with copper wire and ring microstrip antennas. Jpn. J. Appl. Phys. 2018, 57, 72201. [CrossRef]
Fedotov, I.V.; Blakley, S.M.; Serebryannikov, E.E.; Hemmer, P.; Scully, M.O.; Zheltikov, A.M. High-resolution magnetic field
imaging with a nitrogen-vacancy diamond sensor integrated with a photonic-crystal fiber. Opt. Lett. 2016, 41, 472–475. [CrossRef]
Don Klipstein. C.I.E. Photopic Luminous Efficiency Function. Available online: https://donklipstein.com/photopic.html
(accessed on 10 July 2025).

## PDF page 22

Magnetism 2025, 5, 18

38.
39.
40.
41.
42.
43.
44.
45.
46.

22 of 22

Ruiz, A.J.; Giallorenzi, M.K.; Hunt, B.; Samkoe, K.S.; Pogue, B.W. Lighting gel filters as low-cost alternatives for fluorescence
imaging and optical system design. Opt. Eng. 2022, 61, 085103. [CrossRef]
Montalti, M.; Cantelli, A.; Battistelli, G. Nanodiamonds and silicon quantum dots: Ultrastable and biocompatible luminescent
nanoprobes for long-term bioimaging. Chem. Soc. Rev. 2015, 44, 4853–4921. [CrossRef]
Würth Elektronik eiSos GmbH & Co., KG. WL-SMTW SMT Mono-Color TOP LED Waterclear: Order Code: 150224GS73100.
Available online: https://www.we-online.com/components/products/datasheet/150224GS73100.pdf (accessed on 10 July 2025).
Cree, Inc. Cree® 5-mm Blue and Green Round LED C503B-BCS/BCN/GCS/GCN. Available online: https://www.farnell.com/
datasheets/1975638.pdf (accessed on 10 July 2025).
O’Haver, T. Smoothing. Available online: https://terpconnect.umd.edu/~toh/spectrum/Smoothing.html (accessed on 19 May 2025).
Omar, M.; Conta, A.; Westerhoff, A.; Hasse, R.; Chatzidrosos, G.; Budker, D.; Wickenbrock, A. Diamond-optic enhanced photon
collection efficiency for sensing with nitrogen-vacancy centers. Opt. Lett. 2023, 48, 2512. [CrossRef]
Zhang, S.; Ma, Z.; Qin, L.; Fu, Y.; Shi, Y.; Liu, J.; Li, Y.J. Fluorescence detection using optical waveguide collection device with high
efficiency on assembly of nitrogen vacancy centers in diamond. Appl. Phys. Express 2018, 11, 13007. [CrossRef]
Reedu GmbH & Co., KG. senseBox: Your Toolkit for Digital Education, Citizen Science and Environmental Monitoring. Available
online: https://sensebox.de/en/ (accessed on 10 July 2025).
Reedu GmbH & Co., KG. QOOOL Sensing—Quantum Sensing for Digital Education. Available online: https://qoool-sensing.
org/en (accessed on 10 July 2025).

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
