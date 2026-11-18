Source: see manifest row of the PDF
PDF sha256: a625e63c816f8f7a4a49280446aa347776362ca7c3a565a33515a38e33d3b070
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of van_spaendonck_2024_exact_instanton_transseries_for_quantum_mechanics.pdf

Transcription of `van_spaendonck_2024_exact_instanton_transseries_for_quantum_mechanics.pdf` in this directory, 51 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-51 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SciPost Phys. 16, 103 (2024)

Exact instanton transseries for quantum mechanics
Alexander van Spaendonck⋆ and Marcel Vonk†
Institute of Physics, University of Amsterdam, Science Park 904,
1090 GL Amsterdam, The Netherlands
⋆ a.b.n.vanspaendonck@uva.nl ,

† m.l.vonk@uva.nl

Abstract
We calculate the instanton corrections to energy spectra of one-dimensional quantum
mechanical oscillators to all orders and unify them in a closed form transseries description. Using alien calculus, we clarify the resurgent structure of these transseries and
demonstrate two approaches in which the Stokes constants can be derived. As a result,
we formulate a minimal one-parameter transseries for the natural nonperturbative extension to the perturbative energy, which captures the Stokes phenomenon in a single
stroke. We derive these results in three models: quantum oscillators with cubic, symmetric double well and cosine potentials. In the latter two examples, we find that the
resulting full transseries for the energy has a more convoluted structure that we can
factorise in terms of a minimal and a median transseries. For the cosine potential we
briefly discuss this more complicated transseries structure in conjunction with topology
and the concept of the resurgence triangle.
Copyright A. van Spaendonck and M. Vonk.
This work is licensed under the Creative Commons
Attribution 4.0 International License.
Published by the SciPost Foundation.

Received 13-11-2023
Accepted 25-03-2024
Check for
updates
Published 12-04-2024
doi:10.21468/SciPostPhys.16.4.103

Contents
1 Introduction

2

2 Preliminaries
2.1 Resurgence and alien calculus
2.2 All-orders WKB and the quantum prepotential

4
4
7

3 The cubic oscillator
3.1 Iterative solution to the exact quantisation condition
3.2 Deriving exact multi-instanton expressions
3.3 Stokes phenomenon through the PNP relation
3.4 Stokes phenomenon from DDP formula
3.5 On the quantum prepotential transseries

12
13
16
19
22
23

4 The symmetric double well potential
4.1 The full transseries
4.2 The minimal transseries
4.3 The full transseries as a sum of minimal transseries

25
27
30
33

1

## PDF page 2

SciPost Phys. 16, 103 (2024)

5 The cosine potential

35

6 Conclusion

40

A On the PNP relation

41

B Stokes phenomena for the quantum prepotential from DDP

44

C Median resummation

46

References

48

1

Introduction

It has been tested and verified in several quantum physical settings, that perturbative series
encode information about many – but not necessarily all – nonperturbative effects. This information can be extracted from the nonperturbative ambiguities that arise as we attempt to
resum the generally divergent perturbative series into a well-defined and smooth function.
The mathematical tool to extract nonperturbative information from asymptotically divergent series is resurgence [1]. In the realm of ODE’s, where the theory of resurgence was
conceived, there is a very clear understanding of why these ambiguities arise and how to deal
with them. There, resurgence tells us that both perturbative and nonperturbative asympotics
should be unified in a single object called a transseries. These transseries and their resurgent
structure, expressed in the language of alien calculus, illustrate how all ambiguities arising
from the resummation procedure are eventually cancelled, leading to a well-defined answer
where the only remaining ambiguities are related to boundary conditions of the ODE.
The nonperturbative treatment of one-dimensional quantum mechanical oscillators suggests [2] that for these, the perturbative energy spectrum together with all its instanton corrections1 should also be unified in a single transseries expression. The modern approach to
calculate these instanton corrections is through the formulation of exact quantisation conditions, which were derived by Zinn-Justin [3] using instanton calculus and by Voros [4, 5] and
subsequently Delabaere, Dillinger and Pham [6] using exact WKB techniques. Another approach for obtaining these exact quantisation conditions is the uniform WKB method [–10].
As is the case for ODEs, nonperturbative effects in quantum mechanical problems are often encoded in the large order behaviour of the perturbative coefficients. The large order behaviour
of the perturbative coefficients in quantum mechanics models was initially studied by Bender
and Wu in [11], and subsequent works have explored its intricate relation to instantons and
nonperturbative ambiguities, e.g. [12–15] and have employed various tools from resurgence
to study these nonperturbative aspects even further, e.g. [16, 17].
In this work our goal will be to go beyond the status quo and elucidate the structure of
transseries in quantum mechanics. We will follow the approach of Álvarez and Casares [, 10]
for obtaining the instanton corrections to the energy of the quantum states. We clarify some
details of this method and extend it to all nonperturbative orders in closed form, formulating
a complete transseries expression for the energy of the states. We will then advocate that
the natural transseries extension to the perturbative energy E takes the form of the following
1
A remark on terminology: in this paper, following the conventions in the resurgence literature, we use the term
‘instanton’ for exact instanton solutions as well as for nonperturbative effects related to quasi-instantons. Similarly,
we will describe both of these effects as ‘saddle point contributions’, even though strictly speaking quasi-instantons
do not correspond to exact saddle points.

2

## PDF page 3

SciPost Phys. 16, 103 (2024)

generic one-parameter transseries:
Ê(t, σ; ħ
h) = E + ħ
h

∞
n−1
∑∑

un,m σ

n=1 m=0

m+1

 


∂ m ∂ E − n tD
e ħh
ħ
h
.
∂t
∂t

(1)

The details of this equation will be clarified in the core of the paper, but the most important
thing to note is that this equation expresses the energy transseries Ê in terms of purely perturbative quantities E(t; ħ
h) and t D (t; ħ
h), a transseries parameter σ, and some model specific
coefficients un,m for which we will derive a closed form expression. We will demonstrate in
detail how alien calculus encodes the Stokes phenomenon of (1) and will derive its Stokes
constants in two different ways.
Our approach is strongly influenced by a recent line of work investigating the close connection between quantum mechanical oscillators and topological strings. It has been argued
in [18] that quantum periods, which are the essential building blocks of the aforementioned
quantisation conditions, are governed by the holomorphic anomaly equations [19] of the refined topological string in the Nekrasov-Shatashvili background [20]. Subsequently, building
on ideas from [21, 22], the nonperturbative solution to these holomorphic anomaly equations
was studied in [23] and finally solved for in exact form in [24] – also in the so-called selfdual
background [25]. This nonperturbative solution, that appears in the form of a transseries for
the quantum prepotential or Nekrasov-Shatashvili free energy, relates directly to the ordinary
energy E through a relation known as the PNP relation. We will exploit this relation, allowing
us to compare to, and utilise the results of [24] for our goals.
To develop and illustrate our ideas, we will consider three models: quantum mechanics
in a cubic, a symmetric double well and a cosine potential. Each of these will add an extra
layer of complexity to the story and will help us get a deeper understanding of the role that
transeries play in quantum mechanics. The cubic will act as a warm-up example to introduce
our techniques and illustrate the core notions of our work that lead to (1), an object that we call
the minimal resurgent transseries. The double well potential has a more elaborate transseries
structure that factorises (in a way we will make precise) in terms of the minimal transseries
and another object that we call the median transseries. Finally, we discuss the cosine potential
where the energy levels at the nonperturbative level split into bands. Each band consists of a
continuous spectrum of energies that are characterised by an angle θ . The dependence of the
instantons on θ then allows us to identify topological sectors in the model and explain how our
transseries structure relates to the concept of a ‘resurgence triangle’ as described in [26, 27].
This paper is organised as follows. In section 2 we introduce the most important concepts
and tools of resurgence, alien calculus and the all-orders WKB method. In section 3 we then
start with a study of the cubic oscillator: we introduce the closed form expression for the
nonperturbative energy spectrum, illustrate two ways in which the Stokes phenomenon of the
transseries can be decoded, including a computation of the exact values for the Stokes constants, and arrive at the generic one-parameter transseries structure (1). In section 4 we then
move to the double well potential and use the same techniques to derive its energy transseries.
We clarify its resurgent structure and illustrate how it factorises in terms of a minimal and a
median transseries. In section 5 we then adress the cosine potential, for which we repeat the
procedure for obtaining the full energy transseries and comment on its topological structure
in comparison with the resurgence triangle. Finally, in section 6 we state our conclusions, and
three appendices are included in which we derive the PNP relation (A), discuss the Stokes
phenomenon of the quantum prepotential (B) and elaborate more on median resummation
and the median transseries (C).

3

## PDF page 4

SciPost Phys. 16, 103 (2024)

Figure 1: The Borel plane of B ϕ: on the left both Sθ + ϕ and Sθ − ϕ, in the middle their
difference discθ ϕ(x) and on the right also the discontinuity, but now decomposed
in Hankel contours Hω .

2

Preliminaries

In this section we introduce the most important tools and concepts that are necessary for
the calculations that will follow in subsequent sections. This section is subdivided in two
subsections discussing some basics of resurgence and alien calculus and subsequently the allorders WKB method and the transseries solution to the holomorphic anomaly equation.

2.1

Resurgence and alien calculus

Let us recall the aspects of resurgence (originally introduced in Écalle’s seminal work [1]) that
are most relevant to us, and mention some essential tools and notation that will be important
in the forthcoming calculations. For a thorough introduction to the topic of resurgence from
a physics point of view we recommend reading [28–30], and for the more mathematically
inclined reader we recommend [31, 32].
∑∞
We start by considering a formal power series ϕ(x) = n=0 an x n whose coefficients an
diverge factorially: an ∼ n!. Its Borel transform is defined as

B ϕ(s) =

∞
∑
a
n=0

n+1 n

n!

s .

(2)

It allows us to resum the asymptotic series ϕ(x) – minus its constant term, which we can add
again at the end of the procedure – using the Borel resummation Sθ :

Sθ ϕ =

∫ eiθ ∞

B ϕ(s) e−s/x ds ,

(3)

0

where the integration contour runs along a straight line from zero to infinity under an angle
θ in the complex s-plane, which we will henceforth call the Borel plane. Here, one assumes
that the formal series (2) can be summed and analytically continued into a function of s,
so that the integral (3) makes sense. In general, the function B ϕ(s) will have a number of
isolated singularities in the Borel plane. Whenever one or more of these singularities lie on the
integration contour, we call this ray a Stokes line and we find that our resummation procedure
is ill-defined. The resolution to this problem is to slightly deform the contour either above
(Sθ + ) or below the singularities (Sθ − ), leading to two distinct resummations, as depicted in
the left graph of figure 1. The difference between these lateral Borel summations constitutes
the discontinuity:
discθ ϕ(x) = Sθ + ϕ(x) − Sθ − ϕ(x) .
(4)
4

## PDF page 5

SciPost Phys. 16, 103 (2024)

The difference between these two quantities can be computed by integrating around all the
singularities that lie on the ray with angle θ , as shown in figure 1 in the middle. Let Ωθ be the
collection of indices2 that label the singularities that lie along such a ray in the Borel plane of
B [ϕ](s). That is, for every ω ∈ Ωθ , there is a singularity located at Aω with arg(Aω ) = θ . The
contour above can then be decomposed in terms of multiple Hankel contours, each of them
‘grabbing’ a single singularity labeled by one or more ω ∈ Ωθ , as shown in figure 1 on the
right. For many resurgent functions, it turns out that the Borel transform (2), expanded near
each of the singularities Aω , behaves as

B ϕ(s) ≃

Sω aω,0
2πi(s − Aω )

+

Sω log(s − Aω )
B [ϕω ](s − Aω ) + regular.
2πi

(5)

Here aω,0 and Sω are constants and B ϕω (s) is an analytic function. We can then add up the
contributions from the different Hankel contours to calculate the discontinuity, and obtain
∑
discθ ϕ(x) =
Sω e−Aω /x Sθ − ϕω (x) .
(6)
ω∈Ωθ

∑∞
The ϕω (x) = n=0 aω,n x n – where the constant term comes from the leading term in (5) –
are then new diverging formal power series that have ‘resurged’ from the Borel plane, and
the Sω are known as Stokes constants.3 Note that the above equation concerns resummed
power series, that is: Functions. The same phenomenon can also be expressed at the level
of asymptotic expansions, by introducing the Stokes automorphism, which is defined by the
relation
Sθ + = Sθ − ◦ Sθ .
(7)
It essentially tells us what the correct way is to analytically continue an asymptotic expansion
across a Stokes line. Using this definition, we can rewrite equation (6) in terms of asymptotics:
∑
Sθ ϕ(x) = ϕ(x) +
Sω ϕω (x)e−Aω /x .
(8)
ω∈Ωθ

The appearance of the additional nonperturbative contributions on the right hand side, encoded in the transmonomials e−Aω /x , is called the Stokes phenomenon. The above discussion
suggests that to study Sθ , we should extend the notion of an asymptotic expansion from a
power series ϕ(x) to a transseries:
∑
ϕ̂( ⃗
σ, x) = ϕ(x) +
σω ϕω (x)e−Aω /x .
(9)
ω∈Ωθ

A remark regarding notation: in this paper asymptotic quantities without a hat are ordinary
power series whereas those with a hat are transseries. The σω in the above expression are
called transseries parameters and we have collected them on the left hand side in a single
vector σ
⃗ for convenience.4 By introducing these parameters we have constructed a family of
2
We choose Ωθ to be a set of indices rather than a set of singularities since, as we will see in more detail later,
several different indices ω may correspond to the same singularity location. This will imply that a sector with a
certain nonperturbative ‘weight’ e−Aω /x actually gets multiplied by a sum of several different asymptotic series.
3
In some of the literature, these constants are called Borel residues. The Stokes constants are then a set of
equivalent constants that determine the discontinuity, usually defined by the bridge equations of resurgence. In
many physical problems however, we do not have such a bridge equation and we call the constants Sω Stokes
constants instead.
4
Often, it is not necessary to introduce an independent transseries parameter σω for every ω ∈ Ωθ . For example,
in solutions to nonlinear ODEs, one often has that σnA = (σA)n . For now, we will work with the generic case where
all transseries parameters are independent, but in our examples we will generally only see a single independent
transseries parameter σ appear.

5

## PDF page 6

SciPost Phys. 16, 103 (2024)

transseries expressions, and we then interpret the Stokes automorphism as an operation acting
on this family:
S0 ϕ̂( ⃗
σ, x) = ϕ̂(g( ⃗
σ), x) .
(10)
This provides us with a qualitative picture of the Stokes phenomenon. For a more quantitative
understanding, we need to deduce the exact mapping g( ⃗
σ) on the transseries parameter space.
This is in general a complicated problem, which we studied earlier for e.g. the Painlevé I ODE
in [33]. In order to achieve this in the present setting, we need to introduce the notion of alien
calculus [1], which introduces a new set of derivative operators ∆Aω called alien derivatives.
These operators are labeled by the location Aω of the singularities in the Borel plane and act
on formal power series producing new formal power series:
∆Aω : C[[x]] → C[[x]] .

(11)

These operators turn out to have some special properties. First of all, they satisfy the Leibniz
rule when acting on a product of formal power series. Secondly, the Stokes automorphism can
be decomposed in terms of these new operators as follows:
∑


Sθ = exp

ω

e−Aω /x ∆Aω

.

(12)

For the third property, it is convenient to introduce the pointed alien derivative
˙
∆Aω ≡ e−Aω /x ∆Aω .

(13)

This operator has the very useful property that it commutes with differentiation with respect
to the expansion variable x:


∂
˙
= 0.
(14)
∆Aω ,
∂x
With the language of alien calculus, we can now define the minimal resurgent structure [34]
associated to the original series ϕ(x) and the angle5 θ :

B(ϕ,θ ) = { ϕω (x) | ω ∈ Ωθ } .

(15)

Loosely speaking, it contains all the formal power series that resurge from the series ϕ(x).
More precisely, using the alien derivatives we can define B(ϕ,θ ) as the smallest set of power
series that is closed under the Stokes automorphism Sθ and that includes ϕ(x). That is, for
arg(A) = θ and ω, ω′ ∈ Ωθ , we have
∑
A
∆A ϕω =
cωω
(16)
′ ϕω ′ ,
ω′

A
where the cωω
′ are some constants that we can express in terms of the Stokes constants. In
the case where all the formal power series ϕω in (9) reside in the minimal resurgent structure
(15) – therefore making the transseries itself ‘closed’ – we call the corresponding transseries a
minimal resurgent transseries. In the examples that we study in this paper, we will encounter
such minimal transseries, but also transseries which contain additional ‘disconnected’ power
series which make the transseries no longer minimal.
Lastly, in this paper we will mostly be concerned with formal power series and transseries
whose coefficients depend on some other parameter, say y – e.g.

ϕ( y; x) =

∞
∑

an ( y) x n .

n=0
5

We add the angle to the definition so that we can focus on a single Stokes transition.

6

(17)

## PDF page 7

SciPost Phys. 16, 103 (2024)

The study of such objects goes under the name ∑
of parametric resurgence. When we now substi∞
tute y itself with a formal power series φ(x) = n=0 bn x n , we obtain a completely new power
series6 χ(x) = ϕ(φ(x); x) whose resurgence properties might seem unknown. However, in
terms of alien calculus, the substitution can be understood very well and for the pointed alien
derivatives one has the following chain rule of [17] which reads

˙
∆A χ(x) = ˙
∆A ϕ ( y; x)

y=φ(x)

+

∂ϕ
(φ(x); x) ˙
∆A φ(x) .
∂y

(18)

One can think of this rule as the ‘alien analogue’ of the chain rule in ordinary calculus.

2.2

All-orders WKB and the quantum prepotential

We will be interested in one-dimensional quantum mechanics problems described by the timeindependent Schrödinger equation
ħ
h2 ′′
ψ (x) + V (x)ψ(x) = E ψ(x) .
2
Solutions to this equation are constructed via the all-orders WKB Ansatz [35]

 ∫ x
i
′
′
S(x ; ħ
h) dx ,
ψ(x) = exp
ħ
h
∑∞
where S(x; ħ
h) = n=0 pn (x) ħ
hn is a solution to the Riccati equation
−

S 2 − iħ
h

∂S
= 2(E − V (x)) .
∂x

(19)

(20)

(21)

The solution for the leading piece p = p0 (x) of the Riccati solution S(x; ħ
h) defines a Riemann
surface Σ that we call the WKB curve:
Σ : p2 = 2E − 2V (x) .

(22)

In this paper we will consider the cubic, double well and cosine potentials which effectively
have an underlying genus one elliptic WKB curve (see e.g. [36]). Most importantly, we can
integrate the Riccati solution S(x; ħ
h) along nontrivial cycles γ ∈ H1 (Σ) in the WKB curve to
obtain quantum periods
∮
Πγ =

S(x; ħ
h) dx .

(23)

γ

The solution to the Riccati equation can be separated into even and odd parts:
S(x; ħ
h) = S even (x; ħ
h) + S odd (x; ħ
h) ,

(24)

where the even and odd parts contain only even or odd powers of ħ
h, respectively.7 One can
then show that the odd part is a total derivative and that its contribution to the quantum
This substitution does not necessarily produce a well-defined power series. The series ϕ( y; x) therefore needs
to satisfy some mild conditions explained [17].
7
The Ricatti
equation has two possible solutions S (±) determined by the sign of the initial term
p
(±)
p0 (x) = ± 2E − 2V (x). Formally, the even and odd solutions are then defined as
6

S even =

S (+) + S (−)
,
2

and

S odd =

S (+) − S (−)
,
2

which in the absence of quantum corrections to the potential imply the above-mentioned separation in even and
odd powers of ħ
h.

7

## PDF page 8

SciPost Phys. 16, 103 (2024)

periods vanishes. As a consequence, we can expand (23) asymptotically as


∞ ∮
∞
∑
∑
2n
Πγ (E; ħ
h) =
p2n (x, E) dx ħ
h =
Πγ,nħ
h2n .
n=0

γ

(25)

n=0

If we fix the energy E for a moment, one can check that the coefficients of the quantum periods
grow double factorially:
Πγ,n ∼ (2n)! ,
(26)
and hence we need to Borel resum these asymptotic expansions in order to produce sensible
functions.
The analytically continued Borel transforms of the quantum periods have singularities in
the Borel plane. These singularities organise themselves on rays across which the Stokes automorphism Sθ is given by the Delabaere-Dillinger-Pham formula [16, 17] (see also appendix A
of [37]). To state this formula, we first need to define the Voros symbol
i

Vγ = e ħh Πγ (E;ħh) .

(27)

Now, let us consider the case in which for a given angle θ = arg(ħ
h) there is one8 cycle γ′ whose
i
associated quantum period satisfies ħh Πγ′ ,0 ∈ R<0 . If the cycles γ and γ′ intersect, then the Borel
transform of the quantum period Πγ has a ray with singularities on it along the angle θ in its
Borel plane. The Delabaere-Dillinger-Pham formula now tells us that across that Stokes ray,
the Stokes automorphism for the associated Voros symbol Vγ is given by

Sθ Vγ = Vγ 1 + Vγ′

〈γ′ ,γ〉

,

(28)

where 〈γ, γ′ 〉 is the intersection number of the two cycles.
Since all the examples in this paper will involve an underlying genus 1 curve, we have
a basis of two independent cycles γA, γB ∈ H1 (Σ). In general, our potentials will be real,
and following standard conventions we denote cycles around minima of the potential, where
particles can follow classical trajectories, as A-cycles, while labeling ‘tunneling’ cycles around
maxima as B-cycles. In what follows, we will speak of the quantum A-period, which is defined
as
∞
∑
1
t(E; ħ
h) =
t n (E)ħ
h2n =
Πγ (E; ħ
h) .
(29)
2π A
n=0
There will also be a dual period or quantum B-period that we define as
t D (E; ħ
h) =

∞
∑

t D,n (E)ħ
h2n = −iΠγB (E; ħ
h) .

(30)

n=0

The numerical prefactors in these definitions are conventional, and chosen to agree with expressions in the literature. As a consequence of these prefactors, in the quantum mechanical
problems that we study here, where all turning points x i defined by V (x i ) = E lie on the real
axis, the t 0 and t D,0 will be real and positive. Figure 2 gives an impression of the respective
Borel planes and shows that the quantum A-period t is non-Borel summable when ħ
h is real,
whereas the dual quantum period is non-Borel summable when ħ
h is purely imaginary. As a
consequence, the Delabaere-Dillinger-Pham formula tells us how the quantum periods jump
8

In general, there may be multiple cycles γi satisfying this condition. In that case the DDP formula generalises to
∏
〈γi ,γ〉
Sθ Vγ = Vγ
1 + Vγi
.
i

8

## PDF page 9

SciPost Phys. 16, 103 (2024)

Figure 2: A sketch of the Borel planes of the quantum A-period t(E; ħ
h) on the left
and the quantum B-period t D (E; ħ
h) on the right. The singularities are evenly spaced
and continue indefinitely.
across the four Stokes rays located at arg(ħ
h) ∈ π2 Z. For example, along the rays arg(ħ
h) = 0
and arg(ħ
h) = π2 the asymptotic expansions of the quantum periods jump in the following way:

ħ
h
log 1 + e−t D (E;ħh) ,
2πi

π
h) = t D (E; ħ
h) + 〈γA, γB 〉 ħ
h log 1 + e−2πit(E;ħh) ,
S 2 t D (E; ħ

S0 t(E; ħ
h) = t(E; ħ
h) + 〈γB , γA〉

for arg(ħ
h) = 0 ,
for arg(ħ
h) =

π
.
2

(31)

In all of our examples we pick orientations of γA, γB such that 〈γA, γB 〉 = −〈γB , γA〉 = 1.
One can invert the quantum A-period to express the energy E as a formal power series in
ħ
h with coefficients depending on t:
E(t; ħ
h) =

∞
∑

En (t) ħ
h2n .

(32)

n=0

The coefficient functions En (t) are then determined by solving E(t(E; ħ
h); ħ
h) = E. They also
grow double factorially, just like the Πγ,n in (26). In the topological string theory literature,
the above series is often called the quantum mirror map. There is also the classical mirror map,
which is given by the leading piece E0 (t) and which is the inverse of the classical period t 0 (E).
The dual period t D (E; ħ
h) also defines a quantum prepotential or Nekrasov-Shatashvili free
9
energy [20]
∞
∑
F (t; ħ
h) =
Fn (t) ħ
h2n .
(33)
n=0

For our genus 1 examples, up to an integration constant this quantity is defined by the equation
t D (t; ħ
h) =

∂
F (t; ħ
h) .
∂t

(34)

Note that on the left hand side of this equation we abuse the notation slightly: the original
dual quantum period t D defined in (30) is a function of (E, ħ
h) which relates to t D (t; ħ
h) shown
here in the following way:
t D (t; ħ
h) ≡ t D (E(t; ħ
h); ħ
h) .
(35)
9

In this work we will mostly use the term quantum prepotential, for two good reasons: First of all we are
essentially studying the quantisation of elliptic curves and our discussion will be quite remote from supersymmetric
gauge theory context that the story connects to. Secondly, when we discuss the PNP relation in upcoming sections
it might be confusing to speak of both of the energy E and the NS free energy F .

9

## PDF page 10

SciPost Phys. 16, 103 (2024)

On the right hand side of this expression we see the original definition (30) of the quantum
dual period with the argument E substituted by the quantum mirror map E(t; ħ
h), therefore
making it a composition of series in ħ
h. If we switch back to the independent variables (E, ħ
h),
then equation (34) becomes
∂
t D (E; ħ
h) =
F (t(E; ħ
h); ħ
h) .
(36)
∂t
Note moreover that the definition of the quantum prepotential involves a choice of frame:
we can also exchange t and t D in (34) leading to a different quantum prepotential F D defined
by
∂
t(t D ; ħ
h) =
F D (t D ; ħ
h) ,
(37)
∂ tD
where now (t D , ħ
h) are the independent variables. In fact, one can choose two arbitrary Zlinear combinations of cycles as new A- and B-cycles, as long as they form a symplectic basis
for the space of all cycles, and define an associated quantum prepotential – but all of the
quantum prepotentials one obtains in this way can in the end be related to one another using
an appropriate Legendre transformation.
The quantum prepotential turns out to be a factorially divergent power series and is therefore a suitable object to study using resurgence. Let us introduce – again by a slight abuse
of notation – the quantum prepotential F (E; ħ
h), which relates to our quantum prepotential
F (t; ħ
h) in (33) as
F (E; ħ
h) = F (t 0 (E); ħ
h) .
(38)
The transseries extension to this series and its resurgent structure were studied in [24], and
here we briefly recall some key aspects that will be necessary for what is to come.10 The
Borel transform of the quantum prepotential F (E; ħ
h) will have rays along which evenly spaced
singularities lie. Let us take such a ray where the singularities lie at nA with n ∈ Z>0 . Then a
transseries extension of F which includes all the associated nonperturbative sectors will have
the general form
∞
∑
F̂ =
F (n) ,
where
F (n) ∼ e−nA/ħh .
(39)
n=0

Here, the perturbative quantum prepotential F is encoded in F (0) = F − F0 , where following standard conventions the leading term is subtracted to obtain nicer-looking holomorphic
anomaly equations. The first three nonperturbative sectors [24] have the form
F (1) = τ1 e−G /ħh ,


τ
DG
F (2) = − 2 + τ21 2 e−2G /ħh ,
4
2ħ
h



2
τ3
DG
D2 G
(3)
3 (DG )
F =
− τ1 τ2 2 + τ1
−
e−3G /ħh .
9
2ħ
h4
2ħ
h
6ħ
h3

(40)

Here, the τk are yet undetermined constants that we will interpret as transseries parameters.
The operator D and the quantity G are quite subtle objects that depend on which Stokes line
we are studying. For a complete and thorough explanation we refer to [23–25], but for our
purposes it suffices to know that G has the generic form

G = A + D F (0) ,

with A = α

∂ F0
+ β t0 + γ ,
∂t

(41)

10
The key result that we are after is the action of the alien derivatives on the perturbative quantum prepotential
F (E; ħ
h), shown in (46). For the purpose of understanding the main results of the present paper, the finer details
of the quantum prepotential transeries F̂ presented here can be skipped upon first reading.

10

## PDF page 11

SciPost Phys. 16, 103 (2024)

where α, β and γ are constants that express the location A of the first singularity in the
Borel plane in terms of the classical A- and B-periods. In our 1d quantum mechanical models,
there will only be two relevant frames to consider: the first, and for us most important frame
is relevant for the Stokes transition along the real ħ
h-axis. It gives rise to nonperturbative
corrections to the quantum prepotential with

G=α

∂F
,
∂t

and D = α

∂
.
∂t

(42)

Secondly, as we mentioned there is a Stokes phenomenon across the imaginary ħ
h-axis giving
rise to nonperturbative corrections to the quantum prepotential with

G = β t0 ,

and

D = 0.

(43)

In the examples that were studied numerically in [24], the Stokes constants Sω (see (5))
scale with ħ
h2 . To remove this scaling we will slightly modify their normalisation by shifting
τk → ħ
h2 τk . In this new normalisation, the first three transseries sectors therefore take the
form
ħ
h−2 F (1) = τ1 e−G /ħh ,


τ2 1 2
−2 (2)
ħ
h F = −
+ τ1 DG e−2G /ħh ,
(44)
4
2



τ3 1
1
ħ
h
ħ
h−2 F (3) =
− τ1 τ2 DG + τ31
(DG )2 − D2 G e−3G /ħh .
9
2
2
6
In appendix B, we will also need the frame in which D = 0, where the nonperturbative sectors
reduce to
(−1)n+1
ħ
h−2 F (n) =
τn e−2πinA/ħh .
(45)
n2
Note that in the latter frame, the transmonomials contain only the classical period G = A =β t 0 ,
and so the nonperturbative sectors are not ‘dressed’ with asymptotic series of perturbative
fluctuations in ħ
h.
Now we arrive at the last and most important property of the quantum prepotential that
we need: it was proposed in [24] that the pointed alien derivatives (see (13)) should act on
the perturbative quantum prepotential as11
˙ l A F (0) = Sl A F (l) ,
∆
l

(46)

where the Sl A are Stokes constants that are independent of ħ
h, and
(l)

Fl

=

(−1)l+1 2 −l G /ħh
ħ
h e
,
l2

(47)

is simply F (l) with τl = 1 and all other τk for k ̸= l set to zero. Subsequently, one can
straightforwardly check that
˙ l A G = Sl Aħ
∆
h

(−1)l
DG e−l G /ħh ,
l

(48)

˙ l A commute. Given equation (48) and the fact that all instanusing the fact that D and ∆
ton corrections to the quantum prepotential are functions of G , all pointed alien derivatives
commute with eachother, i.e.
˙ A′ ] f (G ) = 0 ,
[˙
∆A , ∆
(49)
11

This expression is adjusted to our normalisation (44).

11

## PDF page 12

SciPost Phys. 16, 103 (2024)

for an arbitrary function f (G ).
Having completed our brief reviews of resurgence, the all-orders WKB method and the
quantum prepotential, we are now ready to study the three quantum mechanical problems of
the forthcoming sections. The techniques and concepts laid out in this subsection, together
with a few more tools that we will introduce along the way, allow us to produce complete
nonperturbative transseries solutions for the energy spectrum. By casting these structures
in the language of alien calculus we can then obtain a deeper understanding of the Stokes
phenomenon for energy spectra in quantum mechanics. As we will see shortly, these transseries
are much more complicated than their cousins in the realm of ODEs. It is for this reason that
we start with the example of the cubic oscillator, which from a resurgence point of view turns
out to be the simplest of the three models, before advancing to the symmetric double well and
cosine potentials.

3

The cubic oscillator

In order to demonstrate our approach we start with the cubic oscillator. This one-dimensional
quantum mechanical model describes a particle in a cubic potential:
V (x) =

x2
− x3 .
2

(50)

Although there is no stable vacuum in this model, the Schrödinger operator Ĥ = p̂2 +V (x̂) does
admit a discrete spectrum of resonances when we impose Gamow-Siegert boundary conditions
[38, 39]: a decaying wave function as x goes to −∞ and a purely outgoing wave as x goes to
+∞. When computing the spectrum of energies of these resonances – which are asymptotic
divergent series in ħ
h – we learn that they are non-Borel summable, i.e. there are singularities
on the positive real axis in the Borel plane, making the resummation procedure ambiguous.
One way to circumvent this problem is to slightly deform ħ
h by giving it a small phase, moving
the Borel singularities away from the real axis and rendering the series Borel-summable.
1
If we assume that the energy E lies within the range 0 < E < 54
, then all three turning
points lie on the real axis, giving rise to a natural choice for the quantum A-period t(E; ħ
h)
and the quantum B-period t D (E; ħ
h), as displayed in figure 3. Using various techniques like
e.g. instanton calculus [40], the Voros-Silverstone connection formula [5, 41] or the uniform
WKB method [, ], one can derive an exact quantisation condition: A functional relation, expressed in terms of the quantum periods, that allows us to compute the full nonperturbative
energy spectrum of the resonances. More precisely, the quantisation condition fixes the value
t that the quantum A-period can attain in terms of an integer N , and therefore quantises the
spectrum E(t; ħ
h), which we obtain after inverting the A-period. Regardless of the choice of
computational method, the resulting quantisation condition will be ambiguous. When we
slightly deform ħ
h as explained above, the ambiguity is resolved and as a result we have two
quantisation conditions, one for Im(ħ
h) < 0 and one for Im(ħ
h) > 0. This therefore leads to two
distinct asympotic expansions for the energy, which after resummation should be identical in
the limit that the phase of ħ
h goes to zero. Understanding the Stokes transition that takes us
from the former (Im(ħ
h) < 0) to the latter expansion (Im(ħ
h) > 0) will be the main objective of
this section.

12

## PDF page 13

SciPost Phys. 16, 103 (2024)

Figure 3: On the left the cubic potential (50) and on the right the same three turning
points in the complex x-plane, with corresponding cycles γA and γB that one integrates over to obtain the A- and B-periods. The black wavy lines are square root
branch cuts.

3.1

Iterative solution to the exact quantisation condition

In the case of the cubic oscillator, using the techniques mentioned above one derives the following two quantisation conditions for Im(ħ
h) < 0 and Im(ħ
h) > 0 respectively:
D− (E; ħ
h) = 1 + e2πit(E;ħh)/ħh + e−t D (E;ħh)/ħh = 0 ,
D+ (E; ħ
h) = 1 + e2πit(E;ħh)/ħh = 0 .

(51)

These conditions lead to two nonperturbatively different asymptotic solutions for the energy
spectrum, whose difference should be accounted for by the Stokes phenomenon. The functions
D+ and D− used in the quantisation conditions defined above are functions of the independent
variables (E; ħ
h). We now wish to change variables to (t; ħ
h). This is achieved by using the
quantum mirror map E(t; ħ
h) to substitute E, leading to conditions that we can now write as
D− (t; ħ
h) = 1 + e2πit/ħh + e−t D (t;ħh)/ħh = 0 ,
D+ (t; ħ
h) = 1 + e2πit/ħh = 0 .

(52)

Note that now t is an unknown which, after picking one of the two conditions, must be solved
for. The quantisation condition D+ (t; ħ
h) = 0 can readily be solved and yields


1
t =ħ
h N+
,
(53)
2
for some nonnegative12 integer N . This condition is called the perturbative quantisation condition, as it gives rise to the perturbative energy spectrum.
To better understand this statement, let us briefly digress from the main story and illustrate
how (53) fixes the perturbative energy spectrum – see also [42]. The classical period t 0 (E)
can be computed and yields


1 5
15E 2 1155E 3
t 0 (E) = E · 2 F1
, , 2, 54E ≃ E +
+
+ O(E 4 ) .
(54)
6 6
4
16
Then using the differential operator technique13 we can express the quantum corrections of
the quantum A-period in terms of the classical period and its derivative with respect to E. The
Note that we require E > 0 for the turning points to be real, otherwise a different Stokes graph with different
quantisation conditions would emerge. Hence, consistency requires us to restrict N to nonnegative integers Z≥0 .
In principle, at finite ħ
h there would also be an upper bound to N where the potential is ‘filled’; however, for us this
upper bound plays no role since we will always work in a small ħ
h-expansion.
13
See e.g. [36, 43] or appendix A of [44] for an explanation. In a nutshell, one uses the fact that the first
cohomology group of a genus g Riemann surface is spanned by 2g meromorphic differentials. The leading piece
of the Riccati solution, p0 (E, x), together with its derivatives with respect to E, form a suitable basis for this space
and so we can decompose any higher order term pn>0 (E, x) in this basis modulo total derivatives with respect to x.
12

13

## PDF page 14

SciPost Phys. 16, 103 (2024)

first two corrections are given by
5(1 − 108E)
3 ∂ t0
t0 +
,
15E(1 − 54E)
4 ∂E
7(4 − 633E + 34182E 2 )
7(1 − 108E) ∂ t 0
t 2 (E) =
t0 −
.
1536E 3 (1 − 54E)3
384E(1 − 54E)2 ∂ E
t 1 (E) = −

(55)

One then inverts the series by imposing that E(t(E; ħ
h); ħ
h) = E, which up to the same order in
ħ
h implies that
∂ E0
t 1 (E0 (t)) ,
∂t
∂ E0
∂ E1
1 ∂ 2 E0
E2 (t) = −
t 1 (E0 (t))2 −
t 2 (E0 (t)) −
t 1 (E0 (t)) .
2
2 ∂t
∂t
∂t
E1 (t) = −

(56)

Computing these corrections and adding them up leads to a perturbative asymptotic expansion
for E:



15t 2 705t 3 115755t 4
5
E(t; ħ
h) = t −
−
−
+O t
4
16
128


 2
7
1155t 209055t 2
3
+ −
−
−
+O t
ħ
h
16
64
256


101479
+ −
+ O (t) ħ
h4
2048
+ O(ħ
h6 ) .
(57)
Finally, if we let ν = N + 21 , the perturbative energy after quantisation (53) becomes



1155ν 705ν3
15ν2
7
2
+
ħ
h −
+
ħ
h3
E(ν; ħ
h) = νħ
h−
16
4
64
16


2
4
101479 209055ν
115755ν
−
+
+
ħ
h4 + O(ħ
h5 ) .
2048
256
128


(58)

One can verify this expression, either by comparing with [] or by computing the energy levels
using the Bender-Wu package [45] in Mathematica.
Returning to our main storyline, in the case of D+ (t; ħ
h) = 0, the perturbative condition is
the full quantisation condition, and we have now succesfully computed the resonance spectrum. However, when we cross the real positive ħ
h-axis clockwise, the quantisation condition
is altered: it obtains additional corrections which are nonperturbative in ħ
h – as shown in (52)
when moving from the bottom to the top equation. The period t which solves the condition
D− = 0 must therefore be different from the perturbative solution, and this difference can
expressed in terms of a new nonperturbative quantity ∆t which promotes t to a transseries
t̂ [, ]:
∞
∑
t̂ = t + ∆t , with ∆t =
t (n) λn ,
(59)
n=1
− ħ1h t D (t;ħ
h)

where λ = e
is an exponentially small quantity, which contains the instanton transmonomial and also a power series of its own. Note that here, we have temporarily gone back to
the ‘unquantised’ situation where t can be any value of the A-period for the ‘+’-resolution of the
nonperturbative ambiguity, and we now want to express the A-period t̂ for the ‘−’-resolution,
including its nonperturbative contributions, in terms of t. From plugging the above Ansatz
14

## PDF page 15

SciPost Phys. 16, 103 (2024)

into D− = 0, we learn that in order to compute the instanton corrections we need to solve the
equation


1
iħ
h
∆t = −
log 1 + e− ħh t D (t+∆t;ħh) .
(60)
2π
We can solve this equation exactly, but before we do so, let us briefly recap how one solves the
equation iteratively [] . By plugging in the Ansatz from above one finds for the leading orders
in λ that
iħ
h
t (1) = −
,
2π
iħ
h
ħ
h F ′′
t (2) =
+
,
(61)
4π 4π2
iħ
h
3ħ
h F ′′ 3iħ
h(F ′′ )2 iħ
h2 F ′′′
t (3) = −
−
+
−
.
6π
8π2
16π3
16π3
The F -derivatives in this expression are with respect to t; recall in particular from (34) that
F ′ (t; ħ
h) = t D (t; ħ
h). Next, we can compute the energy transseries
Ê(t; ħ
h) = E(t + ∆t; ħ
h) =

∞
∑

E (n) λn ,

(62)

n=0

as an expansion in powers of λ around its perturbative solution E (0) = E(t; ħ
h), to obtain a full
transseries. For the first few orders in λ this yields
iħ
hE′
,
2π
iħ
hE′ ħ
h E ′ F ′′ ħ
h2 E ′′
E (2) =
+
−
,
4π
4π2
8π2
E (1) = −

E (3) = −

(63)

′′ 2

hE′ F
h E ′ F ′′ ħ
h2 E ′′ 3iħ
iħ
h E ′ 3ħ
−
+
+
6π
8π2
8π2
16π3

−

iħ
h2 E ′ F ′′′ iħ
h2 E ′′ F ′′ iħ
h3 E ′′′
−
+
.
16π3
8π3
48π3

The nonperturbative corrections t (n) and E (n) above are expressed in terms of the ‘perturbative’
quantities E and F , and are therefore also formal power series in ħ
h themselves. As we go to
higher orders, even in the above form, the expressions for the instanton corrections (61) and
(63) become larger and more unmanageable very fast. Fortunately, one can organise them in
a more efficient way:
iħ
h
λ,
2π


iħ
h 2
ħ
h
∂ 2
t (2) λ2 =
λ −
ħ
h
λ
,
4π
8π2
∂t




2
iħ
h 3
ħ
h
∂ 3
iħ
h
2 ∂
3
(3) 3
t λ =− λ +
ħ
h λ +
ħ
h
λ ,
6π
8π2
∂t
48π3
∂ t2
t (1) λ = −

(64)

and similarly for the energy transseries [, 42]:
iħ
h ′
E λ,
2π

iħ
h ′ 2
ħ
h
∂
′ 2
E (2) λ2 =
Eλ −
ħ
h
E
λ
,
4π
8π2 ∂ t
2


ħ
h
iħ
h
iħ
h ′ 3
∂
2 ∂
′ 3
E (3) λ3 = −
Eλ +
ħ
h
E
λ
+
ħ
h
E ′ λ3 .
2
3
2
6π
8π
∂t
48π
∂t

E (1) λ = −

15

(65)

## PDF page 16

SciPost Phys. 16, 103 (2024)

We have written these expressions using the ‘dimensionless derivative’ ħ
h ∂∂t , which turns out to
be very convenient. More generally, we would like to argue that the full transseries solutions
t̂ and Ê can be put in the following form:
∞ ∑
n−1
∑



∂ m n
h
un,m ħ
t̂ = t + ħ
h
λ ,
∂t
n=1 m=0
and
Ê = E + ħ
h

∞ ∑
n−1
∑


 

∂ m ∂E n
λ .
un,m ħ
h
∂t
∂t
n=1 m=0

(66)

(67)

Remarkably, the coefficients un,m in both transseries are the exact same numbers – a pattern
which is also clear in (64) and (65). In the next subsection we derive the form (66) and (67)
explicitly, including exact expressions for these universal coefficients.

3.2

Deriving exact multi-instanton expressions

In [24], a solution to the holomorphic anomaly equations was presented which involved solving a functional equation using the Lagrange inversion theorem. Inspired by this result, we
show that the same technique can be used to solve (60) and produce the coefficients un,m of
(66) and (67) in closed form. The resemblance between both approaches is not unexpected,
given that the quantum prepotential – which solves the holomorphic anomaly equations in the
NS background – is closely related to the ordinary energy through the PNP relation. We will
introduce the PNP relation in the next subsection.
Consider a function R(∆, z) of the generic form


∞
∑
k ∆∂ t ′
k
R(∆; z) = ħ
h
rk z exp − e F (t) ,
(68)
ħ
h
k=1
where the rk are arbitrary coefficients and e∆∂ t is a shift operator. One could take F ′ (t) to also
be an arbitrary function, but for our purposes it will always be the derivative of the quantum
prepotential. The variable z is a convenient bookkeeping device that we use to count powers
of the instanton transmonomial. Let us for the moment forget about equation (60) and regard
∆t as the solution to the more generic equation
∆t = R(∆t; z) .

(69)

This equation implies that the solution ∆t itself will also be an expansion in z. Now let us take
an arbitrary function ϕ(∆) that is analytic at ∆ = 0. Then the Lagrange inversion theorem
(see e.g. theorem 2.4.1 of [46]) tells us that this function evaluated at ∆ = ∆t, with ∆t the
solution to (69), can be expressed in the following way:
ϕ(∆t) =

∞
∑
1

m
m=1

[∆m−1 ]ϕ ′ (∆)R(∆; z)m .

(70)

Here [∆k ] means that we extract the series coefficient associated to the k-th power of ∆ from
the expression that follows. Let us choose
ϕ(∆) = f (t + ∆) = e∆∂ t f (t) ,

(71)

for some arbitrary function f (t), infinitely differentiable at t = 0. Note again that the evaluation of ϕ at ∆t induces a z dependence which implies that we can write our solution as a
power series
∞
∑
ϕ(∆t) =
fnz n ,
(72)
n=0

16

## PDF page 17

SciPost Phys. 16, 103 (2024)

for some yet unknown coefficients f n . Below, we want to compute the f n and subsequently
show that after removing the bookkeeping variable z (by setting z = 1) we can write the full
solution as


∞ ∑
n−1
∑

∂ m ′
f (t + ∆t) = f (t) + ħ
h
un,m ħ
h
f (t)λn ,
(73)
∂
t
n=1 m=0
and that we can produce explicit expressions for the coefficients un,m .
We start by noting that f0 = f (t), since (68) vanishes as z goes to zero, and therefore so
does ∆t. The extraction [∆m−1 ] in equation (70) can in practice be done through differentiation, allowing us to write
∞
∑

 n 

∂
∂ m−1 ′
1
ϕ (∆)R(∆; z)m
.
fn =
m!n!
∂
z
∂
∆
∆=z=0
m=1

(74)

We first calculate14


∂
∂z

n

m

R(∆; z) =

n 
∑
∂k
k=1

∂ Rk

R

m



Bn,k (R′ , R′′ , . . .) ,

(75)

using Faà di Bruno’s formula, which generalises the chain rule to higher derivatives. The Bn,k
are incomplete Bell polynomials, with arguments that are derivatives of R with respect to z. We
then observe that these Bell polynomials are homogenous in the instanton transmonomial:15

 n
(76)
Bn,k (R′ , R′′ , . . .) = exp − e∆∂ t F ′ Bn,k (R̃′ , R̃′′ , . . .) ,
ħ
h
where we have extracted
the instanton transmonomial from the k-th derivatives:
 (k)
k ∆∂ t ′
(k)
R = exp − ħh e F R̃ . Subsequently, one applies the derivatives with respect to ∆ and
learns from a straightforward calculation that16
 m−1



 n
n ′
∂
∂ m−1 ′
=
ϕ (∆) exp − e∆∂ t F ′
f ′ (t)e− ħh F (t) .
(77)
∂∆
ħ
h
∂t
∆=0
We then obtain
 
n
∞

1 ∑ ∂ k ∑ 1 m ∂ m−1 ′
′
′′
fn =
R
f
(t)B
R
(0;
z),
R
(0;
z),
.
.
.
n,k
n! k=1 ∂ Rk m=1 m!
∂t
z=0


n−1

1 ∑ ∂ k ′
=
f (t)Bn,k+1 R′ (0; 0), R′′ (0; 0), . . . .
n! k=0 ∂ t

(78)

The above derivatives in the Bell polynomials are just instanton transmonomials:
k ′
R(k) (0; 0) = k! rk ħ
h e− ħh F (t) , and so we end up with
n−1
∑
1



n ′
∂ k ′
f (t)e− ħh F (t) ,
fn = ħ
h
Bn,k+1 (1! r1 , 2! r2 , 3! r3 , . . . , (n − k)! rn−k ) ħ
h
n!
∂t
k=0

(79)

14
Note that ϕ(∆), which is evaluated at generic ∆, is independent of z. It is only after evaluating it at ∆t that
the function develops a z-dependence.


15
We will call both exp − ħ1h F ′ (t) and exp − ħ1h F ′ (t + ∆t) an ‘instanton transmonomial’; it will generally be
clear from the context which transmonomial we refer to.
16
One uses the fact that
 n

∂
∂n
∆∂ t
e
=
.
n
∂∆
∂ tn
∆=0

17

## PDF page 18

SciPost Phys. 16, 103 (2024)

Table 1: Values of the coefficients un,m for the energy transseries (67). The index n
labels the rows and m labels the columns.
m

0

1

2

3

E (1)

1
2πi

E (2)

1
− 4πi

− 8π1 2

E (3)

1
6πi

1
8π2

1
− 48π
3i

E (4)

1
− 8πi

11
− 96π
2

1
32π3 i

1
384π4

E (5)

1
10πi

5
48π2

7
− 192π
3i

1
− 192π
4

4

1
3840π5 i

which fits the form suggested in (73). Finally, we can then identify the coefficients
un,m =

1
Bn,m+1 (1! r1 , 2! r2 , . . . , (n − m)! rn−m ) .
n!

(80)

Let us stress that other than infinite differentiability, this procedure makes no assumptions
about f (t) whatsoever: it simply tells us that if we shift its argument by the ∆t that solves
(68), then we find the structure (73) with coefficients un,m as given in (80). The values of
these coefficients are thus independent of the details of the quantity f (t); the approach is
merely a recipe for enhancing the function f (t) to the transseries fˆ(t) = f (t + ∆t).
Going back to our actual problem, we are perturbing the energy E(t) with a ∆t that solves
(60). Therefore we can identify f (t) = E(t; ħ
h) and compare (60) with (68) to find
rk =



(−1)k
1
−
.
k
2πi

(81)

Inserting this into (80) gives us the sought-for coefficients un,m of our energy transseries; we
tabulate some of these coefficients in table 1. Alternatively, when we choose f (t) = t we
obtain the transseries (66), for which we now understand why the same universal coefficients
un,m appear.
Having obtained explicit values for the universal coefficients un,m , we now have a complete
description of the energy transseries solution for the cubic oscillator when ħ
h is located slightly
below the real axis. The Stokes phenomenon that occurs along the ray arg(ħ
h) = 0 accounts for
the appearance of all these instanton corrections, meaning that we should have the following
action of the Stokes automorphism:

S0 E(t; ħ
h) = Ê(t; ħ
h) .

(82)

On the left hand side we have the perturbative energy E(t; ħ
h) which is a solution to the quantisation condition D+ = 0, and on the right hand side we find the transseries Ê(t; ħ
h) = E(t +∆t; ħ
h)
−
which solves D = 0. We would like to fit this Stokes phenomenon into the more universal
framework of one-parameter transseries. This involves introducing a new parameter σ called
the transseries parameter which incorporates the Stokes jump that our asymptotic solution for
the energy undergoes. While being slightly agnostic for the moment about the precise details,

18

## PDF page 19

SciPost Phys. 16, 103 (2024)

we thus enhance the notation of our energy transseries to include this parameter by writing
Ê(t, σ; ħ
h). The above Stokes jump should then translate to
h) = Ê(t, S; ħ
h) ,
S0 Ê(t, 0; ħ

(83)

where S is a yet unknown Stokes constant. It is then natural to expect that the coefficients
un,m encode this Stokes constant in some convoluted way. In order to extract the Stokes constant, we need to decompose the action of the Stokes automorphism in terms of pointed alien
derivatives (cf. (12)), which are labeled by the locations of the singularities l A = l F0′ (t) in
the Borel plane. Accordingly, acting with the automorphism on the perturbative energy yields
for the first few orders:17




1 2
1 3
˙
˙
˙
˙
˙
˙
˙
E + ∆A E +
∆ + ∆2A E +
∆ + ∆2A ∆A + ∆3A E + . . . = Ê(t, S; ħ
h) ,
(84)
⏟⏞⏞⏟
2 A
6 A
⏟
⏟
⏞⏞
⏟
⏞⏞
⏟
1-instanton
2-instanton

3-instanton

which should match the transseries below the Stokes line. Recall that the pointed alien deriva˙ l A by definition (13) contributes a factor e−l A/ħh and hence we can group the terms totive ∆
gether as shown above. If we can now figure out how the individual pointed alien derivatives
act on the perturbative energy E(t; ħ
h), then we should be able to extract the Stokes constant
S. In order to achieve this, we turn to the PNP relation.

3.3

Stokes phenomenon through the PNP relation

Guided by observations made in [47] while studying the Stark effect Hamiltonian, it was recognised in [] that for the cubic oscillator there exists a simple equation relating the tunneling
period t D (t; ħ
h) to the perturbative energy E(t; ħ
h). This equation was subsequently also established in various other quantum mechanical models including the double well [, 9] and
cosine potentials [27] that we will study shortly. In fact, one can derive it for generic polynomial potentials by applying an appropriate Riemann bilinear identity on the WKB curve, as
we illustrate in appendix A. This relation, which is often referred to as the PNP relation,18 has
appeared in the literature in many forms and guises. In our present setting and notation, it
allows us to connect the ordinary energy E to the quantum prepotential F from (33) as
c

∂E
∂ 2F ∂ F
∂ 2F
=t 2 −
+ħ
h
.
∂t
∂t
∂t
∂ t∂ ħ
h

(85)

Here, c is a constant of proportionality that one can compute explicitly, though its actual value
will not be important for our purposes. An alternative expression is obtained by integrating
the equation with respect to t, leading to


∂
∂
cE = t
−2+ħ
h
F + C(ħ
h) .
(86)
∂t
∂ħ
h
The integration constant C(ħ
h) can also be computed for each given model, and turns out to be
a monomial19 in ħ
h. We provide more background information on this equation in appendix A.
Let us stress that the PNP relation (86) is fundamentally different from the exact quantisation
condition (51), despite the fact that both involve E and F . The quantisation condition tells
Formally, the 3-instanton correction contains the term 12 ( ˙
∆2A ˙
∆A + ˙
∆A ˙
∆2A ), but as we argued in section 2.1
the pointed alien derivatives commute.
18
The name PNP stands for ‘perturbative/nonperturbative’ and comes from the fact that the relation connects
the tunneling period – which induces nonperturbative corrections – to the perturbative energy ħ
h-expansion.
19
In fact, dimensional analysis of the Schrödinger equation tells us that if ħ
h has mass dimension 1, then the
energy and quantum prepotential have mass dimension 2, which implies that C(ħ
h) ∼ ħ
h2 .
17

19

## PDF page 20

SciPost Phys. 16, 103 (2024)

us how the energy transseries Ê can be constructed from the perturbative energy E and the
perturbative quantum prepotential F , without making any assumptions about the specifics of
these series expansions themselves. The PNP relation actually relates the two perturbative
series to one another.
Our strategy is now as follows: for the quantum prepotential we have a clear understanding of its transseries solution and resurgent structure. Using the action of the pointed alien
derivative on this quantum prepotential – given in (46) as proposed in [24] – we can use the
PNP relation to probe the resurgent structure of the energy transseries. Formally what we
would like to do, in the spirit of [21] (and also [23]), is therefore to extend the PNP relation
from an equation between formal power series to an equation between transseries:


∂
∂
c Ê = t
F̂ + C(ħ
h) .
(87)
−2+ħ
h
∂t
∂ħ
h
Ê and F̂ now denote the respective transseries extensions of the energy and quantum prepotential. Because the energy transseries admits an expansion in integer powers of λ, the
quantum prepotential transseries, whose first three corrections are given in (44), must have
G = F ′ (t; ħ
h) in order for the above equation to make sense. Starting from the PNP relation
and applying the pointed alien derivative with A = t D,0 (t) to the perturbative energy E we get


1
∂
∂
˙
˙ AF
∆A E =
t
−2+ħ
h
∆
c
∂t
∂ħ
h


SA ħ
h
∂ F ′ −F ′ /ħh
′′
′
=
−t F + F − ħ
h
e
c
∂ħ
h
= −SAħ
hE′λ .
(88)
Here, we used the fact that the pointed alien derviative ˙
∆A commutes with differentiation
with respect to ħ
h or t. In the final expression, we recognise the one-instanton correction from
(65), which allows us to read off the value of the Stokes constant:
SA = −

1
.
2πi

(89)

We can repeat this computation for the pointed alien derivative with arbitrary ‘step size’ l A
for l ∈ Z>0 . Moreover, in anticipation of what is to come, it will be useful to apply the pointed
alien derivatives to the instanton transmonomial λ as well. We then find the following two
similar-looking equations:
Sl Aħ
h(−1)l ∂ E l
λ ,
l
∂t
S ħ
h(−1)l ∂ λ l
˙ lAλ = lA
∆
λ .
l
∂t

˙
∆l A E =

Now, let us define


 

∂ m ∂E n
En,m = ħ
h
λ ,
∂t
∂t

(90)

(91)

which are the essential building blocks of our exact transseries (67) that there are weighed by
the coefficients un,m . Then, by combining equations (90) and (91) with the Leibniz rule for
operators, we obtain
Sl A (−1)l
˙
∆l A En,m =
En+l,m+1 ,
(92)
l
which can alternatively be derived using the PNP relation similar to what we did in (88).
This relation describes the full resurgent structure of the energy transseries in a nutshell, as
20

## PDF page 21

SciPost Phys. 16, 103 (2024)

Figure 4: A pictorial representation of the result (92) which is also known as the alien
lattice of the ordinary energy transseries Ê. The boxes represent the building blocks
(91) with the inclusion of the perturbative energy E, and the arrows illustrate how
the pointed alien derivatives map each sector to one appearing in the next column.
depicted graphically in figure 4, and is a direct consequence of (46). From comparing our
formula (92) to the coefficients un,m in table 1, we learn that all Stokes constants reduce to
one and the same number:
1
Sl A = −
.
(93)
2πi
Remarkably, we now see that the condensed form (67) of writing the transseries is not only
favorable from a notational point of view, but it also exposes its resurgent structure: if we
assign a weight l to the pointed alien derivative ∆l A , then every sector En,m in the transseries
that occurs above the Stokes line is generated by a sum of strings of m pointed alien derivatives
with a total weight n that naturally appears when we expand the automorphism S0 .
Summarizing what we have learned so far, we can now reformulate the energy transseries
in the form of a more generic one-parameter transseries:
Ê(t, σ; ħ
h) = E(t; ħ
h) + ħ
h

∞ ∑
n−1
∑


 

∂ m ∂E
h
un,m σ m+1 ħ
(t; ħ
h)λ(t; ħ
h) n ,
∂t
∂t
n=1 m=0

(94)

with the universal coefficients un,m given by (80), where
rk =

(−1)k
.
k

(95)

Notice how this transseries structure is different from the conventional ODE type oneparameter transseries – see e.g. [30,48] – where the n-th instanton sector only carries a factor
σ n . Here, instead, we see that each instanton sector E (n) consists of multiple parts, each scaling
with a different power of the transseries parameter, running from σ1 up to σ n . The complete
Stokes transition can now be captured in the form (83) by the single expression


1
;ħ
h .
(96)
S0 Ê(t, 0; ħ
h) = Ê t, −
2πi
In fact, from the alien calculus structure uncovered above, we can argue that more generally
when we cross the Stokes line we have

S0 Ê(t, σ; ħ
h) = Ê(t, σ + SA ; ħ
h) ,
21

(97)

## PDF page 22

SciPost Phys. 16, 103 (2024)

for the same transseries with generic σ. Let us emphasise that the Stokes constants Sl A are
first and foremost the Stokes constants of the quantum prepotential, defined in (46). We have
merely picked a convenient normalisation for the generic energy transseries (94), with the
redefinition of the rk given in (95), such that its Stokes constants are exactly the same as those
of the quantum prepotential. This is possible thanks to the linear nature of the PNP relation.
Finally, let us remark that in this example all nonperturbative sectors En,m are connected
to the perturbative energy E through resurgence, as shown in figure 4. This means that from
studying the large order behaviour of the perturbative coefficients one can reconstruct the full
transseries solution with the exception of the value of the transseries parameter σ. Therefore,
the energy transseries Ê that we have constructed is a minimal resurgent transeries. As we
will see shortly, this does not hold for the energy transseries that we find in potentials with
multiple minima.

3.4

Stokes phenomenon from DDP formula

The alien calculus (92) uncovered above, including the value of the Stokes constants, can also
be derived from the Delabaere-Dillinger-Pham formula directly. Let us illustrate this. We first
switch back to the formalism in which the periods are expressed in terms of the independent
variables (E, ħ
h). The DDP formula (31) along the arg(ħ
h) = 0 Stokes ray, expressed for both
periods, then reads:

S0 t(E; ħ
h) = t(E; ħ
h) +


iħ
h
log 1 + e−t D (E;ħh)/ħh ,
2π

(98)

S0 t D (E; ħ
h) = t D (E; ħ
h) .
The first of these two equations allows us to deduce the action of the pointed alien derivative
on the quantum A-period:


h(−1)l+1 −l t D (E;ħh)/ħh
1 ħ
˙
e
.
∆l A t(E; ħ
h) = −
2πi
l

(99)

To derive the action of the pointed alien derivative on the energy, we use the fact that the
energy E(t; ħ
h) is the inverse of the quantum A-period t(E; ħ
h):
0= ˙
∆l A E(t(E; ħ
h); ħ
h) = ˙
∆l A E(t; ħ
h)

t=t(E;ħ
h)

+

∂E
˙
(t; ħ
h)
∆l A t(E; ħ
h) ,
t=t(E;ħ
h)
∂t

(100)

where in the second equality we used the chain rule (18). Combining the previous two equations, we get
˙
∆l A E(t; ħ
h)

t=t(E;ħ
h)

=



∂E
1 ħ
h(−1)l −l t D (E;ħh)/ħh
(t; ħ
h)
−
e
.
t=t(E;ħ
h)
∂t
2πi
l

(101)

We then switch to independent variables (t, ħ
h) by substituting E by its quantum mirror map
E(t; ħ
h) and obtain


1 ħ
h(−1)l ∂ E l
˙
∆l A E = −
λ .
(102)
2πi
l
∂t
1
This is exactly the first equation of (90) with the Stokes constant Sl A = − 2πi
. To obtain the
second equation, we consider the second line of (98), which tells us that the dual quantum
period t D (E; ħ
h) is invariant under the Stokes jump. Given the identity (36) that expresses t D
in terms of the quantum prepotential, and using the chain rule again, we obtain



1 ħ
h(−1)l −l t D (E;ħh)/ħh
(˙
∆l A F ) (t; ħ
h)
= F (t; ħ
h)
−
e
,
t=t(E;ħ
h)
t=t(E;ħ
h)
2πi
l
′

′′

22

(103)

## PDF page 23

SciPost Phys. 16, 103 (2024)

where the primes denote differentiation with respect to t. We then substitute E by its quantum
mirror map E(t; ħ
h), to obtain


1 ħ
h(−1)l −l t D (t;ħh)/ħh
′
′′
˙
∆l A F (t; ħ
h) = F (t; ħ
h) −
e
.
2πi
l

(104)

Finally, using this result we straightforwardly derive the statement


1 ħ
h(−1)l ∂ λ l
˙
∆l A λ = −
λ ,
2πi
l
∂t

(105)

1
. Both equations
which is the second equation of (90) with the same Stokes constant Sl A = − 2πi
in (90) imply the result (92) for En,m , as we argued earlier, and so we once again end up with
the alien lattice displayed in figure 4.
Let us remark that the same approach can be used to derive relations (46) for the quantum
prepotential along any direction in the complex ħ
h-plane. We give two examples of this in
appendix B.

3.5

On the quantum prepotential transseries

We conclude this section by calculating the quantum prepotential transseries that corresponds
to the energy transseries (67), and generalise it to a one-parameter quantum prepotential
transseries just like we did for the energy. There are two ways of doing this. The first one
is by mapping instanton sectors of the quantum prepotential transseries (44) to the energy
transseries via the nonperturbative PNP relation (87) – see e.g. [23]. One can then fix the
parameters τk of the quantum prepotential transseries (44) by comparison to the coefficients
un,m of the energy transseries. As we did for the energy, one can then generalise this quantum
prepotential transseries to a one-parameter transseries. The second option is to use the algorithm of section 3.2 to directly obtain a transseries expression for the quantum prepotential,
and compare it to the solution (44) found in [24]. Here, we illustrate the latter approach.
We start by recalling that our algorithm requires us to pick a function f (t) which we wish
to perturb by shifting t to t + ∆t. Since the quantum prepotential is defined in terms of the
dual quantum period by the relation (34), F ′ (t; ħ
h) = t D (t; ħ
h), a suitable candidate for f (t)
is to use the dual quantum period. We set ϕ(∆) = f (t + ∆) = F ′ (t + ∆; ħ
h) and obtain the
transseries


∞ ∑
n−1
∑

∂ m ′′
′
′
F̂ (t; ħ
h) = F (t; ħ
h) + ħ
h
un,m ħ
h
F (t; ħ
h)λ(t)n ,
(106)
∂t
n=1 m=0
in terms of the universal coefficients un,m (80). Notice that λ(t) = exp(−F ′ (t; ħ
h)/ħ
h) and
therefore we can integrate both sides with respect to t to obtain
F̂ = F + ħ
h2

∞
∑
n=1





m−1
n−1
∑

1
∂
− un,0 λn +
un,m ħ
h
F ′′ λn .
n
∂
t
m=1

(107)

Note that any integration constant must be t-independent and hence must be part of the perturbative quantum prepotential F . Comparing the above transseries to the solution given
in [24], normalized as in (44), allows us to relate the coefficients un,m to the parameters τk of
the quantum prepotential. We show the result in table 2. Plugging in the actual values of the
coefficients un,m – that is, using the original rk from (81) – then tells us that all parameters τk
have the same value:
1
τk = k (−1)k rk = −
.
(108)
2πi

23

## PDF page 24

SciPost Phys. 16, 103 (2024)

Table 2: The coefficients un,m , expressed in terms of the parameters τk (44) of the
quantum prepotential transseries F̂ for the cubic oscillator.
m

0

1

2

F (1)

−τ1

F (2)

τ2
2

F (3)

− 33

− 22 1

− 61

F (4)

τ4
4

τ22
τ3 τ1
3 + 8

τ2 τ21
4

F (5)

− 55

3

4

τ21
2

τ

τ τ

τ

τ3

τ τ

− 44 1 −

τ3 τ2
6

τ τ2

− 36 1 −

τ41
24
τ22 τ1
8

τ τ3

2 1
− 12

τ5

1
− 120

If we introduce a transseries parameter by replacing the coefficients un,m in (106) by un,m σ m+1
and use the new rk from (95), similarly to what we did for the energy transseries, then we can
identify σ as the single transseries parameter of the quantum prepotential transseries, i.e.
τk = σ .

(109)

We can then write the quantum prepotential transseries as
2

F̂ (t, σ; ħ
h) = F + ħ
h

∞
∑
n=1




n−1
∑
1
∂ m−1 ′′ n 
n
m+1
− un,0 σλ +
un,m σ
ħ
h
F λ
,
n
∂t
m=1



(110)

where the universal coefficients un,m from (80) are defined using the new rk coefficients (95).
The Stokes phenomenon of the quantum prepotential is then captured by

S0 F̂ (t, σ; ħ
h) = F̂ (t, σ + SA ; ħ
h) .

(111)

Looking back, we can see that the resurgent structure of both the energy and the quantum prepotential are essentially the same due to the PNP relation. The singularities in their respective
Borel planes naturally lead to the minimal transseries extensions (94) and (110) which carry
a single degree of freedom σ governing the nonperturbative effects. The exact quantisation
conditions D+ = 0 and D− = 0 are then physical boundary conditions which fix the value of
1
this parameter to σ = 0 and σ = − 2πi
respectively. Furthermore, for both energy and quantum prepotential we can deduce the alien lattice structure shown in figure 4 and the exact
values for the Stokes constants (93). These follow from translating the known alien calculus
(46) of the quantum prepotential to the energy transseries and attributing the ambiguities that
come from the quantisation conditions to the Stokes constants. Alternatively, one can reach
the same conclusions directly from the Delabaere-Dillinger-Pham formula.
With that, we conclude the treatment of the cubic potential and move on to the double well
potential, whose energy transseries, as we will see shortly, has an extra layer of complexity to
it: its energy transseries will be no longer minimal, but will be a sum of minimal transseries.

24

## PDF page 25

SciPost Phys. 16, 103 (2024)

Figure 5: On the left we draw the symmetric double well potential (112), and on the
right its four turning points in the complex x-plane with the cycles γA and γB .

4

The symmetric double well potential

In this section, we consider the symmetric double well potential:
V (x) =

x2
(1 + x)2 .
2

(112)

1
When the energy E lies in the range 0 < E < 32
, there are four turning points on the real
axis. These provide us with three cycles – see also figure 5: two cycles around minima that we
both label by γA, since by symmetry they give rise to the same quantum A-period t, and the
‘tunneling cycle’ γB that we associate to the dual quantum period t D . Contrary to the cubic
oscillator, this model does admit bound states. The goal will be to cast its nonperturbative
spectrum of energies E in the form of an exact transseries and study its Stokes phenomenon.
The exact quantisation condition for this model was obtained in [3] through instanton
calculus, and can also be derived using the Voros-Silverstone connection formula [4, 41] (see
also [42]) or the uniform WKB method [, 10]. As was the case for the cubic oscillator, each of
these approaches leads to an ambiguity in the quantisation condition, which can be resolved by
slightly perturbing the phase of ħ
h. As a result, we are presented with two exact quantisation
conditions that we write as D− = 0 for Im(ħ
h) < 0 and D+ = 0 for Im(ħ
h) > 0. In terms of
independent variables (t, ħ
h) these conditions read
1

Dε± = 1 + e±2πit/ħh ∓ iε e− 2ħh t D (t;ħh) = 0 .

(113)

There are two novelties compared to the exact quantization conditions (52) of the cubic. First
of all there are now two pairs of quantization conditions, labeled by a parameter ε ∈ {+1, −1},
which refers to the parity of the wave function for which we compute the energy, and which
can be interpreted as a quantum number. Almost all quantities that we compute will depend
on a choice of ε, but to avoid cluttering the notation with subscripts we generally suppress this
dependence. Secondly, we note the subtle factor 12 in (113) that multiplies the dual quantum
period t D . This factor indicates the presence of nonperturbative corrections that we associate
with instantons that tunnel an odd20 number of times.
Now, we follow a similar approach as for the cubic oscillator (52). We start by noting that
the contribution of the dual ‘tunneling’ quantum period is exponentially suppressed along the
positive real ħ
h-axis, and we therefore first consider the perturbative quantisation condition


1
±2πit/ħ
h
.
(114)
1+e
= 0 , implying t = ħ
h N+
2
20
Note that the cubic only has corrections coming from instantons that tunnel an even number of times. This
can be explained by the fact that the cubic has only a single local minimum which forces any instanton solution to
tunnel back.

25

## PDF page 26

SciPost Phys. 16, 103 (2024)

where N is an integer. Note that the perturbative quantisation condition is insensitive to the
choice of parity ε, and therefore the perturbative energy spectrum, labeled by the quantum
numbers (ε, N ), is doubly degenerate. The next step is then to look for the fully nonperturbative
solution t̂ to (113), which we write as
t̂ = t + ∆t ,

with ∆t =

∞
∑

1

t (n) λ 2 n ,

(115)

n=1

where λ = exp(−t D (t; ħ
h)/ħ
h) as before, but due to the factor of 21 in front of t D in (113) we
now make an Ansatz in half-integer powers of this λ. This difference with the cubic case will
play a central role in much of what follows. One can now show that this Ansatz produces a
transseries for t̂ which is found by solving the equation
∆t = ∓



1
iħ
h
log 1 ∓ iε e− 2ħh t D (t+∆t) ,
2π

(116)

where the signs depend on whether we choose to solve D+ = 0 or D− = 0. Here and below,
we will follow the convention that the upper sign in expressions is the one for the quantisation
condition D+ = 0, and the lower sign is the one for D− = 0. Note that the equation above also
has a factor 21 in front of the dual quantum period t D in the exponent. Therefore our Ansatz
1

for the energy transseries will also be one in powers of λ 2 :
∞ ∑
n−1
∑



 
∂ m ∂ E 1n
2
.
Ê = E + ħ
h
un,m ħ
h
λ
∂t
∂t
n=1 m=0

(117)

We then turn to the algorithm that we introduced in the previous section and compute the
universal coefficients un,m given by (80), with input data
rk =

εk (±i)k+1 1
.
k
2π

(118)

These values follow from expanding (116) and comparing it to the expression
∆ = R(∆; z) = ħ
h

∞
∑



k
rk z k exp − e∆∂ t F ′ (t) ,
2ħ
h
k=1

(119)

which is almost identical to (68), except again for the factor 12 in the exponent. This yields
the universal coefficient values displayed in table 3, the first three rows of which were also
computed in [10] (see also [42]).
A few remarks are in order. First of all, we note that all the odd instanton sectors E (2k+1)
depend on the parity ε whereas the even sectors do not. The odd sectors therefore induce
a nonperturbative level-splitting that lifts the degeneracy of the perturbative energy levels.
From a resurgence point of view, this also has an interesting implication. The insensitivity to
the parity of the even instanton sectors (including the perturbative sector E (0) ) implies that
from a resurgence point of view, one cannot deduce the existence of the odd sectors from
the large order behaviour of the perturbative coefficients. This is a well known fact which is
graphically depicted in the the resurgence triangle of [26, 27]. We will elaborate more on this
when we study the cosine potential in the next section.
Secondly, it is well known [13] that the large order behaviour of the perturbative energy
to leading order probes the imaginary 2-instanton effect that comes from an instanton-antiinstanton pair. Such an imaginary term does appear in table 3 at the 2-instanton level and is
also ambiguous – i.e. dependent on the ± quantisation condition chosen to resolve the nonBorel summability of the perturbative series. In fact, all imaginary parts of the transseries
26

## PDF page 27

SciPost Phys. 16, 103 (2024)

Table 3: The values for the coefficients un,m of the energy transseries (117). The
index n labels the rows and m labels the columns. In tabulating these values we used
(±)2 = ε2 = 1.

m

0

1

2

3

u1,m

1
− 2π
ε

u2,m

i
∓ 4π

1
8π2

u3,m

1
6π ε

± 8πi 2 ε

1
− 48π
3ε

u4,m

i
± 8π

11
− 96π
2

i
∓ 32π
3

1
384π4

u5,m

1
− 10π
ε

5i
∓ 48π
2ε

7
ε
192π3

i
± 192π
4ε

4

1
− 3840π
5ε

are ambiguous in this way, as is evident from equation (116), and one would expect that
when resumming the whole transseries these ambiguities cancel the ambiguities that arise
from resummming individual power series in the transseries. This expectation is supported
by the fact that the double well is a confining potential and therefore its energy spectrum
should be real and unambiguous. This cancellation mechanism has been tested in various
works [14, 15] (see also [42]) and we would like to extend it to all orders by casting it in the
language of alien calculus.

4.1

The full transseries

We would now like to probe the resurgent structure of the energy transseries (117) using alien
calculus and formulate a generic transseries structure as we did in (94) for the cubic. In the
double well potential, this is a more delicate exercise because its energy transseries is an expansion in half-integer powers of λ whereas the singularities in the Borel plane of the perturbative
energy are found at integer multiples of the primitive action A = t D,0 (E), which therefore correspond to integer powers of λ. Hence, there are two different transseries that we can identify:
One that includes all nonperturbative sectors, and which we call the full transseries, and one
that only contains those sectors visible in the Borel plane of the perturbative series, called the
minimal transseries.
The energy transseries (117) with the coefficients shown in table 3 is an example of a full
transseries, and we will construct the corresponding full quantum prepotential transseries in
this subsection. The minimal transseries is, as the name suggests, a truly minimal resurgent
transseries as defined in section 2.1. It allows us to derive the Stokes data that were obtained
in [24] using large order methods, and it admits the same generalisation to a one-parameter
transseries as the energy and quantum prepotential found for the cubic potential. Understanding how one obtains these minimal transseries and how they relate to the full transseries will
be the topic of the subsequent subsections in our treatment of the double well potential.
Let us therefore start by deriving the full quantum prepotential transseries. First, we recall the nonperturbative extension (87) of the PNP relation. Our full energy transseries (117)
relates through this PNP relation to the full quantum prepotential transseries F̂ full , which there27

## PDF page 28

SciPost Phys. 16, 103 (2024)

fore must have the following form:
F̂

full

=

∞
∑

F̃ (n) ,

1

F̃ (n) ∼ λ 2 n .

with

(120)

n=0

We can construct this transseries using the same approach as in section 3.5. Given ∆t which
solves equation (116), we again choose ϕ(∆t) = f (t + ∆t) = F ′ (t + ∆t; ħ
h) and use our
1
algorithm to produce a transseries for the dual quantum period in integer powers of λ 2 . We
then integrate both sides with respect to t and obtain an expression for the full quantum
prepotential transseries:
F̂

full

2

= F +ħ
h

∞
∑
n=1




n−1
∑
1
∂ m−1 ′′ 1 n
2
n
un,m ħ
h
F λ2 ,
− un,0 λ 2 +
n
∂t
m=1



(121)

which is only slightly different from its cubic analogue (107) by a few factors of two. We can
then identify this transseries with the transseries structure from [24] that we wrote in (44),
where we have D = 12 ∂∂t and G = 12 F ′ . As a result, we can express the coefficients un,m in
terms of the parameters τk appearing in that transseries. The result is shown in table 4.
When we then plug in the values of rk given in (118), we obtain (cf. section 4.2 of [23])
τk = 2k (−1)k rk = −

(∓i)k+1 εk
.
π

(122)

Remarkably, the parameters τk play two distinct roles: The parameters with odd k depend on
ε and encode the parity of the corresponding energy solution, whereas only the parameters
with even k behave as genuine transseries parameters implementing the Stokes phenomenon.
This suggests that, if we want to write down a generic one-parameter transseries for the full
quantum prepotential, only the τ2k – or equivalently the r2k – can depend on the transseries
parameter σ. However, as one can see from table 4, this implies that the coefficients un,m are
not homogeneous in the transseries parameter σ, and this prevents us from writing down a
simple and elegant generic one-parameter transseries structure as we did in (94) and (110)
for the cubic oscillator. We will come back to this issue in the next subsection.
Next, let us derive the Stokes data of this full quantum prepotential transseries. Analogous
to (91), we define the building blocks of our energy transseries as

 

∂ m ∂ E 1n
En,m = ħ
h
λ2 .
(123)
∂t
∂t
Let Ã = 21 t D,0 denote the ‘primitive’ instanton action of the transseries (117), or equivalently
of (121). Then an almost identical derivation to the one we performed for the cubic potential
yields the alien calculus relations
˙ l Ã En,m =
∆

S̃l Ã (−1)l
2l

En+l,m+1 ,

(124)

which differ from (92) only by a factor 21 . The Stokes constants S̃l A in this expression once
again originate from relation (46), this time associated to the full quantum prepotential
transseries where G = 12 t D (t; ħ
h). We can then match the action of the pointed alien derivative
with the observed Stokes phenomenon in table 3. Because the first instanton correction is
unambiguous, it does not ‘jump’, and so we have
S̃Ã = 0 .

28

(125)

## PDF page 29

SciPost Phys. 16, 103 (2024)

Table 4: The coefficients un,m expressed in terms of the parameters τk of the full
quantum prepotential transseries, which follows from considering (44) with D = 12 ∂∂t
and G = 12 F ′ .
m

0

1

2

u1,m

− 21

u2,m

τ2
4

u3,m

− 63

− 28 1

− 481

u4,m

τ4
8

τ22
τ3 τ1
12 + 32

τ2 τ21
32

u5,m

− 105

3

4

τ

τ

τ

τ21
8
τ3

τ τ

τ τ

4 1
− 16
−

τ τ2

τ3 τ2
24

3 1
− 48
−

τ41
384
τ22 τ1
64

τ τ3

2 1
− 192

τ5

1
− 3840

At the two-instanton level we observe a jump in the coefficient u2,0 , which must be the conse˙ 2Ã acting on the perturbative energy E, which we can think of (see also figure 6)
quence of ∆
as E0,−1 . This implies
2
S̃2Ã = − .
(126)
iπ
By extending this procedure to the higher orders we are led to infer that
¨
S̃l Ã =

0,

l odd,

2(−1)l/2
,
πi

l even.

(127)

At first sight, this seems to be at odds with results [24] obtained using numerical methods, but
the reason for this apparent discrepancy is that the we are working with the ‘wrong’ normalisation Ã = 21 t D,0 (E). In order to derive the Stokes data in the ‘correct’ normalisation, we need
to consider the minimal transseries, which we demonstrate in the next subsection.
Let us end the discussion of the full transseries by pointing out an elegant feature it has.
One could wonder what happens to the transseries for the energy (117) or the (full) quantum
prepotential (121) if we take the unquantised variable t and rotate it once around the origin
t = 0 in the complex t-plane. Performing such a rotation, we find that the classical dual period
t D,0 (t) obtains a shift:
1
1
1
t D,0 (t) → t D,0 (e2πi t) = t D,0 (t) + 2πi t ,
2
2
2

(128)

whereas its quantum corrections are invariant. For our transseries, this means that the nonperturbative sectors effectively obtain an additional factor:
F̃ (n) → F̃ (n) e2πint/ħh ,

or equivalently

E (n) → E (n) e2πint/ħh .

(129)

It is then after quantising t that all instanton sectors get a factor (−1)n , and so the monodromy
in the t-plane effectively swaps parity.21 In terms of parameters τk , this action swaps the sign
Note that for the cubic oscillator, the instanton corrections have A = t D,0 (t) as the ‘primitive’ action, and
therefore its energy transseries is invariant under a full rotation of t.
21

29

## PDF page 30

SciPost Phys. 16, 103 (2024)

Figure 6: The alien lattice of the ordinary energy transseries of the double well potential as follows from (132). The even sectors and any Stokes derivatives connecting
them are red, whereas all odd sectors and their alien derivatives are blue.
of all odd-k parameters. From a more mathematical point of view, we therefore arrive at the
conclusion that there are two types of actions (or automorphisms) on the space of transseries
spanned by the parameters τk : A Stokes phenomenon in the ħ
h-plane which affects the even
transseries parameters, and a monodromy in the t-plane which affects the odd transseries
parameters.

4.2

The minimal transseries

We now turn to the minimal quantum prepotential transseries F̂ min . This transseries contains
only sectors associated to singularities that appear in the Borel plane of its perturbative series,
and therefore a natural Ansatz is
F̂ min =

∞
∑

F (n) ,

with

F (n) ∼ λn .

(130)

n=0

Note how the n-th instanton correction F (n) to the quantum prepotential F̂ min runs parallel
with the 2n-th instanton correction F̃ (2n) of the full transseries F̂ full – but be aware that they
are not equal, as we will see shortly. Let us stick to the definition (123) for the building blocks
En,m of the energy transseries – where in particular, n still denotes the power of λ1/2 . Under
our Ansatz for the minimal quantum prepotential transseries, our alien calculus with A = t D,0
now leads to
S (−1)l ∂ E l
˙ lA E = lA
∆
λ ,
(131)
l
∂t
where the Stokes constants Sl A are once again defined by (46) and are associated to the
minimal quantum prepotential transseries. This is the same expression as the one we found

30

## PDF page 31

SciPost Phys. 16, 103 (2024)

Table 5: On the left the coefficients un,m that appear in the minimal quantum prepotential transseries. On the right those same coefficients expressed in terms of the
parameters τk of the full quantum prepotential transseries.

m

0

1

2

u1,m

0

u2,m

i
∓ 4π

0

u3,m

0

0

0

u4,m

i
∓ 8π

1
− 32π
2

0

u5,m

0

0

u6,m

i
∓ 12π

1
32π2

...

0

1

2

...

0
τ2
4

0

0

0

0

...

τ4
8

τ22
32

0

...

0

...

0

0

0

...

i
± 384π
3

...

τ6
12

τ4 τ2
32

τ32
384

...

for the cubic in (90) and it generalises straightforwardly to
˙
∆l A En,m =

Sl A (−1)l
En+2l,m+1 .
l

(132)

Comparing the constants Sl A with the ambiguities in table 3 then leads to the following value
for the Stokes constants:
1
Sl A = −
,
(133)
2πi
which are the expected values, now matching the numerical results of [24]. Note that the
Stokes constants, which are defined in relation (46), depend on the normalisation of the instanton sectors which itself is implicitly determined by the labelling of the sectors. From the factor
(−1)l+1 / l 2 in (127) we can see how replacing Ã by A = 2Ã changes the Stokes constants.
In the large order analysis of [24], the first singularity in the Borel plane of the perturbative
series is naturally identified with the first instanton correction, and hence the Stokes constants
of the minimal quantum prepotential transseries given above emerge in their computation.
Now that we have obtained the Stokes data of the minimal transseries F̂ min , we would
like to construct the minimal transseries itself. In order to do so, we recall equation (116),
whose solution ∆t allows for the construction of the full transseries.22 This equation can be
separated into even and odd powers of the nonperturbative transmonomial λ1/2 , and summing
those contributions into separate terms yields






1
1
1
ħ
h
∆t = ±
ħ
h log 1 + e− ħh t D (t+∆t;ħh) +
arctan −ε e− 2ħh t D (t+∆t;ħh) ,
(134)
4πi ⏟
⏞⏞
⏟ ⏟2π
⏞⏞
⏟
∆t DDP

∆t med (ε)

where we used (±)2 = 1. This expression is extremely useful because it splits the nonperturbative correction ∆t coming from the quantisaton condition into a ‘resurgence’ piece ∆t DDP
22
At this point we are going to allow ourselves to be sloppy with the language: We will speak of full and minimal
transseries without specifically refering to E or F , since both quantities are similar and closely related due to the
PNP relation.

31

## PDF page 32

SciPost Phys. 16, 103 (2024)

and a parity-dependent piece ∆t med (ε). The former piece contains only even powers of the instanton transmonomial and therefore determines the values of all the r2k (or equivalently τ2k )
in (119), which are solely responsible for the Stokes phenomenon – note also the similarity to
(60) for the cubic. The latter piece, ∆t med (ε), where ‘med’ stands for median, is responsible
for all the r2k−1 (or τ2k−1 ) and is real and unambiguous, but parity dependent. Its name and
role will be explained in a moment.
Let us for the moment focus on the first piece and consider the new equation






1
1
1
∆t = ±
(135)
∆t DDP = ±
ħ
h log 1 + e− ħh t D (t+∆t;ħh) .
4πi
4πi
We use the approach of section 3.5 again for this ‘partial’ ∆t: consider ϕ(∆t) = F ′ (t + ∆t; ħ
h),
calculate the transseries extension for the quantum dual period F ′ (t; ħ
h) and integrate the result
with respect to t. This yields a transseries that we call F̂ min – as we will justify shortly – and
which only contains integer powers of λ. The result is



m−1
∞
n−1
∑
∑
1
1
∂
2
2
F̂ min = F + ħ
h
h
− un,0 λ 2 n +
un,m ħ
F ′′ λ 2 n ,
(136)
n
∂
t
n=1
m=1
where the un,m receive as input data


1
(−1)k
∓
,
k
4πi
r2k−1 = 0 ,
r2k =

(137)

for positive integers k. In table 5 we have displayed both the coefficients un,m and τk that
appear in this transseries; note in particular that all un,m with odd n vanish, so that indeed only
integer powers of λ survive in the minimal transseries. We want to argue that this transseries is
in fact the minimal transseries associated to the perturbative quantum prepotential F : First of
all note that all the sectors in the transseries are closed under the action of the alien derivatives
as described by equation (132). Secondly, one can check that the ambiguities in table 5 are
i
consistent with the Stokes constants (133). For example, from (132) we get ˙
∆2A E = 4π
E2,0 ,
which explains the observed ambiguity for u2,0 in table 5.
The minimal transseries admits the same generic one-parameter transseries structure in
terms of a single parameter σ as we found for the cubic:




∞
n−1
∑
∑
1
∂ m−1 ′′ n
2
min
n
m+1
F̂ (t, σ; ħ
h) = F + ħ
h
− u2n,0 σλ +
u2n,m σ
ħ
h
F λ ,
(138)
n
∂t
n=1
m=1
where now u2n,m is computed using r2k =
a ‘minimal energy transseries’
Ê

min

(t, σ; ħ
h) = E + ħ
h

(−1)k
k . Analogously, for the same values r2k , there is

n−1
∞ ∑
∑

u2n,m σ

n=1 m=0

m+1



∂ m ′ n
ħ
h
Eλ ,
∂t

(139)

which has a form identical to that of the one-parameter transseries (94) that we found in the
cubic model. We can then check explicitly that


1
min
S0 E(t; ħ
h) = Ê
t, −
;ħ
h ,
(140)
2πi
and hence (139) truly is the minimal transseries extension associated to the perturbative energy. In the same way, we can verify that


1
min
S0 F (t; ħ
h) = F̂
t, −
;ħ
h .
(141)
2πi
32

## PDF page 33

SciPost Phys. 16, 103 (2024)

1
Furthermore, table 5 simply depicts the coefficients un,m σ m+1 of the transseries Ê min (t,±4πi
;ħ
h).
Both transseries (138) and (139) can also be generated using our algorithm by redefining
∆t in equation (135) as


1
∆t(σ) = σ ∆t DDP = σ ħ
h log 1 + e− ħh t D (t+∆t(σ);ħh) ,
(142)

which allows us to produce the generic one-parameter transseries in one fell swoop. For example, we have
Ê min (t, σ; ħ
h) = E(t + ∆t(σ); ħ
h) .
(143)
for the one-parameter energy transseries.

4.3

The full transseries as a sum of minimal transseries

The minimal transseries discussed in the previous subsection contains only a subset of all
nonperturbative sectors of the full energy or quantum prepotential transseries that we are
interested in and that we discussed in section 4.1. However, we can write the full transseries
as a sum of minimal transseries, and when we do so an interesting structure emerges: The full
transseries ‘factorises’ in terms of a minimal transseries and another transseries that we will
call ‘median transseries’.
To arrive at this conclusion, we first observe that each sector En,m gives rise to a minimal
transseries extension of itself:


1
1 2
S0 En,m = En,m − SA En+2,m+1 +
(144)
S2A En+4,m+1 + SA En+4,m+2 + . . .
2
2
We would like to argue that our algorithm with ∆t(σ) from (142) can produce the generic
one-parameter minimal transseries which describes this Stokes phenomenon. To this end, let
us define the transseries
min
(t, σ; ħ
h) = En,m (t + ∆t(σ); ħ
h) .
(145)
Ên,m
Then, given definition (123), we also have


n
min
min
(t, σ; ħ
h) = (ħ
h∂ t )m ∂ t Ê min (t, σ; ħ
Ên,m
h)e− 2ħh ∂ t F̂ (t,σ;ħh) .

(146)

When we expand the right hand side of this equation using (138) and (139) in powers of the
transmonomial λ and regroup the resulting expression in terms of building blocks (123), we
find for the first few orders that


1
1 2
min
Ên,m (t, σ; ħ
h) = En,m − σEn+2,m+1 +
σEn+4,m+1 + σ En+4,m+2 + . . .
(147)
2
2
As advocated, this captures the action of the Stokes automorphism in (144):
min
min
S0 Ên,m
(t, 0; ħ
h) = Ên,m
(t, SA ; ħ
h) ,

(148)

where we use the fact (133) that all Sl A are equal. The minimal transseries extension (147)
of generic nonperturbative sectors can actually be written in closed form as
min
Ên,m
(t, σ; ħ
h) = En,m +

′
∞ n∑
−1
∑

′

un′ ,m′ σ m +1 En+n′ ,m+m′ +1 ,

(149)

n′ =1 m′ =0
(−1)k

with the un′ ,m′ defined by r2k = k and r2k−1 = 0. This expression also covers the original
minimal transseries E min (σ) given in (139) if we identify E0,−1 with the perturbative energy E.
33

## PDF page 34

SciPost Phys. 16, 103 (2024)

Note how this is indeed the natural identification from the alien calculus point of view – see
for example figure 6.
To retrieve the full transseries as a sum of minimal transseries, we then need to know
min
which minimal transseries Ên,m
we need to sum. This is where the second piece of the right
hand side of equation (134) comes into play: let us define
∆t(ε) = ∆t med (ε) =



1
ħ
h
arctan −ε e− 2ħh t D (t+∆t(ε);ħh) .
2π

(150)

Then, following the by now familiar procedure outlined in section 3.5, with
ϕ(∆t(ε)) = E(t + ∆t(ε); ħ
h), we obtain:


∞
n−1
∑∑
∂ m ′ n/2
med
Eλ ,
(151)
Êε (t; ħ
h) = E + ħ
h
u2n,m (ε) ħ
h
∂t
n=1 m=0
with input data
r2k = 0 ,
r2k−1 =

ε (−1)k
,
2π 2k − 1

(152)

for positive integers k, which follows from comparing (150) to (119). The coefficients un,m
for this ‘median’ transseries are displayed in table 6. Note that this transseries is completely
real and unambiguous and its median resummation (see e.g. [17, 49]) provides the easiest
way to obtain the real energy spectrum of the physical quartic oscillator to numerically high
precision.23 We elaborate on this statement in appendix C.
Now we are ready to formulate the full transseries as a sum of minimal transseries. First,
we note that the true equation for ∆t given in (134) can be extended to the two-parameter
generalisation
∆t(σ, ε) = σ∆t DDP + ∆t med (ε)
(153)




1
1
ħ
h
= σħ
h log 1 + e− ħh t D (t+∆t(σ,ε);ħh) +
arctan −ε e− 2ħh t D (t+∆t(σ,ε);ħh) .
2π
1
We can retrieve (134) by setting σ = ∓ 4πi
in the above definition. We can then formulate a
two-parameter transseries for the full energy transseries:

h)
Êεfull (t, σ; ħ
h) = Êεmed (t + σ∆t DDP ; ħ
= Ê

min

∞ ∑
n−1
∑



n
min
∂ m
(σ) + ħ
h
un,m (ε) ħ
h
∂ t Ê min (σ)e− 2ħh ∂ t F̂ (σ)
∂t
n=1 m=0

= Ê min (σ) + ħ
h

∞ ∑
n−1
∑

min
un,m (ε) Ên,m
(σ) ,

(154)

n=1 m=0

with the rk defined in (152). This is the sum of minimal transseries that we advocated at the
start of this subsection. Upon close inspection, one can recognize this structure in table 4: With
every unique product of parameters τ2k−1 with odd indices we can identify a minimal resurgent
min
min
transseries En,m
in the sum (154). For example, the minimal resurgent transseries Ê1,0
is based
on τ1 , and is constructed from those sectors that carry factors { τ1 , τ1 τ2 , τ1 τ4 , τ1 τ22 , . . .},
where τ1 is only multiplied by further τ2k with even indices. The corresponding sectors are
{E1,0 , E3,1 , E5,1 , E5,2 , . . .} respectively. Note that conversely, this construction also allows us to
Alternatively, one can consider exact perturbation theory [50, 51] which approximates these physical values
without the use of transseries altogether.
23

34

## PDF page 35

SciPost Phys. 16, 103 (2024)

write the full energy transseries as a sum of median transseries, weighted by the un,m of the
minimal transeries (137) – since we can identify a median transseries with a unique product
of even τ2k . Heuristically, we have
Full transseries ≃ Minimal transseries ⊗ Median transseries.
That the full transseries can be written as a sum of minimal transseries was to be expected:
if a transseries is not minimal, one should at least be able to partition it into separate parts that
are minimal. What is striking however is that it truely factorises, in the sense that all minimal
transseries extensions of the sectors in the median transseries have the same structure (149).
The full transseries is really a ‘product’ of both structures, which can be best understood from
the split form of the shift ∆t(σ, ε) in (153).
We conclude this section by highlighting some properties of our two-parameter transseries.
First of all, let Eε,N denote the physical values of the nonperturbative energy levels of the
symmetric double well potential. These are obtained from our two-parameter transseries in
the following way:
 


1
1
Eε,N (ħ
h) = S0± Êεfull ħ
h N+
,±
;ħ
h .
(155)
2
4πi
Note that the answer depends on the quantum numbers (ε, N ), but is independent of the
resummation prescription ±, as long as we pick the corresponding value for the transseries
parameter. In the language of resurgence, the Stokes phenomenon that we observe along
the Stokes ray arg(ħ
h) = 0, and which takes us from the Dε+ = 0 to the Dε− = 0 quantisation
condition (113), is captured by


1
1
S0 Êεfull (t,
;ħ
h) = Êεfull t, −
;ħ
h .
(156)
4πi
4πi
The monodromy of the transseries under the rotation t 7→ t e2πi that we discussed earlier also
has a clear manifestation in the two-parameter transseries setting: it acts as
full
(t, σ; ħ
h) .
h) → Ê−ε
Êεfull (t, σ; ħ

(157)

The last property we want to mention is that the minimal and median transseries are easily
obtained from the full two-parameter transseries when we set24 ε or σ to zero respectively:
Ê0full (t, σ; ħ
h) = Ê min (t, σ; ħ
h) ,
h) = Êεmed (t; ħ
h) .
Êεfull (t, 0; ħ

(158)

Of course, all the properties we have mentioned here for the energy transseries can similarly
be deduced for a full two-parameter quantum prepotential transseries F̂εfull (t, σ; ħ
h).

5

The cosine potential

The last example that we want to discuss is the periodic cosine potential
V (x) = 1 − cos(x) ,

(159)

which in the literature is also sometimes called the sine-Gordon potential and its Schrödinger
equation the Mathieu equation. We have two reasons for studying this potential: first, to
Note that physcially ε cannot be set to zero, so this is only mathematical trick to illustrate the factorisation of
the full transseries in terms of the minimal and median transseries.
24

35

## PDF page 36

SciPost Phys. 16, 103 (2024)

Table 6: Values for the coefficients un,m in the median energy transseries of the double
well potential.
m

0

1

2

3

u1,m

1
− 2π
ε

u2,m

0

1
8π2

u3,m

1
6π ε

0

1
− 48π
3 ε

u4,m

0

1
− 12π
2

0

1
384π4

u5,m

1
− 10π
ε

0

1
ε
48π3

0

4

1
− 3840π
5 ε

demonstrate that the intricate transseries structure of the energy of the double well potential
occurs more generally and also applies to the cosine potential. Secondly, in the cosine potential the energy eigenstates are labeled by a continous periodic parameter θ that allows us to
identify and compare topological sectors to transseries sectors.
We take 0 < E < 2 so that the turning points are real, and start by formulating the exact
quantisation condition for the potential, which can be computed using the aforementioned
techniques and which can be found in [14, 27, 52]. To keep the notation tidy, we express the
quantisation conditions in terms of Voros symbols (27):
q
Dθ± = 1 + VA∓1 (1 + VB ) − 2 VA∓1 VB cos(θ ) = 0 ,
(160)
where VA and VB are the Voros symbols associated to the perturbative and tunneling cycles
respectively. As with the doublep
well, we observe a single tunneling contribution from the fact
that there is a power of 21 in the VB in the above equation, hinting at a similar full transseries
structure to the one we found for the double well potential. There is however also a novelty
here: Compared to the double well potential, for which the basis states are labeled by the
parity ε which takes on two values – and which relates to the Z2 symmetry of the potential –
we now have states labeled by the so-called Bloch angle θ which takes any value between 0
and 2π – and which relates to the Z translational symmetry of the potential. The Bloch angle
originates from the Bloch boundary condition on the wave functions,
ψ(x + 2π) = eiθ ψ(x) ,

(161)

which gives rise to the quantisation condition above – see e.g. [52]. At the perturbative level –
that is, ignoring as before all factors of VB – the quantisation condition becomes θ -independent
and reduces to


1
∓1
1 + VA = 0 , implying t = ħ
h N+
.
(162)
2
Subsequently, promoting t to t̂ = t + ∆t in the same manner as before, we can reduce the

36

## PDF page 37

SciPost Phys. 16, 103 (2024)

Figure 7: On the left we draw the cosine potential (159), and on the right some of its
infinite number of turning points in the complex x-plane, with the cycles γA and γB .
exact quantisation condition25 to an equation for ∆t. This leads to
∆t = ∓

Æ


iħ
h
log ±i cos(θ ) e−t D (t+∆t;ħh)/2ħh + 1 + sin2 (θ ) e−t D (t+∆t;ħh)/ħh .
π

(164)

We then solve the above equation by using our algorithm and produce a transseries for the
energy. Note that in the equation above, we again have an instanton transmonomial with 12 t D
in the exponent, and hence the correct Ansatz for the full energy transseries is
∞ ∑
n−1
∑



 
∂ m ∂ E 1n
2
,
Ê = E + ħ
h
un,m ħ
h
λ
∂t
∂t
n=1 m=0

(165)

1

which contains an expansion in λ 2 . Our algorithm computes the coefficients un,m which are
tabulated in table 7.
A few comments are in order. At the nonperturbative level, the energy levels spread out
into continuous bands that are doubly degenerate (Eθ = E−θ ), contrary to the double well,
whose energy levels are nondegenerate at the nonperturbative level. Every energy level in a
band is characterised by its Bloch angle θ , and the edges of the bands correspond to θ = 0
(upper bound) and θ = π (lower bound). When we set θ = 21 π or θ = 32 π, we retrieve the
minimal transseries, as we will explain shortly. Another interesting feature is the rotation of
the period t around the origin in the complex plane, which produces a factor (−1)n for the
instanton sector E (n) after quantisation (162). Given the structure of the energy transseries
(table 7), one can easily see that effectively, this monodromy can be effectuated by sending
θ 7→ θ + π.
As explained in [15], the Bloch angle θ can be incorporated into a path integral description of the problem by adding a topological term to the action. From this perspective, the
θ -dependence of the nonperturbative corrections indicates which saddle point solution is responsible for a particular nonperturbative correction. When a solution tunnels to the right
(left) it obtains a factor eiθ (e−iθ ) and we can assign it a charge +1 (−1). These solutions
are often called (anti-) instantons in the literature. We can then assign a total charge to every saddle point solution which is a composition of instantons and anti-instantons, and in this
way distinguish different topological sectors of solutions. It naturally follows that resurgence
can only mix transseries sectors in the same topological sector, as resurgence analysis of ħ
hexpansions is completely independent of θ . This notion is often graphically depicted in what
25

In doing so one must be careful with the branch of the square root:
q
VA±1 = ±ie±πi∆t/ħh .

(163)

In principle, one should also have a factor of (−1) on the right hand side of this expression, but we can absorb
this into cos θ by a suitable redefinition of θ .
N

37

## PDF page 38

SciPost Phys. 16, 103 (2024)

is called the resurgence triangle [26, 27]. In this section we wish to understand the relation
between topological sectors and transseries sectors.
Let us take a closer look at ∆t, and at the rk that it produces in equation (119). We can
again split ∆t into two parts: a resurgence part ∆t DDP and median part ∆t med , which generate
the even r2k and odd r2k−1 respectively. For the cosine potential, this decomposition reads


1



 ħ
1
e− 2ħh t D (t+∆t;ħh)
h
− ħ1h t D (t+∆t;ħ
h)
∆t = ±
ħ
h log 1 + e
.
(166)
+ arcsin cos(θ ) Æ
2πi ⏟
h)
− ħ1h t D (t+∆t;ħ
⏞⏞
⏟ π
⏟
⏞⏞1 + e
⏟
∆t DDP
∆t med

Remarkably, the form of equation (164) is such that in the expansion all contributions conspire
to cancel the θ dependence of the r2k , and hence the first term on the right hand side of the
above equation is also independent of the angle. From the point of view developed in the
previous section, this is exactly as one would expect: the r2k should parametrize the Stokes
phenomenon, and hence we expect them to be ambiguous but independent of the Bloch angle
θ . In fact, the ∆t DDP in the present context is identical to the one in (134) for the double well
potential. The only subtle difference is that its prefactor is twice the prefactor in (134), which
is a consequence of the fact that the Stokes constants Sl A in the cosine potential are twice the
size of the Stokes constants of the double well potential. Let us derive this fact: if we consider
the minimal transseries extension of E, and its associated minimal quantum prepotential
F

min

=

∞
∑

F (n) ,

with

F (n) ∼ λn ,

(167)

n=0

then we can map the alien calculus (46) of the quantum prepotential back to the energy via
the PNP relation. Following the by now familiar procedure, we obtain the same relations as
for the double well, which read
˙
∆l A En,m =

Sl A (−1)l
En+2l,m+1 ,
l

(168)

where the En,m are defined as in (123). Comparing this to the entries in table 7 leads to the
Stokes constants
1
Sl A = − ,
(169)
πi
Table 7: Values of the coefficients un,m for the full energy transseries of the cosine
potential. The index n labels the rows, m labels the columns and Θ = cos(θ ).
m

0

E (1)

1
πΘ

E (2)

i
∓ 2π

E (3)

1
− 6π
Θ3 − 3Θ

E (4)

i
± 4π

E (5)

1
40π

1

2

3

4

1
Θ2
2π2

∓ 2πi 2 Θ



3Θ5 − 10Θ3 + 15Θ

1
24π2



1
Θ3
6π3

4Θ4 − 12Θ2 − 3

1
3
∓ 12π
2 Θ − 6Θ



38

∓ 4πi 3 Θ2


1
24π3

2Θ5 − 6Θ3 + 3Θ

1
Θ4
24π4



i
3
∓ 12π
4Θ

1
Θ5
120π5

## PDF page 39

SciPost Phys. 16, 103 (2024)

Table 8: Values of the coefficients un,m for the median energy transseries of the cosine
potential. The index n labels the rows, m labels the columns, and Θ = cos(θ ).
m

0

u1,m

1
πΘ

u2,m

0
1
6π

u3,m

1
40π

2

3

4

1
Θ2
2π2



3Θ5 − 10Θ3 + 15Θ

1
Θ3
6π3

0
1
24π2

0

u4,m
u5,m

Θ3 − 3Θ

1



4Θ4 − 12Θ2


1
24π3

0

1
Θ4
24π4

0
2Θ5 − 6Θ3



0

1
Θ5
120π5

which indeed are twice the Stokes constants we found for the cubic (93) and double well
potential (133). The geometrical reason for this factor of two is the fact that the A-cycles in
the cosine potential intersect not one but two B-cycles – see figure 7.
Let us now focus on the median part of ∆t, which is the second term on the right hand
side of (166) and which generates all odd r2k−1 . If we restrict ourselves to


1
ħ
h
e− 2ħh t D (t+∆t(θ );ħh)
∆t(θ ) = ∆t med (θ ) = arcsin cos(θ ) Æ
,
(170)
π
h)
− ħ1h t D (t+∆t(θ );ħ
1+e
then we find the coefficients un,m in table 8 that define the median energy transseries for cosine
potential. As with the double well, when we enhance these sectors in the median transseries
to their respective minimal transseries extensions, we obtain the full transseries.
We now want to address the question of whether and how topological sectors relate to
transseries sectors. Let us first remark that generally we cannot assign a single topological
charge to a transseries sector: the coefficients un,m are polynomials in cos(θ ) = 21 (e iθ + e−iθ )
and therefore we assign multiple topological charges (or sectors) to a single transseries sector.
As we argued before, a necessary condition for resurgence to connect two transseries sectors
is for these sectors to share a topological charge – i.e. they must share the same power of eiθ in
their un,m . The median transseries, however, indicates that this is not a sufficient condition: We
can observe that several transseries sectors share similar powers of eiθ , yet are disconnected
in a resurgence sense. For example, the two-instanton sector E2,1 is fully invisible to the perturbative series E, yet it contains a constant part which has topological charge 0. Therefore,
we can conclude that a single topological sector within the energy transseries is not connected
from a resurgence perspective and moreover that the resurgence triangle does not partition
the full transseries to single minimal transseries.
Curiously, the structure of the median energy transseries for the cosine potential is to a
certain extent identical to that of the double well: their median transseries are constructed
from the same nonzero coefficients un,m , even though the values of these coefficients are different. We thus observe that despite the different topological nature of both quantum systems
(one potential having a quantum number coming from a Z2 reflection symmetry, the other
having one coming from a Z translational symmetry), the resurgent structures of their respective transseries are qualitatively identical. For example, the alien lattice of the double well as
graphically depicted in figure 6 describes the energy transseries of the cosine potential equally
39

## PDF page 40

SciPost Phys. 16, 103 (2024)

well. The qualitative distinction does not lie in the transseries expression for an individual
energy eigenstate. Rather – as also described in [52] for periodic potentials with N minima on
a circle – the topology affects the structure26 of the basis of energy eigenstates for the Hilbert
space.
Let us wrap up this discussion by generalising the above transseries to a two-parameter
transseries. We first note that the minimal transseries expression for the cosine potential has
the same universal form (139) as the double well (and cubic) potential, with r2k =
r2k−1 = 0. We then introduce
∆t(σ, θ ) = σ∆t DDP + ∆t med (θ ) ,

(−1)k
and
k

(171)

and we write the full energy transseries as a sum of minimal transseries weighed by the un,m
of the median transseries. That is:
Êθfull (t, σ; ħ
h) = E(t + σ∆t DDP + ∆t med (θ ); ħ
h)
= Ê

min

(σ) + ħ
h

∞ ∑
n−1
∑

min
un,m Ên,m
(σ) ,

(172)

n=1 m=0
min
where the Ên,m
are the minimal transseries extensions of their respective transseries sectors as
explained in the previous section. The physical energy levels that fill the energy bands of the
cosine potential are then given by
 


1
1
h N+
Eθ ,N = S0± Êθfull ħ
,±
;ħ
h ,
(173)
2
2πi

where N is a nonnegative integer – see footnote 12. Finally, we note that the Stokes phenomenon that maps the quantisation condition D+ = 0 to D− = 0 corresponds to


1
1
S0 Êθfull (t, +
;ħ
h) = Êθfull t, −
;ħ
h ,
(174)
2πi
2πi
and that the minimal transseries is obtained from setting θ = 12 π or θ = 23 π and the median
transseries from setting σ = 0.

6

Conclusion

In this paper we have extended the computation of nonperturbative energy spectrum corrections for one-dimensional quantum oscillators to all orders, and unified them in a single
transseries description. Using alien calculus, we have dissected the Stokes phenomenon and
computed the asociated Stokes constants in two different ways. For the cubic oscillator we
found that the transseries is minimal, and as a result it can be generalised to a one-parameter
transseries which fully describes the Stokes phenomenon along the positive real ħ
h-axis. For the
double well and cosine potentials, we have nonperturbative corrections associated to instanton
solutions that tunnel an odd number of times, and therefore the resulting transseries structure
is no longer minimal. We have demonstrated that this more complicated transseries structure
can be captured in terms of a two-parameter transseries which ‘factorises’ into a minimal and
a median transseries.
One question left open by our work concerns the median transseries of sections 4 and
5, which consist of a countably infinite number of nonperturbative sectors that need to be
26

See also [53] for a recent discussion on the similarities between oscillators with distinct vacuum structures.

40

## PDF page 41

SciPost Phys. 16, 103 (2024)

resummed. The resurgence triangle, though helpful, does not conclusively explain this structure. In quantum field theory, for the O(N ) non-linear sigma model, it was shown [54] that
the ambiguity-free transseries whose median resummation produces the physical value for the
energy density – and which is the analogue of the median transseries described here – consists of a finite27 number of sectors. It would be interesting to understand from a topological
point of view why in this respect, one-dimensional quantum mechanics models seem more
complicated than their quantum field theory cousins.
There are several other directions that we think deserve further investigation. For one,
it would be interesting to extend our analysis of the Stokes phenomenon for the minimal
quantum prepotential transseries to all directions in the complex ħ
h-plane. In the quantum
mechanical examples discussed here, within the parameter regime where all turning points
are real, this would involve four Stokes rays corresponding to four primitive instanton actions
A = ±t 0 and A = ±t D,0 , that we suspect would lead to a four-parameter transseries in the
minimal case. One could then cover its complete alien calculus including the so-called ‘backwards resurgence’ [30] and inspect the action of the monodromy from rotation in the complex
t-plane on this transseries.
Finally, another interesting direction would be to explore the connection between parametric resurgence and wall-crossing. As is well-known [55, 56], the Borel planes of the quantum
periods t(E; ħ
h) and t D (E; ħ
h) change drastically as we cross certain codimension 1 walls that
lie in the complex E-plane. From a physics point of view [57, 58], these are walls of marginal
stability and the singularities in the Borel plane correspond to the BPS states of an associated
supersymmetric gauge theory. The wall-crossing formula [59] then tells us how the spectrum of BPS states changes as we cross these walls in the moduli space parameterized by E.
From a resurgence point of view, this phenomenon was also encountered in [60] where these
same walls were called higher order Stokes curves and the phenomenon was interpreted using
the multi-sheeted Borel plane. It would be interesting to revisit this perspective and study the
wall-crossing phenomenon also in terms of parametric resurgence and the minimal transseries
structures that we uncovered in this work.

Acknowledgments
We would like to thank Tomás Reis and Marco Serone for useful comments and discussions,
and Marcos Mariño for reading and commenting on the final draft of this paper. AvS would
like to thank Giulio Bonelli and the TPP group at SISSA for their hospitality during the spring
of 2023 when a significant part of this research was conducted.
Funding information The research of AvS was supported by the grant OCENW.KLEIN.128,
‘A new approach to nonperturbative physics’, from the Dutch Research Council (NWO).

A

On the PNP relation

The PNP relation is essential in establishing the connection between the energy E and the
quantum prepotential F . In this appendix we provide some more background information on
this relation and show its derivation for polynomial potentials. The relation as used in this
For N ≥ 4 it consist of one part, like in our cubic model. For the ‘special’ N = 3 case, it consist of three parts
that need to be median resummed.
27

41

## PDF page 42

SciPost Phys. 16, 103 (2024)

paper reads
∂E
∂ 2F ∂ F
∂ 2F
=t 2 −
+ħ
h
,
∂t
∂t
∂t
∂ t∂ ħ
h

(A.1)



∂
∂
cE = t
−2+ħ
h
F + C(ħ
h) .
∂t
∂ħ
h

(A.2)

c
or in its integrated version

An alternative common formulation of the PNP relation is one in which the anharmonic coupling g appears. Under the rescaling
x 7→ x g ,

p 7→ p g ,

E 7→ E g 2 ,

(A.3)

we note that the WKB curve Σ in (22) remains invariant when we modify the potential appropriately, e.g. we have
Vcubic =

x2
− g x3 ,
2

and

Vdw =

x2
(1 + g x)2 .
2

(A.4)

One can then set ħ
h = 1 and use g as the expansion parameter, thereby turning the energy E
and quantum prepotential F into asymptotic expansions in g 2 with coefficients depending on
t. The integrated version of the PNP relation (A.2) then becomes


1 C(g 2 )
4 ∂F
E=
+g
,
(A.5)
c
g2
∂ g2
where the t-independent integration constant now appears as C(g 2 ).
The PNP relation is essentially a Riemann bilinear identity: in [61] a derivation of this
statement was given and a refinement of that same computation was provided in [62]. We
would like to improve on these results by repeating the computation for arbitrary genus – which
is rather trivial – and by explicitly calculating the constant c which was left undetermined in
the former two computations. Before doing so, let us remark that the PNP relation (A.1) can
be cast into the form of a quantum corrected Wronskian condition [36]:




∂t
∂ t ∂ tD
∂t
t −ħ
h
− tD − ħ
h D
= c.
(A.6)
∂ħ
h ∂E
∂ħ
h ∂E
In order to obtain this equation, one exchanges the independent variables (t, ħ
h) for (E, ħ
h), as
explained in [63] section 5. This version of the PNP relation makes the connection to the
Riemann bilinear identity manifest, and in what follows we will derive the latter form of the
equation, knowing that we can always map it back to (A.1).
For a genus g Riemann surface, the Riemann bilinear identity (see e.g. [64]) for two meromorphic one-forms ω1 , ω2 is given by


∮
∮
∮
g
∑ ∮
∑
ω1
ω2 −
ω2
ω1 = 2πi
Res f ω2 ,
(A.7)
i=1

Ai

Bi

Ai

Bi

poles

where the sum on the right hand side is over poles of both ω1 and ω2 and locally near each
pole one chooses f such that ω1 = d f . The Ai , B j ∈ H1 (Σ) form a symplectic basis of onej
cycles for the first homology group of the surface: 〈Ai , A j 〉 = 〈B i , B j 〉 = 0 and 〈Ai , B j 〉 = δi .
In our case, the Riemann surface we are interested in is of course the WKB curve. Let the
function S(x, ħ
h) be a solution to the Riccati equation
S 2 − iħ
h

dS
= 2(E − V (x)) .
dx
42

(A.8)

## PDF page 43

SciPost Phys. 16, 103 (2024)

Then we can slightly modify the Riccati solution by defining S̃ = ħ1h S which therefore solves
2
dS̃
= 2 (E − V (x)) .
dx
ħ
h

(A.9)


∂ S̃
ω1 =
dx ,
∂ħ
h


∂ S̃
dx .
ω2 =
∂E

(A.10)

S̃ 2 − i
Now choose the one-forms



In what follows, we will show that with these two one-forms, the Riemann bilinear identity
(A.7) is equivalent to the quantum corrected Wronskian condition (A.6). In order to compute
the residue on the right hand side of the Riemann bilinear identity, we use the argument of [61]
which tells us that the Riccati solution only has a pole at infinity.
From the Riccati equation we can deduce the large x scaling behaviour of the one-forms.
Without loss of generality, by scaling and shifting x we can write the large x behaviour of a
polynomial potential as

(A.11)
V (x) ≃ x d + a x d−2 + O x d−3 ,
for some number a and an integer d > 2. Using dominant balance arguments (see e.g. [65])
one can then deduce the asymptotic behaviour of the two Riccati solutions:
p 
 1

1
i 2
1 1
S̃ ≃ ±
(A.12)
x 2 d + a x 2 d−2 + O x 2 d−3 .
ħ
h
2
The Riccati equation can be differentiated with respect to either ħ
h or E to obtain
∂ S̃
i d ∂ S̃
2
−
= − 3 (E − V (x)) ,
∂ħ
h 2 dx ∂ ħ
h
ħ
h
∂ S̃
i d ∂ S̃
1
S̃
−
= 2.
∂ E 2 dx ∂ E
ħ
h
S̃

(A.13)

Appyling the same dominant balance techiques then yields
∂ S̃
2
≃ 3 V (x) ,
∂ħ
h ħ
h
∂ S̃
1
S̃
≃ 2,
∂E
ħ
h
S̃

which then gives the scaling behaviour
p


∂ S̃
i 2 1d
1
≃ ∓ 2 x 2 1 + a x −2 + O(x −3 ) ,
∂ħ
h
2
ħ
h


∂ S̃
i
1 −2
− 12 d
−3
≃∓ p x
1 − a x + O(x ) .
∂E
2
ħ
h 2

(A.14)

(A.15)

Using these scaling laws, we can compute the right hand side of the Riemann bilinear identity
(A.7). Let ω1 = d f locally for large x, then


∫ x
p
i 2 1 d+1
1
a x −2
f =
ω1 ≃ ∓
x2
+
+ O(x −3 ) ,
(A.16)
1
ħ
h
d
−
2
d
+
1
2
leading to
f ω2 ≃

1
ħ
h3




2 −3
4a −1
0
z + 2
z + O(z ) dz ,
d +2
d −4
43

(A.17)

## PDF page 44

SciPost Phys. 16, 103 (2024)

where in the last line we switched to coordinates z = 1x . Finally, we take the residue:
∑

2πi

Res f ω2 =

poles

16πia
(d 2 − 4)ħ
h3

.

(A.18)

Note that we count the residue of the pole at infinity (z = 0) twice, since Σ is a double cover
of the Riemann sphere parameterized by x or z.
For the left hand side of the Riemann bilinear identity, we note that
∮


∮
∂ Πγ
1 ∂ Πγ
1
∂ S̃
∂ S̃
=
, and
= − 2 Πγ − ħ
.
(A.19)
h
ħ
h ∂E
h
∂ħ
h
ħ
h
γ ∂ħ
γ ∂E
Putting everything together in terms of A-periods t i and B-periods t Di , we then obtain
g 
∑
i=1

∂ ti
t −ħ
h
∂ħ
h
i



∂ t Di
∂E


−

t Di − ħ
h

∂ t Di
∂ħ
h



8a
∂ ti
= 2
.
∂E
d −4

(A.20)

Restricting ourselves to the genus one case that we are interested in in this paper, the index i
disappears and we conclude that
8a
c= 2
,
(A.21)
d −4
in (A.1) and (A.6). We have checked this quantum corrected Wronskian condition for various
potentials of genus one and higher by matching the constant c derived here to the results
in [36]. For example, the cubic potential (50) and double well potential (112) can be written
in the canonical form (A.11) by an appropriate shift and rescaling, leading to
x
1
−
,
12 108
1
x2
+
.
Vdw (x) = x 4 −
2
16

Vcubic (x) = x 3 −

(A.22)

This implies that
2
1
, and cdw = − ,
15
3
which agrees with the PNP relations featured in e.g. [18, 27, 36].
ccubic = −

B

(A.23)

Stokes phenomena for the quantum prepotential from DDP

In the core of this paper we demonstrated two ways in which the alien calculus for the energy
transseries could be derived: from mapping the alien calculus of the quantum prepotential
(46) to the energy via the PNP relation (section 3.3), or directly from the Delabaere-DillingerPham formula (section 3.4). Here we want to close the circle by showing how the alien calculus
of the quantum prepotential can be derived from the Delabaere-Dillinger-Pham formula. We
will illustrate this in the cubic potential setting (50) for two Stokes lines: the one running
along arg(ħ
h) = 0, studied most in the bulk of this paper, and the one along arg(ħ
h) = 12 π. Let
us remark that the reversed argument, deriving the DDP formula from alien calculus of the
quantum prepotential, was presented already in [24,66], both for quantum mechanics and for
quantum mirror curves.

44

## PDF page 45

SciPost Phys. 16, 103 (2024)

The Stokes phenomenon across arg(ħ
h) = 0: Recall that the Delabaere-Dillinger-Pham formula (31) tells us that in the case of the cubic oscillator, when working in the independent
variables (E, ħ
h), the following Stokes jumps occur along the arg(ħ
h) = 0 ray:

S0 t(E; ħ
h) = t(E; ħ
h) +


iħ
h
log 1 + e−t D (E;ħh)/ħh ,
2π

(B.1)

S0 t D (E; ħ
h) = t D (E; ħ
h) .
We see that the dual period is invariant under the action of the automorphism, and so if we
apply the pointed alien derivative to it – similar to what we did in section 3.4 – then we obtain

0= ˙
∆l A t D (E; ħ
h) = ˙
∆l A F ′ (t; ħ
h)

t=t(E;ħ
h)

+ F ′′ (t(E; ħ
h); ħ
h) ˙
∆l A t(E; ħ
h) ,

(B.2)

where we used (36) to express t D (E; ħ
h) in terms of the quantum prepotential and used the
chain rule (18). This identity allows us to express the alien calculus of the (derivative of the)
quantum prepotential in terms of the alien calculus of t(E; ħ
h). It leads to
(˙
∆l A F ′ ) (t; ħ
h)

t=t(E;ħ
h)

= F ′′ (t(E; ħ
h)); ħ
h)

(−1)l+1 ħ
h −l t D (E;ħh)/ħh
e
.
l
2πi

(B.3)

Then we want to integrate both sides with respect to t, but t is not an independent variable at
this point. Therefore we must first substitute the current independent variable E with E(t; ħ
h)
and obtain
(−1)l+1 ħ
h −l F ′ (t;ħh)/ħh
˙ l A F ′ ) (t; ħ
(∆
h) = F ′′ (t; ħ
h)
e
.
(B.4)
l
2πi
Finally, we can perform the integration with respect to t:
˙ l A F )(t; ħ
(∆
h) =

∫ t



1
(l)
′
′
˙
F + c(ħ
h) ,
dt (∆l A F )(t ; ħ
h) = −
2πi l
′

(B.5)

(l)
where Fl is defined in (47). Note that the pointed alien derivative ˙
∆l A maps each formal
power series in ħ
h to a new formal power series weighted by the transmonomial – schematically:

˙ l A : C[[ħ
∆
h]] −→ C[[ħ
h]] e−l A/ħh .

(B.6)

Therefore, the integration constant c(ħ
h) in (B.5) must be of the form
c(ħ
h) = c̃(ħ
h) e−l A/ħh ,

(B.7)

with c̃(ħ
h) an ordinary perturbative expression in ħ
h. Note, however, that the l-instanton action l A = l F0′ (t) is a nontrivial function of t, which is in contradiction with c(ħ
h) being a
t-independent integration constant. Therefore we conclude that c(ħ
h) must vanish, and so


1
(l)
(˙
∆l A F )(t; ħ
h) = −
F .
(B.8)
2πi l
When we substitute t by the classical A-period t 0 (E), we obtain the quantum prepotential
F (E; ħ
h) as defined in (38), which obeys
(l)

˙ l A F )(E; ħ
(∆
h) = S l A F l .

(B.9)

This is precisely the action of the pointed alien derivative (46) as proposed in [24], with Stokes
1
constants Sl A = − 2πi
.
45

## PDF page 46

SciPost Phys. 16, 103 (2024)
π

The Stokes phenomenon across arg(ħ
h) = 2 : Along the positive imaginary axis in the ħ
hplane we observe another Stokes phenomenon, which according to the DDP formula (31) can
be written as
S π2 t(E; ħ
h) = t(E; ħ
h) ,

(B.10)
h) = t D (E; ħ
h) + ħ
h log 1 + e−2πit(E;ħh)/ħh .
S π2 t D (E; ħ
By decomposing the automorphism in terms of pointed alien derivatives with a ‘primitive’
action A = 2πit 0 (E) which is imaginary, these two equations allow us to deduce the action of
those alien derivatives on the dual quantum period:
˙
∆l A t D (E; ħ
h) =

(−1)l+1 −2πil t(E;ħh)/ħh
ħ
he
,
l

(B.11)

where we used the fact that ˙
∆2l A t D (E; ħ
h) = 0, which follows from (B.10). We then write

˙
∆l A F ′ (t; ħ
h)
∆l A t D (E; ħ
h) ≡ ˙
∆l A t D (t(E; ħ
h); ħ
h) = ˙

t=t(E;ħ
h)

,

(B.12)

˙ l A t(E; ħ
where we used the chain rule, the definition of t D (t) and the fact that ∆
h) = 0, which
again follows from (B.10). We then substitute the independent variable E by the quantum
mirror map E(t; ħ
h) and obtain
˙
∆l A F ′ (t; ħ
h) = ħ
h

(−1)l+1 −2πil t/ħh
e
.
l

(B.13)

Then we can integrate with respect to t on both sides, and subsequently substitute t with the
classical A-period t 0 (E) to obtain


1 (−1)l+1 2 −2πil t 0 (E)/ħh
˙
∆l A F (E; ħ
h) = −
ħ
h e
.
2πi
l2

(B.14)

1
When we identify SA = − 2πi
as the Stokes constant, we find a perfect agreement with (46)
where G = A = 2πit 0 (E) and D = 0. When we express the Stokes automorphism in terms of
alien derivatives, we can now write

S π2 F (E; ħ
h) = F (E; ħ
h) + ħ
h2



∞
∑
(−1)n+1
1
−
e−2πint 0 (E)/ħh .
2
n
2πi
n=1

(B.15)

The resulting transseries structure on the right hand side matches the one described by (45)
1
for G = A = 2πit 0 (E) and D = 0 with τn = − 2πi
.

C

Median resummation

The energy transseries (151) with coefficients un,m given in table 6 for the double well and
in table 8 for the cosine potential were called ‘median transseries’ for a reason: their median
resummation corresponds to the lateral resummations of the + and − resolutions of the energy
transseries. Let us elaborate on this statement: first we introduce median resummation (see
e.g. [17, 49])
−1/2
1/2
Sθmed ≡ Sθ + ◦ Sθ
= Sθ − ◦ Sθ ,
(C.1)
where

!

Sνθ = exp ν

∑
ω∈Ωθ

46

˙A
∆
ω

.

(C.2)

## PDF page 47

SciPost Phys. 16, 103 (2024)

The idea of the median resummation operation is to take a well-defined ‘average’ of the two
lateral resummations, thus removing the rather unnatural choice to give ħ
h either a positive
or a negative imaginary part. For the energy spectrum of the double well (155), the above
definition (C.1) then tells us that




1
1
full
med med
full
S0+ Eε
t, +
;ħ
h = S0 Eε (t; ħ
h) = S0− Eε
t, −
;ħ
h ,
(C.3)
4πi
4πi
and similarly for the cosine potential




1
1
S0+ Eθfull t, +
;ħ
h = S0med Eθmed (t; ħ
h) = S0− Eθfull t, −
;ħ
h .
2πi
2πi

(C.4)

In the core of the paper we derived the median transseries by expanding the shift ∆t in terms
of even and odd powers of the instanton transmonomial and subsequently collecting those
terms into a resurgent and median part. An alternative way to obtain the median transseries
is from the median quantisation condition Dmed = 0 which interpolates between the D+ = 0
and D− = 0 conditions. Let us illustrate this for the cosine potential.28
We first change the normalisation of the exact quantisation conditions Dθ± = 0 in (160) to
D̃θ± = q

1



VA∓1 VB

q

1 + VA∓1 (1 + VB ) − 2 VA∓1 VB cos(θ ) = 0 .

(C.5)

The reason for this change of normalisaiton is that we now have that

S0 D̃θ+ = D̃θ− .

(C.6)

We can then define the median quantisation condition Dθmed = 0, which is
1

D̃θmed = S02 D̃θ+ =

 1
‾
⎷ 1 + VB
− 12
2
VA + VA
− 2 cos(θ ) = 0 .
VB

(C.7)

This is equivalent to
cos

π t 
ħ
h

1

= cos(θ ) Æ

e− 2ħh t D (t;ħh)
− ħ1h t D (t;ħ
h)

.

(C.8)

1+e

The perturbative quantisation condition, for which the entire nonperturbative right hand side
can be ignored, then yields the usual


1
t =ħ
h N+
,
(C.9)
2
and after introducing the nonperturbative Ansatz t̂ = t + ∆t we find


1
ħ
h
e− 2ħh t D (t+∆t;ħh)
∆t = arcsin cos(θ ) Æ
,
1
π
1 + e− ħh t D (t+∆t;ħh)
which is exactly (170).
28

See also e.g. [67] for the median quantisation conditions of the double and triple well.

47

(C.10)

## PDF page 48

SciPost Phys. 16, 103 (2024)

References
[1] J. Écalle, Les fonctions résurgentes, Université de Paris-Sud, Paris, France (1981).
[2] J. Zinn-Justin, Multi-instanton contributions in quantum mechanics, Nucl. Phys. B 192,
125 (1981), doi:10.1016/0550-3213(81)90197-8.
[3] J. Zinn-Justin, Multi-instanton contributions in quantum mechanics (II), Nucl. Phys. B
218, 333 (1983), doi:10.1016/0550-3213(83)90369-3.
[4] A. Voros, Spectre de l’équation de Schrödinger et méthode BKW, Université de Paris-Sud,
Paris, France (1982).
[5] A. Voros, The return of the quartic oscillator. The complex WKB method, Ann. Inst. Henri
Poincare - Phys. Theor. 39, 211 (1983).
[6] E. Delabaere, H. Dillinger and F. Pham, Exact semiclassical expansions for one-dimensional
quantum oscillators, J. Math. Phys. 38, 6126 (1997), doi:10.1063/1.532206.
[7] G. Álvarez and C. Casares, Exponentially small corrections in the asymptotic expansion of
the eigenvalues of the cubic anharmonic oscillator, J. Phys. A: Math. Gen. 33, 5171 (2000),
doi:10.1088/0305-4470/33/29/302.
[8] G. Álvarez and C. Casares, Uniform asymptotic and JWKB expansions for anharmonic oscillators, J. Phys. A: Math. Gen. 33, 2499 (2000), doi:10.1088/0305-4470/33/13/304.
[9] G. Álvarez, C. J. Howls and H. J. Silverstone, Anharmonic oscillator discontinuity formulae up to second-exponentially-small order, J. Phys. A: Math. Gen. 35, 4003 (2002),
doi:10.1088/0305-4470/35/18/302.
[10] G. Álvarez, Langer-Cherry derivation of the multi-instanton expansion for the symmetric
double well, J. Math. Phys. 45, 3095 (2004), doi:10.1063/1.1767988.
[11] C. M. Bender and T. T. Wu, Anharmonic oscillator, Phys. Rev. 184, 1231 (1969),
doi:10.1103/PhysRev.184.1231.
[12] C. M. Bender and T. T. Wu, Anharmonic oscillator II. A study of perturbation theory in large
order, Phys. Rev. D 7, 1620 (1973), doi:10.1103/PhysRevD.7.1620.
[13] E. Brézin, G. Parisi and J. Zinn-Justin, Perturbation theory at large orders for a potential
with degenerate minima, Phys. Rev. D 16, 408 (1977), doi:10.1103/PhysRevD.16.408.
[14] J. Zinn-Justin and U. D. Jentschura, Multi-instantons and exact results I: Conjectures, WKB expansions, and instanton interactions, Ann. Phys. 313, 197 (2004),
doi:10.1016/j.aop.2004.04.004.
[15] J. Zinn-Justin and U. D. Jentschura, Multi-instantons and exact results II: Specific
cases, higher-order effects, and numerical calculations, Ann. Phys. 313, 269 (2004),
doi:10.1016/j.aop.2004.04.003.
[16] H. Dillinger, E. Delabaere and F. Pham, Résurgence de Voros et périodes des courbes hyperelliptiques, Ann. Inst. Fourier 43, 163 (1993), doi:10.5802/aif.1326.
[17] E. Delabaere and F. Pham, Resurgent methods in semi-classical asymptotics, Ann. Inst.
Henri Poincare - Phys. Theor. 71, 1 (1999).

48

## PDF page 49

SciPost Phys. 16, 103 (2024)

[18] S. Codesido and M. Mariño, Holomorphic anomaly and quantum mechanics, J. Phys. A:
Math. Theor. 51, 055402 (2017), doi:10.1088/1751-8121/aa9e77.
[19] M. Bershadsky, S. Cecotti, H. Ooguri and C. Vafa, Kodaira-Spencer theory of gravity and
exact results for quantum string amplitudes, Commun. Math. Phys. 165, 311 (1994),
doi:10.1007/BF02099774.
[20] N. A. Nekrasov and S. L. Shatashvili, Quantization of integrable systems and four dimensional gauge theories, in XVIth international congress on mathematical physics, World Scientific, Singapore, ISBN 9789814304627 (2010), doi:10.1142/9789814304634_0015.
[21] R. Couso-Santamaría, J. D. Edelstein, R. Schiappa and M. Vonk, Resurgent transseries and
the holomorphic anomaly, Ann. Henri Poincaré 17, 331 (2015), doi:10.1007/s00023015-0407-z.
[22] R. Couso-Santamaría, J. D. Edelstein, R. Schiappa and M. Vonk, Resurgent transseries and
the holomorphic anomaly: Nonperturbative closed strings in local CP2 , Commun. Math.
Phys. 338, 285 (2015), doi:10.1007/s00220-015-2358-0.
[23] S. Codesido, M. Mariño and R. Schiappa, Non-perturbative quantum mechanics from
non-perturbative strings, Ann. Henri Poincaré 20, 543 (2018), doi:10.1007/s00023-0180751-x.
[24] J. Gu and M. Mariño, On the resurgent structure of quantum periods, SciPost Phys. 15,
035 (2023), doi:10.21468/SciPostPhys.15.1.035.
[25] J. Gu and M. Mariño, Exact multi-instantons in topological string theory, SciPost Phys. 15,
179 (2023), doi:10.21468/SciPostPhys.15.4.179.
[26] G. V. Dunne and M. Ünsal, Resurgence and trans-series in quantum field theory: The CPN −1
model, J. High Energy Phys. 11, 170 (2012), doi:10.1007/JHEP11(2012)170.
[27] G. V. Dunne and M. Ünsal, Uniform WKB, multi-instantons, and resurgent trans-series,
Phys. Rev. D 89, 105009 (2014), doi:10.1103/PhysRevD.89.105009.
[28] D. Dorigoni, An introduction to resurgence, trans-series and alien calculus, Ann. Phys. 409,
167914 (2019), doi:10.1016/j.aop.2019.167914.
[29] M. Mariño, Lectures on non-perturbative effects in large N gauge theories, matrix models
and strings, Fortsch. Phys. 62, 455 (2014), doi:10.1002/prop.201400005.
[30] I. Aniceto, G. Başar and R. Schiappa, A primer on resurgent transseries and their asymptotics, Phys. Rep. 809, 1 (2019), doi:10.1016/j.physrep.2019.02.003.
[31] D. Sauzin, Introduction to 1-summability
doi:10.48550/arXiv.1405.0356.

and

resurgence,

(arXiv

preprint)

[32] B. Pym, Resurgence in geometry and physics, University of Oxford, Oxford, UK (2016),
https://www.math.mcgill.ca/bpym/courses/resurgence.
[33] A. van Spaendonck and M. Vonk, Painlevé I and exact WKB: Stokes phenomenon for twoparameter transseries, J. Phys. A: Math. Theor. 55, 454003 (2022), doi:10.1088/17518121/ac9e29.
[34] J. Gu and M. Mariño, Peacock patterns and new integer invariants in topological string
theory, SciPost Phys. 12, 058 (2022), doi:10.21468/SciPostPhys.12.2.058.
49

## PDF page 50

SciPost Phys. 16, 103 (2024)

[35] J. L. Dunham, The Wentzel-Brillouin-Kramers method of solving the wave equation, Phys.
Rev. 41, 713 (1932), doi:10.1103/PhysRev.41.713.
[36] G. Basar, G. V. Dunne and M. Ünsal, Quantum geometry of resurgent
perturbative/nonperturbative relations, J. High Energy Phys. 05, 087 (2017),
doi:10.1007/JHEP05(2017)087.
[37] K. Iwaki and T. Nakanishi, Exact WKB analysis and cluster algebras, J. Phys. A: Math.
Theor. 47, 474009 (2014), doi:10.1088/1751-8113/47/47/474009.
[38] A. J. F. Siegert, On the derivation of the dispersion formula for nuclear reactions, Phys. Rev.
56, 750 (1939), doi:10.1103/PhysRev.56.750.
[39] G. Gamow, Zur Quantentheorie des Atomkernes,
doi:10.1007/BF01343196.

Z. Phys. 51,

204 (1928),

[40] U. D. Jentschura, A. Surzhykov and J. Zinn-Justin, Multi-instantons and exact results
III: Unification of even and odd anharmonic oscillators, Ann. Phys. 325, 1135 (2010),
doi:10.1016/j.aop.2010.01.002.
[41] H. J. Silverstone, JWKB connection-formula problem revisited via Borel summation, Phys.
Rev. Lett. 55, 2523 (1985), doi:10.1103/PhysRevLett.55.2523.
[42] M. Mariño, Advanced topics in quantum mechanics, Cambridge University Press, Cambridge, UK, ISBN 9781108863384 (2021), doi:10.1017/9781108863384.
[43] F. Fischbach, A. Klemm and C. Nega, WKB method and quantum periods beyond genus
one, J. Phys. A: Math. Theor. 52, 075402 (2019), doi:10.1088/1751-8121/aae8b0.
[44] K. Ito, M. Mariño and H. Shu, TBA equations and resurgent quantum mechanics, J. High
Energy Phys. 01, 228 (2019), doi:10.1007/JHEP01(2019)228.
[45] T. Sulejmanpasic and M. Ünsal, Aspects of perturbation theory in quantum mechanics: The BenderWu Mathematica® package, Comput. Phys. Commun. 228, 273 (2018),
doi:10.1016/j.cpc.2017.11.018.
[46] I. M. Gessel, Lagrange inversion,
doi:10.1016/j.jcta.2016.06.018.

J. Comb. Theory A 144,

212 (2016),

[47] N. Hoe, B. D’Etat, J. Grumberg, M. Caby, E. Leboucher and G. Coulaud, Stark effect of
hydrogenic ions, Phys. Rev. A 25, 891 (1982), doi:10.1103/PhysRevA.25.891.
[48] I. Aniceto, R. Schiappa and M. Vonk, The resurgence of instantons in string theory, Commun. Num. Theor. Phys. 6, 339 (2012), doi:10.4310/CNTP.2012.v6.n2.a3.
[49] I. Aniceto and R. Schiappa, Nonperturbative ambiguities and the reality of resurgent
transseries, Commun. Math. Phys. 335, 183 (2014), doi:10.1007/s00220-014-2165-z.
[50] M. Serone, G. Spada and G. Villadoro, The power of perturbation theory, J. High Energy
Phys. 05, 056 (2017), doi:10.1007/JHEP05(2017)056.
[51] B. Bucciotti, T. Reis and M. Serone, An anharmonic alliance: Exact WKB meets EPT, J.
High Energy Phys. 11, 124 (2023), doi:10.1007/JHEP11(2023)124.
[52] N. Sueishi, S. Kamata, T. Misumi and M. Ünsal, Exact-WKB, complete resurgent structure,
and mixed anomaly in quantum mechanics on S1 , J. High Energy Phys. 07, 096 (2021),
doi:10.1007/JHEP07(2021)096.
50

## PDF page 51

SciPost Phys. 16, 103 (2024)

[53] P. Lo Chiatto, S. Schenk and F. Yu, Quantum imprint of the anharmonic oscillator, (arXiv
preprint) doi:10.48550/arXiv.2308.01244.
[54] Z. Bajnok, J. Balog and I. Vona, The full analytic trans-series in integrable field theories,
Phys. Lett. B 844, 138075 (2023), doi:10.1016/j.physletb.2023.138075.
[55] A. Grassi, J. Gu and M. Mariño, Non-perturbative approaches to the quantum SeibergWitten curve, J. High Energy Phys. 07, 106 (2020), doi:10.1007/JHEP07(2020)106.
[56] A. Grassi, Q. Hao and A. Neitzke, Exact WKB methods in SU(2) Nf = 1, J. High Energy
Phys. 01, 046 (2022), doi:10.1007/JHEP01(2022)046.
[57] D. Gaiotto, G. W. Moore and A. Neitzke, Four-dimensional wall-crossing via threedimensional field theory, Commun. Math. Phys. 299, 163 (2010), doi:10.1007/s00220010-1071-2.
[58] D. Gaiotto, G. W. Moore and A. Neitzke, Wall-crossing, Hitchin systems, and the WKB
approximation, Adv. Math. 234, 239 (2013), doi:10.1016/j.aim.2012.09.027.
[59] M. Kontsevich and Y. Soibelman, Stability structures, motivic Donaldson-Thomas invariants and cluster transformations, (arXiv preprint) doi:10.48550/arXiv.0811.2435.
[60] C. Howls, P. Langman and A. Olde Daalhuis, On the higher-order Stokes phenomenon, Proc.
R. Soc. Lond., A: Math. Phys. Eng. Sci. 460, 2285 (2004), doi:10.1098/rspa.2004.1299.
[61] A. Gorsky and A. Milekhin, RG-Whitham dynamics and complex Hamiltonian systems,
Nucl. Phys. B 895, 33 (2015), doi:10.1016/j.nuclphysb.2015.03.028.
[62] S. Codesido Sanchez, A geometric approach to non-perturbative quantum mechanics,
PhD thesis, University of Geneva, Geneva, Switzerland (2018), doi:10.13097/archiveouverte/unige:102512.
[63] G. Basar and G. V. Dunne, Resurgence and the Nekrasov-Shatashvili limit: Connecting
weak and strong coupling in the Mathieu and Lamé systems, J. High Energy Phys. 02,
160 (2015), doi:10.1007/JHEP02(2015)160.
[64] B. Eynard, Lectures notes on
doi:10.48550/arXiv.1805.06405.

compact

Riemann

surfaces,

(arXiv

preprint)

[65] C. M. Bender and S. A. Orszag, Advanced mathematical methods for scientists and engineers I, Springer, New York, USA, ISBN 9781441931870 (1999), doi:10.1007/978-14757-3069-2.
[66] J. Gu, Relations between Stokes constants of unrefined and Nekrasov-Shatashvili topological
strings, (arXiv preprint) doi:10.48550/arXiv.2307.02079.
[67] S. Kamata, T. Misumi, N. Sueishi and M. Ünsal, Exact WKB analysis for SUSY and quantum
deformed potentials: Quantum mechanics with Grassmann fields and Wess-Zumino terms,
Phys. Rev. D 107, 045019 (2023), doi:10.1103/PhysRevD.107.045019.

51
