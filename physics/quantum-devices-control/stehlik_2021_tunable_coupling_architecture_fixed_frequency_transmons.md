Source: https://doi.org/10.1103/PhysRevLett.127.080505
PDF sha256: ff4b90ccf7f86a0bd86726c066340c3a7e5c99262f9fe4b9ce5c0c9421fa7e36
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of stehlik_2021_tunable_coupling_architecture_fixed_frequency_transmons.pdf

Transcription of `stehlik_2021_tunable_coupling_architecture_fixed_frequency_transmons.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

## **Tunable Coupling Architecture for Fixed-Frequency Transmon Superconducting Qubits**

J. Stehlik, <sup>1,\*</sup> D. M. Zajac, <sup>1,\*</sup> D. L. Underwood, <sup>1</sup> T. Phung, <sup>2</sup> J. Blair, <sup>1</sup> S. Carnevale, <sup>1</sup> D. Klaus, <sup>1</sup> G. A. Keefe, <sup>1</sup> A. Carniol, <sup>1</sup> M. Kumph, <sup>1</sup> Matthias Steffen, <sup>1</sup> and O. E. Dial, <sup>1</sup> IBM Quantum, IBM T. J. Watson Research Center, Yorktown Heights, New York 10598, USA, <sup>2</sup> IBM Quantum, IBM Almaden Research Center, San Jose, California 95120, USA

(Received 24 January 2021; accepted 19 July 2021; published 20 August 2021)

Implementation of high-fidelity 2-qubit operations is a key ingredient for scalable quantum error correction. In superconducting qubit architectures, tunable buses have been explored as a means to higher-fidelity gates. However, these buses introduce new pathways for leakage. Here we present a modified tunable bus architecture appropriate for fixed-frequency qubits in which the adiabaticity restrictions on gate speed are reduced. We characterize this coupler on a range of 2-qubit devices, achieving a maximum gate fidelity of 99.85%. We further show the calibration is stable over one day.

DOI: 10.1103/PhysRevLett.127.080505

Achieving high-fidelity 2-qubit (2Q) gates is one of the largest obstacles toward fault-tolerant quantum computation. Many approaches have been developed based on either fixed-frequency or tunable transmons. Tunable transmons naturally allow for fast iSWAP gates between the  $|10\rangle$ and  $|01\rangle$  states or controlled-Z (CZ) gates by utilizing the interaction between the  $|11\rangle$  and  $|20\rangle$  (or  $|02\rangle$ ) states [1,2]. However, qubit coherence and stability generally suffer from the presence of flux noise. Alternatively, fixedfrequency qubits offer long coherence times and stability, and a variety of microwave-activated entangling gates can be utilized for 2-qubit operations [3–7]. The drawback to these schemes is that qubit frequencies cannot be tuned away from collisions, and gate times tend to be long [8]. Additionally, regardless of whether using fixed-frequency or tunable transmons, the presence of always-on coupling leads to gate errors caused by spectator qubits [9–11].

Recently many groups have turned to tunable buses as a way to both achieve faster 2Q gates and to address issues raised by the presence of always-on coupling [12–18]. Here we explore the tunable bus architecture in a novel regime: with the frequency of the bus below the frequency of the qubits. Here the high-ZZ region is near the bus sweet spot, and there is a smooth transition between the on and off locations. We show that this allows us to achieve high-fidelity gates between fixed-frequency transmons. Our study covers eleven 2Q devices with varying detunings and bus-qubit coupling strengths. The highest-fidelity gate we achieve is 46 ns long with an error per gate (EPG) of

Published by the American Physical Society under the terms of the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the author(s) and the published article's title, journal citation, and DOI.  $0.0015 \pm 0.0001$ , and despite the flux-sensitive nature of the coupler, we find that its optimal calibration is stable for more than one day.

The tunable coupler recently proposed by F. Yan *et al.* [12] provides an elegant method for achieving a high on-off ratio. In their design, schematically captured in Fig. 1(a), a direct capacitor is added in parallel to the tunable bus and engineered to cancel the coupling between the two qubits exactly at a particular frequency for the tunable bus. We can model this system using the following Hamiltonian:

$$H_{\text{tot}} = \sum H_i + H_c, \tag{1}$$

$$H_{i} = \hbar \omega_{i} a_{i}^{\dagger} a_{i} + \frac{\delta_{i}}{2} a_{i}^{\dagger} a_{i}^{\dagger} a_{i} a_{i}, \qquad (2)$$

where  $\omega_i$  is the frequency of the *i*th transmon with  $i \in \{Q1, Q2, bus\}$ ,  $\delta_i$  is the anharmonicity, and  $a_i^{\dagger}$   $(a_i)$  are the raising (lowering) operators. The coupling Hamiltonian is given by

$$H_{\rm c} = \sum_{i \neq j} g_{i,j} (a_i^{\dagger} + a_i) (a_j^{\dagger} + a_j).$$
 (3)

With the bus far-detuned from qubits, we can approximate the effective coupling due to the tunable bus as  $J_{\rm bus} \approx [(g_{Q1,\rm bus}g_{Q2,\rm bus})/\Delta]$ , where  $1/\Delta = [1/(\omega_{Q1}-\omega_{\rm bus})+1/(\omega_{Q2}-\omega_{\rm bus})]$ . The direct capacitor between Q1 and Q2 adds a positive coupling term  $g_{Q1,Q2}$ ; thus, the total effective coupling then becomes  $J_{\rm tot} \approx J_{\rm bus} + g_{Q1,Q2}$  [12]. When  $\omega_{\rm bus} > \omega_{Q1,Q2}$ , the farther the tunable bus is detuned from the qubits, the closer to zero the (negative) effective  $J_{\rm bus}$  is. Therefore, for any positive small  $g_{Q1,Q2}$ , it is always possible to find a zero in  $J_{\rm tot}$  by adjusting  $\omega_{\rm bus}$ . A CZ gate

## PDF page 2

FIG. 1. (a) Schematic representation of previously proposed bus above qubits tunable coupler. (b) ZZ as a function of qubit-qubit detuning and bus frequency for BAQ device. (c) Schematic representation of a bus below qubits tunable coupler. Changing the bypass capacitor to go between opposite islands of the transmons compared to the tunable coupler. (d) ZZ as a function of qubit-qubit detuning and bus frequency for BBQ device. Because of the change in the bypass capacitor, the zero in ZZ now occurs with the bus detuned below the qubits. (e) ZZ as a function of bus-qubit detuning for both BAQ and BBQ. For the same magnitude of coupling, BBQ gives larger "on" coupling and a less complex response curve.

can then be realized by decreasing  $\omega_{\rm bus}$  frequency from the "off" position ( $J_{\rm tot} \sim 0$ ) to an on ( $|J_{\rm tot}| > 0$ ) position. Since in this device the tunable bus is detuned above the frequencies of the qubits, for the purposes of the following discussion we will call this the bus above qubits (BAQ) architecture.

We can more quantitatively analyze the system by setting  $\delta_{Q1}/2\pi=\delta_{Q2}/2\pi=-240$  MHz for the qubits and  $\delta_{\rm bus}/2\pi=-140$  MHz for the bus and using coupling  $g_{Q1,\rm bus}/2\pi=g_{Q2,\rm bus}/2\pi=110$  and  $g_{Q1,Q2}/2\pi=6$  MHz. With these parameters, we diagonalize the system and extract ZZ as

$$ZZ = (E_{11:0} - E_{01:0} - E_{10:0} + E_{00:0})/h.$$
 (4)

Here  $E_{nm;l}$  is the energy of the level with n excitations in qubit 1, m excitations in qubit 2, and l excitation in the bus. We plot ZZ as a function of  $\omega_2$  and  $\omega_{\text{bus}}$  in Fig. 1(b) with fixed  $\omega_1/(2\pi) = 5$  GHz.

The plot features four level crossings that result in large ZZ. We can identify these as the bus being resonant with one of the qubits (either  $\omega_{Q1} = \omega_{\text{bus}}$  or  $\omega_{Q2} = \omega_{\text{bus}}$ ) and with the qubits being detuned by exactly the anharmonicity ( $|\omega_{Q1} - \omega_{Q2}| = |\delta|$ ). Beyond these regions of high ZZ, the plot shows a zero in ZZ [highlighted using a red dashed line in Fig 1(b) near 7 GHz]. This is surrounded by a broad range of small ZZ, which forms the idle point of the bus. To form a CZ gate, the bus will be detuned closer to the qubits.

The BAQ design, however, suffers from several drawbacks that make it challenging for adiabatic gates between fixed-frequency transmons, where the detuning between the qubits is not adjustable. First, during gate operation the bus must be detuned below its maximum frequency. As result, the on state cannot be near the upper sweet spot of the superconducting quantum interference device (SQUID) that forms the tunable bus. While using an asymmetric SQUID can help, the lower sweet spot is narrower [19]. This has the effect of increasing sensitivity to noise and also requires more precise control of the SQUID critical currents and overall device parameters.

More importantly, if the two qubits are in the straddling regime (i.e., detuned by less than the anharmonicity), there is a significant dip in ZZ that appears with the bus detuned from qubits by  $\approx 100$  MHz [see Fig. 1(e) for 1D cut]. We identify this dip with the collision between  $E_{11:0}$  and  $E_{00:2}$ energy levels, that is, between the  $|2\rangle$  state of the coupler and the  $|11\rangle$  state of the two qubits. This is a two-photon transition that is allowed in the Hamiltonian and leads directly to a reduction in ZZ compared to what would be seen with a idealized two-level coupler. Furthermore, due to the two-photon nature of this transition, the associated anticrossing is, in general, smaller than the qubit-bus coupling  $g_{O,\text{bus}}$ . The presence of this anticrossing will complicate the dynamics during gate operation, since accessing high-ZZ regions requires passing through the anticrossing, leading to leakage into the  $|2\rangle$  state of the bus [20]. These dynamics can be avoided by either going to larger detuning  $|\omega_{O1} - \omega_{O2}| > |\delta_O|$  [15,20] or if the qubits can be dynamically detuned to  $\approx 1\delta$  [14].

For these reasons, it is desirable for the off position of the coupler to be such that  $\omega_{\rm bus} < \omega_{\rm qubits}$ —an alternative bus below qubits (BBQ) architecture. This can be achieved by flipping the sign of any of the  $g_{i,j}$ . In our implementation, we change the sign of  $g_{Q1,Q2}$  by using floating transmons and coupling the islands of the same voltage polarity to the tunable bus, while coupling islands of opposite voltage

## PDF page 3

polarity using the bypass capacitor, as schematically captured in Fig. 1(c).

If we set  $g_{Q1,Q2}/2\pi = -6$  MHz and keep all other parameters the same as our BAQ simulation, the resulting plot of ZZ as a function of detuning and bus frequency is depicted in Fig. 1(d). We again have a region of low ZZ, which in this case occurs with the bus near 3 GHz. The decrease associated with the  $|2\rangle$  state of the bus is still present, but in this case does not interfere with turning on the gate because it is above the lower qubit frequency and above the intended operating point of the bus.

To more quantitatively compare BAQ and BBQ devices, we fix the detuning between the qubits at 90 MHz and plot ZZ as a function of the detuning between the bus and the qubit closer in frequency to the bus. This is plotted in Fig. 1(e). We see that, for the same absolute magnitude of coupling and bus detuning, we can achieve more ZZ contrast in the BBQ architecture. In BBQ we can also turn on gates ZZ exceeding 10 MHz without going through any avoided crossings (for example, 11;0 and 00;2—which manifests as a dip in ZZ for the BAO device). As a result, adiabaticity constraints are loosened in the BBO architecture; this allows for adiabatic CZ gates, which are faster and suffer from less leakage. This makes BBQ architecture advantageous for gates between fixed-frequency transmons. Finally, for the proposed values, the bus off position will occur between 3 and 4 GHz. We find these frequencies sufficiently large to avoid thermal heating.

To study and validate the BBQ architecture experimentally, we fabricated several 2Q devices with varying coupling parameters. We use a niobium on silicon process with aluminum junctions, similar to Ref. [21]. We also use a bump bonded test vehicle to ensure compatibility with multiqubit devices. To enable high-fidelity gate operations, we use an asymmetric SQUID to deliberately limit the tunability of the coupler qubit to approximately the range needed to both achieve the minimum ZZ and reach ~50 MHz ZZ. In Fig. 2(a) we plot measured ZZ as a function of the bias applied to the SQUID loop for a typical device with qubit-qubit detuning of 351 MHz. In regions of high ZZ, where it is impossible to calibrate single-qubit gates, we instead rely on a pulsed measurement (see Supplemental Material [22]). We fit the observed ZZ vs flux curve and obtain approximately  $g_{O1,\text{bus}}/2\pi \approx$  $g_{Q2,\text{bus}}/2\pi \approx 120 \text{ MHz}$ , and  $g_{Q1,Q2}/2\pi \approx$ -4 MHz. We note that all three are approximately 10% larger than our designed values.

To implement a 2Q gate, we pulse the flux from the off position to a region of high ZZ as shown schematically in the inset of Fig. 2(a). In order to remain adiabatic, we use a pulse shape similar to the one described in Ref. [25] (see Supplemental Material [22]). We calibrate our pulses by putting one qubit (Q1) on the equator and preparing the other qubit (Q2) in either the  $|1\rangle$  or the  $|0\rangle$  state. We then apply pulses of varying amplitude. Because of the ZZ

FIG. 2. (a) ZZ as a function of applied bias measured on qubit pair 1. To create a 2-qubit gate, we apply static bias to minimize ZZ and then apply pulse to a region of high ZZ. Superimposed with the time axis vertically is a schematic rendition of the applied flux pulse. (b) 2-qubit randomized benchmarking: probability of measuring qubits in the  $|00\rangle$  state as a function of number of Cliffords. We measure an EPG of 0.0015. Inset shows Z rotation as a function of pulse amplitude for two states of the control qubit.

interaction, depending on the state of Q2, Q1 will accumulate a different phase, as shown in the inset of Fig. 2(b). We choose an amplitude that results in a difference of  $\pi$  between the  $|0\rangle$  and  $|1\rangle$  rotations and apply a software Z rotation [26] to both qubits to achieve the following gate unitary:

$$U_{\rm CZ} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1 \end{pmatrix}. \tag{5}$$

We perform interleaved randomized benchmarking on this gate and obtain an EPG of  $0.0015 \pm 0.0001$  [27]. Crucially, we can achieve this error without sacrificing single-qubit gate fidelity, and as a result the noninterleaved benchmarking decay is visible to 800 Cliffords. By dividing the observed error per Clifford (EPC) by the average number of 2Q gates in our Clifford decomposition [22], we find the EPG is bounded from above by

## PDF page 4

FIG. 3. (a) EPG by interleaved benchmarking as a function of gate length for three 2Q devices. (b) Histogram of EPG and EPC/1.5 measured over a period of 20 h. (c) EPG vs time since last calibration on the gate from (b), demonstrating good stability for at least 24 h, despite the use of flux-tunable elements.

 $0.0019 \pm 0.0001$ , which is the gate error we would deduce, assuming our single-qubit gates are perfect.

To ensure reproducibility of these results, we study this gate scheme across different devices. In Fig. 3(a), we plot gate fidelity as extracted from interleaved randomized benchmarking for three different 2Q pairs, as a function of gate length. All three pairs exhibit similar behavior. With longer gate times we see an increase in error due to qubit decoherence, which, once we include the decoherence of the coupler, accounts for 85% of the error [22]. At very short timescales (near 50 ns), we see an increase in error, which we attribute to the evolution during the gate no longer being adiabatic.

One crucial aspect in any gate scheme is stability. This is especially poignant in a flux-based architecture, with 1/f

flux noise ultimately limiting the repeatability [28]. In our BBQ architecture, however, the gate on position can be near the upper sweet spot of the SQUID tuning range. We can use this to realize excellent stability in time. To demonstrate this, we repeatedly measure gate fidelity over a 19-h period without recalibration. In Fig. 3(b), we plot the histogram of the fidelities extracted by interleaved randomized benchmarking, as well as the upper bound on error (established by dividing the EPC by the number of 2Q gates in our decomposition). Both distributions show excursions in fidelity that are, at worst, 60% worse. In Fig. 3(c), we plot the same data as a function of time since calibration. Over the entire measurement period, we observe no significant deviations from the quoted fidelity; furthermore, we do not observe any clear drift toward degraded performance.

We also extend the study to cover different detunings and coupling strengths. A summary of the 11 devices characterized is found in Table I. In general, higher coupling strength results in faster and higher-fidelity gates. While only one pair with a design of  $g_{Q,\rm bus}/2\pi=80$  MHz achieved error less than 0.002, such error was achieved on three of the five pairs with a design of  $g_{Q,\rm bus}/2\pi=110$  MHz.

One noteworthy entry in Table I is pair 8. This pair had a detuning of just 9 MHz. Such low detuning poses a significant problem for our chosen adiabatic CZ gate. This is due to the fact that moving the bus toward the qubits generates an effective exchange interaction between the qubits. The turn on of this exchange interaction needs to be done adiabatically with respect to the detuning between the qubits, otherwise a partial swap will be generated between the qubits. Such swaps have been used to generate arbitrary iSWAP and CZ angles in architectures with tunable qubits [14].

For qubit pair 8, we cancel the swap operation without detuning the qubits by employing a technique similar to the sudden net zero scheme in Ref. [18]. We use the fact that a single pulse can be thought of as a beam splitter—splitting



| TABLE I. | Summary c | of errors and | coherences | over 11 | qubit pair | s studied. |
|----------|-----------|---------------|------------|---------|------------|------------|
|----------|-----------|---------------|------------|---------|------------|------------|

| Qubit pair | Coupling (MHz) | Detuning (MHz) | Average $T_1$ ( $\mu$ s) | Average $T_2$ ( $\mu$ s) | Gate time (ns) | Error<br>per gate   | Error<br>per clifford |
|------------|----------------|----------------|--------------------------|--------------------------|----------------|---------------------|-----------------------|
| 1          | 110            | 351            | 76                       | 105                      | 46             | $0.0015 \pm 0.0001$ | $0.0029 \pm 0.0001$   |
| 2          | 110            | 398            | 82                       | 151                      | 70             | $0.0019 \pm 0.0002$ | $0.0039 \pm 0.0003$   |
| 3          | 110            | 324            | 68                       | 134                      | 54             | $0.0018 \pm 0.0001$ | $0.0037 \pm 0.0002$   |
| 4          | 110            | 503            | 77                       | 104                      | 130            | $0.0056 \pm 0.0003$ | $0.0094 \pm 0.0004$   |
| 5          | 110            | 562            | 86                       | 113                      | 81             | $0.0025 \pm 0.0002$ | $0.0048 \pm 0.0002$   |
| 6          | 80             | 136            | 100                      | 124                      | 63             | $0.0020 \pm 0.0004$ | $0.0044 \pm 0.0002$   |
| 7          | 80             | 145            | 70                       | 77                       | 86             | $0.0035 \pm 0.0004$ | $0.0055 \pm 0.0003$   |
| 8          | 80             | 9              | 80                       | 107                      | 136            | $0.006 \pm 0.002$   | $0.011 \pm 0.001$     |
| 9          | 80             | 166            | 46                       | 106                      | 113            | $0.0046 \pm 0.0007$ | $0.0088 \pm 0.0004$   |
| 10         | 80             | 89             | 63                       | 80                       | 56             | $0.005 \pm 0.002$   | $0.007 \pm 0.001$     |
| 11         | 80             | 160            | 24                       | 35                       | 130            | $0.0049 \pm 0.0006$ | $0.0085 \pm 0.0003$   |

## PDF page 5

FIG. 4. (a) Probability of measuring the first qubit in the excited state as function of the wait time between pulses for input states of  $|00\rangle$ ,  $|01\rangle$ ,  $|10\rangle$ , and  $|11\rangle$ . Depending on the delay, an ISWAP or a CZ gate can be generated. (b) Probability of finding the qubits in a  $|00\rangle$  state as a function of number of applied Cliffords. We extract an EPC of 1% for our highest-fidelity double pulsed gate.

between the swapped and not-swapped possibilities. A second pulse then forms an interferometer and will either constructively or destructively interfere, depending on the path length difference. In our case, we adjust the path length by varying the timing between the pulses. We thus split our gate pulse into two. We use the amplitude of the pulses to adjust the CZ angle and we adjust the wait time between the pulses to cancel out the ISWAP angle.

We explore the swap mechanism in Fig. 4(a), where we plot the probability of finding Q1 in the excited state as a function of the wait time for the four basis states  $|00\rangle$ ,  $|10\rangle$ ,  $|01\rangle$ , and  $|11\rangle$ . While with no delay the pulse sequence results in an almost perfect swap, at 50 ns the swap is canceled. In Fig. 4(b), we plot the results of interleaved randomized benchmarking. Our double pulsed gate of 110 ns achieves an EPG of  $0.006 \pm 0.002$ . Because of a high readout error on this pair, we implement a basic readout correction described in Ref. [29] for the data presented in Fig. 4(b).

In conclusion, we developed a new type of a tunable coupler that is suitable for operations between fixed-frequency transmons. Using this BBQ architecture, we demonstrated gate fidelities of 99.85% on isolated 2-qubit devices. We obtained similar results on additional devices, showing the repeatability of this scheme. BBQ also allows us to operate with the coupler near its flux sweet spot, resulting in enhanced stability.

We thank D. McKay for helpful discussions, P. Gumann and J. Rozen for cryostat assistance, and A. Córcoles, M. Takita, A. Finck, and A. Kandala for technical assistance.

- R. J. Schoelkopf, Demonstration of two-qubit algorithms with a superconducting quantum processor, Nature (London) **460**, 240 (2009).
- [2] A. Blais, R.-S. Huang, A. Wallraff, S. M. Girvin, and R. J. Schoelkopf, Cavity quantum electrodynamics for super-conducting electrical circuits: An architecture for quantum computation, Phys. Rev. A 69, 062320 (2004).
- [3] G. S. Paraoanu, Microwave-induced coupling of super-conducting qubits, Phys. Rev. B **74**, 140504(R) (2006).
- [4] C. Rigetti and M. Devoret, Fully microwave-tunable universal gates in superconducting qubits with linear couplings and fixed transition frequencies, Phys. Rev. B 81, 134507 (2010).
- [5] S. Puri and A. Blais, High-Fidelity Resonator-Induced Phase Gate with Single-Mode Squeezing, Phys. Rev. Lett. 116, 180501 (2016).
- [6] H. Paik, A. Mezzacapo, M. Sandberg, D. T. McClure, B. Abdo, A. D. Córcoles, O. Dial, D. F. Bogorin, B. L. T. Plourde, M. Steffen, A. W. Cross, J. M. Gambetta, and J. M. Chow, Experimental Demonstration of a Resonator-Induced Phase Gate in a Multiqubit Circuit-QED System, Phys. Rev. Lett. 117, 250502 (2016).
- [7] J. M. Chow, J. M. Gambetta, A. W. Cross, S. T. Merkel, C. Rigetti, and M. Steffen, Microwave-activated conditional-phase gate for superconducting qubits, New J. Phys. 15, 115012 (2013).
- [8] J. B. Hertzberg, E. J. Zhang, S. Rosenblatt, E. Magesan, J. A. Smolin, J.-B. Yau, V. P. Adiga, M. Sandberg, M. Brink, J. M. Chow *et al.*, Laser-annealing Josephson junctions for yielding scaled-up superconducting quantum processors, arXiv:2009.00781.
- [9] S. Krinner, S. Lazar, A. Remm, C. K. Andersen, N. Lacroix, G. J. Norris, C. Hellings, M. Gabureac, C. Eichler, and A. Wallraff, Benchmarking Coherent Errors in Controlled-Phase Gates Due to Spectator Qubits, Phys. Rev. Applied 14, 024042 (2020).
- [10] D. C. McKay, S. Sheldon, J. A. Smolin, J. M. Chow, and J. M. Gambetta, Three-Qubit Randomized Benchmarking, Phys. Rev. Lett. 122, 200502 (2019).
- [11] T. Cai, X. Han, Y. Wu, Y. Ma, J. Wang, H. Zhang, H. Wang, Y. Song, and L. Duan, Impact of Spectators on a Two-Qubit Gate in a Tunable Coupling Superconducting Circuit, Phys. Rev. Lett. 127, 060505 (2021).
- [12] F. Yan, P. Krantz, Y. Sung, M. Kjaergaard, D. L. Campbell, T. P. Orlando, S. Gustavsson, and W. D. Oliver, Tunable Coupling Scheme for Implementing High-Fidelity Two-Oubit Gates, Phys. Rev. Applied 10, 054062 (2018).
- [13] P. Mundada, G. Zhang, T. Hazard, and A. Houck, Suppression of Qubit Crosstalk in a Tunable Coupling Superconducting Circuit, Phys. Rev. Applied **12**, 054023 (2019).
- [14] B. Foxen *et al.* (Google AI Quantum), Demonstrating a Continuous Set of Two-Qubit Gates for Near-Term Quantum Algorithms, Phys. Rev. Lett. **125**, 120504 (2020).
- [15] M. C. Collodo, J. Herrmann, N. Lacroix, C. Kraglund Andersen, A. Remm, S. Lazar, J.-C. Besse, T. Walter, A. Wallraff, and C. Eichler, Implementation of Conditional Phase Gates Based on Tunable *zz* Interactions, Phys. Rev. Lett. **125**, 240502 (2020).

<sup>\*</sup>These authors contributed equally to this work.

<sup>[1]</sup> L. DiCarlo, J. M. Chow, J. M. Gambetta, Lev S. Bishop, D. I. Schuster, J. Majer, A. Blais, L. Frunzio, S. M. Girvin, and

## PDF page 6

- [16] D. C. McKay, S. Filipp, A. Mezzacapo, E. Magesan, J. M. Chow, and J. M. Gambetta, Universal Gate for Fixed-Frequency Qubits via a Tunable Bus, [Phys. Rev. Applied](https://doi.org/10.1103/PhysRevApplied.6.064007) 6[, 064007 \(2016\)](https://doi.org/10.1103/PhysRevApplied.6.064007).
- [17] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan, M. Kjaergaard, A. Greene, G. O. Samach, C. McNally, D. Kim, A. Melville, B. M. Niedzielski, M. E. Schwartz, J. L. Yoder, T. P. Orlando, S. Gustavsson, and W. D. Oliver, Realization of High-Fidelity CZ and ZZ-Free ISWAP Gates with a Tunable Coupler, [Phys. Rev. X](https://doi.org/10.1103/PhysRevX.11.021058) 11, 021058 [\(2021\).](https://doi.org/10.1103/PhysRevX.11.021058)
- [18] V. Negîrneac, H. Ali, N. Muthusubramanian, F. Battistel, R. Sagastizabal, M. S. Moreira, J. F. Marques, W. Vlothuizen, M. Beekman, N. Haider, A. Bruno, and L. DiCarlo, High-Fidelity Controlled-Z Gate with Maximal Intermediate Leakage Operating at the Speed Limit in a Superconducting Quantum Processor, Phys. Rev. Lett. 126[, 220502 \(2021\)](https://doi.org/10.1103/PhysRevLett.126.220502).
- [19] M. D. Hutchings, J. B. Hertzberg, Y. Liu, N. T. Bronn, G. A. Keefe, M. Brink, J. M. Chow, and B. L. T. Plourde, Tunable Superconducting Qubits with Flux-Independent Coherence, [Phys. Rev. Applied](https://doi.org/10.1103/PhysRevApplied.8.044003) 8, 044003 (2017).
- [20] Y. Xu, J. Chu, J. Yuan, J. Qiu, Y. Zhou, L. Zhang, X. Tan, Y. Yu, S. Liu, J. Li, F. Yan, and D. Yu, High-Fidelity, High-Scalability Two-Qubit Gate Scheme for Superconducting Qubits, Phys. Rev. Lett. 125[, 240503 \(2020\).](https://doi.org/10.1103/PhysRevLett.125.240503)
- [21] J. Gambetta, J. M. Chow, and M. Steffen, Building logical qubits in a superconducting quantum computing system, [npj](https://doi.org/10.1038/s41534-016-0004-0) [Quantum Inf.](https://doi.org/10.1038/s41534-016-0004-0) 3, 2 (2017).
- [22] See Supplemental Material at [http://link.aps.org/](http://link.aps.org/supplemental/10.1103/PhysRevLett.127.080505) [supplemental/10.1103/PhysRevLett.127.080505](http://link.aps.org/supplemental/10.1103/PhysRevLett.127.080505) for a

- description of our ZZ measurement techniques, pulse shaping, our Clifford decomposition, and coherence limits, which includes [23,24].
- [23] L. Trifunovic, O. Dial, M. Trif, J. R. Wootton, R. Abebe, A. Yacoby, and D. Loss, Long-Distance Spin-Spin Coupling via Floating Gates, Phys. Rev. X 2[, 011006 \(2012\)](https://doi.org/10.1103/PhysRevX.2.011006).
- [24] A. Gold, J. P. Paquette, A. Stockklauser, M. J. Reagor, M. Sohaib Alam, A. Bestwick, N. Didier, A. Nersisyan, F. Oruc, A. Razavi, B. Scharmann, E. A. Sete, B. Sur, D. Venturelli, C. James Winkleblack, F. Wudarski, M. Harburn, and C. Rigetti, Entanglement across separate silicon dies in a modular superconducting qubit device, [arXiv:2102.13293.](https://arXiv.org/abs/2102.13293)
- [25] J. M. Martinis and M. R. Geller, Fast adiabatic qubit gates using only <sup>σ</sup>z control, Phys. Rev. A <sup>90</sup>[, 022307 \(2014\).](https://doi.org/10.1103/PhysRevA.90.022307)
- [26] D. C. McKay, C. J. Wood, S. Sheldon, J. M. Chow, and J. M. Gambetta, Efficient Z gates for quantum computing, [Phys.](https://doi.org/10.1103/PhysRevA.96.022330) Rev. A 96[, 022330 \(2017\)](https://doi.org/10.1103/PhysRevA.96.022330).
- [27] A. D. Córcoles, J. M. Gambetta, J. M. Chow, J. A. Smolin, M. Ware, J. Strand, B. L. T. Plourde, and M. Steffen, Process verification of two-qubit quantum gates by randomized benchmarking, Phys. Rev. A 87[, 030301\(R\) \(2013\).](https://doi.org/10.1103/PhysRevA.87.030301)
- [28] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster, J. Majer, Alexandre Blais, M. H. Devoret, S. M. Girvin, and R. J. Schoelkopf, Charge-insensitive qubit design derived from the Cooper pair box, Phys. Rev. A 76[, 042319 \(2007\).](https://doi.org/10.1103/PhysRevA.76.042319)
- [29] T. F. Watson, S. G. J. Philips, E. Kawakami, D. R. Ward, P. Scarlino, M. Veldhorst, D. E. Savage, M. G. Lagally, M. Friesen, S. N. Coppersmith et al., A programmable twoqubit quantum processor in silicon, [Nature \(London\)](https://doi.org/10.1038/nature25766) 555, [633 \(2018\)](https://doi.org/10.1038/nature25766).
