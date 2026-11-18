Source: https://doi.org/10.1007/JHEP03(2021)219
PDF sha256: 09f160ab48b697215569fde3e16ab882addcc409da4725b6e77bdcfcb0bfaae4
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine-gated

# Transcription of kaviraj_2021_jhep03_219_parisi_sourlas_rg.pdf

Transcription of `kaviraj_2021_jhep03_219_parisi_sourlas_rg.pdf` in this directory, 112 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-112 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: October 28, 2020
Accepted: February 3, 2021
Published: March 23, 2021

Random field Ising model and Parisi-Sourlas
supersymmetry. Part II. Renormalization group

a

Institut de Physique Théorique Philippe Meyer,
École Normale Supérieure, PSL Research University,
24 rue Lhomond, Paris, France
b
Laboratoire de Physique de l’Ecole normale supérieure, ENS,
Université PSL, CNRS, Sorbonne Université, Université de Paris,
F-75005 Paris, France
c
Institut des Hautes Études Scientifiques,
Bures-sur-Yvette, France

E-mail: apratim.kaviraj.01@gmail.com, emiliotrevisani@yahoo.it
Abstract: We revisit perturbative RG analysis in the replicated Landau-Ginzburg description of the Random Field Ising Model near the upper critical dimension 6. Working
in a field basis with manifest vicinity to a weakly-coupled Parisi-Sourlas supersymmetric
fixed point (Cardy, 1985), we look for interactions which may destabilize the SUSY RG
flow and lead to the loss of dimensional reduction. This problem is reduced to studying the
anomalous dimensions of “leaders” — lowest dimension parts of Sn -invariant perturbations
in the Cardy basis. Leader operators are classified as non-susy-writable, susy-writable or
susy-null depending on their symmetry. Susy-writable leaders are additionally classified as
belonging to superprimary multiplets transforming in particular OSp(d|2) representations.
We enumerate all leaders up to 6d dimension ∆ = 12, and compute their perturbative
anomalous dimensions (up to two loops). We thus identify two perturbations (with susynull and non-susy-writable leaders) becoming relevant below a critical dimension dc ≈ 4.2
- 4.7. This supports the scenario that the SUSY fixed point exists for all 3 < d ⩽ 6, but
becomes unstable for d < dc .
Keywords: Conformal Field Theory, Random Systems, Renormalization Group, Supersymmetry and Duality
ArXiv ePrint: 2009.10087

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

https://doi.org/10.1007/JHEP03(2021)219

JHEP03(2021)219

Apratim Kaviraj,a,b Slava Rychkovc,b and Emilio Trevisanib

## PDF page 2

Contents
1
4

2 Replicas and Cardy transform
2.1 Method of replicas
2.2 Standard perturbation theory and the upper critical dimension
2.3 Cardy transform
2.4 Basic RG scenario
2.5 Parisi-Sourlas SUSY
2.6 Dimensional reduction

6
6
7
7
10
10
13

3 RG flow in the basic scenario
3.1 RG flow in LSUSY
3.2 Emergence of SUSY from the L0 theory

14
14
17

4 RG flow in the full Cardy theory: general plan

20

5 Sn invariance in the Cardy basis
5.1 Sn singlets in the replicated basis
5.2 Sn singlets in the Cardy basis

21
24
25

6 The n-suppressed terms

26

7 RG flow in the L0 + L1 theory
7.1 Leader and followers: quartic term
7.2 Leader and followers: general case
7.3 Followers as individual L0 perturbations

28
28
30
31

8 Classification of leaders
8.1 General remarks
8.2 Non-susy-writable leaders
8.3 Susy-writable leaders
8.4 Susy-null leaders
8.5 Fixed point destabilization

31
32
33
34
37
38

9 Anomalous dimensions
9.1 Susy-writable leaders
9.2 Susy-null leaders
9.3 Non-susy-writable leaders

39
40
42
43

10 Scenarios for the loss of SUSY

44

–i–

JHEP03(2021)219

1 Introduction
1.1 Executive summary for RFIM experts

## PDF page 3

48
49
49
50
51
51
51
52
53

A History and prior work
A.1 Early work
A.2 No SUSY and no dimensional reduction in d = 3, 4
A.3 SUSY in d = 5?
A.4 Branched polymers and the Lee-Yang universality class
A.5 Zero-temperature fixed points
A.6 Interface disorder
A.7 Functional renormalization group studies of RFIM
A.8 Comments on the perturbative “cusp operators”
A.8.1 Two-point function of |φ|
A.9 Comparison to the work of Brézin and De Dominicis
A.10 Conformal bootstrap approach to dimensional reduction
A.11 Other approaches

54
54
54
55
55
56
58
61
64
65
67
68
69

B Toy model for the L0 + L1 RG flow
B.1 Integrating out
B.2 Rescaling
B.3 Beta functions and fixed point
B.4 Perturbations around the IR fixed point

70
71
72
74
74

C Correspondence between correlators of χi and ψ, ψ̄

77

D Tables of leaders up to ∆ = 12
D.1 Nφ = 2
D.2 Nφ = 4
D.3 Nφ = 6
D.4 Nφ = 8, 10

79
79
79
81
82

E Free L0 propagators

82

F RG at one loop
F.1 OPE method
F.2 Beta function

84
85
88

– ii –

JHEP03(2021)219

11 Discussion
11.1 Exploring our method further
11.1.1 Symmetry meaning of leaders in the Cardy basis
11.1.2 Higher-loop computations
11.1.3 Branched polymers and the Lee-Yang universality class
11.2 Checking our conclusions with other techniques
11.2.1 Numerical simulations
11.2.2 Conformal bootstrap
11.2.3 Functional renormalization group

## PDF page 4

89
89
91

H Details of anomalous dimension computations
H.1 Susy-writable operators
H.2 Susy-null leaders
H.2.1 ∆0 = 8 + O(ε), n = 4
H.2.2 ∆0 = 10 + O(ε), n = 6
H.2.3 ∆0 = 12 + O(ε), n = 6
H.2.4 ∆0 = 12 + O(ε), n = 8
H.3 Non-susy-writable leaders
H.3.1 Remark on admixture of susy-nulls

92
92
96
97
97
98
99
99
101

I

Remarks about tuning the disorder distribution

102

1

Introduction

This is the second part of our project dedicated to the puzzle of the Random Field Ising
Model. The first paper [1] was about nonperturbative CFT aspects, while here we will
focus on the Renormalization Group (RG) aspects and will propose a tentative resolution
of the puzzle. The two papers can be read largely independently.
As is well known, the usual ferromagnetic Ising model with the Hamiltonian H =
∑
−J ⟨ij⟩ si sj , where si = ±1 are spins on a regular d-dimensional lattice with nearestneighbor interactions, has a thermodynamic second-order phase transition in d ⩾ 2 which
is described by a non-Gaussian fixed point for d < 4. At the phase transition the correlation
length ξ → ∞. This idealized Ising model assumes no impurities, but real materials always
have impurities. Sufficiently near the critical temperature we will have ξ > L, the average
distance between impurities,1 and we should start worrying about their effect. Will they
change the universality class or not?
Specifically, in this work we are interested in impurities which have a random and
frozen magnetic moment (i.e. some of the spins at assigned randomly chosen values +1 or
−1, while others are allowed to fluctuate.2 This is modeled by adding to the usual Ising
Hamiltonian a random magnetic field hi on each site:
H = −J

∑

si sj +

⟨ij⟩
1

∑

hi s i .

(1.1)

i

The cleanest electronics-grade silicon has L ∼ 1000 lattice spacings (about one impurity per billion
atoms). Available ferromagnetic materials have even more impurities.
2
This may be realizable in a ferromagnetic metal with randomly distributed magnetic impurities forming
a spin-glass state, due to the RKKY interaction whose sign depends on the distance. The most common
experimental realizations of the RFIM is a randomly diluted antiferromagnet in a weak external magnetic
field [2]. See [3] for other experimental realizations.

–1–

JHEP03(2021)219

G RG at two loops
G.1 Beta function
G.2 Wavefunction renormalization

## PDF page 5

This equation defines our object of interest: the Random Field Ising Model (RFIM). The
real magnetic field h = (hi ) is assumed to have a factorized probability distribution
P(h)Dh =

∏

P (hi )dhi ,

(1.2)

⟨si sj ⟩h =

∫

(1.3)

Dh P(h)⟨si sj ⟩h ,

where ⟨si sj ⟩h is the thermodynamic average holding h fixed, and the overbar will always
denote a magnetic field average.
Near the phase transition, the lattice model (1.1) may be replaced by an effective
Landau-Ginzburg Hamiltonian
1
S[φ, h] = d x (∂µ φ)2 + V (φ) + h(x)φ(x) ,
2
m2 2 λ 4
V (φ) =
φ + φ ,
2
4!
∫

d

[

]

(1.4)

where the random magnetic field has short-range correlations: h(x)h(y) = Hδ (d) (x − y).
The relevance condition for the disordered coupling is ∆φ < d/2 (“Harris criterion”). Since
∆φ = d/2−1+η/2 and η is small, the Harris criterion is satisfied and the coupling h(x)φ(x)
is strongly relevant.3
Thus, the phase transition in RFIM is different from the usual Ising model in d dimensions. In 1979, Parisi and Sourlas [5] formulated a conjecture relating it instead to the
Ising model in d − 2 dimensions. It is convenient to split the Parisi-Sourlas conjecture into
two parts:
1. Emergence of SUSY: the RFIM transition is described by a conformal field theory
(CFT) in d dimensions, possessing a non-unitary supersymmetry with scalar supercharges (Parisi-Sourlas SUSY);
2. Dimensional reduction: a Parisi-Sourlas supersymmetric CFT in d dimensions
(SCFTd ) has the same critical exponents as an ordinary, non-supersymmetric CFT
in d − 2 dimensions.
3

Alternatively, one could add the h(x)φ2 (x) perturbation which is weakly relevant in 3d by the Harris
criterion, using the Ising fixed point dimension ∆(φ2 ) ≈ 1.41. This describes the phase transition in
∑
a different lattice model: H = − ⟨ij⟩ (J + δJij )si sj where δJij is a random perturbation called bond
disorder. Because the random φ2 perturbation is weakly relevant, the bond-disorder phase transition is
better understood than the RFIM phase transition studied here, see e.g. [4] for a recent discussion. Another
related difference with bond disorder is highlighted in footnote 30.

–2–

JHEP03(2021)219

so that hi are independent identically distributed random variables. It is assumed that hi
has zero mean and a finite variance: h2i = H.
Observables are computed in two steps, first averaging over spin fluctuations with a
fixed magnetic field, and then over the magnetic field (this is called quenched disorder
average). E.g. for the two-point function of spins:

## PDF page 6

The dimensionally reduced CFTd−2 has the same global symmetry Z2 as the parent SCFTd
and is expected to be the ordinary Ising fixed point in d − 2 dimensions. Hence, the RFIM
transition in d dimensions should have the same exponents as the ordinary Ising transition
in d − 2 dimensions.
As subsequent work has shown, this conjecture is subtle: it is not quite true, nor is
it however totally false. In spite of much work, there seems to be no agreement in the
literature about why this happens (see appendix A for the review). Here are some relevant
pro and contra results:

• It fails in d = 3, 4: numerical simulations show a non-SUSY continuous phase transition in the 3d and 4d RFIM [6, 7]. Dimensional reduction also fails: the 1d Ising does
not even have a phase transition, while the 2d Ising exponents do not agree with 4d
RFIM [7].
• It might be correct in d = 5 where there is numerical evidence for both SUSY and
dimensional reduction [8, 9].
• Both SUSY and dimensional reduction work perfectly in a parallel story for the
random field iφ3 model relevant for the description of branched polymers, which
maps on the Lee-Yang universality class in d − 2 dimensions (see section A.4).
The first paper of our project [1]4 performed new checks of Part 2 of the Parisi-Sourlas
conjecture, using nonperturbative CFT techniques. We have not found any inconsistency
from this point of view.5 Since Part 2 held up to scrutiny, the problem must therefore lie
in Part 1. Here we will proceed to study Part 1, and try to understand why sometimes it
works and sometimes fails.
We will start in section 2 with a review of the Parisi-Sourlas dimensional reduction.
From many ways to the Parisi-Sourlas supersymmetry, we choose to base our exposition
on the method of replicas accompanied by the “Cardy transform”: a judicious linear transformation of fields first proposed by Cardy in 1985 [15] but little used since. The Cardy
transform exhibits a Gaussian theory perturbed by various interactions, some of which are
weakly relevant and others are irrelevant in d = 6 − ε dimensions. The “basic RG scenario”
(section 2.4) consists in taking the n → 0 limit and dropping the formally irrelevant terms,
which naively results in a supersymmetric theory (and hence in dimensional reduction).
This SUSY theory and its fixed point are discussed in section 3, including a subtle point
(section 3.2) of how SUSY emerges at long distances in the basic scenario, even though the
Sn -invariant regulator breaks it.
After a short recap in section 4, we plunge into the heart of our study, which is to
examine the validity of the basic RG scenario assumptions. One of them (dropping the
4

See also an online talk [10] for an introduction.
First checks of dimensional reduction were based on perturbation theory (see appendix A.1). Nonperturbative arguments for dimensional reductions were advanced in [11–14]. Our work [1] is different from
these in that it does not rely on the use of Lagrangians.
5

–3–

JHEP03(2021)219

• It works in perturbative expansion near the upper critical dimension d = 6 − ε.

## PDF page 7

Note on phi’s. This paper will have a proliferation of phi’s. Stroked φ is the original field
in the random field Landau-Ginzburg Lagrangian (1.4). Stroked φi with an index denotes
replicated fields introduced in section 2.1. Loopy ϕ is a field from the Cardy transform
basis, section 2.3. All these live in Rd . Big Φ is the superfield (2.28) living in Rd|2 . Finally,
hatted φ̂ is a scalar field in Rd−2 which appears in the dimensionally reduced action (2.39).
1.1

Executive summary for RFIM experts

The great length of this paper is justified by the complexity of the problem, and by our wish
to make our work accessible to the readers without prior RFIM experience. In this section
we will provide a quick summary of our main ideas and results, which on the contrary will
only be understandable to the RFIM experts. All facts mentioned here are discussed in
detail elsewhere in the paper (see the table of contents, the outline in the introduction,
and a roadmap in section 4).
Via the method of replicas, RFIM phase transition is described by the Lagrangian
(n → 0)
∑n
i=1

[

)2
1
H (∑ n
(∂µ φi )2 + V (φi ) −
φi ,
i=1
2
2
]

V (φ) =

m2 2 λ 4
φ + φ .
2
4!

(1.5)

Using the linear transformation of fields φ1 = ϕ + ω/2, φi = ϕ − ω/2 + χi (i = 2 . . . n),
∑
χi = 0, the replicated Lagrangian is mapped to L0 + L1 + L2 , where
) λ (
)
∑n
∑n
m2 (
H 2 1 ∑n
ω +
(∂µ χi )2 +
2ϕω +
χ2i +
4ωϕ3 + 6
χ2i ϕ2 ,
i=2
i=2
i=2
2
2
2
4!
(1.6)
L1 terms vanish for n → 0 and can be safely dropped, while L2 terms are irrelevant and
may be dropped in d = 6 − ε, ε ≪ 1. The quartic interactions in L0 are weakly relevant for

L0 = ∂µ ϕ∂µ ω−

–4–

JHEP03(2021)219

n-suppressed terms) is justified in section 6, after having understood Sn invariance in the
Cardy basis (section 5). Section 5 also introduces the key concept of the “leader” operator,
which is the lowest-dimension part of an Sn -singlet. Scaling dimension of the leader controls
that of the full perturbation, as we explain in section 7. From here on, we work in the
strict n = 0 limit and examine if any perturbation irrelevant in d = 6 − ε may become
relevant in lower d, by looking at the leaders of Sn -singlet perturbations. These leaders
are classified (section 8) into three classes: non-susy-writable, susy-writable and susy-null,
which have only triangular mixing among each other, simplifying the anomalous dimension
computations (section 9). We list all leaders up to dimension 12 in d = 6, which includes
one or more leaders in each of the three classes. Finally, using the computed one- or
two-loop anomalous dimensions, some of which are negative, we build a case for the loss
of SUSY via RG instability of the SUSY fixed point below some critical dimension value
dc (section 10). Section 11 is devoted to a discussion of our results and to a list of open
problems: developing our method further, applying it in different situations (like for the
branched polymers), and checking our conclusions with alternative techniques.
Prior work on the RFIM phase transition being vast, we gather an extensive review
of the literature in appendix A, which may be of independent interest. Other appendices
contain technical details referred to from the main text.

## PDF page 8

ε ≪ 1 and flow to an IR fixed point. Separating weakly relevant and irrelevant effects is
the main point of this transformation. Replacing −2 linearly independent bosons χi by two
scalar fermions ψ, ψ̄, Lagrangian L0 maps to an equivalent Parisi-Sourlas supersymmetric
Lagrangian
H
∂µ ϕ∂µ ω − ω 2 + ωV ′ (ϕ) + ∂µ ψ∂µ ψ̄ + ψ ψ̄V ′′ (ϕ) .
(1.7)
2

• Susy-writable leaders, which make sense in the SUSY field basis ϕ, ω, ψ, ψ̄. E.g. the
∑
∑
leaders of Sn -invariant quadratic and quartic interactions ni=1 φ2i and ni=1 φ4i are,
∑
∑n
see (1.6), 2ϕω + i=2 χ2i → ϕω + 2ψ ψ̄ and 4ωϕ3 + 6 ni=2 χ2i ϕ2 → 4ωϕ3 + 12ψ ψ̄ϕ2 ,
so these are susy-writable, as are any leaders involving only χ2i .
• Susy-null leaders, which can be transformed to the SUSY field basis, but which vanish
after such a transformation because of ψ 2 = ψ̄ 2 = 0. The first such leader is (F4 )L =
∑
∑
( ni=2 χ2i )2 → (2ψ ψ̄)2 = 0 of the Sn -invariant operator F4 = ni,j=1 (φi − φj )4 .
• Non-susy-writable leaders, which cannot even be transformed to the SUSY field basis,
because they involve χi raised to a power higher than 2. The first of them is the
∑
∑
∑
leader (F6 )L = ( ni=2 χ3i )2 − 32 ( ni=2 χ2i )( nj=2 χ4j ) of the Sn -invariant operator F6 =
∑n
6
i,j=1 (φi − φj ) .
Susy-writable and susy-null leaders have O(n−2) symmetry in the field basis (ϕ, χi , ω),
which is the same as symmetry of L0 , while non-susy-writable leaders break this symmetry
to Sn−1 ⊂ O(n − 2).
Susy-writable leader dimensions can be computed from the SUSY Lagrangian (1.7)
or, due to dimensional reduction, from the Wilson-Fisher Lagrangian in d − 2 dimensions.
On the contrary, susy-null and non-susy-writable leader dimensions are inaccessible from
the SUSY Lagrangian or via dimensional reduction, and have to be computed from Lagrangian (1.6).
We did not find any susy-writable leader which becomes relevant. On the other hand,
the first susy-null leader (F4 )L and (F6 )L have sizable negative two-loop dimensions 8 −
8 2
2ε − 27
ε + . . . and 12 − 3ε − 79 ε2 + . . ., and appear to become relevant around dc ≈ 4.5. We
thus predict that for d < dc the Parisi-Sourlas fixed point is destabilized, and the RFIM
transition is described by another, non-supersymmetric, fixed point (about which we have
nothing to say).

–5–

JHEP03(2021)219

This derivation of Parisi-Sourlas supersymmetry (Cardy, 1985) works provided all the L2
terms or any other Sn -invariant terms are irrelevant, as is the case for ε ≪ 1. Our work
investigates for the first time whether this is still the case for ε = O(1).
To do so we build all possible Sn -invariant polynomial operators (not necessarily those
included in the quartic replicated Lagrangian) and transform them into the field basis
ϕ, ω, χi . We prove that the RG behavior of the transformed Sn -invariant operator is determined by the part of the lowest classical dimension (the leader). We compute one- or
two-loop anomalous dimensions of many leaders, up to classical dimension ∆ = 12, and
classifying them into three types by their symmetry:

## PDF page 9

2

Replicas and Cardy transform

Our work begins from two ideas, one standard and one less so. The standard idea is the
method of replicas, used in essentially all known to us renormalization group approaches
to this problem.6 The less standard idea is the Cardy transform, a linear transformation of
replica fields first considered by Cardy [15] in 1985 but little used since. We use it because
it reveals the Gaussian fixed point and clarifies the renormalization group picture.
2.1

Method of replicas

Here S[φ, h] is given in (1.4), A(φ) is any function of the field φ, e.g. a product of φ at
several points, P(h) is the disorder distribution, and overbar denotes the disorder average.
We multiply the integrand in (2.1) by 1 = Zhn−1 /Zhn−1 , rename φ → φ1 , and represent
Zhn−1 in the numerator as the product of partition functions of ‘replica’ fields φ2 , . . . , φn ,
with the same action as φ1 . We get:
⟨A(φ)⟩ =

∫

1
Dh P(h) n
Zh

∫

⃗ A (φ1 )e−
Dφ

∑n
i=1

S[φi ,h]

(2.2)

.

This equation is independent of n. Particularly nice is the limit n → 0, since the denominator Zhn → 1. With the usual provisos for going from integer to real n and commuting
the limit and the integral, we get a simpler formula:
⟨A(φ)⟩ = lim

∫

n→0

Dh P(h)

∫

⃗ A(φ1 )e−
Dφ

∑n
i=1

S[φi ,h]

(2.3)

.

As mentioned our disorder is mean zero and with short-range spatial correlations:
h(x) =

∫

Dh P(h)h(x) = 0 ,

∫

h(x)h(x′ ) =

Dh P(h)h(x)h(x′ ) = H δ(x − x′ ) . (2.4)

The simplest distribution satisfying these properties is the Gaussian white noise:
∫

1

P(h) ∝ e− 2H

dd x h(x)2

(2.5)

.

Assuming this distribution, the integral over h in (2.3) is Gaussian and can be performed.
We obtain:
⟨A(φ)⟩ = lim

∫

n→0

⃗ =
Sn [φ]

∫

d

d x

⃗

⃗ A(φ1 )e−Sn [φ] =: ⟨A(φ1 )⟩,
Dφ
⎧
⎨ n
∑ [1
⎩

6
7

i=1

2

]

(∂µ φi ) + V (φi ) −
2

(2.6)

( n
∑
H

2

i=1

φi

)2 ⎫
⎬

.

(2.7)

⎭

One exception is [16], which develops RG for the probability distribution of magnetic impurities.
This is sometimes called “second variant”, see e.g. [17], section 4.2.2.

–6–

JHEP03(2021)219

We use the version of the method of replicas appropriate for the study of correlation
functions.7 We are interested in quenched averaged correlators, defined first averaging over
φ and then over h:
∫
∫
1
⟨A(φ)⟩ = Dh P(h)
Dφ A(φ)e−S[φ,h] .
(2.1)
Zh

## PDF page 10

This is a pleasing result: we can compute disorder-averaged correlation functions from
a theory where disorder is replaced by a coupling among n → 0 replicas. This can be
generalized to disorder-averaged products of several correlation functions, e.g.
⟨A(φ)⟩⟨B(φ)⟩⟨C(φ)⟩ = lim

n→0

∫

⃗

⃗ A(φ1 )B(φi )C(φj )e−Sn [φ] = ⟨A(φ1 )B(φi )C(φj )⟩,
Dφ

(2.8)

2.2

Standard perturbation theory and the upper critical dimension

From the quadratic part of the action Sn one derives the propagator inverting the matrix
G−1 = k 2 1 − HM ,

(2.9)

where M is an n × n matrix whose all elements are unity. An easy computation gives
G=

1
HM
+
.
k 2 k 2 (k 2 − nH)

(2.10)

This propagator is employed in most perturbative studies of RFIM. Notice that two terms
have a different scaling with k, which renders perturbative computations somewhat awkward.8 One usually has to go through the diagrams looking for terms most singular in the
limit k → 0, hence most important at long distances, which come precisely from the second
term in (2.10). The effective expansion parameter for these terms, deemed most important
in IR, is therefore changed from λ to λH. The H having mass dimension 2, λH becomes
marginal at the upper critical dimension duc = 6.
This way of reasoning, while standard in much of RFIM work, seems like a departure
from the usual Wilsonian paradigm.9 Wilson taught us to think in terms of a Gaussian fixed
point at which fields have well-defined scaling dimensions. One then classifies perturbations
into strongly relevant, weakly relevant, and irrelevant. Strongly relevant perturbations are
tuned, irrelevant dropped, while the weakly relevant may drive the RG flow to a nonGaussian weakly-coupled fixed point nearby. This is much more systematic and powerful
than having to sift through diagrams. Cardy [15] showed that the disordered fixed point is
not an exception and can also be presented this way. We will now describe his construction,
which will form the basis for our work.
2.3

Cardy transform

As mentioned, different components of the propagator (2.10) have different scaling dimensions. The idea of Cardy [15] is to make this manifest via a linear transformation in the
8

Another displeasing feature is that the second term in (2.10) only acquires good scaling in the n → 0
limit.
9
A related concept is that of ‘zero-temperature fixed point’ which we review in appendix A.5.

–7–

JHEP03(2021)219

as long as all the three indices 1, i, j are all different. Note that the replicated theory
contains formally φi with any index, so there is no contradiction in introducing 3 different
fields as in (2.8) which will be compensated by −3 fields when taking n → 0 limit. Such
occurrences of a negative number of fields are a necessary feature of this formalism; we will
encounter it soon in section 2.3.

## PDF page 11

field space. One then drops the irrelevant terms in the resulting effective Lagrangian, and
reaches the disordered fixed point by RG flowing from a Gaussian fixed point perturbed
by a weakly relevant perturbation.
The Cardy transform can be guessed by the following argument. First one decides
to treat φ1 differently from φ2 , . . . , φn (perhaps motivated by eq. (2.3) for the disordered
correlated functions). One then writes
φi = ρ + χi ,

(i = 2 . . . n) ,

with

n
∑

χi = 0 ,

(2.11)

i=2

] 1 ∑′
1[
(∂φ1 )2 + (n − 1)(∂ρ)2 − H[φ1 + (n − 1)ρ]2 +
(∂χi )2 .
2
2

∑′

≡

i=2 ):

∑n

(2.12)

In the n → 0 limit this simplifies even further as
] 1 ∑′
1[
H
1 ∑′
(∂φ1 )2 − (∂ρ)2 − H(φ1 − ρ)2 +
(∂χi )2 = ∂ϕ∂ω − ω 2 +
(∂χi )2 , (2.13)
2
2
2
2

where we defined

1
ϕ = (φ1 + ρ),
ω = φ1 − ρ .
(2.14)
2
The Cardy transform is given, for any n, by eqs. (2.11), (2.14), which equivalently can be
written as
φ1 = ϕ + ω/2,
φi = ϕ − ω/2 + χi

(i = 2 . . . n).

(2.15)

From the quadratic part of (2.13), the transformed fields ω, ϕ, χi have well-defined scaling
dimensions in the n → 0 limit:
∆ϕ =

d
− 2,
2

∆χ =

d
− 1,
2

∆ω =

d
.
2

(2.16)

Note that it would be wrong to think of the ω 2 term in (2.13) as a mass term, because the
kinetic term (∂ω)2 is missing. In fact all propagators are scale invariant:10
1
1
δij −
Πij .
2
k
n−1
(2.17)
2
4
The 1/k and 1/k are the same powers as in (2.10) but now they are nicely separated.
The dimension of ϕ is below the unitarity bound — one sign that we are dealing with a
non-unitary theory.
Applying the Cardy transform to the interaction term in (2.7), we obtain
⟨ϕk ϕ−k ⟩ =

H
,
k4

⟨ϕk ω−k ⟩ =

1
,
k2

⟨ωω⟩ = 0,

V (ϕ + ω/2) +

∑′

⟨(χi )k (χj )−k ⟩ =

V (ϕ − ω/2 + χi ) .

10

(

)

(2.18)

Here Πij is an (n − 1) × (n − 1) matrix whose all elements are 1. Note that the χχ propagator is
∑n
consistent with the constraint
χ = 0.
i=2 i

–8–

JHEP03(2021)219

1
i.e. ρ = n−1
(φ2 +. . .+φn ). The quadratic part of (2.7) then separates nicely as (

## PDF page 12

Taylor-expanding the quartic potential,11 we organize the resulting terms by their scaling
dimension. Since ϕ has the smallest scaling dimension, the most relevant term is obtained
by keeping ϕ in the argument, which gives
[1 + (n − 1)]V (ϕ) = nV (ϕ) .

(2.19)

V ′ (ϕ)

ω
ω
+ (n − 1)V ′ (ϕ) −
2
2
(

)

= ωV ′ (ϕ) + n-suppressed ,

(2.20)

∑′
1 ′′
V (ϕ)
χ2i .
2

These have the same scaling dimension ∆(V (ϕ)) + 2. We define the leading Lagrangian L0
including the quadratic terms and these most relevant terms, in the n → 0 limit:
L0 = ∂ϕ∂ω −

}
H 2
1 ∑′ {
ω + ωV ′ (ϕ) +
(∂χi )2 + χ2i V ′′ (ϕ) .
2
2

(2.21)

Explicitly, for the quartic potential (including the mass term) this is
L0 = ∂ϕ∂ω −

)
∑′ ) λ (
∑′
H 2 1 ∑′
m2 (
ω +
(∂χi )2 +
2ϕω +
χ2i +
4ωϕ3 + 6
χ2i ϕ2 . (2.22)
2
2
2
4!

We can now easily rederive the upper critical dimension duc = 6 in this language: the
quartic interactions have dimension 2d − 6 and become marginal at d = duc .12
Expanding (2.18) to higher order, we get terms of higher scaling dimensions. We
include all such terms which survive in the n → 0 limit into the subleading Lagrangian L1 .
It is easy to see that the lowest nontrivial terms in L1 involve expanding to cubic order:
L1 ⊃ V ′′′ (ϕ) ×

{ ∑′

χ3i , ω

∑′

}

χ2i , ω 3 .

(2.23)

Comparing to the V ′′ (ϕ) χ2i term present in L0 , we see that these L1 terms have dimension 1,2 and 4 units higher, so they are irrelevant, at least in d = duc − ε. The terms in L1
proportional to V ′′′′ (ϕ) (expanding to quartic order) would be even more irrelevant.
Finally, we gather in L2 all n-suppressed terms. They come from both the quadratic
part and the interactions, and some of them were already mentioned. E.g.
∑

{

}

L2 ⊃ n (∂ϕ)2 , ϕω, (∂ω)2 , V (ϕ), . . . .
11

(2.24)

Only the quartic potential will be treated in this work, while the cubic potential (branched polymers
and the Lee-Yang universality class) will be dealt with in a future publication [18]. See section 11.1.3.
12
For the branched polymers (the cubic potential) analogous considerations would give duc = 8.

–9–

JHEP03(2021)219

This is an example of an “n-suppressed” term, i.e. term vanishing in the n → 0 limit.
The naive expectation is that such terms should not matter. Below we will discuss this in
detail, analyze various subtleties, and confirm the naive expectation. For the moment let
us focus on the terms which survive as n → 0. The most relevant such terms appear when
we expand either to first order in ω or to second order in χi (the first order in χi vanishes
∑
thanks to ′ χi = 0):

## PDF page 13

We stress that the Cardy transform being just a linear transformation of fields, it cannot introduce any mistake compared to the original replicated Lagrangian, unless one drops some
terms. Any observable or correlation function which was computable from the replicated
Lagrangian can be equivalently computed in the Cardy basis (ϕ, ω, χi ). E.g., applying
the Cardy transform to φ1 , φi , φj , . . . in a general disordered correlator like (2.8), we can
express it as a linear combination of correlators of Cardy fields.
2.4

Basic RG scenario

LCardy = L0 + L1 + L2 ,

(2.25)

where
• L0 contains the terms which are relevant and do not vanish as n → 0,
• L1 contains the terms which are irrelevant and do not vanish as n → 0,
• L2 contains all n-suppressed terms.
Classification relevant/irrelevant is for small ε = duc − d and it is not a priori clear what
will be the fate of L1 terms for larger ε. Let’s assume that (a) L1 terms remain irrelevant
and can be discarded, and (b) that L2 can be simply dropped in the n → 0 limit. We will
refer to these two assumptions as “basic RG scenario”. So we simply drop L1 and L2 and
assume that the IR physics of the disordered model is captured by L0 alone. Following
this scenario we will draw some interesting conclusions in sections 2.5 and 2.6, concerning
supersymmetry and dimensional reduction. Starting from section 3, we will start carefully
checking whether the two assumptions hold.
2.5

Parisi-Sourlas SUSY

Within the basic RG scenario, we need to understand the n → 0 limit of the Lagrangian
L0 . Here the dependence on n appears only through the (n − 1) fields χi which sum
to zero, so we have effectively (n − 2) linearly independent fields. Since L0 is Gaussian
)− n−2

2 .
in χi , integrating them out would give a result proportional to det[−∂ 2 + V ′′ (ϕ)]
2
′′
When n → 0 this reduces to det[−∂ + V (ϕ)], which is the usual result for a fermionic
Gaussian path integral (up to overall factors which cancel in the computation of correlation
functions). This motivates the substitution

(

n
1∑
n→0
χi [−∂ 2 + V ′′ (ϕ)]χi −→ ψ[−∂ 2 + V ′′ (ϕ)]ψ̄,
2 i=2

(2.26)

where ψ and ψ̄ are two anticommuting real scalar fields. By taking the limit n → 0 of L0 we
thus obtain a Lagrangian of two commuting real scalar fields ϕ, ω and two anticommuting

– 10 –

JHEP03(2021)219

Let us summarize the results so far. Starting from the random field action (1.4) we used
the method of replicas and the Cardy transform (2.15) to obtain a Lagrangian

## PDF page 14

ones ψ, ψ̄,13
H 2
ω + ωV ′ (ϕ) + ∂ψ∂ ψ̄ + ψ ψ̄V ′′ (ϕ).
(2.27)
2
This is the Parisi-Sourlas Lagrangian, which is invariant under a supersymmetry. This can
be made manifest using an orthosymplectic superspace with x as a bosonic and θ, θ̄ as two
real Grassmann coordinates. We can then combine all fields into one superfield
LSUSY = ∂ϕ∂ω −

Φ(x, θ, θ̄) = ϕ(x) + θψ̄(x) + θ̄ψ(x) + θθ̄ω(x) .

(2.28)

Ssuperspace =

∫

1
dd xdθ̄dθ − ΦD2 Φ + V (Φ) ,
2
[

]

(2.29)

where D2 := ∂ 2 −H∂θ ∂θ̄ is the super-Laplacian. It is straightforward to check that integrat∫
ing over θ, θ̄ reduces (2.29) to dd x LSUSY . Parisi-Sourlas supersymmetry transformations
consist of (super)translations Rd|2 and of OSp(d|2) (super)rotations which leave the superspace metric dx2 − H4 dθdθ̄ invariant.
The conclusion is that, if the basic RG scenario holds, the critical point of a random
field theory is in the same universality class as the IR fixed point of the supersymmetric
Parisi-Sourlas action (2.29). This is Part 1 (Emergence of SUSY) of the Parisi-Sourlas
conjecture.
This way to see the emergence of supersymmetry is different from the original one [5]
based on classical solutions of a stochastic partial differential equation. The original argument had some caveats (the solution may not be unique, the fermionic determinant was
missing the absolute sign, etc.). The Cardy transform argument also has assumptions (can
we drop L1 and L2 ?), but as we will see the validity of these assumptions may be easier to
check.
Supersymmetry leads to various nice consequences for correlation functions.
E.g. ⟨ϕ(x)ϕ(0)⟩, ⟨ϕ(x)ω(0)⟩, ⟨ω(x)ω(0)⟩ correlators can be extracted from the single correlator of superfields:
⟨Φ(x, θ1 , θ̄1 )Φ(0, θ2 , θ̄2 )⟩ = ⟨ϕ(x)ϕ(0)⟩ + θ1 θ̄1 ⟨ω(x)ϕ(0)⟩ + θ1 θ̄1 θ2 θ̄2 ⟨ω(x)ω(0)⟩ + . . . (2.30)
The l.h.s. being a function of x2 − H4 (θ1 − θ2 )(θ̄1 − θ̄2 ),this gives relations
⟨ϕ(x)ω(0)⟩ = ⟨ψ̄(x)ψ(0)⟩ = −

4 d
⟨ϕ(x)ϕ(0)⟩,
H dx2

⟨ω(x)ω(0)⟩ = 0.

(2.31)

While the IR scaling dimensions get corrections compared to the UV dimensions (2.16),
these supersymmetric relations imply that ∆ω = ∆ϕ + 2, ∆ψ = ∆ψ̄ = ∆ϕ + 1 remain true
in the IR.
13

Note that this formulation only works for L0 . In fact the Lagrangians L1 and L2 may contain operators
∑′ k
proportional to
χi for k > 2, which are ‘non-susy-writable’ (cannot be written in terms of ψ, ψ̄). This
will be discussed in detail below. In the following sections, to study the RG flow of L1 and L2 , we will
therefore use the formulation in terms of the fields χi .

– 11 –

JHEP03(2021)219

The action in superspace takes the form

## PDF page 15

We can also trace what this implies for physical observables, which are correlators of
φ’s. It is customary to consider connected and disconnected 2-point functions:
Gconn = ⟨φ(x)φ(0)⟩ − ⟨φ(x)⟩⟨φ(0)⟩,

Gdisc = ⟨φ(x)⟩⟨φ(0)⟩.

(2.32)

In the replica formalism these can be expressed as (see (2.8))
Gconn = ⟨φ1 (x)φ1 (0)⟩ − ⟨φ1 (x)φi (0)⟩,

Gdisc = ⟨φ1 (x)φi (0)⟩.

(2.33)

Gconn = ⟨ϕ(x)ω(0)⟩,

Gdisc = ⟨ϕ(x)ϕ(0)⟩.

(2.34)

By (2.31), this gives a relation between Gconn and Gdisc .
We should warn the reader about various subtleties concerning the relations of the Lagrangians L0 and LSUSY . First, while the two are formally equivalent at the classical level,
differences may appear at the level of loop effects because the most natural Sn -invariant
UV regulator of L0 is not SUSY-invariant. We will resolve this subtlety in section 3.2.
Second, Lagrangians L0 and LSUSY have overlapping but not identical sets of correlation functions. Any L0 correlator of operators made from ϕ, ω and O(n − 2)-invariant
∑
objects quadratic in χi can be mapped to an LSUSY correlator via 12 ′ χ2i → ψ ψ̄,
∑
′
1
(∂χi )2 → ∂ψ∂ ψ̄ etc. E.g. we have the following relation
2
⟨ ∑
⟩
′ 2
1
1 ∑′ 2
χi (x)
χi (0) = ⟨ψ ψ̄(x)ψ ψ̄(0)⟩,

2

2

(2.35)

as is easy to check in the free theory (λ = 0). We extend this to other bilinears and their
products in appendix C. Some uncontracted correlators can also be mapped, allowing for
tensorial coefficients: e.g.
⟨χi (x)χj (0)⟩ = −(δij + Πij )⟨ψ(x)ψ̄(0)⟩.

(2.36)

However, this does not extend to general correlators. E.g. as we discuss in appendix C,
it does not seem possible to represent a general 4-point function ⟨χi χj χk χl ⟩ as a linear
combination of ⟨ψψ ψ̄ ψ̄⟩ correlators (where ψ’s and are ψ̄’s may be inserted in arbitrary
order at four points). So, while the Cardy basis still contains an infinitude of different
fields χi , necessary to faithfully represent general replicated observables (2.8), some of this
richness is gone in the SUSY theory which only has two fields ψ, ψ̄.14
We will call “susy-writable” those L0 theory operators whose correlators can be computed by SUSY theory LSUSY . Not all Sn−1 -invariant operators belong to this class, the
∑
simplest examples being ′ χki for k > 2, see footnote 13. These operators are nontrivial,
e.g. their 2-point functions are nonzero. Yet there does not seem to be a way to compute
them using the SUSY fields.
14

Going in the opposite direction, general SUSY correlators of ψ, ψ̄ at different points, like
⟨ψ(x1 ) . . . ψ(xn )ψ̄(y1 ) . . . ψ̄(yn )⟩, do not seem to have any particular meaning in the L0 theory.

– 12 –

JHEP03(2021)219

where i ̸= 1 is arbitrary. Averaging over i = 2, . . . , n, Cardy-transforming, and using
⟨ωω⟩ = 0 as a consequence of SUSY, we get

## PDF page 16

2.6

Dimensional reduction

⟨Φ(x1 , 0, 0)Φ(x2 , 0, 0)⟩ = ⟨ϕ(x1 )ϕ(x2 )⟩.

(2.37)

Next we pick a d − 2 hyperplane Rd−2 ⊂ Rd , for definiteness spanned by the first d − 2
components. Dimensional reduction means that by demanding x’s to lie in this hyperplane
we get a further equality:
⟨ϕ(x1 )ϕ(x2 )⟩ = ⟨φ̂ (x1 )φ̂ (x2 )⟩CFTd−2 ,

(xi ∈ Rd−2 ).

(2.38)

The correlation function in the r.h.s. of (2.38) is computed in a (d − 2)-dimensional conformal field theory, the RG fixed point of the non-supersymmetric Landau-Ginzburg action
S=

4π
H

∫

dd−2 x

[

1
(∂ φ̂ )2 + V (φ̂ ) .
2
]

(2.39)

The potential is the same as the initial random field action, but this theory lives in 2 dimensions less and has no disorder fields. For simplicity we stated (2.38) for 2-point functions,
but it generalizes for higher point functions and for composite operator insertions [1].
With prior studies [11–14]15 and our own tests in [1], Part 2 of the Parisi-Sourlas
conjecture appears to be on rather solid ground, especially compared to Part 1. In this
paper, we will assume that Part 2 is true and we will use it as one of ingredients to
understand what may go wrong with Part 1. E.g. we will need to understand the spectrum
of Sn -invariant perturbations of L0 theory, to see if any of these become relevant. Those
of these perturbations which are susy-writable are captured by the SUSY theory. On
the other hand, by dimensional reduction, the spectrum of the SUSY fixed point can be
understood from the spectrum of the Wilson-Fisher fixed point, which is rather well known
(see sections 8.3 and 9.1). Of course, dimensional reduction does not say anything about
perturbations which are not susy-writable, and those will have to be studied independently.
15

See also recent rigorous work [19, 20].

– 13 –

JHEP03(2021)219

Part 2 (Dimensional reduction) of the Parisi-Sourlas conjecture [5] states that the
supersymmetric theory (2.27), (2.29) is related to a theory in two less dimensions with
no disorder nor supersymmetry. More concretely it says that correlation functions of
the SUSY theory can be mapped to correlation functions of a (d − 2)-dimensional model
with the same interaction V (φ), by restricting the coordinates to a codimension two
hyperplane, and setting to zero the Grassmann variables. In [1] we tested the dimensional
reduction for the strongly coupled fixed point of the RG flow of the supersymmetric
theory. We argued that the map works at the level of axiomatic CFTs, due to particular
superconformal symmetry of the theory.
Let us illustrate how this works by considering the 2-point functions of Φ computed
at the IR fixed point of the action (2.29) with a given potential V (Φ) (e.g. a quartic or a
cubic). First by setting θ = θ̄ = 0 in (2.30) we have a general SUSY relation:

## PDF page 17

3

RG flow in the basic scenario

3.1

RG flow in LSUSY

In this section we will discuss the RG flow of the SUSY theory (2.27), (2.29). As already
mentioned, this theory is invariant under super-Poincaré, which is the semidirect product
of super-translations Rd|2 and super-rotations OSp(d|2):
super-Poincaré = Rd|2 ⋊ OSp(d|2) .

(3.1)

All these transformations leave the superspace distance x2 − H4 θθ̄ invariant. Under supertranslations δθ = ε, δ θ̄ = ε the fields transform as
δϕ = εψ − εψ̄,

δψ = εω,

δ ψ̄ = εω,

δω = 0 .

(3.2)

H
εµθ xµ ,
2

(3.3)

Superrotations act in superspace as
δxµ = εµθ θ + εµθ̄ θ̄ ,

δθ =

H
ε xµ ,
2 µθ̄

δ θ̄ = −

and the corresponding field transformations leaving the action invariant are
H µ
H
x εµθ ψ − xµ εµθ̄ ψ̄,
2
2
H µ
δ ψ̄ = − x εµθ ω − ∂ µ ϕεµθ ,
2
δϕ = −

δω = εµθ ∂ µ ψ + εµθ̄ ∂ µ ψ̄ ,
δψ =

H µ
x εµθ̄ ω + ∂ µ ϕεµθ̄ .
2

(3.4)

There are also bosonic Sp(2) transformations which rotate ψ, ψ̄ and leave ϕ, ω invariant;
we do not write them explicitly.
For the quartic potential and working in d = 6 − ε, we write the SUSY Lagrangian as
LSUSY = ∂ϕ∂ω −

(
)
)
H 2
λ (
ω + ∂ψ∂ ψ̄ + m2 ωϕ + ψ ψ̄ + µε 4ωϕ3 + 12ψ ψ̄ϕ2 .
2
4!

(3.5)

(where we introduced the RG scale µ and made the coupling λ dimensionless). Standard
techniques allow us to compute the RG flow perturbatively. E.g. the one-loop beta function
for the dimensionless quartic coupling λ can be obtained in dimensional regularization as
βλ = −ελ +

3Hλ2
+ O(λ3 ) .
64π 3

– 14 –

(3.6)

JHEP03(2021)219

In this section we will discuss in more detail the RG flow assuming the basic RG scenario
(i.e. dropping L1 and L2 ). We start in section 3.1 with some comments about the RG flow
in the “SUSY theory”, i.e. theory (2.27), (2.29) with field content ϕ, ψ, ψ̄, ω described by the
Lagrangian LSUSY or, equivalently, the superspace action Ssuperspace . Then in section 3.2 we
discuss the RG flow in the theory L0 with field content ϕ, ω, χi and Lagrangian (2.21). We
will see that the L0 theory is not quite equivalent to LSUSY (even in the fermion bilinear sector) because the Sn -invariant Wilsonian UV cutoff partially breaks supersymmetry. Upon
careful analysis we will see that these SUSY breaking effects disappear at long distances.

## PDF page 18

From this we obtain a fixed point at
λ∗ =

64π 3 ε
+ O(ε2 ) .
3H

(3.7)

LWF =

1 ( )2 m2 2 λ̂ 4
∂ φ̂ +
φ̂ + φ̂
2
2
4!

(3.8)

upon identification of couplings

4π
λ̂.
(3.9)
H
One can easily check that (3.6) and (3.7) map under these identification to the familiar
Wilson-Fisher expressions, in particular λ̂∗ = (16π 2 /3)ε + O(ε2 ). This, of course, is a
perturbative manifestation of dimensional reduction, and (3.9) follows from (2.39).
As mentioned in section 2.6, in this paper we assume dimensional reduction (Part 2 of
the Parisi-Sourlas conjecture) settled, so we assume full equivalence between SUSY RG flow
in d dimensions and Wilson-Fisher RG flow in dˆ = d − 2 dimensions, both perturbatively
and nonperturbatively. For dˆ ⩾ 2, the Wilson-Fisher RG flow goes to a fixed point for a
particular value of the bare mass, and the corresponding d = dˆ + 2 SUSY RG flow will
go to a SUSY fixed point for the same bare mass.16 On the other hand, for dˆ = 1, we
get the 1d Wilson-Fisher flow, which is just quantum mechanics with a quartic potential.
For whatever value of the mass, the quantum mechanical spectrum is discrete, and the IR
phase is massive. By the assumed exact correspondence, the 3d SUSY RG flow thus should
also flow to a massive phase, with exactly preserved supersymmetry. We conclude that a
nontrivial 3d SUSY RG fixed point does not exist. Note that the absence of a SUSY IR
fixed point does not imply spontaneous breakdown of SUSY.17
These simple observations show what exactly needs to be explained concerning Part 1
of the Parisi-Sourlas conjecture, depending on d. Down to 4d, the SUSY fixed point exists,
so we need to understand if it is stable or not with respect to the perturbations present in
the L0 + L1 + L2 . If the SUSY fixed point is unstable, then the flow will be driven away
from it, and the RFIM phase transition will be described by another fixed point (about
λ=

16

The Wilson-Fisher fixed point is believed to exist also for 1 < dˆ < 2, but we will not discuss this
intermediate case in detail; see [21].
17
This point does not seem to be universally appreciated in the literature. E.g. ref. [22] says “even if
the RG flow is started with initial conditions obeying supersymmetry, a mechanism should be provided to
describe a spontaneous breakdown of supersymmetry.”

– 15 –

JHEP03(2021)219

(The fixed point lies at m2 =0 in dimensional regularization) One can check that the renormalization of the fields ϕ, ω, ψ, ψ̄ turns out to be equal, in agreement with supersymmetry.
We elaborate on these computations in appendices F and G. Another feature of the RG
flow is that the parameter H does not get renormalized, since it enters in SUSY transformations which cannot get deformed provided that the regulator preserves SUSY, as turns
out to be true for dimensional regularization (see appendix G). Other regulators will be
discussed below.
Finally, the SUSY RG flow is equivalent to the Wilson-Fisher flow in dˆ = 4 − ε dimensions with the Lagrangian:

## PDF page 19

which we will have nothing to say in this paper). The situation is different in 3d: the SUSY
fixed point does not exist there, so the RFIM phase transition must be for sure described
by some other fixed point. The only problem in 3d is to find this other fixed point, not to
explain the absence of SUSY.
Let us come back to the non-renormalization of H. It may look like we have a oneparameter family of RG fixed points parametrized by the choice of H. However all of these
fixed points are trivially related to each other by rescaling the fields, so in practice there
is only one fixed point up to equivalence. Rescaling
ω → rω

ψ, ψ̄ = inv,

(3.10)

has the effect of rescaling H → r2 H, λ → r−2 λ. Since λH is left invariant, the fixed
point (3.7) is mapped to an equivalent one characterized by another value of H.
We will see in section 8.3 that ω 2 can be seen as a member of superstress tensor multiplet,18 which explains why it is exactly marginal, and why adding it to the action can be
undone by changing the superspace metric, which is what rescaling (3.10) secretly is. Usually, when a CFT is deformed by an exactly marginal deformation, we get a different CFT
with different scaling dimensions and different OPE coefficients. This is clearly not the case
when deforming by ω 2 , since this leaves scaling dimensions invariant and OPE coefficients
change trivially due to rescaling, so we get a CFT equivalent to the one we started with. In
the renormalization group theory parlance, such deformations which can be undone by a
field redefinition are classified as “redundant” [23]. Usually redundant operators are those
which are proportional to the equations of motion, and they have zero correlation functions
at non-coincident points. Such operators and their scaling dimensions do not even appear
in CFT description. Operator ω 2 , although “redundant” in the sense described above, does
have nonzero correlators at non-coincident points, and is a bona fide CFT operator.
Finally let us discuss the SUSY RG flow in a Wilsonian scheme with a momentum
cutoff, as opposed to dimensional regularization. We have to regulate the theory in a
SUSY-preserving way, which requires some care in choosing momentum cutoffs. Before
cutoffs, the propagators are19
⟨ϕk ϕ−k ⟩ =

H
,
k4

⟨ϕk ω−k ⟩ =

1
,
k2

⟨ωω⟩ = 0,

1
⟨ψk ψ̄−k ⟩ = − 2 .
k

(3.11)

Momentum cutoff has to be imposed on the super-propagator. In position space, the superpropagator must be a function of x2 − H4 θθ̄, while in supermomentum-space it is a function
of k 2 −Hαα where α, α are Grassmann coordinates Fourier-conjugated to θ, θ̄. This implies
that component propagators must be related by20
Gϕω (k) = Gψ̄ψ (k),

Gϕϕ (k) = −H

18

d
Gϕω (k).
dk 2

(3.12)

More precisely ω 2 is a linear combination of a superstress tensor component and a total derivative, see
eqs. (8.11) and (8.12).
19
Dimensional regularization uses exactly these propagators and it is a SUSY-preserving scheme.
20
It is also possible to obtain these relations directly from position space (2.31) without help of superFourier transform. For this, represent the radially symmetric propagators as linear combinations of Gaus2
sians e−αx and do the usual Fourier transform.

– 16 –

JHEP03(2021)219

ϕ → r−1 ϕ ,

## PDF page 20

We see that eqs. (3.11) satisfy these, and cutoffs must be introduced in a way to preserve
these relations. E.g. we can choose
F (k 2 )
Gϕω (k) = Gψ̄ψ (k) = Λ 2 ,
k

(

Gϕϕ (k) = H

FΛ (k 2 ) FΛ′ (k 2 )
−
k4
k2

)

,

(3.13)

3.2

Emergence of SUSY from the L0 theory

Let us now discuss RG flow in the L0 theory (2.21) with the quartic potential. As dis∑
cussed in section 2.5, this theory can be mapped on LSUSY via replacement 12 ′ χ2i → ψ ψ̄,
1 ∑′
(∂χi )2 → ∂ψ∂ ψ̄. So at first glance this theory has the same flow as the SUSY theory
2
discussed in the previous section. However there is a subtlety: the cutoff is not quite the
same. The L0 theory (2.21) came from the replicated action (2.7) possessing Sn invariance. The replicated action had an Sn -invariant regulator, and the L0 theory inherits this
regulator.
∑
The kinetic part of the L0 theory had two pieces of different origin: ∂ϕ∂ω + 12 ′ (∂χi )2
which came from the kinetic term of (2.7) and − H2 ω 2 which came from integrating out
the magnetic field. In a regulated theory, these two terms will have their own momentum
cutoffs which do not have to coincide. We can model this situation by writing the regulated
kinetic term in momentum space as
HΛ (k 2 )
ωk ω−k ,
(3.14)
2
where FΛ (0) = 1, HΛ (0) = H, both FΛ and HΛ go to zero at large momenta, and we
∑
already performed the map to SUSY fields replacing 12 ′ χi,k χi,−k → ψk ψ̄−k . We get the
propagators:
FΛ (k 2 )−1 k 2 (ϕk ω−k + ψk ψ̄−k ) −

2 2
FΛ (k 2 )
2 [FΛ (k )]
,
G
(k)
=
H
(k
)
.
(3.15)
ϕϕ
Λ
k2
k4
Comparing these with (3.13), we see that SUSY is not in general respected. In fact, while
Gϕω = Gψ̄ψ agree as they should, the Gϕϕ propagators does not have the expected form.
Even if we choose FΛ (k 2 ) = HΛ (k 2 ) = Θ(Λ2 − k 2 ), Gϕϕ is missing the δ(k 2 − Λ2 ) piece.
Thus, to understand the RG flow of L0 , we have to understand the RG flow of LSUSY
regulated in a non-SUSY invariant way. One might worry that a regulator breaking SUSY
can be very dangerous for its fate, but fortunately all is not lost. The point is that the
above regulator breaks SUSY only partially, and what remains will be enough to have the
full SUSY emerge in the IR.
The complete preserved subgroup of super-Poincaré is the semidirect product of the
super-translations and of the bosonic OSp(d|2) subgroup SO(d) × Sp(2):

Gϕω (k) = Gψψ̄ (k) =

Rd|2 ⋊ [SO(d) × Sp(2)] .

– 17 –

(3.16)

JHEP03(2021)219

where FΛ (k 2 ) is a function vanishing for k 2 ⩾ Λ2 , Λ the UV cutoff. Note the second term
in Gϕϕ (k), which is the price to pay for maintaining exact SUSY in a Wilsonian scheme.
E.g. if FΛ (k 2 ) = Θ(Λ2 − k 2 ) we see that we need to add a term proportional to δ(k 2 − Λ2 ).
If the theory were regulated without this term, exact SUSY would be broken. E.g. H would
be renormalized as a result. This will be discussed in the next section.

## PDF page 21

This will be referred to as “partial SUSY”. That the usual bosonic translations, rotations,
and global fermionic Sp(2) are preserved by the propagators (3.15) is fairly obvious. A
more subtle fact is that the super-translations (3.2) are also preserved. Indeed, for the
superfield two-point function, partial SUSY imposes the requirement
⟨Φ(x1 , θ1 , θ̄1 )Φ(x2 , θ2 , θ̄2 )⟩ = A(x212 ) + B(x212 )(θ1 − θ2 )(θ̄1 − θ̄2 ) .

(3.17)

∫

1
1
dd xdθdθ̄ − ΦFΛ−1 (∂ 2 )∂ 2 Φ + ΦHΛ (∂ 2 )∂θ ∂θ̄ Φ ,
2
2
[

]

(3.18)

which makes it manifest that it preserves partial SUSY.
We are therefore led to consider RG flows which preserve only the partial SUSY (3.16)
(as well as the global Ising Z2 invariance which flips the sign of all fields). The most
general term invariant under (3.16) can be written as the superspace integral of a local
operator built from the superfield Φ, allowing contractions of the derivatives in x and θ
which preserve SO(d)×Sp(2) and not necessarily the full OSp(d|2). The two terms in (3.18)
are of such form. The structure of the effective Lagrangian is thus less constrained than
under the full SUSY.
However, and this is the key point which saves the day, at the relevant and marginal
level, we find only one new term which is invariant under partial SUSY and not under full
SUSY: this is the ω 2 originating from Φ∂θ ∂θ̄ Φ. It is obviously invariant because ω does
not transform under supertranslations. All the other term allowed by partial SUSY and
breaking full SUSY are irrelevant.
Let us go through the list of candidates, starting from the SUSY mass term ϕω + ψ ψ̄.
It is fully super-rotation and super-translation invariant, but in fact already partial SUSY
(supertranslations) fixes the relative coefficient, as is easy to check from (3.2). Same for the
quartic interaction ωϕ3 +3ψ ψ̄ϕ2 . Terms ϕ2 or (∂ϕ)2 are not supertranslation invariant, very
fortunately so since they would completely ruin the structure of the quadratic Lagrangian
if generated.
Due to this lucky circumstance, we expect that the following will happen. The theory
LSUSY regulated in a partial-SUSY preserving way will flow, for an appropriate bare mass
value, to the fully SUSY fixed point in the IR, and the only effect will be a renormalization
of the coefficient of ω 2 : HIR ̸= HUV .21
Let us see how this happens in detail in a toy model example. Let S(H) denote the
SUSY theory regulated in a fully SUSY-invariant way, H being the superspace parameter,
21

As discussed in section 3.1, parameter H is unphysical (redundant) when sitting at a SUSY RG fixed
point. But a change in this parameter is physical along an RG flow which breaks SUSY.

– 18 –

JHEP03(2021)219

Expanding in components we get Gϕϕ (x) = A(x2 ), Gφω (x) = Gψ̄ψ (x) = B(x2 ), Gωω =
0. This is precisely what eq. (3.15) says: that Gφω = Gψ̄ψ coincide while Gϕϕ may
be unrelated. The functions A and B are independent for the partial SUSY invariance,
while the full SUSY (3.1) requires the superfield two-point function to be a function of
x212 − H4 (θ1 − θ2 )(θ̄1 − θ̄2 ) and implies further relations (2.31).
We can also write the regulated kinetic term (3.14) in superspace as

## PDF page 22

while S̃ the same theory regulated in a way which preserves only partial SUSY. We will
model the cutoff by adding to the action an irrelevant operator, a higher derivative term,
which makes the propagator decay faster in the UV (e.g. 1/k 2 → 1/(k 2 + k 4 /Λ2 )). So we
take
∫
g
S̃ = S(H) + γ dd x Õ,
(3.19)
Λ
where Λ is the UV cutoff, Õ an irrelevant operator of dimension d + γ, γ > 0, which
preserves partial SUSY but not the full one, g a dimensionless coupling. E.g. we can
choose a γ = 2 operator
∫

dθdθ̄ Φ(∂ 2 )2 Φ = ϕ(∂ 2 )2 ω + ψ(∂ 2 )2 ψ̄ .

(3.20)

[Note that were we to choose
O(H) =

∫

dθdθ̄ Φ(D2 )2 Φ = ϕ(∂ 2 )2 ω + ψ(∂ 2 )2 ψ̄ + Hω∂ 2 ω,

(3.21)

it would have been a fully SUSY-preserving regulator.]
Consider the structure of the RG flow within this toy model. After an RG step Λ →
′
Λ = Λ/2 the irrelevant coupling decreases g → g ′ = 2−γ g. The action S(H) experiences
the usual SUSY renormalizations, on top of which we expect to generate a partial-SUSY
preserving (but full SUSY breaking) term ω 2 , with a coefficient ∆H which should be
interpreted as a change in H. This coefficient vanishes in absence of interactions and in
absence of O, thus ∆H = O(λg) where λ is the quartic. Now we have the action S(H)
which had a SUSY regulator adapted to H but the new H ′ = H + ∆H has changed, so we
have to change the SUSY regulator, e.g. by moving a part of Õ to O(H) in (3.21) which
generates a further change in g, ∆g = O(∆H). To summarize, after the RG step, the full
action at the scale Λ′ has the same form as (3.19) with the couplings H and g replaced by
H ′ = H + ∆H,

∆H = O(λg) ,

g ′ = 2−γ g + O(λg) .

(3.22)

From here we draw the following conclusions. First, assuming that the quartic λ remains
small, as it is the case at least for ε ≪ 1, the irrelevant coupling g approaches zero exponentially fast. Second, the series made up of consecutive changes ∆Hi from infinitely many
RG steps needed to reach the IR fixed point converges. Therefore H flows in the IR to a
finite value HIR . In particular we exclude the situation when H flows in IR to infinity.22
See figure 1.
More abstractly, consider the RG flow of the SUSY theory perturbed by two couplings
breaking to partial SUSY, exactly marginal ω 2 and irrelevant Õ:
∫
g
S(H) + g0 ω 2 + γ Õ.
(3.23)
Λ
This time Õ does not have to have the above quadratic form and the discussion can be
generalized easily to several Õ’s. On general grounds, the beta functions have the form
βg0 = O(g),
βg = (γ + O(λ, g0 ) + O(g))g.
22

The opposite situation when H flows to zero is also excluded as finetuned.

– 19 –

(3.24)

JHEP03(2021)219

Õ =

## PDF page 23

HUV

HIR

1/Λ
Figure 1. Schematic RG flow of H and g.

The small initial coupling g will flow to zero in the IR if γ + O(λ, g0 ) is positive. This
quantity (up to d+) can be interpreted as the scaling dimension of Õ at the SUSY fixed
point corrected by g0 ω 2 and since ω 2 is exactly marginal, it should not depend on g0 at all:
γ + O(λ, g0 ) → γ + O(λ). Operators Õ breaking full SUSY to partial SUSY will reappear
in section 8.3 as the susy-writable leader operators, using the terminology to be introduced
below. We will see in sections 9.1 and 10 that all such operators remain irrelevant also in
presence of O(λ) corrections. Thus the coupling g flows to zero, and in the IR we recover
the SUSY fixed point perturbed by an exactly marginal deformation ω 2 , which as discussed
in the previous section amounts to a change in H.

4

RG flow in the full Cardy theory: general plan

Let us recap. In section 2 we used the Cardy transform to rewrite the replica action in
terms of the variables ϕ, χi , ω. This made manifest the presence of a marginally relevant
interaction close to the upper critical dimension. We then dropped some terms in the
action either because they were irrelevant near d = 6 (L1 ), or because they vanished in
the limit n → 0 (L2 ). This was dubbed “basic RG scenario” in section 2.4. The remaining
Lagrangian L0 could be seen formally equivalent to a supersymmetric one LSUSY , replacing
O(−2)-invariant bilinears made of fields χi by Sp(2)-invariant bilinears made out of two
Grassmann fields ψ, ψ̄. Then, in section 3.1 we discussed RG flow in the SUSY theory,
concluding that it has a nontrivial RG fixed point down to d = 4 but not in 3d. This was
based on dimensional reduction and the well-known Wilson-Fisher fixed point properties.
In section 3.2 we discussed the RG flow of L0 theory. Due to subtleties of the UV regulator
the bare theory preserves SUSY only partially (supertranslations but not superrotations),
yet at long distances full SUSY is recovered.
We will now come back to the full Cardy theory L0 + L1 + L2 . We will discuss the RG
flow in this setup and examine the validity of the basic RG scenario assumptions (a) and
(b). We will work in the ϕ, χi , ω formulation rather then in the SUSY field basis ϕ, ψ, ψ̄, ω.

– 20 –

JHEP03(2021)219

g

## PDF page 24

5

Sn invariance in the Cardy basis

The original replicated action (2.7) is invariant under permutations of the n replicas. While
the Cardy transform clarifies many properties of our RG flow, it somewhat obscures this
Sn symmetry, meriting a discussion.23 We have permutations φ1 ↔ φi and φi ↔ φj
(i, j ∈ {2, . . . , n}). After Cardy transform, the latter give rise to permutations χi ↔ χj
which generate Sn−1 subgroup. This symmetry subgroup is manifest in the Cardy basis:
invariance of LCardy under it just means that χi ’s should enter in singlet combinations.
23

In this paper we will be content with using the standard physics literature operational definition of what
is meant by Sn invariance for n ̸∈ N: all algebraic manipulations are done with arbitrary n ∈ N and the
arising rational functions of n are extrapolated to n non-integer or n = 0. Recently, ref. [24] interpreted such
manipulations in terms of Deligne categories, introducing a notion of “categorical symmetry”. Interestingly,
for any group G, there is also a Deligne category interpolating the replica symmetry Sn ⋉ Gn [25, 26],
see [24], section 9.4. This may turn out useful in future rigorous mathematical justifications of the method
of replicas. In this paper we will not use categorical language.

– 21 –

JHEP03(2021)219

Indeed, the full Lagrangian contains some operators involving odd powers of χi fields (e.g.
∑′ 3
χi ϕ) which cannot be written in terms of SUSY fermions. Such operators will play an
important role in stability of the RG flow.
Our plan is as follows. In section 5 we will describe a somewhat peculiar form taken by
the Sn invariance in the Cardy basis. Here we will introduce the notion of a “leader” — the
lowest-dimension part of an Sn -singlet operator transformed to the Cardy basis — and of
its “followers” which are the higher-dimension parts. In the short but important section 6
we will analyze the role of n-suppressed terms. Here we will explain that the assumption
(b) of the basic RG scenario holds, but in a subtle sense: the theory with a small but
finite n is gapped, but as the n → 0 limit is taken, the approximately scale invariant region
of the RG flow becomes longer and longer. This is different from what happens in the
bond-(as opposed to field-) disordered Ising model, where the n ̸= 0 fixed point is believed
to smoothly connect to n = 0, but it suffices for our purposes: L2 can be dropped.
With L2 out of the way, in section 7 we will focus on the L0 + L1 RG flow, working
in the strict n = 0 limit. We will examine if some L1 perturbations (or other Sn -invariant
perturbations generated by RG) which are irrelevant in d = 6 − ε dimensions, may become
relevant in lower d. The leader-follower distinction becomes very handy here, because as
we will see the relevance of an Sn -singlet perturbation can be decided by computing the
scaling dimension of the leader alone.
Next, in section 8, we will classify the leader operators, dividing them into three classes:
non-susy-writable, susy-writable and susy-null. These three classes RG-mix among each
other only in a triangular way, which will simplify the anomalous dimension computations
(section 9). Exhaustive classification of leaders will be carried out up to dimension 12
in d = 6, which includes one or more lowest-lying leaders in each of the three classes.
Anomalous dimensions will be computed at one or two loops.
Figure 2 is a roadmap for all these steps. Once completed, we will see in section 10
what this implies for the loss of Parisi-Sourlas SUSY.

## PDF page 25

<latexit sha1_base64="wTKXnHMZ/PTdvuEHeblKXb/qhW8=">AAACKnicZVBNTwIxEO3iFyIq6NFLIzHxYMiu0egNohePmIiQACHdbhcaut1NO0skyI/gqj/BX+ORePXqf7DLEiMwSTMvb+ZNXp8bCa7BtmdWZmNza3snu5vby+8fHBaKR886jBVldRqKUDVdopngktWBg2DNSDESuII13MF9Mm8MmdI8lE8wilgnID3JfU4JGKqBbdzmErqFkl2254XXgbMApWqlfF15/ZnWukUr3/ZCGgdMAhVE65ZjR9AZEwWcCjbJtWPNIkIHpMdaBkoSMN0Zz/1O8JlhPOyHyjwJeM4uKbwhj/RC85KK/s/HJNABgf6F6XoUuElPLukEUO+PTnaU9vWKHfBvO2MuoxiYpKkbPxYYQpwkhD2uGAUxMoBQxc2HMO0TRSiYHJdsqBBMjLI3Mfk5q2mtg8Zl2bkqO86jSfIOpZVFJ+gUnSMH3aAqekA1VEcUDdAUvaF368P6tGbWV7qasRaaY7RU1vcvtC6q1w==</latexit>

<latexit sha1_base64="miJKc4oaOVe3fQ1BvtdC+39WVvc=">AAACP3icZVDLSgMxFM34rPVVdSVugiK4kDIjiu5adOOyorUFp5RMJlODmWRI7kjLWPwGP8Kt/oK/4Q+4U9y6M9MWsXog3MO594R7T5AIbsB1X52JyanpmdnCXHF+YXFpubSyemlUqimrUyWUbgbEMMElqwMHwZqJZiQOBGsENyd5v3HLtOFKXkAvYa2YdCSPOCVgpXZp/bwtsY/9OFDdzHDZEQz62OcS2qUtt+wOgP8Tb0S2qpXyQeXu/aHWXnEW/VDRNGYSqCDGXHluAq2MaOBUsH7RTw1LCL0hHXZlqSQxM61scEMfb1slxJHS9knAA3XMEd7yxIw83aHpdz8jsYkJXO/aanpxkNf8J5MTGv7I+Yw2kfmzDkRHrYzLJAUm6XCbKBUYFM5TwyHXjILoWUKo5vYgTK+JJhRstmNraAU2WtnpF22A3t+4/pPGXtnbL3vemY3yGA1RQBtoE+0gDx2iKjpFNVRHFN2jR/SEnp0X5835cD6HoxPOyLOGxuB8fQPgO7M4</latexit>

<latexit sha1_base64="p9GMkSDhz99JdoBvF9rb4TS2rKg=">AAACSXicZVDLSgMxFM3Ud9VadekmWAQXMsyIr52iGzeCorUFW0omk2mDmWRI7ohl7N6tP+JWv8E/8CMEl+LKTFvE2gvhHs6953JygkRwA5737hQmJqemZ2bnivMLi6Wl8vLKtVGppqxKlVC6HhDDBJesChwEqyeakTgQrBbcnuTz2h3Thit5Bd2ENWPSljzilIClWuX1Rv9GdkY6qk1kt4cbcaDus0tG3b1escEltMoVz/X6hceBPwSVo0N39/Dh4+m8teyUGqGiacwkUEGMufG9BJoZ0cCpYPZqalhC6C1psxsLJYmZaWZ9Iz28YZkQR0rbJwH32RFFeMcTM9TcD0R/5xmJTUygs2W76cZB3vNLJgc0/KXzHW0i888ORAfNjMskBSbpwE2UCgwK5/HhkGtGQXQtIFRz+yFMO0QTCjbkERtagc1YtnvFok3Q/5/XOKhtu/6O6/sXNstjNKhZtIbW0Sby0T46QqfoHFURRY/oGb2gV+fN+XS+nO/BasEZalbRSBUmfgBsmLYh</latexit>

<latexit sha1_base64="iGw9l/96jV9um3NW8nzorwFGSh8=">AAADBXicZVLNbtQwEHbCXwkFtnDkYlEhIRWtkgoEt1YgVRwqUQTLVmqWyHGcXauOHdnOahfjK3fegyPqtc/BjRfgHZjsRtXudiTLn7+Z+Twzdl4Lbmwc/wnCGzdv3b6zdTe6t33/wcPezqMvRjWasgFVQunTnBgmuGQDy61gp7VmpMoFG+bn71r/cMq04Up+tvOajSoylrzklFigst7fdKHhxprMPU4VxOaaUObSekKkVZVLK2InlAj3wWfHe6snd5QlfpPZB6ZQ1nj/1blOPBeEnvsoNVTz2hr+jUVpzsZcOqLbex0FJ5f4SurYZ/He6inBaRqBP1czh0s+YwXO59jjT5mTqVU4BgEmi04v8tAKlxbjKMp6u3E/Xhi+DpIO7B4e9F8dfP/38yTbCbahAdpUTFoqiDFnSVzbEUhbTgWDixrDamiIjNkZQEkqZkZu0anHz4ApcKk0LChgwa5lFFNemy5ntkxa9TtSmbbvF7CbeZW3e6tkWkCLK7qN0aY0G+XY8s3IcVk3lkm6rKZsBIYJtY+PC64ZtWIOgMBbQEOYTgi8t4UvslaGVhZ+iBx7mF+yOa3rYLjfT172k+QjTPItWtoWeoKeoucoQa/RIXqPTtAA0eAoEEETTMMf4a/wd3ixDA2DLucxWrPw8j/w5v0J</latexit>

<latexit sha1_base64="C0CZ6xNXt5U78uFeZV9+lNHJC6g=">AAACPHicbZBNS8NAEIY3ftb6VfXoZbEIFaEkouhFLAriQfADawttCJvtti5uNmF3IpSYH+G/8eKf8ObFiwcF8erZTdtDrQ4sPPvODDPz+pHgGmz7xRobn5icms7N5Gfn5hcWC0vL1zqMFWVVGopQ1X2imeCSVYGDYPVIMRL4gtX826MsX7tjSvNQXkE3Ym5AOpK3OSVgJK9w2QwI3FAikrN0f4i9083hX3LsOemosmWUVgh6U+JSDzZwk0vwCkW7bPcC/wVnAMXKQXnn4P7r4dwrPJtuGgdMAhVE64ZjR+AmRAGngqX5ZqxZROgt6bCGQUkCpt2kd3uK143Swu1QmScB99ThjoQEWncD31Rm2+vRXCb+l2vE0N5zEy6jGJik/UHtWGAIcWYkbnHFKIiuAUIVN7tiekMUoWDszhsTnNGT/0Jtq+xslx3nwthxiPqRQ6toDZWQg3ZRBZ2gc1RFFD2iV/SOPqwn6836tL76pWPWoGcF/Qrr+wfiVrHk</latexit>

Sn singlet
<latexit sha1_base64="iA75bQyb3dxpnWE6UCLNMW5Q2WU=">AAACSXicZVBNSwMxEM3W76q16tFLUAQPsuyKRW8VvXgRFK0VbCnZbLYNZpMlmS2WtXev/hGv+hv8B/4IwaN4MtsWsXYgzOPNvOHlBYngBjzv3SlMTc/Mzs0vFBeXlksr5dW1a6NSTVmNKqH0TUAME1yyGnAQ7CbRjMSBYPXg7iSf17tMG67kFfQS1oxJW/KIUwKWapU3G4Mb2RnpqDaRvT5uxIG6zy4ZdSv9YoNLaJW3PNcbFJ4E/ghsHVXdSvXh4+m8teqUGqGiacwkUEGMufW9BJoZ0cCpYPZqalhC6B1ps1sLJYmZaWYDI328bZkQR0rbJwEP2DFF2OWJGWnuh6K/84zEJibQ2bXd9OIg7/klkwMa/tL5jjaR+WcHosNmxmWSApN06CZKBQaF8/hwyDWjIHoWEKq5/RCmHaIJBRvymA2twGYs2/1i0Sbo/89rEtT3XH/f9f0Lm+UxGtY82kCbaAf56AAdoVN0jmqIokf0jF7Qq/PmfDpfzvdwteCMNOtorApTP2rQtiA=</latexit>

Z

<latexit sha1_base64="Q8TocOZpr1EAq0Wnc0FjHDwYNvg=">AAAC/XicbVJNbxMxEPUuXyUUSOHIxaJCQgJF2RaJnqoKJAQnykdIpW4UvN7ZxKrXtuzZKmG1/BROHBFX/gr8G2aTgEjKSCs/P8+8nXl25rQK2O//iuJLl69cvbZ1vXNj++at292dOx+CrbyEgbTa+pNMBNDKwAAVajhxHkSZaRhmZ8/b8+E5+KCseY9zB6NSTIwqlBRI1Lj7s5MuROqJF/MmrUwOPvNCQp26qTBoyzotBU6l0PXrZly/GCfNow1mj5jcYmho90cu00KeNZ00g4kytfCtei2JKDM7q9MgvXIY1CfgoXLUcQiQ82zOCZGwMpOGp+l/sgVynAJ/9ZYXakYlziqDJAsmX/2lQzvixt3dfq+/CH4RJCuwe/RR7vN36Zfj8U60TVPIqgSDUosQTpO+wxGpopIaSLUK4GgqMYFTgkaUEEb1YtyGP6jaAQrr6TPIF+xaRX6uXFjVzJZF/57Xogytq49pDfMya9dWKbRA5n/pNseHImy0g8XBqFbGVQhGLrspKs3R8vbSea48SNRzAoK8pIG4nAq6ZqSnsdaGt0gvg+wn/5JNty6C4V4vedJLkjfk5DO2jC12j91nD1nCnrIj9pIdswGT0WGUR2Vk4s/x1/hb/H2ZGkermrtsLeIfvwFgEPuY</latexit>

∈ L0 + L1
fixed by Sn→0

Z

0 Sec.6
Z
<latexit sha1_base64="l5i8uWcpwU8GvvHVJWOu9vbgI4o=">AAACL3icZVBNTwIxEO3iFyIq6NFLIzHxYMiu0egNohePmIiQsIR0u11o6HY37SyRID/Ci1f9Cf4aEy/Gqwf/g10gRmCSZl7ezJu8Pi8WXINtf1iZldW19Y3sZm4rv72zWyju3esoUZTVaSQi1fSIZoJLVgcOgjVjxUjoCdbw+tfpvDFgSvNI3sEwZu2QdCUPOCVgKFdiFyJsY5dL6BRKdtmeFF4GzgyUqpXyeeXx56nWKVp5149oEjIJVBCtW44dQ3tEFHAq2DjnJprFhPZJl7UMlCRkuj2amB7jI8P4OIiUeRLwhJ1T+AMe65nmYSr6Px+RUIcEeiem62HopT29pFNA/T863VE60At2ILhsj7iME2CSTt0EicAmjTQm7HPFKIihAYQqbj6EaY8oQsGEOWdDRWCylN2xyc9ZTGsZNE7LzlnZcW5NkldoWll0gA7RMXLQBaqiG1RDdURRjJ7RC3q13qx369P6mq5mrJlmH82V9f0LpPms1g==</latexit>

n→0
z
}|
{
Sec.5 O = OL + OF1 + OF2 + · · · + n(. . . )
|
{z
}
<latexit sha1_base64="kBLWEH+6f0fthtQN8b6cdHSmJuk=">AAACSXicZVBNSwMxEM3W76q16tFLUAQPsuyKUm8VvXgRFK0VbCnZbLYNZpMlmS2WtXev/hGv+hv8B/4IwaN4MtsWsXYgzOPNvOHlBYngBjzv3SlMTc/Mzs0vFBeXlksr5dW1a6NSTVmNKqH0TUAME1yyGnAQ7CbRjMSBYPXg7iSf17tMG67kFfQS1oxJW/KIUwKWapU3G4Mb2RnpqDaRvT5uxIG6zy4ZdSv9YoNLaJW3PNcbFJ4E/ghsHVXdg+rDx9N5a9UpNUJF05hJoIIYc+t7CTQzooFTwezV1LCE0DvSZrcWShIz08wGRvp42zIhjpS2TwIesGOKsMsTM9LcD0V/5xmJTUygs2u76cVB3vNLJgc0/KXzHW0i888ORIfNjMskBSbp0E2UCgwK5/HhkGtGQfQsIFRz+yFMO0QTCjbkMRtagc1YtvvFok3Q/5/XJKjvuf6+6/sXNstjNKx5tIE20Q7yUQUdoVN0jmqIokf0jF7Qq/PmfDpfzvdwteCMNOtorApTP25gtiI=</latexit>

suppressed by rescaling

Sec.7

<latexit sha1_base64="Zyk14DF0G64VD/rgeOHKfXO1ptQ=">AAACSXicZVBNSwMxEM3W76q16tFLUAQPsuyKYm8VvXgRFK0VbCnZbLYNZpMlmS2WtXev/hGv+hv8B/4IwaN4MtsWsXYgzOPNvOHlBYngBjzv3SlMTc/Mzs0vFBeXlksr5dW1a6NSTVmNKqH0TUAME1yyGnAQ7CbRjMSBYPXg7iSf17tMG67kFfQS1oxJW/KIUwKWapU3G4Mb2RnpqDaRvT5uxIG6zy4ZdSv9YoNLaJW3PNcbFJ4E/ghsHVXdg+rDx9N5a9UpNUJF05hJoIIYc+t7CTQzooFTwezV1LCE0DvSZrcWShIz08wGRvp42zIhjpS2TwIesGOKsMsTM9LcD0V/5xmJTUygs2u76cVB3vNLJgc0/KXzHW0i888ORJVmxmWSApN06CZKBQaF8/hwyDWjIHoWEKq5/RCmHaIJBRvymA2twGYs2/1i0Sbo/89rEtT3XH/f9f0Lm+UxGtY82kCbaAf56BAdoVN0jmqIokf0jF7Qq/PmfDpfzvdwteCMNOtorApTP3AotiM=</latexit>

<latexit sha1_base64="slUf0dI+ZS860A4Oe5LrTcCVIwc=">AAACMHicZVBdSwJBFJ21L7MsrcdehiToIWQ3inpT6qVHg0zBFZmdndXB2dll5q4k5o/opdf6C/2a6Cl6DfoPzapE6oXhHs6953LmeLHgGmz7w8qsrK6tb2Q3c1vb+Z3dQnHvXkeJoqxOIxGppkc0E1yyOnAQrBkrRkJPsIbXv07njQFTmkfyDoYxa4ekK3nAKQFDua6XCMEAu1xCp1Cyy/ak8DJwZqBUrZTPK48/T7VO0cq7fkSTkEmggmjdcuwY2iOigFPBxjk30SwmtE+6rGWgJCHT7dHE9BgfGcbHQaTMk4An7JzCH/BYzzQPU9H/+YiEOiTQOzFdD0Mv7eklnQLq/9HpjtKBXrADwWV7xGWcAJN06iZIBIYIpzFhnytGQQwNIFRx8yFMe0QRCibMORsqApOl7I5zJkBnMa5l0DgtO2dlx7k1UV6haWXRATpEx8hBF6iKblAN1RFFMXpGL+jVerPerU/ra7qasWaafTRX1vcvqKytrQ==</latexit>

<latexit sha1_base64="CVYdYA0m5fXzpvQZndNJiJS9LBs=">AAACR3icZVA9SwNBEN2L39Fo1NJmNQgWEu5E0U7RxlLBGMGEsLe3lyzux7E7Fwxnamt/iK3+Bf+CP0JLsXQvCWLiwDCPN/OGmRcmglvw/XevMDU9Mzs3v1BcXCotr5RX166tTg1lNaqFNjchsUxwxWrAQbCbxDAiQ8Hq4d1Z3q93mbFcqyvoJawpSVvxmFMCjmqVN3FDhvo+I0pLInRqccQlU/m87eMGV9AqV/yqPwj8HwQjUDk5rh4cP3w8XbRWvVIj0jR1a4AKYu1t4CfQzIgBTgXrFxupZQmhd6TNbh1URDLbzAa/9PG2YyIca+NSAR6wY4qoyxM70twPRX/7GZFWEujsump7MsxrvsnmgEa/dD5jbGwnzoH4qJlxlaTAFB1eE6cCg8a5e84cwyiIngOEGu4ewrRDDKHgPB47w2hwFqt2v+gMDCbt+g/qe9VgvxoEl87KUzSMebSBttAOCtAhOkHn6ALVEEWP6Bm9oFfvzfv0vrzv4WjBG2nW0VgUvB+3nbYf</latexit>

<latexit sha1_base64="gV/31PVOpJslSeBdy9MrytCHLUc=">AAACSXicZVBNSwMxEM3W76q16tFLsAgeZNkVRT0pevEiKFpbsKVks9k2mE2WZFYsa+9e/SNe9Tf4D/wRgkfxZLYtYu1AmMebecPLCxLBDXjeu1OYmJyanpmdK84vLJaWyssr10almrIqVULpekAME1yyKnAQrJ5oRuJAsFpwe5LPa3dMG67kFXQT1oxJW/KIUwKWapXXG/0b2RnpqDaR3R5uxIG6zy4ZdQ96xQaX0CpXPNfrFx4H/hBUjg7d3cOHj6fz1rJTaoSKpjGTQAUx5sb3EmhmRAOngtmrqWEJobekzW4slCRmppn1jfTwhmVCHCltnwTcZ0cU4R1PzFBzPxD9nWckNjGBzpbtphsHec8vmRzQ8JfOd7SJzD87EO03My6TFJikAzdRKjAonMeHQ64ZBdG1gFDN7Ycw7RBNKNiQR2xoBTZj2e4VizZB/39e46C27fo7ru9f2CyP0aBm0RpaR5vIR3voCJ2ic1RFFD2iZ/SCXp0359P5cr4HqwVnqFlFI1WY+AFx8LYk</latexit>

<latexit sha1_base64="slUf0dI+ZS860A4Oe5LrTcCVIwc=">AAACMHicZVBdSwJBFJ21L7MsrcdehiToIWQ3inpT6qVHg0zBFZmdndXB2dll5q4k5o/opdf6C/2a6Cl6DfoPzapE6oXhHs6953LmeLHgGmz7w8qsrK6tb2Q3c1vb+Z3dQnHvXkeJoqxOIxGppkc0E1yyOnAQrBkrRkJPsIbXv07njQFTmkfyDoYxa4ekK3nAKQFDua6XCMEAu1xCp1Cyy/ak8DJwZqBUrZTPK48/T7VO0cq7fkSTkEmggmjdcuwY2iOigFPBxjk30SwmtE+6rGWgJCHT7dHE9BgfGcbHQaTMk4An7JzCH/BYzzQPU9H/+YiEOiTQOzFdD0Mv7eklnQLq/9HpjtKBXrADwWV7xGWcAJN06iZIBIYIpzFhnytGQQwNIFRx8yFMe0QRCibMORsqApOl7I5zJkBnMa5l0DgtO2dlx7k1UV6haWXRATpEx8hBF6iKblAN1RFFMXpGL+jVerPerU/ra7qasWaafTRX1vcvqKytrQ==</latexit>

• classification

Sec.8

• anomalous dimensions

Sec.9

Figure 2. This figure illustrates how a generic Sn -singlet perturbation O is divided into various
pieces (leader, followers, n-suppressed) and shows the sections of our paper where these pieces are
discussed.

Consider now permutations of the former kind, φ1 ↔ φi . Without loss of generality
we focus on φ1 ↔ φ2 since together with Sn−1 it generates the full Sn . Applying Cardy
transform with φ2 and φ1 interchanged, the relation between the new and old Cardy fields
is found from the equations
ω
ω′
= ϕ′ −
+ χ′2 ,
2
2
ω
ω′
φ 2 = ϕ − + χ 2 = ϕ′ + ,
2
2
′
ω
ω
φ i = ϕ − + χ i = ϕ′ −
+ χ′i
2
2
φ1 = ϕ +

(i = 3 . . . n),

(5.1)

where we renumbered the fields χ′i so that their index always runs from 2 to n. We thus
find
2−n
(ω − χ2 ),
2(1 − n)
ω
n
ω′ =
−
χ2 ,
1−n 1−n
2−n
χ2
χ′2 =
ω−
,
1−n
1−n
ω − χ2
χ′i = χi +
(i = 3 . . . n).
1−n
ϕ′ = ϕ −

– 22 –

(5.2)

JHEP03(2021)219

at the IR fixed point

<latexit sha1_base64="TsjX1+EusArsDJ2FTlWdEMI1IRE=">AAACQHicZVDNSgMxEM7Wv1r/qt70EiyCBym7ouhN0YvHCtYW2lKy2WwNZpMlmS2WteAr+BJe9RV8DJ/Ak4hXT2bbUqwdGObjm/mGmc+PBTfguu9ObmZ2bn4hv1hYWl5ZXSuub9wYlWjKqlQJpes+MUxwyarAQbB6rBmJfMFq/t1F1q91mTZcyWvoxawVkY7kIacELNUubjUjX92nVBBjxnQfN7mEdrHklt1B4GngjUDp7LR8dPrw+VRprzsrzUDRJGISBgsbnhtDKyUaOBWsX2gmhsWE3pEOa1goScRMKx080ce7lglwqLRNCXjATiiCLo/NSHM/FP3tpyQyEYHbfVtNL/Kzmm0yGaDBmM5mtAnNv3MgPGmlXMYJMEmH14SJwKBwZhsOuGYURM8CQjW3D2F6SzShYM2dOEMrsCbKTr9gDfT+2zUNagdl77DseVfWynM0jDzaRjtoD3noGJ2hS1RBVUTRI3pGL+jVeXM+nC/neziac0aaTTQRzs8vDda0XA==</latexit>

## PDF page 26

We will mostly use the n → 0 limit of this “extra” symmetry transformation, which is
ϕ′ = ϕ − 2(ω − χ2 ),
ω ′ = ω,
χ′2 = 2ω − χ2 ,
χ′i = χi + ω − χ2

(i = 3 . . . n).

(5.3)

Let us see how LCardy behaves under this. The ω 2 term in L0 , eq. (2.22), is trivially
invariant. It is more interesting to check that the mass term is invariant:
n
∑

χ2i → 2[ϕ − 2(ω − χ2 )]ω + (2ω − χ2 )2 +

i=2

n
∑

(χi + ω − χ2 )2 ,

(5.4)

i=3

and using the constraint ′ χi = 0 we see that the r.h.s. reduces to the l.h.s. Analogously
the kinetic part ∂ϕ∂ω + 12 (∂χi )2 is also invariant.
For the quartic term, Sn invariance is realized in a still more interesting way. The
∑
quartic term is the marginal (in d = 6) part of the Sn invariant term σ4 = ni=1 φ4i whose
full n → 0 limit is
∑

[

σ4 = 4ωϕ3 + 6

∑′

[

+ 4ϕ

∑′

χ3i

]

[

∑′

χ3i

]

− 2ω

χ2i ϕ2

∆=7

]

+

[∆=6
∑′

χ4i − 6ϕω

∑′

χ2i

]
∆=8

3 ∑′ 2
+ ω2
,
χi + ϕω 3
∆=9
2
∆=10
[

]

(5.5)

where we indicated the scaling dimensions in d = 6. The irrelevant terms in the second
and third lines have been assigned to the L1 part of the Lagrangian. It is now possible to
check that the sum of all terms is invariant under the n = 0 symmetry (5.3), although the
first line by itself is not.
We thus learn something very important: the sum L0 + L1 is invariant under the full
Sn symmetry in the n → 0 limit (denoted Sn→0 ), while individually the two parts are
invariant only under the Sn−1 subgroup permuting χi ’s.
And what about L2 ? It was originally defined as consisting of the n-suppressed terms,
but now we can give an alternative description: L2 consists of all terms which are not invariant under the extra symmetry (5.3), nor can be made invariant by adding further terms.
Consider e.g. ϕ2 , which is in L2 according to (2.24). Under the extra symmetry we have:
ϕ2 → [ϕ − 2(ω − χ2 )]2 = ϕ2 − 4(ω − χ2 )ϕ + 4(ω − χ2 )2 .

(5.6)

This is obviously not invariant by itself, nor can it be made invariant by adding other
terms. E.g. variation of ϕ2 contains −4ωϕ and a moment’s thought shows that this cannot
be canceled by variation of anything.
Since the terms in L2 are not invariant under the Sn→0 symmetry, their coefficients
must be proportional to n. This explains why they are “n-suppressed”. The advantage
of this new understanding is that it is not tied to the bare Lagrangian but can be used
along the RG flow. Since L0 + L1 are Sn→0 invariant, they can generate L2 terms only with
n-suppressed coefficients. This guarantees that a term n-suppressed in the bare Lagrangian
remains n-suppressed at a lower RG scale.

– 23 –

JHEP03(2021)219

2ϕω +

## PDF page 27

5.1

Sn singlets in the replicated basis

As pointed out by Brézin and De Dominicis [27], the replicated Lagrangian (2.7), in addition
to the shown bare terms, will generate infinitely many extra Sn invariant terms upon RG
flow.24 Of course, these terms may or may not destabilize the RG flow depending on their
scaling dimensions. Leaving this more complicated question for later, let us first learn to
write general Sn invariant terms (referred to as “singlets” from now on). In the replicated
basis, they can be constructed as finite products:
⎤[
]⎡ n
]
n
∑
∑
A(φi ) ⎣
B(φj )⎦
C(φk ) × . . .
j=1

i=1

(5.7)

k=1

where A, B, C . . . are some polynomial25 functions of φi and of its derivatives. For most
part we will be interested in scalar perturbations, which means that A, B, C either do not
contain derivatives, or that all derivative indices are contracted. 26
∑ ∑
We will use the notation ( ≡ ni=1 )
σk =

∑

φki ,

σk(µ) =

∑

φk−1
∂µ φi ,
i

σk(µν) =

∑

φk−1
∂µ ∂ν φi ,
i

σk(µ)(ν) =

∑

φk−2
∂µ φi ∂ν φi ,
i

etc .

(5.8)

The fields σk were considered in [27], and the others are natural generalizations. More
singlets can be constructed by taking products of these basic building blocks.
In this notation, e.g., the bare replicated Lagrangian (quartic potential) is a linear
combination of singlets
σ2(µ)(µ) ,

σ12 ,

σ2 ,

σ4 .

(5.9)

But we can clearly construct more singlets. E.g. with four fields and no derivatives the full
list has five singlets [27]:
σ4 ,

σ 1 σ3 ,

σ22 ,

σ12 σ2 ,

σ14 .

(5.10)

Still more singlets are obtained by increasing the number of fields or introducing derivatives.
What are the scaling dimension of the corresponding fixed point perturbations? Can they
become relevant as the dimension is lowered? We will study these questions systematically
in the subsequent sections.
24

Depending on the circumstances, these extra terms may be present already in the bare action, as was
demonstrated explicitly in [27] via the Hubbard-Stratonovich transformation from the lattice model.
25
Limiting to polynomial interactions is standard when dealing with perturbation of Gaussian fixed points.
Some literature on the RFIM (e.g. [28]) consider interactions with non-polynomial field dependence, such
as absolute value of the fields (“cusps”). In appendix A.8 we explain that cusp interactions do not yield new
perturbations of Gaussian fixed points, the full spectrum of independent perturbations given by polynomial
interactions.
26
Contractions of derivative indices from different factors, e.g. from A and B, are allowed.

– 24 –

JHEP03(2021)219

[ n
∑

## PDF page 28

Feldman [29]27 discussed a family of singlet operators Fk (k ∈ 2N) given by
Fk =

n
∑

(φi − φj )k =

i,j=1

k−1
∑

( )

(−1)l

l=1

k
σl σk−l
l

(5.11)

(the l = 0, k terms vanish for n → 0). Operators F4 and F6 will play an important role in
our work.
5.2

Sn singlets in the Cardy basis

σ2 = 2ϕω +

∑′

(5.12)

χ2i ,

while σ4 is given in (5.5). We will use this procedure to construct all singlets in the Cardy
basis. Generality of this method follows from the fact that the Cardy transform is an
invertible linear transformation of the field basis. We have the following master formula
(here and below we drop terms vanishing in the n = 0 limit):28
n
∑

(

A(φi ) = A ϕ +

i=1

=

ω
2

)

+

∑′

(

A ϕ−

ω
+ χi
2

)

(5.13)

∑′
δA
1 δ2A
(ϕ)ω +
(ϕ)
χ2i
δϕ
2 δϕ2

+

∞
∑
1 δk A
k=3

k! δϕk

(ϕ)

[( )
ω k

2

+

∑′ ( ω

−

2

+ χi

)k ]

.

(5.14)

Let us introduce some useful terminology. By composite operators (composites, for short)
we will mean products of Cardy fields, their derivatives, and linear combinations thereof.
To each product composite we assign a classical scaling dimension which is the sum of
dimensions of its constituents, eq. (2.16). A linear combination of composites has a “welldefined classical dimension” if all terms have the same dimension. Later on, we will also
discuss anomalous dimensions due to interactions. Due to mixing, only some special linear
combinations will have well-defined anomalous dimensions.
In this terminology, the terms in the first line of (5.14) have the same classical dimension, while those in the second line have a higher dimension. For singlets involving at
most two fields (σ1 , σ2 , σ1(µ) , σ2(µ) , etc), the second line is absent (δ k A/δϕk ≡ 0). Such
fields, and products thereof, are special: they have well-defined classical dimensions in the
Cardy basis.29 One example is (5.12) where both composites have dimension d − 2. Any
27

Ref. [29] focuses on the Random Field O(N ) Model, and the part starting from eq. (8) applies also to
the RFIM setting N = 1. In our work we will find support for some of Feldman’s results, but we will draw
from them a different conclusion.
28
Variational derivative notation allows for the case when A depends on the derivatives of φ. In this case
these derivatives have to be distributed on the fields following δ k A/δϕk , in an obvious manner. Note that
(δ k A/δϕk )ω k terms with k even are n-suppressed (A(ϕ) and (δ 2 A/δϕ2 )ω 2 being two examples).
29
This is only true in the n = 0 limit which is assumed here.

– 25 –

JHEP03(2021)219

Applying the Cardy transform to any singlet in the replicated basis, we get an Sn→0 singlet
in the Cardy basis. We have already seen such expressions above, e.g.

## PDF page 29

other singlet will becomes a linear combination of composites of different dimensions in the
Cardy basis. We have seen one example in (5.5).
Given any singlet O, we can split it into parts with definite classical dimension, which
will come in unit steps:
O = [O]∆ + [O]∆+1 + . . .
(5.15)

Fk = 2

n
∑

(ω − χi )k +

i=2

n
∑

(χi − χj )k .

(5.16)

i,j=2

In particular there is no dependence on ϕ for this very special operator. Expanding we
have
Fk =

k−2
∑

( )

(−1)

l=2

−2kω

l

k (∑′ l ) (∑′ k−l )
χi
χi
l

(∑ ′

(5.17)

)

χk−1
+ ...
i

where we used ′ χi = 0 and that ′ χki cancels between the two terms for n → 0. This
shows the leader (first line) and the first follower for k ⩾ 4. (For k = 2 the shown terms
vanish and F2 = −2ω 2 .)
∑

6

∑

The n-suppressed terms

Following our plan to clarify step-by-step the basic RG scenario of section 2.4, we will
discuss here the effects associated with the n-suppressed terms, which were grouped in
the L2 part of the Cardy-transformed Lagrangian (2.25). As explained in section 5, these
terms can be alternatively characterized as those which break the Sn→0 symmetry of the
L0 + L1 Lagrangian. This implies that the terms n-suppressed in the bare Lagrangian
remain n-suppressed along the RG flow. If we set n = 0, these terms vanish in the bare
Lagrangian and are not regenerated in the RG flow. Still, it is instructive to analyze what
would happen if we worked at a tiny but nonzero n. Note that L2 contains several relevant
terms so that, while n-suppressed, they grow in the IR. One such term is the operator ϕ2 ,
which comes from the operator σ2 ∋ nϕ2 (while the n = 0 part of σ2 goes into L0 ). What
would be the role of these terms for the IR behavior of the theory?
For concreteness let us just focus on this very operator ϕ2 , the discussion being
similar for any other relevant part of L2 such as ϕ4 or (∂ϕ)2 . We thus consider L0 action
perturbed by
∫
g2
dd x ϕ2 ,
(6.1)
Λ4UV

– 26 –

JHEP03(2021)219

We will call the “leader” the lowest scaling dimension part of O, that is [O]∆ , while [O]∆+k
with k ⩾ 1 will be called “followers”. E.g. the first line of the r.h.s. of (5.5) is the leader
of σ4 , while the subsequent lines contains the followers. The rationale for this terminology
will become clear in section 7.
As an exercise which will turn out useful later on, let us transform Feldman operators
to the Cardy basis and extract the leader. Using definition (5.11) we have:

## PDF page 30

<latexit sha1_base64="fr5FT6wDrBCK/1TjXayvCzCzE+U=">AAAClXicbVFbS8MwFM7qfV6nDz74UhyCT6N14uVBGCrimxOdClsZaXq6BZO0JKkyan+Cr/rb/Dc2dchuHwS+fOc7Oefk+DGjSjvOT8mam19YXFpeKa+urW9sblW2n1SUSAItErFIvvhYAaMCWppqBi+xBMx9Bs/+65WJP7+BVDQSj3oQg8dxT9CQEqxz6aHXpd2tqlNzCtjTxB2SKhqi2a2UPjpBRBIOQhOGlWq7Tqy9FEtNCYOs3EkUxJi84h60cyowB+WlRa+ZfZArgR1GMj9C24U6mpFirtSA+7mTY91XkzEjzowFyjw4K9ROdHjmpVTEiQZB/noIE2bryDZ/YgdUAtFskBNMJM3HsEkfS0x0/nPlg9EqkBDMsnHNFJQqVNlkr6Yhowp4JxHnWARpx2cJZG3XS9NOMXtaCFU3m/BJCMZs5l64in2dG5z8b2eaPB3V3Hqtfn9cbVwON7eM9tA+OkQuOkUNdIuaqIUI6qFP9IW+rV3rwrq2bv6sVmmYs4PGYN39Art8zsU=</latexit>

gi
g0
<latexit sha1_base64="rAEDyM9sUU1BRreoah4ASySo6kI=">AAAClXicbVFbS8MwFM7qfV6nDz74UhyCT6N14uVBGCrimxOdClsZaXq6BZO0JKkyan+Cr/rb/Dc2dchuHwS+fOc7Oefk+DGjSjvOT8mam19YXFpeKa+urW9sblW2n1SUSAItErFIvvhYAaMCWppqBi+xBMx9Bs/+65WJP7+BVDQSj3oQg8dxT9CQEqxz6aHXdbpbVafmFLCniTskVTREs1spfXSCiCQchCYMK9V2nVh7KZaaEgZZuZMoiDF5xT1o51RgDspLi14z+yBXAjuMZH6Etgt1NCPFXKkB93Mnx7qvJmNGnBkLlHlwVqid6PDMS6mIEw2C/PUQJszWkW3+xA6oBKLZICeYSJqPYZM+lpjo/OfKB6NVICGYZeOaKShVqLLJXk1DRhXwTiLOsQjSjs8SyNqul6adYva0EKpuNuGTEIzZzL1wFfs6Nzj53840eTqqufVa/f642rgcbm4Z7aF9dIhcdIoa6BY1UQsR1EOf6At9W7vWhXVt3fxZrdIwZweNwbr7BT8Fzow=</latexit>

g2

g1

<latexit sha1_base64="qjtEW0AS+bxHiWhUDTP48zpRk3M=">AAAClXicbVFbS8MwFM7qfV6nDz74UhwDn0Y7xcuDMFTENyc6HWxlpOnpDCZpSVJl1P4EX/W3+W9s6pBd/CDw5TvfyTknx48ZVdpxvkvW3PzC4tLySnl1bX1jc6uy/aiiRBJok4hFsuNjBYwKaGuqGXRiCZj7DJ78l0sTf3oFqWgkHvQwBo/jgaAhJVjn0v2g3+hvVZ26U8CeJe6IVNEIrX6l9N4LIpJwEJowrFTXdWLtpVhqShhk5V6iIMbkBQ+gm1OBOSgvLXrN7FquBHYYyfwIbRfqeEaKuVJD7udOjvWzmo4Z8d9YoMyD/4W6iQ5PvZSKONEgyG8PYcJsHdnmT+yASiCaDXOCiaT5GDZ5xhITnf9cuTZeBRKCWTapmYJShSqb7tU0ZFQBbyTiHIsg7fksgazremnaK2ZPC6HqZlM+CcGEzdwLV7GvM4Pjv+3MksdG3T2sH94dVZsXo80toz20jw6Qi05QE92gFmojggboA32iL2vXOreurOtfq1Ua5eygCVi3P0Njzo4=</latexit>

<latexit sha1_base64="7gD3PmBjlkkfVBuqTNeD6DexB0E=">AAAClXicbVFbS8MwFM7qfV6nDz74UhwDn0ar4uVBGCrimxPdBbYy0vR0BpO0JKkyan+Cr/rb/Dc2dcg2/SDw5TvfyTknx48ZVdpxvkrW3PzC4tLySnl1bX1jc6uy3VZRIgm0SMQi2fWxAkYFtDTVDLqxBMx9Bh3/+crEOy8gFY3Eox7F4HE8FDSkBOtcehgO3MFW1ak7Bey/xB2TKhqjOaiU3vpBRBIOQhOGleq5Tqy9FEtNCYOs3E8UxJg84yH0ciowB+WlRa+ZXcuVwA4jmR+h7UKdzEgxV2rE/dzJsX5SszEj/hsLlHnwv1Av0eGZl1IRJxoE+ekhTJitI9v8iR1QCUSzUU4wkTQfwyZPWGKi858r1yarQEIwy6Y1U1CqUGWzvZqGjCrglUScYxGkfZ8lkPVcL037xexpIVTdbMYnIZiymXvhKvZ1bnDyu52/pH1Yd4/qR/fH1cbleHPLaA/towPkolPUQLeoiVqIoCF6Rx/o09q1Lqxr6+bHapXGOTtoCtbdN0E0zo0=</latexit>

<latexit sha1_base64="saSI9a7gdiyqmhQ6rp1b85+MV58=">AAACqXicbVHbatwwENW6t2R7yaalT3kRXQKF0sVOQi9voX1pIA9J6SZL1+4ylseJiCQbSW5ZVH9MX9svyt9EcpaS3eSA4OjMGc2MJq8FNzaOL3vRvfsPHj5aW+8/fvL02cZg8/mJqRrNcMwqUelJDgYFVzi23Aqc1BpB5gJP84vPIX76E7Xhlfpm5zVmEs4ULzkD66XZ4GV66M0FzFyqJT342v5wb5N2NhjGo7gDvU2SBRmSBY5mm73faVGxRqKyTIAx0ySubeZAW84Etv20MVgDu4AznHqqQKLJXNd/S7e9UtCy0v4oSzv1ZoYDacxc5t4pwZ6b1VgQ74wVJjx4V2ja2PJD5riqG4uKXfdQNoLaioZ/ogXXyKyYewJMcz8GZeeggVn/m/3tm1WwYSDaZS0U1KY07WqvoaGgKvzFKilBFS7NRYPtNMmcS7vZXScMk3bFp7FYsoV75+r29THg3f/t3CYnO6Nkd7R7vDfc/7TY3BrZIq/Ia5KQ92SffCFHZEwYceQP+Uv+RW+i42gSfb+2Rr1FzguyhIhdAUg71hk=</latexit>

Λ−1
<latexit sha1_base64="RIjmjbg0ueZBCZNlGNplRPvepoI=">AAACnnicbVFNb9QwEPUG+sFSSheOXCxWlbh0lVAE7W1FJcQBRJHYdqVNWk2cSWvVdiLbKVq5+Rtc4W/xb7DTFepu+yRLz2/eeGY8eS24sXH8txc9ery2vrH5pP9069n2853BixNTNZrhhFWi0tMcDAqucGK5FTitNYLMBZ7mV0chfnqN2vBK/bDzGjMJF4qXnIH1Upp+8dYCztxe0p7vDONR3IHeJ8mCDMkCx+eD3k1aVKyRqCwTYMwsiWubOdCWM4FtP20M1sCu4AJnniqQaDLXNd3SXa8UtKy0P8rSTr2b4UAaM5e5d0qwl2Y1FsQHY4UJDz4UmjW2PMgcV3VjUbHbHspGUFvR8Dm04BqZFXNPgGnux6DsEjQw67+wv3u3CjYMRLushYLalKZd7TU0FFSFP1klJajCpblosJ0lmXNpN7vrhGHSrvg0Fku2cO9c3b4OA97/3859cvJ2lOyP9r+/G44/Lja3SV6R1+QNScgHMiafyTGZEEZq8ov8Jn8iGn2Kvkbfbq1Rb5Hzkiwhmv4D/JTSQQ==</latexit>

Figure 3. Schematic RG flow (from short to long distances) including n-suppressed terms. The
flow has three parts (left to right): (1) the transitory part where the couplings g0 of L0 flows to a
fixed point, while the irrelevant couplings g1 of L1 go to zero; (2) the shaded part where the flow
stays close to the L0 fixed point; (3) the part where the relevant L2 terms finally grow to overcome
suppression by n, and the flow deviates from the fixed point.

with ΛUV the UV cutoff energy scale, and g2 a dimensionless coupling. The power of ΛUV
is fixed by the dimension of the perturbing operator, d − 4 in the case at hand.
We are considering the situation when in absence of the perturbation the L0 part of
the action flows to an IR fixed point. When we add the perturbation the coupling g2 starts
growing. Since g2 starts at order-n at the UV scale, it reaches order-1 values at the scale
ΛIR ∼ n1/4 ΛUV .

(6.2)

At that point we can no longer treat it as a small perturbation.
The conclusions from this discussion is that, first of all, the n = 0 fixed point is unstable
with respect to turning on nonzero n. For n tiny but nonzero, the RG trajectory stays for a
long time near the fixed point before finally deviating. Thus, for a very small n, we expect
that in a range of distances the theory will be approximately described by the n = 0 fixed
point and will have an approximate scale invariance, and this range will become longer and
longer as n → 0. However, no matter how small n is, the trajectory eventually deviates
(see figure 3).
We do not know what happens with the small n trajectory afterwards — it may flow to
a gapped phase or to another fixed point. Note that even if the trajectory flows to a fixed
point, such a fixed point would have no significance for the disordered physics, not being
continuously connected to the n = 0 fixed point.30 One example of such a fixed point for
nonzero n can be found in the work of Brézin and De Dominicis [27]. Their fixed point has
couplings scaling as inverse powers of n, a clear feature of being disconnected from n = 0.
For the above reasons we will not consider their fixed point any further in the main text,
although we provide more details in appendix A.9.
30

Incidentally, this is radically different from what happens in the bond-disordered Ising model, where the
fixed point is believed to exist for any n so that we can compute CFT data as a function of n and perform
the n → 0 limit at the CFT level (see section 8.3 of [30], and [4]).

– 27 –

JHEP03(2021)219

Λ−1
IR

## PDF page 31

To summarize, when n → 0, the range in which the flow is close to the L0 fixed point
becomes infinitely large. This clarifies in which sense the n-suppressed terms can be safely
discarded in the limit n → 0.

RG flow in the L0 + L1 theory

7

7.1

Leader and followers: quartic term

In section 5 we saw that after the Cardy transform, a generic Sn singlet is a sum of
the leader (the lowest scaling-dimension part) and the followers (higher scaling dimension
parts). The quadratic terms in the replicated Lagrangian do not have any followers, while
the quartic term has both the leader and the followers, see (5.5).
31

As stressed several times this equivalence holds only in the sector of operators invariant under O(n − 2)
rotations of χi ’s.
32
Sometimes in high-energy physics one calls “dangerously irrelevant” operators which are irrelevant at
the UV fixed point but become relevant at the IR fixed point. We will refrain from this usage of the term,
which is different from statistical physics, where dangerously irrelevant operator is a property of a single
fixed point, not of an RG flow (it is an irrelevant operator whose perturbation effect on the fixed point is
non-analytic in the coupling [31], a typical example being the ϕ4 operator around free massless scalar fixed
point in d > 4 dimensions).

– 28 –

JHEP03(2021)219

At this point we are left with studying the RG flow in the theory consisting of L0 + L1 part
of the Cardy Lagrangian, working in the strict n = 0 limit. As discussed in section 3, the
L0 theory by itself flows to an IR fixed point equivalent31 to the SUSY fixed point of LSUSY .
The key remaining question is whether this RG flow is stable under L1 perturbations.
In the original definition, L1 included all terms irrelevant in d just below 6, coming from
the replicated bare Lagrangian with the quartic potential. This was not completely general:
the bare Lagrangian can be expected to contain any possible Z2 -even Sn singlets, and even
if not initially, included such terms will be generated under RG flow [27]. From now on we
will extend the definition of the bare Lagrangian to include all Z2 -even Sn singlets. E.g., at
the quartic level we should consider all terms given in (5.10) (while only the first of these
five singlets was included so far). It is easy to see that with the new definition we do not
get any additional relevant terms in d = 6 − ε. So all new terms end up in L1 .
Now that we have the full bare Lagrangian, we should ask: can it be that some
perturbations, while irrelevant near 6d, become relevant for smaller d?32 If this happens,
the L0 fixed point will not be reached for those d. The RG flow will be instead deviated
to another fixed point, which does not have SUSY if the new relevant interaction is SUSYbreaking (something to be checked).
We wish to explore this mechanism for the loss of Parisi-Sourlas SUSY. The problem is
well defined, at least in perturbation theory: we need to consider L1 perturbations one by
one, and see which of them get anomalous dimensions of sign and size likely to render them
relevant. We are interested in stability with respect to Sn singlet perturbations, because
only such perturbations are present in the microscopic replicated Lagrangian (i.e. before
the Cardy transform).

## PDF page 32

It is instructive to consider first the RG flow of the L0 +L1 theory truncated just to the
quartic perturbation (5.5). We start the RG flow at an energy scale Λ with the Lagrangian
∑
in the Cardy basis (in equations below we use the notation χki ≡ ′i χki )
)
)
]
1
H
m2 (
λ [(
∂ϕ∂ω + (∂χi )2 − ω 2 +
2ϕω + χ2i +
4ωϕ3 + 6χ2i ϕ2 + 4ϕχ3i + . . . , (7.1)
2
2
2
4!

where . . . stands for the other σ4 followers visible in (5.5). Performing the integrating-out
step down to the energy scale Λ′ = Λ/b (but not yet any field rescaling), we will find an
effective Lagrangian
[

]

(

)

−1/2 −∆0ϕ

ϕ(x) → Z1

b

ϕ(x/b),

0
−1/2
χi (x) → Z1 b−∆χ χi (x/b),
0
−1/2
ω(x) → Z1 b−∆ω ω(x/b),

(7.3)

where ∆0ϕ , ∆0χi , ∆0ω are the Gaussian fixed point dimensions (2.16). After rescaling, the
fields again have momenta up to Λ while the Lagrangian becomes:
1
Z2 H 2 (m′ )2 b2
1
∂ϕ∂ω + (∂χi )2 −
ω +
ϕω + χ2i
(7.4)
2
Z1 2
Z1
2
[
(
)]
) 1
) 1
λ ′ bε (
1 ( 4
1 3 2 2
3
2 2
3
2
3
+
4ωϕ
+
6χ
ϕ
+
4ϕχ
+
χ
−
6ϕωχ
ω χi + ϕω 3 .
i
i
i
i − 3 2ωχi + 4
2
2
b
b
b
b 2
4!Z1
(

)

We see that in general Z2 ̸= Z1 and H will be renormalized. However as discussed in
section 3.2 we can expect that this effect is transient and disappears in deep infrared so
that H flows to a constant. Here we are focusing on the behavior of the σ4 followers,
this time written in full. We see that their coefficients rescale with an additional positive
integer power of b compared to that of the leader. But, apart from this additional rescaling,
the relative coefficients stay fixed because determined by Sn invariance. This explain our
choice for the leader-follower terminology.
After many RG steps the coefficients of the followers will flow to zero, and we approach
the fixed point of the L0 theory. It is not so surprising that the follower coefficients flow
to zero as these operators are irrelevant. What is more surprising is that the coefficients of
these irrelevant terms go to zero in a prescribed fashion. This feature of the L0 + L1 RG
flow is dictated by Sn invariance.
We can rephrase the above conclusions as follows. Consider the perturbation (δλ)σ4
on top of the L0 fixed point, splitting it into the leader and the followers:
(δλ)σ4 = δλ

[(

)

]

4ωϕ3 + 6χ2i ϕ2 + 4ϕχ3i + . . . .

– 29 –

(7.5)

JHEP03(2021)219

)
]
1
H
1
λ′ [(
Z1 ∂ϕ∂ω + (∂χi )2 −Z2 ω 2 +(m′ )2 ϕω + χ2i +
4ωϕ3 + 6χ2i ϕ2 + 4ϕχ3i + . . . .
2
2
2
4!
(7.2)
1
2
Crucially, Sn invariance guarantees that the kinetic terms ∂ϕ∂ω + 2 (∂χi ) , the mass terms
2ϕω + χ2i , and the whole quartic interaction renormalize by overall rescaling, since the form
of these terms is fixed uniquely by transforming σ2(µ)(µ) , σ2 and σ4 to the Cardy basis. We
now perform field rescaling

## PDF page 33

At a lower scale Λ/b the perturbation will become
δλ(b)

[(

) 1
4ωϕ3 + 6χ2i ϕ2 + 4ϕχ3i + . . . .
b
]

(7.6)

where y must be positive for δλ to flow to zero.
The simplest way to compute y is to go to deep IR. There the coefficients of the followers
are tiny and can be neglected. We are therefore reduced to the problem of computing the
anomalous dimension of the leader as a perturbation of the L0 fixed point. This recipe
is a key simplification: it would have been much more awkward to compute anomalous
dimension if we had to keep track of both the leader and the followers.
For the quartic coupling case at hand, y is related to the anomalous dimension of
(
)
4ωϕ3 + 6χ2i ϕ2 perturbing the L0 fixed point.
This being )a susy-writable operator, its
(
anomalous dimension is the same as that of 4ωϕ3 + 3ψ ψ̄ϕ2 perturbing the LSUSY fixed
point. In turn, by dimensional reduction, this is the same as the anomalous dimension of
φ̂4 at the Wilson-Fisher fixed point in d − 2 dimensions (see section 9.1 below). The latter
operator is irrelevant since the Wilson-Fisher fixed point has only one relevant Z2 even
singlet (φ̂2 ), hence indeed y > 0.
7.2

Leader and followers: general case

We will now generalize the quartic coupling perturbation considered in the previous section
to any other singlet perturbation gO inside the L0 + L1 flow. Near the L0 fixed point, this
perturbation takes the form
1
1
g(b) OL + OF 1 + 2 OF 2 + . . . + ,
b
b
[

]

d
g = −yO g,
d log b

(7.8)

where OL is the leader, while OF 1 , OF 2 , . . . are the followers. If the leader coefficient flows
to zero (yO > 0), the follower coefficients flow to zero as well, and faster. The RG eigenvalue
yO can be computed as
yO = ∆(OL ) − d,

(7.9)

where ∆(OL ) is the scaling dimension of OL as a perturbation of the L0 fixed point. A
very convenient feature is that the followers do not enter into the latter computation.
We are thus converging on a well-defined problem of quantum field theory. We have to
classify all perturbations of the L0 fixed point which can be realized as leaders of Z2 -even
Sn singlets, and compute their anomalous dimensions. If one of these becomes relevant,
stability of the L0 fixed point is lost. This program will be realized in section 8 and 9 below.

– 30 –

JHEP03(2021)219

We see here two effects. First, the coefficients of the followers are suppressed compared to
that of the leader by integer powers of b. Second, assuming that the fixed point is reached,
δλ(b) flows to zero (which is the same as λ flowing to a constant). Let us introduce the
RG eigenvalue y for δλ:
d
δλ = −yδλ,
(7.7)
d log b

## PDF page 34

7.3

Followers as individual L0 perturbations

[

1
H
∂ϕ∂ω + ∂χi ∂χi − ω 2 + h1 σ4 + h2 σ22 + h3 σ1 σ3 + h4 σ12 σ2 + h5 σ14 .
2
2
]

(7.10)

When we transform these singlets into the Cardy basis, we get a total of 11 monomials.
We then consider a more general RG flow introducing 11 independent couplings for each
of these monomials:
[

1
H
∂ϕ∂ω + ∂χi ∂χi − ω 2 + 6g1 ϕ2 χ2i + 4g2 ϕ3 ω + 4g3 ϕχ3i + g4 χ4i
2
2
2
+ g5 ϕωχi + g6 ωχ3i + g7 ω 2 χ2i + g8 ϕω 3 + g9 χ4i + g10 ϕωχ2i + g11 ω 4 .
]

(7.11)

When these 11 couplings are set to particular linear combinations of 5 hi ’s, we are back
to the Sn -invariant flow (7.10), while when we relax this condition, we get an Sn -breaking
RG flow. In this setup we can do renormalization and see how these couplings evolve when
we approach the IR fixed point. These computations are carried out in appendix B, and
they give a concrete illustration and a confirmation of the picture developed above.

8

Classification of leaders

As the first step of the program set in section 7, let us classify the Z2 -even Sn singlet
leader operators. Of course, the total number of leaders is infinite. We will carry out a
detailed classification for leaders up to scaling dimension 12 in d = 6, and we will make

– 31 –

JHEP03(2021)219

The reader may find somewhat puzzling the feature of the above discussion that followers
completely “go for the ride”. In other words, we are not supposed to consider followers as
individual perturbations of the L0 fixed point. Let us give a few more explanations concerning this fact. We are studying stability of the L0 fixed point in the IR, by adding to it
infinitesimal Sn singlet perturbations and seeing if they grow or decay. In this setup, perturbing the L0 fixed point by a follower alone would not be consistent: the follower always
accompanies a leader, whose coefficient is enhanced by the RG flow with respect to that of
the follower. That is why the correct procedure is to perturb infinitesimally by the leader,
while the follower perturbation then is “doubly infinitesimal” in IR, and can be neglected.
But what if we nevertheless perturb the L0 fixed point by a follower alone and compute
the anomalous dimension of such a perturbation? What would be the physical meaning of
such a computation? The answer is instructive. In addition to Sn singlet perturbations, the
L0 + L1 RG flow possesses perturbations breaking Sn invariance. Were we to perturb the
L0 fixed point by a follower alone, we would be computing dimensions of such Sn -breaking
perturbations. These perturbations are not important for the problem of Sn -invariant RG
stability studied in this paper, but they do exist.
To convince ourselves in the reality of Sn -breaking perturbations, we found useful the
following toy model. Consider the Sn -invariant RG flow with initial conditions corresponding to the quadratic part of the L0 Lagrangian perturbed by 5 quartic singlets without
derivatives from eq. (5.10):

## PDF page 35

8.1

General remarks

We are interested in classifying the scalar leader operators up to classical dimension ∆max =
12 in d = 6. A general singlet operator is constructed, in the replicated basis, as a product
O = Ak 1 . . . A k p ,

(8.1)

where each Ak is either σk or one of its dressings by derivatives, eq. (5.8). The classical
scaling dimension of the leader will be
∆(OL ) = Nφ + 2p + Nder ,

(8.2)

where Nφ = k1 + . . . + kp is the total power of φ in O (an even number for the considered
Z2 -even fields), and Nder is the total number of derivatives (also even, since indices are
contracted to get a scalar). The Nφ + 2p in (8.2) is obtained when we replace in each Aki
one φ by ω and the rest by ϕ, as in the first term in eq. (5.14). Linear combinations of
operators (8.1) may have leaders of higher dimensions than (8.2) if the leading terms cancel.
So we need to consider all possible products (8.1) such that Nφ + 2p + Nder ⩽ ∆max ,
do the Cardy transform, and separate the leaders. Let us show how this works for the
case Nφ = 4, Nder = 0. The basis of singlets is given in eq. (5.10). Performing the Cardy
transform we find:
[

σ4 = 4ωϕ3 + 6χ2i ϕ2

]

+ ...,

∆=6
2 2
2
σ1 σ3 = [3ϕ ω + 3ϕωχi ]∆=8 + . . . ,
σ22 = [4ϕ2 ω 2 + 4ϕωχ2i + (χ2i )2 ]∆=8 ,
σ12 σ2 = [2ϕω 3 + ω 2 χ2i ]∆=10 ,
σ14 = [ω 4 ]∆=12 .

(8.3)

)2

′ 2
Here are below we will continue to omit ′ : χki ≡ ′ χki , (χ2i )2 ≡
χi , etc.
Recall that the operators involving χi ’s only in O(n − 2) symmetric combinations, like
2
χi , are called susy-writable. Their correlators can be computed in the SUSY theory LSUSY
replacing χ bilinears by ψ bilinears: χ2i → 2ψ ψ̄, etc. The full rules are given in appendix C.
We will use the name “susy-writable” only for O(n−2) invariant operators which do not
vanish upon the SUSY substitution of χ’s by ψ’s. Operators which do vanish, because of the

∑

– 32 –

∑

(∑

JHEP03(2021)219

some comments about operators of arbitrarily high dimensions. This will be sufficient for
our goal of understanding the loss of stability of the L0 fixed point.
We will pay close attention to symmetries. Symmetries control mixing of operators
under RG evolution, importantly for the next section where we compute anomalous dimensions. We know that the L0 fixed point has Parisi-Sourlas supersymmetry upon replacing
χ bilinears by ψ bilinears. Some leaders (the susy-writable ones) can thus be located inside
SUSY multiplets. Their anomalous dimensions can then be determined easily, by reusing
known Wilson-Fisher results. This method is not available for leaders which are not susywritable, whose anomalous dimensions will be computed independently starting from the
L0 Lagrangian.

## PDF page 36

Singlet

Leader(+1st follower if susy-null)

Leader type

σ4

[

4ωϕ3 + 6ϕχ2i ∆=6
[3ϕ2 ω 2 + 3ϕωχ2i ]∆=8
[(χ2i )2 ]∆=8 − 43 [ωχ3i ]∆=9

susy-writable

[2ϕω 3 + ω 2 χ2i ]∆=10

susy-writable

[ω 4 ]

susy-writable

σ1 σ3
1
4
2
6 F 4 = σ2 − 3 σ1 σ3
σ12 σ2

σ14

]

∆=12

susy-writable
susy-null

Table 1. Leaders with Nφ = 4, Nder = 0.

4
1
4
σ22 − σ1 σ3 = F4 = [(χ2i )2 ]∆=8 − [ωχ3i ]∆=9 + . . . ,
3
6
3

(8.4)

where we also exhibited the non-susy-writable follower, coming from σ1 σ3 . Interestingly,
this special linear combination turns out proportional to the Feldman operator F4 , see
eqs. (5.11), (5.17).
This completes classification of leaders with Nφ = 4, Nder = 0 (see table 1). We stress
that the leader type (susy-writable, non-susy-writable or susy-null) is determined based on
the expression for the leader, not for the followers.
The described procedure can be analogously carried out for any Nφ and Nder (see
appendix D). When classifying leaders containing derivatives, we separate total derivatives
since those do not affect RG stability, and also do not mix with other operators of the
same classical dimensions. We will next highlight conceptual aspects of this classification,
separately for each leader type.
8.2

Non-susy-writable leaders

We start with the non-susy-writable leaders. These operators break the accidental O(n−2)
symmetry of the L0 Lagrangian to the Sn−1 symmetry permuting the χi fields.33
One might think that non-susy-writable leaders should be more numerous than susywritable ones because of their smaller symmetry. However this turns out not to be true.
The point is that while there are many non-susy-writable operators, most of them end
up being followers rather than leaders. We have seen this already in eq. (5.5), where
33

Note the subgroup relation Sn−1 ⊂ O(n − 2), familiar for integer n. E.g. S4 ⊂ O(3) acts by permuting
the vertices of the tetrahedron centered at the origin of R3 .

– 33 –

JHEP03(2021)219

Grassmann nature of the ψ and ψ̄, will be called “susy-null”. The simplest example is (χ2i )2 ,
which maps to (2ψ ψ̄)2 ≡ 0. Although one might think that susy-null operators do not have
any physical effect, this is not quite true because they may have non-null followers (see section 8.4 below). The susy-null operators will not mix with susy-writable nor with non-susywritable operators under RG, which is another reason to put them into a separate category.
Now, in (8.3), σ1 σ3 and σ22 have the same susy-writable part of their leader, up to a
constant factor We thus can perform a linear transformation to exhibit a singlet with a
purely susy-null leader:

## PDF page 37

ϕχ3i , χ4i and ωχ3i are all followers. Systematic enumeration (appendix D) finds only one
non-susy-writable leader up to ∆ = 12, which comes from the Feldman operator F6 :
(

−

1
F6
20

)

3
= (χ3i )2 − (χ2i )(χ4i )
.
2
L
∆=12
[

]

(8.5)

At higher ∆, non-susy-writable leaders could be constructed e.g. from the singlets
n
∑

(φi − φj )6 P (φi , φj ),

(8.6)

i,j=1

8.3

Susy-writable leaders

Looking at table 1 and appendix D, we see that most leaders up to ∆ ⩽ 12 are susywritable. It would be somewhat tedious to have to compute the anomalous dimensions
of all these operators. Fortunately this turns out unnecessary because general arguments
(section 9.1) will establish that most of them are guaranteed to be irrelevant. But before
we come to that, let us have a general discussion of this class of operators.
We will refer to susy-writable leaders transformed to SUSY fields as “susy-written”.
Consider first the following question: what distinguishes susy-written leaders from all other
operators of the SUSY theory? As one may expect, this has a neat answer based on
symmetry, which is as follows: The susy-written leaders correspond to supertranslationinvariant Sp(2)-invariant operators. In other words, supertranslations (3.2) and Sp(2)
take the role of Sn in fixing linear combinations corresponding to leaders.
Let’s explain how this comes about. The Sp(2) invariance acting on ψ, ψ̄ is manifest in
the rule (C.4). As an example of supertranslation invariance, consider susy-writable leaders
in table 1. Transforming to SUSY fields we get ϕ3 ω + 3ϕ2 ψ ψ̄, ϕ2 ω 2 + 2ϕωψ ψ̄, ϕω 3 + ω 2 ψ ψ̄,
ω 4 . Indeed these are all invariant under δϕ = −εψ̄, δψ = εω, δ ψ̄ = δω = 0, and only for
these relative coefficients. More generally, susy-writable leaders appear from terms in the
first line of eq. (5.14), and it is easy to check that these become supertranslation-invariant
upon passing to SUSY fields. This statement remains true also in presence of derivatives.
It would be interesting to give a formal general proof, although we have tested this property
so extensively that we are absolutely sure in its validity.
As any LSUSY operator, any susy-written leader can be expressed in terms of superfield
Φ given in (2.28) and its (super)derivatives. E.g.
ϕ3 ω + 3ϕ2 ψ ψ̄ = Φ3 Φ,θθ̄ + 3Φ2 Φ,θ̄ Φ,θ |θ=θ̄=0 .

(8.7)

Let us think in terms of superprimaries, i.e. composite operators O built out of the superfield Φ which transform simply under the (super)conformal symmetry of the SUSY fixed

– 34 –

JHEP03(2021)219

with P (φi , φj ) an arbitrary polynomial. In particular, for P (φi , φj ) = (φi − φj )k−6 these
would be the higher Feldman operators Fk whose non-susy-writable leaders are given in
eq. (5.17). Still more non-susy-writable leaders can be obtained by dressing singlets (8.6)
with derivatives, or multiplying them by other singlets. We will not attempt here a full
classification.

## PDF page 38

point [1]. Superprimaries have well-defined anomalous dimensions at the SUSY fixed point,
equal to those of primaries in the Wilson-Fisher fixed point in dˆ = d − 2 dimensions [1].
Identifying susy-written leaders with components of superprimaries, we will easily determine their anomalous dimensions. A general superprimary is expanded in components as
([1], eq. (3.20))
(a)

(a)

(a)

(a)

O(a) (x, θ, θ̄) = O0 (x) + θOθ (x) + θ̄Oθ̄ (x) + θθ̄Oθθ̄ (x),

(8.8)

Sθθ̄ ,

Bθθθ̄θ̄,θθ̄ .

Jθθθ̄θ̄ ,

(8.9)

Let us now discuss superrotations (3.3). For a leader Υ = Oθθ̄ where O is a scalar superprimary, superrotation transformation generalizes that of ω in (3.4):
δΥ = −εµθ ∂ µ Oθ̄ − εµθ̄ ∂ µ Oθ .

(8.10)

This only produces total derivatives, and so dd x Υ will be preserving superrotations
(and thus full SUSY). On the other hand, leaders Υ built out of SO(d) × Sp(2)-invariant
(a)
components Oθθ̄ of a tensor superprimary (like J ab or B ab,cd ) will superrotate to other
∫
components (in addition to the total derivative terms). For such leaders, dd x Υ will
break superrotations (and thus not preserve full SUSY).
Coming back to the problem of identifying susy-written leaders with superprimary
components, we can go through the list of superprimaries, and see what the corresponding
leaders are. We are to classify superprimaries of the Gaussian part of LSUSY , making use
of the SUSY equation of motion D2 Φ = 0.
∫

34

E.g. T µµ ∝ T θθ̄ for spin two representation and does not have to be considered separately.

– 35 –

JHEP03(2021)219

where (a) is a collection of OSp(d|2) indices if superprimary transforms in a nontrivial repre(a)
sentation. Leaders Υ will be found in the component Oθθ̄ ≡ Dθ̄ Dθ O(a) which is supertranslation invariant and has scaling dimension ∆O + 2. The indices (a), if present, have to be
(a)
contracted to get a scalar leader. So we will have Υ = t(a) Oθθ̄ where t(a) is an SO(d)×Sp(2)
invariant tensor, or simply Υ = Oθθ̄ if O is a scalar superprimary. Total derivative leaders
would correspond to x-derivatives of superprimary components; they do not affect RG flow.
In general, O(a) will transform under OSp(d|2) as a traceless tensor with mixed graded
symmetry represented by a Young tableau [1]. Because of the tracelessness condition, the
SO(d)×Sp(2) invariant tensor t(a) above can be chosen as a product of εpq ’s where p, q ∈ θ, θ̄
run over the Grassmann directions.34 In other words, all indices (a) will be pairwise
assigned to θθ̄. Since graded symmetry means antisymmetry for Grassmann directions,
we may conclude that the only Young tableaux giving rise to nonzero Sp(2) invariant
components are those of shape (2, 2, . . . , 2) (i.e. 2 boxes in each row). This observation is
very important, as it radically reduces the number of representations we need to examine.
The representations with more than 2 rows do not occur below dimension 12, and we will
not discuss them except for a few comments below.
(a)
In summary, all needed susy-written scalar leaders are the highest components Oθθ̄
of superprimaries in the scalar S, spin-two J ab , or box B ab,cd representations of OSp(d|2),
where the graded symmetric pairs of indices (ab) and (cd) have to be set to θθ̄, namely:

## PDF page 39

In the sector with two superfields, the lowest two superprimaries are Φ2 and the super
stress tensor T ab ,see eq. (C.4) of [1]. Superconservation fixes the dimension of T ab at d − 2
for any d, while anomalous dimensions of Φ2 will be the same as for the Wilson-Fisher
operator φ̂2 . The supertranslation invariant components are (H = 2),
(Φ2 )θθ̄ = 2ϕω + 2ψ ψ̄,
Tθµµ
= 2Tθθθ̄θ̄ = −∂ϕ∂ω − ∂ψ∂ ψ̄ + 4ω 2 .
θ̄

(8.11)

∂ 2 (Φ2 )θθ̄ = 4(∂ϕ∂ω + ∂ψ∂ ψ̄ − ω 2 ),

(8.12)

where one uses the Gaussian EOM ∂ 2 ϕ = −2ω, ∂ 2 (ω, ψ, ψ̄) = 0.
Higher spin l ⩾ 4 superprimaries built out of two superfields, e.g. the spin-4 J abcd , are
graded symmetric-traceless tensors. They have Young tableaux with l boxes in one row.
As discussed above, such Young tableau do not give rise to supertranslation- and Sp(2)invariant scalars, as the corresponding components vanish by graded-symmetric tracelessness (too many θ’s, e.g. J θθ̄θθ̄ = 0).
Let us carry out a similar exercise in the sector with four superfields. Two lowdimension superprimaries are Φ4 and Φ2 T ab of 6d scaling dimension 4 and 6 respectively.
They give rise to supertranslation invariant components of dimension 6 and 8:
(Φ4 )θθ̄ = 4ϕ3 ω + 12ϕ2 ψ ψ̄,
(Φ2 T µµ )θθ̄ = 6ϕ2 ω 2 + 12ϕωψ ψ̄

(8.13)

−ϕ ∂ψ∂ ψ̄ − 2ϕ∂ϕ(∂ψ ψ̄ + ψ∂ ψ̄) − (∂ϕ) ψ ψ̄ − ϕω(∂ϕ) − ϕ ∂ϕ∂ω.
2

2

2

2

The first one is the SUSY quartic interaction. The second one is recognized as a linear combination of the dimension 8 leaders (σ1 σ3 )L = 3ϕ2 ω 2 + 3ϕωχ2i and (σ4(µ)(µ) )L =
(∂χi )2 ϕ2 + . . . (see tables 1, 6). Another linear combination corresponds to ∂ 2 (Φ4 )θθ̄ .
To extend this story to higher ∆, it is useful to take into account that Parisi-Sourlas
superprimaries in 6 dimensions are in correspondence with the free massless scalar primaries
in 4 dimensions. The latter can be counted using conformal characters [32].35 This gives
the number of primaries and their spin for each dimension. Denoting 4d primaries as ∆j1 ,j2
where ∆ is the scaling dimension and j1 , j2 ∈ Z/2 label the SO(4) representation,36 up to
35

For systematic applications to Wilson-Fisher see [33] and [34], appendix A. Note that this method only
determines the number of primaries of each spin for every dimension. To find their explicit expressions
in terms of the fundamental field one would have to use other techniques, such as directly imposing the
primary condition [Kµ , O(0)] = 0.
36
Here j1 and j2 are the quantum numbers that label the two SU(2) in SO(4) = SU(2)×SU(2). Representations (j1 , j2 ) can be simply related to Young tableaux (l1 , l2 ), i.e. l1 boxes in the first row and l2 boxes in
the second row. E.g. spin l representations are obtained by setting j1 = j2 = l/2. More generically, mixed
symmetric Young tableaux (l1 , l2 ) are related to representations (j1 , j2 ) ⊕ (j2 , j1 ) where j1 = (l1 + l2 )/2 and
j2 = (l1 − l2 )/2.

– 36 –

JHEP03(2021)219

The first one is the SUSY mass term, while the second is a particular linear combinations of
∂ϕ∂ω+∂ψ∂ ψ̄ and ω 2 . Another linear combination with a well-defined anomalous dimension
sits in the total derivative

## PDF page 40

∆ = 10 we find the following counting:37
4 fields : 40,0 , 61,1 , 73/2,3/2 ,
2 × 82,2 , 82,0⊕0,2 , 81,1 , 80,0 ,

(8.14)

95/2,5/2 , 95/2,3/2⊕3/2,5/2 , 95/2,1/2⊕1/2,5/2 , 93/2,1/2⊕1/2,3/2 ,
3 × 103,3 , 103,2⊕2,3 , 2 × 103,1⊕1,3 , 2 × 102,2 , 102,1⊕1,2 , 2 × 101,1 , 100,0 ,
6 fields : 60,0 , 81,1 , 93/2,3/2 , 2 × 102,2 , 102,0⊕0,2 , 101,1 , 100,0 ,
8 fields : 80,0 , 101,1 .

8.4

Susy-null leaders

Susy-null operators are closely related to susy-writable operators. Like susy-writable operators, susy-null operators are O(n − 2) invariant and can be mapped to the ψ-formulation
using the map described in appendix C. The special feature of these operators compared
to susy-writables is that in the ψ-formulation they exactly vanish. The simplest instance
of this class of operator is (χ2i )2 mapped to (ψ ψ̄)2 which clearly vanishes because of anticommutation of ψ.
These operators are evidently null in the susy theory, namely any correlation function
i
of a susy-null operator Onull with any other operator OSUSY
will vanish:
⟨

⟩

1
k
Onull OSUSY
. . . OSUSY
= 0.

(8.15)

i
The property above of course holds also when OSUSY
is itself a susy-null operator, in
particular the 2-point function Onull must vanish,

⟨Onull Onull ⟩ = 0.

(8.16)

One may be tempted to discard these operators, however this conclusion is too quick.
Indeed in the L0 theory we can also consider non-susy-writable operators for which the
vanishing condition does not hold,
⟨

⟩

1
k
Onull Onon-susy
. . . Onon-susy
̸= 0.
(a)

37

(8.17)

We go up to ∆ = 10 because the leader will sit in the Oθθ̄ component and have dimension 2 higher,
and we are classifying leaders up to ∆ = 12.

– 37 –

JHEP03(2021)219

The only representations from this list giving rise to SO(d) × Sp(2) invariant components
in 6d (which are not total derivatives) are scalars (j1 , j2 = 0), rank-2 tensors (j1 , j2 =
1, 1) and mixed-symmetry 4-index tensor corresponding to the (2, 2) “box” Young tableau
(j1 , j2 = 2, 0 ⊕ 0, 2). Mixed symmetry tensors of shape (2, 2, . . .) with more than two rows
are not realized in 4d, although they may exist in 6d. 6d tensors with such symmetry
are examples of representations which project to zero under dimensional reduction [1] in
physical dimension. However when we go to d = 4 − ε dimensions, such representations
reappear as “evanescent operators” [35, 36]. It is possible to study evanescent operators
in the ε-expansion [36], but since their classical dimension is rather high (the lowest scalar
evanescent has dimension 15 in 4d), we will not consider them in this work as already
mentioned above. We will however consider the “box” tensors in full seriousness.

## PDF page 41

susy-null ↔ susy-null
susy-writable → susy-writable,
non-susy-writable → non-susy-writable,

susy-null
susy-writable,

(8.18)
susy-null.

More formally this block-triangular structure holds for the matrix Z relating the bare and
renormalized operators, see eq. (F.11). This in particular implies that renormalized susywritable and non-susy-writable operators with a well-defined anomalous dimension may
contain a susy-null piece. On the other hand, all renormalized susy-null operators will
always stay susy-null.
Now that the definition of susy-null operators is set, let us comment on which are
the possible susy-null leaders with dimensions up to 12 in d = 6. Systematic enumeration
in appendix D produced a few instances of susy-null leaders. The first one is the unique
susy-null operator at dimensions 8: this is the Feldman F4 leader which can be written as
(χ2i )2 . Another susy-null leader is found at dimension 10: ϕ2 (χ2i )2 . At dimension 12 there
are three susy-null leaders built out of 6 fields, which can mix among themselves ϕω(χ2i )2 ,
(χ2i )3 , ∂µ ϕ∂ µ ϕ(χ2i )2 . Finally, also at dimension 12, there is a unique susy-null leader built
of 8 fields ϕ4 (χ2i )2 . In the next section we will go though this list and compute all their
anomalous dimensions.
8.5

Fixed point destabilization

An Sn -singlet perturbation can destabilize the IR fixed point, when its leader becomes
relevant. This criterion is obvious for the susy-writable and non-susy-writable leaders.
The same criterion applies also for the susy-null leaders. Note that the susy-null operators
by themselves do not affect the correlation functions of all operators in the susy-writable
sector. However when the coefficient of a susy-null leader grows and becomes O(1) (as
it may happen when such a leader is relevant), it will enter and modify RG evolution
equations of other perturbations. E.g., non-susy-writable leaders which were irrelevant,
may become relevant in presence of such large susy-null perturbations.
There is a small loophole, because in principle it may happen that the offending susynull coupling flows to a nearby fixed point and never becomes O(1). Whether this happens

– 38 –

JHEP03(2021)219

A simple instance of this is the 5-point function ⟨(χ2i )2 χi1 χi2 χi3 χi4 ⟩ ̸= 0, as one can easily
verify in free theory by Wick contractions. In this sense susy-null operators are physical
operators of the L0 theory.
Because of its special structure, this class of operators satisfies very strict selection
rules for mixing under RG. Namely, susy-null operators can only mix with other susy-null
operators. Indeed, as the susy-writable operators, they cannot mix with non-susy-writables
since the latter are invariant under a smaller symmetry group: Sn−1 symmetry instead of
the accidental O(n − 2). Also they cannot acquire admixtures of susy-writable operators
(which are not null). This must be the case, otherwise we would find that a null operator in
the SUSY theory (which should be set to zero) would mix non-trivially with a non-vanishing
operator. Notice however that the mixing can occur in the opposite direction: non-susy
writable and susy-writable operators can acquire admixtures of susy-nulls. Schematically,
we have the following triangular mixing:

## PDF page 42

of not, depends on the higher-order terms in the beta-function, and on the sign of the
initial value of the RG evolving susy-null coupling. If such a fixed point does occur, SUSY
observables will be unaffected.38 This possibility looks somewhat exotic. In this paper we
will be conservative, and will count relevant susy-null leaders as potentially destabilizing
perturbations.39

9

Anomalous dimensions

38
While the SUSY observables are unaffected, it may be possible to see a presence of a susy-null coupling in more complicated correlation functions involving non-susy-writable operators. E.g. the correlation
function ⟨χ2 (x1 )χ2 (x2 )χ2 (x3 )χ2 (x4 )⟩ would be affected if the leaders (χ2i )2 or ϕ2 (χ2i )2 become relevant.
This correlation can be mapped to the replica variables and back to the random field formulation as follows
1
(namely we substitute χ2 = φ2 − n−1
(φ3 +. . .+φn ), expand the correlator for generic n, translate replicated
correlators to the random field correlators using (2.8), and finally take the limit n → 0 for the coefficients),

⟨χ2 (x1 )χ2 (x2 )χ2 (x3 )χ2 (x4 )⟩ = 14⟨φ(x1 )φ(x2 )φ(x3 )φ(x4 )⟩
−10(⟨φ(x1 )φ(x2 )⟩⟨φ(x3 )φ(x4 )⟩ + 2 perms)
−14(⟨φ(x3 )⟩⟨φ(x1 )φ(x2 )φ(x4 )⟩ + 3 perms)

(8.19)

+24(⟨φ(x1 )φ(x2 )⟩⟨φ(x3 )⟩⟨φ(x4 )⟩ + 5 perms)
−72⟨φ(x1 )⟩⟨φ(x2 )⟩⟨φ(x3 )⟩⟨φ(x4 )⟩.
It may be possible to consider the r.h.s. in a simulation and see if it deviates from the result of the l.h.s.
predicted by using L0 . If so, one can check if the correct result is obtained by perturbing L0 with a relevant
susy-null operator. Admittedly, this is more a question of principle than a concretely realizable proposal,
since simulating 4-point functions is a very hard task. In any case a deviation in (8.19) from the L0 prediction
does not count as a violation of SUSY, since this observable was not protected by SUSY in the first place.
39
In the preliminary report given in [10], as well as in the earlier version of the paper, we used a different
criterion for when a susy-null leader destabilizes the fixed point, which required looking at the first follower,
and requiring that follower be relevant. For this to happen, the susy-null leader dimension has to be below
d − 1. We now think that conclusion, based on a linearized analysis, was not correct.

– 39 –

JHEP03(2021)219

In the previous section we classified the leaders of Z2 -even Sn singlets up to 6d scaling
dimension 12. We will now discuss their anomalous dimensions. Some anomalous dimensions will be computed at two loops, and some at one loop. We will consider separately the
three classes of leaders (susy-null, susy-writable, and non-susy-writable). We will identify
in each class at least one perturbation which becomes less irrelevant as d is lowered. The
next section will discuss the critical dimension dc where these candidate perturbations may
cross the relevance threshold.
We will start in section 9.1 with the susy-writable leaders, the most numerous class.
Their anomalous dimensions can be determined, as discussed above, by writing them as
components of supermultiplets whose dimensions are known from dimensional reduction to
Wilson-Fisher theory. This strategy is not available for the susy-null and non-susy-writable
leaders, whose anomalous dimensions have to be computed from scratch (sections 9.2, 9.3).
As we explained in sections 7, the anomalous dimension computation is greatly simplified by the fact that close to the IR fixed point all follower operators can be dropped. We
are therefore led to consider the anomalous dimensions of leader operators in the theory
defined by the Gaussian L0 Lagrangian perturbed by the interaction 4ωϕ3 + 6χ2i ϕ2 , at its
IR fixed point in d = 6 − ε dimensions. We use dimensional regularization.

## PDF page 43

Consistency of our method to compute anomalous dimensions by restricting to the
leader operators requires that leaders and followers do not mix. For susy-writable leaders
this is guaranteed explicitly by their supertranslation invariance when transformed to the
SUSY fields (section 8.3). From the point of view of the L0 Lagrangian the absence of
leader-follower mixing may appear puzzling, since these operators may have the same
classical dimensions and the same number of fields. However, our extensive checks confirm
the absence of this mixing in all cases we looked at. It would be interesting to find a formal
proof, based on selection rules following from Sn invariance, and for all three classes of
leaders (see section 11.1.1).
Susy-writable leaders

The general remarks in section 8.3 give many handles on the susy-writable leaders. We will
now discuss their IR scaling dimension. We have one low-dimension susy-writable leader:
the SUSY mass term (Φ2 )θθ̄ = 2ϕω +2ψ ψ̄. This operator is relevant in any d, its anomalous
dimension being the same as for the Wilson-Fisher operator φ̂2 in dˆ = d − 2 dimensions.
The coefficient of this operator is finetuned to reach the SUSY fixed point.40
Are there any other susy-writable Z2 -even leaders which are relevant? As we explained,
apart from total x-derivatives, susy-writable leaders Υ, when transformed to the SUSY
(a)
fields, are SO(d) × Sp(2) invariant components Oθθ̄ of superprimaries O(a) . Their scaling
dimension are thus
∆Υ = ∆O + 2 = ∆Ô + 2,
(9.1)
where we used that the scaling dimension of O equals that of the Wilson-Fisher primary
Ô to which O projects under dimensional reduction [1] (see also appendix H.1 for a few
one-loop examples). We have seen above the example Ô = φ̂2 for O = Φ2 . By eq. (9.1), Υ
is relevant d dimensions if and only if Ô is relevant in dˆ dimensions:
∆Υ < d

⇐⇒

∆Ô < dˆ = d − 2.

(9.2)

In addition, as mentioned in section 8.3, we are interested in operators Ô which are either
scalars, spin-2 tensors, or 2 × 2 “box” Young tableau mixed symmetry tensors, since otherwise O will not have SO(d) × Sp(2) invariant components.41 Let us then discuss what
is known about the spectrum of such Z2 -even operators at the Wilson-Fisher (WF) fixed
point.
For any dˆ the WF fixed point has one Z2 -even relevant scalar, φ̂2 , connected to the
relevant SUSY mass term by the above argument. All other Z2 -even scalars are irrelevant,
which corresponds to the fact that the Ising phase transition is reached by tuning one Z2
even parameter (temperature).
40

For a non-finetuned coefficient the RG flow with SUSY initial conditions would end up in a SUSY
massive phase. The L0 + L1 flow is then also expected to end up in a massive phase, which however is not
going to be equivalent to the SUSY one, because of the residual L1 effects, which will not have time to
decay completely to zero.
41
As mentioned in section 8.3, Young tableau of shape (2, 2, . . .) could also be important but we will neglect
them since they have high classical dimension. They are harder to study since they project to zero in 4d.

– 40 –

JHEP03(2021)219

9.1

## PDF page 44

which unfortunately does not guarantee irrelevance (even modulo caveats about the lack of
unitarity in non-integer d). So we have to enter into the details. The lowest box tensor is
82,0⊕0,2 in 4d (see eq. (8.14)). This operator has 4 fields and 4 derivatives and an expression
in terms of fields of the form43
(
2

φ̂,µν φ̂,ρσ φ̂ −

2dˆ
dˆ − 2

)Y

φ̂,µ φ̂,ν φ̂,ρσ φ̂

,

(9.4)

where ()Y means that we should apply the box Young symmetrizer and subtract traces.
The IR scaling dimension of this operator in dˆ = 4 − ε is given by
∆B̂ = (8 − 2ε)class +

(

7
11
ε
+ O(ε2 ) = 8 − ε + O(ε2 ),
9 1-loop
9
)

(9.5)

where the one-loop correction is from [38], table 4 (line “(2,0),(0,2)”, n = 4). Unfortunately
we are not aware of a two-loop computation.
So by eq. (9.1), the dimension of the leader B in d = 6−ε is two units higher than (9.5):
∆B = 10 −

11
ε + O(ε2 ).
9

(9.6)

In appendix H.1 we write the form of the box operator in Cardy variables, and perform
an independent computation of its one-loop anomalous dimension. This agrees with the
Wilson-Fisher computation, providing a further interesting check of dimensional reduction.
By eq. (9.6), the leader B is becoming less irrelevant as the dimension is lowered, but
only very slowly so. So in section 10 it will not be our prime candidate to destabilize the
SUSY fixed point.
42

Put {hi } = (2, 2, 0, . . .) in eq. (2.41) in [37]. This also agrees with [37], (2.45) using “box”= (2, 0)⊕(0, 2)
in 4d.
43
The relative coefficient between the two terms can be found by imposing the primary condition
[Kµ , O(0)] = 0, or by requiring zero two-point functions with the lower primaries φ̂2 and φ̂2 T̂µν .

– 41 –

JHEP03(2021)219

ˆ
In the spin-2 sector the lowest operator is the stress tensor, of dimension exactly d.
All other spin-2 operators are irrelevant in 4d and expected to stay irrelevant in dˆ < 4,
by two arguments. First, we have the unitarity bound ∆ ⩾ dˆ for any spin-2 primary in a
unitary CFT. This argument is rigorous for integer dˆ but it has a caveat for intermediate
ˆ In fact, the Wilson-Fisher theory in dˆ = 4 − ε is known to be not quite unitary because
d.
of the evanescent operators [35, 36] mentioned in section 8.3. However the violations of
unitarity appear secluded at high dimension where all evanescent operators belong, and
the unitarity bound for low-lying operators seems safe even in non-integer dimensions.
The second argument does not rely on unitarity but on the observation that to pass from
irrelevant to relevant a spin-2 operator would have to cross the stress tensor, and level
crossing is believed unlikely in an interacting non-integrable theory.
Finally, let us discuss the “box” tensors. The unitarity bound for these tensors is
relatively weak:42
∆box ⩾ dˆ − 1,
(9.3)

## PDF page 45

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

p3

−

p3

− l1

− p4

<latexit

sha1_base64="sgpTBjHYkjJ1azsvbNX5p0U6zx4=">AAAB83icbZDLSgMxFIbP1Futt6pLN8EiuGmZsQVdFt24rGAv0A5DJs20oZlMSDJCGfoablwo4taXcefbmLaz0NYfDnz85xxy8oeSM21c99spbGxube8Ud0t7+weHR+Xjk45OUkVomyQ8Ub0Qa8qZoG3DDKc9qSiOQ0674eRu3u8+UaVZIh7NVFI/xiPBIkawsdagKoO6rUaVB15Qrrg1dyG0Dl4OFcjVCspfg2FC0pgKQzjWuu+50vgZVoYRTmelQaqpxGSCR7RvUeCYaj9b3DxDF9YZoihRtoRBC/f3RoZjradxaCdjbMZ6tTc3/+v1UxPd+BkTMjVUkOVDUcqRSdA8ADRkihLDpxYwUczeisgYK0yMjalkQ/BWv7wOnauaZ/mhUWne5nEU4QzO4RI8uIYm3EML2kBAwjO8wpuTOi/Ou/OxHC04+c4p/JHz+QM0oJB6</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p2

l2
<latexit sha1_base64="YTO6seXZu7zHYbj3se5C6PKcvho=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz3IQW1QrrhVdyGyDl4OFcjVHJS/+sOYpRFXyCQ1pue5CfoZ1SiY5LNSPzU8oWxCR7xnUdGIGz9brDojF9YZkjDW9ikkC/f3REYjY6ZRYDsjimOzWpub/9V6KYbXfiZUkiJXbPlRmEqCMZnfTYZCc4ZyaoEyLeyuhI2ppgxtOiUbgrd68jq0a1XP8v1VpXGTx1GEMziHS/CgDg24gya0gMEInuEV3hzpvDjvzseyteDkM6fwR87nD/rfjZU=</latexit>

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

p4

l 1 + l 2 − p1
<latexit sha1_base64="7BDZylbDh/Yl/Ghlqh3BPI9pFvI=">AAAB8nicbZDLSgMxFIYz9VbrrerSTbAIglhmiqDLohuXFewFpsOQSTNtaCYZkjNCGfoYblwo4tancefbmLaz0NYfAh//OYec80ep4AZc99spra1vbG6Vtys7u3v7B9XDo45RmaasTZVQuhcRwwSXrA0cBOulmpEkEqwbje9m9e4T04Yr+QiTlAUJGUoec0rAWr4IvQsRNi7T0AurNbfuzoVXwSughgq1wupXf6BoljAJVBBjfM9NIciJBk4Fm1b6mWEpoWMyZL5FSRJmgny+8hSfWWeAY6Xtk4Dn7u+JnCTGTJLIdiYERma5NjP/q/kZxDdBzmWaAZN08VGcCQwKz+7HA64ZBTGxQKjmdldMR0QTCjalig3BWz55FTqNumf54arWvC3iKKMTdIrOkYeuURPdoxZqI4oUekav6M0B58V5dz4WrSWnmDlGf+R8/gC58JA5</latexit>

l1
<latexit sha1_base64="berNMFBEL75BVbf5uEM+UZJp20k=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9SD6ft+tejVvLrIKfgFVKNTou1+9QcKyGKVhgmrd9b3UBDlVhjOB00ov05hSNqZD7FqUNEYd5PNVp+TMOgMSJco+acjc/T2R01jrSRzazpiakV6uzcz/at3MRNdBzmWaGZRs8VGUCWISMrubDLhCZsTEAmWK210JG1FFmbHpVGwI/vLJq9C6qPmW7y+r9ZsijjKcwCmcgw9XUIc7aEATGAzhGV7hzRHOi/PufCxaS04xcwx/5Hz+APlbjZQ=</latexit>

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

p1

9.2

Susy-null leaders

Here we will summarize computations of anomalous dimensions of susy-null leaders (see
appendix H.2 for details).
The susy-null operator with the smallest UV dimension is (χ2i )2 . It is the leader operator of the singlet combination σ3 σ1 + 34 σ22 , which is also the Feldman operator F4 , see
eq. (8.4). Its anomalous dimension receives no one-loop contribution, while the two-loop
correction is given by the diagram in figure 4. Using standard techniques (appendix H.2.1)
we obtain the IR scaling dimension
∆(χ2 )2 = 8 − 2ε −
i

8 2
ε + O(ε3 ).
27

(9.7)

Going higher in the UV dimension, we encounter the susy-null leader ϕ2 (χ2i )2 with classical
dimension 10 − 3ε. Since it is the only susy-null leader at this dimension, it does not mix
with any other operator. It receives a positive one-loop anomalous dimension equal to 3ε,
as discussed in appendix H.2.2. We have not evaluated its two-loop anomalous dimension.
At classical dimension 12 − 3ε, we have three susy-null leaders made of six fields,
which mix with one another in a nontrivial way: ϕω(χ2i )2 , (χ2i )3 and (∂µ ϕ)2 (χ2i )2 . In
appendix H.2.3 we compute their anomalous dimension matrix at one loop. As explained
there, the matrix is not completely diagonalizable, rather it can be brought to the Jordan
form (see also appendix F) with eigenvalues 0 and (11/9)ε, the latter associated to a ranktwo Jordan block. In the CFT context, the Jordan block structure of the mixing matrix
signals the presence of a logarithmic multiplet, and is a symptom that we are dealing with
a logarithmic CFT [39]. This fact is not very surprising since our theory arises from the
n → 0 limit of Sn -symmetric replica Lagrangian (see [40]).
At classical dimension 12 − 4ε there is a single composite of eight fields, ϕ4 (χ2i )2 .
This also receives a positive one-loop anomalous dimension equal to (22/3)ε, as shown in
appendix H.2.4.
We summarize these results in table 2. As discussed in section 8.5, we count relevant
susy-null leaders as possible sources of the SUSY fixed point destabilization. The leader

– 42 –

JHEP03(2021)219

Figure 4. Two-loop correction to the correlator ⟨(χ2i )2 (p = 0)χj (p1 )χk (p2 )χl (p3 )χm (p4 )⟩. The
black dot indicates the bare composite operator (χ2 )2 . We also see two ϕ2 χ2 vertices. The conventions for the propagators are explained in appendix E.

## PDF page 46

Leaders Onull
(χ2i )2
ϕ2 (χ2i )2
ϕω(χ2i )2
(χ2i )3
∂µ ϕ∂ µ ϕ(χ2i )2
ϕ4 (χ2i )2

Full Sn -singlet perturbation O

IR dimension: ∆Onull

σ3 σ1 + 34 σ22
σ2 σ4 − 85 σ1 σ5
σ1 σ2 σ3 − 32 σ12 σ4
σ23 − 2σ1 σ2 σ3 + σ12 σ4
2
σ3(µ)
− 43 σ2(µ) σ4(µ) + 13 σ1(µ) σ5(µ)
σ2 σ6 − 12
7 σ1 σ7

8 2
8 − 2ε − 27
ε + O(ε3 )

10 + O(ε2 )
⎫
⎬ 12 − 3ε + O (ε2 )
( 2)
16
⎭

12 − 9 ε + O ε

2
12 + 10
3 ε+O ε

( )

(χ2i )2 has the smallest dimension and is one candidate which may cause such a destabilization, once it becomes relevant (see section 10).
9.3

Non-susy-writable leaders

In section 8.2, we have identified only one non-susy writable leader up to ∆ = 12 in
d = 6. It is the leader (F6 )L of the Feldman operator F6 . Given its expression (8.5)
in Cardy fields, its anomalous dimension is studied via the 6-point correlation function
⟨(F6 )L (p)χi (p1 )χj (p2 )χk (p3 )χl (p4 )χm (p5 )χn (p6 )⟩. Its leading anomalous dimension appears at two loops, from the first diagram in figure 15 (see appendix H.3 for details),
and it is negative. The two-loop corrected dimension IR dimension of (F6 )L is given by:
7
∆(F6 )L = 12 − 3ε − ε2 + O(ε3 ).
9

(9.8)

This leader is becoming less irrelevant as d gets smaller, and is another candidate which
might destabilize the SUSY RG flow, as we discuss in section 10.
In appendix H.3 we also considered anomalous dimensions of higher Feldman leaders
(Fk )L , finding at two loops
k
k(3k − 4) 2
∆(Fk )L = 2k − ε −
ε + O(ε3 ).
2
108

(9.9)

This confirms the original result of Feldman [29]. It should be noted that ref. [29] used
the “old” formalism for computing anomalous dimensions, working in the replicated basis
with propagator (2.10). The agreement shows that the “old” formalism is not wrong, if
one is careful. We believe however that our new formalism (working in the Cardy basis
in the vicinity of the Gaussian fixed point, distinguishing leaders and followers, classifying
leaders by their symmetry) is more systematic, hence less error prone.
While we confirm Feldman’s result (9.9) for the anomalous dimension, we disagree
with his conclusion that this implies instability of the SUSY fixed point for an arbitrary
small ε; see section 10.

– 43 –

JHEP03(2021)219

Table 2. Summary of anomalous dimension computations for all susy-null leaders with ∆UV ⩽
12 + O (ε). For the leaders ϕω(χ2i )2 , ϕω(χ2i )2 and ∂µ ϕ∂ µ ϕ(χ2i )2 we show the two scaling dimensions
arising after mixing (the second one being associated to a rank-two logarithmic multiplet).

## PDF page 47

12

10

8

6

4

0
3.5

4.0

4.5

5.0

5.5

6.0

Figure 5. Scaling dimensions of the three lowest leaders (one per each class) as a function of the
space dimension d, per eqs. (10.1).

10

Scenarios for the loss of SUSY

In the previous sections we carried out the program of classifying the leaders of Sn singlet
perturbations, and we described many anomalous dimension computations. This is a vast
body of knowledge about the spectrum of potentially destabilizing perturbations. On the
basis of this information we will now discuss possible scenarios for how SUSY may be lost
below a critical dimension dc .
The lowest leaders in each of the three classes have dimensions (9.6), (9.7), (9.8). In
this section we will use them truncated to the known terms:
susy-writable:

∆B = 10 −

11
ε,
9

8 2
ε ,
i
27
7
non-susy-writable: ∆(F6 )L = 12 − 3ε − ε2 .
9
susy-null:

∆(χ2 )2 = 8 − 2ε −

(10.1)

In figure 5 we plot these scaling dimensions as a function of d in the range of interest
3 ⩽ d ⩽ 6. In the same plot we show the marginality threshold line ∆ = d.
The immediate observation is that B does not become relevant in this range of d, while
(F6 )L and (χ2i )2 do so at:
∆(χ2 )2 = d

at

d ≈ 4.6,

∆(F6 )L = d

at

d ≈ 4.2.

i

Taking this at face value, SUSY may be lost between d = 4 and 5 because of these two
perturbations.

– 44 –

JHEP03(2021)219

2

## PDF page 48

∆B′ = (12 − 3ε)class +

(

10
ε
ε
+ O(ε2 ) = 12 + + O(ε2 ).
3 1-loop
3
)

(10.2)

At O(ε) the scaling dimension curves do not intersect, and we do not consider this case
any further.
44

We thank Édouard Brézin and Nicolas Sourlas for suggesting a Padé check.
The one-loop correction is from [38], table 4 (line “(2,0),(0,2)”, n = 6). The number in the table needs
to be multipled by ε/3.
45

– 45 –

JHEP03(2021)219

The first uncertainty in this result is due to the shortness of available perturbative
series, which hopefully will be improved in the future by higher-loop computations. E.g.,
using instead a Padé[1,1] rational approximant for the conformal dimensions, we find that
∆(χ2 )2 crosses marginality at d ≈ 4.7, while ∆(F6 )L at d ≈ 4.5. This provides a rough idea
i
of this uncertainty.44
Another uncertainty is associated with the fact that the coupling of the susy-null (χ2i )2 ,
even if relevant, may flow to a nearby fixed point (“small loophole” from section 8.5), in
which case SUSY may be preserved. But even if this happens, we still have the non-susywritable leader (F6 )L , which will destroy SUSY at a nearby dimension.
Additional uncertainty may be due to the nonperturbative mixing with higherdimension operators, as we will now discuss.
By nonperturbative mixing we mean the following phenomenon. In perturbation theory, mixing happens between operators of the same symmetry, with additional selection
rules that they should have the same number of fields and the same scaling dimension in
d = 6. Beyond perturbation theory, symmetry remains the only selection rule. Let then
∆1 (d) and ∆2 (d) be dimensions of two operators computed in perturbation theory, and
suppose these two curves intersect at some d < 6 (“level crossing”). If these two operators
have different symmetry, e.g. belong to different leader classes like in figure 5, then the
level crossing is allowed also beyond perturbation theory. On the other hand, if the two
operators have the same symmetry, then we should not believe the level crossing literally,
as it will be modified by nonperturbative mixing effects.
Normally, level crossing will be resolved via level repulsion (figure 6, center). Our
theory being non-unitary, level crossing may also be resolved via operator dimensions
becoming complex conjugate (figure 6, right). Which of the two resolutions is realized
depends on the sign of the norm of the crossing operators (which is the same as the sign
of their two-point functions). Operators whose norm has the same sign will repel (as is
always the case in unitary theories), while for the norm of opposite sign, dimension will go
into the complex plane. If the mixing operators have zero norm, as in the susy-null case,
both options are possible.
After these general comments, let us see which of the curves in figure 5 can be affected
by nonperturbative mixing.
The susy-writable leader B could in principle mix nonperturbatively with other susywritable leaders coming from the box representations, the first of which is the 102,0⊕0,2 in
eq. (8.14). The scaling dimension of the corresponding leader B ′ is:45

## PDF page 49

}}]

12
10
8
6
4
2
0
3.5

4.0

4.5

5.0

5.5

6.0

Figure 7. Scaling dimensions of susy-null leaders from table 2 (known terms).

The susy-null leader (χ2i )2 could in principle mix nonperturbatively with other susynull leaders shown in table 2. We plot the perturbative predictions for their scaling dimensions (to known order) in figure 7. We see that while the higher curves intersect among
themselves, they do not reach the lower (χ2i )2 curve.
Finally, the non-susy-writable sector (F6 )L may mix nonperturbatively with any of the
higher non-susy-writable leaders. We know a part of this higher spectrum, namely the twoloop dimensions of the higher Feldman operators, eq. (9.9). In figure 8 we plot the scaling dimension of the first four (Fk )L . This time we do see level crossings. In fact, since the 2-loop
correction is negative and grows with k, it looks like the dimensions of (Fk )L intersect the
dimensions of all lower (Fk′ )L . At least for the first few Feldman operators, these crossings
all appear to happen slightly above d = 4, close to the point where (F6 )L becomes relevant.
This multitude of crossings deserves a discussion. The nonperturbative mixing will
likely repel the Feldman operators. As a result the lower Feldman operator will become

– 46 –

JHEP03(2021)219

Figure 6. Left: level crossing for two operator dimensions ∆1 (d), ∆2 (d) of the same symmetry in
perturbation theory. Center: crossing resolved via level repulsion (for norm of the same sign). Right:
crossing resolved via going to the complex
norm of the opposite sign). These plots were
( plane (for )
∆1 (d) p
obtained by diagonalizing the matrix
, where p is a parameter characterizing the
p ∆2 (d)
nonperturbative mixing strength, taken real or purely imaginary for norms of equal/opposite sign.

## PDF page 50

20

15

Out[324]=

10

5

4.0

4.5

5.0

5.5

6.0

<latexit sha1_base64="sM6CIA74KB1Ft2zdHjFMjIDIYak=">AAACmHicbVHbTtwwEPWmFOhSrn1rX6KuVuJplQDi8raCSrRvC+ouSJsITZwJGGwnsh3QKs0/8Nr+GX/TOLtCezuSpeMzZzwznijjTBvPe2s4H1Y+rq6tf2pufN7c2t7Z3RvoNFcU+zTlqbqNQCNnEvuGGY63mUIQEceb6OnCxm+eUWmWyt9mlGEo4F6yhFEwlTQIfiA3cLfT8jpeDXeR+BPSIhP07nYbf4I4pblAaSgHrYe+l5mwAGUY5Vg2g1xjBvQJ7nFYUQkCdVjU7ZZuu1JiN0lVdaRxa3U6owCh9UhElVOAedDzMSsujcXaPrgsNMxNchoWTGa5QUnHPSQ5d03q2m9xY6aQGj6qCFDFqjFc+gAKqKk+r9meroI5BV7Oarag0oku53u1DVlV4gtNhQAZF0HEcyyHflgUQT17UQstv5zzKYxnbPZeu+p9nVkcv29nkQwOOv5h5/DqqNU9n2xunXwj38k+8ckJ6ZKfpEf6hJJH8kr+kn/OV6frXDq/xlanMcn5QmbgXP8HkcvP+g==</latexit>

∆

Figure 8. Perturbative scaling dimensions of the leaders of the first four Feldman operators.

d
<latexit sha1_base64="C5dnsXnvtWPFCy3/SWxuCQVhIro=">AAACk3icbVFbS8MwFM7qbc7bpvjkS3EIPo3WiRd8GeqDL8IEd4GtSJqealiSliRVRu0v8FV/nP/Gpg7Z5j4IfPnOd3LOyfFjRpV2nO+StbS8srpWXq9sbG5t71Rru10VJZJAh0Qskn0fK2BUQEdTzaAfS8DcZ9DzRzcm3nsFqWgkHvU4Bo/jZ0FDSrDOpYfgqVp3Gk4B+z9xJ6SOJmg/1UrvwyAiCQehCcNKDVwn1l6KpaaEQVYZJgpiTEb4GQY5FZiD8tKi08w+ypXADiOZH6HtQp3OSDFXasz93MmxflHzMSMujAXKPLgoNEh0eOGlVMSJBkF+ewgTZuvINj9iB1QC0WycE0wkzcewyQuWmOj83ypH01UgIZhls5opKFWosvleTUNGFfBGIs6xCNKhzxLIBq6XpsNi9rQQ6m4255MQzNjMvXAV+7o0OPvbzn/SPWm4zUbz4bTeup5srowO0CE6Ri46Ry10h9qogwgC9IE+0Ze1b11Z19btr9UqTXL20Ays+x+zzM3m</latexit>

Figure 9. Schematic dimension curves for Feldman operators after taking nonperturbative mixing
into account. In making this figure we assumed the simplest scenario that all Feldman operators
have the norm of the same sign and hence repel each other rather than go into the complex plane.
It would be interesting to verify the norm sign in the future. For this one would have to determine
the eigenperturbations and compute the sign of the two-point functions. This plot also does not
take into account that there exist other non-susy-writable operators, with which higher Feldman
operators are expected to mix beyond two-loop order, see section H.3.

relevant at a slightly higher dc than without taking mixing into account, while the higher
Feldman operators will become relevant at a slightly lower d, if at all. SUSY will be valid for
d > dc . The final picture may perhaps resemble that of figure 9. This deserves further study,
but we emphasize that any future discussion of this problem should take nonperturbative
mixing into account. It should also be remembered that Feldman operators are but a small
subset of all the non-susy-writable operators which can be expected to take part in this
mixing, see section H.3.

– 47 –

JHEP03(2021)219

0
3.5

## PDF page 51

11

Discussion

In this paper we laid out a comprehensive framework to study RG stability of the ParisiSourlas supersymmetric fixed point describing the phase transition in the Random Field
Ising Model. The key ingredients of our approach are:
• We used the Cardy-transformed basis of fields ϕ, ω, χi , in which the RG flow looks
manifestly as a Gaussian fixed point perturbed by a weakly-relevant interaction near
the upper critical dimension 6.
• We decomposed Sn -invariant perturbations (in the Cardy basis) into the leaders
and followers. Scaling dimension of the leader then determines whether the whole
perturbation is relevant.
• We classified the leaders into three classes by their symmetry (susy-writable, susynull, and non-susy-writable).
46

See e.g. [41] for a recent related discussion of anomalous dimensions of composite operators made of
many fields in the Wilson-Fisher 4 − ε expansion. In this regard it is also instructive to recall that in the
2 + ε expansion for the O(N ) vector model, operators with a large number of gradients s acquire negative
anomalous dimensions at one [42] and two loops [43, 44]. If one takes these terms too literally, infinitely
many such operators (namely all operators with s ≫ N/ε) seem to become relevant, contrary to the usual
expectation that the Wilson-Fisher fixed point should have exactly one relevant O(N )-singlet direction for
any 2 < d < 4. The general conclusion seems to be that this paradox is due to applying 2 + ε expansion
results outside of their regime of validity [45–47].

– 48 –

JHEP03(2021)219

Finally we would like to discuss what would happen if one naively extrapolated figure 8
to extremely high k. The two-loop result eq. (9.9) would seem to predict that (Fk )L
√
becomes relevant for εc ∼ 72/k which goes to zero for k → ∞. This was the argument
advanced by Feldman [29], who thus concluded that arbitrarily close to d = 6 there will
be some sufficiently high (Fk )L which is already relevant. Hence, he argued, SUSY will be
not present at any d < 6. We do not trust this argument for two reasons. First, because
it ignores nonperturbative mixing discussed above. Second, because to have εc small we
would have to consider very large k indeed. E.g. for k = 50 we still have εc = 1.01 from
the two-loop result. On the other hand the coefficients of the perturbative series grow with
k, as already visible in (9.9). Therefore the two-loop prediction at very large k will be
trustworthy only in a tiny range of ε, and cannot by itself be used to find where (Fk )L
becomes relevant and if this happens at all.46 For these reasons, we do not think it likely
that infinitely many Feldman operators will cross or approach the relevance threshold.
To summarize, our computations suggest that Parisi-Sourlas SUSY will be lost below
a critical dimension dc ≈ 4.2 - 4.7. Around this dimension, SUSY-breaking perturbations
from two different symmetry sectors (susy-null and non-susy-writable leaders) become relevant. In particular, for integer dimension 5 all perturbations are irrelevant and ParisiSourlas SUSY is expected to be present. For integer dimension 4, one perturbation with a
susy-null leader and at least one non-susy-writable perturbations are relevant, and the RG
flow is directed away from the SUSY fixed point. The phase transition in the 4d RFIM is
therefore not expected to be supersymmetric.

## PDF page 52

• Susy-writable leaders were additionally classified as belonging to superprimary multiplets transforming in particular OSp(d|2) representations.
• We enumerated all leaders up to 6d dimension ∆ = 12, and computed their perturbative anomalous dimensions (at one or two loops).

1. SUSY fixed point exists for any 3 < d ⩽ 6.
2. SUSY fixed point is stable for d > dc and unstable for d < dc , where dc ≈ 4.2 - 4.7.
Our scenario is therefore different from the loss of SUSY in any d < 6 advocated for various
reasons in some works such as [27, 29, 48, 49].47 It is also different from the disappearance
of the SUSY fixed point via fixed point annihilation, found in Functional Renormalization
Group (FRG) studies [22, 50–53] at dc ≈ 5.1 (see appendix A.7). For them, SUSY is absent
for d < dc because there is no longer any SUSY fixed point, while for us the SUSY fixed
point exists for any d, it just becomes unstable for d < dc . [The value of dc is also different
but this is less important.] We do not see any signs of fixed point annihilation in our
picture. For us, this would require that a SUSY-preserving operator crosses the relevance
threshold. In the language of section 9.1, this would be a scalar Z2 -even susy-writable
leader, and as discussed there all such operators remain irrelevant for all d.
Our work suggests two kinds of open problems: to explore our method further, and to
check our conclusions with other techniques. We discuss these in turn.
11.1
11.1.1

Exploring our method further
Symmetry meaning of leaders in the Cardy basis

One aspect of our construction which deserves further thinking is the symmetry understanding of leaders. Leaders were introduced as the lowest-dimension components of Sn -singlet
operators. We then argued (and checked extensively) that leaders only mix with leaders under RG. If so there must be a symmetry reason for this fact contained in the L0 Lagrangian
47

See appendix A.11 concerning [48, 49], appendix A.9 concerning [27], and section 10 concerning [29].

– 49 –

JHEP03(2021)219

On the basis of the above, we identified two Sn -invariant perturbations which become
relevant at a critical dimension dc slightly above 4. In the replicated field basis φi , these
∑
perturbations correspond to F4 and F6 , where Fk = ni,j=1 (φi − φj )k is the series of
operators considered long ago by Feldman [29]. Although looking similar in the replicated
basis, in our picture the two perturbations belong to two different classes: F4 has a susy-null
leader (χ2i )2 , while F6 has a non-susy-writable leader.
The above conclusions were based on perturbative calculations of anomalous dimensions around 6d, and on considering the lowest leaders in each class. In the non-susywritable class, perturbative calculations indicate level crossing between F6 and the higher
Feldman operators Fk , k > 6. We discussed how this level crossing is expected to be resolved by nonperturbative mixing effects, pushing slightly up the critical dimension dc at
which F6 will become relevant.
To summarize, the main features of our scenario for the loss of SUSY are:

## PDF page 53

(without appealing to the original Sn invariant Lagrangian), and it would be interesting to
identify such a reason. For susy-writable leaders we gave a criterion (section 8.3) that they
become supertranslation invariant when written in the SUSY field basis, and it would be
interesting to prove this more rigorously.

But can we understand this vanishing of correlators directly in terms of leaders, without
appealing to Sn -singlets from which the leaders originated? For susy-writable leaders we
can, since they are the highest component of a supermultiplet, so, by supersymmetry, their
correlation function must be zero (this is the same arguments that predicts ⟨ω(x)ω(0)⟩ = 0).
Also correlation functions of susy-null leaders must vanish, since the operator are null
(similarly this happens for mixed correlation functions of susy-null operators and susywritable ones). A less trivial case is when non-susy-writable leaders are inserted in the
correlation function. In this case SUSY arguments don’t apply, and one has to find a new
strategy to prove the statement.

11.1.2

Higher-loop computations

Perturbative computations of anomalous dimensions played an important role in our considerations. In this work we relied on one- and two-loop predictions. In comparison, 6or 7-loop results are available nowadays for the leading critical exponents in the WilsonFisher 4 − ε expansion [54, 55]. It would be interesting to compute higher loop anomalous
dimensions of composite operators responsible for destabilizing the SUSY fixed point. Resumming these series could lead to improved determinations of dc .
48

This argument works unless we consider Sn -singlets rescaled by powers of n. In this paper we do not con∑n
sider such rescaled operators since they would diverge in the n → 0 limit. One may argue that e.g. i=1 φki
is also vanishing for n → 0, and thus that dividing by n is an allowed operation. However in Cardy variables
∑n k
φ is non-vanishing and for this reason in this formalism the rescaled operators are not allowed.
i=1 i

– 50 –

JHEP03(2021)219

Another hint for such a symmetry may come from an interesting property which all
leader operators have: their correlation functions vanish. One easy argument for this
comes from considering correlation functions of Sn -singlets written in terms of the original
replicated fields φi (namely without writing them in Cardy basis). It is indeed easy to
prove that such correlation functions are proportional to n and thus vanish in the n → 0
limit. [This is related to the fact that the partition function of replicated theory is exactly
1 in the n → 0 limit.] As an example let us consider ⟨σk1 . . . σkm ⟩ in the free replicated
theory (namely (2.7) with V = 0). The result of this correlator can be written as a product
of propagators (2.10), thus it is proportional to the trace of a product of the matrices 1
and M of (2.10). Since tr(1 · · · 1M · · · M) = O(na ) with a ⩾ 1, the result must vanish as
n → 0. This argument generalizes straightforwardly for more generic Sn singlets48 and it is
also easy to see that when V ̸= 0, at any order in perturbation theory, the same property
must hold, since the potential is also an Sn -singlet by construction. We thus conclude that
correlation functions of Sn -singlets vanish. Since the leaders are lowest dimensional pieces
of Sn -singlets, their correlators must vanish too.

## PDF page 54

11.1.3

Branched polymers and the Lee-Yang universality class

11.2
11.2.1

Checking our conclusions with other techniques
Numerical simulations

A feature of our scenario is that the Parisi-Sourlas SUSY fixed point exists in any d > 3
(although it becomes unstable for d < dc ). In principle, this could be tested in numerical
lattice simulations. State-of-the-art simulations study the RFIM phase transition at zero
temperature, by tuning the disorder distribution. In practice one considers a one-parameter
family of distributions with a fixed shape and varying overall strength (i.e. dispersion).
E.g. ref. [7] did this in d = 4 for the Gaussian and Poisson disorders. In both cases they
found identical, non-SUSY, critical exponents (as reviewed in appendix A.2). If the SUSY
fixed point exists in d = 4, it should be possible to observe it by tuning within a family
of disorder distributions depending on a larger number of parameters (as many as there
are relevant perturbations at the SUSY fixed point). As discussed in section 10, it looks
like at least two more perturbations in addition to the SUSY mass become relevant in
d = 4 (F4 and F6 ). If that is the case, one would have to consider a 3-parameter family
of distributions to find a SUSY fixed point in a lattice simulation — a daunting task. But
perhaps the higher-loop terms slightly modify the behavior of anomalous dimensions on d,
and only one extra perturbation becomes relevant in d = 4, so that a 2-parameter family
would suffice. See appendix I for a schematic discussion of this possibility.
Another question is whether one can measure some of the observables considered in this
paper through a lattice simulation, e.g. in d = 5, where the SUSY fixed point is expected
to be reached. In particular it would be interesting to compute the scaling dimensions of
the leaders of the Sn -singlet operators F4 and F6 and check that these are indeed irrelevant
in d = 5. Let us explain how this can be done. Any correlation function of any operator in
Cardy variables can be mapped to a correlator of the random field theory by first rewriting it in terms of the replicated fields φi following eqs. (2.11), (2.14) and then by using
the recipe in eqs. (2.6), (2.8). An example of such computation is done in (2.32)–(2.34)
and (8.19), but it can be easily generalized to any kind of operator, in particular to the
49

As discussed in appendix A.4, there is also a rigorous proof for dimensional reduction of branched
polymers [56]. Done for a model of branched polymers preserving SUSY at the microscopic level, that proof
does not shed light on the stability of the SUSY fixed point with respect to SUSY-breaking perturbations.

– 51 –

JHEP03(2021)219

One can consider the same problem as we studied in this paper, but replacing the quartic
potential φ4 with the imaginary cubic potential iφ3 [18]. As mentioned in section 1 and
reviewed in appendix A.4, this “Random Field Lee-Yang Model”, with upper critical dimension 8, describes the phase transition in the system of random polymers. Dimensional
reduction from d to d−2 dimensions in this case is verified to high precision by Monte Carlo
simulations.49 Therefore, we do not expect to find instability phenomena that we found
here for the RFIM case. In other words, leader anomalous dimensions in the iφ3 theory
should be such that they will not cross the relevance threshold. It would be very interesting
to verify this explicitly. Note that both Z2 invariant and Z2 breaking leaders should be
considered in this computation, since Z2 is not a symmetry of the Lee-Yang model.

## PDF page 55

11.2.2

Conformal bootstrap

In recent years, the conformal bootstrap has emerged as a powerful method to study
nonperturbative CFTs in any dimension (see the review [57]). Most of its successes have
been for unitary CFTs, which can be analyzed rigorously due to the unitarity bounds for
the operator dimensions and reality constraints on the OPE coefficients, as was first shown
in [58]. These rigorous methods do not directly apply to the Parisi-Sourlas SUSY fixed
point which is non-unitary, as visible e.g. in ∆ϕ below the scalar unitarity bound, and in
the violation of spin-statistics by spinless fermions.
Scaling dimensions of susy-writable leaders could be obtained by looking at the corresponding primaries in the Wilson-Fisher fixed point in dˆ = d − 2 dimensions. This is
complicated by the fact that in integer d some interesting representations project to zero,
while for non-integer d the Wilson-Fisher theory is also non-unitary [36] (as already mentioned in section 9.1). For us, the most interesting susy-writable leader is the box operator
B, whose dimension equals that of the Wilson-Fisher box primary B̂. The number of comˆ irrep dimension) of B̂ is given by (see eq. (H.4)) dim(B̂) = (d+2)(d+1)d(d−3) .
ponents (O(d)
12
We have dim(B̂) = 10 for dˆ = 4 consistently with box=(2, 0) ⊕ (0, 2) in that dimension.
Note that dim(B̂) vanishes for dˆ = 3, which means that B̂ does not exist in 3d, i.e. B
projects to zero under dimensional reduction from d = 5 to 3. For 3 < dˆ < 4, dim(B̂)
is positive. Perhaps in this range of dˆ some trustworthy, albeit non-rigorous, information
about the scaling dimension of B̂ can be provided by the standard numerical bootstrap
(applying it e.g. to the 4-point functions of spin-one operators or stress tensors). 51
Apart from the lack of positivity, there are other complications in applying the conformal bootstrap method to the RFIM. First, the fixed point of interest exists only for n = 0,
thus precluding the analytic continuation of CFT data in n (section 6). Second, the CFT
ˆ

50

ˆ

ˆˆ

E.g. O = (χ2 )2 gives a nonzero 3-point function. On the other hand O = χ2 seems to give a vanishing
3-point function because the two point function ⟨χ2 χ2 ⟩ can be expressed in the susy variables as ⟨ψ ψ̄⟩ times
a prefactor, see (2.36).
51
While being still technically challenging to set up the conformal bootstrap for such operators in arbitrary
dimensions, we might see developments in this direction in the near future. E.g. U(1) currents and stress
tensors were recently considered in d = 3 [59–61].

– 52 –

JHEP03(2021)219

leaders of F4 and F6 . It is however important to mention that correlation functions of both
Sn -singlets and of their leaders are vanishing as we explain in section 11.1.1. Hence one
cannot extract the dimension of a leader by computing its two point function, since this
would be zero. One should consider instead more complicated correlation functions involving non-singlet operators. E.g. ∆(F6 )L can be studied with the help of the 3-point function
⟨(F6 )L (x1 )ϕ(x2 )ϕ(x3 )⟩. On the other hand, the susy-null dimension ∆(F4 )L may be accessible via through a 3-point function ⟨(F4 )L (x1 )O(x2 )O(x3 )⟩, where O has to be non-singlet
and in addition non-susy-writable, otherwise the result will vanish. 50 These kind of observables would be very interesting to study. Even if higher point functions are significantly
more complicated to compute in a lattice simulation, we hope that progress can be done in
this direction. E.g. the same scaling dimensions ∆(F6 )L and ∆(F4 )L can be extracted from
finite-volume corrections to scaling of the two point functions ⟨ϕϕ⟩ and ⟨OO⟩.

## PDF page 56

11.2.3

Functional renormalization group

Previous functional renormalization group (FRG) studies of the RFIM phase transition,
such [22, 50–53] (see appendix A.7) used the Sn -symmetric formalism. In principle, it
should also be possible to apply the FRG method in the Cardy field basis. For that one
would have to package an infinite series of singlet operators in a general function. E.g.,
one could generalize Feldman operators to an Sn -invariant interaction parametrized by a
general function R:
n
∑

R(φi − φj ),

(11.1)

i,j=1

which in the Cardy basis becomes
2

n
∑
i=2

R(ω − χi ) +

n
∑

R(χi − χj ).

(11.2)

i,j=2

[Separating it into a leader plus followers may not be necessary in a nonperturbative framework such as FRG.] One could then derive an RG flow equation for the function R, leading
to the anomalous dimension predictions for the Feldman operators. Note that this RG
equation will be different from that in the FRG studies of the interface disorder (section A.6), because of the presence of the quartic coupling in our problem. Also unlike in
section A.6, the function R for us does not have to satisfy any conditions at infinity. It
would be interesting to carry out this exercise, as a way to confirm our expectations from
section 10 about the mixing and level repulsion of these operators.

Acknowledgments
We are grateful to Connor Behan, Lorenzo Di Pietro and Johan Henriksson for discussions
of nonperturbative mixing. We also thank Edouard Brézin, John Cardy, Marco Meineri,
Giorgio Parisi, Leonardo Rastelli, Aninda Sinha, Nicolas Sourlas, Gilles Tarjus and Kay
Wiese for various useful comments and discussions.
52

Its notable further investigations are [63, 64]. See [57], section IV.E for a review and more references.

– 53 –

JHEP03(2021)219

is expected to contain logarithmic multiplets (section 9.2), for which logarithmic conformal
blocks need to be used instead of the usual conformal blocks [39].
At present, the only bootstrap algorithm not relying on positivity and thus applicable
also to non-unitary CFTs is the one proposed by Gliozzi [62].52 In its present incarnation
this algorithm is not rigorous, as well as less systematic than the standard numerical
bootstrap algorithms. In spite of the lack of rigor and the above-mentioned complications,
it would be interesting to try to apply Gliozzi’s algorithm to the RFIM fixed point. This
was attempted by Hikami [65], who found support for the loss of dimensional reduction
below dc ≈ 5. As we explain in appendix A.10, more work in this direction is needed to
verify the robustness of Hikami’s results and to extract what they say about the mechanism
for the loss of dimensional reduction.

## PDF page 57

This work was partially supported by the Simons Foundation grant 488655 (Simons
Collaboration on the Nonperturbative Bootstrap) and by Mitsubishi Heavy Industries
(MHI-ENS Chair).

A
A.1

History and prior work
Early work

A.2

No SUSY and no dimensional reduction in d = 3, 4

The Parisi-Sourlas conjecture fails in d = 3: the d = 3 RFIM is ordered at low temperatures
(for weak disorder) by the Imry-Ma criterion [68], while d = 1 Ising is of course disordered at
all temperatures and does not even have a phase transition. The ordering of 3d RFIM was
also proved rigorously by Imbrie [69, 70] (T = 0) and by Bricmont and Kupiainen [71, 72]
(small T ).
The transition is believed continuous in 3d. Numerical simulations can be done at
T = 0 varying the disorder strength to reach the transition. One uses fast algorithms to
find exact ground states for a collection of disorder samples, and then performs disorder
average. In this setup, a large-scale study on cubic lattices with size up to L = 192 and
with 107 disorder samples was performed by Fytas and Martin-Mayor [6]. They found a
continuous transition with exponents ν ≈ 1.4(1), η ≈ 0.515(1). Defining different exponents
for the connected and disconnected propagators as
∂⟨Sx ⟩/∂hy ∼ 1/rd−2+η ,

⟨Sx ⟩⟨Sy ⟩ ∼ 1/rd−4+η̄

(A.1)

they find η̄ ≈ 2η. SUSY is ruled out as it would predict η̄ = η. Correction to scaling
exponent is ω = 0.52(11).
The d = 4 RFIM and d = 2 Ising both have a phase transition but exponents do not
agree. The d = 4 RFIM exponents were measured precisely in [7], with results ν ≈ 0.872(6),
η ≈ 0.1930(13), 2η − η̄ ≈ 0.032(2), ω ≈ 1.3(1). In particular η̄ ̸= η and SUSY is ruled out.

– 54 –

JHEP03(2021)219

That critical exponents of random-field φ4 theory in d = 6 − ε agree with Wilson-Fisher
in d = 4 − ε was first proved by Aharony, Imry and Ma in 1976 [66] (see also Young [67]).
They picked out a subclass of perturbative diagrams most divergent in IR, and showed
them identical to those of the Wilson-Fisher theory with coupling λ′ = λH, for (d − 2)dimensional external momenta.
Parisi and Sourlas [5] rephrased this calculation in terms of supersymmetry. The diagrams in question being tree-level in φ (before integrating over the random field), their sum
can be done by solving the classical equation of motion in external field h. This can be then
neatly interpreted as a path integral with insertion δ(−∆φ + V ′ (φ) − h) det(−∆ + V ′′ (φ)).
Introducing a Lagrange multiplier field ω for the δ-function and a pair of anticommuting
scalars to represent the determinant, one lands on a supersymmetric action. Dimensional
reduction is then argued in perturbation theory using superpropagators and the identity
∫ d−2
∫
d x F (Yi x, x2 ) = dd xdθdθ̄ F (Yi x, x2 + θ̄θ) where Yi are d−2 dimensional vectors. The
position space argument is thus easier than the momentum space one.

## PDF page 58

A.3

SUSY in d = 5?

The d = 5 RFIM study [8] found ν = 0.626(18), η = 0.055(15), 2η − η̄ = 0.058(8),
ω = 0.66(15). Within error bars, this is largely consistent with both SUSY η̄ = η and
with the 3d Ising exponents (ν = 0.629971(4), η = 0.036298(2), ω = 0.82966(9) from the
conformal bootstrap [73, 74]).

A.4

Branched polymers and the Lee-Yang universality class

Another interesting case of dimensional reduction occurs for the statistics of branched
polymers which can be modeled as connected clusters of N points on a lattice (“lattice animals”). Their number P (N ) and average size R scales as P (N ) ∼ N −θ λN , R ∼ N ν where
θ, ν are critical exponents and λ is a lattice-dependent non-universal constant. Lubensky
and Isaacson [75] proposed a field-theoretic description for extracting these exponents from
a scalar theory in n → 0 limit, similar to de Gennes’s description of self-avoiding walks
but with extra cubic vertices breaking O(n) symmetry to Sn . Parisi and Sourlas [76] then
interpreted this as the replica method limit for the random field model (1.4) with the cubic
potential V (φ) = m2 φ2 + igφ3 . Via supersymmetry, critical exponents should be the same
as for the Lee-Yang universality class in d − 2 dimensions. The lattice animals exponents
are known from precise Monte Carlo simulations [77] for all d < duc = 8 and indeed they
agree with the Lee-Yang exponents (known exactly or approximately depending on d).
Brydges and Imbrie [56] found a model of branched polymers which has manifest supersymmetry at the microscopic level (see also review [78]). In their model branched polymers
∏
2 )∏
2
are represented as a gas of particles in d dimensions with weight i∼j Q(rij
i≁j P (rij )
where Q keeps neighboring nodes at a distance r ∼ a apart, while P repels all other nodes.
Supersymmetry is present if Q(x) = dP (x)/dx. In this case, the model can be written
as a classical gas of particles in Rd|2 interacting with repulsive potential V , e−V = P .
Dimensional reduction follows, to a classical repulsive gas in Rd−2 . The latter model has
a critical point at negative fugacity which is one of two famous microscopic realizations
of the Lee-Yang universality class [79, 80] (the other being the Ising model in imaginary
magnetic field [81]). Brydges and Imbrie’s result is limited to their model of polymers and
to the finetuned case of Q = P ′ . It does not explain why supersymmetry should emerge in
a generic model of branched polymers (i.e. why supersymmetry breaking deformations are
irrelevant). This explanation may come from repeating the analysis of our paper for the
cubic potential (see section 11.1.3).

– 55 –

JHEP03(2021)219

Further evidence for SUSY and dimensional reduction in 5d RFIM was presented
in [9], which simulated elongated hypercube geometries with d − 2 dimensions fixed at L
and 2 remaining ones at RL. For R → ∞ and L fixed, SUSY imposes relations between
connected and disconnected propagators, and these relations were found to be satisfied in
d = 5 (working at R = 5). E.g. three independent finite-volume correlation lengths (which
scale with L) were found equal at a percent level: for the connected and disconnected
propagators in 5d RFIM and for the 3d Ising.

## PDF page 59

A.5

Zero-temperature fixed points

– 56 –

JHEP03(2021)219

Long-distance behavior of disordered systems is often described in terms of “zerotemperature fixed points”. Some features of these fixed points appeared to us rather unusual, and we will attempt here a review for non-expert audience, according to our own
incomplete understanding. We found particularly useful the original references [82, 83],
and section 8.5 of [30].
To set the notation, recall that the usual “fixed point” is a system with an action
S({φ}, {λ}) depending on a collection of fields {φ} and couplings {λ}, which remains invariant under an RG transformation corresponding to the RG change of scale x′ = bx, b > 1,
in the sense that all couplings are invariant: {λ′ } = {λ}. To exhibit this invariance one may
have to reparametrize the fields after performing RG transformation (e.g. rescale them).
One of the RG invariant couplings may be taken to be temperature itself. E.g., the fixed
point describing the ferromagnetic phase transition in the usual, non-disordered Ising model
has a fixed nearest-neighbor coupling J which can be identified also with the inverse temperature, as well as infinitely many other couplings corresponding to the next-to-nearest and
other possible Z2 invariant couplings, which may be neglected in an approximate treatment.
In the same notation, by a “zero-temperature fixed point” one means a system whose
action is written with an explicit T −1 factor, T1 S({φ}, {λ}), and whose behavior under
RG amounts to the change T ′ = b−θ T with θ > 0 a critical exponent, while all the other
couplings {λ} remain invariant. So T → 0 as one iterates RG. Two well-known examples
are the low-temperature fixed points describing the ordered phase of the Ising model, as
well as of the O(N ) model with N > 2, d ⩾ 3. Both of these cases lead to simple long-range
behavior (gapped for Ising, Gaussian with massless Goldstones for O(N )).
What is unusual is that disordered phase transition are often described by nonGaussian
zero-temperature fixed points.
[
] RFIM is one example. Rewriting the Hamil∑
∑
tonian (1.1) as T1 − ⟨ij⟩ si sj + i hi si , h2i = ∆2 , the d > 2 phase diagram in the space
(T, ∆) is shown in figure 10. It contains the usual non-disordered fixed point at T = Tc
which is unstable under arbitrarily small disorder (Harris criterion) and flows to the disordered fixed point at T = 0, ∆ = ∆c . This fixed point is a zero temperature fixed point
according to the above definition. The critical exponent θ is known to be 2 in d = 6 − ε to
all orders, while θ = 1 + ε/2 for d = 2 + ε [82].
Physically, this means that the thermal fluctuations are negligible to those due to
disorder at the phase transition. This is very useful in numerical simulations of the RFIM
phase transition as it can be done at zero temperature with ∆ = ∆c . One picks a large
ensemble of disorder representatives {hi }, for each of these one computes the ground state
∑
∑
(the configuration of spins with minimal energy − ⟨ij⟩ si sj + i hi si ). This can be done
in polynomial time with the push-relabel algorithm [84], the solution is generically unique,
and the critical slow-down is not too bad [85, 86]. These zero-temperature algorithms are
used in modern large scale numerical simulations [6–9].
Let us discuss how the zero-temperature fixed point concept is reconciled with perturbation theory in d = 6 − ε and Parisi-Sourlas SUSY ([83] and [30], section 8.5). Consider
the replicated action (2.7). Restoring the temperature dependence, the Lagrangian takes

## PDF page 60

∆
<latexit sha1_base64="sM6CIA74KB1Ft2zdHjFMjIDIYak=">AAACmHicbVHbTtwwEPWmFOhSrn1rX6KuVuJplQDi8raCSrRvC+ouSJsITZwJGGwnsh3QKs0/8Nr+GX/TOLtCezuSpeMzZzwznijjTBvPe2s4H1Y+rq6tf2pufN7c2t7Z3RvoNFcU+zTlqbqNQCNnEvuGGY63mUIQEceb6OnCxm+eUWmWyt9mlGEo4F6yhFEwlTQIfiA3cLfT8jpeDXeR+BPSIhP07nYbf4I4pblAaSgHrYe+l5mwAGUY5Vg2g1xjBvQJ7nFYUQkCdVjU7ZZuu1JiN0lVdaRxa3U6owCh9UhElVOAedDzMSsujcXaPrgsNMxNchoWTGa5QUnHPSQ5d03q2m9xY6aQGj6qCFDFqjFc+gAKqKk+r9meroI5BV7Oarag0oku53u1DVlV4gtNhQAZF0HEcyyHflgUQT17UQstv5zzKYxnbPZeu+p9nVkcv29nkQwOOv5h5/DqqNU9n2xunXwj38k+8ckJ6ZKfpEf6hJJH8kr+kn/OV6frXDq/xlanMcn5QmbgXP8HkcvP+g==</latexit>

disordered
∆c
<latexit sha1_base64="7vd0/iQTACl+95AiQn9XezPPjjo=">AAACmnicbVFNS8QwEM3W7/Vbj3ooLoKnpVXx4ybqQfGi4OrCtizTdKrBJC1Jqiy1f8Kr/jH/jU1dxF19EHh58yYzk4kyzrTxvM+GMzE5NT0zO9ecX1hcWl5ZXbvTaa4odmjKU9WNQCNnEjuGGY7dTCGIiON99HRm4/fPqDRL5a0ZZBgKeJAsYRRMJXWDc+QG+rS/0vLaXg33L/GHpEWGuO6vNl6DOKW5QGkoB617vpeZsABlGOVYNoNcYwb0CR6wV1EJAnVY1A2X7nalxG6SqupI49bq74wChNYDEVVOAeZRj8es+G8s1vbB/0K93CRHYcFklhuU9LuHJOeuSV37MW7MFFLDBxUBqlg1hksfQQE11fc1t39XwZwCL0c1W1DpRJfjvdqGrCrxhaZCgIyLIOI5lj0/LIqgnr2ohZZfjvkUxiM2e69d9b6OLQ5+tvOX3O22/b323s1+6+R0uLlZskG2yA7xySE5IRfkmnQIJZy8kXfy4Ww6p86lc/VtdRrDnHUyAuf2C4mm0NA=</latexit>

ordered

T

Figure 10. Phase diagram of the RFIM for d > 2.

2
n
H0
′
′
the form T1 ni=1 12 (∂µ φi )2 +λ0 φ4i − 2T
2 (
i=1 φi ) where h(x)h(x ) = H0 δ(x−x ). Rescaling
the fields we get the action as in (2.7) with λ = T λ0 , H = H0 /T . If we use the classical
scalar dimension in 6d, then an RG step with rescaling factor b > 1 will give λ′ = b−2 λ,
H ′ = b2 H. We see that this corresponds to λ0 , H0 being invariant, while T ′ = T /b2 , so we
flow to a zero-temperature fixed point (θ = 2).53

∑

∑

Let us next consider d < 6 and connect with the Cardy-transformed description. In
the basic scenario of section 2.4, the IR fixed point is described by the Lagrangian (2.21)
with H and the quartic λ both RG-invariant, provided that the fields f ∈ {ϕ′ , χ′i , ω ′ } are
rescaled by f ′ (x) = b∆f f (bx) where ∆χ = ∆ϕ + 1, ∆ω = ∆ϕ + 2. If on the other hand we
do the rescaling using ∆χ instead of ∆f for all three fields, the Lagrangian will retain its
form with the unit-normalized kinetic terms, but H, λ will change as H ′ = b2 H, λ′ = λ/b2 ,
which as we have seen above is equivalent to a zero-temperature fixed point. We conclude
that θ = 2 in any d < 6 where Parisi-Sourlas SUSY holds.
We thus see that the zero-temperature fixed point can manifest itself in many guises.
In lattice simulations we can just set T = 0. On the other hand, in the standard replicated
description (2.7) we are forced to keep T ̸= 0 even though it flows to zero (a coupling
which flows to zero but cannot be simply dropped is “dangerously irrelevant”, footnote 32).
Alternatively, we are forced to keep the quartic coupling λ0 in the action although it is
irrelevant and flows to zero, because it combines with another coupling H0 which flows to
infinity. Finally, in the Cardy field basis the zero-temperature fixed point looks like the
usual non-zero temperature one: nothing flows to zero or infinity provided that we use the
correct dimensions of fields in the SUSY multiplet. The latter property is of course the
chief reason why we used the Cardy basis throughout this paper.
But what if we decide, for the sake of the argument, to forego RG and set T = 0
directly in the Landau-Ginzburg description (1.4)? This would mean that we have to find,
53

Note that in the replica formalism zero-temperature fixed points are described with disorder-averaged
terms having higher order in 1/T .

– 57 –

JHEP03(2021)219

Tc
<latexit sha1_base64="ySLO5ZhRCmXvCpUP1he2HJeKuz4=">AAAClXicbVFdS8MwFM3q15xfUx988KU4Bj6NVsWPB0FUxDcVtylsZaTp7QxL0pKkyqj9Cb7qb/Pf2HRD3OaBwMm55+bem+vHjCrtON8la25+YXGpvFxZWV1b36hubrVVlEgCLRKxSD77WAGjAlqaagbPsQTMfQZP/uDKxJ9eQSoaiaYexuBx3Bc0pATrXHps9kivWnMaTgF7lrhjUkNj3Pc2S+/dICIJB6EJw0p1XCfWXoqlpoRBVukmCmJMBrgPnZwKzEF5adFrZtdzJbDDSOZHaLtQ/2akmCs15H7u5Fi/qOmYEf+NBco8+F+ok+jw1EupiBMNgox6CBNm68g2f2IHVALRbJgTTCTNx7DJC5aY6PznKvW/VSAhmGWTmikoVaiy6V5NQ0YV8EYizrEI0q7PEsg6rpem3WL2tBBqbjblkxBM2My9cBX7OjM4/t3OLGkfNNzDxuHDUe3icry5MtpFe2gfuegEXaBbdI9aiKA++kCf6Mvasc6ta+tmZLVK45xtNAHr7geEv86s</latexit>

## PDF page 61

for each random h(x), the field φh solving the classical EOM
− ∂ 2 φh + V ′ (φh ) + h = 0,

(A.2)

and having the minimal energy. This gives in fact the fastest way to “derive” Parisi-Sourlas
SUSY. We represent the resulting path integral as
∫

Dφ δ(φ − φh )P(h)Dh =

∫

Dφ P(h)Dh δ(−∂ 2 φ + V ′ (φ) + h) det(−∂ 2 + V ′′ (φ)). (A.3)

∫

DϕDωDψDψ̄P(h)Dh e

∫

ω(−∂ 2 φ+V ′ (φ)+h)+

∫

ψ(−∂ 2 +V ′′ (ϕ))ψ̄

,

(A.4)

and upon averaging over Gaussian h we land on the SUSY Lagrangian. This was in fact the
derivation used originally by Parisi and Sourlas [5] except that they argued the localization
to solutions of (A.2) based on the structure of most important terms in perturbation theory,
not on the fact that the fixed point is at zero temperature. In retrospect, their argument
proves that fixed point is at zero temperature in perturbation theory [83].
By convexity arguments, eq. (A.2) has a unique solution for any h as long as m2 ⩾ 0.
At the same time, for m2 < 0 there are multiple solutions for some h. This is discussed
in Parisi’s Les Houches 1982 lectures [48] (see also [87, 88]). The bare mass at the phase
transition is expected to be negative, and so multiple solutions are always present at the
short-distance scale. In presence of multiple solutions, Parisi-Sourlas path integral (A.4)
can be reduced to the sum over all solutions weighted by the determinant. This deviates
from what one originally wanted: just the minimal energy solution. One can try to relate
this deviation to nonperturbative effects, which may lead to exponentially small e−C/ε
deviations from dimensional reduction already in d = 6 − ε [48, 49].54 It appears that
the constant C has never been computed, which makes the reality of these corrections
somewhat nebulous. In fact, multiple solutions may be a short-distance phenomenon, their
effect renormalized away when one flows to long distances. To see whether this scenario is
realized, one may wish to study the whole RG flow leading to the zero-temperature fixed
point and see if the RG fixed point is stable (rather than set T = 0 from the start). That
is exactly what we did in the main text of the paper.
A.6

Interface disorder

Another famous occurrence of disorder is in statistical physics of interfaces (see e.g. lecture
notes by Kay Wiese [89] and by Leon Balents [90]). Some aspects of this problem are analogous to RFIM, although there are also differences because the symmetry is not the same.
An interface is a scalar function u(x), x ∈ Rd , described by an action
1
T
54

∫

1
d x (∂u)2 + V (x, u(x)) ,
2
d

[

]

We thank Giorgio Parisi for a discussion.

– 58 –

(A.5)

JHEP03(2021)219

where we reexpressed δ(φ − φh ) assuming the solution of (A.2) is unique. We can further
rewrite this as

## PDF page 62

where V is a random potential. [E.g. one may imagine the interface between two phases of
d + 1 dimensional Ising model at T < Tc , the disorder potential V coming from impurities.]
We kept T explicit in the action. The potential is taken Gaussian random with
V (x, u) = 0,

V (x, u)V (x′ , u′ ) = δ d (x − x′ )R(u − u′ ).

(A.6)

As a consequence of the shift symmetry u → u + const, the variance depends on the
difference R(u − u′ ), assumed an even function. One is interested in computing various
correlators of u(x), e.g.
(⟨u(x)⟩ − ⟨u(y)⟩)2 ∼ |x − y|2ζ
(A.7)

1 ∑1
1 ∑
(∂ui )2 −
R(ui (x) − uj (x)).
T i 2
2T 2 ij

(A.8)

Compared to the RFIM replicated Lagrangian (2.7) (with φi ↔ ui ), this Lagrangian lacks
∑
the individual potential V (ui ) which is forbidden by the shift symmetry. The term ( i ui )2
∑
∑
∑
is reproduced for the quadratic R(u), because ij (ui − uj )2 = −2 ij ui uj = −2 ( ui )2
in the n → 0 limit. For R(u) = uk , the perturbation in (A.8) is nothing but the Feldman
operator Fk which played such an important role in our paper. Applying the Cardy trans∑
form u1 = ϕ + ω/2, ui = ϕ − ω/2 + χi (i = 2, . . . , n, χi = 0) gives, in the n → 0 limit,
the Lagrangian
1
1∑
R′′ (0) 2
∂ϕ∂ω +
(∂χi )2 +
ω −
T
2
2T 2
[
]
R(4) (0) (∑ 2 )2 4 ∑ 3
−
χ
−
ω
χ
i
i + ...
8T 2
3
[

]

(A.9)

The leading Lagrangian (first line of (A.9)) is a free SUSY theory. The second line is the
(∑ 2 )2
Feldman F4 (8.4) in the Cardy basis, with a susy-null leader
χi . In our paper we had
to calculate the scaling dimension of this perturbation working in the 6 − ε expansion, but
in the interface problem the SUSY fixed point is Gaussian (because the shift symmetry
forbids the quartic interaction), and we can just read off the leader scaling dimension as
∆ = 2d − 4, which becomes relevant for d < 4. Thus, according to the discussion in
section 8.5, we expect that at d < 4 the Gaussian SUSY fixed point may be destabilized.
Furthermore, the problem at hand provides a nice illustration of how to deal with the
“small loophole” mentioned in section 8.5, namely that we have to consider the nonlinear
terms in the beta-function to see whether the susy-null coupling actually grows to become
O(1), or perhaps flows to a nearby fixed point, in which case the SUSY would not really be
( ∑ 2 )2
(4)
broken. Denoting by g = − R8T (0)
the
χi coupling, the beta-function at marginality
2
(i.e. in 4d) has the form:
βg = Cg 2 ,
(A.10)
where C is a positive order 1 constant. It turns out that the initial conditions for the RG
evolution in the interface problem are always g(ΛUV ) < 0 at the microscopic scale [89].55
55

We thank Kay Wiese for emphasizing this point to us.

– 59 –

JHEP03(2021)219

at long distances, where ζ is called the roughness exponent .
Replica method then leads to the Lagrangian:

## PDF page 63

where C̃ is an order 1 positive dimensionless coefficient (it is proportional to C in (A.10)).
Starting the RG evolution with an analytic function R(t) having a physically acceptable
behavior at infinity, as well as having R(4) (0) > 0 (which is always the case for the random
interface), one finds that the function ∆(u) = −R′′ (u) develops a cusp at u = 0, i.e. ∆(u) =
c0 + c1 |u| + . . . at small t. This cusp appears at the scale where R(4) (0) → ∞, which we
found above based on (A.10).
Once the cusp forms, one would be tempted to declare that the problem became
strongly coupled and no further analytic progress is possible. That is what happens in
perturbative QCD, where below ΛQCD , when the gauge coupling becomes strong, one has
to resort to lattice Monte Carlo simulations or descriptions in terms of an effective action
using very different degrees of freedom from those in the UV, and whose parameters cannot
be determined from the first principles.
It is somewhat surprising however, that the literature on the disordered interfaces
claims to be able to go beyond the cusp formation point (see [89]). One looks for a selfsimilar solution of the RG equation in the form
R(u) = Λ−4ζ K(Λζ u)

(A.12)
2

Note that, physically, the function R(u) must go to zero at large u. E.g. we might have R(u) ∼ e−u
at the UV cutoff scale for random-bond type of disorder in the underlying Ising model which hosts the
interface, while for random-field type disorder we have instead R′′ (u) → 0 at large u [89]. The requirement
that R(u) go to zero implies nontrivial correlations between the coefficients of its Taylor series. E.g. if we
set all expansion coefficients with k ⩾ k0 to zero, the resulting R(u) is a polynomial, growing at infinity,
which is not allowed by physical constraints.
56

– 60 –

JHEP03(2021)219

With such an initial condition and with C > 0 in (A.10), the RG evolution leads to a
blowup of the coupling g in the IR (similarly to how the QCD gauge coupling formally
blows up at ΛQCD ). We conclude that in the interface problem the “small loophole” does
( ∑ 2 )2
not realize, and once the
χi passes the marginality threshold, the Gaussian SUSY
fixed point is truly destabilized.
( ∑ 2 )2
It should be said that we do not know if the same will happen when
χi crosses
the marginality threshold in our RFIM problem, because we have not calculated the sign
of the beta-function (which may be different in our case due to quantum corrections) and
we do not know if the initial sign of the coupling will be the same in our problem as for
the interface.
Going back to the interface problem, while the SUSY fixed point instability can be
easily understood using our language, there remains the question where the flow goes. For
the interface, this question has been studied using FRG, by writing the RG equation for
the whole function R(u) [91] rather than performing the expansion as in (A.9).56
Consider the replica action (A.8) with n = 0 and some UV cutoff scale Λ. It is
convenient to rescale R = Λε R̄. Then, the one-loop RG equation for R(u) in d = 4 − ε has
the form
[
]
dR̄
1 ′′
2
′′
′′
−
= εR̄(u) + C̃ [R̄ (u)] − R̄ (u)R̄ (0) ,
(A.11)
d log Λ
2

## PDF page 64

which gives a fixed point equation for K(t)
0 = (ε − 4ζ)K(t) + ζtK(t) + C

[

1 ′′ 2
[K (t)] − K ′′ (t)K ′′ (0)
2

]

(A.13)

T → αT,

α = Λd+2ζ−2 < 1

(A.14)

So the effective temperature goes to zero at long distances, while ζ in (A.12) may be
identified with the roughening exponent, giving values in agreement with Monte Carlo
simulations.
A.7

Functional renormalization group studies of RFIM

Tarjus, Tissier and collaborators (Tarjus et al. in what follows) applied the functional
renormalization group (FRG) method to the RFIM phase transition [22, 50–53]. Here we
will attempt to review some aspects of their work in spite of the fact that we understand
it only partially, and compare to our approach.57
Tarjus et al. ([22], section 2.C) allow for unequal sources for different replicas, which
they contrast with the conventional replica approaches using, they say, equal sources. We
tend to disagree that this difference is so crucial. The usual replica formalism allows to
describe all experimentally observable correlators, see eq. (2.8). The Cardy-transformed
Lagrangian used in our work is equivalent to the usual replica Lagrangian, as long as one
does not drop any terms without due RG justification. In this paper we talked about fields
and correlators, which is of course equivalent to introducing sources and differentiating
with respect to them, although we did not find it necessary to stress this standard part of
QFT dictionary explicitly.
In the rest of this appendix we will comment on refs. [50, 92], devoted to the loss
of Parisi-Sourlas SUSY. As far as we can see, this FRG analysis is applied to an action
arrived at by not fully justified assumptions. Namely, one first derives the Parisi-Sourlas Lagrangian using the original Parisi-Sourlas argument. Then one observes that the obtained
result is wrong due to multiple solutions to the classical equation of motion. It is then proposed to fix this via an auxiliary parameter β providing a Boltzmann suppression for the extra contributions, see [92], eq. (28).58 While such a direct modification of the Parisi-Sourlas
Lagrangian may appear physically reasonable, it does not seem a first-principle derivation
from the replicated action. This should be contrasted with our approach, where the terms
L1 , L2 modifying the Parisi-Sourlas Lagrangian came from an explicit Cardy transform.
57
58

We thank Gilles Tarjus for a discussion.
This is somewhat similar in spirit to the modification of mean-field theory considered in [88].

– 61 –

JHEP03(2021)219

This equation turns out to have nontrivial solutions with “cuspy” K ′′ (t), for an appropriately chosen value of ζ.
With R on the self-similar trajectory (A.12), redefining the variable u(x) = Λ−ζ ū(Λy),
effective action in terms of the ū field (which has momenta of order 1) takes the same form
as (A.8) but with a rescaled temperature

## PDF page 65

This line of reasoning leads Tarjus et al. to a theory (see [92], eq. (42)) with N super∫
∫
fields59 Φa (x, θ, θ̄), a = 1, . . . , N and the action ( θ := dθ̄dθ(1 + βθθ̄)
N
∑∫

d

∫ [

d x
θ

a=1

∑
1
H N
(∂µ Φa )2 + V (Φa ) −
2
2 a,b=1
]

∫

d

∫

∫

Φa (x, θ1 , θ1 )Φb (x, θ2 , θ2 ). (A.15)

d x
θ1

θ2

N {
∑
a=1

1 ∑′
H
∂ϕa ∂ωa +
(∂χa,i )2 −
2
2
}

(N
∑

)2

ωa

(A.16)

.

a=1

Assume now for a second that the fields ϕa , χa,i , ωa for each a have the same scaling dimensions as those of ϕ, ω, χi given in (2.16) [this is not quite correct, see below]. Then, dropping
the interaction terms irrelevant in d = 6 − ε with these scaling dimension assignments, we
would get the interaction Lagrangian
N {
∑
a=1

∑′
1
V (ϕa )ωa + V ′′ (ϕa )
χ2a,i .
2
}

′

(A.17)

If we now introduce N supermultiplets Φa = (ϕa , ψa , ψ̄a , ωa ), and replace the χa -bilinears
by ψa ψ̄a ones, the sum of (A.16) and (A.17) maps on the Lagrangian
N
∑{

∂ϕa ∂ωa + ∂ψa ∂ ψ̄a + V ′ (ϕa )ωa + V ′′ (ϕa )ψa ψ̄a

}

a=1

H
−
2

which can be also written in terms of superfields as (A|θθ̄ :=
N
∑[
a=1

1
H
∂µ Φa ∂µ Φa + V (Φ)
−
2
2
θ θ̄
]

(N
∑

∫

(N
∑

)2

ωa

,

(A.18)

a=1

dθ̄dθA)
)2

Φa |θθ̄

.

(A.19)

a=1

This would correspond to the β = 0 case of the Tarjus et al. action (A.15). It has N
independent supertranslation invariances, one for each supermultiplet.
However, it was incorrect to assign to ϕa , χa,i , ωa for each a the same scaling dimensions
as for ϕ, χi , ω. We had to diagonalize the kinetic part before assigning scaling dimensions,
∑
and (A.16) is not fully diagonalized, since ωa appear coupled through ( ωa )2 . For a
∑
∑
better treatment, we have to introduce fields ω0 = ωa , ϕ0 = N1
ϕa , ω̃a = ωa − N1 ω0 ,
∑
∑
ϕ̃a = ϕa − ϕ0 ( ϕ̃a = ω̃a = 0) in terms of which the kinetic Lagrangian takes the form
N
H 2 ∑
1 ∑′
ω0 +
∂ ϕ̃a ∂ ω̃a +
(∂χa,i )2 .
2
2
a=1

{

∂ϕ0 ∂ω0 −
59

Whose number is denoted by n in ref. [92].

– 62 –

}

(A.20)

JHEP03(2021)219

As mentioned it is not clear to us if this action is correct in the first place. Nevertheless,
for the sake of comparison, let us try to get a similar action from our point of view. We
will not fully succeed, but we will learn some interesting lessons along the way. Take our
replicated action (2.7) and replace n → nN for a fixed integer N . The limits n → 0 and
nN → 0 being equivalent, imagine that we have N groups of n → 0 fields, and apply the
Cardy transform in each group separately. We will get a Lagrangian for fields ϕa , χa,i , ωa ,
a = 1 . . . N, i = 2 . . . n. The kinetic term in the n → 0 limit is

## PDF page 66

Therefore, the pair of fields ϕ0 , ω0 has scaling dimensions like ϕ, ω while all the other
fields (χa,i , ϕ̃a , ω̃a ) should be assigned scaling dimensions d/2 − 1. With the new dimension
assignments, more terms in the interaction Lagrangian (A.17) become irrelevant and should
be dropped (while no previously dropped terms became relevant). The only remaining
terms are:
{N
}
∑
1 ∑′ 2
′
′′
V (ϕ0 )ω0 + V (ϕ0 )
ϕ̃a ω̃a +
χa,i .
(A.21)
2
a=1

1
H
LSUSY + β (∂ϕ)2 + V (ϕ) − (βωϕ + β 2 ϕ2 ).
2
2
[

]

(A.22)

Recall that in our picture the Parisi-Sourlas Lagrangian follows from the replicated action
in the n → 0 limit, and the underlying Sn invariance has to be respected. It therefore
appears to us worrisome that the extra terms in (A.22) are not Sn singlets according to
our classification. The Sn invariance is thus explicitly broken by these β-terms. For N > 1
action (A.15) preserves only SN invariance, while we would insist that the full SnN has to
be preserved at the microscopic level.
After we reviewed all the worries that we have about action (A.15), let us describe
the results that Tarjus et al. derive from this action. In [50], section III, they describe
loss of SUSY in terms of its “spontaneous breaking”. Since their action (A.15) is not fully
supersymmetric in the first place (superrotation invariance being broken by the β ̸= 0
terms), it is not clear to us why it is legitimate to talk about spontaneous breaking (in
the standard high-energy physics terminolgy the situation at hand would be called explicit
SUSY breaking). Recall also that the usual spontaneous SUSY breaking is associated with
the appearance of massless particles (goldstinos), which does not appear consistent with
the RFIM phenomenology.
When Tarjus et al. derive the FRG equations they set β = ∞, in which limit the
equations involve only the bosonic components of the superfields, a property they call
“Grassmannian ultralocality”. They claim they have an argument that in this limit supersymmetry is restored, which seems to us rather counterintuitive, but we should admit that
our understanding of this part of their work is very limited. Working with the FRG for
the second cumulant, they give further arguments relating the loss dimensional reduction
60

As observed in [92] this action retains a supertranslation invariance even for nonzero β, corresponding
to Killing vectors of the curved superspace with a constant-curvature metric dθ̄dθ(1 + βθθ̄).

– 63 –

JHEP03(2021)219

Now, the total number of fields ϕ̃a , ω̃a , χa,i is nN − 2 → −2 in the n → 0 limit, and their
effect can be reproduced by a single pair of fermions ψ0 , ψ̄0 . We then end up with a theory
containing one supermultiplet (ϕ0 , ψ0 , ψ̄0 , ω0 ), not N supermultiplets like Tarjus et al.
This discussion suggests that splitting n → 0 fields into N groups does not add new
effects when using the Cardy transform, provided that one correctly identifies scaling dimensions. As we mentioned several times in this paper, the Cardy transform is just a
change of the field basis, and all bases should be equivalent no matter how one slices and
dices the fields, as long as we do not drop any terms without justification.
We next discuss the terms in the Tarjus et al. action (A.15) which appear for nonzero
β. Focusing on N = 1, the full Lagrangian in superfield components takes the form:60

## PDF page 67

A.8

Comments on the perturbative “cusp operators”

In sections A.6 and A.7 we saw that “cusp” interactions appear to play a role in the nonperturbative descriptions of disordered fixed points. We are happy to admit that this might
well be the case in the FRG context, not being experts in that technique. We feel more confident however in perturbative QFT aspects, and here we wish to comment on ref. [28], which
considered a cusp operator in the context of a perturbative expansion around a Gaussian
fixed point in d = 6 − ε dimension. Working with the usual replicated RFIM action (2.7),
this “cusp” operator was defined in [28] in terms of the replica fields as (see their eq. (5))
C=

n
∑

φi φj |φi − φj |.

(A.23)

i,j=1

Before we discuss how they deal with this operator, let us consider a simpler case of a
single free massless scalar φ (in any d > 2). In this Gaussian theory, the full spectrum of
perturbations Oi with well-defined scaling dimensions is given by normal ordered products
of φ and its derivatives. Operators involving non-analytic functions of φ, such as |φ|,
are not in that list. Now one can ask, what if one does consider a correlation function
involving |φ|? E.g. one can imagine measuring ⟨|φ|(x)|φ|(y)⟩ in a Monte Carlo simulation
in a lattice-discretized (∂φ)2 theory (or with another UV cutoff). What would be a
behavior of this correlation function at large distances where the theory is scale invariant?
The answer to this follows from the fact that the operator |φ| will have an expansion
|ϕ|(x) =

∞
∑

ai Oi (x),

(A.24)

i=1

where Oi are the above operators with well-defined scaling dimension. In addition, since
|φ| is Z2 -even, only Z2 -even operators will appear on the r.h.s. We will have O1 = 1

– 64 –

JHEP03(2021)219

to an appearance of a “cusp” in this quantity. Finally by solving the FRG numerically,
they do find a cusp below dc ≈ 5.1 [50]. While in [50] they attribute the loss of dimensional reduction to “spontaneous SUSY breaking” (see our misgivings above), in subsequent
work [53, 93] they ascribe it instead to an annihilation of two SUSY fixed points.
Note that in more familiar situations where two fixed point of the same symmetry
annihilate, they disappear into the complex plane (e.g. in the 2d Potts model where a
stable and an unstable fixed points annihilate for Q = 4, for Q > 4 there is no fixed
point and the transition is weakly first order, see [94, 95] for a recent discussion). This is
not what is found in the FRG work where two SUSY fixed points existing at d > dc are
claimed to annihilate and yet a third, non-SUSY, fixed point emerges at d < dc . It would
be interesting to understand what makes their scenario consistent, from the point of view
of the quantum numbers of the operator crossing the marginality bound (which should be
a full SUSY singlet if the annihilating fixed points are both SUSY, and it is then unclear
how it can give rise to a non-SUSY fixed point at d < dc ).
This concludes our outline of the FRG RFIM studies by Tarjus et al. In the next
section we will try to make contact with their work [28], where cuspy interactions were
discussed in the context of perturbative expansion in d = 6 − ε.

## PDF page 68

δ
δ
δφa (x) δφb (y)

∫

dd z Fk (z) = −2k(k − 1)δ(x − y)(φa − φb )k−2 (1 + O(φa − φb )).

(A.25)

Of course the behavior above is very different from the one of C since it is analytic. However
the fact that all Fk behave as positive powers of (φa −φb ) — in contrast with other operators
∑
of the replicated theory which would scale like a constant, e.g. i φki — is a tantalizing
observation. A similar observation is that the absolute value |φa − φb | can be expanded
(using the regularization described in section A.8.1 below) in terms of operators Fk . It
would be interesting to see if there exists a connection between the alleged cuspy behavior
of the susy-broken IR fixed point and the Feldman perturbations Fk .
A.8.1

Two-point function of |φ|

To convince the reader that our picture is indeed correct, in the following we perform an
explicit computation of the two point function of |φ| in the free massless scalar theory of

– 65 –

JHEP03(2021)219

(unit operator), O2 = : φ2 :, etc. So subtracting the constant, the leading behavior of
the connected two-point function of the operator |φ| will be the same as for φ2 (see section A.8.1 below for a proof via an explicit computation). This just illustrates that we do
not enlarge the spectrum of scaling dimensions by considering non-polynomial operators.
This should not be surprising: e.g. when we study the spectrum of perturbations of the
Wilson-Fisher fixed points, we always consider only polynomial interactions and compute
their anomalous dimensions. If we had to consider non-polynomial operators, there would
be many more anomalous dimensions to compute, and there is no evidence that this is
necessary, from theory, experiment, or simulations.
For similar reason, we believe that operator (A.23) does not exist as a scale-invariant
perturbation of the RFIM replicated Gaussian fixed point in d = 6 − ε dimensions. At long
distances, this operator should be expandable in polynomial operators considered by Brézin
and De Dominicis [27], Feldman [29], and other operators that we studied in our work.
On the other hand, ref. [28] does consider operator (A.23) as an independent perturbation of classical scaling dimension ∆0C = d + 1 − ε/2 = 7 − 3ε/2 (see e.g. their eq. (9)),
without explaining in detail how they arrived to this dimension (no correlator which would
correspond to such a scaling is exhibited). Given that we do not understand the origin
of this classical dimension, and in fact oppose the very existence of C as a scale-invariant
perturbation, we will not enter into the discussion of how ref. [28] computes the anomalous
dimension of C.
Finally we would like to show a property of the Feldman operators Fk , which might
have some positive connections to the work of [28]. The requirement used in [28] to fix the
form of C is that the second cumulant of the partition function perturbed by C should behave
∫
as the absolute value of |φa − φb | in the limit φb → φa , namely δφaδ(x) δφbδ(y) dd z C(z) =
2δ(x−y)|φa −φb |(1+O(φa −φb )). As we explained above, we think that the perturbation C
should not be considered. On the other hand in our work we presented some perturbations
which we think could destabilize the IR SUSY fixed point, the most dangerous candidates
being the Feldman operators Fk . These operators affect the second cumulant as follows,

## PDF page 69

φ regulated with a UV cutoff Λ in momentum space.61 We will show that this can be
expanded in an infinite sum of two-point functions of Z2 -even operators. Naively, to do
this computation one may wish to expand |φ| in terms of monomials φk . Of course this
is not possible since the absolute value is not an analytic function and it does not admit
a power expansion. We will use an alternative definition of |φ| = φ sign(φ) representing
sign(φ) as a limit of an analytic function
x
ε

( )

sign(x) = lim f
ε→0

f (x) =

,

2
Si(πx) ,
π

(A.26)

∫

f (x) =

∞
∑

a2n+1 =

an xn ,

n=0

2(−π 2 )n
,
(2n + 1)2 (2n)!

a2n = 0 .

(A.27)

Using this expansion we rewrite the two point function of |φ| as follows:
⟨|φ(x)||φ(y)|⟩ = lim

ε→0

∞
∑
an am

εn+m
m,n=0

⟨φn+1 (x)φm+1 (y)⟩.

(A.28)

Notice that the operators φn+1 and φm+1 in (A.28) are not normal ordered. It is then convenient to rewrite the correlator ⟨φn+1 (x)φm+1 (y)⟩ as a sum of normal ordered correlation
functions,
(

⟨φ

n+1

(x)φ

m+1

(y)⟩ =

∑

M =0,2,4,...

n+1
M

)(

m+1
⟨φn+1−M (x)⟩⟨φm+1−M (y)⟩⟨:φM (x)::φM (y):⟩ ,
M
)

(A.29)
where M must be even since both n + 1 and m + 1 are even. Here the correlation functions
of k operators inserted at the same point can be computed as ⟨φk (x)⟩ = (k − 1)!!G(0)k/2 ,
where the double factorial (k − 1)!! is the combinatorial factor which counts the number
of pairings in k elements, while G(0) is the two-point function at coincident points G(0) ≡
∫
dd k
−2 = const ×Λd−2 . Combining these results we find that the
⟨φ(x)φ(x)⟩ = |k|<Λ (2π)
d |k|
sums over n and m factorize and can be easily performed,
SM (X) ≡

∞
∑
n=0

(

(n − M )!!

M
n+1
an X n = X 2 2 +1
M

)

(

2 F2

1
3
M
π2 X 2
2 , 2; 2 , 2 − 2 ; − 2

(

)

Γ 2− M
2 Γ(M + 1)
√

)

,

(A.30)

G(0)

where the expansion parameter X takes the form X = ε . In particular we are interested in taking the limit of ε → 0 which corresponds to sending X to infinity,
∞
SM
≡

61

lim SM (X) =

X→∞

2
M !Γ

M −1
2

(

3−M
2

).

We do not know any way to make sense of this operator in a theory without UV cutoff.

– 66 –

(A.31)

JHEP03(2021)219

where Si (x) ≡ 0x dy
y sin y is an entire function known as “sine integral” (see below for why
we choose this particular regulator). We therefore Taylor expand the function f as follows

## PDF page 70

Putting everything together we thus find
⟨|φ(x)||φ(y)|⟩ =

∑

∞ 2
G(0)1−M (SM
) ⟨: φM (x) :: φM (y) :⟩.

(A.32)

M =0,2,4,...

A.9

Comparison to the work of Brézin and De Dominicis

In this paper we used the observation of Brézin and De Dominicis [27] concerning the need
to consider additional Sn invariant interactions in the effective Lagrangian. On the other
hand, we disagree with ref. [27] on how to interpret the instability of n = 0 fixed point with
respect to turning on nonzero n, and in particular about the role of the additional fixed
point identified in [27]. In this appendix we will review this disagreement in more detail.
Ref. [27] worked in the “old” formalism (replicated field basis with propagator (2.10)).
The quadratic part of the replicated Lagrangian was perturbed by a general linear combination of the Sn -singlet perturbations with 4 fields given in eq. (5.10): u1 σ4 + u2 σ1 σ3 +
u3 σ22 + u4 σ12 σ2 + u5 σ14 . All of the couplings ui were assigned in d = 6 − ε the same scaling
dimension ε as u1 , as is visible from RG equations (3.2) in [27], which all have the form
βui = −εui + HCijk uj uk with dimensionless Cijk . In our scheme the couplings u2, u3 , u4 , u5
62

The above is not the only way to perform this computation. E.g., denoting a = φ(x), b = φ(y),
one can integrate out all the space-points in the path integral except for x, y, and obtain the probability
distribution density P (a, b). Since the theory is Gaussian, this is given by a Gaussian distribution P (a, b) ∝
exp(−u(a2 + b2 ) − 2vab), and the coefficients u, v can be fixed uniquely by requiring that the two point
functions ⟨φ(x)φ(x)⟩ and
∫ ⟨φ(x)φ(y)⟩ are correctly reproduced. Then the two-point function ⟨|φ(x)||φ(y)|⟩
can be computed as da db |a||b|P (a, b). This gives the same result as (A.32). See also [96] for how to
deal with non-polynomial operators in field theory (we thank Giorgio Parisi for mentioning this early work,
whose focus is on the UV).

– 67 –

JHEP03(2021)219

The result (A.32) confirms our expectation: the two-point function of |φ| can be written
as sum of two-point functions of Z2 -even operators. In particular at large distances (for
large |x − y|) (A.32) behaves as the two-point function of the identity plus the one of φ2 .
One can eliminate the contribution of the identity by defining a normal ordered version
of |φ| with vanishing one-point function. The resulting normal ordered operator at large
distances would thus behave as φ2 .
To clarify all steps of our computation, we would like to comment on the choice of
the function f (x) in (A.26). There are many possible analytic functions which tend to the
sign function in some limit. We chose to use (A.26) because of its excellent convergence
properties. Indeed it is not enough to consider a function f (x) with a uniformly convergent
expansion. For our computation we must also require that it is possible to commute the
path integral with the series expansion. It is easy to see that this is a more restrictive
requirement. E.g. for the one-point function of |φ|, after commuting the path integral
∑
n
with the sum we find a new series of the form ∞
n=0 (n)!!an x , where the new coefficients
(n)!!an grow much faster than an . If one chooses functions f with weaker convergence it
may happen that the path-integral and the series cannot be swapped or, in other words,
that the integrated expansion diverges.62
We hope that this explicit computation clarifies that it is sufficient to consider perturbations around free theory of the polynomial form.

## PDF page 71

would have dimensions ε−2, ε−2, ε−4, ε−6, looking at the scaling dimension of the leader
of the corresponding interaction. Up to this difference, RG equations (3.2) in [27] bear some
similarity with the Wilsonian RG equations (B.13) in appendix B below. eqs. (B.13) were
derived for n = 0, but (3.2) in [27] contain some terms proportional to powers of n. Ref. [27]
observed that the fixed point u1 = u1∗ , u2 = u3 = . . . = u5 = 0 is unstable with respect to
the inclusion of these n ̸= 0 terms, and identified another fixed point for nonzero n where
the couplings scale singularly as
u1 = O(1),

u2 , u3 = O(1/n),

u4 = O(1/n2 ),

u5 = O(1/n3 ).

(A.33)

A.10

Conformal bootstrap approach to dimensional reduction

In section 11.2.2 we described prospects for applying the conformal bootstrap approach to
study the RFIM fixed point. The only prior work in this direction is by Hikami [65]. We
will now briefly describe how we understand the computations reported in that paper. We
only comment on the part of [65] which concerns the RFIM, leaving aside the branched
polymer case also treated there.
In our language, ref. [65] studies the 4pt function of χi ’s which is called there “φ” and
we will use the same notation in this appendix. This identification is visible from [65],
eq. (27). This 4pt function is considered in the strict n → 0 limit63 and at the fixed point,
63

This should correspond to −2 linearly independent χ’s. Since the crossing equations are not written
explicitly in [65], it is impossible to verify the exact number of fields used in the computations. If ref. [65]
used 0-component χ, it is a mistake.

– 68 –

JHEP03(2021)219

Because of the mentioned mismatch in the scaling dimensions of ui , we are not sure to
agree with the details of this computation, although we do completely agree with the
conclusion that the n = 0 fixed point should be unstable with respect to turning on
n ̸= 0 (see section 6). We disagree however with the interpretation of this instability. As
discussed in section 6, even though the n = 0 fixed point is unstable, the approximately
scale-invariant regime becomes longer and longer as n gets smaller and smaller. The
Brézin-De Dominicis fixed point (A.33) at nonzero n is pushed to longer and longer
distances as n gets smaller, and cannot describe the RFIM phase transition. It is, as we
said in section 6, disconnected from the n = 0 physics. This is why in the main text we
did not at all consider this fixed point.
In particular, we do not believe that one can shed light on the Parisi-Sourlas conjecture
by considering the properties of the Brézin-De Dominicis fixed point. (That is what ref. [27]
tried to do. They observed that their fixed point (A.33) is unstable, and argued that this
instability may lead to the violation of the Parisi-Sourlas conjecture for any d < 6.)
Ref. [27] is also sometimes cited (e.g. in [40]) for the fact that RG in RFIM is singular
as n → 0. Some loop effects singular in n are indeed mentioned in section 2 of [27]. We
are puzzled by that section: e.g. in a Wilsonian RG scheme with a UV and an IR cutoff
we do not see any singularity in their eq. (2.6) for d = 6. Independently of what these
“singularities” might mean, they do not trickle down to their d = 6 − ε RG equations
([27], section 3), which are completely smooth in the limit n → 0, in agreement with our
discussion in section 5.

## PDF page 72

A.11

Other approaches

Without trying to judge the merit, we will briefly mention two other theoretical ideas about
the RFIM transition.
It has been proposed to connect the loss of dimensional reduction to “formation of
bound state of replicas”.64 This scenario was discussed e.g. in [98], section 5, where references to prior work can be found. In ref. [99], numerical simulations of the RFIM in d = 3
64

We are not sure, but perhaps one can think of this mechanism as due to fluctuations with large values
of fields which render the fixed point unstable, in spite of stability with respect to small fluctuations. This

– 69 –

JHEP03(2021)219

assuming conformal invariance. The spectrum of exchanged CFT operators in the OPE
φ × φ is limited to 3 scalar operators of dimension ∆1 , ∆ε , ∆ε′ and one spin-4 operator
whose dimension is called Q. (The operator of dimension ∆1 is non-susy-writable in our
language.) Determinant method of Gliozzi is applied to solve crossing approximately and
determine the scaling dimensions of these operators as a function of the spatial dimension
4 ⩽ d ⩽ 6 ([65], table 4). The so determined scaling dimensions of φ and of the energy
operator ε are seen to satisfy the dimensional reduction predictions reasonably well for
d > 5, while for d < 5 larger deviations are observed.
In each of the figures 7–13, ref. [65] varies ∆φ and ∆ε to find the intersection points
(approximate solution of crossing) while parameters ∆1 and Q are fixed to particular values.
It is not clearly reported how those values are arrived at, and how the predictions would
change if different values were chosen. It is also not clear why a spin-4 operator is included
in this study but not spin-2 operators. One may also question the accuracy of truncation,
because at d = 6, ∆1 = 4.3 in table 4, deviating significantly from the Gaussian prediction
∆1 = 4.
Ref. [65] does not investigate the mechanism by which dimensional reduction is lost
at the critical dimension dc . On theoretical grounds, we know that this loss is associated
with the loss of SUSY, which should happen because some operator becomes relevant. The
operator becoming relevant may be either a SUSY singlet, in which case SUSY would be
lost via fixed point annihilation, as in FRG studies cited in section 11. Or, as we found
in our work, SUSY fixed point may become unstable because a SUSY-breaking leader
operator becomes relevant. In the former case there should be two fixed points above dc :
the two SUSY fixed points which annihilate. In the later case there should be two fixed
points below dc : the unstable SUSY one, and the stable non-SUSY.
Focusing on just one 4pt function, ref. [65] is not sensitive to finer aspects of ParisiSourlas supersymmetry apart from predictions for operator dimensions from dimensional
reduction. It reports only one CFT for any d, which appears incompatible with either
scenario. No operator is reported to become relevant at dc . (A SUSY-singlet should
appear in the OPE φ × φ and hence be visible in this study.)
In our opinion, while the observations of [65] are suggestive, a much more careful study
is needed to verify that they are physical and are not instead due to truncation effects. This
study should confirm explicitly the existence of SUSY above dc and its absence below dc
(beyond dimensional reduction operator dimensions), and clarify the mechanism by which
SUSY is lost.

## PDF page 73

B

Toy model for the L0 + L1 RG flow

In this section we develop a very concrete toy model for the L0 + L1 RG flow, mentioned
in section 7.3. It is important to stress that the aim of this section is not to study all
interesting operators which may have an important role in destabilizing the RG. Here we
want only to show a computation which clarifies some features of the RG (e.g. the role of
Sn symmetry, leaders, followers, etc.).
We consider a setup where the Gaussian piece of the L0 Lagrangian is perturbed by
5 Sn -singlet operators, chosen to be all the perturbations which contain 4 fields and no
derivatives. Since the perturbations are free of derivatives, they can be written as products
of the σi fields. So we get eq. (7.10), where each Sn -singlet multiplies a coupling hi . It is
instructive write this Lagrangian in the Cardy basis. When n = 0, the 5 Sn singlets are
written as linear combinations of 11 fields,
3
σ4 = 6ϕ2 χ2 + 4ϕ3 ω + 4ϕχ3i + (χ4i − 6ϕωχ2i ) − 2ωχ3i + ( ω 2 χ2i + ϕω 3 ),
2
2
2
2 2
2 2
σ2 = 4ϕωχi + 4ϕ ω + (χi ) ,
3
ω4
σ1 σ3 = 3ϕωχ2i + 3ϕ2 ω 2 + ωχ3i − ω 2 χ2i +
,
2
4
σ12 σ2 = ω 2 χ2i + 2ϕω 3 ,

(B.1)

σ14 = ω 4 .
We are therefore led to write a Gaussian action perturbed with eleven independent couplings gi , eq. (7.11). This Lagrangian exactly matches equation (7.10) when the couplings
gi satisfy the following Sn -invariance condition obtained by substituting (B.1) in (7.10)
g1 = g2 = g3 = g4 = h1 ,
3
g7 = (h1 − h3 ) + h4 ,
2
g10 = h2 ,

g5 = −6h1 + 4h2 + 3h3 , g6 = h3 − 2h1 ,
g8 = h1 + 2h4 ,
g11 =

g9 = 4h2 + 3h3 ,

(B.2)

h3
+ h5 .
4

would be somewhat similar to instabilities in fixed points of scalar theories with unstable potentials (like
cubic with a real coupling or quartic with a negative coupling, see e.g. [97]).

– 70 –

JHEP03(2021)219

seemed to provide support for bound states of replicas. Note that as mentioned several
times, we do not expect a SUSY fixed point in d = 3. It would be interesting to know if the
non-self-averaging phenomena observed in [99] persist in d = 4 and d = 5, and whether they
are present in modern high-statistics simulations [6–8] which do not comment on this issue.
Recently, ref. [100] proposed to expand the RFIM around an exact solution on the
“Bethe lattice” (an infinite tree without loops with all vertices equivalent and having coordination number 2d, like for the cubic lattice in d dimension). While this approach is
very different from the traditional one, their calculations were consistent with dimensional
reduction in d close to 6.
Finally, RFIM critical exponents can be studied using the high temperature expansion.
Ref. [101] thus obtained γ = 1.13(3), 1.45(5), 2.1(2) in d = 5, 4, 3, which using γ = ν(2 − η)
is in the ballpark of the more recent accurate Monte Carlo results cited in sections A.2, A.3.

## PDF page 74

In the nest subsections we want to investigate how the couplings gi evolve under RG when
the Sn -condition (B.2) are or are not imposed in the UV.
B.1

Integrating out

Let us start by considering 11 independent couplings gi which are all small perturbation
of the same order. We work in d = 6 − ε dimensions in a theory with a momentum-space
cutoff Λ. We want to compute how the couplings change as we integrate out degrees of
freedom from Λ′ < Λ to Λ. The resulting couplings g̃i , at order O(gi2 ), take the form

g̃2 = g2 + 36g22 I
g̃3 = g3 + 36g1 g3 I
g̃4 = g4 + 36g32 I
g̃5 = g5 + 12(2g1 g5 + g2 g5 + 2g1 g9 )I
(B.3)

g̃6 = g6 + 12g3 g5 I
g̃7 = g7 + (g52 + g9 g5 + 18g1 g8 )I
g̃8 = g8 + 4(g92 + 9g2 g8 )I
g̃9 = g9 + 60g2 g9 I
g̃10 = g10 + 6(6g32 + g1 g5 )I
g̃11 = g11 + 3g8 g9 I,

Here, for simplicity, we consider only the contributions given by the one-loop integral
I which depends logarithmically on the ratio b ≡ Λ/Λ′ of the cutoff scales:65
H
I=
2

dd k
1
1 H
=
log b + O(ε).
d
2
2
2
2 (4π)3
Λ′ (2π) (k ) (p − k)

∫ Λ

(B.4)

From (B.3) we can explicitly test if Sn symmetry is preserved by integrating-out. Namely
we want to check that, when (B.2) is satisfied by the bare couplings, the renormalized
couplings g̃i satisfy the same condition (B.2) where all couplings are tilded, namely
g̃1 = g̃2 = g̃3 = g̃4 = h̃1 ,
3
g̃7 = (h̃1 − h̃3 ) + h̃4 ,
2

g̃5 = −6h̃1 + 4h̃2 + 3h̃3 , g̃6 = h̃3 − 2h̃1 ,

g̃10 = h̃2 ,

g̃11 =

g̃8 = h̃1 + 2h̃4 ,

g̃9 = 4h̃2 + 3h̃3 ,

(B.5)

h̃3
+ h̃5 ,
4

where h̃i define the new values of the couplings hi after integrating out. This amounts to
check that, after imposing (B.2) and (B.5), the eleven equations (B.3) for the couplings gi
65

These are indeed the only contributions which would survive in other schemes, like dimensional regularization. For completeness we also performed a computation which takes into account all the one-loop
integrals — also the ones which scale as powers of the cutoff — and we found that, at leading order in ε,
the IR fixed point does not change. Since the result is unchanged, but all the intermediate step are more
complicated, we decided to present this simpler setup.

– 71 –

JHEP03(2021)219

g̃1 = g1 + 12(2g1 + g2 )g1 I

## PDF page 75

reduce to only five equations for the renormalization of the couplings hi . For example let
us consider what happens to the first four equations of (B.3) which only involve couplings
g1 , . . . , g4 which are all set to h1 by (B.2) (and similarly for their tilded companions). For Sn
to be respected it is crucial that these four equation reduce to the same one in terms of h1 .
It is easy to see that this indeed happens giving rise to g̃1 = g̃2 = g̃3 = g̃4 = h̃1 = h1 +36h21 I.
By applying the same logic to the other equations we obtain the wanted 5 renormalization
equations for hi ,

h̃2 = h2 + (24h1 h2 + 18h1 h3 )I
(B.6)

h̃3 = h3 + (48h1 h2 + 36h1 h3 )I
h̃4 = h4 + (32h22 + 48h3 h2 + 18h23 + 36h1 h4 )I
h̃5 = h5 + (24h2 h4 + 18h3 h4 )I .

In other words, when Sn symmetry is present in the UV, the renormalization of the 11
couplings g̃i can be computed using (B.5) and the renormalization of only 5 Sn -symmetric
couplings (B.6).
Computationally, this is a non-trivial check of Sn symmetry, although conceptually
this should not be surprising. In fact we knew that Sn invariance was actually present in
the initial action, even if it was hidden by the use of Cardy variables. One could have been
worried that Sn would be spoiled by dropping the n-suppressed terms. This computation
exemplifies that even when n is set to zero, Sn symmetry continues to exist and plays an
important role.

B.2

Rescaling

To complete the RG step, and get a Lagrangian of the same form as the initial one but
with new couplings gi (b), we need to rescale the cutoff to its original value. This amounts
to rescale the couplings g̃i defined at Λ′ by a factor bd−∆0 where b ≡ Λ/Λ′ and the power
is dictated by the classical dimensions ∆0 of the fields,

g1 (b) = g̃1 bε ,

g2 (b) = g̃2 bε ,

g3 (b) = g̃3 bε−1 ,

g4 (b) = g̃4 bε−2 ,

g5 (b) = g̃5 bε−2 ,

g6 (b) = g̃6 bε−3 ,

g7 (b) = g̃7 bε−4 ,

g8 (b) = g̃8 bε−4 ,

g9 (b) = g̃9 bε−2 , g10 (b) = g̃10 bε−2 , g11 (b) = g̃11 bε−6

– 72 –

(B.7)

JHEP03(2021)219

h̃1 = h1 + 36h21 I

## PDF page 76

By rescaling the couplings, equations (B.5) get rescaled as follows
g1 (b) = g2 (b) = g3 (b)b = g4 (b)b2 = h̃1 bε
g5 (b) = −(6h̃1 − 4h̃2 − 3h̃3 )bε−2
g6 (b) = −(2h̃1 − h̃3 )bε−3
1
g7 (b) = (3h̃1 − 3h̃3 + 2h̃4 )bε−4
2
g8 (b) = (h̃1 + 2h̃4 )bε−4

(B.8)

g10 (b) = h̃2 bε−2
1
g11 (b) = (h̃3 + 4h̃5 )bε−6 .
4
So while before rescaling Sn symmetry sets certain couplings equal to each other, after
rescaling it relates them by powers of the rescaling factor b. This is due to the fact that fields
ϕ, ω, χi related by the Sn symmetry have different classical scaling dimensions (contrary
to the usual situation that fields forming a multiplet under a symmetry have the same
dimensions). We say that “Sn symmetry does not commute with rescaling”. This makes
Sn symmetry less manifest, since some couplings which start in the UV with the same value,
may evolve differently. However it is important to stress that Sn symmetry is still present
(so it is not broken), and constrains the RG at all scales as it is clear from the relations (B.8).
By setting all h̃i>1 = 0 in (B.8), we can recover exactly formula (7.4) for the form of
σ4 after an RG step. Similarly, by keeping only one non-zero h̃i , we can obtain how the
other Sn singlets rescale after one RG step. The result is as follows
ϕχ3 χ4 − 6ϕωχ2i
ωχ3i 32 ω 2 χ2i + ϕω 3
h1 σ4 → h1 (b) 6ϕ χ + 4ϕ ω + 4 i + i
−
2
+
b
b2
b3
b4
(

2 2

3

)

,

h2 σ22 → h2 (b)(4ϕωχ2i + 4ϕ2 ω 2 + (χ2i )2 ) ,
(

h3 σ1 σ3 → h3 (b)

ωχ3i 3 ω 2 χ2i
ω4
3ϕωχ2i + 3ϕ2 ω 2 +
−
+ 4
2
b

2 b

4b

)

,

(B.9)

h4 σ12 σ2 → h4 (b)(ω 2 χ2i + 2ϕω 3 ) ,
h5 σ14 → h5 (b)ω 4 ,
where we introduced a natural definition for the rescaled couplings hi (b),
h1 (b) ≡ h̃1 bε ,

h2 (b) ≡ h̃2 bε−2 ,

h3 (b) ≡ h̃3 bε−2 ,

h5 (b) ≡ h̃5 bε−6 .
(B.10)
Expression (B.9) is an explicit example of formula (7.8) of the main text.

– 73 –

h4 (b) ≡ h̃4 bε−4 ,

JHEP03(2021)219

g9 (b) = (4h̃2 + 3h̃3 )bε−2

## PDF page 77

B.3

Beta functions and fixed point

After integrating-out (B.3) and rescaling (B.7) we can finally define the beta functions for
d
the eleven couplings by βgi ≡ d log
b gi (b). This gives
βg1 = −g1 ε + 12g1 (2g1 + g2 ) J
βg2 = −g2 ε + 36g22 J
βg3 = g3 (1 − ε) + 36g1 g3 J
βg4 = g4 (2 − ε) + 36g32 J
(B.11)

βg6 = g6 (3 − ε) + 12g3 g5 J
βg7 = g7 (4 − ε) + (g52 + g9 g5 + 18g1 g8 ) J
βg8 = g8 (4 − ε) + 4(g92 + 9g2 g8 ) J
βg9 = g9 (2 − ε) + 60g2 g9 J
βg10 = g10 (2 − ε) + 6(6g32 + g1 g5 ) J
βg11 = g11 (6 − ε) + 3g8 g9 J ,

H
where J ≡ 2(4π)
3 . We are interested in fixed points which can be reached from the Sn
invariant initial conditions (B.2). In particular any such fixed point will have g1 = g2 , as
is clear from (B.8). Imposing this condition, we find a single non-trivial fixed point:

g1⋆ = g2⋆ =

ε
,
36J

⋆
gi>2
= 0.

(B.12)

⋆
Since all couplings gi>2
vanish, this fixed point is the same as that of L0 (equivalent to
LSUSY ). We conclude that every computation done close to the IR fixed point of Lagrangian (7.11) with Sn symmetric initial conditions (B.2) can be equivalently done in a
much simpler setup where the Gaussian piece of L0 is perturbed by the single susy-writable
operator 6ϕ2 χ2i + 4ϕ3 ω.
Finally we show the β-functions for the couplings hi (b) of (B.10):

βh1 = −h1 ε + 36h21 J
βh2 = h2 (2 − ε) + 24h1 h2 J + 18h1 h3 J
βh3 = h3 (2 − ε) + 48h1 h2 J + 36h1 h3 J

(B.13)

βh4 = h4 (4 − ε) + 32h22 J + 48h3 h2 J + 18h23 J + 36h1 h4 J
βh5 = h5 (6 − ε) + 24h2 h4 J + 18h3 h4 J .
The fixed point of the hi flow is given by h⋆1 = 36ε J and h⋆i>1 = 0.
B.4

Perturbations around the IR fixed point

Next we want to study the perturbations around the fixed point.
We first linearize the RG flow of gi around the fixed point and study the 11 eigenvectors
va and eigenvalues λa of the matrix Mij = ∂gj βgi |g⋆ . The eigenvectors va define the IR

– 74 –

JHEP03(2021)219

βg5 = g5 (2 − ε) + 12(g2 g5 + 2g1 (g5 + g9 )) J

## PDF page 78

Oa

6

12 − 2ε

6ϕ2 χ2i + 4ϕ3 ω
(χ2i )2 + 10ϕωχ2i + 10ϕ2 ω 2
(χ2i )2
ω 2 χ2i + 2ϕω 3
ω4

6 − 3ε

ϕ2 χ2i

7−ε

ϕχ3i

8 − 2ε

χ4i

8−ε

ϕωχ2i + 6(χ2i )2

9 − 2ε

ωχ3i

10 − 2ε

ω 2 χ2i

8 − 3ε
8 − 2ε
10 − ε

Table 3. Toy model: all the 11 IR perturbations. The first 5 are Sn -preserving, the last 6 are
Sn -breaking. ∆a is the 1-loop mixing matrix element which encodes how Oa renormalizes itself.

perturbations Oa in operator space, while the eigenvalues define the correspondent 1-loop
scaling dimension as ∆a = d+λa . Here it is necessary to make a disclaimer. Our toy model
does not include operators with derivatives, which can mix with the operators of (7.11) (e.g.
the operator ϕ2 ω 2 may mix with ϕω∂ µ ϕ∂µ ϕ of the same scaling dimension, which was not
included in the toy Lagrangian (7.11)). In cases affected by such mixings, we do not expect
that our toy model computation will obtain the correct renormalized operators nor their
correct anomalous dimensions. (On the contrary in the serious calculations in section 9
and appendix H we were careful to take all possible mixings into account.) So in practice
the dimensions ∆a reported below should be only considered as a component of a mixing
matrix, which encodes how the operator Oa renormalizes itself. Only when Oa does not
mix with any other operators outside of (7.11), then we should expect that ∆a defines its
correct conformal dimension at 1-loop. In the end of the section we will come back to this
point. With this in mind, the result of the diagonalization of Mij is summarized in table 3.
This table lists 11 linear combinations of perturbations of the IR fixed point by quartic
operators without derivatives, which have well-defined anomalous dimensions (in our toy
model). What is their relation with the Sn symmetry? We know that the Sn -preserving directions form a 5-dimensional subspace U of the 11-dimensional space V11 of couplings. The
complementary directions should be classified as Sn -breaking. As the RG flow progresses,
U changes, “rotating” inside V11 in accordance with (B.8). However, the number of Sn preserving (and of Sn -breaking) directions is preserved along the RG flow. At the IR fixed
point U reaches a final form UIR , defining the 5 different Sn -preserving IR perturbations.
Any flow starting in the subspace U in the UV will approach the IR fixed point along a linear combination of these 5 directions. From this argument we expect that UIR has a basis of
operators with well-defined IR anomalous dimensions. Operators with well-defined IR di-

– 75 –

JHEP03(2021)219

∆a (1-loop)

## PDF page 79

∆a (1-loop)

Oa

6

σ4

8 − 3ε

σ22 + 2σ1 σ3

8 − 2ε

σ22 − 43 σ1 σ3

10 − ε

σ12 σ2

12 − 2ε

σ14

mensions which are not in UIR will span a complementary space denoted by ŪIR . So we have
V11 = UIR ⊕ ŪIR , where UIR is a 5-dimensional subspace of Sn -preserving IR perturbations,
and ŪIR is a complementary 6-dimensional subspace of Sn -breaking IR perturbations.
So, which directions are which? We claim that the Sn -preserving IR perturbations are
the first 5 entries of the table 3. To see this, we repeat the diagonalization exercise for the
β-functions (B.13) associated to the Sn couplings hi . When we diagonalize ∂hj βhi |h⋆ we
get 5 eigenvalues and eigenvectors given in table 4 (where we give Sn singlets to which the
5 eigencouplings couple).
The leader pieces of the singlets in table 4 exactly match the first 5 operators in table 3:
(σ4 )L = 6ϕ2 χ2i + 4ϕ3 ω ,
(σ22 + 2σ1 σ3 )L = (χ2i )2 + 10ϕωχ2i + 10ϕ2 ω 2 ,
4
(σ22 − σ1 σ3 )L = (χ2i )2 ,
3
(σ12 σ2 )L = ω 2 χ2i + 2ϕω 3 ,

(B.14)

(σ14 )L = ω 4 ,
and the values of ∆a in both tables 4 also agree. This proves the claim that the first
5 operators in table 3 are Sn invariant directions (and hence, by exclusion, the last 6
directions are Sn -breaking).
Let us now return to the problem of understanding which ∆a of tables 3 and 4 correspond to the actual 1-loop dimensions of the respective operator Oa . As we said above, this
happens when Oa does not mix with operators containing derivatives, since those operators
were not considered in (7.11). Let us consider this question for the Sn -invariant directions.
Are there additional Sn singlets producing leaders with the same number of fields, with
the same classical dimensions and the same symmetry properties (recall that susy-writable,
susy-null, and non-susy-writable leaders do not mix with each other66 )? Fortunately this
exercise is already done in appendix D, where the classification of all quartic operators with
dimensions ∆ ⩽ 12 is given. For our purpose it is enough to consider table 6. There, we see
one leader (χ2iµ )ϕ2 + . . . involving two derivatives, susy-writable and of classical dimensions
66

More precisely there is only triangular mixing, which does not affect scaling dimensions.

– 76 –

JHEP03(2021)219

Table 4. Toy model: the 5 Sn -preserving IR perturbations coming from the β functions (B.13)
linearized near the fixed point. ∆a is the 1-loop mixing matrix element which encodes how Oa
renormalizes itself.

## PDF page 80

C

Correspondence between correlators of χi and ψ, ψ̄

Consider first the Gaussian theory of n − 1 χi ’s subject to the constraint ni=2 χi = 0 and
∫
with the action S[χ] = − 12 dd xχi ∂ 2 χi (sum over repeated i’s implicit here and elsewhere
in this section, unless noted otherwise) and the Gaussian theory of Grassmann fields ψ, ψ̄
∫
with the action S[ψ, ψ̄] = − dd x ψ∂ 2 ψ̄. We can compute correlators from the partition
functions coupled to sources:67
∑

Zχ [Ji ] =

∫

¯ =
Zψ [J, J]

∫

Dχi e−S[χ]+
Dψ Dψ̄ e

∫

Ji χ i

−S[ψ,ψ̄]+

n−2

= Nχ (det ∂ 2 )− 2 exp
∫

¯ ψ̄
ψ J+J

1
2

( ∫

= Nψ (det ∂ ) exp
2

(∫

)

Kij Ji (∂ 2 )−1 Jj ,
)

2 −1 ¯

J(∂ )

J ,

(C.1)

1
where Kij = δij − n−1
Πij is the matrix appearing in (2.17). From here we get the χχ and
ψ ψ̄ propagators shown in (2.17) and (3.11).
As mentioned in section 2.5, the L0 theory defined in terms of χ field contains more
∑
operators than its ψ, ψ̄ counterpart LSUSY . E.g. operators of the form ′ χni do not have
any correspondent due to the Grassmann nature or ψ, ψ̄. Let us show that observable of
67

To do the first path integral it is convenient to represent the constraint
multiplier.

– 77 –

∑n
i=2

χi = 0 by a Lagrange

JHEP03(2021)219

8 (at d = 6), which can mix with (σ22 + 2σ1 σ3 )L (the second line of tables 3 and 4). There
are also three susy-writable operators with dimensions 10, that can mix with (σ12 σ2 )L . Finally, there are 2 susy-writable operators of dimensions 12 which can mix with (σ14 )L . The
value of ∆a for these three operators therefore should not be confused with their scaling
dimension. On the other hand, there are no operators which can mix with (σ4 )L and the
(susy-null) (σ22 − 43 σ1 σ3 )L , thus their dimension is indeed given by ∆a . We can easily check
that the result is correct: the anomalous dimension of (σ4 )L is the well-known one of φ̂4 of
the Wilson-Fisher fixed point, while (χ2i )2 gets no one-loop correction (see appendix H.2.1).
These computations represent a nice toy model to better understand our RG setup,
where Sn symmetry does not commute with rescaling. The final tables 3 and 4 show that by
diagonalizing the possible IR perturbations we get some directions which are Sn -preserving
while others are Sn -breaking. From table 3 we see that the Sn -preserving IR perturbations
are captured by the leaders of the correspondent Sn -singlets of table 4. Moreover table 3
exhibits other eigenperturbations, which are linear combinations of the followers and which
correspond to Sn -breaking directions, in agreement with the interpretation given in section 7.3. It is also important to notice that when two Sn -singlets have leaders of the
same classical dimension (e.g. σ22 and σ1 σ3 ), eigenperturbations are their particular linear combinations, which sometimes can be determined by looking at the leader type (e.g.
(σ22 − 43 σ1 σ3 )L = (χ2i )2 is the only susy-null linear combination at this dimension, so must
be an eigenperturbation). These observations illustrate the general algorithm proposed
in sections 7 and 8 to organize the spectrum of all the Sn -preserving IR perturbations.
Hopefully this discussion convinces the reader that the proposed organization principle is
indeed correct.

## PDF page 81

the χ-formulation which involve O(n−2) singlets, can be recovered from the ψ-formulation.
To this end we compute the path integrals with sources for bilinear operators inserted at
different points
Zχ [A(x, y)] =

∫

Zψ [A(x, y)] =

∫

1

Dχi e−S[χ]− 2

∫

χi (x)χi (y)A(x,y)

∫
1

DψDψ̄ e−S[ψ,ψ̄]− 2

n−2

= Nχ [det(−∂ 2 + A)]− 2 ,

(ψ(x)ψ̄(y)+ψ(y)ψ̄(x))A(x,y)

(C.2)

= Nψ det(−∂ 2 + A).

⟨ψ(x1 )ψ̄(x2 ⟩ + ⟨ψ(x2 )ψ̄(x1 )⟩ = ⟨χi (x1 )χi (x2 )⟩,

(C.3)

⟨(ψ(x1 )ψ̄(x2 ) + ψ(x2 )ψ̄(x1 )(ψ(x3 )ψ̄(x4 ) + ψ(x4 )ψ̄(x3 )⟩ = ⟨χi (x1 )χi (x2 )χj (x3 )χj (x4 )⟩.
We therefore obtain an equivalence map between bilocal operators of the two theories
Oχ (x, y) ←→ Oψ (x, y).
As a next step, we pass from bilocal to local operators. To this end we differentiate
an arbitrary number of times in x and in y and take a limit as y → x. This way we obtain
that any two bilinear local operators of this form are equivalent between the two theories:
(∂ (α) χi )(∂ (β) χi ) ←→ (∂ (α) ψ)(∂ (β) ψ̄) + (∂ (β) ψ)(∂ (α) ψ̄),

(C.4)

where (α), (β) are arbitrary collections of indices. E.g. (denoting derivatives ∂µ as ()µ etc)
χi χi,µ ←→ ψ ψ̄µ + ψµ ψ̄,
χi χi,µν ←→ ψ ψ̄µν + ψµν ψ̄,
χi,σ χi,ρµν ←→ ψσ ψ̄ρµν + ψρµν ψ̄σ ,

(C.5)

Finally we can extend this correspondence to products of bilinear operators, e.g.
χi χi,µν χj χj,ρσ −→ [ψ ψ̄µν + ψµν ψ̄][ψ ψ̄ρσ + ψρσ ψ̄].

(C.6)

However one should be careful of ambiguities which may arise at this level. E.g. we have
χi χi,µ χj χj,µ −→ [ψ ψ̄µ + ψµ ψ̄][ψ ψ̄µ + ψµ ψ̄] = 2ψ ψ̄ψµ ψ̄µ ,

1
χi χi χj,µ χj,µ −→ 2ψ ψ̄ψµ ψ̄µ ,
2

(C.7)

i.e. two different χ operators map to the same ψ operator, meaning that their difference is
susy-null.
This gives us a dictionary to map operators of the two theories. It is important to
stress that a large part of operators of the χ-theory is left out from the dictionary. Indeed

– 78 –

JHEP03(2021)219

Here A(x, y) = A(y, x) is a symmetric function. We consider the Gaussian actions S[χ],
S[ψ, ψ̄] but it is easy to introduce the coupling to ϕ via ∂ 2 → ∂ 2 + V ′′ (ϕ). We see that
the results coincide in the limit n → 0, discarding the overall normalization which cancels
in the computation of any correlator. By taking derivatives in A(x, y) it is straightforward
to see that all correlation functions of the bilocal operators Oχ (x, y) ≡ χi (x)χi (y) and
Oψ (x, y) ≡ ψ(x)ψ̄(y) + ψ(y)ψ̄(x) exactly match. For example

## PDF page 82

Singlet

Leader

σ2

[

σ12

Leader type

2ωϕ + χ2i ∆=4
[ω 2 ]∆=6
]

susy-writable
susy-writable

Table 5. Scalar Z2 -even leaders with Nφ = 2, Nder = 0.

(1)

⟨χi (1)χj (2)χk (3)χl (4)⟩ ̸= Tijkl ⟨ψ(1)ψ(2)ψ̄(3)ψ̄(4)⟩

(C.8)

(2)
(3)
+Tijkl ⟨ψ(1)ψ(3)ψ̄(2)ψ̄(4)⟩ + Tijkl ⟨ψ(1)ψ(4)ψ̄(2)ψ̄(3)⟩.

D

Tables of leaders up to ∆ = 12

D.1

Nφ = 2

The Nφ = 2 singlets are σ2 , σ12 , or derivative dressings thereof. These singlets are particularly simple for two reasons. First, they have well defined classical dimension when
expressed in the Cardy basis (see section 5.2). This means they give pure leaders (no
followers). Second, they involve at most two powers of χi , and so are susy-writable.
The Nφ = 2 singlets without derivatives are given in table 5. We will not write
explicitly the Nφ = 2 singlets with derivatives. One familiar such singlet is the kinetic
[
]
term σ2(µ)(µ) = 2∂ω∂ϕ + (∂χi )2 ∆=6 .
D.2

Nφ = 4

The Nφ = 4 leaders without derivatives were given in table 1.
Table 6 lists scalar Nφ = 4 leaders with Nder = 2 derivatives and dimension ∆ ⩽ 12.
(The Greek indices on ϕ, χi , ω denote partial derivatives: ϕµ = ∂µ ϕ, etc.) They arise from
7 singlets:
σ4(µ)(µ) ,

σ1(µ) σ3(µ) ,

σ1 σ3(µ)(µ) ,

2
σ2(µ)
,

σ2 σ2(µ)(µ) ,

2
σ2 σ1(µ)
,

σ12 σ2(µ)(µ) .

(D.1)

When classifying singlets involving derivatives, we make use of the equations of motion
(EOM) of the Gaussian part of the L0 Lagrangian (working in normalization H = 2):
∂ 2 ϕ = −2ω,

∂ 2 ω = ∂ 2 χi = 0,

– 79 –

(D.2)

JHEP03(2021)219

only O(n − 2) singlets with all indices repeated twice like χi χi,µν have a nice interpretation.
Sn−1 singlet operators with three or more χi carrying the same index cannot be represented
in terms of the fermionic variables. In the opposite direction, also a sector of the fermionic
theory cannot be represented in terms of the χ-theory. Indeed only the Sp(2) bilinear
singlets have meaning in the χ-theory, therefore operators of the form ψ, ψψµν , and so on,
do not have a representative. Moreover also in Sp(2) singlet sector only operators with
derivatives acting symmetrically on ψ and ψ̄ (see (C.4)) make sense in the χ-theory.
One could have hoped that the correspondence can be extended also to χ correlators
with indices non-contracted, at the expense of introducing tensorial coefficients. Sometimes
this can be done, but not in full generality. E.g. this fails for general 4-point functions, as
(I)
one cannot find tensorial coefficients Tijkl , I = 1, 2, 3, making the two sides of the following
equation agree (already in free theory):

## PDF page 83

Singlet

Leader

Leader type

σ4(µ)(µ)

susy-writable

σ2 σ2(µ)(µ)

[(χ2iµ )ϕ2 + 4(χi χiµ )ϕϕµ + (χ2i )ϕ2µ + 2ϕϕ2µ ω + 2ϕ2 ϕµ ωµ ]∆=8
[2(χi χiµ )ϕωµ + (χ2i )ϕµ ωµ + 2ϕϕµ ωωµ + ϕ2 ωµ2 ]∆=10
[(χ2iµ )ϕω + 2(χi χiµ )ϕµ ω + ϕ2µ ω 2 + 2ϕϕµ ωωµ ]∆=10
[(χi χiµ )2 + 12 (χ2i )(χ2iµ )]∆=10
[(χ2i )(χ2jµ ) + 2(χ2iµ )ϕω + 2(χ2i )ϕµ ωµ + 4ϕϕµ ωωµ ]∆=10

susy-writable

2
σ2 σ1(µ)

[(χ2i )ωµ2 + 2ϕωωµ2 ]∆=12

susy-writable

σ12 σ2(µ)(µ)

[(χ2iµ )ω 2 + 2ϕµ ω 2 ωµ ]∆=12

susy-writable

σ1(µ) σ3(µ)
σ1 σ3(µ)(µ)
1 2
48 ∂ F4

susy-writable
susy-writable
susy-null

which can be written equivalently as
∂ 2 φi = −2ω = −2σ1 .

(D.3)

This equation means that we never have to consider, in the replicated basis, the singlets (5.8) involving ∂ 2 φi , such as σk(µµ) . This explains their absence in (D.1).68
One particular linear combination of singlets (D.1) is equivalent, modulo EOM, to the
total derivative ∂ 2 F4 and has a susy-null leader ∂ 2 [(χ2i )2 ]. Indeed, applying eq. (C.4) to
the expression in table 6 we get zero:
1
(χi χiµ )2 + (χ2i )(χ2iµ ) → (ψ∂µ ψ̄ + ∂µ ψ ψ̄)2 + 2ψ ψ̄∂µ ψ∂µ ψ̄ = 0.
2

(D.4)

The other linear combination produce susy-writable leaders. Some of these, such as
(σ4(µ)(µ) )L and one linear combination of σ1(µ) σ3(µ) and σ1 σ3(µ)(µ) , are total derivatives
(modulo EOM) of the Nφ = 4 leaders without derivatives given in table 1. Others are new
primaries. We will not carry out the separation.
Now let us move to scalar Nφ = 4 leaders with Nder = 4 derivatives and dimension
∆ ⩽ 12. Without giving full expressions, the following 12 singlets:
σ4(µ)(µ)(ν)(ν) , σ4(µ)(ν)(µν) , σ4(µν)(µν) ,
σ1 σ3(µ)(ν)(µν) , σ1 σ3(µν)(µν) , σ1(ν) σ3(µ)(µ)(ν) , σ1(ν) σ3(µ)(µν) , σ1(µν) σ3(µ)(ν) , σ1(µν) σ3(µν) ,
σ2 σ2(µν)(µν) , σ2(µν) σ2(µ)(ν) , σ2(ν) σ2(µ)(µν)

(D.5)

give rise to manifestly susy-writable leaders (i.e. either at most quadratic in χ’s, or with
quartic in χ terms none of which vanish upon χ → ψ substitution).
68

This use of EOM is analogous to using the EOM when classifying fields at the Wilson-Fisher fixed
point [36, 38, 102, 103]. In the interacting theory, EOM get modified with a non-linear term appearing in
λ 3
the r.h.s.: ∂ 2 φi = −Hσ1 − 3!
φi . We can still classify fields modulo EOM because fields involving EOM only
have correlators at coincident points. Such fields correspond to redundant operators [23] and their scaling
dimensions do not influence RG stability of the theory; they also do not mix with the non-redundant fields.
So we can write any field involving ∂ 2 φi as a redundant operator (which we drop from consideration) plus
a field which does not involve ∂ 2 φi .

– 80 –

JHEP03(2021)219

1 2
2
Table 6. Scalar Z2 -even leaders with Nφ = 4, Nder = 2. 48
∂ F4 = σ2(µ)
−σ1(µ) σ3(µ) + 12 σ2 σ2(µ)(µ) −
σ1 σ3(µ)(µ) .

## PDF page 84

Singlet

Leader (+ First follower if susy-null)

Leader type

σ6

susy-writable

σ12 σ4

[15(χ2i )ϕ4 + 6ϕ5 ω]∆=8
[10(χ2i )ϕ3 ω + 5ϕ4 ω 2 ]∆=10
[6(χ2i )ϕ2 ω 2 + 4ϕ3 ω 3 ]∆=12

σ2 σ4 − 85 σ1 σ5

[6(χ2i )2 ϕ2 ]∆=10 + [4(χ2i )(χ3i )ϕ − 8(χ3i )ϕ2 ω]∆=11 susy-null

σ1 σ2 σ3 − 32 σ12 σ4

[3(χ2i )2 ϕω]∆=12 + [(χ2i )(χ3i )ω − 4(χ3i )ϕω 2 ]∆=13

σ1 σ5

susy-writable
susy-writable
susy-null

σ23 − 2σ1 σ2 σ3 + σ12 σ4 [(χ2i )3 ]∆=12 − [2(χ2i )(χ3i )ω]∆=13

susy-null
non-susy-writable

1
Table 7. Scalar Z2 -even leaders with Nφ = 6, Nder = 0. − 20
F6 = σ32 − 32 σ2 σ4 + 35 σ1 σ5 .

2
2
Three more singlets σ2(µν)
, σ2(µ)(ν)
, σ2(µ)(µ) σ2(ν)(ν) give rise to leaders containing at
least some quartic in χ terms vanishing upon χ → ψ substitution. An equivalent basis of
leaders (modulo EOM) is obtained by replacing these three singlets by the following total
derivatives combinations:

∂µ ∂ν [σ2 σ2(µν) ], ∂µ ∂ν [σ2 σ2(µ)(ν) ], (∂ 2 )2 F4 .

(D.6)

It can be verified that σ2 σ2(µν) and σ2 σ2(µ)(ν) have susy-writable leaders. To summarize,
at the Nφ = 4, Nder = 4 level with ∆ ⩽ 2 we have only one susy-null leader, and it is the
total derivative of (F4 )L .
Finally, all scalar leaders with Nφ = 4, Nder = 6 and dimension ∆ ⩽ 12 originate from
dressing σ4 with derivatives. They are all susy-writable.
D.3

Nφ = 6

Leaders with Nφ = 6 and Nder = 0 with ∆ ⩽ 12 arise from 7 singlets:
σ6 ,

σ 1 σ5 ,

σ12 σ4 ,

σ 2 σ4 ,

σ32 ,

(D.7)

σ23 .

σ 1 σ2 σ3 ,

Three of them are susy-writable. We also identify one susy-null linear combination of
dimension 10 and two SUSY-nulls of dimension 12. Finally, there is a non-susy-writable
leader of dimension 12, corresponding to the Feldman F6 operator. See table 7.
Moving to the Nφ = 6, Nder = 2 case, the following 5 singlets give rise to scalar
susy-writable leaders with ∆ ⩽ 12:
(D.8)

σ6(µ)(µ) , σ1(µ) σ5(µ) , σ1 σ5(µ)(µ) , σ2(µ)(µ) σ4 , σ3 σ3(µ)(µ) .

Three more singlets give ∆ ⩽ 12 leaders with some quartic in χ pieces which vanish upon
χ → ψ:
[

(σ2(µ) σ4(µ) )L = 3(χi χiµ )2 ϕ2 + 3(χ2i )(χi χiµ )ϕϕµ + susy-writable
[

(σ2 σ4(µ)(µ) )L = 4(χ2i )(χi χiµ )ϕϕµ + (χ2i )2 ϕ2µ + susy-writable
[

]
∆=12

]
∆=12

,

2
(σ3(µ)
)L = 4(χi χiµ )2 ϕ2 + 4(χ2i )(χi χiµ )ϕϕµ + (χ2i )2 ϕ2µ + susy-writable

– 81 –

(D.9)

,
]

∆=12

.

JHEP03(2021)219

[(χ3i )2 − 32 (χ2i )(χ4i )]∆=12

1
− 20
F6

## PDF page 85

Singlet

Leader (+ First follower if susy-null)

Leader type

σ8

[28(χ2i )ϕ6 + 8ϕ7 ω]∆=10
[21(χ2i )ϕ5 ω + 7ϕ6 ω 2 ]∆=12
[15(χ2i )2 ϕ4 ]∆=12 + [20(χ2i )(χ3i )ϕ3 − 20(χ3i )ϕ4 ω]∆=13

susy-writable

σ1 σ7
σ2 σ6 − 12
7 σ1 σ7

susy-writable
susy-null

Table 8. Scalar Z2 -even leaders with Nφ = 8, Nder = 0.

We can form two total derivative combinations including these singlets:

A third one ∂µ (σ2 σ4(µ) ) is linearly dependent with these two at the susy-null level. One
1 2 2
1 2
can also check that 13 ∂µ (σ3 σ3(µ) ) = 18
∂ (σ3 ) has the same susy-null part as 12
∂ (σ4 σ2 ).
Taking these into account, there remains exactly one susy-null singlet scalar at this level
which is not a total derivative, whose explicit expression is
4
1
2
σ3(µ)
− σ2(µ) σ4(µ) + σ1(µ) σ5(µ) = [(χ2i )2 ϕ2µ ]∆=12 + [follower]∆=13 + . . .
3
3

(D.11)

Finally, at Nφ = 6, Nder = 4 with ∆ ⩽ 12 we find only susy-writable leaders, obtained
from σ6 dressed with derivatives.
D.4

Nφ = 8, 10

Leaders with Nφ = 8 and Nder = 0 with ∆ ⩽ 12 arise from 5 singlets:
σ8 ,

σ 1 σ7 ,

σ 2 σ6 ,

σ 3 σ5 ,

σ42 ,

(D.12)

but there are only three independent leaders with ∆ ⩽ 12: two susy-writable and one
15
susy-null (table 8). This is because three linear combinations σ2 σ6 − 12
7 σ1 σ7 , σ3 σ5 − 7 σ1 σ7
2 2 4
and σ42 − 16
7 σ1 σ7 all have the same ∆ = 12 leading term (χi ) ϕ . Taking further differences
we could cancel this leading term and exhibit further leaders of higher dimensions. We will
not do it here since we are interested only in ∆ ⩽ 12.
The only scalar leader with Nφ = 8, Nder = 2 and ∆ ⩽ 12 comes from σ8(µ)(µ) , which
is equivalent to the total derivative ∂ 2 σ8 (modulo EOM and σ1 σ7 ).
There is only one ∆ ⩽ 12 leader with Nφ = 10, and it is susy-writable:
σ10 = [45(χ2i )ϕ8 + 10ϕ9 ω]∆=12 + . . .

E

(D.13)

Free L0 propagators

Propagators follow from (2.21), putting V (ϕ) = 0. The ϕ-ϕ and ω-ϕ propagators are
obtained by diagonalizing the quadratic terms containing ϕ and ω:
Gϕϕ (q) =

H
,
q4

Gωϕ (q) =

– 82 –

1
.
q2

(E.1)

JHEP03(2021)219

1
L
∂µ (σ4 σ2(µ) ) → (χi χiµ )2 ϕ2 + (χ2i )(χi χiµ )ϕϕµ + susy-writable,
(D.10)
12
1 2
L
∂ (σ4 σ2 ) → 4(χi χiµ )2 ϕ2 + 8(χ2i )(χi χiµ )ϕϕµ + (χ2i )2 ϕ2µ − 2(χ2i )2 ϕω + susy-writable.
12

## PDF page 86

Figure 11. (From left to right) Propagators Gϕϕ (p) [solid line], Gωϕ (p) [dotted half connects to
ω, solid to ϕ] and Gχi χj (p) [wavy line, indices i, j understood].
i=2 χi = 0;

∑n

(E.2)

where Πij = 1 for all i, j = 2, . . . , n. This computation is done either by realizing the
constraint by a Lagrange multiplier, or equivalently by eliminating one of the fields via the
constraint, and inverting the quadratic term for the remaining independent fields. E.g. by
∑
eliminating χ2 we get the quadratic action 12 ni,j=3 (∂µ χi )(δij + Πij )(∂ µ χj ) which gives the
above propagator.
In position space the propagators read
Gϕϕ (x) =
where Ad =

HAd
1
,
2(d − 4) (x2 ) d2 −2

Γ( d2 −1)2d−2
d

(4π) 2

Gωϕ (x) =

Ad
(x2 )

d
−1
2

,

Gχi χj (x) = Ad

Kij
d

(x2 ) 2 −1

,

(E.3)

. It is easy to check that ∂ 2 Gϕϕ = −HGωϕ consistently with the

equation of motion ∂ 2 ϕ = −Hω. When drawing Feynman diagrams, propagators are
denoted as in figure 11.
The matrix Kij satisfies some useful relations, which are easy to check:
K T = K,

K 2 = K,

tr K = n − 2,

n
∑

Kij = 0,

i=2
n
∑
i=2

Kij χi = χj ,

n
∑

Kij χm
i χj =

i,j=2

n
∑

χm+1
.
i

n
∑

Kij Kij = n − 2,

i,j=2

(E.4)

i=2

The last two relations follow using ni=2 χi = 0.
Our RG calculations will only involve the χi fields of the L0 theory. Some calculations
could be equivalently performed using the LSUSY theory. For completeness we give the corresponding propagators obtained by setting V = 0 in (2.27). The ϕ-ϕ and ϕ-ω propagators
are the same as for L0 , while the ψ̄-ψ one is
∑

Gψ̄ψ (x) = Gϕω (x) ,

(E.5)

in agreement with the general relation (2.31) for SUSY 2pt functions, be that free or
interacting. All individual propagators can be extracted from the superfield propagator
GΦΦ (x, θ) =

Ad
1
.
d − 4 (x2 − (4/H)θθ̄) d−4
2

– 83 –

(E.6)

JHEP03(2021)219

The χ-χ is obtained from the χ kinetic term, taking into account the constraint
it is given by:
Kij
1
Gχi χj (q) = 2 ,
Kij ≡ δij −
Πij ,
q
n−1

## PDF page 87

F

RG at one loop

Here µ is an arbitrary mass scale. We use dimensional regularization as the regulator.
We start by discussing renormalization of local operators in the theory L, and later use the
same principles for renormalization of λ. Renormalized operators Oi are related to the bare
operators OiB built from bare fields (B stands for “bare”), via a mixing (renormalization)
matrix Zij as follows:
OiB = Zij Oj .
(F.2)
While correlators of bare operators have poles in ε, renormalized operators Oj are defined
so that their correlation functions do not have such poles.
The matrix Zij admits an expansion in powers of 1/ε and λ, which at one loop as we
are interested here takes the form
Zij = δij +

λ
zij + . . . .
ε

(F.3)

It can be shown that the matrix zij has a simple block diagonal form, where each block
corresponds to operators with equal number of fields and the same classical dimension,
∆0i = ∆0j , where ∆0i is the bare dimension of Oi .
The anomalous dimension matrix is defined in terms of the Z matrix as follows:
Γ(λ) ≡ Z −1 .

d
Z.
d log µ

(F.4)

d
dZ dλ
∂λ
2
Then, by using d log
µ Z = dλ d log µ and βλ ≡ ∂ log µ = −ελ + O(λ ) (see below for the
discussion of the beta-function), we obtain a simple formula relating Γij and zij :

Γij (λ) = −λzij + O(λ2 ).

(F.5)

To compute the anomalous dimensions of operators at the fixed point, we should evaluate
the anomalous dimension matrix at the fixed point coupling: Γ ≡ Γ(λ∗ ).
Diagonalizing Γ one obtains the set of renormalized operators with well defined anoma∑ (m)
(m)
lous dimensions. Namely given an eigenvector e(m) such that i ei Γij = γm ei , one ob(
)
R = 1 + γm ∑ e(m) O B with anomalous dimension γ .
tains the renormalized operators Om
m
j j
j
ε
Sometimes it will happen for us that Γ is not fully diagonalizable, i.e. it has fewer
eigenvalues than its size. In this case we can still bring Γ to a Jordan normal form,
(1)
(r)
and define generalized eigenvectors ei , . . . ., ei associated to each eigenvalue γ, where

– 84 –

JHEP03(2021)219

In this section we will discuss how to set up RG computations of beta functions and
anomalous dimensions. To keep technical details to a minimum, we discuss renormalization
here at one loop, and then in appendix G at two loops. At one loop there is no wavefunction
renormalization, and we can think in terms of the free theory L(0) defined by setting V = 0
(
)
in (2.21), in d = 6 − ε dimensions and perturbed by scalar operator V = 4ωϕ3 + 6χ2i ϕ2
of dimension ∆0V = 6 − 2ε:
λ
L = L(0) + µε V.
(F.1)
4!

## PDF page 88

r is the rank of the corresponding Jordan block, which satisfy the Jordan chain prop∑ (k)
(k−1)
erty i ei (Γij − γ1) = (1 − δk1 )ei
. The associated renormalized operators OkR =
(
)
∑
(k) B
1 + γε
j ej Oj (k = 1, . . . , r) define a logarithmic multiplet which satisfies the property
⎛

OrR

⎞

⎛

⎞⎛

∆ 1

⎜
⎟
⎜
⎜
⎜ R ⎟
⎜ Or−1 ⎟
⎜
⎜
⎟
D⎜ . ⎟ = ⎜
⎜
⎜ .. ⎟
⎜
⎝
⎠
⎝

OrR

⎟⎜

⎞
⎟

⎟⎜ R ⎟
∆ 1
⎟ ⎜ Or−1 ⎟
⎟⎜
⎟
⎜ .. ⎟ ,
.. .. ⎟
⎟
⎜
. .
. ⎟
⎠⎝

O1R

O1R

(F.6)

⎠

F.1

OPE method

Another simplification which arises at one loop is that the RG functions can be quickly
computed using the OPE method, which we will review here. This is not obligatory and
the same results can be obtained with Feynman diagrams. The OPE method saves a lot of
time especially in situations when one has to disentangle mixing of many operators. Our
presentation of the OPE method mimics [36]. A classic reference for the OPE method
is [104], chapter 5 (although it uses a real-space cutoff, not dim.reg. like us).
We consider a correlation functions ⟨OiB (0) . . .⟩ of a bare scalar operator OiB with an
arbitrary number . . . of other operators. The leading order correction to this correlator can
be computed by expanding the functional integral (associated to the Lagrangian (F.1)) at
first order, and is given by
−

λµε
4!

∫

dd x⟨V(x)OiB (0) . . .⟩,

(F.7)

with d = 6 − ε. To renormalize Oi , we need to understand the 1/ε pole of this expression,
associated with the x → 0 part of the integration region. This is easy to do using the OPE
between the operators OiB and the interaction. The OPE takes the form
V(x) × OiB (0) =

∑

0

0

0

Ci,j |x|−∆V +∆i −∆j OjB (0)

(F.8)

j

(this form is adequate for the case when the operator OiB does not contain derivatives, see
below for the general case). This needs to be integrated for x near 0, say over |x| ⩽ 1,
the upper limit being arbitrary. For ∆0V = 6 − 2ε as we are considering, the integral
∫
−∆0V +∆0i −∆0j
d
gives a pole in ε as long as ∆0i − ∆0j = O(ε). It can be shown
|x|⩽1 d x |x|
similarly to [36] that a selection rule guarantees that all such operators with nonzero OPE
coefficients Ci,j have ∆0i = ∆0j .

– 85 –

JHEP03(2021)219

where D is the dilatation operator and ∆ = ∆0 + γ (where ∆0 is the classical dimension of
the operators which undergo mixing). The presence of logarithmic multiplets signals that
we are working in a logarithmic CFT. This is somewhat expected since we are studying
a theory with Sn symmetry in the limit n → 0 [40].

## PDF page 89

In our case the OPE matrix Ci,j also has selection rules between the three operator
classes:
V × susy-null = susy-null,
V × susy-writable = susy-writable + susy-null,

(F.9)

V × non-susy-writable = non-susy-writable + susy-writable + susy-null.

Oi = OiB + ε−1

λ∑
Ci,j Sd OjB ,
4! j

(F.10)

d/2

2π
where Sd = Γ(d/2)
denotes the area of the unit sphere in d dimensions. Inverting this
λ
relation, we obtain the matrix zi,j (F.3) as: zij = − 4!
Ci,j Sd .
By eq. (F.9), this matrix (and hence Z itself) has a block-triangular structure among
the three operator classes (susy-null, susy-writable, and non-susy-writable, in this order):

⎛

⎞

∗ 0 0⎟
⎜

Z = ⎜∗ ∗ 0⎟.
⎜
⎝

∗∗∗

(F.11)

⎟
⎠

Symmetry considerations from section 8.4 show that this structure should hold generally, at any number of loops. Furthermore, the same block-triangular structure in inherited
by the anomalous dimension matrix (F.4).
The above explains the general idea, up to the need to generalize eq. (F.8) a bit when
considering operators containing derivatives. The more general expression used in our
computations is
V(x) × OiB (0)

∼

∑

Ci,k

x µ1 . . . x µℓ

k

0

|x|∆V +ℓk

(Tk )µ1 ...µℓk (0) ,

(F.12)

where (Tk )µ1 ...µℓj is a tensor of rank ℓk (not necessarily traceless) and of dimension ∆0k = ∆0i .
The OPE coefficient function is now a tensorial function of scaling −∆0V , and it will give
an ε pole when integrated near x = 0, projecting the operator Tk on its scalar component
(see below).
Let us give an example of how (F.12) works. If we consider the OPE of OiB = ϕω
we find 3 possible operators Tk with the same dimension of OiB : the two scalars ϕω, χ2i
and the rank-2 tensor operator ∂ µ1 ∂ µ2 ϕ2 . The scalars are the remaining operators after
we take two Wick contractions of fields in Oi and in V,
(

)

4ωϕ3 + 6χ2i ϕ2 (x)×ϕω(0) ∼ 6×2⟨ϕϕ⟩0 ⟨ϕω⟩0 χ2i (0) +4×6⟨ϕϕ⟩0 ⟨ϕω⟩0 ϕω(0) +. . . (F.13)

– 86 –

JHEP03(2021)219

I.e. OPE of V with a susy-null operator produces only susy-null operators in the r.h.s.,
etc. These rules follow by the symmetry considerations as in the mixing discussion in
section 8.4.
Going back to eq. (F.8), it implies that any correlator ⟨OiB (0) . . .⟩ has poles in ε
proportional to λ⟨OjB (0) . . .⟩. The renormalized operators are defined by correcting OiB to
cancel these poles. We see that this can be achieved by

## PDF page 90

Here the factor 2 in the first term and 6 in the second, are the combinatorial factors which
count the possible Wick contractions. We use the notation ⟨. . .⟩0 to denote the 2-point
functions of L(0) . Since it is free, we have simply ⟨ϕω⟩0 = ⟨ϕ(x)ω(0)⟩0 = ⟨ϕ(0)ω(x)⟩0 =
Gωϕ (x) and ⟨ϕϕ⟩0 = Gϕϕ (x). The 2-tensor operator arises from the following OPE:
(

)

4ωϕ3 + 6χ2i ϕ2 (x) × ϕω(0) ∼ 4 × 3⟨ϕω⟩0 ⟨ϕω⟩0 ϕ2 (x) + . . .
= 4 × 3⟨ϕω⟩0 ⟨ϕω⟩0

x µ1 x µ 2
∂µ2 ∂µ2 ϕ2 (0) + . . .
2

(F.14)

∫

(d)

(d)

dΩ x̂µ1 . . . x̂µℓ = Pℓ δ (µ1 µ2 . . . δ µℓ−1 µℓ ) Sd ,

(F.15)

(d)

where P2ℓ = 2(2ℓ−1)!!
ℓ (d/2) , P2ℓ+1 = 0 and the brackets imply symmetrization of the indices.
ℓ
After performing these integrals we are left with a product of Kronecker deltas contracted with the tensor operators, i.e. scalars. E.g. the operator ∂µ2 ∂µ2 ϕ2 (0) of (F.14)
after integration is contracted with δ µ1 µ2 and becomes equal to ∂ 2 ϕ2 = 2∂ϕ∂ϕ + 2ϕ∂ 2 ϕ =
2∂ϕ∂ϕ − 2Hϕω. More generally we want to write the contraction of (Tk )µ1 ...µℓ with δ µν ’s
in (F.15) in terms of the scalar operators OiB that we want to study. We write these as
δ (µ1 µ2 . . . δ µℓ−1 µℓ ) (Tk )µ1 ...µℓ =

∑ (k)
nj OjB (0),

(F.16)

j
(k)

where the above formula can be read as a definition for the coefficients nj .
Putting these ingredients together, we rewrite the integral of the k-th operator in (F.12)
ε
(up to the overall factor − λµ
4! Ci,j ) as follows,
∫

dd x

x µ1 . . . x µℓ
|x|

∆0V +ℓ

1 (d) ∑ (k) B
⟨(Tk )µ1 ...µℓ (0) . . .⟩ = Pℓk Sd
nj ⟨Oj (0) . . .⟩.
ε
j

(F.17)

This shows how one should generalize (F.10). From here we obtain a final formula for zij ,
and therefore for the 1-loop anomalous dimensions matrix,
Γij (λ) =

λ ∑ (d)
(k)
Sd
Pℓk Ci,k nj .
4!
k

(F.18)

Given the block-triangular structure (F.11) with respect the three operator classes, only
diagonal blocks of this matrix matter for the purposes of computing the anomalous dimensions. The off-diagonal blocks do influence the eigenperturbations (e.g. scaling susywritable operators will have an admixture of susy-nulls), but do not modify the eigenvalues.

– 87 –

JHEP03(2021)219

In this case the tensor structure is obtained by Taylor expanding the remaining field ϕ2 of
V(x), keeping only the second order term since it gives a field of the same dimensions as
ϕω (others do not produce poles in ε when integrated near x = 0).
When integrating (F.12) over x, we have to deal with tensorial integrals. E.g. after
∫
0
using (F.14) we are led to an integral of the form |x|⩽1 dd x |x|−∆V −2 xµ1 xµ2 , whose pole
part is easily seen equal to ε−1 Sd δ µ1 µ2 /d by rotation invariance. For general ℓ we have:

## PDF page 91

F.2

Beta function

One can also compute beta function of the coupling λ with the OPE approach. Once again
λ
Feynman diagrams will give the same result. Consider the interaction in (F.1) with µε 4!
λB
replaced by 4! . We should find a relation between the bare and renormalized couplings,
λB and λ of the form,70
λB = µε Zλ λ,
(F.19)
which removes poles in ε when everything is expressed in terms of λ. Here at leading order
Zλ = 1 + λ/ε. Note that the wavefunction renormalization of fields ϕ, ω and χ starts at
O(λ2 ), see the next section. Now take any correlator ⟨A⟩ where A is a product of some
fields. Consider its first and second order corrections, which are given below:
−

λB
4!

∫

dd x⟨V(x)A⟩ +

1
2

(

λB
4!

)2 ∫

dd x

∫

dd y⟨V(x + y)V(x)A⟩.

(F.20)

The second term will have an ε pole due to the singularity as y → 0. We choose Zλ such
that this pole is canceled by the first term. For this we consider the OPE (we can do this
69

This is obvious, by differentiating the OPE of the parent operator.
Strictly speaking we should treat the two vertices ϕ3 ω and ϕ2 χ2 differently. If their coupling constants
(1)
(2)
(1)
(1)
(2)
(2)
are λB and λB respectively, we should write λB = Zλ λ(1) and λB = Zλ λ(2) . However as commented
(1)
(2)
(1)
(2)
later, when λB = λB it turns out Zλ = Zλ .
70

– 88 –

JHEP03(2021)219

Furthermore, while using equation (F.18) we will encounter operators that will be
related to one another by addition of a total derivative. Perturbing the action by an
integral of a total derivative of course has no effect on physics since the integral vanishes.
This can be also expressed by saying that under RG, total derivatives may generate only
total derivatives. In the OPE formalism this manifests itself as the fact that when we take
the OPE of V with a total derivative operator, only total derivatives occur in the r.h.s. 69
These observations can be used to simplify the computations of anomalous dimensions, as
follows. We will say that two operators O and O′ belong to the same equivalence class
{O} if they are proportional up to adding a total derivative, i.e. O′ = αO + ∂ µ Õµ for
some constant α and operator Oµ . For each {Oi } we will choose a single representative
element Oi while all other elements can be written in terms of Oi by adding a suitable
total derivative. Eg. in the equivalence class {ω 2 } we have an operator O = ω 2 , and also
another operator O′ = ∂ µ ϕ∂µ ω = Hω 2 + ∂ µ (ω∂µ ϕ), which we can see can be written in
terms of O by using equation of motion and adding a total derivative.
Replacing operators by their equivalence classes (picking one representative in each
class), we eliminate total derivative operators from the problem and get a smaller eigenvalue
system to solve, which however gives rise to the same anomalous dimension for the nontotal-derivative operators as the full system. In some cases one may be interested to recover
in each equivalence class a primary, i.e. an operator which has good scaling behavior under
RG, including the total derivative part, and has zero 2-point functions with other primaries.
The problem of finding such a scaling operator is harder, and to solve it one has to work
with the full operators, not with the equivalence classes, i.e. to diagonalize the full matrix Γ.

## PDF page 92

for x = 0 by translational invariance):
ϕ3 ω(y) × ϕ3 ω(0) ∼ 36⟨ϕω⟩0 ⟨ϕϕ⟩0 ϕ3 ω(0) + . . .

(F.21)

The product ⟨ϕω⟩0 ⟨ϕϕ⟩0 gives a pole in ε when integrated over y near 0. Plugging this
into (F.20) and demanding the cancellation we get
Zλ = 1 +

3λH
.
(4π)3 ε

(F.22)

0=

∂ log λB
∂
3H
1
=
[log (µε Zλ λ)] = ε +
βλ + βλ ,
∂ log µ
∂ log µ
(4π)3 ε
λ

from where
βλ = −ελ +

(F.23)

3Hλ2
+ O(λ3 ) .
64π 3

(F.24)
3

ε
2
This is the beta function (3.6) of our theory. It gives a fixed point at λ∗ = 64π
3H + O ε .
2
2
We can also consider the OPEs that generate χi ϕ . It will give rise to the same Zλ
and the same beta function. This can be seen a consequence of the O(n) symmetry in
n → 0 limit, or of the hidden supersymmetry which becomes manifest in the form (2.27)
that we get from (2.21) once we substitute χi with ψ, ψ̄ using (
(2.26).
)
We could also discuss renormalization of the mass term m2 ϕω + 12 χ2i in the same
language. This term renormalizes as a whole for the same reasons. This matches nicely
with the fact that to reach the critical point (phase transition) we have to tune a single
parameter (m2 ).

G

( )

RG at two loops

After one-loop RG in appendix F, here we set up the more general scheme valid at any loop
order. In practice we will go to the maximum of two loops in some anomalous dimension
computations for which the one-loop result vanishes. The regulator will be the same as in
appendix F (dim. reg.). The OPE method losing its simplicity beyond one loop, here we
will be using instead Feynman diagram to extract poles in ε. We are assuming the reader is
somewhat familiar with dimensionally regulated computations for the Wilson-Fisher fixed
point (see e.g. a nice review in [105]), to which our case is rather similar.
We will present the setup for computations in terms of the fields χi , Although susywritable computations can be done (and even become easier) in terms of ψ, ψ̄, we need the
general setup for computations of anomalous dimensions of susy-null and non-susy-writable
operators.
G.1

Beta function

We start with Lagrangian (2.22) with zero mass term and all quantities set to their bare
values:
)
H 2
1
λB (
L0 = ∂ϕB ∂ωB − ωB
+ (∂χB )2 +
4ωB ϕ3B + 6χ2B ϕ2B .
(G.1)
2
2
4!

– 89 –

JHEP03(2021)219

∂λ
The beta function βλ ≡ µ ∂µ
can then be obtained using that the bare coupling does not
depend on µ:

## PDF page 93

The bare quantities are related to the renormalized ones by:
ϕB = Zϕ ϕ,

ωB = Zω ω,

χB = Zχ χ,

λB = Zλ µε λ.

(G.2)

where Zi are renormalization constants, and µ is an arbitrary mass scale. Correlators of
renormalized fields ϕ, ω, χ have to be free of poles in ε when expanded in the renormalized
coupling dimensionless coupling λ. Compared to appendix F we are adding wavefunction
renormalization constants Zϕ , Zω , Zχ , necessary beyond one loop.
Plugging (G.2) into (G.1) we get:
)
H 2 Zχ2
Zλ µε λ ( 3
ω +
(∂χi )2 +
4Zϕ Zω ωϕ3 + 6Zχ2 Zϕ2 χ2i ϕ2 . (G.3)
2
2
4!

In the Minimal Subtraction (MS) scheme, the renormalization constant Zλ takes the
form:
∑ ∑ (p,q)
Zλ = 1 +
zλ λp ε−q .
(G.4)
p⩾1 1⩽q⩽p

(compare to (F.3)). The quantities Zϕ , Zω , Zχ have similar expansions, except that the
corresponding z (1,1) vanishes (see appendix G.2).
Let us use this formalism to re-compute the one-loop beta function (two-loop beta
function is not needed in this paper). We will consider the momentum-space 4-point
function ⟨ϕ(p1 )ϕ(p2 )ϕ(p3 )ϕ(p4 )⟩ and the condition that it should be free of poles in ε will
(1,1)
determine zλ . At tree level this 4-point function involves a single ωϕ3 vertex. At one
loop, we have the first diagram in figure 12 (and two diagrams for the crossed channels).
Factoring out the trivial dependence on the external momenta coming from the propagators
on the external legs, we get the amputated 4-point function
⟨ϕ(p1 )ϕ(p2 )ϕ(p3 )ϕ(p4 )⟩amp = Zλ µε λ + (Zλ µε λ)2 Iωϕ3 ,

(G.5)

where we have set the wavefunction renormalization constants to 1, and Iωϕ3 is the one-loop
integral
∫
H
dd l
Iωϕ3 = −
+ (t,u channels) ,
(G.6)
(2π)d
(l2 )2 (p1 + p2 + l)2
having an ε−1 pole which we need to cancel. This ε-pole is extracted in the usual way (we
need the UV ε-pole, and the external momenta propagating through the loop serve as a
IR regulator). Omitting these standard details (see e.g. [105]), we get
Iωϕ3 = −

( )
3H
+
O
ε0 .
(4π)3 ε

(G.7)

Note that while the finite piece of Iωϕ3 has nontrivial dependence of the external
momenta, the pole is p-independent so we can cancel it against the tree level contribution
in (G.5). This determines
3λH
Zλ = 1 +
,
(G.8)
(4π)3 ε
the same result as in the previous section. Hence we get the same beta function (F.24).

– 90 –

JHEP03(2021)219

L0 = Zϕ Zω ∂ϕ∂ω − Zω2

## PDF page 94

p2

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

p3

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p2

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

l

p3

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

p4

l
<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p3

➤
➤

p1

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

p4
<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

➤

l + p 1 + p2

p1

<latexit sha1_base64="RHk4ZDbIqLzjaLep82iWlLhFClE=">AAAB8HicbVBNSwMxEJ2tX7V+VT16CRZBEMpuEfRY9OKxgv2QdinZNNuGJtmQZIWy9Fd48aCIV3+ON/+NabsHbX0w8Hhvhpl5keLMWN//9gpr6xubW8Xt0s7u3v5B+fCoZZJUE9okCU90J8KGciZp0zLLaUdpikXEaTsa38789hPVhiXywU4UDQUeShYzgq2THvmF6geuav1yxa/6c6BVEuSkAjka/fJXb5CQVFBpCcfGdANf2TDD2jLC6bTUSw1VmIzxkHYdlVhQE2bzg6fozCkDFCfalbRorv6eyLAwZiIi1ymwHZllbyb+53VTG1+HGZMqtVSSxaI45cgmaPY9GjBNieUTRzDRzN2KyAhrTKzLqORCCJZfXiWtWjVw/P6yUr/J4yjCCZzCOQRwBXW4gwY0gYCAZ3iFN097L96797FoLXj5zDH8gff5A5MWj5c=</latexit>

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

p4

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

➤

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

l − p 2 − p3

p1

<latexit sha1_base64="jTOppr4p+7a7HCC+UFUEf/5KA8A=">AAAB8HicbVBNSwMxEJ31s9avqkcvwSJ4sexWQY9FLx4r2A9pl5JNs21okg1JVihLf4UXD4p49ed489+YtnvQ1gcDj/dmmJkXKc6M9f1vb2V1bX1js7BV3N7Z3dsvHRw2TZJqQhsk4YluR9hQziRtWGY5bStNsYg4bUWj26nfeqLasEQ+2LGiocADyWJGsHXSIz9Xvaqri16p7Ff8GdAyCXJShhz1Xumr209IKqi0hGNjOoGvbJhhbRnhdFLspoYqTEZ4QDuOSiyoCbPZwRN06pQ+ihPtSlo0U39PZFgYMxaR6xTYDs2iNxX/8zqpja/DjEmVWirJfFGccmQTNP0e9ZmmxPKxI5ho5m5FZIg1JtZlVHQhBIsvL5NmtRI4fn9Zrt3kcRTgGE7gDAK4ghrcQR0aQEDAM7zCm6e9F+/d+5i3rnj5zBH8gff5A5xGj50=</latexit>

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

p2

Figure 12. The Feynman diagrams for the one-loop renormalization of λ. The first diagram
corrects ⟨ϕ(p1 )ϕ(p2 )ϕ(p3 )ϕ(p4 )⟩, while the other two would arise for ⟨χj (p1 )χj (p2 )ϕ(p3 )ϕ(p4 )⟩.
l1
<latexit sha1_base64="berNMFBEL75BVbf5uEM+UZJp20k=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9SD6ft+tejVvLrIKfgFVKNTou1+9QcKyGKVhgmrd9b3UBDlVhjOB00ov05hSNqZD7FqUNEYd5PNVp+TMOgMSJco+acjc/T2R01jrSRzazpiakV6uzcz/at3MRNdBzmWaGZRs8VGUCWISMrubDLhCZsTEAmWK210JG1FFmbHpVGwI/vLJq9C6qPmW7y+r9ZsijjKcwCmcgw9XUIc7aEATGAzhGV7hzRHOi/PufCxaS04xcwx/5Hz+APlbjZQ=</latexit>

l 1 + l2 + p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

l 1 + l2 + p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="q6cdWaXpGEW65xQWCh/I17uIx/U=">AAAB8HicbZDLSgMxFIbP1Futt6pLN8EiCIUyUwq6LLpxWcFepB2GTJppQ5PMkGSEMvQp3LhQxK2P4863MW1noa0/BD7+cw455w8TzrRx3W+nsLG5tb1T3C3t7R8cHpWPTzo6ThWhbRLzWPVCrClnkrYNM5z2EkWxCDnthpPbeb37RJVmsXww04T6Ao8kixjBxlqPPPCqPKhXk6BccWvuQmgdvBwqkKsVlL8Gw5ikgkpDONa677mJ8TOsDCOczkqDVNMEkwke0b5FiQXVfrZYeIYurDNEUazskwYt3N8TGRZaT0VoOwU2Y71am5v/1fqpia79jMkkNVSS5UdRypGJ0fx6NGSKEsOnFjBRzO6KyBgrTIzNqGRD8FZPXodOveZZvm9Umjd5HEU4g3O4BA+uoAl30II2EBDwDK/w5ijnxXl3PpatBSefOYU/cj5/AIzMj5M=</latexit>

➤

➤

<latexit sha1_base64="q6cdWaXpGEW65xQWCh/I17uIx/U=">AAAB8HicbZDLSgMxFIbP1Futt6pLN8EiCIUyUwq6LLpxWcFepB2GTJppQ5PMkGSEMvQp3LhQxK2P4863MW1noa0/BD7+cw455w8TzrRx3W+nsLG5tb1T3C3t7R8cHpWPTzo6ThWhbRLzWPVCrClnkrYNM5z2EkWxCDnthpPbeb37RJVmsXww04T6Ao8kixjBxlqPPPCqPKhXk6BccWvuQmgdvBwqkKsVlL8Gw5ikgkpDONa677mJ8TOsDCOczkqDVNMEkwke0b5FiQXVfrZYeIYurDNEUazskwYt3N8TGRZaT0VoOwU2Y71am5v/1fqpia79jMkkNVSS5UdRypGJ0fx6NGSKEsOnFjBRzO6KyBgrTIzNqGRD8FZPXodOveZZvm9Umjd5HEU4g3O4BA+uoAl30II2EBDwDK/w5ijnxXl3PpatBSefOYU/cj5/AIzMj5M=</latexit>

➤

p

l2

l2

<latexit sha1_base64="YTO6seXZu7zHYbj3se5C6PKcvho=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz3IQW1QrrhVdyGyDl4OFcjVHJS/+sOYpRFXyCQ1pue5CfoZ1SiY5LNSPzU8oWxCR7xnUdGIGz9brDojF9YZkjDW9ikkC/f3REYjY6ZRYDsjimOzWpub/9V6KYbXfiZUkiJXbPlRmEqCMZnfTYZCc4ZyaoEyLeyuhI2ppgxtOiUbgrd68jq0a1XP8v1VpXGTx1GEMziHS/CgDg24gya0gMEInuEV3hzpvDjvzseyteDkM6fwR87nD/rfjZU=</latexit>

<latexit sha1_base64="YTO6seXZu7zHYbj3se5C6PKcvho=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz3IQW1QrrhVdyGyDl4OFcjVHJS/+sOYpRFXyCQ1pue5CfoZ1SiY5LNSPzU8oWxCR7xnUdGIGz9brDojF9YZkjDW9ikkC/f3REYjY6ZRYDsjimOzWpub/9V6KYbXfiZUkiJXbPlRmEqCMZnfTYZCc4ZyaoEyLeyuhI2ppgxtOiUbgrd68jq0a1XP8v1VpXGTx1GEMziHS/CgDg24gya0gMEInuEV3hzpvDjvzseyteDkM6fwR87nD/rfjZU=</latexit>

Figure 13 Two- oop correct ons to ⟨ϕ(p)ω(−p)⟩ and ⟨χ (p)χj (−p)⟩ ( abe s i j om tted)

p

+

+p

p

p

+

+p

p

Figure 14 Two- oop correct ons to ⟨ϕ(p)ϕ(−p)⟩

Alternatively we could consider ⟨χj (p1 )χj (p2 )ϕ(p3 )ϕ(p4 )⟩. At one loop we have the last
two diagrams in figure 12. Here too, at one-loop the dependence on the external momenta
and i, j indices is proportional to that in tree level, but now involving the other vertex χ2 ϕ2 .
(1 1)
The amputated function once again gives the same correction zλ . This can be seen as a
consequence of the equivalence of (2.21) with the SUSY theory (2.27). We omit the details.
G.2

Wavefunction renormalization

Here we will calculate the wavefunction renormalization constants Zϕ , Zω , Zχ , which get
the first correction at two loops (we will need it in our two-loop anomalous dimension
computations). These renormalization constants are determined by requiring the 2-point
functions ⟨ϕ(p)ω(−p)⟩, ⟨ϕ(p)ϕ(−p)⟩ and ⟨χ (p)χj (−p)⟩ be free of ε poles. These 2-point
functions receive two-loop corrections shown in figures 13 and 14.
These loop integrals are similar to the usual Wilson-Fisher two-loop field renormalization integral [105]. One integral common to all corrections is:
Iϕω (p2 ) =

λ2 H 2
(2π)2d

∫ ∫

( )
dd l1 dd l2
λ 2 H 2 p2
=
−
+
O
ε0 .
6(4π)6 ε
(l12 )2 (l22 )2 (p + l1 + l2 )2

(G.9)

For the correction to ⟨ϕ(p)ϕ(−p)⟩ we have an extra integral:
λ2 H 2
Iϕϕ =
(2π)2d

∫ ∫

dd l1 dd l2
=
2
2
(l1 )2 (l2 )2 ((p + l1 + l2 )2 )2

– 91 –

−

( )
λ2 H 2
+
O
ε0 .
2(4π)6 ε

(G.10)

JHEP03(2021)219

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

## PDF page 95

Putting in the appropriate symmetry factors, we obtain the following two-loop corrected
2-point functions (where we keep Zϕ , Zω , Zχ at tree level but set them to one in the correction):
(
)
1
1
λ2 H 2
2 0
⟨ϕ(p)ω(−p)⟩ = 2
−
+
O
λ
ε
,
p Zϕ Zω
12(4π)6 ε
[

]

(
)
1 1
λ2 H 2
⟨χi (p)χj (−p)⟩ = 2
−
+ O λ2 ε0 ,
2
6
p Zχ 12(4π) ε
[

]

(G.11)

(
)
H
1
λ2 H 2
2 0
⟨ϕ(p)ϕ(−p)⟩ = 2 2
−
+
O
λ
ε
.
(p ) Zϕ2
12(4π)6 ε
[

]

Zϕ Zω = Zϕ2 = Zχ2 = 1 −

λ2 H 2
+ O(λ3 ).
12(4π)6 ε

(G.12)

Thus we find Zϕ = Zω = Zχ . In particular Zϕ = Zω can be interpreted as the nonrenormalization of H. Recall that our theory is equivalent to the supersymmetric theory (2.27), and H is a parameter in the SUSY transformations. As commented in section 3.1, dimensional regularization preserves full SUSY and hence H. (In section 7.1 we
instead discussed that in other regularization schemes H can renormalize, using a slightly
different notation for wavefunction renormalization constants, see eq. (7.2).)
Finally, from Zϕ , Zω , Zχ by the usual definitions we compute the anomalous dimensions
of the fields:
[
]
( )
∂ log Zϕ
ε2
γϕ = γω = γχ =
=
+ O ε3 ,
(G.13)
∂ log µ λ=λ∗
108
equal to γφ̂ at the usual Wilson-Fisher fixed point, consistently with the dimensional reduction.

H

Details of anomalous dimension computations

In this appendix we will show the details of the anomalous dimension computations presented in section 9. Throughout this section we will denote by γO = ∆O −∆0O the anomalous
dimension for an operator O, where ∆O is the dimension of O at the fixed point (3.7) and
∆0O is its dimension at the Gaussian (free theory) fixed point at d = 6 − ε.
Recall that the three operator classes have the block-diagonal mixing structure shown
in (F.11), which allows to compute anomalous dimensions in each class separately (although
the true scaling susy-writable operators will have an admixture of susy-nulls, while nonsusy-writables will have an admixture of both susy-writables and susy-nulls). We will try
to remind the reader of that whenever a confusion might arise.
H.1

Susy-writable operators

As explained in section 8.3, susy-writable operators have well-defined anomalous dimensions equal to the ones of the Wilson-Fisher (WF) in d = 4 − ε dimensions. Here we give a

– 92 –

JHEP03(2021)219

Requiring that ε poles cancel determines:

## PDF page 96

(Φ2 T µµ )θθ̄ +

15 2 2
(χ ) .
26

(H.1)

As we explain in the main text, the only susy-writable operator which may play an important role in destabilizing the susy RG is the so called box superfield B ab,cd , which transforms
in the (2, 2) representation of OSp(d|2) (recall that unitarity bounds for this representation
are too weak to ensure that the operator is irrelevant). Its WF counterpart is defined in
the main text as
(
)Y
2dˆ
2
B̂µν,ρσ = φ̂,µν φ̂,ρσ φ̂ −
φ̂,µ φ̂,ν φ̂,ρσ φ̂
.
(H.2)
dˆ − 2
The anomalous dimension of (H.2) was computed in [38] and it equals (7/9)ε. We would like
to reproduce this result by studying the superfield B ab,cd . This is a very non-trivial check
that dimensional reduction works also for operators in non-trivial OSp(d|2) representations.
While doing so, we will also show the explicit expression in components for this operator.
We mainly focus on (B θθ̄,θθ̄ )θθ̄ , since this component is bosonic, supertranslation invariant (it is the highest component of a superfield) and it is a scalar with respect to SO(d).
Because of these features, this operator is generated in our RG flow and could destabilize
it (if it becomes relevant).
ˆ Young symmetrizer denoted by Y in (H.2). This is
First let us spell out the SO(d)
a tensor with two sets of four indices, each set transforming in the SO( ˆ
d) representation
(2, 2). By contracting the indices µνρσ inside the brackets of (H.2) with one set, we obtain
an operator depending on the second set of indices, which transforms properly in the (2, 2)

– 93 –

JHEP03(2021)219

few examples of such operators and their anomalous dimensions. In this section we work
at one loop and the reported computations have been performed using the OPE formalism
from appendix F.
In our computations we used the χ-formulation, but in the discussions and in the
comparison with WF it is also convenient to use the superfields. The superfield formulation
by construction misses all contributions proportional to susy-null operators, which are
instead non-vanishing in the χ-formulation. As already mentioned several times, susynull operators cannot generate susy-writables under RG (while the opposite may happen),
so that their mixing matrix is triangular, which ensures that anomalous dimensions of
susy-writable operators can be computed by setting to zero susy-null contributions. In
the following we will use this shortcut. We will be also able to recover the susy-null
contributions by asking that the complete operator is an eigenperturbation.
Let us start by considering the operators (Φ2 )θθ̄ , Tθµµ
, ∂ 2 (Φ2 )θθ̄ , (Φ4 )θθ̄ , (Φ2 T µµ )θθ̄
θ̄
discussed in the main text. As a first step we rewrite all terms involving ψ, ψ̄ using the
χ-formulation (see appendix C). It is then easy to check that the anomalous dimensions
of these operators are respectively equal to ε/3, 0, ε/3, 2ε, (13/9)ε, as expected from the
WF counterpart [38].
We can further study if some susy-null contributions should be added. It is easy to
check that the first four operators above do not get modified by susy-null terms. On
the other hand the last operator is an eigenpertubation only when we add to it a term
proportional to (χ2 )2 , namely

## PDF page 97

irrep. It is convenient to represent the symmetrizer (see [106–108]) by contracting its eight
indices with auxiliary Rdˆ vectors — the symmetric indices in each row are contracted with
the same vector. The first set is contracted with X1 and X2 , while the second set with Z1
and Z2 . The result is expressed in the following polynomial form:
Π2,2 (X1 , X2 ; Z1 , Z2 ) = c2,2 −(X1 · X1 )(Z1 · Z1 )(X2 · Z2 )2 − 2(X1 · X2 )2 (Z1 · Z2 )2
{

+ 2(X1 · X1 )(Z1 · Z2 )(X2 · Z1 )(X2 · Z2 ) + 2(X1 · X1 )(X2 · X2 )(Z1 · Z2 )2
+ 2(X1 · X2 )2 (Z1 · Z1 )(Z2 · Z2 ) − 2(X1 · X1 )(X2 · X2 )(Z1 · Z1 )(Z2 · Z2 )
− 2(dˆ− 1)(X2 · X2 )(Z1 · Z2 )(X1 · Z1 )(X1 · Z2 ) + 2(dˆ− 1)(X1 · X2 )(Z1 · Z2 )(X1 · Z2 )(X2 · Z1 )
+ 2(dˆ− 1)(X1 · X2 )(Z1 · Z2 )(X1 · Z1 )(X2 · Z2 ) + (dˆ− 1)(X2 · X2 )(Z2 · Z2 )(X1 · Z1 )2
− 2(dˆ− 1)(X1 · X2 )(Z2 · Z2 )(X1 · Z1 )(X2 · Z1 ) + (dˆ− 1)(X1 · X1 )(Z2 · Z2 )(X2 · Z1 )

(H.3)

2

− (dˆ− 2)(dˆ− 1)(X1 · Z2 )2 (X2 · Z1 )2 + 2(dˆ− 2)(dˆ− 1)(X1 · Z1 )(X1 · Z2 )(X2 · Z1 )(X2 · Z2 )
ˆ 1 · X1 )(Z1 · Z1 )(X2 · Z2 )2
− (dˆ− 2)(dˆ− 1)(X1 · Z1 )2 (X2 · Z2 )2 + d(X
ˆ 1 · X1 )(Z1 · Z2 )(X2 · Z1 )(X2 · Z2 ) ,
− 2d(X
}

where c2,2 = −

1
3(−2+dˆ)(−1+dˆ)

is a normalization constant which ensures that the sym-

metrizer is idempotent. In order to get back the indices it is then sufficient to take
derivatives with respect to the auxiliary vectors.71 As explained in [1], this contracted form of the Young symmetrizer is also convenient since it trivially generalizes
to OSp(d|2) representations, by considering vectors Xi , Zi in Rd|2 and the scalar product
X · Y = X a gab Y b , with the usual OSp(d|2) metric gab . We stress that the dependence of
the symmetrizer on the parameter dˆ must not be changed (indeed dˆ = d − 2 is equal to the
supertrace).
By some manipulations of this projector, we are able to obtain the final form for the
box superfield,
(B θθ̄,θθ̄ )θθ̄ =

1{ 2
−ϕ ψ,µν ψ̄,µν + ψ ψ̄(−ϕ2,µν − 20ϕ,µ ω,µ + 54ω 2 ) + 4ϕϕ,µ (ψ,ν ψ̄,µν + ψ,µν ψ̄,ν )
6
+2ϕ,µ ϕ,ν (ψ ψ̄,µν + ψ,µν ψ̄) − 2ϕϕ,µν (ψ ψ̄,µν + ψ,µν ψ̄) − 42ϕωψ,µ ψ̄,µ
+2ϕϕ,µν (ψ,µ ψ̄,ν + ψ,ν ψ̄,µ ) + 4ϕ,µ ϕ,µν (ψ ψ̄,ν + ψ,ν ψ̄) − ϕωϕ2,µν + 54ϕω 3
−12ωϕ,µ (ψ ψ̄,µ + ψ,µ ψ̄) + 10ϕω,µ (ψ ψ̄,µ + ψ,µ ψ̄) − 30ψ ψ̄ψ,µ ψ̄,µ
2
+2ωϕ,µ ϕ,ν ϕ,µν + 4ϕω,µ ϕ,ν ϕ,µν + ϕ(2ϕ,µ ϕ,ν − ϕϕ,µν )ω,µν + 5ϕ2 ω,µ

−6ω 2 ϕ2,µ − 32ϕωϕ,µ ω,µ ,

(H.5)

}

where for short the expression is written for d = dˆ+ 2 = 6. We checked that this operator,
upon substitution ψ, ψ̄ → χ has indeed anomalous dimension (7/9)ε as expected.
71

E.g. we can compute the dimensions of the representation as the trace of the projector, which entails
freeing all the indices and contracting them pairwise (up to a combinatorial factor):
dim(2,2) =

1 µ µ ν ν ρ ρ σ σ
1 ˆ
ˆ dˆ+ 1)(dˆ+ 2) ,
∂ ∂ ∂X ∂Z ∂ ∂ ∂X ∂Z Π2,2 (X1 , X2 ; Z1 , Z2 ) =
(d − 3)d(
16 X1 Z1 1 1 X2 Z2 2 2
12

This matches e.g. eq. (10.68) of [109]. We use this result in section 11.2.2.

– 94 –

(H.4)

JHEP03(2021)219

+ (dˆ− 1)(X2 · X2 )(Z1 · Z1 )(X1 · Z2 )2 − 2(dˆ− 1)(X1 · X2 )(Z1 · Z1 )(X1 · Z2 )(X2 · Z2 )

## PDF page 98

ϕ2,µ χ2,ν ,

ϕ,µ χ,µ ϕ,ν χ,ν ,

ϕ2 ϕ2,µνσ ,

ϕϕ,µ ϕ,νσ ϕ,µνσ ,

ϕϕ,µν ϕ,µσ ϕ,νσ ,

ϕ,µ ω,µ ϕ2,ν ,

ϕ,µ ϕ,ν ϕ,σ ϕ,µνσ ,

ϕ,ν ϕ,σ ϕ,µν ϕ,µσ .

ϕ2,ν ϕ2,µσ

(H.6)

This list of 32 monomials is closed upon renormalization, mixing in a non-trivial way.
Diagonalizing the resulting 32 × 32 mixing matrix gives the following list of anomalous
dimensions:
13ε 13ε 13ε 13ε 13ε 19ε 10ε 10ε
,
,
,
,
,
,
,
, ε, ε, ε, ε,
9
9
9
9
9 15 9
9
14ε 8ε 8ε 8ε 8ε 7ε 7ε 7ε 7ε ε ε 4ε ε 2ε ε
, , , , , , , , , , , , , , , 0, 0, 0.
15 9 9 9 9 9 9 9 9 2 2 9 3 9 9

2ε, 2ε,

(H.7)

Let us see next how this list can be related to WF computations. First, we would like to
emphasize that many of the numbers in (H.7) are associated to descendants. Indeed, we
can redo the computation only using equivalence classes of operators defined up to total
derivatives (as discussed in appendix F). The result is that only 8 of the above operators
14ε 8ε 7ε ε ε ε
are not descendants. The associated anomalous dimensions are 10ε
9 , 15 , 9 , 9 , 2 , 3 , 9 , 0, 0.
This also explains why in (H.7) there are many repeated anomalous dimensions: they
correspond to total derivatives of different components of the superfield. To clarify this, let
us focus on the anomalous dimension 7ε
9 (the one of the box operator). This appears four
times in (H.7) and only one of these is not a total derivative — this indeed corresponds to
the operator (H.5). The other three occurrences are related to the following descendants
(we also checked this explicitly):
∂ 2 (B θθ̄,θθ̄ )0 ,

∂µ ∂ν (B θθ̄,µν )0 ,

∂µ (B θθ̄,θµ )θ̄ .

(H.8)

E.g. the first one, before applying ∂ 2 , takes the form
1
2
5
10
(B θθ̄,θθ̄ )0 → − ϕ2 ϕ2,µν + ϕϕ,µ ϕ,ν ϕ,µν − ϕ2 χ2i,µ + ϕχi ϕµ χi,µ − 2ϕωϕ2,µ
6
3
6]
3
[
7ϕ2 ω 2 20 2
10(χ2i )2
+
− ϕχi ω −
,
(H.9)
3
3
7
where we also included, in square brackets, the susy-null contribution.

– 95 –

JHEP03(2021)219

Notice that (H.5) contains the term ψ ψ̄ψ,µ ψ̄,µ which can be mapped in two different
ways (as explained in appendix C, eq. (C.7)) in terms of χ. Both choices are equally good,
since their difference is proportional to the susy-null operator ∂ 2 (χ2 )2 (which can be set to
zero for anomalous dimensions computations). As usual we can also determine the susynull contribution by requiring that the full operator is an eigenperturbation: this gives the
5 2 2 2
above (B θθ̄,θθ̄ )θθ̄ with ψ ψ̄ψ,µ ψ̄,µ → 14 χi χi χj,µ χj,µ + 84
∂ (χ ) .
As a final example we compute the anomalous dimensions of all susy-writable (and
one susy-null) operators at dimensions ∆ = 10 made of four fields. One of such operators
is (H.5), and we would like to check that all of the others also have dimensions consistent
from dimensional reduction. In practice we consider a list of 32 monomials: the 22 summands of (H.5) (terms of the form e.g. ψ ψ̄,ν + ψ,ν ψ̄ are counted as one after the ψ, ψ̄ → χ
map), the susy-null operator ∂ 2 (χ2 )2 discussed above and the following 9 extra operators

## PDF page 99

We also notice that different anomalous dimensions in (H.7) occur a different number
of times. It is easy to see why this happens. This depends on the superprimary Osp(d|2)
representation, and on how many times we need to differentiate to get to the needed dimension. E.g. 2ε in (H.7) is related to the superprimary Φ4 in the following two combinations:
(∂ 2 )2 Φ4θθ̄ , (∂ 2 )3 Φ40 . Here, since Φ4 is a scalar, there is a single OSp component to use (in
constrast with non-scalar operators). Also only total derivatives appear because the superfield itself has too low bare dimension: [Φ40 ] = 4, [Φ4θθ̄ ] = 6. As a final example, the value
13ε
2 ab
2 2
2 θ θ̄
9 in (H.7) is related to five possible descendants of the superfield Φ T : (∂ ) (Φ T )0 ,
∂ 2 ∂µ ∂ν (Φ2 T µν )0 , ∂ 2 ∂µ (Φ2 T µθ̄ )θ , ∂ 2 (Φ2 T θθ̄ )θθ̄ , ∂µ ∂ν (Φ2 T µν )θθ̄ .

H.2

Susy-null leaders

We next consider all the susy-null leaders with 6d classical dimension up to 12 (one at
dimension 8, one at 10, and four at 12). For each of them we compute the one-loop
anomalous dimension, or the two-loop one if the one-loop result is trivial. We use the OPE
method at one loop, and Feynman diagrams whenever we have to go to two loops.
72

As explained in [38], for Z2 symmetry, the anomalous dimensions are the numbers in the table times ε/3.
We thank Johan Henriksson, who confirmed us in a private communication that there exist two WF
ˆ with anomalous
operators with four fields and six derivatives in the spin-two representation of SO(d)
dimensions equal to ε/9 and (14/15)ε. On the other hand the operator with anomalous dimensions 0 was
ˆ
not found in the scalar and spin-two sector, so it must transform in the box (2, 2) representation of SO(d).
73

– 96 –

JHEP03(2021)219

We do not present here a detailed explanation for all anomalous dimensions in (H.7).
However we stress that we checked that they are all in agreement with available WF
results: not only the anomalous dimensions match but also the occurrences (of primaries
and descendants) are the ones expected.
Most of the checks are done by comparing with table 4 of [38] (using the entries with
n = 4 fields),72 where all operators built out of 5 or less derivatives are presented. However
the list (H.7) is also sensitive to operators with six derivatives: indeed the lowest component
of a superfield with four Φ’s and six derivatives has dimension 10. Unfortunately such operators were not fully classified in the WF literature, except for a scalar operator considered
in [33] with γ = ε/3 (see equation (3.12)), which indeed matches our computation.
We can therefore predict that in the WF spectrum of operators with four fields and
six derivatives, there are three operators with anomalous dimensions 0, ε/9, (14/15)ε. We
ˆ representation. Indeed the operators
can further say something about their possible SO(d)
in our list must have an even number of indices which are set to θ and θ̄ (otherwise
ˆ scalar). We thus
the resulting operator would be fermionic or it would not be an SO(d)
conclude that these three operators must transform either in the scalar, or spin two, or
ˆ 73
(2, 2) representation of SO(d).
Finally let us comment on the three operators with γ = 0. Only one of them is a descendant: the susy-null operator ∂ 2 (χ2 )2 . One of the other two operators is a primary, an
operator with six derivatives. The third operator in this group is actually not an eigenvector, but a generalized eigenvector forming a logarithmic multiplet together with the γ = 0
primary. This is a recurrent feature of our non-unitary theory: mixing matrices may not be
fully diagonalizable and can be organized in Jordan blocks, as discussed around eq. (F.6).

## PDF page 100

H.2.1

∆0 = 8 + O(ε), n = 4

The lowest susy-null leader is (χ2i )2 , of classical dimension ∆0 = 8 − 2ε in d = 6 − ε (see
table 1). It is easy to see that it does not receive any anomalous dimension at one loop,
so we proceed to study the 2-loop contribution. Denoting by ((χ2i )2 )B the operator built
of bare fields, and by (χ2i )2 the renormalized operator whose correlators should be free of
poles in ε, they are related by
((χ2i )2 )B = Z (χ2i )2 ,
(H.10)

[

]

Z −1 + I(χ2 )2 + (t,u channels) +
i

4
1∑
Iϕω (p2i )/p2i .
4 i=1

(H.11)

Here Iϕω is the integral in (G.9) which comes from the external leg corrections. The I(χ2 )2
i
comes from the loop diagram of figure 4. It is given by (see [105] for the standard details):
H 2 λ2
I(χ2 )2 =
i
(2π)2d

∫

( )
dd l1 dd l2
H 2 λ2
=
+
O
ε0 .
2(4π)6 ε
l12 (l22 )2 (l1 + p3 + p4 )2 ((l1 + l2 − p1 )2 )2

(H.12)

The Z is obtained by demanding that ε−1 poles cancel:
Z −1 = 1 −

4 H 2 λ2
.
3 (4π)6 ε

(H.13)

From this we get the anomalous dimension of (χ2i )2 as follows:
γ(χ2 )2 = µ
i

H.2.2

∂
8
log Z = − ε2 .
∂µ
27

(H.14)

∆0 = 10 + O(ε), n = 6

The next susy-null leader is ϕ2 (χ2i )2 (table 7), of bare dimension ∆0 = 10 − 3ε. It gets
a nonzero one-loop anomalous dimension, which we compute by the OPE method (appendix F). The following OPEs are important:
ϕ2 (χ2i )2 (x) × χ2j ϕ2 (0) ∼ 32⟨ϕ(x)ϕ(0)⟩0 ⟨χi (x)χj (0)⟩0 ϕ2 (χ2k )χi χj (0) + . . .
ϕ2 (χ2i )2 (x) × ωϕ3 (0) ∼ 6⟨ϕ(x)ϕ(0)⟩0 ⟨ϕ(x)ω(0)⟩0 ϕ2 (χ2i )2 (0) + . . .

(H.15)

From this and using the formula (F.18) we get
γϕ2 (χ2 )2 =
i

[

( )
9Hλ
=
3ε
+
O
ε2 .
64π 3 λ=λ∗
]

– 97 –

(H.16)

JHEP03(2021)219

To find the renormalization factor Z we consider the correlator ⟨(χ2i )2 (p =
0)χj (p1 )χk (p2 )χl (p3 )χm (p4 )⟩. A nonzero two-loop diagram is shown in figure 4. Another
two loop diagram (a double bubble diagram of the type shown in figure 15) vanishes because
it is proportional to n, from contractions of the Kij matrices in the χ-χ propagator (E.2).
At two loops we must also consider the propagator computed in section G.2.
Taking everything into account, the two-loop corrected amputated correlator equals
the tree-level one, times

## PDF page 101

H.2.3

∆0 = 12 + O(ε), n = 6

At dimension ∆0 = 12 − 3ε we have three independent susy-null leaders which are composites of 6 fields. Two of them are shown in table 7 and the third in eq. (D.11).

To compute the mixing matrix we consider the following OPEs of the operators Oi
with the interaction V
ϕω(χ2 )2 (0) × χ2 ϕ2 (x) ∼ 16⟨ϕϕ⟩0 ⟨χi χj ⟩0 ϕωχ2 χi χj + 2⟨ϕϕ⟩0 ⟨ϕω⟩0 (χ2 )3
+8xµ xν ⟨ϕω⟩0 ⟨χi χj ⟩0 ϕχ2 χi ∂µ ∂ν (ϕχj ) + . . .

(H.17)

ϕω(χ ) (0) × ϕ ω(x) ∼ 6⟨ϕϕ⟩0 ⟨ϕω⟩0 ϕω(χ )
2 2

3

2 2

(

)

+3xµ xν ⟨ϕω⟩0 ⟨ϕω⟩0 ∂µ ∂ν ϕ2 (χ2 )2 + . . .
(

)

(

)

(H.18)

(χ2 )3 (0) × χ2 ϕ2 (x) ∼ 24⟨χi χj ⟩0 ⟨χi χj ⟩0 ∂µ ∂ν ϕ2 (χ2 )2
+6⟨χi χj ⟩0 ⟨χi χk ⟩0 ∂µ ∂ν ϕ2 χ2 χj χk + . . .
(

(H.19)

)

(∂ϕ)2 (χ2 )2 (0) × ϕ3 ω(x) ∼ 6xµ xν ∂ σ ⟨ϕϕ⟩0 ∂σ ⟨ϕω⟩0 ∂µ ∂ν ϕ2 (χ2 )2
+6∂ σ ⟨ϕϕ⟩0 ∂σ ⟨ϕϕ⟩0 ϕω(χ2 )2 + . . .

(H.20)

(∂ϕ)2 (χ2 )2 (0) × χ2 ϕ2 (x) ∼ −32xν ⟨χi χj ⟩0 ∂ µ ⟨ϕϕ⟩0 (∂µ ϕ) χ2 χi ∂ν (ϕχj )
+2∂⟨ϕϕ⟩0 ∂⟨ϕϕ⟩0 (χ2 )3 + . . .

(H.21)

In the above OPEs we have expanded the r.h.s. in x wherever needed and kept only the
terms that give 1/ε pole. Following the discussion in appendix F.1, we finally obtain the
3 × 3 anomalous dimension matrix:
⎛

Γ=

⎞

24 −12 2 ⎟
⎜

ε ⎜
⎟
⎜ 3
0 3 ⎟.
⎠
18 ⎝
−2 12 20

(H.22)

This matrix is not fully diagonalizable, but it admits a Jordan decomposition (see around
formula{(F.6)) with} eigenvalues 0 and (11/9)ε, to which there correspond true eigenvectors
(2) = {−1, 0, 1}. There is also a generalized eigenvector e(3) =
e(1) = −1, − 11
6 , 1 and e
{

}

(

)

(3)

27
11
(2)
− 99
2ε , − 4ε , 0 which forms a rank-2 Jordan block with e , namely Γij − 9 εδij ej

(2)
ei .
74

Therefore, corresponding to the anomalous dimension

We add a factor 1/H to (∂ϕ)2 (χ2 )2 so that the mixing matrix is free of H.

– 98 –

=

11
9 ε, there is a 2 × 2 Jordan

JHEP03(2021)219

To compute their anomalous dimensions it is convenient to work with equivalence
classes of operators defined up to total derivatives (as discussed in the end of appendix F.1). We can parametrize the equivalence classes by the following three operators:
O1 = ϕω(χ2 )2 , O2 = (χ2 )3 and74 O3 = H1 (∂ϕ)2 (χ2i )2 . E.g. ϕ∂ϕ(χi ∂χi )(χ2j ) is not considered as an independent operator since it can [be written in
] terms of O1 and O2 up to a
1 µ
2
2
2
total derivative, namely ϕ∂ϕ(χi ∂χi )(χj ) = 4 ∂ ϕ∂µ ϕ(χj ) + H4 O1 − H4 O2 .

## PDF page 102

block and a logarithmic multiplet {O1R , O2R }, such that75
⎛

D⎝

O2R
O1R

⎞

⎛

⎠=⎝

12 − 16ε
9

ε

0

12 − 16ε
9

⎞⎛

O2R

⎠⎝

O1R

⎞
⎠,

(H.23)

H.2.4

∆0 = 12 + O(ε), n = 8

With 8 fields and dimension ∆ = 12 + O (ε) we have a single susy-null leader, ϕ4 (χ2 )2 (See
table 8). Its O (ε) anomalous dimension can be obtained from the following OPEs:
ϕ4 (χ2 )2 (0) × χ2 ϕ2 (x) ∼ 64⟨ϕϕ⟩0 ⟨χi χj ⟩0 ϕ4 χ2 χi χj
ϕ4 (χ2 )2 (0) × ϕ3 ω(x) ∼ 36⟨ϕϕ⟩0 ⟨ϕω⟩0 ϕ4 (χ2 )2 .

(H.24)

Following (F.18) we get the anomalous dimension:
γϕ4 (χ2 )2 =
H.3

22ε
.
3

(H.25)

Non-susy-writable leaders

We will now compute the anomalous dimensions for some specific non-susy writable leaders.
For ∆ ⩽ 12 the only non-susy writable leader operator comes from the Feldman F6 . We
will consider this operator first and then will generalize to higher Feldman operators Fk .
This way we revisit the result of [29] that these operators have negative leading anomalous
dimensions.
As shown in the main text the leader for Feldman operators have the structure:
(Fk )L =

k−2
∑
l=2

( )

(−1)

l

k (∑′ l ) (∑′ k−l )
χi
χj
.
l

(H.26)

In particular (F6 )L = (χ3i )2 − 32 (χ2i )(χ4i ) up to a constant factor. We will see in a second
that (F6 )L has no anomalous dimension at one loop, so we are setting up a two-loop
computation. Let OiB be all leader operators of bare dimension 12 with which O1B = (F6 )L
might mix, related to the renormalized operators by OiB = Zij Oj . Since (F6 )L is the lowest
We rescaled the operator O2R so that it has order one coefficients, and as a consequence the upper right
corner of the dilatation matrix is ε and not 1. The ε → 0 limit is smooth in this form.
75

– 99 –

JHEP03(2021)219

where the dilatation operator D is acting on the renormalized operators O1R ≡ −O1 + O3
27
R
R
and O2R ≡ − 99
2 O1 − 4 O2 . Here the operators O1 and O2 should not be considered as
the actual renormalized operators, since they only parametrize the equivalence classes of
operators up to derivatives.
For the sake of completeness we also performed a much more general computation
which gives us the exact form of the renormalized operators. Computing the anomalous
dimensions matrix of the 49 possible operators which are built out of 6 fields and have
dimensions 12 in d = 6, we obtained that O1R was actually a correct eigenperturbation.
On the other hand, the operator O2R should have been corrected by some total derivatives,
33
2 2
2
2
namely by adding to it 231
32 ∂µ (ϕ,µ ϕχi χj ) − 16 ∂µ (ϕ χi χi,µ χj ).

## PDF page 103

➤

➤

➤

➤

➤

➤

➤
➤

➤

➤

Figure 15. Two-loop diagrams correcting the correlator ⟨(Fk )L (p = 0)χi1 (p1 ) . . . χik (pk )⟩.

⎛

Z11 ∗ . . .

⎞

⎜
⎟
⎜
⎟
⎜ 0 ∗ ...⎟
⎜
⎟,
Z=⎜
⎟
⎜ 0 ∗ ...⎟
⎝
⎠

..
.

(H.27)

.. . .
. .

i.e. in the first column only Z11 is nonzero. Because of this, we only need to know Z11
to compute the anomalous dimension of (F6 )L . We would need to know the potentially
nonzero entries marked by ∗ to compute the full eigenoperator, but we will not do this here.
To compute Z11 we consider the correlator ⟨(F6 )L (p = 0)χi1 (p1 ) . . . χi6 (p6 )⟩. It is easy
to see that there is no one-loop diagram which contributes to this correlator. This implies
that O(λ) correction to Z11 vanishes, i.e. as promised (F6 )L has no one-loop anomalous
dimension. [On the other hand some of the entries marked by ∗ in the first row are nonzero
at one loop. As a result the eigenoperator gets a susy-null admixture already at one loop.
See section H.3.1 for a discussion.] At two loops the correlator gets contributions from the
two diagrams in figure 15 (for k = 6), both with a 1/ε pole.
The first diagram’s tensor structure in the χi indices is precisely that of (F6 )L itself
(this is obvious because of K 2 = K, see (E.4)). Performing Kij -tensor contractions, the
second diagram is instead proportional to the tree-level diagram with insertion of the susynull operator (χ2i )3 . This is an example of a susy-null admixture, a nonzero ∗ entry in the
first row of (H.27). So only the first diagram contributes to Z11 .
That the second diagram does not contribute to Z11 in fact holds for general k, and
we will need this fact below, so let us show it. Its tensor structure splits into two groups of
indices separated by the ϕ loop. The right tensor structure is just that of χ2i . The left tensor
structure with its χ-loop can be obtained by applying Krs δχδ r δχδ s to the Feldman leader
expression. This calculation is greatly simplified using the equivalent equation (see (5.16))
(Fk )L = 2

n
∑

(−χi )k +

i=2

n
∑

(χi − χj )k ,

(H.28)

i,j=2

and it gives 2k(k − 1)(Fk−2 )L after a few lines of algebra, i.e. a multiple of the lower
Feldman leader. Thus the total tensor structure is that of (χ2i )(Fk−2 )L . For k = 6 this
reduces to (χ2i )3 as claimed, since (F4 )L ∝ (χ2i )2 .

– 100 –

JHEP03(2021)219

non-susy-writable leader, all these other operators are susy-null or susy-writable, hence the
mixing matrix has the form (see (F.11))

## PDF page 104

Let us next evaluate the first diagram in (15), also for general k. The loop integral
is the same as I(χ2 )2 in (H.12), the computation being similar to the one for the (χ2 )2
i
in section H.2.1. (Eq. (H.29) below reduces to (H.13) for k → 4.) Taking into account
external leg corrections and combinatorial factors, we get:
k(k − 1)
k
−1
Z11
=1−
[I(χ2 )2 ]1/ε −
i
4

Iϕω (p2 )
k(3k − 4) H 2 λ2
=
1
−
.
4
p2
24
(4π)6 ε
1/ε
[

]

(H.29)

Setting here k = 6 we get the anomalous dimension:
(H.30)

With a small extra input we can upgrade the above discussion and extract the anomalous
dimensions of (Fk )L for general k. We just need to check if one more element of the
mixing matrix is zero. We have seen above that (Fk )L requires adding (χ2i )(Fk−2 )L to get
a finite operator. For k = 6 the latter operator was susy-null, hence the inverse mixing was
guaranteed not to happen. For k > 6 the operator (χ2i )(Fk−2 )L is non-susy-writable, so we
need to see if it mixes back to (Fk )L . It is however easy to see that this does not happen.
Using eq. (H.26), operator (χ2i )(Fk−2 )L can be expanded in monomials each of which is a
product of three O(n − 2) singlets of the form (χ2i1 )(χai2 )(χbi3 ), where a + b = k − 2. If any of
these singlets is plugged into the second diagram in figure 15, it returns a monomial which
is a product of four or three singlets (depending on how the χ-loop is contracted). Since
(Fk )L is made of products of two singlets, its tensor structure cannot arise. This discussion
implies that the anomalous dimension of (Fk )L for any k is not modified by mixing with
(χ2i )(Fk−2 )L and can be computed from Z11 given in (H.29). We obtain:
γ(Fk )L = −

k(3k − 4) 2
ε .
108

(H.31)

This nicely matches the result of [29]. In the future it would be interesting to analyze other
non-susy-writable leaders with the same classical dimension as (Fk )L for k > 6, one obvious
(
)
example being 2ωϕ + χ2i (Fk−2 )L , to see if any of these has the corrected dimension even
lower than (Fk )L .
H.3.1

Remark on admixture of susy-nulls

As mentioned above, the leader (F6 )L experiences a susy-null mixing already at one-loop
level, which does not modify its anomalous dimension (zero at one loop), but does modify the form of the eigenvector. In fact the correct eigenvector at one loop is the linear
combination:
3
3
(H.32)
(χ3i )2 − (χ2i )(χ4j ) + (χ2i )3 ,
2
2
where the first two terms are (proportional to) (F6 )L , while the last term is susy-null.
The form of this one-loop eigenvector can be determined e.g. using the OPE method (appendix F).
Here we would like to point out that (H.32) can also be determined using group theory
reasoning. Namely, we expect that leaders with well-defined anomalous dimensions will

– 101 –

JHEP03(2021)219

7
γ(F6 )L = − ε2 .
9

## PDF page 105

transform in irreducible O(n − 2) representations, which should correspond to symmetric
traceless tensors. Eq. (H.32) can be written as the contraction of 6 χ’s with the symmetric
6-tensor
(
)
3
3
T = δ3 ⊗ δ3 − δ2 ⊗ δ4 + δ2 ⊗ δ2 ⊗ δ2
.
(H.33)
2
2
sym
Here sym is the symmetrization, and δp denotes the rank k-tensor whose only nonzero
components are (δp ) ii...i = 1 i.e. when all p indices coincide (the indices run from 2 to
⏟⏞⏞⏟
p

n
∑

(tr′ T )... =

(δij + Πij )Tij... .

(H.34)

i,j=2

It is then easy to work out (we define δ0 = −1, a constant):
tr′ δp = 2δp−2 ,

(H.35)

tr′ (δp ⊗δq )sym = [Ap,q 2δp−2 ⊗δq +Aq,p 2δp ⊗δq−2 +(1−Ap,q −Aq,p )(δp+q−2 +δp−1 ⊗δq−1 )]sym ,
) /(

p(p−1)
p+q
where Ap,q = p+q−2
= (p+q)(p+q−1)
, and similarly for higher tensor products.
p−2
p
Using these rules, one can check that the tensor (H.33) is indeed traceless, while it would
not have been traceless without the last term.

(

I

)

Remarks about tuning the disorder distribution

As discussed in section 11.2.1, one might be able to look for the SUSY fixed point in
numerical simulations of the RFIM, by tuning the disorder distribution within a family
depending on more than one parameter. Here we discuss some ideas about what parameter
to tune, to set the relevant operator to 0, assuming for simplicity that a single perturbation
has turned relevant, the one corresponding to the susy-null leader (χ2 )2 . This discussion
is meant as schematic and non-rigorous.
Our starting point is the analysis of Brézin-De Dominicis ([27], section 1) who used the
Hubbard-Stratonovich identity to rewrite an Ising spin system in terms of a scalar field.
Introducing replicas and integrating out the disorder, they arrived at the system of n scalar
fields on the lattice with the Sn -invariant potential ([27], eq. (1.9))
V =

where σk =
τp =
76

∑n

1
τ2
1
1
(τ2 − 1)σ2 − σ12 + (1 + 3τ4 − 4τ2 )σ4 + (3τ22 − τ4 )σ14
2
2
12
24
1 2
1
1 2
2
+ (τ2 − τ4 )σ2 + (τ2 − τ4 )σ1 σ3 − (τ2 − τ4 )σ12 σ2 + O(φ6 ),
8
3
4

k
i=1 φi

∫ ∞
−∞

(I.1)

as in section 5.1, and the quantities τp are defined as

dhP (h)(cosh h) (tanh h) →
n

p

∫ ∞
−∞

dh P (h)(tanh h)p

(n → 0).

1
See footnote 10 for the definition of Πij ; δij + Πij is the n → 0 limit of δij − n−1
Πij .

– 102 –

(I.2)

JHEP03(2021)219

n). E.g. (δ2 )ij = δij is the Kronecker delta tensor, while δ1 is the (1, 1, . . .) vector. The
∑
appropriate trace taking into account the constraint ′ χi = 0 is:76

## PDF page 106

Now let us refer to the toy model RG analysis in appendix B. We can express the quartic
part of the potential in terms of eigenperturbations given in table 4: O1 = σ4 , O2 = σ14 ,
∑
O3 = σ1 σ22 , O4 = σ22 + 2σ1 σ3 and O5 = σ22 − 43 σ1 σ3 : V = 5a=1 ca Oa . We are particularly
interested in the coefficient of O5 , which comes out equal:
c5 = −

1
(4τ2 − 3τ22 − τ4 ).
40

(I.3)

Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited.

References
[1] A. Kaviraj, S. Rychkov and E. Trevisani, Random field Ising model and Parisi-Sourlas
supersymmetry. Part 1. Supersymmetric CFT, JHEP 04 (2020) 090 [arXiv:1912.01617]
[INSPIRE].
[2] J.L. Cardy, Random-field effects in site-disordered Ising antiferromagnets, Phys. Rev. B 29
(1984) 505.
[3] D.P. Belanger, Experiments on the random field Ising model, in Spin glasses and random
fields, A.P. Young ed., World Scientific, Singapore (1997), pg. 251 [cond-mat/9706042].
[4] Z. Komargodski and D. Simmons-Duffin, The random-bond Ising model in 2.01 and 3
dimensions, J. Phys. A 50 (2017) 154001 [arXiv:1603.04444] [INSPIRE].
[5] G. Parisi and N. Sourlas, Random magnetic fields, supersymmetry and negative dimensions,
Phys. Rev. Lett. 43 (1979) 744 [INSPIRE].
[6] N.G. Fytas and V. Martín-Mayor, Universality in the three-dimensional random-field Ising
model, Phys. Rev. Lett. 110 (2013) 227201 [arXiv:1304.0318].
[7] N.G. Fytas, V. Martín-Mayor, M. Picco and N. Sourlas, Phase transitions in disordered
systems: the example of the random-field Ising model in four dimensions, Phys. Rev. Lett.
116 (2016) 227201 [arXiv:1605.05072].
[8] N.G. Fytas, V. Martin-Mayor, M. Picco and N. Sourlas, Restoration of dimensional
reduction in the random-field Ising model at five dimensions, Phys. Rev. E 95 (2017)
042117 [arXiv:1612.06156] [INSPIRE].
77

We thank Giorgio Parisi for this remark. Recall that the kurtosis K is defined, for even distributions,
( )1/2
∫
4
as the normalized fourth moment K = σh4 = σ −4 dh P (h)h4 where σ = h2
is the standard deviation.

– 103 –

JHEP03(2021)219

Indeed, the operator O5 has the leader (χ2 )2 and we are assuming that this direction is
relevant, so we coefficient c5 needs to be tuned to reach the SUSY fixed point in the IR. The
needed value of c5 at the UV scale depends on the microscopic details (it may be positive
or negative depending on the sign of the contributions that c5 gets under RG running).
Since c5 is a linear combination involving the second and fourth moments of the disorder,
one can imagine that the necessary tuning may be obtained by adjusting the kurtosis
of the distribution.77 It should be stressed that the Oa ’s are not exact nonperturbative
eigenperturbations, and so the tuning which we described should not be taken too literally.

## PDF page 107

[9] N.G. Fytas, V. Martín-Mayor, G. Parisi, M. Picco and N. Sourlas, Evidence for
supersymmetry in the random-field Ising model at D = 5, Phys. Rev. Lett. 122 (2019)
240603 [arXiv:1901.08473] [INSPIRE].
[10] S. Rychkov, Supersymmetry and its absence in the random field Ising model, in Bootstrap
Zoominar, https://www.youtube.com/watch?v=twCc4lOWKkg, 22 April 2020.
[11] J.L. Cardy, Nonperturbative effects in a scalar supersymmetric theory, Phys. Lett. B 125
(1983) 470 [INSPIRE].
[12] A. Klein and J.F. Perez, Supersymmetry and dimensional reduction: a nonperturbative
proof, Phys. Lett. B 125 (1983) 473 [INSPIRE].

[14] O.V. Zaboronsky, Dimensional reduction in supersymmetric field theories, hep-th/9611157
[INSPIRE].
[15] J.L. Cardy, Nonperturbative aspects of supersymmetry in statistical mechanics, Physica D
15 (1985) 123.
[16] H. Mukaida and Y. Sakamoto, Renormalization group for the probability distribution of
magnetic impurities in a random-field φ4 model, Int. J. Mod. Phys. B 18 (2004) 919
[cond-mat/0302143].
[17] F. Wegner, Supermathematics and its applications in statistical physics: Grassmann
variables and the method of supersymmetry, Springer, Berlin, Heidelberg, Germany (2016)
[INSPIRE].
[18] A. Kaviraj and E. Trevisani, Random field φ3 model and Parisi-Sourlas supersymmetry,
work in progress.
[19] S. Albeverio, F.C. De Vecchi and M. Gubinelli, Elliptic stochastic quantization,
arXiv:1812.04422 [INSPIRE].
[20] S. Albeverio, F.C. De Vecchi and M. Gubinelli, The elliptic stochastic quantization of some
two dimensional Euclidean QFTs, arXiv:1906.11187 [INSPIRE].
[21] J. Golden and M.F. Paulos, No unitary bootstrap for the fractal Ising model, JHEP 03
(2015) 167 [arXiv:1411.7932] [INSPIRE].
[22] G. Tarjus and M. Tissier, Nonperturbative functional renormalization group for random
field models and related disordered systems. I. Effective average action formalism, Phys.
Rev. B 78 (2008) 024203 [arXiv:0712.3550].
[23] F. Wegner, The critical state, general aspects, in Phase transitions and critical phenonema,
volume 6, L. Domb and M. Green eds., Academic Press, U.S.A. (1976), pg. 8.
[24] D.J. Binder and S. Rychkov, Deligne categories in lattice models and quantum field theory,
or making sense of O(N ) symmetry with non-integer N , JHEP 04 (2020) 117
[arXiv:1911.07895] [INSPIRE].
[25] F. Knop, A construction of semisimple tensor categories, C. R. Math. Acad. Sci. Paris 343
(2006) 15 [math.CT/0605126].
[26] F. Knop, Tensor envelopes of regular categories, Adv. Math. 214 (2007) 571
[math.CT/0610552].

– 104 –

JHEP03(2021)219

[13] A. Klein, L.J. Landau and J.F. Perez, Supersymmetry and the Parisi-Sourlas dimensional
reduction: a rigorous proof, Commun. Math. Phys. 94 (1984) 459 [INSPIRE].

## PDF page 108

[27] E. Brézin and C. De Dominicis, New phenomena in the random field Ising model, Europhys.
Lett. 44 (1998) 13 [cond-mat/9804266] [INSPIRE].
[28] G. Tarjus and M. Tissier, Avalanches and perturbation theory in the random-field Ising
model, J. Stat. Mech. 2016 (2016) 023207 [arXiv:1510.01718].
[29] D.E. Feldman, Critical exponents of the random-field O(N ) model, Phys. Rev. Lett. 88
(2002) 177202 [cond-mat/0010012].
[30] J.L. Cardy, Scaling and renormalization in statistical physics, Cambridge Univ. Pr.,
Cambridge, U.K. (1996).

[32] A. Barabanschikov, L. Grant, L.L. Huang and S. Raju, The spectrum of Yang-Mills on a
sphere, JHEP 01 (2006) 160 [hep-th/0501063] [INSPIRE].
[33] P. Liendo, Revisiting the dilatation operator of the Wilson-Fisher fixed point, Nucl. Phys. B
920 (2017) 368 [arXiv:1701.04830] [INSPIRE].
[34] S. Meneses, J. Penedones, S. Rychkov, J.M. Viana Parente Lopes and P. Yvernay, A
structural test for the conformal invariance of the critical 3d Ising model, JHEP 04 (2019)
115 [arXiv:1802.02319] [INSPIRE].
[35] M. Hogervorst, S. Rychkov and B.C. van Rees, Truncated conformal space approach in d
dimensions: a cheap alternative to lattice field theory?, Phys. Rev. D 91 (2015) 025005
[arXiv:1409.1581] [INSPIRE].
[36] M. Hogervorst, S. Rychkov and B.C. van Rees, Unitarity violation at the Wilson-Fisher fixed
point in 4 − ϵ dimensions, Phys. Rev. D 93 (2016) 125025 [arXiv:1512.00013] [INSPIRE].
[37] S. Minwalla, Restrictions imposed by superconformal invariance on quantum field theories,
Adv. Theor. Math. Phys. 2 (1998) 783 [hep-th/9712074] [INSPIRE].
[38] S.K. Kehrein and F. Wegner, The structure of the spectrum of anomalous dimensions in the
N vector model in 4 − ϵ dimensions, Nucl. Phys. B 424 (1994) 521 [hep-th/9405123]
[INSPIRE].
[39] M. Hogervorst, M. Paulos and A. Vichi, The ABC (in any D) of logarithmic CFT, JHEP
10 (2017) 201 [arXiv:1605.03959] [INSPIRE].
[40] J. Cardy, Logarithmic conformal field theories as limits of ordinary CFTs and some physical
applications, J. Phys. A 46 (2013) 494001 [arXiv:1302.4279] [INSPIRE].
[41] G. Badel, G. Cuomo, A. Monin and R. Rattazzi, The ϵ-expansion meets semiclassics, JHEP
11 (2019) 110 [arXiv:1909.01269] [INSPIRE].
[42] F. Wegner, Anomalous dimensions of high-gradient operators in then-vector model in 2 + ϵ
dimensions, Z. Phys. B 78 (1990) 33.
[43] G.E. Castilla and S. Chakravarty, Instability of the fixed point of the O(N ) nonlinear
sigma-model in (2 + ϵ) dimensions, Phys. Rev. Lett. 71 (1993) 384 [INSPIRE].
[44] G.E. Castilla and S. Chakravarty, Is the phase transition in the Heisenberg model described
by the (2 + ϵ) expansion of the nonlinear sigma model?, Nucl. Phys. B 485 (1997) 613
[cond-mat/9605088] [INSPIRE].
[45] E. Brézin and S. Hikami, Fancy and facts in the (d − 2) expansion of nonlinear sigma
models, cond-mat/9612016 [INSPIRE].

– 105 –

JHEP03(2021)219

[31] D.J. Amit and L. Peliti, On dangerous irrelevant operators, Annals Phys. 140 (1982) 207
[INSPIRE].

## PDF page 109

[46] S.E. Derkachov, S.K. Kehrein and A.N. Manashov, High-gradient operators in the N -vector
model, Nucl. Phys. B 493 (1997) 660 [cond-mat/9610106] [INSPIRE].
[47] S.E. Derkachov and A.N. Manashov, On the stability problem in the O(N ) nonlinear sigma
model, Phys. Rev. Lett. 79 (1997) 1423 [hep-th/9705020] [INSPIRE].
[48] G. Parisi, An introduction to the statistical mechanics of amorphous systems, in Recent
advances in field theory and statistical mechanics, proceedings of Les Houches 1982, Session
XXXIX, J.B. Zuber and R. Stora eds., North-Holland, Amsterdam, The Netherlands
(1984), pg. 473.

[50] M. Tissier and G. Tarjus, Nonperturbative functional renormalization group for random
field models. IV: supersymmetry and its spontaneous breaking, Phys. Rev. B 85 (2012)
104203 [arXiv:1110.5500] [INSPIRE].
[51] M. Tissier and G. Tarjus, Supersymmetry and its spontaneous breaking in the random field
Ising model, Phys. Rev. Lett. 107 (2011) 041601 [arXiv:1103.4812] [INSPIRE].
[52] G. Tarjus, I. Balog and M. Tissier, Critical scaling in random-field systems: 2 or 3
independent exponents?, Europhys. Lett. 103 (2013) 61001 [arXiv:1304.4146].
[53] I. Balog, G. Tarjus and M. Tissier, Comment on “evidence for supersymmetry in the
random-field Ising model at D = 5”, arXiv:1906.10058 [INSPIRE].
[54] M.V. Kompaniets and E. Panzer, Minimally subtracted six loop renormalization of
O(n)-symmetric φ4 theory and critical exponents, Phys. Rev. D 96 (2017) 036016
[arXiv:1705.06483] [INSPIRE].
[55] O. Schnetz, Numbers and functions in quantum field theory, Phys. Rev. D 97 (2018) 085018
[arXiv:1606.08598] [INSPIRE].
[56] D. Brydges and J. Imbrie, Branched polymers and dimensional reduction, Ann. Math. 158
(2003) 1019 [math-ph/0107005].
[57] D. Poland, S. Rychkov and A. Vichi, The conformal bootstrap: theory, numerical techniques,
and applications, Rev. Mod. Phys. 91 (2019) 015002 [arXiv:1805.04405] [INSPIRE].
[58] R. Rattazzi, V.S. Rychkov, E. Tonni and A. Vichi, Bounding scalar operator dimensions in
4D CFT, JHEP 12 (2008) 031 [arXiv:0807.0004] [INSPIRE].
[59] A. Dymarsky, J. Penedones, E. Trevisani and A. Vichi, Charting the space of 3D CFTs with
a continuous global symmetry, JHEP 05 (2019) 098 [arXiv:1705.04278] [INSPIRE].
[60] M. Reehorst, E. Trevisani and A. Vichi, Mixed scalar-current bootstrap in three dimensions,
JHEP 12 (2020) 156 [arXiv:1911.05747] [INSPIRE].
[61] A. Dymarsky, F. Kos, P. Kravchuk, D. Poland and D. Simmons-Duffin, The 3d stress-tensor
bootstrap, JHEP 02 (2018) 164 [arXiv:1708.05718] [INSPIRE].
[62] F. Gliozzi, More constraining conformal bootstrap, Phys. Rev. Lett. 111 (2013) 161602
[arXiv:1307.3111] [INSPIRE].
[63] F. Gliozzi and A. Rago, Critical exponents of the 3d Ising and related models from
conformal bootstrap, JHEP 10 (2014) 042 [arXiv:1403.6003] [INSPIRE].
[64] F. Gliozzi, P. Liendo, M. Meineri and A. Rago, Boundary and interface CFTs from the
conformal bootstrap, JHEP 05 (2015) 036 [arXiv:1502.07217] [INSPIRE].

– 106 –

JHEP03(2021)219

[49] G. Parisi and V. Dotsenko, Random magnetic fields and instantons in replica space, J.
Phys. A 25 (1992) 3143 [INSPIRE].

## PDF page 110

[65] S. Hikami, Dimensional reduction by conformal bootstrap, PTEP 2019 (2019) 083A03
[arXiv:1801.09052] [INSPIRE].
[66] A. Aharony, Y. Imry and S.K. Ma, Lowering of dimensionality in phase transitions with
random fields, Phys. Rev. Lett. 37 (1976) 1364 [INSPIRE].
[67] A.P. Young, On the lowering of dimensionality in phase transitions with random fields, J.
Phys. C 10 (1977) L257.
[68] Y. Imry and S.-K. Ma, Random-field instability of the ordered state of continuous
symmetry, Phys. Rev. Lett. 35 (1975) 1399 [INSPIRE].

[70] J.Z. Imbrie, Lower critical dimension of the random field Ising model, Phys. Rev. Lett. 53
(1984) 1747 [INSPIRE].
[71] J. Bricmont and A. Kupiainen, Lower critical dimension for the random field Ising model,
Phys. Rev. Lett. 59 (1987) 1829 [INSPIRE].
[72] J. Bricmont and A. Kupiainen, Phase transition in the 3d random field Ising model,
Commun. Math. Phys. 116 (1988) 539.
[73] F. Kos, D. Poland, D. Simmons-Duffin and A. Vichi, Precision islands in the Ising and
O(N ) models, JHEP 08 (2016) 036 [arXiv:1603.04436] [INSPIRE].
[74] D. Simmons-Duffin, The lightcone bootstrap and the spectrum of the 3d Ising CFT, JHEP
03 (2017) 086 [arXiv:1612.08471] [INSPIRE].
[75] T.C. Lubensky and J. Isaacson, Statistics of lattice animals and dilute branched polymers,
Phys. Rev. A 20 (1979) 2130 [INSPIRE].
[76] G. Parisi and N. Sourlas, Critical behavior of branched polymers and the Lee-Yang edge
singularity, Phys. Rev. Lett. 46 (1981) 871 [INSPIRE].
[77] H.-P. Hsu, W. Nadler and P. Grassberger, Simulations of lattice animals and trees, J. Phys.
A 38 (2005) 775 [cond-mat/0408061].
[78] J. Cardy, Lecture on branched polymers and dimensional reduction, cond-mat/0302495.
[79] S.-N. Lai and M.E. Fisher, The universal repulsive-core singularity and Yang-Lee edge
criticality, J. Chem. Phys. 103 (1995) 8144.
[80] Y. Park and M.E. Fisher, Identity of the universal repulsive-core singularity with Yang-Lee
edge criticality, Phys. Rev. E 60 (1999) 6323.
[81] M.E. Fisher, Yang-Lee edge singularity and φ3 field theory, Phys. Rev. Lett. 40 (1978) 1610
[INSPIRE].
[82] A.J. Bray and M.A. Moore, Scaling theory of the random-field Ising model, J. Phys. C 18
(1985) L927.
[83] D.S. Fisher, Scaling and critical slowing down in random-field Ising systems, Phys. Rev.
Lett. 56 (1986) 416 [INSPIRE].
[84] A.V. Goldberg and R.E. Tarjan, A new approach to the maximum-flow problem, J. ACM
35 (1988) 921.
[85] A.A. Middleton, Critical slowing down in polynomial time algorithms, Phys. Rev. Lett. 88
(2001) 017202.

– 107 –

JHEP03(2021)219

[69] J.Z. Imbrie, The ground state of the three-dimensional random field Ising model, Commun.
Math. Phys. 98 (1985) 145 [INSPIRE].

## PDF page 111

[86] A.A. Middleton and D.S. Fisher, Three-dimensional random-field Ising magnet: interfaces,
scaling, and the nature of states, Phys. Rev. B 65 (2002) 134411.
[87] J. Villain, Equilibrium critical properties of random field systems: new conjectures, J. Phys.
France 46 (1985) 1843.
[88] D. Lancaster, E. Marinari and G. Parisi, Weighted mean-field theory for the random field
Ising model, J. Phys. A 28 (1995) 3959 [cond-mat/9412069].
[89] K.J. Wiese, Lecture notes on selected topics in statistical field theory,
http://www.phys.ens.fr/∼wiese/masterENS/, (2020).

[91] D.S. Fisher, Interface fluctuations in disordered systems: 5 − ϵ-expansion and failure of
dimensional reduction, Phys. Rev. Lett. 56 (1986) 1964 [INSPIRE].
[92] M. Tissier and G. Tarjus, Nonperturbative functional renormalization group for random
field models. III: superfield formalism and ground-state dominance, Phys. Rev. B 85 (2012)
104202 [arXiv:1110.5495] [INSPIRE].
[93] M. Baczyk, G. Tarjus, M. Tissier and I. Balog, Fixed points and their stability in the
functional renormalization group of random field models, J. Stat. Mech. 1406 (2014)
P06010 [arXiv:1312.6375] [INSPIRE].
[94] V. Gorbenko, S. Rychkov and B. Zan, Walking, weak first-order transitions, and complex
CFTs, JHEP 10 (2018) 108 [arXiv:1807.11512] [INSPIRE].
[95] V. Gorbenko, S. Rychkov and B. Zan, Walking, weak first-order transitions, and complex
CFTs II. Two-dimensional Potts model at Q > 4, SciPost Phys. 5 (2018) 050
[arXiv:1808.04380] [INSPIRE].
[96] E.S. Fradkin, Application of functional methods in quantum field theory and quantum
statistics. I. Divergence-free field theory with local non-linear interaction, Nucl. Phys. 49
(1963) 624 [INSPIRE].
[97] S. Giombi, R. Huang, I.R. Klebanov, S.S. Pufu and G. Tarnopolsky, The O(N ) model in
4 < d < 6: instantons and complex CFTs, Phys. Rev. D 101 (2020) 045013
[arXiv:1910.02462] [INSPIRE].
[98] E. Brézin and C.D. Dominicis, Interactions of several replicas in the random field Ising
model, Eur. Phys. J. B 19 (2001) 467 [cond-mat/0007457].
[99] G. Parisi and N. Sourlas, Scale invariance in disordered systems: the example of the
random-field Ising model, Phys. Rev. Lett. 89 (2002) 257204 [cond-mat/0207415].
[100] M.C. Angelini, C. Lucibello, G. Parisi, F. Ricci-Tersenghi and T. Rizzo, Loop expansion
around the Bethe solution for the random magnetic field Ising ferromagnets at zero
temperature, Proc. Nat. Acad. Sci. 117 (2020) 2268 [arXiv:1906.04437] [INSPIRE].
[101] M. Gofman, J. Adler, A. Aharony, A.B. Harris and M. Schwartz, Critical behavior of the
random-field Ising model, Phys. Rev. B 53 (1996) 6362.
[102] S. Kehrein, F. Wegner and Y. Pismak, Conformal symmetry and the spectrum of anomalous
dimensions in the N vector model in 4 − ϵ dimensions, Nucl. Phys. B 402 (1993) 669
[INSPIRE].

– 108 –

JHEP03(2021)219

[90] L. Balents, Lecture notes on glassy phases and dynamics of randomly pinned elastic media,
http://online.kitp.ucsb.edu/online/lnotes/balents/, (1996).

## PDF page 112

[103] S.K. Kehrein, The spectrum of critical exponents in φ2 in two-dimensions theory in
D = (4 − ϵ)-dimensions: resolution of degeneracies and hierarchical structures, Nucl. Phys.
B 453 (1995) 777 [hep-th/9507044] [INSPIRE].
[104] J. Cardy, Scaling and renormalization in statistical physics, Cambridge University Press,
Cambridge, U.K. (1996).
[105] H. Kleinert and V. Schulte-Frohlinde, Critical properties of φ4 -theories, World Scientific,
Singapore (2001).
[106] M.S. Costa and T. Hansen, Conformal correlators of mixed-symmetry tensors, JHEP 02
(2015) 151 [arXiv:1411.7351] [INSPIRE].

[108] E. Lauria, M. Meineri and E. Trevisani, Spinning operators and defects in conformal field
theory, JHEP 08 (2019) 066 [arXiv:1807.02522] [INSPIRE].
[109] P. Cvitanović, Group theory: birdtracks, Lie’s and exceptional groups, Princeton University
Press, Princeton, NJ, U.S.A. (2008).

– 109 –

JHEP03(2021)219

[107] M.S. Costa, T. Hansen, J. Penedones and E. Trevisani, Projectors and seed conformal blocks
for traceless mixed-symmetry tensors, JHEP 07 (2016) 018 [arXiv:1603.05551] [INSPIRE].
