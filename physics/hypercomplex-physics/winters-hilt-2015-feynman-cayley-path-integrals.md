Source: https://doi.org/10.12988/astp.2015.5881
PDF sha256: 1e71b999600e924823852e7d8924f8c84ad09583e6c74caff61cb74f497c638f
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of winters-hilt-2015-feynman-cayley-path-integrals.pdf

Transcription of `winters-hilt-2015-feynman-cayley-path-integrals.pdf` in this directory, 17 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 17 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-16 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Advanced Studies in Theoretical Physics
Vol. 9, 2015, no. 14, 667 - 683
HIKARI Ltd, www.m-hikari.com
http://dx.doi.org/10.12988/astp.2015.5881

Feynman-Cayley Path Integrals Select Chiral
Bi-Sedenions with 10-Dimensional Space-Time
Propagation
Stephen Winters-Hilt
Connecticut College, Box #5564
270 Mohegan Ave., New London, CT 06320, United States
Copyright © 2015 Stephen Winters-Hilt. This article is distributed under the Creative Commons
Attribution License, which permits unrestricted use, distribution, and reproduction in any medium,
provided the original work is properly cited.

Abstract
The Feynman-Cayley Path Integral extends the notion of “all paths”, with path
integration generally involving a real or matrix object, to “all paths with all higherdimensional Cayley algebras and their propagating sub-algebra (loop) objects”. The
highest order algebraic structure that can be ‘propagated’ in the path integral
computations is sought for this reason. An 8 dimensional subspace (two versions, so
chiral) of the 15dim unit norm sedenions is shown to propagate. A 9 dimensional
subspace (chiral again) of the 31dim unit norm bi-sedenions is shown to propagate in
a similar manner. The results are verified both computationally and theoretically. The
theoretical proof, in turn, indicates where the breakdown in the chiral extensions
occurs, which is then verified computationally. This may provide a deeper
understanding of why higher order extensions aren’t allowed in a number of other
mathematical areas, some of which are discussed. At the maximal order of propagateable Feynman-Cayley Path Integral, the computational and theoretical results indicate
a 10-dimensional space-time theory, in agreement with string theory, and yet still
clearly indicates how we have spacetime and Lorenz transformation (and all of the
standard model embedded for that matter). Chirality at the sedenions level, with two
octonions sub-spaces, could be used to describe bosonic and fermionic matter.
Chirality at the bi-sedenion level could provide an explanation for (normal) light
matter and dark matter.

## PDF page 2

668

Stephen Winters-Hilt

1 Introduction
For Real numbers unit norm propagation is trivial, consisting of multiplying by +1 or
-1. For Complex numbers unit norm propagation involves multiplication by complex
numbers on the classic unit circle in the complex plane, which reduces to simple
phase addition according to rotations about the center of that circle (motions on S1).
For quaternion numbers unit norm propagation is still straightforward since it’s still,
in the end, a normed division algebra, where N(xy)=N(x)N(y). Instead of motion on
S1 we now have motion on S3, the unit hypersphere in four dimensions. This still
holds true for Octonions, with unit norm still directly maintained when multiplying
unit norm objects in general. Now the motion is that of a point on a seven
dimensional hypersphere S7. Sedenions are not normed division algebras, lacking
linear alternativity and the moufang loop identities, thus multiplication of unit norm
objects for sedenions (points on S15) will not, generally, remain unit norm, i.e., will
leave the S15 space.

The question then arises is there is a sub-algebra or loop construct in the sedenions,
that is not just trivially the octonions, that can still allow unit norm propagation? If
this works for Sedenions, what about Bi-sedenions and higher dimensional Cayley
algebras? In this paper it will be shown that there are two Sedenion subspaces,
associated with ‘left’ and ‘right’ propagation, where the unit norm property is
retained. This is found again at the level of the Bi-Sedenions by a similar
construction. The results were initially explored computationally, then later
established in theoretical proofs. In those proofs a key step fails when attempting to
go to higher orders beyond the bi-sedenions and its sub-algebra propagation.
(Propagation is taken to mean that a unit norm element of an algebra when multiplied
by a unit norm element of an algebra or subalgebra or loop or chiral-loop can be
propagated: (unit norm)*(unit norm subalgebra)=(unit norm), where the one-sided
multiplication by the special subalgebra results in a product that remains unit norm.)

So, if the Feynman-Cayley construction works on all algebras, it essentially allows a
selection argument to be made for the highest order unit norm propagating algebra in
devising theories to describe matter. The highest order propagating structure might,
thus, be the nine dimensional bi-sedenion elements, that are shown here, that are
(chirally) extended sedenions that are themselves made from chirally extended
octonions. The nine space dimensionality when paired with the implicit time
dimension provides a 10 dim (1,9) spacetime theory, in agreement with string theory.
(If the time is augmented to be a complex limit parameter, then we get an 11-dim
theory, which shows agreement with M-theory and agreement with a role for
Euclideanization related thermodynamics properties.) The core recursive algorithm in
the computational work with the Cayley multiplication is shown after the theoretical
proofs.

## PDF page 3

Feynman-Cayley path integrals

669

2 Background on Cayley Algebras
The list representation for hypercomplex numbers will make things clearer in what
follows so will be introduced here for the first seven Cayley algebras:
Reals: X0  (X0) .
Complex: (X0 + X1 i)  (X0 , X1 ) .
Quaternions: (X0 + X1 i + X2 j + X3 k)  (X0 , X1 , X2 , X3)  (X0 , … , X3) .
Octonions: (X0 , … , X7) with seven imaginary numbers.
Sedenions: (X0 , … , X15) with fifteen imaginary numbers.
Trigintaduonions (a.k.a Bi-Sedenions): (X0 , … , X31) with 31 imaginary numbers.
Bi-Trigintaduonions: (X0 , … , X63) with 63 types of imaginary number.
Consider how the familiar complex numbers can be generated from two real numbers
with the introduction of a single imaginary number ‘i’, {X0 , X1}  (X0 + X1 i). This
construction process can be iterated, using two complex numbers, {Z0 , Z1} , and a
new imaginary number ‘j’:
(Z0 + Z1 j) = (A+Bi ) + (C+Di ) j = A+Bi + Cj +Dij = A+Bi + Cj +Dk,
where we have introduced a third imaginary number ‘k’ where ‘ij=k’. In list notation
this appears as the simple rule ((A,B),(C,D)) = (A,B,C,D). This iterative construction
process can be repeated, generating algebras doubling in dimensionality at each
iteration, to generate the 1, 2, 4, 8, 16, 32, and 64 dimensional algebras listed above.
The process continues indefinitely to higher orders beyond that, doubling in
dimension at each iteration, but we will see that the main algebras of interest for
physics are those with dimension 1, 2, 4, and 8, and sub-spaces of those with
dimension 16 and 32 dimensional algebras.
Addition of hypercomplex numbers is done component-wise, so is straightforward.
For hypercomplex multiplication, list notation makes the freedom for group splittings
more apparent, where any hypercomplex product ZxQ to be expressed as (U,V)x(R,S)
by splitting Z=(U,V) and Q=(R,S). This is important because the product rule,
generalized by Cayley, uses the splitting capability.
The Cayley algebra
multiplication rule is:
(A,B)(C,D) = ([ACD*B],[BC*+DA]),
where conjugation of a hypercomplex number flips the signs of all of its imaginary
components:
(A,B)* = Conj(A,B) = (A*,B)
The specification of new algebras, with addition and multiplication rules as indicated
by the constructive process above, is known as the Cayley-Dickson construction, and
this gives rise to what is referred to as the Cayley algebras in what follows.

## PDF page 4

670

Stephen Winters-Hilt

3 Relation of Hypercomplex Formulations to Physics Theories
Physics has a lengthy ‘love-hate’ relationship with hypercomplex numbers. The
original formulations of electromagnetism by Maxwell involved quaternionic
mathematics, and even at that time this relationship was off to a difficult start. As
stated by Maxwell in a manuscript on the application to electromagnetism in
November of 1870 [1]: “... The invention of the Calculus of Quaternions by Hamilton
is a step towards the knowledge of quantities related to space which can only be
compared for its importance with the invention of triple coordinates by Descartes.
The limited use which has up to the present time been made of Quaternions must be
attributed partly to the repugnance of most mature minds to new methods involving
the expenditure of thought ...” (with emphasis mine). The enthusiasm of Maxwell for
use of Quaternionic mathematics did not win over the great physicists of his day,
Josiah Willard Gibbs and Oliver Heaviside in particular, who discarded the
quaternionic mathematics in favor of a new mathematics (vector calculus) that they
invented so as to avoid the ‘foreign’ hypercomplex mathematics. In a biography of
Hamilton [2], in a quotation attributed to Gibbs: “My first acquaintance with
quaternions was in reading Maxwell's E.&M. where Quaternion notations are
considerably used. ... I saw, that although the methods were called quaternionic the
idea of the quaternion was quite foreign to the subject.”
The stigma associated with hypercomplex mathematics, and the higher-dimensional
physics unification attempts of Maxwell and later Einstein, was still significant
decades later when Feynman obtained an unusual proof of the homogeneous Maxwell
equations [3-6] in a higher (than 3) dimensional space. Feynman was trying to see if
any new theoretical theory would be indicated and the fact that he had obtained a
novel new way to explain the existing Maxwell’s equations in higher dimensions was
not interesting at the time. The inextricable problems of quantum gravity and the
discovery of higher-dimensional string theory, among other things, have changed the
focus since that time almost 70 years ago. The accessibility of computational
resources makes a big difference too.
It has been shown in numerous papers that the (1, 9) dimensional superstring has a
natural parameterization in terms of octonions [7-9]. In [10, 11] the Dirac and
Maxwell equations (in vacuum) are derived using octonionic algebras. In [12] a
quaternionic equation is described for electromagnetic fields in inhomogenous media.
In [13], the D4-D5-E6 model that includes the Standard Model plus Gravity is
constructed using octonionic fermion creators and annihilators. In [14] octonionic
constructions are shown to be consistent with the SU(3)C gauge symmetry of QCD. It
would appear that there are a number of implementations involving hypercomplex
numbers that are consistent with the Standard Model. But there is still the question of
why bother? What is shown here is why the bother might be worth it as a critical new
link to string theory is provided, that may explain what dimensional reduction will
relate to experiments involving the standard model, and the formalism also allows for
an explanation for Dark matter, all in a mathematics that can be absorbed into a
Lagrangian formulation that could be consistent with a theory of Gravity.

## PDF page 5

Feynman-Cayley path integrals

671

4 The Formulation of the Problem for Sedenion Propagation
Further theoretical details on hypercomplex numbers can be found at [15, 16]. In
what follows multiplications involving unit norm Cayley numbers will be done at the
various orders using the Cayley algebra multiplication rule described above, that
reduces the order of hypercomplex complex multiplication, which when iterated
allows all hypercomplex products to reduce to a collection of Real multiplications.
Millions of repeated hypercomplex multiplications are done computationally to
demonstrate unit norm propagation in the situations that follow, where B denotes a
bisedenion, S denotes a sedenion, O a octonion, Q a quaternion, C for complex, and R
for a real:
Sedenions have two unit norm propagators of the form:
S(unit norm)  S(unit norm propagator) = S(unit norm)
S(unit norm) = S1(OLeft,ORight) = S1(OL,OR) = (O1L,O1R)
If S1 is unit norm, then norm(S1) = S1  S1* = 1, which for our notation means:
1 = (O1L,O1R)(O1L*,O1R) = ( [O1LO1L*+O1R*O1R], [O1RO1L+O1RO1L] )
1 = ( [norm(O1L)+norm(O1R)], 0 )
1 = norm(O1L)+norm(O1R)
S(unit norm propagator) = S2(OLeft,OReal) = (O2L, ) for the right octonion real, e.g.,
in list notation have OReal = (,0,0,0,0,0,0,0), so have (O2L, (,0,0,0,0,0,0,0)) which
is abbreviated as (O2L, ) where it is understood that  is real and is the real part of
the purely real right octonion. There is another type of unit norm propagator where
we have (OReal,ORight) where the same results hold, but the example that follows will
use the (O2L, ) form.
If S2 is unit norm, then norm(S2) = S2  S2* = 1, which for our notation means:
1 = norm(O2L)+2
So we can now ask the question,
Does S(unit norm)  S(unit norm propagator), return a unit norm Sedenion when
using the special class of unit norm propagators indicated?

5 Proof that Norm(S1S2)=1
(S1S2)=(O1L,O1R)(O2L, ) = ( [O1LO2L O1R], [O1L+O1RO2L*] )
(S1S2)* = ( [O1LO2L O1R]*, [O1L+O1RO2L*] )
norm(S1S2) = (S1S2)  (S1S2)*
= ( [O1LO2L O1R]  [O1LO2L O1R]* +[O1L+O1RO2L*]*  [O1L+O1RO2L*],
[O1L+O1RO2L*]  [O1LO2L O1R] + [O1L+O1RO2L*]  [O1LO2L O1R])

## PDF page 6

672

Stephen Winters-Hilt

= ( norm(O1LO2L)+norm(O1RO2L*)+2 norm(O1R)+2 norm(O1L)
(O1LO2L)O1R*O1R(O1LO2L)*+O1L*(O1RO2L*)+(O1RO2L*)*O1L, 0)
Multiplying the expressions previously obtained, 1 = norm(O1L)+norm(O1R) with 1 =
norm(O2L)+2, and making use of the norm property norm(xy)=norm(x)norm(y), we
have:
norm(S1S2) = (1-Z, 0), where,
Z = +(O1LO2L)O1R*+O1R(O1LO2L)*O1L*(O1RO2L*)(O1RO2L*)*O1L.
Since we are computing the norm, which returns only the real component, we know Z
must be real. To work with this expression with a little more clarity, switch to the
notation:
A=O1L; B=O2L; C=O1R*, then have
Z = (AB)C + C*(AB)*A*(C*B*)(C*B*)*A
Z = (AB)C + C*(AB)*A*(BC)*(BC)A
The Cayley algebras up to octionic are also known as the composition algebras for
which a number of properties exist. We need the braid laws to proceed, so let’s
briefly detour to address that. The fundamental composition rule is simply that of the
norm of a product being the product of the norms: norm(XY) = norm(X) x normY)
Consider the norm of two things added:
Norm(X+Y) = (X+Y)(X+Y)* = XX* +XY*+YX*+YY*
= norm(X) + norm(Y) + 2 real(XY*)
Define [X,Y] = real(XY*) = [norm(X+Y)norm(X)norm(Y)]/2, then have another
way to express conjugation using norms and real parts:
X* = 2[X,1]-X = 2real(X)-X = (real(X) unchanged, imag(X) negated))
The composition algebras (up to octionic) build from the core norm(XY) = norm(X) x
normY) relation to arrive at a number of interesting properties, including the ‘braid’
laws: [XY,Z] = [Y,X*Z] and [XY,Z]=[X,ZY*]. To arrive at the Braid law (following
[15]) you start with the composition law norm(XY)=norm(X)norm(Y), you then
prove the scaling law, [XY,XZ]=norm(x)[Y,Z], by substituting Y with Y+Z in the
composition law. Then establish the exchange law [XY,UZ] = 2[X,U][Y,Z]-[XZ,UY]
by substituting X with X+U in the scaling law. If you put U=1 in the exchange law, it
reduces to forms allowing the braid law to be shown.
Let’s apply the braid law for the form [XY,Z] to the (BC)A term, so let’s look at
the braid law for [BC,A*] = [C,B*A*], which can be rewritten as:
norm(BC+A*)norm(BC)norm(A*) = norm(C+B*A*)norm(C)norm(B*A*)
norm(BC+A*)=norm(BC)+norm(A*)+(BC)A+A*(BC)*
norm(C+B*A*)=norm(C)+norm(B*A*)+C(AB)+(AB)*C*

## PDF page 7

Feynman-Cayley path integrals

673

putting this together: (BC)A+A*(BC)*=C(AB)+(AB)*C*. So we can now rewrite the
(BC)A term as: (BC)A = C(AB)+(AB)*C*A*(BC)*. Substituting this
back into Z:
Z = (AB)C + C*(AB)*C(AB)(AB)*C*
= [(AB)CC(AB)] + [C*(AB)*(AB)*C*]
What is a commutator on the Cayley numbers, is it necessarily non-real?
XY=(A,B)(C,D) = ([ACD*B],[BC*+DA])
YX=(C,D)(A,B)= ([CAB*D],[DA*+BC])
{X,Y}=XY-YX= ([ACCA+B*DD*B],[BC*BC+DADA*])
{X,Y}= ( [{A,C}+2Im(B*D)], [B 2Im(C) + D 2Im(A)] )
So the commutator at one order of Cayley number is reduced to an expression
involving the commutator at the next lower order Cayley number, plus a bunch of
other terms that don’t contribute to the real component. This can be iterated to arrive
at the real algebra in the commutator, where the commutator is zero, thereby
establishing that the commutator on the Cayley numbers must result in a pure
imaginary Cayley number. This being the case, we see that since Z consists of two
commutator terms, neither of which has a real contribution, and since Z must be real,
this proves that Z=0.
This proves the first extension, for unit-norm propagators that are Sedenions of the
form SLeft=(OLeft,) or SRight=(,ORight), where OLeft and ORight are any octonion. The
next extension is to unit-norm propagators that are Bisedenion by using similar
constructions, e.g., Bisedenions, of the form B=(SLeft,SReal) = ( (OLeft,) ,  ). (Note
that  is a real octonion, while  is a purely real sedenion.)

6 The Formulation of the Problem for Bi-Sedenion Propagation
Bisedenions have two unit norm propagators of the form:
B(unit norm)  B(unit norm propagator) = B(unit norm)
B(unit norm) = B1(SLeft,SRight) = B1(SL,SR) = (S1L,S1R)
If B1 is unit norm, then norm(B1) = B1  B1* = 1, which for our notation means:
1 = (S1L,S1R)(S1L*,S1R) = ( [S1LS1L*+S1R*S1R], [S1RS1L+S1RS1L] )
1 = ( [norm(S1L)+norm(S1R)], 0 )
1 = norm(S1L)+norm(S1R)
B(unit norm propagator) = B2(SLeft,SReal) = (S2L, ) for the right sedenion real, e.g., in
list notation have SReal
= (,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0), so have (O2L,
(,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0)) which is abbreviated as (O2L, ) where it is
understood that  is real and is the real part of the purely real right sedenion. There is

## PDF page 8

674

Stephen Winters-Hilt

another type of unit norm propagator where we have (SReal,SRight) where the same
results hold, but the example that follows will use the (S2L, ) form.
If B2 is unit norm, then norm(B2) = B2  B2* = 1, which for our notation means:
1 = norm(S2L)+2
So we can now ask the question:
Does B(unit norm)  B(unit norm propagator), return a unit norm Bisedenion when
using the special class of unit norm propagators indicated?

7 Proof that Norm(B1B2)=1
(B1B2)=(S1L,S1R)(S2L, ) = ( [S1LS2L S1R], [S1L+S1RS2L*] )
(B1B2)* = ( [S1LS2L S1R]*, [S1L+S1RS2L*] )
norm(B1B2) = (B1B2)  (B1B2)*
= ( [S1LS2L S1R]  [S1LS2L S1R]* +[S1L+S1RS2L*]*  [S1L+S1RS2L*],
[S1L+S1RS2L*]  [S1LS2L S1R] + [S1L+S1RS2L*]  [S1LS2L S1R])
= ( norm(S1LS2L)+norm(S1RS2L*)+2 norm(S1R)+2 norm(S1L)
(S1LS2L)S1R*S1R(S1LS2L)*+S1L*(S1RS2L*)+(S1RS2L*)*S1L, 0)
To proceed as before we need to show that the norm property norm(xy) =
norm(x)norm(y) holds for the sedenions when one of them is constrained to be in the
form of the sedenion propagator, e.g., does norm(S1LS2L)=norm(S1L)norm(S2L)
where S2L is in the form of the sedenion propagator?
norm(S1LS2L) = (S1LS2L)  (S1LS2L)*
= ( [O1LLO2LL O1LR]  [O1LLO2LL O1LR]* +
[O1LL+O1LRO2LL*]*  [O1LL+O1LRO2LL*],
[O1LL+O1LRO2LL*]  [O1LLO2LL O1LR] +
[O1LL+O1LRO2LL*]  [O1LLO2LL O1LR])
= ( norm(O1LLO2LL)+norm(O1LRO2LL*)+2 norm(O1LR)+2 norm(O1LL)
(O1LLO2LL)O1LR*O1LR(O1LLO2LL)*+
O1LL*(O1LRO2LL*)+(O1LRO2LL*)*O1LL, 0)
Now that we’ve reduced to this level, we know that the octonions will offer the
standard norm property whereby norm(O1LLO2LL)=norm(O1LL)norm(O2LL) and we
show the other terms are zero since real yet consisting of commutators, the latter
arrangements made possible by manipulations according to the braid laws that hold
for the composition algebras (including the octonions) without restriction.

## PDF page 9

Feynman-Cayley path integrals

675

So as before, by multiplying the expressions previously obtained, 1 = norm(S1L) +
norm(S1R) with 1 = norm(S2L)+2, and making use of the norm property
norm(xy)=norm(x)norm(y) applicable for the terms of interest, we have:
norm(B1B2) = (1-Z, 0), where,
Z = +(S1LS2L)S1R*+S1R(S1LS2L)*S1L*(S1RS2L*)(S1RS2L*)*S1L.
Since we are computing the norm, which returns only the real component, we know Z
must be real. As with the lower order Cayley extension, we need the braid laws to
proceed at this juncture.
What is (S1LS2L)S1R* when accounting for the special form of S2L=(O2LL, )? First
calculate (S1LS2L):
(S1LS2L)=(O1LL,O1LR)(O2LL, ) = ( [O1LLO2LL O1LR], [O1LL+O1LRO2LL*] )
Then
(S1LS2L)S1R* = ( [O1LLO2LL O1LR], [O1LL+O1LRO2LL*] ) (O1RL*,-O1RR)
= ([O1LLO2LL O1LR]O1RL* + O1RR*[O1LL+O1LRO2LL*],
O1RR [O1LLO2LL O1LR] + [O1LL+O1LRO2LL*]O1RL)
= ( (O1LLO2LL)O1RL* O1LRO1RL*+ O1RR*O1LL+ O1RR*(O1LRO2LL*),
O1RR (O1LLO2LL)+O1RRO1LR+O1LLO1RL+(O1LRO2LL*)O1RL )
S1R(S1LS2L)* = (O1RL,O1RR) ( [O1LLO2LL O1LR]*, [O1LL+O1LRO2LL*] )
= ( O1RL[(O1LLO2LL)* O1LR*]+[O1LL*+(O1LRO2LL*)*]O1RR,
[O1LL+O1LRO2LL*]O1RL+O1RR[O1LLO2LL O1LR] )
= ( O1RL(O1LLO2LL)* O1RLO1LR* +O1LL*O1RR+(O1LRO2LL*)*O1RR ,
O1LLO1RL(O1LRO2LL*)O1RL+O1RR(O1LLO2LL) O1RRO1LR )
Putting these first two terms together:
+(S1LS2L)S1R*+S1R(S1LS2L)* =
( (O1LLO2LL)O1RL*+O1RL(O1LLO2LL)*
 O1LRO1RL*+ O1RR*O1LL O1RLO1LR* +O1LL*O1RR
+ O1RR*(O1LRO2LL*)+(O1LRO2LL*)*O1RR, 0)
For S1L*(S1RS2L*) we have:
(S1RS2L*)=(O1RL,O1RR)(O2LL*, ) = ([O1RLO2LL*+ O1RR], [O1RL+O1RRO2LL] )
So, S1L*(S1RS2L*) = (O1LL*,O1LR)([O1RLO2LL*+O1RR], [O1RL+O1RRO2LL] )
= ( O1LL*(O1RLO2LL*)+O1LL*O1RRO1RL*O1LR+(O1RRO2LL)*O1LR , term)
While for (S1RS2L*)*S1L have
(S1RS2L*)*S1L= ([O1RLO2LL*+ O1RR]*, [O1RLO1RRO2LL] )(O1LL,O1LR)
= ([O1RLO2LL*+ O1RR]*O1LLO1LR*[O1RLO1RRO2LL], - term)

## PDF page 10

676

Stephen Winters-Hilt

S1L*(S1RS2L*)+(S1RS2L*)*S1L=
( O1LL*(O1RLO2LL*)+(O1RLO2LL*)*O1LL
+O1LL*O1RRO1RL*O1LR+ O1RR*O1LLO1LR*O1RL
+(O1RRO2LL)*O1LR+O1LR*(O1RRO2LL), 0)
So have,
Z = ( {(O1LLO2LL)O1RL*+O1RL(O1LLO2LL)*
O1LL*(O1RLO2LL*)(O1RLO2LL*)*O1LL} +
{O1RR*(O1LRO2LL*)+(O1LRO2LL*)*O1RR
(O1RRO2LL)*O1LRO1LR*(O1RRO2LL)} +
 O1LRO1RL*+ O1RR*O1LL O1RLO1LR* +O1LL*O1RR
O1LL*O1RR+O1RL*O1LRO1RR*O1LL+O1LR*O1RL , 0)
Z = ({im}+{O1RL*O1LR+O1LR*O1RL O1LRO1RL* O1RLO1LR*} , 0)
Z = ({im}+{2Im{O1RL*O1LR} +2Im{O1LR*O1RL} , 0)
So again, have that Z = pure imaginary, and since it must be real, it is thus zero.
Thus, we have norm(B1B2) = 1. This proves the second extension, for unit-norm
propagators that are Bisedenions of the form BLeft=(SLeft,) or BRight=(,SRight), where
SLeft and SRight are sedenion propagators shown in the first extension, e.g.,
SLeft=(OLeft,). (Note that  is a purely real octonion, while  is a purely real
sedenion.)

8 The Formulation of the Problem: Bitrigintaduonion Propagation
After the bisedenions (also known as trigintaduonions) come the bitrigintaduonions,
the 64-component Cayley algebra (denoted by ‘T’ in following but later when I
reference the RCHO(ST) hypothesis, the ‘T’ refers to trigintaduonions). Let’s try
extending further to see if we can have norm(T1T2) = 1, when we build with a
similar extension method to define our unit-norm propagator: TLeft=(BLeft,) ,
BLeft=(SLeft,) , and SLeft=(OLeft,), where, as before, once we get to the octionic
Cayley level we are unrestricted (e.g., OLeft can be any octonion). Let’s see if we can
construct, as before, a T unit norm propagators of the form:
T(unit norm)  T(unit norm propagator) = T(unit norm)
T(unit norm) = T1(BLeft,BRight) = T1(BL,BR) = (B1L,B1R)
If T1 is unit norm, then norm(T1) = T1  T1* = 1, which for our notation means:
1 = (B1L,B1R)(B1L*,B1R) = ( [B1LB1L*+B1R*B1R], [B1RB1L+B1RB1L] )
1 = ( [norm(B1L)+norm(B1R)], 0 )
1 = norm(B1L)+norm(B1R)
T(unit norm propagator) = T2(BLeft,BReal) = (B2L, ) for the right bisedenion real  is
real and is the real part of the purely real right bisedenion.

## PDF page 11

Feynman-Cayley path integrals

677

If T2 is unit norm, then norm(T2) = T2  T2* = 1, which for our notation means:
1 = norm(B2L)+2
So we can now ask the question,
Does T(unit norm)  T(unit norm propagator), return a unit norm bitrigintaduonion
when using the special class of unit norm propagators indicated?

9 Failure of Proof construction for Norm(T1T2)=1,
computational proof of failure of Norm(T1T2)=1

and

(T1T2)=(B1L,B1R)(B2L, ) = ( [B1LB2L B1R], [B1L+B1RB2L*] )
(T1T2)* = ( [B1LB2L B1R]*, [B1L+B1RB2L*] )
norm(T1T2) = (T1T2)  (T1T2)*
= ( [B1LB2L B1R]  [B1LB2L B1R]* +[B1L+B1RB2L*]*  [B1L+B1RB2L*],
[B1L+B1RB2L*]  [B1LB2L B1R] + [B1L+B1RB2L*]  [B1LB2L B1R])
= ( norm(B1LB2L)+norm(B1RB2L*)+2 norm(B1R)+2 norm(B1L)
(B1LB2L)B1R*B1R(B1LB2L)*+B1L*(B1RB2L*)+(B1RB2L*)*B1L, 0)
To proceed as before we need to show that the norm property norm(xy) =
norm(x)norm(y) holds for the bisedenions when one of them is constrained to be in
the form of the bisedenion propagator, e.g., does norm(B1LB2L) =
norm(B1L)norm(B2L) where B2L is in the form of the bisedenion propagator?
norm(B1LB2L) = (B1LB2L)  (B1LB2L)*
= ( [S1LLS2LL S1LR]  [S1LLS2LL S1LR]* +
[S1LL+S1LRS2LL*]*  [S1LL+S1LRS2LL*],
[S1LL+S1LRS2LL*]  [S1LLS2LL S1LR] +
[S1LL+S1LRS2LL*]  [S1LLS2LL S1LR])
= ( norm(S1LLS2LL)+norm(S1LRS2LL*)+2 norm(S1LR)+2 norm(S1LL)
(S1LLS2LL)S1LR*S1LR(S1LLS2LL)*+
S1LL*(S1LRS2LL*)+(S1LRS2LL*)*S1LL, 0)
Now that we’ve reduced to this level we see there is a problem. In the prior reduction
we arrived at the variables being octonions at this stage, for which the norm property
and braid laws of the octionoic composition algebra allowed norm(O1LLO2LL) =
norm(O1LL)norm(O2LL) and showed the non-norm terms were zero by manipulations
using the braid laws that hold for the composition algebras. Now that we’ve moved to
the next higher Cayley algebra’s in the derivation, and in our extension construction,
we now are asking the sedenions to act as a composition algebra to proceed (on an
unrestricted part of the Sedenion algebra). The construction fails. Thus, the extension

## PDF page 12

678

Stephen Winters-Hilt

process does not extend past the Bisedenions, it basically requires the Cayley algebra
at two Cayley levels lower to still be a composition algebra. It is still possible to
extend to the bisedenions because at two levels lower you still have the octonions,
which are a composition algebra as needed. Computationally we see a failure to
propagate the bitrigintaduonions so this is consistent.

The key software solution to discover/verify the results computationally is a the
recursive Cayley definition for multiplication, which avoids use of lookup tables and
avoids commutation and associativity issues encountered at higher order. It is shown
next. The cayley subroutine takes the references to any pair of Cayley numbers
(represented in list form, so represented as simple arrays), and multiplies those
Cayley numbers and returns the Cayley number answer (in list form, thus an array).
The main usage was with randomly generated unit norm Cayley numbers that were
multiplied (from right) against a “running product”. Tests on unit norm hold for
millions of running product evaluations in cases where there the unit norm
propagations are validated, so, like the perfectly meshed gears of a machine, or the
perfectly ‘braided’ threads of a very long string.

10 The Code
---------------------------------- cayley_multiplication.pl -------------------------------------------sub cayley {
my ($ref1,$ref2)=@_;
my @input1=@{$ref1};
my @input2=@{$ref2};
my $order1=scalar(@input1);
my $order2=scalar(@input2);
my @output;
if ($order1 != $order2) {die;}
if ($order1 == 1) {
$output[0]=$input1[0]*$input2[0];
}
else{
my @A=@input1[0..$order1/2-1];
my @B=@input1[$order1/2..$order1-1];
my @C=@input2[0..$order1/2-1];
my @D=@input2[$order1/2..$order1-1];
my @conjD=conj(\@D);
my @conjC=conj(\@C);
my @cay1 = cayley(\@A,\@C);
my @cay2 = cayley(\@conjD,\@B);
my @cay3 = cayley(\@D,\@A);
my @cay4 = cayley(\@B,\@conjC);
my @left;
my @right;
my $length = scalar(@cay1);
my $index;
for $index (0..$length-1) {
$left[$index] = $cay1[$index] - $cay2[$index];
$right[$index] = $cay3[$index] + $cay4[$index];

## PDF page 13

Feynman-Cayley path integrals

679

}
@output=(@left,@right);
}
return @output;
}

---------------------------------- cayley_multiplication.pl --------------------------------------------

11 Discussion
Consider the Feynman-Cayley Path Integral, where we extend the notion of all paths
with path integration generally involving a real or matrix object to all paths with all
higher-dimensional Cayley algebras and their propagating sub-algebra (loop) objects.
It is hypothesized that the usual configuration space path integral construction in this
larger Cayley space domain can be undertaken in a straightforward manner, allowing
many choices to be resolved, or explained, from what is allowed within that
formulation. Let’s suppose the following was possible:
(1) Reality can be described in terms of a completely multiplicative propagator.
(2) The Path Integral formalism selects against fields involving algebras with zero
divisors, and loss of braid laws, thereby reducing to a RCHO(ST) based theory, where
equilibrium and martingale constructs occur asymptotically.
(3) The path integral formalism resuling from the propagotor has two forms, the
Feynman-Cayley Path Integral and Weiner Path Integral, according to the
introduction of an analytic (complex) time parameter, where the forms are related via
Euclideanization.
The central role of path integrals and of time Euclideanization is posited as
fundamental in and of itself. The core hypothesis is that complex wavefunctions can
be written in a path integral formalism with propagators that involve fields based on
Cayley algebras at all orders. The Cayley algebras with no zero divisors include the
Real Numbers (R), the Complex Numbers (C), the Quaternions (Q), and the
Octonians (O). And what is shown is here is how to extend by two more dimensions
beyond the octonions, and in the lower algebras the same methods suggest subalgebras (e.g., quaternions have four dimensions, if they were extended would
possibly have five and six dimensional subalgebras of the octonions and sedenions,).
The stationary phase of a solution, or highly peaked density of states in the
Euclideanized time domain, is not possible for fields over the Cayley algebra’s that
have zero divisors, e.g., that are no longer composition algebras. The zero divisors are
posited to disrupt all such higher order Cayley field propagations, thereby eliminating
them from path integral considerations except when such a short step is taken that the
likelihood of a disruptive (to phase or cohesion) zero divisor occurrence is low. In the

## PDF page 14

680

Stephen Winters-Hilt

extension proofs it was shown how a normed algebra allowed for the braid laws to be
valid, which were used repeatedly in the extension proofs. So just as critical as
disruption due to zero divisor is disruption in unit norm propagation due to loss of
‘braiding’. (It is conceivable that you might operate in a sector, where you are not
free to multiply anything together, and the zero divisor problem is avoided, the
braiding failure, however, is still unavoidable.)
A number of embedded Cayley algebra’s arise in a natural way. Recall that embedded
in a Cayley algebra at any order above quaternionic, there is a quaternionic subalgebra. Similarly, within that quaternionic algebra is a complex sub-algebra. The
embeddings on sub-algebras works for octonians within higher order Cayley algebras,
also, but beyond that the sub-algebras don’t appear to embed (so only have a C  H 
O embedding description within the higher order Cayley algebras).

The RCHO(ST) hypothesis, motivated by Maxwell, Feynman and Cayley, may be
able to directly encode the standard model and statistical mechanics, as well as
provide a unified framework whereby matter/antimatter (possibly from braiding since
there are two types of braiding), boson/fermion (from choice of chiral octionic
sector), and light/dark matter or energy (from choice of chiral sedenionic sector), may
be encoded. A variational formalism at the level of the10 dim spacetime description
may allow quantum gravity by use of the renormalizability of the (10 dim) string
theories.

12 Conclusion
The Feynman-Cayley path integral appears to indicate a (1,9) spacetime setting,
sufficient to encompass the standard model [10-14,17] and explain other, chiral,
structures of matter. The 10-dim spacetime indicated by the RCHO(ST) hypothesis is
also consistent with the 10 dimensions indicated by string theory.
Other forms of multiplication rule (than Cayley) are very useful, one being scalarvector representations that ties into representing physics equations in compact form
[17]. Descriptions of the standard model in terms of hypercomplex mathematics is
described in [10-14, 17].

Generalization of the N-square theorem is discussed by Rajwade in [20]. Rajwade
defines generalized N-square theorems to exist when a triple of integers (P,Q,R) are
admissible, where admissible occurs if and only if the product of a sum of P squares
and a sum of Q squares is a sum of R squares (over some field). The standard Nsquare theorem is that (N,N,N) is admissible for N=1,2,4,8, paralleling the
dimensionality of the composition algebra in which they operate. So have (1,1,1) for
the reals, (2,2,2) for the complex numbers, (4,4,4) for the quaternions, and (8,8,8) for
the octonions. Rajwade shows that (16,16,16) is NOT admissible, but that (16,16,32)

## PDF page 15

Feynman-Cayley path integrals

681

is admissible over the reals. The results here appear to partly overlap with Rajwade’s
results and suggests additional admissible triplets:(8,8,16),for products of special
sedenion propagator;(16,8,16) for norm one propagation using sedenion propagator;
(16,16,32), for products of bisedenion propagator (in agreement with Rajwade); and
(32,16,32), for norm one propagation using the bisedenion propagator.

This work appears to relate to efforts to describe a left loop on the 15-sphere and
examining sub-loops on the sedenions [21, 22], suggesting that similar subloops may
be found in the bisedenions as well (but not in higher order Cayley algebras).

Other than a new link to string theory, consistent with the 10-dim theory, the
hypercomplex formulation indicated here may indicate what dimensional reductions
will relate to experiments involving the standard model, and the natural chirality of
the formalism also allows for an explanation for Dark matter, all in a mathematics
that can be absorbed into a Lagrangian formulation that could be consistent with a
theory of Gravity.

References
[1] P.M. Harmon, Editor, The Scientific Letters and Papers of James Clerk Maxwell
II, Cambridge University Press, 1995, 570–576.
[2] T.L. Hankins, Sir William Rowan Hamilton, Johns Hopkins Press, 1980, 316–319.
[3] F.J. Dyson, Feynman’s proof of the Maxwell equations, Am. J. Phys., 58 (1990),
209-211. http://dx.doi.org/10.1119/1.16188
[4] F. J. Dyson, Feynman at Cornell, Phys. Today, 42 (1989), no. 2, 32-38.
http://dx.doi.org/10.1063/1.881190
[5] R. J. Hughes, On Feynman’s proof of the Maxwell equations, Am. J. Phys., 60
(1992), no. 4, 301. http://dx.doi.org/10.1119/1.16921
[6] Z.K. Silagadze, Feynman’s derivation of Maxwell equations and extra
dimensions, Annales de la Fondation Louis de Broglie, 27 (2002), no. 2, 241.
[7] C.A. Manogue and J. Schay, Finite Lorentz Transformations, Automorphisms,
and Division Algebras, J. Math. Phys., 34 (1993), no. 8, 3746-3767.
http://dx.doi.org/10.1063/1.530056
[8] C.A. Manogue and A. Sudbery, General solutions of covariant superstring
equations of motion, Phys., 40 (1989), 4073.

## PDF page 16

682

Stephen Winters-Hilt

http://dx.doi.org/10.1103/physrevd.40.4073
[9] M. Cederwall, Octonionic particles and the S7 symmetry, J. Math. Phys., 33
(1992), 388. http://dx.doi.org/10.1063/1.529919
[10] M. Gogberashvili, Octonionic electrodynamics, J. Phys. A: Math. Gen., 39
(2006), no. 22, 7099. http://dx.doi.org/10.1088/0305-4470/39/22/020
[11] B.C. Chanyal, P.S. Bisht and O.P.S. Negi, Generalized Octonion
Electrodynamics, 49 (2010), no. 6, 1333-1343.
http://dx.doi.org/10.1007/s10773-010-0314-5
[12] V. Kravchenko, Quaternionic equation for electromagnetic fields in
inhomogenous media, 2003, 361-366.
http://dx.doi.org/10.1142/9789812794253_0042
[13] F.D. Smith, Jr., Standard Model plus Gravity from Octonion Creators and
Annihilators, Quant-ph/9503009.
[14] Pushpa, P.S. Bisht, T. Li, and O.P.S. Negi, Quaternion Octonion Reformulation
of Quantum Chromodynamics, Int. J. Theor. Phys., 50 (2011), no. 2, 594-606.
http://dx.doi.org/10.1007/s10773-010-0579-8
[15] J.H. Conway and D.A. Smith, On Quaternions and Octonions: their Geometry,
Arithmetic, and Symmetry, A K Peters, Wellesley, Massachusetts, 2005.
[16] J.C. Baez, The Octonions, Bull. Amer. Math. Soc., 39 (2002), 145-205.
http://dx.doi.org/10.1090/s0273-0979-01-00934-x
[17] V.L. Mironov, S.V. Mironov, Associative Space-Time Sedenions and Their
Application in Relativistic Quantum Mechanics and Field Theory, Applied
Mathematics, (2015), no. 6, 46-56. http://dx.doi.org/10.4236/am.2015.61006
[18] F.D. Smith, Jr., Standard Model plus Gravity from Octonion Creators and
Annihilators, quant-ph/9503009.
[19] V. Chrisitianto, F. Smarandachey, A Derivation of Maxwell Equations in
Quaternion Space, April, Progress In Physics, 2 (2010), 23-27.
[20] A.R. Rajwade, Squares, Cambridge, 1993.
http://dx.doi.org/10.1017/cbo9780511566028
[21] J.D.H. Smith, A Left Loop on the 15-sphere, Journal of Algebr, 176 (1995), no.
1, 128-138. http://dx.doi.org/10.1006/jabr.1995.1237

## PDF page 17

Feynman-Cayley path integrals
683
[22] B.M. Kivunge, J. D. H Smith, Subloops of sedenions, Comment. Math. Univ.
Carolin., 45 (2004), no. 2, 295–302.
Received: August 21, 2015; Published: October 23, 2015
