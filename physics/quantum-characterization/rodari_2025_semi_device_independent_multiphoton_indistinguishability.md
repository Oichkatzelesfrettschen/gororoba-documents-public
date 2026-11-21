Source: https://doi.org/10.1103/PRXQuantum.6.020340
PDF sha256: cc5d89a0cfef647c1bd1091767dd017441d90204f9c10dbd77941a9da403e81a
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of rodari_2025_semi_device_independent_multiphoton_indistinguishability.pdf

Transcription of `rodari_2025_semi_device_independent_multiphoton_indistinguishability.pdf` in this directory, 24 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-24 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PRX QUANTUM 6, 020340 (2025)

Semi-Device-Independent Characterization of Multiphoton Indistinguishability
Giovanni Rodari ,1,§ Leonardo Novo ,2,§ Riccardo Albiero ,3,4 Alessia Suprano ,1
Carlos T. Tavares ,2 Eugenio Caruccio,1 Francesco Hoch ,1 Taira Giordani ,1 Gonzalo Carvacho ,1
Marco Gardina,5 Niki Di Giano ,3,4 Serena Di Giorgio ,5 Giacomo Corrielli,4,5
Francesco Ceccarelli ,4,5 Roberto Osellame ,4,5,† Nicolò Spagnolo ,1,*
Ernesto F. Galvão ,2,6,‡ and Fabio Sciarrino 1
1

Dipartimento di Fisica, Sapienza Università di Roma, Piazzale Aldo Moro 5, I-00185 Roma, Italy
2
International Iberian Nanotechnology Laboratory (INL), Avenida Mestre José Veiga s/n,
4715-330 Braga, Portugal
3
Dipartimento di Fisica, Politecnico di Milano, Piazza Leonardo da Vinci 32, I-20133 Milano, Italy
4
Istituto di Fotonica e Nanotecnologie (IFN), Consiglio Nazionale delle Ricerche (CNR),
Piazza Leonardo da Vinci 32, I-20133 Milano, Italy
5
Ephos, Inc., 333 Bush Street, San Francisco, California 94104, USA
6
Instituto de Física, Universidade Federal Fluminense, Av. Gal. Milton Tavares de Souza s/n,
Niterói, RJ, 24210-340, Brazil
(Received 8 May 2024; revised 6 September 2024; accepted 9 January 2025; published 30 May 2025)
Multiphoton indistinguishability is a central resource for quantum enhancement in sensing and computation. Developing and certifying large-scale photonic devices requires reliable and accurate characterization of this resource, preferably using methods that are robust against experimental errors. Here, we
propose a set of methods for the characterization of multiphoton indistinguishability, based on measurements of bunching and photon-number variance. Our methods are robust in a semi-device-independent
way, in the sense of being eﬀective even when the interferometers are incorrectly dialed. We demonstrate
the eﬀectiveness of this approach using an advanced photonic platform comprising a quantum dot singlephoton source and a universal fully programmable integrated photonic processor. Our results show the
practical usefulness of our methods, providing robust certiﬁcation tools that can be scaled up to larger
systems.
DOI: 10.1103/PRXQuantum.6.020340

I. INTRODUCTION
Multiparticle interference is one of the fundamental
resources for quantum information tasks. In many situations, interference provides a tool to outperform classical strategies for tasks in metrology and information
processing. In photonics, multiphoton interference has
been exploited for advantage in quantum sensing [1–
3], reaching sensitivities beyond the standard quantum
limit. In quantum computation, multiphoton interference
enables a nonuniversal model known as Boson Sampling
*

Contact author: nicolo.spagnolo@uniroma1.it
Contact author: roberto.osellame@cnr.it
‡
Contact author: ernesto.galvao@inl.int
§
These two authors contributed equally to this work.
†

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license. Further distribution of this work must maintain attribution to the
author(s) and the published article’s title, journal citation, and
DOI.

2691-3399/25/6(2)/020340(24)

[4], which involves sampling from the output distribution of indistinguishable photons interfering in a linear interferometer. Boson Sampling machines, featuring variants of the original proposal [5–8], have been
experimentally implemented [9–12] for demonstrations
of quantum computational advantage in Gaussian Boson
Sampling experiments that are hard to simulate by classical
supercomputers.
Embracing the fundamental role of quantum many-body
interference, it is important to develop robust and accurate
methods for the characterization of multiphoton indistinguishability. This is essential for the development of
better photon sources [13] but also for the certiﬁcation of
quantum advantage in applications featuring multiphoton
interference. For pairs of photons, the Hong-Ou-Mandel
(HOM) interference eﬀect [14] can be used to completely
characterize the level of two-particle indistinguishability.
The HOM visibility at the output of a symmetric beam
splitter leads to a direct estimation of the overlap between
the two single-photon spectral functions, describing their
internal degrees of freedom. If we have three or more

020340-1

Published by the American Physical Society

## PDF page 2

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

photons, pairwise HOM interference experiments are no
longer suﬃcient to completely characterize indistinguishability [15,16].
A number of approaches to the characterization of multiphoton indistinguishability have been reported in the
literature. One approach has deﬁned inequalities the violations of which bound parameters that characterize indistinguishability [17–20] or other relevant quantities [21,22] for
multiphoton scenarios. Starting from a prior knowledge of
the model describing the multiparticle state, Bayesian [23]
or maximum-likelihood [24] methods have also been used
to perform a direct estimation of the indistinguishability
parameters by measuring the output pattern after interference within linear interferometers. The ﬂexibility in the
design of linear interferometers requires an identiﬁcation
of the transformations that optimize the amount of information retrieved with respect to data sample size [23].
Other approaches are based on using speciﬁc classes of
interferometers. For instance, a generalization of the HOM
eﬀect to symmetric multimode interferometers leads to a
class of suppression laws [25–30] that identify suppressed
events due to the joint eﬀect of interferometer symmetry and bosonic statistics. Another recent approach uses
cyclic interferometers [31] for the estimation of a notion
of genuine indistinguishability for multiphoton states of a
particular form [17].
The methods discussed above are based on measuring
output patterns after linear-optics interference and often
rely on the implementation of speciﬁc interferometers or
a detailed knowledge of the interferometer that is being
implemented. Hence, a good assessment of multiphoton
indistinguishability using such methods requires an accurate description of the implemented linear-optical dynamics [32], with characterization errors in principle leading
to biases in the analysis of multiphoton indistinguishability. Recent eﬀorts to devise semi-device-independent
approaches have had the goal of providing guarantees on
indistinguishability with less need for trusting the characterization of parts of the experiment [33]. In our work,
we propose in Sec. II semi-device-independent methods
for the characterization of multiphoton indistinguishability, based on measurements of bunching and variance of
the photon number at the output of the device. We then
experimentally test the proposed methods in Sec. III, using
a photonic platform featuring a single-photon quantum-dot
(QD) source and an integrated photonic processor (IPP)
that is universal and fully programmable. Our methods can
also be relevant in scenarios in which we have access to
data coming from an interferometer built by an untrusted
party. As quantum technologies evolve, it is expected to
become more and more common that many users will not
have direct access to quantum hardware, which instead
will be available on the cloud. In this case, it is desirable for the user to be able to check if the data received
from a photonic quantum device are consistent with a

multiphoton interference experiment with highly indistinguishable photons, even though the device may not be
exactly implementing the unitary transformation that was
requested by the user. Finally, we believe that our methods
can also be useful as a way to monitor photonic indistinguishability during arbitrary interferometry experiments
without needing to periodically perform HOM tests.
II. THEORY
The setup that we consider consists of an n-mode general linear-optical interferometer, with n single-photon
inputs, one per photonic mode. The interferometer is
described by a unitary n × n matrix U, which maps input
creation operators to output creation operators. The indistinguishability of the photons is completely
⟨
⟩described by
a Gram matrix of inner products, Sij = χi |χj , where |χi ⟩
is the spectral function describing all the internal degrees
of freedom of the photon entering input port i. This Gram
matrix can be written only in terms of physically relevant
unitary invariant properties of the set of spectral functions
describing the single-photon internal degrees of freedom,
as described in Ref. [34].
We will now discuss the theoretical framework that
allows for a characterization of multiphoton indistinguishability based on measurements of photonic bunching
and photon-number variance at the output of a general
linear-optical device. As we will see, both methods apply
even when we do not have complete information on
the interferometer used. The two methods provide diﬀerent information on indistinguishability, with the photonnumber variance enabling the monitoring of two-photon
overlaps and full-bunching measurements giving us access
to a measure of indistinguishability that is also sensitive to
collective photonic phases [15,16,35].
A. Full-bunching probabilities
The probability of full bunching, studied in, e.g., Refs.
[36–38], is deﬁned as the probability that all n photons
leave the interferometer in a single chosen mode. It is
known that the probability of full bunching, pFB , decreases
exponentially. More precisely, in Ref. [38] it is shown that
pFB is upper bounded by pFB ≤ n!/nn , with the bound saturated by a balanced interferometer, i.e., one that distributes
any single-photon input uniformly among the output
modes. While this makes the measurement of this quantity
very challenging in experiments with many photons, for
small photon numbers one can estimate pFB with photoncounting measurements only on a single output mode.
Let us assume that one can ﬁx the interferometer design
and pick two diﬀerent indistinguishability scenarios characterized by Gram matrices S (1) and S (2) . Tichy has shown,
in Ref. [36], that the ratio of pFB for the two scenarios rFB = pFB (S (1) )/pFB (S (2) ) is exactly equal to the ratio
of the permanents of the Gram matrices S (1) and S (2)

020340-2

## PDF page 3

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
describing them:
(1)

(1)

pFB (S )
Per(S )
=
.
(2)
pFB (S )
Per(S (2) )

(1)

Let us look at one particular application of Eq. (1). A
set of n perfectly indistinguishable photons is described
by a Gram matrix Sij(1) = 1 ∀i, j, for which Per(S (1) ) =
n!. On the other hand, if the photons are perfectly distinguishable, they will be described by a diagonal Gram
matrix Sij(2) = diag(1, 1, . . . , 1), for which Per(S (2) ) = 1,
giving a ratio of full bunching for these two scenarios
that is Per(S (1) )/Per(S (2) ) = n!. This is the full-bunching
law of Ref. [37], which Eq. (1) generalizes for arbitrary
indistinguishability scenarios featuring pure single-photon
spectral functions.
The law in Eq. (1) is valid for any pair of Gram matrices.
As we will see in Sec. III, this means that one can ﬁx an
arbitrary interferometer design and then measure the probability of full bunching for perfectly distinguishable photons [described by a Gram matrix S (2) = diag(1, 1, . . . , 1)].
We can then prepare inputs described by a diﬀerent Gram
matrix S (1) and again measure pFB . According to Eq.
(1), the ratio of the measured full-bunching probabilities in the two scenarios will give us an estimate for
Per(S (1) )/Per(S (2) ) = Per(S (1) ), which can be seen as a
measure of photon indistinguishability [36]. In fact, given
a Gram matrix S,
Per(S)
d(S) =
(2)
n!
measures the fully symmetric component
⨂n of the initial
product state of spectral functions
i=1 |χi ⟩ and so it
takes the value 1 only when all states |χi ⟩ are the same
[39]. Another point worth noting is that pFB , being a function of Per(S), depends on higher-order unitary invariants
encoded in the Gram matrix (for an overview, see Ref.
[34]). This means that measurements of pFB are sensitive to these so-called collective photonic phases [15,16].
Estimating these phases is, however, not a main focus
of our work and all distinguishability scenarios realized
experimentally are consistent with a trivial photonic phase
(see Sec. III B). Our goal is instead to use full-bunching
probabilities as a way to extract a meaningful measure of
indistinguishability in a manner that does not depend on
the interferometer implemented.
B. Photon-number variance
We will now show that the average photon-number
variance at the output of the device can also be used to
characterize multiphoton indistinguishability. We deﬁne
this quantity as
σ =

n
1 ∑ ⟨ 2⟩
n − ⟨ni ⟩2 ,
n i=1 i

(3)

PRX QUANTUM 6, 020340 (2025)

where ni is the number of photons at output mode i,
still assuming that we inject exactly one photon per input
mode. Unlike the probability of full bunching, σ does not
decrease as n increases. On the other hand, its estimation
is experimentally challenging, as in principle it requires
photon-counting detection on all output modes.
In Appendix A, we obtain a universal and simple expression for σ that is valid for any interferometer and any
number of modes:
σ =1+

1 ∑∑
1∑
|⟨χa |χb ⟩|2 |Uia |2 |Uib |2 −
|Uik |4 .
n a̸=b i
n ik
(4)

Note that, unlike the probability of full bunching pFB , the
average photon-number variance σ only depends on twophoton overlaps ab = |⟨χa |χb ⟩|2 and not on higher-order
unitary invariants written as functions of three or more
spectral functions [15,16,34]. Moreover, it depends only
on the absolute value squared of the matrix elements of
the interferometers, which can be measured using classical
light.
It can be seen from Eq. (4) that any increase on the
overlaps ab will result in an increased variance. This
implies that, for a given interferometer, the variance is
maximized when photons are fully indistinguishable. We
show in Appendix A that the overall maximum of the
variance is obtained by further optimizing over possible
interferometers, which leads to the value
σ max = 2 − 2/n,

(5)

obtained for indistinguishable photons and balanced interferometers on n modes, i.e., where |Uij |2 = 1/n, such as
in the Fourier interferometer. In fact, it can be seen that
the implementation of a balanced interferometer gives us
direct access to the average indistinguishability of the input
states, since
σ bal = 1 +

n−1
1
¯ − .

n
n

(6)

¯ as
Here, we deﬁne the average indistinguishability 
∑
a̸=b ab
¯
=
.
(7)
n(n − 1)
This provides a simple way to monitor the average indistinguishability of the photon sources with a single n-photon
interferometry experiment, without requiring O(n2 ) HOM
tests. We remark that for large n, the expression in Eq. (6)
matches the one obtained in Ref. [40] by diﬀerent techniques, which uses the fact that the reduced density matrix
of a single output of the interferometer is well described by
a product of thermal states in the asymptotic limit.

020340-3

## PDF page 4

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

We also show in Appendix B that the measurement
of the variance with the Fourier interferometer for n = 3
also gives us a nontrivial lower bound for all two-photon
overlaps ab as
(
min ab ≥
a̸=b

)2
9 bal
σ −2 ,
4

(8)

without the need for any assumptions on the form of
the Gram matrix S. This shows that σ bal can be used
to certify the minimum value of all three two-photon
indistinguishabilities.
While balanced interferometers give us a direct way
to obtain guarantees on indistinguishability, we can also
show that arbitrary interferometers can be used to reconstruct the matrix of overlaps ab . Assuming knowledge
on the values of |Uij |2 , the measurement of σ for diﬀerent interferometers allows us to reconstruct the matrix 
by solving a linear system of equations (see Sec. III C).
This approach is a practical way of extracting information
on the indistinguishability of the input photons directly
from the photon-number variance σ at the output of arbitrary interferometers. This could be helpful in monitoring
the photon-source indistinguishability, without any need to
interrupt the data acquisition to perform HOM tests.
We may also assume a scenario in which we do not
trust the implementation of some desired unitary matrices,
either because of experimental imperfections or because
we have access to an interferometer built by an untrusted
party. Even then, it may be possible to use such a device
¯
to obtain guarantees on the average indistinguishability .
This can be done by measuring the value of σ for a given
distinguishability scenario deﬁned by the matrix  as well
as the value of σ d , i.e., the average variance when distinguishable photons are sent to the same device. In Appendix
C, we prove the following inequality, which is valid for any
interferometer:
¯ ≥


1
n(n − 1)

(

σ − 2σ d + 1
1 − σd

)2
−

1
¯ LB .
=
n−1

(9)

This bound can be used to give us a guarantee on photon indistinguishability in a semi-device-independent scenario, where the preparation of single photons and the Fock
measurements are trusted but not the interferometer.
It can be seen that the bound is tight for balanced interferometers and fully indistinguishable photons, in which
case ¯
LB = 1. For Haar-random interferometers or scenarios of partial distinguishability, the bound is looser and
may give trivial results in some instances. Assuming fully
indistinguishable photons and n = 3, the bound is nontriv¯ LB > 0) for about 80% of Haar-random interferial (i.e., 
ometers. This percentage increases for larger n and at n =
6 it is nontrivial for more than 99% of the instances (see
Appendix C). In addition, we note that while we focus on

bounding the average indistinguishability, as intermediate
steps to derive Eq. (9), we obtain semi-device-independent
bounds for other quantities that can be seen as measures of
indistinguishability, such as the maximum eigenvalue of
the overlap matrix ab or of the Gram matrix Sij , which
may be of independent interest.
Finally, it is natural to ask whether estimates or lower
bounds on the average indistinguishability, as deﬁned in
Eq. (7), can be used to approximate the other quantiﬁer of photonic indistinguishability d(S) from Eq. (2).
This question is particularly relevant for higher photon
numbers, where measurements of full-bunching probabilities are much more challenging than measurements
of photon-number variances. In Appendix D, we address
this question by showing that the two quantities are
related by a simple expression if we assume a uniform¯ 1/2 , for i ̸= j. This
distinguishability model with Sij = ()
relation shows that asymptotically d(S) decreases pro¯ n/2 . We also consider random Gram
portionally to ()
matrices resulting from small random time delays of the
input-photon wave packets with a ﬁxed variance (which
¯ showing a similar
implies a ﬁxed expected value of ),
exponential decay.
III. EXPERIMENTAL VERIFICATION
As a next step, we have performed experimental measurements of the probability of full bunching pFB and
the average photon-number variance at the output σ . The
employed platform comprises a state-of-the-art solid-state
single-photon source interfaced with a photonic integrated
circuit, with the aim of characterizing the indistinguishability of the output photons and of testing diﬀerent regimes
via controlled tuning. We have implemented speciﬁc interferometers, such as the balanced tritter, as well as randomly chosen 3 × 3 transformations, as a way to test
the semi-device-independent features of our approach. In
Sec. III A, we describe the experimental setup used for
our multiphoton-indistinguishability tests. In Sec. III B, we
describe the results on the full-bunching-ratio measurements, and in Sec. III C we discuss the experimental results
related to the measurement of the average photon-number
variance.
A. Experimental setup
The experimental apparatus corresponds to a photonic
machine named QOLOSSUS, which comprises diﬀerent
components used for photon generation, manipulation, and
detection. The multiphoton input states are generated using
a QD single-photon source (Quandela e-Delight system),
consisting of an InGaAs matrix located in a nanoscale
electrically controlled micropillar cavity [42–46]. The
source operates in a cryogenic environment (at approximately 4 K), obtained within a Attocube-AttoDry800 He
closed-cycle cryostat, and works in a nonresonant regime

020340-4

## PDF page 5

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
exploiting a longitudinal-acoustic (LA) phonon-assisted
conﬁguration [46], pumped by a blue-detuned excitation
obtained with a 927.2 nm central-wavelength pulsed laser,
operating at a Rexc = 79 MHz repetition rate. The photons
are emitted with a wavelength of 927.8 nm, in a train of
pulses emitted in time bins at a ﬁxed distance τ ∼ 12.5 ns,
i.e., the inverse of the pulsed-pump-laser repetition rate.
The output photons are coupled in a single-mode ﬁber
through a confocal microscope mounted on top of the cryostat and then separated from the residual laser pump via
spectral ﬁltering. The latter is implemented in bulk via
a set of three narrow bandpass ﬁlters, with a bandwidth
of a few hundred picometers, tilted in such a way as to
maximize their transmission eﬃciency at the single-photon
wavelength. Here, we measure, on avalanche photodiodes
with a quantum eﬃciency of ηd ∼ 35%, a typical count
rate of R ∼ 3.5 MHz. Accounting for the overall transmission eﬃciency of the collection setup, estimated to
be ηc ∼ 55%, this corresponds to a ﬁrst-lens brightness
B = R/(Rexc ηd ηc ) ∼ 23%. We have assessed the singlephoton purity and pairwise photon indistinguishability by
measuring the second-order autocorrelation function and
the visibility in a HOM experiment, obtaining g (2) (0) ∼
0.02 and VHOM ∼ 0.91, respectively. More speciﬁcally, the
value reported above for the visibility corresponds to that
obtained between photons emitted at adjacent time bins,
i.e., separated by a time distance of τ ∼ 12.5 ns, via a dedicated characterization setup. The train of single-photon
pulses emitted by the source is then converted in a multiphoton input state, corresponding to single photons propagating in diﬀerent spatial modes, via a commercially available temporal-to-spatial demultiplexing system Quandela
QDMX-6 [31,47]. Speciﬁcally, the system employs an rfmodulated acousto-optical material to diﬀract an input
signal toward several output spatial modes. We have optimized the demultiplexing system to continuously divide
the input signal into three bunches, each with a duration
of Tb ∼ 180 ns. We note that this choice depends on a
trade-oﬀ between overall losses due to the ﬁber delay lines
and an eﬀective linear reduction in the repetition rate of
the experiment [47]. The latter depends linearly on the
switching time of the AOM between two subsequent channels of Ts ≈ 60 ns. Indeed, when the device is switching
between two optical output channels, an incoming photon
can be found in either one of them, thus giving a linear
reduction in the eﬀective rate of the experiment as FF =
(Tb − Ts )/Tb ≈ 2/3. To achieve temporal synchronization
of the photon bunches, we have added time delays obtained
via custom-length single-mode ﬁbers. The overall inputoutput transmission eﬃciency has been measured to be
ηDMX ∼ 0.75 in the worst case. The typical degree of HOM
visibility V(T) among photons separated by a time interval T has been found to be VHOM
12(23) (180 ns) = 0.83(1) and
HOM
V13 (360 ns) = 0.81(1). The HOM visibility decreases
with increased pairwise photon delays, as already observed

PRX QUANTUM 6, 020340 (2025)

in Ref. [47]. The reason for the visibility decrease could
be related mainly to spectral wandering eﬀects of the QD
emission on a timescale of several hundreds of nanoseconds [48] and to imperfect control of the polarization in
the DMX setup. We note that the pairwise photon indistinguishability could be further improved via additional
polarization or spectral ﬁltering, as already pointed out in
Ref. [47]. The overall source conﬁguration is shown in Fig.
1(a).
We use an eight-mode fully programmable IPP to characterize the multiphoton indistinguishability of the source.
This device, fabricated via the femtosecond-laser-writing
(FLW) technology [49], consists of a mesh of waveguide interferometers arranged according to the rectangular
layout of Ref. [41]. This layout choice allows the implementation of any linear-optical transformation on eight
modes. As shown in Fig. 1(b), the device is composed
of a network of 28 beam splitters with variable beamsplitting ratios acting as elementary cells Bi , each of which
actually implemented as a programmable Mach-Zehnder
interferometer (MZI). Each MZI is implemented using two
cascaded balanced directional couplers and two thermooptic phase shifters that provide full control of the cell
operation. The fabrication and calibration procedures are
detailed in Appendix E.
B. Measuring the full-bunching ratio
As a ﬁrst step, we have programmed the device to
implement a balanced tritter transformation U3 on three
single-photon inputs, injected into modes [3, 4, 5] [see Fig.
1(c)]. The programming of the device has been performed
in the following way: the ﬁrst three layers of the IPP
have been used to implement the linear-optical unitary
U3 , while the remainder of the device, together with an
external in-ﬁber beam splitter, has been used to split the
three outputs of U3 to perform pseudo-photon-numberresolving detection, using an experimental setup similar to
that used in other implementations of indistinguishability
tests [17,19,33,50]. The implemented transformation Ũ3
†
has been found to reach a ﬁdelity of F = |Tr(U3 Ũ3 )|/3 >
0.999 with respect to the ideal unitary U3 (see Appendix
F). Hereafter, we will use the tilde (“∼”) to label all the
experimentally measured quantities. The general form of a
Gram matrix describing a three-photon indistinguishability
scenario is given by a matrix in the form
⎛
1

⎜√
⎜
Sk = ⎜ kab
⎝√
kac

√
kab
√

1
kbc e−iϕ

√

kac

⎞

⎟
√
⎟
kbc eiϕ ⎟ .
⎠
1

(10)

In what follows, we parametrize the indistinguishability of
a scenario using positive real-valued Gram matrices Sk ,
i.e., we assume ϕ = 0, while k labels the scenario and

020340-5

## PDF page 6

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

(a)

pump
laser

phonon

spectral
ﬁltering
pump

photon

to integrated
photonic processor
single-photon source

(b)

temporal-to-spaal
demulplexing

PBS

(c)

power
supply

integrated photonic
processor

mode spling

processor programming
integrated photonic processor layout

=
elementary cell

→ 3 × 3 transformaon
( )
→ identy over the modes
mode spling → poron of the device used
for detecon

FIG. 1. The experimental setup: the QOLOSSUS machine employed for the veriﬁcation of the proposed tests. (a) A single-photon
source composed of a quantum-dot (QD) operating in a nonresonant regime, emitting a train of single-photon pulses at ﬁxed time
intervals τ . A demultiplexing module converts such a sequence to a set of three-photon input states injected into diﬀerent modes of
an integrated photonic processor (IPP). (b) The scheme of the universal eight-mode IPP, using the layout of Ref. [41]. The elementary
cells Bi are programmable Mach-Zehnder interferometers (MZIs) composed of two balanced directional couplers and of two thermooptic phase shifters. Photons are coupled at the input and at the output of the integrated processor via single-mode ﬁber arrays,
directly pigtailed to the device. (c) The device-programming scheme for the diﬀerent measurements performed. When the processor is
employed to measure the full-bunching ratio, three photons are injected into modes [3, 4, 5], with the ﬁrst three layers of elementary
cells used to program transformation U3 . The subsequent layers, and an oﬀ-chip ﬁber beam splitter, are used to perform pseudo-photonnumber-resolving detection via avalanche photodiodes and a time-tagging system. I corresponds to the identity over the modes.

(a, b, c) label the diﬀerent photons injected at the inputs
of the interferometer. The assumption that the indistinguishability is well described by a Gram matrix as above
comes from the observation that, in the regime of the
experiment, the source of partial indistinguishability can
be approximated by a pure-state model. Indeed, for a high
value of indistinguishability and a limited photon number,
the spectral decomposition of the overall density matrix
can be substantially approximated by its component with
the highest eigenvalue, and this model has been shown
in recent implementations to provide an accurate description of multiphoton data in similar regimes [31,47,51].
Furthermore, the assumption that ϕ = 0 has been veriﬁed
experimentally via two independent tests, i.e., by using a
methodology based on outcomes of a cyclic interferometer
[31], and by direct analysis of the output distribution after
the tritter (see Appendix G). At ﬁrst, we have implemented
a scenario described by a Gram matrix SA that identiﬁes the
intrinsic photon-source indistinguishability reached after

the demultiplexing module. In this conﬁguration, the val˜ Aij have been estimated from the visibilities VHOM
ues 
ij
of independent HOM experiments, by correcting for the
eﬀect of the nonzero value of the second-order correlation function g (2) (0) = 0.0218(6) following the approach
˜ ij = (VHOM
of Ref. [52]: 
+ g (2) (0))/(1 − g (2) (0)). In our
ij
˜ Aac = 0.874(2),
case, we have obtained ˜
Aab = 0.875(4), 
˜ Abc = 0.848(2).
and 
The second scenario corresponds to a diagonal Gram
matrix SD describing photons made completely distinguishable due to other auxiliary degrees of freedom, i.e.,
time and polarization. The tuning of indistinguishability
using polarization is made possible by the polarizationindependent operation of the IPP.
The measured output probability distributions with
three-photon inputs described by those two indistinguishability scenarios are shown in Figs. 2(a)–2(b) and compared
with a model (see Appendix H) that includes all the main

020340-6

## PDF page 7

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
experimental features, such as uniform losses, the eﬀective matrix Ũ3 , the eﬀective Gram matrix of the input
conﬁguration, and multiphoton contributions related to the
nonzero g (2) (0). The data are in good agreement with
the expectation from the model (for more details on the
analysis, see Appendix I). The agreement can be∑quantiﬁed by the total variation distances TVD = 1/2 i |pi −
qi | between the experiment (pi ) and the model (qi ). The
obtained values for the two conﬁgurations are, respectively, TVD(SA ) = 0.015(2) and TVD(SD ) = 0.013(2).
From the measured samples, we have then estimated the full-bunching ratios for the two scenarios
from the full-bunching probabilities [p̃FB (SA ), p̃FB (SD )],
summed over all the three possible output conﬁgurations
[(3, 0, 0), (0, 3, 0), (0, 0, 3)]. The measured value is found
to be r̃FB (SA ) = p̃FB (SA )/p̃FB (SD ) = 4.9(1). This is to be
compared, in principle, with the ratio between the permanents of the Gram matrices, per(SA )/per(SD ) = 5.21(1).
A more accurate prediction of the full-bunching-ratio
value expected from the experiment can be computed
from the model that takes into account all the other
sources of noise in the setup, i.e., multiphoton contributions and optical losses as described in Appendix H. More
speciﬁcally, by including these eﬀects, the expected value
reduces from the ratio between the Gram matrix permanents, per(SA )/per(SD ) = 5.21(1) to rFB (SA ) = 4.91(1),
thus showing a very good agreement with the experimental data. We use Eq. (1) and the two output distributions
to estimate the full-bunching ratio for each of the three
output modes of U3 : {r̃(3,0,0)
(SA ), r̃(0,3,0)
(SA ), r̃(0,0,3)
(SA )} =
FB
FB
FB
{5.1(2), 4.8(2), 4.7(2)}. The obtained values are in good
agreement with the predictions from the model, which
are found to be {r(3,0,0)
(SA ), r(0,3,0)
(SA ), r(0,0,3)
(SA )} =
FB
FB
FB
{4.91(1), 4.91(1), 4.91(1)}. As a further test of our
approach, we have prepared photons described by a diﬀerent Gram matrix SB by tuning the polarization state of photon b to reduce its indistinguishability with respect to the
other two. The corresponding overlaps estimated from the
˜ ab = 0.103(4), 
˜ ac = 0.881(2),
HOM visibilities were 
˜ bc = 0.107(2). The measured distribution is in good
and 
agreement with the predictions from the model [see Fig.
2(c)], quantiﬁed by the total variation distance TVD(SB ) =
0.025(4). This conﬁguration led to a measured fullbunching ratio of r̃FB (SB ) = p̃FB (SB )/p̃FB (SD ) = 2.11(6),
to be compared with the ratio between the permanents
of the Gram matrices, per(SB )/per(SD ) = 2.28(2), and
with the prediction obtained from the model, rFB (SB ) =
2.21(2).
To experimentally show that our approach is robustly
independent of the interferometer implemented, we have
performed additional experiments in which the IPP has
been programmed to implement 23 diﬀerent random 3 ×
3 transformations, obtained by driving the thermo-optic

PRX QUANTUM 6, 020340 (2025)

(a)

(b)

(c)

FIG. 2. The experimental measurement of the output distributions with a balanced tritter. The measured distributions p̃(n1 ,n2 ,n3 )
are obtained by programming the device to act as the Ũ3 transformation according to the discussion in the text. (a) The distribution obtained for a Gram matrix SA , identifying the intrinsic
photon indistinguishability after the DMX module. (b) The distribution obtained for distinguishable particles, corresponding to
a Gram matrix SD . (c) The distribution obtained for a Gram
matrix SB . The colored bars show experimental data; the darker
regions correspond to 1-σ conﬁdence intervals. The white bars
show predictions obtained from a model taking into account the
implemented transformation Ũ3 , the Gram matrices estimated
from pairwise Hong-Ou-Mandel (HOM) experiments, losses,
and multiphoton contributions obtained from the estimated g (2)
value.

020340-7

## PDF page 8

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

(a)

(b)

FIG. 3. The measurement of the full-bunching ratios for 23 randomly drawn interferometers. The measured values of rFB in (a) the
scenario SA and (b) the scenario SB′ as a function of the corresponding measured pFB . The black points correspond to the experimental
data, with the error bars corresponding to the statistical error in the performed measurements (two experimental points nearly overlap
for pFB ≈ 0.18). The red-shaded area in the two scenarios corresponds to a prediction obtained by averaging the expected value with
the model taking into account losses and multiphoton emission from the source, and ﬂuctuation on pairwise indistinguishability during
the experimental run. The bottom histograms show the distribution of pFB over Haar-random unitaries, obtained via a Monte Carlo
simulation in the ideal scenario in the two indistinguishability conﬁgurations (blue) and taking into account experimental imperfections
(orange).

phase shifters of the U3 block of the IPP with random currents [see Fig. 1(c)]. We have measured the full-bunching
ratio rFB of two indistinguishability scenarios against the
one with distinguishable photons. Again, scenario SA features highly indistinguishable photons from the source
after demultiplexing. Conversely, we have reconstructed
a scenario SB′ in which one photon is completely distinguishable from the other two, corresponding to overlaps
˜ Bab′ = 0, 
˜ Bac′ = 0.831(4), 
˜ Bbc′ = 0, by injecting two pho
tons into the interferometer inputs {a, c} and reconstructing the full-bunching probabilities from twofold coincidence counts (see Appendix I). The results are shown
in Fig. 3 as a function of the full-bunching probability
pFB for each random unitary. We observe that in both
cases, the measured values of rFB are very close to the
expected ones, independently of the dialed transformations. In the bottom panels of Fig. 3, we also show histograms for the expected distribution of pFB over a broad
set of Haar-random unitaries, both in an ideal scenario
and taking experimental imperfections into account, for
both the two indistinguishability scenarios. This shows
that the experimentally dialed unitaries cover a signiﬁcant
portion of the available range achieved by pFB in both
conﬁgurations.

probabilities for all possible photon-number output conﬁgurations, done via the detection system described above,
based on mode splitting and coincidence detection.
We have considered the same indistinguishability scenarios SA and SB described above and evaluated the variance σ̃ (Sk ) using the same measured data sample, corresponding to a device programmed to act as a balanced
tritter. The estimated value of the variance has been measured to be σ̃ (SA ) = 1.199(4), while the maximum value
for fully indistinguishable photons would be 4/3 [see Eq.
(5)]. The bound presented in Eq. (8) can then be used to
determine a nontrivial lower bound min ij ≥ 0.49(1) for
the three individual overlaps. The same analysis has been
performed on data collected using the indistinguishability
scenario SB , resulting in an estimated value of the variance
σ̃ (SB ) = 0.885(3). As expected, the previous analysis now
fails to give a nontrivial lower bound for the overlaps values, being below the minimum threshold 8/9 for Eq. (8) to
give a meaningful lower bound on min ij .
Similarly, since the interferometer U3 was set to implement the tritter matrix, we can use the relationship given
by Eq. (6) to extract an estimation of the average pairwise
indistinguishability in the two scenarios, given by
¯ A ) = 0.80(1),
(S

(11)

C. Measuring the photon-number variance

¯ B ) = 0.33(1).
(S

The second step has been dedicated to the characterization of photon indistinguishability based on the measurement of the photon-number variance in our experimental platform. This approach requires measurement of the

These values are found to be compatible with the pairwise
HOM visibilities for each photon pair. Indeed, the experimental estimate of the photon-number variance is sensitive

020340-8

## PDF page 9

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY

PRX QUANTUM 6, 020340 (2025)

(a)

(b)

FIG. 4. The inference of the experimental overlaps (visibilities) via the photon-number variances measured over 23 randomly sampled unitaries. Here, we report the histogram of
pairwise overlaps {′ab , ′bc , ′ac } inferred by numerically minimizing Eq. (13) over 50 000 bootstrapped optimization runs. The
considered photon-number variances in the optimization problem
are obtained experimentally considering three photons injected
into the interferometer set to implement 23 diﬀerent unitaries,
in the indistinguishability scenario SA . Blue bars, ′ab ; orange
bars, ′ac ; green bars, ′bc . The vertical dashed lines identify the
average of the Monte Carlo distributions.

to the presence of multiphoton components in the emitted light and thus the bound is expected to be compatible
with the HOM visibilities, which include both the overlaps
and the multiphoton contributions. Finally, by considering
the expected variance in the distinguishable scenario for
the balanced three-mode interferometer σ d = 2/3, we can
compute a nontrivial lower bound to the average pairwise
¯ LB , as in Eq. (9):
indistinguishability 
¯ A ) ≥ 0.63(1),
(S

(12)

while scenario SB also fails in this case to give a nontrivial lower bound for the overlap values. Again, we note that
¯ is to be considsuch estimation of a lower bound on 
ered semi-device-independent, as it requires as a further
element only a direct measurement of the average variance
in a fully distinguishable scenario σ d or its reconstruction,
as in Eq. (4), via the unitary moduli |Uij |, which can be
measured in a straightforward experiment using classical
light.
Besides this direct application of the photon-number
variance σ either to obtain a lower bound on all overlaps
using Eq. (8) or to estimate an average pairwise overlap
parameter, we now show how σ measurements can also be
used to directly monitor the value of each individual overlap. The key idea is to program the device to implement
interferometers drawn from a random ensemble and use σ
together with information from measurements of the moduli |Uij | as we now describe. We can interpret Eq. (4) as a

FIG. 5. The semi-device-independent lower bounds on the
¯ LB on the average
average overlap ¯
. (a) The lower bounds 
overlap parameter ¯
, inferred from the experimentally measured
photon-number variances σ̃Ui . Here, we show σ̃Ui as a function
¯ LB , which has been inferred from the data. The dashed line
of 
shows the numerically expected behavior in the indistinguishability scenario described by SA . (b) The histogram of a Monte
Carlo simulation of the lower bound on the average overlap
¯ obtained from numerical calculation of the photonparameter 
number variances both in an ideal scenario described by the
Gram matrix SA and taking into account experimental imperfections such as multiphoton contributions—in blue and orange,
respectively. This gives us numerical evidence that even with
Gram matrix SA , which does not correspond to perfect indistinguishability, around 70% of randomly sampled Haar-random
unitaries still give a nontrivial, i.e., positive, lower bound on the
¯ On both plots, this is highlighted as the nonshaded
parameter .
¯ LB .
area corresponding to nontrivial lower bounds for 

linear equation for the three unknown overlaps |⟨χa |χb ⟩|2 ,
|⟨χb |χc ⟩|2 , and |⟨χc |χa ⟩|2 that we would like to estimate,
while the moduli |Uij | and σ as measured (known) coefﬁcients. If we dial three diﬀerent unitaries and measure
the corresponding variances σ , together with knowledge
of the moduli |Uij |, Eq. (4) gives us a linear system of
equations that can be solved to obtain the three individual
overlap values. The robustness of the method to experimental imperfections, e.g., small changes in the overlaps
during the measurement runs, can be improved by collecting an overcomplete data set corresponding to more than
three unitaries and performing a numerical optimization
for a more stable solution. One way of doing this is to consider a given set of unitaries {Ui } and deﬁne the following
numerical minimization problem:

020340-9

min
jk

∑ [σ̃U − σU (′ , ′ , ′ )]2
i

i

i

ab

Var[σ̃Ui ]

ac

bc

,

(13)

## PDF page 10

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

where Var[σ̃Ui ] is the experimental uncertainty associated with the photon-number variance σ̃Ui measured when
the interferometer is programmed to implement unitary
Ui . Here, σUi (′ab , ′ac , ′bc ) represents the photon-number
variance estimated via Eq. (4). Namely, we consider
{′ab , ′ac , ′bc } as free parameters for the optimization
problem and plug in the moduli of the unitary matrices |Ui | measured independently via classical light. We
have applied this method to the output data from the
23 implemented random unitaries, in scenario SA . As
reported in Fig. 4, we show the numerical results of
50 000 bootstrapped optimization runs of the quantity in
Eq. (13). The resulting values for the estimated overlaps,
′ab = 0.818(6), ′bc = 0.796(12), and ′ac = 0.844(11),
are found to be compatible with the average HOM visibilities for each photon pair monitored independently
during the data-acquisition process for the random interferometers. Indeed, Eq. (4) does not take multiphoton
emission between the sources into account, while the presence of multiphoton emission has the eﬀect of reducing the
observed value of the HOM visibilities with respect to the
overlaps |⟨χi |χj ⟩|2 . To conclude, we note that the semidevice-independent bound described by Eq. (9) returns
a positive and thus nontrivial lower bound for the aver¯ LB ≥ 0 for approximately half
age indistinguishability 
the implemented random unitaries, as reported in Fig. 5.
There, we also show the distribution of the lower bounds
¯ LB obtained via a
on the average overlap parameter 
Monte Carlo numerical simulation over 105 randomly
drawn Haar-random matrices, carried out in an ideal scenario described by the indistinguishability conﬁguration SA
and ﬁnally taking into account experimental imperfections
such as multiphoton contributions. This gives us numerical evidence of the fact that even in this scenario, where
perfect indistinguishability is not achieved, a nontrivial,
i.e., positive, lower bound on the average overlap parameter can still be obtained with around 70% of Haar-random
unitaries.

photon-number variances improves upon previous work
on semi-device-independent witnesses of indistinguishability based on a single two-mode correlator [33], by
giving nontrivial guarantees on indistinguishability for a
large fraction of Haar-random interferometers. While the
approach based on bunching probabilities is more tailored
to experiments with low photon numbers, the semi-deviceindependent methods based on the photon-number variance do not suﬀer scalability problems and can be used to
obtain guarantees on the indistinguishability of sources in
experiments with larger numbers of photons.
ACKNOWLEDGMENTS
This work was supported by the Future Emerging Technologies (FET) project PHOQUSING (“PHOtonic Quantum SamplING machine”) under Grant Agreement No. 899544) and by the Centro Nazionale di
Ricerca in High Performance Computing, Big Data,
and Quantum Computing (ICSC), funded by European
Union—NextGenerationEU. L.N. and E.F.G. acknowledge support from the Fundação para a Ciência e a Tecnologia (FCT, Portugal) via Project No. CEECINST/00062/
2018. The fabrication of the IPP was partially performed
at PoliFAB, the micro- and nanofabrication facility of
Politecnico di Milano. We would like to thank the PoliFAB
staﬀ for the valuable technical support.
APPENDIX A: AVERAGE PHOTON-NUMBER
VARIANCE AT THE OUTPUT
In this appendix, we obtain a simple and universal
expression for the average photon-number variance σ that
is valid for any interferometer and any number n of modes:
σ =1+

1 ∑∑
1∑
|⟨χa |χb ⟩|2 |Uia |2 |Uib |2 −
|Uik |4 .
n a̸=b i
n ik
(A1)

IV. CONCLUSIONS
We have reported on the proposal and experimental
implementation of tests to perform robust characterization of multiphoton interference. Our approach, based on
measuring the bunching properties or the average variance of the photon-number distribution at each output, can
be considered semi-device-independent, as they provide
guarantees on indistinguishability without detailed knowledge of which interferometer is being implemented. The
validity of the approach has been veriﬁed experimentally
in an advanced photonic platform comprising diﬀerent
components such as a QD source interfaced with a fully
programmable IPP. The results obtained have conﬁrmed
the robustness of the methods, showing its applicability in
a practical setting. In particular, our approach based on

To derive this expression, we will use the fact that the correlation between photon numbers in modes i and j , with
i ̸= j , can be written as [53]
Cij = ⟨n̂i n̂j ⟩ − ⟨n̂i ⟩⟨n̂j ⟩
∑
∑
|⟨χa |χb ⟩|2 Uia Ujb Uib Uja −
|Uik |2 |Ujk |2 .
=
a̸=b

k

(A2)
The conservation of the total number of photons allows
us to express the average
∑ variance in terms of these correlators. Deﬁning N̂ = i n̂i as the total photon-number

020340-10

## PDF page 11

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
operator, we have, from photon-number conservation, that
⟨N̂ 2 ⟩ − ⟨N̂ ⟩2 = 0,

PRX QUANTUM 6, 020340 (2025)

which n is the number of modes, we obtain

(A3)

σ bal = 1 +

∑ |⟨χa |χb ⟩|2
a̸=b

which leads to
∑

⟨n̂2i ⟩ − ⟨n̂i ⟩2 = −

∑

+
⟨n̂i n̂j ⟩ − ⟨n̂i ⟩⟨n̂j ⟩,

(A4)

i̸=j

i

While a single two-mode correlator Cij has previously
been considered as a semi-device-independent witness of
indistinguishability [33], it can be seen from the above
equation that the average variance takes into account all
possible two-mode correlators in an unbiased way. This
leads to better semi-device-independent guarantees on
indistinguishability for unbiased as well as Haar-random
interferometers, as demonstrated in the main text.
Using Eqs. (A4) and (A2), we can establish the following equality:
1∑ 2
⟨n̂ ⟩ − ⟨n̂i ⟩2
n i i

σ =

=−

(A5)

B

The terms A and B can be simpliﬁed in the following way:
A=−

∑

Uia Uib Uia Uib +

i

=−

∑

∑

Uia Uib Ujb Uja

i,j

|Uia | |Uib | + δa,b δa,b ,
2

2

(A6)

σ bal =

B=−

∑
i

|Uik |4 +

i

|Uik |2

∑
j

|Ujk |2 = 1 −

∑

)
2 2(
+
|⟨χ1 |χ2 ⟩|2 + |⟨χ2 |χ3 ⟩|2 + |⟨χ1 |χ3 ⟩|2 .
3 9
(A9)

In this section, we show that any balanced interferometer on n modes maximizes σ for perfectly indistinguishable
photons; in particular, the Fourier interferometer maximizes σ . In the fully indistinguishable case, all Grammatrix elements equal 1, i.e., ∀a,b : ⟨χa |χb ⟩ = 1, which
leads to

|Uik |4 .

i

(A7)
Plugging in these simpliﬁcations into Eq. (A5), we obtain
the expression for σ shown in the main text and in Eq.
(A1).
Furthermore, by considering a balanced interferometer
such as the Fourier transform, where the absolute value
√ of
the matrix elements of the unitary are equal to 1/ n, in

2∑
|Uia |4 .
n a,i

(A10)

Therefore,
∑ the maximization of σ reduces to the minimization of a,i |Uia |4 . We demonstrate that this term is lower
bounded by 1 and that this lower bound is attained exactly
for balanced interferometers, i.e., |Uij |2 = 1/n ∀i, j , as is
the case for the Fourier transform.
To demonstrate this, we∑deﬁne the
∑ doubly stochastic
matrix Pij = |Uij |2 with
i Pij =
j Pij = 1. Using a
known inequality between the 1-norm and the 2-norm, we
have that
√∑
i

∑

(A8)

1. Maximizing σ for indistinguishable photons

i

and

1
1
=1−
n
n

2 ∑
|⟨χa |χb ⟩|2 .
n2 a>b

σ =2−

A

−

In particular, for the three-mode balanced tritter implemented experimentally (see the main text), we have

∑
1∑
|⟨χa |χb ⟩|2
Uia Ujb Uib Uja
n a̸=b
i̸=j
⏟
⏞⏞
⏟

1 ∑∑
+
|Uik |2 |Ujk |2 .
n k i̸=j
⏟
⏞⏞
⏟

n2

∑
1 ∑
1
Pij2 ≥ √
Pij = 1 =⇒
Pij2 ≥ . (A11)
n
n i
j

∑
Hence i,j Pij2 ≥ 1. Moreover, it is easy to see that the
bound is attained if Pij = 1/n.
A similar reasoning can be taken for the fully distinguishable scenario, where all oﬀ-diagonal elements of the
Gram matrix are 0, i.e., ⟨χa |χb ⟩ = 0, ∀a ̸= b. Here, all the
terms related to a ̸= b vanish, leaving the expression just
as
σd = 1 −

1∑
|Uik |4 ,
n ik

(A12)

which is also maximized for balanced interferometers.

020340-11

## PDF page 12

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

APPENDIX B: LOWER BOUNDS FOR OVERLAPS
USING THE n = 3 BALANCED
INTERFEROMETER
For the three-mode Fourier transform, in Eq. (A9) we
have found an expression for the average variance σ of the
photon number at the output modes in terms of two-photon
overlaps i (1 = AB , 2 = BC , 3 = AC ):
)
( 3
2 2 ∑
bal
i .
(B1)
σ = +
3 9 i=1
In what follows, we show how to obtain a lower bound for
all overlaps using σ . This is a natural task when using σ
to certify the pairwise indistinguishability
of a multipho∑
ton source. We start by writing i i as a function of the
measured σ :
∑

i =

i

9
σ − 3.
2

(B2)

It is easy to see that the following sequence of implications
holds in the three-photon scenario:
∑
σ > 10/9 →
i > 2 → min(i ) > 0.
(B3)

Eq. (B4) does. In particular, it guarantees a nontrivial lower
bound when σ > 8/9, whereas Eq. (B4) only does that for
σ > 10/9. In Fig. 6, we plot the two lower bounds as a
function of σ .

i

i

More precisely, when σ > 10/9, σ gives a nontrivial lower
bound for the smallest two-state overlap:
min i ≥

FIG. 6. The bounds on the two-photon overlaps. Two lower
bounds for the smallest overlap of three states, as a function of
the observed average photon-number variance σ . The blue curve
is the best lower bound, obtained from the results of Ref. [18].
The blue lower bound is nontrivial for σ > 8/9, whereas the red
lower bound is nontrivial only when σ > 10/9.

∑

i

i − 2 =

i

9
σ − 5.
2

(B4)

We can use the measured value of σ in a Fourier interferometer to obtain better lower bounds for all overlaps i .
We recall that three quantum states have three overlaps i
that satisfy the following inequality [18]:
∑
√
i − 2 1 2 3 ≤ 1.
(B5)

APPENDIX C: SEMI-DEVICE-INDEPENDENT
BOUNDS ON THE AVERAGE
INDISTINGUISHABILITY
To simplify the expression for the average photonnumber variance in Eq. (4), it is useful to introduce some
notation. We deﬁne ab = |⟨χa |χb ⟩|2 as the n × n matrix
containing all the overlaps. Moreover, we deﬁne the doubly stochastic matrix Pab = |Uab |2 associated with the
unitary U, as well as the (also doubly stochastic) matrix
Q = P T P. The expression for σ can now be written as
σ =1+

i

Using Eq. (B2) to write
σ , we obtain

∑

i i as a function of the variance

(
)2
√
9
9
1 2 3 ≥ σ − 2 ⇒ 1 2 3 ≥
σ −2 .
4
4
(B6)
The product of all i is a lower bound for each individual
i —in particular, for mini i —so
(
min i ≥ 1 2 3 ≥
i

)2
9
σ −2 .
4

(C1)

For fully distinguishable photons, we obtain
1
σ d = 1 − tr(Q).
n

(C2)

The diﬀerence between the measured values of σ , for some
distinguishability scenario, and σ d gives us
σ − σd =

(B7)

The above inequality gives us a better (larger) lower bound
for all overlaps, in terms of the observed variance σ , than

1
1∑
ab Qab − tr(Q).
n a̸=b
n

1∑
ab Qab .
n a̸=b

(C3)

Unless U is the identity matrix, the diﬀerence between σ
and σ d will be positive and will give some information

020340-12

## PDF page 13

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
about the overlap matrix . To quantify this diﬀerence, let
us rewrite the equation as follows:
σ − σd =

1
(tr(Q) − tr(Q)) .
n

(C4)

Using Eq. (C2), we have
σ − 2σ d + 1 =

tr(Q)
.
n

(C5)

Since Q and  are positive-semideﬁnite matrices, we
can use the inequality tr(Q) ≤ ||||tr(Q), where ||||
denotes the spectral norm (largest eigenvalue) of . This
leads to the following inequality:
σ − 2σ d + 1
||||
≥
.
n
n(1 − σ d )

For balanced interferometers, we have that σ = 2 − 2/n if
the photons are fully indistinguishable and σ d = 1 − 1/n
for distinguishable particles. By replacing these values on
the right-hand side of Eq. (C9), we can see that it becomes
equal to 1 and so the bound is tight in this case. For Haarrandom interferometers, the bound may become trivial.
Via numerical simulations, we have estimated the percentage of cases in which the bound is nontrivial, i.e., strictly
larger than 0, for inputs of n fully indistinguishable photons for diﬀerent values of n (see Table I). For n = 6, we
already see that this percentage is higher than 99%, which
indicates that for large photon numbers, the bound will be
nontrivial only in a vanishingly small percentage of cases.
APPENDIX D: RELATING DIFFERENT
DISTINGUISHABILITY MEASURES

(C6)

While ||||/n itself could be seen as a measure of indistinguishability, our aim here is to use this bound to obtain
¯ from Eq.
guarantees on the average indistinguishability 
(7). To do so, we ﬁrst use the fact that  = S ⊙ S T , where
S is the Gram matrix Sab = ⟨χa |χb ⟩ and ⊙ denotes the
Hadamard (entrywise) product. It follows that |||| ≤ ||S||
[54], which, together with Eq. (C6), implies that
||S||
σ − 2σ d + 1
≥
.
n
n(1 − σ d )

(C7)

In order to write an inequality in terms of the average indistinguishability, we can use the fact that ||S||F =
√
∑
a,b ab ≥ ||S||, where ||S||F is the Frobenius norm,
¯ as
which can be written in terms of 
√
n(n − 1)
||S||F
¯
 + 1/n.
(C8)
=
n
n2

In the main text, diﬀerent methods have been introduced to measure two diﬀerent quantities that can be
seen as quantiﬁers of distinguishability, namely, the average distinguishability deﬁned in Eq. (7) and the rescaled
permanent of the distinguishability matrix,
d(S) =

1
n(n − 1)

(

σ − 2σ d + 1
1 − σd

)2
−

d(S) =

Number of modes
3
4
5
6

¯ LB
Percentage of nontrivial 
80.1
92.3
97.5
99.5

(D1)

1 ∑∏
Siτ (i)
n! τ ∈S i
n

n
∑

1
Dn,k xn−k
n! k=0
n ( )
1 ∑ n
=
Dn−k,0 xn−k ,
n! k=0 k
=

1
¯ LB . (C9)
=
n−1

TABLE I. The percentage of Haar-random interferometer unitaries for which Eq. (9) gives a nontrivial bound, as a function
of the number of modes, assuming one photon per input mode.
In this investigation, we have generated 104 Haar-random interferometers of each size, considering perfectly indistinguishable
photons at the input.

Per(S)
.
n!

It is natural to ask whether we can relate these two quantities and, in particular, obtain some guarantees on d(S)
¯ and vice versa. While we do
from measurements of 
not address this question in full generality here, it is possible to obtain a direct relation between these quantities
for a simple model with uniform photon distinguishability, characterized by a distinguishability matrix Sjk = x =
¯ 1/2 , ∀j ̸= k. In this scenario, we have that
()

This expression, together with the bound ||S||F ≥ ||S|| and
Eq. (C7), implies that
¯ ≥


PRX QUANTUM 6, 020340 (2025)

(D2)

where Dn,k is the number of permutations of n elements
with k ﬁxed points and
⌊
Dn,0 =

n! + 1
e

⌋
(D3)

is the nth derangement number, deﬁned as the number
of permutations of n elements with no ﬁxed points. This
implies that the permanent of this simple family of distinguishability matrices can be computed exactly in a time
that scales polynomially in x. In addition, a simple formula

020340-13

## PDF page 14

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

that describes well the scaling of d(S) with the number of
photons for a given distinguishability parameter x can be
obtained as follows:
n ( )
1 ∑ n (n − k)! n−k
x
d(S) =
+ ϵ,
n! k=0 k
e
= xn e1/x−1 + ϵ.

(a)

(D4)

Using Eq. (D3), the error term can be bounded as
|ϵ| ≤

n ( )
1 ∑ n xn−k
(1 + x)n
≤
,
n! k=0 k e
e n!

(D5)

(b)

which decreases exponentially with n. In fact, Eq. (D4) can
be written in terms of a relative error c,
d(S) = xn e1/x−1 (1 + c),

(D6)

where c decreases exponentially in n for any ﬁxed x as long
as n ≥ e(1 + x)/x. We now compare the analytical formula
for the simple uniform-distinguishability model to a more
realistic model in which the distinguishability matrix can
have ﬂuctuations around a mean value. To generate such
random S matrices, we assume that the spectral functions
of the input photons are described by Gaussian wave packets centered at diﬀerent random times {t1 , . . . , tn }, with the
same width described by a variance σ 2 . Denoting the wave
functions of each input photon as |ti ⟩, the associated Gram
matrix is given by Ref. [15]:
(ti −tj )2
⟨ ∣ ⟩
−
Sij = ti ∣tj = e 4σ 2 ,

(D7)

where we have ignored complex phases that can be
removed by a suitable gauge transformation. To model random time delays, we choose the values of ti from a Gaussian distribution with mean 0 and variance σd2 , resulting in
a random S matrix with real entries, where
‾
│ 1
⟨ ⟩ ⟨ ⟨ ∣ ⟩ 2⟩
│
¯ = | ti ∣tj |

=
,
(D8)
⎷
ti ,tj ∈N (0,σd )
σ2
1 + 2 σd2
in which we have assumed ti , tj ∈ N (0, σd ) to be two
independent random variables. In Fig. 7, we analyze
the scaling of d(S) with the number of photons for the
uniform-distinguishability model as well as the randomdistinguishability model described above for two ﬁxed val¯ =
ues of the average indistinguishability, ¯
 = 0.8 and 
0.9. The average indistinguishability is ﬁxed by appropriately choosing the values of σd2 /σ 2 according to Eq. (D8).
We do not show the comparison to the asymptotic approximation obtained for the uniform-distinguishability model

FIG. 7. The scaling of d(S) for diﬀerent values of average indistinguishability. The behavior of the indistinguishability
measure d(S) [Eq. (D1)] with the number of photons is plotted for two ﬁxed values of the average indistinguishability, (a)
¯
¯ = 0.9, both in the uniform-distinguishability
 = 0.8 and (b) 
model (yellow points) and a random-distinguishability model
assuming random time delays. For the latter, the mean is represented by the blue points, whereas the error bars correspond to
one standard deviation calculated over 1000 samples.

d(S) ≈ xn e1/x−1 , since the approximation is very accurate
and the diﬀerence between this value and the numerically
calculated value would not be visible for any n ≥ 6. As
shown in the ﬁgure, the asymptotic decay of the values
of d(S) is well described by the uniform-distinguishability
model, specially in the high-indistinguishability regimes,
where the ﬂuctuations of the elements of the Gram
matrix—and consequently of the values of d(S)—become
¯ can give us a reasonsmaller. Hence, a measurement of 
able prediction for the value of d(S) assuming typical error
models related to time delays.
APPENDIX E: INTEGRATED PHOTONIC
PROCESSOR
The experiment has been performed by using an eightmode fully programmable IPP. The fabrication of the IPP is

020340-14

## PDF page 15

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
(a)

PRX QUANTUM 6, 020340 (2025)

(b)

FIG. 8. The implementation of Haar-random unitary matrices on the eight-mode IPP. The ﬁdelities over (a) 6000 Haar-random
matrices before the optimization algorithm and (b) 100 Haar-random matrices after the optimization algorithm. The average ﬁdelity is
marked with a horizontal dashed line.

based on FLW as described in Ref. [55]. The single-mode
waveguides have been inscribed in an aluminoborosilicate
glass substrate (Corning Eagle XG); the device features a
mesh of 28 MZIs in a rectangular conﬁguration, allowing
the implementation of any unitary matrix transformation
in eight modes. The waveguides have been optimized for
a wavelength of 928 nm and the designs of the interferometers and the mesh as a whole have been optimized
for a higher integration density as detailed in Ref. [56].
On top of each MZI, a pair of resistive heating elements
has been fabricated through a new two-metal photolithographic approach [56]. These elements allow the control
of the operation of each MZI through phase shifting via
the thermo-optic eﬀect, with a dissipated power needed
to achieve a 2π shift of about 35 mW on average per
MZI. Finally, ﬁber arrays are glued with UV-curing resin
to both the input and output ports of the device, allowing
easy interfacing with the photon sources and detectors. The
integrated interferometer has a planar footprint of about
1 × 80 mm2 and total insertion losses below 3 dB.
The model that we employ for the relationship between
the vector of currents I and the vector of MZI phases φ is
as follows:
φ = φ0 + A1 I 2 + A2 I 4 ,

(E1)

where φ0 is the vector of initial phases, while A1 and A2
are matrices representing, respectively, all the terms that
are linear in the dissipated power at each resistive element,
including the thermal-crosstalk terms, and the terms that
depend on the square of the dissipated power. A calibration procedure has been employed to retrieve the φ0 , A1 ,
and A2 arrays, in order to implement the required unitary
transformations for this work. The calibration consists of a
node-isolation algorithm in which coherent light is injected

at the input of each individual MZI [57]. The performance
of the calibration has been measured with the amplitude
fidelity ﬁgure of merit:

Fampl =

1∑
|(Ut )ij ||(Um )ij |,
8 ij

(E2)

where Ut and Um are the target unitary matrix and the
implemented unitary matrix, respectively. Through this
calibration, it has been possible to achieve an average
ﬁdelity of 0.962 over a sample of 6000 Haar-random
matrices, as reported in Fig. 8(a).
After this preliminary calibration step, the operation
of the device has been further optimized algorithmically.
In particular, the predicted currents from a large sample
size of 6000 Haar-random matrices have been calculated,
taking the initial calibration as a starting point. A machinelearning algorithm has been employed using the data as a
training set, to further tune the calibration parameters in
order to maximize the amplitude ﬁdelity. This algorithm
has optimized the model parameters, addressing imbalances in the couplers in each MZI, nonidealities in the
manual calibration process, and fabrication tolerances.
After this step, the average ﬁdelity has been increased to
0.991, as reported in Fig. 8(b).
APPENDIX F: CHARACTERIZATION OF
TRITTER UNITARY TRANSFORMATION
In this appendix, we describe the procedure employed
to reconstruct the unitary matrix U describing the balanced
tritter transformation, which has been experimentally realized using our integrated photonic device. In the linearoptics formalism, one can characterize the action of an
n-mode integrated interferometer as a n × n unitary matrix

020340-15

## PDF page 16

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

mapping the input creation mode operators ⃗a† into output
mode creation operators b⃗† :
⎛ † ⎞
† ⎞
a0
b0
⎜ a† ⎟
⎜ b† ⎟
⎜ 1 ⎟ = U⎜ 1 ⎟.
⎝ ... ⎠
⎝ ... ⎠

(F2), one can consider the following quantity:
Rij ,mn =

⎛

†
bn

(F1)

†
an

As described in Ref. [58], in order to reconstruct the elements Uαβ = |Uαβ |eiφαβ of U, it is in principle suﬃcient to
estimate the following quantities:

Vij ,mn = 1 −

PijI ,mn
PijD,mn

,

(F2)

where PijI ,mn gives the probability of recovering a coincidence click on outputs (i, j ) when injecting identical
photons into inputs (m, n), while PijD,mn identiﬁes the analogous quantity computed with distinguishable photons,
i.e., in the absence of quantum interference. The quantity Vij ,mn depends on both the moduli and the phases of
each involved unitary element, i.e., (Uim , Uin , Ujm , Ujn ). An
overcomplete characterization of the unitary U requires us
to inject a pair of photons into each possible combination of input modes. Formally, the elements present in Eq.
(F2), are associated with the 2 × 2 sub-block of the unitary
matrix U:
(
)
Uim Uin
Uij,mn =
.
(F3)
Ujm Ujn
Indeed, the output coincidence probability for indistinguishable photons is related to the square moduli of the
permanent of Uij,mn :
PijI ,mn = |Per(Uij,mn )|2 = |Uim Ujn + Uin Ujm |2
= |Uim Ujn |2 + |Uin Ujm |2

(
)
+ 2|Uim Ujn Uin Ujm | cos φim + φjn − φin − φjm ,
(F4)

(F5)

In our optical setup, based on a QD single-photon source
paired with a time-to-spatial demultiplexing setup, a direct
estimation of the quantities described in Eq. (F2) requires
taking into account the presence of the time-to-spatial
demultiplexed setup and the resulting nonunitary indistinguishability amongst photon pairs. Then, similarly to Eq.

Aτij=±T
,mn

,

(F6)

where the terms in the numerator and the denominator are
related, respectively, to the areas of the zero- (±T) delay
coincidence peaks in a typical correlation histogram measured at outputs (i, j ) when injecting a stream of photon
pairs into inputs (m, n). Here, the T represent the 12-ns
separation between subsequent peaks due to the 79-MHz
excitation of the QD. Indeed, the two-photon input state
in our optical interferometer can be described by the overlap ω, where this parameter takes into account the partial
distinguishability amongst the wave packets of the input
photons. Then, when considering the zero-delay coincidence peak Aτij=0
,mn , it can be shown that this quantity is
proportional to
τ =0
I
D
Aτij=0
,mn ∝ Pij ,mn = ωPij ,mn + (1 − ω)Pij ,mn

= |Uim Ujn |2 + |Uin Ujm |2

(
)
+ 2ω|Uim Ujn Uin Ujm | cos φim + φjn − φin − φjm .
(F7)

Conversely, a contribution to the T-delay coincidence
peak will be given by two photons separated by T
entering the interferometer in inputs {(m0 , mT ), (n0 , nT ),
(m0 , nT ), (n0 , mT )}, thus leading to
2
2
2
2
Aτij=T
,mn ∝ |Uim Ujm | + |Uin Ujn | + |Uim Ujn | + |Uin Ujm | .
(F8)

Note that in such a way, the ratios Rij ,mn (U, ω) will be a
function of both the two-photon overlap ω and the implemented unitary transformation U. Thus, by measuring the
ratios in Eq. (F6) for each possible combination of inputs
(m, n) and outputs (i, j ), together with the HOM visibilities, we can solve the following optimization problem to
recover the experimentally implemented Ũ3 transformation:

while for completely distinguishable photons, the output
coincidence probability is given by the permanent of the
moduli square matrix |Uij,mn |2 :
PijD,mn = Per(|Uij,mn |2 ) = |Uim Ujn |2 + |Uin Ujm |2 .

Aτij=0
,mn

min
U

∑ [R̃ijmn − Rijmn (U, Ṽ)]2
ijmn

σ 2 (R̃ijmn )

,

(F9)

where R̃ijmn are the experimentally measured ratios,
σ 2 (R̃ijmn ) are the associated experimental error, and
Rijmn (U, Ṽ) are the theoretical predictions for ω = Ṽ, Ṽ
being the experimental two-photon visibility. Note that,
generally, a 3 × 3 complex unitary matrix will depend
only on eight free parameters. Thus we can exploit the
parametrization presented in Ref. [59] to decrease the complexity of the optimization problem. Overall, we obtain the

020340-16

## PDF page 17

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
reconstructed matrix-element moduli:
⎛
⎞
0.611 ± 0.001 0.552 ± 0.001 0.567 ± 0.001
|Ũ3 | = ⎝0.559 ± 0.001 0.598 ± 0.001 0.575 ± 0.001⎠,
0.561 ± 0.001 0.581 ± 0.001 0.590 ± 0.001
(F10)
with phases
⎛
0
arg(Ũ3 ) = ⎝0
0

0
2.128 ± 0.004
−2.087 ± 0.004

⎞
0
−2.107 ± 0.004⎠ ,
2.155 ± 0.003
(F11)

where, without loss of generality, the complex phases
in both the ﬁrst column and row of the matrix can
be constrained to be zero. The reconstructed matrix Ũ3
†
has reached a ﬁdelity of F = |Tr(U3 Ũ3 )|/3 > 0.999 with
respect to the ideal tritter unitary U3 . Here, standard errors
have been computed as a mean over approximately 500
successfully converged instances of the problem in Eq.
exp
(F9), where the input Rijmn are statistically sampled from
a normal distribution.
APPENDIX G: TESTING THE GRAM-MATRIX
PHASE
In the main text, we have considered the measurement of
the diﬀerent tests by considering positive real-valued Gram
matrices of the form
√
√
⎞
⎛
˜ kab
˜ kac


1
⎟
⎜√
√
⎜ ˜k
k ⎟
˜
Sk = ⎜ 
(G1)
1
bc ⎟ .
⎠
⎝√ ab √
˜ kac
˜ kbc


1
To justify this assumption on the tested input-state conﬁguration, we have veriﬁed experimentally that the output
states generated from our source are well represented by
this form of the Gram matrix. This can be done by exploiting the class of cyclic interferometers employed in Ref.
[31] as a mean to measure the genuine multiphoton indistinguishability. Let us then consider a six-mode cyclic
interferometer described by the matrix
⎛

1
⎜1
1⎜
⎜eıα
Ucyc (α) = ⎜ ıα
2 ⎜e
⎝0
0

−1
−1
eıα
eıα
0
0

1
−1
0
0
1
1

1
−1
0
0
−1
−1

0
0
1
−1
1
−1

⎞
0
0⎟
⎟
−1⎟
⎟ , (G2)
1⎟
1⎠
−1

where α is a tunable phase shift. This matrix belongs to
the same class of cyclic interferometers as in Ref. [31], up

PRX QUANTUM 6, 020340 (2025)

to mode swaps and up to a diﬀerent complex-phase choice
for the elementary beam-splitter unitary cell.
Let us then consider the scenario with three input photons, described by three internal states |χa ⟩, |χb ⟩, and |χc ⟩.
In this case, the general form of the Gram matrix can be
written as
⎛
⎞
√
√
ab
√ acıϕ
√1
S = ⎝√ab √ 1
(G3)
bc e ⎠ .
ac
bc e−ıϕ
1
Let us consider the case in which the three photons are
injected into input ports [1, 3, 5] of Ucyc . The input state
† † †
can thus be described as a1 b3 c5 |0⟩, where the operators
† † †
{ai , bj , ck } label, respectively, the creation operators for
a photon in internal states |χa ⟩, |χb ⟩, and |χc ⟩ and the
input modes i, j , and k, respectively. We consider the
subset of output modes corresponding to the relevant conﬁgurations identiﬁed by Ref. [31], namely, the sets s+ =
{[1, 3, 5], [1, 4, 5], [2, 3, 6], [2, 4, 5]} and s− = {[1, 3, 6],
[1, 4, 5], [2, 3, 5], [2, 4, 6]}. We then transform the creation
operators of the input state according to the action of
the interferometer. This is performed by considering that,
according to the adopted notation, the input-output relation
∑
†
†
is âi → j [Utcyc (α)]ij âj , where t stands for the matrix
†

†

transpose, and analogously for b̂i and ĉi . The input state
† † †
a1 b3 c5 |0⟩ then evolves into
|ψcyc (α)⟩ =

1 †
†
†
†
(â1 + â2 + eıα â3 + eıα â4 )
8
†

†

†

†

†

†

†

†

b̂1 − b̂2 + b̂5 + b̂6 ) × (ĉ3 − ĉ4 + ĉ5 − ĉ6 )|0⟩.
(G4)
Let us ﬁrst focus on output conﬁguration [1, 3, 5] ∈ s+ . We
ﬁrst select the (unnormalized) portion of the output state
containing one operator for each output mode:
|ψ1,3,5 ⟩ =

)
1( † † †
† † †
â1 b̂5 ĉ3 + eıα â3 b̂1 ĉ5 |0⟩.
8

(G5)

The probability of this output conﬁguration can then
be obtained by evaluating the overlap ⟨ψ1,3,5 |ψ1,3,5 ⟩. By
repeating the same calculation for all states belonging to
sets s+ and s− , the output probabilities are found to be
P± (α, ϕ) =

]
√
√
√
1 [
1 ± ab bc ac cos(α + ϕ) ,
32
(G6)

where the ± sign depends on whether the output conﬁguration belongs to set s+ or s− .
The value of the complex phase ϕ of the Gram matrix
can be thus retrieved by injecting the three photons on
input ports [1, 3, 5] measuring the output probabilities, and

020340-17

## PDF page 18

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

( )

FIG. 9. The device programming for the cyclic interferometers. The processor has also been programmed to act as a cyclic
interferometer Ucyc (α) over the ﬁrst six modes to test the assumption of a real-valued Gram matrix. In the scheme, I corresponds
to the identity over the modes.

by measuring the probabilities of output conﬁgurations in
sets s+ and s− after programming the interferometer to
act as Ucyc (α) for diﬀerent values of α (see Fig. 9). The
results of this measurement for scenario SA are shown in
Fig. 10 for ten diﬀerent values of α covering the [0, 2π )
interval. The value of ϕ can be then obtained by grouping
the measured output threefold coincidences according to
the s+ and s− sets and by ﬁtting the grouped data with a
sinusoidal function as a function of α, given that ϕ corresponds to the phase oﬀset of the patterns. In our case
(see Fig. 11), we have found ϕ = −0.03(2), which is compatible with ϕ0 = 0 within two standard deviations. This
approach, and the corresponding experimental veriﬁcation,
justiﬁes the adoption of positive real-valued Gram matrices
in the main text.
An independent veriﬁcation on the assumption of positive real-valued Gram matrices can be also obtained

FIG. 10. Measurements with a six-mode cyclic interferometer.
The measured threefold coincidences C3 obtained by programming the IPP to act as Ucyc (α) for input modes [1, 3, 5] and
output conﬁgurations in s+ (blue bars) and s− (red bars), for different values of α. The darker regions in the bars correspond to
the 1-σ measured interval for the output threefold coincidences
according to the Poissonian statistics of the detected events.

by direct analysis of the measured three-photon distribution after the tritter transformation, assuming knowledge of the two-photon overlaps. Let us then again consider scenario SA , corresponding to measured values of
˜ Aab = 0.875(4), ˜
˜ Abc =
the overlaps 
Aac = 0.874(2), and 
0.848(2). We then consider the general Gauge-invariant
form of the Gram matrix for three photons [Eq. (G3)],
leaving ϕ as a free parameter. Let p̃(n1 ,n2 ,n3 ) be the experimentally measured probabilities after the tritter transformation Ũ3 , where (n1 , n2 , n3 ) is one of the possible photonnumber occupation conﬁgurations on the output modes.
Conversely, let p(n1 ,n2 ,n3 ) (ϕ) be the expected value of the
output probabilities for a Gram matrix having two-photon
overlap equal to the measured values reported above and
value ϕ for the phase. One can then deﬁne the following
quantity:
e(ϕ) =

∑ [p̃(n ,n ,n ) − p(n ,n ,n ) (ϕ)]2
1 2 3
1 2 3
,
2 (p̃
σ
)
(n
,n
1 2 ,n3 )
n ,n ,n

(G7)

1 2 3

where σ (p̃n1 ,n2 ,n3 ) is the experimental uncertainty associated with p̃n1 ,n2 ,n3 and the sum is extended over all possible
three-photon conﬁgurations (n1 , n2 , n3 ), where∑ni is the
occupation number of mode i, thus satisfying i ni = 3.
This quantity represents the squared error between the
expectations for a given value of ϕ and the experimentally
measured values, weighted by the experimental uncertainty. One can then retrieve the value of ϕ by numerically
minimizing this quantity. We have performed this optimization by considering as a model the closed forms of
p(n1 ,n2 ,n3 ) (ϕ) calculated in Ref. [15], which correspond to

FIG. 11. The estimation of the three-photon Gram-matrix
phase ϕ. The threefold coincidences C3 at the output of the interferometer programmed as Ucyc (α) from three photons in input
modes [1, 3, 5], grouped in output sets s+ (blue) and s− (red).
The solid lines are best ﬁt with a sinusoidal model, with the constraint that the two curves share the same phase oﬀset. The error
bars are due to the Poissonian statistic of the detected events.

020340-18

## PDF page 19

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
an ideal tritter with no multiphoton contributions from
the source, and our detailed model, including the main
sources of noises. The values of ϕ obtained with the two
choices of the expectations p(n1 ,n2 ,n3 ) (ϕ) after minimization
of e(ϕ) are found to be ϕ = 0.0053(1) and ϕ = 0.0078(1),
respectively, which are compatible with the measurement
performed via the cyclic interferometer.
APPENDIX H: MODEL OF THE EXPERIMENT
In this appendix, we provide a brief overview of the theoretical model for the experimental data, which follows
a similar approach to the one reported in Ref. [31]. In
the present implementation, we need to take into account
diﬀerent features of the platform: (i) the actual value of
the photon indistinguishability, quantiﬁed by the Gram
matrix S, (ii) multiphoton contributions from the source,
(iii) the eﬀective unitary transformation Ũ implemented by
the integrated device, and (iv) losses in the apparatus.
Regarding photon indistinguishability (i), this is taken
into account by considering that the output probabilities
are evaluated according to the theory reported in Ref.
[36], which explicitly includes the overlap between photon
states according to the Gram matrix S.
Second, we can include the eﬀect of multiphoton emission (ii) by considering that on each time bin (before the
demultiplexing module), and thus on each spatial mode,
there is a non-negligible probability that a second photon
is emitted. This corresponds to writing the input state on
each mode as
ρ = p0 |0⟩⟨0| + p1 |1⟩⟨1| + p2 |1, 1̃⟩⟨1, 1̃|,

APPENDIX I: DATA ANALYSIS
In this appendix, we provide more details on the analysis
performed on the experimental data, reported in the main
text.
1. Pseudo-number-resolved detection
The reconstruction of the bunching probabilities
reported in the main text requires the capability to distinguish the photon number at the output of each mode
of the programmed three-mode unitary transformation.
To this end, we have employed a probabilistic pseudophoton-number-detection approach. More speciﬁcally, if
one wants to detect up to three photons in a given output mode i (i = 1, 2, 3) with threshold detectors, such a
mode can be divided among three auxiliary modes iα (α =
1, 2, 3) by means of an appropriate cascade of beam splitters. In our experiment, we have employed the remaining
layers of the IPP together with an external in-ﬁber singlemode 50:50 beam splitter to perform such a balancedmode splitting. After this operation, the probability of
detecting a photon exiting mode i in the detection mode
iα will be Pi→iα = 1/3. One can then compute the probability∑
of observing an output conﬁguration ⃗n = (n1 , n2 , n3 )
with i ni = 3. It is easy to show that, given a detection
eﬃciency η and by denoting as {n1 , n2 , n3 } a valid permutation of three photons exiting three modes, the detection
probabilities of an output conﬁguration {n1 , n2 , n3 } with the
probabilities scheme read

(H1)

where the 1̃ corresponds to the presence of an additional
noise photon, which for the employed QD source has zero
overlap with the principal photon [52]. The parameters
[p0 , p1 , p2 ] can be retrieved, from the source brightness and
from the measured g (2) (0), as B ∼ p1 + p2 and g (2) (0) =
2p2 /(p1 + 2p2 )2 .
While the eﬀective unitary Ũ (iii) can be directly
included in the probability distribution calculation, the
remaining feature to be taken into account is the presence
of losses (iv). In our apparatus, we observe that losses are
approximately balanced for each photon. We can model
this eﬀect by considering that a round of balanced losses
commutes with passive linear-optical circuits [60]. Thus,
we can approximate that all losses in our apparatus can
be grouped and placed at the output of the source, where
the transmission coeﬃcient per photon η0 is obtained as
the product of all transmissivities of each element. Finally,
we observe that in our model, we do not have to take
into account imbalances in the eﬃciencies of the detection
system, since the measurement apparatus has been characterized and the output probabilities have been normalized
accordingly.

PRX QUANTUM 6, 020340 (2025)

det
P{3,0,0}
= 2η3 /9,

(I1)

det
= 2η3 /3,
P{2,1,0}

(I2)

det
P{1,1,1}
= η3 .

(I3)

These detection probabilities act as an eﬀective additional
loss factor dependent on the output conﬁguration. This
means that to estimate the full three-photon probability
distribution, it is necessary to normalize the measured
threefold counts Ñ(n1 ,n2 ,n3 ) as
det
N(n1 ,n2 ,n3 ) = Ñ(n1 ,n2 ,n3 ) /P{n
,
1 ,n2 ,n3 }

(I4)

where Ñ(n1 ,n2 ,n3 ) is the eﬀective measured number of events
associated with conﬁguration (n1 , n2 , n3 ). In such a way,
with a total of nine detectors, one can reconstruct the
full probability distribution at the output of a generic
transformation U:
N(n1 ,n2 ,n3 )
,
n1 ,n2 ,n3 N(n1 ,n2 ,n3 )

p̃(n1 ,n2 ,n3 ) = ∑

(I5)

∑
where n1 , n2 , n3 ∈ {0, 1, 2, 3} with i ni = 3. Without loss
of generality, the detection eﬃciency can be included in a

020340-19

## PDF page 20

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

TABLE II. Pseudo-number-resolved detection eﬃciencies.
The values reported are estimated according to the procedure
described above.
(n1 , n2 , n3 )

det
P{n
1 ,n2 ,n3 }

(1, 1, 1)
(2, 1, 0)
(2, 0, 1)
(1, 2, 0)
(0, 2, 1)
(0, 1, 2)
(1, 0, 2)
(3, 0, 0)
(0, 3, 0)
(0, 0, 3)

1.0
0.666
0.666
0.6646
0.6646
0.6662
0.6662
0.2216
0.2201
0.2218

where i, α ∈ (1, 2, 3). This expression can be then used
det
, which we
to measure the detection coeﬃcients P{n
1 ,n2 ,n3 }
report in Table II.

2. Reconstruction of bunching probabilities with
distinguishable photons
To estimate the bunching probabilities in the fully distinguishable scenario for the random unitaries, we have
exploited the fact that the three-photon probabilities are a
convex combination of single-particle ones. Given a unitary matrix U describing the programmed interferometer,
where the matrix element Uij describes the transmission
amplitude between input mode j and output mode i, and
considering an input state with one photon on each of the
three input modes, the following relations hold:

direct estimation of the experimental mode-detection probabilities P̃i→iα . These coeﬃcients have been measured by
setting U = I and injecting the IPP with single-photon
states at each input mode i, measuring

D
p(3,0,0)
=

3
∏

|U1l |2 ,

(I7)

|U2l |2 ,

(I8)

l=1

Niα
P̃i→iα = ∑
,
j Niα

D
=
p(0,3,0)

(I6)

3
∏
l=1

TABLE III. The full table of the results obtained for the 23 unitaries for the scenario associated with the Gram matrix SA . Here,
r̃FB (SA ) = p̃FB (SA )/p̃FB (SD ) represents the experimentally measured overall bunching ratio rFB (SA ) = per(SA )/per(SD ), while σ̃ (Ui )
indicates the experimentally measured photon-number variance at the output of the interferometer. We denote by Ñ(n1 ,n2 ,n2 ) the raw
counts measured at the output of the pseudo-number-resolving detection setup.
r̃FB (SA )

σ̃ (Ui )

¯
LB (Ui )

Ñ(3,0,0)
(×103 )

4.84(9)
4.8(1)
4.77(6)
4.7(1)
4.87(5)
5.04(4)
4.99(7)
5.06(8)
5.16(7)
4.83(3)
4.91(5)
5.2(1)
4.99(8)
4.91(4)
5.3(2)
5.09(5)
5.0(1)
4.86(7)
5.09(7)
4.87(4)
4.85(6)
4.9(2)
4.97(7)

0.736(3)
0.606(3)
0.857(4)
0.711(4)
1.071(5)
1.129(5)
0.889(4)
0.800(4)
0.937(4)
1.163(5)
0.985(4)
0.766(3)
0.846(4)
1.101(5)
0.388(2)
0.992(4)
0.693(3)
0.844(4)
0.830(4)
1.031(4)
0.949(4)
0.460(2)
0.824(4)

−0.098(3) 0.26(2)
−0.170(2) 0.92(3)
−0.004(4) 2.15(5)
−0.114(3) 0.90(3)
0.289(9)
2.15(5)
0.41(1)
2.88(5)
0.94(3)
0.030(5)
−0.048(4) 1.79(4)
0.084(5)
2.06(5)
0.51(1)
3.57(6)
0.145(6)
1.05(3)
−0.071(3) 0.63(3)
−0.010(4) 1.53(4)
0.349(9)
2.87(5)
−0.248(1) 0.12(1)
0.155(6)
1.48(4)
−0.121(3) 0.25(2)
−0.013(4) 2.30(5)
−0.025(4) 0.62(2)
0.216(7)
1.04(3)
0.097(5)
0.16(1)
−0.232(1) 0.036(6)
−0.030(4) 1.57(4)

p̃(3,0,0)

p̃(3,0,0)
D
p(3,0,0)

Ñ(0,3,0)
(×103 )

p̃(0,3,0)

p̃(0,3,0)
D
p(0,3,0)

Ñ(0,0,3)
(×103 )

p̃(0,0,3)

p̃(0,0,3)
D
p(0,0,3)

0.0138(8)
4.9(3)
1.58(4) 0.083(2) 4.9(1) 0.47(2) 0.025(1) 4.7(2)
0.048(2)
4.7(1)
0.34(2) 0.0176(9) 5.3(3) 0.56(2) 0.029(1) 4.6(2)
0.114(2)
4.76(9)
1.29(4) 0.069(2) 4.7(1) 0.44(2) 0.023(1) 4.9(2)
0.064(2)
4.6(1)
0.66(3) 0.047(2) 4.8(2) 0.23(2) 0.016(1) 5.0(3)
0.145(3)
5.1(1)
2.30(5) 0.156(3) 4.78(9) 0.89(3) 0.060(2) 4.6(1)
0.162(3)
5.15(8)
2.93(5) 0.166(3) 5.08(8) 1.72(4) 0.096(2) 4.8(1)
0.053(2)
4.8(2)
1.97(4) 0.113(2) 4.9(1) 0.89(3) 0.051(2) 5.3(2)
0.103(2)
5.0(1)
0.85(3) 0.049(2) 5.0(2) 0.48(2) 0.027(1) 5.2(2)
0.127(3)
5.1(1)
1.25(4) 0.077(2) 5.3(1) 0.53(2) 0.033(1) 4.8(2)
0.171(3)
4.99(7)
3.61(6) 0.175(3) 4.88(7) 3.00(5) 0.144(2) 4.60(8)
4.7(1)
2.85(5) 0.155(3) 4.98(8) 1.35(4) 0.073(2) 4.9(1)
0.057(2)
0.034(1)
5.1(2)
0.068(8) 0.0037(4) 13(2)
1.38(4) 0.074(2) 5.1(1)
1.55(4) 0.084(2) 4.7(1) 0.10(1) 0.0052(5) 8.1(8)
0.082(2)
5.2(1)
0.152(3)
5.16(9)
2.20(5) 0.118(2) 4.87(9) 2.76(5) 0.147(2) 4.70(8)
0.0065(6)
5.6(5)
0.40(2) 0.022(1) 5.3(3) 0.068(8) 0.0037(4) 5.3(6)
0.079(2)
5.2(1)
2.16(5) 0.116(2) 5.3(1) 2.29(5) 0.122(2) 4.90(9)
0.0136(9)
5.1(3)
1.02(3) 0.056(2) 5.2(2) 0.92(3) 0.050(2) 4.7(1)
0.120(2)
4.79(9)
0.21(1) 0.0109(8) 5.0(3) 0.62(2) 0.032(1) 5.1(2)
0.034(1)
5.3(2)
1.70(4) 0.093(2) 5.4(1) 1.28(4) 0.069(2) 4.7(1)
0.055(2)
5.3(2)
3.00(5) 0.158(3) 4.95(8) 2.21(5) 0.116(2) 4.57(9)
0.0086(7)
8.3(6)
1.27(4) 0.067(2) 5.3(1) 3.10(6) 0.163(3) 4.58(7)
0.0019(3) 7(1) × 10 0.51(2) 0.027(1) 4.6(2) 0.019(4) 0.0010(2)
4(1)
0.079(2)
5.0(1)
0.19(1) 0.0097(7) 7.6(5) 1.63(4) 0.082(2) 4.7(1)

020340-20

## PDF page 21

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY

PRX QUANTUM 6, 020340 (2025)

TABLE IV. The full table of the results obtained for the 23 unitaries, for the scenario associated with the Gram matrix SB′ . Here,
r̃FB (SB′ ) = p̃FB (SB′ )/p̃FB (SD ) represents the experimentally measured overall bunching ratio rFB (SB′ ) = per(SB′ )/per(SD ). We denote
by Ñ(n1 ,n2 ,n3 ) the raw counts measured at the output of the pseudo-number-resolving detection setup, for the two-photon input as
described above. The three-photon bunching probabilities can be then retrieved as {p̃(n1 ,n2 ,n3 ) T12 , p̃(n1 ,n2 ,n3 ) T22 , p̃(n1 ,n2 ,n3 ) T32 }, where Tij
∣ ∣2
represents the measured square moduli ∣Uij ∣ of the programmed unitary matrix.
r̃FB (SB′ )

Ñ(2,0,0)

p̃(2,0,0) T12

(×104 )
1.83(2)
1.77(1)
1.77(1)
1.71(2)
1.814(6)
1.785(7)
1.776(9)
1.75(1)
1.86(1)
1.766(5)
1.782(9)
1.81(2)
1.83(2)
1.743(6)
1.84(2)
1.851(8)
1.78(2)
1.760(9)
1.91(1)
1.788(6)
1.838(9)
1.99(3)
1.819(6)

1.25(1)
1.87(1)
1.30(1)
0.717(8)
2.68(2)
1.10(1)
0.95(1)
0.467(7)
0.701(8)
1.39(1)
2.16(1)
0.166(4)
0.427(7)
0.812(9)
1.78(1)
1.12(1)
1.49(1)
2.76(2)
1.13(1)
0.242(5)
0.050(2)
0.0041(6)
2.66(2)

0.00510(4)
0.0184(1)
0.0400(3)
0.0211(2)
0.0490(2)
0.0604(5)
0.0190(2)
0.0336(5)
0.0461(5)
0.0596(5)
0.0211(1)
0.0109(3)
0.0298(4)
0.0480(5)
0.00206(1)
0.0299(3)
0.00499(4)
0.0421(2)
0.0117(1)
0.0176(4)
0.0028(1)
0.00037(6)
0.0290(1)

D
p(0,0,3)
=

3
∏

p̃(3,0,0)
D
p(3,0,0)

1.80(1)
1.80(1)
1.67(1)
1.52(2)
1.728(9)
1.92(2)
1.71(2)
1.65(2)
1.87(2)
1.74(1)
1.75(1)
1.66(4)
1.87(3)
1.62(2)
1.78(1)
1.95(2)
1.88(1)
1.675(8)
1.83(2)
1.72(3)
2.7(1)
14(2)
1.841(9)

|U3l |2 ,

Ñ(0,2,0)
(×104 )
0.432(7)
0.056(2)
0.354(6)
0.238(5)
2.31(2)
1.24(1)
2.08(1)
1.31(1)
0.669(8)
1.75(1)
1.05(1)
1.33(1)
0.747(9)
2.61(2)
1.52(1)
1.85(1)
0.238(5)
0.066(3)
1.03(1)
2.63(2)
1.51(1)
0.490(7)
0.029(2)

(I9)

l=1

∣ ∣2
which depend only on the square moduli ∣Uij ∣ of the unitary matrix U. The moduli of the unitary matrix elements
can be measured by injecting the IPP with single photons
into each input j and measuring the corresponding counts
Nij from each output mode i. Note that here the mode splitting matrix has not been programmed on the device, thus
resulting in a one-to-one correspondence between the input
and output modes. Then, the moduli square of the unitary
matrix can be reconstructed as
∣ ∣2
Nij
Tij = ∣Uij ∣ = ∑
.
i Nij

p̃(0,3,0)
D
p(0,3,0)

p̃(0,2,0) T22

(I10)

3. Experimental data tables
We conclude this appendix by describing the dataanalysis procedure supporting the data shown in Fig. 3.
In particular, given a three-mode unitary transformation
U programmed on the IPP, for the scenario related to the
Gram matrix SA , we have proceeded by acquiring raw

0.0309(5)
0.0055(2)
0.0281(5)
0.0189(4)
0.0583(3)
0.0548(5)
0.0397(2)
0.0179(1)
0.0276(3)
0.0646(4)
0.0554(5)
0.000480(4)
0.0322(4)
0.0452(2)
0.00734(5)
0.0403(3)
0.0192(4)
0.0062(2)
0.0330(3)
0.0596(3)
0.0253(2)
0.0113(2)
0.0027(2)

1.80(3)
1.65(7)
1.93(3)
1.89(4)
1.78(1)
1.68(1)
1.74(1)
1.83(1)
1.91(2)
1.81(1)
1.78(2)
1.75(1)
1.81(2)
1.873(9)
1.78(1)
1.83(1)
1.78(4)
2.8(1)
1.91(2)
1.865(9)
2.01(1)
1.94(3)
2.1(1)

Ñ(0,0,2)

p̃(0,0,2) T32

p̃(0,0,3)
D
p(0,0,3)

0.0102(2)
0.01115(6)
0.00847(4)
0.00616(4)
0.0270(4)
0.0351(2)
0.0187(4)
0.0106(2)
0.01175(6)
0.0547(4)
0.0270(3)
0.0269(3)
0.001088(6)
0.0548(4)
0.0016(1)
0.0449(5)
0.0184(2)
0.01102(4)
0.0289(4)
0.0434(2)
0.0622(4)
0.000423(6)
0.0309(1)

1.94(4)
1.79(1)
1.802(9)
1.90(1)
2.09(3)
1.743(8)
1.95(4)
2.02(3)
1.736(9)
1.75(1)
1.82(2)
1.87(2)
1.69(1)
1.75(1)
2.3(2)
1.81(2)
1.75(2)
1.730(7)
1.94(3)
1.717(8)
1.75(1)
1.81(3)
1.778(8)

(×104 )
0.272(5)
2.36(2)
2.77(2)
1.51(1)
0.405(6)
3.09(2)
0.264(5)
0.403(6)
2.49(2)
1.82(1)
0.572(8)
0.606(8)
2.10(1)
1.51(1)
0.015(1)
0.726(9)
0.656(8)
3.47(2)
0.425(7)
2.71(2)
1.56(1)
0.460(7)
3.03(2)

threefold events Ñ(n1 ,n2 ,n3 ) at the output of the interferometric mesh, over a time span of approximately 1 h, in
the complete conﬁguration composed by the unitary transformation plus the mode-splitting setup. We have then
corrected such events as in Eq. (I4) to compute the experimental probability distribution p̃(n1 ,n2 ,n3 ) for each output
conﬁguration (n1 , n2 , n3 ) as in Eq. (I5). Then, we have
computed the bunching ratio r̃FB (SA ) as
r̃FB (SA ) =

p̃(3,0,0) + p̃(0,3,0) + p̃(0,0,3)
p̃FB (SA )
=
, (I11)
D
D
D
p̃FB (SD )
p(3,0,0) + p(0,3,0) + p(0,0,3)

D
where the elements p(n
have been reconstructed by
1 ,n2 ,n3 )
measuring the moduli squared of the unitary transforma∣ ∣2
tion ∣Uij ∣ as described above. In Table III, we report
the complete set of experimental data collected, related
to the 23 chosen conﬁgurations of the three-mode unitary
transformation U.
For the scenario described by the Gram matrix SB′ ,
that is a scenario in which one photon is made completely distinguishable from the others, the reconstruction
of the probability distribution in such a scenario can be

020340-21

## PDF page 22

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

performed by injecting the interferometer with two photons in input ports (1, 3), and the measure the two-photon
probabilities {p̃(2,0,0) , p̃(0,2,0) , p̃(0,0,2) }. To estimate the corresponding elements {p̃(3,0,0) , p̃(0,3,0) , p̃(0,0,3) } for this indistinguishability scenario, it is then enough to perform a
classical convolution of the two-photon probabilities with
the probabilities Ti2 obtained with a distinguishable photon
input in port 2 according to
p̃(3,0,0) = p̃(2,0,0) T12 ,

(I12)

p̃(0,3,0) = p̃(0,2,0) T22 ,

(I13)

p̃(0,0,3) = p̃(0,0,2) T32 .

(I14)

The bunching ratio r̃FB (SB′ ) can be then estimated from
these reconstructed probabilities according to the following expression:
r̃FB (SB′ ) =
=

p̃(2,0,0) T12 + p̃(0,2,0) T22 + p̃(0,0,2) T32
D
D
D
p(3,0,0)
+ p(0,3,0)
+ p(0,0,3)
p̃FB (SB′ )
.
p̃FB (SD )

(I15)

The complete set of data in this scenario SB′ with the 23
random unitaries is reported in Table IV.

[1] V. Giovannetti, S. Lloyd, and L. Maccone, Advances in
quantum metrology, Nat. Photonics 5, 222 (2011).
[2] E. Polino, M. Valeri, N. Spagnolo, and F. Sciarrino, Photonic quantum metrology, AVS Quantum Sci. 2, 024703
(2020).
[3] F. Albarelli, M. Barbieri, M. G. Genoni, and I. Gianani, A
perspective on multiparameter quantum metrology: From
theoretical tools to applications in quantum imaging, Phys.
Lett. A 384, 126311 (2020).
[4] S. Aaronson and A. Arkhipov, in Proceedings of the
Forty-Third annual ACM Symposium on Theory of Computing (ACM Press, San Jose, California, USA, 2011),
pp. 333–342.
[5] C. S. Hamilton, R. Kruse, L. Sansoni, S. Barkhofen, C. Silberhorn, and I. Jex, Gaussian boson sampling, Phys. Rev.
Lett. 119, 170501 (2017).
[6] A. P. Lund, A. Laing, S. Rahimi-Keshari, T. Rudolph, J. L.
O’Brien, and T. C. Ralph, Boson sampling from a Gaussian
state, Phys. Rev. Lett. 113, 100502 (2014).
[7] D. J. Brod, E. F. Galvão, A. Crespi, R. Osellame, N. Spagnolo, and F. Sciarrino, Photonic implementation of boson
sampling: A review, Adv. Photonics 1, 1 (2019).
[8] M. Bentivegna, N. Spagnolo, C. Vitelli, F. Flamini, N.
Viggianiello, L. Latmiral, P. Mataloni, D. J. Brod, E. F.
Galvão, A. Crespi, R. Ramponi, R. Osellame, and F. Sciarrino, Experimental scattershot boson sampling, Sci. Adv. 1,
e1400255 (2015).
[9] L. S. Madsen, F. Laudenbach, M. F. Askarani, F. Rortais,
T. Vincent, J. F. F. Bulmer, F. M. Miatto, L. Neuhaus, L.
G. Helt, M. J. Collins, A. E. Lita, T. Gerrits, S. W. Nam, V.

D. Vaidya, M. Menotti, I. Dhand, Z. Vernon, N. Quesada,
and J. Lavoie, Quantum computational advantage with a
programmable photonic processor, Nature 606, 75 (2022).
[10] H.-S. Zhong, et al., Quantum computational advantage
using photons, Science 370, 1460 (2020).
[11] H.-S. Zhong, et al., Phase-programmable Gaussian boson
sampling using stimulated squeezed light, Phys. Rev. Lett.
127, 180502 (2021).
[12] Y.-H. Deng, et al., Gaussian boson sampling with pseudophoton-number-resolving detectors and quantum computational advantage, Phys. Rev. Lett. 131, 150601 (2023).
[13] F. Bouchard, A. Sit, Y. Zhang, R. Fickler, F. M. Miatto, Y.
Yao, F. Sciarrino, and E. Karimi, Two-photon interference:
The Hong-Ou-Mandel eﬀect, Rep. Prog. Phys. 84, 012402
(2020).
[14] C. K. Hong, Z. Y. Ou, and L. Mandel, Measurement
of subpicosecond time intervals between two photons by
interference, Phys. Rev. Lett. 59, 2044 (1987).
[15] A. J. Menssen, A. E. Jones, B. J. Metcalf, M. C. Tichy, S.
Barz, W. S. Kolthammer, and I. A. Walmsley, Distinguishability and many-particle interference, Phys. Rev. Lett. 118,
153603 (2017).
[16] V. S. Shchesnovich and M. E. O. Bezerra, Collective phases
of identical particles interfering on linear multiports, Phys.
Rev. A 98, 033805 (2018).
[17] D. J. Brod, E. F. Galvão, N. Viggianiello, F. Flamini,
N. Spagnolo, and F. Sciarrino, Witnessing genuine multiphoton indistinguishability, Phys. Rev. Lett. 122, 063602
(2019).
[18] E. F. Galvão and D. J. Brod, Quantum and classical
bounds for two-state overlaps, Phys. Rev. A 101, 062110
(2020).
[19] T. Giordani, D. J. Brod, C. Esposito, N. Viggianiello, M.
Romano, F. Flamini, G. Carvacho, N. Spagnolo, E. F.
Galvão, and F. Sciarrino, Experimental quantiﬁcation of
four-photon indistinguishability, New J. Phys. 22, 043001
(2020).
[20] T. Giordani, C. Esposito, F. Hoch, G. Carvacho, D. J. Brod,
E. F. Galvão, N. Spagnolo, and F. Sciarrino, Witnesses of
coherence and dimension from multiphoton indistinguishability tests, Phys. Rev. Res. 3, 023031 (2021).
[21] R. Wagner, A. Camillini, and E. F. Galvão, Coherence and
contextuality in a Mach-Zehnder interferometer, Quantum
8, 1240 (2024).
[22] T. Giordani, R. Wagner, C. Esposito, A. Camillini, F. Hoch,
G. Carvacho, C. Pentangelo, F. Ceccarelli, S. Piacentini,
A. Crespi, N. Spagnolo, R. Osellame, E. F. Galvao, and
F. Sciarrino, Experimental certiﬁcation of contextuality,
coherence, and dimension in a programmable universal
photonic processor, Sci. Adv. 9, eadj4249 (2013).
[23] N. Viggianiello, F. Flamini, M. Bentivegna, N. Spagnolo,
A. Crespi, D. J. Brod, E. F. Galvao, R. Osellame, and
F. Sciarrino, Optimal photonic indistinguishability tests in
multimode networks, Sci. Bull. 63, 1470 (2018).
[24] J. J. Renema, H. Wang, J. Qin, X. You, C. Lu, and J. Pan,
Sample-eﬃcient benchmarking of multiphoton interference
on a boson sampler in the sparse regime, Phys. Rev. A 103,
023722 (2021).
[25] M. C. Tichy, M. Tiersch, F. de Melo, F. Mintert, and
A. Buchleitner, Zero-transmission law for multiport beam
splitters, Phys. Rev. Lett. 104, 220405 (2010).

020340-22

## PDF page 23

CHARACTERIZATION OF MULTIPHOTON INDISTINGUISHABILITY
[26] M. C. Tichy, K. Mayer, A. Buchleitner, and K. Mølmer,
Stringent and eﬃcient assessment of boson-sampling
devices, Phys. Rev. Lett. 113, 020502 (2014).
[27] A. Crespi, Suppression laws for multiparticle interference
in Sylvester interferometers, Phys. Rev. A 91, 013811
(2015).
[28] A. Crespi, R. Osellame, R. Ramponi, M. Bentivegna, F.
Flamini, N. Spagnolo, N. Viggianiello, L. Innocenti, P.
Mataloni, and F. Sciarrino, Suppression law of quantum
states in a 3D photonic fast Fourier transform chip, Nat.
Commun. 7, 10469 (2016).
[29] C. Dittel, R. Keil, and G. Weihs, Many-body quantum interference on hypercubes, Quantum Sci. Technol. 2, 015003
(2017).
[30] N. Viggianiello, F. Flamini, L. Innocenti, D. Cozzolino,
M. Bentivegna, N. Spagnolo, A. Crespi, D. J. Brod, E.
F. Galvão, R. Osellame, and F. Sciarrino, Experimental
generalized quantum suppression law in Sylvester interferometers, New J. Phys. 20, 033017 (2018).
[31] M. Pont, R. Albiero, S. E. Thomas, N. Spagnolo, F. Ceccarelli, G. Corrielli, A. Brieussel, N. Somaschi, H. Huet, A.
Harouri, A. Lemaître, I. Sagnes, N. Belabas, F. Sciarrino, R.
Osellame, P. Senellart, and A. Crespi, Quantifying n-photon
indistinguishability with a cyclic integrated interferometer,
Phys. Rev. X 12, 031033 (2022).
[32] F. Hoch, T. Giordani, N. Spagnolo, A. Crespi, R. Osellame, and F. Sciarrino, Characterization of multimode linear optical networks, Adv. Photonics Nexus 2, 016007
(2023).
[33] R. van der Meer, P. Hooijschuur, F. H. Somhorst, P. Venderbosch, M. de Goede, B. Kassenberg, H. Snijders, C. T.
Taballione, J. Epping, H. van den Vlekkert, N. Walk, P.
W. H. Pinkse, and J. J. Renema, Experimental demonstration of an eﬃcient, semi-device-independent photonic
indistinguishability witness, ArXiv:2112.00067.
[34] M. Oszmaniec, D. J. Brod, and E. F. Galvão, Measuring relational information between quantum states, and
applications, New J. Phys. 26, 013053 (2024).
[35] A. E. Jones, A. J. Menssen, H. M. Chrzanowski, T. A.
Wolterink, V. S. Shchesnovich, and I. A. Walmsley, Multiparticle interference of pairwise distinguishable photons,
Phys. Rev. Lett. 125, 123603 (2020).
[36] M. C. Tichy, Sampling of partially distinguishable bosons
and the relation to the multidimensional permanent, Phys.
Rev. A 91, 022316 (2015).
[37] N. Spagnolo, C. Vitelli, L. Sansoni, E. Maiorino, P. Mataloni, F. Sciarrino, D. J. Brod, E. F. Galvao, A. Crespi,
R. Ramponi, and R. Osellame, General rules for bosonic
bunching in multimode interferometers, Phys. Rev. Lett.
111, 130503 (2013).
[38] S. Aaronson and T. Hance, Generalizing and derandomizing Gurvits’s approximation algorithm for the permanent,
Quantum Inf. Comput. 14, 541 (2014).
[39] V. Shchesnovich, Tight bound on the trace distance between
a realistic device with partially indistinguishable bosons
and the ideal BosonSampling, Phys. Rev. A 91, 063842
(2015).
[40] M. Robbio, M. G. Jabbour, L. Novo, and N. J. Cerf, A
central limit theorem for partially distinguishable bosons,
ArXiv:2404.11518.

PRX QUANTUM 6, 020340 (2025)

[41] W. R. Clements, P. C. Humphreys, B. J. Metcalf, W.
S. Kolthammer, and I. A. Walmsley, Optimal design
for universal multiport interferometers, Optica 3, 1460
(2016).
[42] O. Gazzano, S. Michaelis de Vasconcellos, C. Arnold, A.
Nowak, E. Galopin, I. Sagnes, L. Lanco, A. Lemaître, and
P. Senellart, Bright solid-state sources of indistinguishable
single photons, Nat. Commun. 4, 1425 (2013).
[43] A. Nowak, S. Portalupi, V. Giesz, O. Gazzano, C. Dal
Savio, P.-F. Braun, K. Karrai, C. Arnold, L. Lanco, I.
Sagnes, A. Lemaître, and P. Senellart, Deterministic and
electrically tunable bright single-photon source, Nat. Commun. 5, 3240 (2014).
[44] N. Somaschi, V. Giesz, L. De Santis, J. Loredo, M. P.
Almeida, G. Hornecker, S. L. Portalupi, T. Grange, C.
Anton, J. Demory, C. Gómez, I. Sagnes, N. D. LanzillotiKimura, A. Lemaître, A. Auﬀeves, A. G. White, L. Lanco,
and P. Senellart, Near-optimal single-photon sources in the
solid state, Nat. Photonics 10, 340 (2016).
[45] H. Ollivier, I. Maillette de Buy Wenniger, S. Thomas, S.
C. Wein, A. Harouri, G. Coppola, P. Hilaire, C. Millet, A.
Lemaitre, I. Sagnes, O. Krebs, L. Lanco, J. C. Loredo, C.
Antòn, N. Somaschi, and P. Senellart, Reproducibility of
high-performance quantum dot single-photon sources, ACS
Photonics 7, 1050 (2020).
[46] S. Thomas, M. Billard, N. Coste, S. Wein, H. Ollivier,
O. Krebs, L. Tazaïrt, A. Harouri, A. Lemaitre, I. Sagnes,
C. Anton, L. Lanco, N. Somaschi, J. C. Loredo, and
P. Senellart, Bright polarized single-photon source based
on a linear dipole, Phys. Rev. Lett. 126, 233601
(2021).
[47] M. Pont, G. Corrielli, A. Fyrillas, I. Agresti, G. Carvacho,
N. Maring, P.-E. Emeriau, F. Ceccarelli, R. Albiero, P. H.
Ferreira, N. Somaschi, J. Senellart, I. Sagnes, M. Morassi,
A. Lemaitre, P. Senellart, F. Sciarrino, M. Liscidini, N.
Belabas, and R. Osellame, High-ﬁdelity four-photon GHZ
states on chip, npj Quantum Inf. 10, 50 (2024).
[48] J. C. Loredo, N. A. Zakaria, N. Somaschi, C. Anton, L. de
Santis, V. Giesz, T. Grange, O. Broome, Matthew A. Gazzano, G. Coppola, I. Sagnes, A. Lemaitre, A. Auﬀeves, P.
Senellart, M. P. Almeida, and A. G. White, Scalable performance in solid-state single-photon sources, Optica 3, 433
(2016).
[49] G. Corrielli, A. Crespi, and R. Osellame, Femtosecond
laser micromachining for integrated quantum photonics,
Nanophotonics 10, 3789 (2021).
[50] T. Giordani, F. Flamini, M. Pompili, N. Viggianiello,
N. Spagnolo, A. Crespi, R. Osellame, N. Wiebe, M.
Walschaers, A. Buchleitner, and F. Sciarrino, Experimental statistical signature of many-body quantum interference,
Nat. Photonics 12, 173 (2018).
[51] G. Rodari, F. Hoch, A. Suprano, T. Giordani, E. Negro,
G. Carvacho, N. Spagnolo, E. F. Galvão, and F. Sciarrino, Polarization-encoded photonic quantum-to-quantum
Bernoulli factory based on a quantum dot source, Sci. Adv.
10, eado6244 (2024).
[52] H. Ollivier, S. E. Thomas, S. C. Wein, I. M. de Buy Wenniger, N. Coste, J. C. Loredo, N. Somaschi, A. Harouri,
A. Lemaitre, I. Sagnes, L. Lanco, C. Simon, C. Anton,
O. Krebs, and P. Senellart, Hong-Ou-Mandel interference

020340-23

## PDF page 24

GIOVANNI RODARI et al.

PRX QUANTUM 6, 020340 (2025)

with imperfect single photon sources, Phys. Rev. Lett. 126,
063602 (2021).
[53] M. Walschaers, Statistical Benchmarks for Quantum Transport in Complex Systems: From Characterisation to Design
(Springer, 2018).
[54] R. A. Horn, Norm bounds for Hadamard products and an
arithmetic-geometric mean inequality for unitarily invariant
norms, Linear Algebra Appl. 223, 355 (1995).
[55] G. Corrielli, S. Atzeni, S. Piacentini, I. Pitsios, A. Crespi,
and R. Osellame, Symmetric polarization-insensitive directional couplers fabricated by femtosecond laser writing,
Opt. Express 26, 15101 (2018).
[56] R. Albiero, C. Pentangelo, M. Gardina, S. Atzeni, F. Ceccarelli, and R. Osellame, Toward higher integration density in

femtosecond-laser-written programmable photonic circuits,
Micromachines 13, 1145 (2022).
[57] C. Pentangelo, N. Di Giano, S. Piacentini, R. Arpe, F.
Ceccarelli, A. Crespi, and R. Osellame, High-ﬁdelity and
polarization-insensitive universal photonic processors fabricated by femtosecond laser writing, Nanophotonics 13,
2259 (2024).
[58] A. Laing and J. L. O’Brien, Super-stable tomography of any
linear optical device, ArXiv:1208.2868.
[59] J. B. Bronzan, Parametrization of SU(3), Phys. Rev. D 38,
1994 (1988).
[60] M. Oszmaniec and D. J. Brod, Classical simulation of photonic linear optics with lost particles, New J. Phys. 20,
092002 (2018).

020340-24
