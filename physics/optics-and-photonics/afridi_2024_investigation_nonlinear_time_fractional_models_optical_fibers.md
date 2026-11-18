Source: see manifest row of the PDF
PDF sha256: 7bf93d08e648412f0afbf18e703493847151bb5fcac56032e9cbbee333b9191f
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of afridi_2024_investigation_nonlinear_time_fractional_models_optical_fibers.pdf

Transcription of `afridi_2024_investigation_nonlinear_time_fractional_models_optical_fibers.pdf` in this directory, 18 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-18 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

fractal and fractional

Article

The Investigation of Nonlinear Time-Fractional Models in
Optical Fibers and the Impact Analysis of Fractional-Order
Derivatives on Solitary Waves
Muhammad Idrees Afridi 1,2, * , Tamanna Islam 3 , Md Ali Akbar 3
1
2
3

4

*

and Mohamed S. Osman 4, *

School of Mathematics and Computer Science, Hanjiang Normal University, Shiyan 442000, China
Applied Science Research Center, Applied Science Private University, Amman 11931, Jordan
Department of Applied Mathematics, University of Rajshahi, Rajshahi 6205, Bangladesh;
s1812028103@ru.ac.bd (T.I.); ali.akbar@ru.ac.bd (M.A.A.)
Department of Mathematics, Faculty of Science, Cairo University, Giza 12613, Egypt
Correspondence: afridi@hjnu.edu.cn (M.I.A.); mofatzi@cu.edu.eg or mofatzi@sci.cu.edu.eg (M.S.O.)

Abstract: In this article, we investigate a couple of nonlinear time-fractional evolution equations,
namely the cubic-quintic-septic-nonic equation and the Davey–Stewartson (DS) equation, both of
which have significant applications in complex physical phenomena such as fiber optical communication, optical signal processing, and nonlinear optics. Using a powerful technique named the extended
generalized Kudryashov approach, we extract different rich structured soliton solutions to these
models, including bell-shaped, cuspon, parabolic soliton, singular soliton, and squeezed bell-shaped
soliton. We also study the impact of fractional-order derivatives on these solutions, providing new
insights into the dynamics of nonlinear models. The results are compared with the existing literature,
revealing novel and distinct solutions that offer a deeper understanding of these fractional models.
The results show that the implemented approach is useful, reliable, and compatible for examining
fractional nonlinear evolution equations in applied science and engineering.

Citation: Afridi, M.I.; Islam, T.; Akbar,

Keywords: soliton solution; time-fractional cubic-quintic-septic-nonic equation; time-fractional DS
equation; extended generalized Kudryashov method

M.A.; Osman, M.S. The Investigation
of Nonlinear Time-Fractional Models
in Optical Fibers and the Impact
Analysis of Fractional-Order
Derivatives on Solitary Waves. Fractal
Fract. 2024, 8, 627. https://doi.org/
10.3390/fractalfract8110627
Academic Editor: Nikolay
A. Kudryashov
Received: 10 September 2024
Revised: 14 October 2024
Accepted: 21 October 2024
Published: 24 October 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://

1. Introduction
In recent times, the study of soliton solutions has become a highly active area of
research in nonlinear fiber optics. Soliton characteristics are principally described by the
nonlinear Schrödinger equation and its various forms, including a form of singleton selfphase modulation (SPM) that arises from the refractive index changes in optical fiber.
This phenomenon generally occurs under Kerr law nonlinearity and is characterized by
a cubic nonlinear structure, which is modeled by the power law nonlinearity of media.
The third form of SPM is associated with optical Gaussian profiles together with optical
solitons governed by a nonlinear logarithmic law. Besides these three forms of single
nonlinear terms, the other types of SPM are governed by saturable and exponential laws,
which are rarely observed. More complex forms of SPM generally involve two or more
nonlinear components that are applicable to different devices, such as LiNbO3 crystals.
Other refractive index structures include the quadratic–cubic (QC) form, the generalized
QC form, the anti-cubic (AC) form, and the generalized AC form of nonlinearity, which are
usually known as cubic–quantal nonlinearity. The SPM form is parabolic, and its theory is
based on the dual power laws of SPM, quadratic–cubic, anti-cubic, and generalized AC
types, also known as refractive index structures. In this study, we investigate the cubicquantic-septic-nonic (CQS) nonlinear structure within the framework of a triple power

creativecommons.org/licenses/by/
4.0/).

Fractal Fract. 2024, 8, 627. https://doi.org/10.3390/fractalfract8110627

https://www.mdpi.com/journal/fractalfract

## PDF page 2

Fractal Fract. 2024, 8, 627

2 of 18

law. This analysis is based on both chromatic dispersion (CD) and the refractive index in
nonlinear structures. The SPM model is
(
)
iVt + a Vxx + F |V |2 V = 0,
(1)

√
where the initial term takes from temporal evolution, where i = −1, although F appear
from SPM here, x describes the space variable and t signifies the time-related variable, and
V ( x, t) denotes the wave profile. Therefore, the cubic-quantic-septic-nonic equation [1] is
(
)
iVt + a Vxx + b1 |V |2 + b2 |V |4 + b3 |V |6 + b4 |V |8 V = 0.
(2)
In fluid dynamics, the Davey–Stewartson (DS) equation is an important model. This
model was established by Davey and Stewartson to describe the evolution of a threedimensional wave packet in water with finite depth. This equation is formed by a system of
partial differential equations that combine a real field (mean flow) and a complex field (wave
amplitude). The soliton solutions of this model can take various forms, including periodic,
dark, bright, exponential, and singular solitons. The DS equation is a three-dimensional
soliton equation. The DS equation is [2]
)
1 (
iVt + σ2 Vxx + σ2 Vyy + λ|V |2 V − VR x = 0,
2
(
)
R xx − σ2 Ryy − 2λ |V |2 = 0.
x

(3)

Here, λ is a real number. If σ = 1, it is known as the DS-I equation, and if σ = −1,
it is the DS-II equation. The cases of focusing and de-focusing are characterized by the
parameter λ. Moreover, two well-known examples of integrable equations in two space
dimensions that arise as higher-dimensional generalizations of the nonlinear Schrödinger
equation are DS-I and DS-II. These equations play an active role in understanding turbulence for plasma waves and other intriguing physical phenomena. Basically, they were
made in terms of water waves, but their utilization has expanded to several sectors of the
scientific and engineering fields, including fluid mechanics and plasma physics.
Fractional Derivative: Fractional calculus, which involves the integration and differentiation of fractional orders, is a natural extension of classical calculus. The concept of a
fractional operator in fractional calculus is derived from classical calculus principles. It was
first mentioned by Leibniz and L’Hospital in their correspondence in 1695. Later, various
physicists and mathematicians defined fractional derivatives from their own points of
view. Some widely used definitions of fractional derivatives are the Lacroix derivative [3],
Riemann–Liouville derivative [4], Jumarie modified Riemann–Liouville (RL) derivative [5],
conformable derivative [6], Caputo derivative [7], and beta derivative [8].
The memory effect, where the current state of a material or phenomenon is influenced
by its entire previous state rather than just the immediate past, known as the memory effect,
can be analyzed using the Riemann–Liouville (RL) and Caputo derivatives, making them
useful for modeling in physical science and engineering, such as viscoelastic materials,
anomalous diffusion, signal processing, etc. However, these definitions of derivative
exhibit shortcomings in adhering to the fundamental principles of derivatives; for instance,
for a constant function, the RL definitions of fractional derivative are unable to yield
zero and do not satisfy the chain rule; for the only zero domain, conformable derivative
produces zero; and Caputo is restricted to highly smooth functions and does follow the
chain rule. In contrast, the beta fractional derivative, presented in 2016 by Atangana
et al. [9], addresses all these issues. The beta fractional derivative in modeling is notable
for its ability to generalize the classical integer-order derivative while retaining important
mathematical properties, such as the Leibnitz rule and the chain rule. This feature facilitates
the application of familiar analytical and numerical methods with minimal modifications.
Unlike intricate fractional derivatives such as the Riemann–Liouville or Caputo derivative,

## PDF page 3

Fractal Fract. 2024, 8, 627

3 of 18

the beta derivative simplifies the mathematical structure of the model introducing fractional
dynamics through fractional order parameters. Although the beta derivative lacks memory
effects, it is particularly useful in models where the aim is to study the effects of noninteger differentiation without complicating the interpretation of physical mechanisms.
Thus, the beta fractional derivative strikes a balance between complexity and analytical
controllability, making it suitable for exploring fractional dynamics in systems with less
emphasis on memory effects. Therefore, in this article, we utilized the beta derivative. The
β derivative [10] is defined as
(
(
) 1− β )
1
− χ(t)
χ t + h t + Γ( β)
A β
D
χ
t
=
lim
, t ≥ 0, 0 < β ≤ 1,
(4)
(
)
0 t
h
h →0
where χ(t) is a differentiable function, and β is the fractional-order derivative. In the
oscillating phenomenon, different types of physical models are created and explained using
fractional calculus for gradual changes from relaxation. The wave solution of the nonlinear
fractional differential equation (NFDE) is an important portion of the investigation of
nonlinear physical explication. The fundamental properties that the beta derivative satisfies
are provided in the following:
i.
ii.
iii.
iv.
v.

A β
0 Dt C = 0.
A β
A β
A β
0 Dt [ c1 χ ( t ) + c2 K( t )] = c1 0 Dt χ ( t ) + c2 0 Dt K( t ).
A β
A β
A β
0 Dt { χ ( t )K( t )} = χ ( t )0 Dt K( t ) + K( t )0 Dt χ ( t ).
β
β
K(t)0A Dt χ(t)−χ(t)0A Dt K(t)
A β χ(t)
.
0 Dt K(t) =
K2 (t)
A D β χ (K( t )) = dχ(K(t)) A D β K( t ).
0 t
dK(t) 0 t

Beside these fundamental properties, the beta derivative satisfies all other theorems
and properties associated with the integer-order derivative [9]. Moreover, the beta derivative has a relationship with the classical derivative, which ensures that the beta derivative
behaves similarly to the classical derivative in all aspects, highlighting its broader applicability and consistency. In the following, we will establish this relationship.
(
(
)1− β
) β −1
1
1
Put δ = h t + Γβ
. Thus, h = δ t + Γβ
. Therefore, as h → 0 implies δ → 0 .
Hence, we obtain
A β
0 Dt χ ( t ) =

(

1
t+
Γβ

) 1− β

χ(t + δ) − χ(t)
lim
=
δ
δ →0

(

1
t+
Γβ

)1− β

dχ(t)
.
dt

The exact solitary wave solutions play a fundamental role in searching nonlinear
equations in various fields, such as applied mathematics, science, and engineering. They
provide a strong interpretation of the behavior of the system. They also make a bridge
between theory and applications. From the exact solutions of an equation, one can understand the effect of the parameters on the system, identify critical points, and predict
qualitative changes. The properties, advantages, and limitations of the beta derivative
and its applicability are discussed in detail in references [10,11]. An in-depth analysis and
potential use in various fields are also discussed in these references.
Exact solutions assist mathematicians, scientists, and engineers to understand, predict,
and manipulate nonlinear phenomena. Therefore, in recent years, several researchers have
developed and improved some analytical and asymptotic methods for solving nonlinear
fractional differential equations (NFDEs). Some widely used methods and strategies are:
the modified auxiliary equation method [12], the improved Bernoulli sub-equation function
approach [13], the local fractional Riccati differential equation method [14], the fractional
reduced differential transform approach [15], the ( G ′ /G )-expansion scheme [16,17], the
sine–Gordon expansion process [18,19], the Lie symmetry technique [20], the homotopy
analysis method [21], the Hirota bilinear procedure [22], the Cole–Hopf transformation [23],

## PDF page 4

Fractal Fract. 2024, 8, 627

4 of 18

the new extended direct algebraic method [24], the F-expansion method [25], the variational
iteration procedure [26], the modified simple equation approach [27], the first integral technique [28], the Adomian polynomial scheme [29], the fractional sub-equation scheme [30],
the modified Kudryashov approach [31], the exp-function technique [32], etc.
Also, there are several studies on fractional derivatives and their applications. Torvik
and Bagley [33] investigated the applicability of fractional derivatives in real materials. Gu and Ou [34] observed chaos in a fractional duplication system. Du et al. [35]
showed using the least square method that the results obtained from fractional models
in memory-related phenomena across mechanics, biology, and psychology fit experimental data. Tarasov [36] discussed the nature of fractional derivatives with integer-order
derivatives. Luchko [37] explained fractional derivatives and the fundamental theorem of
fractional calculus. Jisha et al. [38] investigated the fractional-order KS equation using the
rational function method, etc.
Therefore, the objective of this article is to investigate nonlinear time-fractional models in optical fibers, specifically focusing on the cubic-quintic-septic-nonic equation and
the Davey–Stewartson equation. In this study, we extract soliton solutions to the stated
equations using the extended generalized Kudryashov method and examine the impact of
fractional-order derivatives on these solutions, providing new insights into the behavior
and dynamics of nonlinear models in optical fibers.
2. The Extended Generalized Kudryashov Method
The extended generalized Kudryashov method uses generalized ansatz functions with
adjustable parameters, allowing the method to investigate a wide range of classical and
fractional-order nonlinear evolution equations. The originality of this method is that it
is capable of generating various exact solutions, such as solitons, rational, and periodic
solutions, making it particularly useful for unraveling complex problems in fields such as
mathematical physics and fluid dynamics. The ability to solve complex nonlinear equations such as time-fractional cubic-quintic-septic-nonic and Davey–Stewartson equations
demonstrates the potentiality of the method.
Let us consider the following generic nonlinear equation:
(
)
2α
H u, uαt , u x , uy , u2α
,
u
,
u
,
.
.
.
= 0,
(5)
xx
tt
xt
where H is a polynomial of u and its partial derivative, which includes the highest-order
derivative and nonlinear terms.
First step: Equation (5) can be transformed from fractional-order differential equation to a nonlinear integer-order differential equation by means of the fractional wave
transformation. We consider the subsequent fractional transformation
u( x, y, t) = V (ξ ), ξ = k1 x + k2 y −

(
)α
v
1
t+
,
α
Γ(α)

(6)

where k1 , k2 , and v are nonzero constants used to minimize Equation (5) to the following
equation
(
)
G V, V ′ , V ′′ , V ′′′ , . . . = 0,
(7)
where G is a polynomial in V (ξ ) and its derivatives V ′ (ξ ), V ′′ (ξ ), and so on. Here, V ′ = dV
dξ .
Second step: In agreement with the extended Kudryashov approach, we consider the
solution of Equation (7) in the following form:
V (ξ ) =

∑iN=0 ai Ri
,
∑ jM=0 Cj R j

(8)

## PDF page 5

Fractal Fract. 2024, 8, 627

5 of 18

where ai (i = 0, 1, 2, 3, . . . , N ) and Cj ( j = 0, 1, 2, . . . , M) are constants to be examined,
such that a N ̸= 0 and C M ̸= 0. For the extended Kudryashov approach, we consider the
following supporting equation:
[
]
R′ (ξ ) = R p+1 (ξ ) − R(ξ ) ln l, 0 < l ̸= 1.
(9)
The general solution of Equation (9) is
]1/p
1
R(ξ ) =
,
1 − ln l A exp( pξ )
[

(10)

where A is an integral constant, and p is a positive integer.
Third step: N and M are to be determined by balancing the highest-order derivative
with the highest power of the nonlinear term in Equation (7).
Fourth step: Substituting Solution (8) and Equation (9) in Equation (7), a polynomial
in Rij (i, j = 0, 1, 2 . . . .) can be founded. Collecting and equalizing each term of resemble
power to zero, a group of algebraic equations can be found by using Mathematica to define
the values of λi , λ j , and v. By exploiting these values, the result can be obtained.
3. Determination of Soliton Solutions
Since fractional models can better express the intricate behavior and dynamics of
physical phenomena, in this article, we consider fractional-order models instead of integerorder models. They are especially useful to explain long-range interactions that are difficult
to describe by integer-order models. Fractional models offer further flexibility and precision
in fields such as mechanics, biology, finance, and control systems, where integer-order
models may not be sufficient.
3.1. The Time-Fractional Cubic-Quintic-Septic-Nonic Equation
In this section, we formulate assorted soliton solutions to the time-fractional cubicquantic-septic-nonic equation with the help of the extended generalized Kudryashov
expansion approach. We assume the model of the form [1]
(
)
iuαt + au xx + b1 |u|2 + b2 |u|4 + b3 |u|6 + b4 |u|8 u = 0.
(11)
Here, it is to be noted that bj (1 ≤ j ≤ 4) stems from u j for (1 ≤ j ≤ 4) nonlinearity.
Even though u and u2 are substantialized for LiNbO3 crystals, u3 and u4 are negligibly inconsiderable. This part includes these nonlinearities to discuss the similar type of NLSE and
inquiry its integrability aspect for the initial time. It should be noted that the insignificant
contribution must be set to zero to ensure integrability. This would result in consistency
within mathematical and physical problems. Consider the complex structure of the wave
solution:
u( x, t) = V (ξ )eiϕ( x,t) ,
(12)
with

and

(
)α )
v
1
ξ = k x+
t+
,
α
Γ(α)

(13)

(
)α
w
1
ϕ( x, t) = −kx +
t+
+ θ.
α
Γ(α)

(14)

(

Here, V (ξ ) is the amplitude component, where ξ is the wave variable, and v is the
soliton speed, and ϕ( x, t) arises from the phase component, whereas θ is the phase constant,
w is the angular frequency, and k is the wave number [1].

## PDF page 6

Fractal Fract. 2024, 8, 627

6 of 18

By substituting Equation (12) into Equation (11), it is transformed into a complex
equation, where the real and imaginary parts give us the following simplest equation:
(
)
ak2 V ′′ − V ak2 + w + b4 V 9 + b3 A7 + b2 V 5 + b1 V 3 = 0,
(15)
and

−kV ′ (2ak + v) = 0.

(16)

From Equation (16), is the following is obtained:
v = −2ak.

(17)

The balance number for Equation (15) is 1/4. Thus, in order to simplify Equation (15),
we use the next transformation:
1
V (ξ ) = U (ξ ) 4 .
(18)
Now, using the transformation (18), Equation (15) is converted to the following:
(
)
5
7
2
4ak2 UU ′′ − 3ak2 UU ′ − 16U 2 ak2 + w + 16b1 U 2 + 16b3 U 2 + 16b4 U 4 + 16b2 U 3 = 0. (19)
Placing b1 = b3 = 0 into Equation (19), we obtain
(
)
2
4ak2 UU ′′ − 3ak2 UU ′ − 16U 2 ak2 + w + 16b4 U 4 + 16b2 U 3 = 0.

(20)

Since in Equation (20), b1 and b3 are free from all term-bearing functional exponents,
we can set b1 = b3 = 0 simply for Equation (20) to be rendered integrable. Only b2 and b4
hold up to permit the integrability of Equation (20). Equation (20) and the main equation
are equivalent to study with simply two non-zero terms addressing b2 and b4 . It implies
that the NLSE is integrable with a cubic–quintic nonlinear form.
Now, by balancing UU ′′ and U 4 appearing in Equation (20), we obtain
2( N − M ) + 2 = 4( N − M ) ⇒ N = M + 1 .
Here M is a free parameter; accordingly setting M = 1, we obtain N = 2. Thus, from
(8), the solution structure of Equation (20) can be presented as follows:
a0 + a1 R ( ξ ) + a2 R ( ξ )2
,
C0 + C1 R(ξ )

U (ξ ) =

(21)

where a0 , a1 , a2 , C0 , and C1 are undefined constants to be investigated.
Now, by inserting (21) into Equation (20) and placing the coefficient of the identical
power of ( R(ξ ))i , where (i = 0, 1, 2) equal to zero, we can obtain some algebraic equations.
Solving these equations, we obtain the value of
a0 , a1 , a2 , C0 , C1 , and w as follows:
√ √
√
√
2a2 (−10b2 +3i 5 ak(ln l ) b4 )
b
√2 4 ,
Set 1: a0 = 0, a1 = − a2 , C0 =
, C1 = − √ 4ia
2
2
15ak (ln l )

w=

5 ak(ln l )

1 2
ak (−16 + (ln l )2 ).
16

(22)

Plugging in (22) along with Equation (10) into (21), we obtain the solution as follows:

√

1 ik (16x − akF (−16+(ln l )2 ))
1/4 − 16
α

V11 ( x, t) = 5

e

and

x

a

K
akl k( 2 + α F) ln l sech( 2α
( xα + 2aF) ln l ) a2
( √
√ √ )
2aF
k
(
x
+
)
α ) ln l b0 − 4i
10 ak(1 + l
5a2 b4

1/4

,

(23)

## PDF page 7

Fractal Fract. 2024, 8, 627

7 of 18

√
akM

1

x

a

K
( xα + 2aF) ln l ) a2
akl k( 2 + α F) ln l cosech( 2α
)
√ √
√
2aF
)
k
(
x
+
α ) ln l b0 − 4i
10 ak (1 + l
5a2 b4

2

V12 ( x, t) = 51/4 e− 16 ik(16x− α (−16+(ln l ) )) (
(
)α
1
wherein F = t + Γα
.

Set 2: a0 = 0, a1 = − a2 , C0 = −
w=

√ √
√
2a2 (10b2 +3i 5 ak(lnl ) b4 )
15ak2 (ln l )

2

1/4

,

(24)

√

b4
,
5 ak(ln l )

√2
, C1 = √ 4ia

)
1 2(
ak −16 + (ln l )2 .
16

(25)

We substitute the values presented in (25) along with Equation (10) into (21). This
gives us the following solution:
x

a

k
iak2 l k( 2 + α F) (ln l )2 sech( 2α
( xα + 2aF((ln l ))
15 1/4 − 1 ikE
e 16 (−
V21 ( x, t) = √
)
√
√
√
2a
2a
2
−10i(1 + l k(x+ α F) )b2 + 3 5 a b4 k(ln l )(−1 + l k(x+ α F) )

1/4

,

(26)

and
x

a

k
iak2 l k( 2 + α F) cosch( 2α
( xα + 2aF ) ln l )(ln l )2
15 1/4 − 1 ikE
e 16 (−
)
V22 ( x, t) = √
√ √ √
2aF
2a
2
−10i(1 + l k(x+ α ) )b2 + 3 5 a b4 k(−1 + l k(x+ α F) ) ln l

1/4

,

(27)

2
1
wherein E = (16x − akF
α (−16 + (ln l ) )), F = ( t + Γα ) .
The solutions presented above contain arbitrary constants. By choosing specific values
for these constants, solitons with diverse geometric shapes can be obtained. However, due
to page constraints, these solutions are not presented here.
α

3.2. The Time-Fractional Davey–Stewartson (DS) Equation
In this section, we formulate various soliton solutions to the time-fractional (2 + 1)dimensional Davey–Stewartson equation using the extended generalized Kudryashov
expansion method. We consider the model as shown in [39]:
)
1 (
iVtα + σ2 Vxx + σ2 Vyy + λ|V |2 V − VWx = 0,
2
(
)
Wxx − σ2 Wyy − 2λ |V |2 = 0,
x

(28)

where V ( x, y, t) represents the complex wave function (or amplitude) of the surface wave,
while W ( x, y, t) denotes the real potential function related to this wave. The values of the
constants σ and λ depend on the physical state of the system. The signs and values of σ
and λ are determined by the inherent dispersion and nonlinearity of the system.
To split Equation (28) into its real and imaginary parts, we use the following transformation:
V ( x, y, t) = V (ξ )eiη , W ( x, y, t) = W (ξ ),
(29)
wherein
(
)β
(
)β
α
1
k
1
ξ ( x, y, t) = x − 2αy +
t+
, η ( x, y, t) = αx + y +
t+
+ n,
β
Γ( β)
β
Γ( β)

(30)

where α and k are real constants. To split Equation (28) into real and imaginary parts, we
substitute (29) and (30) into (28). As a result, we obtain
(
)
(
)
σ2 1 + 4σ2 α2 V ′′ (ξ ) + 2λV 3 (ξ ) − 2k + σ2 α2 + σ4 V (ξ ) − 2V (ξ )W ′ (ξ ) = 0,
(31)

## PDF page 8

Fractal Fract. 2024, 8, 627

8 of 18

(

)
[
]
1 − 4σ2 α2 W ′′ (ξ ) = 2λ V 2 (ξ ) ′.

(32)

Integrating (32) with respect to ξ, we obtain
W ′ (ξ ) =

2λ
V 2 (ξ ) + C.
(1 − 4σ2 α2 )

(33)

1
. Substituting (33) into (31), we obtain
Here, C is an integral constant and α ̸= ± 2σ
(
)
(
)
(
)
2
3
2 2
4
σ2 1 + 4σ2 α2 V ′′ (ξ ) + 2λ 1 −
V
ξ
−
2k
+
σ
α
+
σ
+
2C
V (ξ ) = 0.
(34)
(
)
(1 − 4σ2 α2 )

In line with the extended generalized Kudryashov approach, the solution of Equation
(34) is
a0 + a1 R ( ξ ) + a2 R ( ξ )2
,
(35)
V (ξ ) =
b0 + b1 R(ξ )
where a0 , a1 , a2 , b0 , and b1 are undefined constants to be examined.
Putting (35) into Equation (34) and placing the coefficient of the alike power of Ri (ξ ),
where (i = 0, 1, 2) equal to zero, we obtain some algebraic equations. By solving these
equations, we obtain the value
of a0 , a1 , a2 , b0 , b1 , and√C.
√
2 2

2 2

−1+4α σ
, a2 = − iσlnlb1 √−1+4α σ , b0 = 0,
Set 1: a0 = 0, a1 = iσlnlb1 √
2 λ

C=

λ

) (
)
)
1( (
−2 2k + α2 σ2 + σ4 − σ2 + 4α2 σ4 (lnl )2 .
4

(36)

By substituting the values from Equation (36) into Solution (35) along with Equation
(30), we obtain the following solution:
β

V31 ( x, y, t) =

ie

i(αx +y+ βk (t+ Γ(1β) ) +n)

√

√
lnlσ −1 + 4α2 σ2

2 λ

and

β

i(αx +y+ βk (t+ Γ(1β) ) +n)

(
tanh

√
lnlσ −1 + 4α2 σ2

)
ξ
lnl .
2

(37)

)
ξ
√
V32 ( x, y, t) =
coth
lnl .
(38)
2
2 λ
√ √
√ √
Set 2: a0 = − 4λb b 1+2λb2 (2i λσ −1 + 4α2 σ2 lnlb03 + i λσ −1 + 4α2 σ2 lnlb02 b1
0 1
1
√
√
)2
2 σ2 lnl (2b + b )
2 2( 2
0
1
2
2
2
+ −λσ (−1 + 4α σ )(lnl ) b0 2b0 + 3b0 b1 + b12 ), a1 = − iσ −1+4α √
, a2 = 0,
ie

(

2 λ

C=

) (
)
)
1( (
−2 2k + α2 σ2 + σ4 − σ2 + 4α2 σ4 (lnl )2 .
4

(39)

By using Equation (39) together with Equation (35) in Equation (29), we derive the
following solution:
)
√ √
√ √
√
iσ glnl (2b0 + b1 ) 2i λσ glnlb03 + i λσ glnlb02 b1 + h
+
.
(
)√
4λb0 b1 + 2λb12
2 1 + lξ λ

(40)

( √
)
√ √
√ √
σ glnl (2b0 + b1 ) 2 λσ glnlb03 + i λσ glnlb02 b1 + h
V42 ( x, y, t) =
−
,
(
)√
b1
4λb0 b1 + 2λb12
2 −1 + l ξ λ
b0 + 1−
ξ
l

(41)

V41 ( x, y, t) =

eiϕ[ x,y,t]
b1
b0 + 1+
lξ

(

and
eiϕ[ x,y,t]

where g = 1 − 4α2 σ2 and h =

√

(
)2
−λσ2 g(lnl )2 b02 2b02 + 3b0 b1 + b12 .

## PDF page 9

Fractal Fract. 2024, 8, 627

9 of 18

The solutions established above include subjective constants. By selecting particular
values for these constants, it is possible to obtain solitons with various geometric shapes.
However, these solutions are not shown here due to space limitations.
4. Graphical Representations and Physical Explanations
In this section, we discuss the graphical representation and interpretation of the deterministic solutions obtained from the time-fractional cubic-quintic-septic-nonic equation
and the time-fractional DS equation. We depict the 3D and 2D profiles of these solutions
by selecting specific values for various parameters. This helps us understand how the
mechanisms of the physical phenomena work.
4.1. The Nonlinear Time-Fractional Cubic-Quantic-Septic-Nonic Equation
In this part, we provide a physical explanation and demonstration of the solution to
the nonlinear cubic-quintic-septic-nonic equation. We use graphs to graphically represent
the solutions. Various details in the mathematical sciences are also presented, mainly for
the purpose of comparison. The 3D graphics explore the behavior of the wave in terms of
spatial and temporal coordinates ( x, t), and the two-dimensional graphs are plotted for
different values of fractional order to describe the effect of fractional-order derivatives on
solitary waves. These graphs are illustrated by using Wolfram Mathematica. In Figure 1,
the modulus plot of V11 ( x, t) is depicted with the values of the parameters k = 0.9, w = 3,
l = 2, a = 2, a2 = −0.0006, C0 = −0.0001, C2 = −0.0003, and b4 = −0.00015 within the
intervals −20 ≤ x ≤ 20 and 0 ≤ t ≤ 10. When α = 0.1, the wave is initially started in the
form of an asymptotic shape. For the change in the value of α (fractional-order) the soliton
wave becomes a bell-shape soliton, i.e., the soliton transforms the shape from its initial
Fractal Fract. 2024, 8, x FOR PEER REVIEW
9 of the
18
state for α = 0.1 to a bell shape for α = 0.9. We observe that the soliton is moved from
left direction to the right direction. Also, the shape of this soliton is rapidly changed when
α > 0.1.

(a) For 𝛼 = 0.1.

(d) For 𝛼 = 0.9.

(b) For 𝛼 = 0.3.

(c) For 𝛼 = 0.6.

(e) The 2D graph for different values of fractional order (𝛼).

Figure
𝑡) for
for k𝑘==0.9,
0.9,w𝑤==3,3,l =
𝑙 =2,
Figure1.1.Graphical
Graphicalpresentation
presentationofofthe
themodulus
modulusplot
plotof
ofsolution
solution 𝑉V 11(𝑥,
(x,t)
=
−0.0006,
𝐶
=
−0.0001,
𝑏
=
−0.0003,
and
𝑏
=
−0.00015.
2,a =
𝑎=
2,
𝑎
2, a2 = −0.0006, C0 = −0.0001, b2 = −0.0003, and b4 = −0.00015.

In Figure 2, the modulus plot of the solution 𝑉 (𝑥, 𝑡) is depicted with the values of
parameters
𝑘 = 0.03, 𝑤 = 3, 𝑎 = 1, 𝑏 = −0.03, 𝑏 = −0.0015, 𝑙 = 6, 𝐶 = 0.0001,
and
𝑎 = −0.00002 within the intervals −20 ≤ 𝑥 ≤ 20 and 0 ≤ 𝑡 ≤ 10. Initially, the tail of the
soliton cut the 𝑥-axis at (40, 0) approximately, and the soliton cut the 𝑦-axis at (0, 0.01) for
the value of fractional-order 𝛼 = 0.03. When 𝛼 = 0.1, the soliton cut the 𝑦 -axis at the

## PDF page 10

Fractal Fract. 2024, 8, 627

10 of 18

In Figure 2, the modulus plot of the solution V11 ( x, t) is depicted with the values of
parameters k = 0.03, w = 3, a = 1, b2 = −0.03, b4 = −0.0015, l = 6, C0 = 0.0001, and
Fractal Fract. 2024, 8, x FOR PEER REVIEW
10 of 20
a2 = −0.00002 within the intervals −20 ≤ x ≤ 20 and 0 ≤ t ≤ 10. Initially, the tail of the
soliton cut the x-axis at (40, 0) approximately, and the soliton cut the y-axis at (0, 0.01) for
the value of fractional-order α = 0.03. When α = 0.1, the soliton cut the y-axis at the point
(0, 0.35). We observe from 2( a) that for the change in the value of fractional order, the shape
of the soliton is gradually changed.

(a) For 𝛼 = 0.03.

(d) For 𝛼 = 0.9.

(b) For 𝛼 = 0.1.

(c) For 𝛼 = 0.3.

(e) The 2D graph for different values of fractional order (𝛼).

(𝑥,for
Figure
2. Graphical
Graphical presentation
presentationofofmodulus
modulusplot
plot
solution
𝑡) kfor
𝑘 = 0.03,
Figure 2.
of of
solution
V 11𝑉(x,t)
= 0.03,
w = 3,𝑤l ==3,6, 𝑙a =
=6,1,
= −0.00002,
𝑏
=
0.0001,
𝑏
=
−0.03,
and
𝑏
=
−0.0015.
𝑎a ==1,−𝑎0.00002,
b0 = 0.0001, b2 = −0.03, and b4 = −0.0015.
2

The
modulus of
of the
thesolution
solutionV𝑉
revealsa adeformed
deformed
bell-shape
soliThe plot of the modulus
x, t)𝑡)reveals
bell-shape
soliton
11 ((𝑥,
ton
𝑤l ==1,4,𝑙 a==4,2,𝑎a2
==
2, 𝑎
= C0
−10,
−0.000009,
= 0.007
−10
for kfor
= 2,𝑘w==2,1,
−10,
= 𝐶− =
0.000009,
b2 =𝑏0.007,
and ,b4and
= −𝑏10 =
within
within
the −
intervals
<𝑥
< 020< tand
< 10,
is in
presented
in From
Figure
3. From
the
intervals
10 < x−10
< 20
and
< 0
10,< 𝑡
which
is which
presented
Figure 3.
the
figure,
theisfigure,
it isthat
observed
that
of is
the
soliton
is the type
asymptotic
type As
at
it
observed
initially,
theinitially,
shape ofthe
theshape
soliton
the
asymptotic
at α = 0.1.
𝛼the
= 0.1.
of the
fractional
order (𝛼)
gradually
increases,
the graph
slowlya
valueAs
of the
the value
fractional
order (
α) gradually
increases,
the graph
slowly
changes into
deformed
bell-shaped
soliton.
For α =
0.2, we
observe
an we observe
approximately
solitary
changes
into a
deformed
bell-shaped
soliton.
For 𝛼
= 0.2,
an stable
approximately
wave.
After
that,
the
wave
travels
from
the
left
to
right
direction
at
a
constant
stable solitary wave. After that, the wave travels from the left to right direction at aspeed,
conmaintaining
shape anditsize.
stant
speed, its
maintaining
shape and size.
The modulus plot of V 12 (x,t) exhibits a soliton, which is portrayed in Figure 4 by
selecting the parameters k = 2, w = 1, l = 2, a = 0.000012, a2 = 0.00002, C0 = 0.00003,
b2 = 0.003, and b4 = 0.000015 within the intervals −10 ≤ x ≤ 20 and 0 ≤ t ≤ 100. When
α = 0.1, the wave starts with an asymptotic shape. As the value of α (fractional-order)
changes, the soliton transforms into a deformed spike shape. Specifically, it changes from
an asymptotic shape at α = 0.1 to a spike shape at α = 0.9. We notice that the soliton moves
from left to right, and its shape quickly changes when α is greater than 0.1.

## PDF page 11

Fractal Fract. 2024, 8, 627

11 of 18

Figure 3. Graphical presentation of modulus plot of solution V 11 (x,t), k = 2, w = 1, l = 4, a = 2,
a2 = −10, C0 = −0.000009, b2 = 0.007, and b4 = −10.

Figure 4. Graphical presentation of modulus plot of solution V 11 (x,t) for k = 2, w = 1, l = 2, a =
0.000012, a2 = 0.00002, C0 = 0.00003, b2 = 0.003, and b4 = 0.000015.

The modulus plot of V 21 (x,t) exhibits a cuspon, represented in Figure 5 by selecting
the parameters k = 1, w = 1, l = 4, a = 0.1, a2 = 0.3, b2 = −0.003, C0 = 0.1, and b4 = 0.01
inside the range of −10 ≤ x ≤ 20 and 0 ≤ t ≤ 10. For α = 0.01, the wave initially begins in

## PDF page 12

Fractal Fract. 2024, 8, 627

12 of 18

Fractal Fract. 2024, 8, x FOR PEER REVIEW

13 of 20

an asymptotic shape. While the value of α (fractional-order) changes, the soliton changes
into a cuspon-type soliton, i.e., the soliton transforms from an asymptotic shape for α = 0.01
to a cuspon shape for α = 0.9. We observe that the soliton is moved from the left direction
to the right direction, and the shape of this soliton is rapidly changed when α > 0.01.

(a) For 𝛼 = 0.01.

(d) For 𝛼 = 0.9.

(b) For 𝛼 = 0.03.

(c) For 𝛼 = 0.4.

(e) The 2D graph for different values of fractional order (𝛼).

Figure
presentation of
of modulus
modulus plot
plot of
of solution
solutionV𝑉12 (𝑥,
fork 𝑘
𝑤 1,
= l1,=𝑙 4,=a4,=𝑎0.1,
=
Figure 5.
5. Graphical
Graphical presentation
(x,t)𝑡)for
==
1, 1,
w=
=
0.3,
𝐶
=
0.1,
𝑏
=
−0.003,
and
𝑏
=
0.01.
0.1,
𝑎
a2 = 0.3, C0 = 0.1, b2 = −0.003, and b4 = 0.01.

𝑡) exhibits
exhibits aa parabolic
parabolic shape
shape soliton, as showed
The
The modulus
modulus plot
plot of
of solution
solution 𝑉
V 21(𝑥,
(x,t)
in Figure 6 by
by selecting
selecting the
the parameters
parameters k𝑘== 0.03,
0.03 , a𝑎== 0.02,
0.02 , l 𝑙 =
=4
= 0.3
4,, a𝑎2 =
0.3, C𝐶0 =
= 0.1
0.1,,
−0.003
within the
the interval
interval −20
−20≤≤ x𝑥 ≤
≤ 20
and 00≤
≤ t𝑡 ≤
𝑏b2 =
= −
0.003,, and
and b𝑏4 =
= 0.01
0.01 within
20 and
≤ 10
10. When
𝛼
α=
= 0.001,
0.001, the wave
wave is
is initially
initially like
like aaplane.
plane.As
Asthe
thevalue
valueofof𝛼α (fractional-order)
(fractional-order) changes,
changes,
soliton transforms
transforms into
into aa parabolic
parabolicshape.
shape.ItItchanges
changesfrom
fromaaplane
planefor
for𝛼α ==0.001
0.001 to a
the soliton
parabolic-shaped soliton
soliton for
for α
= 0.3.
0.3. We
We observe
observe that
that the
the shape
shape of
of the soliton changes
parabolic-shaped
𝛼=
quickly when α𝛼 >
> 0.001.
0.001.
The plot of the modulus of solution V 22 (x,t) exhibits a squeezed bell-type soliton,
presented in Figure 7 by choosing the parameters k = 7, w = 1, l = 6, a = 0.001, a2 = 3,
C0 = 3, b2 = −0.003, and b4 = 0.0002 within the interval −10 ≤ x ≤ 20 and 0 ≤ t ≤ 10.
When α = 0.0001, initially, the wave shape is a one-sided squeezed soliton. For the change
in the value of α (fractional-order), the soliton wave becomes a squeezed bell-type soliton,
i.e., the soliton transforms the shape from its initial state (a one-sided squeezed soliton) for
α = 0.0001 to a squeezed bell-type soliton for α = 0.05. We observe that the shape of this
soliton is rapidly changed when α > 0.0001.

## PDF page 13

Fractal Fract. 2024, 8, 627

in Figure 6 by selecting the parameters 𝑘 = 0.03 , 𝑎 = 0.02 , 𝑙 = 4 , 𝑎 = 0.3 , 𝐶 = 0.1 ,
𝑏 = −0.003 , and 𝑏 = 0.01 within the interval −20 ≤ 𝑥 ≤ 20 and 0 ≤ 𝑡 ≤ 10 . When
𝛼 = 0.001, the wave is initially like a plane. As the value of 𝛼 (fractional-order) changes,
the soliton transforms into a parabolic shape. It changes from a plane for 𝛼 = 0.001 to a
13 of 18
parabolic-shaped soliton for 𝛼 = 0.3. We observe that the shape of the soliton changes
quickly when 𝛼 > 0.001.

(a) For 𝛼 = 0.001.

(b) For 𝛼 = 0.01.

(c) For 𝛼 = 0.3.

Fractal Fract. 2024, 8, x FOR PEER REVIEW

13 of 18

The plot of the modulus of solution 𝑉 (𝑥, 𝑡) exhibits a squeezed bell-type soliton,
presented in Figure 7 by choosing the parameters 𝑘 = 7, 𝑤 = 1, 𝑙 = 6, 𝑎 = 0.001, 𝑎 = 3,
𝐶 = 3 , 𝑏 = −0.003 , and 𝑏 = 0.0002 within the interval −10 ≤ 𝑥 ≤ 20 and 0 ≤ 𝑡 ≤
10. When 𝛼 = 0.0001, initially, the wave shape is a one-sided squeezed soliton. For the
(d)
The 2D
for different
values of fractional
order (𝛼).
change
in graph
the value
of 𝛼 (fractional-order),
the soliton
wave becomes a squeezed belltype
soliton,
i.e.,
the
soliton
transforms
the
shape
from
initial
state𝑎(a
one-sided
(𝑥,its
Figure6.6.Graphical
Graphical presentation
presentation of
plot
of of
solution
𝑉 V
𝑡) for
𝑘 = 0.03,
= 0.02,
𝑙 = 4,
Figure
ofmodulus
modulus
plot
solution
21 (x,t) for k = 0.03, a = 0.02, l = 4,
squeezed
soliton)
for
𝛼
=
0.0001
to
a
squeezed
bell-type
soliton
for
𝛼
=
0.05.
We ob𝑎 = 0.3, 𝐶 = 0.1, 𝑏 = −0.003, and 𝑏 = 0.01.
a2 = 0.3, C0 = 0.1, b2 = −0.003, and b4 = 0.01.
serve that the shape of this soliton is rapidly changed when 𝛼 > 0.0001.

(a) For 𝛼 = 0.0001.

(b) For 𝛼 = 0.00018.

(c) For 𝛼 = 0.05.

(d): The 2D graph for different values of fractional order (𝛼).
(𝑥,(x,t)
Figure7.7.Graphical
Graphicalpresentation
presentation of
of modulus
𝑡) for
Figure
modulusplot
plotof
ofsolution
solution𝑉V 22
for 𝑘k =
=0.03,
0.03, 𝑎a =
=0.02,
0.02, 𝑙l == 4,
4, 𝑎 = 0.3, 𝑏 = 0.1, 𝑏 = −0.003, and 𝑏 = 0.01.
a2 = 0.3, b0 = 0.1, b2 = −0.003, and b4 = 0.01.

4.2. The Nonlinear Time Fractional Davey–Stewartson Equation
The graph of the modulus plot of solution 𝑉 (𝑥, 𝑡) is exhibited in Figure 8 by selecting the parameters 𝑘 = 1, 𝛼 = 0.1, 𝜎 = 1, 𝜆 = 1, 𝑙 = 4, 𝑡 = 1, 𝑏 = 1, and 𝑏 = 1. Here,
for the 3D graph, we put a fixed value for 𝑡 , and the intervals of 𝑥 and 𝑦 are −10 ≤
𝑥, 𝑦 ≤ 10. Also, for the 2D graph, space is constant in Figure 8d, and time is constant in
Figure 8e, i.e., the graph in Figure 8d is drawn on a plane, and Figure 8e is also drawn on

## PDF page 14

Fractal Fract. 2024, 8, 627

14 of 18

4.2. The Nonlinear Time Fractional Davey–Stewartson Equation
The graph of the modulus plot of solution V 31 (x,t) is exhibited in Figure 8 by selecting
the parameters k = 1, α = 0.1, σ = 1, λ = 1, l = 4, t = 1, b0 = 1, and b1 = 1. Here, for
the 3D graph, we put a fixed value for t, and the intervals of x and y are −10 ≤ x, y ≤ 10.
Also, for the 2D graph, space is constant in Figure 8d, and time is constant in Figure 8e, i.e.,
the graph in Figure 8d is drawn on a plane, and Figure 8e is also drawn on a plane. When
β
= 0.1, the wave is initially started and after a gradual change in the fractional order
( β)
Fractal Fract. 2024, 8, x FOR PEER
REVIEW
14 of
18,
the wave shape is completed, slowly corresponding to the value of β. Here, we observe
that the shape of this soliton becomes a lump shape at β = 0.9.

(a) For 𝛽 = 0.1.

(b) For 𝛽 = 0.2.

(c) For 𝛽 = 0.9.

(d) The 2D graph for different values of fractional order

(e) The 2D graph for different values of fractional order

𝛽.

𝛽.

𝑉31 ((𝑥,
Figure 8. Graphical presentation
presentation of the modulus
modulus plot
plot of solution
solution V
x, t𝑡) for
for 𝑘k =
= 1,
1, 𝑤
w=
= 1,
1, l𝑙 =
= 6,
6,
=
3,
𝑏
=
3,
𝑏
=
−0.003,
and
𝑏
=
0.0002.
= 0.001,
0.001,a𝑎
a𝑎 =
=
3,
b
=
3,
b
=
−
0.003,
and
b
=
0.0002.
2
0
2
4

Figure 9,9,the
themodulus
modulusplot
plotofofsolution
solution
depicted
values
paIn Figure
V32𝑉( x,(𝑥,
t) 𝑡)
is is
depicted
forfor
thethe
values
of of
paramrameters
=1
1, 1,𝜆 l==1,4,𝑙 t==4,1,𝑡b0= =
1, 1,𝑏 and
= 1b, 1 =
and1.𝑏 =
1. for
Here,
for a
3D
eters
k=𝑘
1, α
=, 𝛼
0.1,=σ0.1
=, 1,𝜎 λ==
Here,
a 3D
graph,
we
consider
the 𝑡 as
constant,
the and
valuesthe
of x
and yofare
inside𝑦the
intervalsthe
0≤x
≤ 10
graph,
we t as
consider
the and
constant,
values
𝑥 and
are inside
intervals
and
1010
≤ yand
≤ 10.
Also,
for10.
theAlso,
2D for
graph,
time is
constant
in Figure
one9d,
space
0
≤ 𝑥−≤
−10 ≤
𝑦≤
the 2D
graph,
time is
constant9d,
in and
Figure
and
dimension
is
also
considered
constant
in
Figure
9e.
Initially,
for
β
=
0.04,
the
soliton
starts
one space dimension is also considered constant in Figure 9e. Initially, for 𝛽 = 0.04, the
in
an asymptotic
shape
at α = shape
0.03. For
change
thechange
value of
the
soliton
wave
soliton
starts in an
asymptotic
at 𝛼the
= 0.03.
Forinthe
in β,
the
value
of 𝛽,
the
becomeswave
an becomes
anti-bell-shaped
soliton.
The soliton. The
transforms
shape the
rapidly
fromrapits
soliton
an
anti-bell-shaped
solitonthe
transforms
shape
initial
state
(asymptotic)
= 0.04for
to 𝛽
an= 0.04
anti-bell
shape
for β =
0.2.for
From
idly
from
its initial
state for β
(asymptotic)
to an
anti-bell
shape
𝛽 =the
0.2.above
From
discussion,
can say we
thatcan
thesay
shape
thisshape
soliton
rapidly
changes
for β >
0.04. for 𝛽 >
the
above we
discussion,
thatofthe
of this
soliton
rapidly
changes
In
Figure
10,
the
modulus
plot
of
V
x,
t
is
depicted
for
the
values
of
the
parameters
(
)
33
0.04.
k = 1, α = 1, l = 2, σ = −0.01, λ = 0.001, b0 = −0.1, and b1 = 1. Here, the soliton solution
is the singular type for all values of fractional order β. For various arbitrary values of
the parameters, we obtain additional different graphics even though they have similar
meanings. Therefore, for brevity, a few solutions are presented.

## PDF page 15

Fractal Fract. 2024, 8, x FOR PEER REVIEW

17 of 20

Fractal Fract. 2024, 8, 627

15 of 18

Fractal Fract. 2024, 8, x FOR PEER REVIEW

15 of 18

(a) For 𝛽 → 0.04.

(b) For 𝛽 → 0.2.

(c) For 𝛽 → 0.9.

(d) The 2D graph for different values of fractional order

(e) The 2D graph for different values of fractional order

𝛽.

𝛽.

Figure 9. Graphical presentation of the modulus of solution 𝑉 (𝑥, 𝑡) for 𝑘 = 1, 𝛼 = 0.1, 𝜎 = 1, 𝜆 =
1, 𝑙 = 4, 𝑡 = 1, 𝑏 = 1, and 𝑏 = 1.

In Figure 10, the modulus plot of 𝑉 (𝑥, 𝑡) is depicted for the values of the parame(e) The 2D graph for different values of fractional order
ters 𝑘 = 1, 𝛼 = 1, 𝑙 = 2, 𝜎 = −0.01, 𝜆 = 0.001, 𝑏 = −0.1, and 𝑏 = 1. Here, the soliton
𝛽.
𝛽.
solution
is the singular type for all values of fractional order
𝛽. For various arbitrary values
of
the
parameters,
we
obtain
additional
diﬀerent
graphics
even
they
have
𝑡)for
forkthough
𝑘==1,1,α 𝛼=
=0.1,
0.1,
1,λ𝜆=
=
Figure 9.
9. Graphical
Graphical presentation
presentation of
of the
the modulus
modulus of
of solution
solution V𝑉32 (𝑥,
Figure
(x,t)
σ𝜎==1,similar
meanings.
Therefore,
brevity, a few solutions are presented.
= 4,
4,t𝑡
= 1,
1,b𝑏0 =
= 1,
1,
and b𝑏1for
= 1.
1.
1,1,
l𝑙=
=
=

(d) The 2D graph for different values of fractional order

In Figure 10, the modulus plot of 𝑉 (𝑥, 𝑡) is depicted for the values of the parameters 𝑘 = 1, 𝛼 = 1, 𝑙 = 2, 𝜎 = −0.01, 𝜆 = 0.001, 𝑏 = −0.1, and 𝑏 = 1. Here, the soliton
solution is the singular type for all values of fractional order 𝛽. For various arbitrary values of the parameters, we obtain additional diﬀerent graphics even though they have similar meanings. Therefore, for brevity, a few solutions are presented.

Figure 10. Graphical presentation of the modulus plot of solution V33 ( x, t) for k = 1, α = 1, l = 2,
σ=
−1,10.λ =
0.001, b0 = −
0.1, andofb1the
= 1.
Figure
Graphical
presentation
modulus plot of solution 𝑉 (𝑥, 𝑡) for 𝑘 = 1, 𝛼 = 1, 𝑙 = 2,
𝜎 = −1, 𝜆 = 0.001, 𝑏 = −0.1, and 𝑏 = 1.

5. Comparison of the Results

In this section
the article, we compare the results obtained with those already
5. Comparison
of theofResults
available in the literature. In Table 1, we compare the results of the cubic-quintic-septicIn this section of the article, we compare the results obtained with those already availnonic equation with the results of Samir et al. [1]. This comparison helps us verify the
able in the literature. In Table 1, we compare the results of the cubic-quintic-septic-nonic
accuracy and reliability of this study. On the other hand, in Table 2, we compare the results
equation
the results
of Samir
et al.
[1]. This
helps
verify
accuracy
(𝑥, 𝑡)us
Figure 10.with
Graphical
presentation
of the
modulus
plotcomparison
of solution
forby
𝑘Mirzazadeh
= 1,the
𝛼=
1, 𝑙[39].
= 2,
obtained
for
the Davey–Stewartson
equation
with
the
results 𝑉
obtained
and
reliability
of
this
study.
On
the
other
hand,
in
Table
2,
we
compare
the
results
obtained
𝜎 = −1, 𝜆 = 0.001, 𝑏 = −0.1, and 𝑏 = 1.
The comparison demonstrates the accuracy of the obtained results and the effectiveness of
for the Davey–Stewartson equation with the results obtained by Mirzazadeh [39]. The
the method in solving complex equations.
comparison
demonstrates
the accuracy of the obtained results and the eﬀectiveness of the
5.
Comparison of
the Results
From the analysis of the information in Tables 1 and 2, it is clear that this study has
method
in
solving
complex
equations.
In this several
section of
the article,
compare
thefound
resultsinobtained
those already
availestablished
new
solutionswe
that
were not
previouswith
research.
Furthermore,
able in
thefocuses
literature.
1, we compare
results
of the
cubic-quintic-septic-nonic
this
study
on In Table
fractional-order
models, the
while
earlier
studies were based
on integerTable 1. Comparison of the results of the cubic-quintic-septic-nonic equation.
order models. As a result, the findings of this research could be useful to analyze data
transmission
systems.
Solutions Obtained by
the Present
Study
Solutions Obtained by Samir et al. [1]
(

𝑉 (𝑥, 𝑡) = 5 ⁄ 𝑒
𝐾
)
𝑙𝑛𝑙 Sech( (𝑥𝛼 + 2𝑎F)𝑙𝑛𝑙)𝑎
2𝛼
) ⁄

√𝑎𝑘𝑙
(
10√𝑎𝑘(1 + 𝑙 (

)

)𝑙𝑛𝑙 𝑏 − 4𝑖√5𝑎

𝑞(𝑥, 𝑡) = 𝑒 (
(

)
/

(𝑥 − 𝑣𝑡)]

(1 ± tanh [2

𝑏
(

)

.

## PDF page 16

Fractal Fract. 2024, 8, 627

16 of 18

Table 1. Comparison of the results of the cubic-quintic-septic-nonic equation.
Solutions Obtained by the Present Study
V11 ( x, t) = 51/4 e
(√

Solutions Obtained by Samir et al. [1]

1
− 16
ikE

x a
akl k( 2 + α F) ln l Sech

( K ( xα+2aF) ln l ) a2
) 2α
√ √
√ (
)
k( x + 2aF
α
10 ak 1+l
ln l b0 −4i 5a2 b4

)1/4

(

)1/4

(

3(w+ ak
b2

(
2

q( x, t) = ei(−kx+wt+θ )
[ √
] )1/4
w+ ak2
.
1 ± tanh 2
a ( x − vt )

3(w+ ak
b2

2

(

q( x, t) = ei(−kx+wt+θ )
] )1/4
[ √
2
.
1 ∓ tanh 2 w+aak ( x − vt)

1

V12 ( x, t) = 51/4 e− 16 ikE
(√

x a
akl k( 2 + α F) ln l cosech

( K ( xα+2aF) ln l ) a2
) 2α
√ √
√ (
2aF
10 ak 1+l k(x+ α ) ln l b0 −4i 5a2 b4
15
V21 ( x, t) = √

2

(

x

1/4 − 1 ikE

e

a

k
−iak2 l k( 2 + α F) sech( 2α
( xα+2aF ) ln l )(ln l )2
)
)
√
√ (
√
2aF
2a
−10i 1+l k(x+ α ) b2 +3 5 a b4 k −1+l k(x+ α F) ln l

)1/4

(

)1/4

(

(

15
V22 ( x, t) = √

2

(

x

3(w+ ak
b2

(
2

q( x, t) = ei(−kx+wt+θ )
[ √
] )1/4
2
.
1 ± coth 2 w+aak ( x − vt)

3(w+ ak
b2

(
2

q( x, t) = ei(−kx+wt+θ )
[ √
] )1/4
2
1 ∓ coth 2 w+aak ( x − vt)
.

16

1/4 − 1 ikE

e

16

a

k
−iak2 l k( 2 + α F) Cosch( 2α
( xα+2aF ) ln l )(ln l )2
(
)
)
√
√ (
√
2aF
2a
−10i 1+l k(x+ α ) b2 +3 5 a b4 k −1+l k(x+ α F) ln l

Table 2. Comparison of the results of the Davey–Stewartson (DS) equation.
Solutions Obtained by the Present Study
(
)
√
2 2
√ ln l σ −1+4α σ tanh ξ ln l
2
2 λ

(

U ( x, y, t) = ±eiη ( x,y,t)
)
√
2 2
2 σ ln a −1+λ4α σ csch(ξ ln l )

(
)
√
2 2
√ ln l σ −1+4α σ coth ξ ln l
2
2 λ

(

U ( x, y, t) = −eiη ( x,y,t)
√
(
))
−1+4α2 σ2 tanh ξ ln l
σ ln a
2
2
λ

V41 ( x, y, t) =
( √
)
√ √
√ √
iσ g ln l (2b0 +b1 )
2i λσ g ln l b03 +i λσ g ln l b20 b1 +h
√
+
2
b1
ξ
4λb b +2λb

(

U ( x, y, t) = −eiη ( x,y,t)
√
))
(
σ ln a
−1+4α2 σ2 coth ξ ln l
2
2
λ

β
i (αx +y+ k (t+ 1 ) +n)
β
Γ( β)

V31 ( x, y, t) =

ie

V32 ( x, y, t) =

ie

β
i (αx +y+ k (t+ 1 ) +n)
β
Γ( β)

iϕ[ x,y,t]

e
b0 +

Solutions Obtained by Mirzazadeh [39]

1+ l ξ

iϕ[ x,y,t]

e
b
b0 + 1 ξ
1− l

2(1+ l ) λ

0 1

1

V42 ( x, y, t) =
)
√ √
√ √
2 λσ g ln l b03 +i λσ g ln l b02 b1 +h
σ g ln l (2b0 +b1 )
√
−
4λb0 b1 +2λb12
2(−1+l ξ ) λ

( √

No such solution found.

6. Conclusions
In this study, we investigated two nonlinear time-fractional models, namely the cubicquintic-septic-nonic equation and the Davey–Stewartson (DS) equation, using the extended
generalized Kudryashov technique, and found some fresh and typical solutions. The
fractional derivative is considered in the sense of a beta derivative since it follows all
the characteristics of the classical derivative. The solutions obtained revealed a range of
rich structured solitons, including bell-shaped, parabolic, cuspon, anti-bell-shaped, and
singular solitons. The 3D and 2D graphs show that the fractional-order derivative significantly impacts soliton dynamics and offers new insights into the behavior of nonlinear
models. The beta fractional derivative is important because it offers a balance between
simplicity and the ability to generalize classical integer-order derivative, has an impact on
fractional dynamics on soliton solutions in nonlinear models, and provides new insights
into maintaining the mathematically manageable structure. This study demonstrates the
effectiveness of fractional derivatives in expanding the understanding of complex nonlinear
systems, which could be applied in future studies to other fractional models in fields such
as optical fiber communication and plasma physics.

## PDF page 17

Fractal Fract. 2024, 8, 627

17 of 18

Author Contributions: M.I.A. and T.I.: Conceptualization, Methodology, Investigation, Formal
analysis, Visualization, Software, Validation, Resources, Writing—original draft. M.A.A. and M.S.O.:
Data Curation, Project administration, Supervision, Funding acquisition, Writing—review editing.
All authors have read and agreed to the published version of the manuscript.
Funding: This research received no external funding.
Data Availability Statement: The original contributions presented in the study are included in the
article, further inquiries can be directed to the corresponding authors.
Acknowledgments: The authors sincerely thank the anonymous reviewers for their valuable comments and suggestions, which have helped improve the article.
Conflicts of Interest: The authors have no conflicts of interest to declare that are relevant to the
content of this article.

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

Samir, I.; Arnous, A.H.; Yıldırım, Y.; Biswas, A.; Moraru, L.; Moldovanu, S. Optical solitons with cubic-quantic-septic-nonic
nonlinear and quadrupled power-law nonlinearity: An observation. Mathematics 2022, 10, 4085. [CrossRef]
Ding, C.C.; Zhou, Q.; Triki, H.; Sun, Y.; Biswas, A. Dynamics of dark and anti-dark solitons for the x-nonlocal Davey-Stewartson
II equation. Nonlinear Dyn. 2023, 111, 2621–2629. [CrossRef]
Ross, B. Fractional Calculus: An Introduction to the Theory and Applications of Fractional Differential Equations; John Wiley & Sons:
New York, NY, USA, 1977.
Miller, K.S.; Ross, B. An Introduction to the Fractional Calculus and Fractional Differential Equations; John Wiley & Sons: New York,
NY, USA, 1993.
Jumarie, G. Table of some basic fractional calculus formulae derived from a modified Riemann-Liouville derivative for nondifferentiable functions. Appl. Math. Lett. 2009, 22, 378–385. [CrossRef]
Raza, N.; Osman, M.S.; Abdel-Aty, A.H.; Abdel-Khalek, S.; Besbes, H.R. Optical solitons of space-time fractional Fokas–Lenells
equation with two versatile integration architectures. Adv. Differ. Equ. 2020, 2020, 517. [CrossRef]
Almeida, R. A Caputo fractional derivative of a function with respect to another function. Commun. Nonlinear Sci. Numer. Simul.
2017, 44, 460–481. [CrossRef]
Atangana, A.; Baleanu, D.; Alsaedi, A. Analysis of time-fractional Hunter-Saxton equation: A model of neumatic liquid crystal.
Open Phys. 2016, 14, 145–149. [CrossRef]
Atangana, A.; Alkahtani, B.S.T. Modeling the spread of Rubella disease using the concept of with local derivative with fractional
parameter: Beta-derivative. Complexity 2016, 21, 442–451. [CrossRef]
Atangana, A.; Alqahtani, R.T. Modelling the spread of River blindness disease via the Caputo fractional derivative and the
β-derivative. Entropy 2016, 18, 40. [CrossRef]
Volkan, A. Exact solutions of nonlinear time fractional Schrödinger equation with beta-derivative. Fundam. Contemp. Math. Sci.
2023, 4, 1–8.
Mahak, N.; Akram, G. The modified auxiliary equation method to investigate solutions of the perturbed nonlinear Schrödinger
equation with Kerr law nonlinearity. Optik 2020, 207, 164467. [CrossRef]
Islam, M.E.; Barman, H.K.; Akbar, M.A. Search for interactions of phenomena described by the coupled Higgs field equation
through analytical solutions. Opt. Quant. Electron. 2020, 52, 468. [CrossRef]
Haq, E.U.; Ali, M.; Khan, A.S. On the solution of fractional Riccati differential equations with variation of parameters method.
Engg. Appl. Sci. Lett. 2020, 3, 1–9.
Fadugba, S.E.; Oluwayemi, M.O.; Ajayi, A.O.; Faweya, O.; Okunlola, J.T.; Kekana, M. Fractional reduced differential transform
method for solving fractional order measles model. In Proceedings of the 2023 International Conference on Science, Engineering
and Business for Sustainable Development Goals (SEB-SDG), Omu-Aran, Nigeria, 5–7 April 2023.
Ali, R.; Tag-eldin, E. A comparative analysis of generalized and extended (G′ /G)-expansion methods for travelling wave solutions
of fractional Maccari’s system with complex structure. Alex. Eng. J. 2023, 79, 508–530. [CrossRef]
Çulha Ünal, S. Exact solutions of the Landau-Ginzburg-Higgs equation utilizing the Jacobi elliptic functions. Opt. Quant. Electron.
2024, 56, 1027. [CrossRef]
Korkmaz, A.; Hepson, O.E.; Hosseini, K.; Rezazadeh, H.; Eslami, M. Sine-Gordon expansion method for exact solutions to
conformable time fractional equations in RLW-class. J. King Saud. Univ. Sci. 2020, 32, 567–574. [CrossRef]
Mamun, A.A.; Lu, C.; Ananna, S.N.; Uddin, M.M. Rational sine-Gordon expansion method to analyze the dynamical behavior of
the time-fractional Phi-four and (2+1)- dimensional CBS equations. Sci. Rep. 2024, 14, 9473. [CrossRef]
Kumar, S.; Dhiman, S.K.; Baleanu, D.; Osman, M.S.; Wazwaz, A.M. Lie symmetries, closed-form solutions, and various dynamical
profiles of solitons for the variable coefficient (2 + 1)-dimensional KP equations. Symmetry 2022, 14, 597. [CrossRef]
Akinyemi, L.; Şenol, M.; Osman, M.S. Analytical and approximate solutions of nonlinear Schrödinger equation with higher
dimension in the anomalous dispersion regime. J. Ocean Eng. Sci. 2022, 7, 143–154. [CrossRef]

## PDF page 18

Fractal Fract. 2024, 8, 627

22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.

18 of 18

Umar, T.; Hosseini, K.; Kaymakamzade, B.; Boulaaras, S.; Osman, M.S. Hirota D-operator forms, multiple soliton waves, and
other nonlinear patterns of a 2D generalized Kadomtsev–Petviashvili equation. Alex. Eng. J. 2024, 108, 999–1010. [CrossRef]
Chen, Y.; Fan, E.; Yuen, M. The Hopf-Cole transformation, topological solitons and multiple fusion solutions for the n-dimensional
Burgers system. Phys. Lett. A 2016, 380, 9–14. [CrossRef]
Tasnim, F.; Akbar, M.A.; Osman, M.S. The extended direct algebraic method for extracting analytical solitons solutions to the
cubic nonlinear Schrödinger equation involving beta derivatives in space and time. Fractal Fract. 2023, 7, 426. [CrossRef]
Akbar, M.A.; Ali, N.H.M. The improved F-expansion method with Riccati equation and its applications in mathematical physics.
Cogent Math. 2017, 4, 1282577. [CrossRef]
Wazwaz, A.M. The variational iteration method for solving linear and nonlinear ODEs and scientific models with variable
coefficients. Cent. Eur. J. Eng. 2014, 4, 64–71. [CrossRef]
Irshad, A.; Mohyud-Din, S.T.; Ahmed, N.; Khan, U. A new modification in simple equation method and its applications on
nonlinear equations of physical nature. Results Phys. 2017, 7, 4232–4240. [CrossRef]
Hasan, F.L. First integral method for constructing new exact solutions of the important nonlinear evolution equations in physics.
J. Phys. Conf. Ser. 2020, 1530, 012109. [CrossRef]
Elsaid, A. Adomian polynomials: A powerful tool for iterative methods of series solution of nonlinear equations. J. Appl. Anal.
Comput. 2012, 2, 381–394. [CrossRef]
Jiang, J.; Feng, Y.; Li, S. Improved fractional subequation method and exact solutions to fractional partial differential equations. J.
Funct. Spaces 2020, 2020, 5840920. [CrossRef]
Liu, F.; Feng, Y. The modified generalized Kudryashov method for nonlinear space-time fractional partial differential equations of
Schrödinger type. Results Phys. 2023, 53, 106914. [CrossRef]
Bekir, A.; Guner, O.; Cevikel, A. The exp-function method for some time-fractional differential equations. IEEE/CAA J. Autom. Sin.
2017, 4, 315–321. [CrossRef]
Bagley, R.L.; Torvik, P.J. On the appearance of the fractional derivative in the behavior of real materials. J. Appl. Mech. 1984, 51,
294–298.
Bhalekar, S. Fractional Calculus: Theory and Applications, 1st ed.; Chaos in fractional order systems; Narosa Publishing House: New
Delhi, India, 2013; Chapter 4.
Du, M.; Wang, Z.; Hu, H. Measuring memory with the order of fractional derivative. Sci. Rep. 2013, 3, 3431. [CrossRef] [PubMed]
Tarasov, V.E. Remark to history of fractional derivatives on complex plane: Sonine-Letnikov and Nishimoto derivatives. Fract.
Diff. Cal. 2016, 6, 147–149. [CrossRef]
Luchko, Y. Fractional derivatives and the fundamental theorem of fractional calculus. Fract. Calc. Appl. Anal. 2020, 23, 939–966.
[CrossRef]
Jisha, C.R.; Jang, B. Novel insights into the exact solutions of the modified (3 + 1) dimensional fractional KS equation with variable
coefficients. Nonlinear Dyn. 2024, 112, 7325–7345. [CrossRef]
Mirzazadeh, M. Soliton solutions of Davey-Stewartson equation by trial equation method and ansatz approach. Nonlinear Dyn.
2015, 82, 1775–1780. [CrossRef]

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
