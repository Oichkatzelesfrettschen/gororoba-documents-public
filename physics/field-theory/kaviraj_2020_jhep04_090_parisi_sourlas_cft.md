Source: https://doi.org/10.1007/JHEP04(2020)090
PDF sha256: 1a105f0240376000c9f908c9a7ab8de55e075ceb916626d29ffa0c099feed660
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of kaviraj_2020_jhep04_090_parisi_sourlas_cft.pdf

Transcription of `kaviraj_2020_jhep04_090_parisi_sourlas_cft.pdf` in this directory, 49 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-49 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Published for SISSA by

Springer

Received: January 15, 2020
Accepted: March 26, 2020
Published: April 15, 2020

Random Field Ising Model and Parisi-Sourlas
supersymmetry. Part I. Supersymmetric CFT

a

Institut de Physique Théorique Philippe Meyer,
École Normale Supérieure, PSL Research University,
24 rue Lhomond, Paris, France
b
Laboratoire de Physique de l’Ecole normale supérieure, ENS,
Université PSL, CNRS, Sorbonne Université, Université de Paris,
F-75005 Paris, France
c
Institut des Hautes Études Scientifiques,
Bures-sur-Yvette, France

E-mail: apratim.kaviraj.01@gmail.com, slava.rychkov@gmail.com,
emiliotrevisani@yahoo.it
Abstract: Quenched disorder is very important but notoriously hard. In 1979, Parisi and
Sourlas proposed an interesting and powerful conjecture about the infrared fixed points with
random field type of disorder: such fixed points should possess an unusual supersymmetry,
by which they reduce in two less spatial dimensions to usual non-supersymmetric nondisordered fixed points. This conjecture however is known to fail in some simple cases, but
there is no consensus on why this happens. In this paper we give new non-perturbative
arguments for dimensional reduction. We recast the problem in the language of Conformal
Field Theory (CFT). We then exhibit a map of operators and correlation functions from
Parisi-Sourlas supersymmetric CFT in d dimensions to a (d − 2)-dimensional ordinary
CFT. The reduced theory is local, i.e. it has a local conserved stress tensor operator. As
required by reduction, we show a perfect match between superconformal blocks and the
usual conformal blocks in two dimensions lower. This also leads to a new relation between
conformal blocks across dimensions. This paper concerns the second half of the ParisiSourlas conjecture, while the first half (existence of a supersymmetric fixed point) will be
examined in a companion work.
Keywords: Conformal Field Theory, Random Systems, Supersymmetry and Duality,
Superspaces
ArXiv ePrint: 1912.01617

c The Authors.
Open Access, ⃝
Article funded by SCOAP3 .

https://doi.org/10.1007/JHEP04(2020)090

JHEP04(2020)090

Apratim Kaviraj,a,b Slava Rychkovc,b and Emilio Trevisanib

## PDF page 2

Contents
1

2 Review of the Parisi-Sourlas conjecture
2.1 From random fields to Parisi-Sourlas supersymmetry
2.1.1 Method of replicas
2.1.2 Cardy transformations
2.1.3 The emergence of Parisi-Sourlas supersymmetry
2.1.4 Relation between correlation functions
2.2 Parisi-Sourlas supersymmetry and dimensional reduction

4
4
5
5
6
7
8

3 Non-perturbative Parisi-Sourlas superconformal symmetry
3.1 Symmetries and representations
3.1.1 The symmetries along the flow
3.1.2 The symmetries of the fixed point
3.2 Super-embedding space and correlation functions
3.2.1 Superembedding space
3.2.2 Correlation functions in super-embedding space
3.2.3 OPE and conformal blocks decomposition

9
10
10
13
17
17
19
20

4 Dimensional reduction
4.1 Dimensional reduction and correlation functions
4.2 Decoupling of S1 operators
4.3 The stress tensor multiplet
4.4 OPE and conformal blocks
4.4.1 Dimensional reduction of OPE
4.4.2 Dimensional reductions of superconformal blocks
4.4.3 Relations between conformal blocks in different dimensions
4.5 Comments

21
22
25
26
28
28
29
32
34

5 Conclusions

36

A Perturbative dimensional reduction

38

B Useful relations in super(embedding)space

40

C Example: free theory

41

D Supersymmetry in the problem of critical dynamics

42

–i–

JHEP04(2020)090

1 Introduction

## PDF page 3

1

Introduction

Physical systems realized in nature often have some kind of random impurities. The presence of such impurities may change the behavior of a system. It is therefore of great
importance to understand how these changes can occur. In order to investigate this question one typically considers a statistical model and adds a disorder interaction. Physical
observables are then computed by averaging over the disorder.

In this paper we are concerned with the second case, that of quenched disorder. Here
impurities are not in thermal equilibrium. The observables (e.g. correlation functions)
are computed for a fixed disorder configuration and the disorder average is performed in
the end.
We will consider a specific class of quenched disordered theories, where a disorder field
is coupled to a local order parameter. An interesting example of this, which has a wide
range of physical applications, is the Random Field Ising Model (RFIM). One can think
of this as the regular Ising model in a random magnetic field (or in presence of random
magnetic impurities). This has the Hamiltonian
H = −J

∑

s i s j + hi s i ,

(1.1)

⟨ij⟩

with si = ±1. The hi is a random magnetic field. It is drawn from some distribution,
which we choose to be Gaussian with zero mean hi = 0, and is characterized by the
variance hi hj = Hδij .1 For a nice review on this topic see chapter 8 of [1].
For a fixed configuration of hi , one studies the thermal fluctuations of the spins at a
finite temperature, and then averages over {hi }. The presence of random field drastically
changes critical behavior, in particular the lower and upper critical dimensions are shifted
to 2 and 6. For d ≤ 2, the system is in the disordered phase ( |⟨s⟩| = 0) at any temperature.
This is dictated by the Imry-Ma criterion [2], from an estimate of the free energy cost due
to the flipping of a domain wall. For d > 2, the phase diagram is as in figure 1. There is an
ordered phase and a disordered phase separated by a second-order phase transition. From
the two fixed points shown in the figure, the IM-FP controls the usual critical behavior (no
quenched disorder), while RFIM-FP controls the critical behavior with quenched disorder
turned on. The interesting case is 2 < d < 6, when the latter fixed point is non-gaussian.
The continuous version of RFIM can be realized with a scalar theory having a φ4
interaction:
[
]
∫
1
d
2
2 2
4
d x (∂φ(x)) + m φ (x) + λφ (x) + h(x)φ(x) .
(1.2)
2
1

Averages over h will be denoted by an overline.

–1–

JHEP04(2020)090

Depending on the physical system there are two types of averaging possible. If the
impurities achieve thermal equilibrium, they have to be treated like another degree of
freedom. Hence a sum over disorder configurations should be included in the partition
function. This is called annealed disorder.

## PDF page 4

H/J
disordered
RFIM-FP

ordered
T

Figure 1. The RFIM phase diagram for d > 2.

One can study its fixed point by perturbation theory, in d = 6 − ϵ dimension. This yields
the surprising result2 that the critical exponents are exactly equal to those of the usual
Wilson-Fisher fixed point in d = 4 − ϵ.
An explanation of this is provided by a remarkable conjecture due to Parisi and Sourlas
in 1979 [4].3 The idea is that there is a relation between the IR fixed points of three
seemingly unrelated models:
• The fixed point of a random field model in d dimensions (RF-FPd ),
• The fixed point of a supersymmetric field theory without disorder in d dimensions
(SCFTd ),
• The fixed point of a model without disorder in d − 2 dimensions (CFTd−2 ),
as we show in figure 2. The link A in figure 2 is intriguing, as it relates the fixed point of a
complicated disordered model to the fixed point of a pure system (which can be described by
standard techniques). Even more surprisingly, the pure theory lives in two less dimensions,
providing an unexpected relation between different universality classes across dimensions.
The Parisi and Sourlas conjecture thus explains the link A through B followed by C.
Link B in figure 2 means that the fixed point of a random field theory should possess
an enhanced symmetry, called Parisi-Sourlas supersymmetry. Theories with this kind of
supersymmetry have very unusual features, at least to a high energy physicist. Most
notably they violate spin-statistics, as their anticommuting degrees of freedom transform
as scalars of the rotation group (i.e. fermions have no spinorial indices). In particular, they
are non-unitary. For the case of RFIM, the SUSY theory in d dimensions is given by
[
]
∫
1 a
d
2 2
4
d xdθdθ ∂ Φ(x, θ, θ)∂a Φ(x, θ, θ) + m Φ (x, θ, θ) + λΦ (x, θ, θ) ,
(1.3)
2
2

This was first noticed by Aharony, Imry and Ma in 1976 [3]. They gave a strong evidence for this
connection by showing that at any order in perturbation theory the most IR-divergent Feynman diagrams
of the random field theory can be equivalently written in terms of diagrams of a d − 2 dimensional theory.
3
Parisi and Sourlas have stated the conjecture in different terms, in particular without mentioning CFTs.
We propose a natural reformulation in modern language, which we will find useful.

–2–

JHEP04(2020)090

IM-FP

## PDF page 5

B
RF-FPdd
RF-FP

SCFTdd
SCFT

<latexit sha1_base64="xrYdnEDxhpyodcW29p5s5CQd8sk=">AAAB9XicbZDJSgNBEIZ74hbjFvXopTEIXgwzIugxKASPUcwCyRh6emqSJj0L3TVqGPIeXjwo4tV38ebb2FkOmvhDw8dfVVT17yVSaLTtbyu3tLyyupZfL2xsbm3vFHf3GjpOFYc6j2WsWh7TIEUEdRQooZUoYKEnoekNrsb15gMoLeLoDocJuCHrRSIQnKGx7jsIT5jdVk+qtVHX7xZLdtmeiC6CM4MSmanWLX51/JinIUTIJdO67dgJuhlTKLiEUaGTakgYH7AetA1GLATtZpOrR/TIOD4NYmVehHTi/p7IWKj1MPRMZ8iwr+drY/O/WjvF4MLNRJSkCBGfLgpSSTGm4wioLxRwlEMDjCthbqW8zxTjaIIqmBCc+S8vQuO07Bi+OStVLmdx5MkBOSTHxCHnpEKuSY3UCSeKPJNX8mY9Wi/Wu/Uxbc1Zs5l98kfW5w8bsJI9</latexit>

<latexit sha1_base64="zkvozmbKCiDsrcvOJg9b6bZGmY8=">AAAB+HicbZDLSsNAFIYn9VbrpVGXbgaL4KokIuiyWBCXFXuDNoTJZNIOnVyYORFryJO4caGIWx/FnW/jtM1CW38Y+PjPOZwzv5cIrsCyvo3S2vrG5lZ5u7Kzu7dfNQ8OuypOJWUdGotY9j2imOAR6wAHwfqJZCT0BOt5k+as3ntgUvE4asM0YU5IRhEPOCWgLdesDoE9QnbfvGnnbubnrlmz6tZceBXsAmqoUMs1v4Z+TNOQRUAFUWpgWwk4GZHAqWB5ZZgqlhA6ISM20BiRkCknmx+e41Pt+DiIpX4R4Ln7eyIjoVLT0NOdIYGxWq7NzP9qgxSCKyfjUZICi+hiUZAKDDGepYB9LhkFMdVAqOT6VkzHRBIKOquKDsFe/vIqdM/rtua7i1rjuoijjI7RCTpDNrpEDXSLWqiDKErRM3pFb8aT8WK8Gx+L1pJRzByhPzI+fwD1vpNF</latexit>

A

C

CFT
CFTd−22
<latexit sha1_base64="OV0hUSyHC58MqUhnwqUht+K9mDQ=">AAAB+XicbZDLSsNAFIYn9VbrLerSzWAR3FiSIuiyWBCXFXqDNoTJZNIOnVyYOSmWkDdx40IRt76JO9/GaZuFtv4w8PGfczhnfi8RXIFlfRuljc2t7Z3ybmVv/+DwyDw+6ao4lZR1aCxi2feIYoJHrAMcBOsnkpHQE6znTZrzem/KpOJx1IZZwpyQjCIecEpAW65pDoE9Qda8b+du5l/Vc9esWjVrIbwOdgFVVKjlml9DP6ZpyCKggig1sK0EnIxI4FSwvDJMFUsInZARG2iMSMiUky0uz/GFdnwcxFK/CPDC/T2RkVCpWejpzpDAWK3W5uZ/tUEKwa2T8ShJgUV0uShIBYYYz2PAPpeMgphpIFRyfSumYyIJBR1WRYdgr355Hbr1mq358brauCviKKMzdI4ukY1uUAM9oBbqIIqm6Bm9ojcjM16Md+Nj2VoyiplT9EfG5w8y3JNb</latexit>

Figure 2. The Parisi-Sourlas conjecture (our schematic formulation).

4

There are several proposals in literature to explain its failure. State of the art will be reviewed in a
companion paper [13]. Our impression from studying the vast literature is that link C is usually considered
more trustworthy than B.

–3–

JHEP04(2020)090

where Φ is a superfield and ∂ a is the derivative in superspace. This will be discussed in
detail in section 2.
Finally, link C in figure 2 is called “dimensional reduction”. It says that the correlation
functions of the SUSY theory reduce to those of a d − 2 dimensional theory, which is
identical to the disordered model but without the disorder interaction. The dimensional
reduction heavily relies on the special supersymmetry of the theory. Roughly speaking
in this supersymmetry two fermionic degrees of freedom eat two bosonic ones, effectively
reducing the dimensionality of the system. This mechanism is reminiscent to what happens
in Gaussian theories, where fermionic integrals cancel bosonic ones. As a final remark, we
point out that dimensional reduction was proposed not only for the IR fixed point, but
also all along the RG flow, thus relating quantum field theories in d and d − 2 dimensions.
In some examples, non-perturbative studies have verified some aspects of the ParisiSourlas conjecture. In particular, the critical point of branched polymers in 2 < d < 8
has been shown to undergo dimensional reduction for all integer d [5–7], confirming its
equivalence to the Lee-Yang class of fixed points in d − 2 dimensions. To be precise, these
studies verified directly the A link of the conjecture by establishing an equivalence at the
microscopic level, without considering the B and C links.
On the contrary, the conjecture was found to imply wrong results for the random field
Ising model in d = 3 and 4. E.g. according to the conjecture RFIMd=3 should be related
to Ising model at d = 1, but this does not work: the latter does not even have a phase
transition, but the former does, by the Imry-Ma criterion and by the rigorous results [8, 9].
In the 4 → 2 case there is also a discrepancy: both models have a phase transition, but
the critical exponents of RFIM in d = 4 are found to be significantly far from critical
Ising model in d = 2 [10]. On the positive side, dimensional reduction and supersymmetry
predictions for the case of 5 → 3 have been confirmed by recent numerical studies [11, 12].
There seems to be no consensus on how the conjecture works or fails, prompting us to
undertake our own study.4 Link B will be studied in the companion paper [13], where the
RG flow of the random field theories is analyzed to see if it leads to supersymmetric fixed
points. Here instead we will focus on C, giving new non-perturbative arguments in its
favor. Indeed, one gap in most justifications of C that we have seen is that they rely on a

## PDF page 6

2

Review of the Parisi-Sourlas conjecture

2.1

From random fields to Parisi-Sourlas supersymmetry

In the introduction we explained that the random field models are conjectured to have
an IR fixed point with enhanced supersymmetry [4] (see also [14, 15]). The aim of this
section is to review how this conjecture comes about. In the following we describe the main
ingredients that we need for this — the replica method and a field redefinition introduced
by Cardy.
Let us start with the theory of a single scalar field φ coupled to a random quenched
magnetic field h(x). The partition function of the model is defined by
[
]
∫
∫
1
Zh = Dφe−S[φ,h] ,
S[φ, h] = dd x (∂φ)2 + V (φ) + h(x)φ ,
(2.1)
2
where we are mostly interested in the case where the potential is V (φ) = m2 φ2 + λφ4 which
defines the random field Ising model (another interesting case is the cubic potential which
describes the random field Lee-Yang fixed point).5 The partition function Zh depends on
the shape of h(x), which is sampled from a distribution P (h) with zero mean h(x) = 0 and
no spacial correlation h(x)h(x′ ) = Hδ(x − x′ ). Observables like correlation functions are
computed by averaging over the disorder:
∫
∫
Dφ A(φ) e−S[φ,h]
⟨A(φ)⟩ = DhP (h)
.
(2.2)
Zh
Here ⟨A(φ)⟩ denotes any correlation function built out of φ’s, e.g. ⟨A(φ)⟩ = ⟨φ(x1 )φ(x2 ) · · · ⟩.
Computing this average directly is hard because of the Zh−1 factor.
5

The mass term has to be finetuned to reach the fixed point. This physically corresponds to tuning the
temperature to the transition. The finetuned valued of m2 is regulator dependent and generally nonzero
(although it would be zero in dimensional regularization).

–4–

JHEP04(2020)090

weakly coupled Lagrangian description, while the fixed points in question become strongly
coupled unless d is close to 6. Our aim will be to close this gap.
Our main tool will be to reformulate the problem axiomatically, using the modern language of conformal field theory (CFT). This language is non-perturbative, so it lends itself
naturally to our task. Using this language, we will illustrate the properties of conformal
field theories with Parisi-Sourlas supersymmetry, and check the absence of any pathological
feature. We will then explain the meaning of dimensional reduction in axiomatic CFT, and
what this implies.
The paper is organized as follows. We start by reviewing the Parisi-Sourlas conjecture
in section 2. In section 3 we develop the non-perturbative theory of Parisi-Sourlas supersymmetric fixed points using the CFT language. In section 4, we show how dimensional
reduction takes place in Parisi-Sourlas CFTs. We show that the d − 2 dimensional theory
is local, and that the superconformal blocks of the Parisi-Sourlas CFT in d dimensions are
equal to standard conformal blocks in d − 2 dimensions. As a byproduct, we find a nice
formula relating conformal blocks in d and d − 2 dimensions. We end the paper with some
concluding remarks in section 5.

## PDF page 7

2.1.1

Method of replicas

In the above φi denotes i-th replica field, where i = 1, . . . , n. Notice that the r.h.s. of
this equation reproduces the l.h.s. for any n, as long as it’s a positive integer. If we can
somehow analytically continue it to complex n, we may take the limit n → 0, for which
the denominator Zhn → 1. Assuming that the limit exists and commutes with the integral
over h, we get the following:
∫
∫
∑
⃗ A(φ1 ) e− ni=1 S[φi ,h] .
⟨A(φ)⟩ = lim Dh P (h) Dφ
(2.4)
n→0

To make further
progress, we assume that the magnetic field distribution is Gaussian,
∫ d
1
2
i.e. P (h) ∝ e− 2H d x h(x) . Doing the path integral over h, we end up with a simple
expression:
∫
⃗ A(φ1 ) e−Sn [ ⃗φ] ,
⟨A(φ)⟩ = lim Dφ
(2.5)
n→0

where the action is now free of disorder, however it contains a term which couples the n
replicas:
⎡
( n
)2 ⎤
∫
n
n
∑
∑
∑
1
1
Sn [ ⃗
φ] = dd x ⎣
(∂φi )2 +
V (φi ) − H
φi ⎦ .
(2.6)
2
2
i=1

i=1

i=1

Equations (2.5) and (2.6) define averaged correlation functions. In this formalism we can
also access more observables, like random averages of products of correlation functions:
∫
⃗
⃗ A(φ1 )B(φi ) e−Sn [φ]
⟨A(φ)⟩⟨B(φ)⟩ = lim Dφ
(i ̸= 1) .
(2.7)
n→0

To summarize, with the replica method, we obtained a prescription to compute observables in a disordered theory in terms of correlation functions of a quantum field theory
of n interacting fields. The price to pay is that we have to perform the subtle limit n → 0.
2.1.2

Cardy transformations

The action (2.6) is invariant under the permutation of the n replicas. However, in (2.5)
and (2.7), the direction φ1 is treated differently from the directions φj for j ̸= 1. This
motivates the field redefinition introduced by Cardy [17] (see also [18]), that makes manifest
only the permutation symmetry of n − 1 replicas and better captures the physics of the
n → 0 limit:
)
1(
ϕ = φ1 + ρ ,
ω = φ1 − ρ ,
χ i = φi − ρ
(i = 2, . . . , n) ,
(2.8)
2

–5–

JHEP04(2020)090

In order to circumvent this problem, it is customary to utilize the method of replicas [1].
The idea is to consider n copies of the theory, whose partition function is simply Zhn . From
the n → 0 limit we obtain the averaged free energy log Z = limn→0 n−1 (Z n − 1).
Here we will present an alternative way to implement the replica method, more suitable
to compute correlation functions [16]. For this let us insert 1 = Zhn−1 /Zhn−1 inside the hintegral in (2.2). This gives
∑
∫
∫
⃗ A(φ1 ) e− ni=1 S[φi ,h]
Dφ
⟨A(φ)⟩ = Dh P (h)
.
(2.3)
Zhn

## PDF page 8

(
)
1
where we introduced the notation ρ ≡ n−1
φ2 + · · · + φn . Note that only n − 2 field
∑
χi are actually independent since ni=2 χi = 0. When we use the transformation (2.8) in
the Lagrangian (2.6) we obtain a somewhat complicated result which can be schematically
written as
∫
[
]
⃗
Sn [φ] = dd x L0 + L1 + L2 ,
(2.9)
where L0 is defined as
n

]
H
1 ∑[
L0 ≡ ∂ω∂ϕ − ω 2 + ωV ′ (ϕ) +
(∂χi )2 + χ2i V ′′ (ϕ) .
2
2

(2.10)

All the terms suppressed by some powers of n are put in the Lagrangian L2 . All the
remaining terms are assigned in the Lagrangian L1 . It can be checked that all these L1
terms are less relevant than any term in the Lagrangian L0 (w.r.t. dimension assignments
which follow from L0 ’s kinetic term ∂ω∂ϕ− H2 ω 2 ). In particular if one considers a potential
V such that ωV ′ (ϕ), χ2i V ′′ (ϕ) are marginal, then L1 only contains irrelevant terms. For
the sake of clarity we show here a few of the possible terms contained in L1 and L2 :
{ n
}
n
∑
∑
′′′
3
2
3
L1 ⊃ V (ϕ) ×
χi ,
χi ω , ω , . . . ,
(2.11)
i=2

{

i=2

2

L2 ⊃ n (∂ϕ) , Hϕω , V (ϕ) , . . .

}

.

(2.12)

Following Cardy, in the present paper we will focus on the theory defined by L0 and we
will discard L1 and L2 terms. Naively this is legitimate, since they are either irrelevant
or vanish as n → 0. One point of the companion paper [13] will be to carefully analyze
how the discarded terms affect the RG flow of the replicated theory, and to see if there is
any subtlety.
2.1.3

The emergence of Parisi-Sourlas supersymmetry

In the following we want to show that, in the limit of zero replicas, L0 reduces to a
Lagrangian with Parisi-Sourlas supersymmetry.
Taking the limit n → 0 of the Lagrangian L0 may not look straightforward since the
dependence on n appears through the fields χi , which are n − 2 in number (n − 1 fields
subject to one constraint). However it is easy to show that in the limit of n → 0 we can
replace the n − 2 fields χi with two anticommuting scalar fields ψ and ψ:
n

1∑
n→0
χi [−∂ 2 + V ′′ (ϕ)]χi −→ ψ[−∂ 2 + V ′′ (ϕ)]ψ .
2

(2.13)

i=2

The proof of this statement consists in integrating out the fields χi and ψ, ψ in their
respective functional integrals and check that the result is the same. This manipulation is
possible because the fields enter only quadratically in the Lagrangian. The final result is
that limn→0 L0 is equivalent to the theory defined by
LSUSY = ∂ µ ω∂µ ϕ −

H 2
ω + ωV ′ (ϕ) + ∂ µ ψ∂µ ψ + ψψV ′′ (ϕ) .
2

–6–

(2.14)

JHEP04(2020)090

i=2

## PDF page 9

This is the celebrated Parisi-Sourlas Lagrangian, which surprisingly is invariant under
super-Poincaré transformations (see section 3). In order to make the supersymmetry manifest it is convenient to write the action in superspace:
[
]
∫
1 a
d
SSUSY = 2π d xdθdθ − Φ∂ ∂a Φ + V (Φ) ,
(2.15)
2

It is straightforward to check that by integrating out the variables θ, θ in SSUSY , we recover
the Lagrangian LSUSY .
To summarize, we reviewed the logical path which brings one from the disordered
theory (2.1) to the supersymmetric Parisi-Sourlas action (2.15). This suggests that the
IR fixed point of a random field model may be described by a supersymmetric theory.
However, the path was long and involved some assumptions and approximations which are
not obviously under control. These subtle issues are postponed to [13] (where we will also
review the vast literature and other approaches). In this paper we will study the SUSY
theory (2.15) in its own right.
2.1.4

Relation between correlation functions

Finally it is important to understand how the observables can be computed using the
different actions. Here, as an example, we focus on the two point function of φ of the
random field theory (2.1). Generalizations are straightforward. Using eqs. (2.5) and (2.7)
we obtain two independent physical quantities:
⟨φ(x1 )φ(x2 )⟩ = lim ⟨φ1 (x1 )φ1 (x2 )⟩n ,
n→0

⟨φ(x1 )⟩⟨φ(x2 )⟩ = lim ⟨φ1 (x1 )φi (x2 )⟩n
n→0

(i ̸= 1) ,

(2.17)
where correlators in the r.h.s. are the path integrals with the action Sn , as in the
r.h.s. of (2.5) and (2.7). We may simplify the second equation in (2.17) using the per1 ∑n
mutation symmetry of φi̸=1 , by replacing φi → n−1
i=2 φi = ρ. Further using the Cardy
ω
transformations (2.8) to rewrite φ1 = ϕ + 2 and ρ = ϕ − ω2 , we get
⟨
⟩
⟨φ(x1 )⟩⟨φ(x2 )⟩ = (ϕ(x1 ) + 12 ω(x1 ))(ϕ(x2 ) − 12 ω(x2 )) ,

(2.18)

where the r.h.s. can be now evaluated from the action SSUSY . The first equation in (2.17)
can also be treated in a similar way. The resulting equations then involve the two point
functions ⟨ϕϕ⟩, ⟨ϕω⟩ and ⟨ωω⟩. As we will explain in a moment, ⟨ωω⟩ is zero if we assume
6

If one wants to work with a general H, nice formulas will arise if one normalizes the Berezin integral as
4
dθdθ θθ = H/(4π), and the superspace metric (see below) as x2 − H
θθ. The choice of H can be thought
of as a choice of units. Note that at the level of the SUSY Lagrangian (2.14) we can change H by rescaling
the fields, ϕ̃ = α ϕ, ω̃ = ω/α, Ṽ (φ̃) = α2 V (φ), ψ, ψ = inv for some constant α.
∫

–7–

JHEP04(2020)090

where θ and θ are scalar Grassmann coordinates. For later convenience we set H = 2 and
∫
dθdθ θθ = 1/(2π).6 The super-Laplacian is defined in superspace as ∂ a ∂a = ∂ 2 + 2∂θ ∂θ .
The superfield Φ(x, θ, θ) is a function in superspace which can be expanded in components
as follows:
Φ(x, θ, θ) = ϕ(x) + θψ(x) + θψ(x) + θθω(x) .
(2.16)

## PDF page 10

supersymmetry, and then it can be dropped. Physically important quantities are the
disconnected and connected correlation functions, which then acquire particularly simple
expressions:
⟨φ(x1 )⟩⟨φ(x2 )⟩ = ⟨ϕ(x1 )ϕ(x2 )⟩ ,

⟨φ(x1 )φ(x2 )⟩−⟨φ(x1 )⟩⟨φ(x2 )⟩ = ⟨ϕ(x1 )ω(x2 )⟩ .

Now consider the two point function of the superfield Φ:
⟨
⟩
Φ(x1 , θ1 , θ1 )Φ(x2 , θ2 , θ2 )) = F [(x1 − x2 )2 − 2(θ1 − θ2 )(θ1 − θ2 )] ,

(2.19)

(2.20)

Notice that the r.h.s. does not contain the quartic Grassmann term θ1 θ1 θ2 θ2 . Via expansion (2.16), the coefficient of that term would be a two point function ⟨ω(x1 )ω(x2 )⟩ which
therefore vanishes by supersymmetry as claimed above.
To extract further consequences we set x2 = θ2 = θ2 = 0 and match with (2.16); we get
⟨
⟩
Φ(x, θ, θ)Φ(0) = F (x2 − 2θθ) = ⟨ϕ(x)ϕ(0)⟩ + θθ ⟨ϕ(x)ω(0)⟩ .
(2.22)
The two correlators in the r.h.s. are precisely the two point functions of the random field
theory (2.19). Matching the coefficients of the θ expansion, we get the following supersymmetric relation between them:
1
⟨ϕ(x)ω(0)⟩ = − ∂r ⟨ϕ(x)ϕ(0)⟩ ,
r

(2.23)

√
where r = xµ xµ . Putting together (2.19) and (2.23) one gets a supersymmetric relation
between connected and disconnected two point functions, which was checked by numerical
studies in the RFIM in d = 5 [12]. We will come back to the two point functions of generic
superfields in section 3.2.2.
2.2

Parisi-Sourlas supersymmetry and dimensional reduction

As we explained in the introduction, the Parisi-Sourlas supersymmetric theories (2.15)
undergo dimensional reduction. We now review the original argument by Parisi and
Sourlas [4].
The main claim is that the action (2.15) can be reduced to a d − 2 dimensional action
with no supersymmetry:
[
]
∫
1 2
d−2
Sred = 2π d x̂ − φ̂ ∂ φ̂ + V (φ̂ ) ,
(2.24)
2
where the potential V is the same in the three formulations (2.1), (2.15) and (2.24). The
reduction is in the sense that correlation functions of the SUSY theory SSUSY are equivalent
to the ones of Sred , when restricted to the submanifold defined by xd−1 = xd = θ = θ = 0.
For example
⟨Φ(x̂1 ) . . . Φ(x̂n )⟩ = ⟨φ̂(x̂1 ) . . . φ̂(x̂n )⟩ ,
(2.25)

–8–

JHEP04(2020)090

which by super-Poincaré invariance should be, as shown, some function of the superspace
distance. This has several consequences. First expanding in θ’s we get
⟨
⟩
Φ(x1 , θ1 , θ1 )Φ(x2 , θ2 , θ2 )) = F [(x1 − x2 )2 ] − 2(θ1 − θ2 )(θ1 − θ2 )F ′ [(x1 − x2 )2 ] . (2.21)

## PDF page 11

where x̂i ∈ Rd−2 . A similar relation should hold for correlation functions of composite
operators built out of Φ.
Parisi-Sourlas proved the above correspondence perturbatively. Their argument relied
on this simple equality between integrals:
∫
∫
d
2
d x dθ dθ f (y ) = dd−2 x̂ f (x̂2 ) ,
(2.26)

Φm → φ̂m .

(2.27)

As clear from (2.25), this map also dictates the dimensional reduction of correlation
functions.

3

Non-perturbative Parisi-Sourlas superconformal symmetry

In the previous section we reviewed how Parisi-Sourlas dimensional reduction arises. Usual
arguments rely on the form of the Lagrangian (2.15). For example the original proof
of [4] was only perturbative. Later, some non-perturbative arguments, based on somewhat
formal manipulations of the functional integral, appeared in [19] and in [20] (the latter
ones were put on a firmer mathematical ground in [21]). As a downside they all rely on the
form of the Lagrangian (2.15) and, strictly speaking, prove dimensional reductions only
for n-point functions of the fundamental field φ. A different strategy to prove dimensional
reduction was proposed by Zaboronsky [22] by means of supersymmetric localization. This
proof clarifies which is the set of observables that undergoes dimensional reduction but still
it relies on a Lagrangian formulation.
In the following we pursue a different, axiomatic approach. This is at the foundation of
the recent revival of the conformal bootstrap. In recent years a new way to compute CFT
observables was discovered and applied to many important cases (for a review see [23]).
7

To obtain (2.26) one integrates out the Grassmann coordinates:
∫
∫
∫
∫
1
1
Ωd
dd x dθ dθ f (y 2 ) = −
dd x ∂r f (r2 ) = −
dr r d−2 ∂r f (r2 ) = Ωd−2 dr r d−3 f (r2 ) .
2π
r
2π

Recall our non-standard normalization of the Berezin integral, footnote 6. In the last steps we integrated
d

2π 2
by parts to simplify the radial integral, and reduced the angular part Ωd = Γ(
d ) to Ωd−2 . For d = 2 the
2

r.h.s. of (2.26) simply becomes f (0).

–9–

JHEP04(2020)090

where y 2 = x2 − 2θθ is the norm (recall footnote 6) of the superspace vector y ∈ Rd|2
with x ∈ Rd (as we will review in the next section), while x̂2 is the norm of x̂ ∈ Rd−2 .
For (2.26) to hold, we assume d ≥ 2 and that f (r2 ) decays faster than r−(d−2) at large r.7
This argument can be extended to generic Feynman integrals thus obtaining a perturbative
proof of dimensional reduction to all orders in perturbation theory. This is reviewed in
appendix A.
As is clear from (2.15) and (2.24), the map of the two actions is quite simple. The
functional forms of the two Lagrangians are the same, with the replacement Φ → φ̂. This
suggests a simple map between the operators of the two theories, for example

## PDF page 12

3.1

Symmetries and representations

The goal of this section is to describe the symmetries and associated representation of the
IR fixed point of the Parisi-Sourlas theories. For pedagogical reasons, we first focus on
the symmetries of the theory along the RG flow. This allows us to carefully introduce the
orthosymplectic group OSp(d|2) and its representations which will play a crucial role in the
rest of the paper. In subsection 3.1.2 we proceed to analyze the Parisi-Sourlas superconformal fixed point, we illustrate the superconformal algebra and the representations under
which the CFT operators transform.
3.1.1

The symmetries along the flow

By construction, the action (2.15) enjoys super-Poincaré symmetry, namely it is invariant under supertranslations and superrotations. Let us now forget about the action and
describe the implications of the symmetries themselves.
The supertranslations act as shifts in the superspace coordinates, both in the bosonic
coordinates xµ and in the fermionic coordinates θ, θ. It is convenient to introduce the
superspace coordinate y a ≡ (xα , θ, θ) where a = 1, . . . d, θ, θ and α = 1, . . . , d (unless
explicitly said, we will consistently use lower case latin letters for superspace indices and
greek letters for Rd indices). Supertranslations, in superspace notation, take the form:
y a → y ′a = y a + ca ,

(3.1)

where ca are constants. Notice that cα are Grassmann-even (bosonic) while cθ , cθ
Grassmann-odd (fermionic). The translation generators Pa = (Pα , Pθ , Pθ ) act as derivatives ∂a ≡ ∂/∂y a in superspace. Pα are bosonic generators, while Pθ , Pθ are fermionic.
They graded-commute as
[Pa , Pb } = 0 .
(3.2)
As usual, the graded commutator [X, Y } is defined as the anticommutator [X, Y } = {X, Y }
if both X and Y are Grassmann-odd and as the commutator [X, Y } = [X, Y ] if one or
both of them are Grassmann-even.
8

There is no relation between our work and the non-rigorous attempts to use the numerical conformal
bootstrap for the problem of dimensional reduction by Hikami [24, 25].

– 10 –

JHEP04(2020)090

The idea is that observables can be fixed by requiring that the theory satisfies very general
axioms which arise from symmetries and the existence of an associative operator product
expansion (OPE) in combination with extra assumptions like unitarity. This perspective
has proven incredibly powerful to pinpoint CFTs and it suggests that this axiomatic point
of view should be taken to define the CFTs themselves. The aim of this section is to
show how a CFT with Parisi-Sourlas supersymmetry is defined in this language. The
consequences of dimensional reduction for CFTs will be addressed in section 4.8
In the following subsection 3.1 we will focus on the symmetries and representations
of Parisi-Sourlas theories. In subsection 3.2 we will describe how to make the symmetries
more manifest by means of an auxiliary embedding space. In this formalism it will be easy
to describe correlation functions of the superconformal theory, as shown in subsection 3.2.2.
The OPE and conformal blocks decomposition are finally discussed in subsection 3.2.3.

## PDF page 13

The superrotations form the orthosymplectic supergroup OSp(d|2). This group will
play a very important role in characterizing the little group of the superconformal field
theory, thus defining the transformations of superprimary operators. For this reason in the
following we carefully explain its action, algebra and representations. The orthosymplectic
supergroup OSp(d|2) is the group of super-linear transformations y a → y ′a = Rab y b that
preserves the norm (recall that we set H = 2)
y 2 ≡ y a ya = y a gab y b = x2 − 2θθ .

(3.3)

(
gab ≡

Id 0
0 J2

d

)
,

⏞ ⏟⏟ ⏞
Id ≡ diag(1, 1, . . . , 1) ,

(
J2 ≡

0 −1
1 0

)
.

(3.4)

The elements of the group OSp(d|2) can be realized as (d + 2) × (d + 2) matrices Ra b
which satisfy the following relation:
Ra b Rc d gac = gbd .
The matrices forming the supergroup can be written in block form as
(
)
α Rα
R
q
β
Ra b =
,
Rp β Rp q

(3.5)

(3.6)

where we split indices a = (α, p), b = (β, q) and p, q ∈ θ, θ run over the Grassmann
directions. The coefficients Rα β and Rp q are even elements of a Grassmann algebra, while
Rα q and Rp β are odd elements of a Grassmann algebra.9
It is convenient to introduce the Lie algebra of OSp(d|2), denoted as osp(d|2) [27, 28].
We name the generators of superrotations as M ab , where a, b = 1, . . . , d, θ, θ. They are
bosonic if both a and b have the same grading and fermionic otherwise. M ab are graded
antisymmetric, meaning that M ab = −(−1)[a][b] M ba , where [a] = 0 if for bosonic coordinates and [a] = 1 for fermionic ones (notice in particular that generators with two equal
Grassmann indices M θθ and M θ θ are non-zero, consistently with this equation). They
satisfy the following commutation relations:
[M ab , M cd } = g cb M ad −(−1)[a][b] g ca M bd −(−1)[c][d] g db M ac +(−1)[a][b]+[c][d] g da M bc .

(3.7)

So far we encountered the generators Pa which are in a vector representation of OSp(d|2)
and M ab which are in the graded antisymmetric. In the following it will be crucial to have
under control more generic finite dimensional representations of the superrotations. To
9

We can consider a Grassmann algebra generated by an infinite set of anticommuting Grassmann variables θ1 , θ2 , . . . However this description is redundant. It suffices to consider 2d independent Grasmann
variables to generate all the group elements. These are in one-to-one correspondence with the odd generators of the OSp(d|2) algebra (see e.g. [26]).

– 11 –

JHEP04(2020)090

The orthosymplectic metric gab is an invariant tensor of the group. It can be easily expressed in a block diagonal form, in terms of the d-dimensional flat metric and the symplectic metric:

## PDF page 14

this end we now classify tensor representations of OSp(d|2). They are associated to graded
Young tableaux which take the following form [29]:
···

···

..
.

..
.

..
.

···

···

···

···

}

.

···

..
.

..

···

[ d2 ]

,

(3.8)

..
.

• Indices along the rows are graded symmetrized,
• Indices along the columns are graded antisymmetrized,
• All the super-traces are removed.
The idea can be illustrated with the following examples of tensors with two indices respectively belonging to the graded symmetric and the graded antisymmetric representations:
a

b
a
b

)
1 ( ab
g ab
t + (−1)[a][b] tba − tc c
,
2
d−2
)
1(
tab = tab − (−1)[a][b] tba .
2
tab =

(3.9)
(3.10)

As already mentioned, the generators M ab belong to the second type (3.10). The action of
the generators of superrotations on a tensor with ℓ indices takes the following form:
ab

[M , t

a1 ...aℓ

}=

ℓ
∑

(k)

σ{ai } [Σab ]ak c tc a1 ...ak−1 ak+1 ...aℓ ,

[Σab ]dc ≡ g db δca − (−1)[a][b] g da δcb ,

k=1

(3.11)
(k)
where σ{ai } is the sign acquired by the tensor ta1 ...aℓ after commuting ak to the left of a1 ,
(k)
namely ta1 ...aℓ = σ{ai } tak a1 ...ak−1 ak+1 ...aℓ . For example M ab rotates the index of P c giving

the following commutation relation:
[M ab , P c } = g cb P a − (−1)[a][b] g ca P b .

(3.12)

In the following it will be often convenient to use an index-free formalism. This can be
achieved by contracting tensors with polarization vectors of the form
wa ≡ (z α , ζ, ζ) ,

– 12 –

(3.13)

JHEP04(2020)090

where the i-th row has length li and li ≥ li+1 . The first [ d2 ] rows can be arbitrarily long
and they are roughly speaking associated to the SO(d) part of the group. Similarly the
first column may contain an arbitrary number of boxes, and it is related to Sp(2).
The graded Young tableaux is a straightforward generalization of the usual Young
tableaux, with the following rules:

## PDF page 15

where z α is a Grassmann even d-dimensional vector while ζ, ζ are Grassmann odd variables.
For example, a graded symmetric tensor of spin ℓ is encoded by the following index-free
notation:
t(w) ≡ waℓ · · · wa1 ta1 ...aℓ .
(3.14)
This is consistent since the polarization vectors graded-commute between themselves. A
further simplification is to encode the super-tracelessness of the tensor by using polarization
vectors which are null: 0 = wa wa = z 2 − 2ζζ. The original tensor components can be
extracted from t(w) by taking derivatives:
1
ℓ!( d2 − 2)ℓ

a1
aℓ
Dw
· · · Dw
t(w) ,

a is an appropriate differential operator:
where Dw
(
)
d
1
a
a
2
Dw =
− 2 + w · ∂w ∂w
− w a ∂w
.
2
2

(3.15)

(3.16)

Here the dot-product and the square are defined to build scalars of OSp(d|2), e.g. w1 · w2 ≡
w1a w2 a for some vectors w1 , w2 . Of course to take derivatives we have to extend t(w) away
from the null cone wa wa = 0, but the point of this construction is that the result does
not depend on how the extension is taken and gives back the original graded symmetric,
super-traceless tensor. This technology matches the one used in [30] for SO(d) tensors,
besides that (3.15) and (3.16) depend on a shifted value of the dimension d → d − 2. More
general representations are handled by generalizing the strategy of [31–33]: we contract the
mixed symmetric tensors with a sequence of polarization vectors, where the indices of the
i-th graded symmetric row of the Young tableau are contracted with polarization vectors
wi . We further ask for wi · wj = 0 to encode tracelessness. To undo the contractions and
a and contract the resulting indices
recover the original components, we apply derivatives ∂w
i
with opportune projectors. Interestingly the projectors for OSp(d|2) take the same form
as the ones of SO(d) [32] after the shift d → d − 2 (one example of this is visible in (3.9)).
Finally, let us mention that the finite dimensional representations of OSp(d|2) can
be decomposed in terms of representations of O(d) × Sp(2). The standard technique is
explained in [34, 35].
3.1.2

The symmetries of the fixed point

In this section we focus on the symmetries of fixed point of the RG flow of the action (2.15).
This is, by definition, invariant under superdilations. We will also assume that, along with
superdilations, it is invariant under special superconformal transformations. Superconformal transformations are defined by analogy with conformal transformations as being
locally given as a composition of a superrotation and a superdilation. The assumption
of superconformal invariance can be justified by the usual arguments involving a traceless
stress tensor, as for the usual scale vs conformal invariance story, and with usual caveats.
We will see this later in this section. Superconformal invariance of free massless theory
(i.e. V = 0 in (2.15)) can be checked explicitly [36].

– 13 –

JHEP04(2020)090

ta1 ...aℓ =

## PDF page 16

The generators of the transformations form the Parisi-Sourlas superconformal algebra,
which is denoted by osp(d + 1, 1|2). In this section we show some features of this algebra
and its representations.10
The algebra osp(d + 1, 1|2) consists of the generators of superrotations M ab , supertranslations P a , superdilations D and special superconformal transformations K a , which
correspond to the following superspace vector fields:
P a = ∂a ,

M ab = y a ∂ b −(−1)[a][b] y b ∂ a ,

D = −y a ∂a ,

K a = 2y a y b ∂b −y b yb ∂ a .

(3.17)

Their graded algebra takes the form:

[D, K a } = −K a ,
a

b

ba

(3.18)

[K , P } = 2g D − 2M

ab

,

where g is the orthosymplectic metric (3.4). Here we omitted the commutator of superrotation generators which already appeared in (3.7) and (3.12) (the commutator of M ab
and K a takes the same form as (3.12), since K a is also an OSp(d|2) vector). All the other
commutators vanish.
The graded-commutators (3.18) describe a ladder algebra with raising and lowering
operators P a and K a . Superfields transform in the representation of the little group
OSp(d|2) × U(1) generated by the superrotations M ab and superdilations D. A superprimary operator diagonalizes the superdilation operator and is annihilated by K a :
[K a , O(0)} = 0 ,

[D, O(0)} = ∆O(x) .

(3.19)

Since the condition for superprimaries includes the operator to be annihilated by the two
Grassmann charges K θ , K θ , it is more restrictive that the condition for SO(d + 1, 1) primaries which are only annihilated by K α . Superrotations act on the operator O(0) by
rotating its OSp(d|2) indices according to (3.11). Finally P a creates superdescendants.
So far we explained how to organize the operators of the theory in terms of superfields
which transform naturally under the little group. Since every superconformal theory is
also conformal, it is interesting to know how the spectrum splits in conformal multiplets of
SO(d + 1, 1). Let us show how this works for an operator O with super-dimension ∆ and
transforming in a graded-commuting representation of spin ℓ of OSp(d|2). First we expand
the superfield in θ, θ:
a1 ...aℓ
Oa1 ...aℓ (x, θ, θ) = O0a1 ...aℓ (x) +θ Oθa1 ...aℓ (x) +θ Oθa1 ...aℓ (x) +θθ Oθθ
(x) .
⏟
⏞⏞
⏟ ⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
∆

∆

∆+1

∆+1

(3.20)

∆+2

The four coefficients of the θ, θ polynomial, which we dubbed O0 , Oθ , Oθ , Oθθ , have the
same spin under OSp(d|2), but they have shifted conformal dimensions, according to the
10

There is little literature about representations of this superconformal algebra, which violates spin statistics and thus cannot occur in unitary theories of interest to high energy physicists. The only relevant paper
known to us is [36], which however treats explicitly only scalar superprimaries, and does not relate superconformal invariance to the super-stress tensor.

– 14 –

JHEP04(2020)090

[D, P a } = P a ,

## PDF page 17

mnemonic dimension rule that [θ] = [θ] = −1. The indices ai are naturally organized
in finite irreducible representations of OSp(d|2). We can further decide to exhibit the
rotation symmetry of the CFTd by reorganizing the OSp(d|2) representations in terms of
the SO(d) ones. E.g. the zero component of a vector Oa can be written as a collection
of one SO(d) vector (boson) and two scalars (fermions) as follows O0a = (O0α , O0θ , O0θ ). A
similar decomposition holds for Oθa , Oθa except for the opposite statistics of vector and
scalar components. Each of the four constituents OIa1 ...aℓ (I = 0, θ, θ, θθ) of a general
graded-symmetric OSp(d|2) spin ℓ ≥ 2 tensor superprimary multiplet would thus give rise
µ ...µ

θ

µ ...µ

θ

µ ...µ

θθ

0 = ⟨Ob |Kb P a |Oa ⟩ = ⟨Ob |[Kb , P a }|Oa ⟩ = 2(∆ − d + 3)⟨Oa |Oa ⟩ .

(3.21)

Here we defined a conjugate state by |O⟩† ≡ ⟨O| ≡ limy→0 |y|−2∆ ⟨0|O(y a /y 2 ) (when an
operator has indices they have to be contracted with reflection matrices g ba − 2y a y b /y 2 ).
Since the conjugation is defined by superspace inversion, we can apply the usual logic and
obtain that Pa† = Ka — indeed the generator of special superconfrormal transformations is
obtained from the successive application of inversion-translation-inversion in superspace.
We continue our discussion by showing how short CFTd multiplets are embedded into
the short superconformal multiplets of the Parisi-Sourlas CFT. Let us exemplify how
this works for a spin-two superprimary T ab (generalizations to other short multiplets are
straightforward), which satisfies the conservation equation:
∂ a Tab = 0 .

(3.22)

We recall that graded symmetry and the super-tracelessness respectively imply
Tab = (−1)[a][b] Tba and g ab Tab = 0. Furthermore, as we showed above, conservation (3.22)
fixes the dimension of T ab as d − 2. We refer to T ab as the super-stress tensor of the
Parisi-Sourlas CFT, associated with the supertranslation symmetry. Of course since every
Parisi-Sourlas CFT is also a usual CFTd , as such it should contain the usual stress tensor
T αβ primary, of dimension d. It would be natural to guess that T αβ is contained in the T ab
supermultiplet, and indeed that’s what happens. Expanding Tab (x, θ) as in (3.20) we get
T ab (x, θ, θ) = T0ab (x) +θ Tθab (x) +θ Tθab (x) +θθ Tθθab (x) .
⏟
⏞⏞
⏟ ⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
⏟ ⏞⏞ ⏟
d−2

d−2

d−1

11

d−1

(3.23)

d

Since we are assuming graded symmetry, if we set two indices to the same Grassmann value we obtain
µ ...µ
θθ
zero, e.g. OI 1 ℓ−2 = 0.

– 15 –

JHEP04(2020)090

to four conformal primaries OIµ1 ...µℓ , OI 1 ℓ−1 , OI 1 ℓ−1 and OI 1 ℓ−2 of decreasing
SO(d) spins ℓ, ℓ − 1, ℓ − 1 and ℓ − 2 and of accordingly alternating statistics.11
Let us now discuss some features of short superconformal multiplets. To begin, we
shall see how shortening conditions are used to fix the scaling dimension of the supermultiplet. As a first example we consider the free scalar superprimary |O⟩ ≡ O(y = 0)|0⟩,
defined by P a Pa |O⟩ = 0. By asking that its norm vanishes and using the commutation
relations (3.18), we discover that the dimension of O is fixed as d/2 − 2. We can similarly
consider a conserved superprimary operator Oa1 ...aℓ , in the graded symmetric representation of OSp(d|2). We require that the norm of P a |Oaa2 ...aℓ ⟩ vanishes. This then fixes its
superconformal dimensions to ∆ = ℓ + d − 4. As an example, when ℓ = 1, we have

## PDF page 18

By dimensionality one can guess that the usual d-dimensional stress tensor T αβ = Tθθαβ ,
the spin-two part of the highest-dimension constituent Tθθab . As a check let us verify that
equation (3.22) implies the conservation of Tθθαβ . In fact by plugging (3.23) in (3.22) and
taking the θθ coefficient, one gets precisely
∂α Tθθαβ (x) = 0 ,

(3.24)

dd xdθdθ ∂ a Tab (y)O(0) = ∂b O(0) ,

(3.25)

V

where the l.h.s. is an integral over a region V ⊂ Rd|2 that contains the point y = 0 and O is
local operator which, for simplicity, we consider to be a scalar.13 By using Stokes’ theorem
(see e.g. [37]) the integral in (3.25) can be written as a surface integral on the boundary ∂V
of the region V . Because of the conservation of the stress tensor, the l.h.s. of (3.25) defines
a topological surface operator, which does not depend on the shape of the surface ∂V (as
long as other operator insertions are not crossed). We can e.g. consider V ∈ Rd|2 to be a
superball of radius ϱ, its boundary a supersphere. Since ϱ can be taken arbitrarily small, we
expect the r.h.s. to be written as a local operator inserted at the origin. Moreover, since the
super-stress tensor generates supertranslations, the r.h.s. is fixed in terms of a superspace
derivative acting on O. Eq. (3.25) also fixes the normalization of the super-stress tensor.
Finally let us come back to the assumption of superconformal invariance. In usual
CFTs, conformal invariance descends from the condition of tracelessness of the stress tensor.
Dilation invariance of the fixed point imposes that the stress tensor is either traceless or it
satisfies T µµ = ∂ µ Vµ for some vector field Vµ called “virial current”. Conformal invariance
follows from scale invariance if the virial current is absent (or it is a descendant of some spintwo operator Wµρ , namely Vµ = ∂ ρ Wµρ ) [38]. In practice we are trading the assumption
of conformal invariance with the assumption of the absence of a virial current. The latter
is clearly more satisfying since we do not expect to have, in a generic interacting CFT,
a non-conserved vector operator with dimension d − 1. This expectation should hold in
unitary and non-unitary theories alike.
The same kind of logic can be adopted in our supersymmetric setup. Indeed the
absence of a super-virial current V a — non-conserved and with superdimension (d − 3)
12

Grassmann derivatives like ∂θ T θβ cannot contribute to this equation because they can never produce
a θθ term.
13
The superspace topology is defined by its reduced bosonic topology. The mnemonic rule being that
Grassmann variables are much smaller than the bosonic ones, since they square to zero. E.g. the interior
of a superball is identified by the interior of the ball obtained by setting its Grassmann coordinates to zero.
See [37] for a review on topology and integration over supermanifolds.

– 16 –

JHEP04(2020)090

where α, β run from 1 to d.12 Since Tθθαβ is a conserved spin-two tensor of SO(d), with
conformal dimension d, we conclude that it should correspond to the d-dimensional stress
tensor. It is instructive to explicitly check this statement in free theory as we show in
appendix C.
The super stress tensor is a very important operator since many properties of a CFT
descend from its existence. We shall define locality of the Parisi-Sourlas theory by the
following equation:
∫

## PDF page 19

— and the presence of superdilations are enough to impose that the super-stress tensor is
traceless and therefore to establish superconformal symmetry.14
3.2

Super-embedding space and correlation functions

3.2.1

Superembedding space

The Parisi-Sourlas CFT is invariant under the orthosymplectic group OSp(d+1, 1|2), which
does not act linearly in superspace Rd|2 . The idea of the super-embedding formalism is to
uplift the theory to the space R1,d+1|2 , where the group acts linearly. It is then possible to
go back to the usual superspace Rd|2 by using a simple projection.
Given a point P M = (P 0 , P µ , P d+1 , θ, θ) in the super-embedding space R1,d+1|2 , its
norm is defined as
P 2 ≡ P M PM ≡ PM g M N PN = −(P 0 )2 + (P µ )2 + (P d+1 )2 + 2 θθ ,

(3.26)

where the metric g is a block diagonal matrix build in terms of two pieces: the flat metric
I1,d+1 of R1,d+1 and the symplectic metric J2 of Sp(2):
(
g AB =

I1,d+1 0
0 J2

)

(
,

where

I1,d+1 = diag(−1, 1, . . . , 1) ,
⏟
⏞⏞
⏟

J2 =

0 −1
1 0

)
.

(3.27)

d+2

In order to get rid of the two extra dimensions we consider only the points P M which
belong to the projective null cone P 2 = 0 with P ∼ λP . To get back a result parametrized
by the coordinates (x, θ, θ) in physical space, we will restrict each point P A to lie in the
super-Poincaré (sP) section:
P

A∣

(

∣
sP

=

1 + x2 + 2θθ µ 1 − x2 − 2θθ
,x ,
, θ, θ
2
2

)
.

(3.28)

Scalar primary superfields extended to the projective null cone satisfy the following homogeneity condition:
O(λP ) = λ−∆ O(P ) ,
(3.29)
14

Tracelessness of the super-stress tensor is equivalent to the invariance under local rescaling of the
superspace metric (near flat space). The latter is sufficient to reconstruct all the superconformal Killing
vectors including the ones associated to special superconformal transformations. As in usual CFTs, one
can then further define additional topological surface operators integrating Tab (y) of (3.25) against the
superconformal Killing vectors ϵb (y), thus recovering all generators of (3.17).

– 17 –

JHEP04(2020)090

In this section we analyze the correlation functions of the Parisi-Sourlas CFT. We first introduce the super-embedding space formalism, which generalizes the usual embedding space
formalisms of [30]. This simplifies the action of conformal transformations and trivializes
the problem of finding conformal invariant combinations to build correlation functions. We
then apply this technique to correlation functions and give a few examples of how they are
constrained by supersymmetry. Finally we focus on the OPE and on how this can be used
to decompose four point functions in superconformal blocks.

## PDF page 20

for any λ ∈ R. We can further uplift operators that transform as OSp(d|2) tensors, by
imposing (3.29) and by allowing their indices to take values A = 0, . . . , d + 1, θ, θ. To get a
description which is not redundant, the operators are required to satisfy the transversality
condition PA1 OA1 A2 ...Aℓ (P ) = 0. We also have a condition that “pure gauge” tensors
proportional to PAi project to zero. To deal with these constraints, it is convenient to
contract the tensor indices with super-embedding space polarization vectors. For example
for a spin ℓ graded symmetric superfield we define
O(P, Z) ≡ OA1 ...Aℓ (P ) ZAℓ · · · ZA1 ,

(3.30)

LAB ≡ PA ∂PB − (−1)[A][B] PB ∂PA .

(3.32)

LAB packages together supertranslation, superrotations, superdilations and special superconformal transformations, while making the OSp(d + 1, 1|2) action linear, and the invariance manifest. Indeed it is easy to see that LAB satisfies the osp(d + 1, 1|2) algebra. In
this notation the quadratic superconformal Casimir takes a very compact form:
1 AD BC
g g LAB LCD .
(3.33)
2
The eigenvalue of the Casimir on any operator within a superconformal multiplet labelled
by the super-dimension ∆ and the OSp(d|2) spin ℓ is
(
)
(
)
d|2
c∆,ℓ = ∆ ∆ − (d − 2) + ℓ ℓ + (d − 2) − 2 .
(3.34)
This can be obtained by a direct computation as we explain in section 4.4. Notice that
this eigenvalue exactly equals the Casimir eigenvalue for a spin ℓ, dimension ∆ primary in
a non-supersymmetric CFT living in d − 2 dimensions. This property is indeed true also
for generic representations. This fact will be crucial for the dimensional reduction to work.

– 18 –

JHEP04(2020)090

where polarization vectors are chosen as Z M = (Z 0 , z µ , Z d+1 , ζ, ζ) and ζ, ζ are Grassmann
odd coordinates while Z 0 , z µ , Z d+1 are Grassmann even and z µ is a d-dimensional vector.
The transversality condition and the super-tracelessness conditions can be encoded by
choosing polarization vectors that respectively satisfy P · Z = 0 and Z 2 = 0. When we
restrict coordinates to the super-Poincaré section, the polarization vectors are projected to
vectors tangent to this section, as follows:
∣
(
)
Z M ∣sP = (x · z + ζθ + ζθ), z µ , −(x · z + ζθ + ζθ), ζ, ζ .
(3.31)
∣
Notice that the condition Z 2 = 0 is projected to Z 2 ∣sP = z 2 − 2ζζ = 0 in physical space,
which indeed encodes the super-tracelessness condition of OSp(d|2) tensors as explained
below (3.14). One can also consider more generic representations for the superfields O,
analogously to what was done in [31] for the usual conformal group. Tensors of OSp(d|2) can
be associated to Young tableaux of the form (3.8). One can contract the indices of each row
with a polarization vector Z (i) such that P · Z (i) = 0. It is possible to choose Z (i) · Z (j) = 0.
Finally one can project them into the super-Poincaré section in terms of physical space
polarization vectors z (i) , ζ (i) , ζ (i) by a straightforward generalization of (3.31).
In super-embedding space, the generators of infinitesimal orthosymplectic transformations LAB take a particularly simple form:

## PDF page 21

3.2.2

Correlation functions in super-embedding space

Using the super-embedding formalism it is easy to classify superconformal invariants which
in turn can be used to write correlation functions. In the following we show how to use this
formalism in some simple examples. It will be clear that all applications are straightforward
generalizations of what happens in usual CFTs as detailed in [30].
Since OSp(d + 1, 1|2) transformations act as linear transformations of the points P A ,
conformal invariants are just scalar products Pi · Pj . For example a two point function of
a scalar operator O with superconformal dimension ∆ can be written as
1
(P12 )∆

,

(3.35)

where the scaling is fixed by the requirement (3.29) and we defined Pij ≡ −2Pi · Pj where
−2 is a convenient normalization. This restricts to the super-Poincaré section as
∣
2
−2Pi · Pj ∣sP = yij
= (xij )2 − 2θij θij ,
(3.36)
where θij ≡ θi − θj , θij ≡ θi − θj . Thus restricting (3.35) to the Poincaré section, we get
the two point function in superspace: By further expanding the two point function as a
polynomial in the Grassmann coordinates we obtain
∣
⟨O(P1 )O(P2 )⟩∣sP =

1
.
(x12 − 2θ12 θ12 )2∆

(3.37)

This is similar to eq. (2.20) from the previous section for the fundamental superfield Φ
of the Parisi-Sourlas Lagrangian. In particular we extract correlation functions between
constituents of the θ expansion of O:
⟨O0 (x1 )O0 (x2 )⟩ =

1
,
(x12 )2∆

⟨O0 (x1 )Oθθ (x2 )⟩ =

2∆
,
(xij )2(∆+1)

(3.38)

in agreement with (2.23), while the highest dimension constituent Oθθ has zero two point
function by the argument for the vanishing ⟨ωω⟩ given there:15
⟨Oθθ (x1 )Oθθ (x2 )⟩ = 0 .

(3.39)

It is important to stress that one should not consider ω or more generally any Oθθ as
null states which can be modded out from the theory, in fact their correlation function
with other operators may be non-zero, as is evidenced already by the non-zero two point
function ⟨ω(x)ϕ(y)⟩ ̸= 0.
We can also consider two point functions of operators O transforming in non-trivial
representation of OSp(d|2). For example if O is a graded symmetric superprimary with
super-dimension ∆ and spin ℓ, we have
⟨O(P1 , Z1 )O(P2 , Z2 ) =
15

(H12 )ℓ
,
(P12 )∆

(3.40)

In fact this is a generic property of any n-point function: the highest component, proportional to
θ1 θ1 · · · θn θn , has to vanish. This is a simple consequence of supertranslation invariance, which can be used
to translate any θi to zero.

– 19 –

JHEP04(2020)090

⟨O(P1 )O(P2 )⟩ =

## PDF page 22

where the denominator is fixed by (3.29) and H12 is the unique conformal invariant which
does not scale in Pi and can be built out of null and transverse polarization vectors Zi
(see [30]):
(Zi · Zj )(Pi · Pj ) − (Zi · Pj )(Zi · Pj )
Hij ≡
.
(3.41)
Pi · Pj

ℓ
λ123 V3,12

⟨O1 (P1 )O2 (P2 )O3 (P3 , Z3 )⟩ =
(P12 )

∆1 +∆2 −∆3
2

(P23 )

∆2 +∆3 −∆1
2

(P13 )

∆3 +∆1 −∆2
2

,

(3.42)

where λ123 is the associated OPE coefficient. The powers of Pij are fixed by the requirement (3.29). The term V3,12 does not scale in Pi and it is the only conformal invariant
which can be built out of the null and transverse polarization vector Z3 [30]:
Vi,jk ≡

(Zi · Pj )(Pi · Pk ) − (Zi · Pk )(Pi · Pj )
√
.
(Pj · Pk )(Pj · Pi )(Pk · Pi )

(3.43)

More complicated cases are again handled by following e.g. [33].
Let us then consider a four point function of scalar superprimaries Oi with dimensions
∆i :
(
⟨O1 (P1 )O2 (P2 )O3 (P3 )O4 (P4 )⟩ = K(Pi )f (U, V ) ,

K(Pi ) ≡

P24
P14

) ∆1 −∆2 (

(P12 )

2

∆1 +∆2
2

P14
P13

) ∆3 −∆4

(P34 )

2

∆3 +∆4
2

,

(3.44)
where K(Pi ) is a kinematic function that takes into account the correct scaling required
by (3.29). The result is fixed up to a function f of the two super-cross-ratios which are
scaleless in Pi :
P14 P23
P12 P34
U≡
,
V ≡
.
(3.45)
P13 P24
P13 P24
Finally we can apply the same reasoning to a four point function of spinning operators
Oi (Pi , Zi ). In super-embedding space, the conformal invariants are the same as the ones
introduced by [30], namely one needs combinations Pi ·Pj and Pi ·Zj which scale opportunely
in the Pi , Zi and which are transverse.
The reader used to the formalism introduced in [30], may have recognized that the
super-embedding formalism is a straightforward generalization. So we avoid further details.
3.2.3

OPE and conformal blocks decomposition

In this section we exemplify how the OPE works in a Parisi-Sourlas CFT. We then apply
the OPE to a four point function to obtain its superconformal block decomposition.

– 20 –

JHEP04(2020)090

More complicated representations can be taken into account generalizing the formalism
of [31–33].
Let us see how to apply this technology to three point functions. E.g. take two scalar
operators O1 , O2 with dimensions ∆1 , ∆2 and a spin ℓ operator O3 dimensions ∆3 . Their
three point function is written as

## PDF page 23

The OPE can be conveniently expressed in superspace. For simplicity we focus on the
OPE between two scalar superfields O1 , O2 with dimensions ∆1 , ∆2 :
∑
λ12O
O1 (y)O2 (0) =
[yaℓ · · · ya1 Oa1 ...aℓ (0) + superdesc.] ,
(3.46)
∆
|y| 1 +∆2 −∆+ℓ
∆,ℓ

∆,ℓ

where, as in (3.46), the sum runs over superprimaries O labelled by ∆, ℓ and λO34 are the
OPE coefficients of the right channel 34. Each conformal block resums the contribution of
the primary O and all its descendants into a single function of the super-cross-ratios (3.45).
Even if the superblocks can be defined by applying the left and right OPEs to a two point
function, there are more convenient techniques to compute them. One of the most efficient
ones is the super-analogue of [39] — to find them via the eigenfunctions of a second-order
partial differential operator, the super-Casimir C:
d|2

d|2

d|2

d|2

d|2

G∆,ℓ (Pi ) ≡ K(Pi )g∆,ℓ (U, V ) .

C G∆,ℓ (Pi ) = c∆,ℓ G∆,ℓ (Pi ) ,

(3.48)

The eigenfunctions G are sometimes called conformal partial wave and are related to the
d|2
conformal blocks g by the kinematic factor (3.44). The eigenvalue c∆,ℓ of the Casimir
equation is given by (3.34) and the super-Casimir differential operator C takes the form:
1
(3.49)
C ≡ g AD g BC (L1 + L2 )AB (L1 + L2 )CD ,
2
where Li are the generators of rotations (3.32) acting on points Pi . This discussion can be
easily extended to four point functions of non-scalar operators by considering generators
of the rotations Li which also act on the polarization vectors of the external operators.
More generic exchanged operators can be taken into account by considering the opportune
eigenvalues. In section 4.4 we will show how to compute the superconformal blocks in
terms of conformal blocks of a non-supersymmetric CFT.

4

Dimensional reduction

In this section we want to show how dimensional reduction [4, 19–22] works in the context
of axiomatic CFTs. In particular we want to clarify how the Parisi-Sourlas CFT is related
to a CFT that lives in d − 2 dimensions.

– 21 –

JHEP04(2020)090

where the sum runs over the possible graded symmetric tensor superprimaries O with
dimension ∆ and OSp(d|2)-spin ℓ. Indeed since O1 , O2 are scalars, the indices of the exchanged operators can only be contracted with the superspace points y a , which graded commute between themselves, so only graded symmetric primaries contribute. The ‘superdesc.’
in (3.46) denotes the contribution of the superdescendants, i.e. superspace derivatives (∂ a
and higher order) of the superprimaries. As usual, these terms are completely fixed by
superconformal invariance. Quantities not fixed by the symmetry are the dimensions of
fields and the coefficients λ12O , which already appeared in the three point function (3.42).
By taking the OPE of operators 12 and 34 inside the four point function (3.44), we
can express the function f as a sum over superconformal blocks g d|2 :
∑
d|2
f (U, V ) =
λ12O λO34 g∆,ℓ (U, V ) ,
(3.47)

## PDF page 24

In the next section we define what we mean by dimensional reduction. Then we
explain that the locality of the Parisi-Sourlas CFT implies the locality of the theory in
d − 2. We further demonstrate how dimensional reduction works by showing that the
superconformal blocks of the Parisi-Sourlas CFT match the conformal blocks of a d − 2
dimensional CFT. Finally we describe how the equality of blocks implies a neat relation
between usual conformal blocks in d and d − 2 dimensions.
4.1

Dimensional reduction and correlation functions

– 22 –

JHEP04(2020)090

The basic idea of dimensional reduction is that certain correlation functions of the ParisiSourlas CFT restricted to the subspace Rd−2 ⊂ Rd become correlation functions of a d − 2
dimensional CFT without supersymmetry. Of course any CFT restricted to a subspace
defines a set of conformal correlators living in that subspace. This follows simply from the
fact that d-dimensional conformal group restricts to the conformal group of the subspace.
What is unusual and non-trivial about the Parisi-Sourlas dimensional reduction is that,
unlike a simple restriction, it produces a local theory. Before we explain this, let us recall
some basic features of usual restrictions.
A “restriction” is what happens to a CFTd when we restrict all its correlators to
a linear subspace, or hyperplane, Rp ⊂ Rd (which is sometimes called “trivial defect”).
By selecting this hyperplane we break the symmetry of the theory from SO(d + 1, 1) to
SO(p + 1, 1) × SO(d − p). The group SO(p + 1, 1) realizes conformal symmetry on Rp , while
SO(d − p) is understood as a global symmetry under which the CFTp operators transform.
The resulting CFTp however is non-local, meaning that it does not contain a conserved
SO(p)-spin two operator with dimension p which could be identified as its stress tensor.
In fact the restriction of the CFTd stress tensor T µν does produce in p-dimension a spin-2
operator Trαβ = (T αβ − trace) if we select α, β = 1, . . . p, as well as SO(p) vectors and
scalars. However the Trαβ does not have the correct scaling dimension, which is still d,
nor is it conserved. These facts are of course related because conserved spin-2 primary
in d − 2 dimensions should have dimension d − 2. In fact the stress tensor conservation
in d dimension involves derivatives both tangent and orthogonal to Rp and thus does not
descend to conservation of Trαβ . Physically this is clear: the energy in this setup is not
conserved on Rp because it can escape in the orthogonal directions.
Besides the absence of the stress tensor, the correlation functions of CFT p are well
defined and satisfy the other CFT axioms. In particular, the associative OPE of the CFT d
induces an associative OPE in the restricted theory. As a consequence of this, all four
point functions of the CFTp can be expanded in p-dimensional conformal blocks (CBp ).
It follows that any CFTd correlator, which is expandable in CBd , when restricted can
also be expanded in CBp . The way these two facts are compatible is that every CBd
can be expressed as a linear combination of CBp [40]. The linear combination is infinite,
because an SO(d + 1, 1) conformal multiplet decomposes into a direct sum of infinitely
many SO(p + 1, 1) conformal multiplets.
We now come back to our specific problem of Parisi-Sourlas dimensional reduction.
This will be understood as a special kind of restriction which will only apply to a subsector
of the full Parisi-Sourlas theory. First of all, the restriction will be from the superspace Rd|2

## PDF page 25

to a bosonic Rd−2 subspace defined by setting two bosonic coordinates and both fermionic
ones to zero:
{
}
1
d−2 d−1 d
d|2
d−1
d
Md−2 ≡ y = (x , . . . x , x , x , θ, θ) ∈ R : x
=x =θ=θ=0 .
(4.1)

O(y, w)|Md−2 → Ô(x̂, ẑ) ,

ẑ ≡ w|Md−2 , x̂ ≡ y|Md−2 .

(4.2)

We will denote the restricted operators as Ô and their coordinates as x̂ ∈ Rd−2 . A hatted
operator with indices Ôαβ··· , will automatically imply α, β = 1, . . . , d−2. It is clear from the
SO(d − 1, 1) symmetry that the restricted operators belong to a CFT in d − 2 dimensions.
Since x̂ and ẑ are at the origin of the R2|2 space which is fixed by OSp(2|2), the operators
defined by (4.2) are annihilated by all generators of OSp(2|2), hence they are OSp(2|2)singlets. The definition (4.2) also implies that if O is a superprimary with superconformal
dimension ∆ then Ô transforms under SO(d − 1, 1) as a CFTd−2 primary of dimension ∆.
This follows straightforwardly from (3.19), as Ô is annihilated by K µ (µ = 1, · · · , d − 2)
and diagonalizes the (d − 2)-dilations D.
Note that (4.2) automatically gives the right symmetry structure of the reduced operators. E.g. a super-traceless graded symmetric OSp(d|2) spin ℓ tensor is projected to
a traceless symmetric spin ℓ tensor in d − 2 dimensions. In components, eq. (4.2) means
that Ô is obtained from O by two operations. First, we restrict the OSp(d + 1|2) indices
to the directions in Md−2 . Second, we subtract the traces. The latter operation is implicit
in (4.2) because ẑ µ ẑµ = 0. We can demonstrate this with the following simple example of
a spin 2 superprimary Oab which is super-traceless and graded symmetric. We first restrict
the indices a = µ, b = ν so that µ, ν ∈ {1, . . . , d − 2}, and then subtract the trace, so that:
gµν α
gµν ab
Ôµν (x̂) = Oµν (x̂) −
O α (x̂) ≡ Oµν (x̂) +
g Oab (x̂) .
(4.3)
d−2
d − 2 2|2
Since Oab is assumed traceless in full superspace, we have equivalently rewriten the subtracted d − 2 dimensional trace Oα α as minus the trace over the directions orthogonal to
Md−2 , with g2|2 the corresponding OSp(2|2) invariant metric.
The procedure (4.2) works for any operator O (for a generic mixed symmetric representations we only have to introduce different polarization vectors for each row of their
graded Young tableau). The restriction to θ, θ = 0 selects the bottom component O0 of
the superfield as defined in (3.20). It follows that the bottom component of any given
superprimary operator O gives rise to an operator Ô which is a singlet of OSp(2|2).

– 23 –

JHEP04(2020)090

This subspace breaks the symmetry from OSp(d + 1, 1|2) to SO(d − 1, 1) × OSp(2|2).
Second, dimensional reduction will only apply to the subsector of the supersymmetric
theory which consists of OSp(2|2) singlets of the broken symmetry. Let us illustrate how to
construct such operators. This can be done by simply considering a superfield O(y) inserted
at a point y ∈ Md−2 and contracting it with polarization vectors that also live in Md−2 (an
analogous construction is detailed in [33, 41] in the context of defect CFTs). For example
we may consider a superfield O(y, w) which transforms in the spin ℓ graded symmetric
representation of OSp(d|2) (we recall that w is a polarization vector). By restricting both
y and w to Md−2 we obtain an operator Ô with SO(p)-spin ℓ:

## PDF page 26

Md−2

In the above equation, Ôi is the projection of a superprimary Oi on Md−2 via (4.2).
Equation (4.4) looks like a usual restriction, however the resulting CFTd−2 has further
special properties. The most surprising one is that it has a conserved stress tensor, as we
16

We could in principle also consider the reduction from 3 to 1 dimensions. Since spin does not exist in 1d,
the story changes a bit. In this special case scalars superprimaries reduce to scalars, vector superprimaries
reduce to parity odd scalars, while any other representation reduces to zero. In particular super stress
tensor reduces to zero, so that we do not get a stress tensor in 1d. This is of course natural because we do
not expect local CFTs in 1d. In what follows we will not consider this special case.

– 24 –

JHEP04(2020)090

We emphasize that construction (4.2) can be applied to any operator O of the ParisiSourlas theory. To be sure, there is no requirement that the operator O should have some
protected dimension, or anything of the sort. Thus we obtain a huge number of operators
Ô in (d − 2) dimensions. The construction works simplest for scalars when no indices are
involved, but also for spinning primaries. There is however one subtlety: the attentive
reader may have noticed that depending on the dimension d, for some operators O transforming in complicated OSp(d|2) representations, the resulting operator Ô may come out
identically zero. This subtlety does not occur for most commonly occurring representations
such as graded symmetric traceless tensors as long as d ≥ 4 (so that the reduced space has
dimension at least 2). We will assume that d ≥ 4 in the rest of this paper.16
We wish to consider the theory in (d − 2) dimensions which consists of primary operators Ô defined via (4.2) and of their (d − 2) dimensional descendants. Let us call this space
of operators S0 . It should be pointed out that there are other OSp(2|2) invariant operators
which are not in S0 . E.g. we can take the trace of operator O with respect to orthogonal directions (i.e. the superspace components not in Md−2 ), or we can take derivatives
with respect to these orthogonal directions and contract them with the OSp(2|2) invariant metric g2|2 . Let us call operators of these latter types S1 . E.g. in (4.3), the trace
ab O
part Oα α = −g2|2
ab and hence can be regarded as an S1 operator. Both S0 and S1 are
OSp(2|2) singlets, but it turns out that S1 operators containing g2|2 decouple: correlation
functions of an arbitrary number of singlet operators with an S1 operator vanish on Md−2 .
This will be explained in section 4.2. Also, exchanges of S1 operators will be shown not
to contribute to correlation functions of S0 operators on Md−2 . For this reason it makes
sense to restrict our attention only to S0 operators.
Now we see that the considered reduction works rather differently from the usually
considered trivial defect theories. From each superprimary operator of the d-dimensional
theory we obtain one primary operator of the (d − 2) dimensional theory. In usual trivial
defect theories, even if we restrict to the subsector of operators preserved by the defect,
reduction is one to many. This is because analogues of operators we called above S1 do
not decouple for trivial defects.
Let us now discuss the features of the CFTd−2 thus defined by dimensional reduction.
A generic correlation function in the CFTd−2 is obtained from that of the OSp(d + 1, 1|2)
theory by restricting to Md−2 as follows:
∣
∣
⟨Ô1 (x̂1 ) . . . Ôn (x̂n )⟩ = ⟨O1 (y1 ) . . . On (yn )⟩∣∣
.
(4.4)

## PDF page 27

4.2

Decoupling of S1 operators

As we explained in the last section, there is an important difference between operators S0
and S1 , since the latter decouple from the singlet sector. Let us show how this happens.
Recall that S0 consists of primaries generated using (4.2) and their (d − 2)-dimensional
descendants. These operators are constructed from the (d − 2)-dimensional components of
O’s and of their (d − 2)-dimensional derivatives. The objects orthogonal to Md−2 are never
involved, thus ensuring the OSp(2|2) invariance of the obtained states. On the other hand,
S1 operators are defined by including the orthogonal objects (derivatives or components)
but in singlet combinations, i.e. by contracting them with the metric g2|2 on the space R2|2
(d = 2 case of (3.4)). Some examples of S1 operators are:17
ab
g2|2
Oab ,

ab
g2|2
∂ a Ob ,

ab
g2|2
∂a ∂b O .

(4.5)

With these definitions, S0 and S1 operators span the space of all OSp(2|2) singlets.
Now we will explain that, within singlets, the S1 operators completely decouple on
Md−2 in the following sense. Consider a correlation function of an arbitrary S1 operator
and any number of singlets (which may be S0 or S1 ). We claim that this correlator vanishes
on Md−2 :
⟨Õ O1 . . . On ⟩ = 0 on Md−2 ,
for Õ ∈ S1 , Oi ∈ S0 ⊕ S1 .
(4.6)
We repeat that this is only true if all operators are singlets and they all are positioned
on Md−2 . Because of this limitations, it would be wrong to say that the S1 operators are
identically zero, although they do decouple in the described sense.
Vanishing of (4.6) is proven as follows. By definition of S1 operators, (4.6) is some
OSp(2|2)-invariant expression containing at least one metric g2|2 , and which depends on
coordinates of operators, all in Md−2 . When constructing the invariant, the indices of
17

ab
Recall also the simple example of dimensional reduction (4.3), where Oα α = −g2|2
Oab is an S1 operator.

– 25 –

JHEP04(2020)090

shall demonstrate in section 4.3. From usual arguments, the reduced theory is endowed
with an OPE which arises from the restriction of the full OPE to Rd−2 . Of course the OPE is
closed in the subsector of singlet operators of OSp(2|2), meaning that the OPE of two singlet
operators only exchanges singlets (moreover, as we show in section 4.4, type S1 operators
decouple, so the OPE can be truncated to operators Ô and their (d − 2)-dimensional
descendants). By using the OPE, any four point correlation function of the reduced theory
can be expanded in CBd−2 , which means there should be a relation between the superblocks
of Parisi-Sourlas theory and the blocks of the CFTd−2 . Quite remarkably, this relation is
extremely simple. Indeed, as we prove in section 4.4, each superblock is mapped to a
single (d − 2)-dimensional block! So the operators defined as the OSp(2|2)-singlet parts of
superprimaries of the Parisi-Sourlas theory give rise to a local CFT in d − 2 dimensions.
We have given a general picture of how Parisi-Sourlas dimensional reduction works.
In the next section we discuss the decoupling of S1 operators. This will be important in
the following sections where we prove that the dimensionally reduced theory is indeed local
and that the superblocks are equal to conformal blocks in (d − 2)-dimensions. Additionally,
we will show how this equivalence gives a new relation between CBd−2 and CBd .

## PDF page 28

4.3

The stress tensor multiplet

In this section we shall demonstrate that, assuming that the OSp(d + 1, 1|2) theory is local,
the singlet sector of its restriction to Md−2 is also local. The first step is to show that if
the super-conformal theory has a super stress tensor Tab , then the dimensionally reduced
theory also has a spin two operator with dimension d − 2, which satisfies a conservation
equation.
We discussed in section 3.1.2 the super stress tensor Tab and its conservation. Following
the rule (4.2), the dimensionally reduced stress tensor T̂ will be related to T by the following
equation:
T̂ (x̂, ẑ) ≡ T (y, w)|Md−2 .
(4.7)
Setting the transverse coordinates, in particular θ, θ, to zero, picks out the bottom component T0 which has the same dimension as the Tab superdimension, that is d − 2. Since T̂
has the correct conformal dimension and spin, it is a good candidate for the stress tensor
of the CFTd−2 . Let us see that the conservation of T implies conservation of T̂ . We have
a

0 = ∂ Taν =

d−2
∑

αβ
ab
∂α gd−2
Tβν + ∂a g2|2
Tbν ,

(4.8)

α=1

where we denoted by gd−2 and g2|2 the metrics along and orthogonal to Md−2 . The second
term is an operator of type S1 in the sense of the previous section. In the first term we
have Tβν = T̂βν modulo another S1 operator, see (4.3). So we conclude that ∂ α T̂αβ = 0
modulo S1 operators. As we showed in section 4.2, correlation functions of S1 with other
singlets vanish on Md−2 . So T̂ is conserved within the singlet sector.18
So far we only discussed conservation of T̂µν away from other insertions. In the following we would like to see how the contact terms dimensionally reduce. This would fully
prove that the stress tensor candidate T̂µν generates translations in the CFTd−2 , hence
it is the true stress tensor, and the CFTd−2 is local. In (3.25) we defined the meaning
of locality for a Parisi-Sourlas theory. In what follows we use an alternative definition of
18

The just given argument can be succinctly expressed using the differential operator (3.16), which “opens
up” indices of tensors contracted with the external polarization vectors, by showing that (∂y ·Dw )T (y, w) = 0
implies (∂x̂ · Dẑ )T̂ (x̂, ẑ) = 0 in the singlet sector (where Dẑµ is used to open the indices of SO(d − 2) tensors).
In fact, one can see that on Md−2 , the operator ∂y · Dw acts as ∂x̂ · Dẑ modulo terms of S1 -type.

– 26 –

JHEP04(2020)090

g2|2 may be contracted with the reduced space objects (e.g. x̂, ẑ or the reduced metric),
which will trivially give zero. Alternatively, the indices of g2|2 may be contracted with the
indices of some other g2|2 floating around, such as if there are more than one S1 operators
in (4.6). However, the latter contraction gives the supertrace (g2|2 )aa = 2 − 2 = 0, which
also vanishes. In other words it is not possible to build a nontrivial OSp(2|2) singlet out
of g2|2 and reduced tensors. Hence all singlet correlation functions involving an operator
S1 must vanish.
The lack of singlets built out of g2|2 plays a crucial role in all proofs related to dimensional reduction. E.g. this fact is hidden in various steps of the demonstrations of locality
(see section 4.3) and dimensional reduction of the superblocks (see section 4.4).

## PDF page 29

locality which repackages equation (3.25) in terms of a condition on the OPE between Tab
and O. This is done by analogy with the non-supersymmetric story in [42] (see also the
lucid discussion of such matters in [43]). Indeed (3.25) is related to the following OPE
contribution:
Tab (y)O(0) ∼ · · · + Bab c (y)∂c O(0) + · · · ,

(4.9)

where the tensor structure B has to satisfy the following property:
∫
dd xdθdθ ∂ a Babc (y) = gcb ,

(4.10)

where V is the interior of a supersphere with radius ϱ.
We would like to show that, if (4.9) and (4.10) hold, then the operator T̂µν has the
following OPE with Ô:
T̂µν (x̂)Ô(0) ∼ · · · + Bµν ρ (x̂)∂ρ Ô(0) + · · · ,
with the condition

∫

dd−2 x̂ ∂ µ Bµνρ (x̂) = gνρ ,

(4.11)

(4.12)

V̂

where V̂ is the projection of V on Md−2 . These equations then imply that T̂ generates
(d − 2) dimensional translations.
Before entering the proof, it is convenient to fix the structure of Babc (y). This is
determined by requiring B a ac = 0 and ∂ a Babc = 0 (away from y = 0), respectively from
the tracelessness and conservation of the super stress tensor, as well as scaling as 1/y d−2
for dimensional reasons. This implies:
[
]
gba e
2
ya gcb + yb gac − d−2
yc gba
(ya yb − d−2
y ye )yc
Babc (y) = C
+ (d − 4)
,
(4.13)
d
d
(y a ya ) 2 −1
(y a ya ) 2
d−2
with an overall normalization constant C = 2(d−3)S
(where Sd−2 is the area of the sphere
d−2
in d − 2 dimensions), which we computed by performing the integral (4.10) explicitly.
Now that B is fixed, it is easy to show that the OPE (4.11) follows directly from (4.9),
by simply projecting it to Md−2 . Indeed a, b are trivially projected to µ, ν and it is easy
to see that Bµν c ∂c O = Bµν ρ ∂ρ O (in fact Bµν c vanishes when y = x̂ ∈ Md−2 and c is an
index orthogonal to Md−2 ).
We are then left to show how (4.12) follows from (4.10). For this it is convenient to
use the following equation:
∫
∫
µ
d
2
d xdθdθf (wi xµ , y ) = dd−2 x̂f (wiµ x̂µ , x̂2 ) ,
(4.14)

where y 2 = x2 + 2θθ and wiµ are vectors in Md−2 . To derive it we apply the d = 2 case
of (2.26) integrating over xd−1 , xd , θ, θ and treating the rest of the variables as spectators
(since wiµ ∈ Md−2 , the function being integrated is OSp(2|2) invariant).

– 27 –

JHEP04(2020)090

V

## PDF page 30

V

V̂

which proves the condition (4.12). Not surprisingly, the dimensionally reduced B has the
same functional form as that one given by Cardy [42].
The proof above may look technical, but it is rather explicit and has the advantage
of clearly showing how the contact terms are dimensionally reduced. We thus reach the
important conclusion that the locality of the Parisi-Sourlas CFT implies the locality of
the CFTd−2 . Here it is important to stress that by CFTd−2 we are referring to the
OSp(2|2)-singlet sector of the restricted theory. Indeed for operators which are charged
under OSp(2|2) we would not be able to use (4.14), and our proof would not go through.
4.4
4.4.1

OPE and conformal blocks
Dimensional reduction of OPE

Let us show the implications of the decoupling (4.6) for the OPE. Consider the OPE of
two scalar primaries Ôi ∈ S0 of dimensions ∆i . We can obtain this OPE by dimensionally
reducing the superspace OPE (3.46), which gives the expression of the form:
Ô1 (x̂)Ô2 (0) =

∑
O

λ

12Ô
[x̂αℓ · · · x̂α1 Oα1 ...αℓ (0) + superdesc.] .
|x̂|∆1 +∆2 −∆+ℓ

(4.16)

We can further rearrange the r.h.s of this equation. First of all we want to replace the
components of O by the components of the d − 2 dimensional traceless symmetric primary
Ô defined via (4.2). As explained in section 4.1, this involves some subtracted traces which
are S1 operators. We also want to split the superdescendant contributions into those
of usual d − 2 dimensional descendants and the rest, i.e. the superdescendants involving
superderivatives orthogonal to Md−2 . The latter are also S1 operators: they must appear
in OSp(2|2) singlet combinations, hence will involve contracting superderivatives with the
g2|2 metric. Thus after rearrangement we get:
Ô1 (x̂)Ô2 (0) =

∑

λ12Ô
|x̂|∆1 +∆2 −∆+ℓ

[

]
x̂α1 · · · x̂αℓ Ôα1 ...αℓ (0)+desc. +S1 contribution , (4.17)

Ô∈S0

So, any superprimary O with dimension ∆ and OSp(d|2)-spin ℓ in the superOPE (3.46) gave
rise to an S0 primary Ô contributing to the OPE (4.17), of the same scaling dimension

– 28 –

JHEP04(2020)090

Eq. (4.10) can be put in the form (4.14) as follows. First we note that in (4.14) the
integral is over the whole Rd|2 while in (4.10) it is over the super-ball V . We√
just replace the
d|2
latter with an integral over R with an appropriate step-function Θ(ϱ − y 2 ). Then we
b
c
contract the indices of (4.10) with polarization
√ vectors w1 , w2 that are restricted to Md−2 .
In summary we use (4.14) with f ≡ Θ(ϱ − y 2 )∂ a Babc w1b w2c . Finally we need to show that
∂ a Baνρ (y)|y∈Md−2 = ∂ µ Bµνρ (x̂). This is easy to see from a direct computation and basically
descends from the fact that the superdivergence ∂ a ya = d − 2 is equal to the divergence
∂ µ x̂µ in Rd−2 . Putting together all the ingredients, the equation (4.10) reduces to
∫
∫
d
a
gνρ =
d xdθdθ ∂ Baνρ (y) =
dd−2 x̂ ∂ µ Bµνρ (x̂) ,
(4.15)

## PDF page 31

and with the same OPE coefficient: λ12Ô = λ12O . This primary is accompanied by its
(d − 2)-dimensional descendants, as indicated in (4.17).
Now suppose we are interested in correlation functions of Ôi ∈ S0 , e.g. their four
point function. To compute the four point function, we use OPE (4.17) twice. Then we
are reduced to two point functions of exchanged operators. However as noticed above
the S1 operators have vanishing two point functions with any singlet, in particular among
themselves, and will drop out. Thus, for purposes of any such computation we can truncate
the OPE (4.17) dropping the S1 contribution:
∑

λ12Ô

[

|x̂|∆1 +∆2 −∆+ℓ

]
x̂α1 · · · x̂αℓ Ôα1 ...αℓ (0) + desc. .

(4.18)

Ô

It is in this sense that the OPE of S0 operators is closed on themselves, as already anticipated in section 4.1.
It is nice to rephrase this conclusion in terms of conformal blocks. Indeed, since the
S1 operators decouple, the superblocks will have a very simple relation with the CB d−2 .
This will be discussed in the next subsection.
4.4.2

Dimensional reductions of superconformal blocks

In this section we want to prove that the OSp(d + 1, 1|2) conformal blocks are equal to
conformal blocks in d−2 dimensions. Our strategy is to show that the two functions satisfy
the same differential equation, which arises by applying the (super) conformal Casimir. In
order to make the computation easier the argument is formulated in super-embedding
space, where the super-Casimir operator takes a very simple form.
For simplicity we will first focus on a four point function of scalar superprimaries and
we will analyze the super-Casimir equation (3.48) for the exchange of an operator O with
super-dimension ∆ and which transforms in a graded symmetric representation of OSp(d|2)
with spin ℓ:
d|2

d|2

d|2

C G∆,ℓ (Pi ) = c∆,ℓ G∆,ℓ (Pi ) ,

(4.19)

where Pi are points defined in super-embedding space of section 3.2. The eigenvalue appearing in this equation is given in eq. (3.34) and, as mentioned there, is equal to the
eigenvalue of the d − 2 dimensional Casimir equation. We are thus left to check that action of the differential operator C takes the same form as the Casimir differential operator
in d − 2 dimensions when we restrict this equation to the submanifold Md−2 defined in
section 4.1. This must be true, since the Casimir differential operators are equal up to
terms belonging to S1 , which vanish according to (4.6). However, to be more transparent,
let us show in more details how this match takes place.
For the purpose of the proof, it is convenient to write the superconformal Casimir C,
see eqs. (3.49), (3.32), as follows:
C = CP1 + CP2 + CP1 ,P2 ,

– 29 –

(4.20)

JHEP04(2020)090

Ô1 (x̂)Ô2 (0) =

## PDF page 32

where the operators CP and CP,Q are defined as
CP ≡ (d − 2 + P · ∂P )P · ∂P − P 2 ∂P2 ,
⏟ ⏞⏞ ⏟

CP,Q ≡ 2P A QB (∂P )B (∂Q )A − 2(P · Q)(∂P · ∂Q ) ,

=0

i

∆,ℓ

Md−2

i

α=0

i

∆,ℓ

Md−2

α=0

which takes the same form as their d − 2 dimensional counterpart. For the operator CP1 ,P2
the proof is slightly more complicated. By dropping terms proportional to xd−1 , xd , θ, θ we
only obtain
∣
d|2
CP1 ,P2 G∆,ℓ (Pj )∣M
d−2
⎛
⎞
d−2
d−2
d−2
∑
∑
∑
∣
d|2
= − ⎝2
P1α · P2 α
∂P1α ∂P2α − 2
P1α P2β (∂P1 )β (∂P2 )α ⎠ G∆,ℓ (Pj )∣M
d−2

α=0

−2

d−2
∑
α=0

P1α · P2 α

α=0

[(

α,β=0

) (
)]
∣
d|2
∂P d−1 ∂P d−1 + ∂P d ∂P d − ∂θ1 ∂θ2 + ∂θ2 ∂θ1 G∆,ℓ (Pj )∣M
1

2

1

2

d−2

.

The first line reproduces exactly the term needed for dimensional reduction to hold. It is
straightforward to show that the second line vanishes. Indeed, by conformal invariance,
the blocks are functions of the scalar products Pi · Pj . The two terms in the square brackets
∣
have the same action on any function f (Pi · Pj )∣M , with opposite signs, so that their
d−2

contribution exactly cancels.20
19

To this end it is useful to apply the following formula

1 AD BC
g g L(Pi )AB L(Pj )CD = PiA ∂iB (Pj )B (∂j )A − (−1)[C][D] g AC g BD (Pi )A (∂i )B (Pj )C (∂j )D .
2
Other useful relations are collected in appendix B.
20
To make the argument more explicit let us consider some examples. First we act with the square
bracket on a term (P1 · P3 )(P2 · P4 ). The result of the action is P3d−1 P4d−1 + P3d P4d − θ3 θ4 − θ4 θ3 , which
vanishes on Md−2 because all terms are projected to zero. In order to obtain a result that is not trivially
projected to zero, one can consider the action of the square bracket on (P1 · P2 ). However this would give a
term proportional to the super-trace of the orthogonal space which is zero, (1 + 1) − (1 + 1) = 0. It is easy
to see that the action of the square bracket on any function of (Pi · Pj ) will either be proportional to terms
which vanish on Md−2 or give the vanishing super-trace result. Indeed this is only an explicit example of
the decoupling described in section 4.2.

– 30 –

JHEP04(2020)090

(4.21)
where the term P 2 ∂P2 can be dropped as shown since P 2 = 0 on the projective lightcone.
The terms in (4.20) arise by collecting the contributions (L1 )2 , (L2 )2 and L1 L2 in (3.49)
and by commuting all the derivatives to the right.19 The relations (4.21) are also useful
to explicitly check the expression for the eigenvalue (3.34). In fact the action of Casimir
on O(P, Z) takes the form CP + CZ + CP,Z , where CP,Z reduces to 2Z · ∂Z . By using the
scaling properties of O(P, Z) one directly recovers (3.34).
d|2
We now want to consider the action of C on the function G∆,ℓ (Pi ) when we restrict
the points Pi on the manifold Md−2 . With this restriction, we can simply drop all the
terms which give a contribution proportional to P d−1 , P d , θ, θ. Then it is easy to see that
the operators CPi reduce to
(
) d−2
d−2
∑
∑
∣
∣
d|2
d|2
CP G (Pj )∣
= d−2+
Piα · ∂P α
Piα ∂P α G (Pk )∣
,
(4.22)

## PDF page 33

We therefore proved that the super-Casimir differential equation restricted to Md−2 is
equal to the Casimir equation in d − 2 dimensions. It is also straightforward to show that
the boundary condition at short distances that the conformal partial waves have to satisfy,
d|2
and which follows from the OPE, is the same. Hence, the conformal partial waves G∆,ℓ (Pi )
are identical to the partial waves Gd−2
∆,ℓ (P̂i ) of a d − 2 theory when the points Pi = P̂i are
restricted to Md−2 . This implies that conformal blocks, to which conformal partial waves
are proportional as shown in eq. (3.48), should agree as functions of u, v:
d|2

d−2
gO (u, v) = gO
(u, v) .

(4.23)

21

Notice however that some representations which naively do not exist in d−2 dimensions, may be dualized
to allowed representation, and then this vanishing does not occur. E.g. the representation with ℓ Young
tableau boxes in the first row and 1 box in the second row naively is not realized in three dimensions,
however by contracting it to an epsilon tensor we can transform it to a Young tableau which exists; it
corresponds to a parity odd traceless and symmetric representation of spin ℓ.

– 31 –

JHEP04(2020)090

Indeed, by conformal invariance, knowing conformal blocks on Md−2 is enough to fix their
functional form completely. Note that in the main case of our interest d ≥ 4, d − 2 ≥ 2, we
have two independent cross ratios u, v both before and after reduction.
The only difference between the blocks is the meaning of the argument at which they
are usually evaluated: g d−2 at the standard cross ratios u, v, the superblock g d|2 at the
super-cross-ratios U, V of (3.45).
So far we only considered the case of a spin ℓ exchange in a scalar four point function,
however we can easily run the same argument for generic spinning external operators and
for the exchange of an operator in a generic OSp(d|2) representation. For example, given
a four point function of operators Oi (Pi , Zi ) with spin ℓi , the super-Casimir operator in
the embedding space can be written as a sum of terms CPi , CZi , CZi ,Zj , CPi ,Zj , CPi ,Pj as
defined in (4.21). For all such terms we already proved that dimensional reduction works
as long as they act on scalar functions of Pi and Zj (by superconformal invariance the
superblocks are scalar functions dependent only on the combinations Pi · Pj , Pi · Zj , Zi · Zj )
and as long as we set Pi , Zj ∈ Md−2 .
With this simple argument we thus proved a very general result: the equality of superconformal partial wave and usual CFTd−2 partial waves. There are some exceptions to
the above rule. E.g. when the exchanged operator belongs to a representation which does
not exist in d − 2 dimensions. In this case the associated conformal partial wave vanishes
when restricted to Md−2 .21 See also the discussion in section 4.5. Another case is when the
kinematics of the reduced space does not allow for the complete reconstruction of the superconformal partial wave. For example by going from 3d to 1d we should interpret (4.23)
as a relation between the superblock restricted to a line and the 1d block (where both of
them depend on a single cross ratio).
Equality of conformal blocks for common representations has very important implications for the understanding of dimensional reduction, which we will discuss in section 4.5.
Before doing so, we show how this result also has interesting consequences for the theory
of conformal blocks.

## PDF page 34

4.4.3

Relations between conformal blocks in different dimensions

(d−2)

g∆,ℓ

(d)

(d)

(d)

(d)

(d)

= g∆,ℓ + c2,0 g∆+2,ℓ + c1,−1 g∆+1,ℓ−1 + c0,−2 g∆,ℓ−2 + c2,−2 g∆+2,ℓ−2 ,

(4.24)

where the generic scalar block in d − 2 dimensions is written as a linear combination of
only five blocks in d dimensions. The coefficients can be written in closed form as follows:
c2,0 = −

(∆−1)∆ (∆−∆12 +ℓ) (∆+∆12 +ℓ) (∆−∆34 +ℓ) (∆+∆34 +ℓ)
,
4(d−2∆−4)(d−2∆−2)(∆+ℓ−1)(∆+ℓ)2 (∆+ℓ+1)

c1,−1 = −

(∆−1)∆12 ∆34 ℓ
,
(∆+ℓ−2)(∆+ℓ)(d−∆+ℓ−4)(d−∆+ℓ−2)

c0,−2 = −

(ℓ−1)ℓ
,
(d+2ℓ−6)(d+2ℓ−4)

c2,−2 =

(4.25)

(∆−1)∆(ℓ−1)ℓ (d−∆−∆12 +ℓ−4) (d−∆+∆12 +ℓ−4) (d−∆−∆34 +ℓ−4) (d−∆+∆34 +ℓ−4)
.
4(d−2∆−4)(d−2∆−2)(d+2ℓ−6)(d+2ℓ−4)(d−∆+ℓ−5)(d−∆+ℓ−4)2 (d−∆+ℓ−3)

where as usual ∆ij = ∆i − ∆j are dimension differences of the external scalar primaries.
This assumes conformal blocks normalized as in [39, 44, 45] (see table I in [23] for a
comparison of different normalizations). We were able to obtain these relations in generic
dimensions even though the conformal blocks are not known in a closed form. To do so we
used the recurrence relation [45, 46] which determines the conformal blocks as an expansion
in the radial cross ratio r of [47]. In fact all the coefficients ci,j (for arbitrary values of the
spin ℓ) of the ansatz (4.24) are completely fixed already at order O(r2 ). We then checked
that higher orders in r also agree with eqs. (4.24), (4.25).22
22

We also checked that eqs. (4.24) and (4.25) are satisfied by some closed form expressions of conformal
blocks. In particular for the relation between 2 and 4 dimensions — where both blocks are known from the
early work of [39, 44] — and for 1 and 3 dimensions. In the latter case the 1d blocks depend on a single
cross ratio and should be compared to the 3d diagonal blocks (for ℓ = 0) of [48, 49].

– 32 –

JHEP04(2020)090

In the previous section we showed that the OSp(d + 1, 1|2) superconformal blocks are equal
to blocks in d − 2 dimensions. On the other hand, it is a completely standard fact that
the superconformal block can be decomposed as a sum of regular d-dimensional blocks
which sum up the contributions of all the conformal primaries in the supermultiplet of the
exchanged superprimary operator. Combining these two facts we are led to a somewhat unexpected conjecture: there should be a linear relation expressing a single conformal block
in d − 2 dimensions as a finite linear combination of conformal blocks in d dimensions.
Normally, relations between conformal blocks are studied the other way around. Indeed,
reduction of a d dimensional CFT to a trivial d − 2 dimensional defect implies that a single
d dimensional block should be expressible as an infinite linear combination of d − 2 dimensional blocks. Such infinite linear combinations have been worked out by Hogervorst [40]
for reduction d → d − 1, and by using his formulas twice we will get a doubly infinite sum
for reduction d → d − 2. We thus claim that these doubly infinite sums can be inverted by
a finite linear combination!
Surprising as it is, such a magic finite relation indeed exists, and it takes the following
form, beautiful to the eye of any conformal block expert:

## PDF page 35

Oa1 ...aℓ ⊃ O0α1 ...αℓ ,
⏟ ⏞⏞ ⏟
∆,ℓ

α1 ...αℓ
Oθθ
,
⏟ ⏞⏞ ⏟
∆+2,ℓ

Oθθα2 ...αℓ , Oθθα2 ...αℓ Oθθα2 ...αℓ Oθθα2 ...αℓ ,
⏟
⏞⏞
⏟
∆+1,ℓ−1

O0θθα3 ...αℓ ,
⏟ ⏞⏞ ⏟
∆,ℓ−2

θθα3 ...αℓ
Oθθ
.
⏟ ⏞⏞ ⏟
∆+2,ℓ−2

(4.26)
Since the tensor indices θ and θ can at most appear once (because of graded-symmetry),
primaries with ℓ − 3, ℓ − 4, . . . are forbidden. Hence, from this simple analysis, we obtain
the form of (4.24). Of course for low spins ℓ = 0, 1, some of the five mentioned classes
of representations vanish. For these low spins the corresponding coefficients ci,j vanish, as
can be seen from (4.25).
Another interesting feature of the coefficients ci,j is that they are not sign-definite, in
fact they are all negative for large ∆. This is related to the fact that the Parisi-Sourlas
theory is non-unitary. Notice that the above-mentioned infinite reductions from larger to
smaller d give rise to expressions with positive coefficients.
We can perform an even more refined consistency check, by obtaining the exact form
of the coefficients (4.25) by studying the decomposition of the superconformal multiplets
into conformal multiplets. As an example we recover the coefficient c2,0 for the case of
(d)
ℓ = 0, which multiplies g∆+2,ℓ=0 . This conformal block is associated to a scalar primary
operator Õ which is a descendant at the level two of a scalar superprimary O. In order to
have the right quantum numbers the operator Õ has to have the form:
|Õ⟩ = (P α Pα + a P θ P θ )|O⟩ ,

(4.27)

where the coefficient a can be fixed by requiring that Õ is a primary operator, K µ |Õ⟩ = 0.
We thus find
a = 2∆ − d + 2 .

(4.28)

The coefficient c2,0 arises because of the different normalization of Õ, which is a superdescendant, and therefore is not canonically normalized as a primary operators. In particular
23

We thank Hugh Osborn for pointing this out and for sending us the derivation after our paper appeared [51].

– 33 –

JHEP04(2020)090

Our relation (4.24) is reminiscent of a relation between conformal blocks in different
dimensions found by Dolan and Osborn (see eq. (5.4) of [39] and eq. (4.42) of [50]). However
the two relations are different. In fact the latter relates one block in d dimensions to five
blocks in d − 2 dimensions (so it works in the opposite way). Moreover the d-dimensional
block is multiplied by some function of the cross ratios, while in our relation all coefficients
are pure numbers. Although the connection is not obvious, it turns out that by judiciously
combining eq. (5.4) of [39] with eqs. (5.1), (5.2) of the same article, one can eliminate the
prefactor and obtain our recursion relation.23
Eq. (4.24) is very useful to demonstrate some features of the OSp(d + 1, 1|2) representation theory, which we explained in the previous sections. For example, we may look at
the expansion of a superfield in the Grassmann variables, as shown in (3.20). An operator
Oa1 ...aℓ in traceless graded-symmetric representation of OSp(d|2) of spin ℓ, contains exactly
five classes of Grassmann-even primary operators (which transforms under SO(d)):

## PDF page 36

the coefficient c2,0 is written as
c2,0 (ℓ = 0) =

M (∆12 )M (∆34 )
,
N

(4.29)

where the coefficients N and M are respectively defined in terms of the norm of |Õ⟩ and
its three point functions with other two operators:
⟨Õ|Õ⟩ ≡ N ⟨O|O⟩ ,

⟨Oi Oj Õ⟩ ≡ M (∆ij ) ⟨Oi Oj O⟩ .

(4.30)

N = −4∆(∆ + 1)(d − 2(∆ + 1))(d − 2(∆ + 2)) .

(4.31)

In order to compute M we conveniently choose to act with the combination (P α Pα +aP θ P θ )
on the leading OPE O(x, θ, θ)Oi (0) ∼ cOij (x2 − 2θθ)−(∆+∆ij )/2 Oj (0), following the conventions of [45]. In practice this gives us a very straightforward definition of M :
∣
∆+∆ ∣
∆+2+∆12
α
θ θ
2
− 2 ij ∣
2 −
2
(∂ ∂α + a ∂ ∂ )(x − 2θθ)
≡
M
(∆
)
(x
)
.
(4.32)
ij
∣
θ,θ=0

The result of this computation is
M (∆ij ) = (∆ij − ∆) (∆ + ∆ij ) .

(4.33)

By using formula (4.29) and replacing (4.31) and (4.33), we finally recover the exact form
of c2,0 (ℓ = 0), as predicted by (4.25). One could, of course, recover all the other coefficients
(also for generic ℓ) through similar computations. We did not invest time in doing so.
4.5

Comments

In section 4.4 we showed that each superconformal block of the Parisi-Sourlas theory reduces to a single CBd−2 . This means that in the OPE all the superdescendant exchanges
are reduced to descendant exchanges. As we explained in sections 4.1 and 4.4.1, this is
somewhat non-trivial because contrary to how reductions work for trivial defects. In fact
typically we would expect that a given supermultiplet would reduce to an infinite tower of
CFTd−2 multiplets. Our analysis shows that the infinite tower decouples inside the dimensionally reduced four point function, leaving only the contribution of a single multiplet. In
the language of (4.17), this is the consequence of the fact that the S1 contributions drops
out. It was already explained there but we would like to emphasize this again. We thereby
obtain that the superconformal block decomposition of a scalar four point function reduces
as follows:
⟨O1 (P1 ) . . . O4 (P4 )⟩ =

∑

d|2

λ12 ∆,ℓ λ∆,ℓ 34 G∆,ℓ (Pi ) −→ ⟨Ô1 (P̂1 ) . . . Ô4 (P̂4 )⟩ =

∆,ℓ

∑

λ12 ∆,ℓ λ∆,ℓ 34 Gd−2
∆,ℓ (P̂i ) ,

∆,ℓ

(4.34)
where P̂i are the dimensionally reduced counterparts of Pi . The two sums run over the same
spectrum, meaning that the exchanged operators are labelled by the same values (∆, ℓ).

– 34 –

JHEP04(2020)090

By using the commutation relations of the superalgebra (3.18) (or equivalently by taking
derivatives on a two point function), we obtain

## PDF page 37

24

E.g. we can consider O1 , O2 to transform in a spin ℓ representations in 5d. In their 5-dimensional
OPE we may find operators O′ labeled by two equal rows of length ℓ in the Young tableau. While this
representation exists in 5d, it does not exist in 3d (for ℓ > 1). For ℓ = 1 instead this may be dualized to a
parity odd vector representation, which does exist in d = 3. See also footnote 21.

– 35 –

JHEP04(2020)090

Furthermore all OPE coefficients match. In addition, in section 4.3, we detailed how the
reduction of the super-stress tensor implies that the CFTd−2 is local. These results explicitly show in which sense a sector of the Parisi-Sourlas theory, given by OSp(2|2)-singlet
operators, is described by a local non-supersymmetric CFTd−2 . A few more comments
related to this picture are in order.
From what we say above, and from the definition (4.2), it may seem that any superprimary operator in the SUSY theory descends to a primary operator in the CFT d−2 with
the same dimension ∆ and which transform in a representation of SO(d − 2) labelled by
the same Young tableau. However this is not always true. Some superprimaries have no
description in terms of primaries of the CFTd−2 . This happens when the Young tableau of
OSp(d|2) cannot be associated to a Young tableau of SO(d − 2). Indeed Young tableaux of
SO(d − 2) only have [ d2 − 1] lines while the ones of OSp(d|2) are of the form (3.8). So, for
example, in the Parisi-Sourlas theory there are operators labelled by a column of n gradedantisymmetric boxes (for generic values of n), which are not there in the CFTd−2 when
n is sufficiently large. Indeed one can see that the procedure (4.2), to generate a singlet
of OSp(2|2), would project such operators to zero. In other word, we cannot associate to
all the supersymmetric operators an OSp(2|2) singlet, hence the spectrum of the CFTd−2
does not contain information of all the superprimaries of the Parisi-Sourlas theory.
Let us discuss some simple consequences of this fact. The first trivial comment is that,
if a superprimary O′ is projected to zero by (4.2), then all correlation functions which
contain O′ are projected to zero. One may then ask what happens when O′ is exchanged
inside the OPE of two superprimary operators O1 , O2 which are not projected to zero. The
answer is that the exchange of O′ would be projected to zero. This is bound to happen
since it is not possible to build the SO(d−2) tensor structure which multiplies the projected
operator Ô′ inside the OPE.24 The associated partial wave vanishes since its leading OPE,
which sets the boundary condition of the Casimir equation, is zero.
Finally it is interesting to wonder if the opposite of dimensional reduction may also
work. Namely, given an abstract local CFTd−2 , can we always uplift it to a superspace
Rd|2 and obtain a Parisi-Sourlas CFT? This procedure indeed looks viable since a huge
part of the SUSY CFT data is described by the lower dimensional theory. For example all
four point functions of scalar operators of the CFTd−2 can be easily uplifted preserving all
CFT axioms. In fact it is clear that we can change the direction of the arrow in (4.34).
However, the presence of the operators of the kind O′ , discussed above, stops us from
making the strong claim, since information about them cannot be obtained from lower
dimensions. One could hope that this part of the spectrum can be fixed by imposing extra
consistency conditions, as we speculate in the conclusions. Because of this complication,
reconstruction of the full SUSY CFTd from CFTd−2 is not a completely trivial problem
and requires further analysis. This problem has an interesting analogy in the problem of
critical dynamics, which we review in appendix D.

## PDF page 38

5

Conclusions

25

This should be distinguished from random bond type of disorder, which corresponds to disorder in the
coupling J in Hamiltonian (1.1). Random-bond disorder is also interesting but the physics involved is quite
different; see [52] for recent work.
26
E.g. the classification of [53] assumes that the generators of the supersymmetries transform in the
fundamental spinor representation of the Lorentz group. One may be confused since the algebra OSp(d +
1, 1|2) also describes some unitary theories, as the six-dimensional (2, 0) SCFTs. However, even when the
algebra is of the Parisi-Sourlas type, the generators of the superconformal symmetries classified by [53] are
embedded inside the orthosymplectic rotations in a different way, see e.g. [54].

– 36 –

JHEP04(2020)090

In this paper we studied the implication of Parisi-Sourlas superconformal symmetry. This is
conjectured to be realized in RG fixed points of models with random field type of disorder. 25
The full Parisi-Sourlas conjecture works in some cases and to fail in others, as we will
revisit in a forthcoming paper. Here we narrowed the scope, and studied the problem from
a different point of view, by focussing on the supersymmetric fixed points themselves.
These fixed points enjoy OSp(d + 1, 1|2) superconformal symmetry. They possess some
unusual features which escape the conventional classifications of superconformal theories
available in the high-energy physics literature.26 In fact Parisi-Sourlas theories are nonunitary and the generators of their supersymmetries transform not as spinors but as scalars
or vectors under rotations. While lack of unitarity may seem unusual to a particle physicist,
unitarity is not a request of fundamental importance in statistical physics context, and
numerous non-unitary theories are known to play a role in nature.
In section 3 we showed how these superconformal theories work from an axiomatic
point of view. We started with a detailed analysis of their symmetries and representations.
We explained how to embed the stress tensor of the theory in a superconformal multiplet.
We then analyzed correlation functions by introducing a super-embedding space formalism
and we exemplified it in some simple cases. Finally we showed how to define the OPE and
the superconformal block decomposition of four point functions. While this analysis could
have revealed some pathological features, it did not: these theories seem perfectly healthy.
The most compelling aspect of Parisi-Sourlas supersymmetric theories is that they
undergo the so called “dimensional reduction”. Namely that a sector (the OSp(2|2)-singlet
sector) of the SUSY theory is described by a d−2 dimensional CFT. In section 4 we carefully
explain the meaning of dimensional reduction and its implications at the level of axiomatic
CFTs. We showed that the locality of the Parisi-Sourlas CFT implies the locality of the
d − 2 dimensional theory. We then explained that every superprimary descends under
dimensional reduction to one primary, while infinitely many additional operators which
would naively also be expected to arise (as they do arise for reductions to trivial defects)
decouple. This is explained by direct inspection of the OPE and by the computation of the
superconformal blocks of the theory, which we prove to be equal to the usual conformal
blocks in d − 2 dimensions. Finally, from the study of superconformal blocks, we obtained
a new finite-term linear relation involving conformal blocks in d and d − 2 dimensions. This
relation is between non-supersymmetric blocks and may look like it has nothing to do with
supersymmetry. However, the existence of this surprising relation is a direct consequence
of the Parisi-Sourlas supersymmetry and could not have been guessed otherwise.

## PDF page 39

We have thus illustrated that the Parisi-Sourlas CFTs are axiomatically well defined
and that they undergo dimensional reduction. These facts have some important consequences. First we confirm that such SUSY fixed points do exist, hence they could be
reached at the end of an RG flow. One reason why they are not always reached at the end
of the random field theory flow could be their RG instability. If this is the case, it follows
that they should be reachable by tuning extra parameters (e.g. by changing the disorder
distribution). We find this hypothesis very tempting and it would be really exciting to see
experimental and numerical evidences of this fact. We will have more to say in [13].

We would like to mention here another, seemingly unrelated, known class of examples,
when supersymmetric theories reduced to a trivial defect also give a local theory: N = 2
superconformal theories in d = 4 and six-dimensional (2, 0) theories in d = 6. Reduced to a
plane, they give 2d chiral algebras possessing a local stress tensor [55, 56]. These chiral algebras capture correlation functions of certain supersymmetrically protected operators put
in the plane and contracted with x-dependent polarization vectors (“twisted-translated”).
In [55, 56], the higher dimensional SCFT is unitary, while the reduced chiral algebra is
non-unitary. This is opposite to our case, when the higher dimensional theory is always
non-unitary, while the reduced theory may well be unitary.
Finally we want to comment on a very deep but speculative direction hinted at in
our work. From our analysis there seems to exist a very general relation which connects
CFTs in different dimensions. Indeed we found that the dimensionally reduced CFT d−2
captures a huge part of the CFT data of the Parisi-Sourlas theories. For example the whole
spectrum of scalar superprimaries and all the three point function coefficients appearing
in their OPEs is determined by the CFTd−2 . This seems to suggest that the opposite of
dimensional reduction (“dimensional lift”) may also work. Namely that any given CFT d−2
can be lifted to Rd|2 to define a theory with OSp(d + 1, 1|2) supersymmetry. (This idea can
also be inspired by an analogy in the problem of critical dynamics reviewed in appendix D.)
However, as we explained in section 4.5, this uplift is not trivial because some superprimary
operators of the Parisi-Sourlas theory have no counterpart in the CFTd−2 . It would be
interesting to see if this part of the spectrum can be reconstructed from crossing symmetry
consistency conditions. For example, it should be possible to constrain the CFT data
of these operators by bootstrapping their correlation functions in the higher dimensional
theory. If this picture is proven correct we would conclude that the existence of a local
CFTd , automatically implies the existence of a discrete sequence of CFTd+2n for integer
n, which are local, non-unitary and supersymmetric. Alternatively, if the conjecture is
incorrect, there should be a condition which determines which CFTs can be lifted and
which cannot. Either way this is exciting and deserves further investigation.

– 37 –

JHEP04(2020)090

A straightforward extension of this work is to study theories with superconformal
symmetry OSp(d − 1 + 2n, 1|2n). Loosely speaking, here the 2n fermionic degrees of
freedom should effectively cancel with 2n bosonic ones. So with an analysis analogous to
ours it should be possible to see that these theories undergo a dimensional reduction by
2n. Perhaps such theories also describe observables of some critical disordered theories.

## PDF page 40

Acknowledgments

A

Perturbative dimensional reduction

The equivalence of the supersymmetric theory in (2.15) and the d − 2 dimensional theory (2.24) can be shown from perturbation theory. In this appendix we explain how to
recover (2.25) by showing that any general Feynman integral from the SUSY action reduces
to a Feynman integral of the (d − 2)-theory.
∑
We assume a general polynomial form of V (Φ) = m≥2 gm Φm . Then a generic superfield diagram would be:
∫
∏(
)q
pmax
F (y1 , · · · , yn ) = (2π)
[dyp ]
GΦΦ (yij ) ij .
(A.1)
i<j

Here [dyp ] = p dd xp dθp dθp , and p ∈ I = {1, . . . pmax } labels the internal points (vertices)
of the diagrams. We shall use indices i, j, . . . to number generic points, internal or external.
Also let us call the total number of propagators as N . The factor outside the integral arises
from rescaling of the coupling constants due to the overall factor in the SUSY action (2.15).
The number qij denotes the power with which a certain GΦΦ (yij ) arises, where yij = yi − yj
and GΦΦ is the free theory propagator of the superfield Φ. We can obtain GΦΦ (with the
appropriate normalization factor) from (2.15) by setting V (Φ) = 0,
a
GΦΦ (y) = (
(A.2)
) d−4 ,
2
2
x + 2θθ
(d
)
d
where a ≡ Γ 2 − 2 /(8π 2 ). For simplicity we are using massless propagators and treating
mass as a perturbation. In what follows it will be convenient to split the coordinates in
different groups:
∏

α

y a ≡ {xα , θ, θ} = {x̂α , x⊥ , θ, θ} ,

x̂α ≡ {x1 , · · · , xd−2 } ,

α

x⊥ ≡ {xd−1 , xd } .

(A.3)

In order to prove dimensional reduction of (A.1), we want to show that if we set
α
x⊥
= θi = θi = 0 for any external point yi , the integral reduces to
i
∫
∏(
)q
F (x̂1 , · · · , x̂n ) = (2π)pmax [dx̂p ]
Gφ̂φ̂ (x̂ij ) ij ,
(A.4)
i<j

– 38 –

JHEP04(2020)090

S.R. is grateful to Édouard Brézin for the introduction to Random Field Ising Model, to
Giorgio Parisi for the invitation to the stimulating workshop Beyond Mean Field Theory
(Rome, January 2018), and to Nicolas Sourlas for many stimulating conversations, for mentioning [19], and for comments on the draft. A.K. and E.T. would like to thank R. Gopakumar, N. Ishtiaque, B. Le Floch, G. Mandal, M. Meineri, M. Paulos, J. Penedones, B. van
Rees, V. Schomerus, D. Simmons-Duffin, A. Sinha and participants of Bootstrap 2019
(Perimeter Institute) for useful discussions. A.K. would like to thank YITP, Stony Brook for
hospitality during the course of this work. E.T. would like to thank the participants of the
workshop Nonperturbative Methods for Conformal Theories (Natal, April 2019). This work
was partially supported by the Simons Foundation grant 488655 (Simons Collaboration on
the Nonperturbative Bootstrap) and by Mitsubishi Heavy Industries (MHI-ENS Chair).

## PDF page 41

where [dx̂p ] =

∏

pd

d−2 x̂ .
p

The function Gφ̂φ̂ (x̂12 ) = a (x̂212 )

− d−4
2

is the free theory prop-

agator of φ̂ from (2.24) . Notice that the normalizations of the propagators of φ̂ and Φ
are the same, which is crucial to the simplification of the computations. This follows from
Fourier transforming their respective momentum space propagators as a direct consequence
of (4.14).27
A useful tool to handle propagators in position space is the Schwinger parametrization:
∫ ∞
1
1
=
du ur−1 e−uA .
(A.5)
Ar
Γ(r) 0

i<j

i,j

(A.6)
∏
Here [duij ] = i<j duij , N is a product of Gamma functions, and the matrix Mij is given
by (this matrix is obtained by expanding x2ij and θij θij in terms of xi , θi , θj ):
{∑
Mij =

k uik ,

if i = j

−uij (≡ −uji ),

(A.7)

otherwise .

Now separating the variables as in (A.3) we can rewrite (A.6) as
N

F (y1 , · · · , yn ) = N a (2π)

pmax

∫

[ ∑
]
∏ ( qij ( d −3) ) ∫
2
[dx̂p ] exp −
x̂i ·x̂j Mij
[duij ]
uij
i<j

∫
×

i,j

(A.8)

[ ∑
]
( ⊥ ⊥
)
⊥
[dxp ][dθp ][dθp ] exp −
xi ·xj Mij +2θi θj Mij .
i,j
α

Let us focus on the integral in the second line of (A.8). By setting x⊥
= θi = θ i = 0
i
for the external points, only internal points contribute to the sum over i, j. Namely the
integral becomes
[
]
∫
∑ (
)
⊥
⊥
⊥
xp1 · xp2 M̃p1 p2 + 2θp1 θp2 M̃p1 p2 ,
(A.9)
I = [dxp ][dθp ][dθp ] exp −
p1 ,p2 ∈I

where I is the set of internal points and M̃p1 p2 is a pmax × pmax matrix (recall that pmax is
the number of internal points) obtained by restricting Mij∈I . Now, since the integrals over
x⊥ , θa , θa are Gaussian, I can be computed as follows:
[
] [
]
π pmax
det(M̃ )
I=
×
= 1.
(A.10)
π pmax
det(M̃ )
27

It is possible to normalize both propagators to one, which amounts to rescaling the kinetic terms in the
two actions (2.15) and (2.24).

– 39 –

JHEP04(2020)090

Introducing one Schwinger parameter uij per propagator, eq. (A.1) becomes
[ ∑
]
∫
∫
∏ ( qij ( d −3) )
(
)
F (y1 , · · · , yn ) = N aN (2π)pmax [dyp ] [duij ]
uij 2
exp −
xi ·xj Mij +2θi θj Mij .

## PDF page 42

Here the results in the left (right) square brackets is obtained from the bosonic (fermionic)
integral. We therefore conclude that
[ ∑
]
∫
∏ ( qij ( d −3) ) ∫
pmax
N
2
F (x̂1 , · · · , x̂n ) = N a (2π)
[duij ]
uij
[dx̂p ] exp −
x̂i · x̂j Mij
i<j

= (2π)pmax

∫
[dx̂p ]

∏(

i,j

Gφ̂φ̂ (x̂ij )

)qij

.

(A.11)

i<j

B

Useful relations in super(embedding)space

In order to make more clear of the computations of section 4 we collect here some useful
properties of the superspace and the super-embedding space.
We shall first consider the super-embedding space Rd+1,1|1 . The metric g AB defined
in (3.27) is non-diagonal and non-symmetric because of the J2 piece so we need to be
careful with the position of the indices:
P A P B = (−1)[A][B] P B P A ,

g AB = (−1)[A][B] g BA ,

(B.1)

where [A] = 0 if A = 0, . . . , d + 1 and [A] = 1 for the remaining two grassmannian
coordinates. Equations (B.1) in turn imply that the scalar product is symmetric P · Q =
Q · P . In order to raise and lower indices we use the following conventions:
PA ≡ g AB P B ,

P A ≡ g BA PB .

(B.2)

A and g A =
By using the above formulas on the metric itself we obtain that g AB = δB
B
A
[A][B]
A
B
δB (−1)
. Hence g A = d + 4 while g B = d. Furthermore it is important to remember
that g AB is not the inverse of g AB . In fact

g AB g BC = (−1)[B]([A]+[C]) g BA g CB = (−1)[B](2[A]) g BA g CB = g C A = (−1)[A][C] δ AC . (B.3)
Let us now exemplify how the derivatives ∂M ≡ ∂P M = (∂P 0 , ∂P µ , ∂P d+1 , ∂θ , ∂θ ) act in
super-embedding space. It is again important to keep track of the order of the indices in
all computations. For example,
N
∂ M P N = δM
,

∂ M PN = g N M ,

∂ M P N = gN M ,

M
∂ M PN = (−1)[M ][N ] δN
.

(B.4)

All the previous equations can be alternatively defined in superspace Rd|2 . The results are
basically the same after the map:
g AB → g ab ,

– 40 –

P A → ya ,

(B.5)

JHEP04(2020)090

So we get the same Feynman integral as in d − 2 dimensions. Although it may not be
obvious, the mechanism for dimensional reduction is similar to what was demonstrated
in (2.26). Namely, for integrals of functions of distances, the fermionic components cancel
out with two of the bosonic ones, which results in dimensional reduction.

## PDF page 43

where y a = (xα , θ, θ) ∈ Rd|2 are the superspace points and g ab is the superspace metric
defined in (3.4). In particular let us emphasize that by taking different traces of the
superspace metric the following two results can be obtained:
g aa = d + 2 ,

ga a = d − 2 .

(B.6)

Finally we stress that the trace g aa depends on the choice of the tensor basis. The appropriate OSp(d|2) invariant trace, the so called supertrace, is ga a . It is only the supertrace
that can appear in our computations.

Example: free theory

As a demonstration let us consider the supersymmetric theory of a free massless scalar Φ,
which can be written as
∫
1
SSUSY = 2π dd xdθdθ g ab ∂a Φ∂b Φ .
(C.1)
2
Because of the θ, θ integrals, the dimension of the super-Lagrangian is d − 2, which implies
that the dimension of Φ is d2 − 2. Indeed this is the dimension of a scalar superprimary
that satisfies the equations of motions ∂ a ∂a Φ = 0, as we explained in subsection 3.1.2.
By expanding Φ in θ and θ (see equation (2.16)), we conclude that the dimensions of its
constituents are
[ ] d
ϕ = − 2,
2

[ ] [ ] d
ψ = ψ = − 1,
2

[ ] d
ω = .
2

(C.2)

Noether’s theorem can be used to define a super-stress tensor:
Tab0 =

δL
∂b Φ − gba L ,
δ(∂ a Φ)

(C.3)

with the conservation law, ∂ a Tab0 = 0. From (C.3) it is clear that [T 0 ] = d − 2, as predicted
in section 3.1.2. We construct an improved version of the super-stress tensor that satisfies
the tracelessness property T a a = 0:
Tab = (∂(a Φ)(∂b] Φ) −

d−4
gba
Φ∂a ∂b Φ −
(∂ c Φ)(∂c Φ) ,
d−2
d−2

(C.4)

where (·] implements graded-symmetrization. It is easy to verify, following the equation of
motion of (C.1), that this satisfies a super-conservation equation like (3.22) . Expanding
in θ, θ, we get
Tθθµν = T µν = 2∂ (µ ϕ∂ ν) ω + 2∂ (µ ψ∂ ν) ψ +
−

4−d
(ϕ∂ µ ∂ ν ω + ω∂ µ ∂ ν ϕ + ψ∂ µ ∂ ν ψ − ψ∂ µ ∂ ν ψ)
d−2

2g µν
(∂ρ ϕ∂ ρ ω + ∂ρ ψ∂ ρ ψ) .
d−2

(C.5)

This satisfies the conservation equation ∂µ T µν = 0 and hence is the stress-energy tensor of
the d-dimensional theory that one obtains from (C.1) by performing the θ, θ integral .

– 41 –

JHEP04(2020)090

C

## PDF page 44

Now let us use the formula (4.7) to obtain the SO(d − 2) stress-tensor. This is given by
T̂αβ = (∂α ϕ)(∂β ϕ) −

gαβ
d−4
ϕ∂α ∂β ϕ −
(∂γ ϕ)(∂ γ ϕ) .
d−2
d−2

(C.6)

Here α runs from 1 to d − 2. The above satisfies the conservation equation ∂ α T̂αβ = 0 in
d − 2, given the theory is free, i.e. ∂ 2 ϕ = 0.

D

Supersymmetry in the problem of critical dynamics

⟨φ(x1 ) . . . φ(xn )⟩CFT = ⟨φ(x1 , t) . . . φ(xn , t)⟩ ,

(D.1)

where the average is over equilibrium state, which is time independent.
The problem of critical dynamics is more general and concerns correlators at unequal
times, i.e.
⟨φ(x1 , t1 ) . . . φ(xn , tn )⟩ .
(D.2)
When we insert the operator φ(x1 , t1 ) at the smallest time t1 (say), this disturbs the
system away from equilibrium and it starts relaxing back to it, so that when we complete
the measurement by inserting other operators at later times we probe a perturbed system.
If all operators are inserted at the same time t1 = . . . = tn this perturbation has not spread
and we measure the static correlators as before, but for unequal times we will measure
different quantities which will depend on time differences.
Unequal-time correlators (D.2) are expected to be scale invariant under the transformation
x → λx, t → λz t (λ > 0),
(D.3)
where z is a parameter called the dynamical critical exponent. Unlike for static correlators (D.1), there is no reason to expect any more complicated extended symmetry such as
conformal invariance.
While equilibrium equal-time correlators (D.1) depend only on the Gibbs distribution,
unequal-time correlators (D.2) depend on the additional piece of data: the mechanism
by which the system relaxes back to equilibrium. Various such mechanisms are listed

– 42 –

JHEP04(2020)090

In this paper we dealt with the appearance of Parisi-Sourlas supersymmetry in physics
of disordered systems. In this appendix we will review how supersymmetry plays a role
in another problem of statistical physics: critical dynamics. Our review is based on [57],
chapters 36, 16, and 17. See also [1], chapter 10.
Consider a d-dimensional system at a thermodynamic continuous phase transition.
We are interested in correlation functions of local operators, e.g. the fluctuating order
parameter field φ. The usual problem of critical statics concerns equilibrium correlation
functions, determined by the equilibrium Gibbs distribution. E.g. for the ferromagnetic
phase transition we might consider a d-dimensional path integral with the Landau-Ginzburg
∫
action S[φ] = dd x H[φ], H(φ) = (∂φ)2 + m2 φ2 + λφ4 , tuning m2 to reach the IR fixed
point described by a CFTd . Time dependence is, by definition, absent in critical statics.
Physically, we are dealing with equal-time correlators:

## PDF page 45

where ν is a Gaussian white noise, ⟨ν(x, t)ν(x′ , t′ )⟩ = 2δ(x − x′ )δ(t − t′ ) (for this normalization of its two-point function, the equilibrium Gibbs distribution is precisely e−S[φ] ). This
equation does not preserve the average φ(x, t) so it corresponds to Model A. For other
models the story would be similar with a somewhat different Langevin equation, see [1, 57].
The next step is to encode (D.4) in a path integral. For this we introduce a Lagrange
multiplier field ω and two Grassmann fields c and c to reproduce the determinant arising
from the functional δ-function. Integrating over the noise, we get a path integral with the
action in d + 1 dimensions (see [57], (16.128))
∫
{
}
S[φ] = dd xdt −ω 2 + ω[φ̇ + δH/δφ] − c(∂t + δ 2 H/δφδφ)c .
(D.5)
One then introduces the superfield
Φ(x, t, θ, θ) = φ(x, t) + θc(x, t) + θc(x, t) + θθω(x, t)

(D.6)

and rewrites the action as
∫
S[φ] =

dd x dt dθ dθ{DΦDΦ + H[Φ]} ,

(D.7)

where the superderivatives are D = ∂θ , D = ∂θ − θ∂t . This action has two supersymmetry
generators Q = ∂θ , Q = ∂θ + θ∂t .
This supersymmetry has a physical raison d’être. Any problem of critical dynamics
must satisfy a physical constraint known as the fluctuation-dissipation theorem, which
expresses the two point function ⟨φ(x1 , t1 )φ(x2 , t2 )⟩ as an integral of a response function
(see [1]). In the supersymmetric formulation, the response function is the two point function ⟨φ(x1 , t1 )ω(x2 , t2 )⟩, and the fluctuation-dissipation theorem can be recovered as a
supersymmetric Ward identity.
The problem of critical dynamics thus consists in taking a d-dimensional CFT describing critical statics and in finding a (d+1)-dimensional, space+time, supersymmetric theory
which reduces back to the CFT when all times are set equal. Stated this way, this problem

– 43 –

JHEP04(2020)090

in the literature, but two most well-known ones are Model A and Model B. Model B
conserves the average value of the order parameter, while Model A (also known as the
Glauber dynamics) does not. When doing Monte Carlo simulation of the lattice Ising
model, Model A is the usual Metropolis algorithm flipping individual spins, while Model
B is flipping only opposite sign pairs of nearby spins: +− ↔ −+. Universality holds for
critical dynamics, with models differing by symmetry considerations, like Model A and
Model B, corresponding to different universality classes. Thus each static universality class
may correspond to several dynamic universality classes, which will have different unequaltime correlators (D.2), but will share the same equal-time correlators (D.1). In particular,
they have a different dynamical critical exponent z.
In the continuum description, approach to equilibrium can be described by the
Langevin equation
δ
∂t φ(x, t) = −
H[φ] + ν(x, t) ,
(D.4)
δφ(x, t)

## PDF page 46

is analogous to the problem of “dimensional lift” which we encountered in the random
field Ising model context in section 4.5 and in the conclusions. We find this analogy quite
suggestive, even though it is not complete, most notably because of the absence of any
symmetry mixing x and t in the critical dynamics case.
It should be noted that the d → d + 1 connection does not play much of a role in the
currently existing practical methods of solving critical dynamics, which basically analyze
the (d + 1)-dimensional RG problem from scratch. It would be interesting to find an
alternative method which would take into account the d-dimensional static information
when it is available (e.g. when critical statics is exactly solved, as for the 2d Ising model).

References
[1] J. Cardy, Scaling and Renormalization in Statistical Physics, Cambridge Lecture Notes in
Physics, Cambridge University Press (1996).
[2] Y. Imry and S.-k. Ma, Random-Field Instability of the Ordered State of Continuous
Symmetry, Phys. Rev. Lett. 35 (1975) 1399 [INSPIRE].
[3] A. Aharony, Y. Imry and S.K. Ma, Lowering of Dimensionality in Phase Transitions with
Random Fields, Phys. Rev. Lett. 37 (1976) 1364 [INSPIRE].
[4] G. Parisi and N. Sourlas, Random Magnetic Fields, Supersymmetry and Negative
Dimensions, Phys. Rev. Lett. 43 (1979) 744 [INSPIRE].
[5] G. Parisi and N. Sourlas, Critical Behavior of Branched Polymers and the Lee-Yang Edge
Singularity, Phys. Rev. Lett. 46 (1981) 871 [INSPIRE].
[6] D.C. Brydges and J.Z. Imbrie, Branched polymers and dimensional reduction, Annals Math.
158 (2003) 1019 [math-ph/0107005].
[7] J. Cardy, Lecture on Branched Polymers and Dimensional Reduction, cond-mat/0302495.
[8] J.Z. Imbrie, Lower Critical Dimension of the Random Field Ising Model, Phys. Rev. Lett. 53
(1984) 1747 [INSPIRE].
[9] J.Z. Imbrie, The Ground State of the Three-dimensional Random Field Ising Model,
Commun. Math. Phys. 98 (1985) 145 [INSPIRE].
[10] N.G. Fytas, V. Martin-Mayor, M. Picco and N. Sourlas, Phase Transitions in Disordered
Systems: The Example of the Random-Field Ising Model in Four Dimensions, Phys. Rev.
Lett. 116 (2016) 227201 [arXiv:1605.05072].
[11] N.G. Fytas, V. Martin-Mayor, M. Picco and N. Sourlas, Restoration of Dimensional
Reduction in the Random-Field Ising Model at Five Dimensions, Phys. Rev. E 95 (2017)
042117 [arXiv:1612.06156] [INSPIRE].
[12] N.G. Fytas, V. Martı́n-Mayor, G. Parisi, M. Picco and N. Sourlas, Evidence for
Supersymmetry in the Random-Field Ising Model at D = 5, Phys. Rev. Lett. 122 (2019)
240603 [arXiv:1901.08473] [INSPIRE].

– 44 –

JHEP04(2020)090

Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited.

## PDF page 47

[13] A. Kaviraj, S. Rychkov and E. Trevisani, Random field Ising model and Parisi-Sourlas
supersymmetry II. Renormalization Group, work in progress.
[14] G. Parisi and N. Sourlas, Supersymmetric Field Theories and Stochastic Differential
Equations, Nucl. Phys. B 206 (1982) 321 [INSPIRE].
[15] B. Mcclain, A. Niemi, C. Taylor and L.C.R. Wijewardhana, Superspace, dimensional
reduction, and stochastic quantization, Nucl. Phys. B 217 (1983) 430 [INSPIRE].
[16] T. Castellani and A. Cavagna, Spin-glass theory for pedestrians, J. Stat. Mech. 2005 (2005)
P05012 [cond-mat/0505032].

[18] J.L. Cardy and A.J. Mckane, Field theoretical approach to the study of Yang-Lee and Griffiths
singularities in the randomly diluted Ising model, Nucl. Phys. B 257 (1985) 383 [INSPIRE].
[19] J.L. Cardy, Nonperturbative effects in a scalar supersymmetric THEORY, Phys. Lett. 125B
(1983) 470 [INSPIRE].
[20] A. Klein and J.F. Perez, Supersymmetry and dimensional reduction: a nonperturbative proof,
Phys. Lett. 125B (1983) 473 [INSPIRE].
[21] A. Klein, L.J. Landau and J.F. Perez, Supersymmetry and the Parisi-Sourlas dimensional
reduction: a rigorous proof, Commun. Math. Phys. 94 (1984) 459 [INSPIRE].
[22] O.V. Zaboronsky, Dimensional reduction in supersymmetric field theories, hep-th/9611157
[INSPIRE].
[23] D. Poland, S. Rychkov and A. Vichi, The Conformal Bootstrap: Theory, Numerical
Techniques and Applications, Rev. Mod. Phys. 91 (2019) 015002 [arXiv:1805.04405]
[INSPIRE].
[24] S. Hikami, Conformal Bootstrap Analysis for Single and Branched Polymers, PTEP 2018
(2018) 123I01 [arXiv:1708.03072] [INSPIRE].
[25] S. Hikami, Dimensional Reduction by Conformal Bootstrap, PTEP 2019 (2019) 083A03
[arXiv:1801.09052] [INSPIRE].
[26] V. Hussin and L.M. Nieto, From Super Lie Algebras to Supergroups: Matrix Realizations and
the Factorisation Problem, in Noncompact Lie Groups and Some of Their Applications, E.A.
Tanner and R. Wilson, eds., pp. 367–372, Springer Netherlands, Dordrecht (1994) [DOI].
[27] V.G. Kac, Lie Superalgebras, Adv. Math. 26 (1977) 8 [INSPIRE].
[28] K. Coulembier, The orthosymplectic supergroup in harmonic analysis, J. Lie Theory 23
(2013) 55 [arXiv:1202.0668].
[29] P.H. Dondi and P.D. Jarvis, Diagram and Superfield Techniques in the Classical
Superalgebras, J. Phys. A 14 (1981) 547 [INSPIRE].
[30] M.S. Costa, J. Penedones, D. Poland and S. Rychkov, Spinning Conformal Correlators,
JHEP 11 (2011) 071 [arXiv:1107.3554] [INSPIRE].
[31] M.S. Costa and T. Hansen, Conformal correlators of mixed-symmetry tensors, JHEP 02
(2015) 151 [arXiv:1411.7351] [INSPIRE].
[32] M.S. Costa, T. Hansen, J. Penedones and E. Trevisani, Projectors and seed conformal blocks
for traceless mixed-symmetry tensors, JHEP 07 (2016) 018 [arXiv:1603.05551] [INSPIRE].

– 45 –

JHEP04(2020)090

[17] J.L. Cardy, Nonperturbative aspects of supersymmetry in statistical mechanics, Physica D 15
(1985) 123.

## PDF page 48

[33] E. Lauria, M. Meineri and E. Trevisani, Spinning operators and defects in conformal field
theory, JHEP 08 (2019) 066 [arXiv:1807.02522] [INSPIRE].
[34] R.C. King, Branching Rules for Classical Lie Groups Using Tensor and Spinor Methods,
J. Phys. A 8 (1975) 429 [INSPIRE].
[35] R.J. Farmer and P.D. Jarvis, Representations of Orthosymplectic Superalgebras. 2. Young
Diagrams and Weight Space Techniques, J. Phys. A 17 (1984) 2365 [INSPIRE].
[36] A. Kupiainen and A. Niemi, Dimensional Reduction of Symmetries, Phys. Lett. 130B (1983)
380 [INSPIRE].

[38] J. Polchinski, Scale and Conformal Invariance in Quantum Field Theory, Nucl. Phys. B 303
(1988) 226 [INSPIRE].
[39] F.A. Dolan and H. Osborn, Conformal partial waves and the operator product expansion,
Nucl. Phys. B 678 (2004) 491 [hep-th/0309180] [INSPIRE].
[40] M. Hogervorst, Dimensional Reduction for Conformal Blocks, JHEP 09 (2016) 017
[arXiv:1604.08913] [INSPIRE].
[41] M. Billò, V. Gonçalves, E. Lauria and M. Meineri, Defects in conformal field theory, JHEP
04 (2016) 091 [arXiv:1601.02883] [INSPIRE].
[42] J.L. Cardy, Anisotropic Corrections to Correlation Functions in Finite Size Systems, Nucl.
Phys. B 290 (1987) 355 [INSPIRE].
[43] D. Simmons-Duffin, The Conformal Bootstrap, in Proceedings, Theoretical Advanced Study
Institute in Elementary Particle Physics: New Frontiers in Fields and Strings (TASI 2015),
Boulder, CO, U.S.A., 1–26 June 2015, pp. 1–74 (2017) [DOI] [arXiv:1602.07982] [INSPIRE].
[44] F.A. Dolan and H. Osborn, Conformal four point functions and the operator product
expansion, Nucl. Phys. B 599 (2001) 459 [hep-th/0011040] [INSPIRE].
[45] J. Penedones, E. Trevisani and M. Yamazaki, Recursion Relations for Conformal Blocks,
JHEP 09 (2016) 070 [arXiv:1509.00428] [INSPIRE].
[46] F. Kos, D. Poland and D. Simmons-Duffin, Bootstrapping the O(N ) vector models, JHEP 06
(2014) 091 [arXiv:1307.6856] [INSPIRE].
[47] M. Hogervorst and S. Rychkov, Radial Coordinates for Conformal Blocks, Phys. Rev. D 87
(2013) 106004 [arXiv:1303.1111] [INSPIRE].
[48] S. El-Showk, M.F. Paulos, D. Poland, S. Rychkov, D. Simmons-Duffin and A. Vichi, Solving
the 3D Ising Model with the Conformal Bootstrap, Phys. Rev. D 86 (2012) 025022
[arXiv:1203.6064] [INSPIRE].
[49] M. Hogervorst, H. Osborn and S. Rychkov, Diagonal Limit for Conformal Blocks in d
Dimensions, JHEP 08 (2013) 014 [arXiv:1305.1321] [INSPIRE].
[50] F.A. Dolan and H. Osborn, Conformal Partial Waves: Further Mathematical Results,
arXiv:1108.6194 [INSPIRE].
[51] H. Osborn. personal communication.
[52] Z. Komargodski and D. Simmons-Duffin, The Random-Bond Ising Model in 2.01 and 3
Dimensions, J. Phys. A 50 (2017) 154001 [arXiv:1603.04444] [INSPIRE].

– 46 –

JHEP04(2020)090

[37] E. Witten, Notes On Supermanifolds and Integration, arXiv:1209.2199 [INSPIRE].

## PDF page 49

[53] C. Cordova, T.T. Dumitrescu and K. Intriligator, Multiplets of Superconformal Symmetry in
Diverse Dimensions, JHEP 03 (2019) 163 [arXiv:1612.00809] [INSPIRE].
[54] P. Arvidsson, Manifest superconformal covariance in six-dimensional (2, 0) theory, JHEP 03
(2006) 076 [hep-th/0602193] [INSPIRE].
[55] C. Beem, M. Lemos, P. Liendo, W. Peelaers, L. Rastelli and B.C. van Rees, Infinite Chiral
Symmetry in Four Dimensions, Commun. Math. Phys. 336 (2015) 1359 [arXiv:1312.5344]
[INSPIRE].
[56] C. Beem, L. Rastelli and B.C. van Rees, W symmetry in six dimensions, JHEP 05 (2015)
017 [arXiv:1404.1079] [INSPIRE].

– 47 –

JHEP04(2020)090

[57] J. Zinn-Justin, Quantum Field Theory and Critical Phenomena, 4th edition, Oxford
University Press (2002).
