Source: https://doi.org/10.1007/JHEP08(2022)290
PDF sha256: f50637a20567be8de1804efc1e2f292b6a953a1526c016cab53bac2dadf92e04
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of kaviraj_2022_jhep08_290_random_field_phi3.pdf

Transcription of `kaviraj_2022_jhep08_290_random_field_phi3.pdf` in this directory, 51 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-51 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: July 11, 2022
Accepted: August 6, 2022
Published: August 29, 2022

Random field φ3 model and Parisi-Sourlas
supersymmetry

a

Institut de Physique Théorique Philippe Meyer, Université PSL, CNRS,
Sorbonne Université, Université de Paris,
F-75005 Paris, France
b
Laboratoire de Physique de l’Ecole normale supérieure, ENS, Université PSL, CNRS,
Sorbonne Université, Université de Paris,
F-75005 Paris, France
c
DESY Hamburg, Theory Group,
Notkestraße 85, D-22607 Hamburg, Germany
d
CPHT, CNRS, Ecole Polytechnique, IP Paris,
F-91128 Palaiseau, France

E-mail: apratim.kaviraj@desy.de, emilio.trevisani.et@gmail.com
Abstract: We use the RG framework set up in [1] to explore the φ3 theory with a random
field interaction. According to the Parisi-Sourlas conjecture this theory admits a fixed
point with emergent supersymmetry which is related to the pure Lee-Yang CFT in two less
dimensions. We study the model using replica trick and Cardy variables in d = 8 − ϵ where
the RG flow is perturbative. Allowed perturbations are singlets under the Sn symmetry
that permutes the n replicas. These are decomposed into operators with different scaling
dimensions: the lowest dimensional part, ‘leader’, controls the RG flow in the IR; the
other operators, ‘followers’, can be neglected. The leaders are classified into: susy-writable,
susy-null and non-susy-writable according to their mixing properties. We construct low
lying leaders and compute the anomalous dimensions of a number of them. We argue that
there is no operator that can destabilize the SUSY RG flow in d ≤ 8. This agrees with
the well known numerical result for critical exponents of Branched Polymers (which are in
the same universality class as the random field φ3 model) that match the ones of the pure
Lee-Yang fixed point according to dimensional reduction in all 2 ≤ d ≤ 8. Hence this is a
second strong check of the RG framework that was previously shown to correctly predict
loss of dimensional reduction in random field Ising model.
Keywords: Random Systems, Renormalization Group, Scale and Conformal Symmetries
ArXiv ePrint: 2203.12629

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

https://doi.org/10.1007/JHEP08(2022)290

JHEP08(2022)290

Apratim Kaviraja,b,c and Emilio Trevisanib,d

## PDF page 2

Contents
1

2 The RG flow of random field models
2.1 Method of replicas and Cardy transform
2.2 RG in Cardy variables
2.3 Emergence of supersymmetry for RF φ3 at small ϵ = 8 − d
2.4 Dimensional reduction

3
4
7
9
11

3 Classifying perturbations
3.1 Susy-writable leaders
3.2 Susy-null leaders
3.3 Non-susy-writable leaders

12
13
16
17

4 Stability of the SUSY fixed points

19

5 Discussion

22

A Review of branched polymers and lattice animals

26

B Classification of leaders in RF φ3 theory
B.1 Nφ = 1
B.2 Nφ = 3
B.3 Nφ = 5
B.4 Nφ = 7

33
35
35
36
37

C Box operators

37

D RG computations
D.1 Wavefunction renormalization
D.2 Beta function
D.3 Renormalization of local operators
D.3.1 Anomalous dimension of ϕ, ω, χ
D.3.2 Susy-null leaders
D.3.3 Non-susy-writable leaders
D.3.4 Susy-writable leaders

38
39
40
41
42
42
43
44

–i–

JHEP08(2022)290

1 Introduction

## PDF page 3

1

Introduction

Physical systems with randomly distributed impurities can be modelled through disordered
quantum field theories. Random Field (RF) models constitute a class of such theories where
a disorder field is coupled to a local order parameter. We are interested in the simplest RF
models described by the following continuous action
S[φ, h] =

∫

dd x

[1

2

]

(∂µ φ)2 + V (φ) + h(x)φ(x) ,

(1.1)

1. Emergence of supersymmetry: the IR fixed point of the RF theory is equivalent to
the fixed point of a nonunitary supersymmetric theory (with supercharges that do
not transform in a spinor representation). This is the Parisi-Sourlas CFT.
2. Dimensional reduction: the correlation functions of the SUSY CFT restricted to a
d − 2 hyperplane are equal to those of a d − 2 dimensional CFT with the same action
as the disordered model but without the disorder.
The above implies that critical exponents of a RF model should be the same as those of
a CFTd−2 . However this is not always true as found in the RFIM case from a number
of numerical studies. Indeed the model shows dimensional reduction from 5 → 3 [5, 6]
but not for 4 → 2 [7] or 3 → 1.1 This means that one of the two parts of Parisi-Sourlas
mechanism should stop working for RFIM at some intermediate dimension. In [8] part 2 of
the conjecture was explored in the framework of axiomatic CFTs. It was shown that there
was no issue with dimensional reduction in the Parisi-Sourlas SUSY CFT.
1

The case 3 → 1 cannot work as there is no phase transition for Ising model in 1d.

–1–

JHEP08(2022)290

where the disorder field h is coupled to a single scalar field φ for a given potential V .
This continuous description conveniently captures the physics of the theory near the phase
transition, where the microscopic details of the model are inconsequential. Typically the
disorder field is chosen to be Gaussian, with a zero mean. Physical observables are obtained
by taking correlation functions ⟨A(φ)⟩h for a given configuration of h and then computing
their average ⟨A(φ)⟩h over the disorder. The disordered coupling is relevant if ∆φ < d2 .
This is called Harris criterion. Since ∆φ = d−2
2 + η (with η ≪ 1) close to the usual upper
critical dimension, the disorder is strongly relevant and changes the universality class of the
critical system.
A notable example of RF theories is the Random Field Ising Model (RFIM), which
can be defined on the lattice by adding to the usual Ising model a term which couples the
disorder field to a local Ising spin. This corresponds to V (φ) ∝ φ4 in the action above. In
this paper we focus on another important example: random Field φ3 model (denoted RF
φ3 model), where we set V (φ) ∝ φ3 . We discuss it in a moment. The analysis for both φ4
and φ3 potentials appeared in a shorter paper [2].
In [3] it was first suggested that RF theories of the type (1.1) have a phase transition
with an interesting feature: its critical point is related to that of the same system without
disorder in d − 2 dimension. This was explained by a conjecture due to Parisi and Sourlas
in 1979 [4], in the context of RFIM. The conjecture has two essential parts:

## PDF page 4

Part 1 of the conjecture was explored in [1]. A perturbative RG framework was set up
to study the model. It was shown that the emergent SUSY fixed point ot the RFIM is in
fact unstable below a critical dimension. The key points of the analysis were the following:
• One represents the RF model by using a replica Lagrangian. In this formulation, the
disorder field is integrated out and one is left with a pure quantum field theory of n
coupled fields φi=1,...n in the limit n → 0.

• Near the upper critical dimension duc the model is described by a Gaussian action
perturbed by a weakly relevant interaction. This gives rise to an IR fixed point
equivalent to the Parisi-Sourlas SUSY CFT.
• There is an infinite number of other perturbations, that are irrelevant close to d = duc .
The fixed point would become unstable if any of these perturbations becomes marginal
at d < duc .
• The perturbations are all Sn -singlets i.e. invariant under the Sn symmetry that
permutes the n replicas. These singlets (like the fields φi themselves) do not have well
defined scaling dimensions. Indeed, after Cardy transform, they can be written as a
sum of operators of different dimensions. The lowest dimensional part of the singlet
is called “leader operator”, the other parts are named “followers”.
• The leader operators fully control the behaviour of the Sn -singlet perturbations in
the IR. It is therefore enough to study the anomalous dimensions of leaders (in a
theory —dubbed LL — where all followers are set to zero) to know if the Sn -singlet
perturbations are relevant or irrelevant.
• The leader operators are further classified into 3 categories: susy-writable, susy-null
and non-susy-writable.
• The anomalous dimensions of a number of low dimension leader operators in each
category were computed in [1]. This showed that a few Sn -singlet perturbations
do become marginal at some critical dimensions estimated as dc = 4.2 − 4.7 thus
rendering the fixed point unstable at d < dc .
We review the framework in detail in section 2. The result of the above RG framework
nicely explains when and why dimensional reduction works for the RFIM. If the framework
is correct it should also be applicable to other known cases giving results consistent with
the numerical predictions. In this paper we test the above framework on the RF φ3 model.
Let us briefly review some features of this model. First let us consider the pure version
of the RF φ3 theory. This is described by the scalar φ3 theory which has upper critical

–2–

JHEP08(2022)290

• The fields φi do not have a well defined scaling even in the Gaussian theory (for
V = 0). This is problematic for RG purposes. It is thus convenient to perform a
linear map in field space [9], dubbed Cardy transform, which gives rise to a set of
fields with well defined scaling dimensions.

## PDF page 5

2

The RG flow of random field models

In this section we investigate how SUSY emerges in the RG flow of a RF model. In order
to study this question we follow the logic of [1], summarized in figure 1. We start the next
subsection by reviewing how to compute quenched disorder correlation functions through
the method of replicas [20]. We then define a transformation in field space (first introduced

–3–

JHEP08(2022)290

dimension duc = 6. This theory has a microscopical description realized by considering
the Ising model in an imaginary magnetic field. The critical properties of the model are
captured by the well-known Lee-Yang universality class [10–13].
Once we add the disorder, by the Harris criterion, the fixed point must be in a different
universality class. Interestingly the universality class of the RF φ3 fixed point describes
the critical properties of branched polymers in a solution. Branched polymers are defined
as polymers —long chains of single units called monomers— which branch into other
polymers. Depending on the interactions between the parts of the chain they can appear in
extended or collapsed configurations. One can study the properties of the polymers near
the transition between these two phases. It is also possible to define the branched polymers
on the lattice as connected clusters of sites called ‘Lattice Animals’. The number of their
possible configurations and their average size, scale with some critical exponents that are
known from Monte-Carlo for all dimensions 2 ≤ d < 8 [14, 15]. Lubensky and Isaacson [16]
proposed that branched polymers can also be described in field theory with the n → 0 limit
of a Replica Lagrangian with cubic interaction that allows perturbative computations in
d = 8 − ϵ (see appendix A for a review). Parisi and Sourlas [17] showed that this Lagrangian
also describes the RF φ3 model. Through the Parisi-Sourlas conjecture this is related to
Lee-Yang fixed point without disorder in d − 2 dimensions. Critical exponents in the lower
dimensional theory are known from both perturbative computations (in 6 − ϵ dimensions)
and Monte-Carlo. They agree with the branched polymer critical exponents, showing that
both parts of Parisi-Sourlas conjecture indeed work for this model.
The fact that Parisi-Sourlas conjecture works in this model is supported by the result
of Brydges and Imbrie [18] who found a manifestly supersymmetric model of Branched
polymers, where the dimensional reduction can be rigorously shown (see [19] for a review).
However that analysis does not explain why a generic non-supersymmetric model should
also have a SUSY fixed point, namely why SUSY breaking perturbations are irrelevant (see
appendix A.4 of [1] for more details on this point). Therefore one important goal of this
paper is to explain using the RG analysis of [1] how RF φ3 fixed point flows to a stable
SUSY fixed point that admits dimensional reduction in all allowed dimensions d < 8.
The rest of the paper is organized as follows: in section 2 we review the RG framwork
of [1] focusing on the RF φ3 theory. We introduce ‘leader’ and ‘follower’ operators and show
how the SUSY fixed point arises. In section 3 we classify all the leader operators into three
categories. In each category we compute the anomalous dimensions of the ones that have
low classical dimensions and break SUSY. In section 4 we use the results to argue that the
SUSY fixed point is stable. We conclude in section 5. There are four appendices that show
various technical details and computations.

## PDF page 6

Random
Field

Replica
Trick

SUSY
Cardy
Transform

Leader
Theory

Figure 1. A flowchart summarizing the RG framework of [1] for a random field model.

by Cardy [9]) which makes the scaling properties of the UV Gaussian fixed point more
transparent. In section 2.2 we explain how to do RG in these new variables and we show
that the IR properties of the model are captured by the “leader theory”, which is specified
by a simpler Lagrangian LL . Thanks to this formulation we can easily classify the spectrum
of the theory and see which perturbations are relevant and whether they give rise to a
SUSY IR fixed point or not. In subsection 2.3 we will focus on the case in which ϵ = 8 − d is
small and we will easily show that LL can be mapped to a SUSY model with Parisi-Sourlas
supersymmetry. Finally in subsection 2.4 we explain that the resulting SUSY model can be
dimensionally reduced to a non-SUSY theory in d − 2 dimensions. In principle, when ϵ is of
order one, new relevant SUSY breaking operators could destabilize the SUSY fixed point,
as it happens for the RFIM. This scenario for RF φ3 will be considered and ruled out in
sections 3 and 4.
2.1

Method of replicas and Cardy transform

Quenched averaged correlators are defined by first averaging over the field φ and in the end
over the random magnetic field h
⟨A(φ)⟩ =

∫

Dh P(h)

1
Zh

∫

Dφ A(φ)e−S[φ,h] ,

(2.1)

where overbar denotes the disorder average with distribution P(h), S[φ, h] is the random field
action introduced in (1.1) and A(φ) is a function of the field φ, e.g. A(φ) = φ(x1 ) . . . φ(xn ).
1 ∫ d
In this paper we will focus on a gaussian disorder distribution P(h) ∝ exp(− 2H
d x h(x)2 ).
Because of the presence of the denominator Zh , equation (2.1) is notoriously complicated
to compute. The method of replicas is a prescription to compute these correlation functions
by eliminating the factor Zh−1 .
The idea is to multiply and divide the integrand of (2.1) by Zhn−1 . The resulting
equation is independent of n, thus we can take the limit n → 0, where the denominator
Zhn → 1. The Zhn−1 in the numerator is instead considered as a product of partition
functions for fields φ2 , . . . φn which combine with the original functional integral where φ is

–4–

JHEP08(2022)290

SUSY

## PDF page 7

renamed φ1 . The net result is that we get rid of the denominator Zh at the price of having
n replica fields φ1 , . . . , φn . The advantage of this trick is that the average over h is now
just a Gaussian integral which can be performed giving
⟨A(φ)⟩ = lim

∫

n→0

⃗ =
Sn [φ]

∫

dd x

⃗

⃗ A(φ1 )e−Sn [φ] ≡ ⟨A(φ1 )⟩,
Dφ

⎧
n [
⎨∑
1
⎩

i=1

H
(∂µ φi )2 + V (φi ) −
2
2
]

( n
∑

φi

(2.2)
)2 ⎫
⎬

.

(2.3)

⎭

i=1

⟨A1 (φ)⟩ · · · ⟨AN (φ)⟩ = lim

n→0

∫

⃗

⃗ A1 (φi ) . . . AN (φi )e−Sn [φ] = ⟨A1 (φi ) . . . AN (φi )⟩,
Dφ
1
1
N
N

(2.4)
where the result is independent of the choice of indices i1 , . . . , iN as long as they are all
different. While the definition (2.1) eludes the standard QFT framework because of the
average over disorder, the reformulation in (2.2)–(2.4) is conveniently written in terms a
QFT of n coupled fields (the only subtlety being the limit n → 0). This formulation is thus
well suited to study the RG of the theory.
From the quadratic part of Sn we obtain the propagator
G=

1
HM
+ 2 2
,
2
k
k (k − nH)

(2.5)

where M is an n × n matrix whose all elements are equal to one. We see that, in the limit
n → 0, the two terms in the r.h.s. of (2.5) have different scalings in k. This in turns implies
that the fields φi at the UV fixed point do not possess a definite scaling dimension. The
idea of Cardy [9] is to disentangle the two scaling behaviors through a linear transformation
in field space. The Cardy transform is defined as follows
1
ϕ = (φ1 + ρ),
2

ω = φ1 − ρ ,

χ i = φi − ρ ,

(i = 2 . . . n) ,

(2.6)

1
with ρ = n−1
(φ2 + . . . + φn ). By construction, the variables χi are not independent and
∑
satisfy the constraint ni=2 χi = 0. The quadratic Lagrangian in n → 0 limit thus becomes

Lfree = ∂ϕ∂ω −

H 2 1
ω + (∂χi )2 ,
2
2

(2.7)

where from now on we leave implicit the sum over χi , where i runs from 2 to n. We
borrowed the notation LL from [1] and the superscript ‘free’ denotes the V (φ) = 0 case.
The transformed fields ω, ϕ, χi have now well-defined scaling dimensions:
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

(2.8)

Notice that the dimension of ϕ is one unit below the unitarity bound, signaling that the
resulting theory is actually non unitary. By inverting the kinetic term we then obtain the

–5–

JHEP08(2022)290

We can also generalize this construction to compute the disorder-average of a product
of several correlators as follows

## PDF page 8

free propagators, which are now scale-covariant
1
1
⟨ωω⟩ = 0,
⟨(χi )k (χj )−k ⟩ = 2 δij −
Πij .
k
n−1
(2.9)
Here Πij is an (n − 1) × (n − 1) matrix whose components are all equal to one. In this
new basis the powers 1/k 2 and 1/k 4 of (2.5) appear separated. Notice that to get such a
neat separation we had to work at n = 0. Let us show that indeed order n terms are not
important to study the RG of the random field model.
To model this problem we consider a Lagrangian L independent of n perturbed by a
relevant operator O with dimension ∆ < d, which is multiplied by a coupling g of order n
(which we think as a small parameter),
H
⟨ϕk ϕ−k ⟩ = 4 ,
k

1
⟨ϕk ω−k ⟩ = 2 ,
k

(

Λd−∆
UV

∫

dd x O(x),

(2.10)

with ΛUV the UV cutoff energy scale and g ∝ n. For our problem L is a Lagrangian obtained
by setting n = 0 (e.g. the Gaussian Lagrangian Lfree , where we are also allowed to turn on
any number of n = 0 perturbations discussed in the next sections) while O is any relevant
operator that enters at order n (there are many of such operators e.g. ϕ2 ). We want to see
what happens to the RG of L when n is small and understand how we are supposed to
think of a line of theories parametrized by n which are smoothly connected to the n = 0
theory (indeed this is what we are supposed to have when we use the method of replica).
This is non trivial since there are two conflicting effects: on one hand g looks unimportant
because g ∝ n is small in the UV, on the other hand g is a relevant coupling, thus it should
grow and become important in the IR. Let us explain how we should understand these
fighting effects. The coupling g —which in the UV was order-n — grows along the RG and
becomes order-1 at a scale
1
ΛIR ∼ n d−∆ ΛUV .
(2.11)
At scales Λ ≲ ΛIR the flow is no longer perturbative and we have no means to predict the
fate of the theory (which may flow to a gapped phase or to new fixed point). Formula (2.11)
thus tells us that any fix point of the n = 0 RG is ultimately unstable with respect to order
n perturbations. So in practice no matter how small n is, the coupling g will eventually
become large and destabilize the n = 0 RG. One could then think that it is not possible to
find a smooth interpolation between the n > 0 theories with and the n = 0 one. On the
contrary, in the following we explain how this can be done.
Indeed, as n approaches zero, the scale (2.11) (at which g ∼ 1) becomes smaller and
smaller. In practice the n ≪ 1 instabilities are only triggered at parametrically large
distances. This indicates that we should only focus on the regime Λ ≳ ΛIR . Because of
the IR cutoff at these scales we can only reach approximate scale invariance. However by
lowering n we are able to make the approximate scale invariant region larger and larger,
finally reaching a true fixed point at n = 0 (which is the one of L theory).
Very importantly in the regime Λ ≳ ΛIR all (2.10) contributions are perturbative. They
appear as a Taylor series in n which can be dropped when taking the limit n → 0. It is

–6–

JHEP08(2022)290

g

)

## PDF page 9

thus possible to drop them from the start. In summary from now on we are allowed to
consider the theory at strictly n = 0 and drop all perturbations that which are proportional
to n. This is going to be assumed in the rest of the paper.
2.2

RG in Cardy variables

σk ≡

∑

φki ,

σk(µν) ≡

∑

φk−1
∂µ ∂ν φi ,
i

σk(µ) ≡

∑

φk−1
∂µ φi ,
i

σk(µ)(ν) ≡

∑

φk−2
∂µ φi ∂ν φi ,
i

(2.12)

and so on. On the other hand in order to use the results of the previous section, we need to
rewrite the Sn -singlet operators in Cardy variables. To do so we simply use (2.6) and we set
n = 0. The lowest dimensional singlets in Cardy basis are the following quadratic operators 2
σ2(µ)(µ) = ∂ϕ∂ω + 12 (∂χi )2 ,
(2.13)

σ12 = ω 2 ,
σ2 = 2ϕω + χ2i .

We see that σ2(µ)(µ) and σ12 generate the Gaussian Lagrangian Lfree of (2.7).3 Since they
generate the kinetic terms, they are by definition always marginal. The perturbation σ2
instead has scaling dimensions d − 2, thus it is always strongly relevant. It takes the role of
a mass term, which we need to tune to zero in order to reach an IR fixed point. The next
perturbation is σ3 which appears due to the potential V (φ) = g6 φ3 of the perturbed UV
action (2.3). In Cardy variables it takes the form
[

]

σ3 = 3ϕ2 ω + 3ϕχ2i 3d
2

[

−4

]

+ χ3i 3d
2

−3

−

3[ 2 ]
1 [ 3]
χi ω 3d +
ω 3d .
−2
2
4
2
2

(2.14)

Here the subscript of the square brackets indicate the bare dimensions of the composite
operators computed by summing the dimensions of the fields ϕ, χi , ω in (2.8). We thus
2

In principle one can also consider the perturbation σ1 = ω. This however does not play any role, since
it can be reabsorbed in the Gaussian Lagrangian (2.7) by a shift of fields, ω → ω + const. Indeed, as we
will explain in appendix B, this perturbation is equivalent to the perturbation φ̂ in φ̂3 theory, which is also
discarded because it can be reabsorbed by a shift of φ̂.
3
It is important to see that the two terms belong to different Sn -singlets, so the relative coefficient
is allowed to change along an Sn -preserving RG flow. This is not a problem since the IR fixed point is
independent of such relative rescaling, as it is explained in section 3 of [1].

–7–

JHEP08(2022)290

In the previous section we showed how the gaussian Lagrangian at n = 0 takes a nice form
in Cardy variables. The next step is to consider the RG of the theory.
Independently of the form of the potential, the replica action (2.2) is Sn symmetric. In
order to study the RG of (2.2) we should consider all possible perturbations compatible
with Sn , and possible extra symmetries if they are not broken by the form of the potential.
E.g. in [1] a quartic potential was considered, which allowed for an extra Z2 symmetry. In
this work we will consider a cubic potential V (φ) = φ3 in (2.2), thus the Z2 symmetry will
not be present.
Sn symmetric preturbations are easily written in terms of the replica fields, e.g.

## PDF page 10

conclude that the singlet σ3 can be written as a sum of operators of different dimensions,
which is actually a recurrent feature of the model. While looking very exotic, this feature
should be expected. Indeed, as we stressed in the previous section, the fields φi which are
used to define the Sn singlets do not have a well-defined scaling dimension. Thus we do
not expect to find that combinations of φi give operators with definite dimensions. The
quadratic operators in (2.13) should be considered as exceptions to this rule. In general
a given Sn singlet perturbation O is written in Cardy basis as a sum of operators of
different dimensions
O = OL + OF 1 + OF 2 + . . . ,
(2.15)

g(OL + OF1 + OF2 + . . . )

−→

integrating out

g̃(OL + OF1 + OF2 + . . . ) .

(2.16)

Here g is the coupling associated to O at a scale Λ, while g̃ is new coupling after integrating
out the momentum shell from [Λ′ , Λ]. Second, when we rescale back to initial form of the
action we see that the relative coefficients get rescaled differently and follower operators are
more and more suppressed as we go to the IR,
1
1
g̃(OL + OF1 + OF2 + . . . ) −→ g(b)(OL + OF1 + 2 OF2 + . . . ) .
rescaling
b
b

(2.17)

In particular in the deep IR, b → ∞ and all follower operators are set to zero with respect
to the leader. We can define an RG equation for the perturbation O as the variation of g(b)
in the RG scale b. Close to the fixed point this can be linearized as follows,
dg(g)
= −yO g(b) .
d log b

(2.18)

From this construction it should be clear that the eigenvalue yO can be computed in a
very simple way: it is obtained as yO = ∆OL − d where ∆OL is the scaling dimension of
the leader operator OL computed in a simpler theory —which we call LL — defined by
dropping all follower operators. This is a remarkable conclusion. It gives us a very simple
algorithm to check if an Sn perturbation is relevant or not. The strategy is to construct
the Sn perturbations, map them in Cardy variables and drop all the follower contributions.

–8–

JHEP08(2022)290

where we distinguish its lowest dimensional piece OL which we call leader from all the higher
dimensional terms OFk which we dub followers, where the follower OFk has dimension
k-units bigger than OL . As it should be clear from what follows, this difference in dimension
does not renormalize, so the difference between the dimensions of a leader and its followers
is the same in the UV and in the IR.
It is easy to see that leaders play a much more important role than followers to
characterize the IR properties of the RG. This can be shown in two steps. First, due to
Sn symmetry, the form of the multiplet must be preserved when integrating out degrees of
freedom. E.g. if we introduce a momentum cutoff Λ and we integrate out the momentum
shell [Λ′ , Λ], where Λ/Λ′ ≡ b > 1, the form of O is not allowed to change, meaning that the
relative coefficients between OL and the OFk remain fixed and only the overall coupling is
allowed to change,

## PDF page 11

O1 − O2 = 0 + (O1F1 − O2F1 ) + (O1F2 − O2F2 ) + . . . .

(2.19)

The new Sn perturbation O1 − O2 has a leader (O1F1 − O2F1 ) which clearly has a different
scaling dimension with respect to O1L , thus (O1 − O2 ) and O1 are not degenerate preturbations. When we say that LL is a theory of leader operators, we mean that one should first
diagonalize the Sn perturbations as above and only then one is allowed to set the follower
operators to zero. In appendix B we construct such a diagonalized basis for the low lying
Sn perturbations Oi where each perturbation is associated to a distinct leader OiL . The
resulting basis of OiL defines the possible low lying perturbations of the theory LL .
2.3

Emergence of supersymmetry for RF φ3 at small ϵ = 8 − d

If we work in d = 8 − ϵ (for ϵ ≪ 1), it is easy to see that the full list of relevant leaders
in the theory LL is given by the quadratic terms in (2.13) plus the leader (σ3 )L . The
Landau-Ginzburg Lagrangian thus takes the simple form4
(
) g(
)
1
H
ϕ2 ω + ϕχ2i ,
LL = ∂ϕ∂ω − ω 2 + (∂χi )2 + m2 2ϕω + χ2i +
2
2
2
[

]

(2.20)

Beside the strongly relevant mass term, which must be tuned to zero to reach the IR
fixed point, the Lagrangian (2.20) has the single weakly relevant perturbation (σ3 )L , which
triggers a short RG flow which can be studied perturbatively. This Lagrangian will thus be
the starting point for all the following computations.
4

Using (2.8) it is easy to see that the dimension of the interaction is [ϕ2 ω] = [ϕχ2i ] = 3d
− 4 which
2
is equal to 8 − 3ϵ
in
d
=
8
−
ϵ
and
therefore
is
always
relevant
for
any
ϵ
>
0.
The
Lagrangian
(2.20) is
2
renormalizable and contains all possible relevant perturbations in d = 8 − ϵ for ϵ ≪ 1.

–9–

JHEP08(2022)290

By studying the anomalous dimensions of the leader operators in the LL theory we are
then able to see if yO > 0 and thus the Sn perturbation falls off in the IR, or if yO < 0 and
the perturbation grows. E.g. to study the IR effect of the perturbation σ3 , we should only
consider its leader piece 3ϕ2 ω + 3ϕχ2i , which has bare dimension 3d
2 − 4 and thus gives rise
to a weakly relevant perturbation in d = 8 − ϵ dimensions. In the next section we will detail
what happens to the IR fixed point of this RG flow. Before ending this section we shall
make a final remark about the LL theory.
Of course, as it is written, equation (2.18) works when there are no other degenerate (i.e.
of the same scaling dimension) perturbations. As expected, when some Sn perturbations Oi
i (g)
have degenerate leaders OiL , one gets coupled equations of the form dg
d log b = −(yO )ij gj (b)
where yO is a mixing matrix which must be diagonalized to obtain the eigenvalues of the
correct IR scaling perturbations. However one should be careful because sometimes the
chosen basis for Oi is such that two distinct perturbations O1 , O2 have the same leader
O1L = O2L (namely O1L and O2L do not only have the same dimensions but they are really
the same operator) and different followers. In this case it would not be correct to say that
the O1 and O2 are degenerate (for a detailed exemplification of why this is the case see
appendix B of [1]). In order to correctly diagonalize the RG one should change the basis of
Oi and consider as a new perturbation their difference,

## PDF page 12

Before entering the perturbative computations, we would like to show that many of the
observables of the theory (2.20) are captured by a SUSY Lagrangian. This in turns implies
that for small ϵ the random field φ3 model has an IR fixed point with emergent SUSY.
By looking at (2.20) one notices that χi only appear quadratically, thus the associated
partition function is defined through a Gaussian functional integral in the fields χi which
can be performed. The Gaussian path integral of n − 2 bosonic fields (there are n − 1
fields subjected to one constraint) in the limit n → 0 is equal to a fermionic Gaussian path
integral. This motivates the following replacement,
(2.21)

which is valid for any function f of the field ϕ, where ψ, ψ̄ are fermionic fields which transform
as Lorentz scalars i.e. they are not spinors. In other words we replace a Gaussian O(−2)
model by a Gaussian Sp(2) model, where O(−2)-singlets (χi )2 are replaced Sp(2)-singlets
(ψ ψ̄). The new fermionic action thus takes the form
[

Lsusy = ∂ϕ∂ω −

(
) g(
)
H 2
ω + ∂ψ∂ ψ̄ + 2m2 ϕω + ψ ψ̄ +
ϕ2 ω + 2ϕψ ψ̄ .
2
2
]

(2.22)

The Lagrangian Lsusy is invariant under a special kind of supersymmetry named after Parisi
and Sourlas [4]. In order to make SUSY manifest we can rewrite the action in superspace
as follows
[
]
∫
1
g
Ssuperspace = dd xdθ̄dθ − ΦD2 Φ + m2 Φ2 + Φ3 ,
(2.23)
2
6
where θ, θ̄ are fermionic coordinates (which also transform as Lorentz scalars), D2 ≡
∂ 2 − H∂θ ∂θ̄ is the super-Laplacian and the superfield Φ can be expanded in components as
Φ(x, θ, θ̄) = ϕ(x) + θψ̄(x) + θ̄ψ(x) + θθ̄ω(x) .

(2.24)

The supersymmetry enjoyed by Ssuperspace is the super-Poincaré group Rd|2 ⋊ OSp(d|2),
where Rd|2 denotes super-translations and OSp(d|2) super-rotations. In this theory the supersymmetry generators do not transform as spinors and thus the theory is non-unitary [8].5
One needs to be a bit careful with the map (2.21). While the path-integral of the two
theories is equal, the two theories are actually different since they have a different set of
operators. In particular operators that are not singlets under Sp(2) and O(−2) cannot be
mapped from one theory to the other. E.g. χki for k ̸= 2 has no counterpart in the Sp(2)
theory. Conversely e.g. ψ itself has no counterpart in the O(−2) theory. In appendix C
of [1] it was shown how to explicitly write a map between the singlet operators of the two
theories (this is not trivial since it is possible to map also composite operators which contain
derivatives, e.g. χi ∂µ χi ↔ ψ∂µ ψ̄ + ∂µ ψ ψ̄).
5

This setup avoids standard classifications of supersymmetric theories (e.g. [21]) that are based on
the assumption that supercharges transform as spinors and anticommute giving rise to the translation
operator (and to the special conformal generator in supercorformal theories). In particular Parisi-Sourlas
supersymmetric theories can exist in any dimension d and we will be interested in the case of d = 8 − ϵ.
See [8] for more details on Parisi-Sourlas supersymmetry.

– 10 –

JHEP08(2022)290

n
[
]
[
]
1∑
n→0
χi −∂ 2 + f (ϕ) χi −→ ψ −∂ 2 + f (ϕ) ψ̄ ,
2 i=2

## PDF page 13

Since the χ- and ψ-theories are somewhat different, one may wander if it is correct to
study the fixed point of the LL by using Lsusy . However, it is easy to see that this step is
completely rigorous. Indeed the Lagrangian LL had accidental O(−2) symmetry, therefore
along its RG flow only O(−2)-singlets can be produced. These can in turn be mapped to
Sp(2) singlets. Thus the RG flow of the two theories is restricted to live inside the subspace
of operators which exists (and it is equivalent) in both theories.
To be more pragmatic one can compute the beta function for g with
both Lagrangians (2.20) and (2.22), and obtain the same result (computed in
dimensional regularization):
( )
ϵg
3g 3 H
−
+
O
g5 ,
2
4(4π)4

(2.25)

where the mass term m is tuned to zero in order to reach the fixed point, which is given by
Hg⋆2 = −

( )
2(4π)4
ϵ + O ϵ2 .
3

(2.26)

We stress that the same fixed point is reached independently of the value of H (indeed
√
√
by rescaling ϕ → Hϕ and ω → ω/ H we can get rid of H in the kinetic terms of the
√
actions at the price of rescaling g → Hg). In practice we can consider Hg 2 as a single
coupling.6 At this fixed point we can easily compute the anomalous dimension for some
singlet operators and obtain the same result using both formulation (2.20) and (2.22). E.g.
ϵ
the one-loop anomalous dimension for ϕ and ω is γϕ = γω = − 18
(see appendix D.3.1).
Notice that these are equal as expected since they belong to the same SUSY multiplet in
the (2.22) formulation.
In this section we thus learned that for small ϵ = 8 − d the IR properties of the random
field φ3 model are captured by the leader Lagrangian LL , which can mapped using (2.21)
to the explicitly SUSY Lagrangian (2.22). We can conclude that for small ϵ the random
field φ3 model has emergent supersymmetry. The question that remains to answer is what
happens when ϵ is not small. Before entering this discussion we review a property of the
SUSY Lagrangian (2.22) which is going to be useful in the following.
2.4

Dimensional reduction

Theories with a Parisi-Sourlas type of supersymmetry like Ssuperspace in equation (2.23)
have a remarkable property: most of the observables of the theory can be described in terms
of a model living in dˆ = d − 2 dimensions which does not have any supersymmetry. More
precisely correlation functions of the d-dimensional SUSY theory with an interaction V (Φ)
ˆ
when restricted to a d-dimensional
spatial hyperplane are equal to correlation functions of
a scalar theory with the interaction V (φ̂) in dˆ dimensions. This map can be established for
general axiomatic CFTs just by using the superconformal symmetries [8].
To illustrate this map we consider a 2-point function,
⟨Φ(x1 , 0, 0)Φ(x2 , 0, 0)⟩ = ⟨ϕ(x1 )ϕ(x2 )⟩ = ⟨φ̂(x1 )φ̂(x2 )⟩ , (xi ∈ R) ,
6

(2.27)

An interesting observation is that by taking H negative it is possible to make the critical coupling
g⋆ real.

– 11 –

JHEP08(2022)290

βg = −

## PDF page 14

where the correlators in the l.h.s. is computed using (2.23) while the one in the r.h.s. is
computed in the theory:
4π
S=
H

∫

1
g
d x (∂ φ̂)2 + m2 φ̂2 + φ̂3 .
2
6
dˆ

[

]

(2.28)

The fixed point occurs at
g⋆2 = −

( )
2(4π)3
ϵ + O ϵ2 .
3

(2.30)

One can study anomalous dimensions of operators at this fixed point and get an exact
match with the ones computed using the SUSY formulation (2.22), e.g. γφ̂ = γϕ = γψ = γω .
This fact is going to be very useful in the following since it allows us to relate observables
of the SUSY theory (2.22) to the ones of the better studied and simpler φ̂3 -theory.

3

Classifying perturbations

For infinitesimal ϵ = 8 − d in the previous section we proved that the IR fixed point of the
RF φ3 model must be supersymmetric and should therefore undergo dimensional reduction.
This however may not be the case for larger values of ϵ. Indeed if ϵ is of order one, other
operators could in principle become relevant and destabilize the RG flow, as it happens
for RFIM [1]. Of course, as we reviewed in the introduction, numerical simulations are
compatible with dimensional reduction [17] and therefore we do not expect a destabilization
to occur. However it is interesting to see how this works out theoretically using the RG
setup described in the previous sections. With this in mind, in this section we study the
one-loop anomalous dimensions of a large set of operators. This information will then be
used in section 4 to check if the SUSY fixed point is indeed stable for the RF φ3 model at ϵ
of order one.
In order to achieve this goal we follow the strategy outlined in the previous section.
Namely we consider the Sn singlet perturbations of the Lagrangian (2.3) in the limit n → 0
which are simply captured by the leader perturbations of the model LL . The latter being
obtained by only considering the leading pieces of the Sn singlets when written in terms
of Cardy variables. So our objective is to systematically consider low-lying Sn singlets
and compute the anomalous dimensions of their associated leaders, checking if at (non
infinitesimal) values of ϵ they become relevant.
A large set of low-lying leaders is presented in appendix B. As we shall see, leaders can
be classified into 3 categories: 1. Susy-writable, 2. Susy-null, and 3. Non-susy-writable
operators. This classification is justified since the three types of leaders mix with themselves

– 12 –

JHEP08(2022)290

The φ̂3 -theory (2.28) is a quite well studied model that can even be found as a toy example
in some QFT textbooks (see e.g. [22] for a basic introduction and [23–25] for results at
higher loop orders). In dˆ = 6 − ϵ the one-loop beta function for g, after tuning m to zero, is
given by:
( )
ϵg
3g 3
βg = − −
+ O g5 .
(2.29)
3
2
4 (4π)

## PDF page 15

only in a triangular way. This can be schematically shown as below:
susy-null ↔ susy-null
susy-writable → susy-writable , susy-null
non-susy-writable → non-susy-writable , susy-writable , susy-null .

(3.1)

3.1

Susy-writable leaders

We refer to the operators invariant under O(n − 2) and which do not vanish after the
substitution χ → ψ (i.e. they become Sp(2) invariant after the substitution) as susy-writable
operators. They can thus be written in terms of the susy-fields ϕ, ψ, ψ̄, ω. Since for these
operators the map between χ and ψ is a bijection, with an abuse of language we sometimes
will refer to the operators already written in terms of ψ, ψ̄ variables as susy-writable
operators. However one should keep in mind that the actual operators are the ones defined
in terms of the χ fields.
Susy-writable leaders are the most frequent ones in the low lying spectrum of the LL
theory. This may sound surprising since they come from Sn singlets which do not have any
knowledge of the emergent supersymmetry of LL . The reason why this happens is that
∑
given an Sn singlet of the form ni=1 A(φi ) (for any function A) its leader can be written as
( n
∑
i=1

)

1
= A (ϕ)ω + A′′ (ϕ)χ2i .
2
[

A(φi )
L

′

]

(3.2)

This form is explicitly susy-writable, indeed it can be written as the highest component of
the composite superfield A(Φ), namely ∂θ ∂θ̄ A(Φ). Similarly, product of the leaders (3.2)
are still susy-writable. From this point of view it may in fact seem that only susy-writable
leaders exist in the theory. This is of course false as it is easy to see. Indeed very often two
operators built out of products of singlets of the form (3.2) have the same leader. In this case
the prescription of section 2.2 tells us that we should subtract them to obtain a subleading
contribution. The latter is either non-susy-writable or susy-null. Many examples of this
phenomenon are presented in appendix B. For more discussion see appendix B of [2].
It is important to stress that susy-writable leaders belong to a special class of susywritable operators. As we exemplified below equation (3.2), they can be written as the
highest components Oθθ̄ ≡ ∂θ ∂θ̄ O of superfields O. In other words, once written as susy
fields, they are invariant under super-translations. See [2] appendix B for a formal proof of
this statement.7
7

It was also shown in [2] that any Sp(2) and super-translation invariant operator is a susy-writable leader.

– 13 –

JHEP08(2022)290

This means a susy-null operator mixes only with other susy-null operators, a susy-writable
mixes with only susy-writables and susy-nulls, while a non-susy-writable operator mixes
with all 3 types. In other words a renormalized susy-null operator can be written as a linear
combination of only susy-null operators, and so on.
In the following we explain in detail how we define these three classes and we will
further compute the anomalous dimensions of the low lying operators of each class. Finally
in section 4 we will collect these results and we will comment on the stability of the SUSY
fixed point.

## PDF page 16

Sθθ̄ ,

Jθθθ̄θ̄ ,

Bθθθ̄θ̄,θθ̄ ,

...

(3.3)

where S is a superscalar, J ab transforms in the spin-2 representation and B ab,cd in the box
representation (2, 2) where (a, b) and (c, d) are the graded-symmetric pairs. The dots take
into account the contributions from other representations with more indices, e.g. (2, 2, 2),
(2, 2, 2, 2) and so on. In the following we will not consider the latter since all free theory
primaries in these representations have very high conformal dimensions (many fields and
many derivatives are needed to allow for the required antisymmetrizations). Notice also
that these higher irreps do not appear in integer dimensions d ≤ 5 —e.g. the dimension of
1
the representation (2, 2, 2) is equal to 144
(d − 5)(d − 1)d2 (d + 1)(d + 2) and vanishes for
d = 5. On the other hand they exist in non-integer dimensions. It would be interesting to
study the lightest operators in these irreps and to compute their anomalous dimensions.
We will not attempt this here. In the following we will focus on the lightest operators in
the scalar, spin 2 and box representations.
Luckily we already know a lot about these operators because they are related to
operators in the dimensionally-reduced theory. Indeed, given a superfield O with highest
component Oθθ̄ , the following relation holds
∆Oθθ̄ = ∆O + 2 = ∆Ô + 2 ,

(3.4)

where ∆Ô is the dimension of the operator Ô in the dˆ ≡ d − 2 dimensional theory to which
O gets mapped under dimensional reduction. Therefore the susy-writable leader Oθθ̄ is
relevant in d dimensions exactly when the operator Ô is relevant in the dimensionally
reduced theory.
8

They must be Sp(2) singlets by definition of susy-writable operators. They must be SO(d) scalars
since the relative Sn -singlets perturbations are also scalars (non-scalar perturbations would explicitly break
rotation symmetry).
9
Here (a, b, · · · ) denotes the Young Tableaux that represents mixed symmetry OSp(d|2) tensors [8] with
a boxes in the first row, b boxes in the second row, etc.

– 14 –

JHEP08(2022)290

On the other hand susy-writable leaders do not have to be invariant under OSp(d|2)
super-rotations, they are only required to be singlets of SO(d) × Sp(2) ⊂ OSp(d|2),8 as
it is the case e.g. for the operators σ12 and σ2(µ)(µ) in (2.13). Since superrotations are
not preserved, along the RG flow we may also find superfields which transform in nontrivial representations Oa1 ...aℓ of OSp(d|2), where we use the notation of [8] and define
latin OSp(d|2) tensor indices as ai = 1, . . . , d, θ, θ̄. Indeed we can be obtain singlets of
SO(d) × Sp(2) by contracting the OSp(d|2) indices of the superfields with the Sp(2)-metric,
Sp(2)
e.g. Oab gab
= −Oθθ̄ + Oθ̄θ . This procedure gives rise to operators with indices set
to the θ and θ̄ directions. However one should notice that the Sp(2)-metric cannot be
contracted to graded-antisymmetric directions otherwise the result vanishes. Also operators
O with more that 2 graded-symmetric indices vanish when contracted to the Sp(2) metric
because Oθθa3 ...aℓ = 0. In practice this means that we should only consider irreducible
representations of the kind (2, 0, . . . ), (2, 2, 0, . . . ), (2, 2, 2, 0 . . . ), etc.9
The final result is that only superfield components of the following form do contribute
under the RG (recall that lower θθ̄ refer to the superfield component in θ, θ̄ expansion,
while upper θθ̄ refer to OSp(d|2) indices)

## PDF page 17

Scalars. Let us first consider the case of scalars. For the φ̂3 fixed point it is known that
there is only one operator which is relevant in dˆ dimensions, which corresponds to the
mass term φ̂2 . So we must have only one susy-writable leader operator that is relevant,
which corresponds to [Φ2 ]θθ̄ . This is indeed equal to the term σ2 which was considered
in the previous section (see equation (2.13)) and that must be tuned to reach the fixed
point. All other scalar operators are irrelevant in dˆ dimensions, thus there cannot exist
other relevant susy-writable scalar leaders (remarkably we are able to make this statement
without any computation).

has higher dimension. We thus conclude that in d = 8 the leader Tθθθ̄θ̄ is marginal and that
any other spin two susy-writable leader is irrelevant. One may be worried that in lower
dimensions (namely φ̂3 theory in dˆ < 6) one would get new relevant operators. However,
since the stress tensor is always marginal, this would imply that the new operators would
have to cross it. Since level crossing is unlikely in an interacting non-integrable model, we
conclude that all spin two operators should stay irrelevant even at dˆ < 6.10 Thus the only
spin two operator that we should consider is the component Tθθθ̄θ̄ of the super stress tensor
itself which corresponds to the following susy-writable leader at d = 8 (see appendix C of [8])
2
1
2
Tθθθ̄θ̄ −→ − ∂ϕ∂ω − (∂χi )2 + 2Hω 2 = − σ2(µ)(µ) + 2Hσ12
ψ→χ
3
3
3
(

)

.

(3.5)

L

One could ask what happens when we add this perturbation to the action. On one hand
since Tθθθ̄θ̄ is always marginal one may imagine that the IR fixed point is a one-dimensional
conformal manifold. However this intuition is incorrect as we explain in what follows.
Indeed the super stress tensor can be defined as a variation of the action with respect to
a superspace background metric gab . Conversely we can say that a perturbation by Tθθθ̄θ̄
produces a change of gθθ̄ ,
1
gθθ̄ → gθθ̄ + δgθθ̄ ←→ δS = −
2

∫

√

dd x |g|δgθθ̄ Tθθθ̄θ̄ .

(3.6)

Notice that the metric of (2.23) is defined such that gθθ̄ = H/2, so the perturbation Tθθθ̄θ̄
actually modifies only the value of H. This is also visible from the explicit form of the
operator (3.5), which when added to the quadratic Lagrangian (2.7) has the net effect of
changing the relative coefficient of the kinetic term, namely H. As we explained below
equation (2.26), changes of H do not have physical consequences on the theory. Therefore
Tθθθ̄θ̄ should be considered as a “redundant” perturbation (see [26]) and should be discarded.
Box. Finally we consider the box representation. In φ̂3 theory we can write an infinite
tower of box operators as follows (see appendix C for a detailed discussion),
(
(k)
B̂µν,ρσ
≡ φ̂k−3

φ̂,µν φ̂,ρσ φ̂ −

10

2dˆ
dˆ − 2

)Y

φ̂,µ φ̂,ν φ̂,ρσ

,

(3.7)

For unitary theories one could use the unitarity bounds to argue that all spin-two operators above the
stress tensor are irrelevant. We avoided this argument since the φ̂3 fixed point is known to be non-unitary.

– 15 –

JHEP08(2022)290

Spin two. We can now focus on spin two operators. In dˆ = 6 the lowest spin 2 operator is
the conserved stress tensor T̂ which has dimension ∆T̂ = dˆ = 6. Any other spin 2 operator

## PDF page 18

where B̂ (k) is the lowest dimensional operators in a box representation built out of k ≥ 3
fields φ̂. Here Y denotes the box Young symmetrization and subtraction of traces and the
notation A,µ1 µ2 ... stands for ∂µ1 ∂µ2 . . . A. There is no argument that fixes the dimensions
of B̂ (k) nor were they previously computed, so we have to obtain them in dˆ = 6 − ϵ by
explicit computation. This is done in appendix D.3.4. Using (3.4) we thus conclude that
(k)
the highest components Bθθ̄ (see appendix C for their explicit definition in terms of the
SUSY fields) of the lightest box operators B (k) have the following IR scaling dimension:
(

)

( (
1

6

) )

( )

2k 2 − 5k − 2 ϵ

+ O ϵ2 ,

(3.8)

1-loop

This ends our classification of the low-lying spectrum of susy-writable leaders. To summarize,
we explained that after the χ → ψ map they can be classified in terms of their OSp(d|2)
representations. We argued that for our problem the most important ones are the scalar,
spin two and box representations. We explained how to obtain anomalous dimensions of
susy-writable leaders using the knowledge of the dimensionally reduced theory. Without
any computation we concluded that scalar and spin two leaders cannot be responsible for
the destabilization of the SUSY fixed point. Finally we computed the dimension (3.8) of the
first susy-writable leader in the box representation. This is the susy-writable leader which
we should worry the most about becoming relevant in d < 8. In section 4 we will comment
on if this perturbation can actually be responsible for destabilizing the SUSY fixed point.
3.2

Susy-null leaders

A susy-null operator —like a susy-writable operator— is a composite operator built of
ϕ, ω, χi -s that is invariant under O(n−2) and thus can be rewritten using the map χ → ψ, ψ̄.
The novelty is that after this map the resulting operator vanishes. E.g. (χ2i )2 maps to
(ψ ψ̄)2 = 0. Since they vanish in the SUSY theory these operators have very restrictive
mixing properties. Indeed susy-null perturbations cannot affect susy-writable observables.
In appendix B we list the susy-null leader operators with low classical dimensions in
8d. We find that there exists an infinite class of Sn singlets which plays an important role
2
Nk =
k−3

(

σ2 σk−2 2σ1 σk−1
−
k−2
k−1

)

,

(3.9)

for k = 4, 5, . . . , ∞. Indeed the leaders associated to Nk take the following simple form
(

(Nk )L = ϕk−4 χ2i

)2

(3.10)

,

which makes them the lowest dimensional null operators made of k fields. Because of this
property they cannot mix with any other operator in perturbative computations. We can
then quite easily compute their one-loop dimensions, which in d = 8 − ϵ are given by (see
appendix D.3.2)
k
∆Nk = 2 (k + 2) − ϵ
+
2 class
(

)

(

)
( )
1 ( 2
6k − 7k − 48 ϵ
+ O ϵ2 .
18
1-loop
)

– 16 –

(3.11)

JHEP08(2022)290

k
∆B(k) = 2k + 6 − ϵ
+
2 class
θ θ̄

## PDF page 19

3.3

Non-susy-writable leaders

Finally we discuss non-susy-writable operators. In Cardy variables they are only singlets
under Sn−1 which permutes the n − 1 fields χi , and not of O(n − 2). So they cannot be
∑
mapped to ψ, ψ̄ variables, and hence break SUSY explicitly. E.g. an operator ni=2 χ3i
cannot be mapped to SUSY variables.
If a leader that is non-susy-writable becomes relevant it would clearly destabilize
the SUSY fixed point. In the RG flow non-susy-writable leaders mix with the other two
types mentioned above, although (as expected from the SUSY theory) the opposite mixing
cannot occur.
The non-susy-writable leader with the lowest classical dimension comes from a class of
Sn singlets which we call Feldman operators (see appendix B and also appendix D of [1]).
They are defined as follows [1, 27]:
Fk =

n
∑

(φi − φj ) =
k

i,j=1

k−1
∑

( )

(−1)

l=1

l

k
σl σk−l ,
l

(3.12)

and their leaders take the form
(Fk )L =

k−2
∑

( )

(−1)l

l=2

(
)
k
(χli ) χk−l
.
j
l

(3.13)

We will consider k to be an even integer greater or equal to 6. For all odd k the operator
vanishes. Similarly, for k = 2, Fk=2 → 0 as n → 0. When k = 4 the operator F4 just
11

Indeed the main role is played by N4 which is the lowest dimensional leader in the susy-null class.
However we will further consider N5 to perform a sanity check. It can be interesting to consider other
low lying susy-null leaders like ω(χ2i )2 (which have the same classical dimensions of N5 ) to get further
sanity checks.
12
For completeness we show the one-loop anomalous dimensions of (Nk )L in the RFIM case (which we
obtained using the techniques of appendix H of [1]),
∆RFIM
(Nk )L =

(

k
k+4− ϵ
2

)

(
+
class

(k − 4)(k + 3)
ϵ
6

– 17 –

)

+ O(ϵ2 ) .
1-loop

JHEP08(2022)290

We notice that all operators Nk for any k ≥ 4 have positive anomalous dimensions. In the
next section we show the consequences of this fact on the stability of the fixed point.
Other susy-null leaders (such as ω(χ2i )2 ) are obtained in locality constraints B. However
for our argument it is sufficient to consider the anomalous dimensions (3.11). Nevertheless,
for completeness, it would be nice to also compute their anomalous dimensions. 11 We leave
this task for future investigations.
As a last comment we stress that the operator (N4 )L ≡ (χ2i )2 has a positive one-loop
anomalous dimension. This is in contrast with the RFIM case of [1] where the one-loop
correction of the same operator vanishes (notice that the operator N4 was called F4 in [1]).
In that circumstance we thus needed to consider the two-loop correction which was negative
and played an important role in determining the stability of the RFIM fixed point. 12

## PDF page 20

reduces to N4 which has a susy-null leader and it was already considered in the previous
section.13 The operator F6 has a non-susy-writable leader
(

)

(F6 )L = −10 2χ3i χ3j − 3χ2i χ4j ,

(3.14)

with classical dimension 18 − 3ϵ in d = 8 − ϵ. It is the lowest of its type, and hence we want
to compute its RG correction. Below is the result of IR anomalous dimensions of all (Fk )L :
(

∆(Fk )L = 3k −

kϵ
2

)

+

(

class

( )
1
k(2k − 3)ϵ
+ O ϵ2 .
18
1-loop
)

(3.15)

Gk ≡

σ3 σk−3
σ1 σk−1 (k − 4)σ2 σk−2
+
−
,
3(k − 5)
k−1
(k − 5)(k − 2)

(3.16)

for k = 6, 7, . . . . The leaders of Gk can be written in a very compact way as a composite of
the leader of F6 and powers of ϕ,
(Gk )L ∝ ϕk−6 (F6 )L .

(3.17)

This implies that their classical dimension is 2(k +3)− k2 ϵ in d = 8−ϵ. Since they are written
as a product of the lowest dimensional non-susy-writable leader (F6 )L times powers of the
lowest dimensional field ϕ, the operators (Gk )L are the lowest dimensional non-susy-writable
operators made of k fields. Because of this property in perturbation theory they do not mix
with other operators and it is easy to compute their anomalous dimensions. The result is
k
∆(Gk )L = 2(k + 3) − ϵ
+
2 class
(

)

(

( )
1
(k(6k − 7) − 120)ϵ
+ O ϵ2 .
18
1-loop
)

(3.18)

Once again we notice that the one-loop correction is always positive.15
13

In this paper we avoid the name F4 and we shall use N4 in order to keep the distinction between the
family Fk≥6 with non-susy-writable leaders and the family Nk≥4 with susy-null leaders. However the name
F4 was used in [1].
14
For convenience we quote the result below:
∆RFIM
(Fk )L =
15

(

k
2k − ϵ
2

)

(
+
class

k(3k − 4) 2
−
ϵ
108

)

+ O ϵ3 .

( )

2-loops

A similar computation for the RFIM gives
∆RFIM
(Gk )L =

(
k+6−

k
ϵ
2

)

(
+
cl.

(k − 6)(k + 5)
ϵ
6

where the anomalous dimensions for k > 6 are always positive.

– 18 –

)

+ O ϵ2 ,

( )

1-loop

JHEP08(2022)290

We show the computation in appendix D.3.3. We see that the one-loop correction is strictly
positive. On the contrary, for the RFIM case, the first non vanishing correction comes at
two loops and it is negative [1].14 This difference is very important for the stability of the
respective SUSY fixed point as we will explain in the next section.
Of course there are infinitely many more non-susy-writable leaders. Let us discuss
another infinite family which is interesting because it contains some of the lowest dimensional
operators of this type. The family can be defined by the following combination of Sn singlets

## PDF page 21

For our argument we will mostly focus on the lowest dimensional non-susy-writable
leader (F6 )L , however it will be useful to know the dimensions of the other leaders of the
families (Fk )L and (Gk )L as a sanity check. In particular we found it useful to introduce
the family (Gk )L since (G7 )L in d = 8 has dimension equal to 20 and thus lies well below
(F8 )L which has dimension 24.

4

Stability of the SUSY fixed points

– 19 –

JHEP08(2022)290

In the previous section we computed the one-loop scaling dimensions ∆ of the low-lying
operators of the LL theory in d = 8 − ϵ. It is now time to take our conclusions on the
stability of the SUSY fixed point when ϵ is of order one. The strategy is simple and it
amounts to checking if any scaling dimension ∆, as a function of d, can cross the marginality
line ∆ = d at some dimension d < 8.
One may be worried that we considered only some low lying operators, and that there
exist still an infinite number of operators which we did not take into account and which
may possibly cross the marginality line. If one has to check the whole spectrum of the
theory, the problem would be intractable and our strategy would not have any hope to
work. However it is possible to argue that there is no need to check the higher dimensional
operators because level crossing is unlikely to occur in non-integrable theories.
Let us explain this point in more detail. Operator mixing occurs in perturbation theory
between operators of the same symmetry, which also satisfy extra selection rules like having
the same dimension and being composite of the same number of fields. In a non-perturbative
setup these extra selection rules are lost and any two operators with the same symmetry
can mix. Let us consider two operators with the same symmetry and dimensions ∆1 (d) and
∆2 (d) computed from perturbation theory. Let us assume that at certain dimension d = d˜
we have a crossing ∆1 ( ˜
d) = ∆2 ( ˜
d). At this point we should not fully trust the functions
∆i (d) since nonperturbative mixing effect can modify the dimensions. The modification is
computed by diagonalizing the mixing matrix of the inner products between the associated
˜
states. The corrected ∆i (d) can either repel or become complex conjugate close to d = d,
depending on operators having norms of same sign or opposite signs respectively (see also
section 10 of [1]). One point of view about crossing is that when this happens one should
not trust anymore the perturbative computation. However for our problem this point of
view seems too pessimistic.
Indeed it is important to take into account that in the context of ϵ-expansion the
computations ∆i (d) (when ϵ is of order one) tend to be much more reliable for operators
with low classical dimension. In other words, by computing higher orders in perturbation
theory, the dimensions of the low lying spectrum do not dramatically change, while the
higher dimensional operators may have very important corrections. For this reason, when
level crossing occurs in ϵ-expansion between operators with low and high classical dimensions,
the most likely scenario is that the crossing is non-perturbatively resolved by repulsion of
the higher dimensional operator. The operators with lowest classical dimensions, roughly
speaking, provide a barrier which is unlikely to be crossed by the higher dimensional ones.
With this in mind we can conclude that in ϵ-expansion by knowing the low lying spectrum

## PDF page 22

Type

IR dimension: ∆O

(N4 )L

Susy-null

2
12 − 2ϵ + 10ϵ
9 + O(ϵ )

(N5 )L

Susy-null

67ϵ
2
14 − 5ϵ
2 + 18 + O(ϵ )

Bθθ̄

(3)

Susy-writable (box)

2
12 − 4ϵ
3 + O(ϵ )

Bθθ̄

(4)

Susy-writable (box)

14 − 3ϵ + O(ϵ2 )

(F6 )L

Non-susy-writable

18 + O(ϵ2 )

(G7 )L

Non-susy-writable

2
20 + 31ϵ
9 + O(ϵ )

Table 1. Summary of the computation of anomalous dimensions of the first leader operators of
each type. The computations are performed in the LL theory for the RF φ3 model in d = 8 − ϵ.

of operators in all symmetry sectors, we can answer with reasonable confidence the question
of stability of the fixed point.
In our case the mixing may occur if two operators have leaders in the same class between:
non-susy-writable, susy-null and susy-writable of a given OSp(d|2) representation. By the
argument above it should be enough to study the operator with lowest classical dimension
for each sector. However, to be extra cautious, we further considered (at least) one operator
above it. By checking if the operators above cross the ones below we thus have a measure
of whether non-perturbative mixing effect may be important and slightly affect the result
(namely if there is no crossing we should be more confident about our computation).
We are now ready to analyze the result of section 3. We found that the lowest
dimensional susy-null leader is (N4 )L = (χ2i )2 . This operator belongs to the infinite family
of susy-null leaders (Nk )L with dimensions computed in formula (3.11) for generic k. For
susy-writable leaders we argued that the operators in the box representation of OSp(d|2)
(3)
have a better chance to play a role. The lowest dimensional one is Bθθ̄ and belongs to the
(k)

infinite family of operators Bθθ̄ (k ≥ 3) with dimensions that increase with k as computed
in (3.8). In the non-susy-writable sector the lowest dimensional operator is (F6 )L which
comes from the infinite family (Fk )L for k = 6, 8, 10, . . . . Their dimensions are given in
equation (3.15). We also considered another infinite family of non-susy-writable leaders
(Gk )L which contain the operator (Gk=7 )L that lies right above (F6 )L . Their dimensions are
given in equation (3.18).
In table 1 we summarize the anomalous dimensions of the lowest dimensional operators
(3)
(N4 )L , Bθθ̄ , (F6 )L of each type and we compare them with the dimensions of one operator
above. From the table it is easy to see that the lowest operators are never crossed by the
operators above. Moreover one can also check that they are never crossed by any higher
dimensional operator of the same type. We thus conclude that non-perturbative mixing
should not affect our analysis.
In what follows we can then focus on each of the lowest operators of the three categories.
We have plotted their IR dimensions as a function of the spacetime dimension d in figure 2.

– 20 –

JHEP08(2022)290

Leaders O

## PDF page 23



















Figure 2. Plot showing dimensions of the lowest dangerous leaders from the three categories vs
spacetime dimension d.

Comparing with the marginality line ∆ = d we see that none of the operators becomes
relevant. Since we do not find any new relevant perturbation we can conclude that the
SUSY fixed point persists even at 8 − d = O(1) and thus that the RF φ3 model always
undergoes dimensional reduction.
Of course our conclusion has to be taken with a grain of salt. Besides the nonperturbative mixing (which should not significantly change our results), there is a more
important source of uncertainty. Indeed our conclusion relies on a one-loop computation of
the anomalous dimensions. Since we are extrapolating to ϵ ∼ O(1), higher loop corrections
may become important. It would be very interesting to compute them and see if our results
are confirmed.16 We leave this task for the future.
One of our main motivations for this work was to check if the RG setup introduced
in [1] to study the RFIM model would give consistent results also for RF φ3 . Recall the
discussion from section 1 that the RF φ3 model describes the near critical behavior of
branched polymers. As first established in [17] according to numerical evidence, the critical
point of branched polymers is related to the non-disordered Lee-Yang fixed point (which
describes critical point of Ising model in an imaginary magnetic field) via dimensional
reduction in all 2 ≤ d < 8. Consequently it is expected that the critical RF φ3 model in this
range of dimensions is always described by a supersymmetric fixed point. Our conclusion
above is therefore consistent with this expectation (see the next section for a discussion on
the subtle d = 2 case).
Another motivation was to compare how the single RG setup works in different ways
for RFIM and RF φ3 (see figure 3). Indeed in [1] we found that for the RFIM the SUSY
fixed point becomes unstable at a critical dimension dc ≈ 4.2–4.7 (namely for d ≤ dc the
fixed point is non supersymmetric). On the other hand we expected no instability for the
16

We checked that a Padé[1,1] approximation does not change our observation that none of the considered
operators crosses marginality. However it would be nice include higher loop computations in the analysis.

– 21 –

JHEP08(2022)290



## PDF page 24

Lfree 3

4

<latexit sha1_base64="uaEyuG4lOCDlJXEZ5/R7E2ml+ks=">AAACAnicbZDLSsNAFIYnXmu9RV2Jm2ARXJVEBF0W3bhwUcFeoIllMj1ph04uzJyIJQQ3voobF4q49Snc+TZO2i609YeBj/+cw5zz+4ngCm3721hYXFpeWS2tldc3Nre2zZ3dpopTyaDBYhHLtk8VCB5BAzkKaCcSaOgLaPnDy6LeugepeBzd4igBL6T9iAecUdRW19x3Q4oDRkV2nd9lLsIDZoEEyPOuWbGr9ljWPDhTqJCp6l3zy+3FLA0hQiaoUh3HTtDLqETOBORlN1WQUDakfehojGgIysvGJ+TWkXZ6VhBL/SK0xu7viYyGSo1CX3cWC6vZWmH+V+ukGJx7GY+SFCFik4+CVFgYW0UeVo9LYChGGiiTXO9qsQGVlKFOraxDcGZPnofmSdXRfHNaqV1M4yiRA3JIjolDzkiNXJE6aRBGHskzeSVvxpPxYrwbH5PWBWM6s0f+yPj8AZf5mDA=</latexit>

dc 5

S
SU
SUS

6

Y

d

Lfree 3
<latexit sha1_base64="uaEyuG4lOCDlJXEZ5/R7E2ml+ks=">AAACAnicbZDLSsNAFIYnXmu9RV2Jm2ARXJVEBF0W3bhwUcFeoIllMj1ph04uzJyIJQQ3voobF4q49Snc+TZO2i609YeBj/+cw5zz+4ngCm3721hYXFpeWS2tldc3Nre2zZ3dpopTyaDBYhHLtk8VCB5BAzkKaCcSaOgLaPnDy6LeugepeBzd4igBL6T9iAecUdRW19x3Q4oDRkV2nd9lLsIDZoEEyPOuWbGr9ljWPDhTqJCp6l3zy+3FLA0hQiaoUh3HTtDLqETOBORlN1WQUDakfehojGgIysvGJ+TWkXZ6VhBL/SK0xu7viYyGSo1CX3cWC6vZWmH+V+ukGJx7GY+SFCFik4+CVFgYW0UeVo9LYChGGiiTXO9qsQGVlKFOraxDcGZPnofmSdXRfHNaqV1M4yiRA3JIjolDzkiNXJE6aRBGHskzeSVvxpPxYrwbH5PWBWM6s0f+yPj8AZf5mDA=</latexit>

4

5

6

S
SU

Y

7

8

d

Y
(b) RF φ3 .

(a) RFIM.

RF φ3 . It was interesting for us to see how this would come about. This paper provides an
answer to this puzzle. The main source of instability for the RFIM is due to (N4 )L (which
we called (F4 )L in [1]) and (F6 )L . They are found to have vanishing one-loop anomalous
dimension. The first non-vanishing contribution is found at two-loops and it is negative
(see footnote 14). So the main difference is that in the RFIM their one-loop correction
vanishes, leaving a leading two-loop negative correction. For the RF φ3 we did not compute
the two-loop correction of (N4 )L and (F4 )L because their one-loop anomalous dimension is
already positive and fairly large.17 One can easily understand why the one-loop corrections
behave differently in the two models. Indeed these are computed in a different way: one
needs to insert two interaction vertices to compute a one-loop correction in the RF φ3
while a single vertex is required in the RFIM (this is also true for the pure versions of
the models and it is simply due to the fact that the vertices have odd or even number of
fields). Operators made of only χi fields (like the Feldman operators) clearly do not receive
corrections from the insertion of a single vertex since the latter always contains other fields
(e.g. the vertex ϕk χ2i has extra powers of ϕk which cannot be contracted with the fields χi of
the Feldman operator). Therefore by construction in the RFIM all Feldman operators have
zero anomalous dimension at one loop, while for the RF φ3 this need not be the case and
indeed we find that it is not. We thus conclude that by applying the single RG framework
of [1] we obtain the expected results in two different models. This gives us more confidence
that the framework of [1] is indeed correct.

5

Discussion

In this paper we carry out a perturbative RG analysis of the Random Field φ3 model. We
use the framework introduced to study the Random Field Ising Model in [1].
The results of [1] are compatible with the numerical observations [5–7] that supersymmetry (and thus dimensional reduction) of the RFIM fixed point are lost in d = 3, 4
and are recovered in d = 5, where d = 6 is the upper critical dimension. In [1] this is
17

Still it would be interesting to compute the two-loop correction.

– 22 –

JHEP08(2022)290

Figure 3. RG flow of the leader theory in the RFIM (figure 3a) vs RF φ3 theory (figure 3b). In
RFIM we have an unstable SUSY fixed point below dc ≈ 4.2–4.7. For RF φ3 the SUSY fixed point
is stable.

## PDF page 25

1. Higher loops and other operators: all the anomalous dimensions computed in this
paper are at one loop. It would be interesting to compute higher loop corrections
of the low lying leader operators. This would allow one to verify that SUSY fixed
point is indeed stable for larger values of ϵ. Susy-null and non-susy-writable leaders
like (N0 )L and (F6 )L need to be studied in the LL theory. This is slightly more
complicated than the usual φ̂3 theory (Lee-Yang) fixed point in dˆ = 6 − ϵ, since the LL
Lagrangian contains two interaction vertices and three different propagators. However
using modern multi-loops technologies it should be fairly easy to extend the results
of this work to higher orders in perturbation theory. For the susy-writable leaders
18

E.g. the model proposed in [18] is not sensitive to susy-null and non-susy-writable perturbations which
were crucial to understand the destabilization of the SUSY fixed point in the RFIM.

– 23 –

JHEP08(2022)290

explained by the fact that (at least) one operator becomes relevant in dimensions d < dc
where dc ≈ 4.2–4.7. For the RF φ3 model the numerical expectation [17] is that the SUSY
fixed point is always reached in 2 ≤ d < 8 (where d = 8 is the upper critical dimension,
while the subtle d = 2 case is discussed below). The main result of this work is a check that
the framework introduced in [1] is compatible with the numerical results. Indeed we studied
a large number of low lying perturbations and we found that at one-loop they all have
positive anomalous dimensions and they do not seem to ever cross the marginality line.
This result is important for two main reasons. Firstly it is a check of the RG framework
of [1]. Indeed we gained more confidence that this framework is correct since gives results
compatible with the RF φ3 expectations. Notice that it is crucial to test this framework
since it provides a new understanding of when and why the RFIM undergoes dimensional
reduction, which is a question which was debated for almost fifty years. Secondly it explains
in the same language used for the RFIM why dimensional reduction is not lost for the RF
φ3 itself. The latter is also an important question. Indeed the RF φ3 theory captures the
phase transition of a number of interesting statistical physics models like branched polymers
and lattice animals. For these models dimensional reduction was observed to hold giving
rise to the Lee-Yang universality class in d − 2 dimensions. Our calculations are in perfect
agreement with these results.
Interestingly, for the problem of branched polymers Brydges and Imbrie proposed a
model that has explicit Parisi-Sourlas supersymmetry at the microscopic level and which,
by construction, undergoes dimensional reduction [18]. On one hand the result of Brydges
and Imbrie is impressive because it explicitly shows how dimensional reduction works
in the problem of branched polymers without even using field theory or RG. On the
other hand [18] only shows dimensional reduction for a very fine tuned model where
supersymmetry is taken as a starting point. In particular in [18] it is missing an explanation
of why supersymmetry should emerge in the IR for a generic non-supersymmetric model of
branched polymers.18 Our work provides an answer to this question by showing that all
SUSY-breaking deformations are indeed irrelevant.
There are many open problems which deserve further investigation (see also the
discussion section of [1]) and our work should be viewed as a first step in this direction.
Some of the most interesting ones are listed below.

## PDF page 26

like the box operators the computation can be directly done in the usual φ̂3 theory
(because of dimensional reduction), by computing higher loop anomalous dimensions
of the B̂ operators.

2. Conformal Bootstrap: it would be interesting to set up a conformal bootstrap problem
for the RF φ3 fixed point.19 This would be a strong check of the stability of the SUSY
fixed point and dimensional reduction. Choosing a 4-point function appropriately one
can shed light on the various operators allowed in the theory in the nonperturbative
regime 8 − d = O(1). E.g. non-susy-writable operators like (Fk )L can be exchanged
in the conformal block decomposition of ⟨χi (x1 )χj (x2 )χk (x3 )χl (x4 )⟩, so we could
numerically estimate their dimensions by bootstrapping this correlator.
There are a number of challenges in setting up this bootstrap problem. Firstly, we do
not have a CFT for positive integer values n which we can analytically continue to
n → 0. This is because the fixed point only exists at n = 0 (the fixed point arises as
the limit n → 0 of a sequence of approximate fixed points as we review in section 2.1).
Second, since we are working in an Sn invariant theory with n → 0 we expect to find
a logarithmic CFT [29]. Indeed for the RFIM case we find logarithmic multiplets (see
section 9.2 and appendix H of [1]), and one should expect the same for the RF φ3
model. In order to account for logarithmic multiplets one needs to use a different
bootstrap algorithm which makes use of logarithmic conformal blocks [30]. Finally
the CFT is nonunitary as evident e.g. from the dimension of ϕ. So one cannot impose
unitarity bounds or positivity of OPE coefficients. For nonunitary CFTs one needs to
resort to Gliozzi’s bootstrap algorithm [31] or to variations thereof, which typically
are less systematic. Some work is required to tackle these problems, but certainly it
would be priceless to have at our disposal the bootstrap toolbox to study random
field theories.
3. Dimensional reduction 2 → 0: the RF φ3 model can also be studied in d = 2. In
this case, according to dimensional reduction, one would obtain a relation to the
pure φ̂3 theory in zero dimensions. This case is of course bound to be singular. E.g.
dimensional reduction for correlation functions is obtained by localizing all operators
to a d − 2 dimensional hyperplane, however this prescription is not well defined for
d = 2, since all insertions would collapse to a single point. On the other hand one can
compute the partition function (and related observables) in the RF φ3 model for d = 2
and relate them to the zero-dimensional φ̂3 counterpart, where the zero dimensional
path integral is just understood as an ordinary integral. Parisi and Sourlas in [17]
19

See [28] for an attempt by Hikami, reviewed in appendixA.10 of [1].

– 24 –

JHEP08(2022)290

We also ignored other perturbations with higher classical dimensions, e.g. susy-null
leaders not in the class (Nk )L and non-susy-writable leaders that are not of the form
(F6,k )L or of the Feldman type. It would be interesting to compute their anomalous
dimensions. This may be useful in order to understand nonperturbative mixing when
ϵ is large. It should be kept in mind that for operators with higher classical dimensions
good accuracy is expected only at higher loops.

## PDF page 27

checked that critical exponents behave according to dimensional reduction even at
d = 2. The problem was later reconsidered in [32], where it was suggested that the
d = 2 theory does not have the structure of a conformal theory. Indeed for d = 2 the
Parisi-Sourlas supersymmetric theory is of a subtle type since it is not clear if it can
possess a traceless super-stress tensor. This problem can be explicitly seen in free
theory by looking at formula (C.4) of [8] where the improvement term which makes
the stress tensor traceless is singular for d = 2. We think that it would be worth to
revisit this problem in a modern language to get a more comprehensive understanding
of this two-dimensional theory and of its dimensional reduction.

5. Dimensional reduction 4 → 2: finally we would like to mention that the dimensional
reduction 4 → 2 is not singular but it is very interesting. Indeed the dimensionally
reduced models have emergent Virasoro symmetry (e.g. the RF φ3 theory in d = 4
dimensionally reduces to the Yang-Lee minimal model with central charge c = −22/5).
It would be very interesting to investigate how the Virasoro symmetry is embedded in
the d = 4 supersymmetric theories. This direction deserves further investigation [33].
6. Applications to other models: beside RFIM and RF φ3 theory, there are other models
which could be potentially studied in the RG framework used in this paper. Indeed
in statistical physics one often uses the replica method and sometimes one lands on
Lagrangians of the form (2.3) or generalizations thereof (see e.g. [34] for a model of
the continuous phase transition of glassy materials). It would be interesting to further
apply the RG framework of [1] to these cases both as a test of the method and to see
whether it provides a deeper understanding of a broader class of phenomena.

Acknowledgments
We would like to thank the participants of the workshop “Bootstat 2021” which took place at
Institut Pascal (Université Paris-Saclay) with the support of the program “Investissements
d’avenir” ANR-11-IDEX-0003-01. We especially thank Silvio Franz for interesting discussions
and Slava Rychkov for comments on the draft and collaboration in the early stages of the
project. The work of A.K. is funded by the German Research Foundation DFG under
Germany’s Excellence Strategy — EXC 2121 “Quantum Universe” — 390833306. The work
of E.T. is supported by the European Research Council (ERC) under the European Union’s
Horizon 2020 research and innovation programme (grant agreement No 852386).

– 25 –

JHEP08(2022)290

4. Dimensional reduction 3 → 1: a less singular case arises for the dimensional reduction
3 → 1. Here one can still consider correlation functions restricted to a line. On the
other hand, again we cannot define a stress tensor in dˆ = 1 since all one-dimensional
theories are non-local. This can be again seen in Parisi-Sourlas supersymmetric free
theory where one finds that the dimensionally reduced stress tensor —see e.g. in (C.6)
of [8]— vanishes. It would be interesting to study in more detail the three-dimensional
SUSY theories and their dimensional reduction.

## PDF page 28

(b) Lattice animal.

Figure 4. Different clusters on the lattice.

A

Review of branched polymers and lattice animals

In this appendix we review how to define the problem of diluted branched polymers/lattice
animals and see why it is captured by the RF φ3 theory. We will follow the construction
of [16] and we aim at giving a pedagogical and explicit definition of all the ingredients of
the model (see also chapter 9 of [35]).
Let us start with some basic definitions. A polymer is defined as a linear chain of units
called monomers. A branched polymer is built by sewing together linear polymers. It is
convenient to define the polymers on a lattice so that for any fixed number of monomers,
there is a finite number of configurations. We define a polymer on a d dimensional hypercubic
lattice by placing the monomers at the sites of the lattice and by connecting neighbouring
sites with lines. Sets of connected sites on the lattice are called “lattice animals” or “clusters”.
When lattice animals have a tree-like topology they define branched polymers. General
lattice animals also contain self intersections (i.e. closed loops) as shown in figure 4.
We are interested in studying the statistics of branched polymers/lattice animals when
the number N of monomers is very large: in this limit the number of possible configurations
P (N ) and the average size R of a cluster scale as P (N ) ∼ N −θ λN and R ∼ N ν where
θ, ν are critical exponents, while λ is a non-universal constant. The models of branched
polymers and lattice animals are known to be in the same universal class (see discussion
below). In the following we define a model which counts configurations of lattice animals,
which allows us to choose how many links, loops, clusters and vertices are present in a given
configuration. Finally we will be interested in the so called diluted limit, which suppresses
configurations with multiple clusters.
We will introduce the model in steps. We will start by defining a toy-model that is
used to build random walks (which are equivalently understood as linear polymers). We
then introduce vertices to allow for branching. Finally we explain how to modify the model
to count the number of separate clusters. We conclude the appendix by showing that the
IR behaviour of this model can be described in the continuum limit by an action with Sn
symmetry which is of the same form as the replica action of (2.3).

– 26 –

JHEP08(2022)290

(a) Branched polymer.

## PDF page 29

To start we consider a simple O(m) model with an m-state vector si with partition function
(
)
Z = tr

1+K

∏
⟨xx′ ⟩

m
∑

si (x)si (x′ )

(A.1)

.

i=1

where ⟨x, x′ ⟩ denotes nearest neighbour sites. We want to consider si to be variables in R
which are spatially uncorrelated with trace defined as
tr =

∫ +∞ ∏ ( ∏
m
−∞

x

)

dsi (x) P

(m
∑

i=1

)

s2i (x)

,

(A.2)

i=1

tr si1 (x) · · · sik (x) = Ck (δi1 i2 . . . δik−1 ik + . . . ) ,

(k even)

(A.3)

and zero if k is odd, for some coefficients Ck . The dots in (A.3) represent products of
Kronecker deltas for all possible inequivalent pairings of the indices ik . In order to build
the model we further require the coefficients Ck to satisfy the following conditions
tr 1 = 1 ,

k

Ck = m 2 −1 ck ,

tr si1 (x)si2 (x) = δi1 i2 ,

for k = 4, 6, . . . , 4d ,

(A.4)
where the coefficients ck must be finite in the limit m → 0. Finally we also need to be able
to tune the coefficients ck to the values we want. Later we will explain why these conditions
are useful.
These conditions can be recast as restrictions on the possible distributions P . In
other words it is possible to choose P in such a way that all these conditions are ∑
satisfied.
s2

A simple way to do this is to choose a distribution written as a Gaussian exp(− 2i i )
∑
times a polynomial in i s2i . This distribution gives rise to computable traces (by Wick
contractions) and one can easily check that by tuning the coefficients of the polynomial one
can fix the same number of coefficients Ck .20
∑
∑
′
Formula (A.1) corresponds to a Hamiltonian ⟨xx′ ⟩ log(1 + K m
i=1 si (x)si (x )), which
is a slight modification of the usual O(m) model due to the presence of the logarithm. This
formulation gives a simpler partition function which has at most a single bond between
two sites and thus it can be conveniently described diagrammatically in terms of clusters.
Let us show how this is done. We first expand the product in (A.1) to get a sum of terms
∑
′
′
each of which is just a product of bonds K m
i=1 si (x)si (x ) for a given set of x, x . This
product is then depicted by drawing a line between each two sites if a bond between them
20

To be explicit, given the distribution

∑
P =

∑l

(

e

−

i
2

s2
i

∑

(2π)m/2

)l

(

lmax

al

l=0

)

∑ 2
si

,

i

max l
one finds that Ck =
2 k+m
al , where k are even integers. The linear map between al with
2
l=0
l
l = 0, 1, . . . , lmax and Ck with k = 0, 2, . . . , 2lmax is invertible and we can therefore use it to fix this set of
Ck to any value by opportunely tuning the coefficients al . This means that by considering lmax = 2d it is
possible to satisfy (A.4) and to even choose the values of ck .

– 27 –

JHEP08(2022)290

where P is an O(m) invariant distribution. By O(m) invariance we must have that

## PDF page 30

is present. A cluster is thus a set of connected bonds. Now the important observation is
that by tracing over si the only clusters that survive are closed loops. Indeed for each open
end we get tr si = 0. Moreover for each separate loop we get a factor of m due to the sum
over i. There are also configurations with intersecting loops which arise when more than
two spins are present at the same site. Forgetting about the latter (which we will discuss
below), the partition function can be expressed as
Z=

∑

(A.5)

mN L K N B

C

m
∏
∑
1
⟨s1 (x1 ) s1 (x2 )⟩ = tr s1 (x1 ) s1 (x2 )
1+K
si (x)si (x′ )
Z
i=1
⟨xx′ ⟩

(

)

.

(A.6)

By expanding again the product we notice that presence of s1 makes it possible to draw new
diagrams which are lines that connect x1 to x2 . These configurations are not suppressed
by the m → 0 limit because the operator s1 is selecting a single component of the possible
m. In practice all configurations are written in terms of lines that connect s1 at different
sites (all the other spin components si>1 are not present in any configuration). Conversely,
∑
choosing the two point function of i si would have generated an extra factor of m for the
lines due to the sum over i. Equation (A.6) is used to compute the statistics of self avoiding
walks between two points.
For the problems of branched polymers and lattice animals we want to sew together
many self avoiding walks. A first step to do so is to allow many endpoints, namely we
∏
can multiply the partition function (A.1) by a term x (1 + Hs1 (x)). This is not enough
since as m → 0 it would only generate configurations involving a number Nc of linear self
avoiding walks weighted by H 2Nc . In order to obtain branched configurations we need
to introduce vertices vk (x) which allow us to connect k lines to the site x. These can be
defined by the requirement
lim tr vk (x)si1 (x) · · · sip (x) = δpk δ1i1 ...ik ,

m→0

(A.7)

where δa1 ...ak = 1 if all ai are equal, otherwise it is zero. Since the index k of vk (x) counts
how many lines are attached to a given site, for a hypercubic lattice we need only to build
a finite number of vertices with 3 ≤ k ≤ 2d. Also the k label is restricted by the possible
number of spins si (x) at a given site x in the nearest neighbour interaction (A.1), which
gives 0 ≤ p ≤ 2d. The operators vk (x) are written in terms of the spin variable si (x). We

– 28 –

JHEP08(2022)290

where C is a cluster configuration which only contains loops, NL counts the number of
loops in C and NB the number of bonds. Now we want to take the limit m → 0. This
has two important consequences: first it suppresses loop configurations, secondly because
of (A.3) it suppresses traces of more than two spins at a given vertex, thus eliminating all
configurations with intersecting loops and leaving only linear configurations. E.g. at order
m the limit m → 0 selects only configurations with a unique self avoiding loop. While this
limit trivializes the partition function, it is typically used to study two point functions of a
spin variable s1

## PDF page 31

1
,
6c6 m2

c6 − c24
).
2c6 m2 c4 (m + 2) − c6 (m + 4)
(A.8)
By simple power counting this automatically satisfies (A.7) for all p > k because of the
scaling in m of (A.4).
This example not only shows how to construct the vertices but also it clarifies why we
need to be able to tune the coefficient ck . Indeed we must ask that the denominators of the
equations above are not vanishing, namely c24 (m + 2) − c6 (m + 4) ̸= 0 and c6 ̸= 0.22
In other words, the existence of vertices with the property (A.7) is an extra requirement
which is not trivially satisfied by all distributions P . We can go on by repeating this
construction for vertices vk with higher k. The number of coefficients in the ansatz
for the vertices matches the number of independent tensor structures appearing in the
equations (A.7) for p ≤ k (this is ensured by symmetry) and thus we are able to fix all
the coefficients in terms of the variable ck . We checked this algorithm and found explicit
formulae for the vertices vk for k = 3, . . . 6. We do not report the results here since the
expressions are lengthy.
Using the vertices we can write a new expression for the partition function
a1 =

c4
),
m c4 (m + 2) − c6 (m + 4)
( 2

(

Z = tr

∏
⟨xx′ ⟩

1+K

m
∑

a2 =

a3 =

⎛
)
( ′) ∏
⎝1 + Hs1 (x) +
si (x) si x

i=1

x

( 2

⎞
∑

Wk vk (x)⎠ ,

(A.9)

3≤k≤2d

where the coefficients Wk are introduced to count the number of vertices with k lines in a
configuration. It is important to notice that for a given site we can either have a simple
point, an endpoint or a vertex vk . This means that we never have to consider traces of
two vertices vk1 (x) and vk2 (x) and therefore that (A.7) is enough to compute all possible
configurations. It is also worth mentioning that in this model there cannot be more than
4d spin variables at a given site (this happens when a vertex v2d (x) is attached to 2d lines)
21

We did not include even powers of the spin variable because (A.7) gives rise to an independent set
of linear equations for the correspondent coefficients which is homogeneous and thus has trivial solution,
namely we can set all these coefficient to zero.
22

E.g. these requirements are not satisfied by the distribution P (x) = δ(x − m) which gives ck =

2

1− k
2

( n2 +1) k −1
2

and thus c24 (m + 2) − c6 (m + 4) = 0.

– 29 –

JHEP08(2022)290

ask vk (x) to preserve the O(m − 1) symmetry that rotates the variables si with i = 2, . . . , m.
In practice we can define vk (x) as a polynomial of order k in the spin variables which
∑
2
depends on s1 and m
i=1 si . Let us exemplify this by considering the simplest vertex for
∑
2
21
k = 3. We start by the ansatz v3 (x) = a1 s1 + a2 s31 + a3 s1 m
i=1 si for some coefficients ai .
The coefficients ai of the ansatz are fixed by requiring that (A.7) is satisfied for p = 1, 3.
Notice that from these two requirements we obtain three equations which arise from the
different tensor structures. E.g. from p = 1 we get a single equation that multiplies δ1i1
which we want to set to zero. From p = 3 we get two equations. One from the coefficient of
(δ1i1 δi2 i3 + δ1i2 δi3 i1 + δ1i3 δi1 i2 ) which we want to set to zero and one from the coefficient of
δ1i1 δ1i2 δ1i3 which we want to set to one. In particular using (A.3) and (A.4) we can solve
the full set of equations obtaining

## PDF page 32

which explains why we required the maximal value of k in the conditions (A.4) to take
this value.
Because of the vertices, the partition function now also generates loop configurations
(thus generic lattice animals and not only branched polymers) as long as they are constructed
by connecting vk and endpoints. E.g. the simplest loop configuration is obtained by attaching
an endpoint to one of the lines of a v3 vertex and by making a closed loop with the remaining
two lines — giving a weight HW3 . This term will not scale as m because all the spin
variables in the diagram must be of the form s1 .
A problem of this model is that it does not give us any handle to count the number of
separated clusters. E.g. a diagram weighted by H 3 W3 (see figure 5) could either be a vertex
attached to three open ends or it could be made of two separate clusters, the first being like
the one described above with weight HW3 and the second one being a line that connects
two points with weight H 2 . This is not what we wanted, since we aimed at counting the
number of configurations of a single lattice animal. In the following we explain how to
modify the model in order to count the clusters. This will be crucial to take the dilute limit
in which configurations with multiple clusters are suppressed.
There is a very simple way to count clusters. Indeed, as mentioned above, a linear
∑
cluster obtained by inserting at the open ends the operator i si (instead of s1 ) is weighted
by a factor of m (similarly the weight of m is kept for branched clusters if one uses vertices
that satisfy tr vk (x)si1 (x) · · · sip (x) = δpk δi1 ...ik instead of (A.7)). Here however we do not
want to use m to count the number of clusters, since this variable is already used to count
the number of loops. The idea is thus to introduce a new index j in the spin variable
obtaining sij with i = 1, . . . m and j = 1, . . . n, where the new parameter n will be used to
count clusters. The label j is independent of i but works in a very similar way. The trace is
defined as
tr =

∫ +∞ ∏
−∞

⎛

m ∏
n
∏

⎝
x

⎞

⎛
⎞
m ∑
n
∑
dsij (x)⎠ P ⎝
s2 (x)⎠ ,
ij

i=1 j=1

i=1 j=1

– 30 –

(A.10)

JHEP08(2022)290

Figure 5. Two configurations that scale like H 3 W3 (both made with eleven bonds which thus
give an extra factor of K 11 ). The blue dots represent end points weighted by H, while the red dot
represents a vertex v3 weighted by W3 . The configuration on the left contains a single cluster while
the configuration on the right contains two.

## PDF page 33

where P is an O(m) × O(n) invariant distribution which thus gives
tr si1 j1 (x) · · · sik jk (x) = Dk (δi1 i2 δj1 j2 . . . δik−1 ik δjk−1 jk + . . . ) ,

(k even)

(A.11)

and vanishes when k is odd. The dots contain products of Kronecker deltas for all pairings
of the indices (ik , jk ) —such that every δip iq always appears multiplied by δjp jq with the
same p, q. We require the coefficients Dk to satisfy the conditions
tr 1 = 1 ,

k

Dk = m 2 −1 dk ,

tr si1 j1 (x)si2 j2 (x) = δi1 i2 δj1 j2 ,

⎛

Z = tr

∏

⎝1 + K

⟨xx′ ⟩

m
∑ n
∑

⎞
( ′)

sij (x) sij x ⎠

⎛
∏

⎝1 + H

x

i=1 j=1

n
∑

⎞

s1j (x) +

j=1

∑

Wk wk (x)⎠ ,

3≤k≤2d

(A.13)
where the new vertex wk (x) satisfies
lim tr wk (x)si1 j1 (x) · · · sip jp (x) = δpk δ1i1 ...ik δj1 ...jk ,

m→0

(A.14)

for 0 ≤ p ≤ 2d and 3 ≤ k ≤ 2d. The vertices wk are built as polynomials of order k in the
spin variable sij which preserved Sn × O(m − 1) symmetry and whose terms are assembled
∑
∑
∑n
2
from the building blocks nj=1 sp1j (x) and m
i=1
j=1 sij (x). It is easy to see that the same
ideas used to construct vk can be generalized to define the vertices wk . E.g. a vertex w3
that satisfies (A.14) can be defined as follows
w3 (x) = a1

n
∑

s1j (x) + a2

j=1

n
∑

s31j (x) + a3

j=1

m ∑
n
∑

s2ij (x)

n
∑

s1j ′ (x)

(A.15)

j ′ =1

i=1 j=1

with
1
,
6d6 m2

d6 −d24
).
2d6 m2 d4 (mn+2)−d6 (mn+4)
(A.16)
As before the coefficients dk are tuned to avoid singularities.
By expanding the partition function in the m → 0 limit we obtain
a1 =

d4
),
m d4 (mn+2)−d6 (mn+4)
( 2

Z=

∑

a2 =

K N B H N E nNC

C

a3 =

∏

( 2

NVk

Wk

,

(A.17)

3≤k≤2d

where C is a configuration that contains NB bonds, NE endpoints, NC separated clusters
and NVk vertices with k legs. The presence of all these parameters allows us to count
the number of loops NL in a given configuration, which is obtained through the relation
∑
NL = NC − N2E + k ( k2 − 1)NVk . We thus obtain a partition function of the form
Z=

∑ N N N
B
L
C

ΛB ΛL ΛC

C

∏
3≤k≤2d

– 31 –

NV

ΛV k k ,

(A.18)

JHEP08(2022)290

for k = 4, 6, . . . , 4d ,
(A.12)
where again we want to be able to tune the values of dk which must be finite in the
limit m → 0. As before all these conditions can be met by considering P as a Gaussian
distribution multiplied by a polynomial with opportunely chosen coefficients.
We thus define the partition function

## PDF page 34

where
ΛB = K ,

ΛL = H −2 ,

ΛC = nH 2 ,

ΛVk = Wk H k−2 .

(A.19)

⎛

Z=

∫

m ∏
n
∏∏

⎝

⎞

dsij (x)⎠ e−H[sij ]

(A.20)

x i=1 j=1

where the Hamiltonian takes the form
⎛

H=−

∑

log ⎝1 + K

⟨xx′ ⟩

⎡

−

∑
x

m ∑
n
∑

⎞
( ′)

sij (x) sij x ⎠

i=1 j=1

⎛

⎣log ⎝1 + H

n
∑
j=1

⎞

s1j (x) +

∑

⎛

Wk wk (x)⎠ + log P ⎝

k≥3

(A.21)

⎞⎤
∑

s2ij (x)⎠⎦ .

ij

The model has a continuous symmetry O(m − 1) which rotates the i = 2, . . . m components
of sij . This arises because the original O(m) symmetry is broken by the end points and
vertices which are built in terms of powers of spins in the direction i = 1. The O(m − 1)
symmetry is not going to play any role in the final field theory since the directions i ̸= 1
are not going to be critical. This may not be so counterintuitive since also in the cluster
representation only the spin si=1,j was contributing to the configurations. There is an extra
Sn symmetry which acts by permuting the components j. This arises because the vertices
∑
wk contain powers k of j sk1j with arbitrary k. We thus expect to obtain a model in the
continuum limit which has Sn symmetry in the limit n → 0. In the following we shall
explain how this arises in more detail.
We first consider the nearest neighbour interaction term of (A.21). Each term in the
expansion of the logarithm can be further Taylor expanded for small lattice spacing a between
∑
neighbouring sites. The result is written as a polynomial in s · s ≡ ij sij sij dressed with
derivatives. E.g. let us consider the term k = 1 in the expansion log(1 + y) =

– 32 –

∑∞

k=1

(−1)k k
k y

JHEP08(2022)290

We further want to consider the diluted limit, namely the case in which there are few
clusters. To do so we take the limit n → 0. The resulting partition function generates
lattice animals; in principle one could get branching polymers by forcing the number of
loops to zero by taking ΛL → 0 (or equivalently H → ∞) in (A.18) while keeping the rest
of the Λ’s finite. We avoid this procedure and keep ΛL finite since lattice animals and
branched polymers are known to be in the same universality class. While there is no full
proof of the latter statement, this was checked in various numerical works (see e.g. [36])
and also at low order in perturbation theory in [16]. Given the formulation (A.13), the
fact the two models are in the same universality class can be rephrased by saying that the
RG flows which start at infinite H or finite H in the UV should end up in the same IR
fixed point. As a final comment, we would like to mention that in physical systems where
branched polymers arise one cannot typically exclude the presence of closed loops [37] so in
fact lattice animals define themselves a physically relevant system.
Now that we constructed the model (A.13) which counts diluted lattice animals, we
want to show how to reformulate it in terms of a field theory. We start by rewriting the
partition function as follows

## PDF page 35

of the logarithm and let us work for simplicity in d = 1; in this case a site x has two
nearest neighbours at position x + a and x − a, so s(x) · s(x + a) + s(x) · s(x − a) =
1 4
2s(x) · s(x) + a2 s(x) · ∂ 2 s(x) + 12
a s(x) · ∂ 4 s(x) + . . . . Similarly the k = 2 term give rise to
2
2
[s(x)·s(x+a)] +[s(x)·s(x−a)] = 2[s(x)·s(x)]2 +2[(∂s(x)·s(x))2 +s(x)·s(x) s(x)·∂ 2 s(x)]+. . .
and so on. Of course it is trivial to generalize this to higher dimensions by using derivatives
∂ µ along all space directions. The terms in the second sum in (A.21) are defined at a single
site x so they do not change by taking the continuum limit (however we still have to include
in the final action all possible terms in the expansion of the logarithm). The result takes
the form
[

d x p0 s(x) · ∂ 2 s(x) + p2 s(x) · s(x) + p4 (s(x) · s(x))2 + · · · +
d

+

n
∑
j=1

q1 s1j (x) +

∑
k≥3

qk

n
∑
j=1

sk1j (x) +

∑
k≥1

qk′

n
∑

(A.22)

]

sk1j (x)(s(x) · s(x)) + . . .

,

j=1

where the first dots correspond to terms with higher powers of s(x) · s(x) possibly dressed
with derivatives and the second dots take into account higher powers of s(x) · s(x) which
∑
multiply nj=1 sk1j . The coefficients pi are written in terms of K and the lattice spacing a
while the coefficients qi , qi′ , . . . are written in terms of polynomials in the variables H and
Wi . In order to have an action written in a canonical form we first to rescale the fields sij (x)
to get a kinetic term normalized as 12 ∂ µ s(x) · ∂µ s(x). Secondly we get rid of linear terms
proportional to q1 in the action by shifting s1j (x). Because of this shift, the coefficients
multiplying the monomials in s1j (x) and in si̸=1 j (x) become different. In particular the
∑
mass terms s21j (x) and i>1 s2ij (x) appear with a different coefficient. When we study
this action in the IR we tune the mass for i = 1 in order to reach the critical point. All
other fields are massive and are integrated out. The resulting action takes the form of an
Sn model
⎡

∫

⎤

∑
∑
∑
1∑ µ
dd x ⎣
∂ s1j ∂µ s1j + c1
s21j + c2 ( s1j )2 + c3
s31j + . . . ⎦ ,
2 j
j
j
j

(A.23)

where the dots stand for any Sn invariant interaction defined by powers of s1j possibly
dressed with derivatives and the coefficients ci are written in terms of the pi and qi of (A.22).
After mapping s1j → φj , this action is exactly of the form (2.3) (with V (φ) = c1 φ2 + c3 φ3
and c2 = −H/2) which is the starting point for analyzing the RF φ3 model in terms of
replica variables.23

B

Classification of leaders in RF φ3 theory

The classification of leaders of the RF φ3 theory is very similar to the one of the RFIM
described in [1]. Indeed, the form of the leaders does not depend on the potential V (φ),
23

Notice that in the dots of (A.23) there is also the term
s s2 . This term corresponds to what
j1 ,j2 1j1 1j2
we call σ1 σ2 in the main text, which is an irrelevant deformation.

∑

– 33 –

JHEP08(2022)290

∫

## PDF page 36

Singlet

Leader

σ2

[

Leader type

2ωϕ + χi ∆=6

susy-writable

σ12

[ω 2 ]∆=8

susy-writable

]
2

Table 2. Scalar leaders with Nφ = 2, Nder = 0 in d = 8.

(d=8)

(d=6)

∆leader = ∆leader + Nφ .

(B.1)

Applying the equation above to the cases studied in [1] we find the lowest dimensional
leaders in the even-Nφ spectrum of φ3 theory in d = 8: the first susy-null leader is (χ2i )2
with dimension ∆ = 12 while the first non-susy-writable leader is (F6 )L and only appears
at dimension ∆ = 18. In [1] other susy-null leaders appear at ∆ ≤ 18, the second one is
ϕ2 (χ2i )2 with dimension ∆ = 16 in d = 8. In the following we want to check if in the odd-Nφ
spectrum of φ3 theory there are new low lying leaders in the susy-null and non-susy-writable
sectors. We will see that there are no new non-susy-writable leaders at ∆ ≤ 18, therefore
the lowest dimensional leader of this type is still F6 .24 Similarly we find that the first
susy-null leader is still (χ2i )2 , however we also find other susy-null leaders at ∆ ≤ 18 with
odd Nφ . The first new one is ϕ(χ2i )2 which appears at Nφ = 5 and has dimension 14 in
d = 8. In equation (3.9) in the main text we show that this operator is a member of an
infinite class of susy-null operators named Nk , which have leaders equal to ϕk (χ2i )2 , which
also describe the cases (χ2i )2 and ϕ2 (χ2i )2 discussed above.
24

Another non-susy-writable leader is F6,1 and can be found at dimension 20 as explained in the main
text. In this appendix we will not show this leader because we decided to focus on ∆ ≤ 18.

– 34 –

JHEP08(2022)290

nor on the space dimensions. The only differences are the following. First the classical
dimensions of the fields depend on the spacetime dimension d and the latter is different in
the two models (since we work close to the respective upper critical dimension). Secondly
the RFIM has an extra Z2 symmetry, and thus one is allowed to focus on leaders which
are singlet under Z2 (which are all composite operators made out of an even number of
elementary fields). In the RF φ3 theory the symmetry Z2 is absent, we will thus need to
consider also operators made out of an odd number of elementary fields.
Let us call Nφ the number of elementary fields and Nder the number of derivatives
that are contained in the composite operators. As an example of even-Nφ leaders, let us
consider the case of Nφ = 2. As for the RFIM, the possible singlets without derivatives
are σ2 , σ12 . All leaders with Nφ = 2 must be susy-writable as it was discussed in [1]. Here
the only difference is that their dimensions is computed in d = 8, as shown in table 2.
Similarly operators with derivatives will have the same exact form as the one described
[
]
in [1]. E.g. σ2(µ)(µ) = 2∂ω∂ϕ + (∂χi )2 ∆=8 . This should make it clear that we do not need
to repeat the classification for all even Nφ , which is given in [1] and still holds, up to the
scaling dimension of the fields which can be very easily recomputed following the d = 8
rules that ∆ϕ = 2, ∆χi = 3 and ∆ω = 4. It is easy to see that this amounts to shift the
d = 6 dimension in all tables of [1] by Nφ , namely

## PDF page 37

Singlet

Leader

σ3

[

Leader type

σ1 σ2

[2ϕω 2 + χ2i ω]∆=10

susy-writable

σ13

[ω 3 ]

susy-writable

]
ωϕ2 + χ2 ϕ
i

∆=8

∆=12

susy-writable

Table 3. Scalar leaders with Nφ = 3, Nder = 0 in d = 8.

Leader

σ3(µ)(µ)

[

Leader type

σ1(µ) σ2(µ)

[ωµ (χi χi,µ + ωϕµ + ϕωµ )]∆=12

2χi ϕ,µ χi,µ + ϕχ2i,µ + ωϕ2,µ + 2ϕϕ,µ ω,µ
(

σ1 σ2(µ)(µ)
σ1 σ1(µ) σ1(µ)

[ω χ2i,µ + 2ϕµ ωµ
[ωωµ2 ]∆=14

)

]∆=12

]
∆=10

susy-writable
susy-writable
susy-writable
susy-writable

Table 4. Scalar leaders with Nφ = 3, Nder = 2 in d = 8.

B.1

Nφ = 1

A single operator with Nφ = 1 is present,
σ1 = ω ,

(B.2)

which is susy-writable. When we add this operator to the Lagrangian, the physics does not
change since ω can be reabsorbed by shifting the fields. In SUSY language it corresponds
to adding Φ to the SUSY Lagrangian. Equivalently this corresponds to adding φ̂ to the
dimensionally reduced Lagrangian. In both cases this perturbation can simply be undone
by a shift in the fields (respectively Φ and φ̂).
B.2

Nφ = 3

There are only three leaders with Nφ = 3 and no derivatives. They are all of the susywritable type as shown in table 3. We can also consider leaders with Nφ = 3 and two
derivatives. The result is still a list of susy-writable operators as shown in table 4.
By increasing the number of derivatives we do not find new interesting operators.
Indeed all σk with k ≤ 2 have a susy writable leader with no followers. So, any combination
of these with any number of derivatives will be susy-writable. One can thus focus on
σ3 —which is the only operator with Nφ = 3 that has followers (which are not always
susy-writable)— and try to dress it with derivatives. But one can see that these do not
produce new non-susy-writable or susy-null operators. Indeed we first notice that there
exists a single independent25 way to write a Lorentz scalar by dressing σ3 with derivatives:
∑
(k)
σ3 ≡ i φi (∂µ1 . . . ∂µk φi )2 . The associated leaders are susy-writable. One may still worry
25

(k)

All other dressings are equal to σ3 plus total derivatives plus terms built by dressing σ1 and σ2 with
derivatives (which we already considered above).

– 35 –

JHEP08(2022)290

Singlet

## PDF page 38

Singlet

Leader

σ5

[ 3
]
ϕ (ϕω + 2χ2 )

Leader type
i

susy-writable

N1

∆=12
2
2
[ϕ ω(2ϕω + 3χi )]∆=14
[ϕ(χ2i )2 ]∆=14

σ3 σ12

[ϕω 2 (ϕω + χ2i )]∆=16

susy-writable

4σ3 σ12 − 3σ22 σ1
σ2 σ13

[ω(χ2i )2 ]∆=16
[ω 3 (2ϕω + χ2i )]∆=18

susy-null

σ1 σ4

susy-writable
susy-null

susy-writable

that another singlet could have the same susy-writable leader and that their difference
(k)
should be considered as a new leader. However the leader of σ3 has lower dimension than
any other leader built by composing products of σ1 and σ2 dressed by derivatives, as one
can see for the example of two derivatives in table 4. This ensures that there is no other
(k)
singlet with the same leader and therefore that the followers of σ3 can always be neglected.
In summary we find that no matter how many derivatives we consider, any operator built
out of Nφ = 3 fields must have a susy-writable leader.
B.3

Nφ = 5

We now focus on the operators built out of five fields. The list of Nφ = 5 leaders with
∆ ≤ 18 and Nder = 0 is shown in table 5. Here we find the first odd-Nφ susy-null operator
which we call (N5 )L according to the definition (3.9) in the main text. This operator has
dimension ∆ = 14 and leader equal to ϕ(χ2i )2 . At dimensions ∆ = 16 we also find the new
susy-null leader ω(χ2i )2 .
By considering Nder = 2 we must take into account the following Sn singlets
σ5,(µ)(µ) ,

σ4,(µ)(µ) σ1 ,

σ3,(µ)(µ) σ2 ,

σ3 σ2,(µ)(µ) ,

σ3,(µ)(µ) σ12 ,

σ2,(µ)(µ) σ2 σ1 ,

σ2,(µ)(µ) σ13 ,

σ4,(µ) σ1,(µ) ,

σ3,(µ) σ2,(µ) ,

σ3,(µ) σ1,(µ) σ1 ,

σ2,(µ) σ2,(µ) σ1 ,

σ2,(µ) σ1,(µ) σ12 ,

2
σ1,(µ)
σ13 .

(B.3)

Combinations of these singlets give either susy-writable or susy-null leaders. At dimension
16 there are five leaders: three susy-writable and two susy-null. Since the two susy-null
leaders have dimension greater than (N5 )L , they are not very important for our classification.
However it is instructive to show their explicit form:
(1)

Onull ≡ 2σ3 σ2,(µ)(µ) − 6σ2 σ3,(µ)(µ) + 6σ1 σ4,(µ)(µ) + 3σ22 σ1 − 4σ3 σ12 ,
2σ2(µ)(µ) σ3
(2)
Onull ≡ −2σ1 σ4(µ)(µ) +
− 2σ1(µ) σ4(µ) + 2σ2(µ) σ3(µ) ,
3

(B.4)
(B.5)

which gives rise to the susy-null leaders
(

(1)

Onull

)
L

= −3∂µ [ϕ,µ (χ2i )2 ]∆=16 ,

(

(2)

Onull

– 36 –

)

(

L

)

= [∂µ ϕχ2i ∂µ (χ2j ) ]∆=16 .

(B.6)

JHEP08(2022)290

Table 5. Scalar leaders with Nφ = 5, Nder = 0 in d = 8.

## PDF page 39

Singlet

Leader

σ7

[ 5
]
ϕ (ϕω + 3χ2 )

Leader type
i

∆=16
4
2
[ϕ ω(2ϕω + 5χi )]∆=18
[ϕ3 (χ2i )2 ]∆=18

σ1 σ6
N3

susy-writable
susy-writable
susy-null

Table 6. Scalar leaders with Nφ = 7, Nder = 0 in d = 8.

1
2σ3 σ2(µ) − 3σ2 σ3(µ) − σ4 σ1(µ) + 2σ1 σ4(µ)
2
(
)
2
2
1
(2)
Onull = ∂µ − σ1 σ4(µ) + σ3 σ2(µ) − σ4 σ1(µ) .
3
3
3
(1)
Onull = ∂µ

(

)

,

(B.7)
(B.8)

Since the operators are total derivatives they do not affect the RG and we can discard them
for the purpose of the present classification. Analogous considerations are valid for the next
null operators with Nder = 2, Nφ = 5 which have dimensions 18 and are built by dressing
ω(χ2i )2 with derivatives.
By studying higher number of derivatives with Nφ = 5 we do not find any non-susywritable leader with ∆ ≤ 18. E.g. by considering Nder = 4 the lowest dimensional operator
is σ5 dressed by derivatives which has a susy-writable leader with dimension 16, while the
first susy-null operator has already dimensions ∆ = 18.
To summarize for Nφ = 5 we found that the lowest dimensional susy-null leader is N1
and that there are no non-susy-writable leaders up to ∆ ≤ 18.
B.4

Nφ = 7

The Nφ = 7 leaders with Nder = 0 and ∆ ≤ 18 are considered in table 6 We notice that
the only susy-null operator belongs to the family Nk for k = 7 and it has dimension 18 in
d = 8. It is easy to see that all leaders with Nder > 0 and ∆ ≤ 18 are susy-writable.

C

Box operators

The only susy-writable operators which may destabilize the SUSY fixed point are those which
transform in the (2, 2) irrep of OSp(d|2). Since these are susy-writable their anomalous
dimensions are determined by computing anomalous dimensions of the corresponding
operators in φ̂3 theory in d − 2 dimensions. In this appendix we show the form of these
operators both in φ̂3 theory and in the SUSY theory.
In order to define operators which have good scaling dimension at one loop, we consider
the primary operator built out of free scalars φ̂ in dˆ = d − 2 dimension. We are interested
in primaries that transform in the (2, 2) representation of SO(d). It is easy to show that

– 37 –

JHEP08(2022)290

It is interesting to notice that the leaders of O(1) and O(2) are just total derivatives, indeed
these operators can be written as derivative of spin-one Sn -singlets,

## PDF page 40

they take the form
(
(k)
B̂µν,ρσ
≡ φ̂k−3

φ̂,µν φ̂,ρσ φ̂ −

2dˆ
dˆ − 2

)Y

φ̂,µ φ̂,ν φ̂,ρσ

(C.1)

,

where k ≥ 3. To unpack (C.1), we contract it with polarization vectors z1µ z1ν z2ρ z2σ such that
z12 = z22 = z1 · z2 = 0. We thus obtain
B̂

(k)

(z1 , z2 ) ∝ φ̂

k−3

[

(

)

d (z1 ·∂)2 φ̂ (z2 ·∂)· φ̂ 2 −2d (z1 ·∂) φ̂ (z1 ·∂) (z2 ·∂) φ̂ (z2 ·∂) φ̂
(

2

[ (

+ d (z1 ·∂) φ̂

)

2

2

]

2

]

−(d−2)φ̂ (z1 ·∂) φ̂ (z2 ·∂) φ̂ ,
(C.2)

where each derivative is meant to act only on the closest φ̂ on its right. The two lowest
dimensional operators of this family are thus B̂ (3) and B̂ (4) .26
We now want to write down the correspondent SUSY superprimary B (k),ab,cd . We are
(k),θ θ̄,θ θ̄
especially interested in the highest component Bθθ̄
with all indices in directions θ and
(4)
θ̄. The operator B was explicitly written in [1] (in d = 6). In the following we thus focus
on B (3) , which can be written in components as follows
(3),θ θ̄,θ θ̄

Bθθ̄

(
)
(
)
(
)
∝ ω −86ψ,µ ψ̄,µ −ϕ2,µν −72ϕ,µ ω,µ +6ϕ,µ ψ,ν ψ̄,µν +ψ,µν ψ̄,ν −2ϕ,µν ψ ψ̄,µν +ψ,µν ψ̄
(
)
+6ϕ,µν ψ,µ ψ̄,ν +14ω,µ ψ ψ̄,µ +ψ,µ ψ̄ +6ϕ,µ ω,ν ϕ,µν +3ϕ,µ ϕ,ν ω,µν +158ω 3
(
)
2
+2ϕ −ψ,µν ψ̄,µν −ϕ,µν ω,µν +7ω,µ
,
(C.3)

where here, for simplicity, we set d = 8. To compute anomalous dimensions of this operator,
one can alternatively consider the lowest component of the same supermultiplet, which has
a considerably simpler form
(3),θ θ̄,θ θ̄

(

(

D

∝ ϕ 64ω 2 −2 14ψµ ψ̄µ +ϕ2µ,ν

))

(

)

(

)

+6ϕµ 7ψ ψ̄µ +7ψµ ψ̄+ϕν ϕµ,ν −6ω 42ψ ψ̄+5ϕ2µ .
(C.4)
(3)
In appendix D.3.4 we will compute the anomalous dimensions of B using the formulation (C.2) in terms of the φ̂3 theory. It would be nice to check this computation using the
SUSY descriptions (C.3) or (C.4).
B0

RG computations

In this appendix we give the details of the results shown in section 3. All our computations
will be at one loop order. For our theory this typically involves two vertices. It is suitable to
use Feynman diagrams for such cases, as opposed to the OPE method we used for one-loop
computations in [1]. We will use dimensional regularization scheme in our computations for
which we refer to [22, 38] for a good review.
We will work with the χi fields instead of ψ, ψ̄ fields. This is suitable for computing
anomalous dimensions of general susy-writable, susy-null and non-susy-writable operators.
26

To study the RFIM in [1] we considered the operator B̂ (4) , since it is the lowest dimensional operator in
this representation which is Z2 -even. Here the Z2 symmetry is not present thus we are allowed to consider
operators built out of an odd number of elementary fields like B̂ (3) .

– 38 –

JHEP08(2022)290

+(d−2)φ̂ (z1 ·∂) (z2 ·∂) φ̂

)

## PDF page 41

l

l

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

l
<latexit sha1_base64="P/ERgdEEBbpaoveuN/T2Jkm2UIk=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8GJJpKDHohePFe0HtKFstpN26WYTdjdCCf0JXjwo4tVf5M1/47bNQVtfWHh4Z4adeYNEcG1c99sprK1vbG4Vt0s7u3v7B+XDo5aOU8WwyWIRq05ANQousWm4EdhJFNIoENgOxrezevsJleaxfDSTBP2IDiUPOaPGWg/iIumXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVY9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwzsjaE=</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

l
<latexit sha1_base64="P/ERgdEEBbpaoveuN/T2Jkm2UIk=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8GJJpKDHohePFe0HtKFstpN26WYTdjdCCf0JXjwo4tVf5M1/47bNQVtfWHh4Z4adeYNEcG1c99sprK1vbG4Vt0s7u3v7B+XDo5aOU8WwyWIRq05ANQousWm4EdhJFNIoENgOxrezevsJleaxfDSTBP2IDiUPOaPGWg/iIumXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVY9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwzsjaE=</latexit>

p

p

Figure 6. The Feynman diagrams for the one-loop renormalization of ⟨ϕ(p)ϕ(−p)⟩.

Wavefunction renormalization

Our theory is given by the Lagrangian (2.20) in d = 8 − ϵ dimension, written in Cardy
variables and mass term set to zero:
LL = ∂ϕB ∂ωB −

)
H 2
1
gB (
ωB + (∂χB )2 +
3ωB ϕ2B + 3χ2B ϕB .
2
2
6

(D.1)

The subscript ‘B’ denotes bare quantities that are related to the renormalized ones
as follows:27
ϕB = Zϕ ϕ,

ωB = Zω ω,

gB = Zg Zϕ−2 Zω−1 µϵ/2 g.

χB = Zχ χ,

(D.2)

Here µ is an arbitrary mass scale. The Z-s denote renormalization constants which can be
expanded in powers of 1/ϵ and g 2 as follows:
ZA = 1 +

∑ ∑

(p,q) 2p −q

zA

g ϵ

,

(D.3)

p⩾1 1⩽q⩽p

where the subscript A = g, ϕ, ω, χ. The above is very much similar to the usual φ3 -theory
fixed point in d = 6 − ϵ dimension. Correlation functions of the bare quantities contain poles.
Since those of the renormalized ones must be finite we should choose z (p,q) accordingly.
We begin with the most basic computation which is to obtain the wavefunction
renormalization constants Zϕ , Zω , Zχ . For this we consider the correlators ⟨ϕ(p)ω(−p)⟩,
⟨ϕ(p)ϕ(−p)⟩ and ⟨χi (p)χj (−p)⟩ and demand that they should be finite. Their corrections
are shown in figure 6 and 7. The corrections to ⟨ϕ(p)ω(−p)⟩ and ⟨χi (p)χj (−p)⟩ are equal
and given by the integral:
(

Iϕω p

2

)

g2H
=
(2π)d

∫

( )
dd l
g 2 Hp2
=
−
+
O
ϵ0 .
(l2 )2 (p + l)2
6(4π)4 ϵ

(D.4)

The correction to ⟨ϕ(p)ϕ(−p)⟩ contains the above and also the additional integral:
(

)

Iϕϕ p2 =

g2H
(2π)d

∫

( )
dd l
g2H
=
+
O
ϵ0 .
(l2 )2 ((p + l)2 )2
3(4π)4 ϵ

27

(D.5)

Although we could consider separate renormalizations for the couplings corresponding to ϕ2 ω and χ2 ϕ,
it is sufficient to focus on just one. We comment later that the two vertices lead to the same renormalization
constant and beta function.

– 39 –

JHEP08(2022)290

D.1

## PDF page 42

l

l

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p

<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

p
<latexit sha1_base64="Pxex4gxdEG6Av/OmfvhlQK0fZNY=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjrWYyKFfcqrsQWQcvhwrkagzKX/1hzNIIpWGCat3z3MT4GVWGM4GzUj/VmFA2oSPsWZQ0Qu1ni0Vn5MI6QxLGyj5pyML9PZHRSOtpFNjOiJqxXq3Nzf9qvdSEN37GZZIalGz5UZgKYmIyv5oMuUJmxNQCZYrbXQkbU0WZsdmUbAje6snr0L6qepab15X6bR5HEc7gHC7BgxrU4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh85nz/aG4z0</latexit>

l
<latexit sha1_base64="P/ERgdEEBbpaoveuN/T2Jkm2UIk=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8GJJpKDHohePFe0HtKFstpN26WYTdjdCCf0JXjwo4tVf5M1/47bNQVtfWHh4Z4adeYNEcG1c99sprK1vbG4Vt0s7u3v7B+XDo5aOU8WwyWIRq05ANQousWm4EdhJFNIoENgOxrezevsJleaxfDSTBP2IDiUPOaPGWg/iIumXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVY9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwzsjaE=</latexit>

p

l
<latexit sha1_base64="P/ERgdEEBbpaoveuN/T2Jkm2UIk=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8GJJpKDHohePFe0HtKFstpN26WYTdjdCCf0JXjwo4tVf5M1/47bNQVtfWHh4Z4adeYNEcG1c99sprK1vbG4Vt0s7u3v7B+XDo5aOU8WwyWIRq05ANQousWm4EdhJFNIoENgOxrezevsJleaxfDSTBP2IDiUPOaPGWg/iIumXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVY9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwzsjaE=</latexit>

p

p

Figure 7. The Feynman diagrams for the one-loop renormalization of ⟨ϕ(p)ω(−p)⟩ (left) and
⟨χi ϕ(p)χj (−p)⟩ (right). We have suppressed the i, j indices.

(
)
1
1
g2H
2 0
⟨ϕ(p)ω(−p)⟩ = 2
−
+
O
g
ϵ
,
p Zϕ Zω
6(4π)4 ϵ
[

]

(
)
1 1
g2H
2 0
⟨χi (p)χj (−p)⟩ = 2
−
+
O
g
ϵ
,
p Zχ2
6(4π)4 ϵ
[

]

(D.6)

(
)
H
1
g2H
⟨ϕ(p)ϕ(−p)⟩ = 2 2
−
+ O g 2 ϵ0 .
2
4
(p ) Zϕ 6(4π) ϵ
[

]

This leads to
Zϕ = Zω = Zχ = 1 −
D.2

g2H
.
12(4π)4 ϵ

(D.7)

Beta function

We will now compute the one-loop beta function. For this we consider the 3-point function
⟨ϕ(p1 )ϕ(p2 )ϕ(p3 )⟩ and demand that it is free of ϵ poles. The tree level diagram involves
the ωϕ2 vertex. The one-loop diagrams are of the type shown in figure 8. The amputated
form of the 3-point function is given by:
3 3
⟨ϕ(p1 )ϕ(p2 )ω(p3 )⟩amp = gB + gB
[I(p1 , p2 ) + I(p3 , p1 )],
2

(D.8)

The renormalization constants appear through gB via (D.2). Iωϕ3 is given by the integral
I(p1 , p2 ) =

H
(2π)d

∫

dd l
,
(l2 )(l + p2 )2 ((l − p1 )2 )2

(D.9)

This is a triangular loop integral that can be evaluated using standard methods (see
e.g. [22, 38]), and gives the following ϵ pole:
I(p1 , p2 ) =

( )
H
+
O
ϵ0 .
3(4π)4 ϵ

(D.10)

Demanding that the pole cancels, and using the wave function renormalization constants
from (D.7) we obtain
g2H
Zg = 1 −
,.
(D.11)
(4π)4 ϵ

– 40 –

JHEP08(2022)290

Taking into account the respective symmetry factors the one-loop corrected 2-point
functions are given by:

## PDF page 43

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

p1

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

l
<latexit sha1_base64="NjY4KmoKgpkhBC7ytwmnMWcjm/M=">AAAB7HicbZBNS8NAEIYn9avWr6pHL4tF8GJJRNBj0YvHCqYttKFstpt26WYTdidCCf0NXjwo4tUf5M1/47bNQVtfWHh4Z4adecNUCoOu++2U1tY3NrfK25Wd3b39g+rhUcskmWbcZ4lMdCekhkuhuI8CJe+kmtM4lLwdju9m9fYT10Yk6hEnKQ9iOlQiEoyitXx5kfa9frXm1t25yCp4BdSgULNf/eoNEpbFXCGT1Jiu56YY5FSjYJJPK73M8JSyMR3yrkVFY26CfL7slJxZZ0CiRNunkMzd3xM5jY2ZxKHtjCmOzHJtZv5X62YY3QS5UGmGXLHFR1EmCSZkdjkZCM0ZyokFyrSwuxI2opoytPlUbAje8smr0Lqse5YfrmqN2yKOMpzAKZyDB9fQgHtogg8MBDzDK7w5ynlx3p2PRWvJKWaO4Y+czx8zfo5F</latexit>

p1
l

p1

<latexit sha1_base64="NjY4KmoKgpkhBC7ytwmnMWcjm/M=">AAAB7HicbZBNS8NAEIYn9avWr6pHL4tF8GJJRNBj0YvHCqYttKFstpt26WYTdidCCf0NXjwo4tUf5M1/47bNQVtfWHh4Z4adecNUCoOu++2U1tY3NrfK25Wd3b39g+rhUcskmWbcZ4lMdCekhkuhuI8CJe+kmtM4lLwdju9m9fYT10Yk6hEnKQ9iOlQiEoyitXx5kfa9frXm1t25yCp4BdSgULNf/eoNEpbFXCGT1Jiu56YY5FSjYJJPK73M8JSyMR3yrkVFY26CfL7slJxZZ0CiRNunkMzd3xM5jY2ZxKHtjCmOzHJtZv5X62YY3QS5UGmGXLHFR1EmCSZkdjkZCM0ZyokFyrSwuxI2opoytPlUbAje8smr0Lqse5YfrmqN2yKOMpzAKZyDB9fQgHtogg8MBDzDK7w5ynlx3p2PRWvJKWaO4Y+czx8zfo5F</latexit>

l
<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p1

l

p3

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p3

l + p3

l + p3

<latexit sha1_base64="NYfQ8tnbBwSvGnDaAfxCQk8Nv7I=">AAAB7HicbZBNS8NAEIYn9avWr6pHL4tFEISSqKDHohePFYwttKFstpN26WYTdjdCCf0NXjwo4tUf5M1/47bNQVtfWHh4Z4adecNUcG1c99sprayurW+UNytb2zu7e9X9g0edZIqhzxKRqHZINQou0TfcCGynCmkcCmyFo9tpvfWESvNEPphxikFMB5JHnFFjLV+cpb2LXrXm1t2ZyDJ4BdSgULNX/er2E5bFKA0TVOuO56YmyKkynAmcVLqZxpSyER1gx6KkMeogny07ISfW6ZMoUfZJQ2bu74mcxlqP49B2xtQM9WJtav5X62Qmug5yLtPMoGTzj6JMEJOQ6eWkzxUyI8YWKFPc7krYkCrKjM2nYkPwFk9ehsfzumf5/rLWuCniKMMRHMMpeHAFDbiDJvjAgMMzvMKbI50X5935mLeWnGLmEP7I+fwBM3iORQ==</latexit>

<latexit sha1_base64="NYfQ8tnbBwSvGnDaAfxCQk8Nv7I=">AAAB7HicbZBNS8NAEIYn9avWr6pHL4tFEISSqKDHohePFYwttKFstpN26WYTdjdCCf0NXjwo4tUf5M1/47bNQVtfWHh4Z4adecNUcG1c99sprayurW+UNytb2zu7e9X9g0edZIqhzxKRqHZINQou0TfcCGynCmkcCmyFo9tpvfWESvNEPphxikFMB5JHnFFjLV+cpb2LXrXm1t2ZyDJ4BdSgULNX/er2E5bFKA0TVOuO56YmyKkynAmcVLqZxpSyER1gx6KkMeogny07ISfW6ZMoUfZJQ2bu74mcxlqP49B2xtQM9WJtav5X62Qmug5yLtPMoGTzj6JMEJOQ6eWkzxUyI8YWKFPc7krYkCrKjM2nYkPwFk9ehsfzumf5/rLWuCniKMMRHMMpeHAFDbiDJvjAgMMzvMKbI50X5935mLeWnGLmEP7I+fwBM3iORQ==</latexit>

<latexit sha1_base64="pkDYgGp4MaM5/egwwLMmaa6RlLk=">AAAB63icbZDLSgMxFIbP1Futt6pLN8EiuCozRdBl0Y3LCvYC7VAyaaYNzWVIMkIZ+gpuXCji1hdy59uYaWehrT8EPv5zDjnnjxLOjPX9b6+0sbm1vVPereztHxweVY9POkalmtA2UVzpXoQN5UzStmWW016iKRYRp91oepfXu09UG6bko50lNBR4LFnMCLa5lQwblWG15tf9hdA6BAXUoFBrWP0ajBRJBZWWcGxMP/ATG2ZYW0Y4nVcGqaEJJlM8pn2HEgtqwmyx6xxdOGeEYqXdkxYt3N8TGRbGzETkOgW2E7Nay83/av3UxjdhxmSSWirJ8qM45cgqlB+ORkxTYvnMASaauV0RmWCNiXXx5CEEqyevQ6dRDxw/XNWat0UcZTiDc7iEAK6hCffQgjYQmMAzvMKbJ7wX7937WLaWvGLmFP7I+/wBNheNrQ==</latexit>

p2

<latexit sha1_base64="pkDYgGp4MaM5/egwwLMmaa6RlLk=">AAAB63icbZDLSgMxFIbP1Futt6pLN8EiuCozRdBl0Y3LCvYC7VAyaaYNzWVIMkIZ+gpuXCji1hdy59uYaWehrT8EPv5zDjnnjxLOjPX9b6+0sbm1vVPereztHxweVY9POkalmtA2UVzpXoQN5UzStmWW016iKRYRp91oepfXu09UG6bko50lNBR4LFnMCLa5lQwblWG15tf9hdA6BAXUoFBrWP0ajBRJBZWWcGxMP/ATG2ZYW0Y4nVcGqaEJJlM8pn2HEgtqwmyx6xxdOGeEYqXdkxYt3N8TGRbGzETkOgW2E7Nay83/av3UxjdhxmSSWirJ8qM45cgqlB+ORkxTYvnMASaauV0RmWCNiXXx5CEEqyevQ6dRDxw/XNWat0UcZTiDc7iEAK6hCffQgjYQmMAzvMKbJ7wX7937WLaWvGLmFP7I+/wBNheNrQ==</latexit>

p2

(

)

∂g
We thus obtain the beta function βg ≡ µ ∂µ
as follows:

[
]
∂ log gB
∂
ϵ
3gH
1
=
log Zg Zϕ−2 Zω−1 µϵ/2 g = −
βg + βg ,
3
∂ log µ
∂ log µ
2 2(4π) ϵ
g
ϵg
3g 3 H
⇒ βg = − −
2
4(4π)4

0=

This gives a fixed point at

2(4π)4 ϵ
.
(D.12)
3H
are equivalent as they are related by transforming
g⋆2 = −

The two solutions to g⋆
ϕ → −ϕ, ω → −ω .
The same result can be obtained by considering the 3-point function ⟨χj (p1 )χj (p2 )ϕ(p3 )⟩.
It involves the vertex χ2i ϕ2 at tree level. At one loop we have two diagrams which give the
same Zg . This also follows from the equivalence of the Lagrangian (D.1) with the SUSY
theory (2.22).
D.3

Renormalization of local operators

For RG analysis of local operators we consider bare operators OiB (composed of bare fields),
that are related to renormalized operators OjB by a mixing (renormalization) matrix Zij :
OiB = Zij Oj .

(D.13)

Similar to the renormalization constants of previous subsection, the matrix Zij can be
expanded in powers of 1/ϵ and g as follows
Zij = δij +

g2
zij + . . . .
ϵ

(D.14)

The matrix zij has to be fixed by computing one-loop corrections to correlation functions of
Oj and requiring them to be free of 1/ϵ poles. In general, this matrix is of block diagonal
form. A certain block in zij corresponds to operators with equal number of fields and equal
classical dimension ∆0i = ∆0j .

– 41 –

JHEP08(2022)290

Figure 8. The Feynman diagrams for the one-loop renormalization of g. The shown diagrams
correct the correlator ⟨ϕ(p1 )ϕ(p2 )ω(p3 )⟩ at one loop.

## PDF page 44

The matrix Z gives the anomalous dimension matrix Γ as follows:
d
Γ(g) ≡ Z −1 . d log
µZ .

(D.15)

2

d
dZ d(g )
Writing d log
µ Z = dg 2 d log µ and using the definition of beta function it is then simple
to obtain:
( )
Γij (g) = −g 2 zij + O g 4 .
(D.16)

D.3.1

Anomalous dimension of ϕ, ω, χ

Let us first compute the anomalous dimension of the fundamental fields ϕ, ω, χi . Their
renormalization constants we computed in (D.7) . Using (D.16) we immediately get the
anomalous dimension:
ϵ
γϕ = γω = γχ = − .
(D.17)
18
As expected this is same as the well-known field anomalous dimension for Lee-Yang fixed
point in d = 6 − ϵ dimensions [22].
D.3.2

Susy-null leaders

In this section we will compute the anomalous dimensions of some susy-null leader operators.
The ones we consider correspond to the class of singlet operators Nk we introduced in
section 3.2. For k = 4, 5, 6 their leaders (Nk )L = (χ2i )2 ϕk−4 give susy-null operators with the
three lowest classical dimensions. These are given by (χ2i )2 , ϕ(χ2i )2 , ϕ2 (χ2i )2 respectively.
Since each (Nk )L has the lowest classical dimension among operators with k fields we may
simply represent their respective renormalization constants as follows:
[(Nk )L ]B = Zk (Nk )L .
To compute the renormalization constant Zk we consider the correlator
⟨(Nk )L (p = 0)χj (p1 )χk (p2 )χl (p3 )χm (p4 )ϕ(p5 ) · · · ϕ(pk )⟩.
The one-loop triangle diagram corrections are shown in figure 9. All the diagrams involve
the same loop integral that we had earlier in (D.9).
It is straghtforward to compute the symmetry factors associated to each diagram.
Demanding that the 1ϵ term vanishes from the correlator above we get the following condition:
∑ Iϕω p2
1 k+4
i
k − k − 8 [I(p1 , p1 + p2 )]ϵ−1 −
2
2 i=1
p2i

3
Zk−1 = −

(

2

[

)

– 42 –

(

)]

.
ϵ−1

(D.18)

JHEP08(2022)290

This has to be evaluated at the fixed point given by (D.12).
Diagonalization of Γ gives the renormalized operators, whose dimensions are given by the
∑ (m)
(m)
eigenvalues. For an eigenvector e(m) satisfying i ei Γij = γm ei , we get a renormalized
(
)
R = 1 + γm ∑ e(m) O B having an anomalous dimension ∆ − ∆0 = γ .
operator Om
m
m
m
j j
j
ϵ

## PDF page 45

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p3 p2 p4 p1 l 1
<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

<latexit sha1_base64="berNMFBEL75BVbf5uEM+UZJp20k=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9SD6ft+tejVvLrIKfgFVKNTou1+9QcKyGKVhgmrd9b3UBDlVhjOB00ov05hSNqZD7FqUNEYd5PNVp+TMOgMSJco+acjc/T2R01jrSRzazpiakV6uzcz/at3MRNdBzmWaGZRs8VGUCWISMrubDLhCZsTEAmWK210JG1FFmbHpVGwI/vLJq9C6qPmW7y+r9ZsijjKcwCmcgw9XUIc7aEATGAzhGV7hzRHOi/PufCxaS04xcwx/5Hz+APlbjZQ=</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p3 p2 p4 p1 l 1
<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

<latexit sha1_base64="XjExIuN720nXN9wFn/WS9ivKs8o=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSKdRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVoX1U9y/e1SuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwQOjZs=</latexit>

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

<latexit sha1_base64="berNMFBEL75BVbf5uEM+UZJp20k=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9SD6ft+tejVvLrIKfgFVKNTou1+9QcKyGKVhgmrd9b3UBDlVhjOB00ov05hSNqZD7FqUNEYd5PNVp+TMOgMSJco+acjc/T2R01jrSRzazpiakV6uzcz/at3MRNdBzmWaGZRs8VGUCWISMrubDLhCZsTEAmWK210JG1FFmbHpVGwI/vLJq9C6qPmW7y+r9ZsijjKcwCmcgw9XUIc7aEATGAzhGV7hzRHOi/PufCxaS04xcwx/5Hz+APlbjZQ=</latexit>

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

<latexit sha1_base64="BLT+aPe6yEfBJxz5UwJDYSSlHCI=">AAAB6XicbZBNS8NAEIYn9avWr6pHL4tF8GJJpKDHohePVewHtKFstpt26WYTdidCCf0HXjwo4tV/5M1/47bNQVtfWHh4Z4adeYNECoOu++0U1tY3NreK26Wd3b39g/LhUcvEqWa8yWIZ605ADZdC8SYKlLyTaE6jQPJ2ML6d1dtPXBsRq0ecJNyP6FCJUDCK1nq4kP1yxa26c5FV8HKoQK5Gv/zVG8QsjbhCJqkxXc9N0M+oRsEkn5Z6qeEJZWM65F2Likbc+Nl80yk5s86AhLG2TyGZu78nMhoZM4kC2xlRHJnl2sz8r9ZNMbz2M6GSFLlii4/CVBKMyexsMhCaM5QTC5RpYXclbEQ1ZWjDKdkQvOWTV6F1WfUs39cq9Zs8jiKcwCmcgwdXUIc7aEATGITwDK/w5oydF+fd+Vi0Fpx85hj+yPn8AT1fjSc=</latexit>

p2

l
l + p2
<latexit sha1_base64="/OQV7X9dF+cY7Tpf7RydkIMgzc4=">AAAB7HicbZBNS8NAEIYnftb6VfXoZbEIglCSIuix6MVjBdMW2lA22027dLMJuxOhhP4GLx4U8eoP8ua/cdvmoK0vLDy8M8POvGEqhUHX/XbW1jc2t7ZLO+Xdvf2Dw8rRccskmWbcZ4lMdCekhkuhuI8CJe+kmtM4lLwdju9m9fYT10Yk6hEnKQ9iOlQiEoyitXx5mfbr/UrVrblzkVXwCqhCoWa/8tUbJCyLuUImqTFdz00xyKlGwSSflnuZ4SllYzrkXYuKxtwE+XzZKTm3zoBEibZPIZm7vydyGhsziUPbGVMcmeXazPyv1s0wuglyodIMuWKLj6JMEkzI7HIyEJozlBMLlGlhdyVsRDVlaPMp2xC85ZNXoVWveZYfrqqN2yKOEpzCGVyAB9fQgHtogg8MBDzDK7w5ynlx3p2PReuaU8ycwB85nz8x9I5E</latexit>

l + p 1 + p2
<latexit sha1_base64="RHk4ZDbIqLzjaLep82iWlLhFClE=">AAAB8HicbVBNSwMxEJ2tX7V+VT16CRZBEMpuEfRY9OKxgv2QdinZNNuGJtmQZIWy9Fd48aCIV3+ON/+NabsHbX0w8Hhvhpl5keLMWN//9gpr6xubW8Xt0s7u3v5B+fCoZZJUE9okCU90J8KGciZp0zLLaUdpikXEaTsa38789hPVhiXywU4UDQUeShYzgq2THvmF6geuav1yxa/6c6BVEuSkAjka/fJXb5CQVFBpCcfGdANf2TDD2jLC6bTUSw1VmIzxkHYdlVhQE2bzg6fozCkDFCfalbRorv6eyLAwZiIi1ymwHZllbyb+53VTG1+HGZMqtVSSxaI45cgmaPY9GjBNieUTRzDRzN2KyAhrTKzLqORCCJZfXiWtWjVw/P6yUr/J4yjCCZzCOQRwBXW4gwY0gYCAZ3iFN097L96797FoLXj5zDH8gff5A5MWj5c=</latexit>

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

p1

Here Iϕω is to account for external leg corrections and is given by (D.4). With I(p1 , p1 + p2 )
computed previously in (D.10) we get the following condition for cancellation of 1ϵ singlarities:
(

)

Zk−1 = 1 − 6k 2 − 7k − 48

H g2
.
12(4π)4 ϵ

(D.19)

Using the general formula (D.16) we get the anomalous dimensions of leaders of Nk :
γ(Nk )L =
D.3.3

)
1 ( 2
6k − 7k − 48 ϵ.
18

(D.20)

Non-susy-writable leaders

Next we consider non-susy-writable leader operators. We will focus on leaders of the
particular class of singlets, call Feldman operators. We defined them in equation (3.12)
which we repeat for convenience:
(Fk )L =

k−2
∑
l=2

(−1)

l

( )( ′
∑
k

l

χli

)( ′
∑

)

χk−l
j

.

(D.21)

To compute the anomalous dimension of this we should, in principle, consider all opoerators
Oi with k fields and the same classical dimension as (Fk )L . Let us write their renormalization
matrix as OiB = Zij Oj . We take O1 = (Fk )L . We then have a renormalization matrix that
has the following form:
⎞
⎛
Z11 0 0 . . .
⎜
⎟
⎜ 0 ∗ ∗ ...⎟
⎜
(D.22)
Z = ⎜ 0 ∗ ∗ ...⎟
⎟,
⎝
⎠
.. .. .. . .
. . . .

– 43 –

JHEP08(2022)290

Figure 9. Diagrams that contribute to the one-loop correction of (Nk )L .

## PDF page 46

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

p2

l
<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

l + p2
<latexit sha1_base64="/OQV7X9dF+cY7Tpf7RydkIMgzc4=">AAAB7HicbZBNS8NAEIYnftb6VfXoZbEIglCSIuix6MVjBdMW2lA22027dLMJuxOhhP4GLx4U8eoP8ua/cdvmoK0vLDy8M8POvGEqhUHX/XbW1jc2t7ZLO+Xdvf2Dw8rRccskmWbcZ4lMdCekhkuhuI8CJe+kmtM4lLwdju9m9fYT10Yk6hEnKQ9iOlQiEoyitXx5mfbr/UrVrblzkVXwCqhCoWa/8tUbJCyLuUImqTFdz00xyKlGwSSflnuZ4SllYzrkXYuKxtwE+XzZKTm3zoBEibZPIZm7vydyGhsziUPbGVMcmeXazPyv1s0wuglyodIMuWKLj6JMEkzI7HIyEJozlBMLlGlhdyVsRDVlaPMp2xC85ZNXoVWveZYfrqqN2yKOEpzCGVyAB9fQgHtogg8MBDzDK7w5ynlx3p2PReuaU8ycwB85nz8x9I5E</latexit>

<latexit
sha1_base64="RHk4ZDbIqLzjaLep82iWlLhFClE=">AAAB8HicbVBNSwMxEJ2tX7V+VT16CRZBEMpuEfRY9OKxgv2QdinZNNuGJtmQZIWy9Fd48aCIV3+ON/+NabsHbX0w8Hhvhpl5keLMWN//9gpr6xubW8Xt0s7u3v5B+fCoZZJUE9okCU90J8KGciZp0zLLaUdpikXEaTsa38789hPVhiXywU4UDQUeShYzgq2THvmF6geuav1yxa/6c6BVEuSkAjka/fJXb5CQVFBpCcfGdANf2TDD2jLC6bTUSw1VmIzxkHYdlVhQE2bzg6fozCkDFCfalbRorv6eyLAwZiIi1ymwHZllbyb+53VTG1+HGZMqtVSSxaI45cgmaPY9GjBNieUTRzDRzN2KyAhrTKzLqORCCJZfXiWtWjVw/P6yUr/J4yjCCZzCOQRwBXW4gwY0gYCAZ3iFN097L96797FoLXj5zDH8gff5A5MWj5c=</latexit>

l+

p1 +

p2

p1

Figure 10. One-loop corrections to (Fk )L .

To show this consider the correlator ⟨(Fk )L (p = 0)χi1 (p1 ) . . . χik (pk )⟩. It has a one loop
correction as shown in figure 10. From the χ-χ legs and the associated contractions of K
matrices it is clear that we only get a correction to Z11 and no other component Z1j . The
fact that the components Zi1 (i > 1) would be 0 was argued in appendix H.3 of [1], and
this also applies for the cubic interactions considered in this paper. Hence for computation
of anomalous dimension of (Fk )L we have only to compute the renormalization constant
Z11 = Z(Fk )L and can neglect the other operators Oi̸=1 .
The loop diagram is again that of (D.10) and comes with the symmetry factor 12 k(k − 1).
Considering the correction due to k external legs we get:
1
1
Zk−1 = − k(k − 1)[I(p1 , p1 + p2 )]ϵ−1 −
2

[
]
k
∑
Iϕω (p2i )

2 i=1

This gives:
Zk−1 = 1 −

p2i

g2H
k(2k − 3).
12(4π)4 ϵ

.

(D.23)

ϵ−1

(D.24)

Using (D.16) we get the anomalous dimension:
γ(Fk )L =
D.3.4

k(2k − 3)
ϵ.
18

(D.25)

Susy-writable leaders

In this section we will compute the anomalous dimension of a class of susy-writable leaders,
specifically the box operators discussed in section 3.1 and appendix C. For convenience
we will compute anomalous dimension of the box operator in the φ̂3 theory in dˆ = 6 − ϵ
dimension. Via dimensional reduction that should give the same anomalous dimenision as
the operator we want.
The φ̂3 theory has the Lagrangian shown in (2.28) which we rewrite below for convenience (here we canonically normalize the action since the anomalous dimensions are
independent of this normalization):
S=

∫

dˆ

d x

[ (
1

2

∂ φ̂

)2

g
+ m φ̂ + φ̂3 .
6

– 44 –

2 2

]

(D.26)

JHEP08(2022)290

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

## PDF page 47

<latexit sha1_base64="v0/vP4Il+nxU5vg1a4XbDiBSmjE=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FSSItRj0YvHivYD2lA22027dLMJuxOhhP4ELx4U8eov8ua/cdvmoK0vLDy8M8POvEEihUHX/XYKG5tb2zvF3dLe/sHhUfn4pG3iVDPeYrGMdTeghkuheAsFSt5NNKdRIHknmNzO650nro2I1SNOE+5HdKREKBhFaz0kg9qgXHGr7kJkHbwcKpCrOSh/9YcxSyOukElqTM9zE/QzqlEwyWelfmp4QtmEjnjPoqIRN362WHVGLqwzJGGs7VNIFu7viYxGxkyjwHZGFMdmtTY3/6v1Ugyv/UyoJEWu2PKjMJUEYzK/mwyF5gzl1AJlWthdCRtTTRnadEo2BG/15HVo16qe5furSuMmj6MIZ3AOl+BBHRpwB01oAYMRPMMrvDnSeXHenY9la8HJZ07hj5zPHwEGjZk=</latexit>

l
<latexit sha1_base64="NNsnD3XVqdYxikBIsieTJwBm/Vs=">AAAB7HicbZBNS8NAEIYnftb6VfXoZbEIXixJEfRY9OKxgmkLbSib7aZdutmE3YlQQn+DFw+KePUHefPfuG1z0NYXFh7emWFn3jCVwqDrfjtr6xubW9ulnfLu3v7BYeXouGWSTDPus0QmuhNSw6VQ3EeBkndSzWkcSt4Ox3ezevuJayMS9YiTlAcxHSoRCUbRWr68TPv1fqXq1ty5yCp4BVShULNf+eoNEpbFXCGT1Jiu56YY5FSjYJJPy73M8JSyMR3yrkVFY26CfL7slJxbZ0CiRNunkMzd3xM5jY2ZxKHtjCmOzHJtZv5X62YY3QS5UGmGXLHFR1EmCSZkdjkZCM0ZyokFyrSwuxI2opoytPmUbQje8smr0KrXPMsPV9XGbRFHCU7hDC7Ag2towD00wQcGAp7hFd4c5bw4787HonXNKWZO4I+czx81Ao5G</latexit>

<latexit sha1_base64="uxN1TeCtw/JouRtuqyBIwjhbrqs=">AAAB6nicbZBNS8NAEIYn9avWr6pHL4tF8FQSLeix6MVjRfsBbSib7aRdutmE3Y1QQn+CFw+KePUXefPfuG1z0NYXFh7emWFn3iARXBvX/XYKa+sbm1vF7dLO7t7+QfnwqKXjVDFssljEqhNQjYJLbBpuBHYShTQKBLaD8e2s3n5CpXksH80kQT+iQ8lDzqix1kPSv+yXK27VnYusgpdDBXI1+uWv3iBmaYTSMEG17npuYvyMKsOZwGmpl2pMKBvTIXYtShqh9rP5qlNyZp0BCWNlnzRk7v6eyGik9SQKbGdEzUgv12bmf7VuasJrP+MySQ1KtvgoTAUxMZndTQZcITNiYoEyxe2uhI2ooszYdEo2BG/55FVoXVQ9y/e1Sv0mj6MIJ3AK5+DBFdThDhrQBAZDeIZXeHOE8+K8Ox+L1oKTzxzDHzmfPwKKjZo=</latexit>

p2

p2

l

p3

<latexit sha1_base64="BM8fe6iHHCoJyPx8AuUhP7leDek=">AAAB6HicbZBNS8NAEIYn9avWr6pHL4tF8FQSEeqx6MVjC/YD2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0vLDy8M8POvEEiuDau++0UNja3tneKu6W9/YPDo/LxSVvHqWLYYrGIVTegGgWX2DLcCOwmCmkUCOwEk7t5vfOESvNYPphpgn5ER5KHnFFjraYYlCtu1V2IrIOXQwVyNQblr/4wZmmE0jBBte55bmL8jCrDmcBZqZ9qTCib0BH2LEoaofazxaIzcmGdIQljZZ80ZOH+nshopPU0CmxnRM1Yr9bm5n+1XmrCGz/jMkkNSrb8KEwFMTGZX02GXCEzYmqBMsXtroSNqaLM2GxKNgRv9eR1aF9VPcvN60r9No+jCGdwDpfgQQ3qcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Y+czx/UC4zw</latexit>

l + p1
<latexit sha1_base64="+ggEHMObRQH2QNuu6Li2MXTpUZ8=">AAAB7HicbZBNS8NAEIYn9avWr6pHL4tFEISSiKDHohePFUxbaEPZbDft0s0m7E6EEvobvHhQxKs/yJv/xm2bg7a+sPDwzgw784apFAZd99spra1vbG6Vtys7u3v7B9XDo5ZJMs24zxKZ6E5IDZdCcR8FSt5JNadxKHk7HN/N6u0nro1I1CNOUh7EdKhEJBhFa/nyIu17/WrNrbtzkVXwCqhBoWa/+tUbJCyLuUImqTFdz00xyKlGwSSfVnqZ4SllYzrkXYuKxtwE+XzZKTmzzoBEibZPIZm7vydyGhsziUPbGVMcmeXazPyv1s0wuglyodIMuWKLj6JMEkzI7HIyEJozlBMLlGlhdyVsRDVlaPOp2BC85ZNXoXVZ9yw/XNUat0UcZTiBUzgHD66hAffQBB8YCHiGV3hzlPPivDsfi9aSU8wcwx85nz8wcI5D</latexit>

p1

Figure 11. One-loop correction to B̂ (3) in φ̂3 theory in d = 6 − ϵ.

The arguments are similar to what we described above in section D.3. The standard details
of this theory (beta function, critical point value) are given in section 2.
We want to use a form of the box operator that is simple for computation. In [1]
appendix F we used the idea of equivalence class {O} which contains an operator O and
other operators that are related to it by a total derivative. Hence all operators in {O}
are equivalent for perturbative RG computations. The box operator equivalence class
{B̂ (k) (z1 , z2 )} has the following operator:
B̂ (k) (z1 , z2 ) ≡ φ̂k−2 (((z1 .∂)(z2 .∂)φ̂)2 − (z1 .∂)2 φ̂(z2 .∂)2 φ̂).

(D.27)

which we defined as B̂ (k) for this section. It is easy to show that this is related to the
form (C.2) by a total derivative.
We define its renormalization as follows:
[

B̂ (k) (z1 , z2 )

]
B

= ZB̂ (k) B̂ (k) (z1 , z2 ).

(D.28)

We consider the correlator ⟨B̂ (k) (z1 , z2 )(p = 0)φ̂(p1 ) · · · φ̂(pn )⟩ for computing ZB̂ (k) . It can
be shown that the box operator as shown in (C.1) is a primary in free theory. Therefore for
computing the one-loop anomalous dimension we can ignore mixing with other operators.
We will focus on the case k = 3. The operator B̂ (3) may be written as follows:
(

∂ ρ ∂ σ φ̂ .

)

(D.29)

pµ1 pν1 pρ2 pσ2 + pµ2 pν2 pρ3 pσ3 + pµ3 pν3 pρ1 pσ1 + (µ ↔ ρ, ν ↔ σ) .

(D.30)

B̂ (3) (z1 , z2 ) = (z1µ z2ν z1ρ z2σ − z1µ z1ν z2ρ z2σ ) φ̂ ∂ µ ∂ ν φ̂

)(

At tree level the correlator is proportional to:

The correction to the correlator is given by the triangle diagram as shown in figure 11.

– 45 –

JHEP08(2022)290

<latexit sha1_base64="YgAuzWg+wuyQict0QiuK5Kx+fug=">AAAB6nicbZBNS8NAEIYn9avWr6hHL4tF8FQSEfRY9OKxov2ANpTNdtIu3WzC7kYooT/BiwdFvPqLvPlv3LY5aOsLCw/vzLAzb5gKro3nfTultfWNza3ydmVnd2//wD08aukkUwybLBGJ6oRUo+ASm4YbgZ1UIY1Dge1wfDurt59QaZ7IRzNJMYjpUPKIM2qs9ZD2/b5b9WreXGQV/AKqUKjRd796g4RlMUrDBNW663upCXKqDGcCp5VepjGlbEyH2LUoaYw6yOerTsmZdQYkSpR90pC5+3sip7HWkzi0nTE1I71cm5n/1bqZia6DnMs0MyjZ4qMoE8QkZHY3GXCFzIiJBcoUt7sSNqKKMmPTqdgQ/OWTV6F1UfMt319W6zdFHGU4gVM4Bx+uoA530IAmMBjCM7zCmyOcF+fd+Vi0lpxi5hj+yPn8Af9zjZg=</latexit>

## PDF page 48

Then we have integrals of the following forms depending on which leg(s) the derivatives act:
I1 = pγ3 pδ3

∫

dd l

(l + p1 )α (l + p1 )β
,
(l2 )(l + p1 )2 (l − p2 )2

I2 = pγ3 pδ3

∫

dd l

(l − p2 )α (l − p2 )β
,
(l2 )(l + p1 )2 (l − p2 )2

I3 =

∫

dd l

(l + p1 )α (l + p1 )β (l − p2 )γ (l − p2 )δ
,
(l2 )(l + p1 )2 (l − p2 )2

1
=2
2
(l )(l + p1 )2 (l − p2 )2

∫

dx1 dx2 dx3

δ(x1 + x2 + x3 − 1)
.
[x1 (l + p1 )2 + x2 (l − p2 )2 + x3 l2 ]3

(D.31)

Now using the standard change of variable q = l + x1 p1 − x2 p2 the above becomes
2

∫

dx1 dx2 dx3

δ(x1 + x2 + x3 − 1)
,
[q 2 + F ]3

[

]

F = x1 (1 − x1 )p21 + x2 (1 − x2 )p22 + 2x1 x2 p1 .p2 .
(D.32)

From the numerator of I1 one gets:
[

(

)

(l + p1 )α (l + p1 )β = q α q β + q α x2 pβ2 − (x1 − 1) pβ1 + (α ↔ β)
(

]

)

+ (pα1 (x1 − 1) − x2 pα2 ) pβ1 (x1 − 1) − x2 pβ2 .

(D.33)

The q α q β gives a term proportional to η αβ upon integration. Since the multiplicative factors
of z1 and z2 tensors in (D.29) eliminates all traces, we can ignore it. The terms proportional
to q α or q β are also simultaneously zero. So we are left with the last term of (D.33)
which gives:
)
pγ3 pδ3 ( α β
α β
α β
α β
I1 =
6p
p
+
3p
p
+
3p
p
+
2p
p
+ O (ϵ) .
1
1
2
2
1
2
1
2
12 (4π)3 ϵ

(D.34)

The integral I2 is obtained by simply replacing p1 ↔ −p2 . The I3 is slightly more tedious
as it is quartic in the numerator. But it follows exactly the same method, and gives:
1
1 µ ν ρ σ 1 µ ν ρ σ 1 µ ν ρ σ 1 µ ν ρ σ 1 µ ν ρ σ
p 1 p 1 p 1 p 1 + p2 p1 p 1 p1 + p 1 p 2 p 1 p 1 + p2 p2 p 2 p2 + p 2 p 2 p1 p 1
I3 =
3
60
60
30
90
(4π) ϵ 30
1
1
1
1
1
1
+ pµ1 pν1 pρ2 pσ1 + pµ2 pν1 pρ2 pσ1 + pµ1 pν2 pρ2 pσ1 + pµ2 pν2 pρ2 pσ1 + pµ1 pν1 pρ1 pσ2 + pµ2 pν1 pρ1 pσ2
15
36
36
60
15
36
]
1
1
19
1
1
+ pµ1 pν2 pρ1 pσ2 + pµ2 pν2 pρ1 pσ2 + pµ1 pν1 pρ2 pσ2 + pµ2 pν1 pρ2 pσ2 + pµ1 pν2 pρ2 pσ2 .
(D.35)
36
60
90
15
15
[

The final answer should be written in a form that matches the tree level momentum
dependence (D.30). The result from the loop integral can be brought to this form by using
momentum conservation p1 + p2 + p3 = 0.

– 46 –

JHEP08(2022)290

where the indices α, β, γ, ρ have to be chosen as appropriate.
Let us focus on I1 to show how to evaluate these integrals. We may write the denominator
in I1 as

## PDF page 49

Demanding that the correlator is free of ϵ−1 poles allows us to compute ZB̂ (3) as follows:
Z −1(3) = 1 −
B̂

g2
3g 2
+
.
2(4π)3 ϵ 12(4π)3 ϵ

(D.36)

The last part is the standard φ3 theory correction to the 3 external legs (see [22]). This
gives the following anomalous dimension of B̂ (3) (z1 , z2 ):
ϵ
γB̂ (3) = .
6

(D.37)

I4 =

∫

dd l
1
.
=
2
2
2
l (l + p1 ) (l − p2 )
(4π)3 ϵ

(D.38)

We explicitly computed the anomalous dimension of B̂ (k) (z1 , z2 ) for k = 3, . . . , 9. By
extrapolation we expect the result for generic k to be given by
γB̂ (k) =

)
1( 2
2k − 5k − 2 ϵ.
6

(D.39)

Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited. SCOAP 3 supports
the goals of the International Year of Basic Sciences for Sustainable Development.

References
[1] A. Kaviraj, S. Rychkov and E. Trevisani, Random field Ising model and Parisi-Sourlas
supersymmetry. Part II. Renormalization group, JHEP 03 (2021) 219 [arXiv:2009.10087]
[INSPIRE].
[2] A. Kaviraj, S. Rychkov and E. Trevisani, Parisi-Sourlas Supersymmetry in Random Field
Models, Phys. Rev. Lett. 129 (2022) 045701 [arXiv:2112.06942] [INSPIRE].
[3] A. Aharony, Y. Imry and S.K. Ma, Lowering of Dimensionality in Phase Transitions with
Random Fields, Phys. Rev. Lett. 37 (1976) 1364 [INSPIRE].
[4] G. Parisi and N. Sourlas, Random Magnetic Fields, Supersymmetry and Negative Dimensions,
Phys. Rev. Lett. 43 (1979) 744 [INSPIRE].
[5] N.G. Fytas, V. Martin-Mayor, M. Picco and N. Sourlas, Restoration of Dimensional Reduction
in the Random-Field Ising Model at Five Dimensions, Phys. Rev. E 95 (2017) 042117
[arXiv:1612.06156] [INSPIRE].
[6] N.G. Fytas, V. Martín-Mayor, G. Parisi, M. Picco and N. Sourlas, Evidence for
Supersymmetry in the Random-Field Ising Model at D = 5, Phys. Rev. Lett. 122 (2019)
240603 [arXiv:1901.08473] [INSPIRE].

– 47 –

JHEP08(2022)290

Now let us discuss the case of B̂ (k) (z1 , z2 ) for k > 3. The steps are similar to above. But
there is one extra loop integral where the derivatives of B̂ (k) are not distributed over the
internal legs. It is given by:

## PDF page 50

[7] N.G. Fytas, V. Martin-Mayor, M. Picco and N. Sourlas, Phase Transitions in Disordered
Systems: The Example of the Random-Field Ising Model in Four Dimensions, Phys. Rev. Lett.
116 (2016) 227201 [arXiv:1605.05072].
[8] A. Kaviraj, S. Rychkov and E. Trevisani, Random Field Ising Model and Parisi-Sourlas
supersymmetry. Part I. Supersymmetric CFT, JHEP 04 (2020) 090 [arXiv:1912.01617]
[INSPIRE].
[9] J.L. Cardy, Nonperturbative aspects of supersymmetry in statistical mechanics, Physica D 15
(1985) 123 .

[11] T.D. Lee and C.-N. Yang, Statistical theory of equations of state and phase transitions. II.
Lattice gas and Ising model, Phys. Rev. 87 (1952) 410 [INSPIRE].
[12] M.E. Fisher, Yang-Lee Edge Singularity and φ3 Field Theory, Phys. Rev. Lett. 40 (1978) 1610
[INSPIRE].
[13] J.L. Cardy, Conformal Invariance and the Yang-lee Edge Singularity in Two-dimensions, Phys.
Rev. Lett. 54 (1985) 1354 [INSPIRE].
[14] D.S. Gaunt, The critical dimension for lattice animals, J. Phys. A 13 (1980) L97.
[15] S. Redner, Mean end-to-end distance of branched polymers, J. Phys. A 12 (1979) L239.
[16] T.C. Lubensky and J. Isaacson, Statistics of lattice animals and dilute branched polymers,
Phys. Rev. A 20 (1979) 2130 [INSPIRE].
[17] G. Parisi and N. Sourlas, Critical Behavior of Branched Polymers and the Lee-Yang Edge
Singularity, Phys. Rev. Lett. 46 (1981) 871 [INSPIRE].
[18] D.C. Brydges and J.Z. Imbrie, Branched polymers and dimensional reduction, Annals Math.
158 (2003) 1019 [math-ph/0107005].
[19] J. Cardy, Lecture on Branched Polymers and Dimensional Reduction, cond-mat/0302495.
[20] F. Wegner, Supermathematics and its Applications in Statistical Physics: Grassmann Variables
and the Method of Supersymmetry, Springer, Berlin, Germany (2016) [DOI] [INSPIRE].
[21] C. Cordova, T.T. Dumitrescu and K. Intriligator, Multiplets of Superconformal Symmetry in
Diverse Dimensions, JHEP 03 (2019) 163 [arXiv:1612.00809] [INSPIRE].
[22] M. Srednicki, Quantum Field Theory, Cambridge University Press, Cambridge, U.K. (2007)
[DOI].
[23] L. Fei, S. Giombi, I.R. Klebanov and G. Tarnopolsky, Three loop analysis of the critical O(N)
models in 6-ε dimensions, Phys. Rev. D 91 (2015) 045011 [arXiv:1411.1099] [INSPIRE].
[24] J.A. Gracey, Four loop renormalization of φ3 theory in six dimensions, Phys. Rev. D 92 (2015)
025012 [arXiv:1506.03357] [INSPIRE].
[25] J.A. Gracey, I. Jack and C. Poole, The a-function in six dimensions, JHEP 01 (2016) 174
[arXiv:1507.02174] [INSPIRE].
[26] F.J. Wegner, The Critical State, General Aspects, in 12th School of Modern Physics on Phase
Transitions and Critical Phenomena, Ladek Zdroj Poland, 21–24 June 2001 [INSPIRE].
[27] D.E. Feldman, Critical Exponents of the Random-Field O(N ) Model, Phys. Rev. Lett. 88
(2002) 177202 [cond-mat/0010012].

– 48 –

JHEP08(2022)290

[10] C.-N. Yang and T.D. Lee, Statistical theory of equations of state and phase transitions. I.
Theory of condensation, Phys. Rev. 87 (1952) 404 [INSPIRE].

## PDF page 51

[28] S. Hikami, Conformal Bootstrap Analysis for Single and Branched Polymers, PTEP 2018
(2018) 123I01 [arXiv:1708.03072] [INSPIRE].
[29] J. Cardy, Logarithmic conformal field theories as limits of ordinary CFTs and some physical
applications, J. Phys. A 46 (2013) 494001 [arXiv:1302.4279] [INSPIRE].
[30] M. Hogervorst, M. Paulos and A. Vichi, The ABC (in any D) of Logarithmic CFT, JHEP 10
(2017) 201 [arXiv:1605.03959] [INSPIRE].
[31] F. Gliozzi, More constraining conformal bootstrap, Phys. Rev. Lett. 111 (2013) 161602
[arXiv:1307.3111] [INSPIRE].

[33] E. Trevisani, The Parisi-Sourlas Uplift and Infinitely Many Solvable Models in 4d, work in
progress.
[34] S. Franz, G. Parisi and F. Ricci-Tersenghi, Glassy critical points and the random field ising
model, J. Stat. Mech. 2013 (2013) L02001.
[35] J.L. Cardy, Scaling and renormalization in statistical physics, Cambridge University Press,
Cambridge, U.K. (1996) [DOI].
[36] H.-P. Hsu, W. Nadler and P. Grassberger, Simulations of lattice animals and trees, J. Phys. A
38 (2005) 775.
[37] T.C. Lubensky and J. Isaacson, Field theory for the statistics of branched polymers, gelation,
and vulcanization, Phys. Rev. Lett. 41 (1978) 829.
[38] H. Kleinert and V. Schulte-Frohlinde, Critical properties of φ4 theories, World Scientific,
Singapore (2001) [DOI].

– 49 –

JHEP08(2022)290

[32] J.D. Miller and K. De’Bell, Randomly branched polymers and conformal invariance,
hep-th/9211127 [INSPIRE].
