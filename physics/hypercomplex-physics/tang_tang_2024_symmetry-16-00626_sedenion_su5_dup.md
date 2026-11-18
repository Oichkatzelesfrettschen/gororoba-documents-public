Source: https://doi.org/10.3390/sym16050626
PDF sha256: a19e2a0df1a108b6f7bd9fa9e34008cfb77d8b4d91a7c11ccdd8e6fb2692ade8
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of tang_tang_2024_symmetry-16-00626_sedenion_su5_dup.pdf

Transcription of `tang_tang_2024_symmetry-16-00626_sedenion_su5_dup.pdf` in this directory, 12 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-12 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SS symmetry
Article

Sedenion Algebra Model as an Extension of the Standard Model
and Its Link to SU(5)
Qiang Tang 1

and Jau Tang 2, *
1

2

*

School of Artificial Intelligence, Anhui University of Science and Technology, Huainan 232000, China;
tangqiang@whu.edu.cn
Institute of Technological Sciences, Wuhan University, Wuhan 430072, China
Correspondence: jautang@whu.edu.cn

Abstract: In the Standard Model, ad hoc hypotheses assume the existence of three generations of pointlike leptons and quarks, which possess a point-like structure and follow the Dirac equation involving
four anti-commutative matrices. In this work, we consider the sedenion hypercomplex algebra as an
extension of the Standard Model and show its close link to SU(5), which is the underlying symmetry
group for the grand unification theory (GUT). We first consider the direct-product quaternion model
and the eight-element octonion algebra model. We show that neither the associative quaternion
model nor the non-associative octonion model could generate three fermion generations. Instead,
we show that the sedenion model, which contains three octonion sub-algebras, leads naturally to
precisely three fermion generations. Moreover, we demonstrate the use of basis sedenion operators to
construct twenty-four 5 × 5 generalized lambda matrices representing SU(5) generators, in analogy
to the use of octonion basis operators to generate Gell-Mann’s eight 3 × 3 lambda-matrix generators
for SU(3). Thus, we provide a link between the sedenion algebra and Georgi and Glashow’s SU(5)
GUT model that unifies the electroweak and strong interactions for the Standard Model’s elementary
particles, which obey SU(3)⊗SU(2)⊗U(1) symmetry.
Keywords: Dirac equation; Standard Model; SU(5) GUT; sedenion; octonion; quaternion

Citation: Tang, Q.; Tang, J. Sedenion

1. Introduction

Algebra Model as an Extension of the

The Dirac equation is the Standard Model’s cornerstone for describing all fermionic
elementary particles [1–3]. According to the ad hoc assumptions, the three generations of
leptons and quarks are point-like objects without a physical size [4–6]. However, such a
long-held conceptual picture of a point-like particle is inconsistent with observations. For
example, it is unclear why there are precisely three generations of leptons and quarks [7]
and why a point-like muon or tau can be much heavier than an electron [8,9]; and, for the six
types of point-like quarks, why the charm, strange, top and bottom quarks are heavier than
the up and down quarks [10,11]. In Dirac’s theory of a relativistic electron, he coupled four
4 × 4 anti-commutative matrices {α1 , α2 , α3 , β}, equivalently, to the first-order derivatives in space and time to describe the wave [12,13]. Extending the operator techniques
beyond Dirac’s theory, one can include additional operators in higher dimensions to describe a particle’s internal degrees of freedom. In this work, we analyze two types of
higher-dimensional generalizations, using the direct-product operators constructed from
Pauli’s matrices versus hyper-complex operators beyond quaternions [14,15], which is
equivalent to Dirac’s 4 × 4 gamma matrices. Like the four-element quaternion algebra with
three anti-commutative basis operators [16], the eight-element octonion algebra contains
seven operators. Still, unlike the associative quaternion algebra, the octonion algebra is
non-associative [17–20]. In this work, we examine the corresponding multiplication rules
and compare their multiplication tables to clarify the similarities, differences and physical
implications.

Standard Model and Its Link to SU(5).
Symmetry 2024, 16, 626. https://
doi.org/10.3390/sym16050626
Academic Editor: Alexei
Kanel-Belov
Received: 1 November 2023
Revised: 24 November 2023
Accepted: 28 November 2023
Published: 17 May 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/
4.0/).

Symmetry 2024, 16, 626. https://doi.org/10.3390/sym16050626

https://www.mdpi.com/journal/symmetry

## PDF page 2

Symmetry 2024, 16, 626

2 of 12

In Section 2.1, we briefly review Dirac’s original model and its connection to the quaternion algebra. In Section 2.2, we consider a higher-dimensional model beyond Dirac’s four
anti-commutative gamma matrices. We analyze the group of 16 direct-product operators
constructed from quaternions or, equivalently, Pauli’s matrices and an identity operator,
which are related to the 16 Dirac gamma. In Section 2.3, we discuss the non-associative
16-element sedenion algebra [21–26], and show it comprises three distinctive octonion
algebras. We analyze its differences from the direct-product case and examine whether
the corresponding mass–energy relation is consistent with Einstein’s special relativity. In
Section 2.5, we show how proper operator assignment of the operators from three octonion
sub-algebras can naturally lead to the rise of three generations of leptons and quarks.
Finally, in Section 2.6, we present a mapping of octonions to 8 SU(3) generators, and a
mapping of sedenion operators to 24 generators for SU(5), which was proposed by Geogi
and Glashow [27,28] for their GUT model for the grand unification of the Standard Model’s
elementary particles.
2. Theory
In this section, we present a theoretical analysis of an associative algebra model
using Dirac’s gamma matrices, which are related to direct-product operators constructed
from quaternions or, equivalently, Pauli’s matrices and an identity matrix, versus the nonassociative algebra model based on octonion and sedenion operators. This work extends
Dirac’s original theory of the electron to three generations of leptons and quarks. It opens
up the Standard Model beyond the ad hoc assumption of point-like elementary fermions.
We show that sedenion algebra provides a pivotal link to the SU(5) symmetry of GUT. This
hyper-complex operator model with higher degrees of freedom leads precisely to three
generations of leptons/quarks with internal structures.
2.1. Dirac Equation
According to Dirac’s theory of the electron, when using the gamma matrices, one has
)
iγµ ∂µ − m Ψ = 0, µ = 0, 1, 2, 3
( pk = −i∂)k , p0 = i∂0
(
0
σk
I
γk = iσ2 ⊗ σk =
, γ0 = σ3 ⊗ σ0 = 2
−σk 0
0
(

0
− I2

)

(1A)

where the natural unit ℏ = c = 1 is used. Here, we define five 2 × 2 matrices, including
Pauli’s matrices σ1 , σ2 , σ3 , and an identity matrix I2 , as
(
σ1 =

0
1

)
(
1
0
, σ2 =
0
i

)
(
)
(
)
−i
1 0
1 0
, σ3 =
, σ0 = I2 =
,
0
0 −1
0 1

(1B)

Equivalently, using the matrices αk = γ0 γk and β = γ0 , the Dirac equation can also
be expressed as EΨ = ( α · P + βm)Ψ . The identity matrix and three Pauli matrices form
the basis operators for quaternion algebra. Based on Dirac’s first-order differential equation
in spacetime, one obtains Einstein’s relativistic mass–energy relation E2 = m2 + p2 . These
Dirac gamma matrices are used in the Dirac equation. However, the product of these
matrices does not satisfy the closure property; for example, it does not belong to the same
set. Therefore, these five operators do not form a group.
In the Standard Model, the same Dirac equation is used for all leptons and quarks;
assuming these particles are point-like objects with an infinitely small volume, it does not
offer physical explanations for why there are precisely three generations. To generalize
the Dirac equation to higher dimensions, and to account for three fermion generations
by incorporating internal structural dynamics, we consider in the following sections two
modeling approaches, i.e., a direct-product matrix model of 16 associative 4 × 4 matrices
versus the non-associative hype-complex algebra of 16 sedenion basis operators.

## PDF page 3

Symmetry 2024, 16, x FOR PEER REVIEW

3 of 14

Symmetry 2024, 16, 626

3 of 12

modeling approaches, i.e., a direct-product matrix model of 16 associative 4 × 4 matrices
versus the non-associative hype-complex algebra of 16 sedenion basis operators.

2.2. Associative Algebra of 16 Direct-Product Matrices

2.2. Associative Algebra of 16 Direct‐Product Matrices
{I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 , Θ2 , V1 , V2 , V3 , Θ3 , W1 , W2 , W3 }
I , Γ 1 , Γ 2 , Γ 3 , Θ 1 , U 1 , U 2 , U 3 , Θ 2 , V1 , V2 , V3 , Θ 3 , W1 , W2 , W3 

To generalize Dirac’s description of the electron using four Dirac gamma matrices
To generalize Dirac’s description of the electron using four Dirac gamma matrices
γµ (µ = 0, 1, 2, 3), we can define a set of direct-product operators using three Pauli matri   0 , 1, 2 , 3 , we can define a set of direct-product operators using three Pauli matrices
ces and an identity matrix as

and an identity matrix as

σ
ijij ≡ iσi⊗ jσj
Uk = iσ1k , Vk = iσ2k Wk = iσ3k , Γk = iσ0k

Θ = iσ
Uk  i1k , Vk  i 2k Wk  i 3k , Γk  i 0k Θk ki k 0 k0

(2)

(2)

Onecan
canshow
showthat
thathe
theight-element
eight-element
of direct-product
operators
a group
One
set set
of direct-product
operators
formsforms
a group
closure property
property for
for multiplication.
multiplication.Similarly,
Similarly,one
onecan
canshow
showthat
thatthe
theother
othertwo
two sets
with the closure
I, Γ1I,, Γ21, ΓΓ23,,Γ 3
Θ,2 ,Θ 2V, 1V, 1 ,VV2 ,2 ,V
, 1 ,W1
form
a group
{
} a
and {I, ΓΓ11,,ΓΓ22, ,Γ 3Γ,3 ,Θ 3Θ, 3W
form
group
for for
sets
V33} and
W, 2 ,W
W2 ,3 W3
multiplication.These
Thesedirect-product
direct-product
operators
related
to the
sixteen
direct-product
multiplication.
operators
cancan
be be
related
to the
sixteen
direct-product
matricesof
ofquaternions.
quaternions.The
The
multiplication
table
for the
sixteen
direct-product
operators,
matrices
multiplication
table
for the
sixteen
direct-product
operators,
which are
arerelated
relatedtotoDirac’s
Dirac’sgamma
gamma
matrices,
illustrated
Figure
which
matrices,
is is
illustrated
in in
Figure
1. 1.

Figure
color-coded
multiplication
table for 16
direct-product
operators.
Among
the 16 operFigure1.1.The The
color-coded
multiplication
table for
16
direct-product
operators.
Among
ators,16
the 4th,
8th andthe
12th
operators
are 12th
commutative
withare
other
operators, although
most are
antithe
operators,
4th,
8th and
operators
commutative
with other
operators,
alcommutative.
properties diﬀer from those
sedenion algebra.
con- algethough mostThese
are anti-commutative.
Theseofproperties
differ This
from16-element
those ofgroup
sedenion
tains three 8-element sub-groups with closure properties for multiplication, namely,
bra. This 16-element group contains three 8-element sub-groups with closure properties
,
and
I , Γ1 , Γ 2 , Γ 3 , Θ1 , U 1 , U 2 , U 3 
I , Γ1 , Γ 2 , Γ 3 , Θ 2 , V1 , V2 , V3 

for multiplication, namely, {I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 }, {I, Γ1 , Γ2 , Γ3 , Θ2 , V1 , V2 , V3 } and
I , Γ1 , Γ 2 , Γ 3 , Θ 3 , W1 , W2 , W3 . Each domain contains quaternion triplets following cyclic mul{I, Γ1 , Γ2 , Γ3 , Θ3 , W1 , W2 , W3 }. Each domain contains quaternion triplets following cyclic multitiplication
rules.
plication rules.

Here, we summarize their multiplication rules for these sixteen direct-product operHere, we summarize their multiplication rules for these sixteen direct-product
ators:

operators:

Ui U j = −ε ijk Γk − δij I, Vi V j = −ε ijk Γk − δij I, Wi W j = −ε ijk Γk − δij I
Γi Γ j = −ε ijk Γk − δij I, Θi Θ j = −ε ijk Θk − δij I
Ui V j = −iε ijk Wk − δij Θ3 ,
V j Ui = −iε ijk Wk + δij Θ3
Vi W j = − iε ijk Uk + δij Θ1 ,
W j Vi = −iε ijk Uk + δij Θ1 ,
Wi U j = −iε ijk Vk + δij Θ2

(3A)

## PDF page 4

Symmetry 2024, 16, 626

4 of 12

and

and

Ui Γ j = −σ1i σ0j = −iε ijk σ1k − δij σ10 = − ε ijk Uk + iδij Θ1
Γ j Ui = −σ0j σ1i = iε ijk σ1k − δij σ10 = ε ijk Uk + iδij Θ1
Vi Γ j = −ε ijk Vk + iδij Θ2
Γ j Vi = ε ijk Vk + iδij Θ2
Wi Γ j = −ε ijk Wk + iδij Θ3
Γ j Wi = ε ijk Wk + iδij Θ3

(3B)

Γi Γ j = − ε ijk Γk − δij I, Θi Θ j = −ε ijk Θk − δij I
Θ 1 Γ k = Γ k Θ 1 = i Uk , Θ 2 Γ k = Γ k Θ 2 = i Vk , Θ 3 Γ k = Γ k Θ 3 = i Wk
Uk Θ1 = Θ1 Uk = iΓk , Vk Θ2 = Θ2 Vk = iΓk , Wk Θ3 = Θ3 Wk = iΓk
Uk Θ 2 = − Θ 2 Uk = −Wk , Uk Θ 3 = − Θ 3 Uk = Vk
Vk Θ 1 = − Θ 1 Vk = Wk , Vk Θ 3 = − Θ 3 Vk = −Uk
Wk Θ 1 = − Θ 1 Wk − Vk , Wk Θ 2 = − Θ 2 Wk = Uk .

(3C)

This 16-element group contains three 8-element subgroups, namely, {I, Γ1 , Γ2 , Γ3 , Θ1 ,
U1 , U2 , U3 }, {I, Γ1 , Γ2 , Γ3 , Θ2 , V1 , V2 , V3 } and {I, Γ1 , Γ2 , Γ3 , Θ3 , W1 , W2 , W3 }.
These three subgroups with eight elements of 4 × 4 matrices satisfy the closure and
associative properties. They differ from the non-associative octonion algebra, which will be
discussed in detail later in Section 2.3.
Here, we examine the mass–energy relation based on the operators according to
the first sub-group {I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 }. We propose to extend Dirac’s equation involving four gamma matrices to higher dimensions involving eight direct-product
operators as
3

3

k =1

k =1

m0 = iEΘ1 + ∑ Pk Γk + ∑ Qk Uk

(4A)

By taking the square of both sides of the equation, one obtains
3
3
3
3
{
}
{
}
m0 2 = E2 + ∑ Pk 2 Γk 2 + ∑ Qk 2 Uk 2 + ∑ Pi Pj Γi , Γ j + ∑ Qi Q j Ui , U j
k =1

3

i,̸= j=1

k =1
3

i,̸= j=1

(4B)

+ ∑ Pi Q j Ui , Γ j + iE ∑ ( Pk {Θ1 , Γk } + Qk {Θ1 , Uk })
{

}

i,j=1

k =1

or, equivalently, according to the multiplication rules in Figure 1, one has
)
3 (
3
3
E2 = m0 2 + ∑ Pk 2 + Qk 2 − iΘ1 ∑ Pk Qk − iE ∑ ( Pk Uk + Qk Γk ) .
k =1

k =1

(4C)

k =1

Similarly, for the second assignment, one has
3

3

m0 = iEΘ2 + ∑ Pk Γk + ∑ Qk Vk
k =1
k =1
)
3 (
3
3
2
2
2
2
E = m0 + ∑ Pk + Qk − iΘ2 ∑ Pk Qk − iE ∑ ( Pk Vk + Qk Γk )
k =1

k =1

(4D)

k =1

and for {I, Γ1 , Γ2 , Γ3 , Θ3 , W1 , W2 , W3 }, one obtains
3

3

m0 = iEΘ3 + ∑ Pk Γk , + ∑ Qk Wk
k =1
k =1
)
3 (
3
3
2
2
2
E = m0 + ∑ Pk + Qk 2 − iΘ3 ∑ Pk Qk − iE ∑ ( Pk Wk + Qk Γk ).
k =1

k =1

(4E)

k =1

In Equation (4A,D,E), the last two terms of the equations involve operators Wk , which
lead to mass–energy oscillations in time for a lepton and quark. Therefore, such results
are neither consistent with experimental observations nor in agreement with Einstein’s

## PDF page 5

Symmetry 2024, 16, 626

5 of 12

mass–energy relation, which contains additional kinetic energy ∑k Qk 2 due to a particle’s
internal structural dynamics. Therefore, although the 16-element group of direct-product
operators has three 8-element subgroups, the above direct-product model cannot represent
three generations of leptons and quarks. In the following sections, we will discuss the
non-associative sedenion and octonion algebras, and show that they do not encounter these
problems faced by the associative direct-product operator model.
2.3. Non-Associative Octonion Algebra and a Single Fermion Generation
We consider the octonion algebra to avoid the problems faced by the direct-product
matrix model. Any element x and its conjugate x in the octonion algebra can be expressed
in terms of the identity operator e0 and seven other octonion unit operators
7

x = x0 e0 + X,

x = x0 e0 − X,

X = ∑ x k ek ,

(5)

k =1

{
}
where ek satisfies the anti-commutative relation ei , e j = 0, i ̸= j for a different pair of
Symmetry 2024, 16, x FOR PEER REVIEW
6 of rules
14
indices. These non-associative octonion operators follow the specific multiplication
in
Figure 2.

Figure2.2.The
The
color-coded
multiplication
table
thebasis
eight
basis octonions.
According
Figure
color-coded
multiplication
table for
thefor
eight
octonions.
According to the
multi-to the
plication
rules, other
thethan
identity
operator,operator,
all seven operators
anti-commute
with each other;
multiplication
rules,than
other
the identity
all seven operators
anti-commute
with each
however,
the multiplications
are not associative.
The arrays areThe
color-coded
to illustrate
domains
of
other; however,
the multiplications
are not associative.
arrays are
color-coded
to illustrate
cyclic multiplication rules for quaternions. Each color-coded field of quaternion triplets follows cydomains of cyclic multiplication rules for quaternions. Each color-coded field of quaternion triplets
clic multiplication rules.
follows cyclic multiplication rules.

For the octonion algebra of Figure 2, the fourth element anti-commutes with all other
For the octonion algebra of Figure 2, the fourth element anti-commutes with all
operators except the identity operator. However, in Figure 1, for the direct-product operother
operators except the identity operator. However, in Figure 1, for the direct-product
ators, the fourth element a 4 , a 8 or a12 is commutative with all other operators, except
operators, the fourth element a4 , a8 or a12 is commutative with all other operators, except the
the identity element. This property is essential for the corresponding mass–energy relaidentity element. This property is essential for the corresponding mass–energy relation to
tion to be consistent with Einstein’s relativity. Therefore, the model with seven non-assobe consistent with Einstein’s relativity. Therefore, the model with seven non-associative but
ciative but anti-commutative octonion operators is the correct model to describe a single
anti-commutative
octonion
operators
is the correct
describe
single generation
of
model model
invokestothree
extraadegrees
of freegeneration
of leptons
or quarks.
The octonion
leptons
or
quarks.
The
octonion
model
invokes
three
extra
degrees
of
freedom
to
represent
dom to represent the internal structural dynamics of a fermion as three momentum comthe internal
structural
of a fermion
three momentum
components
ponents
concerning
thedynamics
center-of-mass
referenceasframe.
In contrast, the
other threeconcerning
antithe
center-of-mass
reference
frame.
In
contrast,
the
other
three
anti-commutative
operators
commutative operators define the external degrees of freedom as three momentum operdefine
the
external
degrees
of
freedom
as
three
momentum
operators
for
the
particle
ators for the particle concerning the laboratory frame.

concerning the laboratory frame.
2.4. Three Octonion Sub‐Algebras in Sedenion Algebra and Three Generations of Charged/Neu‐
2.4. Leptons
Three Octonion Sub-Algebras in Sedenion Algebra and Three Generations of
tral

Charged/Neutral Leptons

In the previous section, we explained that the octonion algebra leads to only one ferthe previous
section, we three
explained
that the
octonion
to only one
mionIn
generation.
To accommodate
generations,
one
needs toalgebra
considerleads
a higher-difermion generation.
To accommodate
three
one needs
to consider
a highermensional
hypercomplex
algebra, namely,
thegenerations,
sedenion algebra.
The sedenion
algebra
consists of 16 basis sedenion operators e k , k  0,1, 2, ..., 15 , denoted sequentially.
The multiplication rules for 16 sedenion basis operators are given in Figure 3 and are
diﬀerent from the table for the direct-product operator model shown earlier in Figure 1.

## PDF page 6

Symmetry 2024, 16, 626

6 of 12

dimensional hypercomplex algebra, namely, the sedenion algebra. The sedenion algebra
consists of 16 basis sedenion operators {ek , k = 0, 1, 2, . . . , 15} , denoted sequentially.
Symmetry 2024, 16, x FOR PEER REVIEW The multiplication rules for 16 sedenion basis operators are given in Figure
7 of 14 3 and are
Symmetry 2024, 16, x FOR PEER REVIEW
7 of
different from the table for the direct-product operator model shown earlier
in14Figure 1.

Figure
The color-coded
multiplication table for
16 basis sedenion
operators
k  0,1, 2,
..., 15 operators
Figure3. 3.
The color-coded
multiplication
table for
16 e k ,
basis
sedenion
Figure
The1, 2,
color-coded
multiplication
table for
16 basis
sedenion
operators 
 octonion
ek , k  0
,1, 2
, of
..., 15by
.{ek
The
region
algebra
contains
threeregion
distinct
types
of the
octonion
sub-algebras,
denoted
, k 3.
=
0,
.
. . , 15
The
algebra
contains
three
distinct
types
the
}.
,, Γ , Θ
and
, Γ1
, Γ2
, Γ 3 algebra
, Θ1
, U 1contains
, U 2by
, U 3{I,
, Γ,1the
,UΓ 2, , U
Γ3
,}Θ
,V
,, V
, VΓ3 , Θ ,
.IThe
region
three
distinct
types,IU
of
octonion
sub-algebras,
denoted
by, V } and
2
1
2
sub-algebras,
denoted
,
Γ1 , Γ
I,
Γ
Γ
,
V
,
V
{
2
3
2
3
2
3
2
2
3
1
1
1
1
and
U11,, W
U2 , U
Γ1 , Γ 2 , Γ
color-coded I ,
domain
contains
quaternion
triplets following
I , ΓΓ11,,ΓΓ22,,ΓΓ33, ,ΘΘ31, ,W
W33. Each ,
3, Θ2 , V
1 , V2 , V3 

{I, Γ1 , Γ2 , Γ3 , Θ3 , W1 , W2 , W3 }. Each color-coded domain contains quaternion triplets following
Each
color-coded
domain
quaternion
triplets following
I
, Γ ,Γ2,Γ
, W2 ,
W3 .the
cyclic
multiplication
rules.
Unlike
table in
Figure 1 for
thecontains
associative
direct-product
matrices,
3, Θ3, W
1rules.
cyclic1 multiplication
Unlike the table in Figure 1 for the associative direct-product matrices, the
the
4th, 8th
and 12th
operators
non-associative
sedenion
algebra
anti-commute
with
cyclic
multiplication
rules.
Unlike in
the the
table in Figure
1 for the
associative
direct-product
matrices,
4th,
8th
12th operators in the non-associative sedenion algebra anti-commute with U, V, W
operators.
U
, Wand
the, V
4th,
8th
and 12th operators in the non-associative sedenion algebra anti-commute with
operators.
U , V , W operators.

As can be seen from Figure 3, the sedenion algebra contains three distinct types of
As
canbe
beseen
seen
fromFigure
Figure3,3,are
thesedenion
sedenion
algebra
three
distinct
types
of the octhe As
octonion
algebra,
which
denoted
by
can
from
the
algebra
contains
three
distinct
types
I,contains
Γ
, Θ1 , U
1, Γ2 , Γ3
1, U 2 , U
3  of,
tonion
algebra,
which
are
denoted
by
I,
Γ
,
Γ
,
Γ
,
Θ
,
U
,
U
,
U
,
I,
Γ
,
Γ
,
{
}
{
2
3
2
3
2
1
1
1
1
,
the
octonion
algebra,
which
are
denoted
by
U 2 , U 3 ta- Γ3 , Θ2 ,
The
multiplication
I , Γ1 , Γ 2 , Γ 3 , Θ 2 , V1 , V2 , V3  and I, Γ1 , Γ 2 , Γ 3 , Θ 3 , W1 , 
WI ,2 ,Γ1
W,3Γ2. , Γ
3 , Θ1 , U 1 ,
V
,
V
,
V
and
I,
Γ
,
Γ
,
Γ
,
Θ
,
W
,
W
,
W
.
The
multiplication
tables
}
{
}
2
3
2
3
3
2
3
1
1
1
andof I , Γ
TheFigure 4.
multiplication
ta- for these
I
, Γ1
, Γ2 ,
Γ3, Θ
Θ3, W
W3  . in
bles
for
these
three
distinct
types
octonion
algebra
are
illustrated
2 , V1 , V
2 , V3 
1, Γ 2 , Γ3,
1 , W2 ,
three
distinct
types
of
octonion
algebra
are
illustrated
in
Figure
4.
bles for these hree distinct types of octonion algebra are illustrated in Figure 4.







Figure 4. (A) The multiplication rules for the octonions I, Γ1, Γ2, , Γ3,Θ1. U1, U2 , U3 . (B)
Figure 4. (A) The multiplication rules for the octonions I, Γ , Γ , Γ , Θ , U , U , U }. (B)
The multipliFigure 4. (A) The multiplication rules for the octonions { I, 1Γ1, 2Γ2,3, Γ31,Θ1.1U1,2U2 ,3U
3 . (B)
, 2Γ, 2,V,3Γ}.3,(C)
Θ2,The
V1, V2
, V3of {.I, Γ(C)
The
cationmultiplication
table of {I, Γ1 ,table
Γ2 , Γ3of
, Θ2 , I
V,1Γ
, 1V
table
, Γ3 , table
Θ3 , Wof
1 , Γ2The
1 , W2 , W3 }.
I, Γ1, Γ2
, V1, V2
, V3multiplication
. (C) Therules.
table of
The
multiplicationdomain
table of of
, , Γ3,Θ2
Each color-coded
quaternion
triplets
follows
cyclic







## PDF page 7

Symmetry 2024, 16, 626

7 of 12

We examine here the mass–energy relation according to the octonion algebra of
{I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 } that represents the basis octonion operators {e0 , e1 , e2 , e3 ,
e5 , e6 , e7 , e8 } sequentially. We can generalize Dirac’s equation and utilize
1)

3

m0 I = iEΘ1 + ∑ Pk Γk +
3

k =1

3

∑ A k Uk

k =1
3

3

3

iE I = −m0 Θ1 + ∑ Pk Θ1 Γk , + ∑ Ak Θ1 Uk = −m0 Θ1 − ∑ Pk Uk + ∑ Ak Γk
k =1
k =1
k =1
k =1
(
)2
3
3
− E2 = −m0 Θ1 + ∑ Ak Γk − ∑ Pk Uk ,

k =1
k =1
3
2 2
2
2
= m0 Θ1 + ∑ Ak Γk + Pk 2 Uk 2
k =1
3
3
3
{
}
{
}
+ ∑ Ai A j Γi , Γ j + ∑ Pi Pj Ui , U j − m0 P{Θ1 , Γk } + m0 ∑ Pk {Θ1 , Uk }
3
i,̸= j
k =1
∑ Pi

(6A)

i,̸= j

3

3

m0,e f f 2 = m0 2 + ∑ Ak 2 .

E2 = m0,e f f 2 + ∑ Pk 2 ,
k =1

k =1

The above result is consistent with Einstein’s mass–energy relation, indicating that the
octonion model gives rise to a single generation of fermions with an internal structural dynamic. Similarly, for {I, Γ1 , Γ2 , Γ3 , Θ2 , V1 , V2 , V3 } and {I, Γ1 , Γ2 , Γ3 , Θ3 , W1 , W2 , W3 },
one can obtain
2)

3

E2 = m

0,e f f

2+

3

k =1
2

∑ Pk ,

k =1

and
3)

3

m0 I = iEΘ2 + ∑ Pk Γk +

∑ Bk Vk

k =1
3
2
m0,e f f = m0 2 + ∑ Bk 2 ,
k =1

3

3

k =1

k =1

(6B)

m0 I = iEΘ1 + ∑ Pk Γk + ∑ Ck Wk

E2 = m

0,e f f

2+

3

2

∑ Pk ,

k =1

3

(6C)

m0,e f f 2 = m0 2 + ∑ Ck 2 .
k =1

The three above equations reproduce Einstein’s mass–energy relation, e.g.,
E2 = m0,e f f 2 + ∑k Pk 2 , m0,e f f 2 ≡ m0 2 + ∑k Qk 2 , Qk = Ak , Bk , Ck for a particle with
an effective rest mass m0,e f f , which contains the kinetic energy of its internal structural
dynamics. Equation (6A–C) can represent three generations of charged leptons, namely
the electron, the muon and the tau. For three generations of neutral leptons, i.e., the
corresponding neutrino for each generation of leptons, we use the following assignments:
1)

3

3

m0 I = iE iΘ1 + ∑ Pk Γk + ∑ Ak (Vk + iWk )
3

k =1

3

k =1

iE I = −m0 Θ1 + ∑ Pk Uk + ∑ Ak (Wk − iVk )

k =1
k =1
3
2
2
2
2
2
− E = m0 Θ1 + Pk Uk + ∑ Ak 2 (Wk − iVk )2
k =1
3
3
{
}
− m0 ∑ Ak {Θ1 , Wk − iVk } + ∑ Pi Ui , W j − iV j
i,j=1
k =1
3
E2 = m0 2 + ∑ Pk 2
k =1

(7A)

## PDF page 8

Symmetry 2024, 16, 626

8 of 12

2)

3

3

m0 I = iE iΘ2 + ∑ Pk Γk + ∑ Bk (Wk + iUk )
3

k =1

3

k =1

iE I = −m0 Θ2 + ∑ Pk Vk + ∑ Bk (Uk − iWk )
3

(7B)

k =1

k =1

E2 = m0 2 + ∑ Pk 2
k =1

3)

3

3

m0 I = iE Θ3 + ∑ Pk Γk + ∑ Ck (Uk + iVk )
k =1

3

3

k =1

iE I = −m0 Θ3 + ∑ Pk Wk + ∑ Ck (Vk − iUk )
k =1

3

(7C)

k =1

E2 = m0 2 + ∑ Pk 2 .
k =1

Owing to the absence of ∑k Qk 2 in the above results for three neutrino generations,
one has a vanishingly small rest mass E2 ≈ ∑k Pk 2 if m0 is close to zero. Unlike the
cases for the charged leptons, one has E2 = m0,e f f 2 + ∑k Pk 2 , where m0,e f f 2 = m0 2 +
∑k Qk 2 ≈∑k Qk 2 , even if m0 is close to zero. According to the above sedenion model, their
masses could be close to zero and are much smaller than those of their corresponding
leptons. The experimental observations of flavor mixing and the mass oscillations among
three generations of neutrinos are believed to be induced by the symmetry-breaking
mechanism of the sedenion algebra. It will be shown later in Section 2.6 that the sedenion
algebra can be linked to SU(5). The symmetry breaking of SU(5) into SU(3)⊗SU(2)⊗U(1)
might be caused by the flavor mixing and mass oscillations of neutrinos.
2.5. Sedenion Algebra and Three Generations of Quarks
Here, we propose the following assignments of the sedenion operators for three quark
generations:
3

3

1) m0 I = iE iΘ1 + ∑ Pk Γk + ∑ ( Bk Vk + Ck Wk )
3

k =1

3

k =1

iE I = −m0 Θ1 + ∑ Pk Uk + ∑ ( Bk Wk − Ck Vk )
k =1
k =1
)
3 (
3
2
2
2
E = m0,e f f + ∑ Pk , m0,e f f 2 = m0 2 + ∑ Bk 2 + Ck 2

(8A)

k =1

k =1

3

3

2) m0 I = iE iΘ2 + ∑ Pk Γk + ∑ (Ck Wk + Ak Uk )
3

k =1

3

k =1

iE I = −m0 Θ2 + ∑ Pk Uk + ∑ (Ck Uk − Ak Wk )
k =1
k =1
)
3
3 (
E2 = m0,e f f 2 + ∑ Pk 2 , m0,e f f 2 = m0 2 + ∑ Ak 2 + Ck 2
k =1

(8B)

k =1

3

3

3) im0 I = iE iΘ3 + ∑ Pk Γk + ∑ ( Ak Uk + Bk Vk )
3

k =1

3

k =1

iE I = −m0 Θ3 + ∑ Pk Uk + ∑ (− Ak Vk + Bk Uk )
k =1
k =1
)
3
3 (
2
2
2
E = m0,e f f + ∑ Pk , m0,e f f 2 = m0 2 + ∑ Ak 2 + Bk 2 .
k =1

k =1

(8C)

## PDF page 9

Symmetry 2024, 16, 626

9 of 12

One could also make different assignments to the generalized energy and momentum
operators for the other three heavier quark generations.
3

3

1) m0 I = iEΘ1 + ∑ Pk Γk + ∑ ( Ak Uk + Bk Vk + Bk Wk )
3

k =1

3

k =1

iEI = im0 Θ1 + ∑ Pk Uk + ∑ ( Ak Γk + Bk Wk − Bk Vk )
k =1
k =1
)
3
3 (
2
2
2
E = m0,e f f + ∑ Pk , m0,e f f 2 = m0 2 + ∑ Ak 2 + 2Bk 2 ,
k =1

k =1

3

3

2) m0 I = iEΘ2 + ∑ Pk Γk + ∑ (Ck Uk + Bk Vk + Ak Wk )
k =1
k =1
)
3
3 (
2
E2 = m0,e f f 2 + ∑ Pk ,
m0,e f f 2 = m0 2 + ∑ Bk 2 + 2Ck 2 ,
k =1

(9B)

k =1

3

3

3) m0 I = iEΘ3 + ∑ Pk Γk + ∑ ( Ak Uk + Ak Vk + Ck Wk )
k =1
k =1
)
3
3 (
2
2
2
E = m0,e f f + ∑ Pk ,
m0,e f f 2 = m0 2 + ∑ Ck 2 + 2Ak 2 .
k =1

(9A)

(9C)

k =1

According to the above operator assignments, there are six possible types of assignments for the quarks, namely, the assignments in Equation (8A–C) could be related to the
lighter three-member family of the up, charm and top quarks, while the assignments in
Equation (9A–C) could be linked to the heavier three-member family of the bottom, strange
and bottom quarks. Thus, the sedenion algebra is shown to lead naturally to six types of
quarks of the Standard Model.
2.6. Mapping Octonions to SU(3) Generators and Sedenion to SU(5) Generators
In this section, we discuss the mapping of the octonion operators to 8 SU(3)’s generators and the mapping of sedenion operators to 24 SU(5) generators. Each type of octonion
operator can be shown to be related to Clifford algebra C ↕(6) [20]. Here, we define three
pairs of fermion creation and annihilation operators, which satisfy the anti-commutation
relations as
α1 = (−e6 +
ie5 )/2, α2 = (−
{e3 + ie1})/2, α3 = (−e7 + ie2 )/2
{
} { + +}
αi , α j = αi , α j = 0 ,
αi , α +
= δij
j

(10A)

For the first lepton/quark generation, these eight basis octonion operators are denoted
by {I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 }
α1 = (−U2 + iU1 )/2, α2 = (−Γ3 + iΓ1 )/2, α3 = (−U3 + iΓ2 )/2
α1+ = (U2 + iU1 )/2, α2+ = (Γ3 + iΓ1 )/2, α3+ = (U3 + iΓ2 )/2.

(10B)

One can define a tensor product |i ⟩⟨ j| ≡ αi + α j to construct the following eight SU(3)
generators, which are related to Gell-Mann’s lambda matrices Λk as
Λ1 = |2⟩⟨1| + |1⟩⟨2| = i (U3 − U2 )/2
Λ2 = −i |1⟩⟨2| + i |2⟩⟨1| = −i (U1 − Θ1 )/2
Λ3 = |1⟩⟨1| − |2⟩⟨2| = i (Γ3 − Γ2 )/2
Λ4 = |1⟩⟨3| + |3⟩⟨1| = i (Θ1 − Γ2 )/2
Λ5 = −i |1⟩⟨3| + i |3⟩⟨1| = −i (Γ1 + U3 )/2
Λ6 = |2⟩⟨3| + |3⟩⟨2| = −i (Γ1 + U2 )/4
Λ7 = −i |2⟩⟨3| + i |3⟩⟨2| = −i (Θ1 √
− Γ3 )/2
Λ8 = (|1⟩⟨1| + |2⟩⟨2| − 2|3⟩⟨3|)/ 3 = i (Γ3 + Γ2 − 2U2 )/2.

(10C)

## PDF page 10

Symmetry 2024, 16, 626

10 of 12

We have shown above that the eight lambda matrices, as the SU(3) generators, can be
constructed by {I, Γ1 , Γ2 , Γ3 , Θ1 , U1 , U2 , U3 } because the sedenion algebra consists of
three octonion sub-algebras, similar to other octonion basis sets, e.g., {I, Γ1 , Γ2 , Γ3 , Θ2 , V1 ,
V2 , V3 } to make two other lambda-matrix generators. Together with the U-type, V-type
and W-type octonion algebras, which are the three distinct sub-algebras of the sedenion
algebra, we can build altogether 24 generators for SU(5).
In Equation (10) we use octonion basis operators for the construction of three pairs
of creation and annihilation operators which could be employed to construct eight 3 × 3
lambda matrix generators for the SU(3) symmetry group. Here, by extending the use of
three pairs of creation and annihilation operators for the octonion algebra, we can now
define five pairs of fermion creation and annihilation operators as
α1 = (−e6 + ie5 )/2, α2 = (−e3 + ie1 )/2, α3 = (−e7 + ie2 )/2
α4 = (−e14 {
+ ie13 )/2,
} α5 ={(−e11 +}ie9 )/2
{
}
+
+
αi , α j = αi , α j = 0,
αi , α +
= δij ,
j

(11A)

or, equivalently,
α1 = (−U2 + iU1 )/2, α2 = (−Γ3 + iΓ1 )/2, α3 = (−U3 + iΓ2 )/2
α4 = (−V2 + iV1 )/2,
α5 = (−W2 + iW1 )/2.

(11B)

Similar to the construction of eight 3 × 3 lambda matrices in Equation (10C) for the
SU(3) generators from three pairs of creation and annihilation operators, from five pairs of
fermionic creation and annihilation operators, we could construct a total of twenty-four
generalized lambda matrices as the SU(5) generators. Put simply, there are eight 3 × 3
matrix generators in SU(3). The number eight equates to the square of three minus one
by excluding an identity matrix, whereas in SU(5), there are twenty-four 5 × 5 matrix
generators, which equal the square of five minus one by excluding an identity matrix.
Similar to the automorphic relationship between the octonion algebra and SU(3), in this
work, we establish the relationship between the sedenion algebra and SU(5). We have
shown in Equation (10C) the explicit assignments of the SU(3) generators from pairs of the
octonion basis operators. Similar pair assignments of sedenion operators to the twenty-four
lambda generators for SU(5) are quite lengthy but straightforward, and will not be given
here. Using the five pairs of fermionic creation and annihilation operators, one can construct
ten pairs of 5 × 5 SU(5) generator matrices as |m⟩⟨n| + |n⟩⟨m|,
− i |m⟩⟨n| + i |n⟩⟨m|,
for m ̸= n = 1, 2, . . . , 5. With the same indices, one can make four diagonal but orthogonal
5 × 5 matrices. Therefore, among these twenty-four SU(5) generators represented by
5 × 5 generalized lambda matrices, there are four diagonal matrices and twenty offdiagonal matrices. The SU(5) symmetry plays an essential role in the GUT (grand unification
theory) [27,28], which has been advocated to unify the electromagnetic, weak and strong
interactions of elementary particles. These three types of the eight-element octonion
algebra are not independent of each other because they contain the same quaternion
algebra {I, Γ1 , Γ2 , Γ3 }. The cooling of the universe after the Big Bang plays a vital role
in the symmetry breaking of SU(5) to become SU(3)⊗SU(2)⊗U(1), and in the breakdown
of the sedenion algebra into a direct product of octonion and quaternion algebras. Such a
breakdown results in the flavor mixing of neutrinos and their mass oscillations.
Similar to the construction of eight of 3 × 3 lambda matrices in Equation (10C), for
the SU(3) generators from three pairs of creation and annihilation operators, from pairs
of five fermionic creation and annihilation operators, one can build a total of twenty-four
generalized lambda matrices as the SU(5) generators. Using the five pairs of the fermionic
creation and annihilation operators, one can construct ten pairs of 5 × 5 off-diagonal SU(5)
generator matrices as |m⟩⟨n| + |n⟩⟨m|, −i |m⟩⟨n| + i |n⟩⟨m|, for m ̸= n = 1, 2, . . . , 5. With
the same indices, one can build four off-diagonal but orthogonal 5 × 5 matrices. Therefore,
among these twenty-four SU(5) generators represented by 5 × 5 generalized lambda
matrices, there are four diagonal matrices and twenty off-diagonal matrices. The SU(5)

## PDF page 11

Symmetry 2024, 16, 626

11 of 12

symmetry plays an essential role in the GUT (grand unification theory) [27,28] and it has
been advocated to unify the electromagnetic, weak and strong interactions of elementary
particles. These three types of the eight-element octonion algebra are not independent of
each other because they contain the exact quaternion algebra {I, Γ1 , Γ2 , Γ3 }.
3. Conclusions
In this work, we have presented a theoretical analysis of higher-dimensional models
beyond the conventional Dirac equation, which was proposed for a point-like fermion.
Dirac utilized four anti-commutative matrices for the first derivatives of a particle’s space
and time coordinates. The extension to higher-dimensional models is necessary because
the traditional Dirac theory cannot explain the origin of the observed three generations of
leptons and quarks in the Standard Model. In this study, we first consider a 16-element
group of 4 × 4 matrices as direct products of quaternion operators, i.e., three 2 × 2 Pauli
matrices and an identity matrix. This model contains three extra degrees of freedom to
incorporate a particle’s internal structure. This 16-element group has three 8-element subgroups, possessing a closure property for multiplications among 8 elements of each subset.
However, this direct-product matrix model with associative operators could not reproduce
Einstein’s mass–energy relation, unlike the model with 16 sedenion basis operators. The
significant difference between the two models is whether the operator multiplication is
associative or not, as illustrated by the differences in the multiplication tables of Figures 1
and 2. The 8-element octonion algebra is shown to be able to lead to a single lepton generation. However, we need a 16-element sedenion algebra to encompass precisely three
generations of leptons and quarks. We have shown from the color-coded table arrays in
Figure 2 that the sedenion algebra contains three distinct octonion algebras, with the U-,
V- and W-type operators, each type of octonion sub-algebra corresponding to a single
generation. We have also shown that in Equation (7A–C), the effective neutrinos’ rest mass
could be vanishingly small in comparison to that in Equation (6A–C) for the counterpart
charged leptons. We have also provided operator assignments in Equations (8A–C) and
(9A–C) to represent three generations of lighter and heavier quarks. Moreover, we have
shown that by adequately pairing up the octonion basis operators, one can construct eight
3 × 3 Gell-Mann lambda matrices as the eight generators for SU(3). For the U-, V- and
W-type octonion sub-algebra of the sedenion algebra, we could pair up the sedenion basis
operators to construct a total of twenty-four 5 × 5 matrices to represent the 24 generators
of SU(5). These three types of the eight-element octonion algebra contain the same quaternions {I, Γ1 , Γ2 , Γ3 }. It is commonly believed that soon after the Big Bang of the universe,
the almost instant cooling process played an important role in the symmetry breaking for
SU(5) to become SU(3)⊗SU(2)⊗U(1) of the present Standard Model situation, and breaking
down sedenion algebra into the direct-product algebra of octonions and quaternions results
in neutrinos’ flavor mixing and mass-oscillation behavior. The main purpose of this work
is to point out the interesting relationship between sedenion algebra and SU(5). Although,
in Section 2.4, we explain qualitatively why neutrinos have vanishingly small rest masses
as compared to those of their counterpart charged leptons, we do not intend to solve all the
puzzles faced by the Standard Model such as neutrinos’ mass oscillations. More studies are
needed to address such an issue, which might involve combining this sedenion model for
SU(5) with the Higgs symmetry-breaking mechanism [29]. Such a challenging task is not
the primary interest of this work. The phenomenon of flavor mixing and oscillations among
neutrinos is an interesting and important issue. However, it is beyond the scope of this
work, and it awaits further investigation from other experts in this field of particle physics.
Through this work, by linking the sedenion algebra to SU(5) of GUT, which can be reduced
to SU(3)⊗SU(2)⊗U(1), we hope to offer a potential avenue toward the development of an
improved theory beyond the Standard Model.
Author Contributions: Conceptualization, J.T.; methodology, J.T.; software, Q.T.; validation, J.T.;
formal analysis, J.T.; investigation, J.T.; re-sources, J.T.; data curation, Q.T.; writing—original draft
preparation, J.T.; writing—review and editing, J.T. and Q.T.; visualization, Q.T.; supervision, J.T.;

## PDF page 12

Symmetry 2024, 16, 626

12 of 12

project administration, J.T.; funding acquisition, Q.T. All authors have read and agreed to the published version of the manuscript.
Funding: This research was funded by the Scientific Research Foundation for High-level Talents of
Anhui University of Science and Technology (grant number 2022yjrc67) and National Natural Science
Foundation of China Grant No. 11974264. And The APC was funded by [2022yjrc67].
Data Availability Statement: No new data were created or analyzed in this study.
Conflicts of Interest: The authors declare no conflict of interest.

References
1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.

Finster, F.; Jokel, M. Causal Fermion Systems: An Elementary Introduction to Physical Ideas and Mathematical Concepts; Springer:
Berlin/Heidelberg, Germany, 2020.
Hwang, J.-K. New fermionic dark matters, extended Standard Model and cosmic rays. Mod. Phys. Lett. A 2017, 32, 1730023.
[CrossRef]
Donoghue, J.F.; Golowich, E.; Holstein, B.R. Dynamics of the Standard Model; Cambridge University Press: Cambridge, UK, 2014.
Fryberger, D. A model for the structure of point-like fermions: Qualitative features and physical description. Found. Phys. 1983,
13, 1059–1100. [CrossRef]
Arkani-Hamed, N.; Schmaltz, M. Hierarchies without symmetries from extra dimensions. Phys. Rev. D 2000, 61, 033005.
[CrossRef]
Burch, U.; Lin, C.-H.; Rubbia, A.; Sakharov, A.S.; Ulbricht, J.; Wu, J.; Zhao, J. Test of Non-Point-Like Behavior of Fermions; American
Institute of Physics: College Park, MD, USA, 2017.
Furey, C. Three generations, two unbroken gauge symmetries, and one eight-dimensional algebra. Phys. Lett. B 2018, 785, 84–89.
[CrossRef]
Frampton, P.H.; Hung, P.Q.; Sher, M. Quarks and leptons beyond the third generation. Phys. Rep. 2000, 330, 263–348. [CrossRef]
Hertzog, D.W. Muons: Particles of the moment. Phys. World 2004, 17, 29. [CrossRef]
Lincoln, D. The Inner Life of Qurks. Sci. Am. 2012, 307, 36–43. [CrossRef] [PubMed]
Close, F.; Maddox, J. Getting to the bottom of the top. Nature 1994, 368, 805. [CrossRef]
Thaller, B. The Dirac Equation; Springer Science & Business Media: Berlin/Heidelberg, Germany, 2013.
Joyce, W.P. Dirac theory in spacetime algebra: I. The generalised bivector Dirac equation. J. Phys. A Math. Gen. 2001, 34, 1991.
[CrossRef]
Wang, C.; Li, Z.; Agarwal, R.P. A new quaternion hyper-complex space with hyper argument and essential functions via
quaternion dynamic equations. J. Geom. Anal. 2022, 32, 67. [CrossRef]
Defranceschi, M.; Le Bris, C. Quaternion Symmetry of the Dirac Equation. In Mathematical Models and Methods for Ab Initio
Quantum Chemistry; Springer Science and Business Media LLC: Dordrecht, The Netherlands, 2000; pp. 227–246.
Jakubczyk, D.; Jakubczyk, P. On the SU(2) × SU(2) symmetry in the Hubbard model. Open Phys. 2012, 10, 906–912. [CrossRef]
Gogberashvili, M. Octonionic Electrodynamics. J. Phys. A Math. Gen. 2006, 39, 7099. [CrossRef]
Chanyal, B.C. Octonion generalisation of Pauli and Dirac matrices. Int. J. Geom. Methods Mod. Phys. 2015, 12, 1550007. [CrossRef]
Okubo, S. Introduction to Octonion and Other Non-Associative Algebras in Physics; Cambridge University Press: Cambridge, UK,
1995.
Stoica, O.C. Leptons, quarks, and gauge from the complex Clifford algebra Cl6. Adv. Appl. Clifford Algebra 2018, 28, 52. [CrossRef]
Chanyal, B.C. Classical geometrodynamics with Zorn vector-matrix algebra for gravity-dyons. Rep. Math. Phys. 2015, 76, 1–20.
[CrossRef]
Sedenion, Wikipedia, Sedenion—Wikipedia. Available online: https://en.wikipedia.org/wiki/Sedenion (accessed on 25 October
2023).
Cawagas, R.E. On the structure and zero-divisors of the Cayley-Dickson sedenion algebra. Disc. Math. Gen. Algebra App. 2004, 24,
251–265. [CrossRef]
Gillard, A.B.; Gresnigt, N.G. Three fermion generations with two unbroken gauge symmetries from the complex sedenions. Euro.
Phys. J. C 2019, 9, 44n6. [CrossRef]
Chanyal, B.C. Sedenion unified theory of gravi-electromagnetism. Indian J. Phys. 2014, 88, 1197–1205. [CrossRef]
Weng, Z.H. Color confinement and spatial dimensions in the complex-sedenion space. Adv. Math. Phys. 2017, 2017, 9876464.
[CrossRef]
Georgi, H.; Glashow, S. Unity of all elementary-particle forces. Phys. Rev. Lett. 1974, 32, 438. [CrossRef]
Huebsch, T.; Pallua, S. Symmetry breaking mechanism in an alternative SU(5) model. Phys. Lett. B 1984, 138, 279–282. [CrossRef]
Higgs, P. Broken symmetry and the mass of the gauge bosons. Phys. Rev. Lett. 1964, 13, 508. [CrossRef]

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
