Source: https://doi.org/10.12988/astp.2018.8832
PDF sha256: 968c263dfe079d08b343864a5e39a00aef467ac5c5a6ed7619c96ea42b59069b
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of winters-hilt-2018-22-letters-of-reality.pdf

Transcription of `winters-hilt-2018-22-letters-of-reality.pdf` in this directory, 18 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-18 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Advanced Studies in Theoretical Physics
Vol. 12, 2018, no. 7, 301 - 318
HIKARI Ltd, www.m-hikari.com
https://doi.org/10.12988/astp.2018.8832

The 22 Letters of Reality: Chiral Bisedenion
Properties for Maximal Information Propagation
Stephen Winters-Hilt
Math and Computer Science Department
Western State Colorado University, USA
&
Meta Logos Systems, USA
Copyright © 2018 Stephen Winters-Hilt. This article is distributed under the Creative Commons
Attribution License, which permits unrestricted use, distribution, and reproduction in any medium,
provided the original work is properly cited.

Abstract
Unit norm multiplicative propagation is possible beyond the level of octonions,
into a 10-dimensional subspace of the bi-sedenions (where the first six Cayley
algebras go as: real, complex, quaternion, octonion, sedenion, trigintaduonion aka
bi-sedenion). The resultant, strictly unitary, propagation in 10-dim is more
recently found to be extendable to a perturbatively stable unitary propagation if
the perturbation amplitude is at most alpha (the fine-structure constant). Thus, the
prior exploration also provides a computational/theoretical framework for
derivation of alpha via the maximum perturbation limit for chiral trigintaduonion
propagation. In this work we look at the propagation of ‘maximal information’,
where we work with multiplicative bi-sedenion algebraic evolution when each
multiplicative ‘step’ involves a unit-norm chiral bisedenion with perturbation
contribution allowed in the nearby general bi-sedenion algebra up to the maximal
magnitude of alpha. An analysis of alpha-propagation (where the amplitude is
strictly at alpha) with perturbation concentrated in each of the 22 non-propagating
dimensions is done. Results are shown for the resulting 22 emergent parameters,
or “letters” of reality.
Keywords: Path Integral, Generalized Propagator; Cayley Algebra; 22 letters; 137

1 Introduction
It has long been a mystery as to why so many languages, both man-made and

## PDF page 2

302

Stephen Winters-Hilt

natural, should have arrived at language encoding schemes involving 22 letters (or
22 emergent parameters, such as for the Standard Model with vMSM extension).
In this paper further work with bi-sedenions is shown that builds on prior work [1,
2], and it is explained why 22-letter schemes are actually optimal. Furthermore,
when working with the ‘optimal’ 22-letter encoding schemes, there anomalously
appears the number ‘137’ across all such schemes as a key parameter (in physics)
or scoring (in Babylonian/Hebrew gematria encoding [3], itself an elaborate bisedenion optimization). The occurrence of ‘137’ is now explained as a simple
feature of the bi-sedenion maximal information propagation described in [2].
The Feynman-Cayley Path Integral proposed in [1, 2] involved use of chiral bisedenions in an effort to identify a mathematical framework within which to have
a unified propagator theory (and maximal information propagation was sought for
such a hypothesized propagator). At its root, this is a hypothesis for an algebraic
reality, with algebraic elements describing ‘reality’ and algebraic multiplicative
processes underlying propagation. All of the different ‘paths’ of propagation are
then brought together in a sum – where stationary phase is selected out and the
variational calculus basis for much of physics then takes over to offer all of the
familiar elegant solutions of classical physics.
When speaking of ‘propagation’ for the algebra we mean preservation of unit
norm with each multiplicative operation underlying the propagation steps. Recall
that the classic definition for the normed division algebras is that
N(xy)=N(x)N(y), where unit norm propagation is possible (Hurwitz’s theorem)
for multiplication by a unit norm member of the normed division algebras: real,
complex, quaternion, and octonion algebras. The higher Cayley algebras
(sedenion, bi-sedenion, and beyond) then fail to have a norm for the higher
Cayley algebras, particularly the next two Cayley algebras in the hierarchy. In [1]
it was shown how one-dimensional chiral extensions were possible into the
sedenion algebra, and again into the bi-sedenion algebra, but then no further.
Previously efforts to embed the standard model of physics were restricted, if
propagation of unit norm was desirable, to a standard octonion with its eight
components (minus one free component due to unit norm constraint, giving rise to
an element of S7). Using the aforementioned chiral extensions, a larger space of
viable propagators is possible [1], that offers more ‘room’ to accommodate the
standard model, and that also has natural chiral properties, as already observed in
the standard model.
In this paper we will begin with the theoretical expression for a general element of
the bi-sedenion algebra after two chiral bi-sedenion multiplicative propagation
steps. A simple analysis of the number of terms in this expression, when reduced
to three-element algebraic ‘braid-level’, results in a count on algebraic braids of 137,

## PDF page 3

22 letters of reality: chiral bisedenion properties …

303

plus a little extra (e.g. some lagniappe for the best ‘cooking’) of a contribution
towards a 138th braid, that involves a complex-dimensional extension outside the
10-dim propagation. Further work is then done, computationally, to determine the
22 parameters that emerge. A theoretical/computational discussion for why
parameters should emerge, and do so in a stable manner, is given as well.

2 Background on Cayley Algebras
I reproduce here the very brief background on Cayley algebras from [1], much
more extensive background can be found at [4].
The list representation for hypercomplex numbers will make things clearer in
what follows so will be introduced here for the first seven Cayley algebras:
Reals: X0  (X0) .
Complex: (X0 + X1 i)  (X0 , X1 ) .
Quaternions: (X0 + X1 i + X2 j + X3 k)  (X0 , X1 , X2 , X3)  (X0 , … , X3) .
Octonions: (X0 , … , X7) with seven imaginary numbers.
Sedenions: (X0 , … , X15) with fifteen imaginary numbers.
Trigintaduonions (a.k.a Bi-Sedenions): (X0 , … , X31) with 31 imaginary numbers.
Bi-Trigintaduonions: (X0 , … , X63) with 63 types of imaginary number.
Consider how the familiar complex numbers can be generated from two real
numbers with the introduction of a single imaginary number ‘i’, {X0 , X1}  (X0
+ X1 i). This construction process can be iterated, using two complex numbers,
{Z0 , Z1} , and a new imaginary number ‘j’:
(Z0 + Z1 j) = (A+Bi ) + (C+Di ) j = A+Bi + Cj +Dij = A+Bi + Cj +Dk,
where we have introduced a third imaginary number ‘k’ where ‘ij=k’. In list
notation this appears as the simple rule ((A,B),(C,D)) = (A,B,C,D). This iterative
construction process can be repeated, generating algebras doubling in
dimensionality at each iteration, to generate the 1, 2, 4, 8, 16, 32, and 64
dimensional algebras listed above. The process continues indefinitely to higher
orders beyond that, doubling in dimension at each iteration, but we will see that
the main algebras of interest for physics are those with dimension 1, 2, 4, and 8,
and sub-spaces of those with dimension 16 and 32 dimensional algebras.
Addition of hypercomplex numbers is done component-wise, so is
straightforward. For hypercomplex multiplication, list notation makes the freedom
for group splittings more apparent, where any hypercomplex product ZxQ to be
expressed as (U,V)x(R,S) by splitting Z=(U,V) and Q=(R,S). This is important

## PDF page 4

304

Stephen Winters-Hilt

because the product rule, generalized by Cayley, uses the splitting capability. The
Cayley algebra multiplication rule is:
(A,B)(C,D) = ([ACD*B],[BC*+DA]),
where conjugation of a hypercomplex number flips the signs of all of its
imaginary components:
(A,B)* = Conj(A,B) = (A*,B)
The specification of new algebras, with addition and multiplication rules as
indicated by the constructive process above, is known as the Cayley-Dickson
construction, and this gives rise to what is referred to as the Cayley algebras in
what follows.
The key software solution to discover/verify the results computationally is the
recursive Cayley definition for multiplication, which avoids use of lookup tables
and avoids commutation and associativity issues encountered at higher order. It is
shown in the Methods. Further details on Cayley algebras, and the Sedenions and
Bi-Sedenions in particular, are given in [1, 4].

3 Methods
The Cayley subroutine takes the references to any pair of Cayley numbers
(represented in list form, so represented as simple arrays), and multiplies those
Cayley numbers and returns the Cayley number answer (in list form, thus an
array). The main usage was with randomly generated unit norm Cayley numbers
that were multiplied (from right) against a “running product”. Tests on unit norm
hold for millions of running product evaluations in cases where the unit norm
propagations are validated (running like the perfectly meshed gears of a machine,
or the perfectly ‘braided’ threads of a very long string).
The bignum module was used with 50 decimal places of precision in most
experiments, with some experiments at 100 decimal places of precision in further
validation testing. Using bignum allows much higher precision handling (needed
for the iterative processes of repeated multiplicative updates). The use of bignum,
however, entails number representation/storage via strings and is vastly slower
than normal arithmetic operations. Furthermore, modern GPU enhancements are
not possible with the string handling intermediaries, so the resultant
computational threads are CPU intensive and slow.

## PDF page 5

22 letters of reality: chiral bisedenion properties …

305

---------------------------------- cayley_multiplication.pl ------------------------------------------# using bignum
sub cayley {
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
}
@output=(@left,@right);
}
return @output;
}

---------------------------------- cayley_multiplication.pl -------------------------------------------

Unit-norm multiplicative ‘step’ generation method (same as used in [2])
The randomly generated propagation step is for a unit norm that has a randomly
generated small perturbation. Consider the eight element octonion denoted: {x0,
x1, x2,…x7}, where the real component is x01:
(x0)2 = 1 -  (xi)2 ,
And where each xi is generated by a randomly generated number uniformly
distributed on the interval (-0.5 .. 0.5), with an additional perturbation-factor ‘‘,

## PDF page 6

306

Stephen Winters-Hilt

e.g., the max magnitude imaginary perturbation from pure real (x0=1), measured
with L1 norm, is simply 7 times /2 (for seven imaginary components).
For the octonions unrestricted unit norm propagation is possible, i.e., all of the
components can be independently generated and then normalized to have L2 norm
=1. So, the restriction to x01 isn’t needed. The same is true on the (left) chiral
extension spaces:
Propagating chiral left sedenion: {x0, x1, x2,…x7, x8}, with x9=0,
…, x15=0,
and the
Propagating chiral left bi-sedenion: {x0, x1, x2,…x7, x8, x16}, with
x9=0, …, x15=0,x17=0, …, x31=0.
Consider now the propagating chiral left bi-sedenion with the a small nonpropagating component (here x9 nonzero is chosen), and now let’s return to
formally requiring x01 on propagation steps:
Propagating small perturbation chiral left bi-sedenion: {x0, x1,
x2,…x7, x8, x9, x16}, with x10=0, …, x15=0,x17=0, …, x31=0.
For the small perturbation steps that are randomly generated, there are now ten
imaginary components, so in what follows, the maximum magnitude of the
imaginary components, measured with L1 norm, denoted , is =10/2=5.

4 Results
4.1 Theoretical
Consider a general norm=1 bisedenion in list notation: (A,B), where A and B are
sedenions. Consider a propagator bisedenion (C,), C = (c,), where c is an
octonion and  is shorthand for the real octonion (,0,0,0,0,0,0,0), where  is a
real
number,
and

is
shorthand
for
the
real
sedenion
(,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0), where  is a real number. Using A=(a,b), B=(u,v),
and the multiplication rule from Sec. 2, we have:
(A,B)(C,) = ([AC-*B], [BC*+A]), where
AC = (a,b)(c,) = ([ac-*b],[bc*+a]); BC*=(u,v)(c*,-) = ([uc*+*v],[vc*u]).
Thus, we have:
(A,B)(C,) = ([(ac-*b , bc*+a)-*(u,v)] , [(uc*+*v , vc-u)+(a,b)]), so,

## PDF page 7

22 letters of reality: chiral bisedenion properties …

307

(A,B)(C,) = ([ac-*b-*u , bc*+a-*v] , [uc*+*v+a , vc-u+b]).
Now consider another propagator bisedenion (C,), C = (c,), and form the
product corresponding to the next multiplicative step:
( (A,B)(C,) ) (C,) = ( [(ac)c - *bc - *uc - *(bc*+a-*v) , …] , [… , …]
), where only the first expression at octonionic level is shown. Notice how the
expression is comprised of terms with three octonionic factors. In [1] are
described the ‘braid laws’ for multiplication involving three octonions, which can
be used here to uniquely order any octonion product with an ordering simply
corresponding to their list order.
Returning to the first product expression at octonionic level:
(ac)c - *bc - *uc - *(bc*+a-*v).
Notice how the first three terms involve c, the octonionic part from the latest
propagation, while the next three terms do not, only involving the chiral sedenion
part from the latest propagation step. The term **v contributes to the
collection of terms with c, to complete a set of 10-choose-3 braids (after
reordering to list order using the braid rules), giving rise to 10x9x8/3x2 = 120
terms, or independent ‘braids’ of algebraic information transmission. The **v
term also gives rise to an independent term when further propagations are
considered (than the last two), where, for example, there is a term *(*)nv from
which results 8 independent braid terms traceable to ‘v’. Similarly, the *a term
is part of a more general ‘telescoping’ on  chiral terms: *()na, where again, 8
independent braid terms result traceable to ‘a’. The term *a shows how
original information at the octonionic level is transmitted via two, purely real,
chiral sedenions, bounded to have unit norm at most. The ‘a’ octonion is arbitrary,
involving eight independent octonion parameters, thus eight possible terms. The
same description holds for the expansion (with more propagation multiplications)
of the **v term, except now we see the beginning of mixing on the real
octonions from the sedenion and bisedenion levels, but bounded with norm less
than one, and with another eight information transmission ‘braids’.
All of the octonion products involve octonions with norms at most unity, and by
the normed division algebra rules on octonions, their norm is simply the norm of
the individual octonions multiplied together, all of which are bounded by unity,
thus their product is bounded by unity. The overall bound for the expression, each
individual term being bounded by unity, is therefore simply the counting on the

## PDF page 8

308

Stephen Winters-Hilt

independent terms. This brings the total number of independent terms, each
bounded by one, to 136, with one term left to be addressed.
The last term to be addressed is *bc*. The term describes the first bisedenion’s
‘b’ octonion component multiplied by the first propagator bisedenions ‘c*’
octonion, followed by the last propagation with a real octonion (from the chiral
sedenion). The generation of more terms, in general, with repeated propagation
steps, and eventually repeated multiplication on octonions, is expected to select
out the real octonion in this term. The ‘bc*’ octonion product can be viewed as the
first of a lengthy chain product of octonions as more multiplicative steps are
made, e.g., the last term generalizes (with more propagation multiplication steps)
to include terms like: *b(c*)n. Just like a multiplication involving a random
collection of unit norm complex numbers (motions on S1) will result in
cancellation of the complex components only leaving the real part, the same hold
true for multiplications of unit norm octonions (corresponding to motions on S7),
with cancelation down to a real octonion, giving rise to one more, real, term to
bring the total to 137 independent braid channels. The problem with this last
analysis, however, is that the octonions don’t have unit norm (they are bounded
by unit norm, and the bi-sedenion of which they are part has unit norm), although
they do have an approximately unit norm. So what results is a 137th channel from
the added real channel already indicated, but there is also a non-real remnant
(giving rise to a fraction of an additional channel). In other words, the maximum
magnitude of the real component of the octonion in the product term is given with
a ‘channel multiplier’ of 137. In seeking the maximum information propagation,
we require that the real component never cross zero, thus the strictest condition on
evaluating evolution is when the imaginary components have real component
contribution that is antiphase, e.g., the imaginary angle is , such that the real
component contribution is cos() = 1, bringing the real component closer to the
zero crossing. We would limit the maximum perturbation allowable by this worst
case. Other cases of complex phase n, n odd, are possible to get the maximal real
limitation, but give rise to less strict constraint on the perturbation limit, thus
singling out the cumulative complex angle to be .
If the magnitude is 137, and the (cumulative) imaginary component is , then the
real component of the octonion (containing the real part of the propagation bisedenion) is simply: 137 cos (/137). This gives us an estimate of the ‘channel
multiplier’ mentioned previously, but requires rescaling to be properly normalized

## PDF page 9

22 letters of reality: chiral bisedenion properties …

309

in the full bisedenion space. When arriving at the ‘cumulative’ imaginary phase,
of , there were 29 achiral imaginary component that were free to contribute,
uniformly, each with the phase angle /29. Their L1 phase addition then gave rise
to the ‘’ cumulative phase used thus far. In the non-normalized magnitude
evaluation, the 29 achiral components would be described as having imaginary
magnitude /29 and real magnitude 137, with complex angle /(137*29), thus real
component is [/(137*29)]cos([/(137*29)]). When in the renormalized setting,
however, we expect the real component to be sin([/(137*29)]). So the channel
multiplier upon rescaling is:
M = 137 cos (/137) { sin(/(137*29)) / [/(137*29)cos(/(137*29))] },
Or, using the notation tanc(x) = tan(x)/x, this becomes:
M = 137 cos (/137) tanc(/(137*29)).
So, the worst-case channel multiplier, M, times the maximum perturbation
allowed, must be less than 1, to prevent breaking the norm<1 bounds and realcomponent zero-crossing. Thus, the maximum perturbation, alpha, allowed is
alpha*M=1, thus,
1/alpha = 137 cos (/137) tanc(/(137*29)) = 137.035999786699.
This theoretical expression for the fine-structure constant first appeared in Gilson
[10], but it wasn’t clear in that effort why the number ‘29’ should appear, nor the
origin of the trig terms. In this derivation of the expression, we see that the
number 29, etc., simply results from the number of achiral imaginary components
(that are unconstrained, unlike the two chiral imaginary components) in the
trigintaduonions.
To recap, in the perturbative setting, each of the terms at lowest order would
involve one perturbation parameter factor, and would be bounded by the 137 (plus
a fraction) terms involved times the amount of the maximum perturbation
allowed. We want the starting ‘general’ bi-sedenion, and any subsequent bisedenion resulting from stepwise multiplicative propagation, to have total
perturbation less than 1:
(perturbation) x 137.03599 < 1, thus maximum perturbation is at 1/137.035999.
At this juncture, therefore, we have a theoretical explanation for the alpha
parameter shown that was derived computationally in [2].
In computational experiments in the next subsection, building on the results from
[2], the emergent parameters of the theory are determined. In the 32 dim bisedenion space, where chiral propagation was in only 10 of those dimensions, the

## PDF page 10

310

Stephen Winters-Hilt

other 22 dimensions give rise to 22 emergent parameters (or ‘letters’), and this is
what is shown in the next section. Before doing this, however, further theoretical
description is needed for the 22 types of perturbations considered in the datarun
results.
Consider an “on-shell” propagator bisedenion as before (C,), C = (c,), where c
is an octonion and  is shorthand for the real octonion (,0,0,0,0,0,0,0), where 
is a real number. Now consider a bisedenion propagator perturbed “off-shell”
(norm = 1, but have non-zero component outside the 10 dim chiral bised subalgebra): (C,), C = (c,(,)), where (,) is shorthand for (,0,0,0,,0,0,0),
which is described as the x12 perturbation case in Sec. 3. The x9 perturbation
case in Sec. 3 would be (,,0,0,0,0,0,0), for which computational results are
shown in the next section. Further theoretical derivation is done for the x12
perturbation case in the next few expressions since it’s easiest to work with using
the Cayley multiplication rules:
(C,)(C,) = ([cc - (,)*-* , c*+(,)c] , [c+c , -(,)] ),
where
the added terms with component-level perturbation involve the  terms above.
Consider the first term with :
(,)* = (*,-) = (*,-)(,0) = (* , -*), where ’s shift from real
octonionic to real quaternionic. A different ‘noise injection’ than at parameter x12
would project out a different portion of the propagation.
4.2 Computational
In the tables that follow are shown the emergent parameters when alphaperturbations (perturbations with max perturbation alpha) are injected for each of
the 22 non-propagating parameters. Regardless of injection parameter, if
perturbation exceeds alpha, the norm=1 relation fails, and propagation eventually
dies with norm  0. This is to be expected given the identification of alpha as the
max-perturbation limit in [2]. What is odd is that if perturbation is less than alpha,
but still in the vicinity of alpha, norm=1 behavior appears to eventually fail (after
millions of iterations, and using bignum precision) as can be seen in the real
component eventually falling to zero. In other words, the iterative procedure
underlying the propagator definition, not surprisingly, is giving rise to fractal
behavior (and abrupt transitions). I say not surprisingly because the single
parameter noise injection that we are using (in repeated multiplicative iterations)
is such that we’ve set up an iterative process with a 1-dim parameter space and are

## PDF page 11

22 letters of reality: chiral bisedenion properties …

311

seeing possible fractal behavior -- a well-known phenomenon in 1-D complex
systems. Thus, the results that follow are preliminary estimates on the ‘letters of
reality’ (actually numbers in this numerogenesis algebraic theory) in that both the
noise injection method can lead to artifacts, and due to the slow process of doing
bi-sedenion multiplication with bignum(50).
In the experiments tabulated in what follows we consider unit norm chiral bisedenion propagation. In particular, we consider unit element chiral bisedenion
propagations, with alpha perturbations introduced, separately, at each of the nonpropagating bi-sedenion parameters. If working with a perturbation greater than
alpha we expect the real component to start at one (we begin with a unit element
chiral bisedenion) and eventually decay to zero, and cross-over to negative values,
as it begins to randomly walk. To a lesser extent, and with fractal structure, this
also appears to be true for perturbations introduced that are in the vicinity of alpha
but less than alpha. For perturbations precisely at ‘alpha’, we expect the real
component to decay/search for a while, but to then asymptote/lock-on to a
particular non-zero (emergent) value with well-defined variance about that
asymptote, and never crossing zero. In other words, if we want to propagate one
bit of information via the real component asymptote of the bi-sedenion
indefinitely, it is hypothesized that we can do so using alpha perturbation
propagators. In Fig. 1 is shown the Histogram on real components (rc)
observations after each multiplicative iteration, where an emergent rc=0.971
appears in the first 60,000 propagation iterations.
To recap, for ‘off-shell’ bi-sedenion propagation at maximum perturbation
amplitude alpha, we examine the behavior of the real component (rc) of the bisedenion. This is because we are effectively describing propagation starting with a
unit bi-sedenion (so only have rc=1 nonzero), followed by multiplicative
propagation steps by way of bisedenions perturbed by at most the fraction alpha
into the bisedenions 31 imaginary components. As described in Sec. 4.1, we
consider each of the 22 possible non-propagating parameters in separate
perturbation-at-alpha analyses, where the emergent behavior on the rc value is
obtained. For the ‘alpha propagation’, where noise injection is solely in a
particular non-propagating component, we expect the rc component to decay but
to eventually asymptote to a positive value (and never cross zero). The Results in
Table 1 show the emergent 22 parameters when propagation is done with
precisely alpha perturbation, where alpha is taken to be the highest precision value
known provided by QED (1/137.035999070) [5, 6] (which appears via
=0.001459470514006 in the code).

## PDF page 12

312

Stephen Winters-Hilt

Fig. 1. Histogram of real-component values observed in the first 60,000 iterations
of alpha propagation, where the perturbation parameter is x30. As the propagation
begins the RC value is at 1.0=10,000/10,000, so at the rightmost dot in the
histogram. As the multiplicative operations proceed, the rc value decays thru the
range to rc =0.9750, then begins to catch the asymptote with mean at 0.9710.

The alpha propagations are examined for each of the 22 different non-propagating
components, with each taken individually as sole source of non-propagating
perturbation in its respective alpha propagation experiment. Since this process is
selecting propagators somewhat arbitrarily, perhaps not as much utility can be
extracted from the asymptotic RC values as from their variance information. In
other words, by injecting noise perturbations into each of the 22 parameters
separately (like playing a recorder with only one hole depressed at a time),
computational experiments are attempting to arrive at information respective to 22
parameters, but may do so in a mixed form not so useful when expressed in the
RC values. Furthermore, the Gaussian distributions that appear to be emergent at
the asymptotes have variance values (or their inverses as shown in Table 1) that
may provide the most utility. In essence the variance can be thought of as
describing a statistical restoring force that’s occurring in the bi-sedenion
propagation due to the odd properties of bisedenion in general, e.g., they are: nonassociative, non-commutative, have zero-divisors, and lack of inverse due to lack
of norm. Bisedenion properties are not theoretically fully understood at this time,
thus the computational efforts described here (and in [1, 2]) to try to resolve
matters further.

## PDF page 13

22 letters of reality: chiral bisedenion properties …

Off-shell
parameter
x9
x10
x11
x12
x13
x14
x15
x17
x18
x19
x20
x21
x22
x23
x24
x25
x26
x27
x28
x29
x30
x31

Asymptotic Real
Component (RC)
0.9823
0.9361
0.9585
0.9856
0.9953
0.9343
0.9745
0.9644
0.9745
0.9799
0.9792
0.9639
0.9797
0.9593
0.9826
0.9979
0.9615
0.9892
0.9497
0.9326
0.9710
0.9706

Asymptotic
RC FWHM
0.0047
0.0044
0.0030
0.0021
0.0017
0.0029
0.0023
0.0039
0.0050
0.0060
0.0053
0.0048
0.0028
0.0037
0.0066
0.0012
0.0059
0.0041
0.0051
0.0052
0.0022
0.0020

313

Asympt. RC
1/Variance
246,819
281,623
605,803
1,236,332
1,886,583
648,302
1,030,666
358,463
218,089
151,450
194,098
236,641
695,436
398,263
125,165
3,786,267
156,628
324,344
209,620
201,635
1,126,493
1,363,056

Table 1. The 22 letters of reality. The ‘letters’ are emergent real parameters (i.e.,
just numbers, the ‘best’ set shown in bold in right column) from an iterative
process involving repeated chiral bi-sedenion multiplication. If noise injection at
non-propagating (“off-shell”) parameter x9 is introduced then have non-zero
components {x0, x1, x2,…x7, x8, x9, x16}. The table lists the off-shell
parameter, its asymptotic rc value, the full-width at half maximum (FWHM) of
the peak (FWHM=2.335), and the inverse of the variance (taken as the best set
of ‘letters’ available at this time).

5 Discussion
From the bi-sedenions we find maximal information propagation entails:
(1) 10 dimensions (or weighting factors) on propagation path (or on lettersequence comprising ‘word’). The path is assigned a phase ‘score’; the word is
assigned a gematria score. The 10 dimensions comprise a chiral subspace of the
32-dim bi-sedenion
(2) 22 parameters/letters are emergent.
(3) Three generations of matter are evident from the structure of the chiral
bisedenion: ( (a,),(,) ), where  = “0” = (0,0,0,0,0,0,0,0), and  and  are real
octonions with  = (,0,0,0,0,0,0,0) and  = (,0,0,0,0,0,0,0). In the imaginary

## PDF page 14

314

Stephen Winters-Hilt

octonion components of , , and , we have three clear generations present of
non-propagating, emergent parameters.
(4) Information propagation is carried via 137 paths with different algebraic
‘braid’ or three-octonion-product algebraic terms, plus part of an added ‘path’
associated with an emergent pure imaginary octonion. 1/137 becomes the
approximate limit on allowed perturbation amplitude, as shown in the Results.
Likewise, 137 also presents a special value in the ancient Babylonian/Jewish
gematria word-scoring encoding & systems.
(5) The added complex term indicated in (4) represents the addition of an added
dimension or weighting factor, to a limited degree, thus the 10 dimensions touted
in (1) sometimes have an 11th dimension. This jibes with the mysterious results
seen in physics that euclideanization (continuation of time parameter into
imaginary) provides meaningful information about the system (typically its
thermodynamic and statistical mechanics properties). Similarly this jibes with the
addition of an 11th node in ancient gematria word scoring systems (the Sefirot
diagram has 10 or 11 nodes, or sefiroth).
5.1 Evolution of man-made written systems arrive at 22 letters
It is worthy of note that the existing gematria word-scoring system, and the 22letter alphabet it works on, would have had hundreds of years to seek optimization
at the hands of scribes painstakingly transcribing messages in difficult media (clay
tablet, papyrus, etc.). Gematria was an ancient system for encoding messages used
by the Babylonians and subsequently adopted by the Hebrew people while under
Babylonian control, and it grew in both cases to have religious/numerological
significance (part of the standard religion for Babylonians for 800 hundred years,
adopted by some Jewish sects up to what is modern day Kabbalah). The gematria
word-scoring scheme can be seen as a recursively stable bi-sedenion optimization
or propagation (via its choice of 10 dim and 22 letters, in a 32-dim bisedenion).
Just as the ancient Greeks were fascinated with the recursive properties of the
golden rectangle, incorporating its ‘magic’ into the choice of the temple
foundations and column spacing, etc., the same can be said for the ancient
Babylonians/Hebrews as regards the transcription of their religious texts. It
appears these texts are ‘gematriafied’, thereby incorporating the ‘magic’ or
maximal bisedenion info encoding/transmission into their word foundations.
5.2 Evolution of biological written systems arrive at 22 letters
Biological information involves two written systems, one with nucleic acid
polymer bases (4 DNA or RNA letters), and one amino acid (AA) polymer based
(22 AA letters). The nucleic acid polymer system is thought to be more ancient,

## PDF page 15

22 letters of reality: chiral bisedenion properties …

315

existing before protein (protein is a ‘long’ AA polymer, while a peptide is a
‘short’ AA polymer). This is known as the RNA World Hypothesis [7]. The
original nucleic acid language was optimized for information storage more than
transmission/functionality, and is still retained for that purpose by biological
systems.
Evidently the nucleic acid words written in 4 letters, over vast stretches of
evolutionary time, began to have groupings for optimal information transmission
(where optimality is selected by evolution). In time, these groupings actually
provided a template and mechanism for creating ‘words’ in a new, amino acid
based, alphabet system. These new types of biological words were tasked with
exploring the entire space of functional possibilities (of biomolecules), thus lent
themselves to the typical 22-letter, 10/11 weight-factor (dimension), optimization
result. In ancient gematria the 22 letters are separated into three groups (with
different ‘weight’ factors accordingly): the 3 mother letters (aleph, mem, shin);
the 7 double letters (beth, gimel, daleth,kaph,pe,resh,tau); and the 12 simple
letters (he, vau, zain, cheth, teth, yod, lamed, nun, samekh, ayin, tzaddi, qoph). If
we want to look for a similar splitting into subgroups on properties of the amino
acids we don’t have to look far, as the 22 amino acid ‘letters’ are similarly split
into groups of 3, 7, 12: there are 3 punctuation types of letter (2 stop types, one
start); 7 hydrophobic AAs (alanine, isoleucine, leucine, phenylalanine, proline,
tryptophan, valine), excluding methionine, which codes for ‘start’; and 12
hydrophilic AAs (arginine, asparagine, aspartate, cysteine, glutamate, glutamine,
glycine, histidine, lysine, serine, threonine, tyrosine). Other parallels exist as well,
and not surprisingly so, if they are both an optimized information
transmission/functionality processes that must relate to bi-sedenion propagation
(or weighting) in a 10 element scheme, with emergent ‘letters’ in that scheme
numbering 22.
Since this 22 letter AA alphabet is highly suggestive of a successful bi-sedenion
encoding optimization, this begs the question of what might biochemically
correspond to the 10 (or 11) elements in the gematria-like optimized encoding
scheme? This would indicate a ‘scoring’ on protein words as with text words.
Such scorings on hydrophobicity, etc., have already been employed by biologists,
but it might be possible that an optimal ‘gematria’ scoring system is already builtin, waiting to be discovered. So what might make up the elements in weighting
the different amino acids? We have the standard hydrophilic vs hydrophobic;
polar vs nonpolar; small vs large; monosteric vs allosteric (as a split that
sometimes occurs, especially with complexities of hydrogen bonding); and AA’s
mostly reserved for punctuation (1 start or 2 stops). Counting the polarization pairs of

## PDF page 16

316

Stephen Winters-Hilt

‘this vs that’ as two elements impacting weighting, then the number of elements
impacting the weighting assigned to a ‘letter’ (AA in this instance) is 10 or 11
according to whether allostericity is present. So an exact match with what would
be expected of an optimized bi-sedenion formulation. It is interesting to note that
the richness of the 10/11 parameter polymer scoring/functionalization-capabilities
in aqueous solution may not be possible in non-aqueous solutions. Life may
require water-based biochemical processes to effectively code for functionality in
the geologic time-scales in which it can exist (before catastrophic environmental
change).
5.3 Propagation of physical information arrive at ‘words’ consisting of 22
letters
The breakdown on the emergent 22 parameters in the case of the 19 parameters of
the standard model plus the minimal neutrino extension [8, 9] (have three new
mass parameters for three sterile neutrinos) can similarly be done. The minimal
extended standard model has 3 generations of four mass parameters, so 12 masses
to correspond with the 12. Likewise, there are 7 ‘angle’ or ‘coupling’ parameters,
and 3 other parameters having to do with Higgs or phase.
5.4 Note on optimal information transmission
The bi-sedenion optimization results for maximal information transmission [1],
may also serve another purpose in identifying a new data compression/encoding
scheme. If a 22 symbol alphabet is a fundamental, together with 10 parameter
weighting scheme, it may be that most of the benefits of that optimal encoding
can be obtained by simply remapping to a 22-symbol encoding scheme followed
by one of the usual non-lossy compression methods.
5.5 Oddities of the non-integer part of 1/alpha
In the Results a derivation is given of 137 ‘complete’ braid transmission channels
for propagating information, and of a partial 138 braid channel (that is pure
imaginary). If we take the experimental result from QED, we know the magnitude
of the contribution from the 138th channel to be 0.0359907. The appearance of a
complex value in association with ‘time’ appears in thermodynamics and
statistical mechanics, and is an underlying construct in thermal quantum field
theory. So the appearance of a small complex contribution is no minor thing as it
may provide the explanation for why the variety of euclideanization methods
work, and may provide a better understanding of time (especially in quantum
systems).

## PDF page 17

22 letters of reality: chiral bisedenion properties …

317

6 Conclusion
Maximal information propagation appears to entail communication with 22
‘letters’ operating with a weighting scheme dependent on a 10 (sometimes 11)
dimensional propagation or node-linkage weighting scheme. A ‘quirk’ of all of
these maximal information propagation systems is that an important coupling
term, alpha, or word score, is nearly exactly the integer 137. In the theoretical
analysis of the chiral propagation we see not only ‘why 137’, we also see why
there’s a little extra (since alpha=137.035999070), and arrive at a theoretical
derivation for alpha It is found that the fractional part of 137 relates to
propagation that extends outside the 10 dim bisedenion subspace to a 11th
dimensional subspace (within the 32dim bi-sedenions). In other areas of
communication it is, therefore, not surprising that the highly optimized
languages/systems described involve 22 letters.

References
[1] S. Winters-Hilt, Feynman-Cayley Path Integrals select Chiral Bi-Sedenions
with 10-dimensional space-time propagation, Advanced Studies in
Theoretical Physics, 9 (2015), no. 14, 667 – 683.
https://doi.org/10.12988/astp.2015.5881
[2] S. Winters-Hilt, Unified propagator theory and a non-experimental derivation
for the fine-structure constant, Advanced Studies in Theoretical Physics, 12
(2018), no. 5, 243 – 255. https://doi.org/10.12988/astp.2018.8626
[3] https://en.wikipedia.org/wiki/Gematria. 8/17/2018
[4] J.H. Conway and D.A. Smith, On Quaternions and Octonions: Their
Geometry, Arithmetic, and Symmetry, A. K. Peters, Wellesley,
Massachusetts, 2005.
[5] G. Gabrielse, D. Hanneke, T. Kinoshita, M. Nio, B. Odom, Erratum: New
determination of the fine structure constant from the electron g value and
QED, Physical Review Letters, 99 (2007), no. 3, 039902.
https://doi.org/10.1103/physrevlett.99.039902
[6] G. Gabrielse, D. Hanneke, T. Kinoshita, M. Nio, B. Odom, New
determination of the fine structure constant from the electron g value and
QED, Physical Review Letters, 97 (2006), no. 3, 030802.
https://doi.org/10.1103/physrevlett.97.030802

## PDF page 18

318

Stephen Winters-Hilt

[7] S. Winters-Hilt, Machine-Learning Based Sequence Analysis, Bioinformatics
& Nanopore Transduction Detection, Lulu.com, 2011.
[8] T. Asaka, M. Shaposhnikov, The νMSM, Dark Matter and Baryon
Asymmetry of the Universe, Physics Letters B, 620 (2005), 17–26.
https://doi.org/10.1016/j.physletb.2005.06.020
[9] G. Karagiorgi; A. Aguilar-Arevalo, J. M. Conrad, M. H. Shaevitz, K.
Whisnant, M. Sorel, V. Barger, Leptonic CP violation studies at MiniBooNE
in the (3+2) sterile neutrino oscillation hypothesis, Physical Review D, 75
(2007), 013011. https://doi.org/10.1103/physrevd.75.013011
[10] J. Gilson. https://www.researchgate.net/publication/2187170

Received: August 18, 2018; Published: October 8, 2018
