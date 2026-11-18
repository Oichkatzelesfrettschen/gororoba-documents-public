Source: https://doi.org/10.1088/1742-6596/2667/1/012061
PDF sha256: f58d1ceef19b3a9680028b5475b2fc0ba30de39906b0a582ddaacb359b01e071
License: http://creativecommons.org/licenses/by/3.0/
Language: eng
Fidelity: machine-gated

# Transcription of a-sedenion-algebraic-representation-of-three-colored-fermion-generations--f58d1ceef1.pdf

Transcription of `a-sedenion-algebraic-representation-of-three-colored-fermion-generations--f58d1ceef1.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

A sedenion algebraic representation of three colored
fermion generations
Niels Gresnigt
Department of Physics, School of Mathematics and Physics, Xi’an Jiaotong-Liverpool
University, Suzhou, China
E-mail: niels.gresnigt@xjtlu.edu.cn
Abstract. Three generations of fermions with SU (3)C symmetry are represented
algebraically in terms of the algebra of sedenions, S, generated from the octonions, O, via the
Cayley-Dickson process. Despite significant recent progress in generating the Standard Model
gauge groups and particle multiplets from the four normed division algebras, an algebraic
motivation for the existence of exactly three generations has been difficult to substantiate. In
the sedenion model, one generation of leptons and quarks with SU (3)C symmetry is represented
in terms of two minimal left ideals of Cℓ(6), generated from a subset of all left actions of the
complex sedenions on themselves. Subsequently, the finite group S3 , which are automorphisms
of S but not of O, is used to generate two additional generations. The present paper highlight
the key aspects and ideas underlying this construction.

1. Introduction
In an attempt to establish the geometric and algebraic roots of the Standard Model (SM),
several proposals have been put forth over the years which take as its essential mathematical
ingredients (tensor products of) the only four normed division algebras over the reals: R, C, H,
and O. These proposals seek to unify the gauge groups together with the leptons and quarks
that they act on into a single unified algebraic framework, in terms of an algebra acting on
itself.
The octonions O, the largest of the division algebras, were first considered in the 70s for
their intriguing efficacy in describing quark color symmetry [1]. More recent constructions have
sought to extend these earlier results by describing additional SM structure in terms of tensor
products of division algebras [2, 3, 4, 5, 6, 7]. Many others have contributed to these, and
related, algebraic approaches including those based on topology [8, 9, 10, 11, 12], exceptional
Lie groups [13, 14, 15, 16, 17, 18], Clifford algebras [19, 20, 21, 22, 23, 24, 25, 26, 27], and Jordan
algebras [28, 29, 30, 31, 32, 33].
Existing division algebraic models offer an elegant algebraic construction of the internal space
of a single generation of leptons and quarks. Despite several attempts however [4, 34, 35], a
clear algebraic origin for the existence of three generation is yet to be found. In [34] three
generations of color states are identified directly from the algebra Cℓ(6) generated from the left
adjoint actions of C ⊗ O onto itself. In [3], the algebra T6 = C ⊗ H2 ⊗ O3 , is used to represent
three generations instead. In [36], dimensional reduction is used to isolate three H subalgebras
within O in order to describe three generations of leptons.
Starting with R, each of the remaining three division algebras can be generated via the
Cayley-Dickson (CD) process. This process continues beyond O to produce a series of 2n dimensional algebras. One might therefore ask if the next algebra in the series, the sedenions
S, allows for an elegant algebraic description of three generations of leptons and quarks.

Content from this work may be used under the terms of the Creative Commons Attribution 3.0 licence. Any further distribution
of this work must maintain attribution to the author(s) and the title of the work, journal citation and DOI.
Published under licence by IOP Publishing Ltd
1

## PDF page 2

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

In a recent paper [37] (which builds on earlier work [35, 38]), we argued that S exhibits the
algebraic structure necessary to describe (at least part of) the internal space of three generations.
A single generations of leptons and quarks is represented in terms of two minimal left ideals
of the Cℓ(6), generated from the left adjoint actions of three intersecting C ⊗ O subalgebras of
C ⊗ S onto C ⊗ S. Subsequently, the S3 automorphisms of S (which are not automorphisms
of O) are used to generate two additional generations. The three generations transform under
a single copy of the gauge group SU (3)C , thereby avoiding introducing three generations of
gluons.
2. Normed division algebras
A well-known result by Hurwitz [39] states that there exist only four normed division algebras
(over the reals): R, C, H, O, of dimensions one, two, four and eight respectively.
The octonions O are the largest division algebra. An orthonormal basis is comprised of
seven imaginary units: i1 , ...i7 , along with the unit 1 = i0 . A general octonion x may then
be written as x = x0 i0 + x1 ii + ... + x7 i7 , x0 , ..., x7 ∈ R, with the octonion conjugate x
defined as x = x0 i0 − x1 i1 − ... − x7 i7 . The norm of an octonion |x| is subsequently defined by
|x|2 = xx = xx, and the inverse x−1 = x/|x|2 .
The multiplication of octonions1 is captured in terms of the Fano plane, see Fig. 1. Each
projective line in the Fano plane corresponds (together with the identity i0 ) to a H subalgebra;
there are seven such subalgebras.

Figure 1. The Fano plane, encoding the multiplicative structure of our octonions, where
a ≡ ia , a = 1, ..., 7. Note that each line is cyclic, representing a quaternionic triple.
The automorphism group of O is G2 , which contains SU (3) as one of its maximal subgroups,
corresponding to the stabilizer subgroup of one of the octonion imaginary units, or equivalently,
the subgroup of Aut(O) that preserves the representation of O as the complex space C ⊕ C3 .
This splitting is associated with the quark-lepton symmetry [36].
3. The Cayley-Dickson algebra of sedenions
The CD process is an iterative construction that generates at each stage an algebra (with
involution) of dimension twice that of the previous. A generic element of the CD algebra An ,
can be written as a + bu, where a, b ∈ An−1 , and u is the new imaginary unit introduced by
the CD process applied to An−1 . The fifth CD algebra A4 (A0 = R), generated from O, is the
16-dimensional algebra of sedenions S. This algebra is non-commutative, non-associative, and
not even alternative (x(xy) ̸= (xx)y and y(xx) ̸= (yx)x in general).
An orthonormal basis for S comprises 15 mutually anticommuting imaginary units e1 , ..., e15
together with the unit 1 = e0 . The imaginary units e1 , .., e7 correspond to the original octonion
units i1 , ..., i7 . A general sedenion may then be written as
w = w0 e0 + w1 e1 + ... + w15 e15 ,
1

w0 , ..., w15 ∈ R.

There are different multiplication rules for O used by different authors in the literature. Here we follow the
multiplication table used in [40]

2

## PDF page 3

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

with the sedenion conjugate w defined as w = w0 e0 − w1 e1 − ... − w15 e15 , and the sedenion
norm |w| defined by |w|2 = ww = ww. Whenever |w|2 ̸= 0, the inverse of w is given by
w−1 = w/|w|2 . The product of two sedenions w, v can be determined using the multiplication
table of the orthonormal basis units given in [40, 41], together with linearity.
3.1. Octonion subalgebras inside the sedenions
S contains seven O subalgebras in addition to the original O algebra from which S was generated
[41]. In particular, three O subalgebras can be isolated by applying the CD process to the three
H subalgebras of O that contain i4
Oi : {e0 , ei , e4 , ei+4 , e8 , ei+8 , e12 , ei+12 },

i = 1, 2, 3.

(1)

The intersection O1 ∩ O2 ∩ O3 = H is generated by {e0 , e4 , e8 , e12 }.
3.2. Automorphisms of sedenions
The automorphism group of S is known to be Aut(S) = Aut(O) × S3 = G2 × S3 [42, 43].
Explicitly, the automorphisms of S are given by
θ′ : a + be8 → aθ + (bθ)e8 ,
ϵ : a + be8 → a − be8 ,
√
√
1
1
ψ : a + be8 →
[a + 3a + 3(b − b)] + [b + 3b − 3(a − a)]e8
4
4
where a, b ∈ O, θ ∈ Aut(O), and ϵ and ψ satisfy ϵ2 = ψ 3 = 1, ϵψ = ψ 2 ϵ, generating S3 .
The explicit action of ψ on the sedenion basis elements can be written as:
√
√
3
3
1
1
ψ(ei ) = − ei −
ei+8 , ψ(ei+8 ) = − ei+8 +
ei , ψ(e8 ) = e8 ,
2
2
2
2

(2)
(3)
(4)

(5)

where i = 1, ..., 7. The automorphism ψ corresponds to a simultaneous rotations in the seven
ei − ei+8 planes by 2π/3, and therefore does not correspond to an automorphism of C ⊗ O.
From the action of θ′ on the sedenion units above it is immediately clear that e8 is stabilized
by the G2 automorphisms. Furthermore, these G2 automorphisms map ei , i < 8 to ej , j < 8,
and ei+8 to ej+8 . They therefore do not mix the new sedenion elements ei+8 with the original
octonion elements ei , i = 1, ..., 7. Only the S3 automorphism ψ of order three mixes the original
octonion units with the new sedenion units.
Given that the stabilizer of e4 in G2 is SU (3), and e8 is likewise an SU (3) singlet (as it is
fixed by G2 ), it follows that the SU (3) subgroup of G2 fixes the entire quaternion generated
by {e0 , e4 , e8 , e4 e8 = e12 }, corresponding to O1 ∩ O2 ∩ O3 . The S3 automorphisms on the other
hand do not fix this quaternion, although they do stabilize it.
3.3. The left multiplication algebra of C ⊗ S
Despite the algebras O and S being non-associative, one can consider the left adjoint actions of
these algebras on themselves as linear operators, thereby generating an associative algebra. Due
to the non-associativity of O, this left adjoint algebra of C ⊗ O contains genuinely new maps.
The 64 distinct left-acting complex-linear maps provide a faithful representation of Cℓ(6).
The generalization to C ⊗ S is not immediately obvious since compositions of sedenion
left actions, unlike compositions of octonions left actions, do not in general anti-commute.
Closer inspection reveals that all the left adjoint actions of the original octonion elements
e0 = i0 , ..., e7 = i7 together with e8 onto a general element of S do anticommute, and generate
Cℓ(8) (as do the composed left actions of {e8 , ..., e15 }). A generating basis for Cℓ(8) is therefore
given by the left adjoint actions of {e1 , ..., e8 }. Another possible generating basis is {e8 , ..., e15 }.

3

## PDF page 4

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

4. One generations of color states from C ⊗ S
In [5] it is shown that one generation of leptons and quarks with SU (3)C symmetry can be
elegantly represented in terms of two eight dimensional minimal left ideals of Cℓ(6) generated
from the left adjoint actions of C ⊗ O on itself. The construction of the minimal ideals depends
on a choice of Witt basis of C ⊗ O (or equivalently Cℓ(6)). This Witt basis constitutes three
pairs of fermionic ladder operators, each one defined in terms of one of the three H subalgebras
of O that contain i4 . The dimensions of the minimal ideals then dictates the number of distinct
physical states, whereas the gauge symmetries are those unitary symmetries that preserve the
ideals (or equivalently, the Witt basis).
We generalize this construction of a single generation from C ⊗ O to C ⊗ S. For each
C ⊗ Oi ⊂ S, i = 1, 2, 3 we construct a pair of fermionic ladder operators. The three pairs of
ladder operators via their left adjoint action onto C⊗S then generate a Cℓ(6) subalgebra of Cℓ(8).
Two minimal left ideals of this Cℓ(6) can subsequently be used to represent one generation of
leptons and quarks with SU (3)C symmetry, in what corresponds to a direct generalization of the
construction in [5]. The novelty of this approach is that subsequently (see the next section) the
order three S3 automorphism of S can be used to generate exactly two additional generations.
For each of the three octonion subalgebras O1 , O2 , O3 of S above, define a pair of ladder
operators:
1
(e + iej+4 + ej+8 + iej+12 ),
A†j = 2√
2 j

Aj

1
= √ (−ej + iej+4 − ej+8 + iej+12 ),
2 2

(6)

where j = 1, 2, 3. It is readily checked that Aj (Aj w) = A†j (A†j w) = 0 and Aj (Ak w) =
−Ak (Aj w), ∀w ∈ C ⊗ S, and therefore these ladder operators satisfy (as left actions on a
general w ∈ C ⊗ S) the usual anticommutation relations:
{Aj , Ak }w = {A†j , A†k }w = 0,

{Aj , A†k }w = δjk w,

∀w ∈ C ⊗ S.

(7)

Subsequently we can proceed to construct two minimal left ideals (see [5] for details)
S1u =νe ω1 ω1† +

S1d =ν e ω1† ω1 +

dr A†1 ω1 ω1† +dg A†2 ω1 ω1† + db A†3 ω1 ω1† +

dr A1 ω1† ω1 +dg A2 ω1† ω1 + db A3 ω1† ω1 +

ur A†3 A†2 ω1 ω1† +ug A†1 A†3 ω1 ω1† + ub A†2 A†1 ω1 ω1† +

ur A3 A2 ω1† ω1 +ug A1 A3 ω1† ω1 + ub A2 A1 ω1† ω1 +

e+ A†3 A†2 A†1 ω1 ω1† ,

e− A3 A2 A1 ω1† ω1 ,

where ω1 := A1 A2 A3 is nilpotent, but ω1 ω1† and ω1† ω1 are primitive idempotents.
These ideals are stable under the action of an SU (3)C symmetry, with the basis states of the
ideals transforming as a single generation of leptons and quarks, thereby justifying the labeling
of coefficients in the ideals. Explicitly, the SU (3)C generators are given by
Λ1 = −A†2 A1 − A†1 A2

Λ2 = iA†2 A1 − iA†1 A2

Λ3 = A†2 A2 − A†1 A

Λ4 = −A†1 A3 − A†3 A1

Λ5 = −iA†1 A3 + iA†3 A1

Λ6 = −A†3 A2 − A†2 A3
1
Λ8 = − √ (A†1 A1 + A†2 A2 − 2A†3 A3 ).
3

Λ7 = iA†3 A2 − iA†2 A3

5. Two additional generations from an S3 automorphism
We now proceed to apply ψ to the ladder operators eqn. (6), and subsequently the basis states
of the minimal left ideals, in order to generate two additional generations. It is readily checked
that the S3 automorphisms of S carry over the automorphisms of the left multiplication algebra
Cℓ(8), and so since the action of ψ on e1 , ..., e15 as elements of Cℓ(8) is known, we can via

4

## PDF page 5

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

linearity establish the action of ψ on the ladder operators. This gives two additional sets of
ladder operators:
1
(8)
Bj† = ψ(A†j ) = √ (aej + iaej+4 + bej+8 + ibej+12 )
2 2
1
Bj = ψ(Aj ) = √ (−aej + iaej+4 − bej+8 + ibej+12 )
(9)
2 2
1
Cj† = ψ 2 (A†j ) = √ (bej + ibej+4 + aej+8 + iaej+12 )
(10)
2 2
1
Cj = ψ 2 (Aj ) = √ (−bej + ibej+4 − aej+8 + iaej+12 )
(11)
2 2
√
√
where i = 1, 2, 3, and a = ( 3 − 1)/2, b = (− 3 − 1)/2.
The two additional sets of ladder operators generated in this manner likewise constitute Witt
bases for Cℓ(6), satisfying the same anticommutation relations as {A†i , Ai }, and we proceed to
construct an additional pair of minimal left ideals of Cℓ(6) for each of the two additional sets
of ladder operators {Bi Bi† } and {Ci , Ci† }. We interpret these additional ideals as representing
the second and third generation of color states:
S2u =νµ ω2 ω2† +

S2d =ν µ ω2† ω2 +

cr B1† ω2 ω2† +cg B2† ω2 ω2† + cb B3† ω2 ω2† +

cr B1 ω2† ω2 +cg B2 ω2† ω2 + cb B3 ω2† ω2 +

sr B3† B2† ω2 ω2† +sg B1† B3† ω2 ω2† + sb B2† B1† ω2 ω2† +

sr B3 B2 ω2† ω2 +sg B1 B3 ω2† ω2 + sb B2 B1 ω2† ω2 +

µ+ B3† B2† B1† ω2 ω2† ,

µ− B3 B2 B1 ω2† ω2 ,

S3u =ντ ω3 ω3† +

S3d =ν τ ω3† ω3 +

br C1† ω3 ω3† +bg C2† ω3 ω3† + bb C3† ω3 ω3† +

br C1 ω3† ω3 +bg C2 ω3† ω3 + bb C3 ω3† ω3 +

tr C3† C2† ω3 ω3† +tg C1† C3† ω3 ω3† + tb C2† C1† ω3 ω3† +

tr C3 C2 ω3† ω3 +tg C1 C3 ω3† ω3 + tb C2 C1 ω3† ω3 +

τ + C3† C2† C1† ω3 ω3† ,

τ − C3 C2 C1 ω3† ω3 ,

where ω2 := B1 B2 B3 and ω3 := C1 C2 C3 . The automorphism ψ permutes between these
three generations.
5.1. SU (3)C color symmetry of three generations
The ladder operators belonging to different generations do not satisfy the standard fermionic
anticommutation relations. For example:
{Ai , Bj }w ̸= 0,

{Bi , Cj }w ̸= 0,

{Ci , Aj }w ̸= 0,

∀w ∈ C ⊗ S

(12)

whenever i ̸= j, and likewise for the remaining anticommutation relations. This is a result of
the fact that the three sets of ladder operators are not linearly independent since
ψ 2 (A†i ) + ψ(A†i ) + A†i = 0.

(13)

It is nonetheless readily checked that
{Ai , Bj + Cj }w = 0,

{A†i , (Bj† + Cj† )}w = 0,

{Ai , (Bj† + Cj† )}w = −δij ,

∀w ∈ C ⊗ S. (14)

Despite the inter-generation anticommutation relations in general being complicated
expressions, it turns out that all three generations of states transform correctly under a single

5

## PDF page 6

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061

copy of SU (3). This is because the SU (3)C generators defined in Section 4 are invariant under
the action of S3 automorphisms, as expected since Aut(S) = G2 × S3 . For example:
]
]
]
[
[
[
Λ1 , B1 ω2† ω2 = B2 ω2† ω2 ,
Λ1 , C1 ω3† ω3 = C2 ω3† ω3 .
(15)
Λ1 , A1 ω1† ω1 = A2 ω1† ω1 ,
A single SU (3) generator thus correctly transforms the equivalent states of each generation
Λ1 : dr → dg ,

cr → cg ,

tr → tg .

Despite having three generations of fermions, the sedenion model predicts only one generation
of gauge bosons.
5.2. Linear dependence of minimal ideal states
The three pairs of minimal ideals used to represent three generations of fermions are not expected
to be linearly independent, given the condition eqn. (13) above. Importantly however, the fact
that only two of the three sets of ladder operators are linearly independent does not imply that
only two pairs of minimal ideals are linearly independent.
We speculate that the linear dependence across the minimal ideals might provide an
algebraic basis for incorporating quark mixing and/or neutrino oscillations, although a detailed
investigation into the feasibility of this proposal is yet to be carried out. Nonetheless, some
initial calculations (carried out using Mathematica) indicate that the (anti) down-type quarks
across generations are linearly dependent. That is:
Ai ω1† ω1 + Bi ω2† ω2 + Ci ω3† ω3 = 0,

A†i ω1 ω1† + Bi† ω2 ω2† + Ci† ω3 ω3† = 0,

(16)

where i = 1, 2, 3. On the other hand, all 18 of the (anti) up-type quarks turn out to be linearly
independent. This might be related to the fact that the Yukawa couplings, and subsequent
mass matrix for either the up-type or down-type quarks can be taken to be diagonal, but not
both. Subsequently, one can say without loss of generality that only the down-type quarks mix
via the CKM matrix.
6. Discussion
We have reviewed a recent algebraic representation of three generations of leptons and quarks in
terms of the Cayley-Dickson algebra of sedenions [37]. The internal symmetry of the fermions
has so far been restricted to SU (3)C , arising as a subgroup of the automorphism group of S
that fixes a quaternionic structure.
This algebraic construction uses three O subalgebras of S, with a common intersection
isomorphic to H, in order to construct a Witt basis for Cℓ(6). Subsequently, two of the minimal
left ideals of Cℓ(6) are used to represent a single generation of fermions, in what is a direct
generalization of the construction found in [5]. Finally, the S3 automorphism of order three,
which is an automorphism of S but not of O, is then applied to the Cℓ(6) Witt basis in order
to obtain exactly two additional generations of color states.
In [4, 5], Cℓ(6) arises as the left adjoint algebra of C ⊗ O. Instead, in our approach Cℓ(6)
does not arise from the adjoint actions of a single octonion algebra, but rather from the adjoint
actions of three intersecting octonion subalgebras (of S) onto S.
The model reviewed here is clearly far from complete as we have not considered the remaining
internal symmetries nor the spacetime symmetries. Including additional internal symmetries
into the sedenion model is currently work in progress. It is likewise currently being investigated
if the inevitable linear dependence of some of the minimal ideal states across generations can
provide an algebraic basis for the CKM or PMNS matrix.
Acknowledgements
The authors wish to thank Alessio Marrani insightful discussions and detailed feedback on
earlier drafts of this work.

6

## PDF page 7

XII International Symposium on Quantum Theory and Symmetries (QTS12)
IOP Publishing
Journal of Physics: Conference Series
2667 (2023) 012061 doi:10.1088/1742-6596/2667/1/012061
References
[1] Günaydin M and Gürsey F 1973 Journal of Mathematical Physics 14 1651–1667
[2] Dixon G 1990 Il Nuovo Cimento B (1971-1996) 105 349–364
[3] Dixon G 2004 Journal of mathematical physics 45 3878–3882
[4] Dixon G M 2013 Division Algebras:: Octonions Quaternions Complex Numbers and the Algebraic Design of
Physics vol 290 (Springer Science & Business Media)
[5] Furey C 2016 arXiv preprint arXiv:1611.09182
[6] Furey C 2018 The European Physical Journal C 78 1–12
[7] Gresnigt N G 2020 The European Physical Journal C 80 1–7
[8] Gresnigt N G 2018 Physics Letters B 783 212–221
[9] Gresnigt N G 2019 Braided fermions from Hurwitz algebras Journal of Physics: Conference Series vol 1194
(IOP Publishing) p 012040
[10] Gresnigt N G 2020 Physics Letters B 808 135687
[11] Gresnigt N G 2021 The European Physical Journal C 81 1–7
[12] Gresnigt N, Marcianò A and Zappala E 2021 Physical Review D 104 086021
[13] Manogue C A and Dray T 2010 Octonions, E6 , and particle physics Journal of Physics: Conference Series
vol 254 (IOP Publishing) p 012005
[14] Wilson R A, Dray T and Manogue C A 2022 arXiv preprint arXiv:2204.04996
[15] Manogue C A, Dray T and Wilson R A 2022 Journal of Mathematical Physics 63 081703
[16] Wilson R A 2022 arXiv preprint arXiv:2210.06029
[17] Raj S and Singh T P 2022 arXiv preprint arXiv:2208.09811
[18] Kaushik P, Vaibhav V and Singh T P 2022 arXiv preprint arXiv:2206.06911
[19] Trayling G 1999 arXiv preprint hep-th/9912231
[20] Trayling G and Baylis W E 2001 Journal of Physics A: Mathematical and General 34 3309
[21] Trayling G and Baylis W E 2004 The Cℓ(7) approach to the standard model Clifford Algebras (Springer)
pp 547–558
[22] Stoica O C 2017 Adv. Appl. Clifford Algebras (2018) 28: 52
[23] Stoica O C 2020 arXiv preprint arXiv:2005.08855
[24] Todorov I 2022 https://preprints.ihes.fr/2022/P/P-22-01.pdf
[25] Perelman C C 2019 Advances in Applied Clifford Algebras 29 1–16
[26] Perelman C C 2019 Advances in Applied Clifford Algebras 29 1–20
[27] Pavšič M 2013 arXiv preprint arXiv:1310.6566
[28] Dubois-Violette M 2016 Nuclear Physics B 912 426–449
[29] Dubois-Violette M and Todorov I 2019 Nuclear Physics B 938 751–761
[30] Todorov I and Drenska S 2018 Advances in Applied Clifford Algebras 28 1–36
[31] Todorov I and Dubois-Violette M 2018 International Journal of Modern Physics A 33 1850118
[32] Boyle L and Farnsworth S 2020 New Journal of Physics 22 073023
[33] Boyle L 2020 arXiv preprint arXiv:2006.16265
[34] Furey C 2014 Journal of High Energy Physics 2014 1–11
[35] Gillard A B and Gresnigt N G 2019 The European Physical Journal C 79 1–11
[36] Manogue C A and Dray T 1999 Modern Physics Letters A 14 99–103
[37] Gresnigt N G, Gourlay L and Varma A 2023 The European Physical Journal C 83 1–13
[38] Gresnigt N 2019 Sedenions, the Clifford algebra Cℓ(8), and three fermion generations European Physical
Society Conference on High Energy Physics pp 10–17
[39] Hurwitz A 1898 Nachrichten von der Gesellschaft der Wissenschaften zu Göttingen, MathematischPhysikalische Klasse 1898 309–316
[40] Lohmus J, Paal E and Sorgsepp L 1994 Nonassociative algebras in physics (Hadronic Press)
[41] Cawagas R 2004 Discussiones Mathematicae-General Algebra and Applications 24 251–265
[42] Schafer R D 1954 American Journal of Mathematics 76 435–446
[43] Brown R 1967 Pacific Journal of Mathematics 20 415–422

7
