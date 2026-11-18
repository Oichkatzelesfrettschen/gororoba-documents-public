Source: https://link.springer.com/content/pdf/10.1007/JHEP07(2014)079.pdf
PDF sha256: 875b92ad3cd30a1fe3ee764d2b1455f7240b8a9f62523f7bc4ca4c963d387141
License: CC-BY
Language: eng
Fidelity: machine-gated

# Transcription of alwall_2014_automated_computation_tree_level_next.pdf

Transcription of `alwall_2014_automated_computation_tree_level_next.pdf` in this directory, 157 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-157 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: May 20, 2014
Accepted: June 25, 2014
Published: July 17, 2014

The automated computation of tree-level and
next-to-leading order differential cross sections, and
their matching to parton shower simulations

a

Department of Physics, National Taiwan University, Taipei 10617, Taiwan
PH Department, TH Unit, CERN, CH-1211 Geneva 23, Switzerland
c
SLAC National Accelerator Laboratory,
2575 Sand Hill Road, Menlo Park, CA 94025-7090 U.S.A.
d
CP3, Université Catholique de Louvain, B-1348 Louvain-la-Neuve, Belgium
e
Department of Physics and State Key Laboratory of Nuclear Physics and Technology,
Peking University,
Beijing 100871, China
f
University of Illinois, Urbana, IL 61801-3080, U.S.A.
g
Physik-Institut, Universität Zürich, Winterthurerstrasse 190, 8057 Zurich, Switzerland
h
Sorbonne Universités, UPMC Univ. Paris 06, UMR 7589, LPTHE, F-75005, Paris, France
i
CNRS, UMR 7589, LPTHE, F-75005, Paris, France
b

E-mail: johan.alwall@gmail.com, rikkert.frederix@cern.ch,
stefano.frixione@cern.ch, vahirsch@slac.stanford.edu,
fabio.maltoni@uclouvain.be, olivier.mattelaer@uclouvain.be,
huasheng.shao@cern.ch, tstelzer@illinois.edu, torriell@physik.uzh.ch,
zaro@lpthe.jussieu.fr
Abstract: We discuss the theoretical bases that underpin the automation of the computations of tree-level and next-to-leading order cross sections, of their matching to parton
shower simulations, and of the merging of matched samples that differ by light-parton multiplicities. We present a computer program, MadGraph5 aMC@NLO, capable of handling
all these computations — parton-level fixed order, shower-matched, merged — in a unified
framework whose defining features are flexibility, high level of parallelisation, and human
intervention limited to input physics quantities. We demonstrate the potential of the program by presenting selected phenomenological applications relevant to the LHC and to a
1-TeV e+ e− collider. While next-to-leading order results are restricted to QCD corrections
to SM processes in the first public version, we show that from the user viewpoint no changes
have to be expected in the case of corrections due to any given renormalisable Lagrangian,
and that the implementation of these are well under way.
Keywords: Monte Carlo Simulations, NLO Computations
ArXiv ePrint: 1405.0301

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

doi:10.1007/JHEP07(2014)079

JHEP07(2014)079

J. Alwall,a R. Frederix,b S. Frixione,b V. Hirschi,c F. Maltoni,d O. Mattelaer,d
H.-S. Shao,e T. Stelzer,f P. Torriellig and M. Zaroh,i

## PDF page 2

Contents
1

2 Theoretical bases and recent progress
2.1 Methodology of computation
2.2 General features for SM and BSM physics
2.2.1 Complex mass scheme
2.2.2 BSM-specific capabilities
2.3 LO computations
2.3.1 Generation of tree-level matrix elements
2.3.2 Width calculator
2.3.3 Event reweighting
2.3.4 Tree-level merging
2.4 NLO computations
2.4.1 NLO cross sections and FKS subtraction: MadFKS
2.4.2 One-loop matrix elements: MadLoop
2.4.3 Integration of one-loop contributions
2.4.4 Matching to showers: MC@NLO
2.4.5 Merging samples at the NLO: FxFx
2.5 Spin correlations: MadSpin

3
4
5
6
7
8
9
11
12
15
16
21
25
39
43
50
55

3 How to perform a computation
3.1 LO-type generation and running
3.2 NLO-type generation and running
3.2.1 (N)LO+PS results
3.2.2 f(N)LO results
3.3 Possibilities for LO simulations

59
60
62
64
67
69

4 Illustrative results
4.1 Total cross sections
4.2 Differential distributions
4.3 One-loop SM and BSM results: a look ahead

70
70
83
100

5 Conclusions and outlook

106

A Technical prerequisites, setup, and structure

109

B Advanced usage
B.1 Models, basic commands, and extended options
B.2 Setting the hard scales at the NLO
B.3 Scale and PDF uncertainties: the NLO case
B.4 Scale and PDF uncertainties: the LO case

112
113
118
120
124

–i–

JHEP07(2014)079

1 Introduction

## PDF page 3

B.5 Other LO reweighting applications
B.6 Output formats and standalone libraries

125
126

C Features of one-loop computations
C.1 TIR and IREGI
C.2 Quantitative profile of MadLoop performances
C.3 Computation of the integrand polynomial coefficients

127
127
130
131

D Third-party codes included in MadGraph5 aMC@NLO

134

Introduction

Quantum Chromo Dynamics is more than forty years old [1, 2], and perturbative calculations of observables beyond the leading order are almost as old, as is clearly documented in
several pioneering works (see e.g. refs. [3–9]), where the implications of asymptotic freedom
had been quickly understood. The primary motivation for such early works was a theoretical one, stemming from the distinctive features of QCD (in particular, the involved infrared
structure, and the fact that its asymptotic states are not physical), which imply the need
of several concepts (such as infrared safety, hadron-parton duality, and the factorisation of
universal long-distance effects) that come to rescue, and supplement, perturbation theory.
On the other hand, the phenomenological necessity of taking higher-order effects into account was also acknowledged quite rapidly, in view of the structure of jet events in e+ e−
collisions and of the extraction of αS from data.
Despite this very early start, the task of computing observables beyond the Born level
in QCD has remained, until very recently, a highly non-trivial affair: the complexity of
the problem, due to both the calculations of the (tree and loop) matrix elements and the
need of cancelling the infrared singularities arising from them, has generated a very significant theoretical activity by a numerous community. More often than not, different cases
(observables and/or processes) have been tackled in different manners, with the introduction of ad-hoc solutions. This situation has been satisfactory for a long while, given that
beyond-Born results are necessary only when precision is key (and, to a lesser extent, when
large K factors are relevant), and when many hard and well-separated jets are crucial for
the definition of a signature; these conditions have characterized just a handful of cases in
the past, especially in hadronic collisions (e.g., the production of single vector bosons, jet
pairs, or heavy quark pairs).
The advent of the LHC has radically changed the picture since, in a still relatively
short running time, it has essentially turned hadronic physics into a high-precision domain, and one where events turning up in large-pT tails are in fact not so rare, in spite
of being characterised by small probabilities. Furthermore, the absence so far of clear
signals of physics beyond the Standard Model implies an increased dependence of discovery strategies upon theoretical predictions for known phenomena. These two facts show

–1–

JHEP07(2014)079

1

## PDF page 4

–2–

JHEP07(2014)079

that presently the phenomenological motivations are extremely strong for higher-order and
multi-leg computations of all observables of relevance to LHC analyses.
While a general solution is not known for the problem of computing exactly the perturbative expansion for any observable up to an arbitrarily large order in αS , if one restricts
oneself to the case of the first order beyond the Born one (next-to-leading order, NLO
henceforth), then such a solution does actually exist; in other words, there is no need
for ad-hoc strategies, regardless of the complexity of the process under study. This remarkable fact results from two equally important theoretical achievements. Namely, a
universal formalism for the cancellation of infrared singularities [10–14], and a technique
for the algorithmic evaluation of renormalised one-loop amplitudes [15–25], both of which
must work in a process- and observable independent manner. At the NLO (as opposed
to the NNLO and beyond) there is the further advantage that fixed-order computations
can be matched to parton-shower event generators (with either the MC@NLO [26] or the
POWHEG [27] method — see also refs. [28–37] for early, less-developed, or newer related
approaches), thus enlarging immensely the scope of the former, and increasing significantly
the predictive power of the latter.
It is important to stress that while so far we have explicitly considered the case of
QCD corrections, the basic theoretical ideas at the core of the subtraction of infrared
singularities, of the computation of one-loop matrix elements, and of the matching to
parton showers will require no, or minimal, changes in the context of other renormalisable
theories, QCD being essentially a worst-case scenario. This is evidently true for treelevel multi-leg computations, as is proven by the flexibility and generality of tools such as
MadGraph5 [38], that is able to deal with basically any user-defined Lagrangian.
In summary, there are both the phenomenological motivations and the theoretical
understanding for setting up a general framework for the computation of (any number of)
arbitrary observables in an arbitrary process at the tree level or at the NLO, with or without
the matching to parton showers. We believe that the most effective way of achieving this
goal is that of automating the whole procedure, whose technological challenges can be
tackled with high-level computer languages capable of dealing with abstract concepts, and
which are readily available.
The aim of this paper is that of showing that the programme sketched above has
been realised, in the form of a fully automated and public computer code, dubbed MadGraph5 aMC@NLO. As the name suggests, such a code merges in a unique framework all
the features of MadGraph5 and of aMC@NLO, and thus supersedes both of them (and
must be used in their place). It also includes several new capabilities that were not available in these codes, most notably those relevant to the merging of event samples with
different light-parton multiplicities. We point out that MadGraph5 aMC@NLO contains
all ingredients (the very few external dependencies that are needed are included in the
package) that are necessary to perform an NLO, possibly plus shower (with the MC@NLO
formalism), computation: it thus is the first public (since Dec. 16th , 2013) code, and so
far also the only one, with these characteristics. Particular attention has been devoted to
the fact that calculations must be doable by someone who is not familiar with Quantum
Field Theories, and specifically with QCD. We also show, in general as well as with explicit

## PDF page 5

2

Theoretical bases and recent progress

At the core of MadGraph5 aMC@NLO lies the capability of computing tree-level and oneloop amplitudes for arbitrary processes. Such computations are then used to predict physical observables with different perturbative accuracies and final-state descriptions. Since
there are quite a few possibilities, we list them explicitly here, roughly in order of increasing
complexity, and we give them short names that will render their identification unambiguous
in what follows.
1. fLO: this is a tree- and parton-level computation, where the exponents of the coupling
constants are the smallest for which a scattering amplitude is non zero. No shower
is involved, and observables are reconstructed by means of the very particles that
appear in the matrix elements.
2. fNLO: the same as fLO, except for the fact that the perturbative accuracy is the
NLO one. As such, the computation will involve both tree-level and one-loop matrix
elements.
3. LO+PS: uses the matrix elements of an fLO computation, but matches them to
parton showers. Therefore, the observables will have to be reconstructed by using
the particles that emerge from the Monte Carlo simulation.
4. NLO+PS: same as LO+PS, except for the fact that the underlying computation is
an NLO rather than an LO one. In this paper, the matching of the NLO matrix
elements with parton showers is done according to the MC@NLO formalism.

–3–

JHEP07(2014)079

examples, how the construction of our framework lends itself naturally to its extension to
NLO corrections in theories other than QCD, in keeping with the fact that such a flexibility
is one of the standard features of the tree-level computations which were so far performed
by MadGraph, and that has been inherited by MadGraph5 aMC@NLO.
It is perhaps superfluous to point out that approaches to automated computations constitute a field of research which has a long history, but which has had an exponential growth
in the past few years, out of the necessities and possibilities outlined above. The number of
codes which have been developed, either restricted to leading order (LO henceforth) predictions [38–53], or including NLO capabilities [54–82] is truly staggering. The level of automation and the physics scope of such codes, not to mention other, perhaps less crucial, characteristics, is extremely diverse, and we shall make no attempt to review this matter here.
We have organized this paper as follows. In section 2, we review the theoretical bases
of our work, and discuss new features relevant to future developments. In section 3 we
explain how computations are performed. Section 4 presents some illustrative results,
relevant to a variety of situations: total cross sections at the LHC and future e+ e− colliders,
differential distributions in pp collisions, and benchmark one-loop pointwise predictions, in
the Standard Model and beyond. We finally conclude in section 5. Some technicalities are
reported in appendices A to D.

## PDF page 6

5. MLM-merged: combines several LO+PS samples, which differ by final-state multiplicities (at the matrix-element level). In our framework, two different approaches,
called kT -jet and shower-kT schemes, may be employed.
6. FxFx-merged: combines several NLO+PS samples, which differ by final-state multiplicities.

2.1

Methodology of computation

The central idea of MadGraph5 aMC@NLO is the same as that of the MadGraph family.
Namely, that the structure of a cross section, regardless of the theory under consideration
and of the perturbative order, is essentially independent of the process, and as such it can
be written in a computer code once and for all. For example, phase spaces can be defined
in full generality, leaving only the particle masses and their number as free parameters (see
e.g. ref. [83]). Analogously, in order to write the infrared subtractions that render an NLO
cross section finite, one just needs to cover a handful of cases, which can be done in a universal manner. Conversely, matrix elements are obviously theory- and process-dependent,
but can be computed starting from a very limited number of formal instructions, such as
Feynman rules or recursion relations. Thus, MadGraph5 aMC@NLO is constructed as a
meta-code, that is a (Python) code that writes a (Python, C++, Fortran) code, the latter
being the one specific to the desired process. In order to do so, it needs two ingredients:
• a theory model;
• a set of process-independent building blocks.
A theory model is equivalent to the Lagrangian of the theory plus its parameters, such as
couplings and masses. Currently, the method of choice for constructing the model given a
Lagrangian is that of deriving its Feynman rules, that MadGraph5 aMC@NLO will eventually use to assemble the matrix elements. At the LO, such a procedure is fully automated in

–4–

JHEP07(2014)079

We would like to stress the fact that having all of these different simulation possibilities
embedded in a single, process-independent framework allows one to investigate multiple
scenarios while being guaranteed of their mutual consistency (including that of the physical
parameters such as coupling and masses), and while keeping the technicalities to a minimum
(since the majority of them are common to all types of simulations). For example, one
may want to study the impact of perturbative corrections with (NLO+PS vs LO+PS) or
without (fNLO vs fLO) the inclusion of a parton shower. Or to assess the effects of the
showers at the LO (LO+PS vs fLO) and at the NLO (NLO+PS vs fNLO). Or to check how
the inclusion of different-multiplicity matrix elements can improve the predictions based
on a fixed-multiplicity underlying computation, at the LO (MLM-merged vs LO+PS) and
at the NLO (FxFx-merged vs NLO+PS).
In the remainder of this section we shall review the theoretical ideas that constitute the
bases of the computations listed above in items 1–6. Since such a background is immense,
we shall sketch the main characteristics in the briefest possible manner, and rather discuss
recent advancements that have not yet been published.

## PDF page 7

FeynRules [84–89]. NLO cross sections pose some extra difficulties, because Feynman rules

2.2

General features for SM and BSM physics

Since the release of MadGraph5 a significant effort, whose results are now included in
MadGraph5 aMC@NLO, went into extending the flexibility of the code at both the input and the output levels. While the latter is mostly a technical development (see appendix B.6), which allows one to use different parts of the code as standalone libraries
and to write them in various computer languages, the former extends the physics scope of
MadGraph5 aMC@NLO w.r.t. that of MadGraph5 in several ways, and in particular for
what concerns the capability of handling quantities (e.g., form factors, particles with spin
larger than one, and so forth) that are relevant to BSM theories. Such an extension, to be
1

We expect they will in the next public version [90], since development versions exist that are already
capable of doing so — see e.g. section 4.3.
2
Note that these are a finite and typically small number of process-independent quantities.

–5–

JHEP07(2014)079

are not sufficient for a complete calculation — one needs at least UV counterterms, possibly
plus other rules necessary to carry out the reduction of one-loop amplitudes (we shall generically denote the latter by R2 , adopting the notation of the Ossola-Papadopoulos-Pittau
method [18]). These NLO-specific terms are presently not computed by FeynRules1 and
have to be supplied by hand,2 as was done for QCD corrections to SM processes. Therefore,
while the details are unimportant here, one has to bear in mind that there are “LO” and
“NLO” models to be employed in MadGraph5 aMC@NLO — the former being those that
could also be adopted by MadGraph5, and the latter being the only ones that permit the
user to exploit the NLO capabilities of MadGraph5 aMC@NLO.
Given a process and a model, MadGraph5 aMC@NLO will build the process-specific
code (which it will then proceed to integrate, unweight, and so forth) by performing two
different operations. a) The writing of the matrix elements, by computing Feynman diagrams in order to define the corresponding helicity amplitudes, using the rules specified
by the model. b) Minimal editing of the process-independent building blocks. In the examples given before, this corresponds to writing definite values for particles masses and
the number of particles, and to select the relevant subtraction terms, which is simply done
by assigning appropriate values to particle identities. The building blocks modified in this
manner will call the functions constructed in a). Needless to say, these operations are
performed automatically, and the user will not play any role in them.
We conclude this section by emphasising a point which should already be clear from the
previous discussion to the reader familiar with recent MadGraph developments. Namely
that, in keeping with the strategy introduced in MadGraph5 [38], we do not include among
the process-independent building blocks the routines associated with elementary quantities
(such as vertices and currents), whose roles used to be played by the HELAS routines [91]
in previous MadGraph versions [39, 51]. Indeed, the analogues of those routines are now
automatically and dynamically created by the module ALOHA [92] (which is embedded
in MadGraph5 aMC@NLO), which does so by gathering directly the relevant information
from the model, when this is written in the Universal FeynRules Output (UFO [93])
format. See section 2.3.1 for more details on this matter.

## PDF page 8

discussed in the remainder of this section and partly in section 2.3.1, goes in parallel with
the analogous enhanced capabilities of FeynRules, and focuses on models and on their use.
Thus, it is an overarching theme of relevance to both LO and NLO simulations, in view of
the future complete automation of the latter in theories other than the SM. Some of the
topics to which significant work has been lately devoted in MadGraph5 aMC@NLO, and
which deserve highlighting, are the following:
1. Complex mass scheme (section 2.2.1).
2. Support of various features, of special relevance to BSM physics (section 2.2.2).

4. Output formats and standalone libraries (appendix B.6).
5. Feynman gauge in the SM (section 2.4.2).
6. Improvements to the front-end user interface (the MadGraph5 aMC@NLO shell —
appendix A).
7. Hierarchy of couplings: models that feature more than one coupling constant order
them in terms of their strengths, so that for processes with several coupling combinations at the cross section level only the assumed numerically-leading contributions
will be simulated (unless the user asks otherwise) — section 2.4 and appendix B.1.
We would finally like to emphasise that in the case of LO computations, be they fLO,
LO+PS, or merged, one can always obtain from the short-distance cross sections a set of
physical unweighted events. The same is not true at the NLO: fNLO cross sections cannot
be unweighted, and unweighted MC@NLO events are not physical if not showered. This
difference explains why at the LO we often adopt the strategy of performing computations
with small, self-contained modules whose inputs are Les Houches event (LHE henceforth)
files [94, 95], while at the NLO this is typically not worth the effort — compare e.g. appendices B.3 and B.4, where the computation of scale and PDF uncertainties at the NLO and
LO, respectively, is considered. Further examples of modules relevant to LO simulations
are given in section 2.3.3.
2.2.1

Complex mass scheme

In a significant number of cases, the presence of unstable particles in perturbative calculations can be dealt with by using the Narrow Width Approximation (NWA).3 However,
when one is interested in studying either those kinematical regions that correspond to such
unstable particles being very off-shell, or the production of broad resonances, or very involved final states, it is often necessary to go beyond the NWA. In such cases, one needs
to perform a complete calculation, in order to take fully into account off-shell effects, spin
correlations, and interference with non-resonant backgrounds in the presence of possibly
large gauge cancellations. Apart from technical difficulties, the inclusion of all resonant
3

See section 2.5 for a general discussion of the NWA and of other related approaches.

–6–

JHEP07(2014)079

3. Improvements to the FeynRules/UFO/ALOHA chain (section 2.3.1).

## PDF page 9

• The EW scheme is chosen where α(mZ ), mZ , and mW (the former a real number, the
latter two complex numbers defined as in the previous item) are input parameters.

• All other parameters (e.g., GF and θW ) assume complex values. In particular, Yukawa
couplings are defined by using the complex masses introduced in the first item.
At the NLO, the necessity of performing UV renormalisation introduces additional complications. At present, the prescriptions of ref. [103] have been explicitly included and
validated. As was already mentioned in section 2.1, this operation will not be necessary in
the future, when it will be replaced by an automatic procedure performed by FeynRules.
2.2.2

BSM-specific capabilities

One of the main motivations to have very precise SM predictions, and therefore to include
higher order corrections, is that of achieving a better experimental sensitivity in the context
of New Physics (NP) searches. At the same time, it is necessary to have as flexible,
versatile, and accurate simulations as is possible not only for the plethora of NP models
proposed so far, but for those to be proposed in the future as well. These capabilities have
been one of the most useful aspects of the MadGraph5 suite; they are still available in
MadGraph5 aMC@NLO and, in fact, have been further extended.
As was already mentioned, the required flexibility is a direct consequence of using the
UFO models generated by dedicated packages such as FeynRules or SARAH [104], and of
making MadGraph5 aMC@NLO compatible with them. Here, we limit ourselves to listing
the several extensions recently made to the UFO format and the MadGraph5 aMC@NLO
code, which have a direct bearing on BSM simulations.
• The possibility for the user to define the analytic expression for the propagator of a
given particle in the model [105].

–7–

JHEP07(2014)079

and non-resonant diagrams does not provide one with a straightforward solution, since the
(necessary) inclusion of the widths of the unstable particles — which amounts to a resummation of a specific subset of terms that appear at all orders in perturbation theory —
leads, if done naively, to a violation of gauge invariance. While this problem can be evaded
in several ways at the LO (see e.g. refs. [96–101]), the inclusion of NLO effects complicates
things further. Currently, the most pragmatic and widely-used solution is the so-called
complex mass scheme [102, 103], that basically amounts to an analytic continuation in the
complex plane of the parameters that enter the SM Lagrangian, and which are related
to the masses of the unstable particles. Such a scheme can be shown to maintain gauge
invariance and unitarity at least at the NLO, which is precisely our goal here.
In MadGraph5 aMC@NLO it is possible to employ the complex mass scheme in the
context of both LO and NLO simulations, by instructing the code to use a model that includes the analytical continuation mentioned above (see the Setup part of appendix B.1 for
an explicit example). For example, at the LO this operation simply amounts to upgrading
the model that describes SM physics in the following way [102]:
√
• The masses mk of the unstable particles are replaced by m2k − imk Γk .

## PDF page 10

• The implementation of the analytical formulae for two-body decay widths [106], which
allows one to save computing time when the knowledge of the widths of all unstable
particles in the model is needed (see section 2.3.2).

• Models and processes are supported that feature massive and massless particles of
spin 3/2 [105]. This implies that all spins are supported in the set {0, 1/2, 1, 3/2, 2}.
• The support of multi-fermion interactions, including the case of identical particles
in the final state, and of UFO models that feature vertices with more than one
fermion flow. Multi-fermion interactions with fermion-flow violation, such as in the
presence of Majorana particles, are not supported. Such interactions, however, can
be implemented by the user by splitting the interaction in multiple pieces connected
via heavy scalar particles, a procedure that allows one to define unambiguously the
fermion flow associated with each vertex.
While not improved with respect to what was done in MadGraph5, we remind the reader
that the module responsible for handling the colour algebra is capable of treating particles
whose SUc (3) representation and interactions are non-trivial, such as the sextet and ǫijk type vertices respectively.
2.3

LO computations

The general techniques and strategies used in MadGraph5 aMC@NLO to integrate a treelevel partonic cross section, and to obtain a set of unweighted events from it, have been
inherited from MadGraph5; the most recent developments associated with them have been
presented in ref. [38], and will not be repeated here. After the release of MadGraph5, a
few optimisations have been introduced in MadGraph5 aMC@NLO, in order to make it
more efficient and flexible than its predecessor. Here, we limit ourselves to listing the two
which have the largest overall impact.
1. The phase-space integration of decay-chain topologies has been rewritten, in order
to speed up the computations and to deal with extremely long decay chains (which
can now easily extend up to sixteen particles). In addition, the code has also been
optimised to better take into account invariant-mass cuts, and to better handle the
case where interference effects are large.
4

Which obviously implies that this option is not available should other type of outputs be chosen (see appendix B.6).
Further details are given at: https://cp3.irmp.ucl.ac.be
/projects/madgraph/wiki/FormFactors.

–8–

JHEP07(2014)079

• The possibility to define form factors (i.e., coupling constants depending on the kinematic of the vertex) directly in the UFO model. Note that, since form factors cannot
be derived from a Lagrangian, they cannot be dealt with by programs like FeynRules,
and have therefore to be coded by hand in the models. In order to be completely
generic, the possibility is also given to go beyond the format of the current UFO
syntax, and to code the form factors directly in Fortran.4

## PDF page 11

In the following sections, we shall discuss various topics relevant to the calculation of
LO-accurate physical quantities. Section 2.3.1 briefly reviews the techniques employed
in the generation of tree-level amplitudes, emphasising the role of recent UFO/ALOHA
developments. Section 2.3.2 presents the module that computes the total widths of all
unstable particles featured in a given model. Section 2.3.3 describes reweighting techniques.
Finally, in section 2.3.4 we review the situation of MLM-merged computations.
2.3.1

Generation of tree-level matrix elements

The computation of amplitudes at the tree level in MadGraph5 aMC@NLO has a scope
which is in fact broader than tree-level physics simulations, since all matrix elements used
in both LO and NLO computations are effectively constructed by using tree-level techniques. While this is obvious for all amplitudes which are not one-loop ones, in the case of
the latter it is a consequence of the L-cutting procedure, which was presented in detail in
ref. [68] and which, roughly speaking, stems from the observation that any one-loop diagram
can be turned into a tree-level one by cutting one of the propagators that enter the loop.
Furthermore, as was also explained in ref. [68] and will be discussed in section 2.4.2, all
of the companion operations of one-loop matrix element computations (namely, UV renormalisation and R2 counterterms) can also be achieved through tree-level-like calculations,
which are thus very central to the whole MadGraph5 aMC@NLO framework.
The construction of tree-level amplitudes in MadGraph5 aMC@NLO is based on three
key elements: Feynman diagrams, helicity amplitudes, and colour decomposition. Helicity
amplitudes [107–113] provide a convenient and effective way to evaluate matrix elements
for any process in terms of complex numbers, which is quicker and less involved than one
5

We stress that this statement is non-trivial just because it applies to LO computations. In the context
of NLO simulations this is the standard situation, and aMC@NLO has obviously been always capable of
handling it.

–9–

JHEP07(2014)079

2. It is now possible to integrate matrix elements which are not positive-definite.5 This is
useful e.g. when one wants to study a process whose amplitude can be written as a sum
of two terms, which one loosely identifies with a “signal” and a “background”. Rather
than integrating |S + B|2 , one may consider |S|2 + 2ℜ(SB ⋆ ) and |B|2 separately,
which is a more flexible approach (e.g. by giving one the possibility of scanning a
parameter space, in a way that affects S while leaving B invariant), that also helps
reduce the computation time by a significant amount. One example of this situation
is the case when |B|2 is numerically dominant, and thus corresponds to a very large
sample of events which can however be generated only once, while smaller samples
of events, that correspond to |S|2 + 2ℜ(SB ⋆ ) for different parameter choices, can be
generated as many times as necessary. Another example is that of an effective theory
where a process exists (S) that is also present in the SM (B). In such a case, it
is typically |B|2 + 2ℜ(SB ⋆ ) which is kept at the lowest order in 1/Λ (with Λ being
the cutoff scale). Finally, this functionality is needed in order to study the largeNc expansion in multi-parton amplitudes, where beyond the leading 1/Nc terms the
positive definiteness of the integrand is not guaranteed.

## PDF page 12

– 10 –

JHEP07(2014)079

based on the contraction of Lorentz indices. As the name implies, helicity amplitudes
are computed with the polarizations of the external particles fixed. Then, by employing
colour decompositions [114–116], they can be organised into gauge-invariant subsets (often
called dual amplitudes), each corresponding to an element of a colour basis. In this way,
the complexity of the calculation grows linearly with the number of diagrams instead of
quadratically; furthermore, the colour matrix that appears in the squared amplitude can
be easily computed automatically (to any order in 1/Nc ) once and for all, and then stored
in memory. If the number of QCD partons entering the scattering process is not too large
(say, up to five or six), this procedure is manageable notwidthstanding the fact that the
number of Feynman diagrams might grow factorially. Otherwise, other techniques that
go beyond the Feynman-diagram expansion have to be employed [45, 49, 52, 117]. The
algorithm used in MadGraph5 aMC@NLO for the determination of the Feynman diagrams
has been described in detail in ref. [38]. There, it has been shown that it is possible to
efficiently “factorise” diagrams, such that if a particular substructure shows up in several
of them, it only needs to be calculated once, thus significantly increasing the speed of the
calculation. In addition, a not-yet-public version of the algorithm can determine directly
dual amplitudes by generating only the relevant Feynman diagrams, thereby reducing the
possible factorial growth to less than an exponential one.
The diagram-generation algorithm of MadGraph5 aMC@NLO is completely general,
though it needs as an input the Feynman rules corresponding to the Lagrangian of a given
theory. The information on such Feynman rules is typically provided by FeynRules, in a
dedicated format (UFO). We remind the reader that FeynRules is a Mathematica-based
package that, given a theory in the form of a list of fields, parameters and a Lagrangian, returns the associated Feynman rules in a form suitable for matrix element generators. It now
supports renormalisable as well as non-renormalisable theories, two-component fermions,
spin-3/2 and spin-2 fields, superspace notation and calculations, automatic mass diagonalization and the UFO interface. In turn, a UFO model is a standalone Python module, that
features self-contained definitions for all classes which represent particles, parameters, and
so forth. With the information from the UFO, the dedicated routines that will actually perform the computation of the elementary blocks that enter helicity amplitudes are built by
ALOHA. Amplitudes are then constructed by initializing a set of external wavefunctions,
given their helicities and momenta. The wavefunctions are next combined, according to the
interactions present in the Lagrangian, to form currents attached to the internal lines. Once
all of the currents are determined, they are combined to calculate the complex number that
corresponds to the amplitude for the diagram under consideration. Amplitudes associated
with different diagrams are then added (as complex numbers), and squared by making use
of the colour matrix calculated previously, so as to give the final result. We point out
that versions of MadGraph earlier than MadGraph5 used the HELAS [91, 118] library
instead of ALOHA. By adopting the latter, a significant number of limitations inherent to
the former could be lifted. A few examples follow here. ALOHA is not forced to deal with
pre-coded Lorentz structures; although its current implementation of the Lorentz algebra
assumes four space-time dimensions, this could be trivially generalised to any even integer,
as the algebra is symbolic and its actual representation enters only at the final stage of the

## PDF page 13

2.3.2

Width calculator

Among the basic ingredients for Monte Carlo simulations of new-physics models are the
masses and widths of unstable particles; which particle is stable and which unstable may
depend on the particular parameter benchmark chosen. Masses are typically obtained by
going to the mass eigenbasis and, if necessary, by evolving boundary conditions from a large
scale down to the EW one. Very general codes exist that perform these operations starting
from a FeynRules model, such as AsperGe [89]. The determination of the corresponding
widths, on the other hand, requires the explicit calculation of all possible decay channels
into lighter (SM or BSM) states. The higher the number of the latter, the more daunting
it is to accomplish this task by hand. Furthermore, depending on the mass hierarchy
and interactions among the particles, the computation of two-body decay rates could be
insufficient, as higher-multiplicity decays might be the dominant modes for some of the
particles. The decay channels that are kinematically allowed are highly dependent on the
mass spectrum of the model, so that the decay rates need to be re-evaluated for every choice
of the input parameters. The program MadWidth [106] has been introduced in order to
address the above issues. In particular, MadWidth is able to compute partial widths for
N -body decays, with arbitrary values of N , at the tree-level and by working in the narrowwidth approximation.6 The core of MadWidth is based on new routines for diagram
generation that have been specifically designed to remove certain classes of diagrams:
• Diagrams with on-shell intermediate particles. If the kinematics of an A → nparticles decay allows an internal particle B, that appears in an s-channel, to be
on shell, the corresponding diagram can be seen as a cascade of two decays, A →
B+(n−k)-particles followed by B → k-particles. It is thus already taken into account
in the calculation of lower-multiplicity decay channels, and the diagram is discarded.
6

Even if those two assumptions are quite generic, there are particles for which they do not give
sufficiently-accurate results, such as the Standard Model Higgs, which has significant loop-induced decay
modes.

– 11 –

JHEP07(2014)079

output writing; its flexibility has allowed the implementation of the complex mass scheme
(see section 2.2.1), and of generic UV and R2 computations (see section 2.4.2); it includes
features needed to run on GPU’s, and the analogues of the Heget [119, 120] libraries
can be automatically generated for any BSM model; finally, it caters to matrix-element
generators other than MadGraph, such as those now used in Herwig++ [121, 122] and
Pythia8 [123]. Since its release in 2011 [92], several important improvements have been
made in ALOHA. On top of the support to the complex mass scheme and to the Feynman
gauge, and of specific features relevant to one-loop computations (which are discussed in
sects. 2.2.1 and 2.4.2), we would like to mention here that there has been a conspicuous gain
in speed, both at the routine-generation phase as well as in the actual evaluation, thanks
to the extensive use of caching. In addition, the user is now allowed to define the form of
a propagator (which is not provided by FeynRules), while previously this was determined
by the particle spin: non-trivial forms, such as those relevant to spin-2 particles in ADD
models [124], or to unparticles, can now be used.

## PDF page 14

• Radiative diagrams. Roughly speaking, if one or more zero-mass particles are
radiated by another particle, the diagram is considered to be a radiative correction
to a lower-multiplicity decay — the interested reader can find the precise definition
in ref. [106]. Such a diagram is therefore discarded, because it should be considered
only in the context of a higher-order calculation. Furthermore, all diagrams with the
same coupling-constant combination and the same external states are also discarded,
so that gauge invariance is preserved.

2.3.3

Event reweighting

The generation of large samples of events for experimental analyses can be a very timeconsuming operation, especially if it involves a full simulation of the detector response.
It is therefore convenient, whenever possible, to apply corrections, or to study systematics of theoretical or modelling nature, by using reweighting techniques. The reweighting
of either one-dimensional distributions or that performed on a event-by-event basis are
equally-common practices in experimental physics. Although the basic idea (that a nonnull function can be used to map any other function defined in the same domain) behind
these two procedures is the same, one must bear in mind that they are not identical, and
in particular that the former can never be proven to be formally correct, since correlations
(with other, non-reweighted variables) may be lost or modified, while the latter is correct
in general, at least in the limit of a large number of events. For this reason, we consider
only event-by-event reweighting approaches in what follows.
7

Both of these conditions can be controlled by the user.

– 12 –

JHEP07(2014)079

MadWidth begins by generating all two-body decay diagrams, and then iteratively adds
extra final state particles with the condition that any diagram belonging to either of the
classes above is forbidden. This iterative procedure stops when all N = 4 modes have
been considered, or estimated to be numerically irrelevant.7 All diagrams thus generated
are integrated numerically. MadWidth uses several methods to reduce significantly the
overall computation time. Firstly, it features two fast (and conservative) estimators, one
for guessing the impact of adding one extra final-state particle before the actual diagramgeneration phase, and another one for evaluating the importance of a single integration
channel. Both of these estimators are used to neglect parts of the computation which are
numerically irrelevant. Secondly, if the model is compatible with the recent UFO extension
of ref. [106], and thus includes the analytical formulae for two-body decays, then the code
automatically uses those formulae and avoids the corresponding numerical integrations.
We conclude this section by remarking that, although essential for performing BSM
cross-section computations, MadWidth should be seen as a complement for the existing
tools that generate models. This is because the information it provides one with must
be available before the integration of the matrix elements is carried out but, at the same
time, really cannot be included in a model itself, since it depends on the chosen benchmark scenario. For more details on the use of this model-complementing feature in MadGraph5 aMC@NLO, and of its mass-matrix diagonalisation analogue to which we have
alluded above, see the Setup part of appendix B.1.

## PDF page 15

Thanks to its flexibility and the possibility of accessing a large amount of information
in a direct and straightforward manner (model and running parameters, matrix elements,
PDFs, and so forth) MadGraph5 aMC@NLO provides one with an ideal framework for
the implementation of such approaches. The strategy is rather simple: one starts with a
set of hard events, such as those contained in an LHE file, and rescales their weights:
wnew = r wold

(2.1)

r=

finew (x1 , µnew
)fjnew (x2 , µnew
)
)αSb (µnew
F
R
F
old (x , µold ) αb (µold )
fiold (x1 , µold
2 F
F )fj
S
R

.

(2.2)

It should be stressed that, although scale and PDF systematics can also be computed with
reweighting techniques at the NLO (see ref. [125]), in general they cannot be written in the
very simple form of eq. (2.1), which is that of an overall rescaling. For a direct comparison
of the NLO and LO techniques employed in this context by MadGraph5 aMC@NLO, and
for fuller details about them, see appendices B.3 and B.4 respectively.
Another rather simple example is that of the case where one is interested in studying
the implications of changing the modelling of a process, with the sole constraint that its
initial and final states be the same. Such a situation can for example occur when the
numerical values of the coupling constants are modified, or when the contributions of
classes of diagrams are included or eliminated (e.g., Higgs exchange in EW vector boson
scattering). The common feature of all examples of this kind is that they are associated
8

There may be cases where such matrix elements do not factorise a single αS factor — see e.g. section 2.4.
We limit ourselves to discussing the simplest, and more common, situation here.

– 13 –

JHEP07(2014)079

without modifying their kinematics. The rescaling factor r is not a constant, and may
change on an event-by-event basis. This implies that, even when the original sample of
events is unweighted (i.e., the wold ’s are all equal), the reweighted one will be in general
weighted (i.e., the wnew ’s may be different), and therefore degraded from a statistical point
of view. If, however, the spread of the new weights is not too large (i.e., the r’s are
close to each other, and feature a small number of outliers), the reweigthing is typically
advantageous with respect to generating a new independent sample from scratch.
While eq. (2.1) is completely general, its practical implementation depends on the kind
of problems one wants to solve. We shall consider three of them in this section, two of
which constitute a direct application of the basic formula (2.1), and a third one which
is more sophisticated. Since these procedures address different types of physics, they are
conveniently associated with different modules in MadGraph5 aMC@NLO, but they are
all fully embedded into our framework and easily accessible through it, as we shall briefly
explain in what follows and in appendices B.4 and B.5.
The simplest example is that of the evaluation of the uncertainties through to the
variations of the renormalisation and factorisation scales, and of the PDFs. In such a case
r is easily determined by using the identities i and j of the initial-state partons, and the
power (b) of αS in the Born matrix elements:8

## PDF page 16

with changes to matrix elements, all computed with the same kinematic configuration.
Therefore, one can simply write:
r = |Anew |2 /|Aold |2 ,

(2.3)

P (q|α) =

V
|Aα (q)|2 ,
σ̂α

(2.4)

with V a suitable volume factor, and σ̂α the total rate associated with the given assumptions α. The advantage of eq. (2.4) is that it is suitable to handle cases which are much
more complicated than the purely-theoretical exercise of eq. (2.3), which has led to its introduction here. For example, in the first approximation one may think of q as the actual
kinematic configuration measured by an experiment, whose accuracy is such that it can
be directly used as an argument of the matrix elements, as is done in eq. (2.4). Note that
this is a rather strong assumption, that in practice identifies hadron-level with parton-level
quantities, and assumes that the knowledge of the final state is complete (such as that which
one can ideally obtain in Drell-Yan production, pp → Z → ℓ+ ℓ− ). It is clear that there are
many ways in which this simple approximation (which is used, for example, in refs. [131–
135]) can break down: the effects of radiation, of the imperfect knowledge of the detector,
of the impossibility of a strict identification of parton- with hadron-level quantities, the
uncertainties that plague the latter, the fact that all the relevant four-momenta cannot
in general be measured, are but a few examples. It is therefore necessary to generalise
eq. (2.4), which one can do as follows:
∫
1
P (q|α) =
dx1 dx2 dφ(p)f (1) (x1 )f (2) (x2 ) |Aα (p)|2 W (q, p) .
(2.5)
σα
In eq. (2.5), we have denoted by p the parton kinematic configuration. All effects that
may turn p into the detector-level quantity q (whose dimensionality therefore need not

– 14 –

JHEP07(2014)079

which for obvious reasons is dubbed matrix-element reweighting. Despite its simplicity,
this method has very many different applications, from parameter scanning in new-physics
models (where one starts with a single sample of events, that corresponds to a given benchmark point, and generates as many new ones as the number of parameter configurations of
interest), to more advanced approaches, such as the inclusion of exact loop effects (Anew )
in processes that can be also, and more simply, described by effective theories (Aold ) —
see refs. [126, 127] for recent results of the latter type that make use of MadGraph5 and
MadGraph5 aMC@NLO. Some further comments on matrix-element reweighting and its
practical usage in MadGraph5 aMC@NLO are given in appendix B.5.
We finally turn to discussing the matrix-element method [128–130], which can be seen
as a reweighting one because the weights determined at the parton level through matrixelement computations are possibly modified by a convolution to take into account a variety
of blurring effects (such as those due to a detector). On the other hand, from the practical
point of view it turns out to be more convenient, rather than talking about reweighting
factors, to introduce a likelihood P (q|α) for the observation of a given kinematic configuration (q) given a set of theoretical assumptions (α). By doing so, one can just re-express
eq. (2.3) in a different language:

## PDF page 17

2.3.4

Tree-level merging

The goal of merging is that of combining samples associated with different parton multiplicities in a consistent manner, that avoids double counting after showering, thus allowing
one to effectively define a single fully-inclusive sample. The tree-level merging algorithms
implemented in MadGraph5 aMC@NLO are a hybrid version of those available in Alpgen [45] and SHERPA [140]; they work for both SM and BSM hard processes, but are
fully automated only when the shower phase is performed with either Pythia6 [141] or
Pythia8 [123] (however, there are no reasons in principle which prevents these schemes
from working with HERWIG6 [142, 143] or Herwig++ [121, 122]). They are based on the
use of a kT -measure [144] to define hardness and to separate processes of different multiplicities, and do not perform any analytic-Sudakov reweighting of events; rather, this operation
is effectively achieved by rejecting showered events under certain conditions (see later),
which implies a direct use of the well-tuned showering and hadronization mechanisms of
the parton shower Monte Carlos.
There are two merging schemes that can be used in conjunction with Pythia6 and
Pythia8; in the case of the latter, one is also given the possibility of considering CKKWL approaches [145–147] (after having generated the samples relevant to various parton
multiplicities with MadGraph5 aMC@NLO); in what follows, we shall limit ourselves to
briefly describe the former two methods. Firstly, one has the kT -jet MLM scheme [148],
where final-state partons at the matrix-element level are clustered according to a kT jet
algorithm to find the “equivalent parton shower history” of the event. In our implementation the Feynman diagram information from MadGraph5 aMC@NLO is used to retain
only those clusterings that correspond to actual Feynman diagrams. In order to mimic the
behaviour of the parton shower, the kT value for each clustering vertex associated with a
QCD branching is used as the renormalisation scale for αS in that vertex. All factorisation

– 15 –

JHEP07(2014)079

coincide with that of p) are parametrised by W (q, p), called transfer function. As for any
hadron-collision measurable quantity, eq. (2.5) features the convolution with the PDFs.
The likelihood introduced in this way can be used in the context e.g. of an hypothesis test
in order to determine which among various choices of α is the most probable.
Although this method is both conceptually simple and very attractive, the numerical evaluation of P (q|α) is difficult because the transfer function W (q, p) behaves in a
way which cannot be probed efficiently by phase-space parametrisations that work well
for just the matrix elements. In order to address this issue, a dedicated program, dubbed
MadWeight [136], has been introduced that includes an optimised phase-space treatment
specifically designed for eq. (2.5). The new version of the code [137] embedded in MadGraph5 aMC@NLO features several improvements w.r.t. that of ref. [136]. It includes the
method for the approximate description of higher-order effects due to initial-state radiation, as proposed in ref. [138]. Furthermore, several optimizations have been achieved that
render the computations much faster (sometimes by orders of magnitude); this allows one
to use this approach also in the case of very involved final states, such as those relevant to
Higgs production in association with a tt̄ pair [139]. Further details on MadWeight and
its use within MadGraph5 aMC@NLO can be found in appendix B.5.

## PDF page 18

2.4

NLO computations

When discussing the problem of perturbative corrections, one should bear in mind that one
usually considers an expansion in terms of a single quantity (which is a coupling constant
for fixed-order computations). However, this is just a particular case of the more general
scenario in which that expansion is carried out simultaneously in two or more couplings,
all of which are thus treated as “small” parameters — we shall refer to such a scenario
as mixed-coupling expansion. Despite the fact that there is typically a clear numerical
hierarchy among these couplings, a mixed-coupling situation is far from being academic;
in fact, as we shall show in the following, there are cases when one is obliged to work with
it. In order to study a generic mixed-coupling expansion without being too abstract, let
us consider an observable Σ which receives contributions from processes that stem from
both QCD and QED interactions. The specific nature of the interactions is in fact not
particularly relevant (for example, QED here may be a keyword that also understands the

– 16 –

JHEP07(2014)079

scales squared, and the renormalisation scale squared for the hard process (the process with
the zero-extra-parton multiplicity), are constructed by clustering back to the irreducible
2 → 2 system and by using the transverse mass in the resulting frame: µ2 = p2T + m2 . The
smallest kT value found in the jet-reconstruction procedure is restricted to be larger than
some minimum cutoff scale, which we denote by QME
cut ; if this condition is not satisfied,
the event is rejected. The hard events are then showered by Pythia: at the end of the
perturbative-shower phase, final-state partons are clustered into jets, using the very same kT
jet algorithm as before, with the jets required to have a transverse momentum larger than a
given scale Qmatch , with Qmatch > QME
cut . The resulting jets are compared to the partons at
the hard subprocess level (i.e., those that result from the matrix-element computations): a
jet j is said to be matched to a parton p if the distance between the two, defined according
to ref. [144], is smaller than the minimal jet hardness: kT (j, p) < Qmatch . The event is then
rejected unless each jet is matched to a parton, except in the case of the largest-multiplicity
sample, where extra jets are allowed if softer than the kT of the softest matrix-element parton in the event, QME
softest . Secondly, and with the aim to give one a non-parametric way
to study merging systematics, one has the shower-kT scheme, which can be used only with
Pythia’s pT -ordered shower. In this case, events are generated by MadGraph5 aMC@NLO
as described above and then showered, but information is also retained on the hardest
(which is also the first, in view of the pT -ordered nature of Pythia here) emission in the
ME
shower, QPS
hardest ; furthermore, one sets Qmatch = Qcut , which cannot be done in the context of the kT -jet MLM scheme. For all samples but the largest-multiplicity one, events are
rejected if QPS
hardest > Qmatch , while in the case of the largest-multiplicity sample events are
ME
rejected when QPS
hardest > Qsoftest . This merging scheme is simpler than the kT -jet MLM one,
but it rather effectively mimics it. Furthermore, it probes the Sudakov form factors used
in the shower in a more direct manner. Finally, the treatment of the largest-multiplicity
sample is fairly close to that used in the CKKW-inspired merging schemes. In both the
kT -jet MLM and shower-kT methods, merging systematics are associated with variations
of Qmatch ; in the former case, changes to Qmatch must be done by keeping Qmatch − QME
cut a
constant. For applications of the two schemes described here, see e.g. refs. [126, 148–151].

## PDF page 19

pure-EW contributions); what matters, for the sake of the present discussion, is that Σ
may depend on more than one coupling constant. We assume that the regular function
Σ(αS , α)

(2.6)

admits a Taylor representation:
Σ(αS , α) =

[
]
∞ ∑
∞
∑
αn αm ∂ n+m Σ
S

n=0 m=0

n!m!

∂ n αS ∂ m α (αS ,α)=(0,0)

,

(2.7)

l = n − m,

k = n + m,

(2.8)

whence:
]
(k+l)/2 (k−l)/2 [
α
Pk,l αS
∂kΣ
Σ(αS , α) =
,
((k + l)/2)!((k − l)/2)! ∂ (k+l)/2 αS ∂ (k−l)/2 α (αS ,α)=(0,0)
k=0 l=−k
k
∞ ∑
∑

where

(2.9)

(
)
Pk,l = δ mod(k, 2), mod(l, 2) ,

(2.10)

− k ≤ lm (k) ≤ lM (k) ≤ k ,

(2.11)

which enforces the sum over l to run only over those integers whose parity is the same as
that of k (therefore, there are k + 1 terms in each sum over l for a given k). Equation (2.9)
implies that we need to call Born the sum (over l) of all the contributions with the smallest
k ≡ k0 which are non-vanishing. Hence, the NLO corrections will correspond to the sum
over l of all terms with k = k0 + 1. This notation is compatible with the usual one used in
the context of the perturbation theory of a single coupling: the QCD- or QED-only cases are
recovered by considering l = k or l = −k respectively. In a completely general case, for any
given k there will exist two integers lm (k) and lM (k) which satisfy the following conditions:

and such that all contributions to eq. (2.9) with
l < lm (k)

or

l > lM (k)

(2.12)

vanish, and l = lm (k), l = lM (k) are both non-vanishing. This implies that in the range
lm (k) ≤ l ≤ lM (k) ,

– 17 –

(2.13)

JHEP07(2014)079

which is by definition the perturbative expansion of Σ. The first few terms of the sums in
eq. (2.7) will be equal to zero, with the number of such vanishing terms increasing with the
complexity of the process under consideration — this is because n and m are directly related
to the number of vertices that enter a given diagram. In general, it is clear that for a given
pair (n, m) which gives a non-vanishing contribution to eq. (2.7), there may exist another
pair (n′ , m′ ), with n ̸= n′ , m ̸= m′ , and n + m = n′ + m′ whose contribution to eq. (2.7) is
also non zero. It appears therefore convenient to rewrite eq. (2.7) with a change of variables:

## PDF page 20

there will be at least one (two if lm (k) ̸= lM (k)) non-null contribution(s) to eq. (2.9) (the
typical situation being actually that where all the terms in eq. (2.13) are non-vanishing).
Given eq. (2.13), one can re-write eq. (2.9) in the following way:
Σ(αS , α) =

∞
∑

∆(k)
cs (k) c(k)

αS

α

∑

∆(k)−q q

Σk,q αS

α ,

(2.14)

q=0

k=k0

where
1
(k + lm (k)) ,
2
1
c(k) = (k − lM (k)) ,
2
1
∆(k) = (lM (k) − lm (k)) .
2

(2.15)

cs (k) =

(2.17)

The coefficients Σk,l of eq. (2.14) can be expressed in terms of the quantities that appear
in eq. (2.9), but this is unimportant here. A typical situation is where:
lM (k + 1) = lM (k) + 1 ,

(2.18)

lm (k + 1) = lm (k) − 1 ,

(2.19)

cs (k + 1) = cs (k) ,

(2.20)

c(k + 1) = c(k) ,

(2.21)

∆(k + 1) = ∆(k) + 1 ,

(2.22)

so that:

whence:
cs (k0 ) c(k0 )

Σ(αS , α) = αS

α

∞ ∆(k
0 )+p
∑
∑
p=0

∆(k0 )+p−q q

Σk0 +p,q αS

α ,

(2.23)

q=0

where the Born and NLO contributions correspond to p = 0 and p = 1 respectively. Note
that eq. (2.23) is the most general form of the observable Σ(αS , α) if one allows the possibility of having Σk0 +p,0 = 0 or Σk0 +p,∆(k0 )+p = 0 (or both) for p > k0 , since this renders
eqs. (2.18) and (2.19) always true. Equation (2.23) has the advantage of a straightforward
interpretation of the role of NLO corrections.
An example may help make the points above more explicit. Consider the contribution
to dijet production due to the partonic process uu → uu; the corresponding lowest-order
t- and u-channel Feynman diagrams feature the exchange of either a gluon or a photon (or
a Z, but we stick to the pure-U(1) theory here). The Born matrix elements will therefore
be the sum of terms that factorise the following coupling combinations:
αS2 ,

αS α ,

α2 ,

(2.24)

which implies k0 = 2, ∆(2) = 2, and cs (2) = c(2) = 0. Therefore, according to eq. (2.23),
the NLO contribution p = 1 will feature the following coupling combinations:
αS3 ,

αS2 α ,

αS α 2 ,

– 18 –

α3 .

(2.25)

JHEP07(2014)079

(2.16)

## PDF page 21

α 2s

α 2s α

α 3s

α2

αsα

αsα2

α3

Figure 1. QCD (blue, right-to-left arrows) corrections and QED (red, left-to-right arrows) corrections to dijet production. See the text for details.

αSn αm

QCD

αSn+1 αm ,

(2.26)

αSn αm

QED

αSn αm+1 ,

(2.27)

−→

−→

which has an immediate graphic interpretation, depicted in figure 1. Such an interpretation
has a Feynman-diagram counterpart in the case of real-emission contributions, which is
made explicit once one considers cut-diagrams, like those presented in figure 2. Loosely
speaking, one can indeed identify the diagram on the left of that figure as representing QED
(since the photon is cut) real-emission corrections to the αS2 Born contribution. On the
other hand, the diagram on the right represents QCD (since the gluon is cut) real-emission
corrections to the αS α Born contribution. This immediately shows that, in spite of being
useful in a technical sense, QCD and QED corrections are not physically meaningful if
taken separately: in general, one must consider them both in order to arrive at a sensible,
NLO-corrected result. This corresponds to the fact that a given coupling combination in
the bottom row of figure 1 can be reached by means of two different arrows when starting
from the top row (i.e., the Born level). Therefore, figure 1 also immediately shows that
when one considers only the Born term associated with the highest power of αS (α), then
QCD-only (QED-only) corrections are sensible (because only a right-to-left or left-to-right
arrow is relevant, respectively): they coincide with the NLO corrections as defined above
(see the paragraph after eq. (2.10)). It also should be clear that the above arguments have a
general validity, whatever the values of cs (k0 ), c(k0 ), and ∆(k0 ) in eq. (2.23) — the former
two quantities never play a role in the analogues of figure 1, while by increasing ∆(k0 )
one simply inserts more blobs (i.e., coupling combinations) in both of the rows of figure 1.
Finally, note that reading eqs. (2.26) and (2.27) in terms of diagrams, as has been done
for those of figure 2, becomes much harder when one considers virtual contributions. For
example, the one whose O(αS2 α) cut-diagram is shown in figure 3 (and its analogues) can
indeed be equally well interpreted as a QED loop correction to a QCD×QCD O(αS2 ) Born
cut-diagram, or as a QCD loop correction to a QCD×QED O(αS α) Born cut-diagram.
MadGraph5 aMC@NLO has been constructed by having eq. (2.23) in mind; although
the majority of the relevant features are not yet available in the public version of the code,

– 19 –

JHEP07(2014)079

From the procedural point of view, it is convenient to identify QCD and QED corrections
according to the relationship between one coupling combination in eq. (2.24) and one in
eq. (2.25), as follows:

## PDF page 22

Figure 3. Virtual contribution to dijet production at the NLO and O(αS2 α). The saw-shaped line
represents a Cutkosky cut.

all of them have already been thoroughly tested in the module responsible for computing
one-loop matrix elements (see sects. 2.4.2 and 4.3), which is by far the hardest from this
point of view, and the checks on the real-emission part are also at quite an advanced
stage. The basic idea is that of giving the user the choice of which coupling combinations
to retain either at the Born or at the NLO level; this corresponds to choosing a set of
blobs in the upper or lower row of figure 1, respectively. MadGraph5 aMC@NLO will
then automatically also consider the blobs in the row not involved in the selection by the
user, in order to construct a physically-meaningful cross section, compatible with both
the user’s choices, and the constraints due to a mixed-coupling expansion (the arrows in
figure 1). It should be stressed that, although the results for the coefficients Σk0 +p,q can be
handled separately by MadGraph5 aMC@NLO, such coefficients are not (all) independent
from each other from a computational viewpoint, because a single Feynman diagram (an
amplitude-level quantity) may contribute to several Σk0 +p,q ’s (the latter being amplitudesquared quantities). For this reason, as far as the CPU load is concerned the choice of which

– 20 –

JHEP07(2014)079

Figure 2. Real-emission contributions to dijet production at the NLO and O(αS2 α). The sawshaped lines represent Cutkosky cuts.

## PDF page 23

coupling combinations to consider can be equivalently made at the amplitude level. Indeed,
this is the only option presently available in the public version of MadGraph5 aMC@NLO;
more detailed explanations are given in appendix B.1.
2.4.1

NLO cross sections and FKS subtraction: MadFKS

r = (I1 , . . . In+2 ) ∈ Rn .

(2.28)

The first operation performed by MadGraph5 aMC@NLO is that of constructing Rn , given
the process and the theory model. For example, if one is interested in the hadroproduction
of a W + Z pair in association with a light jet
pp −→ W + Zj

(2.29)

as described by the SM, MadGraph5 aMC@NLO will obtain:
R3 =

{(
)
(
)
}
¯ W + , Z, g , . . . u, g, W + , Z, d , . . . .
u, d,

(2.30)

Since the processes in Rn are tree-level, MadGraph5 aMC@NLO will construct them very
efficiently using the dedicated algorithms (see section 2.3.1). Beyond the Born level, an
NLO cross section receives contributions from the one-loop and real-emission matrix elements. As is well known, the set of the former subprocesses coincides9 with that of the
Born, Rn . Real-emission processes are by nature tree-level, and can therefore be obtained
by using the very same algorithms as those employed to generate the Born contributions.
This is achieved by making the code generate all tree-level processes that have the same
final-state as the Born’s, plus one light jet — using the example of eq. (2.29), these would
correspond to:
pp −→ W + Zjj .
(2.31)
Such was the strategy adopted in the original MadFKS implementation [61]. There is
however an alternative procedure, which we have implemented in MadGraph5 aMC@NLO
because it is more efficient than the previous one in a variety of ways. Namely, for any
given r0 ∈ Rn , one considers all possible a → bc branchings for each non-identical a ∈ r0
with a strongly-interacting (i.e., g → gg, g → q q̄, and q → qg, but also Q → Qg, with
Q a quark with non-zero mass). For each of these branchings, a new list is obtained
9

This is because we are considering here only those cases where one-loop matrix elements are obtained
by multiplying the one-loop amplitudes times the Born ones. Loop-induced processes, in which the LO
contribution is a one-loop amplitude squared, are not to be treated as part of an NLO computation.

– 21 –

JHEP07(2014)079

In this section, we briefly review the FKS subtraction [10, 12] procedure, and emphasise the
novelties of its implementation in MadGraph5 aMC@NLO w.r.t. its previous automation
in MadFKS [61], the dedicated module included in aMC@NLO.
We shall denote by n the number of final-state particles relevant to the Born contributions to a given cross section. The set of all the partonic 2 → n subprocesses that
correspond to these contributions will be denoted by Rn ; each of these subprocesses can
be represented by the ordered list of the identities of its 2 + n partons, thus:

## PDF page 24

∑
j

Sij (r) −→ 1

Sij (r) −→ 1

i, j collinear ,

(2.32)

i soft ,

(2.33)

all other IR limits ,

(2.34)

(i,j)∈PFKS (r)

∑

Sij (r) −→ 0

Sij (r) = 1 .

(2.35)

(i,j)∈PFKS (r)

One exploits eq. (2.35) by rewriting the real matrix elements as follows:
∑
∑
(n+1,0)
Mij
.
Sij (r)M(n+1,0) (r) ≡
M(n+1,0) (r) =

(2.36)

(i,j)∈PFKS (r)

(i,j)∈PFKS (r)

(n+1,0)

has the very simple singularity structure mentioned
Thanks to eqs. (2.32)–(2.34), Mij
above. Furthermore, the terms in the sum on the r.h.s. of eq. (2.36) are independent of
each other, and MadGraph5 aMC@NLO is thus able to handle them in parallel.
The FKS method exploits the fact that phase-space sectors associated with different Sij
functions are independent of each other by choosing different phase-space parametrisations
in each of them. There is ample freedom in such a choice, bar for two integration variables:
the rescaled energy of parton i (denoted by ξi ), and the cosine of the angle between partons
i and j (denoted by yij ), both defined in the incoming-parton c.m. frame. The idea is that
these quantities are in one-to-one correspondence with the soft (ξi → 0) and collinear (yij →
1) singularities respectively, which renders it particularly simple to write the subtracted
cross section. The (n + 1)-body phase space is then written as follows:
)
(
(ij)
(n+1)
(ij)
(2.37)
dφn+1 = Φij
Kn+1 (χn+1 ) dχn+1 ,
(ij)

where χn+1 collectively denote the 3n − 1 independent integration variables, with
(ij)

{ξi , yij } ⊂ χn+1 ,
10

(2.38)

The exceedingly rare cases of non-singular real-emission contributions can be obtained by crossing; one
example is q q̄ → Hg, which is the crossed process of qg → Hq.

– 22 –

JHEP07(2014)079

by removing a from r0 , and by inserting the pair (b, c) in its place. By looping over r0
one thus constructs the set10 of real-emission processes Rn+1 . As a by-product, one also
naturally obtains, for each r ∈ Rn+1 , the pairs of particles which are associated with a
soft and/or a collinear singularity of the corresponding matrix element (which we denote
by M(n+1,0) (r)); by definition [61], these pairs form the set of FKS pairs, PFKS (r), which
is central in the FKS subtraction procedure. We point out, finally, that regardless of
the type of strategy adopted to construct Rn+1 and PFKS , it is immediate to apply it in
MadGraph5 aMC@NLO to theories other than QCD, such as QED.
After having obtained PFKS (r), MadGraph5 aMC@NLO constructs the S functions
that are used by FKS in order to achieve what is effectively a dynamic partition of the
phase space: in each sector of such a partition, the structure of the singularities of the
matrix elements is basically the simplest possible, amounting (at most) to one soft and one
collinear divergence. The properties of the S functions are:

## PDF page 25

and where
Kn+1 = {k3 , k4 , · · · kn+3 }

(2.39)

is the set of final-state momenta. Given eq. (2.38), MadGraph5 aMC@NLO chooses the
(n+1)
and the functional depenother 3n − 3 integration variables and thus determines Φij
(ij)

(E)

Kn+1 = {k3 , k4 , · · · kn+3 }

non special

(2.40)

MadGraph5 aMC@NLO constructs its soft, collinear, and soft-collinear limits with:
(S)

(E)

Kn+1 = Kn+1 (ξi = 0) ,

(2.41)

(E)
(C)
Kn+1 = Kn+1 (yij = 1) ,
(SC)
(E)
Kn+1 = Kn+1 (ξi = 0, yij = 1) .

(2.42)
(2.43)

Furthermore, all the phase-space parametrisations employed by MadGraph5 aMC@NLO
are such that:11
(SC)
(C)
(S)
(2.44)
Kn+1 = Kn+1 = Kn+1 ,
which is beneficial from the point of view of the numerical stability of observables computed
at the NLO, and is necessary in view of matching with the parton shower according to
the MC@NLO formalism. As is usual in the context of NLO computations, we call the
non-special and the IR-limit configurations (and, by extension, the corresponding crosssection contributions) the event and the soft, collinear, and soft-collinear counterevents
respectively.
Given a real-emission process rR ∈ Rn+1 and an Sij contribution, the FKS-subtracted
cross section consists of four terms:
{
}
(NLO,α)
(NLO)
(2.45)
dσij
(rR ) ←→ dσij
(rR )
α=E,S,C,SC
)
(
(α)
(ij)
(ij)
(ij)
(NLO,α)
dσij
(rR ) = L(α) rR ; χBj Wij (rR ) dχBj dχn+1 ,
(2.46)
(ij)

where dχBj is the integration measure over Bjorken x’s, L(α) is the corresponding parton(α)

luminosity factor,12 and the short-distance weights Wij
11

are reported in refs. [61, 125].

Equation (2.44) holds for all particles except the FKS-pair partons; for the latter, it is the sum of
their four-momenta that is the same in the three configurations. This is sufficient owing to the underlying
infrared-safety conditions.
12
Whose dependence on α is a consequence of eq. (2.44) when j = 1, 2 — see ref. [26] for more details.

– 23 –

JHEP07(2014)079

dence Kn+1 (χn+1 ) according to the form of the integrand, gathered from the underlying
Feynman diagrams. In general, this implies splitting the computation in several integration channels, which are independent of each other and can be dealt with in parallel. Such
multi-channel technique is irrelevant here, and will be understood in the following. More
details can be found in refs. [152, 153] and [61]. Implicit in eq. (2.37) are the maps that allow one to construct soft and collinear kinematic configurations starting from a non-special
configuration (i.e., one where no parton is soft, and no two partons are collinear). This we
shall denote as follows. Given:

## PDF page 26

In ref. [61], in particular, an extended proof is given that all contributions to an NLO
cross section which are not naturally (n + 1)-body ones (such as the Born, virtual, and
initial-state collinear remainders) can be cast in a form formally identical to that of the
soft or collinear counterterms, and can thus be dealt with simultaneously with the latter.
The fully differential cross section that emerges from eqs. (2.45) and (2.46) is:
(NLO)
dσij
(rR )

dK

(2.47)

where we have understood the complete integration over the measures on the r.h.s.. Mad(ij)
(ij)
Graph5 aMC@NLO scans the phase space by generating randomly {χBj , χn+1 }. For each
(E)

of these points, an event kinematic configuration Kn+1 and its weight, and a counterevent
(S)

kinematic configuration Kn+1 and its weight are given in output; with these, any number
of (IR-safe) observables can be constructed. As can be seen from eq. (2.47), the weight
associated with the single counterevent kinematics is the sum of the soft, collinear, softcollinear, Born, virtual, and initial-state collinear remainders contributions, which reduces
the probability of mis-binning and thus increases the numerical stability of the result.
In order for the results of eq. (2.47) to be physical, they must still be summed over
all processes rR ∈ Rn+1 and all FKS pairs (i, j) ∈ PFKS (rR ). As far as the latter sum is
concerned, it is easy to exploit the symmetries due to identical final-state particles, and
thus to arrive at the set [61]:
P FKS ⊆ PFKS ,

(2.48)

whose elements give non-identical contributions to the sum over FKS pairs. Therefore:
∑

∑

rR ∈Rn+1 (i,j)∈PFKS (rR )

(NLO)
dσij
(rR )

dK

=

∑

∑

rR ∈Rn+1 (i,j)∈P FKS (rR )

(n+1)

(NLO)

(n+1) dσij
ςij

dK

(rR )

,

(2.49)

with ςij
a suitable symmetry factor. The sum on the r.h.s. of eq. (2.49) is obviously more
convenient to perform than that on the l.h.s.; it is customary to include the symmetry factor
in the short-distance weights (see e.g. ref. [125]). The number of elements in P FKS (rR ) can
indeed be much smaller than that in PFKS (rR ). For example, when rR is a purely gluonic
process, we have #(P FKS (rR )) = 3 (i.e., independent of n), while #(PFKS (rR )) = (n+1)(n+
2). While the former figure typically increases when quarks are considered, it remains true
that, for asymptotically large n’s, #(P FKS ) is a constant while #(PFKS ) scales as n2 .
The sum on the r.h.s. of eq. (2.49) is what has been originally implemented in MadFKS.
It emphasises the role of the real-emission processes, which implies that for quantities which
are naturally Born-like (such as the Born matrix elements themselves) one needs to devise
a way to map unambiguously Rn onto Rn+1 . The interested reader can find the definition
of such a map in section 6.2 of ref. [61], which we summarise here using the Born cross

– 24 –

JHEP07(2014)079

(
) dσ (NLO,E) (rR )
ij
(ij)
(ij)
(E)
dχBj dχn+1
= δ K − Kn+1
(ij)
(ij)
dχBj dχn+1
(
) ∑ dσ (NLO,α) (rR )
ij
(S)
(ij)
(ij)
+δ K − Kn+1
dχBj dχn+1 ,
(ij)
(ij)
α=S,C,SC dχBj dχn+1

## PDF page 27

section dσ (LO) as an example:
∑

dσ (LO) (rR ) =

i\

(i,j)∈P FKS (rR )

δgIi Sij (ξi = 0)dσ (LO) (rR ) ,

(2.50)

where
rR = (I1 , . . . Ii , . . . Ij , . . . In+3 )

i\

rR = (I1 , . . . I\i , . . . Ij , . . . In+3 ) .

=⇒

(2.51)

rR ∈Rn+1 (i,j)∈P FKS (rR )

rB ∈Rn

Here we have defined:
dσ

(NLO,E)

(rB ) =

∑

∑

rR ∈Rn+1 (i,j)∈P FKS (rR )

(

j⊕i,i\

δ rB , rR

)

(n+1)

ςij

(NLO,E)
(rR ) dσij
(rR ) ,

(2.53)

where the generalised Kronecker symbol δ(. . .) is equal to one if its arguments are equal,
and to zero otherwise, and
j⊕i,i\

rR

= (I1 , . . . I\i , . . . Ij⊕i , . . . In+3 ) .

(2.54)

Although the first sum in eq. (2.53) might seem to involve a very large number of terms,
MadGraph5 aMC@NLO knows immediately which terms will give a non-zero contribution,
thanks to the procedure used to construct Rn+1 which was outlined at the beginning of
this section. On top of organising the sums over processes and FKS pairs in a different way
w.r.t. the first version of MadFKS, MadGraph5 aMC@NLO also performs some of these
(and, specifically, those in eq. (2.53)) using MC techniques (whereas all sums are performed
explicitly in ref. [61]). In particular, for any given rB ∈ Rn , one real-emission process and
one FKS pair are chosen randomly among those which contribute to eq. (2.53); these
choices are subject to importance sampling, and are thus adaptive. In summary, while the
procedure adopted originally in MadFKS takes a viewpoint from the real-emission level,
that adopted in MadGraph5 aMC@NLO emphasises the role of Born processes. The two
are fully equivalent, but the latter is more efficient in the cases of complicated processes,
and it offers some further advantages in the context of matching with parton showers.
2.4.2

One-loop matrix elements: MadLoop

Both MadGraph5 aMC@NLO and its predecessor aMC@NLO are capable of computing
the virtual contribution to an NLO cross section in a completely independent manner (while

– 25 –

JHEP07(2014)079

In other words, through the r.h.s. of eq. (2.50) one is able to define a Born-level quantity
as a function of a real-emission process. In MadGraph5 aMC@NLO we have followed the
opposite strategy, namely that of defining real-emission level quantities as functions of a
Born process. The proof that this can indeed be done is given in appendix E of ref. [61];
(NLO,E)
here, we limit ourselves to summarising it as follows, using the event contribution dσij
to the NLO cross section as an example. One has the identity:
∑
∑
∑
(n+1)
(NLO,E)
dσij
ςij
(rR ) =
dσ (NLO,E) (rB ) .
(2.52)

## PDF page 28

A. The adoption of the procedures introduced with MadGraph5, and in particular the
UFO/ALOHA chain for constructing amplitudes starting from a given model.
B. The possibility of switching between two reduction methods for one-loop integrals,
namely the Ossola-Papadopoulos-Pittau (OPP [18]) and the Tensor Integral Reduction (TIR [154, 155]) procedures.
C. The organization of the calculation in a way consistent with the mixed-coupling
expansion described in section 2.4, and in particular with eq. (2.23).
It should be clear that these capabilities induce an extremely significant broadening of the
scope of MadLoop (in particular, extending it beyond the SM). As a mere by-product,
they have also completely lifted the limitations affecting MadLoop4, which were described
in section 4 of ref. [68]. It is instructive to see explicitly how this has happened. Item A.
is responsible for lifting MadLoop4 limitation #1 (MadLoop4 cannot generate a process
whose Born contains a four-gluon vertex, because the corresponding R2 routines necessary
in the OPP reduction were never validated, owing to the technically-awkward procedure
for handling them in MadGraph4; this step is now completely bypassed thanks to the
UFO/ALOHA chain). Limitation #2 (MadLoop4 cannot compute some loops that feature
massive vector bosons, which is actually a limitation of CutTools [156], in turn due to
the use of the unitary gauge) is now simply absent because of the possibility of adopting
the Feynman gauge, thanks again to item A. Limitation #4 (MadLoop4 cannot handle
finite-width effects in loops) is removed thanks to the implementation of the complex
mass scheme, a consequence of item A. Finally, item C. lifts MadLoop4 limitation #3
(MadLoop4 cannot generate a process if different contributions to the Born amplitudes do
not factorise the same powers of all the relevant coupling constants).
The advances presented in items A.–C. above are underpinned by many technical
differences and improvements w.r.t. MadLoop4. Here, we limit ourselves to listing the
most significant ones:
13

Some of them are not yet public, but are fully tested.

– 26 –

JHEP07(2014)079

still allowing one to interface to a third-party one-loop provider if so desired), through a
module dubbed MadLoop [68]. However, there are very significant differences between
the MadLoop embedded in aMC@NLO (i.e., the one documented in ref. [68]), and the
MadLoop currently available in MadGraph5 aMC@NLO; hence, in order to avoid confusion between the two, we shall call the former MadLoop4, and the latter MadLoop5. The
aim of this section is that of reviewing the techniques for automated one-loop numerical
computations, and of giving the first public documentation of MadLoop5.
As the above naming scheme suggests, core functionalities relevant to the handling of
tree-level amplitudes were inherited from MadGraph4 in MadLoop4, while MadLoop5 uses
MadGraph5. This was a necessary improvement in view of the possibility of computing
virtual corrections in arbitrary renormalisable models (i.e., other than the SM). More in
general, one can identify the following three items as strategic capabilities, that were lacking
in MadLoop4, and that are now available in MadLoop5:13

## PDF page 29

• MadLoop5 is written in Python, the same language which was adopted for MadGraph5 (MadLoop4 was written in C++).
• The UV-renormalisation procedure has been improved and rendered fully general
(that of MadLoop4 had several hard-coded simplifying solutions, motivated by QCD).
• An extensive use is made of the optimisations proposed in ref. [24] (OpenLoops).
• The self-diagnostic numerical-stability tests, and the procedures for fixing
numerically-unstable loop-integral reductions, have been redesigned.

Generalities.
the quantity:

Given a 2 → n partonic process r (see eq. (2.28)), MadLoop computes
V (r) =

∑

colour
spin

{
}
⋆
2ℜ A(n,1) (r)A(n,0) (r) ,

(2.55)

with A(n,0) and A(n,1) being the relevant tree-level and UV-renormalised one-loop amplitudes respectively; the averages over initial-state colour and spin degrees of freedom are
understood. The result for V (r) is given as a set of three numbers, corresponding to the
residues of the double and single IR poles, and the finite part, all in the ’t Hooft-Veltman
scheme [157]. In the case of a mixed-coupling expansion, each of these three numbers is
replaced by a set of coefficients, in the form given by eq. (2.23). There may be processes
for which A(n,0) is identically equal to zero, and A(n,1) is finite; for these processes (called
loop-induced), MadLoop computes the quantity:
∣2
∑ ∣∣
∣
(2.56)
VLI (r) =
∣A(n,1) (r)∣ .
colour
spin

Only eq. (2.55) is relevant to NLO computations proper, and we shall mostly deal with it in
what follows. In the current version of MadGraph5 aMC@NLO, the loop-induced VLI (r)
cannot be automatically integrated (for want of an automated procedure for multi-channel
integration), and hence in this case the code output by MadLoop5 must be interfaced in an
ad-hoc way to any MC integrator (including MadGraph5 aMC@NLO — see e.g. ref. [127]
for a recent application).
The basic quantity which MadLoop needs to compute and eventually renormalise in
order to obtain A(n,1) that enters eq. (2.55) is the one-loop UV-unrenormalised amplitude:
∑
(n,1)
C,
(2.57)
=
AU
diagrams

where C denotes the contribution of a single Feynman diagram after loop integration, whose
possible colour, helicity, and Lorentz indices need not be specified here, and are understood;

– 27 –

JHEP07(2014)079

More details on these points will be given in what follows. Before turning to that, we shall
discuss the basic principles used by MadLoop5 for the automation of the computation of
one-loop integrals.

## PDF page 30

they will be re-instated later. A standard technique for the evaluation of C is a so-called
reduction procedure, pioneered by Passarino and Veltman [154], which can be written as
follows:
∑
ci (C)Ji(Red) + R(C) .
(2.58)
C = Red [C] =
i

(Red)

where d = 4 − 2ǫ, and we have assumed the diagram to have m propagators in the loop
and have defined:
D̄i = (ℓ̄ + pi )2 − m2i ,

0 ≤ i ≤ m − 1,

(2.60)

with mi the mass of the particle relevant to the ith loop propagator, and pi some linear
combination of external momenta. For any four-dimensional quantity x, its (4 − 2ǫ)dimensional counterpart is denoted by x̄, and its (−2ǫ)-dimensional one by x̃. The fact
that pi , rather than p̄i , enters eq. (2.60) is a consequence of the use of the ’t Hooft-Veltman
scheme. The loop momentum is decomposed as follows:
ℓ̄ = ℓ + ℓ̃

with

ℓ· ℓ̃ = 0 ,

(2.61)

with similar decompositions holding for the Dirac matrices γ̄ µ and metric tensor ḡ µν . One
can thus define [158] the purely four-dimensional part of the numerator that appears in
eq. (2.59):
(2.62)
N (ℓ) = lim N̄ (ℓ̄ = ℓ; γ̄ µ = γ µ , ḡ µν = g µν ) ,
ǫ→0

from whence one can obtain its (−2ǫ)-dimensional counterpart:
Ñ (ℓ, ℓ̃) = N̄ (ℓ̄) − N (ℓ) .

– 28 –

(2.63)

JHEP07(2014)079

The quantities Ji
are one-loop integrals, independent of C. The essence of any reduction
procedure is that it is an algebraic operation that determines the coefficients ci and R
(which are functions of external momenta and of masses, and some of which may be equal
to zero); the intricacies of loop integration are dealt once and for all in the computations
of the Ji(Red) ’s (which are much simpler than any C). As the leftmost equality in eq. (2.58)
indicates, from the operator point of view Red[ ] is the identity; its meaning is that of
replacing C with the linear combination in the rightmost member of eq. (2.58). As the
notation {Ji(Red) } suggests, different reduction procedures can possibly make use of different
sets of one-loop integrals.
Equation (2.58) is basically what one would do if one were to compute C in a nonautomated manner. In automated approaches, however, additional problems arise, for
example due to the necessity of relying on numerical methods, which have obvious difficulties in dealing with the non-integer dimensions needed in the context of dimensional
regularisation, and with the analytical information on the integrand of C, which is extensively used in non-automated reductions. In order to discuss how these issues can be
solved, let us write C in the following form:
∫
N̄ (ℓ̄)
C = dd ℓ̄ C̄(ℓ̄) ,
C̄(ℓ̄) = ∏m−1
,
(2.59)
D̄
i
i=0

## PDF page 31

The quantity defined in eq. (2.62), not involving non-integer dimensions, can be treated by
a computer with ordinary techniques. By using eq. (2.63) in eq. (2.59) one obtains:
C = Cnon−R2 + R2 ,
where
Cnon−R2 =
R2 =

∫

Ñ (ℓ, ℓ̃)
.
dd ℓ̄ ∏m−1
i=0 D̄i

(2.65)
(2.66)

Both integrals in eq. (2.65) and eq. (2.66) still depend on (4−2ǫ)-dimensional quantities, but
they do so in a way that allows one to further manipulate and cast them in a form suitable
for a fully numerical treatment. In particular, one can show [158] that the computation
of R2 is equivalent to that of a tree-level amplitude, constructed with a universal set of
theory-dependent rules (see ref. [159], refs. [160–162], and refs. [163–165] for the QCD,
QED+EW, and some BSM cases respectively), analogous to the Feynman ones and that
can be derived once and for all (for each model) by just considering the one-particleirreducible amplitudes with up to four external legs [166]. On the other hand, eq. (2.65)
is still potentially divergent in four dimensions. The details of how this is dealt with may
vary, but the common characteristic is that all of them are entirely defined by a reduction
procedure. In other words, we shall use the following identity:
C = Red [Cnon−R2 ] + R2 ,

(2.67)

which is a consequence of eqs. (2.58) and (2.64). The general idea is that all things that
are inherently (4 − 2ǫ)-dimensional in Red[Cnon−R2 ] can be parametrized in terms of the
one-loop integrals Ji(Red) , so that any piece of computation that would require an analytical
knowledge of the integrand and an analytical treatment of the (−2ǫ)-dimensional terms is
indeed treated analytically, but in a universal manner through Ji(Red) .
We emphasise that, although the decomposition of eq. (2.64) is inspired by the OPP
reduction method, it is universal, in the sense that the operator Red[ ] in eq. (2.67) does
not need to be OPP-inspired, and that the definition of R2 has nothing to do with the OPP
procedure as such, but rather with the interplay of (4−2ǫ)-dimensional quantities and their
four-dimensional counterparts. There are of course several alternative approaches, but the
majority of them do not lend themselves to the numerical computation of the rational
part R(Cnon−R2 ) + R2 . The two methods which have been used for complicated numerical
simulations are bootstrap [17] and D-dimensional unitarity [19, 20, 23]. However, they
also involve rather non-trivial issues, such as the presence of spurious singularities (for
bootstrap), or the necessity of performing additional computations in 6 and 8 dimensions
(for D-dimensional unitarity). The latter problem can be bypassed by means of a mass
shift [167], which however might imply additional complications in the case of axial couplings in massive theories. In summary, while it is true that there are advantages and
disadvantages in each of these approaches, we point out that R2 must not really be seen
as an extra issue in the context of a complete calculation, simply because one has to carry
out UV renormalisation anyhow, which is similar to R2 but more involved.

– 29 –

JHEP07(2014)079

∫

N (ℓ)
,
dd ℓ̄ ∏m−1
i=0 D̄i

(2.64)

## PDF page 32

b

for the Born amplitude. Here, h denotes a given helicity configuration, and b runs over all
(0)
possible single-colour factors. The quantity λb is one such colour factor, that collects all
the colour indices, which are understood. Hence, Bh,b is a scalar quantity which does not
contain any colour index. In the case of one-loop diagrams, we shall use a similar notation,
thus replacing the quantities that appear in eqs. (2.65) and (2.66) with:
N (ℓ) −→ λl Nh,l (ℓ) ,

(1)

(2.69)

D̄i −→ D̄i,l ,

(2.70)

R2 −→ R2,h,l .

(2.71)
(0)

(1)

The quantity λl in eq. (2.69) has the same meaning as λb in eq. (2.68), but is relevant
to one-loop amplitudes rather than tree-level ones, hence the different notation. Since
the index l unambiguously identifies a single-colour-structure subamplitude, and the latter
has a non-trivial kinematic dependence, different l’s may correspond to different one-loop
Feynman diagrams, and thus the necessity of inserting a dependence on l on the r.h.s. of
eq. (2.70). Finally, we did not factor out the colour structure in eq. (2.71), since this will
not be relevant in the following. We remark that decompositions such as those on the
r.h.s.’s of eqs. (2.68) and (2.69) are easily handled by MadGraph5 aMC@NLO, which has
inherited the treatment of the colour algebra from MadGraph5 (see section 2.3 of ref. [38]).
It should be stressed that such a treatment is symbolic and that, although introduced to
deal with tree-level quantities, is perfectly capable of computing one-loop ones such as
(1)
λl . Furthermore, the colour algebra is internally decomposed in terms of colour flows (for
which several different representations are available); although this information is presently
not used in the integral-reduction procedure, it will be trivial to exploit it in the future,
should this need arise. By using eqs. (2.68)–(2.71) one obtains:
(
)⋆
)(
∑ ∑ ∑ (1) ∫
∑ (0)
∑
N
(ℓ)
h,l
(n,1) (n,0) ⋆
λl
dd ℓ̄ ∏ml −1
AU A
=
λb Bh,b .
R2,h,l
+
i=0 D̄i,l
l
colour h
b
l
(2.72)
As was already mentioned, the R2 term gives rise to what is effectively a tree-level computation; therefore, we shall drop it in what follows, and just deal with:
∣
∑∑∑∫
Nh,l (ℓ)
(n,1) (n,0) ⋆ ∣
⋆
dd ℓ̄ ∏ml −1
AU A
=
Λlb Bh,b
,
(2.73)
∣
non−R2
i=0 D̄i,l
h
l
b
– 30 –

JHEP07(2014)079

Integral reduction in MadLoop. We now turn to discussing the way in which the
previous formulae are handled by MadLoop. In order to do so, we shall re-instate in the
notation the dependence of the amplitudes on the relevant quantities; in particular, we
work with scalar sub-amplitudes that have definite helicities (i.e., all Lorentz indices are
contracted away, and all Dirac matrices are sandwiched between spinors), and that factorise
a single colour factor. The latter condition implies that, in general, our sub-amplitudes are
not in one-to-one correspondence with Feynman diagrams (typically when these feature at
least a four-gluon vertex), but that they can be written as follows:
∑ (0)
(n,0)
λb Bh,b ,
(2.68)
Ah
=

## PDF page 33

Λlb =

∑

(1) (0) ⋆

λl λb

.

(2.74)

colour

The integral-reduction procedure of MadLoop4 [68] can be read directly from eq. (2.73),
and is as follows:
[∫
]
∣
∑∑∑
Nh,l (ℓ)
(n,1) (n,0) ⋆ ∣
d
⋆
Red
d ℓ̄ ∏ml −1
AU A
=
Λlb Bh,b
,
(2.75)
∣
non−R2
D̄
i,l
i=0
h
l
b

m∏
l −1
i=0

mp −1

D̄i,l =

∏

D̄i,p ,

i=0

∀ l, p ∈ t ,

t ∈ topologies .

(2.76)

By exploiting eq. (2.76), one can rewrite eq. (2.75) as follows:
]
[∫
∑ ∑ ∑
⋆
∣
∑
N
(ℓ)
Λ
B
h,l
lb
h
l∈t
b
h,b
(n,1) (n,0) ⋆ ∣
,
dd ℓ̄
Red
AU A
=
∣
∏mlt −1
non−R2
D̄i,lt
t
i=0

(2.77)

r∑
max

(2.78)

for any lt ∈ t. Eq. (2.77) is optimal from the viewpoint of reducing the number of calls to
Red[ ], and thus addresses the first of the issues mentioned before. As far as the second of
those issues is concerned, MadLoop5 makes a systematic use of the fact that any numerator
Nh,l (ℓ) admits the following representation:
Nh,l (ℓ) =

(r)

Cµ1 ...µr ;h,l ℓµ1 . . . ℓµr ,

r=0

where the coefficients C (r) are independent of the loop momentum; when r = 0, we understand that no Lorentz indices and no loop momenta appear on the r.h.s. of eq. (2.78).
The quantity rmax is the largest rank in Nh,l , and in the Feynman gauge in renormalisable

– 31 –

JHEP07(2014)079

where Red ≡ OPP, since in MadLoop4 only OPP reduction has been considered. Equation (2.75) is not particularly satisfactory from an efficiency point of view, for two reasons,
both of which have to do with the fact that the integral-reduction operation is quite timeconsuming. Firstly, the Red[ ] operator is called #h × #l number of times (we recall that,
by construction, #l is equal to or larger than the number of loop diagrams). Secondly, each
of these calls involves the recomputation of Nh,l (ℓ) a large number of times (determined
by the OPP procedure), but which involve only changing the numerical value of ℓ, without
affecting any other quantity entering it. The first issue is solved by reducing the number
of integral-reduction operations, while the second by rendering more efficient the computation of Nh,l (ℓ). The strategies adopted in MadLoop5 are the following. One begins by
observing that the operator Red[ ] acts on the “space” of one-loop integrals. Therefore,
Born amplitudes must be seen as c-numbers as far as this operator is concerned. One can
thus exploit the fact that Red[ ] is linear. Furthermore, what really drives integral reduction is the structure of the denominators (numerators are just numbers computed with
suitable values of ℓ, specific to the given Red[ ] operator). Hence, one can organize loop
integrals in sets of topologies, the latter being defined as subsets of integrals with the same
denominator combinations:

## PDF page 34

Then, when using OPP the Lorentz indices of the two members of these sets are contracted
in order to give OPP the scalar functions it needs. On the other hand, when using TIR the
first members in eq. (2.79) are all that is needed for this type of reduction to work. It is
clear that the practical success of the decomposition in eq. (2.78) relies on the capability of
a fast and efficient computation of the coefficients C (r) . MadLoop5 has a fully independent
implementation of the recursion-construction procedure presented in ref. [24] (thanks to a
dedicated treatment by ALOHA), and its own internal system of caching and retrieving
the C (r) ’s. At variance with what is done in ref. [24], MadLoop5 does not assume rmax
to be less than or equal to the number of loop propagators, i.e. it admits the possibility
that the contribution of any given vertex to the rank of Nh,l (ℓ) be larger than one. This
is useful, for example, in the context of the computation of QCD corrections to processes
stemming from a Higgs EFT Lagrangian. See appendix C.3 for more details.
We conclude this part with a few diverse observations. Firstly, given the advantages
of an efficient caching and recycling of the coefficients C (r) , in the case of a mixed-coupling
expansion MadLoop5 starts from determining all of the coefficients that will contribute
to Σk0 +1,0 (we recall that we always associate the largest power of the dominant coupling
constant, as defined by the hierarchy of the model, with the terms q = 0: see section 2.4).
Some of the C (r) ’s thus computed will also contribute to Σk0 +1,1 , for which MadLoop5 will
only calculate those C (r) ’s not yet found, and just recycle the others. This procedure is
then iterated till necessary, in the sense that it can be stopped when reaching the largest q’s
among those selected by the user; it is maximally efficient when the smallest user-selected q
is equal to zero, which is justified from a physics viewpoint given the coupling hierarchy of
the model. Secondly, in general the kinematic configurations which are potentially unstable
in TIR are rather different than with OPP; therefore, the possibility of using TIR as an
alternative to OPP before turning to quadruple-precision calculations (see below) is very
beneficial for reducing the overall computing time when numerically-unstable situations

– 32 –

JHEP07(2014)079

theories is always lower than or equal to the number of loop propagators. However, since
different Nh,l functions appear in the inner sums in eq. (2.77), it is actually convenient
(just for the sake of using the present simplified notation) to regard it as the largest rank
in the whole one-loop amplitude; for a given Nh,l , this simply implies that some of the
C (r) coefficients will be equal to zero. Equation (2.78) can be exploited in two ways. One
starts by determining the C (r) ’s once and for all. Then, in the context of the OPP reduction, the numerical computation of Nh,l (ℓ) becomes much faster, as suggested originally
in OpenLoops (see ref. [24]), because for each new value of ℓ generated within the OPP
reduction one simply needs to perform the sums and multiplications explicit in eq. (2.78),
without recomputing the C (r) ’s. Furthermore, when eq. (2.78) is symbolically (as opposed
to numerically) replaced in eq. (2.77), the structures of tensor integrals naturally emerge.
Thus, eq. (2.78) paves the way to performing a Tensor Integral Reduction (TIR) as well.
Therefore, regardless of whether an OPP or TIR procedure will be applied, the inputs to
the Red[ ] operator in MadLoop5 are the sets:
{∫
}rmax
µ 1 . . . ℓ µr
∑ ∑ ∑ (r)
ℓ
⋆
dd ℓ̄ ∏ml −1
,
Cµ1 ...µr ;h,l Λlb Bh,b
.
(2.79)
t
D̄
i,l
h
l∈t
b
t
i=0
r=0

## PDF page 35

are encountered. Finally, since TIR essentially performs integral reduction at the level
of amplitudes, rather than at that of amplitude squared as OPP, it allows one to use
efficiently the decomposition of eq. (2.78) and its caching-and-recycling system also in the
case of loop-induced matrix elements, eq. (2.56).

colour
spin

In an automated approach, the computation of A(n,X) may be performed in the same manner as that of A(n,0) , provided that the usual Feynman rules are supplemented by new UV
and R2 rules, and by imposing that A(n,X) contain one and only one UV- or R2 -type vertex.14 This was indeed the procedure adopted by MadLoop4 for the R2 computation. As
far as UV renormalisation was concerned, the fact that MadLoop4 was limited to considering QCD corrections to SM processes allowed significant simplifications, and eq. (2.80) was
effectively computed in a simpler way, by taking the Born amplitude squared multiplied
by suitable UV factors. Mass insertions cannot be accounted for in this way; however,
their structure being identical to that of the R2 two-point vertex, the two could always be
treated together (see ref. [68] for more details).
The above solution is not tenable when considering an arbitrary renormalisable theory,
and therefore MadLoop5 must explicitly compute eq. (2.80) for both the UV and R2 contributions. This is not the only significant difference between MadLoop4 and MadLoop5.
According to the general philosophy of the current MadGraph5 aMC@NLO approach, the
UV and R2 rules are part of the NLO theory model15 chosen by the user, and that MadLoop adopts when performing a computation: they are not (as opposed to what happened
with MadLoop4) hard-coded UV or R2 computer routines corresponding to n-point counterterms, but a set of instructions in UFO, that ALOHA will dynamically translate into
the latter routines.
After including the UV and R2 rules into a UFO model (an operation that, we remind
the reader, has to be performed once and for all per theory and per type of corrections, and
which FeynRules will soon be able to perform automatically), it should be clear that the
computation by MadGraph5 aMC@NLO of A(n,X) becomes identical to that of a regular
tree-level amplitude for which only Feynman rules are relevant; thus, we shall call this a
tree-matching construction. In order to increase the flexibility of MadLoop5, in particular
for what concerns the exclusion of the contributions of certain loop integrals, and to allow
developers more freedom when debugging, an alternative but fully equivalent procedure
14
15

Note that in this context a “vertex” can have two external legs.
In fact, it is their very presence that tells NLO and LO models apart. See also section 2.1.

– 33 –

JHEP07(2014)079

UV renormalisation and R2 contribution. In order to obtain V (r) as defined in
eq. (2.55), MadLoop must sum to the result of the integral-reduction procedure, eq. (2.77),
the R2 (see eq. (2.72)) and the UV-renormalisation contributions. Both of these can be
cast in the form of a tree-level-like amplitude A(n,X) times the Born amplitude, whose
contribution to eq. (2.55) will therefore be:
{
}
∑
⋆
2ℜ A(n,X) (r)A(n,0) (r) ,
X = R2 , UV .
(2.80)

## PDF page 36

has been implemented, which we shall call loop-matching construction. The tree-matching
and loop-matching constructions (an explanation of which will be given below) can be
understood by considering the physics contents of the generic UV and R2 counterterm G,
which we shall denote as follows:
{{
}
} {
}kloop
(e)
(lk )
(e)
(lk )
G=
I1 , . . . Im ; I1 , . . . Ink
; W, L, λ, c, X .
(2.81)
k=1

16

A mass insertion is treated in a similar manner as vertices; therefore, all external particles must be
outgoing, whence the t̄.
17
The term “set” implies that two or more identical particles contribute one particle identity to this set,
(e)
(e)
as opposed to the case of external particles, which are all explicitly present in the list {I1 , . . . Im }. Note
that, when circulating in a loop, a quark and its antiquark can be identified. Furthermore, it should be
clear that the present “topology” has nothing to do with that introduced in eq. (2.76).

– 34 –

JHEP07(2014)079

The quantity X determines the kind of counterterm one is working with — UV wavefunction, or internal n-point UV and R2 functions; it also allows the builder of the model
to specify whether G will be used in the context of a tree-matching or loop-matching
construction. In other words, and in order to stress this point again: MadLoop5 can
handle both types of construction, which are simply seen as attributes of the model used
for the computation. This flexibility is important for example because models constructed
“by hand” are set up in a different way w.r.t. that adopted by FeynRules. The quantity c
is symbolically (i.e., not numerically) set equal to a coupling constant, with that implying
that G is a counterterm relevant to NLO corrections in the theory whose perturbative
expansion is governed by that coupling. Note that in a model there may be several subsets
of counterterms, each associated with a different type of correction; in the example of the
mixed QCD-QED case discussed at the beginning of section 2.4, when c = αS one has
counterterms for QCD corrections (eq. (2.26)), and when c = α one has counterterms for
QED corrections (eq. (2.27)). The quantities L and λ in eq. (2.81) denote the Lorentz and
(e)
(e)
colour structures of G respectively. The set {I1 , . . . Im } is the list of “external” particle
identities associated with G. For example, if G is the contribution to αS renormalisation
due to the guū vertex, then this set is equal to {g, u, ū}; if G corresponds to the mass
insertion for the top quark, then one has16 {t, t̄}. The counterterm G in general receives
(l )
(l )
contributions from kloop ≥ 1 different types of loop diagrams, and {I1 k , . . . Inkk } is called
the k th loop topology, i.e. the set of the identities of the particles circulating in the k th
type of loop.17 When counting these loops, one needs to take into account the physical
meaning of G. By using again the example of the guū vertex, one may be tempted to
conclude that kloop = 1, which corresponds to the triangle corrections to such a vertex.
This would be incorrect: in fact, since G is a contribution to αS renormalisation, it must
include wave-function renormalisation factors; therefore, in the kloop types of loops one
must include the bubble diagrams relevant to the g, u, and ū external legs. Thus, in this
example one will need to consider both {g, u} (for triangles and the u self-energy) and
{g}, {q}, {b}, {t} (for the gluon self-energy; q is a massless quark, and b and t are heavy
quarks). It should be clear that this complication (there are more loop topologies that
contribute to G than the list of its external particles would suggest) is basically due to
wave-function renormalisation, which physically corresponds to the fact that renormalised

## PDF page 37

i

for coupling and internal 2-point (bubble) renormalisation respectively, and
W ∝ δm ,

W ∝ WR2 ,vertex ,

(2.83)

for UV mass insertions and an R2 correction, respectively. From the discussion presented
before, it follows that the Z and δm terms in eqs. (2.82) and (2.83) will be related to the sets
(l )
(l )
{I1 k , . . . Inkk }. On the other hand, MadLoop5 leaves the model builder the possibility of
implementing coupling-constant renormalisation by directly working at the level of vertex
renormalisation. This can be simply done for example by adopting:
−1
W ∝ 1 − Zvertex
,

W ∝ 1 − Zwf,i ,

(2.84)

instead of the settings of eq. (2.82). One may (slightly improperly, since the physics
contents are exactly the same) refer to the procedures induced by eq. (2.82) and eq. (2.84) as
coupling-constant and vertex renormalisation respectively. The latter is the current method
of choice for the extension of FeynRules to NLO. Note that, when working with vertex
renormalisation, wave-function factors for external legs need not be included (as opposed
to the usual case of coupling-constant renormalisation), which can be easily specified in
the model definition. Again, no assumption is made in MadLoop5 on the treatment of
external legs, and full flexibility is maintained by reading the relevant information from
the model.
Now we suppose that an NLO model is given, and thus eq. (2.81) is fully specified
for all counterterms relevant to all types of corrections dealt with by the model. We
shall now discuss how MadLoop5 exploits such information. First of all, one may want to
exclude some loops from the calculation (this can be motivated by physics requirements, for
example when leaving out heavy-flavour contributions, or done for debugging purposes); we
call this operation loop-content filtering (not to be confused with diagram filtering, which
discards over-counting L-cut diagrams at generation time — see section 3.2.1 of ref. [68]).
This filtering is basically trivial in the generation of diagrams: one simply does not include
(l )
(l )
the undesired particles in the list of L-cut particles. The presence of {I1 k , . . . Inkk } in
eq. (2.81) allows one to do the same when computing the UV and R2 contributions: if
this set contains the particle(s) to be discarded, the corresponding contributions are not
included in eqs. (2.82)–(2.84). Apart from loop-content filtering, eq. (2.81) can be exploited
in the context of the tree-matching construction in the same way as all other elementary

– 35 –

JHEP07(2014)079

couplings are defined in terms of renormalised Green functions. When this is not the case,
and notably for mass insertions, and for R2 contributions (because the latter are directly
defined in terms of specific loop integrals — see eq. (2.66)), loop topologies are indeed in
one-to-one correspondence with those naively deduced from the list of external particles.
Finally, in eq. (2.81) W represents the actual value of the counterterm G. By following
the usual textbook procedure which makes use of renormalised coupling constants, and by
ignoring the Lorentz and colour structures, one may e.g. have:
∏
−1
−1
W ∝ 1 − Zcoupling
= 1 − Zvertex
Zwf,i ,
W = 0,
(2.82)

## PDF page 38

building blocks derived from ordinary Feynman rules, by using the information on external
particles, and Lorentz and colour structures. As far as the loop-matching construction
is concerned, one starts from a given loop integral C, and determines what we call its
associated tree topology:
C −→ Γ(C) =

({

})
} { (l )
T1 , . . . TT (C) , I1 C , . . . In(lC )
.

(2.85)

{

} {
(
)}
(e)
(e)
I1 , . . . Im
= R (T1 ) , . . . R TT (C) ,

(2.86)

{

(2.87)

where by R(Tα ) we have denoted the root of the αth tree Tα (the root being obviously the
single particle that stems from the loop, and branches into the tree); note that eq. (2.86)
implies m = T (C). Among the counterterms thus found, one further considers the UV
mass insertion and R2 ones, and discards those that do not fullfil the equation:
} {
}
(l )
(l )
I1 k , . . . In(lkk ) = I1 C , . . . In(lC ) .

Equation (2.87) guarantees a rather strict correlation between a generated diagram and
its UV and R2 counterterms, which is quite useful for example when establishing the correctness of a model. It should be pointed out, however, that such a correlation can never
be turned into a one-to-one map, because of coupling-constant or vertex renormalisation,
in which case eq. (2.87) cannot be imposed (since vertex corrections and wave-function
renormalisation are always strictly related, and this is true also when carrying out a vertexrenormalisation procedure). Finally, for each counterterm G selected as explained above,
MadLoop5 builds the corresponding tree amplitude by attaching to G the off-shell currents
relevant to the tree structures {T1 , . . . TT (C) }. When performing coupling-constant renormalisation, MadLoop5 also constructs additional tree-amplitude counterterms by multiplying each Born amplitude by the suitable combination of external wave-function factors.
We conclude this part by re-iterating its main message: MadLoop5 has a fully-flexible
structure that allows it to handle on equal footing several different strategies, such as treematching vs loop-matching construction, or coupling vs vertex renormalisation, thanks to
its capability of obeying the relevant instructions encoded in the model. This includes the
prescription for the renormalisation scheme, which now must be simply seen as one of the
model characteristics.
18

A four-gluon vertex, with two gluons belonging to the loop, gives rise to two trees, both of which are
attached to the loop at the same point.

– 36 –

JHEP07(2014)079

The notation understands that there are T (C) trees Tα attached to the loop18 (see figure 2
(l )
(l )
of ref. [68] for a graphical example of such trees); {I1 C , . . . In C } is the set of particles
that flow in the loop. Since different loops can have the same associated tree topology,
MadLoop5 first collects all of the different tree topologies relevant to the computation
being performed. Next, for each of these, all counterterm vertices G (that have survived
loop-content filtering) are found that fulfill the following equation:

## PDF page 39

19

Incidentally, these tests can also be performed in the context of tree-level matrix-element computations.
Apart from that on the dependence on the mass of an heavy quark, which is still available but too
process-specific to be worth automating.
20

– 37 –

JHEP07(2014)079

Checks, stability, and recovery of numerically-unstable integral reductions.
MadLoop4 featured many self-consistency checks, that served to establish the correctness of any one-loop matrix element generated by the code; they are described extensively
in section 3.3 of ref. [68], and all of them are inherited by MadLoop5. On top of those, in
MadLoop5 we have included two new checks: firstly, we verify that the matrix elements are
Lorentz scalars, by recomputing them using a kinematic configuration obtained by boosting
and rotating the original one; and secondly, in the case of QCD corrections we test whether
the matrix elements computed in the unitary gauge are identical to those computed in the
Feynman gauge.19 The experience with MadLoop4 and MadLoop5 has shown that there
is a vast amount of redundancy in all of these checks; therefore, in MadLoop5 we have
decided to perform only one of them before proceeding to integrate the matrix elements.
We have chosen the most complete one, namely that on the residues of the infrared poles
(where the numerical values of such residues as returned by MadLoop are compared to
those known analytically from the subtraction of real-emission singularities), which has the
virtue of being an indirect test on the UV-renormalisation procedure as well. The other
checks can still be performed if need be, by simply executing a single command from the
MadGraph5 aMC@NLO interactive shell.20
Integral-reduction procedures are fairly involved, and some kinematic configurations
may give rise to numerically-unstable results. Any automated approach must therefore
have solid self-diagnostic and recovery strategies: those of MadLoop4 have been presented
in section 3.4 of ref. [68]. In view of the extended scope of MadLoop5 w.r.t. that of
MadLoop4, both of these strategies have been completely redesigned, for the technical
reasons which we shall now discuss. Firstly, MadLoop4 based the instability diagnostics
on the results of tests performed within CutTools, on a loop-by-loop basis. Therefore,
the capability of MadLoop5 to exploit both the OPP and TIR methods has forced us to
set up a CutTools-independent diagnostic tool. Furthermore, a loop-by-loop method is in
any case not ideal, because it is never trivial to determine the threshold that decides when
a computation is flagged as unstable (e.g., a single loop integral may be unstable, but give
a totally negligible contribution to the full amplitude). This problem is exacerbated when
increasing the final-state multiplicity, and indeed suggests to use an “inclusive” (i.e., at the
level of the amplitude, rather than of the individual loop integral) type of test in MadLoop5,
which can handle more complicated processes than MadLoop4. Secondly, the recovery
strategy used by MadLoop4 (which involved a small deformation of the kinematics) is on
the one hand related to the loop-by-loop diagnostic (because when one considers two or
more integrals simultaneously, the deformation of the kinematics that renders stable an
unstable integral can turn a stable integral into an unstable one), and on the other hand
not particularly satisfactory when increasing the process multiplicity (because it becomes
more difficult to obtain a stable result out of the deformed kinematic configuration).
The diagnostic procedure of MadLoop5 works as follows. Let us write the result
of eq. (2.55), obtained by MadLoop after integral reduction and UV renormalisation, as

## PDF page 40

follows:
(4π)ǫ
V (r) =
Γ(1 − ǫ)

(

µ2F
Q2

)ǫ (

)
c−2 c−1
+
+
c
0 .
ǫ2
ǫ

(2.88)

For any given kinematic configuration, the coefficients cj of eq. (2.88) are evaluated 1 + ntest
times (in a way specified below), which we denote as follows:
(i)

cj −→ cj ,

i = 0, . . . ntest ,

for j = −2, −1, 0 .

i=0

i=0

(2.90)
(2.91)

which in turn enter the definition of the relative accuracy of the MadLoop evaluation:
∑0
j=−2 ∆cj
χ = ∑0
.
(2.92)
j=−2 c̄j

A computation is deemed unstable, and the corresponding kinematic configuration called
an Unstable Phase-Space point (UPS), when:
χ > ε,

(2.93)

with ε a quantity which can be defined by the user, but whose default value is 10−3 .
(i=0)
results in eqs. (2.89)–(2.91) are those obtained by applying the OPP reduction
The cj
(i>0)

are obtained in two different ways,
with the given kinematic configuration. The cj
by performing again the integral reduction either: a) by using a kinematic configuration
obtained by rotating the original one (hence, by following the same procedure as is used in
one of the self-consistency checks previously discussed); or b) by using a different ordering of
the loop propagators D̄i as input to OPP (this changes the inner workings of the reduction
procedure, and is thus numerically different from, although physically completely equivalent
to, what one does with the original ordering). These two re-computation procedures are
called Lorentz test and Direction test respectively. By default, MadLoop5 sets ntest =
2, and performs one Lorentz test and one Direction test. Both ntest and the type of
tests performed can be controlled by the user. Note that any Direction test re-uses the
(i=0)
coefficients C (r) of eq. (2.78) computed in the context of the first evaluation (cj
), and is
thus less time-consuming than Lorentz tests, despite the fact that both require the integral
reduction to be performed from scratch. In the case of a mixed-coupling expansion, each
(i)
(i)
of the cj is expanded as is done in eq. (2.23), so that it will correspond to a set {cj,q }. By
fixing q (which is associated with a given combination of coupling constants, see section 2.4),
one defines χq as in eqs. (2.90)–(2.92); a kinematic configuration is a UPS if, following
eq. (2.93), χq > ε for any q.
When a UPS is found, MadLoop5 has two main methods for recovery, which are
attempted in turn. It starts by changing the integral-reduction procedure, from OPP to

– 38 –

JHEP07(2014)079

These coefficients are used to define the following quantities:
{∣ ∣}ntest )
{∣ ∣}ntest
1(
∣ (i) ∣
∣ (i) ∣
c̄j =
,
+ min ∣cj ∣
max ∣cj ∣
2 {∣ ∣} i=0
i=0
∣
}
{∣
∣ (i) ∣ ntest
∣ (i) ∣ ntest
,
− min ∣cj ∣
∆cj = max ∣cj ∣

(2.89)

## PDF page 41

2.4.3

Integration of one-loop contributions

The way in which the virtual contributions are integrated by MadGraph5 aMC@NLO in
either an fNLO or an NLO+PS computation is quite different w.r.t. what was done in
aMC@NLO. In the latter, one-loop matrix elements were integrated separately from the
other contributions, and eventually combined with them at the level of either distributions
(in the case of fNLO), or unweighted events (in the case of NLO+PS); on the other hand,
in MadGraph5 aMC@NLO all contributions are integrated simultaneously. The original
strategy of aMC@NLO had been adopted because it allowed one to control, in a very
direct manner, the number of phase-space points for which the virtual corrections were
computed, and by doing so to reduce such a number, without this implying a degradation
of the overall accuracy of the physical results.22 The fact that the accuracy of the final
result does not change significantly despite the reduction mentioned above stems from the
following two observations. a) n-body phase-space integrals are significantly simpler than
(n + 1)-body ones, and therefore require to be sampled a smaller number of times than
the latter. b) Virtual corrections are usually smaller than the Born, which implies that
a smaller number of phase-space points has to be used to integrate the former than the
latter, in order to obtain the same absolute precision for the two resulting integrals. The
21

This being a single integral, it should be clear that this procedure will not necessarily result again in
being classified as a UPS — the original UPS was due to all integrals being reduced with OPP.
22
The reduction of the number of evaluations of the one-loop matrix elements was (and still is) highly
desirable because virtual contributions are typically the numerical bottleneck in our NLO computations
(owing to the efficiency of the FKS subtraction, which leads to a relatively fast convergence of the realemission contributions).

– 39 –

JHEP07(2014)079

TIR. The results of TIR depend on the specific TIR library MadLoop5 is linked to. In
principle, any library might be used; in practice, so far we have considered IREGI [168]
and PJFry++ [169, 170]. A given TIR library has a maximal number of propagators it
can handle (presently, up to hexagons for IREGI and up to pentagons for PJFry++);
in the case one particular loop integral exceeds that number, OPP is used again for it
and only for it.21 More than one TIR library can be linked to MadLoop5 at the same
time. After having found a UPS with OPP, MadLoop5 switches to the first of such TIR
libraries, and repeats the diagnostic tests mentioned above. If the result is again classified
as a UPS, the next TIR library is used, and so forth. If none of the available TIR libraries
is able to give a numerically-stable reduction, MadLoop5 resorts to the second method
of recovery, namely the OPP integral reduction with all relevant quantities (Nh,l and the
internal CutTools algebra) computed in quadruple precision. This is usually extremely
effective, but has the disadvantage of being extremely slow. In the case when the recovery
in quadruple precision fails as well, MadLoop5 gives up, sets c0 = 0, and proceeds to the
next kinematic configuration; the user is warned when this happens. We emphasise that
the order in which the various integral-reduction procedures are used in the context of UPS
recovery (OPP, TIR library #1 to TIR library #n) can be controlled through an input
card. So in the present public version of MadGraph5 aMC@NLO, where TIR reduction is
not yet included, only OPP and quadruple-precision calculations are employed.

## PDF page 42

{ (n,1) (n,0) ⋆ }
2ℜ Ah Ah
,
∣
∣
∣ ≡
∣
∣ (n,0) ∣2
∣ (n,0) ∣2
∣A h ∣
∣A h ∣
Vh

(n,0)

(2.94)

where Ah
has been introduced in eq. (2.68), and Vh can be obtained e.g. from eq. (2.72)
by not performing the sum over h there (and similarly for the corresponding UV counterterms). The ratio in eq. (2.94) is a slowly-varying function over the phase space (behaving
essentially as logarithms or dilogarithms), and is to a good extent independent of the helicity configuration h (note that the same helicity configuration h is used in the numerator
and in the denominator): in other words, one-loop and Born matrix elements have very
similar dependencies on helicity configurations and, in particular, there are no helicity
(n,0)
is null while Vh is not. This also implies that the ratio of
configurations for which Ah
eq. (2.94) is numerically of the same order as its helicity-summed counterpart:
∑
Vh
V
(2.95)
∣ .
∣
∣2 ≡ ∑ ∣ h
∣ (n,0) ∣2
∣A(n,0) ∣
h′ ∣ A h′ ∣

In MadGraph5 aMC@NLO we exploit the behaviour w.r.t. to h of eq. (2.94) by performing
the sum over helicities implicit in V by means of MC methods: for each phase-space
∣
∣ point,
∣ (n,0) ∣2
a single helicity configuration is chosen, according to the relative weights of ∣Ah ∣ . What
23

On top of item a) discussed above: all other things being equal, two or more contributions integrated
together lead to a better accuracy than when integrated separately, in the case of cancellation among them,
as it often happens with NLO cross sections; also, a smaller number of integration channels implies a
reduction of negative-weighted NLO+PS events.
24
With some abuse of notation, V here denotes only the finite part of the one-loop contribution, i.e. the
coefficient c0 of eq. (2.88) up to overall factors, which are irrelevant for the present discussion.

– 40 –

JHEP07(2014)079

possibility of exploiting observation a) in a flexible manner was the main reason why in
aMC@NLO the virtual contributions were integrated separately. In fact, without a separate
integration, n-body matrix elements were previously evaluated the same number of times
as (n + 1)-body ones (see eq. (2.50) for an explicit example, relevant to the Born). This
could of course be bypassed in several ways, none of which however is simpler than a separate treatment, and better suited to an adaptive multi-channel integration. As explained
in section 2.4.1, MadGraph5 aMC@NLO combines n- and (n + 1)-body contributions in
the opposite way w.r.t. that of aMC@NLO, taking an n-body viewpoint. This is what
allows MadGraph5 aMC@NLO to naturally use observation a) while integrating one-loop
matrix elements together with all other contributions.
The simultaneous versus separate integration is only one of the differences between
the current treatment in MadGraph5 aMC@NLO and what was done previously. While
the former has several advantages over the latter,23 if applied straightforwardly it implies
that the same number of evaluations are performed for the one-loop as for the Born matrix
elements, which is not ideal in view of observation b). In order to amend this situation, and
thus to increase the speed of MadGraph5 aMC@NLO without a loss of accuracy, several
solutions have been devised. They are based on the properties of the following quantity:24

## PDF page 43

where EV denotes all contributions other than V (the integration over the extra degrees of
freedom relevant to the real matrix elements plays no role here, and is understood). Integrals such as that of eq. (2.96) are performed by adaptive methods, which entail successive
estimates (called iterations) of quantities relevant to the integrals. For the generic integral:
∫
dφn F
(2.97)
we shall denote by

Ik (F ) ,

σk (F ) ,

(2.98)

the results of the k th iteration for the mean (i.e., the integral itself) and the standard
deviation. One expects that:
∫
lim Ik (F ) = dφn F ,
lim σk (F ) = 0 .
(2.99)
k→∞

k→∞

It will be convenient for what follows to have an explicit expression for the mean:
pk
(
) (
)
1 ∑
Φn φ(k,i)
F φ(k,i)
Ik (F ) =
.
(2.100)
n
n
pk
i=1

(k,i)

Here, we have denoted by φn the ith phase-space point, generated at random during the
course of the k th iteration; a total of pk points are considered. The quantity Φn collects all
normalisation and jacobian factors. We point out that, when applying eqs. (2.97)–(2.100)
to the case of interest, eq. (2.96), one is able to obtain not only the integral of the sum
EV + V , but also those of EV and V individually, by keeping track of Ik (EV ) and Ik (V )
respectively (despite the fact that the two terms are still integrated simultaneously). This
is useful in view of the following manipulation: we introduce an approximant of V , that
we denote by Ṽk , which we use in the identity:
∫
∫
(
[
)]
dφn V = dφn Ṽk + V − Ṽk .
(2.101)
As the notation suggests, the approximant Ṽk is a function of the adaptive-integration
iteration, where it is used according to the following formula:
p

p f

k
)
) (
)[ (
(
)
)]
(
∑k (
1 ∑
1 k
(k,i)
(k,i)
(k,i)
(k,i)
Ik (V ) =
Ṽ
−
Ṽ
V
φ
Φ φ(k,i)
Φ
φ
+
φ
.
φ
k
k
n
n
n
n
n
pk
p k fk
i=1
i=1
(2.102)

– 41 –

JHEP07(2014)079

has been said above guarantees the efficiency and the fast convergence of this procedure, as
well as a reduction of the time spent in computing the one-loop contribution (see eq. (2.79)
— such a reduction is due to the fact that the numerator is simpler and therefore less
time-consuming: the time spent carrying out the integral reduction is not affected).
Let us finally see how the fact that the quantity in eq. (2.95) is a slowly-varying function
of the kinematics helps reduce further the CPU load necessary to compute the integral of
V . In order to shorten the notation introduced in section 2.4.1, we symbolically write the
integral of the NLO cross section as follows:
∫
dφn (EV + V ) ,
(2.96)

## PDF page 44

A number 0 < fk ≤ 1 has been introduced in eq. (2.102), which implies that the difference
V − Ṽk is computed only in a fraction fk of the total number of point thrown.25 For an
explicit evaluation of eq. (2.102), we need to define what enters it. We have:
∣
∣2
∣
∣
Ṽk = ck ∣A(n,0) ∣ ,
(2.103)

with ck a quantity to be determined iteration-by-iteration, similarly to what happens for
fk . The initial conditions are:
f1 = 1 ,
c1 = 0 ,
(2.104)

grid {Ik−1 (V )}
{
(∣
∣2 )} ,
grid Ik−1 ∣A(n,0) ∣
{
{
} }
1
2σk−1 (V − Ṽk−1 )
fk = fk−1 max min
,2 ,
.
σk−1 (EV + V )
4
ck =

(2.105)

(2.106)

The value of fk obtained from eq. (2.106) is further constrained to be in the range
0.005 ≤ fk ≤ 1 .

(2.107)

A few explanations are in order. Firstly, ck and fk are dynamically constructed, using
the information that the numerical integrator (we use a modified version of MINT [171])
has gathered during the previous iteration. One such piece of information is a grid, which
among other things stores the averages of the function that is being integrated in nonoverlapping phase-space regions which cover the whole phase space. Therefore, ck as defined
in eq. (2.105) is a piecewise-constant function. Because of the properties of eq. (2.95), we
expect it to be close to an overall constant, and Ṽk defined in eq. (2.103) to be a good
approximant of V . Secondly, if indeed Ṽk is an increasingly (with k) good approximant of
V , we expect the quantity σk−1 (V − Ṽk−1 ) that appears in eq. (2.106) to decrease faster
than the estimated error on the integral of EV + V , thus inducing the values of fk to
decrease. On the other hand, eq. (2.106) prevents the series of fk ’s to be fluctuating:
w.r.t. the preceding value fk−1 , fk can be at most a factor of 2 larger, or a factor 1/4
smaller — these values are simply sensible, but can of course be changed, as the absolute
minimum for fk given in eq. (2.107).
The rationale behind eqs. (2.101)–(2.107) should now be clear, and it has to do with
the fact that one can compute Ṽk much faster than V . One starts in the first iteration
by always computing V ; while doing so, MadGraph5 aMC@NLO gathers the information
that will allow it to construct the approximant Ṽ2 to be used in the next iteration. While
this procedure is iterated, the relative26 number of times V (Ṽk ) is computed is decreased
(increased). The procedure is exact, being based on the local identity (2.101). Furthermore,
25

Although eq. (2.102) literally implies that these are the first pk fk points, in the actual computation
they are chosen randomly in the whole set of the pk points, so that biases are avoided.
26
MadGraph5 aMC@NLO, following MadGraph, starts with a relatively small number of points
p1 ≃ 80Ndim , and doubles it at each iteration.

– 42 –

JHEP07(2014)079

and for k > 1 we define:

## PDF page 45

the code is protected against any pathological behaviour: if, for example, Ṽk does not turn
out to be a good approximant of V , one will have fk ≃ 1 for all k’s, so that Ṽk will not
play any role (see eq. (2.102)). In practice, this situation has not been encountered so far.
2.4.4

Matching to showers: MC@NLO

In this section, we review the MC@NLO formalism [26] and its implementation in MadGraph5 aMC@NLO, making extensive use of the results given in section 2.4.1. We start by

(i,j)∈PFKS

dσ

(S)

= dσ (MC) +

∑

∑

(NLO,α)
dσij
,

(2.109)

(i,j)∈PFKS α=S,C,SC
(NLO,α)
(NLO,E)
where dσij
and dσij
are exactly the same quantities (eqs. (2.45) and (2.46)) that
appear in the NLO cross section (eq. (2.47)). The only new (w.r.t. the NLO) ingredient
in MC@NLO is thus dσ (MC) , which is the cross section one obtains from the parton shower
Monte Carlo (PSMC) one interfaces to by truncating the perturbative expansion at O(αSb+1 )
(the Born matrix elements being of O(αSb )), in the case of resolved emission (eq. (2.108))
and of no resolved emission (eq. (2.109)) — indeed, as is implicit in the notation these
two cases result in the same cross section, up to a sign. The crucial point is that, since
the leading IR behaviour of any PSMC must be the same as that resulting from an exact
matrix-element computation in QCD, eqs. (2.108) and (2.109) are locally finite.27 This is
the reason why the dσ (MC) terms are called the MC counterterms, and the MC@NLO cross
section, contrary to the NLO one, can be unweighted.
The definition of the MC counterterms immediately implies that their actual expressions depend on the specific PSMC one interfaces to. These expressions have therefore to
be worked out case-by-case, which has been done for the following PSMCs, whose matching
with NLO calculations has been fully validated in MadGraph5 aMC@NLO: Pythia8 [123],
Herwig++ [121, 122], HERWIG6 [142, 143], and Pythia6 [141] (in the case of pT -ordered
Pythia6, only processes with no strongly-interacting particles in the final state are supported). The details of the construction of the MC counterterms for some of these PSMCs
are given in refs. [26, 172–175]. On the other hand, the general structure of the MC counterterms is actually PSMC-independent, and it is easy to convince oneself that they can
27

In fact, this locality property may be spoiled by certain approximations inherent in the PSMC. It is
not difficult to restore it [26], as we shall briefly discuss later.

– 43 –

JHEP07(2014)079

considering the formulation where the short-distance cross sections are defined for a given
real-emission process rR ∈ Rn+1 , which also allows one to symplify the notation, since the
dependence on rR can thus be easily understood. We shall eventually arrive at expressions
which lend themselves to the same manipulations as those carried out at the end of section 2.4.1, which MadGraph5 aMC@NLO exploits in order to deal with MC@NLO cross
sections defined at given Born processes, precisely as for their NLO counterparts.
In essence, MC@NLO defines two short-distance cross sections, associated with realemission-type kinematics (i.e., (n + 1)-body) and Born-type kinematics (i.e., n-body),
dubbed H- and S-event contributions respectively. Their forms are written as follows:
∑
(NLO,E)
dσij
− dσ (MC) ,
(2.108)
dσ (H) =

## PDF page 46

always be written in the following way:
dσ (MC) =

∑

(MC)
dσij
,

(2.110)

(i,j)∈PFKS

(MC,0)
dσij
=

∑∑
c

(MC,0)

dσij,cl

=L

(MC,0)
dσij,cl
,

(2.111)

l∈c

(MC)

(

(l)
x1,2

(l)
i⊕j∈l αS PIj Ii⊕j (zij )
(l) (l) dϕ
dφn . (2.112)
M(n,0)
Θ(MC) dξij dzij
c
(l)
Ni⊕j 2π
2π
ξij

)δ

(MC,0)
(MC)
As the notation suggests, although dσij
does not necessarily coincide with dσij
(the
possible differences between the two will be explained below), it does fully include its
physics contents, which we now turn to describing.
The sums in eq. (2.111) run over all possible planar colour configurations (c), and the
individual colour lines belonging to them (l). In MadGraph5 aMC@NLO we represent a
colour configuration as a list, c = {l1 , . . . lm }, where the individual colour line is represented
as an ordered pair, lk = (s(k), e(k)), whose meaning is that of a connection between particle
Is(k) (the starting point of the line) and particle Ie(k) (the end point of the line). This
implies that, for any given c, a quark or an antiquark will belong to a single colour line
(through its colour or anticolour respectively), while a gluon will belong to two colour lines
(one for colour and one for anticolour). This is the reason for the factor Ni⊕j in eq. (2.112),
which is equal to 1(2) if i⊕j is a quark or an antiquark (a gluon). MadGraph5 aMC@NLO
constructs the colour configurations during an initialisation phase, by gathering the relevant
(l)
(l)
information from the underlying matrix elements. ξij and zij are the PSMC shower
variables; as the notation indicates, in general their forms depend on the branching particle
i ⊕ j (in particular, on whether it is in the final or initial state), and on the colour line
(which determines the colour partner of i ⊕ j). The actual shower variables are very
PSMC-dependent, and they are coded in MadGraph5 aMC@NLO for all the PSMCs one
may match with. The colour connections in general also determine the choice of Bjorken
x’s made by the PSMC (see e.g. ref. [26]), which is the reason for the dependence on l in the
28

Different classes of PSMCs may be conceived, for example dipole-shower-based or by going beyond the
leading-Nc approximation (see e.g. refs. [183–186]), which could induce a different form. However, the idea
of MC counterterms in general, and of eq. (2.110) in particular, would still be valid.
29
In order to simplify the notation, we understand the universal, azimuthal-dependent part of the branching (see e.g. appendix B of ref. [10]).

– 44 –

JHEP07(2014)079

since FKS pairs are in one-to-one correspondence with IR singularities, which in turn are
at the core of the shower mechanism. It is important to bear in mind that this implies
that eq. (2.110) is therefore valid not only for those PSMCs based on a 1 → 2 branching
picture (such as those just mentioned), but more generally for any PSMC consistent with
QCD (in particular, those that adopt a dipole picture [34, 176–182]). The functional form
(MC)
of the terms dσij
is the same for all of the PSMCs considered here,28 and we shall briefly
describe its construction in what follows. One starts with the PSMC cross section that
results from a single branching:29

## PDF page 47

2

with µ1 ≤ µ2 two given mass scales. While we typically regard D as a smooth function, it
is perfectly fine to consider its sharp version:
D(µ) = Θ (µQ − µ) ,

µ Q = µ1 = µ2 ,

(2.114)

which is a particular case of eq. (2.113). Secondly, on an event-by-event basis we determine
a mass scale by using:
µr = D−1 (r) ,
(2.115)
with r a flat random number (note that with eq. (2.114) one obtains µr ≡ µQ ). Thirdly, we
give µr in input to the PSMC, where it acts as an upper bound to the internally-generated
shower scales as explained before. The physical meaning of µr (be it a relative transverse
momentum, a virtuality, or whatever else) depends on the specific PSMC chosen, but is
irrelevant here and need not be specified. The crucial thing is the following: by means of
this procedure, we are effectively changing the shower w.r.t. what the PSMC would do if
30

This technique has been used sparingly in MC@NLO v3.3 and higher.

– 45 –

JHEP07(2014)079

argument of the luminosity factor L(MC) in eq. (2.112). Pba (z) is the Altarelli-Parisi oneloop kernel [187], for parton b emerging from the branching of parton a with momentum
(n,0)
fraction z. Mc
is the Born matrix element multiplied by a factor determined by the
colour configuration c, according to the prescription of ref. [188]. Finally, Θ(MC) symbolically
denotes all kind of kinematics constraints, such as generation-level cuts (an n-body Born
must have n well-separated partons), possible dead-zone conditions, and so forth.
Implicit in eq. (2.112) is the choice of a shower scale, which roughly speaking sets
an upper bound for the hardness of each branching. Since PSMCs are based on a smallscale approximation, it is clear that the larger the shower scale, the worse the description of
physics by any PSMC. While in the context of standalone-PSMC simulations it may be necessary to consider shower scales that stretch that approximation (simply to fill phase-space
regions otherwise inaccessible), such an attitude is not justified when PSMC are matched
with NLO computations, since the latter provide a much better description of hard-emission
regions. Note that in MC@NLO these undesirable large-shower-scale effects are indeed removed completely at O(αSb+1 ) by the MC counterterms (see eqs. (2.108) and (2.109)).
However, at O(αSb+2 ) and beyond the PSMC may still radiate in the hard regions, potentially giving effects which are simply not sensible from the physics viewpoint. Furthermore,
even at O(αSb+1 ) it does not make much sense to allow the PSMC to produce radiation
only to eventually remove it. Fortunately, it is possible to give the PSMC an external mass
scale in input; during the course of the shower, the PSMC will generate branchings after
choosing the smallest between this external scale and its internally-generated shower scale.
In MadGraph5 aMC@NLO, we exploit this possibility in the following way.30 Firstly, we
introduce a function of a mass scale µ:


µ ≤ µ1 ,

1
D(µ) = monotonic
(2.113)
µ1 < µ ≤ µ2 ,


0
µ>µ ,

## PDF page 48

left alone. This change must therefore correspond to a change in the MC counterterms,
because of the very definition of the latter. This amounts to:
(MC,D)
(MC,0)
dσij
= D (µ(Kn+1 )) dσij
.

(2.116)

(MC,D)
(MC)
(NLO,S)
dσij
= (1 − G) dσij
+ G dσij
|real .

(2.117)

Here, G is a smooth function defined so that G → 1 in the soft limit, and G = 0 outside
(NLO,S)
of the soft region; dσij
|real is the soft part of the NLO cross section, eq. (2.46), where
only the real-emission matrix element contribution is kept.33
A few comments concerning eq. (2.117) are in order. Given that what the PSMC is
(MC,D)
supposed to do is dσij
, while what MC@NLO assumes the PSMC does is dσ (MC) of
31

The main reason being that MC@NLO short-distance cross sections have no contributions of O(αSb+2 )
or higher; terms of these orders in the physical cross sections can only be generated through MC radiation.
32
On top of being, obviously, matching-method dependent. We stress that the results of D variations in
MadGraph5 aMC@NLO can not be used, even as a mere indication, of the matching systematics that
affects other matching methods, such as POWHEG.
33
An analogous solution is adopted when the azimuthal part of the PSMC branching kernel does not
agree with that predicted by the matrix elements.

– 46 –

JHEP07(2014)079

Note that the argument of D in eq. (2.116) is computed by using the underlying
√ kinematic
configuration (after having taken into account its PSMC-specific form: pT , Q2 , and so
forth), and must not be generated randomly. Equation (2.116) can always be used in place
of eq. (2.112), the latter being a particular case of the former, which one can formally
obtain by setting µ1 = µ2 = ∞.
As was discussed before, the function D controls perturbative effects higher than NLO;
hence, its variations can be used to assess the NLO+PS matching systematics (which is,
by definition, the size of terms beyond the formal accuracy of the computation) of the
MC@NLO method. Although this is expected to be small,31 its actual size is observable-,
process- and (especially) PSMC-dependent,32 and it is therefore convenient to be able to
study it in a straightforward way. This is the case in MadGraph5 aMC@NLO, where one
can control the values of the scales µi of eq. (2.113) through the external parameters fi ,
√
with µi = fi ŝ0 , and ŝ0 the Born-level partonic c.m. energy squared.
Equation (2.116) would give the desired MC counterterms if the corresponding PSMC
behaved as expected in the IR regions, namely if it gave exactly the same result as a QCD
matrix-element computation in both the collinear and the soft limits, whence the local
cancellations in eqs. (2.108) and (2.109). Unfortunately, this is not the case in the soft
limit, at least for Herwig and Pythia, where this deficiency is basically a consequence of
the necessity of having a Markovian shower. What is true, however, is that the amount of
soft radiation predicted by the PSMCs is correct; in other words, only its angular pattern
is not consistent with the one required by QCD. Fortunately, such an undesirable feature of
certain PSMCs will not have dramatic consequences on physical observables, because of the
infrared-safety of the latter (the interested reader can find a fuller discussion of this issue in
section A.5 of ref. [26]). The technical problem of the local finiteness of the MC@NLO shortdistance cross sections can be solved by the following definition of the MC counterterms:

## PDF page 49

– 47 –

JHEP07(2014)079

eq. (2.117), there is a mismatch of O(αSb+1 ) between the two. This mismatch, however, is
utterly irrelevant for several reasons. Firstly, because of the properties of G, it is confined
to the soft regions, where effects of all orders in αS are equally important. Secondly, in
(MC,D)
if not in a
practice in the soft region the PSMC does not even correspond to dσij
fully inclusive sense, since the PSMC is unable to handle emissions below the IR cutoffs,
which are of the order of the typical hadron mass (and this for a very fundamental reason:
QCD does not have infinite resolution power). Thirdly, because of the previous point all
NLO+PS matching schemes are liable to have O(αSb+1 ) effects in small-scale regions which
are not in formal agreement with fixed-order results at the NLO, even if the second term
on the r.h.s. of eq. (2.117) were not present (see appendix B.3 of ref. [26] for a discussion
specific to the MC@NLO formalism). Ultimately, then, the differences driven by the G
function are power suppressed (see e.g. ref. [189]); eq. (2.117) is nothing but a formal trick
to render the O(αSb+1 ) MC@NLO cross sections non-divergent (which is important in view
of their numerical integration) in a region where not even the perturbative predictions of
PSMCs are sensible, let alone those of fixed-order computations.
Equation (2.117) also gives us the opportunity of commenting briefly on the alternative
implementation of the MC@NLO method presented in ref. [36]. There, the function G
does not appear, for the simple reason that the two short-distance cross sections on the
r.h.s. of eq. (2.117) coincide in the soft limit and, as explained above, this is a sufficient
condition for not having to introduce G. In turn, this situation occurs because the shower
used in ref. [36], and in subsequent papers, in the context of NLO-matched simulations
is constructed to have the same soft behaviour of the matrix elements (see, in particular,
eq. (2.5) of ref. [190]). Once this is done, the form of the MC counterterms is uniquely
determined, lest one has a mismatch of O(αSb+1 ) (everywwhere in the phase space). One
may opt (as is done in ref. [36]) to see this as a choice made at the level of short-distance
cross sections (the soft behaviour of the MC counterterms), that forces one to modify
the shower in order to preserve the perturbative accuracy. While the point of view of
ref. [26] and of this paper is the opposite one (namely that it is the chosen PSMC which
determines the MC counterterms), the fundamental idea is just the same, and therefore the
MC@NLO subtractions of ref. [36] do not differ in any significant way from those that had
been adopted in MC@NLO and are now used in MadGraph5 aMC@NLO. What has been
changed in the approach of ref. [36] (w.r.t. the previous default) is the shower adopted in
conjunction with the NLO matching performed there (which happens not to be the same as
that used in simulations which are not matched to NLO results). We point out that should
a version of the Pythia or Herwig showers become available with a matrix-element-type
soft behaviour, the relevant MC counterterms would be constructed without a G function.
Furthermore, we stress that the NLO accuracy of the MC@NLO method (including, in
particular, the whole 1/Nc expansion) is maintained, and that the O(αSb+1 ) results are thus
in agreement with those of the corresponding matrix elements (up to power-suppressed
effects, as explained above), regardless of the behaviour of the PSMC and thus of the
presence of a G function. On the other hand, if some aspect of the PSMC is deficient (for
example the treatment of subleading-colour contributions), the MC@NLO method itself
cannot provide an improvement in the MC-dominated kinematic regions — any issue of
this kind must be addressed at the level of the PSMC itself.

## PDF page 50

Equation (2.117) is the final form to be used in eq. (2.110); when the latter is in turn
replaced in eqs. (2.108) and (2.109), one immediately realises that it is convenient to define
the H- and S-event contributions at fixed FKS pair:
(H)
(NLO,E)
(MC)
dσij
= dσij
− dσij
,
∑
(NLO,α)
(S)
(MC)
.
dσij
= dσij
+
dσij

(2.118)
(2.119)

α=S,C,SC

(E)

Kn(H) ≡ Kn+1 ,

(S)

Kn(S) ≡ Kn+1 ,

(2.120)

so that the generating functional finally reads as follows:


(
(
) dσ (H) (rR )
) dσ (S) (rR ) 
∑
∑ 
ij
ij
,
FMC@NLO =
Kn(H)
F
+ FMC Kn(S)
(ij)
(ij)
(ij)
(ij) 
 MC
dχ dχ
dχ dχ
rR ∈Rn+1 (i,j)∈PFKS

Bj

n+1

Bj

n+1

(2.121)
where FMC is the generating functional of the PSMC one interfaces to, and its argument
indicates the parton configuration to be adopted as the starting condition for the shower. In
eq. (2.121) we have reinstated the formal dependence of the short-distance cross sections on
the real-emission process rR . In this way, the complete similarity between the MC@NLO
and NLO cross sections in terms of sums over partonic processes and FKS pairs (i.e.,
between the r.h.s. of eq. (2.121) and the l.h.s. of eq. (2.49)) is evident. Thus, as was
anticipated at the beginning of this section, all the manipulations performed at the end of
section 2.4.1 apply to the MC@NLO case as well. In particular, the formulation where the
MC@NLO short-distance cross sections are defined by fixing the Born-level process is the
one adopted in MadGraph5 aMC@NLO. Among other things, this renders it particularly
easy to obtain S events by integrating over ξi and yij before unweighting (which is expected
to reduce the number of negative-weight events, as advocated in ref. [26] in the context
of the MC@NLO formalism; the same idea, dubbed “folding”, has been independently
proposed and implemented in POWHEG).
Before concluding this section, we present two variants of what was discussed so far,
that we shall want to consider for future MadGraph5 aMC@NLO developments. The first
one concerns the definition of the MC counterterms. The advantage of using eqs. (2.118)
(l) (l)
and (2.119) is a one-to-one correspondence between the shower variables (zij , ξij ) and the
FKS integration variables (ξi , yij ). Apart from a transparent way of identifying the IR
(H)
(S)
singular structure (which in turn is related to dσij
and dσij
being locally finite at fixed
(i, j)), this implies that, when the integration measure over the MC variables is expressed
(ij)
in terms of dχn+1 , as it must according to eq. (2.121), one can factorise the jacobian
)
(
(l) (l)
∂ zij , ξij
;
(2.122)
∂ (ξi , yij )

– 48 –

JHEP07(2014)079

It is easy to see that these quantities are locally finite (by construction of the shower
(l)
(l)
variables ξij and zij ), precisely as their summed counterparts of eqs. (2.108) and (2.109).
Eqs. (2.118) and (2.119) can now be used to define the MC@NLO generating functional. In
order to do that we also introduce, for consistency with the standard notation and in view
of the discussion to be given in section 2.4.5, the H- and S-event kinematic configurations:

## PDF page 51

in the current version of MadGraph5 aMC@NLO, this jacobian is computed analytically.
The definitions of eqs. (2.118) and (2.119) might however have a numerical drawback, due
(NLO,α)
. Its absence in the MC countertto the presence of the factor Sij only in the terms dσij
erms could induce differences in the damping of singularities not due to the FKS pair (i, j),
that in turn could result in an unnecessary large fraction of events with negative weights.
This situation can be amended as follows: by using eq. (2.35) one obtains the identity:
∑
∑
∑
(MC)
(MC)
Skp dσij
(2.123)
dσij
=
dσ (MC) =
(i,j)∈PFKS (k,p)∈PFKS

(i,j)∈PFKS

∑

dσ (MC) =

(MC)
dσ̂ij
,

(2.124)

(i,j)∈PFKS
(MC)

dσ̂ij

= Sij

∑

(MC)
.
dσkp

(2.125)

(k,p)∈PFKS

(MC)
(MC)
By using dσ̂ij
in place of dσij
in eqs. (2.118) and (2.119), one can factor out a term

(l)

(l)

Sij . The disadvantage of course is that the pair (zkp , ξkp ) is not in one-to-one correspondence with (ξi , yij ) any longer, which implies that the relevant jacobians will be much more
involved than that in eq. (2.122). However, this is clearly only a technical problem, which
can be overcome by giving up the requirement that jacobians be computed analytically.
With modern routines for the numerical evaluation of derivatives this appears definitely
feasible, and it would also pave the way for a leaner interface to new PSMCs.
We now turn to the second variant, which concerns the MC@NLO formulation proper.
A good feature of the MC@NLO cross section is that it gives a clear separation of matrix
element and Monte Carlo effects. A drawback is that one is forced to ignore the fact that in
the MC-dominated region (i.e., at small scales) real-emission matrix elements do not give a
good description of the underlying physics, which implies that the contribution of H events
there is important only in terms of total rate, but not in terms of shapes, which indeed
are dominated by showered S events. From the viewpoint of final (physical) results this is
irrelevant, but it entails a loss of efficiency, since typically H events have negative weights
in the MC-dominated region. A possible way to address this problem is the following.
Consider a function ∆ with the properties:
∆ = 1 + O(αS ) ,
∆ −→ 0

IR limits .

It is immediate to see that the following definitions:
(
)
(H)
(NLO,E)
(MC)
dσij
= dσij
− dσij
∆,
∑
(NLO,α)
(S)
(MC)
(NLO,E)
dσij
= dσij
∆+
dσij
+ dσij
(1 − ∆) .

(2.126)
(2.127)

(2.128)
(2.129)

α=S,C,SC

result in a generating MC@NLO functional with the same formal accuracy as that of
eq. (2.121). It is clear that, while this conclusion holds regardless of the form of ∆, provided

– 49 –

JHEP07(2014)079

which implies

## PDF page 52

that the conditions in eqs. (2.126) and (2.127) are satisfied, from the physical viewpoint
one would identify ∆ with a suitable combination of Sudakovs, whose explicit forms would
ideally be extracted from the same PSMC one interfaces to. Although at present there is no
straightforward way to obtain (numerically) the Sudakovs from a PSMC, there is no reason
of principle which prevents the implementation of such a possibility in future versions of
modern PSMCs. In the meanwhile, MadGraph5 aMC@NLO will have the means to test
eqs. (2.128) and (2.129), by using the analytical expression for the Sudakovs which are
currently used in the context of the FxFx NLO merging method (see section 2.4.5).
Merging samples at the NLO: FxFx

In this section, we present a brief review of the FxFx procedure [191], whose aim is that
of improving, by systematically including PSMC matching at the NLO, the multi-leg treelevel merging techniques established in the course of the past decade, such as CKKW,
CKKW-L, and MLM (see refs. [145–148, 192–197]). The key word here is merging, which
identifies the following problem. If one obtains hard events from the processes:
I1 + I2 −→ S + i partons ,

(2.130)

where S is a set of p particles which does not contain any QCD massless partons, how does
one match them to PSMCs when different i values (i.e., different final-state hard-process
multiplicities) are simultaneously considered? The core of the problem is the avoidance
of double counting; note that this is on top of, and more complicated than, the doublecounting problem that one faces when fixing i in eq. (2.130), and which is a matching (not
a merging) issue. While the formulation of the problem of merging is independent of the
perturbative order (i.e., of the accuracy to which the cross sections of the processes in
eq. (2.130) are computed), its solution is not, being strictly connected with the adopted
matching strategy. NLO (and beyond) mergings are thus inherently more complicated than
LO ones, because LO-matching is basically trivial; they have attracted a significant amount
of attention lately [184, 191, 198–207]. The quickest way to realise this is that of considering
the tree-level matrix element associated with the process in eq. (2.130); this will give the
Born contribution to that process, but at the same time it will also be needed at the NLO
as real-emission contribution to a process whose Born features a S + (i − 1) partons final
state. Such a double role of a given matrix element is specific to an NLO merging, and is
absent at the LO.
This example of the tree-level matrix-element double role suggests a way to tackle
the NLO-merging problem. In particular, in view of the fact that, in the context of a
given calculation, the perturbative accuracy of the prediction for an observable is larger
the more inclusive the observable, one wants to use as much as is possible an i-parton
tree-level matrix element as a Born, rather than as a real-emission, contribution. The
role of hard emissions will thus be mainly played by the Born’s associated with processes
with larger multiplicities, while for any given multiplicity the real-emission contributions
will mostly provide the correct (NLO) normalisation. Because the MC@NLO formalism
is designed to perturb in a minimal way both the underlying matrix-element description
and the PSMC one uses for showering events, the above scheme essentially corresponds to

– 50 –

JHEP07(2014)079

2.4.5

## PDF page 53

limiting the hardness of H-event emissions. Technically, this can be achieved by simply
exploiting the D function introduced in eq. (2.113), and by applying analogous conditions
at the matrix element level. In order to do so, it is convenient (and particularly sensible
physics-wise) to re-interpret the parameters µi of eq. (2.113) in the following way:
µ ≤ µ1

soft (MC − dominated),

µ1 < µ ≤ µ2

intermediate,

hard (ME − dominated).

µ > µ2

dn ≤ dn−1 ≤ . . . ≤ d2 ≤ d1 .

(2.131)

It will also turn out to be convenient to define
dj =

√

ŝ ,

j ≤ 0,

(2.132)

√
with ŝ the parton c.m. energy, i.e. the largest energy scale available event-by-event. Since
the function D determines rather directly the way in which the various partonic processes
of eq. (2.130) are combined, the results of variations of the parameters that enter into it can
be associated with the systematics of the merging procedure (and not of the matching one,
as is the case for the unmerged cross sections discussed in section 2.4.4). This is particularly
straightfoward, and totally analogous to what is typically done at the LO, when one chooses
a sharp D function, in which case µQ has to be seen as the merging scale.
We now limit ourselves to reporting the final forms of the short-distance cross sections
necessary to implement the FxFx merging scheme; the interested reader can find more
details in ref. [191]. We denote by N the largest light-parton multiplicity at the Born level
that we consider (therefore, N is the largest value that i can possibly assume in eq. (2.130)).
The cross sections given below are the analogues of those in eqs. (2.118) and (2.119), i.e.,
at fixed real-emission process and FKS pair; in the present section, we understand these
quantities, lest we clutter the notation with unnecessary details. On the other hand, each
H- or S-event contribution or short-distance cross section will carry an index, equal to the
number of final-state particles in the corresponding hard process (at the Born level), this

– 51 –

JHEP07(2014)079

Note that in the case of a sharp D function, eq. (2.114), the intermediate region collapses
to a zero-measure set. Once one has defined hard and soft mass scales, one needs to define
a way to measure the hardness; because of the fact that NLO corrections will be computed,
it is mandatory that such a measure be IR-safe. The easiest way to achieve this is that
of employing quantities that arise from a jet-reconstruction algorithm. We denote by dj
the scale (with canonical dimension equal to one, i.e. mass) at which a given S+partons
configuration passes from being reconstructed as a j-jet one to being reconstructed as a
(j − 1)-jet one, according to a kT jet-finding algorithm [144] (in other words, there are j
jets of hardness dj − ε, and (j − 1) jets of hardness dj + ε, with ε arbitrarily small). In
general, for n final-state partons one will have

## PDF page 54

information being crucial in all merging procedures. We have:
]
[ ∑
(H)
(NLO,α)
(MC,0)
(S)
dσ̄p+i
=
dσp+i
+ dσp+i
D(di+1 (Kp+i ))

(2.133)

α=S,C,SC

α=S,C,SC

×

(

(S)
1 − D(dN (Kp+N ))

)

(

(S)
dN −1 (Kp+N ) − µ2

)

,
)
(
(H)
(H)
(NLO,E)
(H)
1 − D(dN (Kp+N )) Θ dN −1 (Kp+N ) − µ2
= dσp+N
dσ̄p+N
(
) (
)
(S)
(S)
(MC,0)
−dσp+N
1 − D(dN (Kp+N )) Θ dN −1 (Kp+N ) − µ2 ,
(

Θ

)

(2.136)

where in eqs. (2.133) and (2.134) one has 0 ≤ i < N , and in writing the MC counterterms we have understood the G dependence as given in eq. (2.117), which is irrelevant for
the sake of the present discussion. The MC@NLO cross section defined by eqs. (2.133)
and (2.134) (eqs. (2.135) and (2.136)), and its analogue that we shall introduce later, is
called the i-parton (N -parton) sample. With the cross sections above, one defines the FxFx
generating functional:
FFxFx =

p+N
∑
n=p

(n)

FFxFx ,

)
(
(n)
FFxFx = FMC Kn(H)

(2.137)
)
(
dσ̄n(S)
dσ̄n(H)
+ FMC Kn(S)
.
dχBj dχn+1
dχBj dχn+1

(2.138)

Note that eq. (2.138) and eq. (2.121) are formally identical (as was said above, the sums
on the r.h.s. of eq. (2.121) are understood here), the difference being in the form of the
short-distance cross sections. Equation (2.137) implies that the FxFx generating functional is the incoherent sum of MC@NLO generating functionals, each of which incorporates FxFx-specific type of cuts but that are otherwise fully analogous to their non-merged
counterparts. This renders it straightforward to implement the FxFx merging prescription
into MadGraph5 aMC@NLO.
As was discussed in ref. [191], the formulation of FxFx according to eq. (2.138) can be
supplemented by a Sudakov suppression, in keeping with what is done at the LO in the
CKKW(-L) and MLM methods. The modifications of the short-distance cross sections are
in fact rather minimal, and amount to what follows:
)
] (
[
(S)
(S)
(∆)
(S)
(S)
(2.139)
dσ̂p+i
= dσ̄p+i
+ dσp+i ∆i µi,min , µi,max ,
(
)
(H)
(H)
(H)
(H)
(2.140)
dσ̂p+i
= dσ̄p+i
∆i µi,min , µi,max ,

(S)
(H)
with dσ̄p+i
and dσ̄p+i
defined in eq. (2.133) (for i < N ) or eq. (2.135) (for i = N ), and in
eq. (2.134) (for i < N ) or eq. (2.136) (for i = N ) respectively. ∆i is a suitable combination

– 52 –

JHEP07(2014)079

)
) (
(
(S)
(S)
× 1 − D(di (Kp+i )) Θ di−1 (Kp+i ) − µ2 ,
)
[
(
) (
(H)
(H)
(H)
(NLO,E)
(2.134)
dσ̄p+i
= dσp+i
1 − D(di (Kp+i )) Θ di−1 (Kp+i ) − µ2
)]
) (
(
(H)
(S)
(S)
(MC,0)
−dσp+i
1 − D(di (Kp+i )) Θ di−1 (Kp+i ) − µ2 D(di+1 (Kp+i )) ,
]
[ ∑
(MC,0)
(NLO,α)
(S)
+ dσp+N
(2.135)
dσp+N
=
dσ̄p+N

## PDF page 55

(1)

where only the Born matrix element contribution is kept. By ∆i we have denoted the
O(αS ) term in the perturbative expansion of ∆i . It should be clear that ∆i satisfies
eqs. (2.126) and (2.127); therefore, a by-product of the Sudakov-improved FxFx merging
procedure (which we regard as our “best” FxFx scheme, and is thus the default in MadGraph5 aMC@NLO) is the possibility of testing the alternative (non-merged) MC@NLO
formulation presented in eqs. (2.128) and (2.129).
We conclude this section by discussing two arguments of general relevance to NLOmerging techniques, and which may have significant bearings on their phenomenological
predictions: unitarity, and merging systematics. In the context of merging, imposing a
unitarity condition means that the fully-inclusive merged cross section (i.e., the sum over
all i’s of the i-parton-sample predictions) is equal to the total rate of the unmerged 0parton sample.34 In FxFx unitarity is not imposed, for the reasons we shall now explain.
One of the advantages of unitarity is the fact that the merging scale µQ can be chosen35
in an arbitrarily-large range, whereas in non-unitary approaches this is not possible, and a
sensible choice (which takes into account the hardness of the process, and the fact that µQ
must itself be hard) is always arbitrary to a certain extent. Such a benefit of unitarity has
however a less-pleasant side. Namely, in the general context of resummed computations
matched with fixed orders, constraints on total rates contribute to significant modifications of matrix-elements predictions, in shape and absolute value, also in regions where
one would expect large-logarithms effects to be suppressed (the Higgs pT spectrum is a
spectacular example of this phenomenon — see e.g. figures 1 and 2 of ref. [208]). This is of
course acceptable, and actually constitutes a defining prediction of a matched formalism,
if all contributions to the latter are perturbatively consistent: an example is that of an
MC@NLO unmerged cross section, where the total rate is of O(αSb+1 ), which is the same
perturbative order to which both S and H events contribute. When unitarised-merging is
considered, the total rate is still imposed to be that of O(αSb+1 ); however, S- and H-event iparton samples (and their analogues within any merging formalism) are of O(αSb+i+1 ); this
mismatch of perturbative orders present for any i ≥ 1 might result in a bias (uniquely due
to the total-rate constraint) at the level of shapes, the stronger the larger i. Note that one
could impose the unitarity constraint using an NNLO total-rate prediction (O(αSb+2 )), were
34

We neglect here possible complications due to heavy-flavour thresholds, and to contributions to i-parton
samples that cannot be shower-generated starting from a lower multiplicity.
35
In principle; in practice, there may be efficiency issues, which are however not of concern here.

– 53 –

JHEP07(2014)079

of Sudakov form factors, the construction of which follows closely the CKKW prescription.
Further details, including the definition of the hard scales that enter these formulae can be
found in ref. [191]. Here, we limit ourselves to stressing the following fact: while for the
processes studied in ref. [191] the flavour structure of ∆i had been worked out by hand, it
(∆)
has now been fully automated in MadGraph5 aMC@NLO. The term dσp+i is necessary in
order not to spoil the formal NLO accuracy of the formalism:
)
(
(
) (
)
(1)
(S)
(S)
(S)
(S)
(∆)
(NLO,S)
dσp+i = −dσp+i
|Born 1 − D(di (Kp+i )) Θ di−1 (Kp+i ) − µ2 ∆i µi,min , µi,max ,
(2.141)
(NLO,S)
where dσp+i
|Born is the soft part of the NLO cross section, eqs. (2.45) and (2.46),

## PDF page 56

For what concerns the study of merging-scale systematics, we emphasise that the discussion presented above by no means justifies the practice of not being conservative with
the choice of µQ in non-unitary approaches. There is a particularly common misconception,
relevant when the physics one wants to study features a threshold for jet hardness (that we
(cut)
(cut)
shall denote by pT
henceforth): such a misconception entails choosing µQ < pT . The
(implicit) argument for this choice is that a tagged jet is by definition a hard quantity, and
(cut)
by setting µQ > pT
one might spoil the underlying NLO accuracy36 for the correspond(cut)
as a
ing jet cross section. Several observations are in order here. Firstly, the use of pT
criterion to determine µQ is a contradiction in terms: by definition, a merging prescription
is what allows one to use samples of hard events without knowing a priori for which observables they will be employed, in particular which minimal jet hardness will be imposed. The
fact that the merging is not perfect (i.e., it does not have zero systematics) just implies that
(cut)
(cut)
are not particularly sensible, and nothing else. Secondly,
and µQ ≫ pT
both µQ ≪ pT
(cut)
misunderstands the meaning of hardness, which is not absoa criterion based solely on pT
(cut)
lute, but relative. For example, a jet with pT
= 40 GeV can rightly be defined to be hard
in inclusive W production; the same jet is less hard in Higgs production, basically soft in tt̄
production, and certainly soft in the production of a 1-TeV Z ′ resonance. Indeed, it should
be obvious that it is always a ratio of mass scales (one of which is of the order of the intrinsic
hardness of the production process, essentially defined by the masses of the final-state par(cut)
ticles, and the other of the order of pT ), and never the absolute value of one such scale,
that matters: the argument of a logarithm is a dimensionless quantity. Thirdly, and related
(cut)
one might indeed spoil some underlying
to the previous item. When choosing µQ > pT
NLO description, and for a very good reason: such matrix-element-driven prediction may
36

Or the tree-level matrix element accuracy in the case of LO mergings, where this argument is also
applied.

– 54 –

JHEP07(2014)079

that available. This would marginally alleviate the problem above, but not solve it: firstly,
it merely shifts it to i ≥ 2, and secondly one still uses NLO-matched (and not NNLOmatched) i-parton samples which thus require, at the very least, to be re-normalised. The
counter argument is that, although a bias might indeed be present, it appears at perturbative orders which are in any case beyond accuracy. This is correct, but does not have
any implications on the presence of large logarithmic terms, that could enhance such contributions. More importantly, it is also an argument that can be used in the context of a
non-unitary approach, where it would apply chiefly to total rates (and, by construction, in
non-unitary approaches there is no bias due to total-rate constraints). In fact, the dependence on µQ of inclusive results can be used effectively in non-unitary mergings as a way to
arrive at a sensible µQ range, to be employed to assess the merging systematics of differential distributions. Examples of this, and of the fact that FxFx exhibits a rather small µQ
dependence, will be given in section 4.2. In conclusion, the arguments above can be argued
in different ways; it should be clear, however, that regardless of whether a merging approach
imposes or not unitarity, in those phase-space regions where matrix elements and PSMCs
will be vastly different the µQ dependence is bound to be large. In order to be able to study
such effects as locally as is possible, we prefer not to use unitarity arguments in FxFx.

## PDF page 57

(cut)

2.5

Spin correlations: MadSpin

In both SM physics and BSM searches the role of unstable particles, that are not directly
observable but (some of) whose decay products may be seen in detectors, is very prominent.
Let us consider the production of p unstable particles uk (k = 1, . . . p; for example, u1 = Z,
u2 = t, u3 = t̄, and so forth), each of which decays into nk particles d1,k , . . . dnk ,k , in
association with l stable particles s1 , . . . sl :
x + y −→ u1 (→ d1,1 + . . . dn1 ,1 + X1 ) + . . . up (→ d1,p + . . . dnp ,p + Xp ) +
s 1 + . . . s l + X0 .

(2.142)

It is convenient to regard eq. (2.142) as a parton-level quantity, so that x, y, and all the
particles in the sets Xk are gluons or light quarks; the contents of Xk depend on the
perturbative order considered,37 and need not be specified here. Equation (2.142) does not
properly define a process, but has the following intuitive meaning: it corresponds to the
37

And, in general, on the type of corrections. In order to be definite, we consider here the case of QCD.

– 55 –

JHEP07(2014)079

simply be irrelevant in the case of a strong scale hierarchy where pT
is much smaller
than the intrinsic hardness of the process, because there one believes the correct type of
prediction for jet observables to be rather a PSMC-dominated one. Even if the presence
of Sudakov suppression factors in the merged matrix elements may allow one to employ a
merging scale which is smaller than what naive expectations would suggest, still by choosing
(cut)
µQ < pT
one runs the risk of spoiling the underlying PSMC description of the lowestmultiplicity sample. In conclusion, given that a merging-scale choice necessarily represents
a non-perfect compromise between a matrix-element- and a PSMC-dominated prediction,
(cut)
for processes where a scale hierarchy is not overwhelmingly clear (i.e., when pT
is a
non-negligible fraction of the hardness of the production process), one must not decide beforehand whether it is either a matrix-element or a PSMC description which is suited best:
they are in principle both valid alternatives, and a sufficiently large range of µQ in the sur(cut)
rounding of pT
must be probed, lest one underestimates the merging-scale systematics.
A final technical remark: given that the work of ref. [191] has used HERWIG6 as
PSMC, and that the FxFx formalism naturally matches a pT -ordered shower, its use with
Pythia8 and Herwig++ does not pose any conceptual problems. In fact, a fully automatic
FxFx interface with Pythia8 has now been achieved, but is not part of the current public
MadGraph5 aMC@NLO release (the related, specific routine inside the Pythia8 code has
become available starting from v8.185). For this reason, the sample FxFx-merged results
which will be presented in section 4.2 will make use of HERWIG6. The FxFx-Pythia8
interface also paves the way for a fully analogous procedure, that will be carried out with
Herwig++. We also remind the reader that the FxFx method has so far been formulated
only for processes that do not feature light jets at the Born level of the lowest-multiplicity
sample, and that the merging of b-quark production processes has not been explicitly
studied. Although we believe that these cases can be treated with only minor modifications
(if any) w.r.t. the present implementation, we postpone their discussion to a future work.

## PDF page 58

contributions to the process
x + y −→ d1,1 + . . . dn1 ,1 + . . . d1,p + . . . dnp ,p + s1 + . . . sl + X ,
p
⋃
Xk ,
X =

(2.143)
(2.144)

k=0

x + y −→ u1 + . . . up + s1 + . . . sl + X0 ,
uk −→ d1,k + . . . dnk ,k + Xk

(2.145)
k = 1, . . . p .

(2.146)

As this notation suggests, the particles uk in eqs. (2.145) and (2.146) are regarded as finaland initial-state objects respectively, rather than as intermediate ones as in eq. (2.143). The
calculation of amplitudes in the narrow-width approximation can be done by employing
well-established spin-density-matrix techniques, which allow one to account for all spin
correlations (we remind the reader that the process of eq. (2.143) is said to have decay spin
correlations if its matrix elements depend non-trivially on the invariants di,k·dj,k for some k;
production spin correlations are present in the case of non-trivial dependences on dik ,k·di′ ′ ,k′ ,
k
for any ik and i′k′ with k ′ ̸= k, or on dik ,k ·sq , dik ,k ·x, dik ,k ·y and dik ,k ·X0 for some ik and k).

– 56 –

JHEP07(2014)079

whose Feynman diagrams feature an s-channel propagator for each of the p unstable particles uk , with one end of the propagator attached to a subdiagram that contains at least the
decay products d1,k , . . . dnk ,k (such a subdiagram is a tree at the leading order). These diagrams may be called p-resonant diagrams and, by extension, any diagram that features n
such propagator-plus-subdiagram structures will be called n-resonant (so that, by including
the case n = 0, all diagrams contributing to eq. (2.143) can be classified in this way). This
implies that it would be natural to associate with eq. (2.142) the matrix elements obtained
by considering only the p-resonant diagrams in their computations. Unfortunately, this is
not straightforward, since in general it violates gauge invariance. So the only possibility
is that of an operative meaning: thus, eq. (2.142) stands for the matrix elements relevant
to the process of eq. (2.143), subject to selection cuts whose purpose is that of forcing
the p-resonant diagrams to be numerically dominant. While this approach is the cleanest
possible from a theoretical viewpoint, it has an obvious problem of efficiency: the non-presonant contributions to eq. (2.143) might swamp the p-resonant ones; furthermore, the
matrix elements of eq. (2.143) are usually very involved. The difficulties mentioned above
can be overcome by observing that a computation that uses only p-resonant diagrams is
formally correct in the limit where all the widths of unstable particles vanish, Γuk → 0, ∀k
(narrow-width approximation, which can be systematically improved in the context of a
pole expansion [101, 209, 210]). An immediate consequence of the narrow-width approximation is that the amplitudes associated with parton emissions (i.e., beyond leading order)
from the decay products dik ,k do not interfere with those associated with emissions either
from di′ ′ ,k′ , for any k ′ ̸= k, or from any particle which is not a decay product. Hence,
k
higher-order corrections factorise, and can thus be sensibly considered separately for production and decay. This results in a significant simplification of the calculation, since in
the narrow-width approximation one can therefore write:

## PDF page 59

k=1

where U is a universal factor, and the matrix elements at the numerator and denominator
on the l.h.s. are the tree-level ones relevant to the processes of eqs. (2.143) (with p-resonant
diagrams only) and (2.145) (with X0 = X) respectively, and:
2
2 2
2
∆−1
uk = (puk − muk ) + (muk Γuk ) .

(2.148)

Note that the factors ∆−1
uk in eq. (2.147) cancel exactly the denominators of the unstableparticle propagators, so that the limit is indeed a finite quantity. The fact that the set X
of radiated partons is the same at the numerator and denominator in eq. (2.147) implies
that the two matrix elements are computed at the same relative order w.r.t. the leading
one; this allows one to correctly take into account the effects of hard radiation at the production level. Finally, the factor U depends only on the identities of the unstable particles
(and possibly on the decay kinematics), but is independent of the production process. It
is computed by considering the decays of eq. (2.146) at the LO (i.e., with Xk = ∅), in a
fully numerical manner by MadSpin.
38

In other words, the narrow-width approximation allows one to get rid of the non-p-resonant diagrams,
whereas the simplification mentioned here gives a prescription for the actual computation of the p-resonant
diagrams where one does not use spin-density matrices.
39
For an alternative method, based on the knowledge of the polarization states of the unstable particles
and on spin-density matrices, and which is adopted in Herwig++, see ref. [212].
40
When working at the LO, production spin correlations can be recovered not only by using MadSpin,
but also by adopting the so-called decay-chain syntax — see appendix B.1 for more details.

– 57 –

JHEP07(2014)079

When spin correlations effects are small or can be neglected, a further simplification
can be made, where one replaces the squared amplitudes associated with the p-resonant
diagrams relevant to eq. (2.143) with those relevant to the production (eq. (2.145)) and
decays (eq. (2.146)) separately.38 Despite being a priori rather crude, such a simplification
is very widely used in the context of PSMCs, since the narrow-width approximation is
more difficult to automate already at LO, and more so beyond LO. Besides, unweightedevent generation is significantly more efficient for the process of eq. (2.145) than it is for
that of eq. (2.143). The procedure is therefore that of generating (unweighted) events that
correspond to eq. (2.145), and then let the PSMC decay the unstable particles according
to eq. (2.146) (with Xk = ∅, i.e., at the leading order) during the shower phase. Note that
the PSMC must know how to handle these decays, which sometimes involve non-trivial
matrix elements (e.g., in top decays, or for H 0 → 2ℓ2ν). If this is not the case, decay spin
correlations are also incorrectly predicted.
In order to retain the advantages of the separation of production from decays at the
level of squared amplitudes, such as efficiency and ease of automation, without losing
the capability of predicting spin correlations, MadGraph5 aMC@NLO uses the method
introduced in ref. [211],39 and studied there for top and W decays in the SM, which has been
fully automated and extended to generic models in ref. [213]; the corresponding module in
the code has been dubbed MadSpin.40 The method is based on the following identity:
(
) p
(
)
M x + y → d1,1 + . . . dnp ,p + s1 + . . . sl + X ∏ −1
∆uk ≤ U {uk }pk=1 , (2.147)
lim
M (x + y → u1 + . . . up + s1 + . . . sl + X)
{Γuk }→0

## PDF page 60

– 58 –

JHEP07(2014)079

Equation (2.147) is used within a standard hit-and-miss procedure, that determines the
kinematics of the decay products dik ,k given that of the unstable particles uk . In practice,
unweighted events are first obtained for the process in eq. (2.145); then, for each of these
the phase-space of the decay products is sampled, and through hit-and-miss unweighted
events for the process in eq. (2.143) are obtained. It should be clear that the latter events
thus correctly incorporate the information on both production and decay spin correlations.
Furthermore, there is evidence that, at the NLO, eq. (2.147) gives a general better description of the exact result for eq. (2.143) than that of an NLO narrow-width prediction, in
spite of the LO-only treatment of the decays in the former. This has to do with the fact
that, in the narrow-width approximation, configurations where the virtuality of an unstable particle (as reconstructed from final-state objects) is larger than the particle mass are
suppressed both by αS (being due to hard NLO corrections) and by a kinematical factor —
for a recent discussion relevant to top physics, see section 3 of ref. [214]. Furthermore, the
NLO origin of these configurations implies that, in the case of the production of more than
one unstable particle, such off-shell effects can be possibly included only for one particle at
a time in the NWA. On the other hand, eq. (2.147) trivially allows one to include off-shell
effects without any kinematics suppression, already at the leading order, and for all unstable particles simultaneously. In particular, one starts by generating the virtualities of uk
according to a Breit-Wigner distribution (rather than using the pole masses), and employs
those in the generation of the momenta of the decay particles that enter the hit-and-miss
procedure mentioned above. In so doing, one may introduce back into the problem gaugeviolating terms formally of O(Γuk /muk ), i.e., within the accuracy of the method. So the
only potential issue might result from the numerical coefficients in front of such terms not
being of O(1). However, one can use eq. (2.147) to check that this is not the case; indeed,
the bound of that equation is a fairly good one, even for configurations where the virtuality
of some unstable particle is more than ten widths away from the pole mass.
We have so far tacitly assumed to deal with the most common and numerically-relevant
case in the SM, namely that of QCD corrections to the production of weakly-decaying
unstable particles. When one starts considering EW NLO effects, one may face a selfconsistency problem, due e.g. to the fact that the loop propagators relevant to EW vector
bosons would have to feature non-zero widths (through the complex mass scheme prescription), while the same particles would have to be treated as on-shell (owing to the Γuk → 0
limits) when appearing in the final state. Hence, in the context of a mixed-coupling expansion, or in general when width effects are induced by the same type of interactions which
are responsible for higher-order corrections, the method discussed in this section has to be
employed by carefully considering the characteristics of the production process.
The MadSpin module included in MadGraph5 aMC@NLO features a number of upgrades w.r.t. that presented in ref. [213]. The most important of these is that the phasespace generation is now handled by the Fortran code (rather than by a Python routine).
The determination of the maximum weight has been fully restructured as well; on top of
that, it has been noticed that using more events, but less phase-space points per event,
is more efficient (the defaults have changed from 20 and 104 to 75 and 400, respectively).
These two major improvements have resulted in a dramatic decrease of the running time

## PDF page 61

3

How to perform a computation

The theoretical background discussed in section 2 can be ignored if one is only interested
in obtaining phenomenological predictions. This is the attitude that will be taken in this
section, whose aim is that of giving the briefest documentation for the basic running of the
code, and thus to show its extreme simplicity and level of automation.
The MadGraph5 aMC@NLO package is self-contained (third-party codes are included
in the tarball — see appendix D for their complete list). The local directory where its
tarball is unpacked is called main directory; there is a miniminal (and optional) setup
to be done, as described in appendix A. In essence, the computation of a cross section
by MadGraph5 aMC@NLO consists of three steps: generation, output, and running. All
three steps are performed by executing on-line commands in the MadGraph5 aMC@NLO
shell,41 which can be accessed by executing from a terminal shell in the main directory the
following command:
./bin/mg5 aMC
The prompt now reads:
MG5 aMC>
which signals the fact that one is inside the MadGraph5 aMC@NLO shell. The three steps
mentioned above correspond to the following commands:
MG5 aMC> generate process
MG5 aMC> output
MG5 aMC> launch
respectively; here, process denotes the specific process one is interested into generating (see
appendix B.1 for full details on the syntax).
When generating a process, one must decide whether he/she is interested in including
or not including NLO effects. In fact, although by definition an NLO cross section does
include an LO part (the Born contribution), if NLO effects are not an issue it does not
make much sense to include their contributions only to discard them at run time, especially
in view of their being much more involved than their Born counterparts. Furthermore, the
majority of physics models (see section 2.1) have not yet been extended to include NLO
corrections, and in these cases the whole procedure could not even be conceived.
41

As in MadGraph5, scripting commands is of course possible.

– 59 –

JHEP07(2014)079

(by a factor of about 10). Furthermore, the former one has paved the way for lifting the
present limitation that restricts the code to dealing only with (a succession of) 1 → 2
decays. From the phenomenology viewpoint, two important novelties are the following.
Firstly, MadSpin now always writes the information on the polarization of final-state particles, gathered from the matrix elements, onto the LHE files. This implies, in particular,
that PSMCs, if equipped with a suitable module, can handle τ decays including exactly
all decay spin correlations, and also the production ones due to the diagonal terms of the
spin-density matrix. Secondly, one can now use a UFO model in the determination of the
decays which can be different from the one adopted in the computation of the short-distance
undecayed matrix elements.

## PDF page 62

For these reasons, we talk about LO-type and NLO-type generations, and we note
that these two types of generation give access to different running options. We shall discuss
their different merits in the following sects. 3.1 and 3.2 respectively. Before going into that,
we point out that an LO-type generation produces the same short-distance cross section
code (and hence the same type of physics) as that one would have obtained by running
MadGraph5. All possibilities that were available in MadGraph5 are still available in
MadGraph5 aMC@NLO; at the same time, it should be clear that, even in the context of an
LO-type generation, MadGraph5 aMC@NLO has a much wider scope than MadGraph5.
LO-type generation and running

♦ Generation
In the generation phase, MadGraph5 aMC@NLO constructs the cross section relevant
to the process given as input by the user, and thus performs the operations sketched in
section 2.1. For example, if one is interested in tt̄W + production in pp collisions at the
LO, one will need to execute the following command:
MG5 aMC> generate p p > t t~ w+
When generating a process, MadGraph5 aMC@NLO assumes the model to be the SM
(with massive b quarks); a different model can be adopted, by “importing” it before the
generation (see appendix B.1). For example, the generation of a pair of top quarks in
association with a pair of neutralinos (the latter denoted by n1) can be achieved as follows:
MG5 aMC> import model mssm
MG5 aMC> generate p p > t t~ n1 n1
♦ Output
When the process generation is complete, the relevant information is still in the computer
memory, and needs to be written on disk in order to proceed. This is done by executing
the command:
MG5 aMC> output MYPROC
where MYPROC is a name chosen by the user42 that MadGraph5 aMC@NLO will in turn
assign to the directory under whose tree the cross section of the process just generated
is written. We call such a directory the current-process directory, which is where all
subsequent operations will be performed. For more details on this and for an overview of
the structure of the current-process directory, see appendix A.
♦ Running
The running stage allows one to accomplish a variety of tasks, the most important of
which are the production of unweighted events, and the plotting of user-defined physical
observables. Regardless of the final product(s) of the run, MadGraph5 aMC@NLO will
42

Such a name may be omitted; in this case, MadGraph5 aMC@NLO will choose one. On the
other hand, there are a few names which are reserved, since they are interpreted as options of the output
command. See appendix B.6 for more details.

– 60 –

JHEP07(2014)079

3.1

## PDF page 63

start by integrating the cross section generated and written in the two previous steps. In
order to run MadGraph5 aMC@NLO, one executes the command:
MG5 aMC> launch
What is prompted afterwards opens an interactive talk-to (which, again, can be scripted)
that allows the user to choose among various options. This looks as follows:

We would like to emphasise that the structure of the above prompt will evolve in the near
future, and be made more similar to its NLO counterpart (see section 3.2); however, the general idea that underpins its use will remain the same, so that what follows has to be regarded
as an exemplification of the general features of the MadGraph5 aMC@NLO talk-to phase.
By entering 1, 2, 3, 4, or 5 at the prompt one toggles between the two values ON and OFF
of the corresponding feature. For example, by entering 1 one is prompted again with the
display above, except for the fact that pythia=OFF has now become pythia=ON. By entering
1 again, one gets back to pythia=OFF. By entering 0, or done, or by simply hitting return,
the talk-to phase ends, and MadGraph5 aMC@NLO starts the actual run. The defaults
shown above imply that MadGraph5 aMC@NLO will simply limit itself to integrating the
cross section, and to producing the required number of unweighted events. On the other
hand, by turning the various switches above to ON, one enables the following features.
pythia=ON: with such a setting MadGraph5 aMC@NLO will steer the showering of
the hard events previously generated, by employing Pythia6. However, it is crucial to bear
in mind that the same hard events can be showered with PSMCs other than Pythia6, but
in this case MadGraph5 aMC@NLO is not capable of steering the shower43 (the steering
of Pythia8 will soon become available). The user may have an independent installation of
Pythia6, but also install the code using the MadGraph5 aMC@NLO shell, by executing
the command install pythia-pgs.
pgs=ON: in this case, MadGraph5 aMC@NLO will also steer the run of the Pretty
Good Simulator (PGS) [215] after that of Pythia6 (i.e., first all events are showered and
hadronised, and next they are passed through the basic detector simulation as implemented by PGS). For this reason, when pgs=ON MadGraph5 aMC@NLO automatically
sets pythia=ON. Note, also, that when the MadGraph5 aMC@NLO shell is used to install
Pythia with the install pythia-pgs command, PGS is installed too.
43

This is not the case for NLO simulations — see later.

– 61 –

JHEP07(2014)079

The following switches determine which programs are run:
1 Run the pythia shower/hadronization:
pythia=OFF
2 Run PGS as detector simulator:
pgs=OFF
3 Run Delphes as detector simulator:
delphes=OFF
4 Decay particles with the MadSpin module:
madspin=OFF
5 Add weight to events based on coupling parameters: reweight=OFF
Either type the switch number (1 to 5) to change its default setting,
or set any switch explicitly (e.g. type ‘madspin=ON’ at the prompt)
Type ‘0’, ‘auto’, ‘done’ or just press enter when you are done.
[0, 4, 5, auto, done, madspin=ON, madspin=OFF, madspin, reweight=ON,...]

## PDF page 64

3.2

NLO-type generation and running

♦ Generation
The generation phase of an NLO-type generation has the same conceptual meaning of that
relevant to the LO case, described at the beginning of section 3.1. The syntax is also very
similar: adopting again the example of tt̄W + production in pp collisions, one will need to
execute the following command in order to include QCD NLO effects:
MG5 aMC> generate p p > t t~ w+ [QCD]
As one can see, the only difference w.r.t. the case of the LO-generation is in the presence
of the keyword [QCD] here. Fuller details on the syntax for NLO-type generation are given
in appendix B.1.
♦ Output
There is no conceptual or technical difference w.r.t. the case of an LO-type generation in
the output phase. Specifically, the command one will need to execute is the same as that
described in section 3.1:
MG5 aMC> output MYPROC
The same comments concerning the choice of MYPROC as made for LO simulations apply
here (see footnote 42).
♦ Running
Also in the case of an NLO-type generation, the running phase begins by integrating the
cross section generated and written in the two previous steps. There is an important
44

Or install Delphes2, if one wanted to use the older Delphes 2 [217] version.

– 62 –

JHEP07(2014)079

delphes=ON: this allows one to steer the run of Delphes 3 [216] for a fast detector simulation. Delphes can also be installed through the MadGraph5 aMC@NLO shell
with the command install Delphes.44 As for switch number 2, when delphes=ON MadGraph5 aMC@NLO sets automatically pythia=ON.
madspin=ON: by doing so, one includes production spin correlations by means of MadSpin (see section 2.5). Note that the decay-chain syntax (see appendix B.1) is actually
faster and features a better approximation of the exact cross section than MadSpin, which
is thus more conveniently used in the context of NLO simulations.
reweight=ON: instructs MadGraph5 aMC@NLO to store in the LHE file information to be used later within the matrix-element reweighting procedure, for example relevant to assessing the impact of different theoretical assumptions (see section 2.3.3 and
appendix B.5).
When switches 1–5 are set as desired by the user and 0, or done, or <return> are
entered, MadGraph5 aMC@NLO proceeds with the run, whose first stage is that of giving
the user the possibility of modifying the various inputs relevant to the options selected
above. Such inputs, and the * card.dat files where they are stored, have a self-explanatory
meaning, and we will not discuss them in detail here.

## PDF page 65

The following switches determine which operations are executed:
1 Perturbative order of the calculation:
order=NLO
2 Fixed order (no event generation and no MC@[N]LO matching):
fixed order=OFF
3 Shower the generated events:
shower=ON
4 Decay particles with the MadSpin module:
madspin=OFF
Either type the switch number (1 to 4) to change its default setting,
or set any switch explicitly (e.g. type ‘order=LO’ at the prompt)
Type ‘0’, ‘auto’, ‘done’ or just press enter when you are done.
[0, 1, 2, 3, 4, auto, done, order=LO, order=NLO,...]
By entering 1, 2, 3, or 4 at the prompt one toggles between the two values of the corresponding feature (which are NLO and LO for 1, and ON or OFF for 2–4). For example,
by entering 2 one is prompted again what is displayed above, except for the fact that
fixed order=OFF has now become fixed order=ON. By entering 2 again, one gets back
to fixed order=ON. By entering 0, or done, or by simply hitting return, the talk-to phase
ends, and MadGraph5 aMC@NLO starts the actual runs.
It is the combinations of the values of the switches 1 and 2 that control which kind of
computation the program will perform. More explicitly, we have:
−→
NLO+PS and FxFx-merged45
(order=NLO,fixed order=OFF)
(order=NLO,fixed order=ON)
−→
fNLO
(order=LO,fixed order=OFF)
−→
LO+PS
(order=LO,fixed order=ON)
−→
fLO
One need not be suprised by the fact that LO+PS and fLO results can be obtained following
an NLO-type generation, since all the LO information is obviously there, being part of the
45

We remind the reader that i-parton samples, the contributions to an FxFx cross section of a given
multiplicity, are nothing but unmerged NLO+PS samples with some extra damping factors, which are
included by MadGraph5 aMC@NLO through a parameter (ickkw) in an input card.

– 63 –

JHEP07(2014)079

difference w.r.t. the LO case that must be stressed here. Namely, at the LO the shortdistance cross sections relevant to LO+PS and to fLO computations are identical. This
is not the case at the NLO: the MC@NLO cross sections used in NLO+PS computations
are different from the fixed-order ones used in fNLO computations (the former contain the
MC counterterms, the latter do not; the former can be unweighted, the latter cannot —
see section 2.4.4 for more details). However, when MadGraph5 aMC@NLO generates and
outputs a process, it writes both cross sections, and in so doing allows the user to choose
at runtime which type of computation to perform. In other words, after having generated
a process and used it to obtain (say) fNLO results, there is no need to re-generate it to
obtain NLO+PS results: it is sufficient to run MadGraph5 aMC@NLO again.
In order to run MadGraph5 aMC@NLO, one executes the same command as that relevant
to the LO-type generation:
MG5 aMC> launch
However, what is prompted afterwards opens an interactive talk-to which is different from
the one of the LO-type generation. In particular, one now obtains what follows:

## PDF page 66

3.2.1

(N)LO+PS results

The aim of this section is that of giving some details on the (N)LO+PS runs that follow an NLO-type generation. We recall that (N)LO+PS results are obtained by setting
fixed order=OFF, and the perturbative order is assigned according to the value of the
switch order (see section 3.2).
There are two types of objects46 that may be obtained with an (N)LO+PS run:
1. One or two files of unweighted events at the hard-subprocess level.
2. One file that collects results at the end of the shower, be them in the form of histograms, or n-tuples, or events; we call it MC.output.
The first of the files in 1 is the result of the integration of the short-distance partonic cross
section performed by MadGraph5 aMC@NLO. The second file is present only in the case
when MadSpin is used (madspin=ON), and results from feeding the former file to MadSpin.
These two files will be found under the current-process directory tree:
46

There are actually several other auxiliary files produced by MadGraph5 aMC@NLO, whose role
is however not important here. See appendix A for more details.

– 64 –

JHEP07(2014)079

NLO cross section. Rather, one may wonder why these options are not disabled, since they
lead to the same physics as a run that follows an LO-type generation. A discussion on this
point will be given in section 3.3; here, we limit ourselves to giving the shortest answer,
which is the following: the access to both LO and NLO results within the same generation
procedure (i.e., in the same current-directory process) guarantees an extremely easy and
swift comparison between them.
Switch 3 controls whether one employs MadGraph5 aMC@NLO to steer the showering
of hard-subprocess events previously generated (shower=ON) or not (shower=OFF). We shall
give a more extended discussion about this point in section 3.2.1. Here, we would like to
stress one crucial point: if the hard events are relevant to an NLO+PS run, they do not
have any physical meaning unless they are showered. Hence, one is free to use or not use
MadGraph5 aMC@NLO for showering them, but shower them he/she must. Note that
this is not the case for LO+PS hard events, although of course shower or not shower them
leads to different types of physics (in particular, observables constructed with unshowered
LO+PS hard events are the same as those resulting from an fLO computation).
Finally, switch 4 allows one to decide whether to include production spin correlations by means of MadSpin (see section 2.5). Since the method works starting from unweighted events, MadSpin is disabled when a fixed-order run is selected (in other words, the
inputs fixed order=ON and madspin=ON are incompatible, and MadGraph5 aMC@NLO
will automatically prevent the user from making such a choice; this is not necessary when
order=LO, but it is done anyway in order to simplify things).
As in the case of an LO-type generation, after setting switches 1–4 to the desired values
and entering 0, or done, or <return>, MadGraph5 aMC@NLO proceeds with the run by
giving the user the possibility of modifying the various input cards relevant to the options
selected.

## PDF page 67

x + y −→ t + t̄ + W + (+z) ,

(3.1)

where x, y, and z are quarks or gluons.47 The integration of the cross section that results in
the actual events is performed once the values of the relevant parameters (such as particles
masses, collider energy, PDFs) are given in input by the user. The two primary input cards
are:
MYPROC/Cards/run card.dat
MYPROC/Cards/param card.dat
One can obtain an undecayed event file with some parameter settings, then change these
settings, integrate the cross section again, and obtain a second event file; the procedure
can be iterated as many times as one likes. Each run is identified by an integer number,
chosen by MadGraph5 aMC@NLO, which unambiguously names the directory where the
event files will be stored. So, in the example given above, we shall have nn=01 for the first
run, nn=02 for the second run, and so forth.
Each undecayed event file can be fed to MadSpin in order to obtain a decayed event
file. In order to do so, the user is expected to give in input to MadSpin the actual decay(s)
he/she is interested into, which can be done by means of the input card:
MYPROC/Cards/madspin card.dat
Using again the generation example given before, and supposing that one wants to study
the decays:
t → b e+ ν e ,
t̄ → b̄ e− ν̄e ,
W + → µ+ ν µ ,
(3.2)
then the decayed event file will contain events of the following kind:
x + y −→ b + e+ + νe + b̄ + e− + ν̄e + µ+ + νµ (+z) .

(3.3)

It is possible to run MadSpin multiple times, by feeding it with the same undecayed event
file and by changing the type of decays considered (e.g., semileptonic top decays after the
di-leptonic ones of eq. (3.2)). For each MadSpin run, MadGraph5 aMC@NLO will store
the decayed event file in a different directory — this is the reason for the integer number
mm in the example above, which is automatically assigned to each new run: so mm=1 will
identify the first MadSpin run, mm=2 the second, and so forth.
47

The parton z is present in the case of H events, and absent in S events [26].

– 65 –

JHEP07(2014)079

MYPROC/Events/run nn/events.lhe.gz
MYPROC/Events/run nn decayed mm/events.lhe.gz
Although of course MadSpin may not be used (or it may simply be not relevant, if the
generated process does not feature particles that decay), the above structure is the most
general, and hence we shall discuss it so as to encompass all cases. We shall call the two
files above the undecayed and decayed (hard-subprocess) event files, respectively; both files
are fully compliant with the recent Les Houches Accord v3.0 [218].
The undecayed event file will contain events whose particle content is the same as that
given as input during the generation step (up to one final-state parton at the NLO), i.e.,
using the example of section 3.2:

## PDF page 68

48

See http://amcatnlo.cern.ch −→ Help and FAQs −→ Special settings for the parton shower.
These codes are essentially frozen, so we expect no or very minor changes in the future. Should the
need arise to use versions different w.r.t. those included here, copy them to MYPROC/MCatNLO/srcHerwig
and MYPROC/MCatNLO/srcPythia, and write their names in MYPROC/MCatNLO/MCatNLO MadFKS.inputs. In
the case of Pythia6, the routines UPINIT, UPEVNT, PDFSET, STRUCTP, and STRUCTM need also be commented
out of the source code.
49

– 66 –

JHEP07(2014)079

In summary, directories that contain undecayed event files are identified by an integer
nn, which roughly speaking corresponds to a given choice of settings in run card.dat
and param card.dat. On the other hand, directories that contain decayed event files are
identified by a pair of integers (nn,mm), which correspond to a given choice of settings in
run card.dat, param card.dat, and madspin card.dat.
Both undecayed and decayed hard-subprocess event files are non physical (at the NLO),
and must be showered in order to obtain physical results. Such a showering can be done
without using MadGraph5 aMC@NLO, since it is nothing but the nowadays typical PSMC
run starting from an external (to the PSMC) LH-compliant event file. On the other hand,
MadGraph5 aMC@NLO can steer PSMC runs: this is convenient for a varienty of reasons, among which the most important are probably those of ensuring a full consistency
among the parameters used when integrating the cross section and those adopted by the
PSMC, and the correct setting of a few control switches in the PSMC itself.48 As was
explained in section 3.2, MadGraph5 aMC@NLO will steer the shower when shower=ON:
in this case, several of the features of the PSMC run can be controlled through a MadGraph5 aMC@NLO input card:
MYPROC/Cards/shower card.dat
The parameters not explicitly included in this card must be controlled directly in the
relevant PSMC, in the same way as one would follow in a PSMC standalone run.
The steering of the PSMC by MadGraph5 aMC@NLO also guarantees that the PSMC
adopted is consistent with that assumed during the integration of the short-distance cross
section. Indeed, it is important to keep in mind that NLO+PS events obtained with the
MC@NLO formalism are PSMC-dependent, and for this reason one of the input parameters in run card.dat is the name of the PSMC which will be eventually used to shower
the hard-subprocess events. This kind of consistency is the user’s responsibility in the case
of a PSMC not steered by MadGraph5 aMC@NLO. Finally, we point out that the most
recent versions of the source codes of the Fortran77 PSMCs (HERWIG6 and Pythia6)
are included in the MadGraph5 aMC@NLO tarball.49 On the other hand, the modern
C++ PSMC (Pythia8 and Herwig++) must be installed locally prior to running MadGraph5 aMC@NLO. The paths to their executables/libraries have to be included in the
setup file mg5 configuration.txt (see appendix A).
When steering of the PSMC by MadGraph5 aMC@NLO one will obtain, at the end
of the PSMC run, the file MC.output mentioned in item 2 at the beginning of this section.
By default (i.e., if the user does not write his/her own analysis) this file will contain the
full event record of each showered event (in StdHEP format for Fortran MCs, and in HepMC
format for C++ PSMCs), and it will be named as follows:
MYPROC/Events/run */events MCTYPE ll.hep.gz

## PDF page 69

3.2.2

f(N)LO results

As was discussed in section 3.2, fixed-order results can be obtained with MadGraph5 aMC@NLO by setting fixed order=ON, with the perturbative order assigned according to the value of the switch order.
We remind the reader that an NLO computation not matched to a parton shower
cannot produce unweighted events, since the matrix elements are not bounded from
50

Note that in general pp ̸= ll: for example, a PSMC run may not create an StdHEP event record, in
which case pp would be increased, while ll would not.
51
Which contain several ready-to-run templates.

– 67 –

JHEP07(2014)079

Here, the run * directory is one of those introduced before; MC.output is moved to the same
directory where one finds the hard-subprocess event file fed to the PSMC during the course
of the run. MCTYPE is a string equal to the name of the PSMC used, and ll is an integer,
chosen by MadGraph5 aMC@NLO, that allows one to distinguish different files obtained
by showering the same hard-event file multiple times (for example by changing the shower
parameters). Any other output created by the PSMC (such as its standard output, which
would be printed on the screen during an interactive run) will be found in the directory:
MYPROC/MCatNLO/RUN MCTYPE pp
with pp an integer that enumerates the various runs.50
While StdHEP full event records may be analysed off-line, they have the disadvantage
of using a very significant amount of disk space. It is very often more convenient to analyse
showered events on-the-fly, using the event kinematics and weight to construct observables
and fill the corresponding histograms. This can be done in a very flexible manner in the
PSMC runs steered by MadGraph5 aMC@NLO. The user’s analysis can be stored in one
of the directories51
MYPROC/MCatNLO/XYZAnalyzer
where the string XYZ depends on the PSMC adopted. The name of such an analysis, and
those of all its dependencies (be they in the form of either source codes or libraries) can be
given in input to MadGraph5 aMC@NLO at runtime, as parameters in shower card.dat.
It is clear that it is the user’s analysis that determines the format of MC.output. Since MadGraph5 aMC@NLO cannot know it beforehand, it will treat MC.output as any other standard file produced by the PSMC, which will thus be found in the directory RUN MCTYPE pp.
An exception is that of the topdrawer format (which is human readable); in this case,
MC.output will be named as follows:
MYPROC/Events/run */plot MCTYPE kk *.top
with again kk an integer that allows one to distinguish the outputs relevant to different
showering of the same hard-event file.
We conclude this section by mentioning the fact that when the launch command is
executed with madspin=ON and shower=ON (i.e., both undecayed and decayed events are
produced, the PSMC runs immediately follows the integration of the cross section, and it is
steered by MadGraph5 aMC@NLO) only the decayed event file will be showered. In order
to shower the undecayed event file, or to perform other shower runs, one needs to use the
MadGraph5 aMC@NLO shell command shower. Please see appendix B.1 for more details.

## PDF page 70

above in the phase space; unweighting events would require the introduction of unphysical
cutoffs that would bias predictions, and must therefore be avoided. The only thing one can
do is that of considering weighted events, namely parton-level kinematic configurations
supplemented by a weight (which is basically equal to the matrix element times a
phase-space factor). Such events, which are readily obtained when sampling the phase
space in the course of the integration of the cross section, can be either stored in a file or
used on-the-fly to predict physical observables. While we choose the latter option as our
default, we remark that the former can be easily implemented by the interested user, as
it will become clear in what follows.

MYPROC/FixedOrderAnalysis
which contains several templates, meant to be used as examples. As the templates show,
MadGraph5 aMC@NLO at present supports two output formats for user’s analyses —
Root and topdrawer (see appendix. A for more details about this). The analysis name and
the format of its output must be given in input to MadGraph5 aMC@NLO, which is done
by including them in the input card:
MYPROC/Cards/FO analyse card.dat
where the user will also be able to specify any other source file or library needed by the
analysis. Upon running, MadGraph5 aMC@NLO will produce the final-result file:
MYPROC/Events/run nn/MADatNLO.root
if the Root format has been chosen, and:
MYPROC/Events/run nn/MADatNLO.top
for the topdrawer format; these will contain plots for the observables defined by the user. As
in the case of NLO+PS runs, the integer nn will be chosen by MadGraph5 aMC@NLO in
a non-ambiguous way (it should be obvious that both (N)LO+PS and f(N)LO simulations
can be performed any number of times starting from a given generation, and nn will
allow one to distinguish their results). By default, if the user does not write an analysis,
MadGraph5 aMC@NLO will produce a file which will contain the predictions for the total
rate (possibly within the cuts, as specified in run card.dat and cuts.f).
In essence, the user’s analysis will have to construct the desired observables, given
in input the pair composed of a kinematic configuration and its corresponding weight,52
which are provided by MadGraph5 aMC@NLO. These pairs can be read from eq. (2.47):
(ij)
(ij)
for each choice of the random variables {χBj , χn+1 } that scan the phase space and Bjorken
52

Such a weight becomes an array of weights when the user asks MadGraph5 aMC@NLO to compute
scale and PDF uncertainties. See section B.3 for more details.

– 68 –

JHEP07(2014)079

The input parameters relevant to f(N)LO runs can be found in the same cards that
control NLO+PS runs, namely run card.dat and param card.dat. Since observables will
be plotted on the fly, the user is expected to write his/her own analysis (which is a trivial
task, in view of the rather small final-state multiplicities of parton-level computations).
This analysis must be written in Fortran (or at least it must include a Fortran front-end
interface to the user’s core analysis, written in a language other than Fortran) and stored
in the directory:

## PDF page 71

where

(NLO,α)
(NLO,α)
dσij
|non−Born = dσij

(NLO,S)
(NLO,S)
(NLO,S)
dσij
|Born + dσij
|non−Born = dσij
,

α = C, SC ,

(3.7)
(3.8)

(NLO,S)
and dσij
|Born is the contribution of the Born matrix elements to the soft-counterevent
weight. The user’s analysis must treat eqs. (3.4)–(3.6) precisely in the same way: this is an
essential condition which guarantees that infrared safety is not spoiled. In particular, to
any given histogram all of these weights must contribute (obviously, to the bins and subject
(S)
(E)
to the cuts determined by the respective kinematics configurations, Kn+1 and Kn+1 ), if the
NLO accuracy is to be maintained. Note, also, that the weights (3.4)–(3.6) are correlated,
and thus cannot be individually used in a statistical analysis as they would if they had
been the result e.g. of an unweighted-event procedure.
Thanks to the fact that the Born weight, eq. (3.6), is kept separate from the other
contributions to the NLO cross section, MadGraph5 aMC@NLO allows the user to plot,
during the course of the same run, a given observable both at the NLO accuracy (by using
eqs. (3.4)–(3.6)) and at the LO accuracy (by using eq. (3.6) only). In order to allow the
user’s analysis to tell eq. (3.6) apart from eqs. (3.4) and (3.5), MadGraph5 aMC@NLO will
tag these weights with an integer, equal to 3, 1, and 2 respectively. For explicit examples,
see one of the template analyses in MYPROC/FixedOrderAnalysis.
We conclude this section by pointing out that the writing of weighted events can be
seen as a special type of analysis. The flexibility inherent in the structure sketched above
should easily allow a user to write and exploit such an analysis. In this case, we also
note that, rather than associating a single weight with each event, one can use all of the
scale- and PDF-independent ones defined in ref. [125] (which are available as variables in
a common block) in order to be able to compute scale and PDF uncertainties through
reweighting. These uncertainties can obviously be included when plotting observables on
the fly — see appendix B.3.

3.3

Possibilities for LO simulations

As was mentioned in section 3, MadGraph5 aMC@NLO offers two ways to obtain LO
results. One is through an LO-type generation, where when executing the command
generate one does not include the keyword [QCD]; this is completely equivalent to

– 69 –

JHEP07(2014)079

x’s, MadGraph5 aMC@NLO will call the user’s analysis three times, with input pairs:


(NLO,E)
dσ
ij
(E)
,
Kn+1
(3.4)
,
(ij)
(ij)
dχBj dχn+1


(NLO,α)
∑
dσij
|non−Born
(S)
Kn+1
,
,
(3.5)
(ij)
(ij)
dχ
dχ
α=S,C,SC
n+1
Bj


(NLO,S)
dσ
|
Born
ij
(S)
Kn+1
,
,
(3.6)
(ij)
(ij)
dχBj dχn+1

## PDF page 72

4
4.1

Illustrative results
Total cross sections

In this section we present benchmark results for total rates (possibly within the cuts which
will be specified later), at both the LO and the NLO. These are fLO and fNLO results
respectively, with the former computed in the context of an NLO-type generation (see
section 3.3). On the one hand, the aim of this section is that of showing the extreme
flexibility and reach of MadGraph5 aMC@NLO: in keeping with our general philosophy,
no part of the code has been customised to the computation of any of the processes below.
The code has been run as is extracted from the tarball (apart from the occasional necessity
of defining some final-state cuts in cuts.f, in some cases relevant to (b-)jet production,
which are explicitly mentioned in the captions of tables 1–11). We stress that several of
these cross sections have never been computed before to NLO accuracy.
We summarise here the main physics parameters used in our runs; the complete list
of inputs, in the form of the input cards of MadGraph5 aMC@NLO, can be found by
visiting http://amcatnlo.cern.ch/cards paper.htm, which should render it particularly easy
to reproduce the results that follow.

– 70 –

JHEP07(2014)079

what one would do if using MadGraph5. The other is accessed through an NLO-type
generation, by using order=LO.
We stress once again that all of the capabilities of MadGraph5 are inherited by
MadGraph5 aMC@NLO. Therefore, if one is interested only in LO physics, there is no
reason to simulate it within an NLO-type generation (which in that case would simply
be a waste of time). This is also in view of the fact that many of the options available in
the context of an LO-type generation are disabled when an LO process is computed after
an NLO-type generation. The idea of LO runs in the context of NLO-type generation is
that of rendering the comparison between LO and NLO a completely trivial affair. Note,
for example, that the input cards relevant to LO- and NLO-type generations are different:
many of the cuts that are present in the former would simply not make sense in the latter
(owing to the necessity of being compliant with infrared safety). Also, one should bear in
mind that the functional form of αS used by MadGraph5 aMC@NLO (i.e., at one or two
loops) is determined by the set of PDFs employed in the runs. Therefore, when working
with an NLO-type generation, and assuming that fLO (or LO+PS) results are obtained
during the same run as their fNLO (or NLO+PS) counterparts, the former will be based
on NLO PDFs and two-loop αS (which is of course fully consistent with perturbation
theory, and actually the best option if one is interested in assessing the perturbative
behaviour of the partonic short-distance matrix elements).
In summary, both options for LO runs lead to exactly the same physics. However, by
running the code at the LO with its default inputs one generally does not obtain exactly
the same numbers, since the relevant input cards are tailored either to LO-type or to NLOtype generations, which have different necessities and emphases. Hence, we recommend to
consider fLO and/or LO+PS results obtained through NLO-type generation mainly in the
context of studies that feature fNLO and/or NLO+PS simulations as well.

## PDF page 73

• mH = 125 GeV, mt = 173.2 GeV.
• MSTWnlo2008 [219] PDFs with errors at 68%CL, nf = 4, 5. Note that these PDFs
are used to obtain the fLO results as well, and that they set the value of αS (mZ ).
• Central scale choice: µ0 = HT /2, with HT the scalar sum of the transverse masses
√
p2T + m2 of all final state particles.

• Scale variations: independent, 1/2µ0 < µR , µF < 2µ0 .

Final-state objects are defined as follows:
• Jets: anti-kT algorithm [220] with R = 0.5, pT (j) > 30 GeV, |η(j)| < 4.
• Photons: Frixione isolation [221] with R = 0.7, pT (γ) > 20 GeV, |η(γ)| < 2.
While MadGraph5 aMC@NLO can handle intermediate resonances by using the complex
mass scheme, in this section we consider W ’s, Z’s, and top quarks as stable, and thus
set their widths equal to zero. Furthermore, although matrix elements for loop-induced
processes (e.g. such as gg → ZZ), can be obtained with MadLoop, they have not been considered in this section. Apart from reporting the absolute values of the total cross sections,
the following tables also show (as percentages) scale and PDF uncertainties. These are
computed exactly but without re-running, by exploiting the reweighting method presented
in ref. [125]. Following ref. [68], Yukawa’s are renormalised with an on-shell scheme.
We tag the processes for which we are not aware of any fNLO result being available
in the literature with an asterisk. We stress that, in those cases where an fNLO prediction
had been previously obtained, the corresponding matching to PSMCs might not necessarily have been achieved; this is the typical situation for several of the high-multiplicity
reactions. On the other hand, for all processes presented in the tables below the corresponding NLO+PS event samples can be obtained with MadGraph5 aMC@NLO. Some
non-exhaustive examples will be given in section 4.2.
The following results are organised into broad classes of processes that share some
defining characteristic. In hadroproduction (with a c.m. energy of 13 TeV), we have considered vector bosons plus up to three light jets (table 1), vector boson pairs plus up to
two light jets (table 2), three vector bosons plus up to one light jet (table 3), four vector
bosons (table 4), light jets, b-jets, and top quarks, possibly in association with each other
(table 5), vector bosons in association with top or bottom quarks and light jets (table 6),
single top quarks in association with b quarks (four-flavour scheme53 ) and vector bosons
(table 7), Higgs and double-Higgs in association with (possibly multiple) light jets, vector
bosons and heavy quarks (tables 8 and 9). In e+ e− collisions (with a c.m. energy of 1 TeV),
we have considered light jets, possibly in association with heavy quarks (table 10), and top
quark pairs in association with (possibly multiple) vector or Higgs bosons (table 11).
53

Throughout this paper, we adopt standard definitions for the four- and five-flavour schemes. See
e.g. section 1 of ref. [222] for a recent short review.

– 71 –

JHEP07(2014)079

• Diagonal CKM matrix.

## PDF page 74

Process

Syntax

Cross section (pb)

Vector boson +jets
a.1
a.2
a.3
a.4
a.5
a.6
a.7
a.9
a.10

LO 13 TeV
p p > wpm

pp → W ± j

p p > wpm j

pp → W ± jjj

p p > wpm j j j

pp → W ± jj

p p > wpm j j

pp → Z

p p > z

pp → Zjj

p p > z j j

pp → γj

p p > a j

pp → Zj

p p > z j

pp → Zjjj

p p > z j j j

pp → γjj

p p > a j j

5

1.375 ± 0.002 · 10

2.045 ± 0.001 · 104
6.805 ± 0.015 · 103

1.821 ± 0.002 · 103

4.248 ± 0.005 · 104

7.209 ± 0.005 · 103

2.348 ± 0.006 · 103
6.314 ± 0.008 · 102

1.964 ± 0.001 · 104

7.815 ± 0.008 · 103

+15.4% +2.0%
−16.6% −1.6%
+19.7% +1.4%
−17.2% −1.1%
+24.5% +0.8%
−18.6% −0.7%
+41.0% +0.5%
−27.1% −0.5%
+14.6% +2.0%
−15.8% −1.6%
+19.3% +1.2%
−17.0% −1.0%
+24.3% +0.6%
−18.5% −0.6%
+40.8% +0.5%
−27.0% −0.5%
+31.2% +1.7%
−26.0% −1.8%
+32.8% +0.9%
−24.2% −1.2%

NLO 13 TeV
1.773 ± 0.007 · 105

2.843 ± 0.010 · 104
7.786 ± 0.030 · 103

2.005 ± 0.008 · 103

5.410 ± 0.022 · 104

9.742 ± 0.035 · 103

2.665 ± 0.010 · 103
6.996 ± 0.028 · 102

5.218 ± 0.025 · 104

1.004 ± 0.004 · 104

+5.2% +1.9%
−9.4% −1.6%
+5.9% +1.3%
−8.0% −1.1%
+2.4% +0.9%
−6.0% −0.8%
+0.9% +0.6%
−6.7% −0.5%
+4.6% +1.9%
−8.6% −1.5%
+5.8% +1.2%
−7.8% −1.0%
+2.5% +0.7%
−6.0% −0.7%
+1.1% +0.5%
−6.8% −0.5%
+24.5% +1.4%
−21.4% −1.6%
+5.9% +0.8%
−10.9% −1.2%

Table 1. Sample of LO and NLO rates for vector-boson production, possibly within cuts and in association with jets, at the 13-TeV LHC; we
also report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. Where relevant, the notation understands the sum
of the W + and W − cross sections, and wpm is a label that includes both W + and W − , defined from the shell with define wpm = w+ w-. All
cross sections are calculated in the five-flavour scheme. Results at the NLO accuracy for W/Z plus jets are also available in MCFM for up to
two jets [223–225], including heavy-flavour identification [226–230], and in POWHEG [231–233]. NLO cross sections for W plus three jets have
appeared in refs. [234, 235]. The BlackHat+SHERPA collaboration has provided samples and results for up to Z plus four jets and W plus five
jets at the NLO [236–240]. NLO+PS merged samples for W plus up to three jets are also available in SHERPA [241]. γ plus up to three jets
calculations have been presented in refs. [242, 243]. We do not show cross sections for EW-induced V plus two jets processes with V = γ, Z, W ± ,
which are available in VBFNLO [244] and have been studied in ref. [245].

JHEP07(2014)079

– 72 –

a.8

pp → W

±

## PDF page 75

Syntax
p p > w+ wp p > z z
p p > z wpm
p p > a a
p p > a z
p p > a wpm
p p > w+ w- j
p p > z z j
p p > z wpm j
p p > a a j
p p > a z j
p p > a wpm j
p p > w+ w+ j j
p p > w- w- j j
p p > w+ w- j j
p p > z z j j
p p > z wpm j j
p p > a a j j
p p > a z j j
p p > a wpm j j

Cross section (pb)
LO 13 TeV
NLO 13 TeV
+4.0% +1.9%
+5.0% +2.0%
1
1.028 ± 0.003 · 102 −4.5%
7.355 ± 0.005 · 10 −6.1% −1.5%
−1.4%
+3.1% +1.8%
+4.5% +1.9%
1
1
1.415 ± 0.005 · 10 −3.7%
1.097 ± 0.002 · 10 −5.6% −1.5%
−1.4%
+4.4% +1.7%
+3.6% +2.0%
1
4.487
±
0.013
·
10
2.777 ± 0.003 · 101 −4.7%
−4.4% −1.3%
−1.5%
+17.6% +2.0%
+22.1% +2.4%
6.593 ± 0.021 · 101 −18.8%
2.510 ± 0.002 · 101 −22.4%
−1.9%
−2.1%
+5.4% +1.8%
+9.9%
+2.0%
3.695 ± 0.013 · 101 −7.1%
2.523 ± 0.004 · 101 −11.2% −1.6%
−1.4%
+9.7% +1.5%
+2.0%
7.124 ± 0.026 · 101 −9.9%
2.954 ± 0.005 · 101 +9.5%
−1.3%
−11.0% −1.7%
+4.9%
+1.1%
+11.6%
+1.0%
3.730 ± 0.013 · 101 −4.9% −0.8%
2.865 ± 0.003 · 101 −10.0% −0.8%
+5.0% +1.1%
+10.9% +1.0%
4.830 ± 0.016 · 100 −4.8%
3.662 ± 0.003 · 100 −9.3%
−0.9%
−0.8%
+4.9% +0.9%
+11.6% +0.9%
1
1
2.086 ± 0.007 · 10 −4.8% −0.7%
1.605 ± 0.005 · 10 −10.0% −0.7%
+17.2% +1.0%
+20.3% +1.2%
2.292 ± 0.010 · 101 −15.1%
1.022 ± 0.001 · 101 −17.7%
−1.4%
−1.5%
+14.5% +1.0%
+7.3% +0.9%
0
1
8.310 ± 0.017 · 10 −12.8% −1.0%
1.220 ± 0.005 · 10 −7.4%
−0.9%
+13.7% +0.9%
+7.2% +0.9%
2.546 ± 0.010 · 101 −12.1%
3.713 ± 0.015 · 101 −7.1%
−1.0%
−1.0%
+10.5% +2.2%
+25.4% +2.1%
−1
−1
2.251 ± 0.011 · 10
1.484 ± 0.006 · 10
−10.6% −1.6%
−18.9% −1.5%
+25.4% +2.4%
+10.1% +2.5%
6.752 ± 0.007 · 10−2 −18.9%
1.003 ± 0.003 · 10−1 −10.4%
−1.7%
−1.8%
+27.2% +0.7%
+5.0% +0.7%
1
1
1.144 ± 0.002 · 10 −19.9% −0.5%
1.396 ± 0.005 · 10 −6.8% −0.6%
+5.8% +0.8%
+26.6% +0.7%
1.706 ± 0.011 · 100 −7.2%
1.344 ± 0.002 · 100 −19.6%
−0.6%
−0.6%
+3.1% +0.7%
+26.7% +0.7%
0
9.139
±
0.031
·
10
8.038 ± 0.009 · 100 −19.7%
−5.1% −0.5%
−0.5%
+8.8% +0.6%
+26.2% +0.6%
7.501 ± 0.032 · 100 −10.1%
5.377 ± 0.029 · 100 −19.8%
−1.0%
−1.0%
+6.5% +0.6%
+24.3% +0.6%
0
4.242
±
0.016
·
10
3.260 ± 0.009 · 100 −18.4%
−7.3% −0.6%
−0.6%
+3.6% +0.6%
+24.7% +0.6%
1.448 ± 0.005 · 101 −5.4%
1.233 ± 0.002 · 101 −18.6%
−0.7%
−0.6%

Table 2. Sample of LO and NLO rates for vector-boson pair production, possibly within cuts and in association with jets, at the 13-TeV LHC;
we also report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. See table 1 for the meaning of wpm. All cross
sections are calculated in the five-flavour scheme, except for processes b.1, b.7, and b.15, which are obtained in the four-flavour scheme to avoid
resonant-top contributions. NLO results for V V production have been known for some time [246–254, 256], are publicly available in MCFM and
in VBFNLO [244], and are matched to parton showers in MC@NLO [26] and POWHEG [257]. NLO results for V V with up to an extra jet have
been made available in POWHEG [258, 259]. NLO corrections to γγ plus up to three jets are also known [260–264]. Other available results are:
W + W − jj [255, 359], W ± W ± jj [265], W ± W ± jj (EW+QCD) [266], Zγj [267], W γjj [268], W Zjj [269], W γj [270, 271], W Zj [272]. We do not
show results for NLO corrections to EW-induced production of V V plus two jets, such as W ± W ∓ jj [273], W Zjj [274], and ZZjj [275], which can
also be obtained with POWHEG and VBFNLO.

JHEP07(2014)079

– 73 –

Process
Vector-boson pair +jets
b.1
pp → W + W − (4f)
b.2
pp → ZZ
b.3
pp → ZW ±
b.4
pp → γγ
b.5
pp → γZ
b.6
pp → γW ±
b.7
pp → W + W − j (4f)
b.8
pp → ZZj
b.9
pp → ZW ± j
b.10
pp → γγj
b.11∗ pp → γZj
b.12∗ pp → γW ± j
b.13
pp → W + W + jj
b.14
pp → W − W − jj
b.15
pp → W + W − jj (4f)
b.16
pp → ZZjj
b.17
pp → ZW ± jj
b.18
pp → γγjj
∗
b.19
pp → γZjj
b.20∗ pp → γW ± jj

## PDF page 76

Syntax
p p > w+ w- wpm
p p > z w+ wp p > z z wpm
p p > z z z
p p > a w+ wp p > a a wpm
p p > a z wpm
p p > a z z
p p > a a z
p p > a a a
p p > w+ w- wpm j
p p > z w+ w- j
p p > z z wpm j
p p > z z z j
p p > a w+ w- j
p p > a a wpm j
p p > a z wpm j
p p > a z z j
p p > a a z j
p p > a a a j

Cross section (pb)
LO 13 TeV
NLO 13 TeV
+5.1% +1.6%
+0.0% +2.0%
−1
2.109 ± 0.006 · 10−1 −4.1%
1.307 ± 0.003 · 10
−1.2%
−0.3% −1.5%
+6.3% +1.6%
+0.8% +2.1%
−1
−2
1.679 ± 0.005 · 10
9.658 ± 0.065 · 10
−5.1% −1.2%
−1.1% −1.6%
+6.8% +1.5%
+1.0% +2.0%
5.550 ± 0.020 · 10−2 −5.5%
2.996 ± 0.016 · 10−2 −1.4%
−1.1%
−1.6%
+0.0% +1.9%
+2.7% +1.9%
−2
−2
1.085 ± 0.002 · 10
1.417 ± 0.005 · 10
−0.5% −1.5%
−2.1% −1.5%
+1.9% +2.0%
+1.4%
1.427 ± 0.011 · 10−1 −2.6%
2.581 ± 0.008 · 10−1 +5.4%
−1.5%
−4.3% −1.1%
+4.4% +1.9%
+7.6% +1.0%
−2
−2
2.681 ± 0.007 · 10
8.251 ± 0.032 · 10
−5.6% −1.6%
−7.0% −1.0%
+0.8% +1.9%
+7.2% +1.2%
−2
4.994 ± 0.011 · 10
1.117 ± 0.004 · 10−1 −5.9%
−1.4% −1.6%
−0.9%
+2.8% +1.8%
+2.0% +1.9%
−2
3.118
±
0.012
·
10
2.320 ± 0.005 · 10−2 −2.9%
−2.7% −1.4%
−1.5%
+4.5% +1.7%
+5.6% +1.9%
4.634 ± 0.020 · 10−2 −5.0%
3.078 ± 0.007 · 10−2 −6.8%
−1.3%
−1.6%
+11.8% +1.4%
+9.8% +2.0%
−2
3.441
±
0.012
·
10
1.269 ± 0.003 · 10−2 −11.0%
−11.6% −1.5%
−1.8%
+5.2% +1.0%
+15.0% +1.0%
1.197 ± 0.004 · 10−1 −5.6%
9.167 ± 0.010 · 10−2 −12.2%
−0.8%
−0.7%
+4.5% +1.0%
+15.6% +1.0%
−1
1.066
±
0.003
·
10
8.340 ± 0.010 · 10−2 −12.6%
−5.3% −0.7%
−0.7%
+4.8% +1.0%
+16.1% +1.0%
3.660 ± 0.013 · 10−2 −5.6%
2.810 ± 0.004 · 10−2 −13.0%
−0.7%
−0.7%
+4.9% +1.4%
+14.3% +1.4%
6.341 ± 0.025 · 10−3 −5.4%
4.823 ± 0.011 · 10−3 −11.8%
−1.0%
−1.0%
+18.9% +1.0%
+13.4% +0.8%
3
1.233
±
0.004
·
10
1.182 ± 0.004 · 10−1 −11.2%
−19.9% −1.5%
−0.7%
+5.8% +0.7%
+11.8% +0.6%
5.807 ± 0.023 · 10−2 −5.5%
4.107 ± 0.015 · 10−2 −10.2%
−0.7%
−0.8%
+5.1% +0.8%
+14.4% +0.7%
−2
7.764
±
0.025
·
10
5.833 ± 0.023 · 10−2 −12.0%
−5.5% −0.6%
−0.6%
+12.5% +1.2%
+5.6% +1.2%
9.995 ± 0.013 · 10−3 −10.6%
1.371 ± 0.005 · 10−2 −5.5%
−0.9%
−0.9%
+10.9% +1.0%
+7.0% +1.0%
−2
1.372 ± 0.003 · 10−2 −9.4%
2.051
±
0.011
·
10
−0.9%
−6.3% −0.9%
+14.3% +0.9%
+12.8% +0.8%
1.031 ± 0.006 · 10−2 −12.6%
2.020 ± 0.008 · 10−2 −11.0%
−1.2%
−1.2%

Table 3. Sample of LO and NLO rates for triple-vector-boson production, possibly within cuts and in association with one jet, at the 13-TeV LHC;
we also report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. See table 1 for the meaning of wpm. All cross
sections are calculated in the five-flavour scheme, except for processes with at least two W bosons, where the four-flavour scheme is adopted to
avoid resonant-top contributions. Triple-vector-boson cross sections at the NLO have been computed in: Zγγ [267, 276], γγW ± [277], γZW ± [278],
W W γ and ZZγ [279], ZW W [358], ZZW and W W W [280, 358], γγγ [281, 282], ZZZ [283, 358]. The complete set of triple-vector-boson cross
sections at the NLO is also available in VBFNLO [244]. Except for γγW ± j and W + W − W ± j that have appeared in ref. [284] and ref. [285]
respectively, V V V j cross sections at the NLO have been computed here for the first time.

JHEP07(2014)079

– 74 –

Process
Three vector bosons +jet
c.1
pp → W + W − W ± (4f)
c.2
pp → ZW + W − (4f)
c.3
pp → ZZW ±
c.4
pp → ZZZ
c.5
pp → γW + W − (4f)
c.6
pp → γγW ±
c.7
pp → γZW ±
c.8
pp → γZZ
c.9
pp → γγZ
c.10
pp → γγγ
c.11
pp → W + W − W ± j (4f)
c.12∗ pp → ZW + W − j (4f)
c.13∗ pp → ZZW ± j
c.14∗ pp → ZZZj
c.15∗ pp → γW + W − j (4f)
c.16
pp → γγW ± j
∗
c.17
pp → γZW ± j
∗
c.18
pp → γZZj
∗
c.19
pp → γγZj
c.20∗ pp → γγγj

## PDF page 77

Process

Syntax

Cross section (pb)

Four vector bosons
∗

c.21

c.22∗
c.23∗
c.24∗
c.25∗
∗

c.26

c.27∗
c.29∗
c.30∗
c.31∗
c.32∗
c.33∗
c.34∗
c.35∗

−

+

pp → W W W W

LO 13 TeV
−

(4f)

p p > w+ w- w+ w-

pp → W + W − W ± Z (4f)

p p > w+ w- wpm z

pp → W + W − ZZ (4f)

p p > w+ w- z z

pp → W + W − W ± γ (4f)

p p > w+ w- wpm a

pp → W + W − Zγ (4f)

p p > w+ w- z a

+

−

pp → W W γγ (4f)

p p > w+ w- a a

pp → W ± ZZγ

p p > wpm z z a

pp → W ± γγγ

p p > wpm a a a

pp → ZZZγ

p p > z z z a

pp → Zγγγ

p p > z a a a

pp → W ± ZZZ

p p > wpm z z z

pp → W ± Zγγ

p p > wpm z a a

pp → ZZZZ

p p > z z z z

pp → ZZγγ

p p > z z a a

pp → γγγγ

p p > a a a a

−4

5.721 ± 0.014 · 10

6.391 ± 0.076 · 10−4

8.115 ± 0.064 · 10−4

4.320 ± 0.013 · 10−4
8.403 ± 0.016 · 10−4
−4

5.198 ± 0.012 · 10

5.862 ± 0.010 · 10−5
1.148 ± 0.003 · 10−4
1.054 ± 0.004 · 10−4
3.600 ± 0.013 · 10−5
1.989 ± 0.002 · 10−5
3.945 ± 0.007 · 10−5
5.513 ± 0.017 · 10−5
4.790 ± 0.012 · 10−5
1.594 ± 0.004 · 10−5

+3.7% +2.3%
−3.5% −1.7%
+4.4% +2.4%
−4.1% −1.8%
+2.5% +2.2%
−2.5% −1.7%
+4.4% +2.4%
−4.1% −1.7%
+3.0% +2.3%
−2.9% −1.7%
+0.6% +2.1%
−0.9% −1.6%
+5.1% +2.4%
−4.7% −1.8%
+3.6% +2.2%
−3.5% −1.7%
+1.7% +2.1%
−1.9% −1.7%
+0.4% +2.0%
−1.0% −1.6%
+3.8% +2.2%
−3.6% −1.7%
+1.9% +2.1%
−2.1% −1.6%
+0.0% +2.1%
−0.3% −1.6%
+2.3% +2.0%
−3.1% −1.6%
+4.7% +1.9%
−5.7% −1.7%

NLO 13 TeV
9.959 ± 0.035 · 10−4

1.188 ± 0.004 · 10−3

1.546 ± 0.005 · 10−3

7.107 ± 0.020 · 10−4
1.483 ± 0.004 · 10−3

9.381 ± 0.032 · 10−4

1.240 ± 0.004 · 10−4
2.945 ± 0.008 · 10−4
3.033 ± 0.010 · 10−4
1.246 ± 0.005 · 10−4

2.629 ± 0.008 · 10−5
5.224 ± 0.016 · 10−5
7.518 ± 0.032 · 10−5
7.103 ± 0.026 · 10−5
3.389 ± 0.012 · 10−5

+7.4% +1.7%
−6.0% −1.2%
+8.4% +1.7%
−6.8% −1.2%
+7.9% +1.5%
−6.3% −1.1%
+7.0% +1.8%
−5.7% −1.3%
+7.2% +1.6%
−5.8% −1.2%
+6.7% +1.4%
−5.3% −1.1%
+9.9% +1.7%
−8.0% −1.2%
+10.8% +1.3%
−8.7% −1.0%
+10.6% +1.1%
−8.6% −0.8%
+9.8% +0.9%
−8.1% −0.8%
+3.5% +2.2%
−3.0% −1.7%
+3.3% +2.1%
−2.7% −1.6%
+3.4% +2.0%
−2.6% −1.5%
+3.4% +1.6%
−3.2% −1.5%
+7.0% +1.3%
−6.7% −1.3%

Table 4. Sample of LO and NLO rates for quadruple-vector-boson production, possibly within cuts, at the 13-TeV LHC; we also report the
integration errors, and the fractional scale (left) and PDF (right) uncertainties. See table 1 for the meaning of wpm. All cross sections are calculated
in the five-flavour scheme, except the processes with at least two W bosons, where the four-flavour scheme is adopted to avoid resonant-top
contributions. For all processes in this table NLO QCD corrections have never been computed before.

JHEP07(2014)079

– 75 –

c.28∗

+

## PDF page 78

Syntax

Cross section (pb)

p p > j j
p p > j j j
p p > b b∼
p p > b b∼ j
p p > b b∼ j j
p p > b b∼ b b∼
p p > t t∼
p p > t t∼ j
p p > t t∼ j j
p p > t t∼ t t∼
p p > t t∼ b b∼

LO 13 TeV
+24.9% +0.8%
1.162 ± 0.001 · 106 −18.8%
−0.9%
+43.8% +1.2%
8.940 ± 0.021 · 104 −28.4%
−1.4%
+25.2% +1.5%
3.743 ± 0.004 · 103 −18.9%
−1.8%
+44.1% +1.6%
1.050 ± 0.002 · 103 −28.5%
−1.8%
+61.8% +2.1%
1.852 ± 0.006 · 102 −35.6%
−2.4%
+61.7% +2.9%
5.050 ± 0.007 · 10−1 −35.6%
−3.4%
+29.0% +1.8%
4.584 ± 0.003 · 102 −21.1%
−2.0%
+45.1% +2.2%
3.135 ± 0.002 · 102 −29.0%
−2.5%
+61.4% +2.6%
1.361 ± 0.001 · 102 −35.6%
−3.0%
+63.8% +5.4%
4.505 ± 0.005 · 10−3 −36.5%
−5.7%
+62.1% +2.9%
6.119 ± 0.004 · 100 −35.7%
−3.5%

NLO 13 TeV
+8.4% +0.7%
1.580 ± 0.007 · 106 −9.0%
−0.9%
+2.1% +1.1%
7.791 ± 0.037 · 104 −23.2%
−1.3%
+15.9% +1.5%
6.438 ± 0.028 · 103 −13.3%
−1.7%
+6.8% +1.5%
1.327 ± 0.007 · 103 −11.6%
−1.8%
+8.2% +2.0%
2.471 ± 0.012 · 102 −16.4%
−2.3%
+20.9% +2.9%
8.736 ± 0.034 · 10−1 −22.0%
−3.4%
+1.8%
6.741 ± 0.023 · 102 +9.8%
−10.9% −2.1%
+8.1% +2.1%
4.106 ± 0.015 · 102 −12.2%
−2.5%
+9.3% +2.4%
1.795 ± 0.006 · 102 −16.1%
−2.9%
+30.8% +5.5%
9.201 ± 0.028 · 10−3 −25.6%
−5.9%
+37.6% +2.9%
1.452 ± 0.005 · 101 −27.5%
−3.5%

Table 5. Sample of LO and NLO total rates for the production of heavy quarks and/or jets, possibly within cuts, at the 13-TeV LHC; we also
report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. Processes d.1 and d.2, as well as processes involving
at least a top pair, are computed in the five-flavour scheme. Processes that explicitly involve b-quarks in the final state are calculated in the
four-flavour scheme. For processes d.3–d.6 we require 2 (or 4) b-jets in the final state with |η| < 2.5. For processes d.1–d.6, we require the (b)-jets to
have pT > 80 GeV, with at least one of them with pT > 100 GeV. Calculations of cross sections at the NLO for this class of processes are available
in the literature as well as in public codes: from the seminal results for the hadroproduction of a heavy quark pair [286–290], to their NLO+PS
implementation in MC@NLO [172] and POWHEG [291], to tt̄j [292] (also including top decays [258, 293] and parton shower effects [294, 365]),
to the computation of tt̄jj [295]. Merged NLO+PS results for tt̄ plus jets are also available [191, 296, 297]. NLO results for three jets [298], four
jets [74], and up to five jets [299, 300] have been published. Two- and three-jet event generation is available in POWHEG [301, 302]. Calculations
for bb̄bb̄ [303, 304], tt̄bb̄ [305–307, 362], and tt̄tt̄ [308] production have appeared in the literature.

JHEP07(2014)079

– 76 –

Process
Heavy quarks and jets
d.1
pp → jj
d.2
pp → jjj
d.3
pp → bb̄ (4f)
∗
d.4
pp → bb̄j (4f)
d.5∗ pp → bb̄jj (4f)
d.6
pp → bb̄bb̄ (4f)
d.7
pp → tt̄
d.8
pp → tt̄j
d.9
pp → tt̄jj
d.10 pp → tt̄tt̄
d.11 pp → tt̄bb̄ (4f)

## PDF page 79

Syntax
p p > wpm b b∼
p p > z b b∼
p p > a b b∼
p p > wpm b b∼ j
p p > z b b∼ j
p p > a b b∼ j
p p > t t∼ wpm
p p > t t∼ z
p p > t t∼ a
p p > t t∼ wpm j
p p > t t∼ z j
p p > t t∼ a j
p p > t t∼ w+ wp p > t t∼ wpm z
p p > t t∼ wpm a
p p > t t∼ z z
p p > t t∼ z a
p p > t t∼ a a

Cross section (pb)
LO 13 TeV
NLO 13 TeV
+29.8% +1.5%
+42.3% +2.0%
8.162
±
0.034
· 102 −23.6%
3.074 ± 0.002 · 102 −29.2%
−1.2%
−1.6%
+19.9% +1.0%
+33.5% +1.0%
3
1.235
±
0.004
·
10
6.993 ± 0.003 · 102 −24.4%
−17.4% −1.4%
−1.4%
+33.7% +1.4%
+51.9% +1.6%
4.171 ± 0.015 · 103 −27.1%
1.731 ± 0.001 · 103 −34.8%
−1.9%
−2.1%
+27.0% +0.7%
+42.5% +0.7%
2
3.957
±
0.013
·
10
1.861 ± 0.003 · 102 −27.7%
−21.0% −0.6%
−0.7%
+21.0% +0.8%
+42.4% +0.9%
2.805 ± 0.009 · 102 −17.6%
1.604 ± 0.001 · 102 −27.6%
−1.0%
−1.1%
+18.9% +1.0%
+51.2% +1.0%
3
1.233
±
0.004
·
10
7.812 ± 0.017 · 102 −32.0%
−19.9% −1.5%
−1.5%
+11.2% +1.7%
+23.9% +2.1%
5.662 ± 0.021 · 10−1 −10.6%
3.777 ± 0.003 · 10−1 −18.0%
−1.3%
−1.6%
+9.7% +1.9%
+30.5% +1.8%
7.598 ± 0.026 · 10−1 −11.1%
5.273 ± 0.004 · 10−1 −21.8%
−2.2%
−2.1%
+9.8% +1.7%
+29.6% +1.6%
0
1.744
±
0.005
·
10
1.204 ± 0.001 · 100 −21.3%
−11.0% −2.0%
−1.8%
+11.2% +1.2%
+40.9% +1.3%
3.404 ± 0.011 · 10−1 −14.0%
2.352 ± 0.002 · 10−1 −27.1%
−0.9%
−1.0%
+7.0% +2.5%
+46.2% +2.7%
−1
−1
5.074
±
0.016
·
10
3.953 ± 0.004 · 10
−12.3% −2.9%
−29.5% −3.0%
+7.5% +2.2%
+45.4% +2.3%
1.135 ± 0.004 · 100 −12.2%
8.726 ± 0.010 · 10−1 −29.1%
−2.5%
−2.6%
+10.9% +2.1%
+30.9% +2.1%
−3
9.904
±
0.026
·
10
6.675 ± 0.006 · 10−3 −21.9%
−11.8% −2.1%
−2.0%
+10.6% +2.3%
+26.6% +2.5%
3.525 ± 0.010 · 10−3 −10.8%
2.404 ± 0.002 · 10−3 −19.6%
−1.6%
−1.8%
+10.3% +2.0%
+25.4% +2.3%
−3
3.927
±
0.013
·
10
2.718 ± 0.003 · 10−3 −18.9%
−10.4% −1.5%
−1.8%
+29.3% +1.7%
+7.9% +1.7%
1.349 ± 0.014 · 10−3 −21.1%
1.840 ± 0.007 · 10−3 −9.9%
−1.5%
−1.5%
+30.1% +1.7%
+9.7% +1.8%
−3
2.548 ± 0.003 · 10−3 −21.5%
3.656
±
0.012
·
10
−1.6%
−11.0% −1.9%
+28.4% +1.3%
+7.8% +1.4%
3.272 ± 0.006 · 10−3 −20.6%
4.402 ± 0.015 · 10−3 −9.7%
−1.1%
−1.4%

Table 6. Sample of LO and NLO total rates for the production of heavy quarks in association with vector bosons, possibly within cuts and
in association with jets, at the 13-TeV LHC; we also report the integration errors, and the fractional scale (left) and PDF (right) uncertainties.
Processes that explicitly involve b-quarks in the final state, and process e.13, are calculated in the four-flavour scheme, while all of the others are
in the five-flavour scheme. Results are available in the literature for W bb̄ [68, 309–312], Zbb̄ [68, 311, 313], tt̄γ [314], tt̄Z [68, 315, 316, 363, 364],
tt̄W [68, 316, 317] production. For the majority of the processes in this table, NLO corrections are calculated in this work for the first time.

JHEP07(2014)079

– 77 –

Process
Heavy quarks+vector bosons
e.1
pp → W ± bb̄ (4f)
e.2
pp → Z bb̄ (4f)
e.3
pp → γ bb̄ (4f)
∗
e.4
pp → W ± bb̄ j (4f)
∗
e.5
pp → Z bb̄ j (4f)
∗
e.6
pp → γ bb̄ j (4f)
e.7
pp → tt̄ W ±
e.8
pp → tt̄ Z
e.9
pp → tt̄ γ
∗
e.10
pp → tt̄ W ± j
∗
e.11
pp → tt̄ Zj
e.12∗ pp → tt̄ γj
e.13∗ pp → tt̄ W − W + (4f)
e.14∗ pp → tt̄ W ± Z
e.15∗ pp → tt̄ W ± γ
e.16∗ pp → tt̄ ZZ
e.17∗ pp → tt̄ Zγ
e.18∗ pp → tt̄ γγ

## PDF page 80

Process

Syntax

Cross section (pb)

Single-top
f.1
f.2
f.3
f.4
∗

f.5

∗

f.6

∗

f.8

∗

f.9

pp → tγj (t-channel)

pp → tZj (t-channel)

pp → tbj (t-channel, 4f)

pp → tbjγ (t-channel, 4f)

pp → tbjZ (t-channel, 4f)
pp → tb (s-channel, 4f)

pp → tbγ (s-channel, 4f)

pp → tbZ (s-channel, 4f)

p p > tt j $$ w+ wp p > tt a j $$ w+ wp p > tt z j $$ w+ wp p > tt bb j $$ w+ wp p > tt bb j a $$ w+ wp p > tt bb j z $$ w+ wp p > w+ > t b∼, p p > w- > t∼ b
p p > w+ > t b∼ a, p p > w- > t∼ b a
p p > w+ > t b∼ z, p p > w- > t∼ b z

+9.4% +0.4%
1.520 ± 0.001 · 10 −11.9%
−0.6%
+6.4% +0.9%
9.956 ± 0.014 · 10−1 −8.8%
−1.0%
+3.5% +0.9%
6.967 ± 0.007 · 10−1 −5.5%
−1.0%
+13.8% +0.4%
1.003 ± 0.000 · 102 −11.5%
−0.5%
+16.8% +0.8%
6.293 ± 0.006 · 10−1 −13.5%
−0.9%
+18.7% +1.0%
3.934 ± 0.002 · 10−1 −14.7%
−0.9%
+3.5% +1.9%
7.489 ± 0.007 · 100 −4.4%
−1.4%
+1.2% +1.9%
1.490 ± 0.001 · 10−2 −1.8%
−1.5%
+1.3% +2.0%
1.072 ± 0.001 · 10−2 −1.5%
−1.6%
2

NLO 13 TeV
+1.4% +0.4%
−1.8% −0.6%
+1.3% +0.8%
1.017 ± 0.003 · 100 −1.2%
−0.9%
+1.6% +0.9%
6.993 ± 0.021 · 10−1 −1.1%
−1.0%
+5.8% +0.4%
1.319 ± 0.003 · 102 −5.2%
−0.5%
+6.2% +0.8%
8.612 ± 0.025 · 10−1 −6.6%
−0.9%
+7.7% +0.9%
5.657 ± 0.014 · 10−1 −7.9%
−0.9%
+3.7% +1.9%
1.001 ± 0.004 · 101 −3.9%
−1.5%
+2.6% +1.7%
1.952 ± 0.007 · 10−2 −2.3%
−1.4%
+3.9% +1.9%
1.539 ± 0.005 · 10−2 −3.2%
−1.5%

1.563 ± 0.005 · 102

Table 7. Sample of LO and NLO total rates for the production of a single top, possibly in association and within cuts, at the 13-TeV LHC; we also
report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. The notation understands the sum of the t and t̄ cross
sections for all processes, and tt is a label that includes both t and t̄, defined from the shell with define tt = t t~ (and analogously for the label
bb). Processes that explicitly involve b-quarks in the final state are calculated in the four-flavour scheme, while all of the others are in the five-flavour
scheme. Being an EW-induced process, single-top production requires special care for the MadGraph5 aMC@NLO generation syntax: $$ means
excluding particles in the s-channel, while the > w+ > (> w- > ) forces a W + (W − ) to be present in the s-channel (see appendix B.1). Total
NLO cross sections for t- and s-channel single-top production have been known for some time [318, 319]. All single-top channels are also available
in MCFM [320–323], MC@NLO [173, 324], and POWHEG [325, 326]. An NLO calculation for tZj production has appeared in ref. [327].

JHEP07(2014)079

– 78 –

f.7

pp → tj (t-channel)

LO 13 TeV

## PDF page 81

Syntax
p p > h
p p > h j
p p > h j j
p p > h j j $$ w+ w- z
p p > h j j j $$ w+ w- z
p p > h wpm
p p > h wpm j
p p > h wpm j j
p p > h z
p p > h z j
p p > h z j j
p p > h w+ wp p > h wpm a
p p > h z wpm
p p > h z z
p p > h t t∼
p p > h tt j
p p > h b b∼
p p > h t t∼ j
p p > h b b∼ j

Cross section (pb)
LO 13 TeV
NLO 13 TeV
+20.2% +1.1%
+34.8% +1.2%
3.261
±
0.010
· 101 −17.9%
1.593 ± 0.003 · 101 −26.0%
−1.6%
−1.7%
+18.5% +1.1%
+39.4% +1.2%
1
1.422
±
0.006
·
10
8.367 ± 0.003 · 100 −26.4%
−16.6% −1.4%
−1.4%
+59.1% +1.4%
+20.7% +1.3%
3.020 ± 0.002 · 100 −34.7%
5.124 ± 0.020 · 100 −21.0%
−1.7%
−1.5%
+0.8% +2.0%
+1.7% +1.9%
0
1.900
±
0.006
·
10
1.987 ± 0.002 · 100 −2.0%
−0.9% −1.5%
−1.4%
+1.5%
+15.7% +1.5%
3.085 ± 0.010 · 10−1 +2.0%
2.824 ± 0.005 · 10−1 −12.7%
−3.0% −1.1%
−1.0%
+1.9%
+3.5% +1.9%
1.419 ± 0.005 · 100 +2.1%
1.195 ± 0.002 · 100 −4.5%
−2.6% −1.4%
−1.5%
+3.6% +1.2%
+10.7% +1.2%
−1
−1
4.842 ± 0.017 · 10
4.018 ± 0.003 · 10
−3.7% −1.0%
−9.3% −0.9%
+0.9%
+26.1% +0.8%
−1
1.574 ± 0.014 · 10−1 +5.0%
1.198 ± 0.016 · 10
−6.5% −0.6%
−19.4% −0.6%
+2.0% +1.9%
+3.5% +1.9%
7.674 ± 0.027 · 10−1 −2.5%
6.468 ± 0.008 · 10−1 −4.5%
−1.4%
−1.4%
+3.5%
+10.6%
+1.1%
2.225 ± 0.001 · 10−1 −9.2% −0.8% 2.667 ± 0.010 · 10−1 −3.6% +1.1%
−0.9%
+0.7%
+26.2% +0.7%
8.753 ± 0.037 · 10−2 +4.8%
7.262 ± 0.012 · 10−2 −19.4%
−6.3% −0.6%
−0.6%
+2.5%
+2.0%
+0.0%
+2.0%
1.065 ± 0.003 · 10−2 −1.9% −1.5%
8.325 ± 0.139 · 10−3 −0.3% −1.6%
+2.7% +1.7%
+0.7% +1.9%
−3
3.309 ± 0.011 · 10−3 −2.0%
2.518 ± 0.006 · 10
−1.4%
−1.4% −1.5%
+3.9% +1.8%
+1.1% +2.0%
−3
−3
5.292 ± 0.015 · 10
3.763 ± 0.007 · 10
−3.1% −1.4%
−1.5% −1.6%
+0.1% +1.9%
+1.9% +2.0%
2.093 ± 0.003 · 10−3 −0.6%
2.538 ± 0.007 · 10−3 −1.4%
−1.5%
−1.5%
+5.7% +2.0%
+30.0% +1.7%
−1
−1
4.608 ± 0.016 · 10
3.579 ± 0.003 · 10
−9.0% −2.3%
−21.5% −2.0%
+2.9% +1.5%
+2.4% +1.2%
6.328 ± 0.022 · 10−2 −1.8%
4.994 ± 0.005 · 10−2 −4.2%
−1.6%
−1.3%
+28.1% +1.5%
+7.3% +1.6%
−1
−1
4.983 ± 0.002 · 10
6.085 ± 0.026 · 10
−21.0% −1.8%
−9.6% −2.0%
+3.5% +2.5%
+45.6% +2.6%
3.244 ± 0.025 · 10−1 −8.7%
2.674 ± 0.041 · 10−1 −29.2%
−2.9%
−2.9%
+7.9% +1.8%
+45.6% +1.8%
−2
−2
9.034 ± 0.032 · 10
7.367 ± 0.002 · 10
−11.0% −2.2%
−29.1% −2.1%

Table 8. Sample of LO and NLO total rates for the production of a single SM Higgs, possibly in association and within cuts, at the 13-TeV
LHC; we also report the integration errors, and the fractional scale (left) and PDF (right) uncertainties. See table 1 for the meaning of wpm, and
table 7 for the meaning of tt, bb, and the generation syntax. Processes that explicitly involve b-quarks in the final state are calculated in the
four-flavour scheme, while all of the others are in the five-flavour scheme, except for g.12. A complete set of references relevant to NLO rates for
Higgs production can be found in refs. [328–330, 360, 361]. The W -boson width is set equal to 2.0476 GeV for process g.17. Cross sections at the
NLO for HV jj and HV V production appear in this work for the first time.

JHEP07(2014)079

– 79 –

Process
Single Higgs production
g.1
pp → H (HEFT)
g.2
pp → Hj (HEFT)
g.3
pp → Hjj (HEFT)
g.4
pp → Hjj (VBF)
g.5
pp → Hjjj (VBF)
g.6
pp → HW ±
g.7
pp → HW ± j
g.8∗
pp → HW ± jj
g.9
pp → HZ
g.10
pp → HZ j
∗
g.11
pp → HZ jj
g.12∗ pp → HW + W − (4f)
g.13∗ pp → HW ± γ
g.14∗ pp → HZW ±
g.15∗ pp → HZZ
g.16
pp → Htt̄
g.17
pp → Htj
g.18
pp → Hbb̄ (4f)
g.19
pp → Htt̄j
g.20∗ pp → Hbb̄j (4f)

## PDF page 82

Process

Syntax

Cross section (pb)

Higgs pair production
pp → HH (Loop improved)

h.1

pp → HHjj (VBF)

h.2

pp → HHW ±

h.3
h.4∗
h.5∗
h.6
h.7∗
h.8∗
h.10

h.11∗
h.12
h.13
h.14∗

p p > h h
p p > h h j j $$ w+ w- z
p p > h h wpm
p p > h h wpm j

pp → HHZ

p p > h h z

pp → HHW ± γ

p p > h h wpm a

pp → HHZj

p p > h h z j

pp → HHZZ

pp → HHZW

p p > h h z a
p p > h h z z
±

pp → HHW + W − (4f)

p p > h h z wpm
p p > h h w+ w-

pp → HHtt̄

p p > h h t t∼

pp → HHbb̄

p p > h h b b∼

pp → HHtj

p p > h h tt j

1.772 ± 0.006 · 10

6.503 ± 0.019 · 10−4

4.303 ± 0.005 · 10−4

1.922 ± 0.002 · 10−4
1.952 ± 0.004 · 10−6

2.701 ± 0.007 · 10−4

1.211 ± 0.001 · 10−4
1.397 ± 0.003 · 10−6
2.309 ± 0.005 · 10−6
−6

3.708 ± 0.013 · 10

7.524 ± 0.070 · 10−6

6.756 ± 0.007 · 10−4

1.844 ± 0.008 · 10−5

7.849 ± 0.022 · 10−8

+29.5% +2.1%
−21.4% −2.6%
+7.2% +2.3%
−6.4% −1.6%
+0.9% +2.0%
−1.3% −1.5%
+14.2% +1.5%
−11.7% −1.1%
+3.0% +2.2%
−3.0% −1.6%
+0.9% +2.0%
−1.3% −1.5%
+14.1% +1.4%
−11.7% −1.1%
+2.4% +2.2%
−2.5% −1.7%
+3.9% +2.2%
−3.8% −1.7%
+4.8% +2.3%
−4.5% −1.7%
+3.5% +2.3%
−3.4% −1.7%
+30.2% +1.8%
−21.6% −1.8%
+0.0% +1.8%
−0.6% −1.8%
+34.3% +3.1%
−23.9% −3.7%

NLO 13 TeV
2.763 ± 0.008 · 10−2

6.820 ± 0.026 · 10−4

5.002 ± 0.014 · 10−4

2.218 ± 0.009 · 10−4

2.347 ± 0.007 · 10−6

3.130 ± 0.008 · 10−4

1.394 ± 0.006 · 10−4

1.604 ± 0.005 · 10−6
2.754 ± 0.009 · 10−6

4.904 ± 0.029 · 10−6

9.268 ± 0.030 · 10−6

7.301 ± 0.024 · 10−4

2.444 ± 0.009 · 10−5

1.084 ± 0.012 · 10−7

+11.4% +2.1%
−11.8% −2.6%
+0.8% +2.4%
−1.0% −1.7%
+1.5% +2.0%
−1.2% −1.6%
+2.7% +1.6%
−3.3% −1.1%
+2.4% +2.1%
−2.0% −1.6%
+1.6% +2.0%
−1.2% −1.5%
+2.7% +1.5%
−3.2% −1.1%
+1.7% +2.3%
−1.4% −1.7%
+2.3% +2.3%
−2.0% −1.7%
+3.7% +2.2%
−3.2% −1.6%
+2.3% +2.3%
−2.1% −1.7%
+1.4% +2.2%
−5.7% −2.3%
+4.5% +2.8%
−3.1% −3.0%
+7.4% +3.1%
−10.8% −3.7%

Table 9. Sample of LO and NLO total rates for Higgs-pair production, possibly in association and within cuts, at the 13-TeV LHC; we also report
the integration errors, and the fractional scale (left) and PDF (right) uncertainties. See table 1 for the meaning of wpm, and table 7 for the meaning
of tt. All cross sections are calculated in the five-flavour scheme, except for process h.11 which is obtained in the four-flavour scheme to avoid
resonant-top contributions. Processes h.1, h.2, h.3, h.6, h.12, and h.13 have appeared in ref. [127] as NLO+PS results; some of these were already
known at the NLO [331]. The W -boson width is set equal to 2.0476 GeV for process h.13. Previous to the release of MadGraph5 aMC@NLO, the
only available public code for Higgs pair production was HPAIR [332, 333], relevant to process h.1 (see ref. [127] for more details on the different
approach adopted by MadGraph5 aMC@NLO). Process h.2 has been recently added to VBFNLO.

JHEP07(2014)079

– 80 –

∗

−2

pp → HHW ± j

pp → HHZγ

h.9∗

LO 13 TeV

## PDF page 83

Syntax

Cross section (pb)

e+ e- > j j
e+ e- > j j j
e+ e- > j j j j
e+ e- > j j j j j
e+ e- > t t∼
e+ e- > t t∼ j
e+ e- > t t∼ j j
e+ e- > t t∼ j j j
e+ e- > t t∼ t t∼
e+ e- > t t∼ t t∼ j
e+ e- > b b∼
e+ e- > b b∼ j
e+ e- > b b∼ j j
e+ e- > b b∼ j j j
e+ e- > b b∼ b b∼
e+ e- > b b∼ b b∼ j
e+ e- > t t∼ b b∼
e+ e- > t t∼ b b∼ j

LO 1 TeV
6.223 ± 0.005 · 10−1
3.401 ± 0.002 · 10−1
1.047 ± 0.001 · 10−1
2.211 ± 0.006 · 10−2
1.662 ± 0.002 · 10−1
4.813 ± 0.005 · 10−2
8.614 ± 0.009 · 10−3
1.044 ± 0.002 · 10−3
6.456 ± 0.016 · 10−7
2.719 ± 0.005 · 10−8
9.198 ± 0.004 · 10−2
5.029 ± 0.003 · 10−2
1.621 ± 0.001 · 10−2
3.641 ± 0.009 · 10−3
1.644 ± 0.003 · 10−4
7.660 ± 0.022 · 10−5
1.819 ± 0.003 · 10−4
4.045 ± 0.011 · 10−5

+0.0%
−0.0%
+9.6%
−8.0%
+20.0%
−15.3%
+31.4%
−22.0%
+0.0%
−0.0%
+9.3%
−7.8%
+19.4%
−15.0%
+30.5%
−21.6%
+19.1%
−14.8%
+29.9%
−21.3%
+0.0%
−0.0%
+9.5%
−8.0%
+20.0%
−15.3%
+31.4%
−22.1%
+19.9%
−15.3%
+31.3%
−22.0%
+19.5%
−15.0%
+30.5%
−21.6%

NLO 1 TeV
6.389 ± 0.013 · 10−1
3.166 ± 0.019 · 10−1
1.090 ± 0.006 · 10−1
2.771 ± 0.021 · 10−2
1.745 ± 0.006 · 10−1
5.276 ± 0.022 · 10−2
1.094 ± 0.005 · 10−2
1.546 ± 0.010 · 10−3
1.221 ± 0.005 · 10−6
5.338 ± 0.027 · 10−8
9.282 ± 0.031 · 10−2
4.826 ± 0.026 · 10−2
1.817 ± 0.009 · 10−2
4.936 ± 0.038 · 10−3
3.601 ± 0.017 · 10−4
1.537 ± 0.011 · 10−4
2.923 ± 0.011 · 10−4
7.049 ± 0.052 · 10−5

+0.2%
−0.2%
+0.2%
−2.1%
+0.0%
−2.8%
+4.4%
−8.6%
+0.4%
−0.4%
+1.3%
−2.1%
+5.0%
−6.3%
+10.6%
−11.6%
+13.2%
−11.2%
+18.3%
−15.4%
+0.0%
−0.0%
+0.5%
−2.5%
+0.0%
−3.1%
+4.8%
−8.9%
+15.2%
−12.5%
+17.9%
−15.3%
+9.2%
−8.9%
+13.7%
−13.1%

Table 10. Sample of LO and NLO rates for the production of light jets in association with heavy quarks, possibly within cuts, at a 1-TeV e+ e−
collider; we also report the integration errors, and the fractional scale uncertainties. Cross sections for processes i.1–i.10 are calculated in the fiveflavour scheme. For processes i.11–i.18 we use the four-flavour scheme, and require the presence of at least two (four in i.15–i.16) b-jets in the final
state. b-jets are clustered with the same parameters as light jets. Results at NLO accuracy for up to seven light jets can be found in refs. [9, 70, 334–
338], and for a heavy-quark-pair plus up to one jet in refs. [339–345]. All other processes are computed here for the first time at the NLO.

JHEP07(2014)079

– 81 –

Process
Heavy quarks and jets
i.1
e+ e− → jj
i.2
e+ e− → jjj
i.3
e+ e− → jjjj
i.4
e+ e− → jjjjj
i.5
e+ e− → tt̄
i.6
e+ e− → tt̄j
∗
i.7
e+ e− → tt̄jj
i.8∗
e+ e− → tt̄jjj
∗
i.9
e+ e− → tt̄tt̄
∗
i.10
e+ e− → tt̄tt̄j
i.11
e+ e− → bb̄ (4f)
i.12
e+ e− → bb̄j (4f)
i.13∗ e+ e− → bb̄jj (4f)
i.14∗ e+ e− → bb̄jjj (4f)
i.15∗ e+ e− → bb̄bb̄ (4f)
i.16∗ e+ e− → bb̄bb̄j (4f)
i.17∗ e+ e− → tt̄bb̄ (4f)
i.18∗ e+ e− → tt̄bb̄j (4f)

## PDF page 84

Syntax

Cross section (pb)

e+ e- > t t∼ h
e+ e- > t t∼ h j
e+ e- > t t∼ h j j
e+ e- > t t∼ a
e+ e- > t t∼ a j
e+ e- > t t∼ a j j
e+ e- > t t∼ z
e+ e- > t t∼ z j
e+ e- > t t∼ z j j
e+ e- > t t∼ wpm j j
e+ e- > t t∼ h z
e+ e- > t t∼ a z
e+ e- > t t∼ a h
e+ e- > t t∼ a a
e+ e- > t t∼ z z
e+ e- > t t∼ h h
e+ e- > t t∼ w+ w-

LO 1 TeV
2.018 ± 0.003 · 10−3
2.533 ± 0.003 · 10−4
2.663 ± 0.004 · 10−5
1.270 ± 0.002 · 10−2
2.355 ± 0.002 · 10−3
3.103 ± 0.005 · 10−4
4.642 ± 0.006 · 10−3
6.059 ± 0.006 · 10−4
6.351 ± 0.028 · 10−5
2.400 ± 0.004 · 10−7
3.600 ± 0.006 · 10−5
2.212 ± 0.003 · 10−4
9.756 ± 0.016 · 10−5
3.650 ± 0.008 · 10−4
3.788 ± 0.004 · 10−5
1.358 ± 0.001 · 10−5
1.372 ± 0.003 · 10−4

+0.0%
−0.0%
+9.2%
−7.8%
+19.3%
−14.9%
+0.0%
−0.0%
+9.3%
−7.9%
+19.5%
−15.0%
+0.0%
−0.0%
+9.3%
−7.8%
+19.4%
−15.0%
+19.3%
−14.9%
+0.0%
−0.0%
+0.0%
−0.0%
+0.0%
−0.0%
+0.0%
−0.0%
+0.0%
−0.0%
+0.0%
−0.0%
+0.0%
−0.0%

NLO 1 TeV
1.911 ± 0.006 · 10−3
2.658 ± 0.009 · 10−4
3.278 ± 0.017 · 10−5
1.335 ± 0.004 · 10−2
2.617 ± 0.010 · 10−3
4.002 ± 0.021 · 10−4
4.949 ± 0.014 · 10−3
6.940 ± 0.028 · 10−4
8.439 ± 0.051 · 10−5
3.723 ± 0.012 · 10−7
3.579 ± 0.013 · 10−5
2.364 ± 0.006 · 10−4
9.423 ± 0.032 · 10−5
3.833 ± 0.013 · 10−4
4.007 ± 0.013 · 10−5
1.206 ± 0.003 · 10−5
1.540 ± 0.006 · 10−4

+0.4%
−0.5%
+0.5%
−1.5%
+4.0%
−5.7%
+0.5%
−0.4%
+1.6%
−2.4%
+5.4%
−6.6%
+0.6%
−0.5%
+2.0%
−2.6%
+5.8%
−6.8%
+9.6%
−9.1%
+0.1%
−0.0%
+0.6%
−0.5%
+0.3%
−0.4%
+0.4%
−0.4%
+0.5%
−0.5%
+0.9%
−1.1%
+1.0%
−0.9%

Table 11. Sample of LO and NLO rates for the production of top quarks in association with bosons, possibly within cuts and in association with
jets, at a 1-TeV e+ e− collider, and the fractional scale uncertainties. Cross sections are calculated in the five-flavour scheme; see table 1 for the
meaning of wpm. Results at NLO accuracy for tt̄H production can be found in ref. [346]. All of the other processes are computed here for the first
time at the NLO.

JHEP07(2014)079

– 82 –

Process
Top quarks +bosons
j.1
e+ e− → tt̄H
j.2∗
e+ e− → tt̄Hj
∗
j.3
e+ e− → tt̄Hjj
j.4∗
e+ e− → tt̄γ
∗
j.5
e+ e− → tt̄γj
j.6∗
e+ e− → tt̄γjj
∗
j.7
e+ e− → tt̄Z
∗
j.8
e+ e− → tt̄Zj
j.9∗
e+ e− → tt̄Zjj
∗
j.10
e+ e− → tt̄W ± jj
j.11∗ e+ e− → tt̄HZ
j.12∗ e+ e− → tt̄γZ
j.13∗ e+ e− → tt̄γH
j.14∗ e+ e− → tt̄γγ
j.15∗ e+ e− → tt̄ZZ
j.16∗ e+ e− → tt̄HH
j.17∗ e+ e− → tt̄W + W −

## PDF page 85

4.2

Differential distributions

♦ Six-lepton production.
tons:

We start by studying the (N)LO+PS production of six leppp −→ e+ e− µ+ νµ τ − ν̄τ ,

(4.1)

which we have computed by using the complex mass scheme; the τ − lepton is set stable,
and its mass is kept at the physical value, while the electron and the muon are treated as
massless. On top of the computation carried out with the exact six-lepton matrix elements
of eq. (4.1), we have also considered the production of the ZW + W − triplet, with the
subsequent decays of the vector bosons performed with either MadSpin or by the PSMC
(in this case, HERWIG6):
pp −→ Z(→ e+ e− ) W + (→ µ+ νµ ) W − (→ τ − ν̄τ ) .

(4.2)

While MadSpin multiplies the undecayed matrix elements by the branching ratios of the
relevant decays, so that the rates resulting from eq. (4.2) are in absolute value directly
comparable to those of eq. (4.1), the PSMC does not; in that case, we have therefore
manually included such an overall factor. To all samples, we have applied the following cut:
M (ℓ+ ℓ(′)− ) > 30 GeV ,

(4.3)

on all opposite-charged lepton pairs; given the lepton flavours considered here, not
surprisingly the vastly dominant effect of such a cut is that due to the e+ e− pair. We

– 83 –

JHEP07(2014)079

In this section we present sample results for differential observables relevant to several
processes, which we have simulated at the 8, 13, or 14 TeV LHC. While some of these have
never been computed before at the NLO+PS accuracy (or even at fNLO; see section 4.1),
and appear here for the first time, we do not aim to present a series of phenomenological
analyses, which would be out of the scope of this work, but rather at showing yet again
the flexibility of MadGraph5 aMC@NLO, and the type of results that one can obtain
with it. For this reason, the various PSMCs which we shall use have been run with
their default parameters, and no underlying events have been generated. Having said
that, some of the predictions given here are motivated by recent measurements by ATLAS
and CMS. Furthermore, the present section constitutes a complement in particular to
section 2.4.5, since we shall discuss, using explicit examples, several features of the FxFx
merging procedure which have been outlined before in a general fashion. We shall be mainly
concerned with (N)LO+PS results, but we shall also consider f(N)LO ones where necessary.
As was the case for the total rates presented in section 4.1, the computation of scale and
PDF uncertainties has been carried out by using the reweighting procedure introduced
in ref. [125] (see also appendix B.3). NLO+PS results that have never appeared in the
literature are: six-lepton, tt̄W + W − , and SM Higgs in VBF+1j production; furthermore,
double-Higgs production in association with either a tt̄ pair or a Z boson has been solely
computed with MadGraph5 aMC@NLO, in ref. [127]. Finally, FxFx-merged results for
ZZ and He+ νe production are also presented here for the first time.

## PDF page 86

10-5

10-5

e+e-µ+νµτ-ντ production at the 13 TeV LHC

NLO, ME

LO, ME (x0.5)

NLO, ME V-reco

LO, ME V-reco (x0.5)

NLO, MS V-reco

LO, MS V-reco (x0.5)

NLO, PSMC V-reco

LO, PSMC V-reco (x0.5)

10-8

10-7

10-8

Ratio over NLO, ME V-reco

1
1
0.8
0.6
0.4
0.2
0

Ratios LO over NLO (LO not resc.)

1

LO, MS V-reco (x0.5)

NLO, PSMC V-reco

LO, PSMC V-reco (x0.5)

2

3

log10(pT(e+e-µ+νµτ-ντ)/GeV)

Ratios LO over NLO (LO not resc.)

250

500

750
1000
1250
m(e+e-µ+νµτ-ντ) [GeV]

1500

1750

2000

Figure 4. Transverse momentum (left panel) and invariant mass (right panel) of the six-lepton
system, for the processes of eqs. (4.1) and (4.2). See the text for details.

shall call eq. (4.3) the generation cut.54 On top of eq. (4.3), we have also imposed (also
at the analysis level):
∣
∣
∣M (e+ e− ) − mZ ∣ < 20 GeV ,
(4.4)
∣
∣
+
∣M (µ νµ ) − mW ∣ < 20 GeV ,
(4.5)
∣
∣
∣M (τ − ν̄τ ) − mW ∣ < 20 GeV ,
(4.6)

which we shall call V -reco cuts. Since eq. (4.2) features only 3-resonant contributions (see
section 2.5 about the notation used here for resonant and non-resonant diagrams), the
results of the MadSpin- and PSMC-decayed samples are basically the same if one considers
only the generation cut, or the generation and V -reco cuts together; for this reason, we
shall discuss only the latter scenario. On the other hand, one of the reasons for comparing
eqs. (4.1) and (4.2) is precisely that of assessing the importance of non-3-resonant
contributions to six-lepton matrix elements; hence, in this case we shall present both the
generation-cut-only and the generation-plus-V -reco cuts results.
In figure 4 we show observables relevant to the six-lepton system, i.e. obtained by
summing the four-momenta of the leptons: the transverse momentum (left panel) and the
invariant mass (right panel). Both the NLO+PS (solid histograms) and LO+PS (dashed
histograms, rescaled as indicated in order to fit into the layout) are displayed. The green histograms are the results of eq. (4.1) with only the generation cut (denoted by “(N)LO ME”);
the results for the generation-plus-V -reco cuts are shown as yellow (eq. (4.1), denoted by
“(N)LO ME V -reco”), red (eq. (4.2) with MadSpin, denoted by “(N)LO MS V -reco”), and
blue (eq. (4.2) with PSMC decays, denoted by “(N)LO PSMC V -reco”) histograms respectively. In the middle insets, the ratios of all the NLO results over the NLO ME V -reco ones
54

Despite the fact that it has been imposed at the analysis level, and the true generation cut is marginally
lower so as to avoid biases.

– 84 –

JHEP07(2014)079

1.2

1

0

LO, ME (x0.5)
LO, ME V-reco (x0.5)

NLO, MS V-reco

Ratio over NLO, ME V-reco

1.2

1
0.8
0.6
0.4
0.2
0

NLO, ME
NLO, ME V-reco

MadGraph5_aMC@NLO

10-7

σ per bin [pb]

10-6

MadGraph5_aMC@NLO

σ per bin [pb]

10-6

e+e-µ+νµτ-ντ production at the 13 TeV LHC

## PDF page 87

-6

-6

4.0 10

+ - +

3.0 10

-

+ - +

e e µ νµτ ντ production at the 13 TeV LHC

-6

-

e e µ νµτ ντ production at the 13 TeV LHC

3.5 10

NLO, ME

LO, ME (x1.7)

NLO, ME V-reco

LO, ME V-reco (x1.85)

NLO, MS V-reco

LO, MS V-reco (x1.85)

NLO, PSMC V-reco

LO, PSMC V-reco (x1.85)

-6

2.5 10
LO, ME
LO, ME V-reco

NLO, MS V-reco

LO, MS V-reco

NLO, PSMC V-reco

LO, PSMC V-reco

2.0 10

-6

1.5 10

-6

1.0 10

-7

5.0 10

σ per bin [pb]

-6

NLO, ME
NLO, ME V-reco

MadGraph5_aMC@NLO

σ per bin [pb]

-6

2.5 10

-6

2.0 10

-6

1.5 10

-6

1.0 10

Ratio over NLO, ME V-reco

1.4

MadGraph5_aMC@NLO

-6

3.0 10

Ratio over NLO, ME V-reco

1.4

1.2

1.2
1
0.7

Ratios LO over NLO (LO not resc.)

0.6

Ratios LO over NLO (LO not resc.)

0.6

0.5

0.5
-1

-0.8

-0.6

-0.4

-0.2

0
0.2
cosψµ+τ-

0.4

0.6

0.8

1

-1

-0.8

-0.6

-0.4

-0.2

0
0.2
cosχµ+τ-

0.4

0.6

0.8

1

Figure 5. Cosine of correlation angles for the µ+ τ − pair, in six-lepton production, eqs. (4.1)
and (4.2). See the text for details.

are presented. Finally, in the lower insets each LO prediction is divided by its NLO counterpart (so these are essentially the inverse of the K factors). The plots show clearly the
large impact of non-3-resonant contributions, which induce dramatic shape modifications
for M (6ℓ) < 500 GeV and 10 < pT (6ℓ) < 250 GeV (the very small pT region being dominated by PSMC radiation effects). On the other hand, by imposing V -reco cuts the three
predictions agree rather well with each other, which is the signal that spin correlations are
unimportant for these observables (and, more importantly in view of the aim of this paper,
that all is fine from a technical viewpoint, in the context of a very involved production process). We have performed similar comparisons for a large number of observables; here, we
limit ourselves to reporting the results for the cosine of the angle defined by the directions
of flight of the µ+ and τ − leptons, which we denote by ψµ+ τ − (left panel of figure 5) when
it is computed in the laboratory frame, and by χµ+ τ − (right panel of figure 5) when it is
computed by first boosting the four-momentum of the µ+ and τ − leptons to the rest frame
of the µ+ νµ and τ − ν̄τ systems respectively (i.e., to the virtual-W + and W − rest frames in
the case of resonant contributions); the latter observable is known to be particularly suitable for the study of spin-correlation effects. The same conclusions as for the observables
of figure 4 apply here, bar for the χµ+ τ − NLO PSMC V -reco one that is fairly different
from both the NLO ME V -reco and NLO MS V -reco predictions, which in turn agree with
each other quite well. As it was expected, this is a manifestation of the importance of spin
correlations for such an observable, and a direct validation of the MadSpin procedure.
The overall messages that one can obtain from the present study are the following.
Firstly, we did verify that the conclusions reached above are not qualitatively modified
if one replaces the (N)LO ME results with those obtained by imposing the generation
cut and eq. (4.4) only — in other words, it is the simultaneous action of the three cuts
of eqs. (4.4)–(4.6) that brings the predictions for eq. (4.1) in agreement with those for
eq. (4.2) and MadSpin; this is obviously because it is important that all three vector

– 85 –

JHEP07(2014)079

1
0.7

## PDF page 88

♦ tt̄W − W + production.

We now turn to considering the process:

pp −→ t(→ e+ νe b) t̄(→ e− ν̄e b̄) W − (→ µ− ν̄µ ) W + (→ µ+ νµ ) ,

(4.7)

which we have simulated at the (N)LO+PS accuracy, by only considering the undecayed
matrix elements with tt̄W + W − final states, and by using Pythia8 as PSMC and either
MadSpin or the internal Pythia8 routine (which correctly accounts for decay spin correlations) for the decays of the top quarks and W bosons. In figure 6 we present the transverse
momentum of the tt̄W + W − system, which is the typical observable whose small-pT behaviour is dominated by MC effects (whose systematics will not be studied here), and
which is thus unreliable if computed at fNLO accuracy. Both the NLO+PS (solid histograms) and LO+PS (dashed histograms) results are displayed, with the respective scaleuncertainty bands (in dark and light shades respectively). The very significant reduction
of such theoretical systematics when higher-order corrections are included is evident in the
whole range considered (see also entry e.13 in table 6 for its total-rate counterpart). While
for asymptotically-large transverse momenta one expects the NLO+PS scale dependence to
be of LO type (because in that region the computation is dominated by tree-level contributions), for such a massive system these pT ’s are confortably in the TeV-range. In figure 7 we
show the transverse momenta of the four-hardest charged leptons in the events; the leptons
are required to have pT (ℓ) > 20 GeV and |η(ℓ)| < 2.5. At variance with those of figure 6,
these plots include the branching ratios of the decays reported in eq. (4.7). The LO+PS
results in the main frames are rescaled so as to fit into the layout. Each plot displays
four histograms, that correspond to NLO+PS (solid, with MadSpin decays; dashed, with
Pythia8 decays) and to LO+PS (dot-dashed, with MadSpin decays; dotted, with Pythia8
decays) results. The ratios of these predictions over the NLO+PS, MadSpin-decayed ones
are shown in the insets. The radiative corrections are large, but relatively flat in the pT
ranges considered here; as in the case of the pT of the system, their inclusion reduces the
scale uncertainty in a dramatic manner. Production spin correlations are sizable, so much so
that MadSpin- and Pythia8-decayed results have shapes which are barely within, or slightly
outside of, the theoretical systematics bands. This is true at the NLO; at the LO, the two
predictions are compatible within uncertainties, but this is solely due to the fact that the

– 86 –

JHEP07(2014)079

bosons be near their respective mass shell. Secondly, the effects of NLO corrections are
non negligible, in both rate and shape; however, the patterns of comparison among the
various calculations are to a large extent independent of the perturbative accuracy of the
latter. Thirdly, production spin correlations are present, that can be properly described
only by the full six-lepton computation, and by MadSpin as well if one limits oneself to the
3-resonant region. It is clear that the cuts of eqs. (4.5) and (4.6), and the definition of the
observables considered here, bar ψµ+ τ − , cannot be achieved experimentally, owing to the
presence of the neutrino four-momenta. However, they have helped us reach conclusions
which have a general validity, and in particular in the case of a fully realistic analysis:
namely, that non-resonant effects in six-lepton production may be quite large and that,
for all those cuts that render the 3-resonant contributions dominant, the undecayed-plusMadSpin simulation provides one with a very good approximation of the exact calculation.

## PDF page 89

σ per bin [pb]

-4
- + ttW W production at 13 TeV LHC 10

10-5
0

10-4

10 20 30 40 50 60 70 80
p (tt-W+W-) [GeV]

10-5

MadGraph5_aMC@NLO

T

NLO+PS
LO+PS

0

100

200

300

400

500
pT(tt-W+W-) [GeV]

600

Figure 6. Transverse momentum of the system of the four primary final-state particles in tt̄W + W −
production.

LO scale dependence is rather large: in fact, the pattern of the inclusion of production spin
correlations is basically independent of the perturbative order at which one is working. This
is nothing but another manifestation of the benefits inherent to the increased predictive
power of simulations that include both NLO and production spin correlation effects.
♦ Double-Higgs production. We now consider double-Higgs production in the SM at
the 14 TeV LHC. This process has been investigated recently with MadGraph5 aMC@NLO
in ref. [127], where all the six dominant channels at the LHC have been computed up to
NLO+PS accuracy, some of them for the first time. For all channels, the results of ref. [127]
have improved what was available in the literature in at least one respect. In ref. [127]
we have only presented (N)LO+PS distributions. Here, we amend this by showing also
f(N)LO spectra; we use the transverse momentum of the Higgs pair, and the tt̄HH and
ZHH channels, as a definite example; as PSMCs, we adopt Pythia8 and HERWIG6. The
results are shown in figure 8, as solid (for NLO-accurate) and dashed (for LO-accurate)
histograms. The main frames display the NLO predictions in absolute value, while the
LO ones are rescaled in order to fit into the layout; the K factors can be read from the
insets, where we present the ratios of all results over those at the NLO+PS obtained with
Pythia8. The common feature of the two plots is that NLO results are mutually closer
than the corresponding LO ones; the two NLO+PS predictions are extremely similar for
both processes, while the fNLO spectrum in ZHH production is only marginally softer (an
overall effect smaller than 20%). It is interesting to see that this stabilisation due to the in-

– 87 –

JHEP07(2014)079

σ per bin [pb]

10-3

## PDF page 90

tt-W+W- production at 13 TeV LHC
σ per bin [pb]

10

NLO+PS+MS
NLO+PS
LO+PS+MS (x 0.5)
LO+PS (x 0.5)

-7

10-8

pT(l2)

pT(l1)
Ratio over NLO+PS+MS

0.6

σ per bin [pb]

MadGraph5_aMC@NLO

cuts: require at least 4 leptons with
pT(l) > 20 GeV and |η(l)| < 2.5

10-7

10-8

pT(l3)

10-9
1.2
1
0.8

pT(l4)

0.6
0

50

100

150

200

250

0

50

100

150

200
250
pT [GeV]

Figure 7. Transverse momentum of the hardest four charged leptons in tt̄W + W − production —
see eq. (4.7). The LO+PS results that appear in the insets have not been rescaled.

clusion of higher-order corrections follows different patterns for the two channels considered
here. ZHH is predominantly a q q̄-initiated process: therefore, the difference between the
two standalone PSMCs (i.e., LO+PS) is expected to be smaller than in the case of tt̄HH
production, which mainly proceeds through gg fusion. This is precisely what we see in figure 8 (compare the purple and red histograms in the insets). On the other hand, at fLO the
Higgs pair recoils against a Z boson and a tt̄-system in ZHH and tt̄HH production respectively; the kinematics of the tt̄ pair being non-trivial (at variance with that of a single Z)
implies that the fLO prediction for pT (HH) is farther away from the corresponding LO+PS
ones in the ZHH channel than in the tt̄HH channel (see the green dashed histograms in
the insets, and compare the position of the peaks of the fLO and fNLO results).
♦ Single-Higgs production. We now turn to discussing the production of a single
SM Higgs at the 13 TeV LHC. The aims of figure 9, where we show the Higgs transverse momentum, are twofold. Firstly, we compare LO+PS with NLO+PS predictions;
secondly, we present results for all PSMCs which are matched to NLO calculations in

– 88 –

JHEP07(2014)079

10-9
1.2
1
0.8

## PDF page 91

10-4

tt-HH production at the 14 TeV LHC

ZHH production at the 14 TeV LHC

fNLO

fLO (x0.4)

fNLO

fLO (x0.7)

NLO PY8

LO PY8 (x0.4)

NLO PY8

LO PY8 (x0.7)

NLO HW6

LO HW6 (x0.4)

NLO HW6

LO HW6 (x0.7)

Ratio over NLO PY8 (LO curves not rescaled)

1.5

10-6

1
0.5
100

150
200
250
pT(HH) [GeV]

300

350

400

0

50

100

150
200
250
pT(HH) [GeV]

300

350

400

Figure 8. Transverse momentum of the two-Higgs system in tt̄HH (left panel) and ZHH (right
panel) production. (N)LO+PS and f(N)LO results are shown. We have used Pythia8 and
HERWIG6.
MadGraph5 aMC@NLO.55 The comparison between the two panels of the figure shows

the two expected behaviours: at large pT ’s, all NLO+PS predictions coincide (and are just
on top of the corresponding fNLO result, not displayed here), while the LO+PS are vastly
different; on the other hand, at small pT ’s, the relative behaviour of the various PSMCs
is the same, regardless of the perturbative order of the underlying matrix-element computations. We point out that all PSMCs are treated on equal footing, i.e. they are given
the same numerical values as shower-scales parameters (such scales are equal to mH at the
LO, and controlled by the D function at the NLO); so while different scales for different
PSMCs could bring them in better agreement at the LO, this is actually a negative implication of the loss of predictivity at this perturbative order, and it is unnecessary when
NLO corrections are included in the simulations; a further example of this pattern will
be given below, in the study of Higgs production through VBF. We conclude this part by
showing, in figure 10, the Higgs pT that results from the five dominant production channels
at the 13 TeV LHC (whose total rates are reported in lines g.1, g.4, g.6, g.9, and g.16 of
table 8, where one can also find the MadGraph5 aMC@NLO shell commands relevant to
their generation); the thickness of the bands represent the combined scale and PDF uncertainties; all the predictions are obtained at the NLO+PS, with the use of Pythia8. This
plot is another demonstration of the flexibility of the MadGraph5 aMC@NLO framework.

♦ Higgs production in VBF. As a further example of the stabilisation of the predictions that result from including higher-order matrix elements (which in turn serves as
a validation exercise for the whole NLO+PS machinery in MadGraph5 aMC@NLO), we
consider Higgs production in VBF, which we compute in two ways: by considering the process whose Born is of O(α3 ) (which we denote by VBF+0j [347], and whose final state at
55

We remind the reader that Pythia6(pT ) is available for ISR-only processes.

– 89 –

JHEP07(2014)079

1

50

Ratio over NLO PY8 (LO curves not rescaled)

1.5

0.5
0

MadGraph5_aMC@NLO

σ per bin [pb]

10-5

MadGraph5_aMC@NLO

σ per bin [pb]

10-5

## PDF page 92

Higgs production at the 13 TeV LHC

101

Higgs production at the 13 TeV LHC

101

MH = 125 GeV, LO + PS

MH = 125 GeV, NLO + PS

LO PY8

10-2

2

NLO PY6(Q )
NLO PY6(pT)
NLO HW6

10-1

MadGraph5_aMC@NLO

LO HW6

σ per bin [pb]

LO PY6(pT)

10-1

NLO HW++

100

2

LO PY6(Q )

MadGraph5_aMC@LO

σ per bin [pb]

NLO PY8

LO HW++

100

10-2

2

2
Ratio over LO+PY8

1.5

Ratio over NLO+PY8

1.5
1

0.5

0.5

0

0
0

50

100
pT(H) [GeV]

150

200

0

50

100

150
pT(H) [GeV]

200

250

300

Figure 9. Higgs pT spectrum in gg fusion (HEFT), for various PSMCs, at the LO+PS (left panel)
and NLO+PS (right panel) accuracy. Note the larger pT range in the right panel.
1

Higgs production at the 13 TeV LHC

10

MH = 125 GeV, NLO + Pythia8
ggH
VBF

0

WH
ZH
ttH

-1

10

MadGraph5_aMC@NLO

σ per bin [pb]

10

-2

10

-3

10

0

50

100
pT(H) [GeV]

150

200

Figure 10. Higgs pT spectrum for the five dominant production channels at the LHC, at the
NLO+PS accuracy with Pythia8.

the Born level thus features a Higgs-plus-two-parton system), and the process whose Born
is of O(α3 αS ) (which we denote by VBF+1j, and whose final state at the Born level thus
features a Higgs-plus-three-parton system). These are the processes reported in lines g.4
and g.5 of table 8, where the interested reader can also find the MadGraph5 aMC@NLO
shell commands that one must use in order to generate them. The only analysis cuts we
impose here are on the transverse momenta of the (anti-kT , R = 0.5) jets, by requiring
that pT (j) > 20 GeV. The only observables for which a direct comparison between VBF+0j
and VBF+1j is sensible, and allow one to assess the impact of perturbative corrections,
are those related to the third jet, where one expects to have an effective LO and NLO
description respectively. In figure 11 we present predictions for the transverse momen-

– 90 –

JHEP07(2014)079

1

## PDF page 93

10

100

1

Higgs production via VBF (+1j) at the 13 TeV LHC

Higgs production via VBF (+1j) at the 13 TeV LHC

MH = 125 GeV, NLO + PS

MH = 125 GeV, NLO + PS
H+3j PY8
H+3j PY6(Q )

10-1

0

H+3j PY8

H+3j HW6

H+3j PY6(Q2)

H+2j PY8 (x0.2)

H+3j HW6

10-3

10-4

10

H+2j PY8 (x0.2)

-1

H+2j PY6(Q2) (x0.2)
H+2j HW6 (x0.2)

10

-2

10

-3

MadGraph5_aMC@NLO

H+2j HW6 (x0.2)

σveto [pb]

2

H+2j PY6(Q ) (x0.2)

10-2

MadGraph5_aMC@NLO

σ per bin [pb]

10

2

Ratio over H+3j HW6 (H+2j not resc.)

1.2
1.1
1
0.9
0.8

Ratio over H+3j HW6 (H+2j not resc.)

1.2
1.1
1
0.9
0.8

Ratio over H+2j HW6 (PY8 x0.75)

1.2
1.1
1
0.9
0.8

Ratio over H+2j HW6 (PY8 x0.55)

20

30

40

50

60
70
pT(j3) [GeV]

80

90

100

20

30

40

50
60
70
pT(jveto) [GeV]

80

90

100

Figure 11. Third-jet observables in Higgs VBF+0j and VBF+1j production, both at the
NLO+PS, with Pythia8, HERWIG6, and Pythia6(Q2 ).

tum spectrum of the third-hardest jet, and for the rate as a function of the transverse
momentum of the veto jet:
∫ ∞
dσ
.
(4.8)
dpT
σveto (pT (jveto )) =
dp
T
pT (jveto )
The veto jet is the hardest jet which is not one of the two tagging jet (which are defined
to be the two hardest ones overall, and which we denote by j1 and j2 respectively), and
whose rapidity obeys the condition:
min (yj1 , yj2 ) ≤ y(jveto ) ≤ max (yj1 , yj2 ) .

(4.9)

The quantity defined in eq. (4.8) is related to Pveto , defined e.g. in eq. (41) of ref. [330], by
a simple normalisation factor, σveto = σNLO Pveto . For both VBF+0j (dashed histograms)
and VBF+1j (solid histograms) the results for three PSMCs (Pythia8 (red), Pythia6(Q2 )
(green), and HERWIG6 (black)) are displayed, with the VBF+0j ones rescaled by a factor
1/5 in order for them to fit into the layout. The ratios of the Pythia predictions over
the HERWIG6 ones are presented in the insets. In the inset relevant to VBF+1j, we also
report the ratio of the HERWIG6 VBF+0j result over the VBF+1j one (black dashed
histogram), which is related to the inverse of the K factor — for both observables, the
latter is of the order of 1.05–1.15. In the insets we also display the scale uncertainties
as gray bands: it is evident that the inclusion of the contributions of relative O(αS ) in
VBF+1j significantly reduces the theoretical systematics. Apart from this, the most
striking consequence of such an inclusion is the fact that the three PSMCs in VBF+1j
are fairly close to each other; this is not the case in VBF+0j, where Pythia8 has a
much softer shape than either Pythia6 or HERWIG6. We point out that this is a feature
of quantities related to the third jet: other observables which have an NLO nature in

– 91 –

JHEP07(2014)079

1.2
1.1
1
0.9
0.8

## PDF page 94

VBF+0j are much better behaved, with the three PSMCs in good agreement already at
O(α3 (1 + αS )). Therefore, although one could possibly find settings for the PSMCs that
would bring the predictions for the pT (j3 ) and σveto VBF+0j spectra in better agreement
than in figure 11, this would simply be the signal of an unsatisfactory predictive capability,
which is restored by considering these observables in VBF+1j production.

56

If visually that may not seem to be the case, it is because the bin widths are not equal: note that the
cross section is differential.

– 92 –

JHEP07(2014)079

♦ Top-pair production. While differential distributions relevant to tt̄ production measured at the LHC by the ATLAS (at 7 TeV in lepton+jets events [348]) and the CMS (at
7 and 8 TeV, in lepton+jets and dilepton events [349–351]) collaborations are generally
in very good agreement with theoretical predictions, the CMS data for the reconstructed
transverse momentum of the top quark (pT (t)) are visibly softer than NLO+PS predictions,
and in disagreement with those of ATLAS for pT (t) < 200 GeV (ATLAS data are harder).
Given this inconsistency between measurements it is premature to speculate on the origin
of a possible discrepancy between data and theory; it is however of some interest to discuss
the theoretical systematics that affect the NLO+PS spectrum. Among these, those due to
scale, PDFs, and choice of top-quark mass have been studied by the experimental collaborations, and shown to be smaller than the disagreement between data and theory [349].
Here, we therefore concentrate on other sources of systematics. One of these is due to missing higher orders, since the NLO+PS predictions used by the experiments include only up
to O(αS3 ) terms, namely tt̄+0j samples at the NLO. While the impact of missing higher orders in perturbation theory is estimated by scale variations, an important and independent
check of this assessment may be obtained by considering NLO-merged prections. In the
left panel of figure 12 we thus compare the unmerged tt̄ + 0j prediction with the FxFx one,
where the tt̄ + 0j and tt̄ + 1j samples are combined with µQ = 100 GeV. Both merged and
unmerged results have been obtained with HERWIG6, by setting the collider energy equal
to 8 TeV; the latter curve has been rescaled56 in order for its visible integral to coincide
with that of the former (since in this case we are specifically interested in a shape comparison: in absolute values, the two cross sections differ however by only 2.5%). As one can
gather from the plot, the two predictions are close to each other; the FxFx prediction is
sightly softer than the unmerged one, but this does not appear to be sufficient to bring it in
agreement with the CMS measurement. The variation of the merging scale in a large range
(30–155 GeV) does not induce any significant change. It therefore appears that the systematics due to higher-order corrections are fully under control, since scale variations and
NLO-merging give consistent results for this observable, and we thus confirm the previous
findings that it cannot explain the discrepancy between theory and CMS data. Another
source of theoretical systematics in NLO+PS predictions is that due to the choice of the
PSMC. This is presented in the right panel of figure 12, where we compare the (tt̄ + 0j
unmerged) predictions obtained with Pythia8 (cyan), HERWIG6 (red), and Pythia6(Q2 )
(grey); the lower inset presents the bin-by-bin ratios of the latter two predictions over that
of Pythia8. It is clear from the plot that the three PSMCs are amply consistent with
each other; this is expected, since the pure-NLO result for pT (t) must not be dramatically

## PDF page 95

102

tt- production at the 8 TeV LHC

tt- production at the 8 TeV LHC

NLO (+ PS)

1.5

fNLO

0.5

0
1.05

NLO PY8
2

NLO PY6(Q )
NLO HW6

100

MadGraph5_aMC@NLO

1

σ per bin [pb]

101

MadGraph5_aMC@NLO

dσ/dpT [pb/GeV]

Unmerged (resc.)
Fx-Fx, µQ = 100 GeV

10-1
1.2

Ratio over unmerged

Ratio over NLO PY8

0.95

0.8
0

50

100

150

200
250
pT(t) [GeV]

300

350

400

0

50

100

150

200
250
pT(t) [GeV]

300

350

400

Figure 12. Transverse momentum of the top quark in tt̄ production. Left panel: comparison
between FxFx-merged (blue) and unmerged (red) predictions; the binning is the same as that of
ref. [350]. Right panel: NLO+PS predictions obtained with different PSMCs, compared to the
fNLO result.

modified by shower effects; such an expectation is confirmed by the fNLO prediction, also
reported in the right panel of figure 12 as the dashed histogram overlaid with full circles,
which is in fair agreement with all the other curves. We therefore conclude that it does not
seem possible to get NLO+PS predictions to agree with CMS data by changing the PSMC
used in the simulations. We also point out that this statement by no means implies that
acceptance corrections, which we do not compute here, are PSMC-independent; a careful
investigation of these may be necessary should the discrepancy discussed here persist, given
that pT (t) is not a quantity that can be measured directly.
Inclusive quantities that stem from either or both tops in tt̄ events are an ideal testing
ground for NLO+PS predictions, which should give a good description of the data for absolute normalisation as well as for shapes. On the other hand, tt̄ events are characterised
by large c.m. energies which imply a large amount of QCD radiation (only a tiny fraction of
which originate from the top quarks, owing to their being very massive). The study of such
radiation and of its topological properties is an interesting subject, particularly in view of
the large statistical accuracy that can be obtained at the LHC. At variance with the case
of inclusive observables, there is no reason to expect that all radiation-related observables
will be well described by NLO+PS tt̄ + 0j predictions. In particular, those for which large
jet multiplicities are important should be sensibly compared only to merged results, or at
least to unmerged samples whose underlying matrix elements feature a sufficiently large
number of hard partons — the most obvious example is that of Njet . On the other hand, for
radiation-related observables which are also inclusive enough, NLO+PS simulations should
do relatively well. One such case is that of the so-called gap fractions, which have been
measured in the dilepton channel by both ATLAS (at 7 TeV [352]) and CMS (at 7 [353]
and 8 TeV [354]), and compared to various theoretical predictions — MC@NLO with HERWIG6, POWHEG with both HERWIG6 and Pythia, MadGraph with Pythia, Alpgen

– 93 –

JHEP07(2014)079

1

1

## PDF page 96

with HERWIG6, and SHERPA. There are different levels of agreement among generators
and with the data, whose discussion is outside the scope of this work; here, we concentrate
on MC@NLO, since the relevant formalism is the same as that used in NLO+PS simulations
in MadGraph5 aMC@NLO. Before going into the details, let us define the main quantity
that we shall study, namely the gap fraction for the pT of the hardest jet. In order to be definite, we shall use the same setup as in ref. [354] (which is CMS’s at the 8 TeV LHC): jets are
reconstructed with the anti-kT algorithm with R = 0.5, and the following cuts are imposed:
pT (ℓ) ≥ 20 GeV ,

|η(ℓ)| ≤ 2.4 ,

pT (jb ) ≥ 30 GeV ,

|η(jb )| ≤ 2.4 ,

(4.10)

where σ is the cross section within the cuts of eq. (4.10), and for the notation of the
argument of the gap fraction we adopt one similar to that of ref. [352], which is not liable
to generate confusion. We have also introduced:
{
pT (j1 )
pT (j1 ) ≥ 30 GeV and ηmin ≤ |η(j1 )| ≤ ηmax ,
p̂T (j1 ) =
(4.12)
0
otherwise ,
with j1 the hardest jet which is neither of the two b-jets on which the cuts of eq. (4.10)
are applied. Note that if there is no jet harder than 30 GeV in the pseudorapidity interval
(ηmin , ηmax ), eq. (4.12) implies that the Θ function in eq. (4.11) is identically equal to one.
Therefore, GFpT (j1 ) (Q) is a constant for Q < 30 GeV, equal to the fraction of events which
do not have any jet harder than 30 GeV in the relevant pseudorapidity interval: for this
reason, gap fractions are not displayed in this range. The quantity p̂T (j1 ) in eq. (4.11)
can be replaced by a function, defined analogously to what is done in eq. (4.12) in terms
of any observable O with mass dimension equal to one; in this way, one constructs a
different type of gap fraction, GFO (Q). The transverse momentum of the second-hardest
jet [354], and HT [352, 354] have been considered in the literature; they are rather strongly
correlated with pT (j1 ), and will not be investigated any further here.
We now aim to compare the NLO+PS predictions of the MC@NLO program (v4.09)
with those obtained with MadGraph5 aMC@NLO (both NLO+PS and FxFx-merged),
which is interesting in two respects. Firstly, the unmerged NLO+PS results of the two
codes would be identical, were it not for the fact that in the latter we have included the
effect of the function D (see eq. (2.113)); therefore, any difference between the two is the
signal of matching systematics.57 Secondly, the comparison between unmerged tt̄ + 0j
and FxFx simulations helps assess the impact of the inclusion of matrix elements of
higher order in the latter. We have adopted HERWIG6 as PSMC, and the FxFx-merged
57

There may be other very tiny differences between MC@NLO and MadGraph5 aMC@NLO
NLO+PS predictions, owing to possibly non-identical choices of parameters, which are negligible for all
purposes.

– 94 –

JHEP07(2014)079

on both charged leptons, and on the two hardest b-jets. Other type of cuts (e.g. lepton
isolation) are seen to be unimportant, and are not imposed here. We then define:
∫
1
dσ
GFpT (j1 ) (Q) =
dΦ Θ (Q − p̂T (j1 ))
,
(4.11)
σ
dΦ

## PDF page 97

1

T 1

GFp (j )

0.9

Fx-Fx µQ = 30 GeV
Fx-Fx µQ = 155 GeV
MC@NLO
aMC@NLO

0.8
0.7

|η(j1)|<2.4

|η(j1)|<0.8

0.6

0.9
1.5<|η(j1)|<2.1

0.8<|η(j1)|<1.5
0.8

tt- production at the 8 TeV LHC

MadGraph5_aMC@NLO

T 1

GFp (j )

Ratio over aMC@NLO

1.02
1
0.98
100

200

300

400

Q [GeV]

100

200

300

400

Q [GeV]

Figure 13. Gap fraction for the pT of the hardest jet, in four different pseudorapidity intervals,
as predicted by FxFx-merged, unmerged (labelled aMC@NLO), and MC@NLO simulations. The
setup follows closely that of ref. [354]. See the text for details.

simulations have been performed for two extreme choices of the merging scale, µQ = 30
and 155 GeV. The results for the hardest-jet gap fraction are presented in figure 13, for the
same four pseudorapidity intervals (ηmin , ηmax )=(0, 2.4), (0, 0.8), (0.8, 1.5), and (1.5, 2.1) as
in ref. [354]; the insets display the ratios of the MC@NLO v4.09 and FxFx-merged results
over the unmerged MadGraph5 aMC@NLO ones. We first observe that all predictions are
quite close to each other, the largest deviation being about 3%. Interestingly, some of the
largest relative differences are between the two unmerged predictions, which implies that
the matching systematics is not negligible. In general, MadGraph5 aMC@NLO predicts
more jet activity (i.e., a lower curve) at NLO+PS than MC@NLO v4.09 in the central
and widest pseudorapidity regions, this difference decreasing with increasing ηmin . This
appears to be fairly consistent with what is seen in the 8-TeV CMS data (compare the
upper left corner of figure 13 with figure 7 in ref. [354], and the other panels of figure 13
with the upper row of figure 8 in ref. [354]), whose analysis we have followed here. A
similar trend as NLO+PS of MadGraph5 aMC@NLO is seen in the FxFx-merged result
with µQ = 155 GeV, while that obtained with µQ = 30 GeV follows a slightly different
pattern. Although these findings are encouraging, it is certaintly too early to draw any
firm conclusions; preliminarly, we can observe that the inclusion of more matrix-elements
results into matched predictions seems to be beneficial (be either through an NLO-merging

– 95 –

JHEP07(2014)079

1.02
1
0.98
1

## PDF page 98

no cuts
two jets

µQ = 20 GeV

µQ = 30 GeV

µQ = 50 GeV

µQ = 70 GeV

FxFx

14.47(−0.6%)

14.56

14.77(+1.5%)

14.78(+1.5%)

Alpgen

8.84(−0.9%)

8.92

9.08(+1.8%)

9.07(+1.7%)

FxFx

1.65(+0.8%)

1.63

1.60(−2.4%)

1.55(−5.4%)

Alpgen

1.27(+13.2%)

1.12

1.01(−9.5%)

0.92(−18.4%)

procedure, or because the D function limits the impact of the HERWIG6 shower to smaller
scales than it happens in MC@NLO). Furthermore, even by choosing an extremely large
range for the merging scale, the FxFx systematics is smaller than that of the MLM-type
merging in MadGraph5 aMC@NLO (see the results labelled MadGraph in ref. [354]).
We shall in fact see below another clear example of the pattern of the reduction of the
merging systematics when going from the LO to the NLO.
♦ Multi-parton merged predictions. We now turn to illustrate some results of the
FxFx merging which are directly relevant to the unitarity and the merging-scale-choice
arguments which have been discussed in general at the end of section 2.4.5. We shall do
so by using an example which one expects to be critical from these viewpoints, namely
Higgs production in gluon-gluon fusion (in HEFT) at the 8 TeV LHC, since such a process
is characterised by very large higher-order corrections and by a very significant amount of
radiation in PSMCs. As was done in ref. [191], we shall also compare to the predictions
obtained with Alpgen, which we shall take as a benchmark for the typical behaviour of LO
merging procedures; we have used HERWIG6 as PSMC. We start by presenting in table 12
the results for the fully inclusive rates, both in the absence of cuts (upper two rows), and
by imposing the presence of at least two jets (lower two rows): the latter are defined by
means of the anti-kT algorithm with R = 0.4, and have to obey the following conditions:
pT (j) ≥ 25 GeV ,

|η(j)| ≤ 5 .

(4.13)

The rates have been obtained by considering four different values for the merging scale,
which cover the very large range µQ ∈ (20, 70) GeV. In order to be definite, we shall
take µQ = 30 GeV as our central value; in table 12, we report in parenthesis the fractional
difference of all results obtained with µQ ̸= 30 GeV w.r.t. those obtained with µQ = 30 GeV
that appear in the same row. The rates in absence of jet cuts are seen to be extremely stable
against merging-scale variations. LO results have an only marginally-larger µQ dependence,
which is in any case much smaller than the scale uncertainty (not shown here); the same
applies to NLO predictions. The NLO fully-inclusive rate for the unmerged H + 0j sample
is 13.40 pb: it is therefore from 8% to 10% lower than the FxFx-merged results. Thus,
despite the fact that FxFx does not impose any unitarity condition, the merged predictions

– 96 –

JHEP07(2014)079

Table 12. Total rates (in pb) for single-Higgs production in gluon-gluon fusion in HEFT, resulting
from FxFx-merged (with up to two extra partons at the NLO) and Alpgen (with up to three extra
partons at the LO) samples. Fractional differences w.r.t. the corresponding results obtained with
µQ = 30 GeV are also reported.

## PDF page 99

Merged Higgs production at the 8 TeV LHC

Merged Higgs production at the 8 TeV LHC
100

Fx-Fx merging (≤2 partons, NLO)

µQ = 20 GeV, incl.

µQ = 50 GeV, incl.

µQ = 50 GeV, incl.

10-1

10-2

µQ = 70 GeV, incl.
2-jet cuts

10-1

10-2
Alpgen

2-jet cuts

σ per bin [pb]

µQ = 30 GeV, incl.

µQ = 20 GeV, incl.
µQ = 70 GeV, incl.

1.5

Alpgen, MLM merging (≤3 partons, LO)

µQ = 30 GeV, incl.

MadGraph5_aMC@NLO

σ per bin [pb]

100

1.5

µQ dependence, incl. (ratio over µQ = 30 GeV)

1

0.5
1.5

0.5
1.5

µQ dependence, ATLAS cuts (ratio over µQ = 30 GeV)

1

µQ dependence, ATLAS cuts (ratio over µQ = 30 GeV)

1

0.5

0.5
0

50

100
pT(H) [GeV]

150

200

0

50

100
pT(H) [GeV]

150

200

Figure 14. Higgs transverse momentum in single-Higgs production (gluon-gluon fusion in HEFT),
as predicted by FxFx (left panel) and Alpgen (right panel), for various choices of the merging
scale µQ .

are “naturally” quite close to the unmerged one. They are not equal, nor they should be
— at the end of the day, we are including here contributions up to O(αS5 ). The increase in
the cross section when passing from unmerged to merged results is rather consistent with
expectations based on perturbative scaling, and the known large NNLO/NLO K factor
that characterises the Higgs-production mechanism we study here. We stress that this
feature is not an accident of this process, since we have observed it in all cases studied
so far (see later for further examples). When considering rates obtained within the cuts
of eq. (4.13), we see that the NLO results are still quite stable, while the merging-scale
dependence of the LO ones becomes sizable. In order to further investigate this matter,
we present in figure 14 the Higgs transverse momentum spectra, obtained with FxFx and
Alpgen for the same four merging scales as before; the insets display the ratios of the
various curves over the µQ = 30 GeV corresponding ones. Obviously, the µQ -dependence
pattern reflects that of table 12. However, it is interesting to see that when no jet cuts
are applied there is a significant compensation in terms of rates in the Alpgen curves (this
can be clearly seen in the ratio plot, with the presence of a crossing point at a pT (H) of
about 70 GeV) — in other words, the very small µQ dependence of the LO total rates is
partly an artifact, since locally in the phase space the various predictions differ by a larger
amount. To some extent, the same is true for the FxFx-merged results, but the effects
are much more modest there. Note that, when jet cuts are applied, this phenomenon does
not occur any longer, and local and global merging-scale dependences are quite similar:
in particular, one sees how all the NLO curves are close to each other also within these
cuts. The significance of this (in)dependence is tightly related to the range chosen for the
merging scale variation. The function log(µQ /mH ), which one may take as an indicator of

– 97 –

JHEP07(2014)079

1

µQ dependence, incl. (ratio over µQ = 30 GeV)

## PDF page 100

µQ

(↓)

µQ

(c)

µQ

(↑)

unmerged

e

7059(−0.9%)

7121

7160(+0.5%)

7067(−0.8%)

pp → ZZ

7.383(−0.01%)

7.384

7.387(+0.04%)

7.355(−0.4%)

0.05180 (+0.9%)

0.05131

0.05117(−0.2%)

0.05066(−1.3%)

pp → e+ ν

pp → He+ ν

e

Table 13. Total rates (in pb) for three processes, computed with FxFx by using three different
merging scales (whose values are process-dependent, see eqs. (4.15)–(4.17)), and with the unmerged
lowest-multiplicity samples. Relative differences w.r.t the FxFx results obtained with the central
merging scales are also reported.

Mj1 j2 ≥ 400 GeV ,

|∆yj1 j2 | ≥ 2.8 ,

(4.14)

the mild dependences shown in table 12 become huge (of the order of 80% and 70% at the
LO and NLO respectively). It is clear that the invariant-mass cut of eq. (4.14) introduces
a third scale in the game which renders its treatment a complicated matter. Given that
such a large merging-scale dependence is basically driven by the largest µQ ’s, the problem
is likely due to intrinsic differences between the PSMC and matrix-element descriptions of
the VBF region. However, we are able to immediately notice this only because we have
considered a relatively large range of µQ , which does not give any issues for sufficiently
inclusive quantities, but it does when VBF cuts are applied. We conclude by pointing out
that the uncovering of this issue by means of merging-scale systematics does not imply
its most naive solution, which would be that of restricting, to small values, the range of
µQ in this kinematic region, thus relying on a matrix-element-dominated description: in
fact, such a description is not necessarily better than a PSMC one in the context of the
multi-scale dynamics induced by eq. (4.13) and (4.14).
In order to further the previous arguments, and as a way to validate the FxFx merging
procedure with a special attention to cases where the construction of the Sudakovs that
enter eqs. (2.139)–(2.141) is involved owing to the flavour structure of the hard process, we
consider here three different final states, namely e+ νe , ZZ, and He+ νe , which we simulate
at the 8 TeV LHC. In FxFx we include the 0-, 1-, and 2-parton samples for the former
process, and the 0- and 1-parton samples for the latter two. In all cases, the unmerged
0-parton results are also presented. All merged and unmerged samples are showered with
HERWIG6. We start with the fully-inclusive rates, reported in table 13; the values of the
three merging scales are as follows:
(↓)

(c)

(↑)

(µQ , µQ , µQ ) = (15, 25, 45) GeV

– 98 –

pp → e+ νe ,

(4.15)

JHEP07(2014)079

the typical quantity relevant when the merging scale is varied, changes by a factor of 3.16
in the range (20, 70) GeV considered here; we believe that this is a sufficiently-large range
to give a sensible indication of merging-scale systematics. As the results presented here
clearly show, the supposed spoiling of some underlying NLO accuracy that occurs when
“large” values of µQ are adopted is simply not an issue if NLO and MC predictions are
properly merged, and are reasonably consistent with each other. The latter is in fact a key
point: we have observed that, by imposing VBF-type cuts, e.g.:

## PDF page 101

102
101

102

1

10

101
100

µQ = 25 GeV

0

µQ = 45 GeV

10

102

1.2
1.1
1
0.9
0.8

101
100

1

10
d1 [GeV]

100

1

10

100

Figure 15. One-jet rate in e+ νe production. The main frame presents the three FxFx-merged
predictions as well as the unmerged one. The lower inset displays the ratios of these curves over the
central FxFx-merged one. The insets to the right show the separate contributions of the unphysical
0- (long-dashed), 1- (dashed), and 2-parton (dotted) samples, for the three merging scales.

101

2

10

102

1

10

101

no FxFx
µQ = 15 GeV

100

µQ = 25 GeV

0

σ per bin [pb]

100

µQ = 45 GeV

10

102

1.2
1.1
1
0.9
0.8

101
100

1

10
d2 [GeV]

100

1

10

100

Figure 16. As in figure 15, for the two-jet rate in e+ νe production.

– 99 –

σ per bin [pb]

σ per bin [pb]

102

σ per bin [pb]

+

FxFx merged e νe+0,1,2j production

JHEP07(2014)079

no FxFx
µQ = 15 GeV

σ per bin [pb]

100

σ per bin [pb]

σ per bin [pb]

2

10

σ per bin [pb]

+

FxFx merged e νe+0,1,2j production

## PDF page 102

σ per bin [pb]

10-1

10-2
10-3

-2

10

10-1
10-2
no FxFx
µQ = 45 GeV

-3

10

10-3

σ per bin [pb]

10-1

σ per bin [pb]

FxFx merged ZZ+0,1j production

10-1

1.05

10-2

1
10-3

0.95

1

10

100

1

10

100

d1 [GeV]

Figure 17. As in figure 15, for the one-jet rate in ZZ production. Only the 0- and 1-parton
samples have been considered here.

= (45, 65, 105) GeV
= (50, 75, 100) GeV

pp → ZZ ,

+

pp → He νe ,

(4.16)
(4.17)

which cover quite wide ranges. The message emerging from the table is analogous to
that relevant to Higgs production, which we have discussed previously: the merging-scale
dependence is very small. Furthermore, the unmerged results are extremely close to the
merged one, in fact much closer than in the case of gg → H; this is a natural consequence of
the relatively small (compared to Higgs) K factors for the present processes. Again, this
fact emerges naturally, without the need to impose any unitarity condition in the merging.
We conclude by showing some selected differential distributions, and in particular the j-jet
rates of the kT algorithm (denoted by dj , see eq. (2.131)); these quantities are known to
be critical in the context of merging procedures, since they are very sensitive to artefacts
of the latter, which show up as discontinuities in the spectra. Our results are presented in
figures 15–18, where the main frames display the predictions in absolute values. The lower
insets display the ratios of the FxFx-merged and unmerged predictions over the FxFx one
obtained with the central merging-scale values. The insets at the right of the figures show
the way in which the i-parton samples combine in order to give the physical curves. All
results for all processes behave as expected.
4.3

One-loop SM and BSM results: a look ahead

All the results presented in sects. 4.1 and 4.2 exploit the one-loop computations performed
by the public version of MadLoop5, which amply demonstrates the reach and flexibility
of this code. The aim of this section is on the other hand that of showing that the
current, still-private MadLoop5 program has a much larger scope, being able to handle

– 100 –

JHEP07(2014)079

µQ = 105 GeV

σ per bin [pb]

µQ = 65 GeV

## PDF page 103

σ per bin [pb]

10-3

10-4
10-5

-4

10

10-3
10-4
no FxFx
µQ = 50 GeV

-5

10

10-5

σ per bin [pb]

10-3

σ per bin [pb]

+

FxFx merged He νe+0,1j production

10-3

1.1

10-4

1
10-5

0.9

1

10

100

1

10

100

d1 [GeV]

Figure 18. As in figure 15, for the one-jet rate in He+ νe production. Only the 0- and 1-parton
samples have been considered here.

computations of very high complexity also in the context of a mixed-coupling expansion
(see section 2.4), and in theories other than the SM. As was already discussed, while the
corresponding capabilities on the real-emission side have not yet been fully validated in
MadGraph5 aMC@NLO, they do not pose any problem of principle, and only minor ones
from the technical point of view; therefore, the results presented below constitute the proof
that the major obstacles have been cleared which prevent MadGraph5 aMC@NLO from
performing NLO computations in arbitrary renormalisable theories.
We shall give here benchmark results for given phase-space configurations. They will
be presented in the form of the coefficients cj , j = −2, −1, 0, introduced in eq. (2.88) for
V , the colour- and helicity-summed virtual amplitude contracted with the corresponding
Born one (see eq. (2.55)). We shall also denote by a0 the Born amplitude squared:
∣2
∑ ∣∣
(n,0) ∣
A
(4.18)
a0 =
∣
∣ ,
colour
spin

where, similarly to V , the averages over initial-state colour and spin degrees of freedom
√
are understood. Throughout this section, we have set µ ≡ Q = µF = µR = s, and all
particles widths equal to zero for simplicity; the leptons that circulate in the loops are
taken to be massless. In order to maximize the numerical accuracy, the computations
reported here have been performed by using quadruple-precision arithmetics; the stability
tests described in section 2.4.2 have shown that these results are numerically stable
beyond the seventeen digits quoted below. The coefficients cj are computed in the ’t
Hooft-Veltman scheme and, in the case of the pole residues c−2 and c−1 , compared to
their analytically-known forms (see e.g. eq. (B.2) of ref. [61], whose generalisation to cases

– 101 –

JHEP07(2014)079

µQ = 100 GeV

σ per bin [pb]

µQ = 75 GeV

## PDF page 104

other than QCD is straighforward). Units for quantities of canonical dimension equal to
one are understood to be GeV. The CKM matrix is diagonal. The integral-reduction OPP
procedure has been adopted in all cases; processes C) and D) have also been computed
with TIR (using IREGI), and perfect agreement with the OPP results has been found. We
point out that processes A) and B) feature 8- and 7-point rank-5 loop integrals respectively,
and are therefore beyond the present capabilities of any TIR library. Further technical
details relevant to the calculations presented in this section are given in appendix C.2. We
emphasise that the one-loop results shown here have never been presented in the literature,
and can serve as benchmarks for comparisons with future independent computations.

Parameter

value

Parameter

value

αS

0.118

nlf

4

mt

173.0

mb

4.7

The kinematic configuration considered is (we use an (E, px , py , pz ) notation):
pg = ( 500

, 0

, 0

, 500

)

pg = ( 500

, 0

, 0

, -500

)

pd = ( 159.884957663500

, -100.187853644511

, 83.9823400815702

, 92.0465111972672

)

pd¯ = ( 203.546206153656

, -154.329441032052

, -0.512510195103158

, 132.714803257139

)

pb = ( 81.9036633616240

, 4.56741073895954

, -80.4386221767117

, 13.9601895942747

)

pb̄ = ( 41.5312244194448

, 6.99982274816896

, 9.96034329509376

, 39.4277395334349

)

pt = ( 239.961310957973

, 84.0110736983121

, 18.3862699981019

, -142.325385396572

)

pt̄ = ( 273.172637443802

, 158.938987491122

, -31.3778210029510

, -135.823858185543

)

For the O(αS6 ) Born matrix element and O(αS7 ) V coefficients we have obtained:
gg → d ¯
dbb̄tt̄
a0

1.7614866952133752e-14

c0

7.1888721656398052e-14

c−1

-3.8948541926529643e-15

c−2

-2.8670389920110557e-15

The relevant MadGraph5 aMC@NLO-shell generation command is:
MG5 aMC> generate g g > d d~ b b~ t t~ [virt=QCD]
More details on this syntax can be found in appendix B.1. After the generation phase,
the usual output and launch commands are executed. We point out, however, than in
the present context (i.e., when one computes one-loop matrix elements pointwise), launch
allows the user to specify the kinematic configuration for which the said matrix elements
are to be computed.

– 102 –

JHEP07(2014)079

¯ b̄tt̄. This process
A)
High-multiplicity multi-scale QCD process: gg → ddb
involves up to 8-point loop diagrams with three external scales: the top- and bottom-quark
masses, and the partonic c.m. energy. A total of 54614 loop diagrams contribute, and all
pure-QCD UV renormalisation counterterms are necessary, which makes it an excellent
test case for MadLoop5. The following parameters have been used:

## PDF page 105

Parameter

value

Parameter

αS

0.118

nlf

5

mt

173.0

yt

173.0

mW

80.419

mZ

91.188

125.0

α−1

132.507

mH

value

The kinematical configuration is:
pu = ( 500

, 0

, 0

, 500

)

pd¯ = ( 500

, 0

, 0

, -500

)

pd = ( 77.3867935143263

, -13.6335837243927

, 33.7255664483738

, -68.3039338032245

)

pd¯ = ( 251.029839835656

, -74.4940380485791

, -235.871950829717

, 42.7906718212678

)

pW + = ( 139.739680522225

, -81.0565319364851

, -74.5408139008771

, 30.5527158347332

)

pZ = ( 382.164100735946

, 208.038848497860

, 298.200182616267

, -74.3682536477996

)

pH = ( 149.679585391847

, -38.8546947884028

, -21.5129843340470

, 69.3287997950232

)

The corresponding Born results are:
¯ + ZH
ud¯ → ddW
O(αS2 α3 )
O(α α4 )

a0
2.8791434190645365e-16

S

-4.2378807039987007e-17

O(α5 )

5.8013051661550053e-18

where the O(αS α4 ) interference term happens to be negative, while at one loop we obtain:

– 103 –

JHEP07(2014)079

B)
Mixed-coupling expansion: ud¯ → d ¯
dW + ZH. The Born matrix elements
for this process receive contributions at O(αS2 α3 ), O(αS α4 ), and O(α5 ), resulting from
O(gS2 e3 ) and O(e5 ) amplitudes. In the notation of section 2.4, this corresponds to k0 = 5,
cs (k0 ) = 0, c(k0 ) = 3, and ∆(k0 ) = 2. We have considered the full set of NLO corrections,
thus obtaining four terms of O(αSn αm ), with 0 ≤ n ≤ 3 and m = 6 − n (see eqs. (2.22)
and (2.23)). This process features essentially all complications one faces in the case of
a mixed QCD-EW expansion, and in particular it tests fully the UV- and R2 -related
machinery, described in section 2.4.2, beyond the pure-QCD cases considered so far. From
a technical viewpoint, the major challenges are represented by the fact that genuine EW
corrections (as opposed to QCD corrections to processes that may feature EW external
particles) significantly complicate the flavour structure of the diagrams (whose number
therefore grows and which always pose a multi-scale problem), and by the necessity of
keeping separate track of the Σk0 +1,q coefficients of eq. (2.23). We have performed our
computation in the Feynman gauge, with an (α(mZ ), mZ , mW ) input scheme for the EW
parameters, and adopted the α(mZ ) renormalisation scheme [355] (we point out that the
Gµ scheme [355, 356] is also available in MadLoop5). The full set of inputs is thus:

## PDF page 106

¯ + ZH
ud¯ → ddW

O(αS2 α4 )

-4.9670212643498834e-17

3.5197577360529166e-18

c−1

-1.0437771535958436e-16

1.5619709675879874e-17

c−2

-2.8837935481452971e-17

3.9757576347989499e-18

c0

O(αS α5 )

O(α6 )

2.3220780285374270e-18

-1.4592469761033279e-18

c−1

-1.8146075843176133e-18

-5.0799804067050324e-21

c−2

-5.4147748433007504e-19

-5.4195415714279579e-21

The relevant MadGraph5 aMC@NLO-shell generation command is:
MG5 aMC> generate u d~ > d d~ w+ z h QCD=99 QED=99 [virt=QCD QED]
where the QCD=99 QED=99 bit instructs MadLoop5 to consider the corrections to all Bornlevel contributions, and not only to the leading (QCD) O(αS2 α3 ) one, while the [virt=QCD
QED] syntax implies that both QCD and QED/EW corrections need to be included. More
details on this extended syntax can be found in appendix B.1.
¯ t̄. Although the one-loop corrections to
C) Mixed-coupling expansion: uū → ddt
this process feature a smaller number of diagrams than those relevant to ud¯ → d ¯
dW + ZH
studied above, owing to the fact that the corresponding Born amplitudes have three
quark lines the mixed-coupling expansion ladder depicted in figure 1 is wider: we have
in fact ∆(k0 ) = 4, with k0 = 4, cs (k0 ) = 0, c(k0 ) = 0. The input-parameter and scheme
choices are the same as those adopted in the case of ud¯ → d ¯
dW + ZH production, while
the kinematic configuration is:
pu = ( 500

, 0

, 0

, 500

)

pū = ( 500

, 0

, 0

, -500

)

pd = ( 77.6887158960956

, -19.3895923374881

, 35.1636848900680

, -66.5063572263756

)

pd¯ = ( 288.053156184158

, -91.1103505191485

, -264.895455921162

, 67.1112676698377

)

pt = ( 218.623451637725

, -92.8925122931906

, -85.7235692614867

, 43.4702707482150

)

pt̄ = ( 415.634676282022

, 203.392455149827

, 315.455340292580

, -44.0751811916771

)

We thus obtain at the Born level:
¯ t̄
uū → ddt
O(αs4 )

O(αs3 α)
O(αs2 α2 )
O(αs α3 )
O(α4 )

a0
8.0443110796911884e-10
-4.1964024114099949e-11
3.2368049995513863e-11
-7.9030872133243511e-13
1.8667390802029741e-13

while the one-loop coefficients turn out to be:

– 104 –

JHEP07(2014)079

c0

O(αS3 α3 )

## PDF page 107

¯ t̄
uū → ddt

O(αs4 α)

2.7744575300036875e-10

-6.1309409133299879e-11

c−1

-2.4891722473717473e-10

5.1973614496390480e-12

c−2

-8.0573035150936874e-11

3.1296167547367972e-12

c0

O(αs3 α2 )

O(αs2 α3 )

1.2122291790182845e-11

-4.0611498141889722e-12

c−1

-8.6161115635612362e-12

4.3209683736654367e-15

c−2

-3.1860291930204890e-12

3.5961341456741816e-14

c0

O(αs α4 )

O(α5 )

-3.8642357648130340e-14

-1.1866388556893426e-14

c−1

-3.6050223887148020e-14

-4.7983631557836333e-16

c−2

-1.7642824564621470e-14

-2.4912793041300221e-16

The relevant MadGraph5 aMC@NLO-shell generation command is:
MG5 aMC> generate u u~ > d d~ t t~ QCD=99 QED=99 [virt=QCD QED]

D) A BSM case study: QCD corrections to gg → t̃1 t̃⋆1 g. While MadLoop has
been used to compute one-loop corrections to a very large number of processes in the SM,
its applications to other theories have been pretty limited so far. Here, we present the first
MadLoop5 results in a fully-fledged BSM model; namely, we compute QCD corrections
to t̃1 t̃⋆1 g production in the MSSM. From the technical point of view, the MSSM UFO
model at the NLO is immensely complicated, and its writing by hand (which has been the
procedure adopted for the SM) is inconceivable: we have therefore obtained it by using a
development version of FeynRules. All massive modes are subtracted at zero momentum,
following the same strategy as e.g. in ref. [357]. It should be pointed out that some of
the elementary expressions and structures of such a model (related e.g. to the presence of
Majorana fermions) are not featured in any other UFO model employed so far. For this
reason, we have double checked our MadLoop5 results against a completely independent
calculation performed with Mathematica. This guarantees that the elementary building
blocks are correct, thus rendering analogous tests more and more irrelevant in the future.
We have chosen the input parameters as follows:

– 105 –

JHEP07(2014)079

c0

O(αs5 )

## PDF page 108

value

Parameter

value

αS

0.118

nlf

4

mb

4.75

mt

175

mW

79.82901

mZ

91.1876

mg̃

607.7137

tan β

9.748624

mũ1

561.119

mũ2

549.2593

mc̃1

561.119

mc̃2

549.2593

mt̃1

399.6685

mt̃2

585.7858

md˜1

568.4411

md˜2

545.2285

ms̃1

568.4411

ms̃2

545.2285

mb̃1

513.0652

mb̃2

543.7267

with a diagonal squark-mixing matrix. By using the following kinematic configuration:
pg = ( 500

, 0

, 0

, 500

)

pg = ( 500

, 0

, 0

, -500

)

pt̃1 = ( 465.457552338590

, 88.1561012782457

, 197.510478842819

, -100.667451003198

)

pt̃⋆1 = ( 442.275748385439

, -9.53590501776566

, -180.889189039748

, 55.3271680251616

)

pg = ( 92.2666992759711

, -78.6201962604800

, -16.6212898030706

, 45.3402829780365

)

we obtain:
gg → t̃1 t̃⋆1 g
a0

2.839872059757065e-4

c0

-2.081163174420354e-5

c−1

-1.550338075591894e-4

c−2

-4.800024159745521e-5

The relevant MadGraph5 aMC@NLO-shell commands are:
MG5 aMC> import model loop MSSM
MG5 aMC> generate g g > t1 t1~ g [virt=QCD]
We point out that, similarly to the version of MadLoop5 used to derive the results presented
in this section, the loop MSSM model used here is not yet public.

5

Conclusions and outlook

The motivation for pursuing this project stems from the fact that all aspects of the
computations of tree-level and NLO cross sections, including their matching to parton
shower simulations, are well understood, in a manner which is fully independent of the
process under consideration. Therefore, the best way to make use of this understanding
is that of the full automation of such computations. Automation has indeed already
proven to be a very successful strategy for obtaining tree-level results, as documented
by the theoretical and experimental activities based on, and spurred by, MadGraph. In

– 106 –

JHEP07(2014)079

Parameter

## PDF page 109

– 107 –

JHEP07(2014)079

this paper we have presented the successor of MadGraph5, a code that we have named
MadGraph5 aMC@NLO, which extends the capabilities of the former by giving the
user the possibility of computing NLO QCD corrections, if desired in association with
parton-shower matching. MadGraph5 aMC@NLO is indeed the successor, and not just
a plugin, of MadGraph5, its main virtue being that of treating tree-level and NLO QCD
computations on the very same footing — as far as the user is concerned, the difference
between them is a switch in input. In particular, irrespective of the perturbative order
of the computation, MadGraph5 aMC@NLO features the following characteristics: very
lean dependencies, simplicity of use, and flexibility. The information that the user has to
provide is only related to physics, such as values of masses, couplings, and scales, and the
definitions of observables, as well as the hard process one wants to generate.
In the current public version of MadGraph5 aMC@NLO the inclusion of higher-order
effects is restricted to QCD corrections to SM processes. Such a limitation is mostly due
to the fact that, in the context of one-loop computations (performed by MadLoop or by
any other one-loop provider), one needs to take care of the UV renormalisation procedure
and (typically, but not always necessarily) of that related to the so-called R2 counterterms,
which are in any case just a simpler version of the former. Both procedures are expressed as
a set of rules that can be worked out directly from the Lagrangian, an operation that has to
be done only once for a given theory, and that so far has been performed by means of analytical computations. However, all obstacles preventing the automatic computation of the UV
and R2 rules have now essentially been cleared, as hinted by the results we have presented in
section 4.3. Given that all remaining obstacles are minor and of technical nature, this will
allow MadGraph5 aMC@NLO to evaluate, in the near future, any type of NLO corrections,
starting from the same user-defined Lagrangians that are used in tree-level calculations.
This work shows clearly that automated techniques at the NLO are well past the developmental phase, and are indeed fully established, as was already the case for their tree-level
counterparts; we believe that this is amply demonstrated by the results of section 4. For the
non-trivial cases now of relevance to collider phenomenology, automated computations are
more robust, faster by orders of magnitude, and less error-prone than analytical, processby-process traditional approaches. Furthermore, an increase in complexity generally only
requires more CPU power but no conceptually new solutions, one example of such a situation being that of the computation of EW or QCD corrections to supersymmetric processes.
As a counterexample, one may mention the calculation of cross sections that feature final
states with a very large number of QCD partons, for which dedicated optimisations (such
as recursive relations and colour reorganisation, which are being investigated by us) will
be needed in order to go beyond what is currently feasible by MadGraph5 aMC@NLO.
The ready availability in MadGraph5 aMC@NLO of perturbatively-accurate and realistic predictions for an extremely large range of processes of significant complexity should
be seen as both solving a few problems, and opening up new and exciting possibilities.
Among the former, we would like to mention explicitly the fact that automated tools help
free experts in perturbative calculations from spending their resources in the increasingly
involved computations necessary to the experiments, thus allowing them to concentrate on
obtaining other, cutting-edge results (such as, to limit oneself to perturbative QCD, cal-

## PDF page 110

Acknowledgments
We are grateful to Roberto Pittau for his support of CutTools, to Stefan Prestel for his
dedicated help with the NLO matching to Pythia8 and for discussions on related topics, to
Matteo Cacciari for his help and support with FastJet (core), to Andreas Papaefstathiou
for his dedicated help with Herwig++, to Simon Badger, Daniel Maitre, and Markus
Schulze for clarifications concerning bootstrap and D-dimensional unitarity methods, to
Markus Cristinziani and Roberto Chierici for information on top-physics measurements by
ATLAS and CMS, to Adam Alloul, Neil Christensen, Celine Degrande, Claude Duhr and
Benjamin Fuks for their collaboration to BSM developments and support of FeynRules,
to Frank Krauss for explanations on the use of the MC@NLO method in SHERPA,
to Simon de Visscher for his help with LO merging, to Pierre Artoisenet and Robbert
Rietkerk for their work on MadSpin, to Valery Yundin and Andreas van Hameren for their
support of PJFry++ and OneLoop, to Diogo Buarque Franzosi for his collaboration on
the implementation of the complex mass scheme, to Alexis Kalogeropoulos for his contributions in developing and testing large-scale event production, to Kentarou Mawatari for
many fruitful collaborations, to Stefano Pozzorini, Peter Skands and Torbjörn Sjöstrand
for useful clarifications, to Josh Bendavid, Vitaliano Ciulli, and Sanjay Padhi for the very
useful feedback on the use of the code, and to Michelangelo Mangano for his support
and insight. We are thankful to our cluster management team, Jerôme de Favereau,
Pavel Demin, and Larry Nelson, for their help and collaboration over the years. FM
and TS are particularly thankful to Kaoru Hagiwara for the constant support and many

– 108 –

JHEP07(2014)079

culations of NNLO accuracy with universal subtraction methods, improvements to parton
showers, and so forth). As far as future possibilities are concerned, one important characteristic of MadGraph5 aMC@NLO to bear in mind is its modularity: we shall be happy
to support and help those interested in improving parts of the code and the underpinning
physics strategies (such as recursive relations, alternative matching and merging schemes,
integral-reduction techniques and libraries). From a phenomenological viewpoint, many
different applications of MadGraph5 aMC@NLO can be foreseen. The capability of the
code to assess systematically and in an easy manner the theoretical uncertainties due to
scales, PDFs, and matching and merging methods should be routinely exploited by both
theorists and experimentalists. The fact of having a basically unlimited set of processes
predicted at the NLO accuracy has two immediate consequences: it gives one the chance
of extracting the PDFs by using a much wider set of observables than employed at present,
at the same time possibly including EW and parton-shower effects; and that of finally
achieving PSMC tunings that properly include NLO results. Exploratory studies at future
colliders, such as circular or linear e+ e− ones, or very-high-energy hadron machines, can
also be performed without the need of a dedicated effort. Finally, it is hard to predict
the kind of applications that will be relevant to BSM physics. In any case, extending the
current flexibility of MadGraph5 aMC@NLO for SM processes to new-physics models, be
they renormalisable or effective, and thus being able to readily investigate the implications
of any theory, will certainly be crucial in current and future analyses.

## PDF page 111

A

Technical prerequisites, setup, and structure

MadGraph5 aMC@NLO is being developed and is routinely run on a variety of Linux

platforms and on Mac OS-X systems. The basic requirements for running the code are
the following:
• A bash shell;
• perl 5.8 or higher;
• Python 2.6 or higher, but lower than 3.0;
• gfortran/gcc 4.6 or higher; any other modern Fortran/C++ compiler should work,
provided it supports computations in quadruple precision.
After downloading the tarball, and upacking it in what will be called the main directory
(which will contain several sub-directories, such as aloha, apidoc, bin, and so forth), the
code is ready to run. No installation of external packages is mandatory, thanks to the fact
that the tarball includes copies of the third-party codes listed in appendix D.
Setup. From a terminal shell in the main directory, type:
./bin/mg5 aMC
At this point, one has entered the MadGraph5 aMC@NLO shell, which is made evident
by the fact that the prompt now reads as follows:

– 109 –

JHEP07(2014)079

insightful suggestions since the very beginning of the MadGraph project. SF wishes to
thank Bryan Webber for his collaboration, over the course of many years, on several of
the topics discussed in this paper. The authors not based at CERN are grateful to the
PH/TH Unit for the support and hospitality in many different occasions. This work has
been supported in part by and performed in the framework of the ERC grant 291377
“LHCtheory: theoretical predictions and analyses of LHC physics: advancing the precision
frontier”, supported in part by the Swiss National Science Foundation (SNF) under
contract 200020-149517, by the European Commission through the “LHCPhenoNet”
Initial Training Network PITN-GA-2010-264564, by the Research Executive Agency
(REA) of the European Union under Grant Agreement number PITN-GA-2012-315877
(MCNet). The work of FM and OM is supported by the IISN “MadGraph” convention
4.4511.10, by the IISN “Fundamental interactions” convention 4.4517.08, and in part
by the Belgian Federal Science Policy Office through the Interuniversity Attraction Pole
P7/37. OM is “Chercheur scientifique logistique postdoctoral F.R.S.-FNRS”, and wishes
to thank the IPPP Durham for the kind hospitality extended to him during his stay
there. The work of FM has been supported by the Francqui Foundation via a Francqui
Research Professorship. The work of MZ has been partly supported by the ILP LABEX
(ANR-10-LABX-63), in turn supported by French state funds managed by the ANR within
the “Investissements d’Avenir” programme under reference ANR-11-IDEX-0004-02. VH
is supported by the SNF with grant PBELP2 146525. This material is based upon work
supported in part by the US National Science Foundation under Grant No. PHY-1068326.

## PDF page 112

Structure. The various subdirectories of the main directory will be of no interest to the
regular user. The only possible exceptions are
Template/NLO
Template/LO
a copy (with minor differences) of which is created in the subdirectory
MYPROC
of the main directory upon executing the command:
MG5 aMC> output MYPROC
after having executed one of the two following commands:
MG5 aMC> generate a b > c 1...c n [QCD]
MG5 aMC> generate a b > c 1...c n
for the NLO and LO case respectively (see section 3). The minor differences in the copy
alluded to before are due to the fact that, after the generate command has been issued,
the program knows e.g. the number of final-state particles (equal to n in the examples given
here), which is thus explicitly written in some include files in the directory tree of MYPROC.
In any case, these include files and their analogues must not be modified by the user.
The directory MYPROC will be called the current-process directory, and all the operations
relevant to the process whose generation gave rise to it are performed somewhere in its
directory tree. Such operations can roughly be arranged in two classes: input-type, to
be performed by the user before the launch command, and output-type, performed by
MadGraph5 aMC@NLO after the launch command.
The user may consider input-type operations in the following subdirectory:
MYPROC/Cards
58

We point out that FastJet (core) is part of the MadGraph5 aMC@NLO tarball.

– 110 –

JHEP07(2014)079

MG5 aMC>
A minimal setup phase may take place here, before generating and running the first
process. This phase, that must be done at most once (i.e., it does not have to be
repeated before the generation of any process after the first), consists essentially in
defining configuration variables. For example, in the case where a local installation of
FastJet were available,58 the path to it must be known by MadGraph5 aMC@NLO: this
is achieved by executing the following command:
MG5 aMC> set fastjet /<PATH TO FASTJET>/bin/fastjet-config
Likewise, for the local installation of LHAPDF [366] to be found, one should execute the
command:
MG5 aMC> set lhapdf /<PATH TO LHAPDF>/bin/lhapdf-config
Each of these commands associates the given value with a variable in the file:
input/mg5 configuration.txt
The user can find a list of all possible configuration variables by visiting that file (or
by auto-completion with the <TAB> key after typing set in the MadGraph5 aMC@NLO
shell). We point out that each of these variables can be directly edited in the file, as an
alternative to executing the set command as shown above. More advanced setup options
are described in appendix B.1.

## PDF page 113

1. For all types of runs: various plain-text files that summarise the inputs used and the
results of the integration of the short-distance cross sections.
59

Runs may e.g. differ by choices of input parameters, or type of physics simulated, such as f(N)LO vs
(N)LO+PS, or the inclusion of spin correlations as predicted by MadSpin vs stable-particle production.

– 111 –

JHEP07(2014)079

which contains the input cards (these are in plain text format, and liberally commented)
that steer the MadGraph5 aMC@NLO run (e.g., run card.dat) or control the physical
parameters of the theory (e.g., param card.dat). Contrary to other input-type operations,
which will be mentioned below, the values of the entries in the input cards can not only
be modified by the user by visiting the appropriate cards before the launch command,
but can also be accessed after the launch command through an interactive talk-to within
the MadGraph5 aMC@NLO shell. Both accessing modes can be used in the same run;
note that the values of the inputs used in the actual run will be those stored in the input
cards at the end of the talk-to phase.
Further input-type operations are specific to NLO-type generations, require a minimal
knowledge of Fortran, and must be completed before the launch command is issued. They
will involve editing files in the following subdirectories:
MYPROC/FixedOrderAnalysis
MYPROC/MCatNLO
MYPROC/SubProcesses
The FixedOrderAnalysis subdirectory will need to contain the user’s fixed-order analysis
file(s) relevant to fLO or fNLO runs. The MCatNLO subdirectory is used only in the case
when the user chooses to steer the shower phase within the MadGraph5 aMC@NLO framework; when the LHE files produced by MadGraph5 aMC@NLO are showered externally,
such a subdirectory is ignored. If also the showering is steered by MadGraph5 aMC@NLO,
the user will be able to access the drivers of the various event generators, and to write
his/her own analysis inside the MCatNLO directory tree (whose structure is analogous to
that of the MC@NLO package, for those familiar with it). Finally, the subdirectory
SubProcesses contains the codes necessary for the computation of the cross section proper,
and specific to the process that has been constructed in the generation step. Typically, the
user will not need to modify any of these files; exceptions are those of setscales.f, where
one defines the functional forms used for dynamic-scale computations (see section B.2),
and of cuts.f, where one sets any desired parton-level cuts (on top of those accessible
through run card.dat); both of these files are amply commented.
As far as output-type operations are concerned, these are by definition dealt with by
MadGraph5 aMC@NLO; we shall mainly describe in what follows those relevant to an
NLO-type generation. The relevant directories are
MYPROC/Events/run *
There will be as many run * subdirectories as number of runs;59 the string * will feature
a run-identification number. These subdirectories will contain the final outputs of the
corresponding MadGraph5 aMC@NLO runs, provided that such outputs are in one of the
formats recognised by the code. In particular, one will have:

## PDF page 114

2. In (N)LO+PS runs: the Les Houches event file(s) that contain hard-subprocess unweighted events which are to be showered.
3. In (N)LO+PS runs when MadGraph5 aMC@NLO is used to steer the shower phase:
the final results after shower, provided that these are either: a) an StdHEP/HepMC
file that contains the event records; or b) a topdrawer file that contains histograms
defined by the user in his/her analysis.
4. In f(N)LO runs: the histograms defined by the user in his/her analysis, provided that
their format be either Root or topdrawer.

B

Advanced usage

This section reports on some of the features of MadGraph5 aMC@NLO whose understanding allows the user to exploit the full physics potential of the code. It is not meant to be
60

This assumes the output is a set of histograms. In case of n-tuples, these will need to be combined,
possibly after having rescaled their weights.

– 112 –

JHEP07(2014)079

There is no problem if the format of the output of the user’s analysis relevant to the shower
phase (when MadGraph5 aMC@NLO is used to steer the shower) is not compliant with
either 3.a or 3.b. Simply, such an output will not be moved into MYPROC/Events/run *,
but will be kept in the directory where the PSMC run has actually been performed. This
directory will be named:
MYPROC/MCatNLO/RUN MCTYPE nn
with MCTYPE=PYTHIA8 and so forth (depending on the PSMC used), and nn an integer
number increased by one unity for each new PSMC run.
On the other hand, the use of formats other than Root or topdrawer in f(N)LO runs
is deprecated, since it implies some manual operations and the writing of code by the user.
The reason is the following: cross sections are integrated by MadGraph5 aMC@NLO
through multi-channel techniques — this ensures optimal convergence and high degree of
parallelisation, but each channel is non-physical (only their sum is). Analysis routines
(regardless of the output format) are used by individual channels; hence, their outputs are
to be summed.60 Summing the results of the individual channels is performed automatically
by MadGraph5 aMC@NLO for Root and topdrawer outputs, via dedicated auxiliary codes;
any new format would thus require the user to write a new such code, and a script that
finds all single-channel outputs and feed them to his/her summing code.
We conclude this section by stressing again that the source codes which are compiled
after executing the command launch, and the input cards used throughout the run,
are those in the current-process directory tree, and not in the Template directory tree.
Therefore, any modifications to files in the Template directory tree will have no effect
on the current run. However, they will affect all subsequent process generations, since
as clarified at the beginning of this section it is the files in Template that form the core
of the contents of each current-process directory. Hence, this procedure is reserved to the
very experienced users, and we strongly deprecate it.

## PDF page 115

a usage manual, but only to briefly expand on some of the subjects which have been only
touched upon in the main text.
B.1

Models, basic commands, and extended options

We start with the following general comment: within the MadGraph5 aMC@NLO shell,
the <TAB> key plays the same role as in a normal terminal shell: when hitting it, a list
of possible completions (e.g., commands relevant to the current context, or completion of
the command syntax) is printed on the screen. Note that the shell commands help and
tutorial can be used as well, and will provide the user with some minimal guidance.

– 113 –

JHEP07(2014)079

Models. As was explained in section 2.1, MadGraph5 aMC@NLO needs a model in
order to generate a process. When one enters the MadGraph5 aMC@NLO shell, the
default is that of assuming the SM: however one can choose to work in another theory by
loading a new model, by simply executing the command:
MG5 aMC> import model ModelName
where ModelName is the name of the desired model. The list of available models (to
which as usual the user can add his/her own) can be obtained by hitting the <TAB> key
after import model. Each of these models is associated with a directory (under the main
directory):
models/ModelClass
In the directory ModelClass, one collects the definition of all those models which are tightly
connected with each other, for example by having the same Lagrangian and differing by
the choice of some fundamental parameter. To give an explicit example: the default model
for the SM in MadGraph5 aMC@NLO assumes the charm quark to be massless, but there
is a model where the charm quark is massive. For both of these, we have:
models/ModelClass ≡ models/sm
The massless-charm or massive-charm SM is explicitly loaded by typing:
MG5 aMC> import model sm
MG5 aMC> import model sm-c mass
respectively. Technically, these two commands are in one-to-one correspondence with the
two files:
models/sm/restrict default.dat
models/sm/restrict c mass.dat
The user interested in some non-extensive modification of the SM can thus simply create his/her own file models/sm/restrict XXX.dat, which may be eventually loaded
by executing import model sm-XXX. For more details on these matters, please visit:
https://cp3.irmp.ucl.ac.be/projects/madgraph/wiki/Models/USERMOD.
We finally stress again that not all models support the computation of NLO corrections.
In the first public version of MadGraph5 aMC@NLO such corrections are restricted to
QCD to SM processes. The relevant models are all found in the directory:
models/loop sm
Note that, by default, when performing an NLO-type generation (i.e., by using the [QCD]
keyword) the code switches automatically from the LO-type model to the corresponding

## PDF page 116

NLO-type one (i.e., in the SM it switches from sm to loop sm). If the latter is not available,
a warning is issued and the code proceeds no further.

Generation. The most general form of the generate command is the following:
MG5 aMC> generate Process {AmpOrders} [{{Mode} Couplings}]
the only mandatory option being Process, i.e. the actual process one needs to generate. We
shall now comment on the four options above in turn.
The option Process is simply the list of initial- and final-state particles, separated by
the conventional > sign:
Process ≡
a b > c 1...c n
One can further refine the syntax above in order to include in the computation only some
of the contributions that one would normally obtain. Such refinements are reported in
table 14, and have the following meaning:
s.1 A production process is generated that features x in the final state, with x subsequently decaying into the list of particles that follow the “x >” string; more in general,
there may be p primary particles that play the same role as x. Only p-resonant diagrams (see section 2.5) are included in the computation. In the example of table 14,

– 114 –

JHEP07(2014)079

Setup. A short description of the setup procedure has been already given at the beginning
of appendix A. Here, we wish to point out that, on top of the environment variables
found in input/mg5 configuration.txt, the user can also control other options, which
for example affect the physics schemes used by MadGraph5 aMC@NLO during the various
computations. All such options can be listed with the following command:
MG5 aMC> display options
which will display all options and their current values. In order to change the latter, one
executes the set command, whose general syntax is:
MG5 aMC> set Option Value
For example, MadGraph5 aMC@NLO by default does not use the complex mass scheme
in its computations. In order to change this, it is sufficient to execute:
MG5 aMC> set complex mass scheme True
Other examples relevant to environment variables have already been given in appendix A.
The operation of computing the widths of the unstable particles present in the imported
model can be seen as part of the setup procedure, being a complement to the model itself,
independent of the generation procedure, and mandatorily performed before the running
phase (see section 2.3.2). Such an operation is carried out by issuing the shell command:
MG5 aMC> compute widths [{Options}]
which in turn executes the MadWidth module; the possible options of the above command
can be as usual explored by hitting the <TAB> key. We remind the reader that MadWidth
works at tree level and in the narrow-width approximation (in other words, the manual
setting of widths in the context of an NLO simulation may be necessary).
Finally, another setup-type operation is the diagonalisation of the mass matrix. This is
only available in a restricted class of UFO models which include the AsperGe [89] module,
whose inputs are accessible to the user during the interactive talk-to phase.

## PDF page 117

syntax

example

meaning

x, x>

p p > z j, z > b b~

s.1

$ x

p p > e+ e- $ z

s.2

/ x

p p > e+ e- / z

s.3

> x >

p p > z > e+ e-

s.4

$$ x

p p > e+ e- $$ z

s.5

one has the associated production of a Z and a jet, with the Z further decayed into
a bb̄ pair. Spin correlations and x off-shell effects are taken into account exactly, but
the virtuality m⋆x of x is forced to be in the following range:
|m⋆x − mx | ≤ bwcutoff Γx ,

(B.1)

where mx is the pole mass of x, Γx its width, and bwcutoff is a parameter controlled
by the user (through run card.dat). Syntax s.1 thus loosely imposes an on-shell
condition; it is called decay-chain syntax, and can be iterated: any decay product
can be decayed itself by using this syntax (e.g. x > y z, y > w s).
s.2 If x appears as an intermediate particle in the generated process, its virtuality is
forced to be in the range:
|m⋆x − mx | > bwcutoff Γx ,

(B.2)

which is the region complementary to that of eq. (B.1), and thus loosely imposes
an off-shell condition. All diagrams are kept. In the example of table 14, one has
Drell-Yan production with the invariant mass of the e+ e− pair larger than or smaller
than the Z mass by at least bwcutoff ΓZ . A consequence of the complementarity
mentioned above is that, while cross sections generated with either s.1 or s.2 are
bwcutoff-dependent, their sum is not (up to interference terms, which are neglected
by the process of discarding non-resonant diagrams in s.1 ), and corresponds to the
process generated with the simplest syntax. For example:
dσ
dσ
dσ
(p p > z) ≃
(p p > z, z > e + e−) +
(p p > e + e − $ z) , (B.3)
dO
dO
dO
for any observable O.
s.3 All diagrams that feature (anywhere) the particle x are discarded.
s.4 The process is generated by demanding that at least one particle of type x be in an
s-channel.
s.5 All diagrams that feature the particle x in an s-channel are discarded.

– 115 –

JHEP07(2014)079

Table 14. Process-generation syntax refinements, also exemplified in the case of various processes
that involve a Z boson. See the text for the explanation of the keywords s.1 –s.5. Only syntaxes
s.3 –s.5 are supported for NLO-type generations.

## PDF page 118

p + p −→ W + + Jb + Jlight ,

(B.4)

where Jb and Jlight are a b- and a light-jet respectively, and the five-flavour scheme is
adopted. Numerically, the dominant contributions to such a process are due to diagrams
whose corresponding amplitudes factorise the couplings gS2 gW . However, amplitudes of
3 are more interesting, since they feature diagrams with one top-propagator
order gW
exchange, and are thus identified with single-top production (although of course at the
same order one has non-resonant diagrams as well). By executing the command (after
including the b-quark in the proton)
MG5 aMC> generate p p > w+ b j
one would obtain only the amplitudes of O(gS2 gW ), the choice being made by the code automatically according to the hierarchy shown above. In order to study single-top production,
one can execute what follows instead [214]:
MG5 aMC> generate p p > w+ b j QED=3 QCD=0
3 ) amplitudes. Note that, by entering
which will force the code to consider only O(gW
3 ) amplitudes. In future version of
QED=3 QCD=2, one will generate both O(gS2 gW ) and O(gW

– 116 –

JHEP07(2014)079

We stress that all syntaxes but s.2 produce in general results which are non physical, because gauge invariance might be violated (although there are exceptions: see e.g. ref. [214]),
and have therefore to be used with extreme caution. The situation becomes more involved
at the NLO, so even more care is required. Syntaxes s.3, s.4, and s.5 are supported; more
refined selections of individual loop diagrams in MadLoop5 can be imposed by editing the
function user filter in the source code loop diagram generation.py.
The option AmpOrders allows the user to specify the upper bounds on the powers
of the coupling constants that enter the scattering amplitudes (i.e., not the amplitudes
squared); therefore, the coefficients Σk0 +p,q are selected only in an indirect manner —
see section 2.4. Furthermore, in the case of an NLO-type generation, such amplitudes
are the Born ones: the couplings of the one-loop and real-emission amplitudes are then
automatically determined according to the type of corrections to be included. The syntax
for this option is the following:
AmpOrders ≡
coupling1 = p1 coupling2 = p2 . . . couplingn = pn
where couplingi is the name of the ith coupling in the model currently used, and p1 is
an integer which represents the upper bound mentioned above. It should be obvious that
couplingi is an arbitrary name, chosen by the author of the model in use. In order to see
the list of all coupling names, one has just to type (after having imported the model):
MG5 aMC> display coupling order
For example, by executing this command in the context of the SM, one obtains what
follows:
QCD : weight = 1
QED : weight = 2
which implies that the internal names of the SM couplings gS and gW is QCD and QED
respectively, with the latter being hierarchically suppressed w.r.t. the former. As an explicit
example of the use of the AmpOrders option in the SM, let us consider the case of:

## PDF page 119

MadGraph5 aMC@NLO, the syntax of the option AmpOrders will be extended, so as to

Output. The most general form of the output command is the following:
MG5 aMC> output [OutputForm] [MYPROC]
As was already mentioned in section 3 (see in particular footnote 42) the target-directory
name MYPROC may be omitted, in which case MadGraph5 aMC@NLO will choose automatically a name (and print it out on the screen for the user to know). As the full syntax
above implies, however, there are a few names that are reserved because, if used, the code
will interpret them as one of the (optional) OutputForm keywords. These essentially serve
to create executables (or standalone libraries) which are not those typically used for the
integration of the cross sections and the unweighting of the events. They are described in
appendix B.6.
Running. The most general form of the launch command is the following:
MG5 aMC> launch {ProcDir} {RunMode} {Options}
61

The use of which requires the use of the option Couplings as well. The opposite is not true.

– 117 –

JHEP07(2014)079

give the user the possibility of selecting directly cross-section-level quantities (Σk0 +p,q ’s),
at both the leading and the next-to-leading order.
The option Mode 61 allows the user to select which contributions to an NLO cross
section (on top of that due to the Born, which is always present) will be included in the
computation. The possible settings are the following:
Mode ≡ all=
=⇒ both one-loop and FKS-subtracted real-emission
Mode ≡ real=
=⇒ only FKS-subtracted real-emission
Mode ≡ virt=
=⇒ only one-loop
The setting all= is equivalent to omitting the option Mode altogether, and should be
the only one considered by the non-expert user, being the only one that leads to physical
results. The setting real= instructs MadGraph5 aMC@NLO to not generate the part of
the code relevant to virtual matrix elements with MadLoop. In this way, the cross section
can still be dealt with as explained in section 3, but the results will be non-physical, unless
an external one-loop provider is linked to MadGraph5 aMC@NLO (such an external OLP
will thus effectively play the same role as MadLoop). Finally, the setting virt= corresponds
to the MadLoop standalone mode. In such a mode, the commands output and launch will
behave differently w.r.t. what is described in section 3, the idea being that of using the code
so generated in order to obtain the pole residues and finite part of the virtual corrections
for user-defined kinematic configurations — see section 4.3 for explicit examples.
The option Couplings allows the user to specify which kind of NLO corrections MadGraph5 aMC@NLO will compute. The general syntax for this option is the following:
Couplings ≡
coupling1 coupling2 . . . couplingn
However, in the current version only QCD corrections can be computed, and therefore the
only valid option read as follows:
Couplings ≡
QCD
as already mentioned several times in this paper. For examples of the more general syntax
that can be used in a still-private MadGraph5 aMC@NLO version, see section 4.3.

## PDF page 120

B.2

Setting the hard scales at the NLO

The short distance NLO(+PS) cross sections in MadGraph5 aMC@NLO feature three
hard scales: the renormalisation (µR ), factorisation (µF ), and Ellis-Sexton (QES ) scales.
The latter appears only at the NLO and, at variance with the former two, its variations
do not induce any changes in the cross sections. For this reason, QES is only useful in the
context of validation studies, performed by developers; regular users are recommended to

– 118 –

JHEP07(2014)079

We cannot possibly describe in this paper all possibilities implied by the syntax above,
which we plan to do in a forthcoming user manual; we urge the interested reader to explore
them by either using the on-line tutorial, or executing the help launch command, or
exploiting the <TAB> key.
Here, we limit ourselves to point out that ProcDir, if present, must coincide with one
of the current-process directories previously generated. The implication is that, after the
generation and output phase, a user may not immediately run the process, but rather
generate a second one, or also quit the MadGraph5 aMC@NLO shell. Being saved on
disk, the full information of a generated and outputed process can be retrieved at any later
time. In order to do this, one needs simply to execute:
MG5 aMC> launch MYPROC -i
where MYPROC is the name of the current-process directory used throughout this paper.
It should be clear that, upon executing the command above, one is again dealing with a
specific current process. For this reason, many early-stage commands (such as generate)
are disabled. In order to help the user remind this fact, the prompt itself is actually
changed, and reads:
MYPROC>
In short, we shall call the environment accessed by executing the launch -i command
the running mode. One can re-enter the running mode of a given process an unlimited
amount of times. Again, we shall not attempt to give here a full description of the various
implications of this fact. However, it is interesting to discuss a specific usage in connection
to what has been described in section 3.2.1, and namely how to shower hard-subprocess
event files previously generated. For example, we have discussed in section 3.2.1 how, in the
case of a process which features particles whose decay products are dealt with MadSpin,
one obtains (at least) one undecayed and one decayed hard-event files, for example:
MYPROC/Events/run 01/events.lhe.gz
MYPROC/Events/run 01 decayed 1/events.lhe.gz
only the latter of which is showered by default when MadGraph5 aMC@NLO steers the
shower. In order to shower the former, one simply has to execute:
MG5 aMC> launch MYPROC -i
MYPROC> shower run 01
Namely, to access the running mode of the relevant process directory, and then execute
the command shower followed by the name of the subdirectory of the Events directory
where the events to be showered are stored. We point out that the shower command can
be executed any number of times with the same argument, e.g. if one desires to change the
seeds or the parameters in the PSMC.

## PDF page 121

always set it equal to the factorisation scale. In view of the standard way of performing
scale variations, it is convenient to write the hard scales as follows:
µR = fR µR 0 ,

µF = fF µF 0 ,

QES = fES QES0 ,

(B.5)

µR0 = muR ref dynamic .

(B.6)

The quantity muR ref dynamic is a function of the four-momenta of the final-state particles; its body is found in the file MYPROC/SubProcesses/setscales.f, where the user may
include his/her definition of the dynamical scale best suited to the process of interest. Although a few examples of typical dynamical scales are given in the version of setscales.f
which is included in the tarball of the package, we urge the user to study the structure
of that file (which is amply commented — note, in particular, the role of the variable
temp scale id in that file, which helps keep track of the functional forms used), and to
change it if need be. It should be clear that setscales.f follows the same rules as all
the other core files of the package (see section A). Hence, in order for any modifications
to it to be taken into account in the current run, one must edit the file before the launch
command is issued.
What said above for the renormalisation scale applies without changes to the factorisation and Ellis-Sexton scales; the relevant parameters and functions in run card.dat and
setscales.f have self-explanatory names. Note that, in the case of the factorisation scale,
one can in principle assign two different values to the two incoming hadrons — hence, in
the input cards one can find the variables * ref fixed and * over ref, with *=muF1 and

– 119 –

JHEP07(2014)079

where µR0 , µF 0 , and QES0 are called reference scales.
Hard scales must be set by the user prior to compiling and running the code. They
can be organised into two categories, typically called “fixed” and “dynamical”; the scales
belonging to the former have constant values, independent of the event kinematics, while
those belonging to the latter depend on the four-momenta of the final-state particles, and
hence have values that change event-by-event during the course of the run. Whether a
scale is fixed or dynamical is determined by an input parameter. For example, in the case
of µR , the following setting in run card.dat:
T = fixed ren scale ! if .true. use fixed ren scale
will instruct the code to use a fixed renormalisation scale. Such a fixed value is also given
by the user in input by setting the pre-factor fR and the reference scale µR0 that appear
in eq. (B.5). For example, the following entries in run card.dat:
91.188 = muR ref fixed ! fixed ren reference scale
2
= muR over ref ! ratio of current muR over reference muR
set µR0 = 91.188 GeV and fR = 2 respectively, and hence µR = 182.376 GeV.
We now address the case of dynamical scales, again using the renormalisation scale to
give definite examples. A dynamical µR is used when:
F = fixed ren scale ! if .true. use fixed ren scale
With this setting, one still has fR =muR over ref. On the other hand, the input
muR ref fixed is ignored, and the reference scale is defined as follows:

## PDF page 122

1. Decide whether to use fixed (fixed * scale=T) or dynamical (fixed * scale=F)
scales. This is done at runtime, either by editing run card.dat before executing the
launch command, or directly at the prompt after having executed it.
2a. If fixed scales are chosen: the relevant input parameters are * over ref (these are
the f∗ factors in eq. (B.5)) and * ref fixed (these are the reference scales µ∗0 in
eq. (B.5)). Both can be set at runtime in the same way as fixed * scale.
2b. If dynamical scales are chosen: the relevant quantities are the input parameters
* over ref as in case 2a., and the functions responsible for defining the reference
scales, to be found in setscales.f. Modifications to the latter file must be carried
out before executing the launch command (i.e., no modifications are possible at
runtime); by default, the reference dynamical scales are set equal to HT /2.
Note that the situation of FxFx-merged simulations is somewhat different, owing to the
specific prescriptions for the settings of the scales which are inherent to the method; for
more details, the user is encouraged to check http://amcatnlo.cern.ch/FxFx merging.htm.
B.3

Scale and PDF uncertainties: the NLO case

Among all the dependencies of a cross section, those due to hard scales and PDFs are
special, since it is always possible to write
σ=

∑

w i bi ,

(B.7)

i

where the coefficients wi (typically called “weights”) are independent of both scales and
PDFs, while the “basis” members bi contain all the information on scales and PDFs in
simple forms such as:
{
µR
µF }
(i) (i)
bi = fH1 fH2 αSki 1, log
.
(B.8)
, log
QES
QES

– 120 –

JHEP07(2014)079

muF2, which are respectively relevant to the hadron coming from the left and the right.
At the LO, this is unambiguous — the scales only enter the relevant PDFs. At the NLO,
however, there are several ways to write the logarithmic terms whose arguments are ratios
of scales. In order to avoid complications, at the NLO the two factorisation scales must
always be chosen to be equal; when this is not the case, the code stops.
We point out that the structure outlined above will allow the user to choose one scale
to be fixed and another one to be dynamical; however, in the vast majority of cases one will
want the scales to be either all fixed (not necessarily to the same value), or all dynamical.
In the latter case, the functions in setscales.f are such that different functional forms
can be adopted for different scales. Again, this is a somehow infrequent situation. Having
this in mind, the default version of setscales.f sets all * ref dynamic functions (with
*=muR, muF, and QES) equal to the same function scale global reference, and one can
limit oneself to modifying the latter for a standard usage.
We conclude this section by summarising schematically what has been described above.

## PDF page 123

(fR↓ , fF↓ ) ,
↓

(fRc , fF↓ ) ,

↑

c

(fR , fF ) ,
(fR↓ , fF↑ ) ,

(fR↑ , fF↓ ) ,

(fRc , fF↑ ) ,

c

(B.9)

(fR , fF ) ,

(B.10)

(fR↑ , fF↑ ) ,

(B.11)

these being the pre-factors introduced in eq. (B.5) to define the renormalisation and fac62

The dependence on PDFs of the (parton-shower) Sudakovs cannot be accounted for by eq. (B.7).
However, this is expected to be rather small, and particularly so when computing PDF uncertainties. See
ref. [125] for more details.

– 121 –

JHEP07(2014)079

The key point is that, while the weights might be very expensive to compute CPU-wise,
the basis members are straightforward. A convenient strategy is therefore that of first
evaluating the wi ’s, and then of using them in eq. (B.7) for all the desired choices of scales
and PDFs; each of these will therefore result in a basically instantaneous evaluation of the
corresponding σ. In practice, what is done in MadGraph5 aMC@NLO is to compute σ for
a given choice of scales and PDFs (the “central” or “default” choice), while at the same time
storing the values of the wi ’s (if this is required by the user in input — see later), in order
to re-use them at a later stage, typically for the assessment of the theoretical uncertainties.
We stress that eq. (B.7) is exact,62 and therefore so is the computation of a cross section
starting from the weights for any given scale and PDF choice. A complete discussion, which
includes all the relevant definitions of wi and bi for both fixed-order and MC@NLO cross
sections, is given in ref. [125] and will not be repeated here. The aim of this appendix is
rather that of giving some details on the way in which eq. (B.7) is exploited when computing
scale and PDF uncertainties in the context of (N)LO+PS and f(N)LO simulations.
The basic idea relevant to (N)LO+PS is the following. In the LHE file and event-byevent, the values of σ will be stored that correspond to all the combinations of scales and
PDFs selected by the user in input (we denote the numbers of these combinations by Nµ
and NPDF respectively). These σ’s will have to be treated in the same way as the cross
section associated with the central scales and PDFs (which is part of the standard LHE
information, and corresponds to the variable XWGTUP); namely, each of them will constitute
an entry in a histogram associated with that particular combination of scales and PDFs. In
other words, for each observable of interest, one will have to fill 1 + Nµ + NPDF histograms
(the “1” being for the central choices). At the end of the run, and for each observable, the
envelope of the 1 + Nµ histograms will give the scale uncertainty affecting that observable,
and the envelope of the 1 + NPDF histograms will be the PDF uncertainty. The precise
definition of these two envelopes is the user’s responsibility. In the case of the scales, one
will typically want to consider the largest and smallest cross sections bin-by-bin, possibly
excluding from the computation of such extremes some of the (µR , µF ) combinations (see
e.g. [367] for a discussion on this point). In the case of the PDFs, the envelope must be
defined following the prescription of the PDF authors.
We now show how the user can choose in input the scales and PDFs that will be used
in the calculation of the uncertainties; we start from the former. In the present version
of MadGraph5 aMC@NLO we have fixed Nµ = 8, which corresponds to the following
combinations:

## PDF page 124

torisation scales given the reference scales:
(
)
) (
µαR , µβF = fRα µR0 , fFβ µF 0 ,

{α, β} ∈ {↓, c, ↑} .

(B.12)

fR↓ = muR over ref × rw Rscale down ,

(B.13)

c

(B.14)

↑

(B.15)

↓

(B.16)

c

(B.17)

↑

(B.18)

fR = muR over ref ,

fR = muR over ref × rw Rscale up ,

fF = muF over ref × rw Fscale down ,
fF = muF over ref ,

fF = muF over ref × rw Fscale up .

Given these inputs, MadGraph5 aMC@NLO will consider all the combinations given in
eqs. (B.9)–(B.11), compute the corresponding bi ’s of eq. (B.8) using the central PDFs, and
combine them with the weights according to eq. (B.7). The resulting σ (which could be
denoted by σ (α,β) for consistency with eq. (B.12)) will be stored in the LHE file, provided
the user sets:
.true. = reweight scale ! reweight to get scale dependence
in input.
As far as PDF uncertainties are concerned, we have assumed that one will use
LHAPDF, where all members of an error set are identified by adjacent integer numbers.
Using NNPDF 2.0 [368] as an example to be definite, one will have the following inputs:
lhapdf = pdlabel ! PDF set
90800 = lhaid ! if pdlabel=lhapdf, this is the lhapdf number
90801 = PDF set min ! First of the error PDF sets
90900 = PDF set max ! Last of the error PDF sets
The first two lines instruct the code to use LHAPDF and to choose the central NNPDF
2.0 set as the default. The last two lines will set NPDF = 100; for each of these hundred
NNPDF 2.0 error sets, MadGraph5 aMC@NLO will compute the bi ’s of eq. (B.8) using
the central scales, and combine them with the weights according to eq. (B.7). The resulting
σ will be stored in the LHE file, provided the user sets:
.true. = reweight PDF ! reweight to get PDF uncertainty
in input.
For what concerns the storage in the LHE file of the σ’s computed as described above,
we use a format which is fully compatible with the LHA v2.0 [95], and which is now officially
adopted as v3.0 [218]. In the file header, there will be a part (which we call the reweight

– 122 –

JHEP07(2014)079

The combination (fRc , fFc ) missing in eqs. (B.9)–(B.11) is obviously that corresponding to
the central scales, which is always computed. Equation (B.12) implies that scale variations
are defined by choosing the reference renormalisation and factorisation scales (which is
done as explained in section B.2), and by varying the pre-factors in front of them. Such
prefactors are defined by means of some input parameters found in run card.dat. More
specifically, we have:

## PDF page 125

– 123 –

JHEP07(2014)079

section) where a description is given of the meaning of the weights that will appear in each
event. Its structure may read as follows:
<initrwgt>
<weight id=’1’> This is the central weight </weight>
<weightgroup type=’scale variation’ combine=’envelope’>
<weight id=’2’> muR=0.5 muF=0.5 </weight>
<weight id=’3’> muR=0.5 muF=1.0 </weight>
...
<weight id=’9’> muR=2.0 muF=2.0 </weight>
</weightgroup>
<weightgroup type=’NNPDF20’ combine=’gaussian’>
<weight id=’10’> set001 </weight>
...
<weight id=’109’> set100 </weight>
</weightgroup>
</initrwgt>
Thus, each choice of scales and of PDFs is uniquely identified by an ID number. For
example, id=’1’ will correspond to the central scale and PDF choices, (fR , fF ) = (fRc , fFc )
and PDF number 90800 in the examples given above (this is the same as XWGTUP, and
hence is redundant, but it is convenient to include it in the reweight section as well). As
far as id=’2’ to id=’9’ are concerned, these will correspond to the Nµ combinations
given in eqs. (B.9)–(B.11), the numerical values reported in the header next to muR and
muF being those of fRα and fFβ respectively. Finally, id=’10’ to id=’109’ correspond to
the NPDF error sets 90801–90900.
In keeping with the reweight section in the LHE file header, there will be a reweight
section event-by-event, which contains the actual numbers to be used to fill the histograms
as described previously. Its structure will read as follows:
<event>
...
<rwgt>
<weight id=’1’> 3.905e+01</wgt>
<weight id=’2’> 4.142e+01</wgt>
...
<weight id=’109’> 3.876e+01</wgt>
</rwgt>
</event>
The presence of the ID numbers in the reweight section of each event facilitates debugging,
does not require the weights to be always in the same order, and is especially convenient
for on-the-fly manipulations (such as discarding some contributions, sorting them, and so
forth).
We conclude this section with some general comments. The condition Nµ = 8 can be
trivially relaxed (which requires the inclusion of Nµ itself in the list of the inputs); we have
refrained from doing so in the first public version of the code since three choices for each

## PDF page 126

1 + (1 + Nµ ) + NPDF

reweight scale = .true.

reweight PDF = .true. (B.19)

1 + (1 + Nµ )

reweight scale = .true.

reweight PDF = .false. (B.20)

1 + NPDF

reweight scale = .false.

reweight PDF = .true. (B.21)

The first entry thus always gives the value of the weight associated with central parameters.
In the case of scale variations, this weight is present twice (the “1” in (1 + Nµ )) essentially
for reasons of backward compatibility which should not concern the user. The information
of which weight is which is returned as the array of strings weights info and made available
to the user’s initialisation routine analysis begin — this is equivalent to the id number
discussed before in the context of LHE files.
B.4

Scale and PDF uncertainties: the LO case

At the LO, the structure of the cross section, eq. (B.7), is trivial — the sum contains one
term i = 1 (see however footnote 8), which corresponds to the single PDF-and-coupling
combination (i.e., to a single basis member, eq. (B.8)) relevant to this perturbative order:
this is the reason for the simplicity of eq. (2.2). Thus here, at variance with the NLO case,
from the user’s viewpoint it is therefore as simple to handle w1 as is to handle σ. This
suggests the following strategy: when unweighted events are produced, they are stored in
an intermediate LHE file with a non-standard format, that features the weights w1 . After
the end of the run, this LHE file is read by a standalone module, dubbed SysCalc, that
converts the weights w1 into the corresponding cross sections σ, and stores them in a new
LHE file, which has this time the standard format already described in appendix B.3. This
procedure is advantageous because it allows one to run SysCalc as many times as desired
using the same intermediate LHE file obtained at generation time; this implies that the
63

This not being the case at the LO, in LO-type generations we can adopt a different strategy — see
appendix B.4.

– 124 –

JHEP07(2014)079

of the hard scales typically give a good estimate of the uncertainties. A more extended set
of input parameters would also give one the possibility of performing scale variations by
changing the functional forms of the reference scales w.r.t. those adopted for the central
results. Finally, the complete generality could be achieved by storing in the LHE file the
weights wi ’s. This would require, however, that additional information be stored as well
(such as the values of the Bjorken x’s — more details can be found in ref. [125]). While
this can be trivially done, it would render the computation of the basis members bi ’s of
eq. (B.8), and their subsequent combination with weights according to eq. (B.7), a much
more involved operation than the present one if performed by an external user.63 Such a
possibility is left open for future developments.
In the case of f(N)LO runs, the information on scale and PDF variations is also available
on an event-by-event basis. In keeping with the fact that here one cannot have unweighted
events, MadGraph5 aMC@NLO will associate to each kinematic configuration an array of
weights (rather than a single weight), each of which gives eq. (B.7) with the basis elements
of eq. (B.8) recomputed for all desired scale and PDF choices. This implies that the second
elements of the pairs in eqs. (3.4)–(3.6) will be turned into arrays, with dimensionality:

## PDF page 127

0.5 1 2 = sys_scalefact # Central scale factors
-1
= sys_scalecorrelation # for renormalization/scale variate
# -1: make all combination
# -2: only correlated variation
0.5 1 2 = sys_alpsfact # \alpha_s emission scale factors
30 50 = sys_matchscale # variation of merging scale
# PDF sets and number of members (0 or none for all members).
CT10nlo.LHgrid = sys_pdf #
The list of values to the left of sys scalefact collects the multiplicative factors in front
of the reference (fixed or dynamic65 ) scales, and are thus analogous to the quantities fRα
and fFβ that appear in eq. (B.12); at variance with the current NLO implementation, such
a list can contain more than three numbers. We stress that, when use syst=T, the value
of scalefact in run card.dat is ignored. The flag sys scalecorrelation allows one to
choose which of the renormalisation/factorisation scale combinations are considered. When
“-1’ is entered, then all µR and µF values determined by the list sys scalefact are taken
into account, while with “-2” one restricts to code to dealing with µR = µF . More sophisticated options are also available (allowing one to select only some of the possible (µR , µF )
combinations), which will be documented elsewhere. The entry sys pdf is associated with
the study of PDF systematics; if set equal to a PDF error set, all PDF members in that set
will be considered. Alternatively, one can specify the individual PDF members to be taken
into account. Finally, through SysCalc one can also investigate the systematics relevant
to tree-level merging (see section 2.3.4), with sys alpsfact and sys matchscale corresponding to αS -argument and Qmatch variations respectively. More details on SysCalc can
be found at: https://cp3.irmp.ucl.ac.be/projects/madgraph/wiki/SysCalc.
B.5

Other LO reweighting applications

In this appendix we comment in the briefest of manners on some technicalities relevant
to the matrix-element reweighting (eq. (2.3)) and the matrix-element method (eq. (2.5))
discussed in section 2.3.3.
64

SysCalc requires that LHAPDF be installed as well.

65

Note that the setscales.f code relevant to LO calculations is different w.r.t that used in NLO ones.

– 125 –

JHEP07(2014)079

type of scale or PDF variations need not be chosen before the event-generation phase, as
is the case at the NLO. The SysCalc module can be installed64 with:
MG5 aMC> install syscalc
from the MadGraph5 aMC@NLO shell. At runtime, MadGraph5 aMC@NLO is instructed to save the weights w1 in the intermediate LHE file by setting
T = use syst ! Enable systematics studies
in run card.dat. When this is done, SysCalc is automatically called at the end of the
run (although, as was said before, it can also be run independently afterwards). The
type of scale and PDF variations considered are determined by the following entries in
run card.dat:

## PDF page 128

B.6

Output formats and standalone libraries

The main purpose of MadGraph5 aMC@NLO is that of providing a self-contained framework where to compute cross sections and generate events at the desired level of perturbative accuracy, in both the SM and new-physics theories. On the other hand, the code may
also be used to provide one with only a given ingredient of a calculation (e.g., a matrix
element) which is to be performed elsewhere. This has been one of the defining characteristic of MadGraph, and has been wholly inherited by MadGraph5 aMC@NLO. Another
example is the computation of a quantity which is not a cross section; a case in point is
the likelihood dealt with by MadWeight (see section 2.3.3 and appendix B.5).
All possible executables, libraries, or more elementary objects that can be produced
by MadGraph5 aMC@NLO can simply be seen as outputs of the (meta-)code; they are in
fact in one-to-one correspondence with the optional first keyword of the shell command:
MG5 aMC> output [OutputForm] [MYPROC]

– 126 –

JHEP07(2014)079

As was already mentioned in section 3.1, the former procedure is straightforwardly
accessed through the MadGraph5 aMC@NLO shell, by simply setting reweight=ON in
the interactive talk-to phase. By doing so, MadGraph5 aMC@NLO will use the file
reweight card.dat to modify the parameters (found in param card.dat) used for the
benchmark computation (that essentially corresponds to the denominator of eq. (2.3)).
One may enter any number of such modifications, each of which may contain any number
of parameter changes, to be done through the set command (see the comments inside
the file reweight card.dat). There are currently two main limitations to this procedure.
Firstly, the changes must occur within one given model (i.e., one cannot reweight to matrix
elements computed in a model different w.r.t. that adopted in the benchmark calculation).
Secondly, the accessible kinematical region in the “new” hypothesis must be equal to or
smaller than the original one. The interested reader can find more information by visiting:
https://cp3.irmp.ucl.ac.be/projects/madgraph/wiki/Reweight.
The matrix-element method is handled by MadWeight. As was discussed in section 3.1, the current version embedded in MadGraph5 aMC@NLO has vastly increased
the speed of the previous version [136]. Such an increase is mainly due to a better combination of subprocesses, to a Monte-Carlo-type sum over jet-parton assigments (as opposed
to an exact sum), and to the possibility of performing the simultaneous computation of
P (q|α) in the case of multiple choices of the transfer function. The MadWeight executable
specific to the process generated by the user simply corresponds to employing one of the
reserved output keywords (see appendix B.6), namely to executing, after the generation
phase, the command:
MG5 aMC> output madweight MYPROC
After that, one may continue with using the MadGraph5 aMC@NLO shell interface by
executing:
MG5 aMC> launch MYPROC
Further details can be found at: https://cp3.irmp.ucl.ac.be/projects/madgraph/wiki/
MadWeight.

## PDF page 129

The possible choices of OutputForm can be readily obtained by using the autocompletion
<TAB> key in the shell after having typed output (or with help output). By doing so,
one will notice that they all apply, bar one case (standalone, see below), to LO-type
generations. Here we shall not list them all, but limit ourselves to commenting on those
which are the most useful from the user’s point of view. These are:

• standalone cpp: the same as above, but in C++ rather than in Fortran77. Works
only for tree-level matrix elements.
• pythia8: self-contained library for the computation of tree-level matrix elements, in
a format which can be directly used in the Pythia8 PSMC. It includes a simple driver
that one can employ to steer Pythia8 sample runs, and a Processes * directory that
contains the said matrix elements. More details can be found in section 3.2 of ref. [38].
• madweight: this output keyword allows one to set up a computation with MadWeight (see appendix B.5).
We conclude this appendix by stressing that the above list (supplemented by that of the
other output keywords not explicitly given here) is by no means all-inclusive. The reader
who is interested in a particular output format specifically suited to his/her need is encouraged to contact us in order for that to be developed and included in future versions of MadGraph5 aMC@NLO. For instance, dedicated outputs for matrix elements to be used in the
MatchBox [181] framework and by EventDeconstruction [369, 370] are being developed.

C

Features of one-loop computations

C.1

TIR and IREGI

The aim of this section is that of presenting the basic procedures used in TIR, and in
particular by the program IREGI;66 more details on the latter will be given elsewhere [168].
IREGI computes the integral that appears as first element in the set of eq. (2.79); owing
to the fact that we apply TIR to a given loop topology (see eq. (2.77)), we can exploit
eq. (2.76) to simplify the notation here and drop the dependence on lt . On the other hand,
at variance with what was done in section 2.4.2, in order to make things more explicit it
is convenient to insert in the notation the dependence on the external (four-dimensional,
owing to the ’t Hooft-Veltman scheme) four-momenta pi and on the masses mi that circulate
in the loop (see eq. (2.60)), so that the integral we are interested in reads as follows:
∫
ℓ µ1 . . . ℓ µr
µ1 ...µr
({pi }, {mi }) = dd ℓ̄ ∏m−1
I
.
(C.1)
i=0 D̄i
66

The acronym stands for “Integral REduction with General positive propagator Indices”.

– 127 –

JHEP07(2014)079

• standalone: self-contained Fortran77 library for the computation of either tree-level
matrix elements (after an LO-type generation), or one-loop matrix elements (after an
NLO-type generation with the keyword virt=coupling1 ... — see appendix B.1).
The directory structure thus created contains a simple program (check sa.f) which
allows one to evaluate the matrix elements pointwise for test purposes.

## PDF page 130

Lorentz-covariance then guarantees that eq. (C.1) can be re-written as follows:
I µ1 ...µr ({pi }, {mi }) =
∑

(C.2)

2j+i0 +i1 +···+im−1 =r

{[g]j [p0 ]i0 · · · [pm−1 ]im−1 }µ1 ...µr Iji0 ...im−1 ({pi }, {mi }) ,

for certain scalar integrals Iji0 ...im−1 , and where the symmetric tensor form
{[g]j [p0 ]i0 . . . [pm−1 ]im−1 }µ1 ...µr is defined in such a way that all non-equivalent permutations
of the Lorentz indices µ1 , . . . µr on j metric tensors g and is external momenta ps contribute
with weight one. For example:
{[g]1 [p0 ]0 [p1 ]2 }µ1 ...µ4 = g µ1 µ2 pµ1 3 pµ1 4 + g µ1 µ3 pµ1 2 pµ1 4 + g µ1 µ4 pµ1 2 pµ1 3 ,
{[g]0 [p0 ]0 [p1 ]4 }µ1 ...µ4 = pµ1 1 pµ1 2 pµ1 3 pµ1 4 ,

{[g]0 [p0 ]1 [p1 ]2 }µ1 µ2 µ3 = pµ0 1 pµ1 2 pµ1 3 + pµ0 2 pµ1 1 pµ1 3 + pµ0 3 pµ1 1 pµ1 2 .

(C.3)

Given eq. (C.2), the computation of the original tensor integral of eq. (C.1) is reduced
to that of the scalar integrals Iji0 ...im−1 . One starts by observing that the latter are
independent of the number of dimensions used in the numerator of eq. (C.1), because
the decomposition of eq. (C.2) would hold, with the formal replacement g → ḡ, if one
had replaced ℓ → ℓ̄ in eq. (C.1). Therefore, since working with the same number of
dimensions in all parts of a computation is algebraically convenient, one determines the
Iji0 ...im−1 directly in d dimensions. This is done by recursively expressing such scalar
integrals in terms of lower-point ones, till only integrals that cannot be further reduced
are obtained — these are just a few and well known: IREGI makes use of those tabulated
in OneLoop [371] and QCDloop [372].
One way of performing such recursive reduction stems from the pioneering work of
Passarino and Veltman [154]: by contracting both sides of eq. (C.1) (in d-dimensions) with
metric tensors and external four-momenta, one relates the Iji0 ...im−1 integrals to lower-rank
tensor or lower-point scalar integrals. This lowering is due to the fact that, when contracting, one obtains the scalar products ℓ̄2 and ℓ̄·pi , which are then re-expressed as follows:
ℓ̄2 = D̄0 + m20 ,
ℓ̄·pi = (D̄i − D̄0 + m2i − m20 )/2 ,

(C.4)
(C.5)

thus either cancelling some of the denominators or simplifying the dependence on ℓ̄ in
the numerator. The procedure is algebraic, and one ends up with a system of equations
where the unknowns are the scalar integrals, and the coefficients known functions of the
kinematic variables. The solution of such a system is non-trivial, owing for example to
the presence of special kinematic configurations; IREGI implements to a large extent the
strategies proposed in ref. [373].
An alternative and independent way for performing the recursive reduction follows the
work of Davydychev [155]. One introduces the generalised loop-tensor and basic-scalar
integrals:
∫
µ1
µr
(µ2 )2−d/2
µ1 ...µr
d ℓ̄ . . . ℓ̄
¯
(d, {νi }, {pi }, {mi }) =
I
ℓ̄
d
(C.6)
∏
m−1 νi ,
(2π)d
i=0 D̄i
– 128 –

JHEP07(2014)079

{[g]2 [p0 ]0 [p1 ]0 }µ1 ...µ4 = g µ1 µ2 g µ3 µ4 + g µ1 µ3 g µ2 µ4 + g µ1 µ4 g µ2 µ3 ,

## PDF page 131

(µ2 )2−d/2
I0 (d, {νi }, {pi }, {mi }) =
(2π)d

∫

1
dd ℓ̄ ∏m−1
i=0

D̄iνi

,

(C.7)

where the scale-dependent prefactor is conventional, and the indices ν0 , ν1 , · · · , νm−1 are
positive integers. By using a Feynman-parameter representation and the d-dimensional
analogue of eq. (C.2):
I¯µ1 ...µr (d, {νi }, {pi }, {mi }) =

i
(4πµ2 )2−d/2
(4π)
∑
×
{[ḡ]j [p0 ]i0 . . . [pm−1 ]im−1 }µ1 ...µr

(C.8)

×(−1)

∑m−1
i=0

νi +r−j Γ(

∑m−1

i=0 νi − d/2 − j)
∏
2j im−1 Γ(νi )

∫ 1 ∏
m−1
0

dyi yiνi +ii −1

i=0


j+d/2−∑m−1
i=0 νi
)
(m−1
m−1
∑
∑
∑
yi m2i
yi yj (pi −pj )2 +
,
yi −1 −
×δ
I0 (d, {νi }, {pi }, {mi }) =

∑m−1

∑m−1
Γ( i=0 νi − d/2)
i
(4πµ2 )2−d/2
(−1) i=0 νi
∏m−1
(4π)
i=0 Γ(νi )
∫ 1 m−1
m−1
∑
∏
yi − 1)
dyi yiνi −1 δ(
×
0

i=0

i=0



one arrives at:

i=0

i<j

i=0

× −

∑
i<j

I¯µ1 ...µr (d, {νi }, {pi }, {mi }) =

yi yj (pi − pj )2 +

∑

2j+i0 +···+im−1 =r

(4πµ2 )r−j
×
(−2)j

m−1
∑
i=0

d/2−∑m−1
i=0 νi

yi m2i 

,

(C.9)

{[ḡ]j [p0 ]i0 · · · [pm−1 ]im−1 }µ1 ···µr

(m−1
)
∏ Γ(νi + ii )
i=0

Γ(νi )

×I0 (d + 2(r − j), {νi + ii }, {pi }, {mi }) .

(C.10)

By using eqs. (C.2) (in d dimensions) and (C.10), one finally obtains the relation:
Iji0 ...im−1 ({pi }, {mi }) =

[

(µ2 )2−d/2
(2π)d

]−1

(4πµ2 )r−j
(−2)j

(m−1
)
∏ Γ(1 + ii )
i=0

Γ(1)

× I0 (d + 2(r − j), {1 + ii }, {pi }, {mi })|d=4−2ǫ .

(C.11)

With eq. (C.9) one is also able to derive relationships among scalar integrals in different
dimensions. For instance, eq. (6) of ref. [155] can be easily obtained:
I0 (d − 2, {νi }, {pi }, {mi }) = −4πµ

2

m−1
∑
s=0

νs I0 (d, {νi + δis }, {pi }, {mi }) ,

– 129 –

(C.12)

JHEP07(2014)079

2j+i0 +...+im−1 =r

## PDF page 132

¯ b̄tt̄
gg → ddb

¯ t̄
uū → ddt

¯ + ZH
ud¯→ ddW

gg → t̃1 t̃⋆1 g

8190

811

8098

437

∆(k0 )

0

4

2

0

# non-zero hel. configs.

128

16

27

8

Generation time

15h

28min

25h

1min 38s

Running time

18.6s (19%)

895ms (72%)

26.4s (32%)

83.6ms (68%)

Output code size

600 Mb

20 Mb

700 Mb

6 Mb

Runtime RAM usage

3.6 Gb

152 Mb

8.3 Gb

81 Mb

Stability

2 · 10−8

1 · 10−7

4 · 10−7

1 · 10−7

# Feynman diagrams
# topologies

54614

10947

187138

3952

where by δis we have denoted the Kronecker symbol. Furthermore, other recursion relations for the scalar integrals I0 (d, {νi }, {pi }, {mi }) can be obtained with the help of
the integration-by-parts method [374, 375], which exploits the fact that integrals are
translation-invariant in dimensional regularization. The practical implementation in IREGI
of the method discussed here follows ref. [375].
IREGI can use either of the two methods presented above for the recursive reduction,
the actual choice being made by the calling code (in our case, MadLoop5). The current
default in MadGraph5 aMC@NLO is the use of Passarino and Veltman; this is straightforward to change, since it is simply controlled by a parameter in an input card. IREGI
has a minimal internal stability control: should e.g. Passarino and Veltman procedure be
flagged unstable, the code will turn to using Davydychev’s. We stress that this by no
means replaces the stability control performed by MadLoop5, described in section 2.4.2.
C.2

Quantitative profile of MadLoop performances

We have already stressed that the results presented in section 4.3 can be used as benchmarks
for the validation of other codes. However, they reveal only one aspect of the performances
of MadLoop5, which we complement in this appendix by reviewing some quantitative
characteristics of the handling of the scattering processes considered before. A summary
of such characteristics is reported in table 15.
The number of topologies is the upper bound of the sum over the index t in eq. (2.77),
and it corresponds to the number of independent loop reductions (i.e., of evaluations of
the Red[ ] operator introduced in eq. (2.58)) for one kinematic configuration. As one can
see from the table, such a number is much smaller than the number of Feynman diagrams,
which emphasises the importance of the optimization induced by eq. (2.76). The quantity
∆(k0 ) is equal to the number of coupling-constant combinations, minus one, at the Born
level, which is larger than zero in the case of a mixed-coupling expansion. See the beginning
of section 2.4, and eqs. (2.17) and (2.22) in particular, for more details. The generation

– 130 –

JHEP07(2014)079

Table 15. Performances of MadLoop5 in the context of the computations presented in section 4.3.
See the text for details.

## PDF page 133

C.3

Computation of the integrand polynomial coefficients

We have discussed in section section 2.4.2 how the use of the loop-integrand representation
of eq. (2.78) increases the speed of OPP-based integral reductions, as well as giving one
the possibility of using TIR methods. This appendix elaborates on the techniques adopted
(r)
in MadLoop5 for the computation of the coefficients Cµ1 ...µr ;h,l . The key fact is that such
( )
independent entries. In
coefficients are fully symmetric tensors of rank r with only 3+r
r
renormalisable theories and in the Feynman gauge the number of loop propagators sets
the maximal rank in ℓµ of that loop-integrand numerator, so that the total number of
coefficients necessary to express the numerator of any loop of a, say, 2 → 6 process, is at
∑ max =8 (3+r)
= 495 which is well within the reach of modern
most Ncoef f (rmax = 8) ≡ rr=0
r
computers. We start by rewriting the analogue of eq. (2.78) for any polynomial P (rmax ) (ℓµ )
of maximal rank rmax with the following shorthand and symbolic notation:
(r

)

P (rmax ) (ℓµ ) = Ck̇ max ℓk̇ ,

(C.13)

where k̇ takes values between 1 and Ncoef f (rmax ), and effectively defines a map between
the sets of Lorentz indices µi and integer numbers. The choice of such a map is arbitrary,
and we use what follows:
(r)

Cµ1 ,··· ,µr ,

µ1 ≤ · · · ≤ µr

→

67

(r

)

Ck̇(µmax,··· ,µ ) ,
1

r

(C.14)

The timing indicated is for a single core of a 2.7 GHz i7 CPU, with the gfortran compiler v4.8.1 without
optimization flags (which have been shown to have a negligible impact).

– 131 –

JHEP07(2014)079

time includes the compilation of the source code. The running time corresponds to the
time taken by the code output by MadLoop5 to compute the one-loop squared matrix
element summed over colours but for a single helicity configuration.67 The percentage in
parenthesis specifies the fraction of the running time spent in the loop reduction which,
we remind the reader, is independent of the number of non-zero helicity configurations
considered. The complementary fraction of the time is spent in the computation of the
(r)
coefficients Cµ1 ...µr ;h,l of eq. (2.79), and scales linearly with the number of helicity combinations. The size of the output code includes external data files (that essentially contain
the colour coefficients Λlb ) loaded by the library which is in itself much lighter. The RAM
measure reported is the runtime peak of residential memory allocated. The figures given
in the last row are the relative accuracies estimated by the MadLoop5 internal stability
tests in the context of double-precision computations that use the kinematic configurations
considered in section 4.3 (however, we stress again that the matrix-element results have
been obtained in quadruple precision); obviously, these pointwise accuracies have only an
indicative value, since the real figure of merit necessitates averaging over a large statistical
sample of independent kinematic configurations.
We conclude this appendix by stressing that the data reported in table 15 can be obtained by the user by using the command check profile in the MadGraph5 aMC@NLO
shell. For example, one would have
MG5 aMC> check profile g g > t t~ z [virt=QCD]
in the case of the virtual corrections to tt̄Z production (i.e., process e.8 of table 6).

## PDF page 134

ℓ
(1)
Wi,0,k˙ ,j
1

δ mi
(4)

(1)

(5)

Vν,1,s˙4 ,m

Vj,1,s˙1 ,k

Wi,3,k˙ ,m
5

p1
(2)

Wi,1,k˙ ,k
2

(3)

Vµ,1,s˙3 ,ν

(4)

wp(4)

Wi,2,k˙ ,ν
4

(3)

Wi,1,k˙ ,µ
3

wn(2)

wσ(3)
(r

)

Figure 19. An example of the MadLoop5 construction of the coefficients Ck̇ max . W denotes the
loop currents and V the vertex polynomials (see the text). The figure depicts an L-cut diagram;
the original box loop is obtained by sewing the two fermion lines at the top.

k̇(µ1 , · · · , µr ) = Ncoef f (r − 1) +

r
∑
i=1

(1 − δ0µi )

(µi + i − 1)!
,
i!(µi − 1)!

(C.15)

where we define Ncoef f (−1) = 0 (relevant to r = 0). To make things more explicit with
one example, eq. (C.13) reads, with rmax = 2:
(2)

(2)

(2)

(2)

(2)

(4)

Ck̇ ℓk̇ ≡ C0 + C1 ℓ0 + C2 ℓ1 + C3 ℓ2 + C4 ℓ3
(2)

(2)

(2)

(2)

(2)

(2)

(2)

(2)

(2)

(2)

+C5 ℓ0 ℓ0 + C6 ℓ0 ℓ1 + C7 ℓ1 ℓ1 + C8 ℓ0 ℓ2 + C9 ℓ1 ℓ2
+C10 ℓ2 ℓ2 + C11 ℓ0 ℓ3 + C12 ℓ1 ℓ3 + C13 ℓ2 ℓ3 + C14 ℓ3 ℓ3 .
(r

)

(C.16)

The computation of the coefficients Ck̇ max with MadLoop5 is entirely numerical and follows the MadGraph procedure for evaluating Feynman diagrams. At tree level, the internal
(n)
currents of a given Feynman diagram are denoted by wj , with the integer n labeling them
and the index j spanning the representation of the particle associated with the current. In
MadLoop5 the loop currents are promoted to more general objects embedding polynomials
(n)
in ℓµ and they are denoted by Wi,r,k̇,j , with the additional index i specifying the choice
of the external current for the first L-cut particle (which is non-physical and whose only
constraint is to reproduce the Lorentz trace when summed over). The index k̇ labels the
coefficients of the polynomial of maximal rank r according to the convention of eq. (C.15).
Figure 19 shows a complete example of the different numerical objects manipulated by
MadLoop5 in order to construct the polynomial coefficients for the integrand of a box loop
diagram . Note that since the currents w(#) attached to the loop are independent of the
loop momentum ℓµ , it is irrelevant to know whether they are external currents or originate
(1)
from larger trees. The starting loop current Wi,0,k˙ ,j is a polynomial of rank 0 since it does
1
not have any loop momentum dependence; its index k˙1 can therefore only take the value
(1)

0. For all loop diagrams, the starting current is always Wi,0,k˙ ,j = δij δk˙1 0 .
1

– 132 –

JHEP07(2014)079

wρ(1)

(2)

Vk,0,s˙2 ,µ

## PDF page 135

(#)

The objects Va,r,ṡ,b are the representations (polynomials of rank r in the loop momentum) of the vertex plus propagator structures, with a and b the incoming and outgoing loop
(1)
current indices respectively. For example, the explicit expression of Vj,1,s˙1 ,k for a massless
quark in figure 19 reads:
(1)

ρ (1) µ
wρ γik (ℓµ + p1µ ) ,
Vj,1,s˙1 ,k ℓs˙1 = ıgs γji
⏞⏞
⏟
⏟ ⏞⏞ ⏟ ⏟
vertex propagator

(C.17)

(1)

(1)

Vj,1,s˙1 ,k = ıgs (w
/ (1) γ (s˙1 −1) )jk

Vj,1,0,k = ıgs (w
/ (1) p/1 )jk ,

for

s˙1 = 1, . . . , 4 . (C.18)

In renormalisable theories, the rank of the vertex polynomials is maximally equal to one
as only one power of the loop momentum can arise from either the propagator or the
vertex itself (but not from both). This constraint in not enforced by MadLoop5, since
it would make it impossible to compute one-loop diagrams in effectives theories (such as
HEFT). The numerical routines for the evaluation of vertex polynomials are generated
automatically by ALOHA for each process, using the UFO model specifications; this is
what renders the optimisation discussed in this appendix applicable to any model.
Each subsequent loop current W (n+1) is obtained from the previous one W (n) and the
vertex polynomial V (n) placed in between via the defining implicit relation:
˙

(n+1)

˙

(n)

(n)

Wi,r +r ,k˙ ,j ℓk1 = (Wi,r ,k˙ ,m ℓk2 )(Vm,r2 ,ṡ,j ℓṡ ).
1

2

1

1

2

(C.19)

The r.h.s. of eq. (C.19) is a multiplication of two polynomials and each coefficient of W (n+1)
is obtained by summing the corresponding terms in the expanded product. This implies
that a symmetrisation of the coefficients is performed after each loop vertex and this step is
crucial in order to limit their proliferation and the resulting computing time. To illustrate
this, eq. (C.19) is rewritten here for the case r1 = r2 = 1 with k˙1 = 9, corresponding to
the term multiplying ℓ1 ℓ2 which can come either from k˙2 = 2, ṡ = 3 or k˙2 = 3, ṡ = 2:
(n+1)

(n)

(n)

(n)

(n)

Wi,2,9,j = Wi,1,2,m Vm,1,3,j + Wi,1,3,m Vm,1,2,j .

(C.20)

Note the implicit summation on the index m which spans the representation of the particle
circulating in the loop just before the vertex V (n) . Eq. (C.19) is then iteratively used to
compute all loop currents, until the second L-cut leg, which includes the last vertex and
the L-cut propagator, is reached. The coefficients Ck̇ of an n-point loop diagram are then
simply obtained by closing the Lorentz trace:
(n+1)

Ck̇ = Wi,r,k̇,i .

(C.21)

In the example of figure 19, this translates into:
(5)
Ck̇ = Wi,3,k̇,m δ mi =

4
∑
i=1

– 133 –

(5)

Wi,3,k̇,i ,

(C.22)

JHEP07(2014)079

where the denominator of the propagator is removed since it is already accounted for in
the integral-reduction procedure. To be more definite, we show here the expression of each
coefficient of the vertex polynomial of eq. (C.17):

## PDF page 136

D

Third-party codes included in MadGraph5 aMC@NLO

The tarball of MadGraph5 aMC@NLO is self-contained, and ready-to-run. This is also
thanks to the fact that several third-party codes are included into it. We list all of them
here: ALOHA [92], CutTools [156], FastJet (core) [376], HELAS [91], HERWIG6 [142],
MINT [171], OneLoop [371], Pythia6 [141], QCDloop [372], RAMBO [377], StdHEP [378],
Vegas [379, 380].
In the case of FastJet, what is included in MadGraph5 aMC@NLO is a stripped
version of that code (visit www.fastjet.fr for more details). For more extended jetreconstruction capabilities, the user might want to install FastJet proper (thus including
all the relevant plugins).
Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited.

References
[1] D.J. Gross and F. Wilczek, Ultraviolet behavior of non-Abelian gauge theories,
Phys. Rev. Lett. 30 (1973) 1343 [INSPIRE].
[2] H.D. Politzer, Reliable perturbative results for strong interactions?,
Phys. Rev. Lett. 30 (1973) 1346 [INSPIRE].
[3] T. Appelquist and H. Georgi, e+ e− annihilation in gauge theories of strong interactions,
Phys. Rev. D 8 (1973) 4000 [INSPIRE].
[4] G.F. Sterman and S. Weinberg, Jets from quantum chromodynamics,
Phys. Rev. Lett. 39 (1977) 1436 [INSPIRE].
[5] A.J. Buras, E.G. Floratos, D.A. Ross and C.T. Sachrajda, Asymptotic freedom beyond the
leading order, Nucl. Phys. B 131 (1977) 308 [INSPIRE].
[6] W.A. Bardeen, A.J. Buras, D.W. Duke and T. Muta, Deep inelastic scattering beyond the
leading order in asymptotically free gauge theories, Phys. Rev. D 18 (1978) 3998 [INSPIRE].

– 134 –

JHEP07(2014)079

with the sum written explicitly for clarity. It is clear that many loop diagrams can share
some of their constituting loop currents; for example the L-cut box diagram of figure 19
can be prolonged to form loops with more propagators. MadLoop5 takes advantage of this
and computes each loop current only once, for the first loop diagram in which it appears.
An algorithm analogous to the one described in ref. [24] is used for choosing the L-cut
location in order to maximise the number of loop currents recycled.
We conclude this appendix by stressing that all of the optimisations inherited from the
integrand representation of eq. (2.78) can be turned off in MadGraph5 aMC@NLO via the
option loop optimized output of the interactive interface and that, when this is done,
the structure of the code output by MadLoop5 is completely different. For this reason
and despite being significantly slower, the non optimized output mode provides a powerful
self-consistency check and is useful for debugging purposes.

## PDF page 137

[7] G. Altarelli, R.K. Ellis and G. Martinelli, Leptoproduction and Drell-Yan processes beyond
the leading approximation in chromodynamics, Nucl. Phys. B 143 (1978) 521 [Erratum
ibid. B 146 (1978) 544] [INSPIRE].
[8] W. Celmaster and R.J. Gonsalves, Fourth order QCD contributions to the e+ e−
annihilation cross-section, Phys. Rev. D 21 (1980) 3112 [INSPIRE].
[9] R.K. Ellis, D.A. Ross and A.E. Terrano, The perturbative calculation of jet structure in
e+ e− annihilation, Nucl. Phys. B 178 (1981) 421 [INSPIRE].

[11] S. Catani and M.H. Seymour, A general algorithm for calculating jet cross-sections in NLO
QCD, Nucl. Phys. B 485 (1997) 291 [Erratum ibid. B 510 (1998) 503] [hep-ph/9605323]
[INSPIRE].
[12] S. Frixione, A general approach to jet cross-sections in QCD, Nucl. Phys. B 507 (1997) 295
[hep-ph/9706545] [INSPIRE].
[13] D.A. Kosower, Antenna factorization of gauge theory amplitudes,
Phys. Rev. D 57 (1998) 5410 [hep-ph/9710213] [INSPIRE].
[14] J.M. Campbell, M.A. Cullen and E.W.N. Glover, Four jet event shapes in electron-positron
annihilation, Eur. Phys. J. C 9 (1999) 245 [hep-ph/9809429] [INSPIRE].
[15] Z. Bern, L.J. Dixon, D.C. Dunbar and D.A. Kosower, One loop n-point gauge theory
amplitudes, unitarity and collinear limits, Nucl. Phys. B 425 (1994) 217 [hep-ph/9403226]
[INSPIRE].
[16] F. del Aguila and R. Pittau, Recursive numerical calculus of one-loop tensor integrals,
JHEP 07 (2004) 017 [hep-ph/0404120] [INSPIRE].
[17] Z. Bern, L.J. Dixon and D.A. Kosower, Bootstrapping multi-parton loop amplitudes in
QCD, Phys. Rev. D 73 (2006) 065013 [hep-ph/0507005] [INSPIRE].
[18] G. Ossola, C.G. Papadopoulos and R. Pittau, Reducing full one-loop amplitudes to scalar
integrals at the integrand level, Nucl. Phys. B 763 (2007) 147 [hep-ph/0609007] [INSPIRE].
[19] C. Anastasiou, R. Britto, B. Feng, Z. Kunszt and P. Mastrolia, D-dimensional unitarity cut
method, Phys. Lett. B 645 (2007) 213 [hep-ph/0609191] [INSPIRE].
[20] C. Anastasiou, R. Britto, B. Feng, Z. Kunszt and P. Mastrolia, Unitarity cuts and reduction
to master integrals in d dimensions for one-loop amplitudes, JHEP 03 (2007) 111
[hep-ph/0612277] [INSPIRE].
[21] R.K. Ellis, W.T. Giele and Z. Kunszt, A numerical unitarity formalism for evaluating
one-loop amplitudes, JHEP 03 (2008) 003 [arXiv:0708.2398] [INSPIRE].
[22] R.K. Ellis, W.T. Giele, Z. Kunszt and K. Melnikov, Masses, fermions and generalized
D-dimensional unitarity, Nucl. Phys. B 822 (2009) 270 [arXiv:0806.3467] [INSPIRE].
[23] W.T. Giele, Z. Kunszt and K. Melnikov, Full one-loop amplitudes from tree amplitudes,
JHEP 04 (2008) 049 [arXiv:0801.2237] [INSPIRE].
[24] F. Cascioli, P. Maierhofer and S. Pozzorini, Scattering amplitudes with open loops,
Phys. Rev. Lett. 108 (2012) 111601 [arXiv:1111.5206] [INSPIRE].

– 135 –

JHEP07(2014)079

[10] S. Frixione, Z. Kunszt and A. Signer, Three jet cross-sections to next-to-leading order,
Nucl. Phys. B 467 (1996) 399 [hep-ph/9512328] [INSPIRE].

## PDF page 138

[25] P. Mastrolia, E. Mirabella and T. Peraro, Integrand reduction of one-loop scattering
amplitudes through Laurent series expansion, JHEP 06 (2012) 095 [Erratum ibid. 11 (2012)
128] [arXiv:1203.0291] [INSPIRE].
[26] S. Frixione and B.R. Webber, Matching NLO QCD computations and parton shower
simulations, JHEP 06 (2002) 029 [hep-ph/0204244] [INSPIRE].
[27] P. Nason, A new method for combining NLO QCD with shower Monte Carlo algorithms,
JHEP 11 (2004) 040 [hep-ph/0409146] [INSPIRE].

[29] Y.-J. Chen, J. Collins and X.-M. Zu, NLO corrections in MC event generator for angular
distribution of Drell-Yan lepton pair production, JHEP 04 (2002) 041 [hep-ph/0110257]
[INSPIRE].
[30] Y. Kurihara et al., QCD event generators with next-to-leading order matrix elements and
parton showers, Nucl. Phys. B 654 (2003) 301 [hep-ph/0212216] [INSPIRE].
[31] Z. Nagy and D.E. Soper, Matching parton showers to NLO computations,
JHEP 10 (2005) 024 [hep-ph/0503053] [INSPIRE].
[32] C.W. Bauer and M.D. Schwartz, Event generation from effective field theory,
Phys. Rev. D 76 (2007) 074004 [hep-ph/0607296] [INSPIRE].
[33] Z. Nagy and D.E. Soper, Parton showers with quantum interference, JHEP 09 (2007) 114
[arXiv:0706.0017] [INSPIRE].
[34] W.T. Giele, D.A. Kosower and P.Z. Skands, A simple shower and matching algorithm,
Phys. Rev. D 78 (2008) 014026 [arXiv:0707.3652] [INSPIRE].
[35] C.W. Bauer, F.J. Tackmann and J. Thaler, GenEvA. I. A new framework for event
generation, JHEP 12 (2008) 010 [arXiv:0801.4026] [INSPIRE].
[36] S. Hoeche, F. Krauss, M. Schonherr and F. Siegert, A critical appraisal of NLO+PS
matching methods, JHEP 09 (2012) 049 [arXiv:1111.1220] [INSPIRE].
[37] K. Hamilton, P. Nason, E. Re and G. Zanderighi, NNLOPS simulation of Higgs boson
production, JHEP 10 (2013) 222 [arXiv:1309.0017] [INSPIRE].
[38] J. Alwall, M. Herquet, F. Maltoni, O. Mattelaer and T. Stelzer, MadGraph 5: going beyond,
JHEP 06 (2011) 128 [arXiv:1106.0522] [INSPIRE].
[39] T. Stelzer and W.F. Long, Automatic generation of tree level helicity amplitudes,
Comput. Phys. Commun. 81 (1994) 357 [hep-ph/9401258] [INSPIRE].
[40] F. Caravaglios and M. Moretti, An algorithm to compute Born scattering amplitudes
without Feynman graphs, Phys. Lett. B 358 (1995) 332 [hep-ph/9507237] [INSPIRE].
[41] F. Yuasa et al., Automatic computation of cross-sections in HEP: status of GRACE system,
Prog. Theor. Phys. Suppl. 138 (2000) 18 [hep-ph/0007053] [INSPIRE].
[42] A. Kanaki and C.G. Papadopoulos, HELAC: a package to compute electroweak helicity
amplitudes, Comput. Phys. Commun. 132 (2000) 306 [hep-ph/0002082] [INSPIRE].
[43] M. Moretti, T. Ohl and J. Reuter, O’Mega: an optimizing matrix element generator,
hep-ph/0102195 [INSPIRE].

– 136 –

JHEP07(2014)079

[28] M. Dobbs, Incorporating next-to-leading order matrix elements for hadronic diboson
production in showering event generators, Phys. Rev. D 64 (2001) 034016
[hep-ph/0103174] [INSPIRE].

## PDF page 139

[44] F. Krauss, R. Kuhn and G. Soff, AMEGIC++ 1.0: a matrix element generator in C++,
JHEP 02 (2002) 044 [hep-ph/0109036] [INSPIRE].
[45] M.L. Mangano, M. Moretti, F. Piccinini, R. Pittau and A.D. Polosa, ALPGEN, a generator
for hard multiparton processes in hadronic collisions, JHEP 07 (2003) 001
[hep-ph/0206293] [INSPIRE].
[46] J. Fujimoto et al., GRACE/SUSY automatic generation of tree amplitudes in the minimal
supersymmetric standard model, Comput. Phys. Commun. 153 (2003) 106
[hep-ph/0208036] [INSPIRE].

[48] S. Tsuno, T. Kaneko, Y. Kurihara, S. Odaka and K. Kato, GR@PPA 2.7 event generator
for pp/pp̄ collisions, Comput. Phys. Commun. 175 (2006) 665 [hep-ph/0602213] [INSPIRE].
[49] A. Cafarella, C.G. Papadopoulos and M. Worek, Helac-Phegas: a generator for all parton
level processes, Comput. Phys. Commun. 180 (2009) 1941 [arXiv:0710.2427] [INSPIRE].
[50] W. Kilian, T. Ohl and J. Reuter, WHIZARD: simulating multi-particle processes at LHC
and ILC, Eur. Phys. J. C 71 (2011) 1742 [arXiv:0708.4233] [INSPIRE].
[51] J. Alwall et al., MadGraph/MadEvent v4: the new web generation, JHEP 09 (2007) 028
[arXiv:0706.2334] [INSPIRE].
[52] T. Gleisberg and S. Hoeche, Comix, a new matrix element generator, JHEP 12 (2008) 039
[arXiv:0808.3674] [INSPIRE].
[53] A. Belyaev, N.D. Christensen and A. Pukhov, CalcHEP 3.4 for collider physics within and
beyond the standard model, Comput. Phys. Commun. 184 (2013) 1729 [arXiv:1207.6082]
[INSPIRE].
[54] T. Hahn and M. Pérez-Victoria, Automatized one loop calculations in four-dimensions and
D-dimensions, Comput. Phys. Commun. 118 (1999) 153 [hep-ph/9807565] [INSPIRE].
[55] T. Hahn, Generating Feynman diagrams and amplitudes with FeynArts 3,
Comput. Phys. Commun. 140 (2001) 418 [hep-ph/0012260] [INSPIRE].
[56] T. Gleisberg and F. Krauss, Automating dipole subtraction for QCD NLO calculations,
Eur. Phys. J. C 53 (2008) 501 [arXiv:0709.2881] [INSPIRE].
[57] C.F. Berger et al., An automated implementation of on-shell methods for one-loop
amplitudes, Phys. Rev. D 78 (2008) 036003 [arXiv:0803.4180] [INSPIRE].
[58] R. Frederix, T. Gehrmann and N. Greiner, Automation of the dipole subtraction method in
MadGraph/MadEvent, JHEP 09 (2008) 122 [arXiv:0808.2128] [INSPIRE].
[59] W.T. Giele and G. Zanderighi, On the numerical evaluation of one-loop amplitudes: the
gluonic case, JHEP 06 (2008) 038 [arXiv:0805.2152] [INSPIRE].
[60] M. Czakon, C.G. Papadopoulos and M. Worek, Polarizing the dipoles, JHEP 08 (2009) 085
[arXiv:0905.0883] [INSPIRE].
[61] R. Frederix, S. Frixione, F. Maltoni and T. Stelzer, Automation of next-to-leading order
computations in QCD: the FKS subtraction, JHEP 10 (2009) 003 [arXiv:0908.4272]
[INSPIRE].

– 137 –

JHEP07(2014)079

[47] CompHEP collaboration, E. Boos et al., CompHEP 4.4: automatic computations from
Lagrangians to events, Nucl. Instrum. Meth. A 534 (2004) 250 [hep-ph/0403113]
[INSPIRE].

## PDF page 140

[62] K. Hasegawa, S. Moch and P. Uwer, AutoDipole: automated generation of dipole subtraction
terms, Comput. Phys. Commun. 181 (2010) 1802 [arXiv:0911.4371] [INSPIRE].
[63] S. Hoche, F. Krauss, M. Schonherr and F. Siegert, Automating the POWHEG method in
Sherpa, JHEP 04 (2011) 024 [arXiv:1008.5399] [INSPIRE].
[64] S. Alioli, P. Nason, C. Oleari and E. Re, A general framework for implementing NLO
calculations in shower Monte Carlo programs: the POWHEG BOX, JHEP 06 (2010) 043
[arXiv:1002.2581] [INSPIRE].

[66] R. Frederix, T. Gehrmann and N. Greiner, Integrated dipoles with MadDipole in the
MadGraph framework, JHEP 06 (2010) 086 [arXiv:1004.2905] [INSPIRE].
[67] S. Becker, C. Reuschle and S. Weinzierl, Numerical NLO QCD calculations,
JHEP 12 (2010) 013 [arXiv:1010.4187] [INSPIRE].
[68] V. Hirschi et al., Automation of one-loop QCD corrections, JHEP 05 (2011) 044
[arXiv:1103.0621] [INSPIRE].
[69] G. Bevilacqua et al., HELAC-NLO, Comput. Phys. Commun. 184 (2013) 986
[arXiv:1110.1499] [INSPIRE].
[70] S. Becker, D. Goetz, C. Reuschle, C. Schwan and S. Weinzierl, NLO results for five, six and
seven jets in electron-positron annihilation, Phys. Rev. Lett. 108 (2012) 032005
[arXiv:1111.1733] [INSPIRE].
[71] G. Cullen et al., Automated one-loop calculations with GoSam,
Eur. Phys. J. C 72 (2012) 1889 [arXiv:1111.2034] [INSPIRE].
[72] T. Binoth et al., Automized squark-neutralino production to next-to-leading order,
Phys. Rev. D 84 (2011) 075005 [arXiv:1108.1250] [INSPIRE].
[73] S. Agrawal, T. Hahn and E. Mirabella, FormCalc 7, J. Phys. Conf. Ser. 368 (2012) 012054
[arXiv:1112.0124] [INSPIRE].
[74] Z. Bern et al., Four-jet production at the Large Hadron Collider at next-to-leading order in
QCD, Phys. Rev. Lett. 109 (2012) 042001 [arXiv:1112.3940] [INSPIRE].
[75] S. Actis, A. Denner, L. Hofer, A. Scharf and S. Uccirati, Recursive generation of one-loop
amplitudes in the standard model, JHEP 04 (2013) 037 [arXiv:1211.6316] [INSPIRE].
[76] S. Badger, B. Biedermann, P. Uwer and V. Yundin, Numerical evaluation of virtual
corrections to multi-jet production in massless QCD,
Comput. Phys. Commun. 184 (2013) 1981 [arXiv:1209.0100] [INSPIRE].
[77] D. Goncalves-Netto, D. Lopez-Val, K. Mawatari, T. Plehn and I. Wigmore, Automated
squark and gluino production to next-to-leading order, Phys. Rev. D 87 (2013) 014002
[arXiv:1211.0286] [INSPIRE].
[78] S. Badger, B. Biedermann, P. Uwer and V. Yundin, Computation of multi-leg amplitudes
with NJet, J. Phys. Conf. Ser. 523 (2014) 012057 [arXiv:1312.7140] [INSPIRE].
[79] Z. Bern et al., The BlackHat library for one-loop amplitudes,
J. Phys. Conf. Ser. 523 (2014) 012051 [arXiv:1310.2808] [INSPIRE].

– 138 –

JHEP07(2014)079

[65] P. Mastrolia, G. Ossola, T. Reiter and F. Tramontano, Scattering amplitudes from
unitarity-based reduction algorithm at the integrand-level, JHEP 08 (2010) 080
[arXiv:1006.0710] [INSPIRE].

## PDF page 141

[80] G. Cullen et al., GoSam-2.0: a tool for automated one-loop calculations within the standard
model and beyond, arXiv:1404.7096 [INSPIRE].
[81] H. van Deurzen et al., Multi-leg one-loop massive amplitudes from integrand reduction via
Laurent expansion, JHEP 03 (2014) 115 [arXiv:1312.6678] [INSPIRE].
[82] T. Peraro, Ninja: automated integrand reduction via Laurent expansion for one-loop
amplitudes, arXiv:1403.1229 [INSPIRE].
[83] E. Byckling and K. Kajantie, Particle kinematics, Wiley, U.S.A. (1971).

[85] N.D. Christensen et al., A comprehensive approach to new physics simulations,
Eur. Phys. J. C 71 (2011) 1541 [arXiv:0906.2474] [INSPIRE].
[86] N.D. Christensen, C. Duhr, B. Fuks, J. Reuter and C. Speckner, Introducing an interface
between WHIZARD and FeynRules, Eur. Phys. J. C 72 (2012) 1990 [arXiv:1010.3251]
[INSPIRE].
[87] C. Duhr and B. Fuks, A superspace module for the FeynRules package,
Comput. Phys. Commun. 182 (2011) 2404 [arXiv:1102.4191] [INSPIRE].
[88] A. Alloul, N.D. Christensen, C. Degrande, C. Duhr and B. Fuks, FeynRules 2.0 — a
complete toolbox for tree-level phenomenology, Comput. Phys. Commun. 185 (2014) 2250
[arXiv:1310.1921] [INSPIRE].
[89] A. Alloul, J. D’Hondt, K. De Causmaecker, B. Fuks and M. Rausch de Traubenberg,
Automated mass spectrum generation for new physics, Eur. Phys. J. C 73 (2013) 2325
[arXiv:1301.5932] [INSPIRE].
[90] C. Degrande, Automated computation of the R2 rational terms and ultraviolet counterterms
by NLOCT: an illustration on the 2HDM, in preparation.
[91] H. Murayama, I. Watanabe and K. Hagiwara, HELAS: helicity amplitude subroutines for
Feynman diagram evaluations, KEK-91-11, Japan (1992) [INSPIRE].
[92] P. de Aquino, W. Link, F. Maltoni, O. Mattelaer and T. Stelzer, ALOHA: automatic
libraries of helicity amplitudes for Feynman diagram computations,
Comput. Phys. Commun. 183 (2012) 2254 [arXiv:1108.2041] [INSPIRE].
[93] C. Degrande et al., UFO — the Universal FeynRules Output,
Comput. Phys. Commun. 183 (2012) 1201 [arXiv:1108.2040] [INSPIRE].
[94] J. Alwall et al., A standard format for Les Houches event files,
Comput. Phys. Commun. 176 (2007) 300 [hep-ph/0609017] [INSPIRE].
[95] J.M. Butterworth et al., The tools and Monte Carlo working group summary report,
arXiv:1003.1643 [INSPIRE].
[96] E.N. Argyres et al., Stable calculations for unstable particles: restoring gauge invariance,
Phys. Lett. B 358 (1995) 339 [hep-ph/9507216] [INSPIRE].
[97] W. Beenakker et al., The Fermion loop scheme for finite width effects in e+ e− annihilation
into four fermions, Nucl. Phys. B 500 (1997) 255 [hep-ph/9612260] [INSPIRE].
[98] G. Passarino, Unstable particles and nonconserved currents: a generalization of the fermion
loop scheme, Nucl. Phys. B 574 (2000) 451 [hep-ph/9911482] [INSPIRE].

– 139 –

JHEP07(2014)079

[84] N.D. Christensen and C. Duhr, FeynRules — Feynman rules made easy,
Comput. Phys. Commun. 180 (2009) 1614 [arXiv:0806.4194] [INSPIRE].

## PDF page 142

[99] W. Beenakker, F.A. Berends and A.P. Chapovsky, An effective Lagrangian approach for
unstable particles, Nucl. Phys. B 573 (2000) 503 [hep-ph/9909472] [INSPIRE].
[100] W. Beenakker, A.P. Chapovsky, A. Kanaki, C.G. Papadopoulos and R. Pittau, Towards an
effective Lagrangian approach to fermion loop corrections, Nucl. Phys. B 667 (2003) 359
[hep-ph/0303105] [INSPIRE].
[101] M. Beneke, A.P. Chapovsky, A. Signer and G. Zanderighi, Effective theory approach to
unstable particle production, Phys. Rev. Lett. 93 (2004) 011602 [hep-ph/0312331]
[INSPIRE].

[103] A. Denner, S. Dittmaier, M. Roth and L.H. Wieders, Electroweak corrections to
charged-current e+ e− → 4 fermion processes: technical details and further results,
Nucl. Phys. B 724 (2005) 247 [Erratum ibid. B 854 (2012) 504] [hep-ph/0505042]
[INSPIRE].
[104] F. Staub, SARAH 3.2: Dirac gauginos, UFO output and more,
Comput. Phys. Commun. 184 (2013) 1792 [arXiv:1207.0906] [INSPIRE].
[105] N.D. Christensen et al., Simulating spin- 32 particles at colliders,
Eur. Phys. J. C 73 (2013) 2580 [arXiv:1308.1668] [INSPIRE].
[106] J. Alwall et al., Computing decay rates for new physics theories with FeynRules and
MadGraph5/aMC@NLO, arXiv:1402.1178 [INSPIRE].
[107] F.A. Berends, R. Kleiss, P. De Causmaecker, R. Gastmans and T.T. Wu, Single
Bremsstrahlung processes in gauge theories, Phys. Lett. B 103 (1981) 124 [INSPIRE].
[108] P. De Causmaecker, R. Gastmans, W. Troost and T.T. Wu, Multiple Bremsstrahlung in
gauge theories at high-energies. 1. General formalism for quantum electrodynamics,
Nucl. Phys. B 206 (1982) 53 [INSPIRE].
[109] R. Kleiss and W.J. Stirling, Spinor techniques for calculating pp̄ → W ± /Z 0 + jets,
Nucl. Phys. B 262 (1985) 235 [INSPIRE].
[110] R. Gastmans and T. Wu, The ubiquitous photon: helicity method for QED and QCD, Int.
Ser. Monogr. Phys. 80 (1990) 1 [INSPIRE].
[111] Z. Xu, D.-H. Zhang and L. Chang, Helicity amplitudes for multiple Bremsstrahlung in
massless non-Abelian gauge theories, Nucl. Phys. B 291 (1987) 392 [INSPIRE].
[112] J.F. Gunion and Z. Kunszt, Improved analytic techniques for tree graph calculations and the
Ggq q̄ lepton anti-lepton subprocess, Phys. Lett. B 161 (1985) 333 [INSPIRE].
[113] K. Hagiwara and D. Zeppenfeld, Helicity amplitudes for heavy lepton production in e+ e−
annihilation, Nucl. Phys. B 274 (1986) 1 [INSPIRE].
[114] M.L. Mangano and S.J. Parke, Multiparton amplitudes in gauge theories,
Phys. Rept. 200 (1991) 301 [hep-th/0509223] [INSPIRE].
[115] V. Del Duca, L.J. Dixon and F. Maltoni, New color decompositions for gauge amplitudes at
tree and loop level, Nucl. Phys. B 571 (2000) 51 [hep-ph/9910563] [INSPIRE].
[116] F. Maltoni, K. Paul, T. Stelzer and S. Willenbrock, Color flow decomposition of QCD
amplitudes, Phys. Rev. D 67 (2003) 014026 [hep-ph/0209271] [INSPIRE].

– 140 –

JHEP07(2014)079

[102] A. Denner, S. Dittmaier, M. Roth and D. Wackeroth, Predictions for all processes
e+ e− → 4 fermions + γ, Nucl. Phys. B 560 (1999) 33 [hep-ph/9904472] [INSPIRE].

## PDF page 143

[117] C. Duhr, S. Hoeche and F. Maltoni, Color-dressed recursive relations for multi-parton
amplitudes, JHEP 08 (2006) 062 [hep-ph/0607057] [INSPIRE].
[118] K. Hagiwara, J. Kanzaki, Q. Li and K. Mawatari, HELAS and MadGraph/MadEvent with
spin-2 particles, Eur. Phys. J. C 56 (2008) 435 [arXiv:0805.2554] [INSPIRE].
[119] K. Hagiwara, J. Kanzaki, N. Okamura, D. Rainwater and T. Stelzer, Fast calculation of
HELAS amplitudes using graphics processing unit (GPU), Eur. Phys. J. C 66 (2010) 477
[arXiv:0908.4403] [INSPIRE].

[121] M. Bahr et al., HERWIG++ physics and manual, Eur. Phys. J. C 58 (2008) 639
[arXiv:0803.0883] [INSPIRE].
[122] J. Bellm et al., HERWIG++ 2.7 release note, arXiv:1310.6877 [INSPIRE].
[123] T. Sjöstrand, S. Mrenna and P.Z. Skands, A brief introduction to PYTHIA 8.1,
Comput. Phys. Commun. 178 (2008) 852 [arXiv:0710.3820] [INSPIRE].
[124] N. Arkani-Hamed, S. Dimopoulos and G.R. Dvali, The hierarchy problem and new
dimensions at a millimeter, Phys. Lett. B 429 (1998) 263 [hep-ph/9803315] [INSPIRE].
[125] R. Frederix et al., Four-lepton production at hadron colliders: aMC@NLO predictions with
theoretical uncertainties, JHEP 02 (2012) 099 [arXiv:1110.4738] [INSPIRE].
[126] J. Alwall, Q. Li and F. Maltoni, Matched predictions for Higgs production via heavy-quark
loops in the SM and beyond, Phys. Rev. D 85 (2012) 014031 [arXiv:1110.1728] [INSPIRE].
[127] R. Frederix et al., Higgs pair production at the LHC with NLO and parton-shower effects,
Phys. Lett. B 732 (2014) 142 [arXiv:1401.7340] [INSPIRE].
[128] K. Kondo, Dynamical likelihood method for reconstruction of events with missing
momentum. 1: method and toy models, J. Phys. Soc. Jap. 57 (1988) 4126 [INSPIRE].
[129] R.H. Dalitz and G.R. Goldstein, The decay and polarization properties of the top quark,
Phys. Rev. D 45 (1992) 1531 [INSPIRE].
[130] K. Kondo, Dynamical likelihood method and top quark mass measurement at CDF,
J. Phys. Conf. Ser. 53 (2006) 202 [INSPIRE].
[131] Y. Gao et al., Spin determination of single-produced resonances at hadron colliders,
Phys. Rev. D 81 (2010) 075022 [arXiv:1001.3396] [INSPIRE].
[132] P. Avery et al., Precision studies of the Higgs boson decay channel H → ZZ → 4ℓ with
MEKD, Phys. Rev. D 87 (2013) 055006 [arXiv:1210.0896] [INSPIRE].
[133] J.M. Campbell, W.T. Giele and C. Williams, The matrix element method at next-to-leading
order, JHEP 11 (2012) 043 [arXiv:1204.4424] [INSPIRE].
[134] J.S. Gainer, J. Lykken, K.T. Matchev, S. Mrenna and M. Park, Geolocating the Higgs boson
candidate at the LHC, Phys. Rev. Lett. 111 (2013) 041801 [arXiv:1304.4936] [INSPIRE].
[135] T. Plehn, P. Schichtel and D. Wiegand, MadMax, or where boosted significances come from,
arXiv:1311.2591 [INSPIRE].
[136] P. Artoisenet, V. Lemaitre, F. Maltoni and O. Mattelaer, Automation of the matrix element
reweighting method, JHEP 12 (2010) 068 [arXiv:1007.3300] [INSPIRE].

– 141 –

JHEP07(2014)079

[120] K. Hagiwara, J. Kanzaki, N. Okamura, D. Rainwater and T. Stelzer, Calculation of HELAS
amplitudes for QCD processes using graphics processing unit (GPU),
Eur. Phys. J. C 70 (2010) 513 [arXiv:0909.5257] [INSPIRE].

## PDF page 144

[137] P. Artoisenet and O. Mattelaer, MadWeight5.0, in preparation.
[138] J. Alwall, A. Freitas and O. Mattelaer, The matrix element method and QCD radiation,
Phys. Rev. D 83 (2011) 074010 [arXiv:1010.2263] [INSPIRE].
[139] P. Artoisenet, P. de Aquino, F. Maltoni and O. Mattelaer, Unravelling tth via the matrix
element method, Phys. Rev. Lett. 111 (2013) 091802 [arXiv:1304.6414] [INSPIRE].
[140] T. Gleisberg et al., SHERPA 1.α: a proof of concept version, JHEP 02 (2004) 056
[hep-ph/0311263] [INSPIRE].

[142] G. Corcella et al., HERWIG 6: an event generator for hadron emission reactions with
interfering gluons (including supersymmetric processes), JHEP 01 (2001) 010
[hep-ph/0011363] [INSPIRE].
[143] G. Corcella et al., HERWIG 6.5 release note, hep-ph/0210213 [INSPIRE].
[144] S. Catani, Y.L. Dokshitzer, M.H. Seymour and B.R. Webber, Longitudinally invariant Kt
clustering algorithms for hadron hadron collisions, Nucl. Phys. B 406 (1993) 187 [INSPIRE].
[145] L. Lönnblad, Correcting the color dipole cascade model with fixed order matrix elements,
JHEP 05 (2002) 046 [hep-ph/0112284] [INSPIRE].
[146] L. Lönnblad and S. Prestel, Matching tree-level matrix elements with interleaved showers,
JHEP 03 (2012) 019 [arXiv:1109.4829] [INSPIRE].
[147] L. Lönnblad and S. Prestel, Unitarising matrix element + parton shower merging,
JHEP 02 (2013) 094 [arXiv:1211.4827] [INSPIRE].
[148] J. Alwall et al., Comparative study of various algorithms for the merging of parton showers
and matrix elements in hadronic collisions, Eur. Phys. J. C 53 (2008) 473
[arXiv:0706.2569] [INSPIRE].
[149] J. Alwall, S. de Visscher and F. Maltoni, QCD radiation in the production of heavy colored
particles at the LHC, JHEP 02 (2009) 017 [arXiv:0810.5350] [INSPIRE].
[150] P. de Aquino, F. Maltoni, K. Mawatari and B. Oexl, Light gravitino production in
association with gluinos at the LHC, JHEP 10 (2012) 008 [arXiv:1206.7098] [INSPIRE].
[151] P. Artoisenet et al., A framework for Higgs characterisation, JHEP 11 (2013) 043
[arXiv:1306.6464] [INSPIRE].
[152] F. Maltoni and T. Stelzer, MadEvent: automatic event generation with MadGraph,
JHEP 02 (2003) 027 [hep-ph/0208156] [INSPIRE].
[153] R. Kleiss and R. Pittau, Weight optimization in multichannel Monte Carlo,
Comput. Phys. Commun. 83 (1994) 141 [hep-ph/9405257] [INSPIRE].
[154] G. Passarino and M.J.G. Veltman, One loop corrections for e+ e− annihilation into µ+ µ−
in the Weinberg model, Nucl. Phys. B 160 (1979) 151 [INSPIRE].
[155] A.I. Davydychev, A simple formula for reducing Feynman diagrams to scalar integrals,
Phys. Lett. B 263 (1991) 107 [INSPIRE].
[156] G. Ossola, C.G. Papadopoulos and R. Pittau, CutTools: a program implementing the OPP
reduction method to compute one-loop amplitudes, JHEP 03 (2008) 042 [arXiv:0711.3596]
[INSPIRE].

– 142 –

JHEP07(2014)079

[141] T. Sjöstrand, S. Mrenna and P.Z. Skands, PYTHIA 6.4 physics and manual,
JHEP 05 (2006) 026 [hep-ph/0603175] [INSPIRE].

## PDF page 145

[157] G. ’t Hooft and M.J.G. Veltman, Regularization and renormalization of gauge fields,
Nucl. Phys. B 44 (1972) 189 [INSPIRE].
[158] G. Ossola, C.G. Papadopoulos and R. Pittau, On the rational terms of the one-loop
amplitudes, JHEP 05 (2008) 004 [arXiv:0802.1876] [INSPIRE].
[159] P. Draggiotis, M.V. Garzelli, C.G. Papadopoulos and R. Pittau, Feynman rules for the
rational part of the QCD 1-loop amplitudes, JHEP 04 (2009) 072 [arXiv:0903.0356]
[INSPIRE].

[161] M.V. Garzelli, I. Malamos and R. Pittau, Feynman rules for the rational part of the
electroweak 1-loop amplitudes in the Rx i gauge and in the unitary gauge,
JHEP 01 (2011) 029 [arXiv:1009.4302] [INSPIRE].
[162] H.-S. Shao, Y.-J. Zhang and K.-T. Chao, Feynman rules for the rational part of the
standard model one-loop amplitudes in the ’t Hooft-Veltman γ5 scheme,
JHEP 09 (2011) 048 [arXiv:1106.5030] [INSPIRE].
[163] R. Pittau, Primary Feynman rules to calculate the epsilon-dimensional integrand of any
1-loop amplitude, JHEP 02 (2012) 029 [arXiv:1111.4965] [INSPIRE].
[164] H.-S. Shao and Y.-J. Zhang, Feynman rules for the rational part of one-loop QCD
corrections in the MSSM, JHEP 06 (2012) 112 [arXiv:1205.1273] [INSPIRE].
[165] B. Page and R. Pittau, R2 vertices for the effective ggH theory, JHEP 09 (2013) 078
[arXiv:1307.6142] [INSPIRE].
[166] T. Binoth, J.P. Guillet and G. Heinrich, Algebraic evaluation of rational polynomials in
one-loop amplitudes, JHEP 02 (2007) 013 [hep-ph/0609054] [INSPIRE].
[167] S.D. Badger, Direct extraction of one loop rational terms, JHEP 01 (2009) 049
[arXiv:0806.4600] [INSPIRE].
[168] H.-S. Shao, Iregi user manual, unpublished.
[169] J. Fleischer, T. Riemann and V. Yundin, New developments in PJFry, PoS(LL2012)020
[arXiv:1210.4095] [INSPIRE].
[170] V. Yundin, Massive loop corrections for collider physics, Ph.D. thesis,
Humboldt-Universitat zu Berlin, Berlin Germany (2012).
[171] P. Nason, MINT: a computer program for adaptive Monte Carlo integration and generation
of unweighted distributions, arXiv:0709.2085 [INSPIRE].
[172] S. Frixione, P. Nason and B.R. Webber, Matching NLO QCD and parton showers in heavy
flavor production, JHEP 08 (2003) 007 [hep-ph/0305252] [INSPIRE].
[173] S. Frixione, E. Laenen, P. Motylinski and B.R. Webber, Single-top production in MC@NLO,
JHEP 03 (2006) 092 [hep-ph/0512250] [INSPIRE].
[174] P. Torrielli and S. Frixione, Matching NLO QCD computations with PYTHIA using
MC@NLO, JHEP 04 (2010) 110 [arXiv:1002.4293] [INSPIRE].
[175] S. Frixione, F. Stoeckli, P. Torrielli and B.R. Webber, NLO QCD corrections in
HERWIG++ with MC@NLO, JHEP 01 (2011) 053 [arXiv:1010.0568] [INSPIRE].

– 143 –

JHEP07(2014)079

[160] M.V. Garzelli, I. Malamos and R. Pittau, Feynman rules for the rational part of the
electroweak 1-loop amplitudes, JHEP 01 (2010) 040 [Erratum ibid. 10 (2010) 097]
[arXiv:0910.3130] [INSPIRE].

## PDF page 146

[176] L. Lönnblad, ARIADNE version 4: a program for simulation of QCD cascades
implementing the color dipole model, Comput. Phys. Commun. 71 (1992) 15 [INSPIRE].
[177] Z. Nagy and D.E. Soper, A new parton shower algorithm: shower evolution, matching at
leading and next-to-leading order level, hep-ph/0601021 [INSPIRE].
[178] M. Dinsdale, M. Ternick and S. Weinzierl, Parton showers from the dipole formalism,
Phys. Rev. D 76 (2007) 094003 [arXiv:0709.1026] [INSPIRE].
[179] S. Schumann and F. Krauss, A parton shower algorithm based on Catani-Seymour dipole
factorisation, JHEP 03 (2008) 038 [arXiv:0709.1027] [INSPIRE].

[181] S. Platzer and S. Gieseke, Dipole showers and automated NLO matching in HERWIG++,
Eur. Phys. J. C 72 (2012) 2187 [arXiv:1109.6256] [INSPIRE].
[182] M. Ritzmann, D.A. Kosower and P. Skands, Antenna showers with hadronic initial states,
Phys. Lett. B 718 (2013) 1345 [arXiv:1210.6345] [INSPIRE].
[183] C. Friberg, G. Gustafson and J. Hakkinen, Color connections in e+ e− annihilation,
Nucl. Phys. B 490 (1997) 289 [hep-ph/9604347] [INSPIRE].
[184] W.T. Giele, D.A. Kosower and P.Z. Skands, Higher-order corrections to timelike jets,
Phys. Rev. D 84 (2011) 054003 [arXiv:1102.2126] [INSPIRE].
[185] S. Platzer and M. Sjodahl, Subleading Nc improved parton showers, JHEP 07 (2012) 042
[arXiv:1201.0260] [INSPIRE].
[186] Z. Nagy and D.E. Soper, Parton shower evolution with subleading color,
JHEP 06 (2012) 044 [arXiv:1202.4496] [INSPIRE].
[187] G. Altarelli and G. Parisi, Asymptotic freedom in parton language,
Nucl. Phys. B 126 (1977) 298 [INSPIRE].
[188] K. Odagiri, Color connection structure of supersymmetric QCD (2 → 2) processes,
JHEP 10 (1998) 006 [hep-ph/9806531] [INSPIRE].
[189] P. Nason and B. Webber, Next-to-leading-order event generators,
Ann. Rev. Nucl. Part. Sci. 62 (2012) 187 [arXiv:1202.1251] [INSPIRE].
[190] S. Hoeche, F. Krauss and M. Schonherr, Uncertainties in MEPS@NLO calculations of
h+jets, arXiv:1401.7971 [INSPIRE].
[191] R. Frederix and S. Frixione, Merging meets matching in MC@NLO, JHEP 12 (2012) 061
[arXiv:1209.6215] [INSPIRE].
[192] S. Catani, F. Krauss, R. Kuhn and B.R. Webber, QCD matrix elements + parton showers,
JHEP 11 (2001) 063 [hep-ph/0109231] [INSPIRE].
[193] F. Krauss, Matrix elements and parton showers in hadronic interactions,
JHEP 08 (2002) 015 [hep-ph/0205283] [INSPIRE].
[194] S. Mrenna and P. Richardson, Matching matrix elements and parton showers with
HERWIG and PYTHIA, JHEP 05 (2004) 040 [hep-ph/0312274] [INSPIRE].
[195] N. Lavesson and L. Lönnblad, W +jets matrix elements and the dipole cascade,
JHEP 07 (2005) 054 [hep-ph/0503293] [INSPIRE].

– 144 –

JHEP07(2014)079

[180] J.-C. Winter and F. Krauss, Initial-state showering based on colour dipoles connected to
incoming parton lines, JHEP 07 (2008) 040 [arXiv:0712.3913] [INSPIRE].

## PDF page 147

[196] S. Hoeche, F. Krauss, S. Schumann and F. Siegert, QCD matrix elements and truncated
showers, JHEP 05 (2009) 053 [arXiv:0903.1219] [INSPIRE].
[197] K. Hamilton, P. Richardson and J. Tully, A modified CKKW matrix element merging
approach to angular-ordered parton showers, JHEP 11 (2009) 038 [arXiv:0905.3072]
[INSPIRE].
[198] N. Lavesson and L. Lönnblad, Extending CKKW-merging to one-loop matrix elements,
JHEP 12 (2008) 070 [arXiv:0811.2912] [INSPIRE].
[199] K. Hamilton and P. Nason, Improving NLO-parton shower matched simulations with higher
order matrix elements, JHEP 06 (2010) 039 [arXiv:1004.1764] [INSPIRE].

[201] S. Alioli, K. Hamilton and E. Re, Practical improvements and merging of POWHEG
simulations for vector boson production, JHEP 09 (2011) 104 [arXiv:1108.0909] [INSPIRE].
[202] S. Hoeche, F. Krauss, M. Schonherr and F. Siegert, QCD matrix elements + parton
showers: the NLO case, JHEP 04 (2013) 027 [arXiv:1207.5030] [INSPIRE].
[203] S. Plätzer, Controlling inclusive cross sections in parton shower + matrix element merging,
JHEP 08 (2013) 114 [arXiv:1211.5467] [INSPIRE].
[204] S. Alioli et al., Combining higher-order resummation with multiple NLO calculations and
parton showers in GENEVA, JHEP 09 (2013) 120 [arXiv:1211.7049] [INSPIRE].
[205] L. Lönnblad and S. Prestel, Merging multi-leg NLO matrix elements with parton showers,
JHEP 03 (2013) 166 [arXiv:1211.7278] [INSPIRE].
[206] K. Hamilton, P. Nason, C. Oleari and G. Zanderighi, Merging H/W/Z + 0 and 1 jet at
NLO with no merging scale: a path to parton shower + NNLO matching,
JHEP 05 (2013) 082 [arXiv:1212.4504] [INSPIRE].
[207] S. Alioli et al., Matching fully differential NNLO calculations and parton showers,
JHEP 06 (2014) 089 [arXiv:1311.0286] [INSPIRE].
[208] G. Bozzi, S. Catani, D. de Florian and M. Grazzini, Transverse-momentum resummation
and the spectrum of the Higgs boson at the LHC, Nucl. Phys. B 737 (2006) 73
[hep-ph/0508068] [INSPIRE].
[209] R.G. Stuart, Gauge invariance, analyticity and physical observables at the Z 0 resonance,
Phys. Lett. B 262 (1991) 113 [INSPIRE].
[210] A. Aeppli, G.J. van Oldenborgh and D. Wyler, Unstable particles in one loop calculations,
Nucl. Phys. B 428 (1994) 126 [hep-ph/9312212] [INSPIRE].
[211] S. Frixione, E. Laenen, P. Motylinski and B.R. Webber, Angular correlations of lepton pairs
from vector boson and top quark decays in Monte Carlo simulations, JHEP 04 (2007) 081
[hep-ph/0702198] [INSPIRE].
[212] P. Richardson, Spin correlations in Monte Carlo simulations, JHEP 11 (2001) 029
[hep-ph/0110108] [INSPIRE].
[213] P. Artoisenet, R. Frederix, O. Mattelaer and R. Rietkerk, Automatic spin-entangled decays
of heavy resonances in Monte Carlo simulations, JHEP 03 (2013) 015 [arXiv:1212.3460]
[INSPIRE].

– 145 –

JHEP07(2014)079

[200] S. Hoche, F. Krauss, M. Schonherr and F. Siegert, NLO matrix elements and truncated
showers, JHEP 08 (2011) 123 [arXiv:1009.1127] [INSPIRE].

## PDF page 148

[214] A.S. Papanastasiou, R. Frederix, S. Frixione, V. Hirschi and F. Maltoni, Single-top
t-channel production with off-shell and non-resonant effects, Phys. Lett. B 726 (2013) 223
[arXiv:1305.7088] [INSPIRE].
[215] J. Conway, Pretty Good Simulator webpage,
http://www.physics.ucdavis.edu/∼conway/research/software/pgs/pgs4-general.htm.
[216] DELPHES 3 collaboration, J. de Favereau et al., DELPHES 3, a modular framework for
fast simulation of a generic collider experiment, JHEP 02 (2014) 057 [arXiv:1307.6346]
[INSPIRE].

[218] SM Working group collaboration, Proceedings of the workshop physics at TeV colliders,
Les Houches, 2013, to appear.
[219] A.D. Martin, W.J. Stirling, R.S. Thorne and G. Watt, Parton distributions for the LHC,
Eur. Phys. J. C 63 (2009) 189 [arXiv:0901.0002] [INSPIRE].
[220] M. Cacciari, G.P. Salam and G. Soyez, The anti-kt jet clustering algorithm,
JHEP 04 (2008) 063 [arXiv:0802.1189] [INSPIRE].
[221] S. Frixione, Isolated photons in perturbative QCD, Phys. Lett. B 429 (1998) 369
[hep-ph/9801442] [INSPIRE].
[222] R. Frederix, E. Re and P. Torrielli, Single-top t-channel hadroproduction in the four-flavour
scheme with POWHEG and aMC@NLO, JHEP 09 (2012) 130 [arXiv:1207.5391]
[INSPIRE].
[223] J.M. Campbell and R.K. Ellis, Next-to-leading order corrections to W + 2 jet and Z + 2 jet
production at hadron colliders, Phys. Rev. D 65 (2002) 113007 [hep-ph/0202176]
[INSPIRE].
[224] J.M. Campbell, R.K. Ellis and D.L. Rainwater, Next-to-leading order QCD predictions for
W + 2 jet and Z + 2 jet production at the CERN LHC, Phys. Rev. D 68 (2003) 094021
[hep-ph/0308195] [INSPIRE].
[225] J.M. Campbell, R.K. Ellis, P. Nason and G. Zanderighi, W and Z bosons in association with
two jets using the POWHEG method, JHEP 08 (2013) 005 [arXiv:1303.5447] [INSPIRE].
[226] J.M. Campbell et al., Associated production of a W boson and one b jet,
Phys. Rev. D 79 (2009) 034023 [arXiv:0809.3003] [INSPIRE].
[227] J.M. Campbell, R.K. Ellis, F. Maltoni and S. Willenbrock, Associated production of a Z
boson and a single heavy quark jet, Phys. Rev. D 69 (2004) 074021 [hep-ph/0312024]
[INSPIRE].
[228] J.M. Campbell, R.K. Ellis, F. Maltoni and S. Willenbrock, Production of a Z boson and
two jets with one heavy-quark tag, Phys. Rev. D 73 (2006) 054007 [Erratum ibid. D 77
(2008) 019903] [hep-ph/0510362] [INSPIRE].
[229] J.M. Campbell, R.K. Ellis, F. Maltoni and S. Willenbrock, Production of a W boson and
two jets with one b− quark tag, Phys. Rev. D 75 (2007) 054015 [hep-ph/0611348]
[INSPIRE].

– 146 –

JHEP07(2014)079

[217] S. Ovyn, X. Rouby and V. Lemaitre, DELPHES, a framework for fast simulation of a
generic collider experiment, arXiv:0903.2225 [INSPIRE].

## PDF page 149

[230] J.M. Campbell, F. Caola, F. Febres Cordero, L. Reina and D. Wackeroth, NLO QCD
predictions for W + 1 jet and W + 2 jet production with at least one b jet at the 7 TeV LHC,
Phys. Rev. D 86 (2012) 034021 [arXiv:1107.3714] [INSPIRE].
[231] S. Alioli, P. Nason, C. Oleari and E. Re, NLO vector-boson production matched with shower
in POWHEG, JHEP 07 (2008) 060 [arXiv:0805.4802] [INSPIRE].
[232] S. Alioli, P. Nason, C. Oleari and E. Re, Vector boson plus one jet production in POWHEG,
JHEP 01 (2011) 095 [arXiv:1009.5594] [INSPIRE].
[233] E. Re, NLO corrections merged with parton showers for Z + 2 jets production using the
POWHEG method, JHEP 10 (2012) 031 [arXiv:1204.5433] [INSPIRE].

[235] K. Melnikov and G. Zanderighi, W + 3 jet production at the LHC as a signal or background,
Phys. Rev. D 81 (2010) 074025 [arXiv:0910.3671] [INSPIRE].
[236] C.F. Berger et al., Precise predictions for W + 3 jet production at hadron colliders,
Phys. Rev. Lett. 102 (2009) 222001 [arXiv:0902.2760] [INSPIRE].
[237] C.F. Berger et al., Next-to-leading order QCD predictions for W + 3-jet distributions at
hadron colliders, Phys. Rev. D 80 (2009) 074036 [arXiv:0907.1984] [INSPIRE].
[238] C.F. Berger et al., Next-to-leading order QCD predictions for Z, γ ∗ + 3-jet distributions at
the Tevatron, Phys. Rev. D 82 (2010) 074002 [arXiv:1004.1659] [INSPIRE].
[239] C.F. Berger et al., Precise predictions for W + 4 jet production at the Large Hadron
Collider, Phys. Rev. Lett. 106 (2011) 092001 [arXiv:1009.2338] [INSPIRE].
[240] H. Ita et al., Precise predictions for Z + 4 jets at hadron colliders,
Phys. Rev. D 85 (2012) 031501 [arXiv:1108.2229] [INSPIRE].
[241] S. Hoeche, F. Krauss, M. Schonherr and F. Siegert, W + n-jet predictions at the Large
Hadron Collider at next-to-leading order matched with a parton shower,
Phys. Rev. Lett. 110 (2013) 052001 [arXiv:1201.5882] [INSPIRE].
[242] S. Catani, M. Fontannaz, J.P. Guillet and E. Pilon, Cross-section of isolated prompt
photons in hadron hadron collisions, JHEP 05 (2002) 028 [hep-ph/0204023] [INSPIRE].
[243] Z. Bern et al., Driving missing data at next-to-leading order,
Phys. Rev. D 84 (2011) 114002 [arXiv:1106.1423] [INSPIRE].
[244] K. Arnold et al., VBFNLO: a parton level Monte Carlo for processes with electroweak
bosons — manual for version 2.5.0, arXiv:1107.4038 [INSPIRE].
[245] B. Jager, S. Schneider and G. Zanderighi, Next-to-leading order QCD corrections to
electroweak Zjj production in the POWHEG BOX, JHEP 09 (2012) 083
[arXiv:1207.2626] [INSPIRE].
[246] B. Mele, P. Nason and G. Ridolfi, QCD radiative corrections to Z boson pair production in
hadronic collisions, Nucl. Phys. B 357 (1991) 409 [INSPIRE].
[247] J. Ohnemus and J.F. Owens, An order αs calculation of hadronic ZZ production,
Phys. Rev. D 43 (1991) 3626 [INSPIRE].
[248] S. Frixione, P. Nason and G. Ridolfi, Strong corrections to W Z production at hadron
colliders, Nucl. Phys. B 383 (1992) 3 [INSPIRE].

– 147 –

JHEP07(2014)079

[234] R.K. Ellis, K. Melnikov and G. Zanderighi, Generalized unitarity at work: first NLO QCD
results for hadronic W + 3 jet production, JHEP 04 (2009) 077 [arXiv:0901.4101]
[INSPIRE].

## PDF page 150

[249] J. Ohnemus, An order αs calculation of hadronic W − W + production,
Phys. Rev. D 44 (1991) 1403 [INSPIRE].
[250] J. Ohnemus, An order αs calculation of hadronic W ± Z production,
Phys. Rev. D 44 (1991) 3477 [INSPIRE].
[251] S. Frixione, A next-to-leading order calculation of the cross-section for the production of
W + W − pairs in hadronic collisions, Nucl. Phys. B 410 (1993) 280 [INSPIRE].
[252] J.M. Campbell and R.K. Ellis, An update on vector boson pair production at hadron
colliders, Phys. Rev. D 60 (1999) 113006 [hep-ph/9905386] [INSPIRE].

[254] D. De Florian and A. Signer, W γ and Zγ production at hadron colliders,
Eur. Phys. J. C 16 (2000) 105 [hep-ph/0002138] [INSPIRE].
[255] N. Greiner et al., NLO QCD corrections to the production of W + W − plus two jets at the
LHC, Phys. Lett. B 713 (2012) 277 [arXiv:1202.6004] [INSPIRE].
[256] J.M. Campbell, R.K. Ellis and C. Williams, Vector boson pair production at the LHC,
JHEP 07 (2011) 018 [arXiv:1105.0020] [INSPIRE].
[257] P. Nason and G. Ridolfi, A positive-weight next-to-leading-order Monte Carlo for Z pair
hadroproduction, JHEP 08 (2006) 077 [hep-ph/0606275] [INSPIRE].
[258] T. Melia, P. Nason, R. Rontsch and G. Zanderighi, W + W − , W Z and ZZ production in the
POWHEG BOX, JHEP 11 (2011) 078 [arXiv:1107.5051] [INSPIRE].
[259] P. Nason and G. Zanderighi, W + W − , W Z and ZZ production in the POWHEG-BOX-V 2,
Eur. Phys. J. C 74 (2014) 2702 [arXiv:1311.1365] [INSPIRE].
[260] V. Del Duca, F. Maltoni, Z. Nagy and Z. Trócsányi, QCD radiative corrections to prompt
diphoton production in association with a jet at hadron colliders, JHEP 04 (2003) 059
[hep-ph/0303012] [INSPIRE].
[261] T. Gehrmann, N. Greiner and G. Heinrich, Precise QCD predictions for the production of a
photon pair in association with two jets, Phys. Rev. Lett. 111 (2013) 222002
[arXiv:1308.3660] [INSPIRE].
[262] S. Badger, A. Guffanti and V. Yundin, Next-to-leading order QCD corrections to di-photon
production in association with up to three jets at the Large Hadron Collider,
JHEP 03 (2014) 122 [arXiv:1312.5927] [INSPIRE].
[263] Z. Bern et al., Next-to-leading order diphoton+2-jet production at the LHC,
arXiv:1312.0592 [INSPIRE].
[264] Z. Bern et al., Next-to-leading order γγ + 2-jet production at the LHC, arXiv:1402.4127
[INSPIRE].
[265] T. Melia, K. Melnikov, R. Rontsch and G. Zanderighi, Next-to-leading order QCD
predictions for W + W + jj production at the LHC, JHEP 12 (2010) 053 [arXiv:1007.5313]
[INSPIRE].
[266] F. Campanario, M. Kerner, L.D. Ninh and D. Zeppenfeld, Next-to-leading order QCD
corrections to W + W + and W − W − production in association with two jets,
Phys. Rev. D 89 (2014) 054009 [arXiv:1311.6738] [INSPIRE].

– 148 –

JHEP07(2014)079

[253] L.J. Dixon, Z. Kunszt and A. Signer, Vector boson pair production in hadronic collisions at
order αs : lepton correlations and anomalous couplings, Phys. Rev. D 60 (1999) 114037
[hep-ph/9907305] [INSPIRE].

## PDF page 151

[267] J.M. Campbell, H.B. Hartanto and C. Williams, Next-to-leading order predictions for
Zγ+jet and Zγγ final states at the LHC, JHEP 11 (2012) 162 [arXiv:1208.0566]
[INSPIRE].
[268] F. Campanario, M. Kerner, L.D. Ninh and D. Zeppenfeld, Next-to-leading order QCD
corrections to W γ production in association with two jets, arXiv:1402.0505 [INSPIRE].
[269] F. Campanario, M. Kerner, L.D. Ninh and D. Zeppenfeld, NLO QCD corrections to W Zjj
production at the LHC, arXiv:1310.4369 [INSPIRE].
[270] F. Campanario, C. Englert, M. Spannowsky and D. Zeppenfeld, NLO-QCD corrections to
W γj production, Europhys. Lett. 88 (2009) 11001 [arXiv:0908.1638] [INSPIRE].

[272] F. Campanario, C. Englert, S. Kallweit, M. Spannowsky and D. Zeppenfeld, NLO QCD
corrections to W Z+jet production with leptonic decays, JHEP 07 (2010) 076
[arXiv:1006.0390] [INSPIRE].
[273] B. Jager and G. Zanderighi, Electroweak W + W − jj prodution at NLO in QCD matched with
parton shower in the POWHEG-BOX, JHEP 04 (2013) 024 [arXiv:1301.1695] [INSPIRE].
[274] F. Schissler and D. Zeppenfeld, Parton shower effects on W and Z production via vector
boson fusion at NLO QCD, JHEP 04 (2013) 057 [arXiv:1302.2884] [INSPIRE].
[275] B. Jäger, A. Karlberg and G. Zanderighi, Electroweak ZZjj production in the standard
model and beyond in the POWHEG-BOX-V 2, JHEP 03 (2014) 141 [arXiv:1312.3252]
[INSPIRE].
[276] G. Bozzi, F. Campanario, M. Rauch and D. Zeppenfeld, Zγγ production with leptonic
decays and triple photon production at next-to-leading order QCD,
Phys. Rev. D 84 (2011) 074028 [arXiv:1107.3149] [INSPIRE].
[277] G. Bozzi, F. Campanario, M. Rauch and D. Zeppenfeld, W +− γγ production with leptonic
decays at NLO QCD, Phys. Rev. D 83 (2011) 114035 [arXiv:1103.4613] [INSPIRE].
[278] G. Bozzi, F. Campanario, M. Rauch, H. Rzehak and D. Zeppenfeld, NLO QCD corrections
to W ± Zγ production with leptonic decays, Phys. Lett. B 696 (2011) 380
[arXiv:1011.2206] [INSPIRE].
[279] G. Bozzi, F. Campanario, V. Hankele and D. Zeppenfeld, NLO QCD corrections to
W + W − γ and ZZγ production with leptonic decays, Phys. Rev. D 81 (2010) 094030
[arXiv:0911.0438] [INSPIRE].
[280] F. Campanario, V. Hankele, C. Oleari, S. Prestel and D. Zeppenfeld, QCD corrections to
charged triple vector boson production with leptonic decay, Phys. Rev. D 78 (2008) 094012
[arXiv:0809.0790] [INSPIRE].
[281] J.M. Campbell and C. Williams, Triphoton production at hadron colliders,
Phys. Rev. D 89 (2014) 113001 [arXiv:1403.2641] [INSPIRE].
[282] M.K. Mandal, P. Mathews, V. Ravindran and S. Seth, Three photon production to
NLO+PS accuracy at the LHC, arXiv:1403.2917 [INSPIRE].
[283] A. Lazopoulos, K. Melnikov and F. Petriello, QCD corrections to tri-boson production,
Phys. Rev. D 76 (2007) 014001 [hep-ph/0703273] [INSPIRE].

– 149 –

JHEP07(2014)079

[271] F. Campanario, C. Englert and M. Spannowsky, Precise predictions for (non-standard) W γ
+ jet production, Phys. Rev. D 83 (2011) 074009 [arXiv:1010.1291] [INSPIRE].

## PDF page 152

[284] F. Campanario, C. Englert, M. Rauch and D. Zeppenfeld, Precise predictions for W γγ +jet
production at hadron colliders, Phys. Lett. B 704 (2011) 515 [arXiv:1106.4009] [INSPIRE].
[285] S. Hoeche et al., Triple vector boson production through Higgs-Strahlung with NLO multijet
merging, Phys. Rev. D 89 (2014) 093015 [arXiv:1403.7516] [INSPIRE].
[286] P. Nason, S. Dawson and R.K. Ellis, The total cross-section for the production of heavy
quarks in hadronic collisions, Nucl. Phys. B 303 (1988) 607 [INSPIRE].
[287] W. Beenakker, H. Kuijf, W.L. van Neerven and J. Smith, QCD corrections to heavy quark
production in pp̄ collisions, Phys. Rev. D 40 (1989) 54 [INSPIRE].

[289] W. Beenakker, W.L. van Neerven, R. Meng, G.A. Schuler and J. Smith, QCD corrections to
heavy quark production in hadron hadron collisions, Nucl. Phys. B 351 (1991) 507
[INSPIRE].
[290] M.L. Mangano, P. Nason and G. Ridolfi, Heavy quark correlations in hadron collisions at
next-to-leading order, Nucl. Phys. B 373 (1992) 295 [INSPIRE].
[291] S. Frixione, P. Nason and G. Ridolfi, A positive-weight next-to-leading-order Monte Carlo
for heavy flavour hadroproduction, JHEP 09 (2007) 126 [arXiv:0707.3088] [INSPIRE].
[292] S. Dittmaier, P. Uwer and S. Weinzierl, NLO QCD corrections to tt̄ + jet production at
hadron colliders, Phys. Rev. Lett. 98 (2007) 262002 [hep-ph/0703120] [INSPIRE].
[293] K. Melnikov, A. Scharf and M. Schulze, Top quark pair production in association with a jet:
QCD corrections and jet radiation in top quark decays, Phys. Rev. D 85 (2012) 054002
[arXiv:1111.4991] [INSPIRE].
[294] S. Alioli, S.-O. Moch and P. Uwer, Hadronic top-quark pair-production with one jet and
parton showering, JHEP 01 (2012) 137 [arXiv:1110.5251] [INSPIRE].
[295] G. Bevilacqua, M. Czakon, C.G. Papadopoulos and M. Worek, Dominant QCD backgrounds
in Higgs boson analyses at the LHC: a study of pp → tt̄ + 2 jets at next-to-leading order,
Phys. Rev. Lett. 104 (2010) 162002 [arXiv:1002.4009] [INSPIRE].
[296] M. Schönherr, S. Höche, J. Huang, G. Luisoni and J. Winter, NLO merging in tt̄+jets,
PoS(EPS-HEP 2013)246 [arXiv:1311.3621] [INSPIRE].
[297] S. Hoeche et al., Next-to-leading order QCD predictions for top-quark pair production with
up to two jets merged with a parton shower, arXiv:1402.6293 [INSPIRE].
[298] Z. Nagy, Next-to-leading order calculation of three jet observables in hadron hadron
collision, Phys. Rev. D 68 (2003) 094002 [hep-ph/0307268] [INSPIRE].
[299] S. Badger, B. Biedermann, P. Uwer and V. Yundin, NLO QCD corrections to multi-jet
√
production at the LHC with a centre-of-mass energy of s = 8 TeV,
Phys. Lett. B 718 (2013) 965 [arXiv:1209.0098] [INSPIRE].
[300] S. Badger, B. Biedermann, P. Uwer and V. Yundin, Next-to-leading order QCD corrections
to five jet production at the LHC, Phys. Rev. D 89 (2014) 034019 [arXiv:1309.6585]
[INSPIRE].
[301] S. Alioli, K. Hamilton, P. Nason, C. Oleari and E. Re, Jet pair production in POWHEG,
JHEP 04 (2011) 081 [arXiv:1012.3380] [INSPIRE].

– 150 –

JHEP07(2014)079

[288] P. Nason, S. Dawson and R.K. Ellis, The one particle inclusive differential cross-section for
heavy quark production in hadronic collisions, Nucl. Phys. B 327 (1989) 49 [Erratum ibid.
B 335 (1990) 260] [INSPIRE].

## PDF page 153

[302] A. Kardos, P. Nason and C. Oleari, Three-jet production in POWHEG,
JHEP 04 (2014) 043 [arXiv:1402.4001] [INSPIRE].
[303] N. Greiner, A. Guffanti, T. Reiter and J. Reuter, NLO QCD corrections to the production
of two bottom-antibottom pairs at the LHC, Phys. Rev. Lett. 107 (2011) 102002
[arXiv:1105.3624] [INSPIRE].
[304] G. Bevilacqua, M. Czakon, M. Krämer, M. Kubocz and M. Worek, Quantifying quark mass
effects at the LHC: a study of pp → bb̄bb̄ + X at next-to-leading order, JHEP 07 (2013) 095
[arXiv:1304.6860] [INSPIRE].

[306] A. Bredenstein, A. Denner, S. Dittmaier and S. Pozzorini, NLO QCD corrections to
pp → tt̄bb̄ + X at the LHC, Phys. Rev. Lett. 103 (2009) 012002 [arXiv:0905.0110]
[INSPIRE].
[307] A. Bredenstein, A. Denner, S. Dittmaier and S. Pozzorini, NLO QCD corrections to top
anti-top bottom anti-bottom production at the LHC: 2. Full hadronic results,
JHEP 03 (2010) 021 [arXiv:1001.4006] [INSPIRE].
[308] G. Bevilacqua and M. Worek, Constraining BSM physics at the LHC: four top final states
with NLO accuracy in perturbative QCD, JHEP 07 (2012) 111 [arXiv:1206.3064]
[INSPIRE].
[309] R.K. Ellis and S. Veseli, Strong radiative corrections to W bb̄ production in pp̄ collisions,
Phys. Rev. D 60 (1999) 011501 [hep-ph/9810489] [INSPIRE].
[310] S. Badger, J.M. Campbell and R.K. Ellis, QCD corrections to the hadronic production of a
heavy quark pair and a W -boson including decay correlations, JHEP 03 (2011) 027
[arXiv:1011.6647] [INSPIRE].
[311] R. Frederix et al., W and Z/γ∗ boson production in association with a bottom-antibottom
pair, JHEP 09 (2011) 061 [arXiv:1106.6019] [INSPIRE].
[312] C. Oleari and L. Reina, W ± bb̄ production in POWHEG, JHEP 08 (2011) 061 [Erratum
ibid. 11 (2011) 040] [arXiv:1105.4488] [INSPIRE].
[313] J.M. Campbell and R.K. Ellis, Radiative corrections to Zbb̄ production,
Phys. Rev. D 62 (2000) 114012 [hep-ph/0006304] [INSPIRE].
[314] K. Melnikov, M. Schulze and A. Scharf, QCD corrections to top quark pair production in
association with a photon at hadron colliders, Phys. Rev. D 83 (2011) 074013
[arXiv:1102.1967] [INSPIRE].
[315] A. Lazopoulos, T. McElmurry, K. Melnikov and F. Petriello, Next-to-leading order QCD
corrections to tt̄Z production at the LHC, Phys. Lett. B 666 (2008) 62 [arXiv:0804.2220]
[INSPIRE].
[316] M.V. Garzelli, A. Kardos, C.G. Papadopoulos and Z. Trócsányi, tt̄W +− and tt̄Z
hadroproduction at NLO accuracy in QCD with parton shower and hadronization effects,
JHEP 11 (2012) 056 [arXiv:1208.2665] [INSPIRE].
[317] J.M. Campbell and R.K. Ellis, tt̄W +− production and decay at NLO, JHEP 07 (2012) 052
[arXiv:1204.5678] [INSPIRE].

– 151 –

JHEP07(2014)079

[305] G. Bevilacqua, M. Czakon, C.G. Papadopoulos, R. Pittau and M. Worek, Assault on the
NLO wishlist: pp → tt̄bb̄, JHEP 09 (2009) 109 [arXiv:0907.4723] [INSPIRE].

## PDF page 154

[318] T. Stelzer and S. Willenbrock, Single top quark production via q q̄ → tb̄,
Phys. Lett. B 357 (1995) 125 [hep-ph/9505433] [INSPIRE].
[319] T. Stelzer, Z. Sullivan and S. Willenbrock, Single top quark production via W -gluon fusion
at next-to-leading order, Phys. Rev. D 56 (1997) 5919 [hep-ph/9705398] [INSPIRE].
[320] J.M. Campbell, R.K. Ellis and F. Tramontano, Single top production and decay at
next-to-leading order, Phys. Rev. D 70 (2004) 094012 [hep-ph/0408158] [INSPIRE].
[321] J.M. Campbell, R. Frederix, F. Maltoni and F. Tramontano, NLO predictions for t-channel
production of single top and fourth generation quarks at hadron colliders,
JHEP 10 (2009) 042 [arXiv:0907.3933] [INSPIRE].

[323] J.M. Campbell and F. Tramontano, Next-to-leading order corrections to W t production and
decay, Nucl. Phys. B 726 (2005) 109 [hep-ph/0506289] [INSPIRE].
[324] S. Frixione, E. Laenen, P. Motylinski, B.R. Webber and C.D. White, Single-top
hadroproduction in association with a W boson, JHEP 07 (2008) 029 [arXiv:0805.3067]
[INSPIRE].
[325] S. Alioli, P. Nason, C. Oleari and E. Re, NLO single-top production matched with shower in
POWHEG: s- and t-channel contributions, JHEP 09 (2009) 111 [Erratum ibid. 02 (2010)
011] [arXiv:0907.4076] [INSPIRE].
[326] E. Re, Single-top W t-channel production matched with parton showers using the POWHEG
method, Eur. Phys. J. C 71 (2011) 1547 [arXiv:1009.2450] [INSPIRE].
[327] J. Campbell, R.K. Ellis and R. Rötsch, Single top production in association with a Z boson
at the LHC, Phys. Rev. D 87 (2013) 114006 [arXiv:1302.3856] [INSPIRE].
[328] LHC Higgs Cross section Working Group collaboration, S. Dittmaier et al.,
Handbook of LHC Higgs cross sections: 1. Inclusive observables, arXiv:1101.0593
[INSPIRE].
[329] LHC Higgs Cross section Working Group collaboration, S. Dittmaier et al.,
Handbook of LHC Higgs cross sections: 2. Differential distributions, arXiv:1201.3084
[INSPIRE].
[330] LHC Higgs Cross section Working Group collaboration, S. Heinemeyer et al.,
Handbook of LHC Higgs cross sections: 3. Higgs properties, arXiv:1307.1347 [INSPIRE].
[331] J. Baglio et al., The measurement of the Higgs self-coupling at the LHC: theoretical status,
JHEP 04 (2013) 151 [arXiv:1212.5581] [INSPIRE].
[332] T. Plehn, M. Spira and P.M. Zerwas, Pair production of neutral Higgs particles in
gluon-gluon collisions, Nucl. Phys. B 479 (1996) 46 [Erratum ibid. B 531 (1998) 655]
[hep-ph/9603205] [INSPIRE].
[333] S. Dawson, S. Dittmaier and M. Spira, Neutral Higgs boson pair production at hadron
colliders: QCD corrections, Phys. Rev. D 58 (1998) 115012 [hep-ph/9805244] [INSPIRE].
[334] A. Signer and L.J. Dixon, Electron-positron annihilation into four jets at next-to-leading
order in αs , Phys. Rev. Lett. 78 (1997) 811 [hep-ph/9609460] [INSPIRE].

– 152 –

JHEP07(2014)079

[322] J.M. Campbell, R. Frederix, F. Maltoni and F. Tramontano, Next-to-leading-order
predictions for t-channel single-top production at hadron colliders,
Phys. Rev. Lett. 102 (2009) 182003 [arXiv:0903.0005] [INSPIRE].

## PDF page 155

[335] A. Signer, Next-to-leading order corrections to e+ e− → four jets, hep-ph/9705218
[INSPIRE].
[336] Z. Nagy and Z. Trócsányi, Four jet production in e+ e− annihilation at next-to-leading
order, Nucl. Phys. Proc. Suppl. 64 (1998) 63 [hep-ph/9708344] [INSPIRE].
[337] Z. Nagy and Z. Trócsányi, Next-to-leading order calculation of four jet shape variables,
Phys. Rev. Lett. 79 (1997) 3604 [hep-ph/9707309] [INSPIRE].
[338] R. Frederix, S. Frixione, K. Melnikov and G. Zanderighi, NLO QCD corrections to five-jet
production at LEP and the extraction of αs (MZ ), JHEP 11 (2010) 050 [arXiv:1008.5313]
[INSPIRE].

[340] C.R. Schmidt, Top quark production and decay at next-to-leading order in e+ e−
annihilation, Phys. Rev. D 54 (1996) 3250 [hep-ph/9504434] [INSPIRE].
[341] C. Oleari, Next-to-leading order corrections to the production of heavy flavor jets in e+ e−
collisions, hep-ph/9802431 [INSPIRE].
[342] P. Nason and C. Oleari, Next-to-leading order corrections to the production of heavy flavor
jets in e+ e− collisions, Nucl. Phys. B 521 (1998) 237 [hep-ph/9709360] [INSPIRE].
[343] W. Bernreuther, A. Brandenburg and P. Uwer, Next-to-leading order QCD corrections to
three jet cross-sections with massive quarks, Phys. Rev. Lett. 79 (1997) 189
[hep-ph/9703305] [INSPIRE].
[344] A. Brandenburg and P. Uwer, Next-to-leading order QCD corrections and massive quarks in
e+ e− → three jets, Nucl. Phys. B 515 (1998) 279 [hep-ph/9708350] [INSPIRE].
[345] A. Brandenburg, The reaction e+ e− → tt̄g at next-to-leading order in αs , hep-ph/9908383
[INSPIRE].

[346] S. Dittmaier, M. Krämer, Y. Liao, M. Spira and P.M. Zerwas, Higgs radiation off top
quarks in e+ e− collisions, Phys. Lett. B 441 (1998) 383 [hep-ph/9808433] [INSPIRE].
[347] S. Frixione, P. Torrielli and M. Zaro, Higgs production through vector-boson fusion at the
NLO matched with parton showers, Phys. Lett. B 726 (2013) 273 [arXiv:1304.7927]
[INSPIRE].
[348] ATLAS collaboration, Measurement of top-quark pair differential cross-sections in the
√
l+jets channel in pp collisions at s = 7 TeV using the ATLAS detector,
ATLAS-CONF-2013-099, CERN, Geneva Switzerland (2013).
[349] CMS collaboration, Measurement of differential top-quark pair production cross sections in
√
pp colisions at s = 7 TeV, Eur. Phys. J. C 73 (2013) 2339 [arXiv:1211.2220] [INSPIRE].
[350] CMS collaboration, Measurement of differential top-quark pair production cross sections in
the lepton+jets channel in pp collisions at 8 TeV, CMS-TOP-12-027, CERN, Geneva
Switzerland (2012).
[351] CMS collaboration, Measurement of the differential tt̄ cross section in the dilepton channel
at 8 TeV, CMS-TOP-12-028, CERN, Geneva Switzerland (2012).
[352] ATLAS collaboration, Measurement of tt̄ production with a veto on additional central jet
√
activity in pp collisions at s = 7 TeV using the ATLAS detector,
Eur. Phys. J. C 72 (2012) 2043 [arXiv:1203.5015] [INSPIRE].

– 153 –

JHEP07(2014)079

[339] M.S. Bilenky, G. Rodrigo and A. Santamaria, Three jet production at LEP and the bottom
quark mass, Nucl. Phys. B 439 (1995) 505 [hep-ph/9410258] [INSPIRE].

## PDF page 156

[353] CMS collaboration, Measurement of jet multiplicity distributions in top quark events with
two leptons in the final state at a centre-of-mass energy of 7 TeV, CMS-TOP-12-023,
CERN, Geneva Switzerland (2012).
[354] CMS collaboration, Measurement of the jet multiplicity in dileptonic top quark pair events
at 8 TeV, CMS-TOP-12-041, CERN, Geneva Switzerland (2012).
[355] S. Dittmaier and M. Kramer, Electroweak radiative corrections to W boson production at
hadron colliders, Phys. Rev. D 65 (2002) 073007 [hep-ph/0109062] [INSPIRE].

[357] W. Beenakker et al., NLO QCD corrections to tt̄H production in hadron collisions,
Nucl. Phys. B 653 (2003) 151 [hep-ph/0211352] [INSPIRE].
[358] T. Binoth, G. Ossola, C.G. Papadopoulos and R. Pittau, NLO QCD corrections to tri-boson
production, JHEP 06 (2008) 082 [arXiv:0804.0350] [INSPIRE].
[359] T. Melia, K. Melnikov, R. Rontsch and G. Zanderighi, NLO QCD corrections for W + W −
pair production in association with two jets at hadron colliders,
Phys. Rev. D 83 (2011) 114043 [arXiv:1104.2327] [INSPIRE].
[360] G. Cullen et al., Next-to-leading-order QCD corrections to Higgs boson production plus three
jets in gluon fusion, Phys. Rev. Lett. 111 (2013) 131801 [arXiv:1307.4737] [INSPIRE].
[361] H. van Deurzen et al., Next-to-leading-order QCD corrections to Higgs boson production in
association with a top quark pair and a jet, Phys. Rev. Lett. 111 (2013) 171801
[arXiv:1307.8437] [INSPIRE].
[362] A. Kardos and Z. Trócsányi, Hadroproduction of tt̄ pair with a bb̄ pair using PowHel,
J. Phys. G 41 (2014) 075005 [arXiv:1303.6291] [INSPIRE].
[363] A. Kardos, Z. Trócsányi and C. Papadopoulos, Top quark pair production in association
with a Z-boson at NLO accuracy, Phys. Rev. D 85 (2012) 054015 [arXiv:1111.0610]
[INSPIRE].
[364] M.V. Garzelli, A. Kardos, C.G. Papadopoulos and Z. Trócsányi, Z 0 -boson production in
association with a top anti-top pair at NLO accuracy with parton shower effects,
Phys. Rev. D 85 (2012) 074022 [arXiv:1111.1444] [INSPIRE].
[365] A. Kardos, C. Papadopoulos and Z. Trócsányi, Top quark pair production in association
with a jet with NLO parton showering, Phys. Lett. B 705 (2011) 76 [arXiv:1101.2672]
[INSPIRE].
[366] M.R. Whalley, D. Bourilkov and R.C. Group, The Les Houches accord PDFs (LHAPDF)
and LHAGLUE, hep-ph/0508110 [INSPIRE].
[367] M. Cacciari, S. Frixione, M.L. Mangano, P. Nason and G. Ridolfi, Updated predictions for
the total production cross sections of top and of heavier quark pairs at the Tevatron and at
the LHC, JHEP 09 (2008) 127 [arXiv:0804.2800] [INSPIRE].
[368] R.D. Ball et al., A first unbiased global NLO determination of parton distributions and their
uncertainties, Nucl. Phys. B 838 (2010) 136 [arXiv:1002.4407] [INSPIRE].
[369] D.E. Soper and M. Spannowsky, Finding top quarks with shower deconstruction,
Phys. Rev. D 87 (2013) 054012 [arXiv:1211.3140] [INSPIRE].

– 154 –

JHEP07(2014)079

[356] A. Denner, Techniques for calculation of electroweak radiative corrections at the one loop
level and results for W physics at LEP-200, Fortsch. Phys. 41 (1993) 307
[arXiv:0709.1075] [INSPIRE].

## PDF page 157

[370] D.E. Soper and M. Spannowsky, Finding physics signals with event deconstruction,
arXiv:1402.1189 [INSPIRE].
[371] A. van Hameren, OneLOop: for the evaluation of one-loop scalar functions,
Comput. Phys. Commun. 182 (2011) 2427 [arXiv:1007.4716] [INSPIRE].
[372] R.K. Ellis and G. Zanderighi, Scalar one-loop integrals for QCD, JHEP 02 (2008) 002
[arXiv:0712.1851] [INSPIRE].
[373] A. Denner and S. Dittmaier, Reduction schemes for one-loop tensor integrals,
Nucl. Phys. B 734 (2006) 62 [hep-ph/0509141] [INSPIRE].

[375] G. Duplancic and B. Nizic, Reduction method for dimensionally regulated one loop N point
Feynman integrals, Eur. Phys. J. C 35 (2004) 105 [hep-ph/0303184] [INSPIRE].
[376] M. Cacciari, G.P. Salam and G. Soyez, FastJet user manual,
Eur. Phys. J. C 72 (2012) 1896 [arXiv:1111.6097] [INSPIRE].
[377] R. Kleiss, W.J. Stirling and S.D. Ellis, A new Monte Carlo treatment of multiparticle phase
space at high-energies, Comput. Phys. Commun. 40 (1986) 359 [INSPIRE].
[378] L. Garren and P. Lebrun, StdHEP v5 manual, http://cepa.fnal.gov/psm/stdhep/.
[379] G.P. Lepage, A new algorithm for adaptive multidimensional integration,
J. Comput. Phys. 27 (1978) 192 [INSPIRE].
[380] G.P. Lepage, VEGAS: an adaptive multidimentional integration program, CLNS-80/447,
(1980) [INSPIRE].

– 155 –

JHEP07(2014)079

[374] O.V. Tarasov, Connection between Feynman integrals having different values of the
space-time dimension, Phys. Rev. D 54 (1996) 6479 [hep-th/9606018] [INSPIRE].
