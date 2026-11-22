Source: https://www.hb.fh-muenster.de/opus4/files/18207/sensors-24-03138-with-cover.pdf
PDF sha256: 9167d4ad286ab49f1f97ffa18d5c5793b566f46555b2e82eed14b721976f4f27
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: text-layer)

# Transcription of stiegekotter_2024_microcontroller_measurement_electronics_coherent_control_nv.pdf

Transcription of `stiegekotter_2024_microcontroller_measurement_electronics_coherent_control_nv.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

# Article

# Microcontroller-Optimized Measurement Electronics for Coherent Control Applications of NV Centers

Dennis Stiegekötter, Jens Pogorzelski, Ludwig Horsthemke, Frederik Hoffmann, Markus Gregor and Peter Glösekötter

# Special Issue

[Quantum Sensors and Sensing Technology](https://www.mdpi.com/journal/sensors/special_issues/0979AD7W33)

Edited by Dr. Ettore Bernardi

## PDF page 2

*Article*

# **Microcontroller-Optimized Measurement Electronics for Coherent Control Applications of NV Centers**

**Dennis Stiegekötter 1,\* [,](https://orcid.org/0009-0008-2665-1262) Jens Pogorzelski <sup>1</sup> [,](https://orcid.org/0009-0004-1068-0529) Ludwig Horsthemke [1](https://orcid.org/0009-0006-9490-4204) , Frederik Hoffmann <sup>1</sup> [,](https://orcid.org/0009-0008-6945-0751) Markus Gregor [2](https://orcid.org/0000-0003-1099-1445) and Peter Glösekötter [1](https://orcid.org/0000-0002-6937-468X)**

- <sup>1</sup> Department of Electrical Engineering and Computer Science, FH Münster—University of Applied Sciences, Stegerwaldstraße 39, 48565 Steinfurt, Germany; l.horsthemke@fh-muenster.de (L.H.)
- <sup>2</sup> Department of Engineering Physics, FH Münster—University of Applied Sciences, Stegerwaldstraße 39, 48565 Steinfurt, Germany
- **\*** Correspondence: dennis.stiegekoetter@fh-muenster.de

**Abstract:** Long coherence times at room temperature make the NV center a promising candidate for quantum sensors and quantum computers. The necessary coherent control of the electron spin triplet in the ground state requires microwave *π* pulses in the nanosecond range, obtained from the Rabi oscillation of the m<sup>S</sup> spin states of the magnetic resonances of the NV centers. Laboratory equipment has a high temporal resolution for these measurements but is expensive and, therefore, uninteresting for fields such as education. In this work, we present measurement electronics for NV centers that are optimized for microcontrollers. It is shown that the Rabi frequency is linear to the output of the digital-to-analog converter (DAC) and is used to adapt the time length *π* of the electron spin flip, to the limited pulse width resolution of the microcontroller. This was achieved by breaking down the most relevant functions of conventional laboratory devices and replacing them with commercially available integrated components. The result is a cost-effective handheld setup for coherent control applications of NV centers.

**Keywords:** NV center in diamond; quantum sensing; microcontroller; Rabi oscillation; ODMR; handheld; *π* pulse

**Citation:** Stiegekötter, D.; Pogorzelski, J; Horsthemke, L.; Hoffmann, F.; Gregor, M.; Glösekötter, P. Microcontroller-Optimized Measurement Electronics for Coherent Control Applications of NV Centers. *Sensors* **2024**, *24*, 3138. [https://](https://doi.org/10.3390/s24103138) [doi.org/10.3390/s24103138](https://doi.org/10.3390/s24103138)

Academic Editor: Ettore Bernardi

Received: 15 April 2024 Revised: 7 May 2024 Accepted: 10 May 2024 Published: 15 May 2024

**Copyright:** © 2024 by the authors. Licensee MDPI, Basel, Switzerland. This article is an open access article distributed under the terms and conditions of the Creative Commons Attribution (CC BY) license [\(https://](https://creativecommons.org/licenses/by/4.0/) [creativecommons.org/licenses/by/](https://creativecommons.org/licenses/by/4.0/) 4.0/).

# **1. Introduction**

The nitrogen-vacancy center is a solid-state emitter that emits photons by optical pumping with a dependency on the photon intensity from the internal electron spin. This property makes the NV center interesting for an application as a magnetic sensor and is being investigated in detail in this respect. Some integrated sensors have already demonstrated that they could achieve sensitivities of 344 pT/<sup>√</sup> Hz and that the performance can already exceed those of conventional Hall sensors [\[1\]](#page-17-0). The focus is often on miniaturizing the sensor head with the diamond, radio frequency (RF) excitation via an antenna, and a photodiode for detection as a compact component [\[1](#page-17-0)[–4\]](#page-17-1). However, these sensors still require laboratory measuring instruments to evaluate the weak photocurrent signal and are, therefore, anything but easy to transport. Thus, the main focus is on the electronics behind it and not on the integration of a sensor head. The electronics include a switchable source for microwaves in the GHz range, a detector for photodiodes, a lock-in amplifier (LIA) with a low-pass filter for signal acquisition, a microcontroller for the output of pulse sequences, and the data acquisition from the LIA and the control of the microwave source. Research in this direction has been carried out already but does not show a completely integrated solution and is either limited to FPGA-based development boards or the simple plugging together of COTS modules [\[5–](#page-17-2)[7\]](#page-17-3). Pulse sequences needed for various spin manipulation experiments can be programmed using a simple array and can be modified on the fly. The central control of the lock-in reference together with the laser driver and the microwave guarantees synchronization of the individual ICs, which makes phase correction with the

## PDF page 3

LIA obsolete. These features—given by the microcontroller as the central control unit for TIA, LIA, laser drivers, and microwaves—considerably simplify handling. The structure is designed for a  $\pm 9$  V power supply, allowing operation from block batteries. The result is a portable system that can be carried in a pocket. To demonstrate the function, measurements of ODMR and Rabi oscillation are presented, and the  $\pi/2$  time can be adjusted to the output pulse length of the microcontroller with little effort via DAC feedback. This eliminates the need for a high temporal resolution of the pulse sequences, which is otherwise necessary to reduce errors in coherent control.

#### 2. Background

The NV center defect in the diamond crystal structure consists of a substituted nitrogen atom next to a vacancy in the carbon lattice and can be oriented in a total of four spatial orientations. The NV center can be described in a simplified view by an energy level diagram of the spin-triplet states (<sup>3</sup>A and <sup>3</sup>E) as shown in Figure 1a for a single NV center, which is subdivided into the m<sub>S</sub> spin states, and the spin singlet states (<sup>1</sup>A and <sup>1</sup>E) of the electrons. The energetic transition from the ground state <sup>3</sup>A to the excited state <sup>3</sup>E can be achieved by off-resonant excitation with a laser at a wavelength of 520 nm. By decaying back to the ground state <sup>3</sup>A, the NV center emits photons in a wavelength range between 637 nm and 800 nm. In the excited state <sup>3</sup>E, there is also the possibility of decaying back to the ground state <sup>3</sup>A via the singlet states <sup>1</sup>A, <sup>1</sup>E. The probability of this decay path is higher for electrons in the  $m_S = \pm 1$  state than for electrons in the  $m_S = 0$  state. This means that electrons that cycle between the  $m_S = \pm 1$  ground state and the  $m_S = \pm 1$  excited state emit fewer photons than electrons that cycle between the  $m_S = 0$  ground state and the  $m_S = 0$ excited state. The photon difference between  $m_S = 0$  state and  $m_S = \pm 1$  leads to an optical contrast of the luminescence of a maximum of 30% [8-10]. The cycle of optical excitation to the <sup>3</sup>E state followed by decay to the ground state <sup>3</sup>A is spin-preserving. However, if the decay occurs via the singlet state (<sup>1</sup>A, <sup>1</sup>E) to the ground state <sup>3</sup>A, a transition to the  $m_S = 0$  state is possible. This initialization results in a lift of the thermal equilibrium between the  $m_S = 0$  and  $m_S = \pm 1$  states. The spins can be flipped, while still being in the initialized state, between the  $m_S=0$  and  $m_S=\pm 1$  states by an oscillating magnetic field,  $B_{\rm mw}$ , applied perpendicular to the NV axis. This field's frequency must resonate with the Larmor frequency of the electrons. The zero-field splitting (ZFS) of the  $m_S=\pm 1$  states is at  $D=2.87\,\mathrm{GHz}$  and is split apart by an external magnetic field  $B_{\mathrm{||NV}}$  in parallel alignment to the NV axis with the gyromagnetic ratio  $\gamma = 28 \, \text{GHz/T}$  by  $2\gamma B_{\parallel \text{NV}}$ .

#### 2.1. Measurement Protocol

The theoretical 30% contrast is not achieved in the application. This value refers to a single NV center. However, the measurements were performed on a micro-diamond containing an ensemble of NV centers. The lattice structure of the diamond allows the NV centers to adopt four different crystal directions, resulting in the ensemble being equally distributed across these directions. The major factor leading to reduced contrast is the background fluorescence of the NV centers that are not excited to the  $m_S = \pm 1$  state via microwave excitation because the frequency of the microwave can only be tuned to one resonance [8,11]. This causes the SNR to deteriorate. A LIA and a boxcar averager (BCA) are, therefore, implemented in the hardware to measure the weak fluorescence change. The LIA multiplies input signals by a specified reference frequency and filters the mixed signals with a low-pass filter. The result is a bandpass characteristic that detects signals within the low-pass filter bandwidth, centered around the reference frequency. For the reference frequency  $f_{ref} = 1/T$  as a symmetrical square wave and a low pass filter at the output, with a time constant  $\tau = RC >> T = 2\pi/\omega$ , the procedure is simplified to a difference of the mean values in both reference half-waves [12].

$$\langle U_{\text{sig}} \rangle = \frac{2}{T} \int_0^{\frac{\pi}{\omega}} U_{\text{PLsig}}(\omega t) dt - \frac{2}{T} \int_{\frac{\pi}{\omega}}^{\frac{2\pi}{\omega}} U_{\text{PLsig}}(\omega t) dt. \tag{1}$$

## PDF page 4

Sensors **2024**, 24, 3138 3 of 18

In order to measure the spin signals from the fluorescence of the NV centers, these spin signals must be modulated at the reference frequency. Figure 2a illustrates the principle. During the first reference half-wave, a laser pulse polarizes the spins to the  $m_S=0$  state, followed by a microwave pulse that manipulates the spins. A second laser pulse reads out the diamond and simultaneously repolarizes the spins back to the  $m_S=0$  state. In the second reference half-wave, the microwave remains switched off. This leads to a difference in the mean values between spin-manipulated fluorescence in the first reference half-wave and non-spin-manipulated fluorescence in the second reference half-wave [8]. However, signals with a very low duty cycle, such as the  $T_1$  measurement, lead to a deterioration in the signal-to-noise ratio (SNR), making the LIA no longer suitable.

**Figure 1.** (a) Interrelationships of the individual energy levels in the NV center. Ground state  ${}^{3}$ A and excited state  ${}^{3}$ E are separated by 1.945 eV and divided into three  $m_{S}$  states. The green arrow represents the optical pumping of electrons to the excited state, while the red arrow marks the light-emitting decay back to the ground state. The transition can also be non-radiative via the singlet states  ${}^{1}$ A,  ${}^{1}$ E back to the ground state and initialize the electron spins into the  $m_{S}=0$  state. This path is shown by the black arrows. The dashed arrows represent lower-probability decay paths. (b) pulsed ODMR spectrum of the NV ensemble at a microwave power of 17 dBm and a pulse length of 1.2 μs. The four NV axes 1–4 correspond to the eight visible resonances at a static magnetic field  $B_{0}$  perpendicular to the [111] orientation. (c)  $T_{1}$  relaxation of the polarized electron spins from the  $m_{S}=0$  state back into a Boltzmann distribution of the thermal equilibrium without using resonant microwaves. (d)  $T_{2}$  relaxation of the second innermost  $m_{S}=-1$  resonance using a Hahn echo sequence with a spin-flip time  $T_{\pi}=106.6$  ns. The dashed lines in (c,d) correspond to a fit function of the form  $Ae^{-t/T_{x}}+O$  with a decay time constant of  $T_{1}=0.855$  ms and  $T_{2}^{Hahn}=674$  ns.

## PDF page 5

Sensors **2024**, 24, 3138 4 of 18

Figure 2. Measurement principle. (a) The pulse pattern of laser and microwave operations (ODMR, Rabi,  $T_2$ ) is repeated ten times in the first reference half-wave of the LIA. In the second reference half-wave, only the laser pattern is repeated ten times. At the LIA output, the difference is calculated from the fluorescence mean values of the reference half-waves. (b) The integration time window of the BCA only records signals while the laser is active. The  $\tau_{\text{spacing}}$  time is ignored. The mean value is then calculated from N integrals.

In this case, a BCA is the better choice. A BCA multiplies the input signal by a rectangular pulse train, as shown in Figure 2b, which means that only signal components within the boxcar window are integrated. Noise that lies between the pulses is ignored. The integrated signal is averaged over N periods. The BCA measures the change in the fluorescence area of the diamond and can use the same pulse sequences as the LIA. A laser pulse polarizes the spins to the  $m_S=0$  state and a subsequent microwave pulse manipulates the spins (or, as in the case of the  $T_1$  measurement, without microwaves at all). A second laser pulse then reads the NV centers and the fluorescence is integrated. The process is repeated N times and the mean value of the area is calculated.

#### 2.2. Detection of Spin Signals

A simple permanent magnet, generating the magnetic bias field  $B_0 = 15$  mT, is placed near the diamond. The four different orientations of the NV center axis result in eight detectable magnetic resonances. Based on the ODMR pulse pattern outlined in Figure 2a, the measurement is repeated in 1 MHz steps with a pulse width of  $\tau_{mw}$  = 1.6  $\mu$ s, at a power of 17 dBm. Feeding ten repetitions of the ODMR pattern for the laser and microwave into the low-pass filter in the first half-wave of the LIA reference [8] results in the fluorescence signal in Figure 1b. The Lorentz-shaped signals in the frequency range from 2.55 GHz to 3.25 GHz correspond to the contrast differences of an NV axis as soon as the frequency is in resonance with the transitions  $m_S = 0$  and  $m_S = \pm 1$ . The eight different resonant frequencies result from different  $B_{\parallel NV}$  for each axis as a result of the different orientations in the diamond and their angle to the  $B_0$  field of the permanent magnet. The low contrast of axis 1 is caused by its orientation in the diamond (more about the axis orientation in Section 4). The decrease in contrast toward low and high frequencies is due to the 400 MHz bandwidth of the antenna used. Deviating center frequencies (CF) from the ZFS with CF1 = 2.934 GHz, CF2 = 2.933 GHz, CF3 = 2.897 GHz, and CF4 = 2.887 GHz are calculated from resonances 1–4. The drift is due to the non-axial magnetic field component  $B_{\perp}$ , which is present at the NV center and cannot be neglected for magnetic flux densities in the 10 mT range [13].

A simple method to determine the  $T_1$  relaxation is to polarize the spins according to the pulse pattern in Figure 2b and optically read out the distribution of the  $m_S$  states after time  $\tau_{\rm spacing}$ . Figure 1c shows the calculated fluorescence area as an exponentially decaying curve as a function of the pulse spacing  $\tau_{\rm spacing}$  in 100  $\mu$ s steps, for a time interval of 5 ms. This measurement is performed without a microwave and only the laser is pulsed. In the time  $\tau_{\rm spacing}$  between the laser pulses, the polarized spins decay from the  $m_S=0$  state and reoccupy the  $m_S=\pm 1$  states. With increasing  $\tau_{\rm spacing}$ , the occupation also increases until thermal equilibrium is reached again. The proportion of spins in the  $m_S=\pm 1$  states

## PDF page 6

Sensors **2024**, 24, 3138 5 of 18

increases the contrast and leads to a falling curve in the output signal. The measured  $T_1$  time is 0.855 ms and is, thus, within the expected time range of NV centers in HPHT diamonds, which have a relaxation time constant of a few milliseconds at room temperature [14].

For more complex measurements, such as the  $T_2$  time constant, coherent control of the electron spin is required. Coherent control is achieved when the spins can be controlled from the initial state  $m_S=0$  to a target state by an external alternating magnetic field  $B_{\rm mw}$  perpendicular to the NV axis. The time to flip the electron spin from the  $m_S=0$  state directly to the  $m_S=\pm 1$  state is called  $\pi$  pulse and is determined in Section 4 with a time of 106.6 ns by measuring the Rabi oscillation.

 $T_2$  describes the transverse decay, which results from a change in the phase coherence of the precessing spins. Since the phase coherence of the spins drifts apart at a constant rate in the case of static inhomogeneities, this process can be reversed by a  $\pi$  pulse, so that the phases of the spins drift toward each other at the same rate. This approach is also known as the Hahn echo sequence [15], outlined in Figure 2a. The  $T_2$  measurement in Figure 1d examines the single resonance at 2.878 GHz with a power  $P_{mw} = 17$  dBm. First, the spins are polarized to the  $m_S = 0$  state and brought into superposition between  $m_S = 0$  and  $m_S = -1$  state by a  $\pi/2 = 53.3$  ns microwave pulse. The spins then 'precess' freely for a time  $\tau$  and are varied in a range between 106 ns to 5.2  $\mu$ s with a step size of 53.3 ns. A  $\pi$ pulse then changes the direction of propagation of the phases for a further  $\tau$  before readout. The exponential curve of the LIA signal is caused by interactions between the electron spins with the spin bath within the time  $\tau$  of free precession. The influence of the spin bath can be described as fluctuating magnetic fields at the NV center [16] that arise in the diamond mainly from impurities with P1 centers [17,18]. This leads to a dephasing of the electron spins in superposition. At the end of the sequence, some spins are, therefore, in the  $m_S = -1$  state again. The occupation of the  $m_S = -1$  state increases with increasing  $\tau$ and leads to a rise in contrast.  $T_2^{\text{Hahn}} = 674 \text{ ns}$  was measured from the output signal. A low  $T_2$  time in the lower  $\mu s$  or ns range indicates high contamination of the diamond with P1 centers [17] and determines the time range in which coherent control can be applied before the signal is lost in noise.

The measurements in Figure 1b–d confirm the function of the measuring device. However, the measurements also show that the performance is dependent on the applied static magnetic field  $B_0$ . A larger  $B_0$  field splits the resonances further outside of the bandwidth of the antenna and the contrast of the resonances reduces significantly. The larger splitting also requires a wider frequency range to be scanned in order to capture all resonances. Due to the fixed time constant of the LIA filter, the scanning time for the measurement increases if the frequency step size is kept constant. For the application as a sensor, it must be taken into account that the resonances do not evolve linearly with the magnetic field because of the non-axial magnetic field component  $B_{\perp}$ .

#### 3. Hardware Development

Both the detection and the excitation of the spin-dependent fluorescence are performed via the modules shown in Figure 3 and their interconnection. The pulse sequences for the microwave generator and laser driver required for spin manipulation are controlled centrally by a microcontroller (STM32G491, STMicroelectronics, Geneva, Switzerland). The photodiode signals (S5971, Hamamatsu Photonics K.K., Hamamatsu City, Japan) are processed by an analog LIA (AD630, Analog Devices Inc., Norwood, MA, USA) with a following low-pass filter at a cut-off frequency of 1 Hz. The sample rate of the analog-to-digital converter (ADC) is reduced to the settling time of the filter. The data are transmitted via a universal serial bus interface and can be plotted on a PC. To excite the resonances, a serial peripheral interface (SPI) controlled phase-locked loop (PLL) (ADF4351, Analog Devices Inc., Norwood, MA, USA) with an output frequency range between 35 MHz and 4400 MHz is used. The amplitude can be adjusted with the DAC 1 signal of the microcontroller via an I/Q modulator (LTC5589, Analog Devices Inc., Norwood, MA, USA) to vary the microwave power.

## PDF page 7

*Sensors* **2024**, *24*, 3138 6 of 18

**Figure 3.** Schematic diagram of the measurement electronics and the optics as a setup in blue. The black arrows show the electrical paths between the individual modules, while red and green represent the fluorescence of the NV diamond and the excitation light. Light blue shows the peripherals used by the microcontroller.

### *3.1. Bootstrapped Transimpedance Amplifier*

The photodiode is mounted at the end of a shielded cable as shown in Figure [4a](#page-7-0) and is connected to the transimpedance amplifier (TIA) with a sub-miniature version A (SMA) screw connector so that the measuring electronics have a purely electrical interface and do not require any optical components such as fiber couplers, dichroic mirrors, etc. A high SNR is crucial for detecting weak signals with sufficiently high bandwidth to follow the edges of the pulses. In conventional NV readout methods, a difference in the fluorescence rate between the m<sup>S</sup> = 0 state and the m<sup>S</sup> = ±1 state can be measured in the first 500 ns [\[18](#page-17-13)[,19\]](#page-17-14). The bandwidth of the detector should therefore be at least 2 MHz. The incoming photons of the NV centers are Poisson-distributed and are detected as individual particles in the PN junction of the photodiode. This process is stochastic and leads to a noise current *i*Nshot = p 2*qI* where *q* is the elementary charge and *I* is the photocurrent. It is, therefore, independent of the temperature and increases with the root of the photocurrent. Thermal noise, on the other hand, is caused by fluctuations in the charge carrier velocity in the conduction band of the TIA feedback resistor *R<sup>f</sup>* . These fluctuations are caused by thermal energy and lead to a noise current *i*Nth = √ 4*kT*/*R* with the Boltzmann constant *k*. The noise current is in turn independent of other currents and depends on the temperature and the resistance value. In optical measurements, the shot noise sets the limit for the sensitivity. Improvements in the SNR can then only be achieved by increasing the photocurrent or lowering the bandwidth. Therefore, the construction of the TIA should ensure that the shot noise dominates within the desired bandwidth at a given photocurrent. The SNR of the signal depends on the ratio of the two noise sources *i*Nth/*i*Nshot, as well as the input current noise *i*Namp and input voltage noise *e<sup>n</sup>* of the operational amplifier (OpAmp). The SNR decreases if one of these noise sources becomes larger compared to the shot noise [\[20\]](#page-17-15). A simple way to reduce *i*Nth is to increase the resistance value *R<sup>f</sup>* . However, a larger *R<sup>f</sup>* also reduces the bandwidth of the detector and forms, with the input capacitance of OpAmp and the capacitances of the photodiode as well as the line, a low-pass filter with the cutoff frequency *f*RC = 1/2*πR<sup>f</sup> C*in. An acceptable compromise is achieved with *i*Nth = 0.5 · *i*Nshot, which is accompanied by a loss of 1 dB in SNR and an output voltage at the TIA of 200 mV at room temperature [\[20\]](#page-17-15). *i*Namp and *e<sup>n</sup>* depend on the specification of the OpAmp. For FET inputs, *i*Namp is small compared to *e<sup>n</sup>* and the input voltage noise dominates for low light intensity with large *R<sup>f</sup> C*in. An equivalent noise current *i<sup>N</sup>* = *enωC*in results from *R<sup>f</sup>* and *C*in, which is proportionally dependent on the input capacitance and the angular frequency *ω* [\[12](#page-17-7)[,20\]](#page-17-15). To increase the bandwidth and minimize the influence of *iN*, the capacitive load at the summing node of the OpAmp can be reduced with a bootstrap circuit. So, when choosing a suitable amplifier, *e<sup>n</sup>* should be as small as possible. Also, when selecting a suitable photodiode, care should be taken to ensure a low junction capacitance, *C<sup>d</sup>* . The value depends on the expansion of the space charge region and can be decreased with little effort by a negative bias at the anode by a factor of 7–10, this only increases the leakage

## PDF page 8

Sensors **2024**, 24, 3138 7 of 18

current and decreases the SNR for negligible 0.004 dB [12,20]. Since the photodiode is at the end of a shielded cable, a non-negligible capacitance,  $C_l$ , is also introduced with  $\approx 100 \text{ pF/m}$  [12]. To counteract this, an AC-coupled bootstrap is connected between the summing node of the TIA and the cable. Figure 4a shows the entire circuit. The bootstrap copies a replica of the high-side signal, AC coupled to the low-side of the cable output. The replicated signal reduces recharging of the effective capacitances of the photodiode and cable, which decreases the effective capacitance at the summing node and attenuates it by typically a factor of 10. A signal at the summing node is copied across the junction field effect transistor (JFET) follower  $Q_1$  and AC coupled through a buffer  $Q_2$  via capacitor  $C_{\rm ac}$  to the anode of the photodiode. Negative bias is applied across  $R_1$  and prevents shorting with the signal across  $C_{\rm ac}$  [12].  $R_2$  and  $R_4$  are dimensioned so that a voltage of 0 V is applied to the buffer output at rest.  $R_3$  limits the current through JFET  $Q_1$  with  $R_4$ . The feedback capacitance  $C_f$  is calculated from

$$C_f = \frac{1}{2\pi R_f \sqrt{f_T \cdot f_{RC_{\text{in,eff}}}}} \tag{2}$$

with  $f_T$  as the transit frequency of the used OpAmp and  $C_{\text{in,eff}} = \frac{1}{10}(C_d + C_l) + C_{\text{rss}} + C_{\text{amp}}$  effective capacitance.  $C_d$  is the capacitance of the photodiode,  $C_l$  is the capacitance of the cable,  $C_{\text{rss}}$  is the reverse transfer capacitance, and  $C_{\text{amp}}$  is the capacitance of the OpAmp input. For exact component values see Appendix A.1.

**Figure 4.** Electronics design for (a) bootstrapped photodetector with an additional transistor driver stage Q2. (b) The configuration of the AD630 IC as an analog LIA with a third-order active multiple feedback filter (MFB).

#### 3.2. Lock-In-Amplifier and Boxcar Averager

The luminescence signals from the NV centers provided by the TIA are demodulated in the next step using the analog LIA. The demodulator is specified with a bandwidth of 350 kHz, a slew rate of  $45 \text{ V/}\mu\text{s}$ , and a signal amplification of 100 dB. The input signal is mixed with a square wave by alternately switching the positive amplifier (AMP) A and the negative AMP B to the output filter by means of a reference frequency-controlled FET switch. The internal structure is sketched in Figure 4b with the corresponding component values in Appendix A.2. AMP A closes the path to the filter in the first half of the reference signal, while AMP B closes the path to the filter in the second half of the reference signal. To allow the amplitude response to fall sharply outside the 1 Hz range, the filter has an

## PDF page 9

Sensors **2024**, 24, 3138 8 of 18

order of N=3 and thus an attenuation of 60 dB per decade. Figure 4b shows the filter cascade at the output of the LIA, consisting of a first-order inverting low-pass filter and a second-order multiple-feedback topology in series. Compared to the Sallen–Key design, the MFB filter has a higher quality factor and is better suited for larger gains [21]. The weak fluorescence signals are amplified by the filter with a factor of 100. The transfer function of the entire filter is calculated by multiplying the transfer functions of the individual filters to give

 $G(s) = \frac{A_1}{1 + a_1 s} \cdot \frac{A_2}{1 + a_2 s + b_2 s^2} \tag{3}$ 

The filter coefficients determine the frequency response and are selected according to Table 1 with a Butterworth characteristic to provide a maximally flat passband [21].

A boxcar averager is implemented by using the PWM channel of timer 2 for pulse output to the laser driver. At the same time, the counter status is monitored in a second channel of the timer and an interrupt is triggered before the PWM output switches to a high level. The TIA is connected to a general-purpose input/output (GPIO) port to which two ADCs have access. The two ADCs achieve a sampling rate of 8 Msps with 12-bit resolution in interleaved mode and sample the GPIO port alternately. The samples of the ADCs are stored in a common data register. Within the interrupt routine, the processor reads the data register each time the end-of-conversion flag of each ADC is set. The sampling process is repeated until a total of ten register values have been recorded. The integral is then calculated from the recorded samples according to the extended Simpson's rule [22]


$$\int_{x_1}^{x_N} f(x) \, dx = \frac{h}{3} \left( \sum_{n=2}^{N-1} ((-1)^n + 3) x_n \right) + \frac{h}{3} (x_1 + x_N) \tag{4}$$

with h = 125 ns as the time difference between sampled values. Equation (4) is executed by the microcontroller after the interrupt routine and the calculation result is processed to determine the average value.



| <b>Table 1.</b> Component calculation with filter coefficients and the corresponding values for a Butterworth |
|---------------------------------------------------------------------------------------------------------------|
| characteristic. Index 1 for the first-order filter and index 2 for the second-order filter.                   |

| Coefficient | Butterworth | Formula                                                                                                                                                                          |
|-------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $a_1$       | 1           | $\omega_{g}R_{4}C_{3}$ $\omega_{g}C_{1}\left(R_{2}+R_{3}+\frac{R_{2}R_{3}}{R_{1}}\right)$ $\omega_{g}^{2}C_{1}C_{2}R_{2}R_{3}$ $-\frac{R_{4}}{R_{5}}$ $-\frac{R_{2}}{R_{1}^{2}}$ |
| $a_2$       | 1           | $\omega_g C_1 \left( R_2 + R_3 + \frac{R_2 R_3}{R_1} \right)$                                                                                                                    |
| $b_2$       | 1           | $\omega_g^2 C_1 C_2 R_2 R_3$                                                                                                                                                     |
| $A_1$       | _           | $-\frac{R_4}{R_5}$                                                                                                                                                               |
| $A_2$       | _           | $-\frac{\widetilde{R}_2^2}{R_1}$                                                                                                                                                 |
| $f_{g1}$    | 1 Hz        | _                                                                                                                                                                                |
| $f_{g2}$    | 1.272 Hz    | -                                                                                                                                                                                |

#### 3.3. Microwave Source

The internal electron spin of the NV centers is manipulated by excitation with microwaves that resonate with the Larmor frequency of the electrons. These microwaves are generated using a voltage-controlled oscillator (VCO) and can be set to precise values within a controlled loop. The design of the filter and the output of the PLL correspond to the topologies from the data sheet of the ADF with a balun at the differential outputs  $RF_{\text{out}}A+$  and  $RF_{\text{out}}A-$  for 3 dB more output power compared to a single-ended application. An overview of the wired ICs can be seen in Appendix A.3. The PLL serves as a local oscillator for the I/Q modulator, its in-phase and quadrature inputs are differential at a common mode voltage level of 1.4 V and are driven by the microcontroller's 12-bit digital-to-analog converter. The signal at frequency  $f_{\text{LO}}$  is fed into the I/Q modulator via an LC matching network, passing through a phase shifter, and is split into two paths that are 90° out of phase with each other. The modulator supports DC coupling at the

## PDF page 10

*Sensors* **2024**, *24*, 3138 9 of 18

inputs and can vary the output power with the DAC (with differential mode driver). The external circuit design is based on its evaluation board (DC2391A, Analog Devices Inc., Norwood, MA, USA). RF switches (M3SWA2, Mini-Circuits, Brooklyn, NY, USA) are used to pulse the microwave with a duration of *τ*mw. These have a rise/fall time of 6 ns and are switched via transistor-transistor-logic (TTL) logic. As the output power of the PLL has a maximum of 5 dBm and is subject to further losses due to lossy transmission lines, I/Q modulator, and RF switches, the modulated and pulsed output frequency is amplified by a gain stage with three adjustable levels, as shown in Figure [5a](#page-9-0). The antenna for microwave excitation corresponds to the design of Sasaki et al. [\[23\]](#page-17-18). They achieved a Rabi frequency of 4.6 MHz at a power *P*mw = 1 W using an N-doped type IIA substrate diamond [\[23\]](#page-17-18). This indicates that due to the angle between *B*mw and the NV axes, less power is required with an NV axis alignment to achieve the same Rabi frequency. Therefore, the first path (1) contains a cascade of two gain block amplifiers (GRF2012, Guerrilla RF Inc., Greensboro, NC, USA), which each have a gain of 14.8 dB and a 1-dB compression point of 23 dBm at a voltage supply of 5 V and a current of 100 mA. The resulting amplification of the cascade is therefore 29.7 dB. The second path (1.1) passes through a single amplifier with a gain of 14.8 dB. At the third path (1.2), the microwave is provided without gain via a coaxial jack and corresponds to the power of the I/Q modulator minus attenuations due to switches as well as line reflections. In any case, we can control the power by the DAC and I/Q modulator.

**Figure 5.** (**a**) Fully assembled demonstrator in an SLA-printed package. The dimensions are 82 mm × 167 mm. (**b**) Optical assembly, manufactured with a stereolithography (SLA) printer. The simple design uses a minimum of optical components and only requires an adjustable collimator lens for the laser diode as well as a filter for the photodiode. (**c**) Microscope image of the 200 µm NV diamond in the center hole of the antenna [\[23\]](#page-17-18) at a front view. Crystal axes are drawn based on the geometry with the [111] orientation perpendicular to the antenna. (**d**) Side view with the measured angle between the (111) and (001) planes.

#### *3.4. Microcontroller*

The control of the individual modules on the board is handled by the microcontroller with an ARM Cortex-M4 processor at a clock frequency of 150 MHz. In addition to calculating the register contents of the I/Q modulator and the PLL, the pulse sequences are implemented using the GPIO peripherals. In order to be able to stream more complex

## PDF page 11

pulse patterns such as the Hahn-echo-Sequence, functions like pulse-width-modulation are unsuitable. The simplest solution is to update the GPIO ports at equidistant time points and switch the corresponding ports on or off, as required. The information about which GPIO outputs are set or reset is stored in a  $1 \times 1440$  32-bit array in the SRAM2 memory to modulate the laser and microwave and provide a reference for the LIA. Placement in the SRAM2 is necessary to ensure the lowest possible jitter so that the bus connection between the DMA controller and GPIO port A is free of all other signals and there is no transmission delay. These bit masks are written via the direct memory access (DMA) controller directly into the GPIO bit set and reset register (BSRR) in which the first half-word defines the pins to be set and the second half-word specifies which ones are reset. Pulses can be generated at the respective outputs by means of periodic write commands, the length of which depends on the period duration and the interval between the set and reset instructions. A DMA data transfer is triggered via the TRGO signal at each update event of timer 2 and increments the DMA pointer to the next position in the array. The entire process requires eight clock cycles, which results in the minimum pulse width of  $T_{p,min} = 8/150 \text{ MHz} = 53.3 \text{ ns}$ . The size of the array determines the reference frequency with  $1/L_A T_{p,min}$ . Once started, the array is passed through circularly. Every 700 ms an interrupt of timer 6 is triggered, via which the callback function takes a sample of the filter. Afterward, either the frequency for ODMR or the pulse pattern can be modified for the next sample.

#### 4. Setup and Optimization

The NV diamond used is a high-pressure, high-temperature (HPHT) 150  $\mu m$  microdiamond (MDNV150umHi50mg, Adámas Nanotechnologies, Raleigh, NC, USA) with a NV concentration between  $\approx 2.5$ –3 ppm. The sample is located in the hole of the planar ring antenna, with a spatially homogeneous magnetic field distribution within an area of 1 mm² [23] parallel to one of the [111] NV axes. The orientation of the diamond is determined by its geometry. Diamonds grow in discrete directions with the crystal axes as the normal vector to the growth surface. Hexagonal sectors correspond to the NV axes, while octagonal sectors are assigned to the [100], [010], and [001] directions [24]. In Figure 5c, the hexagonal structure can be clearly recognized by the top view. To confirm the orientation, the angle to the (001) surface is measured at a 90° angle to the [111] axis as shown in Figure 5d. In theory, the calculated angle between the (111) and (001) surface is 125.3°, and the measured values are between 120° and 130° and, thus, lie in an area that excludes any confusion with another NV surface that is separated by 109.28°.

The printed circuit board (PCB) antenna is clamped in a 3D-printed structure (see Figure 5b) and is located vertically below a laser diode (PLT5 520B, OSRAM GmbH, Munich, Germany). The laser is encapsulated in an adjustable collimator (LDA-56, Roithner Lasertechnik GmbH, Vienna, Austria) and is emitting light at a wavelength of 520 nm. To collect the fluorescence, the photodiode is placed at an angle to the antenna with a glued-on long-pass filter (OG590, Schott AG, Mainz, Germany) and is connected via a shielded cable to suppress interfering signals. The largest contrast in Figure 1b results for the resonances with the crystal orientation  $[11\overline{1}]$  and  $[\overline{1}\overline{1}1]$  (see Figure 5c), which are approximately perpendicular to the applied bias magnetic field and lie within the 400 MHz antenna bandwidth. The innermost resonances correspond to the [111], [111] NV axis and emit with low contrast, as they are aligned parallel to the alternating magnetic field  $B_{\text{mw}}$ of the antenna. The resonance splitting and crystal orientation enable a single resonance to be filtered out that deviates by 19.23° from the vertical of the antenna's alternating magnetic field  $B_{\rm mw}$ . A good microwave excitation plays an important role in measuring the Rabi oscillation when it comes to obtaining a fast fundamental Rabi frequency. Therefore, the microwave frequency is fixed to the  $m_S = -1$  resonance at 2.822 GHz and a sweep of the pulse width  $\tau_{\rm mw}$  is run to measure the Rabi oscillation. The oscillation as a function of the pulse length  $\tau_{\rm mw}$  can be described with an exponentially decaying sine function.


$$S_{\text{rabi}}(\tau_{\text{mw}}) = A \sin\left(2\pi f_{\text{rabi}} \cdot \tau_{\text{mw}} + \phi\right) e^{-\frac{\tau_{\text{mw}}}{T_2^{\text{rabi}}}} + m\tau_{\text{mw}} + b \tag{5}$$

## PDF page 12

where A is the amplitude of the Rabi oscillation,  $f_{\rm rabi}$  is the Rabi frequency,  $\phi$  is the phase offset,  $T_2^{\rm rabi}$  is the decay time constant, m is the slope to counteract temperature drift and b is the signal offset [8]. The orange curve in Figure 6a depicts a  $\pi$  pulse at a microwave power of 17 dBm with approximately 106.6 ns.

Figure 6. (a) Change of the Rabi oscillation of the second innermost  $m_S = -1$  resonance when the microwave power is reduced to one-eighth step. The blue line refers to an interpolated and fitted exponential decay to the 0 dB curve. (b) Extracted Rabi frequency from the found fit parameters of Equation (5) versus the root of the power. The dependency can be described as a linear relationship. (c) Step increase in DAC value at the I input of the I/Q modulator at a fixed frequency of 2.87 GHz. The red measuring points have a distance of 100 and also show a linear relationship to the output power.

#### Control of Rabi Frequency

If the time for a  $\pi$  pulse does not match the time resolution of the microcontroller  $T_{p,min}$ , or integer multiples  $NT_{p,min}$ , the applied operations lead to coherent errors. To reduce these errors, it is not necessary to increase the resolution if the Rabi oscillation can be matched to any value for a  $\pi$  pulse through the control of the microwave power. Since  $B_{\rm mw} \propto I_{\rm mw} = \sqrt{P_{\rm mw}}/R$ , the Rabi frequency should be linearly dependent on the square root of the power. For verification, the output power is attenuated in 9 dB steps and contrasted in Figure 6a. These are fitted to an exponentially decaying sinusoidal function, and the respective Rabi frequency is read from the fit parameters. Then, the power  $P_{\rm mw}$  is determined and the square root is taken. The comparison between  $\sqrt{P_{\rm mw}}$  and  $\Omega_R$  in Figure 6b shows the linear relationship. The I/Q modulators I and Q inputs are analog mixers whose input signal is multiplied by the local oscillator signal. For a DC voltage from the DAC to I, the amplitude of the output frequency becomes the product  $U_{\text{mod}}(t) = U_{\text{dac}}U_{\text{lo}}(t)$  and is proportional to the DAC voltage. This means that due to the relationship  $U = R\sqrt{P}$ , the square root of the output power is also in a linear relationship with  $U_{\rm dac}$ . The output frequency is fixed at 2.87 GHz in continuous wave (CW) mode, and the output power is recorded for all 100 DAC step values. The individual measurement points are converted to power  $(P_{mw})$  before the root is taken.

Figure 6c shows a clear, linear relationship between  $\sqrt{P_{\rm mw}}$  and the DAC value. The measured data points are plotted in red, while the blue represents the fit using a linear magnitude function. The characteristic V-shape results from the hardware implementation. The I and Q inputs of the modulator are differentials around an average value of 1.4 V. If the DAC is increased, the differential voltage decreases and overlaps at the point  $U_{\rm dac}/2$

## PDF page 13

before it increases again. The result is the characteristic V-shape. From the two results, we can now conclude that the frequency of the Rabi oscillation is linearly dependent on the voltage level of DAC. This observation makes it very useful to fit the  $\pi$  or  $\pi/2$  time to the limited resolution of  $T_{\rm mw}$ . With  $\pi$  as the half oscillation period and  $T_{\rm mw}=NT_{\rm p,min}$ , we obtain  $\Omega_R=2\pi/(2NT_{\rm p,min})$ , with which the respective DAC value over both straight-line equations is determined to

$$\sqrt{P_{\rm mw}} = \frac{\Delta\sqrt{P_{\rm mw}}}{\Delta\Omega_R} \Omega_R + b_{\Omega_R} \tag{6}$$

$$\sqrt{P_{\rm mw}} = \frac{\Delta \sqrt{P_{\rm mw}}}{\Delta C} C + b_C \tag{7}$$


$$\Rightarrow C = \frac{b_{\Omega_R} - b_C}{\Delta \sqrt{P_{\text{mw}}} / \Delta C} + \frac{\Delta C}{\Delta \Omega_R} \frac{2\pi}{2NT_{\text{p,min}}} \tag{8}$$

The Rabi frequency depends mainly on the oscillating magnetic field perpendicular to the NV symmetry axis and the microwave power used. Slight differences in the angle between the  $B_{\rm mw}$  component of the microwave and one of the [111] axes of different NV samples will lead to different Rabi frequencies. To determine the straight-line equation for a given resonance, it must be calibrated initially using at least two measured frequencies. Fast Fourier transformation (FFT) analysis is a widely used and well-understood method to decompose a signal into its frequency components. Therefore, a routine for calibration using the rfft function from the CMSIS library [25] is implemented on the microcontroller, which transforms the Rabi signal into the frequency domain and filters out the dominant frequency. The sampled signal is stored in an array and to minimize the DC component, the value of the last sample is subtracted from the entire array at the end of the measurement. The signal is only recorded for 30 values because, due to a small decay time constant  $T_2^{\rm rabi}$ , it does not contain any more significant information and would only drag out the measurement. Instead, zero padding is used to stretch the signal to 256 values before transforming it.

Zero padding does not improve the real frequency resolution, but the FFT output signal is interpolated and can be processed by a peak detection function. Figure 7a shows the calculated spectra for two different DAC values. The colored points are the resonance frequencies where we measured a shift of 2.197 MHz for a DAC difference of 1000. From these values follows the calculation of the required parameters with  $\Delta C/\Delta\Omega_R = -4096/18\pi$ and  $(b_{\Omega_R} - b_C)/(\Delta\sqrt{P_{mw}}/\Delta C) = 2200$ , which the microcontroller uses for the application of Equation (8). Figure 7c shows the application of the equation for different pulse lengths of the size  $NT_{p,min}$  of the microwave in blue and represents the time of the measured  $\pi$ pulse. For this measurement, the respective Rabi oscillation was fitted to Equation (5), the result was derived and the first zero crossing was calculated. The ideal curve is shown as a black dashed line and shows that the measured  $\pi$  pulse duration deviates from the pulse length of the microwave. The reason for the deviation is the changing phase of the fundamental frequency, which leads to a standard deviation of  $\sigma_b = 42.77$  ns between the blue data points and the dashed line. The relationship between the phase position of the Rabi oscillation and the DAC output can be calculated directly from the FFT and is shown in Figure 7b in radians. The dashed regression line also indicates a linear relationship to the DAC value. The temporal deviation can be calculated from the phase using the relationship  $t_{\rm diff} = \phi_R/2\pi f_R$ , based on an initial phase of the Rabi frequency of  $\pi$  (180°). Combined with the linearity, t<sub>diff</sub> is used in the microcontroller to correct the output value of the DAC in order to minimize the standard deviation between the  $\pi$  pulse and the length of the microwave pulse. First, the register value C is calculated according to Equation (8) and inserted into the linear equation of the phase position. The correction value is calculated according to the following:


$$t_{\rm adj} = \frac{\Phi_R}{2\pi \frac{1}{NT_{\rm action}}} \tag{9}$$

## PDF page 14

*Sensors* **2024**, *24*, 3138 13 of 18

and is added to the denominator of the original Equation [\(8\)](#page-12-0) to calculate the adjusted register value. The red data points in Figure [7c](#page-13-0) are the same measurements as in blue, but with a correction of the phase shift. The resulting standard deviation is then reduced to *σ<sup>r</sup>* = 7.53 ns.

**Figure 7.** (**a**) FFT spectra calculated by the microcontroller correspond in color to the Rabi oscillation insets. The measured frequency in resonance at 2.872 GHz (red ODMR signal) shifts from 4.83 MHz (blue) to 2.64 MHz (green) for a DAC change of 1000. (**b**) Phase shift of the fundamental Rabi oscillation for decreasing microwave power through the DAC from an initial position of *π*. (**c**) Time to reach the m<sup>S</sup> = ±1 state for a microwave pulse of length *NT*p,min in blue using Equation [\(8\)](#page-12-0). Extension of the equation by a compensation of the phase shift in red.

#### **5. Conclusions and Outlook**

In summary, we present a low-cost and portable measurement device for NV centers based on a microcontroller. The pulse sequences required for typical measurements, such as ODMR, Rabi oscillation, or Hahn echoes were recorded via a programmable pulse pattern, and the resulting fluorescence change of the diamond was measured with the ADC of the microcontroller. The linear dependence of the Rabi frequency on the output of the DAC was utilized to match the *π* pulses required for coherent control to the limited temporal resolution of the microcontroller's GPIO pulses. The process yielded a standard deviation of *σ<sup>r</sup>* = 7.53 ns, which is better compared to similar microcontroller-based systems with 62.5 ns [\[5\]](#page-17-2) but does not come close to the resolution of commercially available pulse generators with 2 ns [\[8\]](#page-17-4). FPGA-based setups also achieve minimal pulse widths in the single-digit nanosecond range [\[26](#page-17-21)[,27\]](#page-17-22). However, the measurement electronics presented in this work still leave enough room for future improvements. We expect to further increase the accuracy by making the FFT resolution finer to better fit the linear equations of Equations [\(8\)](#page-12-0) and [\(9\)](#page-12-1). This can be achieved by using a less doped NV diamond, which results in a longer coherence time [\[17,](#page-17-12)[28\]](#page-18-0) and the Rabi oscillation can be sampled for a longer period of time. Additionally, a decrease in microwave power with increasing time was observed, which has a direct influence on the Rabi oscillation and requires further investigation for compensation. Overall, other parameters such as the temperature dependency of the microwave power of the unregulated microwave source can be determined in order to include them in the calculation of the DAC value. Despite the possibilities for improvement, the handheld measuring device shown here is the prototype that was

## PDF page 15

*Sensors* **2024**, *24*, 3138 14 of 18

produced with a total material cost of less than USD 300. There are exclusively commercially available electronic components on the circuit board, which makes machine assembly possible. The existing demonstrator can therefore be produced on an industrial scale and the costs reduced even further. The total power consumption is only 5.4 W and offers further savings potential by improving the RF technology. However, the device can already be operated with a battery pack, making it very easy to handle. Combined with the simple programming of the pulse sequences, which are required for coherent control, their use in educational settings will be promising, as students can be introduced to future technologies and learn about quantum-based sensor technology or quantum computing. The developed system also offers advantages outside of laboratory environments. By replacing the SLAprinted structure with a compact sensor head, as in Pogorzelski et al. [\[2\]](#page-17-23), or by extending a fiber-coupled system, a variety of interesting applications arise for the commercial sector. With the four orientations of the NV centers, vector magnetometry for static or slowly changing magnetic fields can be realized using ODMR. If the crystal orientation is known, the parallel *B*0-field component can be determined by splitting the resonances and the angle of incidence can be calculated back. Homrighausen et al. [\[29\]](#page-18-1) have already demonstrated this in a fiber-based setup. The Hahn echo, in which the NV center becomes sensitive to alternating magnetic fields whose frequency corresponds to twice the pulse spacing *τ*, is suitable for measuring AC fields. This approach is investigated in more detail in [\[30\]](#page-18-2). The coherence time of the diamond used determines the measurable frequencies, which can be between the kHz and MHz range. Temperature measurement is also possible by using the *T*<sup>1</sup> time. Mrozek et al. [\[14\]](#page-17-9) show a comparison of the *T*<sup>1</sup> times of different diamond samples as functions of temperature, showing a change in 1/*T*<sup>1</sup> by several orders of magnitude in a range from 100 to 500 Kelvin. The great advantage of NV centers over other magnetic sensors is the high local resolution that can be achieved. The diamond used has a size of 150 µm. Single NV centers are already available in the lower nanometer range and show how far the local resolution can be further increased. Very sensitive detectors, such as avalanche photodiodes (APDs), which are operated with a high bias voltage of several 100 V, are required to measure individual NV centers. Since such a high-voltage source is missing in the hardware, it is not suitable for the measurement of individual NV centers. The operation of APDs in Geiger mode for the detection of single photons also presents further technical hurdles. Active quenching is necessary for a high count rate in order to reduce the dead time of the APD. In addition, a circuit with a sufficiently high bandwidth is required to be able to count the current pulses. However, the extension to measure individual NV centers is highly interesting for future development.

**Author Contributions:** Conceptualization, D.S.; methodology, D.S., L.H. and J.P.; validation, D.S., L.H. and M.G.; formal analysis, D.S.; investigation, D.S. and M.G.; resources, D.S.; data curation, D.S.; writing—original draft preparation, D.S.; writing—review and editing, L.H., J.P., F.H., M.G. and P.G.; visualization, D.S.; supervision, M.G. and P.G.; project administration, P.G.; funding acquisition, M.G. and P.G. All authors have read and agreed to the published version of the manuscript.

**Funding:** This research was funded by Bundesministerium für Bildung und Forschung (13N15971, 13N15489 and 13N16710).

**Institutional Review Board Statement:** Not applicable.

**Informed Consent Statement:** Not applicable.

**Data Availability Statement:** Data underlying the results presented in this paper are not publicly available at this time but may be obtained from the authors upon reasonable request.

**Acknowledgments:** The authors would like to thank the members of the projects OCQNV, RaQuEl, and QuantumMiniLabs for fruitful discussions as well as the Research Centre for Information and Communications Technologies of the University of Granada (CITIC-UGR) for the fruitful exchange.

**Conflicts of Interest:** The authors declare no conflicts of interest. The funders had no role in the design of the study; in the collection, analyses, or interpretation of data; in the writing of the manuscript; or in the decision to publish the results.

## PDF page 16

Sensors **2024**, 24, 3138 15 of 18

#### Abbreviations

The following abbreviations are used in this manuscript:

NV nitrogen vacancy ZFS zero-field splitting DAC digital-to-analog converter CF center frequency LIA lock-in amplifier **BCA** boxcar averager SPI serial peripheral interface **SRAM** static random-access memory DMA direct memory access GPIO general-purpose input/output **BSRR** bit set and reset register **ADC** analog-to-digital converter PLL phase-locked loop TIA transimpedance amplifier SNR signal-to-noise ratio **IFET** junction field effect transistor OpAmp operational amplifier MFB multiple feedback VCO voltage-controlled oscillator TTL transistor-transistor-logic **HPHT** high-temperature, high-pressure **PCB** printed circuit board CW continuous wave **SMA** Sub-Miniature Version A IC integrated circuit RF radio frequency amplifier **AMP** FFT fast Fourier transformation SLA stereolithography

#### Appendix A

Appendix A.1. Transimpedance Amplifier

**Table A1.** Used SMD parts and their values for building the TIA.

| Part           | Value                   | Package |
|----------------|-------------------------|---------|
| $C_f$          | 1.5 pF                  | 0603    |
| $C_{ac}$       | $0.1~\mathrm{\mu F}$    | 0603    |
| $R_1$          | $10~\mathrm{k}\Omega$   | 0603    |
| $R_2$          | $4.7~\mathrm{k}\Omega$  | 0603    |
| $R_3$          | $2  \mathrm{k}\Omega$   | 0603    |
| $R_4$          | $5\mathrm{k}\Omega$     | 0603    |
| $\mathrm{R}_f$ | $23.5 \mathrm{k}\Omega$ | 0603    |
| $\vec{Q_1}$    | CPH3910                 | CPH-3   |
| $Q_2$          | MMBTA06                 | SOT-23  |
| PD             | S5971                   | TO-18   |
| OpAmp          | ADA4627-1               | SOIC_N  |

## PDF page 17

## Appendix A.2. Lock-In Amplifier

Table A2. Used SMD parts and their values for building the LIA and the MFB filter.

| Part           | Value                  | Package |
|----------------|------------------------|---------|
| C <sub>1</sub> | 10 nF                  | 0603    |
| $C_2$          | 4.7 μF                 | 0603    |
| $C_3$          | 100 nF                 | 0603    |
| $R_1$          | $30  \mathrm{k}\Omega$ | 0603    |
| $R_2$          | $300~\mathrm{k}\Omega$ | 0603    |
| $R_3$          | $1.1~\mathrm{M}\Omega$ | 0603    |
| $R_4$          | $1.6\mathrm{M}\Omega$  | 0603    |
| $R_5$          | $160~\mathrm{k}\Omega$ | 0603    |
| OpAmp          | OPA4141AID             | SOIC-14 |
| Demodulator    | AD630ANZ               | SOIC-20 |

**Figure A1.** Bode plot of the MFB filter at the output of the AD630 demodulator IC. It shows the amplitude response in red and the phase shift in blue. The dashed lines are simulated values from an LTspice model while the dots correspond to the real measured values. The cut-off frequency is 1.16 Hz.

## Appendix A.3. Microwave Source

Figure A2. Schematic drawing of the microwave source.

**Table A3.** Used SMD parts and their values for building the microwave source.

| Part          | Value         | Package |
|---------------|---------------|---------|
| Crystal       | TG2520SMN     | TG2520  |
| PLL           | ADF4351BCP2   | CP-32-7 |
| I/Q modulator | LTC5589IUF    | QFN-24  |
| switch        | M3SWA2-63DRC+ | MCLP-12 |
| $G_1$         | GRF2012       | DFN-6   |
| $G_2$         | 2× GRF2012    | DFN-6   |

## PDF page 18

*Sensors* **2024**, *24*, 3138 17 of 18

## **References**

1. Stürner, F.M.; Brenneis, A.; Buck, T.; Kassel, J.; Rölver, R.; Fuchs, T.; Savitsky, A.; Suter, D.; Grimmel, J.; Hengesbach, S.; et al. Integrated and Portable Magnetometer Based on Nitrogen–Vacancy Ensembles in Diamond. *Adv. Quantum Technol.* **2021**, *4*, 2000111. [\[CrossRef\]](http://doi.org/10.1002/qute.202000111)

- 2. Pogorzelski, J.; Horsthemke, L.; Homrighausen, J.; Stiegekötter, D.; Gregor, M.; Glösekötter, P. Compact and Fully Integrated LED Quantum Sensor Based on NV Centers in Diamond. *Sensors* **2024**, *24*, 743. [\[CrossRef\]](http://dx.doi.org/10.3390/s24030743) [\[PubMed\]](http://www.ncbi.nlm.nih.gov/pubmed/38339463)
- 3. Huang, K.; Nie, Y.; Du, B.; Jiang, J.; Zhang, Z.; Wang, Q.; Xu, R. A compact two-dimensional quantum magnetometer module based on the fixed-frequency optical detection of magnetic resonance using nitrogen vacancy centers. *Appl. Phys. Lett.* **2021**, *119*, 114005. [\[CrossRef\]](http://dx.doi.org/10.1063/5.0061156)
- 4. Zheng, D.; Ma, Z.; Guo, W.; Niu, L.; Wang, J.; Chai, X.; Li, Y.; Sugawara, Y.; Yu, C.; Shi, Y.; et al. A hand-held magnetometer based on an ensemble of nitrogen-vacancy centers in diamond. *J. Phys. D Appl. Phys.* **2020**, *53*, 155004. [\[CrossRef\]](http://dx.doi.org/10.1088/1361-6463/ab6af2)
- 5. Mariani, G.; Umemoto, A.; Nomura, S. A home-made portable device based on Arduino Uno for pulsed magnetic resonance of NV centers in diamond. *AIP Adv.* **2022**, *12*, 065321. [\[CrossRef\]](http://dx.doi.org/10.1063/5.0089161)
- 6. Song, S.; Li, X.; Zhu, X.; Chen, B.; Yu, Z.; Xu, N.; Chen, B. An integrated and scalable experimental system for nitrogen-vacancy ensemble magnetometry. *Rev. Sci. Instruments* **2023**, *94*, 014703. [\[CrossRef\]](http://dx.doi.org/10.1063/5.0125441)
- 7. Ran, G.; Zhang, Z.; Huang, K.; Cheng, L.; Qu, S.; Huang, Q.; Mao, X. A Highly Integrated, High-Sensitivity Magnetometer Based on Diamond Nitrogen-Vacancy Centers. *IEEE Trans. Electron Devices* **2023**, *70*, 3223–3227. [\[CrossRef\]](http://dx.doi.org/10.1109/TED.2023.3265916)
- 8. Sewani, V.K.; Vallabhapurapu, H.H.; Yang, Y.; Firgau, H.R.; Adambukulam, C.; Johnson, B.C.; Pla, J.J.; Laucht, A. Coherent control of NV− centers in diamond in a quantum teaching lab. *Am. J. Phys.* **2020**, *88*, 1156–1169. [\[CrossRef\]](http://dx.doi.org/10.1119/10.0001905)
- 9. Schirhagl, R.; Chang, K.; Loretz, M.; Degen, C.L. Nitrogen-vacancy centers in diamond: Nanoscale sensors for physics and biology. *Annu. Rev. Phys. Chem.* **2014**, *65*, 83–105. [\[CrossRef\]](http://dx.doi.org/10.1146/annurev-physchem-040513-103659)
- 10. Grosz, A.; Haji-Sheikh, M.J.; Mukhopadhyay, S.C. (Eds.) *High Sensitivity Magnetometers*; Smart Sensors, Measurement and Instrumentation; Springer International Publishing: Cham, Switzerland, 2017. [\[CrossRef\]](http://dx.doi.org/10.1007/978-3-319-34070-8)
- 11. Jensen, K.; Kehayias, P.; Budker, D. Magnetometry with Nitrogen-Vacancy Centers in Diamond. In *High Sensitivity Magnetometers*; Grosz, A., Haji-Sheikh, M.J., Mukhopadhyay, S.C., Eds.; Smart Sensors, Measurement and Instrumentation; Springer: Cham, Switzerland, 2017; Volume 19, pp. 553–576. [\[CrossRef\]](http://dx.doi.org/10.1007/978-3-319-34070-8_18)
- 12. Horowitz, P.; Hill, W. *The Art of Electronics*, 3rd ed.; Cambridge University Press: Cambridge, NY, USA, 2015.
- 13. Rondin, L.; Tetienne, J.P.; Hingant, T.; Roch, J.F.; Maletinsky, P.; Jacques, V. Magnetometry with nitrogen-vacancy defects in diamond. *Rep. Prog. Phys. Phys. Soc.* **2014**, *77*, 056503. [\[CrossRef\]](http://dx.doi.org/10.1088/0034-4885/77/5/056503)
- 14. Mrozek, M.; Rudnicki, D.; Kehayias, P.; Jarmola, A.; Budker, D.; Gawlik, W. Longitudinal spin relaxation in nitrogen-vacancy ensembles in diamond. *arXiv* **2015**, arXiv:1505.02253. [\[CrossRef\]](https://doi.org/10.48550/arXiv.1505.02253)
- 15. Hahn, E.L. Spin Echoes. *Phys. Rev.* **1950**, *80*, 580–594. [\[CrossRef\]](http://dx.doi.org/10.1103/PhysRev.80.580)
- 16. de Lange, G.; Wang, Z.H.; Ristè, D.; Dobrovitski, V.V.; Hanson, R. Universal dynamical decoupling of a single solid-state spin from a spin bath. *Science* **2010**, *330*, 60–63. [\[CrossRef\]](http://dx.doi.org/10.1126/science.1192739) [\[PubMed\]](http://www.ncbi.nlm.nih.gov/pubmed/20829452)
- 17. Hayashi, K.; Matsuzaki, Y.; Ashida, T.; Onoda, S.; Abe, H.; Ohshima, T.; Hatano, M.; Taniguchi, T.; Morishita, H.; Fujiwara, M.; et al. Experimental and Theoretical Analysis of Noise Strength and Environmental Correlation Time for Ensembles of Nitrogen-Vacancy Centers in Diamond. *J. Phys. Soc. Jpn.* **2020**, *89*, 054708. [\[CrossRef\]](http://dx.doi.org/10.7566/JPSJ.89.054708)
- 18. Barry, J.F.; Schloss, J.M.; Bauch, E.; Turner, M.J.; Hart, C.A.; Pham, L.M.; Walsworth, R.L. Sensitivity optimization for NV-diamond magnetometry. *Rev. Mod. Phys.* **2020**, *92*, 015004. [\[CrossRef\]](http://dx.doi.org/10.1103/RevModPhys.92.015004)
- 19. Doherty, M.W.; Manson, N.B.; Delaney, P.; Jelezko, F.; Wrachtrup, J.; Hollenberg, L.C. The nitrogen-vacancy colour centre in diamond. *Phys. Rep.* **2013**, *528*, 1–45. [\[CrossRef\]](http://dx.doi.org/10.1016/j.physrep.2013.02.001)
- 20. Hobbs, P.C.D. *Building Electro-Optical Systems: Making It All Work*, 3rd ed.; Wiley Series in Pure and Applied Optics, John Wiley & Sons Inc: Hoboken, NJ, USA, 2022. [\[CrossRef\]](http://dx.doi.org/10.1002/9781119439080)
- 21. Ron Mancini. *Op Amps for Everyone*; Texas Instruments Incorporated: Dallas, TX, USA, 2002.
- 22. Press, W.H.; Teukolsky, S.A.; Vetterling, W.T.; Flannery, B.P. (Eds.) *Numerical Recipes in C: The Art of Scientific Computing*, 2nd ed.; Cambridge University Press: Cambridge, NY, USA, 2002.
- 23. Sasaki, K.; Monnai, Y.; Saijo, S.; Fujita, R.; Watanabe, H.; Ishi-Hayase, J.; Itoh, K.M.; Abe, E. Broadband, large-area microwave antenna for optically-detected magnetic resonance of nitrogen-vacancy centers in diamond. *arXiv* **2016**, arXiv:1605.04627. [\[CrossRef\]](https://doi.org/10.48550/arXiv.1605.04627)
- 24. Diggle, P.L.; D'Haenens-Johansson, U.F.S.; Green, B.L.; Welbourn, C.M.; Tran Thi, T.N.; Katrusha, A.; Wang, W.; Newton, M.E. Decoration of growth sector boundaries with nitrogen vacancy centers in as-grown single crystal high-pressure high-temperature synthetic diamond. *Phys. Rev. Mater.* **2020**, *4*, 093402. [\[CrossRef\]](http://dx.doi.org/10.1103/PhysRevMaterials.4.093402)
- 25. CMSIS DSP Software Library, Version Number 5.9.0. 2022. Available online: [https://www.keil.com/pack/doc/CMSIS/DSP/](https://www.keil.com/pack/doc/CMSIS/DSP/html/index.html) [html/index.html](https://www.keil.com/pack/doc/CMSIS/DSP/html/index.html) (accessed on 12 October 2023).
- 26. Qin, X.; Zhang, W.; Wang, L.; Zhao, Y.; Tong, Y.; Rong, X.; Du, J. An FPGA-Based Hardware Platform for the Control of Spin-Based Quantum Systems. *IEEE Trans. Instrum. Meas.* **2020**, *69*, 1127–1139. [\[CrossRef\]](http://dx.doi.org/10.1109/TIM.2019.2910921)
- 27. Zhang, Z.D.; Yin, S.Y.; Wang, L.C.; Wang, Y.D.; Li, Y.F.; Tian, Z.N.; Chen, Q.D. Single NV centers array preparation and static magnetic field detection. *Opt. Express* **2022**, *30*, 32355–32365. [\[CrossRef\]](http://dx.doi.org/10.1364/OE.470400)

## PDF page 19

*Sensors* **2024**, *24*, 3138 18 of 18

28. Bauch, E.; Singh, S.; Lee, J.; Hart, C.A.; Schloss, J.M.; Turner, M.J.; Barry, J.F.; Pham, L.M.; Bar-Gill, N.; Yelin, S.F.; et al. Decoherence of ensembles of nitrogen-vacancy centers in diamond. *Phys. Rev. B* **2020**, *102*, 134210. [\[CrossRef\]](http://dx.doi.org/10.1103/PhysRevB.102.134210)

- 29. Homrighausen, J.; Hoffmann, F.; Pogorzelski, J.; Glösekötter, P.; Gregor, M. Microscale Fiber-Integrated Vector Magnetometer with On-Tip Field Biasing using NV Ensembles in Diamond Microcystals. *arXiv* **2024**, arXiv:2404.14089
- 30. Taylor, J.M.; Cappellaro, P.; Childress, L.; Jiang, L.; Budker, D.; Hemmer, P.R.; Yacoby, A.; Walsworth, R.; Lukin, M.D. Highsensitivity diamond magnetometer with nanoscale resolution. *Nat. Phys.* **2008**, *4*, 810–816. [\[CrossRef\]](http://dx.doi.org/10.1038/nphys1075)

**Disclaimer/Publisher's Note:** The statements, opinions and data contained in all publications are solely those of the individual author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to people or property resulting from any ideas, methods, instructions or products referred to in the content.
