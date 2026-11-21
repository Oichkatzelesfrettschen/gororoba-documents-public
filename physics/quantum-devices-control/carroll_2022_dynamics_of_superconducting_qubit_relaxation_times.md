Source: https://doi.org/10.1038/s41534-022-00643-y
PDF sha256: 52cf6c0c5b20d4fc00f86759203bc24ee2da4531756235cbfa2b254098a58097
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of carroll_2022_dynamics_of_superconducting_qubit_relaxation_times.pdf

Transcription of `carroll_2022_dynamics_of_superconducting_qubit_relaxation_times.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

# ARTICLE OPEN

# Dynamics of superconducting qubit relaxation times

M. Carroll , S. Rosenblatt , P. Jurcevic , I. Lauer and A. Kandala .

Superconducting qubits are a leading candidate for quantum computing but display temporal fluctuations in their energy relaxation times  $T_1$ . This introduces instabilities in multi-qubit device performance. Furthermore, autocorrelation in these time fluctuations introduces challenges for obtaining representative measures of  $T_1$  for process optimization and device screening. These  $T_1$  fluctuations are often attributed to time varying coupling of the qubit to defects, putative two level systems (TLSs). In this work, we develop a technique to probe the spectral and temporal dynamics of  $T_1$  in single junction transmons by repeated  $T_1$  measurements in the frequency vicinity of the bare qubit transition, via the AC-Stark effect. Across 10 qubits, we observe strong correlations between the mean  $T_1$  averaged over approximately nine months and a snapshot of an equally weighted  $T_1$  average over the Stark shifted frequency range. These observations are suggestive of an ergodic-like spectral diffusion of TLSs dominating  $T_1$ , and offer a promising path to more rapid  $T_1$  characterization for device screening and process optimization.

npj Quantum Information (2022)8:132; https://doi.org/10.1038/s41534-022-00643-y

## **INTRODUCTION**

Superconducting qubits are a leading platform for quantum computing<sup>1,2</sup>. This has been driven, in part, by improvements in coherence times over five orders of magnitude since the realization of coherent dynamics in a Cooper-pair box<sup>3</sup>. However, further improving coherence times remains crucial for enhancing the scope of noisy superconducting quantum processors as well as the long-term challenge of building a fault tolerant quantum computer. Recent advances<sup>4–7</sup> in two-qubit gate control have placed their fidelities at the cusp of their coherence limit, implying that improvements in coherence could directly drive gate fidelities past the fault tolerant threshold. In this context, coherence stability and its impact on multi-qubit device performance is also an important theme, since superconducting qubits have been shown to display large and correlated temporal fluctuations (i.e.,  $1/f^{\alpha}$ ) in their energy relaxation times  $T_1^{8-14}$ . This places additional challenges for benchmarking the coherence properties of these devices<sup>13</sup>, and also for error mitigation strategies such as zero noise extrapolation<sup>12</sup>.

The fluctuations of qubit  $T_1$  are often attributed to resonant couplings with two-level systems (TLSs) that have been historically studied in the context of amorphous solids  $^{15,16}$  and their low temperature properties. More recently, TLSs have attracted renewed interest due to their effect on the coherence properties of superconducting quantum circuits  $^{11,13,14,17-20}$ , and are attributed to defects in amorphous materials at surfaces, interfaces, and the Josephson junction tunnel barrier. Frequency resolved measurements of  $T_1$  in flux and stress tunable devices  $^{11,19-21}$  have also displayed fluctuations, suggesting an environment of TLSs with varying coupling strengths around the qubit frequency. The variability of  $T_1$  over time is explained  $^{11,16}$ , at least in part, by temporal fluctuations in this frequency environment, associated with the spectral diffusion of the TLSs  $^{15,22}$ .

Furthermore, two-qubit gates that involve frequency excursions<sup>5,11,23</sup> can also interact with TLSs near the qubit frequency leading to additional incoherent error. The fluctuations in TLS peak positions, therefore, can also introduce fluctuations in two-qubit fidelity. Spectroscopy of defect TLS is, therefore,

central to understanding the short and long time  $T_1$  and gate fidelity of qubits.

Single Josephson junction transmons with fixed frequency couplings represent a successful device architecture achieving networks of over 60 qubits<sup>1</sup> with all microwave control and state of the art device coherence. The single junction configuration offers advantages such as reduced sensitivity to flux noise, while preserving the transmon charge insensitivity and also reducing system complexity with fewer control inputs. However, there is little TLS spectroscopy of single junction transmons because of the limited tunability, despite the central importance of understanding the TLS environment both for device and process characterization.

In this work, we introduce an all-microwave technique for the fast spectroscopy of TLSs in single junction transmon qubits that requires no additional hardware resources. In contrast to flux-based approaches to TLS spectroscopy, we employ off-resonant microwave tones to drive AC-Stark shifts of the fundamental qubit transition and spectrally resolve qubit relaxation times. Dips in relaxation times serve as a probe of the frequency location of a strongly coupled TLS. We use repeated frequency sweeps to probe the time dynamics of the relaxation probabilities including tracking the spectral diffusion of strongly coupled TLS. Across 10 qubits, we observe strong correlations between the long time mean, averaged over several months  $\langle T_1 \rangle_T$ , and the short time mean, averaged around the local qubit frequency  $\langle T_1 \rangle_{out}$ .

This strong correlation suggests a quasi-ergodic behavior of the TLS spectral diffusion in the nearby frequency neighborhood of the qubit. In contrast, there is lower correlation between  $\langle T_1 \rangle_T$  and  $T_1$  measured over a single day. The  $\langle T_1 \rangle_{\omega,t}$  can provide, therefore, a more rapid estimate of long-time behavior.

#### **RESULTS**

## Device and spectroscopy technique

The experiments reported in this letter were performed on ibmq\_almaden, a 20 qubit processor based off single junction transmons and fixed couplings. The device topology is

<sup>&</sup>lt;sup>1</sup>BM Quantum, IBM T.J. Watson Research Center, Yorktown Heights, NY 10598, USA. <sup>2</sup>These authors contributed equally: M. Carroll, S. Rosenblatt, A. Kandala.

<sup>&</sup>lt;sup>™</sup>email: malcolm.carroll@ibm.com; srosenb@us.ibm.com; akandala@us.ibm.com

## PDF page 2

Fig. 1 Device map and T1s. a Map of a 20 qubit device including the qubit number, two-qubit connectivity, and the qubit frequency in (GHz). b Box and whisker plot of T<sub>1</sub>'s measured daily.

shown in Fig. 1a, and qubit frequencies are around  $\sim$ 5 GHz. Figure 1b depicts the characteristic spread of the qubit  $T_1$ s and their mean, from  $\sim$ 250 measurements over 9 months. The base plate (to which the device was mounted) temperature of the dilution refrigerator was typically  $\sim$ 13 mK excepting several temperature excursions to  $\sim$ 1 K, which were not observed to have any significant effects on the long time  $T_1$  time series or distributions of  $T_1$  values discussed in this work, discussed later. Several qubits on the device display mean  $T_1$ s exceeding 100 µs. However, the large spread in individual qubit  $T_1$ s highlights the challenge for rapid benchmarking of device coherence, since any single  $T_1$  measurement can disagree substantially from its long-time mean.

We study the spectral dynamics of these  $T_1$  times by employing off-resonant microwave tones<sup>24</sup> to induce an effective frequency shift  $\Delta \omega_q$  in single junction transmons by the AC Stark effect. This has been employed previously for coherent state transfer between coupled qubits that are Stark shifted into resonance<sup>25</sup>. In this work, shifting the qubit frequency into resonance with a defect TLS induces a faster relaxation time, which in turn is used to detect the frequency location of the TLS<sup>26</sup>, as depicted in Fig. 2a. The Stark shift can be described analytically by a Duffing oscillator model<sup>27,28</sup>

$$\Delta\omega_{q} = \frac{\delta_{q}\Omega_{s}^{2}}{2\Delta_{qs}(\delta_{q} + \Delta_{qs})} \tag{1}$$

where  $\delta_q$  is the qubit anharmonicity,  $\Omega_s$  is the drive amplitude and  $\Delta_{qs} = \omega_q - \omega_s$  is the detuning between the qubit frequency and the Stark tone.

As seen from the expression above, the magnitude and sign of the Stark shift can be manipulated by the detuning and the drive amplitude of the Stark tone, Fig. 2c. Very large frequency shifts can be obtained by driving close to the transmon transitions, but this typically leads to undesired excitations/leakage out the two-state manifold. In this work, we obtain Stark shifts of 10's of MHz, with modest drive amplitudes and a fixed detuning  $\Delta_{qs}$  of  $\pm 50$  MHz. The frequency shifts are experimentally measured using a modified Ramsey sequence<sup>29</sup>, schematically shown in Fig. 2b, and display good agreement with the quadratic dependence of the perturbative model in the low-drive limit. A representative case is shown in Fig. 2d.

We focus on the spectrally resolved  $T_1$  measurements in Fig. 3 that we use as a probe of defect TLS transition frequencies. However, instead of measuring the entire  $T_1$  decay, we use the excited state probability,  $P_1$ , after a fixed delay time as a measure of  $T_1$ . This speeds up the spectral scans significantly. Our experiments are performed at a repetition rate of 1 kHz, but our scheme can be further accelerated with reset techniques<sup>30</sup>, which

can be crucial for probing faster TLS dynamics. For an effective frequency sweep, we run an amplitude sweep with off-resonant pulses at fixed detuning (±50 MHz) and duration (delay time of 50  $\mu$ s), after exciting the gubit with an initial  $\pi$  pulse. The pulsed Stark sequence enables faster spectroscopy by circumventing the need to re-calibrate the  $\pi$ ,  $\pi/2$  pulses at every frequency. The offresonant pulses have Gaussian-square envelopes with a  $2\sigma$  rise-fall profile, where  $\sigma = 10$  ns. This pulse sequence is shown in Fig. 2b. The amplitude points in the sweep are then related to Stark shifts by Ramsey sequences. Figure 3 shows representative data of such a sweep on qubit 19  $(Q_{19})$  with distinctive dips in  $P_1$  that we attribute to strongly coupled TLS at their transition frequencies.  $T_1$ measurements at Stark tone amplitudes corresponding to high/ low  $P_1$  points, as seen in the bottom panel of Fig. 3, explicitly show the substantial variation in  $T_1$  as a function of frequency and the consistent tracking of  $T_1$  with  $P_1$ .

Variations in  $P_1$  can potentially be caused by sources other than TLS. In our experiments,  $P_1$  is spectrally resolved to  $\sim \pm 25$  MHz around the individual qubit frequencies. The narrow frequency range combined with measuring non-neighbor sets of qubits simultaneously avoids strong  $P_1$  suppression from resonances with neighboring qubits, the coupling bus or common low-Q parasitic microwave modes. Control experiments show that time insensitive features in the  $P_1$  fingerprint are robust to choice of the Stark tone detuning, ruling out a power dependence for the power range used in this work. Finally, while a recent report<sup>31</sup> modeled their broadband  $T_1$  scatter as arising from quasi-particle fluctuations, this is not sufficient to explain the sharp frequency-dependent  $P_1$  features depicted, for instance in Fig. 3. Furthermore, recent experiments on our qubits suggest a quasi-particle limit to  $T_1$  that exceeds several milliseconds<sup>32</sup>.

# TLS dynamics and correlations of $P_1(\omega, t)$ and $\langle T_1 \rangle_T$

We repeat the line traces of Fig. 3 for both positive and negative 50 MHz detuning, approximately once every 3–4 h, extended over hundreds of hours for all the qubits. A representative example of the cumulative scans is shown in Fig. 4 for  $Q_{15}$ . Spectroscopy of the other qubits is shown in the supplemental information S1. The TLS dynamics around the qubit frequency are qualitatively similar to previous TLS spectroscopy using flux or stress tunable devices  $^{16}$ .

In the case of  $Q_{15}$ , Fig. 4, there are prominent dips in relaxation probability around positive 1 MHz, negative 5–10 MHz, and negative 15–20 MHz. The spectral diffusion of the positions of the  $T_1$  dips can vary between order of 1 to 10 MHz over the 272 h of measurement providing a qualitative measure of linewidths. A more quantitative discussion of linewidths can be found in supplemental information S2. The background is covered by an

## PDF page 3

**Fig. 2 Stark tone implementation. a** Schematic of qubit  $T_1$  response to shift in qubit frequency (red traces), at different times, t. The qubit frequency is tuned by an amount  $\Delta \omega_q$  by an off-resonant tone placed  $|\Delta_{qs}|$  above the qubit frequency  $\omega_q$ . The dependence of the frequency shift on the off-resonant tone amplitude  $\Omega_s$  is depicted by the blue trace. The  $T_1$  dips are indicative of the qubit coming into resonance with a strongly coupled TLS, at the frequency  $\omega_{TLS}$ . The TLS frequency shifts in time due to spectral diffusion, schematically indicated by changes in the  $T_1$  dips at different time snapshots. **b** Schematic of a Ramsey pulse sequence used to calibrate  $\Delta \omega_q$  as a function of  $\Omega_s$  (top); and (bottom) schematic pulse sequence for the relaxation time spectroscopy. For each  $\Omega_s$  (i.e.,  $\Delta \omega_q$ ), the  $|1\rangle$  occupation is measured at a fixed time (i.e.,  $\tau = 50 \,\mu s$  in this work). **c** An illustrative case of the 01 transition dependence on  $\omega_s$  for constant  $\Omega_s$ . The 01 qubit frequency,  $\omega_q + \Delta \omega_q$ , uses an unperturbed frequency of  $\omega_q = 5.0 \, \text{GHz}$  and an anharmonicity of  $\delta_q = -340 \, \text{MHz}$ . The locations of the unperturbed 01 and 12 transitions are shown as vertical lines overlaid with 5 MHz offsets to make their locations more visible on the figure. Negative and positive qubit shifts can be produced and large shifts can be induced depending on  $\Delta_{qs}$ . **d** Measured  $\Delta \omega_q$  as a function of normalized DAC amplitude,  $\Omega_s$  using the AC Stark shifted Ramsey technique. Solid line is a quadratic fit functionally consistent with a perturbative model.

Fig. 3 Representative example of relaxation time dependence on frequency. a Measured probability of being in the  $|1\rangle$  state,  $P_1$ , at 50  $\mu$ s wait time with varying  $\Delta \omega_q$  and tone detuned 50 MHz above  $\omega_q/2\pi$  for  $Q_{19}$ . **b** Example of Ramsey measurements used to extract frequency shifts  $\Delta \omega_q/2\pi$  from pulse amplitudes. The two curves result from starting the Ramsey oscillations with a  $X_{\pi/2}$  or  $Y_{\pi/2}$ . **c** and **d** are  $T_1$  measurement with Stark shifts  $\Delta \omega_q/2\pi = -18.9$  and -5.3 MHz, respectively. **e**  $T_1$  measurement with no Stark shift (i.e., no Stark tone).

ensemble of smaller dips of relaxation, Fig. 3, that also dynamically evolve, with features that are larger than the sampling noise in the measurement.

Fig. 4 Time dependence of energy relaxation spectroscopy. Time dependence of the energy relaxation spectroscopy for  $Q_{15}$  using  $\Delta \omega_s = \pm 50 \, \text{MHz}$  and varying  $\Omega_s$  over 501 different j amplitude points,  $\Omega_{s,j}$ , to sweep  $\Delta \omega_q(\Omega_{s,j})$  in a positive or negative direction (see Eqn. (1)). The  $P_1$  is measured at 50  $\mu$ s.

As discussed previously,  $T_1$  fluctuations introduce uncertainty in the coherence benchmarking, stability of multi-qubit circuit performance and process optimization of superconducting qubit devices. In this context of better estimator, we examine if the long-time averages ( $T \sim 9$  months)  $\langle T_1 \rangle_T$  and  $\langle P_1 \rangle_T$  are correlated

## PDF page 4

| Symbol                              | Definition                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| $\omega_q$                          | Qubit frequency                                                                                             |
| $\Omega_{s,j}$                      | jth Stark drive amplitude point                                                                             |
|                                     | in a frequency scan (see Eqn. (1))                                                                          |
| $\omega_j$                          | <i>j</i> th Qubit Stark shift,                                                                              |
|                                     | $\Delta\omega_q(\Omega_{s,j})$ (see Eqn. (1))                                                               |
| $d\omega_j$                         | Frequency bin size at the                                                                                   |
|                                     | Stark shifted frequency location                                                                            |
| $\Delta \omega$                     | Maximum qubit Stark shift                                                                                   |
| N                                   | Number of $T_1$ measurements                                                                                |
|                                     | for ~9 month time series in an average                                                                      |
| n                                   | Total number of spectroscopy                                                                                |
|                                     | time slices in a moving average                                                                             |
| T <sub>i</sub>                      | Time of ith time bin for the                                                                                |
|                                     | ~9 month $T_1$ time series                                                                                  |
| $t_i$                               | Time of ith time bin                                                                                        |
|                                     | of the spectroscopy time series                                                                             |
| $T_1(T_i)$                          | $T_1$ measured at <i>i</i> th time                                                                          |
| τ                                   | Decay time at                                                                                               |
|                                     | which $P_1$ was evaluated                                                                                   |
| $P_1(\omega_q+\omega_{j},\tau,t_i)$ | Probability of $ 1\rangle$ at $\tau$ delay for                                                              |
|                                     | time slice $t_i$ and frequency shift $\omega_j$                                                             |
| $\langle P_1 \rangle_T$             | Probability of $ 1\rangle$ at $\tau$                                                                        |
|                                     | averaged over ~9 month time series                                                                          |
| $\langle P_1 \rangle_{\omega,t}$    | Probability of $ 1\rangle$ at $\tau$ averaged over                                                          |
|                                     | frequency and spectroscopy time                                                                             |
| $\langle T_1 \rangle_{T_{0 \to N}}$ | Moving average of $T_i$                                                                                     |
|                                     | measurements from $T_0$ to $T_n$                                                                            |
| $\langle T_1 \rangle_T$             | $T_1$ averaged over entire ~9 months                                                                        |
| $\langle T_1 \rangle_{\omega,t}$    | $T_1$ average from $\langle P_1 \rangle_{\omega,t}$                                                         |
| $Q_k$                               | k'th qubit                                                                                                  |
| $R(t_i)$                            | $\langle T_1 \rangle_T$ correlation to $\langle T_1 \rangle_{\omega}$ at $t_i$ for $\{Q_k\}$                |
| $R(T_i)$                            | $\langle T_1 \rangle_T$ correlation to $T_1$ at a single time                                               |
|                                     | $T_i$ of the ~9 month series for $\{Q_k\}$                                                                  |
| $\langle R \rangle_{t_{0 \to n}}$   | $\langle T_1 \rangle_T$ correlation to $\langle T_1 \rangle_{\omega, \mathfrak{t}_{0 \to n}}$ for $\{Q_k\}$ |
| $\langle R \rangle_{T_{0 \to N}}$   | $\langle T_1 \rangle_T$ correlation to $\langle T_1 \rangle_{T_{0 \to N}}$ for $\{Q_k\}$                    |

with the frequency neighborhood of the qubit  $\langle T_1 \rangle_{\omega,t}$  and  $\langle P_1 \rangle_{\omega,t'}$  respectively. The averaged relaxation probabilities and  $T_1$ s are defined as

$$\langle P_1 \rangle_T = \frac{1}{N} \sum_{i=1}^N P_1(\omega_q, \tau, T_i)$$
 (2)

$$\langle T_1 \rangle_T = \frac{1}{N} \sum_{i=1}^N T_1(\omega_q, T_i)$$
(3)

$$\langle P_1 \rangle_{\omega,t} = \frac{1}{n} \sum_{i=1}^n \frac{1}{2\Delta\omega} \sum_{\omega_i = -\Delta\omega}^{\Delta\omega} P_1(\omega_q + \omega_j, \tau, t_i) d\omega_j, \tag{4}$$

$$\langle T_1 \rangle_{\omega,t} = \frac{1}{n} \sum_{i=1}^n \frac{1}{2\Delta\omega} \sum_{-\Delta\omega}^{\Delta\omega} \frac{-\tau}{\ln(P_1(\omega_q + \omega_j, \tau, t_i)d\omega_j)},\tag{5}$$

where definitions of variables can be found in Table 1.

We compare  $\langle P_1 \rangle_{\omega,t}$  to  $\langle P_1 \rangle_T$  from the daily  $T_1$  measurements over  $T_{\rm max} \sim 9$  months evaluated at  $\tau = 53\,\mu \rm s$ , shown in Fig. 1.

The  $\langle P_1 \rangle_{\omega,t}$  are calculated for a  $T_1$  delay time of  $\tau=50\,\mu s$  for 10 qubits in the device for the first time slice and a cutoff frequency  $\Delta \omega/2\pi=5$  MHz. A qualitatively close agreement for all 10 qubits is observed, see Fig. 5a.

A  $\langle T_1 \rangle_{\omega,t}$  can also be estimated for each  $\langle P_1 \rangle_{\omega,t}$  at  $\tau = 50~\mu s$  by assuming an exponential decay. The approximate equivalence of  $\langle T_1 \rangle_{\omega,t}$  and  $\langle T_1 \rangle_{\tau}$  is seen in the scatter plot of Fig. 5a inset. A near 1:1 relationship is observed when this approach is applied more broadly across many IBM devices, see supplemental information S3. Furthermore, the poorer correlation between  $\langle T_1 \rangle_{\tau}$  and a single instance of  $T_1$  measurements, is also shown by larger scatter, as seen in Fig. 5a inset.

To quantify with a single value the correlation between  $\langle T_1 \rangle_T$  or  $\langle P_1 \rangle_T$  and their estimators for many qubits, we use a Pearson R measure across the ten odd-labeled qubits,

$$R = \frac{\sum\limits_{k=0}^{d-1} (\langle X \rangle_{T,Q_i} - \overline{\langle X \rangle_T}) (\langle X \rangle_{\omega,t,Q_i} - \overline{\langle X \rangle}_{\omega,t})}{\sqrt{\sum\limits_{k=0}^{d-1} (\langle X \rangle_{T,Q_k} - \overline{\langle X \rangle_T})^2 \sum\limits_{k=0}^{d-1} (\langle X \rangle_{\omega,t,Q_i} - \overline{\langle X \rangle}_{\omega,t})^2}}$$
(6)

where d is the number of qubits in the device or analysis, 10 in this case, and X is the observable  $P_1$  or  $T_1$ . The Pearson correlation is a normalized covariance between two variables reflecting a linear correlation from 1 to -1, where R=1 (-1) represents a 100% positive (negative) correlation and R=0 indicates no correlation. Strong R correlation can therefore signal the existence of a potential linear mapping between the estimator and  $\langle T_1 \rangle_T$ , in particular, possibly one that is 1:1 or a scaling factor that will reliably estimate  $\langle T_1 \rangle_T$ .

For a single frequency sweep that takes ~20 min, we obtain  $0.76 < R(t_i) < 0.84$  correlation between  $\langle T_1 \rangle_T$  and  $\langle T_1 \rangle_{\omega,t}$  for 0.5 MHz  $< \Delta \omega < 5$  MHz. Using the  $P_1$  values without assuming an exponential dependence leads to stronger correlations of  $0.87 < R(t_i) < 0.91$ . Both of these are substantially stronger than the correlation found between the representative instance of  $T_1$  and  $\langle T_1 \rangle_T$ , which was R = 0.29. We note this instance of R can have a large spread, as seen by simulations of Gaussian-distributed fluctuations in supplemental information S4.

A better estimate of the  $\langle T_1 \rangle_T$  for each qubit,  $Q_{kr}$  in the device can be obtained from a moving average of multiple, N, measurements. We show the evolution of  $\langle R \rangle_{T_0 \dots N}$  using a moving average of the  $T_1(T_i)$  measurements,  $\langle T_1 \rangle_{T_0 \dots N}$ , for each qubit, Fig. 5b. The  $\langle R \rangle_{T_0 \dots N}$  exceeds  $R \sim 0.8$  (i.e., strong correlation) after  $\sim 10$  measurements, corresponding to a time exceeding 100 h. Approximately 10 independent measurements is sufficient for fluctuations with magnitude  $\sim 0.2 \langle T_1 \rangle_T$  to obtain a strong correlation,  $R \sim 0.8$ , between an estimator (e.g.,  $\langle T_1 \rangle_{T_0 \dots N}$ ) and  $\langle T_1 \rangle_T$ . The details of R dependence on fluctuation magnitude and number of measurements in the moving average are discussed more completely in supplemental information S4.

Autocorrelation between  $T_1(T_i)$  and  $T_1(T_{i-1})$  measurements is an underlying challenge to fast estimation of  $\langle T_1 \rangle_T$ . Evidence of autocorrelation can be seen for example in long-term drifts in the average and short-term correlations between  $T_1$ , inset of Fig. 5b. On shorter time scales, our experimental data shows evidence of stronger autocorrelation frustrating faster accurate estimation of  $\langle T_1 \rangle_T$  and that the fastest  $R \sim 0.8$  can be obtained on order of 1–2 days, see supplemental information S5 and S6. We conclude that  $\langle T_1 \rangle_{\omega,t}$  shows promise as a method for faster estimation of  $\langle T_1 \rangle_T$  than repeated  $T_1(\omega = \omega_q)$  measurements at only the qubit frequency. Extending the  $\langle T_1 \rangle_{\omega,t}$  estimator to a set of many qubits,  $\{Q_k\}$ , in a device result in larger R, in the same time, compared to relying only on  $T_1(\omega_q)$  measurements for each qubit. The R value simply being a quantitative single value expression of the high correlation between each  $\langle T_1 \rangle_{\omega,t}$  and  $\langle T_1 \rangle_T$  across the entire set of qubits.

## PDF page 5

**Fig. 5** Correlation between different T1 estimators. a Comparison of  $\langle P_1 \rangle_{\omega,t}$  at 50 μs and  $\langle P_1 \rangle_T$  averaged for ~9 months and evaluated at a  $\tau$  of 53 μs decay time.  $\langle P_1 \rangle_{\omega,t}$ , is averaged over  $\Delta \omega/2\pi = 5$  MHz after a single measurement that took ~ 20 min. (inset) A scatter plot using  $\langle T_1 \rangle_T$ 's averaged over 9 months of measurement as the dependent variable and  $\langle T_1 \rangle_{\omega,t}$  or  $T_1$ s from a single day. The line is a guide to the eye showing a 1:1 correlation. **b** The Pearson R dependence on time averaging of the  $T_1$ 's of the odd numbered qubits up to time,  $T_1$ , for three cases: (i) the entire time series (dash), (ii) the time series between temperature excursion B and D (dash-dot), lettered locations indicated in the inset, and (iii) the time series between C and D for which no temperature excursions were recorded (solid). The intermediate time series are shifted in time index to compare more directly at short times with the full-time series. The differences in R are within the standard deviation calculated for sampling  $T_1$  time series with a Gaussian-distributed range of values, see supplemental information S4. (inset) The  $T_1$  (black, left) and mixing chamber temperature (blue, right) time series for  $Q_{13}$ . Spacing of measurements is non-uniform. The minimum spacing is ~ 24 h apart. Each temperature excursion is labeled with a letter. **c** Pearson correlation, R, dependence on time slice averaging and frequency range,  $\Delta \omega$ , of the odd numbered qubits.

It is important to note that our calculations of  $\langle T_1 \rangle_{\omega,t}$  employ an equal weighting of  $P_1$  associated with every frequency bin and the same choice of  $\Delta\omega$  for every qubit. However, it is not a priori clear that equal weighting is a representative choice over the  $\Delta\omega$  range. For example, how evenly does the spectral diffusion of each TLS contribute to the  $T_1$  of the qubit? The strong correlation of  $\langle T_1 \rangle_{\omega,t}$  with  $\langle T_1 \rangle_T$  with equal weighting suggests that an ergodic-like sampling of the TLSs near the qubit frequency is a reasonable first approximation. The ergodic behavior of the  $T_1$  estimators is examined more completely in supplemental information S7 and supplemental information S8. Central to the question of assigning a  $T_1$  estimate to any qubit, we observe that  $\langle T_1 \rangle_T$  behaves ergodically for all the qubits despite short-term  $1/f^{\alpha}$  correlated behavior (i.e., a constant mean  $\langle T_1 \rangle_T$  can be identified). Assignment of any  $T_1$  estimate could alternatively be made impossible in the presence of drift, which is not observed in these qubits, see supplemental information S9 and supplemental information S7 for further details about weak stationarity and ergodicity. Furthermore, the strong correlation of  $\langle T_1 \rangle_T$  to  $\langle T_1 \rangle_{\omega,t}$  using only the  $P_1(\omega,\tau,t)$  spectrum around the qubit is consistent with a leading hypothesis that the  $\langle T_1 \rangle_T$  is dominated by TLS behavior rather than other stochastic or static contributions.

# Correlation dependence on frequency and measurement time

A natural question about the estimator  $\langle T_1 \rangle_{\omega,t}$  is, what are the optimal parameter choices for frequency range  $\Delta \omega$ , n autocorrelated samples and the spacing in time,  $\Delta t = t_i - t_{i-1}$ , to obtain sufficiently weakly autocorrelated measurements and a fast, accurate measure of  $\langle \mathcal{T}_1 \rangle_{\mathcal{T}}.$  Since the optimum choices are presently not known a priori, we evaluate and plot  $\langle R \rangle_{t_{0}=a}$  versus  $\Delta \omega$  and  $t_i$  in Fig. 5c to guide future application of this approach. Equal frequency bin weighting of  $P_1$  is used. While this order of magnitude choice of  $\Delta\omega$  produces a reasonably good first approximation for correlation across the entire range, the plot displays several unexplained features (e.g., non-monotonic dependence on  $\Delta\omega$ ) indicating the unsurprising insufficiency of these two globally applied parameters (i.e.,  $\Delta \omega$  and t) alone to weight the frequency contribution of all the qubits and approach  $R \sim 1$ . Additional sensitivity analysis in supplemental information S8 also examines correlation between frequencies and highlights that individual qubits have different sensitivity to the range sampled,  $\Delta \omega$ . We see that a wide span of  $\Delta \omega$  produces high  $\langle R \rangle_{t_0\dots r}$ , comparable or better than  $R(T_i)$  from a single  $T_1(\omega_q)$  measurement. We further show that not only is there a strong R correlation (e.g., linear dependence) but that  $\langle T_1 \rangle_{\omega,t}$  approaches 1:1 quantitative agreement with  $\langle T_1 \rangle_T$ . The degree to which a  $T_1$  estimator, from sampling the nearby frequency space, is quasiergodic and would converge to 1:1 agreement is addressed in much more detail in supplemental information S8 and supplemental information S3.

## **DISCUSSION**

# Implications for process characterization

The strong correlation between  $\langle T_1 \rangle_{\omega,t}$  and  $\langle T_1 \rangle_T$  suggests that long-time  $T_1$  averages might be estimated relatively rapidly using spectroscopy. This is in contrast to overcoming correlation times in  $T_1$  at a single  $\omega_q$  to obtain a representative  $\langle T_1 \rangle_T$  for the qubit.

Identification of better choices of  $\Delta\omega$  and n in this study were made with pre-knowledge of what  $\langle T_1 \rangle_T$  was. These parameters will have to be chosen without this pre-characterization for future implementation of this method. Encouragingly, the R dependence on both these parameters appears to be relatively weak suggesting that a heuristic choice for a single  $\Delta\omega$  and n might be sufficient to obtain useful estimates (i.e., R > 0.8) of  $\langle T_1 \rangle_T$  for new processes when using this simple equal weighting approach until improved choices can be formulated (i.e., different frequency spans for each qubit and or weighted averaging over frequency).

More specifically we observe that  $\mathcal{O}(10)$  independent measurements is sufficient to obtain an R ~ 0.8 or higher, see supplemental information S4. We conjecture that one can obtain 10 approximately independent samples, S, in a single scan by sampling at frequency spacings, Y, that are greater than the autocorrelation frequency width (i.e., a frequency spacing where correlation drops below ~ 0.2). In this work, we found the correlation to become weak for  $\mathcal{O}(1 \text{ MHz})$ , see supplemental information S8. Then by this heuristic, a single spectroscopy scan would require a  $\Delta \omega = \frac{(S-1)}{2} \chi$ , where S = 10 for the target of  $R \sim 0.8$ . We assume one of the measurements is done at the qubit frequency,  $T_1(\omega_a)$ , so for a  $\chi \sim 1 \text{ MHz}$ , a scan from  $\pm 4.5 \text{ MHz}$

## PDF page 6

would be suggested by such a heuristic. Extra n measurements can be obtained by waiting longer than the autocorrelation time. The autocorrelation width, furthermore, can be evaluated in the same scan as that used for the  $\langle T_1 \rangle_T$  estimate as long as a sufficiently wide range is sampled. Alternatively, a second scan can be taken if the initial  $\Delta \omega$  guess was too small.

Empirically we see diminishing gains in using ever larger  $\Delta\omega$ . Further research is needed to guide better limits on  $\Delta\omega$  beyond the operational observation that  $S\sim \mathcal{O}(10)$  produces a quasiergodic result for qubits with  $\langle T_1\rangle_T$  in the range of 10– $200~\mu s$ , see supplemental information S8 for more details on quasi-ergodicity. Since we do find ~1:1 agreement using a relatively small  $\Delta\omega\sim 10~\text{MHz}$  for the ~9 month time series and we observe that the distribution of  $T_1(\omega_q,T_i)$  produces a constant standard deviation, see supplemental information S9, rather than growing (e.g., proportional to a random walk  $\propto \sqrt{t}$ ), we speculate that optimal  $\Delta\omega$  is bounded rather than growing indefinitely from spectral diffusion processes. Notably, Klauder et al. calculate that dipole-coupled ensembles that are proposed for TLS spectral diffusion  $^{22}$ , will produce a truncated linewidth  $^{33}$ .

## Remarks on technique, correlations, and ergodicity

In this work, we probe the temporal and spectral dynamics of superconducting qubit relaxation times. We study these dynamics in high coherence, single-junction transmons by developing a technique for energy relaxation spectroscopy of defect TLSs via the AC Stark effect. Our technique requires no additional hardware resources and can be easily sped up further by integration with reset schemes. Autocorrelation of  $T_1$  frustrates rapid characterization of the long-time average  $\langle T_1 \rangle_T$  and therefore accurate characterization of devices. Our analysis of the dynamics identifies a strong correlation between  $\langle T_1 \rangle_T$  and its short time average over the local frequency span,  $\langle T_1 \rangle_{\omega,t}$ . The strong correlation of  $\langle T_1 \rangle_T$ with  $\langle T_1 \rangle_{\omega,t}$  is also consistent with a TLS dominated  $T_1$  that quasiergodically samples the qubit local frequency neighborhood in contrast to static or uncorrelated stochastic processes. This work opens up several new promising directions for rapid process characterization and evaluation of device stability.

#### **DATA AVAILABILITY**

The data that support the findings of this study are available from the corresponding author on reasonable request.

Received: 21 July 2021; Accepted: 17 October 2022; Published online: 17 November 2022

#### **REFERENCES**

- 1. Zhang, E. J. et al. High-performance superconducting quantum processors via laser annealing of transmon qubits. *Sci. Adv.* **8**, eabi6690 (2022).
- Arute, F. et al. Quantum supremacy using a programmable superconducting processor. Nature 574, 505–510 (2019).
- Nakamura, Y., Pashkin, Y. A. & Tsai, J. S. Coherent control of macroscopic quantum states in a single-cooper-pair box. Nature 398, 786–788 (1999).
- Hong, S. S. et al. Demonstration of a parametrically activated entangling gate protected from flux noise. *Phys. Rev. A* 101, 012302 (2020).
- Kandala, A. et al. Demonstration of a high-fidelity CNOT for fixed-frequency transmons with engineered zz suppression. Phys. Rev. Lett. 127, 130501 (2021).
- Hashim, A. et al. Randomized compiling for scalable quantum computing on a noisy superconducting quantum processor. *Phys. Rev. X* 11, 041039 (2021).
- Foxen, B. et al. Demonstrating a continuous set of two-qubit gates for near-term quantum algorithms. Phys. Rev. Lett. 125, 120504 (2020).
- Müller, C., Lisenfeld, J., Shnirman, A. & Poletto, S. Interacting two-level defects as sources of fluctuating high-frequency noise in superconducting circuits. *Phys. Rev. B* 92, 035442 (2015).
- 9. Paladino, E., Galperin, Y. M., Falci, G. & Altshuler, B. L.  $\frac{1}{\ell}$  noise: Implications for solid-state quantum information. *Rev. Mod. Phys.* **86**, 361–418 (2014).

- Weissman, M. B. <sup>1</sup>/<sub>f</sub> noise and other slow, nonexponential kinetics in condensed matter. Rev. Mod. Phys. 60, 537–571 (1988).
- Klimov, P. et al. Fluctuations of energy-relaxation times in superconducting qubits. Phys. Rev. Lett. 121, 090502 (2018).
- Kandala, A. et al. Error mitigation extends the computational reach of a noisy quantum processor. Nature 567, 491–495 (2019).
- Burnett, J. J. et al. Decoherence benchmarking of superconducting qubits. npj Quantum Inf. 5, 1–8 (2019).
- Schlör, S. et al. Correlating decoherence in transmon qubits: low frequency noise by single fluctuators. Phys. Rev. Lett. 123, 190502 (2019).
- Phillips, W. Tunneling states in amorphous solids. J. Low. Temp. Phys. 7, 351–360 (1972).
- Müller, C., Cole, J. H. & Lisenfeld, J. Towards understanding two-level-systems in amorphous solids—insights from quantum circuits. Rep. Prog. Phys. 82, 124501 (2019).
- Martinis, J. M. et al. Decoherence in Josephson qubits from dielectric loss. Phys. Rev. Lett. 95, 210503 (2005).
- Grabovskij, G. J., Peichl, T., Lisenfeld, J., Weiss, G. & Ustinov, A. V. Strain tuning of individual atomic tunneling systems detected by a superconducting qubit. Science 338, 232–234 (2012).
- Barends, R. et al. Coherent Josephson qubit suitable for scalable quantum integrated circuits. Phys. Rev. Lett. 111, 080502 (2013).
- Lisenfeld, J. et al. Electric field spectroscopy of material defects in transmon qubits. npj Quantum Inf. 5, 1–6 (2019).
- 21. Abdurakhimov, L. V. et al. Driven-state relaxation of a coupled qubit-defect system in spin-locking measurements. *Phys. Rev. B* **102**, 100502 (2020).
- Black, J. L. & Halperin, B. I. Spectral diffusion, phonon echoes, and saturation recovery in glasses at low temperatures. *Phys. Rev. B* 16, 2879–2895 (1977).
- Stehlik, J. et al. Tunable coupling architecture for fixed-frequency transmons. Phys. Rev. Lett. 127, 080505 (2021).
- Gambetta, J. et al. Qubit-photon interactions in a cavity: measurement-induced dephasing and number splitting. Phys. Rev. A 74, 042318 (2006).
- Majer, J. et al. Coupling superconducting qubits via a cavity bus. Nature 449, 443–447 (2007).
- Simmonds, R. W., Lang, K. M., Hite, D. A., Pappas, D. P. & Martinis, J. M. Decoherence in Josephson qubits from junction resonances. *Phys. Rev. Lett.* 93, 077003 (2004).
- Magesan, E. & Gambetta, J. M. Effective hamiltonian models of the crossresonance gate. Phys. Rev. A 101, 052308 (2020).
- Schneider, A. et al. Local sensing with the multilevel ac stark effect. Phys. Rev. A 97, 062334 (2018).
- Ramsey, N. F. A molecular beam resonance method with separated oscillating fields. *Phys. Rev.* 78, 695–699 (1950).
- Egger, D. J. et al. Pulsed reset protocol for fixed-frequency superconducting qubits. Phys. Rev. Appl. 10, 044030 (2018).
- 31. Yan, F. et al. The flux qubit revisited to enhance coherence and reproducibility. *Nat. Commun.* **7**, 1–9 (2016).
- 32. Kurter, C. et al. Quasiparticle tunneling as a probe of Josephson junction barrier and capacitor material in superconducting qubits. npj Quantum Inf. 8, 31 (2022).
- Klauder, J. R. & Anderson, P. W. Spectral diffusion decay in spin resonance experiments. *Phys. Rev.* 125, 912–932 (1962).

## **ACKNOWLEDGEMENTS**

We acknowledge technical support on the ibmq\_almaden device from the IBM Quantum deployment team. Additional insightful discussions, suggestions and assistance came from Nick Bronn, Andrew Cross, Oliver Dial, Doug McClure, Easwar Magesan, Hasan Nayfeh, James Raferty, Martin Sandberg, Srikanth Srinivasan, Neereja Sundaresan, Jerry Tersoff, Ben Fearon, Karthik Balakrishnan, James Hannon, and Jerry Chow. M.C. also acknowledges support from Princeton Plasma Physics Laboratory through the Department of Energy Laboratory Directed Research and Development program and contract number DE-AC02-09CH11466 to complete parts of the analysis and manuscript.

#### **AUTHOR CONTRIBUTIONS**

S.R. and A.K. developed the technique with contributions from M.C., I.L., and P.J. M.C. and S.R. performed the experiments. M.C., S.R., and A.K. analyzed the data. M.C., S.R., and A.K. wrote the manuscript with feedback from the other authors.

## **COMPETING INTERESTS**

The authors declare that elements of this work will be included in patents filed by the International Business Machines Corporation with the US Patent and Trademark office. The authors declare no other financial or non/financial competing interests in relation to this published work.

## PDF page 7

## ADDITIONAL INFORMATION

Supplementary information The online version contains supplementary material available at [https://doi.org/10.1038/s41534-022-00643-y.](https://doi.org/10.1038/s41534-022-00643-y)

Correspondence and requests for materials should be addressed to M. Carroll, S. Rosenblatt or A. Kandala.

Reprints and permission information is available at [http://www.nature.com/](http://www.nature.com/reprints) [reprints](http://www.nature.com/reprints)

Publisher's note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional affiliations.

Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons license, and indicate if changes were made. The images or other third party material in this article are included in the article's Creative Commons license, unless indicated otherwise in a credit line to the material. If material is not included in the article's Creative Commons license and your intended use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly

from the copyright holder. To view a copy of this license, visit [http://](http://creativecommons.org/licenses/by/4.0/)

© The Author(s) 2022

[creativecommons.org/licenses/by/4.0/.](http://creativecommons.org/licenses/by/4.0/)
