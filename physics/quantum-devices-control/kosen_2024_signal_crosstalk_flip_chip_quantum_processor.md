Source: https://doi.org/10.1103/PRXQuantum.5.030350
PDF sha256: 452cc36bdfa37a638a0fcd0610f3b94131f0d771af35bd1c3aeceee01438f74e
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of kosen_2024_signal_crosstalk_flip_chip_quantum_processor.pdf

Transcription of `kosen_2024_signal_crosstalk_flip_chip_quantum_processor.pdf` in this directory, 21 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

# **Signal Crosstalk in a Flip-Chip Quantum Processor**

Sandoko Kosen [,](https://orcid.org/0000-0001-9560-9932) [,\\*](#page-0-0) Hang-Xi Li [,](https://orcid.org/0000-0002-2578-306X) Marcus Rommel,<sup>1</sup> Robert Rehammar [,](https://orcid.org/0000-0001-8167-3810) Marco Caputo [,](https://orcid.org/0009-0006-1321-1108) 2 Leif Grönberg,<sup>2</sup> Jorge Fernández-Pendás [,](https://orcid.org/0000-0003-3814-9364) Anton Frisk Kockum [,](https://orcid.org/0000-0002-2534-3021) Janka Biznárová,<sup>1</sup> Liangyu Chen [,](https://orcid.org/0000-0002-5072-2445) Christian Križa[n](https://orcid.org/0000-0002-5059-7998) , Andreas Nylander [,](https://orcid.org/0000-0002-9724-1892) Amr Osman,<sup>1</sup> Anita Fadavi Roudsari [,](https://orcid.org/0000-0002-1165-4515) 1 Daryoush Shiri [,](https://orcid.org/0000-0001-6115-5821) Giovanna Tancredi [,](https://orcid.org/0000-0002-3628-8398) Joonas Govenius [,](https://orcid.org/0000-0002-7208-9556) and Jonas Bylander [1](https://orcid.org/0000-0003-4521-710X)[,†](#page-0-1)

> 1 *[Chalmers University of Technology,](https://ror.org/040wg7k59) Gothenburg 412 96, Sweden [VTT Technical Research Centre of Finland,](https://ror.org/04b181w54) VTT Espoo FI-02044, Finland*

(Received 9 March 2024; revised 13 June 2024; accepted 16 July 2024; published 12 September 2024)

Quantum processors require a signal-delivery architecture with high addressability (low crosstalk) to ensure high performance already at the scale of dozens of qubits. Signal crosstalk causes inadvertent driving of quantum gates, which will adversely affect quantum gate fidelities in scaled-up devices. Here, we demonstrate packaged flip-chip superconducting quantum processors with signal-crosstalk performance competitive with those reported in other platforms. For capacitively coupled qubit-drive lines, we find on-resonant crosstalk better than −27 dB (average −37 dB). For inductively coupled magnetic-flux-drive lines, we find less than 0.13% direct-current flux crosstalk (average 0.05%). These observed crosstalk levels are adequately small and indicate a decreasing trend with increasing distance, which is promising for further scaling up to larger numbers of qubits. We discuss the implications of our results for the design of a low-crosstalk on-chip signal-delivery architecture, including the influence of a shielding tunnel structure, potential sources of crosstalk, and estimation of crosstalk-induced qubit-gate error in scaled-up quantum processors.

DOI: [10.1103/PRXQuantum.5.030350](http://dx.doi.org/10.1103/PRXQuantum.5.030350)

# **I. INTRODUCTION**

The quest for demonstrating quantum computational advantage and fault-tolerant quantum computation has inspired the realization of integrated quantum processors [\[1–](#page-18-0)[4\]](#page-18-1). A prominent physical platform is based on superconducting qubits, which are typically submillimeter in size, made of lithographically defined thin-film devices on low-loss substrates and which operate at frequencies below 10 GHz in a cryogenic environment. Scaling up superconducting quantum processors requires microchip integration in an extensible design while maintaining high-fidelity qubit performance through predictable device parameters and high-yield fabrication.

An outstanding problem for extensible designs is onchip signal routing that enables components within the processor to be selectively addressed and read out. In current

\*Contact author: sandoko.kosen@gmail.com †Contact author: jonas.bylander@chalmers.se

*Published by the American Physical Society under the terms of the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) license. Further distribution of this work must maintain attribution to the author(s) and the published article's title, journal citation, and DOI.*

technology, signals are usually routed from the edge of the chip, where wire bonds make connection to a printed circuit board (PCB) and further on to connectors on a microwave package. If the signal is insufficiently shielded, crosstalk ensues and results in quantum gate errors that render quantum computation infeasible. Active crosstalksuppression techniques, which involve characterizing the crosstalk matrix and applying its inverse [\[5](#page-18-2)[–10\]](#page-19-0), are prohibitively challenging at scale. We must thus ensure that the circuit architecture supports adequate passive crosstalk suppression by proper routing and shielding techniques. Therefore, the road map for next-generation quantum processors requires an understanding of the influence of densely routed signal lines and an informed strategy for signal delivery with low crosstalk. This challenge has not received the attention that it deserves.

Signal crosstalk can be investigated in dedicated devices, yielding data that is conceptually simple to interpret. Alternatively, it can be performed with devices that are designed for actual implementations of quantum algorithms. Such an approach enables a more accurate assessment of the relevant crosstalk level and can tease out potential crosstalk mechanisms that are dominant at a larger scale, although at the expense of a more complicated data interpretation. This work adopts the second approach but we consider the two approaches to be equally

## PDF page 2

FIG. 1. A packaged 25-qubit superconducting quantum processor. (a) An enlargement of the flip-chip processor packaged with wire bonds and printed-circuit-board (PCB) technology. (b) An illustration of the cross section, showing the copper lid and base, with an enlargement showing the material stack (not to scale—Si, silicon; Al, aluminum; NbN, niobium nitride; In, indium).

valuable, necessary, and complementary to each other in the long run.

In this work, we demonstrate packaged multiqubit processors consisting of 25 qubits in a flip-chip module, as shown in Fig. [1.](#page-1-0) The processor is designed according to a repeating signal-line routing pattern, which is, in principle, scalable to hundreds of qubits. We characterize the microwave crosstalk (selectivity of driving) of the qubit drive lines ("*xy* lines"), which are capacitively coupled to their target qubits, and of flux lines ("*z* lines"), which are inductively coupled to frequency-tunable couplers that mediate two-qubit gates.

The results show crosstalk performance approaching average values of −40 dB for microwave-drive *xy* crosstalk and 0.05% for direct-current flux crosstalk, competitive with reported performance from other superconducting [\[5,](#page-18-2)[8](#page-19-1)[,9,](#page-19-2)[11](#page-19-3)[,12\]](#page-19-4) and nonsuperconducting [\[13](#page-19-5)[–15\]](#page-19-6) platforms. We show that a substantial contribution to the flux crosstalk is due to the proximity of the grounded end of a victim *z* line to a neighboring source *z* line and it can be suppressed either by a shielding tunnel structure or by adequate separation. On the other hand, enclosing the *xy* lines with shielding tunnels does not improve *xy* crosstalk despite the denser routing layout, suggesting that the intrinsic crosstalk level due to direct capacitive interaction is better than the observed performance (simulation of a simplified model of our processor also suggests that this is the case).

It is generally desirable for the crosstalk level to be not only low but also to decrease with increasing separation and our results suggest such a trend. To quantify, a reasonable *xy*-crosstalk magnitude to aim for is such that the total single-qubit gate error does not exceed the 0.1% threshold recommended for quantum error correction [\[16\]](#page-19-7). We provide numerical estimates of the total single-qubit gate error based on the measured *xy* crosstalk and sketch the further improvement required for the total error to stay below the 0.1% threshold for processors at the 100-qubit level. We discuss potential sources of crosstalk, its impact on gate fidelities, and its implication for future designs of low-crosstalk processors.

# **II. QUANTUM PROCESSOR ARCHITECTURE**

Our superconducting quantum processing unit (QPU) consists of a two-tiered architecture [\[17](#page-19-8)[–20\]](#page-19-9) separating the circuit into a qubit chip ("Q-chip") and a control chip ("C-chip") [see Figs. [1](#page-1-0) and [2\(a\)\]](#page-2-0). The Q-chip comprises 25 fixed-frequency transmon (Xmon) qubits [\[21](#page-19-10)[–23\]](#page-19-11) and 40 frequency-tunable two-qubit couplers laid out on a square grid with 2-mm pitch [\[24\]](#page-19-12). This relatively large pitch is a choice made out of convenience, since the QPU performance is limited by gate performance rather than the number of devices that can be fitted on a die. The C-chip comprises a signal-delivery system routed through coplanar waveguide transmission lines on the chip surface. This signal-routing strategy is extensible to hundreds of qubits. In Fig. [2\(b\),](#page-2-0) we show a part of the flip-chip module with the Q-chip overlaid on the C-chip.

In Fig. [2\(c\),](#page-2-0) we show the coupling points of the control wires to the qubit and coupler. The qubit-readout resonators ["ro" in Fig. [2\(c\)\]](#page-2-0) are quarter-wavelength resonators with the open end positioned directly opposite a qubit. The resonators are undulated to reduce coupling with neighboring couplers. The open ends of the qubitcontrol lines (*xy*) are positioned to ensure adequate capacitive coupling while minimizing Purcell decay of the qubit into its own *xy* line. Finally, the coupler-control lines (*z*) each terminate in a loop of wire that is shorted to ground at one end, without a ground plane within the loop. The current in the *z* loop couples magnetic flux into the superconducting quantum interference device (SQUID) of the coupler positioned opposite the loop; this SQUID connects the island of the coupler to the ground plane.

The second processor discussed in this work has aluminum tunnel structures [\[25](#page-19-13)[,26\]](#page-19-14) added to the C-chip, shielding the signal lines as shown in Fig. [2\(d\).](#page-2-0) These tunnels extend across the signal lines and connect the ground planes on either side.

The Q-chip and C-chip consist of 12 mm × 12 mm and 14.3 mm × 14.3 mm silicon dies, respectively, which are aligned and joined together by flip-chip bonding, with a target interchip separation of 8 µm. The bump-bond layout is symmetrical across the dies, with 2900 superconducting bumps connecting the ground planes of the two tiers and with a denser distribution surrounding the qubit and

## PDF page 3

FIG. 2. The quantum processor architecture. (a) The two-tier flip-chip material stack (not to scale). (b) An overlapped view of the Q-chip (qubits and couplers) and C-chip (control and readout elements) for the bottom 15 qubits of a 25-qubit QPU, showing the bump pattern (black dots). For an easier view, both ground planes are removed from this illustration. (c) Left: a transmon (Xmon) qubit located on the Q-chip, with the xy line (qubit drive) and the readout resonator located on the C-chip. The cutout on the Q-chip layer shows the end parts of the xy line and of the resonator. The panel on the far left shows an enlargement of the region around the tip of the xy line. Right: a z loop (flux loop) on the C-chip, the center of which lies directly opposite a superconducting quantum interference device (SQUID) on the Q-chip (wiring and substrate on the Q-chip not shown). (d) The aluminum tunnel structure shielding a signal line. The micrograph shows one part of the transmission line covered with a tunnel. (e) The qubit indexing used in this paper. (f) The two-frequency subgroup strategy: the filled and empty circles indicate transmons with two different anharmonicities;  $a_k$  and  $b_k$  indicate different qubit frequencies ( $a_k < b_k$ ), giving a total of eight different frequencies that are tiled according to the schematic.

coupler devices. The bumps consist of evaporated indium cylinders (25- $\mu$ m-wide precompression) with a niobium nitride underbump metallization layer [20].

The two-tier flip-chip module represents a straightforward method for three-dimensional (3D) integration of QPUs, offering more flexibility for signal-wire routing and qubit-array layouts than planar layouts, with a modest increase of fabrication-process complexity. It also enables the use of different fabrication processes for the two chips. In more advanced 3D-integration implementations, superconducting bumps can be used to pass signals between tiers and to provide shielding between components; hard stops (e.g., posts or pillars) can help achieve precise interchip separation [27,28]; furthermore, substrates with metallized through-silicon vias (TSVs) and buried conductors can help create signal redistribution layers [29–31].

Aluminum wire bonds along the periphery of the C-chip transfer signals to and from a multilayer PCB (see Fig. 1). Two wire bonds are placed on every signal launch pad and two grounding wire bonds are placed in between neighboring signal lines. This wiring method works up to hundreds of wires but begins to scale poorly beyond that, which is why ultimately higher-density interconnects and packaging solutions, e.g., ball-grid arrays or land-grid arrays, need to be adapted to superconducting QPU technology.

Our flip-chip fabrication process has been demonstrated to be compatible with qubit (transmon) coherence at the 100-µs level [20]. The wiring layer (signal and ground) on each chip is fabricated in an aluminum process and the Josephson junctions consist of an angle-evaporated Al/AlO<sub>x</sub>/Al sandwich using the two-step Manhattan process [32,33]. The fabrication and packaging steps are

## PDF page 4

outlined in Appendix [A.](#page-9-0) Details on the flip-chip bonding processes can be found in the supplementary material of Ref. [\[20\]](#page-19-9).

The qubits are labeled *qi*, where the index *i* starts in the top left corner of the chip; see Fig. [2\(e\),](#page-2-0) which shows *q*11–*q*25. The element *xyi* is the corresponding *xy* line for *qi*. The couplers and the corresponding *z* lines are labeled *cpi* and *zi*, where the index *i* is a pair of indices indicating the two qubits that are connected by the coupler; e.g., *cp*(11,16) is the coupler connecting *q*<sup>11</sup> and *q*16. The closest separation between a qubit and another *xy* line (excluding its own *xy* line) is about 500 µm.

The routing of signal lines is designed to be as identical as possible for these rows of qubits: *q*6–*q*10, *q*11–*q*15, and *q*16–*q*20. The control elements (*xy*, *z*) are always routed to the desired positions from the corridor above the qubits, while the readout elements are positioned below [see Fig. [2\(b\)\]](#page-2-0). The signal lines are routed horizontally to the periphery of the chip. In each corridor, there is always a *z* line in between the closest pair of *xy* lines. These *z* lines are needed to control horizontally oriented tunable couplers. The vertically oriented couplers, however, are controlled by *z* lines that are routed side by side. Nearest-neighbor control lines are separated by at least 100 µm. For readout purposes, a feed-through transmission line is routed across each corridor and is coupled to five λ/4 resonators. Once a signal line emerges at the qubit-array perimeter, it is routed to the closest available wire-bond launch pad. For qubits in the top row (*q*1–*q*5), the bottom row (*q*21–*q*25), and the corresponding horizontally oriented couplers, the control lines are routed vertically toward the closest wire-bond launch pads. No bumps or air-bridge crossovers are used for signal delivery, i.e., there is no intersection of signal lines.

The allocation of qubit frequency and anharmonicity follows the two-frequency subgroup strategy designed to be compatible with the implementation of parametric controlled-*Z* (CZ) and *i*SWAP gates, which avoids frequency collision between neighboring couplers and minimizes crosstalk due to frequency crowding [\[34\]](#page-20-0). Each subgroup, labeled {*ak*} and {*bk*} (*k* = 1, 2, 3, 4), has four qubit frequencies that are distributed around a central frequency; subgroup *a* has lower frequencies and anharmonicities than subgroup *b*. The layout has a unit cell of 2 × 4 qubits that can be repeatedly tiled as shown in Fig. [2\(f\).](#page-2-0) An alternative visualization is the following: a qubit with frequency in one subgroup is pairwise coupled to qubits with frequencies in the other subgroup.

The readout-resonator frequency allocation is set up to ensure that at the targeted interchip separation, the qubitresonator frequency detuning is generally between 2.1 and 2.6 GHz, which provides sufficient leeway for tolerating frequency shift in case the achieved chip separation is off target. The coupler frequency at zero flux bias is designed to be above the readout-resonator frequency.

We have designed and simulated the flip-chip QPU layout using a combination of the IBM QISKIT METAL design toolkit [\[35\]](#page-20-1), the ANSYS electromagnetic simulation software [\[36\]](#page-20-2), and the L-Edit layout editor [\[37\]](#page-20-3). The simulation technique for individual qubits and resonators is described in Ref. [\[20\]](#page-19-9).

Refer to Appendix [D](#page-12-0) for the chosen numerical values of the qubit frequencies, anharmonicities, readout-resonator frequencies, and coupler frequencies at zero flux bias. Appendix [E](#page-12-1) lists the measured frequency parameters and coherence performance of both processors.

# **III. AGGREGATE CROSSTALK PERFORMANCE**

Here, we quantify the crosstalk (unintended driving) affecting qubits and couplers due to signals applied to the various *xy* lines and *z* lines of the circuit, respectively. To begin with the microwave crosstalk of *xy* lines, consider any pair of a victim qubit (*qi*) and a source *xy* line (*xyj* -<sup>=</sup>*i*) as shown in Fig. [3\(a\).](#page-3-0) The crosstalk is quantified by the rotation of the quantum state vector of *qi* due to a signal being delivered through *xyj* aiming to control its corresponding qubit *qj* . In practice, we compare the Rabi frequency of the victim qubit, *i*,*<sup>j</sup>* , with that of the qubit of the source *xy* line, *<sup>j</sup>* ,*<sup>j</sup>* , for the same *xyj* signal amplitude. Due to the low-crosstalk nature, we always drive the victim qubit on resonance. Their ratio, expressed in decibels (dB), is the

FIG. 3. The aggregate performance of *xy* crosstalk (*xy*) , and dc-flux crosstalk β(dc). (a) An illustration of *xy* crosstalk from a source *xy* line (*j* ) to a victim qubit (*i*) and (b) dc-flux crosstalk from a source *z* line (*j* ) to a SQUID loop of a victim coupler (*i*). (c) The histogram of the on-resonant *xy* crosstalk, *i*,*<sup>j</sup>* , measured on 72 pairs for one flip-chip module with bare transmission lines (labeled "bare") and another module with the majority of the transmission lines covered by "tunnel" structures (labeled "+tunnel"). (d) The histogram of the dc-flux crosstalk, β(dc), measured on 240 pairs.The data indicated as Group 2 are associated with a subset of pairs the *z* lines of which are nearest neighbor. With the tunnels, the maximum value of the dc-flux crosstalk drops to βmax = 0.13%.

## PDF page 5

on-resonant xy crosstalk  $\Lambda_{i,j}$  (referred to as xy selectivity in Ref. [12]),

$$\Lambda_{i,j} = 10 \times \log_{10} \left( \frac{\Omega_{i,j}}{\Omega_{i,j}} \right)^2. \tag{1}$$

The lower the magnitude of  $\Lambda_{i,j}$ , the better that xy line is at selectively driving its corresponding qubit compared to any other qubit (lower crosstalk).

We also characterize the magnetic flux crosstalk in the z lines by examining changes in the magnetic flux  $(\Delta \Phi_i)$  that threads the SQUID of a victim coupler  $cp_i$  due to direct-current (dc) or alternating-current (ac) signals on a source z line  $(z_{j\neq i})$ , aimed to control its corresponding coupler  $cp_j$  [see Fig. 3(b)]. The magnetic flux crosstalk is defined as [38]

$$\beta_{i,j} = \left| \frac{\Delta \Phi_i}{\Delta \Phi_j} \right|. \tag{2}$$

Generally,  $\Phi_i = \Phi_i^{(\mathrm{dc})} + \Phi_i^{(\mathrm{ac})} \cos{(\omega_i^{(\mathrm{ac})} t + \theta_i)}$ , where  $\omega_i^{(\mathrm{ac})}$  is the angular frequency of the ac-flux drive signal and  $\theta_i$  is its phase offset. In practice, the dc- and ac-flux crosstalk, i.e.,  $\beta_{i,j}^{(\mathrm{dc})}$  and  $\beta_{i,j}^{(\mathrm{ac})}$ , are characterized separately. The measurement procedures for the xy, dc-flux, and

The measurement procedures for the *xy*, dc-flux, and ac-flux crosstalk are discussed in Appendix C. As there are also some defective elements in these first-generation processors, the data sets presented in this section are only associated with source-victim pairs that are functional in both processors (bare waveguides and with tunnels) to allow fair comparisons. The complete data sets can be found in Appendix F.

In Fig. 3(c), we show a histogram of the xy crosstalk  $\Lambda^{(xy)}$  with average and standard deviation values of  $-39.4 \pm 3.7$  dB for the processor without tunnels and  $-37.4 \pm 3.9$  dB for the processor with tunnels. These results show that the addition of the tunnel structures to shield the xy lines does not decrease the average xy crosstalk for these packaged processors.

In Fig. 3(d), we show a histogram of the dc-flux crosstalk  $\beta^{(dc)}$  measured both with and without the tunnel structures. Statistics from both data sets show average values of approximately 0.05%. The data from the processor without the tunnels have outliers in between 0.3% and 0.6% (indicated as group 2), which originate from pairs the z lines of which are not only nearest neighbor but also arranged in a specific way (see Sec. IV). These outliers are not present in the data from the processor with the tunnel structures, indicating a suppression of dc-flux crosstalk; here, the maximum measured value is 0.13%. We also note that the measured dc-flux offsets from the processor with tunnels ( $\Phi_{\text{offset, tunnel}}/\Phi_0 = -0.035 \pm 0.008)$  are more narrowly distributed than those from the processor without tunnels  $(\Phi_{\text{offset, no-tunnel}}/\Phi_0 = -0.048 \pm 0.044$ , excluding an outlier at  $0.325\Phi_0$ ).

As the ac-flux crosstalk  $\beta^{(ac)}$  measurement is more involved, we have only characterized it for Group-2 pairs of z lines and couplers, i.e., those that exhibit elevated dc-flux crosstalk in the absence of tunnels. We have chosen to characterize it at a signal frequency of 200 MHz, close to the typical modulation frequency of our parametric couplers. Similarly to dc crosstalk, the largest ac crosstalk drops from 0.85% to 0.24% for tunnel-covered z lines.

In Sec. IV, we examine the distance dependence of the  $\Lambda^{(xy)}$ ,  $\beta^{(dc)}$ , and  $\beta^{(ac)}$  data.

## IV. CROSSTALK VERSUS DISTANCE

During the operation of a quantum processor, gate operations on different qubits and couplers will be performed simultaneously via multiple signal lines. It is therefore important to design the QPU such that the crosstalk decreases for larger separation. Such a property allows for the reuse of the qubit parameters from one unit cell in another as part of our qubit-frequency allocation scheme [see Fig. 2(f)]. It also ensures that the total error due to signal crosstalk remains sufficiently small. In this section, we begin to address this by demonstrating smaller average crosstalk for larger separations.

We have sorted the  $\Lambda^{(xy)}$  data in Fig. 3(c) according to the distance  $d^{(xy)}$  between the victim qubit and the target qubit of the source xy line; the results are shown in Fig. 4. It should be pointed out that there are fewer data points for larger  $d^{(xy)}$  in Fig. 4, i.e., this is natural for planar connectivity such as that implemented in our processors. The dashed lines connecting average  $\Lambda^{(xy)}$  values ( $\bar{\Lambda}^{(xy)}$ , indicated by larger symbols of circles and crosses) hint at a trend of decreasing  $\bar{\Lambda}^{(xy)}$  with  $d^{(xy)}$ . Fitting the average values with an empirical linear model (see Appendix J) yields a slope of approximately -1 dB/mm for these processors.

FIG. 4. The distance dependence of the xy crosstalk,  $\Lambda^{(xy)}$ . The distance  $d^{(xy)}$  is defined as the separation between the victim qubit and the target qubit of the source xy line as illustrated in the inset and further described in Sec. IV. The scatter plot indicates the distribution of the  $\Lambda^{(xy)}$  data for each  $d^{(xy)}$  and the larger symbols denote the average.

## PDF page 6

For the flux-crosstalk data associated with neighboring z lines, we have measured a total of four different configurations within the two lowest-routing corridors shown in Fig. 2(b). Here, we focus specifically on two layouts of neighboring z lines as shown in Figs. 5(a) and 5(b) but the trend is similar in the other two. The first layout consists of the set  $\{A, B, C\} = \{z_{(11,16)}, z_{(12,17)}, z_{(13,18)}\}$ , and the second consists of  $\{A', B', C'\} = \{z_{(16,21)}, z_{(17,22)}, z_{(18,23)}\}$ . The two layouts are very similar: most of the lines are nearest neighbors, beginning from the wire-bond launch pads and leading all the way to the target position (see the chip layout in Fig. 2). The only major difference is in the third z line: C' is routed on the upper side of A' and B', while C

FIG. 5. The layout-dependent flux-crosstalk behavior. (a),(b) Detailed comparisons of the flux crosstalk for two different configurations of nearest-neighbor z lines (refer to the main text for more detail). The darker the background color, the smaller is the crosstalk. (c) The distance dependence of the dc- and ac-flux crosstalk for source-victim pairs arranged as shown in the inset, where the red arrow indicates the source current. The dashed lines connecting the data points are meant as a guide to the eye.

is routed on the *lower* side of A and B. The data with C' as victim from the processor with tunnels are not available due to a defective SQUID in coupler  $cp_{(18,23)}$ .

On the first layout without the tunnel structure, Fig. 5(a), the highest crosstalk  $\beta$  (dc, 0.44%; ac, 0.58%) appears with A as the victim and B as the source line. However, a much lower crosstalk (dc, 0.06%; ac, 0.10%) appears between victim B and source C despite these being nearestneighbor lines in the same way as victim A and source B. Almost similar results are observed on the second layout in Fig. 5(b), with the exception that substantial crosstalk is also observed between victim A' and source C' (and also between victim B' and source C').

Another noteworthy feature is the asymmetry of crosstalk for nearest-neighbor lines. The effect is most pronounced for the processor without tunnels. While there is substantial crosstalk from source B to victim A (dc, 0.44%; ac, 0.58%), much lower crosstalk is measured when the roles of victim and source are interchanged (dc, 0.01%; ac, 0.09%). Similar asymmetry is observed in the other layout.

These observations, combined with the symmetric positioning of the wire-bond launch pads of the z lines, indicate that the major source of flux crosstalk in the processor without tunnels is coming from the proximity of the end (current loop) of a victim z line and the nearest section of a source z line. Under this model, we have plotted the flux crosstalk for victim-source pairs arranged as shown in the inset of Fig. 5(c). Without tunnels, the flux crosstalk becomes smaller for larger spatial separation  $d_z$ . By adding tunnels, the previously high flux crosstalk at small separation ( $d_z = 150 \, \mu \text{m}$ ) decreases by close to a factor of 10, down to the level of 0.1–0.2%. Flux crosstalk at larger separation ( $d_z = 250 \, \mu \text{m}$ ) is relatively unaffected by the presence of tunnels.

### V. DISCUSSION

#### A. Qubit-drive crosstalk

A distinct feature in this processor is the presence of densely routed signal lines in the proximity of qubits within the flip-chip environment [see Fig. 2(b)]. However, for xy crosstalk, direct capacitive interaction between qubits and these signal lines cannot be the dominant mechanism, since we do not observe any decrease in average crosstalk after covering the xy lines with shielding tunnel structures [see Figs. 3(c) and 4]. This conclusion is consistent with several electrostatic simulations designed to study the expected impact of the tunnel structure and xy-crosstalk level due to the direct xy-qubit capacitive interaction. First, we simulate a simplified model containing two victim qubits (denoted as  $q_1$  and  $q_2$ ) and two source xy lines (denoted as  $xy_3$  and  $xy_4$ ) under two situations: with and without a tunnel structure on  $xy_4$  (see Appendix G). The result shows that while the coupling capacitances

## PDF page 7

between *xy*<sup>3</sup> and both qubits remain unaffected, the coupling capacitances between *xy*<sup>4</sup> and both qubits are lower when the tunnel structure is present on top of *xy*4. Second, we simulate the expected *xy*-crosstalk level that is solely caused by the direct capacitive interaction between the *xy* lines in the processor (excluding wire bonds, PCB signal traces, and tunnels) and the qubits (see Appendix [H\)](#page-14-0). The result puts the expected *xy*-crosstalk level within the range of −49 dB to −150 dB, much smaller than the measured *xy*-crosstalk level in our work.

The average of (*xy*) is −36 dB for the nearest-neighbor pairs (*d*(*xy*) = 2.0 mm) and −37 dB for the next-nearestneighbor pairs (*d*(*xy*) = 2.8 mm). The highest values are −30 dB for both nearest and next-nearest neighbors. This performance compares favorably with results from a 17-qubit processor (in a single-chip geometry) employed in Ref. [\[11\]](#page-19-3) for the demonstration of distance-three quantum error correction. There, the highest crosstalk among the reported values for next-nearest-neighbor qubit (*d*(*xy*) = 2.4 mm) was −20 dB (excluding one outlier at −4 dB). It is not straightforward to identify the factors that have led to the lower *xy*-crosstalk level demonstrated in our work despite having a denser signal-line layout. However, there are good reasons to believe that the chip geometry is important. The electric field of a coplanar waveguide is more confined in a flip-chip geometry than in a planar chip, due to the presence of a ground plane on the opposing chip (the typical size of a transmission line is approximately 10 µm and our chip separation is 8 µm) [\[20\]](#page-19-9). Additionally, in a single planar chip, the signal lines can interact parasitically with qubits via the field in the substrate, whereas in our flip-chip module, the signal lines and qubits are separated onto different chips.

The data for (*xy*) are sorted according to the qubitqubit distance *d*(*xy*) in Fig. [4](#page-4-1) purely for a scaling argument. We believe that for a signal-delivery architecture to be scalable, not only should (*xy*) decrease with *d*(*xy*) but the behavior should not be too dependent on the architecture itself. Such a behavior would not only unlock favorable scaling behavior but it would also simplify the hardware design process by reducing the number of factors that need to be accounted for. When combined with a judicious choice of qubit-frequency allocation and a substantial decrease in (*xy*) for increasing *d*(*xy*) , it can lead to very low total crosstalk error. Having said that, the relatively large spread of (*xy*) for every qubit-qubit distance *d*(*xy*) in Fig. [4](#page-4-1) provides a clue that the major parasitic interaction in our processors does not have a strong dependence on *d*(*xy*) . The dominant source of crosstalk must therefore be sought elsewhere. Nevertheless, there is a hint of lower crosstalk for larger separation when comparing the average value of (*xy*) versus *d*(*xy*) , suggesting a favorable scaling behavior, at least for the size of processors examined in this work.

An alternative to flip-chip geometry called the "coaxmon" has reported nearest-neighbor (*d*(*xy*) = 2 mm) crosstalk (*xy*) ∼ −56 dB, roughly 20 dB better than the result reported in this work [\[12\]](#page-19-4). This has been obtained using a smaller 2 × 2 qubit chip (5 × 5 mm2) in an enclosure that is inductively shunted at the center to repel the cavity modes to higher frequencies, an additional feature that is yet to be present in our system. It will be interesting to compare the crosstalk performance between the two geometries for increasing processor size.

Going forward, a combination of experimental investigations on more dedicated devices and numerical validations will be useful to further understand various *xy*-crosstalk mechanisms and configurations in which they might prevail. Electromagnetic modeling of the whole system (chips, wire bonds, packaging), such as the one presented here, is computationally challenging due to the wide range of feature sizes (several micrometers for signal lines to several centimeters for the packaging) that need to be accounted for.

In this work, we have instead taken an alternative approach of simulating simplified versions of the model to understand the relative impact of direct capacitive interaction and the proximity of the signal lines to the *xy*crosstalk level. As discussed before and in more detail in Appendix [H,](#page-14-0) the expected *xy*-crosstalk level caused by the direct *xy*-qubit capacitive interaction between the qubits and the signal lines (excluding the wire bonds, PCB signal traces, and tunnels) is between −49 dB and −150 dB, with an average of −94 dB, which is much smaller than the range measured in this work. In addition, we simulate the expected microwave crosstalk between neighboring signal lines in a simplified model consisting of five signal lines beginning at the PCB level all the way into the flip-chip environments (Appendix [I\)](#page-15-0). The results show nearest-neighbor and next-nearest neighbor crosstalk at the level of −55 dB and −69 dB at the PCB level, which are then substantially increased to −40 dB and −49 dB after including the wire bonds and signal launch pads. Further extension of the signal lines into the flip-chip environment does not substantially change the crosstalk level, a trend that is attributed to the much smaller geometry of the transmission line compared to the line-to-line separation. Crucially, the closest pair of *xy* lines in our processor is at least in a *next-nearest neighbor* configuration, as there is at least one *z* line needed to control the tunable coupler connecting two neighboring qubits. The simulation puts a bound of around −47 dB to the next-nearest neighbor signal lines, which is still one order of magnitude smaller than the average *xy* crosstalk measured for qubits controlled by the next-nearest neighbor pairs of *xy* lines (−36 dB).

The *xy*-crosstalk performance of our quantum processors compares competitively with those demonstrated in trapped ions [\[13,](#page-19-5)[39–](#page-20-5)[44\]](#page-20-6), neutral atoms [\[14,](#page-19-21)[45,](#page-20-7)[46\]](#page-20-8), and

## PDF page 8

spin qubits [15,47]. In trapped-ion systems, the lowest nearest-neighbor crosstalk (without active cancellation) has been reported to be 0.2% for a linear chain of four <sup>171</sup>Yb<sup>+</sup> ions, which is equivalent to an individual excitation-error probability of  $10^{-5}$  [13]. In our case, the qubit-frequency allocation strategy results in nearest-neighbor qubits that are naturally far detuned. For  $\Omega_R/2\pi = 25$  MHz and with the smallest nearest-neighbor detuning being 420 MHz, the individual excitation-error probability is already at the level of 10<sup>-6</sup>; larger detuning will further reduce the signal-crosstalk-induced error probability. Neutral-atoms systems have reported an average spin-flip crosstalk probability of  $2 \times 10^{-3}$  on a twodimensional array of 49 Cs atoms [14]. Spin-qubit systems, such as the four-atom Ge processor in Ref. [15], show an average individual single-qubit gate error between  $10^{-2}$ and  $10^{-4}$ .

#### B. Flux crosstalk

The flux-crosstalk data [Figs. 5(a) and 5(b)] clearly illustrate specific configurations of z lines that cause some of the largest flux-crosstalk values measured in our processors (between 0.4 and 1%). We have demonstrated two strategies to achieve lower flux crosstalk. The first strategy uses a tunnel structure to suppress crosstalk for the same pairs of z lines below approximately 0.2%. This conclusion is only made possible due to the use of identical signalline footprints in the two devices. The second strategy is by ensuring a sufficiently large separation  $d_z$  between the head of the victim z line and the closest point of a source z line, in our case  $d_z = 250 \,\mu\text{m}$ . Further investigation is needed to pinpoint precisely the cause of crosstalk reduction due to the tunnel structure: whether the tunnel prevents current leakage to the victim z line and/or if it suppresses the direct interaction between the source z line and the victim SQUID.

The average dc-flux crosstalk  $\beta^{(dc)}$  over all measurable pairs is approximately 0.05%. At least another tenfold reduction is possible through active flux compensation, potentially pushing the dc-flux crosstalk level below 0.01%. A similar reduction has also been demonstrated in a 16-qubit processor [8]. Note that the passive stability of our system is much better: a variation of 32  $\mu\Phi_0$  is measured for one of the z lines over a period of 3 h, corresponding to a lowest measurable  $\beta^{(dc)} = 0.003\%$  (for more information, see Appendix C 2).

The relative standard deviation of dc-flux offset in the processor with the tunnels ( $\pm 0.008\Phi_0, 23\%$ ) is smaller than the value in the processor without the tunnels ( $\pm 0.044\Phi_0, 92\%$ ). In our system, we believe that the dc-flux offsets are determined by the magnetic field present in the system when the aluminum film becomes superconducting. The magnetic field can be due to the remnant static field generated by sources external to the processor as well

as any circulating current in it. The two processors are measured in the same cryogenic environment, except for the different PCBs, oxygen-free high-thermal-conductivity copper base plate and cover lid, and screws. The remnant static field should, in principle, remain the same at the base temperature and this is likely reflected in the nonzero average values. In addition, the input current into each z line is always set to zero during the cool-down. Therefore, it is not straightforward to determine the role of the tunnel structure in narrowing down the dc-flux offset distribution solely from the data presented in this work.

There is a varying degree of tolerable  $\beta^{(dc)}$  performance. An active flux-calibration technique applied to devices for quantum annealing applications achieves a maximum calibration error of 0.17% [5], which is still higher than the passive performance already obtained by our architecture. In another work employing a superconducting quantum simulator to study many-body dynamics,  $\beta^{(dc)}$  has been reduced from 6% down to 0.01% through active compensation [9].

Overall, this work demonstrates that careful routing and shielding of z lines can already enable low crosstalk without active flux compensation. The crosstalk performance can be compared with various leading devices (flipchip, single-chip) where the maximum flux crosstalk (no compensation) varies between 0.8% and 40% [5,9,11, 38,48–50]. In Refs. [49,50], the authors have noted an improvement in maximum flux crosstalk down to the level of 1.6% when moving from single-chip to flip-chip geometry on nominally similar chip sizes, attributed to the use of a smaller SQUID area. Meanwhile, Ref. [11] has already registered a maximum flux crosstalk of 0.8% on a singlechip geometry, lower than those achieved in Ref. [50]. The use of air-bridge crossovers meant to stitch the ground plane of a z line does not immediately result in full crosstalk reduction, as demonstrated by Ref. [48], where the authors have measured flux crosstalk of between 0.1% and 4%. Finally, we note that in Ref. [51], the author has obtained  $\beta^{(dc)} = 0.8\%$ , despite using a z line with a dedicated return-current line. This illustrates the complex story of flux-crosstalk improvement efforts and the signal-line architecture presented in this work is proof that it is still possible to achieve lower crosstalk via careful design. Further investigations are required to understand the source of flux crosstalk at the 0.1% level.

#### C. Impact on gate fidelities

It is instructive to understand the detrimental effect of the *xy*-crosstalk performance on the single-qubit gate fidelity. In previous work, we have calculated the fidelity using the relative coupling strength between the relevant processes and detuning between the associated transitions [34]. The calculation models the qubits as two-level systems and assumes that the crosstalk activates undesired

## PDF page 9

processes one by one. The measured (*xy*) varies between −56 dB and −27 dB, which corresponds to relative coupling strengths between 0.15% and 4%. Assuming a 20-ns single-qubit gate, the worst (*xy*) of −27 dB would require detuning between the relevant qubit transitions larger than 28 and 42 MHz (about 1% of typical qubit frequencies) to have average gate fidelities above 99.9% and 99.99%, respectively.

The limits are more stringent when we consider influence from all other qubits on the chip. We examine the total single-qubit gate fidelity *F*1*<sup>Q</sup>* for increasing processor size. We assume an empirical linear behavior of ¯ (*xy*) on *d*(*xy*) and numerically simulate the impact on *F*1*<sup>Q</sup>* under certain assumptions (see Appendixes [J–](#page-16-0)[L\)](#page-17-0). For the data in Fig. [4,](#page-4-1) the slope *mxy* and intercept <sup>0</sup> values of the empirical linear model are approximately −1 dB/mm and −34 dB, respectively. The simulations suggest, for QPUs with up to 1000 qubits, that an improvement to −2.0 dB/mm and −50 dB would result in a total single-qubit gate error (due to *xy* crosstalk) well below the 0.1% threshold recommended for quantum error correction using the surface-code [\[16\]](#page-19-7). This conclusion assumes linear dependence of ¯ (*xy*) versus *d*(*xy*) for processor sizes beyond the one measured in this work. We have no reasonable physical argument to assume that it will be the case; nevertheless, this number can serve as a guide for future hardware development and can hopefully spur further effort in verifying this relation for larger processors. Note that a sparser lattice architecture, such as the heavy square or the heavy hexagon, will benefit from less stringent criteria due to fewer neighboring qubits and more relaxed frequency constraints [\[52\]](#page-20-14).

It is more challenging to analyze the influence of flux crosstalk on the two-qubit gate fidelity, since the gate strength depends on both the dc bias and the ac amplitude in a nontrivial way (ω*cp* () is nonlinear). However, there is a relevant situation for which the analysis becomes simpler, at least qualitatively: a parametric gate is applied to a coupler while the other ones idle. Two related conditions arise in that case: (1) the driving amplitude produced on the idling couplers will be very small for low crosstalk such as the one measured in this work, allowing for a perturbative expansion; and (2) the dc contribution stemming from the periodic modulation will be negligible, as it is a higherorder effect in the small-amplitude perturbative expansion. Furthermore, as the dc bias usually stays untouched during the parametric-gate operation, the effect of dc crosstalk on the idling couplers should not change during the gate operations.

An expression for the first-order contribution to the gate strength of the *i*SWAP gate is known for this smallamplitude expansion [\[53\]](#page-20-15), although the result is limited to the regime in which the detunings between the coupler and the qubits are much larger than their coupling strengths. The expression clearly shows that the gate strength is less sensitive to changes in both ac amplitude and dc bias near the zero-flux bias region. This region is also where the couplers are typically more far detuned from the qubits, thus avoiding the physical consequences of being near avoided level crossings, i.e., Rabi oscillations or extra phase acquisition. Therefore, the general prescription to avoid a large impact of crosstalk during the application of parametric gates would be to idle the other couplers to be as far detuned as possible from the neighboring qubits.

# **VI. CONCLUSIONS AND OUTLOOK**

We have demonstrated superconducting quantum processors utilizing an on-chip signal-delivery architecture with competitive crosstalk performance—average onresonant *xy* crosstalk approximately 40 dB, average dc-flux crosstalk approximately 0.05%—surpassing the majority of those demonstrated in other physical platforms. The systematic comparison enabled by adding a tunnel structure on an identical signal-line footprint combined with electrostatic simulations shows that the direct capacitive interaction between densely routed signal lines and the qubits is not the main contributor to the *xy*-crosstalk level in these processors. Electromagnetic simulation of the microwave crosstalk between neighboring signal lines indicates a crosstalk level that is still one order of magnitude smaller than our measured *xy*-crosstalk level. Our work demonstrates wiring layouts that can lead to flux crosstalk at the approximately 1% level and strategies to reduce it down to approximately 0.1%.

Further investigations into the source of crosstalk would be required before proposing reliable mitigation strategies; the lists below are nonexhaustive. For *xy* crosstalk, there are at least three possible avenues to investigate. The first is to numerically investigate the additional *xy* crosstalk caused by the direct capacitive interaction between a victim qubit and the PCB signal traces, including the wire bonds. While they are further away from the qubits, they are also much larger in size compared to the on-chip signal lines. The second is to investigate the role of packaging cavity modes in influencing the *xy*-crosstalk level, as suggested in Ref. [\[54\]](#page-20-16); in particular, the indirect *xy*-qubit interaction mediated by the cavity modes. The third is to investigate the indirect *xy*-qubit interaction mediated by other elements in the processor such as the qubits, the couplers, the readout resonators, and possible parasitic modes. For flux crosstalk, it will be instructive to investigate if it is limited by the leakage of the return current into the victim line (around the launch pads or the area around the SQUID) or if the return current is contributing non-negligible magnetic flux at the location of the victim SQUID.

More advanced signal-delivery architectures will benefit from the use of on-chip signal multiplexers, bumps, and especially redistribution layers enabled by TSVs in a

## PDF page 10

multitiered stack [\[29–](#page-19-17)[31](#page-19-18)[,55](#page-20-17)[,56\]](#page-20-18). Bumps and TSVs are typically a few tens of micrometers in size, which is relatively large compared to typical transmission lines. The extent to which they influence the overall signal-crosstalk level remains to be seen.

The low crosstalk demonstrated in this work and other cited works highlights the strength and flexibility afforded by superconducting circuit architectures. There is still no clear lower limit for the achievable passive crosstalk performance via further system design. We hope to inspire further efforts and discussion in the quantum hardware community, both within and outside superconducting platforms, to investigate the source of crosstalk as well as its behavior as systems scale up in size.

The data that support this work are available from the corresponding author upon reasonable request.

## **ACKNOWLEDGMENTS**

This work was funded by the Knut and Alice Wallenberg (KAW) Foundation through the Wallenberg Centre for Quantum Technology (WACQT) and the European Union Flagship on Quantum Technology HORIZON-CL4-2022-QUANTUM-01-SGA project 101113946 OpenSuperQPlus100. We are grateful to Eleftherios Moschandreou for the technical support. We acknowledge the use of support and resources from Myfab Chalmers, the National Academic Infrastructure for Supercomputing in Sweden (NAISS), and the Swedish National Infrastructure for Computing (SNIC) at Linköping University (partially funded by the Swedish Research Council through Grant Agreements No. 2022-06725 and No. 2018- 05973).

S.K. planned and performed the experiments, analyzed the data, and produced the numerical simulations. S.K. and H.X.L. designed the QPU with inputs from M.R., R.R., J.F.P., A.O., A.F.R., D.S., A.F.K., G.T., and J.Byl. M.R., S.K., A.N., and H.X.L. fabricated the control and quantum chips with inputs from J.Biz, A.O., and A.F.R. M.C. and L.G. formed the In bumps and performed the flipchip bonding. R.R., G.T., and S.K. developed the QPU packaging. C.K. assisted with the writing of measurement instrument drivers. S.K., L.C., C.K., H.X.L., and G.T. set up and maintained the measurement and cryogenic facilities. S.K. and J.Byl wrote the manuscript with input from all authors. G.T., J.G., and J.Byl supervised the project.

R.R., G.T., and S.K. are cofounders and shareholders of Scalinq AB. The other authors declare no competing interests.

# **APPENDIX A: FABRICATION AND PACKAGING**

In this appendix, we outline the fabrication and packaging steps of the processors used in this work. The overall procedure, with the exception of the tunnel-structure fabrication, closely follows Refs. [\[20,](#page-19-9)[32,](#page-19-19)[57\]](#page-20-19).

The first fabrication steps are done on our 2-in. wafers at Chalmers University of Technology. We use two highresistivity intrinsic silicon wafers: one containing four designs of C-chip, while the other has four designs of Qchip. The fabrication process of the ground and wiring layer follows the "Chalmers standard fabrication process" outlined in Ref. [\[57\]](#page-20-19). Each wafer goes through the *SC-1* process, then a deionized- (DI) water rinse, followed by a 1-min dip in a 2% aqueous solution of hydrofluoric acid, before another round of DI-water rinse. The wafer is blow dried using nitrogen gas and is immediately loaded into the load-lock chamber of an electron-beam evaporator to minimize the reoxidation of the silicon surface. Inside the vacuum chamber, the wafer is heated to 300◦C for 10 min and is left to cool down over the course of approximately 20 h. Then, a 150-nm-thick aluminum film is evaporated on the wafer, followed by static oxidation of the exposed aluminum surface for 10 min before we unload the wafer from the evaporator.

Next, a 50-nm-thick niobium nitride film is sputtered on electron-beam patterned resists (after an *in situ* ion-milling step to remove the oxide layer on top of the aluminum film), followed by a lift-off process to create the underbump metallization layer on each wafer. Then, the ground and wiring layer is formed on the aluminum film using optically patterned resists followed by a wet-etching step.

On the wafer containing the Q-chips, we form crosstype Josephson junctions using a two-step process similar to that of Ref. [\[32\]](#page-19-19). The first step is to pattern the junction electrodes on a resist stack using electron-beam lithography, followed by a two-angle evaporation technique (aluminum junction) in an electron-beam evaporator, and then a lift-off process. The second step is to form the patch layer connecting each junction with the rest of the qubit circuitry. The patch layer is electron-beam patterned on a resist stack, followed by ion milling the exposed wiring layer and aluminum-film deposition, after which we perform a lift-off process.

In parallel, we form the tunnel structures following Ref. [\[25\]](#page-19-13), on the wafer containing the C-chips. First, we optically define a pattern of the tunnel "foot" across the wafer on a resist layer, which is then reflowed to form the arch of the tunnel. Then, we perform ion milling on the exposed ground plane before evaporating another aluminum film for the tunnel structure. At this point, the tunnel foot region is the only place where the aluminum tunnel structure is in contact with the ground plane of the chip. Next, we add a second resist on top of the wafer and optically expose the area that is not part of the tunnel structure. The wafer then goes through a wet-etching process before we remove the rest of the resists from the wafer.

We package both wafers in an antistatic bag and send them to VTT. There, 8-µm-tall indium pillars are formed on both wafers on an optically patterned resist layer with a side profile optimized for lift-off. The wafers are then diced

## PDF page 11

into chips before being flip-chip bonded at room temperature. The chip separation is characterized by measuring the distance between the two chips at the various edges of the flip-chip module using a scanning electron microscope. The flip-chip modules are then sent back to Chalmers.

At Chalmers, we glue the flip-chip module or processor on the four corners using GE varnish and let it dry overnight. Afterward, aluminum wire bonds are applied using an automatic wire-bonding machine. The packaged module is finally installed at the mixing chamber stage of the dilution fridge.

## **APPENDIX B: EXPERIMENTAL SETUP**

In Fig. [6,](#page-10-2) we show the measurement apparatus employed in this work at cryogenic and room temperature.

## **APPENDIX C: MEASUREMENT TECHNIQUES**

# **1. The** *xy* **crosstalk**

The *xy* crosstalk *i*,*<sup>j</sup>* [Eq. [\(1\)\]](#page-4-2) is the ratio of the on-resonant Rabi frequencies squared, i.e., (*i*,*<sup>j</sup>* /*<sup>j</sup>* ,*j*)2, expressed in decibels for a fixed drive amplitude *Vj* . We obtain a series of Rabi frequencies for various drive amplitudes [Fig. [7\(a\)\]](#page-10-3) and fit the data with a linear relation

FIG. 6. The measurement apparatus at cryogenic and room temperature.

FIG. 7. The *xy*-crosstalk measurement. (a) The measured Rabi frequencies as a function of the drive amplitude for the self-drive (*i* = *j* ) and cross-drive (*i* -= *j* ) cases. (b) An example of the combined output and transmission characteristics of an rf source with the cables and components all the way down to the PCB level (measured at room temperature).

*i*,*<sup>j</sup>* = *ki*,*<sup>j</sup> Vj* to obtain the slope *ki*,*<sup>j</sup>* . We obtain *kj* ,*<sup>j</sup>* in a separate measurement. *i*,*<sup>j</sup>* is then equal to the ratio (*ki*,*<sup>j</sup>* /*kj* ,*j*)<sup>2</sup> expressed in decibels.

We operate the radio-frequency (rf) source (Rohde & Schwarz SGS100A) in IQ modulation mode. We fix its output power to 14 dBm and vary the amplitudes *Vj* of the signals sent to its IQ input ports. For each *Vj* , we obtain a Rabi oscillation and fit it with an exponentially decaying sinusoidal function. In Fig. [7\(a\),](#page-10-3) we show *i*,*<sup>j</sup>* and *<sup>j</sup>* ,*<sup>j</sup>* versus *Vj* for *i* = 15, *j* = 14.

In the measurement of *i*,*<sup>j</sup>* , we take into account the frequency dependence of the transmission of the cables and components, measured using a vector network analyzer at room temperature. We measure the output characteristic of the rf source for different frequencies with a spectrum analyzer (Rohde & Schwarz FSL18, frequency span 1 MHz, intermediate frequency bandwidth 10 KHz, 20 averages, 101 points). In Fig. [7\(b\),](#page-10-3) we show an example of the transmission characteristics of the cables and components.

## **2. The dc-flux crosstalk**

The first step in the characterization of flux crosstalk is to relate the direct current *I* of the *z* line with the magnetic flux (dc) applied to the SQUID of the coupler [see Figs. [2\(c\)](#page-2-0) and [3\(b\)\]](#page-3-0). This is done via continuous-wave (cw) frequency spectroscopy of the neighboring qubit (which is coupled to the victim coupler) [an example is shown in Fig. [8\(a\)\]](#page-11-0). When the coupler comes close to resonance with the qubit, we observe an avoided crossing. By identifying a series of such crossings, we are able to deduce the current required to apply one flux quantum to the SQUID, as well as the dc offset current corresponding to the true zero dc-flux bias on the SQUID. In our case, one flux quantum (<sup>0</sup> = 2.067 × 10<sup>−</sup><sup>15</sup> Wb) corresponds to approximately 3 mA.

## PDF page 12

FIG. 8. The dc-flux crosstalk measurement. (a) Qubitfrequency spectroscopy versus current I applied to a neighboring tunable coupler. Detuning refers to the frequency difference between the probe tone and the qubit at I = 0. The avoidedcrossing regions are used to probe for small shifts in the coupler frequency due to qubit-coupler hybridization. The "1 flux quantum" label refers to the magnetic flux periodicity of the coupler frequency. (b) The shift in the flux  $\Phi_{\text{victim}}$  of the victim coupler versus the flux  $\Phi_{\text{source}}$  of the source coupler. Each curve in the left panel represents a narrow vertical slice of the data in (a) in the vicinity of one of the avoided crossings ( $a_0 = 0.365696$ ). For each  $\Phi_{source}$ , we have extracted  $\Phi_{victim}$  as shown in the right panel. The slope yields the dc-flux crosstalk coefficient (here,  $|\beta_{i,j}| = 0.13\%$ ). (c) Repeated qubit-frequency spectroscopy for 3 h to demonstrate the stability of the system. Here, we have fixed the probe frequency and varied the current I at the neighboring coupler. (d) A demonstration of active dc-flux compensation by subtraction of the crosstalk.

To measure dc-flux crosstalk  $\beta_{i,j}^{(dc)}$  [Eq. (2)], the victim coupler  $cp_i$  is first biased close to one such avoided crossing. In the absence of a dedicated coupler-state readout resonator, this is a sensitive region to probe  $\beta^{(dc)}$  through qubit-state readout. A small shift in the frequency of  $cp_i$ , from  $f_p$  to  $f_p'$ , can be inferred from the change in the hybridized coupler-qubit frequency  $f_p$ , imparted by the source current  $I_i$ . In an ideal condition with zero crosstalk, i.e.,  $\beta_{i,j}^{(dc)} = 0$ ,  $f_p$  is independent of the value of the current  $I_i$  applied on source  $z_i$ . Due to non-negligible crosstalk,  $f_n^{(i)}$ will shift slightly as a function of  $I_i$  and the goal is to find the new current value  $I'_i$  that restores  $f'_p$  to  $f_p$ . In practice, we fix the qubit probe frequency  $f_p$  (typically approximately 10 MHz away from the qubit bare frequency) and determine  $I'_i$  for three different dc currents  $I_i$  corresponding to source coupler  $(cp_i)$  flux bias values  $-\Phi_0$ , 0, and  $\Phi_0$  [an example is shown in Fig. 8(b)]. Then, we obtain  $\beta_{i,j}^{(dc)}$  by converting  $I'_i$  to the corresponding flux applied on  $z_i$ .

In Fig. 8(c), we demonstrate the passive stability of the dc-flux environment of a z line for 3 h. There, we have repeatedly swept the input current to the z line while maintaining the same probe frequency. From the positions of the extracted peak, we have obtained a standard deviation of the variation of the current to be 100 nA—or, equivalently,  $32 \mu \Phi_0$ —which is smaller than the minimum step in output current allowed by the source (approximately 380 nA). Furthermore, this flux variation is much smaller than the typical dc-flux crosstalk observed in our system, which is around  $500 \mu \Phi_0$  when  $1 \Phi_0$  is applied to the source z line.

We also demonstrate active dc-flux compensation on one of the victim z lines using the obtained crosstalk coefficient, as shown in Fig. 8(d). As the dc flux on the source line is varied between  $-\Phi_0$  and  $\Phi_0$  (the vertical axis is displayed in the equivalent unit of current), the range of variation in the resonance frequency (horizontal axis) drops more than tenfold (when compared to the uncompensated version, labeled as "raw" in the figure), from 7.12 MHz to 0.53 MHz. Further studies are required to understand this number and optimize the crosstalk-calibration procedure to push it below the limit allowed by the measurement setup.

#### 3. The ac-flux crosstalk

For the case of ac-flux crosstalk, interference between ac-flux signals applied to the victim z line and parasitic signals from the source z line renders the technique used for dc-flux crosstalk measurement inapplicable. Instead, we employ a modified Ramsey-pulse sequence following Ref. [38]. We first give an overview of this technique before describing the calibration and measurement steps leading up to the crosstalk data.

First, consider a qubit-coupler system  $(q_i, cp_i)$ . The original Ramsey-pulse sequence consists of two frequency-detuned  $\pi/2$  pulses on the qubit, separated by an idle time  $\Delta t$  [see Fig. 9(a)]. By measuring the  $q_i$  population as a function of  $\Delta t$ , we obtain a Ramsey fringe the oscillation frequency  $\delta \omega = \omega_i^q - \omega_{\text{drive}}$  of which corresponds precisely to the detuning between the applied pulse and the actual frequency of  $q_i$ . In the modified Ramsey-pulse sequence, an ac-flux pulse at angular frequency  $\omega_i^{(\text{ac})}$  is also applied to the coupler, via  $z_i$ , during that idle duration, as shown in Fig. 9(a). This ac pulse modulates the qubit frequency and consequently also the detuning, which makes the observed  $\delta \omega$  sensitive to the applied ac-flux pulse amplitude.

Now, we modulate the victim coupler  $cp_i$  through a source line  $z_j$  to quantify the ac-flux crosstalk  $\beta_{i,j}^{(ac)}$ . The victim coupler is biased at specific dc-flux and ac-flux bias points (angular frequency  $\omega_i^{(ac)}$ , phase  $\theta_i$ ) chosen to render it susceptible to the detection of parasitic ac-flux signals.

## PDF page 13

FIG. 9. The ac-flux crosstalk measurement. (a) The control-pulse sequence. (b) The data obtained from running the ac-flux calibration sequence for a series of ac voltages  $V_i^{\rm (ac)}$ . (c) The simulated version of the data in (b), using the measured parameters of the device for a series of  $\Phi_i^{\rm (ac)}$ . (d) Fits of the extracted frequency  $\delta\omega$  of the data in (b) to the simulation in (c), assuming a linear relation  $V^{\rm (ac)} = k(\Phi^{\rm (ac)}/\Phi_0)$ . The star symbol indicates the typical ac-flux bias point. (e) The measured  $\delta\omega$  for  $0 < \Delta\theta < 3\pi$  in the presence of source ac flux. The oscillation amplitude (the swing of  $\delta\omega$ ) is proportional to the ac-flux crosstalk  $\beta^{\rm (ac)}$  as discussed in the text.

An ac-flux signal on a source line  $z_j$ , at frequency  $\omega_j^{(\text{ac})} = \omega_i^{(\text{ac})}$ , will cause a noticeable shift in  $\delta\omega$  obtained via the modified Ramsey-pulse sequence. We measure  $\delta\omega$  for a range of phase offsets  $\Delta\theta = |\theta_j - \theta_i|$  spanning  $[0, 3\pi]$ , as shown in Fig. 9(e). The maximum swing of  $\delta\omega$  (or  $\Delta(\delta\omega)$ ) corresponds to an equivalent ac-flux shift in  $cp_i$ :  $\Delta\Phi_i^{(\text{ac})} = 2\beta_{i,j}^{(\text{ac})}\Phi_j^{(\text{ac})}$ .

In practice, we proceed with the following steps: (1) relate  $\Phi^{(ac)}$  to the ac-voltage amplitude  $V^{(ac)}$  applied by the instrument, (2) make a choice of dc- and ac-flux bias points for the victim  $cp_i$ , (3) apply a large ac-flux signal on the source  $z_j$ , and (4) run the sequence in Fig. 9(a) and relate the measured swing  $\Delta(\delta\omega)$  to  $\Delta\Phi_i^{(ac)}$  at the bias point, which in turn enables the determination of  $\beta_{i,j}^{(ac)}$ .

To relate  $V_i^{(\text{ac})}$  to  $\Phi_i^{(\text{ac})}$  for any pairs of  $z_i$  and  $cp_i$ , we run the ac-flux calibration pulse sequence in Fig. 9(a). In Fig. 9(b), we show the measured Ramsey fringes for a range of voltages  $V_i^{(\text{ac})}$ . In parallel, we run a QuTiP simulation [58,59] of this pulse sequence using the measured parameters of the qubit, the qubit drive, and the coupler zero-flux bias frequencies. This simulation leads to equivalent Ramsey fringes for a range of  $\Phi_i^{(\text{ac})}$ ; an example is shown in Fig. 9(c). Finally, the extracted frequencies of the measured and the simulated Ramsey fringes are fitted to each other by assuming a linear relation, i.e.,  $V_i^{(\text{ac})} = k_i(\Phi_i^{(\text{ac})}/\Phi_0)$ . In our setup, we typically obtain  $k_i$  in the range from 6 to 10.

The choice of dc-flux bias points is made by following the typical bias points that we use for two-qubit gate operation, which are around  $0.3\Phi_0$  [20]. The ac-flux bias point is generally chosen for maximum sensitivity to small changes in ac flux; an example is shown in Fig. 9(c). For the ac-flux frequency, we set  $\omega^{(ac)}/2\pi=200$  MHz, which is a typical frequency for parametric modulation in this system.

Next, we assume that the measured ac-flux crosstalk is small, which allows us to linearize the region around the bias point, i.e.,  $\Delta\Phi_i^{(\mathrm{ac})} \approx \gamma_i^{(\mathrm{ac})} \Delta(\delta\omega)$ . The slope  $\gamma_i^{(\mathrm{ac})}$  is extracted using the nearest data points and it allows us to infer  $\Delta\Phi_i^{(\mathrm{ac})}$  from the measured  $\Delta(\delta\omega)$ :  $\beta_{i,j}^{(\mathrm{ac})} = \gamma_i^{(\mathrm{ac})} \Delta(\delta\omega)/2\Phi_i^{(\mathrm{ac})}$ .

### APPENDIX D: TARGET FREQUENCIES

The allocation of qubit frequencies in this processor follows the two-frequency subgroup strategy as described in Ref. [34] and in Sec. II. The readout-resonator frequencies are arranged to maintain qubit-resonator detunings that are above 2 GHz throughout the processor. All couplers are identical and the target frequency at the zero-flux bias is 7.9 GHz. In Fig. 10, we show the target qubit frequencies ( $f_{01}$ ), the anharmonicity ( $\eta$ ), and the readout-resonator frequencies ( $f_r$ ).

## APPENDIX E: BASIC QPU PARAMETERS

In Table I, we list the range of measured or inferred qubit frequencies  $(f_{01})$ , anharmonicities  $(\eta)$ , readout-resonator frequencies  $(f_r)$ , coupler frequencies at zero flux bias  $(f_{c0})$ , and single-qubit coherences  $(T_1 \text{ and } T_2^*)$ . The frequencies of the qubits and couplers are approximately 1 GHz lower than the design values due to an off-target Josephson-junction fabrication result.

### APPENDIX F: COMPLETE DATA SETS

In Fig. 11, we show the complete data sets of measured xy and dc-flux crosstalk from both processors. Due to the different numbers of pairs present in each data set, we plot

## PDF page 14

FIG. 10. The target qubit frequencies ( $f_{01}$ , upper values) and readout-resonator frequencies ( $f_r$ , lower values). The alternating background color illustrates the two-frequency subgroup strategy with two distinct anharmonicity values ( $\eta$ ).

a normalized histogram indicated by the normalized count on the vertical axis.

# APPENDIX G: EXPECTED EFFECT OF THE TUNNEL

In this appendix, we are interested in the expected reduction of the coupling between a source xy line and a victim qubit due to the tunnel structure. To do so, we have simulated the coupling-capacitance values between two xy lines on the C-chip with two qubits on the Q-chip. In Fig. 12(a), we show a simplified version of the simulation model. The major differences with the actual processor layout are the qubit-qubit distance (which is 2 mm, in contrast to 1.5 mm

TABLE I. The range of the measured parameters of the two QPUs examined in this work. QPU 1 has the tunnels; QPU 2 does not have any tunnels.

| Parameters     | QPU 1          | QPU 2          |
|----------------|----------------|----------------|
| $f_{01}$ (GHz) | [3.262, 4.077] | [3.166, 3.982] |
| η (MHz)        | [-249, -191]   | [-245, -193]   |
| $f_r$ (GHz)    | [6.317, 6.987] | [6.335, 7.059] |
| $f_{c0}$ (GHz) | [6.476, 7.049] | [6.470, 7.329] |
| $T_1$ (µs)     | [76, 143]      | [30, 80]       |
| $T_2^*$ (µs)   | [19, 83]       | [16, 42]       |

FIG. 11. The complete data sets on the aggregate performance of xy crosstalk  $\Lambda^{(xy)}$  and dc-flux crosstalk  $\beta^{(\text{dc})}$ . (a) The histogram of the on-resonant xy crosstalk  $\Lambda_{i,j}$  for a flip-chip module with bare transmission lines (labeled "bare", 210 pairs,  $\bar{\Lambda}_{\text{bare}} = (39.8 \pm 4.0)$  dB), and another flip-chip module with the majority of the transmission lines covered in tunnel structures (labeled "+tunnel", 72 pairs,  $\bar{\Lambda}_{(\text{+tunnel})} = (37.4 \pm 3.9)$  dB). (b) The histogram of the dc-flux crosstalk  $\beta^{(\text{dc})}$  (bare: 462 pairs, tunnel: 274 pairs). The data indicated as group 2 are associated with pairs the z lines of which are nearest neighbor.

in this model) and the closest distance between a source xy line with a victim qubit (which is 500  $\mu$ m, in contrast to 375  $\mu$ m in this model). The tunnel structure is modeled as a metal enclosure with a sinusoidal roof profile (3  $\mu$ m height, 50  $\mu$ m width) and no opening along both sides of the structure, which is different from the actual structure, where there are periodically spaced openings along the tunnel to allow access to the cleaning solvent [see Fig. 2(d)].

**(b)** Simulated coupling capacitance (× 10<sup>-6</sup> fF)

| With tunnel |       |       | Without tunnel |       |       |
|-------------|-------|-------|----------------|-------|-------|
|             | $q_1$ | $q_2$ |                | $q_1$ | $q_2$ |
| $xy_3$      | 530   | 18    | $xy_3$         | 530   | 18    |
| $xy_4$      | 2     | 61    | $xy_4$         | 14    | 403   |

FIG. 12. Simulation of the effect of the tunnel structure in reducing the direct xy-qubit coupling capacitance. (a) A simplified model of the simulation: two qubit structures ( $q_1$  and  $q_2$ ) on the Q-chip and two xy lines ( $xy_3$  and  $xy_4$ ) on the C-chip. The ground planes on both the C-chip and the Q-chip and the coupler structure on the Q-chip are not shown. (b) The extracted coupling-capacitance values between two models: one with a tunnel structure on  $xy_4$  and the other without a tunnel structure.

## PDF page 15

However, these differences should not, in principle, matter for the purpose of this simulation.

We have used ANSYS MAXWELL [36] to obtain the capacitance matrix. The table in Fig. 12(b) shows the coupling-capacitance values in two situations: with and without the tunnel structure on  $xy_4$ . First, the coupling capacitance is smaller for larger separation: compare  $C(xy_3, q_1)$  and  $C(xy_3, q_2)$  in both cases. As a reference, the coupling capacitance between a qubit and its own xy line, e.g.,  $C(xy_1, q_1)$ , is at least 100 times larger than  $C(xy_3, q_1)$ . Second, by comparing the coupling-capacitance values between  $xy_4$  and either  $q_1$  or  $q_2$  before and after adding the tunnel structure, we can see that it does indeed weaken the direct coupling between the xy line and the qubits. Note that  $C(xy_4, q_2) < C(xy_3, q_1)$ , despite both of them being identical in length and equally spaced from the respective qubits; this is because the CPW geometry of  $xy_4$  is slightly narrower to retain  $50-\Omega$  characteristic impedance after adding the tunnel.

Therefore, we have shown that the tunnel structure can indeed reduce the direct capacitive coupling between an xy line located on the C-chip and a qubit located on the Q-chip, at least for the simplified model discussed in this appendix. Given that the tunnel structure modifies the radiation profile of the xy line, it is possible that other xy-crosstalk mechanisms may be impacted as well and future work should investigate this in more detail.

# APPENDIX H: CROSSTALK DUE TO DIRECT xy-QUBIT CAPACITIVE INTERACTION

In this appendix, we are interested in the expected crosstalk level due to the direct capacitive interaction between a victim qubit with any other source xy line (excluding its own xy line). The model includes both the full-sized C-chip and the Q-chip, without the wire bonds and the PCB packaging around it. To simplify the model, we retain the 25 transmon objects on the Q-chip and replace the coupler structures with a ground plane. On the C-chip, we only retain the 15 xy lines controlling the three bottom rows of the qubits  $(q_{11} \text{ to } q_{25})$ . The rest of the xy lines and z lines are replaced with a ground plane. The model retains the full bump structures connecting the two chips. No tunnels are included in the model.

We have employed ANSYS MAXWELL [36] to simulate the capacitance matrix of such a problem. The relation between the capacitance values and the Rabi frequency  $(\Omega_R)$  is obtained via the relation

$$\int_{0}^{T_{\pi}} \Omega_{R}(t)dt = \pi, \tag{H1}$$

$$2\sqrt{\kappa}bA_0T_{\pi} = \pi,\tag{H2}$$

where  $\kappa$  is the photon loss rate via the xy line, b is the pulse-shape-dependent constant obtained from the

integration (b=1 for a square pulse,  $b=2/\pi$  for a sinusoidal-shape pulse),  $A_0$  is the pulse amplitude, and  $T_{\pi}$  is the characteristic pulse duration to create a  $\pi$  pulse. The expression for  $\kappa$  is

$$\kappa = Z_{\text{tml}} \frac{C_{\kappa}^2 \omega_q^2}{C_q},\tag{H3}$$

where  $Z_{\rm tml}$  is the xy-line characteristic impedance (50  $\Omega$  in our case),  $C_{\kappa}$  is the coupling capacitance between the xy line and the qubit,  $\omega_q$  is the qubit angular frequency, and  $C_q$  is the qubit capacitance. This treatment closely follows the derivation described in Ref. [60] (specifically, Secs. VIII.A, IV.F, and IV.B, and Appendix C in Ref. [60]). Reexpressing the xy-crosstalk definition in terms of the simulated capacitance values, we obtain

$$\Lambda_{\text{dir}}^{(xy)} := \Lambda_{i,j} = 10 \times \log_{10} \left( \frac{\Omega_{i,j}}{\Omega_{j,j}} \right)^2$$
 (H4)

$$= 20 \times \log_{10} \left( \frac{\omega_i C_{i,j}}{\omega_j C_{j,j}} \sqrt{\frac{C_j}{C_i}} \right), \quad (H5)$$

where  $C_{i,j}$  is the coupling capacitance between the victim qubit i and the source xy line j and  $\{C_i, C_j\}$  are the capacitances of qubits i and j.

In Fig. 13(a), we show a histogram of the predicted crosstalk  $\Lambda_{\rm dir}^{(xy)}$  due to direct xy-qubit capacitive interaction. The average value is -95 dB, with the worst at -49 dB, which are much lower values than those measured in our processor. This simulation shows that the direct capacitive interaction between a victim qubit and any other source xy line cannot be the major contributor to the xy-crosstalk level measured in our processors, at least within the simplified model used here.

FIG. 13. Simulation of the xy crosstalk  $\Lambda_{\rm dir}^{(xy)}$  between victim qubits and other source xy lines due to direct xy-qubit interaction. (a) The histogram of  $\Lambda_{\rm dir}^{(xy)}$  with an average and standard deviation of  $(-96 \pm 26)$  dB. (b)  $\Lambda_{\rm dir}^{(xy)}$  versus  $d^{(xy)}$ , which is the distance between the victim qubits and the target qubits of the source xy lines. The parameters m and  $\Lambda_0$  are from the linear fit to the average of  $\Lambda_{\rm dir}^{(xy)}$  versus  $d^{(xy)}$ .

## PDF page 16

We have plotted the distance-dependent xy crosstalk (due to the direct xy-qubit interaction) in Fig. 13(b), similarly to Fig. 4. The data exhibit a relatively large spread of  $\Lambda_{\rm dir}^{(xy)}$  versus  $d_{i,j}$  (the distance between the victim qubit i and the target qubit of the source xy line j). We have performed an empirical linear fit of the average crosstalk  $\bar{\Lambda}_{\rm dir}^{(xy)}$  versus  $d_{i,j}$  and obtained the distance-scaling parameters  $m_{xy} = -8.8$  dB/mm and  $\Lambda_0 = -57$  dB, well below the values needed to bring the total single-qubit gate error below the 0.1% threshold for 100-qubit processors ( $m_{xy} = -2.0$  dB/mm and  $\Lambda_0 = -50$  dB; see Sec. IV and Appendix K).

As discussed previously, the model used in this simulation does not include the wire bonds and the PCB signal traces. While they are positioned further away from the qubits, they are also much larger than the rest of the signal lines in the processor. Including them in the model is computationally expensive and future investigations should look into the strength of the interaction between the combined wire bonds and the PCB system with the qubits.

# APPENDIX I: CROSSTALK BETWEEN SIGNAL LINES

In this appendix, we are interested in the expected rf-crosstalk level between neighboring signal lines. To do so, we have performed electromagnetic simulation of a small-scale model shown in Fig. 14(a). The model includes a representative section of the PCB signal traces, wire bonds, and a section of the chips. No tunnel structure is included in this simulation.

In Fig. 14(c), we show a simplified version of the model. We model five neighboring signal lines with input ports located at the PCB side (labeled "reference plane" or "ref") and consider signal output ports at various locations. The latter is to illustrate the relative contribution from various parts of the signal lines. The quoted crosstalk levels  $S(j,i) = V_{\text{out}}(j)/V_{\text{in}}(i)$ , expressed in decibels, are the average between the highest and lowest values obtained for the considered pairs and the uncertainty is half of that range. The various locations correspond to the boundary between the PCB and the C-chip (location A, no wire bonds and chips in the model), after the launch pad (location B, with wire bonds and C-chip, no Q-chip in the model), just before the Q-chip (location C, but no Q-chip is included in the model), and within the flip-chip environment (location *D*). The simulations have employed ANSYS HFSS [36] (driven modal, maximum  $\Delta S$ : 0.005, 4 GHz frequency, and the outer boundary of the model set by default to the Perfect E boundary condition). Due to the limited computational resources, we have only included a certain section of the PCB ( $x_A = 5.0 \text{ mm}$ ) and the Q-chip ( $x_D = 2.0$ ). When simulating the results for intermediate locations, e.g., location A, we have removed the rest of the signals lines (from B all the way to D) from the model.

FIG. 14. Simulation of the crosstalk between signal lines. (a) The actual simulation model, showing a part of the PCB (with its vias), the wire bonds, and the C-chip with its signal lines. The Qchip is not shown but is included in the model when required. Five signal lines are included in the simulation. (b) A photograph of the actual packaging and the chips (the wire bonds are not shown). (c) A simplified model of (a) showing an input port  $[V_{\rm in}(i)]$  and two output ports  $[V_{\rm in}(j)]$  (drawing not to scale). The table summarizes the simulated S parameter S(j,i) (in decibels) between the input port i at the reference plane and the output port j at one of the locations (A, B, C, and D). The model assumes  $x_A = 5.0 \text{ mm}, x_B = 500 \text{ }\mu\text{m}, x_C = 650 \text{ }\mu\text{m}, \text{ and } x_D = 2 \text{ mm}.$  (d) A model that is similar to (c) but with the signal lines within the flip-chip environment spaced by 100 µm to replicate the actual separation between lines in our processors. Here,  $x_A = 5.0$  mm,  $x_B = 500 \,\mu\text{m}$ ,  $x_C = 650 \,\mu\text{m}$ , and  $x_D = 5 \,\text{mm}$  (drawing is not to

First of all, we see that up to the edge of the PCB [location A, row "Ref-A" in Fig. 14(c)], nearest-neighbor line crosstalk  $(j = i \pm 1)$  is at the level of -56 dB, with rapidly

## PDF page 17

decreasing crosstalk down to the level of -90 dB for third-next-nearest-neighbor lines ( $j = i \pm 4$ ). However, after including the wire bonds and the launch-pad area (row "Ref-B"), the crosstalk level worsens substantially, to the level of -40 dB for nearest neighbors and -58 dB for third-next-nearest neighbors. The subsequent addition of signal lines at the chip level ("Ref-C", "Ref-D") does not substantially worsen the crosstalk, even though we have only simulated a 2-mm portion of the signal lines within the flip-chip environment. The relatively small change in the crosstalk level for the transmission lines within the chip can be explained by the much narrower transmission lines used at the chip area (approximately  $10 \mu m$  excluding the launch-pad structure) compared to the line-to-line separation, which is  $600 \mu m$ .

In Fig. 14(d), we have modified the model for the neighboring signal lines within the flip-chip environment to be spaced by 100  $\mu$ m, corresponding to the actual separation in our processor layout. To account for the additional space required to bend the signal lines and bring them closer to each other, we have extended  $x_D$  to 5 mm. We also note that  $x_D$  is close to half the width of the Q-chip (12  $\mu$ m). The simulation results show a crosstalk level that is not substantially worse than those obtained in Fig. 14(c).

In our processor design, there is no pair of qubits controlled by xy lines that are nearest neighbors, as we always need at least a signal line for flux control of the tunable coupler in between two qubits. For any pair of nearest-neighbor qubits, they are controlled by xy lines that are at least next-nearest neighbors. Typically, the corresponding qubits are located along the same row. In the index notation introduced in Fig. 14, they correspond to pairs of i,j with  $j = i \pm 2$ . For next-nearest qubits, they are controlled by xy lines that are at least in third-next-nearest neighbor configuration, i.e.,  $j = i \pm 4$ .

The average *xy*-crosstalk level measured for pairs of qubits that are controlled by next-nearest neighbor and third-next-nearest-neighbor *xy* lines are -36.2 dB -38.5 dB, respectively. Simulation results from Fig. 14(d) (-47 dB for next-nearest, -58 dB for third-nearest) suggest that the crosstalk between signal lines is not the dominant source of crosstalk, at least within the simplified model considered here.

The accuracy of this result is limited by the model, in which we consider only five signal lines on a small section of the combined PCB and QPU system. In addition, the actual layout of neighboring signal lines is not quite as simple as illustrated in Figs. 14(c) and 14(d). However, these simplified models are already very challenging to simulate, given the available computational resources and the large range of physical sizes that need to be taken into account (from a few tens of micrometers up to a few tens of millimeters). It is possible that the overall crosstalk level may change when we consider an area that is larger than the one considered here. It is also unclear if the convergence

criteria used are adequate to yield results that are representative of the actual processor. In the future, it will be useful to test the accuracy of such simulations on smaller-scale devices before employing them to predict the performance of much larger devices. It will be also interesting to look for alternative modeling techniques that can yield sufficiently reliable results with a much lower computational cost.

# APPENDIX J: EMPIRICAL LINEAR FIT OF $\bar{\Lambda}^{(xy)}$ VERSUS $d^{(xy)}$

To further illustrate the trend within the data of average xy crosstalk  $\bar{\Lambda}^{(xy)}$  versus the qubit-qubit distance  $d^{(xy)}$ , we have performed an empirical linear fit of the form  $\bar{\Lambda}^{(xy)} = m_{xy}d^{(xy)} + \Lambda_0$ . The fit is performed by assigning equal weight to each data point. The results are shown in Fig. 15. The associated error bars of  $m_{xy}$  and  $\Lambda_0$  are the fit uncertainties. The analyses yield approximately similar  $m_{xy}$  and  $\Lambda_0$  for both processors.

### APPENDIX K: SINGLE-OUBIT GATE ERROR

We have introduced the distance-scaling parameters, denoted as  $m_{xy}$  and  $\Lambda_0$ , which are obtained from an empirical linear fit to the data  $\bar{\Lambda}^{(xy)}$  versus  $d^{(xy)}$ . These parameters can be used as a starting point in estimating the impact of xy crosstalk on the total gate fidelity during parallel applications of single-qubit gates. From the hardware-architecture perspective, these parameters should be as low as possible. We find approximately  $m_{xy} = -1.1$  dB/mm and  $\Lambda_0 = -33.9$  dB.

Clearly, the actual error depends on the pulse sequences (implementing quantum gates) that are being applied to all of the qubits. Here, we consider a specific scenario to obtain a concrete estimate of the effect on gate fidelity: a situation in which single-qubit X gates are simultaneously applied on all qubits. The qubit frequencies are allocated

FIG. 15. The data of the xy crosstalk  $\Lambda^{(xy)}$  versus the qubit-qubit distance  $d^{(xy)}$  with an empirical log-linear fit (i.e., empirical here means that the fit expression is not based on a physical model or numerical simulation of  $\Lambda^{(xy)}$ ).

## PDF page 18

FIG. 16. The predicted total single-qubit gate error in a square lattice of  $N \times N$  qubits (the nearest-neighbor separation is 2 mm). The gate error is assumed to only come from the off-resonant excitation due to adversary single-qubit signals applied on other xy lines. The solid line represents a scenario described in the text and the dashed line assumes additional phase related to propagation from the location of the source line to the victim qubit.

according to the two-frequency subgroup strategy shown in Fig. 2(f) and specified in Appendix D. Here, the gate error is due to parasitic excitation (both off-resonant and on-resonant) of the victim qubit from adversary X gates applied to all other source xy lines. These signals are assumed to be on resonant with the qubits that they are meant to excite. The details of the simulation are described in Appendix L.

The results are shown in Fig. 16. The simulation yielding the solid lines assumes no additional phase offset between the signal and the adversary signals. In this case, the total gate error begins to plateau (up to the considered processor sizes) as we begin to consider processors with hundreds of qubits, which is attributed to weakening crosstalk due to larger values of  $d^{(xy)}$ . This assumption of no phase offset is not a realistic one but we believe that it provides an easily understandable setting and a relatively stringent criterion to give us an idea of the total gate error. If we could improve the crosstalk and its scaling behavior to  $m_{xy} = -1.5$  dB/mm and  $\Lambda_0 = -45$  dB, for processors with roughly 1000 qubits, we would find a projected total single-qubit gate fidelity in excess of 99.7%, and for even better crosstalk,  $m_{xy} = -2.0$  dB/mm and  $\Lambda_0 = -50$  dB, we would find 99.97%.

We have also simulated the total single-qubit gate error (dashed lines in Fig. 16) by assuming additional phase offset due to signal propagation between the positions of the source xy line (approximated as the position of the target qubit of the source xy line) and the victim qubit. The assumption makes a negligible difference for

small qubit arrays due to the small  $d^{(xy)}$ . The difference is more pronounced for larger qubit arrays, as there are more contributions from victim-source pairs with larger  $d^{(xy)}$ . In such a setting, the total gate fidelities for processors beyond 1000 qubits (33 × 33) increase to 99.95% for  $m_{xy} = -1.5$  dB/mm,  $\Lambda_0 = -45$  dB and 99.99% for  $m_{xy} = -2.0$  dB/mm,  $\Lambda_0 = -50$  dB.

We emphasize that this is a very simplified model; we have no quantitative model predicting a log-linear behavior, nor one predicting that a similar trend would continue beyond the range of  $d_{xy}$  examined in this work. However, we believe that these parameters can be useful as a set of quantitative metrics to help guide near-term scaling-up effort and to guide hardware road maps.

#### APPENDIX L: NUMERICAL SIMULATIONS

In this appendix, we briefly describe the models used to numerically simulate the ac-flux calibration curve and the total single-qubit gate error due to *xy* crosstalk.

#### 1. The ac-flux calibration curve

In this simulation, we focus on a system comprising a fixed-frequency qubit coupled to a frequency-tunable coupler. The goal is to extract the Ramsey-fringe frequency of a qubit when the coupler is being subjected to specific dc-flux bias and ac-flux modulation.

The system Hamiltonian  $\mathcal{H}_{\text{sys}}$  is

$$\mathcal{H}_{\text{sys}} = \mathcal{H}_a + \mathcal{H}_c + \mathcal{H}_{\text{int}}, \tag{L1}$$

where  $\mathcal{H}_q$ ,  $\mathcal{H}_c$ , and  $\mathcal{H}_{int}$  represent the Hamiltonian of the qubit, the coupler, and their interaction, respectively. We employ a doubly rotating frame at the qubit-drive angular frequency  $\omega^{(xy)}$  and the coupler angular frequency at its dc-flux bias,  $\omega_c(\Phi = \Phi^{(dc)})$ .

The qubit Hamiltonian is as follows:

$$\mathcal{H}_a/\hbar = -\Delta_a(\sigma_z \otimes \mathbb{I}) + \Omega^{(xy)}(t)(\sigma_x \otimes \mathbb{I}), \qquad (L2)$$

where  $\omega_q$  is the qubit angular frequency,  $\Delta_q = \omega^{(xy)} - \omega_q$ ,  $\Omega^{(xy)}(t)$  is the time-dependent qubit-drive signal appropriately expressed in the angular-frequency unit, and  $\sigma_{x/z}$  are the Pauli matrices.

The coupler Hamiltonian is

$$\mathcal{H}_c/\hbar = -\Delta_c(t)(\mathbb{I} \otimes \sigma_z), \tag{L3}$$

where  $\Delta_c(t) = \omega_c(\Phi^{(\mathrm{dc})}) - \omega_c(\Phi^{(\mathrm{dc})} + \Phi^{(\mathrm{ac})}(t))$  and  $\omega_c(\Phi) = \omega_{c0}\sqrt{|\cos(\pi\Phi/\Phi_0)|}$ . The parameters  $\omega_{c0}$  and  $\Phi_0$  are the coupler angular frequency at zero-flux bias and the magnetic flux quantum, respectively.

## PDF page 19

The interaction Hamiltonian is

$$\mathcal{H}_{\text{int}}/\hbar = ge^{i(\omega^{(xy)} - \omega_c(\Phi^{(\text{dc})}))t}(\sigma^+ \otimes \sigma^-) + \text{H.c.}, \quad (\text{L4})$$

where g is the coupler-qubit coupling strength expressed in the angular-frequency unit. Here, we make use of the rotating-wave approximation to neglect the counter-rotating terms.

We simulate the state of the combined system (both the qubit and the coupler are initially in the ground state) evolving under  $\mathcal{H}_{\text{sys}}$  with the pulse sequence shown in Fig. 9(a). The solver is QUTIP.SESOLVE [58,59] and the simulation time step is 1 ns. From the expectation value of  $\sigma_z \otimes \mathbb{I}$  at the end of the pulse sequence, we reconstruct the expected Ramsey fringes. An example of the simulation result is shown in Fig. 9(c).

## 2. Single-qubit error

In this simulation, we consider a system comprising a square array of qubits (total  $N \times N$  qubits), each of them being driven by an on-resonant X gate. Due to nonzero xy crosstalk, each qubit also experiences parasitic qubit driving from the rest of the qubits.

We assume distance-dependent xy-crosstalk behavior that follows the empirical linear model described in Appendix J. We focus on a victim qubit at the center of this array (we assume that N is an odd number). Our goal is to calculate the resultant single-qubit error on this victim qubit due to the parasitic drives.

The Hamiltonian of interest considers a single qubit that is being driven by microwave signals. We ignore the evolution of other qubits and group the parasitic drives into the drive term; specifically,

$$\mathcal{H}_{\text{sys}} = \mathcal{H}_i + \mathcal{H}_{i,j}. \tag{L5}$$

We employ a reference frame rotating with the drive frequency of the victim qubit.

The Hamiltonian  $\mathcal{H}_i$  is

$$\mathcal{H}_i/\hbar = -\Delta_i \sigma_z + \Omega_{i,i}(t)\sigma_x, \tag{L6}$$

where  $\Delta_i = \omega_i^{(xy)} - \omega_i$  is the qubit-drive detuning, assumed to be zero in this simulation. The parameter  $\Omega_{i,i}(t)$  is the time-dependent microwave-drive-pulse amplitude applied to the victim qubit by its own xy line and is appropriately expressed in the angular-frequency unit. The symbols  $\sigma_{x/y/z}$  are the Pauli matrices.

The Hamiltonian corresponding to the parasitic drives from other qubits is

$$\mathcal{H}_{i,j}/\hbar = \sum_{j \neq i} \Omega_{i,j}(t) (\sigma_x \cos(\phi_j(t)) + \sigma_y \sin(\phi_j(t)), \text{ (L7)}$$

where  $\phi_j(t) = \delta_{i,j}t + \phi_{i,j}$ . The parameters  $\delta_{i,j}$  and  $\phi_{i,j}$  are the detuning  $(\omega_j - \omega_i)$  and the additional phase, respectively. For simplicity, each qubit drive is assumed to

produce the same Rabi angular frequency to its own qubit. Thus  $\Omega_{i,i}(t) = \Omega^{(xy)}(t)$  for any *i*. The parasitic Rabi amplitude  $\Omega_{i,i}$  is

$$\Omega_{i,j}(t) = 10^{\Lambda_{i,j}/20} \Omega^{(xy)}(t),$$
 (L8)

where  $\Lambda_{i,j} = m_{xy}d_{i,j} + \Lambda_0$  and  $d_{i,j}$  is the distance between  $q_i$  and  $q_j$ . The phase  $\phi_{i,j}$  is the phase related to crosstalk between the source xy line  $xy_j$  and the victim qubit  $q_i$ . In Fig. 16, we have simulated two specific cases:  $\phi_{i,j} = 0$  (solid line), and  $\phi_{i,j} = (\omega_j/c)d_{i,j}$  (dashed line) corresponding to the phase delay due to signal propagation from the location of the target qubit of the source xy line to the location of the victim qubit, through vacuum.

We employ the QUTIP.SESOLVE solver [58,59], with a simulation time step of 0.125 ns. From the expectation value of  $\sigma_z$ , we extract the probability  $P_g$  of the qubit being in the ground state at the end of the pulse sequence. We repeat this simulation for a victim qubit with the eight different frequencies in Appendix D, and we average the probabilities. This is the single-qubit gate error  $(1 - F_{1Q})$  that is plotted on the vertical axis of Fig. 16.

- [1] Google Quantum AI, Exponential suppression of bit or phase errors with cyclic error correction, Nature **595**, 383 (2021).
- [2] Y. Kim, A. Eddins, S. Anand, K. X. Wei, E. Van Den Berg, S. Rosenblatt, H. Nayfeh, Y. Wu, M. Zaletel, K. Temme, and A. Kandala, Evidence for the utility of quantum computing before fault tolerance, Nature 618, 500 (2023).
- [3] C. Ryan-Anderson, J. G. Bohnet, K. Lee, D. Gresh, A. Hankin, J. P. Gaebler, D. Francois, A. Chernoguzov, D. Lucchetti, N. C. Brown, T. M. Gatterman, S. K. Halit, K. Gilmore, J. A. Gerber, B. Neyenhuis, D. Hayes, and R. P. Stutz, Realization of real-time fault-tolerant quantum error correction, Phys. Rev. X 11, 041058 (2021).
- [4] D. Bluvstein, *et al.*, Logical quantum processor based on reconfigurable atom arrays, Nature **626**, 58 (2023).
- [5] X. Dai, D. M. Tennant, R. Trappen, A. J. Martinez, D. Melanson, M. A. Yurtalan, Y. Tang, S. Novikov, J. A. Grover, S. M. Disseler, J. I. Basham, R. Das, D. K. Kim, A. J. Melville, B. M. Niedzielski, S. J. Weber, J. L. Yoder, D. A. Lidar, and A. Lupascu, Calibration of flux crosstalk in large-scale flux-tunable superconducting quantum circuits, PRX Quantum 2, 040313 (2021).
- [6] Y. Sung, L. Ding, J. Braumüller, A. Vepsäläinen, B. Kannan, M. Kjaergaard, A. Greene, G. O. Samach, C. McNally, D. Kim, A. Melville, B. M. Niedzielski, M. E. Schwartz, J. L. Yoder, T. P. Orlando, S. Gustavsson, and W. D. Oliver, Realization of high-fidelity CZ and ZZ-free iSWAP gates with a tunable coupler, Phys. Rev. X 11, 021058 (2021).
- [7] W. Nuerbolati, Z. Han, J. Chu, Y. Zhou, X. Tan, Y. Yu, S. Liu, and F. Yan, Canceling microwave crosstalk with fixed-frequency qubits, Appl. Phys. Lett. **120**, 174001 (2022).

## PDF page 20

- [8] C. N. Barrett, A. H. Karamlou, S. E. Muschinske, I. T. Rosen, J. Braumüller, R. Das, D. K. Kim, B. M. Niedzielski, M. Schuldt, K. Serniak, M. E. Schwartz, J. L. Yoder, T. P. Orlando, S. Gustavsson, J. A. Grover, and W. D. Oliver, Learning-based calibration of flux crosstalk in transmon qubit arrays, [Phys. Rev. Appl.](https://doi.org/10.1103/PhysRevApplied.20.024070) **20**, 024070 (2023).
- [9] X. Zhang, E. Kim, D. K. Mark, S. Choi, and O. Painter, A superconducting quantum simulator based on a photonicbandgap metamaterial, Science **379**[, 278 \(2023\).](https://doi.org/10.1126/science.ade7651)
- [10] X. Dai, R. Trappen, R. Yang, S. M. Disseler, J. I. Basham, J. Gibson, A. J. Melville, B. M. Niedzielski, R. Das, D. K. Kim, J. L. Yoder, S. J. Weber, C. F. Hirjibehedin, D. A. Lidar, and A. Lupascu, Optimizing for periodicity: A model-independent approach to flux crosstalk calibra[tion for superconducting circuits,](https://doi.org/10.1088/2058-9565/ad1ecf) Quantum Sci. Technol. **9**, 025007 (2024).
- [11] S. Krinner, N. Lacroix, A. Remm, A. Di Paolo, E. Genois, C. Leroux, C. Hellings, S. Lazar, F. Swiadek, J. Herrmann, G. J. Norris, C. K. Andersen, M. Müller, A. Blais, C. Eichler, and A. Wallraff, Realizing repeated quantum error [correction in a distance-three surface code,](https://doi.org/10.1038/s41586-022-04566-8) Nature **605**, 669 (2022).
- [12] P. A. Spring, S. Cao, T. Tsunoda, G. Campanaro, S. Fasciati, J. Wills, M. Bakr, V. Chidambaram, B. Shteynas, L. Carpenter, P. Gow, J. Gates, B. Vlastakis, and P. J. Leek, High coherence and low cross-talk in a tileable 3D integrated [superconducting circuit architecture,](https://doi.org/10.1126/sciadv.abl6698) Sci. Adv. **8**, eabl6698 (2022).
- [13] Y. Wang, S. Crain, C. Fang, B. Zhang, S. Huang, Q. Liang, P. H. Leung, K. R. Brown, and J. Kim, High-fidelity twoqubit gates using a microelectromechanical-system-based [beam steering system for individual qubit addressing,](https://doi.org/10.1103/PhysRevLett.125.150505) Phys. Rev. Lett. **125**, 150505 (2020).
- [14] T. Xia, M. Lichtman, K. Maller, A. W. Carr, M. J. Piotrowicz, L. Isenhower, and M. Saffman, Randomized benchmarking of single-qubit gates in a 2D array of neutral-atom qubits, Phys. Rev. Lett. **114**[, 100503 \(2015\).](https://doi.org/10.1103/PhysRevLett.114.100503)
- [15] W. I. L. Lawrie, M. Rimbach-Russ, F. V. Riggelen, N. W. Hendrickx, S. L. D. Snoo, A. Sammak, G. Scappucci, J. Helsen, and M. Veldhorst, Simultaneous single-qubit driving of semiconductor spin qubits at the fault-tolerant threshold, [Nat. Commun.](https://doi.org/10.1038/s41467-023-39334-3) **14**, 3617 (2023).
- [16] J. M. Martinis, Qubit metrology for building a fault-tolerant quantum computer, [npj Quantum Inf.](https://doi.org/10.1038/npjqi.2015.5) **1**, 15005 (2015).
- [17] D. Rosenberg, D. Kim, R. Das, D. Yost, S. Gustavsson, D. Hover, P. Krantz, A. Melville, L. Racz, G. O. Samach, S. J. Weber, F. Yan, J. L. Yoder, A. J. Kerman, and W. D. Oliver, [3D integrated superconducting qubits,](https://doi.org/10.1038/s41534-017-0044-0) npj Quantum Inf. **3**, 42 (2017).
- [18] B. Foxen, *et al.*, Qubit compatible superconducting interconnects, [Quantum Sci. Technol.](https://doi.org/10.1088/2058-9565/aa94fc) **3**, 014005 (2018).
- [19] A. Gold, J. P. Paquette, A. Stockklauser, M. J. Reagor, M. S. Alam, A. Bestwick, N. Didier, A. Nersisyan, F. Oruc, A. Razavi, B. Scharmann, E. A. Sete, B. Sur, D. Venturelli, C. J. Winkleblack, F. Wudarski, M. Harburn, and C. Rigetti, Entanglement across separate silicon dies in a [modular superconducting qubit device,](https://doi.org/10.1038/s41534-021-00484-1) npj Quantum Inf. **7**, 142 (2021).
- [20] S. Kosen, *et al.*, Building blocks of a flip-chip integrated [superconducting quantum processor,](https://doi.org/10.1088/2058-9565/ac734b) Quantum Sci. Technol. **7**, 035018 (2022).

- [21] J. Koch, T. M. Yu, J. Gambetta, A. A. Houck, D. I. Schuster, J. Majer, A. Blais, M. H. Devoret, S. M. Girvin, and R. J. Schoelkopf, Charge-insensitive qubit design derived [from the Cooper pair box,](https://doi.org/10.1103/PhysRevA.76.042319) Phys. Rev. A **76**, 042319 (2007).
- [22] J. A. Schreier, A. A. Houck, J. Koch, D. I. Schuster, B. R. Johnson, J. M. Chow, J. M. Gambetta, J. Majer, L. Frunzio, M. H. Devoret, S. M. Girvin, and R. J. Schoelkopf, Suppressing charge noise decoherence in superconducting charge qubits, Phys. Rev. B **77**[, 180502\(R\) \(2008\).](https://doi.org/10.1103/PhysRevB.77.180502)
- [23] R. Barends, J. Kelly, A. Megrant, D. Sank, E. Jeffrey, Y. Chen, Y. Yin, B. Chiaro, J. Mutus, C. Neill, P. O'Malley, P. Roushan, J. Wenner, T. C. White, A. N. Cleland, and J. M. Martinis, Coherent Josephson qubit suitable for scalable [quantum integrated circuits,](https://doi.org/10.1103/PhysRevLett.111.080502) Phys. Rev. Lett. **111**, 080502 (2013).
- [24] D. C. McKay, S. Filipp, A. Mezzacapo, E. Magesan, J. M. Chow, and J. M. Gambetta, Universal gate for fixed[frequency qubits via a tunable bus,](https://doi.org/10.1103/PhysRevApplied.6.064007) Phys. Rev. Appl. **6**, 064007 (2016).
- [25] Z. Chen, A. Megrant, J. Kelly, R. Barends, J. Bochmann, Y. Chen, B. Chiaro, A. Dunsworth, E. Jeffrey, J. Y. Mutus, P. J. J. O'Malley, C. Neill, P. Roushan, D. Sank, A. Vainsencher, J. Wenner, T. C. White, A. N. Cleland, and J. M. Martinis, Fabrication and characterization of aluminum airbridges for [superconducting microwave circuits,](https://doi.org/10.1063/1.4863745) Appl. Phys. Lett. **104**, 052602 (2014).
- [26] A. Dunsworth, *et al.*, A method for building low loss multi[layer wiring for superconducting microwave devices,](https://doi.org/10.1063/1.5014033) Appl. Phys. Lett. **112**, 063502 (2018).
- [27] B. M. Niedzielski, J. L. Yoder, D. Ruth-Yost, W. D. Oliver, D. K. Kim, M. E. Schwartz, D. Rosenberg, G. Calusine, R. Das, A. J. Melville, J. Plant, and L. Racz, in *IEEE International Electron Devices Meeting (IEDM)* (IEEE, San Francisco, CA, USA, 2019).
- [28] G. J. Norris, L. Michaud, D. Pahl, M. Kerschbaum, C. Eichler, J.-C. Besse, and A. Wallraff, Improved parameter targeting in 3D-integrated superconducting circuits through [a polymer spacer process,](https://doi.org/10.1140/epjqt/s40507-023-00213-x) EPJ Quantum Technol. **11**, 5 (2024).
- [29] M. Vahidpour, W. O'Brien, J. T. Whyland, J. Angeles, J. Marshall, D. Scarabelli, G. Crossman, K. Yadav, Y. Mohan, C. Bui, V. Rawat, R. Renzas, N. Vodrahalli, A. Bestwick, and C. Rigetti, Superconducting through-silicon vias for quantum integrated circuits, [ArXiv:1708.02226.](https://arxiv.org/abs/1708.02226)
- [30] J. L. Mallek, D.-R. W. Yost, D. Rosenberg, J. L. Yoder, G. Calusine, M. Cook, R. Das, A. Day, E. Golden, D. K. Kim, J. Knecht, B. M. Niedzielski, M. Schwartz, A. Sevi, C. Stull, W. Woods, A. J. Kerman, and W. D. Oliver, Fabrication of superconducting through-silicon vias, [ArXiv:2103.08536.](https://arxiv.org/abs/2103.08536)
- [31] K. Grigoras, *et al.*, Qubit-compatible substrates with super[conducting through-silicon vias,](https://doi.org/10.1109/TQE.2022.3209881) IEEE Trans. Quantum Eng. **3**, 5100310 (2022).
- [32] J. J. Burnett, A. Bengtsson, M. Scigliuzzo, D. Niepce, M. Kudra, P. Delsing, and J. Bylander, Decoherence bench[marking of superconducting qubits,](https://doi.org/10.1038/s41534-019-0168-5) npj Quantum Inf. **5**, 54 (2019).
- [33] A. Osman, J. Simon, A. Bengtsson, S. Kosen, P. Krantz, D. P. Lozano, M. Scigliuzzo, P. Delsing, J. Bylander, and A. Fadavi Roudsari, Simplified Josephson-junction fabrication

## PDF page 21

- process for reproducibly high-performance superconducting qubits, [Appl. Phys. Lett.](https://doi.org/10.1063/5.0037093) **118**, 064002 (2021).
- [34] A. Osman, J. Fernández-Pendás, C. Warren, S. Kosen, M. Scigliuzzo, A. Frisk Kockum, G. Tancredi, A. Fadavi Roudsari, and J. Bylander, Mitigation of frequency colli[sions in superconducting quantum processors,](https://doi.org/10.1103/PhysRevResearch.5.043001) Phys. Rev. Res. **5**, 043001 (2023).
- [35] P. A. Shah, *et al.*, Qiskit-community/qiskit-metal: QISKIT METAL 0.1.5a1 (2023).
- [36] ANSYS Electronics Desktop, Release 21.2 (2021).
- [37] Tanner L-Edit IC (2021).
- [38] D. M. Abrams, N. Didier, S. A. Caldwell, B. R. Johnson, and C. A. Ryan, Methods for measuring magnetic [flux crosstalk between tunable transmons,](https://doi.org/10.1103/PhysRevApplied.12.064022) Phys. Rev. Appl. **12**, 064022 (2019).
- [39] U. Warring, C. Ospelkaus, Y. Colombe, R. Jördens, D. Leibfried, and D. J. Wineland, Individual-ion address[ing with microwave field gradients,](https://doi.org/10.1103/PhysRevLett.110.173002) Phys. Rev. Lett. **110**, 173002 (2013).
- [40] C. Piltz, T. Sriarunothai, A. Varón, and C. Wunderlich, A trapped-ion-based quantum byte with 10−<sup>5</sup> next-neighbour cross-talk, [Nat. Commun.](https://doi.org/10.1038/ncomms5679) **5**, 4679 (2014).
- [41] D. P. L. Aude Craik, N. M. Linke, M. A. Sepiol, T. P. Harty, J. F. Goodwin, C. J. Ballance, D. N. Stacey, A. M. Steane, D. M. Lucas, and D. T. C. Allcock, High-fidelity spatial and polarization addressing of 43Ca<sup>+</sup> qubits using near-field microwave control, Phys. Rev. A **95**[, 022337 \(2017\).](https://doi.org/10.1103/PhysRevA.95.022337)
- [42] I. Pogorelov, T. Feldker, Ch. D. Marciniak, L. Postler, G. Jacob, O. Krieglsteiner, V. Podlesnic, M. Meth, V. Negnevitsky, M. Stadler, B. Höfer, C. Wächter, K. Lakhmanskiy, R. Blatt, P. Schindler, and T. Monz, Compact [ion-trap quantum computing demonstrator,](https://doi.org/10.1103/PRXQuantum.2.020343) PRX Quantum **2**, 020343 (2021).
- [43] C. Fang, Y. Wang, S. Huang, K. R. Brown, and J. Kim, Crosstalk suppression in individually addressed two-qubit [gates in a trapped-ion quantum computer,](https://doi.org/10.1103/PhysRevLett.129.240504) Phys. Rev. Lett. **129**, 240504 (2022).
- [44] A. Binai-Motlagh, M. L. Day, N. Videnov, N. Greenberg, C. Senko, and R. Islam, A guided light system for agile individual addressing of Ba<sup>+</sup> qubits with 10<sup>−</sup><sup>4</sup> level intensity crosstalk, [Quantum Sci. Technol.](https://doi.org/10.1088/2058-9565/ace6cb) **8**, 045012 (2023).
- [45] H. Levine, A. Keesling, G. Semeghini, A. Omran, T. T. Wang, S. Ebadi, H. Bernien, M. Greiner, V. Vuletic, H. ´ Pichler, and M. D. Lukin, Parallel implementation of high[fidelity multiqubit gates with neutral atoms,](https://doi.org/10.1103/PhysRevLett.123.170503) Phys. Rev. Lett. **123**, 170503 (2019).
- [46] Y. Wang, A. Kumar, T.-Y. Wu, and D. S. Weiss, Singlequbit gates based on targeted phase shifts in a 3D neutral atom array, Science **352**[, 1562 \(2016\).](https://doi.org/10.1126/science.aaf2581)
- [47] B. Undseth, X. Xue, M. Mehmandoost, M. Rimbach-Russ, P. T. Eendebak, N. Samkharadze, A. Sammak, V. V. Dobrovitski, G. Scappucci, and L. M. K. Vandersypen, Nonlinear response and crosstalk of electrically driven silicon spin qubits, [Phys. Rev. Appl.](https://doi.org/10.1103/PhysRevApplied.19.044078) **19**, 044078 (2023).
- [48] C. Neill, *et al.*, A blueprint for demonstrating quantum [supremacy with superconducting qubits,](https://doi.org/10.1126/science.aao4309) Science **360**, 195 (2018).
- [49] J. Braumüller, A. H. Karamlou, Y. Yanay, B. Kannan, D. Kim, M. Kjaergaard, A. Melville, B. M. Niedzielski,

- Y. Sung, A. Vepsäläinen, R. Winik, J. L. Yoder, T. P. Orlando, S. Gustavsson, C. Tahan, and W. D. Oliver, Probing quantum information propagation with out-of-timeordered correlators, Nat. Phys. **18**[, 172 \(2022\).](https://doi.org/10.1038/s41567-021-01430-w)
- [50] A. H. Karamlou, I. T. Rosen, S. E. Muschinske, C. N. Barrett, A. Di Paolo, L. Ding, P. M. Harrington, M. Hays, R. Das, D. K. Kim, B. M. Niedzielski, M. Schuldt, K. Serniak, M. E. Schwartz, J. L. Yoder, S. Gustavsson, Y. Yanay, J. A. Grover, and W. D. Oliver, Probing entanglement [in a 2D hard-core Bose-Hubbard lattice,](https://doi.org/10.1038/s41586-024-07325-z) Nature **629**, 561 (2024).
- [51] V. Schmitt, Ph.D. thesis, Pierre and Marie Curie University—Paris VI (2015), [https://theses.hal.science/tel-012](https://theses.hal.science/tel-01214394/) 14394/.
- [52] J. B. Hertzberg, E. J. Zhang, S. Rosenblatt, E. Magesan, J. A. Smolin, J.-B. Yau, V. P. Adiga, M. Sandberg, M. Brink, J. M. Chow, and J. S. Orcutt, Laser-annealing Josephson junctions for yielding scaled-up superconducting quantum processors, [npj Quantum Inf.](https://doi.org/10.1038/s41534-021-00464-5) **7**, 129 (2021).
- [53] M. Roth, M. Ganzhorn, N. Moll, S. Filipp, G. Salis, and S. Schmidt, Analysis of a parametrically driven exchange-type gate and a two-photon excitation gate [between superconducting qubits,](https://doi.org/10.1103/PhysRevA.96.062323) Phys. Rev. A **96**, 062323 (2017).
- [54] J. Wenner, M. Neeley, R. C. Bialczak, M. Lenander, E. Lucero, A. D. O'Connell, D. Sank, H. Wang, M. Weides, A. N. Cleland, and J. M. Martinis, Wirebond crosstalk and cavity modes in large chip mounts for superconducting qubits, [Supercond. Sci. Technol.](https://doi.org/10.1088/0953-2048/24/6/065001) **24**, 065001 (2011).
- [55] D. R. W. Yost, M. E. Schwartz, J. Mallek, D. Rosenberg, C. Stull, J. L. Yoder, G. Calusine, M. Cook, R. Das, A. L. Day, E. B. Golden, D. K. Kim, A. Melville, B. M. Niedzielski, W. Woods, A. J. Kerman, and W. D. Oliver, Solid-state qubits [integrated with superconducting through-silicon vias,](https://doi.org/10.1038/s41534-020-00289-8) npj Quantum Inf. **6**, 59 (2020).
- [56] T. M. Hazard, W. Woods, D. Rosenberg, R. Das, C. F. Hirjibehedin, D. K. Kim, J. M. Knecht, J. Mallek, A. Melville, B. M. Niedzielski, K. Serniak, K. M. Sliwa, D. R. W. Yost, J. L. Yoder, W. D. Oliver, and M. E. Schwartz, Characterization of superconducting through-silicon vias as [capacitive elements in quantum circuits,](https://doi.org/10.1063/5.0170055) Appl. Phys. Lett. **123**, 154004 (2023).
- [57] L. Chayanun, J. Biznárová, L. Zeng, P. Malmberg, A. Nylander, A. Osman, M. Rommel, P. L. Tam, E. Olsson, P. Delsing, A. Yurgens, J. Bylander, and A. Fadavi Roudsari, Characterization of process-related interfacial dielectric loss in aluminum-on-silicon by resonator microwave mea[surements, materials analysis, and imaging,](https://doi.org/10.1063/5.0208140) APL Quantum **1**, 026115 (2024).
- [58] J. Johansson, P. Nation, and F. Nori, QuTiP: An opensource PYTHON framework for the dynamics of open quantum systems, [Comput. Phys. Commun.](https://doi.org/10.1016/j.cpc.2012.02.021) **183**, 1760 (2012).
- [59] J. Johansson, P. Nation, and F. Nori, QuTiP 2: A PYTHON framework for the dynamics of open quantum systems, [Comput. Phys. Commun.](https://doi.org/10.1016/j.cpc.2012.11.019) **184**, 1234 (2013).
- [60] A. Blais, A. L. Grimsmo, S. M. Girvin, and A. Wallraff, [Circuit quantum electrodynamics,](https://doi.org/10.1103/RevModPhys.93.025005) Rev. Mod. Phys. **93**, 025005 (2021).
