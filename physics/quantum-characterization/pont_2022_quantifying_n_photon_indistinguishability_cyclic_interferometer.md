Source: https://doi.org/10.1103/PhysRevX.12.031033
PDF sha256: 0993250cf6f10adcc26ad17bb1855b6c1fbc2644e1e670d8b7d64b776af0c274
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of pont_2022_quantifying_n_photon_indistinguishability_cyclic_interferometer.pdf

Transcription of `pont_2022_quantifying_n_photon_indistinguishability_cyclic_interferometer.pdf` in this directory, 22 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

## Quantifying *n*-Photon Indistinguishability with a Cyclic Integrated Interferometer

Mathias Pont<sup>®</sup>, <sup>1,‡</sup> Riccardo Albiero<sup>®</sup>, <sup>2,3,‡</sup> Sarah E. Thomas<sup>®</sup>, <sup>1,\*,‡</sup> Nicolò Spagnolo<sup>®</sup>, <sup>4</sup> Francesco Ceccarelli<sup>®</sup>, <sup>3</sup> Giacomo Corrielli<sup>®</sup>, Alexandre Brieussel, <sup>5</sup> Niccolo Somaschi, <sup>5</sup> Hêlio Huet<sup>®</sup>, <sup>1</sup> Abdelmounaim Harouri, <sup>1</sup> Aristide Lemaître<sup>®</sup>, <sup>1</sup> Isabelle Sagnes<sup>®</sup>, <sup>1</sup> Nadia Belabas, <sup>1</sup> Fabio Sciarrino, <sup>4</sup> Roberto Osellame<sup>®</sup>, <sup>3</sup> Pascale Senellart, and Andrea Crespi<sup>2,3,†</sup>

<sup>1</sup>Centre for Nanosciences and Nanotechnology, CNRS, Université Paris-Saclay, UMR 9001,10 Boulevard Thomas Gobert, 91120, Palaiseau, France <sup>2</sup>Dipartimento di Fisica-Politecnico di Milano, piazza Leonardo da Vinci 32, 20133 Milano, Italy <sup>5</sup>Istituto di Fotonica e Nanotecnologie-Consiglio Nazionale delle Ricerche (IFN-CNR), piazza Leonardo da Vinci 32, 20133 Milano, Italy <sup>4</sup>Dipartimento di Fisica, Sapienza Università di Roma, piazzale Aldo Moro 5, 00185, Rome, Italy <sup>5</sup>Quandela SAS, 7 Rue Léonard de Vinci, 91300 Massy, France

(Received 31 January 2022; revised 6 June 2022; accepted 11 August 2022; published 2 September 2022)

We report on a universal method to measure the genuine indistinguishability of n photons—a crucial parameter that determines the accuracy of optical quantum computing. Our approach relies on a low-depth cyclic multiport interferometer with N=2n modes, leading to a quantum interference fringe whose visibility is a direct measurement of the genuine n-photon indistinguishability. We experimentally demonstrate this technique for an eight-mode integrated interferometer fabricated using femtosecond laser micromachining and four photons from a quantum dot single-photon source. We measure a fourphoton indistinguishability up to  $0.81 \pm 0.03$ . This value decreases as we intentionally alter the photon pairwise indistinguishability. The low-depth and low-loss multiport interferometer design provides an original path to evaluate the genuine indistinguishability of resource states of increasing photon number.

DOI: 10.1103/PhysRevX.12.031033 Subject Areas: Optics, Quantum Physics **Quantum Information** 

## I. INTRODUCTION

Optical quantum computing has recently gained important momentum with the demonstration of the so-called "quantum advantage" regime [1-3]. Quantum states of many indistinguishable photons are key elements for photonic quantum computing since the indistinguishable nature of the particles enables the implementation of effective photon-photon gates. Furthermore, scaling up to larger photon numbers is a key element to activate quantum speedup, implement fault tolerance, and reach a higher number of users in a quantum network. Experimentally, the efficient generation of identical single photons is indeed an important technological challenge that is currently

Corresponding author. s.thomas14@imperial.ac.uk

Published by the American Physical Society under the terms of the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the author(s) and the published article's title, journal citation, and DOI.

addressed with two main approaches, one based on multiplexing many heralded single-photon sources [4,5], the other based on bright single emitters, namely semiconductor quantum dots (QDs) [6–9].

On the fundamental side, quantifying the indistinguishability of the targeted multiple-photon states has recently been identified as a complex task. In the case of two photons, the indistinguishability is readily measured by performing a Hong-Ou-Mandel (HOM) interference experiment [10,11]. For two-photon wave packets, the visibility of the quantum interference fringe gives full access to the indistinguishability parameter, provided that the sources of noise are well understood [12–14]. However, when more than two photons are involved, indistinguishability is not completely characterized by pairwise HOM experiments [11]. For instance, multiphoton states could be engineered that show nonzero visibility in the HOM interference of all possible pairs, but yield vanishing overlap with pure states of all-identical photons [15]. Indeed, to describe exhaustively multiphoton interference processes, concepts such as the genuine multiparticle indistinguishability [15] must be considered—a parameter that quantifies the overlap of the multiphoton state with the pure state of *n* identical photons. Currently, only methods

Corresponding author. andrea.crespi@polimi.it

<sup>\*</sup>These authors contributed equally to this work.

## PDF page 2

capable of providing the lower and upper bounds to this key quantity have been defined [\[15](#page-20-10)[,16\]](#page-20-11).

Different generalizations of the HOM effect to the manyparticle case have been proposed theoretically and observed in experiments [\[17](#page-20-12)–[22\]](#page-20-13). Such generalized HOM effects, which harness multiport interferometers with specific symmetries, consist of suppression laws [\[17](#page-20-12)–[21](#page-20-14)]: indistinguishability of the photons in the input state results in a large number of forbidden output states among the manyparticle possible ones. Indeed, the observation of such suppression effects can be used to validate multiphotoninterference experiments against other hypotheses, namely to assess whether it is more likely that the detected outputs result from true quantum interference of indistinguishable photons, rather than from specific classical input states considered as alternatives [\[23](#page-20-15)[,24\]](#page-20-16). However, quantifying the genuine multiphoton indistinguishability is a different task, which is challenging to achieve. Totally destructive interference is observed in specific cases also with partially distinguishable photon states that obey certain symmetries [\[25\]](#page-20-17), which highlights the nonintuitive connections between genuine indistinguishability and quantum interference. Notable insights on the requirements for multiparticle interference were also provided recently in Ref. [[26](#page-20-18)]. At present, only witnesses of indistinguishability have been proposed [\[16](#page-20-11)[,27\]](#page-20-19), while a general technique to quantitatively measure the genuine indistinguishability of many photons is missing.

Here, we propose a method to quantify the genuine n-photon indistinguishability, applicable to an arbitrary number of photons. Our scheme relies on a cyclic multiport interferometer with <sup>N</sup> ¼ <sup>2</sup><sup>n</sup> optical modes, composed of <sup>2</sup><sup>n</sup> beam splitters placed along two cascaded layers. Notably, this two-layer optical depth does not depend on n, thus keeping the layout extremely simple also for states with a large number of photons. We show that when n indistinguishable photons are injected in the interferometer, the output distribution exhibits quantum interference depending on a single internal phase, and the interference visibility directly corresponds to the genuine n-photon indistinguishability. Conversely, no quantum interference is observed for input Fock states with less than n photons. We demonstrate experimentally our idea with four photons and an eightmode version of this interferometer. The four-photon state is obtained from a quantum dot single-photon source (QDSPS) [[28](#page-20-20)] using a time-to-spatial mode demultiplexer, while the interferometer is fabricated in integrated optics by taking advantage of the three-dimensional capabilities of the femtosecond laser micromachining technology [\[29,](#page-21-0)[30](#page-21-1)]. We observe full compatibility between the measured amplitude of the quantum interference fringe and the bounds given by the pairwise indistinguishabilities of the four-photon state. This is done for a large range of pairwise indistinguishability values of the input photons, which we tune through spectral filtering or exploiting the polarization degree of freedom. In addition, we see excellent agreement between our measurements and the numerical simulations that take into account the imperfections of our experimental apparatus.

## II. THEORETICAL PROPOSAL: CYCLIC INTERFEROMETER DESIGN

## A. Premise

As mentioned above, the typical way to measure the indistinguishability of two single photons exploits the HOM effect. Namely, the photons are injected in the two separate input ports of a balanced beam splitter; the delay between the two photons is scanned by varying the optical length of one of the incoming paths, while coincidence detections at the two separate output ports are monitored. A dip in the interference pattern, i.e., the suppression of coincidence detection, is observed for null relative delay, and the visibility of this dip quantifies the indistinguishability of the photon pair.

As a matter of fact, this experimental layout is not the only one that gives access to the latter quantity. For instance, the two photons could be injected simultaneously in the separate input ports of a Mach-Zehnder interferometer with balanced arms, while again monitoring the coincidence detection of two photons at the two separate output ports. If the internal phase of the Mach-Zehnder interferometer is scanned, a quantum interference fringe is measured in the coincidences [\[31\]](#page-21-2). This fringe shows half of the period that would be observed in the case of classical light, and its visibility is directly linked to the visibility of the HOM dip, thus also providing a quantification of the two-photon indistinguishability.

Our proposed 2n-mode cyclic interferometer in some sense generalizes the latter kind of measurement to the case of n photons. Indeed, we will show that in our device n-photon interference fringes are measured while scanning one of the internal phase delays, and that the visibility of this fringe directly quantifies the n-photon indistinguishability. However, in contrast to the two-arm Mach-Zehnder interferometer, which demonstrates interference fringes with either single photons or classical light, in our case interference fringes cannot be observed with input states of less than n photons. In fact, no closed Mach-Zehnder rings are present in our cyclic layout.

A conceptual scheme of our experiment is shown in Fig. [1\(a\)](#page-2-0). A first layer of balanced beam splitters splits the input state composed of n photons into two alternative series of paths. The two series are then interfered by a second layer of balanced beam splitters. Connections between the layers are designed in such a way that each photon is directly overlapped only with the adjacent ones in the input state. Connections yield cyclic symmetry, as the

## PDF page 3

FIG. 1. (a) Conceptual scheme of the interference process. The cyclic interferometer consists of two cascaded layers of balanced beam splitters. If we inject one photon per pair of adjacent input modes, the first beam splitter layer branches the input state into two alternative paths (reflected R and transmitted T). Paths are interfered pairwise at the second layer, employing a cyclic layout. (b) In most general terms, the phase delays that are physically introduced by the optical propagation on the internal arms of the interferometers can be described by phase terms  $\phi_i$ . (c) Schematic representation of an interferometer equivalent to the one shown in (b), where the many phase shifts  $\phi_i$  are replaced by a single element  $\alpha_1$  on the first arm, with phase delays considered as null in the other arms.

*n*th photon is interfered with the first one. Interestingly, by performing collective coincidence measurements at the output, we show that it is possible to infer an intrinsic property of the whole set of photons, i.e., their genuine indistinguishability.

In the following, we describe in detail the optical layout of the interferometer and then discuss its properties in a series of propositions. First, we show that the many phase delays that are involved in the optical circuit can be combined in a single relevant phase term (Sec. II B). Then, we analyze theoretically multiphoton interference in this device, showing that an *n*-photon interference fringe is visible in certain conditions when varying the single phase term (Sec. II C), and that the visibility of this fringe is a measure of the genuine *n*-photon indistinguishability (Sec. II D).

## B. Layout of the proposed interferometer

The proposed two-layer cyclic scheme is schematically represented in Fig. 1(b) in the most general fashion. The circuit contains N = 2n modes and is composed of two layers of cascaded beam splitters. The beam splitters in the first layer connect each odd mode with the subsequent even one (i.e., the mode 2m - 1 with the mode 2m). The beam splitters in the second layer connect each even mode with the subsequent odd one (i.e., the mode 2m with the mode 2m + 1). In this second layer, the Nth mode is connected with the first one, such that the device has perfect cyclical symmetry. All the beam splitters are balanced and symmetric. The phase delays that correspond to the individual optical paths connecting the first to the second layer of beam splitters can be described by phase shifts with values  $\phi_i$ . For the sake of simplicity, in the following we will refer to an interferometer with this layout as cyclic interferometer (CI).

In general terms, the operation of a linear optical interferometer can be described by a unitary matrix U that transforms, in the Heisenberg picture, the creation operators of the input modes into the creation operators of the output modes. This matrix allows us to describe the interferometer operation on any possible input state.

When studying multiphoton interference, however, one is often interested in the operation of the linear circuit on Fock states. A generic Fock state of k photons on N modes can be written as

$$|s\rangle = \left(\prod_{i=1}^{k} a_{s_i}^{\dagger}\right)|0\rangle,\tag{1}$$

where  $a_{s_i}^{\dagger}$  is the creation operator on the mode  $s_i$ . Such a state can be identified by the k-element vector  $\underline{s} = (s_1, s_2, ..., s_k)$ , with  $1 \le s_i \le N$ . In the following, we write as  $P_{\underline{g},\underline{h}}$  the probability to measure a certain Fock state  $\underline{h}$  at the output when a given Fock state  $\underline{g}$  is fed at the input of the device.

## PDF page 4

Definition 1.—Two N-mode interferometers are here defined as *equivalent* if they give the same  $P_{\underline{g},\underline{h}}$  for each possible couple of input and output Fock states g and  $\underline{h}$ .

Note that two equivalent interferometers may not be described by the same unitary matrix U. In particular, it is well known that two interferometers are equivalent in the sense of Definition 1 if their optical circuits differ only in phase terms placed at the input or output ports [32]. We refer the reader to the example in Appendix A, where the simple case of a Mach-Zehnder interferometer is analyzed.

Proposition 1.—The CI of Fig. 1(b), with arbitrary phase delays  $\phi_i$  in the internal arms, is equivalent to the CI of Fig. 1(c), where a single phase shift,

$$\alpha_1 = \sum_{m=1}^{N/2} \phi_{2m-1} - \phi_{2m},\tag{2}$$

is placed on the first arm, and null phase delays are assumed in the other ones.

The proof of this proposition is given in full in Appendix B. Such proof is constructed by showing that the phase delay  $\phi_i$  on an arbitrary ith arm can be replaced, without changing the unitary matrix U of the interferometer, by a null phase delay on the ith arm, a different phase delay  $\phi'_{i-1}$  on the (i-1)th arm, and two additional phase shifts placed directly on the input or the output ports of the interferometer. This procedure can be iterated starting from the Nth arm up to the second one, and one ends up with a CI with several more phase shifts on the input and output ports, and null phase delays on all internal arms except the first one. In particular, one shows that the phase delay on the first arm now takes the value given by Eq. (2). At this point, the added phases at the inputs and outputs can be removed producing a CI equivalent to the first one, which is indeed the one shown in Fig. 1(c).

Actually, due to the cyclic symmetry of the device, one may alternatively implement the phase-delay replacements described above starting from a different point [say, the (j-1)th arm], which results in a single remaining phase shifter placed on the jth mode. Working out the details, the following corollary is easily proven.

Corollary 1.1.—There are N CIs equivalent to the one shown in Fig. 1(b), each with a phase element  $\alpha_j$  on an arbitrary internal arm j and null phases in the others. If j is odd,  $\alpha_i = \alpha_1$ ; otherwise,  $\alpha_i = -\alpha_1$ .

For the experimenter, Proposition 1 and its Corollary 1.1 mean that a single active phase shifter in the CI is sufficient to access all the operation space that would be given by controlling separately all the  $\phi_i$ .

### C. Interference of indistinguishable photons

To study multiphoton interference in the CI, we address first the case in which the device, having N=2n modes, is injected with arbitrary input states having  $k \le n-1$ 

photons. In fact, for these input states the following interesting fact holds.

Proposition 2.—If the CI is fed with  $k \le n-1$  photons, the values of the internal phases  $\phi_i$  of the device do not have any influence on the output photon distribution.

Indeed, in this case, at least one of the beam splitters of the first layer has no photon at the input; say that this beam splitter is connecting modes 2m-1 and 2m. Because of Corollary 1.1 we can compose an equivalent CI which has only one phase shift  $\alpha_{2m}$  on the mode 2m. No photon of the input state will then travel through this phase shift  $\alpha_{2m}$ ; thus a change  $\alpha_{2m}$  cannot affect the output distribution. Since  $\alpha_{2m}$  is defined as an algebraic sum of all the phases  $\phi_i$ , this means that variation of any  $\phi_i$  does not affect the output.

Note that, to prove Proposition 2, we have crucially exploited the fact that interferometers that are equivalent according to Definition 1 yield the same output distribution, and therefore we can investigate this distribution by choosing the most convenient device configuration among the possible ones.

Given the absence of closed interferometric rings in the CI layout, and the result of Proposition 2, one may doubt that the internal phases  $\phi_i$  influence the output distribution at all. Actually, interference fringes modulated by the  $\phi_i$  can be observed in certain cases, in which the CI is fed with n indistinguishable photons.

An instructive example is the case in which the n identical photons are distributed one per odd input mode, and coincidence detection of one photon per odd output mode is monitored. We prove in Appendix C the following.

*Proposition 3.*—Given a CI with N = 2n modes, and considering the input state  $\underline{g} = (1, 3, 5, ..., 2n - 1)$  of n identical photons, the probability to detect the output state  $\underline{h} = (1, 3, 5, ..., 2n - 1)$  is given by

$$P = \frac{1}{2^{2n-1}} [1 + (-1)^n \cos \alpha_1]. \tag{3}$$

While the previous propositions are based on purely topological features of the device, Proposition 3 involves specific properties of its unitary matrix, whose details are discussed in Appendix C.

This result indicates an interference fringe with unit visibility, as a function of the phase term  $\alpha_1$ . An intuition of the physical process underlying this interference fringe can be given by the observation that, due to the specific layout of the CI, a photon from any given input mode 2m-1 can reach only two different odd modes at the output: either the mode 2m-1 (i.e., the same mode) or the mode 2m+1 (i.e., the subsequent odd mode). It can be noted that, regardless of the distinguishable or indistinguishable nature of the input photons, there are only two possible evolutions that produce the desired output state  $\underline{h}$ : either each photon remains in the same odd mode in which it has been injected, or each photon shifts to the subsequent odd mode. In fact,

## PDF page 5

if all the photons are perfectly indistinguishable, one cannot distinguish between the two possibilities and interference arises between the two evolution paths.

Actually, the case studied in Proposition 3 is the archetype of all the possible input and output states of n photons that can result in an interference fringe as a function of the internal phases. Indeed, we prove in Appendix D the following result.

*Proposition 4.*—Given a CI with N=2n modes, an n-photon interference fringe as a function of the internal phases can be measured if and only if the input state has precisely one photon per pair of input ports  $(1,2)-\ldots-(2m-1,2m)-\ldots$  and the output state has precisely one photon per pair of output ports  $(2,3)-\ldots-(2m,2m+1)-\ldots-(1,N)$ . In particular, for all input-output states of identical photons satisfying this rule, the detection probability takes the form:


$$P = \frac{1}{2^{2n-1}} [1 + (-1)^{n+p+q} \cos \alpha_1], \tag{4}$$

where p is the number of occupied even modes in the input state and q is the number of occupied even modes in the output state.

For instance, in the case of an eight-mode interferometer, the combination  $\{\underline{g}=(2,3,5,7);\underline{h}=(1,2,4,7)\}$  has one occupied even mode (the mode 2) in the input state  $\underline{g}$  and two occupied even modes (the modes 2 and 4) in the output state  $\underline{h}$ . Since in this case n=4, one has  $(-1)^{(4+1+2)}=-1$  and the term  $\cos\alpha_1$  in the equation has to be taken with the minus sign.

We would again like to highlight the fact that, whereas Propositions 3 and 4 ensure that the internal phase  $\alpha_1$ affects the quantum interference of *n* photons, Proposition 2 warns that it does not have influence on two-photon experiments. This contrasts with the standard techniques currently in use to characterize multiport devices, such as the one devised in Ref. [33], which allows us to retrieve the unitary matrix of the interferometer through one- and twophoton statistics only. These techniques are often tacitly assumed to be universal, but here they would not be able to provide the value of the phase  $\alpha_1$ . As a matter of fact, such methods implicitly assume that the unitary matrix of the device has at least one column and one row made of nonvanishing elements. This appears not to be the case here, where each input is connected with a small set of outputs, and thus the unitary matrix of the circuit is highly sparse.

## D. Interference of partially distinguishable photons

We now consider the effect of input states of n photons that are not perfectly indistinguishable. Namely, the n photons may present differences in any of their internal degrees of freedom (time distribution, wavelength, polarization, etc.) [34]. At the same time, we consider that the

structure of the interferometer is instead insensitive to such differences.

Using the approach of Refs. [15,16] we describe the photon states with a density matrix of the kind

$$\rho = c_1 \rho^{\parallel} + \sum_i c_i \rho_i^{\perp},\tag{5}$$

where  $\rho^{\parallel}$  is a pure state with all n photons absolutely indistinguishable, while the states  $\rho_i^{\perp}$ , i>1, are pure states where a subset of the photons are perfectly identical in all degrees of freedom, while the remaining ones (at least two) are orthogonal with respect to all others (i.e., distinguishable). The coefficient  $c_1$  represents the genuine indistinguishability of the set of photons.

The decomposition is convex; namely, the real coefficients  $c_i$  are all positive and  $c_1 + \sum c_i = 1$ .

In particular, we can first study again the *n*-photon experiment with input state  $\underline{g} = (1, 3, 5, ...)$  and output state  $\underline{h} = (1, 3, 5, ...)$ . Note that, even if we use the same notation for  $\underline{g}$  and  $\underline{h}$  that we used for Fock states of identical photons, here the photons occupying the optical modes can be partly or fully distinguishable, and  $\underline{g}$  is described by  $\rho$ .

Proposition 5.—If the CI is fed with one photon per odd mode, with the *n*-photon state described by Eq. (5), the probability to detect at the output again one photon per odd mode is given by

$$P' = \frac{1}{2^{2n-1}} [1 + (-1)^n c_1 \cos \alpha]. \tag{6}$$

To calculate P' we need to retrieve first the probability of the desired output state  $\underline{h}$  considering as input  $\rho^{\parallel}$  and each of the components  $\rho_i^{\perp}$ . The probability in the case of  $\rho^{\parallel}$  is the one studied in Sec. II C, and is given by Eq. (3). For any of the other states  $\rho_i^{\perp}$ , the fact that at least two photons of this state are orthogonal implies that at least two photons injected in adjacent odd modes are orthogonal, say, 2m-1and 2m + 1. Considering the layout of the CI we observe that the distinguishability of these two photons implies the distinguishability of the two possible evolution paths that the photons follow in the interferometer after the first layer of beam splitter: since we can distinguish the photon initially on mode 2m-1 from the photon initially on mode 2m + 1, we can tell whether they have remained on the same output port or they have shifted two modes forward (see the discussion following Proposition 3, in the previous section). Indeed, if we know the path followed by one photon [e.g., the (2m-1)th one], then there is only one possible path for all the others, independently of their distinguishability or indistinguishability, that produces an output state with photons on odd modes. This leads us to conclude that, if at least one photon is distinguishable from the others, then we can track the path of all of them and they behave as if they were all distinguishable.

## PDF page 6

The probability of detecting an output state  $\underline{h} = (1, 3, 5, ...)$  for input photons that are all distinguishable and in a state  $\underline{g} = (1, 3, 5, ...)$  is demonstrated explicitly in Appendix C to be

$$P_{\text{dist}} = \frac{1}{2^{2n-1}}. (7)$$

Because of the above discussion, this expression holds for all the states  $\rho_i^{\perp}$ .

Finally, the probability of detecting one photon per each odd output mode, for an input state with one photon per each odd mode, described by Eq. (5), is computed as

$$P' = c_1 P + \sum_{i} c_i P_{\text{dist}} = c_1 P + (1 - c_1) P_{\text{dist}}$$
$$= \frac{1}{2^{2n-1}} [1 + (-1)^n c_1 \cos \alpha], \tag{8}$$

which proves the proposition.

One notes that Eq. (6) describes a multiphoton interference fringe with visibility  $V = c_1$ . Therefore, such fringe visibility is a direct indicator of the genuine n indistinguishability of the set of n input photons.

It is not difficult to show that the above discussion also applies identically to all the other pairs of n-photon input and output states which give an observable interference fringe for varying  $\alpha_1$ , as described in Proposition 4. Hence, if n photons are distributed with one photon for each pair of ports  $(1,2)-\ldots-(2m-1,2m)-\ldots$ , one can characterize their n-photon indistinguishability by monitoring the interference fringe observable for any of the  $2^n$  output states having one photon for each pair of ports  $(2,3)-\ldots-(2m,2m+1)-\ldots-(1,N)$ .

This approach can be applied to quantify the amount of genuine indistinguishability in different classes of multiphoton states. Notable examples are the output of quantumdot-based photon sources, employed for the experimental verification described below. Additionally, this approach can be employed with states generated via other technologies, such as spontaneous parametric down-conversion (SPDC) processes. Indeed, the decomposition in Eq. (5) provides an accurate approximation of multimode states generated via sets of SPDC sources when adequate spectral filtering is used [16]. We note that output states useful to this characterization can be detected with a probability decreasing exponentially with n. However, no up-to-date alternative method is able to produce an equivalent measurement in a more efficient way. Thus, the present approach can be fruitfully applied especially in near-term intermediate-scale experiments, which involve a number of photons that is not too large.

### III. EXPERIMENTAL RESULTS

#### A. Measurement of four-photon indistinguishability

We demonstrate experimentally the use of an eight-port CI to characterize the indistinguishability of four-photon states. The CI is realized as a reconfigurable waveguide circuit, using the femtosecond laser direct writing technology [29,30,35,36]. In detail, single-mode waveguides are inscribed in a commercial alumino-borosilicate glass substrate (Eagle XG, Corning, Inc.) by irradiating the desired paths with multiple laser scans and by performing thermal annealing thereafter [37]. Note that, to implement the CI layout in a compact fashion, waveguides are required to pass one over the others without crossing, to reach the last beam splitter connecting modes 1 and N; this is uniquely made possible by the three-dimensional capabilities of femtosecond laser micromachining. The integrated interferometer has a planar footprint of about  $1 \times 30 \text{ mm}^2$ ; at the crossing points, vertical separation between the waveguides is in the order of 20– $30 \mu m$ .

A phase shifter is fabricated on the top surface, in correspondence of one of the interferometer's arm, by patterning a resistive microheater in a gold film through femtosecond laser ablation. Driving an electric current in the microheater produces a local temperature increase, which in turn induces a controlled phase shift on the underlying waveguides due to the thermo-optic effect. To interface the circuit with the photon sources and with the detectors, single-mode fibers are glued with UV-curing resin, to both the input and the output ports of the chip. In order to enable the efficient collection of four-photon coincidences, particular care was given to reducing the insertion loss of the optical device, which results to be lower than 2 dB.

A four-photon state is generated from a quantum dot single-photon source. The QDSPS is based on a neutral InGaAs quantum dot embedded in an electrically contacted micropillar cavity [28,38], which is placed inside a cryostat at 5 K. The QDSPS is excited using acousticphonon-assisted near-resonant excitation [9] using a 15 ps laser pulse centered at 924.4 nm, at a repetition rate of 82 MHz. This excitation scheme allows for increased source efficiency and stability, a key requirement for multiphoton experiments. The single photons are emitted at 925.0 nm and are separated from the excitation laser using three 0.8 nm bandpass filters with a transmission of 95% and a laser suppression of approximately 40 dB per filter, before being collected into a single-mode fiber. We characterize the single-photon purity of the source in a Hanbury-Brown and Twiss measurement, obtaining  $\mathcal{P} = 1 - g^{(2)}(0) = (98.1 \pm 0.1)\%$ .

The stream of single photons is separated into four spatial modes using a demultiplexer (DMX) from Quandela. The DMX consists of an acousto-optic modulator (AOM) which, when driven by a time-varying radio-frequency (rf) signal, diffracts the incoming light into different spatial modes depending on the driving frequency. The time-varying signal driving the AOM has a total cycle time of  $4\Delta T$ : the rf signal is on at three distinct frequencies for  $\Delta T$  each, and then off for  $\Delta T$ . As pictured in Fig. 2, the incoming photons are thus

## PDF page 7

FIG. 2. Schematic of the experimental setup. A quantum-dot-based single-photon source (QDSPS) is excited periodically and emits a stream of single photons. The photons are separated into four spatial modes using a demultiplexer which is based on a periodically driven acousto-optic modulator (AOM). The polarization of the photons is controlled using wave plates, and delay fibers are used to ensure the simultaneous arrival times of the four photons. The photons are sent into the odd modes of the integrated CI, fabricated by femtosecond laser micromachining. The photons are detected at the output of the interferometer using superconducting nanowire single-photon detectors (SNSPDs), and four-photon coincidences are recorded using a correlator. The internal phase of the interferometer  $\alpha_1$  is varied by scanning the voltage applied to the microheater realized on the chip surface.

switched among four spatial modes: three corresponding to first-order diffraction through the AOM at different frequencies, and one corresponding to direct transmission through the AOM when no rf signal is applied. Note that the frequency shift of the photons induced via first-order diffraction through the AOM is quite a lot smaller than the bandwidth of the photons (~200 MHz versus ~2.1 GHz), and hence it does not affect significantly their indistinguishability. After the DMX, the photons in all four spatial modes are coupled into single-mode fibers of different lengths such that the photons enter the CI simultaneously. We can experimentally achieve a precision of a few picoseconds in the arrival time of the single photons, which is much smaller than their lifetime of about 145 ps. A quarter and a half wave plate are used on each spatial mode to adjust the polarization of each photon at the input of the CI. Special care was taken to achieve passive mechanical and thermal stability of the DMX and fiber delays. We use two versions of the DMX with different cycle times  $4\Delta T$  (see Sec. III C), and the total transmission of the DMX is  $\sim$ 45% ( $\sim$ 65%) for the first (second) design.

The initial design of the DMX has an operating time of  $\Delta T = 320$  ns, meaning that the photons entering ports 1 and 7 of the interferometer were emitted by the QDSPS at a separation time of 960 ns. In order to understand the impact of delays on the multiphoton state, we investigate the indistinguishability of the photons emitted by the ODSPS at different separation times. We measure the indistinguishability via two-photon HOM interference in a path-unbalanced Mach-Zender interferometer. We extract the visibility of HOM interference  $V_{HOM}$  and correct for the nonzero  $q^{(2)}(0)$  to extract the indistinguishability of the single-photon component  $M_s$  [14]. When the delay between the photons is 12.3 ns, corresponding to the pulse separation of the laser, the visibility [indistinguishability] is  $V_{\text{HOM}} = (88.6 \pm 0.1)\%$  [ $M_s = (92.3 \pm 0.1)\%$ ]. At longer separation times the visibility (indistinguishability) decreases due to residual charge noise in the QD environment which leads to spectral wandering of the QD emission, as shown in Table II (Appendix E), and at a delay of 960 ns the HOM visibility [indistinguishability] is  $V_{\text{HOM}} = (72.7 \pm 0.1)\%$  [ $M_s = (76.0 \pm 0.1)\%$ ]. We note that such decrease—stronger than previously reported [39]—arises from the specific doping structure of the devices under investigation, which favors a particular charge state of the quantum dot at the expense of increased charge noise.

We inject four simultaneous photons with parallel polarization into the input ports (1, 3, 5, 7) of the interferometer, and monitor the four-photon coincidences on the output. Table I gives the 16 possible four-photon output states where we expect to observe an interference fringe according to the discussion in Sec. II C. The fringe, i.e., the term  $\cos \alpha_1$  in the detection probability, takes either a plus or minus sign according to Proposition 4, as indicated in Table I. Figures 3(a)-3(c) show the number of detected four-photon coincidence events in 30 min in each of the 16 output states, and we see a clear difference in the detected probability for the states that show constructive and destructive interference. Each histogram is for a different value of the electric power  $\mathcal{P}_{\alpha_1}$  dissipated on the resistive microheater, which changes the internal phase  $\alpha_1$ . The total four-photon coincidence rate here is approximately 1.6 Hz. The integration window to define a fourphoton coincidence is set to 2 ns. With this integration window the accidental-to-coincidences ratio is in the order of  $0.013 \pm 0.002$ ; this is defined as the ratio between the average number of four-photon coincidences detected at the output with three photons sent into the interferometer, and the average number of four-photon coincidences detected when four photons are injected. We add together the detected events of all eight states characterized by fringes with the same sign, to increase the measurement statistics. In Fig. 3(d) we plot the total number of coincidences for the outputs corresponding to constructive (blue) or destructive (orange) interference as a function

## PDF page 8

TABLE I. Output states whose detection probability is described by Eq. (4) when four identical photons in the state (1, 3, 5, 7) are injected at the input of the CI. The sign of the interference fringe, i.e., the sign of the term  $\cos \alpha_1$ , is specified for each state.

| Output state | Fringe sign | Output state | Fringe sign |
|--------------|-------------|--------------|-------------|
| (1, 3, 5, 7) | +           | (1, 3, 5, 6) | _           |
| (1, 3, 4, 6) | +           | (1, 3, 4, 7) | _           |
| (1, 2, 5, 6) | +           | (1, 2, 5, 7) | _           |
| (1, 2, 4, 7) | +           | (1, 2, 4, 6) | _           |
| (3, 5, 6, 8) | +           | (3, 5, 7, 8) | _           |
| (3, 4, 7, 8) | +           | (3, 4, 6, 8) | _           |
| (2, 5, 7, 8) | +           | (2, 5, 6, 8) | _           |
| (2, 4, 6, 8) | +           | (2, 4, 7, 8) | _           |

of  $\mathcal{P}_{\alpha_1}$ , normalized to the mean value. We observe a clear interference fringe in the four-photon coincidences, while no variation is observed in the two- and three-photon coincidence rates (graphs reported in Appendix F). We fit the data according to  $P' \propto (1 \pm c_1 \cos \alpha)$  for both the constructive and destructive interference fringes. We extract a visibility, or equivalently a four-photon indistinguishability, of  $c_1 = 0.61 \pm 0.01$ .

## B. Verification: Two-photon bounds and full model

In order to verify and qualify this experimental result, we use two techniques. Firstly, we deduce an upper and a lower bound on the four-photon indistinguishability using the two-photon pairwise indistinguishabilities. The geometry of this interferometer also allows us to simultaneously measure some of the pairwise indistinguishabilities of the input photons, without changing the experimental setup. In particular, photons A and B undergo HOM interference at beam splitter BS5 (see Fig. 2). Therefore, by observing the two-photon coincidences on outputs 2 and 3 we directly measure the HOM interference visibility (and the twophoton indistinguishability [14]) between photons A and B,  $V_{\rm AB}$  ( $M_{\rm AB}$ ). Similarly, the interference between photons B and C is measured at outputs 4 and 5, C and D at outputs 6 and 7, and D and A at outputs 1 and 8. Note that these measurements can be carried out simultaneously while monitoring also the four-photon coincidences.

We use these values to obtain upper and lower bounds for  $c_1$ , by following the methodology discussed in Ref. [15]. In particular, by considering the specific layout of the CI, the following bounds for  $c_1$ , based on the four

FIG. 3. (a)–(c) Number of detected coincidences in 30 min for the 16 four-photon output states for a given electrical power  $P_{\alpha}$  applied to the internal phase shifter of the integrated interferometer. We observe a clear shift from (a) destructive interference at  $P_{\alpha}=290\,$  mW ( $\alpha_1\sim 3\pi$ ) to (c) constructive interference at  $P_{\alpha}=426\,$  mW ( $\alpha_1\sim 4\pi$ ). The error bars indicate the shot-noise error  $\sqrt{N}$  for a given number of coincidences N. (d) The total normalized four-photon coincidence rate (sum of all eight output states) for the constructive and destructive outputs, as a function of  $P_{\alpha 1}$  or the phase  $\alpha_1$ .

## PDF page 9

FIG. 4. Indistinguishability of photon A is reduced with respect to the others, by rotating its polarization using a half wave plate (with respect to the reference position  $\theta=0^\circ$  of the experiment in Fig. 3). (a)–(d) Measured four-photon interference fringe when photon A is made increasingly distinguishable, by rotating the half wave plate respectively by  $\theta_{(a)}=11^\circ$ ,  $\theta_{(b)}=19^\circ$ ,  $\theta_{(c)}=31^\circ$ ,  $\theta_{(d)}=45^\circ$ . The visibility of the interference fringe decreases, as the minimum measured two-photon Hong-Ou-Mandel interference visibility (extracted single-photon indistinguishability)  $V_{\min}$  ( $M_{\min}$ ) decreases. The measured four-photon interference fringe contrast drops to almost zero when photon A is almost fully distinguishable.

indistinguishabilities  $(M_{AB}, M_{BC}, M_{CD}, M_{DA})$  that are experimentally accessible, hold (see Appendix G):

$$c_1 \ge M_{AB} + M_{BC} + M_{CD} + M_{DA} - 3,$$
 (9)

$$c_1 \le \min(M_{AB}, M_{BC}, M_{CD}, M_{DA}).$$
 (10)

For the data presented in Fig. 3, the measured pairwise HOM visibilities (indistinguishabilities) are  $V_{\rm AB}=0.727\pm0.001~(M_{\rm AB}=0.760\pm0.002),~V_{\rm BC}=0.790\pm0.001~(M_{\rm BC}=0.825\pm0.002),~V_{\rm CD}=0.848\pm0.001~(M_{\rm CD}=0.884\pm0.002),~V_{\rm DA}=0.755\pm0.002~(M_{\rm DA}=0.789\pm0.003).$ 

In order to establish robust upper and lower bounds on  $c_1$ , we account for the experimental error in the measured indistinguishability values via a bootstrapping approach (see Appendix G). This provides upper and lower bounds on the four-photon indistinguishability of  $0.235 \le c_1 \le 0.766$ . The measured value  $c_1 = 0.61 \pm 0.01$  falls indeed within these bounds.

Secondly, we developed a model to simulate the experiment and explore the effect of experimental imperfections. In fact, the visibility of the multiphoton interference precisely corresponds to the parameter  $c_1$ , which is the multiphoton indistinguishability coefficient in the photonic density matrix of Eq. (5), only in the ideal situation outlined in Sec. II D. However, in a real experiment other physical effects can be responsible for a reduction in the measured visibility value. Some of these imperfections are intrinsically due to the source properties, such as multiphoton emission, while other ones may depend on the measurement apparatus, and include losses, imperfections of the fabricated interferometer, and unbalanced detection efficiencies. We developed a complete model to evaluate how such imperfections affect the measurement of the visibility and the extracted value of  $c_1$  (see Appendix H for more details). By using the actual parameters of the apparatus,

the model predicts a value of  $c_1 = 0.590 \pm 0.005$ , which is in good agreement with the experimental results. This value increases to  $c_1 = 0.661 \pm 0.006$  when only the partial photon distinguishability is included (deduced from the four accessible two-photon HOM measurements), while all other noise sources are neglected. This means that all other sources of imperfections contribute to a reduction of  $\sim 0.07$  in the measured value of  $c_1$ . More specifically, the main contribution to this reduction in the present experiment is found to be provided by multiphoton emission  $[q^{(2)}(0) \simeq 0.019 \neq 0]$ , while the effects of circuit errors and unbalanced detection efficiencies are negligible. This additional analysis allows us to evaluate the impact of each experimental imperfection, and provides a detailed benchmark for the performance of the experiment and photon source.

### C. Tuning indistinguishability

We measure how the visibility of the interference fringe varies when one of the photons is made gradually distinguishable. We plot in Figs. 4(a)–4(d) the four-photon interference fringes as we make photon A more and more distinguishable by rotating its polarization with a half wave plate (see arrow in Fig. 2). For each dataset we fit the interference fringe according to  $P' \propto 1 \pm c_1 \cos \alpha_1$  and extract  $c_1$ . The experimental values of  $c_1$  are plotted as a function of the minimum measured pairwise indistinguishability  $M_{\min}$  in Fig. 5(a) as black circles. We calculate the upper and lower bounds for the expected value of  $c_1$ from the two-photon overlaps, and these are shown as the shaded blue regions in the same graph. We also perform numerical simulations which account for experimental imperfections, as described before and more fully in Appendix H, and calculate the expected visibilities, which

## PDF page 10

FIG. 5. (a) Four-photon indistinguishability  $c_1$  as a function of the minimum pairwise indistinguishability  $M_{\min}$ . Black circles: experimental data, extracted from the visibility of the four-photon interference fringe. Orange squares: simulated interference visibility including all experimental imperfections. Green diamonds: simulated interference visibility only accounting for partial distinguishability of the input photons, and assuming zero multiphoton emission ( $g^{(2)} = 0$ ), an ideal interferometer, and perfect detection efficiency. Blue shaded regions: upper and lower bounds calculated from Eqs. (9) and (10) using the four measured pairwise indistinguishabilities. (b) Measured four-photon coincidence fringe as a function of the internal phase of the interferometer  $\alpha$  using a faster DMX to give access to a higher  $M_{\rm min} = 0.800 \pm 0.004$ . The visibility here is  $c_1 = 0.67 \pm 0.02$ . The purple points were obtained using a 12 pm Fabry-Perot etalon to spectrally filter the photons and improve the minimum pairwise indistinguishability to  $M_{\rm min} = 0.8727 \pm 0.0007$ . Only one phase value is sampled here, and we obtain a visibility of  $c_1 = 0.81 \pm 0.03$ .

are plotted as orange squares. In all cases, there is a very good agreement between the data and simulations. For comparison, we calculate the expected value of the visibility if only the partial indistinguishability of the photons was considered (i.e., a perfect interferometer and  $g^{(2)}=0$ ), and these values are plotted as green diamonds.

We finally increase the two-photon indistinguishability using two different methods, in order to explore higher values of  $M_{\rm min}$  and  $c_1$ . Firstly, we use the second version of the DMX which has a shorter operating time of  $\Delta T = 175$  ns. The maximum separation time between

the interfering photons is then 525 ns and therefore the minimal two-photon indistinguishability is higher at  $M_{\rm min} = 0.800 \pm 0.004$ , because of reduced spectral wandering of the quantum dot between the photon emissions. In this case we extract a four-photon indistinguishability of  $c_1 = 0.67 \pm 0.02$ . The experimental interference fringes are shown in Fig. 5(b), and the extracted value of  $c_1$  is also plotted in Fig. 5(a) together with the calculated bounds and simulated values. Secondly, we add a 12 pm Fabry-Perot etalon to spectrally filter the single-photon source. This decreases the effect that spectral wandering has on the twophoton indistinguishability by postselecting the singlephoton emission within a narrow bandwidth. However, this reduces the source brightness by approximately at factor of 3, which significantly decreases the four-photon coincidence rate; thus we characterize this condition only for  $\alpha_1 = 2\pi$  [see the purple dots in Fig. 5(b), which were acquired with an integration time of 16 h]. The minimum two-photon indistinguishability in the latter case is  $M_{\rm min} = 0.8727 \pm 0.0007$  and the experimental four-photon indistinguishability is  $c_1 = 0.81 \pm 0.03$ . As can be seen in Fig. 5(a) there is again a good agreement between the experiment and simulations for these data points.

### IV. CONCLUSIONS

We have proposed a robust way to measure the *genuine* n-photon indistinguishability of multiphoton states. Our method relies on a photonic circuit with 2n modes and a cyclic array of beam splitters. When n photons are injected in the circuit in specific input configurations, a quantum interference fringe is observed while scanning the internal phases of the device. In practice, we demonstrate that it is sufficient to harness a single phase term, governed by a single thermo-optic phase shifter fabricated upon one arm of the interferometer. The visibility of this fringe provides a direct quantification of the multiphoton indistinguishability.

Our experimental study with four photons demonstrates the reliability of our approach. In fact, the conducted measurements are shown to be very robust against the interferometer imperfections and allow access to the true multiphoton indistinguishability for photons of various quantum purity.

We emphasize that our CI can be scaled to an arbitrary number of modes, while keeping the same depth of only two layers of beam splitters and thus maintaining low optical loss. This makes it a powerful tool to characterize multiphoton indistinguishability for increasing number of photons, a key resource in photonic quantum technologies.

As a matter of fact, the estimation of the bounds to the genuine indistinguishability provided by pairwise Hong-Ou-Mandel experiments, as those discussed in Ref. [15], can be measured with high efficiency and could be preferred in some scenarios to evaluate quickly the photon-source performance. However, the separation between the estimated bounds, which corresponds to an uncertainty for

## PDF page 11

the measured indistinguishability, depends only on the characteristics of the photon states and cannot be improved by, e.g., a longer measurement. The method presented here provides a direct estimator of the genuine indistinguishability, which can be evaluated with arbitrarily good precision provided that the measurement is conducted for a sufficiently long time to accumulate statistics.

We believe this study may open new paths in fundamental research on quantum interference beyond photonics. Indeed, the novel design of our device shows that it is possible to access physical properties of a whole set of quantum particles, such as their genuine quantum indistinguishability, by overlapping their paths only pairwise in a cyclical way between next neighbors in the initial states, and by performing collective detection at the output. Further ramifications may be foreseen in the quantum metrology field. In fact, we provide here an example of a device whose properties (namely, its internal phases) are accessible and measurable only with states composed by a minimum number of photons, while they are transparent to Fock states with lower numbers.

#### ACKNOWLEDGMENTS

This work is supported by the European Union's Horizon 2020 Research and Innovation Programme under the PHOQUSING project GA No. 899544, by the European Union's Horizon 2020 Research and Innovation Programme QUDOT-TECH under the Marie Sklodowska-Curie Grant Agreement No. 861097, by the IAD-ANR (Agence de l'Innovation de Défense-Agence Nationale de la Recherche) support ASTRID program Projet No. ANR-18-ASTR-0024 LIGHT, by the QuantERA ERA-NET Cofund in Quantum Technologies project HIPHOP, by the French RENATECH network, and by the Paris Ile-de-France Région in the framework of DIM SIRTEQ. The interferometer fabrication was partially performed at PoliFAB, the microfabrication and nanofabrication facility of Politecnico di Milano. The authors would like to thank Mr. Clément Gouriou for stimulating discussions, and Igor Shavrin from Swabian Instruments for his assistance in setting up the data acquisition with a "Time Tagger 20" timeto-digital converter.

## APPENDIX A: INFLUENCE OF THE PHASE TERMS

Physical phase shifts, placed in one of the internal optical paths of a multimode interferometer, can affect the measurable output state in a way that is not straightforward. In addition, the observation that distinct phase shifters affect in a measurable way the output state does not mean that they are acting on independent parameters of the unitary transformation of the multimode device.

Here we exemplify these considerations in the simple case of a two-arm Mach-Zehnder interferometer, such as

FIG. 6. The Mach-Zehnder interferometers (a) and (b) are described by precisely the same unitary matrix  $U_{\rm MZI}$ . The interferometer in (c) is described instead by an equivalent matrix  $U'_{\rm MZI} = C \ U_{\rm MZI}$ , where C is a diagonal matrix with only phase terms.

the one depicted in Fig. 6(a). The device is composed of two symmetric beam splitters and two different phase plates in the internal arms. If we model the beam splitters with the matrix

$$U_{\rm BS} = \frac{\sqrt{2}}{2} \begin{bmatrix} 1 & i \\ i & 1 \end{bmatrix},\tag{A1}$$

the matrix of the full interferometer is calculated as

$$\begin{split} U_{\text{MZI}} &= U_{\text{BS}} \begin{bmatrix} e^{i\psi_1} & 0 \\ 0 & e^{i\psi_2} \end{bmatrix} U_{\text{BS}} \\ &= \frac{1}{2} \begin{bmatrix} e^{i\psi_1} - e^{i\psi_2} & i(e^{i\psi_1} + e^{i\psi_2}) \\ i(e^{i\psi_1} + ie^{i\psi_2}) & -e^{i\psi_1} + e^{i\psi_2} \end{bmatrix}. \end{split} \tag{A2}$$

It is clear that, in general, both varying  $\psi_1$  or  $\psi_2$  will have some measurable influence on the output state of the interferometer; in particular, a change in either of the two phases will produce interference fringes.

Let us now calculate the matrix of the other interferometer depicted in Fig. 6(b). Actually, one would observe that it is exactly the same as  $U_{\rm MZI}$ :

$$\begin{bmatrix} e^{i\psi_{2}} & 0 \\ 0 & e^{i\psi_{2}} \end{bmatrix} U_{\text{BS}} \begin{bmatrix} e^{i(\psi_{1}-\psi_{2})} & 0 \\ 0 & 1 \end{bmatrix} U_{\text{BS}}$$

$$= \frac{1}{2} \begin{bmatrix} e^{i\psi_{1}} - e^{i\psi_{2}} & i(e^{i\psi_{1}} + e^{i\psi_{2}}) \\ i(e^{i\psi_{1}} + ie^{i\psi_{2}}) & -e^{i\psi_{1}} + e^{i\psi_{2}} \end{bmatrix} = U_{\text{MZI}}.$$
 (A3)

The perfect correspondence between the two configurations of Figs. 6(a) and 6(b) can also be understood by analyzing the phase delays accumulated along the optical

## PDF page 12

paths. All possible paths result in either  $\psi_1$  or  $\psi_2$  delay in both configurations.

At this point, one would comment that the phases  $\psi_2$  at the outputs of the second Mach-Zehnder interferometer may be removed without altering the effective circuit operation on Fock states. This means that the interferometers in Figs. 6(a) and 6(b) are both equivalent to the one represented in Fig. 6(c), which is described by the matrix:

$$U'_{\text{MZI}} = \frac{1}{2} \begin{bmatrix} e^{i(\psi_1 - \psi_2)} - 1 & i(e^{i(\psi_1 - \psi_2)} + 1) \\ i(e^{i(\psi_1 - \psi_2)} + 1) & -e^{i(\psi_1 - \psi_2)} + 1 \end{bmatrix}. \quad (A4)$$

This also means that what is actually affecting the operation of this interferometer is the *phase difference*  $\psi_1 - \psi_2$  and not the two individual phases. In other terms, there is only one degree of freedom available for both of these elements.

# APPENDIX B: EQUIVALENT CYCLIC INTERFEROMETERS

We discuss in this appendix how to transform the general layout of CI shown in Fig. 1(b) into the simplified one of Fig. 1(c).

We consider the two procedures schematized in Fig. 7. In Fig. 7(a) it is shown how the phase delay  $\phi_B$ , placed on an odd mode 2m+1, can be removed (i.e., the phase on that arm can be set to zero), without any change in the matrix of the device. To do so, the phase  $\phi_A$  present on mode 2m is changed to  $\phi_A - \phi_B$ , and two phase shifts equal to  $\phi_B$  are added at the outputs 2m and 2m+1. One observes that, for any chosen couple of input and output ports, a photon traveling in the circuit undergoes the same overall phase delay in the two configurations. Since beam splitter operations have not changed, this means that the two configurations are described by precisely the same unitary matrix. The procedure shown in Fig. 7(b) is analogous to the one just

described, but applies to a phase delay  $\phi_B$  placed on an even mode 2m. In this case, the phase shifter  $\phi_A$  already present on mode 2m-1 is changed to  $\phi_A - \phi_B$ , and two phase shifters  $\phi_B$  are added at the inputs 2m-1 and 2m.

These two procedures can be applied alternately starting from the Nth mode up to the second mode of the CI in Fig. 1(b), producing an interferometer with all the phase terms on the internal arms set to zero, except for the phase  $\alpha_1$  on the first arm. Given the iterative simplification procedures that have been operated, the phase term  $\alpha_1$  contains an algebraic sum of all the phases  $\phi_i$  initially considered in the interferometer, as in Eq. (2). Then, the phase shifters at the inputs and at the outputs, represented with dashed contours, can be removed without changing the output distribution of the device (see also the example in Appendix A). This proves that the interferometer in Fig. 1(c) is equivalent to the one in Fig. 1(b), in the sense of Definition 1.

# APPENDIX C: ODD MODES TO ODD MODES DETECTION PROBABILITY

We consider in this appendix an experiment conducted using a CI with N=2n modes, in which n photons are injected one per each odd input mode, and n-photon coincidence detection is operated at the output, detecting one photon per each odd output mode.

### 1. Indistinguishable photons

If the n photons are perfectly identical, the probability to detect this output state is given by [40]

$$P_{\underline{g},\underline{h}} = \frac{|\operatorname{perm} S_{\underline{g},\underline{h}}|^2}{\mu_1!\mu_2!\cdots\mu_N!\nu_1!\nu_2!\cdots\nu_N!},$$
 (C1)

FIG. 7. Procedures for reducing the number of phase shifters in the device of Fig. 1(a), without changing its output distribution when Fock states are injected at the inputs. The procedures allow us to set to zero the phase term placed on one of the internal arms, by modifying the phase on the upper adjacent arm and by adding phase shifts at the inputs or at the outputs. Panels (a) and (b) hold, respectively, for odd and even arms.

## PDF page 13

where  $\mu_i$  and  $\nu_i$  are the number of particles present in mode i in the g and h states, respectively.  $S_{\underline{g},\underline{h}}$  is the scattering matrix with elements  $S_{i,j} = U_{h_i,g_j}$  (where U is the unitary matrix of the interferometer) and perm S denotes the permanent of the matrix S.

The elements of the  $n \times n$  scattering matrix S can be worked out by inspection of the interferometer layout, considering the attenuation and phase delays undergone by a photon in all the relevant optical paths. In detail, for the considered input and output states, the element  $S_{r,c}$  (with  $1 \le r \le n$  and  $1 \le c \le n$ ) is related to the path from the input port 2c - 1 to the output port 2c - 1 of the full device. Among the different equivalent interferometers, we refer to the one represented in Fig. 1(c).

A photon injected in the (2m-1)th mode can reach the (2m+1)th mode undergoing two 50% transmissions on the first and second beam splitters, each giving a phase delay equal to  $i=e^{i\pi/2}$  [we describe the beam splitters as in Eq. (A1)]. Thus,

$$S_{m+1,m} = \frac{1}{2}i^2 = -\frac{1}{2}, \qquad m \neq n, m \neq 1.$$
 (C2)

Alternatively, a photon from the same input may exit from the (2m-1)th mode undergoing two 50% reflections (each giving a null phase delay, according to our beam splitter model):

$$S_{m,m} = \frac{1}{2}, \qquad m \neq 1.$$
 (C3)

All other elements of the scattering matrix associated to this input are vanishing, because there are no other odd modes connected to it.

To complete the picture, we take into account the special case given by the first and by the (N-1)th inputs of the interferometer, which produce the following elements that do not obey to the previous rules:

$$S_{1,1} = \frac{1}{2}e^{i\alpha_1}, \qquad S_{1,n} = -\frac{1}{2}.$$
 (C4)

Finally, the scattering matrix S is given by

$$S = \frac{1}{2} \begin{bmatrix} e^{i\alpha_1} & & & & -1 \\ -1 & 1 & & & & \\ & -1 & 1 & & & \\ & & \ddots & \ddots & & \\ & & & \ddots & \ddots & \\ & & & &$$

which is essentially a bidiagonal matrix with an additional  $S_{1,n}$  element. The permanent of S can be developed as

follows, according to the Laplace formula (adapted to permanents):

$$\operatorname{perm} S = \frac{e^{i\alpha_{1}}}{2} \operatorname{perm} \frac{1}{2} \begin{bmatrix} 1 & & & \\ -1 & 1 & & & \\ & \ddots & \ddots & & \\ & & \ddots & \ddots & \\ & & & -1 & 1 \end{bmatrix}$$

$$-\frac{1}{2} \operatorname{perm} \frac{1}{2} \begin{bmatrix} -1 & 1 & & & \\ & -1 & 1 & & \\ & & -1 & 1 & & \\ & & & \ddots & \ddots & \\ & & & & \ddots & 1 \\ & & & & -1 \end{bmatrix}. \quad (C6)$$

Now, by applying recursively the Laplace formula it is not difficult to show that

$$\operatorname{perm} \frac{1}{2} \begin{bmatrix} 1 & & & & \\ -1 & 1 & & & \\ & \ddots & \ddots & & \\ & & \ddots & \ddots & \\ & & & -1 & 1 \end{bmatrix} = \left(\frac{1}{2}\right)^{n-1} \quad (C7)$$

and

$$\operatorname{perm} \frac{1}{2} \begin{bmatrix} -1 & 1 & & & \\ & -1 & 1 & & \\ & & \ddots & \ddots & \\ & & & \ddots & 1 \\ & & & & -1 \end{bmatrix} = \left( -\frac{1}{2} \right)^{n-1}, \quad (C8)$$

where n-1 is the dimension of the matrix. Hence, we obtain

perm 
$$S = \frac{1}{2^n} [e^{i\alpha_1} + (-1)^n].$$
 (C9)

As a consequence, the probability to detect the output state  $\underline{h} = (1, 3, 5, ...)$ , given the input state  $\underline{g} = (1, 3, 5, ...)$ , has the expression given by Eq. (3) and Proposition 3 is proven.

## PDF page 14

## 2. Distinguishable photons

If the photons injected in the odd modes are completely distinguishable, the probability to detect them at the output again on the odd modes is given by [40]

$$P_{\text{dist}} = \text{perm}\{|S_{i,i}|^2\}. \tag{C10}$$

Thus, we need to calculate

$$\operatorname{perm}\{|S_{i,j}|^2\} = \operatorname{perm} \frac{1}{2^2} \begin{bmatrix} 1 & & & & 1 \\ 1 & 1 & & & \\ & 1 & 1 & & \\ & & \ddots & \ddots & \\ & & & \ddots & \ddots & \\ & & & &$$

Proceeding similarly to the previous case, we have

$$\operatorname{perm}\{|S_{i,j}|^2\} = \frac{1}{4}\operatorname{perm}\frac{1}{4}\begin{bmatrix} 1 & & & \\ 1 & 1 & & \\ & \ddots & \ddots & \\ & & \ddots & \ddots \\ & & & 1 & 1 \end{bmatrix} \\ + \frac{1}{4}\operatorname{perm}\frac{1}{4}\begin{bmatrix} 1 & 1 & & \\ 1 & 1 & & \\ & & \ddots & \ddots & \\ & & & \ddots & \ddots \\ & & & \ddots & 1 \\ & & & \ddots & 1 \\ & & & \ddots & 1 \\ & & & & 1 \end{bmatrix}, \quad (C12)$$

where

$$\operatorname{perm} \frac{1}{4} \begin{bmatrix} 1 & & & & \\ 1 & 1 & & & \\ & \ddots & \ddots & & \\ & & \ddots & \ddots & \\ & & & 1 & 1 \end{bmatrix}$$

$$= \operatorname{perm} \frac{1}{4} \begin{bmatrix} 1 & 1 & & & \\ & 1 & 1 & & \\ & & \ddots & \ddots & \\ & & & \ddots & \ddots & \\ & & & \ddots & 1 & \\ & & & & 1 & 1 \end{bmatrix} = \left(\frac{1}{4}\right)^{n-1}. \quad (C13)$$

Therefore, we obtain

perm{
$$|S_{i,j}|^2$$
} =  $2\frac{1}{4} \left(\frac{1}{4}\right)^{n-1} = \frac{1}{2^{2n-1}}$ , (C14)

as in Eq. (7).

# APPENDIX D: GENERIC *n*-PHOTON INTERFERENCE FRINGES

We prove here Proposition 4, which we report again below for convenience. Proposition 4.—Given a N=2n mode CI, an n-photon interference fringe as a function of the internal phases can be measured if and only if the input state has precisely one photon per each pair of input ports  $(1,2)-\ldots-(2m-1,2m)-\ldots$  and the output state has precisely one photon per each pair of output ports  $(2,3)-\ldots-(2m,2m+1)-\ldots-(1,N)$ . In particular, for each input-output combination satisfying this rule, the detection probability takes the form:

$$P = \frac{1}{2^{2n-1}} [1 + (-1)^{n+p+q} \cos \alpha_1], \tag{D1}$$

where p is the number of occupied even modes in the input state, and q is the number of occupied even modes in the output state.

First, we prove that an input state with n photons that does not satisfy the above described condition will not produce any interference fringe, as a function of the internal phases of the CI.

Let us indeed consider an input state for which at least a given pair of inputs (2m-1, 2m) is empty. Then we can choose, as a model for the interferometer, the one having a single phase shifter  $\alpha_{2m-1}$  on the (2m-1)th mode: no photon of the input state would propagate across this arm, which means that varying its phase value would not give any interference fringe. An analogous reasoning can be

## PDF page 15

FIG. 8. (a) A photon that enters the upper port of a beam splitter, according to our modeling [Eq. (A1)], acquires  $\theta_1 = 0$  phase delay when exiting on the upper port, and  $\theta_1 = \pi/2$  phase delay when exiting on the lower port. (b) A photon that enters the lower port has the symmetric behavior. (c) Suitable phase shifters, placed on the input and output ports, make a photon entering the upper port to acquire the same phase delays as if it entered the lower one.

made, considering an output state with at least a given pair of outputs (2m, 2m + 1) empty. Choosing indeed the model of the interferometer that has a single phase shifter on mode 2m + 1, we observe that this phase shifter would not be able to influence any of the photons present in the output state.

Second, we prove that all the mentioned input and output states provide multiphoton interference fringes.

We know already (see Proposition 3, proved in Appendix C) that the couple of states  $\underline{g} = \underline{h} = (1,3,5,...)$  produces interference fringes as a function of the internal phases. Let us consider what happens when we change the position of one input photon of  $\underline{g}$  from an odd mode to the following even mode (i.e., from mode 2m - 1 to mode 2m). This pair of odd and even input modes of the interferometer correspond respectively to the upper and lower input modes of the same beam splitter, among the ones composing the first layer.

Since the beam splitter is balanced, the probability for a photon to exit in the upper or lower port of the beam splitter is the same, independently of the port from which it has entered. However, depending on the input, the phase acquired is different, according to the phase terms of the elements of the unitary matrix Eq. (1), as shown in Figs. 8(a) and 8(b). If we place suitable phase shifters as in Fig. 8(c), a photon entering the upper (odd) mode acquires at the two output arms the same phase delays as if it entered the lower (even) mode. One of such phase shifters, having value  $-\pi/2$ , is placed directly at the input port and cannot affect in any way the probability distribution of the photons at output of the complete interferometer.

FIG. 9. (a) A photon detected at the upper output port of a beam splitter acquires a total phase  $\theta_1' = \theta_1$  if it has entered the beam splitter from the upper input port carrying a phase  $\theta_1$ , or a phase  $\theta_1' = \theta_1$  if it has entered the beam splitter from the lower input port carrying a phase  $\theta_2$ . (b) Symmetric considerations can be made for a photon detected at the lower output port. (c) Suitable phase shifters can be added, to make the phases acquired by a photon detected on the upper output port equal to the ones that would have been acquired if detection occurred on the lower output port, as in case (b).

The other phase shifter, having value  $\pi$ , is instead added in the internal paths of the interferometer. In practice, exchanging the position of one of the input photons (within the same pair of allowed inputs) is equivalent to adding  $\pi$  to the internal phase  $\alpha_1$  in Eq. (3); we further note that adding  $\pi$  to  $\alpha_1$  is equivalent to a change of the sign of  $\cos \alpha_1$  in the formula.

A similar reasoning can be made regarding the change in the position of one photon of the output state, from an even mode to the following odd mode (i.e., from mode 2m to mode 2m + 1, with the exception of mode 2m = N which has to be exchanged with mode 1). This pair of odd and even input modes of the interferometer correspond respectively to the upper and lower input modes of one beam splitter of the second layer, looking at the full interferometer. Let  $\theta_1$  and  $\theta_2$  be the phases that a photon, entering respectively the upper and lower input ports of the beam splitter, has already acquired before entering. Upon detection on the upper output mode [Fig. 9(a)], the total phase is  $\theta_1' = \theta_1$  or  $\theta_2' = \theta_2 + \pi/2$ , respectively, depending on the input port. On the other hand, upon detection on the lower output mode [Fig. 9(b)], the total phase at the output is, respectively,  $\theta'_1 = \theta_1 + \pi/2$  or  $\theta'_2 = \theta_2$ . If we add suitable phase shifters on the upper input and output modes [Fig. 9(c)], we can make a photon detected on the upper mode acquire the same phases as if it were detected on the lower mode. The relevant phase shifter, with regard to the

## PDF page 16

FIG. 10. Schematic of the experimental setup to generate a single-photons stream. (a) The single-photons stream is generated by a quantum dot single-photons source based on a neutrally charged InGaAs quantum dot embedded in an electrically contacted micropillar ( $\emptyset = 2 \mu m$ ) cavity operating at  $\sim 5 \text{ K}$ . The QDSPS is excited using acoustic-phonon-assisted nearresonant ( $\Delta \lambda = 0.7$  nm) excitation [9] with a 15 ps pulsed (82 MHz) laser at  $\lambda = 924.4$  nm. We apply a voltage of V =-2.0 V to tune the QD into resonance with the cavity. The photons emitted at  $\lambda = 925.0$  nm are collected with a high numerical aperture (NA = 0.7) aspheric lens mounted inside the cryostat to mitigate mechanical noise. This excitation scheme allows us to reach a high polarized first lens brightness ( $\sim$ 19%), defined as the probability per pulse that a single photon is generated and exits the micropillar and reaches the aspheric lens. This is calculated by recording the generated rate of photons and accounting for the optical losses of the setup. We separate the single photon from the laser using three bandpass filters, resulting in a total suppression of the excitation laser of around 120 dB. This optical setup allows for a high fibered brightness ( $\sim$ 9.5%).

output photon distribution, is only the one that would be added on the internal arms of the full interferometer, i.e., the one at the input of the considered beam splitter, having a value of  $\pi$ . Also in this case, the addition of this phase term to the internal phase is equivalent to a change of the sign of  $\cos \alpha_1$  in Eq. (3).

We note that both the exchange operations discussed above, when they are performed on a state compatible with Proposition 4, produce again a state compatible with that proposition. More precisely, all the input and output states compatible with Proposition 4 can be transformed one into the other by a certain number of such exchange operations.

In particular, all the input states compatible with the proposition can be derived from the state  $\underline{g} = (1, 3, 5, ..., 2n-1)$  with p exchanges of photon position, and analogously all the relevant output states can be obtained from  $\underline{h} = (1, 3, 5, ..., 2n-1)$  with q exchanges. Each of these exchanges is associated to a sign change of the term  $\cos \alpha_1$ , resulting in a multiplicative factor  $(-1)^{p+q}$ .

One notes that p and q correspond to the number of occupied even modes in the input and output states, respectively, and proof of the proposition is completed.

# APPENDIX E: EXPERIMENTAL DETAILS OF THE PHOTON SOURCE

The single-photon source is based on a QD coupled to a micropillar cavity. The micropillar is fabricated from a planar sample embedding a  $\lambda$  cavity, surrounded by two DBRs (distributed Bragg reflectors) [GaAs/Al<sub>0.9</sub>Ga<sub>0.1</sub>As, with 14 (28) pairs for the top (bottom) mirror]. The  $\lambda$  cavity is made of a GaAs, with a single InGaAs QD, and a 20-nm-thick tunneling barrier of Al<sub>0.1</sub>Ga<sub>0.9</sub>As positioned 10 nm above the QD layer. The sample is doped to get an effective p-i-n diode structure and the micropillar is contacted to a larger structure for electrical contact, as shown in Fig. 10.

The electrically contacted micropillar fabricated using the *in situ* lithography technique [38,41] has a quality factor of  $Q \sim 2770$ . Using the Stark effect induced by the electrical field applied to the p-i-n diode we are able to tune the QD in resonance with the microcavity, yielding an emission lifetime of  $T_1 = 145$  ps and an indistinguishability of  $M_s = (92.3 \pm 0.1)\%$ . The potential difference also induces bending of the energy bands that flush all trapped charges, thus reducing the charge noise and spectral wandering of the emission [28].

We show in Table II the measured visibility (indistinguishability) of two photons emitted by the QDSPS as a function of the delay between their emission. The repetition rate of the laser is 82 MHz, which means the delay between a photon and the *p*th subsequent photon is a multiple of 12.2 ns.

Two different time-to-spatial demultiplexers are used to generate a four-photon state at the input of the CI, i.e., four photons synchronized in four different fibers, from a single-channel stream of photon at 82 MHz. Practically speaking, in both versions the stream of single photon is sent to a

TABLE II. Visibility (indistinguishability) of two photons emitted by the QDSPS as a function of the delay between their emission. The  $q^{(2)}(0)$  value is also specified.

| Delay (ns)             | $12.2 \pm 0.1$ | 175 ± 1        | 320 ± 1        | 525 ± 1        | 960 ± 1        |
|------------------------|----------------|----------------|----------------|----------------|----------------|
| Emitted photons        | 1              | 14             | 26             | 43             | 79             |
| $g^{(2)}(0)$ (%)       | $1.9 \pm 0.1$  | $1.7\pm0.1$    | $1.9\pm0.1$    | $1.7\pm0.1$    | $1.2 \pm 0.1$  |
| $V_{\mathrm{HOM}}$ (%) | $88.6 \pm 0.1$ | $86.4 \pm 0.4$ | $84.8 \pm 0.1$ | $76.9 \pm 0.4$ | $74.2 \pm 0.1$ |
| $M_s$ (%)              | $92.3\pm0.2$   | $89.6 \pm 0.2$ | $88.4 \pm 0.2$ | $80.0 \pm 0.2$ | $76.0 \pm 0.2$ |

## PDF page 17

free-space AOM driven by a varying rf signal acting as a switch between four different fibered outputs (see Fig. 2). What differs in the two versions is the switching time between two rf frequencies, and the total insertion loss. The first version (DMX4) is a prototype provided by Quandela as a proof of concept. The switching time between two rf frequencies, defined as the time to switch from 5% (channel off) to 95% (channel on) of maximal transmission, is of the order of 120 ns. The rf driver is set to a predefined frequency corresponding to diffraction to a given output for a duration  $\tau = 200$  ns. The operating time of one channel is thus  $\Delta T = 320$  ns, yielding a maximum delay between two photons of 960 ns. For this first version the total insertion loss (fiber to fiber) is  $\sim$ 3.5 dB. The second version (DMX6) is a commercially available rackable sixoutputs spatial demultiplexer loaned by Quandela. The design of the DMX has been revisited and optimized to reach a high mechanical stability, a low insertion loss, and a fast switching time. The switching time between two rf frequencies has been lowered to 60 ns. We address each output for  $\tau = 115$  ns so that the operating time is  $\Delta T =$ 175 ns and the maximal delay between photon is 525 ns. The total insertion loss is  $\sim 1.9$  dB.

### APPENDIX F: n < 4 PHOTON COINCIDENCES

We show experimentally that the global internal phase of the interferometer only gives rise to interference fringes for four-photon coincidences, as expected from the theory (see Proposition 2, Sec. II C).

While acquiring the four-photon coincidences we also monitor all two- and three-photon coincidences. We select here two particular four-channel output states of interest from Table I, namely (1, 3, 5, 7) and (1, 3, 5, 6), on which

FIG. 11. Normalized rate of four-photon coincidences as a function of the internal phase of the CI,  $\alpha_1$ , for two output modes corresponding to constructive (destructive) interference, compared to a selection of normalized two- and three-photon coincidences. Note that the two- and three-photon coincidences have been normalized by the mean number of two-photon and three-photon coincidences, respectively, and offset by a constant value so they do not overlap on the plot. The four-photon interference data in this graph are taken from Fig. 3.

we observe clear variation in the four-photon coincidences corresponding to constructive and destructive four-photon interference, respectively. We display the rate of two- and three-photon coincidences on various subsets of these channels, as we vary the internal phase: In Fig. 11 we show the normalized three-photon coincidence rate on channels (1, 3, 6) and (1, 3, 7), as well as the two-photon coincidence rate on channels (5, 6) and (5, 7). We observe no variation in the rate of two- and three-photon coincidences with the phase  $\alpha_1$ , as expected. Note that the same result is observed for all permutations of channels. We only plot a small selection here for clarity.

# APPENDIX G: BOUNDS FOR $c_1$ AND FOR UNMEASURED OVERLAPS

As discussed in Refs. [15,16,42], specific families of interferometers can be employed to perform n-photon indistinguishability tests based on the measurement of pairwise overlaps  $M_{ij}$  between the photons. The overlaps are related to the bunching probabilities  $p_{ij}^b$  in a 50/50 beam splitter as  $M_{ij} = 2p_{ij}^b - 1$ , and can be estimated from the Hong-Ou-Mandel visibilities  $V_{ij}$ . The possibility of bounding the value of *n*-photon indistinguishability is obtained by considering that certain families of interferometers can be described as graphs. More specifically, in interferometers performing measurement of pairwise HOM interference, nodes on the graphs can be associated to the different photons, while edges between two nodes correspond to the measurement of a HOM visibility between the corresponding particles. By considering a state model such as the one of Eq. (5), logical propositions associated to the graph structure can be used to provide bounds on  $c_1$  based on the measured overlaps. Notably, this methodology can be applied to the interferometer implemented in this paper which, besides allowing for fourphoton interference fringes, also performs two-photon HOM interference between certain pairs of input photons. By using the approach of Refs. [15,16,42], the graph edges can be mapped to logical propositions, which must satisfy an appropriate set of inequalities to represent a consistent set of probabilities. We obtain the following bounds for  $c_1$ based on the four overlaps for particles A, B, C, and D according to the notation in Fig. 3  $(M_{AB}, M_{BC}, M_{CD}, M_{DA})$ measured via the CI:

$$c_1 \ge M_{AB} + M_{BC} + M_{CD} + M_{DA} - 3,$$
 (G1)

$$c_1 \le \min(M_{AB}, M_{BC}, M_{CD}, M_{DA}), \tag{G2}$$

$$M_{AB} + M_{BC} - 1 \le M_{AC} \le 1 - |M_{AB} - M_{BC}|,$$
 (G3)

$$M_{\rm BC} + M_{\rm CD} - 1 \le M_{\rm BD} \le 1 - |M_{\rm BC} - M_{\rm CD}|.$$
 (G4)

## PDF page 18

FIG. 12. Schematic and synoptic view on the parameters involved to model the action of multiphoton emission, circuit errors, losses, and unbalanced detection on the performed experiment to retrieve indistinguishability  $c_1$ . The modeling of each noise contribution and their respective relevant parameters are detailed in the text of Appendix H. The estimated values  $c_1^{\text{mod}}$  turning on successive noise contributions in the model are given in Table IV which also specifies the values of the parameters used in each case.

To estimate the upper and lower bounds from experimentally estimated overlaps, which are affected by measurement error, we have applied a bootstrapping approach. More specifically, we generate  $10^4$  sets of the four indistinguishability values with a normal distribution matching the experimentally obtained mean and standard deviation, and then calculate the upper and lower bound for each set  $\{c_{1\min}(i), c_{1\max}(i)\}$  using Eqs. (9) and (10), respectively. We then take the lower bound as  $c_{1\min} = \max\{c_{1\min}(i)\} - 3 \text{ s.d.}\{c_{1\min}(i)\}$ ,  $c_{1\max} = \max\{c_{1\max}(i)\} + 3 \text{ s.d.}\{c_{1\max}(i)\}$ .

# APPENDIX H: MODELING EXPERIMENTAL IMPERFECTIONS

Here we discuss a model to take into account the effect of experimental imperfections in the estimation of  $c_1$ . In particular, we consider different effects that influence the measured value of  $c_1$  following the method described in the main text. A schematic representation of the full model is shown in Fig. 12 that displays the relevant parameters that we detail and explain below. The main source of deviation of the estimate from the true  $c_1$  value is multiphoton emission, i.e., the nonzero probability that the source emits more than one photon per mode  $(p_2)$ . We then consider and include the effect of losses  $(\eta)$  within the apparatus, the presence of fabrication errors in the integrated device  $[U_{\rm eff}(\alpha_1)]$ , and unbalanced detection efficiencies  $(\eta_i)$ . Note that in the model we have also included the effect of partial photon distinguishability  $(\rho_x^{(4)})$ , which is the actual physical effect that the experiment aims at reconstructing via the estimation of the parameter  $c_1$ . A detailed description of how these effects are included in the model is reported below.

Multiphoton emission and losses.—Let us consider that the photon source has a nonzero  $g^{(2)}(0)$ . The state generated by the source, on each time bin (separated by 12.2 ns) before demultiplexing, can be written as


$$\rho_i = p_0 |0_i\rangle\langle 0_i| + p_1 |1_i\rangle\langle 1_i| + p_2 |(1,\tilde{1})_i\rangle\langle (1,\tilde{1})_i|.$$
 (H1)

Here,  $|k_i\rangle$  stands for k photons on mode i, while  $p_0$ ,  $p_1$ , and  $p_2$  are the probabilities of having 0, 1, and 2 photons in a single time bin, respectively. Their values can be obtained from the source brightness  $B \sim p_1 + p_2$  and from the  $g^{(2)}(0)$  parameter as  $g^{(2)}(0) = 2p_2/(p_1 + 2p_2)^2$  by direct calculation from the definition  $g^{(2)}(0) = \langle n(n-1)\rangle/\langle n\rangle^2$ . Notation  $|(1,\tilde{1})_i\rangle$  describes the emission of two photons in the same time bin, corresponding to the addition of a noise photon to the principal one. Within this model, we will neglect higher-order noise terms. For quantum dot sources [14], the overlap of such noise photon with the principal one can be approximated to  $\sim$ 0; that is, the noise photon  $(\tilde{1})$  is distinguishable from the others (1) [14]. The complete input state after demultiplexing can be written as a density matrix:

$$\rho^{(4)} = \rho_1 \rho_3 \rho_5 \rho_7, \tag{H2}$$

where  $\rho_i$  is the incoherent mixture of Eq. (H1). For the low values of  $g^{(2)}(0)$  attained by the source described in this paper,  $p_2$  is small with respect to  $p_1$ . It is then possible to neglect all terms with more than one noise photon in state  $\rho^{(4)}$ . By further keeping only terms with at least four photons (that are the only relevant ones for the four-photon coincidence measurements), the density matrix can thus be approximated as

## PDF page 19

TABLE III. Configurations providing contributions to the input-output probability, in the presence of multiphoton emission and losses, for output modes (1, 3, 5, 7). Analogous tables can be constructed for each set of 4 output modes.

| Input configuration                                             | Output configuration                                          |  |  |
|-----------------------------------------------------------------|---------------------------------------------------------------|--|--|
| (1, 0, 1, 0, 1, 0, 1, 0)                                        | (1, 0, 1, 0, 1, 0, 1, 0)                                      |  |  |
| (2, 0, 1, 0, 1, 0, 0, 0) + permutations on modes $(1, 3, 5, 7)$ | (1, 0, 1, 0, 1, 0, 1, 0)                                      |  |  |
| (2, 0, 2, 0, 0, 0, 0, 0) + permutations on modes (1, 3, 5, 7)   | (1, 0, 1, 0, 1, 0, 1, 0)                                      |  |  |
| (2, 0, 1, 0, 1, 0, 1, 0) + permutations on modes $(1, 3, 5, 7)$ | (2, 0, 1, 0, 1, 0, 1, 0) + permutations on modes (1, 3, 5, 7) |  |  |
| (2, 0, 2, 0, 1, 0, 0, 0) + permutations on modes $(1, 3, 5, 7)$ | (2, 0, 1, 0, 1, 0, 1, 0) + permutations on modes (1, 3, 5, 7) |  |  |

$$\begin{split} \rho^{(4)} &\sim p_1^4 | 1_1, 1_3, 1_5, 1_7 \rangle \langle 1_1, 1_3, 1_5, 1_7 | \\ &+ p_0 p_1^2 p_2 \{ | (1, \tilde{1})_1, 0_3, 1_5, 1_7 \rangle \langle (1, \tilde{1})_1, 0_3, 1_5, 1_7 | \\ &+ | (1, \tilde{1})_1, 1_3, 0_5, 1_7 \rangle \langle (1, \tilde{1})_1, 1_3, 0_5, 1_7 | + \ldots \} \\ &+ p_1^3 p_2 \{ | (1, \tilde{1})_1, 1_3, 1_5, 1_7 \rangle \langle (1, \tilde{1})_1, 1_3, 1_5, 1_7 | \\ &+ | 1_1, (1, \tilde{1})_3, 1_5, 1_7 \rangle \langle 1_1, (1, \tilde{1})_3, 1_5, 1_7 | + \ldots \}, \end{split}$$
 (H3)

where all possible permutations have to be included in the parentheses.

Up to now we have neglected the effect of losses. If losses are almost equally distributed among the arms of the interferometer, we can apply the results of Ref. [43]. In this case, losses commute with linear optical elements, including demultiplexing and detection efficiencies. Thus, we can equivalently put all the losses occurring in the apparatus right before the input of the eight-mode interferometer, by defining the overall transmission parameter  $\eta$  (per photon). The state after losses can be written as the sum of different contributions:

$$\begin{split} \rho^{(4),\eta} &= [p_1^4 \eta^4 + 4 p_1^3 p_2 \eta^4 (1 - \eta)] |1_1, 1_3, 1_5, 1_7 \rangle \langle 1_1, 1_3, 1_5, 1_7 |\\ &+ [p_1^3 p_2 \eta^4 (1 - \eta)] \{ |\tilde{1}_1, 1_3, 1_5, 1_7 \rangle \langle \tilde{1}_1, 1_3, 1_5, 1_7 | + |1_1, \tilde{1}_3, 1_5, 1_7 \rangle \langle 1_1, \tilde{1}_3, 1_5, 1_7 | + \cdots \}\\ &+ [p_0 p_1^2 p_2 \eta^4 + p_1^3 p_2 \eta^4 (1 - \eta)] \{ |(1, \tilde{1})_1, 0_3, 1_5, 1_7 \rangle \langle (1, \tilde{1})_1, 0_3, 1_5, 1_7 | + |(1, \tilde{1})_1, 1_3, 0_5, 1_7 \rangle \langle (1, \tilde{1})_1, 1_3, 0_5, 1_7 | + \cdots \}\\ &+ [p_1^3 p_2 \eta^5] \{ |(1, \tilde{1})_1, 1_3, 1_5, 1_7 \rangle \langle (1, \tilde{1})_1, 1_3, 1_5, 1_7 | + |1_1, (1, \tilde{1})_3, 1_5, 1_7 \rangle \langle 1_1, (1, \tilde{1})_3, 1_5, 1_7 | + \cdots \}, \end{split}$$
 (H4)

where the states are written according to the notation described above.

The first three groups of terms correspond to states with four input photons on the device, and will provide a contribution to the detection of a given four-photon event whenever the corresponding probability is nonzero. Conversely, the last terms correspond to five input photons on the device. By considering that SNSPDs are nonphoton number resolving detectors, it is necessary to consider that they can provide nonzero contribution to four-detector clicks in different cases. For instance, let us take output modes (1, 3, 5, 7). A nonzero contribution is obtained for the five-photon terms when one of the following output configurations is obtained:


$$(2,0,1,0,1,0,1,0),$$
  $(1,0,2,0,1,0,1,0),$   $(1,0,1,0,2,0,1,0,1,0,2,0),$   $(H5)$ 

where  $(i_1, i_2, ..., i_8)$  stand for  $i_k$  photons on output mode k (see the second line of Table III).

The overall output probability is finally retrieved by summing up all probabilities corresponding to terms and weights of Eq. (H4), by considering for five-photon terms all possible configurations yielding to a useful signal according to Eq. (H5).

Partial photon distinguishability.—To include the effect of partial photon distinguishability, one can rely on different papers discussing such effect in a boson sampling framework [44–46]. These models substantially take into account that indistinguishability between the particles is described by a Hermitian matrix  $S_{ij}$ , representing the set of pairwise overlaps. In general, one has  $|S_{ij}| \leq 1$  (for  $i \neq j$ ), while  $S_{ij} = 1$  is obtained when photons i and j are indistinguishable. Such overlaps can be different for each photon pair, and include all degrees of freedom that add distinguishability to the generated photon state. Notably, HOM pairwise visibility between particles i and j provides information on the moduli  $|S_{ij}|$ , while it is insensitive to the complex phases.

We have assumed, in our model, the simplified scenario where  $S_{ij}$  are real numbers. Furthermore, we have considered a description where each principal photon has a probability  $x_i$  to be indistinguishable, and a probability  $(1-x_i)$  to be fully distinguishable from the others. As

## PDF page 20

TABLE IV. Results of the numerical simulation for the experiment modeling. In particular, we have progressively added noise contributions for the configuration detailed in Sec. III B leading to an experimental value of  $c_1 = 0.61 \pm 0.01$ . The corresponding parameters for such simulation are reported here. Brightness:  $B \sim 0.098$ . Second-order correlation:  $g^{(2)}(0) = 0.019 \pm 0.001$ . Directional coupler (DC) transmissivities:  $T_1 \sim 0.503$ ,  $T_2 \sim 0.508$ ,  $T_3 \sim 0.505$ ,  $T_4 \sim 0.507$ ,  $T_5 \sim 0.506$ ,  $T_6 \sim 0.512$ ,  $T_7 \sim 0.5045$ ,  $T_8 \sim 0.534$ . Indistinguishability parameters:  $x_A \sim 0.852$ ,  $x_B \sim 0.883$ ,  $x_C \sim 0.941$ ,  $x_D \sim 0.932$ . Detection imbalance:  $\tilde{\eta}_1 = 0.92$ ,  $\tilde{\eta}_2 = 0.90$ ,  $\tilde{\eta}_3 = 0.92$ ,  $\tilde{\eta}_4 = 0.91$ ,  $\tilde{\eta}_5 = 0.90$ ,  $\tilde{\eta}_6 = 0.90$ ,  $\tilde{\eta}_7 = 0.90$ ,  $\tilde{\eta}_8 = 0.90$ . Effective losses:  $\eta \sim 0.25$  are included in all simulations. Similar analyses are shown in Sec. III C, Fig. 5, for other indistinguishability configurations.

| $c_1^{\rm mod}$   | Partial distinguishability | Multiphoton terms | Imperfect DC | Unbalanced detection |
|-------------------|----------------------------|-------------------|--------------|----------------------|
| $0.661 \pm 0.006$ | Yes                        | No                | No           | No                   |
| $0.592 \pm 0.005$ | Yes                        | Yes               | No           | No                   |
| $0.591 \pm 0.005$ | Yes                        | Yes               | Yes          | No                   |
| $0.590 \pm 0.005$ | Yes                        | Yes               | Yes          | Yes                  |

shown in the main text, this specific choice is able to provide an accurate description of our multiphoton experiment, performed with the QDSPS and the CI device. Thus, the density matrix of the input state  $\rho^{(4)}$ , and  $\rho^{(4),\eta}$  after including the effective action of losses, has to be replaced with effective states  $\rho_{\mathbf{x}}^{(4)}$  and  $\rho_{\mathbf{x}}^{(4),\eta}$ , where  $\mathbf{x}$  is the vector of parameters  $(x_{\mathbf{A}}, x_{\mathbf{B}}, x_{\mathbf{C}}, x_{\mathbf{D}})$ . Conversely, noise photons are considered fully distinguishable, thus corresponding to a value  $\tilde{x} = 0$ .

Circuit parameters.—Circuit errors can be introduced in the presence of fabrication imperfections. The relevant error to be considered in the model corresponds to directional couplers with transmissivities different from the expected value  $T_j=0.5$ . Losses can be included in the parameter  $\eta$  discussed above. The values of the different transmissivities  $T_j$  for the eight directional couplers implemented in the structure have been characterized before the experiment, and are reported in Table IV. Their values can be used to correct the effective unitary transformation  $U_{\rm eff}(\alpha_1)$  implemented by the integrated device. This effective matrix is used to calculate the output probabilities in the model.

Unbalanced detection efficiencies.—Finally, we can include the action of unbalanced detection efficiencies. This is performed by considering that detection efficiency for each output mode can be written as  $\eta_i = \eta_0 \tilde{\eta}_i$ , where  $\eta_0$ is equal for all the modes, while  $\tilde{\eta}_i$  represents the imbalance. Note that by construction,  $\max_i \tilde{\eta}_i = 1$ . Starting from this equation, we observe that  $\eta_0$  is a common set of balanced losses that can be included within the parameter  $\eta$ discussed above. Conversely, the imbalance  $\tilde{\eta}_i$  are included by considering that each detector clicks with probability  $p_i(n_i) = 1 - (1 - \tilde{\eta}_i)^{n_i}$ , where  $n_i$  is the number of impinging photons. Output probabilities obtained from the calculations can thus be corrected accordingly, by adding the imbalance in the transition probabilities from the input states of the density matrix expansion in Eq. (H4) and the corresponding output configuration.

Numerical simulations.—Starting from the model described above, we have performed some numerical

simulations to investigate how such errors affect the measurement of  $c_1$ . Such a parameter  $c_1$  is indeed retrieved in the experiment from the visibility of the output probabilites as a function of  $\alpha_1$ , that is, the internal phase of the interferometer. In particular, in the experiment we have summed up all eight output configurations varying as  $1 + c_1 \cos(\alpha_1)$ , and all eight terms changing as varying as  $1 - c_1 \cos(\alpha_1)$  to obtain the final estimate of  $c_1$ . We have thus performed a full numerical simulation of the experiment, which allowed us to evaluate the contribution of each term to the measured value of  $c_1$ .

As a first step, parameters  $p_0$ ,  $p_1$ ,  $p_2$  have been obtained by considering the actual source brightness B, and the value of  $g^{(2)}(0)$ . Regarding losses, transmission parameter  $\eta$  has been chosen to obtain the measured single-photon count rate (thus including an effective transmission parameter for the demultiplexing stage). Conversely, the imbalance  $\tilde{\eta}_i$  in detection efficiencies and the directional coupler transmittivities have been directly calibrated in the setup.

The first stage of the simulation corresponds to finding an estimate of parameters  $x_i$  describing partial photon distinguishabilities for modes (A, B, C, D). This can be performed by considering that those parameters are strictly related to the two-photon overlaps  $M_{ij} = x_i x_j$ , and can thus be retrieved from the measured visibilities  $V_{ij} = (V_{AB}, V_{BC}, V_{CD}, V_{DA})$ , by including the effect of  $g^{(2)}(0)$  to find the intrinsic indistinguishability  $M_{ij}$  as discussed in Ref. [14], and by correcting for imperfect directional couplers.

Then, we have performed a full simulation of the experiment for the estimate of  $c_1$  according to the model above. As an example, in Table IV we report the effect of each contribution on one of the experimental points reported in the paper, corresponding to  $V_{\rm AB}=0.727\pm0.001~(M_{\rm AB}=0.760\pm0.002), V_{\rm BC}=0.790\pm0.001~(M_{\rm BC}=0.825\pm0.002), V_{\rm CD}=0.848\pm0.001~(M_{\rm CD}=0.884\pm0.002), V_{\rm DA}=0.755\pm0.002~(M_{\rm DA}=0.789\pm0.003),$  corresponding to an extracted value of  $c_1=0.61\pm0.01$ . By including all effects, the predicted value of  $c_1^{\rm mod}$  is  $c_1^{\rm mod}\sim0.590\pm0.005,$  in good agreement with the experimental measurement. For this value, the major

## PDF page 21

contribution ∼0.07 derives from multiphoton emission, while a minor correction is provided by imperfect directional couplers (∼0.001) and unbalanced detection efficiencies (∼0.001).

- [1] D. J. Brod, E. F. Galvão, A. Crespi, R. Osellame, N. Spagnolo, and F. Sciarrino, Photonic Implementation of Boson Sampling: A Review, Adv. Photonics 1[, 034001 \(2019\)](https://doi.org/10.1117/1.AP.1.3.034001).
- [2] H.-S. Zhong, H. Wang, Y.-H. Deng, M.-C. Chen, L.-C. Peng, Y.-H. Luo, J. Qin, D. Wu, X. Ding, Y. Hu et al., Quantum Computational Advantage Using Photons, Science 370[, 1460 \(2020\).](https://doi.org/10.1126/science.abe8770)
- [3] H.-S. Zhong, Y.-H. Deng, J. Qin, H. Wang, M.-C. Chen, L.-C. Peng, Y.-H. Luo, D. Wu, S.-Q. Gong, H. Su et al., Phase-Programmable Gaussian Boson Sampling Using Stimulated Squeezed Light, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.127.180502) 127, 180502 [\(2021\).](https://doi.org/10.1103/PhysRevLett.127.180502)
- [4] J. B. Spring, P. L. Mennea, B. J. Metcalf, P. C. Humphreys, J. C. Gates, H. L. Rogers, C. Söller, B. J. Smith, W. S. Kolthammer, P. G. R. Smith, and I. A. Walmsley, Chip-Based Array of Near-Identical, Pure, Heralded Single-Photon Sources, Optica 4[, 90 \(2017\).](https://doi.org/10.1364/OPTICA.4.000090)
- [5] F. Kaneda and P. G. Kwiat, High-Efficiency Single-Photon Generation via Large-Scale Active Time Multiplexing, [Sci.](https://doi.org/10.1126/sciadv.aaw8586) Adv. 5[, eaaw8586 \(2019\)](https://doi.org/10.1126/sciadv.aaw8586).
- [6] P. Senellart, G. Solomon, and A. White, High-Performance Semiconductor Quantum-Dot Single-Photon Sources, [Nat.](https://doi.org/10.1038/nnano.2017.218) Nanotechnol. 12[, 1026 \(2017\)](https://doi.org/10.1038/nnano.2017.218).
- [7] H. Wang, Y.-M. He, T.-H. Chung, H. Hu, Y. Yu, S. Chen, X. Ding, M.-C. Chen, J. Qin, X. Yang et al., Towards Optimal Single-Photon Sources from Polarized Microcavities, [Nat.](https://doi.org/10.1038/s41566-019-0494-3) Photonics 13[, 770 \(2019\)](https://doi.org/10.1038/s41566-019-0494-3).
- [8] N. Tomm, A. Javadi, N. O. Antoniadis, D. Najer, M. C. Lobl, A. R. Korsch, R. Schott, S. R. Valentin, A. D. Wieck, A. Ludwig, and R. J. Warburton, A Bright and Fast Source of Coherent Single Photons, [Nat. Nanotechnol.](https://doi.org/10.1038/s41565-020-00831-x) 16, 399 [\(2021\).](https://doi.org/10.1038/s41565-020-00831-x)
- [9] S. E. Thomas, M. Billard, N. Coste, S. C. Wein, Priya, H. Ollivier, O. Krebs, L. Tazaïrt, A. Harouri, A. Lemaitre, I. Sagnes, C. Anton, L. Lanco, N. Somaschi, J. C. Loredo, and P. Senellart, Bright Polarized Single-Photon Source Based on a Linear Dipole, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.126.233601) 126, 233601 [\(2021\).](https://doi.org/10.1103/PhysRevLett.126.233601)
- [10] C. K. Hong, Z. Y. Ou, and L. Mandel, Measurement of Subpicosecond Time Intervals between Two Photons by Interference, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.59.2044) 59, 2044 (1987).
- [11] A. J. Menssen, A. E. Jones, B. J. Metcalf, M. C. Tichy, S. Barz, W. S. Kolthammer, and I. A. Walmsley, Distinguishability and Many-Particle Interference, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.118.153603) 118[, 153603 \(2017\).](https://doi.org/10.1103/PhysRevLett.118.153603)
- [12] K. A. Fischer, R. Trivedi, and D. Lukin, Particle Emission from Open Quantum Systems, [Phys. Rev. A](https://doi.org/10.1103/PhysRevA.98.023853) 98, 023853 [\(2018\).](https://doi.org/10.1103/PhysRevA.98.023853)
- [13] R. Trivedi, K. A. Fischer, J. Vučković, and K. Müller, Generation of Non-Classical Light Using Semiconductor Quantum Dots, [Adv. Quantum Technol.](https://doi.org/10.1002/qute.201900007) 3, 1900007 (2020).
- [14] H. Ollivier, S. E. Thomas, S. C. Wein, I. M. de Buy Wenniger, N. Coste, J. C. Loredo, N. Somaschi,

- A. Harouri, A. Lemaitre, I. Sagnes, L. Lanco, C. Simon, C. Anton, O. Krebs, and P. Senellart, Hong-Ou-Mandel Interference with Imperfect Single Photon Sources, [Phys.](https://doi.org/10.1103/PhysRevLett.126.063602) Rev. Lett. 126[, 063602 \(2021\).](https://doi.org/10.1103/PhysRevLett.126.063602)
- [15] T. Giordani, D. J. Brod, C. Esposito, N. Viggianiello, M. Romano, F. Flamini, G. Carvacho, N. Spagnolo, E. F. Galvão, and F. Sciarrino, Experimental Quantification of Four-Photon Indistinguishability, [New J. Phys.](https://doi.org/10.1088/1367-2630/ab7a30) 22, 043001 [\(2020\).](https://doi.org/10.1088/1367-2630/ab7a30)
- [16] D. J. Brod, E. F. Galvão, N. Viggianiello, F. Flamini, N. Spagnolo, and F. Sciarrino, Witnessing Genuine Multiphoton Indistinguishability, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.122.063602) 122, 063602 [\(2019\).](https://doi.org/10.1103/PhysRevLett.122.063602)
- [17] M. C. Tichy, M. Tiersch, F. de Melo, F. Mintert, and A. Buchleitner, Zero-Transmission Law for Multiport Beam Splitters, Phys. Rev. Lett. 104[, 220405 \(2010\).](https://doi.org/10.1103/PhysRevLett.104.220405)
- [18] A. Crespi, Suppression Laws for Multiparticle Interference in Sylvester Interferometers, [Phys. Rev. A](https://doi.org/10.1103/PhysRevA.91.013811) 91, 013811 [\(2015\).](https://doi.org/10.1103/PhysRevA.91.013811)
- [19] C. Dittel, R. Keil, and G. Weihs, Many-Body Quantum Interference on Hypercubes, [Quantum Sci. Technol.](https://doi.org/10.1088/2058-9565/aa540c) 2, [015003 \(2017\).](https://doi.org/10.1088/2058-9565/aa540c)
- [20] C. Dittel, G. Dufour, M. Walschaers, G. Weihs, A. Buchleitner, and R. Keil, Totally Destructive Many-Particle Interference, Phys. Rev. Lett. 120[, 240404 \(2018\)](https://doi.org/10.1103/PhysRevLett.120.240404).
- [21] N. Viggianiello, F. Flamini, L. Innocenti, D. Cozzolino, M. Bentivegna, N. Spagnolo, A. Crespi, D. J. Brod, E. F. Galvão, R. Osellame et al., Experimental Generalized Quantum Suppression Law in Sylvester Interferometers, New J. Phys. 20[, 033017 \(2018\)](https://doi.org/10.1088/1367-2630/aaad92).
- [22] A. Crespi, R. Osellame, R. Ramponi, M. Bentivegna, F. Flamini, N. Spagnolo, N. Viggianiello, L. Innocenti, P. Mataloni, and F. Sciarrino, Suppression Law of Quantum States in a 3D Photonic Fast Fourier Transform Chip, [Nat.](https://doi.org/10.1038/ncomms10469) Commun. 7[, 10469 \(2016\)](https://doi.org/10.1038/ncomms10469).
- [23] M. C. Tichy, K. Mayer, A. Buchleitner, and K. Mølmer, Stringent and Efficient Assessment of Boson-Sampling Devices, Phys. Rev. Lett. 113[, 020502 \(2014\)](https://doi.org/10.1103/PhysRevLett.113.020502).
- [24] N. Viggianiello, F. Flamini, M. Bentivegna, N. Spagnolo, A. Crespi, D. J. Brod, E. F. Galvão, R. Osellame, and F. Sciarrino, Optimal Photonic Indistinguishability Tests in Multimode Networks, [Science bulletin](https://doi.org/10.1016/j.scib.2018.10.009) 63, 1470 (2018).
- [25] J. Münzberg, C. Dittel, M. Lebugle, A. Buchleitner, A. Szameit, G. Weihs, and R. Keil, Symmetry Allows for Distinguishability in Totally Destructive Many-Particle Interference, PRX Quantum 2[, 020326 \(2021\)](https://doi.org/10.1103/PRXQuantum.2.020326).
- [26] A. E. Jones, A. J. Menssen, H. M. Chrzanowski, T. A. W. Wolterink, V. S. Shchesnovich, and I. A. Walmsley, Multiparticle Interference of Pairwise Distinguishable Photons, Phys. Rev. Lett. 125[, 123603 \(2020\).](https://doi.org/10.1103/PhysRevLett.125.123603)
- [27] R. van der Meer, P. Hooijschuur, F. H. Somhorst, P. Venderbosch, M. de Goede, B. Kassenberg, H. Snijders, C. Taballione, J. Epping, H. v. d. Vlekkert et al., Experimental Demonstration of an Efficient, Semi-Device-Independent Photonic Indistinguishability Witness, [arXiv:](https://arXiv.org/abs/2112.00067) [2112.00067.](https://arXiv.org/abs/2112.00067)
- [28] N. Somaschi, V. Giesz, L. De Santis, J. C. Loredo, M. P. Almeida, G. Hornecker, S. L. Portalupi, T. Grange, C. Antón, J. Demory, C. Gómez, I. Sagnes, N. D. Lanzillotti-Kimura, A. Lemaítre, A. Auffeves, A. G. White, L. Lanco, and

## PDF page 22

- P. Senellart, Near-Optimal Single-Photon Sources in the Solid State, [Nat. Photonics](https://doi.org/10.1038/nphoton.2016.23) 10, 340 (2016).
- [29] T. Meany, M. Gräfe, R. Heilmann, A. Perez-Leija, S. Gross, M. J. Steel, M. J. Withford, and A. Szameit, Laser Written Circuits for Quantum Photonics, [Laser Photonics Rev.](https://doi.org/10.1002/lpor.201500061) 9, [363 \(2015\)](https://doi.org/10.1002/lpor.201500061).
- [30] G. Corrielli, A. Crespi, and R. Osellame, Femtosecond Laser Micromachining for Integrated Quantum Photonics, [Nanophotonics](https://doi.org/10.1515/nanoph-2021-0419) 10, 3789 (2021).
- [31] J. G. Rarity, P. R. Tapster, E. Jakeman, T. Larchuk, R. A. Campos, M. C. Teich, and B. E. A. Saleh, Two-Photon Interference in a Mach-Zehnder Interferometer, [Phys.](https://doi.org/10.1103/PhysRevLett.65.1348) Rev. Lett. 65[, 1348 \(1990\)](https://doi.org/10.1103/PhysRevLett.65.1348).
- [32] W. R. Clements, P. C. Humphreys, B. J. Metcalf, W. S. Kolthammer, and I. A. Walmsley, Optimal Design for Universal Multiport Interferometers, Optica 3[, 1460](https://doi.org/10.1364/OPTICA.3.001460) [\(2016\).](https://doi.org/10.1364/OPTICA.3.001460)
- [33] A. Laing and J. L. O'Brien, Super-Stable Tomography of Any Linear Optical Device, [arXiv:1208.2868.](https://arXiv.org/abs/1208.2868)
- [34] V. S. Shchesnovich, Sufficient Condition for the Mode Mismatch of Single Photons for Scalability of the Boson-Sampling Computer, Phys. Rev. A 89[, 022333 \(2014\).](https://doi.org/10.1103/PhysRevA.89.022333)
- [35] F. Flamini, L. Magrini, A. S. Rab, N. Spagnolo, V. D'Ambrosio, P. Mataloni, F. Sciarrino, T. Zandrini, A. Crespi, R. Ramponi et al., Thermally Reconfigurable Quantum Photonic Circuits at Telecom Wavelength by Femtosecond Laser Micromachining, [Light Sci. Appl.](https://doi.org/10.1038/lsa.2015.127) 4, [e354 \(2015\).](https://doi.org/10.1038/lsa.2015.127)
- [36] F. Ceccarelli, S. Atzeni, A. Prencipe, R. Farinaro, and R. Osellame, Thermal Phase Shifters for Femtosecond Laser Written Photonic Integrated Circuits, [J. Lightwave Technol.](https://doi.org/10.1109/JLT.2019.2923126) 37[, 4275 \(2019\)](https://doi.org/10.1109/JLT.2019.2923126).
- [37] A. Arriola, S. Gross, N. Jovanovic, N. Charles, P. G. Tuthill, S. M. Olaizola, A. Fuerbach, and M. J. Withford, Low Bend Loss Waveguides Enable Compact, Efficient 3D Photonic Chips, Opt. Express 21[, 2978 \(2013\)](https://doi.org/10.1364/OE.21.002978).

- [38] A. K. Nowak, S. L. Portalupi, V. Giesz, O. Gazzano, C. Dal Savio, P. F. Braun, K. Karrai, C. Arnold, L. Lanco, I. Sagnes, A. Lemaître, and P. Senellart, Deterministic and Electrically Tunable Bright Single-Photon Source, [Nat.](https://doi.org/10.1038/ncomms4240) Commun. 5[, 1 \(2014\)](https://doi.org/10.1038/ncomms4240).
- [39] J. C. Loredo, N. A. Zakaria, N. Somaschi, C. Anton, L. de Santis, V. Giesz, T. Grange, M. A. Broome, O. Gazzano, G. Coppola, I. Sagnes, A. Lemaitre, A. Auffeves, P. Senellart, M. P. Almeida, and A. G. White, Scalable Performance in Solid-State Single-Photon Sources, Optica 3[, 433 \(2016\).](https://doi.org/10.1364/OPTICA.3.000433)
- [40] N. Spagnolo, C. Vitelli, L. Sansoni, E. Maiorino, P. Mataloni, F. Sciarrino, D. J. Brod, E. F. Galvao, A. Crespi, R. Ramponi et al., General Rules for Bosonic Bunching in Multimode Interferometers, [Phys. Rev. Lett.](https://doi.org/10.1103/PhysRevLett.111.130503) 111[, 130503 \(2013\).](https://doi.org/10.1103/PhysRevLett.111.130503)
- [41] A. Dousse, J. Suffczyński, R. Braive, A. Miard, A. Lemaître, I. Sagnes, L. Lanco, J. Bloch, P. Voisin, and P. Senellart, Scalable Implementation of Strongly Coupled Cavity-Quantum Dot Devices, [Appl. Phys. Lett.](https://doi.org/10.1063/1.3100781) 94, [121102 \(2009\).](https://doi.org/10.1063/1.3100781)
- [42] E. F. Galvão and D. J. Brod, Quantum and Classical Bounds for Two-State Overlaps, Phys. Rev. A 101[, 062110 \(2020\).](https://doi.org/10.1103/PhysRevA.101.062110)
- [43] M. Oszmaniec and D. J. Brod, Classical Simulation of Photonic Linear Optics with Lost Particles, [New J. Phys.](https://doi.org/10.1088/1367-2630/aadfa8) 20[, 092002 \(2018\).](https://doi.org/10.1088/1367-2630/aadfa8)
- [44] M. C. Tichy, Sampling of Partially Distinguishable Bosons and the Relation to the Multidimensional Permanent, [Phys.](https://doi.org/10.1103/PhysRevA.91.022316) Rev. A 91[, 022316 \(2015\)](https://doi.org/10.1103/PhysRevA.91.022316).
- [45] J. J. Renema, A. Menssen, W. R. Clements, G. Triginer, W. S. Kolthammer, and I. A. Walmsley, Efficient Classical Algorithm for Boson Sampling with Partially Distinguishable Photons, Phys. Rev. Lett. 120[, 220502 \(2018\)](https://doi.org/10.1103/PhysRevLett.120.220502).
- [46] A. Moylett, R. Garcia-Patron, J. J. Renema, and P. S. Turner, Classically Simulating Near-Term Partially-Distinguishable and Lossy Boson Sampling, [Quantum Sci. Technol.](https://doi.org/10.1088/2058-9565/ab5555) 5, [015001 \(2020\).](https://doi.org/10.1088/2058-9565/ab5555)
