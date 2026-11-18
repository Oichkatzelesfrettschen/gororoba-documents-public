Source: see manifest row of the PDF
PDF sha256: d90399c19c9a29fa9becb63f0d72eea8e5b44752a04a41c545238d3fcc5ff13b
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of belin_2017_siegel_modular_forms_and_black_hole_entropy.pdf

Transcription of `belin_2017_siegel_modular_forms_and_black_hole_entropy.pdf` in this directory, 50 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-50 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ETH Library

Siegel modular forms and black
hole entropy
Journal Article
Author(s):
Belin, Alexandre; Castro, Alejandra; Gomes, João; Keller, Christoph A.
Publication date:
2017-04
Permanent link:
https://doi.org/10.3929/ethz-b-000130613
Rights / license:
Creative Commons Attribution 4.0 International
Originally published in:
Journal of High Energy Physics 2017(4), https://doi.org/10.1007/JHEP04(2017)057

This page was generated automatically upon download from the ETH Zurich Research Collection.
For more information, please consult the Terms of use.

## PDF page 2

Published for SISSA by

Springer

Received: December 20, 2016
Revised: March 13, 2017
Accepted: April 2, 2017
Published: April 11, 2017

Alexandre Belin,a Alejandra Castro,a João Gomesa,b and Christoph A. Kellerc
a

Institute for Theoretical Physics, University of Amsterdam,
Science Park 904, Postbus 94485, 1090 GL Amsterdam, The Netherlands
b
Institute for Theoretical Physics, University of Utrecht,
Leuvenlaan 3584 CE Utrecht, The Netherlands
c
Department of Mathematics, ETH Zurich,
CH-8092 Zurich, Switzerland

E-mail: a.m.f.belin@uva.nl, a.castro@uva.nl, j.m.vieiragomes@uva.nl,
christoph.keller@math.ethz.ch
Abstract: We discuss the application of Siegel Modular Forms to Black Hole entropy
counting. The role of the Igusa cusp form χ10 in the D1D5P system is well-known, and
its transformation properties are what allows precision microstate counting in this case.
We apply a similar method to extract the Fourier coefficients of other Siegel modular
and paramodular forms, and we show that they could serve as candidates for other types
of black holes. We investigate the growth of their coefficients, identifying the dominant
contributions and the leading logarithmic corrections in various regimes. We also discuss
similarities and differences to the behavior of χ10 , and possible physical interpretations of
such forms both from a microscopic and gravitational point of view.
Keywords: AdS-CFT Correspondence, Black Holes, Black Holes in String Theory
ArXiv ePrint: 1611.04588

Open Access, c
⃝ The Authors.
Article funded by SCOAP3 .

doi:10.1007/JHEP04(2017)057

JHEP04(2017)057

Siegel modular forms and black hole entropy

## PDF page 3

Contents
1 Introduction

2

1.1

The black hole side of the problem

2

1.2

The microscopic side of the problem

4
6

2.1

Basic definitions and properties of SMFs

6

2.2

SMFs for paramodular groups

8

2.3

Exponential lifts

9

2.4

Zeros and poles

10

2.5

Mapping to CFT variables

11

3 Asymptotic growth and log tails

13

3.1

Poles and growth behavior

13

3.2

New and old examples

16

3.2.1

The Igusa cusp form χ10

16

3.2.2

Exponential lifts of weak Jacobi forms

21

3.2.3

χ35

24

3.2.4

χ12

28

4 Physical interpretation of SMFs

29

4.1

CFT origin of a SMF

29

4.2

The gravitational dual of a SMF

32

5 Discussion

34

A Jacobi forms

36

A.1 Properties of Jacobi forms

36

A.2 Jacobi forms as partition functions

37

A.3 Hecke operators

39

B Logarithms in the Cardy regime: n ≫ m

40

C Black hole near-horizon geometry and attractor equations

41

–1–

JHEP04(2017)057

2 Siegel modular forms

## PDF page 4

1

Introduction

1.1

The black hole side of the problem

An important open question is to describe the entropy of a black hole, SBH , in terms of a
suitable microscopic degeneracy, d(Q), i.e.
SBH = ln d(Q) .

(1.1)

This equality can be made rather precise for a class of supersymmetric black holes.1 In
particular there is compelling evidence that there is a reasonable definition of SBH after
1

For non-extremal (finite temperature) black holes the identification in (1.1) is much more delicate in a
full quantum theory due to Hawking radiation, among other effects. For extremal but not supersymmetric
black holes, there might be an analogous definition but this will depend on the details of the solution and
the theory; it is not clear that an extremal black hole is generically well defined in the full quantum theory
or if it is an emergent IR state.

–2–

JHEP04(2017)057

In the language of statistical physics, an extremal black hole is a zero temperature system
with a huge amount of residual entropy. Understanding which features of a quantum
system can account for a large degeneracy of ground states will not only unveil interesting
properties of quantum gravity, but will also uncover novel quantum systems. Our aim
here is to present statistical systems, or more precisely counting formulas, that have the
potential to account for the entropy of an extremal black hole.
Our inspiration arises from supersymmetric black holes in string theory, with the most
famous example being the D1D5P system first considered by Strominger & Vafa [1]. This
is a situation where there has been remarkable success in accounting for the entropy of
black holes in string theory not only at leading order, but also various classes of subleading
corrections. Despite the specificity of the system, there is more than one lesson to draw
from this example. The lesson we want to emphasis here is the following: the function that
naturally captures the microstates is a Siegel Modular Form (SMF).
From a physics perspective, SMFs can be seen as a class of generating functions for
families of CFT2 with increasing central charge. Similar to a grand canonical partition
function, in addition to having a Boltzmann factor associated to, for instance, the energy,
they also have a fugacity associated to the central charge of the theories. They usually
appear as generating functions of supersymmetric (BPS) states, such as in [2–4] among
many other examples, for reasons that will become clearer later on. What is powerful
about these types of generating functions is the mathematical structure that underlies
them. The symmetry group of a SMF is not just the ordinary modular group SL(2, Z),
but the larger Siegel modular group Sp(4, Z). This is the key feature that allows us to find
that the degeneracy of states is exponentially large for a wide range of parameters even
when the temperature of the system is zero.
In the following we would like to give an overview of both sides of this problem. On the
macroscopic side, black holes do have very robust features which any microscopic proposal
should account for. This robustness in gravity is what we would like to translate into data
of the quantum system. On the microscopic side, which is the main emphasis of this work,
we want to illustrate not only how one can construct generating functions with the desired
features, but also present a procedure to extract the entropy systematically.

## PDF page 5

Here the subscript “AdS2 ” indicates that the path integral is performed on the near horizon
geometry with suitable boundary conditions that allow for single centered black holes.
The path integral is over all fields (massless and massive), and Sgrav is an effective action
containing both boundary terms in addition to all interactions of these fields. We use Q
as a shorthand to denote the electric and magnetic charges carried by the black hole.
From here the entropy of the black hole is defined as follows. First, in general Sgrav will
have a divergent piece due to infinite volume effects of AdS2 . To regulate this divergence
we introduce a cutoff L and eventually take L → ∞. One of key the observations in [5, 6] is
that from general principles of AdS2 /CFT1 , Z(Q)AdS2 can be interpreted as the partition
function of a dual quantum mechanical system sitting at the boundary of AdS2 on a
Euclidean circle of length L. This allows us to interpret
Z(Q)AdS2 = TrCFT1 (e−LH ) −−−−→ d(Q)e−E0 L ,
L→∞

(1.3)

where E0 is the ground state energy and L is the length of the boundary circle in AdS2 ;
the infrared limit is L → ∞. The macroscopic entropy is hence given by2
(
)
d
SBH = ln d(Q) = lim 1 − L
ln Z(Q)AdS2 .
(1.4)
L→∞
dL
We stress that this relation is derived from general principles of AdS2 /CFT1 , which are
carefully discussed in the above references. The strength of this method lies in the fact
that it can capture the local contributions due to the Wald entropy and non-local quantum
corrections.
We are interested in a regime where SBH is governed by the two derivative theory of
gravity for which the black hole is a smooth solution. More concretely, we want a regime
where the near horizon geometry of the black hole is weakly curved. It is well known that
the contribution to SBH from the two derivative theory is proportional to the area of the
horizon (AH ). This two derivative action also predicts the leading quantum logarithmic
corrections controlled by AH in Planck units. These are the contributions to Z(Q)AdS2
that arise from the one-loop effective action of all massless fields in the low energy theory.
This includes local and non-local contributions at the one-loop level.
2

Z(Q)AdS2 can also contain contributions from exponentially suppressed geometries which we are ignoring. Strictly speaking, we should write in (1.4) the symbol ≈ where we mean that we are only extracting
the contribution from the largest exponential contribution.

–3–

JHEP04(2017)057

local and non-local corrections are taken into account: in string theory, this includes both
α′ and gs corrections. Our focus will be in building candidates for d(Q) with the guidance
of universal features encoded in SBH . In the following we will review such features and
how they can constraint potential candidates for d(Q).
The most systematic procedure to evaluate SBH for extremal black holes is given by
the quantum entropy function, which was first introduced in [5, 6]. Comprehensive reviews
are given in [7, 8]. In a nutshell, the quantum entropy function is defined via a path integral
∫
Z(Q)AdS2 = Dφ e−Sgrav .
(1.2)

## PDF page 6

SBH =

AH
AH
+ w ln
+ ··· ,
4G
4G

for

AH
≫ 1,
4G

(1.5)

where w is some numerical coefficient that depends mostly on the number of massless modes
in the spectrum, among other features of the solution. Our emphasis will be in building new
examples d(Q) whose asymptotic growth has exactly this form. We approach the problem
from the mathematical side, and will not be able to give a description of the matching
black hole. But if a match can be found, our results give a statistical interpretation to not
just the leading area law term but also w.
1.2

The microscopic side of the problem

On the microscopic side we know that for many black holes the entropy formula SBH can
be accounted for by modular invariance. If the partition function in question is given
by some modular function or a Jacobi type form, we can use SL(2, Z) invariance to obtain its asymptotic growth. If it has non-vanishing polar part, then we will get Cardy
growth [20], i.e.
√c
d(E) ∼ e2π 6 E .
(1.6)
This is exactly the right behavior to give the Bekenstein-Hawking entropy SBH [1]. Note
however that (1.6) only holds in the regime where E ≫ c. In the language of gravity
this means that the black hole has to be very heavy. In general we would however expect
SBH to also hold for small black holes. The natural supergravity regime is c ≫ 1, but not
necessarily E ≫ c. An arbitrary Jacobi form will usually not obey (1.6) in this regime
— that is, it will not have an extended Cardy regime. If we want to find forms that can
count the entropy of black holes, we therefore need quite special forms, or, more precisely,
families of forms.
The best known example of this is the Siegel modular form χ10 , or rather its reciprocal, which is the generating function appearing in the counting of 1/4-BPS dyons in four
dimensions [2]. We interpret it as the generating function of a family of Jacobi forms. Its
symmetries are not simply the expected SL(2, Z), but are enhanced to the Siegel modular
group Sp(4, Z). Its Fourier coefficients d(E) then have an extended Cardy regime, which

–4–

JHEP04(2017)057

Logarithmic corrections to black hole entropy are very powerful: they are governed by
low energy data that probe non-trivially any theory of quantum gravity that attempts to
account for the black hole microstates. As such, they are a successful and robust test in
several situations [9–12]. For CHL models both d(Q) and its 4D(5D) supersymmetric black
hole counterpart are known explicitly, and the agreement is remarkable (see appendix C for
a quick review of this class of black holes). Logarithmic corrections have been computed
as well for several other supersymmetric configurations [13, 14] and using novel techniques
in [15–17]. There are also very interesting results for non-extremal black holes [18, 19].
Many of these examples do not have a microscopic counterpart yet, but their logarithmic
corrections will give key clues to building a microscopic description. Understanding the
statistical nature of these corrections gives a powerful insight in the quantum nature of the
black hole.
To summarise, a two derivative theory of gravity predicts that

## PDF page 7

There is an extended Cardy regime: the exponential growth in (1.6) is valid
even if E ∼ c ≫ 1. This is the natural scale in supergravity where we expect
black holes to dominate the ensemble.
We will identify several SMFs that satisfy this condition. And within this class it is
important to make two further distinctions:4
1. The Cardy regime extends also to c ≫ E ≫ 1. Moreover, the perturbative part of
the spectrum, i.e. polar states, does not exhibit Hagedorn growth. This corresponds
to a very sparse low energy spectrum, which hints that there is a supergravity regime.
2. The Cardy regime breaks down for c ≫ E ≫ 1, and a Hagedorn spectrum takes its
place. This type of behavior is more compatible with a string theory spectrum (with
no semi-classical supergravity regime).
We will elaborate more on these conditions as we go along with our analysis. Having an
extended Cardy regime should be viewed as necessary for the SMFs to have a black hole
(or gravitational) interpretation, but it might not be sufficient. Moreover, satisfying the
first condition is necessary for there to be a supergravity description of the black hole. In
our opinion, satisfying this requirement is a very compelling reason to study these cases
further. And an important part of our results is that we can meet the first condition for
examples that deviate significantly from the well known case of χ10 and cousins examples.
In some cases we can find physical interpretations of the Siegel modular forms we study.
For instance, 1/χ10 is, up to an overall factor, the generating function of the symmetric
orbifold of K3. Similar forms exist for the symmetric orbifolds of higher dimensional
Calabi-Yau manifolds. The ultimate goal would of course be to identify the CFT and
gravity (string) dual of those forms. We discuss some steps in that direction.
3

To avoid cluttering, we will refer to both Siegel modular forms and Siegel paramodular forms as SMFs.
Demanding that the Cardy regime extends for c ≫ E ≫ 1 is a much stronger condition than that
demanded in [22]. Therefore, their notion of sparseness (which allows Hagedorn growth) is much looser
than ours.
4

–5–

JHEP04(2017)057

allows it to be interpreted as describing the entropy of the D1D5P black hole in four dimensions. It is very natural to suspect that the extended Cardy regime and the enhanced
symmetry group should be related; see also [21]. This motivates the study of other SMFs.
Our general strategy is therefore to investigate the space of SMFs and their generalizations, so-called Siegel paramodular forms.3 In the D1D5P case Sp(4, Z) transformations
is one of the key symmetries that allows one to compute the dominant contribution to
the entropy and its logarithmic corrections. We apply the same strategy to more general
SMFs. Our goal is to work out the final result in terms of only a few properties of the
underlying form. In fact we find that the result depends only on the weight of the SMF,
the position of its poles, and some properties of the residue at the poles.
As we sample the space of SMFs, we will be interested in identifying SMFs that have
the correct features to account for black hole entropy. Following the criteria discussed
in [22–24], a necessary feature we will require to make this identification is:

## PDF page 8

2

Siegel modular forms

Our starting point is to consider generating functions which are of the form
∑
Φ(ρ, τ, z) =
d(m, n, l)pm q n y l ,

(2.1)

m,n,l

m

where the Fourier coefficients of ϕk,m are given by d(m, n, l). We are interested in cases
where ϕk,m (τ, z) is a Jacobi form, where k is the weight and m is the index. The definition
of Jacobi forms and some of their properties are listed in appendix A. In addition, here we
will be interested in a rather specific class of generating functions Φ: we will also consider
functions that are symmetric up to a sign under the exchange of p and q,
Φ(ρ, τ, z) = (−1)k Φ(τ, ρ, z) .

(2.3)

This transformation, combined with the transformation properties of Jacobi forms, generates the full Siegel modular group Sp(4, Z), so that Φ has the transformation properties of
a so-called Siegel modular form (SMF).
In the following we will review various properties of SMFs. In addition to its transformation properties with respect to Sp(4, Z), we will discuss its zeros and poles, introduce
the concept of exponential lift, and present generalizations for paramodular groups.
2.1

Basic definitions and properties of SMFs

In this section we will summarise the key features of SMFs we will use; for a more complete
and mathematical discussion see [25, 26], and for a review of SMFs in string theory see
e.g. [7, 27]. We start with classical holomorphic Siegel modular forms of degree g = 2 of
the full group Sp(4, Z) of weight k, whose space we denote by Mk = Mk (Γ2 ). We take5
(
)
τ z
Ω=
.
(2.4)
z ρ
The Siegel upper half plane H2 is given by
det(ℑ(Ω)) > 0 ,

Tr(ℑ(Ω)) > 0 .

(2.5)

)

(2.6)

A matrix γ ∈ Sp(4, Z) is given by
γ=
5

(

A B
C D

,

In comparison to, e.g., [7] we have z = v and τ = σ, and relative to [28], we have ω = σ.

–6–

JHEP04(2017)057

where p = e2πiρ , q = e2πiτ , and y = e2πiz ; for now the domain of (m, n, l) is unspecified
and it will be narrowed as needed. We can alternatively write
∑
Φ(ρ, τ, z) =
ϕk,m (τ, z)pm ,
(2.2)

## PDF page 9

with the 2 × 2 blocks satisfying
AB T = BAT ,

CDT = DC T ,

ADT − BC T = 12 .

(2.7)

The action of γ on Ω is given by
γ(Ω) = (AΩ + B)(CΩ + D)−1 .

(2.8)

A Siegel modular form Φ(Ω) of weight k is a holomorphic function on the Siegel upper
half plane that satisfies

Note that

(

σ1 0
0 σ1

)

∈ Sp(4, Z) ,

(2.9)

(2.10)

exchanges ρ ↔ τ ; SMF of even weight are invariant under this transformation.
By definition SMFs are holomorphic. This in particular implies that they have nonnegative weight. The space of classical Siegel modular forms generated by just five gener(2)
(2)
ators, E4 , E6 , χ10 , χ12 , χ35 , whose weights are given by their subscripts [29, 30]. Here
(2)
E4,6 are the genus 2 Eisenstein series of weight 4 and 6. The only relation between those
generators is that χ235 can be expressed as a polynomial of the other four generators. The
ring of Siegel modular forms is thus given by
(2)

(2)

(2)

(2)

Mk = C[E4 , E6 , χ10 , χ12 ] ⊕ χ35 · C[E4 , E6 , χ10 , χ12 ] .

(2.11)

We will present explicit properties of these forms in section 3.2. We say Φ is a cusp form if
(
)
τ 0
lim Φ
= 0,
(2.12)
t→∞
0 it
and denote the space of such cusp forms Sk .
For Φ ∈ Mk , we can write down a Fourier expansion in p = e2πiρ , i.e.
∑
Φ(Ω) =
ϕk,m (τ, z)pm .

(2.13)

m

The coefficients ϕk,m of this expansion are then Jacobi forms of weight k and index m (see
section 8 of [25]). To see this explicitly, note that


a0 b 0
0 1 0 0


γ=
(2.14)
 , with ad − bc = 1 ,
c 0 d 0
0001
gives the coordinate transformation
τ ↦→

aτ + b
,
cτ + d

z ↦→

z
,
cτ + d

–7–

ρ ↦→ ρ −

cz 2
.
cτ + d

(2.15)

JHEP04(2017)057

Φ((AΩ + B)(CΩ + D)−1 ) = det(CΩ + D)k Φ(Ω) .

## PDF page 10

This gives the correct transformation behavior for ϕk,m in (A.1). Moreover the transformation


1 0 0 µ
λ 1 µ 0 


γ=
(2.16)
,
 0 0 1 −λ 
0 0 0 1

the reciprocal of the Igusa cusp form χ10 . The goal of our paper is to go beyond this case.
2.2

SMFs for paramodular groups

Next we want to generalize the concept of Siegel modular forms to so-called paramodular
groups, that is certain subgroups of Sp(4, R).
The paramodular group ΓN of level N is defined as [31]



Z NZ Z
Z
 Z Z Z N −1 Z 


ΓN := 
 ∩ Sp(4, Q).
 Z NZ Z
Z 
NZ NZ NZ Z

(2.18)

We denote by Mk (ΓN ) the space of Siegel modular forms of weight k under ΓN . The
paramodular group has an extension

Γ+
N = Γ N ∪ Γ N VN ,




0N 0 0

1 
1 0 0 0
√
VN =

 .
N 0 0 0 1
0 0 N 0

(2.19)

Note that ΓN contains both (2.14) and (2.16). The Fourier-Jacobi identity of a form
Φ ∈ Mk (ΓN ) thus again leads to Jacobi forms of weight k and index m. Note however that

–8–

JHEP04(2017)057

leads to the other transformation property for Jacobi forms in (A.2). It is interesting
to note that Sp(4, Z) is generated by (2.10), (2.14), and (2.16) [26]: these are the basic
ingredients to construct a SMF.
For our purposes, holomorphic SMF do not have the right properties. In particular
their Fourier-Jacobi coefficients ϕk,m are true Jacobi forms, whose coefficients only grow
polynomially. For black hole entropies, we expect exponential (or, more precisely, Cardy
type) growth. We will therefore also consider meromorphic SMF. In that case the ϕk,m will
still have the correct Jacobi form transformation properties, but they are no longer true
Jacobi forms, but rather weak Jacobi forms, or even meromorphic Jacobi forms, in which
case the Fourier coefficients can have exponential growth (see appendix A). Meromorphic
SMF can be obtained from rational functions of classical SMF. In the physics literature
the best known example for this is
1
,
(2.17)
χ10

## PDF page 11

Φ has to be invariant under


100 0
 0 1 0 N −1 


,

0 0 1 0 
000 1


(2.20)

which means that all non-vanishing powers of p are multiples of N . It follows that we get
a family of Jacobi forms with index N m rather than just m as in the original case.
2.3

Exponential lifts

nh be a nearly holomorphic Jacobi form of weight 0 and index t with
Let ϕ ∈ J0,t
integral coefficients
∑
c(n, l)q n y l .
(2.21)
ϕ(τ, z) =
n,l

Define
A=

1 ∑
c(0, l) ,
24
l

B=

1∑
lc(0, l) ,
2
l>0

C=

1∑ 2
l c(0, l) .
4

(2.22)

l

Then the exponential lift of ϕ is the product
∏
(1 − q n y l ptm )c(nm,l) ,
Exp-Lift(ϕ)(Ω) = q A y B pC

(2.23)

n,l,m∈Z
(n,l,m)>0

where (n, l, m) > 0 means m > 0 ∨ (m = 0 ∧ n > 0) ∨ (n = m = 0 ∧ l < 0), and
it defines a meromorphic modular form of weight 12 c(0, 0) with respect to Γ+
t .
It has a character (or a multiplier system if the weight is half-integral) induced
2B . Here v is a 24th root of unity, and v = ±1.
by vη24A × vH
η
H
Note that if ϕ has a pole at τ = i∞, i.e. if it really is a nearly holomorphic form, then
the infinite product contains terms with negative n. If ϕ is a weak Jacobi form, then we
actually have C = tA.
There is an analogue statement for forms of half-integer weights. We can use the Hecke
operator U2 (see appendix A.3) which maps any ϕ(τ, z) ∈ J0,d/2 to ϕ(τ, 2z) ∈ J0,2d . (The
converse is obviously not true.) For half-integer t, we can then apply the above theorem to
ϕ|U2 to get a Siegel paramodular form in M0 (Γ+
4t ), possibly with a multiplier system. Note
that half-integer index weak Jacobi forms have automatically c(0, 0) = 0, so that their lifts
have weight 0.

–9–

JHEP04(2017)057

Through the Fourier-Jacobi expansion, we know how to obtain Jacobi forms from SMF.
Let us now discuss the converse question: given some type of Jacobi form, can we lift it
to a SMF? It turns out that this is possible for certain forms, and that there are in fact
two types of lifts: additive and exponential lifts. Our focus will be mostly on the later; the
additive lift will play a minor role around (3.14).
The exponential lift is described in Theorem 2.1 of [32], which first portion states:

## PDF page 12

The exponential lift can be naturally split into two factors, namely
Exp-Lift(ϕ)(Ω) = q A y B pC

∏

(1 − q n y l )c(0,l) ×

(n,l)>0

∏

n,l,m∈Z
m>0

(1 − q n y l ptm )c(nm,l) .

(2.24)

Here (n, l) > 0 means n > 0 ∨ (n = 0 ∧ l < 0). The second factor can be naturally written
in terms of Hecke operators T− (r), namely as
exp −

∑
r≥1



r−1 ptr ϕ|T− (r) =

1
.
Φϕ

(2.25)

If ϕ is some elliptic genus or partition function χ of a CFT, then Φϕ is the generating
function for the partition functions of the symmetric orbifolds of that theory,
Φχ =

∞
∑

ptr χ(τ, z; Symr (M )) .

(2.26)

r=0

A famous example of this is the Igusa cusp form χ10 , which is the exponential lift of the
weak Jacobi form 2φ0,1 . Another example is χ35 , which is the exponential lift of a nearly
holomorphic Jacobi form of weight 0 and index 1, namely φ0,1 |T2 − 2φ0,1 . We will return
to this in sections 3.2 and 4.1.
2.4

Zeros and poles

Let us now discuss the zeros and poles of meromorphic SMF that can be cast as exponential
lifts, which is the second portion in Theorem 2.1 of [32]. These zeros and poles are located
on the divisors of the SMF, and for a SMF that has a product expansion (such as (2.23)) it
is rather simple to identify them: choosing τ, z, ρ such that q n y l ptm = 1 in one of the factors
will make that factor vanish, so that the product either vanishes or diverges. Because of
+
the invariance under Γ+
t , divisors will always come as orbits of Γt .
To describe the divisors of lifted SMF, it is useful to introduce Humbert surfaces:
this is how we will package the orbits of Γ+
t . We are following section 1.3 of [32] here.
b
Define ℓ = (e, a, − 2t
, c, f ) with e, a, b, c, f ∈ Z and gcd(e, a, b, c, f ) = 1. We define its
discriminant as
D(ℓ) = 2t(ℓ, ℓ) = b2 − 4tef − 4tac .
(2.27)
It turns out that there is a natural action of Γ+
t on ℓ that leaves D(ℓ) invariant. ℓ then
defines a divisor in H2 via the quadratic equation
tf (z 2 − τ ρ) + tcρ + bz + aτ + e = 0 .

(2.28)

The crucial observation in [32] is that all zeros and poles of SMF that are exponential lifts
are given by Humbert surfaces HD (b). These divisors can always be written as
HD (b) = πt+ ({Z ∈ H2 : aτ + bz + tρ = 0}) ,

– 10 –

(2.29)

JHEP04(2017)057



## PDF page 13

2
where πt+ is the set of images of Γ+
t . The discriminant D is given by D = b − 4ta and b
mod 2t. This determines its position, but each divisor has its on multiplicity (or degree).
In general, the divisors of the exponential lift (2.23) are given by the Humbert surfaces
∑
mD,b HD (b) ,
(2.30)
D,b

and the multiplicities mD,b are given by
mD,b =

c(n2 a, nb) ,

(2.31)

n>0

where c(n, l) are the Fourier coefficients of the underlying form ϕ. From this we see that the
Humbert surface of maximal discriminant D comes from the term with maximal polarity
nh .
of ϕ ∈ J0,t
In the following section an important case will be the Humbert surface H1 (1) for
exponential lifts of weak Jacobi forms. Note that due to the transformation


1 t 0 0
0 1 0 0


γ=
(2.32)
 ∈ Γ+
t ,
0 0 1 0
0 0 −t 1

which maps z ↦→ z + tρ, the divisor z = 0 is in H1 (1). The behavior near z = 0 will be
vital as we extract asymptotic formulas. The crucial identity here is the ‘Witten index’
weak ,
identity, i.e. for ϕ ∈ J0,t
∑
c(n, l) = 0 , ∀ n > 0 .
l

The leading zero or pole near z = 0, up to numerical coefficients, is then
∏
∏
∏
q A ptA
(1 − ptm )24A
(1 − q n )24A (1 − y l )c(0,l)
m>0

n>0

∼z

m1,1 A tA

=z

m1,1

q p

η(τ )

∏

m>0
24A

(1 − p

η(tρ)

l<0

tm 24A

)

∏

(1 − q n )24A

n>0

24A

(2.33)

with
m1,1 =

∑

c(0, l) .

(2.34)

l<0

Note that the zero (or pole) has indeed multiplicity m1,1 .
2.5

Mapping to CFT variables

To end this section, we will set our conventions on how some basic data of a SMF is mapped
to CFT jargon. In particular, we will translate quantities such as (m, n, l) to the quantum
numbers, anomalies and Casimir energies.

– 11 –

JHEP04(2017)057

∑

## PDF page 14

Very broadly speaking, from its definition, a SMF is intimately related to Jacobi forms
via (2.13). And a Jacobi form, as reviewed in appendix A.2, can be thought as a generalized
partition function of a system whose algebra contains at least one copy of Virasoro and a
U(1) Kac-Moody current. For instance, ϕk,m can be interpreted as the Elliptic genus of a
SCFT or the partition function of a chiral theory. Hence, we can interpret ϕk,m as
TrH (q L0 −c/24 y J0 ) ,

or

(
)
TrRR (−1)F (−1)F̄ q L0 −c/24 q̄ L̄0 −c/24 y J0 ,

(2.35)

E = n,

J =l.

(2.36)

The index m of ϕ is the level of the Kac-Moody algebra, i.e. the anomaly in the current
OPE. An ‘effective’ central charge can be inferred from the most polar term in ϕk,m . We
recall that polar terms are those whose discriminant is negative: ∆ = 4nm − l2 < 0. In
this sense the maximal polarity is the analogous of the Casimir energy of the ground state.
If we denote the most polar term as (n0 , l0 ), then we identify schematically the an effective
central charge as6
√
ceff
l02 − 4n0 m =
.
(2.37)
24

For weak Jacobi forms l0 is bounded by the index m, while for nearly holomorphic forms
(n0 , l0 ), are arbitrary. In either case, a large ‘c’ limit is closely related to a large m
limit, and for this reason it is useful to think of m as controlling the central charge. For
supersymmetric examples this can be made more sharp since c = 6m, but this relation is
not generic.
SMFs that have the most natural interpretation as describing a family of CFTs are
those that can be cast as an exponential lift. Calling ϕk,t in (2.23) the seed, then the
resulting SMF is the generating function of symmetric products of ϕk,t . The coefficient of
q m , that is the weak Jacobi form of index m, then corresponds to the symmetric orbifold
or order r := m/t. If we denote by D the discriminant of the most polar term in the seed,
then this r-th symmetric orbifold has a polar term of maximal polarity
Dr2 = D

m2
= l02 − 4n0 m ,
t2

(2.38)

where on the right-hand side l0 and n0 are the data of the most polar state in the r-th
symmetric orbifold.
6

Strictly speaking, here we use “effective central charge” to denote the quantity that controls the asymptotic growth of states at very high energies, i.e. the Cardy regime. Its precise relation to the central charge
can be derived depending on the physical origin of ϕ, but for now (2.37) is enough.

– 12 –

JHEP04(2017)057

where L0 and J0 are the zero modes of the Virasoro algebra and Kac-Moody current
respectively. If we denote E and J the eigenvalues of L0 and J0 , the relation to the
notation used above is straight forward:

## PDF page 15

3

Asymptotic growth and log tails

In this section we will obtain the asymptotic behavior of the Fourier coefficients of a class
of meromorphic SMF. Our analysis follows very closely the results in [4, 7, 33], which
is specific to the reciprocal of the Igusa cusp form χ10 and its cousin functions for CHL
models. As we will show, the key is to exploit the zeros of Φ(Ω): this will allow us to
identify generating functions that have the desired physical properties and, moreover, we
can extract the leading and subleading behavior easily.
Poles and growth behavior

To start, lets estimate the leading growth behavior. For reasons that will become clear
shortly, it will be useful to introduce some notation. In particular we will introduce so(2, 1)
vectors, whose inner product is given by
X · Y = (X 1 , X 2 , X 3 ) · (Y 1 , Y 2 , Y 3 ) = X 1 Y 2 + X 2 Y 1 − 2X 3 Y 3 .
Using this notation, the Fourier coefficients of the reciprocal of Φ(Ω) are given by
∫
1
d(Q) = dτ dρdz e−2πiQ·Y
,
Φ(Ω)
C

(3.1)

(3.2)

where, relative to (2.1), d(Q) ≡ d(m, n, l) and
Q := (m, n, l/2) ,

Y := (τ, ρ, −z) .

(3.3)

The integration contour C in (3.2) is chosen according to the domain in which we want
to compute the degeneracy, though many asymptotic properties are not sensitive to the
details of this choice. We will elaborate more on this as we examine our examples.
Our goal is to obtain an asymptotic formula for d(Q), i.e. we want to estimate the
Fourier coefficients in a regime where all the entries in Q are large, and Q2 is positive. We
schematically write this scaling regime as
Q2 ≫ 1 .

(3.4)

Typically these states correspond to black hole states. The gravitational counterpart
of (3.4) is roughly AH /4G ≫ 1, i.e. a smooth and weakly curved black hole solution.
More importantly, we are looking for examples where the growth is exponentially large
in this regime. To achieve this, we will consider functions Φ(Ω) that obey the following
properties
1. 1/Φ(Ω) is a meromorphic SMF with poles in the Siegel upper half plane. The simplest
way to build such a function is by taking the reciprocal of a cusp SMF.
2. Φ(Ω) can be cast as an exponential lift as defined in section 2.3.
Let’s briefly justify our choices. If 1/Φ(Ω) is meromorphic it is rather easy to perform at
least one of the integrals in (3.2): we can simply do a residue integral around the appropriate

– 13 –

JHEP04(2017)057

3.1

## PDF page 16

Here the Lagrange multiplier λ constrains Y to be on the divisor (2.28). Adapting the
notation used in section 2.4 to the so(2, 1) notation used here, we have
)
(
b
.
(3.6)
β := t c, a,
2
Extremizing f (λ) gives
λ = ±i

√

2Q2
,
D

1
Ymax =
tf

where
1
β + 2tf e = − D ,
2

(

Q
+β
λ

)

,

(3.7)

)
(
l2
,
Q = 2 mn −
4

(3.8)

2

2

and D is given by (2.27). After neglecting a phase,9 we then get that at the extremum (3.7)
the leading behavior of the Fourier coefficient is
2

d(Q) ∼ e

Q
−i2π tf
λ

=e

π
− tf

√

2DQ2

,

7

(3.9)

The meromorphicity of 1/Φ(Ω) highlights that d(Q) depends on the contour: as C crosses a pole we
get a jump in d(Q). This is the well-known phenomenon of wall crossing, and while very interesting, we
will not explore this subject. We will comment on this in section 5.
8
Checking the validity of this assumption relies on the value of Y near the saddle point. For our
discussion, we see from (3.7) that as Q2 ≫ 1 we roughly have Y ∼ O(1) and hence the residue of Φ(Ω) near
this most dominant pole is of order one. However, this is a very heuristic argument that we will revisit as
we move along.
9
Replacing (3.7) gives
2

e

Q +2πi Q·β
−i2π tf
λ
tf

.

Since Q · β/(tf ) is a rational number, its potential contribution is at most a phase.

– 14 –

JHEP04(2017)057

contour.7 This simplifies greatly the integrand, since to extract d(Q) in principle we only
need the residues of 1/Φ(Ω). Our second choice is more restrictive, but rather powerful.
If Φ(Ω) has a product expansion it is possible to read off the residues at a given pole, and
moreover to locate of all divisors in Φ(Ω). This is crucial since we really don’t want to
keep track of every detail in d(Q): we want a practical algorithm to estimate the largest
contribution in (3.2) for large values of Q.
With these ingredients in hand we can make a first estimate of the behavior of d(Q).
Since we are considering exponentials lifts, the poles of 1/Φ(Ω) are given by the Humbert
surfaces (2.28), which is nothing more complicated than a quadratic equation for Y . To
identify the most dominant pole, we will need to add one assumption: for Q2 ≫ 1 we can
assume that the integrand in (3.2) is dominated by the explicit exponential factor. This in
particular means that the residue of Φ(Ω) does not compete with e−2πiQ·Y ;8 of course this
assumption has to be checked (and refined) for each example, but for now we will take it
as given. Hence, in order to find the most dominant pole in the regime (3.4) we need to
extremize
(
)
1
2
f (λ) = Q · Y + λ − t f Y + β · Y + e .
(3.5)
2

## PDF page 17

where we selected the minus sign in (3.7) since D > 0. The dominant contribution is thus
for f = −1 and D of maximal polarity, which leads to
√
√
2
2
d(Q) ∼ eπ 2DQ /t = eπ (4mn−l )D/t .
(3.10)
At this stage it is useful to compare this result with the ordinary Cardy formula.
Comparing (3.10) with (B.6) we have

In many of the cases we will discuss in section 3.2 we will be allowed to set e = 0, b = 1
and hence D = 1: this corresponds to the Humbert surface H1 (1).
It is important to emphasize that in (3.4) we don’t need for all entries to be equally
large: there can be relative scalings among each component. This leads to a powerful
conclusion: assuming that 1/Φ(Ω) has a pole, we can obtain an asymptotic growth as
in (3.10) for a wide range of energies relative to the central charge. More concretely, in
terms of the components of Q, we have exponential growth in three general cases:
I. n ≫ 1, m ∼ 1 : this is the usual Cardy regime, where the energy of the state is much
bigger than the central charge of the system, which is also proportional to the index.
Recall that the index controls the maximal polarity of the Jacobi form which controls
the validity of the Cardy regime.
II. n ∼ m ≫ 1 : here energies are comparable to the central charge. Gravitational systems
for which this scaling is relevant are, for example, BPS black holes in N = 4, 8
in four dimensional supergravity (see appendix C). The BTZ black hole in three
dimensions [34] falls as well in this category.
III. m ≫ n ≫ 1 : we can naively access the opposite scaling as I due to the exchange
symmetry among ρ and τ of SMFs. Note however that this regime is not the exact
opposite of regime I, since we do not hold n fixed as in the Cardy regime. The access
to this regime does depend on how freely we can choose the contour C as we will
see in the examples. A gravitational system for which this regime is relevant is the
5D BMPV black hole: in the type IIB frame we have m ∼ Q1 Q5 and n ∼ P ; see
e.g. [11, 35, 36].

– 15 –

JHEP04(2017)057

D
1
= (l02 − 4n0 m) 2 .
(3.11)
t2
m
This is in agreement with our results in appendix B. Recall that we are considering an
nh , and hence we should compare with the r-th symmetric product
exponential lift of ϕ ∈ J0,t
of ϕ. The relation in (3.11) shows that the Humbert surface that dominates the residue
is indeed correctly related to the term with maximal polarity in a Jacobi from of degree
m = tr.
As in [7], we can use translation symmetry to restrict further the remaining integers
in (3.6). Taking ρ → ρ + 1/t allows us to set a = 0, translations τ → τ + 1 can be used
to set c = 0. Then shifts z → z + 1 lower b → b − 2t, which is compatible with b mod 2t.
And e is finally fixed by D and b via (3.8). This allows us to identify the most dominant
pole as
t(τ ρ − z 2 ) + bz + e = 0 .
(3.12)

## PDF page 18

For sake of simplicity, in the above classification we have omitted the scaling properties of
l, but it can easily be incorporated. And of course more variants could be included, but
these three regimes will suffice to illustrate the properties of d(Q).
Even though all three cases listed above have the same leading behavior, given
by (3.10), the subleading corrections are sensitive to the details of the relative scalings
of the components in Q. This is extremely important if we wanted to identify d(Q) with
the entropy of a gravitational system: our aim is to not just capture the leading area contributions, but account for subleading corrections. In the following we will show how to
extract this information and subtleties that might arise.
New and old examples

In this section we will list a few examples of meromorphic SMF and properties of its Fourier
coefficients. The first two examples mostly involve SMF built out of exponential lifts of
weak Jacobi forms. The later examples are more exotic, and involve the less explored
behavior of χ35 and χ12 .
3.2.1

The Igusa cusp form χ10

The most successful example of this program is given by the counting formula that captures
the degeneracy 1/4 BPS black holes in four dimensional N = 4 supergravity. In this case,
the object of interest is10
∫
1
l+1
dτ dρdz e−2πiQ·Y
d(Q) = (−1)
.
(3.13)
χ10 (Ω)
C
where χ10 is the Igusa cusp form. In the following we will summarise the procedure done
in [4, 7, 33] to extract the asymptotic growth; this will serve as a guiding principle for the
later cases. In the next example we will derive more general expressions and capture more
broadly the data that governs the logarithmic corrections from the statistical point of view.
To start, it is useful to highlight some basic properties of χ10 . As an additive lift we
can write it as
∞
∑
(φ10,1 |Vm )(τ, z)pm ,
(3.14)
χ10 (Ω) =
m=1

where

φ10,1 = η 18 (τ )θ12 (τ, z) ,

(3.15)

and Vm is the Hecke operator in (A.15). For now it is not important the details behind
Vm ; in what follows, the important observation is that φ10,1 is the seed. The miracle of χ10
is that it can also be written as an exponential lift, which reads
χ10 (Ω) = Exp-Lift(2φ0,1 )
∏
2
(1 − q s y t pr )2C0 (4rs−t ) .
= qyp

(3.16)

(r,s,t)>0

10

Note that the black hole degeneracy d(Q) has a factor of (−1)l+1 relative to the definition (3.2). This
factor arises from a careful treatment of the helicity quantum numbers when we go from five down to four
dimensions [37, 38].

– 16 –

JHEP04(2017)057

3.2

## PDF page 19

Here C0 are the Fourier coefficients of φ0,1 given in (A.6). What is physically interesting
of this example is its intimate relation to the elliptic genera of K3. More concretely
1
φ0,1 = χ(τ, z; K3) ,
2

(3.17)

and hence another way to write the Igusa form is as
1
Ẑ(Ω)
=
,
χ10 (Ω)
φ10,1 (τ, z)

(3.18)

Ẑ(Ω) =

∞
∑

χ(τ, z; Symm+1 (K3))pm

m=−1

= p−1

2

∏

r>0,s≥0,t

(1 − q s y t pr )−2C0 (4rs−t ) .

(3.19)

Equation (3.18) has an interesting physics interpretation. As whole, (3.18) counts four
dimensional 1/4-BPS dyons. The factor of Ẑ(Ω), while it is not a SMF, it is the counting
formula for the Strominger-Vafa 5D black hole. The factor of φ10,1 (τ, z) arises from placing
the 5D black hole on Taub-Nut: it counts bound states of the Kaluza-Klein monopole and
the center of mass motion of the black hole. This is know as the 4D-5D lift [3, 4, 39]. It is
both remarkable and powerful that χ10 has the capacity to capture the degeneracy of BPS
4D and 5D configurations.
We now discuss the asymptotic behavior of the Fourier coefficients (3.13). As we
outlined above, we will first perform a residue integral around the most dominant pole.
The positions of the zeros of χ10 are given by H1 (1), and from (3.12) we deduce that the
most dominant pole in the regime (3.4) is given by
τ ρ − z2 + z = 0 .

(3.20)

As in [7], it is convenient to map this pole to z = 0 for the simple reason that the residue
there takes the form given in (2.33). The Sp(4, Z) element that maps does the trick is


(3.21)

Ω̂ := γ(Ω) = (AΩ + B)(CΩ + D)−1 ,

(3.22)

γ=

(

A B
C D

)

which acts as


0 1 −1 0
 0 1 0 0


=
,
 1 0 0 0
−1 0 0 1

and the individual components transform as
τ=

1
,
2ẑ − ρ̂ − τ̂

ρ=

ẑ 2 − ρ̂τ̂
,
2ẑ − ρ̂ − τ̂

– 17 –

z=

ẑ − ρ̂
.
2ẑ − ρ̂ − τ̂

(3.23)

JHEP04(2017)057

where

## PDF page 20

Under such a transformation (3.20) goes to ẑ = 0 and the integrand (3.13) will change as
∫
1
d(Q) = (−1)l+1 dτ dρdz e−2πiQ·Y
χ
10 (Ω)
∫C
1
= (−1)l+1 dτ̂ dρ̂dẑ e−2πiQ·Y det(CΩ + D)3+k
.
(3.24)
χ10 (Ω̂)
C

Following (2.33), near ẑ = 0 we have
1
1
=
η(τ̂ )−24A η(ρ̂)−24A + · · · ,
χ10 (Ω)
(2πiẑ)2
where
A=

(3.26)

k+2
1 ∑
c(0, l) =
.
24
12

(3.27)

l

The first equality expresses A in terms of φ0,1 (which is the seed in the exponential
lift (3.16)); the second equality highlights the fact that the weight of the SMF fixes the
weight of the residue, that is the power of the η functions. Note that here m1,1 = 2 which
follows from (2.34) and (A.6).
Performing a contour integral around a contour C that encloses (3.20) gives
∫
(−1)l
− 2πi (mτ̂ ρ̂−n+lρ̂)
d(Q) ≈
dτ̂ dρ̂ e ρ̂+τ̂
η(τ̂ )−24A η(ρ̂)−24A gres (τ̂ , ρ̂) ,
(3.28)
2
4π
with
(
))
d ( −2πiQ·Y
.
e
det(CΩ + D)3+k
gres (τ̂ , ρ̂) = 2πi e2πiQ·Y
dẑ
ẑ=0

(3.29)

The derivative comes from the fact that we have a quadratic pole. Here the symbol “≈”
reflects upon the fact that we are only considering the pole (3.20); corrections to (3.28)
are exponential suppressed for large Q and come from considering other integer values of
f in H1 (1). These corrections are tractable, hence a generalization to an exact formula for
d(Q) is rather feasible.
It is convenient to redefine variables in (3.28): we introduce complex variables τ1,2
which are defined as
ρ̂ =: τ1 + iτ2 , τ̂ =: −τ1 + iτ2 ,
(3.30)
and we have
∫
π
1
(m(τ12 +τ22 )+n−lτ1 )
d(Q) ≈ 2 dτ1 dτ2 e τ2
η(−τ1 + iτ2 )−24A η(τ1 + iτ2 )−24A gres (τ1 , τ2 ) , (3.31)
4π
and (3.29) becomes
gres (τ1 , τ2 ) = −4πi(−2iτ2 )

−(k+4)

(

π
(3 + k) + (n − lτ1 + m(τ12 + τ22 ))
τ2

– 18 –

)

.

(3.32)

JHEP04(2017)057

We have used (2.9), and for χ10 we have k = 10. The Jacobian of the transformation (3.21) is
det(CΩ + D)3 = (2ẑ − ρ̂ − τ̂ )−3 .
(3.25)

## PDF page 21

Equation (3.31) gives a systematic way on how to compare the statistical degeneracy to
a dual holographic system. In particular to extract the leading contribution and its logarithmic correction, the next and final step is to estimate this integral by a saddle point
approximation.
As Q2 ≫ 1, the position of the saddle point is governed by the explicit exponential
term in (3.31), and its location is given by
τ1∗ =

l
,
2m

τ2∗ =

d(Q) ≈ e

√
π 2Q2

η(−τ1∗ + iτ2∗ )−24A η(τ1∗ + iτ2∗ )−24A gres (τ1∗ , τ2∗ )

(3.33)

(
)
(τ2∗ )2
2√
,
2Q2

(3.34)

where the last term in parenthesis is the contribution of the measure in (3.31). From (3.33)
one can see that for Q2 ≫ 1 the most dominant term is the explicit exponential factor
in (3.31), and it justifies our initial assumption in (3.5). The η-functions, while they can
contribute with exponential contributions if its entries are small, give subleading corrections
in this large charge limit. This class of corrections to d(Q) are as well interesting (they
are usually interpreted as higher derivative corrections), but not our present focus; see,
e.g., [7, 40] and references within.
Note that the leading exponential in (3.34) is in agreement with (3.10): for χ10 we have
D = 1 and t = 1. This is the universal correction that in the gravitational language would
be the “area law” and in the CFT it mimics the Cardy growth of states. However, we want
to make a contrast among these regimes and how subleading corrections are sensitive to
them. In the following we will record the leading and subleading logarithmic correction in
physically different scaling regimes for which (3.34) holds.
I. n ≫ 1, m ∼ O(1) : without loss of generality, it is convenient to introduce a scale Λ ≫ 1
and take
n ∼ Λ2 , m ∼ Λ0 , l ∼ Λ .
(3.35)
In this regime we have
τ1∗ ∼ Λ ,

τ2∗ ∼ Λ ,

Q2 ∼ Λ2 ,

and the asymptotic growth behaves as
√
ln d(Q) ≈ π 2Q2 − 12 ln τ2∗ + · · ·
√
≈ π 2Q2 − 12 ln Λ + · · · ,

(3.36)

(3.37)

where we included the logarithmic correction and used that k = 10. Note that the
logarithm in this scaling regime is independent of the eta-functions: only gres and
the measure in (3.34) contribute. This is in complete agreement with the expected
correction in the Cardy regime in (B.6). From the standpoint the Fourier decomposition in (3.14) of χ10 , this correction is rather predictable since it is the universal

– 19 –

JHEP04(2017)057

and the leading contribution to (3.31) becomes

1 √ 2
2Q ,
2m

## PDF page 22

contribution that is controlled by modular properties of φ10,1 . From the standpoint
of the exponential lift in (3.16), this data is more intricate: k is controlled by the low
lying coefficients in φ0,1 .
II. n ∼ m ≫ 1 : here we set

n ∼ Λ,

m ∼ Λ,

l 2 ∼ Λ2 ,

(3.38)

τ1∗ ∼ Λ0 ,

τ2∗ ∼ Λ0 ,

Q2 ∼ Λ2 .

(3.39)

which gives

This reproduces the results in [7, 9]. Note that the logarithmic correction will vanish
every time we have a pole of order 2 and τ1,2 do not scale with Λ. In general, this
will be the easiest regime to capture since the moduli are of order one.
III. m ≫ n ≫ 1 : if now instead we take the m to be arbitrarily large, we have
m ∼ Λ2 ,

n ∼ Λ,

l 2 ∼ Λ3 .

(3.41)

In this regime we have
τ1∗ ∼ Λ−1/2 ,

τ2∗ ∼ Λ−1/2 ,

Q2 ∼ Λ3 .

(3.42)

The degeneracy is
√

2Q2 + 12 ln τ2∗ + · · ·
√
≈ π 2Q2 − 12 ln Λ1/2 + · · · .

d(Q) ≈ π

(3.43)

In this regime all factors in (3.34) have a non-trivial contribution to the logarithm.
Even though d(Q) here needs to be modified to account for the statistical entropy of
5D black holes, this expression reproduces the logarithmic correction of the BMPV
solution obtained in [11].11 It is also a coincidence, that (3.40) and (3.43) give the
same correction; in our following examples we will generalize this result and the
differences among regimes will be explicit.
The devil is in the details. Each of these scalings regimes has a universal leading contribution, which is identified with the area law contribution in gravity. The logarithmic
corrections are also crucial for this identification: a two derivative theory of gravity makes
a prediction on both the exponential piece (which measures the size of the black hole) and
the logarithmic piece (which captures the perturbative fluctuations of the theory). As we
mentioned before, for χ10 and CHL models, the agreement is a remarkable test of quantum
gravity.
And in addition, in [11] the scaling differed slightly from (3.41) by including l2 ∼ Λ3+α . This new
parameter α is sensitive to the 4D-5D lift and hence it affects the coefficient in front of the log.
11

– 20 –

JHEP04(2017)057

Since the moduli τ1,2 do not scale, the only logarithmic correction arises from the
explicit dependence of Q in (3.34), i.e. from gres and the measure factor. The degeneracy is
√
√
ln d(Q) ≈ π 2Q2 + (1 − 1) ln Q + · · ·
√
(3.40)
≈ π 2Q2 + · · · .

## PDF page 23

3.2.2

Exponential lifts of weak Jacobi forms

χ10 is just one of a larger class of SMF that serves our purpose, i.e. the purpose of building
counting formulas with “black hole” features. In this subsection we will identify such SMFs
and quantify the behavior of their Fourier coefficients. These examples involve exponential
lifts of weak Jacobi forms whose modular group is Γ+
t .
Our starting point is to consider
∫
1
d(Q) = dτ dρdz e−2πiQ·Y
,
(3.44)
Φk (Ω)
C

t(ρτ − z 2 ) + z = 0 ,

(3.45)

As we did for χ10 it is useful to map this pole to ẑ = 0, where we have a simple expression
for the residue. A Γ+
t transformation that accomplishes this is


√
0
t − √1t 0
(
) 

 0 √1t 0 0 
A B

,
γ=
= 1
(3.46)

√
C D
0
0
0
 √t

− t 0 0 √1t
which acts in the individual components as
τ=

1
,
2tẑ − t2 ρ̂ − τ̂

ρ=

ẑ 2 − ρ̂τ̂
,
2tẑ − t2 ρ̂ − τ̂

z=

ẑ − tρ̂
.
2tẑ − t2 ρ̂ − τ̂

(3.47)

The contour integral around this pole will generically give (up to numerical factors)
∫
d(Q) ≈ dτ̂ dρ̂ e−2πiQ·Y (ẑ=0) η(τ̂ )−24A η(ρ̂)−24A gres (τ̂ , ρ̂) ,
(3.48)

where we have used that Φk around ẑ = 0 takes the general form (2.33). The difference
relative to (3.28) is that now we have
∑
k + m1,1
1 ∑
A=
c(0, n) ,
(3.49)
c(0, l) =
,
m1,1 =
24
12
n>0

l

which generalizes the order of the pole;12 recall that here c(n, l) are the Fourier coefficients

of ϕ in the exponential lift. And the remaining piece in (3.48) is now given by
(
))
m1,1 −1 (
2πi
2πiQ·Y d
−2πiQ·Y
3+k
e
. (3.50)
gres (τ̂ , ρ̂) =
e
det(CΩ + D)
(m1,1 − 1)!
dẑ m1,1 −1
ẑ=0
12

We are assuming that m1,1 > 0; otherwise we would have a zero instead of a pole. This is however
easily fix by taking in (3.44) Φk instead of 1/Φk .

– 21 –

JHEP04(2017)057

weak . The zeros of Φ are given by (2.29), and we
where Φk is of the form (2.23) and ϕ ∈ J0,t
k
are assuming they are non-trivial. The procedure to obtain d(Q) follows very closely those
steps for χ10 : we first do a contour integral over the most dominant pole which brings the
integral to the form similar to (3.28) and then a saddle point approximation as in (3.34).
As we argued around (3.9)–(3.12), the most dominant pole will be that with maximal
polarity D. And the simplest case is when the dominance is given by D = 1 and b = 1,
i.e. the Humbert surface is H1 (1), and it will be the focus of the remainder of this section.
The most dominant pole is then described by the curve

## PDF page 24

Scaling regime

∗
τ1,2

Q2

ln Λ

I. n ≫ 1

Λ

Λ2

−(k + 2)

II. n ∼ m ≫ 1

Λ0

Λ2

m1,1 − 2

III. m ≫ n ≫ 1

Λ−1/2

Λ3

m1,1 − 3 − k2

n ∼ Λ2 , m ∼ O(1), l ∼ Λ
n ∼ Λ, m ∼ Λ, l ∼ Λ
n ∼ Λ, m ∼ Λ2 , l ∼ Λ3/2

The rest of the steps from here follow very closely as those in section 3.2.1. Changing
variables to ρ̂ = t−1 (τ1 + iτ2 ) and τ̂ = t(−τ1 + iτ2 ) gives an integral similar to (3.31), and
after making a saddle point approximation we obtain
(
)
√
π
(τ2∗ )2
2
√
,
(3.51)
d(Q) ≈ e t 2Q η(−τ1∗ + iτ2∗ )−24A η(τ1∗ + iτ2∗ )−24A gres (τ1∗ , τ2∗ )
π 2Q2
where
τ1∗ =

l
,
2m

τ2∗ =

1 √ 2
2Q .
2m

(3.52)

As expected again, the leading exponential contribution in this case agrees with (3.10).
With these expressions we can easily extract the logarithmic corrections to ln d(Q).
The results for the three cases of interest are in table 1. The two pieces of data that can
affect the logarithmic correction is either the weight of Φk , or the order of the pole. What
is interesting about this result is how this data is controlled by the seed in the exponential
lift: being capable of capturing these logarithmic corrections in a gravitational setup probes
non-trivially ϕ. As we mentioned in section 2.3, ϕ would be the starting point to give a
physical interpretation of Φk as a generating function for a family of CFTs.
It might seem like restricting our attention to SMFs that have H1 (1) as the most
dominant divisor is too restrictive. There are however examples of such forms and in
particular for which the results in table 1 applies. These examples were first presented
in [28], and the weak Jacobi forms used in the exponential lifts are related to Elliptic
Genera of Calabi-Yau manifolds. The idea is to take exponential lifts of weak Jacobi forms
whose most polar terms have polarity −1 rather than −t2 . Geometrically this means that
some of the Hodge numbers conspire to cancel the leading polar terms. To describe these
examples it is useful to introduce the quantity
∑
χp (M ) =
(−1)j hj,p (M ) ,
(3.53)
j

where hj,p are the Hodge numbers of CYd . Note that we are abusing a bit notation: we
hope it is clear when χp refers to a topological invariant versus an example of a SMF or
elliptic genera as used in other sections.

– 22 –

JHEP04(2017)057

Table 1. Summary of logarithmic corrections to ln d(Q) for SMF built out of weak Jacobi Forms,
and with maximal polarity D = 1. Here Λ ≫ 1 which controls the scaling of Q.

## PDF page 25

CY6 : As a first example, which is not related to χ10 , consider
Φ1 (Ω) = Exp-Lift( φ0,3 ) .

(3.54)

The paramodular group is Γ+
3 , the weight is 1, and the first few coefficients of the
Jacobi form are
(3.55)
φ0,3 = φ20, 3 = y + 2 + y −1 + q(· · · ) ,
2

with φ0,3/2 as defined in (A.9).
If χ0 = χ1 = 0, then the relation between φ0,3 is the elliptic genus for a CY6 is
(3.56)

For this specific class of Calabi-Yau manifolds we will have that the divisor is just
H1 (1).
CY4 : Another example of SMFs is given by
Φ2 (Ω) = Exp-Lift(φ0,2 ) .

(3.57)

The paramodular group is Γ+
2 , the weight is 2, and φ0,2 is defined in (A.10). Its
relation to the Elliptic genus for a CY4 is
χ(τ, z)CY4 = −χ1 φ0,2 (τ, z) ,

(3.58)

where CY4 has χ0 = 0. And as expected the only divisor in this case is H1 (1).
CY3 : In this case we have
Φ(3) (Ω) = Exp-Lift(φ0, 3 (τ, 2z)) .
2

(3.59)

The paramodular group is Γ+
6 , but it is important to note that the weight is zero
(the subscript ‘3’ here refers to CY3 ). What is interesting of this example is that the
divisor is H1 (1) − H1 (5): we have both a pole and a zero. In a sense, Φ(3) is for Γ+
6
what the J-function represents for SL(2, Z). Having a zero and a pole does not affect
in an obvious manner our derivations, but it might be interesting to explore if such
feature has any physical repercussions.
The relation between φ0, 3 to the elliptic genus of CY3 is
2

1
χ(τ, z)CY3 = e(M )φ0,3/2 (τ, z) ,
2
where
e(M ) =

3
∑
p=0

(−1)p χp (M ) = 2(h1,1 − h2,1 ) .

(3.60)

(3.61)

Note that depending on the sign of e(M ) we would either want to consider in (3.44)
Φ(3) itself or its reciprocal. Assuming that e(M ) > 0, we have
1
k = c(0, 0) = 0 ,
2

– 23 –

1
m1,1 = e(M ) ,
2

(3.62)

JHEP04(2017)057

χ(τ, z)CY6 = −χ2 φ0,3 (τ, z) ,

## PDF page 26

which is the data that governs the logarithmic corrections. While Φ(3) is not the
counting formula for N = 2 BPS black holes in 4D, it is interesting to compare
the coefficients of the log corrections; the results in [10] predict that logarithmic
correction to the black hole entropy is (2 − e(M )/24) ln Λ2 which does not match any
of the regimes listed in table 1.

|y| < 1

⇒

Imz > 0 .

(3.63)

Our contour C has to lie within this domain, and therefore any further manipulation of the
variables has to be compatible with this restriction. In particular, our saddle point (3.7)
needs to be compatible with (3.63), which requires
Imzmax =

l
>0.
2tf |λ|

(3.64)

Therefore, our derivations so far only apply if the U(1) quantum number is positive. But
this is rather mild condition that does not tamper with the main portion of our results in
table 1. More generally, the convergence condition (3.63) depends on the Humbert surface
in play. As we will see in our next example, the specification of the contour dramatically
tampers with the growth in d(Q).
Our second obstacle is the residue at a given pole. In certain cases, such as H1 (1)
and ϕ ∈ J weak , we can write simple expressions such as (2.33) which allow us to derive
universal results for d(Q) that are applicable in a wide regime of charges. For general
Humbert surfaces the task is more difficult. In the next subsection we will show how we
can overcome some of these difficulties for Humbert surfaces of the type HD (0).
3.2.3

χ35

Let us now return to classical SMF. The Igusa modular form χ35 is the first SMF of odd
weight with respect to Γ1 = Sp(4, Z). The most common definition of χ35 is given in terms
of a theta series which can be found in e.g. [25]. For our purposes it is better to write it as

– 24 –

JHEP04(2017)057

Before addressing other SMFs, let us discuss briefly what are potential differences and
obstacles if we have a form where the most dominant Humbert surface is not H1 (1). So
far, there are two important technical features in our derivations: identifying the most
dominant pole, and the explicit expressions of the residue around that pole. The first
feature is straightforward and transparent, which is outlined in (3.5)–(3.12). However,
there is an important issue that we have not addressed so far. Basically we need to discuss
our choice of contour that encloses this pole and if this imposes significant restrictions on
the saddle point.
In a nutshell, our contour is restricted by the convergence of the expansion of the SMF.
This is important since we are taking reciprocals of cusp forms which contain poles and we
have to decide on which side of the pole we stand. Fortunately, the potential restrictions
for H1 (1) are rather simple: we are expanding 1/Φ(Ω) around z = 0, and to guarantee
convergence we choose

## PDF page 27

an exponential lift (2.23) as in [32]. Explicitly we have
(2)

χ35 = Exp-Lift(ϕ0,1 )(Ω)
∏
(2)
2
= q 3 yp2
(1 − q n y l pm )f1 (4nm−l ) .

(3.65)

(n,l,m)>0

Here the seed in the lift is the nearly holomorphic Jacobi form
(2)

ϕ0,1 = (T2 − 2)φ0,1 ,

(3.66)

(2)

ϕ0,1 (τ, 0) = q −1 + 72 + 196884q + 21493760q 2 + · · ·
= 72 + J(q) ,

(3.69)

with J(q) the J-function. This gives an elegant tie of χ35 to near-extremal CFTs as
defined [41] which would be interesting to study further. The first few Fourier coefficients
of χ35 are
[
(
(
)
χ35 = q 2 yp2 (q − p) 1 − y −2 + q y −4 + 69y −2 − 69 − y 2 + p y −4 + 69y −2 − 69
)
]
−y 2 + q(−y −6 + 32384y −3 + 129421y −2 − 129421 − 32384y + y 4 ) + · · · , (3.70)

and the first few terms of its Fourier-Jacobi decomposition are
(
)
( 3
)3
φ−1,2
χ35 = p2
E4 − E62
5159780352
)
(
)
( 3
2 2 (
)
E
−
E
φ
−1,2
4
6
+ ··· ,
+p3
18E42 E6 φ−2,1 − 11E43 φ0,1 − 7E62 φ0,1
644972544

– 25 –

(3.71)

JHEP04(2017)057

(2)

with T2 the Hecke operator (A.15). That is, the function c(2) (mn, l) = f1 (4mn − l2 ) is
(2)
given by the Fourier coefficients of ϕ0,1 . We can evaluate (A.15) acting on φ0,1 explicitly
to obtain
)
(
−N
(4)
(2)
− 1)f1 (N ) + δ0,N f1 (N/4) ,
(3.67)
f1 (N ) = 8f1 (4N ) + 2(
2
(
)
where δ (k) is the periodic Kronecker delta, −N
is the Kronecker symbol and f1 (N ) are
2
the Fourier coefficients of φ0,1 .
The exponential lift (3.65) is rather interesting. Although the Hecke operators Tp map
Jacobi forms to Jacobi forms of the same weight and index, their action on weak Jacobi
forms is not as nice. In particular, they do not map weak Jacobi forms to weak Jacobi
(2)
forms. For example, the function ϕ0,1 has coefficients with 4n − l2 < −1, and therefore is
not holomorphic. However, it is a nearly holomorphic Jacobi form. Its first few Fourier
coefficients are given by
(
)
(2)
ϕ0,1 (τ, z) = q −1 + y −2 + 70+y 2 + q 70y −2 + 32384y −1 + 131976 + 32384y + 70y 2 + · · · .
(3.68)
The generator χ35 can thus be written as the exponential lift of a nearly holomorphic
Jacobi form. Moreover, for y = 1, we have

## PDF page 28

where E4,6 are the Eisenstein series with E43 − E62 = 1728∆ and the other Jacobi forms are
defined in (A.6).
In relation to our goal, the question is: could χ35 count the entropy of a black hole?
Or more broadly, could it have a gravitational (or stringy) interpretation? To answer that,
as for the other examples, let us consider the asymptotic growth of
∫
1
d(Q) = dτ dρdz e−2πiQ·Y
.
(3.72)
χ35 (Ω)
C

While this has an elegant structure, it is not the dominant pole as Q2 ≫ 1. Nonetheless,
as a side remark note that the residue of 1/χ35 is governed by the J-function and powers
of the η-function; this will give a drastically different behavior for d(Q) relative to 1/χ10 ,
as we will show below.
In the asymptotic regime the focus has to be on H4 (0) (the Humbert surface with
maximal discriminant) for which the relevant poles are the images of
p=q .

(3.74)

However, relative to a pole at y = 1 and the analysis around (3.63), this pole is more subtle:
our contour is restricted by the convergence of the expansion which will affect dramatically
d(Q). Given (3.65), we want to expand 1/χ35 in the regime14
∣ −1 ∣
∣pq ∣ < 1
⇒
Imρ > Imτ .
(3.75)

The inequality clearly breaks the exchange symmetry ρ ↔ τ . Throughout our approximations to estimate d(Q) we have to respect (3.75). In particular, the saddle point (3.7) has
to be compatible with this inequality, and this leads to
n>m.

(3.76)

This sharpens our second regime from n ∼ m to a strict inequality. It won’t be impossible
to access our third regime, when m ≫ n ≫ 1; as we will see below it will just require a
more detailed inspection of the contour and the residue.
For n > m, we can proceed as we did before with our approximations and test their
validity. An interesting feature, absent in other examples, is that in the case of χ35 special
care is needed because the residue will have additional poles at finite values of (ρ, τ, z).
13

We note that there is a typo in [29] for the residue of χ35 . The steps to derive this residue follow closely
from those in [42].
∣
∣
14
We could as well be on the other side of the pole (3.74) by choosing instead ∣qp−1 ∣ < 1. Physically we
are making a choice if either p or q capture the polar contribution of the CFT. Regardless of this choice
our results are unchanged.

– 26 –

JHEP04(2017)057

Recall that we take the reciprocal so that we can have exponential growth in the Cardy
regime. To estimate the growth of d(Q) we need to analyze its divisor, which are given
by the surfaces H1 (1) and H4 (0). For H1 (1), the pole is in the orbit of z = 0 and around
there we have13
χ35 = 4πiz η(τ )72 η(ρ)72 (J(p) − J(q)) + · · · .
(3.73)

## PDF page 29

To proceed, lets evaluate the contribution of the surface H4 (0). Using (3.12) we need to
integrate around
(τ ρ − z 2 ) + 1 = 0 ,
(3.77)
where we used that for χ35 we have t = 1, D = 4, b = 0 and e = 1. Solving for ρ and
performing the contour integral gives
(
)
∫
2πimz 2 2πim
d(Q) ≈ 2πi dτ dz exp −2πinτ − 2πilz −
+
fres (τ, z) ,
(3.78)
τ
τ
C

with
τ⋆ = i

√

2m2
,
Q2

z⋆ = −

lτ⋆
.
2m

(3.80)

We can easily see that the constraint Im(ρ) > Im(τ ) implies n > m.
One might be concerned about the behavior of the residue at (3.77) and hence the
validity of (3.79). It is a difficult problem to extract an exact formula for the residue, so
the best we can do at this stage is to proceed as follows. First we expand χ35 in powers of
ρ̂ = ρ − (z 2 − 1)/τ , that is,
( 2
)
z −1
χ35 (Ω) = h
, τ, z ρ̂ + O(ρ̂2 ) .
(3.81)
τ
The residue is then simply
fres (τ, z) =

1
h

(

z 2 −1
τ , τ, z

) .

(3.82)

On the other hand we can expand χ35 first in powers of z and then in powers of ρ̂, that is,
χ35 (Ω) = 4πi∆(−1/τ )3 ∆(τ )3 J ′ (−1/τ )z ρ̂ + O(z 2 , ρ̂2 ) ,

∆(τ ) = η(τ )24 ,

(3.83)

where we used the fact that ρ̂ = ρ + 1/τ + O(z 2 ) and (3.73). This implies that we must
have
)
( 2
z −1
, τ, z = 4πi∆(−1/τ )3 ∆(τ )3 J ′ (−1/τ )z + O(z 2 ) ,
z≪1.
(3.84)
h
τ
where J ′ (τ ) is the derivative of the J-function. Moreover, using the fact that
J ′ (−1/τ ) = τ 2 J ′ (τ ) ,

(3.85)

we have J ′ (i) = 0, and therefore fres (τ, z) has a pole at (z, τ ) = (0, i). At this point we also
have ρ = i and thus the pole (z, τ ) = (0, i) lies precisely at the boundary Im(ρ) = Im(τ ).

– 27 –

JHEP04(2017)057

where fres (τ, z) is the residue of 1/χ35 around (3.77). We choose a contour C such that
one has Im(ρ) > Im(τ ). If we do a saddle point approximation, where we assume that the
integral is dominated by the explicit exponential factor, we obtain
( 2)
√
τ⋆
4π Q2 /2
d(Q) ∼ 2πi e
fres (τ⋆ , z⋆ )
,
(3.79)
2m

## PDF page 30

d(Q) ∼ 2πi e

4π

√ 2

Q /2

fres (τ⋆ , z⋆ )

(

τ⋆2
2m

)

− 2π 2

e2π(m+n)
,
∆(i)6 J ′′ (i)

m>n.

(3.86)

For m ∼ n, with m > n, τ⋆ and z⋆ are O(1) and so fres cannot become large. Moreover,
√
since we have the strict inequality m + n > 2 Q2 /2, we can approximate
d(Q) ∼ e2π(m+n) ,

m > n ≫ 1,

(3.87)

which shows that for m > n the degeneracy has Hagedorn growth instead of Cardy growth,
characteristic of the regime n > m.
3.2.4

χ12

As a last example we now turn to χ12 : this is a SMF of weight 12 under Sp(4, Z). It is a
cusp form defined by
)
1 ( (2)
(2)
χ12 =
E12 − (E6 )2 ,
(3.88)
N
(2)

where E12,6 are the Eisenstein series of genus two defined in [25] and N is a normalization
such that the coefficient of qpy is set to one. The first few coefficients are
(
)
χ12 = p q(y −1 + 12 + y) + q 2 (10y −2 − 88y −1 − 132 − 88y + 10y 2 ) + · · · ,
(3.89)

and the few terms in the Fourier-Jacobi expansion of χ12 .
( 3
)
)
E4 − E62 (
E 3 − E62
6E4 φ2−2,1 − φ20,1
φ0,1 + p2
χ12 = p 4
1728
864
( 3
)
2
)
(
2
3
3
3 E4 − E6
63E4 φ−2,1 φ0,1 − 60E6 φ−2,1 − 7φ0,1 + · · · .
−p
6912

(3.90)

To our knowledge, χ12 cannot be written as a exponential lift of the form (2.23).
However, we can still use it to build counting formulas with ‘black hole’ features. In [30]

– 28 –

JHEP04(2017)057

Since the contour C is chosen to lie inside the region Im(ρ) > Im(τ ), for n > m we
really don’t need to know the exact expression for fres if we only want to estimate the
leading growth and its logarithmic correction. In the intermediate regime where n ≳ m
(close to the inequality (3.76)) the moduli near the saddle point (3.80) does not scale as
m ∼ Λ. And in the regime n ≫ m, the robustness and universality of the Cardy regime
guarantees that the residue cannot affect the position of the saddle, which implies that
fres should not diverge as τ⋆ → i0+ . Therefore, for n > m the growth will be exponential
as in (3.79); and the logarithmic corrections will be dominated by the weight (k = 35) as
n ≫ m, and by the order of the pole (m4,0 = 1) for n ≳ m.
However when m > n one has that Im(ρ) < Im(τ ) at the saddle point (3.80). Therefore
one has to deform the initial contour C to pass through the new saddle point and as a
consequence it will have to cross the boundary Im(ρ) = Im(τ ). Since the pole of fres (τ, z)
at (z, τ ) = (0, i) lies precisely at this boundary, when deforming the contour we will pick
the contribution of this pole, and thus

## PDF page 31

it is shown that χ10 and χ12 do not share any zeroes.15 This in particular implies that the
Fourier coefficients of a combination such as
Φ(Ω) =

χ12
,
χ10

(3.91)

where we integrated over the pole ẑ = 0, and the hatted variables are given in (3.23). In
contrast to (3.28), note that we don’t have a contribution from the residue since near ẑ = 0
the behavior is [30]
χ12 = η(τ̂ )24A η(ρ̂)24A + · · · ,
(3.93)
and hence the contribution from the residue in (3.26) cancels against χ12 . The results
for the asymptotic behavior are also very simple: following the results in table 1 we have
k = −2 and m1,1 = 2. Therefore, for all three scaling regimes we find
√
Q≫1.
(3.94)
ln d(Q) ∼ π 2Q2 + 0 × ln Q ,

One important assumption we are making in this example is that the contour of integration is further restricted by the addition of χ12 relative to the one used for χ10 . We
have not found evidence of such restriction, but we do not have a rigorous proof.

4

Physical interpretation of SMFs

In this section we will discuss physical interpretation of SMFs from a CFT2 perspective
and a gravitational perspective. On the CFT side the emphasis will be on how and when
can we interpret our examples in terms elliptic genera of SCFTs. On the gravitational side
we will suggest how we could read off more detailed information about the gravitational
theory besides its black hole features.
4.1

CFT origin of a SMF

We would now like to give a physical interpretation to at least some of the SMFs that we
have been discussing. For those that can be cast as an exponential lift, the interpretation
is simple: as illustrated by (2.25), we can easily interpret it as the generating function of
symmetric products (up to the contribution of possible prefactors), and the only challenge
is to interpret the Jacobi form that enters in the exponential lift. In this section we want to
deviate from this class of examples. Without resorting to a product expansion of a SMF,
we want to discuss if it is possible to interpret them as generating functions of generalized
partition functions such as the elliptic genus of families of SCFTs.
As discussed in the section 2, the key observation is that the coefficients of the FourierJacobi expansions of a SMF of weight k, that is its expansion in p, are Jacobi forms of
15

We thank Miranda Cheng and Gerard van der Geer for discussions on this point.

– 29 –

JHEP04(2017)057

will have the desired features. The strategy taken in section 3.2.1 still applies with only
minor modifications: we will have
∫
2πi
(−1)l
(nτ̂ ρ̂−m+lρ̂)
− ρ̂+τ̂
gres (τ̂ , ρ̂) ,
(3.92)
d(Q) ≈
dτ̂
dρ̂
e
2
4π

## PDF page 32

weight k and index m. It is thus natural to try to interpret those forms as for instance
the elliptic genera of a family of CFTs. An immediate problem however is that the Jacobi
forms have weight k, whereas we want forms of weight 0. To address this we can try to
pull out an overall prefactor of weight k. More precisely, we define a Siegel Modular Form
Φ (possibly of negative weight) to be of Elliptic Genera type if it can be written as
Φ(Ω) = pℓ M(q, y)

∞
∑

pm ϕ0,m (q, y) ,

(4.1)

m=0

as can be seen from the exponential lift expression. The prefactor pℓ M(q, y) is thus
pφ10,1 (τ, z) (see (A.6)), and we can indeed get a family of weak Jacobi forms of weight
0. Note that this is simply a consequence of the fact that χ10 can be written as an exponential lift, and the prefactor is the first factor in (2.24). A slightly different example is
χ12 , which to our knowledge can not be written as an exponential lift. Unlike χ10 , the first
term of its Jacobi-Fourier is not a prefactor of all other terms. However, note that
χ12 =

)
E43 − E62 (
pφ0,1 + 2p2 (6E4 φ2−2,1 − φ20,1 ) + · · · ,
1728

(4.3)

and since χ12 is a cusp form, in general, we can consider
Z :=

χ12
,
∆(τ )

∆(τ ) = η(τ )24 =

E43 − E62
,
1728

(4.4)

where Z is holomorphic and hence each term in the p expansion will be a weak Jacobi
form of weight 0 and increasing index. These Jacobi forms are constrained by the fact that
χ12 was holomorphic and that it had an expansion in terms of Jacobi forms with no polar
terms, which therefore only have polynomial growth. The exponential growth thus comes
from ∆(q) in the denominator. Using this fact, one can show that the coefficients of the
weak Jacobi forms of (4.4) obey the property
c(4mn − l2 ) = 0,

4mn − l2 < −4m .

(4.5)

This means they don’t have the most polar terms as would be allowed for a generic weak
Jacobi form of that index. As a consequence, the asymptotic growth of the coefficients is

– 30 –

JHEP04(2017)057

for some holomorphic weak Jacobi forms ϕ0,m (q, y) that have zero weight and index m and
for some prefactor pℓ M(q, y) with ℓ ∈ Z. Note that M(q, y) has weight k under SL(2, Z)
transformations. If a SMF is of Elliptic Genera type, it can naturally be interpreted as
coming from a family of supersymmetric 2d CFTs theories. The SMF is then built by
taking the generating function of the elliptic genus and multiplying it with some prefactor
pℓ M(q, y). The prefactor can sometimes be given a physical interpretation as for χ10 . We
now discuss this property in a class of examples. First, we consider holomorphic SMF,
which are in the ring given in (2.11).
The Fourier-Jacobi expansion of χ10 is given by
)
p ( 3
E4 − E62 φ−2,1 (1 − 2pφ0,1 + · · · ) ,
(4.2)
χ10 =
1728

## PDF page 33

given by (B.6) with n0 = −1 and l0 = 0, namely
2

c(4mn − l ) ∼ e

4π

√(

2

l
n− 4m

)

(4.6)

1
1
1
)
= p ( 3
2
χ10
1
−
2pφ
0,1 + · · ·
1728 E4 − E6 φ−2,1
=

1

Ẑ

)
(1 + 2pφ0,1 + · · · ) =
p ( 3
2
pφ10,1
1728 E4 − E6 φ−2,1

(4.7)

Because we could pull out the factor of (E43 − E62 )φ−2,1 , the p expansion in the parentheses
of (4.7) only contains positive powers of the generators and is therefore a holomorphic
weak Jacobi form. In fact, for χ10 we know this is precisely the generating function of
the symmetric orbifold of K3. The prefactor in this case has a physical intrepretation
as counting degrees of freedom coming from the KK monopole as well as the center of
mass modes.
Note that it was crucial here that we could pull out an overall prefactor which left the
remaining expansion starting as 1 + O(p). This allowed us to use the geometric series to
invert the denominator. This procedure would not work for instance for 1/χ12 : from (4.3)
we see that the denominator contains a factor of φ0,1 , which, when expanding, would lead
to higher and higher poles in the Jacobi forms of the expansion. In fact one may ask
whether the reciprocal of any other holomorphic SMF gives a form of elliptic genera type.
We have checked this explicitly for any element of the ring up to weight 20 and none of
those SMF have such a property.
We can however consider examples of the form
χ12
1 ∑ m
p ϕ0,m .
=
χ10
p φ−2,1 m

(4.8)

For some weight zero weak Jacobi forms of increasing index. These will have an exponential
growth of the form
√
(4.9)
c(4mn − l2 ) ∼ e4π nm .
coming mostly from 1/χ10 although χ12 will give potentially interesting subleading corrections. The weak Jacobi forms are not exactly the symmetric orbifolds of K3. It would be
very interesting to give them a physical interpretation. For example, it would be interesting

– 31 –

JHEP04(2017)057

which is much slower than the usually Cardy type growth. Giving these weak Jacobi forms
a CFT interpretation, it means for instance the vacuum does not contribute to the elliptic
genus. It would be interesting to see what type of gravity interpretation can be given to
such an object.
The issue with holomorphic SMF is thus that we will never get proper Cardy growth
that increases with the index n. To get such exponential growth, we need to consider
meromorphic SMF. The simplest types of examples are reciprocals of a holomorphic SMF.
For example, in the previous section we saw that 1/χ10 was a SMF of elliptic genera type.
More precisely, we can use (4.2) to write

## PDF page 34

to check whether they correspond to an orbifold by a different oligomorphic permutation
group [23, 24, 43].
Finally, note that χ35 is a somewhat special example. It is not of elliptic genera type
in the sense we defined it here, but it can still be given a natural CFT interpretation. From
the exponential lift we know that the family of CFTs is again a symmetric orbifold of a
nearly holomorphic Jacobi seed form rather than a weak Jacobi form. If we are willing to
work with such nearly holomorphic forms, we can then give an interpretation to both χ35
and its reciprocal.
The gravitational dual of a SMF

We have provided examples of SMFs that have an extended Cardy regime. This suggests
that we could attribute this growth to a black hole within the natural ranges where a
semi-classical gravitational description is valid. The question is, if we can identify the
specific gravitational dual theory. In this section we suggest how to give a more refined
bulk interpretation of our results, and in particular how to interpret the residue formula.
This is best understood for χ10 . We will review previous work on the spectrum of chiral
primaries on AdS3 [44, 45] and its interpretation as gas of BPS multiparticle states. From
here we would like to suggest a similar interpretation for our other examples, and leave it
as future work to test this interpretation.
For exponential lifts of weak Jacobi forms for which the dominant pole is in H1 (1), we
found the residue formula (2.33) for the Fourier coefficients. Since this is an exact formula,
we can study further corrections to the leading saddle point contribution, and try to extract
information on the spectrum of the gravity dual. In particular, the pole at ẑ = 0 and its
images under modular transformations has the special feature that their residue factorize.
Near ẑ = 0 one finds
1
Φk (Ω̂)

=

1
ẑ m1,1

η(τ̂ )−24A η(tρ̂)−24A + · · · ,

A=

k + m1,1
12

(4.10)

where k is the weight of the modular form Φk and m1,1 is the order of the pole. We can
recast (3.48) as
d(Q) ≈

∫

π

dτ1 dτ2 e tτ2

(n−lτ1 +m(τ12 +τ22 ))

η(t(−τ1 + iτ2 ))−24A η(τ1 + iτ2 )−24A gres (τ1 , τ2 ) (4.11)

where we have neglected the contribution coming from the other poles, gres is given
by (3.50), and we have defined ρ̂ = t−1 (τ1 + iτ2 ) and τ̂ = t(−τ1 + iτ2 ). For simplicity
we scale all charges uniformly, i.e. m ∼ n ∼ Λ2 ≫ 1, so that τ1,2 ∼ O(λ0 ). In this regime
we can approximate
√ m1,1 −1 −1−k−m
1,1
gres ∼ Q2
,
(4.12)
τ2
so that

d(Q) ∼

∫

−1−k−m1,1

dτ1 dτ2 τ2

π

e tτ2

(n−lτ1 +m(τ12 +τ22 ))

η(t(−τ1 + iτ2 ))−24A η(τ1 + iτ2 )−24A , (4.13)

– 32 –

JHEP04(2017)057

4.2

## PDF page 35

∞
∏
− 2π
Zsugra = (1 − ζ n )−nχ(M ) , ζ = e φ0

(4.14)

n=1

where χ(M ) = 2(h1,1 − h2,1 ) is the Euler character of the Calabi-Yau manifold M .
The most interesting part comes from tracing over the BPS states due to (anti)-M2
branes wrapping holomorphic two cycles in M . This can be shown to equal the GopakumarVafa BPS invariants partition function [45]: that gives
ZM 2 =

∏

(
)kd0n
ta
a
k −2πna φ0
1− ζ e

2r−2
∏(

∏

na >0,r>0 l=0

na >0,k>0

1 − ζ r−l−1 e

a
−2πna t 0
φ

(

)

)(−1)r+l 2r−2 drn
l

a

,

(4.15)
and Z M 2 for the anti-M2 brane trace. Here ta denotes the complexified Kahler class of the
holomorphic cycle, that is, ta = pa + iφa in the near horizon variables. The first product
comes from M2 branes wrapping genus zero curves while the second corresponds to the
wrapping of genus r curves.
If M has the form T 2 × K3 then the counting simplifies considerably. Firstly the
supergravity modes contribution (4.14) is trivial since we have χ(M ) = 0. On the other
hand the M2 brane contribution is independent of the parameter ζ and gives simply
ZM 2 =

∞
∏

1

(1 − e

−2πn1 t 0 −χ(K3)
φ

)

,

χ(K3) = 24 ,

(4.16)

n1 >0

where, in this case, t1 is the Kahler parameter of T 2 . For χ10 , the gravity counting (4.16)
is precisely the infinite product in (4.13), with a suitable identification of the supergravity
variable t1 /φ0 = (p1 + iφ1 )/φ0 with τ2 + iτ1 .

– 33 –

JHEP04(2017)057

where we ignored overall factors of Q2 . This formula contains more information than just
the leading black hole entropy area formula. To illustrate how much is captured by it, let
us discuss the case of χ10 , for which t = 1 and A = 1.
An interesting portion to interpret from this formula is the infinite products in the ηfunctions. For χ10 the infinite product arises from a trace over a gas of multiparticle BPS
particles: in [45] they show that this piece comes from contributions of the 5D supergravity
multiplets which includes the graviton, vectors and hypermultiplets and also from (anti)M2 branes wrapping holomorphic two cycles on the Calabi-Yau.
Lets discuss in a bit more detail how the analysis of [45] breaks down for M-theory
on AdS3 × S 2 × M with M a Calabi-Yau 6-fold. Here one has thermal AdS3 . To relate
to the black hole problem we have to perform a modular transformation, which takes the
complex structure of the boundary torus τ to −1/τ . For the extremal black hole that
we are interested we have τ = iφ0 , where 1/φ0 can be identified with the radius of the
M-theory circle in the near horizon geometry (C.15) of the black hole. The analysis of the
supergravity modes is standard: the massless spectrum consists of the graviton multiplet,
nV = h1,1 − 1 vectormultiplets and nH = 2(h2,1 + 1) hypermultiplets. The spectrum on
AdS3 × S 2 × M organizes into short representations of SL(2, R) × SU(1, 1|2) that can be
found in [44, 46]. The trace that one obtains after summing over the supergravity modes is

## PDF page 36

Both (4.16) and (4.13) are valid in a large central charge limit, i.e. m ≫ 1 and τ1,2 ∼
However we know that at finite central charge the counting of chiral primaries on
AdS3 suffers from a stringy exclusion principle [47] and the result of [45] does not take
this into account. In addition the expressions (4.16) and (4.13) are not spectral flow
invariant. The large central charge limit allows us to relax both the stringy exclusion
principle and the spectral flow symmetry, and thus sum over all the chiral primaries in
supergravity with no restriction. It is interesting to note that for χ10 one can take into
account the exclusion principle in [47] by studying instead (4.11). In [48, 49] the result
for the microscopic degeneracy is shown to be a finite sum of Bessel functions, which is
suggestive of a Rademacher expansion. As a matter of fact, the factors that multiply
the Bessel functions can be identified with the polar coefficients [49] in a mock-Jacobi
expansion [27]. Since under spectral flow from R to NS sector, the polar state degeneracy
is mapped to the counting of chiral primaries, one can use the residue formula to make
interesting predictions about the spectrum of KK fields of the dual bulk theory. Moreover,
on a general note the study of the polar coefficients gives non-trivial information about
both perturbative and non-perturbative corrections to black hole entropy. It would be
interesting to address these corrections using localization techniques as in [48, 50, 51].
The general lesson that we draw from χ10 is that the residue can be interpreted as
counting fluctuations around the black hole, and these fluctuations are governed by the
gravitational modes in question: basically counting the chiral primaries in the supergravity
spectrum. Since (4.11) and (4.13) is as well applicable for other SMFs, it is rather natural
to speculate that we can give a gravitational interpretation for our examples in section 3.2.2
that involve elliptic genera of other Calabi-Yau manifolds. The task we have ahead of us is
to craft the appropriate supergravity theory which has the right spectrum to account for
all the factors in (4.13).16 We leave the answers to these questions for future work.
Λ0 .

Discussion

The goal of this work was to generalize the black hole microstate counting from the wellknown examples such as χ10 to more general setups. We have shown that many of the
methods used in the original setup can also be applied for general Siegel modular forms.
More importantly, we also found novel examples of SMFs that satisfy the criteria in section 1.2: SMFs that have the correct features to account for black hole entropy, and seemingly a supergravity regime, includes the exponential lifts of Elliptic Genera of Calabi-Yau
manifolds in section 3.2.2, and the combination of χ12 and χ10 in section 3.2.4. This shows
how we can easily build and characterize SMFs that have the potential to describe black
holes or other gravitational systems.
We found that the leading contributions and the logarithmic corrections only depend
on some very elementary data, namely the weight of the form, the poles and their residues;
and we have cast this data also in terms of the Jacobi form that defines the exponential
lift of the SMF. This gives the logarithmic correction in (1.5) a microscopic interpretation
16

Note that if we consider a different Calabi-Yau manifold in (4.15) and (4.16), we will not obtain (4.13).
This makes it more challenging to decode which gravitational theory is the dual to the examples listed in
section 3.2.2.

– 34 –

JHEP04(2017)057

5

## PDF page 37

– 35 –

JHEP04(2017)057

in terms of CFT data. In this sense the entropy is quite universal. For forms with the
same type of poles as 1/χ10 , that is with divisors given by H1 (1) listed in section 3.2.2, we
were able to repeat the original arguments fully and thus give complete results. For more
complicated divisors, it is clear that the same methods still work, but doing the analysis
will require some more work. We were able to obtain the entropy in some of the regimes,
but our analysis for χ35 shows that the results can be different, such as having a Hagedorn
regime rather than Cardy regime. The main technical issues here are obtaining efficient
expressions for the residue, and choosing the contours of integration carefully. It will be
very interesting to explore the behavior of d(Q) for more general Humbert surfaces. A first
direction along this lines is when the Humbert surface is HD (0), i.e. extending the analysis
of χ35 for other SMFs.
This is related to a second point. In this paper we only considered the growth of black
hole states, that is states with polarity Q · Q > 0. To investigate potential gravity duals,
knowing the perturbative spectrum, i.e. the polar states, is just as important. The growth
of these states will for instance help to decide whether we are looking at a supergravity
theory, or a full blown string theory. Moreover the growth will be related to how far
the Cardy regime extends. Our results for χ35 for instance indicate that the polar states
grow like Hagedorn. Using similar techniques as in [52], one can indeed check this explicitly.
This is in contrast to χ10 , where the polar states agree with just the supergravity spectrum,
which of course grows much more slowly. We expect that the examples in section 3.2.2 can
also be identified with a supergravity theory, which we will settle in future work.
Ultimately of course the goal is to decide if our SMF have gravity duals. For this we
still need to better understand the spectrum, as discussed in section 4.2. It is particularly
important to understand in what cases we have supergravity growth and a Cardy regime
that extends even to E ≪ c, and in which cases we have Hagedorn growth. In the former
case, it may be possible to construct corresponding supergravity solutions. In the latter
case, we should not expect such supergravity solutions, since the duals will be intrinsically
stringy. Moreover the appearance of nearly holomorphic Jacobi forms suggests that some
of the duals will have less supersymmetry than what we are used to. We leave this for
future work.
In the context of finding counting formulas with black hole features, it would be interesting to explore if we can relax the condition of having Sp(4, Z) as a symmetry. This
exchange symmetry among ρ and τ is usually interpreted in the gravitational theory as
electro-magnetic duality. This is a symmetry we know does not persist at the full quantum
level for many black holes (such as N = 2 theories in 4D and 5D solutions). It would
be interesting to investigated if we can achieve an extended Cardy regime by exploiting a
different symmetry of the generating function. Along these lines, an interesting example is
to understand in this language the counting formula for BPS states in N = 8 supergravity:
there are exact formulas for the index [53, 54], and it would be interesting to investigate if
there are related forms with similar mathematical properties.
Finally, we would like to mention wall crossing phenomena. They are intimately related
to the meromophicity of the generating functional, leading to interesting properties related
to Mock modularity [27]. On the gravitational side the interpretation of wall crossing is
in terms of multicentered black holes [38, 55]. In contrast to χ10 , where the order of the

## PDF page 38

pole is m1,1 = 2, our other examples have generically higher order poles, a phenomenon
that also appeared in a different context in [56]. This may have interesting repercussions
for the phase space of black holes.

Acknowledgments

A
A.1

Jacobi forms
Properties of Jacobi forms

A Jacobi form ϕk,m (τ, z) is a holomorphic function on H × C → C that has the following
defining properties: first, under modular transformations
(
)
)
(
)
(
2
2πimcz
z
aτ + b
a
b
= (cτ + d)k exp
ϕk,m (τ, z) , ∀
∈ SL(2, Z) ,
,
ϕk,m
cτ + d cτ + d
cτ + d
c d
(A.1)
and second, under translations
(
)
ϕk,m (τ, z + λτ + µ) = exp −2πim(λ2 τ + 2λz + µ) ϕk,m (τ, z) , λ, µ ∈ Z ,
(A.2)

and it has Fourier expansion
ϕk,m (τ, z) =

∑

c(n, l)q n y l ,

q = e2πiτ ,

y = e2πiz .

(A.3)

n≥0,l
4mn≥l2

We define the discriminant ∆ := 4nm − l2 . The coefficients c(n, l) then only depend on ∆
and l (mod 2m), and in fact only on ∆ if m is prime. We will denote the space of Jacobi
forms of weight k and index m by Jk,m .
There are several special cases and generalizations of Jacobi forms which have to
do with the summation range in (A.3). Jacobi cusp forms are Jacobi forms for which
c(0, l) = 0. In particular they vanish at the cusp τ = i∞.
Weak Jacobi forms are holomorphic functions that satisfy (A.1) and (A.2), but for
which we don’t impose the condition that c(n, l) = 0 if ∆ < 0. One can however show that
we have c(n, l) = 0 if ∆ < −m2 , leading to a Fourier expansion
∑
c(n, l)q n y l .
(A.4)
ϕk,m (τ, z) =
n≥0,l
4mn−l2 ≥−m2

Note that we are still only summing over n.

– 36 –

JHEP04(2017)057

It is a pleasure to thank Kathrin Bringmann, Miranda Cheng, Francesca Ferrari, Gerard
van der Geer, Finn Larsen, Sameer Murthy and Ashoke Sen for helpful discussions. CAK
thanks the Harvard University High Energy Theory Group for hospitality. AB is supported
by the Foundation for Fundamental Research on Matter (FOM). AC is supported by Nederlandse Organisatie voor Wetenschappelijk Onderzoek (NWO) via a Vidi grant. CAK is
supported by the Swiss National Science Foundation through the NCCR SwissMAP. The
work of AB, AC and JG is part of the Delta ITP consortium, a program of the NWO that
is funded by the Dutch Ministry of Education, Culture and Science (OCW).

## PDF page 39

Nearly holomorphic Jacobi forms finally satisfy (A.1) and (A.2), but are allowed to
have a pole at the cusp q = 0. More precisely, ϕ is a nearly holomorphic Jacobi form if
there is a non-negative n such that ∆(q)n ϕ is a Jacobi form. In total we thus have the
inclusions
J cusp ⊂ J ⊂ J weak ⊂ J nh .
(A.5)
We will mostly work with weak Jacobi forms. A few commonly used weak Jacobi forms are
φ10,1 (τ, z) = η(τ )18 θ1 (τ, z)2 ,

φ−1,2 (τ, z) =

θ1 (τ, 2z)2
,
η(τ )3

(A.6)

where η(τ ) and θi (τ, z) are the usual Dedekind eta function and theta functions, and
1
θi (τ ) ≡ θi (τ, 0). In some portions of the text we use ∆(τ ) ≡ η(τ )24 = 1728
(E43 − E62 ). In
fact, the ring of weak Jacobi forms of integer index is freely generated,
J weak = C[E4 , E6 , φ0,1 , φ−2,1 , φ−1,2 ]/(432φ2−1,2 − φ−2,1 φ30,1 + 3E4 φ3−2,1 φ0,1 − 2E6 φ4−2,1 ) .
(A.7)
weak
The space Jk,m of weak Jacobi forms of weight k and index m is given by appropriate
polynomials of the generators. The space of half-integer index weak Jacobi form is closely
weak . We have
related to Jk,m
weak
weak
J2k,m+
1 = φ0, 3 J2k,m−1 ,
2

2

weak
weak
J2k+1,m+
1 = φ−1, 1 J2k+2,m ,
2

2

(A.8)

where
φ0, 3 (τ, z) =
2

φ−1, 1 (τ, z) =
2

∞

∏
θ1 (τ, 2z)
(1 + q n−1 y)(1 + q n y −1 )(1 − q 2n−1 y 2 )(1 − q 2n−1 y −2 )
= y −1/2
θ1 (τ, z)
θ1 (τ, z)
= −y
η(τ )3

n=1
∞
∏
−1/2

(1 − q n−1 y)(1 − q n y −1 )(1 − q n )−2

n=1

Another weak Jacobi form used in the main text is
( )( )
∑
m+n
3m2 +n2
1
−4
12
−4
φ0,2 (τ, z) = η(τ )
(3m − n)
q 24 y 2
2
m
n
m,n∈Z
−1

= (y + 4 + y

A.2

(A.9)

) + q(y ±3 − 8y ±2 − y ±1 + 16) + q 2 (· · · ) .

(A.10)

Jacobi forms as partition functions

Jacobi forms appear in physics quite often in the form of generalized partition functions.
Consider a fermionic CFT with a U(1) current J. In the Ramond sector partition function

– 37 –

JHEP04(2017)057

θ1 (τ, z)2
,
η(τ )6
(
)
θ2 (τ, z)2 θ3 (τ, z)2 θ4 (τ, z)2
φ0,1 (τ, z) = 4
+
+
,
θ2 (τ )2
θ3 (τ )2
θ4 (τ )2

φ−2,1 (τ, z) =

## PDF page 40

with the fermion parity operator (−1)F inserted, τ and z are then the chemical potentials
of the weight and U(1) charge respectively. Eq. (A.1) is then a direct consequence of the
modular transformation properties of genus 1 amplitudes. Eq. (A.2) is usually interpreted
as invariance under spectral flow by one unit.
The most common setup for this is the elliptic genus of theories with at least N = (2, 2)
superconformal symmetry. In that case we can define the elliptic genus as
χ(τ, z) = TrRR (−1)F (−1)F̄ q L0 −c/24 q̄ L̄0 −c/24 y J0 ,

(A.11)

L0 −

c
= (G0 )2 ≥ 0 ,
24

(A.12)

which means that in (A.3) n ≥ 0. It follows that χ is a weak Jacobi form, in fact of weight
0 and index m = c/6. A typical example of this is the non-linear sigma model on K3,
whose elliptic genus is simply
χK3 (τ, z) = 2φ0,1 (τ, z) .

(A.13)

For Calabi-Yau threefolds, there is a one-dimensional vector space. The elliptic genus
depends only on the Hodge numbers and is given by
1
χ(τ, z) = (h1,1 − h2,1 )φ0,3/2 (τ, z) = e(M )φ0,3/2 (τ, z) .
2

(A.14)

Note that generically we expect the elliptic genus to be a weak Jacobi form, and not a
Jacobi form. The coefficients of Jacobi forms grow only polynomially, whereas we expect
the underlying CFT to have Cardy growth, which agrees with the exponential growth of
weak Jacobi forms. In this supersymmetric setup we can in particular spectrally flow by
half a unit from the NS sector to the Ramond sector and vice versa. The left-moving NS
vacuum is then mapped to the term y c/6 , which is clearly a polar state, so that the resulting
form is a weak Jacobi form. It is however possible that due to an enhanced symmetry, the
Witten index of the right-moving states that couple to the left-moving vacuum vanishes,
so that this term does not appear in the elliptic genus, and similar for all other polar
terms. Unless such cancellations happen however, we will get a weak Jacobi form and not
a Jacobi form.
On the other hand we can try to generalize the elliptic genus to CFTs with less supersymmetry. To ensure that the resulting partition function is (nearly) holomorphic, we
need either a chiral (purely left-moving) theory, or at least N = 1 supersymmetry for the
right-movers, so that we can repeat the Witten index argument. On the left-moving side
we need a U(1) current. Eq. (A.1) is then automatically satisfied, see e.g. [57, 58] and references therein. To satisfy (A.2), it is enough to have something similar to integer spectral
flow. A sufficient condition for that is to only have states of integer U(1) charge: the idea
is that we can bosonize the U(1) current, and under suitable integrality conditions on the
charges, eiφ is then a local operator that induces integral spectral flow. In such a theory we

– 38 –

JHEP04(2017)057

which due to right-moving supersymmetry is indeed independent of q̄. Left-moving supersymmetry gives the constraint

## PDF page 41

no longer have the condition that n ≥ 0, which would allow for nearly holomorphic Jacobi
forms as partition functions.
More generally, ϕk,m (τ, z) are also the building blocks of for chiral CFTs, as well
as warped CFTs [59, 60]. And in particular, many of the properties of exponential lifts
discussed here in principle apply to these non-supersymmetric theories. For example, it
is simple to construct a SMF for symmetric products of the Monster CFT in [61]. But
unfortunately other examples not involving supersymmetry are much less developed.
A.3

Hecke operators

Up : Jk,m → Jk,mp2

∑

n,r c(n, r)q

Vp : Jk,m → Jk,mp

Tp : Jk,m → Jk,m

nyl :

(A.15)

Note that they all map Jacobi forms to Jacobi forms. Up simply maps φ(τ, z) ↦→ φ(τ, pz),
so that
∑
φ|Up =
c(n, l/p)q n y l .
(A.16)
n,l

(Our convention is to take c(n, l) = 0 if its arguments are non-integer or outside the original
summation range.) From this it is clear that it also maps weak Jacobi forms to weak Jacobi
forms. In [32] this is essentially the operator Λp .
Vl is probably the best known Hecke operator. It acts as
φ|Vp =

∑ ∑

ak−1 c

n,l a|(n,l,p)

(

np l
,
a2 a

)

qn yl .

(A.17)

It is again clear that this also maps weak Jacobi forms to weak Jacobi forms. Physically
it is related to cyclic orbifolds, and therefore shows up crucially in symmetric orbifold
partition functions. In [32] this is essentially the operator T− (p).
Tp finally is the operator in [32] denoted by T0 (p). For φ with weight k = 0 it gives a
new form with coefficients
(
)
∑
n + λl + λ2 m l + 2λm
3
2
c
(A.18)
,
cp (n, l) = p c(p n, pl) + Gp (n, l, m)c(n, l) +
p2
p
λ

mod p

where the Gauss sum is
Gp (n, l, m) = −p +

a,b

∑

mod p

(
)
na + lab + mab2
exp 2πi
.
p

(A.19)

Very importantly, Tp does not map weak Jacobi forms to weak Jacobi forms: in general it
will give nearly holomorphic Jacobi forms instead.

– 39 –

JHEP04(2017)057

Ref. [26] defines three types of Hecke operators acting on φ =

## PDF page 42

B

Logarithms in the Cardy regime: n ≫ m

In this appendix we derive the logarithmic correction to the leading asymptotic growth of a
Jacobi form in the Cardy regime; this is the regime that we denote I in section 3. Consider
the follow integral
∫
d(n, l) =

dτ dz e−2πiτ n−2πizl ϕk,m (τ, z) ,

(B.1)

where we used (A.1). Assuming that the saddle is at some small imaginary value of τ and
)
(
z of order one,17 we can approximate ϕk,m − τ1 , τz by its most polar term
(
)
(
)
(
)
1 z
2πin0
2πil0 z
ϕk,m − ,
∼ exp −
exp
,
(B.3)
τ τ
τ
τ
where we assigned to the most polar state charges (n, l) = (n0 , l0 ), i.e. the state with most
negative discriminant ∆.18 This gives at leading order
)
(
)
(
)
(
∫
1
2πimz 2
2πin0
2πil0 z
d(n, l) ∼ dτ dz k exp −2πinτ − 2πilz −
exp −
exp
. (B.4)
τ
τ
τ
τ
The saddle point of the above integral is at
√
n0 − l02 /4m
τ⋆ =
,
n − l2 /4m
z⋆ =

l0
lτ⋆
−
.
2m 2m

(B.5)

We assumed that the original integral was dominated by the behavior of ϕk,m at τ → i0+
and z ∼ O(1): this requires that n − l2 /4m ≫ |n0 − l02 /4m| and n0 − l02 /4m < 0. For many
systems, the discriminant of the most polar term is related to the central charge c of the
system, i.e. n0 − l02 /4m ∼ c, hence we are estimating d(n, l) for n ≫ c. Performing the
saddle point approximation gives
(
(
))
4πi
l2
d(n, l) ∼ τ⋆2−k exp −
n0 − 0
τ⋆
4m
( √(
)(
))
l02
l2
2−k
− 4n0 +
∼ τ⋆ exp 2π
.
(B.6)
n−
m
4m
17

One can weaken the assumption that τ is small, but this requires further restrictions on the spectrum
of ϕ(τ, z) which are not needed for the purposes of this section. See e.g. [22] for a recent discussion on such
restrictions.
18
There could be a degeneracy associated to the most polar state, but it is negligible within the approximation taken here.

– 40 –

JHEP04(2017)057

where ϕk,m (τ, z) is a weak Jacobi form of weight k and level m. We want to estimate d(n, l)
for large values of n and l, and the easiest is to do a saddle point approximation. First we
rewrite (B.1) as
(
)
)
(
∫
1
2πimz 2
1 z
d(n, l) = dτ dz k exp −2πinτ − 2πilz −
ϕk,m − ,
,
(B.2)
τ
τ
τ τ

## PDF page 43

The leading exponential contribution is the usual Cardy formula; the polynomial contribution controlled only by the weight of ϕk,m . These corrections should be compared with
the analogous logarithmic correction in other scaling regimes.

C

Black hole near-horizon geometry and attractor equations

D4 : pa Σa , Σa ∈ H4 (Z)

(C.1)

D0 : q0

(C.3)

a

a

D2 : qa Σ̃ , Σ̃ ∈ H2 (Z)

– 41 –

(C.2)

JHEP04(2017)057

In this appendix we revisit the D1-D5-P-KK system in IIB string theory on K3 × S 1 × S̃ 1 .
This configuration preserves four out of sixteen supercharges of four dimensional N = 4
supergravity. We describe the brane Kaluza-Klein monopole configuration and the black
hole near-horizon geometry that it gives rise to. As we show, it is easier to analyze the
geometry from the IIA point of view where the attractor equations are naturally embedded
in N = 2 supergravity. We will map first the configuration to IIA and then to M-theory
where it has an interpretation as a MSW string.
This configuration consists of Q5 D5-branes wrapping K3×S 1 , Q1 D1-branes wrapping
S 1 , K Kaluza-Klein monopoles associated with the circle S̃ 1 and n units of momentum
along the circle S 1 . For K = 1 this is equivalent to putting the D1-D5-P system on the
background of a Kaluza-Klein monopole. Since the Taub-Nut geometry approaches R3 × S̃ 1
at infinity while it is R4 near the origin, this provides a five/four dimensional connection,
which relates the four dimensional black hole to the BMPV black hole. Following [62], we
start by performing a mirror symmetry transformation on K3, which take us to a D3-brane
configuration. We have now Q1 D3-branes wrapping γ × S 1 and Q5 D3-branes wrapping
γ̃ × S 1 where γ, γ̃ are a pair of dual 2-cycles in K3. A T-duality along the circle S̃ 1 takes
the D3 to D4 branes wrapping γ × S 1 × Ŝ 1 and similarly for the dual cycle, with Ŝ 1 the
T-dual circle. The Kaluza-Klein monopoles map to K NS5-branes wrapping K3 × S 1 .
1 ,
From the M-theory point of view we have Q1 M5-branes wrapping γ × S 1 × Ŝ 1 × SM
1 , K M5-branes on K3 × S 1 × Ŝ 1 × S 1 and n
Q5 M5-branes wrapping γ̃ × S 1 × Ŝ 1 × SM
M
1
1 is the M-theory circle. From the eleven
units of momentum along the circle S where SM
dimensional point of view we can reduce instead along the circle S 1 . For convenience denote
1 so we know that we are reducing M-theory along this circle. The
the circle S 1 by S̄M
final configuration corresponds to a MSW string configuration consisting of an M5-brane
1 where P is a four cycle in the class P = pa Σ ∈ H (K3×Ŝ 1 ×S 1 )
wrapping the cycle P ×S̄M
a
4
M
1 , γ̃ × Ŝ 1 × S 1 , K3). In addition one has n units of momentum along
and Σ = (γ × Ŝ 1 × SM
M
1 . From the type IIA point of view, this configuration gives rise to a D4-D0
the circle S̄M
black hole. We have pa D4-branes wrapping cycles Σa and n D0-branes. To introduce D2branes we can start form the IIB configuration and consider momentum along the circle
S̃ 1 . Under the chain of dualities described above this gives rise to D2-branes wrapping
2-cycles dual to Σa .
Summarizing one has the IIA D-brane configuration

## PDF page 44

For example, for the D1-D5-P-KK configuration one has Σ1 = K3 and Σa̸=1 = γa × T 2
with γa ∈ H2 (K3, Z). Similarly Σ̃1 = T 2 and Σ̃a̸=1 = γ̃a .
It is also useful to map the D1-D5-P-KK system to a configuration in Heterotic string
theory compactified on T 6 , consisting only of NS-NS charges. This theory has a U-duality
group G consisting of the following factors
G(Z) = SL(2, Z) × SO(6, 22; Z) .

(C.4)

Here Qi and P i are respectively the electric and magnetic charge vectors. The subscript
i denotes that it transforms under the vector representation of SO(6, 22; Z). In addition,
the dyon Γ transforms under electric-magnetic duality as
)
(
) (
)( ) (
a b
Q′ i
a b
Qi
,
∈ SL(2, Z) .
(C.6)
=
c d
c d
Pi
P ′i
It is natural to associate to the dyon the following T-duality invariant combinations
Q2 ≡ Qi Lij Qj ,

P 2 = P i Lij P j ,

Q · P ≡ Qi Lij P i ,

(C.7)

where Lij is the SO(6, 22) invariant metric. Furthermore, it is easy to check that the triplet
(Q2 , P 2 , Q.P ) transforms under the vector representation of SO(1, 2) or the symmetric
representation 3 of SL(2, Z).
Under the map from Heterotic on T 4 × S 1 × S̃ 1 to IIA on K 3 × S 1 × S̃ 1 , the charges
are assigned in the following way
Qi = (q0 , p1 , qa ) ,
P i = (−q1 , p0 , pa ) .

(C.8)

We have not included the charges corresponding to momentum/winding and NS-5/KK
monopole associated with the circles on T 4 . For example q0 D0-branes map to momentum
along the circle S 1 while p1 D4-branes wrapping K 3 map to p1 units of winding along the
circle S 1 . The T-duality invariants are therefore
Q2 = 2q0 p1 + Dab qa qb ,
P 2 = −2q1 p0 + Dab pa pb ,

Q · P = p0 q 0 − p1 q 1 + pa q a ,
where Dab is the intersection matrix of K3, that is, Dab =

– 42 –

(C.9)
∫

γa ∧ γb .

JHEP04(2017)057

The SL(2, Z) factor is responsible for electric magnetic duality while the second factor
corresponds to the T-duality group. A dyon charge configuration transforms in the fundamental of SL(2, Z) and in the vector representation of SO(6, 22; Z). Lets denote the dyon
configuration by the vector
( )
Qi
Γ=
, i = 1 . . . 28 .
(C.5)
Pi

## PDF page 45

We now describe the near-horizon geometry of the four dimensional D4-D2-D0 black
hole. The analysis is valid for any Calabi-Yau manifold and relies only on the four dimensional N = 2 supergravity. Further details of the attractor equations can be found
in [63].
The ten dimensional near-horizon metric is
(
)
L2
dr2
2
2
2
2
2
2
ds10 =
−(r − 1)dt + 2
+ dθ + sin (θ)dφ + ds2CY .
(C.10)
4
r −1
The graviphoton field is given by
(C.11)

while the remaining nV vectormultiplet gauge fields, that couple to the D2 charges, have
field strength
F a = −φa dr ∧ dt + pa sin(θ)dθ ∧ dφ ,
(C.12)
with pa the magnetic charges. The scalar fields, on the other hand, are determined in terms
of the electric fields and the magnetic charges, that is,
LX 0 = φ0 ,

LX a = φa + ipa ,

(C.13)

with p0 = 0. The remaining hypermultiplet scalar fields are freely adjustable parameters throughout the black hole geometry. Finally the Kahler form of the Calabi-Yau is
determined by
J∝

pa
.
L

(C.14)

The M-theory lift of this configuration corresponds to promoting the graviphoton gauge
field as the Kaluza-Klein gauge field associated with the M-theory circle. The uplifted
geometry contains now a local AdS3 factor,
[
]
)2
1 (
L2
ds2AdS2 + 0 2 dy − φ0 (r − 1)dt + dΩ2 + ds2CY ,
(C.15)
ds211 =
4
(φ )
where ds2AdS2 and dΩ2 denote unit size metrics for AdS2 and S 2 respectively, and y is the
M-theory circle. The vector-multiplet gauge fields uplift to
Aa5D = −

φa
dy + AaDirac ,
φ0

(C.16)

with AaDirac the Dirac monopole gauge field that gives rise to the magnetic flux (C.12).
The attractor equations relate the values of the scalar fields to the charges of the black
hole in the following way
Im(LFI ) = qI , I = 0 . . . nV ,
(C.17)
where FI = ∂X I F(X) with F(x) the prepotential of N = 2 supergravity. The attractor
equations (C.17) arise from the extremization of the functional
S(φ, p, q) = −πqI φI + πImF(φ + ip) .

– 43 –

(C.18)

JHEP04(2017)057

F 0 = φ0 dr ∧ dt ,

## PDF page 46

This fact has led to the conjecture that the black hole partition function equals the square
of the topological string partition function ZBH = |Ztop |2 [64]. Recently, it was shown that
S(φ, p, q) follows from a localization computation on AdS2 × S 2 [50].
In the two derivative approximation the prepotential is a polynomial of the scalar
fields. For the K3 × T 2 compactification one has
23

1 X1 ∑
F(X) = −
Dab X a X b .
2 X0

(C.19)

a,b=2

1
φ0
aφ
+
p
,
p1
p1
Q·P
φ1 = − 2 φ0 ,
P
p1 P 2
φ0 = √
.
Q2 P 2 − (Q · P )2

φa = −q a

(C.20)

For a more general Calabi-Yau compactification, the two derivative prepotential (C.19)
is instead given by
b2
X aX bX c
1 ∑
Dabc
,
(C.21)
F(X) = −
6
X0
a,b,c=1

where Dabc is the intersection matrix and b2 is the dimension of H (1,1) , the Kahler class.
The attractor equations are modified as
φa = −q a φ0 ,
√
P 3 /6
φ0 =
,
q̂0

(C.22)

where q̂0 = q0 − Dab q a q b /2 is the spectral flow invariant charge combination, and we have
defined P 3 = Dabc pa pb pc and Dab = Dabc pc .
Note that the attractor equations are invariant under the scaling symmetry
φI → λφI ,

qI → λqI ,

pI → λpI ,

I = 0 . . . nV .

(C.23)

When λ ≫ 1 the M-theory circle radius 1/φ0 , in units of the AdS length L, becomes very
small. This corresponds to the string-theory limit. In the other limit, that is when q ≫ 1
and p is kept fixed we have that 1/φ0 is of order one or bigger and thus the theory is well
described in M-theory.
The number of 1/4BPS states of D1-D5-P-KK system is describe by the reciprocal of
χ10 . The notation used here mapped to the one used in section 3.2.1 is as follows. The
T-duality invariants (C.7) in terms of the charge vector (3.3) is
Q2 = 2n ,

P 2 = 2m ,

– 44 –

l =Q·P ,

(C.24)

JHEP04(2017)057

Note that a, b run over the 2-cycles of K3. This leads to the following attractor solutions

## PDF page 47

and hence 2Q2 = Q2 P 2 − (Q · P )2 . The entropy (C.18) for a two derivative supergravity
√
prepotential is SBH = π 2Q2 , and in N = 4 supergravity the logarithmic correction
vanishes. On the microscopic side this corresponds to the results in (3.40). It is important
to emphasize that the dictionary (C.24) is what dictates the scaling regime for which we
need to evaluate d(Q); without this data there is room for ambiguity.
Open Access. This article is distributed under the terms of the Creative Commons
Attribution License (CC-BY 4.0), which permits any use, distribution and reproduction in
any medium, provided the original author(s) and source are credited.

[1] A. Strominger and C. Vafa, Microscopic origin of the Bekenstein-Hawking entropy,
Phys. Lett. B 379 (1996) 99 [hep-th/9601029] [INSPIRE].
[2] R. Dijkgraaf, E.P. Verlinde and H.L. Verlinde, Counting dyons in N = 4 string theory,
Nucl. Phys. B 484 (1997) 543 [hep-th/9607026] [INSPIRE].
[3] D. Shih, A. Strominger and X. Yin, Recounting Dyons in N = 4 string theory,
JHEP 10 (2006) 087 [hep-th/0505094] [INSPIRE].
[4] J.R. David and A. Sen, CHL Dyons and Statistical Entropy Function from D1 − D5 System,
JHEP 11 (2006) 072 [hep-th/0605210] [INSPIRE].
[5] A. Sen, Quantum Entropy Function from AdS2 /CF T1 Correspondence,
Int. J. Mod. Phys. A 24 (2009) 4225 [arXiv:0809.3304] [INSPIRE].
[6] A. Sen, Arithmetic of Quantum Entropy Function, JHEP 08 (2009) 068 [arXiv:0903.1477]
[INSPIRE].
[7] A. Sen, Black Hole Entropy Function, Attractors and Precision Counting of Microstates,
Gen. Rel. Grav. 40 (2008) 2249 [arXiv:0708.1270] [INSPIRE].
[8] I. Mandal and A. Sen, Black Hole Microstate Counting and its Macroscopic Counterpart,
Nucl. Phys. Proc. Suppl. 216 (2011) 147 [arXiv:1008.3801] [INSPIRE].
[9] S. Banerjee, R.K. Gupta, I. Mandal and A. Sen, Logarithmic Corrections to N = 4 and
N = 8 Black Hole Entropy: A One Loop Test of Quantum Gravity, JHEP 11 (2011) 143
[arXiv:1106.0080] [INSPIRE].
[10] A. Sen, Logarithmic Corrections to N = 2 Black Hole Entropy: An Infrared Window into the
Microstates, Gen. Rel. Grav. 44 (2012) 1207 [arXiv:1108.3842] [INSPIRE].
[11] A. Sen, Logarithmic Corrections to Rotating Extremal Black Hole Entropy in Four and Five
Dimensions, Gen. Rel. Grav. 44 (2012) 1947 [arXiv:1109.3706] [INSPIRE].
[12] A. Sen, Microscopic and Macroscopic Entropy of Extremal Black Holes in String Theory,
Gen. Rel. Grav. 46 (2014) 1711 [arXiv:1402.0109] [INSPIRE].
[13] A. Chowdhury, R.K. Gupta, S. Lal, M. Shyani and S. Thakur, Logarithmic Corrections to
Twisted Indices from the Quantum Entropy Function, JHEP 11 (2014) 002
[arXiv:1404.6363] [INSPIRE].
[14] R.K. Gupta, S. Lal and S. Thakur, Logarithmic corrections to extremal black hole entropy in
N = 2, 4 and 8 supergravity, JHEP 11 (2014) 072 [arXiv:1402.2441] [INSPIRE].

– 45 –

JHEP04(2017)057

References

## PDF page 48

[15] C. Keeler, F. Larsen and P. Lisbao, Logarithmic Corrections to N ≥ 2 Black Hole Entropy,
Phys. Rev. D 90 (2014) 043011 [arXiv:1404.1379] [INSPIRE].
[16] F. Larsen and P. Lisbao, Quantum Corrections to Supergravity on AdS2 × S 2 ,
Phys. Rev. D 91 (2015) 084056 [arXiv:1411.7423] [INSPIRE].
[17] C. Keeler, P. Lisbao and G.S. Ng, Partition functions with spin in AdS2 via quasinormal
mode methods, JHEP 10 (2016) 060 [arXiv:1601.04720] [INSPIRE].
[18] A. Sen, Logarithmic Corrections to Schwarzschild and Other Non-extremal Black Hole
Entropy in Different Dimensions, JHEP 04 (2013) 156 [arXiv:1205.0971] [INSPIRE].

[20] J.L. Cardy, Operator Content of Two-Dimensional Conformally Invariant Theories,
Nucl. Phys. B 270 (1986) 186 [INSPIRE].
[21] P. de Lange, A. Maloney and E. Verlinde, Ads/cft in the grand canonical ensemble, to appear.
[22] T. Hartman, C.A. Keller and B. Stoica, Universal Spectrum of 2d Conformal Field Theory in
the Large c Limit, JHEP 09 (2014) 118 [arXiv:1405.5137] [INSPIRE].
[23] F.M. Haehl and M. Rangamani, Permutation orbifolds and holography, JHEP 03 (2015) 163
[arXiv:1412.2759] [INSPIRE].
[24] A. Belin, C.A. Keller and A. Maloney, String Universality for Permutation Orbifolds,
Phys. Rev. D 91 (2015) 106005 [arXiv:1412.7159] [INSPIRE].
[25] J.H. Bruinier, G. van der Geer, G. Harder and D. Zagier, The 1-2-3 of modular forms,
Lectures at a Summer School on Modular Forms and their Applications, Nordfjordeid
Norway (2004), Universitext, Springer-Verlag, Berlin Germany (2008).
[26] M. Eichler and D. Zagier, The Theory of Jacobi Forms, Progress in Mathematics,
Birkhäuser, Boston U.S.A. (2013).
[27] A. Dabholkar, S. Murthy and D. Zagier, Quantum Black Holes, Wall Crossing and Mock
Modular Forms, arXiv:1208.4074 [INSPIRE].
[28] V. Gritsenko, Elliptic genus of Calabi-Yau manifolds and Jacobi and Siegel modular forms,
Algebra i Analiz 11 (1999) 100 [math/9906190] [INSPIRE].
[29] J.-I. Igusa, Modular forms and projective invariants, Am. J. Math. 89 (1967) 817.
[30] J.-I. Igusa, On siegel modular forms of genus two, Am. J. Math. 84 (1962) 175.
[31] B. Roberts and R. Schmidt, On modular forms for the paramodular groups, in Automorphic
forms and zeta functions, World Scientific Publications, Hackensack U.S.A. (2006), pg. 334.
[32] V.A. Gritsenko and V.V. Nikulin, Automorphic forms and Lorentzian Kac-Moody algebras.
Part 2, alg-geom/9611028 [INSPIRE].
[33] D.P. Jatkar and A. Sen, Dyon spectrum in CHL models, JHEP 04 (2006) 018
[hep-th/0510147] [INSPIRE].
[34] M. Bañados, M. Henneaux, C. Teitelboim and J. Zanelli, Geometry of the (2+1) black hole,
Phys. Rev. D 48 (1993) 1506 [Erratum ibid. D 88 (2013) 069902] [gr-qc/9302012]
[INSPIRE].
[35] A. Castro and S. Murthy, Corrections to the statistical entropy of five dimensional black
holes, JHEP 06 (2009) 024 [arXiv:0807.0237] [INSPIRE].

– 46 –

JHEP04(2017)057

[19] A.M. Charles and F. Larsen, Universal corrections to non-extremal black hole entropy in
N ≥ 2 supergravity, JHEP 06 (2015) 200 [arXiv:1505.01156] [INSPIRE].

## PDF page 49

[36] N. Banerjee, Subleading Correction to Statistical Entropy for BMPV Black Hole,
Phys. Rev. D 79 (2009) 081501 [arXiv:0807.1314] [INSPIRE].
[37] D. Shih and X. Yin, Exact black hole degeneracies and the topological string,
JHEP 04 (2006) 034 [hep-th/0508174] [INSPIRE].
[38] M.C.N. Cheng and E. Verlinde, Dying Dyons Don’t Count, JHEP 09 (2007) 070
[arXiv:0706.2363] [INSPIRE].
[39] D. Gaiotto, A. Strominger and X. Yin, New connections between 4 − D and 5 − D black
holes, JHEP 02 (2006) 024 [hep-th/0503217] [INSPIRE].

[41] N. Benjamin, E. Dyer, A.L. Fitzpatrick, A. Maloney and E. Perlmutter, Small Black Holes
and Near-Extremal CFTs, JHEP 08 (2016) 023 [arXiv:1603.08524] [INSPIRE].
[42] R.E. Borcherds, The monster Lie algebra, Adv. Math. 83 (1990) 30.
[43] A. Belin, C.A. Keller and A. Maloney, Permutation Orbifolds in the large N Limit,
arXiv:1509.01256 [INSPIRE].
[44] J. de Boer, Large-N elliptic genus and AdS/CFT correspondence, JHEP 05 (1999) 017
[hep-th/9812240] [INSPIRE].
[45] D. Gaiotto, A. Strominger and X. Yin, From AdS3 /CF T2 to black holes/topological strings,
JHEP 09 (2007) 050 [hep-th/0602046] [INSPIRE].
[46] A. Fujii, R. Kemmoku and S. Mizoguchi, D = 5 simple supergravity on AdS3 × S 2 and N = 4
superconformal field theory, Nucl. Phys. B 574 (2000) 691 [hep-th/9811147] [INSPIRE].
[47] J.M. Maldacena and A. Strominger, AdS3 black holes and a stringy exclusion principle,
JHEP 12 (1998) 005 [hep-th/9804085] [INSPIRE].
[48] J. Gomes, Exact Holography and Black Hole Entropy in N = 8 and N = 4 String Theory,
arXiv:1511.07061 [INSPIRE].
[49] S. Murthy and V. Reys, Single-centered black hole microstate degeneracies from instantons in
supergravity, JHEP 04 (2016) 052 [arXiv:1512.01553] [INSPIRE].
[50] A. Dabholkar, J. Gomes and S. Murthy, Quantum black holes, localization and the topological
string, JHEP 06 (2011) 019 [arXiv:1012.0265] [INSPIRE].
[51] A. Dabholkar, J. Gomes and S. Murthy, Localization & Exact Holography,
JHEP 04 (2013) 062 [arXiv:1111.1161] [INSPIRE].
[52] N. Benjamin, S. Kachru, C.A. Keller and N.M. Paquette, Emergent space-time and the
supersymmetric index, JHEP 05 (2016) 158 [arXiv:1512.00010] [INSPIRE].
[53] J.M. Maldacena, G.W. Moore and A. Strominger, Counting BPS black holes in toroidal Type
II string theory, hep-th/9903163 [INSPIRE].
[54] D. Shih, A. Strominger and X. Yin, Counting dyons in N = 8 string theory,
JHEP 06 (2006) 037 [hep-th/0506151] [INSPIRE].
[55] A. Sen, N = 8 Dyon Partition Function and Walls of Marginal Stability,
JHEP 07 (2008) 118 [arXiv:0803.1014] [INSPIRE].
[56] M.-x. Huang, S. Katz and A. Klemm, Topological String on elliptic CY 3-folds and the ring
of Jacobi forms, JHEP 10 (2015) 125 [arXiv:1501.04891] [INSPIRE].

– 47 –

JHEP04(2017)057

[40] N. Banerjee, D.P. Jatkar and A. Sen, Asymptotic Expansion of the N = 4 Dyon Degeneracy,
JHEP 05 (2009) 121 [arXiv:0810.3472] [INSPIRE].

## PDF page 50

[57] P. Kraus, Lectures on black holes and the AdS3 /CF T2 correspondence, Lect. Notes Phys.
755 (2008) 193 [hep-th/0609074] [INSPIRE].
[58] N. Benjamin, E. Dyer, A.L. Fitzpatrick and S. Kachru, Universal Bounds on Charged States
in 2d CFT and 3d Gravity, JHEP 08 (2016) 041 [arXiv:1603.09745] [INSPIRE].
[59] S. Detournay, T. Hartman and D.M. Hofman, Warped Conformal Field Theory,
Phys. Rev. D 86 (2012) 124018 [arXiv:1210.0539] [INSPIRE].
[60] A. Castro, D.M. Hofman, and G. Sarosi, Warped Weyl fermion partition functions,
JHEP 11 (2015) 129 [arXiv:1508.06302] [INSPIRE].

[62] A. Dabholkar, J. Gomes, S. Murthy and A. Sen, Supersymmetric Index from Black Hole
Entropy, JHEP 04 (2011) 034 [arXiv:1009.3226] [INSPIRE].
[63] S. Ferrara, R. Kallosh and A. Strominger, N = 2 extremal black holes,
Phys. Rev. D 52 (1995) R5412 [hep-th/9508072] [INSPIRE].
[64] H. Ooguri, A. Strominger and C. Vafa, Black hole attractors and the topological string,
Phys. Rev. D 70 (2004) 106007 [hep-th/0405146] [INSPIRE].

– 48 –

JHEP04(2017)057

[61] E. Witten, Three-Dimensional Gravity Revisited, arXiv:0706.3359 [INSPIRE].
