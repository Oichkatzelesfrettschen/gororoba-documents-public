Source: see manifest row of the PDF
PDF sha256: 9afbc77bb0966c817a2354f7eb99e3a9cde9a561cf36df506c698313f5efd1aa
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: text-layer)

# Transcription of liu_2025_exploring_the_boundary_of_quantum_correlations_with_a_time_domain_optical_processor_arxiv_html_print.pdf

Transcription of `liu_2025_exploring_the_boundary_of_quantum_correlations_with_a_time_domain_optical_processor_arxiv_html_print.pdf` in this directory, 65 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 14, 20 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-13, 15-19, 21-65 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

This is
experimental
HTML to
improve
accessibility.
We invite you
to report
Why
Report Back to
Download
rendering
HTML conversions sometimes
display
errors due to
content
that did not convert
HTML?
Issue
Abstract
PDF
errors. Learn
correctly from the source. This paper uses the following packages that are not yet
more about
supported bythis
theproject
HTML conversion tool. Feedback on these issues are not necessary; they
are known and
being worked on.
andare
help
improve
conversions.
failed: multibib

failed: tipa
Authors: achieve the best HTML results from your LaTeX submissions by following these
best practices.

License: CC BY 4.0
arXiv:2208.07794v3 [quant-ph] 29 Jan 2025

Exploring the boundary of quantum correlations
with a time-domain optical processor
Zheng-Hao Liu ∘,#
CAS Key Laboratory of Quantum Information, University of Science and Technology of China,
Hefei 230026, China
CAS Centre for Excellence in Quantum Information and Quantum Physics, University of Science
and Technology of China, Hefei 230026, China
Beijing QBoson Quantum Technology Co., Ltd., Beijing 100015, China

Yu Meng ◆,#

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 1 of 65

## PDF page 2

Yu Meng ◆,#
CAS Key Laboratory of Quantum Information, University of Science and Technology of China,
Hefei 230026, China
CAS Centre for Excellence in Quantum Information and Quantum Physics, University of Science
and Technology of China, Hefei 230026, China

Yu-Ze Wu #
School of Mathematical Sciences, University of Science and Technology of China, Hefei 230026,
China

Ze-Yan Hao
CAS Key Laboratory of Quantum Information, University of Science and Technology of China,
Hefei 230026, China
CAS Centre for Excellence in Quantum Information and Quantum Physics, University of Science
and Technology of China, Hefei 230026, China

Zhen-Peng Xu
zhen-peng.xu@ahu.edu.cn
School of Physics and Optoelectronics
Engineering, Anhui University, 230601 Hefei,
People’s Republic of China

Cheng-Jun Ai

Naturwissenschaftlich-Technische Fakultät,
Universität Siegen, Walter-Flex-Straße 3, 57068
Siegen, Germany

Hai Wei
Beijing QBoson Quantum Technology Co., Ltd., Beijing 100015, China

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 2 of 65

## PDF page 3

Kai Wen
wenk@boseq.com
Beijing QBoson Quantum Technology Co., Ltd., Beijing 100015, China
Quantum Science Center of Guangdong-Hong Kong-Macao Greater Bay Area, Shenzhen 518045,
China

Jing-Ling Chen
chenjl@nankai.edu.cn
Theoretical Physics Division, Chern Institute of Mathematics, Nankai University, Tianjin 300071,
China

Jie Ma
jiema@ustc.edu.cn
School of Mathematical Sciences, University of Science and Technology of China, Hefei 230026,
China
Hefei National Laboratory, University of Science and Technology of China, Hefei 230088, China

Jin-Shi Xu
jsxu@ustc.edu.cn

Chuan-Feng Li
cfli@ustc.edu.cn

Guang-Can Guo
CAS Key Laboratory of Quantum Information, University of Science and Technology of China,
Hefei 230026, China

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 3 of 65

## PDF page 4

Hefei 230026, China
CAS Centre for Excellence in Quantum Information and Quantum Physics, University of Science
and Technology of China, Hefei 230026, China
Anhui Province Key Laboratory of Quantum Network, University of Science and Technology of
China, Hefei, Anhui 230026, China
Hefei National Laboratory, University of Science and Technology of China, Hefei 230088, China

(January 28, 2025)

Abstract
Contextuality is a hallmark feature of the quantum theory that captures its incompatibility
with any noncontextual hidden-variable model. The Greenberger–Horne–Zeilinger (GHZ)type paradoxes are proofs of contextuality that reveal this incompatibility with deterministic logical arguments. However, the GHZ-type paradox whose events can be included in the
fewest contexts and which brings the strongest nonclassicality remains elusive. Here, we
derive a GHZ-type paradox with a context-cover number of three and show this number
saturates the lower bound posed by quantum theory. We demonstrate the paradox with a
time-domain fiber optical platform and recover the quantum prediction in a 37-dimensional
setup based on high-speed modulation, convolution, and homodyne detection of time-multiplexed pulsed coherent light. By proposing and studying a strong form of contextuality in
high-dimensional Hilbert space, our results pave the way for the exploration of exotic quantum correlations with time-multiplexed optical systems.
$\circ$
$\circ$Present address: Center for Macroscopic Quantum States (bigQ), Department of Physics, Technical

University

of

Denmark,

Fysikvej,

2800

Kongens

Lyngby,

Denmark.

https://manekime-

ow.github.io/
$\lozenge$

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 4 of 65

## PDF page 5

$\lozenge$Present address: Center for Hybrid Quantum Networks (Hy-Q), The Niels Bohr Institute, Universi-

ty of Copenhagen, DK-2100 Copenhagen Ø, Denmark.
$\#$
$\#$

These authors contributed equally to this work.

Introduction
Measurement in quantum theory is the origin of many nonclassical effects [1, 2, 3]. A measurement of a physical property in the classical world reveals its preexisting value. Such an
interpretation cannot hold true in the quantum regime, not only because noncommuting
operators have no meaningful joint values [4], but also due to the impossibility of specifying the preexisting value, even for a set of commuting operators, without specifying the full
set of observables jointly measured. The latter effect, known as the Kochen–Specker contextuality [5], captures some most defining aspects of quantum correlations. It has a wide
spectrum of applications like randomness expansion [6, 7], dimension witnessing [8, 9] and
self-testing [10, 11], and can be considered as the origin of nonclassicality behind Bell nonlocality [12, 13].

Intriguingly, the failure of noncontextual hidden-variable descriptions can manifest as a
“perfect” form of contextuality, namely, the Greenberger–Horne–Zeilinger (GHZ)-type paradoxes [14, 15], where the quantum system generates an outcome deterministically different
from the noncontextual prediction. Such paradoxes formulated as inequality-free logical
arguments serve as a conceptually clear and mathematically strong [16] alternative of noncontextuality inequalities for detecting contextuality. We argue that these perfect contextuality are also a resource for the acceleration and universality of quantum computing [17, 18,
19, 20, 21, 22]. We refer our readers to the Supplementary Material for a more in-depth discussion about the role of contextuality in quantum computing.

The figure of merit of a GHZ-type paradox can be defined in several ways. It has been
proved that the construction in [23] uses the fewest number of rays [24] to show the para-

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 5 of 65

## PDF page 6

dox, and the number of contexts that must be utilized to prove the logical argument (the
“number of context”) is at least four [25]. Here, we focus on an alternative point: what is
the minimal number of contexts required to include, or “cover” all the events in a GHZ-type
paradox? Hereafter, we call this quantity the “number of context-cover” to differentiate
from the number of context. Later, the word choice will be made more reasonable. The
number of context-cover is a proper measure of the strength of a GHZ-type paradox for
two reasons: firstly, when transformed into noncontextuality inequalities, a GHZ-type paradox with a lower number of context-cover yields a larger ratio of violation. This violation
also sustains to the one of Kochen–Specker-type paradox [24], a fundamental resource for
various applications [20, 26, 27]. Secondly, to observe a GHZ-type paradox, the number of
groups of fundamental event probabilities required is also equal to the number of contextcover. Therefore, the GHZ-type paradox with the lowest number of context-cover is a
strong resource of nonclassicality that is expected to have potential applications in quantum protocols. However, after more than 30 years of GHZ’s seminal work [14], the exact
lower bound of this number is still undetermined.

Here, we take a step towards answering the above question and observing this strong form
of GHZ-type paradox. Specifically, we have constructed and demonstrated such a paradox
with a number of context-cover of only three. Inspired by the graph-theoretic approach to
quantum correlations [28], we have developed a method to systematically construct GHZtype paradoxes by searching for graphs whose graph-theoretic constants satisfy a set of
criteria. Based on this method, we have explicitly constructed a three-context GHZ-type
paradox that can be realized with a set of 37-dimensional measurements, and proved its
optimality in the sense that the number of contexts to include all the events cannot be further reduced. This way, the proposed GHZ-type paradox delineates the boundary of correlations allowed by the quantum theory.

To experimentally study the three-context GHZ-type paradox, we have built a fiber-based
photonic processor capable of reproducing the probability of all the high-dimensional measurements in the paradox with the time-bin degree of freedom of photons. Our experiment
was based on high-speed electro-optical modulation, multiplication, and convolution on
temporal modes of pulsed coherent light, with which we implemented a prepare-and-mea-

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 6 of 65

## PDF page 7

sure experiment through a correspondence between single-photon and coherent state interference [29] and extracted all the statistics required in a test of contextuality [30]. A major contribution from the experimental side is that we have made the setup scalable by detecting the complete amplitude and phase information of the coherent light via homodyne
detection. This enabled us to substantially expand the applicable Hilbert space dimension
and achieve the desired high-dimensionality.

Our results epitomized the potential of the temporal-multiplexed optical system, which has
found applications in coherent Ising machine [31, 32, 33], continuous-variable measurement-based quantum computing [34, 35, 36, 37], and (Gaussian) boson sampling [38, 39,
40], in investigating exotic quantum correlations. As any Kochen–Specker set utilizing 𝑛
context-cover implies the existence of a GHZ-type paradox with 𝑛 − 1 context-cover [24],
our finding also paves the way to the search for a Kochen–Specker set whose events can be
included in only four context-cover. We also envisage that our findings could benefit the
search for exotic quantum correlations that are the building blocks for quantum computing
or even constitute a step toward achieving stronger quantum advantage in shallow circuits
[21, 22].

Results
Graph-theoretic approach to GHZ-type paradox

The GHZ-type paradoxes are logical proofs and extreme manifestations of contextuality.
They refer to scenarios where, given an assemblage of event probabilities, the predictions
by quantum theory and any noncontextual model for another set of event probabilities

contradict each other in a deterministic way. Formally, a GHZ-type paradox can be expressed using the conditional probabilities as follows: where 1 | [𝑗, 𝑘], 𝑗, 𝑘 ∈ ℕ + denotes an
event where the outcome of the 𝑘-th projective measurement in the 𝑗-th context is 1, 𝑚𝑗 is

the number of measurements in the 𝑗-th context, and 𝑛 is the total number of contexts
used in the paradox. The qualifiers Q and NCHV indicate the probabilities shall be calculated via the quantum theory and a noncontextual hidden-variable model, respectively. We

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 7 of 65

## PDF page 8

can also label all the events with a single index: [𝑗, 𝑘] = ∑ 𝑖 = 1 𝑚𝑖 + 𝑘. In layman’s terms, a
𝑗−1

GHZ-type paradox indicates some events deemed impossible by noncontextual models are
bound to happen according to the quantum theory. In the Supplementary Material, we provide an explicit illustration using the original GHZ paradox.

To study the mathematical structure of contextuality, a common approach is the graphtheoretic approach to quantum correlations [28] which uses an exclusivity graph to capture
the impossibility of some events taking place simultaneously. Concretely, the vertices 𝑉(𝐺)
of the exclusivity graph 𝐺 represent the events of observing certain measurement outcomes, and its edges 𝐸(𝐺) connect pairs of exclusive events. Once an exclusivity graph is
given, the sum of event probabilities in noncontextual and quantum theories will be bounded by graph constants, namely, the independence number and Lovász number [30, 41]:
∑ Pr(1 | 𝑖) −

𝑖∈𝑉

∑ Pr(1, 1 | 𝑖, 𝑗)

(𝑖, 𝑗) ∈ 𝐸

Q
NCHV
⩽ 𝛼(G) ⩽ 𝜗(G).

(1)

Here, Pr(1, 1 | 𝑖, 𝑗) is the probability of simultaneously observing events 𝑖, 𝑗; this term compensates for the deviation from exclusivity [42]. Graphs with a large ratio 𝜗/𝛼 thus have the
merit of producing more significant inconsistency between noncontextual and quantum
theories. The advantage of the graph-theoretic approach is that many properties of the underlying quantum correlation can be revealed by the graph constants, and the concrete setting for the quantum states and measurements achieving these properties can then be
found efficiently via semidefinite programming.

To date, no direct method has, to the best of our knowledge, been established for studying
the GHZ-type paradox via this approach. Here, we undertake this task and elucidate the link
between a GHZ-type paradox and the clique number of its exclusivity graph, or equivalently, the chromatic number of the graph with the rays in the GHZ-type paradox being its orthogonal representation [43]. Formally, our finding can be formulated as the following theorem.

Theorem 1 (informal).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 8 of 65

## PDF page 9

Necessary and sufficient condition for a graph 𝐺 to be the exclusivity graph of an 𝑛-context
GHZ-type paradox is
2) = 𝑛,
𝛼(𝐺) = 𝑛 − 1, 𝜗(𝐺) = 𝑛, and 𝜒( 𝐺

2 is the graph complement of 𝐺 and 𝜒( 𝐺
2) is its chromatic number.
where 𝐺

(2)

Note that the notion of 𝑛-context throughout this paper refers the number of context-cover
instead of the number of context; to complete the logical proof, additional contexts may be
counted. The proof of Theorem 1 and the discussion regarding the above point can be
found in the Methods section. As the left-hand side value of Eq. (1) in any no-signaling theory is upper bounded by the exclusivity graph’s fractional packing number 𝛼 ∗ (𝐺), and
𝛼 ∗ (𝐺) ⩽ 𝜒( 𝐺
2) [44], a quantum correlation associated with a GHZ-type paradox must also
be a fully contextual correlation [45] that lays on the boundary of the no-signaling polytope, but the converse is not necessarily true. Our results thus clearly show the role of the
GHZ-type paradox as a peculiar class of the strongest quantum correlation allowed by special relativity.

A three-context GHZ-type paradox
Because the graphs of exclusivity in GHZ-type paradoxes have a fixed 𝜗 − 𝛼 = 1, a GHZtype paradox whose events can be covered by fewer contexts is associated with a larger
quantum–classical ratio and stronger nonclassicality. However, the minimum of this number is not known: as we will prove in the Methods section, it must be greater than two, but
all the known examples of GHZ-type paradox have the number of context-cover of at least
four, leaving the three-context case unexplored. Although noncontextuality inequality [46]
and logical proofs of contextuality [47] using three context-cover have been studied in experiments [48, 49], the corresponding exclusivity graph—a pentagon (cf. Fig. 1(a))—has only
a 𝜗 − 𝛼 = √5 − 2 < 1. As such, the quantum violation is less than 1 and the logical proof
does not constitute a GHZ-type paradox. Further, a GHZ-type paradox can also be con-

structed from a Kochen–Specker set by selecting one ray as the input state and removing
all its orthogonal rays, but all known Kochen–Specker sets employ at least five contexts [50

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 9 of 65

## PDF page 10

]. The exclusivity graph in the smallest case (cf. Fig. 1(b)) is exactly the same as that in the
original GHZ paradox. The existence of a four-context Kochen–Specker set is thus a longstanding open question.

Fig. 1: Graphs of exclusivity. The vertices with the same color belong to the same context.
(a) A pentagon is the simplest graph which shows nonclassicality when considered as an
exclusivity graph. Measurements with such an exclusivity structure exhibit a three-context
Hardy-type paradox, but the quantum success probability is less than 1. (b) The graph
complement of the Shrikhande graph is the underlying exclusivity structure of the original
GHZ paradox with four contexts. In both (a) and (b) the connected vertices represent
mutually exclusive events. (c) The Perkel graph is the orthogonal representation of the rays
in the three-context GHZ-type paradox. Note that the exclusivity graph here is
complementary to the Perkel graph. Black (gray) lines connect the (non-)exclusive events.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 10 of 65

## PDF page 11

All the above observations make the search for a three-context GHZ-type paradox an interesting task. Towards this objective, our next contribution is to identify an exclusivity graph
hosting such a paradox. According to 1, the desired exclusivity graph 𝐺 has some fixed

graph-theoretic constants, including an independence number of 𝛼(𝐺) = 2 and a Lovász
number of 𝜗(𝐺) = 3; moreover, its graph complement should have a chromatic number of
2) = 3, that is, 𝐺
2 is triangle-free and three-colorable. We have identified the graph
𝜒( 𝐺
complement of the Perkel graph [51] as shown in Fig. 1(c) as a candidate for the exclusivity
graph. The approach we use is to search across the graphs with known graph constants,
and we do not know if a graph with fewer vertices exists that can satisfy the same conditions, due to the difficulty of traversing the exponentially many possible graphs. Nevertheless, we also prove in the Methods section that these requirements cannot be satisfied by a
strongly regular graph [52] which is highly symmetric and widely used in previous proofs of
contextuality [14, 23], thus posing further limitations to the existence of other examples.

Once the candidate exclusivity graph is determined, we can calculate the explicit form of
the measurement events by representing them with a set of rays; each ray corresponds to
the nondegenerate eigenstate of a projector. These rays form an orthogonal representation
of the Perkel graph. The procedure for obtaining the orthogonal representation is to first
determine the Gram matrix of the rays by semidefinite programming known as Lovász optimization [41], and then solve the individual rays by Cholesky decomposition and Gaussian
elimination. The procedure will be extensively discussed in the Supplementary Material. We
realized the semidefinite programming using a Python package cvxopt and the Cholesky
decomposition using Mathematica 11.2. Assuming perfect exclusivity as dictated by the
exclusivity graph so the second term of Eq. (1) vanishes, the three-context GHZ-type paradox can be expressed as:
𝑝1 := ∑ 𝑘 = 1 Pr(1 | 𝑘) = 1,
19

𝑝2 := ∑ 𝑘 = 20 Pr(1 | 𝑘) = 1,
38

0, NCHV,
𝑝3 := ∑ 𝑘 = 39 Pr(1 | 𝑘) = {
1, Q.
57

(3)

The explicit definition of the individual rays, as well as the Gram matrix, will be given in the
Methods section. The Gram matrix we found has a rank of 37, which is also the Hilbert

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 11 of 65

## PDF page 12

space dimension in which the corresponding set of rays can be embedded. As will be further discussed in the Supplementary Material, we do not know if a lower-dimensional realization of the Gram matrix exists, as the set of rank-limited matrices is non-convex and we
could not efficiently run the optimization.

Towards a time-multiplexed optical test

Our proposed three-context GHZ-type paradox would be worth an experimental test, both
because it uses the least possible number of orthonormal basis and that a noncontextuality
inequality with a high quantum–classical ratio of 3/2 can be checked via its comprised
measurements. According to Eq. (3), to observe such a paradox, it is sufficient to measure
the projection probability of the initial state on various measurement basis, and additionally to confirm the orthogonality of measurements corresponding to mutually exclusive
events. The procedure is akin to Cabello’s simplified method for testing contextuality using
prepare-and-measure experiments [30] with graph-theoretic approach-based inequalities:
as shown in Fig. 2(a) and (b), it has the merit of requiring no sequential, non-demolition
measurements.

However, the requirement of high-dimensional measurements poses a substantial challenge for experimentally observing the three-context GHZ-type paradox. While such measurements would in principle be amenable in a multi-qubit system available in different
platforms [53, 54, 55], due to the complicated form of the projectors, they will require many
entangling operations and suffer from decreased accuracy. Noticing this point, we chose to
use the photons as a natural courier for encoding high-dimensional quantum information.
Our endeavor made use of the observation that a strong coherent light can provide a faithful phase reference—often called a “local oscillator” in the context of continuous-variable
quantum optics, allowing the extraction of a photonic object’s full complex amplitude information. With this information, we were able to devise a strategy to decompose a high-dimensional measurement into relatively lower-dimensional subspaces, thus greatly enhancing the scalability of the platform and facilitating the experiment. Despite the highly desirable scalability, our current setup is not fully compatible with a noncontextual theory description; therefore, we could not claim the experiment to be a test of contextuality in a

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 12 of 65

## PDF page 13

strict sense. However, this can be fixed by changing the last measurement stage back to
photodetection, as we will discuss close to the end of the paper.

We utilized the time-bin degree of freedom of light to encode the analogous time-bin qudit
and implement the prepare-and-measure experiment. The choice of degree of freedom is
due to that it can best accommodate the requirement of a local oscillator. Concretely, we
used the following encoding method to map a 𝑑-dimensional quantum state onto a series
of pulsed coherent states:
|𝒂⟩ = (𝑎1 𝑎2 ⋯ 𝑎𝑑 ) †

↔ {|𝛼1 , Δ𝑡⟩, |𝛼2 , 2Δ𝑡⟩, ⋯, |𝛼𝑑 , 𝑑Δ𝑡⟩}.

(4)

The encoded states contain two entries: The first entry, 𝛼𝑘 = 𝛼
˜𝑎𝑘 denotes the displacement of the individual coherent states and 𝛼
˜ is a constant determined by the intensity of
the input coherent state. The second entry specifies the time that it is generated. The encoding is possible with coherent states because when subjected to an interferometer network transformation, the probability distribution of a single photon at the output ports is

the same as the intensity distribution if the single photon is replaced by a coherent state [
29]. In our experiment, this coherent state train was created by casting intensity modulation on a pulsed laser.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 13 of 65

## PDF page 14

<math>\boldsymbol{o}_2 |\boldsymbol{a}_2\rangle</math>
<math>|\mathbf{o}_2|</math>
<math>\boldsymbol{a}_2</math>
<math>\mathbf{o}_2</math>

<math>\oplus</math>
<math>\oplus</math>
<math>\langle \mathbf{o}_b | \boldsymbol{a}_b \rangle</math>
<math>\langle {\bf o}_b |</math>
max size
<math>\bigoplus</math>
<math>\oplus</math>
per round
<math>a_b</math>
<math>\mathbf{o}_b</math>
LO
<math>|\tilde{\mathbf{c}}\rangle</math>
<math>\ket{\tilde{\bm{a}}}</math> ::
<math>\mathbf{C}</math>
Round 1
<math>\mathbf{T}</math>
<math>\begin{aligned} \langle \mathbf{o}_1 | \boldsymbol{a}_1 \rangle \ \langle \mathbf{o}_2 | \boldsymbol{a}_2 \rangle \end{aligned}</math>
<math>\langle {\bf o}_1 |</math>
1
Round 2
<math>\langle \mathbf{o}_b | \boldsymbol{a}_b \rangle</math>
<math>\langle \mathbf{o}_2 |</math>
Round <i>b</i>
Round <math>b + 1</math>
<math>\|\boldsymbol{a}_b\rangle</math>
<math>\langle \mathbf{o}_b \rangle</math>
<math>\langle \mathbf{o}_b | \boldsymbol{a}_b \rangle</math>
<math>=\langle \mathbf{o}|\boldsymbol{a}\rangle</math>
<math>\propto \langle \mathbf{o}_b | \boldsymbol{a}_b \rangle_{\mathsf{COS}} | \theta_k \rangle</math>
D
<math>\theta_k</math>
<math>\Delta t = 3\tau</math>
<math>\sum (\lambda, \lambda, \gamma, \cdots)</math>

Fig. 2: <b>Experimental design.</b> (a) A contextuality test requires a set of prepare-and-measure
probabilities, obtained from either single-photon or coherent-state interference. The
challenge is the required Hilbert-space dimension can exceed the size that a photonic
processor can handle. (b) The high-dimensional inner product can be decomposed into
subspaces and evaluated separately. (c) Extraction of the inner product with a local
oscillator (LO). In the first b rounds of the experiment, the inner products in subspaces were
measured. In the last round, a ray was reconstructed from previous measurement results,
and its projection on a unit basis recovered the result of the high-dimensional interference.
https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com
2/5/25, 4:47 PM
Page 14 of 65

## PDF page 15

(d) Sketch of the experimental setup. An intensity modulator prepared various input states.
A fiber ring implemented optical convolution. The output mode at a specific time
corresponded to the post-measurement state, whose amplitude was subsequently
extracted via homodyne detection. IM intensity modulator, PM phase modulator.

Fig. 3: Data acquisition. (a) An exemplary control signal and recorded oscilloscope trace
centered at the measure period. The control signal consists of an intensity notch for
synchronization, a 𝜋/2-pulse at the local oscillator for phase calibration, and the intensity

modulations encoding the preparation and convolution basis. The gray background
indicates the lock period and the colored bands highlight the points where operations are
performed or data is being taken. (b) The deduced phase error of the convolution fiber ring
and the local oscillator. The red-colored data points had at least one phase error greater
than 𝜋/24 and were excluded from the final calculation.

To measure the encoded state on a specific basis, hereafter denoted as |\textopeno⟩, we
sent the pulse train into a fiber ring that has a round-trip time of Δ𝑡, so a pulsed coherent

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 15 of 65

## PDF page 16

state would meet and interfere with another emitted at a later time after it circumnavigated
the ring. The output modes from the ring thus acquired a component from every earlier
pulse. Effectively, it can be expressed as a discrete convolution of the input state 𝒂 ∗ 𝒄0 with
the kernel of convolution being 𝒄0 = {𝑐1 , 𝑐2 , …, 𝑐𝑘 , …}, where 𝑐𝑘 denote the complex amplitude ejection ratio of a pulse upon its 𝑘-th encounter of the output coupler. Focusing on the
𝑑
output pulse at time 𝑑Δ𝑡, we found that it will have an amplitude of ∑ 𝑘 = 1 𝑎(𝑑 + 1 − 𝑘) 𝑐𝑘
which

is

equivalent

to

the

inner

product,

⟨\textopeno0 |𝒂⟩,

where

\textopeno0 = {𝑐𝑑 , 𝑐𝑑 − 1 , …, 𝑐1 } represents the first 𝑑-terms of the entry-reversed convolu-

tion kernel. Further, the basis of the projective measurement |\textopeno⟩ can be adjusted
from |\textopeno0 ⟩ by driving the intensity modulator before the pulses enter the fiber ring.
The probability of a qudit measurement can thus be efficiently evaluated by looking at the
strength of the output pulse at a specific time.

In practice, a fiber ring is inevitably accompanied by ejection into unwanted time-bins, insertion losses, and chromatic dispersion, so the ejection ratio quickly decreases for a large
number of loops. As such, the kernel of convolution only has a limited number of meaningful nonzero terms, hampering the capability of measuring high-dimensional states. To overcome this limitation we notice the input state and measurement basis can be written into a
𝑏
𝑏
direct-sum expansion: 𝒂 = ⨁ 𝑘 = 1 𝒂𝑘 , \textopeno = ⨁ 𝑘 = 1 \textopeno𝑘 , where 𝑏 is the total
number of partitions, such that Dim(𝒂𝑘 ) = Dim(\textopeno𝑘 ) and ∑ 𝑘 = 1 Dim(𝒂𝑘 ) = Dim(𝒂).
Then, the inner product can be expressed as:

⟨\textopeno|𝒂⟩ = ∑𝑘 = 1 ⟨\textopeno𝑘 |𝒂𝑘 ⟩.
𝑏

𝑏

(5)

The decomposition thus offered a possibility to divide-and-conquer the high-dimensional
interference. The challenge in using such a decomposition is that the summation is taken
for complex amplitudes instead of photodetection probabilities, and monitoring the power
output for each of the right-hand side terms does not provide sufficient information for reconstructing the projection probabilities.

We employ homodyne detection to resolve this final challenge and provide the setup scalability: by interfering the optical mode with the local oscillator on a balanced beam splitter,

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 16 of 65

## PDF page 17

the intensity difference between the two output ports will be proportional to the mode’s inphase amplitude with the local oscillator. Since the projectors in the three-context GHZtype paradox (Eq. (3)) comprise only real numbers, the in-phase amplitude can already capture all information of the input coherent states after convolution, and thus the complex
amplitude was recovered by experimentally observable quantities.

Overall, our experimental design is outlined in Fig. 2(c); a concrete example of encoding the
pulse sequence for a prepare-and-measure experiment is provided in the Supplementary
𝑏
Material. Firstly, we expressed the state |𝒂⟩ as the decomposed form: 𝒂 = ⨁ 𝑘 𝒂𝑘 . For
=1

each sub-normalized state 𝒂𝑘 we employed the optical convolution with the kernel
\textopeno𝑘 and homodyne detection to register the amplitude on the desired partial mea-

surement basis. Measurement of all the 𝑏 groups of inner products yielded a sequence of 𝑏
elements—all the right-hand-side terms in Eq. (5). To extract the initial high-dimensional
𝒂 ⟩ = {⟨\textopeno𝑘 |𝒂𝑘 ⟩}
inner product, we encoded these 𝑏 elements as a new ray: |˜
setting

the

kernel

to

be

˜ | = {1, 1, …, 1}T ,
⟨\textopeno

the

initial

inner

𝑏

𝑘=1

. By

product

˜ |𝒂
⟨\textopeno|𝒂⟩ = ⟨\textopeno
˜⟩ can be measured via another round of optical convolu-

tion. Finally, the measurement probabilities in Eq. (3) was calculated as the absolute square
of the homodyne results normalized against a set of orthonormal basis.

Experimental implementation

We realized the prepare-and-measure experiment in a fiber-based, electro-optic modulated
photonic processor as shown in Fig. 2(d); the full experimental setup is extensively described in the Methods section. We have developed a MATLAB 2020b script to control an
arbitrary function generator and a digital oscilloscope to run a fully automated experiment.

A correct and stable phase at different parts of our setup is a crucial requirement for implementing the desired convolution and homodyne detection. To this objective, we used a
photodetector at the second output port of the convolution ring’s injection fiber coupler
and the DC monitor output of the homodyne detector to extract the phase information, and

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 17 of 65

## PDF page 18

adopted a lock–measure scheme to alternate the setup between a phase locking operation
and the pulse measurement. The details about the individual locks can be found in the
Methods section. The scheme ran on a 10 kHz cycle: in the first 98.5 𝜇s of the cycle (lock
period), the intensity modulator was set at maximal transmission, and the servo (TEM
Messtechnik LaseLock) implemented active phase stabilization. In the last 1.5 𝜇s (measure
period), the electro-optic modulators delivered the modulations to prepare the actual input
state and implement the change of the measurement basis. The resulted output intensity

from the setup was much weaker than in the lock period; however, due to the low-pass filter
in the servo and the limited frequency-response range, the piezo controlling the phases of
the setup could not respond to the sudden change of the input. This way, the phases would
remain almost constant during the measure period.

We registered the homodyne outcome with an oscilloscope. An exemplary waveform together with the curves of modulation voltages is depicted in Fig. 3(a). When the last pulse
for encoding the input state exited the fiber ring, the homodyne result was recorded, and
the outcome would be proportional to one term of the desired inner product (right-hand
side of Eq. (5)). To verify the locking phase, we added a 𝜋/2 phase on the local oscillator be-

fore the pulses for measurement basis selection, and observed the response from the homodyne detector. As detailed in the Methods section, both the convolution and the homodyne phases can be extracted from two checkpoint voltages in the waveform. The result of
phase calibration is shown in Fig. 3(b). The standard deviations of the convolution phase
and the local oscillator phase error were measured to be 2.74 ∘ and 3.94 ∘ . Additionally, we
discarded all data points with at least one phase error greater than 7.5 ∘ to avoid undesired
noise.

With the precise electro-optic modulation and phase-locking, the obtained measurement
probabilities closely resembled that would be in an ideal quantum prepare-and-measure
experiment. The ideality can be best witnessed in that whenever the state rays of preparation and measurements were orthogonal, the homodyne detection amplitude would almost
vanish. We confirmed the above witness by implementing the prepare-and-measure procedure corresponding to the |𝐸(𝐺)| = 1425 pairs of exclusive rays and projectors in the orthogonal representation of the Perkel graph. Note that the procedures were not implement-

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 18 of 65

## PDF page 19

ed if at least one of the prepared or measured rays equaled the computational basis; in
which case the probability would only depend on the extinction ratio of intensity modulation and not on interference. The results for the remaining events (cf. Fig. 4(a)) demonstrat-

ed an average detection probability for such a procedure of only 1.74(11) % . Henceforth, the
error bars corresponding to 1𝜎 standard deviations were obtained from bootstrapping. The
high orthogonality ensured the statistics from our prepare-and-measure procedure conformed to the requirements of exclusivity, so the prerequisite of exclusivity in the theory
was indeed fulfilled in this platform.

Next, we proceed to test the three-context GHZ-type paradox by directly measuring the
three sums of probabilities in Eq. (3). Our experimental result gives:
𝑝1 = 0.9939(15), 𝑝2 = 0.9980(2), 𝑝3 = 0.9983(2).

(6)

It was in excellent accord with quantum predictions and displayed strong disagreement
with the prediction of the noncontextual theories.

Note that the orthogonality between exclusive events is never perfect in a real experiment,
so the observation of a GHZ-type paradox should be taken as a strong, but qualitative indication of contextuality. To substantiate the observation, we further implement a test of the
noncontextuality inequality (Eq. (1)) associated with the same exclusivity graph. Violation of
such an inequality compensates for the deviation from ideal exclusivity and can refute noncontextual models with realistic experimental data [30]. The test is made possible using the
same data from the GHZ-type paradox which gives the first term of Eq. (1), together with a
verification of orthogonality between all projectors supposed to be orthogonal to each other, which gives the first term of Eq. (1). We describe the detailed procedure in the Methods section. We observe:
∑

𝑖∈𝑉

𝛼(𝐺) +

Pr(1 | 𝑖) = 2.9902(4),

∑ Pr(1, 1 | 𝑖, 𝑗) = 2.651(4)

(𝑖, 𝑗) ∈ 𝐸

(7)

which means that, after correcting for the imperfect exclusivity and adding the correlation

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 19 of 65

## PDF page 20

term to the ideal-case classical bound, the experimental data still violated the upper bound
of noncontextuality by 8.06 standard deviations and thus rejecting such a description with
almost absolute confidence.
A
57
<math>\times 10^{-2}</math>
50
5.
Measurement
40
2.5
30
0.
20
20
30
40
50
57
Preparation
B
Exclusivity—corrected NCHV
Qmax
NCHV <b>←</b>
3
2
0
Fig 4: Experimental results (a) Calculated values of the second term in (1) for each pair of
https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com
2/5/25, 4:47 PM
Page 20 of 65

## PDF page 21

Fig. 4: Experimental results. (a) Calculated values of the second term in (1) for each pair of
compatible projectors that does not equal the computational basis. The colors stand for the
probabilities of ideally orthogonal measurements not giving exclusive responses; for nonorthogonal measurements rays the corresponding boxes are left as white. (b) Experimental
results for the three-context GHZ-type paradox vs. the predictions of noncontextual
models, exclusivity-corrected noncontextual models and the quantum theory. The three
colored bands correspond to the three sums of probabilities in Eq. (3), respectively.

Discussion
In conclusion, we have derived and observed a highly exotic quantum correlation by exploring the potential of optical interferometry. Firstly, by developing the graph-theoretical approach for the study of the GHZ-type paradoxes, we have found a strong GHZ-type contextuality whose constituent events can be included in only three contexts—the least possible
number of contexts in theory, but still reveal a deterministic contradiction between classical
and quantum descriptions of the same underlying correlations. When translated into experimentally testable noncontextuality inequality, the argument also gives the largest quantum–classical ratio among all GHZ-type paradoxes. Interestingly, the argument was found
by examining named graphs with known graph-theoretic constants, instead of using the
modern computer-assisted search method [42, 24] or being derived from a Bell inequality
already with a large quantum violation [56]. In fact, with a vertex clique cover number less
than four, the exclusivity graph here cannot host any Bell-type inequalities. Our result thus
highlights the link between the most exotic quantum correlations and graphs with high degrees of symmetry and may shed light on the search for other strong forms of quantum
correlations.

Secondly, we have exploited a time-multiplexed optical setup to reproduce the full probability distribution of the three-context GHZ-type paradox in an analogous system. By virtue
of the direct sum decomposition of a high-dimensional state into lower-dimensional components and the detection of the full complex amplitude information using the homodyne

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 21 of 65

## PDF page 22

detection, we dramatically scaled up the dimensionality that the optical interferometry can
study and implemented a 37-dimensional prepare-and-measure experiment with a precision high enough to demonstrate contextuality. Our result clearly showcased the power of
combining the time-bin interferometry and homodyne detection, and it would not be hard
to directly apply this method in the study of synthetic dimensions of photons [57, 58, 59] to
reveal the rich physics in phase space and more complicated quantum dynamic features in
high-dimensional systems.

Our experimental platform using the time-multiplexing technique is also well-compatible
with quantum computing applications. The technique was adopted in large-scale entanglement (i.e., cluster state) generation [60] and Gaussian operations based on measurementbased quantum computing [36]; moreover, non-Gaussian operations can also be implemented with homodyne measurements together with photodetection [61] to obtain universality. Another relevant application would be the Gaussian boson sampling [62] that is a
leading approach to quantum computational advantage [38]. When photons from multiple
output times are looked at, the convolution ring setup is equivalent to the fully connected
interferometer in Reference [39] and can gain universality by adding another layer of ring [
63, 40, 64, 65]. Compared to the interferometer based on the spatial degree of freedom,
the platform here has the advantage of being relatively easy to build, economically friendly,
and possessing better scalability.

A limitation of the current experiment is that the setup does not include any kind of operation that produces discretized event outcomes. This causes us to be unable to detect contextuality in the normal sense by measuring the probability of individual events. We could
recover the probability distribution that violates the noncontextuality inequality, but these
probabilities cannot be interpreted in the way that a discrete-variable noncontextuality theory would require. In fact, as the Wigner function of the system is nonnegative, it can be
taken as a continuous-variable hidden-variable description and it is noncontextual. Also,
the current process of probability calculation involves Eq. (5) which in turn requires quantum theory. However, we believe both of the points can be fixed by using photodetection as
the last stage of the measurement. In Supplementary Material, we describe a setup that
would address all the above issues and promote the experiment to a real contextuality test.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 22 of 65

## PDF page 23

It would be a reasonable to target at realizing such a setup in a succeeding work.

We believe this work has opened several avenues for future research. From a fundamental
perspective, the existence of a three-context GHZ-type paradox leaves open the possibility
of finding a Kochen–Specker set whose events can be covered by four contexts. It would be
interesting to consider if such a set can already be constructed as a state-independent version of the GHZ-type paradox here, using some methods of expansion, e.g., as in Reference
[66]. Pertinent to this topic, we also prove in the Methods section that if any four-context
Kochen–Specker set does exist then the four contexts must be disjoint; hence, this
Kochen–Specker set would not accept a simple parity proof [23, 67]. Finally, an interesting
endeavor would be to convert the large amount of nonclassicality in the three-context
GHZ-paradox to a quantum advantage. Based on contextuality, quantum advantage in
shallow circuits has been composed [22]. We hope our findings can be used to build even
stronger quantum advantages in high-dimensional systems.

Methods
Proofs of the propositions. Here we prove the necessary and sufficient conditions for a
graph to be the exclusivity graph of a set of rays in a GHZ-type paradox (Theorem 1). This
gives a corollary that the minimum number of context-cover in a GHZ-type paradox is three
(Theorem 2). Then, we show that no strongly regular graph can host a three-context GHZtype paradox (Theorem 3), and that if a Kochen–Specker set consists only four contextcover, then those contexts are all disjoint (Theorem 4). Finally, in Fig. 5, we give the explicit
definition of the individual rays in the three-context GHZ-type paradox and the corresponding Gram matrix. We restate every proposition before the proof to keep the results
self-contained.
Theorem 1. A graph 𝐺 is the exclusivity graph of an 𝑛-context GHZ-type paradox iff.
2) = 𝑛, where 𝐺
2 is the graph complement of 𝐺.
𝛼(𝐺) = 𝑛 − 1, 𝜗(𝐺) = 𝑛, and 𝜒( 𝐺
𝛼(𝐺), 𝜗(𝐺), and 𝜒(𝐺) are 𝐺’s independence number, Lovász number, and chromatic number, respectively.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 23 of 65

## PDF page 24

Fig. 5: Numeric settings. (a) An orthogonal representation of the Perkel graph obtained
from Lovász semidefinite programming and Cholesky decomposition. (b) The Gram matrix
of the orthogonal representation of the Perkel graph. The values of the diagonal (red-ish),
the yellow-ish and the white entries are 1, 1/3, and 0, respectively.

Proof.
Necessity—The first two equations can be justified by adding all the conditional probabilities in Eq. (LABEL:eq:ghz-general) together, comparing the sum with Eq. (1) and noticing that
the second term vanishes for ideal exclusivity. To prove the last equation, we observe that
𝐺
2 can be colored by assigning the same color to all vertices that represent the events in
the same context and using a different color for each context. This explicit construction
2) ⩽ 𝑛. But according to Lovász’s sandwich theorem [68], 𝜒( 𝐺
2) ⩾ 𝜗(𝐺) = 𝑛,
guarantees 𝜒( 𝐺
2) = 𝑛.
so it must be 𝜒( 𝐺

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 24 of 65

## PDF page 25

Sufficiency—The classical bound can be trivially proved using the original graph-theoretic
approach to contextuality [28]. To prove the quantum part that the event probabilities can
be disassembled into groups of unit probabilities given the graph constants, we notice that
the Lovász number of a graph 𝐺 is the optimum of the objective function in the following
semidefinite program (“Lovász optimization”):
max 𝜗 = tr(𝐁𝐉)
𝐁

(8)

subject to 𝐁 ≽ 0, tr(𝐁) = 1,

𝐵𝑖𝑗 = 0, ∀ (𝑖, 𝑗) ∈ 𝐸(𝐺),

where 𝐉 is an 𝑁 × 𝑁 matrix with all of its entries being 1, (⋅) ≽ 0 means the matrix on the
left-hand side of the operator is positive semidefinite, and 𝐸(𝐺) is the edge set of 𝐺. Let the
matrix 𝐁 be the Gram matrix of the set of rays 𝒓𝑘 , 𝑘 ∈ [1, 𝑁] and denote 𝐺′ as the exclusivity
graph of |𝒓𝑘 ⟩⟨𝒓𝑘 |. As the last constraint in Eq. (S4) guarantees ⟨𝒓𝑖 |𝒓𝑗 ⟩ = 0, ∀ (𝑖, 𝑗) ∈ 𝐸(𝐺), it
2), therefore, a 𝜒( 𝐺
2)-coloring for 𝐺
2 is also a
must be 𝐸(𝐺) ⊆ 𝐸(𝐺′ ) and thus 𝐸(2
𝐺′ ) ⊆ 𝐸( 𝐺
2) → [𝑗, 𝑘], where 𝑗 indicates the
proper coloring for 2
𝐺′ . We denote such a coloring as 𝑉( 𝐺
color and 𝑘 ∈ [1, 𝑚𝑗 ] is the index of the vertex among those 𝑚𝑗 -vertices with the same col-

2 must correspond to mutually exclusive
or. Now, the vertices with the same color in 𝐺
𝑚𝑗
′
events in 𝐺 . Due to the exclusivity principle [69], we have ∑ 𝑘 =
Pr(1 | [𝑗, 𝑘]) ⩽ 1, ∀ 𝑗, but
1

𝑗
2).
from the definition of the Lovász number we also have ∑ 𝑗 = 1 ∑ 𝑘 =
Pr(1 | [𝑗, 𝑘]) = 𝜒( 𝐺
1

𝜒( 𝐺
2)

𝑚

𝑗
Therefore, it must be ∑ 𝑘 =
Pr(1 | [𝑗, 𝑘]) = 1 for all 𝑗. The GHZ-type paradox in Eq. (LA1

𝑚

BEL:eq:ghz-general) is thus recovered. ∎

Theorem 2. The lower bound of the number of context-cover in a GHZ-type paradox is
three. There exists no GHZ-type paradox using one or two context-cover.

Proof.

By Theorem 1, the underlying graph 𝐺 of exclusivity corresponding to an 𝑛-context GHZtype contextuality has an independence number of 𝛼(𝐺) = 𝑛 − 1. An 𝑛 = 1 paradox would

require 𝛼(𝐺) = 0 which is a null graph: |𝑉(𝐺)| = 0, where the measurement events are undefined. An 𝑛 = 2 paradox would require 𝛼(𝐺) = 1 which is a complete graph, but a complete

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 25 of 65

## PDF page 26

graph also has a Lovász number of 𝜗(𝐺) = 1 = 𝛼(𝐺), and thus its corresponding noncontextuality inequality cannot have any quantum violation. ∎

Theorem 3. No strongly regular graph hosts a three-context GHZ-type paradox.

Proof.
We sketch the proof in this section and defer the complete proof to the Supplementary Material. A strongly regular graph with four parameters 𝑛, 𝑘, 𝑎 and 𝑐, denoted by
SRG(𝑛, 𝑘, 𝑎, 𝑐), is a 𝑛-vertex 𝑘-regular graph such that every two adjacent vertices have 𝑎
common neighbors, and that every two non-adjacent vertices have 𝑐 common neighbors.
By Theorem 1, we only need to prove the nonexistence of a strongly regular graph 𝐺 with a
clique number of two and a chromatic number of three such that the Lovász number of its
complement graph is also three.

The proof is by exhaustion. As the exclusivity graph for a three-context GHZ-type paradox
is triangle-free, we have 𝑎 = 0. Starting from this observation, we can study the spectrum
of the adjacency matrix of 𝐺, and find its only three nonzero eigenvalues are 𝑘 and

𝑐2 + 4(𝑘 − 𝑐) − 𝑐)/2. Using the Hoffman–Delsarte eigenvalue bound [70, 71], we link
√
the eigenvalues to the known graph constants to have 𝑐 ⩽ 𝑘 ⩽ 2𝑐 + 3; the condition can be
further narrowed to 𝑘 ∈ {𝑐, 2𝑐 + 1} by looking at the multiplicities of the eigenvalues. Finally,
for both of the cases, we show that the resulted graph cannot satisfy the desired graph(±

constant constraints. ∎

Theorem 4. If there exists a Kochen–Specker set consisting of only four complete contexts,
then those contexts are all disjoint.

Proof.

The proof is by contradiction. Let the four complete contexts be {𝐶𝑖 }𝑖 = 1 . Without loss of
4

generality, we can assume 𝐶1 ∩ 𝐶2 ≠ ∅ and 𝑣0 ∈ 𝐶1 ∩ 𝐶2 . According to the relation between

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 26 of 65

## PDF page 27

GHZ-type proof and Kochen–Specker set [24], we can obtain the exclusivity graph 𝐺 of a
GHZ-type proof by removing 𝑣0 and other vertices connected to 𝑣0 , especially all other vertices in 𝐶1 and 𝐶2 . Consequently, this exclusivity graph 𝐺 can be covered by two cliques,
which implies that 𝜗(𝐺) ≤ 2. Since it stands for a GHZ-type proof, 𝛼(𝐺) should be strictly
less than 𝜗(𝐺), thus the only possibility is that 𝛼(𝐺) = 1. This can only happen in the case
that the graph can be covered by one clique, where 𝜗(𝐺) = 𝛼(𝐺) = 1. This contradicts the
assumption that 𝐺 is the exclusivity graph of a GHZ-type proof. ∎
Number of context and context-cover. In calculating the number of contexts in a GHZtype paradox, two definitions are possible. The number of context is the number of all orthonormal basis that must be used to derive the deterministic contradiction between the
noncontextual and quantum theory [67, 25]. Here, we define the number of context-cover
as the number of contexts required to include all the elementary events in a GHZ-type
paradox. As we have discussed before, the number of context-cover determines the quantum-classical ratio.

In the graph-theoretic approach, the number of context and context-cover and are naturally linked to the graph constants of the exclusivity graph, 𝐺, corresponding to the events in a
GHZ-type paradox. Note that 𝐸(𝐺) only includes the exclusivity relations that are necessary

for deriving the logical paradox and excludes the orthogonal relations that “accidentally”
appear at finding the numeric solution of the exclusivity graph. In Theorem 1, we have
2 or the verproved that the number of context-cover is the (vertex) chromatic number of 𝐺
tex clique cover number of 𝐺, denoted by 𝗏𝖼𝖼(𝐺). In the same vein, the number of context is
2 or the edge clique number of 𝐺, denoted by 𝖾𝖼𝖼(𝐺). As for
the edge chromatic number of 𝐺

any graph 𝖾𝖼𝖼(𝐺) ⩾ 𝗏𝖼𝖼(𝐺) holds, the number of context is at least not less than the number
of context-cover.

According to Vorob’ev’s theorem, a necessary condition for the existence of a quantum realization producing contextuality is that the graph of compatibility of the observables has
cycles of length more than 3 [72, 25]. Therefore, the minimal number of proof-context in a
GHZ-type paradox is at least four, which is saturated by e.g., GHZ and Mermin’s construction [15]. In our case, as the Perkel graph has an edge chromatic number of seven, the proof

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 27 of 65

## PDF page 28

of its corresponding GHZ-type paradox must use at least seven contexts.

Fig. 6: Detailed experimental setup. The blue lines denote optical fibers, and the red
strokes indicate light propagating in free-space sessions. Electronic connections are
denoted by gray lines. The beam-splitter ports marked with the same color have higher
transmissivity. Acronyms: AFG arbitrary function generator, IM intensity modulator, Osc.
oscilloscope, PM phase modulator, PZT piezoelectric fiber stretcher.

Experimental setup. The full experimental setup is shown in Fig. 6. A frequency-locked
pulsed fiber laser with a repetition rate of 1/𝜏 = 75.91 MHz, a central wavelength of 1560

nm, and a spectral bandwidth of 12 nm was adopted as the source of pulsed coherent
states. From the parameters of the laser, we estimate the maximal displacement of the co4
herent state as 𝛼
˜ = 1.014 × 10 , so the shot noise from the fluctuation of photon numbers
between individual pulses is comparatively small.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 28 of 65

## PDF page 29

The 37-dimensional state was encoded in six direct-sum subspaces and implemented in
different runs of the experiment; each of the subspaces was in turn represented by up to
seven pulsed coherent states. To implement both the preparation of the initial state and the
adjustment of the convolution basis, we utilized a commercial lithium niobate intensity
modulator (Thorlabs LN81S-FC) with a power extinction ratio of 28 dB. The intensity modulator only generated preparation and measurement basis with real coefficients, but it can
be easily upgraded to realize complex coefficients by employing an additional phase modulator. The intensity modulator was driven by an arbitrary function generator which has a
rising and falling edge time measured as 7 ns. Due to the limited bandwidth of the function
generator, we could not address the individual pulses from the laser. Instead, we always
modulated three consecutive pulses and only measured the amplitude of the middle one to
avoid clashing with the modulation edges; this resulted in an effective pulse frequency of
1/Δ𝑡 = 1/(3𝜏).
To construct the fiber ring for convolution, we utilized two fiber beamsplitters with an amplitude splitting ratio of 90:10 and a free-space delay line. The length of the entire delay line

was carefully adjusted to 3𝜏 to align the pulses at different times and maximize the visibility
of the interference. We manually calibrated the kernel of convolution instead of using the
round-trip loss of the fiber ring cavity (estimated to be 27%) as the pulses emitted from the
ring after different numbers of circulation would have different spectral distribution and
interference visibility with the local oscillator. The homodyne detector used in our experiment (Thorlabs PDB480C-AC) had a linear response to power difference up to 5 𝜇W as
shown in Fig. 7, and all experimental points fell well in the linear regime.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 29 of 65

## PDF page 30

Fig. 7: Detector response curve. Data points: homodyne detector (HD)’s voltage response
to the power difference between two input ports. Curve: linear fit of those data points with
power differences below 5 𝜇W; the 1 dB gain compression point is at 6.63 𝜇W. Histogram:
distribution of the power differences of the data points registered during the experiment;
the maximal power difference was 3.05 𝜇W and all data points fell in the linear response
range.

Phase stabilization. The experimental setup contained two interference points that needed to be phase stabilized. The first is the convolution ring which is a fiber cavity and we
adopted the Pound–Drever–Hall technique [73] to stabilize its length. Concretely, A 3.2 kHz
sine-wave modulation signal is sent from the servo to a piezoelectric crystal attached to a
mirror in the free-space delay line. The voltage would dither the convolution phase by ±3 ∘
maximum. As shown in Fig. 2, we monitored the optical power at one port of the input coupler of the convolution ring. Essentially, this is the “reflection” from the fiber cavity and it

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 30 of 65

## PDF page 31

will be minimized when the convolution phase is an integer multiply of 2𝜋. By demodulating
the monitor signal, the servo would be able to find out the direction of the phase drift, and
then send a voltage to the piezo to correct the drift and establish the phase lock.

The second phase lock is required to align the phase of the local oscillator with the rest of
the setup. With our lock–measure cycle, this can be ensured by maximizing the power difference at the local oscillator during the lock stage. To this purpose, a dither signal would
again be needed to reveal the direction of the phase drift. We sent the 7.2 kHz sine-wave
modulation to a fiber stretcher (Optiphase PZ2) in the local oscillator path. The choice of
the frequency was to both accommodate the intrinsic frequency response of the fiber
stretcher and avoid the high-order harmonic from the upstream lock’s dithering. After demodulating and low-pass filtering the signal from the monitor port of the homodyne detector, the resulted error signal would be proportional to the quadrature amplitude (i.e., outof-phase part to the local oscillator) of the setup, and the servo can drive the fiber stretcher
accordingly to stabilize the phase of the local oscillator.

Phase error readout. As elaborated in the main text, both the convolution and the homodyne phase will remain almost constant during the entire measure period; we denote them
as 𝜑 and 𝜙, respectively. To extract the phase errors, we also need to know the entire kernel
of convolution {𝑐1 , 𝑐2 , …, 𝑐𝑘 , …}. We pre-calibrated up to 12 terms before the experiment and
found the effect of the other terms was sufficiently small. During the locking stage, the
readout value of the homodyne detector can be expressed as:
ℎ0 = 𝛼
˜Re(e−𝑖𝜙 ∑ 𝑘 = 1 𝑐𝑘 e𝑖𝑘𝜑 ).

(9)

The phase error readout procedure worked as follows. Firstly, from the state of the lock
stage, we added a 𝜋/2-phase to the local oscillator through the phase modulator. When the
modulated pulse arrived at the homodyne detector (first green band in Fig. 3(a)), the homodyne value became:

ℎ1 = 𝛼
˜Re(e−𝑖𝜙 + 𝜋/2 ∑ 𝑘 = 1 𝑐𝑘 e𝑖𝑘𝜑 ).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

(10)

2/5/25, 4 47 PM
Page 31 of 65

## PDF page 32

Secondly, we kept the state of the phase modulator and shut off the intensity modulator.
This caused no light to enter the fiber cavity and the existing pulses started to leak out of
the convolution ring. After three round-trip time (second green band in Fig. 3(a)), the homodyne value became:

ℎ2 = 𝛼
˜Re(e−𝑖𝜙 + 𝜋/2 ∑ 𝑘 = 4 𝑐𝑘 e𝑖𝑘𝜑 ).

Comparing the values of ℎ0 , ℎ1 , and ℎ2 gives the desired phase errors 𝜑 and 𝜙.

(11)

Correcting for non-ideal exclusivity. To measure the correlator terms in Eq. 1 and arrive
at Eq. 7, we notice that the term 𝑃(1, 1 | 𝑖, 𝑗) as the probability of the measurement outcome
on the first projector 𝑖 is +1, and then the measurement outcome of the post-measurement
state, which is the +1-eigenstate of the projector 𝑖, on the second projector 𝑗 is again +1.
Experimentally, we prepare the +1-eigenstate of the projector 𝑖, and measure it with the
other projectors that are supposed to be orthogonal to it. Define the probability of finding
the +1-eigenstate of the 𝑖-th projector on the +1-eigenstate of the 𝑗-th projector to be
𝑃(1 | 𝑗, 𝑖 = 1), we have:
𝑃(1, 1 | 𝑖, 𝑗) = 𝑃(1 | 𝑖)𝑃(1 | 𝑗, 𝑖 = 1).

(12)

By iterating the procedure over all the possible combinations (𝑖, 𝑗) ∈ 𝐸(𝐺), we obtained all
the probabilities 𝑃(1 | 𝑗, 𝑖 = 1) as shown in Fig. 4(a). The probabilities 𝑃(1 | 𝑗, 𝑖 = 1) have already been recorded in the observation of the GHZ-type paradox. From these probabilities,
we can calculate the desired correction due to the non-ideal exclusivity.

Error analysis. We identify four main sources of the experimental error. The first was the
dither for the phase lock. To lock at the top of an interference fringe generally necessitates
a dither signal and demodulation, but the dither also disturbs the lock itself. In our experiment, the inferred level of phase noise was very close to the dither signal, and we could not
further weaken the dither and still have a stable lock. This could be fixed by only sending
the dither signal during the lock stage and freezing the output of the servo; such an operation, although cannot be incorporated in our current setup, has native support in some
software [74] that implements versatile field-programmable gate array-based phase locks.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 32 of 65

## PDF page 33

The second was the imperfection of the intensity modulator, which has both a limited extinction ratio and a drift of zero-output voltage due to the heating of the element. We
strived to eliminate the drift by sending the pulses used in the experiment for one hour before data registration so the element was sufficiently “thermalized” with the environment.
This could be further improved by cascading more intensity modulators to increase the extinction ratio and introducing a feedback control loop to auto-correct the zero-output voltage.

The third was the imperfect interference visibility. The laser used in the experiment was a
femtosecond pulsed laser and the pulses were very localized in space. After the spectral
filtering, we could only observe an interference when the distance of the two pulses was
below 0.4 cm. This made the adjustment of the fiber ring’s length challenging. Moreover,
the chromatic dispersion in the fiber ring system causes the pulses traveled different times
inside the ring to have different spectra. As such, even when a specific preparation and
measurement setting should result in perfect destructive interference, the output from the
fiber ring could not be eliminated and would be seen by the homodyne detector. We consider this effect as the culprit for the imperfect exclusivity in Fig. 4(a).

Finally, that we cannot fully exploit the 10-bit readout precision of the oscilloscope also limited the precision of the experiment. Due to the phase error readout scheme, the entire oscilloscope trace must not go out of range during the lock period (otherwise ℎ0 in Eq. (9) can-

not be measured). This prevented us from selecting a smaller voltage scale and achieving
better readout resolution. In the future, it would be helpful to put the phase error estimation subroutine to the servo and use the full precision of the oscilloscope to register the
data.

Acknowledgements.—We would like to thank Adán Cabello, Jonatan B. Brask, Daniel Cavalcanti and Jonas S. Neergaard-Nielsen for inspiring discussion and Lucas Nunes Faria for
helpful feedback on an earlier version of the paper.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 33 of 65

## PDF page 34

References
Einstein et al. [1935]

A. Einstein,
B. Podolsky, and N. Rosen, Can quantummechanical description of physical reality
be considered complete?, Phys.
Rev. 47, 777 (1935).

Wigner [1961]

E. P. Wigner, in The Scientist Speculates

Kochen and Specker [1967]

S. Kochen and E. P. Specker, The problem

Heisenberg [1927]

W. Heisenberg, Über den anschaulichen

[5]

Throughout this paper, we omit the

Abbott et al. [2012]

A. A. Abbott, C. S. Calude,
J. Conder, and K. Svozil, Strong Kochen–
Specker theorem and incomputability of

(ed. Good, I.
J.) (Heinemann, 1961) pp. 284–302.
of hidden variables in quantum
mechanics, J. Math. Mech. 17, 59 (1967).
inhalt der quantentheoretischen
kinematik und mechanik, Z.
Physik 43, 172 (1927).
qualifier “Kochen–Specker” or “quantum”
before “contextuality” for the sake of
brevity.

quantum randomness, Phys. Rev.
A 86, 062109 (2012).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 34 of 65

## PDF page 35

Um et al. [2020]

M. Um, Q. Zhao, J. Zhang, P. Wang,
Y. Wang, M. Qiao, H. Zhou,
X. Ma, and K. Kim, Randomness
expansion secured by quantum
contextuality, Phys. Rev.
Applied 13, 034077 (2020).

Gühne et al. [2014]

O. Gühne, C. Budroni, A. Cabello,
M. Kleinmann, and J.-Å. Larsson, Bounding
the quantum dimension with
contextuality, Phys. Rev. A 89, 062107
(2014).

Ray et al. [2021]

M. Ray, N. G. Boddu, K. Bharti, L.-

Bharti et al. [2019]

K. Bharti, M. Ray, A. Varvitsiotis,
N. A. Warsi, A. Cabello, and L.C. Kwek, Robust self-testing of quantum

C. Kwek, and A. Cabello, Graph-theoretic
approach to dimension witnessing, New J.
Phys. 23, 033006 (2021).

systems via noncontextuality
inequalities, Phys. Rev. Lett. 122, 250403
(2019).
Hu et al. [2023]

X.-M. Hu, Y. Xie, A. S. Arora, M.-Z. Ai,
K. Bharti, J. Zhang, W. Wu, P.-X. Chen, J.M. Cui, B.-H. Liu, et al., Self-testing of a
single quantum system from theory to
experiment, npj Quant. Inf. 9, 103 (2023).

Clifton [1993]

R. Clifton, Getting contextual and
nonlocal elements-of-reality the easy
way, Am. J. Phys. 61, 443 (1993).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 35 of 65

## PDF page 36

Cabello [2021a]

A. Cabello, Bell non-locality and Kochen–
Specker contextuality: How are they
connected?, Found. Phys. 51, 61 (2021a).

Greenberger et al. [1989]

D. M. Greenberger,
M. A. Horne, and A. Zeilinger, in Bell’s
theorem, quantum theory and
conceptions of the
universe (Springer, 1989) pp. 69–72.

Mermin [1990]

N. D. Mermin, Simple unified form for the
major no-hidden-variables
theorems, Phys. Rev. Lett. 65, 3373
(1990).

Abramsky and Brandenburger [2011]

S. Abramsky and A. Brandenburger, The
sheaf-theoretic structure of non-locality
and contextuality, New J. Phys. 13, 113036
(2011).

Anders and Browne [2009]

J. Anders and D. E. Browne, Computational
power of correlations, Phys. Rev.
Lett. 102, 050502 (2009).

Raussendorf [2013]

R. Raussendorf, Contextuality in
measurement-based quantum
computation, Phys. Rev. A 88, 022322
(2013).

Abramsky et al. [2017]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

S. Abramsky, R. S. Barbosa,
G. Carù, and S. Perdrix, A complete
characterization of all-versus-nothing
arguments for stabilizer states, Philos.
Trans. R. Soc. A 375, 20160385 (2017).

2/5/25, 4 47 PM
Page 36 of 65

## PDF page 37

Howard et al. [2014]

M. Howard, J. Wallman,
V. Veitch, and J. Emerson, Contextuality
supplies the ‘magic’ for quantum
computation, Nature 510, 351 (2014).

Bravyi et al. [2018]

S. Bravyi,

Bravyi et al. [2020]

S. Bravyi, D. Gosset,
R. Koenig, and M. Tomamichel, Quantum
advantage with noisy shallow
circuits, Nat. Phys. 16, 1040 (2020).

Cabello et al. [1996]

A. Cabello, J. Estebaranz, and G. GarcíaAlcaine, Bell–Kochen–Specker theorem:
A proof with 18 vectors, Phys. Lett.

D. Gosset, and R. König, Quantum
advantage with shallow
circuits, Science 362, 308 (2018).

A 212, 183 (1996).
Xu et al. [2020]

Z.-P. Xu, J.-L. Chen, and O. Gühne, Proof
of the Peres conjecture for
contextuality, Phys. Rev.
Lett. 124, 230401 (2020).

Budroni et al. [2022]

C. Budroni, A. Cabello, O. Gühne,

Miller and Shi [2017]

C. A. Miller and Y. Shi, Universal security
for randomness expansion from the
spot-checking protocol, SIAM J.
Comput. 46, 1304 (2017).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

M. Kleinmann, and J.-Å. Larsson, Quantum
contextuality, Rev. Mod.
Phys. 94, 045007 (2022).

2/5/25, 4 47 PM
Page 37 of 65

## PDF page 38

Zhen et al. [2023]

Y.-Z. Zhen, Y. Mao, Y.-Z. Zhang,
F. Xu, and B. C. Sanders, Deviceindependent quantum key distribution
based on the Mermin-Peres magic
square game, Phys. Rev.
Lett. 131, 080801 (2023).

Cabello et al. [2014]

A. Cabello,
S. Severini, and A. Winter, Graphtheoretic approach to quantum
correlations, Phys. Rev. Lett. 112, 040401
(2014).

Barnett [2022]

S. M. Barnett, On single-photon and

Cabello [2016]

A. Cabello, Simple method for

McMahon et al. [2016]

P. L. McMahon, A. Marandi, Y. Haribara,
R. Hamerly, C. Langrock, S. Tamate,
T. Inagaki, H. Takesue, S. Utsunomiya,

classical interference, Phys.
Scr. 97, 114004 (2022).
experimentally testing any form of
quantum contextuality, Phys. Rev.
A 93, 032102 (2016).

K. Aihara, et al., A fully programmable
100-spin coherent Ising machine with allto-all connections, Science 354, 614
(2016).
Inagaki et al. [2016]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 38 of 65

## PDF page 39

T. Inagaki, Y. Haribara, K. Igarashi,
T. Sonobe, S. Tamate, T. Honjo,
A. Marandi, P. L. McMahon, T. Umeki,
K. Enbutsu, et al., A coherent Ising
machine for 2000-node optimization
problems, Science 354, 603 (2016).
Honjo et al. [2021]

T. Honjo, T. Sonobe, K. Inaba, T. Inagaki,
T. Ikuta, Y. Yamada, T. Kazama,
K. Enbutsu, T. Umeki, R. Kasahara,
et al., 100,000-spin coherent Ising
machine, Sci. Adv. 7, eabh0952 (2021).

Asavanant et al. [2019]

W. Asavanant, Y. Shiozawa, S. Yokoyama,
B. Charoensombutamon, H. Emura,
R. N. Alexander, S. Takeda, J.-i. Yoshikawa,
N. C. Menicucci, H. Yonezawa,
et al., Generation of time-domainmultiplexed two-dimensional cluster
state, Science 366, 373 (2019).

Larsen et al. [2019]

M. V. Larsen, X. Guo, C. R. Breum,

Larsen et al. [2021]

M. V. Larsen, X. Guo, C. R. Breum,
J. S. NeergaardNielsen, and U. L. Andersen, Deterministic

J. S. NeergaardNielsen, and U. L. Andersen, Deterministic
generation of a two-dimensional cluster
state, Science 366, 369 (2019).

multi-mode gates on a scalable photonic
quantum computing platform, Nat.
Phys. 17, 1018 (2021).
Ren et al. [2024]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 39 of 65

## PDF page 40

S. Ren, D. Han,
M. Wang, and X. Su, Continuous variable
quantum teleportation and remote state
preparation between two spaceseparated local networks, Sci. China Inf.
Sci. 67, 142502 (2024).
L. S. Madsen, F. Laudenbach,

Madsen et al. [2022]

M. F. Askarani, F. Rortais, T. Vincent,
J. F. Bulmer, F. M. Miatto, L. Neuhaus,
L. G. Helt, M. J. Collins, et al., Quantum
computational advantage with a
programmable photonic
processor, Nature 606, 75 (2022).

Sempere-Llagostera et al. [2022]

S. Sempere-Llagostera, R. B. Patel,

I. A. Walmsley, and W. S. Kolthammer, Experimentall
finding dense subgraphs using a time-bin
encoded gaussian boson sampling
device, Phys. Rev. X 12, 031045 (2022).

He et al. [2017]

Y. He, X. Ding, Z.-E. Su, H.-L. Huang,
J. Qin, C. Wang, S. Unsleber, C. Chen,
H. Wang, Y.-M. He, X.-L. Wang, W.J. Zhang, S.-J. Chen, C. Schneider,
M. Kamp, L.-X. You, Z. Wang, S. Höfling,
C.-Y. Lu, and J.-W. Pan, Time-bin-encoded
boson sampling with a single-photon
device, Phys. Rev. Lett. 118, 190501
(2017).

Lovász [1979]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 40 of 65

## PDF page 41

L. Lovász, On the Shannon capacity of a
graph, IEEE Trans. Inf. Theory 25, 1
(1979).
Cabello et al. [2015]

A. Cabello,
M. Kleinmann, and C. Budroni, Necessary
and sufficient condition for quantum
state-independent contextuality, Phys.
Rev. Lett. 114, 250402 (2015).
L. Lovász,
M. Saks, and A. Schrijver, Orthogonal

Lovász et al. [1989]

Acín et al. [2017]

representations and connectivity of
graphs, Linear Algebra Its Appl. 114, 439
(1989).

A. Acín, R. Duan, D. E. Roberson,
A. B. Sainz, and A. Winter, A new property
of the Lovász number and duality
relations between graph
parameters, Discrete Appl.
Math. 216, 489 (2017).

Amselem et al. [2012]

E. Amselem, L. E. Danielsen, A. J. LópezTarrida, J. R. Portillo,
M. Bourennane, and A. Cabello, Experimental
fully contextual correlations, Phys. Rev.
Lett. 108, 200405 (2012).

Klyachko et al. [2008]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 41 of 65

## PDF page 42

A. A. Klyachko, M. A. Can,
S. Binicioğlu, and A. S. Shumovsky, Simple
test for hidden variables in spin-1
systems, Phys. Rev. Lett. 101, 020403
(2008).
Cabello et al. [2013]

A. Cabello, P. Badziag,
M. T. Cunha, and M. Bourennane, Simple
Hardy-like proof of quantum
contextuality, Phys. Rev. Lett. 111, 180404
(2013).

Marques et al. [2014]

B. Marques, J. Ahrens, M. Nawareg,
A. Cabello, and M. Bourennane, Experimental
observation of Hardy-like quantum
contextuality, Phys. Rev.
Lett. 113, 250403 (2014).

Jerger et al. [2016]

M. Jerger, Y. Reshitnyk, M. Oppliger,
A. Potočnik, M. Mondal, A. Wallraff,
K. Goodenough, S. Wehner, K. Juliusson,
N. K. Langford, et al., Contextuality
without nonlocality in a superconducting
quantum system, Nat. Commun. 7, 12930
(2016).

Mermin [1993]

N. D. Mermin, Hidden variables and the
two theorems of John Bell, Rev. Mod.
Phys. 65, 803 (1993).

Perkel [1979]

M. Perkel, Bounding the valency of
polygonal graphs with odd girth, Can. J.
Math. 31, 1307 (1979).

Bose [1963]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 42 of 65

## PDF page 43

R. C. Bose, Strongly regular graphs,
partial geometries and partially balanced
designs., Pac. J. Math. 13, 389 (1963).
Chi et al. [2023]

Y. Chi, Y. Yu, Q. Gong, and J. Wang, Highdimensional quantum information
processing on programmable integrated
photonic chips, Sci. China Inf.
Sci. 66, 180501 (2023).

Qiao et al. [2024]

M. Qiao, Z. Cai, Y. Wang, B. Du, N. Jin,
W. Chen, P. Wang, C. Luan, E. Gao, X. Sun,
H. Tian, J. Zhang, and K. Kim, Tunable
quantum simulation of spin models with
a two-dimensional ion crystal, Nat.
Phys. 20, 623 (2024).
Z. Bao, S. Xu, Z. Song, K. Wang, L. Xiang,
Z. Zhu, J. Chen, F. Jin, X. Zhu, Y. Gao,
Y. Wu, C. Zhang, N. Wang, Y. Zou, Z. Tan,

Bao et al. [2024]

A. Zhang, Z. Cui, F. Shen, J. Zhong, T. Li,
J. Deng, X. Zhang, H. Dong, P. Zhang, Y.R. Liu, L. Zhao, J. Hao, H. Li, Z. Wang,
C. Song, Q. Guo,
B. Huang, and H. Wang, Creating and
controlling global greenberger-hornezeilinger entanglement on quantum
processors, Nat. Commun. 15, 8823
(2024).

Liu et al. [2023]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 43 of 65

## PDF page 44

Z.-H. Liu, H.-X. Meng, Z.-P. Xu, J. Zhou, J.L. Chen, J.-S. Xu, C.-F. Li, G.C. Guo, and A. Cabello, Experimental test
of high-dimensional quantum
contextuality based on contextuality
concentration, Phys. Rev.
Lett. 130, 240202 (2023).
Yuan et al. [2018]

L. Yuan, Q. Lin,
M. Xiao, and S. Fan, Synthetic dimension
in photonics, Optica 5, 1396 (2018).

Weidemann et al. [2020]

S. Weidemann, M. Kremer, T. Helbig,
T. Hofmann, A. Stegmaier, M. Greiter,
R. Thomale, and A. Szameit, Topological
funneling of light, Science 368, 311
(2020).
C. Leefmans, A. Dutt, J. Williams, L. Yuan,
M. Parto, F. Nori,
S. Fan, and A. Marandi, Topological
dissipation in a time-multiplexed
photonic resonator network, Nat.

Leefmans et al. [2022]

Phys. 18, 442 (2022).

Yokoyama et al. [2013]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 44 of 65

## PDF page 45

S. Yokoyama, R. Ukai, S. C. Armstrong,
C. Sornphiphatphong, T. Kaji, S. Suzuki, J.i. Yoshikawa, H. Yonezawa,
N. C. Menicucci, and A. Furusawa, Ultralarge-scale continuous-variable cluster
states multiplexed in the time
domain, Nat. Photon. 7, 982 (2013).
Sakaguchi et al. [2023]

A. Sakaguchi, S. Konno, F. Hanamura,
W. Asavanant, K. Takase, H. Ogawa,
P. Marek, R. Filip, J.-i. Yoshikawa,
E. Huntington,
H. Yonezawa, and A. Furusawa, Nonlinear
feedforward enabling quantum
computation, Nat. Commun. 14, 3817
(2023).

Hamilton et al. [2017]

C. S. Hamilton, R. Kruse, L. Sansoni,
S. Barkhofen,
C. Silberhorn, and I. Jex, Gaussian boson
sampling, Phys. Rev. Lett. 119, 170501
(2017).

Motes et al. [2014]

K. R. Motes, A. Gilchrist,
J. P. Dowling, and P. P. Rohde, Scalable
boson sampling with time-bin encoding
using a loop-based architecture, Phys.
Rev. Lett. 113, 120501 (2014).

Yu et al. [2023]

S. Yu, Z.-P. Zhong, Y. Fang, R. B. Patel, Q.P. Li, W. Liu, Z. Li, L. Xu, S. SagonaStophel, E. Mer, et al., A universal
programmable gaussian boson sampler
for drug discovery, Nat. Comput.
Sci. 3, 839 (2023).

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 45 of 65

## PDF page 46

Yonezu et al. [2023]

K. Yonezu, Y. Enomoto,
T. Yoshida, and S. Takeda, Time-domain
universal linear-optical operations for
universal quantum information
processing, Phys. Rev. Lett. 131, 040601
(2023).

Cabello [2021b]

A. Cabello, Converting contextuality into

Lisoněk et al. [2014]

P. Lisoněk, P. Badziag,

Grötschel et al. [1981]

M. Grötschel,
L. Lovász, and A. Schrijver, The ellipsoid
method and its consequences in
combinatorial

nonlocality, Phys. Rev. Lett. 127, 070401
(2021b).
J. R. Portillo, and A. Cabello, Kochen–
Specker set with seven contexts, Phys.
Rev. A 89, 042101 (2014).

optimization, Combinatorica 1, 169 (1981).
Cabello [2013]

A. Cabello, Simple explanation of the
quantum violation of a fundamental
inequality, Phys. Rev. Lett. 110, 060402
(2013).
D. M. Cvetković,

Cvetković et al. [1980]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

M. Doob, and H. Sachs, Spectra of
graphs (Academic Press Inc. [Harcourt
Brace Jovanovich Publishers], New
York, 1980) p. 115.

2/5/25, 4 47 PM
Page 46 of 65

## PDF page 47

Delsarte [1973]

P. Delsarte, An algebraic approach to the
association schemes of coding
theory, Philips Res. Rep. Suppl. 10, vi+
(1973).

Xu and Cabello [2019]

Z.-P. Xu and A. Cabello, Necessary and
sufficient condition for contextuality from
incompatibility, Phys. Rev. A 99, 020103
(2019).

Black [2001]

E. D. Black, An introduction to Pound–
Drever–Hall laser frequency
stabilization, Am. J. Phys. 69, 79 (2001).

Neuhaus et al. [2023]

L. Neuhaus, M. Croquette, R. Metzdorff,
S. Chua, P.-E. Jacquet, A. Journeaux,
A. Heidmann, T. Briant, T. Jacqmin, P.F. Cohadon, et al., FPGA-based feedback
control of quantum optics experiments
with the open source software package
PyRPL (2023), arXiv:2310.00086 .

Gottesman [1998]

D. Gottesman, arXiv:9807006 [quant-ph]
(1998).

Braunstein and Van Loock [2005]

S. L. Braunstein and P. Van Loock, Quantum
information with continuous
variables, Rev. Mod. Phys. 77, 513 (2005).

Delfosse et al. [2017]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

N. Delfosse, C. Okay, J. Bermejo-Vega,
D. E. Browne, and R. Raussendorf, Equivalence
between contextuality and negativity of
the Wigner function for qudits, New J.
Phys. 19, 123024 (2017).

2/5/25, 4 47 PM
Page 47 of 65

## PDF page 48

Booth et al. [2022]

R. I. Booth, U. Chabaud, and P.E. Emeriau, Contextuality and Wigner
negativity are equivalent for continuousvariable quantum measurements, Phys.
Rev. Lett. 129, 230401 (2022).

Kleinmann et al. [2011]

M. Kleinmann, O. Guehne, J. R. Portillo,
J.-Å. Larsson, and A. Cabello, Memory
cost of quantum contextuality, New J.
Phys. 13, 113011 (2011).

Hindlycke and Larsson [2022]

C. Hindlycke and J.-Å. Larsson, Efficient

Yu et al. [2022]

X.-D. Yu, T. Simnacher,
H. C. Nguyen, and O. Gühne, Quantuminspired hierarchy for rank-constrained
optimization, PRX Quantum 3, 010340

contextual ontological model of n-qubit
stabilizer quantum mechanics, Phys. Rev.
Lett. 129, 130401 (2022).

(2022).
Canas et al. [2014]

G. Canas, M. Arias, S. Etcheverry,
E. S. Gómez, A. Cabello,
G. B. Xavier, and G. Lima, Applying the
simplest Kochen–Specker set for
quantum information processing, Phys.
Rev. Lett. 113, 090404 (2014).

Aguilar et al. [2018]

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 48 of 65

## PDF page 49

E. A. Aguilar, M. Farkas, D. Martínez,
M. Alvarado, J. Cariñe, G. B. Xavier,
J. F. Barra, G. Cañas,
M. Pawłowski, and G. Lima, Certifying an
irreducible 1024-dimensional photonic
state using refined dimension
witnesses, Phys. Rev. Lett. 120, 230503
(2018).
Higman [1964]

D. G. Higman, Finite permutation groups
of rank 3, Math. Z. 86, 145 (1964).

Delsarte [1972]

P. Delsarte, Weights of linear codes and
strongly regular normed spaces, Discrete
Math. 3, 47 (1972).

Delsarte [1898]

P. Delsarte, Sur le théorème de
tait, L’Intermédiaire des
Mathématiciens 5, 225 (1898).

Clebsch [1868]

A. Clebsch, Ueber die flächen vierter
ordnung, welche eine doppelcurve
zweiten grades besitzen., Journal für die
reine und angewandte
Mathematik 69, 142 (1868).

with a time-domain optical processor”
.1 GHZ-type paradoxes for quantum computing
It is known that the Clifford (Gaussian) subtheory in discrete- (continuous-)variable quantum theory is efficiently simulable with a classical computer [75, 76] and cannot provide
acceleration for quantum computing. Starting from this observation, contextuality has been

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 49 of 65

## PDF page 50

flagged as crucial for quantum computing through its link to negativity [77, 78]. On the
other hand, although it is also known that the simulation of contextual correlations is hard
(e.g., by requiring a quadratic cost of memory [79, 80]), how to derive practical acceleration
from contextual relation is a more subtle topic. In this regard, the Greenberg–Horne–
Zeilinger (GHZ)-type contextuality is a noteworthy resource. Here, we discuss how the “perfect correlations” in the GHZ-type contextuality enable the three different approaches to
quantum computing; for an extended review of the role of contextuality (not necessarily
GHZ-type) in quantum computing we would point the readers to the Section VIA of Reference [25].

• GHZ-type contextuality signifies maximal magic.—Howard et al. [20] identified contextuality as the necessary condition for a quantum state to be useful in the “magic state
distillation” subroutine. which enables universal quantum computation. In this paper,
the constructed noncontextuality inequality also comes from the graph-theoretic approach. Moreover, for an odd prime dimension 𝑝, the exclusivity graph 𝐺𝑝 satisfies

3
l)
2 means the graph complement of 𝐺.
𝛼(𝐺𝑝 ) = 𝑝3 , 𝜗(𝐺𝑝 ) = 𝜒( 𝐺
𝑝 = 𝑝 + 1, where 𝐺

From the Theorem 1 in the main text, we know that 𝐺𝑝 is the exclusivity graph of a

(𝑝3 + 1)-context GHZ-type contextuality: when a quantum state is the maximal resource state for magic state distillation, it will demonstrate a GHZ-type contextuality
using Howard et al.’s projector construction.

• GHZ-type contextuality promotes measurement-based quantum computation.—Using the
sheaf-theoretic approach to contextuality, Abramsky et al. [19] found that when one
uses an empirical model with a contextual fraction of 𝜆 for an 𝑙2-measurement-based
quantum computing task, the success probability of the task will be upper bounded by
𝜆. The contextual fraction of an empirical model is the infimum of the weight of the
contextual part when the model is decomposed into a noncontextual model and a contextual, no-signaling model. For a no-signaling model, the sum of the event probabilities is upper bounded by the fractional packing number 𝛼 ∗ (𝐺) of the exclusivity graph
𝐺 corresponding to the set of events. In the case of GHZ-type contextuality, the sum of
2) and as, from graph theory, we know that
the event probabilities is 𝜗(𝐺) = 𝜒( 𝐺
∗
2) ⩾ 𝛼 (𝐺), we are able to conclude that the empirical model in a GHZ-type con𝜒( 𝐺
textuality has a contextual fraction of 1. Therefore, the model will be an ideal resource

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 50 of 65

## PDF page 51

for measurement-based quantum computation. The application has been established
in some small-scale cases. For example, a tripartite GHZ-type correlation can enable
the deterministic computation of an nand gate [17]. Such a correlation can promote an
oracle only able to implement parity check to a universal computer and is thus of practical relevance.
• GHZ-type contextuality brings shallow-circuit quantum advantage.—The quantum advantage in shallow circuits refers to a type of computational problem, that is solvable by a
constant-depth quantum circuit with high certainty, whereas any classical circuit solving the problem with the same certainty must have a depth growing logarithmically
with the input size. Such a quantum advantage does not rely on the polynomial hierarchy in the computational complexity theory; it is known to exist [21] and can tolerate a
small amount of noise [22]. At the center of this kind of quantum advantage is the
GHZ-type contextuality: the quantum circuit can solve the problem due to its ability to
generate “perfectly” contextual correlations. The contextual correlation must be GHZtype in order to guarantee the output is deterministic regardless of the input size; a
Bell-type correlation that only statistically outperforms a local hidden-variable model
will fail to do so. This way, the GHZ-type contextual correlation levitated the memory
or communication cost in the classical circuit which finally converted into the penalty
in circuit depth. Also, the GHZ-type contextuality is necessary to bring the error rate of
the circuit below the fault-tolerance threshold and make the quantum advantage robust.
All the above examples unravel a strong link between GHZ-type contextuality and quantum
computing. Remarkably, at least two of these approaches (i.e., measurement-based quantum computing and quantum advantage in shallow circuits) require a GHZ-type contextuality beyond a Bell-type correlation. In this regard, the Theorem 1 in the main text capable of
identifying GHZ-type contextuality from the exclusivity graph of measurements paves a
step toward these applications. Also, the 37-dimensional GHZ-type contextuality has a
large quantum–classical ratio of 3/2 that exceeds all the known previous examples for a
single quantum system (see, for example, Figure S2 in the supplemental material of Reference [56] for a comparison). We envisage that a shallow quantum circuit can be constructed based on the contextuality identified here to implement a deterministic calculation of a
target function, with a success probability impossible to achieve using any multi-valued

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 51 of 65

## PDF page 52

classical circuit that has a fixed depth, and thus converting the large quantum–classical ratio to a strong quantum advantage.

.2 The original GHZ paradox in the probability form
ℳ1 = 𝜎𝑥 𝜎𝑦 𝜎𝑦 , ℳ2 = 𝜎𝑦 𝜎𝑥 𝜎𝑦 , ℳ3 = 𝜎𝑦 𝜎𝑦 𝜎𝑥 , and ℳ4 = 𝜎𝑥 𝜎𝑥 𝜎𝑥 . If the system is
Consider the following Pauli product measurements on a three-qubit system:
(1) (2) (3)

(1) (2) (3)

(1) (2) (3)

(1) (2) (3)

initiated at a state so the measurement outcome of ℳ1 , ℳ2 and ℳ3 are all +1, then a noncontextual theory will predict the measurement of ℳ4 on the system definitely returns +1,

because the assumption of noncontextuality means the outcome of measuring 𝜎𝑥 will not
(2) (3)
(2) (3)
depend on whether it is measured with 𝜎𝑥 𝜎𝑥 as in ℳ0 or 𝜎𝑦 𝜎𝑦 as in ℳ1 ; this is similar
(1)

(3)
for 𝜎(2)
𝑥 , 𝜎𝑥 . Taking into account the involutory of Pauli operators, the outcome of ℳ0 in

such theories will be the product of ℳ1 , ℳ2 and ℳ3 that is +1. However, quantum theory is
contextual: the only three-qubit state |𝜓⟩ giving ⟨ℳ1 ⟩𝜓 = ⟨ℳ2 ⟩𝜓 = ⟨ℳ3 ⟩𝜓 = +1 is the GHZ
state |𝜓⟩ = |GHZ⟩ = (|000⟩ − |111⟩)/ √2, which satisfies ⟨ℳ4 ⟩GHZ = −1.

Each of the four Pauli product measurements is composed of three local dichotomic measurements. If the outcomes of ℳ1 through ℳ4 are specified as in the above GHZ paradox,

then the local dichotomic measurements corresponding to each Pauli product measurement will have four possible combinations. For example, ℳ4 = −1 implies either
(2)
(3)
(1) (2)
𝜎(1)
𝑥 = 𝜎𝑥 = 𝜎𝑥 = −1, or that one and only one local measurement among 𝜎𝑥 , 𝜎𝑥 and
±(𝜈)
𝜎(3)
= (𝟙 ± 𝜎𝜈𝜇 )/𝟚, then the four elementary events can be ex𝑥 evaluates to −1. Let Π𝜇
pressed as:

−(1)
−(2)
−(3)
1 | [4, 1] : = 1 | Π𝑥 ⊗ Π𝑥 ⊗ Π𝑥 ,
−(1)
+(2)
+(3)
1 | [4, 2] : = 1 | Π𝑥 ⊗ Π𝑥 ⊗ Π𝑥 ,
−(2)
1 | [4, 3] : = 1 | Π𝑥+(1) ⊗ Π𝑥 ⊗ Π𝑥+(3) ,
− (3)
+(1)
+(2)
1 | [4, 4] : = 1 | Π𝑥 ⊗ Π𝑥 ⊗ Π𝑥 .

(S1)

In the same vein, we can define the elementary events 1 | [𝑗, 𝑘], 𝑗 ∈ {1, 2, 3}, 𝑘 ∈ [1, 4]. The
exclusivity graph for all these events, as discussed in the main text, is the graph complement of the Shrikhande graph, so the total number of events that are allowed to happen

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 52 of 65

## PDF page 53

according to any noncontextual model is no more than 3 for any initial state. That is, given
4
∑ 𝑘 = 1 Pr(1 | [𝑗, 𝑘]) = 1, 𝑗 ∈ {1, 2, 3} it must be
4

∑ Pr(1 | [4, 𝑘])

𝑘=1

NCHV
= 0.

(S2)

However, according to the calculated quantum expectations, the total probabilities of all
the four groups of events will saturate the upper bound allowed by the principle of exclusivity, that is,

Q
∑ Pr(1 | [𝑗, 𝑘]) = 1, j ∈ [1, 4].
4

𝑘=1

(S3)

This completes the transformation of the original GHZ paradox into the probability form as
in the Eq. (1) in the main text.

.3 Quantum realization of the exclusivity graph
Here we discuss how to obtain a detailed numeric setting for a set of rays that demonstrates the GHZ-type paradox from the exclusivity graph. Let 𝐺 be the exclusivity graph of
interest with |𝑉(𝐺)| = 𝑁, where 𝑉(𝐺) is the vertex set of 𝐺. The Gram matrix 𝐁 here is an
𝑁 × 𝑁 matrix associated with the orthogonal representation [43] of the graph complement
of 𝐺. Specifically, it can be calculated using semidefinite programming from the dual form
of the Lovász optimization:

max tr(𝐁𝐉)
𝐁

subject to 𝐁 ≽ 0

𝐵𝑖𝑗 = 0, ∀ (𝑖, 𝑗) ∈ 𝐸(𝐺)

tr(𝐁) = 1

(positive semidefiniteness)

(S4)

(orthogonality)

(normalisation).

Here, 𝐉 is an 𝑁 × 𝑁 matrix with all of its entries being 1, (⋅) ≽ 0 means the matrix on the lefthand side of the operator is positive semidefinite, and 𝐸(𝐺) is the edge set of 𝐺. The second
constraint is due to that when (𝑖, 𝑗) ∈ 𝐸(𝐺), the rank-1 projectors Π𝑖 = |𝑣𝑖 ⟩⟨𝑣𝑖 | and

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 53 of 65

## PDF page 54

Π𝑗 = |𝑣𝑗 ⟩⟨𝑣𝑗 | corresponding to the vertices 𝑖 and 𝑗 are exclusive: Π𝑖 Π𝑗 = 0, so the rays |𝑣𝑖 ⟩
and |𝑣𝑗 ⟩ must be orthogonal, that is, 𝐵𝑖𝑗 = ⟨𝑣𝑗 |𝑣𝑖 ⟩ = 0. The maximum of the objective func-

tion is precisely the Lovász number of the exclusivity graph, 𝜗(𝐺). By running the Lovász
optimization and calculating 𝜗(𝐺), the Gram matrix is automatically obtained. In our study,
we used the Python package cvxopt as the optimizer for the semidefinite programming.
Since the optimizer is a black-box model we can only get access to the final output matrix 𝐁
. After several trials of optimization, we always get the same Gram matrix in the Extended
Data Figure 1, and the solution has Rank(𝐁) = 37.

To work out the set of rays 𝐫 that give rise to the Gram matrix, we will need to write 𝐁 as the
product of a real matrix and its transpose:
𝐁 = 𝐫𝐫T .

(S5)

The objective is akin to the Cholesky decomposition where the result is limited to be a lower
triangle matrix. However, the Cholesky decomposition only works for symmetric and positive-definite matrices and thus would not work directly for the gram matrix here which is
𝐁 . We
not full-rank. Therefore, we take the first 37 rows and columns of 𝐁 and denote it as ˜
˜ is nondegenerate and thus the Cholesky decomposition can be run on it.
can check that 𝐁
This way, we obtain the first 37 rays. Further, Each of the other 20 rays can be parameterized as a 37-dimensional vector. As the Gram matrix specified their inner product with the
existing rays, it is possible to write these relations as 20 sets of rank-37 linear equations.
𝐁 is full-rank, all these linear systems are uniquely determined, and the last 20
Due to that ˜
rays can be obtained in a deterministic manner using Gaussian elimination.

For the Lovász optimization of the complementary of the Perkel graph, the solution of 𝐁 is
robust probably because it has a symmetric form and preserves the symmetry of the graph.
We cannot prove the optimality of the solution found in terms of dimensionality, that is, we
cannot exclude the possibility that an orthogonal representation of the Perkel graph with a
Gram matrix rank below 37 exists and saturates the Lovász number. The primary difficulty
is because a rank-constrained optimization is generally not convex and it is not possible to
find a solution with semidefinite programming [81]. We have run several trials of see-saw
optimization and cannot find a rank-36 matrix 𝐁 saturating the upper bound of the target

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 54 of 65

## PDF page 55

function and satisfying all the conditions in (S4).

The best estimation of the lowest dimensional realization seems to come from the exis2) to allow the ortence of the graph’s orthogonal realization. The lowest dimension 𝑑 ∗ ( 𝐺
2 to exist satisfies 𝛼( 𝐺
2) ⩽ 𝑑 ∗ ( 𝐺
2) ⩽ 𝜒( 𝐺
2). In our
thogonal representation of a graph 𝐺
2 to be the Perkel graph, we have 𝛼( 𝐺
2) = 19, 𝜒( 𝐺
2) = 29; therefore, some
case, setting 𝐺
improvement for the dimension seems to be allowed, but the resulted orthogonal representation will still be of quite a high dimensionality. As such, it would not reduce the challenge
for the experimental side by a lot. Instead, it is convenient to use the symmetric Gram ma-

trix as found in the semidefinite programming and pursue an experimental observation of
the high-dimensional GHZ-type contextuality.

.4 Pulse encoding
In this subsection, we exemplify how a prepare-and-measure experiment is done in our experiment with a pulse-sequence encoding. We would like to evaluate the projection proba2
bility |⟨\textopeno|𝒂⟩| of the following ray:
⎧
⎪
1
1
1
𝒂=⎪
,
, …,
,
⎨ √19 √19
19
√
⎪⏟⎵⎵⎵⎵⎵⏟⎵⎵⎵⎵⎵⎵⏟
× 19
⎩

on the measurement basis:

⎫
⎪
0,⎵0,
…,⏟0⎪,
⏟
⏟⎵⎵
⎬
× 18
⎪
⎭

(S6)

\textopeno = {− 0.110, 0.170, 0.091, 0.257, 0.040, 0.019, −0.427, −0.131, −0.276, 0.387,

0.112, −0.252, 0.157, 0.233, −0.010, −0.023, 0.119, −0.147, −0.210, 0, 0,
0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0.424,− 0.140, 0.074, 0.028,− 0.123}.

The basis here is not any of the 57 rays in the orthogonal representation of the Perkel
graph, but it is orthogonal to the rays #20 through #38. Thus, this projection probability is
required to build the probability distribution on an orthonormal basis. Also, the first seven

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 55 of 65

## PDF page 56

terms of the intrinsic pulse amplitude ejection ratio from the fiber ring, normalized against
the first pulse, are:
𝒄𝟎 = {1. , 0.783, 0.606, 0.465, 0.356, 0.272, 0.208}.

(S8)

For convenience, we also denote \textopeno0 = {0.208, 0.272, 0.356, 0.465, 0.606, 0.783.1. } as

the entry-reversed kernel of convolution. In Table 1, we summarize the meaning of various
definitions used in this section.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 56 of 65

## PDF page 57

Symbol

Definition

𝒂

𝒄0

(\textopeno)
\textopeno0

Desired input state (measurement basis)
The kernel of convolution, determined only by the fiber ring
The kernel of convolution, but with the entry written in a reversed
direction

The 𝑘-th part of 𝒂 (\textopeno) in the direct-sum expansion:
𝒂𝑘 (
𝑏
𝑏
𝒂 = ⨁ 𝑘 = 1 𝒂𝑘 , \textopeno = ⨁ 𝑘 = 1 \textopeno𝑘 ,
\textopeno𝑘 )
Dim(𝒂𝑘 ) = Dim(\textopeno𝑘 )
\textopeno𝑘

↓

𝒂𝑘↓

𝑉𝑘 (𝑉𝑘 )
↓

𝒂
˜

↓̸

˜
\textopeno

A list with the same elements as \textopeno𝑘 but sorted in the absoluteA list with the same elements as 𝒂𝑘 but sorted according to that
(𝒂𝑘↓ )𝑚 = (𝒂𝑘 )𝑛 if (\textopeno𝑘↓ ) = (\textopeno𝑘 )
value descending order

𝑛

𝑚

Modulation voltages for generating a pulse sequence with the
↓
↓
amplitudes being ⟨\textopeno𝑘 |𝒂𝑘 ⟩ (⟨\textopeno𝑘 |𝒂𝑘 ⟩)

A ray reconstructed by measuring the amplitudes of all ⟨\textopeno𝑘 |𝒂𝑘 ⟩
’s: the theoretical value is 𝒂
˜𝑘 = ⟨\textopeno𝑘 |𝒂𝑘 ⟩
˜ = {1, 1, …, 1}. Also,
An all-one vector: \textopeno
˜ )=𝑏
𝒂 ) = Dim(\textopeno
Dim(˜

Table 1: Summary of various symbol definitions used in the section .4.

To measure the detection probability with the subspace method, the first step is to write
the ray and basis into direct-sum decompositions:
6

𝒂 = ⨁ 𝒂𝑘 ,
𝑘=1

where

𝒂1 = 𝒂2 = {

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

1

,

1

,

1

,

1

,

1

,

1

,

1

√19 √19 √19 √19 √19 √19 √19

},

2/5/25, 4 47 PM
Page 57 of 65

## PDF page 58

𝒂3 = {

and

1

,

1

,

1

,

1

,

√19 √19 √19 √19 √19

𝒂4 = 𝒂5 = 𝒂6 = {0, 0, 0, 0, 0, 0}.
6

\textopeno = ⨁ \textopeno𝑘 ,
𝑘=1

1

where

},

\textopeno1 = {−0.110, 0.170, 0.091, 0.257, 0.040
\textopeno2 = {−0.131, −0.276, 0.387, 0.112, −
\textopeno3 = {−0.010, −0.023, 0.119, −0.147,
\textopeno4 = \textopeno5 = {0, 0, 0, 0, 0, 0},

\textopeno6 = {0, 0.424, −0.140, 0.074, 0.028, −

This way, the inner product can be expressed as ⟨\textopeno|𝒂⟩ = ∑𝑘 = 1 ⟨\textopeno𝑘 |𝒂𝑘 ⟩ as
in the Eq. (7) in the main text.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

𝑏

2/5/25, 4 47 PM
Page 58 of 65

## PDF page 59

Fig. S1: Explanation of waveforms. Left: The pulse encoding for evaluating the inner
product ⟨\textopeno2 |𝒂2 ⟩. Right: The effect of sorting the entries of
\textopeno → \textopeno ↓ . This is how the pulse for the intensity modulator needs to be if
the entries are not sorted. Note the amplitude required to encode some of the entries
exceeds the amplitude in the locking stage.

The second step is to construct the correct modulation signal for the intensity modulator to
measure the inner products ⟨\textopeno𝑘 |𝒂𝑘 ⟩. Throughout this part, we always make the

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 59 of 65

## PDF page 60

intensity modulator work in a small transmission range, so the amplitude after the intensity
modulator has a linear response to the modulation voltage. The modulation signal works by
both creating the desired input state 𝒂 and changing the natural convolution basis
\textopeno0 to the measurement basis \textopeno𝑘 , 𝑘 ∈ [1, 6]. To this purpose, the amplitude of the pulses in the 𝑘-th pulse sequence generated by the intensity modulator should
−1
be proportional to 𝑉𝑘 = 𝒂𝑘 ∘ \textopeno𝑘 ∘ \textopeno0∘ . Here, ∘ means Hadamard (entry-

wise) product and (⋅)
means Hadamard (entry-wise) inverse. In case the dimension of
\textopeno0 does not match that of 𝒂𝑘 and \textopeno𝑘 , the excess entries of \textopeno0 are
∘ −1

truncated. Additionally, to better utilize the linear range of the intensity modulator, we also
sort the entries of the basis \textopeno𝑘 in an absolute-value descending order, hereafter
denoted as \textopeno𝑘↓ , and use \textopeno𝑘↓ to replace \textopeno𝑘 in the experiment.
The entries of the input states are also adjusted accordingly.

We use the second direct-sum subspace as an example. According to the definition above,
the modulation voltage we applied on the intensity modulator, after sorting the entries,
should be proportional to
𝑉2

↓

= 𝒂2 ∘ \textopeno2 ∘ \textopeno0
={

1

,

1

,

↓

1

,

1

,

1

∘ −1

,

1

,

1

√19 √19 √19 √19 √19 √19 √19

}∘{

0.112
0.131 0.157 0.233
0.252
,−
,
,
,−
0.208
0.272 0.356 0.465
0.606

= {0.540, −0.481, 0.441, 0.501, −0.417, −0.352, 0.387}/ √19.

This corresponds to the waveform displayed in the Fig. 3 in the main text. For convenience,
we also show it here in the left subplot of Fig. S1. On the other hand, if we did not implement the sorting procedure, the modulation voltage would become:
𝑉2

↓̸

= 𝒂2 ∘ \textopeno2 ∘ \textopeno0
={

1

,

1

,

↓̸

1

,

1

,

1

∘ −1

,

1

,

1

√19 √19 √19 √19 √19 √19 √19

} ∘ {−

0.131
0.276 0.387 0.112
0.252
,−
,
,
,−
0.208
0.272 0.356 0.465
0.606

= {−0.629, −1.01, 1.09, 0.241, −0.417, 0.201, 0.233}/ √19.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 60 of 65

## PDF page 61

This waveform, corresponding to the right subplot of Fig. S1, would thus require larger modulation amplitudes for some of the entries, and become more susceptible to the non-perfect linear response of the modulator.

The final step is we register the homodyne amplitude when the pulses from all the seven
time-bins have entered the ring, and use this for all the subspaces to create a new pulsed
state. In our case, we measured these six homodyne amplitudes to be:
𝒂 = {1.389, 4.389, −1.650, 0.756, 0.756, 5.66316}. The values are direct readouts from the
˜
oscilloscope trace and no normalization is needed. By taking this as a new ray and convolv˜ = {1, 1, 1, 1, 1, 1} using again the above-mentioned proceing it with a unit kernel \textopeno
˜ |𝒂
dure, we obtained the final unnormalized inner product ⟨\textopeno
˜⟩. Normalizing the
square of the inner product across an orthonormal basis yields the detection probabilities
of different measurements.

.5 Proposed improvement of the setup
As we mentioned in the main text, the current setup is unable to observe contextuality at
the event-level by producing individual events and measure their probability. It is thus not
fully compatible with the requirements of a noncontextual hidden-variable theory, However, we believe that it is possible to modify the setup to accommodate the requirements of
the standard noncontextual model and, at the same time, manifest contextuality. The key
point is to introduce an operation in the measurement procedure that (1) produces eventlevel outcomes and (2) induces negativity to the Wigner function. A photodetection process
at the last stage of the measurement (labeled as “Round b+1” in Fig. 2c in the main text) will
satisfy both of the requirements and promote the current experiment to a bona fide contextuality test. This extended schematic setup is shown in Fig. S2.

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 61 of 65

## PDF page 62

Fig. S2: Proposed setup modification for combining different measurement stages,
“discretizing” the measurement outcome, producing Wigner negativity and making the
experiment meet the prerequisites of the NCHV theory. Comparing with the main setup, the
modification is twofold: a delay and switch stage is added, and the last stage of
measurement uses feedforward and photodetection. SW switch, PD photodetector.

The setup in Fig. S2 contains three more stages compared to our setup. The first is that the
encoding of the high-dimensional state should happen on the different segments of a single
pulse train. At the beginning of the setup, a routing and delaying unit is added to enable the
measurement from round 1 to round 𝑏 in the main setup to happen one by one in the same
setup. The switch and routing between MHz-frequency pulses are possible with commercial
electro-optical modulators [38] and the fiber delay lines for separating different segments
of pulses will be of moderate length. Moreover, it appears that the relative phases between

different delay lines does not need to be locked: by adding a pilot wave in front of every
segment, the phase between them can be individually determined, which will greatly reduce
the challenge due to the phase locking of long fibers.

The second point of change is that, after the homodyne detection, the outcomes would be
sent to a field programmable gate array (FPGA) for real-time processing, thus the 𝑏-rounds

of homodyne measurement outcomes would be stored inside the FPGA, and the FPGA
would make another round of preparation process, but this time with the quantum state
encoded on a single photon. A photodetection process at the end of the setup would then
project the input state on a single basis. This way, the measurement stage starting from the
“basis” selection until the photodetection would constitute a mapping from a Hilbert space
to an event-level outcome, and conform to the requirements of a NCHV theory. Further,
changing the power detection to photodetection will maintain the probability, so we would

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 62 of 65

## PDF page 63

expect to observe the same amount of contextuality with the modified setup. We consider
encoding the photonic qudit on the spatial mode degree of freedom using spatial light
modulation as a possible approach [56]. This kind of setup is also compatible with a FPGAbased control system [82, 83]. Finally, the FPGA for doing the necessary calculation and
implementing the feedforward operation itself was available in the setting of coherent Ising
machine [31, 32].

.6 Full proof of the Theorem 3
In this subsection, we prove that there is no strongly regular graph with clique number 2
and chromatic number 3 such that the Lovász number of its complement graph is 3. By the
Theorem 1 in the main text, it means no strongly regular graph hosts a three-context GHZtype paradox.
A strongly regular graph with four parameters 𝑛, 𝑘, 𝑎 and 𝑐, denoted by SRG(𝑛, 𝑘, 𝑎, 𝑐), is a
𝑛-vertex 𝑘-regular graph such that every two adjacent vertices have 𝑎 common neighbors,

and that every two non-adjacent vertices have 𝑐 common neighbors. The theory of strongly
regular graphs was introduced by Bose [52] in 1963 and was then used in many different
mathematical fields, such as partial geometry [52], group theory [84] and coding theory [
85].
Before proving the main lemma, let us list out some necessary symbols. For any graph 𝐺,
we use 𝐴(𝐺), 𝛼(𝐺), 𝜔(𝐺), 𝜒(𝐺) and 𝜗(𝐺) to denote its adjacent matrix, independence number, clique number, chromatic number and Lovász number, respectively. Suppose that there
exists a strongly regular graph 𝐺 = SRG(𝑛, 𝑘, 𝑎, 𝑐) satisfying 𝜔(𝐺) = 2, 𝜒(𝐺) = 3 and
2) = 3. Note that as 𝜔(𝐺) = 2, we have 𝑎 = 0.
𝜗( 𝐺

We will first establish an inequality that 𝑐 ⩽ 𝑘 ⩽ 2𝑐 + 3. Let 𝐴 = 𝐴(𝐺). We will consider the
entries of 𝐴2 . For any two vertices 𝑖 and 𝑗, (𝐴2 )𝑖𝑗 is the number of walks of length 2 which
starts at 𝑖 and ends at 𝑗. So for adjacent vertices 𝑖 and 𝑗, (𝐴2 )𝑖𝑗 = 0 because 𝑖 and 𝑗 has no

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 63 of 65

## PDF page 64

common neighbors. For non-adjacent vertices 𝑖 and 𝑗, (𝐴2 )𝑖𝑗 = 𝑐 because 𝑖 and 𝑗 has exact-

ly 𝑐 common neighbors. And for any vertex 𝑖, (𝐴2 )𝑖𝑖 = 𝑘 because 𝐺 is a 𝑘-regular graph.
Therefore, we have 𝐴2 = 𝑐(𝐽 − 𝐴) + (𝑘 − 𝑐)𝐼, where 𝐽 is the 𝑛 × 𝑛 matrix with all entries
equal to 1 and 𝐼 is the 𝑛 × 𝑛 identity matrix. This implies that 𝐴 has exactly three different
eigenvalues 𝑘, 𝜆1 , 𝜆2 such that 𝜆1 and 𝜆2 are the roots of 𝜆2 + 𝑐𝜆 − (𝑘 − 𝑐) = 0. Therefore
𝜆1 =

−𝑐 −

𝑐2 + 4(𝑘 − 𝑐)
√
2

−𝑐 +

, and 𝜆2 =

𝑐2 + 4(𝑘 − 𝑐)
√
2

.

(S23)

The famous Hoffman–Delsarte [70, 71] eigenvalue bound says that for 𝑛-vertex 𝑘-regular
−𝜏
𝑛, where 𝜏 is the smallest eigenvalue of 𝐴(𝐻). Using this
graph 𝐻, we have 𝛼(𝐻) ⩽
𝑘−𝜏
bound, we have
𝛼(𝐺) ⩽

−𝜆1
𝑛.
𝑘 − 𝜆1

(S24)

Also, since 𝛼(𝐺)𝜒(𝐺) ⩾ 𝑛, we get another inequality
𝑘 − 𝜆1
3 = 𝜒(𝐺) ⩾
=
−𝜆1

2𝑘 + 𝑐 +
𝑐+

𝑐2 + 4(𝑘 − 𝑐)
√

𝑐2

√

+ 4(𝑘 − 𝑐)

.

(S25)

By solving this inequality, we have 𝑐 + 2 − √𝑐2 + 4 ⩽ 𝑘 ⩽ 𝑐 + 2 + √𝑐2 + 4. Since 𝑘, 𝑐 are
non-negative integers and 𝑐 ⩽ 𝑘, we now have
𝑐 ⩽ 𝑘 ⩽ 2𝑐 + 3.

(S26)

Next we show that in fact 𝑘 only can be two possible integer values, namely 𝑘 ∈ {𝑐, 2𝑐 + 1},
by considering the multiplicities of 𝜆1 and 𝜆2 . Let 𝑚𝑖 be the multiplicity of 𝜆𝑖 for 𝑖 ∈ {1, 2}.
Since the multiplicity of 𝑘 is one, we have 𝑚1 + 𝑚2 = 𝑛 − 1; also by considering the trace of
𝐴, we get 𝑚1 𝜆1 + 𝑚2 𝜆2 + 𝑘 = 0. Solving the above two equations, we obtain that

(S27)

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 64 of 65

## PDF page 65

− 𝑘2 + (2 − 𝑐)𝑘
(𝑛 − 1)𝜆2 + 𝑘
𝑛−1
𝑚1 =
=
+
.
𝜆2 − 𝜆1
2
2 𝑐2 + 4(𝑘 − 𝑐)
√

As 𝑚1 is an integer, we conclude that
𝑐 ⩽ 𝑘 ⩽ 2𝑐 + 3, we have

𝑐⩽

So

(S27)

𝑐2 + 4(𝑘 − 𝑐) must be an integer. Using
√

𝑐2 + 4(𝑘 − 𝑐) ⩽ √𝑐2 + 4𝑐 + 12 < 𝑐 + 4.
√

𝑐2 + 4(𝑘 − 𝑐) ∈ {𝑐, 𝑐 + 1, 𝑐 + 2, 𝑐 + 3}. An easy analysis shows that 𝑘 ∈ {𝑐, 2𝑐 + 1}.
√

(S28)

By considering the number of paths of length 2 with a fixed an endpoint in 𝐺, we have an
equality (𝑛 − 𝑘 − 1)𝑐 = 𝑘(𝑘 − 1). Therefore, 𝑛 = 2𝑐 when 𝑘 = 𝑐, and 𝑛 = 6𝑐 + 4 when

𝑘 = 2𝑐 + 1. That is, 𝐺 is either SRG(2𝑐, 𝑐, 0, 𝑐) or SRG(6𝑐 + 4, 2𝑐 + 1, 0, 𝑐). In the former case,
𝐺 = SRG(2𝑐, 𝑐, 0, 𝑐) must be a complete bipartite graph such that each part has exactly 𝑐
vertices. Therefore 𝜒(𝐺) = 2, a contradiction. So from now on, we only need to consider
the later case 𝐺=SRG(6𝑐 + 4, 2𝑐 + 1, 0, 𝑐).
We first consider the cases when 𝑐 ⩽ 2. If 𝑐 = 0, then 𝐺 is exactly a single edge, implying

that 𝜒(𝐺) = 2, a contradiction. If 𝑐 = 1, then 𝐺 = SRG(10, 3, 0, 1) is unique, i.e., the famous
5
Peterson graph [86]. So we have 𝜗( 𝐺
2) = [41] which is again a contradiction. If 𝑐 = 2,
2
then 𝐺 = SRG(16, 5, 0, 2) is also unique, i.e., the famous Clebsch graph [87]. In this case, we
have 𝜒(𝐺) = 4, a contradiction.

It remains to show that 𝐺=SRG(6𝑐 + 4, 2𝑐 + 1, 0, 𝑐) does not exist for 𝑐 ⩾ 3. Suppose such 𝐺
exists. Take an arbitrary vertex 𝑣 in 𝐺. Let 𝑁(𝑣) denote the set of neighbors of 𝑣, and 𝑉1 denote the non-neighbors of 𝑣. As 𝐺 has no triangles, 𝑁(𝑣) is an independent set of size
2𝑐 + 1 and |𝑉1 | = 4𝑐 + 2. By the properties of strongly regularity of 𝐺, any vertex 𝑤 in 𝑁(𝑣)
has exactly 2𝑐 neighbors in 𝑉1 , and any vertex 𝑢 in 𝑉1 has exactly 𝑐 neighbors in 𝑁(𝑣) and
𝑐 + 1 neighbors in 𝑉1 .

:

https://arxiv.org/html/2208.07794v3?utm_source=chatgpt.com

2/5/25, 4 47 PM
Page 65 of 65
