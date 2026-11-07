Source: https://link.springer.com/content/pdf/10.12942/lrr-2014-2.pdf
PDF sha256: 62362a29389997d4b2d7e90f54a12c5daa9c33cd71a3c4fb5da396d4b41278fb
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of a_2014_gravitational_radiation_post_newtonian_sources.pdf

Transcription of `a_2014_gravitational_radiation_post_newtonian_sources.pdf` in this directory, 187 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 6 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-5, 7-187 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

,)6).'

Living Rev. Relativity, 17, (2014), 2
DOI 10.12942/lrr-2014-2

2% 6)% 73

IN RELATIVITY

Gravitational Radiation from Post-Newtonian Sources
and Inspiralling Compact Binaries
Luc Blanchet
Institut d’Astrophysique de Paris
98bis Boulevard Arago
75014 Paris, France
email: blanchet@iap.fr
http://www2.iap.fr/users/blanchet

Accepted: 27 January 2014
Published: 13 February 2014
Revised: 16 February 2016
(Update of lrr-2006-4)

Abstract
To be observed and analyzed by the network of gravitational wave detectors on ground
(LIGO, VIRGO, etc.) and by the future detectors in space (eLISA, etc.), inspiralling compact
binaries – binary star systems composed of neutron stars and/or black holes in their late
stage of evolution – require high-accuracy templates predicted by general relativity theory.
The gravitational waves emitted by these very relativistic systems can be accurately modelled
using a high-order post-Newtonian gravitational wave generation formalism. In this article, we
present the current state of the art on post-Newtonian methods as applied to the dynamics and
gravitational radiation of general matter sources (including the radiation reaction back onto
the source) and inspiralling compact binaries. We describe the post-Newtonian equations
of motion of compact binaries and the associated Lagrangian and Hamiltonian formalisms,
paying attention to the self-field regularizations at work in the calculations. Several notions
of innermost circular orbits are discussed. We estimate the accuracy of the post-Newtonian
approximation and make a comparison with numerical computations of the gravitational selfforce for compact binaries in the small mass ratio limit. The gravitational waveform and
energy flux are obtained to high post-Newtonian order and the binary’s orbital phase evolution
is deduced from an energy balance argument. Some landmark results are given in the case of
eccentric compact binaries – moving on quasi-elliptical orbits with non-negligible eccentricity.
The spins of the two black holes play an important role in the definition of the gravitational
wave templates. We investigate their imprint on the equations of motion and gravitational
wave phasing up to high post-Newtonian order (restricting to spin-orbit effects which are linear
in spins), and analyze the post-Newtonian spin precession equations as well as the induced
precession of the orbital plane.

Keywords: Gravitational radiation, Post-Newtonian approximations, Multipolar expansion,
Inspiralling compact binary

c
○ The Author(s). This article is distributed under a
Creative Commons Attribution 4.0 International License.
http://creativecommons.org/licenses/by/4.0/

## PDF page 2

Imprint / Terms of Use
Living Reviews in Relativity is a peer-reviewed open access journal published by the Springer
International Publishing AG, Gewerbestrasse 11, 6330 Cham, Switzerland. ISSN 1433-8351.
This article is distributed under the terms of the Creative Commons Attribution 4.0 International
License (http://creativecommons.org/licenses/by/4.0/), which permits unrestricted use, distribution, and reproduction in any medium, provided you give appropriate credit to the original
author(s) and the source, provide a link to the Creative Commons license, and indicate if changes
were made. Figures that have been previously published elsewhere may not be reproduced without
consent of the original copyright holders.

Luc Blanchet,
“Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries”,
Living Rev. Relativity, 17, (2014), 2.
DOI 10.12942/lrr-2014-2.

## PDF page 3

Article Revisions
Living Reviews supports two ways of keeping its articles up-to-date:
Fast-track revision. A fast-track revision provides the author with the opportunity to add short
notices of current research results, trends and developments, or important publications to
the article. A fast-track revision is refereed by the responsible subject editor. If an article
has undergone a fast-track revision, a summary of changes will be listed here.
Major update. A major update will include substantial changes and additions and is subject to
full external refereeing. It is published with a new publication number.
For detailed documentation of an article’s evolution, please refer to the history document of the
article’s online version at http://dx.doi.org/10.12942/lrr-2014-2.

13 February 2014: Major revision, updated and expanded. About 180 new references. Improved introduction with added Section 1.2 on quadrupole formalism; More extensive description
of asymptotic waveform and relation between radiative and source moments (Section 3.3); More
complete discussion on radiation reaction effects (5.2) and explicit radiation reaction potentials
(5.4); New Section 7.5 on the PN metric in the near zone; New sections on conservative dynamics:
stability of orbits (8.2), first law of binary dynamics (8.3), comparison with self-force computations
(8.4); New Section 9.5 on spherical-harmonic modes of gravitational waves; New sections on eccentric binaries: structure of the motion (10.1), quasi-Keplerian representation (10.2), averaged fluxes
(10.3); New sections on spin effects: Lagrangian formalism (11.1), equations of motion (11.2),
spin-orbit terms in the phase (11.3).
15 January 2016: Minor update. Added 13 new references. More accurate quotations on spins.
Minor improvements in wording. Added new PN subdominant gravitational-wave modes and SF
comparisons.
16 February 2016: Minor update. Added 12 new references. Added a discussion on 4PN
equations of motion.

## PDF page 4

Contents
1 Introduction
1.1 Analytic approximations and wave generation formalism . . . . . . . . . . . . . . .
1.2 The quadrupole moment formalism . . . . . . . . . . . . . . . . . . . . . . . . . . .
1.3 Problem posed by compact binary systems . . . . . . . . . . . . . . . . . . . . . . .
1.4 Post-Newtonian equations of motion . . . . . . . . . . . . . . . . . . . . . . . . . .
1.5 Post-Newtonian gravitational radiation . . . . . . . . . . . . . . . . . . . . . . . . .

7
8
12
14
17
20

Part A: Post-Newtonian Sources

23

2 Non-linear Iteration of the Vacuum Field Equations
2.1 Einstein’s field equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.2 Linearized vacuum equations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.3 The multipolar post-Minkowskian solution . . . . . . . . . . . . . . . . . . . . . . .
2.4 Generality of the MPM solution . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.5 Near-zone and far-zone structures . . . . . . . . . . . . . . . . . . . . . . . . . . . .

23
23
25
28
31
33

3 Asymptotic Gravitational Waveform
3.1 The radiative multipole moments . . . . . . . . . . . . . . . . . . . . . . . . . . . .
3.2 Gravitational-wave tails and tails-of-tails . . . . . . . . . . . . . . . . . . . . . . . .
3.3 Radiative versus source moments . . . . . . . . . . . . . . . . . . . . . . . . . . . .

35
35
37
42

4 Matching to a Post-Newtonian Source
4.1 The matching equation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
4.2 General expression of the multipole expansion . . . . . . . . . . . . . . . . . . . . .
4.3 Equivalence with the Will–Wiseman formalism . . . . . . . . . . . . . . . . . . . .
4.4 The source multipole moments . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

46
46
48
50
51

5 Interior Field of a Post-Newtonian Source
5.1 Post-Newtonian iteration in the near zone . . . . . . . . . . . . . . . . . . . . . . .
5.2 Post-Newtonian metric and radiation reaction effects . . . . . . . . . . . . . . . . .
5.3 The 3.5PN metric for general matter systems . . . . . . . . . . . . . . . . . . . . .
5.4 Radiation reaction potentials to 4PN order . . . . . . . . . . . . . . . . . . . . . .

53
55
57
59
62

Part B: Compact Binary Systems

65

6 Regularization of the Field of Point Particles
6.1 Hadamard self-field regularization . . . . . . . . . . . . . . . . . . . . . . . . . . . .
6.2 Hadamard regularization ambiguities . . . . . . . . . . . . . . . . . . . . . . . . . .
6.3 Dimensional regularization of the equations of motion . . . . . . . . . . . . . . . .
6.4 Dimensional regularization of the radiation field . . . . . . . . . . . . . . . . . . . .

65
66
68
72
76

7 Newtonian-like Equations of Motion
7.1 The 3PN acceleration and energy for particles . . . . . . . . . . . . . . . . . . . . .
7.2 Lagrangian and Hamiltonian formulations . . . . . . . . . . . . . . . . . . . . . . .
7.3 Equations of motion in the center-of-mass frame . . . . . . . . . . . . . . . . . . .
7.4 Equations of motion and energy for quasi-circular orbits . . . . . . . . . . . . . . .
7.5 The 2.5PN metric in the near zone . . . . . . . . . . . . . . . . . . . . . . . . . . .

78
78
84
90
94
97

## PDF page 5

8 Conservative Dynamics of Compact Binaries
8.1 Concept of innermost circular orbit . . . . . . . . . . . . . . . . . . . . . . . . . . .
8.2 Dynamical stability of circular orbits . . . . . . . . . . . . . . . . . . . . . . . . . .
8.3 The first law of binary point-particle mechanics . . . . . . . . . . . . . . . . . . . .
8.4 Post-Newtonian approximation versus gravitational self-force . . . . . . . . . . . .

101
101
103
108
112

9 Gravitational Waves from Compact Binaries
9.1 The binary’s multipole moments . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.2 Gravitational wave energy flux . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.3 Orbital phase evolution . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.4 Polarization waveforms for data analysis . . . . . . . . . . . . . . . . . . . . . . . .
9.5 Spherical harmonic modes for numerical relativity . . . . . . . . . . . . . . . . . .

116
117
120
123
125
131

10 Eccentric Compact Binaries
10.1 Doubly periodic structure of the motion of eccentric binaries . . . . . . . . . . . .
10.2 Quasi-Keplerian representation of the motion . . . . . . . . . . . . . . . . . . . . .
10.3 Averaged energy and angular momentum fluxes . . . . . . . . . . . . . . . . . . . .

135
135
137
140

11 Spinning Compact Binaries
11.1 Lagrangian formalism for spinning point particles . . . . . . . . . . . . . . . . . . .
11.2 Equations of motion and precession for spin-orbit effects . . . . . . . . . . . . . . .
11.3 Spin-orbit effects in the gravitational wave flux and orbital phase . . . . . . . . . .

146
148
152
157

References

161

List of Tables
1
2
3

4

Numerically determined value of the 3PN coefficient for the SF part of the redshift
observable defined by Eq. (292). . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Numerically determined values of higher-order PN coefficients for the SF part of the
redshift observable defined by Eq. (292). . . . . . . . . . . . . . . . . . . . . . . . .
Post-Newtonian contributions to the accumulated number of gravitational-wave cycles 𝒩cycle for compact binaries detectable in the bandwidth of LIGO-VIRGO detectors. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
Spin-orbit contributions to the number of gravitational-wave cycles 𝒩cycle for binaries detectable by ground-based detectors LIGO-VIRGO. . . . . . . . . . . . . . .

115
115

125
159

## PDF page 6



## PDF page 7

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

1

7

Introduction

The theory of gravitational radiation from isolated sources, in the context of general relativity, is a
fascinating science that can be explored by means of what was referred to in the XVIIIth century
France as l’analyse sublime: The analytical (i.e., mathematical) method, and more specifically the
resolution of partial differential equations. Indeed, the field equations of general relativity, when use
is made of the harmonic-coordinate conditions, take the form of a quasi-linear hyperbolic differential
system of equations, involving the famous wave operator or d’Alembertian [140]. The resolution
of that system of equations constitutes a problème bien posé in the sense of Hadamard [236, 104],
and which is amenable to an analytic solution using approximation methods.
Nowadays, the importance of the field lies in the exciting comparison of the theory with contemporary astrophysical observations, of binary pulsars like the historical Hulse–Taylor pulsar
PSR 1913+16 [250], and, in a forthcoming future, of gravitational waves produced by massive and
rapidly evolving systems such as inspiralling compact binaries. These should be routinely detected
on Earth by the network of large-scale laser interferometers, including the advanced versions of
the ground-based interferometers LIGO and VIRGO, with also GEO and the future cryogenic
detector KAGRA. The first direct detection of a coalescence of two black holes has been achieved
on September 14, 2015 by the advanced LIGO detector [1]. Further ahead, the space-based laser
interferometer LISA (actually, the evolved version eLISA) should be able to detect supermassive
black-hole binaries at cosmological distances.
To prepare these experiments, the required theoretical work consists of carrying out a sufficiently
general solution of the Einstein field equations, valid for a large class of matter systems, and
describing the physical processes of the emission and propagation of the gravitational waves from
the source to the distant detector, as well as their back-reaction onto the source. The solution
should then be applied to specific sources like inspiralling compact binaries.
For general sources it is hopeless to solve the problem via a rigorous deduction within the
exact theory of general relativity, and we have to resort to approximation methods. Of course the
ultimate aim of approximation methods is to extract from the theory some firm predictions to be
compared with the outcome of experiments. However, we have to keep in mind that such methods
are often missing a clear theoretical framework and are sometimes not related in a very precise
mathematical way to the first principles of the theory.
The flagship of approximation methods is the post-Newtonian approximation, which has been
developed from the early days of general relativity [303]. This approximation is at the origin of
many of the great successes of general relativity, and it gives wonderful answers to the problems of
motion and gravitational radiation of systems of compact objects. Three crucial applications are:
1. The motion of N point-like objects at the first post-Newtonian approximation level [184], is
taken into account to describe the solar system dynamics (motion of the centers of mass of
planets);
2. The gravitational radiation-reaction force, which appears in the equations of motion at the
second-and-a-half post-Newtonian (2.5PN) order [148, 147, 143, 142], has been experimentally
verified by the observation of the secular acceleration of the orbital motion of the Hulse–Taylor
binary pulsar PSR 1913+16 [399, 400, 398];
3. The analysis of gravitational waves emitted by inspiralling compact binaries – two neutron
stars or black holes driven into coalescence by emission of gravitational radiation – necessitates the prior knowledge of the equations of motion and radiation field up to very high
post-Newtonian order.
This article reviews the current status of the post-Newtonian approach to the problems of the
motion of inspiralling compact binaries and their emission of gravitational waves. When the

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 8

8

Luc Blanchet

two compact objects approach each other toward merger, the post-Newtonian expansion will lose
accuracy and should be taken over by numerical-relativity computations [359, 116, 21]. We shall
refer to other review articles like Refs. [233, 187] for discussions of numerical-relativity methods.
Despite very intensive developments of numerical relativity, the post-Newtonian approximation
remains indispensable for describing the inspiral phase of compact binaries to high accuracy, and
for providing a powerful benchmark against which the numerical computations are tested.
Part A of the article deals with general post-Newtonian matter sources. The exterior field of
the source is investigated by means of a combination of analytic post-Minkowskian and multipolar
approximations. The physical observables in the far-zone of the source are described by a specific
set of radiative multipole moments. By matching the exterior solution to the metric of the postNewtonian source in the near-zone the explicit expressions of the source multipole moments are
obtained. The relationships between the radiative and source moments involve many non-linear
multipole interactions, among them those associated with the tails (and tails-of-tails, etc.) of
gravitational waves.
Part B is devoted to the application to compact binary systems, with particular emphasis on
black hole binaries with spins. We present the equations of binary motion, and the associated
Lagrangian and Hamiltonian, at the third post-Newtonian (3PN) order beyond the Newtonian
acceleration. The gravitational-wave energy flux, taking consistently into account the relativistic
corrections in the binary’s moments as well as the various tail effects, is derived through 3.5PN
order with respect to the quadrupole formalism. The binary’s orbital phase, whose prior knowledge
is crucial for searching and analyzing the signals from inspiralling compact binaries, is deduced
from an energy balance argument (in the simple case of circular orbits).
All over the article we try to state the main results in a form that is simple enough to be
understood without the full details; however, we also outline some of the proofs when they present
some interest on their own. To emphasize the importance of some key results, we present them in
the form of mathematical theorems. In applications we generally show the most up-to-date results
up to the highest known post-Newtonian order.1

1.1

Analytic approximations and wave generation formalism

The basic problem we face is to relate the asymptotic gravitational-wave form ℎ𝑖𝑗 generated by
some isolated source, at the location of a detector in the wave zone of the source, to the material
content of the source, i.e., its stress-energy tensor 𝑇 𝛼𝛽 , using approximation methods in general
relativity.2 Therefore, a general wave-generation formalism must solve the field equations, and
the non-linearity therein, by imposing some suitable approximation series in one or several small
physical parameters. Some important approximations that we shall use in this article are the postNewtonian method (or non-linear 1/𝑐-expansion), the post-Minkowskian method or non-linear
iteration (𝐺-expansion), the multipole decomposition in irreducible representations of the rotation
group (or equivalently 𝑎-expansion in the source radius), the far-zone expansion (1/𝑅-expansion
in the distance to the source), and the perturbation in the small mass limit (𝜈-expansion in the
mass ratio of a binary system). In particular, the post-Newtonian expansion has provided us in
the past with our best insights into the problems of motion and radiation. The most successful
wave-generation formalisms make a gourmet cocktail of these approximation methods. For reviews
on analytic approximations and applications to the motion and the gravitational wave-generation
1 A few errata have been published in this intricate field; all formulas take into account the latest changes.
2 In this article Greek indices 𝛼𝛽 . . . 𝜇𝜈 . . . take space-time values 0, 1, 2, 3 and Latin indices 𝑎𝑏 . . . 𝑖𝑗 . . .
spatial values 1, 2, 3. Cartesian coordinates are assumed throughout and boldface notation is often used for
ordinary Euclidean vectors. In Section 11 upper Latin letters 𝐴𝐵 . . . will refer to tetrad indices 0, 1, 2, 3 with
𝑎𝑏 . . . the corresponding spatial values 1, 2, 3. Our signature is +2; hence the Minkowski metric reads 𝜂𝛼𝛽 =
diag(−1, +1, +1, +1) = 𝜂𝐴𝐵 . As usual 𝐺 and 𝑐 are Newton’s constant and the speed of light.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 9

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

9

see Refs. [404, 142, 144, 145, 405, 421, 46, 52, 378]. For reviews on black-hole pertubations and
the self-force approach see Refs. [348, 373, 177, 23].
The post-Newtonian approximation is valid under the assumptions of a weak gravitational field
inside the source (we shall see later how to model neutron stars and black holes), and of slow
internal motions.3 The main problem with this approximation, is its domain of validity, which is
limited to the near zone of the source – the region surrounding the source that is of small extent
with respect to the wavelength of the gravitational waves. A serious consequence is the a priori
inability of the post-Newtonian expansion to incorporate the boundary conditions at infinity, which
determine the radiation reaction force in the source’s local equations of motion.
The post-Minkowskian expansion, by contrast, is uniformly valid, as soon as the source is
weakly self-gravitating, over all space-time. In a sense, the post-Minkowskian method is more
fundamental than the post-Newtonian one; it can be regarded as an “upstream” approximation
with respect to the post-Newtonian expansion, because each coefficient of the post-Minkowskian
series can in turn be re-expanded in a post-Newtonian fashion. Therefore, a way to take into
account the boundary conditions at infinity in the post-Newtonian series is to control first the
post-Minkowskian expansion. Notice that the post-Minkowskian method is also upstream (in the
previous sense) with respect to the multipole expansion, when considered outside the source, and
with respect to the far-zone expansion, when considered far from the source.
The most “downstream” approximation that we shall use in this article is the post-Newtonian
one; therefore this is the approximation that dictates the allowed physical properties of our matter
source. We assume mainly that the source is at once slowly moving and weakly stressed, and
we abbreviate this by saying that the source is post-Newtonian. For post-Newtonian sources, the
parameter defined from the components of the matter stress-energy tensor 𝑇 𝛼𝛽 and the source’s
Newtonian potential 𝑈 by
{︃⃒
⃒ ⃒ }︃
⃒ ⃒
⃒
⃒ 𝑇 0𝑖 ⃒ ⃒ 𝑇 𝑖𝑗 ⃒1/2 ⃒ 𝑈 ⃒1/2
⃒
⃒
⃒
⃒
,
(1)
𝜖 ≡ max ⃒ 00 ⃒ , ⃒ 00 ⃒ , ⃒⃒ 2 ⃒⃒
𝑇
𝑇
𝑐
is much less than one. This parameter represents essentially a slow motion estimate 𝜖 ∼ 𝑣/𝑐,
where 𝑣 denotes a typical internal velocity. By a slight abuse of notation, following Chandrasekhar
et al. [122, 124, 123], we shall henceforth write formally 𝜖 ≡ 1/𝑐, even though 𝜖 is dimensionless whereas 𝑐 has the dimension of a velocity. Thus, 1/𝑐 ≪ 1 in the case of post-Newtonian
sources. The small post-Newtonian remainders will be denoted 𝒪(1/𝑐𝑛 ). Furthermore, still following Refs. [122, 124, 123], we shall refer to a small post-Newtonian term with formal order 𝒪(1/𝑐𝑛 )
relative to the Newtonian acceleration in the equations of motion, as 𝑛2 PN.
We have |𝑈/𝑐2 |1/2 ≪ 1/𝑐 for sources with negligible self-gravity, and whose dynamics are
therefore driven by non-gravitational forces. However, we shall generally assume that the source is
self-gravitating; in that case we see that it is necessarily weakly (but not negligibly) self-gravitating,
i.e., |𝑈/𝑐2 |1/2 = 𝒪(1/𝑐).4 Note that the adjective “slow-motion” is a bit clumsy because we shall
in fact consider very relativistic sources such as inspiralling compact binaries, for which 𝑣/𝑐 can
be as large as 50% in the last rotations, and whose description necessitates the control of high
post-Newtonian approximations.
At the lowest-order in the Newtonian limit 1/𝑐 → 0, the gravitational waveform of a postNewtonian matter source is generated by the time variations of the quadrupole moment of the
source. We shall review in Section 1.2 the utterly important “Newtonian” quadrupole moment
formalism [183, 285]. Taking into account higher post-Newtonian corrections in a wave generation
3 Establishing the post-Newtonian expansion rigorously has been the subject of numerous mathematically oriented works, see e.g., [361, 362, 363].
4 Note that for very eccentric binaries (with say 𝑒 → 1− ) the Newtonian potential 𝑈 can be numerically much
larger than the estimate 𝒪(1/𝑐2 ) ∼ 𝑣 2 /𝑐2 at the apastron of the orbit.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 10

10

Luc Blanchet

formalism will mean including into the waveform the contributions of higher multipole moments,
beyond the quadrupole. Post-Newtonian corrections of order 𝒪(1/𝑐𝑛 ) beyond the quadrupole
formalism will still be denoted as 𝑛2 PN. Building a post-Newtonian wave generation formalism
must be concomitant to understanding the multipole expansion in general relativity.
The multipole expansion is one of the most useful tools of physics, but its use in general relativity is difficult because of the non-linearity of the theory and the tensorial character of the
gravitational interaction. In the stationary case, the multipole moments are determined by the
expansion of the metric at spatial infinity [219, 238, 384], while, in the case of non-stationary fields,
the moments, starting with the quadrupole, are defined at future null infinity. The multipole moments have been extensively studied in the linearized theory, which ignores the gravitational forces
inside the source. Early studies have extended the Einstein quadrupole formula [given by Eq. (4)
below] to include the current-quadrupole and mass-octupole moments [332, 333], and obtained the
corresponding formulas for linear momentum [332, 333, 30, 358] and angular momentum [339, 134].
The general structure of the infinite multipole series in the linearized theory was investigated by
several works [369, 367, 343, 403], from which it emerged that the expansion is characterized by
two and only two sets of moments: Mass-type and current-type moments. Below we shall use a
particular multipole decomposition of the linearized (vacuum) metric, parametrized by symmetric
and trace-free (STF) mass and current moments, as given by Thorne [403]. The expressions of the
multipole moments as integrals over the source, valid in the linearized theory but irrespective of
a slow motion hypothesis, have been worked out in [309, 119, 118, 154]. In particular, Damour
& Iyer [154] obtained the complete closed-form expressions for the time-dependent mass and spin
multipole moments (in STF guise) of linearized gravity.
In the full non-linear theory, the (radiative) multipole moments can be read off the coefficient
of 1/𝑅 in the expansion of the metric when 𝑅 → +∞, with a null coordinate 𝑇 − 𝑅/𝑐 = const. The
solutions of the field equations in the form of a far-field expansion (power series in 1/𝑅) have been
constructed, and their properties elucidated, by Bondi et al. [93] and Sachs [368]. The precise way
under which such radiative space-times fall off asymptotically has been formulated geometrically
by Penrose [337, 338] in the concept of an asymptotically simple space-time (see also Ref. [220]).
The resulting Bondi–Sachs–Penrose approach is very powerful, but it can answer a priori only a
part of the problem, because it gives information on the field only in the limit where 𝑅 → +∞,
which cannot be connected in a direct way to the actual matter content and dynamics of the source.
In particular the multipole moments that one considers in this approach are those measured at
infinity – we call them the radiative multipole moments. These moments are distinct, because of
non-linearities, from some more natural source multipole moments, which are defined operationally
by means of explicit integrals extending over the matter and gravitational fields.
An alternative way of defining the multipole expansion within the complete non-linear theory is
that of Blanchet & Damour [57, 41], following pioneering works by Bonnor and collaborators [94,
95, 96, 251] and Thorne [403]. In this approach the basic multipole moments are the source
moments, rather than the radiative ones. In a first stage, the moments are left unspecified, as
being some arbitrary functions of time, supposed to describe an actual physical source. They are
iterated by means of a post-Minkowskian expansion of the vacuum field equations (valid in the
source’s exterior). Technically, the post-Minkowskian approximation scheme is greatly simplified
by the assumption of a multipolar expansion, as one can consider separately the iteration of the
different multipole pieces composing the exterior field.5 In this “multipolar-post-Minkowskian”
(MPM) formalism, which is physically valid over the entire weak-field region outside the source,
and in particular in the wave zone (up to future null infinity), the radiative multipole moments are
obtained in the form of some non-linear functionals of the more basic source moments. A priori,
the method is not limited to post-Newtonian sources; however, we shall see that, in the current
5 Whereas, the direct attack of the post-Minkowskian expansion, valid at once inside and outside the source,
faces some calculational difficulties [408, 136].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 11

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

11

situation, the closed-form expressions of the source multipole moments can be established only in
the case where the source is post-Newtonian [44, 49]. The reason is that in this case the domain of
validity of the post-Newtonian iteration (viz. the near zone) overlaps the exterior weak-field region,
so that there exists an intermediate zone in which the post-Newtonian and multipolar expansions
can be matched together. This is a standard application of the method of matched asymptotic
expansions in general relativity [114, 113, 7, 357].
To be more precise, we shall show how a systematic multipolar and post-Minkowskian iteration scheme for the vacuum Einstein field equations yields the most general physically admissible
solution of these equations [57]. The solution is specified once we give two and only two sets of
time-varying (source) multipole moments. Some general theorems about the near-zone and farzone expansions of that general solution will be stated. Notably, we show [41] that the asymptotic
behaviour of the solution at future null infinity is in agreement with the findings of the Bondi–
Sachs–Penrose [93, 368, 337, 338, 220] approach to gravitational radiation. However, checking
that the asymptotic structure of the radiative field is correct is not sufficient by itself, because the
ultimate aim, as we said, is to relate the far field to the properties of the source, and we are now
obliged to ask: What are the multipole moments corresponding to a given stress-energy tensor
𝑇 𝛼𝛽 describing the source? The general expression of the moments was obtained at the level of
the second post-Newtonian (2PN) order in Ref. [44], and was subsequently proved to be in fact
valid up to any post-Newtonian order in Ref. [49]. The source moments are given by some integrals
extending over the post-Newtonian expansion of the total (pseudo) stress-energy tensor 𝜏 𝛼𝛽 , which
is made of a matter part described by 𝑇 𝛼𝛽 and a crucial non-linear gravitational source term Λ𝛼𝛽 .
These moments carry in front a particular operation of taking the finite part (ℱ𝒫 as we call it
below), which makes them mathematically well-defined despite the fact that the gravitational part
Λ𝛼𝛽 has a spatially infinite support, which would have made the bound of the integral at spatial
infinity singular (of course the finite part is not added a posteriori to restore the well-definiteness
of the integral, but is proved to be actually present in this formalism). The expressions of the
moments had been obtained earlier at the 1PN level, albeit in different forms, in Ref. [59] for the
mass-type moments [see Eq. (157a) below], and in Ref. [155] for the current-type ones.
The wave-generation formalism resulting from matching the exterior multipolar and postMinkowskian field [57, 41] to the post-Newtonian source [44, 49] is able to take into account,
in principle, any post-Newtonian correction to both the source and radiative multipole moments
(for any multipolarity of the moments). The relationships between the radiative and source moments include many non-linear multipole interactions, because the source moments mix with each
other as they “propagate” from the source to the detector. Such multipole interactions include
the famous effects of wave tails, corresponding to the coupling between the non-static moments
with the total mass M of the source. The non-linear multipole interactions have been computed
within the present wave-generation formalism up to the 3.5PN order in Refs. [60, 50, 48, 74, 197].
Furthermore, the back-reaction of the gravitational-wave emission onto the source, up to the 1.5PN
order relative to the leading order of radiation reaction, has also been studied within this formalism [58, 43, 47]. Now, recall that the leading radiation reaction force, which is quadrupolar, occurs
already at the 2.5PN order in the source’s equations of motion. Therefore the 1.5PN “relative”
order in the radiation reaction corresponds in fact to the 4PN order in the equations of motion,
beyond the Newtonian acceleration. It has been shown that the gravitational-wave tails enter the
radiation reaction at precisely the 1.5PN relative order, i.e., 4PN absolute order [58]. A systematic
post-Newtonian iteration scheme for the near-zone field, formally taking into account all radiation
reaction effects, has been obtained, fully consistent with the present formalism [357, 75].
A different wave-generation formalism has been devised by Will & Wiseman [424] (see also
Refs. [422, 335, 336]), after earlier attempts by Epstein & Wagoner [185] and Thorne [403]. This
formalism has exactly the same scope as the one of Refs. [57, 41, 44, 49], i.e., it applies to any
isolated post-Newtonian sources, but it differs in the definition of the source multipole moments

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 12

12

Luc Blanchet

and in many technical details when properly implemented [424]. In both formalisms, the moments
are generated by the post-Newtonian expansion of the pseudo-tensor 𝜏 𝛼𝛽 , but in the Will–Wiseman
formalism they are defined by some compact-support integrals terminating at some finite radius
enclosing the source, e.g., the radius ℛ of the near zone. By contrast, in Refs. [44, 49], the moments
are given by some integrals covering the whole space (R3 ) and regularized by means of the finite
part ℱ𝒫. Nevertheless, in both formalisms the source multipole moments, which involve a whole
series of relativistic corrections, must be coupled together in a complicated way in the true nonlinear solution; such non-linear couplings form an integral part of the radiative moments at infinity
and thereby of the observed signal. We shall prove in Section 4.3 the complete equivalence, at the
most general level, between the two formalisms.

1.2

The quadrupole moment formalism

The lowest-order wave generation formalism is the famous quadrupole formalism of Einstein [183]
and Landau & Lifshitz [285]. This formalism applies to a general isolated matter source which
is post-Newtonian in the sense of existence of the small post-Newtonian parameter 𝜖 defined by
Eq. (1). However, the quadrupole formalism is valid in the Newtonian limit 𝜖 → 0; it can rightly
be qualified as “Newtonian” because the quadrupole moment of the matter source is Newtonian
and its evolution obeys Newton’s laws of gravity. In this formalism the gravitational field ℎTT
𝑖𝑗 is
expressed in a transverse and traceless (TT) coordinate system covering the far zone of the source
at retarded times,6 as
{︂ 2
(︂ )︂}︂
(︂ )︂
d Q𝑎𝑏
1
1
2𝐺
𝒫
(𝑁
)
(𝑇
−
𝑅/𝑐)
+
𝒪
+
𝒪
,
(2)
ℎTT
=
𝑖𝑗𝑎𝑏
𝑖𝑗
4
2
𝑐 𝑅
d𝑇
𝑐
𝑅2
where 𝑅 = |𝑋| is the distance to the source, 𝑇 − 𝑅/𝑐 is the retarded time, 𝑁 = 𝑋/𝑅 is the
unit direction from the source to the far away observer, and 𝒫𝑖𝑗𝑎𝑏 = 𝒫𝑖𝑎 𝒫𝑗𝑏 − 12 𝒫𝑖𝑗 𝒫𝑎𝑏 is the TT
projection operator, with 𝒫𝑖𝑗 = 𝛿𝑖𝑗 − 𝑁𝑖 𝑁𝑗 being the projector onto the plane orthogonal to 𝑁 .
The source’s quadrupole moment takes the familiar Newtonian form
(︂
)︂
∫︁
1
Q𝑖𝑗 (𝑡) =
d3 x 𝜌(x, 𝑡) 𝑥𝑖 𝑥𝑗 − 𝛿𝑖𝑗 x2 ,
(3)
3
source
where 𝜌 is the Newtonian mass density. The total gravitational power emitted by the source in all
directions around the source is given by the Einstein quadrupole formula
(︂
ℱ≡

d𝐸
d𝑇

)︂GW
{︂
(︂ )︂}︂
𝐺 1 d3 Q𝑎𝑏 d3 Q𝑎𝑏
1
= 5
+
𝒪
.
3
3
𝑐
5 d𝑇
d𝑇
𝑐2

(4)

Our notation ℱ stands for the total gravitational energy flux or gravitational “luminosity” of the
source. Similarly, the total angular momentum flux is given by
(︂
𝒢𝑖 ≡

dJ𝑖
d𝑇

)︂GW
{︂
(︂ )︂}︂
𝐺 2
d2 Q𝑎𝑐 d3 Q𝑏𝑐
1
= 5
𝜖𝑖𝑎𝑏
+𝒪 2
,
𝑐
5
d𝑇 2 d𝑇 3
𝑐

(5)

where 𝜖𝑎𝑏𝑐 denotes the standard Levi-Civita symbol with 𝜖123 = 1.
Associated with the latter energy and angular momentum fluxes, there is also a quadrupole
formula for the radiation reaction force, which reacts on the source’s dynamics in consequence of
the emission of waves. This force will inflect the time evolution of the orbital phase of the binary
6 The TT coordinate system can be extended to the near zone of the source as well; see for instance Ref. [282].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 13

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

13

pulsar and inspiralling compact binaries. At the position (x, 𝑡) in a particular coordinate system
covering the source, the reaction force density can be written as [114, 113, 319]
{︂
(︂ )︂}︂
𝐺
2 d5 Q𝑖𝑎
1
𝐹𝑖reac = 5 𝜌 − 𝑥𝑎
+
𝒪
.
(6)
𝑐
5
d𝑡5
𝑐2
This is the gravitational analogue of the damping force of electromagnetism. However, notice
that gravitational radiation reaction is inherently gauge-dependent, so the expression of the force
depends on the coordinate system which is used. Consider now the energy and angular momentum
of a matter system made of some perfect fluid, say
[︂ 2
]︂
(︂ )︂
∫︁
v
𝑈
1
3
𝐸 = d x𝜌
(7a)
+Π−
+𝒪 2 ,
2
2
𝑐
)︂
(︂
∫︁
1
J𝑖 = d3 x 𝜌 𝜖𝑖𝑎𝑏 𝑥𝑎 𝑣𝑏 + 𝒪 2 .
(7b)
𝑐
The specific internal energy of the fluid is denoted Π, and obeys the usual thermodynamic relation
dΠ = −𝑃 d(1/𝜌) where 𝑃 is the pressure; the gravitational potential obeys the Poisson equation
Δ𝑈 = −4𝜋𝐺𝜌. We compute the mechanical losses of energy and angular momentum from the
time derivatives of 𝐸 and J𝑖 . We employ the usual Eulerian equation of motion 𝜌 d𝑣 𝑖 /d𝑡 = −𝜕𝑖 𝑃 +
𝜌𝜕𝑖 𝑈 + 𝐹𝑖reac and continuity equation 𝜕𝑡 𝜌 + 𝜕𝑖 (𝜌 𝑣 𝑖 ) = 0. Note that we add the small dissipative
radiation-reaction contribution 𝐹𝑖reac in the equation of motion but neglect all conservative postNewtonian corrections. The result is
∫︁
d𝐸
d𝑓
= d3 x 𝑣 𝑖 𝐹𝑖reac = −ℱ +
,
(8a)
d𝑡
d𝑡
∫︁
d𝑔𝑖
dJ𝑖
= d3 x 𝜖𝑖𝑎𝑏 𝑥𝑎 𝐹𝑏reac = −𝒢𝑖 +
,
(8b)
d𝑡
d𝑡
where one recognizes the fluxes at infinity given by Eqs. (4) and (5), and where the second terms
denote some total time derivatives made of quadratic products of derivatives of the quadrupole
moment. Looking only for secular effects, we apply an average over time on a typical period of
variation of the system; the latter time derivatives will be in average numerically small in the case
of quasi-periodic motion (see e.g., [103] for a discussion). Hence we obtain
d𝐸
⟩ = −⟨ℱ⟩ ,
d𝑡
dJ𝑖
⟨
⟩ = −⟨𝒢𝑖 ⟩ ,
d𝑡
⟨

(9a)
(9b)

where the brackets denote the time averaging over an orbit. These balance equations encode the
secular decreases of energy and angular momentum by gravitational radiation emission.
The cardinal virtues of the Einstein–Landau–Lifshitz quadrupole formalism are: Its generality –
the only restrictions are that the source be Newtonian and bounded; its simplicity, as it necessitates
only the computation of the time derivatives of the Newtonian quadrupole moment (using the
Newtonian laws of motion); and, most importantly, its agreement with the observation of the
dynamics of the binary pulsar PSR 1913+16 [399, 400, 398]. Indeed let us apply the balance
equations (9) to a system of two point masses moving on an eccentric orbit modelling the binary
pulsar PSR 1913+16 – the classic references are [340, 339]; see also [186, 415]. We use the binary’s
Newtonian energy and angular momentum,
𝐸=−

𝐺𝑚1 𝑚2
,
2𝑎

(10a)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 14

14

Luc Blanchet

√︃
J = 𝑚1 𝑚2

𝐺𝑎(1 − 𝑒2 )
,
𝑚1 + 𝑚2

(10b)

where 𝑎 and 𝑒 are the semi-major axis and eccentricity of the orbit and 𝑚1 and 𝑚2 are the two
masses. From the energy balance equation (9a) we obtain first the secular evolution of 𝑎; next
changing from 𝑎 to the orbital period 𝑃 using Kepler’s third law,7 we get the secular evolution of
the orbital period 𝑃 as
192𝜋
d𝑃
⟩=− 5
⟨
d𝑡
5𝑐

(︂

2𝜋𝐺
𝑃

)︂5/3

37 4
73 2
𝑒 + 96
𝑒
1 + 24
𝑚1 𝑚2
.
1/3
2
7/2
(𝑚1 + 𝑚2 )
(1 − 𝑒 )

(11)

The last factor, depending on the eccentricity, comes out from the orbital average and is known as
the Peters & Mathews [340] “enhancement” factor, so designated because in the case of the binary
pulsar, which has a rather large eccentricity 𝑒 ≃ 0.617, it enhances the effect by a factor ∼ 12.
Numerically, one finds ⟨d𝑃/d𝑡⟩ = −2.4 × 10−12 , a dimensionless number in excellent agreement
with the observations of the binary pulsar [399, 400, 398]. On the other hand the secular evolution
of the eccentricity 𝑒 is deduced from the angular momentum balance equation (9b) [together with
the previous result (11)], as
608𝜋 𝑒
d𝑒
⟨ ⟩=−
d𝑡
15𝑐5 𝑃

(︂

2𝜋𝐺
𝑃

)︂5/3

121 2
1 + 304
𝑒
𝑚1 𝑚2
.
(𝑚1 + 𝑚2 )1/3 (1 − 𝑒2 )5/2

(12)

Interestingly, the system of equations (11) – (12) can be thoroughly integrated in closed analytic
form. This yields the evolution of the eccentricity [339]:
𝑒2
(1 − 𝑒2 )19/6

)︂145/121
(︂
121 2
𝑒
= 𝑐0 𝑃 19/9 ,
1+
304

(13)

where 𝑐0 denotes an integration constant to be determined by the initial conditions at the start of
the binary evolution. When 𝑒 ≪ 1 the latter relation gives approximately 𝑒2 ≃ 𝑐0 𝑃 19/9 .
For a long while, it was thought that the various quadrupole formulas would be sufficient for
sources of gravitational radiation to be observed directly on Earth – as they had proved to be
amply sufficient in the case of the binary pulsar. However, further works [139]8 and [87, 138]
showed that this is not true, as one has to include post-Newtonian corrections to the quadrupole
formalism in order to prepare for the data analysis of future detectors, in the case of inspiralling
compact binaries. From the beautiful test of the orbital decay (11) of the binary pulsar, we can say
that the post-Newtonian corrections to the “Newtonian” quadrupole formalism – which we shall
compute in this article – have already received a strong observational support.

1.3

Problem posed by compact binary systems

Inspiralling compact binaries, containing neutron stars and/or black holes, are likely to become
the bread-and-butter sources of gravitational waves for the detectors LIGO, VIRGO, GEO and
KAGRA on ground, and also eLISA in space. The two compact objects steadily lose their orbital
binding energy by emission of gravitational radiation; as a result, the orbital separation between
them decreases, and the orbital frequency increases. Thus, the frequency of the gravitational-wave
7 Namely (𝐺𝑚)1 = Ω2 𝑎3 , where 𝑚 = 𝑚 + 𝑚 is the total mass and Ω = 2𝜋/𝑃 is the orbital frequency. This
1
2
law is also appropriately called the 1-2-3 law [319].
8 This work entitled: “The last three minutes: Issues in gravitational-wave measurements of coalescing compact
binaries” is sometimes coined the “3mn Caltech paper”.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 15

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

15

signal, which equals twice the orbital frequency for the dominant harmonics, “chirps” in time (i.e.,
the signal becomes higher and higher pitched) until the two objects collide and merge.
The orbit of most inspiralling compact binaries can be considered to be circular, apart from
the gradual inspiral, because the gravitational radiation reaction forces tend to circularize the
motion rapidly. This effect is due to the emission of angular momentum by gravitational waves,
resulting in a secular decrease of the eccentricity of the orbit, which has been computed within
the quadrupole formalism in Eq. (12). For instance, suppose that the inspiralling compact binary
was long ago (a few hundred million years ago) a system similar to the binary pulsar system, with
an orbital frequency Ω0 ≡ 2𝜋/𝑃0 ∼ 10−4 rad/s and a rather large orbital eccentricity 𝑒0 ∼ 0.6.
When it becomes visible by the detectors on ground, i.e., when the gravitational wave signal
frequency reaches about 𝑓 ≡ Ω/𝜋 ∼ 10 Hz, the eccentricity of the orbit should be 𝑒 ∼ 10−6
according to the formula (13). This is a very small eccentricity, even when compared to high-order
relativistic corrections. Only non-isolated binary systems could have a non negligible eccentricity.
For instance, the Kozai mechanism [283, 300] is one important scenario that produces eccentric
binaries and involves the interaction between a pair of binaries in the dense cores of globular
clusters [315]. If the mutual inclination angle of the inner binary is strongly tilted with respect
to the outer compact star, then a resonance occurs and can increase the eccentricity of the inner
binary to large values. This is one motivation for looking at the waves emitted by inspiralling
binaries in non-circular, quasi-elliptical orbits (see Section 10).
The main point about modelling the inspiralling compact binary is that a model made of two
structureless point particles, characterized solely by two mass parameters 𝑚a and possibly two
spins 𝑆a (with a = 1, 2 labelling the particles), is sufficient in first approximation. Indeed, most
of the non-gravitational effects usually plaguing the dynamics of binary star systems, such as the
effects of a magnetic field, of an interstellar medium, of the internal structure of extended bodies,
are dominated by gravitational effects. The main justification for a model of point particles is that
the effects due to the finite size of the compact bodies are small. Consider for instance the influence
of the Newtonian quadrupole moments Qa induced by tidal interaction between two neutron stars.
Let 𝑎a be the radius of the stars, and 𝑟12 be the distance between the two centers of mass. We
have, for tidal moments,
𝑚1 𝑎5
𝑚2 𝑎5
(14)
Q1 = 𝑘1 3 1 and Q2 = 𝑘2 3 2 ,
𝑟12
𝑟12
where 𝑘a are the star’s dimensionless (second) Love numbers [321], which depend on their internal
structure, and are, typically, of the order unity. On the other hand, for compact objects, we can
introduce their “compactness” parameters, defined by the dimensionless ratios
𝐾a ≡

𝐺𝑚a
,
𝑎a 𝑐2

(15)

and equal ∼ 0.2 for neutron stars (depending on their equation of state). The quadrupoles Qa will
affect the Newtonian binding energy 𝐸 of the two bodies, and also the emitted total gravitational
flux ℱ as computed using the Newtonian quadrupole formula (4). It is known that for inspiralling
compact binaries the neutron stars are not co-rotating because the tidal synchronization time is
much larger than the time left till the coalescence. As shown by Kochanek [276] the best models
for the fluid motion inside the two neutron stars are the so-called Roche–Riemann ellipsoids,
which have tidally locked figures (the quadrupole moments face each other at any instant during
the inspiral), but for which the fluid motion has zero circulation in the inertial frame. In the
Newtonian approximation, using the energy balance equation (9a), we find that within such a
model (in the case of two identical neutron stars with same mass 𝑚, compactness 𝐾 and Love
number 𝑘), the orbital phase reads
{︂
(︁ 𝑥 )︁5 }︂
1
,
(16)
𝜑finite size − 𝜑0 = − 5/2 1 + const 𝑘
𝐾
8𝑥

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 16

16

Luc Blanchet

where “const” denotes a numerical coefficient of order one, 𝜑0 is some initial phase, and 𝑥 ≡
(𝐺𝑚Ω/𝑐3 )2/3 is a standard dimensionless post-Newtonian parameter of the order of ∼ 1/𝑐2 (with
Ω = 2𝜋/𝑃 the orbital frequency). The first term in the right-hand side of Eq. (16) corresponds to
the gravitational-wave damping of two point masses without internal structure; the second term is
the finite-size effect, which appears as a relative correction, proportional to (𝑥/𝐾)5 , to the latter
radiation damping effect. Because the finite-size effect is purely Newtonian, its relative correction
∼ (𝑥/𝐾)5 should not depend on the speed of light 𝑐; and indeed the factors 1/𝑐2 cancel out in
the ratio 𝑥/𝐾. However, the compactness 𝐾 of neutron stars is of the order of 0.2 say, and by
definition of compact objects we can consider that 𝐾 is formally of the order of unity or one half;
therefore the factor 1/𝑐2 it contains in (15) should not be taken into account when estimating
numerically the effect. So the real order of magnitude of the relative contribution of the finite-size
effect in Eq. (16) is given by the factor 𝑥5 alone. This means that for compact objects the finite-size
effect should roughly be comparable, numerically, to a post-Newtonian correction of magnitude
𝑥5 ∼ 1/𝑐10 namely 5PN order. This is a much higher post-Newtonian order than the one at which
we shall investigate the gravitational effects on the phasing formula. Using 𝑘 ∼ 1, 𝐾 ∼ 0.2 and the
bandwidth of detectors between 10 Hz and 1000 Hz, we find that the cumulative phase error due
to the finite-size effect amounts to less that one orbital rotation over a total of ∼ 16 000 produced
by the gravitational-wave damping of two neutron stars. The conclusion is that the finite-size
effects can in general be neglected in comparison with purely gravitational-wave damping effects.
The internal structure of the two compact bodies is “effaced” and their dynamics and radiation
depend only, in first approximation, on the masses (and possibly spins); hence this property has
been called the “effacement” principle of general relativity [142]. But note that for non-compact
or moderately compact objects (such as white dwarfs for instance) the Newtonian tidal interaction
dominates over the radiation damping. The constraints on the nuclear equation of state and the
tidal deformability of neutron stars which can be inferred from gravitational wave observations
of neutron star binary inspirals have been investigated in Refs. [320, 200, 414]. For numerical
computations of the merger of two neutron stars see Refs. [187, 249].
Inspiralling compact binaries are ideally suited for application of a high-order post-Newtonian
wave generation formalism. These systems are very relativistic, with orbital velocities as high as
0.5𝑐 in the last rotations (as compared to ∼ 10−3 𝑐 for the binary pulsar), so it is not surprising
that the quadrupole-moment formalism (2) – (6) constitutes a poor description of the emitted
gravitational waves, since many post-Newtonian corrections are expected to play a substantial
role. This expectation has been confirmed by measurement-analyses [139, 137, 198, 138, 393, 346,
350, 284, 157], which have demonstrated that the post-Newtonian precision needed to implement
successfully the optimal filtering technique for the LIGO/VIRGO detectors corresponds grossly,
in the case of neutron-star binaries, to the 3PN approximation, or 1/𝑐6 beyond the quadrupole
moment approximation. Such a high precision is necessary because of the large number of orbital
rotations that will be monitored in the detector’s frequency bandwidth, giving the possibility of
measuring very accurately the orbital phase of the binary. Thus, the 3PN order is required mostly
to compute the time evolution of the orbital phase, which depends, via Eq. (9a), on the center-ofmass binding energy 𝐸 and the total gravitational-wave energy flux ℱ.
In summary, the theoretical problem is two-fold: On the one hand 𝐸, and on the other hand
ℱ, are to be computed with 3PN precision or better. To obtain 𝐸 we must control the 3PN
equations of motion of the binary in the case of general, not necessarily circular, orbits; as for ℱ it
necessitates the application of a 3PN wave generation formalism. It is remarkable that such high
PN approximation is needed in preparation for the LIGO and VIRGO data analyses. As we shall
see, the signal from compact binaries contains the signature of several non-linear effects which are
specific to general relativity. We thus have the possibility of probing, experimentally, some aspects
of the non-linear structure of Einstein’s theory [84, 85, 15, 14].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 17

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

1.4

17

Post-Newtonian equations of motion

By equations of motion we mean the explicit expression of the accelerations of the bodies in terms
of the positions and velocities. In Newtonian gravity, writing the equations of motion for a system
of N particles is trivial; in general relativity, even writing the equations in the case N = 2 is
difficult. The first relativistic terms, at the 1PN order, were derived by Lorentz & Droste [303].
Subsequently, Einstein, Infeld & Hoffmann [184] obtained the 1PN corrections for N particles by
means of their famous “surface-integral” method, in which the equations of motion are deduced
from the vacuum field equations, and are therefore applicable to any compact objects (be they
neutron stars, black holes, or, perhaps, naked singularities). The 1PN-accurate equations were
also obtained, for the motion of the centers of mass of compact bodies, by Fock [201] (see also
Refs. [341, 330]).
The 2PN approximation was tackled by Ohta et al. [324, 327, 326, 325], who considered the postNewtonian iteration of the Hamiltonian of N point-particles. We refer here to the Hamiltonian as a
“Fokker-type” Hamiltonian, which is obtained from the matter-plus-field Arnowitt–Deser–Misner
(ADM) Hamiltonian by eliminating the field degrees of freedom. The 2.5PN equations of motion
were obtained in harmonic coordinates by Damour & Deruelle [148, 147, 175, 141, 142], building
on a non-linear (post-Minkowskian) iteration of the metric of two particles initiated in Ref. [31].
The corresponding result for the ADM-Hamiltonian of two particles at the 2PN order was given
in Ref. [169] (see also Refs. [375, 376]). The 2.5PN equations of motion have also been derived in
the case of two extended compact objects [280, 234]. The 2.5PN equations of two point masses as
well as the near zone gravitational field in harmonic-coordinate were computed in Ref. [76].9
Up to the 2PN level the equations of motion are conservative. Only at the 2.5PN order does
the first non-conservative effect appear, associated with the gravitational radiation emission. The
equations of motion up to that level [148, 147, 175, 141, 142], have been used for the study of the
radiation damping of the binary pulsar – its orbital 𝑃˙ [142, 143, 173]. The result was in agreement
with the prediction of the quadrupole formalism given by (11). An important point is that the
2.5PN equations of motion have been proved to hold in the case of binary systems of strongly selfgravitating bodies [142]. This is via the effacing principle for the internal structure of the compact
bodies. As a result, the equations depend only on the “Schwarzschild” masses, 𝑚1 and 𝑚2 , of the
neutron stars. Notably their compactness parameters 𝐾1 and 𝐾2 , defined by Eq. (15), do not enter
the equations of motion. This has also been explicitly verified up to the 2.5PN order by Kopeikin
et al. [280, 234], who made a physical computation à la Fock, taking into account the internal
structure of two self-gravitating extended compact bodies. The 2.5PN equations of motion have
also been obtained by Itoh, Futamase & Asada [256, 257] in harmonic coordinates, using a variant
(but, much simpler and more developed) of the surface-integral approach of Einstein et al. [184],
that is valid for compact bodies, independently of the strength of the internal gravity.
At the 3PN order the equations of motion have been worked out independently by several
groups, by means of different methods, and with equivalent results:
1. Jaranowski & Schäfer [261, 262, 263], and then with Damour [162, 164], employ the ADMHamiltonian canonical formalism of general relativity, following the line of research initiated
in Refs. [324, 327, 326, 325, 169];
2. Blanchet & Faye [69, 71, 70, 72], and with de Andrade [174] and Iyer [79], founding their approach on the post-Newtonian iteration initiated in Ref. [76], compute directly the equations
of motion (instead of a Hamiltonian) in harmonic coordinates;
3. Itoh & Futamase [255, 253] (see [213] for a review), continuing the surface-integral method
9 All the works reviewed in this section concern general relativity. However, let us mention here that the equations
of motion of compact binaries in scalar-tensor theories are known up to 2.5PN order [318].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 18

18

Luc Blanchet

of Refs. [256, 257], obtain the complete 3PN equations of motion in harmonic coordinates,
without need of a self-field regularization;
4. Foffa & Sturani [203] derive the 3PN Lagrangian in harmonic coordinates within the effective
field theory approach pioneered by Goldberger & Rothstein [223].
It has been shown [164, 174] that there exists a unique “contact” transformation of the dynamical
variables that changes the harmonic-coordinates Lagrangian of Ref. [174] (identical to the ones
issued from Refs. [255, 253] and [203]) into a new Lagrangian, whose Legendre transform coincides with the ADM-Hamiltonian of Ref. [162]. The equations of motion are therefore physically
equivalent. For a while, however, they depended on one unspecified numerical coefficient, which is
due to some incompleteness of the Hadamard self-field regularization method. This coefficient has
been fixed by means of a better regularization, dimensional regularization, both within the ADMHamiltonian formalism [163], and the harmonic-coordinates equations of motion [61]. These works
have demonstrated the power of dimensional regularization and its adequateness to the classical
problem of interacting point masses in general relativity. By contrast, notice that, interestingly,
the surface-integral method [256, 257, 255, 253] by-passes the need of a regularization. We devote
Section 6 to questions related to the use of self-field regularizations.
The effective field theory (EFT) approach to the problems of motion and radiation of compact
binaries, has been extensively developed since the initial proposal [223] (see [206] for a review). It
borrows techniques from quantum field theory and consists of treating the gravitational interaction
between point particles as a classical limit of a quantum field theory, i.e., in the “tree level”
approximation. The theory is based on the effective action, defined from a Feynman path integral
that integrates over the degrees of freedom that mediate the gravitational interaction.10 The phase
factor in the path integral is built from the standard Einstein–Hilbert action for gravity, augmented
by a harmonic gauge fixing term and by the action of particles. The Feynman diagrams naturally
show up as a perturbative technique for solving iteratively the Green’s functions. Like traditional
approaches [163, 61] the EFT uses the dimensional regularization.
Computing the equations of motion and radiation field using Feynman diagrams in classical
general relativity is not a new idea by itself: Bertotti & Plebanski [35] defined the diagrammatic
tree-level perturbative expansion of the Green’s functions in classical general relativity; Hari Dass
& Soni [240]11 showed how to derive the classical energy-loss formula at Newtonian approximation using tree-level propagating gravitons; Feynman diagrams have been used for the equations
of motion up to 2PN order in general relativity [324, 327, 326, 325] and in scalar-tensor theories [151]. Nevertheless, the systematic EFT treatment has proved to be powerful and innovative
for the field, e.g., with the introduction of a decomposition of the metric into “Kaluza–Klein
type” potentials [277], the interesting link with the renormalization group equation [222], and the
systematization of the computation of diagrams [203].
The 3.5PN terms in the equations of motion correspond to the 1PN relative corrections in the
radiation reaction force. They were derived by Iyer & Will [258, 259] for point-particle binaries
in a general gauge, relying on energy and angular momentum balance equations and the known
expressions of the 1PN fluxes. The latter works have been extended to 2PN order [226] and to
include the leading spin-orbit effects [428]. The result has been then established from first principles
(i.e., not relying on balance equations) in various works at 1PN order [260, 336, 278, 322, 254].
The 1PN radiation reaction force has also been obtained for general extended fluid systems in
a particular gauge [43, 47]. Known also is the contribution of gravitational-wave tails in the
10 The effective action should be equivalent, in the tree-level approximation, to the Fokker action [207], for which
the field degrees of freedom (i.e., the metric), that are solutions of the field equations derived from the original
matter + field action with gauge-fixing term, have been inserted back into the action, thus defining the Fokker
action for the sole matter fields.
11 This reference has an eloquent title: “Feynman graph derivation of the Einstein quadrupole formula”.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 19

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

19

equations of motion, which arises at the 4PN order and represents a 1.5PN modification of the
radiation damping force [58]. This 1.5PN tail-induced correction to the radiation reaction force
was also derived within the EFT approach [205, 215].
The state of the art on equations of motion is the 4PN approximation. Partial results on
the equations of motion at the 4PN order have been obtained in [264, 265, 266] using the ADM
Hamiltonian formalism, and in [204] using the EFT. The first derivation of the complete 4PN
dynamics was accomplished in [166] by combining the local contributions [264, 265, 266] with
a non-local contribution related to gravitational wave tails [58, 43], with the help of the result
of an auxiliary analytical self-force calculation [36]. The non-local dynamics of [166] has been
transformed in Ref. [167] into a local Hamiltonian containing an infinite series of even powers
of the radial momentum. A second computation of the complete 4PN dynamics (including the
same non-local interaction as in [166], but disagreeing on the local interaction) was accomplished
in [33] using a Fokker Lagrangian in harmonic coordinates. Further works [39, 248] have given
independent confirmations of the results of Refs. [166, 167]. More work is needed to understand
the difference between the results of [166] and [33].
An important body of works concerns the effects of spins on the equations of motion of compact
binaries. In this case we have in mind black holes rather than neutron stars, since astrophysical
stellar-size black holes as well as super-massive galactic black holes have spins which can be close
to maximal. The dominant effects are the spin-orbit (SO) coupling which is linear in spin, and
the spin-spin (SS) coupling which is quadratic. For maximally spinning objects, and adopting a
particular convention in which the spin is regarded as a 0.5PN quantity (see Section 11), the leading
SO effect arises at the 1.5PN order while the leading SS effect appears at 2PN order. The leading
SO and SS effects in the equations of motion have been determined by Barker & O’Connell [27, 28]
and Kidder, Will & Wiseman [275, 271]. The next-to-leading SO effect, i.e., 1PN relative order
corresponding to 2.5PN order, was obtained by Tagoshi, Ohashi & Owen [394], then confirmed and
completed by Faye, Blanchet & Buonanno [194]. The results were also retrieved by two subsequent
calculations, using the ADM Hamiltonian [165] and using EFT methods [292, 352]. The ADM
calculation was later generalized to the N -body problem [241] and extended to the next-to-leading
spin-spin effects (including both the coupling between different spins and spin square terms) in
Refs. [387, 389, 388, 247, 243], and the next-to-next-to-leading SS interactions between different
spins at the 4PN order [243]. In the meantime EFT methods progressed concurrently by computing
the next-to-leading 3PN SS and spin-squared contributions [354, 356, 355, 293, 299], and the nextto-next-to-leading 4PN SS interactions for different spins [294] and for spin-squared [298]. Finally,
the next-to-next-to-leading order SO effects, corresponding to 3.5PN order equivalent to 2PN
relative order, were obtained in the ADM-coordinates Hamiltonian [242, 244] and in the harmoniccoordinates equations of motion [307, 90], with complete equivalence between the two approaches.
Comparisons between the EFT and ADM Hamiltonian schemes for high-order SO and SS couplings
can be found in Refs. [295, 299, 297]. We shall devote Section 11 to spin effects (focusing mainly
on spin-orbit effects) in black hole binaries.
So far the status of post-Newtonian equations of motion is very satisfying. There is mutual
agreement between all the results obtained by means of many different approaches and techniques,
whenever they can be compared: point particles described by Dirac delta-functions or extended
post-Newtonian fluids; surface-integrals methods; mixed post-Minkowskian and post-Newtonian
expansions; direct post-Newtonian iteration and matching; EFT techniques versus traditional expansions; harmonic coordinates versus ADM-type coordinates; different processes or variants of
the self-field regularization for point particles; different ways to including spins within the postNewtonian approximation. In Part B of this article, we present complete results for the 3.5PN
equations of motion (including the 1PN radiation reaction), and discuss the conservative part of
the equations in the case of quasi-circular orbits. Notably, the conservative part of the dynamics
is compared with numerical results for the gravitational self-force in Section 8.4.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 20

20

1.5

Luc Blanchet

Post-Newtonian gravitational radiation

The second problem, that of the computation of the gravitational waveform and the energy flux
ℱ, has to be solved by application of a wave generation formalism (see Section 1.1). The earliest
computations at the 1PN level beyond the quadrupole moment formalism were done by Wagoner
& Will [416], but based on some ill-defined expressions of the multipole moments [185, 403]. The
computations were redone and confirmed by Blanchet & Schäfer [86] applying the rigorous wave
generation formalism of Refs. [57, 60]. Remember that at that time the post-Newtonian corrections
to the emission of gravitational waves had only a purely academic interest.
The energy flux of inspiralling compact binaries was then completed to the 2PN order by
Blanchet, Damour & Iyer [64, 224], and, independently, by Will & Wiseman [424, 422], using their
own formalism; see Refs. [66, 82] for joint reports of these calculations. The energy flux has been
computed using the EFT approach in Ref. [221] with results agreeing with traditional methods.
At the 1.5PN order in the radiation field, appears the first contribution of “hereditary” terms,
which are a priori sensitive to the entire past history of the source, i.e., which depend on all
previous times up to 𝑡 → −∞ in the past [60]. This 1.5PN hereditary term represents the dominant
contribution of tails in the wave zone. It has been evaluated for compact binaries in Refs. [426, 87]
by application of the formula for tail integrals given in Ref. [60]. Higher-order tail effects at the
2.5PN and 3.5PN orders, as well as a crucial contribution of tails generated by the tails themselves
(the so-called “tails of tails”) at the 3PN order, were obtained in Refs [45, 48].
The 3PN approximation also involves, besides the tails of tails, many non-tail contributions
coming from the relativistic corrections in the (source) multipole moments of the compact binary.
Those have been almost completed in Refs. [81, 73, 80], in the sense that the result still involved
one unknown numerical coefficient, due to the use of the Hadamard regularization. We shall review
in Section 6 the computation of this parameter by means of dimensional regularization [62, 63], and
shall present in Section 9 the most up-to-date results for the 3.5PN energy flux and orbital phase,
deduced from the energy balance equation. In recent years all the results have been generalized to
non-circular orbits, including both the fluxes of energy and angular momentum, and the associated
balance equations [10, 9, 12]. The problem of eccentric orbits will be the subject of Section 10.
Besides the problem of the energy flux there is the problem of the gravitational waveform itself,
which includes higher-order amplitude corrections and correlatively higher-order harmonics of the
orbital frequency, consistent with the post-Newtonian order. Such full post-Newtonian waveform
is to be contrasted with the so-called “restricted” post-Newtonian waveform which retains only the
leading-order harmonic of the signal at twice the orbital frequency, and is often used in practical
data analysis when searching the signal. However, for parameter estimation the full waveform is
to be taken into account. For instance it has been shown that using the full waveform in the
data analysis of future space-based detectors like eLISA will yield substantial improvements (with
respect to the restricted waveform) of the angular resolution and the estimation of the luminosity
distance of super-massive black hole binaries [16, 17, 410].
The full waveform has been obtained up to 2PN order in Ref. [82] by means of two independent
wave generations (respectively those of Refs. [57, 44] and [424]), and it was subsequently extended
up to the 3PN order in Refs. [11, 273, 272, 74]. At that order the signal contains the contributions
of harmonics of the orbital frequency up to the eighth mode. The motivation is not only to build
accurate templates for the data analysis of gravitational wave detectors, but also to facilitate the
comparison and match of the high post-Newtonian prediction for the inspiral waveform with the
numerically-generated waveforms for the merger and ringdown. For the latter application it is
important to provide the post-Newtonian results in terms of a spin-weighted spherical harmonic
decomposition suitable for a direct comparison with the results of numerical relativity. Recently the
dominant quadrupole mode (ℓ, 𝑚) = (2, 2) in the spin-weighted spherical harmonic decomposition
has been obtained at the 3.5PN order [197]. Available results will be provided in Sections 9.4

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 21

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

21

and 9.5.
At the 2.5PN order in the waveform appears the dominant contribution of another hereditary
effect called the “non-linear memory” effect (or sometimes Christodoulou effect) [128, 427, 406, 60,
50]. This effect was actually discovered using approximation methods in Ref. [42] (see [60] for a
discussion). It implies a permanent change in the wave amplitude from before to after a burst of
gravitational waves, which can be interpreted as the contribution of gravitons in the known formulas
for the linear memory for massless particles [99]. Note that the non-linear memory takes the form
of a simple anti-derivative of an “instantaneous” term, and therefore becomes instantaneous (i.e.,
non-hereditary) in the energy flux which is composed of the time-derivative of the waveform. In
principle the memory contribution must be computed using some model for the evolution of the
binary system in the past. Because of the cumulative effect of integration over the whole past,
the memory term, though originating from 2.5PN order, finally contributes in the waveform at the
Newtonian level [427, 11]. It represents a part of the waveform whose amplitude steadily grows
with time, but which is nearly constant over one orbital period. It is therefore essentially a zerofrequency effect (or DC effect), which has rather poor observational consequences in the case of the
LIGO-VIRGO detectors, whose frequency bandwidth is always limited from below by some cut-off
frequency 𝑓seismic > 0. Non-linear memory contributions in the waveform of inspiralling compact
binaries have been thoroughly computed by Favata [189, 192].
The post-Newtonian results for the waveform and energy flux are in complete agreement (up
to the 3.5PN order) with the results given by the very different technique of linear black-hole
perturbations, valid when the mass of one of the bodies is small compared to the other. This is the
test-mass limit 𝜈 → 0, in which we define the symmetric mass ratio to be the reduced mass divided
by the total mass, 𝜈 ≡ 𝜇/𝑚 such that 𝜈 = 1/4 for equal masses. Linear black-hole perturbations,
triggered by the geodesic motion of a small particle around the black hole, have been applied
to this problem by Poisson [345] at the 1.5PN order (following the pioneering work [216]), by
Tagoshi & Nakamura [393], using a numerical code up to the 4PN order, and by Sasaki, Tagoshi &
Tanaka [372, 395, 397] (see also Ref. [316]), analytically up to the 5.5PN order. More recently the
method has been improved and extended up to extremely high post-Newtonian orders: 14PN [209]
and even 22PN [210] orders – but still for linear black-hole perturbations.
To successfully detect the gravitational waves emitted by spinning black hole binaries and
to estimate the binary parameters, it is crucial to include spins effects in the templates, most
importantly the spin-orbit effect which is linear in spins. The spins will affect the gravitational
waves through a modulation of their amplitude, phase and frequency. Notably the orbital plane
will precess in the case where the spins are not aligned or anti-aligned with the orbital angular
momentum, see e.g., Ref. [8]. The leading SO and SS contributions in the waveform and flux
of compact binaries are known from Refs. [275, 271, 314]; the next-to-leading SO terms at order
2.5PN were obtained in Ref. [53] after a previous attempt in [328]; the 3PN SO contribution is
due to tails and was computed in Ref. [54], after intermediate results at the same order (but
including SS terms) given in [353]. Finally, the next-to-next-to-leading SO contributions in the
multipole moments and the energy flux, corresponding to 3.5PN order, and the next-to-leading SO
tail corresponding to 4PN order, have been obtained in Refs. [89, 306]. The next-to-leading 3PN
SS and spin-squared contributions in the radiation field were derived in Ref. [88]. In Section 11
we shall give full results for the contributions of spins (at SO linear level) in the energy flux and
phase evolution up to 4PN order.
A related topic is the loss of linear momentum by gravitational radiation and the resulting
gravitational recoil (or “kick”) of black-hole binary systems. This phenomenon has potentially
important astrophysical consequences [313]. In models of formation of massive black holes involving
successive mergers of smaller “seed” black holes, a recoil with sufficient velocity could eject the
system from the host galaxy and effectively terminate the process. Recoils could eject coalescing
black holes from dwarf galaxies or globular clusters. Even in galaxies whose potential wells are

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 22

22

Luc Blanchet

deep enough to confine the recoiling system, displacement of the system from the center could have
important dynamical consequences for the galactic core.
Post-Newtonian methods are not ideally suited to compute the recoil of binary black holes
because most of the recoil is generated in the strong field regime close to the coalescence [199].
Nevertheless, after earlier computations of the dominant Newtonian effect [30, 199]12 and the 1PN
relative corrections [425], the recoil velocity has been obtained up to 2PN order for point particle
binaries without spin [83], and is also known for the dominant spin effects [271]. Various estimations
of the magnitude of the kick include a PN calculation for the inspiraling phase together with a
treatment of the plunge phase [83], an application of the effective-one-body formalism [152], a
close-limit calculation with Bowen–York type initial conditions [385], and a close-limit calculation
with initial PN conditions for the ringdown phase [288, 290].
In parallel the problem of gravitational recoil of coalescing binaries has attracted considerable
attention from the numerical relativity community. These computations led to increasingly accurate estimates of the kick velocity from the merger along quasicircular orbits of binary black holes
without spins [115, 20] and with spins [117]. In particular these numerical simulations revealed
the interesting result that very large kick velocities can be obtained in the case of spinning black
holes for particular spin configurations.

12 In absence of a better terminology, we refer to the leading-order contribution to the recoil as “Newtonian”,
although it really corresponds to a 3.5PN subdominant radiation-reaction effect in the binary’s equations of motion.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 23

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

23

Part A: Post-Newtonian Sources
2

Non-linear Iteration of the Vacuum Field Equations

2.1

Einstein’s field equations

The field equations of general relativity are obtained by varying the space-time metric 𝑔𝛼𝛽 in the
famous Einstein–Hilbert action,
∫︁
[︀
]︀
√
𝑐3
𝐼EH =
d4 𝑥 −𝑔 𝑅 + 𝐼mat Ψ, 𝑔𝛼𝛽 .
(17)
16𝜋𝐺
They form a system of ten second-order partial differential equations obeyed by the metric,
𝐸 𝛼𝛽 [𝑔, 𝜕𝑔, 𝜕 2 𝑔] =

8𝜋𝐺 𝛼𝛽
𝑇 [Ψ, 𝑔] ,
𝑐4

(18)

where the Einstein curvature tensor 𝐸 𝛼𝛽 ≡ 𝑅𝛼𝛽 − 12 𝑅 𝑔 𝛼𝛽 is generated, through the gravitational
coupling constant 𝜅 = 8𝜋𝐺/𝑐4 , by the stress-energy tensor 𝑇 𝛼𝛽 ≡ √2−𝑔 𝛿𝐼mat /𝛿𝑔𝛼𝛽 of the matter
fields Ψ. Among these ten equations, four govern, via the contracted Bianchi identity, the evolution
of the matter system,
∇𝜇 𝐸 𝛼𝜇 = 0 =⇒ ∇𝜇 𝑇 𝛼𝜇 = 0 .
(19)
The matter equations can also be obtained by varying the matter action in (17) with respect to
the matter fields Ψ. The space-time geometry is constrained by the six remaining equations, which
place six independent constraints on the ten components of the metric 𝑔𝛼𝛽 , leaving four of them
to be fixed by a choice of the coordinate system.
In most of this paper we adopt the conditions of harmonic coordinates, sometimes also called
de Donder coordinates. We define, as a basic variable, the gravitational-field amplitude
√
ℎ𝛼𝛽 ≡ −𝑔 𝑔 𝛼𝛽 − 𝜂 𝛼𝛽 ,
(20)
where 𝑔 𝛼𝛽 denotes the contravariant metric (satisfying 𝑔 𝛼𝜇 𝑔𝜇𝛽 = 𝛿𝛽𝛼 ), where 𝑔 is the determinant
of the covariant metric, 𝑔 ≡ det(𝑔𝛼𝛽 ), and where 𝜂 𝛼𝛽 represents an auxiliary Minkowskian metric
𝜂 𝛼𝛽 ≡ diag(−1, 1, 1, 1). The harmonic-coordinate condition, which accounts exactly for the four
equations (19) corresponding to the conservation of the matter tensor, reads13
𝜕𝜇 ℎ𝛼𝜇 = 0 .

(21)

Equation (21) introduces into the definition of our coordinate system a preferred Minkowskian
structure, with Minkowski metric 𝜂𝛼𝛽 . Of course, this is not contrary to the spirit of general relativity, where there is only one physical metric 𝑔𝛼𝛽 without any flat prior geometry, because the
coordinates are not governed by geometry (so to speak), but rather can be chosen at convenience,
depending on physical phenomena under study. The coordinate condition (21) is especially useful
when studying gravitational waves as perturbations of space-time propagating on the fixed background metric 𝜂𝛼𝛽 . This view is perfectly legitimate and represents a fruitful and rigorous way
13 Considering the coordinates 𝑥𝛼 as a set of four scalars, a simple calculation shows that

𝜕𝜇 ℎ𝛼𝜇 =

√

−𝑔 𝑔 𝑥𝛼 ,

where 𝑔 ≡ 𝑔 𝜇𝜈 ∇𝜇 ∇𝜈 denotes the curved d’Alembertian operator. Hence the harmonic-coordinate condition
tells that the coordinates 𝑥𝛼 themselves, considered as scalars, are harmonic, i.e., obey the vacuum (curved)
d’Alembertian equation.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 24

24

Luc Blanchet

to think of the problem using approximation methods. Indeed, the metric 𝜂𝛼𝛽 , originally introduced in the coordinate condition (21), does exist at any finite order of approximation (neglecting
higher-order terms), and plays the role of some physical “prior” flat geometry at any order of
approximation.
The Einstein field equations in harmonic coordinates can be written in the form of inhomogeneous flat d’Alembertian equations,
ℎ𝛼𝛽 =

16𝜋𝐺 𝛼𝛽
𝜏 ,
𝑐4

(22)

where  ≡ 𝜂 = 𝜂 𝜇𝜈 𝜕𝜇 𝜕𝜈 . The source term 𝜏 𝛼𝛽 can rightly be interpreted as the stress-energy
pseudo-tensor (actually, 𝜏 𝛼𝛽 is a Lorentz-covariant tensor) of the matter fields, described by 𝑇 𝛼𝛽 ,
and the gravitational field, given by the gravitational source term Λ𝛼𝛽 , i.e.,
𝜏 𝛼𝛽 = |𝑔|𝑇 𝛼𝛽 +

𝑐4
Λ𝛼𝛽 .
16𝜋𝐺

(23)

The exact expression of Λ𝛼𝛽 in harmonic coordinates, including all non-linearities, reads14
1
2
Λ𝛼𝛽 = −ℎ𝜇𝜈 𝜕𝜇𝜈
ℎ𝛼𝛽 + 𝜕𝜇 ℎ𝛼𝜈 𝜕𝜈 ℎ𝛽𝜇 + 𝑔 𝛼𝛽 𝑔𝜇𝜈 𝜕𝜆 ℎ𝜇𝜏 𝜕𝜏 ℎ𝜈𝜆
2
− 𝑔 𝛼𝜇 𝑔𝜈𝜏 𝜕𝜆 ℎ𝛽𝜏 𝜕𝜇 ℎ𝜈𝜆 − 𝑔 𝛽𝜇 𝑔𝜈𝜏 𝜕𝜆 ℎ𝛼𝜏 𝜕𝜇 ℎ𝜈𝜆 + 𝑔𝜇𝜈 𝑔 𝜆𝜏 𝜕𝜆 ℎ𝛼𝜇 𝜕𝜏 ℎ𝛽𝜈
)︀(︀
)︀
1 (︀
+ 2𝑔 𝛼𝜇 𝑔 𝛽𝜈 − 𝑔 𝛼𝛽 𝑔 𝜇𝜈 2𝑔𝜆𝜏 𝑔𝜖𝜋 − 𝑔𝜏 𝜖 𝑔𝜆𝜋 𝜕𝜇 ℎ𝜆𝜋 𝜕𝜈 ℎ𝜏 𝜖 .
8

(24)

As is clear from this expression, Λ𝛼𝛽 is made of terms at least quadratic in the gravitational-field
strength ℎ and its first and second space-time derivatives. In the following, for the highest postNewtonian order that we shall consider, we will need the quadratic, cubic and quartic pieces of
Λ𝛼𝛽 ; with obvious notation, we can write them as
Λ𝛼𝛽 = 𝑁 𝛼𝛽 [ℎ, ℎ] + 𝑀 𝛼𝛽 [ℎ, ℎ, ℎ] + 𝐿𝛼𝛽 [ℎ, ℎ, ℎ, ℎ] + 𝒪(ℎ5 ) .

(25)

These various terms can be straightforwardly computed from expanding Eq. (24); for instance the
leading quadratic piece is explicitly given by15
(︀
)︀
1
1
2
𝑁 𝛼𝛽 = − ℎ𝜇𝜈 𝜕𝜇𝜈
ℎ𝛼𝛽 + 𝜕 𝛼 ℎ𝜇𝜈 𝜕 𝛽 ℎ𝜇𝜈 − 𝜕 𝛼 ℎ𝜕 𝛽 ℎ + 𝜕𝜈 ℎ𝛼𝜇 𝜕 𝜈 ℎ𝛽𝜇 + 𝜕𝜇 ℎ𝛽𝜈
2
4
[︁ 1
]︁
1
1
(𝛼
𝜇 𝛽)𝜈
𝛼𝛽
− 2𝜕 ℎ𝜇𝜈 𝜕 ℎ
+𝜂
− 𝜕𝜏 ℎ𝜇𝜈 𝜕 𝜏 ℎ𝜇𝜈 + 𝜕𝜇 ℎ𝜕 𝜇 ℎ + 𝜕𝜇 ℎ𝜈𝜏 𝜕 𝜈 ℎ𝜇𝜏 .
(26)
4
8
2
As we said, the condition (21) is equivalent to the matter equations of motion, in the sense of
the conservation of the total pseudo-tensor 𝜏 𝛼𝛽 ,
𝜕𝜇 𝜏 𝛼𝜇 = 0

⇐⇒

∇𝜇 𝑇 𝛼𝜇 = 0 .

(27)

In this article, we shall look for approximate solutions of the field equations (21) – (22) under the
following four hypotheses:
1. The matter stress-energy tensor 𝑇 𝛼𝛽 is of spatially compact support, i.e., can be enclosed
into some time-like world tube, say 𝑟 ⩽ 𝑎, where 𝑟 = |x| is the harmonic-coordinate radial
distance. Outside the domain of the source, when 𝑟 > 𝑎, the gravitational source term,
according to Eq. (27), is divergence-free,
𝜕𝜇 Λ𝛼𝜇 = 0

(when 𝑟 > 𝑎) ;

(28)

14 In 𝑑 + 1 space-time dimensions, only one coefficient in this expression is modified; see Eq. (175) below.
15 See Eqs. (3.8) in Ref. [71] for the cubic and quartic terms.

𝛼𝜈 , ℎ = 𝜂
𝜇𝜈 , and
We denote e.g., ℎ𝛼
𝜇𝜈 ℎ
𝜇 = 𝜂𝜇𝜈 ℎ
𝜕 𝛼 = 𝜂 𝛼𝜇 𝜕𝜇 . A parenthesis around a pair of indices denotes the usual symmetrization: 𝑇 (𝛼𝛽) = 21 (𝑇 𝛼𝛽 + 𝑇 𝛽𝛼 ).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 25

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

25

2. The matter distribution inside the source is smooth: 𝑇 𝛼𝛽 ∈ 𝐶 ∞ (R3 ).16 We have in mind a
smooth hydrodynamical fluid system, without any singularities nor shocks (a priori ), that is
described by some Euler-type equations including high relativistic corrections. In particular,
we exclude from the start the presence of any black holes; however, we shall return to this
question in Part B when we look for a model describing compact objects;
3. The source is post-Newtonian in the sense of the existence of the small parameter defined by
Eq. (1). For such a source we assume the legitimacy of the method of matched asymptotic
expansions for identifying the inner post-Newtonian field and the outer multipolar decomposition in the source’s exterior near zone;
4. The gravitational field has been independent of time (stationary) in some remote past, i.e.,
before some finite instant −𝒯 in the past, namely
]︀
𝜕 [︀ 𝛼𝛽
ℎ (x, 𝑡) = 0
𝜕𝑡

when 𝑡 ⩽ −𝒯 .

(29)

The latter condition is a means to impose, by brute force, the famous no-incoming radiation
condition, ensuring that the matter source is isolated from the rest of the Universe and does
not receive any radiation from infinity. Ideally, the no-incoming radiation condition should be
imposed at past null infinity. As we shall see, this condition entirely fixes the radiation reaction
forces inside the isolated source. We shall later argue (see Section 3.2) that our condition of
stationarity in the past (29), although weaker than the ideal no-incoming radiation condition, does
not entail any physical restriction on the general validity of the formulas we derive. Even more,
the condition (29) is actually better suited in the case of real astrophysical sources like inspiralling
compact binaries, for which we do not know the details of the initial formation and remote past
evolution. In practice the initial instant −𝒯 can be set right after the explosions of the two
supernovæ yielding the formation of the compact binary system.
Subject to the past-stationarity condition (29), the differential equations (22) can be written
equivalently into the form of the integro-differential equations
ℎ𝛼𝛽 =

16𝜋𝐺 −1 𝛼𝛽
ret 𝜏 ,
𝑐4

(30)

containing the usual retarded inverse d’Alembertian integral operator, given by
∫︁∫︁∫︁
)︀
d3 x′ (︀ ′
1
−1
𝜏 x , 𝑡 − |x − x′ |/𝑐 ,
(ret 𝜏 )(x, 𝑡) ≡ −
4𝜋
|x − x′ |

(31)

extending over the whole three-dimensional space R3 .

2.2

Linearized vacuum equations

In what follows we solve the field equations (21) – (22), in the vacuum region outside the compactsupport source, in the form of a formal non-linearity or post-Minkowskian expansion, considering
the field variable ℎ𝛼𝛽 as a non-linear metric perturbation of Minkowski space-time. At the linearized level (or first-post-Minkowskian approximation), we write:
𝛼𝛽
2
ℎ𝛼𝛽
ext = 𝐺 ℎ(1) + 𝒪(𝐺 ) ,

(32)

16 N, Z, R, and C are the usual sets of non-negative integers, integers, real numbers, and complex numbers; 𝐶 𝑝 (Ω)
is the set of 𝑝-times continuously differentiable functions on the open domain Ω (𝑝 ⩽ +∞).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 26

26

Luc Blanchet

where the subscript “ext” reminds us that the solution is valid only in the exterior of the source,
and where we have introduced Newton’s constant 𝐺 as a book-keeping parameter, enabling one to
label conveniently the successive post-Minkowskian approximations. Since ℎ𝛼𝛽 is a dimensionless
variable, with our convention the linear coefficient ℎ𝛼𝛽
(1) in Eq. (32) has the dimension of the inverse
of 𝐺 (which should be a mass squared in a system of units where ~ = 𝑐 = 1). In vacuum, the
harmonic-coordinate metric coefficient ℎ𝛼𝛽
(1) satisfies
ℎ𝛼𝛽
(1) = 0 ,

(33a)

𝜕𝜇 ℎ𝛼𝜇
(1) = 0 .

(33b)

We want to solve those equations by means of an infinite multipolar series valid outside a timelike world tube containing the source. Indeed the multipole expansion is the appropriate method
for describing the physics of the source as seen from its exterior (𝑟 > 𝑎). On the other hand,
the post-Minkowskian series is physically valid in the weak-field region, which surely includes the
exterior of any source, starting at a sufficiently large distance. For post-Newtonian sources the
exterior weak-field region, where both multipole and post-Minkowskian expansions are valid, simply
coincides with the exterior region 𝑟 > 𝑎. It is therefore quite natural, and even, one would say
inescapable when considering general sources, to combine the post-Minkowskian approximation
with the multipole decomposition. This is the original idea of the “double-expansion” series of
Bonnor and collaborators [94, 95, 96, 251], which combines the 𝐺-expansion (or 𝑚-expansion in
their notation) with the 𝑎-expansion (equivalent to the multipole expansion, since the ℓ-th order
multipole moment scales with the source radius like 𝑎ℓ ).
The multipolar-post-Minkowskian (MPM) method will be implemented systematically, using
symmetric-trace-free (STF) harmonics to describe the multipole expansion [403], and looking for a
definite algorithm for the approximation scheme [57]. The solution of the system of equations (33)
takes the form of a series of retarded multipolar waves17
(︃
)︃
+∞
∑︁
K𝛼𝛽
𝛼𝛽
𝐿 (𝑡 − 𝑟/𝑐)
ℎ(1) =
𝜕𝐿
,
(34)
𝑟
ℓ=0

𝛼𝛽
where 𝑟 = |x|, and where the functions K𝛼𝛽
𝐿 ≡ K𝑖1 ...𝑖ℓ are smooth functions of the retarded time
∞
𝑢 ≡ 𝑡 − 𝑟/𝑐 [i.e., K𝐿 (𝑢) ∈ 𝐶 (R)], which become constant in the past, when 𝑡 ⩽ −𝒯 , see Eq. (29).
Since a monopolar wave satisfies (K𝐿 (𝑢)/𝑟) = 0 and the d’Alembertian commutes with the
multi-derivative 𝜕𝐿 , it is evident that Eq. (34) represents the most general solution of the wave
equation (33a); but see Section 2 in Ref. [57] for a rigorous proof based on the Euler–Poisson–
Darboux equation. The gauge condition (33b), however, is not fulfilled in general, and to satisfy it
𝑖𝑗
0𝑖
we must algebraically decompose the set of functions K00
𝐿 , K𝐿 , K𝐿 into ten tensors which are STF
with respect to all their indices, including the spatial indices 𝑖, 𝑖𝑗. Imposing the condition (33b)
17 Our notation is the following: 𝐿 = 𝑖 𝑖 . . . 𝑖 denotes a multi-index, made of ℓ (spatial) indices. Similarly, we
1 2
ℓ
write for instance 𝐾 = 𝑗1 . . . 𝑗𝑘 (in practice, we generally do not need to write explicitly the “carrier” letter 𝑖 or
𝑗), or 𝑎𝐿 − 1 = 𝑎𝑖1 . . . 𝑖ℓ−1 . Always understood in expressions such as Eq. (34) are ℓ summations over the indices
𝑖1 , . . . , 𝑖ℓ ranging from 1 to 3. The derivative operator 𝜕𝐿 is a short-hand for 𝜕𝑖1 . . . 𝜕𝑖ℓ . The function K𝐿 (for any
space-time indices 𝛼𝛽) is symmetric and trace-free (STF) with respect to the ℓ indices composing 𝐿. This means
that for any pair of indices 𝑖𝑝 , 𝑖𝑞 ∈ 𝐿, we have K...𝑖𝑝 ...𝑖𝑞 ... = K...𝑖𝑞 ...𝑖𝑝 ... and that 𝛿𝑖𝑝 𝑖𝑞 K...𝑖𝑝 ...𝑖𝑞 ... = 0 (see Ref. [403]
and Appendices A and B in Ref. [57] for reviews about the STF formalism). The STF projection is denoted with
^ 𝐿 , or sometimes with carets around the indices, K𝐿 ≡ K⟨𝐿⟩ . In particular, ^
a hat, so K𝐿 ≡ K
𝑛𝐿 = 𝑛⟨𝐿⟩ is the STF
𝑛𝑖𝑗𝑘 = 𝑛⟨𝑖𝑗𝑘⟩ =
projection of the product of unit vectors 𝑛𝐿 = 𝑛𝑖1 . . . 𝑛𝑖ℓ , for instance 𝑛
^ 𝑖𝑗 = 𝑛⟨𝑖𝑗⟩ = 𝑛𝑖𝑗 − 13 𝛿𝑖𝑗 and ^
𝑛𝑖𝑗𝑘 − 15 (𝛿𝑖𝑗 𝑛𝑘 + 𝛿𝑖𝑘 𝑛𝑗 + 𝛿𝑗𝑘 𝑛𝑖 ); an expansion into STF tensors ^
𝑛𝐿 = 𝑛
^ 𝐿 (𝜃, 𝜑) is equivalent to the usual expansion
in spherical harmonics Y𝑙𝑚 = Y𝑙𝑚 (𝜃, 𝜑), see Eqs. (75) below. Similarly, we denote 𝑥𝐿 = 𝑥𝑖1 . . . 𝑥𝑖ℓ = 𝑟𝑙 𝑛𝐿 where
𝑟 = |x|, and 𝑥
^𝐿 = 𝑥⟨𝐿⟩ = STF[𝑥𝐿 ]. The Levi-Civita antisymmetric symbol is denoted 𝜖𝑖𝑗𝑘 (with 𝜖123 = 1).
Parenthesis refer to symmetrization, 𝑇(𝑖𝑗) = 12 (𝑇𝑖𝑗 + 𝑇𝑗𝑖 ). Superscripts (𝑞) indicate 𝑞 successive time derivations.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 27

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

27

reduces the number of independent tensors to six, and we find that the solution takes an especially
simple “canonical” form, parametrized by only two moments, plus some arbitrary linearized gauge
transformation [403, 57].
Theorem 1. The most general solution of the linearized field equations (33) outside some time-like
world tube enclosing the source (𝑟 > 𝑎), and stationary in the past [see Eq. (29)], reads
𝛼𝛽
𝛼 𝛽
𝛽 𝛼
𝛼𝛽
ℎ𝛼𝛽
𝜕𝜇 𝜙𝜇(1) .
(1) = 𝑘(1) + 𝜕 𝜙(1) + 𝜕 𝜙(1) − 𝜂

(35)

The first term depends on two STF-tensorial multipole moments, I𝐿 (𝑢) and J𝐿 (𝑢), which are
arbitrary functions of time except for the laws of conservation of the monopole: I = const, and
dipoles: I𝑖 = const, J𝑖 = const. It is given by
(︂
)︂
1
4 ∑︁ (−)ℓ
00
𝜕𝐿
I𝐿 (𝑢) ,
(36a)
𝑘(1) = − 2
𝑐
ℓ!
𝑟
ℓ⩾0
{︂
(︂
)︂
(︂
)︂}︂
1 (1)
ℓ
1
4 ∑︁ (−)ℓ
0𝑖
𝑘(1)
𝜕𝐿−1
I𝑖𝐿−1 (𝑢) +
𝜖𝑖𝑎𝑏 𝜕𝑎𝐿−1
J𝑏𝐿−1 (𝑢)
,
(36b)
= 3
𝑐
ℓ!
𝑟
ℓ+1
𝑟
ℓ⩾1
{︂
)︂
)︂}︂
(︂
(︂
4 ∑︁ (−)ℓ
2ℓ
1 (2)
1
(1)
𝑖𝑗
𝑘(1) = − 4
𝜕𝐿−2
I
(𝑢) +
𝜕𝑎𝐿−2
𝜖𝑎𝑏(𝑖 J𝑗)𝑏𝐿−2 (𝑢)
.
(36c)
𝑐
ℓ!
𝑟 𝑖𝑗𝐿−2
ℓ+1
𝑟
ℓ⩾2

The other terms represent a linearized gauge transformation, with gauge vector 𝜙𝛼
(1) parametrized
by four other multipole moments, say W𝐿 (𝑢), X𝐿 (𝑢), Y𝐿 (𝑢) and Z𝐿 (𝑢) [see Eqs. (37)].
The conservation of the lowest-order moments gives the constancy of the total mass of the source,
(1)
M ≡ I = const, center-of-mass position, X𝑖 ≡ I𝑖 /I = const, total linear momentum P𝑖 ≡ I𝑖 = 0,18
and total angular momentum, J𝑖 = const. It is always possible to achieve X𝑖 = 0 by translating
the origin of our coordinates to the center of mass. The total mass M is the ADM mass of the
Hamiltonian formulation of general relativity. Note that the quantities M, X𝑖 , P𝑖 and J𝑖 include
the contributions due to the waves emitted by the source. They describe the initial state of the
source, before the emission of gravitational radiation.
The multipole functions I𝐿 (𝑢) and J𝐿 (𝑢), which thoroughly encode the physical properties of
the source at the linearized level (because the other moments W𝐿 , . . . , Z𝐿 parametrize a gauge
transformation), will be referred to as the mass-type and current-type source multipole moments.
Beware, however, that at this stage the moments are not specified in terms of the stress-energy
tensor 𝑇 𝛼𝛽 of the source: Theorem 1 follows merely from the algebraic and differential properties
of the vacuum field equations outside the source.
For completeness, we give the components of the gauge-vector 𝜙𝛼
(1) entering Eq. (35):
4 ∑︁ (−)ℓ
𝜕𝐿
𝑐3
ℓ!

)︂
1
W𝐿 (𝑢) ,
𝑟
ℓ⩾0
(︂
)︂
4 ∑︁ (−)ℓ
1
𝜙𝑖(1) = − 4
𝜕𝑖𝐿
X𝐿 (𝑢)
𝑐
ℓ!
𝑟
ℓ⩾0
{︂
(︂
)︂
(︂
)︂}︂
4 ∑︁ (−)ℓ
1
ℓ
1
− 4
𝜕𝐿−1
Y𝑖𝐿−1 (𝑢) +
𝜖𝑖𝑎𝑏 𝜕𝑎𝐿−1
Z𝑏𝐿−1 (𝑢)
.
𝑐
ℓ!
𝑟
ℓ+1
𝑟
𝜙0(1) =

(︂

(37a)
(37b)
(37c)

ℓ⩾1

18 The constancy of the center of mass X – rather than a linear variation with time – results from our assumption
𝑖
of stationarity before the date −𝒯 , see Eq. (29). Hence, P𝑖 = 0.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 28

28

Luc Blanchet

Because the theory is covariant with respect to non-linear diffeomorphisms and not merely with
respect to linear gauge transformations, the moments W𝐿 , . . . , Z𝐿 do play a physical role starting
at the non-linear level, in the following sense. If one takes these moments equal to zero and
continues the post-Minkowskian iteration [see Section 2.3] one ends up with a metric depending
on I𝐿 and J𝐿 only, but that metric will not describe the same physical source as the one which
would have been constructed starting from the six moments I𝐿 , J𝐿 , . . . , Z𝐿 altogether. In other
words, the two non-linear metrics associated with the sets of multipole moments {I𝐿 , J𝐿 , 0, . . . , 0}
and {I𝐿 , J𝐿 , W𝐿 , . . . , Z𝐿 } are not physically equivalent – they are not isometric. We shall point
out in Section 2.4 below that the full set of moments {I𝐿 , J𝐿 , W𝐿 , . . . , Z𝐿 } is in fact physically
equivalent to some other reduced set of moments {M𝐿 , S𝐿 , 0, . . . , 0}, but with some moments M𝐿 ,
S𝐿 that differ from I𝐿 , J𝐿 by non-linear corrections [see Eqs. (97) – (98)]. The moments M𝐿 , S𝐿 are
called “canonical” moments; they play a useful role in intermediate calculations. All the multipole
moments I𝐿 , J𝐿 , W𝐿 , X𝐿 , Y𝐿 , Z𝐿 will be computed in Section 4.4.

2.3

The multipolar post-Minkowskian solution

By Theorem 1 we know the most general solution of the linearized equations in the exterior of
the source. We then tackle the problem of the post-Minkowskian iteration of that solution. We
consider the full post-Minkowskian series
ℎ𝛼𝛽
ext =

+∞
∑︁

𝐺𝑛 ℎ𝛼𝛽
(𝑛) ,

(38)

𝑛=1

where the first term is composed of the result given by Eqs. (35) – (37). In this article, we shall
always understand the infinite sums such as the one in Eq. (38) in the sense of formal power
series, i.e., as an ordered collection of coefficients, (ℎ𝛼𝛽
(𝑛) )𝑛∈N . We do not attempt to control the
mathematical nature of the series and refer to the mathematical-physics literature for discussion
of that point (see, in the present context, Refs. [130, 171, 361, 362, 363]).
We substitute the post-Minkowski ansatz (38) into the vacuum Einstein field equations (21) –
(22), i.e., with 𝜏 𝛼𝛽 simply given by the gravitational source term Λ𝛼𝛽 , and we equate term by term
the factors of the successive powers of our book-keeping parameter 𝐺. We get an infinite set of
equations for each of the ℎ𝛼𝛽
(𝑛) ’s: namely, ∀𝑛 ⩾ 2,
𝛼𝛽
ℎ𝛼𝛽
(𝑛) = Λ(𝑛) [ℎ(1) , ℎ(2) , . . . , ℎ(𝑛−1) ] ,

(39a)

𝜕𝜇 ℎ𝛼𝜇
(𝑛) = 0 .

(39b)

The right-hand side of the wave equation (39a) is obtained from inserting the previous iterations,
known up to the order 𝑛 − 1, into the gravitational source term. In more details, the series of
equations (39a) reads
𝛼𝛽
ℎ𝛼𝛽
[ℎ(1) , ℎ(1) ] ,
(2) = 𝑁

(40a)

𝛼𝛽
ℎ𝛼𝛽
[ℎ(1) , ℎ(1) , ℎ(1) ] + 𝑁 𝛼𝛽 [ℎ(1) , ℎ(2) ] + 𝑁 𝛼𝛽 [ℎ(2) , ℎ(1) ] ,
(3) = 𝑀

(40b)

𝛼𝛽
ℎ𝛼𝛽
[ℎ(1) , ℎ(1) , ℎ(1) , ℎ(1) ]
(4) = 𝐿

+ 𝑀 𝛼𝛽 [ℎ(1) , ℎ(1) , ℎ(2) ] + 𝑀 𝛼𝛽 [ℎ(1) , ℎ(2) , ℎ(1) ] + 𝑀 𝛼𝛽 [ℎ(2) , ℎ(1) , ℎ(1) ]
+ 𝑁 𝛼𝛽 [ℎ(2) , ℎ(2) ] + 𝑁 𝛼𝛽 [ℎ(1) , ℎ(3) ] + 𝑁 𝛼𝛽 [ℎ(3) , ℎ(1) ] ,
..
.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(40c)

## PDF page 29

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

29

The quadratic, cubic and quartic pieces of Λ𝛼𝛽 are defined by Eq. (25) – (26).
Let us now proceed by induction. Some 𝑛 ∈ N being given, we assume that we succeeded in
constructing, starting from the linearized solution ℎ(1) , the sequence of post-Minkowskian solutions
ℎ(2) , ℎ(3) , . . . , ℎ(𝑛−1) , and from this we want to infer the next solution ℎ(𝑛) . The right-hand side
of Eq. (39a), Λ𝛼𝛽
(𝑛) , is known by induction hypothesis. Thus the problem is that of solving a flat
wave equation whose source is given. The point is that this wave equation, instead of being valid
everywhere in R3 , is physically correct only outside the matter source (𝑟 > 𝑎), and it makes no
sense to solve it by means of the usual retarded integral. Technically speaking, the right-hand side
of Eq. (39a) is composed of the product of many multipole expansions, which are singular at the
origin of the spatial coordinates 𝑟 = 0, and which make the retarded integral divergent at that
point. This does not mean that there are no solutions to the wave equation, but simply that the
retarded integral does not constitute the appropriate solution in that context.
What we need is a solution which takes the same structure as the source term Λ𝛼𝛽
(𝑛) , i.e., is
expanded into multipole contributions, with a singularity at 𝑟 = 0, and satisfies the d’Alembertian
equation as soon as 𝑟 > 0. Such a particular solution can be obtained, following the method
of Ref. [57], by means of a mathematical trick, in which one first “regularizes” the source term
𝐵
Λ𝛼𝛽
(𝑛) by multiplying it by the factor 𝑟 , where 𝑟 = |x| is the spatial radial distance and 𝐵 is a
complex number, 𝐵 ∈ C. Let us assume, for definiteness, that Λ𝛼𝛽
(𝑛) is composed of multipolar
pieces with maximal multipolarity ℓmax . This means that we start the iteration from the linearized
metric (35) – (37) in which the multipolar sums are actually finite.19 The divergences when 𝑟 → 0
of the source term are typically power-like, say 1/𝑟𝑘 (there are also powers of the logarithm of
𝑟), and with the previous assumption there will exist a maximal order of divergency, say 𝑘max .
Thus, when the real part of 𝐵 is large enough, i.e., ℜ(𝐵) > 𝑘max − 3, the “regularized” source
term 𝑟𝐵 Λ𝛼𝛽
(𝑛) is regular enough when 𝑟 → 0 so that one can perfectly apply the retarded integral
operator. This defines the 𝐵-dependent retarded integral, when ℜ(𝐵) is large enough,
[︁
]︁
𝐼 𝛼𝛽 (𝐵) ≡ −1
̃︀𝐵 Λ𝛼𝛽
(41)
ret 𝑟
(𝑛) ,
where the symbol −1
ret stands for the retarded integral defined by Eq. (31). It is convenient to
introduce inside the regularizing factor some arbitrary constant length scale 𝑟0 in order to make it
dimensionless. Everywhere in this article we pose
𝑟̃︀ ≡

𝑟
.
𝑟0

(42)

The fate of the constant 𝑟0 in a detailed calculation will be interesting to follow, as we shall see.
Now the point for our purpose is that the function 𝐼 𝛼𝛽 (𝐵) on the complex plane, which was
originally defined only when ℜ(𝐵) > 𝑘max − 3, admits a unique analytic continuation to all values
of 𝐵 ∈ C except at some integer values. Furthermore, the analytic continuation of 𝐼 𝛼𝛽 (𝐵) can be
expanded, when 𝐵 → 0 (namely the limit of interest to us) into a Laurent expansion involving
in general some multiple poles. The key idea, as we shall prove, is that the finite part, or the
coefficient of the zeroth power of 𝐵 in that expansion, represents the particular solution we are
looking for. We write the Laurent expansion of 𝐼 𝛼𝛽 (𝐵), when 𝐵 → 0, in the form
𝐼

𝛼𝛽

(𝐵) =

+∞
∑︁

𝑝
𝜄𝛼𝛽
𝑝 𝐵 ,

(43)

𝑝=𝑝0
19 This assumption is justified because we are ultimately interested in the radiation field at some given finite

post-Newtonian precision like 3PN, and because only a finite number of multipole moments can contribute at any
finite order of approximation. With a finite number of multipoles in the linearized metric (35) – (37), there is a
maximal multipolarity ℓmax (𝑛) at any post-Minkowskian order 𝑛, which grows linearly with 𝑛.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 30

30

Luc Blanchet

where 𝑝 ∈ Z, and the various coefficients 𝜄𝛼𝛽
𝑝 are functions of the field point (x, 𝑡). When 𝑝0 ⩽ −1
there are poles; and −𝑝0 , which depends on 𝑛, refers to the maximal order of these poles. By
applying the d’Alembertian operator onto both sides of Eq. (43), and equating the different powers
of 𝐵, we arrive at
𝑝0 ⩽ 𝑝 ⩽ −1

=⇒

𝜄𝛼𝛽
𝑝 = 0,

(44a)
𝑝

𝑝⩾0

=⇒

𝜄𝛼𝛽
𝑝 =

(ln 𝑟) 𝛼𝛽
Λ(𝑛) .
𝑝!

(44b)

As we see, the case 𝑝 = 0 shows that the finite-part coefficient in Eq. (43), namely 𝜄𝛼𝛽
0 , is a
𝛼𝛽
.
Furthermore,
we
can
prove
that
this
=
Λ
particular solution of the requested equation: 𝜄𝛼𝛽
0
(𝑛)
solution, by its very construction, owns the same structure made of a multipolar expansion singular
at 𝑟 = 0 as the corresponding source.
Let us forget about the intermediate name 𝜄𝛼𝛽
0 , and denote, from now on, the latter solution
𝛼𝛽
by 𝑢𝛼𝛽
≡
𝜄
,
or,
in
more
explicit
terms,
0
(𝑛)
[︁
]︁
−1
𝐵 𝛼𝛽
𝑢𝛼𝛽
=
ℱ𝒫

𝑟
̃︀
Λ
𝐵=0
ret
(𝑛)
(𝑛) ,

(45)

where the finite-part symbol ℱ𝒫 𝐵=0 means the previously detailed operations of considering the
analytic continuation, taking the Laurent expansion, and picking up the finite-part coefficient when
𝐵 → 0. The story is not complete, however, because 𝑢𝛼𝛽
(𝑛) does not fulfill the constraint of harmonic
𝛼
coordinates (39b); its divergence, say 𝑤(𝑛)
= 𝜕𝜇 𝑢𝛼𝜇
,
(𝑛) is different from zero in general. From the
fact that the source term is divergence-free in vacuum, 𝜕𝜇 Λ𝛼𝜇
(𝑛) = 0 [see Eq. (28)], we find instead
[︁
]︁
𝛼
𝐵 𝑛𝑖 𝛼𝑖
𝑤(𝑛)
= ℱ𝒫 𝐵=0 −1
𝐵
𝑟
̃︀
Λ
.
ret
𝑟 (𝑛)

(46)

𝛼
The factor 𝐵 comes from the differentiation of the regularization factor 𝑟̃︀𝐵 . So, 𝑤(𝑛)
is zero only
in the special case where the Laurent expansion of the retarded integral in Eq. (46) does not
develop any simple pole when 𝐵 → 0. Fortunately, when it does, the structure of the pole is quite
easy to control. We find that it necessarily consists of an homogeneous solution of the source-free
d’Alembertian equation, and, what is more (from its stationarity in the past), that solution is
𝛼
a retarded one. Hence, taking into account the index structure of 𝑤(𝑛)
, there must exist four
STF-tensorial functions of 𝑢 = 𝑡 − 𝑟/𝑐, say 𝑁𝐿 (𝑢), 𝑃𝐿 (𝑢), 𝑄𝐿 (𝑢) and 𝑅𝐿 (𝑢), such that

0
𝑤(𝑛)
=

𝑖
𝑤(𝑛)
=

+∞
∑︁
𝑙=0
+∞
∑︁

[︀
]︀
𝜕𝐿 𝑟−1 𝑁𝐿 (𝑢) ,

(47a)

∑︁ {︀
[︀
]︀ +∞
[︀
]︀
[︀
]︀}︀
𝜕𝑖𝐿 𝑟−1 𝑃𝐿 (𝑢) +
𝜕𝐿−1 𝑟−1 𝑄𝑖𝐿−1 (𝑢) + 𝜖𝑖𝑎𝑏 𝜕𝑎𝐿−1 𝑟−1 𝑅𝑏𝐿−1 (𝑢) .

𝑙=0

(47b)

𝑙=1

𝛼𝛽
From that expression we are able to find a new object, say 𝑣(𝑛)
, which takes the same structure
𝛼
as 𝑤(𝑛) (a retarded solution of the source-free wave equation) and, furthermore, whose divergence
𝛼𝜇
𝛼𝛽
𝛼
is exactly the opposite of the divergence of 𝑢𝛼𝛽
(𝑛) , i.e. 𝜕𝜇 𝑣(𝑛) = −𝑤(𝑛) . Such a 𝑣(𝑛) is not unique,
𝛼𝛽
but we shall see that it is simply necessary to make a choice for 𝑣(𝑛)
(the simplest one) in order to
obtain the general solution. The formulas that we adopt are
[︁
(︁
)︁]︁
00
𝑣(𝑛)
= −𝑟−1 𝑁 (−1) + 𝜕𝑎 𝑟−1 −𝑁𝑎(−1) + 𝐶𝑎(−2) − 3𝑃𝑎 ,
(48a)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 31

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

0𝑖
= 𝑟−1
𝑣(𝑛)

(︁

(−1)
(1)
−𝑄𝑖
+ 3𝑃𝑖

)︁

[︁

− 𝜖𝑖𝑎𝑏 𝜕𝑎 𝑟

−1

(−1)
𝑅𝑏

]︁

−

+∞
∑︁

[︀
]︀
𝜕𝐿−1 𝑟−1 𝑁𝑖𝐿−1 ,

31

(48b)

𝑙=2
𝑖𝑗
= −𝛿𝑖𝑗 𝑟−1 𝑃 +
𝑣(𝑛)

+∞{︂
∑︁
[︀
]︀
[︀
]︀
2𝛿𝑖𝑗 𝜕𝐿−1 𝑟−1 𝑃𝐿−1 − 6𝜕𝐿−2(𝑖 𝑟−1 𝑃𝑗)𝐿−2

(48c)

𝑙=2

}︂
[︁
]︁
[︀
]︀
(1)
(2)
+ 𝜕𝐿−2 𝑟−1 (𝑁𝑖𝑗𝐿−2 + 3𝑃𝑖𝑗𝐿−2 − 𝑄𝑖𝑗𝐿−2 ) − 2𝜕𝑎𝐿−2 𝑟−1 𝜖𝑎𝑏(𝑖 𝑅𝑗)𝑏𝐿−2 .
∫︀ 𝑢
Notice the presence of anti-derivatives, denoted e.g., by 𝑁 (−1) (𝑢) = −∞ d𝑣 𝑁 (𝑣); there is no
problem with the limit 𝑣 → −∞ since all the corresponding functions are zero when 𝑡 ⩽ −𝒯 .
The choice made in Eqs. (48) is dictated by the fact that the 00 component involves only some
𝑖𝑖
monopolar and dipolar terms, and that the spatial trace 𝑖𝑖 is monopolar: 𝑣(𝑛)
= −3𝑟−1 𝑃 . Finally,
if we pose
𝛼𝛽
𝛼𝛽
(49)
ℎ𝛼𝛽
(𝑛) = 𝑢(𝑛) + 𝑣(𝑛) ,
we see that we solve at once the d’Alembertian equation (39a) and the coordinate condition (39b).
That is, we have succeeded in finding a solution of the field equations at the 𝑛-th post-Minkowskian
order. By induction the same method applies to any order 𝑛, and, therefore, we have constructed
a complete post-Minkowskian series (38) based on the linearized approximation ℎ𝛼𝛽
(1) given by
Eqs. (35) – (37). The previous procedure constitutes an algorithm, which can be (and has recently
been [74, 197]) implemented by an algebraic computer programme. Again, note that this algorithm
permits solving the full Einstein field equations together with the gauge condition (i.e., not only
the relaxed field equations).

2.4

Generality of the MPM solution

We have a solution, but is that a general solution? The answer, “yes”, is provided by the following
result [57].
Theorem 2. The most general solution of the harmonic-coordinates Einstein field equations in
the vacuum region outside an isolated source, admitting some post-Minkowskian and multipolar
expansions, is given by the previous construction as
ℎ𝛼𝛽
ext =

+∞
∑︁

𝐺𝑛 ℎ𝛼𝛽
(𝑛) [I𝐿 , J𝐿 , . . . , Z𝐿 ] .

(50)

𝑛=1

It depends on two sets of arbitrary STF-tensorial functions of time I𝐿 (𝑢) and J𝐿 (𝑢) (satisfying the
conservation laws) defined by Eqs. (36), and on four supplementary functions W𝐿 (𝑢), . . . , Z𝐿 (𝑢)
parametrizing the gauge vector (37).
The proof is quite easy. With Eq. (49) we obtained a particular solution of the system of equations (39). To it we should add the most general solution of the corresponding homogeneous system
of equations, which is obtained by setting Λ𝛼𝛽
(𝑛) = 0 into Eqs. (39). But this homogeneous system
of equations is nothing but the linearized vacuum field equations (33), to which we know the most
𝛼𝛽
general solution ℎ𝛼𝛽
(1) given by Eqs. (35) – (37). Thus, we must add to our particular solution ℎ(𝑛) a
general homogeneous solution that is necessarily of the type ℎ𝛼𝛽
(1) [𝛿I𝐿 , . . . , 𝛿Z𝐿 ], where 𝛿I𝐿 , . . . , 𝛿Z𝐿
denote some corrections to the multipole moments at the 𝑛-th post-Minkowskian order (with the
monopole 𝛿I and dipoles 𝛿I𝑖 , 𝛿J𝑖 being constant). It is then clear, since precisely the linearized
metric is a linear functional of all these moments, that the previous corrections to the moments
can be absorbed into a re-definition of the original ones I𝐿 , . . . , Z𝐿 by posing
Inew
= I𝐿 + 𝐺𝑛−1 𝛿I𝐿 ,
𝐿

(51a)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 32

32

Luc Blanchet

..
.
Znew
= Z𝐿 + 𝐺𝑛−1 𝛿Z𝐿 .
𝐿

(51b)

After re-arranging the metric in terms of these new moments, taking into account the fact that the
precision of the metric is limited to the 𝑛-th post-Minkowskian order, and dropping the superscript
“new”, we find exactly the same solution as the one we had before (indeed, the moments are
arbitrary functions of time) – hence the proof.
The six sets of multipole moments I𝐿 (𝑢), . . . , Z𝐿 (𝑢) contain the physical information about any
isolated source as seen in its exterior. However, as we now discuss, it is always possible to find two,
and only two, sets of multipole moments, M𝐿 (𝑢) and S𝐿 (𝑢), for parametrizing the most general
isolated source as well. The route for constructing such a general solution is to get rid of the
moments W𝐿 , X𝐿 , Y𝐿 , Z𝐿 at the linearized level by performing the linearized gauge transformation
𝛼
𝛿𝑥𝛼 = 𝜙𝛼
(1) , where 𝜙(1) is the gauge vector given by Eqs. (37). So, at the linearized level, we have
𝛼𝛽
by the same formulas as in Eqs. (36).
only the two types of moments M𝐿 and S𝐿 , parametrizing 𝑘(1)
We must be careful to denote these moments with names different from I𝐿 and J𝐿 because they
will ultimately correspond to a different physical source. Then we apply exactly the same postMinkowskian algorithm, following the formulas (45) – (49) as we did above, but starting from the
𝛼𝛽
gauge-transformed linear metric 𝑘(1)
instead of ℎ𝛼𝛽
(1) . The result of the iteration is therefore some

𝛼𝛽
𝑘ext
=

+∞
∑︁

𝛼𝛽
𝐺𝑛 𝑘(𝑛)
[M𝐿 , S𝐿 ] .

(52)

𝑛=1

Obviously this post-Minkowskian algorithm yields some simpler calculations as we have only two
multipole moments to iterate. The point is that one can show that the resulting metric (52)
is isometric to the original one (50) if and only if the so-called canonical moments M𝐿 and S𝐿
are related to the source moments I𝐿 , J𝐿 , . . . , Z𝐿 by some (quite involved) non-linear equations.
We shall give in Eqs. (97) – (98) the most up to date relations we have between these moments.
Therefore, the most general solution of the field equations, modulo a coordinate transformation,
𝛼𝛽
can be obtained by starting from the linearized metric 𝑘(1)
[M𝐿 , S𝐿 ] instead of the more complicated
𝛼𝛽
𝛼𝛽
𝑘(1)
[I𝐿 , J𝐿 ] + 𝜕 𝛼 𝜙𝛽(1) + 𝜕 𝛽 𝜙𝛼
𝜕𝜇 𝜙𝜇(1) , and continuing the post-Minkowskian calculation.
(1) − 𝜂

So why not consider from the start that the best description of the isolated source is provided by
only the two types of multipole moments, M𝐿 and S𝐿 , instead of the six types, I𝐿 , J𝐿 , . . . , Z𝐿 ? The
reason is that we shall determine in Theorem 6 below the explicit closed-form expressions of the
six source moments I𝐿 , J𝐿 , . . . , Z𝐿 , but that, by contrast, it seems to be impossible to obtain some
similar closed-form expressions for the canonical moments M𝐿 and S𝐿 . The only thing we can do is
to write down the explicit non-linear algorithm that computes M𝐿 , S𝐿 starting from I𝐿 , J𝐿 , . . . , Z𝐿 .
In consequence, it is better to view the moments I𝐿 , J𝐿 , . . . , Z𝐿 as more “fundamental” than M𝐿 and
S𝐿 , in the sense that they appear to be more tightly related to the description of the source, since
they admit closed-form expressions as some explicit integrals over the source. Hence, we choose to
refer collectively to the six moments I𝐿 , J𝐿 , . . . , Z𝐿 as the multipole moments of the source. This
being said, the moments M𝐿 and S𝐿 are generally very useful in practical computations because
they yield a simpler post-Minkowskian iteration. Then, one can generally come back to the more
fundamental source-rooted moments by using the fact that M𝐿 and S𝐿 differ from the corresponding
I𝐿 and J𝐿 only by high-order post-Newtonian terms like 2.5PN; see Eqs. (97) – (98) below. Indeed,
this is to be expected because the physical difference between both types of moments stems only
from non-linearities.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 33

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

2.5

33

Near-zone and far-zone structures

In our presentation of the post-Minkowskian algorithm (45) – (49) we have for the moment omitted
a crucial recursive hypothesis, which is required in order to prove that at each post-Minkowskian
order 𝑛, the inverse d’Alembertian operator can be applied in the way we did – notably that the
𝐵-dependent retarded integral can be analytically continued down to a neighbourhood of 𝐵 = 0.
This hypothesis is that the “near-zone” expansion, i.e., when 𝑟 → 0, of each one of the postMinkowskian coefficients ℎ(𝑛) has a certain structure (here we often omit the space-time indices
𝛼𝛽); this hypothesis is established as a theorem once the mathematical induction succeeds.
Theorem 3. The general structure of the expansion of the post-Minkowskian exterior metric in
the near-zone (when 𝑟 → 0) is of the type: ∀𝑁 ∈ N,20
ℎ(𝑛) (x, 𝑡) =

∑︁

𝑛𝐿 𝑟𝑚 (ln 𝑟)𝑝 𝐹𝐿,𝑚,𝑝,𝑛 (𝑡) + 𝑜(𝑟𝑁 ) ,
^

(53)

where 𝑚 ∈ Z, with 𝑚0 ⩽ 𝑚 ⩽ 𝑁 (and 𝑚0 becoming more and more negative as 𝑛 grows), 𝑝 ∈ N
with 𝑝 ⩽ 𝑛 − 1. The functions 𝐹𝐿,𝑚,𝑝,𝑛 are multilinear functionals of the source multipole moments
I𝐿 , . . . , Z𝐿 .
For the proof see Ref. [57]. As we see, the near-zone expansion involves, besides the simple powers
of 𝑟, some powers of the logarithm of 𝑟, with a maximal power of 𝑛 − 1. As a corollary of that
theorem, we find, by restoring all the powers of 𝑐 in Eq. (53) and using the fact that each 𝑟 goes
into the combination 𝑟/𝑐, that the general structure of the post-Newtonian expansion (𝑐 → +∞)
is necessarily of the type
∑︁ (ln 𝑐)𝑝
,
(54)
ℎ(𝑛) (𝑐) ≃
𝑐𝑞
𝑝,𝑞∈N

where 𝑝 ⩽ 𝑛 − 1 (and 𝑞 ⩾ 2). The post-Newtonian expansion proceeds not only with the normal
powers of 1/𝑐 but also with powers of the logarithm of 𝑐 [57]. It is remarkable that there is no
more complicated structure like for instance ln(ln 𝑐).
Paralleling the structure of the near-zone expansion, we have a similar result concerning the
structure of the far-zone expansion at Minkowskian future null infinity, i.e., when 𝑟 → +∞ with
𝑢 = 𝑡 − 𝑟/𝑐 = const: ∀𝑁 ∈ N,
(︂ )︂
∑︁ 𝑛
1
^ 𝐿 (ln 𝑟)𝑝
ℎ(𝑛) (x, 𝑡) =
𝐺
(𝑢)
+
𝑜
,
(55)
𝐿,𝑘,𝑝,𝑛
𝑘
𝑟
𝑟𝑁
where 𝑘, 𝑝 ∈ N, with 1 ⩽ 𝑘 ⩽ 𝑁 , and where, likewise in the near-zone expansion (53), some powers
of logarithms, such that 𝑝 ⩽ 𝑛−1, appear. The appearance of logarithms in the far-zone expansion
of the harmonic-coordinates metric has been known since the work of Fock [202]. One knows also
that this is a coordinate effect, because the study of the “asymptotic” structure of space-time
at future null infinity by Bondi et al. [93], Sachs [368], and Penrose [337, 338], has revealed the
existence of other coordinate systems that avoid the appearance of any logarithms: the so-called
radiative coordinates, in which the far-zone expansion of the metric proceeds with simple powers
of the inverse radial distance. Hence, the logarithms are simply an artifact of the use of harmonic
coordinates [252, 304, 41]. The following theorem, proved in Ref. [41], shows that our general
construction of the metric in the exterior of the source, when developed at future null infinity, is
consistent with the Bondi–Sachs–Penrose [93, 368, 337, 338] approach to gravitational radiation.
20 We employ the Landau symbol 𝑜 for remainders with its standard meaning. Thus, 𝑓 (𝑟) = 𝑜[𝑔(𝑟)] when 𝑟 → 0
means that 𝑓 (𝑟)/𝑔(𝑟) → 0 when 𝑟 → 0. Furthermore, we generally assume some differentiability properties such as
d𝑛 𝑓 (𝑟)/d𝑟𝑛 = 𝑜[𝑔(𝑟)/𝑟𝑛 ].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 34

34

Luc Blanchet

Theorem 4. The most general multipolar-post-Minkowskian solution, stationary in the past [see
Eq. (29)], admits some radiative coordinates (𝑇, X), for which the expansion at future null infinity,
𝑅 → +∞ with 𝑈 ≡ 𝑇 − 𝑅/𝑐 = const, takes the form
𝐻(𝑛) (X, 𝑇 ) =

∑︁ 𝑁
^𝐿
𝑅𝑘

(︂
𝐾𝐿,𝑘,𝑛 (𝑈 ) + 𝒪

1
𝑅𝑁

)︂
.

(56)

The functions 𝐾𝐿,𝑘,𝑛 are computable functionals of the source multipole moments. In radiative
𝛼𝛽
coordinates the retarded time 𝑈 is a null coordinate in the asymptotic limit. The metric 𝐻ext
=
∑︀
𝑛 𝛼𝛽
is
asymptotically
simple
in
the
sense
of
Penrose
[337,
338,
220],
perturbatively
to
𝐺
𝐻
𝑛⩾1
(𝑛)
any post-Minkowskian order.
Proof. We introduce a linearized “radiative” metric by performing a gauge transformation of the
harmonic-coordinates metric defined by Eqs. (35) – (37), namely
𝜇
𝛼𝛽
𝛼 𝛽
𝛽 𝛼
𝛼𝛽
,
𝜕𝜇 𝜉(1)
= ℎ𝛼𝛽
𝐻(1)
(1) + 𝜕 𝜉(1) + 𝜕 𝜉(1) − 𝜂

(57)

𝛼
where the gauge vector 𝜉(1)
is

2M
𝛼
𝜉(1)
= 2 𝜂 0𝛼 ln

(︂

𝑐

𝑟
𝑟0

)︂
.

(58)

This gauge transformation is non-harmonic:
𝛼𝜇
𝛼
𝜕𝜇 𝐻(1)
= 𝜉(1)
=

2M 0𝛼
𝜂 .
𝑐2 𝑟2

(59)

Its effect is to correct for the well-known logarithmic deviation of the retarded time in harmonic
coordinates, with respect to the true space-time characteristic or light cones. After the change of
gauge, the coordinate 𝑢 = 𝑡 − 𝑟/𝑐 coincides with a null coordinate at the linearized level.21 This
is the requirement to be satisfied by a linearized metric so that it can constitute the linearized
approximation to a full (post-Minkowskian) radiative field [304]. One can easily show that, at the
dominant order when 𝑟 → +∞,
(︂ )︂
1
𝜇𝜈
𝑘𝜇 𝑘𝜈 𝐻(1)
=𝒪
,
(60)
𝑟2
where 𝑘 𝜇 = 𝜂 𝜇𝜈 𝑘𝜈 = (1, n) is the outgoing Minkowskian null vector. Given any 𝑛 ⩾ 2, let us
recursively assume that we have obtained all the previous radiative post-Minkowskian coefficients
𝛼𝛽
𝐻(𝑚)
, i.e. ∀𝑚 ⩽ 𝑛 − 1, and that all of them satisfy
𝜇𝜈
𝑘𝜇 𝑘𝜈 𝐻(𝑚)
=𝒪

(︂

1
𝑟2

)︂
.

(61)

From this induction hypothesis one can prove that the 𝑛-th post-Minkowskian source term Λ𝛼𝛽
(𝑛) =
Λ𝛼𝛽
(𝑛) (𝐻(1) , . . . , 𝐻(𝑛−1) ) is such that
(︀
)︀
𝑘𝛼 𝑘𝛽
Λ𝛼𝛽
=
𝜎(𝑛) 𝑢, n + 𝒪
(𝑛)
2
𝑟

(︂

1
𝑟3

)︂
.

(62)

To the leading order this term takes the classic form of the stress-energy tensor of massless particles,
with 𝜎(𝑛) being proportional to the power in the massless waves. One can show that all the problems
21 In this proof the coordinates are considered as dummy variables denoted (𝑡, 𝑟). At the end, when we obtain
the radiative metric, we shall denote the associated radiative coordinates by (𝑇, 𝑅).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 35

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

35

with the appearance of logarithms come from the retarded integral of the terms in Eq. (62) that
behave like 1/𝑟2 : See indeed the integration formula (83), which behaves like ln 𝑟/𝑟 at infinity.
But now, thanks to the particular index structure of the term (62), we can correct for the effect
by adjusting the gauge at the 𝑛-th post-Minkowskian order. We pose, as a gauge vector,
]︂
[︂ 𝛼 ∫︁ 𝑢
−1 𝑘
𝛼
d𝑣 𝜎(𝑛) (𝑣, n) ,
(63)
𝜉(𝑛) = ℱ𝒫 ret
2𝑟2 −∞
where ℱ𝒫 refers to the same finite part operation as in Eq. (45). This vector is such that the
logarithms that will appear in the corresponding gauge terms cancel out the logarithms coming
from the retarded integral of the source term (62); see Ref. [41] for the details. Hence, to the 𝑛-th
post-Minkowskian order, we define the radiative metric as
𝛼𝛽
𝛽
𝜇
𝛼𝛽
𝛼𝛽
𝛼
+ 𝜕 𝛼 𝜉(𝑛)
+ 𝜕 𝛽 𝜉(𝑛)
− 𝜂 𝛼𝛽 𝜕𝜇 𝜉(𝑛)
.
+ 𝑉(𝑛)
= 𝑈(𝑛)
𝐻(𝑛)

(64)

𝛼𝛽
𝛼𝛽
𝛼𝛽
denote the quantities that are the analogues of 𝑢𝛼𝛽
and 𝑉(𝑛)
Here 𝑈(𝑛)
(𝑛) and 𝑣(𝑛) , which were
introduced into the harmonic-coordinates algorithm: See Eqs. (45) – (48). In particular, these
𝛼𝛽
𝛼𝛽
quantities are constructed in such a way that the sum 𝑈(𝑛)
+ 𝑉(𝑛)
is divergence-free, so we see that
the radiative metric does not obey the harmonic-gauge condition, but instead
∫︁
𝑘𝛼 𝑢
𝛼𝜇
𝛼
d𝑣 𝜎(𝑛) (𝑣, n) .
(65)
𝜕𝜇 𝐻(𝑛)
= 𝜉(𝑛)
= 2
2𝑟 −∞

The far-zone expansion of the latter metric is of the type (56), i.e., is free of any logarithms, and
the retarded time in these coordinates tends asymptotically toward a null coordinate at future null
infinity. The property of asymptotic simplicity, in the form given by Geroch & Horowitz [220], is
proved by introducing the usual conformal factor Ω = 1/𝑅 in radiative coordinates [41]. Finally,
it can be checked that the metric so constructed, which is a functional of the source multipole
moments I𝐿 , . . . , Z𝐿 (from the definition of the algorithm), is as general as the general harmoniccoordinate metric of Theorem 2, since it merely differs from it by a coordinate transformation
(𝑡, x) −→ (𝑇, X), where (𝑡, x) are the harmonic coordinates and (𝑇, X) the radiative ones, together
with a re-definition of the multipole moments.

3

Asymptotic Gravitational Waveform

3.1

The radiative multipole moments

The leading-order term 1/𝑅 of the metric in radiative coordinates (𝑇, X) as given in Theorem 4,
neglecting 𝒪(1/𝑅2 ), yields the operational definition of two sets of STF radiative multipole moments, mass-type U𝐿 (𝑈 ) and current-type V𝐿 (𝑈 ). As we have seen, radiative coordinates are
such that the retarded time 𝑈 ≡ 𝑇 − 𝑅/𝑐 becomes asymptotically a null coordinate at future null
infinity. The radiative moments are defined from the spatial components 𝑖𝑗 of the metric in a
transverse-traceless (TT) radiative coordinate system. By definition, we have [403]
+∞

∑︁ 1
4𝐺
𝒫
(𝑁
)
𝑖𝑗𝑎𝑏
𝑐2 𝑅
𝑐ℓ ℓ!
ℓ=2
(︂ )︂
1
+𝒪
.
𝑅2

TT
𝐻𝑖𝑗
(𝑈, X) =

{︂
𝑁𝐿−2 U𝑎𝑏𝐿−2 (𝑈 ) −

}︂
2ℓ
𝑁𝑐𝐿−2 𝜖𝑐𝑑(𝑎 V𝑏)𝑑𝐿−2 (𝑈 )
𝑐(ℓ + 1)
(66)

We have formally re-summed the whole post-Minkowskian series in Eq. (56) from 𝑛 = 1 up to
+∞. As before we denote for instance 𝑁𝐿−2 = 𝑁𝑖1 · · · 𝑁𝑖ℓ−2 and so on, where 𝑁𝑖 = (𝑁 )𝑖 and

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 36

36

Luc Blanchet

𝑁 = 𝑋/𝑅. The TT algebraic projection operator 𝒫𝑖𝑗𝑎𝑏 has already been defined at the occasion
of the quadrupole-moment formalism in Eq. (2); and obviously the multipole decomposition (66)
represents the generalization of the quadrupole formalism. Notice that the meaning of Eq. (66) is
for the moment rather empty, because we do not yet know how to relate the radiative moments to
the actual source parameters. Only at the Newtonian level do we know this relation, which is
(︂ )︂
1
(2)
(67)
U𝑖𝑗 (𝑈 ) = Q𝑖𝑗 (𝑈 ) + 𝒪 2 ,
𝑐
where Q𝑖𝑗 is the Newtonian quadrupole moment (3). Associated to the asymptotic waveform (66)
we can compute by standard methods the total energy flux ℱ = (d𝐸/d𝑈 )GW and angular momentum flux 𝒢𝑖 = (dJ𝑖 /d𝑈 )GW in gravitational waves [403]:
+∞
∑︁

{︂

}︂
(ℓ + 1)(ℓ + 2)
4ℓ(ℓ + 2)
(1) (1)
(1) (1)
U U + 2
V V
.
(68a)
ℱ=
𝑐2ℓ+1 (ℓ − 1)ℓℓ!(2ℓ + 1)!! 𝐿 𝐿
𝑐 (ℓ − 1)(ℓ + 1)!(2ℓ + 1)!! 𝐿 𝐿
ℓ=2
{︂
}︂
+∞
∑︁
𝐺
(ℓ + 1)(ℓ + 2)
4ℓ2 (ℓ + 2)
(1)
(1)
𝒢𝑖 = 𝜖𝑖𝑎𝑏
U𝑎𝐿−1 U𝑏𝐿−1 + 2
V𝑎𝐿−1 V𝑏𝐿−1 .
𝑐2ℓ+1 (ℓ − 1)ℓ!(2ℓ + 1)!!
𝑐 (ℓ − 1)(ℓ + 1)!(2ℓ + 1)!!
𝐺

ℓ=2

(68b)
Next we introduce two unit polarization vectors 𝑃 and 𝑄, orthogonal and transverse to the
direction of propagation 𝑁 (hence 𝑁𝑖 𝑁𝑗 + 𝑃𝑖 𝑃𝑗 + 𝑄𝑖 𝑄𝑗 = 𝛿𝑖𝑗 ). Our convention for the choice of
𝑃 and 𝑄 will be clarified in Section 9.4. Then the two “plus” and “cross” polarization states of
the asymptotic waveform are defined by
1
TT
(𝑃𝑖 𝑃𝑗 − 𝑄𝑖 𝑄𝑗 ) 𝐻𝑖𝑗
,
2
1
TT
ℎ× = (𝑃𝑖 𝑄𝑗 + 𝑃𝑗 𝑄𝑖 ) 𝐻𝑖𝑗
.
2
ℎ+ =

(69a)
(69b)

Although the multipole decomposition (66) is completely general, it will also be important, having in view the comparison between the post-Newtonian and numerical results (see for instance
Refs. [107, 34, 237, 97, 98]), to consider separately the various modes (ℓ, 𝑚) of the asymptotic
waveform as defined with respect to a basis of spin-weighted spherical harmonics of weight −2.
Those harmonics are function of the spherical angles (𝜃, 𝜑) defining the direction of propagation
𝑁 , and given by
√︂
2ℓ + 1 ℓ𝑚
ℓ𝑚
𝑌(−2) =
𝑑 (𝜃) 𝑒i 𝑚 𝜑 ,
(70a)
4𝜋
(︂
)︂2ℓ+𝑚−2𝑘−2(︂
)︂2𝑘−𝑚+2
𝑘2
∑︁
𝜃
𝜃
(−)𝑘 ℓ𝑚
𝑑 ℓ𝑚 =
𝑒𝑘
cos
sin
,
(70b)
𝑘!
2
2
𝑘=𝑘1
√︀
(ℓ + 𝑚)!(ℓ − 𝑚)!(ℓ + 2)!(ℓ − 2)!
ℓ𝑚
𝑒𝑘 =
,
(70c)
(𝑘 − 𝑚 + 2)!(ℓ + 𝑚 − 𝑘)!(ℓ − 𝑘 − 2)!
where 𝑘1 = max(0, 𝑚 − 2) and 𝑘2 = min(ℓ + 𝑚, ℓ − 2). We thus decompose ℎ+ and ℎ× onto the
basis of such spin-weighted spherical harmonics, which means (see e.g., [107, 272])
ℎ+ − iℎ× =

+∞ ∑︁
ℓ
∑︁
ℓ=2 𝑚=−ℓ

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

ℓ𝑚
ℎℓ𝑚 𝑌(−2)
(𝜃, 𝜑) .

(71)

## PDF page 37

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

37

Using the orthonormality properties of these harmonics we can invert the latter decomposition and
obtain the separate modes ℎℓ𝑚 from a surface integral,
∫︁
[︀
]︀ ℓ𝑚
ℎℓ𝑚 = dΩ ℎ+ − iℎ× 𝑌 (−2) (𝜃, 𝜑) ,
(72)
where the overline refers to the complex conjugation. On the other hand, we can also relate ℎℓ𝑚
to the radiative multipole moments U𝐿 and V𝐿 . The result is
[︂
]︂
𝐺
i ℓ𝑚
ℓ𝑚
ℓ𝑚
U − V
ℎ = −√
,
(73)
𝑐
2 𝑅 𝑐ℓ+2
where Uℓ𝑚 and Vℓ𝑚 denote the radiative mass and current moments in standard (non-STF) guise.
These are related to the STF moments by
√︃
(ℓ + 1)(ℓ + 2) ℓ𝑚
4
𝛼𝐿 U𝐿 ,
Uℓ𝑚 =
(74a)
ℓ!
2ℓ(ℓ − 1)
√︃
ℓ(ℓ + 2)
8
ℓ𝑚
𝛼ℓ𝑚 V𝐿 .
(74b)
V =−
ℓ! 2(ℓ + 1)(ℓ − 1) 𝐿
ℓ𝑚
Here 𝛼𝐿
denotes the STF tensor connecting together the usual basis of spherical harmonics 𝑌 ℓ𝑚
^𝐿 = 𝑁⟨𝑖 . . . 𝑁𝑖 ⟩ (where the brackets indicate the STF projection).
to the set of STF tensors 𝑁
1
ℓ
ℓ𝑚
^
Indeed both 𝑌
and 𝑁𝐿 are basis of an irreducible representation of weight ℓ of the rotation
group; the two basis are related by22

^𝐿 (𝜃, 𝜑) =
𝑁

ℓ
∑︁

ℓ𝑚 ℓ𝑚
𝛼𝐿
𝑌 (𝜃, 𝜑) ,

(75a)

(2ℓ + 1)!! ℓ𝑚 ^
𝛼𝐿 𝑁𝐿 (𝜃, 𝜑) .
4𝜋𝑙!

(75b)

𝑚=−ℓ

𝑌 ℓ𝑚 (𝜃, 𝜑) =

In Section 9.5 we shall present all the modes (ℓ, 𝑚) of gravitational waves from inspiralling compact
binaries up to 3PN order, and even 3.5PN order for the dominant mode (2, 2).

3.2

Gravitational-wave tails and tails-of-tails

We learned from Theorem 4 the general method which permits the computation of the radiative
multipole moments U𝐿 , V𝐿 in terms of the source moments I𝐿 , J𝐿 , . . . , Z𝐿 , or in terms of the
intermediate canonical moments M𝐿 , S𝐿 discussed in Section 2.4. We shall now show that the
relation between U𝐿 , V𝐿 and M𝐿 , S𝐿 (say) includes tail effects starting at the relative 1.5PN
order.
Tails are due to the back-scattering of multipolar waves off the Schwarzschild curvature generated by the total mass monopole M of the source. They correspond to the non-linear interaction
between M and the multipole moments M𝐿 and S𝐿 , and are given by some non-local integrals,
extending over the past history of the source. At the 1.5PN order we find [59, 44]
)︂
]︂
(︂ )︂
[︂ (︂
∫︁
2𝐺M +∞
𝑐𝜏
1
(ℓ)
(ℓ+2)
U𝐿 (𝑈 ) = M𝐿 (𝑈 ) + 3
d𝜏 M𝐿 (𝑈 − 𝜏 ) ln
+ 𝜅ℓ + 𝒪 5 ,
(76a)
𝑐
2𝑟
𝑐
0
0
22 The STF tensorial coefficient 𝛼ℓ𝑚 can be computed as 𝛼ℓ𝑚 =
𝐿
𝐿
ℓ𝑚 = (2ℓ+1)!! 𝛼ℓ𝑚 .
used in Refs. [403, 272] by 𝒴𝐿
𝐿
4𝜋𝑙!

∫︀

^𝐿 𝑌
dΩ 𝑁

ℓ𝑚

. Our notation is related to that

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 38

38

Luc Blanchet

2𝐺M
(ℓ)
V𝐿 (𝑈 ) = S𝐿 (𝑈 ) + 3
𝑐

[︂ (︂
)︂
]︂
(︂ )︂
∫︁ +∞
𝑐𝜏
1
(ℓ+2)
d𝜏 S𝐿 (𝑈 − 𝜏 ) ln
+ 𝜋ℓ + 𝒪 5 ,
2𝑟0
𝑐
0

(76b)

where 𝑟0 is the length scale introduced in Eq. (42), and the constants 𝜅ℓ and 𝜋ℓ are given by
ℓ−2

𝜅ℓ =

∑︁ 1
2ℓ2 + 5ℓ + 4
+
,
ℓ(ℓ + 1)(ℓ + 2)
𝑘

(77a)

𝑘=1

ℓ−1

𝜋ℓ =

∑︁ 1
ℓ−1
+
.
ℓ(ℓ + 1)
𝑘

(77b)

𝑘=1

𝛼
Recall from the gauge vector 𝜉(1)
found in Eq. (58) that the retarded time 𝑈 = 𝑇 −𝑅/𝑐 in radiative
coordinates is related to the retarded time 𝑢 = 𝑡 − 𝑟/𝑐 in harmonic coordinates by
(︂ )︂
(︀ )︀
𝑟
2𝐺M
𝑈 = 𝑢 − 3 ln
+ 𝒪 𝐺2 .
(78)
𝑐
𝑟0

Inserting 𝑈 as given by Eq. (78) into Eqs. (76) we obtain the radiative moments expressed in terms
of “source-rooted” harmonic coordinates (𝑡, 𝑟), e.g.,
(︂ )︂
∫︁
[︁ (︁ 𝑐𝜏 )︁
]︁
2𝐺M +∞
1
(ℓ+2)
(ℓ)
d𝜏 M𝐿 (𝑢 − 𝜏 ) ln
+ 𝜅ℓ + 𝒪 5 .
U𝐿 (𝑈 ) = M𝐿 (𝑢) + 3
(79)
𝑐
2𝑟
𝑐
0
The remainder 𝒪(𝐺2 ) in Eq. (78) is negligible here. This expression no longer depends on the
constant 𝑟0 , i.e., we find that 𝑟0 gets replaced by 𝑟. If we now replace the harmonic coordinates
(𝑡, 𝑟) to some new ones, such as, for instance, some “Schwarzschild-like” coordinates (𝑡′ , 𝑟′ ) such
that 𝑡′ = 𝑡 and 𝑟′ = 𝑟 + 𝐺M/𝑐2 (and 𝑢′ = 𝑢 − 𝐺M/𝑐3 ), we get
(︂ )︂
∫︁
]︁
[︁ (︁ 𝑐𝜏 )︁
1
2𝐺M +∞
(ℓ)
(𝑙+2)
′
+
𝜅
+
𝒪
U𝐿 (𝑈 ) = M𝐿 (𝑢′ ) + 3
d𝜏 M𝐿 (𝑢′ − 𝜏 ) ln
,
(80)
ℓ
′
5
𝑐
2𝑟
𝑐
0
where 𝜅′ℓ = 𝜅ℓ + 1/2. This shows that the constant 𝜅ℓ (and 𝜋ℓ as well) depends on the choice of
source-rooted coordinates (𝑡, 𝑟): For instance, we have 𝜅2 = 11/12 in harmonic coordinates from
Eq. (77a), but 𝜅′2 = 17/12 in Schwarzschild coordinates [345].
The tail integrals in Eqs. (76) involve all the instants from −∞ in the past up to the current
retarded time 𝑈 . However, strictly speaking, they do not extend up to infinite past, since we have
assumed in Eq. (29) that the metric is stationary before the date −𝒯 . The range of integration
of the tails is therefore limited a priori to the time interval [−𝒯 , 𝑈 ]. But now, once we have
derived the tail integrals, thanks to the latter technical assumption of stationarity in the past,
we can argue that the results are in fact valid in more general situations for which the field has
never been stationary. We have in mind the case of two bodies moving initially on some unbound
(hyperbolic-like) orbit, and which capture each other, because of the loss of energy by gravitational
radiation, to form a gravitationally bound system around time −𝒯 .
In this situation let us check, using a simple Newtonian model for the behaviour of the multipole
moment M𝐿 (𝑈 − 𝜏 ) when 𝜏 → +∞, that the tail integrals, when assumed to extend over the whole
time interval [−∞, 𝑈 ], remain perfectly well-defined (i.e., convergent) at the integration bound
𝜏 = +∞. Indeed it can be shown [180] that the motion of initially free particles interacting
gravitationally is given by 𝑥𝑖 (𝑈 − 𝜏 ) = 𝑉 𝑖 𝜏 + 𝑊 𝑖 ln 𝜏 + 𝑋 𝑖 + 𝑜(1), where 𝑉 𝑖 , 𝑊 𝑖 and 𝑋 𝑖 denote
constant vectors, and 𝑜(1) → 0 when 𝜏 → +∞. From that physical assumption we find that the
multipole moments behave when 𝜏 → +∞ like
M𝐿 (𝑈 − 𝜏 ) = 𝐴𝐿 𝜏 ℓ + 𝐵𝐿 𝜏 ℓ−1 ln 𝜏 + 𝐶𝐿 𝜏 ℓ−1 + 𝑜(𝜏 ℓ−1 ) ,

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(81)

## PDF page 39

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

39

where 𝐴𝐿 , 𝐵𝐿 and 𝐶𝐿 are constant tensors. We used the fact that the moment M𝐿 will agree at
the Newtonian level with the standard expression for the ℓ-th mass multipole moment Q𝐿 . The
appropriate time derivatives of the moment appearing in Eq. (76a) are therefore dominantly like
(ℓ+2)

M𝐿

(𝑈 − 𝜏 ) =

𝐷𝐿
+ 𝑜(𝜏 −3 ) ,
𝜏3

(82)

which ensures that the tail integral is convergent. This fact can be regarded as an a posteriori
justification of our a priori too restrictive assumption of stationarity in the past. Thus, this
assumption does not seem to yield any physical restriction on the applicability of the final formulas.
However, once again, we emphasize that the past-stationarity is appropriate for real astrophysical
sources of gravitational waves which have been formed at a finite instant in the past.
To obtain the results (76), we must implement in details the post-Minkowskian algorithm
presented in Section 2.3. Let us flash here some results obtained with such algorithm. Consider
first the case of the interaction between the constant mass monopole moment M (or ADM mass) and
the time-varying quadrupole moment M𝑖𝑗 . This coupling will represent the dominant non-static
multipole interaction in the waveform. For these moments we can write the linearized metric using
Eq. (35) in which by definition of the “canonical” construction we insert the canonical moments
M𝑖𝑗 in place of I𝑖𝑗 (notice that M = I). We must plug this linearized metric into the quadraticorder part 𝑁 𝛼𝛽 (ℎ, ℎ) of the gravitational source term (24) – (25) and explicitly given by Eq. (26).
This yields many terms; to integrate these following the algorithm [cf. Eq. (45)], we need some
explicit formulas for the retarded integral of an extended (non-compact-support) source having
some definite multipolarity ℓ. A thorough account of the technical formulas necessary for handling
the quadratic and cubic interactions is given in the Appendices of Refs. [50] and [48]. For the
present computation the most crucial formula, needed to control the tails, corresponds to a source
term behaving like 1/𝑟2 :
]︂
[︂
∫︁ +∞
^𝐿
−1 𝑛
F(𝑡 − 𝑟) = −^
𝑛𝐿
d𝑥 𝑄ℓ (𝑥)F(𝑡 − 𝑟𝑥) ,
(83)
ret
𝑟2
1
where F is any smooth function representing a time derivative of the quadrupole moment, and
𝑄ℓ denotes the Legendre function of the second kind.23 Note that there is no need to include a
finite part operation ℱ𝒫 in Eq. (83) as the integral is convergent. With the help of this and other
formulas we obtain successively the objects defined in this algorithm by Eqs. (45) – (48) and finally
obtain the quadratic metric (49) for that multipole interaction. The result is [60]24
]︁
M𝑛𝑎𝑏 [︁
(1)
2 (2)
3 (3)
ℎ00
−21M
−
21𝑟M
+
7𝑟
M
+
10𝑟
M
𝑎𝑏
(2) =
𝑎𝑏
𝑎𝑏
𝑎𝑏
𝑟4
∫︁ +∞
(4)
+ 8M𝑛𝑎𝑏
d𝑥 𝑄2 (𝑥)M𝑎𝑏 (𝑡 − 𝑟𝑥) ,
(84a)
1
[︂
]︂
1
M𝑛𝑖𝑎𝑏
(1)
(2)
(3)
−M𝑎𝑏 − 𝑟M𝑎𝑏 − 𝑟2 M𝑎𝑏
ℎ0𝑖
(2) =
3
𝑟
3
]︂
[︂
M𝑛𝑎
19 2 (3)
(1)
(2)
+ 3 −5M𝑎𝑖 − 5𝑟M𝑎𝑖 + 𝑟 M𝑎𝑖
𝑟
3
23 The function 𝑄 is given in terms of the Legendre polynomial 𝑃 by
ℓ
ℓ

𝑄ℓ (𝑥) =

1
2

∫︁ 1

d𝑧 𝑃ℓ (𝑧)
1
= 𝑃ℓ (𝑥) ln
2
−1 𝑥 − 𝑧

(︂

𝑥+1
𝑥−1

)︂
−

ℓ
∑︁
1
𝑗=1

𝑗

𝑃ℓ−𝑗 (𝑥)𝑃𝑗−1 (𝑥) .

In the complex plane there is a branch cut from −∞ to 1. The first equality is known as the Neumann formula for
the Legendre function.
24 We pose 𝑐 = 1 until the end of this section.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 40

40

Luc Blanchet

∫︁ +∞
(4)
d𝑥 𝑄1 (𝑥)M𝑎𝑖 (𝑡 − 𝑟𝑥) ,
1
[︂
]︂
M𝑛𝑖𝑗𝑎𝑏
15
15
1 3 (3)
(1)
𝑖𝑗
2 (2)
ℎ(2) =
− M𝑎𝑏 − 𝑟M𝑎𝑏 − 3𝑟 M𝑎𝑏 − 𝑟 M𝑎𝑏
𝑟4
2
2
2
[︂
]︂
1
1
11 3 (3)
M𝛿𝑖𝑗 𝑛𝑎𝑏
(1)
2 (2)
− M𝑎𝑏 − 𝑟M𝑎𝑏 − 2𝑟 M𝑎𝑏 − 𝑟 M𝑎𝑏
+
𝑟4
2
2
6
[︁
]︁
M𝑛𝑎(𝑖
(1)
2 (2)
3 (3)
6M
+
6𝑟M
+
6𝑟
M
+
4𝑟
M
+
𝑗)𝑎
𝑗)𝑎
𝑗)𝑎
𝑗)𝑎
𝑟[︂4
]︂
M
11
(1)
(2)
(3)
+ 4 −M𝑖𝑗 − 𝑟M𝑖𝑗 − 4𝑟2 M𝑖𝑗 − 𝑟3 M𝑖𝑗
𝑟
3
∫︁ +∞
(4)
+ 8M
d𝑥 𝑄0 (𝑥)M𝑖𝑗 (𝑡 − 𝑟𝑥) .
+ 8M𝑛𝑎

(84b)

(84c)

1

The metric is composed of two types of terms: “instantaneous” ones depending on the values of
the quadrupole moment at the retarded time 𝑢 = 𝑡 − 𝑟, and “hereditary” tail integrals, depending
on all previous instants 𝑡 − 𝑟𝑥 < 𝑢.
Let us investigate now the cubic interaction between two mass monopoles M with the mass
quadrupole M𝑖𝑗 . Obviously, the source term corresponding to this interaction will involve [see
Eq. (40b)] cubic products of three linear metrics, say ℎM × ℎM × ℎM𝑖𝑗 , and quadratic products
between one linear metric and one quadratic, say ℎM2 ×ℎM𝑖𝑗 and ℎM ×ℎMM𝑖𝑗 . The latter case is the
most tricky because the tails present in ℎMM𝑖𝑗 , which are given explicitly by Eqs. (84), will produce
in turn some tails of tails in the cubic metric ℎM2 M𝑖𝑗 . The computation is rather involved [48] but
can now be performed by an algebraic computer programme [74, 197]. Let us just mention the
most difficult of the needed integration formulas for this calculation:25
]︂
[︂
∫︁
∫︁ +∞
𝑛𝐿 +∞
−1 ^
d𝑥 𝑄𝑚 (𝑥)F(𝑡 − 𝑟𝑥) = 𝑛
^𝐿
d𝑦 F(−1) (𝑡 − 𝑟𝑦)
ℱ𝒫ret
𝑟 1
1
}︂
{︂
∫︁ +∞
∫︁ 𝑦
d𝑄ℓ
d𝑃ℓ
(𝑥) + 𝑃ℓ (𝑦)
d𝑥 𝑄𝑚 (𝑥)
(𝑥) ,
(85)
× 𝑄ℓ (𝑦)
d𝑥 𝑄𝑚 (𝑥)
d𝑥
d𝑥
𝑦
1
where F(−1) is the time anti-derivative of F. With this formula and others given in Ref. [48]
we are able to obtain the closed algebraic form of the cubic metric for the multipole interaction
M × M × M𝑖𝑗 , at the leading order when the distance to the source 𝑟 → ∞ with 𝑢 = const. The
result is26
[︂
∫︁
(︁ 𝜏 )︁
(︁ 𝜏 )︁ 116 (︂ 𝜏 )︂ 7136 ]︂
M2 𝑛𝑎𝑏 +∞
(5)
2
00
ℎ(3) =
d𝜏 M𝑎𝑏 −4 ln
− 4 ln
+
ln
−
𝑟
2𝑟
2𝑟
21
2𝑟0
2205
(︂ )︂ 0
1
+𝑜
,
(86a)
𝑟
[︂
(︂
)︂
]︂
∫︁
M2 ^
𝑛𝑖𝑎𝑏 +∞
2 (︁ 𝜏 )︁
4
𝜏
716
(5)
ℎ0𝑖
=
d𝜏
M
−
ln
−
ln
−
(3)
𝑎𝑏
𝑟
3
2𝑟
105
2𝑟0
1225
0
25 The equation (85) has been obtained using a not so well known mathematical relation between the Legendre
functions and polynomials:
∫︁
1 1
d𝑧 𝑃ℓ (𝑧)
√︀
= 𝑄ℓ (𝑥)𝑃ℓ (𝑦) ,
2 −1 (𝑥𝑦 − 𝑧)2 − (𝑥2 − 1)(𝑦 2 − 1)

where 1 ⩽ 𝑦 < 𝑥 is assumed. See Appendix A in Ref. [48] for the proof. This relation constitutes a generalization
of the Neumann formula (see the footnote 23).
26 The neglected remainders are indicated by 𝑜(1/𝑟) rather than 𝒪(1/𝑟 2 ) because they contain powers of the
logarithm of 𝑟; in fact they could be more accurately written as 𝑜(𝑟𝜖−2 ) for some 𝜖 ≪ 1.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 41

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

[︂
∫︁
(︁ 𝜏 )︁ 18 (︁ 𝜏 )︁ 416 (︂ 𝜏 )︂ 22724 ]︂
M2 𝑛𝑎 +∞
(5)
2
+
d𝜏 M𝑎𝑖 −4 ln
−
+
ln
ln
−
𝑟
2𝑟
5
2𝑟
75
2𝑟0
7875
(︂ )︂ 0
1
+𝑜
,
𝑟
[︂
∫︁
(︁ 𝜏 )︁ 191 ]︂
M2 ^
𝑛𝑖𝑗𝑎𝑏 +∞
(5)
d𝜏
M
−
ln
−
ℎ𝑖𝑗
=
𝑎𝑏
(3)
𝑟
2𝑟
210
0
[︂
(︂
)︂
]︂
∫︁ +∞
)︁
(︁
2
80
32
𝜏
𝜏
296
M 𝛿𝑖𝑗 𝑛𝑎𝑏
(5)
d𝜏 M𝑎𝑏 − ln
−
ln
−
+
𝑟
21
2𝑟
21
2𝑟0
35
0
[︂
(︂
)︂
]︂
∫︁ +∞
)︁
(︁
2
M ^
𝑛𝑎(𝑖
104
𝜏
𝜏
8812
(5) 52
d𝜏 M𝑗)𝑎
+
+
ln
ln
+
𝑟
7
2𝑟
35
2𝑟0
525
0
[︂
(︂
)︂
]︂
∫︁
+∞
)︁
)︁
(︁
(︁
2
M
24
76
𝜏
𝜏
𝜏
198
(5)
2
+
d𝜏 M𝑖𝑗 −4 ln
−
+
ln
ln
−
𝑟 0
2𝑟
5
2𝑟
15
2𝑟0
35
(︂ )︂
1
+𝑜
,
𝑟

41

(86b)

(86c)

where all the moments M𝑎𝑏 are evaluated at the instant 𝑢−𝜏 = 𝑡−𝑟−𝜏 . Notice that the logarithms
in Eqs. (86) contain either the ratio 𝜏 /𝑟 or 𝜏 /𝑟0 . We shall discuss in Eqs. (93) – (94) below the
interesting fate of the arbitrary constant 𝑟0 .
From Theorem 4, the presence of logarithms of 𝑟 in Eqs. (86) is an artifact of the harmonic
coordinates 𝑥𝛼 , and it is convenient to gauge them away by introducing radiative coordinates
𝑋 𝛼 at future null infinity. For controling the leading 1/𝑅 term at infinity, it is sufficient to
take into account the linearized logarithmic deviation of the light cones in harmonic coordinates:
𝛼
𝛼
𝑋 𝛼 = 𝑥𝛼 + 𝐺𝜉(1)
+ 𝒪(𝐺2 ), where 𝜉(1)
is the gauge vector defined by Eq. (58) [see also Eq. (78)].
With this coordinate change one removes the logarithms of 𝑟 in Eqs. (86) and we obtain the
radiative (or Bondi-type [93]) logarithmic-free expansion
[︂
]︂
(︂
)︂
(︂
)︂
∫︁
M2 𝑁𝑎𝑏 +∞
𝜏
𝜏
7136
(5)
d𝜏 M𝑎𝑏 −4 ln2
+ 3221 ln
−
𝑅
2𝑟0
2𝑟0
2205
(︂ )︂ 0
1
+𝒪
,
𝑅2
[︂
(︂
)︂
]︂
^𝑖𝑎𝑏 ∫︁ +∞
M2 𝑁
74
𝜏
716
(5)
0𝑖
𝐻(3) =
d𝜏 M𝑎𝑏 −
ln
−
𝑅
105
2𝑟0
1225
0
[︂
(︂
)︂
(︂
)︂
]︂
∫︁
+∞
2
M 𝑁𝑎
𝜏
146
𝜏
22724
(5)
2
+
d𝜏 M𝑎𝑖 −4 ln
+
ln
−
𝑅
2𝑟0
75
2𝑟0
7875
(︂ )︂0
1
+𝒪
,
𝑅2
[︂
(︂
)︂
]︂
^𝑖𝑗𝑎𝑏 ∫︁ +∞
M2 𝑁
𝜏
191
(5)
𝑖𝑗
𝐻(3)
=
d𝜏 M𝑎𝑏 − ln
−
𝑅
2𝑟0
210
0
[︂
(︂
)︂
]︂
∫︁ +∞
2
M 𝛿𝑖𝑗 𝑁𝑎𝑏
16
𝜏
296
(5)
+
d𝜏 M𝑎𝑏 − ln
−
𝑅
3
2𝑟0
35
0
[︂
(︂
)︂
]︂
∫︁ +∞
2 ^
M 𝑁𝑎(𝑖
𝜏
8812
(5) 52
+
d𝜏 M𝑗)𝑎
ln
+
𝑅
5
2𝑟0
525
0
[︂
(︂
)︂
(︂
)︂
]︂
∫︁
M2 +∞
𝜏
4
𝜏
198
(5)
+
d𝜏 M𝑖𝑗 −4 ln2
+
ln
−
𝑅 0
2𝑟0
15
2𝑟0
35
00
𝐻(3)
=

(87a)

(87b)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 42

42

Luc Blanchet

(︂
+𝒪

1
𝑅2

)︂
,

(87c)

where the moments are evaluated at time 𝑈 −𝜏 = 𝑇 −𝑅−𝜏 . It is trivial to compute the contribution
of the radiative moments corresponding to that metric. We find the “tail of tail” term which will
be reported in Eq. (91) below.

3.3

Radiative versus source moments

We first give the result for the radiative quadrupole moment U𝑖𝑗 expressed as a functional of the
intermediate canonical moments M𝐿 , S𝐿 up to 3.5PN order included. The long calculation follows
from implementing the explicit MPM algorithm of Section 2.3 and yields various types of terms:
(︂ )︂
1
inst
tail
tail-tail
mem
(88)
U𝑖𝑗 = U𝑖𝑗 + U𝑖𝑗 + U𝑖𝑗
+ U𝑖𝑗 + 𝒪 8 .
𝑐
up to 3.5PN order reads
1. The instantaneous (i.e., non-hereditary) piece Uinst
𝑖𝑗
(2)

Uinst
𝑖𝑗 = M𝑖𝑗
[︂
]︂
𝐺 1 (5)
5 (4) (1) 2 (3) (2) 1
(4)
+ 5 M𝑎⟨𝑖 M𝑗⟩𝑎 − M𝑎⟨𝑖 M𝑗⟩𝑎 − M𝑎⟨𝑖 M𝑗⟩𝑎 + 𝜖𝑎𝑏⟨𝑖 M𝑗⟩𝑎 S𝑏
𝑐 7
7
7
3
[︂
5
19 (3) (4)
𝐺
64 (2) (3) 1957 (3) (4)
(3)
(4)
M M +
M M
+
M M
+ 7 − S𝑎⟨𝑖 S𝑗⟩𝑎 +
𝑐
63
3024 𝑖𝑗𝑎𝑏 𝑎𝑏
2268 𝑎𝑏⟨𝑖 𝑗⟩𝑎𝑏 648 𝑎𝑏 𝑖𝑗𝑎𝑏
16 (1) (4) 1685 (2) (5)
5
5
(2)
(5)
(2) (5)
+ S𝑎⟨𝑖 S𝑗⟩𝑎 +
M𝑖𝑗𝑎𝑏 M𝑎𝑏 +
M𝑎𝑏⟨𝑖 M𝑗⟩𝑎𝑏 −
M M
63
1008
126
756 𝑎𝑏 𝑖𝑗𝑎𝑏
80
5
41 (1) (6)
5
(5)
(5)
(1)
(6)
+ S𝑎⟨𝑖 S𝑗⟩𝑎 + S𝑎 S𝑖𝑗𝑎 + M𝑖𝑗𝑎𝑏 M𝑎𝑏 +
M M
63
42
28
189 𝑎𝑏⟨𝑖 𝑗⟩𝑎𝑏
1
91
5
1
(1) (6)
(7)
(7)
(7)
+
M𝑎𝑏 M𝑖𝑗𝑎𝑏 +
M𝑖𝑗𝑎𝑏 M𝑎𝑏 −
M𝑎𝑏⟨𝑖 M𝑗⟩𝑎𝑏 −
M𝑎𝑏 M𝑖𝑗𝑎𝑏
432
216
252
432
(︁ 32
1 (3) (3)
3 (2) (4)
10 (2) (4)
(3) (3)
M𝑗⟩𝑏𝑐 S𝑎𝑏 − M𝑎𝑏 S𝑗⟩𝑏𝑐 + S𝑗⟩𝑏𝑐 M𝑎𝑏 +
S M
+ 𝜖𝑎𝑐⟨𝑖
189
6
56
189 𝑎𝑏 𝑗⟩𝑏𝑐
65 (2) (4)
1 (2) (4)
187 (1) (5)
1 (1) (5)
+
M𝑗⟩𝑏𝑐 S𝑎𝑏 + M𝑎𝑏 S𝑗⟩𝑏𝑐 +
S𝑗⟩𝑏𝑐 M𝑎𝑏 −
S M
189
28
168
189 𝑎𝑏 𝑗⟩𝑏𝑐
5
1 (1) (5)
65
1
(1) (5)
(6)
(6)
−
M𝑗⟩𝑏𝑐 S𝑎𝑏 + M𝑎𝑏 S𝑗⟩𝑏𝑐 + S𝑗⟩𝑏𝑐 M𝑎𝑏 +
S𝑎𝑏 M𝑗⟩𝑏𝑐
189
24
84
189
)︁]︂
10
1
(6)
(6)
− M𝑗⟩𝑏𝑐 S𝑎𝑏 +
M𝑎𝑏 S𝑗⟩𝑏𝑐 .
63
168

(89)

The Newtonian term in this expression contains the Newtonian quadrupole moment Q𝑖𝑗 and
recovers the standard quadrupole formalism [see Eq. (67)];
2. The hereditary tail integral Utail
𝑖𝑗 is made of the dominant tail term at 1.5PN order in agreement with Eq. (76a) above:
Utail
𝑖𝑗 =

2𝐺M
𝑐3

∫︁ +∞
0

[︂ (︂
)︂
]︂
𝑐𝜏
11
(4)
d𝜏 ln
+
M𝑖𝑗 (𝑈 − 𝜏 ) .
2𝑟0
12

(90)

The length scale 𝑟0 is the one that enters our definition of the finite-part operation ℱ𝒫 [see
Eq. (42)] and it enters also the relation between the radiative and harmonic retarded times
given by Eq. (78);

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 43

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

43

3. The hereditary tail-of-tail term appears dominantly at 3PN order [48] and is issued from the
radiative metric computed in Eqs. (87):
Utail-tail
=2
𝑖𝑗

(︂

𝐺M
𝑐3

)︂2 ∫︁ +∞
0

[︂ (︂
)︂
(︂
)︂
]︂
𝑐𝜏
57
𝑐𝜏
124627
(5)
d𝜏 ln2
+
ln
+
M𝑖𝑗 (𝑈 − 𝜏 ) ;
2𝑟0
70
2𝑟0
44100

(91)

contributes at orders 2.5PN and 3.5PN and
4. Finally the memory-type hereditary piece Umem
𝑖𝑗
is given by
[︂
]︂
∫︁
𝐺
2 +∞
(3)
(3)
Umem
=
−
d𝜏
M
M
(𝑈
−
𝜏
)
(92)
𝑖𝑗
𝑎⟨𝑖
𝑗⟩𝑎
𝑐5
7 0
[︂
∫︁
∫︁ +∞
32 +∞
5
𝐺
(3) (3)
(4)
(4)
d𝜏 S𝑎⟨𝑖 S𝑗⟩𝑎 (𝑈 − 𝜏 ) −
d𝜏 M𝑎𝑏 M𝑖𝑗𝑎𝑏 (𝑈 − 𝜏 )
+ 7 −
𝑐
63 0
756 0
]︂
∫︁ +∞
∫︁ +∞
20
5
(4)
(3)
(3) (4)
−
d𝜏 S𝑎𝑐 M𝑗⟩𝑏𝑐 (𝑈 − 𝜏 ) +
d𝜏 M𝑎𝑐 S𝑗⟩𝑏𝑐 (𝑈 − 𝜏 ) .
𝜖𝑎𝑏⟨𝑖
𝜖𝑎𝑏⟨𝑖
189
42
0
0
The 2.5PN non-linear memory integral – the first term inside the coefficient of 𝐺/𝑐5 – has been
obtained using both post-Newtonian methods [42, 427, 406, 60, 50] and rigorous studies of the field
at future null infinity [128]. The expression (92) is in agreement with the more recent computation
of the non-linear memory up to any post-Newtonian order in Refs. [189, 192].
Be careful to note that the latter post-Newtonian orders correspond to “relative” orders when
counted in the local radiation-reaction force, present in the equations of motion: For instance, the
1.5PN tail integral in Eq. (90) is due to a 4PN radiative effect in the equations of motion [58];
similarly, the 3PN tail-of-tail integral is expected to be associated with some radiation-reaction
terms occurring at the 5.5PN order.
Note that U𝑖𝑗 , when expressed in terms of the intermediate moments M𝐿 and S𝐿 , shows a
dependence on the (arbitrary) length scale 𝑟0 ; cf. the tail and tail-of-tail contributions (90) – (91).
Most of this dependence comes from our definition of a radiative coordinate system as given by (78).
Exactly as we have done for the 1.5PN tail term in Eq. (79), we can remove most of the 𝑟0 ’s by
inserting 𝑈 = 𝑢 − 2𝐺M
𝑐3 ln(𝑟/𝑟0 ) back into (89) – (92), and expanding the result when 𝑐 → ∞,
keeping the necessary terms consistently. In doing so one finds that there remains a 𝑟0 -dependent
term at the 3PN order, namely
(2)

U𝑖𝑗 = M𝑖𝑗 (𝑢) −

214
ln
105

(︂

𝑟
𝑟0

)︂ (︂

𝐺M
𝑐3

)︂2

(4)

M𝑖𝑗 (𝑢) + terms independent of 𝑟0 .

(93)

However, the latter dependence on 𝑟0 is fictitious and should in fine disappear. The reason is that
when we compute explicitly the mass quadrupole moment M𝑖𝑗 for a given matter source, we will
find an extra contribution depending on 𝑟0 occurring at the 3PN order which will cancel out the
one in Eq. (93). Indeed we shall compute the source quadrupole moment I𝑖𝑗 of compact binaries at
the 3PN order, and we do observe on the result (300) – (301) below the requested terms depending
on 𝑟0 , namely27
M𝑖𝑗 = Q𝑖𝑗 +

214
ln
105

(︂

𝑟12
𝑟0

)︂ (︂

𝐺𝑚
𝑐3

)︂2

(2)

Q𝑖𝑗 + terms independent of 𝑟0 .

(94)

where Q𝑖𝑗 = 𝜇 𝑥
^𝑖𝑗 denotes the Newtonian quadrupole, 𝑟12 is the separation between the particles,
and 𝑚 is the total mass differing from the ADM mass M by small post-Newtonian corrections.
27 The canonical moment M

𝑖𝑗 differs from the source moment I𝑖𝑗 by small 2.5PN and 3.5PN terms; see Eq. (97).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 44

44

Luc Blanchet

Combining Eqs. (93) and (94) we see that the 𝑟0 -dependent terms cancel as expected. The appearance of a logarithm and its associated constant 𝑟0 at the 3PN order was pointed out in Ref. [7]; it
was rederived within the present formalism in Refs. [58, 48]. Recently a result equivalent to Eq. (93)
was obtained by means of the EFT approach using considerations related to the renormalization
group equation [222].
The previous formulas for the 3.5PN radiative quadrupole moment permit to compute the
dominant mode (2, 2) of the waveform up to order 3.5PN [197]; however, to control the full waveform
one has also to take into account the contributions of higher-order radiative moments. Here we list
the most accurate results we have for all the moments that permit the derivation of the waveform
up to order 3PN [74]:28
[︂ (︂
)︂
]︂
∫︁
𝑐𝜏
97
2𝐺𝑀 +∞
(5)
(3)
d𝜏
ln
+
M𝑖𝑗𝑘 (𝑈 − 𝜏 )
U𝑖𝑗𝑘 (𝑈 ) = M𝑖𝑗𝑘 (𝑈 ) +
𝑐3
2𝑟
60
0
0
{︂∫︁ +∞ [︂
]︂
1 (3) (4)
𝐺
4
(3) (3)
d𝜏 − M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 − 𝜖𝑎𝑏⟨𝑖 M𝑗𝑎 S𝑘⟩𝑏 (𝑈 − 𝜏 )
+ 5
𝑐
3
5
0
9 (4) (2)
1 (2) (4)
3 (5) (1)
1 (1) (5)
4 (3) (3)
− M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 − M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 + M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 − M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 + M𝑎⟨𝑖 M𝑗𝑘⟩𝑎
3
4
4
4
4
[︁
1 (6)
1
1
(6)
(2) (3)
(2) (3)
(1) (4)
+ M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 + M𝑎⟨𝑖 M𝑗𝑘⟩𝑎 + 𝜖𝑎𝑏⟨𝑖 −12S𝑗𝑎 M𝑘⟩𝑏 − 8M𝑗𝑎 S𝑘⟩𝑏 − 3S𝑗𝑎 M𝑘⟩𝑏
12
4
5
]︂
}︂
9
12
(1) (4)
(5)
(5)
(5)
(4)
−27M𝑗𝑎 S𝑘⟩𝑏 − S𝑗𝑎 M𝑘⟩𝑏 − 9M𝑗𝑎 S𝑘⟩𝑏 − S𝑎 M𝑗𝑘⟩𝑏 + S⟨𝑖 S𝑗𝑘⟩
4
5
(︂ )︂
1
+𝒪 6 ,
(95a)
𝑐
[︂ (︂
]︂
)︂
∫︁
𝑐𝜏
2𝐺𝑀 +∞
7 (4)
(2)
d𝜏 ln
S (𝑈 − 𝜏 )
V𝑖𝑗 (𝑈 ) = S𝑖𝑗 (𝑈 ) +
+
𝑐3
2𝑟0
6 𝑖𝑗
0
𝐺 {︁ (2) (3)
(2) (3)
(1) (4)
(1) (4)
(5)
+ 5 4S𝑎⟨𝑖 M𝑗⟩𝑎 + 8M𝑎⟨𝑖 S𝑗⟩𝑎 + 17S𝑎⟨𝑖 M𝑗⟩𝑎 − 3M𝑎⟨𝑖 S𝑗⟩𝑎 + 9S𝑎⟨𝑖 M𝑗⟩𝑎
7𝑐
[︂
1
1
353 (2) (4)
(5)
(5)
(4)
(3) (3)
− 3M𝑎⟨𝑖 S𝑗⟩𝑎 − S𝑎 M𝑖𝑗𝑎 − 7𝜖𝑎𝑏⟨𝑖 S𝑎 S𝑗⟩𝑏 + 𝜖𝑎𝑐⟨𝑖 3M𝑎𝑏 M𝑗⟩𝑏𝑐 +
M M
4
2
24 𝑗⟩𝑏𝑐 𝑎𝑏
]︂}︂
113 (1) (5) 3 (1) (5)
15
3
5 (2) (4)
(6)
(6)
M𝑗⟩𝑏𝑐 M𝑎𝑏 − M𝑎𝑏 M𝑗⟩𝑏𝑐 + M𝑗⟩𝑏𝑐 M𝑎𝑏 + M𝑎𝑏 M𝑗⟩𝑏𝑐
− M𝑎𝑏 M𝑗⟩𝑏𝑐 +
12
8
8
4
8
(︂ )︂
1
+𝒪 6 .
(95b)
𝑐
{︂
[︂
(︂
)︂
]︂
∫︁ +∞
𝐺
𝑐𝜏
59
(4)
(6)
U𝑖𝑗𝑘𝑙 (𝑈 ) = M𝑖𝑗𝑘𝑙 (𝑈 ) + 3 2𝑀
d𝜏 ln
+
M𝑖𝑗𝑘𝑙 (𝑈 − 𝜏 )
𝑐
2𝑟0
30
0
}︂
∫︁
21 (5)
63 (4) (1) 102 (3) (2)
2 +∞
(3) (3)
d𝜏 M⟨𝑖𝑗 M𝑘𝑙⟩ (𝑈 − 𝜏 ) − M⟨𝑖𝑗 M𝑘𝑙⟩ − M⟨𝑖𝑗 M𝑘𝑙⟩ −
M⟨𝑖𝑗 M𝑘𝑙⟩
+
5 0
5
5
5
(︂ )︂
1
+𝒪 5 ,
(95c)
𝑐
{︂
)︂
]︂
∫︁ +∞ [︂ (︂
𝐺
𝑐𝜏
5 (5)
(3)
V𝑖𝑗𝑘 (𝑈 ) = S𝑖𝑗𝑘 (𝑈 ) + 3 2𝑀
+
S (𝑈 − 𝜏 )
d𝜏 ln
𝑐
2𝑟0
3 𝑖𝑗𝑘
0
}︂
1
1
(5)
(4) (1)
(4)
+ 𝜖𝑎𝑏⟨𝑖 M𝑗𝑎 M𝑘⟩𝑏 − 𝜖𝑎𝑏⟨𝑖 M𝑗𝑎 M𝑘⟩𝑏 − 2S⟨𝑖 M𝑗𝑘⟩
10
2
28 In all formulas below the STF projection ⟨⟩ applies only to the “free” indices denoted 𝑖𝑗𝑘𝑙 . . . carried by the
moments themselves. Thus the dummy indices such as 𝑎𝑏𝑐 . . . are excluded from the STF projection.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 45

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

(︂
+𝒪

1
𝑐5

45

)︂
.

(95d)
{︂
)︂
]︂
∫︁ +∞ [︂ (︂
𝑐𝜏
𝐺
232
(5)
(7)
d𝜏 ln
U𝑖𝑗𝑘𝑙𝑚 (𝑈 ) = M𝑖𝑗𝑘𝑙𝑚 (𝑈 ) + 3 2𝑀
+
M𝑖𝑗𝑘𝑙𝑚 (𝑈 − 𝜏 )
𝑐
2𝑟0
105
0
∫︁
710 (3) (3)
20 +∞
265 (2) (4)
120 (2) (4)
(3) (4)
d𝜏 M⟨𝑖𝑗 M𝑘𝑙𝑚⟩ (𝑈 − 𝜏 ) −
+
M⟨𝑖𝑗 M𝑘𝑙𝑚⟩ −
M⟨𝑖𝑗𝑘 M𝑙𝑚⟩ −
M⟨𝑖𝑗 M𝑘𝑙𝑚⟩
21 0
21
7
7
}︂
155 (1) (5)
41 (1) (5)
34
15
(6)
(6)
−
M⟨𝑖𝑗𝑘 M𝑙𝑚⟩ − M⟨𝑖𝑗 M𝑘𝑙𝑚⟩ − M⟨𝑖𝑗𝑘 M𝑙𝑚⟩ − M⟨𝑖𝑗 M𝑘𝑙𝑚⟩
7
7
7
7
(︂ )︂
1
(95e)
+𝒪 4 ,
𝑐
{︂
)︂
]︂
∫︁ +∞ [︂ (︂
𝑐𝜏
𝐺
119 (6)
(4)
d𝜏 ln
V𝑖𝑗𝑘𝑙 (𝑈 ) = S𝑖𝑗𝑘𝑙 (𝑈 ) + 3 2𝑀
+
S𝑖𝑗𝑘𝑙 (𝑈 − 𝜏 )
𝑐
2𝑟0
60
0
35 (2) (3) 25 (2) (3) 65 (1) (4) 25 (1) (4) 19
(5)
− S⟨𝑖𝑗 M𝑘𝑙⟩ − M⟨𝑖𝑗 S𝑘𝑙⟩ − S⟨𝑖𝑗 M𝑘𝑙⟩ − M⟨𝑖𝑗 S𝑘𝑙⟩ − S⟨𝑖𝑗 M𝑘𝑙⟩
3
3
6
6
6
[︂
11
1
11 (4) (2)
5 (2) (4)
11
(5)
(5)
(3) (3)
− M⟨𝑖𝑗 S𝑘𝑙⟩ − S⟨𝑖 M𝑗𝑘𝑙⟩ + 𝜖𝑎𝑏⟨𝑖 −5M𝑗𝑎 M𝑘𝑙⟩𝑏 − M𝑗𝑎 M𝑘𝑙⟩𝑏 − M𝑗𝑎 M𝑘𝑙⟩𝑏
6
12
6
2
2
]︂}︂
1 (5) (1)
37 (1) (5)
3 (6)
1
(6)
− M𝑗𝑎 M𝑘𝑙⟩𝑏 + M𝑗𝑎 M𝑘𝑙⟩𝑏 + M𝑗𝑎 M𝑘𝑙⟩𝑏 + M𝑗𝑎 M𝑘𝑙⟩𝑏
2
10
10
2
(︂ )︂
1
+𝒪 4 .
(95f)
𝑐
For all the other multipole moments in the 3PN waveform, it is sufficient to assume the agreement
between the radiative and canonical moments, namely
(︂ )︂
1
(ℓ)
U𝐿 (𝑈 ) = M𝐿 (𝑈 ) + 𝒪 3 ,
(96a)
𝑐
(︂ )︂
1
(ℓ)
(96b)
V𝐿 (𝑈 ) = S𝐿 (𝑈 ) + 𝒪 3 .
𝑐
In a second stage of the general formalism, we must express the canonical moments {M𝐿 , S𝐿 }
in terms of the six types of source moments {I𝐿 , J𝐿 , W𝐿 , X𝐿 , Y𝐿 , Z𝐿 }. For the control of the (2, 2)
mode in the waveform up to 3.5PN order, we need to relate the canonical quadrupole moment M𝑖𝑗
to the corresponding source quadrupole moment I𝑖𝑗 up to that accuracy. We obtain [197]
]︁
4𝐺 [︁
(1)
M𝑖𝑗 = I𝑖𝑗 + 5 W(2) I𝑖𝑗 − W(1) I𝑖𝑗
[︂ 𝑐
1
5
4𝐺 4 (1) (3) 6
(4)
(3)
(3)
(3)
W I + W𝑎⟨𝑖 I𝑗⟩𝑎 − I𝑎⟨𝑖 Y𝑗⟩𝑎 − Y𝑎⟨𝑖 I𝑗⟩𝑎 − 2XI𝑖𝑗 − I𝑖𝑗𝑎 W𝑎(4)
+ 7
𝑐 7 𝑎⟨𝑖 𝑗⟩𝑎 7
7
21
25
5
1 (1)
22 (1)
(2)
+ I𝑖𝑗𝑎 W𝑎(3) − I𝑖𝑗𝑎 Y𝑎(3) − I𝑖𝑗𝑎 Y𝑎(2) + Y𝑎(1) I𝑖𝑗𝑎 + 2W𝑖𝑗 W(3)
63
21
63
63
4
(1)
(3)
(2)
+ 2W𝑖𝑗 W(2) − W⟨𝑖 W𝑗⟩ + 2Y𝑖𝑗 W(2) − 4W⟨𝑖 Y𝑗⟩
3
)︂]︂
(︂ )︂
(︂
1
4
4
8 (1) (1)
1
(3)
(3)
(2)
(3)
+ 𝜖𝑎𝑏⟨𝑖
I𝑗⟩𝑎 Z𝑏 + J𝑗⟩𝑎 W𝑏 − J𝑗⟩𝑎 Y𝑏 + J𝑗⟩𝑎 Y𝑏 + Z𝑎 I𝑗⟩𝑏
+ 𝒪 8 . (97)
3
9
9
9
𝑐
Here, for instance, W denotes the monopole moment associated with the moment W𝐿 , and Y𝑖 is
the dipole moment corresponding to Y𝐿 . Notice that the difference between the canonical and
source moments starts at the relatively high 2.5PN order. For the control of the full waveform

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 46

46

Luc Blanchet

up to 3PN order we need also the moments M𝑖𝑗𝑘 and S𝑖𝑗 , which admit similarly some correction
terms starting at the 2.5PN order:
(︂ )︂
]︁
4𝐺 [︁
1
(1)
(1)
M𝑖𝑗𝑘 = I𝑖𝑗𝑘 + 5 W(2) I𝑖𝑗𝑘 − W(1) I𝑖𝑗𝑘 + 3 I⟨𝑖𝑗 Y𝑘⟩ + 𝒪 6 ,
(98a)
𝑐
𝑐
]︁
)︁
(︁
2𝐺 [︁
(1)
(1)
(3)
(1)
S𝑖𝑗 = J𝑖𝑗 + 5 𝜖𝑎𝑏⟨𝑖 −I𝑗⟩𝑏 W𝑎 − 2I𝑗⟩𝑏 Y𝑎(2) + I𝑗⟩𝑏 Y𝑎(1) + 3J⟨𝑖 Y𝑗⟩ − 2J𝑖𝑗 W(1)
𝑐
(︂ )︂
1
(98b)
+𝒪 6 .
𝑐
The remainders in Eqs. (98) are consistent with the 3PN approximation for the full waveform.
Besides the mass quadrupole moment (97), and mass octopole and current quadrupole moments
(98), we can state that, with the required 3PN precision, all the other moments M𝐿 , S𝐿 agree with
their source counterparts I𝐿 , J𝐿 :
(︂ )︂
1
M𝐿 = I𝐿 + 𝒪 5 ,
(99a)
𝑐
(︂ )︂
1
S𝐿 = J𝐿 + 𝒪 5 .
(99b)
𝑐
With those formulas we have related the radiative moments {U𝐿 , V𝐿 } parametrizing the asymptotic
waveform (66) to the six types of source multipole moments {I𝐿 , J𝐿 , W𝐿 , X𝐿 , Y𝐿 , Z𝐿 }. What is
missing is the explicit dependence of the source moments as functions of the actual parameters of
some matter source. We come to grips with this important question in the next section.

4

Matching to a Post-Newtonian Source

By Theorem 2 we control the most general class of solutions of the vacuum equations outside
the source, in the form of non-linear functionals of the source multipole moments. For instance,
these solutions include the Schwarzschild and Kerr solutions for black holes, as well as all their
perturbations. By Theorem 4 we learned how to construct the radiative moments at infinity,
which constitute the observables of the radiation field at large distances from the source, and we
obtained in Section 3.3 explicit relationships between radiative and source moments. We now want
to understand how a specific choice of matter stress-energy tensor 𝑇 𝛼𝛽 , i.e., a specific choice of
some physical model describing the material source, selects a particular physical exterior solution
among our general class, and therefore a given set of multipole moments for the source.

4.1

The matching equation

We shall provide the answer to that problem in the case of a post-Newtonian source for which the
post-Newtonian parameter 𝜖 ∼ 1/𝑐 defined by Eq. (1) is small. The fundamental fact that permits
the connection of the exterior field to the inner field of the source is the existence of a “matching”
region, in which both the multipole expansion and the post-Newtonian expansion are valid. This
region is nothing but the exterior part of the near zone, such that 𝑟 > 𝑎 (exterior) and 𝑟 ≪ 𝜆 (near
zone); it always exists around post-Newtonian sources whose radius is much less than the emitted
wavelength, 𝜆𝑎 ∼ 𝜖 ≪ 1. In our formalism the multipole expansion is defined by the multipolarpost-Minkowskian (MPM) solution; see Section 2. Matching together the post-Newtonian and
MPM solutions in this overlapping region is an application of the method of matched asymptotic
expansions, which has frequently been applied in the present context, both for radiation-reaction
[114, 113, 7, 58, 43] and wave-generation [59, 155, 44, 49] problems.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 47

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

47

Let us denote by ℳ(ℎ) the multipole expansion of ℎ (for simplicity, we suppress the spacetime indices). By ℳ(ℎ) we really mean the MPM exterior metric that we have constructed in
Sections 2.2 and 2.3:
+∞
∑︁
ℳ(ℎ) ≡ ℎext =
𝐺𝑛 ℎ(𝑛) [I𝐿 , . . . , Z𝐿 ] .
(100)
𝑛=1

This solution is formally defined for any radius 𝑟 > 0. Of course, the true solution ℎ agrees with
its own multipole expansion in the exterior of the source, i.e.
𝑟>𝑎

=⇒

ℳ(ℎ) = ℎ .

(101)

By contrast, inside the source, ℎ and ℳ(ℎ) disagree with each other because ℎ is a fully-fledged
solution of the field equations within the matter source, while ℳ(ℎ) is a vacuum solution becoming
singular at 𝑟 = 0. Now let us denote by ℎ the post-Newtonian expansion of ℎ. We have already
anticipated the general structure of this expansion which is given in Eq. (54). In the matching
region, where both the multipolar and post-Newtonian expansions are valid, we write the numerical
equality
(102)
𝑎 < 𝑟 ≪ 𝜆 =⇒ ℳ(ℎ) = ℎ .
This “numerical” equality is viewed here in a sense of formal expansions, as we do not control the
convergence of the series. In fact, we should be aware that such an equality, though quite natural
and even physically obvious, is probably not really justified within the approximation scheme
(mathematically speaking), and we simply take it here as part of our fundamental assumptions.
We now transform Eq. (102) into a matching equation, by replacing in the left-hand side ℳ(ℎ)
by its near-zone re-expansion ℳ(ℎ), and in the right-hand side ℎ by its multipole expansion ℳ(ℎ).
The structure of the near-zone expansion (𝑟 → 0) of the exterior multipolar field has been found in
Theorem 3, see Eq. (53). We denote the corresponding infinite series ℳ(ℎ) with the same overbar
as for the post-Newtonian expansion because it is really an expansion when 𝑟/𝑐 → 0, equivalent
to an expansion when 𝑐 → ∞. Concerning the multipole expansion of the post-Newtonian metric,
ℳ(ℎ), we simply postulate for the moment its existence, but we shall show later how to construct
it explicitly. Therefore, the matching equation is the statement that
ℳ(ℎ) = ℳ(ℎ) ,

(103)

by which we really mean an infinite set of functional identities, valid ∀(x, 𝑡) ∈ R3* × R, between
the coefficients of the series in both sides of the equation. Note that such a meaning is somewhat
different from that of a numerical equality like Eq. (102), which is valid only when x belongs
to some limited spatial domain. The matching equation (103) tells us that the formal near-zone
expansion of the multipole decomposition is identical, term by term, to the multipole expansion
of the post-Newtonian solution. However, the former expansion is nothing but the formal farzone expansion, when 𝑟 → ∞, of each of the post-Newtonian coefficients. Most importantly, it
is possible to write down, within the present formalism, the general structure of these identical
expansions as a consequence of Eq. (53):
∑︁
ℳ(ℎ) =
𝑛
^ 𝐿 𝑟𝑚 (ln 𝑟)𝑝 𝐹𝐿,𝑚,𝑝 (𝑡) = ℳ(ℎ) ,
(104)
∑︀
where the functions 𝐹𝐿,𝑚,𝑝 = 𝑛⩾1 𝐺𝑛 𝐹𝐿,𝑚,𝑝,𝑛 . The latter expansion can be interpreted either as
the singular re-expansion of the multipole decomposition when 𝑟 → 0 – i.e., the first equality in
Eq. (104) –, or the singular re-expansion of the post-Newtonian series when 𝑟 → +∞ – the second
equality.
We recognize the beauty of singular perturbation theory, where two asymptotic expansions,
taken formally outside their respective domains of validity, are matched together. Of course, the

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 48

48

Luc Blanchet

method works because there exists, physically, an overlapping region in which the two approximation series are expected to be numerically close to the exact solution. As we shall detail in
Sections 4.2 and 5.2, the matching equation (103), supplemented by the condition of no-incoming
radiation [say in the form of Eq. (29)], permits determining all the unknowns of the problem: On
the one hand, the external multipolar decomposition ℳ(ℎ), i.e., the explicit expressions of the
multipole moments therein (see Sections 4.2 and 4.4); on the other hand, the terms in the inner
post-Newtonian expansion ℎ that are associated with radiation-reaction effects, i.e., those terms
which depend on the boundary conditions of the radiative field at infinity, and which correspond in
the present case to a post-Newtonian source which is isolated from other sources in the Universe;
see Section 5.2.

4.2

General expression of the multipole expansion

Theorem 5. Under the hypothesis of matching, Eq. (103), the multipole expansion of the solution
of the Einstein field equation outside a post-Newtonian source reads
𝛼𝛽

ℳ(ℎ

) = ℱ𝒫 𝐵=0 −1
ret

[︁

𝐵

𝛼𝛽

𝑟̃︀ ℳ(Λ

}︂
]︁ 4𝐺 +∞
∑︁ (−)ℓ {︂ 1 𝛼𝛽
𝜕𝐿
ℋ (𝑡 − 𝑟/𝑐) ,
) − 4
𝑐
ℓ!
𝑟 𝐿

(105)

ℓ=0

where the “multipole moments” are given by
𝛼𝛽
ℋ𝐿
(𝑢) = ℱ𝒫 𝐵=0

∫︁

d3 x 𝑟̃︀𝐵 𝑥𝐿 𝜏 𝛼𝛽 (x, 𝑢) .

(106)

Here, 𝜏 𝛼𝛽 denotes the post-Newtonian expansion of the stress-energy pseudo-tensor in harmonic
coordinates as defined by Eq. (23).
Proof (see Refs. [44, 49]): First notice where the physical restriction of considering a postNewtonian source enters this theorem: The multipole moments (106) depend on the post-Newtonian
expansion 𝜏 𝛼𝛽 of the pseudo-tensor, rather than on 𝜏 𝛼𝛽 itself. Consider Δ𝛼𝛽 , namely the difference
between ℎ𝛼𝛽 , which is a solution of the field equations everywhere inside and outside the source,
and the first term in Eq. (105), namely the finite part of the retarded integral of the multipole
expansion ℳ(Λ𝛼𝛽 ):
𝛼𝛽
Δ𝛼𝛽 ≡ ℎ𝛼𝛽 − ℱ 𝒫 −1
)] .
(107)
ret [ℳ(Λ
From now on we shall generally abbreviate the symbols concerning the finite-part operation at
𝐵 = 0 by a mere ℱ𝒫. According to Eq. (30), ℎ𝛼𝛽 is given by the retarded integral of the pseudotensor 𝜏 𝛼𝛽 . So,
[︀
]︀
16𝜋𝐺 −1 𝛼𝛽
𝛼𝛽
Δ𝛼𝛽 =
) .
(108)
ret 𝜏 − ℱ 𝒫 −1
ret ℳ(Λ
4
𝑐
In the second term the finite part plays a crucial role because the multipole expansion ℳ(Λ𝛼𝛽 )
is singular at 𝑟 = 0. By contrast, the first term in Eq. (108), as it stands, is well-defined because
we are considering only some smooth field distributions: 𝜏 𝛼𝛽 ∈ 𝐶 ∞ (R4 ). There is no need to
include a finite part ℱ𝒫 in the first term, but a contrario there is no harm to add one in front of
it, because for convergent integrals the finite part simply gives back the value of the integral. The
advantage of adding artificially the ℱ𝒫 in the first term is that we can re-write Eq. (108) into the
more interesting form
[︀ 𝛼𝛽
]︀
16𝜋𝐺
Δ𝛼𝛽 =
ℱ𝒫 −1
− ℳ(𝜏 𝛼𝛽 ) ,
(109)
ret 𝜏
𝑐4
𝛼𝛽
in which we have also used the fact that ℳ(Λ𝛼𝛽 ) = 16𝜋𝐺
) because 𝑇 𝛼𝛽 has a compact
𝑐4 ℳ(𝜏
𝛼𝛽
support. The interesting point about Eq. (109) is that Δ appears now to be the (finite part

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 49

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

49

of a) retarded integral of a source with spatially compact support. This follows from the fact
that the pseudo-tensor agrees numerically with its own multipole expansion when 𝑟 > 𝑎 [by the
same equation as Eq. (102)]. Therefore, ℳ(Δ𝛼𝛽 ) can be obtained from the known formula for
the multipole expansion of the retarded solution of a wave equation with compact-support source.
This formula, given in Appendix B of Ref. [59], yields the second term in Eq. (105),
+∞

ℳ(Δ𝛼𝛽 ) = −

4𝐺 ∑︁ (−)ℓ
𝜕𝐿
𝑐4
ℓ!
ℓ=0

{︂

}︂
1 𝛼𝛽
ℋ𝐿 (𝑢) ,
𝑟

but in which the moments do not yet match the result (106); instead,29
∫︁
[︁
]︁
𝛼𝛽
ℋ𝐿
= ℱ𝒫 d3 x 𝑥𝐿 𝜏 𝛼𝛽 − ℳ(𝜏 𝛼𝛽 ) .

(110)

(111)

The reason is that we have not yet applied the assumption of a post-Newtonian source. Such
sources are entirely covered by their own near zone (i.e., 𝑎 ≪ 𝜆), and, in addition, for them the
integral (111) has a compact support limited to the domain of the source. In consequence, we can
replace the integrand in Eq. (111) by its post-Newtonian expansion, valid over all the near zone:
∫︁
]︁
[︁
𝛼𝛽
(112)
ℋ𝐿
= ℱ𝒫 d3 x 𝑥𝐿 𝜏 𝛼𝛽 − ℳ(𝜏 𝛼𝛽 ) .
Strangely enough, we do not get the expected result because of the presence of the second term
in Eq. (112). Actually, this term is a bit curious, because the object ℳ(𝜏 𝛼𝛽 ) it contains is
only known in the form of the formal series whose structure is given by the first equality in
Eq. (104) (indeed 𝜏 and ℎ have the same type of structure). Happily – because we would not
know what to do with this term in applications – we are now going to prove that the second
term in Eq. (112) is in fact identically zero. The proof is based on the properties of the analytic
continuation as applied to the formal structure (104) of ℳ(𝜏 𝛼𝛽 ). Each term of this series yields
a contribution to Eq. (112) that takes the form, after performing the angular integration, of the
∫︀ +∞
integral ℱ𝒫 𝐵=0 0 d𝑟 𝑟𝐵+𝑏 (ln 𝑟)𝑝 , and multiplied by some function of time. We want to prove
∫︀ +∞
that the radial integral 0 d𝑟 𝑟𝐵+𝑏 (ln 𝑟)𝑝 is zero by analytic continuation (∀𝐵 ∈ C). First we
can get rid of the logarithms by considering some repeated
differentiations with respect to 𝐵;
∫︀ +∞
thus we need only to consider the simpler integral 0 d𝑟 𝑟𝐵+𝑏 . We split the integral into a
∫︀ ℛ
∫︀ +∞
“near-zone” integral 0 d𝑟 𝑟𝐵+𝑏 and a “far-zone” one ℛ d𝑟 𝑟𝐵+𝑏 , where ℛ is some constant
radius. When ℜ(𝐵) is a large enough positive number, the value of the near-zone integral is
ℛ𝐵+𝑏+1 /(𝐵 + 𝑏 + 1), while when ℜ(𝐵) is a large negative number, the far-zone integral reads the
opposite, −ℛ𝐵+𝑏+1 /(𝐵 + 𝑏 + 1). Both obtained values represent the unique analytic continuations
the near-zone and far-zone integrals for any 𝐵 ∈ C except −𝑏 − 1. The complete integral
∫︀of+∞
d𝑟 𝑟𝐵+𝑏 is equal to the sum of these analytic continuations, and is therefore identically zero
0
(∀𝐵 ∈ C, including the value −𝑏 − 1). At last we have completed the proof of Theorem 5:
∫︁
𝛼𝛽
(113)
ℋ𝐿
= ℱ𝒫 d3 x 𝑥𝐿 𝜏 𝛼𝛽 .
The latter proof makes it clear how crucial the analytic-continuation finite part ℱ𝒫 is, which we
recall is the same as in our iteration of the exterior post-Minkowskian field [see Eq. (45)]. Without a
finite part, the multipole moment (113) would be strongly divergent, because the pseudo-tensor 𝜏 𝛼𝛽
has a non-compact support owing to the contribution of the gravitational field, and the multipolar
29 Recall that our abbreviated notation ℱ 𝒫 includes the crucial regularization factor 𝑟
̃︀𝐵 .

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 50

50

Luc Blanchet

factor 𝑥𝐿 behaves like 𝑟ℓ when 𝑟 → +∞. The latter divergence has plagued the field of postNewtonian expansions of gravitational radiation for many years. In applications such as in Part B
of this article, we must carefully follow the rules for handling the ℱ𝒫 operator.
The two terms in the right-hand side of Eq. (105) depend separately on the length scale 𝑟0
that we have introduced into the definition of the finite part, through the analytic-continuation
factor 𝑟̃︀𝐵 = (𝑟/𝑟0 )𝐵 introduced in Eq. (42). However, the sum of these two terms, i.e., the exterior
multipolar field ℳ(ℎ) itself, is independent of 𝑟0 . To see this, the simplest way is to differentiate
formally ℳ(ℎ) with respect to 𝑟0 ; the differentiations of the two terms of Eq. (105) cancel each
other. The independence of the field upon 𝑟0 is quite useful in applications, since in general many
intermediate calculations do depend on 𝑟0 , and only in the final stage does the cancellation of
the 𝑟0 ’s occur. For instance, we have already seen in Eqs. (93) – (94) that the source quadrupole
moment I𝑖𝑗 depends on 𝑟0 starting from the 3PN level, but that this 𝑟0 is compensated by another
𝑟0 coming from the non-linear “tails of tails” at the 3PN order.

4.3

Equivalence with the Will–Wiseman formalism

Will & Wiseman [424] (see also Refs. [422, 335]), extending previous work of Epstein & Wagoner [185] and Thorne [403], have obtained a different-looking multipole decomposition, with different definitions for the multipole moments of a post-Newtonian source. They find, instead of our
multipole decomposition given by Eq. (105),
𝛼𝛽

ℳ(ℎ

) = −1
ret

}︂
{︂
+∞
[︁
]︁
1 𝛼𝛽
4𝐺 ∑︁ (−)ℓ
𝛼𝛽
𝜕𝐿
𝒲 (𝑡 − 𝑟/𝑐) .
ℳ(Λ ) − 4
𝑐
ℓ!
𝑟 𝐿
ℛ

(114)

ℓ=0

There is no ℱ𝒫 operation in the first term, but instead the retarded integral is truncated, as
indicated by the subscript ℛ, to extend only in the “far zone”: i.e., |x′ | > ℛ in the notation of
Eq. (31), where ℛ is a constant radius enclosing the source (ℛ > 𝑎). The near-zone part of the
retarded integral is thereby removed, and there is no problem with the singularity of the multipole
expansion ℳ(Λ𝛼𝛽 ) at the origin. The multipole moments 𝒲𝐿 are then given, in contrast with our
result (106), by an integral extending over the “near zone” only:
∫︁
𝛼𝛽
𝒲𝐿 (𝑢) =
d3 x 𝑥𝐿 𝜏 𝛼𝛽 (x, 𝑢) .
(115)
|x|<ℛ

Since the integrand is compact-supported there is no problem with the bound at infinity and the
integral is well-defined (no need of a ℱ𝒫).
Let us show that the two different formalisms are equivalent. We compute the difference
between our moment ℋ𝐿 defined by Eq. (106), and the moment 𝒲𝐿 given by Eq. (115). For the
comparison we split ℋ𝐿 into far-zone and near-zone pieces corresponding to the radius ℛ. Since
the finite part ℱ𝒫 present in ℋ𝐿 deals only with the bound at infinity, it can be removed from the
near-zone piece, which is then seen to reproduce 𝒲𝐿 exactly. So the difference between the two
moments is simply given by the far-zone piece:
∫︁
𝛼𝛽
ℋ𝐿
(𝑢) − 𝒲𝐿𝛼𝛽 (𝑢) = ℱ𝒫
d3 x 𝑥𝐿 𝜏 𝛼𝛽 (x, 𝑢) .
(116)
|x|>ℛ

We transform next this expression. Successively we write 𝜏 𝛼𝛽 = ℳ(𝜏 𝛼𝛽 ) because we are outside
the source, and ℳ(𝜏 𝛼𝛽 ) = ℳ(𝜏 𝛼𝛽 ) thanks to the matching equation (103). At this stage, we recall
from our reasoning right after Eq. (112) that the finite part of an integral over the whole space R3
of a quantity having the same structure as ℳ(𝜏 𝛼𝛽 ) is identically zero by analytic continuation.
The main ingredient of the present proof is made possible by this fact, as it allows us to transform

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 51

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

51

the far-zone integration |x| > ℛ in Eq. (116) into a near-zone one |x| < ℛ, at the price of changing
the overall sign in front of the integral. So,
∫︁
𝛼𝛽
(117)
ℋ𝐿
(𝑢) − 𝒲𝐿𝛼𝛽 (𝑢) = −ℱ𝒫
d3 x 𝑥𝐿 ℳ(𝜏 𝛼𝛽 )(x, 𝑢) .
|x|<ℛ

Finally, it is straightforward to check that the right-hand side of this equation, when summed
up over all multipolarities ℓ, accounts exactly for the near-zone part that was removed from the
retarded integral of ℳ(Λ𝛼𝛽 ) in the first term in Eq. (114), so that the “complete” retarded integral
as given by the first term in our own definition (105) is exactly reconstituted. In conclusion, the
formalism of Ref. [424] is equivalent to the one of Refs. [44, 49].

4.4

The source multipole moments

In principle, the bridge between the exterior gravitational field generated by the post-Newtonian
source and its inner field is provided by Theorem 5; however, we still have to make the connection
with the explicit construction of the general multipolar and post-Minkowskian metric in Section 2.
Namely, we must find the expressions of the six STF source multipole moments I𝐿 , J𝐿 , . . . , Z𝐿
parametrizing the linearized metric (35) – (37) at the basis of that construction.30
To do this we first find the equivalent of the multipole expansion given in Theorem 5, which
𝛼𝛽
was parametrized by non-trace-free multipole functions ℋ𝐿
, in terms of new multipole functions
𝛼𝛽
ℱ𝐿 that are STF in all their indices 𝐿. The result is
}︂
{︂
+∞
[︁
]︁ 4𝐺 ∑︁
(−)ℓ
1 𝛼𝛽
𝛼𝛽
𝜕
ℱ
(𝑡
−
𝑟/𝑐)
,
ℳ(ℎ𝛼𝛽 ) = ℱ𝒫 −1
ℳ(Λ
)
−
𝐿
ret
𝑐4
ℓ!
𝑟 𝐿

(118)

ℓ=0

where the STF multipole functions (witness the multipolar factor 𝑥
^𝐿 ≡ STF[𝑥𝐿 ]) read
∫︁
∫︁ 1
ℱ𝐿𝛼𝛽 (𝑢) = ℱ𝒫 d3 x 𝑥
^𝐿
d𝑧 𝛿ℓ (𝑧) 𝜏 𝛼𝛽 (x, 𝑢 + 𝑧𝑟/𝑐) .

(119)

−1

Notice the presence of an extra integration variable 𝑧, ranging from −1 to 1. The 𝑧-integration
involves the weighting function
𝛿ℓ (𝑧) =

(2ℓ + 1)!!
(1 − 𝑧 2 )ℓ ,
2ℓ+1 ℓ!

(120)

which approaches the Dirac delta-function (hence its name) in the limit of large multipolarities,
limℓ→+∞ 𝛿ℓ (𝑧) = 𝛿(𝑧), and is normalized in such a way that
∫︁ 1
𝑑𝑧 𝛿ℓ (𝑧) = 1 .
(121)
−1

The next step is to impose the harmonic-gauge conditions (21) onto the multipole decomposition (118), and to decompose the multipole functions ℱ𝐿𝛼𝛽 (𝑢) into STF irreducible pieces with
respect to both 𝐿 and their spatial indices contained into 𝛼𝛽 = 00, 0𝑖, 𝑖𝑗. This technical part
of the calculation is identical to the one of the STF irreducible multipole moments of linearized
gravity [154]. The formulas needed in this decomposition read
ℱ𝐿00 = 𝑅𝐿 ,

(122a)

30 Recall that in actual applications we need mostly the mass-type moment I and current-type one J , because
𝐿
𝐿
the other moments simply parametrize a linearized gauge transformation.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 52

52

Luc Blanchet

ℱ𝐿0𝑖 =(+) 𝑇𝑖𝐿 + 𝜖𝑎𝑖<𝑖ℓ (0) 𝑇𝐿−1>𝑎 + 𝛿𝑖<𝑖ℓ (−) 𝑇𝐿−1> ,

(122b)

ℱ𝐿𝑖𝑗 =(+2) 𝑈𝑖𝑗𝐿 + 𝑆𝑇 𝐹 𝑆𝑇 𝐹 [𝜖𝑎𝑖𝑖ℓ (+1) 𝑈𝑎𝑗𝐿−1 + 𝛿𝑖𝑖ℓ (0) 𝑈𝑗𝐿−1
𝑖𝑗
𝐿

(122c)

+ 𝛿𝑖𝑖ℓ 𝜖𝑎𝑗𝑖ℓ−1 (−1) 𝑈𝑎𝐿−2 + 𝛿𝑖𝑖ℓ 𝛿𝑗𝑖ℓ−1 (−2) 𝑈𝐿−2 ] + 𝛿𝑖𝑗 𝑉𝐿 ,

(122d)

where the ten tensors 𝑅𝐿 , (+) 𝑇𝐿+1 , . . . , (−2) 𝑈𝐿−2 , 𝑉𝐿 are STF, and are uniquely given in terms of
the ℱ𝐿𝛼𝛽 ’s by some inverse formulas. Finally, the latter decompositions yield the following.
Theorem 6. The STF multipole moments I𝐿 and J𝐿 of a post-Newtonian source are given, formally up to any post-Newtonian order, by (ℓ ⩾ 2)
∫︁
∫︁ 1 {︂
4(2ℓ + 1)
(1)
3
I𝐿 (𝑢) = ℱ𝒫 d x
d𝑧 𝛿ℓ 𝑥
^𝐿 Σ − 2
𝛿ℓ+1 𝑥
^𝑖𝐿 Σ𝑖
𝑐
(ℓ
+
1)(2ℓ
+
3)
−1
}︂
2(2ℓ + 1)
(2)
+ 4
𝛿ℓ+2 𝑥
^𝑖𝑗𝐿 Σ𝑖𝑗 (x, 𝑢 + 𝑧𝑟/𝑐) ,
(123a)
𝑐 (ℓ + 1)(ℓ + 2)(2ℓ + 5)
}︂
{︂
∫︁
∫︁ 1
2ℓ + 1
(1)
𝛿ℓ+1 𝑥
^𝐿−1⟩𝑎𝑐 Σ𝑏𝑐 (x, 𝑢 + 𝑧𝑟/𝑐) .
J𝐿 (𝑢) = ℱ𝒫 d3 x
d𝑧 𝜖𝑎𝑏⟨𝑖ℓ 𝛿ℓ 𝑥
^𝐿−1⟩𝑎 Σ𝑏 − 2
𝑐 (ℓ + 2)(2ℓ + 3)
−1
(123b)
These moments are the ones that are to be inserted into the linearized metric ℎ𝛼𝛽
(1) that represents
∑︀
𝛼𝛽
𝑛 𝛼𝛽
the lowest approximation to the post-Minkowskian field ℎext = 𝑛⩾1 𝐺 ℎ(𝑛) defined in Eq. (50).
In these formulas the notation is as follows: Some convenient source densities are defined from the
post-Newtonian expansion (denoted by an overbar) of the pseudo-tensor 𝜏 𝛼𝛽 by
𝜏 00 + 𝜏 𝑖𝑖
,
𝑐2
𝜏 0𝑖
Σ𝑖 =
,
𝑐
Σ𝑖𝑗 = 𝜏 𝑖𝑗 ,
Σ=

(124a)
(124b)
(124c)

(where 𝜏 𝑖𝑖 ≡ 𝛿𝑖𝑗 𝜏 𝑖𝑗 ). As indicated in Eqs. (123) all these quantities are to be evaluated at the
spatial point x and at time 𝑢 + 𝑧𝑟/𝑐.
For completeness, we give also the formulas for the four auxiliary source moments W𝐿 , . . . , Z𝐿 ,
which parametrize the gauge vector 𝜙𝛼
1 as defined in Eqs. (37):
∫︁
∫︁ 1 {︂
2ℓ + 1
3
W𝐿 (𝑢) = ℱ𝒫 d x
𝛿ℓ+1 𝑥
^𝑖𝐿 Σ𝑖
d𝑧
(ℓ + 1)(2ℓ + 3)
−1
}︂
2ℓ + 1
(1)
− 2
𝛿ℓ+2 𝑥
^𝑖𝑗𝐿 Σ𝑖𝑗 ,
(125a)
2𝑐 (ℓ + 1)(ℓ + 2)(2ℓ + 5)
}︂
∫︁
∫︁ 1 {︂
2ℓ + 1
X𝐿 (𝑢) = ℱ𝒫 d3 x
d𝑧
𝛿ℓ+2 𝑥
^𝑖𝑗𝐿 Σ𝑖𝑗 ,
(125b)
2(ℓ + 1)(ℓ + 2)(2ℓ + 5)
−1
∫︁
∫︁ 1 {︂
3(2ℓ + 1)
(1)
3
Y𝐿 (𝑢) = ℱ𝒫 d x
d𝑧 −𝛿ℓ 𝑥
^𝐿 Σ𝑖𝑖 +
𝛿ℓ+1 𝑥
^𝑖𝐿 Σ𝑖
(ℓ
+
1)(2ℓ
+
3)
−1
}︂
2(2ℓ + 1)
(2)
− 2
𝛿ℓ+2 𝑥
^𝑖𝑗𝐿 Σ𝑖𝑗 ,
(125c)
𝑐 (ℓ + 1)(ℓ + 2)(2ℓ + 5)
{︂
}︂
∫︁
∫︁ 1
2ℓ + 1
Z𝐿 (𝑢) = ℱ𝒫 d3 x
d𝑧 𝜖𝑎𝑏⟨𝑖ℓ −
𝛿ℓ+1 𝑥
^𝐿−1⟩𝑏𝑐 Σ𝑎𝑐 .
(125d)
(ℓ + 2)(2ℓ + 3)
−1

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 53

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

53

As discussed in Section 2, one can always find two intermediate “packages” of multipole moments,
namely the canonical moments M𝐿 and S𝐿 , which are some non-linear functionals of the source
moments (123) and (125), and such that the exterior field depends only on them, modulo a change of
coordinates. However, the canonical moments M𝐿 , S𝐿 do not admit general closed-form expressions
like (123) – (125).31
These source moments are physically valid for post-Newtonian sources and make sense only
in the form of a post-Newtonian expansion, so in practice we need to know how to expand the
𝑧-integrals as series when 𝑐 → +∞. Here is the appropriate formula:
∫︁ 1
d𝑧 𝛿ℓ (𝑧) Σ(x, 𝑢 + 𝑧𝑟/𝑐) =
−1

+∞
∑︁
𝑘=0

(︂
)︂2𝑘
𝑟 𝜕
(2ℓ + 1)!!
Σ(x, 𝑢) .
2𝑘 𝑘!(2ℓ + 2𝑘 + 1)!! 𝑐 𝜕𝑢

(126)

Since the right-hand side involves only even powers of 1/𝑐, the same result holds equally well for
the advanced variable 𝑢 + 𝑧𝑟/𝑐 or the retarded one 𝑢 − 𝑧𝑟/𝑐. Of course, in the Newtonian limit,
the moments I𝐿 and J𝐿 (and also M𝐿 and S𝐿 ) reduce to the standard Newtonian expressions. For
instance, I𝑖𝑗 (𝑢) = Q𝑖𝑗 (𝑢) + 𝒪(1/𝑐2 ) recovers the Newtonian quadrupole moment (3).32
Needless to say, the formalism becomes prohibitively difficult to apply at very high postNewtonian approximations. Some post-Newtonian order being given, we must first compute the
relevant relativistic corrections to the pseudo stress-energy-tensor 𝜏 𝛼𝛽 ; this necessitates solving the
field equations inside the matter, which we shall investigate in the next Section 5. Then 𝜏 𝛼𝛽 is to
be inserted into the source moments (123) and (125), where the formula (126) permits expressing
all the terms up to that post-Newtonian order by means of more tractable integrals extending over
R3 . Given a specific model for the matter source we then have to find a way to compute all these
spatial integrals; this is done in Section 9.1 for the case of point-mass binaries. Next, we must
substitute the source multipole moments into the linearized metric (35) – (37), and iterate them
until all the necessary multipole interactions taking place in the radiative moments U𝐿 and V𝐿 are
under control. In fact, we have already worked out these multipole interactions for general sources
in Section 3.3 up to the 3PN order in the full waveform, and 3.5PN order for the dominant (2, 2)
mode. Only at this point does one have the physical radiation field at infinity, from which we can
build the templates for the detection and analysis of gravitational waves. We advocate here that
the complexity of the formalism simply reflects the complexity of the Einstein field equations. It is
probably impossible to devise a different formalism, valid for general sources devoid of symmetries,
that would be substantially simpler.

5

Interior Field of a Post-Newtonian Source

Theorem 6 solves in principle the question of the generation of gravitational waves by extended
post-Newtonian matter sources. However, notice that this result has still to be completed by
the precise procedure, i.e., an explicit “algorithm”, for the post-Newtonian iteration of the nearzone field, analogous to the multipolar-post-Minkowskian algorithm we defined in Section 2. Such
procedure will permit the systematic computation of the source multipole moments, which contain
the full post-Newtonian expansion of the pseudo-tensor 𝜏 𝛼𝛽 , and of the radiation reaction effects
occurring within the matter source.
Before proceeding, let us recall that the “standard” post-Newtonian approximation, as it was
used until, say, the early 1980’s (see for instance Refs. [6, 181, 269, 270, 334] and also the earlier
works [344, 122, 124, 123]), was plagued with some apparently inherent difficulties, which croped
31 The work [65] provided some alternative expressions for all the multipole moments (123) – (125), useful for
some applications, in the form of surface integrals extending on the outer part of the source’s near zone.
32 The moments W , . . . , Z have also a Newtonian limit, but which is not particularly illuminating.
𝐿
𝐿

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 54

54

Luc Blanchet

up at some high post-Newtonian order. Historically these difficulties, even appearing at higher
approximations, have cast a doubt on the actual soundness, from a theoretical point of view, of the
post-Newtonian expansion. Practically speaking, they posed the question of the reliability of the
approximation, when comparing the theory’s predictions with very precise experimental results.
This was one of the main reason for the famous radiation-reaction controversy raging at the time
of the binary pulsar data [182, 418]. In this section we assess the nature of these difficulties – are
they purely technical or linked with some fundamental drawback of the approximation scheme? –
and eventually resolve them.
1. The first problem we face is that in higher approximations some divergent Poisson-type integrals appear. Indeed the post-Newtonian expansion replaces the resolution of a hyperboliclike d’Alembertian equation by a perturbatively equivalent hierarchy of elliptic-like Poisson
equations. Rapidly it is found during the post-Newtonian iteration that the right-hand side
of the Poisson equations acquires a non-compact support (it is distributed all over space R3 ),
and that as a result the standard Poisson integral diverges at the bound of the integral at
spatial infinity, i.e., when 𝑟 ≡ |x| → +∞, with 𝑡 = const.
2. The second problem is related with the limitation of the post-Newtonian approximation
to the near zone – the region surrounding the source of small extent with respect to the
wavelength of the emitted radiation: 𝑟 ≪ 𝜆. As we have seen, the post-Newtonian expansion
assumes from the start that all retardations 𝑟/𝑐 are small, so it can rightly be viewed as
a formal near-zone expansion, when 𝑟 → 0. Note that the fact which makes the Poisson
integrals to become typically divergent, namely that the coefficients of the post-Newtonian
series blow up at spatial infinity, when 𝑟 → +∞, has nothing to do with the actual behaviour
of the field at infinity. However, the serious consequence is that it is a priori impossible
to implement within the post-Newtonian scheme alone the physical information that the
matter system is isolated from the rest of the Universe. Most importantly, the no-incoming
radiation condition, imposed at past null infinity, cannot be taken directly into account, a
priori, into the post-Newtonian scheme. In this sense the post-Newtonian approximation is
not “self-supporting”, because it necessitates some information taken from outside its own
domain of validity.
The divergencies are linked to the fact that the post-Newtonian expansion is actually a singular
perturbation, in the sense that the coefficients of the successive powers of 1/𝑐 are not uniformly
valid in space, since they typically blow up at spatial infinity like some powers of 𝑟. We know for
instance that the post-Newtonian expansion cannot be “asymptotically flat” starting at the 2PN
or 3PN level, depending on the adopted coordinate system [362]. The result is that the standard
Poisson integrals are in general badly-behaving at infinity. Trying to solve the post-Newtonian
equations by means of the Poisson integral does not make sense. However, this does not mean that
there are no solutions to the problem, but simply that the Poisson integral does not constitute the
appropriate solution of the Poisson equation in the context of post-Newtonian expansions.
Here we present, following Refs. [357, 75], a solution of both problems, in the form of a general
expression for the near-zone gravitational field, developed to any post-Newtonian order, which
has been determined from implementing the matching equation (103). This solution is free of the
divergences of Poisson-type integrals we mentioned above, and yields, in particular, some general
expression, valid up to any order, of the terms associated with the gravitational radiation reaction
force inside the post-Newtonian source.
Though we shall focus our attention on the particular approach advocated in [357, 75], there are
other ways to resolve the problems of the post-Newtonian approximation. Notably, an alternative
solution to the problem of divergencies, proposed in Refs. [214, 211], is based on an initial-value
formulation. In this method the problem of the appearance of divergencies is avoided because

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 55

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

55

of the finiteness of the causal region of integration, between the initial Cauchy hypersurface and
the considered field point. On the other hand, a different approach to the problem of radiation
reaction, which does not use a matching procedure, is to work only within a post-Minkowskian
iteration scheme without expanding the retardations, see e.g., Ref. [126].

5.1

Post-Newtonian iteration in the near zone

We perform the post-Newtonian iteration of the field equations in harmonic coordinates in the near
zone of an isolated matter distribution. We deal with a general hydrodynamical fluid, whose stressenergy tensor is smooth, i.e., 𝑇 𝛼𝛽 ∈ 𝐶 ∞ (R4 ). Thus the scheme a priori excludes the presence of
singularities and black holes; these will be dealt with in Part B of this article.
We shall now prove [357] that the post-Newtonian expansion can be indefinitely iterated without
divergences. Like in Eq. (106) we denote by means of an overline the formal (infinite) postNewtonian expansion of the field inside the source’s near-zone. The general structure of the
post-Newtonian expansion is denoted (skipping the space-time indices 𝛼𝛽) as
ℎ(x, 𝑡, 𝑐) =

+∞
∑︁

1
ℎ (x, 𝑡; ln 𝑐) .
𝑚 𝑚
𝑐
𝑚=2

(127)

The 𝑚-th post-Newtonian coefficient is naturally the factor of the 𝑚-th power of 1/𝑐. However, we
know from restoring the factors 𝑐’s in Theorem 3 [see Eq. (53)], that the post-Newtonian expansion
also involves powers of the logarithm of 𝑐; these are included for convenience here into the definition
of the coefficients ℎ𝑚 .33 For the stress-energy pseudo-tensor appearing in Eq. (106) we have the
same type of expansion,
+∞
∑︁
1
𝜏 (x, 𝑡, 𝑐) =
𝜏 (x, 𝑡; ln 𝑐) .
(128)
𝑚 𝑚
𝑐
𝑚=−2
Note that the expansion starts with a term of order 𝑐2 corresponding to the rest mass-energy (𝜏 has
the dimension of an energy density). As usual we shall understand the infinite sums such as (127) –
(128) in the sense of formal series, i.e., merely as an ordered collection of coefficients. Because
of our consideration of regular extended matter distributions the post-Newtonian coefficients are
smooth functions of space-time, i.e., ℎ𝑚 (x, 𝑡) ∈ 𝐶 ∞ (R4 ).
Inserting the post-Newtonian ansatz (127) into the harmonic-coordinates Einstein field equation (21) – (22) and equating together the powers of 1/𝑐, results is an infinite set of Poisson-type
equations (∀𝑚 ⩾ 2),
Δ ℎ = 16𝜋𝐺 𝜏 + 𝜕𝑡2 ℎ ,
(129)
𝑚

𝑚−4

𝑚−2

where the second term comes from the split of the d’Alembertian operator into a Laplacian and
a second time derivative:  = Δ − 𝑐12 𝜕𝑡2 (this term is zero when 𝑚 = 2 and 3). We proceed
by induction, i.e., we work at some given but arbitrary post-Newtonian order 𝑚, assume that we
succeeded in constructing the sequence of previous coefficients ℎ𝑝 (∀𝑝 ⩽ 𝑚 − 1), and from that
show how to infer the next-order coefficient ℎ𝑚 .
To cure the problem of divergencies we introduce a generalized solution of the Poisson equation
with non-compact support source, in the form of an appropriate finite part of the usual Poisson
integral obtained by regularization of the bound at infinity by means of a specific process of
analytic continuation. For any source term like 𝜏 𝑚 , we multiply it by the regularization factor
𝑟̃︀𝐵 already extensively used in the construction of the exterior field, thus 𝐵 ∈ C and 𝑟̃︀ = 𝑟/𝑟0 is
given by Eq. (42). Only then do we apply the usual Poisson integral, which therefore defines a
33 For this argument we assume the validity of the matching equation (103) and that the post-Minkowskian series
over 𝑛 = 1, . . . , ∞ in Eq. (53) has been formally summed up.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 56

56

Luc Blanchet

certain function of 𝐵. The well-definedness of that integral heavily relies on the behaviour of the
integrand at the bound at infinity. There is no problem with the vicinity of the origin inside the
source because of the smoothness of the pseudo-tensor. Then one can prove [357] that the latter
function of 𝐵 generates a (unique) analytic continuation down to a neighbourhood of the value of
interest 𝐵 = 0, except at 𝐵 = 0 itself, at which value it admits a Laurent expansion with multiple
poles up to some finite order (but growing with the post-Newtonian order 𝑚). Then, we consider
the Laurent expansion of that function when 𝐵 → 0 and pick up the finite part, or coefficient of
the zero-th power of 𝐵, of that expansion. This defines our generalized Poisson integral:
∫︁
[︀ ]︀
1
d3 x′
−1
𝜏 (x, 𝑡) ≡ −
(130)
ℱ𝒫 𝐵=0
𝑟̃︀′𝐵 𝜏 (x′ , 𝑡) .
Δ
𝑚
𝑚
4𝜋
|x − x′ |
The integral extends over all three-dimensional space but with the latter finite-part regularization
at infinity denoted ℱ𝒫 𝐵=0 or ℱ𝒫 for short. The main properties of this generalized Poisson
operator is that it solves the Poisson equation,
(︁
[︀ ]︀)︁
=𝜏,
Δ Δ−1 𝜏
(131)
𝑚

𝑚

−1

and that the solution Δ 𝜏 𝑚 owns the same properties as its source 𝜏 𝑚 , i.e., the smoothness and
the same type of behaviour at infinity, as given by Eq. (104). Similarly, we define the generalized
iterated Poisson integral as
∫︁
[︀ ]︀
1
|x − x′ |2𝑘−1 ′𝐵
Δ−𝑘−1 𝜏 (x, 𝑡) ≡ −
ℱ𝒫 𝐵=0
𝑟̃︀ 𝜏 (x′ , 𝑡) .
(132)
d3 x′
𝑚
𝑚
4𝜋
(2𝑘)!
The most general solution of the Poisson equation will be obtained by application of the previous
generalized Poisson operator to the right-hand side of Eq. (129), and augmented by the most general
homogeneous solution of the Poisson equation. Thus, we can write
ℎ = 16𝜋𝐺 Δ−1

𝑚

[︀

𝜏

𝑚−4

]︀

+ 𝜕𝑡2 Δ−1

[︀

ℎ

𝑚−2

]︀

+

+∞
∑︁
ℓ=0

^𝐿 .
ℬ 𝐿 (𝑡) 𝑥

(133)

𝑚

The last term represents the most general solution of the Laplace equation that is regular at the
origin 𝑟 = 0. It can be written in STF guise as a multipolar series of terms of the type 𝑥
^𝐿 , and
multiplied by arbitrary STF-tensorial functions of time 𝑚 ℬ𝐿 (𝑡). These functions will be associated
with the radiation reaction of the field onto the source; they will depend on which boundary
conditions are to be imposed on the gravitational field at infinity from the source.
It is now trivial to iterate the process. We substitute for ℎ𝑚−2 in the right-hand side of Eq. (133)
the same expression but with 𝑚 replaced by 𝑚 − 2, and similarly come down until we stop at either
one of the coefficients ℎ0 = 0 or ℎ1 = 0. At this point ℎ𝑚 is expressed in terms of the previous
𝜏 𝑝 ’s and 𝑝 ℬ𝐿 ’s with 𝑝 ⩽ 𝑚 − 2. To finalize the process we introduce what we call the operator
of the “instantaneous” potentials and denote −1
inst . Our notation is chosen to contrast with the
standard operator of the retarded potentials −1
ret defined by Eq. (31). However, beware of the fact
−1
that unlike −1
the
operator

will
be
defined
only when acting on a post-Newtonian series
ret
inst
such as 𝜏 . Indeed, we pose
∑︁ (︂ 𝜕 )︂2𝑘
[︀ ]︀ +∞
[︀ ]︀
−1
inst 𝜏 ≡
Δ−𝑘−1 𝜏 ,
(134)
𝑐𝜕𝑡
𝑘=0

where the 𝑘-th iteration of the generalized Poisson operator is defined by Eq. (132). This operator
is instantaneous in the sense that it does not involve any integration over time. It is readily checked
that in this way we have a solution of the source-free d’Alembertian equation,
(︀
[︀ ]︀)︀
 −1
=𝜏.
(135)
inst 𝜏

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 57

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

57

On the other hand, the homogeneous solution in Eq. (133) will yield by iteration an homogeneous
solution of the d’Alembertian equation that is necessarily regular at the origin. Hence it should be
of the anti-symmetric type, i.e., be made of the difference between a retarded multipolar wave and
the corresponding advanced wave. We shall therefore introduce a new definition for some STFtensorial functions 𝒜𝐿 (𝑡) parametrizing those advanced-minus-retarded free waves. It is very easy
to relate if necessary the post-Newtonian expansion of 𝒜𝐿 (𝑡) to the functions 𝑚 ℬ𝐿 (𝑡) previously
introduced in Eq. (133). Finally the most general post-Newtonian solution, iterated ad infinitum
and without any divergences, is obtained into the form
{︂
}︂
+∞
16𝜋𝐺 −1 [︀ ]︀ 4𝐺 ∑︁ (−)ℓ ^
𝒜𝐿 (𝑡 − 𝑟/𝑐) − 𝒜𝐿 (𝑡 + 𝑟/𝑐)
inst 𝜏 − 4
𝜕𝐿
.
(136)
ℎ=
𝑐4
𝑐
ℓ!
2𝑟
ℓ=0

We shall refer to the 𝒜𝐿 (𝑡)’s as the radiation-reaction functions. If we stay at the level of the
post-Newtonian iteration which is confined into the near zone we cannot do more than Eq. (136):
There is no means to compute the radiation-reaction functions 𝒜𝐿 (𝑡). We are here touching the
second problem faced by the standard post-Newtonian approximation.

5.2

Post-Newtonian metric and radiation reaction effects

As we have understood this problem is that of the limitation to the near zone. Such limitation can
be circumvented to the lowest post-Newtonian orders by considering retarded integrals that are
formally expanded when 𝑐 → +∞ as series of “instantaneous” Poisson-like integrals, see e.g., [6].
This procedure works well up to the 2.5PN level and has been shown to correctly fix the dominant
radiation reaction term at the 2.5PN order [181, 269, 270, 334]. Unfortunately such a procedure
assumes fundamentally that the gravitational field, after expansion of all retardations 𝑟/𝑐 → 0,
depends on the state of the source at a single time 𝑡, in keeping with the instantaneous character of
the Newtonian interaction. However, we know that the post-Newtonian field (as well as the source’s
dynamics) will cease at some stage to be given by a functional of the source parameters at a single
time, because of the imprint of gravitational-wave tails in the near zone field, in the form of the
hereditary modification of the radiation reaction force at the 1.5PN relative order [58, 60, 43]. Since
the reaction force is itself of order 2.5PN this means that the formal post-Newtonian expansion of
retarded Green functions is no longer valid starting at the 4PN order.
The solution of the problem resides in the matching of the near-zone field to the exterior
field. We have already seen in Theorems 5 and 6 that the matching equation (103) yields the
expression of the multipole expansion in the exterior domain. Now we prove that it also permits
the full determinantion of the post-Newtonian metric in the near-zone, i.e., the radiation-reaction
functions 𝒜𝐿 which have been left unspecified in Eq. (136).
We find [357] that the radiation-reaction functions 𝒜𝐿 are composed of the multipole moment
functions ℱ𝐿 defined by Eq. (119), which will here characterize “linear-order” radiation reaction
effects starting at 2.5PN order, and of an extra piece ℛ𝐿 , which will be due to non-linear effets in
the radiation reaction and turn out to arise at the 4PN order. Thus,
𝒜𝐿 (𝑡) = ℱ𝐿 (𝑡) + ℛ𝐿 (𝑡) .

(137)

The extra piece ℛ𝐿 is obtained from the multipole expansion of the pseudo-tensor ℳ(𝜏 ).34 Hence
the radiation-reaction functions do depend on the behaviour of the field far away from the matter
source (as physical intuition already told us). The explicit expression reads
∫︁
∫︁ +∞
3
ℛ𝐿 (𝑡) = ℱ𝒫
d x𝑥
^𝐿
d𝑧 𝛾ℓ (𝑧) ℳ(𝜏 ) (x, 𝑡 − 𝑧𝑟/𝑐) .
(138)
1
34 We mean the fully-fledge ℳ(𝜏 ); i.e., not the formal object ℳ(𝜏 ).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 58

58

Luc Blanchet

The fact that the multipolar expansion ℳ(𝜏 ) is the source term for the function ℛ𝐿 is the consequence of the matching equation (103). The specific contributions due to ℛ𝐿 in the post-Newtonian
metric (136) are associated with tails of waves [58, 43]. Notice that, remarkably, the ℱ𝒫 regularization deals with the bound of the integral at 𝑟 = 0, in contrast with Eq. (119) where it deals
with the bound at 𝑟 = +∞. The weighting function 𝛾ℓ (𝑧) therein, where 𝑧 extends up to infinity
in contrast to the analogous function 𝛿ℓ (𝑧) in Eq. (119), is simply related to it by 𝛾ℓ (𝑧) ≡ −2𝛿ℓ (𝑧);
such definition is motivated by the fact that the integral of that function is normalized to one:35
∫︁ +∞
d𝑧 𝛾ℓ (𝑧) = 1 .
(139)
1

The post-Newtonian metric (136) is now fully determined. However, let us now prove a more
interesting alternative formulation of it, derived in Ref. [75].
Theorem 7. The expression of the post-Newtonian field in the near zone of a post-Newtonian
source, satisfying correct boundary conditions at infinity (no incoming radiation), reads
{︃
}︃
+∞
𝛼𝛽
ℛ𝛼𝛽
16𝜋𝐺 −1 [︀ 𝛼𝛽 ]︀ 4𝐺 ∑︁ (−)ℓ ^
𝛼𝛽
𝐿 (𝑡 − 𝑟/𝑐) − ℛ𝐿 (𝑡 + 𝑟/𝑐)
ℎ =
− 4
ret 𝜏
𝜕𝐿
.
(140)
𝑐4
𝑐
ℓ!
2𝑟
ℓ=0

The first term represents a particular solution of the hierarchy of post-Newtonian equations, while
the second one is a homogeneous multipolar solution of the wave equation, of the “anti-symmetric”
type that is regular at the origin 𝑟 = 0 located inside the source, and parametrized by the multipolemoment functions (138).
Let us be more precise about the meaning of the first term in Eq. (140). Indeed such term is
made of the formal expansion of the standard retarded integral (31) when 𝑐 → ∞, but acting on
a post-Newtonian source term 𝜏 ,
+∞
[︀ 𝛼𝛽 ]︀
1 ∑︁ (−)𝑚
−1
𝜏
(x,
𝑡)
≡
−
ret
4𝜋 𝑚=0 𝑚!

(︂

𝜕
𝑐 𝜕𝑡

)︂𝑚

∫︁
ℱ𝒫

d3 x′ |x − x′ |𝑚−1 𝜏 𝛼𝛽 (x′ , 𝑡) .

(141)

We emphasize that (141) constitutes the definition of a (formal) post-Newtonian expansion, each
term of which being built from the post-Newtonian expansion of the pseudo-tensor. Crucial in the
present formalism, is that each of the terms is regularized by means of the ℱ𝒫 operation in order
to deal with the bound at infinity at which the post-Newtonian expansion is singular. Because
of the presence of this regularization, the object (141) should carefully be distinguished from the
“global” solution −1
ret [𝜏 ] defined by Eq. (31), with global non-expanded pseudo-tensor 𝜏 .
The definition (141) is of interest because it corresponds to what one would intuitively think
as the natural way of performing the post-Newtonian iteration, i.e., by formally Taylor expanding
the retardations in Eq. (31), as was advocated by Anderson & DeCanio [6]. Moreover, each of the
terms of the series (141) is mathematically well-defined thanks to the finite part operation, and
can therefore be implemented in practical computations. The point is that Eq. (141) solves the
wave equation in a perturbative post-Newtonian sense,
(︀
[︀ 𝛼𝛽 ]︀)︀
 −1
= 𝜏 𝛼𝛽 ,
(142)
ret 𝜏
so constitutes a good prescription for a particular solution of the wave equation – as legitimate as
the solution (134). Therefore the two solutions should differ by an homogeneous solution of the
35 Though the latter integral is a priori divergent, its value can be determined by invoking complex analytic
continuation in ℓ ∈ C.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 59

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

59

wave equation which is necessarily of the anti-symmetric type (regular inside the source). Detailed
investigations [357, 75] yield
}︃
{︃
+∞
[︀ 𝛼𝛽 ]︀
[︀ 𝛼𝛽 ]︀
ℱ𝐿𝛼𝛽 (𝑡 − 𝑟/𝑐) − ℱ𝐿𝛼𝛽 (𝑡 + 𝑟/𝑐)
1 ∑︁ (−)ℓ ^
−1
−1
,
(143)
ret 𝜏
𝜕𝐿
= inst 𝜏
−
4𝜋
ℓ!
2𝑟
ℓ=0

where the homogeneous solution is parametrized by the multipole-moments ℱ𝐿 (𝑡). By combining
Eqs. (140) and (143), we indeed become reconciled with the previous expression of the postNewtonian field found in Eq. (136).
For computations limited to the 3.5PN order (level of the 1PN correction to the radiation
reaction force), the first term in Eq. (140) with the “intuitive” prescription (141) is sufficient.
But because of the second term in (140) there is a fundamental breakdown of this scheme at the
4PN order where it becomes necessary to take into account non-linear radiation reaction effects
associated with tails. The second term in (140) constitutes a generalization of the tail-transported
radiation reaction arising at the 4PN order, i.e., 1.5PN order relative to the dominant radiation
reaction order, as determined in Ref. [58]. The tail-transported radiation reaction is required by
energy conservation and the presence of tails in the wave zone. The usual radiation reaction terms,
up to 3.5PN order, are contained in the first term of Eq. (140), and are parametrized by the same
multipole-moment functions ℱ𝐿 as the exterior multipolar field, as Eq. (143) explicitly shows. In
Section 5.4 we shall give an explicit expression of the radiation reaction force showing the usual
radiation reaction terms to 3.5PN order, issued from ℱ𝐿 , and exhibiting the above tail-induced
4PN effect, issued from ℛ𝐿 .
Finally note that the post-Newtonian solution, in either form (136) or (140), has been obtained
without imposing the condition of harmonic coordinates (21) in an explicit way. We have simply
matched together the post-Newtonian and multipolar expansions, satisfying the “relaxed” Einstein
field equations (22) in their respective domains, and found that the matching determines uniquely
the solution. An important check done in [357, 75], is therefore to verify that the harmonic
coordinate condition (21) is indeed satisfied as a consequence of the conservation of the pseudotensor (27), so that we really grasp a solution of the full Einstein field equations.

5.3

The 3.5PN metric for general matter systems

The detailed calculations that are called for in applications necessitate having at one’s disposal
some explicit expressions of the metric coefficients 𝑔𝛼𝛽 , in harmonic coordinates, at the highest
possible post-Newtonian order. The 3.5PN metric that we present below can be viewed as an
application of the formalism of the previous section. It is expressed by means of some particular
^ 𝑖𝑗 , . . . , whose main advantages are to somewhat minimize the
retarded-type potentials, 𝑉 , 𝑉𝑖 , 𝑊
number of terms, so that even at the 3.5PN order the metric is still tractable, and to delineate
the different problems associated with the computation of different categories of terms. Of course,
these potentials have no direct physical significance by themselves, but they offer a convenient
parametrization of the 3.5PN metric.
The basic idea in our post-Newtonian iteration scheme is to use wherever possible a “direct”
𝜇
2
integration, with the help of some formulas like −1
ret (𝜕𝜇 𝑉 𝜕 𝑉 + 𝑉 𝑉 ) = 𝑉 /2. The 3.5PN
harmonic-coordinates metric reads [71]
(︂
)︂
3
2
8
2
^ + 𝑉𝑖 𝑉𝑖 + 𝑉
𝑔00 = −1 + 2 𝑉 − 4 𝑉 2 + 6 𝑋
𝑐
𝑐
𝑐
6
(︂
)︂
(︂
)︂
32
1 ^
^ 𝑖 𝑉𝑖 − 1 𝑉 𝑉𝑖 𝑉𝑖 − 1 𝑉 4 + 𝒪 1
+ 8 𝑇^ − 𝑉 𝑋
+𝑅
,
(144a)
𝑐
2
2
48
𝑐10
(︂
)︂
(︂ )︂
4
8 ^
16 ^
1 ^
1 2
1
𝑔0𝑖 = − 3 𝑉𝑖 − 5 𝑅
−
𝑌
+
𝑊
𝑉
+
𝑉
𝑉
+
𝒪
,
(144b)
𝑖
𝑖
𝑖𝑗 𝑗
𝑖
7
𝑐
𝑐
𝑐
2
2
𝑐9

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 60

60

Luc Blanchet

(︂
[︂
)︂]︂
2 2
8
𝑉3
2
4 ^
^
𝑔𝑖𝑗 = 𝛿𝑖𝑗 1 + 2 𝑉 + 4 𝑉 + 6 𝑋 + 𝑉𝑘 𝑉𝑘 +
+ 4𝑊
𝑖𝑗
𝑐
𝑐
𝑐
6
𝑐
(︂
)︂
(︂ )︂
16
1 ^
1
+ 6 𝑍^𝑖𝑗 + 𝑉 𝑊
.
𝑖𝑗 − 𝑉𝑖 𝑉𝑗 + 𝒪
𝑐
2
𝑐8

(144c)

All the potentials are generated by the matter stress-energy tensor 𝑇 𝛼𝛽 through some convenient
definitions recalling Eqs. (124),
𝑇 00 + 𝑇 𝑖𝑖
,
𝑐2
𝑇 0𝑖
𝜎𝑖 =
,
𝑐
𝑖𝑗
𝜎𝑖𝑗 = 𝑇 .
𝜎=

(145a)
(145b)
(145c)

Starting at Newtonian and 1PN orders, 𝑉 and 𝑉𝑖 represent some retarded versions of the usual
Newtonian and gravitomagnetic potentials,
𝑉 = −1
ret [−4𝜋𝐺𝜎] ,

(146a)

𝑉𝑖 = −1
ret [−4𝜋𝐺𝜎𝑖 ] .

(146b)

From the 2PN order we have the potentials
[︂
]︂
3
−1
2
2
^
^
𝑋 = ret −4𝜋𝐺𝑉 𝜎𝑖𝑖 + 𝑊𝑖𝑗 𝜕𝑖𝑗 𝑉 + 2𝑉𝑖 𝜕𝑡 𝜕𝑖 𝑉 + 𝑉 𝜕𝑡 𝑉 + (𝜕𝑡 𝑉 ) − 2𝜕𝑖 𝑉𝑗 𝜕𝑗 𝑉𝑖 ,
2
]︂
[︂
3
^ 𝑖 = −1
𝑅
ret −4𝜋𝐺(𝑉 𝜎𝑖 − 𝑉𝑖 𝜎) − 2𝜕𝑘 𝑉 𝜕𝑖 𝑉𝑘 − 𝜕𝑡 𝑉 𝜕𝑖 𝑉 ,
2
−1
^
𝑊𝑖𝑗 = ret [−4𝜋𝐺(𝜎𝑖𝑗 − 𝛿𝑖𝑗 𝜎𝑘𝑘 ) − 𝜕𝑖 𝑉 𝜕𝑗 𝑉 ] .

(147a)
(147b)
(147c)

Some parts of these potentials are directly generated by compact-support matter terms, while
other parts are made of non-compact-support products of 𝑉 -type potentials. There exists also an
^ 𝑖𝑗 and 𝑉 , see the second
important cubically non-linear term generated by the coupling between 𝑊
^
term in the 𝑋-potential. Note the important point that here and below the retarded integral
operator −1
ret is really meant to be the one given by Eq. (141); thus it involves in principle the
finite part regularization ℱ𝒫 to deal with (IR-type) divergences occurring at high post-Newtonian
orders for non-compact-support integrals. For instance, such finite part regularization is important
to take into account in the computation of the near zone metric at the 3PN order [68].
At the next level, 3PN, we have even more complicated potentials, namely
[︂
(︂
)︂
1 2
1
^
^
^
^
^
−4𝜋𝐺
𝑇^ = −1
𝜎
𝑊
+
𝑉
𝜎
+
𝜎𝑉
𝑉
𝑖𝑗 𝑖𝑗
𝑖𝑖
𝑖 𝑖 + 𝑍𝑖𝑗 𝜕𝑖𝑗 𝑉 + 𝑅𝑖 𝜕𝑡 𝜕𝑖 𝑉 − 2𝜕𝑖 𝑉𝑗 𝜕𝑗 𝑅𝑖 − 𝜕𝑖 𝑉𝑗 𝜕𝑡 𝑊𝑖𝑗
ret
4
2
]︂
1
3
1
3
+ 𝑉 𝑉𝑖 𝜕𝑡 𝜕𝑖 𝑉 + 2𝑉𝑖 𝜕𝑗 𝑉𝑖 𝜕𝑗 𝑉 + 𝑉𝑖 𝜕𝑡 𝑉 𝜕𝑖 𝑉 + 𝑉 2 𝜕𝑡2 𝑉 + 𝑉 (𝜕𝑡 𝑉 )2 − (𝜕𝑡 𝑉𝑖 )2 , (148a)
2
2
2
2
[︂
(︂
)︂
1 ^
1
1
^
𝑌^𝑖 = −1
ret −4𝜋𝐺 −𝜎 𝑅𝑖 − 𝜎𝑉 𝑉𝑖 + 𝜎𝑘 𝑊𝑖𝑘 + 𝜎𝑖𝑘 𝑉𝑘 + 𝜎𝑘𝑘 𝑉𝑖
2
2
2
^ 𝑘𝑙 𝜕𝑘𝑙 𝑉𝑖 − 𝜕𝑡 𝑊
^ 𝑖𝑘 𝜕𝑘 𝑉 + 𝜕𝑖 𝑊
^ 𝑘𝑙 𝜕𝑘 𝑉𝑙 − 𝜕𝑘 𝑊
^ 𝑖𝑙 𝜕𝑙 𝑉𝑘 − 2𝜕𝑘 𝑉 𝜕𝑖 𝑅
^ 𝑘 − 3 𝑉𝑘 𝜕𝑖 𝑉 𝜕𝑘 𝑉
+𝑊
2
]︂
3
2
− 𝑉 𝜕𝑡 𝑉 𝜕𝑖 𝑉 − 2𝑉 𝜕𝑘 𝑉 𝜕𝑘 𝑉𝑖 + 𝑉 𝜕𝑡 𝑉𝑖 + 2𝑉𝑘 𝜕𝑘 𝜕𝑡 𝑉𝑖 ,
(148b)
2
[︂
𝑍^𝑖𝑗 = −1
ret −4𝜋𝐺𝑉 (𝜎𝑖𝑗 − 𝛿𝑖𝑗 𝜎𝑘𝑘 ) − 2𝜕(𝑖 𝑉 𝜕𝑡 𝑉𝑗) + 𝜕𝑖 𝑉𝑘 𝜕𝑗 𝑉𝑘 + 𝜕𝑘 𝑉𝑖 𝜕𝑘 𝑉𝑗 − 2𝜕(𝑖 𝑉𝑘 𝜕𝑘 𝑉𝑗)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 61

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

]︂
3
2
− 𝛿𝑖𝑗 (𝜕𝑡 𝑉 ) − 𝛿𝑖𝑗 𝜕𝑘 𝑉𝑚 (𝜕𝑘 𝑉𝑚 − 𝜕𝑚 𝑉𝑘 ) .
4

61

(148c)

These involve many types of compact-support contributions, as well as quadratic-order and cubicorder parts; but, surprisingly, there are no quartically non-linear terms. Indeed it has been possible
to “integrate directly” all the quartic contributions in the 3PN metric; see the terms composed of
^ in the first of Eqs. (144).
𝑉 4 and 𝑉 𝑋
Note that the 3PN metric (144) does represent the inner post-Newtonian field of an isolated
system, because it contains, to this order, the correct radiation-reaction terms corresponding to
outgoing radiation. These terms come from the expansions of the retardations in the retarded
potentials (146) – (148); we elaborate more on radiation-reaction effects in the next Section 5.4.
The above potentials are not independent: They are linked together by some differential identities issued from the harmonic gauge conditions, which are equivalent, via the Bianchi identities,
to the equations of motion of the matter fields; see Eq. (27). These identities read
[︂
]︂
[︂
]︂}︂
{︂
4 ^ 1^
1 ^
2 3
1 1 ^
2
𝑊𝑘𝑘 + 2𝑉 + 4 𝑋 + 𝑍𝑘𝑘 + 𝑉 𝑊𝑘𝑘 + 𝑉
(149a)
𝜕𝑡 𝑉 + 2
𝑐 2
𝑐
2
2
3
{︂
[︂
]︂}︂
(︂
)︂
]︁
4 ^
1 ^
1 ^
1
2 [︁ ^
2
^
+ 𝜕𝑖 𝑉𝑖 + 2 𝑅
=𝒪 6 ,
𝑖 + 𝑉 𝑉𝑖 + 4 𝑌𝑖 − 𝑊𝑖𝑗 𝑉𝑗 + 𝑊𝑘𝑘 𝑉𝑖 + 𝑉 𝑅𝑖 + 𝑉 𝑉𝑖
𝑐
𝑐
2
2
𝑐
[︂
]︂}︂
(︂ )︂
{︂
{︂
]︁}︂
4 ^
1^
1 ^
1
2 [︁ ^
^
𝜕𝑡 𝑉𝑖 + 2 𝑅𝑖 + 𝑉 𝑉𝑖 + 𝜕𝑗 𝑊𝑖𝑗 − 𝑊𝑘𝑘 𝛿𝑖𝑗 + 2 𝑍𝑖𝑗 − 𝑍𝑘𝑘 𝛿𝑖𝑗
=𝒪 4 .
(149b)
𝑐
2
𝑐
2
𝑐
For latter applications to systems of compact objects, let us give the geodesic equations of a
particle moving in the 3.5PN metric (144).36 It is convenient to write these equations as
d𝑃 𝑖
= 𝐹𝑖 ,
d𝑡

(150)

where the “linear momentum density” 𝑃 𝑖 and the “force density” 𝐹 𝑖 of the particle are given by
𝑔𝑖𝜇 𝑣 𝜇
𝑃𝑖 = 𝑐√
,
−𝑔𝜌𝜎 𝑣 𝜌 𝑣 𝜎
𝑐 𝜕𝑖 𝑔𝜇𝜈 𝑣 𝜇 𝑣 𝜈
𝐹𝑖 = √
,
2 −𝑔𝜌𝜎 𝑣 𝜌 𝑣 𝜎

(151a)
(151b)

where 𝑣 𝜇 = (𝑐, 𝑣 𝑖 ) with 𝑣 𝑖 = d𝑥𝑖 /d𝑡 being the particle’s ordinary coordinate velocity, and where the
metric components are taken at the location of the particle. Notice that we are here viewing the
particle as moving in the fixed background metric (144). In Part B of this article, the metric will
be generated by the system of particles itself, and we shall have to supplement the computation of
the metric at the location of one of these particles by a suitable self-field regularization.
The expressions of both 𝑃 𝑖 and 𝐹 𝑖 in terms of the non-linear potentials follow from insertion of the 3.5PN metric coefficients (144). We obtain some complicated-looking (but useful in
applications) sums of products of potentials given by
(︂
)︂
1 1 2 𝑖
𝑃 𝑖 = 𝑣𝑖 + 2
𝑣 𝑣 + 3𝑉 𝑣 𝑖 − 4𝑉𝑖
(152a)
𝑐
2
(︂
)︂
9
1 3 4 𝑖 7 2 𝑖
^ 𝑖𝑗 𝑣 𝑗 − 8𝑅
^𝑖
𝑣 𝑣 + 𝑉 𝑣 𝑣 − 4𝑉𝑗 𝑣 𝑖 𝑣 𝑗 − 2𝑉𝑖 𝑣 2 + 𝑉 2 𝑣 𝑖 − 4𝑉 𝑉𝑖 + 4𝑊
+ 4
𝑐
8
2
2
36 Of course the geodesic equations are appropriate for the motion of particles without spins; for spinning particles
one has also to take into account the coupling of the spin to the space-time curvature, see Eq. (377).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 62

62

Luc Blanchet

1
+ 6
𝑐

(︂

5 6 𝑖 33 4 𝑖 3
49
^ 𝑖𝑗 𝑣 𝑗 𝑣 2
𝑣 𝑣 + 𝑉 𝑣 𝑣 − 𝑉𝑖 𝑣 4 − 6𝑉𝑗 𝑣 𝑖 𝑣 𝑗 𝑣 2 + 𝑉 2 𝑣 2 𝑣 𝑖 + 2𝑊
16
8
2
4
^ 𝑗𝑘 𝑣 𝑖 𝑣 𝑗 𝑣 𝑘 − 10𝑉 𝑉𝑖 𝑣 2 − 20𝑉 𝑉𝑗 𝑣 𝑖 𝑣 𝑗 − 4𝑅
^ 𝑖 𝑣 2 − 8𝑅
^ 𝑗 𝑣 𝑖 𝑣 𝑗 + 9 𝑉 3 𝑣 𝑖 + 12𝑉𝑗 𝑉𝑗 𝑣 𝑖
+2𝑊
2
(︂ )︂
)︁
1
𝑗
𝑖
𝑗
2
^
^
^
^
^
^
+12𝑊𝑖𝑗 𝑉 𝑣 + 12𝑋𝑣 + 16𝑍𝑖𝑗 𝑣 − 10𝑉 𝑉𝑖 − 8𝑊𝑖𝑗 𝑉𝑗 − 8𝑉 𝑅𝑖 − 16𝑌𝑖 + 𝒪 8 ,
𝑐
(︂
)︂
1
3
𝑖
2
𝑗
𝐹 = 𝜕𝑖 𝑉 + 2 −𝑉 𝜕𝑖 𝑉 + 𝜕𝑖 𝑉 𝑣 − 4𝜕𝑖 𝑉𝑗 𝑣
(152b)
𝑐
2
(︂
1 7
9
^ 𝑗𝑘 𝑣 𝑗 𝑣 𝑘
+ 4
𝜕𝑖 𝑉 𝑣 4 − 2𝜕𝑖 𝑉𝑗 𝑣 𝑗 𝑣 2 + 𝑉 𝜕𝑖 𝑉 𝑣 2 + 2𝜕𝑖 𝑊
𝑐
8
2
)︂
1 2
𝑗
𝑗
𝑗
^
^
−4𝑉𝑗 𝜕𝑖 𝑉 𝑣 − 4𝑉 𝜕𝑉𝑗 𝑣 − 8𝜕𝑖 𝑅𝑗 𝑣 + 𝑉 𝜕𝑖 𝑉 + 8𝑉𝑗 𝜕𝑖 𝑉𝑗 + 4𝜕𝑖 𝑋
2
(︂
3
49
1 11 6
^ 𝑗𝑘 𝑣 2 𝑣 𝑗 𝑣 𝑘 − 10𝑉𝑗 𝜕𝑖 𝑉 𝑣 2 𝑣 𝑗 − 10𝑉 𝜕𝑖 𝑉𝑗 𝑣 2 𝑣 𝑗
𝑣 𝜕𝑖 𝑉 − 𝜕𝑖 𝑉𝑗 𝑣 𝑗 𝑣 4 + 𝑉 𝜕𝑖 𝑉 𝑣 4 + 𝜕𝑖 𝑊
+ 6
𝑐
16
2
8
^ 𝑗𝑘 𝜕𝑖 𝑉 𝑣 𝑗 𝑣 𝑘 + 6𝑉 𝜕𝑖 𝑊
^ 𝑗𝑘 𝑣 𝑗 𝑣 𝑘
^ 𝑗 𝑣 2 𝑣 𝑗 + 27 𝑉 2 𝜕𝑖 𝑉 𝑣 2 + 12𝑉𝑗 𝜕𝑖 𝑉𝑗 𝑣 2 + 6𝑊
−4𝜕𝑖 𝑅
4
^ 𝑗𝑘 𝑣 𝑗 − 8𝑊
^ 𝑗𝑘 𝜕𝑖 𝑉𝑘 𝑣 𝑗
+6𝜕𝑖 ^
𝑋𝑣 2 + 8𝜕𝑖 𝑍^𝑗𝑘 𝑣 𝑗 𝑣 𝑘 − 20𝑉𝑗 𝑉 𝜕𝑖 𝑉 𝑣 𝑗 − 10𝑉 2 𝜕𝑖 𝑉𝑗 𝑣 𝑗 − 8𝑉𝑘 𝜕𝑖 𝑊
^ 𝑗 𝜕𝑖 𝑉 𝑣 𝑗 − 8𝑉 𝜕𝑖 𝑅
^ 𝑗 𝑣 𝑗 − 16𝜕𝑖 𝑌^𝑗 𝑣 𝑗 − 1 𝑉 3 𝜕𝑖 𝑉 − 4𝑉𝑗 𝑉𝑗 𝜕𝑖 𝑉 + 16𝑅
^ 𝑗 𝜕𝑖 𝑉𝑗 + 16𝑉𝑗 𝜕𝑖 𝑅
^𝑗
−8𝑅
6
)︂
(︂
)︁
^ 𝑖 𝑉 − 4𝑉 𝜕𝑖 𝑋
^ + 16𝜕𝑖 𝑇^ + 𝒪 1 .
−8𝑉 𝑉𝑗 𝜕𝑖 𝑉𝑗 − 4𝑋𝜕
𝑐8
Note that it will be supposed that all the accelerations appearing in the potentials and in the
final expression of the equations of motion are order-reduced by means of the equations of motion
themselves. For instance, we see from Eq. (152a) that when computing the time-derivative of 𝑃𝑖
we shall meet an acceleration at 1PN order which is therefore to be replaced by the explicit 2.5PN
equations of motion. The order-reduction is a crucial aspect of the post-Newtonian method. It is
justified by the fact that the matter equations of motion, say ∇𝜇 𝑇 𝛼𝜇 = 0, represent four out of the
ten Einstein field equations, see Section 2.1 for discussion. In the harmonic-coordinate approach the
equations of motion are equivalent to the harmonic gauge conditions 𝜕𝜇 ℎ𝛼𝜇 = 0. Thus, each time
we get an acceleration in some PN expression (including the PN expression of the acceleration
itself), we have also another equation (or the same equation) which tells that the acceleration
is given by another PN expression. The post-Newtonian method assumes that it is legitimate
to replace that acceleration and to re-expand consistently with the PN order. Post-Newtonian
predictions based on such consistent PN order-reduction have been very successful.37

5.4

Radiation reaction potentials to 4PN order

We said that the metric (144) contains the correct radiation-reaction terms appropriate for an
isolated system up to the 3.5PN level included. The metric can even be generalized to include the
radiation-reaction terms up to 4PN order. To show this we shall use a particular non-harmonic
coordinate system to describe the radiation reaction terms up to 4PN order, which constitutes a
natural generalization of the Burke & Thorne [114, 113] coordinate system at 2.5PN order. Recall
that at the lowest 2.5PN order the radiation reaction force takes the simple form of Eq. (6), in
37 Note, however, that the operation of order-reduction is illicit at the level of the Lagrangian. In fact, it is known

that the elimination of acceleration terms in a Lagrangian by substituting the equations of motion derived from that
Lagrangian, results in a different Lagrangian whose equations of motion differ from those of the original Lagrangian
by a gauge transformation [374].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 63

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

which the force 𝐹𝑖reac = 𝜌 𝜕𝑖 𝑉 reac involves only a scalar potential given by
(︂ )︂
𝐺 𝑖 𝑗 (5)
1
reac
𝑉
(x, 𝑡) = − 5 𝑥 𝑥 Q𝑖𝑗 (𝑡) + 𝒪 7 .
5𝑐
𝑐

63

(153)

At such dominant 2.5PN level (“Newtonian” radiation reaction) the source quadrupole moment
Q𝑖𝑗 is simply given by the usual Newtonian expression (3).
The novel feature when one extends the Newtonian radiation reaction to include the 1PN
corrections is that the reaction force is no longer composed of a single scalar depending on the
mass-type multipole moments, but involves also a vectorial component depending in particular on
the current-type quadrupole moment. This was noticed in the physically restricted case where the
dominant quadrupolar radiation from the source is suppressed [56]. The vectorial component of
the reaction force could be important in some astrophysical situations like rotating neutron stars
undergoing gravitational instabilities. Here we report the results of the extension to 1.5PN order
of the lowest-order Burke & Thorne scalar radiation reaction potential (153), in some appropriate
coordinate system, following Refs. [43, 47].
At that level (corresponding to 4PN order in the metric), and in this particular coordinate
system, it suffices to incorporate some radiation-reaction contributions into the scalar and vectorial
potentials 𝑉 and 𝑉𝑖 which parametrize the metric in Eq. (144). We thus pose
𝒱 = 𝑉 inst + 𝑉 reac ,

(154a)

𝒱𝑖 = 𝑉𝑖inst + 𝑉𝑖reac .

(154b)

Then the metric, accurate to 4PN order regarding the radiation-reaction contributions – we indicate
this by using the symbol 𝒪reac for the remainders – reads
(︂
)︂
2
1
2
,
(155a)
𝑔00 = −1 + 2 𝒱 − 4 𝒱 2 + 𝒪reac
𝑐
𝑐
𝑐11
(︂
)︂
4
1
𝑔0𝑖 = − 3 𝒱𝑖 + 𝒪reac
,
(155b)
𝑐
𝑐10
]︂
(︂ )︂
[︂
1
2
𝑔𝑖𝑗 = 𝛿𝑖𝑗 1 + 2 𝒱 + 𝒪reac
.
(155c)
𝑐
𝑐9
The other contributions, which are conservative (i.e., non radiative), are given up to 3PN order by
the metric (144) in which all the potentials take the same form as in Eqs. (146) – (148), but where
one neglects all the retardations, which means that the retarded integral operator −1
ret should be
replaced by the operator of the instantaneous potentials −1
defined
by
Eq.
(134).
This is for
inst
instance what we have indicated in Eqs. (154) by writing 𝑉 inst and 𝑉𝑖inst . Up to 3.5PN order, in
this particular coordinate system, the effect of all these retardations gets replaced by the effect
of the radiation-reaction potentials 𝑉 reac and 𝑉𝑖reac ; furthermore, at the 4PN order there is a
modification of the scalar radiation-reaction potential that is imposed by gravitational-wave tails
propagating in the wave zone [58]. The explicit form of these potentials is [43, 47]38
[︂
]︂
𝐺 1 𝑖𝑗𝑘 (7)
1
𝐺
(5)
(7)
𝑥 I𝑖𝑗𝑘 (𝑡) − x2 𝑥𝑖𝑗 I𝑖𝑗 (𝑡)
𝑉 reac (x, 𝑡) = − 5 𝑥𝑖𝑗 I𝑖𝑗 (𝑡) + 7
5𝑐
𝑐 189
70
)︂
]︂
(︂ )︂
[︂ (︂
∫︁ +∞
2
4𝐺 M 𝑖𝑗
11
1
𝑐𝜏
(7)
−
+
+
𝒪
𝑥
d𝜏
I
(𝑡
−
𝜏
)
ln
,
(156a)
𝑖𝑗
9
5𝑐8
2𝑟
12
𝑐
0
0
38 Recall the footnote 17 for our notation. In particular 𝑥
^𝑖𝑗𝑘 in the vector potential denotes the STF combination
2
𝑥
^𝑖𝑗𝑘 = 𝑥𝑖𝑗𝑘 − 𝑟5 (𝑥𝑖 𝛿 𝑗𝑘 + 𝑥𝑗 𝛿 𝑘𝑖 + 𝑥𝑘 𝛿 𝑖𝑗 ) with 𝑥𝑖𝑗𝑘 = 𝑥𝑖 𝑥𝑗 𝑥𝑘 .

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 64

64

Luc Blanchet

𝐺
𝑉𝑖reac (x, 𝑡) = 5
𝑐

[︂

]︂
(︂ )︂
4
1
1 𝑖𝑗𝑘 (6)
𝑗𝑙 (5)
𝑥
^ I𝑗𝑘 (𝑡) −
𝜖𝑖𝑗𝑘 𝑥 J𝑘𝑙 (𝑡) + 𝒪 7 ,
21
45
𝑐

(156b)

where the multipole moments I𝐿 and J𝐿 denote the source multipole moments defined in Eqs. (123).
Witness the tail integral at 4PN order characterized by a logarithmic kernel; see Section 3.2.
The scalar potential 𝑉 reac will obviously reproduce Eq. (153) at the dominant order. However,
note that it is crucial to include in Eq. (156a) the 1PN correction in the source quadrupole moment
I𝑖𝑗 . The mass-type moments I𝐿 to 1PN order (and the current-type J𝐿 to Newtonian order), read
{︂
}︂
(︂ )︂
∫︁
1
4(2ℓ + 1)
1
3
2
2
I𝐿 = d x 𝑥
^𝐿 𝜎 + 2
(157a)
x 𝑥
^𝐿 𝜕𝑡 𝜎 − 2
𝑥
^𝑖𝐿 𝜕𝑡 𝜎𝑖 + 𝒪 4 ,
2𝑐 (2ℓ + 3)
𝑐 (ℓ + 1)(2ℓ + 3)
𝑐
(︂ )︂
∫︁
1
J𝐿 = d3 x 𝜖𝑎𝑏<𝑖ℓ 𝑥
(157b)
^𝐿−1>𝑎 𝜎𝑏 + 𝒪 2 .
𝑐
The matter source densities 𝜎 and 𝜎𝑖 are given in Eqs. (145). Note that the mass multipole
moments I𝐿 extend only over the compact support of the source even at the 1PN order. Only at
the 2PN order will they involve some non-compact supported contributions – i.e., some integrals
extending up to infinity [44].
The 3.5PN radiation reaction force in the equations of motion of compact binary systems has
been derived by Iyer & Will [258, 259] in an arbitrary gauge, based on the energy and angular momentum balance equations at the relative 1PN order. As demonstrated in Ref. [259] the expressions
of the radiation scalar and vector radiation-reaction potentials (156), which are valid in a particular
gauge but are here derived from first principles, are fully consistent with the works [258, 259].
With the radiation-reaction potentials (156) in hands, one can prove [47] the energy balance
equation up to 1.5PN order, namely
(︂
[︂ (︂
)︂
]︂)︂2
∫︁
d𝐸 4PN
𝐺
𝑐𝜏
2𝐺M +∞
11
(3)
(5)
= − 5 I𝑖𝑗 + 3
d𝜏 I𝑖𝑗 (𝑡 − 𝜏 ) ln
+
d𝑡
5𝑐
𝑐
2𝑟0
12
0
]︂
(︂ )︂
[︂
1
𝐺 1 (4) (4) 16 (3) (3)
I I + J J
+𝒪 9 .
− 7
𝑐 189 𝑖𝑗𝑘 𝑖𝑗𝑘 45 𝑖𝑗 𝑖𝑗
𝑐

(158)

One recognizes in the right-hand side the known positive-definite expression for the energy flux at
1.5PN order. Indeed the effective quadrupole moment which appears in the parenthesis of (158)
agrees with the tail-modified radiative quadrupole moment U𝑖𝑗 parametrizing the field in the far
zone; see Eq. (90) where we recall that M𝐿 and I𝐿 are identical up to 2.5PN order.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 65

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

65

Part B: Compact Binary Systems
The problem of the motion and gravitational radiation of compact objects in post-Newtonian
approximations is of crucial importance, for at least three reasons listed in the Introduction of this
article: Motion of N planets in the solar system; gravitational radiation reaction force in binary
pulsars; direct detection of gravitational waves from inspiralling compact binaries. As discussed
in Section 1.3, the appropriate theoretical description of inspiralling compact binaries is by two
structureless point-particles, characterized solely by their masses 𝑚1 and 𝑚2 (and possibly their
spins), and moving on a quasi-circular orbit.
Strategies to detect and analyze the very weak signals from compact binary inspiral involve
matched filtering of a set of accurate theoretical template waveforms against the output of the detectors. Many analyses [139, 137, 198, 138, 393, 346, 350, 284, 157, 158, 159, 156, 105, 106, 3, 18, 111]
have shown that, in order to get sufficiently accurate theoretical templates, one must include postNewtonian effects up to the 3PN level or higher. Recall that in practice, the post-Newtonian templates for the inspiral phase have to be matched to numerical-relativity results for the subsequent
merger and ringdown phases. The match proceeds essentially through two routes: Either the socalled Hybrid templates obtained by direct matching between the PN expanded waveform and the
numerical computations [4, 371], or the Effective-One-Body (EOB) templates [108, 109, 161, 168]
that build on post-Newtonian results and extend their realm of validity to facilitate the analytical
comparison with numerical relativity [112, 329]. Note also that various post-Newtonian resummation techniques, based on Padé approximants, have been proposed to improve the efficiency of PN
templates [157, 158, 161].

6

Regularization of the Field of Point Particles

Our aim is to compute the metric (and its gradient needed in the equations of motion) at the 3PN
order (say) for a system of two point-like particles. A priori one is not allowed to use directly
some metric expressions like Eqs. (144) above, which have been derived under the assumption of
a continuous (smooth) matter distribution. Applying them to a system of point particles, we find
that most of the integrals become divergent at the location of the particles, i.e., when x → 𝑦1 (𝑡)
or 𝑦2 (𝑡), where 𝑦1 (𝑡) and 𝑦2 (𝑡) denote the two trajectories. Consequently, we must supplement
the calculation by a prescription for how to remove the infinite part of these integrals. At this
stage different choices for a “self-field” regularization (which will take care of the infinite self-field
of point particles) are possible. In this section we review the:
1. Hadamard self-field regularization, which has proved to be very convenient for doing practical computations (in particular, by computer), but suffers from the important drawback of
yielding some ambiguity parameters, which cannot be determined within this regularization,
starting essentially at the 3PN order;
2. Dimensional self-field regularization, an extremely powerful regularization which is free of any
ambiguities (at least up to the 3PN level), and therefore permits to uniquely fix the values
of the ambiguity parameters coming from Hadamard’s regularization. However, dimensional
regularization has not yet been implemented to the present problem in the general case (i.e.,
for an arbitrary space dimension 𝑑 ∈ C).
The why and how the final results are unique and independent of the employed self-field regularization (in agreement with the physical expectation) stems from the effacing principle of general
relativity [142] – namely that the internal structure of the compact bodies makes a contribution
only at the formal 5PN approximation. However, we shall review several alternative computations,
independent of the self-field regularization, which confirm the end results.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 66

66

Luc Blanchet

6.1

Hadamard self-field regularization

In most practical computations we employ the Hadamard regularization [236, 381] (see Ref. [382]
for an entry to the mathematical literature). Let us present here an account of this regularization,
as well as a theory of generalized functions (or pseudo-functions) associated with it, following the
detailed investigations in Refs. [70, 72].
Consider the class ℱ of functions 𝐹 (x) which are smooth (𝐶 ∞ ) on R3 except for the two points
𝑦1 and 𝑦2 , around which they admit a power-like singular expansion of the type:39
∀𝒩 ∈ N,

𝐹 (x) =

∑︁

𝑟1𝑎 𝑓𝑎 (n1 ) + 𝑜(𝑟1𝒩 ) ,

𝑎0 ⩽𝑎⩽𝒩

(159)

1

and similarly for the other point 2. Here 𝑟1 = |x − 𝑦1 | → 0, and the coefficients 1 𝑓𝑎 of the various
powers of 𝑟1 depend on the unit direction n1 = (x − 𝑦1 )/𝑟1 of approach to the singular point.
The powers 𝑎 of 𝑟1 are real, range in discrete steps [i.e., 𝑎 ∈ (𝑎𝑖 )𝑖∈N ], and are bounded from
below (𝑎0 ⩽ 𝑎). The coefficients 1 𝑓𝑎 (and 2 𝑓𝑎 ) for which 𝑎 < 0 can be referred to as the singular
coefficients of 𝐹 . If 𝐹 and 𝐺 belong to ℱ so does the ordinary product 𝐹 𝐺, as well as the ordinary
gradient 𝜕𝑖 𝐹 . We define the Hadamard partie finie of 𝐹 at the location of the point 1 where it is
singular as
∫︁
dΩ1
(160)
𝑓0 (n1 ) ,
(𝐹 )1 =
4𝜋 1
where dΩ1 = dΩ(n1 ) denotes the solid angle element centered on 𝑦1 and of direction n1 . Notice
that because of the angular integration in Eq. (160), the Hadamard partie finie is “non-distributive”
in the sense that
(𝐹 𝐺)1 ̸= (𝐹 )1 (𝐺)1 in general .
(161)
The non-distributivity of Hadamard’s partie finie is the main source of the appearance of ambiguity
parameters at the 3PN order, as discussed in Section 6.2.
∫︀
The second notion of Hadamard partie finie (Pf) concerns that of the integral d3 x 𝐹 , which
is generically divergent at the location of the two singular points 𝑦1 and 𝑦2 (we assume that the
integral converges at infinity). It is defined by
∫︁
Pf 𝑠1 𝑠2

{︃∫︁

3

d x 𝐹 = lim

𝑠→0

(︂ )︂
∑︁ 𝑠𝑎+3 (︂ 𝐹 )︂
𝑠 (︀ 3 )︀
d x 𝐹 + 4𝜋
𝑟1 𝐹 1 + 1 ↔ 2
+
4𝜋
ln
𝑎
𝑎 + 3 𝑟1 1
𝑠1
𝒮(𝑠)
𝑎+3<0
3

}︃
.

(162)
The first term integrates over a domain 𝒮(𝑠) defined as R3 from which the two spherical balls 𝑟1 ⩽ 𝑠
and 𝑟2 ⩽ 𝑠 of radius 𝑠 and centered on the two singularities, denoted ℬ(𝑦1 , 𝑠) and ℬ(𝑦2 , 𝑠), are
excised: 𝒮(𝑠) ≡ R3 ∖ ℬ(𝑦1 , 𝑠) ∪ ℬ(𝑦2 , 𝑠). The other terms, where the value of a function at point 1
takes the meaning (160), are precisely such that they cancel out the divergent part of the first term
in the limit where 𝑠 → 0 (the symbol 1 ↔ 2 means the same terms but corresponding to the other
point 2). The Hadamard partie-finie integral depends on two strictly positive constants 𝑠1 and 𝑠2 ,
associated with the logarithms present in Eq. (162). We shall look for the fate of these constants
in the final equations of motion and radiation field. See Ref. [70] for alternative expressions of the
partie-finie integral.
We now come to a specific variant of Hadamard’s regularization called the extended Hadamard
regularization (EHR) and defined in Refs. [70, 72]. The basic idea is to associate to any 𝐹 ∈ ℱ
39 The function 𝐹 (x) depends also on (coordinate) time 𝑡, through for instance its dependence on the velocities
𝑣1 (𝑡) and 𝑣2 (𝑡), but the time 𝑡 is purely “spectator” in the regularization process, and thus will not be indicated.
See the footnote 20 for the definition of the Landau symbol 𝑜 for remainders.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 67

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

67

a pseudo-function, called the partie finie pseudo-function Pf𝐹 , namely a linear form acting on
functions 𝐺 of ℱ, and which is defined by the duality bracket
∫︁
∀𝐺 ∈ ℱ,
⟨Pf𝐹, 𝐺⟩ = Pf d3 x 𝐹 𝐺 .
(163)
When restricted to the set 𝒟 of smooth functions, i.e., 𝐶 ∞ (R4 ), with compact support (obviously
we have 𝒟 ⊂ ℱ), the pseudo-function Pf𝐹 is a distribution in the sense of Schwartz [381]. The
product of pseudo-functions coincides, by definition, with the ordinary point-wise product, namely
Pf𝐹 ·Pf𝐺 = Pf(𝐹 𝐺). In practical computations, we use an interesting pseudo-function, constructed
on the basis of the Riesz delta function [365], which plays a role analogous to the Dirac measure
in distribution theory, 𝛿1 (x) ≡ 𝛿(x − 𝑦1 ). This is the delta-pseudo-function Pf𝛿1 defined by
∫︁
∀𝐹 ∈ ℱ,
⟨Pf𝛿1 , 𝐹 ⟩ = Pf d3 x 𝛿1 𝐹 = (𝐹 )1 ,
(164)
where (𝐹 )1 is the partie finie of 𝐹 as given by Eq. (160). From the product of Pf𝛿1 with any Pf𝐹
we obtain the new pseudo-function Pf(𝐹 𝛿1 ), that is such that
∀𝐺 ∈ ℱ,

⟨Pf(𝐹 𝛿1 ), 𝐺⟩ = (𝐹 𝐺)1 .

(165)

As a general rule, we are not allowed, in consequence of the “non-distributivity” of the Hadamard
partie finie, Eq. (161), to replace 𝐹 within the pseudo-function Pf(𝐹 𝛿1 ) by its regularized value:
Pf(𝐹 𝛿1 ) ̸= (𝐹 )1 Pf𝛿1 in general. It should be noticed that the object Pf(𝐹 𝛿1 ) has no equivalent in
distribution theory.
Next, we treat the spatial derivative of a pseudo-function of the type Pf𝐹 , namely 𝜕𝑖 (Pf𝐹 ).
Essentially, we require [70] that the rule of integration by parts holds. By this we mean that we are
allowed to freely operate by parts any duality bracket, with the all-integrated (“surface”) terms
always being zero, as in the case of non-singular functions. This requirement is motivated by our
will that a computation involving singular functions be as much as possible the same as if we were
dealing with regular functions. Thus, by definition,
∀𝐹, 𝐺 ∈ ℱ,

⟨𝜕𝑖 (Pf𝐹 ), 𝐺⟩ = −⟨𝜕𝑖 (Pf𝐺), 𝐹 ⟩ .

(166)

Furthermore, we assume that when all the singular coefficients of 𝐹 vanish, the derivative of Pf𝐹
reduces to the ordinary derivative, i.e., 𝜕𝑖 (Pf𝐹 ) = Pf(𝜕𝑖 𝐹 ). Then it is trivial to check that the
rule (166) contains as a particular case the standard definition of the distributional derivative [381].
Notably, we see that the integral of a gradient is always zero: ⟨𝜕𝑖 (Pf𝐹 ), 1⟩ = 0. This should
certainly be the case if we want to compute a quantity like a Hamiltonian density which is defined
only modulo a total divergence. We pose
𝜕𝑖 (Pf𝐹 ) = Pf(𝜕𝑖 𝐹 ) + D𝑖 [𝐹 ],

(167)

where Pf(𝜕𝑖 𝐹 ) represents the “ordinary” derivative and D𝑖 [𝐹 ] is the distributional term. The
following solution of the basic relation (166) was obtained in Ref. [70]:
(︃ [︂
]︂ )︃
∑︁ 1
𝑖 1
D𝑖 [𝐹 ] = 4𝜋 Pf 𝑛1 𝑟1 𝑓−1 +
𝑓−2−𝑘 𝛿1 + 1 ↔ 2 ,
(168)
2
𝑟𝑘 1
1
𝑘⩾0 1
where for simplicity we assume that the powers 𝑎 in the expansion (159) of 𝐹 are relative integers.
The distributional term (168) is of the form Pf(𝐺𝛿1 ) plus 1 ↔ 2; it is generated solely by the

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 68

68

Luc Blanchet

singular coefficients of 𝐹 .40 The formula for the distributional term associated with the ℓ-th
distributional derivative, i.e. D𝐿 [𝐹 ] = 𝜕𝐿 Pf𝐹 − Pf𝜕𝐿 𝐹 , where 𝐿 = 𝑖1 𝑖2 · · · 𝑖ℓ , reads
D𝐿 [𝐹 ] =

ℓ
∑︁

𝜕𝑖1 ...𝑖𝑘−1 D𝑖𝑘 [𝜕𝑖𝑘+1 ...𝑖ℓ 𝐹 ] .

(169)

𝑘=1

We refer to Theorem 4 in Ref. [70] for the definition of another derivative operator, representing
the most general derivative satisfying the same properties as the one defined by Eq. (168), and, in
addition, the commutation of successive derivatives (or Schwarz lemma).41
The distributional derivative defined by (167) – (168) does not satisfy the Leibniz rule for the
derivation of a product, in accordance with a general result of Schwartz [380]. Rather, the investigation of Ref. [70] suggests that, in order to construct a consistent theory (using the ordinary
point-wise product for pseudo-functions), the Leibniz rule should be weakened, and replaced by
the rule of integration by part, Eq. (166), which is in fact nothing but an integrated version of the
Leibniz rule. However, the loss of the Leibniz rule stricto sensu constitutes one of the reasons for
the appearance of the ambiguity parameters at 3PN order, see Section 6.2.
The Hadamard regularization (𝐹 )1 is defined by Eq. (160) in a preferred spatial hypersurface
𝑡 = const of a coordinate system, and consequently is not a priori compatible with the Lorentz
invariance. Thus we expect that the equations of motion in harmonic coordinates (which manifestly
preserve the global Lorentz invariance) should exhibit at some stage a violation of the Lorentz
invariance due to the latter regularization. In fact this occurs exactly at the 3PN order. Up to
the 2.5PN level, the use of the regularization (𝐹 )1 is sufficient to get some unambiguous equations
of motion which are Lorentz invariant [76]. This problem can be dealt with within Hadamard’s
regularization, by introducing a Lorentz-invariant variant of this regularization, denoted [𝐹 ]1 in
Ref. [72]. It consists of performing the Hadamard regularization within the spatial hypersurface
that is geometrically orthogonal (in a Minkowskian sense) to the four-velocity of the particle. The
regularization [𝐹 ]1 differs from the simpler regularization (𝐹 )1 by relativistic corrections of order
1/𝑐2 at least. See [72] for the formulas defining this regularization in the form of some infinite power
series in 1/𝑐2 . The regularization [𝐹 ]1 plays a crucial role in obtaining the equations of motion at
the 3PN order in Refs. [69, 71]. In particular, the use of the Lorentz-invariant regularization [𝐹 ]1
permits to obtain the value of the ambiguity parameter 𝜔kinetic in Eq. (170a) below.

6.2

Hadamard regularization ambiguities

The standard Hadamard regularization yields some ambiguous results for the computation of
certain integrals at the 3PN order, as noticed by Jaranowski & Schäfer [261, 262, 263] in their
computation of the equations of motion within the ADM-Hamiltonian formulation of general relativity. By standard Hadamard regularization we mean the regularization based solely on the
definitions of the partie finie of a singular function, Eq. (160), and the partie finie of a divergent
integral, Eq. (162), and without using a theory of pseudo-functions and generalized distributional
derivatives as in Refs. [70, 72]. It was shown in Refs. [261, 262, 263] that there are two and only two
types of ambiguous terms in the 3PN Hamiltonian, which were then parametrized by two unknown
numerical coefficients called 𝜔static and 𝜔kinetic .
Progressing concurrently, Blanchet & Faye [70, 72] introduced the “extended” Hadamard regularization – the one we outlined in Section 6.1 – and obtained [69, 71] the 3PN equations of motion
40 The sum over 𝑘 in Eq. (168) is always finite since there is a maximal order 𝑎 of divergency in Eq. (159).
0
41 It was shown in Ref. [71] that using one or the other of these derivatives results in some equations of motion

that differ by a coordinate transformation, and the redefinition of some ambiguity parameter. This indicates that
the distributional derivatives introduced in Ref. [70] constitute some technical tools devoid of physical meaning
besides precisely the appearance of Hadamard’s ambiguity parameters.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 69

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

69

complete except for one and only one unknown numerical constant, called 𝜆. The new extended
Hadamard regularization is mathematically well-defined and yields unique results for the computation of any integral in the problem; however, it turned out to be in a sense “incomplete” as it could
not determine the value of this constant. The comparison of the result with the work [261, 262],
on the basis of the computation of the invariant energy of compact binaries moving on circular
orbits, revealed [69] that
41
,
24
11
1987
𝜔static = − 𝜆 −
.
3
840

𝜔kinetic =

(170a)
(170b)

Therefore, the ambiguity 𝜔kinetic is fixed, while 𝜆 is equivalent to the other ambiguity 𝜔static .
Notice that the value (170a) for the kinetic ambiguity parameter 𝜔kinetic , which is in factor of
some velocity dependent terms, is the only one for which the 3PN equations of motion are Lorentz
invariant. Fixing up this value was possible because the extended Hadamard regularization [70, 72]
was defined in such a way that it keeps the Lorentz invariance.
The value of 𝜔kinetic given by Eq. (170a) was recovered in Ref. [162] by directly proving that
such value is the unique one for which the global Poincaré invariance of the ADM-Hamiltonian
formalism is verified. Since the coordinate conditions associated with the ADM formalism do not
manifestly respect the Poincaré symmetry, it was necessary to prove that the 3PN Hamiltonian is
compatible with the existence of generators for the Poincaré algebra. By contrast, the harmoniccoordinate conditions preserve the Poincaré invariance, and therefore the associated equations of
motion at 3PN order are manifestly Lorentz-invariant, as was found to be the case in Refs. [69, 71].
The appearance of one and only one physical unknown coefficient 𝜆 in the equations of motion
constitutes a quite striking fact, that is related specifically with the use of a Hadamard-type
regularization.42 Technically speaking, the presence of the ambiguity parameter 𝜆 is associated
with the non-distributivity of Hadamard’s regularization, in the sense of Eq. (161). Mathematically
speaking, 𝜆 is probably related to the fact that it is impossible to construct a distributional
derivative operator, such as Eqs. (167) – (168), satisfying the Leibniz rule for the derivation of the
product [380]. The Einstein field equations can be written in many different forms, by shifting the
derivatives and operating some terms by parts with the help of the Leibniz rule. All these forms
are equivalent in the case of regular sources, but since the derivative operator (167) – (168) violates
the Leibniz rule they become inequivalent for point particles.
Physically speaking, let us also argue that 𝜆 has its root in the fact that in a complete computation of the equations of motion valid for two regular extended weakly self-gravitating bodies, many
non-linear integrals, when taken individually, start depending, from the 3PN order, on the internal
structure of the bodies, even in the “compact-body” limit where the radii tend to zero. However,
when considering the full equations of motion, one expects that all the terms depending on the
internal structure can be removed, in the compact-body limit, by a coordinate transformation (or
by some appropriate shifts of the central world lines of the bodies), and that finally 𝜆 is given by a
pure number, for instance a rational fraction, independent of the details of the internal structure
of the compact bodies. From this argument (which could be justified by the effacing principle in
general relativity) the value of 𝜆 is necessarily the one we compute below, Eq. (172), and will be
valid for any compact objects, for instance black holes.
The ambiguity parameter 𝜔static , which is in factor of some static, velocity-independent term,
and hence cannot be derived by invoking Lorentz invariance, was computed by Damour, Jaranowski
42 Note also that the harmonic-coordinates 3PN equations of motion [69, 71] depend, in addition to 𝜆, on two

arbitrary constants 𝑟1′ and 𝑟2′ parametrizing some logarithmic terms. These constants are closely related to the
constants 𝑠1 and 𝑠2 in the partie-finie integral (162); see Ref. [71] and Eq. (185) below for the precise definition.
However, 𝑟1′ and 𝑟2′ are not “physical” in the sense that they can be removed by a coordinate transformation.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 70

70

Luc Blanchet

& Schäfer [163] by means of dimensional regularization, instead of some Hadamard-type one, within
the ADM-Hamiltonian formalism. Their result is
𝜔static = 0 .

(171)

As argued in [163], clearing up the static ambiguity is made possible by the fact that dimensional regularization, contrary to Hadamard’s regularization, respects all the basic properties of
the algebraic and differential calculus of ordinary functions: Associativity, commutativity and distributivity of point-wise addition and multiplication, Leibniz’s rule, and the Schwarz lemma. In
this respect, dimensional regularization is certainly superior to Hadamard’s one, which does not
respect the distributivity of the product [recall Eq. (161)] and unavoidably violates at some stage
the Leibniz rule for the differentiation of a product.
The ambiguity parameter 𝜆 is fixed from the result (171) and the necessary link (170b) provided
by the equivalence between the harmonic-coordinates and ADM-Hamiltonian formalisms [69, 164].
However, 𝜆 has also been computed directly by Blanchet, Damour & Esposito-Farèse [61] applying
dimensional regularization to the 3PN equations of motion in harmonic coordinates (in the line of
Refs. [69, 71]). The end result,
1987
,
(172)
𝜆=−
3080
is in full agreement with Eq. (171).43 Besides the independent confirmation of the value of 𝜔static or
𝜆, the work [61] provides also a confirmation of the consistency of dimensional regularization, since
the explicit calculations are entirely different from the ones of Ref. [163]: Harmonic coordinates
instead of ADM-type ones, work at the level of the equations of motion instead of the Hamiltonian,
a different form of Einstein’s field equations which is solved by a different iteration scheme.
Let us comment that the use of a self-field regularization, be it dimensional or based on
Hadamard’s partie finie, signals a somewhat unsatisfactory situation on the physical point of view,
because, ideally, we would like to perform a complete calculation valid for extended bodies, taking
into account the details of the internal structure of the bodies (energy density, pressure, internal
velocity field, etc.). By considering the limit where the radii of the objects tend to zero, one
should recover the same result as obtained by means of the point-mass regularization. This would
demonstrate the suitability of the regularization. This program was undertaken at the 2PN order
in Refs. [280, 234] which derived the equations of motion of two extended fluid balls, and obtained
equations of motion depending only on the two masses 𝑚1 and 𝑚2 of the compact bodies.44 At the
3PN order we expect that the extended-body program should give the value of the regularization
parameter 𝜆 – probably after a coordinate transformation to remove the terms depending on the
internal structure. Ideally, its value should also be confirmed by independent and more physical
methods like those of Refs. [407, 281, 172].
An important work, in several aspects more physical than the formal use of regularizations,
is the one of Itoh & Futamase [255, 253, 254], following previous investigations in Refs. [256,
257]. These authors derived the 3PN equations of motion in harmonic coordinates by means of a
particular variant of the famous “surface-integral” method à la Einstein, Infeld & Hoffmann [184].
The aim is to describe extended relativistic compact binary systems in the so-called strong-field
point particle limit which has been defined in Ref. [212]. This approach is interesting because it
is based on the physical notion of extended compact bodies in general relativity, and is free of the
problems of ambiguities. The end result of Refs. [255, 253] is in agreement with the 3PN harmonic
43 One may wonder why the value of 𝜆 is a complicated rational fraction while 𝜔
static is so simple. This is because
𝜔static was introduced precisely to measure the amount of ambiguities of certain integrals, while by contrast, 𝜆 was
introduced [see Eq. (185)] as an unknown constant entering the relation between the arbitrary scales 𝑟1′ , 𝑟2′ on the
one hand, and 𝑠1 , 𝑠2 on the other hand, which has a priori nothing to do with the ambiguous part of integrals.
44 See however some comments on the latter work in Ref. [145], pp. 168 – 169.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 71

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

71

coordinates equations of motion [69, 71] and is unambiguous, as it does directly determine the
ambiguity parameter 𝜆 to exactly the value (172).
The 3PN equations of motion in harmonic coordinates or, more precisely, the associated 3PN
Lagrangian, were also derived by Foffa & Sturani [203] using another important approach, coined
the effective field theory (EFT) [223]. Their result is fully compatible with the value (172) for the
ambiguity parameter 𝜆; however, in contrast with the surface-integral method of Refs. [255, 253],
this does not check the method of regularization because the EFT approach is also based on
dimensional self-field regularization.
We next consider the problem of the binary’s radiation field, where the same phenomenon
occurs, with the appearance of some Hadamard regularization ambiguity parameters at 3PN order.
More precisely, Blanchet, Iyer & Joguet [81], computing the 3PN compact binary’s mass quadrupole
moment I𝑖𝑗 , found it necessary to introduce three Hadamard regularization constants 𝜉, 𝜅, and 𝜁,
which are independent of the equation-of-motion related constant 𝜆. The total gravitational-wave
flux at 3PN order, in the case of circular orbits, was found to depend on a single combination of
the latter constants, 𝜃 = 𝜉 + 2𝜅 + 𝜁, and the binary’s orbital phase, for circular orbits, involved
only the linear combination of 𝜃 and 𝜆 given by 𝜃^ = 𝜃 − 73 𝜆, as shown in [73].
Dimensional regularization (instead of Hadamard’s) has next been applied in Refs. [62, 63] to
the computation of the 3PN radiation field of compact binaries, leading to the following unique
determination of the ambiguity parameters:45
9871
,
9240
𝜅 = 0,
7
𝜁=− .
33
𝜉=−

(173a)
(173b)
(173c)

These values represent the end result of dimensional regularization. However, several alternative calculations provide a check, independent of dimensional regularization, for all the parameters (173). One computes [80] the 3PN binary’s mass dipole moment I𝑖 using Hadamard’s regularization, and identifies I𝑖 with the 3PN center of mass vector position G𝑖 , already known as
a conserved integral associated with the Poincaré invariance of the 3PN equations of motion in
harmonic coordinates [174]. This yields 𝜉 + 𝜅 = −9871/9240 in agreement with Eqs. (173). Next,
one considers [65] the limiting physical situation where the mass of one of the particles is exactly
zero (say, 𝑚2 = 0), and the other particle moves with uniform velocity. Technically, the 3PN
quadrupole moment of a boosted Schwarzschild black hole is computed and compared with the
result for I𝑖𝑗 in the limit 𝑚2 = 0. The result is 𝜁 = −7/33, and represents a direct verification
of the global Poincaré invariance of the wave generation formalism (the parameter 𝜁 representing
the analogue for the radiation field of the parameter 𝜔kinetic ). Finally, one proves [63] that 𝜅 = 0
by showing that there are no dangerously divergent diagrams corresponding to non-zero 𝜅-values,
where a diagram is meant here in the sense of Ref. [151].
The determination of the parameters (173) completes the problem of the general relativistic
prediction for the templates of inspiralling compact binaries up to 3.5PN order. The numerical
values of these parameters indicate, following measurement-accuracy analyses [105, 106, 159, 156],
that the 3.5PN order should provide an excellent approximation for both the on-line search and
the subsequent off-line analysis of gravitational wave signals from inspiralling compact binaries in
the LIGO and VIRGO detectors.
45 The result for 𝜉 happens to be amazingly related to the one for 𝜆 by a cyclic permutation of digits; compare
3𝜉 = −9871/3080 with 𝜆 = −1987/3080.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 72

72

6.3

Luc Blanchet

Dimensional regularization of the equations of motion

As reviewed in Section 6.2, work at 3PN order using Hadamard’s self-field regularization showed
the appearance of ambiguity parameters, due to an incompleteness of the Hadamard regularization
employed for curing the infinite self field of point particles. We give here more details on the determination using dimensional regularization of the ambiguity parameter 𝜆 [or equivalently 𝜔static ,
see Eq. (170b)] which appeared in the 3PN equations of motion.
Dimensional regularization was invented as a means to preserve the gauge symmetry of perturbative quantum field theories [391, 91, 100, 131]. Our basic problem here is to respect the
gauge symmetry associated with the diffeomorphism invariance of the classical general relativistic
description of interacting point masses. Hence, we use dimensional regularization not merely as a
trick to compute some particular integrals which would otherwise be divergent, but as a powerful
tool for solving in a consistent way the Einstein field equations with singular point-mass sources,
while preserving its crucial symmetries. In particular, we shall prove that dimensional regularization determines the kinetic ambiguity parameter 𝜔kinetic (and its radiation-field analogue 𝜁), and is
therefore able to correctly keep track of the global Lorentz–Poincaré invariance of the gravitational
field of isolated systems. The dimensional regularization is also an important ingredient of the
EFT approach to equations of motion and gravitational radiation [223].
The Einstein field equations in 𝑑+1 space-time dimensions, relaxed by the condition of harmonic
coordinates 𝜕𝜇 ℎ𝛼𝜇 = 0, take exactly the same form as given in Eqs. (18) – (23). In particular the
box operator  now denotes the flat space-time d’Alembertian operator in 𝑑 + 1 dimensions with
signature (−1, 1, 1, · · · ). The gravitational constant 𝐺 is related to the usual three-dimensional
Newton’s constant 𝐺N by
𝐺 = 𝐺N ℓ𝑑−3
,
(174)
0
where ℓ0 denotes an arbitrary length scale. The explicit expression of the gravitational source term
Λ𝛼𝛽 involves some 𝑑-dependent coefficients, and is given by
1
2
Λ𝛼𝛽 = − ℎ𝜇𝜈 𝜕𝜇𝜈
ℎ𝛼𝛽 + 𝜕𝜇 ℎ𝛼𝜈 𝜕𝜈 ℎ𝛽𝜇 + 𝑔 𝛼𝛽 𝑔𝜇𝜈 𝜕𝜆 ℎ𝜇𝜏 𝜕𝜏 ℎ𝜈𝜆
2
− 𝑔 𝛼𝜇 𝑔𝜈𝜏 𝜕𝜆 ℎ𝛽𝜏 𝜕𝜇 ℎ𝜈𝜆 − 𝑔 𝛽𝜇 𝑔𝜈𝜏 𝜕𝜆 ℎ𝛼𝜏 𝜕𝜇 ℎ𝜈𝜆 + 𝑔𝜇𝜈 𝑔 𝜆𝜏 𝜕𝜆 ℎ𝛼𝜇 𝜕𝜏 ℎ𝛽𝜈
(︁
)︁
1
1
+ (2𝑔 𝛼𝜇 𝑔 𝛽𝜈 − 𝑔 𝛼𝛽 𝑔 𝜇𝜈 ) 𝑔𝜆𝜏 𝑔𝜖𝜋 −
𝑔𝜏 𝜖 𝑔𝜆𝜋 𝜕𝜇 ℎ𝜆𝜋 𝜕𝜈 ℎ𝜏 𝜖 .
4
𝑑−1

(175)

When 𝑑 = 3 we recover Eq. (24). In the following we assume, as usual in dimensional regularization,
that the dimension of space is a complex number, 𝑑 ∈ C, and prove many results by invoking
complex analytic continuation in 𝑑. We shall often pose 𝜀 ≡ 𝑑 − 3.
We parametrize the 3PN metric in 𝑑 dimensions by means of some retarded potentials 𝑉 , 𝑉𝑖 ,
^ 𝑖𝑗 , . . . , which are straightforward 𝑑-dimensional generalizations of the potentials used in three
𝑊
dimensions and which were defined in Section 5.3. Those are obtained by post-Newtonian iteration
of the 𝑑-dimensional field equations, starting from appropriate definitions of matter source densities
generalizing Eqs. (145):
2 (𝑑 − 2)𝑇 00 + 𝑇 𝑖𝑖
,
𝑑−1
𝑐2
𝑇 0𝑖
𝜎𝑖 =
,
𝑐
𝜎𝑖𝑗 = 𝑇 𝑖𝑗 .
𝜎=

(176a)
(176b)
(176c)

As a result all the expressions of Section 5.3 acquire some explicit 𝑑-dependent coefficients. For
instance we find [61]
𝑉 = −1
ret [−4𝜋𝐺𝜎] ,

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(177a)

## PDF page 73

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

[︂
(︂
)︂
]︂
𝜎𝑘𝑘
𝑑−1
−1
^
𝑊𝑖𝑗 = ret −4𝜋𝐺 𝜎𝑖𝑗 − 𝛿𝑖𝑗
−
𝜕𝑖 𝑉 𝜕 𝑗 𝑉 .
𝑑−2
2(𝑑 − 2)

73

(177b)

Here −1
ret means the retarded integral in 𝑑 + 1 space-time dimensions, which admits, though, no
simple expression generalizing Eq. (31) in physical (𝑡, x) space.46
As reviewed in Section 6.1, the generic functions 𝐹 (x) we have to deal with in 3 dimensions,
are smooth on R3 except at 𝑦1 and 𝑦2 , around which they admit singular Laurent-type expansions
in powers and inverse powers of 𝑟1 ≡ |x − 𝑦1 | and 𝑟2 ≡ |x − 𝑦2 |, given by Eq. (178). In 𝑑 spatial
dimensions, there is an analogue of the function 𝐹 , which results from the post-Newtonian iteration
process performed in 𝑑 dimensions as we just outlined. Let us call this function 𝐹 (𝑑) (x), where
x ∈ R𝑑 . When 𝑟1 → 0 the function 𝐹 (𝑑) admits a singular expansion which is more involved than
in 3 dimensions, as it reads
∑︁ 𝑝+𝑞𝜀
𝒩
𝐹 (𝑑) (x) =
𝑟1
𝑓 (𝜀)
(178)
𝑝,𝑞 (n1 ) + 𝑜(𝑟1 ) .
1

𝑝0 ⩽𝑝⩽𝒩
𝑞0 ⩽𝑞⩽𝑞1
(𝜀)

The coefficients 𝑓1 𝑝,𝑞 (n1 ) depend on 𝜀 = 𝑑 − 3, and the powers of 𝑟1 involve the relative integers
𝑝 and 𝑞 whose values are limited by some 𝑝0 , 𝑞0 and 𝑞1 as indicated. Here we will be interested
in functions 𝐹 (𝑑) (x) which have no poles as 𝜀 → 0 (this will always be the case at 3PN order).
Therefore, we can deduce from the fact that 𝐹 (𝑑) (x) is continuous at 𝑑 = 3 the constraint
𝑞1
∑︁

𝑓 (𝜀=0)
𝑝,𝑞 (n1 ) = 𝑓 𝑝 (n1 ) .

𝑞=𝑞0 1

(179)

1

For the problem at hand, we essentially have to deal with the regularization of Poisson integrals,
or iterated Poisson integrals (and their gradients needed in the equations of motion), of the generic
function 𝐹 (𝑑) . The Poisson integral of 𝐹 (𝑑) , in 𝑑 dimensions, is given by the Green’s function for
the Laplace operator,
∫︁
[︁
]︁
d𝑑 x
𝑘˜
𝐹 (𝑑) (x) ,
𝑃 (𝑑) (x′ ) = Δ−1 𝐹 (𝑑) (x) ≡ −
4𝜋
|x − x′ |𝑑−2
where 𝑘˜ is a constant related to the usual Eulerian Γ-function by47
(︀
)︀
Γ 𝑑−2
2
˜
𝑘=
.
𝑑−2
𝜋 2

(180)

(181)

We need to evaluate the Poisson integral at the point x′ = 𝑦1 where it is singular; this is quite easy
in dimensional regularization, because the nice properties of analytic continuation allow simply to
get [𝑃 (𝑑) (x′ )]x′ =𝑦1 by replacing x′ by 𝑦1 inside the explicit integral (180). So we simply have
𝑃 (𝑑) (𝑦1 ) = −

∫︁ 𝑑
𝑘˜
d x (𝑑)
𝐹 (x) .
4𝜋
𝑟1𝑑−2

(182)

46 In higher approximations there will be also IR divergences and one should really employ the 𝑑-dimensional
version of Eq. (141).
47 We have lim
˜
˜
𝑑→3 𝑘 = 1. Notice that 𝑘 is closely linked to the volume Ω𝑑−1 of the sphere with 𝑑 − 1 dimensions
(i.e. embedded into Euclidean 𝑑-dimensional space):

˜ Ω𝑑−1 =
𝑘

4𝜋
.
𝑑−2

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 74

74

Luc Blanchet

It is not possible at present to compute the equations of motion in the general 𝑑-dimensional
case, but only in the limit where 𝜀 → 0 [163, 61]. The main technical step of our strategy consists
of computing, in the limit 𝜀 → 0, the difference between the 𝑑-dimensional Poisson potential (182),
and its Hadamard 3-dimensional counterpart given by (𝑃 )1 , where the Hadamard partie finie is
defined by Eq. (160). But we must be precise when defining the Hadamard partie finie of a Poisson
integral. Indeed, the definition (160) stricto sensu is applicable when the expansion of the function
𝐹 , for 𝑟1 → 0, does not involve logarithms of 𝑟1 ; see Eq. (160). However, the Poisson integral
𝑃 (x′ ) of 𝐹 (x) will typically involve such logarithms at the 3PN order, namely some ln 𝑟1′ where
𝑟1′ ≡ |x′ − 𝑦1 | formally tends to zero (hence ln 𝑟1′ is formally infinite). The proper way to define
the Hadamard partie finie in this case is to include the ln 𝑟1′ into its definition; we arrive at [70]
∫︁ 3
1
d x
𝐹 (x) − (𝑟12 𝐹 )1 .
(183)
(𝑃 )1 = − Pf 𝑟1′ ,𝑠2
4𝜋
𝑟1
The first term follows from Hadamard’s partie finie integral (162); the second one is given by
Eq. (160). Notice that in this result the constant 𝑠1 entering the partie finie integral (162) has
been “replaced” by 𝑟1′ , which plays the role of a new regularization constant (together with 𝑟2′
for the other particle), and which ultimately parametrizes the final Hadamard regularized 3PN
equations of motion. It was shown that 𝑟1′ and 𝑟2′ are unphysical, in the sense that they can be
removed by a coordinate transformation [69, 71]. On the other hand, the constant 𝑠2 remaining in
the result (183) is the source for the appearance of the physical ambiguity parameter 𝜆. Denoting
the difference between the dimensional and Hadamard regularizations by means of the script letter
𝒟, we pose (for what concerns the point 1)
𝒟𝑃1 ≡ 𝑃 (𝑑) (𝑦1 ) − (𝑃 )1 .

(184)

That is, 𝒟𝑃1 is what we shall have to add to the Hadamard-regularization result in order to get the
𝑑-dimensional result. However, we shall only compute the first two terms of the Laurent expansion
of 𝒟𝑃1 when 𝜀 → 0, say 𝒟𝑃1 = 𝑎−1 𝜀−1 +𝑎0 +𝒪(𝜀). This is the information we need to clear up the
ambiguity parameter. We insist that the difference 𝒟𝑃1 comes exclusively from the contribution
of terms developing some poles ∝ 1/𝜀 in the 𝑑-dimensional calculation.
Next we outline the way we obtain, starting from the computation of the “difference”, the 3PN
equations of motion in dimensional regularization, and show how the ambiguity parameter 𝜆 is
determined. By contrast to 𝑟1′ and 𝑟2′ which are pure gauge, 𝜆 is a genuine physical ambiguity,
introduced in Refs. [70, 71] as the single unknown numerical constant parametrizing the ratio
between 𝑠2 and 𝑟2′ [where 𝑠2 is the constant left in Eq. (183)] as
(︂ ′ )︂
159
𝑚1 + 𝑚2
𝑟
+𝜆
(and1 ↔ 2) ,
(185)
ln 2 =
𝑠2
308
𝑚2
where 𝑚1 and 𝑚2 are the two masses. The terms corresponding to the 𝜆-ambiguity in the acceleration 𝑎1 = 𝑑𝑣1 /𝑑𝑡 of particle 1 read simply
Δ𝑎1 [𝜆] = −

44𝜆 𝐺4N 𝑚1 𝑚22 (𝑚1 + 𝑚2 )
𝑛12 ,
5 𝑐6
3
𝑟12

(186)

where the relative distance between particles is denoted 𝑦1 − 𝑦2 ≡ 𝑟12 𝑛12 (with 𝑛12 being the unit
vector pointing from particle 2 to particle 1). We start from the end result of Ref. [71] for the 3PN
harmonic coordinates acceleration 𝑎1 in Hadamard’s regularization, abbreviated as HR. Since the
result was obtained by means of the specific extended variant of Hadamard’s regularization (in
short EHR, see Section 6.1) we write it as
(HR)

𝑎1

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(EHR)

= 𝑎1

+ Δ𝑎1 [𝜆] ,

(187)

## PDF page 75

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

75

(EHR)

where 𝑎1
is a fully determined functional of the masses 𝑚1 and 𝑚2 , the relative distance
𝑟12 𝑛12 , the coordinate velocities 𝑣1 and 𝑣2 , and also the gauge constants 𝑟1′ and 𝑟2′ . The only
ambiguous term is the second one and is given by Eq. (186).
Our strategy is to extract from both the dimensional and Hadamard regularizations their
common core part, obtained by applying the so-called “pure-Hadamard–Schwartz” (pHS) regularization. Following the definition in Ref. [61], the pHS regularization is a specific, minimal
Hadamard-type regularization of integrals, based on the partie finie integral (162), together with a
minimal treatment of “contact” terms, in which the definition (162) is applied separately to each
of the elementary potentials 𝑉 , 𝑉𝑖 , etc. (and gradients) that enter the post-Newtonian metric.
Furthermore, the regularization of a product of these potentials is assumed to be distributive, i.e.,
(𝐹 𝐺)1 = (𝐹 )1 (𝐺)1 in the case where 𝐹 and 𝐺 are given by such elementary potentials; this is thus
in contrast with Eq. (161). The pHS regularization also assumes the use of standard Schwartz
distributional derivatives [381]. The interest of the pHS regularization is that the dimensional
regularization is equal to it plus the “difference”; see Eq. (190).
To obtain the pHS-regularized acceleration we need to substract from the EHR result a series
of contributions, which are specific consequences of the use of EHR [70, 72]. For instance, one
of these contributions corresponds to the fact that in the EHR the distributional derivative is
given by Eqs. (167) – (168) which differs from the Schwartz distributional derivative in the pHS
regularization. Hence we define
∑︁
(pHS)
(EHR)
𝑎1
= 𝑎1
−
𝛿𝑎1 ,
(188)
where the 𝛿𝑎1 ’s denote the extra terms following from the EHR prescriptions. The pHS-regularized
acceleration (188) constitutes essentially the result of the first stage of the calculation of 𝑎1 , as
reported in Ref. [193].
The next step consists of evaluating the Laurent expansion, in powers of 𝜀 = 𝑑 − 3, of the
difference between the dimensional regularization and the pHS (3-dimensional) computation. As
we reviewed above, this difference makes a contribution only when a term generates a pole ∼ 1/𝜀,
in which case the dimensional regularization adds an extra contribution, made of the pole and the
finite part associated with the pole [we consistently neglect all terms 𝒪(𝜀)]. One must then be
especially wary of combinations of terms whose pole parts finally cancel but whose dimensionally
regularized finite parts generally do not, and must be evaluated with care. We denote the above
defined difference by
∑︁
𝒟𝑎1 =
𝒟𝑃1 .
(189)
It is made of the sum of all the individual differences of Poisson or Poisson-like integrals as computed
in Eq. (184). The total difference (189) depends on the Hadamard regularization scales 𝑟1′ and 𝑠2
(or equivalently on 𝜆 and 𝑟1′ , 𝑟2′ ), and on the parameters associated with dimensional regularization,
namely 𝜀 and the characteristic length scale ℓ0 introduced in Eq. (174). Finally, the result is the
explicit computation of the 𝜀-expansion of the dimensional regularization (DR) acceleration as
(DR)

𝑎1

(pHS)

= 𝑎1

+ 𝒟𝑎1 .

(190)

With this result we can prove two theorems [61].
Theorem 8. The pole part ∝ 1/𝜀 of the DR acceleration (190) can be re-absorbed (i.e. renormalized) into some shifts of the two “bare” world-lines: 𝑦1 → 𝑦1 + 𝜉1 and 𝑦2 → 𝑦2 + 𝜉2 , with
𝜉1,2 ∝ 1/𝜀 say, so that the result, expressed in terms of the “dressed” quantities, is finite when
𝜀 → 0.
The situation in harmonic coordinates is to be contrasted with the calculation in ADM-type coordinates within the Hamiltonian formalism, where it was shown that all pole parts directly cancel

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 76

76

Luc Blanchet

out in the total 3PN Hamiltonian: No renormalization of the world-lines is needed [163]. The
central result is then:
Theorem 9. The renormalized (finite) DR acceleration is physically equivalent to the Hadamardregularized (HR) acceleration (end result of Ref. [71]), in the sense that
[︁
]︁
(HR)
(DR)
𝑎1
= lim 𝑎1
+ 𝛿𝜉 𝑎1 ,
(191)
𝜀→0

where 𝛿𝜉 𝑎1 denotes the effect of the shifts on the acceleration, if and only if the HR ambiguity
parameter 𝜆 entering the harmonic-coordinates equations of motion takes the unique value (172).
The precise shifts 𝜉1 and 𝜉2 needed in Theorem 9 involve not only a pole contribution ∝ 1/𝜀, but
also a finite contribution when 𝜀 → 0. Their explicit expressions read:48
[︃
)︃
]︃
(︃
327
11 𝐺2N 𝑚21 1
𝑟1′ 𝑞 1/2
−
𝑎N
(together with 1 ↔ 2) ,
(192)
− 2 ln
𝜉1 =
1
3
𝑐6
𝜀
ℓ0
1540
where 𝐺N is Newton’s constant, ℓ0 is the characteristic length scale of dimensional regularization,
cf. Eq. (174), where 𝑎N
1 is the Newtonian acceleration of the particle 1 in 𝑑 dimensions, and
𝑞 ≡ 4𝜋𝑒𝛾E depends on Euler’s constant 𝛾E ≃ 0.577.

6.4

Dimensional regularization of the radiation field

We now address the similar problem concerning the binary’s radiation field – to 3PN order beyond
Einstein’s quadrupole formalism (2) – (3). As reviewed in Section 6.2, three ambiguity parameters:
𝜉, 𝜅 and 𝜁, have been shown to appear in the 3PN expression of the quadrupole moment [81, 80].
To apply dimensional regularization, we must use as in Section 6.3 the 𝑑-dimensional postNewtonian iteration leading to potentials such as those in Eqs. (177); and we have to generalize to
𝑑 dimensions some key results of the wave generation formalism of Part A. Essentially, we need the
𝑑-dimensional analogues of the multipole moments of an isolated source I𝐿 and J𝐿 in Eqs. (123).
Here we report the result we find in the case of the mass-type moment:
{︂
∫︁
𝑑−1
4(𝑑 + 2ℓ − 2)
(𝑑)
I𝐿 (𝑡) =
ℱ𝒫 d𝑑 x 𝑥
^𝐿 Σ (x, 𝑡) − 2
𝑥
^𝑎𝐿 Σ (1)
𝑎 (x, 𝑡)
2(𝑑 − 2)
𝑐 (𝑑 + ℓ − 2)(𝑑 + 2ℓ)
[ℓ]
[ℓ+1]
}︂
2(𝑑 + 2ℓ − 2)
(2)
+ 4
𝑥
^𝑎𝑏𝐿 Σ 𝑎𝑏 (x, 𝑡) ,
(193)
𝑐 (𝑑 + ℓ − 1)(𝑑 + ℓ − 2)(𝑑 + 2ℓ + 2)
[ℓ+2]
in which we denote, generalizing Eqs. (124),
2 (𝑑 − 2)𝜏 00 + 𝜏 𝑖𝑖
,
𝑑−1
𝑐2
𝜏 0𝑖
,
Σ𝑖 =
𝑐
Σ𝑖𝑗 = 𝜏 𝑖𝑗 ,
Σ=

and where for any source densities the underscript [ℓ] means the infinite series
(︀
)︀ (︂
)︂2𝑘
+∞
∑︁
Γ 𝑑2 + ℓ
1
𝑟 𝜕
(︀
)︀
(x,
𝑡)
=
Σ(x, 𝑡) .
Σ
22𝑘 𝑘! Γ 𝑑2 + ℓ + 𝑘
𝑐 𝜕𝑡
[ℓ]

(194a)
(194b)
(194c)

(195)

𝑘=0

48 When working at the level of the equations of motion (not considering the metric outside the world-lines), the
effect of shifts can be seen as being induced by a coordinate transformation of the bulk metric as in Ref. [71].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 77

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

77

The latter definition represents the 𝑑-dimensional version of the post-Newtonian expansion se(𝑑)
order, the expression (193) reduces to the standard result I𝐿 =
∫︀ries𝑑 (126). At Newtonian
2
00 2
d x𝜌𝑥
^𝐿 + 𝒪(1/𝑐 ) with 𝜌 = 𝑇 /𝑐 denoting the usual Newtonian density.
The ambiguity parameters 𝜉, 𝜅 and 𝜁 come from the Hadamard regularization of the mass
quadrupole moment I𝑖𝑗 at the 3PN order. The terms corresponding to these ambiguities were
found to be
[︂(︂
)︂
]︂
44 𝐺2N 𝑚31
𝑚1 + 𝑚2
⟨𝑖 𝑗⟩
⟨𝑖 𝑗⟩
ΔI𝑖𝑗 [𝜉, 𝜅, 𝜁] =
𝜉
+
𝜅
𝑦
𝑎
+
𝜁
𝑣
𝑣
+ 1 ↔ 2,
(196)
1 1
1 1
3
𝑐6
𝑚1
where 𝑦1 , 𝑣1 and 𝑎1 denote the first particle’s position, velocity and acceleration (and the brackets
⟨ ⟩ surrounding indices refer to the STF projection). Like in Section 6.3, we express both the
Hadamard and dimensional results in terms of the more basic pHS regularization. The first step
(HR)
of the calculation [80] is therefore to relate the Hadamard-regularized quadrupole moment I𝑖𝑗 ,
for general orbits, to its pHS part:
]︂
[︂
9
1
(HR)
(pHS)
.
(197)
I𝑖𝑗
= I𝑖𝑗
+ ΔI𝑖𝑗 𝜉 + , 𝜅, 𝜁 +
22
110
In the right-hand side we find both the pHS part, and the effect of adding the ambiguities, with
some numerical shifts of the ambiguity parameters (𝜉 → 𝜉 + 1/22, 𝜁 → 𝜁 + 9/110) due to the
difference between the specific Hadamard-type regularization scheme used in Ref. [81] and the
pHS one. The pHS part is free of ambiguities but depends on the gauge constants 𝑟1′ and 𝑟2′
introduced in the harmonic-coordinates equations of motion [69, 71].
We next use the 𝑑-dimensional moment (193) to compute the difference between the dimensional
regularization (DR) result and the pHS one [62, 63]. As in the work on equations of motion, we find
that the ambiguities arise solely from the terms in the integration regions near the particles, that
give rise to poles ∝ 1/𝜀, corresponding to logarithmic ultra-violet (UV) divergences in 3 dimensions.
The infra-red (IR) region at infinity, i.e., |x| → +∞, does not contribute to the difference between
DR and pHS. The compact-support terms in the integrand of Eq. (193), proportional to the matter
source densities 𝜎, 𝜎𝑎 , and 𝜎𝑎𝑏 , are also found not to contribute to the difference. We are therefore
left with evaluating the difference linked with the computation of the non-compact terms in the
expansion of the integrand of (193) near the singularities that produce poles in 𝑑 dimensions.
Let 𝐹 (𝑑) (x) be the non-compact part of the integrand of the quadrupole moment (193) (with
indices 𝐿 = 𝑖𝑗), where 𝐹 (𝑑) includes the appropriate multipolar factors such as 𝑥
^𝑖𝑗 , so that
∫︁
(𝑑)
I𝑖𝑗 = d𝑑 x 𝐹 (𝑑) (x) .
(198)
We do not indicate that we are considering here only the non-compact part of the moments. Near
the singularities the function 𝐹 (𝑑) (x) admits a singular expansion of the type (178). In practice,
(𝜀)
the various coefficients 1 𝑓𝑝,𝑞 are computed by specializing the general expressions of the non-linear
^ 𝑎𝑏 , etc. (valid for general extended sources) to point particles in 𝑑
retarded potentials 𝑉 , 𝑉𝑎 , 𝑊
dimensions. On the other hand, the analogue of Eq. (198) in 3 dimensions is
∫︁
I𝑖𝑗 = Pf d3 x 𝐹 (x) ,
(199)
where Pf refers to the Hadamard partie finie defined in Eq. (162). The difference 𝒟I𝑖𝑗 between
the DR evaluation of the 𝑑-dimensional integral (198) and its corresponding three-dimensional
evaluation (199), reads then
(𝑑)
𝒟I𝑖𝑗 = I𝑖𝑗 − I𝑖𝑗 .
(200)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 78

78

Luc Blanchet

Such difference depends only on the UV behaviour of the integrands, and can therefore be computed
“locally”, i.e., in the vicinity of the particles, when 𝑟1 → 0 and 𝑟2 → 0. We find that Eq. (200)
depends on two constant scales 𝑠1 and 𝑠2 coming from Hadamard’s partie finie (162), and on the
constants belonging to dimensional regularization, i.e., 𝜀 = 𝑑 − 3 and ℓ0 defined by Eq. (174). The
dimensional regularization of the 3PN quadrupole moment is then obtained as the sum of the pHS
part, and of the difference computed according to Eq. (200), namely
(DR)

I𝑖𝑗

(pHS)

= I𝑖𝑗

+ 𝒟I𝑖𝑗 .

(201)

An important fact, hidden in our too-compact notation (201), is that the sum of the two terms in
the right-hand side of Eq. (201) does not depend on the Hadamard regularization scales 𝑠1 and
𝑠2 . Therefore it is possible without changing the sum to re-express these two terms (separately)
by means of the constants 𝑟1′ and 𝑟2′ instead of 𝑠1 and 𝑠2 , where 𝑟1′ , 𝑟2′ are the two fiducial scales
entering the Hadamard-regularization result (197). This replacement being made the pHS term in
Eq. (201) is exactly the same as the one in Eq. (197). At this stage all elements are in place to
prove the following theorem [62, 63].
Theorem 10. The DR quadrupole moment (201) is physically equivalent to the Hadamard-regularized
one (end result of Refs. [81, 80]), in the sense that
[︁
]︁
(DR)
(HR)
(202)
I𝑖𝑗
= lim I𝑖𝑗 + 𝛿𝜉 I𝑖𝑗 ,
𝜀→0

where 𝛿𝜉 I𝑖𝑗 denotes the effect of the same shifts as determined in Theorems 8 and 9, if and only if
the HR ambiguity parameters 𝜉, 𝜅 and 𝜁 take the unique values reported in Eqs. (173). Moreover,
the poles 1/𝜀 separately present in the two terms in the brackets of Eq. (202) cancel out, so that the
physical (“dressed”) DR quadrupole moment is finite and given by the limit when 𝜀 → 0 as shown
in Eq. (202).
This theorem finally provides an unambiguous determination of the 3PN radiation field by dimensional regularization. Furthermore, as reviewed in Section 6.2, several checks of this calculation
could be done, which provide independent confirmations for the ambiguity parameters. Such checks
also show the powerfulness of dimensional regularization and its validity for describing the classical
general-relativistic dynamics of compact bodies.

7

Newtonian-like Equations of Motion

7.1

The 3PN acceleration and energy for particles

We present the acceleration of one of the particles, say the particle 1, at the 3PN order, as well
as the 3PN energy of the binary, which is conserved in the absence of radiation reaction. To get
this result we used essentially a “direct” post-Newtonian method (issued from Ref. [76]), which
consists of reducing the 3PN metric of an extended regular source, worked out in Eqs. (144), to the
case where the matter tensor is made of delta functions, and then curing the self-field divergences
by means of the Hadamard regularization technique. The equations of motion are simply the 3PN
geodesic equations explicitly provided in Eqs. (150) – (152); the metric therein is the regularized
metric generated by the system of particles itself. Hadamard’s regularization permits to compute
all the terms but one, and the Hadamard ambiguity parameter 𝜆 is obtained from dimensional
regularization; see Section 6.3. We also add the 3.5PN terms in harmonic coordinates which are
known from Refs. [258, 259, 260, 336, 278, 322, 254]. These correspond to radiation reaction effects
at relative 1PN order (see Section 5.4 for discussion on radiation reaction up to 1.5PN order).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 79

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

79

Though the successive post-Newtonian approximations are really a consequence of general
relativity, the final equations of motion must be interpreted in a Newtonian-like fashion. That is,
once a convenient general-relativistic (Cartesian) coordinate system is chosen, we should express
the results in terms of the coordinate positions, velocities, and accelerations of the bodies, and
view the trajectories of the particles as taking place in the absolute Euclidean space of Newton.
But because the equations of motion are actually relativistic, they must:
1. Stay manifestly invariant – at least in harmonic coordinates – when we perform a global
post-Newtonian-expanded Lorentz transformation;
2. Possess the correct “perturbative” limit, given by the geodesics of the (post-Newtonianexpanded) Schwarzschild metric, when one of the masses tends to zero;
3. Be conservative, i.e., to admit a Lagrangian or Hamiltonian formulation, when the gravitational radiation reaction is turned off.
We denote by 𝑟12 = |𝑦1 (𝑡) − 𝑦2 (𝑡)| the harmonic-coordinate distance between the two particles,
with 𝑦1 = (𝑦1𝑖 ) and 𝑦2 = (𝑦2𝑖 ), by 𝑛12 = (𝑦1 − 𝑦2 )/𝑟12 the corresponding unit direction, and by
𝑣1 = d𝑦1 /d𝑡 and 𝑎1 = d𝑣1 /d𝑡 the coordinate velocity and acceleration of the particle 1 (and idem
for 2). Sometimes we pose 𝑣12 = 𝑣1 − 𝑣2 for the relative velocity. The usual Euclidean scalar
product of vectors is denoted with parentheses, e.g., (𝑛12 𝑣1 ) = 𝑛12 · 𝑣1 and (𝑣1 𝑣2 ) = 𝑣1 · 𝑣2 . The
equations of the body 2 are obtained by exchanging all the particle labels 1 ↔ 2 (remembering
that 𝑛12 and 𝑣12 change sign in this operation):
𝐺𝑚2
2 𝑛12
𝑟12
{︃ [︂
(︂
)︂]︂
5𝐺2 𝑚1 𝑚2
4𝐺2 𝑚22
𝐺𝑚2 3
1
2
2
2
+
+ 2
(𝑛12 𝑣2 ) − 𝑣1 + 4(𝑣1 𝑣2 ) − 2𝑣2
𝑛12
+ 2
3
3
𝑐
𝑟12
𝑟12
𝑟12
2
}︃
𝐺𝑚2
+ 2 (4(𝑛12 𝑣1 ) − 3(𝑛12 𝑣2 )) 𝑣12
𝑟12
{︃[︂
1
57𝐺3 𝑚21 𝑚2
69𝐺3 𝑚1 𝑚22
9𝐺3 𝑚32
+ 4
−
−
−
4
4
4
𝑐
4𝑟12
2𝑟12
𝑟12
(︂
3
9
𝐺𝑚2
15
+ 2
− (𝑛12 𝑣2 )4 + (𝑛12 𝑣2 )2 𝑣12 − 6(𝑛12 𝑣2 )2 (𝑣1 𝑣2 ) − 2(𝑣1 𝑣2 )2 + (𝑛12 𝑣2 )2 𝑣22
𝑟12
8
2
2
)︂
+ 4(𝑣1 𝑣2 )𝑣22 − 2𝑣24
(︂
)︂
𝐺2 𝑚1 𝑚2 39
17
15 2 5
5 2
2
2
+
(𝑛12 𝑣1 ) − 39(𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 ) − 𝑣1 − (𝑣1 𝑣2 ) + 𝑣2
3
𝑟12
2
2
4
2
4
]︂
2 2 (︀
)︀
𝐺 𝑚
+ 3 2 2(𝑛12 𝑣1 )2 − 4(𝑛12 𝑣1 )(𝑛12 𝑣2 ) − 6(𝑛12 𝑣2 )2 − 8(𝑣1 𝑣2 ) + 4𝑣22 𝑛12
𝑟12
[︂ 2 2
(︂
)︂
𝐺 𝑚2
𝐺2 𝑚1 𝑚2
63
55
+
(−2(𝑛12 𝑣1 ) − 2(𝑛12 𝑣2 )) +
− (𝑛12 𝑣1 ) + (𝑛12 𝑣2 )
3
3
𝑟12
𝑟12
4
4
(︂
𝐺𝑚2
9
+ 2
− 6(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 + (𝑛12 𝑣2 )3 + (𝑛12 𝑣2 )𝑣12 − 4(𝑛12 𝑣1 )(𝑣1 𝑣2 )
𝑟12
2
)︂]︂ }︃

𝑎1 = −

+ 4(𝑛12 𝑣2 )(𝑣1 𝑣2 ) + 4(𝑛12 𝑣1 )𝑣22 − 5(𝑛12 𝑣2 )𝑣22

𝑣12

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 80

80

Luc Blanchet

{︃ [︂

]︂
208𝐺3 𝑚1 𝑚22
24𝐺3 𝑚21 𝑚2
12𝐺2 𝑚1 𝑚2
2
(𝑛
𝑣
)
−
(𝑛
𝑣
)
+
(𝑛
𝑣
)𝑣
12 12
12 12
12 12 12 𝑛12
4
4
3
15𝑟12
5𝑟12
5𝑟12
}︃
]︂
[︂ 3 2
32 𝐺3 𝑚1 𝑚22
4𝐺2 𝑚1 𝑚2 2
8𝐺 𝑚1 𝑚2
−
−
𝑣12 𝑣12
+
4
4
3
5𝑟12
5𝑟12
5𝑟12
{︃[︂
(︂
1
𝐺𝑚2 35
15
15
+ 6
(𝑛12 𝑣2 )6 − (𝑛12 𝑣2 )4 𝑣12 + (𝑛12 𝑣2 )4 (𝑣1 𝑣2 ) + 3(𝑛12 𝑣2 )2 (𝑣1 𝑣2 )2
2
𝑐
𝑟12
16
8
2
1
+ 5
𝑐

15
3
(𝑛12 𝑣2 )4 𝑣22 + (𝑛12 𝑣2 )2 𝑣12 𝑣22 − 12(𝑛12 𝑣2 )2 (𝑣1 𝑣2 )𝑣22 − 2(𝑣1 𝑣2 )2 𝑣22
2
2
)︂
15
+ (𝑛12 𝑣2 )2 𝑣24 + 4(𝑣1 𝑣2 )𝑣24 − 2𝑣26
2
(︂
171
𝐺2 𝑚1 𝑚2
171
723
−
+
(𝑛12 𝑣1 )4 +
(𝑛12 𝑣1 )3 (𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2
3
𝑟12
8
2
4
383
455
229
+
(𝑛12 𝑣1 )(𝑛12 𝑣2 )3 −
(𝑛12 𝑣2 )4 +
(𝑛12 𝑣1 )2 𝑣12
2
8
4
205
191
91
229
−
(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12 +
(𝑛12 𝑣2 )2 𝑣12 − 𝑣14 −
(𝑛12 𝑣1 )2 (𝑣1 𝑣2 )
2
4
8
2
225
91
+ 244(𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 ) −
(𝑛12 𝑣2 )2 (𝑣1 𝑣2 ) + 𝑣12 (𝑣1 𝑣2 )
2
2
177
229
283
2
2 2
−
(𝑣1 𝑣2 ) +
(𝑛12 𝑣1 ) 𝑣2 −
(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣22
4
4
2
)︂
91
81
259
(𝑛12 𝑣2 )2 𝑣22 − 𝑣12 𝑣22 + 43(𝑣1 𝑣2 )𝑣22 − 𝑣24
+
4
4
8
(︂
𝐺2 𝑚22
+ 3
− 6(𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 + 12(𝑛12 𝑣1 )(𝑛12 𝑣2 )3 + 6(𝑛12 𝑣2 )4
𝑟12
−

+ 4(𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 ) + 12(𝑛12 𝑣2 )2 (𝑣1 𝑣2 ) + 4(𝑣1 𝑣2 )2
)︂
− 4(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣22 − 12(𝑛12 𝑣2 )2 𝑣22 − 8(𝑣1 𝑣2 )𝑣22 + 4𝑣24
(︂
)︂
𝐺3 𝑚3
43
+ 4 2 −(𝑛12 𝑣1 )2 + 2(𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 )2 + 18(𝑣1 𝑣2 ) − 9𝑣22
𝑟12
2
(︂
3
2
375
1113
615
𝐺 𝑚1 𝑚2 415
+
(𝑛12 𝑣1 )2 −
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) +
(𝑛12 𝑣2 )2 −
(𝑛12 𝑣12 )2 𝜋 2
4
𝑟12
8
4
8
64
)︂
123 2 2
33
+ 18𝑣12 +
𝜋 𝑣12 + 33(𝑣1 𝑣2 ) − 𝑣22
64
2
(︂
3 2
𝐺 𝑚1 𝑚2
45887
24025
10469
48197 2
+
−
(𝑛12 𝑣1 )2 +
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) −
(𝑛12 𝑣2 )2 +
𝑣
4
𝑟12
168
42
42
840 1
)︂
(︂
)︂ )︂
(︂
𝑟12
36227
36227 2
𝑟12
2
−
22𝑣
ln
−
(𝑣1 𝑣2 ) +
𝑣2 + 110(𝑛12 𝑣12 )2 ln
12
420
840
𝑟1′
𝑟1′
(︂
)︂
(︂
(︂
)︂)︂
16𝐺4 𝑚42
𝐺4 𝑚21 𝑚22
41
𝐺4 𝑚31 𝑚2
3187 44
𝑟12
+
175 − 𝜋 2 +
−
+
ln
+
5
5
5
𝑟12
𝑟12
16
𝑟12
1260
3
𝑟1′
(︂
(︂
)︂)︂
]︂
𝑟12
𝐺4 𝑚1 𝑚32 110741 41 2 44
+
− 𝜋 −
ln
𝑛12
5
𝑟12
630
16
3
𝑟2′
[︂
(︂
𝐺𝑚2 15
45
3
+
(𝑛12 𝑣1 )(𝑛12 𝑣2 )4 − (𝑛12 𝑣2 )5 − (𝑛12 𝑣2 )3 𝑣12 + 6(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 (𝑣1 𝑣2 )
2
𝑟12
2
8
2

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 81

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

81

− 6(𝑛12 𝑣2 )3 (𝑣1 𝑣2 ) − 2(𝑛12 𝑣2 )(𝑣1 𝑣2 )2 − 12(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 𝑣22 + 12(𝑛12 𝑣2 )3 𝑣22
+ (𝑛12 𝑣2 )𝑣12 𝑣22 − 4(𝑛12 𝑣1 )(𝑣1 𝑣2 )𝑣22 + 8(𝑛12 𝑣2 )(𝑣1 𝑣2 )𝑣22 + 4(𝑛12 𝑣1 )𝑣24
)︂
− 7(𝑛12 𝑣2 )𝑣24
(︂
𝐺2 𝑚2
+ 3 2 − 2(𝑛12 𝑣1 )2 (𝑛12 𝑣2 ) + 8(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 + 2(𝑛12 𝑣2 )3 + 2(𝑛12 𝑣1 )(𝑣1 𝑣2 )
𝑟12
)︂
+ 4(𝑛12 𝑣2 )(𝑣1 𝑣2 ) − 2(𝑛12 𝑣1 )𝑣22 − 4(𝑛12 𝑣2 )𝑣22
(︂
243
565
269
𝐺2 𝑚1 𝑚2
−
(𝑛12 𝑣1 )3 +
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )(𝑛12 𝑣2 )2
+
3
𝑟12
4
4
4
95
207
137
− (𝑛12 𝑣2 )3 +
(𝑛12 𝑣1 )𝑣12 −
(𝑛12 𝑣2 )𝑣12 − 36(𝑛12 𝑣1 )(𝑣1 𝑣2 )
12
8
8
)︂
27
81
83
+ (𝑛12 𝑣2 )(𝑣1 𝑣2 ) + (𝑛12 𝑣1 )𝑣22 + (𝑛12 𝑣2 )𝑣22
4
8
8
3 3
𝐺 𝑚
+ 4 2 (4(𝑛12 𝑣1 ) + 5(𝑛12 𝑣2 ))
𝑟12
)︂
(︂
479
123
𝐺3 𝑚1 𝑚22
307
2
(𝑛
𝑣
)
+
(𝑛
𝑣
)
+
(𝑛
𝑣
)𝜋
+
−
12 1
12 2
12 12
4
𝑟12
8
8
32
(︂
(︂
)︂)︂ ]︂ }︃
𝐺3 𝑚21 𝑚2 31397
36227
𝑟12
+
(𝑛12 𝑣1 ) −
(𝑛12 𝑣2 ) − 44(𝑛12 𝑣12 ) ln
𝑣12
4
𝑟12
420
420
𝑟1′
{︃[︂
(︂
)︂
𝐺4 𝑚31 𝑚2 3992
4328
1
(𝑛12 𝑣1 ) −
(𝑛12 𝑣2 )
+ 7
5
𝑐
𝑟12
105
105
)︂
(︂
𝐺4 𝑚21 𝑚22
2872
3172 𝐺4 𝑚1 𝑚32
13576
+
(𝑛
𝑣
)
+
(𝑛
𝑣
)
−
(𝑛12 𝑣12 )
−
12 1
12 2
6
6
𝑟12
105
21
21
𝑟12
(︂
𝐺3 𝑚21 𝑚2
744
288
696
+
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 ) +
(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 −
(𝑛12 𝑣2 )3
48(𝑛12 𝑣1 )3 −
4
𝑟12
5
5
5
4888
5056
2056
−
(𝑛12 𝑣1 )𝑣12 +
(𝑛12 𝑣2 )𝑣12 +
(𝑛12 𝑣1 )(𝑣1 𝑣2 )
105
105
21
)︂
1028
5812
2224
(𝑛12 𝑣2 )(𝑣1 𝑣2 ) −
(𝑛12 𝑣1 )𝑣22 +
(𝑛12 𝑣2 )𝑣22
−
21
21
105
(︂
3
2
𝐺 𝑚1 𝑚2
582
1746
1954
+
−
(𝑛12 𝑣1 )3 +
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )(𝑛12 𝑣2 )2
4
𝑟12
5
5
5
3568
2864
+ 158(𝑛12 𝑣2 )3 +
(𝑛12 𝑣12 )𝑣12 −
(𝑛12 𝑣1 )(𝑣1 𝑣2 )
105
35
)︂
10048
1432
5752
+
(𝑛12 𝑣2 )(𝑣1 𝑣2 ) +
(𝑛12 𝑣1 )𝑣22 −
(𝑛12 𝑣2 )𝑣22
105
35
105
(︂
2
𝐺 𝑚1 𝑚2
2
2
− 56(𝑛12 𝑣12 )5 + 60(𝑛12 𝑣1 )3 𝑣12
− 180(𝑛12 𝑣1 )2 (𝑛12 𝑣2 )𝑣12
+
3
𝑟12
246
2
2
+ 174(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 𝑣12
− 54(𝑛12 𝑣2 )3 𝑣12
−
(𝑛12 𝑣12 )𝑣14
35
1068
984
1068
+
(𝑛12 𝑣1 )𝑣12 (𝑣1 𝑣2 ) −
(𝑛12 𝑣2 )𝑣12 (𝑣1 𝑣2 ) −
(𝑛12 𝑣1 )(𝑣1 𝑣2 )2
35
35
35

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 82

82

Luc Blanchet

180
534
90
(𝑛12 𝑣2 )(𝑣1 𝑣2 )2 −
(𝑛12 𝑣1 )𝑣12 𝑣22 + (𝑛12 𝑣2 )𝑣12 𝑣22
7
35
7
984
732
204
2
+
(𝑛12 𝑣1 )(𝑣1 𝑣2 )𝑣2 −
(𝑛12 𝑣2 )(𝑣1 𝑣2 )𝑣22 −
(𝑛12 𝑣1 )𝑣24
35
35
35
)︂]︂
24
4
+ (𝑛12 𝑣2 )𝑣2 𝑛12
7
[︂
4 3
6224 𝐺4 𝑚21 𝑚22
6388 𝐺4 𝑚1 𝑚32
184 𝐺 𝑚1 𝑚2
+
+
+ −
5
6
6
21
𝑟12
105
𝑟12
105
𝑟12
(︂
3 2
𝐺 𝑚1 𝑚2 52
56
44
132 2 152
+
(𝑛12 𝑣1 )2 − (𝑛12 𝑣1 )(𝑛12 𝑣2 ) − (𝑛12 𝑣2 )2 −
𝑣 +
(𝑣1 𝑣2 )
4
𝑟12
15
15
15
35 1
35
)︂
48
− 𝑣22
35
(︂
𝐺3 𝑚1 𝑚22 454
372
854
152 2
+
(𝑛12 𝑣1 )2 −
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) +
(𝑛12 𝑣2 )2 −
𝑣
4
𝑟12
15
5
15
21 1
)︂
1768 2
2864
(𝑣1 𝑣2 ) −
𝑣
+
105
105 2
(︂
𝐺2 𝑚1 𝑚2
348
684
2
2
+
60(𝑛12 𝑣12 )4 −
(𝑛12 𝑣1 )2 𝑣12
+
(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12
3
𝑟12
5
5
334 4 1336 2
1308
654 2 2
2
− 66(𝑛12 𝑣2 )2 𝑣12
+
𝑣 −
𝑣 (𝑣1 𝑣2 ) +
(𝑣1 𝑣2 )2 +
𝑣 𝑣
35 1
35}︃ 1
35
35 1 2
)︂]︂
(︂ )︂
1
1252
292 4
−
(𝑣1 𝑣2 )𝑣22 +
𝑣
𝑣12 + 𝒪 8 .
(203)
35
35 2
𝑐
+

The 2.5PN and 3.5PN terms are associated with gravitational radiation reaction.49 The 3PN
harmonic-coordinates equations of motion depend on two arbitrary length scales 𝑟1′ and 𝑟2′ associated with the logarithms present at the 3PN order. It has been proved in Ref. [71] that 𝑟1′ and 𝑟2′
are merely linked with the choice of coordinates – we can refer to 𝑟1′ and 𝑟2′ as “gauge constants”.
In our approach [69, 71], the harmonic coordinate system is not uniquely fixed by the coordinate
condition 𝜕𝜇 ℎ𝛼𝜇 = 0. In fact there are infinitely many “locally-defined” harmonic coordinate systems. For general smooth matter sources, as in the general formalism of Part A, we expect the
existence and uniqueness of a global harmonic coordinate system. But here we have some pointparticles, with delta-function singularities, and in this case we do not have the notion of a global
coordinate system. We can always change the harmonic coordinates by means of the gauge vector
𝜂 𝛼 = 𝛿𝑥𝛼 , satisfying Δ𝜂 𝛼 = 0 except at the location of the two particles (we assume that the
transformation is at the 3PN level, so we can consider simply a flat-space Laplace equation). More
precisely, we can show that the logarithms appearing in Eq. (203), together with the constants 𝑟1′
and 𝑟2′ therein, can be removed by the coordinate transformation associated with the 3PN gauge
vector (with 𝑟1 = |x − 𝑦1 (𝑡)| and 𝑟2 = |x − 𝑦2 (𝑡)|; and 𝜕 𝛼 = 𝜂 𝛼𝜇 𝜕𝜇 ):
[︂
(︂
)︂
(︂
)︂]︂
𝑟12
𝐺𝑚2
𝑟12
22 𝐺2 𝑚1 𝑚2 𝛼 𝐺𝑚1
𝜂 =−
𝜕
ln
+
ln
.
3
𝑐6
𝑟2
𝑟1′
𝑟1
𝑟2′
𝛼

(204)

Therefore, the arbitrariness in the choice of the constants 𝑟1′ and 𝑟2′ is innocuous on the physical
49 Notice the dependence upon the irrational number 𝜋 2 . Technically, the 𝜋 2 terms arise from non-linear interactions involving some integrals such as
∫︁
1
d3 x
𝜋2
=
.
2
2
𝜋
𝑟1 𝑟2
𝑟12

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 83

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

83

point of view, because the physical results must be gauge invariant. Indeed we shall verify that 𝑟1′
and 𝑟2′ cancel out in our final results.
When retaining the “even” relativistic corrections at the 1PN, 2PN and 3PN orders, and
neglecting the “odd” radiation reaction terms at the 2.5PN and 3.5PN orders, we find that the
equations of motion admit a conserved energy (and a Lagrangian, as we shall see); that energy can
be straightforwardly obtained by guess-work starting from Eq. (203), with the result
𝑚1 𝑣12
𝐺𝑚1 𝑚2
−
2
2𝑟12
{︂
(︂
)︂}︂
3𝑚1 𝑣14
𝐺𝑚1 𝑚2
1
3 2 7
1 𝐺2 𝑚21 𝑚2
+
+
− (𝑛12 𝑣1 )(𝑛12 𝑣2 ) + 𝑣1 − (𝑣1 𝑣2 )
+ 2
2
𝑐
2𝑟12
8
𝑟12
4
2
4
{︃
3 3
3 2 2
6
1
𝐺 𝑚1 𝑚2
19𝐺 𝑚1 𝑚2
5𝑚1 𝑣1
+ 4 −
−
+
3
3
𝑐
2𝑟12
8𝑟12
16
(︂
𝐺𝑚1 𝑚2 3
3
9
(𝑛12 𝑣1 )3 (𝑛12 𝑣2 ) + (𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 − (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12
+
𝑟12
8
16
8
21
13
3
13
− (𝑛12 𝑣2 )2 𝑣12 + 𝑣14 + (𝑛12 𝑣1 )2 (𝑣1 𝑣2 ) + (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )
8
8
8
4
)︂
55 2
17
31 2 2
2
− 𝑣1 (𝑣1 𝑣2 ) + (𝑣1 𝑣2 ) + 𝑣1 𝑣2
8
8
16
(︂
)︂ }︃
2 2
13
1
3 2 7 2
𝐺 𝑚1 𝑚2 29
2
2
(𝑛12 𝑣1 ) − (𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 ) − 𝑣1 + 𝑣2
+
2
𝑟12
4
4
2
2
4
{︃
1 35𝑚1 𝑣18
+ 6
𝑐
128
(︂
5
5
𝐺𝑚1 𝑚2
5
+
− (𝑛12 𝑣1 )5 (𝑛12 𝑣2 ) − (𝑛12 𝑣1 )4 (𝑛12 𝑣2 )2 − (𝑛12 𝑣1 )3 (𝑛12 𝑣2 )3
𝑟12
16
16
32
15
3
19
+ (𝑛12 𝑣1 )3 (𝑛12 𝑣2 )𝑣12 + (𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 𝑣12 + (𝑛12 𝑣1 )(𝑛12 𝑣2 )3 𝑣12
16
16
4
19
21
4 2
4
2 4
+ (𝑛12 𝑣2 ) 𝑣1 − (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣1 − 2(𝑛12 𝑣2 ) 𝑣1
16
16
55 6 19
+ 𝑣1 − (𝑛12 𝑣1 )4 (𝑣1 𝑣2 ) − (𝑛12 𝑣1 )3 (𝑛12 𝑣2 )(𝑣1 𝑣2 )
16
16
15
45
− (𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 (𝑣1 𝑣2 ) + (𝑛12 𝑣1 )2 𝑣12 (𝑣1 𝑣2 )
32
16
5
11
139 4
2
+ (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣1 (𝑣1 𝑣2 ) + (𝑛12 𝑣2 )2 𝑣12 (𝑣1 𝑣2 ) −
𝑣 (𝑣1 𝑣2 )
4
4
16 1
3
5
41
1
− (𝑛12 𝑣1 )2 (𝑣1 𝑣2 )2 + (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )2 + 𝑣12 (𝑣1 𝑣2 )2 + (𝑣1 𝑣2 )3
4
16
8
16 )︂
45
23
79
161 2
− (𝑛12 𝑣1 )2 𝑣12 𝑣22 − (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12 𝑣22 + 𝑣14 𝑣22 −
𝑣 (𝑣1 𝑣2 )𝑣22
16
32
16
32 1
(︂
𝐺2 𝑚21 𝑚2
49
75
187
+
− (𝑛12 𝑣1 )4 + (𝑛12 𝑣1 )3 (𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2
2
𝑟12
8
8
8
247
49
81
(𝑛12 𝑣1 )(𝑛12 𝑣2 )3 + (𝑛12 𝑣1 )2 𝑣12 + (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12
+
24
8
8
21
11 4 15
3
2 2
2
− (𝑛12 𝑣2 ) 𝑣1 + 𝑣1 − (𝑛12 𝑣1 ) (𝑣1 𝑣2 ) − (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )
4
2
2
2

𝐸=

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 84

84

Luc Blanchet

21
55
49
(𝑛12 𝑣2 )2 (𝑣1 𝑣2 ) − 27𝑣12 (𝑣1 𝑣2 ) + (𝑣1 𝑣2 )2 + (𝑛12 𝑣1 )2 𝑣22
4
2
4
)︂
27
3
55
135 4
2
2 2
2 2
2
− (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣2 + (𝑛12 𝑣2 ) 𝑣2 + 𝑣1 𝑣2 − 28(𝑣1 𝑣2 )𝑣2 +
𝑣
2
4
4
16 2
(︂
)︂)︂
(︂
𝐺4 𝑚31 𝑚22 9707 22
𝑟12
3𝐺4 𝑚41 𝑚2
+
−
ln
+
4
4
8𝑟12
𝑟12
420
3
𝑟1′
(︂
3 2 2
𝐺 𝑚1 𝑚2 547
3115
123
575 2
+
(𝑛12 𝑣1 )2 −
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )(𝑛12 𝑣12 )𝜋 2 −
𝑣
3
𝑟12
12
48
64
18 1
)︂
41
4429
+ 𝜋 2 (𝑣1 𝑣12 ) +
(𝑣1 𝑣2 )
64
144
(︂
𝐺3 𝑚31 𝑚2
44627
3
32027
24187 2
+
−
(𝑛12 𝑣1 )2 +
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 )2 +
𝑣
3
𝑟12
840
840
2
2520 1
(︂ )︂
(︂ )︂)︂}︃
22
5 2
𝑟12
𝑟12
27967
(𝑣1 𝑣2 ) + 𝑣2 + 22(𝑛12 𝑣1 )(𝑛12 𝑣12 ) ln ′ − (𝑣1 𝑣12 ) ln ′
−
2520
4
𝑟1
3
𝑟1
(︂ )︂
1
+1↔2+𝒪 7 .
(205)
𝑐
+

To the terms given above, we must add the same terms but corresponding to the relabelling 1 ↔ 2.
Actually, this energy is not conserved because of the radiation reaction. Thus its time derivative,
as computed by means of the 3PN equations of motion themselves (i.e., by order-reducing all the
accelerations), is purely equal to the 2.5PN effect,
[︂
(︂
)︂
(︂
)︂]︂
d𝐸
4 𝐺2 𝑚21 𝑚2
𝐺𝑚1
𝐺𝑚2
𝐺𝑚1 52 𝐺𝑚2
2
2
=
(𝑣1 𝑣12 ) −𝑣12 + 2
−8
+ (𝑛12 𝑣1 )(𝑛12 𝑣12 ) 3𝑣12 − 6
+
3
d𝑡
5 𝑐5 𝑟12
𝑟12
𝑟12
𝑟12
3 𝑟12
(︂ )︂
1
(206)
+1↔2+𝒪 7 .
𝑐
The resulting energy balance equation can be better expressed by transfering to the left-hand side
certain 2.5PN terms so that we recognize in the right-hand side the familiar form of a total energy
flux. Posing
[︂
]︂
4𝐺2 𝑚21 𝑚2
2𝐺(𝑚1 − 𝑚2 )
2.5PN
2
𝐸
=𝐸+
(𝑛12 𝑣1 ) 𝑣12 −
+ 1 ↔ 2,
(207)
2
5𝑐5 𝑟12
𝑟12
we find agreement with the standard Einstein quadrupole formula (4):
(︂ )︂
𝐺 d3 Q𝑖𝑗 d3 Q𝑖𝑗
1
d𝐸 2.5PN
=− 5
+
𝒪
,
d𝑡
5𝑐 d𝑡3 d𝑡3
𝑐7

(208)

where the Newtonian trace-free quadrupole moment reads Q𝑖𝑗 = 𝑚1 (𝑦1𝑖 𝑦1𝑗 − 31 𝛿 𝑖𝑗 𝑦12 ) + 1 ↔ 2. We
refer to [258, 259] for the discussion of the energy balance equation up to the next 3.5PN order.
See also Eq. (158) for the energy balance equation at relative 1.5PN order for general fluid systems.

7.2

Lagrangian and Hamiltonian formulations

The conservative part of the equations of motion in harmonic coordinates (203) is derivable from
a generalized Lagrangian, depending not only on the positions and velocities of the bodies, but
also on their accelerations: 𝑎1 = d𝑣1 /d𝑡 and 𝑎2 = d𝑣2 /d𝑡. As shown in Ref. [147], the accelerations in the harmonic-coordinates Lagrangian occur already from the 2PN order. This fact is in

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 85

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

85

accordance with a general result [308] that N -body equations of motion cannot be derived from an
ordinary Lagrangian beyond the 1PN level, provided that the gauge conditions preserve the manifest Lorentz invariance. Note that we can always arrange for the dependence of the Lagrangian
upon the accelerations to be linear, at the price of adding some so-called “multi-zero” terms to the
Lagrangian, which do not modify the equations of motion (see, e.g., Ref. [169]). At the 3PN level,
we find that the Lagrangian also depends on accelerations. It is notable that these accelerations are
sufficient – there is no need to include derivatives of accelerations. Note also that the Lagrangian is
not unique because we can always add to it a total time derivative d𝐹/d𝑡, where 𝐹 is any function
depending on the positions and velocities, without changing the dynamics. We find [174]
𝑚1 𝑣12
𝐺𝑚1 𝑚2
+
2𝑟12
2
{︂
(︂
)︂}︂
2 2
𝐺 𝑚1 𝑚2
𝑚1 𝑣14
1
𝐺𝑚1 𝑚2
1
3 2 7
+
+ 2 −
+
−
(𝑛
𝑣
)(𝑛
𝑣
)
+
𝑣
−
(𝑣
𝑣
)
12 1
12 2
1 2
2
𝑐
2𝑟12
8
𝑟12
4
2 1 4
{︃
1 𝐺3 𝑚31 𝑚2
19𝐺3 𝑚21 𝑚22
+ 4
+
3
3
𝑐
2𝑟12
8𝑟12
(︂
)︂
7
1
1 2 7
7 2
𝐺2 𝑚21 𝑚2 7
2
2
(𝑛12 𝑣1 ) − (𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 ) + 𝑣1 − (𝑣1 𝑣2 ) + 𝑣2
+
2
𝑟12
2
2
2
4
4
4
(︂
𝐺𝑚1 𝑚2 3
7
7
3
+
(𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 − (𝑛12 𝑣2 )2 𝑣12 + 𝑣14 + (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )
𝑟12
16
8
8
4
)︂
6
1
15
𝑚
𝑣
1 1
− 2𝑣12 (𝑣1 𝑣2 ) + (𝑣1 𝑣2 )2 + 𝑣12 𝑣22 +
8
16
16
)︂ }︃
(︂
1
7
7
+ 𝐺𝑚1 𝑚2 − (𝑎1 𝑣2 )(𝑛12 𝑣2 ) − (𝑛12 𝑎1 )(𝑛12 𝑣2 )2 + (𝑛12 𝑎1 )𝑣22
4
8
8
{︃
(︂
1 𝐺2 𝑚21 𝑚2 13
83
35
245
+ 6
(𝑛12 𝑣1 )4 + (𝑛12 𝑣1 )3 (𝑛12 𝑣2 ) − (𝑛12 𝑣1 )2 (𝑛12 𝑣2 )2 −
(𝑛12 𝑣1 )2 𝑣12
2
𝑐
𝑟12
18
18
6
24

𝐿harm =

179
235
373 4 529
(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12 −
(𝑛12 𝑣2 )2 𝑣12 +
𝑣 +
(𝑛12 𝑣1 )2 (𝑣1 𝑣2 )
12
24
48 1
24
97
719 2
463
7
− (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 ) −
𝑣 (𝑣1 𝑣2 ) +
(𝑣1 𝑣2 )2 − (𝑛12 𝑣1 )2 𝑣22
6
24 1
24
24
)︂
1
463 2 2 19
45 4
1
2
2 2
2
𝑣 𝑣 − (𝑣1 𝑣2 )𝑣2 + 𝑣2
− (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣2 + (𝑛12 𝑣2 ) 𝑣2 +
2
4
48 1 2
2
16

+

+

5𝑚1 𝑣18
128 (︂

+ 𝐺𝑚1 𝑚2

3
5
1
(𝑎1 𝑣2 )(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 + (𝑎1 𝑣2 )(𝑛12 𝑣2 )3 + (𝑛12 𝑎1 )(𝑛12 𝑣1 )(𝑛12 𝑣2 )3
8
12
8
1
11
+ (𝑛12 𝑎1 )(𝑛12 𝑣2 )4 + (𝑎1 𝑣1 )(𝑛12 𝑣2 )𝑣12 − (𝑎1 𝑣2 )(𝑛12 𝑣2 )𝑣12
16
4
1
− 2(𝑎1 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 ) + (𝑎1 𝑣2 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )
4
3
5
15
2
+ (𝑛12 𝑎1 )(𝑛12 𝑣2 ) (𝑣1 𝑣2 ) − (𝑛12 𝑎1 )(𝑛12 𝑣1 )2 𝑣22 + (𝑎1 𝑣1 )(𝑛12 𝑣2 )𝑣22
8
8
8
15
1
2
2
− (𝑎1 𝑣2 )(𝑛12 𝑣2 )𝑣2 − (𝑛12 𝑎1 )(𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣2
8
)︂2
5
2 2
− (𝑛12 𝑎1 )(𝑛12 𝑣2 ) 𝑣2
16

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 86

86

Luc Blanchet

𝐺2 𝑚21 𝑚2
+
𝑟12

(︂

235
29
235
(𝑎2 𝑣1 )(𝑛12 𝑣1 ) − (𝑛12 𝑎2 )(𝑛12 𝑣1 )2 −
(𝑎1 𝑣2 )(𝑛12 𝑣2 )
24
24
24
17
185
235
− (𝑛12 𝑎1 )(𝑛12 𝑣2 )2 +
(𝑛12 𝑎1 )𝑣12 −
(𝑛12 𝑎2 )𝑣12
6
16
48
)︂
20
185
2
(𝑛12 𝑎1 )(𝑣1 𝑣2 ) + (𝑛12 𝑎1 )𝑣2
−
8
3
(︂
𝐺𝑚1 𝑚2
5
1
5
+
− (𝑛12 𝑣1 )3 (𝑛12 𝑣2 )3 + (𝑛12 𝑣1 )(𝑛12 𝑣2 )3 𝑣12 + (𝑛12 𝑣2 )4 𝑣12
𝑟12
32
8
8
1
11
11
− (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣14 + (𝑛12 𝑣2 )2 𝑣14 + 𝑣16
16
4
16
15
2
2
− (𝑛12 𝑣1 ) (𝑛12 𝑣2 ) (𝑣1 𝑣2 ) + (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12 (𝑣1 𝑣2 )
32
3
13
5
+ (𝑛12 𝑣2 )2 𝑣12 (𝑣1 𝑣2 ) − 𝑣14 (𝑣1 𝑣2 ) + (𝑛12 𝑣1 )(𝑛12 𝑣2 )(𝑣1 𝑣2 )2
8
16
16
1
5
23
1
+ (𝑣1 𝑣2 )3 − (𝑛12 𝑣1 )2 𝑣12 𝑣22 − (𝑛12 𝑣1 )(𝑛12 𝑣2 )𝑣12 𝑣22 + 𝑣14 𝑣22
16
8)︂
32
16
1
− 𝑣12 (𝑣1 𝑣2 )𝑣22
32
(︂
(︂
)︂)︂
𝑟12
3𝐺4 𝑚41 𝑚2
𝐺4 𝑚31 𝑚22
9707 22
+
ln
−
+
−
4
4
8𝑟12
𝑟12
420
3
𝑟1′
(︂
3 2 2
889
123
305 2
𝐺 𝑚1 𝑚2 383
(𝑛12 𝑣1 )2 −
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) −
(𝑛12 𝑣1 )(𝑛12 𝑣12 )𝜋 2 −
𝑣
+
3
𝑟12
24
48
64
72 1
)︂
439
41
(𝑣1 𝑣2 )
+ 𝜋 2 (𝑣1 𝑣12 ) +
64
144
(︂
𝐺3 𝑚31 𝑚2
8243
15541
3
15611 2
+
−
(𝑛12 𝑣1 )2 +
(𝑛12 𝑣1 )(𝑛12 𝑣2 ) + (𝑛12 𝑣2 )2 +
𝑣
3
𝑟12
210
420
2
1260 1
(︂
)︂
𝑟12
17501
5
−
(𝑣1 𝑣2 ) + 𝑣22 + 22(𝑛12 𝑣1 )(𝑛12 𝑣12 ) ln
1260
4
𝑟1′
(︂
)︂ )︂}︃
(︂ )︂
22
𝑟12
1
− (𝑣1 𝑣12 ) ln
+1↔2+𝒪 7 .
(209)
3
𝑟1′
𝑐
−

Witness the accelerations occurring at the 2PN and 3PN orders; see also the gauge-dependent
logarithms of 𝑟12 /𝑟1′ and 𝑟12 /𝑟2′ . We refer to [174] for the explicit expressions of the ten conserved
quantities corresponding to the integrals of energy [also given in Eq. (205)], linear and angular
momenta, and center-of-mass position. Notice that while it is strictly forbidden to replace the
accelerations by the equations of motion in the Lagrangian, this can and should be done in the
final expressions of the conserved integrals derived from that Lagrangian.
Now we want to exhibit a transformation of the particles’ dynamical variables – or contact
transformation, as it is called in the jargon – which transforms the 3PN harmonic-coordinates
Lagrangian (209) into a new Lagrangian, valid in some ADM or ADM-like coordinate system,
and such that the associated Hamiltonian coincides with the 3PN Hamiltonian that has been
obtained by Jaranowski & Schäfer [261, 262]. In ADM coordinates the Lagrangian will be ordinary,
depending only on the positions and velocities of the bodies. Let this contact transformation be
𝑌1 (𝑡) = 𝑦1 (𝑡) + 𝛿𝑦1 (𝑡) and 1 ↔ 2, where 𝑌1 and 𝑦1 denote the trajectories in ADM and harmonic
coordinates, respectively. For this transformation to be able to remove all the accelerations in the

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 87

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

87

initial Lagrangian 𝐿harm up to the 3PN order, we determine [174] it to be necessarily of the form
]︂
(︂ )︂
[︂
1 𝜕𝐿harm
1
𝜕𝐹
1
𝛿𝑦1 =
(and idem 1 ↔ 2) ,
(210)
+
+ 6 𝑋1 + 𝒪 8
𝑚1
𝜕𝑎1
𝜕𝑣1
𝑐
𝑐
where 𝐹 is a freely adjustable function of the positions and velocities, made of 2PN and 3PN
terms, and where 𝑋1 represents a special correction term, that is purely of order 3PN. The point
is that once the function 𝐹 is specified there is a unique determination of the correction term
𝑋1 for the contact transformation to work (see Ref. [174] for the details). Thus, the freedom
we have is entirely encoded into the function 𝐹 , and the work then consists in showing that there
exists a unique choice of 𝐹 for which our Lagrangian 𝐿harm is physically equivalent, via the contact
transformation (210), to the ADM Hamiltonian of Refs. [261, 262]. An interesting point is that not
only the transformation must remove all the accelerations in 𝐿harm , but it should also cancel out
all the logarithms ln(𝑟12 /𝑟1′ ) and ln(𝑟12 /𝑟2′ ), because there are no logarithms in ADM coordinates.
The result we find, which can be checked to be in full agreement with the expression of the gauge
vector in Eq. (204), is that 𝐹 involves the logarithmic terms
[︂
(︂
)︂
(︂
)︂]︂
𝑟12
𝑟12
22 𝐺3 𝑚1 𝑚2
2
2
𝑚
(𝑛
𝑣
)
ln
−
𝑚
(𝑛
𝑣
)
ln
+ ··· ,
(211)
𝐹 =
1 12 1
2 12 2
2
3 𝑐6 𝑟12
𝑟1′
𝑟2′
together with many other non-logarithmic terms (indicated by dots) that are entirely specified by
the isometry of the harmonic and ADM descriptions of the motion. For this particular choice of
𝐹 the ADM Lagrangian reads
(︂ )︂
1
𝛿𝐿harm 𝑖 𝛿𝐿harm 𝑖 d𝐹
𝛿𝑦
+
𝛿𝑦
+
+
𝒪
𝐿ADM = 𝐿harm +
.
(212)
1
2
d𝑡
𝑐8
𝛿𝑦1𝑖
𝛿𝑦2𝑖
Inserting into this equation all our explicit expressions we find
1
𝐺𝑚1 𝑚2
+ 𝑚1 𝑉12
2𝑅12
2
{︂
)︂}︂
(︂
1
𝐺2 𝑚21 𝑚2
1
𝐺𝑚1 𝑚2
3 2 7
1
4
+ 2 −
+ 𝑚1 𝑉1 +
− (𝑁12 𝑉1 )(𝑁12 𝑉2 ) + 𝑉1 − (𝑉1 𝑉2 )
2
𝑐
2𝑅12
8
𝑅12
4
2
4
{︃
5𝐺3 𝑚21 𝑚22
𝑚1 𝑉16
1 𝐺3 𝑚31 𝑚2
+
+
+ 4
3
3
𝑐
4𝑅12
8𝑅12
16
(︂
)︂
𝐺2 𝑚21 𝑚2 15
11 2 15
2
2
+
(𝑁
𝑉
)
+
𝑉
−
(𝑉
𝑉
)
+
2𝑉
12 1
1 2
2
2
𝑅12
8
8 1
4
(︂
𝐺𝑚1 𝑚2 3
1
5
7
(𝑁12 𝑉1 )2 (𝑁12 𝑉2 )2 − (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉12 − (𝑁12 𝑉2 )2 𝑉12 + 𝑉14
+
𝑅12
16
4
8
8
)︂}︃
3
7 2
1
11 2 2
2
+ (𝑁12 𝑉1 )(𝑁12 𝑉2 )(𝑉1 𝑉2 ) − 𝑉1 (𝑉1 𝑉2 ) + (𝑉1 𝑉2 ) + 𝑉1 𝑉2
4
4
8
16
{︃
(︂
)︂
1 5𝑚1 𝑉18
𝐺4 𝑚41 𝑚2
𝐺4 𝑚31 𝑚22
227 21 2
+ 6
−
+
−
+ 𝜋
4
4
𝑐
128
8𝑅12
𝑅12
24
32
(︂
𝐺𝑚1 𝑚2
5
3
+
− (𝑁12 𝑉1 )3 (𝑁12 𝑉2 )3 + (𝑁12 𝑉1 )2 (𝑁12 𝑉2 )2 𝑉12
𝑅12
32
16
9
3
5
+ (𝑁12 𝑉1 )(𝑁12 𝑉2 )3 𝑉12 − (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉14 − (𝑁12 𝑉2 )2 𝑉14
16
16
16
11 6 15
3
2
2
+ 𝑉1 − (𝑁12 𝑉1 ) (𝑁12 𝑉2 ) (𝑉1 𝑉2 ) + (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉12 (𝑉1 𝑉2 )
16
32
4

𝐿ADM =

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 88

88

Luc Blanchet

1
21
5
(𝑁12 𝑉2 )2 𝑉12 (𝑉1 𝑉2 ) − 𝑉14 (𝑉1 𝑉2 ) + (𝑁12 𝑉1 )(𝑁12 𝑉2 )(𝑉1 𝑉2 )2
16
16
16
1
1
5
+ 𝑉12 (𝑉1 𝑉2 )2 + (𝑉1 𝑉2 )3 − (𝑁12 𝑉1 )2 𝑉12 𝑉22
8
16
16
)︂
9
7 4 2 15 2
2 2
2
− (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉1 𝑉2 + 𝑉1 𝑉2 − 𝑉1 (𝑉1 𝑉2 )𝑉2
32
8
32
(︂
2 2
5
𝐺 𝑚1 𝑚2
13
23
− (𝑁12 𝑉1 )4 − (𝑁12 𝑉1 )3 (𝑁12 𝑉2 ) − (𝑁12 𝑉1 )2 (𝑁12 𝑉2 )2
+
2
𝑅12
12
8
24
13
1
5
21
+ (𝑁12 𝑉1 )2 𝑉12 + (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉12 + (𝑁12 𝑉2 )2 𝑉12 + 𝑉14
16
4
6
16
1
97
1
− (𝑁12 𝑉1 )2 (𝑉1 𝑉2 ) + (𝑁12 𝑉1 )(𝑁12 𝑉2 )(𝑉1 𝑉2 ) − 𝑉12 (𝑉1 𝑉2 )
2
3
16
29
43
341
(𝑉1 𝑉2 )2 + (𝑁12 𝑉1 )2 𝑉22 − (𝑁12 𝑉1 )(𝑁12 𝑉2 )𝑉22 + 𝑉12 𝑉22
+
48
24 )︂
12
71
47
− (𝑉1 𝑉2 )𝑉22 + 𝑉24
8
16
(︂
3 2 2
3
𝐺 𝑚1 𝑚2 73
(𝑁12 𝑉1 )2 − 11(𝑁12 𝑉1 )(𝑁12 𝑉2 ) + 𝜋 2 (𝑁12 𝑉1 )(𝑁12 𝑉12 )
+
3
𝑅12
16
64
)︂
265 2
1 2
59
−
𝑉 − 𝜋 (𝑉1 𝑉12 ) + (𝑉1 𝑉2 )
48 1
64
8
(︂
)︂ }︃
173 2 27
13 2
𝐺3 𝑚31 𝑚2
1
2
𝑉 − (𝑉1 𝑉2 ) + 𝑉2
+
−5(𝑁12 𝑉1 ) − (𝑁12 𝑉1 )(𝑁12 𝑉2 ) +
3
𝑅12
8
48 1
8
8
(︂ )︂
1
+1↔2+𝒪 7 .
(213)
𝑐
−

The notation is the same as in Eq. (209), except that we use upper-case letters to denote the ADMcoordinates positions and velocities; thus, for instance 𝑁12 = (𝑌1 −𝑌2 )/𝑅12 and (𝑁12 𝑉1 ) = 𝑁12 ·𝑉1 .
The Hamiltonian is simply deduced from the latter Lagrangian by applying the usual Legendre
transformation. Posing 𝑃1 = 𝜕𝐿ADM /𝜕𝑉1 and 1 ↔ 2, we get [261, 262, 263, 162, 174]
𝐺𝑚1 𝑚2
𝑃2
+ 1
2𝑅
2𝑚1
{︂ 12 4
(︂
)︂}︂
1
𝑃1
𝐺2 𝑚21 𝑚2
𝐺𝑚1 𝑚2 1 (𝑁12 𝑃1 )(𝑁12 𝑃2 ) 3 𝑃12
7 (𝑃1 𝑃2 )
+ 2 − 3+
+
−
+
2
𝑐
8𝑚1
2𝑅12
𝑅12
4
𝑚1 𝑚2
2 𝑚21
4 𝑚1 𝑚2
{︃
1
𝐺3 𝑚31 𝑚2
5𝐺3 𝑚21 𝑚22
𝑃16
+ 4
−
−
5
3
3
𝑐 16𝑚1
4𝑅12
8𝑅12
(︂
)︂
3 (𝑁12 𝑃1 )(𝑁12 𝑃2 ) 19 𝑃12
𝐺2 𝑚21 𝑚2
27 (𝑃1 𝑃2 )
5𝑃22
−
+
−
+
+
2
𝑅12
2
𝑚1 𝑚2
4 𝑚21
4 𝑚1 𝑚2
2𝑚22
(︂
𝐺𝑚1 𝑚2
3 (𝑁12 𝑃1 )2 (𝑁12 𝑃2 )2
5 (𝑁12 𝑃2 )2 𝑃12
+
−
+
2
2
𝑅12
16
𝑚1 𝑚2
8
𝑚21 𝑚22
)︂}︃
5 𝑃14
3 (𝑁12 𝑃1 )(𝑁12 𝑃2 )(𝑃1 𝑃2 ) 1 (𝑃1 𝑃2 )2
11 𝑃12 𝑃22
+
−
−
−
8 𝑚41
4
𝑚21 𝑚22
8 𝑚21 𝑚22
16 𝑚21 𝑚22
{︃
(︂
)︂
1
5𝑃18
𝐺4 𝑚41 𝑚2
𝐺4 𝑚31 𝑚22 227 21 2
+ 6 −
+
+
−
𝜋
4
4
𝑐
128𝑚71
8𝑅12
𝑅12
24
32

𝐻 ADM = −

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 89

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

𝐺3 𝑚21 𝑚22
+
3
𝑅12

89

43 (𝑁12 𝑃1 )2
119 (𝑁12 𝑃1 )(𝑁12 𝑃2 )
3 2 (𝑁12 𝑃1 )2
+
−
𝜋
16
𝑚21
16
𝑚1 𝑚2
64
𝑚21
2
2
3
1
143 (𝑃1 𝑃2 )
(𝑁12 𝑃1 )(𝑁12 𝑃2 ) 473 𝑃1
𝑃
+ 𝜋2
+ 𝜋 2 12 +
−
2
64
𝑚1 𝑚2
48 𝑚1
64 𝑚1
16 𝑚1 𝑚2
)︂
1 2 (𝑃1 𝑃2 )
− 𝜋
64 𝑚1 𝑚2
(︂
)︂
𝐺3 𝑚31 𝑚2 5 (𝑁12 𝑃1 )2
21 (𝑁12 𝑃1 )(𝑁12 𝑃2 ) 425 𝑃12
77 (𝑃1 𝑃2 ) 25𝑃22
+
+
+
−
−
3
𝑅12
4
𝑚21
8
𝑚1 𝑚2
48 𝑚21
8 𝑚1 𝑚2
8𝑚22
(︂
2 2
4
3
2
2
𝐺 𝑚1 𝑚2 5 (𝑁12 𝑃1 )
3 (𝑁12 𝑃1 ) (𝑁12 𝑃2 ) 10 (𝑁12 𝑃1 ) (𝑁12 𝑃2 )
+
−
+
2
4
𝑅12
12
𝑚1
2
𝑚31 𝑚2
3
𝑚21 𝑚22
2 2
2
17 (𝑁12 𝑃1 ) 𝑃1
15 (𝑁12 𝑃1 )(𝑁12 𝑃2 )𝑃1
55 (𝑁12 𝑃2 )2 𝑃12
+
−
−
16
𝑚41
8
𝑚31 𝑚2
12
𝑚21 𝑚22
𝑃14
11 (𝑁12 𝑃1 )2 (𝑃1 𝑃2 ) 125 (𝑁12 𝑃1 )(𝑁12 𝑃2 )(𝑃1 𝑃2 )
+
−
+
4
16𝑚1
8
𝑚31 𝑚2
12
𝑚21 𝑚22
115 𝑃12 (𝑃1 𝑃2 ) 25 (𝑃1 𝑃2 )2
193 (𝑁12 𝑃1 )2 𝑃22
371 𝑃12 𝑃22
−
+
−
+
3
2
2
2
2
16 𝑚1 𝑚2
48 𝑚1 𝑚2
48
𝑚1 𝑚2
48 𝑚21 𝑚22
)︂
27 𝑃24
−
16 𝑚42
(︂
𝐺𝑚1 𝑚2 5 (𝑁12 𝑃1 )3 (𝑁12 𝑃2 )3
3 (𝑁12 𝑃1 )2 (𝑁12 𝑃2 )2 𝑃12
+
+
3
3
𝑅12
32
𝑚1 𝑚2
16
𝑚41 𝑚22
5 (𝑁12 𝑃2 )2 𝑃14
7 𝑃16
9 (𝑁12 𝑃1 )(𝑁12 𝑃2 )3 𝑃12
−
−
−
3
4
3
2
16
𝑚1 𝑚2
16
𝑚1 𝑚2
16 𝑚61
15 (𝑁12 𝑃1 )2 (𝑁12 𝑃2 )2 (𝑃1 𝑃2 ) 3 (𝑁12 𝑃1 )(𝑁12 𝑃2 )𝑃12 (𝑃1 𝑃2 )
+
+
32
𝑚31 𝑚32
4
𝑚41 𝑚22
1 (𝑁12 𝑃2 )2 𝑃12 (𝑃1 𝑃2 )
5 (𝑁12 𝑃1 )(𝑁12 𝑃2 )(𝑃1 𝑃2 )2
+
−
3
3
16
𝑚1 𝑚2
16
𝑚31 𝑚32
1 𝑃12 (𝑃1 𝑃2 )2
1 (𝑃1 𝑃2 )3
5 (𝑁12 𝑃1 )2 𝑃12 𝑃22
+
−
−
8 𝑚41 𝑚22
16 𝑚31 𝑚32
16
𝑚41 𝑚22
)︂}︃
1 𝑃14 𝑃22
1 𝑃12 (𝑃1 𝑃2 )𝑃22
7 (𝑁12 𝑃1 )(𝑁12 𝑃2 )𝑃12 𝑃22
+
+
+
32
𝑚31 𝑚32
2 𝑚41 𝑚22
32
𝑚31 𝑚32
(︂ )︂
1
+1↔2+𝒪 7 .
(214)
𝑐
(︂

−

Arguably, the results given by the ADM-Hamiltonian formalism (for the problem at hand) look
simpler than their harmonic-coordinate counterparts. Indeed, the ADM Lagrangian is ordinary
– no accelerations – and there are no logarithms nor associated gauge constants 𝑟1′ and 𝑟2′ .50 Of
course, one is free to describe the binary motion in whatever coordinates one likes, and the two
formalisms, harmonic (209) and ADM (213) – (214), describe rigorously the same physics. On the
other hand, the higher complexity of the harmonic-coordinates Lagrangian (209) enables one to
perform more tests of the computations, notably by inquiring about the future of the constants 𝑟1′
and 𝑟2′ , that we know must disappear from physical quantities such as the center-of-mass energy
and the total gravitational-wave flux.
50 On the other hand, the ADM-Hamiltonian formalism provides a limited description of the gravitational radiation
field, compared to what will be done using harmonic coordinates in Section 9.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 90

90

7.3

Luc Blanchet

Equations of motion in the center-of-mass frame

In this section we translate the origin of coordinates to the binary’s center-of-mass by imposing the
vanishing of the binary’s mass dipole moment: I𝑖 = 0 in the notation of Part A. Actually the dipole
moment is computed as the center-of-mass conserved integral associated with the boost symmetry
of the 3PN equations of motion [174, 79]. This condition results in the 3PN-accurate relationship
between the individual positions in the center-of-mass frame 𝑦1 and 𝑦2 , and the relative position
𝑥 ≡ 𝑦1 − 𝑦2 and velocity 𝑣 ≡ 𝑣1 − 𝑣2 = d𝑥/d𝑡 (formerly denoted 𝑦12 and 𝑣12 ). We shall also use
the orbital separation 𝑟 ≡ |𝑥|, together with 𝑛 = 𝑥/𝑟 and 𝑟˙ ≡ 𝑛 · 𝑣. Mass parameters are: The
total mass 𝑚 = 𝑚1 + 𝑚2 (to be distinguished from the ADM mass denoted by M in Part A); the
relative mass difference Δ = (𝑚1 − 𝑚2 )/𝑚; the reduced mass 𝜇 = 𝑚1 𝑚2 /𝑚; and the very useful
symmetric mass ratio
𝑚1 𝑚2
𝜇
.
(215)
≡
𝜈≡
𝑚
(𝑚1 + 𝑚2 )2
The usefulness of this ratio lies in its interesting range of variation: 0 < 𝜈 ⩽ 1/4, with 𝜈 = 1/4
in the case of equal masses, and 𝜈 → 0 in the test-mass limit for one of the bodies. Thus 𝜈
is numerically rather small and may be viewed as a small expansion parameter. We also pose
𝑋1 = 𝑚1 /𝑚 and 𝑋2 = 𝑚2 /𝑚 so that Δ = 𝑋1 − 𝑋2 and 𝜈 = 𝑋1 𝑋2 .
For reference we give the 3PN-accurate expressions of the individual positions in the center-ofmass frame in terms of relative variables. They are in the form
(︂ )︂
[︁
]︁
1
𝑦1 = 𝑋2 + 𝜈 Δ 𝒫 𝑥 + 𝜈 Δ 𝒬 𝑣 + 𝒪 7 ,
(216a)
𝑐
(︂ )︂
[︁
]︁
1
𝑦2 = −𝑋1 + 𝜈 Δ 𝒫 𝑥 + 𝜈 Δ 𝒬 𝑣 + 𝒪 7 ,
(216b)
𝑐
where all post-Newtonian corrections, beyond Newtonian order, are proportional to the mass ratio
𝜈 and the mass difference Δ. The two dimensionless coefficients 𝒫 and 𝒬 read
{︂
}︂
1 𝑣2
𝐺𝑚
𝒫= 2
−
𝑐
2
2𝑟
{︂ 4
(︂ 2
)︂
(︂
)︂}︂
1 3𝑣
3 𝜈 𝑣4
𝐺𝑚
𝑟˙
3 𝑟˙ 2 𝜈
19 𝑣 2
3 𝜈 𝑣2
𝐺2 𝑚2 7 𝜈
+ 4
−
+
− +
+
+
+
−
𝑐
8
2
𝑟
8
4
8
2
𝑟2
4 2
{︂ 6
6
1 5𝑣
11 𝜈 𝑣
+ 6
−
+ 6 𝜈 2 𝑣6
𝑐
16
4
(︂
𝐺𝑚 𝑟˙ 4
5 𝑟˙ 4 𝜈
21 𝑟˙ 4 𝜈 2
5 𝑟˙ 2 𝑣 2
21 𝑟˙ 2 𝜈 𝑣 2
+
−
+
−
+
𝑟
16
8
16
16
16
)︂
2 2 2
4
2 4
11 𝑟˙ 𝜈 𝑣
53 𝑣
15 𝜈 𝑣
4
−
+
− 7𝜈 𝑣 −
2
16
2
)︂
(︂
2 2
2
2
2
𝐺 𝑚
73 𝑟˙ 𝜈
101 𝑣
33 𝜈 𝑣 2
7 𝑟˙
2 2
2 2
+
−
+
+ 4 𝑟˙ 𝜈 +
−
+ 3𝜈 𝑣
𝑟2
3
8
12
8
)︂}︂
(︂
𝜈2
22 (︁ 𝑟 )︁
𝐺3 𝑚3
14351 𝜈
+
−
+
−
+
ln ′′
,
(217a)
𝑟3
1260
8
2
3
𝑟0
{︂
}︂
{︂
}︂
1
7 𝐺𝑚 𝑟˙
1 4 𝐺𝑚 𝑣 2
8 𝐺2 𝑚2
𝒬= 4 −
+ 5
−
𝑐
4
𝑐
5
5𝑟
{︂
(︂ 2
)︂
(︂
)︂}︂
1
5 𝑟˙
19 𝑟˙ 2 𝜈
15 𝑣 2
21 𝜈 𝑣 2
𝐺2 𝑚2 𝑟˙
235 21 𝜈
+ 6 𝐺𝑚 𝑟˙
−
−
+
+
−
−
.
(217b)
𝑐
12
24
8
4
𝑟
24
4

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 91

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

91

Up to 2.5PN order there is agreement with the circular-orbit limit of Eqs. (6.4) in Ref. [45]. Notice
the 2.5PN radiation-reaction term entering the coefficient 𝒬; such 2.5PN term is explicitly displayed
for circular orbits in Eqs. (224) below. In Eqs. (217) the logarithms at the 3PN order appear only
in the coefficient 𝒫. They contain a particular combination 𝑟0′′ of the two gauge-constants 𝑟1′ and
𝑟2′ defined by
Δ ln 𝑟0′′ = 𝑋12 ln 𝑟1′ − 𝑋22 ln 𝑟2′ ,
(218)
and which happens to be different from a similar combination 𝑟0′ we shall find in the equations of
relative motion, see Eq. (221).
The 3PN and even 3.5PN center-of-mass equations of motion are obtained by replacing in the
3.5PN equations of motion (203) in a general frame, the positions and velocities by their centerof-mass expressions (216) – (217), applying as usual the order-reduction of all accelerations where
necessary. We write the relative acceleration in the center-of-mass frame in the form
(︂ )︂
]︁
)︀
𝐺𝑚 [︁(︀
1
d𝑣
(219)
= − 2 1+𝒜 𝑛+ℬ𝑣 +𝒪 8 ,
d𝑡
𝑟
𝑐
and find that the coefficients 𝒜 and ℬ are [79]
}︂
{︂
1
𝐺𝑚
3𝑟˙ 2 𝜈
𝒜= 2 −
+ 𝑣 2 + 3𝜈𝑣 2 −
(4 + 2𝜈)
𝑐
2
𝑟
{︂
1 15𝑟˙ 4 𝜈
45𝑟˙ 4 𝜈 2
9𝑟˙ 2 𝜈𝑣 2
+ 4
−
−
+ 6𝑟˙ 2 𝜈 2 𝑣 2 + 3𝜈𝑣 4 − 4𝜈 2 𝑣 4
𝑐
8
8
2
)︂
(︂
(︂
)︂ }︂
𝐺2 𝑚2
𝐺𝑚
13𝜈𝑣 2
87𝜈
+ 2𝜈 2 𝑣 2 +
+
−2𝑟˙ 2 − 25𝑟˙ 2 𝜈 − 2𝑟˙ 2 𝜈 2 −
9
+
𝑟
2
𝑟2
4
{︂
}︂
2
2 2
1
24 ˙𝑟𝜈𝑣 𝐺𝑚 136 ˙𝑟𝜈 𝐺 𝑚
+ 5 −
−
𝑐
5
𝑟
15
𝑟2
{︂
1
35𝑟˙ 6 𝜈
175𝑟˙ 6 𝜈 2
175𝑟˙ 6 𝜈 3
15𝑟˙ 4 𝜈𝑣 2
135𝑟˙ 4 𝜈 2 𝑣 2
255𝑟˙ 4 𝜈 3 𝑣 2
+ 6 −
+
−
+
−
+
𝑐
16
16
16
2
4
8
2
4
2 2 4
2 3 4
6
2 6
15𝑟˙ 𝜈𝑣
237𝑟˙ 𝜈 𝑣
45𝑟˙ 𝜈 𝑣
11𝜈𝑣
49𝜈 𝑣
−
+
−
+
−
+ 13𝜈 3 𝑣 6
2(︂
8
2
4
4
𝐺𝑚
69𝑟˙ 4 𝜈 2
75𝜈𝑣 4
+
79𝑟˙ 4 𝜈 −
− 30𝑟˙ 4 𝜈 3 − 121𝑟˙ 2 𝜈𝑣 2 + 16𝑟˙ 2 𝜈 2 𝑣 2 + 20𝑟˙ 2 𝜈 3 𝑣 2 +
𝑟
2
4
)︂
+ 8𝜈 2 𝑣 4 − 10𝜈 3 𝑣 4
(︂
𝐺2 𝑚2 2 32573𝑟˙ 2 𝜈
11𝑟˙ 2 𝜈 2
26987𝜈𝑣 2
615𝑟˙ 2 𝜈𝜋 2
2 3
+
𝑟
˙
+
−
7
𝑟
˙
−
+ 𝜈 3 𝑣2
+
𝜈
+
𝑟2
168
8
64
840
(︂ )︂
(︂ )︂ )︂
123𝜈𝜋 2 𝑣 2
𝑟
𝑟
2
2
−
− 110𝑟˙ 𝜈 ln
+ 22𝜈𝑣 ln
′
64
𝑟0
𝑟0′
(︂
)︂ }︂
3 3
2
2
𝐺 𝑚
437𝜈
71𝜈
41𝜈𝜋
+
−16 −
−
+
3
𝑟
4
2
16
{︂
(︂
)︂
1 𝐺𝑚
366 4
+ 7
𝑟˙
𝜈𝑣 + 12𝜈 2 𝑣 4 − 114𝑣 2 𝜈 𝑟˙ 2 − 12𝜈 2 𝑣 2 𝑟˙ 2 + 112𝜈 𝑟˙ 4
𝑐
𝑟
35
(︂
)︂
𝐺2 𝑚2
692 2 724 2 2 294 2 376 2 2
+
𝑟
˙
𝜈𝑣
−
𝑣
𝜈
+
𝜈
𝑟
˙
+
𝜈
𝑟
˙
𝑟2
35
15
5
5
(︂
)︂ }︂
𝐺3 𝑚3
3956
184 2
+
𝑟˙
𝜈+
𝜈
,
(220a)
𝑟3
35
5

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 92

92

Luc Blanchet

1
{−4𝑟˙ + 2 ˙𝑟𝜈}
𝑐2 {︂
(︂
)︂}︂
1 9𝑟˙ 3 𝜈
15 ˙𝑟𝜈𝑣 2
𝐺𝑚
41 ˙𝑟𝜈
3 2
2 2
2
+ 4
+ 3𝑟˙ 𝜈 −
− 2 ˙𝑟𝜈 𝑣 +
2𝑟˙ +
+ 4 ˙𝑟𝜈
𝑐
2
2
𝑟
2
{︂
}︂
1 8𝜈𝑣 2 𝐺𝑚 24𝜈 𝐺2 𝑚2
+ 5
+
𝑐
5
𝑟
5
𝑟2
{︂
5
1
45𝑟˙ 𝜈
15𝑟˙ 5 𝜈 3
111𝑟˙ 3 𝜈 2 𝑣 2
65 ˙𝑟𝜈𝑣 4
+ 6 −
+ 15𝑟˙ 5 𝜈 2 +
+ 12𝑟˙ 3 𝜈𝑣 2 −
− 12𝑟˙ 3 𝜈 3 𝑣 2 −
𝑐
8
4
4
8

ℬ=

+ 19 ˙𝑟𝜈 2 𝑣 4 + 6 ˙𝑟𝜈 3 𝑣 4
(︂
)︂
𝐺𝑚 329𝑟˙ 3 𝜈
59𝑟˙ 3 𝜈 2
+
+
+ 18𝑟˙ 3 𝜈 3 − 15 ˙𝑟𝜈𝑣 2 − 27 ˙𝑟𝜈 2 𝑣 2 − 10 ˙𝑟𝜈 3 𝑣 2
𝑟
6
2
(︂
(︂ )︂)︂ }︂
18169 ˙𝑟𝜈
𝐺2 𝑚2
123 ˙𝑟𝜈𝜋 2
𝑟
2
3
−4
𝑟
˙
−
+
+
25
𝑟𝜈
˙
+
8
𝑟𝜈
˙
−
+
44
𝑟𝜈
˙
ln
2
𝑟
840
32
𝑟0′
{︂
(︂
)︂
1 𝐺𝑚
626 4 12 2 4 678 2 2 12 2 2 2
+ 7
−
𝜈𝑣 − 𝜈 𝑣 +
𝜈𝑣 𝑟˙ + 𝜈 𝑣 𝑟˙ − 120𝜈 𝑟˙ 4
𝑐
𝑟
35
5
5
5
)︂
(︂
𝐺2 𝑚2 164 2 148 2 2 82 2 848 2 2
+
𝜈𝑣
+
𝜈
𝑣
−
𝜈
𝑟
˙
−
𝜈
𝑟
˙
𝑟2
21
5
3
15
)︂ }︂
(︂
3 3
𝐺 𝑚
104 2
1060
+
𝜈−
𝜈
.
−
𝑟3
21
5

(220b)

Up to the 2.5PN order the result agrees with Ref. [302]. The 3.5PN term is issued from Refs. [258,
259, 260, 336, 278, 322, 254]. At the 3PN order we have some gauge-dependent logarithms containing a constant 𝑟0′ which is the “logarithmic barycenter” of the two constants 𝑟1′ and 𝑟2′ :
ln 𝑟0′ = 𝑋1 ln 𝑟1′ + 𝑋2 ln 𝑟2′ .

(221)

The logarithms in Eqs. (220), together with the constant 𝑟0′ therein, can be removed by applying
the gauge transformation (204), while still staying within the class of harmonic coordinates. The
resulting modification of the equations of motion will affect only the coefficients of the 3PN order
in Eqs. (220); let us denote them by 𝒜3PN and ℬ3PN . The new values of these coefficients, obtained
after removal of the logarithms by the latter harmonic gauge transformation, will be denoted 𝒜MH
3PN
MH
and ℬ3PN
. Here MH stands for the modified harmonic coordinate system, differing from the SH
(standard harmonic) coordinate system containing logarithms at the 3PN order in the coefficients
𝒜3PN and ℬ3PN . See Ref. [9] for a full description of the coordinate transformation between SH
and MH coordinates for various quantities. We have [320, 9]
{︂
1
35𝑟˙ 6 𝜈
175𝑟˙ 6 𝜈 2
175𝑟˙ 6 𝜈 3
15𝑟˙ 4 𝜈𝑣 2
135𝑟˙ 4 𝜈 2 𝑣 2
255𝑟˙ 4 𝜈 3 𝑣 2
15𝑟˙ 2 𝜈𝑣 4
MH
𝒜3PN = 6 −
+
−
+
−
+
−
𝑐
16
16
16
2
4
8
2
2 2 4
2 3 4
6
2 6
237𝑟˙ 𝜈 𝑣
45𝑟˙ 𝜈 𝑣
11𝜈𝑣
49𝜈 𝑣
+
−
+
−
+ 13𝜈 3 𝑣 6
8
2
4
4
(︂
𝐺𝑚
69𝑟˙ 4 𝜈 2
75𝜈𝑣 4
+
79𝑟˙ 4 𝜈 −
− 30𝑟˙ 4 𝜈 3 − 121𝑟˙ 2 𝜈𝑣 2 + 16𝑟˙ 2 𝜈 2 𝑣 2 + 20𝑟˙ 2 𝜈 3 𝑣 2 +
𝑟
2
4
)︂
+ 8𝜈 2 𝑣 4 − 10𝜈 3 𝑣 4
(︂
𝐺2 𝑚2 2 22717𝑟˙ 2 𝜈
11𝑟˙ 2 𝜈 2
615𝑟˙ 2 𝜈𝜋 2
20827𝜈𝑣 2
+
𝑟˙ +
+
− 7𝑟˙ 2 𝜈 3 +
−
+ 𝜈 3 𝑣2
2
𝑟
168
8
64
840
)︂
123𝜈𝜋 2 𝑣 2
−
64

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 93

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

93

(︂
)︂ }︂
1399𝜈
𝐺3 𝑚3
71𝜈 2
41𝜈𝜋 2
−16 −
+
−
+
,
(222a)
𝑟3
12
2
16
{︂
45𝑟˙ 5 𝜈
1
15𝑟˙ 5 𝜈 3
111𝑟˙ 3 𝜈 2 𝑣 2
65 ˙𝑟𝜈𝑣 4
MH
ℬ3PN
= 6 −
+ 15𝑟˙ 5 𝜈 2 +
+ 12𝑟˙ 3 𝜈𝑣 2 −
− 12𝑟˙ 3 𝜈 3 𝑣 2 −
𝑐
8
4
4
8
+ 19 ˙𝑟𝜈 2 𝑣 4 + 6 ˙𝑟𝜈 3 𝑣 4
(︂
)︂
𝐺𝑚 329𝑟˙ 3 𝜈
59𝑟˙ 3 𝜈 2
3 3
2
2 2
3 2
+
+
+ 18𝑟˙ 𝜈 − 15 ˙𝑟𝜈𝑣 − 27 ˙𝑟𝜈 𝑣 − 10 ˙𝑟𝜈 𝑣
𝑟
6
2
(︂
)︂ }︂
𝐺2 𝑚2
5849 ˙𝑟𝜈
123 ˙𝑟𝜈𝜋 2
2
3
−4
𝑟
˙
−
.
+
+
25
𝑟𝜈
˙
+
8
𝑟𝜈
˙
−
𝑟2
840
32

(222b)

Again, the other terms in the equations of motion (219) – (220) are unchanged. These gaugetransformed coefficients in MH coordinates are useful because they do not yield the usual complications associated with logarithms. However, they must be handled with care in applications
such as in Ref. [320], because one must ensure that all other quantities in the problem (energy,
angular momentum, gravitational-wave fluxes, etc.) are defined in the same specific MH gauge
avoiding logarithms. In the following we shall no longer use the MH coordinate system leading to
Eqs. (222), except when constructing the generalized quasi-Keplerian representation of the 3PN
motion in Section 10.2. Therefore all expressions we shall derive below, notably all those concerning the radiation field, are valid in the SH coordinate system in which the equations of motion are
fully given by Eq. (203) or, in the center-of-mass frame, by Eqs. (219) – (220).
For future reference let also give the 3PN center-of-mass Hamiltonian in ADM coordinates
derived in Refs. [261, 262, 162]. In the center-of-mass frame the conjugate variables are the relative
separation 𝑋 = 𝑌1 − 𝑌2 and the conjugate momentum (per unit reduced mass) 𝑃 such that
𝜇𝑃 = 𝑃1 = −𝑃2 where 𝑃1 and 𝑃2 are defined in Section 7.2). Posing 𝑁 ≡ 𝑋/𝑅 with 𝑅 ≡ |𝑋|,
together with 𝑃 2 ≡ 𝑃 2 and 𝑃𝑅 ≡ 𝑁 · 𝑃 , we have
𝐻 ADM
𝑃2
𝐺𝑚
=
−
𝜇
2
𝑅
{︂
(︂
)︂
}︂
1
𝑃4
3𝜈 𝑃4
𝐺𝑚
𝑃𝑅 2 𝜈
3𝑃2
𝜈 𝑃2
𝐺2 𝑚2
+ 2 −
+
+
−
−
−
+
𝑐
8
8
𝑅
2
2
2
2𝑅2
{︂ 6
6
2 6
1 𝑃
5𝜈 𝑃
5𝜈 𝑃
+ 4
−
+
𝑐
16
16
16
(︂
)︂
4 2
𝐺𝑚
3 𝑃𝑅 𝜈
𝑃𝑅 2 𝑃 2 𝜈 2
5𝑃4
5𝜈 𝑃4
3 𝜈2 𝑃 4
+
−
−
+
−
−
𝑅
8
4
8
2
8
(︂
)︂
2
2 2
2
𝐺 𝑚
3 𝑃𝑅 𝜈
5𝑃
+
+
+ 4𝜈 𝑃2
𝑅2
2
2
(︂
)︂ }︂
𝐺3 𝑚3
1 3𝜈
+
−
−
𝑅3
4
4
{︂
8
8
5𝑃
35 𝜈 𝑃
35 𝜈 2 𝑃 8
35 𝜈 3 𝑃 8
1
+
−
+
+ 6 −
𝑐
128
128
64
128
(︂
6 3
4 2 2
𝐺𝑚
5 𝑃𝑅 𝜈
3 𝑃𝑅 𝑃 𝜈
3 𝑃𝑅 4 𝑃 2 𝜈 3
𝑃𝑅 2 𝑃 4 𝜈 2
+
−
+
−
+
𝑅
16
16
16
8
)︂
2 4 3
6
6
2 6
7𝑃
21 𝜈 𝑃
53 𝜈 𝑃
5 𝜈3 𝑃 6
3 𝑃𝑅 𝑃 𝜈
−
−
+
−
−
16
16
8
16
16
(︂
𝐺2 𝑚2 5 𝑃𝑅 4 𝜈
43 𝑃𝑅 4 𝜈 2
17 𝑃𝑅 2 𝑃 2 𝜈
+
+
+
𝑅2
12
12
16

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 94

94

Luc Blanchet

15 𝑃𝑅 2 𝑃 2 𝜈 2
27 𝑃 4
17 𝜈 𝑃 4
109 𝜈 2 𝑃 4
+
−
+
+
8
16
2
16
(︂
2
2 2
3 3
2
85 𝑃𝑅 𝜈
𝐺 𝑚
7 𝑃𝑅 𝜈
25 𝑃
335 𝜈 𝑃 2
−
+
−
−
−
3
𝑅
16
4
8
48
)︂
2
2 2
2
2 2
23 𝜈 𝑃
3 𝑃𝑅 𝜈 𝜋
𝜈𝑃 𝜋
−
−
+
8
64
64
(︂
)︂ }︂
(︂ )︂
4 4
2
𝐺 𝑚
1 109 𝜈
21 𝜈 𝜋
1
+
+
−
+𝒪 8 .
𝑅4
8
12
32
𝑐

7.4

)︂

(223)

Equations of motion and energy for quasi-circular orbits

Most inspiralling compact binaries will have been circularized by the time they become visible by
the detectors LIGO and VIRGO; see Section 1.2. In the case of orbits that are circular – apart from
the gradual radiation-reaction inspiral – the complicated equations of motion simplify drastically,
since we have 𝑟˙ = (𝑛𝑣) = 𝒪(1/𝑐5 ). For circular orbits, up to the 2.5PN order, the relation between
center-of-mass variables and the relative ones reads
(︂ )︂
[︁
]︁ 4 𝐺2 𝜈𝑚2 Δ
1
𝑦1 = 𝑥 𝑋2 + 3𝛾 2 𝜈Δ −
𝑣
+
𝒪
,
(224a)
5
𝑟𝑐5
𝑐6
(︂ )︂
[︁
]︁ 4 𝐺2 𝜈𝑚2 Δ
1
𝑣
+
𝒪
𝑦2 = 𝑥 −𝑋1 + 3𝛾 2 𝜈Δ −
,
(224b)
5
𝑟𝑐5
𝑐6
where we recall 𝑋1 = 𝑚1 /𝑚, 𝑋2 = 𝑚2 /𝑚 and Δ = 𝑋1 − 𝑋2 . See Eqs. (216) – (217) for more
general formulas. To conveniently display the successive post-Newtonian corrections, we employ
the post-Newtonian parameter
(︂ )︂
1
𝐺𝑚
(225)
𝛾≡ 2 =𝒪 2 .
𝑟𝑐
𝑐
Notice that there are no corrections of order 1PN in Eqs. (224) for circular orbits; the dominant
term is of order 2PN, i.e., is proportional to 𝛾 2 = 𝒪(1/𝑐4 ). See Ref. [79] for a systematic calculation
of Eqs. (224) to higher order.
The relative acceleration 𝑎 ≡ 𝑎1 − 𝑎2 of two bodies moving on a circular orbit at the 3.5PN
order is then given by
[︂
(︂
)︂]︂
(︂ )︂
32 𝐺3 𝑚3 𝜈
743 11
1
𝑎 = −Ω2 𝑥 −
1
+
𝛾
−
−
𝜈
𝑣
+
𝒪
,
(226)
5
4
5 𝑐 𝑟
336
4
𝑐8
where 𝑥 ≡ 𝑦1 − 𝑦2 is the relative separation (in harmonic coordinates) and Ω denotes the angular
frequency of the circular motion. The second term in Eq. (226), opposite to the velocity 𝑣 ≡ 𝑣1 −𝑣2 ,
represents the radiation reaction force up to 3.5PN order, which comes from the reduction of the
coefficients of 1/𝑐5 and 1/𝑐7 in Eqs. (220). The radiation-reaction force is responsible for the
secular decrease of the separation 𝑟 and increase of the orbital frequency Ω:
[︂
(︂
)︂]︂
64 𝐺3 𝑚3 𝜈
1751 7
𝑟˙ = −
1
+
𝛾
−
−
𝜈
,
(227a)
5 𝑟 3 𝑐5
336
4
[︂
(︂
)︂]︂
96 𝐺𝑚𝜈 5/2
2591 11
Ω̇ =
𝛾
1
+
𝛾
−
−
𝜈
.
(227b)
5 𝑟3
336
12
Concerning conservative effects, the main content of the 3PN equations (226) is the relation
between the frequency Ω and the orbital separation 𝑟, which is given by the following generalized

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 95

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

95

version of Kepler’s third law:
{︂
(︂
)︂
41
𝐺𝑚
2
Ω = 3 1 + (−3 + 𝜈)𝛾 + 6 + 𝜈 + 𝜈 𝛾 2
(228)
𝑟
4
(︂
[︂
(︂ )︂]︂
)︂ }︂
(︂ )︂
19
75707 41 2
𝑟
1
𝜈 + 𝜈2 + 𝜈3 𝛾3 + 𝒪 8 .
+ −10 + −
+ 𝜋 + 22 ln
′
840
64
𝑟0
2
𝑐
2

The length scale 𝑟0′ is given in terms of the two gauge-constants 𝑟1′ and 𝑟2′ by Eq. (221). As for the
energy, it is inferred from the circular-orbit reduction of the general result (205). We have
{︂
(︂
)︂
(︂
)︂
7 1
7 49
1 2
𝜇𝑐2 𝛾
1 + − + 𝜈 𝛾 + − + 𝜈 + 𝜈 𝛾2
(229)
𝐸=−
2
4 4
8
8
8
(︂
[︂
(︂ )︂]︂
)︂ }︂
(︂ )︂
27
235
46031 123 2 22
𝑟
5
1
𝜈 + 𝜈2 + 𝜈3 𝛾3 + 𝒪 8 .
+ −
+
−
𝜋 +
ln
′
64
2240
64
3
𝑟0
32
64
𝑐
This expression is that of a physical observable 𝐸; however, it depends on the choice of a coordinate system, as it involves the post-Newtonian parameter 𝛾 defined from the harmonic-coordinate
separation 𝑟. But the numerical value of 𝐸 should not depend on the choice of a coordinate system, so 𝐸 must admit a frame-invariant expression, the same in all coordinate systems. To find
it we re-express 𝐸 with the help of the following frequency-related parameter 𝑥, instead of the
post-Newtonian parameter 𝛾:51
(︂
𝑥≡

𝐺𝑚Ω
𝑐3

)︂2/3

(︂
=𝒪

1
𝑐2

)︂
.

(230)

We readily obtain from Eq. (228) the expression of 𝛾 in terms of 𝑥 at 3PN order,
{︂
(︂
)︂
(︁
𝜈 )︁
65
𝛾 =𝑥 1+ 1−
𝑥 + 1 − 𝜈 𝑥2
3
12
(︂ )︂]︂
)︂
(︂ )︂}︂
(︂
[︂
𝑟
1
41 2 22
1 3
2203
229 2
3
−
𝜋 −
ln
𝜈 + 𝜈 𝑥 +𝒪 8
+ 1+ −
𝜈+
,
′
2520 192
3
𝑟0
36
81
𝑐

(231)

that we substitute back into Eq. (229), making all appropriate post-Newtonian re-expansions. As
a result, we gladly discover that the logarithms together with their associated gauge constant 𝑟0′
have cancelled out. Therefore, our result is [160, 69]
)︂
(︂
)︂
{︂
(︂
1
27 19
1 2
3
𝜇𝑐2 𝑥
1 + − − 𝜈 𝑥 + − + 𝜈 − 𝜈 𝑥2
𝐸=−
2
4 12
8
8
24
(︂
[︂
]︂
)︂ }︂
(︂ )︂
675
34445 205 2
155 2
35 3
1
3
+ −
+
−
𝜋 𝜈−
𝜈 −
𝜈 𝑥 +𝒪 8 .
64
576
96
96
5184
𝑐

(232)

For circular orbits one can check that there are no terms of order 𝑥7/2 in Eq. (232), so this result
is actually valid up to the 3.5PN order. We shall discuss in Section 11 how the effects of the spins
of the two black holes affect the latter formula.
The formula (232) has been extended to include the logarithmic terms ∝ ln 𝑥 at the 4PN and
5PN orders [67, 289], that are due to tail effects occurring in the near zone, see Sections 5.2 and
51 This parameter is an invariant in a large class of coordinate systems – those for which the metric becomes
asymptotically Minkowskian far from the system: 𝑔𝛼𝛽 → diag(−1, 1, 1, 1).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 96

96

Luc Blanchet

5.4. Adding also the Schwarzschild test-mass limit52 up to 5PN order, we get:
{︂
(︂
)︂
(︂
)︂
𝜇𝑐2 𝑥
3
𝜈
27 19
𝜈2
𝐸=−
1+ − −
𝑥+ − + 𝜈−
𝑥2
2
4 12
8
8
24
(︂
[︂
]︂
)︂
675
34445 205 2
155 2
35 3
+ −
+
−
𝜋 𝜈−
𝜈 −
𝜈 𝑥3
64
576
96
96
5184
(︂
)︂
3969
448
+ −
+ 𝜈 𝑒4 (𝜈) +
𝜈 ln 𝑥 𝑥4
128
15
)︂
(︂
[︂
]︂
)︂ }︂
(︂
45927
4988 656
1
5
+ −
+ 𝜈 𝑒5 (𝜈) + −
−
𝜈 𝜈 ln 𝑥 𝑥 + 𝒪 12 .
512
35
5
𝑐
We can write also a similar expression for the angular momentum,
{︂
(︂
)︂
(︂
)︂
𝐺𝜇𝑚
3 𝜈
27 19
𝜈2
J=
1
+
+
𝑥
+
−
𝜈
+
𝑥2
2 6
8
8
24
𝑐 𝑥1/2
(︂
[︂
]︂
)︂
135
6889 41 2
31
7 3
+
+ −
+ 𝜋 𝜈 + 𝜈2 +
𝜈 𝑥3
16
144
24
24
1296
(︂
)︂
2835
64
+
+ 𝜈 𝑗4 (𝜈) − 𝜈 ln 𝑥 𝑥4
128
3
(︂
[︂
]︂
)︂ }︂
(︂
)︂
15309
9976 1312
1
+
+ 𝜈 𝑗5 (𝜈) +
+
𝜈 𝜈 ln 𝑥 𝑥5 + 𝒪 12 .
256
105
15
𝑐

(233)

(234)

For circular orbits the energy 𝐸 and angular momentum J are known to be linked together by the
so-called “thermodynamic” relation
𝜕J
𝜕𝐸
=Ω
,
(235)
𝜕Ω
𝜕Ω
which is actually just one aspect of the “first law of binary black hole mechanics” that we shall
discuss in more details in Section 8.3.
We have introduced in Eqs. (233) – (234) some non-logarithmic 4PN and 5PN coefficients 𝑒4 (𝜈),
𝑗4 (𝜈) and 𝑒5 (𝜈), 𝑗5 (𝜈), which can however be proved to be polynomials in the symmetric mass ratio
𝜈.53 Recent works on the 4PN approximation to the equations of motion by means of both EFT
methods [204] and the traditional ADM-Hamiltonian approach [264, 265], and complemented by
an analytic computation of the gravitational self-force in the small mass ratio 𝜈 limit [36], have
yielded the next-order 4PN coefficient as (𝛾E being Euler’s constant)
123671 9037 2 1792
896
𝑒4 (𝜈) = −
+
𝜋 +
ln 2 +
𝛾E
1536
15
]︂ 15
[︂ 5760
301 2
77 3
498449 3157 2
+
𝜋 𝜈+
𝜈 +
𝜈 .
+ −
3456
576
1728
31104

(236)

The numerical value 𝑒4 (0) ≃ 153.88 was predicted before thanks to a comparison with numerical
self-force calculations [289, 287].
52 Namely,

[︂
]︂
1 − 2𝑥
𝐸 Schw = 𝜇𝑐2 √
−1 .
1 − 3𝑥
53 From the thermodynamic relation (235) we necessarily have the relations

5
64
𝑗4 (𝜈) = − 𝑒4 (𝜈) +
,
7
35
2
4988
656
𝑗5 (𝜈) = − 𝑒5 (𝜈) −
−
𝜈.
3
945
135

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 97

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

7.5

97

The 2.5PN metric in the near zone

The near-zone metric is given by Eqs. (144) for general post-Newtonian matter sources. For pointparticles binaries all the potentials 𝑉 , 𝑉𝑖 , · · · parametrizing the metric must be computed and
iterated for delta-function sources. Up to the 2.5PN order it is sufficient to cure the divergences
due to singular sources by means of the Hadamard self-field regularization. Let us point out that
the computation is greatly helped – and indeed is made possible at all – by the existence of the
following solution 𝑔 of the elementary Poisson equation
Δ𝑔 =

1
,
𝑟1 𝑟2

(237)

which takes the very nice closed analytic form [202]
𝑔 = ln 𝑆 ,
𝑆 ≡ 𝑟1 + 𝑟2 + 𝑟12 ,

(238a)
(238b)

where 𝑟a = |𝑥 − 𝑦a | and 𝑟12 = |𝑦1 − 𝑦2 |. Furthermore, to obtain the metric at the 2.5PN order,
the solutions of even more difficult elementary Poisson equations are required. Namely we meet
(︂ )︂
1
Δ𝐾1 = 2 𝜕𝑖 𝜕𝑗
𝜕𝑖 𝜕𝑗 ln 𝑟1 ,
(239a)
𝑟2
(︂ )︂
1
(239b)
Δ𝐻1 = 2 𝜕𝑖 𝜕𝑗
𝜕𝑖 𝜕𝑗 𝑔 ,
𝑟1 1 2
with a 𝜕𝑖 denoting the partial derivatives with respect to the source points 𝑦a𝑖 (and as usual 𝜕𝑖 being
the partial derivative with respect to the field point 𝑥𝑖 ). It is quite remarkable that the solutions of
the latter equations are known in closed analytic form. By combining several earlier results from
Refs. [120, 324, 377], one can write these solutions into the form [64, 76]
(︂
)︂ [︂
]︂
[︂
]︂
1
1
ln 𝑟1
1
ln 𝑟12
𝑟2
𝐾1 =
Δ − Δ1
+ Δ2
+ 2 2+ 2
,
(240a)
2
𝑟2
2
𝑟2
2𝑟12 𝑟1
𝑟12 𝑟2
)︂]︂
[︂
(︂
𝑟2
1
𝑔
ln 𝑟1
𝑟1 + 𝑟12
𝑔
− 2 2
𝐻1 = Δ1
+
− Δ1
2
𝑟1
𝑟12
2
2𝑟1 𝑟12
[︂
]︂
[︂
]︂
ln 𝑟12
ln 𝑟1
1
ln 𝑟12
+ 𝜕𝑖 𝜕𝑖
+
+ Δ2
,
(240b)
𝑟1
2𝑟12
2
𝑟1
2
where Δa are the Laplacians with respect to the two source points.
We report here the complete expression of the 2.5PN metric in harmonic coordinates valid at
any field point in the near zone. Posing 𝑔𝛼𝛽 = 𝜂𝛼𝛽 + 𝑘𝛼𝛽 we have [76]
[︂
)︀
1 𝐺𝑚1 (︀
𝐺2 𝑚2
2𝐺𝑚1
+ 4
−(𝑛1 𝑣1 )2 + 4𝑣12 − 2 2 1
𝑘00 = 2
𝑐 𝑟1
𝑐
𝑟1
𝑟1
(︂
)︂]︂
2
2
𝑟
𝑟
5
4𝐺2 𝑚1 𝑚2
1
1
2
+ 𝐺 𝑚1 𝑚2 −
− 3 +
−
+
(𝑛12 𝑣12 )
3
2
𝑟1 𝑟2
2𝑟12
2𝑟2 𝑟12
2𝑟2 𝑟12
3𝑐5 𝑟12
[︂
(︂
)︂
)︀
1 𝐺𝑚1 3
𝐺2 𝑚21 (︀
𝐺3 𝑚31
2
2
+ 6
(𝑛1 𝑣1 )4 − 3(𝑛1 𝑣1 )2 𝑣12 + 4𝑣14 +
3(𝑛
𝑣
)
−
𝑣
+
2
1
1
1
𝑐
𝑟1
4
𝑟12
𝑟13
(︂ (︂ 3
2
2
3
2
3𝑟1
3𝑟 𝑟2
3𝑟1 𝑟2
3𝑟
37𝑟1
𝑟
3𝑟2
+ 𝐺2 𝑚1 𝑚2 𝑣12
− 15 −
+ 52 − 3 + 13 + 3
5
5
8𝑟12
8𝑟12
8𝑟12
8𝑟12
8𝑟12
𝑟2 𝑟12
8𝑟12
)︂
2𝑟22
6
5
8𝑟12
16
+ 3 +
−
−
+
𝑟1 𝑟12
𝑟1 𝑟12
𝑟2 𝑟12
𝑟1 𝑟2 𝑆
𝑟12 𝑆

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 98

98

Luc Blanchet

)︂
3𝑟12 𝑟2
13𝑟1
2𝑟12
6
8
3𝑟13
16
12
+ (𝑣1 𝑣2 )
− 5 +
−
−
5 + 4𝑟 3 − 𝑟 𝑟 3 − 𝑟 𝑟
𝑟1 𝑟2
4𝑟12
4𝑟12
𝑟1 𝑆
𝑟12 𝑆
2 12
1 12
12
(︂
2
2
3
2
3
15𝑟1 𝑟2
15𝑟1 𝑟2
15𝑟
57𝑟1
3𝑟1
33𝑟2
15𝑟
+
− 52 + 3 −
− 3
+ (𝑛12 𝑣1 )2 − 51 +
5
5
3
8𝑟12
8𝑟12
8𝑟
8𝑟12
8𝑟12
4𝑟2 𝑟12
8𝑟12
)︂ 12
16
7
16
+
− 2−
4𝑟2 𝑟12
𝑆
𝑟12 𝑆
(︂
)︂
15𝑟13
15𝑟12 𝑟2
9𝑟1
12
12
+ (𝑛12 𝑣1 )(𝑛12 𝑣2 )
− 3 + 2+
5 − 4𝑟 5
4𝑟12
4𝑟12
𝑆
𝑟12 𝑆
12
(︂
)︂
2
3𝑟
7
8
2
𝑟
8
1
2
2
+ (𝑛1 𝑣1 )
− 3 −
− 2−
3 + 4𝑟 𝑟
𝑟1 𝑟2
4𝑟12
4𝑟1 𝑟12
𝑆
𝑟1 𝑆
1 12
)︂
(︂
)︂
(︂
16
16
8
8
𝑟1
2
+
− (𝑛1 𝑣2 )
+ (𝑛1 𝑣1 )(𝑛1 𝑣2 )
3 + 𝑆2 + 𝑟 𝑆
𝑟12
𝑆2
𝑟1 𝑆
1
(︂
)︂
3𝑟12
3𝑟22
3
16
16(𝑛1 𝑣2 )(𝑛2 𝑣1 )
+ (𝑛12 𝑣1 )(𝑛1 𝑣1 ) − 4 + 4 + 2 + 2 +
𝑟
2𝑟12
2𝑟12
𝑆
𝑆2
(︂ 212
)︂
3𝑟1
3𝑟2
13
40
12(𝑛1 𝑣1 )(𝑛2 𝑣2 )
+ (𝑛12 𝑣2 )(𝑛1 𝑣1 )
− 42 + 2 − 2 −
4
𝑟
2𝑟12
2𝑟12
𝑆
𝑆2
)︂
(︂
)︂)︂
(︂ 122
4
16
−3𝑟12
3
16
3𝑟1
+
+
+
(𝑛
𝑣
)(𝑛
𝑣
)
−
+
+(𝑛12 𝑣1 )(𝑛1 𝑣2 )
12 2
1 2
4
2
4
2
2𝑟12
𝑟12
𝑆2
2𝑟12
𝑟12
𝑆2
(︂
1
9
3𝑟14
𝑟2 𝑟2
𝑟1 𝑟2
𝑟3
5𝑟1
4
𝑟3
+ 𝐺3 𝑚21 𝑚2
+ 3 + 2 − 16 +
− 1 6 + 62 − 26 + 4
3
6
𝑟1
2𝑟2
2𝑟1 𝑟2
4𝑟12
16𝑟2 𝑟12
8𝑟12
4𝑟12
16𝑟12
4𝑟12
23𝑟12
43𝑟2
5𝑟22
3
3𝑟1
𝑟2
5𝑟2
4𝑟3
3
−
+ 4 −
− 3 +
+
− 2 23 + 3 23 +
4
4
3
3
2
8𝑟2 𝑟12
8𝑟12
2𝑟1 𝑟12
𝑟12
𝑟2 𝑟12
𝑟1 𝑟12
𝑟1 𝑟12
𝑟1 𝑟12
2𝑟1 𝑟12
)︂]︂
2
𝑟2
3
15𝑟2
4𝑟22
5
5
4𝑟2
𝑟12
− 31 2 +
+
−
+
+
−
−
2
2
2
4𝑟2 𝑟12
16𝑟2 𝑟12
4𝑟12 𝑟12
𝑟13 𝑟12
𝑟12 𝑟12
𝑟1 𝑟2 𝑟12
𝑟13 𝑟12
4𝑟12 𝑟23
[︂
)︂
(︂
)︂
(︂
(︂
1
16𝑟1
8𝑟13
5𝑟1
8𝑟13
2
2
2
+ 7 𝐺 𝑚1 𝑚2 (𝑛12 𝑣12 ) (𝑛1 𝑣1 ) − 5 − 3
+ (𝑛12 𝑣12 ) (𝑛1 𝑣2 )
5 + 𝑟3
𝑐
𝑟12
𝑟12
𝑟12
12
(︂
)︂
4
2 2
2
7𝑟
7𝑟
𝑟
11𝑟
37
+ (𝑛12 𝑣12 )3 − 61 + 16 2 − 4 1 − 2
2𝑟12
2𝑟12
𝑟12
4𝑟12
(︂
)︂
2
2
20𝑟1
11
2 𝑟1
+ (𝑛12 𝑣1 )(𝑛12 𝑣12 )2
−
−
4(𝑛
𝑣
)(𝑛
𝑣
)
12
12
1
1
4
2
4
𝑟12
2𝑟12
𝑟12
2
𝑟
𝑟1
+ 4(𝑛12 𝑣12 )(𝑛1 𝑣1 )(𝑛1 𝑣2 ) 41 + (𝑛12 𝑣1 )2 (𝑛1 𝑣1 ) 3
𝑟12
𝑟12
𝑟1
𝑟1
+ 22(𝑛12 𝑣1 )(𝑛12 𝑣12 )(𝑛1 𝑣1 ) 3 − (𝑛12 𝑣1 )2 (𝑛1 𝑣2 ) 3
𝑟12
𝑟12
𝑟1
1
+ 4(𝑛12 𝑣1 )(𝑛12 𝑣12 )(𝑛1 𝑣2 ) 3 + 11(𝑛12 𝑣1 )2 (𝑛12 𝑣12 ) 2
𝑟12
2𝑟12
(︂
)︂
(︂ 3
)︂
8𝑟13
2𝑟1
8𝑟1
11𝑟1
2
2
+ (𝑛1 𝑣2 )𝑣12 − 5 − 3 + (𝑛1 𝑣1 )𝑣12
+ 3
5𝑟
3𝑟12
5𝑟5
3𝑟12
(︂ 212
)︂
(︂ 12
)︂
2
4𝑟1
5
12𝑟1
5
2
2
− (𝑛12 𝑣1 )𝑣12
+ 2 − (𝑛12 𝑣12 )𝑣1
+ 2
4
𝑟4
2𝑟12
𝑟12
2𝑟12
(︂ 12 4
)︂
2 2
2
3𝑟1
3𝑟 𝑟
7𝑟
27
2
+ (𝑛12 𝑣12 )𝑣12
− 16 2 + 41 + 2
6
2𝑟12
2𝑟12
𝑟12
4𝑟12
(︂

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 99

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

99

𝑟1
2 𝑟1
2 1
3 + (𝑛1 𝑣2 )𝑣1 𝑟 3 + 5(𝑛12 𝑣1 )𝑣1 𝑟 2
3𝑟12
12
(︂
)︂12
12𝑟12
3
𝑟1
+ (𝑛12 𝑣12 )(𝑣1 𝑣2 )
+ 2 + 8(𝑛1 𝑣1 )(𝑣1 𝑣2 ) 3
4
𝑟12
𝑟12
𝑟12
)︂
𝑟1
1
+2(𝑛1 𝑣2 )(𝑣1 𝑣2 ) 3 − 5(𝑛12 𝑣1 )(𝑣1 𝑣2 ) 2
3𝑟12
𝑟12
(︂
(︂
)︂
3
2
8𝑟1
8𝑟1 𝑟2
16𝑟1
8
8𝑟22
8
+ 𝐺3 𝑚21 𝑚2 (𝑛1 𝑣12 ) −
+
−
+
−
+
6
6
4
3
3
15𝑟12
15𝑟12
3𝑟12
𝑟12
𝑟12 𝑟12
𝑟12 𝑟12
(︂
)︂
4𝑟2
4𝑟2
20
𝑟1
+ (𝑛12 𝑣1 ) − 51 + 52 + 3 + 8(𝑛1 𝑣1 ) 4
3𝑟12
3𝑟12
3𝑟12
3𝑟12
(︂
3
4𝑟12
68𝑟22
3𝑟1
6𝑟22
3𝑟24
76
+ (𝑛12 𝑣12 )
−
+
+
−
+
5
5
4
4
4 − 3𝑟 3
𝑟13
3𝑟12
15𝑟12
𝑟12
𝑟1 𝑟12
𝑟13 𝑟12
12
)︂)︂]︂
(︂ )︂
6𝑟22
1
2
(241a)
+1↔2+𝒪 8 ,
+ 2 − 3 2
𝑟1 𝑟
𝑟1 𝑟12
𝑐
[︂ 12(︂
4𝐺𝑚1
𝐺2 𝑚1 𝑚2
1
𝐺2 𝑚2
𝑘0𝑖 = − 3 𝑣1𝑖 + 5 𝑛𝑖1 − 2 1 (𝑛1 𝑣1 ) +
(−16(𝑛12 𝑣1 ) + 12(𝑛12 𝑣2 )
𝑐 𝑟1
𝑐
𝑟1
𝑆2
)︁
−16(𝑛2 𝑣1 ) + 12(𝑛2 𝑣2 ))
(︂
𝑟1
1
1
+ 𝑛𝑖12 𝐺2 𝑚1 𝑚2 −6(𝑛12 𝑣12 ) 3 − 4(𝑛1 𝑣1 ) 2 + 12(𝑛1 𝑣1 ) 2
𝑟12
𝑟12
𝑆
(︂
)︂)︂
1 1
1
1
+
−16(𝑛1 𝑣2 ) 2 + 4(𝑛12 𝑣1 )
𝑆
𝑆 𝑆
𝑟12
(︂
)︂
(︂
2 2
(︀
)︀
𝐺 𝑚1
𝐺𝑚1
2𝑟2
3𝑟1
2
+ 𝑣1𝑖
2(𝑛1 𝑣1 )2 − 4𝑣12 +
+
𝐺
𝑚
𝑚
−
1 2
3
3
𝑟1
𝑟12
𝑟12
𝑟12
)︂)︂]︂
(︂
3
8
4
𝑟2
+𝐺2 𝑚1 𝑚2 − 23 −
+
−
𝑟1 𝑟12
𝑟1 𝑟12
𝑟2 𝑟12
𝑟12 𝑆
[︂
)︂
(︂
(︂
2
2
1
𝑟1
𝑣12
𝑖
2 𝑟1
2
2 𝑟1
+ 6 𝑛12 𝐺 𝑚1 𝑚2 −10(𝑛12 𝑣12 ) 4 − 12(𝑛12 𝑣12 )(𝑛1 𝑣1 ) 3 + 2𝑣12 4 − 4 2
𝑐
𝑟12
𝑟12
𝑟12
𝑟12
(︂ 2
)︂)︂
2
2𝑟1
2𝑟2
2
+𝐺3 𝑚21 𝑚2
5 − 3𝑟 5 − 𝑟 3
3𝑟12
12
12
(︂
)︂
2
16(𝑛
𝑣
)𝑟
𝐺
𝑚
𝑚
1
12
1
1
2
𝑖
− 4(𝑛12 𝑣2 )𝑟12
+ 𝑣1
3
𝑟12
3
(︂
)︂]︂
(︂ )︂
2
𝑟12
1
𝑖 𝐺 𝑚1 𝑚2
+𝑣12
−2(𝑛12 𝑣1 ) + 6(𝑛12 𝑣12 ) 2
+1↔2+𝒪 7 ,
(241b)
2
𝑟12
𝑟12
𝑐
[︂ (︂
2𝐺𝑚1
1
𝐺𝑚1
𝐺2 𝑚21
𝑘𝑖𝑗 = 2 𝛿 𝑖𝑗 + 4 𝛿 𝑖𝑗 −
(𝑛1 𝑣1 )2 +
𝑐 𝑟1
𝑐
𝑟1
𝑟12
(︂
)︂)︂
2
𝑟1
𝑟12
5
4
2
+𝐺 𝑚1 𝑚2
− 3 +
+
3 − 2𝑟 𝑟
𝑟1 𝑟2
2𝑟12
2𝑟2 𝑟12
𝑟12 𝑆
1 12
(︂
)︂
1
𝐺𝑚1 𝑖 𝑗 𝐺2 𝑚21 𝑖 𝑗
1
𝑗
2
𝑖
−
4𝐺
𝑚
𝑚
𝑛
𝑛
+4
𝑣1 𝑣1 +
𝑛
𝑛
+
1
2
1 1
12 12
𝑟1
𝑟12
𝑆2
𝑟12 𝑆
]︂
)︁
(︁
4𝐺2 𝑚1 𝑚2
(𝑖 𝑗)
(𝑖 𝑗)
+
𝑛1 𝑛2 + 2𝑛1 𝑛12
𝑆2
− 29(𝑛1 𝑣1 )𝑣12

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 100

100

Luc Blanchet

𝐺2 𝑚1 𝑚2
+
2
𝑐5 𝑟12

(︂

2
(𝑖 𝑗)
− (𝑛12 𝑣12 )𝛿 𝑖𝑗 − 6(𝑛12 𝑣12 )𝑛𝑖12 𝑛𝑗12 + 8𝑛12 𝑣12
3

)︂

(︂
+1↔2+𝒪

1
𝑐6

)︂
.

(241c)

Here we pose 𝑆 = 𝑟1 + 𝑟2 + 𝑟12 and 1 ↔ 2 refers to the same quantity but with all particle labels
exchanged. To higher order one needs the solution of elementary equations still more intricate
than (239) and the 3PN metric valid in closed form all over the near zone is not currently known.
Let us also display the latter 2.5PN metric computed at the location of the particle 1 for
instance, thanks to the Hadamard self-field regularization, i.e., in the sense of the Hadamard
partie finie defined by Eq. (160). We get
(︂
)︂
2𝐺𝑚2
𝐺𝑚2
𝐺𝑚1
𝐺𝑚2
2
2
(𝑘00 )1 = 2
+ 4
4𝑣2 − (𝑛12 𝑣2 ) − 3
−2
𝑐 𝑟12
𝑐 𝑟12
𝑟12
𝑟12
(︂
)︂
𝐺𝑚2 3
8𝐺2 𝑚1 𝑚2
4
2 2
4
(𝑛
𝑣
)
+
(𝑛
𝑣
)
−
3(𝑛
𝑣
)
𝑣
+
4𝑣
+
12
12
12
2
12
2
2
2
2
3𝑐5 𝑟12
𝑐6 𝑟12 4
(︂
)︂
𝐺2 𝑚1 𝑚2
87
55
47
23 2 39
2
2
+
−
(𝑛
𝑣
)
(𝑛
𝑣
)(𝑛
𝑣
)
−
(𝑛
𝑣
)
𝑣
(𝑣
𝑣
)
+
+
−
12
1
12
1
12
2
12
2
1
2
2
𝑐6 𝑟12
4
2
4
4 1
2
{︂
}︂
2 2
2
]︀
47 𝐺2 𝑚1 𝑚2 2 𝐺𝑚2 𝐺𝑚2 [︀
𝐺
𝑚
17
𝐺
𝑚
𝑚
𝐺2 𝑚22
1 2
1
2
2
+
𝑣
+
3(𝑛
𝑣
)
−
𝑣
−
+
+
2
12 2
2
2
2
2
2
2
4 𝑐6 𝑟12
𝑐6 𝑟12
𝑟12
𝑟12
2
𝑟12
𝑟12
𝐺2 𝑚1 𝑚2 {︀
+
−20(𝑛12 𝑣1 )3 + 40(𝑛12 𝑣1 )2 (𝑛12 𝑣2 ) − 36(𝑛12 𝑣1 )(𝑛12 𝑣2 )2 + 16(𝑛12 𝑣2 )3
2
𝑐7 𝑟12
116
104
232
296
(𝑛12 𝑣1 )𝑣12 −
(𝑛12 𝑣2 )𝑣12 −
(𝑛12 𝑣1 )(𝑣1 𝑣2 ) +
(𝑛12 𝑣2 )(𝑣1 𝑣2 )
+
15
15
5 (︂
15
)︂
56
52
𝐺𝑚1
104
64
+ (𝑛12 𝑣1 )𝑣22 − (𝑛12 𝑣2 )𝑣22 +
(𝑛12 𝑣2 )
− (𝑛12 𝑣1 ) +
15
5
𝑟12
5
5
)︂}︂
(︂ )︂
(︂
𝐺𝑚2
392
1
144
+
(𝑛12 𝑣1 ) +
(𝑛12 𝑣2 )
+𝒪 8 ,
−
(242a)
𝑟12
5
15
𝑐
{︂
[︂
]︂}︂
4𝐺𝑚2 𝑖
𝐺𝑚2
𝐺𝑚1
𝐺𝑚2
(𝑘0𝑖 )1 = − 3
𝑣2 + 5
𝑛𝑖12
(10(𝑛12 𝑣1 ) + 2(𝑛12 𝑣2 )) −
(𝑛12 𝑣2 )
𝑐 𝑟12
𝑐 𝑟12
𝑟12
𝑟12
{︂
(︂
)︂}︂
𝐺𝑚
𝐺𝑚2
𝐺𝑚1 𝑖
𝐺𝑚
2
1
+ 5
4
𝑣 + 𝑣2𝑖 2(𝑛12 𝑣2 )2 − 4𝑣22 − 2
+
𝑐 𝑟12
𝑟12 1
𝑟12
𝑟12
𝐺2 𝑚1 𝑚2 {︀ 𝑖 (︀
+
𝑛12 10(𝑛12 𝑣1 )2 − 8(𝑛12 𝑣1 )(𝑛12 𝑣2 ) − 2(𝑛12 𝑣2 )2 − 6𝑣12
2
𝑐6 𝑟12
)︂
8 𝐺𝑚1
4 𝐺𝑚2
+4(𝑣1 𝑣2 ) + 2𝑣22 −
+
3 𝑟12
3 𝑟12
(︂
)︂}︂
(︂ )︂
20
4
1
−8(𝑛12 𝑣1 )𝑣1𝑖 + 𝑣2𝑖
(𝑛12 𝑣1 ) + (𝑛12 𝑣2 )
+𝒪 7 ,
(242b)
3
3
𝑐
(︂
)︂
2𝐺𝑚2 𝑖𝑗 𝐺𝑚2 𝑖𝑗
𝐺𝑚1
𝐺𝑚2
(𝑘𝑖𝑗 )1 = 2
𝛿 + 4 𝛿
−(𝑛12 𝑣2 )2 +
+
𝑐 𝑟12
𝑐 𝑟12
𝑟12
𝑟12
(︂
}︂
{︂
)︂
𝐺𝑚1
4𝐺2 𝑚1 𝑚2 𝑖𝑗
𝐺𝑚2
𝐺𝑚2
+ 4
𝑛𝑖𝑗
+
+ 4𝑣2𝑖𝑗 −
𝛿 (𝑛12 𝑣12 )
12 −8
2
𝑐 𝑟12
𝑟12
𝑟12
3𝑐5 𝑟12
(︂ )︂
}︁
1
𝐺2 𝑚1 𝑚2 {︁
(𝑖 𝑗)
𝑖𝑗
𝑣
+
𝒪
+
−12𝑛
(𝑛
𝑣
)
+
16𝑛
.
(242c)
12 12 12
12 12
2
𝑐5 𝑟12
𝑐6
When regularized at the location of the particles, the metric can be computed to higher order, for
instance 3PN. We shall need it when we compute the so-called redshift observable in Sections (8.3)
and (8.4); indeed, see Eq. (276).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 101

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

8

Conservative Dynamics of Compact Binaries

8.1

Concept of innermost circular orbit

101

Having in hand the conserved energy 𝐸(𝑥) for circular orbits given by Eq. (232), or even more
accurate by (233), we define the innermost circular orbit (ICO) as the minimum, when it exists,
of the energy function 𝐸(𝑥) – see e.g., Ref. [51]. Notice that the ICO is not defined as a point of
dynamical general-relativistic unstability. Hence, we prefer to call this point the ICO rather than,
strictly speaking, an innermost stable circular orbit or ISCO. A study of the dynamical stability
of circular binary orbits in the post-Newtonian approximation is reported in Section 8.2.
The previous definition of the ICO is motivated by the comparison with some results of
numerical relativity. Indeed we shall confront the prediction of the standard (Taylor-based)
post-Newtonian approximation with numerical computations of the energy of binary black holes
under the assumptions of conformal flatness for the spatial metric and of exactly circular orbits [228, 232, 133, 121]. The latter restriction is implemented by requiring the existence of an
“helical” Killing vector (HKV), which is time-like inside the light cylinder associated with the circular motion, and space-like outside. The HKV will be defined in Eq. (273) below. In the numerical
approaches of Refs. [228, 232, 133, 121] there are no gravitational waves, the field is periodic in
time, and the gravitational potentials tend to zero at spatial infinity within a restricted model
equivalent to solving five out of the ten Einstein field equations (the so-called Isenberg–Wilson–
Mathews approximation; see Ref. [228] for a discussion). Considering an evolutionary sequence of
equilibrium configurations the circular-orbit energy 𝐸(Ω) and the ICO of binary black holes are
obtained numerically (see also Refs. [92, 229, 301] for related calculations of binary neutron stars
and strange quark stars).
Since the numerical calculations [232, 133] have been performed in the case of two corotating
black holes, which are spinning essentially with the orbital angular velocity, we must for the
comparison include within our post-Newtonian formalism the effects of spins appropriate to two
Kerr black holes rotating at the orbital rate. The total relativistic masses of the two Kerr black
holes (with a = 1, 2 labelling the black holes) are given by54
𝑚2a = 𝜇2a +

𝑆a2
.
4𝜇2a

(243)

We assume the validity of the Christodoulou mass formula for Kerr black holes [127, 129]; i.e., we
neglect the influence of the companion. Here 𝑆a is the spin, related to the usual Kerr parameter
mass, not to be confused with the reduced mass of
by 𝑆a = 𝑚a 𝑎a , and 𝜇a ≡ 𝑚irr
a is the irreducible
√
the binary system, and given by 4𝜋𝜇a = 𝐴a (𝐴a is the hole’s surface area). The angular velocity
of the black hole, defined by the angular velocity of the outgoing photons that remain for ever at
the location of the light-like horizon, is
⃒
𝜕𝑚a ⃒⃒
𝑆a
𝜔a =
=
.
(244)
𝜕𝑆a ⃒𝜇a
4𝑚a 𝜇2a
We shall give in Eq. (284) below a more general formulation of the “internal structure” of the black
holes. Combining Eqs. (243) – (244) we obtain 𝑚a and 𝑆a as functions of 𝜇a and 𝜔a ,
𝑚a = √︀

𝜇a
,
1 − 4𝜇2a 𝜔a2

(245a)

𝑆a = √︀

4𝜇3a 𝜔a
.
1 − 4𝜇2a 𝜔a2

(245b)

54 In all of Section 8 we pose 𝐺 = 1 = 𝑐.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 102

102

Luc Blanchet

In the limit of slow rotation we get
(︀ )︀
𝑆a = 𝐼a 𝜔a + 𝒪 𝜔a3 ,
(︀ )︀
1
𝑚a = 𝜇a + 𝐼a 𝜔a2 + 𝒪 𝜔a4 ,
2

(246a)
(246b)

where 𝐼a = 4𝜇3a is the moment of inertia of the black hole. We see that the total mass-energy 𝑚a
involves the irreducible mass augmented by the usual kinetic energy of the spin.
We now need the relation between the rotation frequency 𝜔a of each of the corotating black
holes and the orbital frequency Ω of the binary system. Indeed Ω is the basic variable describing each equilibrium configuration calculated numerically in Refs. [232, 133], with the irreducible
masses held constant along the numerical evolutionary sequences. Here we report the result of an
investigation of the condition for corotation based on the first law of mechanics for spinning black
holes [55], which concluded that the corotation condition at 2PN order reads
)︂
}︂
{︂
(︂
3 𝜈
2
3
𝑥 + 𝒪(𝑥 ) ,
𝜔a = Ω 1 − 𝜈 𝑥 + 𝜈 − +
2 3

(247)

where 𝑥 denotes the post-Newtonian parameter (230) and 𝜈 the symmetric mass ratio (215). The
condition (247) is issued from the general relation which will be given in Eq. (285). Interestingly,
notice that 𝜔1 = 𝜔2 up to the rather high 2PN order. In the Newtonian limit 𝑥 → 0 or the
test-particle limit 𝜈 → 0 we simply have 𝜔a = Ω, in agreement with physical intuition.
To take into account the spin effects our first task is to replace all the masses entering the
energy function (232) by their equivalent expressions in terms of 𝜔a and the irreducible masses
𝜇a , and then to replace 𝜔a in terms of Ω according to the corotation prescription (247).55 It is
clear that the leading contribution is that of the spin kinetic energy given in Eq. (246b), and it
comes from the replacement of the rest mass-energy 𝑚 = 𝑚1 + 𝑚2 . From Eq. (246b) this effect
is of order Ω2 in the case of corotating binaries, which means by comparison with Eq. (232) that
it is equivalent to an “orbital” effect at the 2PN order (i.e., ∝ 𝑥2 ). Higher-order corrections in
Eq. (246b), which behave at least like Ω4 , will correspond to the orbital 5PN order at least and
are negligible for the present purpose. In addition there will be a subdominant contribution, of the
order of Ω8/3 equivalent to 3PN order, which comes from the replacement of the masses into the
Newtonian part, proportional to 𝑥 ∝ Ω2/3 , of the energy 𝐸; see Eq. (232). With the 3PN accuracy
we do not need to replace the masses that enter into the post-Newtonian corrections in 𝐸, so in
these terms the masses can be considered to be the irreducible ones.
Our second task is to include the specific relativistic effects due to the spins, namely the spinorbit (SO) interaction and the spin-spin (SS) one. In the case of spins 𝑆1 and 𝑆2 aligned parallel
to the orbital angular momentum (and right-handed with respect to the sense of motion) the SO
energy reads
(︂
]︂
)︂
)︂
[︂(︂
4 𝑚21
4 𝑚22
𝑆1
𝑆2
𝐸SO = −𝑚 𝜈 (𝑚Ω)5/3
+
.
(248)
+
𝜈
+
𝜈
3 𝑚2
𝑚21
3 𝑚2
𝑚22
We shall review in Section 11 the most up-to-date results for the spin-orbit energy and related
quantities; here we are simply employing the leading-order formula obtained in Refs. [27, 28, 275,
271] and given by the first term in Eq. (415). We immediately infer from this formula that in the
case of corotating black holes the SO effect is equivalent to a 3PN orbital effect and thus must
be retained with the present accuracy. With this approximation, the masses in Eq. (248) can be
replaced by the irreducible ones. As for the SS interaction (still in the case of spins aligned with
55 Note that this is an iterative process because the masses in Eq. (247) are themselves to be replaced by the
irreducible masses.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 103

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

103

the orbital angular momentum) it is given by
𝐸SS = 𝜇 𝜈 (𝑚Ω)2

𝑆1 𝑆2
.
𝑚21 𝑚22

(249)

The SS effect can be neglected here because it is of order 5PN for corotating systems. Summing
up all the spin contributions to 3PN order we find that the supplementary energy due to the
corotating spins is [51, 55]56
[︁
]︁
Δ𝐸 corot = 𝜇𝑥𝜇 (2 − 6𝜂) 𝑥2𝜇 + 𝜂 (−10 + 25𝜂) 𝑥3𝜇 + 𝒪(𝑥4𝜇 ) .
(250)
The total mass 𝜇 = 𝜇1 + 𝜇2 , the symmetric mass ratio 𝜂 = 𝜇1 𝜇2 /𝜇2 , and the dimensionless
invariant post-Newtonian parameter 𝑥𝜇 = (𝜇Ω)2/3 are now expressed in terms of the irreducible
masses 𝜇a , rather than the masses 𝑚a . The complete 3PN energy of the corotating binary is finally
given by the sum of Eqs. (232) and (250), in which all the masses are now understood as being
the irreducible ones, which must be assumed to stay constant when the binary evolves for the
comparison with the numerical calculation.
The left panel of Figure 1 shows the results for 𝐸ICO in the case of irrotational and corotational
binaries. Since Δ𝐸 corot , given by Eq. (250), is at least of order 2PN, the result for 1PNcorot is
the same as for 1PN in the irrotational case; then, obviously, 2PNcorot takes into account only
the leading 2PN corotation effect, i.e., the spin kinetic energy given by Eq. (246b), while 3PNcorot
involves also, in particular, the corotational SO coupling at the 3PN order. In addition we present
the numerical point obtained by numerical relativity under the assumptions of conformal flatness
and of helical symmetry [228, 232]. As we can see the 3PN points, and even the 2PN ones, are in
good agreement with the numerical value. The fact that the 2PN and 3PN values are so close to
each other is a good sign of the convergence of the expansion. In fact one might say that the role
of the 3PN approximation is merely to “confirm” the value already given by the 2PN one (but of
course, had we not computed the 3PN term, we would not be able to trust very much the 2PN
value). As expected, the best agreement we obtain is for the 3PN approximation and in the case of
corotation, i.e., the point 3PNcorot . However, the 1PN approximation is clearly not precise enough,
but this is not surprising in the highly relativistic regime of the ICO. The right panel of Figure 1
shows other very interesting comparisons with numerical relativity computations [133, 121], done
not only for the case of corotational binaries but also in the irrotational (non-spinning) case.
Witness in particular the almost perfect agreement between the standard 3PN point (PN standard,
shown with a green triangle) and the numerical quasi-equilibrium point (QE, red triangle) in the
case of irrotational non-spinning (NS) binaries.
However, we recall that the numerical works [228, 232, 133, 121] assume that the spatial metric
is conformally flat, which is incompatible with the post-Newtonian approximation starting from the
2PN order (see [196] for a discussion). Nevertheless, the agreement found in Figure 1 constitutes
an appreciable improvement of the previous situation, because the first estimations of the ICO in
post-Newtonian theory [274] and numerical relativity [132, 342, 29] disagreed with each other, and
do not match with the present 3PN results.

8.2

Dynamical stability of circular orbits

In this section, following Ref. [79], we shall investigate the problem of the stability, against dynamical perturbations, of circular orbits at the 3PN order. We propose to use two different methods,
one based on a linear perturbation at the level of the center-of-mass equations of motion (219) –
(220) in (standard) harmonic coordinates, the other one consisting of perturbing the Hamiltonian
56 In Ref. [51] it was assumed that the corotation condition was given by the leading-order result 𝜔 = Ω. The
a
1PN correction in Eq. (247) modifies the 3PN terms in Eq. (250) with respect to the result of Ref. [51].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 104

104

Luc Blanchet

NS: QE
LN: QE
NS: IVP conf
NS: PN EOB
NS: PN standard
CO: QE
CO: HKV-GGB
CO: PN EOB
CO: PN standard

-0.014

EICO / M

-0.016

-0.018

-0.020

-0.022
0.08

0.12

0.16

MΩICO
Figure 1: The binding energy 𝐸ICO versus ΩICO in the equal-mass case (𝜈 = 1/4). Left panel: Comparison
with the numerical relativity result of Gourgoulhon, Grandclément et al. [228, 232] valid in the corotating
case (marked by a star). Points indicated by 𝑛PN are computed from the minimum of Eq. (232), and
correspond to irrotational binaries. Points denoted by 𝑛PNcorot come from the minimum of the sum of
Eqs. (232) and (250), and describe corotational binaries. Note the very good convergence of the standard
(Taylor-expanded) PN series. Right panel: Numerical relativity results of Cook, Pfeiffer et al. [133, 121]
for quasi-equilibrium (QE) configurations and various boundary conditions for the lapse function, in the
non-spinning (NS), leading-order non spinning (LN) and corotating (CO) cases. The point from [228, 232]
(HKV-GGB) is also reported as in the left panel, together with IVP, the initial value approach with
effective potential [132, 342], as well as standard PN predictions from the left panel and non-standard
(EOB) ones. The agreement between the QE computation and the standard non-resummed 3PN point is
excellent especially in the irrotational NS case.

equations in ADM coordinates for the center-of-mass Hamiltonian (223). We shall find a criterion
for the stability of circular orbits and shall present it in an invariant way – the same in different
coordinate systems. We shall check that our two methods agree on the result.
We deal first with the perturbation of the equations of motion, following Kidder, Will & Wiseman [275] (see their Section III.A). We introduce polar coordinates (𝑟, 𝜙) in the orbital plane and
pose 𝑢 ≡ 𝑟˙ and Ω ≡ ˙
𝜙. Then Eq. (219) yields the system of equations
𝑟˙ = 𝑢 ,
]︁
𝐺𝑚 [︁
𝑢˙ = − 2 1 + 𝒜 + ℬ𝑢 + 𝑟Ω2 ,
𝑟[︂
]︂
𝐺𝑚
2𝑢
,
Ω̇ = −Ω
ℬ
+
𝑟2
𝑟

(251a)
(251b)
(251c)

where 𝒜 and ℬ are given by Eqs. (220) as functions of 𝑟, 𝑢 and Ω (through 𝑣 2 = 𝑢2 + 𝑟2 Ω2 ).
In the case of an orbit that is circular apart from the adiabatic inspiral at the 2.5PN order
(we neglect the radiation-reaction damping effects), we have 𝑟˙0 = 𝑢˙ 0 = Ω̇0 = 0 hence 𝑢0 = 0. In
this section we shall indicate quantities associated with the circular orbit, which constitutes the
zero-th approximation in our perturbation scheme, using the subscript 0. Hence Eq. (251b) gives

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 105

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

105

the angular velocity Ω0 of the circular orbit as
Ω20 =

)︀
𝐺𝑚 (︀
1 + 𝒜0 .
3
𝑟0

(252)

Solving iteratively this relation at the 3PN order using the equations of motion (219) – (220), we
obtain Ω0 as a function of the circular-orbit radius 𝑟0 in standard harmonic coordinates; the result
agrees with Eq. (228).57
We now investigate the linear perturbation around the circular orbit defined by the constants
𝑟0 , 𝑢0 = 0 and Ω0 . We pose
𝑟 = 𝑟0 + 𝛿𝑟 ,
𝑢 = 𝛿𝑢 ,
Ω = Ω0 + 𝛿Ω ,

(253a)
(253b)
(253c)

where 𝛿𝑟, 𝛿𝑢 and 𝛿Ω denote the linear perturbations of the circular orbit. Then a system of linear
equations readily follows:
˙ = 𝛿𝑢 ,
𝛿𝑟
˙ = 𝛼0 𝛿𝑟 + 𝛽0 𝛿Ω ,
𝛿𝑢

(254b)

˙ = 𝛾0 𝛿𝑢 ,
𝛿Ω

(254c)

(254a)

where the coefficients, which solely depend on the unperturbed circular orbit (hence the added
subscript 0), read as [275]
(︂
)︂
𝐺𝑚 𝜕𝒜
2
,
(255a)
𝛼0 = 3Ω0 − 2
𝑟0
𝜕𝑟 0
(︂
)︂
𝐺𝑚 𝜕𝒜
𝛽0 = 2𝑟0 Ω0 − 2
,
(255b)
𝑟0
𝜕Ω 0
(︂
)︂ ]︂
[︂
2
𝐺𝑚 𝜕ℬ
𝛾0 = −Ω0
.
(255c)
+ 2
𝑟0
𝑟0
𝜕𝑢 0
In obtaining these equations we use the fact that 𝒜 is a function of the square 𝑢2 through
𝑣 2 = 𝑢2 + 𝑟2 Ω2 , so that 𝜕𝒜/𝜕𝑢 is proportional to 𝑢 and thus vanishes in the unperturbed configuration (because 𝑢 = 𝛿𝑢). On the other hand, since the radiation reaction is neglected, ℬ is also
proportional to 𝑢 [see Eq. (220b)], so only 𝜕ℬ/𝜕𝑢 can contribute at the zero-th perturbative order.
Now by examining the fate of perturbations that are proportional to some 𝑒𝑖𝜎𝑡 , we arrive at the
condition for the frequency 𝜎 of the perturbation to be real, and hence for stable circular orbits to
exist, as being [275]
𝐶^0 ≡ −𝛼0 − 𝛽0 𝛾0 > 0 .
(256)
Substituting into this 𝒜 and ℬ at the 3PN order we then arrive at the orbital-stability criterion
{︃
)︂
)︁ 𝐺2 𝑚2 (︂
𝐺𝑚 (︁
65
𝐺𝑚
2
^
−
9
+
𝜈
+
30
+
𝜈
+
𝜈
(257)
𝐶0 = 3 1 +
𝑟0
𝑟0 𝑐2
𝑟02 𝑐4
4
(︂
[︂
)︂
(︂ )︂ }︃
(︁ 𝑟 )︁]︂
19 2
𝐺3 𝑚3
29927 451 2
1
0
3
𝜈+ 𝜈 +𝜈 +𝒪 8
+ 3 6 −70 + −
−
𝜋 + 22 ln ′
,
𝑟0 𝑐
840
64
𝑟0
2
𝑐
57 One should not confuse the circular-orbit radius 𝑟 with the constant 𝑟 ′ entering the logarithm at the 3PN
0
0
order in Eq. (228) and which is defined by Eq. (221).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 106

106

Luc Blanchet

where we recall that 𝑟0 is the radius of the orbit in harmonic coordinates.
Our second method is to use the Hamiltonian equations associated with the 3PN center-of-mass
Hamiltonian in ADM coordinates 𝐻 ADM given by Eq. (223). We introduce the polar coordinates
(𝑅, Ψ) in the orbital plane – we assume that the orbital plane is equatorial, given by Θ = 𝜋2 in the
spherical coordinate system (𝑅, Θ, Ψ) – and make the substitution
𝑃 2 = 𝑃𝑅 2 +

𝑃Ψ2
.
𝑅2

(258)

This yields a reduced Hamiltonian that is a function of 𝑅, 𝑃𝑅 and 𝑃Ψ , and describes the motion in
polar coordinates in the orbital plane; henceforth we denote it by ℋ = ℋ[𝑅, 𝑃𝑅 , 𝑃Ψ ] ≡ 𝐻 ADM /𝜇.
The Hamiltonian equations then read
d𝑅
𝜕ℋ
=
,
d𝑡
𝜕𝑃𝑅
dΨ
𝜕ℋ
=
,
d𝑡
𝜕𝑃Ψ
𝜕ℋ
d𝑃𝑅
=−
,
d𝑡
𝜕𝑅
d𝑃Ψ
= 0.
d𝑡

(259a)
(259b)
(259c)
(259d)

Evidently the constant 𝑃Ψ is nothing but the conserved angular-momentum integral. For circular
orbits we have 𝑅 = 𝑅0 (a constant) and 𝑃𝑅 = 0, so
]︀
𝜕ℋ [︀
𝑅0 , 0, 𝑃Ψ0 = 0 ,
𝜕𝑅
which gives the angular momentum 𝑃Ψ0 of the circular orbit as a function of 𝑅0 , and
(︂
)︂
]︀
dΨ
𝜕ℋ [︀
=
𝑅0 , 0, 𝑃Ψ0 ,
Ω0 ≡
d𝑡 0
𝜕𝑃Ψ

(260)

(261)

which yields the angular frequency of the circular orbit Ω0 , which is evidently the same numerical
quantity as in Eq. (252), but is here expressed in terms of the separation 𝑅0 in ADM coordinates.
The last equation, which is equivalent to 𝑅 = const = 𝑅0 , is
]︀
𝜕ℋ [︀
𝑅0 , 0, 𝑃Ψ0 = 0 .
𝜕𝑃𝑅

(262)

It is automatically verified because ℋ is a quadratic function of 𝑃𝑅 and hence 𝜕ℋ/𝜕𝑃𝑅 is zero for
circular orbits.
We consider now a perturbation of the circular orbit defined by
𝑃𝑅 = 𝛿𝑃𝑅 ,

(263a)

𝑃Ψ = 𝑃Ψ0 + 𝛿𝑃Ψ ,

(263b)
(263c)
(263d)

𝑅 = 𝑅0 + 𝛿𝑅 ,
Ω = Ω0 + 𝛿Ω .
The Hamiltonian equations (259), worked out at the linearized order, read as
𝛿𝑃˙ 𝑅 = −𝜋0 𝛿𝑅 − 𝜌0 𝛿𝑃Ψ ,

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(264a)

## PDF page 107

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

107

𝛿𝑃˙ Ψ = 0 ,
˙ = 𝜎0 𝛿𝑃𝑅 ,
𝛿𝑅

(264b)
(264c)
(264d)

𝛿Ω = 𝜌0 𝛿𝑅 + 𝜏0 𝛿𝑃Ψ ,
where the coefficients, which depend on the unperturbed orbit, are given by
]︀
𝜕 2 ℋ [︀
𝑅0 , 0, 𝑃Ψ0 ,
2
𝜕𝑅
]︀
𝜕 2 ℋ [︀
𝜌0 =
𝑅0 , 0, 𝑃Ψ0 ,
𝜕𝑅 𝜕𝑃Ψ
]︀
𝜕 2 ℋ [︀
0
𝜎0 =
2 𝑅0 , 0, 𝑃Ψ ,
𝜕𝑃𝑅
]︀
𝜕 2 ℋ [︀
0
𝜏0 =
2 𝑅0 , 0, 𝑃Ψ .
𝜕𝑃Ψ

(265a)

𝜋0 =

(265b)
(265c)
(265d)

By looking to solutions proportional to some 𝑒𝑖𝜎𝑡 one obtains some real frequencies, and therefore
one finds stable circular orbits, if and only if
𝐶^0 ≡ 𝜋0 𝜎0 > 0 .

(266)

Using explicitly the Hamiltonian (223) we readily obtain
{︃
(︂
)︂
𝐺𝑚
𝐺2 𝑚2 117 43
𝐺𝑚
2
^
(−9 + 𝜈) + 2 4
+ 𝜈+𝜈
𝐶0 = 3 1 +
𝑅0
𝑅0 𝑐2
𝑅0 𝑐
4
8
(︂
[︂
]︂
)︂
(︂ )︂ }︃
𝐺3 𝑚3
4777 325 2
31 2
1
3
+ 3 6 −61 +
−
𝜋 𝜈− 𝜈 +𝜈 +𝒪 8
.
𝑅0 𝑐
48
64
8
𝑐

(267)

This result does not look the same as our previous result (257), but this is simply due to the fact
that it depends on the ADM radial separation 𝑅0 instead of the harmonic one 𝑟0 . Fortunately
we have derived in Section 7.2 the material needed to connect 𝑅0 to 𝑟0 with the 3PN accuracy.
Indeed, with Eqs. (210) we have the relation valid for general orbits in an arbitrary frame between
the separation vectors in both coordinate systems. Specializing that relation to circular orbits we
find
{︃
]︂
(︂
)︂
(︂[︂
)︂
(︂ )︂ }︃
𝐺2 𝑚2
1 29
𝐺3 𝑚3
3163 21 2 22 (︁ 𝑟0 )︁
3 2
1
𝑅0 = 𝑟0 1 + 2 4 − − 𝜈 + 3 6
+ 𝜋 −
ln ′
𝜈+ 𝜈 +𝒪 8
.
𝑟0 𝑐
4
8
𝑟0 𝑐
1680 32
3
𝑟0
8
𝑐
(268)
Note that the difference between 𝑅0 and 𝑟0 starts only at 2PN order. That relation easily permits
to perfectly reconcile both expressions (257) and (267).
Finally let us give to 𝐶^0 an invariant meaning by expressing it with the help of the orbital
frequency Ω0 of the circular orbit, or, more conveniently, of the frequency-related parameter 𝑥0 ≡
(𝐺𝑚 Ω0 /𝑐3 )2/3 – cf. Eq. (230). This allows us to write the criterion for stability as 𝐶0 > 0, where
2
2
𝐶0 = 𝐺𝑥𝑚
𝐶^0 admits the gauge-invariant form
3
0

𝐶0 = 1 − 6 𝑥0 + 14 𝜈 𝑥20 +

(︂[︂

]︂
)︂
(︀ )︀
397 123 2
2
−
𝜋 𝜈 − 14𝜈
𝑥30 + 𝒪 𝑥40 .
2
16

(269)

This form is more interesting than the coordinate-dependent expressions (257) or (267), not only because of its invariant form, but also because as we see the 1PN term yields exactly the Schwarzschild

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 108

108

Luc Blanchet

result that the innermost stable circular orbit or ISCO of a test particle (i.e., in the limit 𝜈 → 0)
is located at 𝑥ISCO = 16 . Thus we find that, at the 1PN order, but for any mass ratio 𝜈,
𝑥1PN
ISCO =

1
.
6

(270)

One could have expected that some deviations of the order of 𝜈 already occur at the 1PN order, but it turns out that only from the 2PN order does one find the occurrence of some nonSchwarzschildean corrections proportional to 𝜈. At the 2PN order we obtain
(︃
)︃
√︂
14𝜈
3
2PN
1− 1−
.
(271)
𝑥ISCO =
14𝜈
9
For equal masses this gives 𝑥2PN
ISCO ≃ 0.187. Notice also that the effect of the finite mass corrections
is to increase the frequency of the ISCO with respect to the Schwarzschild result, i.e., to make it
more inward :58
[︂
]︂
7
1
2
𝜈
+
𝒪(𝜈
)
1
+
.
(272)
𝑥2PN
=
ISCO
6
18
Finally, at the 3PN order, for equal masses 𝜈 = 41 , we find that according to our criterion all the
circular orbits are stable. More generally, we find that at the 3PN order all orbits are stable when
the mass ratio 𝜈 is larger than some critical value 𝜈𝑐 ≃ 0.183.
The stability criterion (269) has been compared in great details to various other stability criteria
by Favata [191] and shown to perform very well, and has also been generalized to spinning black
hole binaries in Ref. [190]. Note that this criterion is based on the physical requirement that
a stable perturbation should have a real frequency. It gives an innermost stable circular orbit,
when it exists, which differs from the innermost circular orbit or ICO defined in Section 8.1; see
Ref. [378] for a discussion on the difference between an ISCO and the ICO in the PN context. Note
also that the criterion (269) is based on systematic post-Newtonian expansions, without resorting
for instance to Padé approximants. Nevertheless, it performs better than other criteria based on
various resummation techniques, as discussed in Ref. [191].

8.3

The first law of binary point-particle mechanics

In this section we shall review a very interesting relation for binary systems of point particles
modelling black hole binaries and moving on circular orbits, known as the “first law of pointparticle mechanics”. This law was obtained using post-Newtonian methods in Ref. [289], but is
actually a particular case of a more general law, valid for systems of black holes and extended fluid
balls, derived by Friedman, Uryū & Shibata [208].
Before tackling the problem it is necessary to make more precise the notion of circular orbits. These are obtained from the conservative part of the dynamics, neglecting the dissipative
radiation-reaction force responsible for the gravitational-wave inspiral. In post-Newtonian theory
this means neglecting the radiation-reaction force at 2.5PN and 3.5PN orders, i.e., considering
only the conservative dynamics at the even-parity 1PN, 2PN and 3PN orders. We have seen in
Sections 5.2 and 5.4 that this clean separation between conservative even-parity and dissipative
odd-parity terms breaks at 4PN order, because of a contribution originating from gravitationalwave tails in the radiation-reaction force. We expect that at any higher order 4PN, 4.5PN, 5PN,
etc. there will be a mixture of conservative and dissipative effects; here we assume that at any
higher order we can neglect the radiation-reaction dissipation effects.
58 This tendency is in agreement with numerical and analytical self-force calculations [24, 287].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 109

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

109

Consider a system of two compact objects moving on circular orbits. We examine first the case
of non-spinning objects. With exactly circular orbits the geometry admits a helical Killing vector
(HKV) field 𝐾 𝛼 , satisfying the Killing equation ∇𝛼 𝐾 𝛽 + ∇𝛽 𝐾 𝛼 = 0. Imposing the existence of
the HKV is the rigorous way to implement the notion of circular orbits. A Killing vector is only
defined up to an overall constant factor. The helical Killing vector 𝐾 𝛼 extends out to a large
distance where the geometry is essentially flat. There,
𝐾 𝛼 𝜕𝛼 = 𝜕𝑡 + Ω 𝜕𝜙 ,

(273)

in any natural coordinate system which respects the helical symmetry [370]. We let this equality
define the overall constant factor, thereby specifying the Killing vector field uniquely. In Eq. (273)
Ω denotes the angular frequency of the binary’s circular motion.
An observer moving with one of the particles (say the particle 1), while orbiting around the
other particle, would detect no change in the local geometry. Thus the four-velocity 𝑢𝛼
1 of that
particle is tangent to the Killing vector 𝐾 𝛼 evaluated at the location of the particle, which we
denote by 𝐾1𝛼 . A physical quantity is then defined as the constant of proportionality 𝑢𝑇1 between
these two vectors, namely
𝑇
𝛼
𝑢𝛼
(274)
1 = 𝑢1 𝐾1 .
The four-velocity of the particle is normalized by (𝑔𝜇𝜈 )1 𝑢𝜇1 𝑢𝜈1 = −1, where (𝑔𝜇𝜈 )1 denotes the
metric at the location of the particle. For a self-gravitating compact binary system, the metric at
point 1 is generated by the two particles and has to be regularized according to one of the self-field
regularizations discussed in Section 6. It will in fact be sometimes more convenient to work with
the inverse of 𝑢𝑇1 , denoted 𝑧1 ≡ 1/𝑢𝑇1 . From Eq. (274) we get
𝑧1 = −(𝑢1 𝐾1 ) ,

(275)

where (𝑢1 𝐾1 ) = (𝑔𝜇𝜈 )1 𝑢𝜇1 𝐾1𝜈 denotes the usual space-time dot product. Thus we can regard 𝑧1
as the Killing energy of the particle that is associated with the HKV field 𝐾 𝛼 . The quantity
𝑧1 represents also the redshift of light rays emitted from the particle and received on the helical
symmetry axis perpendicular to the orbital plane at large distances from it [176]. In the following
we shall refer to 𝑧1 as the redshift observable.
If we choose a coordinate system such that Eq. (273) is satisfied everywhere, then in particular
𝐾1𝑡 = 1, thus 𝑢𝑇1 simply agrees with 𝑢𝑡1 , the 𝑡-component of the four-velocity of the particle. The
𝑡
Killing vector on the particle is then 𝐾1𝛼 = 𝑢𝛼
1 /𝑢1 , and simply reduces to the particle’s ordinary
𝛼
𝛼
𝛼
𝛼
coordinate velocity: 𝐾1 = 𝑣1 /𝑐 where 𝑣1 = d𝑦1 /d𝑡 and 𝑦1𝛼 (𝑡) = [𝑐𝑡, 𝑦1 (𝑡)] denotes the particle’s
trajectory in that coordinate system. The redshift observable we are thus considering is
√︁
1
(276)
𝑧1 = 𝑇 = −(𝑔𝜇𝜈 )1 𝑣1𝜇 𝑣1𝜈 /𝑐2 .
𝑢1
It is important to note that for circular orbits this quantity does not depend upon the choice
of coordinates; in a perturbative approach in which the perturbative parameter is the particles’
mass ratio 𝜈 ≪ 1, it does not depend upon the choice of perturbative gauge with respect to the
background metric. We shall be interested in the invariant scalar function 𝑧1 (Ω), where Ω is the
angular frequency of the circular orbit introduced when imposing Eq. (273).
We have obtained in Section 7.4 the expressions of the post-Newtonian binding energy 𝐸 and
angular momentum J for point-particle binaries on circular orbits. We shall now show that there
are some differential and algebraic relations linking 𝐸 and J to the redshift observables 𝑧1 and 𝑧2
associated with the two individual particles. Here we prefer to introduce instead of 𝐸 the total
relativistic (ADM) mass of the binary system
M=𝑚+

𝐸
,
𝑐2

(277)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 110

110

Luc Blanchet

where 𝑚 is the sum of the two post-Newtonian individual masses 𝑚1 and 𝑚2 – those which have
been used up to now, for instance in Eq. (203). Note that in the spinning case such post-Newtonian
masses acquire some spin contributions given, e.g., by Eqs. (243) – (246).
For point particles without spins, the ADM mass M, angular momentum J, and redshifts 𝑧a ,
are functions of three independent variables, namely the orbital frequency Ω that is imposed by
the existence of the HKV, and the individual masses 𝑚a . For spinning point particles, we have
also the two spins 𝑆a which are necessarily aligned with the orbital angular momentum. We first
recover that the ADM quantities obey the “thermodynamical” relation already met in Eq. (235),
𝜕J
𝜕M
=Ω
.
𝜕Ω
𝜕Ω

(278)

Such relation is commonly used in post-Newtonian theory (see e.g., [160, 51]). It states that
the gravitational-wave energy and angular momentum fluxes are strictly proportional for circular
orbits, with Ω being the coefficient of proportionality. This relation is used in computations of the
binary evolution based on a sequence of quasi-equilibrium configurations [228, 232, 133, 121], as
discussed in Section 8.1.
The first law will be a thermodynamical generalization of Eq. (278), describing the changes
in the ADM quantities not only when the orbital frequency Ω varies with fixed masses, but also
when the individual masses 𝑚a of the particles vary with fixed orbital frequency. That is, one
compares together different conservative dynamics with different masses but the same frequency.
This situation is answered by the differential equations
𝜕J
𝜕M
−Ω
= 𝑧a
𝜕𝑚a
𝜕𝑚a

(a = 1, 2) .

(279)

Finally the three relations (278) – (279) can be summarized in the following result.
Theorem 11. The changes in the ADM mass and angular momentum of a binary system made of
point particles in response to infinitesimal variations of the individual masses of the point particles,
are related together by the first law of binary point-particle mechanics as [208, 289]
∑︁
𝛿M − Ω 𝛿J =
𝑧a 𝛿𝑚a .
(280)
a

This law was proved in a very general way in Ref. [208] for systems of black holes and extended
bodies under some arbitrary Killing symmetry. The particular form given in Eq. (280) is a specialization to the case of point particle binaries with helical Killing symmetry. It has been proved
directly in this form in Ref. [289] up to high post-Newtonian order, namely 3PN order plus the
logarithmic contributions occurring at 4PN and 5PN orders.
The first law of binary point-particle mechanics (280) is of course reminiscent of the celebrated
𝜅
𝛿𝐴, which holds for any non-singular, asymptotfirst law of black hole mechanics 𝛿M − 𝜔H 𝛿J = 8𝜋
ically flat perturbation of a stationary and axisymmetric black hole of mass M, intrinsic angular
momentum (or spin) J ≡ M𝑎, surface area 𝐴, uniform surface gravity 𝜅, and angular frequency 𝜔H
on the horizon [26, 417]; see Ref. [289] for a discussion.
An interesting by-product of the first law (280) is the remarkably simple algebraic relation
∑︁
M − 2ΩJ =
𝑧a 𝑚a ,
(281)
a

which can be seen as a first integral of the differential relation (280). Note that the existence
of such a simple algebraic relation between the local quantities 𝑧1 and 𝑧2 on one hand, and the
globally defined quantities M and J on the other hand, is not trivial.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 111

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

111

Next, we report the result of a generalization of the first law applicable to systems of point
particles with spins (moving on circular orbits).59 This result is valid through linear order in the
spin of each particle, but holds also for the quadratic coupling between different spins (interaction
spin terms 𝑆1 × 𝑆2 in the language of Section 11). To be consistent with the HKV symmetry, we
must assume that the two spins 𝑆a are aligned or anti-aligned with the orbital angular momentum.
We introduce the total (ADM-like)
angular momentum J which is related to the orbital angular
∑︀
momentum 𝐿 by J = 𝐿 + a 𝑆a for aligned or anti-aligned spins. The first law now becomes [55]
]︁
∑︁[︁
(︀
)︀
𝛿M − Ω 𝛿J =
𝑧a 𝛿𝑚a + Ωa − Ω 𝛿𝑆a ,
(282)
a

where Ωa = |Ωa | denotes the precession frequency of the spins. This law has been derived in
Ref. [55] from the canonical Hamiltonian formalism. The spin variables used here are the canonical
spins 𝑆a , that are easily seen to obey, from the algebra satisfied by the canonical variables, the
usual Newtonian-looking precession equations d𝑆a /d𝑡 = Ωa × 𝑆a . These variables are identical
to the “constant-in-magnitude” spins which will be defined and extensively used in Section 11.
Similarly, to Eq. (281) we have also a first integral associated with the variational law (282):
]︁
∑︁[︁
M − 2ΩJ =
𝑧a 𝑚a − 2(Ω − Ωa )𝑆a .
(283)
a

Notice that the relation (282) has been derived for point particles and arbitrary aligned spins.
We would like now to derive the analogous relation for binary black holes. The key difference
is that black holes are extended finite-size objects while point particles have by definition no
spatial extension. For point particle binaries the spins can have arbitrary magnitude and still be
compatible with the HKV. In this case the law (282) would describe also (super-extremal) naked
singularities. For black hole binaries the HKV constraints the rotational state of each black hole
and the binary system must be corotating.
Let us derive, in a heuristic way, the analogue of the first law (282) for black holes by introducing
some “constitutive relations” 𝑚a (𝜇a , 𝑆a , · · · ) specifying the energy content of the bodies, i.e., the
relations linking their masses 𝑚a to the spins 𝑆a and to some irreducible masses 𝜇a . More precisely,
we define for each spinning particle the analogue of an irreducible mass 𝜇a ≡ 𝑚irr
a via the variational
relation 𝛿𝑚a = 𝑐a 𝛿𝜇a + 𝜔a 𝛿𝑆a ,60 in which the “response coefficient” 𝑐a of the body and its proper
rotation frequency 𝜔a are associated with the internal structure:
⃒
𝜕𝑚a ⃒⃒
,
(284a)
𝑐a ≡
𝜕𝜇a ⃒𝑆a
⃒
𝜕𝑚a ⃒⃒
.
(284b)
𝜔a ≡
𝜕𝑆a ⃒𝜇a
For instance, using the Christodoulou mass formula (243) for Kerr black holes, we obtain the
rotation frequency 𝜔a given by Eq. (244). On the other hand, the response coefficient 𝑐a differs
from 1 only because of spin effects, and we can check that 𝑐a = 1 + 𝒪(𝑆a2 ).
Within the latter heuristic model a condition for the corotation of black hole binaries has been
proposed in Ref. [55] as
𝑧a 𝜔a + Ωa = Ω .
(285)
This condition determines the value of the proper frequency 𝜔a of each black hole appropriate
to the corotation state. When expanded to 2PN order the condition (285) leads to Eq. (247)
59 The first law (280) has also been generalized for binary systems of point masses moving along generic stable
bound (eccentric) orbits in Ref. [286].
60 In the case of extended material bodies, 𝜇 would represent the baryonic mass of the bodies.
a

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 112

112

Luc Blanchet

that we have already used in Section 8.1. With Eq. (285) imposed, the first law (282) simplifies
considerably:
∑︁
𝛿M − Ω 𝛿J =
𝑐a 𝑧a 𝛿𝜇a .
(286)
a

This is almost identical to the first law for non-spinning binaries given by Eq. (280); indeed it
simply differs from it by the substitutions 𝑐a → 1 and 𝜇a → 𝑚a . Since the irreducible mass 𝜇a of
a rotating black hole is the spin-independent part of its total mass 𝑚a , this observation suggests
that corotating binaries are very similar to non-spinning binaries, at least from the perspective of
the first law. Finally we can easily reconcile the first law (286) for corotating systems with the
known first law of binary black hole mechanics [208], namely
𝛿M − Ω 𝛿J =

∑︁ 𝜅a
a

8𝜋

𝛿𝐴a .

(287)

Indeed it suffices to make the formal identification in Eq. (286) of 𝑐a 𝑧a with 4𝜇a 𝜅a , where 𝜅a denotes
the constant surface gravity, and using the surface areas 𝐴a = 16𝜋𝜇2a instead of the irreducible
masses of the black holes. This shows that the heuristic model based on the constitutive relations
(284) is able to capture the physics of corotating black hole binary systems.

8.4

Post-Newtonian approximation versus gravitational self-force

The high-accuracy predictions from general relativity we have drawn up to now are well suited
to describe the inspiralling phase of compact binaries, when the post-Newtonian parameter (1) is
small independently of the mass ratio 𝑞 ≡ 𝑚1 /𝑚2 between the compact bodies. In this section
we investigate how well does the post-Newtonian expansion compare with another very important approximation scheme in general relativity: The gravitational self-force approach, based on
black-hole perturbation theory, which gives an accurate description of extreme mass ratio binaries
having 𝑞 ≪ 1 or equivalently 𝜈 ≪ 1, even in the strong field regime. The gravitational self-force
analysis [317, 360, 178, 231] (see [348, 177, 23] for reviews) is thus expected to provide templates
for extreme mass ratio inspirals (EMRI) anticipated to be present in the bandwidth of space-based
detectors.
Consider a system of two (non-spinning) compact objects with 𝑞 = 𝑚1 /𝑚2 ≪ 1; we shall call
the smaller mass 𝑚1 the “particle”, and the larger mass 𝑚2 the “black hole”. The orbit of the
particle around the black hole is supposed to be exactly circular as we neglect the radiation-reaction
effects. With circular orbits and no dissipation, we are considering the conservative part of the
dynamics, and the geometry admits the HKV field (273). Note that in self-force theory there is
a clean split between the dissipative and conservative parts of the dynamics (see e.g., [22]). This
split is particularly transparent for an exact circular orbit, since the radial component (along 𝑟) is
the only non-vanishing component of the conservative self-force, while the dissipative part of the
self-force are the components along 𝑡 and 𝜙.
The problem of the comparison between the post-Newtonian and perturbative self-force analyses
in their common domain of validity, that of the slow-motion and weak-field regime of an extreme
mass ratio binary, is illustrated in Figure 2. This problem has been tackled by Detweiler [176], who
computed numerically within the self-force (SF) approach the redshift observable 𝑢𝑇1 associated
with the particle, and compared it with the 2PN prediction extracted from existing post-Newtonian
results [76]. This comparison proved to be successful, and was later systematically implemented and
extended to higher post-Newtonian orders in Refs. [68, 67]. In this section we review the works [68,
67] which have demonstrated an excellent agreement between the analytical post-Newtonian result
derived through 3PN order, with inclusion of specific logarithmic terms at 4PN and 5PN orders,
and the exact numerical SF result.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 113

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

113

log10("12 /!)
4

3

Post-Newtonian
Theory

Post-Newtonian
Theory
&
Perturbation
Theory

Numerical
Relativity

Perturbation
Theory

2

1

0
0

1

2

3

4

log10(!2 /!1)

Figure 2: Different analytical approximation schemes and numerical techniques to study black hole
binaries, depending on the mass ratio 𝑞 = 𝑚1 /𝑚2 and the post-Newtonian parameter 𝜖2 ∼ 𝑣 2 /𝑐2 ∼
𝐺𝑚/(𝑐2 𝑟12 ). Post-Newtonian theory and perturbative self-force analysis can be compared in the postNewtonian regime (𝜖 ≪ 1 thus 𝑟12 ≫ 𝐺𝑚/𝑐2 ) of an extreme mass ratio (𝑚1 ≪ 𝑚2 ) binary.

For the PN-SF comparison, we require two physical quantities which are precisely defined in
the context of each of the approximation schemes. The orbital frequency Ω of the circular orbit as
measured by a distant observer is one such quantity and has been introduced in Eq. (273); the second quantity is the redshift observable 𝑢𝑇1 (or equivalently 𝑧1 = 1/𝑢𝑇1 ) associated with the smaller
mass 𝑚1 ≪ 𝑚2 and defined by Eqs. (274) or (275). The truly coordinate and perturbative-gauge
independent properties of Ω and the redshift observable 𝑢𝑇1 play a crucial role in this comparison.
In the perturbative self-force approach we use Schwarzschild coordinates for the background, and
we refer to “gauge invariance” as a property which holds within the restricted class of gauges for
which (273) is a helical Killing vector. In all other respects, the gauge choice is arbitrary. In the
post-Newtonian approach we work with harmonic coordinates and compute the explicit expression
(276) of the redshift observable.
The main difficulty in the post-Newtonian calculation is the control to high PN order of the
near-zone metric (𝑔𝜇𝜈 )1 entering the definition of the redshift observable (276), and which has to be
regularized at the location of the particle by means of dimensional regularization (see Sections 6.3 –
6.4). Up to 2.5PN order the Hadamard regularization is sufficient and the regularized metric has
been provided in Eqs. (242). Here we report the end result of the post-Newtonian computation of
the redshift observable including all terms up to the 3PN order, and augmented by the logarithmic
contributions up to the 5PN order (and also the known Schwarzschild limit) [68, 67, 289]:
)︂
(︂
)︂
3 3
𝜈
27 27
5
5
1
− Δ−
𝑥+
− Δ − 𝜈 + Δ 𝜈 + 𝜈 2 𝑥2
4 4
2
16 16
2
8
24
(︂
)︂
135 135
37
67
115 2
5
1 3
+
−
Δ − 𝜈 − Δ𝜈 +
𝜈 − Δ 𝜈2 +
𝜈 𝑥3
32
32
4
16
32
32
48

𝑢𝑇1 = 1 +

(︂

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 114

114

Luc Blanchet

(︂

[︂
]︂
[︂
]︂
2835 2835
2183 41 2
12199 41 2
+
−
Δ+ −
+ 𝜋 𝜈+
− 𝜋 Δ𝜈
256
256
48
64
384
64
]︂
)︂
[︂
41 2 2 795
2827 3
25
35 4
17201
2
3
−
𝜋 𝜈 −
Δ𝜈 −
𝜈 −
Δ𝜈 +
𝜈 𝑥4
+
576
192
128
864
1728
10368
(︂
[︂
]︂
)︂
[︀
]︀
15309 15309
32 32
32
+
−
Δ + 𝜈 𝑢4 (𝜈) + Δ 𝑣4 (𝜈) + − + Δ − 𝜈 𝜈 ln 𝑥 𝑥5
512
512
5
5
15
(︂
[︀
]︀
168399 168399
+
−
Δ + 𝜈 𝑢5 (𝜈) + Δ 𝑣5 (𝜈)
2048
2048
)︂
[︂
]︂
)︂
(︂
478 478
10306
296 2
1
6
(288)
+
−
Δ+
𝜈 − 36Δ𝜈 −
𝜈 𝜈 ln 𝑥 𝑥 + 𝒪 14 .
105 105
105
15
𝑐
We recall that 𝑥 denotes the post-Newtonian parameter (230), 𝜈 is the mass ratio (215), and
Δ = (𝑚1 − 𝑚2 )/𝑚. The redshift observable of the other particle is deduced by setting Δ → −Δ.
In Eq. (288) we denote by 𝑢4 (𝜈), 𝑣4 (𝜈) and 𝑢5 (𝜈), 𝑣5 (𝜈) some unknown 4PN and 5PN coefficients, which are however polynomials of the symmetric mass ratio 𝜈. They can be entirely
determined from the related coefficients 𝑒4 (𝜈), 𝑗4 (𝜈) and 𝑒5 (𝜈), 𝑗5 (𝜈) in the expressions of the energy and angular momentum in Eqs. (233) and (234). To this aim it suffices to apply the differential
first law (280) up to 5PN order; see Ref. [289] for more details.
The post-Newtonian result (288) is valid for any mass ratio, and for comparison purpose with
the SF calculation we now investigate the small mass ratio regime 𝑞 ≪ 1. We introduce a postNewtonian parameter appropriate to the small mass limit of the “particle”,
(︂
)︂2/3
(︀
)︀−2/3
𝐺 𝑚2 Ω
𝑦≡
=𝑥 1+𝑞
.
(289)
3
𝑐
We express the symmetric mass ratio in terms of the asymmetric one: 𝜈 = 𝑞/(1+𝑞)2 , together with
Δ = (𝑞 − 1)/(𝑞 + 1). Then Eq. (288), expanded through first order in 𝑞, which means including
only the linear self-force level, reads
𝑢𝑇1 = 𝑢𝑇Schw + 𝑞 𝑢𝑇SF + 𝒪(𝑞 2 ) .

(290)

The Schwarzschildean result is known in closed form as
1
,
𝑢𝑇Schw = √
1 − 3𝑦
and for the self-force contribution one obtains61
(︂
)︂
121 41 2 4
𝑇
2
3
𝑢SF (𝑦) = −𝑦 − 2𝑦 − 5𝑦 + −
+ 𝜋 𝑦
3
32
)︂
(︂
)︂
(︂
956
64
5
ln 𝑦 𝑦 + 𝛼5 +
ln 𝑦 𝑦 6 + 𝑜(𝑦 6 ) .
+ 𝛼4 −
5
105

(291)

(292)

The analytic coefficients were determined up to 2PN order in Ref. [176]; the 3PN term was computed in Ref. [68] making full use of dimensional regularization; the logarithmic contributions at
the 4PN and 5PN orders were added in Refs. [67, 146].
The coefficients 𝛼4 and 𝛼5 represent some pure numbers at the 4PN and 5PN orders. By an
analytic self-force calculation [36] the coefficient 𝛼4 has been obtained as
𝛼4 = −

1157 677 2 256
128
+
𝜋 −
ln 2 −
𝛾E .
15
512
5
5

(293)

61 Since there are logarithms in this expansion we use the Landau 𝑜-symbol for remainders; see the footnote 20.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 115

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

115

Using the first law (280), we know how to deduce from the PN coefficients in the redshift variable the
corresponding PN coefficients in the energy function (233). Thus, the result reported in Eq. (236)
for the 4PN term in the energy function for circular orbits has been deduced from Eq. (293) by
application of the first law.
On the self-force front the main problem is to control the numerical resolution of the computation of the redshift observable in order to distinguish more accurately the contributions of very
high order PN terms. The comparison of the post-Newtonian expansion (292) with the numerical
SF data has confirmed with high precision the determination of the 3PN coefficient [68, 67]: Witness Table 1 where the agreement with the analytical value involves 7 significant digits. Notice
that such agreement provides an independent check of the dimensional regularization procedure
invoked in the PN expansion scheme (see Sections 6.3 – 6.4). It is remarkable that such procedure
is equivalent to the procedure of subtraction of the singular field in the SF approach [178].
Table 1: Numerically determined value of the 3PN coefficient for the SF part of the redshift observable
defined by Eq. (292). The analytic post-Newtonian computation [68] is confirmed with many significant
digits.

3PN coefficient
𝛼3 ≡ −

SF value

121 41 2
+ 𝜋 = −27.6879026 · · ·
3
32

−27.6879034 ± 0.0000004

Table 2: Numerically determined values of higher-order PN coefficients for the SF part of the redshift
observable defined by Eq. (292). The uncertainty in the last digit (or two last digits) is indicated in
parentheses. The 4PN numerical value agrees with the analytical expression (293).

PN coefficient

SF value

𝛼4
𝛼5
𝛼6
𝛽6
𝛼7

−114.34747(5)
−245.53(1)
−695(2)
+339.3(5)
−5837(16)

Furthermore the PN-SF comparison has permitted to measure the coefficients 𝛼4 and 𝛼5 with
at least 8 significant digits for the 4PN coefficient, and 5 significant digits for the 5PN one. In
Table 2 we report the result of the analysis performed in Refs. [68, 67] by making maximum
use of the analytical coefficients available at the time, i.e., all the coefficients up to 3PN order
plus the logarithmic contributions at 4PN and 5PN orders. One uses a set of five basis functions
corresponding to the unknown non-logarithmic 4PN and 5PN coefficients 𝛼4 , 𝛼5 in Eq. (292), and
augmented by the 6PN and 7PN non-logarithmic coefficients 𝛼6 , 𝛼7 plus a coefficient 𝛽6 for the
logarithm at 6PN. A contribution 𝛽7 from a logarithm at 7PN order is likely to confound with the
𝛼7 coefficient. There is also the possibility of the contribution of a logarithmic squared at 7PN
order, but such a small effect is not permitted in this fit.
Gladly we discover that the more recent analytical value of the 4PN coefficient, Eq. (293),
matches the numerical value which was earlier measured in Ref. [67] (see Table 2). This highlights
the predictive power of perturbative self-force calculations in determining numerically new postNewtonian coefficients [176, 68, 67]. This ability is obviously due to the fact (illustrated in Figure 2)
that perturbation theory is legitimate in the strong field regime of the coalescence of black hole
binary systems, which is inaccessible to the post-Newtonian method. Of course, the limitation

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 116

116

Luc Blanchet

of the self-force approach is the small mass-ratio limit; in this respect it is taken over by the
post-Newtonian approximation.
More recently, the accuracy of the numerical computation of the self-force, and the comparison
with the post-Newtonian expansion, have been drastically improved by Shah, Friedman & Whiting [383]. The PN coefficients of the redshift observable were obtained to very high 10.5PN order
both numerically and also analytically, for a subset of coefficients that are either rational or made
of the product of 𝜋 with a rational. The analytical values of the coefficients up to 6PN order have
also been obtained from an alternative self-force calculation [38, 37]. An interesting feature of the
post-Newtonian expansion at high order is the appearance of half-integral PN coefficients (i.e., of
the type 𝑛2 PN where 𝑛 is an odd integer) in the conservative dynamics of binary point particles,
moving on exactly circular orbits. This is interesting because any instantaneous (non-tail) term at
any half-integral PN order will be zero for circular orbits, as can be shown by a simple dimensional
argument [77]. Therefore half-integral coefficients can appear only due to truly hereditary (tail)
integrals. Using standard post-Newtonian methods it has been proved in Refs. [77, 78] that the
dominant half-integral PN term in the redshift observable (292) occurs at the 5.5PN order (confirming the earlier finding of Ref. [383]) and originates from the non-linear “tail-of-tail” integrals
investigated in Section 3.2. The results for the 5.5PN coefficient in Eq. (292), and also for the
next-to-leading 6.5PN and 7.5PN ones, are
81077
82561159
13696
𝜋,
𝛼6.5 =
𝜋,
𝛼7.5 =
𝜋,
(294)
525
3675
467775
and fully agree between the PN and SF computations. We emphasize that the results (294)
are achieved by the traditional PN approach, which is completely general (contrary to various
analytical and numerical SF calculations [383, 38, 37, 268]), i.e., is not tuned to a particular type
of source but is applicable to any extended PN source (see Part A). Note that Eqs. (294) represent
the complete coefficients as there are no logarithms at these orders.
To conclude, the consistency of this “cross-cultural” comparison between the analytical postNewtonian and the perturbative self-force approaches confirms the soundness of both approximations in describing the dynamics of compact binaries. Furthermore this interplay between PN and
SF efforts (which is now rapidly growing [383]) is important for the synthesis of template waveforms
of EMRIs to be analysed by space-based gravitational wave detectors, and has also an impact on
efforts of numerical relativity in the case of comparable masses.
𝛼5.5 = −

9

Gravitational Waves from Compact Binaries

We pointed out that the 3.5PN equations of motion, Eqs. (203) or (219) – (220), are merely 1PN
as regards the radiative aspects of the problem, because the radiation reaction force starts at the
2.5PN order. A solution would be to extend the precision of the equations of motion so as to
include the full relative 3PN or 3.5PN precision into the radiation reaction force, but the equations
of motion up to the 5.5PN or 6PN order are beyond the present state-of-the-art. The much
better alternative solution is to apply the wave-generation formalism described in Part A, and to
determine by its means the work done by the radiation reaction force directly as a total energy flux
at future null infinity.62 In this approach, we replace the knowledge of the higher-order radiation
reaction force by the computation of the total flux ℱ, and we apply the energy balance equation
d𝐸
= −ℱ .
(295)
d𝑡
Therefore, the result (232) that we found for the 3.5PN binary’s center-of-mass energy 𝐸 constitutes
only “half” of the solution of the problem. The second “half” consists of finding the rate of decrease
62 In addition, the wave generation formalism will provide the waveform itself, see Sections 9.4 and 9.5.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 117

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

117

d𝐸/d𝑡, which by the balance equation is nothing but the total gravitational-wave flux ℱ at the
relative 3.5PN order beyond the Einstein quadrupole formula (4).
Because the orbit of inspiralling binaries is circular, the energy balance equation is sufficient, and
there is no need to invoke the angular momentum balance equation for computing the evolution
of the orbital period 𝑃˙ and eccentricity ˙𝑒, see Eqs. (9) – (13) in the case of the binary pulsar.
Furthermore the time average over one orbital period as in Eqs. (9) is here irrelevant, and the
energy and angular momentum fluxes are related by ℱ = Ω 𝒢. This all sounds good, but it is
important to remind that we shall use the balance equation (295) at the very high 3.5PN order,
and that at such order one is missing a complete proof of it (following from first principles in
general relativity). Nevertheless, in addition to its physically obvious character, Eq. (295) has
been verified by radiation-reaction calculations, in the cases of point-particle binaries [258, 259]
and extended post-Newtonian fluids [43, 47], at the 1PN order and even at 1.5PN, the latter order
being especially important because of the first appearance of wave tails; see Section 5.4. One
should also quote here Refs. [260, 336, 278, 322, 254] for the 3.5PN terms in the binary’s equations
of motion, fully consistent with the balance equations.
Obtaining the energy flux ℱ can be divided into two equally important steps: Computing the
source multipole moments I𝐿 and J𝐿 of the compact binary system with due account of a self-field
regularization; and controlling the tails and related non-linear effects occurring in the relation
between the binary’s source moments and the radiative ones U𝐿 and V𝐿 observed at future null
infinity (cf. the general formalism of Part A).

9.1

The binary’s multipole moments

The general expressions of the source multipole moments given by Theorem 6, Eqs. (123), are
worked out explicitly for general fluid systems at the 3.5PN order. For this computation one uses
the formula (126), and we insert the 3.5PN metric coefficients (in harmonic coordinates) expressed
in Eqs. (144) by means of the retarded-type elementary potentials (146) – (148). Then we specialize
each of the (quite numerous) terms to the case of point-particle binaries by inserting, for the matter
stress-energy tensor 𝑇 𝛼𝛽 , the standard expression made out of Dirac delta-functions. In Section 11
we shall consider spinning point particle binaries, and in that case the stress-energy tensor is
given by Eq. (378). The infinite self-field of point-particles is removed by means of the Hadamard
regularization; and, as we discussed in Section 6.4, dimensional regularization is used to fix the
values of a few ambiguity parameters. This computation has been performed in Ref. [86] at the
1PN order, and in [64] at the 2PN order; we report below the most accurate 3PN results obtained
in Refs. [81, 80, 62, 63] for the flux and [11, 74, 197] for the waveform.
A difficult part of the analysis is to find the closed-form expressions, fully explicit in terms of
the particle’s positions and velocities, of many non-linear integrals. Let us give a few examples of
the type of technical formulas that are employed in this calculation. Typically we have to compute
some integrals like
∫︁
(𝑝,𝑞)
1
(296)
^𝐿 𝑟1𝑝 𝑟2𝑞 ,
𝑌𝐿 (𝑦1 , 𝑦2 ) = − ℱ𝒫 d3 x 𝑥
2𝜋
where 𝑟1 = |x − 𝑦1 | and 𝑟2 = |x − 𝑦2 |. When 𝑝 > −3 and 𝑞 > −3, this integral is perfectly welldefined, since the finite part ℱ𝒫 deals with the IR regularization of the bound at infinity. When
𝑝 ⩽ −3 or 𝑞 ⩽ −3, we cure the UV divergencies by means of the Hadamard partie finie defined
by Eq. (162); so a partie finie prescription Pf is implicit in Eq. (296). An example of closed-form
formula we get is
ℓ
(−1,−1)
𝑟12 ∑︁ ⟨𝐿−𝐾 𝐾⟩
𝑌𝐿 =
𝑦1
𝑦2 ,
(297)
ℓ+1
𝑘=0

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 118

118

Luc Blanchet

𝑖

𝑖

where we pose 𝑦1𝐿−𝐾 ≡ 𝑦1𝑖1 · · · 𝑦1ℓ−𝑘 and 𝑦2𝐾 ≡ 𝑦2ℓ−𝑘+1 · · · 𝑦2𝑖ℓ , the brackets surrounding indices
denoting the STF projection. Another example, in which the ℱ𝒫 regularization is crucial, is (in
the quadrupole case ℓ = 2)
(−2,−1)

]︂
(︂
)︂
]︂
(︂
)︂
]︂
[︂
[︂
188
𝑟12
4
𝑟12
2
8
⟨𝑖 𝑗⟩
⟨𝑖𝑗⟩ 2
𝑌𝑖𝑗
−
+ 𝑦1 𝑦2
ln
−
+ 𝑦2
ln
−
,
225
15
𝑟0
225
5
𝑟0
25
(298)
where the IR scale 𝑟0 is defined in Eq. (42). Still another example, which necessitates both the
ℱ𝒫 and a UV partie finie regularization at the point 1, is
]︂
[︂
(︂ )︂
(−3,0)
16 ⟨𝑖𝑗⟩
𝑠1
+
𝑦
,
(299)
𝑌𝑖𝑗 = 2 ln
𝑟0
15 1
⟨𝑖𝑗⟩
= 𝑦1

[︂

16
ln
15

(︂

𝑟12
𝑟0

)︂

where 𝑠1 is the Hadamard-regularization constant introduced in Eq. (162).
The most important input for the computation of the waveform and flux is the mass quadrupole
moment I𝑖𝑗 , since this moment necessitates the full post-Newtonian precision. Here we give the
mass quadrupole moment complete to order 3.5PN, for non-spinning compact binaries on circular
orbits, as
(︂
)︂
(︂ )︂
𝑟2
48 𝐺2 𝑚2 𝜈
1
I𝑖𝑗 = 𝜇 𝐴 𝑥⟨𝑖𝑗⟩ + 𝐵 2 𝑣 ⟨𝑖𝑗⟩ +
𝐶
𝑥
𝑣
+
𝒪
,
(300)
⟨𝑖 𝑗⟩
5
𝑐
7
𝑐 𝑟
𝑐8
where 𝑥 = 𝑦1 − 𝑦2 = (𝑥𝑖 ) and 𝑣 = 𝑣1 − 𝑣2 = (𝑣𝑖 ) are the orbital separation and relative velocity.
The third term with coefficient 𝐶 is a radiation-reaction term, which will affect the waveform at
orders 2.5PN and 3.5PN; however it does not contribute to the energy flux for circular orbits. The
two conservative coefficients are 𝐴 and 𝐵. All those coefficients are [81, 74, 197]
)︂
(︂
)︂
(︂
13
461
18395
241 2
1
−
𝜈−
𝜈
(301a)
𝐴 = 1 + 𝛾 − − 𝜈 + 𝛾2 −
42 14
1512
1512
1512
(︂
(︂
)︂
(︂
)︂ [︂
)︂]︂
𝑟12
𝑟12
395899 428
3304319 44
2351 3
162539 2
−
ln
−
ln
𝜈
+
𝜈
,
+
𝜈
+
+ 𝛾3
13200
105
𝑟0
166320
3
𝑟′ 0
16632
33264
(︂
)︂
11 11
1607 1681
229 2
𝐵=
− 𝜈+𝛾
−
𝜈+
𝜈
21
7
378
378
378
(︂
(︂
)︂
)︂
357761
428
𝑟
92339
35759 2
457 3
12
+ 𝛾2 −
+
ln
−
𝜈+
𝜈 +
𝜈
,
(301b)
19800
105
𝑟0
5544
924
5544
(︂
)︂
256 1532
𝐶 =1+𝛾 −
−
𝜈 .
(301c)
135
405
These expressions are valid in harmonic coordinates via the post-Newtonian parameter 𝛾 = 𝐺𝑚
𝑟𝑐2
defined in Eq. (225). As we see, there are two types of logarithms at 3PN order in the quadrupole
moment: One type involves the UV length scale 𝑟0′ related by Eq. (221) to the two gauge constants
𝑟1′ and 𝑟2′ present in the 3PN equations of motion; the other type contains the IR length scale 𝑟0
coming from the general formalism of Part A – indeed, recall that there is a ℱ𝒫 operator in front
of the source multipole moments in Theorem 6. As we know, the UV scale 𝑟0′ is specific to the
standard harmonic (SH) coordinate system and is pure gauge (see Section 7.3): It will disappear
from our physical results at the end. On the other hand, we have proved that the multipole
expansion outside a general post-Newtonian source is actually free of 𝑟0 , since the 𝑟0 ’s present
in the two terms of Eq. (105) cancel out. Indeed we have already found in Eqs. (93) – (94) that
the constant 𝑟0 present in I𝑖𝑗 is compensated by the same constant coming from the non-linear
wave “tails of tails” in the radiative moment U𝑖𝑗 . For a while, the expressions (301) contained the
ambiguity parameters 𝜉, 𝜅 and 𝜁, which have now been replaced by their correct values (173).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 119

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

119

Besides the 3.5PN mass quadrupole (300) – (301), we need also (for the 3PN waveform) the
mass octupole moment I𝑖𝑗𝑘 and current quadrupole moment J𝑖𝑗 , both of them at the 2.5PN order;
these are given for circular orbits by [81, 74]
{︂
[︂
(︂
)︂]︂
139 11923
29 2
I𝑖𝑗𝑘 = −𝜈 𝑚 Δ 𝑥⟨𝑖𝑗𝑘⟩ 1 − 𝛾𝜈 − 𝛾 2
+
𝜈+
𝜈
330
660
110
[︂
(︂
)︂]︂
2
1066
𝑟
1433
21
+ 2 𝑥⟨𝑖 𝑣𝑗𝑘⟩ 1 − 2𝜈 − 𝛾 −
+
𝜈 − 𝜈2
𝑐
165
330
55
}︂
(︂ )︂
196 𝑟 2
1
(302a)
+
𝛾 𝜈 𝑥⟨𝑖𝑗 𝑣𝑘⟩ + 𝒪 6 ,
15 𝑐
𝑐
{︂
[︂
(︂
)︂
(︂
)︂]︂
67 2
13 4651
1 2
J𝑖𝑗 = −𝜈 𝑚 Δ 𝜖𝑎𝑏⟨𝑖 𝑥𝑗⟩𝑎 𝑣𝑏 1 + 𝛾
− 𝜈 + 𝛾2
−
𝜈−
𝜈
28 7
9
252
168
}︂
(︂ )︂
188 𝑟 2
1
(302b)
−
𝛾 𝜈 𝜖𝑎𝑏⟨𝑖 𝑣𝑗⟩𝑎 𝑥𝑏 + 𝒪 6 .
35 𝑐
𝑐
The list of required source moments for the 3PN waveform continues with the 2PN mass 24 -pole
and current 23 -pole (octupole) moments, and so on. Here we give the most updated moments:63
{︂
[︂
(︂
)︂
3
25
69 2
I𝑖𝑗𝑘𝑙 = 𝜈 𝑚 𝑥⟨𝑖𝑗𝑘𝑙⟩ 1 − 3𝜈 + 𝛾
− 𝜈+ 𝜈
110 22
22
(︂
)︂]︂
126901 58101
204153 2 1149 3
+ 𝛾2 −
−
𝜈+
𝜈 +
𝜈
200200
2600
2860
1144
[︂
2
𝑟
78
+ 2 𝑥⟨𝑖𝑗 𝑣𝑘𝑙⟩
(1 − 5𝜈 + 5𝜈 2 )
𝑐
55
(︂
)︂]︂
30583 107039
8792 2 639 3
+ 𝛾
−
𝜈+
𝜈 −
𝜈
3575
3575
715
715
}︂
(︂ )︂
(︀
)︀
71 𝑟4
1
2
3
𝑣⟨𝑖𝑗𝑘𝑙⟩ 1 − 7𝜈 + 14𝜈 − 7𝜈
+𝒪 5 ,
(303a)
+
715 𝑐4
𝑐
)︂
{︂
[︂
(︂
13
181 109
−
𝜈 + 𝜈2
J𝑖𝑗𝑘 = 𝜈 𝑚 𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑘⟩𝑎 𝑣𝑏 1 − 3𝜈 + 𝛾
90
18
18
(︂
)︂]︂
1469 5681
48403 2
559 3
+ 𝛾2
−
𝜈+
𝜈 −
𝜈
3960
264
660
3960
[︂
(︂
)︂]︂}︂
)︀
𝑟2
7 (︀
1621 4879
1084 2 259 3
2
+ 2 𝜖𝑎𝑏⟨𝑖 𝑥𝑎 𝑣𝑗𝑘⟩𝑏
1 − 5𝜈 + 5𝜈 + 𝛾
−
𝜈+
𝜈 −
𝜈
𝑐
45
990
990
495
990
(︂ )︂
1
+𝒪 5 .
(303b)
𝑐
{︂
[︂
(︂
)︂]︂
2
47
28
I𝑖𝑗𝑘𝑙𝑚 = −𝜈 𝑚 Δ 𝑥⟨𝑖𝑗𝑘𝑙𝑚⟩ 1 − 2𝜈 + 𝛾
− 𝜈 + 𝜈2
39 39
13
}︂
(︂ )︂
2
(︀
)︀
70 𝑟
1
+
𝑥⟨𝑖𝑗𝑘 𝑣𝑙𝑚⟩ 1 − 4𝜈 + 3𝜈 2 + 𝒪 4 ,
(303c)
39 𝑐2
𝑐
{︂
[︂
(︂
)︂]︂
20 155
5
J𝑖𝑗𝑘𝑙 = −𝜈 𝑚 Δ 𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑘𝑙⟩𝑎 𝑣𝑏 1 − 2𝜈 + 𝛾
−
𝜈 + 𝜈2
11
44
11
}︂
(︂ )︂
(︀
)︀
4 𝑟2
1
2
+
𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑎 𝑣𝑘𝑙⟩𝑏 1 − 4𝜈 + 3𝜈
+𝒪 4 .
(303d)
11 𝑐2
𝑐
63 The STF projection ⟨⟩ applies only on “living” indices 𝑖𝑗𝑘𝑙 · · ·

but not on the summed up indices 𝑎 and 𝑏.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 120

120

Luc Blanchet

{︂
[︂
(︂
)︂]︂
1
3
11 3
2
2
I𝑖𝑗𝑘𝑙𝑚𝑛 = 𝜈 𝑚 𝑥⟨𝑖𝑗𝑘𝑙𝑚𝑛⟩ 1 − 5𝜈 + 5𝜈 + 𝛾
− 𝜈 + 6𝜈 − 𝜈
14 2
2
}︂
(︂ )︂
2
(︀
)︀
1
15 𝑟
𝑥⟨𝑖𝑗𝑘𝑙 𝑣𝑚𝑛⟩ 1 − 7𝜈 + 14𝜈 2 − 7𝜈 3 + 𝒪 4 ,
+
7 𝑐2
𝑐
{︂
[︂
(︂
)︂]︂
1549 1081
107 2 29 3
2
J𝑖𝑗𝑘𝑙𝑚 = 𝜈 𝑚 𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑘𝑙𝑚⟩𝑎 𝑣𝑏 1 − 5𝜈 + 5𝜈 + 𝛾
−
𝜈+
𝜈 − 𝜈
910
130
13
26
)︂
}︂
(︂
2
(︀
)︀
54 𝑟
1
𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑘𝑎 𝑣𝑙𝑚⟩𝑏 1 − 7𝜈 + 14𝜈 2 − 7𝜈 3 + 𝒪 4 .
+
2
91 𝑐
𝑐
(︂ )︂
1
I𝑖𝑗𝑘𝑙𝑚𝑛𝑜 = −𝜈 𝑚 Δ(1 − 4𝜈 + 3𝜈 2 ) 𝑥⟨𝑖𝑗𝑘𝑙𝑚𝑛𝑜⟩ + 𝒪 2 ,
𝑐
(︂ )︂
1
2
J𝑖𝑗𝑘𝑙𝑚𝑛 = −𝜈 𝑚 Δ(1 − 4𝜈 + 3𝜈 ) 𝜖𝑎𝑏⟨𝑖 𝑥𝑗𝑘𝑙𝑚𝑛⟩𝑎 𝑣𝑏 + 𝒪 2 .
𝑐

(303e)

(303f)
(303g)
(303h)

All the other higher-order moments are required at the Newtonian order, at which they are trivial
to compute with result (∀ ℓ ∈ N)
(︂ )︂
1
I𝐿 = 𝜈 𝑚 𝜎ℓ (𝜈) 𝑥⟨𝐿⟩ + 𝒪
,
(304a)
𝑐
(︂ )︂
1
J𝐿−1 = 𝜈 𝑚 𝜎ℓ (𝜈) 𝜖𝑎𝑏⟨𝑖𝑙−1 𝑥𝐿−2⟩𝑎 𝑣𝑏 + 𝒪
.
(304b)
𝑐
𝑚2
1
Here we introduce the useful notation 𝜎ℓ (𝜈) ≡ 𝑋2ℓ−1 + (−)ℓ 𝑋1ℓ−1 , where 𝑋1 = 𝑚
𝑚 and 𝑋2 = 𝑚
are such that 𝑋1 + 𝑋2 = 1, 𝑋1 − 𝑋2 = Δ and 𝑋1 𝑋2 = 𝜈. More explicit expressions are (𝑘 ∈ N):

𝜎2𝑘 (𝜈) =

𝑘−1
∑︁

(−)𝑝

2𝑘 − 1
2𝑘 − 1 − 𝑝

𝑘−1
∑︁

(︂

𝑝=0

𝜎2𝑘+1 (𝜈) = −Δ

(−)𝑝

𝑝=0

where

(︁ )︁

9.2

Gravitational wave energy flux

𝑛
𝑝

(︂

2𝑘 − 1 − 𝑝
𝑝

2𝑘 − 1 − 𝑝
𝑝

)︂

𝜈𝑝 ,

)︂

𝜈𝑝 ,

(305a)

(305b)

is the usual binomial coefficient.

The results (300) – (304) permit the control of the instantaneous part of the total energy flux, by
which we mean that part of the flux which is generated solely by the source multipole moments,
i.e., not counting the hereditary tail and related integrals. The instantaneous flux ℱinst is defined
by the replacement into the general expression of ℱ given by Eq. (68a) of all the radiative moments
U𝐿 and V𝐿 by the corresponding ℓ-th time derivatives of the source moments I𝐿 and J𝐿 . Up to
the 3.5PN order we have
{︂
[︂
]︂
[︂
]︂
𝐺 1 (3) (3)
1
1 (4) (4) 16 (3) (3)
1
1 (5) (5)
1 (4) (4)
ℱinst = 5
I𝑖𝑗 I𝑖𝑗 + 2
I𝑖𝑗𝑘 I𝑖𝑗𝑘 + J𝑖𝑗 J𝑖𝑗 + 4
I𝑖𝑗𝑘𝑚 I𝑖𝑗𝑘𝑚 + J𝑖𝑗𝑘 J𝑖𝑗𝑘
𝑐
5
𝑐 189
45
𝑐 9072
84
[︂
]︂
(︂ )︂}︂
1
1
4
1
(6)
(6)
(5)
(5)
+ 6
I
I
+
J
J
+𝒪 8
.
(306)
𝑐 594000 𝑖𝑗𝑘𝑚𝑛 𝑖𝑗𝑘𝑚𝑛 14175 𝑖𝑗𝑘𝑚 𝑖𝑗𝑘𝑚
𝑐
in which we insert the explicit expressions (300) – (304) for the moments. The time derivatives of
these source moments are computed by means of the circular-orbit equations of motion given by

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 121

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

Eq. (226) together with (228). The net result is
{︂
(︂
)︂
(︂
)︂
32𝑐5 2 5
2927 5
293383 380
ℱinst =
𝜈 𝛾 1+ −
− 𝜈 𝛾+
+
𝜈 𝛾2
5𝐺
336
4
9072
9
[︂
(︂
)︂
53712289 1712
𝑟12
+
−
ln
1108800
105
𝑟0
)︂)︂
(︂
(︂
]︂
(︂ )︂}︂
383 2 3
50625 123 2 110
𝑟12
1
𝜈−
.
+ −
+
𝜋 +
ln
𝜈 𝛾 +𝒪 8
112
64
3
𝑟0′
9
𝑐

121

(307)

The Newtonian approximation agrees with the prediction of the Einstein quadrupole formula (4), as
reduced for quasi-circular binary orbits by Landau & Lifshitz [285]. At the 3PN order in Eq. (307),
there was some Hadamard regularization ambiguity parameters which have been replaced by their
values computed with dimensional regularization.
To the instantaneous part of the flux, we must add the contribution of non-linear multipole
interactions contained in the relationship between the source and radiative moments. The needed
material has already been provided in Sections 3.3. Similar to the decomposition of the radiative
quadrupole moment in Eq. (88), we can split the energy flux into the different terms
ℱ = ℱinst + ℱtail + ℱtail-tail ,

(308)

where ℱinst has just been obtained in Eq. (307); ℱtail is made of the quadratic multipolar tail
integrals in Eqs. (90) and (95); ℱtail-tail involves the square of the quadrupole tail in Eq. (90) and
the quadrupole tail of tail given in Eq. (91).
We shall see that the tails play a crucial role in the predicted signal of compact binaries. It is
quite remarkable that so small an effect as a “tail of tail” should be relevant to the data analysis of
the current generation of gravitational wave detectors. By contrast, the non-linear memory effects,
given by the integrals inside the 2.5PN and 3.5PN terms in Eq. (92), do not contribute to the
gravitational-wave energy flux before the 4PN order in the case of circular-orbit binaries. Indeed
the memory integrals are actually “instantaneous” in the flux, and a simple general argument
based on dimensional analysis shows that instantaneous terms cannot contribute to the energy
flux for circular orbits.64 Therefore the memory effect has rather poor observational consequences
for future detections of inspiralling compact binaries.
Let us also recall that following the general formalism of Part A, the mass M which appears in
front of the tail integrals of Sections 3.2 and 3.3 represents the binary’s mass monopole M or ADM
mass. In a realistic model where the binary system has been formed as a close compact binary at
a finite instant in the past, this mass is equal to the sum of the rest masses 𝑚 = 𝑚1 + 𝑚2 , plus
the total binary’s mass-energy 𝐸/𝑐2 given for instance by Eq. (229). At 3.5PN order we need 2PN
corrections in the tails and therefore 2PN also in the mass 𝑀 , thus
(︂ )︂]︂
[︂
𝜈
1
𝜈
2
.
(309)
M = 𝑚 1 − 𝛾 + (7 − 𝜈) 𝛾 + 𝒪 6
2
8
𝑐
Notice that 2PN order in M corresponds to 1PN order in 𝐸.
We give the two basic technical formulas needed when carrying out the reduction of the tail
and tail-of-tail integrals to circular orbits (see e.g., [230]):
∫︁ +∞

(︂
d𝜏 ln

0

𝜏
2𝜏0

)︂

𝑒−i𝜔𝜏 =

)︀
𝜋 )︁
i (︁ (︀
ln 2𝜔𝜏0 + 𝛾E + i
,
𝜔
2

(310a)

64 The same argument shows that the non-linear multipole interactions in Eq. (89) as well as those in Eqs. (97)
and (98) do not contribute to the flux for circular orbits.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 122

122

Luc Blanchet

∫︁ +∞

2

d𝜏 ln
0

(︂

𝜏
2𝜏0

)︂

−i𝜔𝜏

𝑒

[︂
]︂
)︀
i (︁ (︀
𝜋 )︁2 𝜋 2
=−
ln 2𝜔𝜏0 + 𝛾E + i
+
,
𝜔
2
6

(310b)

where 𝜔 > 0 is a strictly positive frequency (a multiple of the orbital frequency Ω), where 𝜏0 = 𝑟0 /𝑐
and 𝛾E is the Euler constant.
Notice the important point that the tail (and tail-of-tail) integrals can be evaluated, thanks to
these formulas, for a fixed (i.e., non-decaying) circular orbit. Indeed it can be shown [60, 87] that
the “remote-past” contribution to the tail integrals is negligible; the errors due to the fact that
the orbit has actually evolved in the past, and spiraled in by emission of gravitational radiation,
are of the order of the radiation-reaction scale 𝒪(𝑐−5 ),65 and do not affect the signal before the
4PN order. We then find, for the quadratic tails stricto sensu, the 1.5PN, 2.5PN and 3.5PN
contributions
{︂
(︂
)︂
(︂
)︂
25663 125
90205 505747
12809 2
32𝑐5 5 2
𝛾 𝜈 4𝜋𝛾 3/2 + −
−
𝜈 𝜋𝛾 5/2 +
+
𝜈+
𝜈
𝜋𝛾 7/2
ℱtail =
5𝐺
672
8
576
1512
756
(︂ )︂}︂
1
.
(311)
+𝒪 8
𝑐
For the sum of squared tails and cubic tails of tails at 3PN, we get
{︂(︂
(︂
)︂
)︂
116761 16 2 1712
1712
𝑟12
32𝑐5 5 2
856
𝛾 𝜈
−
+ 𝜋 −
𝛾E +
ln
ln (16𝛾) 𝛾 3
ℱtail-tail =
−
5𝐺
3675
3
105
105
𝑟0
105
(︂ )︂}︂
1
+𝒪 8
.
(312)
𝑐
By comparing Eqs. (307) and (312) we observe that the constants 𝑟0 cleanly cancel out. Adding
together these contributions we obtain
)︂
{︂
(︂
32𝑐5 5 2
2927 5
ℱ=
𝛾 𝜈 1+ −
− 𝜈 𝛾 + 4𝜋𝛾 3/2
5𝐺
336
4
)︂
(︂
)︂
(︂
25663 125
293383 380
2
+
𝜈 𝛾 + −
−
𝜈 𝜋𝛾 5/2
+
9072
9
672
8
[︂
129386791 16𝜋 2
1712
856
+
+
−
𝛾E −
ln(16𝛾)
7761600
3
105
105
(︂
(︂
)︂
)︂
]︂
50625 110
𝑟12
123𝜋 2
383 2 3
+ −
+
ln
+
𝜈−
𝜈 𝛾
112
3
𝑟′ 0
64
9
(︂
)︂
(︂ )︂}︂
90205 505747
12809 2
1
+
+
𝜈+
𝜈 𝜋𝛾 7/2 + 𝒪 8
.
(313)
576
1512
756
𝑐
The gauge constant 𝑟0′ has not yet disappeared because the post-Newtonian expansion is still
parametrized by 𝛾 instead of the frequency-related parameter 𝑥 defined by Eq. (230) – just as for
𝐸 when it was given by Eq. (229). After substituting the expression 𝛾(𝑥) given by Eq. (231), we
find that 𝑟0′ does cancel as well. Because the relation 𝛾(𝑥) is issued from the equations of motion,
the latter cancellation represents an interesting test of the consistency of the two computations, in
harmonic coordinates, of the 3PN multipole moments and the 3PN equations of motion. At long
last we obtain our end result:66
{︂
(︂
)︂
32𝑐5 2 5
1247 35
ℱ=
𝜈 𝑥 1+ −
− 𝜈 𝑥 + 4𝜋𝑥3/2
5𝐺
336
12
65 Or, rather, 𝒪(𝑐−5 ln 𝑐) as shown in the Appendix of Ref. [87].
66 See Section 10 for the generalization of the flux of energy to eccentric binary orbits.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 123

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

123

(︂

)︂
)︂
(︂
44711 9271
65 2
8191 583
2
+ −
+
𝜈+ 𝜈 𝑥 + −
−
𝜈 𝜋𝑥5/2
9072
504
18
672
24
[︂
856
6643739519 16 2 1712
+ 𝜋 −
𝛾E −
ln(16 𝑥)
+
69854400
3
105
105
(︂
)︂
]︂
134543 41 2
94403 2 775 3 3
+ −
+ 𝜋 𝜈−
𝜈 −
𝜈 𝑥
7776
48
3024
324
(︂
)︂
(︂ )︂}︂
16285 214745
193385 2
1
+ −
.
+
𝜈+
𝜈 𝜋𝑥7/2 + 𝒪 8
504
1728
3024
𝑐

(314)

In the test-mass limit 𝜈 → 0 for one of the bodies, we recover exactly the result following from linear
black-hole perturbations obtained by Tagoshi & Sasaki [395] (see also [393, 397]). In particular, the
rational fraction 6643739519
69854400 comes out exactly the same as in black-hole perturbations. On the other
hand, the ambiguity parameters discussed in Section 6.2 were part of the rational fraction − 134543
7776 ,
belonging to the coefficient of the term at 3PN order proportional to 𝜈 (hence this coefficient cannot
be computed by linear black-hole perturbations).
The effects due to the spins of the two black holes arise at the 1.5PN order for the spin-orbit
(SO) coupling, and at the 2PN order for the spin-spin (SS) coupling, for maximally rotating black
holes. Spin effects will be discussed in Section 11. On the other hand, the terms due to the
radiating energy flowing into the black-hole horizons and absorbed rather than escaping to infinity,
have to be added to the standard post-Newtonian calculation based on point particles as presented
here; such terms arise at the 4PN order for Schwarzschild black holes [349] and at 2.5PN order for
Kerr black holes [392].

9.3

Orbital phase evolution

We shall now deduce the laws of variation with time of the orbital frequency and phase of an
inspiralling compact binary from the energy balance equation (295). The center-of-mass energy 𝐸
is given by Eq. (232) and the total flux ℱ by Eq. (314). For convenience we adopt the dimensionless
time variable67
)︀
𝜈𝑐3 (︀
Θ≡
𝑡c − 𝑡 ,
(315)
5𝐺𝑚
where 𝑡c denotes the instant of coalescence, at which the frequency formally tends to infinity,
although evidently, the post-Newtonian method breaks down well before this point. We transform the balance equation into an ordinary differential equation for the parameter 𝑥, which is
immediately integrated with the result
{︂
(︂
)︂
1
743
11
1
𝑥 = Θ−1/4 1 +
+ 𝜈 Θ−1/4 − 𝜋Θ−3/8
4
4032 48
5
(︂
)︂
(︂
)︂
19583
24401
31 2
11891
109
+
+
𝜈+
𝜈 Θ−1/2 + −
+
𝜈 𝜋Θ−5/8
254016 193536
288
53760 1920
[︂
(︂
)︂
10052469856691 1 2 107
107
Θ
+ −
+ 𝜋 +
𝛾E −
ln
6008596070400
6
420
3360
256
(︂
)︂
]︂
3147553127
451 2
15211 2
25565 3
+
−
𝜋 𝜈−
𝜈 +
𝜈 Θ−3/4
780337152
3072
442368
331776
(︂
)︂
(︂ )︂}︂
113868647
31821
294941 2
1
+ −
−
𝜈+
𝜈 𝜋Θ−7/8 + 𝒪 8
.
(316)
433520640 143360
3870720
𝑐
67 Notice the “strange” post-Newtonian order of this time variable: Θ = 𝒪(𝑐+8 ).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 124

124

Luc Blanchet

The orbital phase is defined as the angle 𝜑, oriented in the sense of the motion, between the
separation of the two bodies and the direction of the ascending node (called 𝒩 in Section 9.4)
within the plane of the sky. We have d𝜑/d𝑡 = Ω, which translates, with our notation, into
d𝜑/dΘ = −5𝑥3/2 /𝜈, from which we determine68
{︂
(︂
)︂
1
3715 55
3
𝜑 = − Θ5/8 1 +
+ 𝜈 Θ−1/4 − 𝜋Θ−3/8
𝜈
8064 96
4
(︂
)︂
(︂
)︂
(︂ )︂
9275495
284875
1855 2
38645
65
Θ
+
+
𝜈+
𝜈 Θ−1/2 + −
+
𝜈 𝜋Θ−5/8 ln
14450688 258048
2048
172032 2048
Θ0
(︂
)︂
[︂
107
Θ
831032450749357 53 2 107
− 𝜋 −
𝛾E +
ln
+
57682522275840
40
56
448
256
(︂
)︂
]︂
126510089885 2255 2
154565 2 1179625 3
+ −
+
𝜋 𝜈+
𝜈 −
𝜈 Θ−3/4
4161798144
2048
1835008
1769472
)︂
(︂ )︂}︂
(︂
488825
141769 2
1
188516689
,
(317)
+
𝜈−
𝜈 𝜋Θ−7/8 + 𝒪 8
+
173408256𝑥 516096
516096
𝑐
where Θ0 is a constant of integration that can be fixed by the initial conditions when the wave
frequency enters the detector. Finally we want also to dispose of the important expression of the
phase in terms of the frequency 𝑥. For this we get
)︂
{︂
(︂
𝑥−5/2
3715 55
𝜑=−
+ 𝜈 𝑥 − 10𝜋𝑥3/2
1+
32𝜈
1008 12
(︂
)︂
(︂
)︂
(︂ )︂
15293365 27145
3085 2
38645 65
𝑥
+
+
𝜈+
𝜈 𝑥2 +
− 𝜈 𝜋𝑥5/2 ln
1016064
1008
144
1344
16
𝑥0
[︂
12348611926451 160 2 1712
856
+
−
𝜋 −
𝛾E −
ln(16 𝑥)
18776862720
3
21
21
(︂
)︂
]︂
15737765635 2255 2
76055 2 127825 3 3
+ −
+
𝜋 𝜈+
𝜈 −
𝜈 𝑥
12192768
48
6912
5184
)︂
(︂ )︂}︂
(︂
74045 2
1
77096675 378515
+
𝜈−
𝜈 𝜋𝑥7/2 + 𝒪 8
,
(318)
+
2032128
12096
6048
𝑐
where 𝑥0 is another constant of integration. With the formula (318) the orbital phase is complete
up to the 3.5PN order for non-spinning compact binaries. Note that the contributions of the
quadrupole moments of compact objects which are induced by tidal effects, are expected from
Eq. (16) to come into play only at the 5PN order.
As a rough estimate of the relative importance of the various post-Newtonian terms, we give
in Table 3 their contributions to the accumulated number of gravitational-wave cycles 𝒩cycle in
the bandwidth of ground-based detectors. Note that such an estimate is only indicative, because a
full treatment would require the knowledge of the detector’s power spectral density of noise, and a
complete simulation of the parameter estimation using matched filtering techniques [138, 350, 284].
We define 𝒩cycle as
𝜑ISCO − 𝜑seismic
𝒩cycle ≡
.
(319)
𝜋
The frequency of the signal at the entrance of the bandwidth is the seismic cut-off frequency
𝑓seismic of ground-based detectors; the terminal frequency is assumed for simplicity to be given
68 This procedure for computing analytically the orbital phase corresponds to what is called in the jargon the
“Taylor T2 approximant”. We refer to Ref. [98] for discussions on the usefulness of defining several types of
approximants for computing (in general numerically) the orbital phase.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 125

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

125

3

by the Schwarzschild innermost stable circular orbit: 𝑓ISCO = 63/2𝑐𝜋𝐺𝑚 . Here we denote by 𝑓 =
Ω/𝜋 = 2/𝑃 the signal frequency of the dominant harmonics at twice the orbital frequency. As
we see in Table 3, with the 3PN or 3.5PN approximations we reach an acceptable accuracy level
of a few cycles say, that roughly corresponds to the demand made by data-analysists in the case
of neutron-star binaries [139, 137, 138, 346, 105, 106]. Indeed, the above estimation suggests that
the neglected 4PN terms will yield some systematic errors that are, at most, of the same order of
magnitude, i.e., a few cycles, and perhaps much less.
Table 3: Post-Newtonian contributions to the accumulated number of gravitational-wave cycles 𝒩cycle
for compact binaries detectable in the bandwidth of LIGO-VIRGO detectors. The entry frequency is
3
𝑓seismic = 10 Hz and the terminal frequency is 𝑓ISCO = 63/2𝑐𝜋𝐺 𝑚 . The main origin of the approximation
(instantaneous vs. tail) is indicated. See also Table 4 in Section 11 below for the contributions of spin-orbit
effects.

PN order
N
1PN
1.5PN
2PN
2.5PN
3PN
3.5PN

9.4

1.4 𝑀⊙ + 1.4 𝑀⊙

10 𝑀⊙ + 1.4 𝑀⊙

10 𝑀⊙ + 10 𝑀⊙

15952.6
439.5
−210.3
9.9
−11.7
2.6
−0.9

3558.9
212.4
−180.9
9.8
−20.0
2.3
−1.8

598.8
59.1
−51.2
4.0
−7.1
2.2
−0.8

(inst)
(inst)
(leading tail)
(inst)
(1PN tail)
(inst + tail-of-tail)
(2PN tail)

Polarization waveforms for data analysis

The theoretical templates of the compact binary inspiral follow from insertion of the previous
solutions for the 3.5PN-accurate orbital frequency and phase into the binary’s two polarization
waveforms ℎ+ and ℎ× defined with respect to a choice of two polarization vectors 𝑃 = (𝑃𝑖 ) and
𝑄 = (𝑄𝑖 ) orthogonal to the direction 𝑁 of the observer; see Eqs. (69).
Our convention for the two polarization vectors is that they form with 𝑁 a right-handed triad,
and that 𝑃 and 𝑄 lie along the major and minor axis, respectively, of the projection onto the plane
of the sky of the circular orbit. This means that 𝑃 is oriented toward the orbit’s ascending node –
namely the point 𝒩 at which the orbit intersects the plane of the sky and the bodies are moving
toward the observer located in the direction 𝑁 . The ascending node is also chosen for the origin of
the orbital phase 𝜑. We denote by 𝑖 the inclination angle between the direction of the detector 𝑁
as seen from the binary’s center-of-mass, and the normal to the orbital plane (we always suppose
that the normal is right-handed with respect to the sense of motion, so that 0 ⩽ 𝑖 ⩽ 𝜋). We use
the shorthands 𝑐𝑖 ≡ cos 𝑖 and 𝑠𝑖 ≡ sin 𝑖 for the cosine and sine of the inclination angle.
We shall include in ℎ+ and ℎ× all the harmonics, besides the dominant one at twice the orbital
frequency, consistent with the 3PN approximation [82, 11, 74]. In Section 9.5 we shall give all
the modes (ℓ, 𝑚) in a spherical-harmonic decomposition of the waveform, and shall extend the
dominant quadrupole mode (2, 2) at 3.5PN order [197]. The post-Newtonian terms are ordered by
2/3
means of the frequency-related variable 𝑥 = ( 𝐺𝑚Ω
; to ease the notation we pose
𝑐3 )
+∞

2𝐺𝜇𝑥 ∑︁ 𝑝/2
ℎ+,× = 2
𝑥
𝐻 +,× (𝜓, 𝑐𝑖 , 𝑠𝑖 ; ln 𝑥) + 𝒪
𝑐 𝑅 𝑝=0
𝑝/2

(︂

1
𝑅2

)︂
.

(320)

Note that the post-Newtonian coefficients will involve the logarithm ln 𝑥 starting at 3PN order;
see Eq. (127). They depend on the binary’s phase 𝜑, explicitly given at 3.5PN order by Eq. (318),

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 126

126

Luc Blanchet

through the very useful auxiliary phase variable 𝜓 that is “distorted by tails” [87, 11] and reads
2𝐺M Ω
𝜓 ≡𝜑−
ln
𝑐3

(︂

Ω
Ω0

)︂
.

(321)

Here M denotes the binary’s ADM mass and it is very important to include all its relevant postNewtonian contributions as given by Eq. (309). The constant frequency Ω0 can be chosen at will,
for instance to be the entry frequency of some detector. For the plus polarization we have69
1 2
2
𝑠 (17 + 𝑐2𝑖 ) ,
𝐻 + = −(1 + 𝑐𝑖 ) cos 2𝜓 −
96 𝑖
0
)︂
(︂
)︂]︂
[︂
(︂
9 9 2
5 1 2
+ 𝑐 − cos 3𝜓
+ 𝑐
,
𝐻 + = − 𝑠𝑖 Δ cos 𝜓
8 8 𝑖
8 8 𝑖
1/2
[︂
(︂
)︂]︂
19 3 2 1 4
19 11 2
+ 𝑐𝑖 − 𝑐𝑖 + 𝜈 − +
𝑐 + 𝑐4𝑖
𝐻 + = cos 2𝜓
6
2
3
6
6 𝑖
1
]︂
[︂
4 2
2
𝑠 (1 + 𝑐𝑖 )(1 − 3𝜈) ,
− cos 4𝜓
3 𝑖
(︂
)︂]︂
[︂
5 2
1 4
49 1 2
1 4
19
+
𝑐 −
𝑐 + 𝜈 − + 𝑐𝑖 +
𝑐
𝐻 + = 𝑠𝑖 Δ cos 𝜓
64 16 𝑖
192 𝑖
96 8
96 𝑖
3/2
[︁
]︁
+ cos 2𝜓 −2𝜋(1 + 𝑐2𝑖 )
[︂
(︂
)︂]︂
657 45 2
225 9 2 81 4
81 4
+ 𝑠𝑖 Δ cos 3𝜓 −
−
𝑐 +
𝑐 +𝜈
− 𝑐𝑖 −
𝑐
128 16 𝑖
128 𝑖
64
8
64 𝑖
[︂
]︂
625 2
+ 𝑠𝑖 Δ cos 5𝜓
𝑠 (1 + 𝑐2𝑖 )(1 − 2𝜈) ,
384 𝑖
[︂
]︂
5 1 2
𝐻 + = 𝜋 𝑠𝑖 Δ cos 𝜓 − − 𝑐𝑖
8 8
2
[︂
(︂
)︂
11 33 2 29 4
1 6
353
251 4
5 6
+ cos 2𝜓
+
𝑐𝑖 +
𝑐𝑖 −
𝑐𝑖 + 𝜈
− 3 𝑐2𝑖 −
𝑐𝑖 +
𝑐𝑖
60 10
24
24
36
72
24
(︂
)︂]︂
49 9
7 4
5 6
+ 𝜈 2 − + 𝑐2𝑖 −
𝑐 −
𝑐
12 2
24 𝑖
24 𝑖
]︂
[︂
27
(1 + 𝑐2𝑖 )
+ 𝜋 𝑠𝑖 Δ cos 3𝜓
8
[︂
]︂
)︀
(︀
)︀
2 2
5 (︀
+
𝑠𝑖 cos 4𝜓 59 + 35 𝑐2𝑖 − 8 𝑐4𝑖 − 𝜈 131 + 59 𝑐2𝑖 − 24 𝑐4𝑖 + 5 𝜈 2 21 − 3 𝑐2𝑖 − 8 𝑐4𝑖
15
3
[︂
]︂
(︀
)︀
81
+ cos 6𝜓 − 𝑠4𝑖 (1 + 𝑐2𝑖 ) 1 − 5𝜈 + 5𝜈 2
40
[︂
(︂
)︂]︂
11 5 ln 2
7
ln 2
+ 𝑠𝑖 Δ sin 𝜓
+
+ 𝑐2𝑖
+
40
4
40
4
[︂(︂
)︂
]︂
189 27
+ 𝑠𝑖 Δ sin 3𝜓 −
+
ln(3/2) (1 + 𝑐2𝑖 ) ,
40
4

(322a)
(322b)

(322c)

(322d)

(322e)

69 Notice the obvious fact that the polarization waveforms remain invariant when we rotate by 𝜋 the separation
direction between the particles and simultaneously exchange the labels of the two particles, i.e., when we apply the
transformation (𝜓, Δ) → (𝜓 + 𝜋, −Δ). Moreover, due to the parity invariance, the 𝐻+ ’s are unchanged after the
replacement 𝑖 → 𝜋 − 𝑖, while the 𝐻× ’s being the projection of ℎTT
𝑖𝑗 on a tensorial product of two vectors of inverse
parity types, is changed into its opposite.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 127

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

127

[︂

1771 1667 2
217 4
1 6
−
𝑐𝑖 +
𝑐𝑖 −
𝑐𝑖
𝐻 + = 𝑠𝑖 Δ cos 𝜓
5120
5120
9216
9216
5/2
(︂
)︂
681
13 2
35 4
1 6
+𝜈
+
𝑐𝑖 −
𝑐𝑖 +
𝑐
256 768
768
2304 𝑖
(︂
)︂]︂
3451
673 2
5 4
1 6
2
+𝜈 −
+
𝑐 −
𝑐 −
𝑐
9216 3072 𝑖
9216 𝑖
3072 𝑖
[︂
(︂
)︂]︂
19
2 4
16 14 2
2
4
+ 𝜋 cos 2𝜓
+ 3 𝑐𝑖 − 𝑐𝑖 + 𝜈 − +
𝑐 + 2 𝑐𝑖
3
3
3
3 𝑖
[︂
3537 22977 2 15309 4
729 6
+ 𝑠𝑖 Δ cos 3𝜓
−
𝑐𝑖 −
𝑐𝑖 +
𝑐
1024
5120
5120
5120 𝑖
(︂
)︂
23829 5529 2 7749 4
729 6
+𝜈 −
+
𝑐𝑖 +
𝑐𝑖 −
𝑐
1280
1280
1280
1280 𝑖
(︂
)︂]︂
29127 27267 2 1647 4 2187 6
2
+𝜈
−
𝑐 −
𝑐 +
𝑐
5120
5120 𝑖
5120 𝑖
5120 𝑖
]︂
[︂
16𝜋
(1 + 𝑐2𝑖 ) 𝑠2𝑖 (1 − 3𝜈)
+ cos 4𝜓 −
3
[︂
108125 40625 2 83125 4 15625 6
+ 𝑠𝑖 Δ cos 5𝜓 −
+
𝑐 +
𝑐 −
𝑐
9216
9216 𝑖
9216 𝑖
9216 𝑖
(︂
)︂
8125 40625 2 48125 4 15625 6
+𝜈
−
𝑐 −
𝑐 +
𝑐
256
2304 𝑖
2304 𝑖
2304 𝑖
(︂
)︂]︂
119375 40625 2 44375 4 15625 6
2
+𝜈 −
+
𝑐 +
𝑐 −
𝑐
9216
3072 𝑖
9216 𝑖
3072 𝑖
[︂
]︂
117649 5
+ Δ cos 7𝜓
𝑠 (1 + 𝑐2𝑖 )(1 − 4𝜈 + 3𝜈 2 )
46080 𝑖
[︂
(︂
)︂]︂
9 14 2 7 4
56 2 28 4
+ sin 2𝜓 − +
𝑐 + 𝑐𝑖 + 𝜈 32 +
𝑐 −
𝑐
5
5 𝑖
5
5 𝑖
5 𝑖
(︂
)︂]︂
[︂
1193
56 32 ln 2
2
2
+ 𝑠𝑖 (1 + 𝑐𝑖 ) sin 4𝜓
−
+𝜈 −
+ 32 ln 2
,
5
3
30
[︂
(︂
)︂]︂
19
5 2
1 4
19
3 2
1 4
+
𝑐 −
𝑐 +𝜈 − +
𝑐 +
𝑐
𝐻 + = 𝜋 Δ 𝑠𝑖 cos 𝜓
64 16 𝑖
192 𝑖
96 16 𝑖
96 𝑖
3
(︂
)︂
[︂
856
2 𝜋2
428
465497
+
𝛾E −
+
ln(16 𝑥) (1 + 𝑐2𝑖 )
+ cos 2𝜓 −
11025
105
3
105
1 8
3561541 2 943 4 169 6
𝑐𝑖 −
𝑐𝑖 +
𝑐𝑖 −
𝑐𝑖
−
88200
720
720
360
(︂
)︂
2209 41𝜋 2
2039 2 3311 4 853 6
7 8
2
+𝜈
−
(1 + 𝑐𝑖 ) +
𝑐 +
𝑐 −
𝑐 +
𝑐
360
96
180 𝑖
720 𝑖
720 𝑖
360 𝑖
(︂
)︂
12871 1583 2 145 4 56 6
7 8
+ 𝜈2
−
𝑐 −
𝑐 +
𝑐 −
𝑐
540
60 𝑖
108 𝑖
45 𝑖
180 𝑖
(︂
)︂]︂
3277 19661 2 281 4
73 6
7 8
3
+𝜈 −
+
𝑐 −
𝑐 −
𝑐 +
𝑐
810
3240 𝑖
144 𝑖
720 𝑖
360 𝑖
[︂
(︂
)︂]︂
1971 135 2 243 4
567 81 2 243 4
+ 𝜋 Δ 𝑠𝑖 cos 3𝜓 −
−
𝑐 +
𝑐 +𝜈
−
𝑐 −
𝑐
128
16 𝑖
128 𝑖
64
16 𝑖
64 𝑖

(322f)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 128

128

Luc Blanchet

[︂
2189 1123 2 56 4 16 6
−
+
𝑐 +
𝑐 −
𝑐
210
210 𝑖
9 𝑖
45 𝑖
(︂
)︂
6271 1969 2 1432 4 112 6
−
𝑐 −
𝑐 +
𝑐
+𝜈
90
90 𝑖
45 𝑖
45 𝑖
(︂
)︂
(︂
)︂]︂
3007 3493 2 1568 4 224 6
161 1921 2 184 4 112 6
2
3
+𝜈 −
+
𝑐 +
𝑐 −
𝑐 +𝜈
−
𝑐 −
𝑐 +
𝑐
27
135 𝑖
45 𝑖
45 𝑖
6
90 𝑖
45 𝑖
45 𝑖
[︂
]︂
3125 𝜋 3
+ Δ cos 5𝜓
𝑠 (1 + 𝑐2𝑖 )(1 − 2𝜈)
384 𝑖
[︂
(︂
)︂
1377 891 2 729 4
7857 891 2 729 4
4
+ 𝑠𝑖 cos 6𝜓
+
𝑐 −
𝑐 +𝜈 −
−
𝑐 +
𝑐
80
80 𝑖
280 𝑖
80
16 𝑖
40 𝑖
(︂
)︂
(︂
)︂]︂
567 567 2 729 4
729 243 2 729 4
2
3
+𝜈
+
𝑐 −
𝑐 +𝜈 −
−
𝑐 +
𝑐
4
10 𝑖
20 𝑖
16
80 𝑖
40 𝑖
[︂
]︂
1024 6
𝑠 (1 + 𝑐2𝑖 )(1 − 7𝜈 + 14𝜈 2 − 7𝜈 3 )
+ cos 8𝜓 −
315 𝑖
(︂
)︂
(︂
)︂
[︂
19 ln 2
95
5 ln 2
181
ln 2
2159
−
+ −
−
𝑐2𝑖 +
+
𝑐4𝑖
+ Δ 𝑠𝑖 sin 𝜓 −
40320
32
224
8
13440
96
(︂
(︂
)︂
(︂
)︂ )︂]︂
1369 19 ln 2
41 3 ln 2
313 ln 2
+𝜈
+
+ − −
𝑐2𝑖 + −
−
𝑐4𝑖
160
48
48
8
480
48
[︂
]︂
428 𝜋
+ sin 2𝜓 −
(1 + 𝑐2𝑖 )
105
[︂
(︂
)︂
205119 1971
1917 135
+ Δ 𝑠𝑖 sin 3𝜓
−
ln(3/2) +
−
ln(3/2) 𝑐2𝑖
8960
64
224
8
)︂
(︂
43983 243
+
ln(3/2) 𝑐4𝑖
+ −
8960
64
(︂
(︂
)︂
54869 567
923 81
+𝜈 −
+
ln(3/2) + −
−
ln(3/2) 𝑐2𝑖
960
32
80
8
(︂
)︂ )︂]︂
41851 243
+
−
ln(3/2) 𝑐4𝑖
2880
32
[︂
(︂
)︂]︂
113125 3125
17639 3125
+ Δ 𝑠3𝑖 (1 + 𝑐2𝑖 ) sin 5𝜓 −
+
ln(5/2) + 𝜈
−
ln(5/2)
.
(322g)
5376
192
320
96
+ 𝑠2𝑖 cos 4𝜓

For the cross polarizations we obtain
𝐻 × = −2𝑐𝑖 sin 2𝜓 ,
0
[︂
]︂
3
9
=
𝑠
𝑐
Δ
−
sin
𝜓
+
sin
3𝜓
,
𝐻×
𝑖 𝑖
4
4
1/2
[︂
(︂
)︂]︂
17 4 2
13
2
− 𝑐𝑖 + 𝜈 − + 4 𝑐𝑖
𝐻 × = 𝑐𝑖 sin 2𝜓
3
3
3
1
[︂
]︂
8
+ 𝑐𝑖 𝑠2𝑖 sin 4𝜓 − (1 − 3𝜈) ,
3
[︂
(︂
)︂]︂
21
5 2
23
5 2
−
𝑐 +𝜈 − +
𝑐
𝐻 × = 𝑠𝑖 𝑐𝑖 Δ sin 𝜓
32 96 𝑖
48 48 𝑖
3/2
− 4𝜋 𝑐𝑖 sin 2𝜓

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(323a)
(323b)

(323c)

## PDF page 129

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

129

[︂
(︂
)︂]︂
603 135 2
171 135 2
+ 𝑠𝑖 𝑐𝑖 Δ sin 3𝜓 −
+
𝑐 +𝜈
−
𝑐
64
64 𝑖
32
32 𝑖
[︂
]︂
625
(1 − 2𝜈) 𝑠2𝑖 ,
(323d)
+ 𝑠𝑖 𝑐𝑖 Δ sin 5𝜓
192
[︂
]︂
9
3
𝐻 × = 𝑠𝑖 𝑐𝑖 Δ cos 𝜓 − − ln 2
20 2
2
[︂
]︂
189 27
+ 𝑠𝑖 𝑐𝑖 Δ cos 3𝜓
−
ln(3/2)
20
2
[︂
]︂
3𝜋
− 𝑠𝑖 𝑐𝑖 Δ
sin 𝜓
4
[︂
(︂
)︂
(︂
)︂]︂
17 113 2 1 4
143 245 2 5 4
14 35 2 5 4
2
+ 𝑐𝑖 sin 2𝜓
+
𝑐 − 𝑐𝑖 + 𝜈
−
𝑐 + 𝑐𝑖 + 𝜈 − +
𝑐 − 𝑐𝑖
15
30 𝑖
4
9
18 𝑖
4
3
6 𝑖
4
]︂
[︂
27𝜋
+ 𝑠𝑖 𝑐𝑖 Δ sin 3𝜓
4
[︂
]︂
)︀
(︀
)︀
5 (︀
4
𝑐𝑖 𝑠2𝑖 sin 4𝜓 55 − 12 𝑐2𝑖 − 𝜈 119 − 36 𝑐2𝑖 + 5 𝜈 2 17 − 12 𝑐2𝑖
+
15
3
[︂
]︂
81
+ 𝑐𝑖 sin 6𝜓 − 𝑠4𝑖 (1 − 5𝜈 + 5𝜈 2 ) ,
(323e)
20
6 2
𝐻 × = 𝑠𝑖 𝑐𝑖 𝜈
5
5/2
(︂
)︂]︂
[︂
282 94 2
22 2
𝑐𝑖 + 𝜈 −
+
𝑐𝑖
+ 𝑐𝑖 cos 2𝜓 2 −
5
5
5
(︂
)︂]︂
[︂
1193
112 64
+ 𝑐𝑖 𝑠2𝑖 cos 4𝜓 −
+
ln 2 + 𝜈
− 64 ln 2
5
3
15
[︂
913
1891 2
7 4
+ 𝑠𝑖 𝑐𝑖 Δ sin 𝜓 −
+
𝑐 −
𝑐
7680 11520 𝑖
4608 𝑖
(︂
)︂
(︂
)︂]︂
1165 235 2
7 4
1301
301 2
7 4
+𝜈
−
𝑐𝑖 +
𝑐𝑖 + 𝜈 2 −
+
𝑐𝑖 −
𝑐𝑖
384
576
1152
4608 2304
1536
(︂
[︂
)︂]︂
34 8 2
20
− 𝑐𝑖 + 𝜈 − + 8 𝑐2𝑖
+ 𝜋 𝑐𝑖 sin 2𝜓
3
3
3
[︂
12501 12069 2 1701 4
+ 𝑠𝑖 𝑐𝑖 Δ sin 3𝜓
−
𝑐 +
𝑐
2560
1280 𝑖
2560 𝑖
(︂
)︂
(︂
)︂]︂
19581 7821 2 1701 4
18903 11403 2 5103 4
+𝜈 −
+
𝑐𝑖 −
𝑐𝑖 + 𝜈 2
−
𝑐𝑖 +
𝑐𝑖
640
320
640
2560
1280
2560
[︂
]︂
32𝜋
+ 𝑠2𝑖 𝑐𝑖 sin 4𝜓 −
(1 − 3𝜈)
3
[︂
101875 6875 2 21875 4
+ Δ 𝑠𝑖 𝑐𝑖 sin 5𝜓 −
+
𝑐 −
𝑐
4608
256 𝑖
4608 𝑖
(︂
)︂
(︂
)︂]︂
66875 44375 2 21875 4
100625 83125 2 21875 4
−
𝑐𝑖 +
𝑐𝑖 + 𝜈 2 −
+
𝑐𝑖 −
𝑐𝑖
+𝜈
1152
576
1152
4608
2304
1536
[︂
]︂
(︀
)︀
117649
+ Δ 𝑠5𝑖 𝑐𝑖 sin 7𝜓
1 − 4𝜈 + 3𝜈 2 ,
(323f)
23040

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 130

130

Luc Blanchet

[︂

(︂
)︂
11617 21
251
5
+
ln 2 + −
−
ln 2 𝑐2𝑖
𝐻 × = Δ 𝑠𝑖 𝑐𝑖 cos 𝜓
20160 16
2240 48
3
(︂
(︂
)︂ )︂]︂
5
727
5
2419
−
ln 2 +
+
ln 2 𝑐2𝑖
.
+𝜈 −
240
24
240 24
[︂
]︂
856 𝜋
+ 𝑐𝑖 cos 2𝜓
105
[︂
(︂
)︂
36801 1809
65097 405
+ Δ 𝑠𝑖 𝑐𝑖 cos 3𝜓 −
+
ln(3/2) +
−
ln(3/2) 𝑐2𝑖
896
32
4480
32
(︂
(︂
)︂ )︂]︂
28445 405
7137 405
+𝜈
−
ln(3/2) + −
+
ln(3/2) 𝑐2𝑖
288
16
160
16
[︂
(︂
)︂]︂
113125 3125
17639 3125
3
+ Δ 𝑠𝑖 𝑐𝑖 cos 5𝜓
−
ln(5/2) + 𝜈 −
+
ln(5/2)
2688
96
160
48
[︂
(︂
)︂]︂
21
5 2
5 2
5
+ 𝜋 Δ 𝑠𝑖 𝑐𝑖 sin 𝜓
−
𝑐 +𝜈 − +
𝑐
32 96 𝑖
48 48 𝑖
[︂
4 𝜋2
856
3413 2 2909 4
1 6
3620761 1712
+
𝛾E −
+
ln(16 𝑥) −
𝑐 +
𝑐 −
𝑐
+ 𝑐𝑖 sin 2𝜓 −
44100
105
3
105
1260 𝑖
2520 𝑖
45 𝑖
(︂
)︂
3391 2 2287 4
7 6
743 41 𝜋 2
−
+
𝑐 −
𝑐 +
𝑐
+𝜈
90
48
180 𝑖
360 𝑖
45 𝑖
(︂
)︂
(︂
)︂]︂
7919 5426 2 382 4 14 6
6457 1109 2 281 4
7 6
2
3
+𝜈
−
𝑐 +
𝑐 −
𝑐 +𝜈 −
+
𝑐 −
𝑐 +
𝑐
270
135 𝑖
45 𝑖
45 𝑖
1620
180 𝑖
120 𝑖
45 𝑖
(︂
[︂
)︂]︂
405 405 2
1809 405 2
+
𝑐 +𝜈
−
𝑐
+ 𝜋 Δ 𝑠𝑖 𝑐𝑖 sin 3𝜓 −
64
64 𝑖
32
32 𝑖
[︂
1781 1208 2 64 4
+ 𝑠2𝑖 𝑐𝑖 sin 4𝜓 −
+
𝑐 −
𝑐
105
63 𝑖
45 𝑖
)︂
(︂
)︂
(︂
24838 2224 2 896 4
5207 536 2 448 4
2
−
𝑐 +
𝑐 +𝜈 −
+
𝑐 −
𝑐
+𝜈
45
5 𝑖
45 𝑖
135
15 𝑖
45 𝑖
(︂
)︂]︂
1703 1976 2 448 4
+𝜈 3
−
𝑐 +
𝑐
45
45 𝑖
45 𝑖
[︂
]︂
3125 𝜋 3
+ Δ sin 5𝜓
𝑠 𝑐𝑖 (1 − 2𝜈)
192 𝑖
[︂
(︂
)︂
9153 243 2
7371 243 2
+ 𝑠4𝑖 𝑐𝑖 sin 6𝜓
−
𝑐𝑖 + 𝜈 −
+
𝑐𝑖
280
35
40
5
(︂
)︂
(︂
)︂]︂
1296 486 2
3159 243 2
+𝜈 2
−
𝑐𝑖 + 𝜈 3 −
+
𝑐𝑖
5
5
40
5
[︂
]︂
2048 6
+ sin 8𝜓 −
𝑠 𝑐𝑖 (1 − 7𝜈 + 14𝜈 2 − 7𝜈 3 ) .
(323g)
315 𝑖
Notice the non-linear memory zero-frequency (DC) term present in the Newtonian plus polarization
0 𝐻+ ; see Refs. [427, 11, 189] for the computation of this term. Notice also that there is another
DC term in the 2.5PN cross polarization 5/2 𝐻× , first term in Eq. (323f).
The practical implementation of the theoretical templates in the data analysis of detectors follows from the standard matched filtering technique. The raw output of the detector 𝑜(𝑡) consists
of the superposition of the real gravitational wave signal ℎreal (𝑡) and of noise 𝑛(𝑡). The noise is
assumed to be a stationary Gaussian random variable, with zero expectation value, and with (supposedly known) frequency-dependent power spectral density 𝑆𝑛 (𝜔). The experimenters construct

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 131

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

131

the correlation between 𝑜(𝑡) and a filter 𝑞(𝑡), i.e.,
∫︁ +∞
𝑐(𝑡) =

d𝑡′ 𝑜(𝑡′ )𝑞(𝑡 + 𝑡′ ) ,

(324)

−∞

and divide 𝑐(𝑡) by the square root of its variance, or correlation noise. The expectation value of
this ratio defines the filtered signal-to-noise ratio (SNR). Looking for the useful signal ℎreal (𝑡) in
the detector’s output 𝑜(𝑡), the data analysists adopt for the filter
𝑞˜(𝜔) =

ℎ̃(𝜔)
,
𝑆𝑛 (𝜔)

(325)

where 𝑞˜(𝜔) and ℎ̃(𝜔) are the Fourier transforms of 𝑞(𝑡) and of the theoretically computed template
ℎ(𝑡). By the matched filtering theorem, the filter (325) maximizes the SNR if ℎ(𝑡) = ℎreal (𝑡). The
maximum SNR is then the best achievable with a linear filter. In practice, because of systematic
errors in the theoretical modelling, the template ℎ(𝑡) will not exactly match the real signal ℎreal (𝑡);
however if the template is to constitute a realistic representation of nature the errors will be small.
This is of course the motivation for computing high order post-Newtonian templates, in order to
reduce as much as possible the systematic errors due to the unknown post-Newtonian remainder.
To conclude, the use of theoretical templates based on the preceding 3PN/3.5PN waveforms,
and having their frequency evolution built in via the 3.5PN phase evolution (318) [recall also the
“tail-distorted” phase variable (321)], should yield some accurate detection and measurement of
the binary signals, whose inspiral phase takes place in the detector’s bandwidth [105, 106, 159, 156,
3, 18, 111]. Interestingly, it should also permit some new tests of general relativity, because we
have the possibility of checking that the observed signals do obey each of the terms of the phasing
formula (318) – particularly interesting are those terms associated with non-linear tails – exactly
as they are predicted by Einstein’s theory [84, 85, 15, 14]. Indeed, we don’t know of any other
physical systems for which it would be possible to perform such tests.

9.5

Spherical harmonic modes for numerical relativity

The spin-weighted spherical harmonic modes of the polarization waveforms have been defined in
Eq. (71). They can be evaluated either from applying the angular integration formula (72), or
alternatively from using the relations (73) – (74) giving the individual modes directly in terms of
separate contributions of the radiative moments U𝐿 and V𝐿 . The latter route is actually more
interesting [272] if some of the radiative moments are known to higher PN order than others. In
this case the comparison with the numerical calculation for these particular modes can be made
with higher post-Newtonian accuracy.
A useful fact to remember is that for non-spinning binaries, the mode ℎℓ𝑚 is entirely given by
the mass multipole moment U𝐿 when ℓ + 𝑚 is even, and by the current one V𝐿 when ℓ + 𝑚 is
odd. This is valid in general for non-spinning binaries, regardless of the orbit being quasi-circular
or elliptical. The important point is only that the motion of the two particles must be planar,
i.e., takes place in a fixed plane. This is the case if the particles are non-spinning, but this will
also be the case if, more generally, the spins are aligned or anti-aligned with the orbital angular
momentum, since there is no orbital precession in this case. Thus, for any “planar” binaries,
Eq. (73) splits to (see Ref. [197] for a proof)
𝐺
Uℓ𝑚
ℓ+2
2𝑅𝑐
𝐺
ℓ𝑚
ℎ =√
i Vℓ𝑚
2𝑅𝑐ℓ+3

ℎℓ𝑚 = − √

(when ℓ + 𝑚 is even) ,

(326a)

(when ℓ + 𝑚 is odd) .

(326b)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 132

132

Luc Blanchet

Let us factorize out in all the modes an overall coefficient including the appropriate phase
factor 𝑒−i𝑚𝜓 , where we recall that 𝜓 denotes the tail-distorted phase introduced in Eq. (321), and
such that the dominant mode with (ℓ, 𝑚) = (2, 2) conventionally starts with one at the Newtonian
order. We thus pose
√︂
2𝐺 𝑚 𝜈 𝑥 16𝜋 ℓ𝑚 −i𝑚 𝜓
ℓ𝑚
ℎ =
ℋ 𝑒
.
(327)
𝑅 𝑐2
5
We now list all the known results for ℋℓ𝑚 . We assume 𝑚 ⩾ 0; the modes having 𝑚 < 0 are easily
ℓ𝑚
deduced using ℋℓ,−𝑚 = (−)ℓ ℋ . The dominant mode ℋ22 , which is primarily important for
numerical relativity comparisons, is known at 3.5PN order and reads [74, 197]
(︂
)︂
(︂
)︂
107 55
2173 1069
2047 2
ℋ22 = 1 + 𝑥 −
+ 𝜈 + 2𝜋𝑥3/2 + 𝑥2 −
−
𝜈+
𝜈
42
42
1512
216
1512
(︂
)︂
(︂
107𝜋
34𝜋
27027409
856
428 𝜋
2𝜋 2
+ 𝑥5/2 −
− 24 i 𝜈 +
𝜈 + 𝑥3
−
𝛾E +
i+
21
21
646800
105
105
3
)︂
)︂
(︂
2
20261 2 114635 3 428
278185 41𝜋
+
𝜈−
𝜈 +
𝜈 −
ln(16𝑥)
+ −
33264
96
2772
99792
105
(︂
(︂
)︂
(︂
)︂ )︂
(︂ )︂
40𝜋 4066
1
2173𝜋
2495𝜋 14333
+ 𝑥7/2 −
+ −
+
i 𝜈+
−
i 𝜈2 + 𝒪 8 .
(328a)
756
378
162
27
945
𝑐
Similarly, we report the subdominant modes ℋ33 and ℋ31 also known at 3.5PN order [195]
√︂
[︂
(︂
)︂
(︂
[︁ 21
]︁)︂
3
15
33
1/2
3/2
2
ℋ =− i
Δ 𝑥 +𝑥
−4 + 2𝜈 + 𝑥 3𝜋 + i − + 6 ln(3/2)
4
14
5
(︂
)︂
(︂
2
123
1838𝜈
887𝜈
9𝜋𝜈
+ 𝑥5/2
−
+
+ 𝑥3 − 12𝜋 +
110
165
330
2
[︁ 84
(︁ 48103
)︁]︁)︂
+i
− 24 ln (3/2) + 𝜈 −
+ 9 ln (3/2)
5
1215
(︂
[︁ 41
]︁
19388147 492
78
3
+ 𝑥7/2
+
ln (3/2) − 18 ln2 (3/2) − 𝛾E + 𝜋 2 + 6i𝜋 −
+ 3 ln(3/2)
280280
35
7
2
35
)︂]︂
(︂ )︂
𝜈 [︁ 7055 41 2 ]︁ 318841 2 8237 3 39
1
+
+ 𝜋 −
𝜈 +
𝜈 −
ln(16𝑥) + 𝒪 8 ,
(328b)
−
8
429
8
17160
2860
7
𝑐
[︂
(︂
)︂
(︂
)︂
[︁ 7
]︁
iΔ
8 2𝜈
ℋ31 = √
𝑥1/2 + 𝑥3/2 − −
+ 𝑥2 𝜋 + i − − 2 ln 2
3
3
5
12 14
(︂
)︂
(︂
2
607
136𝜈
247𝜈
8𝜋
7𝜋𝜈
−
−
+ 𝑥3 −
−
+ 𝑥5/2
198
99
198
3
6
)︂
[︁ 56 16 ln 2
(︁
1
7 ln 2 )︁]︁
+i
+
+𝜈 −
+
15
3
15
3
(︂
[︁ 212
]︁ 26
[︁ 41
]︁
10753397
𝜋2
+ 𝑥7/2
− 2 ln 2
+ ln 2 − 𝛾E +
− 2i𝜋
+ ln 2
1513512
105
21
6
105
(︂
)︂
)︂]︂
(︂ )︂
𝜈
1738843 41 2
327059 2 17525 3 13
1
+
−
+ 𝜋 +
𝜈 −
𝜈 −
ln 𝑥 + 𝒪 8 . (328c)
8
19305
8
30888
15444
21
𝑐
The other modes are known with a precision consistent with 3PN order in the full waveform [74]:
[︂
(︂
)︂
(︂
(︂
)︂)︂
17 5𝜈
1
i
ℋ21 = Δ 𝑥1/2 + 𝑥3/2 − +
+ 𝑥2 𝜋 + i − − 2 ln 2
3
28
7
2

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 133

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

133

)︂
(︂
43
509𝜈
79𝜈 2
17𝜋 3𝜋𝜈
3
+𝑥
−
−
+
+𝑥 −
+
126
126
168
28
14
(︂
(︂
)︂
)︂ )︂]︂
(︂ )︂
17
353 3 ln 2
17 ln 2
1
(329a)
+i
+𝜈 −
−
+
+𝒪 7 ,
56
28
7
14
𝑐
(︂ )︂
5
1
ℋ20 = − √ + 𝒪 7 ,
(329b)
𝑐
14 6
√︂ [︂
(︂
)︂
(︂
(︂
)︂)︂
1 5
193 145𝜈
73𝜈 2
66𝜈
ℋ32 =
𝑥(1 − 3𝜈) + 𝑥2 −
+
−
+ 𝑥5/2 2𝜋 − 6𝜋𝜈 + i −3 +
3 7
90
18
18
5
(︂
)︂ ]︂
(︂ )︂
2
3
1451 17387𝜈
5557𝜈
5341𝜈
1
+ 𝑥3 −
(329c)
−
+
−
+𝒪 7 ,
3960
3960
220
1320
𝑐
√︂
(︂ )︂
2
6 5/2
1
30
ℋ =− i
(329d)
𝑥 𝜈+𝒪 7 ,
5
7
𝑐
√︂ [︂
(︂
)︂
8 5
593 1273𝜈
175𝜈 2
ℋ44 = −
𝑥(1 − 3𝜈) + 𝑥2 −
+
−
9 7
110
66
22
(︂
(︂
(︂
)︂
)︂)︂
42
1193
+ 𝑥5/2 4𝜋 − 12𝜋𝜈 + i − + 𝜈
− 24 ln 2 + 8 ln 2
5
40
(︂
)︂ ]︂
(︂ )︂
1068671 1088119𝜈
146879𝜈 2
226097𝜈 3
1
+ 𝑥3
−
+
−
+𝒪 7 ,
(329e)
200200
28600
2340
17160
𝑐
[︂
(︂
)︂
39 1267𝜈
131𝜈 2
9i
−
ℋ43 = − √ Δ 𝑥3/2 (1 − 2𝜈) + 𝑥5/2 − +
11
132
33
4 70
(︂
(︂
(︂
)︂
)︂)︂ ]︂
(︂ )︂
32
16301
1
+ 𝑥3 3𝜋 − 6𝜋𝜈 + i − + 𝜈
− 12 ln (3/2) + 6 ln (3/2)
+ 𝒪 7 , (329f)
5
810
𝑐
[︂
(︂
)︂
(︂
437 805𝜈
19𝜈 2
1√
+ 𝑥5/2 2𝜋 − 6𝜋𝜈
5 𝑥(1 − 3𝜈) + 𝑥2 −
+
−
ℋ42 =
63
110
66
22
)︂ )︂
(︂
)︂ ]︂
(︂ )︂
(︂
1038039 606751𝜈
400453𝜈 2
25783𝜈 3
1
21 84𝜈
+ 𝑥3
−
+
+
+𝒪 7 ,
+i − +
5
5
200200
28600
25740
17160
𝑐
(329g)
[︂
(︂
)︂
2
i
101 337𝜈
83𝜈
ℋ41 = √ Δ 𝑥3/2 (1 − 2𝜈) + 𝑥5/2 −
+
−
33
44
33
84 10
(︂
)︂)︂)︂ ]︂
(︂ )︂
(︂
(︂
1661
1
32
3
+ 4 ln 2
+𝒪 7 ,
(329h)
+ 𝑥 𝜋 − 2𝜋𝜈 + i − − 2 ln 2 + 𝜈
15
30
𝑐
(︂ )︂
1
1
√ +𝒪 7 ,
ℋ40 = −
(329i)
𝑐
504 2
)︂
[︂
(︂
256𝜈 2
625i
263 688𝜈
+
−
ℋ55 = √ Δ 𝑥3/2 (1 − 2𝜈) + 𝑥5/2 −
39
39
39
96 66
(︂
(︂
(︂
)︂
)︂)︂ ]︂
(︂ )︂
105834
1
181
3
+𝜈
− 20 ln (5/2) + 10 ln (5/2)
+𝒪 7 ,
+ 𝑥 5𝜋 − 10𝜋𝜈 + i −
14
3125
𝑐
(329j)
[︂
(︂
)︂
]︂
(︂
)︂
(︀
)︀
32
4451 3619𝜈
521𝜈 2
339𝜈 3
1
ℋ54 = − √
𝑥2 1 − 5𝜈 + 5𝜈 2 + 𝑥3 −
+
−
+
+𝒪 7 ,
910
130
13
26
𝑐
9 165
(329k)
√︂
[︂
(︂
)︂
2
3
69 464𝜈
88𝜈
9
ℋ53 = − i
Δ 𝑥3/2 (1 − 2𝜈) + 𝑥5/2 − +
−
32
110
13
39
39
5/2

(︂

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 134

134

Luc Blanchet

(︂
(︂
(︂
)︂
)︂)︂ ]︂
(︂ )︂
543
83702
1
+ 𝑥 3𝜋 − 6𝜋𝜈 + i −
+𝜈
− 12 ln (3/2) + 6 ln (3/2)
+ 𝒪 7 , (329l)
70
3645
𝑐
)︂ ]︂
(︂ )︂
[︂
(︂
(︀
)︀
2
413𝜈 2
231𝜈 3
1
3911 3079𝜈
52
2
2
3
ℋ = √
+
−
+
+𝒪 7 ,
𝑥 1 − 5𝜈 + 5𝜈 + 𝑥 −
910
130
13
26
𝑐
27 55
(329m)
[︂
(︂
)︂
2
i
179 352𝜈
4𝜈
√
ℋ51 =
Δ 𝑥3/2 (1 − 2𝜈) + 𝑥5/2 −
+
−
39
39
39
288 385
(︂
(︂
(︂
)︂)︂)︂ ]︂
(︂ )︂
181
626
1
(329n)
+ 𝑥3 𝜋 − 2𝜋𝜈 + i −
− 2 ln 2 + 𝜈
+ 4 ln 2
+𝒪 7 ,
70
5
𝑐
(︂ )︂
1
ℋ50 = 𝒪 7 ,
(329o)
𝑐
[︂
(︂
)︂ ]︂
(︂ )︂
(︀
)︀
54
113 91𝜈
39𝜈 3
1
ℋ66 = √
(329p)
𝑥2 1 − 5𝜈 + 5𝜈 2 + 𝑥3 −
+
− 64𝜈 2 +
+𝒪 7 ,
14
2
2
𝑐
5 143
[︂
]︂
(︂ )︂
3125𝑖 𝑥5/2
1
√
ℋ65 =
(329q)
Δ 1 − 4𝜈 + 3𝜈 2 + 𝒪 7 ,
𝑐
504 429
√︂ [︂
(︂
)︂ ]︂
(︂ )︂
)︀
128 2 2 (︀
93 71𝜈
19𝜈 3
1
64
2
3
2
ℋ =−
𝑥 1 − 5𝜈 + 5𝜈 + 𝑥 − +
− 44𝜈 +
+ 𝒪 7 , (329r)
495 39
14
2
2
𝑐
[︂
]︂
(︂ )︂
5/2
1
81𝑖
𝑥
√ Δ 1 − 4𝜈 + 3𝜈 2 + 𝒪 7 ,
ℋ63 = −
(329s)
𝑐
616 65
[︂
(︂
)︂ ]︂
(︂ )︂
(︀
)︀
2
81 59𝜈
7𝜈 3
1
√
ℋ62 =
𝑥2 1 − 5𝜈 + 5𝜈 2 + 𝑥3 − +
− 32𝜈 2 +
+𝒪 7 ,
(329t)
14
2
2
𝑐
297 65
[︂
]︂
(︂ )︂
1
𝑖 𝑥5/2
√ Δ 1 − 4𝜈 + 3𝜈 2 + 𝒪 7 ,
ℋ61 =
(329u)
𝑐
8316 26
(︂ )︂
1
(329v)
ℋ60 = 𝒪 7 .
𝑐
3

Notice that the modes with 𝑚 = 0 are zero except for the DC (zero-frequency) non-linear memory
contributions. We already know that this effect arises at Newtonian order [see Eq. (322a)], hence
the non zero values of the modes ℋ20 and ℋ40 . See Ref. [189] for the DC memory contributions
in the higher modes having 𝑚 = 0.
With the 3PN approximation all the modes with ℓ ⩾ 7 can be considered as merely Newtonian.
We give here the general Newtonian leading order expressions of any mode with arbitrary ℓ and
non-zero 𝑚 (see the derivation in [272]):
(︂
)︂1/2
(−)(ℓ−𝑚+2)/2
5(ℓ + 1)(ℓ + 2)(ℓ + 𝑚)!(ℓ − 𝑚)!
ℋ = ℓ+1 ℓ+𝑚 ℓ−𝑚
ℓ(ℓ − 1)(2ℓ + 1)
2 ( 2 )!( 2 )!(2ℓ − 1)!!
(︂
)︂
1
× 𝜎ℓ (𝜈) (i𝑚)ℓ 𝑥ℓ/2−1 + 𝒪 ℓ−2
(for ℓ + 𝑚 even) ,
𝑐
(︂
)︂1/2
(−)(ℓ−𝑚−1)/2
5(ℓ + 2)(2ℓ + 1)(ℓ + 𝑚)!(ℓ − 𝑚)!
ℓ𝑚
ℋ = ℓ−1 ℓ+𝑚−1 ℓ−𝑚−1
ℓ(ℓ − 1)(ℓ + 1)
2 ( 2 )!( 2 )!(2ℓ + 1)!!
(︂
)︂
1
× 𝜎ℓ+1 (𝜈) i (i𝑚)ℓ 𝑥(ℓ−1)/2 + 𝒪 ℓ−2
(for ℓ + 𝑚 odd) ,
𝑐
ℓ𝑚

in which we employ the function 𝜎ℓ (𝜈) = 𝑋2ℓ−1 + (−)ℓ 𝑋1ℓ−1 , also given by Eqs. (305).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(330a)

(330b)

## PDF page 135

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

10

135

Eccentric Compact Binaries

Inspiralling compact binaries are usually modelled as moving in quasi-circular orbits since gravitational radiation reaction circularizes the orbit towards the late stages of inspiral [340, 339], as we
discussed in Section 1.2. Nevertheless, there is an increased interest in inspiralling binaries moving
in quasi-eccentric orbits. Astrophysical scenarios currently exist which lead to binaries with nonzero eccentricity in the gravitational-wave detector bandwidth, both terrestrial and space-based.
For instance, inner binaries of hierarchical triplets undergoing Kozai oscillations [283, 300] could
not only merge due to gravitational radiation reaction but a fraction of them should have non
negligible eccentricities when they enter the sensitivity band of advanced ground based interferometers [419]. On the other hand the population of stellar mass binaries in globular clusters is
expected to have a thermal distribution of eccentricities [32]. In a study of the growth of intermediate black holes [235] in globular clusters it was found that the binaries have eccentricities between
0.1 and 0.2 in the eLISA bandwidth. Though, supermassive black hole binaries are powerful gravitational wave sources for eLISA, it is not known if they would be in quasi-circular or quasi-eccentric
orbits. If a Kozai mechanism is at work, these supermassive black hole binaries could be in highly
eccentric orbits and merge within the Hubble time [40]. Sources of the kind discussed above provide
the prime motivation for investigating higher post-Newtonian order modelling for quasi-eccentric
binaries.

10.1

Doubly periodic structure of the motion of eccentric binaries

In Section 7.3 we have given the equations of motion of non-spinning compact binary systems in
the frame of the center-of-mass for general orbits at the 3PN and even 3.5PN order. We shall
now investigate (in this section and the next one) the explicit solution to those equations. In
particular, let us discuss the general “doubly-periodic” structure of the post-Newtonian solution,
closely following Refs. [142, 143, 149].
The 3PN equations of motion admit, when neglecting the radiation reaction terms at 2.5PN
order, ten first integrals of the motion corresponding to the conservation of energy, angular momentum, linear momentum, and center of mass position. When restricted to the frame of the center
of mass, the equations admit four first integrals associated with the energy 𝐸 and the angular
momentum vector J, given in harmonic coordinates at 3PN order by Eqs. (4.8) – (4.9) of Ref. [79].
The motion takes place in the plane orthogonal to J. Denoting by 𝑟 = |𝑥| the binary’s orbital
separation in that plane, and by 𝑣 = 𝑣1 − 𝑣2 the relative velocity, we find that 𝐸 and J are
functions of 𝑟, 𝑟˙ 2 , 𝑣 2 and 𝑥 × 𝑣. We adopt polar coordinates (𝑟, 𝜑) in the orbital plane, and express
˙ The
𝐸 and the norm J = |J|, thanks to 𝑣 2 = 𝑟˙ 2 + 𝑟2 𝜑˙ 2 , as some explicit functions of 𝑟, 𝑟˙ 2 and 𝜑.
latter functions can be inverted by means of a straightforward post-Newtonian iteration to give 𝑟˙ 2
and 𝜑˙ in terms of 𝑟 and the constants of motion 𝐸 and J. Hence,
[︀
]︀
𝑟˙ 2 = ℛ 𝑟; 𝐸, J ,
(331a)
[︀
]︀
𝜑˙ = 𝒮 𝑟; 𝐸, J ,
(331b)
where ℛ and 𝒮 denote certain polynomials in 1/𝑟, the degree of which depends on the postNewtonian approximation in question; for instance it is seventh degree for both ℛ and 𝒮 at 3PN
order [312]. The various coefficients of the powers of 1/𝑟 are themselves polynomials in 𝐸 and
J, and also, of course, depend on the total mass 𝑚 and symmetric mass ratio 𝜈. In the case of
bounded elliptic-like motion, one can prove [143] that the function ℛ admits two real roots, say 𝑟p
and 𝑟a such that 𝑟p ⩽ 𝑟a , which admit some non-zero finite Newtonian limits when 𝑐 → ∞, and
represent respectively the radii of the orbit’s periastron (p) and apastron (a). The other roots are
complex and tend to zero when 𝑐 → ∞.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 136

136

Luc Blanchet

Let us consider a given binary’s orbital configuration, fully specified by some values of the
integrals of motion 𝐸 and J corresponding to quasi-elliptic motion.70 The binary’s orbital period,
or time of return to the periastron, is obtained by integrating the radial motion as
∫︁ 𝑟a
d𝑟
√︁ [︀ ]︀ .
𝑃 =2
(332)
𝑟p
ℛ 𝑟
We introduce the fractional angle (i.e., the angle divided by 2𝜋) of the advance of the periastron
per orbital revolution,
[︀ ]︀
∫︁
𝒮 𝑟
1 𝑟a
d𝑟 √︁ [︀ ]︀ ,
(333)
𝐾=
𝜋 𝑟p
ℛ 𝑟
which is such that the precession of the periastron per period is given by ΔΦ = 2𝜋(𝐾 − 1). As
𝐾 tends to one in the limit 𝑐 → ∞ (as is easily checked from the usual Newtonian solution), it is
often convenient to pose 𝑘 ≡ 𝐾 − 1, which will then entirely describe the relativistic precession.
Let us then define the mean anomaly ℓ and the mean motion 𝑛 by
ℓ ≡ 𝑛 (𝑡 − 𝑡p ) ,
2𝜋
.
𝑛≡
𝑃

(334a)
(334b)

Here 𝑡p denotes the instant of passage to the periastron. For a given value of the mean anomaly
ℓ, the orbital separation 𝑟 is obtained by inversion of the integral equation
∫︁ 𝑟
d𝑠
√︀
ℓ=𝑛
.
(335)
ℛ [𝑠]
𝑟p
This defines the function 𝑟(ℓ) which is a periodic function in ℓ with period 2𝜋. The orbital phase
𝜑 is then obtained in terms of the mean anomaly ℓ by integrating the angular motion as
∫︁
1 ℓ
d𝑙 𝒮 [𝑟(𝑙)] ,
(336)
𝜑 = 𝜑p +
𝑛 0
where 𝜑p denotes the value of the phase at the instant 𝑡p . We may define the origin of the orbital
phase at the ascending node 𝒩 with respect to some observer. In the particular case of a circular
orbit, 𝑟 = const, the phase evolves linearly with time, 𝜑˙ = 𝒮 [𝑟] = Ω, where Ω is the orbital
frequency of the circular orbit given by
Ω = 𝐾 𝑛 = (1 + 𝑘) 𝑛 .

(337)

In the general case of a non-circular orbit it is convenient to keep that definition Ω = 𝐾𝑛 and to
explicitly introduce the linearly growing part of the orbital phase (336) by writing it in the form
𝜑 = 𝜑p + Ω (𝑡 − 𝑡p ) + 𝑊 (ℓ)
= 𝜑p + 𝐾 ℓ + 𝑊 (ℓ) .

(338)

Here 𝑊 (ℓ) denotes a certain function of the mean anomaly which is periodic in ℓ with period 2𝜋,
hence periodic in time with period 𝑃 . According to Eq. (336) this function is given in terms of the
mean anomaly ℓ by
∫︁
)︀
1 ℓ (︀
d𝑙 𝒮 [𝑟(𝑙)] − Ω .
(339)
𝑊 (ℓ) =
𝑛 0
70 The dependence on 𝐸 and J will no longer be indicated but is always understood as implicit in what follows.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 137

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

137

Finally, the decomposition (338) exhibits clearly the nature of the compact binary motion, which
may be called doubly periodic in that the mean anomaly ℓ is periodic with period 2𝜋, and the
periastron advance 𝐾 ℓ is periodic with period 2𝜋 𝐾. Notice however that, though standard, the
term “doubly periodic” is misleading since the motion in physical space is not periodic in general.
The radial motion 𝑟(𝑡) is periodic with period 𝑃 while the angular motion 𝜑(𝑡) is periodic [modulo
2𝜋] with period 𝑃/𝑘 where 𝑘 = 𝐾 − 1. Only when the two periods are commensurable, i.e., when
𝑘 = 1/𝑁 where 𝑁 ∈ N, is the motion periodic in physical space (with period 𝑁 𝑃 ).

10.2

Quasi-Keplerian representation of the motion

The quasi-Keplerian (QK) representation of the motion of compact binaries is an elegant formulation of the solution of the 1PN equations of motion parametrized by the eccentric anomaly 𝑢
(entering a specific generalization of Kepler’s equation) and depending on various orbital elements,
such as three types of eccentricities. It was introduced by Damour & Deruelle [149, 150] to study
the problem of binary pulsar timing data including relativistic corrections at the 1PN order, where
the relativistic periastron precession complicates the simpler Keplerian solution.
In the QK representation the radial motion is given in standard parametric form as
𝑟 = 𝑎𝑟 (1 − 𝑒𝑟 cos 𝑢) ,

(340)

where 𝑢 is the eccentric anomaly, with 𝑎𝑟 and 𝑒𝑟 denoting two constants representing the semimajor axis of the orbit and its eccentricity. However, these constants are labelled after the radial
coordinate 𝑟 to remember that they enter (by definition) into the radial equation; in particular 𝑒𝑟
will differ from other kinds of eccentricities 𝑒𝑡 and 𝑒𝜑 . The “time” eccentricity 𝑒𝑡 enters the Kepler
equation which at the 1PN order takes the usual form
(︂ )︂
1
(341)
ℓ = 𝑢 − 𝑒𝑡 sin 𝑢 + 𝒪 4 ,
𝑐
where the mean anomaly is proportional to the time elapsed since the instant 𝑡p of passage at the
periastron, ℓ = 𝑛 (𝑡 − 𝑡p ) where 𝑛 = 2𝜋/𝑃 is the mean motion and 𝑃 is the orbital period; see
Eqs. (334). The “angular” eccentricity 𝑒𝜑 enters the equation for the angular motion at 1PN order
which is written in the form
(︂ )︂
𝜑 − 𝜑p
1
=𝑣+𝒪 4 ,
(342)
𝐾
𝑐
where the true anomaly 𝑣 is defined by71
)︂1/2
]︂
[︂(︂
𝑢
1 + 𝑒𝜑
tan
.
𝑣 ≡ 2 arctan
1 − 𝑒𝜑
2

(343)

The constant 𝐾 is the advance of periastron per orbital revolution defined by Eq. (333); it may
Φ
be written as 𝐾 = 2𝜋
where Φ is the angle of return to the periastron.
Crucial to the formalism are the explicit expressions for the orbital elements 𝑛, 𝐾, 𝑎𝑟 , 𝑒𝑟 , 𝑒𝑡
and 𝑒𝜑 in terms of the conserved energy 𝐸 and angular momentum J of the orbit. For convenience
we introduce two dimensionless parameters directly linked to 𝐸 and J by
𝜀≡−

2𝐸
,
𝜇𝑐2

(344a)

71 Comparing with Eqs. (338) we have also

𝑣 =ℓ+

𝑊 (ℓ)
+𝒪
𝐾

(︂

1
𝑐4

)︂
.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 138

138

Luc Blanchet

𝑗≡−

2𝐸 ℎ2
,
𝜇3

(344b)

where 𝜇 = 𝑚𝜈 is the reduced mass with 𝑚 the total mass (recall that 𝐸 < 0 for bound orbits) and
J
we have used the intermediate standard notation ℎ ≡ 𝐺𝑚
. The equations to follow will then appear
as expansions in powers of the small post-Newtonian parameter 𝜀 = 𝒪(1/𝑐2 ),72 with coefficients
depending on 𝑗 and the dimensionless reduced mass ratio 𝜈; notice that the parameter 𝑗 is at
Newtonian order, 𝑗 = 𝒪(1/𝑐0 ). We have [149]
{︂
(︂ )︂}︂
𝜀
1
𝜀3/2 𝑐3
,
(345a)
1 + (−15 + 𝜈) + 𝒪 4
𝑛=
𝐺𝑚
8
𝑐
(︂ )︂
3𝜀
1
𝐾 =1+
(345b)
+𝒪 4 ,
𝑗
𝑐
{︂
(︂ )︂}︂
𝐺𝑚
𝜀
1
1 + (−7 + 𝜈) + 𝒪 4
,
(345c)
𝑎𝑟 =
𝜀 𝑐2
4
𝑐
(︂
)︂
[︁
]︁
√︀
𝜀
1
𝑒𝑟 = 1 − 𝑗 + √
24 − 4𝜈 + 5𝑗(−3 + 𝜈) + 𝒪 4 ,
(345d)
𝑐
8 1−𝑗
(︂
)︂
[︁
]︁
√︀
1
𝜀
−8 + 8𝜈 + 𝑗(17 − 7𝜈) + 𝒪 4 ,
(345e)
𝑒𝑡 = 1 − 𝑗 + √
𝑐
8 1−𝑗
(︂
)︂
[︁
]︁
√︀
1
𝜀
𝑒𝜑 = 1 − 𝑗 + √
24 + 𝑗(−15 + 𝜈) + 𝒪 4 .
(345f)
𝑐
8 1−𝑗
The dependence of such relations on the coordinate system in use will be discussed later. Notice
the interesting point that there is no dependence of the mean motion 𝑛 and the radial semi-major
axis 𝑎𝑟 on the angular momentum J up to the 1PN order; such dependence will start only at 2PN
order, see e.g., Eq. (347a).
The above QK representation of the compact binary motion at 1PN order has been generalized
at the 2PN order in Refs. [170, 379, 420], and at the 3PN order by Memmesheimer, Gopakumar
& Schäfer [312]. The construction of a generalized QK representation at 3PN order exploits the
fact that the radial equation given by Eq. (331a) is a polynomial in 1/𝑟 (of seventh degree at 3PN
order). However, this is true only in coordinate systems avoiding the appearance of terms with
the logarithm ln 𝑟; the presence of logarithms in the standard harmonic (SH) coordinates at the
3PN order will obstruct the construction of the QK parametrization. Therefore Ref. [312] obtained
it in the ADM coordinate system and also in the modified harmonic (MH) coordinates, obtained
by applying the gauge transformation given in Eq. (204) on the SH coordinates. The equations
of motion in the center-of-mass frame in MH coordinates have been given in Eqs. (222); see also
Ref. [9] for details about the transformation between SH and MH coordinates.
At the 3PN order the radial equation in ADM or MH coordinates is still given by Eq. (340).
However, the Kepler equation (341) and angular equation (342) acquire extra contributions and
now become
(︂ )︂
1
ℓ = 𝑢 − 𝑒𝑡 sin 𝑢 + 𝑓𝑡 sin 𝑣 + 𝑔𝑡 (𝑣 − 𝑢) + 𝑖𝑡 sin 2𝑣 + ℎ𝑡 sin 3𝑣 + 𝒪 8 ,
(346a)
𝑐
(︂ )︂
𝜑 − 𝜑p
1
= 𝑣 + 𝑓𝜑 sin 2𝑣 + 𝑔𝜑 sin 3𝑣 + 𝑖𝜑 sin 4𝑣 + ℎ𝜑 sin 5𝑣 + 𝒪 8 ,
(346b)
𝐾
𝑐
in which the true anomaly 𝑣 is still given by Eq. (343). The new orbital elements 𝑓𝑡 , 𝑓𝜑 , 𝑔𝑡 , 𝑔𝜑 ,
𝑖𝑡 , 𝑖𝜑 , ℎ𝑡 and ℎ𝜑 parametrize the 2PN and 3PN relativistic corrections.73 All the orbital elements
72 Note that this post-Newtonian parameter 𝜀 is precisely specified by Eq. (344a), while we only intended to define
𝜖 in Eq. (1) as representing a post-Newtonian estimate.
73 More precisely, 𝑓 , 𝑓 , 𝑔 , 𝑔 are composed of 2PN and 3PN terms, but 𝑖 , 𝑖 , ℎ , ℎ start only at 3PN order.
𝑡
𝑡
𝑡 𝜑
𝑡
𝜑
𝜑
𝜑

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 139

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

139

are now to be related, similarly to Eqs. (345), to the constants 𝜀 and 𝑗 with 3PN accuracy in a
given coordinate system. Let us make clear that in different coordinate systems such as MH and
ADM coordinates, the QK representation takes exactly the same form as given by Eqs. (340) and
(346). But, the relations linking the various orbital elements 𝑎𝑟 , 𝑒𝑟 , 𝑒𝑡 , 𝑒𝜑 , 𝑓𝑡 , 𝑓𝜑 , . . . to 𝐸 and J
or 𝜀 and 𝑗, are different, with the notable exceptions of 𝑛 and 𝐾.
Indeed, an important point related to the use of gauge invariant variables in the elliptical orbit
case is that the functional forms of the mean motion 𝑛 and periastron advance 𝐾 in terms of the
gauge invariant variables 𝜀 and 𝑗 are identical in different coordinate systems like the MH and
ADM coordinates [170]. Their explicit expressions at 3PN order read
{︂
[︂
]︂
𝜀
𝜀2
192
𝜀3/2 𝑐3
2
1 + (−15 + 𝜈) +
555 + 30 𝜈 + 11 𝜈 + 1/2 (−5 + 2 𝜈)
𝑛=
𝐺𝑚
8
128
𝑗
(︂
)︂
[︂
3
𝜀
5760
2
2
3
+
−29385 − 4995 𝜈 − 315 𝜈 + 135 𝜈 + 1/2 17 − 9 𝜈 + 2 𝜈
3072
𝑗
(︂
)︂]︂
(︂ )︂ }︂
16
1
2
2
+ 3/2 − 10080 + (13952 − 123𝜋 )𝜈 − 1440𝜈
+𝒪 8
.
(347a)
𝑐
𝑗
]︂
[︂
3𝜀 𝜀2 3
15
𝐾 =1+
+
(−5 + 2 𝜈) + 2 (7 − 2 𝜈)
𝑗
4 𝑗
𝑗
[︂
(︂
)︂
3
𝜀
24
1
2
2
2
+
(5 − 5𝜈 + 4𝜈 ) + 2 −10080 + (13952 − 123𝜋 )𝜈 − 1440𝜈
128 𝑗
𝑗
(︂
)︂]︂
(︂ )︂
5
1
2
2
+ 3 7392 + (−8000 + 123𝜋 )𝜈 + 336𝜈
+𝒪 8 .
(347b)
𝑗
𝑐
Because of their gauge invariant meaning, it is natural to use 𝑛 and 𝐾 as two independent gaugeinvariant variables in the general orbit case. Actually, instead of working with the mean motion 𝑛
it is often preferable to use the orbital frequency Ω which has been defined for general quasi-elliptic
orbits in Eq. (337). Moreover we can pose
(︂
𝑥=

𝐺𝑚Ω
𝑐3

)︂2/3
(with Ω = 𝐾𝑛) ,

(348)

which constitutes the obvious generalization of the gauge invariant variable 𝑥 used in the circular
orbit case. The use of 𝑥 as an independent parameter will thus facilitate the straightforward
reading out and check of the circular orbit limit. The parameter 𝑥 is related to the energy and
angular momentum variables 𝜀 and 𝑗 up to 3PN order by
[︂
]︂
𝑥
5
1
2
=1+𝜀 − + 𝜈+
(349)
𝜀
4 12
𝑗
[︂
(︂
)︂
(︂
)︂]︂
5
5
1
1
1
7
1 33
+ 𝜀2
+ 𝜈 + 𝜈 2 + 1/2 (−5 + 2𝜈) +
−5 + 𝜈 + 2
− 5𝜈
2 24
18
𝑗
6
𝑗
2
𝑗
[︂
(︂
)︂
235 25
25 2
35 3 1 35 5
25
+ 𝜀3 −
− 𝜈−
𝜈 +
𝜈 +
− 𝜈 + 𝜈2
48
24
576
1296
𝑗 4
3
36
)︂
)︂
)︂
(︂
(︂
(︂
1
29
1
145 235
472 41 2
+ 1/2
−
𝜈 + 𝜈 2 + 3/2 −45 +
− 𝜋 𝜈 − 5𝜈 2
8
24
12
9
96
𝑗
𝑗
(︂
(︂
)︂
)︂
1
565
1903 41 2
95
+ 2 −
+
− 𝜋 𝜈 − 𝜈2
𝑗
8
24
64
12
(︂
(︂
)︂
)︂]︂
(︂ )︂
1 529
610 205 2
35
1
+ 3
+ −
+
𝜋 𝜈 + 𝜈2
+𝒪 8 .
𝑗
3
3
64
4
𝑐

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 140

140

Luc Blanchet

Besides the very useful gauge-invariant quantities 𝑛, 𝐾 and 𝑥, the other orbital elements 𝑎𝑟 , 𝑒𝑟 ,
𝑒𝑡 , 𝑒𝜑 , 𝑓𝑡 , 𝑔𝑡 , 𝑖𝑡 , ℎ𝑡 , 𝑓𝜑 , 𝑔𝜑 , 𝑖𝜑 , ℎ𝜑 parametrizing Eqs. (340) and (346) are not gauge invariant; their
expressions in terms of 𝜀 and 𝑗 depend on the coordinate system in use. We refer to Refs. [312, 9]
for the full expressions of all the orbital elements at 3PN order in both MH and ADM coordinate
systems. Here, for future use, we only give the expression of the time eccentricity 𝑒𝑡 (squared) in
MH coordinates:
[︂
]︂
𝜀
2
−8 + 8𝜈 + 𝑗(17 − 7𝜈)
(350)
𝑒𝑡 = 1 − 𝑗 +
4
[︂
𝜀2
+
12 + 72𝜈 + 20𝜈 2 + 𝑗(−112 + 47𝜈 − 16𝜈 2 ) + 24𝑗 1/2 (5 − 2𝜈)
8
]︂
16
24
+ (4 − 7𝜈) + 1/2 (−5 + 2 𝜈)
𝑗
𝑗
[︂
(︂
)︂
3
𝜀
2
3
2
3
+
23520 − 464800𝜈 + 179760𝜈 + 16800𝜈 + 525 𝑗 528 − 200𝜈 + 77𝜈 − 24𝜈
6720
(︂
)︂
6
1/2
2
2
2
+ 2520𝑗 (−265 + 193 𝜈 − 46 𝜈 ) +
− 73920 + (260272 − 4305𝜋 )𝜈 − 61040𝜈
𝑗
(︂
)︂
70
2
2
+ 1/2 16380 + (−19964 + 123𝜋 )𝜈 + 3240 𝜈
𝑗
(︂
)︂
70
2
2
+ 3/2 − 10080 + (13952 − 123𝜋 )𝜈 − 1440𝜈
𝑗
(︂
)︂]︂
(︂ )︂
8
1
2
2
+ 2 53760 + (−176024 + 4305𝜋 )𝜈 + 15120𝜈
+𝒪 8 .
𝑗
𝑐
Again, with our notation (344), this appears as a post-Newtonian expansion in the small parameter
𝜀 → 0 with fixed “Newtonian” parameter 𝑗.
In the case of a circular orbit, the angular momentum variable, say 𝑗circ , is related to the
constant of energy 𝜀 by the 3PN gauge-invariant expansion
(︂
[︂
]︂
)︂ (︂
)︂
(︂
)︂
(︂ )︂
9 𝜈
𝜈2
7699 41 2
𝜈2
𝜈3
81
945
1
2
3
𝑗circ = 1+
+
𝜀+
− 2𝜈 +
𝜀 +
+ −
+ 𝜋 𝜈+
+
𝜀 +𝒪 8 .
4 4
16
16
64
192
32
2
64
𝑐
This permits to reduce various quantities to circular orbits, for instance, the periastron advance is
found to be well defined in the limiting case of a circular orbit, and is given at 3PN order in terms
of the PN parameter (230) [or (348)] by
]︂
)︂
(︂ )︂
(︂
)︂
(︂
[︂
1
27
135
649 123 2
− 7𝜈 𝑥2 +
+ −
+
𝜋 𝜈 + 7𝜈 2 𝑥3 + 𝒪 8 .
𝐾circ = 1 + 3𝑥 +
2
2
4
32
𝑐
See Ref. [291] for a comparison between the PN prediction for the periastron advance of circular
orbits and numerical calculations based on self-force theory in the small mass ratio limit.

10.3

Averaged energy and angular momentum fluxes

The gravitational wave energy and angular momentum fluxes from a system of two point masses
in elliptic motion was first computed by Peters & Mathews [340, 339] at Newtonian level. The
1PN and 1.5PN corrections to the fluxes were provided in Refs. [416, 86, 267, 87, 366] and used
to study the associated secular evolution of orbital elements under gravitational radiation reaction
using the QK representation of the binary’s orbit at 1PN order [149]. These results were extended
to 2PN order in Refs. [224, 225] for the instantaneous terms (leaving aside the tails) using the

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 141

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

141

generalized QK representation [170, 379, 420]; the energy flux and waveform were in agreement
with those of Ref. [424] obtained using a different method. Arun et al. [10, 9, 12] have fully
generalized the results at 3PN order, including all tails and related hereditary contributions, by
computing the averaged energy and angular momentum fluxes for quasi-elliptical orbits using the
QK representation at 3PN order [312], and deriving the secular evolution of the orbital elements
under 3PN gravitational radiation reaction.74
The secular evolution of orbital elements under gravitational radiation reaction is in principle
only the starting point for constructing templates for eccentric binary orbits. To go beyond the
secular evolution one needs to include in the evolution of the orbital elements, besides the averaged
contributions in the fluxes, the terms rapidly oscillating at the orbital period. An analytic approach,
based on an improved method of variation of constants, has been discussed in Ref. [153] for dealing
with this issue at the leading 2.5PN radiation reaction order.
The generalized QK representation of the motion discussed in Section 10.2 plays a crucial
role in the procedure of averaging the energy and angular momentum fluxes ℱ and 𝒢𝑖 over one
orbit.75 Actually the averaging procedure applies to the “instantaneous” parts of the fluxes,
while the “hereditary” parts are treated separately for technical reasons [10, 9, 12]. Following the
decomposition (308) we pose ℱ = ℱinst + ℱhered where the hereditary part of the energy flux is
composed of tails and tail-of-tails. For the angular momentum flux one needs also to include a
contribution from the memory effect [12]. We thus have to compute for the instantaneous part
⟨ ℱinst ⟩ =

1
𝑃

∫︁ 𝑃
d𝑡 ℱinst =
0

1
2𝜋

∫︁ 2𝜋
d𝑢
0

dℓ
ℱinst ,
d𝑢

(351)

and similarly for the instantaneous part of the angular momentum flux 𝒢𝑖 .
Thanks to the QK representation, we can express ℱinst , which is initially a function of the
natural variables 𝑟, 𝑟˙ and 𝑣 2 , as a function of the varying eccentric anomaly 𝑢, and depending on
two constants: The frequency-related parameter 𝑥 defined by (348), and the “time” eccentricity 𝑒𝑡
given by (350). To do so one must select a particular coordinate system – the MH coordinates for
instance. The choice of 𝑒𝑡 rather than 𝑒𝑟 (say) is a matter of convenience; since 𝑒𝑡 appears in the
Kepler-like equation (346a) at leading order, it will directly be dealt with when averaging over one
orbit. We note that in the expression of the energy flux at the 3PN order there are some logarithmic
terms of the type ln(𝑟/𝑟0 ) even in MH coordinates. Indeed, as we have seen in Section 7.3, the
MH coordinates permit the removal of the logarithms ln(𝑟/𝑟0′ ) in the equations of motion, where
𝑟0′ is the UV scale associated with Hadamard’s self-field regularization [see Eq. (221)]; however
there are still some logarithms ln(𝑟/𝑟0 ) which involve the IR constant 𝑟0 entering the definition of
the multipole moments for general sources, see Theorem 6 where the finite part ℱ𝒫 contains the
regularization factor (42). As a result we find that the general structure of ℱinst (and similarly for
𝒢inst , the norm of the angular momentum flux) consists of a finite sum of terms of the type
ℱinst =

d𝑢 ∑︁ 𝛼𝑙 (𝑥, 𝑒𝑡 ) + 𝛽𝑙 (𝑥, 𝑒𝑡 ) sin 𝑢 + 𝛾𝑙 (𝑥, 𝑒𝑡 ) ln(1 − 𝑒𝑡 cos 𝑢)
.
dℓ
(1 − 𝑒𝑡 cos 𝑢)𝑙+1

(352)

𝑙

The factor d𝑢/dℓ has been inserted to prepare for the orbital average (351). The coefficients 𝛼𝑙 ,
𝛽𝑙 and 𝛾𝑙 are straightforwardly computed using the QK parametrization as functions of 𝑥 and
the time eccentricity 𝑒𝑡 . The 𝛽𝑙 ’s correspond to 2.5PN radiation-reaction terms and will play no
role, while the 𝛾𝑙 ’s correspond to the logarithmic terms ln(𝑟/𝑟0 ) arising at the 3PN order. For
74 On the other hand, for the computation of the gravitational waveform of eccentric binary orbits up to the 2PN
order in the Fourier domain, see Refs. [401, 402].
75 Recall that the fluxes are defined in a general way, for any matter system, in terms of the radiative multipole
moments by the expressions (68).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 142

142

Luc Blanchet

convenience the dependence on the constant ln 𝑟0 has been included into the coefficients 𝛼𝑙 ’s. To
compute the average we dispose of the following integration formulas (𝑙 ∈ N)76
∫︁ 2𝜋
d𝑢
sin 𝑢
= 0,
(353a)
𝑙+1
2𝜋
(1
−
𝑒
𝑡 cos 𝑢)
0
[︂
]︂)︂⃒
(︂
∫︁ 2𝜋
⃒
d𝑢
(−)𝑙 d𝑙
1
1
⃒
√︀
,
(353b)
=
⃒
𝑙+1
𝑙
2
2
2𝜋
(1
−
𝑒
cos
𝑢)
𝑙!
d𝑧
𝑡
𝑧 − 𝑒𝑡
0
𝑧=1
[︂
]︂)︂⃒
(︂
∫︁ 2𝜋
⃒
d𝑢 ln(1 − 𝑒𝑡 cos 𝑢)
(−)𝑙 d𝑙 𝑍(𝑧, 𝑒𝑡 )
⃒
√︀
.
(353c)
=
𝑙+1
𝑙
2𝜋 (1 − 𝑒𝑡 cos 𝑢)
𝑙!
d𝑧
𝑧 2 − 𝑒2 ⃒
0

𝑧=1

𝑡

In the right-hand sides of Eqs. (353b) and (353c) we have to differentiate 𝑙 times with respect to
the intermediate variable 𝑧 before applying 𝑧 = 1. The equation (353c), necessary for dealing with
the logarithmic terms, contains the not so trivial function
√︀
]︂
[︂ √︀
]︂
[︂
1 − 𝑒2𝑡 + 1
1 − 𝑒2𝑡 − 1
√︀
𝑍(𝑧, 𝑒𝑡 ) = ln
+ 2 ln 1 +
.
(354)
2
𝑧 + 𝑧 2 − 𝑒2𝑡
From Eq. (353a) we see that there will be no radiation-reaction terms at 2.5PN order in the final
result; the 2.5PN contribution is proportional to 𝑟˙ and vanishes after averaging since it involves
only odd functions of 𝑢.
Finally, after implementing all the above integrations, the averaged instantaneous energy flux
in MH coordinates at the 3PN order is obtained in the form [9]
⟨ ℱinst ⟩ =

)︁
32𝑐5 2 5 (︁
𝜈 𝑥 ℐ0 + 𝑥 ℐ1 + 𝑥2 ℐ2 + 𝑥3 ℐ3 ,
5𝐺

(355)

where we recall that the post-Newtonian parameter 𝑥 is defined by (348). The various instantaneous
post-Newtonian pieces depend on the symmetric mass ratio 𝜈 and the time eccentricity 𝑒𝑡 in MH
coordinates as
{︂
}︂
73 2 37 4
1
1+
ℐ0 =
𝑒 +
𝑒 ,
(356a)
24 𝑡 96 𝑡
(1 − 𝑒2𝑡 )7/2
(︂
)︂
{︂
10475 1081
1
1247 35
− 𝜈 + 𝑒2𝑡
−
𝜈
(356b)
ℐ1 =
−
2
9/2
336
12
672
36
(1 − 𝑒𝑡 )
)︂
)︂}︂
(︂
(︂
10043 311
2179 851
+𝑒4𝑡
−
𝜈 + 𝑒6𝑡
−
𝜈
,
384
12
1792 576
{︂
1
203471 12799
65
ℐ2 =
−
+
𝜈 + 𝜈2
(356c)
9072
504
18
(1 − 𝑒2𝑡 )11/2
(︂
)︂
(︂
)︂
3807197 116789
5935 2
268447 2465027
247805 2
+𝑒2𝑡 −
+
𝜈+
𝜈 +𝑒4𝑡 −
−
𝜈+
𝜈
18144
2016
54
24192
8064
864
(︂
)︂
(︂
)︂
1307105 416945
185305 2
86567 9769
21275 2
+𝑒6𝑡
−
𝜈+
𝜈 +𝑒8𝑡
−
𝜈+
𝜈
16128
2688
1728
64512 4608
6912
[︂
(︂
)︂
√︁
35
6425 1285
+ 1 − 𝑒2𝑡
− 7𝜈 + 𝑒2𝑡
−
𝜈
2
48
24
76 The second of these formulas can alternatively be written with the standard Legendre polynomial 𝑃

∫︁ 2𝜋
0

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(︂

d𝑢
1
1
1
=
𝑃𝑙 √︁
𝑙+1
2𝜋 (1 − 𝑒𝑡 cos 𝑢)𝑙+1
(1 − 𝑒2𝑡 ) 2
1 − 𝑒2𝑡

)︂
.

𝑙 as

## PDF page 143

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

143

(︂

)︂
)︂]︂}︂
(︂
5065 1013
185 37
6
−
𝜈 + 𝑒𝑡
− 𝜈
,
64
32
96
48
{︂
[︂
]︂
1
2193295679
8009293 41𝜋 2
209063 2 775 3
ℐ3 =
+
−
𝜈−
𝜈 −
𝜈
(356d)
9979200
54432
64
3024
324
(1 − 𝑒2𝑡 )13/2
(︂
[︂
]︂
)︂
20506331429
649801883 4879𝜋 2
3008759 2 53696 3
+𝑒2𝑡
+
+
𝜈−
𝜈 −
𝜈
19958400
272160
1536
3024
243
(︂
[︂
]︂
)︂
3611354071
755536297 29971𝜋 2
179375 2 10816087 3
4
+𝑒𝑡 −
+
−
𝜈−
𝜈 −
𝜈
13305600
136080
1024
576
7776
(︂
[︂
]︂
)︂
1108811471 84501𝜋 2
87787969 2 983251 3
4786812253
6
+𝑒𝑡
+
−
𝜈+
𝜈 −
𝜈
26611200
1451520
4096
48384
648
(︂
[︂
]︂
)︂
21505140101
32467919 4059𝜋 2
79938097 2 4586539 3
+𝑒8𝑡
+ −
−
𝜈+
𝜈 −
𝜈
141926400
129024
4096
193536
15552
(︂
)︂
9287
8977
8977637
567617
+
𝜈+
𝜈2 −
𝜈3
+𝑒10
−
𝑡
11354112 48384
55296
124416
[︂
]︂
[︂
√︁
165761 287𝜋 2
455 2
14047483
+ −
+
𝜈+
𝜈
+ 1 − 𝑒2𝑡 −
151200
1008
192
12
(︂
[︂
)︂
]︂
36863231
14935421 52685𝜋 2
43559 2
+ 𝑒2𝑡
+ −
+
𝜈
𝜈+
100800
6048
4608
72
[︂
)︂
(︂
]︂
2
759524951
31082483 41533𝜋
303985 2
+ 𝑒4𝑡
+ −
+
𝜈
𝜈+
403200
8064
6144
288
(︂
[︂
]︂
)︂
2
1399661203
40922933 1517𝜋
73357 2
+ 𝑒6𝑡
+ −
+
𝜈+
𝜈
2419200
48384
9216
288
)︂]︂
(︂
407 2
185 1073
+ 𝑒8𝑡
−
𝜈+
𝜈
48
288
288
]︃}︃
√︀
(︂
)︂ [︃
1712 14552 2 553297 4 187357 6 10593 8
𝑥 1 + 1 − 𝑒2𝑡
.
+
+
𝑒 +
𝑒 +
𝑒 +
𝑒 ln
105
63 𝑡
1260 𝑡
1260 𝑡
2240 𝑡
𝑥0 2(1 − 𝑒2𝑡 )
+𝑒4𝑡

The Newtonian coefficient ℐ0 is nothing but the Peters & Mathews [340] enhancement function
of eccentricity that enters in the orbital gravitational radiation decay of the binary pulsar; see
Eq. (11). For ease of presentation we did not add a label on 𝑒𝑡 to indicate that it is the time
eccentricity in MH coordinates; such MH-coordinates 𝑒𝑡 is given by Eq. (350). Recall that on the
contrary 𝑥 is gauge invariant, so no such label is required on it.
The last term in the 3PN coefficient is proportional to some logarithm which directly arises
from the integration formula (353c). Inside the logarithm we have posed
𝑥0 ≡

𝐺𝑚
,
𝑐2 𝑟0

(357)

exhibiting an explicit dependence upon the arbitrary length scale 𝑟0 ; we recall that 𝑟0 was introduced in the formalism through Eq. (42). Only after adding the hereditary contribution to the
3PN energy flux can we check the required cancellation of the constant 𝑥0 . The hereditary part is
made of tails and tails-of-tails, and is of the form
)︁
32𝑐5 2 5 (︁ 3/2
⟨ ℱhered ⟩ =
𝜈 𝑥 𝑥 𝒦3/2 + 𝑥5/2 𝒦5/2 + 𝑥3 𝒦3 ,
(358)
5𝐺
where the post-Newtonian pieces, only at the 1.5PN, 2.5PN and 3PN orders, read [10]
𝒦3/2 = 4𝜋 𝜙(𝑒𝑡 ) ,

(359a)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 144

144

Luc Blanchet

8191
583
𝜋 𝜓(𝑒𝑡 ) −
𝜈 𝜋 𝜁(𝑒𝑡 ) ,
672
24
[︂
(︂ 3/2 )︂]︂
116761
16 2 1712
1712
4𝑥
𝒦3 = −
𝜅(𝑒𝑡 ) +
𝜋 −
𝛾E −
ln
𝐹 (𝑒𝑡 ) ,
3675
3
105
105
𝑥0

𝒦5/2 = −

(359b)
(359c)

where 𝜙(𝑒𝑡 ), 𝜓(𝑒𝑡 ), 𝜁(𝑒𝑡 ), 𝜅(𝑒𝑡 ) and 𝐹 (𝑒𝑡 ) are certain “enhancement” functions of the eccentricity.
Among them the four functions 𝜙(𝑒𝑡 ), 𝜓(𝑒𝑡 ), 𝜁(𝑒𝑡 ) and 𝜅(𝑒𝑡 ) appearing in Eqs. (359) do not
admit analytic closed-form expressions. They have been obtained in Refs. [10] (extending Ref. [87])
in the form of infinite series made out of quadratic products of Bessel functions. Numerical plots
of these four enhancement factors as functions of eccentricity 𝑒𝑡 have been provided in Ref. [10];
we give in Figure 3 the graph of the function 𝜙(𝑒𝑡 ) which enters the dominant 1.5PN tail term in
Eq. (358).

3

6x10

40

40

20

20

3

4x10

(e)
3

2x10

0

0

0.0

0.2

0.4

0.6

0.0

0.2

0.4

0.6

0
0.8

1.0

e

Figure 3: Variation of the enhancement factor 𝜙(𝑒) with the eccentricity 𝑒. This function agrees with the
numerical calculation of Ref. [87] modulo a trivial rescaling with the Peters–Mathews function (356a). The
inset graph is a zoom of the function at a smaller scale. The dots represent the numerical computation
and the solid line is a fit to the numerical points. In the circular orbit limit we have 𝜙(0) = 1.

Furthermore their leading correction term 𝑒2𝑡 in the limit of small eccentricity 𝑒𝑡 ≪ 1 can be
obtained analytically as [10]
(︀ )︀
2335 2
𝑒𝑡 + 𝒪 𝑒4𝑡 ,
192
(︀ )︀
22988 2
𝜓 (𝑒𝑡 ) = 1 −
𝑒𝑡 + 𝒪 𝑒4𝑡 ,
8191
(︀ )︀
1011565 2
𝜁 (𝑒𝑡 ) = 1 +
𝑒𝑡 + 𝒪 𝑒4𝑡 ,
(︂48972
)︂
(︀ )︀
62 4613840
24570945
𝜅 (𝑒𝑡 ) = 1 +
−
ln 2 +
ln 3 𝑒2𝑡 + 𝒪 𝑒4𝑡 .
3
350283
1868176
𝜙 (𝑒𝑡 ) = 1 +

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(360a)
(360b)
(360c)
(360d)

## PDF page 145

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

145

On the other hand the function 𝐹 (𝑒𝑡 ) in factor of the logarithm in the 3PN piece does admit some
closed analytic form:
[︂
]︂
85 2 5171 4 1751 6
1
297 8
1 + 𝑒𝑡 +
𝐹 (𝑒𝑡 ) =
𝑒 +
𝑒 +
𝑒 .
(361)
6
192 𝑡
192 𝑡 1024 𝑡
(1 − 𝑒2𝑡 )13/2
The latter analytical result is very important for checking that the arbitrary constant 𝑥0 disappears from the final result. Indeed we immediately verify from comparing the last term in
Eq. (356d) with Eq. (359c) that 𝑥0 cancels out from the sum of the instantaneous and hereditary
contributions in the 3PN energy flux. This fact was already observed for the circular orbit case in
Ref. [81]; see also the discussions around Eqs. (93) – (94) and at the end of Section 4.2.
Finally we can check that the correct circular orbit limit, which is given by Eq. (314), is
recovered from the sum ⟨ℱinst ⟩ + ⟨ℱhered ⟩. The next correction of order 𝑒2𝑡 when 𝑒𝑡 → 0 can
be deduced from Eqs. (360) – (361) in analytic form; having the flux in analytic form may be
useful for studying the gravitational waves from binary black hole systems with moderately high
eccentricities, such as those formed in globular clusters [235].
Previously the averaged energy flux was represented using 𝑥 – the gauge invariant variable (348)
– and the time eccentricity 𝑒𝑡 which however is gauge dependent. Of course it is possible to provide
a fully gauge invariant formulation of the energy flux. The most natural choice is to express the
result in terms of the conserved energy 𝐸 and angular momentum J, or, rather, in terms of the
pair of rescaled variables (𝜀, 𝑗) defined by Eqs. (344). To this end it suffices to replace 𝑒𝑡 by its
MH-coordinate expression (350) and to use Eq. (349) to re-express 𝑥 in terms of 𝜀 and 𝑗. However,
there are other possible choices for a couple of gauge invariant quantities. As we have seen the
mean motion 𝑛 and the periastron precession 𝐾 are separately gauge invariant so we may define
the pair of variables (𝑥, 𝜄), where 𝑥 is given by (348) and we pose
𝜄≡

3𝑥
.
𝐾 −1

(362)

Such choice would be motivated by the fact that 𝜄 reduces to the angular-momentum related
variable 𝑗 in the limit 𝜀 → 0. Note however that with the latter choices (𝜀, 𝑗) or (𝑥, 𝜄) of gaugeinvariant variables, the circular-orbit limit is not directly readable from the result; this is why we
have preferred to present it in terms of the gauge dependent couple of variables (𝑥, 𝑒𝑡 ).
As we are interested in the phasing of binaries moving in quasi-eccentric orbits in the adiabatic
approximation, we require the orbital averages not only of the energy flux ℱ but also of the
angular momentum flux 𝒢𝑖 . Since the quasi-Keplerian orbit is planar, we only need to average
the magnitude 𝒢 of the angular momentum flux. The complete computation thus becomes a
generalisation of the previous computation of the averaged energy flux requiring similar steps (see
Ref. [12]): The angular momentum flux is split into instantaneous 𝒢inst and hereditary 𝒢hered
contributions; the instantaneous part is averaged using the QK representation in either MH or
ADM coordinates; the hereditary part is evaluated separately and defined by means of several
types of enhancement functions of the time eccentricity 𝑒𝑡 ; finally these are obtained numerically
as well as analytically to next-to-leading order 𝑒2𝑡 . At this stage we dispose of both the averaged
energy and angular momentum fluxes ⟨ℱ⟩ and ⟨𝒢⟩.
The procedure to compute the secular evolution of the orbital elements under gravitational
radiation-reaction is straightforward. Differentiating the orbital elements with respect to time, and
using the heuristic balance equations, we equate the decreases of energy and angular momentum to
the corresponding averaged fluxes ⟨ℱ⟩ and ⟨𝒢⟩ at 3PN order [12]. This extends earlier analyses at
previous orders: Newtonian [339] as we have reviewed in Section 1.2; 1PN [86, 267]; 1.5PN [87, 366]
and 2PN [224, 153]. Let us take the example of the mean motion 𝑛. From Eq. (347a) together with
the definitions (344) we know the function 𝑛(𝐸, J) at 3PN order, where 𝐸 and J are the orbit’s

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 146

146

Luc Blanchet

constant energy and angular momentum. Thus,
d𝑛
𝜕𝑛 d𝐸
𝜕𝑛 dJ
=
+
.
d𝑡
𝜕𝐸 d𝑡
𝜕J d𝑡

(363)

The usual balance equations for energy and angular momentum
d𝐸
⟩ = −⟨ℱ⟩ ,
d𝑡
dJ
⟨ ⟩ = −⟨𝒢⟩ ,
d𝑡

⟨

(364a)
(364b)

have already been used at Newtonian order in Eqs. (9). Although heuristically assumed at 3PN
order, they have been proved through 1.5PN order in Section 5.4. With the averaged fluxes known
through 3PN order, we obtain the 3PN averaged evolution equation as
⟨

d𝑛
𝜕𝑛
𝜕𝑛
⟩=−
⟨ℱ⟩ −
⟨𝒢⟩ .
d𝑡
𝜕𝐸
𝜕J

(365)

We recall that this gives only the slow secular evolution under gravitational radiation reaction for
eccentric orbits. The complete evolution includes also, superimposed on the averaged adiabatic
evolution, some fast but smaller post-adiabatic oscillations at the orbital time scale [153, 279].

11

Spinning Compact Binaries

The post-Newtonian templates have been developed so far for compact binary systems which can
be described with great precision by point masses without spins. Here by spin, we mean the
intrinsic (classical ) angular momentum 𝑆 of the individual compact body. However, including
the effects of spins is essential, as the astrophysical evidence indicates that stellar-mass black
holes [2, 390, 311, 227, 323] and supermassive black holes [188, 101, 102] (see Ref. [364] for a
review) can be generically close to maximally spinning. The presence of spins crucially affects the
dynamics of the binary, in particular leading to orbital plane precession if they are not aligned
with the orbital angular momentum (see for instance [138, 8]), and thereby to strong modulations
in the observed signal frequency and phase.
In recent years an important effort has been undertaken to compute spin effects to high postNewtonian order in the dynamics and gravitational radiation of compact binaries:
1. Dynamics. The goal is to obtain the equations of motion and related conserved integrals of
the motion, the equations of precession of the spins, and the post-Newtonian metric in the
near zone. For this step we need a formulation of the dynamics of particles with spins (either
Lagrangian or Hamiltonian);
2. Radiation. The mass and current radiative multipole moments, including tails and all hereditary effects, are to be computed. One then deduces the gravitational waveform and the
fluxes, from which we compute the secular evolution of the orbital phase. This step requires
plugging the previous dynamics into the general wave generation formalism of Part A.
We adopt a particular post-Newtonian counting for spin effects that actually refers to maximally
spinning black holes. In this convention the two spin variables 𝑆a (a = 1, 2) have the dimension of
an angular momentum multiplied by a factor 𝑐, and we pose
𝑆a = 𝐺 𝑚2a 𝜒a ,

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(366)

## PDF page 147

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

147

where 𝑚a is the mass of the compact body, and 𝜒a is the dimensionless spin parameter, which
equals one for maximally spinning Kerr black holes. Thus the spins 𝑆a of the compact bodies can
be considered as “Newtonian” quantities [there are no 𝑐’s in Eq. (366)], and all spin effects will
carry (at least) an explicit 1/𝑐 factor with respect to non-spin effects. With this convention any
post-Newtonian estimate is expected to be appropriate (i.e., numerically correct) in the case of
maximal rotation. One should keep in mind that spin effects will be formally a factor 1/𝑐 smaller
for non-maximally spinning objects such as neutron stars; thus in this case a given post-Newtonian
computation will actually be a factor 1/𝑐 more accurate.
As usual we shall make a distinction between spin-orbit (SO) effects, which are linear in the
spins, and spin-spin (SS) ones, which are quadratic. In this article we shall especially review the
SO effects as they play the most important role in gravitational wave detection and parameter
estimation. As we shall see a good deal is known on spin effects (both SO and SS), but still it will
be important in the future to further improve our knowledge of the waveform and gravitationalwave phasing, by computing still higher post-Newtonian SO and SS terms, and to include at least
the dominant spin-spin-spin (SSS) effect [305]. For the computations of SSS and even SSSS effects
see Refs. [246, 245, 296, 305, 413].
The SO effects have been known at the leading level since the seminal works of Tulczyjew [411,
412], Barker & O’Connell [27, 28] and Kidder et al. [275, 271]. With our post-Newtonian counting
such leading level corresponds to the 1.5PN order. The SO terms have been computed to the
next-to-leading level which corresponds to 2.5PN order in Refs. [394, 194, 165, 292, 352, 241]
for the equations of motion or dynamics, and in Refs. [53, 54] for the gravitational radiation
field. Note that Refs. [394, 194, 165, 241] employ traditional post-Newtonian methods (both
harmonic-coordinates and Hamiltonian), but that Refs. [292, 352] are based on the effective field
theory (EFT) approach. The next-to-next-to-leading SO level corresponding to 3.5PN order has
been obtained in Refs. [242, 244] using the Hamiltonian method for the equations of motion, in
Ref. [297] using the EFT, and in Refs. [307, 90] using the harmonic-coordinates method. Here we
shall focus on the harmonic-coordinates approach [307, 90, 89, 306] which is in fact best formulated
using a Lagrangian, see Section 11.1. With this approach the next-to-next-to-leading SO level was
derived not only for the equations of motion including precession, but also for the radiation field
(energy flux and orbital phasing) [89, 306]. An analytic solution for the SO precession effects
will be presented in Section 11.2. Note that concerning the radiation field the highest known SO
level actually contains specific tail-induced contributions at 3PN [54] and 4PN [306] orders, see
Section 11.3.
The SS effects are known at the leading level corresponding to 2PN order from Barker &
O’Connell [27, 28] in the equations of motion (see [271, 351, 110] for subsequent derivations), and
from Refs. [275, 271] in the radiation field. Next-to-leading SS contributions are at 3PN order and
have been obtained with Hamiltonian [387, 389, 388, 247, 241], EFT [354, 356, 355, 293, 299] and
harmonic-coordinates [88] techniques (with [88] obtaining also the next-to-leading SS terms in the
gravitational-wave flux). With SS effects in a compact binary system one must make a distinction
between the spin squared terms, involving the coupling between the two same spins 𝑆1 or 𝑆2 ,
and the interaction terms, involving the coupling between the two different spins 𝑆1 and 𝑆2 . The
spin-squared terms 𝑆12 and 𝑆22 arise due to the effects on the dynamics of the quadrupole moments
of the compact bodies that are induced by their spins [347]. They have been computed through
2PN order in the fluxes and orbital phase in Refs. [217, 218, 314]. The interaction terms 𝑆1 × 𝑆2
can be computed using a simple pole-dipole formalism like the one we shall review in Section 11.1.
The interaction terms 𝑆1 × 𝑆2 between different spins have been derived to next-to-next-to-leading
4PN order for the equations of motion in Refs. [294, 298] (EFT) and [243] (Hamiltonian). In this
article we shall generally neglect the SS effects and refer for these to the literature quoted above.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 148

148

11.1

Luc Blanchet

Lagrangian formalism for spinning point particles

Some necessary material for constructing a Lagrangian for a spinning point particle in curved
spacetime is presented here. The formalism is issued from early works [239, 19] and has also been
developed in the context of the EFT approach [351]. Variants and alternatives (most importantly
the associated Hamiltonian formalism) can be found in Refs. [389, 386, 25]. The formalism yields
for the equations of motion of spinning particles and the equations of precession of the spins the
classic results known in general relativity [411, 412, 310, 331, 135, 409, 179].
Let us consider a single spinning point particle moving in a given curved background metric
𝑔𝛼𝛽 (𝑥). The particle follows the worldline 𝑦 𝛼 (𝜏 ), with tangent four-velocity 𝑢𝛼 = d𝑦 𝛼 /d𝜏 , where
𝜏 is a parameter along the representative worldline. In a first stage we do not require that the
four-velocity be normalized; thus 𝜏 needs not be the proper time elapsed along the worldline.
To describe the internal degrees of freedom associated with the particle’s spin, we introduce a
moving orthonormal tetrad 𝑒𝐴𝛼 (𝜏 ) along the trajectory, which defines a “body-fixed” frame.77
The rotation tensor 𝜔 𝛼𝛽 associated with the tetrad is defined by
D𝑒𝐴𝛼
= −𝜔 𝛼𝛽 𝑒𝐴𝛽 ,
d𝜏

(367)

where D/d𝜏 ≡ 𝑢𝛽 ∇𝛽 is the covariant derivative with respect to the parameter 𝜏 along the worldline;
equivalently, we have
D𝑒𝐴𝛽
𝜔 𝛼𝛽 = 𝑒𝐴𝛼
.
(368)
d𝜏
Because of the normalization of the tetrad the rotation tensor is antisymmetric: 𝜔 𝛼𝛽 = −𝜔 𝛽𝛼 .
We look for an action principle for the spinning particle. Following Refs. [239, 351] and the
general spirit of effective field theories, we require the following symmetries to hold:
1. The action is a covariant scalar, i.e., behaves as a scalar with respect to general space-time
diffeomorphisms;
2. It is a global Lorentz scalar, i.e., stays invariant under an arbitrary change of the tetrad
vectors: 𝑒𝐴𝛼 (𝜏 ) −→ Λ𝐵 𝐴 𝑒𝐵 𝛼 (𝜏 ) where Λ𝐵 𝐴 is a constant Lorentz matrix;
3. It is reparametrization-invariant, i.e., its form is independent of the parameter 𝜏 used to
follow the particle’s worldline.
In addition to these symmetries we need to specify the dynamical degrees of freedom: These are
chosen to be the particle’s position 𝑦 𝛼 and the tetrad 𝑒𝐴𝛼 . Furthermore we restrict ourselves to a
Lagrangian depending only on the four-velocity 𝑢𝛼 , the rotation tensor 𝜔 𝛼𝛽 , and the metric 𝑔𝛼𝛽 .
Thus, the postulated action is of the type
∫︁ +∞
[︀
]︀
(︀
)︀
𝐼 𝑦 𝛼 , 𝑒𝐴𝛼 =
d𝜏 𝐿 𝑢𝛼 , 𝜔 𝛼𝛽 , 𝑔𝛼𝛽 .
(369)
−∞

These assumptions confine the formalism to a “pole-dipole” model and to terms linear in the spins.
An important point is that such a model is universal in the sense that it can be used for black
holes as well as neutrons stars. Indeed, the internal structure of the spinning body appears only
at the quadratic order in the spins, through the rotationally induced quadrupole moment.
The tetrad is orthonormal in the sense that 𝑔𝛼𝛽 𝑒𝐴𝛼 𝑒𝐵 𝛽 = 𝜂𝐴𝐵 , where 𝜂𝐴𝐵 = diag(−1, 1, 1, 1) denotes a
Minkowski metric. The indices 𝐴𝐵 · · · = 0, 1, 2, 3 are the internal Lorentz indices, while as usual 𝛼𝛽 . . . 𝜇𝜈 · · · =
𝛽
0, 1, 2, 3 are the space-time covariant indices. The inverse dual tetrad 𝑒𝐴𝛼 , defined by 𝑒𝐴𝛽 𝑒𝐴𝛼 = 𝛿𝛼
, satisfies
𝛽
𝐵.
𝜂𝐴𝐵 𝑒𝐴𝛼 𝑒𝐵 𝛽 = 𝑔𝛼𝛽 . We have also the completeness relation 𝑒𝐴 𝑒𝐵 𝛽 = 𝛿𝐴
77

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 149

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

149

As it is written in (369), i.e., depending only on Lorentz scalars, 𝐿 is automatically a Lorentz
scalar. By performing an infinitesimal coordinate transformation, one easily sees that the requirement that the Lagrangian be a covariant scalar specifies its dependence on the metric to be such
that (see e.g., Ref. [19])
𝜕𝐿
2
= 𝑝𝛼 𝑢𝛽 + 𝑆 𝛼𝛾 𝜔 𝛽𝛾 .
(370)
𝜕𝑔𝛼𝛽
We have defined the conjugate linear momentum 𝑝𝛼 and the antisymmetric spin tensor 𝑆 𝛼𝛽 by
⃒
𝜕𝐿 ⃒⃒
,
(371a)
𝑝𝛼 ≡
𝜕𝑢𝛼 ⃒𝜔,𝑔
⃒
𝜕𝐿 ⃒
(371b)
𝑆𝛼𝛽 ≡ 2 𝛼𝛽 ⃒⃒ .
𝜕𝜔
𝑢,𝑔

Note that the right-hand side of Eq. (370) is necessarily symmetric by exchange of the indices 𝛼
and 𝛽. Finally, imposing the invariance of the action (369) by reparametrization of the worldline,
we find that the Lagrangian must be a homogeneous function of degree one in the velocity 𝑢𝛼 and
rotation tensor 𝜔 𝛼𝛽 . Applying Euler’s theorem to the function 𝐿(𝑢𝛼 , 𝜔 𝛼𝛽 ) immediately gives
1
𝐿 = 𝑝𝛼 𝑢𝛼 + 𝑆𝛼𝛽 𝜔 𝛼𝛽 ,
2

(372)

where the functions 𝑝𝛼 (𝑢, 𝜔) and 𝑆𝛼𝛽 (𝑢, 𝜔) must be reparametrization invariant. Note that, at
this stage, their explicit expressions are not known. They will be specified only when a spin
supplementary condition is imposed, see Eq. (379) below.
We now investigate the unconstrained variations of the action (369) with respect to the dynamical variables 𝑒𝐴𝛼 , 𝑦 𝛼 and the metric. First, we vary it with respect to the tetrad 𝑒𝐴𝛼 while keeping
the position 𝑦 𝛼 fixed. A worry is that we must have a way to distinguish intrinsic variations of
the tetrad from variations which are induced by a change of the metric 𝑔𝛼𝛽 . This is conveniently
solved by decomposing the variation 𝛿𝑒𝐴𝛽 according to
(︁
)︁
1
𝛿𝑒𝐴𝛽 = 𝑒𝐴𝛼 𝛿𝜃𝛼𝛽 + 𝛿𝑔 𝛼𝛽 ,
2

(373)
𝛽]

in which we have introduced the antisymmetric tensor 𝛿𝜃𝛼𝛽 ≡ 𝑒𝐴[𝛼 𝛿𝑒𝐴 , and where the corre𝛽)
sponding symmetric part is simply given by the variation of the metric, i.e. 𝑒𝐴(𝛼 𝛿𝑒𝐴 ≡ 21 𝛿𝑔 𝛼𝛽 .
𝛼𝛽
𝛼𝛽
Then we can consider the independent variations 𝛿𝜃 and 𝛿𝑔 . Varying with respect to 𝛿𝜃𝛼𝛽 ,
but holding the metric fixed, gives the equation of spin precession which is found to be
D𝑆𝛼𝛽
= 𝜔𝛼 𝛾 𝑆𝛽𝛾 − 𝜔𝛽 𝛾 𝑆𝛼𝛾 ,
d𝜏

(374)

or, alternatively, using the fact that the right-hand side of Eq. (370) is symmetric,
D𝑆𝛼𝛽
= 𝑝𝛼 𝑢𝛽 − 𝑝𝛽 𝑢𝛼 .
d𝜏

(375)

We next vary with respect to the particle’s position 𝑦 𝛼 while holding the tetrad 𝑒𝐴𝛼 fixed. Operationally, this means that we have to parallel-transport the tetrad along the displacement vector,
i.e., to impose
𝛿𝑦 𝛽 ∇𝛽 𝑒𝐴𝛼 = 0 .
(376)
A simple way to derive the result is to use locally inertial coordinates, such that the Christoffel
𝛼
𝛼
𝛽
𝛼
symbols Γ𝛼
𝛽𝛾 = 0 along the particle’s worldline 𝑦 (𝜏 ); then, Eq. (376) gives 𝛿𝑒𝐴 = 𝛿𝑦 𝜕𝛽 𝑒𝐴 =

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 150

150

Luc Blanchet

𝛾
−𝛿𝑦 𝛽 Γ𝛼
𝛽𝛾 𝑒𝐴 = 0. The variation leads then to the well-known Mathisson–Papapetrou [310, 331,
135] equation of motion
D𝑝𝛼
1
= − 𝑢𝛽 𝑅𝛼𝛽𝜇𝜈 𝑆 𝜇𝜈 ,
(377)
d𝜏
2
which involves the famous coupling of the spin tensor to the Riemann curvature.78 With a little
more work, the equation of motion (377) can also be derived using an arbitrary coordinate system,
making use of the parallel transport equation (376). Finally, varying with respect to the metric
while keeping 𝛿𝜃𝛼𝛽 = 0, gives the stress-energy tensor of the spinning particle. We must again
take into account the scalarity of the action, as imposed by Eq. (370). We obtain the standard
pole-dipole result [411, 412, 310, 331, 135, 409, 179]:

𝑇 𝛼𝛽 =

∫︁ +∞

d𝜏 𝑝(𝛼 𝑢𝛽)

−∞

𝛿(4) (𝑥 − 𝑦)
√
− ∇𝛾
−𝑔

∫︁ +∞

d𝜏 𝑆 𝛾(𝛼 𝑢𝛽)

−∞

𝛿(4) (𝑥 − 𝑦)
√
,
−𝑔

(378)

where 𝛿(4) (𝑥 − 𝑦) denotes the four-dimensional Dirac function. It can easily be checked that the
covariant conservation law ∇𝛽 𝑇 𝛼𝛽 = 0 holds as a consequence of the equation of motion (377) and
the equation of spin precession (375).
Up to now we have considered unconstrained variations of the action (369), describing the
particle’s internal degrees of freedom by the six independent components of the tetrad 𝑒𝐴𝛼 (namely
a 4×4 matrix subject to the 10 constraints 𝑔𝛼𝛽 𝑒𝐴𝛼 𝑒𝐵 𝛽 = 𝜂𝐴𝐵 ). To correctly account for the number
of degrees of freedom associated with the spin, we must impose three supplementary spin conditions
(SSC). Several choices are possible for a sensible SSC. Notice that in the case of extended bodies
the choice of a SSC corresponds to the choice of a central worldline inside the body with respect
to which the spin angular momentum is defined (see Ref. [271] for a discussion). Here we adopt
the Tulczyjew covariant SSC [411, 412]
𝑆 𝛼𝛽 𝑝𝛽 = 0 .

(379)

As shown by Hanson & Regge [239] in the flat space-time case, it is possible to specify the Lagrangian in our original action (369) in such a way that the constraints (379) are directly the
consequence of the equations derived from that Lagrangian. Here, for simplicity’s sake, we shall
simply impose the constraints (379) in the space of solutions of the Euler-Lagrange equations.
From Eq. (379) we can introduce the covariant spin vector 𝑆𝜇 associated with the spin tensor by79
1 𝛼𝛽𝜇𝜈
𝜀
𝑝𝜇 𝑆𝜈 ,
(380)
𝑚
where we have defined the mass of the particle by 𝑚2 ≡ −𝑔 𝜇𝜈 𝑝𝜇 𝑝𝜈 . By contracting Eq. (375) with
𝑝𝛽 and using the equation of motion (377), one obtains
𝑆 𝛼𝛽 ≡

𝑝𝛼 (𝑝𝑢) + 𝑚2 𝑢𝛼 =

1 𝛾 𝛽
𝑢 𝑅 𝛾𝜇𝜈 𝑆 𝜇𝜈 𝑆𝛼𝛽 ,
2

(381)

where we denote (𝑝𝑢) ≡ 𝑝𝜇 𝑢𝜇 . By further contracting Eq. (381) with 𝑢𝛼 we obtain an explicit
expression for (𝑝𝑢), which can then be substituted back into (381) to provide the relation linking
the four-momentum 𝑝𝛼 to the four-velocity 𝑢𝛼 . It can be checked using (379) and (381) that the
mass of the particle is constant along the particle’s trajectory: d𝑚/d𝜏 = 0. Furthermore the
four-dimensional magnitude 𝑠 of the spin defined by 𝑠2 ≡ 𝑔 𝜇𝜈 𝑆𝜇 𝑆𝜈 is also conserved: d𝑠/d𝜏 = 0.
78 Our conventions for the Riemann tensor 𝑅
𝛼𝛽𝜇𝜈 follow those of MTW [319].
√
√
79 The four-dimensional Levi-Civita tensor is defined by 𝜀
−𝑔 𝜖𝛼𝛽𝜇𝜈 and 𝜀𝛼𝛽𝜇𝜈 ≡ −𝜖𝛼𝛽𝜇𝜈 / −𝑔; here
𝛼𝛽𝜇𝜈 ≡
𝛼𝛽𝜇𝜈
0123
𝜖𝛼𝛽𝜇𝜈 = 𝜖
denotes the completely anti-symmetric Levi-Civita symbol such that 𝜖0123 = 𝜖
= 1. For

convenience in this section we pose 𝑐 = 1.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 151

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

151

Henceforth we shall restrict our attention to spin-orbit (SO) interactions, which are linear in
the spins.
√︀ We shall also adopt for the parameter 𝜏 along the particle’s worldline the proper time
d𝜏 ≡ −𝑔𝜇𝜈 d𝑦 𝜇 d𝑦 𝜈 , so that 𝑔𝜇𝜈 𝑢𝜇 𝑢𝜈 = −1. Neglecting quadratic spin-spin (SS) and higherorder interactions, the linear momentum is simply proportional to the normalized four-velocity:
𝑝𝛼 = 𝑚 𝑢𝛼 + 𝒪(𝑆 2 ). Hence, from Eq. (375) we deduce that D𝑆𝛼𝛽 /d𝜏 = 𝒪(𝑆 2 ). The equation for
the spin covariant vector 𝑆𝛼 then reduces at linear order to
D𝑆𝛼
= 𝒪(𝑆 2 ) .
d𝜏

(382)

Thus the spin covector is parallel transported along the particle’s trajectory at linear order in spin.
We can also impose that the spin should be purely spatial for the comoving observer:
𝑆𝛼 𝑢𝛼 = 0 .

(383)

From now on, we shall often omit writing the 𝒪(𝑆 2 ) remainders.
In applications (e.g., the construction of gravitational wave templates for the compact binary
inspiral) it is very useful to introduce new spin variables that are designed to have a conserved threedimensional Euclidean norm (numerically equal to 𝑠). Using conserved-norm spin vector variables
is indeed the most natural choice when considering the dynamics of compact binaries reduced to
the frame of the center of mass or to circular orbits [90]. Indeed the evolution equations of such
spin variables reduces, by construction, to ordinary precession equations, and these variables are
secularly constant (see Ref. [423]).
A standard, general procedure to define a (Euclidean) conserved-norm spin spatial vector consists of projecting the spin covector 𝑆𝛼 onto an orthonormal tetrad 𝑒𝐴𝛼 , which leads to the four
scalar components (𝐴 = 0, 1, 2, 3)
𝑆𝐴 = 𝑒𝐴𝛼 𝑆𝛼 .
(384)
If we choose for the time-like tetrad vector the four-velocity itself, 𝑒0𝛼 = 𝑢𝛼 ,80 the time component
tetrad projection 𝑆0 vanishes because of the orthogonality condition (383). We have seen that
𝑆𝛼 𝑆 𝛼 = 𝑠2 is conserved along the trajectory; because of (383) we can rewrite this as 𝛾 𝛼𝛽 𝑆𝛼 𝑆𝛽 =
𝑠2 , in which we have introduced the projector 𝛾 𝛼𝛽 = 𝑔 𝛼𝛽 + 𝑢𝛼 𝑢𝛽 onto the spatial hypersurface
orthogonal to 𝑢𝛼 . From the orthonormality of the tetrad and our choice 𝑒0𝛼 = 𝑢𝛼 , we have
𝛾 𝛼𝛽 = 𝛿 𝑎𝑏 𝑒𝑎𝛼 𝑒𝑏𝛽 in which 𝑎, 𝑏 = 1, 2, 3 refer to the spatial values of the tetrad indices, i.e.,
𝐴 = (0, 𝑎) and 𝐵 = (0, 𝑏). Therefore the conservation law 𝛾 𝛼𝛽 𝑆𝛼 𝑆𝛽 = 𝑠2 becomes
𝛿 𝑎𝑏 𝑆𝑎 𝑆𝑏 = 𝑠2 ,

(385)

which is indeed the relation defining a Euclidean conserved-norm spin variable 𝑆𝑎 .81 However,
note that the choice of the spin variable 𝑆𝑎 is still somewhat arbitrary, since a rotation of the
tetrad vectors can freely be performed. We refer to [165, 90] for the definition of some “canonical”
choice for the tetrad in order to fix this residual freedom. Such choice presents the advantage
of providing a unique determination of the conserved-norm spin variable in a given gauge. This
canonical choice will be the one adopted in all explicit results presented in Section 11.3.
The evolution equation (382) for the original spin variable 𝑆𝛼 now translates into an ordinary
precession equation for the tetrad components 𝑆𝑎 , namely
d𝑆𝑎
= Ω𝑎𝑏 𝑆𝑏 ,
d𝑡

(386)

80 Because of this choice, it is better to consider that the tetrad is not the same as the one we originally employed
to construct the action (369).
81 Beware that here we employ the usual slight ambiguity in the notation when using the same carrier letter 𝑆
to denote the tetrad components (384) and the original spin covector. Thus, 𝑆𝑎 should not be confused with the
spatial components 𝑆𝑖 (with 𝑖 = 1, 2, 3) of the covariant vector 𝑆𝛼 .

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 152

152

Luc Blanchet

where the precession tensor Ω𝑎𝑏 is related to the tetrad components 𝜔𝐴𝐵 of the rotation tensor
defined in (368) by Ω𝑎𝑏 = 𝑧 𝜔𝑎𝑏 where we pose 𝑧 ≡ d𝜏 /d𝑡, remembering the redshift variable (276).
The antisymmetric character of the matrix Ω𝑎𝑏 guaranties that 𝑆𝑎 satisfies the Euclidean precession
equation
d𝑆
=Ω×𝑆,
(387)
d𝑡
where we denote 𝑆 = (𝑆𝑎 ), and Ω = (Ω𝑎 ) with Ω𝑎 = − 12 𝜖𝑎𝑏𝑐 Ω𝑏𝑐 . As a consequence of (387)
the spin has a conserved Euclidean norm: 𝑆 2 = 𝑠2 . From now on we shall no longer make any
distinction between the spatial tetrad indices 𝑎𝑏 . . . and the ordinary spatial indices 𝑖𝑗 . . . which
are raised and lowered with the Kronecker metric. Explicit results for the equations of motion and
gravitational wave templates will be given in Sections 11.2 and 11.3 using the canonical choice for
the conserved-norm spin variable 𝑆.

11.2

Equations of motion and precession for spin-orbit effects

The previous formalism can be generalized to self-gravitating systems consisting of two (or more
generally N ) spinning point particles. The metric generated by the system of particles, interacting
only through gravitation, is solution of the Einstein field equations (18) with stress-energy tensor
given by the sum of the individual stress-energy tensors (378) for each particles. The equations
of motion of the particles are given by the Mathisson–Papapetrou equations (377) with “selfgravitating” metric evaluated at the location of the particles thanks to a regularization procedure
(see Section 6). The precession equations of each of the spins are given by
d𝑆a
= Ωa × 𝑆a ,
d𝑡

(388)

where a = 1, 2 labels the particles. The spin variables 𝑆a are the conserved-norm spins defined
in Section 11.1. In the following it is convenient to introduce two combinations of the individuals
spins defined by (with 𝑋a ≡ 𝑚a /𝑚 and 𝜈 ≡ 𝑋1 𝑋2 )82
𝑆 ≡ 𝑆1 + 𝑆2 ,
𝑆2
𝑆1
−
.
Σ≡
𝑋2
𝑋1

(389a)
(389b)

We shall investigate the case where the binary’s orbit is quasi-circular, i.e., whose radius is
constant apart from small perturbations induced by the spins (as usual we neglect the gravitational
radiation damping effects). We denote by 𝑥 = 𝑦1 − 𝑦2 and 𝑣 = d𝑥/d𝑡 the relative position and
velocity.83 We introduce an orthonormal moving triad {𝑛, 𝜆, ℓ} defined by the unit separation
vector 𝑛 = 𝑥/𝑟 (with 𝑟 = |𝑥|) and the unit normal ℓ to the instantaneous orbital plane given
by ℓ = 𝑛 × 𝑣/|𝑛 × 𝑣|; the orthonormal triad is then completed by 𝜆 = ℓ × 𝑛. Those vectors
are represented on Figure 4, which shows the geometry of the system. The orbital frequency Ω is
defined for general orbits, not necessarily circular, by 𝑣 = ˙𝑟𝑛 + 𝑟Ω𝜆 where 𝑟˙ = 𝑛 · 𝑣 represents
82 Notation adopted in Ref. [271]; the inverse formulas read

𝑆1 = 𝑋1 𝑆 − 𝜈Σ ,
𝑆2 = 𝑋2 𝑆 + 𝜈Σ .
83 Note that the individual particle’s positions 𝑦 in the frame of the center-of-mass (defined by the cancellation
a
of the center-of-mass integral of motion: 𝐺 = 0) are related to the relative position and velocity 𝑥 and 𝑣 by some
expressions similar to Eqs. (224) but containing spin effects starting at order 1.5PN.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 153

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

153

the derivative of 𝑟 with respect to the coordinate time 𝑡. The general expression for the relative
acceleration 𝑎 ≡ d𝑣/d𝑡 decomposed in the moving basis {𝑛, 𝜆, ℓ} is
(︀
)︀
(︀
)︀
𝑎 = 𝑟¨ − 𝑟 Ω2 𝑛 + 𝑟 Ω̇ + 2𝑟˙ Ω 𝜆 + 𝑟 𝜛 Ω ℓ .
(390)
Here we have introduced the orbital plane precession 𝜛 of the orbit defined by 𝜛 ≡ −𝜆 · dℓ/d𝑡.
Next we impose the restriction to quasi-circular precessing orbits which is defined by the conditions
𝑟˙ = Ω̇ = 𝒪(1/𝑐5 ) and 𝑟¨ = 𝒪(1/𝑐10 ) so that 𝑣 2 = 𝑟2 Ω2 +𝒪(1/𝑐10 ); see Eqs. (227). Then 𝜆 represents
the direction of the velocity, and the precession frequency 𝜛 is proportional to the variation of ℓ
in the direction of the velocity. In this way we find that the equations of the relative motion in the
frame of the center-of-mass are
(︂ )︂
1
2
(391)
𝑎 = −𝑟 Ω 𝑛 + 𝑟 𝜛 Ω ℓ + 𝒪 5 .
𝑐
Since we neglect the radiation reaction damping there is no component of the acceleration along 𝜆.
This equation represents the generalization of Eq. (226) for spinning quasi-circular binaries with
no radiation reaction. The orbital frequency Ω will contain spin effects in addition to the non-spin
terms given by (228), while the precessional frequency 𝜛 will entirely be due to spins.
Here we report the latest results for the spin-orbit (SO) contributions into these quantities at
the next-to-next-to-leading level corresponding to 3.5PN order [307, 90]. We project out the spins
on the moving orthonormal basis, defining 𝑆 = 𝑆𝑛 𝑛 + 𝑆𝜆 𝜆 + 𝑆ℓ ℓ and similarly for Σ. We have
{︂
[︂(︂
)︂
(︂
)︂ ]︂
𝛾 3/2
45 27
27 13
2
ΩSO =
−5𝑆ℓ − 3ΔΣℓ + 𝛾
− 𝜈 𝑆ℓ + Δ
− 𝜈 Σℓ
(392)
𝑚 𝑟3
2
2
2
2
)︂
(︂
)︂ ]︂}︂
[︂(︂
(︂ )︂
51
297 341
21
1
495 561
−
𝜈 − 𝜈 2 𝑆ℓ + Δ −
−
𝜈 − 𝜈 2 Σℓ
+ 𝛾2 −
+𝒪 8 ,
8
8
8
8
8
8
𝑐
which has to be added to the non-spin terms (228) up to 3.5PN order. We recall that the ordering
post-Newtonian parameter is 𝛾 = 𝐺𝑚
𝑟𝑐2 . On the other hand the next-to-next-to-leading SO effects
into the precessional frequency read
)︂ ]︂
{︂
[︂
(︂
𝑐3 𝑥3
11
𝜛 = 2 3 7𝑆𝑛 + 3ΔΣ𝑛 + 𝑥 (−3 − 12𝜈) 𝑆𝑛 + Δ −3 − 𝜈 Σ𝑛
(393)
𝐺 𝑚
2
)︂
(︂
)︂ ]︂}︂
(︂ )︂
[︂(︂
3 77
13
1
3 59
+𝒪 8 ,
+ 𝑥2 − − 𝜈 + 9𝜈 2 𝑆𝑛 + Δ − − 𝜈 + 𝜈 2 Σ𝑛
2
2
2
8
3
𝑐
2/3
where this time the ordering post-Newtonian parameter is 𝑥 ≡ ( 𝐺𝑚Ω
. The SO terms at
𝑐3 )
the same level in the conserved energy associated with the equations of motion will be given in
Eq. (415) below. In order to complete the evolution equations for quasi-circular orbits we need
also the precession vectors Ωa of the two spins as defined by Eq. (388). These are given by
{︂
[︂
(︂
)︂]︂
𝑐3 𝑥5/2
3 1
3
9
5
1
9
5
Ω1 =
ℓ
+ 𝜈− Δ+𝑥
+ 𝜈 − 𝜈2 + Δ − + 𝜈
(394)
𝐺𝑚
4 2
4
16 4
24
16 8
[︂
(︂
)︂]︂}︂
(︂ )︂
27
3
105 2
1
27 39
5
1
+ 𝑥2
+ 𝜈−
𝜈 − 𝜈3 + Δ − + 𝜈 − 𝜈2
+𝒪 8 .
32 16
32
48
32
8
32
𝑐

We obtain Ω2 from Ω1 simply by exchanging the masses, Δ → −Δ. At the linear SO level the
precession vectors Ωa are independent of the spins.84
84 Beware of our inevitably slightly confusing notation: Ω is the binary’s orbital frequency and Ω
SO refers to the
spin-orbit terms therein; Ωa is the precession frequency of the a-th spin while 𝜛 is the precession frequency of the
orbital plane; and 𝜔a defined earlier in Eqs. (244) and (284) is the rotation frequency of the a-th black hole. Such
different notions nicely mix up in the first law of spinning binary black holes in Section 8.3; see Eq. (282) and the
corotation condition (285).

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 154

154

Luc Blanchet

We now investigate an analytical solution for the dynamics of compact spinning binaries on
quasi-circular orbits, including the effects of spin precession [54, 306]. This solution will be valid
whenever the radiation reaction effects can be neglected, and is restricted to the linear SO level.

Figure 4: Geometric definitions for the precessional motion of spinning compact binaries [54, 306]. We
show (i) the source frame defined by the fixed orthonormal basis {𝑥, 𝑦, 𝑧}; (ii) the instantaneous orbital
plane which is described by the orthonormal basis {𝑥ℓ , 𝑦ℓ , ℓ}; (iii) the moving triad {𝑛, 𝜆, ℓ} and the
associated three Euler angles 𝛼, 𝜄 and Φ; (v) the direction of the total angular momentum J which
coincides with the 𝑧–direction. Dashed lines show projections into the 𝑥–𝑦 plane.

In the following, we will extensively employ the total angular momentum of the system, that
we denote by J, and which is conserved when radiation-reaction effects are neglected,
dJ
= 0.
d𝑡

(395)

It is customary to decompose the conserved total angular momentum J as the sum of the orbital
angular momentum 𝐿 and of the two spins,85
J=𝐿+

𝑆
.
𝑐

(396)

This split between 𝐿 and 𝑆 = 𝑆1 + 𝑆2 is specified by our choice of spin variables, here the
conserved-norm spins defined in Section 11.1. Note that although 𝐿 is called the “orbital” angular
momentum, it actually includes both non-spin and spin contributions. We refer to Eq. (4.7) in [90]
for the expression of 𝐿 at the next-to-next-to-leading SO level for quasi-circular orbits.
Our solution will consist of some explicit expressions for the moving triad {𝑛, 𝜆, ℓ} at the SO
level in the conservative dynamics for quasi-circular orbits. With the previous definitions of the
orbital frequency Ω and the precessional frequency 𝜛 we have the following system of equations
for the time evolution of the triad vectors,
d𝑛
= Ω𝜆,
d𝑡

(397a)

85 Recall from Eq. (366) that in our convention the spins have the dimension of an angular momentum times 𝑐.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 155

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

d𝜆
= −Ω 𝑛 + 𝜛 ℓ ,
d𝑡
dℓ
= −𝜛 𝜆 .
d𝑡

155

(397b)
(397c)

Equivalently, introducing the orbital rotation vector Ω ≡ Ω ℓ and spin precession vector 𝜛 ≡ 𝜛 𝑛,
these equations can be elegantly written as
d𝑛
= Ω × 𝑛,
d𝑡
)︀
d𝜆 (︀
= Ω + 𝜛 × 𝜆,
d𝑡
dℓ
= 𝜛 × ℓ.
d𝑡

(398a)
(398b)
(398c)

Next we introduce a fixed (inertial) orthonormal basis {x, y, z} as follows: z is defined to be the
normalized value J/J of the total angular momentum J; y is orthogonal to the plane spanned by z
and the direction 𝑁 = 𝑋/𝑅 of the detector as seen from the source (notation of Section 3.1) and
is defined by y = z × 𝑁 /|z × 𝑁 |; and x completes the triad – see Figure 4. Then, we introduce
the standard spherical coordinates (𝛼, 𝜄) of the vector ℓ measured in the inertial basis {x, y, z}.
Since 𝜄 is the angle between the total and orbital angular momenta, we have
sin 𝜄 =

|J × ℓ|
,
J

(399)

where J ≡ |J|. The angles (𝛼, 𝜄) are referred to as the precession angles.
We now derive from the time evolution of our triad vectors those of the precession angles (𝛼, 𝜄),
and of an appropriate phase Φ that specifies the position of 𝑛 with respect to some reference
direction in the orbital plane denoted xℓ . Following Ref. [13], we pose
J×ℓ
,
|J × ℓ|
yℓ = ℓ × xℓ ,
xℓ =

(400a)
(400b)

such that {xℓ , yℓ , ℓ} forms an orthonormal basis. The motion takes place in the instantaneous
orbital plane spanned by 𝑛 and 𝜆, and the phase angle Φ is such that (see Figure 4):

from which we deduce

𝑛 = cos Φ xℓ + sin Φ yℓ ,
𝜆 = − sin Φ xℓ + cos Φ yℓ ,

(401a)
(401b)

(︀
)︀
J𝜆 − i J𝑛
𝑒−i Φ = xℓ · 𝑛 + i𝜆 = √︀
.
J2𝑛 + J2𝜆

(402)

Combining Eqs. (402) with (399) we also get
sin 𝜄 𝑒−i Φ =

J𝜆 − i J𝑛
.
J

(403)

By identifying the right-hand sides of (397) with the time-derivatives of the relations (401) we
obtain the following system of equations for the variations of 𝛼, 𝜄 and Φ,
d𝛼
sin Φ
=𝜛
,
d𝑡
sin 𝜄

(404a)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 156

156

Luc Blanchet

d𝜄
= 𝜛 cos Φ ,
d𝑡
sin Φ
dΦ
=Ω−𝜛
.
d𝑡
tan 𝜄

(404b)
(404c)

On the other hand, using the decompositon of the total angular momentum (396) together
with the fact that the components of 𝐿 projected along 𝑛 and 𝜆 are of the order 𝒪(𝑆), see e.g.,
Eq. (4.7) in Ref. [90], we deduce that sin 𝜄 is itself a small quantity of order 𝒪(𝑆). Since we also
have 𝜛 = 𝒪(𝑆), we conclude by direct integration of the sum of Eqs. (404a) and (404c) that
Φ + 𝛼 = 𝜑 + 𝒪(𝑆 2 ) ,
in which we have defined the “carrier” phase as
∫︁
𝜑 ≡ Ω d𝑡 = Ω(𝑡 − 𝑡0 ) + 𝜑0 ,

(405)

(406)

with 𝜑0 the value of the carrier phase at some arbitrary initial time 𝑡0 . An important point we
have used when integrating (406) is that the orbital frequency Ω is constant at linear order in the
spins. Indeed, from Eq. (392) we see that only the components of the conserved-norm spin vectors
along ℓ can contribute to Ω at linear order. As we show in Eq. (409c) below, these components
are in fact constant at linear order in spins. Thus we can treat Ω as a constant for our purpose.
The combination Φ + 𝛼 being known by Eq. (405), we can further express the precession angles
𝜄 and 𝛼 at linear order in spins in terms of the components J𝑛 and J𝜆 ; from Eqs. (399) and (403):
√︀
J2𝑛 + J2𝜆
sin 𝜄 =
+ 𝒪(𝑆 2 ) ,
(407a)
𝐿NS
J𝜆 − i J𝑛 i 𝜑
𝑒 + 𝒪(𝑆 2 ) ,
(407b)
𝑒i 𝛼 = √︀
2
2
J𝑛 + J 𝜆
where we denote by 𝐿NS the norm of the non-spin (NS) part of the orbital angular momentum 𝐿.
It remains to obtain the explicit time variation of the components of the two individual spins
𝑆𝑛a , 𝑆𝜆a and 𝑆ℓa (with a = 1, 2). Using Eqs. (407) together with the decomposition (396) and the
explicit expression of 𝐿 in Ref. [90], we shall then be able to obtain the explicit time variation of
the precession angles (𝛼, 𝜄) and phase Φ. Combining (388) and (397) we obtain
(︀
)︀
d𝑆𝑛a
= Ω − Ωa 𝑆𝜆a ,
d𝑡
(︀
)︀
d𝑆𝜆a
= − Ω − Ωa 𝑆𝑛a + 𝜛 𝑆ℓa ,
d𝑡
d𝑆ℓa
= −𝜛 𝑆𝜆a ,
d𝑡

(408a)
(408b)
(408c)

where Ωa is the norm of the precession vector of the a-th spin as given by (394), and the precession
frequency 𝜛 is explicitly given by (393). At linear order in spins these equations translate into
(︀
)︀
d𝑆𝑛a
= Ω − Ωa 𝑆𝜆a ,
d𝑡
(︀
)︀
d𝑆𝜆a
= − Ω − Ωa 𝑆𝑛a + 𝒪(𝑆 2 ) ,
d𝑡
d𝑆ℓa
= 𝒪(𝑆 2 ) .
d𝑡

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

(409a)
(409b)
(409c)

## PDF page 157

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

157

We see that, as stated before, the spin components along ℓ are constant, and so is the orbital
frequency Ω given by (392). At the linear SO level, the equations (409) can be decoupled and
integrated as
a
𝑆𝑛a = 𝑆⊥
cos 𝜓a ,
a
a
𝑆𝜆 = −𝑆⊥ sin 𝜓a ,
𝑆ℓa = 𝑆‖a .

(410a)
(410b)
(410c)

a
Here 𝑆⊥
and 𝑆‖a denote two quantities for each spins, that are constant up to terms 𝒪(𝑆 2 ). The
phase of the projection perpendicular to the direction ℓ of each of the spins is given by

𝜓a = (Ω − Ωa )(𝑡 − 𝑡0 ) + 𝜓a0 ,

(411)

where 𝜓a0 is the constant initial phase at the reference time 𝑡0 .
Finally we can give in an explicit way, to linear SO order, the triad {𝑛(𝑡), 𝜆(𝑡), ℓ(𝑡)} in terms
of some reference triad {𝑛0 , 𝜆0 , ℓ0 } at the reference time 𝑡0 in Eqs. (411) and (406). The best way
to express the result is to introduce the complex null vector 𝑚 ≡ √12 (𝑛 + i𝜆) and its complex
conjuguate 𝑚; the normalization is chosen so that 𝑚 · 𝑚 = 1. We obtain
)︀
i (︀
𝑚 = 𝑒−i(𝜑−𝜑0 ) 𝑚0 + √ sin 𝜄 𝑒i𝛼 − sin 𝜄0 𝑒i𝛼0 𝑒−i𝜑 ℓ0 + 𝒪(𝑆 2 ) ,
2
[︂
]︂
)︀
i (︀
ℓ = ℓ0 + √ sin 𝜄 𝑒−i𝛼 − sin 𝜄0 𝑒−i𝛼0 𝑒i𝜑0 𝑚0 + c.c. + 𝒪(𝑆 2 ) .
2

(412a)
(412b)

The precession effects in the dynamical solution for the evolution of the basis vectors {𝑛, 𝜆, ℓ} are
given by the second terms in these equations. They depend only in the combination sin 𝜄 𝑒i𝛼 and
its complex conjugate sin 𝜄 𝑒−i𝛼 , which follows from Eqs. (407) and the known spin and non-spin
contributions to the total angular momentum J. One can check that precession effects in the above
dynamical solution (412) for the moving triad start at order 𝒪(1/𝑐3 ).

11.3

Spin-orbit effects in the gravitational wave flux and orbital phase

Like in Section 9 our main task is to control up to high post-Newtonian order the mass and
current radiative multipole moments U𝐿 and V𝐿 which parametrize the asymptotic waveform and
gravitational fluxes far away from the source, cf. Eqs. (66) – (68). The radiative multipole moments
are in turn related to the source multipole moments I𝐿 and J𝐿 through complicated relationships
involving tails and related effects; see e.g., Eqs. (76).86
The source moments have been expressed in Eqs. (123) in terms of some source densities Σ,
Σ𝑖 and Σ𝑖𝑗 defined from the components of the post-Newtonian expansion of the pseudo-tensor,
denoted 𝜏 𝛼𝛽 . To lowest order the (PN expansion of the) pseudo-tensor reduces to the matter tensor
𝑇 𝛼𝛽 which has compact support, and the source densities Σ, Σ𝑖 , Σ𝑖𝑗 reduce to the compact support
quantities 𝜎, 𝜎𝑖 𝜎𝑖𝑗 given by Eqs. (145). Now, computing spin effects, the matter tensor 𝑇 𝛼𝛽 has
been found to be given by (378) in the framework of the pole-dipole approximation suitable for
SO couplings (and sufficient also for SS interactions between different spins). Here, to give a flavor
of the computation, we present the lowest order spin contributions (necessarily SO) to the general
mass and current source multipole moments (∀ℓ ∈ N):
{︂ [︁
]︁
2ℓ 𝜈
SO
I𝐿 = 3
ℓ 𝜎ℓ (𝜈)(𝑣 × 𝑆)⟨𝑖ℓ − 𝜎ℓ+1 (𝜈)(𝑣 × Σ)⟨𝑖ℓ 𝑥𝐿−1⟩
𝑐 (ℓ + 1)
86 In this section we can neglect the gauge multipole moments W

𝐿 , · · · , Z𝐿 .

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 158

158

Luc Blanchet

[︁

− (ℓ − 1) 𝜎ℓ (𝜈)(𝑥 × 𝑆)

⟨𝑖ℓ

⟨𝑖ℓ

]︁

− 𝜎ℓ+1 (𝜈)(𝑥 × Σ)
𝑣
)︂
(︂
]︁
1
(ℓ + 1)𝜈 [︁
JSO
𝜎ℓ−1 (𝜈)𝑆 ⟨𝑖ℓ − 𝜎ℓ (𝜈)Σ⟨𝑖ℓ 𝑥𝐿−1⟩ + 𝒪 3 .
𝐿 =
2𝑐
𝑐

𝑖ℓ−1 𝐿−2⟩

𝑥

}︂

(︂
+𝒪

1
𝑐5

)︂
,

(413a)
(413b)

Paralleling the similar expressions (304) for the Newtonian approximation to the source moments
in the non-spin case, we posed 𝜎ℓ (𝜈) ≡ 𝑋2ℓ−1 + (−)ℓ 𝑋1ℓ−1 with 𝑋a = 𝑚a /𝑚 [see also Eqs. (305)].
In Eqs. (413) we employ the notation (389) for the two spins and the ordinary cross product ×
of Euclidean vectors. Thus, the dominant level of spins is at the 1.5PN order in the mass-type
moments I𝐿 , but only at the 0.5PN order in the current-type moments J𝐿 . It is then evident
that the spin part of the current-type moments will always dominate over that of the mass-type
moments. We refer to [53, 89] for higher order post-Newtonian expressions of the source moments.
If we insert the expressions (413) into tail integrals like (76), we find that some spin contributions
originate from tails starting at the 3PN order [54].
Finally, skipping details, we are left with the following highest-order known result for the SO
contributions to the gravitational wave energy flux, which is currently 4PN order [53, 89, 306]:87
{︂
5
32𝑐5 𝜈 2 𝑥13/2
(414)
−4𝑆ℓ − ΔΣℓ
ℱSO =
5 𝐺2 𝑚2
4
)︂
(︂
)︂
[︂(︂
]︂
13 43
9 272
𝜈 𝑆ℓ + − + 𝜈 ΔΣℓ
+𝑥 − +
2
9
16
4
[︂
]︂
31𝜋
+𝑥3/2 −16𝜋 𝑆ℓ −
ΔΣℓ
6
)︂
(︂
)︂
[︂(︂
]︂
2810 2
9535 1849
1501 2
476645 6172
2
+
𝜈−
𝜈 𝑆ℓ +
+
𝜈−
𝜈 ΔΣℓ
+𝑥
6804
189
27
336
126
36
[︂(︂
)︂
(︂
)︂
]︂
(︂ )︂}︂
3485𝜋 13879𝜋
7163𝜋 130583𝜋
1
5/2
+𝑥
−
+
𝜈 𝑆ℓ + −
+
𝜈 ΔΣℓ + 𝒪 6
.
96
72
672
2016
𝑐
We recall that 𝑆ℓ ≡ ℓ · S and Σℓ ≡ ℓ · Σ, with S and Σ denoting the combinations (389), and the
individual spins are the specific conserved-norm spins that have been introduced in Section 11.1.
The result (414) superposes to the non-spin contributions given by Eq. (314). Satisfyingly it is in
complete agreement in the test-mass limit where 𝜈 → 0 with the result of black-hole perturbation
theory on a Kerr background obtained in Ref. [396].
Finally we can compute the spin effects in the time evolution of the binary’s orbital frequency
Ω. We rely as in Section 9 on the equation (295) balancing the total emitted energy flux ℱ with
the variation of the binary’s center-of-mass energy 𝐸. The non-spin contributions in 𝐸 have been
provided for quasi-circular binaries in Eq. (232); the SO contributions to next-to-next-to-leading
order are given by [307, 90]
{︂
[︂(︂
)︂
(︂
)︂ ]︂
𝑐2 𝜈 𝑥5/2 14
61
10
𝐸SO = −
𝑆ℓ + 2ΔΣℓ + 𝑥 11 − 𝜈 𝑆ℓ + Δ 3 − 𝜈 Σℓ
(415)
2 𝐺𝑚
3
9
3
[︂(︂
)︂
(︂
)︂ ]︂}︂
(︂ )︂
135 367
29
27
5
1
+ 𝑥2
−
𝜈 + 𝜈 2 𝑆ℓ + Δ
− 39𝜈 + 𝜈 2 Σℓ
+𝒪 8 .
4
4
12
4
4
𝑐
Using 𝐸 and ℱ expressed as functions of the orbital frequency Ω (through 𝑥) and of the spin
variables (through 𝑆ℓ and Σℓ ), we transform the balance equation into
(︂
)︂
ℱ
Ω̇SO = −
.
(416)
d𝐸/dΩ SO
87 Notice that the spin-orbit contributions due to the absorption by the black-hole horizons have to be added to
this post-Newtonian result [349, 392, 5, 125].

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 159

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

159

However, in writing the latter equation it is important to justify that the spin quantities 𝑆ℓ
and Σℓ are secularly constant, i.e., do not evolve on a gravitational radiation reaction time scale
so we can neglect their variations when taking the time derivative of Eq. (415). Fortunately, this
is the case of the conserved-norm spin variables, as proved in Ref. [423] up to relative 1PN order,
i.e., considering radiation reaction effects up to 3.5PN order. Furthermore this can also be shown
from the following structural general argument valid at linear order in spins [54, 89]. In the centerof-mass frame, the only vectors at our disposal, except for the spins, are 𝑛 and 𝑣. Recalling that
the spin vectors are pseudovectors regarding parity transformation, we see that the only way SO
contributions can enter scalars such as the energy 𝐸 or the flux ℱ is through the mixed products
(𝑛, 𝑣, 𝑆a ), i.e., through the components 𝑆ℓa . Now, the same reasoning applies to the precession
vectors Ωa in Eqs. (388): They must be pseudovectors, and, at linear order in spin, they must
only depend on 𝑛 and 𝑣; so that they must be proportional to ℓ, as can be explicitly seen for
instance in Eq. (394). Now, the time derivative of the components along ℓ of the spins are given by
d𝑆ℓa /d𝑡 = Sa ·(dℓ/d𝑡+ℓ×Ωa ). The second term vanishes because Ωa ∝ ℓ, and since dℓ/d𝑡 = 𝒪(𝑆),
we obtain that 𝑆ℓa is constant at linear order in the spins. We have already met an instance of this
important fact in Eq. (409c). This argument is valid at any post-Newtonian order and for general
orbits, but is limited to spin-orbit terms; furthermore it does not specify any time scale for the
variation, so it applies to short time scales such as the orbital and precessional periods, as well as
to the long gravitational radiation reaction time scale (see also Ref. [218] and references therein
for related discussions).
Table 4: Spin-orbit contributions to the number of gravitational-wave cycles 𝒩cycle [defined by Eq. (319)]
for binaries detectable by ground-based detectors LIGO-VIRGO. The entry frequency is 𝑓seismic = 10 Hz
3
and the terminal frequency is 𝑓ISCO = 63/2𝑐𝜋𝐺 𝑚 . For each compact object the magnitude 𝜒a and the
orientation 𝜅a of the spin are defined by 𝑆a = 𝐺 𝑚2a 𝜒a 𝑆^a and 𝜅a = 𝑆^a · ℓ; remind Eq. (366). The spin-spin
(SS) terms are neglected.
PN order
1.5PN
2.5PN
3PN
3.5PN
4PN

(leading SO)
(1PN SO)
(leading SO-tail)
(2PN SO)
(1PN SO-tail)

1.4 𝑀⊙ + 1.4 𝑀⊙

10 𝑀⊙ + 1.4 𝑀⊙

10 𝑀⊙ + 10 𝑀⊙

65.6𝜅1 𝜒1 + 65.6𝜅2 𝜒2
9.3𝜅1 𝜒1 + 9.3𝜅2 𝜒2
−3.2𝜅1 𝜒1 − 3.2𝜅2 𝜒2
1.9𝜅1 𝜒1 + 1.9𝜅2 𝜒2
−1.5𝜅1 𝜒1 − 1.5𝜅2 𝜒2

114.0𝜅1 𝜒1 + 11.7𝜅2 𝜒2
33.8𝜅1 𝜒1 + 2.9𝜅2 𝜒2
−13.2𝜅1 𝜒1 − 1.3𝜅2 𝜒2
11.1𝜅1 𝜒1 + 0.8𝜅2 𝜒2
−8.0𝜅1 𝜒1 − 0.7𝜅2 𝜒2

16.0𝜅1 𝜒1 + 16.0𝜅2 𝜒2
5.7𝜅1 𝜒1 + 5.7𝜅2 𝜒2
−2.6𝜅1 𝜒1 − 2.6𝜅2 𝜒2
1.7𝜅1 𝜒1 + 1.7𝜅2 𝜒2
−1.5𝜅1 𝜒1 − 1.5𝜅2 𝜒2

We are then allowed to apply Eq. (416) with conserved-norm spin variables at the SO level. We
thus obtain the secular evolution of Ω and from that we deduce by a further∫︀ integration (following
the Taylor approximant T2) the secular evolution of the carrier phase 𝜑 ≡ Ω d𝑡:
𝜑SO = −

{︂
𝑥−1
235
125
𝑆ℓ +
ΔΣℓ
32 𝐺 𝑚2 𝜈
6
8
[︂(︂
)︂
(︂
)︂
]︂
554345 55
41745 15
+𝑥 ln 𝑥 −
− 𝜈 𝑆ℓ + −
+ 𝜈 ΔΣℓ
2016
8
448
8
[︂
]︂
940𝜋
745𝜋
+𝑥3/2
𝑆ℓ +
ΔΣℓ
3
6
[︂(︂
)︂
8980424995 6586595
305 2
+ 𝑥2 −
+
𝜈−
𝜈 𝑆ℓ
6096384
6048
288
(︂
)︂
]︂
170978035 2876425
4735 2
+ −
+
𝜈+
𝜈 ΔΣℓ
387072
5376
1152

(417)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 160

160

Luc Blanchet

5/2

+𝑥

[︂(︂

)︂
(︂
)︂
]︂
(︂ )︂}︂
2388425𝜋 9925𝜋
3237995𝜋 258245𝜋
1
.
−
𝜈 𝑆ℓ +
−
𝜈 ΔΣℓ + 𝒪 6
3024
36
12096
2016
𝑐

This expression, when added to the expression for the non-spin terms given by Eq. (318), and
considering also the SS terms, constitutes the main theoretical input needed for the construction
of templates for spinning compact binaries. However, recall that in the case of precessional binaries,
for which the spins are not aligned or anti-aligned with the orbital angular momentum, we must
subtract to the carrier phase 𝜑 the precessional correction 𝛼 arising from the precession of the
orbital plane. Indeed the physical phase variable Φ which is defined in Figure 4, has been proved
to be given by Φ = 𝜑 − 𝛼 at linear order in spins, cf. Eq. (405). The precessional correction 𝛼 can
be computed at linear order in spins from the results of Section 11.2.
As we have done in Table 3 for the non-spin terms, we evaluate in Table 4 the SO contributions to the number of gravitational-wave cycles accumulated in the bandwidth of LIGO-VIRGO
detectors, Eq. (319). The results show that the SO terms up to 4PN order can be numerically
important, for spins close to maximal and for suitable orientations. They can even be larger than
the corresponding non-spin contributions at 3.5PN order and perhaps at 4PN order (but recall
that the non-spin terms at 4PN order are not known); compare with Table 3. We thus conclude
that the SO terms are relevant to be included in the gravitational wave templates for an accurate
extraction of the binary parameters. Although numerically smaller, the SS terms are also relevant;
for these we refer to the literature quoted at the beginning of Section 11.

Acknowledgments
The author’s works reviewed in this article have been done in a series of collaborations with K.G.
Arun, Alejandro Bohé, Alessandra Buonanno, Thibault Damour, Steven Detweiler, Gilles EspositoFarèse, Guillaume Faye, Bala R. Iyer, Alexandre Le Tiec, Sylvain Marsat, Samaya Nissanke, Olivier
Poujade, B.S. Sathyaprakash, Gerhard Schäfer, Bernard F. Whiting, Clifford M. Will, and Alan
G. Wiseman.

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 161

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

161

References
[1] Abbott, B. P. et al. (LIGO Scientific Collaboration and Virgo Collaboration), “Observation of Gravitational Waves from a Binary Black Hole Merger”, Phys. Rev. Lett., 116, 061102 (2016). [DOI],
[ADS], [arXiv:1602.03837 [gr-qc]]. (Cited on page 7.)
[2] Abramowicz, M. A. and Kluźniak, W., “A precise determination of black hole spin in GRO J1655-40”,
Astron. Astrophys., 374, L19–L20 (2001). [DOI], [ADS], [astro-ph/0105077]. (Cited on page 146.)
[3] Ajith, P., Iyer, B. R., Robinson, C. A. K. and Sathyaprakash, B. S., “New class of post-Newtonian
approximants to the waveform templates of inspiralling compact binaries: Test mass in the
Schwarzschild spacetime”, Phys. Rev. D, 71, 044029 (2005). [gr-qc/0412033]. (Cited on pages 65
and 131.)
[4] Ajith, P. et al., “Template bank for gravitational waveforms from coalescing binary black holes:
Nonspinning binaries”, Phys. Rev. D, 77, 104017 (2008). [DOI], [ADS], [arXiv:0710.2335 [gr-qc]].
Erratum: Phys. Rev. D, 79, 129901(E) (2009). (Cited on page 65.)
[5] Alvi, K., “Energy and angular momentum flow into a black hole in a binary”, Phys. Rev. D, 64,
104020 (2001). [DOI], [arXiv:0107080 [gr-qc]]. (Cited on page 158.)
[6] Anderson, J. L. and DeCanio, T. C., “Equations of hydrodynamics in general relativity in the slow
motion approximation”, Gen. Relativ. Gravit., 6, 197–237 (1975). [DOI]. (Cited on pages 53, 57,
and 58.)
[7] Anderson, J. L., Kates, R. E., Kegeles, L. S. and Madonna, R. G., “Divergent integrals of postNewtonian gravity: Nonanalytic terms in the near-zone expansion of a gravitationally radiating
system found by matching”, Phys. Rev. D, 25, 2038–2048 (1982). [DOI], [ADS]. (Cited on pages 11,
44, and 46.)
[8] Apostolatos, T. A., Cutler, C., Sussman, G. J. and Thorne, K. S., “Spin induced orbital precession
and its modulation of the gravitational wave forms from merging binaries”, Phys. Rev. D, 49, 6274–
6297 (1994). [DOI]. (Cited on pages 21 and 146.)
[9] Arun, K. G., Blanchet, L., Iyer, B. R. and Qusailah, M. S., “Inspiralling compact binaries in
quasi-elliptical orbits: The complete 3PN energy flux”, Phys. Rev. D, 77, 064035 (2008). [DOI],
[arXiv:0711.0302]. (Cited on pages 20, 92, 138, 140, 141, and 142.)
[10] Arun, K. G., Blanchet, L., Iyer, B. R. and Qusailah, M. S., “Tail effects in the 3PN gravitational
wave energy flux of compact binaries in quasi-elliptical orbits”, Phys. Rev. D, 77, 064034 (2008).
[DOI], [arXiv:0711.0250]. (Cited on pages 20, 141, 143, and 144.)
[11] Arun, K. G., Blanchet, L., Iyer, B. R. and Qusailah, M. S. S., “The 2.5PN gravitational wave
polarizations from inspiralling compact binaries in circular orbits”, Class. Quantum Grav., 21, 3771–
3801 (2004). [DOI], [gr-qc/0404185]. Erratum: Class. Quantum Grav., 22, 3115 (2005). (Cited on
pages 20, 21, 117, 125, 126, and 130.)
[12] Arun, K. G., Blanchet, L., Iyer, B. R. and Sinha, S., “Third post-Newtonian angular momentum
flux and the secular evolution of orbital elements for inspiralling compact binaries in quasi-elliptical
orbits”, Phys. Rev. D, 80, 124018 (2009). [DOI], [arXiv:0908.3854]. (Cited on pages 20, 141, and 145.)
[13] Arun, K. G., Buonanno, A., Faye, G. and Ochsner, E., “Higher-order spin effects in the amplitude and
phase of gravitational waveforms emitted by inspiraling compact binaries: Ready-to-use gravitational
waveforms”, Phys. Rev. D, 79, 104023 (2009). [DOI], [arXiv:0810.5336]. (Cited on page 155.)
[14] Arun, K. G., Iyer, B. R., Qusailah, M. S. S. and Sathyaprakash, B. S., “Probing the non-linear
structure of general relativity with black hole binaries”, Phys. Rev. D, 74, 024006 (2006). [DOI],
[gr-qc/0604067]. (Cited on pages 16 and 131.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 162

162

Luc Blanchet

[15] Arun, K. G., Iyer, B. R., Qusailah, M. S. S. and Sathyaprakash, B. S., “Testing post-Newtonian
theory with gravitational wave observations”, Class. Quantum Grav., 23, L37–L43 (2006). [DOI],
[ADS], [arXiv:gr-qc/0604018]. (Cited on pages 16 and 131.)
[16] Arun, K. G., Iyer, B. R., Sathyaprakash, B. S. and Sinha, S., “Higher harmonics increase LISA’s
mass reach for supermassive black holes”, Phys. Rev. D, 75, 124002 (2007). [DOI], [arXiv:0704.1086].
(Cited on page 20.)
[17] Arun, K. G., Iyer, B. R., Sathyaprakash, B. S., Sinha, S. and Van Den Broeck, C., “Higher signal
harmonics, LISA’s angular resolution, and dark energy”, Phys. Rev. D, 76, 104016 (2007). [DOI],
[ADS], [arXiv:0707.3920]. (Cited on page 20.)
[18] Arun, K. G., Iyer, B. R., Sathyaprakash, B. S. and Sundararajan, P. A., “Parameter estimation of
inspiralling compact binaries using 3.5 post-Newtonian gravitational wave phasing: The nonspinning
case”, Phys. Rev. D, 71, 084008 (2005). [DOI], [gr-qc/0411146]. (Cited on pages 65 and 131.)
[19] Bailey, I. and Israel, W., “Lagrangian dynamics of spinning particles and polarized media in general
relativity”, Commun. Math. Phys., 42, 65 (1975). [DOI]. (Cited on pages 148 and 149.)
[20] Baker, J. G., Centrella, J., Choi, D.-I., Koppitz, M., van Meter, J. and Miller, M. C., “Getting a kick
out of numerical relativity”, Astrophys. J., 653, L93–L96 (2006). [DOI], [astro-ph/0603204]. (Cited
on page 22.)
[21] Baker, J. G., Centrella, J., Choi, D.-I., Koppitz, M. and van Meter, J. R., “Gravitational-Wave
Extraction from an Inspiraling Configuration of Merging Black Holes”, Phys. Rev. Lett., 96, 111102
(2006). [DOI], [ADS], [arXiv:gr-qc/0511103]. (Cited on page 8.)
[22] Barack, L., “Gravitational self-force in extreme mass-ratio inspirals”, Class. Quantum Grav., 26,
213001 (2009). [DOI], [ADS], [arXiv:0908.1664 [gr-qc]]. (Cited on page 112.)
[23] Barack, L., “Computational Methods for the Self-Force in Black Hole Spacetimes”, in Blanchet, L.,
Spallicci, A. and Whiting, B., eds., Mass and Motion in General Relativity, Lectures from the CNRS
School on Mass held in Orléans, France, 23 – 25 June 2008, Fundamental Theories of Physics, 162,
pp. 327–366, (Springer, Dordrecht; New York, 2011). [DOI], [ADS]. (Cited on pages 9 and 112.)
[24] Barack, L. and Sago, N., “Gravitational self-force correction to the innermost stable circular orbit of
a Schwarzschild black hole”, Phys. Rev. Lett., 102, 191101 (2009). [DOI], [arXiv:0902.0573]. (Cited
on page 108.)
[25] Barausse, E., Racine, E. and Buonanno, A., “Hamiltonian of a spinning test particle in curved
spacetime”, Phys. Rev. D, 80, 104025 (2009). [DOI], [arXiv:0907.4745 [gr-qc]]. (Cited on page 148.)
[26] Bardeen, J. M., Carter, B. and Hawking, S. W., “The Four Laws of Black Hole Mechanics”, Commun.
Math. Phys., 31, 161–170 (1973). [DOI], [ADS]. (Cited on page 110.)
[27] Barker, B. M. and O’Connell, R. F., “Gravitational two-body problem with arbitrary masses, spins,
and quadrupole moments”, Phys. Rev. D, 12, 329–335 (1975). [DOI]. (Cited on pages 19, 102,
and 147.)
[28] Barker, B. M. and O’Connell, R. F., “The Gravitational Interaction: Spin, Rotation, and Quantum
Effects – A Review”, Gen. Relativ. Gravit., 11, 149–175 (1979). [DOI]. (Cited on pages 19, 102,
and 147.)
[29] Baumgarte, T. W., “Innermost stable circular orbit of binary black holes”, Phys. Rev. D, 62, 024018
(2000). [DOI], [ADS]. (Cited on page 103.)
[30] Bekenstein, J. D., “Gravitational Radiation Recoil and Runaway Black Holes”, Astrophys. J., 183,
657–664 (1973). [DOI], [ADS]. (Cited on pages 10 and 22.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 163

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

163

[31] Bel, L., Damour, T., Deruelle, N., Ibáñez, J. and Martin, J., “Poincaré-Invariant Gravitational
Field and Equations of Motion of two Pointlike Objects: The Postlinear Approximation of General
Relativity”, Gen. Relativ. Gravit., 13, 963–1004 (1981). [DOI]. (Cited on page 17.)
[32] Benacquista, M. J. and Downing, J. M. B., “Relativistic Binaries in Globular Clusters”, Living Rev.
Relativity, 16, lrr-2013-4 (2013). [DOI], [ADS], [arXiv:1110.4423]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2013-4. (Cited on page 135.)
[33] Bernard, L., Blanchet, L., Bohé, A., Faye, G. and Marsat, S., “Fokker action of non-spinning compact
binaries at the fourth post-Newtonian approximation”, arXiv, e-print, (2015). [arXiv:1512.02876 [grqc]]. (Cited on page 19.)
[34] Berti, E., Cardoso, V., Gonzalez, J. A., Sperhake, U., Hannam, M., Husa, S. and Brügmann, B.,
“Inspiral, merger, and ringdown of unequal mass black hole binaries: A multipolar analysis”, Phys.
Rev. D, 76, 064034 (2007). [DOI], [ADS], [arXiv:gr-qc/0703053]. (Cited on page 36.)
[35] Bertotti, B. and Plebański, J. F., “Theory of gravitational perturbations in the fast motion approximation”, Ann. Phys. (N.Y.), 11, 169–200 (1960). [DOI]. (Cited on page 18.)
[36] Bini, D. and Damour, T., “Analytical determination of the two-body gravitational interaction potential at the fourth post-Newtonian approximation”, Phys. Rev. D, 87, 121501 (2013). [DOI], [ADS],
[arXiv:1305.4884 [gr-qc]]. (Cited on pages 19, 96, and 114.)
[37] Bini, D. and Damour, T., “Analytic determination of the eight-and-a-half post-Newtonian self-force
contributions to the two-body gravitational interaction potential”, Phys. Rev. D, 89, 104047 (2014).
[DOI], [arXiv:1403.2366 [gr-qc]]. (Cited on page 116.)
[38] Bini, D. and Damour, T., “High-order post-Newtonian contributions to the two-body gravitational
interaction potential from analytical gravitational self-force calculations”, Phys. Rev. D, 89, 064063
(2014). [DOI], [arXiv:1312.2503 [gr-qc]]. (Cited on page 116.)
[39] Bini, D., Damour, T. and Geralico, A., “Confirming and improving post-Newtonian and effectiveone-body results from self-force computations along eccentric orbits around a Schwarzschild black
hole”, arXiv, e-print, (2015). [arXiv:1511.04533 [gr-qc]]. (Cited on page 19.)
[40] Blaes, O., Lee, M. H. and Socrates, A., “The Kozai Mechanism and the Evolution of Binary Supermassive Black Holes”, Astrophys. J., 578, 775–786 (2002). [DOI], [ADS], [astro-ph/0203370]. (Cited
on page 135.)
[41] Blanchet, L., “Radiative gravitational fields in general-relativity. II. Asymptotic-behaviour at future
null infinity”, Proc. R. Soc. London, Ser. A, 409, 383–399 (1987). [DOI]. (Cited on pages 10, 11,
33, and 35.)
[42] Blanchet, L., Contribution à l’étude du rayonnement gravitationnel émis par un système isolé, Habil.
thesis, (Université Paris VI, Paris, 1990). (Cited on pages 21 and 43.)
[43] Blanchet, L., “Time asymmetric structure of gravitational radiation”, Phys. Rev. D, 47, 4392–4420
(1993). [DOI]. (Cited on pages 11, 18, 19, 46, 57, 58, 63, and 117.)
[44] Blanchet, L., “Second-post-Newtonian generation of gravitational radiation”, Phys. Rev. D, 51,
2559–2583 (1995). [DOI], [gr-qc/9501030]. (Cited on pages 11, 12, 20, 37, 46, 48, 51, and 64.)
[45] Blanchet, L., “Energy losses by gravitational radiation in inspiralling compact binaries to five halves
post-Newtonian order”, Phys. Rev. D, 54, 1417–1438 (1996). [DOI], [gr-qc/9603048]. Erratum: Phys.
Rev. D, 71, 129904(E) (2005). (Cited on pages 20 and 91.)
[46] Blanchet, L., “Gravitational radiation from relativistic sources”, in Marck, J.-A. and Lasota, J.-P.,
eds., Relativistic Gravitation and Gravitational Radiation, Proceedings of the Les Houches School of
Physics, held in Les Houches, Haute Savoie, 26 September – 6 October, 1995, Cambridge Contemporary Astrophysics, pp. 33–66, (Cambridge University Press, Cambridge, 1997). [gr-qc/9609049],
[Google Books]. (Cited on page 9.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 164

164

Luc Blanchet

[47] Blanchet, L., “Gravitational radiation reaction and balance equations to post-Newtonian order”,
Phys. Rev. D, 55, 714–732 (1997). [DOI], [gr-qc/9609049]. (Cited on pages 11, 18, 63, 64, and 117.)
[48] Blanchet, L., “Gravitational-wave tails of tails”, Class. Quantum Grav., 15, 113–141 (1998). [DOI],
[gr-qc/9710038]. Erratum: Class. Quantum Grav., 22, 3381 (2005). (Cited on pages 11, 20, 39, 40,
43, and 44.)
[49] Blanchet, L., “On the multipole expansion of the gravitational field”, Class. Quantum Grav., 15,
1971–1999 (1998). [DOI], [gr-qc/9801101]. (Cited on pages 11, 12, 46, 48, and 51.)
[50] Blanchet, L., “Quadrupole-quadrupole gravitational waves”, Class. Quantum Grav., 15, 89–111
(1998). [DOI], [gr-qc/9710037]. (Cited on pages 11, 21, 39, and 43.)
[51] Blanchet, L., “Innermost circular orbit of binary black holes at the third post-Newtonian approximation”, Phys. Rev. D, 65, 124009 (2002). [DOI], [gr-qc/0112056]. (Cited on pages 101, 103,
and 110.)
[52] Blanchet, L., “Post-Newtonian theory and the two-body problem”, in Blanchet, L., Spallicci, A. and
Whiting, B., eds., Mass and Motion in General Relativity, Lectures from the CNRS School on Mass
held in Orléans, France, 23 – 25 June 2008, Fundamental Theories of Physics, pp. 125–166, (Springer,
Dordrecht; New York, 2011). [DOI], [ADS], [arXiv:0907.3596 [gr-qc]]. (Cited on page 9.)
[53] Blanchet, L., Buonanno, A. and Faye, G., “Higher-order spin effects in the dynamics of compact
binaries II. Radiation field”, Phys. Rev. D, 74, 104034 (2006). [DOI], [gr-qc/0605140]. Erratum:
Phys. Rev. D, 75, 049903 (2007). (Cited on pages 21, 147, and 158.)
[54] Blanchet, L., Buonanno, A. and Faye, G., “Tail-induced spin-orbit effect in the gravitational radiation
of compact binaries”, Phys. Rev. D, 84, 064041 (2011). [DOI], [arXiv:1104.5659 [gr-qc]]. (Cited on
pages 21, 147, 154, 158, and 159.)
[55] Blanchet, L., Buonanno, A. and Le Tiec, A., “First law of mechanics for black hole binaries with
spins”, Phys. Rev. D, 87, 024030 (2013). [DOI], [arXiv:1211.1060 [gr-qc]]. (Cited on pages 102, 103,
and 111.)
[56] Blanchet, L. and Damour, T., “Multipolar radiation reaction in general relativity”, Phys. Lett. A,
104, 82–86 (1984). [DOI]. (Cited on page 63.)
[57] Blanchet, L. and Damour, T., “Radiative gravitational fields in general relativity I. General structure
of the field outside the source”, Philos. Trans. R. Soc. London, Ser. A, 320, 379–430 (1986). [DOI].
(Cited on pages 10, 11, 20, 26, 27, 29, 31, and 33.)
[58] Blanchet, L. and Damour, T., “Tail-transported temporal correlations in the dynamics of a gravitating system”, Phys. Rev. D, 37, 1410–1435 (1988). [DOI]. (Cited on pages 11, 19, 43, 44, 46, 57,
58, 59, and 63.)
[59] Blanchet, L. and Damour, T., “Post-Newtonian generation of gravitational waves”, Ann. Inst. Henri
Poincare A, 50, 377–408 (1989). (Cited on pages 11, 37, 46, and 49.)
[60] Blanchet, L. and Damour, T., “Hereditary effects in gravitational radiation”, Phys. Rev. D, 46,
4304–4319 (1992). [DOI]. (Cited on pages 11, 20, 21, 39, 43, 57, and 122.)
[61] Blanchet, L., Damour, T. and Esposito-Farèse, G., “Dimensional regularization of the third postNewtonian dynamics of point particles in harmonic coordinates”, Phys. Rev. D, 69, 124007 (2004).
[DOI], [gr-qc/0311052]. (Cited on pages 18, 70, 72, 74, and 75.)
[62] Blanchet, L., Damour, T., Esposito-Farèse, G. and Iyer, B. R., “Gravitational radiation from inspiralling compact binaries completed at the third post-Newtonian order”, Phys. Rev. Lett., 93, 091101
(2004). [DOI], [gr-qc/0406012]. (Cited on pages 20, 71, 77, 78, and 117.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 165

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

165

[63] Blanchet, L., Damour, T., Esposito-Farèse, G. and Iyer, B. R., “Dimensional regularization of the
third post-Newtonian gravitational wave generation of two point masses”, Phys. Rev. D, 71, 124004
(2005). [DOI], [ADS], [gr-qc/0503044]. (Cited on pages 20, 71, 77, 78, and 117.)
[64] Blanchet, L., Damour, T. and Iyer, B. R., “Gravitational waves from inspiralling compact binaries:
Energy loss and wave form to second post-Newtonian order”, Phys. Rev. D, 51, 5360–5386 (1995).
[DOI], [gr-qc/9501029]. (Cited on pages 20, 97, and 117.)
[65] Blanchet, L., Damour, T. and Iyer, B. R., “Surface-integral expressions for the multipole moments
of post-Newtonian sources and the boosted Schwarzschild solution”, Class. Quantum Grav., 22, 155
(2005). [DOI], [gr-qc/0410021]. (Cited on pages 53 and 71.)
[66] Blanchet, L., Damour, T., Iyer, B. R., Will, C. M. and Wiseman, A. G., “Gravitational-Radiation
Damping of Compact Binary Systems to Second Post-Newtonian Order”, Phys. Rev. Lett., 74, 3515–
3518 (1995). [DOI], [gr-qc/9501027]. (Cited on page 20.)
[67] Blanchet, L., Detweiler, S., Le Tiec, A. and Whiting, B. F., “Higher-order Post-Newtonian fit of the
gravitational self-force for circular orbits in the Schwarzschild geometry”, Phys. Rev. D, 81, 084033
(2010). [DOI], [ADS], [arXiv:1002.0726 [gr-qc]]. (Cited on pages 95, 112, 113, 114, and 115.)
[68] Blanchet, L., Detweiler, S., Le Tiec, A. and Whiting, B. F., “Post-Newtonian and numerical calculations of the gravitational self-force for circular orbits in the Schwarzschild geometry”, Phys. Rev.
D, 81, 064004 (2010). [DOI], [ADS], [arXiv:0910.0207 [gr-qc]]. (Cited on pages 60, 112, 113, 114,
and 115.)
[69] Blanchet, L. and Faye, G., “Equations of motion of point-particle binaries at the third postNewtonian order”, Phys. Lett. A, 271, 58–64 (2000). [DOI], [gr-qc/0004009]. (Cited on pages 17,
68, 69, 70, 71, 74, 77, 82, and 95.)
[70] Blanchet, L. and Faye, G., “Hadamard regularization”, J. Math. Phys., 41, 7675–7714 (2000). [DOI],
[gr-qc/0004008]. (Cited on pages 17, 66, 67, 68, 69, 74, and 75.)
[71] Blanchet, L. and Faye, G., “General relativistic dynamics of compact binaries at the third postNewtonian order”, Phys. Rev. D, 63, 062005 (2001). [DOI], [gr-qc/0007051]. (Cited on pages 17,
24, 59, 68, 69, 70, 71, 74, 76, 77, and 82.)
[72] Blanchet, L. and Faye, G., “Lorentzian regularization and the problem of point-like particles in
general relativity”, J. Math. Phys., 42, 4391–4418 (2001). [DOI], [gr-qc/0006100]. (Cited on pages 17,
66, 68, 69, and 75.)
[73] Blanchet, L., Faye, G., Iyer, B. R. and Joguet, B., “Gravitational-wave inspiral of compact binary
systems to 7/2 post-Newtonian order”, Phys. Rev. D, 65, 061501(R) (2002). [DOI], [gr-qc/0105099].
Erratum: Phys. Rev. D, 71, 129902(E) (2005). (Cited on pages 20 and 71.)
[74] Blanchet, L., Faye, G., Iyer, B. R. and Sinha, S., “The third post-Newtonian gravitational wave
polarisations and associated spherical harmonic modes for inspiralling compact binaries in quasicircular orbits”, Class. Quantum Grav., 25, 165003 (2008). [DOI], [arXiv:0802.1249]. (Cited on
pages 11, 20, 31, 40, 44, 117, 118, 119, 125, and 132.)
[75] Blanchet, L., Faye, G. and Nissanke, S., “Structure of the post-Newtonian expansion in general
relativity”, Phys. Rev. D, 72, 044024 (2005). [DOI]. (Cited on pages 11, 54, 58, and 59.)
[76] Blanchet, L., Faye, G. and Ponsot, B., “Gravitational field and equations of motion of compact
binaries to 5/2 post-Newtonian order”, Phys. Rev. D, 58, 124002 (1998). [DOI], [gr-qc/9804079].
(Cited on pages 17, 68, 78, 97, and 112.)
[77] Blanchet, L., Faye, G. and Whiting, B. F., “Half-integral conservative post-Newtonian approximations in the redshift factor of black hole binaries”, Phys. Rev. D, 89, 064026 (2014). [DOI],
[arXiv:1312.2975 [gr-qc]]. (Cited on page 116.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 166

166

Luc Blanchet

[78] Blanchet, L., Faye, G. and Whiting, B. F., “High-order half-integral conservative post-Newtonian
coefficients in the redshift factor of black hole binaries”, Phys. Rev. D, 90, 044017 (2014). [DOI],
[arXiv:1405.5151 [gr-qc]]. (Cited on page 116.)
[79] Blanchet, L. and Iyer, B. R., “Third post-Newtonian dynamics of compact binaries: Equations of
motion in the center-of-mass frame”, Class. Quantum Grav., 20, 755 (2003). [DOI], [gr-qc/0209089].
(Cited on pages 17, 90, 91, 94, 103, and 135.)
[80] Blanchet, L. and Iyer, B. R., “Hadamard regularization of the third post-Newtonian gravitational
wave generation of two point masses”, Phys. Rev. D, 71, 024004 (2005). [DOI], [gr-qc/0409094].
(Cited on pages 20, 71, 76, 77, 78, and 117.)
[81] Blanchet, L., Iyer, B. R. and Joguet, B., “Gravitational waves from inspiralling compact binaries:
Energy flux to third post-Newtonian order”, Phys. Rev. D, 65, 064005 (2002). [gr-qc/0105098].
Erratum: Phys. Rev. D, 71, 129903(E) (2005). (Cited on pages 20, 71, 76, 77, 78, 117, 118, 119,
and 145.)
[82] Blanchet, L., Iyer, B. R., Will, C. M. and Wiseman, A. G., “Gravitational wave forms from inspiralling compact binaries to second-post-Newtonian order”, Class. Quantum Grav., 13, 575–584
(1996). [DOI], [gr-qc/9602024]. (Cited on pages 20 and 125.)
[83] Blanchet, L., Qusailah, M. S. and Will, C. M., “Gravitational recoil of inspiraling black-hole binaries
to second post-Newtonian order”, Astrophys. J., 635, 508 (2005). [DOI], [astro-ph/0507692]. (Cited
on page 22.)
[84] Blanchet, L. and Sathyaprakash, B. S., “Signal analysis of gravitational wave tails”, Class. Quantum
Grav., 11, 2807–2831 (1994). [DOI]. (Cited on pages 16 and 131.)
[85] Blanchet, L. and Sathyaprakash, B. S., “Detecting a Tail Effect in Gravitational-Wave Experiments”,
Phys. Rev. Lett., 74, 1067–1070 (1995). [DOI], [ADS]. (Cited on pages 16 and 131.)
[86] Blanchet, L. and Schäfer, G., “Higher order gravitational radiation losses in binary systems”, Mon.
Not. R. Astron. Soc., 239, 845–867 (1989). [DOI]. (Cited on pages 20, 117, 140, and 145.)
[87] Blanchet, L. and Schäfer, G., “Gravitational wave tails and binary star systems”, Class. Quantum
Grav., 10, 2699–2721 (1993). [DOI]. (Cited on pages 14, 20, 122, 126, 140, 144, and 145.)
[88] Bohé, A., Faye, G., Marsat, S. and Porter, E. K., “Quadratic-in-spin effects in the orbital dynamics
and gravitational-wave energy flux of compact binaries at the 3PN order”, Class. Quantum Grav.,
32, 195010 (2015). [DOI], [arXiv:1501.01529 [gr-qc]]. (Cited on pages 21 and 147.)
[89] Bohé, A., Marsat, S. and Blanchet, L., “Next-to-next-to-leading order spin-orbit effects in the gravitational wave flux and orbital phasing of compact binaries”, Class. Quantum Grav., 30, 135009
(2013). [arXiv:1303.7412]. (Cited on pages 21, 147, 158, and 159.)
[90] Bohé, A., Marsat, S., Faye, G. and Blanchet, L., “Next-to-next-to-leading order spin-orbit effects in
the near-zone metric and precession equations of compact binary systems”, Class. Quantum Grav.,
30, 075017 (2013). [arXiv:1212.5520]. (Cited on pages 19, 147, 151, 153, 154, 156, and 158.)
[91] Bollini, C. G. and Giambiagi, J. J., “Lowest order ‘divergent’ graphs in 𝑣-dimensional space”, Phys.
Lett. B, 40, 566–568 (1972). [DOI]. (Cited on page 72.)
[92] Bonazzola, S., Gourgoulhon, E. and Marck, J.-A., “Numerical models of irrotational binary neutron
stars in general relativity”, Phys. Rev. Lett., 82, 892–895 (1999). [DOI], [ADS], [arXiv:gr-qc/9810072
[gr-qc]]. (Cited on page 101.)
[93] Bondi, H., van der Burg, M. G. J. and Metzner, A. W. K., “Gravitational Waves in General Relativity.
VII. Waves from Axi-Symmetric Isolated Systems”, Proc. R. Soc. London, Ser. A, 269, 21–52 (1962).
[DOI], [ADS]. (Cited on pages 10, 11, 33, and 41.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 167

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

167

[94] Bonnor, W. B., “Spherical gravitational waves”, Philos. Trans. R. Soc. London, Ser. A, 251, 233–271
(1959). [DOI]. (Cited on pages 10 and 26.)
[95] Bonnor, W. B. and Rotenberg, M. A., “Transport of momentum by gravitational waves: Linear
approximation”, Proc. R. Soc. London, Ser. A, 265, 109–116 (1961). [DOI]. (Cited on pages 10
and 26.)
[96] Bonnor, W. B. and Rotenberg, M. A., “Gravitational waves from isolated sources”, Proc. R. Soc.
London, Ser. A, 289, 247–274 (1966). [DOI]. (Cited on pages 10 and 26.)
[97] Boyle, M., Brown, D. A., Kidder, L. E., Mroué, A. H., Pfeiffer, H. P., Scheel, M. A., Cook, G. B. and
Teukolsky, S. A., “High-accuracy comparison of numerical relativity simulations with post-Newtonian
expansions”, Phys. Rev. D, 76, 124038 (2007). [DOI], [ADS], [arXiv:0710.0158 [gr-qc]]. (Cited on
page 36.)
[98] Boyle, M., Buonanno, A., Kidder, L. E., Mroué, A. H., Pan, Y., Pfeiffer, H. P. and Scheel, M. A.,
“High-accuracy numerical simulation of black-hole binaries: Computation of the gravitational-wave
energy flux and comparisons with post-Newtonian approximants”, Phys. Rev. D, 78, 104020 (2008).
[DOI], [arXiv:0804.4184 [gr-qc]]. (Cited on pages 36 and 124.)
[99] Braginsky, V. B. and Thorne, K. S., “Gravitational-wave bursts with memory and experimental
prospects”, Nature, 327, 123–125 (1987). [DOI]. (Cited on page 21.)
[100] Breitenlohner, P. and Maison, D., “Dimensional renormalization and the action principle”, Commun.
Math. Phys., 52, 11–38 (1977). [DOI]. (Cited on page 72.)
[101] Brenneman, L. W. and Reynolds, C. S., “Constraining Black Hole Spin via X-Ray Spectroscopy”,
Astrophys. J., 652, 1028–1043 (2006). [DOI], [ADS], [arXiv:astro-ph/0608502]. (Cited on page 146.)
[102] Brenneman, L. W. et al., “The Spin of the Supermassive Black Hole in NGC 3783”, Astrophys. J.,
736, 103 (2011). [DOI], [arXiv:1104.1172 [astro-ph.HE]]. (Cited on page 146.)
[103] Breuer, R. and Rudolph, E., “Radiation reaction and energy loss in the post-Newtonian approximation of general relativity”, Gen. Relativ. Gravit., 13, 777 (1981). [DOI]. (Cited on page 13.)
[104] Bruhat, Y., “The Cauchy Problem”, in Witten, L., ed., Gravitation: An Introduction to Current
Research, pp. 130–168, (Wiley, New York; London, 1962). (Cited on page 7.)
[105] Buonanno, A., Chen, Y. and Vallisneri, M., “Detection template families for gravitational waves
from the final stages of binary black-holes binaries: Nonspinning case”, Phys. Rev. D, 67, 024016
(2003). [DOI], [gr-qc/0205122]. (Cited on pages 65, 71, 125, and 131.)
[106] Buonanno, A., Chen, Y. and Vallisneri, M., “Detection template families for precessing binaries
of spinning compact binaries: Adiabatic limit”, Phys. Rev. D, 67, 104025 (2003). [DOI], [grqc/0211087]. (Cited on pages 65, 71, 125, and 131.)
[107] Buonanno, A., Cook, G. B. and Pretorius, F., “Inspiral, merger, and ring-down of equal-mass blackhole binaries”, Phys. Rev. D, 75, 124018 (2007). [DOI], [ADS], [gr-qc/0610122]. (Cited on page 36.)
[108] Buonanno, A. and Damour, T., “Effective one-body approach to general relativistic two-body dynamics”, Phys. Rev. D, 59, 084006 (1999). [DOI], [ADS], [arXiv:gr-qc/9811091]. (Cited on page 65.)
[109] Buonanno, A. and Damour, T., “Transition from inspiral to plunge in binary black hole coalescences”,
Phys. Rev. D, 62, 064015 (2000). [DOI], [ADS], [arXiv:gr-qc/0001013]. (Cited on page 65.)
[110] Buonanno, A., Faye, G. and Hinderer, T., “Spin effects on gravitational waves from inspiralling
compact binaries at second post-Newtonian order”, Phys. Rev. D, 87, 044009 (2013). [DOI],
[arXiv:1209.6349]. (Cited on page 147.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 168

168

Luc Blanchet

[111] Buonanno, A., Iyer, B. R., Pan, Y., Ochsner, E. and Sathyaprakash, B. S., “Comparison of postNewtonian templates for compact binary inspiral signals in gravitational-wave detectors”, Phys. Rev.
D, 80, 084043 (2009). [DOI], [arXiv:0907.0700 [gr-qc]]. (Cited on pages 65 and 131.)
[112] Buonanno, A., Pan, Y., Pfeiffer, H. P., Scheel, M. A., Buchman, L. T. and Kidder, L. E., “Effectiveone-body waveforms calibrated to numerical relativity simulations: Coalescence of nonspinning,
equal-mass black holes”, Phys. Rev. D, 79, 124028 (2009). [DOI], [ADS], [arXiv:0902.0790 [gr-qc]].
(Cited on page 65.)
[113] Burke, W. L., “Gravitational radiation damping of slowly moving systems calculated using matched
asymptotic expansions”, J. Math. Phys., 12, 401–418 (1971). [DOI], [ADS]. (Cited on pages 11, 13,
46, and 62.)
[114] Burke, W. L. and Thorne, K. S., “Gravitational Radiation Damping”, in Carmeli, M., Fickler, S. I.
and Witten, L., eds., Relativity, Proceedings of the Relativity Conference in the Midwest, held at
Cincinnati, Ohio, June 2 – 6, 1969, pp. 209–228, (Plenum Press, New York; London, 1970). (Cited
on pages 11, 13, 46, and 62.)
[115] Campanelli, M., “Understanding the fate of merging supermassive black holes”, Class. Quantum
Grav., 22, S387 (2005). [DOI], [astro-ph/0411744]. (Cited on page 22.)
[116] Campanelli, M., Lousto, C. O., Marronetti, P. and Zlochower, Y., “Accurate Evolutions of Orbiting
Black-Hole Binaries without Excision”, Phys. Rev. Lett., 96, 111101 (2006). [DOI], [ADS], [arXiv:grqc/0511048]. (Cited on page 8.)
[117] Campanelli, M., Lousto, C. O., Zlochower, Y. and Merritt, D., “Large merger recoils and spin
flips from generic black-hole binaries”, Astrophys. J. Lett., 659, L5–L8 (2007). [DOI], [arXiv:grqc/0701164 [gr-qc]]. (Cited on page 22.)
[118] Campbell, W. B., Macek, J. and Morgan, T. A., “Relativistic time-dependent multipole analysis for
scalar, electromagnetic, and gravitational fields”, Phys. Rev. D, 15, 2156–2164 (1977). [DOI]. (Cited
on page 10.)
[119] Campbell, W. B. and Morgan, T. A., “Debye Potentials For Gravitational Field”, Physica, 53(2),
264 (1971). [DOI]. (Cited on page 10.)
[120] Carmeli, M., “The equations of motion of slowly moving particles in the general theory of relativity”,
Nuovo Cimento, 37, 842 (1965). [DOI]. (Cited on page 97.)
[121] Caudill, M., Cook, G. B., Grigsby, J. D. and Pfeiffer, H. P., “Circular orbits and spin in black-hole
initial data”, Phys. Rev. D, 74, 064011 (2006). [DOI], [ADS], [gr-qc/0605053]. (Cited on pages 101,
103, 104, and 110.)
[122] Chandrasekhar, S., “The Post-Newtonian Equations of Hydrodynamics in General Relativity”, Astrophys. J., 142, 1488–1540 (1965). [DOI], [ADS]. (Cited on pages 9 and 53.)
[123] Chandrasekhar, S. and Esposito, F. P., “The 2 12 -Post-Newtonian Equations of Hydrodynamics and
Radiation Reaction in General Relativity”, Astrophys. J., 160, 153–179 (1970). [DOI]. (Cited on
pages 9 and 53.)
[124] Chandrasekhar, S. and Nutku, Y., “The Second Post-Newtonian Equations of Hydrodynamics in
General Relativity”, Astrophys. J., 158, 55–79 (1969). [DOI]. (Cited on pages 9 and 53.)
[125] Chatziioannou, K., Poisson, E. and Yunes, N., “Tidal heating and torquing of a Kerr black hole
to next-to-leading order in the tidal coupling”, Phys. Rev. D, 87, 044022 (2013). [DOI], [ADS],
[arXiv:1211.1686 [gr-qc]]. (Cited on page 158.)
[126] Chicone, C., Kopeikin, S. M., Mashhoon, B. and Retzloff, D. G., “Delay equations and radiation
damping”, Phys. Lett. A, 285, 17–26 (2001). [DOI], [gr-qc/0101122]. (Cited on page 55.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 169

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

169

[127] Christodoulou, D., “Reversible and irreversible transformations in black-hole physics”, Phys. Rev.
Lett., 25, 1596 (1970). [DOI]. (Cited on page 101.)
[128] Christodoulou, D., “Nonlinear Nature of Gravitation and Gravitational-Wave Experiments”, Phys.
Rev. Lett., 67, 1486–1489 (1991). [DOI]. (Cited on pages 21 and 43.)
[129] Christodoulou, D. and Ruffini, R., “Reversible transformations of a charged black hole”, Phys. Rev.
D, 4, 3552–3555 (1971). [DOI]. (Cited on page 101.)
[130] Christodoulou, D. and Schmidt, B. G., “Convergent and Asymptotic Iteration Methods in General
Relativity”, Commun. Math. Phys., 68, 275–289 (1979). [DOI]. (Cited on page 28.)
[131] Collins, J. C., Renormalization: An introduction to renormalization, the renormalization group, and
the operator-product expansion, (Cambridge University Press, Cambridge; New York, 1984). [Google
Books]. (Cited on page 72.)
[132] Cook, G. B., “Three-dimensional initial data for the collision of two black holes. II. Quasicircular
orbits for equal-mass black holes”, Phys. Rev. D, 50, 5025–5032 (1994). [DOI], [ADS]. (Cited on
pages 103 and 104.)
[133] Cook, G. B. and Pfeiffer, H. P., “Excision boundary conditions for black hole initial data”, Phys.
Rev. D, 70, 104016 (2004). [DOI], [ADS]. (Cited on pages 101, 102, 103, 104, and 110.)
[134] Cooperstock, F. I. and Booth, D. J., “Angular-Momentum Flux For Gravitational Radiation to
Octupole Order”, Nuovo Cimento B, 62(1), 163–170 (1969). [DOI]. (Cited on page 10.)
[135] Corinaldesi, E. and Papapetrou, A., “Spinning test-particles in general relativity. II”, Proc. R. Soc.
London, Ser. A, 209, 259–268 (1951). [DOI]. (Cited on pages 148 and 150.)
[136] Crowley, R. J. and Thorne, K. S., “Generation of gravitational waves. II. Post-linear formalism
revisited”, Astrophys. J., 215, 624–635 (1977). [DOI]. (Cited on page 10.)
[137] Cutler, C., Finn, L. S., Poisson, E. and Sussman, G. J., “Gravitational radiation from a particle in
circular orbit around a black hole. II. Numerical results for the nonrotating case”, Phys. Rev. D, 47,
1511–1518 (1993). [DOI]. (Cited on pages 16, 65, and 125.)
[138] Cutler, C. and Flanagan, É. É., “Gravitational waves from merging compact binaries: How accurately
can one extract the binary’s parameters from the inspiral wave form?”, Phys. Rev. D, 49, 2658–2697
(1994). [DOI], [arXiv:gr-qc/9402014]. (Cited on pages 14, 16, 65, 124, 125, and 146.)
[139] Cutler, C. et al., “The Last Three Minutes: Issues in Gravitational-Wave Measurements of Coalescing
Compact Binaries”, Phys. Rev. Lett., 70, 2984–2987 (1993). [DOI], [astro-ph/9208005]. (Cited on
pages 14, 16, 65, and 125.)
[140] D’Alembert, J., Traité de Dynamique, (David L’Aine, Paris, 1743). [Google Books].
page 7.)

(Cited on

[141] Damour, T., “Problème des deux corps et freinage de rayonnement en relativité générale”, C. R.
Acad. Sci. Ser. II, 294, 1355–1357 (1982). (Cited on page 17.)
[142] Damour, T., “Gravitational radiation and the motion of compact bodies”, in Deruelle, N. and Piran,
T., eds., Rayonnement Gravitationnel / Gravitational Radiation, Proceedings of the Les Houches
Summer School, 2 – 21 June 1982, pp. 59–144, (North-Holland, Amsterdam, 1983). (Cited on
pages 7, 9, 16, 17, 65, and 135.)
[143] Damour, T., “Gravitational radiation reaction in the binary pulsar and the quadrupole formula
controvercy”, Phys. Rev. Lett., 51, 1019–1021 (1983). [DOI]. (Cited on pages 7, 17, and 135.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 170

170

Luc Blanchet

[144] Damour, T., “An Introduction to the Theory of Gravitational Radiation”, in Carter, B. and Hartle,
J. B., eds., Gravitation in Astrophysics: Cargèse 1986, Proceedings of a NATO Advanced Study
Institute on Gravitation in Astrophysics, Cargése, France, 15 – 31 July, 1986, NATO ASI Series B,
156, pp. 3–62, (Plenum Press, New York, 1987). (Cited on page 9.)
[145] Damour, T., “The problem of motion in Newtonian and Einsteinian gravity”, in Hawking, S. W.
and Israel, W., eds., Three Hundred Years of Gravitation, pp. 128–198, (Cambridge University Press,
Cambridge; New York, 1987). [ADS]. (Cited on pages 9 and 70.)
[146] Damour, T., “Gravitational self-force in a Schwarzschild background and the effective one-body
formalism”, Phys. Rev. D, 81, 024017 (2010). [DOI], [arXiv:0910.5533 [gr-qc]]. (Cited on page 114.)
[147] Damour, T. and Deruelle, N., “Lagrangien généralisé du système de deux masses ponctuelles, à
l’approximation post-post-newtonienne de la relativité générale”, C. R. Acad. Sci. Ser. II, 293,
537–540 (1981). (Cited on pages 7, 17, and 84.)
[148] Damour, T. and Deruelle, N., “Radiation reaction and angular momentum loss in small angle gravitational scattering”, Phys. Lett. A, 87, 81–84 (1981). [DOI]. (Cited on pages 7 and 17.)
[149] Damour, T. and Deruelle, N., “General relativistic celestial mechanics of binary systems I. The postNewtonian motion”, Ann. Inst. Henri Poincare A, 43, 107–132 (1985). Online version (accessed 17
October 2013):
http://www.numdam.org/item?id=AIHPA_1985__43_1_107_0.
(Cited on pages 135, 137, 138,
and 140.)
[150] Damour, T. and Deruelle, N., “General relativistic celestial mechanics of binary systems II. The
post-Newtonian timing formula”, Ann. Inst. Henri Poincare A, 44, 263–292 (1986). Online version
(accessed 17 October 2013):
http://www.numdam.org/item?id=AIHPA_1986__44_3_263_0. (Cited on page 137.)
[151] Damour, T. and Esposito-Farèse, G., “Testing gravity to second post-Newtonian order: A fieldtheory approach”, Phys. Rev. D, 53, 5541–5578 (1996). [DOI], [ADS], [gr-qc/9506063]. (Cited on
pages 18 and 71.)
[152] Damour, T. and Gopakumar, A., “Gravitational recoil during binary black hole coalescence using
the effective one body approach”, Phys. Rev. D, 73, 124006 (2006). [DOI], [gr-qc/0602117]. (Cited
on page 22.)
[153] Damour, T., Gopakumar, A. and Iyer, B. R., “Phasing of gravitational waves from inspiralling
eccentric binaries”, Phys. Rev. D, 70, 064028 (2004). [DOI], [gr-qc/0404128]. (Cited on pages 141,
145, and 146.)
[154] Damour, T. and Iyer, B. R., “Multipole analysis for electromagnetism and linearized gravity with
irreducible Cartesian tensors”, Phys. Rev. D, 43, 3259–3272 (1991). [DOI]. (Cited on pages 10
and 51.)
[155] Damour, T. and Iyer, B. R., “Post-Newtonian generation of gravitational waves. II. The spin moments”, Ann. Inst. Henri Poincare A, 54, 115–164 (1991). Online version (accessed 17 October 2013):
http://www.numdam.org/item?id=AIHPA_1991__54_2_115_0. (Cited on pages 11 and 46.)
[156] Damour, T., Iyer, B. R., Jaranowski, P. and Sathyaprakash, B. S., “Gravitational waves from black
hole binary inspiral and merger: The span of third post-Newtonian effective-one-body templates”,
Phys. Rev. D, 67, 064028 (2003). [DOI], [gr-qc/0211041]. (Cited on pages 65, 71, and 131.)
[157] Damour, T., Iyer, B. R. and Sathyaprakash, B. S., “Improved filters for gravitational waves from
inspiraling compact binaries”, Phys. Rev. D, 57, 885–907 (1998). [DOI], [gr-qc/9708034]. (Cited on
pages 16 and 65.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 171

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

171

[158] Damour, T., Iyer, B. R. and Sathyaprakash, B. S., “Frequency-domain P-approximant filters for
time-truncated inspiral gravitational wave signals from compact binaries”, Phys. Rev. D, 62, 084036
(2000). [DOI], [gr-qc/0001023]. (Cited on page 65.)
[159] Damour, T., Iyer, B. R. and Sathyaprakash, B. S., “Comparison of search templates for gravitational
waves from binary inspiral: 3.5PN update”, Phys. Rev. D, 66, 027502 (2002). [DOI], [gr-qc/0207021].
(Cited on pages 65, 71, and 131.)
[160] Damour, T., Jaranowski, P. and Schäfer, G., “Dynamical invariants for general relativistic twobody systems at the third post-Newtonian approximation”, Phys. Rev. D, 62, 044024 (2000). [grqc/9912092]. (Cited on pages 95 and 110.)
[161] Damour, T., Jaranowski, P. and Schäfer, G., “On the determination of the last stable orbit for
circular general relativistic binaries at the third post-Newtonian approximation”, Phys. Rev. D, 62,
084011 (2000). [ADS], [gr-qc/0005034]. (Cited on page 65.)
[162] Damour, T., Jaranowski, P. and Schäfer, G., “Poincaré invariance in the ADM Hamiltonian approach
to the general relativistic two-body problem”, Phys. Rev. D, 62, 021501(R) (2000). [gr-qc/0003051].
Erratum: Phys. Rev. D, 63, 029903(E) (2000). (Cited on pages 17, 18, 69, 88, and 93.)
[163] Damour, T., Jaranowski, P. and Schäfer, G., “Dimensional regularization of the gravitational interaction of point masses”, Phys. Lett. B, 513, 147–155 (2001). [DOI], [gr-qc/0105038]. (Cited on
pages 18, 70, 74, and 76.)
[164] Damour, T., Jaranowski, P. and Schäfer, G., “Equivalence between the ADM-Hamiltonian and the
harmonic-coordinates approaches to the third post-Newtonian dynamics of compact binaries”, Phys.
Rev. D, 63, 044021 (2001). [DOI], [gr-qc/0010040]. Erratum: Phys. Rev. D, 66, 029901(E) (2002).
(Cited on pages 17, 18, and 70.)
[165] Damour, T., Jaranowski, P. and Schäfer, G., “Hamiltonian of two spinning compact bodies with
next-to-leading order gravitational spin-orbit coupling”, Phys. Rev. D, 77, 064032 (2008). [DOI],
[arXiv:0711.1048]. (Cited on pages 19, 147, and 151.)
[166] Damour, T., Jaranowski, P. and Schäfer, G., “Non-local-in-time action for the fourth postNewtonian conservative dynamics of two-body systems”, Phys. Rev. D, 89, 064058 (2014). [DOI],
[arXiv:1401.4548 [gr-qc]]. (Cited on page 19.)
[167] Damour, T., Jaranowski, P. and Schäfer, G., “Fourth post-Newtonian effective one-body dynamics”,
Phys. Rev. D, 91, 084024 (2015). [DOI], [arXiv:1502.07245 [gr-qc]]. (Cited on page 19.)
[168] Damour, T. and Nagar, A., “The Effective One-Body description of the Two-Body Problem”, in
Blanchet, L., Spallicci, A. and Whiting, B., eds., Mass and Motion in General Relativity, Lectures
from the CNRS School on Mass held in Orléans, France, 23 – 25 June 2008, Fundamental Theories
of Physics, 162, pp. 211–252, (Springer, Dordrecht; New York, 2011). [DOI], [ADS]. (Cited on
page 65.)
[169] Damour, T. and Schäfer, G., “Lagrangians for 𝑛 Point Masses at the Second Post-Newtonian Approximation of General Relativity”, Gen. Relativ. Gravit., 17, 879–905 (1985). [DOI]. (Cited on
pages 17 and 85.)
[170] Damour, T. and Schäfer, G., “Higher-Order Relativistic Periastron Advances in Binary Pulsars”,
Nuovo Cimento B, 101, 127–176 (1988). [DOI]. (Cited on pages 138, 139, and 141.)
[171] Damour, T. and Schmidt, B. G., “Reliability of perturbation theory in general relativity”, J. Math.
Phys., 31, 2441–2458 (1990). [DOI]. (Cited on page 28.)
[172] Damour, T., Soffel, M. and Xu, C., “General-relativistic celestial mechanics. I. Method and definition
of reference systems”, Phys. Rev. D, 43, 3273–3307 (1991). [DOI], [ADS]. (Cited on page 70.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 172

172

Luc Blanchet

[173] Damour, T. and Taylor, J. H., “On the Orbital Period Change of the Binary Pulsar PSR 1913+16”,
Astrophys. J., 366, 501–511 (1991). [DOI], [ADS]. (Cited on page 17.)
[174] de Andrade, V. C., Blanchet, L. and Faye, G., “Third post-Newtonian dynamics of compact binaries: Noetherian conserved quantities and equivalence between the harmonic-coordinate and ADMHamiltonian formalisms”, Class. Quantum Grav., 18, 753–778 (2001). [DOI], [gr-qc/0011063]. (Cited
on pages 17, 18, 71, 85, 86, 87, 88, and 90.)
[175] Deruelle, N., Sur les équations du mouvement et le rayonnement gravitationnel d’un système binaire
en Relativité Générale, Ph.D. thesis, (Université Pierre et Marie Curie, Paris, 1982). (Cited on
page 17.)
[176] Detweiler, S., “Consequence of the gravitational self-force for circular orbits of the Schwarzschild
geometry”, Phys. Rev. D, 77, 124026 (2008). [DOI], [arXiv:0804.3529]. (Cited on pages 109, 112,
114, and 115.)
[177] Detweiler, S., “Elementary Development of the Gravitational Self-Force”, in Blanchet, L., Spallicci,
A. and Whiting, B., eds., Mass and Motion in General Relativity, Lectures from the CNRS School on
Mass held in Orléans, France, 23 – 25 June 2008, Fundamental Theories of Physics, 162, pp. 271–307,
(Springer, Dordrecht; New York, 2011). [DOI], [ADS]. (Cited on pages 9 and 112.)
[178] Detweiler, S. and Whiting, B. F., “Self-force via a Green’s function decomposition”, Phys. Rev. D,
67, 024025 (2003). [DOI], [arXiv:gr-qc/0202086]. (Cited on pages 112 and 115.)
[179] Dixon, W. G., “Extended bodies in general relativity: Their description and motion”, in Ehlers, J.,
ed., Isolated Gravitating Systems in General Relativity (Sistemi gravitazionali isolati in relatività generale), Proceedings of the International School of Physics ‘Enrico Fermi’, Course 67, Varenna on Lake
Como, Villa Monastero, Italy, 28 June – 10 July, 1976, pp. 156–219, (North-Holland, Amsterdam;
New York, 1979). (Cited on pages 148 and 150.)
[180] Eder, E., “Existence, uniqueness and iterative construction of motions of charged particles with
retarded interactions”, Ann. Inst. Henri Poincare A, 39, 1–27 (1983). Online version (accessed 17
October 2013):
http://www.numdam.org/item?id=AIHPA_1983__39_1_1_0. (Cited on page 38.)
[181] Ehlers, J., “Isolated systems in general relativity”, Ann. N.Y. Acad. Sci., 336, 279–294 (1980).
[DOI]. (Cited on pages 53 and 57.)
[182] Ehlers, J., Rosenblum, A., Goldberg, J. N. and Havas, P., “Comments on gravitational radiation
damping and energy loss in binary systems”, Astrophys. J. Lett., 208, L77–L81 (1976). [DOI], [ADS].
(Cited on page 54.)
[183] Einstein, A., “Über Gravitationswellen”, Sitzungsber. K. Preuss. Akad. Wiss., 1918, 154–167 (1918).
[ADS]. Online version (accessed 31 January 2014):
http://echo.mpiwg-berlin.mpg.de/MPIWG:8HSP60BU. (Cited on pages 9 and 12.)
[184] Einstein, A., Infeld, L. and Hoffmann, B., “The Gravitational Equations and the Problem of Motion”,
Ann. Math. (2), 39, 65–100 (1938). [DOI]. (Cited on pages 7, 17, and 70.)
[185] Epstein, R. and Wagoner, R. V., “Post-Newtonian Generation of Gravitational Waves”, Astrophys.
J., 197, 717–723 (1975). [DOI], [ADS]. (Cited on pages 11, 20, and 50.)
[186] Esposito, L. W. and Harrison, E. R., “Properties of the Hulse-Taylor binary pulsar system”, Astrophys. J. Lett., 196, L1–L2 (1975). [DOI]. (Cited on page 13.)
[187] Faber, J. A. and Rasio, F. A., “Binary Neutron Star Mergers”, Living Rev. Relativity, 15, lrr-2012-8
(2012). [DOI], [ADS], [arXiv:1204.3858 [gr-qc]]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2012-8. (Cited on pages 8 and 16.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 173

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

173

[188] Fabian, A. C. and Miniutti, G., “The X-ray spectra of accreting Kerr black holes”, in Wiltshire, D. L.,
Visser, M. and Scott, S. M., eds., The Kerr Spacetime: Rotating Black Holes in General Relativity,
9, (Cambridge University Press, Cambridge; New York, 2009). [ADS], [arXiv:astro-ph/0507409].
(Cited on page 146.)
[189] Favata, M., “Post-Newtonian corrections to the gravitational-wave memory for quasicircular, inspiralling compact binaries”, Phys. Rev. D, 80, 024002 (2009). [DOI], [ADS], [arXiv:0812.0069]. (Cited
on pages 21, 43, 130, and 134.)
[190] Favata, M., “Conservative corrections to the innermost stable circular orbit (ISCO) of a Kerr black
hole: a new gauge-invariant post-Newtonian ISCO condition, and the ISCO shift due to test-particle
spin and the gravitational self-force”, Phys. Rev. D, 83, 024028 (2011). [DOI], [arXiv:1010.2553].
(Cited on page 108.)
[191] Favata, M., “Conservative self-force correction to the innermost stable circular orbit: comparison with multiple post-Newtonian-based methods”, Phys. Rev. D, 83, 024027 (2011). [DOI],
[arXiv:1008.4622]. (Cited on page 108.)
[192] Favata, M., “The gravitational-wave memory from eccentric binaries”, Phys. Rev. D, 84, 124013
(2011). [DOI], [arXiv:1108.3121]. (Cited on pages 21 and 43.)
[193] Faye, G., Equations du mouvement d’un système binaire d’objets compact à l’approximation postnewtonienne, Ph.D. thesis, (Université Paris VI, Paris, 1999). (Cited on page 75.)
[194] Faye, G., Blanchet, L. and Buonanno, A., “Higher-order spin effects in the dynamics of compact
binaries I. Equations of motion”, Phys. Rev. D, 74, 104033 (2006). [DOI], [gr-qc/0605139]. (Cited
on pages 19 and 147.)
[195] Faye, G., Blanchet, L. and Iyer, B. R., “Non-linear multipole interactions and gravitational-wave
octupole modes for inspiralling compact binaries to third-and-a-half post-Newtonian order”, Class.
Quantum Grav., 32, 045016 (2015). [arXiv:1409.3546 [gr-qc]]. (Cited on page 132.)
[196] Faye, G., Jaranowski, P. and Schäfer, G., “Skeleton approximate solution of the Einstein field equations for multiple black-hole systems”, Phys. Rev. D, 69, 124029 (2004). [DOI], [gr-qc/0311018].
(Cited on page 103.)
[197] Faye, G., Marsat, S., Blanchet, L. and Iyer, B. R., “The third and a half post-Newtonian gravitational
wave quadrupole mode for quasi-circular inspiralling compact binaries”, Class. Quantum Grav., 29,
175004 (2012). [DOI], [arXiv:1204.1043]. (Cited on pages 11, 20, 31, 40, 44, 45, 117, 118, 125, 131,
and 132.)
[198] Finn, L. S. and Chernoff, D. F., “Observing binary inspiral in gravitational radiation: One interferometer”, Phys. Rev. D, 47, 2198–2219 (1993). [DOI], [arXiv:gr-qc/9301003]. (Cited on pages 16
and 65.)
[199] Fitchett, M. J., “The influence of gravitational wave momentum losses on the centre of mass motion
of a Newtonian binary system”, Mon. Not. R. Astron. Soc., 203, 1049–1062 (1983). [ADS]. (Cited
on page 22.)
[200] Flanagan, É.É. and Hinderer, T., “Constraining neutron star tidal Love numbers with gravitational
wave detectors”, Phys. Rev. D, 77, 021502 (2008). [DOI], [ADS], [arXiv:0709.1915 [astro-ph]]. (Cited
on page 16.)
[201] Fock, V. A., “On motion of finite masses in general relativity”, J. Phys. (Moscow), 1(2), 81–116
(1939). (Cited on page 17.)
[202] Fock, V. A., Theory of space, time and gravitation, (Pergamon, London, 1959). (Cited on pages 33
and 97.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 174

174

Luc Blanchet

[203] Foffa, S. and Sturani, R., “Effective field theory calculation of conservative binary dynamics at third
post-Newtonian order”, Phys. Rev. D, 84, 044031 (2011). [DOI], [arXiv:1104.1122 [gr-qc]]. (Cited
on pages 18 and 71.)
[204] Foffa, S. and Sturani, R., “The dynamics of the gravitational two-body problem in the postNewtonian approximation at quadratic order in the Newton’s constant”, Phys. Rev. D, 87, 064011
(2012). [arXiv:1206.7087 [gr-qc]]. (Cited on pages 19 and 96.)
[205] Foffa, S. and Sturani, R., “Tail terms in gravitational radiation reaction via effective field theory”,
Phys. Rev. D, 87, 044056 (2013). [DOI], [arXiv:1111.5488 [gr-qc]]. (Cited on page 19.)
[206] Foffa, S. and Sturani, R., “Effective field theory methods to model compact binaries”, Class. Quantum
Grav., 31, 043001 (2014). [DOI], [ADS], [arXiv:1309.3474 [gr-qc]]. (Cited on page 18.)
[207] Fokker, A. D., “Ein invarianter Variationssatz für die Bewegung mehrerer elektrischer Massenteilchen”, Z. Phys., 58, 386–393 (1929). [DOI], [ADS]. (Cited on page 18.)
[208] Friedman, J. L., Uryū, K. and Shibata, M., “Thermodynamics of binary black holes and neutron
stars”, Phys. Rev. D, 65, 064035 (2002). [DOI]. Erratum: Phys. Rev. D, 70, 129904(E) (2004).
(Cited on pages 108, 110, and 112.)
[209] Fujita, R., “Gravitational Radiation for Extreme Mass Ratio Inspirals to the 14th Post-Newtonian
Order”, Prog. Theor. Phys., 127, 583–590 (2012). [DOI], [arXiv:1104.5615 [gr-qc]].
(Cited on
page 21.)
[210] Fujita, R., “Gravitational Waves from a Particle in Circular Orbits around a Schwarzschild Black
Hole to the 22nd Post-Newtonian Order”, Prog. Theor. Phys., 128, 971–992 (2012). [DOI], [ADS],
[arXiv:1211.5535 [gr-qc]]. (Cited on page 21.)
[211] Futamase, T., “Gravitational radiation reaction in the Newtonian limit”, Phys. Rev. D, 28, 2373–
2381 (1983). [DOI]. (Cited on page 54.)
[212] Futamase, T., “Strong-field point-particle limit and the equations of motion in the binary pulsar”,
Phys. Rev. D, 36, 321–329 (1987). [DOI]. (Cited on page 70.)
[213] Futamase, T. and Itoh, Y., “The Post-Newtonian Approximation for Relativistic Compact Binaries”,
Living Rev. Relativity, 10, lrr-2007-2 (2007). [DOI], [ADS]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2007-2. (Cited on page 17.)
[214] Futamase, T. and Schutz, B. F., “Newtonian and post-Newtonian approximations are asymptotic to
general relativity”, Phys. Rev. D, 28, 2363–2372 (1983). [DOI]. (Cited on page 54.)
[215] Galley, C. R., Leibovich, A. K., Porto, R. A. and Ross, A., “The tail effect in gravitational
radiation-reaction: time non-locality and renormalization group evolution”, arXiv, e-print, (2015).
[arXiv:1511.07379 [gr-qc]]. (Cited on page 19.)
[216] Gal’tsov, D. V., Matiukhin, A. A. and Petukhov, V. I., “Relativistic corrections to the gravitational
radiation of a binary system and the fine structure of the spectrum”, Phys. Lett. A, 77, 387–390
(1980). [DOI]. (Cited on page 21.)
[217] Gergely, L.Á., “Spin-spin effects in radiating compact binaries”, Phys. Rev. D, 61, 024035 (1999).
[DOI], [gr-qc/9911082]. (Cited on page 147.)
[218] Gergely, L.Á., “Second post-Newtonian radiative evolution of the relative orientations of angular
momenta in spinning compact binaries”, Phys. Rev. D, 62, 024007 (2000). [DOI], [gr-qc/0003037].
(Cited on pages 147 and 159.)
[219] Geroch, R., “Multipole Moments. II. Curved Space”, J. Math. Phys., 11, 2580–2588 (1970). [DOI],
[ADS]. (Cited on page 10.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 175

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

175

[220] Geroch, R. and Horowitz, G. T., “Asymptotically simple does not imply asymptotically
Minkowskian”, Phys. Rev. Lett., 40, 203–206 (1978). (Cited on pages 10, 11, 34, and 35.)
[221] Goldberger, W. D. and Ross, A., “Gravitational radiative corrections from effective field theory”,
Phys. Rev. D, 81, 124015 (2010). [DOI], [arXiv:0912.4254]. (Cited on page 20.)
[222] Goldberger, W. D., Ross, A. and Rothstein, I. Z., “Black hole mass dynamics and renormalization
group evolution”, Phys. Rev. D, 89, 124033 (2014). [DOI], [ADS], [arXiv:1211.6095 [hep-th]]. (Cited
on pages 18 and 44.)
[223] Goldberger, W. D. and Rothstein, I. Z., “Effective field theory of gravity for extended objects”, Phys.
Rev. D, 73, 104029 (2006). [DOI], [arXiv:hep-th/0409156 [hep-th]]. (Cited on pages 18, 71, and 72.)
[224] Gopakumar, A. and Iyer, B. R., “Gravitational waves from inspiraling compact binaries: Angular
momentum flux, evolution of the orbital elements and the waveform to the second post-Newtonian
order”, Phys. Rev. D, 56, 7708–7731 (1997). [DOI], [arXiv:gr-qc/9710075]. (Cited on pages 20, 140,
and 145.)
[225] Gopakumar, A. and Iyer, B. R., “Second post-Newtonian gravitational wave polarizations for compact binaries in elliptical orbits”, Phys. Rev. D, 65, 084011 (2002). [DOI], [arXiv:gr-qc/0110100].
(Cited on page 140.)
[226] Gopakumar, A., Iyer, B. R. and Iyer, S., “Second post-Newtonian gravitational radiation reaction
for two-body systems: Nonspinning bodies”, Phys. Rev. D, 55, 6030–6053 (1997). [DOI], [arXiv:grqc/9703075]. (Cited on page 18.)
[227] Gou, L. et al., “The extreme spin of the black hole in Cygnus X-1”, Astrophys. J., 742, 85 (2011).
[DOI], [arXiv:1106.3690 [astro-ph.HE]]. (Cited on page 146.)
[228] Gourgoulhon, E., Grandclément, P. and Bonazzola, S., “Binary black holes in circular orbits. I. A
global spacetime approach”, Phys. Rev. D, 65, 044020 (2002). [DOI], [ADS], [gr-qc/0106015]. (Cited
on pages 101, 103, 104, and 110.)
[229] Gourgoulhon, E., Grandclément, P., Taniguchi, K., Marck, J.-A. and Bonazzola, S., “Quasiequilibrium sequences of synchronized and irrotational binary neutron stars in general relativity”,
Phys. Rev. D, 63, 064029 (2001). [DOI], [gr-qc/0007028]. (Cited on page 101.)
[230] Gradshteyn, I. S. and Ryzhik, I. M., Table of Integrals, Series and Products, (Academic Press, San
Diego; London, 1980). (Cited on page 121.)
[231] Gralla, S. E. and Wald, R. M., “A rigorous derivation of gravitational self-force”, Class. Quantum
Grav., 25, 205009 (2008). [DOI], [arXiv:0806.3293]. (Cited on page 112.)
[232] Grandclément, P., Gourgoulhon, E. and Bonazzola, S., “Binary black holes in circular orbits. II.
Numerical methods and first results”, Phys. Rev. D, 65, 044021 (2002). [DOI], [ADS]. (Cited on
pages 101, 102, 103, 104, and 110.)
[233] Grandclément, P. and Novak, J., “Spectral Methods for Numerical Relativity”, Living Rev. Relativity,
12, lrr-2009-1 (2009). [DOI], [ADS], [arXiv:0706.2286 [gr-qc]]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2009-1. (Cited on page 8.)
[234] Grishchuk, L. P. and Kopeikin, S. M., “Equations of motion for isolated bodies with relativistic
corrections including the radiation-reaction force”, in Kovalevsky, J. and Brumberg, V. A., eds.,
Relativity in Celestial Mechanics and Astrometry: High Precision Dynamical Theories and Observational Verifications, Proceedings of the 114th Symposium of the International Astronomical Union,
held in Leningrad, USSR, May 28 – 31, 1985, pp. 19–34, (Reidel, Dordrecht; Boston, 1986). (Cited
on pages 17 and 70.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 176

176

Luc Blanchet

[235] Gultekin, K., Miller, M. C. and Hamilton, D. P., “Growth of Intermediate-Mass Black Holes in
Globular Clusters”, Astrophys. J., 616, 221 (2004). [DOI], [astro-ph/0402532]. (Cited on pages 135
and 145.)
[236] Hadamard, J., Le problème de Cauchy et les équations aux dérivées partielles linéaires hyperboliques,
(Hermann, Paris, 1932). (Cited on pages 7 and 66.)
[237] Hannam, M., Husa, S., González, J. A., Sperhake, U. and Brügmann, B., “Where post-Newtonian
and numerical-relativity waveforms meet”, Phys. Rev. D, 77, 044020 (2008). [DOI], [ADS],
[arXiv:0706.1305]. (Cited on page 36.)
[238] Hansen, R. O., “Multipole moments of stationary space-times”, J. Math. Phys., 15, 46–52 (1974).
[DOI], [ADS]. (Cited on page 10.)
[239] Hanson, A. J. and Regge, T., “The Relativistic Spherical Top”, Ann. Phys. (N.Y.), 87, 498–566
(1974). [DOI]. (Cited on pages 148 and 150.)
[240] Hari Dass, N. D. and Soni, V., “Feynman graph derivation of the Einstein quadrupole formula”, J.
Phys. A: Math. Gen., 15, 473–492 (1982). [DOI]. (Cited on page 18.)
[241] Hartung, J. and Steinhoff, J., “Next-to-leading order spin-orbit and spin(a)-spin(b) Hamiltonians for
𝑛 gravitating spinning compact objects”, Phys. Rev. D, 83, 044008 (2011). [DOI], [arXiv:1011.1179
[gr-qc]]. (Cited on pages 19 and 147.)
[242] Hartung, J. and Steinhoff, J., “Next-to-next-to-leading order post-Newtonian spin-orbit Hamiltonian for self-gravitating binaries”, Ann. Phys. (Berlin), 523, 783–790 (2011). [DOI], [ADS],
[arXiv:1104.3079 [gr-qc]]. (Cited on pages 19 and 147.)
[243] Hartung, J. and Steinhoff, J., “Next-to-next-to-leading order post-Newtonian spin(1)-spin(2) Hamiltonian for self-gravitating binaries”, Ann. Phys. (Berlin), 523, 919–924 (2011). [DOI], [ADS],
[arXiv:1107.4294 [gr-qc]]. (Cited on pages 19 and 147.)
[244] Hartung, J., Steinhoff, J. and Schäfer, G., “Next-to-next-to-leading order post-Newtonian
linear-in-spin binary Hamiltonians”, Ann. Phys. (Berlin), 525, 359–394 (2013). [DOI], [ADS],
[arXiv:1302.6723 [gr-qc]]. (Cited on pages 19 and 147.)
[245] Hergt, S. and Schäfer, G., “Higher-order-in-spin interaction Hamiltonians for binary black holes from
Poincaré invariance”, Phys. Rev. D, 78, 124004 (2008). [DOI], [arXiv:0809.2208 [gr-qc]]. (Cited on
page 147.)
[246] Hergt, S. and Schäfer, G., “Higher-order-in-spin interaction Hamiltonians for binary black holes from
source terms of Kerr geometry in approximate ADM coordinates”, Phys. Rev. D, 77, 104001 (2008).
[DOI], [arXiv:0712.1515 [gr-qc]]. (Cited on page 147.)
[247] Hergt, S., Steinhoff, J. and Schäfer, G., “The reduced Hamiltonian for next-to-leading-order spinsquared dynamics of general compact binaries”, Class. Quantum Grav., 27, 135007 (2010). [DOI],
[arXiv:1002.2093 [gr-qc]]. (Cited on pages 19 and 147.)
[248] Hopper, S., Kavanagh, C. and Ottewill, A. C., “Analytic self-force calculations in the post-Newtonian
regime: eccentric orbits on a Schwarzschild background”, Phys. Rev. D, 93, 044010 (2016). [DOI],
[arXiv:1512.01556 [gr-qc]]. (Cited on page 19.)
[249] Hotokezaka, K., Kyutoku, K. and Shibata, M., “Exploring tidal effects of coalescing binary neutron
stars in numerical relativity”, Phys. Rev. D, 87, 044001 (2013). [DOI], [arXiv:1301.3555 [gr-qc]].
(Cited on page 16.)
[250] Hulse, R. A. and Taylor, J. H., “Discovery of a pulsar in a binary system”, Astrophys. J., 195,
L51–L53 (1975). [DOI], [ADS]. (Cited on page 7.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 177

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

177

[251] Hunter, A. J. and Rotenberg, M. A., “The double-series approximation method in general relativity.
I. Exact solution of the (24) approximation. II. Discussion of ‘wave tails’ in the (2s) approximation”,
J. Phys. A: Math. Gen., 2, 34–49 (1969). [DOI]. (Cited on pages 10 and 26.)
[252] Isaacson, R. A. and Winicour, J., “Harmonic and Null Descriptions of Gravitational Radiation”,
Phys. Rev., 168, 1451–1456 (1968). [DOI]. (Cited on page 33.)
[253] Itoh, Y., “Equation of motion for relativistic compact binaries with the strong field point particle
limit: Third post-Newtonian order”, Phys. Rev. D, 69, 064018 (2004). [DOI]. (Cited on pages 17,
18, 70, and 71.)
[254] Itoh, Y., “Third-and-a-half order post-Newtonian equations of motion for relativistic compact
binaries using the strong field point particle limit”, Phys. Rev. D, 80, 124003 (2009). [DOI],
[arXiv:0911.4232 [gr-qc]]. (Cited on pages 18, 70, 78, 92, and 117.)
[255] Itoh, Y. and Futamase, T., “New derivation of a third post-Newtonian equation of motion for
relativistic compact binaries without ambiguity”, Phys. Rev. D, 68, 121501(R) (2003). [DOI], [grqc/0310028]. (Cited on pages 17, 18, 70, and 71.)
[256] Itoh, Y....., Futamase, T. and Asada, H., “Equation of motion for relativistic compact binaries with
the strong field point particle limit: Formulation, the first post-Newtonian order, and multipole
terms”, Phys. Rev. D, 62, 064002 (2000). [DOI], [gr-qc/9910052]. (Cited on pages 17, 18, and 70.)
[257] Itoh, Y., Futamase, T. and Asada, H., “Equation of motion for relativistic compact binaries with
the strong field point particle limit: The second and half post-Newtonian order”, Phys. Rev. D, 63,
064038 (2001). [DOI], [gr-qc/0101114]. (Cited on pages 17, 18, and 70.)
[258] Iyer, B. R. and Will, C. M., “Post-Newtonian gravitational radiation reaction for two-body systems”,
Phys. Rev. Lett., 70, 113–116 (1993). [DOI]. (Cited on pages 18, 64, 78, 84, 92, and 117.)
[259] Iyer, B. R. and Will, C. M., “Post-Newtonian gravitational radiation reaction for two-body systems:
Nonspinning bodies”, Phys. Rev. D, 52, 6882–6893 (1995). [DOI]. (Cited on pages 18, 64, 78, 84,
92, and 117.)
[260] Jaranowski, P. and Schäfer, G., “Radiative 3.5 post-Newtonian ADM Hamiltonian for many-body
point-mass systems”, Phys. Rev. D, 55, 4712–4722 (1997). [DOI]. (Cited on pages 18, 78, 92,
and 117.)
[261] Jaranowski, P. and Schäfer, G., “Third post-Newtonian higher order ADM Hamilton dynamics for
two-body point-mass systems”, Phys. Rev. D, 57, 7274–7291 (1998). [DOI], [gr-qc/9712075]. (Cited
on pages 17, 68, 69, 86, 87, 88, and 93.)
[262] Jaranowski, P. and Schäfer, G., “Binary black-hole problem at the third post-Newtonian approximation in the orbital motion: Static part”, Phys. Rev. D, 60, 124003 (1999). [DOI], [gr-qc/9906092].
(Cited on pages 17, 68, 69, 86, 87, 88, and 93.)
[263] Jaranowski, P. and Schäfer, G., “The binary black-hole dynamics at the third post-Newtonian order
in the orbital motion”, Ann. Phys. (Berlin), 9, 378–383 (2000). [DOI], [gr-qc/0003054]. (Cited on
pages 17, 68, and 88.)
[264] Jaranowski, P. and Schäfer, G., “Towards the fourth post-Newtonian Hamiltonian for two-point-mass
systems”, Phys. Rev. D, 86, 061503(R) (2012). [DOI], [arXiv:1207.5448 [gr-qc]]. (Cited on pages 19
and 96.)
[265] Jaranowski, P. and Schäfer, G., “Dimensional regularization of local singularities in the 4th
post-Newtonian two-point-mass Hamiltonian”, Phys. Rev. D, 87, 081503(R) (2013). [DOI],
[arXiv:1303.3225 [gr-qc]]. (Cited on pages 19 and 96.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 178

178

Luc Blanchet

[266] Jaranowski, P. and Schäfer, G., “Derivation of the local-in-time fourth post-Newtonian ADM Hamiltonian for spinless compact binaries”, Phys. Rev. D, 92, 124043 (2015). [DOI], [arXiv:1508.01016
[gr-qc]]. (Cited on page 19.)
[267] Junker, W. and Schäfer, G., “Binary systems: higher order gravitational radiation damping and wave
emission”, Mon. Not. R. Astron. Soc., 254, 146–164 (1992). [ADS]. (Cited on pages 140 and 145.)
[268] Kavanagh, C., Ottewill, A. C. and Wardell, B., “Analytical high-order post-Newtonian expansions
for extreme mass ratio binaries”, Phys. Rev. D, 92, 084025 (2015). [DOI], [ADS], [arXiv:1503.02334
[gr-qc]]. (Cited on page 116.)
[269] Kerlick, G. D., “Finite reduced hydrodynamic equations in the slow-motion approximation to general
relativity. Part I. First post-Newtonian equations”, Gen. Relativ. Gravit., 12, 467–482 (1980). [DOI].
(Cited on pages 53 and 57.)
[270] Kerlick, G. D., “Finite reduced hydrodynamic equations in the slow-motion approximation to general
relativity. Part II. Radiation reaction and higher-order divergent terms”, Gen. Relativ. Gravit., 12,
521–543 (1980). [DOI]. (Cited on pages 53 and 57.)
[271] Kidder, L. E., “Coalescing binary systems of compact objects to (post)5/2 -Newtonian order. V. Spin
effects”, Phys. Rev. D, 52, 821–847 (1995). [DOI], [ADS]. (Cited on pages 19, 21, 22, 102, 147, 150,
and 152.)
[272] Kidder, L. E., “Using full information when computing modes of post-Newtonian waveforms
from inspiralling compact binaries in circular orbits”, Phys. Rev. D, 77, 044016 (2008). [DOI],
[arXiv:0710.0614]. (Cited on pages 20, 36, 37, 131, and 134.)
[273] Kidder, L. E., Blanchet, L. and Iyer, B. R., “A note on the radiation reaction in the 2.5PN waveform
from inspiralling binaries in quasi-circular orbits”, Class. Quantum Grav., 24, 5307 (2007). [DOI],
[arXiv:0706.0726]. (Cited on page 20.)
[274] Kidder, L. E., Will, C. M. and Wiseman, A. G., “Coalescing binary systems of compact objects to
(post)5/2 -Newtonian order. III. Transition from inspiral to plunge”, Phys. Rev. D, 47, 3281–3291
(1993). [DOI], [ADS]. (Cited on page 103.)
[275] Kidder, L. E., Will, C. M. and Wiseman, A. G., “Spin effects in the inspiral of coalescing compact
binaries”, Phys. Rev. D, 47, R4183–R4187 (1993). [DOI]. (Cited on pages 19, 21, 102, 104, 105,
and 147.)
[276] Kochanek, C. S., “Coalescing binary neutron stars”, Astrophys. J., 398, 234–247 (1992). [DOI],
[ADS]. (Cited on page 15.)
[277] Kol, B. and Smolkin, M., “Non-relativistic gravitation: From Newton to Einstein and back”, Class.
Quantum Grav., 25, 145011 (2008). [DOI], [arXiv:0712.4116 [hep-th]]. (Cited on page 18.)
[278] Königsdörffer, C., Faye, G. and Schäfer, G., “The binary black-hole dynamics at the third-and-a-half
post-Newtonian order in the ADM-formalism”, Phys. Rev. D, 68, 044004 (2003). [DOI], [astroph/0305048]. (Cited on pages 18, 78, 92, and 117.)
[279] Königsdörffer, C. and Gopakumar, A., “Phasing of gravitational waves from inspiralling eccentric
binaries at the third-and-a-half post-Newtonian order”, Phys. Rev. D, 73, 124012 (2006). [DOI],
[ADS], [gr-qc/0603056]. (Cited on page 146.)
[280] Kopeikin, S. M., “The equations of motion of extended bodies in general-relativity with conservative
corrections and radiation damping taken into account”, Astron. Zh., 62, 889–904 (1985). (Cited on
pages 17 and 70.)
[281] Kopeikin, S. M., “Celestial Coordinate Reference Systems in Curved Spacetime”, Celest. Mech., 44,
87 (1988). [DOI]. (Cited on page 70.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 179

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

179

[282] Kopeikin, S. M., Schäfer, G., Gwinn, C. R. and Eubanks, T. M., “Astrometric and timing effects
of gravitational waves from localized sources”, Phys. Rev. D, 59, 084023 (1999). [DOI], [ADS], [grqc/9811003]. (Cited on page 12.)
[283] Kozai, Y., “Secular perturbations of asteroids with high inclination and eccentricity”, Astron. J.,
67, 591–598 (1962). [DOI], [ADS]. (Cited on pages 15 and 135.)
[284] Królak, A., Kokkotas, K. D. and Schäfer, G., “Estimation of the post-Newtonian parameters in
the gravitational-wave emission of a coalescing binary”, Phys. Rev. D, 52, 2089–2111 (1995). [DOI],
[gr-qc/9503013]. (Cited on pages 16, 65, and 124.)
[285] Landau, L. D. and Lifshitz, E. M., The classical theory of fields, (Pergamon Press, Oxford; New
York, 1971), 3rd edition. (Cited on pages 9, 12, and 121.)
[286] Le Tiec, A., “First law of mechanics for compact binaries on eccentric orbits”, Phys. Rev. D, 92,
084021 (2015). [DOI], [arXiv:1506.05648 [gr-qc]]. (Cited on page 111.)
[287] Le Tiec, A., Barausse, E. and Buonanno, A., “Gravitational Self-Force Correction to the Binding
Energy of Compact Binary Systems”, Phys. Rev. Lett., 108, 131103 (2012). [DOI], [arXiv:1111.5609
[gr-qc]]. (Cited on pages 96 and 108.)
[288] Le Tiec, A. and Blanchet, L., “The Close-Limit Approximation for Black Hole Binaries with PostNewtonian Initial Conditions”, Class. Quantum Grav., 27, 045008 (2010). [DOI], [arXiv:0901.4593
[gr-qc]]. (Cited on page 22.)
[289] Le Tiec, A., Blanchet, L. and Whiting, B. F., “First law of binary black hole mechanics in general
relativity and post-Newtonian theory”, Phys. Rev. D, 85, 064039 (2012). [DOI], [arXiv:1111.5378
[gr-qc]]. (Cited on pages 95, 96, 108, 110, 113, and 114.)
[290] Le Tiec, A., Blanchet, L. and Will, C. M., “Gravitational-Wave Recoil from the Ringdown Phase of
Coalescing Black Hole Binaries”, Class. Quantum Grav., 27, 012001 (2010). [DOI], [arXiv:0901.4594
[gr-qc]]. (Cited on page 22.)
[291] Le Tiec, A., Mroué, A. H., Barack, L., Buonanno, A., Pfeiffer, H. P., Sago, N. and Taracchini, A.,
“Periastron Advance in Black-Hole Binaries”, Phys. Rev. Lett., 107, 141101 (2011). [arXiv:1106.3278
[gr-qc]]. (Cited on page 140.)
[292] Levi, M., “Next-to-leading order gravitational spin-orbit coupling in an effective field theory approach”, Phys. Rev. D, 82, 104004 (2010). [DOI], [arXiv:1006.4139 [gr-qc]]. (Cited on pages 19
and 147.)
[293] Levi, M., “Next-to-leading order gravitational spin1-spin2 coupling with Kaluza-Klein reduction”,
Phys. Rev. D, 82, 064029 (2010). [DOI], [ADS], [arXiv:0802.1508 [gr-qc]]. (Cited on pages 19
and 147.)
[294] Levi, M., “Binary dynamics from spin1-spin2 coupling at fourth post-Newtonian order”, Phys. Rev.
D, 85, 064043 (2012). [DOI], [ADS], [arXiv:1107.4322]. (Cited on pages 19 and 147.)
[295] Levi, M. and Steinhoff, J., “Equivalence of ADM Hamiltonian and Effective Field Theory approaches
at next-to-next-to-leading order spin1-spin2 coupling of binary inspirals”, J. Cosmol. Astropart.
Phys., 2014(12), 003 (2014). [DOI], [arXiv:1408.5762 [gr-qc]]. (Cited on page 19.)
[296] Levi, M. and Steinhoff, J., “Leading order finite size effects with spins for inspiralling compact
binaries”, J. High Energy Phys., 2015(06), 059 (2015). [DOI], [arXiv:1410.2601 [gr-qc]]. (Cited on
page 147.)
[297] Levi, M. and Steinhoff, J., “Next-to-next-to-leading order gravitational spin-orbit coupling via the
effective field theory for spinning objects in the post-Newtonian scheme”, arXiv, e-print, (2015).
[arXiv:1506.05056 [gr-qc]]. (Cited on pages 19 and 147.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 180

180

Luc Blanchet

[298] Levi, M. and Steinhoff, J., “Next-to-next-to-leading order gravitational spin-squared potential via
the effective field theory for spinning objects in the post-Newtonian scheme”, arXiv, e-print, (2015).
[arXiv:1506.05794 [gr-qc]]. (Cited on pages 19 and 147.)
[299] Levi, M. and Steinhoff, J., “Spinning gravitating objects in the effective field theory in the postNewtonian scheme”, J. High Energy Phys., 2015(09), 219 (2015). [DOI], [arXiv:1501.04956 [gr-qc]].
(Cited on pages 19 and 147.)
[300] Lidov, M. L., “The evolution of orbits of artificial satellites of planets under the action of gravitational
perturbations of external bodies”, Planet. Space Sci., 9, 719 (1962). [DOI]. (Cited on pages 15
and 135.)
[301] Limousin, F., Gondek-Rosinska, D. and Gourgoulhon, E., “Last orbits of binary strange quark stars”,
Phys. Rev. D, 71, 064012 (2005). [DOI], [ADS], [arXiv:gr-qc/0411127 [gr-qc]]. (Cited on page 101.)
[302] Lincoln, C. W. and Will, C. M., “Coalescing binary systems of compact objects to (post)5/2 Newtonian order: Late-time evolution and gravitational-radiation emission”, Phys. Rev. D, 42,
1123–1143 (1990). [DOI], [ADS]. (Cited on page 92.)
[303] Lorentz, H. A. and Droste, J., “The motion of a system of bodies under the influence of their mutual
attraction, according to Einstein’s theory”, in The Collected Papers of H.A. Lorentz, Vol. 5, pp.
330–355, (Nijhoff, The Hague, 1937). [DOI], Translated from Versl. K. Akad. Wet. Amsterdam, 26,
392 and 649 (1917). (Cited on pages 7 and 17.)
[304] Madore, J., “Gravitational radiation from a bounded source. I”, Ann. Inst. Henri Poincare, 12,
285–305 (1970). Online version (accessed 6 October 2013):
http://www.numdam.org/item?id=AIHPA_1970__12_3_285_0. (Cited on pages 33 and 34.)
[305] Marsat, S., “Cubic order spin effects in the dynamics and gravitational wave energy flux of compact
object binaries”, Class. Quantum Grav., 32, 085008 (2015). [DOI], [arXiv:1411.4118 [gr-qc]]. (Cited
on page 147.)
[306] Marsat, S., Bohé, A., Blanchet, L. and Buonanno, A., “Next-to-leading tail-induced spin-orbit effects
in the gravitational radiation of compact binaries”, Class. Quantum Grav., 31, 025023 (2013). [DOI],
[arXiv:1307.6793 [gr-qc]]. (Cited on pages 21, 147, 154, and 158.)
[307] Marsat, S., Bohé, A., Faye, G. and Blanchet, L., “Next-to-next-to-leading order spin-orbit effects
in the equations of motion of compact binary systems”, Class. Quantum Grav., 30, 055007 (2013).
[DOI], [arXiv:1210.4143]. (Cited on pages 19, 147, 153, and 158.)
[308] Martin, J. and Sanz, J. L., “Slow motion approximation in predictive relativistic mechanics. II.
Non-interaction theorem for interactions derived from the classical field-theory”, J. Math. Phys., 20,
25–34 (1979). [DOI]. (Cited on page 85.)
[309] Mathews, J., “Gravitational multipole radiation”, J. Soc. Ind. Appl. Math., 10, 768–780 (1962).
[DOI]. (Cited on page 10.)
[310] Mathisson, M., “Republication of: New mechanics of material systems”, Gen. Relativ. Gravit., 42,
1011–1048 (2010). [DOI]. (Cited on pages 148 and 150.)
[311] McClintock, J. E., Shafee, R., Narayan, R., Remillard, R. A., Davis, S. W. and Li, L.-X., “The Spin
of the Near-Extreme Kerr Black Hole GRS 1915+105”, Astrophys. J., 652, 518–539 (2006). [DOI],
[ADS], [arXiv:astro-ph/0606076]. (Cited on page 146.)
[312] Memmesheimer, R., Gopakumar, A. and Schäfer, G., “Third post-Newtonian accurate generalized
quasi-Keplerian parametrization for compact binaries in eccentric orbits”, Phys. Rev. D, 70, 104011
(2004). [DOI], [gr-qc/0407049]. (Cited on pages 135, 138, 140, and 141.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 181

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

181

[313] Merritt, D., Milosavljević, M., Favata, M., Hughes, S. A. and Holz, D. E., “Consequences of Gravitational Radiation Recoil”, Astrophys. J. Lett., 607, L9–L12 (2004). [DOI], [ADS], [astro-ph/0402057].
(Cited on page 21.)
[314] Mikóczi, B., Vasúth, M. and Gergely, L.Á., “Self-interaction spin effects in inspiralling compact
binaries”, Phys. Rev. D, 71, 124043 (2005). [DOI], [astro-ph/0504538]. (Cited on pages 21 and 147.)
[315] Miller, M. C. and Hamilton, D. P., “Four-Body Effects in Globular Cluster Black Hole Coalescence”,
Astrophys. J., 576, 894 (2002). [DOI], [astro-ph/0202298]. (Cited on page 15.)
[316] Mino, Y., Sasaki, M., Shibata, M., Tagoshi, H. and Tanaka, T., “Black Hole Perturbation”, Prog.
Theor. Phys. Suppl., 128, 1–121 (1997). [DOI], [gr-qc/9712057]. (Cited on page 21.)
[317] Mino, Y., Sasaki, M. and Tanaka, T., “Gravitational radiation reaction to a particle motion”, Phys.
Rev. D, 55, 3457–3476 (1997). [DOI], [arXiv:gr-qc/9606018]. (Cited on page 112.)
[318] Mirshekari, S. and Will, C. M., “Compact binary systems in scalar-tensor gravity: Equations of motion to 2.5 post-Newtonian order”, Phys. Rev. D, 87, 084070 (2013). [DOI], [ADS], [arXiv:1301.4680
[gr-qc]]. (Cited on page 17.)
[319] Misner, C. W., Thorne, K. S. and Wheeler, J. A., Gravitation, (W. H. Freeman, San Francisco,
1973). [ADS]. (Cited on pages 13, 14, and 150.)
[320] Mora, T. and Will, C. M., “Post-Newtonian diagnostic of quasi-equilibrium binary configurations
of compact objects”, Phys. Rev. D, 69, 104021 (2004). [DOI], [arXiv:gr-qc/0312082]. (Cited on
pages 16, 92, and 93.)
[321] Moritz, H., Advanced Physical Geodesy, (H. Wichmann, Karlsruhe, 1980). (Cited on page 15.)
[322] Nissanke, S. and Blanchet, L., “Gravitational radiation reaction in the equations of motion of compact
binaries to 3.5 post-Newtonian order”, Class. Quantum Grav., 22, 1007–1031 (2005). [DOI], [grqc/0412018]. (Cited on pages 18, 78, 92, and 117.)
[323] Nowak, M. A., Wilms, J., Pottschmidt, K., Schulz, N., Miller, J. and Maitra, D., “Suzaku observations of 4U 1957+11: The most rapidly spinning black hole in the galaxy?”, in Petre, R., Mitsuda, K.
and Angelini, L., eds., SUZAKU 2011. Exploring the X-ray Universe: Suzaku and Beyond (SUZAKU
2011), Palo Alto, California, USA, 20 – 22 July 2011, AIP Conference Proceedings, 1427, pp. 48–51,
(AIP Publishing, Melville, NY, 2012). [DOI], [ADS]. (Cited on page 146.)
[324] Ohta, T., Okamura, H., Kimura, T. and Hiida, K., “Physically acceptable solution of Einstein’s
equation for many-body system”, Prog. Theor. Phys., 50, 492–514 (1973). [DOI]. (Cited on pages 17,
18, and 97.)
[325] Ohta, T., Okamura, H., Kimura, T. and Hiida, K., “Coordinate Condition and Higher Order Gravitational Potential in Canocical Formalism”, Prog. Theor. Phys., 51, 1598–1612 (1974). [DOI]. (Cited
on pages 17 and 18.)
[326] Ohta, T., Okamura, H., Kimura, T. and Hiida, K., “Higher-order gravitational potential for manybody system”, Prog. Theor. Phys., 51, 1220–1238 (1974). [DOI]. (Cited on pages 17 and 18.)
[327] Okamura, H., Ohta, T., Kimura, T. and Hiida, K., “Perturbation calculation of gravitational potentials”, Prog. Theor. Phys., 50, 2066–2079 (1973). [DOI]. (Cited on pages 17 and 18.)
[328] Owen, B. J., Tagoshi, H. and Ohashi, A., “Nonprecessional spin-orbit effects on gravitational waves
from inspiraling compact binaries to second post-Newtonian order”, Phys. Rev. D, 57, 6168–6175
(1998). [DOI], [gr-qc/9710134]. (Cited on page 21.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 182

182

Luc Blanchet

[329] Pan, Y., Buonanno, A., Buchman, L. T., Chu, T., Kidder, L. E., Pfeiffer, H. P. and Scheel,
M. A., “Effective-one-body waveforms calibrated to numerical relativity simulations: Coalescence
of non-precessing, spinning, equal-mass black holes”, Phys. Rev. D, 81, 084041 (2010). [DOI], [ADS],
[arXiv:0912.3466 [gr-qc]]. (Cited on page 65.)
[330] Papapetrou, A., “Equations of motion in general relativity”, Proc. Phys. Soc. London, Sect. B, 64,
57–75 (1951). (Cited on page 17.)
[331] Papapetrou, A., “Spinning Test-Particles in General Relativity. I”, Proc. R. Soc. London, Ser. A,
209, 248–258 (1951). [DOI]. (Cited on pages 148 and 150.)
[332] Papapetrou, A., “Relativité – une formule pour le rayonnement gravitationnel en première approximation”, C. R. Acad. Sci. Ser. II, 255, 1578 (1962). (Cited on page 10.)
[333] Papapetrou, A., “Étude systématique du rayonnement gravitationnel 4-polaire. Énergie-impulsion
et moment cinétique du rayonnement”, Ann. Inst. Henri Poincare, XIV, 79 (1971). (Cited on
page 10.)
[334] Papapetrou, A. and Linet, B., “Equation of motion including the reaction of gravitational radiation”,
Gen. Relativ. Gravit., 13, 335 (1981). [DOI]. (Cited on pages 53 and 57.)
[335] Pati, M. E. and Will, C. M., “Post-Newtonian gravitational radiation and equations of motion via
direct integration of the relaxed Einstein equations: Foundations”, Phys. Rev. D, 62, 124015 (2000).
[DOI], [gr-qc/0007087]. (Cited on pages 11 and 50.)
[336] Pati, M. E. and Will, C. M., “Post-Newtonian gravitational radiation and equations of motion via
direct integration of the relaxed Einstein equations. II. Two-body equations of motion to second postNewtonian order, and radiation reaction to 3.5 post-Newtonian order”, Phys. Rev. D, 65, 104008
(2002). [DOI], [ADS], [gr-qc/0201001]. (Cited on pages 11, 18, 78, 92, and 117.)
[337] Penrose, R., “Asymptotic Properties of Fields and Space-Times”, Phys. Rev. Lett., 10, 66–68 (1963).
[DOI], [ADS]. (Cited on pages 10, 11, 33, and 34.)
[338] Penrose, R., “Zero Rest-Mass Fields Including Gravitation: Asymptotic Behaviour”, Proc. R. Soc.
London, Ser. A, 284, 159–203 (1965). [DOI], [ADS]. (Cited on pages 10, 11, 33, and 34.)
[339] Peters, P. C., “Gravitational Radiation and the Motion of Two Point Masses”, Phys. Rev., 136,
B1224–B1232 (1964). [DOI], [ADS]. (Cited on pages 10, 13, 14, 135, 140, and 145.)
[340] Peters, P. C. and Mathews, J., “Gravitational Radiation from Point Masses in a Keplerian Orbit”,
Phys. Rev., 131, 435–440 (1963). [DOI], [ADS]. (Cited on pages 13, 14, 135, 140, and 143.)
[341] Petrova, N. M., “Ob Uravnenii Dvizheniya i Tenzore Materii dlya Sistemy Konechnykh Mass v
Obshchei Teorii Otnositielnosti”, J. Exp. Theor. Phys., 19(11), 989–999 (1949). (Cited on page 17.)
[342] Pfeiffer, H. P., Teukolsky, S. A. and Cook, G. B., “Quasicircular orbits for spinning binary black
holes”, Phys. Rev. D, 62, 104018 (2000). [DOI], [ADS], [gr-qc/0006084]. (Cited on pages 103
and 104.)
[343] Pirani, F. A. E., “Introduction to Gravitational Radiation Theory”, in Trautman, A., Pirani, F.
A. E. and Bondi, H., eds., Lectures on General Relativity, Vol. 1, Brandeis Summer Institute in
Theoretical Physics 1964, pp. 249–373, (Prentice-Hall, Englewood Cliffs, NJ, 1965). [ADS]. (Cited
on page 10.)
[344] Plebański, J. F. and Bażański, S. L., “The general Fokker action principle and its application in
general relativity theory”, Acta Phys. Pol., 18, 307–345 (1959). (Cited on page 53.)
[345] Poisson, E., “Gravitational radiation from a particle in circular orbit around a black hole. I. Analytic
results for the nonrotating case”, Phys. Rev. D, 47, 1497–1510 (1993). [DOI], [ADS]. (Cited on
pages 21 and 38.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 183

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

183

[346] Poisson, E., “Gravitational radiation from a particle in circular orbit around a black-hole. VI. Accuracy of the post-Newtonian expansion”, Phys. Rev. D, 52, 5719–5723 (1995). [DOI], [gr-qc/9505030].
Erratum: Phys. Rev. D, 55, 7980 (1997). (Cited on pages 16, 65, and 125.)
[347] Poisson, E., “Gravitational waves from inspiraling compact binaries: The quadrupole-moment term”,
Phys. Rev. D, 57, 5287–5290 (1997). [DOI], [gr-qc/9709032]. (Cited on page 147.)
[348] Poisson, E., Pound, A. and Vega, I., “The Motion of Point Particles in Curved Spacetime”, Living
Rev. Relativity, 14, lrr-2011-7 (2011). [DOI], [ADS], [arXiv:1102.0529 [gr-qc]]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2011-7. (Cited on pages 9 and 112.)
[349] Poisson, E. and Sasaki, M., “Gravitational radiation from a particle in circular orbit around a black
hole. V. Black-hole absorption and tail corrections”, Phys. Rev. D, 51, 5753–5767 (1995). [DOI],
[gr-qc/9412027]. (Cited on pages 123 and 158.)
[350] Poisson, E. and Will, C. M., “Gravitational waves from inspiraling compact binaries: Parameter
estimation using second-post-Newtonian wave forms”, Phys. Rev. D, 52, 848–855 (1995). [DOI],
[arXiv:gr-qc/9502040]. (Cited on pages 16, 65, and 124.)
[351] Porto, R. A., “Post-Newtonian corrections to the motion of spinning bodies in NRGR”, Phys. Rev.
D, 73, 104031 (2006). [DOI], [gr-qc/0511061]. (Cited on pages 147 and 148.)
[352] Porto, R. A., “Next-to-leading-order spin–orbit effects in the motion of inspiralling compact binaries”,
Class. Quantum Grav., 27, 205001 (2010). [DOI], [arXiv:1005.5730 [gr-qc]]. (Cited on pages 19
and 147.)
[353] Porto, R. A., Ross, A. and Rothstein, I. Z., “Spin induced multipole moments for the gravitational wave flux from binary inspirals to third Post-Newtonian order”, J. Cosmol. Astropart. Phys.,
2011(3), 009 (2011). [DOI], [arXiv:1007.1312 [gr-qc]]. (Cited on page 21.)
[354] Porto, R. A. and Rothstein, I. Z., “Calculation of the first nonlinear contribution to the generalrelativistic spin-spin interaction for binary systems”, Phys. Rev. Lett., 97, 021101 (2006). [DOI],
[arXiv:gr-qc/0604099]. (Cited on pages 19 and 147.)
[355] Porto, R. A. and Rothstein, I. Z., “Next to leading order spin(1)spin(1) effects in the motion of
inspiralling compact binaries”, Phys. Rev. D, 78, 044013 (2008). [DOI], [ADS], [arXiv:0804.0260
[gr-qc]]. (Cited on pages 19 and 147.)
[356] Porto, R. A. and Rothstein, I. Z., “Spin(1)spin(2) effects in the motion of inspiralling compact
binaries at third order in the post-Newtonian expansion”, Phys. Rev. D, 78, 044012 (2008). [DOI],
[arXiv:0802.0720 [gr-qc]]. (Cited on pages 19 and 147.)
[357] Poujade, O. and Blanchet, L., “Post-Newtonian approximation for isolated systems calculated by
matched asymptotic expansions”, Phys. Rev. D, 65, 124020 (2002). [DOI], [gr-qc/0112057]. (Cited
on pages 11, 54, 55, 56, 57, and 59.)
[358] Press, W. H., “Gravitational Radiation from Sources Which Extend Into Their Own Wave Zone”,
Phys. Rev. D, 15, 965–968 (1977). [DOI]. (Cited on page 10.)
[359] Pretorius, F., “Evolution of Binary Black-Hole Spacetimes”, Phys. Rev. Lett., 95, 121101 (2005).
[DOI], [ADS], [arXiv:gr-qc/0507014]. (Cited on page 8.)
[360] Quinn, T. C. and Wald, R. M., “Axiomatic approach to electromagnetic and gravitational radiation
reaction of particles in curved spacetime”, Phys. Rev. D, 56, 3381–3394 (1997). [DOI], [arXiv:grqc/9610053]. (Cited on page 112.)
[361] Rendall, A. D., “Convergent and divergent perturbation series and the post-Minkowskian scheme”,
Class. Quantum Grav., 7, 803 (1990). [DOI]. (Cited on pages 9 and 28.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 184

184

Luc Blanchet

[362] Rendall, A. D., “On the definition of post-Newtonian approximations”, Proc. R. Soc. London, Ser.
A, 438, 341–360 (1992). [DOI]. (Cited on pages 9, 28, and 54.)
[363] Rendall, A. D., “The Newtonian limit for asymptotically flat solutions of the Einstein-Vlasov system”, Commun. Math. Phys., 163, 89–112 (1994). [DOI], [gr-qc/9303027]. (Cited on pages 9 and 28.)
[364] Reynolds, C. S., “Measuring Black Hole Spin Using X-Ray Reflection Spectroscopy”, Space Sci. Rev.,
183, 277–294 (2014). [DOI], [ADS], [arXiv:1302.3260 [astro-ph.HE]]. (Cited on page 146.)
[365] Riesz, M., “L’intégrale de Riemann–Liouville et le problème de Cauchy”, Acta Math., 81, 1–218
(1949). [DOI]. (Cited on page 67.)
[366] Rieth, R. and Schäfer, G., “Spin and tail effects in the gravitational-wave emission of compact
binaries”, Class. Quantum Grav., 14, 2357 (1997). [DOI]. (Cited on pages 140 and 145.)
[367] Sachs, R. K., “Gravitational waves in general relativity. VI. The outgoing radiation condition”, Proc.
R. Soc. London, Ser. A, 264, 309–338 (1961). [DOI]. (Cited on page 10.)
[368] Sachs, R. K., “Gravitational Waves in General Relativity. VIII. Waves in Asymptotically Flat SpaceTime”, Proc. R. Soc. London, Ser. A, 270, 103–126 (1962). [DOI], [ADS]. (Cited on pages 10, 11,
and 33.)
[369] Sachs, R. K. and Bergmann, P. G., “Structure of Particles in Linearized Gravitational Theory”,
Phys. Rev., 112, 674–680 (1958). [DOI]. (Cited on page 10.)
[370] Sago, N., Barack, L. and Detweiler, S., “Two approaches for the gravitational self force in black
hole spacetime: Comparison of numerical results”, Phys. Rev. D, 78, 124024 (2008). [DOI],
[arXiv:0810.2530]. (Cited on page 109.)
[371] Santamarı́a, L. et al., “Matching post-Newtonian and numerical relativity waveforms: Systematic
errors and a new phenomenological model for non-precessing black hole binaries”, Phys. Rev. D, 82,
064016 (2010). [DOI], [ADS], [arXiv:1005.3306 [gr-qc]]. (Cited on page 65.)
[372] Sasaki, M., “Post-Newtonian Expansion of the Ingoing-Wave Regge-Wheeler Function”, Prog. Theor.
Phys., 92, 17–36 (1994). [DOI]. (Cited on page 21.)
[373] Sasaki, M. and Tagoshi, H., “Analytic Black Hole Perturbation Approach to Gravitational Radiation”, Living Rev. Relativity, 6, lrr-2003-6 (2003). [DOI], [ADS], [arXiv:gr-qc/0306120]. URL (accessed 6 October 2013):
http://www.livingreviews.org/lrr-2003-6. (Cited on page 9.)
[374] Schäfer, G., “Acceleration-dependent Lagrangians in general relativity”, Phys. Lett. A, 100, 128
(1984). [DOI]. (Cited on page 62.)
[375] Schäfer, G., “The Gravitational Quadrupole Radiation-Reaction Force and the Canonical Formalism
of ADM”, Ann. Phys. (N.Y.), 161, 81–100 (1985). [DOI]. (Cited on page 17.)
[376] Schäfer, G., “The ADM Hamiltonian at the Postlinear Approximation”, Gen. Relativ. Gravit., 18,
255–270 (1986). [DOI]. (Cited on page 17.)
[377] Schäfer, G., “Three-body Hamiltonian in general relativity”, Phys. Lett., 123, 336–339 (1987). [DOI].
(Cited on page 97.)
[378] Schäfer, G., “Post-Newtonian Methods: Analytic Results on the Binary Problem”, in Blanchet, L.,
Spallicci, A. and Whiting, B., eds., Mass and Motion in General Relativity, Lectures from the CNRS
School on Mass held in Orléans, France, 23 – 25 June 2008, Fundamental Theories of Physics, 162,
pp. 167–210, (Springer, Dordrecht; New York, 2011). [DOI], [ADS]. (Cited on pages 9 and 108.)
[379] Schäfer, G. and Wex, N., “Second post-Newtonian motion of compact binaries”, Phys. Lett. A, 174,
196–205 (1993). [DOI]. Erratum: Phys. Lett. A, 177, 461 (1993). (Cited on pages 138 and 141.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 185

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

185

[380] Schwartz, L., “Sur l’impossibilité de la multiplication des distributions”, C. R. Acad. Sci. Ser. II,
239, 847–848 (1954). (Cited on pages 68 and 69.)
[381] Schwartz, L., Théorie des distributions, (Hermann, Paris, 1978). (Cited on pages 66, 67, and 75.)
[382] Sellier, A., “Hadamard’s finite part concept in dimension 𝑛 ≥ 2, distributional definition, regularization forms and distributional derivatives”, Proc. R. Soc. London, Ser. A, 445, 69–98 (1994). [DOI].
(Cited on page 66.)
[383] Shah, A., Friedmann, J. and Whiting, B. F., “Finding high-order analytic post-Newtonian parameters
from a high-precision numerical self-force calculation”, Phys. Rev. D, 89, 064042 (2014). [DOI],
[arXiv:1312.1952 [gr-qc]]. (Cited on page 116.)
[384] Simon, W. and Beig, R., “The multipole structure of stationary space-times”, J. Math. Phys., 24,
1163–1171 (1983). [DOI]. (Cited on page 10.)
[385] Sopuerta, C. F., Yunes, N. and Laguna, P., “Gravitational Recoil from Binary Black Hole Mergers:
the Close-Limit Approximation”, Phys. Rev. D, 74, 124010 (2006). [DOI], [astro-ph/0608600]. (Cited
on page 22.)
[386] Steinhoff, J., “Canonical formulation of spin in general relativity”, Ann. Phys. (Berlin), 523, 296
(2011). [DOI], [arXiv:1106.4203 [gr-qc]]. (Cited on page 148.)
[387] Steinhoff, J., Hergt, S. and Schäfer, G., “Next-to-leading order gravitational spin(1)-spin(2) dynamics
in Hamiltonian form”, Phys. Rev. D, 77, 081501(R) (2008). [arXiv:0712.1716 [gr-qc]]. (Cited on
pages 19 and 147.)
[388] Steinhoff, J., Hergt, S. and Schäfer, G., “Spin-squared Hamiltonian of next-to-leading order gravitational interaction”, Phys. Rev. D, 78, 101503(R) (2008). [arXiv:0809.2200 [gr-qc]]. (Cited on
pages 19 and 147.)
[389] Steinhoff, J., Schäfer, G. and Hergt, S., “ADM canonical formalism for gravitating spinning objects”,
Phys. Rev. D, 77, 104018 (2008). [DOI], [arXiv:0805.3136 [gr-qc]]. (Cited on pages 19, 147, and 148.)
[390] Strohmayer, T. E., “Discovery of a 450 Hz quasi-periodic oscillation from the microquasar GRO
J1655–40 with the Rossi X-ray Timing Explorer”, Astrophys. J. Lett., 552, L49–L53 (2001). [DOI],
[ADS]. (Cited on page 146.)
[391] ’t Hooft, G. and Veltman, M., “Regularization and renormalization of gauge fields”, Nucl. Phys. B,
44, 139 (1972). [DOI]. (Cited on page 72.)
[392] Tagoshi, H., Mano, S. and Takasugi, E., “Post-Newtonian Expansion of Gravitational Waves from
a Particle in Circular Orbits around a Rotating Black Hole”, Prog. Theor. Phys., 98, 829 (1997).
[DOI], [gr-qc/9711072]. (Cited on pages 123 and 158.)
[393] Tagoshi, H. and Nakamura, T., “Gravitational waves from a point particle in circular orbit around
a black hole: Logarithmic terms in the post-Newtonian expansion”, Phys. Rev. D, 49, 4016–4022
(1994). [DOI]. (Cited on pages 16, 21, 65, and 123.)
[394] Tagoshi, H., Ohashi, A. and Owen, B. J., “Gravitational field and equations of motion of spinning compact binaries to 2.5-post-Newtonian order”, Phys. Rev. D, 63, 044006 (2001). [DOI], [grqc/0010014]. (Cited on pages 19 and 147.)
[395] Tagoshi, H. and Sasaki, M., “Post-Newtonian Expansion of Gravitational Waves from a Particle in
Circular Orbit around a Schwarzschild Black Hole”, Prog. Theor. Phys., 92, 745–771 (1994). [DOI],
[gr-qc/9405062]. (Cited on pages 21 and 123.)
[396] Tagoshi, H., Shibata, M., Tanaka, T. and Sasaki, M., “Post-Newtonian expansion of gravitational
waves from a particle in circular orbit around a rotating black hole: Up to 𝑂(𝑣 8 ) beyond the
quadrupole formula”, Phys. Rev. D, 54, 1439–1459 (1996). [DOI]. (Cited on page 158.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 186

186

Luc Blanchet

[397] Tanaka, T., Tagoshi, H. and Sasaki, M., “Gravitational Waves by a Particle in Circular Orbit around
a Schwarzschild Black Hole: 5.5 Post-Newtonian Formula”, Prog. Theor. Phys., 96, 1087–1101
(1996). [DOI], [gr-qc/9701050]. (Cited on pages 21 and 123.)
[398] Taylor, J. H., “Pulsar timing and relativistic gravity”, Class. Quantum Grav., 10, 167–174 (1993).
[DOI]. (Cited on pages 7, 13, and 14.)
[399] Taylor, J. H., Fowler, L. A. and McCulloch, P. M., “Measurements of general relativistic effects in the
binary pulsar PSR 1913+16”, Nature, 277, 437–440 (1979). [DOI]. (Cited on pages 7, 13, and 14.)
[400] Taylor, J. H. and Weisberg, J. M., “A New Test of General Relativity: Gravitational Radiation and
the Binary Pulsar PSR 1913+16”, Astrophys. J., 253, 908–920 (1982). [DOI]. (Cited on pages 7,
13, and 14.)
[401] Tessmer, M. and Schäfer, G., “Full-analytic frequency-domain 1PN-accurate gravitational wave forms
from eccentric compact binaries”, Phys. Rev. D, 82, 124064 (2010). [DOI], [arXiv:1006.3714 [gr-qc]].
(Cited on page 141.)
[402] Tessmer, M. and Schäfer, G., “Full-analytic frequency-domain gravitational wave forms from
eccentric compact binaries to 2PN accuracy”, Ann. Phys. (Berlin), 523, 813 (2011). [DOI],
[arXiv:1012.3894 [gr-qc]]. (Cited on page 141.)
[403] Thorne, K. S., “Multipole expansions of gravitational radiation”, Rev. Mod. Phys., 52, 299–339
(1980). [DOI], [ADS]. (Cited on pages 10, 11, 20, 26, 27, 35, 36, 37, and 50.)
[404] Thorne, K. S., “The theory of gravitational radiation: An introductory review”, in Deruelle, N.
and Piran, T., eds., Gravitational Radiation, NATO Advanced Study Institute, Centre de physique
des Houches, 2 – 21 June 1982, pp. 1–57, (North-Holland; Elsevier, Amsterdam; New York, 1983).
(Cited on page 9.)
[405] Thorne, K. S., “Gravitational radiation”, in Hawking, S. W. and Israel, W., eds., Three Hundred
Years of Gravitation, pp. 330–458, (Cambridge University Press, Cambridge; New York, 1987).
[Google Books]. (Cited on page 9.)
[406] Thorne, K. S., “Gravitational-wave bursts with memory: The Christodoulou effect”, Phys. Rev. D,
45, 520 (1992). [DOI]. (Cited on pages 21 and 43.)
[407] Thorne, K. S. and Hartle, J. B., “Laws of motion and precession for black holes and other bodies”,
Phys. Rev. D, 31, 1815–1837 (1985). [DOI]. (Cited on page 70.)
[408] Thorne, K. S. and Kovàcs, S. J., “Generation of gravitational waves. I. Weak-field sources”, Astrophys. J., 200, 245–262 (1975). [DOI]. (Cited on page 10.)
[409] Trautman, A., “Lectures on General Relativity”, Gen. Relativ. Gravit., 34, 721–762 (2002). [DOI].
Lectures delivered at King’s College in London in May – June 1958. (Cited on pages 148 and 150.)
[410] Trias, M. and Sintes, A. M., “LISA observations of supermassive black holes: Parameter estimation
using full post-Newtonian inspiral waveforms”, Phys. Rev. D, 77, 024030 (2008). [DOI], [ADS],
[arXiv:0707.4434 [gr-qc]]. (Cited on page 20.)
[411] Tulczyjew, W., “On the energy-momentum tensor density for simple pole particles”, Bull. Acad.
Polon. Sci. Cl. III, 5, 279 (1957). (Cited on pages 147, 148, and 150.)
[412] Tulczyjew, W., “Motion of multipole particles in general relativity theory”, Acta Phys. Pol., 18, 37
(1959). (Cited on pages 147, 148, and 150.)
[413] Vaidya, V., “Gravitational spin Hamiltonians from the 𝑆 matrix”, Phys. Rev. D, 91, 024017 (2015).
[DOI], [arXiv:1410.5348 [hep-th]]. (Cited on page 147.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2

## PDF page 187

Gravitational Radiation from Post-Newtonian Sources and Inspiralling Compact Binaries

187

[414] Vines, J., Hinderer, T. and Flanagan, É.É., “Post-1-Newtonian tidal effects in the gravitational
waveform from binary inspirals”, Phys. Rev. D, 83, 084051 (2011). [DOI], [arXiv:1101.1673 [gr-qc]].
(Cited on page 16.)
[415] Wagoner, R. V., “Test for Existence of Gravitational Radiation”, Astrophys. J. Lett., 196, L63–L65
(1975). [DOI]. (Cited on page 13.)
[416] Wagoner, R. V. and Will, C. M., “Post-Newtonian gravitational radiation from orbiting point
masses”, Astrophys. J., 210, 764–775 (1976). [DOI]. (Cited on pages 20 and 140.)
[417] Wald, R. M., “On perturbations of a Kerr black hole”, J. Math. Phys., 14, 1453–1461 (1973). [DOI].
(Cited on page 110.)
[418] Walker, M. and Will, C. M., “The approximation of radiative effects in relativistic gravity: Gravitational radiation reaction and energy loss in nearly Newtonian systems”, Astrophys. J. Lett., 242,
L129–L133 (1980). [DOI], [ADS]. (Cited on page 54.)
[419] Wen, L., “On the Eccentricity Distribution of Coalescing Black Hole Binaries Driven by the Kozai
Mechanism in Globular Clusters”, Astrophys. J., 598, 419 (2003). [DOI], [astro-ph/0211492]. (Cited
on page 135.)
[420] Wex, N., “The second post-Newtonian motion of compact binary-star systems with spin”, Class.
Quantum Grav., 12, 983–1005 (1995). [DOI]. (Cited on pages 138 and 141.)
[421] Will, C. M., “Gravitational Waves from Inspiralling Compact Binaries: A Post-Newtonian Approach”, in Sasaki, M., ed., Relativistic Cosmology, Proceedings of the 8th Nishinomiya-Yukawa
Memorial Symposium, Shukugawa City Hall, Nishinomiya, Hyogo, Japan, 28 – 29 October, 1993,
NYMSS, 8, pp. 83–98, (Universal Academy Press, Tokyo, 1993). [gr-qc/9403033]. (Cited on page 9.)
[422] Will, C. M., “Generation of post-Newtonian gravitational radiation via direct integration of the
relaxed Einstein equations”, Prog. Theor. Phys. Suppl., 136, 158–167 (1999). [DOI], [gr-qc/9910057].
(Cited on pages 11, 20, and 50.)
[423] Will, C. M., “Post-Newtonian gravitational radiation and equations of motion via direct integration
of the relaxed Einstein equations. III. Radiation reaction for binary systems with spinning bodies”,
Phys. Rev. D, 71, 084027 (2005). [DOI], [gr-qc/0502039]. (Cited on pages 151 and 159.)
[424] Will, C. M. and Wiseman, A. G., “Gravitational radiation from compact binary systems: Gravitational waveforms and energy loss to second post-Newtonian order”, Phys. Rev. D, 54, 4813–4848
(1996). [DOI], [gr-qc/9608012]. (Cited on pages 11, 12, 20, 50, 51, and 141.)
[425] Wiseman, A. G., “Coalescing binary systems of compact objects to (post)5/2 -Newtonian order. II.
Higher-order wave forms and radiation recoil”, Phys. Rev. D, 46, 1517–1539 (1992). [DOI], [ADS].
(Cited on page 22.)
[426] Wiseman, A. G., “Coalescing binary systems of compact objects to (post)5/2 -Newtonian order. IV.
The gravitational wave tail”, Phys. Rev. D, 48, 4757–4770 (1993). [DOI], [ADS]. (Cited on page 20.)
[427] Wiseman, A. G. and Will, C. M., “Christodoulou’s nonlinear gravitational-wave memory: Evaluation
in the quadrupole approximation”, Phys. Rev. D, 44, R2945–R2949 (1991). [DOI]. (Cited on
pages 21, 43, and 130.)
[428] Zeng, J. and Will, C. M., “Application of energy and angular momentum balance to gravitational
radiation reaction for binary systems with spin-orbit coupling”, Gen. Relativ. Gravit., 39, 1661
(2007). [DOI], [arXiv:0704.2720]. (Cited on page 18.)

Living Reviews in Relativity
DOI 10.12942/lrr-2014-2
