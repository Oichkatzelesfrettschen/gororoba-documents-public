Source: https://arxiv.org/abs/2303.12219v2
PDF sha256: 8f21aa3a8b638babd1ae3a3ec474ef51cd269b470dce528b23f5cf408b42cac3
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2303.12219.pdf

Transcription of `arxiv_2303.12219.pdf` in this directory, 17 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-17 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT
QUASICRYSTALS

arXiv:2303.12219v2 [math.RA] 17 Apr 2023

DANIELE CORRADETTI, DAVID CHESTER, RAYMOND ASCHHEIM, AND KLEE IRWIN
Abstract. In this paper present a general setting for aperiodic Jordan algebras arising from icosahedral
quasicrystals that are obtainable as model sets of a cut-and-project scheme with a convex acceptance
window. In these hypothesis, we show the existence of an aperiodic Jordan algebra structure whose generators are in one-to-one correspondence with elements of the quasicrystal. Moreover, if the acceptance
window enjoys a non-crystallographic symmetry arising from H2 , H3 or H4 then the resulting Jordan
algebra enjoys the same H2 , H3 or H4 symmetry. Finally, we present as special cases some examples of
Jordan algebras over a Fibonacci-chain quasicrystal, a Penrose tiling, and the Elser-Sloane quasicrystal.

MSC2020: 52C23, 17B65, 17C50

1. introduction and motivation
Crystallographic Coxeter groups are an indispensable tool in classification of simple Lie algebras and
thus play a prominent role in mathematical physics. The Chevalley-Serre theorem [Se, Kac] notoriously
prevents the existence of finite-dimensional Lie algebras arising from non-crystallographic groups such
as H2 , H3 and H4 . Therefore, even though numerous attempts have been made to encounter algebraic
structures (e.g. [PT02, PPT98, Tw99a, DBT12]) and integrable systems (e.g. [Shc, FrKo, Tw99a, Tw00])
based non-crystallographic groups, those are far less used and known in their physical and algebraic applications. Nevertheless, the interest on non-crystallographic groups has incredibily grown since Setchman
in 1982 found a metallic alloy with icosahedral point group symmetry [ShBGC], that was later defined
by Levine and Steinhard [LeSt] as quasicrystal, in the sense of a crystal with quasi-periodic translational
symmetry. Indeed, a very general mathematical set-up for the modelization of such type of quasicrystals
was introduced by Moody and Patera in [MP93], making use of an interesting embedding of the non
crystallographic group H4 into E8 noticed by Elser and Sloane in [ES] and then developed noticed by
Shcherbak in [Shc]. In their work, Moody and Patera showed that a large class of icosahedral quasicrystals
are obtainable as a cut and project scheme on the lattice of icosians or, equivalently, over an E8 -lattice.
Here, we will have their cut-and-project scheme as a starting point, focusing on a special class of quasicrystals arising from an acceptance window that must be a convex set. In this framework, we show in
a constructive way the existence of a Jordan algebra structure whose generator are in one-to-one correspondence with elements of the quasicrystal. These Jordan algebras thus fits into the class of aperiodic
algebras that were first introduced by Patera et al. in [PPT98] and later on studied by Twarock[Tw00] and
Mazochurck [Ma02], even though their analysis was limited to aperiodic Lie algebras and never extended
to Jordan algebras. Moreover, due to the H4 -symmetry of icosians, if the acceptance window enjoys an
H1 ∼
= A1 , H2 , H3
= A1 , H2 , H3 or H4 symmetry, then the resulting Jordan algebra enjoys the same H1 ∼
or H4 symmetry. In fact, this class of Jordan algebras are an algebraic structure naturally endowed with
these non-crystallographic symmetries.
The present work is organized as follows. In section 2 we review basic definitions in order to fix
notations and present crystallographic groups H2 , H3 and H4 . In section 3 we present a reformulation
of the cut-and-project scheme in [MP93, ES] for both an icosian lattice and an E8 -lattice. Section 4 is
entirely devoted to a binary operation, called quasiaddition, first introduced in [BM94] and which will
be crucial in the definition of the aperiodic Jordan algebra. Section 5 deals with aperiodic algebras,
reviewing some known aperiodic algebras from [PPT98, Tw00, Ma02], then we present the definition of
the aperiodic Jordan algebra J (Ξ) defined for every quasicrystal Ξ from convex cut-and-project schemes,
and we investigate basic properties of such class of algebras. Finally, to show that the selected class
of quasicrystals is not only broad, but also highly significant, in section 6 we present some well-known
1

## PDF page 2

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

2

examples of icosahedral quasicrystals, and thus of aperiodic Jordan algebras, that fall in this category:
the Fibonacci-chain quasicrystal, a Penrose tiling, a Z6 -quasicrystal and the
quasicrystal.
√ )
( Elser-Sloane
In the whole paper symbol τ indicates the golden mean, i.e. τ = 12 1 + 5 ≈ 1.618 and while,
to avoid any
the other root of the equation x2 + x + 1 is referred as 1 − τ or −τ −1 , i.e.
√ )
( ambiguity,
1
1 − τ = 2 1 − 5 ≈ −0.618.
.
2. icosians and non-crystallographic root systems
The cut-and-project scheme that we will use in later section is a reformulation of that proposed by
Moody and Patera in [MP93] and that makes use of icosians developing Elser-Sloane construction in
[ES]. The goal of this section is to review all concepts needed to fully express such mathematical set-up.
Icosians are a special set of quaternions that are vertices of a convex regular 4-polytope {3, 3, 5}, i.e. a
600-cell, which forms a group under quaternionic multiplication and, also, a non-crystallographic root
system of type H4 with the Euclidean norm. In fact, it can be easily shown [De21] that the group arising
from icosians is the binary icosahedral group 2I, the order-120 dicyclic group, which is double cover of
the rotational symmetry group of the icosahedron. The H4 -symmetry of the icosian group allows the
Jordan algebras that we will define in sec. 5 to be H4 -symmetric, and it is of paramount importance in
order to model icosahedral quasicrystals.
2.1. Euclidean spaces and root systems. Let En be an Euclidean space, i.e. a vector space
over the real numbers R endowed with a positive defined symmetric
bilinear form ⟨· | ·⟩ called inner
√
product. Then the lenght of a vector v ∈ En is given by ∥v∥ = ⟨v | v⟩, and the angle θ (v, w) of two
vectors v, w ∈ En is defined as
(2.1)

cos θ (v, w) =

⟨v | w⟩
.
∥v∥ ∥w∥

A reflection in the Euclidean space En is a linear transformation rα that fixes all vectors orthogonal to
the vector α, i.e.
(2.2)

rα (v) = v −

2 ⟨v | α⟩
α,
⟨α | α⟩

for every α, v ∈ En . Obviously, the composition of two reflections is still a reflection. Moreover, the
inverse of any reflection is the reflection itself, i.e. rα−1 = rα , and, finally, identity itself is a reflection
once we set α = 0. As a consequence, the reflections of an Euclidean space form a group. Even more,
a straightforward computation shows that ⟨rα (v) | rα (w)⟩ = ⟨v | w⟩ for every v, w ∈ En , so that every
reflection rα is an isometry. A group generated by reflections (2.2) is called a reflection group.
Let En be an Euclidean space. Then a subset Φ of vectors in En is called a root system, if it contains
the opposite of every elements and it is invariant to every reflection generated by its elements, i.e.
(2.3)

± α ∈ Φ and rα (Φ) = Φ,

for every α ∈ Φ. If the subset Φ is a root system, then all vectors α belonging to Φ are called roots and
the dimension n of the embedding space n is called the rank of the system. Finally, for every root system
Φ, we call the root lattice of Φ in En as the Z-span of Φ, i.e.
(2.4)

Λ (Φ) = {β ∈ En : β = nα, α ∈ Φ, n ∈ Z} .

It is important to stress out that, by definition (2.3), root systems and reflection groups are linked one
another, so that any root system give rise to the reflection group that leave its roots invariant and the
converse is also true. Finally, all root systems are notoriously classified in the following families
• four one-parameter families of type An , Bn , Cn , Dn of rank n ≥ 1;
• a one-parameter family of type I2 (m) of rank 2 with m ∈ N. Special cases I2 (3) , I2 (4) , I2 (5)
and I2 (6) are historically labeled as A2 , B2 , H2 and G2 respectively;
• and six exceptional systems of type E6 , E7 , E8 , F4 , H3 and H4 .

## PDF page 3

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

3

A special class of root systems, called crystallographic systems, found a major role in Lie theory. Indeed,
let us consider the quantities generated by ⟨β | α⟩ and ⟨α | α⟩ where α, β are roots of the same system
Φ. If the ratio between the two roots is always an integer, i.e.
⟨β | α⟩
∈ Z,
⟨α | α⟩

(2.5)

for every α, β ∈ Φ, then the root system is called crystallographic, while is called non crystallographic
otherwise. As famously proved by Serre [Se], any crystallographic system allows the definition of a finite
dimensional Lie algebra with Cartan decomposition related to the root system. On the other hand, noncrystallographic root system do not satisfy Serre relations and thus do not give rise to finite dimensional
Lie algebra [Kac].
2.2. non-crystallographic root systems. A concrete example of a type-H4 root system is
△4 ⊂ R4 given by the following 120 vertices of a 600-cell C600 , i.e.
(2.6)

△4 =

{

(±1, 0, 0,(0) , 12 (±1, ±1, )±1, ±1)
1
1
2 0, ±1, ± τ , ±τ

and all permutation
and all even permutation

}

.

A subsystem of △4 ⊂ R4 is given by △3 ⊂ R3 , which is a root system of type H3 , defined by the following
30 vertices of an icosahedron, i.e.
(2.7)

△3 =

{

( (±1, 0,1 0) )
1
2 ±1, ± τ , ±τ

and all permutation
and all even permutation

}

.

Finally, △3 ⊂ R3 contains a type-H2 root system △2 ⊂ R2 given by the 10 vertices of a decagon, i.e.
(2.8)

△2 =

{

(±1, 0)
1
2 (±1, ±τ )

and all permutation

}

,

so that we have the following chain of root systems △2 ⊂ △3 ⊂ △4 that are of type H2 , H3 and H4
respectively.
2.3. non-crystallographic coxeter groups. In order to study reflection groups and root systems in an efficient way, it is a common practice to define Coxeter groups which are abstract presentations
of reflection groups. Let a Coxeter matrix M be a symmetric matrix of finite dimension n with integer
off diagonal entries ≥ 2 and diagonal entries equal to 1, i.e. mij ∈ N, mij = mji , mii = 1 and mij ≥ 2 if
i ̸= j. Then a Coxeter group is an abstract group with presentation
(2.9)

mij

⟨R1 , ..., Rn | (Ri Rj )

= 1⟩ .

As Coxeter himself proved in [Co34], every reflection group is a Coxeter group and, even more, every
finite Coxeter group admits a faithful representation as a finite reflection group of some Euclidean space.
In case of the non-crystallographic root systems of type H2 , H3 and H4 , we have a presentation of the
m
respective Coxeter groups given by ⟨R1 , ..., Rn | (Ri Rj ) ij = 1⟩, with n equal to 2, 3 and 4 respectively,
and with coefficients mij of the Coxeter matrices given by the following




1 3 2 2
(
)
1 3 2
 3 1 3 2 
1 5

(2.10)
(H2 )ij =
, (H3 )ij =  3 1 5  , (H4 )ij = 
 2 3 1 5 .
5 1
2 5 1
2 2 5 1

To give some concrete realisations of such groups, the Coxeter group H2 of order 10 can be realised as
the symmetry group of a decagon, i.e. the reflection group that leaves invariant the roots of the system
△2 ; the group H3 of order 120 can be realised as the full symmetry group of an icosahedron, i.e. the
reflection group that leaves invariant the roots of the system △3 ; finally, the group H4 of order 14400 can
be realised as the symmetry group of a 600-cell, i.e. the reflection group that leaves invariant the roots
of the system △4 .

## PDF page 4

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

4

Isometry of R3


−1 τ1 −τ
1 1
± (0, 1, 0, 0)
±i
(2, 3) (4, 5)
−τ −1 
τ
2
−τ
−1 τ1 

−τ
1 − τ1
1 
1 − τ1
τ 
± (0, 0, 1, 0)
±j
(2, 4) (5, 3)
2
1
−
τ
−1

 τ1
1
− τ −τ
1 
−τ −1 − τ1 
± (0, 0, 0, 1)
±k
(2, 5) (3, 4)
2
1
 1 −1τ −τ 
τ
−1 τ
1
1 

± 21 (−1, 1, 1, 1) ± 21 (1 + i + j + k)
(3, 4, 5)
−
τ
−1
τ
2
1
−τ
−1
−
τ 

τ
−1 − τ1
(
)
(
)
1 
− τ1 −τ −1 
± 12 0, 1, − τ1 , τ
± 12 i − τ1 j + τ k
(1, 3) (4, 5)
2
τ
−1 τ1
Table 1. Correspondence between root of the system △4 of type H4 , element of the
icosian group I , elements of the alternating group A5 and the icosahedral symmetries
in R3 of which the icosian group I is a double cover.
Root of △4

Icosian in H

Permutation in A5

2.4. the icosian ring. In section 2.2 we showed concrete examples of root systems of type of type
H2 , H3 and H4 . Here, we show a notable quaternionic realisation of the root system △4 of type H4 , and
thus of its subsystems △3 and △2 of type H3 and H2 respectively. With this in mind we identify R4 with
quaternions H through the canonical identification ı from R4 to H given by
(2.11)

ı (a, b, c, d) −→ a + bi + cj + dk,

and define the subset of icosians I ⊂ H as the quaternions that are image of ı (△4 ), where elements
of △4 ⊂ R4 are explicitly defined in (2.6). Obviously I is root system of type H4 . Notice that the
quaternionic units 1, i, j, k belong to I ⊂ H since they are image of even permutations of (1, 0, 0, 0) that
belong to △4 .
Moreover, it is easy to see that the 120 elements of I form a group under quaternionic multiplication.
This group is known as the icosian group [CoSl] and is isomorphic to the binary icosahedral group.
The reason behind the name it is due to Hamilton [Ha] and lies in its relationship with the icosahedral
rotational group A5 of order 60 of which I is the double cover. Indeed, the homomorphism from I ⊂ H
to A5 given by

(2.12)

(0, 1, 0, 0)
(0, 0, 1, 0)
(0, 0, 0, 1)
1
2 ((−1, 1, 1, 1))
1
1
2 0, 1, − τ , τ

−→
−→
−→
−→
−→

(2, 3) (4, 5) ,
(2, 4) (5, 3) ,
(2, 5) (3, 4) ,
(3, 4, 5) ,
(1, 3) (4, 5) ,

it is well defined and has kernel {1, −1}. Table 1 shows the correspondence between roots of △4 , elements
of the icosians group I , elements of the alternating group A5 and, elements of the icosahedral group as
isometries in R3 .
From the icosian group, we define the icosian ring I as the Z−span, i.e. all finite sums of the icosian
group I . Obviously, the icosian ring I is a subset of the algebra of quaternions H, and from such algebra
inherits a conjugation and a norm, that we will call quaternionic norm n, given by
(2.13)

n (x) = ⟨x, x⟩ = xx,

for every x ∈ I. It is worth noting that elements of the icosians group I are icosians with unitary norm,
i.e.
(2.14)

I = {x ∈ I : n (x) = 1} ,

## PDF page 5

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

5

so that icosians I of unitary quaternionic norm form a root system of type H4 . In a next section we will
see that this is not the only norm we set over the ring of icosians and that ring of icosians I endowed
with the Euclidean norm nE that we will later define is isomorphic to an E8 -lattice [CoSl].
Now, consider the map ∗ on the Dirichlet ring Z [τ ] that sends τ in 1 − τ , i.e. defined by
∗

(2.15)

(a + τ b) = (a + b) − τ b,

with a, b ∈ Z. Clearly, the map ∗ can be extended to the whole icosian ring I and it will be of paramount
importance in defining icosahedral quasicrystals in the next section.
Finally, an useful way of working with icosians is through their Z8 decomposition, which is the following
(2.16)

x = (a + τ b) + (c + τ d) i + (e + τ f ) j + (g + τ h) k,

where a, b, c, d, e, f, g ∈ Z. Thus, from now on we will use ambivalently what we will call integral coordinates of a generic icosian x ∈ I, i.e. x = (a, b, c, d, e, f, g, h), or the quaternionic notation depending on
the convenience. Moreover, it is straightforward to note that
(2.17)

x∗ = (a + b, −b, c + d, −d, e + f, −f, g + h, −h) ,

which gives us an explicit formula for the star map in integral coordinates.
3. icosahedral quasicrystals as model sets
It is well-known that a general mathematical setup for cut-and-project quasicrystals is given by model
sets that arise from cut-and-project schemes [Mo00]. More specifically, a broad class of icosahedral
quasicrystals, which is the one of our interest, is linked to cut-and-project schemes over an icosian
lattice (e.g. see [MP93, Mo00]). In this section we present the notion of convex cut-and-project scheme,
introducing a scheme inspired by [Mo00, sec. 4.1] and that make use of an icosian lattice. Moreover, we
present an equivalent scheme that make use of an E8 -lattice. Since for the definition of the aperiodic
Jordan algebra the acceptance window of the scheme must be convex, we will restrict ourself to this
condition. It is worth noting that the setting of the cut-and-project scheme through the use of the
“icosian lattice” or its equivalent E8 -lattice is endowed with an H4 symmetry that will be useful for
Theorem 5.7 on the non-crystallographic symmetries of the Jordan algebra.
3.1. model sets and cut-and-project schemes. A cut-and-project scheme is a lattice Λ in
an embedding space Rd1 × G, where Rd1 is a real euclidean space called the physical space and, G is a
locally compact abelian group that, for our purposes, will simply be Rd2 and that is called the inner
space. Along with the previous embedding, a cut-and-project scheme is endowed with two projections π1
and π2 that have image into Rd1 and Rd2 respectively. In brief, a cut-and-project scheme is given by the
following collection of spaces and mappings
(3.1)

Ξ
∩
Rd1

π

1
←−

Λ
∩
Rd1 × Rd2

Ω
∩
π2
−→
Rd2

such that the restriction π1 |Λ is injective in Rd and the image π2 (Λ) is dense in Rd2 . Given a cutand-project scheme and a set Ω called acceptance window, such that the closure of the interior int (Ω) is
compact, then a model set Ξ is defined as the points in physical space that are image of points that once
are projected in the inner space belong to the window Ω, i.e.
}
{
(3.2)
Ξ = π1 (x) ∈ Rd1 : x ∈ Λ, π2 (x) ∈ Ω .
In practice, it is often useful to define the model set Ξ through a star map ∗ that goes directly from Rd1
to Rd2 , i.e.
(
)
(3.3)
x∗ = π2 π1 |−1
Λ (x) ,

so that the model set is then given by points in the physical space that are sent by the star map into the
acceptance window, i.e. Ξ = {x ∈ π1 (Λ) : x∗ ∈ Ω}. In accordance with a common practice, we will call
the model set Ξ a cut-and-project quasicrystal ; moreover, we will add the adjective convex if the window
Ω is a convex subset of Rd2 .

## PDF page 6

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

6

3.2. icosahedral quasicrystals from icosians. Consider the cut-and-project scheme obtained embedding a lattice Ĩ made by two copies of the ring of icosians I, i.e. Ĩ ∼
= I × I, in the embedding
space H × H ∼
= R4 × R4 through the map x ↦→ (x, x∗ ) where ∗ is the star map defined in (2.15). We then
have the following cut-and-project scheme
Ξ
∩
H

(3.4)

Ĩ
∩
π∥
←− H × H

Ω
∩
π⊥
−→
H

where π∥ and π⊥ are the trivial projections and Ω is the acceptance window which, in this case, is a
subset whose closure is compact. The model set Ξ is then given by
Ξ = {x ∈ I : x∗ ∈ P } .

(3.5)

This cut-and-project scheme essentially encompasses the generic situation for icosahedral symmetry in
model sets. In fact, almost all known icosahedral quasicrystals, obtainable from cut-and-project methods,
arise from this mathematical set up [Mo00, sec. 4.1]. Nevertheless, in order to build an aperiodic Jordan
algebra over the model set, we will restrict ourself to the special cases where Ω is a convex set.
3.3. icosahedral quasicrystals from an E8 lattice. The ring of icosians enjoys a deep
relation with the E8 lattice, which can be made explicit with the aid of a different norm over icosians (see
[CoSl, MP93]). Indeed, in a previous section we have seen that icosian ring I inherits, from its natural
embedding in H, a quaternionic norm n.
√ We now notice that the norm of a generic element x ∈ I, i.e.
n (x), is a real number of the form p + q 5 with p, q being rational numbers. Thus, we can define a new
Euclidean norm nE , given by
(3.6)

nE (x) = p + q.

To be more explicit, in integral coordinates the quaternionic norm n (x) of an icosian x = (a0 , b0 , a1 , b1 , a2 , b2 , a3 , b3 )
is
3 (
∑
√ )2
(3.7)
n (x) =
ak + 5bk ∈ Z [τ ] ,
k=1

while the Euclidean norm nE (x) is
(3.8)

nE (x) =

3
∑

k=1

a2k + 5b2k + 2ak bk ∈ Z.

It can be shown that the icosian ring, with the Euclidean norm, is isomorphic to an E8 lattice Λ (E8 )
(see [CoSl, Ch. 8]). As a consequence of this isomorphism, icosahedral quasicrystals, that are obtainable
as model set of a cut-and-project scheme over icosians, can also be modeled through a cut-and-project
scheme over an E8 lattice.
Indeed, following [Pa95] let a1 , a2 , a3 , a4 ∈ R4 be
(3.9)

a1 =
a3 =

(

)

Ξ
∩

Λ (E8 )
∩

1 1
2 (τ , −τ, 0, −1
) ,
1
1
2 0, 1, τ , −τ ,

)

(

1
1
2 ( 0, τ , −τ, 1) ,
1
1
2 0, −1, τ , τ .

a2 =
a4 =

A cut-and-project scheme equivalent to (3.4) is obtained embedding the E8 -lattice Λ (E8 ) in R8 ∼
= R4 ×R4 ,
with the following maps, i.e.
(3.10)

R4

π∥

←−

R4 × R4

π

Ω
∩

⊥
−→
R4

where Ω is the acceptance window and the projections π∥ and π⊥ are defined as follows. Given an element
X ∈ Λ (E8 ), i.e.
(3.11)

X = c1 α1 + ... + c8 α8 ,

## PDF page 7

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

7

with c1 , ..., c8 ∈ Z and α1 , ..., α8 simple roots of E8 , we define
(3.12)

π∥ (X)
=( (c1 + τ c7)) a1 +((c2 + τ c6)) a2 + ((c3 + τ c5 ))a3 + (c
( 8 + τ c4 ) )a4 ,
π⊥ (X) = c1 − τ1 c7 a∗1 + c2 − τ1 c6 a∗2 + c3 − τ1 c5 a∗3 + c8 − τ1 c4 a∗4 ,

where a1 , a2 , a3 , a4 are the elements defined in (3.9) and a∗1 , a∗2 , a∗3 , a∗4 are their respective images through
the the star map in (2.15). Notice that through the canonical identification between R4 and H in (2.11),
we have that
(3.13)

ι (a1 ) =
ι (a3 ) =

(

)

1 1
2 ( τ − τ i − k ),
1
1
2 i + τ j − τk ,

ι (a2 ) =
ι (a4 ) =

(

)

1 1
2( τ i − τ j + k ),
1
1
2 −i + τ j + τ k ,

are all icosians, therefore the image of the E8 -lattice Λ (E8 ) is the icosian ring I, thus making the model
set Ξ an aperiodic subset of the icosian ring.
4. Quasiaddition
All convex cut-and-project quasicrystals enjoy a simmetry that it can be easily expressed by a binary
operation called quasiaddition [BM94, Pa95, CCAI] as contraction of “quasicrystal addition” and that
can be defined for the icosian ring I, i.e.
x ⊢ y = τ 2 x − τ y,

(4.1)

for every x, y ∈ I. Such binary operation is not commutative, nor associative, and does not have a
unit. Nevertheless is power-associative and flexible [CCAI2]. The major properties of quasiaddition are
summarized in the following
Proposition 4.1. Let x, y ∈ I. Then

(4.2)

x ⊢ (x ⊢ (x ⊢ (. . . ⊢ x))) = x,

(4.3)

x ⊢ (y ⊢ x) = (x ⊢ y) ⊢ x,

(4.4)

x ⊢ (y ⊢ y) = (x ⊢ x) ⊢ y = x ⊢ y,

(4.5)

x ⊢ (x ⊢ y) = y ⊢ x.

Proof. The first property is just the plain result of τ being solution of τ 2 − τ − 1 = 0. Indeed,
x ⊢ x = (1 + τ ) x − τ x = x,

and thus the (4.2) follows. As corollary, quasiaddition is power-associative. Flexibility is expressed
by (4.3) which is a straightforward calculation. Since is flexible and not associative, then obviously
x ⊢ (x ⊢ y) ̸= (x ⊢ x) ⊢ y. But, since x ⊢ (x ⊢ y) = (1 + τ ) y − τ x, then, in a rather interesting way, we
have
(4.6)

x ⊢ (x ⊢ y) = y ⊢ x,

(4.7)

(x ⊢ x) ⊢ y = x ⊢ y,

from which (4.4) and (4.5) follow.

□

An useful technical Lemma, whose straightforward proof we omit but can found in [CCAI2], is the
following
Lemma 4.2. Let x, y ∈ I. Then
(4.8)

k

((((y ⊢ x) ⊢ x) ⊢ x) ⊢ . . .) ⊢ x = (1 + τ ) (y − x) + x,

where k is the number of times the element x is quasiadded to y.

Another interesting property of quasiaddition, which is again the result of a straightforward calculation,
is called the translational invariance [BM94], i.e.
(4.9)

(x + u) ⊢ (y + u) = (x ⊢ y) + u,

for every x, y, u ∈ I. This property is useful when working with model sets resulting from a cut-and-project
scheme. Indeed, if quasiaddition acts over quasicrystals as special kind of inflation of the quasicrystal.

## PDF page 8

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

8

Thus, the translational invariance in (4.9) ensures that the inflation of a translated quasicrystal matches
the translation of the already inflated quasicrystal.
Finally, the most important feature of quasiaddition is expressed by the following
Theorem 4.3. If x, y belong to a convex cut-and-project icosahedral quasicrystal Ξ then also x ⊢ y
belongs to it, i.e. x, y ∈ Ξ implies
(4.10)

x ⊢ y ∈ Ξ.

Proof. Let x, y ∈ Ξ where Ξ is the model set of a cut-and-project scheme as in (3.4) with the acceptance
window Ω that is a convex set, i.e. (1 − t) x − ty ∈ Ω for every x, y ∈ Ω and t ∈ [0, 1]. Then
(x ⊢ y)∗ = (1 − τ )2 x − (1 − τ ) y
= (1 − t) x + ty,
∗

where t = 1 − τ ≈ 0.618... Since Ω is a convex, then (x ⊢ y) ∈ Ω, thus x ⊢ y ∈ Ξ.

□

Now, an useful Lemma is the one that shows how quasiaddition behaves on the integral coordinates
of two icosians as defined in (2.16).
Lemma 4.4. Let x, y ∈ I with x = (a, b, c, d, e, f, g, h) and y = (a′ , b′ , c′ , d′ , e′ , f ′ , g ′ , h′ ). Then

t
(a − a′ ) + (b − b′ ) + a′
 (a − a′ ) + (b − b′ ) + b 


 (c − c′ ) + (d − d′ ) + c′ 


 (c − c′ ) + (d − d′ ) + d 

(4.11)
x⊢y=
 (e − e′ ) + (f − f ′ ) + e′  .


 (e − e′ ) + (f − f ′ ) + f 


 (g − g ′ ) + (h − h′ ) + g ′ 
(g − g ′ ) + (h − h′ ) + h
Proof. The proof is a straightforward once we notice that for an Dirichlet number z = (a, b) = a + τ b ∈
Z [τ ], then τ z = τ a + τ 2 b and τ 2 z = (1 + τ ) (a + τ b) so that multiplication by τ and τ 2 act on integral
coordinates as
τ : (a, b) −→
(b, a + b) ,
τ 2 : (a, b) −→ (a + b, a + 2b) .

(4.12)

In case of x, y ∈ I, as in the hypothesis of the Lemma, we have
(4.13)

τ 2 : x −→ (a + b, a + 2b, c + d, c + 2d, e + f, e + 2f, g + h, g + 2h) ,
τ : y −→
(b′ , a′ + b′ , c′ , c′ + d′ , e′ , e′ + f ′ , g ′ , g ′ + h′ ) ,

from which follows the Lemma.

□

An immediate Corollary of the previous Lemma, which will be useful in the next section is the following
Corollary 4.5. Let x, y ∈ I.Then x ⊢ y = x if and only if y = x.
5. Aperiodic Jordan Algebras from icosahedral quasicrystals
In this section we briefly review some important aperiodic algebras studied by Patera and Twarock
in [PPT98, Tw00, MT03]. Then we show how to define an aperiodic Jordan algebra for convex cut-andproject icosahedral quasicrystals. Even though specific quasicrystals give rise to different features of the
algebra, all Jordan algebras arising from this process enjoy some common properties that we present here.
Finally, to give concreteness to the definition we analyze a three aperiodic Jordan algebra: one defined
over the palindromic Fibonacci-chain quasicrystal; one for the Penrose tiling in (6.6); and, finally, one for
the Elser-Sloane quasicrystal.

## PDF page 9

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

9

5.1. aperiodic algebras. Aperiodic algebras were introduced by Patera, Pelantova and Twarock in
[PPT98] with a specific class of aperiodic algebras named Quasicrystal Lie algebras whose generators are
in one to one correspondence with a one-dimensional quasicrystal which was a modification of a Fibonaccichain quasicrystal. Such quasicrystal Lie algebras were inspired by the usual Witt algebra, but they did
not possess a Virasoro extension, which was an interesting feature that the authors were aiming for.
Later on Twarock defined an aperiodic Witt algebra which indeed had a Virasoro extension [Tw00] and
thus allowing some interesting physical applications in the study of the breaking of Virasoro symmetry
and in the realisation of a class of integrable systems [Tw99a, TW00b]. A similar algebra, related to the
Penrose tiling we reviewed in (6.6), was then studied by Twarock and Mazorchuk in [MT03].
Unfortunately, Twarock and Mazochurck’s work on Penrose Tiling cannot be extended to the quaternions and, thus, to icosahedral quasicrystal arising from a cut-and-project system of the kind in (3.4).
Indeed we have the following
Theorem 5.1. Let I be the ring of icosians and {Lx }x∈I be a basis for the infinite-dimensional algebra
W with bilinear product defined by for every x, y ∈ I
(5.1)

[Lx , Ly ] = f (x − y) Lx+y .

The only f that makes W a Lie algebra is the zero function and in that case W is an abelian Lie algebra.
Proof. To proof the theorem we notice that for W to be a Lie algebra the product must be antisymmetric
and thus f (−x) = −f (x). On the other hand, to be satisfied the Jacobi identity we need
(5.2)

[Lx , [Ly , Lz ]] + [Ly , [Lz , Lx ]] + [Lz , [Lx , Ly ]] = 0,

and since
(5.3)
(5.4)
(5.5)

[Lx , [Ly , Lz ]] = f (z − y) f (y + z − x) Lx+y+z ,

[Ly , [Lz , Lx ]] = f (x − z) f (z + x − y) Lx+y+z ,

[Lz , [Lx , Ly ]] = f (y − x) f (x + y + z) Lx+y+z ,

this means that f (xy) = f (x) · f (y). Unfortunately this cannot happen over the quaternions. Indeed
let i,j be two imaginary unit, since f is real and the reals are abelians, we have f (i) f (j) = f (j) f (i), but
on the other hand ij = −ji we have
(5.6)

f (ij) = f (i) f (j) = f (j) f (i) = f (ji) = −f (ij) ,

and thus f ≡ 0. Then for any quaternion we have f (q) = f (ij (−jiq)) = f (ij) f (−jiq) = 0.

□

Having reviewed why Twarock and Mazochurck approach cannot be extended to icosians or quaternions
in general, we will now switch from Lie algebras to Jordan algebras showing how aperiodic Jordan algebras
arise quite naturally in this context.
5.2. jordan algebras from quasicrystals. The previous theorem prevents the extension of
aperiodic Witt algebras to icosahedral quasicrystals arising from cut-and-project schemes such a (3.4).
On the other hand, the definition of an aperiodic Jordan algebra is possible for every model set arising
from the cut-and-project scheme (3.4) with a convex window Ω. Indeed, let Ξ be the convex cut-andproject quasicrystal arising from a convex window Ω and let J (Ξ) be the real vector space spanned by
{Lx }x∈Ξ equipped with the bilinear product given by
1
(Lx⊢y + Ly⊢x ) ,
2
for every x, y ∈ Ξ. Since, by Theorem 4.3 we have that x ⊢ y ∈ Ξ, then the product is well defined.
Moreover, we have the following
(5.7)

Lx ◦ Ly =

Theorem 5.2. The algebra J (Ξ) is a Jordan algebra.
Proof. The product in (5.7) is bilinear by definition and is clearly commutative, i.e.
(5.8)

Lx ◦ Ly = Ly ◦ Lx .

## PDF page 10

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

10

Therefore, it is sufficient to show that the Jordan identity is valid. Indeed, since (4.2) and the commutativity of the product, we have that
1
(Lx ◦ Ly ) ◦ (Lx⊢x + Lx⊢x )
2
= (Lx ◦ Ly ) ◦ Lx

(Lx ◦ Ly ) ◦ (Lx ◦ Lx ) =

= Lx ◦ (Ly ◦ Lx )

= Lx ◦ (Ly ◦ (Lx ◦ Lx )) ,
thus fulfilling the Jordan identity.

□

It is well-known that Jordan algebras have an abundance of idempotent elements. This algebra is no
exception since (4.2) implies that all elements of the basis used for its definition are idempotents, i.e.
(5.9)

(Lx ◦ Lx ) = Lx ,

for every x ∈ Ξ.
Clearly there are specific features of the Jordan algebra J (Ξ) that depends on the choice of the
quasycrystal Ξ from which is originated. Nevertheless there are few basic properties that are common to
all Jordan algebras arising from (5.7). Indeed, an interesting feature is expressed by the the following
Lemma 5.3. Let x, x′ , y, y ′ ∈ Ξ. If
(5.10)

Lx ◦ Ly =

1
(Lx′ + Ly′ ) ,
2

then x + y = x′ + y ′ .
Proof. Is a straightforward implication from Lemma 4.4, but it can be seen directly since, by definition,
x′ = x ⊢ y and y ′ = y ⊢ x. Thus x′ + y ′ = (1 + τ ) x − τ y + (1 + τ ) y − τ x = x + y.
□
From now on, we will suppose the Jordan algebra J (Ξ) to be infinite dimensional, since the only case
when this does not happen is in the trivial case of the acceptance window Ω being a point, for which the
resulting algebra can hardly be considered “aperiodic” being a one-dimensional algebra.
Beside being infinite dimensional, the algebras J (Ξ) are not unital. This is a consequence of Corollary
4.5 for which x ⊢ y = x if and only if y = x, as shown by the following
Proposition 5.4. The Jordan algebras J (Ξ) are not unital.
Proof. The proof is given
∑ by contraddiction. Let I ∈ J (Ξ) be the identity, i.e. I ◦ X = X for every
X ∈ J (Ξ) , and let I =
ξx Lx , with ξx ∈ R and x ∈ Ξ, be a decomposition of I. Then, let us consider
the product I ◦ L0 = L0 . For the bilinearity we have
∑
(5.11)
I ◦ L0 =
ξx Lx ◦ L0 = L0 ,
x∈Ξ

but, for Corollary 4.5 we have that Lx ◦ L∑
0 = L0 if and only if x = 0, therefore the L0 component ξ0 is
ξx Lx . Repeating the same argument for all x ∈ Ξ we then
equal to 1 and I is of the form I = L0 +
x̸=0

have that all ξx = 1 and I must be of the form
(5.12)

I=

∑

Lx .

x∈Ξ

But, let us consider again the product I ◦ L0 that we now know to be of the form
∑
(5.13)
I ◦ L0 = L0 ◦ L0 +
Lx ◦ L0 = L0 ,
x̸=0

∑

this means that the remaining
Lx ◦ L0 must be equal to 0. Nevertheless, this is impossible since the
terms Lx ◦ L0 give rise only to terms of the form 12 Lx⊢0 and 12 L0⊢x thus with positive coefficients for
every x ∈ Ξ.
□

## PDF page 11

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

11

Remark 5.5. Even though the algebra J (Ξ) is not unital, it can be extended to an unital algebra with a
one-dimensional extension. Indeed, let J (Ξ)ext be the vector space J (Ξ) ⊕ K endowed with the bilinear
product defined by
(5.14)

(Lx + α) ∗ (Ly + β) = Lx ◦ Ly + αv + βu + αβ,

where Lx , Ly ∈ J (Ξ) and α, β ∈ K. It is easy to show that this is a Jordan algebra with 1 ∈ K as unit
element and, that J (Ξ)ext contains a copy of the original algebra J (Ξ). Nevertheless, we will not pursue
the study of such algebra and we hold to the the original aperiodic Jordan algebra J (Ξ) .
An interesting feature of these algebras is the lack of finite dimensional sub-algebras that are not the
one-dimensional ones generated by an element Lx . Indeed, we have the following
Theorem 5.6. The algebras J (Ξ) do not have finite dimensional subalgebras with dimension greater
than 1.
Proof. Let A be a subalgebra in J (Ξ). If dimA = 1 then A is just the algebra generated by Lx with
x ∈ Ξ. If dimA > 1 then it exist x, y ∈ Ξ such that Lx and Ly belong to A. If Lx and Ly are in A, then
also all elements of the form
(5.15)

Lx⊢y , L(x⊢y)⊢y , . . . , L((x⊢y)⊢y)···⊢y , . . .

belong to A. By Lemma 4.2 the series if infinite since
(5.16)

(1 + τ )k1 (x − y) + y = (1 + τ )k2 (x − y) + y

if and only if k1 = k2 , therefore implying that A is infinite dimensional and thus proving the theorem. □
As for the simplicity, or the non-simplicity, of the algebra J (Ξ), at the moment no model set Ξ led
to the construction of of a simple aperiodic Jordan algebra J (Ξ) (see [CCAI, CCAI2]). In fact, this is
no surprise, since simple infinite-dimensional Jordan algebras are all classified by Zel’manov in [Ze]. To
have a simple aperiodic Jordan algebra of the type in (5.7), would mean to have a quasicrystal Ξ arising
from a convex window Ω that would give rise to an algebra J (Ξ) of the Clifford type or of the Hermitian
type, since those are the only allowed types from Zel’manov classification theorem. In both cases that
would be astonishing and if possible that would be the result of a very special ad hoc construction which
would not be relevant for our practical purposes.
As a final note, even though the definition of an aperiodic Jordan Algebra J (Ξ) is always possible for
a convex cut-and-project icosahedral quasicrystal, the Hn -symmetry of the quasicrystal, and thus of the
Jordan algebra, is the result of the joint properties of the lattice and the acceptance window Ω. In fact
we have the following
Theorem 5.7. Let J (Ξ) be an aperiodic Jordan algebra, where the model set Ξ the set-up defined in
(3.4) with a convex window Ω. Then J (Ξ) has an H1 ∼
= A1 , H2 , H3 or H4 if and only if the acceptance
window Ω enjoys an H1 ∼
= A1 , H2 , H3 or H4 respectively.
Proof. Consider a quasicrystal resulting from the set-up defined in (3.4) such that
(5.17)

Ξ = {x ∈ I : x∗ ∈ Ω} .

Now, let ρ be a reflection of the Coxeter group of Hn with n ∈ {1, 2, 3, 4}. Since the icosians I enjoy the
H4 symmetry, then ρ (I) = I. Thus, if we also have that the acceptance window is invariant through this
reflection, i.e. ρ (Ω) = Ω, then also the quasicrystal is invariant, i.e. ρ (Ξ) = Ξ. Then, from the definition
of a reflection in (2.2) follows that
(5.18)

ρ (x ⊢ y) = ρ (x) ⊢ ρ (y) ,

for every x, y ∈ Ξ. The Jordan
{
}algebra J (Ξ) it is thus invariant under ρ since canonically isomorphic to
the algebra spanned by Lρ(x) ρ(x)∈Ξ equipped with the bilinear product given by
(5.19)
for every ρ (x) , ρ (y) ∈ Ξ.

Lρ(x) ◦ Lρ(y) =

)
1(
Lρ(x)⊢ρ(y) + Lρ(y)⊢ρ(x) ,
2

□

## PDF page 12

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

n
Fpal (n)

···
-4
-3
-2
-1
0
1
2
3
· · · −2 − 4τ −2 − 3τ −1 − 2τ −1 − τ 0 1 + τ 1 + 2τ 2 + 3τ
Table 2. Elements of the Fibonacci-chain Quasicrystal Fpal (n).

4
2 + 4τ

12

···
···

6. A few examples
In the previous section we showed some common properties of aperiodic Jordan Algebra J (Ξ). In
this section we want to give a hint of what these algebras are. Thus, making use of cut-and-project
schemes defined in section 3 we define here four aperiodic Jordan algebras related to four well-known
quasicrystal: the palindromic Fibonacci-chain quasicrystal; a Penrose tiling; a Z6 -quasicrystal; the ElserSloane quasicrystal. It is worth noting that the Fibonacci-chain quasicrystal enjoy a reflection symmetry,
i.e. an H1 ∼
= A1 symmetry; the Penrose tiling a fivefold symmetry which is a subgroup of H2 ; the specific
Z6 -quasicrystal enjoys an H3 -symmetry; while the Elser-Slone quasicrystal, and thus the Jordan algebra
defined over it, enjoys an H4 -symmetry.
6.1. Fibonacci-chain quasicrystal. Let us start from the cut-and-project scheme in (3.4) and set the
acceptance window Ω as (0, 1]. Then, since the star map ∗ leaves 1, i, j, k invariant, then the resulting
model set
Ξ = {x ∈ I : x∗ ∈ Ω} ,

(6.1)
is equivalent to
(6.2)

Ξ∼
= F = {x ∈ Z [τ ] : x∗ ∈ (0, 1]} ,

which is the definition of the Fibonacci-chain quasicrystal as model set (e.g. see [PPT98, CCAI]). While
the acceptance window Ω = (0, 1] corresponds to the most known Fibonacci-chain quasicrystal, we are
interested here on its symmetric
]version, i.e. the palindromic Fibonacci-chain quasicrystal Fpal which can
[
be obtained setting Ω = − 21 , 21 . A sample of element of the palindromic Fibonacci-chain
] quasicrystal
[
can be found in Tab. 2. Since both the icosians I and the acceptance window Ω = − 21 , 12 enjoy the 180degree symmetry given by ρ (x) = −x, then also the quasicrystal enjoys such symmetry, i.e. ρ (Ξ) = Ξ,
and more specifically, the palindromic Fibonacci-chain quasicrystal is such that
(6.3)

Fpal (−n) = −Fpal (n) .

The Jordan algebra J (Fpal ), is defined as the real vector space spanned by {Lx }x∈Fpal equipped with
the bilinear product given by
1
(Lx⊢y + Ly⊢x ) .
2
An equivalent definition of the Fibonacci-chain Jordan algebra J (Fpal ) can be obtained on a vector space
indexed by integral numbers, i.e. spanned by {Ln }n∈Z , with bilinear product defined as
(6.4)

Lx ◦ Ly =

1
(Ln′ −m′ +2n−m + Lm′ −n′ +2m−n ) ,
2
where n′ , m′ ∈ Z and n′ = Fpal (n) − τ n and m′ = Fpal (m) − τ m. We will call algebra the integral
formulation of the Jordan algebra J (Fpal ). An analysis of Tab. 3, along with few computations allows to
see that J (Fpal ) is not simple since L0 J (Fpal ) = {L0 ◦ x : x ∈ J (Fpal )} is a proper ideal of the algebra.
Similar results holds for all the examples presented and, as already discussed before, we doubt the
existence of a simple Jordan algebra from this set-up.

(6.5)

Ln ◦ Lm =

6.2. A Penrose tiling. Penrose tilings are aperiodic tilings of the plane, introduced by Roger Penrose
in [Pen], making use of four different prototiles: two different rhombi and two different tiles called kites
and darts. In this context, different cut-and-project schemes were proposed by Baake [BaHu, Ba98] and
recently refined [ShuMa], to give rise to different Penrose tilings. For our purposes it is interesting the

## PDF page 13

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

Ln ◦ Lm

L−2

L−1

L0

L1

L2

L−4
L−3
L−2
L−1
L0
L1
L2
L3
L4

1
(L1 + L−7 )
2
1
(L0 + L−5 )
2

1
(L−8 + L3 )
2
1
(L−6 + L2 )
2
1
(L−3 + L0 )
2

1
(L6 + L−10 )
2
1
(L5 + L−8 )
2
1
(L3 + L−5 )
2
1
(L2 + L−3 )
2

1
(L9 + L−12 )
2
1
(L8 + L−10 )
2
1
(L6 + L−7 )
2
1
(L5 + L−5 )
2
1
(L3 + L−2 )
2

1
(L11 + L−13 )
2
1
(L10 + L−11 )
2
1
(L8 + L−10 )
2
1
(L7 + L−6 )
2
1
(L5 + L−3 )
2
1
(L3 + L0 )
2

L−2
1
(L
−3 + L0 )
2
1
(L
−5 + L3 )
2
1
(L
−7 + L6 )
2
1
(L−8 + L8 )
2
1
(L−10 + L11 )
2
1
(L−11 + L13 )
2

L−1
1
(L
2 + L−3 )
2
1
(L
5 + L−5 )
2
1
(L−6 + L7 )
2
1
(L−8 + L10 )
2
1
(L−9 + L12 )
2

L0
1
(L
−2 + L3 )
2
1
(L−3 + L5 )
2
1
(L−5 + L8 )
2
1
(L−6 + L10 )
2

L1
1
(L0 + L3 )
2
1
(L−2 + L6 )
2
1
(L−3 + L8 )
2

13

L2
1
(L0 + L5 )
2
1
(L−1 + L7 )
2

Table 3. Multiplication table for a sample of generators of the aperiodic Jordan algebra J (Fpal ).

specific tiling presented in [MT03] that is a special case of the general setting proposed by Baake. Indeed,
the vertices of such tilings are given by the aperiodic set
Ξ = {z ∈ Z [τ ] △ ⊂ C : z ∗ ∈ Ω} ,
{
}
where the acceptance window Ω is the convex pentagon with vertices 1, ξ, ξ 2 , ξ 3 , ξ 4 , with ξ = exp (2πi/5),
and △ is the root system of type H2 given by
)}
)
(
)
(
{
(
(6.7)
△ = ±1, ±ξ 2 , ± 1 + τ ξ 2 , ± τ + ξ 2 , ± τ + τ ξ 2 .

(6.6)

The aperiodic set Ξ is a model set of the following cut-and-project scheme
Ξ
∩
C

(6.8)

π

1
←−

Λ
∩
C×C

Ω
∩
π2
−→
C

where the lattice Λ is given by (Z + iZ) × (Z + iZ) and
(6.9)

π1 (x, y, z, w) = x + yτ + (z + wτ ) ξ 2 ,

(6.10)

π2 (x, y, z, w) = x + y (1 − τ ) + (z + w (1 − τ )) ξ 4 ,

so that the star-map ∗ sends
(6.11)

{

ξ ∗ −→
ξ2,
∗
τ −→ 1 − τ.

Such cut-and-project scheme allows the labeling of elements of the quasicrystal Ξ through the use of
quadruples (a, b, c, d) of Z4 , i.e.
(a, b, c, d) −→ z = a + bτ + (c + dτ ) ξ 2 ,

(6.12)

where a, b, c, d ∈ Z which are also called the integer coordinates of z. A sample of the quasicrystal in its
integer coordinates is given in Tab. 4.
The aperiodic Jordan algebra J (Ξ) is defined to be the real vector space spanned by {Lz }z∈Ξ equipped
with the bilinear product given by
1
(Lz⊢w + Lw⊢z ) ,
2
for
{ every z,
} w ∈ Ξ. An integral formulation of the same algebra, i.e. an isomorphic algebra with generators
L(a,b,c,d) (a,b,c,d)∈Z4 , can be obtained from (4.4) as
(6.13)

(6.14)
(6.15)

Lz ◦ Lw =

L(a,b,c,d) ◦ L(a′ ,b′ ,c′ ,d′ ) =

1(
L(a′ +(a−a′ )+(b−b′ ),b+(a−a′ )+(b−b′ ),c′ +(c−c′ )+(d−d′ ),d+(c−c′ )+(d−d′ )) +
2
)
+L(a+(a−a′ )+(b−b′ ),b′ +(a−a′ )+(b−b′ ),c+(c−c′ )+(d−d′ ),d′ +(c−c′ )+(d−d′ )) .

## PDF page 14

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

Ξ

z2 (n2 )

z1 (n1 )

14

−3

−2

−1

0

1

2

..
.

..
.

..
.

..
.

..
.

..
.

−5

...

(−2, −2, −2 − 4)

(−2, −2, −1, −2)

(−2, −2, 0, 1)

(−2, −2, 0, 0)

(−2, −2, 1, 1)

(−2, −2, 2, 3)

−4

...

(−1, −3, −4, −6)

(−1, −3, −3, −5)

(−1, −3, −2, −3)

(−1, −3, 0, 0)

(−1, −3, 1, 2)

(−1, −3, 2, 3)

−3

...

(−1, −2, −1, −2)

(−1, −2, −1, −1)

(−1, −2, 0, −1)

(−1, −2, 0, 0)

(−1, −2, 0, 1)

(−1, −2, 1, 1)

−2

...

(−1, −1, −1, −2)

(−1, −1, −1, −1)

(−1, −1, 0, −1)

(−1, −1, 0, 0)

(−1, −1, 0, 1)

(−1, −1, 1, 1)

−1

...

(0, −1, −2, −2)

(0, −1, −1, −2)

(0, −1, −1, −1)

(0, −1, 0, 0)

(0, −1, 0, 1)

(0, −1, 1, 1)

0

...

(0, 0, −1, −2)

(0, 0, −1, −1)

(0, 0, 0, −1)

0

(0, 0, 0, 1)

(0, 0, 1, 0)

1

...

(0, 1, −1, −2)

(0, 1, −1, −1)

(0, 1, 0, −1)

(0, 1, 0, 0)

(0, 1, 1, 1)

(0, 1, 1, 2)

2

...

(1, 1, −1, −2)

(1, 1, −1, −1)

(1, 1, 0, −1)

(1, 1, 0, 0)

(1, 1, 0, 1)

(1, 1, 1, 1)

3

...

(1, 2, −1, −2)

(1, 2, −1, −1)

(1, 2, 0, −1)

(1, 2, 0, 0)

(1, 2, 0, 1)

(1, 2, 1, 1)

4

...

(1, 3, −4, −7)

(1, 3, −2, −4)

(1, 3, −1, −2)

(1, 3, 0, −1)

(1, 3, 1, 1)

(1, 3, 3, 4)

5

...

(2, 2, −2, −3)

(2, 2, −1, −2)

(2, 2, −1, −1)

(2, 2, 0, 0)

(2, 2, 1, 2)

(2, 2, 2, 3)

Table 4. A sample of elements z in the quasicrystal. Every element z is given by
z (n, m) = z1 (n) + z2 (m) ξ 2 , with z1 (n) , z2 (m) ∈ Z [τ ] . Moreover, we intended
(a, b, c, d) ∈ Z4 as a short notation that corresponds to z = a + bτ + (c + dτ ) ξ 2 .

6.3. A Z6 -quasicrystal . Three-dimensional icosahedral quasicrystals can be obtained by projection
from three different lattices in a six-dimensional embedding space R6 . These lattices are the primitive
cubic lattice P , i.e. Z6 lattice, the face-centred cubic lattice 2F , i.e. the root lattice D6 , and the bodycentred cubic lattice I (reciprocal to 2F ), i.e. the weight lattice D6 , respectively [PKK97]. Here we
consider a cut and project scheme analogous to that of the Z6 -quasicrystal obtained in [KD86], where
the embedding space is R6 and the lattice is given by the integral lattice Z6 , i.e.

(6.16)

Ξ
∩
R3

π

1
←−

Z6
∩
3
R × R3

where the maps π1 and π2 are given by



1 τ 0 0 0 0
1
(6.17)
π1 =  0 0 1 τ 0 0  , π2 =  0
0 0 0 0 1 τ
0

Ω3
∩
π2
−→ R3

(1 − τ )
0
0

0
0
1 (1 − τ )
0
0


0
0
,
0
0
1 (1 − τ )

and the acceptance window Ω3 is given by the rhombic triacontahedron, i.e. the convex hull obtained
from the following 32 vertices

(6.18)

(0, ±1, ±τ ) ,

(
)
0, ±τ, ±τ −1 ,

(±τ, 0, ±1) ,
(±1,
( −1±1, ±1)),
±τ , 0, ±τ ,

(±1, ±τ, 0) ,

(
)
±τ, ±τ −1 , 0 .

We thus have that the Z6 -quasicrystal is given by the model set
}
{
(6.19)
Ξ = π1 (x) ∈ R3 : x ∈ Z6 , π2 (x) ∈ Ω3 .

An equivalent definition of Ξ can be achieved in a straightforward way through the aid of an icosian
cut and project set-up as in (3.4), considering the embedding of R3 in the pure immaginary quaternions
Pu [H] given by
(6.20)

R3 ∋ (x, y, z) −→ xi + yj + zk ∈ Pu [H] .

We thus obtain the icosian formulation of the model set of Ξ as
(6.21)

Ξ = {x ∈ Pu [I] : x∗ ∈ Ω3 } ,

where the star-map is the usual one defined in (2.15).

## PDF page 15

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

15

6.4. The Elser-Sloane quasicrystal. The Elser-Sloane quasicrystal C is a famous quasicrystal with
an H4 symmetry that was introduced by Elser and Sloane in [ES] obtained as a projection of the eight
dimensional lattice Λ (E8 ). In order to follow Elser and Sloane construction in [ES], we use for this
quasicrystal the cut-and-project scheme over the E8 lattice
√ as in (3.10), which is equivalent to that
in (3.4) over the icosians lattice Ĩ. Therefore, let c∗ = 1/ (4 + 2τ ) and κ = τ c∗ . Moreover, let the
acceptance window ΩES be the convex hull of the following 720 vertices, i.e.
(6.22)
(
)
1
1
1
±1, ±τ, ±τ −1) ,
2 κ (±2, 0, 0, 0) , )
2 κ (±1, ±1, ±1, ±1) ,
2 κ 0,
(
(
)
(
1
1
1
1
2
−2
2
−1
±1, 0 , )
, ±τ −1 , ±τ −1 ,
3 κ ±τ , ±τ
2(κ 0, ±1, ±τ, ± τ ,)
(3 κ ±τ , ±τ , −1
1
1
1
−2
, ±τ, 0 ,
,
3 κ ± (2τ − 1) , ±τ
3 κ (±((2τ − 1) , ±1, ±1, ±1)
3 κ ±τ, ±τ, ±τ, ±τ
) ,
1
1
−1
κ
(±2,
±2,
0,
0)
,
κ
±2,
±1,
±τ,
±τ
,
3
3

considered with all choices of signs and any even permutation of the coordinates. Then, the Elser-Sloane
quasicrystal C is the model set from the cut-and-project scheme in (3.10) given by
{
}
(6.23)
Ξ∼
= C = x ∈ π∥ (X) : X ∈ Λ (E8 ) , π⊥ (X) ∈ ΩES ,
for a complete treatment reference see [ES, sec. 4].
Even though from an historical point of view the Elser-Sloane quasicrystal was defined as (6.23), an
equally valid quaternionic realisation of the quasicrystal that make use of the cut-and-project scheme in
(3.4) is
(6.24)
C ∼
= Ξ = {x ∈ I : x∗ ∈ ι (ΩES )} ,

where the star map ∗ is that in (2.15) and ι (ΩES ) is the image of the acceptance window ΩES through
the canonical identification (2.11) between R4 and H.
7. conclusions and further developments
In this work we presented a Jordan structure naturally linked to a class of icosahedral quasicrystal
arising from a cut-and-project setup with convex acceptance window. The resulting Jordan algebras are
infinite dimensional and fits into the class of aperiodic algebras introduced by Patera et al. in [PPT98].
Aperiodic Jordan algebras were firstly defined by the authors in [CCAI] for a Fibonacci chain quasicrystal
and later on extended to a Penrose tiling in [CCAI2], but never fully studied in a general setting as this
one. In this work we showed some common features of such algebras, such as the lack of the unit
element (even though they can obviously be extended to a unital Jordan algebra) and the lack of finite
dimensional subalgebras with dimension greater than 1. We also showed that such algebras enjoy a noncrystallographic symmetry when the acceptance window does. As for the physical applications and future
works, aperiodic algebras found applications in integrable systems [TW00b] and in theoretical frameworks
[Tw99a]. On the other hand, it is well known that Jordan algebras are relevant in exactly solvable models
involving propagation of solitons. Indeed, it is well known a one-to-one correspondence between finite
dimensional Jordan algebra and multifield Korteweg-de Vries equations[Sv91]. Similar results hold for
the modified KdV equation [Sv93], for the Sine-Gordon equation and for generalisations of the nonlinear Schrodinger equation [Sv92]. We thus expect that propagation of certain kind of excitations in
quasicrystal structures might be related with the Jordan algebras presented here.
8. Acknowledgment
This work was funded by the Quantum Gravity Research institute. Authors would like to thank Fang
Fang, Marcelo Amaral, Dugan Hammock, and Richard Clawson for insightful discussions and suggestions.
References
[AC03]

E.L. Albuquerque and M.G. Cottam Theory of elementary excitations in quasiperiodic structures Physics Reports
Volume 376, Issues 4–5, March 2003, Pages 225-337
[Ba98] Baake M., A guide to mathematical quasicrystals in: Quasicrystals, eds. J. B. Luck, M. Schreiber, P. Haussler,
Springer, (1998).
[Ba13] Baake M. and Grimm U. Aperiodic Order. Cambrage University Press, 2013.
[BaHu] Baake, M. & Huck, C. Discrete tomography of Penrose model sets Philosophical Magazine, 87 (2007) 2839-2846
[BM94] Berman S. & Moody R. The algebraic theory of quasicrystals with icosahedral symmetries, Journal of Physics A
27 (1994) 115-129

## PDF page 16

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

[CoSl]
[CCAI]

16

Conway J.H. & Sloane N.J.A., Sphere Packings, Lattices and Groups, Springer New York, 1993.
Corradetti D., Chester D., Aschheim R., Irwin K., Three Fibonacci-chain Aperiodic Algebras, Quaest. Math. 46,1
(2023) 1-13.
[CCAI2] Corradetti D., Chester D., Aschheim R., Irwin K., An aperiodic Jordan algebra over a Penrose tiling, arXiv
(2022).
[Co34] Coxeter, H. S. M. Discrete groups generated by reflections, Annals of Mathematics, (1934) 35 (3): 588–621
[Co73] Coxeter, H. S. M. (1973). Regular Complex Polytopes, Cambridge University Press, Cambridge
[DBT12] Dechant, P. P., Boehm, C. & Twarock, R. (2012). Novel Kac–Moody-type affine extensions of non-crystallographic
Coxeter groups J. Phys. A: Math. Gen. 45 (28), 285202.
[De21] Dechant P., Clifford Spinors and Root System Induction: H4 and the Grand Antiprism, Adv. Appl. Clifford
Algebras (2021) 31:57
[ES]
Elser V. and Sloane N. J., A highly symmetric quasicrystal, J. Phys. A: Math.Gen., 20 (1987) 6161.
[FK15] Fang F. and Klee I. An Icosahedral Quasicrystal as a Golden Modification of the Icosagrid and its Connection to
the E8 Lattice Acta Crystallogr. A: Found. Adv. (2015) 71(a1).
[FrKo] Fring A. and Korff C., Affine Toda field theories related to Coxeter groups of non-crystallographic type, Nucl.
Phys. B729 (2005), 361–386.
[Ha]
Hamilton W.R., Memorandum respecting a new system of roots of unity. The London, Edinburgh, and Dublin
Philosophical Magazine and Journal of Science: 12 (1856), p. 446.
[HMSK] J. Hielscher, M. Martinsons, M. Schmiedeberg, and S. C. Kapfer. Detection of phonon and phason modes in
intrinsic colloidal quasicrystals by reconstructing their structure in hyperspace. J. Phys. Condens. Matter, 29:
094002, 2017.
[Kac]
Kac V., Infinite dimensional Lie algebras, Cambridge University Press, 1990.
[Koc89] Koca M., Icosians versus octonions as descriptions of the E8 lattice, J. Phys. A: Math. Gen. 22 (1989) 1949
[KD86] Katz, A.; Duneau, M. Quasiperiodic patterns and icosahedral symmetry. J. Phys. France 1986, 47, 181–196.
[MP93] Moody R. V. and Patera J. Quasicrystals and icosians. Journal of Physics A: Mathematical and General ,
26(12):2829, 1993.
[LeSt]
D. Levine and P. J. Steinhardt. Quasicrystals: A New Class of Ordered Structures. Phys. Rev. Lett., 53:2477,
1984.
[Ma]
Macia E., The role of aperiodic order in science and technology 2006 Rep. Prog. Phys. 69 397
[Ma02] V. Mazorchuk, On quasicrystal lie algebras. Journal of Mathematical Physics, 43.5 (2002):2791.
[MT03] V. Mazorchuk and R. Twarock, Virasoro-type algebras associated with a penrose tiling, Journal of Physics A:
Mathematical and General, 36.15 (2003):4363-4373.
[MW94] Moody R. V. & Weiss A. On Shelling E8 Quasicrystals. Journal of Number Theory, 47(3) (1994) 405–412.
[Mo00] Moody R.V., Model Sets: A Survey. In: Axel F., Donoyer F., Gazeau, JP. (eds) From Quasicrystals to More
Complex Systems. Centre de Physique des Houches, vol 13. Springer, Berlin, Heidelberg, 2000.
[PKK97] Papadopolos Z., Klitzing R., and Kramer P. Quasiperiodic icosahedral tilings from the six-dimensional bcc lattice.
Journal of Physics A: Mathematical and General, 30 6 (1997) L143–L147.
[Pa95] Patera J., The pentacrystals. In: Axel, F., Gratias, D. (eds) Beyond Quasicrystals. Centre de Physique des
Houches, vol 3. Springer, Berlin, Heidelberg, 1995.
[PPT98] Patera J. , E. Pelantova, and R. Twarock, Quasicrystal Lie Algebras Phys Lett 246A (1998) 209-213.
[PT02] Patera J. and Twarock R., Affine extension of noncrystallographic Coxeter groups and quasicrystals J. Phys. A:
Math. Gen. 35 (2002) 1551
[Pen]
Penrose R., The role of aesthetics in pure and applird mathematical research, Bulletin of the Institute of Mathematics and Its Applications, 10 (1974) 266-271.
[Se95]
M. Senechal, Quasicrystals and Geometry Cambridge University Press (1995).
[Se]
Serre J.P., Algebres de Lie semi-simples complexes. W.A. Benjamin, 1966.
[Shc]
O. P. Shcherbak, Wavefronts and reflection groups, Uspekhi Mat. Nauk, 1988, 43,3 (261), 125– 160
[ShBGC] D. Shechtman, I. Blech, D. Gratias, and J. W. Cahn, Metallic Phase with Long-Range Orientational Order and
No Translational Symmetry, Phys. Rev. Lett. 53 (1984) 1951.
[ShuMa] Shutov A.V., Maleev A.V. , Penrose tilings as model sets. Crystallogr. Rep. 60 (2015) 797–804.
[Sv91]
Svinolupov S.I., Jordan algebras and generalized Korteweg-de Vries equations. Theor Math Phys 87 (1991) 611–
620.
[Sv92]
Svinolupov S.I., Generalized Schrodinger equations and Jordan pairs. Commun.Math. Phys. 143 (1992) 559–575.
[Sv93]
Svinolupov S.I., Jordan algebras and integrable systems Funct. Anal. its Appl. 27 (1993) 257–265
[Tw00] R. Twarock, Aperiodic Virasoro algebra, J.Math Phys 41 (2000) 5088- 5106.
[TW00b] R. Twarock, An exactly solvable Calogero model for a non-integrally laced group. Physics Letters A, 275.3
(2000):169172.
[Tw99a] R. Twarock, Breaking Virasoro symmetry in Quantum Theory and Symmetries ed H-D Doebner, V K Dobrev,
J-D Hennig and W Lucke, Singapore: World Scientific, 1999, pp 530–4.
[Ze]
Zel’manov E.I., On prime Jordan algebras, Alg. i Logika 18 (1979), 162-175.

## PDF page 17

JORDAN ALGEBRAS OVER ICOSAHEDRAL CUT-AND-PROJECT QUASICRYSTALS

Departamento de Matematica, Universidade do Algarve, Campus de Gambelas, Faro, PT
Email address: d.corradetti@gmail.com
Quantum Gravity Research, Los Angeles, California, CA 90290, USA,
Email address: DavidC@QuantumGravityResearch.org
Quantum Gravity Research, Los Angeles, California, CA 90290, USA,
Email address: Raymond@QuantumGravityResearch.org
Quantum Gravity Research, Los Angeles, California, CA 90290, USA,
Email address: Klee@QuantumGravityResearch.org

17
