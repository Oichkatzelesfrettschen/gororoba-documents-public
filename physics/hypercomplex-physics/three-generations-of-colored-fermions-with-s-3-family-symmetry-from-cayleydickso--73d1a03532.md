Source: https://doi.org/10.1140/epjc/s10052-023-11923-y
PDF sha256: 73d1a03532d62ef7dc9f1871f47af7007979838c52ec25030420690c085f2679
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine-gated

# Transcription of three-generations-of-colored-fermions-with-s-3-family-symmetry-from-cayleydickso--73d1a03532.pdf

Transcription of `three-generations-of-colored-fermions-with-s-3-family-symmetry-from-cayleydickso--73d1a03532.pdf` in this directory, 13 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-13 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Eur. Phys. J. C (2023) 83:747
https://doi.org/10.1140/epjc/s10052-023-11923-y

Regular Article - Theoretical Physics

Three generations of colored fermions with S3 family symmetry
from Cayley–Dickson sedenions
Niels Gresnigta , Liam Gourlay, Abhinav Varma
Department of Physics, Xi’an Jiaotong-Liverpool University, 111 Ren’ai Rd., Dushu Lake Science and Education Innovation District, Suzhou
Industrial Park, Suzhou 215123, People’s Republic of China

Received: 19 June 2023 / Accepted: 9 August 2023 / Published online: 24 August 2023
© The Author(s) 2023

Abstract An algebraic representation of three generations of fermions with SU (3)C color symmetry based on
the Cayley–Dickson algebra of sedenions S is constructed.
Recent constructions based on division algebras convincingly describe a single generation of leptons and quarks with
Standard Model gauge symmetries. Nonetheless, an algebraic origin for the existence of exactly three generations
has proven difficult to substantiate. We motivate S as a natural algebraic candidate to describe three generations with
SU (3)C gauge symmetry. We initially represent one generation of leptons and quarks in terms of two minimal left ideals
of Cℓ(6), generated from a subset of all left actions of the
complex sedenions on themselves. Subsequently we employ
the S3 automorphism of order three, which is an automorphism of S but not of O, to generate two additional generations. Given the relative obscurity of sedenions, efforts have
been made to present the material in a self-contained manner.

1 Introduction
Despite its great practical success in colliders and other
experiments, there are several unexplained features of the
Standard Model of particle physics (SM) which lack a
deeper theoretical motivation. These include, among others,
a derivation of the SM gauge group from first principles, an
explanation for why some representations of the SM gauge
group correspond to particle multiplets whereas others do
not, and an account for why fermions come in three generations. These theoretical shortcomings may be suggestive
that the SM ultimately emerges from a more fundamental
physical principle or mathematical structure.
In an attempt to establish the geometric and algebraic roots
of the SM, several proposals have been put forth over the

years which take as its essential mathematical ingredients
(tensor products of) the only four normed division algebras
over the reals: R, C, H, and O. Instead of unifying the internal
symmetries into a single larger group, as is done in grand unified theories (GUTs) such as SU (5) and Spin(10), these division algebraic approaches attempt to unify the gauge groups
together with the leptons and quarks that they act on into a
single unified algebraic framework, in terms of an algebra
acting on itself.
The octonions O, the largest of the division algebras, were
first considered in the 70s for their intriguing efficacy in
describing quark color symmetry [1]. Dixon [2–4] considers the algebra R ⊗ C ⊗ H ⊗ O and its invariant subspaces
in connection to the particles and charges of the SM. The
algebra R ⊗ C ⊗ H ⊗ O has exactly the right dimensions
(32 complex) to describe one generation of fermions. In a
closely related approach, Furey studies the minimal ideals
of the Clifford algebras Cℓ(4), and Cℓ(6), generated from
C ⊗ H, and C ⊗ O respectively [5,6]. In her approach, the
leptons and quarks correspond to elements of these minimal
ideals, and the gauge symmetries are those unitary symmetries that preserve the ideals. In particular, the C ⊗ O part
of Dixon’s algebra can be associated to the color and electric charge internal degrees of freedom, with the color gauge
group SU (3) corresponding to the maximal subgroup of the
exceptional group G 2 of automorphisms of O which fixes
one of the octonion units.
Many others have contributed to these, and related, algebraic approaches including those based on topology [7–11],
exceptional Lie groups [12–17], Clifford algebras [18–26],
and Jordan algebras [27–32].
Existing division algebraic models offer an elegant algebraic construction for the internal space of a single generation
of leptons and quarks. Despite several attempts [4,33,34], a
clear algebraic origin for the existence of three generations

a e-mail: niels.gresnigt@xjtlu.edu.cn (corresponding author)

123

## PDF page 2

747 Page 2 of 13

is yet to be found. The Pati–Salam model, as well as both
the SU (5) and Spin(10) grand unified theories likewise correspond to single generation models, lacking any theoretical basis for three generations, which ultimately has to be
imposed by hand.
Furey identifies three generations of color states directly
from the algebra Cℓ(6) generated from the adjoint actions of
C ⊗ O [33]. The algebra Cℓ(6) is 64 complex dimensional.
Constructing two representations of the Lie algebra su(3)
within this algebra, the remaining 48 degrees of freedom
transform under the action of the SU (3) as three generations of leptons and quarks. The most obvious extension is
to include U (1)em via the number operator, which works in
the context of a one-generation model, but fails to assign the
correct electric charges to states in a three-generation model.
A generalized action that leads to a generator that produces
the correct electric charges for all states is introduced in [35].
Dixon on the other hand considers the algebra T6 = C ⊗
2
H ⊗ O3 , where T = R ⊗ C ⊗ H ⊗ O in order to represent
three generations, with a single generation being described
by T2 , a complexified (hyper) spinor in 1+9D spacetime [3].
However, the choice T6 , as opposed to any other T2n appears
rather arbitrary, although can be motivated from the Leech
lattice.
These division algebraic models share many similarities
with those based on the exceptional Jordan algebra J3 (O)
consisting of three by three matrices over O, which has likewise been proposed to describe three generations [27–32]. In
these models, each of the three octonions in J3 (O) is likewise
associated with one generation via the three canonical J2 (O)
subalgebras of J3 (O).
In [24] it is argued that R ⊗ C ⊗ H ⊗ O-valued gravity can
naturally describe a grand unified field theory of Einstein’s
gravity with a Yang–Mills theory containing the SM, leading
to a SU (4)4 symmetry group that potentially extends the SM
with an extra fourth family of fermions. The existence of
a fourth generation of fermions lacks experimental support
however.
In [36] it is shown how, by choosing a privileged C subalgebra of O, it is possible to reduce ten dimensional spacetime represented by S L(2, O) to four dimensional spacetime
S L(2, C). This process of dimensional reduction naturally
isolates three H subalgebras of O: those that contain the privileged C subalgebra. These three intersecting H subalgebras
are subsequently interpreted as describing three generations
of leptons.
Starting with R, each of the remaining three division algebras can be generated via what is called the Cayley–Dickson
(CD) process. This process does not terminate with O however, but continues indefinitely to produce a series of 2n dimensional algebras. We therefore ask the question: Can
we go beyond the division algebras, to the CD algebra of

123

Eur. Phys. J. C (2023) 83:747

sedenions S, generated from O, in order to describe three
generations?
The present paper advocates that the CD algebra of sedenions S constitutes a natural mathematical object which
exhibits the algebraic structure necessary to describe the
internal space of three generations. We restrict ourselves for
the time being to considering only the SU (3)C color symmetry of leptons and quarks.
The algebra S was first proposed to play a role in describing three generations in [34]. The key idea behind that proposal was to generalize the constructing of three generations
of leptons in terms of three H subalgebras of O in [36] to three
generations in terms of three O subalgebras of S, where each
generation is associated with one copy of O. One finds, as
in [36], that the resulting three generations are not linearly
independent. It was suggested in [34] (and later in [14]) that
this overlap could provide an algebraic basis for neutrino
oscillations and quark mixing, although the viability of this
idea remains to be investigated.
The model in [34] suffers from two significant drawbacks.
Each generation comes with its own copy of SU (3)C thereby
also requiring three generations of gluons, for which there
is currently no experimental evidence. Additionally, it turns
out that Aut (S) = Aut (O) × S3 , where Aut (O) = G 2 , and
S3 is the permutation group of three objects [37,38]. The
S3 automorphisms of S were however not given any clear
physical interpretation, in part because these automorphisms
stabilize the octonion subalgebras in S.
The model we present here builds on [34] and seeks to
resolve the shortcomings just mentioned. Instead of associating each O subalgebra of S with one generation, we use
all three O subalgebras to construct a single generation. This
corresponds to a direct generalization of the construction in
[5] where three H subalgebras of O are used to construct a
single generation. Subsequently, we utilize the sedenion S3
automorphism of order three to generate the additional two
generations. This construction provides a clear interpretation
of the new S3 automorphism. Furthermore, all three generations transform as required under a single copy of the gauge
group SU (3)C , thereby avoiding introducing three generations of gluons.
In the next section we provide a brief overview of the
normed division algebras, in particular the quaternions H
and octonions O. In Sect. 3 we review the construction of
one generation of fermions with unbroken SU (3)c ×U (1)em
gauge symmetry from C ⊗ O, following closely [5]. The CD
construction and the algebra of sedenions are discussed in
Sect. 4. Finally we present our three generation model based
on the algebra of sedenions in Sect. 5. We conclude with an
outlook of how to develop the model further, and a discussion.

## PDF page 3

Eur. Phys. J. C (2023) 83:747

Page 3 of 13 747

2 Normed division algebras
An algebra A over a field K is a vector space over K (where
the scalars used in scalar multiplication come from the field
K), equipped with a bilinear product A×A → A, that allows
for multiplication of algebra elements.
A division algebra is an algebra over a field where division
is always well-defined, except by zero. A normed division
algebra has the additional property that it is also a normed
vector space, with the norm defined in terms of a conjugate. A well-known result by Hurwitz [39] is that there exist
only four normed division algebras (over the field of real
numbers): R, C, H, O, of dimensions one, two, four and
eight respectively. In going to higher-dimensional algebras,
successive algebraic properties are lost: R is self-conjugate,
commutative and associative, C is commutative and associative (but no longer self-conjugate), H is associative but no
longer commutative, and finally O is neither commutative
nor associative (but alternative).
The quaternions H are a generalization of the complex
numbers C with three mutually anticommuting imaginary
units I, J, K , satisfying;
I 2 = J 2 = K 2 = I J K = −1,
which implies I J = K = −J I , J K = I = −K J , and
K I = J = −I K . A general quaternion q may then be
written as
q = q0 1 + q1 I + q2 J + q3 K , q0 , q1 , q2 , q3 ∈ R
With the quaternion conjugate q defined as q = q0 − q1 I −
q2 J − q3 K . The norm of a quaternion |q| is subsequently
defined by |q|2 = qq = qq, and the inverse q −1 = q/|q|2 .
The automorphism group of H is SU (2). Indeed, there
is an isomorphism between the quaternions H and the real
Clifford algebra Cℓ(0, 2), while the complexified quaternions C ⊗ H (isomorphic to the Pauli algebra) are isomorphic to the complex Clifford algebra Cℓ(2). Note, however,
that C ⊗ H is not a division algebra (but remains associative), and manifestly contains projectors, for example:
(1 + i K )(1 − i K ) = 0.
The octonions O are the largest division algebra, of dimension eight. Its orthonormal basis is comprised of seven imaginary units: i 1 , . . . i 7 , along with the unit 1 = i 0 . A general
octonion x may then be written as
x = x0 i 0 + x1 i 1 + · · · + x7 i 7 , x0 , . . . , x7 ∈ R
with the octonion conjugate x defined as x = x0 i 0 − x1 i 1 −
· · · − x7 i 7 . The norm of an octonion |x| is subsequently
defined by |x|2 = x x = x x, and the inverse x −1 = x/|x|2 .

Fig. 1 The Fano plane, encoding the multiplicative structure of our
octonions, where a ≡ i a , a = 1, . . . , 7. Note that each line is cyclic,
representing a quaternionic triple

The multiplication of octonions1 is captured in terms of
the Fano plane, see Fig. 1. Each projective line in the Fano
plane corresponds (together with the identity i 0 ) to a H
subalgebra; there are seven such subalgebras. Like with H,
all the imaginary units anticommute under multiplication.
Unlike with H, the multiplication of elements not belonging
to the same H subalgebra is non-associative. For example
i 4 (i 7 i 6 ) = −i 5 ̸= i 5 = (i 4 i 7 )i 6 . Octonion multiplication
however is alternative x(x y) = (x x)y and y(x x) = (yx)x,
∀x, y ∈ O. The complexified octonions C ⊗ O are again not
a division algebra (but remains alternative).
As vector spaces O = C4 . The splitting of O as C ⊕ C3
relies on choosing a preferred octonion unit i a (and hence a
preferred C subalgebra in O). For our purpose we choose i 4 .
The map [36]
π(x) =

1
(x + i 4 x i¯4 ), x ∈ O
2

where i¯4 indicates the octonion conjugation, then projects O
down to this preferred C ⊂ O, and we can write the octonion
x = x0 i 0 + · · · + x7 i 7 as:
x = (x0 + x4 i 4 )i 0 + (x1 − x5 i 4 )i 1
+(x2 − x6 i 4 )i 2 + (x3 − x7 i 4 )i 3 .
Note that the product i 4 x i¯4 is defined unambiguously since
O is alternative.
The automorphism group of O is known to be the exceptional Lie group G 2 . This exceptional group contains SU (3)
as one of its maximal subgroups, corresponding to the stabilizer subgroup of one of the octonion imaginary units, or
equivalently, the subgroup of Aut(O) that preserves the representation of O as the complex space C ⊕ C3 . This splitting
is associated with the quark-lepton symmetry [36]. The space
1 There are different multiplication rules for O used by different authors

in the literature. Here we follow the multiplication table used in [40].

123

## PDF page 4

747 Page 4 of 13

Eur. Phys. J. C (2023) 83:747

of internal states of a quark is then the three complex dimensional space C3 whereas the internal space of a lepton is C.
Since O and C ⊗ O are nonassociative, they are not representable as matrix algebras (with the standard matrix product). The algebra generated from the composition of left and
right actions of O (and C ⊗ O) however is associative, since
each such left (right) action corresponds to a linear operator
(endomorphism).
Let L a (Ra ) denote the linear operator of left (right) multiplication by a ∈ C ⊗ O:
L a [x] = ax,

Ra [x] = xa, ∀a, x ∈ C ⊗ O.

(1)

Then
L a L b [x] = a(bx) ̸= L ab [x] = (ab)x,
Ra Rb [x] = (xb)a ̸= Rab [x] = x(ab).
The mappings a → L a and a → Ra do not correspond to
algebra homomorphisms as they each generate an associative
algebra called the associative multiplication algebra.2 They
do however preserve the quadratic relations ⟨x, y⟩ = 21 (x y +
yx) where x, y ∈ C ⊗ O
L x L y 1 + L y L x 1 = 2⟨x, y⟩1 = Rx R y 1 + R y Rx 1
Since L a (Ra ) correspond to linear operators, they can be
represented as 8 × 8 complex matrices (acting on the vector
space C ⊗ O written as a column vector).
For C ⊗ O, one finds the following identities [4,5]:
L i1 L i2 L i3 L i4 L i5 L i6 x = L i7 x,

(2)

...L ib L ia L ia L ic ....x = −...L ib L ic ....x

(3)

...L ia L ib ...x = −...L ib L ia ...,

(4)

where a, b, c = 1, . . . , 7.
Due to the nonassociativity of O, the left (right) associative
multiplication algebra of C⊗O contains genuinely new maps
which are not captured by C ⊗ O. For example, i 3 (i 4 (i 6 +
i 2 )) ̸= y(i 6 + i 2 ) for any y ∈ C ⊗ O. There are a total of
64 distinct left-acting complex-linear maps from C ⊗ O to
itself, and these (due to the given identities above) provide a
faithful representation of Cℓ(6).
Denoting the 64-dimensional left (right) associative multiplication algebra generated from left (right) actions of C ⊗ O
on itself by (C ⊗ O) L ((C ⊗ O) R ), one finds that any left
(right) action can always be rewritten as a right (left) action
[4]. That is:
(C ⊗ O) L ∼
= (C ⊗ O) R ∼
= Cℓ(6).

(5)

This is in contrast to a similar construction for C ⊗ H, where
one finds that the left and right actions are genuinely distinct,
each generating a copy of Cℓ(2). The left and right adjoint

actions in this case commute, and only by considering both
does one obtain a basis for Mat (4, C) ∼
= Cℓ(4).
3 One generation of electrocolor states from C ⊗ O
Let e1 := L i1 , . . . , e6 := L i6 be a generating basis (over C6 )
for Cℓ(6) associated with the left multiplication algebra of
the complex octonions, satisfying ei2 = −1, ei e j = −e j ei .
Define the Witt basis
1
1
α1† = (e1 + ie5 ), α1 = (−e1 + ie5 ),
2
2
1
1
α2† = (e2 + ie6 ), α2 = (−e2 + ie6 ),
2
2
1
1
†
α3 = (e3 + ie7 ), α3 = (−e3 + ie7 ).
2
2
Here † corresponds to the composition of complex and octonion conjugation. This new basis satisfies the anticommutation relations3
{αi , α j } = {αi† , α †j } = 0, {αi , α †j } = δi j .

(6)

Each pair of ladder operators in isolation generates Cℓ(2),
and is associated with one of the three H subalgebras of
O that contain the privileged complex subalgebra generated
by e4 . Subsequently, we obtain three anticommuting copies
of Cℓ(2), which when considered together generate the full
Cℓ(6) left multiplication algebra of C ⊗ O.
From the Witt basis, it is possible to construct two minimal
left ideals of the algebra Cℓ(6), following the procedure in
[41] (see [5] for a detailed construction):
Cℓ(6)ωω† ,

Cℓ(6)ω† ω,

where ω = α1 α2 α3 and ω† = α3† α2† α1† are nilpotents, but
ωω† and ω† ω are primitive idempotents. Each ideal is eight
complex dimensional. Explicitly,
S u = νωω†
+d r α1† ωω† + d g α2† ωω† + d b α3† ωω†
+u r α3† α2† ωω† + u g α1† α3† ωω† + u b α2† α1† ωω†
+e+ α3† α2† α1† ωω† ,
S d = νω† ω
+d r α1 ω† ω + d g α2 ω† ω + d b α3 ω† ω
+u r α3 α2 ω† ω + u g α1 α3 ω† ω + u b α2 α1 ω† ω
+e− α3 α2 α1 ω† ω,
where the suggestively labelled coefficients are elements of
C.
The unitary symmetries that preserve the Witt basis, and
hence the minimal left ideals is U (3) = SU (3) × U (1).

2 We will henceforth refer to this algebra simply as the left action alge-

bra or left multiplication algebra.

123

3 Note that as left actions we have {L

αi , L α j }x = 0 etc for x ∈ C ⊗ O.

## PDF page 5

Eur. Phys. J. C (2023) 83:747

Page 5 of 13 747

The generators of this symmetry, written in terms of the Witt
basis, are:
Λ1 = −α2† α1 − α1† α2 ,

Λ2 = iα2† α1 − iα1† α2 ,

Λ3 = α2† α2 − α1† α1 ,

Λ4 = −α1† α3 − α3† α1 ,

An orthonormal basis for S comprises 15 mutually anticommuting imaginary units s1 , . . . , s15 together with the unit
1 = s0 . The imaginary units s1 , .., s7 correspond to the original octonion units i 1 , . . . , i 7 . A general sedenion may then
be written as

Λ5 = −iα1† α3 + iα3† α1 , Λ6 = −α3† α2 − α2† α3 ,

w = w0 s0 + w1 s1 + · · · + w15 s15 , w0 , . . . , w15 ∈ R.

Λ7 = iα3† α2 − iα2† α3 ,

with the sedenion conjugate w defined as w = w0 s0 −w1 s1 −
· · · − w15 s15 , and the sedenion norm |w| defined by |w|2 =
ww = ww. Whenever |w|2 ̸= 0, the inverse of w is given
by w −1 = w/|w|2 .
The product of two sedenions w, v can be determined
using the multiplication table of the orthonormal basis units
of S provided in Appendix A, source [40,42], together with
linearity.
Because S is not a division algebra, it contains zero divisors. These are elements of the form

1
Λ8 = − √ (α1† α1 + α2† α2 − 2α3† α3 ),
3
and
Q=

1 †
(α α1 + α2† α2 + α3† α3 ).
3 1

(7)

The basis states of the Cℓ(6) minimal ideals transform as
1 ⊕ 3 ⊕ 3 ⊕ 1 under SU (3), and this symmetry can therefore
be associated with the color symmetry SU (3)C , justifying
the choice of coefficients. The U (1) generator Q (together
with −Q ∗ ), related to the number operator Q = N /3, on the
other hand gives correct electric charge for each state. The
ideal S u contains the isospin up states, whereas the ideal S d
contains the isospin down states.
One generation of leptons and quarks with correct unbroken SU (3)C × U (1)em symmetry can therefore be elegantly
represented in terms of two minimal left ideals of Cℓ(6) generated from C ⊗ O. The dimension of the minimal ideals
dictates the number of distinct physical states, whereas the
gauge symmetries are those unitary symmetries that preserve
the ideals (or equivalently, the Witt basis).

4 The Cayley–Dickson construction and the algebra of
sedenions
The CD process is an iterative construction that generates at
each stage an algebra (with involution) of dimension twice
that of the previous. Each algebra is constructed as a direct
sum of the previous algebra, so that C = R⊕Ri where i is the
complex structure introduced in the process. Similarly, H =
C ⊕ CJ , where i, J and i J are identified with the quaternion
imaginary bases I, J, K , and similarly O = H ⊕ Hi 4 .
This process does not terminate with O but continues,
generating a series of 2n -dimensional (non division) algebras. A generic element of the CD algebra An , can then
be written as a + bu, where a, b ∈ An−1 , and u is the
new imaginary unit introduced by the CD process applied
to An−1 . The fifth CD algebra A4 (A0 = R), generated
from O, is the 16-dimensional algebra of sedenions S. This
algebra is non-commutative, non-associative, and not even
alternative (x(x y) ̸= (x x)y and y(x x) ̸= (yx)x in general).
Other properties, like flexibility ((x y)x = x(yx)) and powerassociativity (x n associative), still hold (and hold for all CD
algebras).

(sa + sb )(sc + sd ) = 0,

sa , sb , sc , sd ∈ S.

There are 84 such zero divisors, and the subspace of zero
divisors of unit norm is homeomorphic to G 2 [43].
4.1 Octonion subalgebras inside the sedenions
Let us now use {e0 , e1 , . . . , en 2 −1 } to denote an orthonormal
basis for An , so that
A1 = C : {e0 , e1 },

e1 = i,

A2 = H : {e0 , e1 , e2 , e3 },

e1 = i = I, e2 = J, e3 = K

A3 = O : {e0 , e1 , . . . , e7 },

e1 = i = I = i 1 , . . . , e7 = i 7

A4 = S : {e0 , e1 , . . . , e15 },

e 1 = i = I = i 1 = s1 , . . . ,
e15 = s15

Consider A2 = H with basis {e0 , e1 , e2 , e3 }. Then there
are three subalgebras isomorphic to C within H, each containing the identity and one of the imaginary units of H. These
subalgebras correspond to three different complex structures
in H, and the common intersection of these three C subalgebras is isomorphic to R. The automorphism group of H is
Aut(H) = SU(2). The subset of automorphisms of H that
preserve a given complex structure is U (1), corresponding
to the element wise stabilizer subgroup of SU (2).
Applying the CD process to H generates O with basis
{e0 , e1 , e2 , e3 , e4 , e5 , e6 , e7 } where e4 is a newly introduced
anticommuting imaginary unit satisfying ei e4 = ei+4 . Via
this same construction, each of the three C ⊂ H subalgebras
generate a quaternion:

123

## PDF page 6

747 Page 6 of 13

Eur. Phys. J. C (2023) 83:747

CD

The generalisation from (C ⊗ O) L to (C ⊗ S) L is not
immediately obvious because the identities which held for
(C ⊗ O) L , namely

C1 : {e0 , e1 } −−→ H1 : {e0 , e1 , e4 , e5 },
CD

C2 : {e0 , e2 } −−→ H2 : {e0 , e2 , e4 , e6 },
CD

C3 : {e0 , e3 } −−→ H3 : {e0 , e3 , e4 , e7 }.
The common intersection of these three H ∈ O is isomorphic
to C, spanned by e0 and e4 . These Hi , i = 1, 2, 3 however
are not the only H subalgebras of O, and in total there are
seven such subalgebras. However H1 , H2 , H3 are the only
(quaternions) subalgebras that contain the new e4 . Together
with the identity, e4 corresponds to a complex structure.
Applying the CD process to O generates S. Apart from
the original O with basis {e0 , e1 , . . . , e7 }, S contains seven O
subalgebras (which we call non-principal). These are explicitly listed in [42]. Interestingly, all of these contain the new
imaginary unit e8 , introduced in the CD construction of S
from O.4 Via this process, each of Hi ⊂ O above generates
one Oi ∈ S.
CD

H1 −−→ O1 : {e0 , e1 , e4 , e5 , e8 , e9 , e12 , e13 },
CD

H2 −−→ O2 : {e0 , e2 , e4 , e6 , e8 , e10 , e12 , e14 },
CD

H3 −−→ O3 : {e0 , e3 , e4 , e7 , e8 , e11 , e12 , e15 }
Since each Hi contains e4 , and each Oi contains e8 , it follows
that each Oi also contains e4 e8 = e12 . That is, common
intersection of the three Oi now corresponds to a H ⊂ S:
O1 ∩ O2 ∩ O3 = H,
where this H is generated by {e0 , e4 , e8 , e12 }. O1 , O2 , O3
are the only (octonion) subalgebras of S that contain e4 , e8 ,
and e12 . Together with the identity, this corresponds to a
quaternionic structure.
In addition to the eight octonion subalgebras of S, there are
also a further seven quasi-octonion subloops Õ, satisfying all
the same properties of the octonion subalgebras, except for
the Moufang identities.5 As such, they are not isomorphic to
the octonion subalgebras. None of the Õ contain the element
e8 .
4.2 The left multiplication algebra of C ⊗ S
Despite the algebra S being non-associative and nonalternative, just as for O, we can consider the left actions
of S on itself as linear operators generating an associative
algebra.
4 Note that this is a new feature that appears with S. There are three
new, (that is excluding the original H with basis {e0 , e1 , e2 , e3 } used to
generate O) H subalgebras of O that do no contain e4 . For S there are
no new O that do not contain e8 .
5 The Moufang identities, describing a weaker notion of associativity,

are essentially equivalent to left and right alternativity, and flexibility.

123

L i1 L i2 L i3 L i4 L i5 L i6 x = L i7 x,

(8)

...L ib L ia L ia L ic ....x = −...L ib L ic ....x,

(9)

...L ia L ib ...x = −...L ib L ia ...,

(10)

where a, b, c = 1, . . . , 7 are no longer satisfied by general
composition of sedenion left multiplications. Although one
finds a new identify
L s1 L s2 ...L s14 w = L s15 w,

(11)

the two identities (9) and (10), crucial for generating a
Clifford algebra, no longer hold in general. For example,
s3 (s14 (s1 )) = −s14 (s3 (s1 )), but s3 (s14 (s2 )) = +s14 (s3 (s2 ).
Consequently, the left multiplications of the (complex) sedenions do not generate Cℓ(14), as one might initially expect.
However, since the linear operators corresponding to each
complex sedenion left multiplication can be written as a
16 × 16 matrix with complex entries acting on C ⊗ S written
as a column vector, one would expect to be able to generate Mat (16, C) ∼
= Cℓ(8). It then remains to find a suitable
set of sedenion elements that generate Cℓ(8) via their left
multiplication. Closer inspection reveals that all the left multiplications of the original octonion elements e0 = i 0 =
s0 , . . . , e7 = i 7 = s7 do satisfy the identities (9) and (10)
(where now the action is on C ⊗ S instead of C ⊗ O), as do
all new sedenion basis elements e9 = s9 , . . . , e15 = s15 :
ei (e j w) = −e j (ei w),

(12)

ei (ei w) = −w,

(13)

ei+8 (e j+8 w) = −e j+8 (ei+8 w),

(14)

ei+8 (ei+8 w) = −w,

(15)

where i, j = 1, . . . , 7, ∀ w ∈ C ⊗ S. However, ei and ei+8
fail to anti-commute (or commute) with each other as left
actions
ei (e j+8 w) ̸= −e j+8 (ei w).

(16)

The left action of e8 however anti-commutes with the left
action of every other basis element. One possible generating basis for Cℓ(8) is therefore given by the left multiplications of {e1 , . . . , e8 }. Another possible generating basis is
{e8 , . . . , e15 }.
Accepting some abuse of notation, we now simple write
L ei = ei and take e0 , e1 , . . . , e8 as our generating basis for
Cℓ(8). We will also no longer explicitly write w to indicate
that Cℓ(8) acts on w ∈ S from the left via composition.
The left action of the remaining sedenion basis elements
e9 , . . . , e15 then need to be expressed as the left action of
some element of Cℓ(8). After careful consideration one finds
that

## PDF page 7

Eur. Phys. J. C (2023) 83:747

1
(−e123458 + e123678 + e145678 − e18 ),
2
1
e10 = (−e123468 − e123578 + e245678 − e28 ),
2
1
e11 = (−e123478 + e123568 + e345678 − e38 ),
2
1
e12 = (e124568 + e134578 + e234678 − e48 ),
2
1
e13 = (e124578 − e134568 + e235678 − e58 ),
2
1
e14 = (e124678 − e135678 − e234568 − e68 ),
2
1
e15 = (e125678 + e134678 − e234578 − e78 ),
2

Page 7 of 13 747

e9 =

ψ : a + be8 →

(17)

4.3 Automorphisms of sedenions
Schafer [37] showed that for CD algebras An with n ≥ 4
(A0 = R), the derivation algebra der(An ) consists of derivations of the form a +bu → a D+(bD)u, where a, b ∈ An−1 ,
u is the new anticommuting imaginary unit introduced in the
CD construction of An from An−1 , and D is a derivation of
An−1 . Brown [38] demonstrated that if θ ∈ Aut (An−1 ), then
θ ′ : a + bu → aθ + (bθ )u,

(18)

ϵ : a + bu → a − bu,
√
1
ψ : a + bu → [a + 3a ∗ + 3(b − b∗ )]
4
√
1
+ [b + 3b∗ − 3(a − a ∗ )]u,
4

(19)

(20)

are automorphisms of An . Here ∗ denotes conjugation in
An−1 , and ϵ and ψ, satisfying ϵ 2 = ψ 3 = 1, ϵψ = ψ 2 ϵ,
generate S3 . That is, in general
(21)

It follows that SU (2) × S3 are automorphisms of O, but
crucially, these are not all of the octonion automorphisms:
SU (2)× S3 ⊂ G 2 . However, for the cases where n = 4, 5, 6,
the equality holds [38]
Aut (An−1 ) × S3 = Aut (An ), n = 4, 5, 6.

(22)

In particular, this means that:
Aut (S) = Aut (O) × S3 = G 2 × S3 .

(26)

where a, b ∈ O. The explicit action of ψ on the sedenion
basis elements can be written as:
√
3
1
ψ(ei ) = − ei −
ei+8 ,
(27)
2
2√
3
1
ψ(ei+8 ) = − ei+8 +
(28)
ei ,
2
2
ψ(e8 ) = e8 ,
(29)

where we can see that e18 = e1 e8 = L e1 L e8 , e123458 =
e1 e2 e3 e4 e5 e8 = L e1 L e2 L e3 L e4 L e5 L e8 etc are elements of
Cℓ(8).

Aut (An−1 ) × S3 ⊆ Aut (An ).

√
1
[a + 3a + 3(b − b)]
4
√
1
+ [b + 3b − 3(a − a)]e8 ,
4

where i = 1, . . . , 7. The automorphism ψ corresponds to
simultaneous rotations in the seven ei −ei+8 planes by 2π/3,
and therefore does not correspond to an automorphism of
C ⊗ O. It is also possible to write the S3 automorphisms in
matrix form:
√ )(
)
(
)
(
ei
−1/2 − 3/2
ei
→ √
ψ:
ei+8
ei+8
3/2 −1/2
)
(
)(
)
(
1 0
ei
ei
→
, i = 1, . . . , 7.
ϵ:
ei+8
ei+8
0 −1
The fundamental symmetries of S are the same as those of
O, although one find an additional S3 symmetry, suggesting
a threefold multiplicity of the automorphisms of O.
From the action of θ ′ on the sedenion units above it is
immediately clear that e8 is stabilized by the G 2 automorphisms. Furthermore, these G 2 automorphisms map ei , i < 8
to e j , j < 8, and ei+8 to e j+8 . They therefore do not mix
the new sedenion elements ei+8 with the original octonion
elements ei , i = 1, . . . , 7. Only the S3 automorphism ψ of
order three mixes the original octonion units with the new
sedenion units.
Given that the stabilizer of e4 in G 2 is SU (3), and e8 is
likewise an SU (3) singlet (as it is fixed by G 2 ), it follows
that the SU (3) subgroup of G 2 fixes the entire quaternion
generated by {e0 , e4 , e8 , e4 e8 = e12 }. The S3 automorphisms
on the other hand do not fix this quaternion, although they do
stabilize it. Note that this quaternion corresponds precisely to
the common intersection of our previously isolated octonion
subalgebras Oi .

5 Three generations of color states from C ⊗ S
5.1 Why not sedenions?

(23)

Explicitly, the automorphisms of S are therefore give by
θ ′ : a + be8 → aθ + (bθ )e8 ,

(24)

ϵ : a + be8 → a − be8 ,

(25)

Since one generation of electrocolor states are efficiently represented starting from C ⊗ O, one might ask if S (or rather
C ⊗ S) is an appropriate larger algebraic structure capable
of describing three generations. Not being a division algebra
is not grounds to disqualify S, for we point out that neither

123

## PDF page 8

747 Page 8 of 13

C ⊗ O nor Cℓ(6) generated as the left multiplication algebra
are themselves division algebras. Furthermore, the algebra
R ⊗ C ⊗ H ⊗ O is, like S, not even alternative. In fact, the
construction of invariant subspaces (minimal ideals) relies
explicitly on the use of projectors (and nilpotents), which
altogether do not exist in division algebras.
There are several natural reasons to suspect that S exhibits
the algebraic structure necessary to describe three full generations:
1. Aut (S) = Aut (O) × S3 , and one finds a threefold multiplicity of the symmetries associated with O,
2. The process in Sect. 4 shows how to naturally isolate thee
O subalgebras within S, which could perhaps be used to
construct three generations,
3. The group Spin(8) generated from Cℓ(8) admits a triality, which has on occasion been suggested as a potential
source of three generations [32,44]. The group of outerautomorphisms of Spin(8) is precisely S3 .
One approach to construct three generations with SU (3)C
symmetry is to use each of the three C ⊗ Oi ⊂ S to generate
(via its left action on itself, but not as a left action of C⊗S!) a
Cℓ(6) algebra, and subsequently representing three generations in terms of the minimal left ideals of these three Cℓ(6).
This approach was considered in [34], as a generalization
of the construction three generations of leptons from three
H ⊂ O developed in [36].
There are several drawbacks to this approach however.
Each generation requires its own copy of SU (3) resulting in
three generations of gluons. Finally, the physical interpretation of the S3 automorphisms remains obscured, because
these automorphisms stabilize the (non-principle) octonion
subalgebras in S.
The approach pursued here is different and seeks to resolve
these shortcomings. We instead use each C ⊗ Oi ⊂ S to construct a pair or fermionic ladder operators that each generate
Cℓ(2), via their left multiplication action on all of C ⊗ S
(instead of just C ⊗ Oi ). The three pairs of ladder operators
are independent of one another and hence we identify a single
ˆ
ˆ
copy of Cℓ(6) ∼
⊗Cℓ(2),
corresponding to a
= Cℓ(2)⊗Cℓ(2)
subalgebra of Cℓ(8). Thus, we will employ all three Oi ⊂ S
in order to construct a single generation of states. This corresponds to a direct generalization of the construction reviewed
in Sect. 3 where three H subalgebras of O are used to construct a single generation of color states. Subsequently, the
order three S3 automorphism of S will be used to generate
two additional generations. This construction will therefore
provide a clear interpretation of the new S3 automorphism ψ.
All three generations constructed in this manner transform
as required under a single copy of the gauge group SU (3)C ,
thereby avoiding introducing three generations of gluons.

Eur. Phys. J. C (2023) 83:747

5.2 One generation of electrocolor states from C ⊗ S
We proceed by first constructing a single generation with
unbroken SU (3)C × U (1) symmetry from C ⊗ S. Considering the three octonion subalgebras O1 , O2 , O3 of S defined
above:
O1 : {e0 , e1 , e4 , e5 , e8 , e9 , e12 , e13 },
O2 : {e0 , e2 , e4 , e6 , e8 , e10 , e12 , e14 },
O3 : {e0 , e3 , e4 , e7 , e8 , e11 , e12 , e15 }.
For each Oi subalgebra, we define a single pair of raising
and lowering operators as follows:
1
A†1 ≡ √ (e1 + ie5 + e9 + ie13 ),
2 2
1
A1 ≡ √ (−e1 + ie5 − e9 + ie13 ),
2 2
1
†
A2 ≡ √ (e2 + ie6 + e10 + ie14 ),
2 2
1
A2 ≡ √ (−e2 + ie6 − e10 + ie14 ),
2 2
1
A†3 ≡ √ (e3 + ie7 + e11 + ie15 ),
2 2
1
A3 ≡ √ (−e3 + ie7 − e11 + ie15 ).
2 2

(31)
(32)
(33)
(34)
(35)

It is readily checked that Ai (Ai w) = Ai† (Ai† w) = 0 and
Ai (A j w) = −A j (Ai w), ∀w ∈ C ⊗ S, and therefore these
ladder operators satisfy (as left actions on a general w ∈ S)
the usual anticommutation relations:
{Ai , A j }w = {Ai† , A†j }w = 0,

(36)

{Ai , A†j }w = δi j w, ∀w ∈ C ⊗ S.

(37)

Each Ai ∈ Oi ⊂ S corresponds to a generalization of αi ∈
Hi ⊂ O where now each ladder operators consists of four
terms instead of just two.
Subsequently we can proceed to construct two minimal
left ideals, in a manner identical as in Sect. 3. These ideals
are identical to S u and S d above, and (as will be demonstrated
shortly) preserved by the same unitary symmetries, but with
both the states and symmetry generators written in terms of
the generalised ladder operators Ai and Ai† .
S1u = νe ω1 ω1† + d r A†1 ω1 ω1† + d g A†2 ω1 ω1† + d b A†3 ω1 ω1†
+u r A†3 A†2 ω1 ω1† + u g A†1 A†3 ω1 ω1† + u b A†2 A†1 ω1 ω1†
+e+ A†3 A†2 A†1 ω1 ω1† ,
S1d = ν e ω1† ω1 + d r A1 ω1† ω1 + d g A2 ω1† ω1 + d b A3 ω1† ω1
+u r A3 A2 ω1† ω1 + u g A1 A3 ω1† ω1 + u b A2 A1 ω1† ω1
+e− A3 A2 A1 ω1† ω1 ,
where ω1 := A1 A2 A3 .

123

(30)

## PDF page 9

Eur. Phys. J. C (2023) 83:747

Page 9 of 13 747

The SU (3)C generators are now a direct generalization of
those in Sect. 3, with αi replaced by Ai :
Λ1 = −A†2 A1 − A†1 A2 , Λ2 = i A†2 A1 − i A†1 A2 ,
Λ4 = −A†1 A3 − A†3 A1 ,
Λ3 = A†2 A2 − A†1 A,
Λ5 = −i A†1 A3 + i A†3 A1 , Λ6 = −A†3 A2 − A†2 A3 ,
Λ7 = i A†3 A2 − i A†2 A3 ,
1
Λ8 = − √ (A†1 A1 + A†2 A2 − 2 A†3 A3 )
3
Furthermore, the number generator can again be used to
define a U (1) generator that (together with −Q ∗ ) assigns
the correct electric charges to all the states:
Q=

1
N
= (A†1 A1 + A†2 A2 + A†3 A3 ).
3
3

(38)

5.3 Two additional generations from an S3 automorphism
Having constructed one generation of electrocolor states, we
now proceed to apply ψ to the ladder operators eqns. (30)–
(34), and subsequently the basis states of the minimal left
ideals, in order to generate two additional generations.
The first thing to check is that the S3 automorphisms of S
carry over the automorphisms of the left multiplication algebra Cℓ(8). Given the generating basis e0 , . . . , e8 for Cℓ(8),
it is readily verified that
ψ(ei )ψ(ei ) = ψ(ei2 ) = −1,

(39)

ψ(ei )ψ(e j ) + ψ(e j )ψ(ei ) = 0.

(40)

Subsequently, ψ extends to an automorphism of the entire
Cℓ(8) algebra (see Lemma 9.7 of [45]). A similar argument
holds for the order two S3 automorphism ϵ of S, which likewise extends to an automorphism of Cℓ(8). It can furthermore be checked that:
2
) = −1,
ψ(ei+8 )ψ(ei+8 ) = ψ(ei+8

(41)

ψ(ei+8 )ψ(e j+8 ) = −ψ(e j+8 )ψ(ei+8 ).

(42)

Finally, one also find that

1
Ai = √ (−ei + iei+4 − ei+8 + iei+12 ),
2 2
1
†
Bi = √ (aei + iaei+4 + bei+8 + ibei+12 ),
2 2
1
Bi = √ (−aei + iaei+4 − bei+8 + ibei+12 ),
2 2
1
†
Ci = √ (bei + ibei+4 + aei+8 + iaei+12 ),
2 2
1
Ci = √ (−bei + ibei+4 − aei+8 + iaei+12 ),
2 2

(46)
(47)
(48)
(49)
(50)

where Bi† = ψ(Ai† ), Bi = ψ(Ai ), Ci† = ψ 2 (Ai† ), Ci =
ψ 2 (Ai ) as well as i = 1, 2, 3, and
√
√
− 3−1
3−1
,
b=
,
(51)
a=
2
2
satisfying a 2 + b2 = 2, a + b = −1, ab = −1/2.
The three sets of ladder operators are not linearly independent since
ψ 2 (Ai† ) + ψ(Ai† ) + Ai† = 0.

(52)

The two additional sets of ladder operators {Bi† , Bi } and
†
{C , Ci } generated in this manner likewise constitute Witt

bases for Cℓ(6), satisfying the same anticommutation relations as {Ai† , Ai }, and we proceed to construct an additional
pair of minimal left ideals of Cℓ(6) for each of the two additional sets of ladder operators {Bi , Bi† } and {Ci , Ci† }. We
interpret these additional pairs of minimal ideals as representing the second and third generation of electrocolor states:
S2u = νμ ω2 ω2† + cr B1† ω2 ω2† + c g B2† ω2 ω2† + cb B3† ω2 ω2†
+s r B3† B2† ω2 ω2† + s g B1† B3† ω2 ω2† + s b B2† B1† ω2 ω2†
+μ+ B3† B2† B1† ω2 ω2† ,
S2d = ν μ ω2† ω2 + cr B1 ω2† ω2 + c g B2 ω2† ω2 + cb B3 ω2† ω2
+s r B3 B2 ω2† ω2 + s g B1 B3 ω2† ω2 + s b B2 B1 ω2† ω2
+μ− B3 B2 B1 ω2† ω2 ,
S3u = ντ ω3 ω3† + br C1† ω3 ω3† + b g C2† ω3 ω3† + bb C3† ω3 ω3†

ψ 2 (ei ) + ψ(ei ) + ei = 0,

(43)

+t r C3† C2† ω3 ω3† + t g C1† C3† ω3 ω3† + t b C2† C1† ω3 ω3†

ψ 2 (ei+8 ) + ψ(ei+8 ) + ei+8 = 0,

(44)

+τ + C3† C2† C1† ω3 ω3† ,

indicating that ψ 2 (ei ), ψ(ei ) and ei (as well as ψ 2 (ei+8 ),
ψ(ei+8 ) and ei+8 ) are not linearly independent. These conditions however are not satisfied by more general Cℓ(8) multivectors (nor for e8 , which is fixed by ψ).
Since the action of ψ on e1 , . . . , e15 as elements of Cℓ(8)
is known, we can via linearity establish the action of ψ on the
ladder operators. This gives the three sets of ladder operators:
1
Ai† = √ (ei + iei+4 + ei+8 + iei+12 ),
2 2

(45)

S3d = ν τ ω3† ω3 + br C1 ω3† ω3 + +b g C2 ω3† ω3 + bb C3 ω3† ω3
+t r C3 C2 ω3† ω3 + t g C1 C3 ω3† ω3 + t b C2 C1 ω3† ω3
+τ − C3 C2 C1 ω3† ω3 .
Here, ω2 := B1 B2 B3 , ω3 := C1 C2 C3 .
That is the order three automorphism ψ of the finite group
S3 can be used to construct exactly two additional generations
of color states. This automorphism then permutes between
the three generations.

123

## PDF page 10

747 Page 10 of 13

On the other hand, the order two automorphism ϵ does
not generate transformations between the three generations.
Applying ϵ to the ladder operators Ai and Ai† generates an
complementary set of ladder operators satisfying the same
anticommutation relations as Ai and Ai† (since ϵ is an automorphism of Cℓ(8)), and hence can likewise be used to construct minimal ideals. The automorphism ϵ can then be used
to incorporate an additional degree of freedom (perhaps chirality, handedness, or spin). It is not immediately clear at
present however what the most natural physical interpretation for ϵ is.
5.4 SU (3)C color symmetries of three generations
Although the ladder operators belonging to a fixed generation satisfy the standard fermionic anticommutation relations, ladder operators belonging to different generations do
not. That is
{Ai , B j }w ̸= 0, {Bi , C j }w ̸= 0, {Ci , A j }w ̸= 0,
whenever i ̸= j, and likewise for the remaining anticommutation relations. This is not unexpected, for if all eighteen
ladder operators were to satisfy the standard fermionic anticommutation relations, then we would have a Witt basis for
a Clifford algebra that is much too large to be generated from
C ⊗ S acting on itself. Instead, Eq. (53) simply reflects the
fact that the three sets of ladder operators are not linearly
independent (see Eq. (52)), and subsequently we have three
nontrivial (since e9 , . . . , e15 do not correspond to simple one
vectors), and overlapping Cℓ(6) subalgebras of the full Cℓ(8)
associative left multiplication algebra of C ⊗ S. Indeed it is
readily checked (using Eq. (53)) that
{Ai , B j + C j }w = 0,
{Ai† , (B †j + C †j )}w = 0,
{Ai , (B †j + C †j )}w = −δi j .
To the best of our knowledge, the nonstandard intergeneration anticommutation relations do not imply any physical consequences within the scope of the present construction, although we speculate that the lack of linear independence of the three sets of ladder operators might provide an
algebraic basis for incorporating quark mixing and neutrino
oscillations.
Despite the inter-generation anticommutation relations
being complicated expressions, nonetheless it turns out that
all three generations of ladder states transform correctly
under a single copy of SU (3), which may be generated from
any of the three sets of Cℓ(6) ladder operators. In fact, the
SU (3) generators are invariant under the action of S3 automorphisms, as expected since Aut (S) = G 2 × S3 . We will
here use the SU (3)C generators from Sect. 5.2. One then
finds for example that

123

Eur. Phys. J. C (2023) 83:747

]
[
Λ1 , A1 ω1† ω1 = A2 ω1† ω1 ,
[
]
Λ1 , B1 ω2† ω2 = B2 ω2† ω2 ,
]
[
Λ1 , C1 ω3† ω3 = C2 ω3† ω3 .

(53)
(54)
(55)

A single SU (3) generator thus correctly transforms the
equivalent states of each generation
Λ1 : d r → d g , cr → c g , t r → t g .
The same holds true for the other SU (3) generators and
states. Despite having three generations of fermions, only one
copy of SU (3), and hence one generation of gauge bosons is
needed in the present construction.
On the other hand, one finds that the number operator
Eq. (38) only assigns the correct electric charge for one
of the generations, although two additional number operators could be constructed for the remaining two generations.
This same issue was encountered in [33]. Thus although the
number operator can be used to obtain the correct electric
charge within the context of a single generation model, this
approach fails to work in a three generation model. A generalized action to obtain the correct electric charges is presented
in [35]. This approach, which makes extensive use of both
left and right projectors would work for the present model as
well. However, it remains unclear why this action takes the
particular form that it does, and so this issue will be revisited
at a later time once the weak (or electroweak) symmetry has
been included within the present sedenion model.
5.5 Linear dependence of minimal ideal states
Although we have been able to construct three pairs of minimal ideals to represent three generations of fermions, these
minimal ideals are not linearly independent. Indeed, one
might expect a certain degree of overlap of the minimal ideals, given the condition Eq. (52) above.
We propose (as in [34] and [14]) that the inevitable overlap
of the three generations could form a basis for including quark
mixing and neutrino oscillations into the present algebraic
model based on sedenions. However, a detailed investigation
into the feasibility of this proposal is beyond the scope of
this article, and requires first an understanding of the weak
interaction within the present algebraic context.
Nonetheless, some initial calculations (carried out using
Mathematica) indicate that the (anti) down-type quarks
across generations are linearly dependent. That is:
Ai ω1† ω1 + Bi ω2† ω2 + Ci ω3† ω3 = 0,

(56)

Ai† ω1 ω1† + Bi† ω2 ω2† + Ci† ω3 ω3† = 0,

(57)

where i = 1, 2, 3. On the other hand, all 18 of the (anti) uptype quarks turn out to be linearly independent. This might be
related to the fact that the Yukawa couplings, and subsequent

## PDF page 11

Eur. Phys. J. C (2023) 83:747

mass matrix for either the up-type or down-type quarks can
be taken to be diagonal, but not both. Subsequently, one can
say without loss of generality that only the down-type quarks
mix via the CKM matrix.

6 Outlook
The model presented here is clearly far from complete as our
focus has been restricted to the SU (3)C color gauge symmetry, and we have not considered the remaining internal
symmetries nor the spacetime symmetries.
One way to include chiral SU (2) L states it is via a copy
of Cℓ(4) [46]. In [5] it is shown that the right actions of
C ⊗ H together with the right actions of the Cℓ(6) nilpotents ω and ω† generate the required Cℓ(4) to represent chiral
SU (2) L states in terms of two four-dimensional minimal ideals. The resulting model is then based on Cℓ(10) [6,47,48].
In our present construction, we have restricted ourselves to a
Cℓ(6) subalgebra of the full Cℓ(8) left multiplication algebra. The thus far unused Cℓ(2) could be combined with the
right actions of the nilpotents ωi and ωi† to generate Cℓ(4)
without the need to invoke H. This approach is currently
being investigated by the authors.
It is well known that C ⊗ H ∼
= Cℓ(2) ∼
= S L(2, C). By
complementing the present model sedenion model with a factor of H, it should be possible to include the Lorentz (spacetime) symmetries into the model. Specifically, it was shown
in [5] that Weyl-, Dirac- and Majorana-spinors can all be
represented in terms of the ideals of C ⊗ H ∼
= Cℓ(2). The
spacetime symmetries would then be identical for all three
generations, a desirable feature.
By choosing a complex structure within O, the ten dimensional spacetime described by S L(2, O) is reduced to four
dimensional spacetime S L(2, C) [36,49]. It would be interesting to see whether S L(2, O) spacetime can be extended
to an 18 dimensional spacetime S L(2, S) which is then broken to S L(2, H) via our quaternionic structure inside S, and
subsequently to S L(2, C) by choosing a complex structure
inside H.
The construction of three generations presented here bears
some intriguing resemblance to the three generation construction in [33,35]. In our case, all three generations reside
in a Cℓ(6) subalgebra of Cℓ(8). Likewise in [33], the 48
degrees of freedom that remain in Cℓ(6) once two representations of the Lie algebra su(3) have been accounted for are
shown under the action of SU (3) to transform as three generations of leptons and quarks. The number operator in this
construction no longer assigns the correct electric charges to
the states however, an issue that was overcome in a later paper
[35]. How to include U (1)em into the sedenion model, as well
as a detailed understanding of how these two complementary
constructions are related remains to be worked out.

Page 11 of 13 747

Likewise, it remains to be investigated in detail how the
sedenion model proposed here relates to the constructions of
three generations based on the exceptional Jordan J3 (O), in
which each of the three octonions in J3 (O) is associated with
one generation via the three canonical J2 (O) subalgebras of
J3 (O) [27–32].
Given the richer algebraic structure provided by S, it
may be possible to describe additional features of the SM.
The S3 automorphism of order three not only generates two
additional generations, but also facilitate transformations
between physical states of different generations. This suggests that S3 could perhaps be used as a basis for including
quark mixing and neutrino oscillations. This is something
that has not yet been considered within the context of division
algebras. It is interesting that several authors have proposed
S3 extensions of the SM to explain the hierarchy of quark
masses and mixing in the SM [50–54].

7 Discussion
We have argued that the CD algebra S provides a suitable
algebraic structure to describe three generations. Our focus
has been restricted to the SU (3)C color gauge symmetry.
Three intersecting O subalgebras of S are used to construct a
Witt basis for Cℓ(6). Two minimal left ideals are then use to
represent one generation of electrocolor states. Subsequently,
the S3 automorphism of order three of S is then applied to
the Cℓ(6) Witt basis in order to obtain exactly two additional
generations of color states, but not electrocolor states.
In [4,5], Cℓ(6) arises as the left multiplication algebra
of C ⊗ O. Instead, in our approach Cℓ(6) does not arise
as the multiplication algebra of a single octonion algebras,
but rather from three intersection octonion subalgebras of
the sedenions, with each octonion subalgebra contributing a
Cℓ(2) factor. The model presented here overcomes two limitations of a previous three generation model based on sedenions. First, only a single copy of SU (3)C correctly transforms the states of all three generations. We thereby avoid
introducing three generations of gauge bosons. Additionally
in the present model, the order three S3 automorphisms of S
is given a clear physical interpretation as a family symmetry,
responsible for generating two additional generations from
the first.
One compelling reason to consider division algebras as
the foundational mathematical input from which to generate
SM particle multiplets and gauge symmetries, is that there
are only four of them. Since the CD process generates an
infinite series of algebras, one might question whether going
beyond the division algebras and including S is a wise idea,
or if it opens the door to considering ever larger algebras.
The derivation algebra for all CD algebras An , n ≥ 3 is
equal to g2 however [37]. Furthermore, at least for the cases

123

## PDF page 12

747 Page 12 of 13

Eur. Phys. J. C (2023) 83:747

n = 4, 5, 6, the automorphism group of each successive CD
algebra only picks up additional factors of S3 [38]. It therefore
seems unlikely that CD algebras beyond A4 = S will provide
additional physical insight. As an interesting aside, the sphere
S 15 , associated with the imaginary (pure) sedenions, is the
largest sphere to appear in any of the four Hopf fibrations.
Acknowledgements The authors wish to thank Alessio Marrani for
insightful discussions and detailed feedback on an earlier draft of this
work.
Data Availability Statement This manuscript has no associated data or
the data will not be deposited. [Authors’ comment: This is a theoretical
study and there is no additional data to be deposited.]
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation,
distribution and reproduction in any medium or format, as long as you
give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes
were made. The images or other third party material in this article
are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit http://creativecomm
ons.org/licenses/by/4.0/.
Funded by SCOAP3 . SCOAP3 supports the goals of the International
Year of Basic Sciences for Sustainable Development.

Appendix A: Sedenion multiplication table
The multiplication table for the Cayley–Dickson sedenions
in terms of the indices (i ≡ ei ) (Table 1).

References
1. M. Günaydin, F. Gürsey, Quark structure and octonions. J. Math.
Phys. 14(11), 1651–1667 (1973)
2. G. Dixon, Derivation of the standard model. Il Nuovo Cimento B
(1971–1996) 105(3), 349–364 (1990)
3. G. Dixon, Division algebras: family replication. J. Math. Phys.
45(10), 3878–3882 (2004)
4. G.M. Dixon, Division Algebras: Octonions Quaternions Complex
Numbers and the Algebraic Design of Physics, vol. 290 (Springer
Science & Business Media, Berlin, 2013)
5. C. Furey, Standard model physics from an algebra? arXiv preprint
arXiv:1611.09182 (2016)
6. C. Furey, SU (3)C × SU (2) L × U (1)Y (×U (1) X ) as a symmetry
of division algebraic ladder operators. Eur. Phys. J. C 78(5), 1–12
(2018)
7. N.G. Gresnigt, Braids, normed division algebras, and standard
model symmetries. Phys. Lett. B 783, 212–221 (2018)
8. N.G. Gresnigt, Braided fermions from Hurwitz algebras. In: Journal of Physics: Conference Series, vol. 1194, p. 012040. IOP Publishing (2019)
9. N.G. Gresnigt, A topological model of composite preons from the
minimal ideals of two Clifford algebras. Phys. Lett. B 808, 135687
(2020)
10. N.G. Gresnigt, Topological preons from algebraic spinors. Eur.
Phys. J. C 81(6), 1–7 (2021)
11. N. Gresnigt, A. Marcianò, E. Zappala, Braided matter interactions
in quantum gravity via one-handle attachment. Phys. Rev. D 104(8),
086021 (2021)
12. C.A. Manogue, T. Dray. Octonions, E 6 , and particle physics. In:
Journal of Physics: Conference Series, vol. 254, p. 012005. IOP
Publishing (2010)
13. R.A. Wilson, T. Dray, C.A. Manogue, An octonionic construction of E 8 and the lie algebra magic square. arXiv preprint
arXiv:2204.04996 (2022)
14. C.A. Manogue, T. Dray, R.A. Wilson, Octions: an E 8 description
of the standard model. J. Math. Phys. 63(8), 081703 (2022)

Table 1 Sedenion multiplication table, generated from e1 , e2 , e4 and e8 corresponding to the new C, H, O and S imaginary units respectively
0

1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

0

0

1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

1

1

−0

3

−2

5

−4

−7

6

9

−8

− 11

10

− 13

12

15

− 14

2

2

−3

−0

1

6

7

−4

−5

10

11

−8

−9

− 14

− 15

12

13

3

3

2

−1

−0

7

−6

5

−4

11

− 10

9

−8

− 15

14

− 13

12

4

4

−5

−6

−7

−0

1

2

3

12

13

14

15

−8

−9

− 10

− 11

5

5

4

−7

6

−1

−0

−3

2

13

− 12

15

− 14

9

−8

11

− 10

6

6

7

4

−5

−2

3

−0

−1

14

− 15

− 12

13

10

− 11

−8

9

7

7

−6

5

4

−3

−2

1

−0

15

14

− 13

− 12

11

10

−9

−8

8

8

−9

− 10

− 11

− 12

− 13

− 14

− 15

−0

1

2

3

4

5

6

7

9

9

8

− 11

10

− 13

12

15

− 14

−1

−0

−3

2

−5

4

7

−6

10

10

11

8

−9

− 14

− 15

12

13

−2

3

−0

−1

−6

−7

4

5
4

11

11

− 10

9

8

− 15

14

− 13

12

−3

−2

1

−0

−7

6

−5

12

12

13

14

15

8

−9

− 10

− 11

−4

5

6

7

−0

−1

−2

−3

13

13

− 12

15

− 14

9

8

11

− 10

−5

−4

7

−6

1

−0

3

−2

14

14

− 15

− 12

13

10

− 11

8

9

−6

−7

−4

5

2

−3

−0

1

15

15

14

− 13

− 12

11

10

−9

8

−7

6

−5

−4

3

2

−1

−0

123

## PDF page 13

Eur. Phys. J. C (2023) 83:747
15. R.A. Wilson, Chirality in an E 8 model of elementary particles.
arXiv preprint arXiv:2210.06029 (2022)
16. S. Raj, T.P. Singh, A lagrangian with E 8 × E 8 symmetry for the
standard model and pre-gravitation. I.–the bosonic Lagrangian, and
a theoretical derivation of the weak mixing angle. arXiv preprint
arXiv:2208.09811 (2022)
17. P. Kaushik, V. Vaibhav, T.P. Singh, An E 8 × E 8 unification of the
standard model with pre-gravitation, on an octonion-valued twistor
space. arXiv preprint arXiv:2206.06911 (2022)
18. G. Trayling, A geometric approach to the standard model. arXiv
preprint arXiv:hep-th/9912231 (1999)
19. G. Trayling, W.E. Baylis, A geometric basis for the standard-model
gauge group. J. Phys. A Math. Gen. 34(15), 3309 (2001)
20. G. Trayling, W.E. Baylis, The Cℓ(7) approach to the standard
model, in Clifford Algebras. (Springer, Berlin, 2004), pp.547–558
21. O.C. Stoica, The standard model algebra. Adv. Appl. Clifford Algebras 28(52), 2017 (2018)
22. O.C. Stoica, Chiral asymmetry in the weak interaction via Clifford
Algebras. arXiv preprint arXiv:2005.08855 (2020)
23. I. Todorov, Octonionic Clifford algebra for the internal space of
the standard model. https://preprints.ihes.fr/2022/P/P-22-01.pdf
(2022)
24. C.C. Perelman, R ⊗ C ⊗ H ⊗ O-Valued gravity as a grand unified
field theory. Adv. Appl. Clifford Algebras 29(1), 1–20 (2019)
25. C.C. Perelman, On C ⊗ H ⊗ O-valued gravity, sedenions, hermitian matrix geometry and nonsymmetric Kaluza–Klein theory.
Adv. Appl. Clifford Algebras 29(3), 1–16 (2019)
26. M. Pavšič, Geometric spinors, generalized Dirac equation and mirror particles. arXiv preprint arXiv:1310.6566 (2013)
27. M. Dubois-Violette, Exceptional quantum geometry and particle
physics. Nucl. Phys. B 912, 426–449 (2016)
28. M. Dubois-Violette, I. Todorov, Exceptional quantum geometry
and particle physics II. Nucl. Phys. B 938, 751–761 (2019)
29. I. Todorov, S. Drenska, Octonions, exceptional Jordan algebra and
the role of the group F4 in particle physics. Adv. Appl. Clifford
Algebras 28(4), 1–36 (2018)
30. I. Todorov, M. Dubois-Violette, Deducing the symmetry of the
standard model from the automorphism and structure groups of the
exceptional jordan algebra. Int. J. Mod. Phys. A 33(20), 1850118
(2018)
31. L. Boyle, S. Farnsworth, The standard model, the Pati–Salam
model, and ‘Jordan geometry’. New J. Phys. 22(7), 073023 (2020)
32. L. Boyle, The standard model, the exceptional Jordan algebra, and
triality. arXiv preprint arXiv:2006.16265 (2020)
33. C. Furey, Generations: three prints, in colour. J. High Energy Phys.
2014(10), 1–11 (2014)
34. A.B. Gillard, N.G. Gresnigt, Three fermion generations with two
unbroken gauge symmetries from the complex sedenions. Eur.
Phys. J. C 79(5), 1–11 (2019)
35. C. Furey, Three generations, two unbroken gauge symmetries, and
one eight-dimensional algebra. Phys. Lett. B 785, 84–89 (2018)

Page 13 of 13 747
36. C.A. Manogue, T. Dray, Dimensional reduction. Mod. Phys. Lett.
A 14(02), 99–103 (1999)
37. R.D. Schafer, On the algebras formed by the Cayley–Dickson process. Am. J. Math. 76(2), 435–446 (1954)
38. R. Brown, On generalized Cayley–Dickson algebras. Pac. J. Math.
20(3), 415–422 (1967)
39. A. Hurwitz, Ueber die Composition der quadratischen Formen
von belibig vielen Variablen. Nachrichten von der Gesellschaft der
Wissenschaften zu Göttingen, Mathematisch-Physikalische Klasse
309–316, 1898 (1898)
40. J. Lohmus, E. Paal, L. Sorgsepp, Nonassociative algebras in
physics (Hadronic Press, Palm Harbor, 1994)
41. R. Abłamowicz, Construction of spinors via Witt decomposition
and primitive idempotents: a review. In: Clifford Algebras and
Spinor Structures: A Special Volume Dedicated to the Memory
of Albert Crumeyrolle 1919–1992, pp. 113–123 (1995)
42. R. Cawagas, On the structure and zero divisors of the Cayley–
Dickson sedenion algebra. Discussiones Mathematicae-General
Algebra and Applications 24(2), 251–265 (2004)
43. R. Guillermo Moreno, The zero divisors of the Cayley–Dickson
algebras over the real numbers. arXiv preprint arXiv:q-alg/9710013
(1997)
44. N. Masi, An exceptional G(2) extension of the standard model from
the correspondence with Cayley–Dickson algebras automorphism
groups. Sci. Rep. 11(1), 1–18 (2021)
45. F.R. Harvey, Spinors and Calibrations, vol. 8 (Elsevier, Amsterdam, 1990)
46. C. Furey, A demonstration that electroweak theory can violate
parity automatically (leptonic case). Int. J. Mod. Phys. A 33(04),
1830005 (2018)
47. N.G. Gresnigt, The standard model particle content with complete
gauge symmetries from the minimal ideals of two Clifford algebras.
Eur. Phys. J. C 80(6), 1–7 (2020)
48. I. Todorov, Octonion internal space algebra for the standard model.
Universe 9(5), 222 (2023)
49. T. Dray, C.A. Manogue, The Geometry of the Octonions (World
Scientific, Singapore, 2015)
50. J. Kubo, A. Mondragón, M. Mondragón, E. Rodríguez-Jáuregui,
The flavor symmetry. Prog. Theor. Phys. 109(5), 795–807 (2003)
51. J. Kubo, H. Okada, F. Sakamaki, Higgs potential in a minimal
S3 invariant extension of the standard model. Phys. Rev. D 70(3),
036007 (2004)
52. J. Kubo, Majorana phase in minimal S3 invariant extension of the
standard model. Phys. Lett. B 578(1–2), 156–164 (2004)
53. J. Kubo, A. Mondragon, M. Mondragon, E. Rodriguez-Jauregui,
O. Felix-Beltran, E. Peinado, A minimal S3 -invariant extension
of the standard model. In: Journal of Physics: Conference Series,
vol. 18, p. 380. IOP Publishing (2005)
54. A. Mondragon, M. Mondragon, E. Peinado, Lepton masses, mixings, and flavor-changing neutral currents in a minimal S3 -invariant
extension of the standard model. Phys. Rev. D 76(7), 076003 (2007)

123
