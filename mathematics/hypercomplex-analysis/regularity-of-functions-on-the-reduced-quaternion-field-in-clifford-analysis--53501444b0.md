Source: https://doi.org/10.1155/2014/654798
PDF sha256: 53501444b0c5459f6590ce87d62ee419cc91617a3e83bea6f405a2353b980993
License: https://creativecommons.org/licenses/by/3.0/
Language: eng
Fidelity: machine-gated

# Transcription of regularity-of-functions-on-the-reduced-quaternion-field-in-clifford-analysis--53501444b0.pdf

Transcription of `regularity-of-functions-on-the-reduced-quaternion-field-in-clifford-analysis--53501444b0.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Hindawi Publishing Corporation
Abstract and Applied Analysis
Volume 2014, Article ID 654798, 8 pages
http://dx.doi.org/10.1155/2014/654798

Research Article
Regularity of Functions on the Reduced Quaternion
Field in Clifford Analysis
Ji Eun Kim, Su Jin Lim, and Kwang Ho Shon
Department of Mathematics, Pusan National University, Busan 609-735, Republic of Korea
Correspondence should be addressed to Kwang Ho Shon; khshon@pusan.ac.kr
Received 11 December 2013; Revised 12 February 2014; Accepted 18 February 2014; Published 20 March 2014
Academic Editor: Junesang Choi
Copyright © 2014 Ji Eun Kim et al. This is an open access article distributed under the Creative Commons Attribution License,
which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.
We define a new hypercomplex structure of R3 and a regular function with values in that structure. From the properties of regular
functions, we research the exponential function on the reduced quaternion field and represent the corresponding Cauchy-Riemann
equations in hypercomplex structures of R3 .

1. Introduction
Meglihzon [1], Sudbery [2], and Fueter [3] demonstrated that
there are three possible approaches (the Cauchy approach,
Weierstrass approach, and Riemann approach) in the theories
of functions that would generalize holomorphic functions
with respect to several complex variables. Sudbery [2], Soucek
[4], and Sommen [5] attempted to research the Cauchy
approach using differential forms and differential operators
in Clifford analysis. Fueter [3] and Naser [6] studied the
properties of quaternionic differential equations as a generalization of the extended Cauchy-Riemann equations in
the complex holomorphic function theory. Nôno [7–9] and
Sudbery [2] gave a definition and the development of regular
functions over the quaternion field. Ryan [10, 11] developed
the theories of regular functions in a complex Clifford analysis using a generalization of the Cauchy-Riemann equation.
Malonek [12] considered analogously the function theory
of hypercomplex variables. He defined the hypercomplex
differentiability for the existence of a function over the
Clifford algebra and monogenicity based on a generalized
Cauchy-Riemann system. Gotô and Nôno [13] and Koriyama
et al. [14] dealt with differential operators with the derivative
of regular functions in quaternion.
We shall denote by C, R, and Z, respectively, the field
of complex numbers, the field of real numbers, and the
set of all integers. We [15, 16] showed that any complexvalued harmonic function 𝑓1 in a pseudoconvex domain

𝐷 of C2 × C2 has a hyperconjugate harmonic function 𝑓2
in 𝐷 such that the quaternion-valued function 𝑓1 + 𝑓2 𝑗 is
hyperholomorphic in 𝐷 and gave a regeneration theorem
in quaternion analysis in the view of complex and Clifford
analysis. Further, we [17, 18] investigated the existence of the
hyperconjugate harmonic functions of the octonion number
system and some properties of dual quaternion functions.
In this paper, we introduce the Fueter variables on R3 and
investigate a hypercomplex structure of R3 . We define regular
functions and obtain the representation of the corresponding
Cauchy-Riemann equations for regular functions in the
reduced quaternion field.

2. Preliminaries
A three-dimensional, noncommutative, and associative real
field, called a ternary number system, is constructed by three
base elements 𝑒0 , 𝑒1 , and 𝑒2 which satisfy
𝑒02 = 1,

𝑒12 = 𝑒22 = −1,

𝑒0 = 𝑒0 ,

𝑒𝑟 = −𝑒𝑟

𝑒1 𝑒2 = −𝑒2 𝑒1 ,

(𝑟 = 1, 2) .

(1)

In addition, let 𝑒0 be the identity of a ternary number system
and 𝑒1 identifies the imaginary unit √−1 in the complex field,
and
C (T) := {𝑧 = 𝑒1 𝑧1 + 𝑒2 𝑧2 | 𝑧1 , 𝑧2 ∈ C} ,

(2)

## PDF page 2

2

Abstract and Applied Analysis

where 𝑧𝑟 = 𝑥𝑟 − (1/2)𝑒𝑟 𝑥0 (𝑟 = 1, 2) and 𝑥𝑚 (𝑚 = 0, 1, 2) are
real variables. They satisfy the equations
𝑧𝑟 𝑤𝑘 = 𝑤𝑘 𝑧𝑟

(𝑟 ≠ 𝑘) ,

(3)

where 𝑧𝑟 = 𝑥𝑟 + (1/2)𝑒𝑟 𝑥0 (𝑟 = 1, 2), 𝑤𝑘 = 𝑦𝑘 − (1/2)𝑒𝑘 𝑦0 ,
𝑤𝑘 = 𝑦𝑘 + (1/2)𝑒𝑘 𝑦0 (𝑘 = 1, 2), and 𝑦𝑚 (𝑚 = 0, 1, 2) are real
variables.
For any two elements 𝑧 = 𝑒1 𝑧1 + 𝑒2 𝑧2 and 𝑤 = 𝑒1 𝑤1 + 𝑒2 𝑤2
of C(T), their product is given by
𝑧𝑤 = 𝑧 ∙ 𝑤 + 𝑧 ⊙ 𝑤,

(4)

where the corresponding commutative inner product ∙ satisfies
1
𝑧 ∙ 𝑤 = (𝑧𝑤 + 𝑤𝑧)
2
(5)
2
1
= −∑𝑧𝑟 𝑤𝑟 + 𝑒1 𝑒2 (𝑧1 𝑤2 − 𝑤2 𝑧1 + 𝑤1 𝑧2 − 𝑧2 𝑤1 )
2
𝑟=1
and the corresponding noncommutative outer product ⊙
satisfies
1
𝑧 ⊙ 𝑤 = (𝑧𝑤 − 𝑤𝑧)
2
1
= 𝑒1 𝑒2 (𝑧1 𝑤2 + 𝑤2 𝑧1 − 𝑤1 𝑧2 − 𝑧2 𝑤1 )
2

(6)

= −𝑤 ⊙ 𝑧.
The conjugation 𝑧∗ , the corresponding norm |𝑧|, and the
inverse 𝑧−1 of 𝑧 in C(T) are given by
𝑧∗ = 𝑒1 𝑧1 + 𝑒2 𝑧2 ,
2

𝑟=1

(8)

Theorem 1. Let 𝑧 be an arbitrary number in C(T). Then the
corresponding exponential function exp(𝑧) of 𝑧 in C(T) is given
as
𝑘

if 𝑥1 = 𝑘𝜋,
(9)
if 𝑥2 = 𝑡𝜋,

where 𝑘, 𝑡 ∈ Z.
Furthermore, as hyperbolic functions, one has
exp (𝑧)
𝑘
{
{ (−1) exp (𝑒2 𝑥2 ) (cosh (𝑥0 ) − sinh (𝑥0 )) , if 𝑥1 = 𝑘𝜋,
={
{
𝑡
{ (−1) exp (𝑒1 𝑥1 ) (cosh (𝑥0 ) − sinh (𝑥0 )) , if 𝑥2 = 𝑡𝜋,
(10)

where 𝑘, 𝑡 ∈ Z.

Since a scalar part of 𝑒1 𝑧1 is (1/2)𝑥0 , a vector part of 𝑒1 𝑧1 is
𝑒1 𝑥1 , and |𝑒1 | = 1, by [19],
𝑥
𝑒𝑥
󵄨
󵄨
󵄨
󵄨
exp (𝑒1 𝑧1 ) = exp ( 0 ) {cos (󵄨󵄨󵄨𝑒1 𝑥1 󵄨󵄨󵄨) + 󵄨󵄨 1 1 󵄨󵄨 sin (󵄨󵄨󵄨𝑒1 𝑥1 󵄨󵄨󵄨)}
2
󵄨󵄨𝑒1 𝑥1 󵄨󵄨
𝑥
= exp ( 0 ) {cos (𝑥1 ) + 𝑒1 sin (𝑥1 )}
2
(12)
and, similarly, we have
𝑥
𝑒𝑥
󵄨
󵄨
󵄨
󵄨
exp (𝑒2 𝑧2 ) = exp ( 0 ) {cos (󵄨󵄨󵄨𝑒2 𝑥2 󵄨󵄨󵄨) + 󵄨󵄨 2 2 󵄨󵄨 sin (󵄨󵄨󵄨𝑒2 𝑥2 󵄨󵄨󵄨)}
2
󵄨󵄨𝑒2 𝑥2 󵄨󵄨
𝑥
= exp ( 0 ) {cos (𝑥2 ) + 𝑒2 sin (𝑥2 )} .
2
(13)
Then we have
𝑥
exp (𝑧) = exp ( 0 ) {cos (𝑥1 ) + 𝑒1 sin (𝑥1 )}
2
𝑥
× exp ( 0 ) {cos (𝑥2 ) + 𝑒2 sin (𝑥2 )}
2
= exp (𝑥0 ) {cos (𝑥1 ) + 𝑒1 sin (𝑥1 )}

(7)

𝑧
(𝑧 ≠ 0) .
|𝑧|2
For any element 𝑧 in C(T), we have the corresponding
exponential function 𝑒𝑧 denoted by
exp (𝑧) = exp (𝑒1 𝑧1 + 𝑒2 𝑧2 ) .

(11)

(14)

= exp (𝑥0 ) {cos (𝑥1 ) cos (𝑥2 ) + 𝑒2 cos (𝑥1 )

∗

(−1) exp (𝑥0 ) exp (𝑒2 𝑥2 ) ,
{
{
exp (𝑧) = {
{
𝑡
{(−1) exp (𝑥0 ) exp (𝑒1 𝑥1 ) ,

exp (𝑧) = exp (𝑒1 𝑧1 + 𝑒2 𝑧2 ) = exp (𝑒1 𝑧1 ) exp (𝑒2 𝑧2 ) .

× {cos (𝑥2 ) + 𝑒2 sin (𝑥2 )}

|𝑧|2 = 𝑧𝑧∗ = 𝑧 ∙ 𝑧∗ = ∑𝑧𝑟 𝑧𝑟 ,
𝑧−1 =

Proof. For any element 𝑧 = 𝑒1 𝑧1 + 𝑒2 𝑧2 of C(T),

× sin (𝑥2 ) + 𝑒1 sin (𝑥1 ) cos (𝑥2 )}
+ exp (𝑥0 ) 𝑒1 𝑒2 sin (𝑥1 ) sin (𝑥2 ) .
Also, we obtain
exp (𝑧) = exp (𝑒2 𝑧2 + 𝑒1 𝑧1 )
= exp (𝑒2 𝑧2 ) exp (𝑒1 𝑧1 )
= exp (𝑥0 ) {cos (𝑥2 ) + 𝑒2 sin (𝑥2 )}
× {cos (𝑥1 ) + 𝑒1 sin (𝑥1 )}

(15)

= exp (𝑥0 ) {cos (𝑥1 ) cos (𝑥2 ) + 𝑒2 cos (𝑥1 )
× sin (𝑥2 ) + 𝑒1 sin (𝑥1 ) cos (𝑥2 )}
+ exp (𝑥0 ) 𝑒2 𝑒1 sin (𝑥1 ) sin (𝑥2 ) .
Since (15) has to be equal to (14), sin (𝑥1 ) sin (𝑥2 ) = 0, that is,
sin (𝑥1 ) = 0 or sin (𝑥2 ) = 0. Therefore, 𝑥1 = 𝑘𝜋 or 𝑥2 = 𝑡𝜋,
and then cos (𝑥1 ) = (−1)𝑘 or cos (𝑥2 ) = (−1)𝑡 , where 𝑘, 𝑡 ∈ Z.
If 𝑥1 = 𝑘𝜋 (𝑘 ∈ Z), then
exp (𝑧) = exp (𝑥0 ) {(−1)𝑘 (cos (𝑥2 ) + 𝑒2 sin (𝑥2 ))}
= (−1)𝑘 exp (𝑥0 ) exp (𝑒2 𝑥2 ) .

(16)

## PDF page 3

Abstract and Applied Analysis

3
= (cos (𝑥1 ) + 𝑒1 sin (𝑥1 )) (cos (𝑥2 ) + 𝑒2 sin (𝑥2 ))

Similarly, if 𝑥2 = 𝑡𝜋 (𝑡 ∈ Z), then

2
𝑥
𝑥
× (cosh ( 0 ) − sinh ( 0 )) .
2
2

𝑡

exp (𝑧) = exp (𝑥0 ) {(−1) (cos (𝑥1 ) + 𝑒1 sin (𝑥1 ))}
= (−1)𝑡 exp (𝑥0 ) exp (𝑒1 𝑥1 ) .

(17)

(19)

Since
Further, by the Euler formula and the addition rule of
trigonometric functions,
exp (𝑧) = exp (𝑒1 𝑧1 + 𝑒2 𝑧2 ) = exp (𝑒1 𝑧1 ) exp (𝑒2 𝑧2 )
= (cos (𝑧1 ) + 𝑒1 sin (𝑧1 )) (cos (𝑧2 ) + 𝑒2 sin (𝑧2 ))
𝑥0
𝑥
) + sin (𝑥1 ) sin (𝑒1 0 )
2
2
𝑥
+ 𝑒1 (sin (𝑥1 ) cos (𝑒1 0 )
2
𝑥
− cos (𝑥1 ) sin (𝑒1 0 ))}
2
𝑥
𝑥
⋅ {cos (𝑥2 ) cos (𝑒2 0 ) + sin (𝑥2 ) sin (𝑒2 0 )
2
2
𝑥0
+ 𝑒2 (sin (𝑥2 ) cos (𝑒2 )
2
𝑥
− cos (𝑥2 ) sin (𝑒2 0 ))} .
2
(18)

= {cos (𝑥1 ) cos (𝑒1

Since cos (𝑒𝑟 (𝑥0 /2)) = cosh (𝑥0 /2) and sin (𝑒𝑟 (𝑥0 /2)) =
𝑒𝑟 sinh (𝑥0 /2) (𝑟 = 1, 2), we have
𝑥
𝑥
exp (𝑧) = {cos (𝑥1 ) cosh ( 0 ) + 𝑒1 sin (𝑥1 ) sinh ( 0 )
2
2
𝑥
+ 𝑒1 (sin (𝑥1 ) cosh ( 0 )
2
𝑥
−𝑒1 cos (𝑥1 ) sinh ( 0 ))}
2
𝑥
𝑥
⋅ {cos (𝑥2 ) cosh ( 0 ) + 𝑒2 sin (𝑥2 ) sinh ( 0 )
2
2
𝑥0
+ 𝑒2 (sin (𝑥2 ) cosh ( )
2
𝑥
−𝑒2 cos (𝑥2 ) sinh ( 0 ))}
2
= { (cos (𝑥1 ) + 𝑒1 sin (𝑥1 ))
𝑥
𝑥
× (cosh ( 0 ) − sinh ( 0 ))}
2
2
× { (cos (𝑥2 ) + 𝑒2 sin (𝑥2 ))
𝑥
𝑥
× (cosh ( 0 ) − sinh ( 0 ))}
2
2

2
𝑥
𝑥
(cosh ( 0 ) − sinh ( 0 ))
2
2
𝑥
𝑥
𝑥
𝑥
= cosh2 ( 0 ) + sinh2 ( 0 ) − 2cosh2 ( 0 ) sinh2 ( 0 )
2
2
2
2

=1+2

cosh (𝑥0 ) − 1
− sinh (𝑥0 )
2

= cosh (𝑥0 ) − sinh (𝑥0 ) ,
(20)
we obtain
exp (𝑧) = exp (𝑒1 𝑧1 ) exp (𝑒2 𝑧2 ) = (cos (𝑥1 ) + 𝑒1 sin (𝑥1 ))
× (cos (𝑥2 ) + 𝑒2 sin (𝑥2 )) (cosh (𝑥0 ) − sinh (𝑥0 ))
(21)
and, similarly,
exp (𝑧) = exp (𝑒2 𝑧2 ) exp (𝑒1 𝑧1 ) = (cos (𝑥2 ) + 𝑒2 sin (𝑥2 ))
× (cos (𝑥1 ) + 𝑒1 sin (𝑥1 )) (cosh (𝑥0 ) − sinh (𝑥0 )) .
(22)
Since (22) has to be equal to (21), sin (𝑥1 ) sin (𝑥2 ) = 0, that is,
sin (𝑥1 ) = 0 or sin (𝑥2 ) = 0. Therefore, 𝑥1 = 𝑘𝜋 or 𝑥2 = 𝑡𝜋,
and then cos (𝑥1 ) = (−1)𝑘 or cos (𝑥2 ) = (−1)𝑡 , where 𝑘, 𝑡 ∈ Z.
If 𝑥1 = 𝑘𝜋 (𝑘 ∈ Z), then
exp (𝑧) = (cos (𝑥2 ) + 𝑒2 sin (𝑥2 ))
× (−1)𝑘 (cosh (𝑥0 ) − sinh (𝑥0 ))

(23)

= (−1)𝑘 exp (𝑒2 𝑥2 ) (cosh (𝑥0 ) − sinh (𝑥0 )) .
Similarly, if 𝑥2 = 𝑡𝜋 (𝑡 ∈ Z), then
exp (𝑧) = (cos (𝑥1 ) + 𝑒1 sin (𝑥1 ))
× (−1)𝑡 (cosh (𝑥0 ) − sinh (𝑥0 ))

(24)

= (−1)𝑡 exp (𝑒1 𝑥1 ) (cosh (𝑥0 ) − sinh (𝑥0 )) .
Remark 2. By Theorem 1 and the properties of the Euler
formula, if 𝑥1 = 𝑘𝜋, then we can write
exp (𝑧) = (−1)𝑘 exp (𝑒2 𝑥2 ) (cosh (𝑥0 ) − sinh (𝑥0 ))
= (−1)𝑘 exp (𝑒2 𝑥2 − 𝑥0 ) = (−1)𝑘 exp (𝑒2 𝐹2 ) ,

(25)

## PDF page 4

4

Abstract and Applied Analysis
𝜕𝑓
𝜕
𝜕
= (𝑒1
+ 𝑒2
) (𝑒1 𝑓1 + 𝑒2 𝑓2 )
𝜕𝐴∗
𝜕𝑧1
𝜕𝑧2

also, if 𝑥2 = 𝑡𝜋, then
exp (𝑧) = (−1)𝑡 exp (𝑒1 𝑥1 ) (cosh (𝑥0 ) − sinh (𝑥0 ))
𝑡

𝑡

= (−1) exp (𝑒1 𝑥1 − 𝑥0 ) = (−1) exp (𝑒1 𝐹1 ) ,

=−

(26)

where 𝑘, 𝑡 ∈ Z and 𝐹𝑟 = 𝑥𝑟 + 𝑒𝑟 𝑥0 (𝑟 = 1, 2) are the conjugate
Fueter variables of 𝐹𝑟 = 𝑥𝑟 − 𝑒𝑟 𝑥0 (𝑟 = 1, 2) (see [20]).

𝑓

𝜕
𝜕
𝜕
− 𝑒2
)
= (𝑒1 𝑓1 + 𝑒2 𝑓2 ) (−𝑒1
𝜕𝐴
𝜕𝑧1
𝜕𝑧2
= 𝑓1

Let Ω be an open subset of R3 and let a function 𝑓(𝑎) be
defined by the following form on Ω with values in C(T):
𝑓 : Ω 󳨀→ C (T) ,

𝑓

𝑎 = (𝑥0 , 𝑥1 , 𝑥2 ) ∈ Ω 󳨃󳨀→ 𝑓 (𝑎) = 𝑒1 𝑓1 (𝑥0 , 𝑥1 , 𝑥2 )
+ 𝑒2 𝑓2 (𝑥0 , 𝑥1 , 𝑥2 ) ∈ C (T) ,

= −𝑓1

where 𝑓𝑟 = 𝑢𝑟 − (1/2)𝑒𝑟 𝑢0 , 𝑓𝑟 = 𝑢𝑟 + (1/2)𝑒𝑟 𝑢0 (𝑟 = 1, 2) and
𝑢𝑚 (𝑚 = 0, 1, 2) are real-valued functions.
From the chain rule, we use the following differential
operators:

𝜕
𝜕
𝜕
𝜕
𝜕
𝜕
1
1
=2
+ 𝑒
+ 𝑒
= 𝑒1
+ 𝑒2
,
𝜕𝐴∗
𝜕𝑥0 2 1 𝜕𝑥1 2 2 𝜕𝑥2
𝜕𝑧1
𝜕𝑧2
(29)

(32)

𝜕
𝜕
𝜕
= (𝑒1 𝑓1 + 𝑒2 𝑓2 ) (𝑒1
+ 𝑒2
)
∗
𝜕𝐴
𝜕𝑧1
𝜕𝑧2

(28)

𝜕
𝜕
𝜕
𝜕
1
1
𝜕
𝜕
− 𝑒
− 𝑒
= −𝑒1
− 𝑒2
,
:= 2
𝜕𝐴
𝜕𝑥0 2 1 𝜕𝑥1 2 2 𝜕𝑥2
𝜕𝑧1
𝜕𝑧2

𝜕
𝜕
𝜕
𝜕
+ 𝑓2
+ 𝑒1 𝑒2 (𝑓2
− 𝑓1
)
𝜕𝑧1
𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
= 1 + 2 + 𝑒1 𝑒2 {( 2 ) − ( 1 )} ,
𝜕𝑧1 𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

(27)

satisfying

𝜕𝑓1 𝜕𝑓2
𝜕𝑓
𝜕𝑓
−
+ 𝑒1 𝑒2 ( 2 − 1 ) ,
𝜕𝑧1 𝜕𝑧2
𝜕𝑧1 𝜕𝑧2

=−

𝜕
𝜕
𝜕
𝜕
− 𝑓2
+ 𝑒1 𝑒2 (𝑓1
− 𝑓2
)
𝜕𝑧1
𝜕𝑧2
𝜕𝑧2
𝜕𝑧1

𝜕𝑓
𝜕𝑓
𝜕𝑓1 𝜕𝑓2
−
+ 𝑒1 𝑒2 {( 1 ) − ( 2 )} .
𝜕𝑧1 𝜕𝑧2
𝜕𝑧2
𝜕𝑧1

Thus, we have a corresponding Laplacian in the reduced
quaternion C(T):

Δ𝑎 =

𝜕2
𝜕2
1 𝜕2
1 𝜕2
𝜕2
=
+
+
.
=
4
𝜕𝐴𝜕𝐴∗ 𝜕𝐴∗ 𝜕𝐴
𝜕𝑥02 4 𝜕𝑥12 4 𝜕𝑥22

(33)

where
𝜕
𝜕
1 𝜕
=
+ 𝑒1
,
𝜕𝑧1 2 𝜕𝑥1
𝜕𝑥0

𝜕
𝜕
1 𝜕
=
+ 𝑒2
,
𝜕𝑧2 2 𝜕𝑥2
𝜕𝑥0

𝜕
𝜕
1 𝜕
=
− 𝑒1
,
𝜕𝑧1 2 𝜕𝑥1
𝜕𝑥0

𝜕
𝜕
1 𝜕
=
− 𝑒2
𝜕𝑧2 2 𝜕𝑥2
𝜕𝑥0

Remark 3. Let Ω be an open set of R3 . From the definition of
the differential operators in C(T), we have
(30)
𝜕𝑓
𝜕
𝜕
𝜕
1 𝜕𝑓
+ 𝑓2
)
∙ 𝑓 = ( 1 + 2 + 𝑓1
𝜕𝐴
2 𝜕𝑧1 𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

in C(T). We have the following equations:
𝑓𝑟

𝜕𝑓
𝜕
= 𝑟,
𝜕𝑧𝑟 𝜕𝑧𝑟

𝑓𝑟

𝜕𝑓
𝜕
= 𝑟
𝜕𝑧𝑟 𝜕𝑧𝑟

𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
+ 𝑒1 𝑒2 (𝑓2
− 2 + 1 − 𝑓1
)
2
𝜕𝑧1 𝜕𝑧1 𝜕𝑧2
𝜕𝑧2

(𝑟 = 1, 2) ,

𝜕𝑓
𝜕
𝑓1
= ( 1 ),
𝜕𝑧2
𝜕𝑧2

𝜕𝑓
𝜕
𝑓2
= ( 2 ),
𝜕𝑧1
𝜕𝑧1

𝜕𝑓
𝜕
𝑓1
= ( 1 ),
𝜕𝑧2
𝜕𝑧2

𝜕𝑓
𝜕
𝑓2
= ( 2 ),
𝜕𝑧1
𝜕𝑧1

and then, the operator 𝜕/𝜕𝐴 operates to 𝑓 as follows:

(31)

=

𝜕𝑓1 𝜕𝑓2 1
+
+ 𝑒𝑒
𝜕𝑧1 𝜕𝑧2 2 1 2
× {(

𝜕𝑓2
𝜕𝑓
𝜕𝑓
𝜕𝑓
) − ( 1) − 2 + 1},
𝜕𝑧1
𝜕𝑧2
𝜕𝑧1 𝜕𝑧2

𝜕𝑓
𝜕
𝜕
𝜕
1 𝜕𝑓
− 𝑓2
)
⊙ 𝑓 = ( 1 + 2 − 𝑓1
𝜕𝐴
2 𝜕𝑧1 𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

𝜕𝑓
𝜕
𝜕
− 𝑒2
) (𝑒1 𝑓1 + 𝑒2 𝑓2 )
= (−𝑒1
𝜕𝐴
𝜕𝑧1
𝜕𝑧2

𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
+ 𝑒1 𝑒2 (𝑓1
+ 1 − 2 − 𝑓2
)
2
𝜕𝑧2 𝜕𝑧2 𝜕𝑧1
𝜕𝑧1

𝜕𝑓1 𝜕𝑓2
𝜕𝑓
𝜕𝑓
+
+ 𝑒1 𝑒2 ( 1 − 2 ) ,
𝜕𝑧1 𝜕𝑧2
𝜕𝑧2 𝜕𝑧1

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
1
= 𝑒1 𝑒2 {( 1 ) + 1 − 2 − ( 2 )} ,
2
𝜕𝑧2
𝜕𝑧2 𝜕𝑧1
𝜕𝑧1

=

## PDF page 5

Abstract and Applied Analysis

5

𝜕𝑓
𝜕
𝜕
𝜕
1 𝜕𝑓
∙ 𝑓 = − ( 1 + 2 + 𝑓1
+ 𝑓2
)
𝜕𝐴∗
2 𝜕𝑧1 𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

𝑓⊙

𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
𝜕
= (−𝑓1
− 𝑓2
+ 1 + 2)
𝜕𝐴∗ 2
𝜕𝑧1
𝜕𝑧2 𝜕𝑧1 𝜕𝑧2

𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
+ 𝑒1 𝑒2 ( 2 − 𝑓2
+ 𝑓1
− 1)
2
𝜕𝑧1
𝜕𝑧1
𝜕𝑧2 𝜕𝑧2
=−

𝜕𝑓
𝜕𝑓
1
𝜕
𝜕
+ 𝑒1 𝑒2 (𝑓1
− 𝑓2
− 2 + 1)
2
𝜕𝑧2
𝜕𝑧1 𝜕𝑧1 𝜕𝑧2

𝜕𝑓1 𝜕𝑓2 1
−
+ 𝑒𝑒
𝜕𝑧1 𝜕𝑧2 2 1 2

×{

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
1
= 𝑒1 𝑒2 {( 1 ) − ( 2 ) − 2 + 1 }
2
𝜕𝑧2
𝜕𝑧1
𝜕𝑧1 𝜕𝑧2

𝜕𝑓2
𝜕𝑓
𝜕𝑓
𝜕𝑓
− ( 2) + ( 1) − 1},
𝜕𝑧1
𝜕𝑧1
𝜕𝑧2
𝜕𝑧2

(36)
and, therefore,

𝜕𝑓
𝜕𝑓
𝜕
𝜕
𝜕
1
⊙ 𝑓 = (− 1 − 2 + 𝑓1
+ 𝑓2
)
∗
𝜕𝐴
2
𝜕𝑧1 𝜕𝑧2
𝜕𝑧1
𝜕𝑧2

𝑓

𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
+ 𝑒1 𝑒2 ( 2 + 𝑓2
− 𝑓1
− 1)
2
𝜕𝑧1
𝜕𝑧1
𝜕𝑧2 𝜕𝑧2
𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
1
= 𝑒1 𝑒2 { 2 + ( 2 ) − ( 1 ) − 1 }
2
𝜕𝑧1
𝜕𝑧1
𝜕𝑧2
𝜕𝑧2
(34)
and, therefore,
𝜕𝑓
𝜕
𝜕
=
∙𝑓+
⊙ 𝑓,
𝜕𝐴 𝜕𝐴
𝜕𝐴

𝜕𝑓
𝜕
𝜕
=
∙ 𝑓 + ∗ ⊙ 𝑓.
∗
∗
𝜕𝐴
𝜕𝐴
𝜕𝐴
(35)

Similarly, we have
𝜕𝑓
𝜕𝑓
𝜕
𝜕
𝜕
1
𝑓∙
+ 𝑓2
+ 1 + 2)
= (𝑓1
𝜕𝐴 2
𝜕𝑧1
𝜕𝑧2 𝜕𝑧1 𝜕𝑧2
+ 𝑒1 𝑒2 (𝑓1

𝜕𝑓
𝜕𝑓
𝜕
𝜕
− 𝑓2
+ 2 − 1)
𝜕𝑧2
𝜕𝑧1 𝜕𝑧1 𝜕𝑧2

𝜕𝑓
𝜕𝑓
1
= 1 + 2 + 𝑒1 𝑒2
𝜕𝑧1 𝜕𝑧2 2
× {(
𝑓⊙

𝜕𝑓1
𝜕𝑓
𝜕𝑓
𝜕𝑓
) − ( 2) + 2 − 1},
𝜕𝑧2
𝜕𝑧1
𝜕𝑧1 𝜕𝑧2

𝜕𝑓
𝜕𝑓
𝜕
𝜕
𝜕
1
+ 𝑓2
− 1 − 2)
= (𝑓1
𝜕𝐴 2
𝜕𝑧1
𝜕𝑧2 𝜕𝑧1 𝜕𝑧2
𝜕𝑓
𝜕𝑓
𝜕
𝜕
1
+ 𝑒1 𝑒2 (𝑓1
− 𝑓2
− 2 + 1)
2
𝜕𝑧2
𝜕𝑧1 𝜕𝑧1 𝜕𝑧2
𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
1
= 𝑒1 𝑒2 {( 1 ) − ( 2 ) − 2 + 1 } ,
2
𝜕𝑧2
𝜕𝑧1
𝜕𝑧1 𝜕𝑧2

𝑓∙

𝜕𝑓
𝜕𝑓
𝜕
𝜕
𝜕
1
= (−𝑓1
− 𝑓2
− 1 − 2)
∗
𝜕𝐴
2
𝜕𝑧1
𝜕𝑧2 𝜕𝑧1 𝜕𝑧2
𝜕𝑓
𝜕𝑓
1
𝜕
𝜕
+ 𝑒1 𝑒2 (𝑓1
− 𝑓2
+ 2 − 1)
2
𝜕𝑧2
𝜕𝑧1 𝜕𝑧1 𝜕𝑧2
=−

𝜕𝑓1 𝜕𝑓2 1
−
+ 𝑒𝑒
𝜕𝑧1 𝜕𝑧2 2 1 2

× {(

𝜕𝑓1
𝜕𝑓
𝜕𝑓
𝜕𝑓
) − ( 2) + 2 − 1},
𝜕𝑧2
𝜕𝑧1
𝜕𝑧1 𝜕𝑧2

𝜕
𝜕
𝜕
=𝑓∙
+𝑓⊙
,
𝜕𝐴
𝜕𝐴
𝜕𝐴

𝜕
𝜕
𝜕
𝑓 ∗ = 𝑓 ∙ ∗ + 𝑓 ⊙ ∗.
𝜕𝐴
𝜕𝐴
𝜕𝐴

(37)

Definition 4. Let Ω be an open set in R3 and for any element
𝑎 in Ω. A function 𝑓(𝑎) is said to be L(R)-regular on Ω if the
following conditions are satisfied:
(i) 𝑓𝑟 (𝑟 = 1, 2) are continuously differential functions
on Ω, and
(ii) 𝜕𝑓(𝑎)/𝜕𝐴∗ = 0 (𝑓(𝑎)(𝜕/𝜕𝐴∗ ) = 0) on Ω.
In particular, the equation 𝜕𝑓/𝜕𝐴∗ = 0 of Definition 4 is
equivalent to
𝜕
𝜕
∙ 𝑓 (𝑎) = − ∗ ⊙ 𝑓 (𝑎) .
∗
𝜕𝐴
𝜕𝐴
Moreover, (38) is equivalent to the following system:
𝜕𝑓
𝜕𝑓1
= − 2,
𝜕𝑧1
𝜕𝑧2
𝜕𝑓
𝜕𝑓1
= 2.
𝜕𝑧2 𝜕𝑧1

(38)

(39)

The above system is a corresponding Cauchy-Riemann system in C(T).
Remark 5. From the multiplications of C(T), the equation
𝑓(𝜕/𝜕𝐴∗ ) = 0 of Definition 4 is equivalent to
𝜕
𝜕
(40)
∙ 𝑓 (𝑎) =
⊙ 𝑓 (𝑎) .
∗
𝜕𝐴
𝜕𝐴∗
Also, the above equation (40) is equivalent to the following
system:
𝜕𝑓
𝜕𝑓1
= − 2,
𝜕𝑧1
𝜕𝑧2
𝜕𝑓
𝜕𝑓
𝜕
𝜕
𝑓1
= 𝑓2
⇐⇒ ( 1 ) = ( 2 ).
𝜕𝑧2
𝜕𝑧1
𝜕𝑧2
𝜕𝑧1

(41)

Further, the above system (41) is also a corresponding
Cauchy-Riemann system in C(T). Since the system (39) is
equivalent to the system (41), we say that 𝑓(𝑎) of Definition 4
is a regular function on Ω ⊂ R3 . When the function 𝑓(𝑎)
is either an L-regular function or an R-regular function on
Ω ⊂ R3 , we simply say that 𝑓(𝑎) is a regular function on
Ω ⊂ R3 .

## PDF page 6

6

Abstract and Applied Analysis
Similarly, by calculating the derivative 𝑓󸀠 (𝑧) of 𝑓(𝑧),

3. Properties of Regular Functions with
Values in C(T)

𝜕𝑓
𝜕𝑓
𝜕
∙𝑓= 1 + 2
𝜕𝑧
𝜕𝑥1 𝜕𝑥2

We define the derivative 𝑓󸀠 (𝑎) of 𝑓(𝑎) by the following:
𝑓󸀠 (𝑎) :=

𝜕𝑓 (𝑎)
.
𝜕𝐴

Proposition 6. Let Ω be an open set in R3 and let a function
𝑓(𝑎) be a regular function defined on Ω. Then
𝑓󸀠 (𝑎) = −2𝑒𝑟 (

𝜕𝑓
𝜕𝑓
𝜕𝑓
−
)=4
𝜕𝑧𝑟 𝜕𝑧𝑟
𝜕𝑥0

𝜕𝑓
𝜕𝑓
= −𝑒1
− 𝑒2
𝜕𝑥1
𝜕𝑥2
Proof. From the definition
(: (𝜕𝑓/𝜕𝐴∗ ) = 0), we have
𝜕𝑓
𝜕𝑓1
= − 2,
𝜕𝑧1
𝜕𝑧2

of

regular

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕
⊙ 𝑓 = (𝑒1 2 − 𝑒1 2 − 𝑒2 1 + 𝑒2 1 )
𝜕𝑧
𝜕𝑥1
𝜕𝑥1
𝜕𝑥2
𝜕𝑥2

(47)

𝜕𝑓
𝜕𝑓
1
1
− 𝑒1 𝑒2 ( 2 ) + 𝑒1 𝑒2 ( 1 ).
2
𝜕𝑧1
2
𝜕𝑧2

(43)

(𝑟 = 1, 2) .
a

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
1
+ 𝑒1 𝑒2 {( 2 ) − ( 1 ) + 1 − 2 } ,
2
𝜕𝑧1
𝜕𝑧2
𝜕𝑥2 𝜕𝑥1

(42)

Therefore, we have the equation
function

𝜕𝑓1
𝜕𝑓
= 2.
𝜕𝑧2 𝜕𝑧1

(44)

Therefore,

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕
𝜕
=
∙𝑓+
⊙ 𝑓 = −𝑒1 (𝑒1 1 + 𝑒2 2 )
𝜕𝑧 𝜕𝑧
𝜕𝑧
𝜕𝑥1
𝜕𝑥1
𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
− 𝑒2 (𝑒2 2 + 𝑒1 1 ) = −𝑒1
− 𝑒2
.
𝜕𝑥2
𝜕𝑥2
𝜕𝑥1
𝜕𝑥2

(48)

Further, using the same procedure, we obtain the equations

𝜕𝑓
𝜕𝑓
𝜕𝑢
𝜕𝑢
𝜕𝑢
𝜕𝑢
𝜕
∙ 𝑓 = 1 + 2𝑒1 1 + 0 + 2 + 2𝑒2 2 + 0
𝜕𝑧
𝜕𝑧1
𝜕𝑥0 𝜕𝑥0 𝜕𝑧2
𝜕𝑥0 𝜕𝑥0
𝜕𝑓
𝜕𝑢
𝜕𝑢
𝜕
1
+ 𝑒1 𝑒2 (𝑓2
+ 2𝑒1 2 + 𝑒2 𝑒1 0 − 2 )
2
𝜕𝑧1
𝜕𝑥0
𝜕𝑥0 𝜕𝑧1
𝜕𝑓
𝜕𝑢
𝜕𝑢
𝜕𝑢
1
+ 𝑒1 𝑒2 (2𝑒1 2 − 𝑒1 𝑒2 0 + 1 − 2𝑒2 1
2
𝜕𝑥0
𝜕𝑥0 𝜕𝑧2
𝜕𝑥0
+ 𝑒2 𝑒1
−2𝑒2
=4

𝜕𝑢0
𝜕
− 𝑓1
𝜕𝑥0
𝜕𝑧2

Proposition 7. Let Ω be an open set in R3 . If 𝑓(𝑎) is a regular
function on Ω, then we have
𝑛
𝜕𝑛 𝑓
𝑛𝜕 𝑓
=
4
,
𝜕𝐴𝑛
𝜕𝑥0𝑛

𝜕𝑓
𝜕𝑓
𝜕
𝜕
(4
)=4
( ∗ ) = 0.
∗
𝜕𝐴
𝜕𝑥0
𝜕𝑥0 𝜕𝐴

(51)

Hence, 𝜕𝑓/𝜕𝑥0 is a regular function with values in C(T). From
Proposition 6, we have

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕
+ 2𝑒2 1 + 1 − 2𝑒2 1 − 2
𝜕𝑧2
𝜕𝑥0 𝜕𝑧2
𝜕𝑥0 𝜕𝑧1

2
𝜕2 𝑓
𝜕 𝜕𝑓
2𝜕 𝑓
=
.
(
)
=
4
𝜕𝐴2 𝜕𝐴 𝜕A
𝜕𝑥02

𝜕𝑓
𝜕𝑓
𝜕
+2𝑒1 2 − 𝑓2
− 2𝑒1 2 )
𝜕𝑥0
𝜕𝑧1
𝜕𝑥0

(52)

By repeating the above process, we can obtain the equation

𝜕𝑓
𝜕𝑓
𝜕𝑓
𝜕𝑓
= 2𝑒1 𝑒2 (𝑒1 1 − 𝑒1 1 − 𝑒2 2 + 𝑒2 2 )
𝜕𝑥0
𝜕𝑥0
𝜕𝑥0
𝜕𝑥0

(45)

𝑛
𝜕𝑛 𝑓
𝑛𝜕 𝑓
=
4
.
𝜕𝐴𝑛
𝜕𝑥0𝑛

(53)

𝜕2
𝜕2
1 𝜕2
1 𝜕2
= 2 2 + 𝑒1 2 + 𝑒2 2
𝜕𝑥0 4 𝜕𝑥1 4 𝜕𝑥2
𝑟=1 𝜕𝑧𝑟 𝜕𝑧𝑟

(54)

We let
2

◻𝑎 = ∑

Hence, we obtain the equation
𝜕𝑓
𝜕𝑓
𝜕
𝜕
.
=
∙𝑓+
⊙𝑓=4
𝜕𝑧 𝜕𝑧
𝜕𝑧
𝜕𝑥0

(50)

Proof. Since 𝑓 is a regular function on Ω with values in C(T),
by Definition 4,

𝜕
1
⊙ 𝑓 = 𝑒1 𝑒2
𝜕𝑧
2

𝜕𝑓
𝜕𝑓
1
1
− 𝑒1 𝑒2 ( 2 ) + 𝑒1 𝑒2 ( 1 ) = 0.
2
𝜕𝑧1
2
𝜕𝑧2

(49)

where 𝑛 is a positive integer.

𝜕𝑢
𝜕𝑢1
− 𝑒1 𝑒2 0 )
𝜕𝑥0
𝜕𝑥0

𝜕𝑓
𝜕𝑓
𝜕𝑓 1
1
+ 𝑒1 𝑒2 ( 2 ) − 𝑒1 𝑒2 ( 1 ),
𝜕𝑥0 2
𝜕𝑧1
2
𝜕𝑧2

× (𝑓1

𝜕𝑓
𝜕𝑓
𝜕𝑓
−
= −2𝑒𝑟 (
) (𝑟 = 1, 2) .
𝜕𝑧
𝜕𝑧𝑟 𝜕𝑧𝑟

(46)

on an open set Ω in R3 .

## PDF page 7

Abstract and Applied Analysis

7

Theorem 8. Let Ω be an open set in R3 . If 𝑓 is a regular
function on Ω, then the following equation holds true:
◻𝑎 𝑓 (𝑎) = −

1 𝜕2 𝑓 (𝑎)
.
8 𝜕𝐴2

(55)

Proof. Since 𝑓 is a regular function on Ω, we have the
following system:
𝜕𝑢
𝜕𝑢
𝜕𝑢 𝜕𝑢
𝜕𝑢
4 0 = 1 + 2, 2 = 1,
𝜕𝑥0 𝜕𝑥1 𝜕𝑥2 𝜕𝑥1 𝜕𝑥2
𝜕𝑢
𝜕𝑢
4 𝑟 =− 0
𝜕𝑥0
𝜕𝑥𝑟

=2

(56)

(𝑟 = 1, 2) .

= {(4

𝜕2 𝑓
𝜕2 𝑢0
𝜕2 𝑢1
𝜕2 𝑢2
−
2𝑒
−
2𝑒
=
−2
.
1
2
𝜕𝑥02
𝜕𝑥02
𝜕𝑥02
𝜕𝑥02

(57)

(58)

Theorem 9. Let Ω be an open set in R3 and let 𝑈 be any
domain on Ω with a smooth distinguished boundary 𝑏𝑈 such
that 𝑈 ⊂ Ω. If 𝑓 is a regular function on Ω, then one has

𝑏𝑈

(59)

where 𝜔𝑓 is the reduced quaternionic product of the form 𝜔 on
the function 𝑓(𝑎).
Proof. Since 𝜔𝑓 = 4𝑓𝑑𝑥1 ∧𝑑𝑥2 −𝑒1 𝑓𝑑𝑥0 ∧𝑑𝑥2 +𝑒2 𝑓𝑑𝑥0 ∧𝑑𝑥1 ,
we have
𝜕𝑓
𝜕𝑓
𝑑𝑥0 ∧ 𝑑𝑥1 ∧ 𝑑𝑥2 + 𝑒1
𝑑𝑥 ∧ 𝑑𝑥1 ∧ 𝑑𝑥2
𝜕𝑥0
𝜕𝑥1 0

+ 𝑒2

𝜕𝑓
𝑑𝑥 ∧ 𝑑𝑥1 ∧ 𝑑𝑥2
𝜕𝑥2 0

𝜕𝑢2 𝜕𝑢0
𝜕𝑢
𝜕𝑢
+
) + 𝑒1 𝑒2 ( 2 − 1 )} 𝑑𝐼,
𝜕𝑥0 𝜕𝑥2
𝜕𝑥1 𝜕𝑥2
(60)

where 𝑑𝐼 = 𝑑𝑥0 ∧ 𝑑𝑥1 ∧ 𝑑𝑥2 in 𝑈. From the corresponding
Cauchy-Riemann system (39) for 𝑓(𝑎) in C(T), we have the
system (56). Hence, 𝑑(𝜔𝑓) = 0 and, therefore, by Stokes
theorem, we obtain the following result:
∫ 𝜔𝑓 = ∫ 𝑑 (𝜔𝑓) = 0.
𝑏𝑈

𝑈

(61)

Acknowledgment

Next, we consider a differential form

∫ 𝜔𝑓 = 0,

𝜕𝑢
𝜕𝑢0 𝜕𝑢1 𝜕𝑢2
𝜕𝑢
−
−
) + 𝑒1 (4 1 + 0 )
𝜕𝑥0 𝜕𝑥1 𝜕𝑥2
𝜕𝑥0 𝜕𝑥1

The authors declare that there is no conflict of interests
regarding the publication of this paper.

From Proposition 7, we have 𝜕2 𝑓/𝜕𝐴2 = 42 (𝜕2 𝑓/𝜕𝑥02 ). Hence,
by calculating and comparing the above polynomials, we
obtain that ◻𝑎 𝑓 is equal to −(1/8)(𝜕2 /𝜕𝐴2 )𝑓.

𝜔 = 4𝑑𝑥1 ∧ 𝑑𝑥2 − 𝑒1 𝑑𝑥0 ∧ 𝑑𝑥2 + 𝑒2 𝑑𝑥0 ∧ 𝑑𝑥1 .

𝜕 (𝑒1 𝑓1 + 𝑒2 𝑓2 )
𝑑𝐼
𝜕𝑥2

Conflict of Interests

𝜕2 𝑢0
𝜕2 𝑢0
𝜕2 𝑢2
+ 𝑒1
−
+ 𝑒2
𝜕𝑥0 𝜕𝑥1 𝜕𝑥0 𝜕𝑥2
𝜕𝑥0 𝜕𝑥2

𝑑 (𝜔𝑓) = 4

+ 𝑒2

𝜕2
1 𝜕2
1 𝜕2
+ 𝑒1 2 + 𝑒2 2 ) (𝑢0 + 𝑒1 𝑢1 + 𝑒2 𝑢2 )
2
𝜕𝑥0 4 𝜕𝑥1 4 𝜕𝑥2

𝜕2 𝑢0
𝜕2 𝑢1
𝜕2 𝑢2
𝜕2 𝑢1
+
2𝑒
+
2𝑒
−
1
2
𝜕𝑥0 𝜕𝑥1
𝜕𝑥02
𝜕𝑥02
𝜕𝑥02

= −2

𝜕 (𝑒1 𝑓1 + 𝑒2 𝑓2 )
𝜕 (𝑒1 𝑓1 + 𝑒2 𝑓2 )
𝑑𝐼 + 𝑒1
𝑑𝐼
𝜕𝑥0
𝜕𝑥1

+𝑒2 (4

By the definition of ◻𝑎 , we have
◻𝑎 𝑓 = (2

=4

The third author was supported by a 2-Year Research Grant
of Pusan National University.

References
[1] A. S. Meglihzon, “Po povodu monogennosti kvaternionov,” DoKlady Akademii Nauk SSSR 3, vol. 59, pp. 431–434, 1948.
[2] A. Sudbery, “Quaternionic analysis,” Mathematical Proceedings
of the Cambridge Philosophical Society, vol. 85, no. 2, pp. 199–
224, 1979.
[3] R. Fueter, “Die Funktionentheorie der Differentialgleichungen
Δ𝑢 = 0 und ΔΔ𝑢 = 0 mit vier reellen Variablen,” Commentarii
Mathematici Helvetici, vol. 7, no. 1, pp. 307–330, 1934.
[4] V. Soucek, Regularni funkce quaternionove promenne [Thesis],
Charles University Prague, 1980.
[5] F. Sommen, “Monogenic differential forms and homology
theory,” Proceedings of the Royal Irish Academy A, vol. 84, no.
2, pp. 87–109, 1984.
[6] M. Naser, “Hyperholomorphic functions,” Siberian Mathematical Journal, vol. 12, pp. 959–968, 1971.
[7] K. Nôno, “Hyperholomorphic functions of a quaternion variable,” Bulletin of Fukuoka University of Education III, vol. 32, p.
2137, 1983.
[8] K. Nôno, “Characterization of domains of holomorphy by
the existence of hyper-conjugate harmonic functions,” Revue
Roumaine de Mathématiques Pures et Appliquées, vol. 31, no. 2,
pp. 159–161, 1986.
[9] K. Nōno, “Domains of hyperholomorphy in 𝐶2 × C2 ,” Bulletin
of Fukuoka University of Education III, vol. 36, pp. 1–9, 1987.
[10] J. Ryan, “Complexified Clifford analysis,” Complex Variables and
Elliptic Equations, vol. 1, no. 1, pp. 119–149, 1982/83.

## PDF page 8

8
[11] J. Ryan, “Special functions and relations within complex Clifford analysis. I,” Complex Variables and Elliptic Equations, vol.
2, no. 2, pp. 177–198, 1983.
[12] H. Malonek, “A new hypercomplex structure of the Euclidean
space R𝑚+1 and the concept of hypercomplex differentiability,”
Complex Variables: Theory and Applications, vol. 14, no. 1–4, pp.
25–33, 1990.
[13] S. Gotô and K. Nôno, “Regular functions with values in a
commutative subalgebra C(C) of matrix algebra 𝑀(4, R),”
Bulletin of Fukuoka University of Education III, vol. 61, pp. 9–
15, 2012.
[14] H. Koriyama, H. Mae, and K. Nôno, “Hyperholomorphic
functions and holomorphic functions in quaternionic analysis,”
Bulletin of Fukuoka University of Education III, vol. 60, pp. 1–9,
2011.
[15] J. Kajiwara, X. D. Li, and K. H. Shon, “Regeneration in
complex, quaternion and Clifford analysis,” in Finite or Infinite
Dimensional Complex Analysis and its Applications, vol. 2 of
Advances in Complex Analysis and Its Applications, pp. 287–298,
Kluwer Academic, Hanoi, Vietnam, 2004.
[16] J. Kajiwara, X. D. Li, and K. H. Shon, “Function spaces
in complex and Clifford analysis,” in Inhomogeneous Cauchy
Riemann System of Quaternion and Clifford Analysis in Ellipsoid,
International Colloquium on Finite or Infinite Dimensional
Complex Analysis and Its Applications, vol. 14, pp. 127–155, Hue
University, Hue, Vietnam, 2006.
[17] S. J. Lim and K. H. Shon, “Hyperholomorphic fucntions and
hyperconjugate harmonic functions of octonion variables,”
Journal of Inequalities and Applications, vol. 77, pp. 1–8, 2013.
[18] S. J. Lim and K. H. Shon, “Dual quaternion functions and its
applications,” Journal of Applied Mathematics, vol. 2013, Article
ID 583813, 6 pages, 2013.
[19] D. H. Titterton and J. L. Weston, “Strapdown inertial navigation
technology,” Peter Pregrinus, 1997.
[20] R. Fueter, “Die theorie der regularen funktionen einer quaternionenvariablen,” in Comptés Rendus du Congrès International
des Mathenaticiens, vol. 1, pp. 75–91, Oslo, Norway, 1936.

Abstract and Applied Analysis

## PDF page 9

Advances in

Advances in

Journal of

Operations Research

Decision Sciences

Applied Mathematics

Algebra

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Volume 2014

Volume 2014

Journal of

Probability and Statistics
Volume 2014

The Scientific
World Journal
Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

International Journal of

Differential Equations
Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Volume 2014

Submit your manuscripts at
http://www.hindawi.com
International Journal of

Advances in

Combinatorics
Hindawi Publishing Corporation
http://www.hindawi.com

Mathematical Physics
Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Journal of

Journal of

Complex Analysis

Mathematics

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

International
Journal of
Mathematics and
Mathematical
Sciences

Volume 2014

Mathematical Problems
in Engineering

Abstract and
Applied Analysis

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Volume 2014

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Discrete Mathematics

Journal of

Volume 2014

Discrete Dynamics in
Nature and Society

Journal of

Function Spaces
Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

International Journal of

Journal of

Stochastic Analysis

Optimization

Hindawi Publishing Corporation
http://www.hindawi.com

Hindawi Publishing Corporation
http://www.hindawi.com

Volume 2014

Volume 2014
