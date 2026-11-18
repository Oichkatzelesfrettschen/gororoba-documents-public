Source: https://doi.org/10.1038/s41598-021-01814-1
PDF sha256: 27a962a7788709347522c6a5a3882fbce3b3a02e607f6b547efc24dfc0cafb91
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of g2_extension_sm_cd_2021_nature_srep.pdf

Transcription of `g2_extension_sm_cd_2021_nature_srep.pdf` in this directory, 18 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-18 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

www.nature.com/scientificreports

OPEN

An exceptional G(2) extension
of the Standard Model
from the correspondence
with Cayley–Dickson algebras
automorphism groups
Nicolò Masi
In this article I propose a new criterion to extend the Standard Model of particle physics from a
straightforward algebraic conjecture: the symmetries of physical microscopic forces originate from
the automorphism groups of main Cayley–Dickson algebras, from complex numbers to octonions
and sedenions. This correspondence leads to a natural enlargement of the Standard Model color
sector, from a SU(3) gauge group to an exceptional Higgs-broken G(2) group, following the octonionic
automorphism relation guideline. In this picture, an additional ensemble of massive G(2)-gluons
emerges, which is separated from the particle dynamics of the Standard Model.
Despite its great success and prediction capability, the Standard Model (SM) of particle physics is afflicted
by internal and external problems, i.e. theoretical issues (such as hierarchy and strong CP problems) and not
explained phenomena, like dark matter (DM), dark energy or matter–antimatter ­asymmetry1. Above all, DM is
probably the most compelling and very long-standing problem of modern physics, with no evident nor univocal
solution: all the efforts made, from particle ­theory2,3 to modified ­gravities4–6, have not been successful in clarifying
its nature. The most convincing particle candidates, the weakly interacting massive particles (WIMPS), have not
been discovered yet: direct, indirect and collider searches show no evidence of new particles approximately up
to the 1 TeV ­scale3,7–10. This is a strong hint that the Naturalness ­criterion11 for the Higgs sector and the so-called
WIMP Miracle12, which postulate the existence of a thermal particle relic of the Big Bang at the electroweak scale
O(100GeV) which interacts via weak force, could not be a prerogative of Nature or, at any rate, not sufficient
to individuate the origin of dark matter and describe the physics beyond Standard Model. Even the possibility
that the weak interaction between DM and SM particles is disfavored must be considered: new particles could
hide at different energy scales and they could be not capable of interacting with the visible world, at least at the
experimentally explored energies.
Therefore, to proceed in the investigation of beyond Standard Model phenomenology, one has to fill up the
lack of a theoretical guideline and integrate some new simplicity criteria to select reliable candidates and explain
the complex astrophysical and cosmological ­observations13–15. Today physics seems to need some extra inputs to
go beyond current paradigms and reach a deepest understanding of the dark matter conundrum: in this complex
situation mathematics could provide fresh insights and conjectures to overcome physical prejudices.
Here we propose an approach based on a division algebras conjecture capable of selecting a unique extension
of the SM, which introduces a branch of exceptional matter particles from a simple and minimally high symmetry.
The criterion is to identify fundamental interactions with the automorphism groups of Cayley-Dickson algebras
(an automorphism is a bijective way of mapping a mathematical object to itself preserving its structure: the set
of all automorphisms forms the automorphism group, i.e. the symmetry group of the object). Then, from the
automorphism of octonions (and sedenions) algebra, the promising exceptional symmetry group G(2) can be pinpointed to solve the DM problem. We will demonstrate that, once broken through a Higgs-like mechanism, G(2)
represents the optimal gauge group to describe strong interaction and dark matter at the same time, shedding
light on a primordial high energy phase transition which generated the strong sector. This minimal extension of
the SM, via Cayley–Dickson algebras automorphism correspondence, uniquely fix the content of particle physics.
To the best of our knowledge, no existing work in literature is devoted to an exceptional G(2) enlargement of
the strong sector nor to the possibility that dark matter is formed by massive gluons from a broken-G(2) gauge
Physics Department, INFN & Bologna University, Via Irnerio 46, 40136 Bologna, Italy. email: masin@bo.infn.it

Scientific Reports |

(2021) 11:22528

| https://doi.org/10.1038/s41598-021-01814-1

1
Vol.:(0123456789)

## PDF page 2

www.nature.com/scientificreports/
group, which naturally incorporates the standard SU(3) color Quantum Chromodynamics (QCD): even if G(2)
lattice models have been largely applied to simplify standard QCD ­computations16,17, the implications of such an
extension of the SM have not been explored. Hence, the present dissertation is not intended as a mere review of
the current status of Cayley–Dickson algebras applied to particle physics, but as a phenomenological proposal
to build up an exceptional Standard Model framework and incorporate new particle physics.

Fundamental forces from division algebras automorphisms

In the last decades many attempts to connect the Standard Model of elementary particles with division algebras
have been made, showing it is worthwhile establishing relations between algebraic structures and symmetry
­groups18–26.
It is well-known that following the Cayley–Dickson construction ­process18,20, one can build up a sequence
of larger and larger algebras, adding new imaginary units. In detail, from Hurwitz and Zorn ­theorem19, one can
identify the so-called division algebras ℝ, ℂ, ℍ, 𝕆, i.e. the only four alternative algebraic fields with no non-trivial
zero ­divisors20,27, which are real numbers, complex numbers, quaternions and octonions, respectively. During the
construction process, the algebras lose some peculiar properties, one at a time. For example, complex numbers
are not ordered but commutative, quaternions are not commutative but associative, whereas octonions lose all
the familiar commutative and associative properties, but they are still an alternative ­algebra27. The process does
not terminate with octonions: applying the Cayley–Dickson construction, greater 2 -dimensional algebras can
be constructed, for any positive integer n. For n > 3, however, as anticipated, they all include non-trivial zero
divisors, i.e. they have problems in a general definition of norm (in abstract algebra, a non-zero element a of a
ring R is called a zero divisor if there exists a non-zero x such that ax = 0; for general properties of zero divisors
­see28). This was considered an obstacle for the use of these extended algebras, such as n = 4 sedenions, in science.
But, as shown ­in29,30, sedenions should not be ruled out as playing a role in particle physics on the basis that they
do not constitute a division algebra. We will return to this topic later.
The link between unitary groups and division algebras 𝔸n has been diffusely ­studied31–33. Unitary groups are
the fundamental bricks to build the particle Standard Model, because each fundamental force can be described
by a unitary or special unitary ­group1,34–37, being G = SU(3) × SU(2) × U(1) the SM group of strong SU(3),
weak SU(2) and hypercharge U(1) ­interactions1. Besides its symmetry, the SM includes three fermions families:
between these three generations, particles differ by their flavour quantum number and mass, but their interactions are identical.
In the following, we want to briefly highlight the relations between the automorphisms of Cayley-Dickson
algebras and these important physical gauge groups, including some considerations about the tripartite structure
of the Standard Model.
Starting from the most simple complex algebra and SM symmetry group, it is easy to find a direct connection
between the electromagnetism (or Quantum Electrodynamics) U(1) formalism and the complex number field
ℂ: in fact the group U(1), the smallest compact real Lie group, corresponds to the circle group S1, consisting
of all complex numbers with absolute value 1 under multiplication, which is isomorphic to the SO(2) group of
­rotation38. All the unitary groups contain copies of this fundamental group. For n ≥ 1, one can also consider for
the comparison the n-torus Tn, that is defined to be ℝn ∕ℤn ≅ U(n) ≅ SO(2)n ≅ (S1 )n, where / denotes the quotient group between reals and integers, which shows off the deep connection between U(1) gauge symmetry and
other representations strictly connected to complex ­numbers38,39. It is also true that the n × n complex matrices
which leave the scalar product ⟨, ⟩ invariant form the group U(n) = Aut(ℂn , ⟨, ⟩), i.e. the group of automorphisms
of ℂn as a Hilbert ­space40.
These links are not surprising because, from a mathematical point of view, the existence of infinite distinct
wild automorphisms of the complex numbers, beyond identity and complex conjugation, is well-known21,41.
We find another noteworthy examination i­n39, where the unitary group U(1) is showed as defining binary
complex relations ℂ × ℂ, i.e. the U(1) numbers effectively operate as automorphisms of ℂ via multiplication of
a phase factor. As we know, the complex numbers can be expressed in polar coordinates and this implies that
the general linear multiplicative group ℂ∗ = ℂ�0 = eℂ ≅ GL(1, ℂ) is uniquely decomposable (ez = ex ⋅ eiy ) into
the totally ordered group with real exponential |ℂ∗ | = eℝ and into the phase group with imaginary exponentials
ℂ∗ ∕|ℂ∗ | = eiℝ ≅ U(1), which is approximately U(1) ­(see39,42 for details). This is another way to underline the
intimate connection between the unitary group and the complex numbers. Furthermore, from a physical point
of view, one can also think at the Riemann-Silberstein field reformulation of the ­electromagnetism43 in terms of
a complex vector that combines the electric field E, as the real part, and the magnetic field B, as the imaginary
part, in order to put in evidence this essential relation.
Even SU(2) weak isospin can be clearly represented with the algebraic quaternionic basis, i.e. Pauli matrices23: SU(2) naturally embeds into ℍ as the group of quaternion elements of norm 1, with a perfect analogy with
respect to U(1) and complex numbers. More precisely, the group SU(2) is isomorphic to the group of quaternions of norm 1, and it is thus diffeomorphic to the 3-sphere S3 (a diffeomorphism is an isomorphism of smooth
manifolds, i.e. a map between manifolds which is differentiable and has a differentiable inverse). Indeed, since
unit quaternions can be used to represent rotations in 3-dimensional space (up to a sign), there is a surjective
homomorphism from SU(2) to the rotation group SO(3)23 (an homomorphism is a structure-preserving map
between two algebraic structures of the same type): one can show that the local SU(2) spinors are exactly the same
two-component spinors derived from the local quaternion matrix representation, i.e. the three Pauli matrices
along with the identity matrix I (spinors are defined as vectors of a representation of the group of automorphisms
of a Clifford algebra defined on space–time). In other words, the correspondence between the automorphism
of quaternion algebra and the Standard Model symmetry group of weak force can be clearly shown: for quaternions Aut(ℍ) = SO(3), where SO(3) is homomorphic to SU(2) in turn, and the universal cover of SO(3) is

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

2

## PDF page 3

www.nature.com/scientificreports/
the spin group Spin(3), which is isomorphic to SU(2). So SU(2) and SO(3) algebraic structures are equivalent.
An interesting demonstration of the correspondence between the two groups using M ö bius transformation is
described ­in44. The quaternionic representation of (electro-) weak isospin has been used by many ­authors45,46.
Hence, both in the U(1) electromagnetic case and in the SU(2) weak interaction, the solutions can be
expressed in terms of division algebras, respectively the complex and the quaternion algebras: the division
property is important to define the mathematical structure and in the determination of solutions. This could
be a coincidence, but the possibility that fundamental gauge interactions can be described by the apparatus of
division algebras should be explored.
It seems logical to revise the next division algebra, the octonion algebra 𝕆 (which is not a Clifford algebra,
unlike ℝ, ℂ and ℍ, because non associative)27,47 for a possible description of the SU(3) gauge ­field45,48, but the
result is less clear than in quaternion case for the SU(2) gauge field. The interesting fact to be considered is that
the group of automorphisms of the octonion algebra, the largest of the normed division algebras, corresponds to
the exceptional Lie algebra G(2), the smallest among the known exceptional Lie algebras: Aut(𝕆) = G(2)49. So it
is noteworthy to point out that the Standard Model gauge group SU(3) is not isomorphic to the group of automorphisms of the octonions, which is G(2). Nonetheless, it is possible to fix one of the octonion basis elements
to obtain seven possible subalgebras, each of which has a subgroup of automorphisms isomorphic to SU(3). For
example, SU(3) itself may be defined as the subgroup of G(2) which leaves the octonionic unit e 7 ­invariant23. Of
course, alternative SU(3) subgroups of G(2) may be found, corresponding to other imaginary units. In addition,
recent works in the framework of particle physics show the possibility to rewrite Gell-Mann matrices of SU(3)
strong force (the group generators) with ­octonions45. Also split-octonions representations have been proposed
as alternative formalism for SU(3) color gauge ­symmetry48.
But here a crucial difference appears: it must be noted that for ℂ and ℍ the direct automorphism groups contain an equal, or comparable, amount of “mathematical information” than U(1) and SU(2) themselves (through
the approximate algebraic correspondences, via homomorphism in SU(2) case), whereas the exceptional G(2)
group is certainly bigger than SM SU(3), as it includes SU(3) and is equipped with six additional ­generators50.
In other words, if we want to study the application of the octonion automorphism in physics, it is mandatory to
invoke a gauge group which is not the strong color symmetry SU(3).
Summarizing, for non real division algebras it turns out that:

Aut(ℂ) ≅ U(1), Aut(ℍ) ≅ SU(2), Aut(𝕆) ≡ G(2).

(1)

These relations show an ordered correspondence between (approximate) automorphisms of algebras and
gauge groups useful for Standard Model description, where G(2) contains SU(3) color force. We will see in the
next section that, besides SU(2) Pauli matrices, also G(2) generators can be written in terms of SU(3) Gell-Mann
matrices as 14 unitary matrices.
Fundamental correlations between division algebras and symmetry groups, as anticipated, have been
already stressed in the last decades. Using division algebras, Dixon proposed an elegant representation
of particle physics ­in20. Furey has recently suggested the appealing possibility to reformulate the SM group
G = SU(3) × SU(2) × U(1) in terms of a 𝔸 = ℝ ⊗ ℂ ⊗ ℍ ⊗ 𝕆 tensor product algebra, restarting from Dixon’s work, using the concept of Ideals, i.e. using subspaces of proper Clifford Algebras as “particles” ­(see24,51–54
for details). Also string theory and supersymmetrical theories invoked division algebra to study particle
­interactions32,55–59. Moreover, G(2) as automorphism of 𝕆 has important applications in terms of the so-called
G2 structure or G2 ­manifolds60, in the context of M-theory61.
Indeed, one solid reason for studying division algebras in relation to particle symmetries is that, unlike Lie
algebras and Clifford ­algebras21, there is a finite number of division algebras and corresponding automorphisms
(see again the extensive works of ­Dixon20). If we start with a division algebra, the physical symmetries are dictated
by the mathematical structure and the choice of a proper symmetry group is constrained.
To proceed with the reasoning, we are going to see why 16-dimensional sedenions can be easily added to this
picture and how dark matter description can benefits from this algebraic facts, summarizing the main features
of sedenions algebra.
The sedenion algebra is the fifth Cayley-Dickson algebra 𝔸4 = 𝕊, where 𝔸0,1,2,3 correspond to reals, complex
numbers, quaternions and octonions. This is not a division algebra, it is non-commutative, non-associative,
and non-alternative (an algebra A is alternative if the subalgebra generated by any two elements is associative,
i.e. iff for all a, b ∈ A we have (aa)b = a(ab), (ba)a = b(aa)62), hence it cannot be a composition ­algebra29,63
(where a composition algebra is an algebra A over a field K with a non-degenerate quadratic form N, called
norm, that satifies N(ab) = N(a)N(b) for all a, b in A19). However sedenion algebra is power-associative and
flexible (an algebra is power-associative if the subalgebra generated by any one element is associative: it is a sort
of lowest level of ­associativity27; the flexible property, for any a, b ∈ A, can be defined as a(ba) = (ab)a ), and
satisfies the weak inversive properties for non-zero elements. Each Cayley-Dickson algebra satisfies the weak
inversive property: a−1 (ab) = a(a−1 b), (ba−1 )a = (ba)a−1 , a−1 (ab) = (ba)a−1—see30,62 for details. In principle,
the Cayley-Dickson construction can be indefinitely carried on and, at each step, a new power-associative and
flexible algebra is produced, doubling in size. So, in first approximation, no new fundamental properties and
information are added nor lost enlarging the algebra beyond sedenions. One can choose a canonical basis for 𝕊
to be E16 = {ei ∈ S|i = 0, 1, . . . , 15} where e0 is the real unit and e1 , … , e15 are anticommuting imaginary units.
In this basis, a general element A ∈ 𝕊 is written as

A=

15
∑
i=0

Scientific Reports |

(2021) 11:22528 |

ai ei = a0 +

15
∑

ai ei ,

ai ∈ ℝ.

(2)

i=1

https://doi.org/10.1038/s41598-021-01814-1

3
Vol.:(0123456789)

## PDF page 4

www.nature.com/scientificreports/
The basis elements satisfy the multiplication rules

e0 = 1,

ei2 = −e0 ,

ei ej = γijk ek

e0 ei = ei e0 = ei ,
i �= 0,
i �= 0,

(3)

i �= j,

with 𝛾ijk the real structure constants, which are completely antisymmetric. For two sedenions A, B, one has
)
)( 15
( 15
15
15
∑
∑
∑
∑
ai bj (ei ej ) =
fij 𝛾ijk ek ,
bj ei =
AB =
ai ei
(4)
i=0

i=0

i,j=0

i,j,k=0

where fij ≡ ai bj.
Because the sedenion algebra is not a division algebra, it contains zero divisors: for 𝕊 these are elements of
the form

(ea + eb )◦(ec + eb ) = 0,

ea , eb , ec , ed ∈ 𝕊.

(5)

There are 84 such zero divisors in sedenion space and the subspace of zero divisors with unit norm is homeomorphic to G(2)28,64. To understand the role and emergency of zero divisors, one has to consider not only single
algebras but also compositions of them. For example, whereas ℝ, ℂ, ℍ and 𝕆 are by themselves division algebras,
their tensor products, such as ℂ ⊗ ℍ, ℂ ⊗ 𝕆 and ℝ ⊗ ℂ ⊗ ℍ ⊗ 𝕆, largely applied in SM algebraic extensions, are
not, and in fact the zero divisors of these algebras play a crucial role in the construction of Furey’s ­Ideals24,51–53.
Moreover, the two by two compositions of division algebras, which are not division algebras and contain zero
divisors, are the subjects of the well-known Freudenthal–Tits magic square65–67:
⊗

ℝ

ℂ

ℍ

𝕆

ℝ

SO(3)

SU(3)

Sp(3)

F4

ℂ

SU(3)

SU(3)2

SU(6)

E6

ℍ

Sp(3)

SU(6)

SO(12)

E7

𝕆

F4

E6

E7

E8

This is a symmetric square (SO(N) and SU(N) are the usual special orthogonal and unitary groups of order
N, Sp(3) is the symplectic group of order three), which exhibits the “unexpected” relation between octonions
products and exceptional groups ( F4 , E6, E7 , E8)49, except for the exceptional G(2) which represents octonions
automorphism itself. The exceptional groups on the last line/row are not exactly automorphisms of the octonions products, because of mathematical problems in the definition of projective planes, due to the appearance
of zero divisors: they are called bioctonions (ℂ ⊗ 𝕆), quateroctonions (ℍ ⊗ 𝕆) and octooctonions (𝕆 ⊗ 𝕆)
and find correspondence into Jordan’s ­algebras27. Exceptional Ei are also largely used in supergravity and string
­theory35,57. Therefore it seems reasonable to continue the Cayley-Dickson algebraic construction into the nondivision algebras, such as 𝕊.
Interestingly, ­in29,68 the authors put in evidence an important relation between sedenions and the exceptional
group G(2), demonstrated by Brown ­in69:

Aut(𝕊) = Aut(𝕆) × S3 .

(6)

where we know that Aut(𝕆) = G(2) and S3 is the permutation group of degree three. So the inner symmetries of
this non-division algebra can be again extracted from the automorphism group of octonions and, in particular,
from a proper product of the exceptional G(2) group with a symmetric group. The only difference between octonions and sedenions automorphism groups is a factor of the permutation group S3: this permutation group can
be constructed from the triality automorphism of the spin group Spin(8) (triality is a trilinear map among three
vector spaces, most commonly described as a special symmetry between vectors and spinors in 8-dimensional
euclidean space—see21,27 for details). Eq.(6) suggests that the fundamental symmetries of 𝕊 are the same as those
of 𝕆, even if the factor S3 introduces a three copies scenario, that is exactly what we need in order to describe the
observed three generations of fermions in the Standard Model of particles.
The previous formula can be generalized, for an arbitrary algebra constructed via Cayley-Dickson process
(for n > 3), ­into29,70

Aut(𝔸n ) ≅ Aut(𝕆) × (n − 3)S3 .

(7)

This tells us that the underlying symmetry is always G(2), the automorphism group of the octonions. The
higher Cayley-Dickson algebras only add additional trialities, i.e. copies of G(2), and reasonably no new physics
beyond sedenions. Futhermore, sedenion algebra might represent the archetype of all non-associative and nondivision flexible algebras, if n > 3 Cayley-Dickson algebras do not differ from sedenions for what concerns the
multilinear identities (or algebraic properties) content, as suggested ­in71.
In this picture, sedenion algebra could constitute the searched simplicity criterion to select the full symmetry
of a three generations Standard Model strong force and include a new particle physics content, which might represent the unknown dark matter sector. This could be also read as a sort of a naive indirect proof that fundamental
forces should be a small number (only three), because all algebras beyond octonions point towards the very same
exceptional group, adding only copies (particle generations). Finally, as it will be discussed in the next section,
Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

4

## PDF page 5

www.nature.com/scientificreports/

Charge (ng )

Group

Force

Algebra

Dim

Commutative

Associative

Alternative

Normed

Flexible

Q(1)

U(1)

EM

ℂ

2

Yes

Yes

Yes

Yes

Yes

T(3)

SU(2)

Weak

ℍ

4

No

Yes

Yes

Yes

Yes

C(8)

SU(3)

Strong

𝕆 or 𝕊

8/16

No

No

Yes

Yes

Yes

Broken-G(2)

Exceptional
strong

𝕆 or 𝕊

8/16

No

No

No

No

Yes

EC(6)

Table 1.  Schematic correspondence between forces, groups and algebras. In the first column the charge of
the physical interaction is displayed along with the number ng of associated generators (bosons). Q, T, C are
usual SM electric charge, weak isospin and color charge, respectively; here EC stands for “exceptional-colored”,
to indicate the six broken generators which originate the massive exceptional G(2) bosons which have quark
and anti-quark color quantum numbers (see next section). The second and third columns associate gauge
groups and forces, highlighting the link between G(2) and the 6 new exceptional-colored particles, separated
from visible strong phenomena. G(2) algebraic automorphism representation is valid for both octonions and
sedenions (the only difference is the S3 factor). In principle, strong force and exceptional sector represent the
same interaction but they are disconnected, coming from the broken exceptional symmetry. For this reason
their algebras are both displayed as 𝕆 or 𝕊. Algebraic dimensions are showed in the fifth column. As shown
in the subsequent columns, each division algebra loses inner properties hierarchically, from commutativity to
alternativity, as the dimensions increase. All algebras are flexible (and power-associative). ­See27,63 for proper
descriptions of the algebraic properties and insights.

to recover the usual SU(3) strong force the octonions-sedenions automorphism group must be broken at our
energy scales and new physics extracted: this enlarged algebraic content is going to be associated to dark matter.
So, without the presumption of a rigorous and definitive mathematical definition of the problem, we can
reformulate and summarize the algebraic phenomenological conjecture in a general way as follows.
The fundamental symmetry of the Standard Model of particle physics with three fermion families might be
the realization of some tensor products between the associative division algebras and the most comprehensive
non-division algebra obtained through the Cayley–Dickson construction, i.e. the sedenion algebra. The sedenionic description, like the octonionic one, corresponds, via automorphism, to the simplest exceptional group
G(2), but tripled. It could provide an explanation to the N = 3 fermion families of the Standard Model, which lie
in the sedenions S3 automorphism factor, as suggested ­by29. This is consistent with the proposal of a S3-invariant
extension of the Standard Model, as discussed ­in72–75.
The gauge groups U(1), SU(2), SU(3), describing the three fundamental forces, find mathematical correspondence into the division algebras ℂ, ℍ, 𝕆 respectively: Table 1 summarizes this correspondence. However, whereas
U(1) and SU(2) are approximate isomorphisms of complex and quaternion algebras automorphism groups (see
Eq.(1)), the octonion and sedenion automorphism relations point towards a different group, which is manifestly
larger than the usual 8-dimensional SU(3) color group of the Standard Model, i.e. the 14-dimensional G(2) group;
SU(3) and G(2) differ for 6 dimensions/generators. Therefore

Aut(ℂ) × Aut(ℍ) × Aut(𝕊) = Aut(ℂ) × Aut(ℍ) × Aut(𝕆) × S3 = U(1) × SU(2) × G(2) × S3

(8)

could give the overall unbroken Standard Model symmetry. This is the first main statement of the present dissertation. Here the automorphism selection is invoked to predict something beyond current SM, and SU(3) in particular, and it works as a guideline to replace SU(3) color itself with the smallest exceptional group: fundamental
forces must be isomorphic to the automorphisms groups of the division algebras built up through the Cayley–Dickson
construction. Tensor products between the corresponding algebras (see Freudenthal–Tits magic square) could
be effective symmetries but not fundamental forces.
A new particle content come from the aforementioned difference between G(2) and SU(3) groups and lie
in the spectrum gap between them. Following the Cayley–Dickson algebraic automorphism criterion, no more
physics is needed nor predicted, except for the six additional degrees of freedom, i.e. boson fields, which represent
the discrepancy between G(2) and SU(3) generators. Hence, the automorphism selection rule extends the strong
color sector and provides a rich exceptional phenomenology.
A further novelty is the definition of an original algebraic criterion to predict physics beyond the Standard
Model, which substitutes Higgs Naturalness and the Wimp Miracle. In this scenario, the strong force acquires a
more complex structure, which includes the usual color sector and an enlarged strong exceptional dynamics, due
to six residual generators of exceptional G(2), which might gain mass via a symmetry breaking: to recover standard SU(3) color strong force description, the new G(2) color sector should be broken by a Higgs-like mechanism
and separated into two parts, one visible and the other excluded from the dynamics due to its peculiar properties.
The next section is devoted to a deep analysis of the exceptional G(2) group and to the emergency of these
massive exceptional bosons.

A G(2) gauge theory for the strong sector

G(2) can be described as the automorphism group of the octonion algebra or, equivalently, as the subgroup of the special orthogonal group SO(7) that preserves any chosen particular vector in its 8-dimensional real spinor ­representation21,47,76. The group G(2) is the simplest among the exceptional Lie ­groups31;
it is well known that the compact simple Lie groups are completely described by the following classes:

Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

5
Vol.:(0123456789)

## PDF page 6

www.nature.com/scientificreports/
AN (= SU(N + 1)), BN (= SO(N + 1)), CN (= Sp(N)), DN (= SO(2N)) and exceptional groups G2 , F4 , E6 , E7 , E8, with
N = 1, 2, 3, . . .(for DN , N > 2)77. Among them, only SU(2), SU(3), SO(4) and symplectic Sp(1) have 3-dimensional
irreducible representations and only one, SU(3), has a complex triplet representation (this was one of the historical criteria to associate SU(3) to the three color strong force, with quark states different from antiquarks ­states78).
There is only one non-Abelian simple compact Lie algebra of rank 1, i.e. the one of SO(3) ≃ SU(2) = Sp(1), which
describes the weak force, whereas there are four of rank 2, which generate the groups G(2), SO(5) ≃ Sp(2), SU(3)
and SO(4) ≃ SU(2) ⊗ SU(2), with 14, 10, 8 and 6 generators, ­respectively50.
If we want to enlarge the QCD sector to include dark matter, it is straightforward we have to choose G(2)
or SO(5). The group G(2), beside its clear relation with division algebras described in the previous section,
is of particular interest because it has a trivial center, the identity, and it is its own universal covering group,
meanwhile SO(5) has ℤ2 as a center (and SU(3) has ℤ3); SO(N) in general are not simply connected and their
universal covering groups for n > 2 are spin Spin(N)79. It is also well-know in literature that G(2), thanks to its
aforementioned peculiarities, can be used to mimic QCD in lattice simulations, avoiding the so-called sign
­problem80 which afflicts SU(3). Proposing to enlarge QCD above the TeV scale and have the SM as a low energy
theory is surely not an unprecedented nor odd idea: for example, modern composite Higgs ­theories81–83 try to
introduce (cosets) gauge groups beyond SU(3), such as SU(6)/SO(6), SO(7)/SO(6) or SO(5)/SO(4), dealing with
multiple Higgs, strong composite states and dark matter candidates.
Focusing on the present proposal, G(2) can be constructed as a subgroup of SO(7), which has rank 3 and 21
­generators50,79. The 7 × 7 real matrices U of the group SO(7) have determinant 1, orthogonal relation UU † = 1
and fulfill the constraint Uab Uac = 𝛿bc . The G(2) subgroup is described by the matrices that also satisfy the cubic
constraint
(9)

Tabc = Tdef Uda Ueb Ufc

where T is an anti-symmetric tensor defining the octonions multiplication rules, whose non-zero elements are

T127 = T154 = T163 = T235 = T264 = T374 = T576 = 1.

(10)

To explicitly construct the matrices in the fundamental representation, one can choose the first eight generators
of G(2) ­as50,79:
�
�
𝜆a 0
0
1
∗
0 − 𝜆a 0 .
Λa = √
(11)
2 0
0 0
where 𝜆a (with a ∈ {1, 2, … , 8}) are the Gell-Mann generators of SU(3), which indeed is a subgroup of G(2), with
standard normalization Tr 𝜆a 𝜆b = Tr Λa Λb = 2𝛿ab . Λ3 and Λ8 are diagonal and represent the Cartan generators w.r.t. SU(3). The G(2) coset space by its subgroup SU(3) is a 6-sphere G(2)∕SU(3) ≅ S6 ≅ SO(7)∕SO(6)84, in
analogy with the composite Higgs ­proposal82.
The remaining six generators can be found studying the root and weight diagrams of the ­group85–87, and can
be written as:
√
√
⎛ 0
⎛
2e3 ⎞
− i𝜆2 √2e3 ⎞
0
− 𝜆2 i √
⎟
⎟
1 ⎜
1 ⎜
Λ9 = √ ⎜ i𝜆2
,
Λ
=
0
0
− i 2e3 ⎟,
2e3 ⎟ 10 √ ⎜ −𝜆
(12)
2
√
√
√
√
6 ⎜ 2eT 2eT 0 ⎟
6 ⎜ −i 2eT i 2eT
⎟
0
⎝
⎝
⎠
⎠
3
3
3
3

√
√
⎛ 0
⎛
2e2 ⎞
i𝜆5 √2e2 ⎞
0
𝜆5
i √
⎜
⎜
⎟
⎟
1
1
Λ11 = √ ⎜ −i𝜆5
0
𝜆5
0
− i 2e2 ⎟,
2e2 ⎟, Λ12 = √ ⎜ √
√
√
√
6 ⎜ 2eT 2eT 0 ⎟
6 ⎜ −i 2eT i 2eT
⎟
0
⎝
⎝
⎠
⎠
2
2
2
2

(13)

√
√
⎛ 0
⎛
2e1 ⎞
− i𝜆7 √2e1 ⎞
0
− 𝜆7 i √
⎟
⎟
1 ⎜
1 ⎜
Λ13 = √ ⎜ i𝜆7
,
Λ
=
0
0
− i 2e1 ⎟,
2e1 ⎟ 14 √ ⎜ −𝜆
7
√
√
√
√
6 ⎜ 2eT 2eT 0 ⎟
6 ⎜ −i 2eT i 2eT
⎟
0
⎝
⎝
⎠
⎠
1
1
1
1

(14)

where ei are the unit vectors

e1 =

( )
( )
0
1
0 , e2 = 1 ,
0
0

e3 =

( )
0
0
.
1

(15)

In the chosen basis of the generators it is manifest that, under SU(3) subgroup transformations, the 7-dimensional representation decomposes ­into50,79

{7} = {3} ⊕ {3} ⊕ {1}.

(16)

Since all G(2) representations are real, the {7} representation is identical to its complex conjugate, so that G(2)
“quarks” and “anti-quarks” are conceptually indistinguishable. This representation describes a SU(3) quark {3},

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

6

## PDF page 7

www.nature.com/scientificreports/

a SU(3) anti-quark {3} and a SU(3) singlet {1}. The generators transform under the 14-dimensional adjoint
representation of G(2)50,79, which decomposes ­into50,79,88
(17)

{14} = {8} ⊕ {3} ⊕ {3}.

So the G(2) “gluons” ensemble is made of SU(3) gluons {8} plus six additional “gluons” which have SU(3)
quark and anti-quark color quantum numbers. As mentioned before, the center of G(2) is trivial, containing
only the identity, and the universal covering group of G(2) is G(2) itself. This has important consequences for
­confinement79,88–90: we will see that the color string between G(2) “quarks” is capable of breaking via the creation
of dynamical gluons. As discussed ­in50, the product of two fundamental representations
(18)

{7} ⊗ {7} = {1} ⊕ {7} ⊕ {14} ⊕ {27},

shows a singlet {1}: as a noteworthy implication, two G(2) “quarks” can form a color-singlet, or a “diquark”.
Moreover, just as for SU(3) color, three G(2) “quarks” can form a color-singlet “baryon”:

{7} ⊗ {7} ⊗ {7} = {1} ⊕ 4 {7} ⊕ 2 {14} ⊕ 3 {27} ⊕ 2 {64} ⊕ {77}.

(19)

Due to the fact that “quarks” and “antiquarks” are indistinguishable, it is straightforward to show for the
one flavor Nf = 1 case that the U(1)L=R = U(1)B baryon number symmetry of SU(3) QCD is reduced to a Z2B
­symmetry50,91: one can only distinguish between states with an even and odd number of “quark” constituents.
Another useful example is
(20)

{7} ⊗ {14} ⊗ {14} ⊗ {14} = {1} ⊕ ⋯

From this composition it is clear that three G(2) “gluons” are sufficient to screen a G(2) “quark”, producing a
color-singlet hybrid qGGG​. It is also true that:
(21)

{7} ⊗ {7} ⊗ {7} ⊗ {7} = 4{1} ⊕ ⋯

so that the product contains four singlets.
Summarizing: a G(2) gauge theory has colors, anticolors and color-singlet, and 14 generators. So it is characterized by 14 gluons, 8 of them transforming as ordinary gluons (as an octuplet of SU(3)), while the other 6
G(2) gauge bosons separates into {3} and {3}, keeping the color quarks/antiquarks quantum numbers, but they
are still vector bosons. A general Lagrangian for G(2) Yang–Mills theory can be written ­as1,50,79:

1
2
LYM [A] = − Tr [F𝜇𝜈
],
2

(22)

F𝜇𝜈 = 𝜕𝜇 A𝜈 − 𝜕𝜈 A𝜇 − igG [A𝜇 , A𝜈 ],

(23)

with the field strength
obtained from the vector potential

A𝜇 (x) = Aa𝜇 (x)

Λa
.
2

(24)

with gG a proper coupling constant for all the gauge bosons and Λa the G(2) generators. The Lagrangian is invariant under non-Abelian gauge transformations A′µ = U(Aµ + ∂µ )U †, with U(x) ∈ G(2). G(2) Yang–Mills theory
is asymptotically free like all non-Abelian SU(N) gauge theories and, on the other hand, we expect confinement
at low ­energies79. The G(2) confinement is surely peculiar with a different realization with respect to SU(3), where
gluons cannot screen quarks (and screening arises due to dynamical quark-antiquark pair creation). In particular,
as we have already seen in Eq.(20), G(2) admits a new form of exceptional confinement. It has been showed that
G(2) lattice Yang–Mills theory is indeed in the confined phase in the strong coupling ­limit50.
But we know that G(2) is not a proper gauge theory for a real Quantum Chromodynamics theory. Therefore
we must add a Higgs-like field in the fundamental {7} representation in order to break G(2) down to SU(3).
The consequence is simple and fundamental: 6 of the 14 G(2) “gluons” gain a mass proportional to the vacuum
expectation value (vev) w of the Higgs-like field, the other 8 SU(3) gluons remaining untouched and massless.
The Lagrangian of such a G(2)-Higgs model can be written ­as17,50,79,88:

LG2 H [A, Φ] = LYM [A] + (D𝜇 Φ)2 − V (Φ)

(25)

where Φ(x) = (Φ1 (x), Φ2 (x), … , Φ7 (x)) is the real-valued Higgs-like field, Dµ � = (∂µ − igG Aµ )� is the covariant derivative and
(26)

V (Φ) = 𝜆(Φ2 − w 2 )2

the quadratic scalar potential, with 𝜆 > 0. Because of the {7} ⊗ {7} ⊗ {7} = {1} ⊕ ⋯ singlet state seen before,
in the fundamental representation a Higgs cubic term should be considered but, according to the antisymmetric
property of Tabc , such a term disappears. Following the product in Eq.(21), the four singlets corresponds to w 2 Φ2,
Φ4 and two vanishing due to antisymmetry, making the aforementioned potential general and consistent with
G(2) symmetry breaking and renormalizability. We can choose a simple vev like Φ0 = √1 (0, 0, 0, 0, 0, 0, w) to
2

Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

7
Vol.:(0123456789)

## PDF page 8

www.nature.com/scientificreports/
break G(2) and re-obtain the familiar unbroken SU(3) symmetry: it is easy to notice from the diagonal and nondiagonal structure of Eqs. (11–14) that

Λ1−8 Φ0 = 0

(unbroken generators)

(27)

Λ9−14 Φ0 ≠ 0

(broken generators)

(28)

Plugging this scalar field vev into the square of the Higgs covariant derivative, we get the usual quadratic term
in the gauge fields

gG2 Φ†0

Λa Λb
1
Φ Aa (x)A𝜇,b (x) = Mab Aa𝜇 (x)A𝜇,b (x)
2 2 0 𝜇
2

(29)

that gives the diagonal mass matrix Mab for the gauge bosons, of which we can use the aforementioned trace
normalization relation, which Gell-Mann matrices and G(2) generators share, to put the squared masses terms
gG2 w 2 in evidence. This new scalar , which acquires a typical mass of
√
(30)
MH = 2𝜆w
from the expansion of the potential about its ­minimum1, should be a different Higgs field w.r.t. the SM one, with
a much higher vev, in order to disjoin massive gluons dynamics from SM one, and a strong phenomenology.
Such a strongly coupled massive field could be ruled out by future LHC and Future Circular Collider ­searches92
(it is enough to think of heavy scalars models searches, such as the two-Higgs doublet ­model93 or the composite
Higgs ­models94). In this picture, as anticipated, following the standard Higgs mechanism to build up the dark
candidates, 6 massless Goldstone bosons are eaten and become the longitudinal components of G(2) vector
gluons corresponding to the broken generators, which acquire the eigenvalue mass

M G = gG w

(31)

1

through the Higgs ­mechanism , according to Eg. (29), and exhibit the color quarks/antiquarks quantum numbers.
No additional Yukawa-like terms are needed for the purpose of the present proposal, so that quarks remain massless at the scale of G(2) symmetry breaking, since the SM Higgs has not yet acquired its vev. Then, if the sedenions
description via automorphisms group is invoked, the symmetry breaking process could in principle act on three
different copies of G(2), expressed by the permutation factor S3 which keeps track of the three fermion families. In other words, a Higgs sector (the SM one or an additional strong-coupled one for G(2)) of a S3-invariant
extension of the SM could also break the flavour symmetry in order to produce the correct patterns of different
masses and mixing angles for fermions families ­(see72,95 for insights). Additionally, it has been shown that, in a
phenomenologically viable electroweak S3 extension of the SM, S3 symmetry should be broken to prevent flavor
changing neutral ­currents72 and the Higgs potential becomes more complicated due to the presence of three
Higgs ­fields74. For simplicity, we could assume that this hypothetical process, involving S3 breaking and Yukawa
fermion masses generation, triggers at the electroweak scale, without interfering with the G(2) Higgs potential.
Using the Higgs mechanism to smoothly interpolate between SU(3) and G(2) Yang–Mills theory, we can
study the deconfinement phase transition. In the SU(3) case this transition is weakly first order. In fact, in (3 + 1)
dimensions only SU(2) Yang–Mills theory manifest a second order phase transition, whereas, in general, SU(N)
Yang–Mills theories with any higher N seem to have first order deconfinement phase ­transitions96–100, which are
more markedly first order for increasing N. The peculiarities of the phase transition from lattice G(2)-Higgs to
SU(3) have been extensively studied ­in16,90,101–103, confirming that G(2) gauge theory has a finite-temperature
deconfining phase transition mainly of first order and a similar but discernable behavior with respect to SU(N)103.
It is interesting to mention that it has been ­shown104–107 that first order phase transitions in the early Universe
could produce gravitational waves detectable by future space-based gravitational observatories such as LISA.
Moving back to the G(2) color string, the breaking of this string between two static G(2) “quarks” happens
due to the production of two triplets of G(2) “gluons” which screen the quarks. Hence, the string breaking scale is
related to the mass of the six G(2) “gluons” popping out of the vacuum. The resulting quark-gluons bound states
(colorless qGGG​states) coming from the string breaking, must be both G(2)-singlets and SU(3)-singlets. When
we switch on the interaction with the Higgs field, six G(2) gluons acquire a mass thanks to the Higgs mechanism.
The larger is MG , the greater is the distance where string breaking occurs. When the expectation value of the
Higgs-like field is sent to infinity, so that the 6 massive G(2) “gluons” are completely removed from the dynamics,
also the string breaking scale is infinite. Thus the scenario of the usual SU(3) string potential reappears. For small
w (on the order of ΛQCD ), on the other hand, the additional G(2) “gluons” could be light and participate in the
dynamics. As long as w remains finite, as we know it should be in the SM and in its extensions, the massive G(2)
“gluons” can mediate weak baryon number violating ­processes50 (only in the w → ∞ limit baryon number is an
exact discrete symmetry of the Lagrangian). Finally, for w = 0 the Higgs mechanism disappears and we come
back to G(2). As stressed before, hereafter only high w values (with w much greater that the SM Higgs vev) are
considered in order to realize a consistent dark matter scenario.
For what concerns the hadronic spectrum of a hypothetical G(2)-QCD, the physics appears to be qualitatively
similar to SU(3) ­QCD108, but richer. This can be easily demonstrated from the decomposition of representations
products, like Eq.(18), (19), (20), (21). In the (massless) spectrum of the unbroken G(2) phase there are many
more states beyond standard mesons and baryons: one-quark-three-G(2) gluons hybrid states (and, in general,
the quark confinement for one-quark-N-G(2) gluons, with N ≥ 3), diquarks, (qqqq) tetraquarks and (qqqqq)
pentaquarks. States with baryon number 0 and 3 are in common with QCD whereas nB = 1, 2, of J = 1∕2 hybrids

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

8

## PDF page 9

www.nature.com/scientificreports/
and J = 0, 1 diquarks respectively, are G(2) specific. A tentative spectrum for the bosonic diquarks from lattice
simulations has been proposed ­in108. G(2) and SU(3) also share glueballs states, for any numbers of G(2) gluons
(2 and 3 in the ground states) and hexaquarks. The complete explicit decompositions of the products are:
{7} ⊗ {14} ⊗ {14} ⊗ {14} = {1} ⊕ 10{7} ⊕ 6{14} ⊕ 15{27} ⊕ 20{64} ⊕ 13{77} ⊕ 13{77′ } ⊕ 10{182}
⊕ 15{189} ⊕ 9{286} ⊕ 3{378} ⊕ 6{448} ⊕ 3{729} ⊕ {896} ⊕ 2{924}

{7} ⊗ {7} ⊗ {7} ⊗ {7} = 4{1} ⊕ 10{7} ⊕ 9{14} ⊕ 12{27} ⊕ 8{64} ⊕ 6{77} ⊕ 2{77′ } ⊕ {182} ⊕ 3{189}
{7} ⊗ {7} ⊗ {7} ⊗ {7} ⊗ {7} = 10{1} ⊕ 35{7} ⊕ 30{14} ⊕ 45{27} ⊕ 40{64} ⊕ 30{77}

⊕ 11{77′ } ⊕ 10{182} ⊕ 20{189} ⊕ 5{286} ⊕ {378} ⊕ 4{448}
{7} ⊗ {7} ⊗ {7} ⊗ {7} ⊗ {7} ⊗ {7} = 35{1} ⊕ 120{7} ⊕ 120{14} ⊕ 180{27} ⊕ 176{64} ⊕ 145{77}

⊕ 65{77′ } ⊕ 65{182} ⊕ 120{189} ⊕ 5{273} ⊕ 40{286} ⊕ 15{378} ⊕ 40{448} ⊕ {714} ⊕ 9{729} ⊕ 5{924}

{14} ⊗ {14} = {1} ⊕ {14} ⊕ {27} ⊕ {77} ⊕ {77′ }

{14} ⊗ {14} ⊗ {14} = {1} ⊕ {7} ⊕ 5{14} ⊕ 3{27} ⊕ 2{64} ⊕ 4{77} ⊕ 3{77′ } ⊕ {182} ⊕ 3{189} ⊕ {273} ⊕ 2{448}.

Even collective manifestations of G(2) exceptional matter could be different: for example, a G(2)-QCD neutron star could display a distinct behavior with respect to a SU(3) neutron gas star, as discussed ­in109.
In the next section the focus will be on the phenomenology of the massive G(2) glueball states.

The exceptional gluonic content of the theory: a possible dark matter
phenomenology

As discussed before, the G(2) extension of the SM produces an exceptional particle sector: if we move away the six
G(2) gluons from the dynamics, these bosons must be secluded and separated from the visible SM sector in first
approximation, without experimentally accessible electroweak interactions, unlike WIMPs, and extreme energies (and distances) should be mandatory to access the G(2) string breaking. This could be due to the very high
energy scale of the G(2) − SU(3) phase transition, occurring at much greater energies than electroweak breaking
scale. This could be the realization of a beyond Naturalness criterion. Indeed, G(2) gluons, as SU(3) ones, are
electrically neutral and immune to interactions with light and weak W, Z bosons at tree level. Another advantage
of a G(2) broken theory is that no additional families are added to the Standard Model, unlike SU(N) theories.
Overall, this seems to be a good scenario for a cold dark matter (CDM) theory (cold means non-relativistic
and refers to the standard Lambda-CDM cosmological model), if we find a stable or long-lived candidate. Many
vector bosons composite states have been proposed as DM candidates in the last two decades: light hidden
­glueballs110–113, gluon ­condensates114, exceptional dark matter referring to a composite Higgs model with SO(7)
symmetry broken to the exceptional G(2)115, SU(N) vector gauge ­bosons116, vector Bose-Einstein condensates
(BECs)117 and, in general, non-Abelian dark ­forces118. These studies demonstrate the growing interest in beyond
SM non-Abelian frameworks where to develop consistent DM theories, without invoking string theory and
keeping the theoretical apparatus sufficiently minimal.
In our case, the six dark gluons can form dark glueballs constituted by two or three (or multiples) G(2) gluons,
according to {14} ⊗ {14} = {1} ⊕ ⋯ and {14} ⊗ {14} ⊗ {14} = {1} ⊕ ⋯ ­representations108, with integer total
angular momentum J = 0, 2 and J = 1, 3 for 2-gluons and 3-gluons balls respectively. In principle, exceptionalcolored broken-G(2) glueballs should not be stable, if these massive composite states themselves have no extra
symmetries to prevent their decay; since the proposed G(2) theory includes QCD, unlike hidden Yang–Mills
theories with no direct connections with the ­SM111,119, there exist states that couple to both the exceptionalcolored glueballs and SU(3) particles (for example the G(2)-breaking Higgs field): hence, whether at tree-level
or via loops, these heavy glueballs would not be stable. To avoid this, first of all the new G(2) Higgs should be at
least more massive than the lightest 2-gluons glueball, so that MH > MGG, which implies the qualitative constraint
√
2𝜆 > 2gG from Eq.(30), (31); secondly, the decays into meson states should be also forbidden. In principle, a
lightest J PC = 0++ state, in analogy with standard QCD, could dominate the glueball ­spectrum120, but this could
be unstable, like the lightest meson 𝜋 0 and the other known scalar particle, the SM Higgs h0. The possibility of
a conserved charge or a peculiar phenomenon which guarantees stability to the lightest glueball states should
not be ruled out a priori, considering that analytical and topological properties of Yang–Mills theory solutions
are still not completely understood: even the fundamental problem of color confinement has not a definitive
answer nor an analytical proof.
For example, in analogy with the baryon number conservation and the forbidden proton decay into 𝜋 0, one
can introduce a conserved additive gluon number Ŵ for the glueball states, which counts the number of massive
G(2) gluons (and “antigluons”), preventing the glueball from decaying into SM mesons, which are not made
of G(2) gluons (one has to keep in mind that these peculiar bosons do mantain the color quarks/antiquarks
quantum number). Indeed, also the U(1)B global symmetry of the Standard Model which prevents the proton
decay is an accidental symmetry and not a fundamental law, that can be broken by quantum effects. A large class
of ­models121–123 imposes global discrete Z2 (or generally Zn124) or continuous U(1) symmetries to guarantee DM
stability, in which DM is odd under the new symmetry while SM fields are assumed to be even: even in our case
one can introduce such a Z2 symmetry, inherited from the new G(2)-breaking Higgs field, preventing the lightest
G(2) two-gluons glueball decay. A complementary choice is to invoke another multiplicative quantum number,
i.e. a G-parity conservation for a generic Yang–Mills theory as suggested ­in125, to generalize the C-parity and
apply it to meson-like multiplets; unlike the lightest QCD mesons π which possess electroweak interactions, the
lightest G(2) glueball could represent a sort of stable dark meson (due to the quark–antiquark quantum numbers
Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

9
Vol.:(0123456789)

## PDF page 10

www.nature.com/scientificreports/
carried by the two G(2) gluons), whose dynamics is constrained inside the G(2) broken sector itself, leading to
an exactly conserved G-parity and the impossibility to decay into G-even SM particles.
We have the same lack of knowledge for the glueballs interactions with their own environments: as for residual
nuclear force between hadrons in nuclei, the possibility of a residual binding interaction between glueballs,
preventing the decay (like the neutron case in the nucleus), must be investigated.
Possibly, one can also postulate a suppression scale 1∕fG (ΔM) for the couplings with SM which depends on
the relative mass difference between the interacting particles, i.e. the dark glueball and the quarks: if the masses
of the glueballs are too high w.r.t. the QCD scale, their decay might be highly suppressed.
Another interesting opportunity is to invoke the J PC = 0++ , 2++ dark G(2) glueball states as graviton counterparts in a AdS/CFT correspondence framework, as discussed ­in126 for QCD glueballs (even if this does not
exhaust the quest for stability). Moreover, the scalar glueball could be part of a scalar-tensor gravity ­approach127,
whereas the tensor glueball could play the role of a massive graviton-like particle, for example in the context of
bimetric gravity ­theory128,129, where the massive gravitational dark matter can non-trivially interact with gravity itself. The couplings to SM quarks of such a tensor DM can be by far too ­weak129, making it undetectable in
collider searches; besides, the requirement of a correct DM abundance and stability constrains a non-thermal
spin-2 mass to be >> 1 ­TeV130.
Furthermore, it must be considered that bosonic ensembles could eventually clump together to form a BEC:
once the temperature of a cosmological boson gas is less than the critical temperature, a Bose-Einstein condensation process can always take place during the cosmic history of the Universe, even if the not low mass of these
candidates should disfavor this scenario. For example, the occurence of glueballs condensates and glueball stars
have been recently discussed ­in119,131–133.
Such a dark sector can naturally accommodate the fact that there is only gravitational evidence for dark matter
so far, certainly disfavoring direct and indirect searches, and it can also qualitatively account for the observation
that dark matter and ordinary matter are in commensurable quantities (approximately 5:1 from recent Planck
experiment ­measurements134), as they come from the same broken gauge group. Given the forbidden or extremely
weak interactions between the G(2) glueball states and ordinary matter, the usual WIMP-like scenario in which
the DM relic abundance is built via the freeze-out mechanism cannot be achieved, since these bosons are not
in thermal equilibrium with the baryon-photon fluid in the early Universe: their production should be abruptly
triggered by a first-order cosmological phase transition, possibly fixing their initial abundance. It is well-known
that several non freeze-out models has been proposed in literature, such as the FIMP (Feebly Interacting Massive
Particle) cosmology via a freeze-in ­mechanism135,136, in which the comoving DM abundance freezes when the
number densities of the visible sector, generating DM by decays or annihilations, become Boltzmann-suppressed,
ending the yield. This requires an extremely small coupling (O(10−7 ) or less) with the visible sector. Another
intriguing alternative is represented by the so-called Dark freeze-out, for which DM reaches an equilibrium heat
bath within the dark sector itself, never interacting with SM particles: in this case, the dark ensemble was initially
populated by a freeze-in-type yield from part of the visible sector.
In analogy, trying to construct a particle cosmology for the exceptional gluonic content of the present theory,
let’s suppose that a two-gluons G(2) glueball could be ab initio produced out of thermal equilibrium, for instance
by a heavy mediator decay in the visible sector heat bath, such as the new G(2)–Higgs ( H → DMDM ): this is
viable if MH ≥ MGG and the coupling between DM and the heavy Higgs is sufficiently weak, realizing an exoticHiggs portal DM137.
In principle, the most general scalar glueball effective potential, in the large N limit of a SU(N) gauge theory, may contain not only a quartic interaction, proper of a Higgs portal, but also the cubic and higher order
­terms119,138,139, in the form

V (S) =

∞
∑
ai ( 4𝜋 )i−2

i!
i=2

N

m4−i Si

(32)

where S is the scalar G(2) glueball field, m the mass term and the coefficients are ai ≈ 1, which could be obtained
from lattice computations. The trilinear interaction might generate an attractive Yukawa-like ­potential138, whereas
the quartic one may be repulsive, according to the sign of the coupling; the fifth and higher terms might be suppressed by the mass scale and the decreasing couplings. Choosing the simplest scalar case with a Z2 symmetry
with a negligible cubic interaction (according to the minimal Higgs-portal paradigm), from now on we adopt a
renormalizable scalar G(2)-glueball potential, coupled to the exotic heavy Higgs sector, of the type

V (Φ, S) = V (Φ) +

m2 2 𝜆S 4 𝜆HS 2 2
S + S +
ΦS
2
4
2

(33)

where 𝜆S is the quartic self-interaction strength, 𝜆HS the heavy Higgs-scalar glueball coupling and V (Φ) is
described by Eq. (26); MS 2 = m2 + 𝜆HS w 2 ∕2 can be defined as the total mass after the G(2) symmetry breaking
(which trivially implies 𝜆HS ≤ 2MS 2 ∕w 2). If the portal coupling is sufficiently ­small135, one can recover a correct
dark matter relic abundance Ωh2 ≃ 0.12134. In fact, the approximate solution for this present-day DM abundance,
assuming the initial number density of DM particles negligible, ­is135

�S h2 ≃ 4.48 × 108

gH
MS MPl ŴH→SS
,
√
g∗s g∗ GeV
MH2

(34)

where g∗s and g∗ are effective numbers of degrees of freedom for entropy and energy densities, gH is the intrinsic
number of degrees of freedom of H (the expression is evaluated around T ≃ MH ) and where MPl is the Planck

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

10

## PDF page 11

www.nature.com/scientificreports/

mass. For g∗s ≃ g∗ and ŴH→SS ≃ 2HS MH /(8π), Eq. (34) gives an estimate for the coupling intensity as a function of the DM abundance:

𝜆HS ≃ 10−12

( Ω h2 )1∕2 ( g )3∕4 ( M )1∕2
S

∗

H

0.12

100

MS

.

(35)

It’s easy to verify that, for Ωh2 ≃ 0.12, g∗ ≃ 100 and not MH ∕MS >> 1 ratios, 𝜆HS << 1. Furthermore, studying the exotic Higgs-portal135 in the context of the G(2)-breaking mechanism, one can approximate again
MS
Eqs. (34)–(35) as �S h2 /0.12 ≃ 1024 2HS M
and insert the scalar glueball mass for m2 << 𝜆HS w 2 , i.e. a scalar
H
mass integrally generated by the Higgs expectation value
√
MS = MGG ≃ 2gG w ≈ 𝜆HS ∕2w,
(36)
as an explicit function of the Higgs-scalar coupling, to obtain:
5/2

�S h2 /0.12 ≃ 1024 HS (w/MH ).

(37)

For w∕MH = O(1), to reproduce the correct relic density the coupling should be very tiny, i.e. 𝜆HS ∼ 10−(10÷9),
as in most FIMP ­theories135,140.
The situation can change if 𝜆S is large enough (𝜆S > 10−3122), i.e. if scalar self-interactions are active: the DM
particles, initially produced by the previous mechanism, may thermalize among themselves even if the dark
sector consists of only one particle species, due to number-changing processes (generic nDM → n′DM processes),
which reduce the average temperature of DM particles and increase the number density until equilibrium is
reached. The resulting relic abundance could therefore change even though the coupling between the visible
and dark sector is absent. This could be the case of a SIMP (Strongly Interacting Massive Particle) scenario with
a dark freeze-out ­mechanism122,135,137. For example, in case of a quartic self-interaction, thermalization of the
dark sector within itself through 2 ↔ 4 scatterings is active if 𝜆S exceeds a critical value, so that DM reaches a
thermal equilibrium. When DM is no longer relativistic, 4 → 2 processes dominate the dynamics in the so-called
cannibalization era, which ends when its rate drops below the Hubble rate, fixing the DM number density to a
modified yield through the dark freeze-out. Odd processes, such as 2 ↔ 3, could be neglected for DM potential
without odd powers terms and are forbidden for multiplicative Zn symmetry conservation for even n122, like in
most well-established DM ­setups141. As shown ­in122,142, if DM relic abundance is solely computed via a Higgs
decay in a freeze-in framework, without dark thermalization for 4 → 2 interactions, it could be appreciably
underestimated (over an order of magnitude) and, consequently, the previous bounds for the parameters space
could be altered. Quartic self-interactions should also fulfill additional constraints from ­cosmology140,142, such
as the isocurvature bound, for which the scalar mass is bounded from above:
)−3/2
( H
MS
∗
3/8
< 6S
(38)
GeV
1011 GeV
with H∗ the Hubble parameter at the inflationary scale.
The resolution of Boltzmann equation for SIMP DM usually leads to scenarios where the dark freeze-out
temperature is less than the visible ensemble one, making DM naturally colder than SM particles. ­See141,143–147
for insights regarding 3 → 2 dark thermalization and explicit formulas for the relic density for a SIMP DM with
3 ↔ 2 annihilations, which do not have immediate analytic representations.
For smaller interactions with the visible sector, the thermal production of DM particles is insignificant and
DM must come from a non-thermal mechanism, leading to a Super-WIMP (SWIMP)-like scenario, for example
through a direct DM-producing inflaton ­decay148–150, if the heavy Higgs scalar responsible for the G(2) → SU(3)
transition is identified as the inflaton field. In this inflaton-portal ­case151, the glueball abundance is basically fixed
by few parameters, i.e. the reheating temperature Trh, the inflaton mass and branching ratio into G(2) gluons/
scalar glueball BS148:

�S h2 ≃ 2 × 108 BS (MS /MH )

Trh
GeV

(39)

For a cosmological reheating above the GeV scale, the BS (MS ∕MH ) factor should be quite small, i.e. < 10−9.
The scenario works well especially for large DM masses, between the weak scale and the PeV ­scale149, and for
extremely decoupled EeV ­candidates151.
Finally we are going to briefly discuss possible manifestations of G(2) gluons in the present Universe. The six
massive gluons from the broken exceptional G(2) group, mainly as stable J PC = 0++ (and possibly J PC = 2++)
glueballs, could clump and organize into dark matter halos, in form of a heavy bosons gas or in some fluid
­systems152,153, for sufficiently low temperatures and/or enough high densities. Indeed, the idea of a (super)
fluid dark matter has recently attracted attention in literature, from Khoury’s promising proposal of a unified
superfluid dark ­sector154,155. The fact that dark matter particles could assume different “phases” according to the
environment (gas, fluid or BECs) is very suitable to account for the plethora of dark matter observations at all
scales, from galactic to cosmological ones. The realization of this scenario usually involves axions or ALPS (axion
like particles)156, which are light or ultralight (with masses from 10−24 to 1 eV in natural units) and capable of
reproducing DM halos properties: dark matter condensation and self-gravitating Bose-Einstein condensates
have been extensively studied ­in157–159.
In our scenario we hypothesize the main constituents of a possible dark fluid are broken-G(2) massive gluons
composite states. They are certainly massive, so that we cannot invoke the axion-like description. But still G(2)
Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

11
Vol.:(0123456789)

## PDF page 12

www.nature.com/scientificreports/
glueballs could aggregate into extended objects: one can explore the possibility that heavy G(2) gluon dark matter
is capable of producing stellar objects, which could populate the dark halos. Many models of exotic stars made
of unknown particles have been proposed, especially for sub-GeV masses, such as bosonic stars (where the
particle is a scalar or ­pseudoscalar160–162, most likely for a quartic order repulsive self-interaction162), Proca stars
(for massive spin 1 ­bosons163–165—one could invoke a correspondence with 3-gluons glueballs), BEC ­stars166, or
QCD glueballs ­stars133. The key ingredients to try to build up stellar objects with non-light bosons are mainly the
magnitude of the quartic order self-interaction 𝜆4 of the constitutive boson and its mass. Our glueball scalar field
S evolving in the General Relativity framework can be described by the Einstein-Klein-Gordon (EKG) action,
�
√ � R
S=
d4 x −g
− g 𝜇𝜈 𝜕 𝜇 S̄ 𝜕𝜈 S − V (S) ,
(40)
∫
16𝜋G
where V(S) is the bosonic potential, S̄ the complex conjugate for a complex scalar, R is the Ricci scalar, g 𝜇𝜈 is
the metric of the space–time, g its determinant and G is Newton’s gravitational costant. The variation of the
action with respect to the metric leads to the related Einstein ­equations162,167 for static, spherically–symmetric
geometries. To build up a massive boson star, a quartic self-interaction potential is needed to
balance the inward
M2
𝜆
gravitational force, in the form of the previously described (Eq. 33) potential, i.e. V (|S|2 ) = 2S |S|2 + 44 |S|4, where
𝜆S ≡ 𝜆4 > 0 (𝜆4 < 0) signifies a repulsive (attractive) interaction: repulsive self-interactions can give rise to very
dense boson stars. The maximum mass for such an object ­is162,166,168
√
𝜆4 MPl3
Mmax ∼ (0.1 ÷ 1) 2
(41)
MS ∕GeV2
√
1∕3
where MPl ≡ 1∕ G ≈ 1.2 × 1019 GeV ∼ M⊙ is the Planck mass and M⊙ the solar mass, with a consequent
119
boson star ­radius
√
𝜆4 × 10 km
RBS ∼ (0.1 ÷ 1)
.
(42)
MS2 ∕GeV2
For example,√
for a heavy MS ∼ 10 TeV
√ scalar, the maximum values, as a function of the self-interaction, are
Mmax ≲ 10−8 𝜆4 M⊙ and RBS ≲ 10−4 𝜆4 m: the resulting object carries a small mass w.r.t. usual stars (about
one hundredth of the Earth mass) and a √
sub-millimeter radius
√for not two high 𝜆4 , making it a tiny ball of glueballs. Instead, for a 1 GeV scalar, Mmax ≲ 𝜆4 M⊙ and RBS ≲ 𝜆4 × 10 km stand, producing a solar mass object
with a neutron star-like radius. As stressed ­in168, at the maximum mass the radius is slightly larger than the
corresponding Schwarzschild radius. In addition, for 𝜆4 = O(1), the relation is similar to the Chandrasekhar
M3
mass for white dwarf stars Mwd ≈ mPl2 : this could resemble the case of SU(N) glueballs, estimating the quartic
p

coupling as 𝜆4 ∼ (4𝜋)2 ∕N 2168 (see Eq. (32)), being 4 < 4π for ­perturbativity161. Even if it is fair that G(2) glueballs
are strongly self interacting, it is quite hard to make precise estimates for their scattering process, given our
general limited knowledge concerning strongly coupled theories. Nevertheless, considering the dimension of
the exceptional G(2) group and its lattice ­behaviour103, we could qualitatively approximate it to a SU(4) theory
and obtain 𝜆4 ∼ 𝜋 2 , which almost saturates the perturbativity condition 4 < 4π . For example, for such a 𝜆4 ,
both the aforementioned Mmax ranges, i.e. 10−8 M⊙ and few M⊙, fall into mass windows with weak constraints
for MACHOs from up-to-date microlensing ­analysis169,170. Obviously, the feasibility of a star made of self-interacting scalars also depends on a correct estimate of the possible 3 → 1, 3 → 2 and 4 → 2 annihilation processes
inside the ­star168, which in turn depend on the symmetries (e.g. Zn ) of the exotic sector; for a non-conserved
glueballs number, i.e. for a real scalar with no additional symmetries, 3∕4 → 2 processes could trigger the decay
of massive bosons stars,leading to severe bounds on their mass: Mmax < 10−11 M⊙.
For the so-called mini boson stars (with no scalar interaction potential) and Proca stars, the maximum mass
M2
is quite smaller and scales with ∼ MPl . Furthermore, unlike complex scalar fields, real scalars stars could not
S
possess the required stability: however, with a non-trivial time-dependent stress-energy tensor, long-term stable
oscillating geometries can be ­achieved167. These “oscillatons” mass-radius relations are indeed very similar to the
boson stars ones.
It is well-known that the inclusion of self-interactions in the DM sector should be in agreement with the
upper limits which come from several astrophysical ­observations2,171,172, mainly from colliding galaxy clusters
dynamics, like the the Bullet ­Cluster173. The DM-DM scattering cross section must qualitatively satisfy
2
9𝜆4 2
cm2
𝜎
135
< 1 cmg ∼ 10−24 GeV
. Assuming 𝜎 = 32𝜋M
, the ­bound161 results in
2 at tree ­level
MS
S
( M )3∕2
S
|𝜆4 | < 4 ⋅ 102
(43)
GeV
which is consistent with the one obtained ­in137. In principle the intensity of the self-interaction is not effectively
bounded by the scalar mass scale of the present theory: the more the DM particle is massive the more the constraint for 𝜆4 is relaxed. Exploiting Eq. (36) with a FIMP-like 𝜆HS ∼ 10−10, Eq. (43) becomes
)
(
w 3∕2
|𝜆4 | < 10−5
.
(44)
GeV

For the aforementioned 𝜆4 ∼ 𝜋 2 self-interaction assumption, this formula implies an expectation value for the
heavy Higgs satisfying w ≥ 104 GeV, which is completely consistent with a beyond SM phenomenology. Such a
Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

12

## PDF page 13

www.nature.com/scientificreports/
FIMP/SIMP-like singlet scalar model, constrained by astrophysical observations and the perturbativity condition, naturally leads to a DM mass in the GeV/sub-GeV ­region122 (Eq. (43)). This is also valid from Eq. (38) for
an inflation scale H∗ ≳ 1012 GeV. The empirical Eq. (43) relation for the glueball scalar mass is quite equivalent
to the theoretical ones in Eqs. (35)–(36), for which 𝜆HS ∼ 10−10 and w∕MH = O(1) imply MS ∼ 10−(5÷4) MH .
DM candidates could be certainly studied from peculiar behaviors of the compact astrophysical objects they
form, characterizing physical observables useful to disentangle standard scenarios from exotic ­phenomenology167.
In fact, for a few years we can take advantage of both electromagnetic and gravitational waves astronomy as
powerful probes to discriminate compact objects as a function of their “compactness” (or “closeness” to a black
hole—a quantity related to the mass to radius ratio M/R is a possibility), “shadow” and gravitational waves
­emission167. For example, a hypothetical binary SU(N) gluons star could be disentangled from a binary black
hole system, due to possible differences in the gravitational wave frequency and amplitude, as demonstrated
­in119: this comes from the fact that the mass-radius relation of the glueball dark star, as in our case, is different
from that of a black hole, as discussed before. In addition, ­in119 the authors show that, adopting a large N glueball
potential like the one in Eq. (32), the dark star is allowed to be more massive and larger at the same time, w.r.t.
the quartic potential case in Eq. (33). No accompanying luminous signal is obviously expected for G(2) glueballs
astrophysical objects, unlike generic beyond SM theories equipped with electro-weak interactions.
Even more ambitious, one should consider the possibility to probe the SU(3) − G(2) phase transition from
black hole formation, as suggested i­n174 for quark matter: this is possible if black holes are formed through
exotic condensed matter stages beyond degenerate neutron matter, maybe exploiting the theoretical framework
of gauge/gravity ­dualities175. It could be also worthwhile to speculate on the possibility that, in extremely high
pressure and temperature quark matter phases, unbroken G(2) quarks can combine into multiquarks particles or
can be seized by G(2) gluons to form qGGG​screened states, rearranging QCD matter into a phase of color-singlet
hybrids and exotic hadrons. For example, the preliminary work ­by109 demonstrates the possibility to distinguish
a simplified G(2)–QCD neutron star using the mass-radius relation.
So dark G(2) glueballs can be very versatile and exploitable within theoretical speculations, especially for
exotic scalars coupled to a Higgs sector.

Conclusions

If Nature physical description is intrinsically mathematical, fundamental microscopic forces might be manifestation of the algebras that can be built via the Cayley-Dickson construction process. In other words, algebras can
guide physics through the understanding of fundamental interactions. To translate the mathematical meaning
into a physical language, one has to move from abstract algebras to groups of symmetry, through a correspondence here proposed as an automorphism relation. This leads to the discovery of a mismatch between SU(3) strong
force and octonions: the octonions automorphism group is the exceptional group G(2), which contains SU(3),
but it is not exhausted by SU(3) itself. In the difference between the physical content of G(2) and SU(3) new
fundamental particles lie, in the form of six additional massive bosons organized in composite states, disconnected by Standard Model dynamics: the exceptional-colored G(2) gluons. These gluons cannot interact with SM
particles, at least at the explored energy scales, due to their mass and QCD string behavior. Mathematical realism
has been the guide and criterion to build this minimal extension of the Standard Model.
Hence, for the first time in literature, G(2) was treated and developed as a realistic symmetry to enlarge the
Standard Model, and not only as a lattice QCD tool for computation. G(2) is a good gauge group to describe a
larger interaction, which operated in the Early Universe before the emergence of visible matter; when the Universe cooled down, reaching a proper far beyond TeV energy scale at which G(2) is broken, usual SU(3) QCD
appeared, while an extra Higgs mechanism produced a secluded sector of cold exceptional-colored bosons. The
SM is naturally embedded in this framework with a minimal additional particle content, i.e. a heavy scalar Higgs
particle, responsible for a Higgs mechanism for the strong sector symmetrical w.r.t. the electroweak one, and a
bunch of massive gluons, in principle with the same masses, whose composite states might play the role of dark
matter. Some accidental stability mechanisms for the dark glueballs have been proposed. The presence of a new
Higgs field represents the usual need of a scalar sector to induce the symmetry breaking of a fundamental gauge
symmetry. The extra Higgs might have visible decay channels, but it belongs to a very high energy scale which
is certainly beyond current LHC searches, i.e. a multi-TeV or tens/hundreds of TeV scale defined by the vaccum
expectation value of the extra Higgs. The resulting exceptional glueball DM is certainly compatible with direct,
indirect, collider searches and astrophysical observations, as it is almost collisionless. Several cosmological scenarios for these candidates were discussed, constraining the parameters space of the theory.
In addition, if one tries to extend the correspondence between mathematical algebras and physical symmetries further beyond octonions, sedenions show an intriguing property: they still have G(2) as a fundamental
automorphism, but “tripled” by an S3 factor, which resembles the three fermion families of the Standard Model
and its S3-invariant extension. We know larger symmetries can be constructed using the products of octonions
(sedenions) and the other division algebras, pointing towards subsequent exceptional groups, as illustrated by
the Freudenthal–Tits magic square, which have been the subjects of string theories, but we did not want to push
the dissertation in this direction. Indeed the choice of G(2), as automorphism group of octonions and minimally
enlarged non-Abelian compact Lie algebra of rank 2, is the minimal exceptional extension of the Standard Model
including a reliable exotic sector, requiring no additional particle families nor extra fundamental forces. This fact
reconciles the particle desert observed between the SM Higgs mass scale and the TeV scale. G(2) could guarantee
peculiar manifestations in extreme astrophysical compact objects, such as boson stars made of G(2) glueballs,
which can populate the dark halos and be observed in the future studying their gravitational waves and dynamics.
The development of a definitive theory is beyond the purpose of the present phenomenological proposal,
which is intended as a guideline for further speculations.

Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

13
Vol.:(0123456789)

## PDF page 14

www.nature.com/scientificreports/
Received: 10 June 2021; Accepted: 3 November 2021

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
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.
50.
51.
52.

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

Thomson, M. Modern Particle Physics (Cambridge University Press, 2013).
Bertone, G. Particle Dark Matter: Observations, Models and Searches (Cambridge University Press, 2010).
Profumo, S. An Introduction to Particle Dark Matter (World Scientific Publishing Europe Ltd., 2017).
Mitsou, E. Infrared Non-local Modifications of General Relativity (Springer, 2016).
Eleftherios, P. Modifications of Einstein’s Theory of Gravity at Large Distances (Springer, 2015).
Clifton, T., Ferreira, P. G., Padilla, A. & Skordis, C. Modified gravity and cosmology. Phys. Rep. 513, 1–189. https://​doi.​org/​10.​
1016/j.​physr​ep.​2012.​01.​001 (2012).
Baudis, L. The search for dark matter. Eur. Rev. 26, 70–81 (2018).
Schramm, S. Searching for Dark Matter with the ATLAS Detector 1st edn. (Springer, 2017). https://​doi.​org/​10.​1007/​
978-3-​319-​44453-6.
Masi, N. Dark matter: TeV-ish rather than miraculous, collisionless rather than dark. Eur. Phys. J. Plus 130, 1–12 (2015).
Salvio, A. & Sannino, F. From the Fermi scale to cosmology. Front. Astron. Space Sci. 6, 61 (2019).
Giudice, G. F. The Dawn of the Post-Naturalness Era. In From My Vast Repertoire ...: Guido Altarelli’s Legacy (eds Levy, A. et al.)
267–292 (World Scientific, 2019).
Young, B. L. A survey of dark matter and related topics in cosmology. Front. Phys. (Beijing) 12, 121201 (2017).
Hooper, D. TASI Lectures on Indirect Searches for Dark Matter. PoS TASI2018, 010. arXiv preprint, arXiv:​1812.​02029 (2019).
Gaskins, J. M. A review of indirect searches for particle dark matter. Contemp. Phys. 57, 496–525. https://​doi.​org/​10.​1080/​00107​
514.​2016.​11751​60 (2016).
Masi, N. & Ballardini, M. A conservative assessment of the current constraints on dark matter annihilation from cosmic rays
and CMB observations. Int. J. Mod. Phys. D 26, 1750041. https://​doi.​org/​10.​1142/​S0218​27181​75004​19 (2017).
Wellegehausen, B. H., Wipf, A. & Wozar, C. Phase diagram of the lattice G2 Higgs model. Phys. Rev. D 83, 114502. https://​doi.​
org/​10.​1103/​PhysR​evD.​83.​114502 (2011).
Maas, A. & Wellegehausen, B. H. G2Gauge Theories. PoS LATTICE2012, 080. arXiv preprint, arXiv:​1210.​7950 (2012).
Gursey, F. & Tze, C.-H. On the Role of Division, Jordan, and Related Algebras in Particle Physics (World Scientific, 1996).
Conway, J. H. & Smith, D. A. On Quaternions and Octonions: Their Geometry, Arithmetic, and Symmetry (AK Peters/CRC Press,
2003).
Dixon, G. M. Division Algebras: Octonions, Quaternions, Complex Numbers, and the Algebraic Design of Physics (Kluwer Academic
Publishers, 1994).
Lounesto, P. & London Mathematical Society. Clifford Algebras and Spinors 2nd edn. (Cambridge University Press, 2001).
Gresnigt, N. G. Braids, normed division algebras, and standard model symmetries. Phys. Lett. B 783, 212–221 (2018).
Maia, M. D. Geometry of the Fundamental Interactions (Springer, 2011).
Furey, C. Standard Model Physics from an Algebra? arXiv:​1611.​09182 (2016).
Manogue, C. A. & Dray, T. Octonions, E6, and particle physics. J. Phys: Conf. Ser. 254, 012005. https://​doi.​org/​10.​1088/​1742-​
6596/​254/1/​012005 (2010).
Gording, B. & Schmidt-May, A. The Unified Standard Model. arXiv:​1909.​05641 (2019).
Baez, J. C. The octonions. Bull. Am. Math. Soc. 39, 145–205 (2002).
Daniel, K. Biss. & Daniel Dugger, D. C. I. Large annihilators in Cayley–Dickson algebras. Commun. Algebra 36, 632–664. https://​
doi.​org/​10.​1080/​00927​87070​17240​94 (2008).
Gillard, A. B. & Gresnigt, N. G. Three fermion generations with two unbroken gauge symmetries from the complex sedenions.
Eur. Phys. J. C 79, 1–11. https://​doi.​org/​10.​1140/​epjc/​s10052-​019-​6967-1 (2019).
Cawagas, R. On the structure and zero divisors of the Cayley–Dickson sedenion algebra. Discuss. Math. General Algebra Appl.
24, 251–265 (2004).
Cacciatori, S. L. & Cerchiai, B. L. Exceptional Groups, Symmetric Spaces and Applications. arXiv:​0906.​0121 (2009).
Evans, J. Supersymmetric Yang–Mills theories and division algebras. Nuclear Phys. B 298, 92–108 (1988).
Schwerdtfeger, H. Geometry of Complex Numbers: Circle Geometry, Moebius Transformation, Non-Euclidean Geometry (Dover
Publications, 1979).
Schwichtenberg, J. Physics from Symmetry 2nd edn. (Springer, 2018).
Nath, P. Supersymmetry, Supergravity, and Unification (Cambridge University Press, 2017). https://​doi.​org/​10.​1017/​97811​39048​
118.
Burgess, C. P. & Moore, G. D. The Standard Model: A Primer (Cambridge University Press, 2012).
Schwinger, J. Particles, Sources, and Fields Vol. 1 (Taylor and Francis Ltd, 2018).
Field, M. Dynamics and Symmetry (London Imperial College Press, 2007).
Saller, H. Operational Symmetries: Basic Operations in Physics (Springer, 2017).
Aguilar, M. A. & Socolovsky, M. On the topology of the symmetry group of the standard model. Int. J. Theor. Phys. 38, 2485–2509
(1999).
Yale, P. B. Automorphisms of the complex numbers. Math. Mag. 39, 135–141. https://​doi.​org/​10.​1080/​00255​70X.​1966.​11975​699
(1966).
Saller, H. Operational Quantum Theory I: Nonrelativistic Structures (Springer, 2006).
Bialynicki-Birula, I. & Bialynicka-Birula, Z. The role of the Riemann–Silberstein vector in classical and quantum theories of
electromagnetism. J. Phys. A: Math. Theor. 46, 053001. https://​doi.​org/​10.​1088/​1751-​8113/​46/5/​053001 (2013).
Gelfand, I. M., Minlos, R. A. & Ya, S. Z. Representations of the Rotation and Lorentz Groups and Their Applications (Oxford
Pergamon Press; Dover Publications Inc., 1963) (New edition 2018).
Pushpa, T. L., Bisht, P. S. & Negi, O. Quaternion octonion reformulation of grand unified theories. Int. J. Theor. Phys. 51,
3228–3235. https://​doi.​org/​10.​1007/​s10773-​012-​1204-9 (2012).
Potter, F. CKM and PMNS mixing matrices from discrete subgroups of SU(2). J. Phys: Conf. Ser. 631, 012024. https://​doi.​org/​
10.​1088/​2F1742-​6596/​2F631/​2F1/​2F012​024 (2015).
Dray, T. & Manogue, C. A. The Geometry of the Octonions (World Scientific, 2015).
Chanyal, B. C., Bisht, P. S., Li, T. & Negi, O. P. S. Octonion quantum chromodynamics. Int. J. Theor. Phys. 51, 3410–3422. https://​
doi.​org/​10.​1007/​s10773-​012-​1222-7 (2012).
Wilson, R. The Finite Simple Groups (Springer, 2009).
Holland, K., Minkowski, P., Pepe, M. & Wiese, U.-J. Exceptional confinement in G(2) gauge theory. Nuclear Phys. B 668, 207–236.
https://​doi.​org/​10.​1016/​S0550-​3213(03)​00571-6 (2003).
Furey, C. A demonstration that electroweak theory can violate parity automatically (leptonic case). Int. J. Mod. Phys. A 33,
1830005 (2018).
Furey, C. Charge quantization from a number operator. Phys. Lett. B 742, 195–199 (2015).

https://doi.org/10.1038/s41598-021-01814-1

14

## PDF page 15

www.nature.com/scientificreports/
53. Furey, C. SU(3) × SU(2) × U(1)(×U(1)) as a symmetry of division algebraic ladder operators. Eur. Phys. J. C 78, 375. https://​doi.​
org/​10.​1140/​epjc/​s10052-​018-​5844-7 (2018).
54. Furey, C. Unified theory of ideals. Phys. Rev. D 86, 025024. https://​doi.​org/​10.​1103/​PhysR​evD.​86.​025024 (2012).
55. Anastasiou, A., Borsten, L., Duff, M. J., Hughes, L. J. & Nagy, S. Super Yang–Mills, division algebras and triality. J. High Energy
Phys. https://​doi.​org/​10.​1007/​JHEP0​8(2014)​080 (2014).
56. Deligne, P. Quantum Fields and Strings: A Course for Mathematicians (American Mathematical Society, Institute for Advanced
Study, 1999).
57. Green, M. M. B., Schwarz, J. H. & Witten, E. Superstring Theory. Volume 1, Introduction. 25th Anniversary Edition (Cambridge
University Press, 2012).
58. Kugo, T. & Townsend, P. K. Supersymmetry and the division algebras. Nuclear Phys. B 221, 357–380 (1983).
59. Preitschopf, C. R. Octonions and Supersymmetry, in Gauge Theories, Applied Supersymmetry, Quantum Gravity. Proceedings,
Workshop, Leuven, Belgium, July 10–14, 1995, 225–231 (1995).
60. Joyce, D. D. Compact Manifolds with Special Holonomy (Oxford University Press, 2000).
61. Becker, K., Becker, M. & Robbins, D. M-theory and g2 manifolds. Phys. Scr. 90, 118004. https://​doi.​org/​10.​1088/​2F0031-​8949/​
2F90/​2F11/​2F118​004 (2015).
62. Culbert, C. Cayley–Dickson algebras and loops. J. Gener. Lie Theory Appl. 1, 1–17 (2007).
63. Smith, J. A left loop on the 15-sphere. J. Algebra 176, 128–138 (1995).
64. Moreno, R. G. The zero divisors of the Cayley–Dickson algebras over the real numbers. arXiv preprint, arXiv:q-​alg/​97100​13 (1997).
65. Barton, C. H. & Sudbery, A. Magic squares of lie algebras. arXiv preprint, arXiv:​math/​00010​83 (2000).
66. Barton, C. & Sudbery, A. Magic squares and matrix models of lie algebras. Adv. Math. 180, 596–647 (2003).
67. Cacciatori, S. L., Cerchiai, B. L. & Marrani, A. Squaring the magic. Adv. Theor. Math. Phys. 19, 923–954. https://​doi.​org/​10.​4310/​
ATMP.​2015.​v19.​n5.​a1 (2015).
68. Gillard, A. B. & Gresnigt, N. G. TheC𝓁(8)Algebra of Three Fermion Generations with Spin and Full Internal Symmetries. arXiv:​
1906.​05102 (2019).
69. Brown, R. B. On generalized Cayley–Dickson algebras. Pac. J. Math. 20, 415–422 (1967).
70. Eakin, P. & Sathaye, A. On automorphisms and derivations of Cayley–Dickson algebras. J. Algebra 129, 263–278 (1990).
71. Hentzel, I. Identities for algebras obtained from the Cayley–Dickson process. Commun. Algebra 29, 3523–3534 (2000).
72. Kubo, J., Okada, H. & Sakamaki, F. Higgs potential in a minimal S3 invariant extension of the standard model. Phys. Rev. D 70,
036007. https://​doi.​org/​10.​1103/​PhysR​evD.​70.​036007 (2004).
73. Kubo, J. et al. A minimal S3-invariant extension of the standard model. J. Phys: Conf. Ser. 18, 380–384. https://​doi.​org/​10.​1088/​
2F1742-​6596/​2F18/​2F1/​2F013 (2005).
74. Mondragón, A., Mondragón, M. & Peinado, E. Lepton masses, mixings, and flavor-changing neutral currents in a minimal S3
-invariant extension of the standard model. Phys. Rev. D 76, 076003. https://​doi.​org/​10.​1103/​PhysR​evD.​76.​076003 (2007).
75. González, Canales F., Mondragón, A. & Mondragón, M. The S3 flavour symmetry: Neutrino masses and mixings.. Fortschr. Phys.
61, 546–570. https://​doi.​org/​10.​1002/​prop.​20120​0121 (2012).
76. Aschbacher, M. Finite Group Theory 2nd edn. (Cambridge University Press, Cambridge, 2000).
77. Rotman, J. J. Advanced Modern Algebra 3rd edn. (American Mathematical Society, 2015).
78. Muta, T. Foundations of Quantum Chromodynamics: An Introduction to Perturbative Methods in Gauge Theories 3rd edn. (World
Scientific, 2010).
79. Pepe, M. Confinement and the center of the gauge group. Nucl. Phys. B Proc. Suppl. 153, 207–214. https://​doi.​org/​10.​1016/j.​
nuclp​hysbps.​2006.​01.​045 (2006).
80. Wipf, A. Statistical Approach to Quantum Field Theory: An Introduction Vol. 864 (Springer, 2013).
81. Marzocca, D. & Urbano, A. Composite dark matter and LHC interplay. J. High Energy Phys. https://​doi.​org/​10.​1007/​JHEP0​
7(2014)​107 (2014).
82. Da Rold, L. & Rossia, A. N. The minimal simple composite Higgs model. J. High Energy Phys. https://​doi.​org/​10.​1007/​JHEP1​
2(2019)​023 (2019).
83. Cacciapaglia, G., Cai, H., Deandrea, A. & Kushwaha, A. Composite Higgs and dark matter model in SU(6)/SO(6). J. High Energy
Phys. https://​doi.​org/​10.​1007/​JHEP1​0(2019)​035 (2019).
84. Macfarlane, A. J. The sphere S 6 viewed as a G 2 /SU(3) coset space. Int. J. Mod. Phys. A 17, 2595–2613. https://​doi.​org/​10.​1142/​
S0217​751X0​20106​50 (2002).
85. Behrends, R. E., Dreitlein, J., Fronsdal, C. & Lee, W. Simple groups and strong interaction symmetries. Rev. Mod. Phys. 34, 1–40.
https://​doi.​org/​10.​1103/​RevMo​dPhys.​34.1 (1962).
86. Carone, C. D. & Rastogi, A. Exceptional electroweak model. Phys. Rev. D 77, 035011. https://​doi.​org/​10.​1103/​PhysR​evD.​77.​
035011 (2008).
87. Dehghan, Z. & Deldar, S. Cho decomposition, Abelian gauge fixing, and monopoles in G(2) Yang–Mills theory. Phys. Rev. D 99,
116024. https://​doi.​org/​10.​1103/​PhysR​evD.​99.​116024 (2019).
88. Pepe, M. & Wiese, U.-J. Exceptional deconfinement in gauge theory. Nucl. Phys. B 768, 21–37. https://​doi.​org/​10.​1016/j.​nuclp​
hysb.​2006.​12.​024 (2007).
89. Greensite, J., Langfeld, K., Olejník, Š, Reinhardt, H. & Tok, T. Color screening, Casimir scaling, and domain structure in G(2)
and SU(N) gauge theories. Phys. Rev. D 75, 034501. https://​doi.​org/​10.​1103/​PhysR​evD.​75.​034501 (2007).
90. Nejad, S. H. & Deldar, S. Role of the SU(2) and SU(3) subgroups in observing confinement in the G(2) gauge group. Phys. Rev.
D 89, 014510. https://​doi.​org/​10.​1103/​PhysR​evD.​89.​014510 (2014).
91. Wellegehausen, B. H. Phase Diagram of the G(2) Higgs Model and G(2)-QCD. PoS LATTICE2011, 266. arXiv preprint, arXiv:​
1111.​0496 (2011).
92. Adhikary, A., Banerjee, S., Barman, R. K. & Bhattacherjee, B. Resonant heavy Higgs searches at the HL-LHC. J. High Energy
Phys. https://​doi.​org/​10.​1007/​JHEP0​9(2019)​068 (2019).
93. Arhrib, A., Ferreira, P. M. & Santos, R. Are there hidden scalars in LHC Higgs results?. J. High Energy Phys. https://​doi.​org/​10.​
1007/​JHEP0​3(2014)​053 (2014).
94. Banerjee, A., Bhattacharyya, G., Kumar, N. & Ray, T. S. Constraining composite Higgs models using LHC data. J. High Energy
Phys. https://​doi.​org/​10.​1007/​JHEP0​3(2018)​062 (2018).
95. González Canales, F., Mondragón, A., Mondragón, M., Saldaña Salazar, U. J. & Velasco-Sevilla, L. Quark sector of S3 models:
Classification and comparison with experimental data. Phys. Rev. D 88, 096004. https://​doi.​org/​10.​1103/​PhysR​evD.​88.​096004
(2013).
96. Lucini, B., Teper, M. & Wenger, U. The high temperature phase transition in SU(N) gauge theories. J. High Energy Phys. 2004,
061. https://​doi.​org/​10.​1088/​1126-​6708/​2004/​01/​061 (2004).
97. Nada, A. Universal Aspects in the Equation of State for Yang–Mills Theories. PoS EPS-HEP2015, 373. arXiv preprint, arXiv:​1510.​
01146 (2015).
98. Lucini, B. & Panero, M. Introductory lectures to large-QCD phenomenology and lattice results. Prog. Part. Nucl. Phys. 75, 1–40.
https://​doi.​org/​10.​1016/j.​ppnp.​2014.​01.​001 (2014).
99. Teper, M. Large N and confining flux tubes as strings—A view from the lattice. Acta Phys. Polon. B 40, 3249–3320 (2009).

Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

15
Vol.:(0123456789)

## PDF page 16

www.nature.com/scientificreports/
100. Panero, M. Thermodynamics of the QCD plasma and the large-N limit. Phys. Rev. Lett. 103, 232001. https://​doi.​org/​10.​1103/​
PhysR​evLett.​103.​232001 (2009).
101. Cossu, G., DElia, M., Giacomo, A. D., Lucini, B. & Pica, C. G2 gauge theory at finite temperature. J. High Energy Phys. 2007,
100. https://​doi.​org/​10.​1088/​1126-​6708/​2007/​10/​100 (2007).
102. von Smekal, L., Wellegehausen, B. H., Maas, A. & Wipf, A. G2-QCD: Spectroscopy and the Phase Diagram at Zero Temperature
and Finite Density. PoS LATTICE2013, 186. arXiv preprint, arXiv:​1310.​7745 (2014).
103. Bruno, M., Caselle, M., Panero, M. & Pellegrini, R. Exceptional thermodynamics: The equation of state of G(2) gauge theory. J.
High Energy Phys. 2015, 57 (2014).
104. Cutting, D., Hindmarsh, M. & Weir, D. J. Gravitational waves from vacuum first-order phase transitions: From the envelope to
the lattice. Phys. Rev. D 97, 123513. https://​doi.​org/​10.​1103/​PhysR​evD.​97.​123513 (2018).
105. Schwaller, P. Gravitational waves from a dark phase transition. Phys. Rev. Lett. 115, 181101. https://​doi.​org/​10.​1103/​PhysR​evLett.​
115.​181101 (2015).
106. Zhou, R., Yang, J. & Bian, L. Gravitational waves from first-order phase transition and domain wall. J. High Energy Phys. https://​
doi.​org/​10.​1007/​JHEP0​4(2020)​071 (2020).
107. Zhang, Z. et al. Phase transition gravitational waves from pseudo-Nambu-Goldstone dark matter and two Higgs doublets. J.
High Energy Phys. 2021, 160 (2021) (2102.01588.).
108. Wellegehausen, B., Maas, A., Wipf, A. & Von Smekal, L. Hadron masses and baryonic scales in G2-QCD at finite density. Phys.
Rev. D 89, 056007 (2014).
109. Hajizadeh, O. & Maas, A. Constructing a neutron star from the lattice in G2-QCD. Eur. Phys. J. A 53, 1–13. https://​doi.​org/​10.​
1140/​epja/​i2017-​12398-x (2017).
110. Juknevich, J., Melnikov, D. & Strassler, M. A pure-glue hidden valley I. States and decays. J. High Energy Phys. 2009, 055. https://​
doi.​org/​10.​1088/​1126-​6708/​2009/​07/​055 (2009).
111. Juknevich, J. E. Pure-glue hidden valleys through the Higgs portal. JHEP 08, 121. https://​doi.​org/​10.​1007/​JHEP0​8(2010)​121
(2010).
112. Boddy, K. K., Feng, J. L., Kaplinghat, M. & Tait, T. M. Self-interacting dark matter from a non-Abelian hidden sector. Phys. Rev.
D 89, 115017. https://​doi.​org/​10.​1103/​PhysR​evD.​89.​115017 (2014).
113. Yamanaka, N., Fujibayashi, S., Gongyo, S. & Iida, H. Dark Matter in the Hidden Gauge Theory. arXiv:​1411.​2172 (2014).
114. Klinkhamer, F. R. Gluon condensate, modified gravity, and the accelerating universe. Phys. Rev. D 81, 043006. https://​doi.​org/​
10.​1103/​PhysR​evD.​81.​043006 (2010).
115. Ballesteros, G., Carmona, A. & Chala, M. Exceptional composite dark matter. Eur. Phys. J. C 77, 1–18. https://​doi.​org/​10.​1140/​
epjc/​s10052-​017-​5040-1 (2017).
116. Koorambas, E. Vector gauge Boson dark matter for the SU(N) gauge group model. Int. J. Theor. Phys. 52, 4374–4388 (2013).
117. Yukawa, E. & Ueda, M. Hydrodynamic description of spin-1 Bose-Einstein condensates. Phys. Rev. A 86, 063614. https://​doi.​
org/​10.​1103/​PhysR​evA.​86.​063614 (2012).
118. Forestell, L., Morrissey, D. E. & Sigurdson, K. Cosmological bounds on non-Abelian dark forces. Phys. Rev. D 97, 075029. https://​
doi.​org/​10.​1103/​PhysR​evD.​97.​075029 (2018).
119. Soni, A. & Zhang, Y. Gravitational waves from SU(N) glueball dark matter. Phys. Lett. B 771, 379–384 (2017).
120. West, G. B. Theorem on the lightest glueball state. Phys. Rev. Lett. 77, 2622–2625. https://​doi.​org/​10.​1103/​PhysR​evLett.​77.​2622
(1996).
121. Ahriche, A., McDonald, K. L., Nasri, S. & Toma, T. A model of neutrino mass and dark matter with an accidental symmetry.
Phys. Lett. B 746, 430–435 (2015) (1504.05755).
122. Bernal, N. & Chu, X. Z2 SIMP dark matter. J. Cosmol. Astropart. Phys. 2016, 006. https://​doi.​org/​10.​1088/​1475-​7516/​2016/​01/​
006 (2016).
123. Branco, G. et al. Theory and phenomenology of two-Higgs-doublet models. Phys. Rep. 516, 1–102. https://​doi.​org/​10.​1016/j.​
physr​ep.​2012.​02.​002 (2012).
124. Yaguna, C. E. & Zapata, Ó. Multi-component scalar dark matter from a ZN symmetry: A systematic analysis. J. High Energy Phys.
https://​doi.​org/​10.​1007/​JHEP0​3(2020)​109 (2020).
125. Bai, Y. & Hill, R. J. Weakly interacting stable hidden sector pions. Phys. Rev. D 82, 111701. https://​doi.​org/​10.​1103/​PhysR​evD.​
82.​111701 (2010).
126. Rinaldi, M. & Vento, V. Scalar and tensor glueballs as gravitons. Eur. Phys. J. A 54, 1–7. https://​doi.​org/​10.​1140/​epja/​i2018-​
12600-9 (2018).
127. Quiros, I. Selected topics in scalar-tensor theories and beyond. Int. J. Mod. Phys. D 28, 1930012. https://​doi.​org/​10.​1142/​S0218​
27181​93001​2X (2019).
128. Akrami, Y., Hassan, S., Könnig, F., Schmidt-May, A. & Solomon, A. R. Bimetric gravity is cosmologically viable. Phys. Lett. B
748, 37–44. https://​doi.​org/​10.​1016/j.​physl​etb.​2015.​06.​062 (2015).
129. Babichev, E. et al. Bigravitational origin of dark matter. Phys. Rev. D 94, 084055. https://​doi.​org/​10.​1103/​PhysR​evD.​94.​084055
(2016).
130. Babichev, E. et al. Heavy spin-2 dark matter. J. Cosmol. Astropart. Phys. 2016, 016. https://​doi.​org/​10.​1088/​1475-​7516/​2016/​09/​
016 (2016).
131. Giacosa, F. Heavy glueballs: Status and large-Nc widths estimate. Acta Phys. Polon. Supp. 10, 1021–1027 (2017).
132. Lucini, B. Glueballs from the Lattice. PoS QCD-TNT-III, 023. arXiv preprint, arXiv:​1401.​1494 (2013).
133. da Rocha, R. Dark SU(N) glueball stars on fluid branes. Phys. Rev. D 95, 124017. https://​doi.​org/​10.​1103/​PhysR​evD.​95.​124017
(2017).
134. Aghanim, N. et al. Planck 2018 Results. VI. Cosmological Parameters. arXiv:​1807.​06209 (2018).
135. Bernal, N., Heikinheimo, M., Tenkanen, T., Tuominen, K. & Vaskonen, V. The dawn of FIMP dark matter: A review of models
and constraints. Int. J. Mod. Phys. A 32, 1730023. https://​doi.​org/​10.​1142/​S0217​751X1​73002​3X (2017).
136. Hall, L. J., Jedamzik, K., March-Russell, J. & West, S. M. Freeze-in production of FIMP dark matter. J. High Energy Phys. https://​
doi.​org/​10.​1007/​JHEP0​3(2010)​080 (2010).
137. Bernal, N., Cosme, C. & Tenkanen, T. Phenomenology of self-interacting dark matter in a matter-dominated universe. Eur. Phys.
J. C 79, 1–19. https://​doi.​org/​10.​1140/​epjc/​s10052-​019-​6608-8 (2019).
138. Yamanaka, N., Iida, H., Nakamura, A. & Wakayama, M. Glueball scattering cross section in lattice SU(2) Yang–Mills theory.
Phys. Rev. D 102, 054507. https://​doi.​org/​10.​1103/​PhysR​evD.​102.​054507 (2020).
139. Soni, A. & Zhang, Y. Hidden SU(N) glueball dark matter. Phys. Rev. D 93, 115025. https://​doi.​org/​10.​1103/​PhysR​evD.​93.​115025
(2016).
140. Enqvist, K., Hardwick, R. J., Tenkanen, T., Vennin, V. & Wands, D. A novel way to determine the scale of inflation. J. Cosmol.
Astropart. Phys. 2018, 006. https://​doi.​org/​10.​1088/​1475-​7516/​2018/​02/​006 (2018).
141. Bernal, N., Chu, X., Garcia-Cely, C., Hambye, T. & Zaldivar, B. Production regimes for self-interacting dark matter. J. Cosmol.
Astropart. Phys. 2016, 018. https://​doi.​org/​10.​1088/​1475-​7516/​2016/​03/​018 (2016).
142. Heikinheimo, M., Tenkanen, T., Tuominen, K. & Vaskonen, V. Observational constraints on decoupled hidden sectors. Phys.
Rev. D 94, 063506 (2016) [Erratum: Phys. Rev. D 96, 109902 (2017)], 1604.02401.

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

16

## PDF page 17

www.nature.com/scientificreports/
143. Choi, S.-M., Lee, H. M. & Seo, M.-S. Cosmic abundances of SIMP dark matter. J. High Energy Phys. https://​doi.​org/​10.​1007/​
JHEP0​4(2017)​154 (2017).
144. Forestell, L., Morrissey, D. E. & Sigurdson, K. Non-Abelian dark forces and the relic densities of dark glueballs. Phys. Rev. D 95,
015032. https://​doi.​org/​10.​1103/​PhysR​evD.​95.​015032 (2017).
145. Bhattacharya, S., Ghosh, P. & Verma, S. Simpler realisation of scalar dark matter. J. Cosmol. Astropart. Phys. 2020, 040. https://​
doi.​org/​10.​1088/​1475-​7516/​2020/​01/​040 (2020).
146. Choi, S.-M., Kim, J., Lee, H. M. & Zhu, B. Connecting between inflation and dark matter in models with gauged Z 3 symmetry.
JHEP 06, 135. https://​doi.​org/​10.​1007/​JHEP0​6(2020)​135 (2020).
147. Samir Acharya, B., Fairbairn, M. & Hardy, E. Glueball dark matter in non-standard cosmologies. arXiv e-prints, arXiv:​1704.​
01804 (2017).
148. Allahverdi, R. & Drees, M. Production of massive stable particles in inflaton decay. Phys. Rev. Lett. 89, 091302. https://​doi.​org/​
10.​1103/​PhysR​evLett.​89.​091302 (2002).
149. Almeida, J. P. B., Bernal, N., Rubio, J. & Tenkanen, T. Hidden inflation dark matter. JCAP 03, 012. https://​doi.​org/​10.​1088/​1475-​
7516/​2019/​03/​012 (2019).
150. de la Macorra, A. Dark matter from the inflaton field. Astropart. Phys. 35, 478–484. https://​doi.​org/​10.​1016/j.​astro​partp​hys.​
2011.​11.​009 (2012).
151. Heurtier, L. & Huang, F. Inflaton portal to a highly decoupled EeV dark matter particle. Phys. Rev. D 100, 043507. https://​doi.​
org/​10.​1103/​PhysR​evD.​100.​043507 (2019).
152. Mirza, B. & Mohammadzadeh, H. Condensation of an ideal gas obeying non-Abelian statistics. Phys. Rev. E 84, 031114. https://​
doi.​org/​10.​1103/​PhysR​evE.​84.​031114 (2011).
153. Harko, T. Cosmological dynamics of dark matter Bose-Einstein condensation. Phys. Rev. D 83, 123515. https://​doi.​org/​10.​1103/​
PhysR​evD.​83.​123515 (2011).
154. Sharma, A., Khoury, J. & Lubensky, T. The equation of state of dark matter superfluids. JCAP 1905, 054. https://​doi.​org/​10.​1088/​
1475-​7516/​2019/​05/​054 (2019).
155. Ferreira, E. G., Franzmann, G., Khoury, J. & Brandenberger, R. Unified superfluid dark sector. J. Cosmol. Astropart. Phys. 2019,
027. https://​doi.​org/​10.​1088/​1475-​7516/​2019/​08/​027 (2019).
156. Kuster, M. M., Beltran, B. B. & Raffelt, G. G. Axions: Theory, Cosmology, and Experimental Searches (Springer, 2010).
157. Proukakis, S. D. W., Nick, P. & Littlewood, P. B. Universal Themes of Bose-Einstein Condensation (Cambridge University Press,
2017).
158. Balhmer, C. G. & Harko, T. Can dark matter be a Bose–Einstein condensate?. J. Cosmol. Astropart. Phys. 2007, 025. https://​doi.​
org/​10.​1088/​1475-​7516/​2007/​06/​025 (2007).
159. Chavanis, P.-H. Dissipative self-gravitating Bose–Einstein condensates with arbitrary nonlinearity as a model of dark matter
halos. Eur. Phys. J. Plus 132, 248. https://​doi.​org/​10.​1140/​epjp/​i2017-​11544-3 (2017).
160. Sanchis-Gual, N. et al. Nonlinear dynamics of spinning bosonic stars: Formation and stability. Phys. Rev. Lett. 123, 221101.
https://​doi.​org/​10.​1103/​PhysR​evLett.​123.​221101 (2019).
161. Eby, J., Kouvaris, C., Nielsen, N. G. & Wijewardhana, L. C. R. Boson stars from self-interacting dark matter. JHEP 02, 028. https://​
doi.​org/​10.​1007/​JHEP0​2(2016)​028 (2016).
162. Liebling, S. L. & Palenzuela, C. Dynamical boson stars. Living Rev. Relativ. 20(5), 2017. https://​doi.​org/​10.​1007/​s41114-​017-​
0007-y (2017).
163. Brito, R., Cardoso, V., Herdeiro, C. A. R. & Radu, E. Proca stars: Gravitating Bose–Einstein condensates of massive spin 1 particles. Phys. Lett. B 752, 291–295. https://​doi.​org/​10.​1016/j.​physl​etb.​2015.​11.​051 (2016).
164. Landea, I. S. & García, F. Charged Proca stars. Phys. Rev. D 94, 104006. https://​doi.​org/​10.​1103/​PhysR​evD.​94.​104006 (2016).
165. Minamitsuji, M. Vector Boson star solutions with a quartic order self-interaction. Phys. Rev. D 97, 104023. https://​doi.​org/​10.​
1103/​PhysR​evD.​97.​104023 (2018).
166. Chavanis, P.-H. & Harko, T. Bose–Einstein condensate general relativistic stars. Phys. Rev. D 86, 064011. https://​doi.​org/​10.​1103/​
PhysR​evD.​86.​064011 (2012).
167. Cardoso, V. & Pani, P. Testing the nature of dark compact objects: A status report. Living Rev. Relativ. 22, 4. https://​doi.​org/​10.​
1007/​s41114-​019-​0020-4 (2019).
168. Hertzberg, M. P., Rompineve, F. & Yang, J. Decay of boson stars with application to glueballs and other real scalars. Phys. Rev.
D 103, 023536. https://​doi.​org/​10.​1103/​PhysR​evD.​103.​023536 (2021).
169. Calcino, J., Garcia-Bellido, J. & Davis, T. M. Updating the MACHO fraction of the Milky Way dark halo with improved mass
models. Mon. Not. R. Astron. Soc. 479, 2889–2905. https://​doi.​org/​10.​1093/​mnras/​sty13​68 (2018).
170. Brandt, T. D. Constraints on MACHO dark matter from compact stellar systems in ultra-faint dwarf galaxies. Astrophys. J. Lett.
824, L31. https://​doi.​org/​10.​3847/​2041-​8205/​824/2/​L31 (2016).
171. Harvey, D., Robertson, A., Massey, R. & McCarthy, I. G. Observable tests of self-interacting dark matter in galaxy clusters: BCG
wobbles in a constant density core. Mon. Not. R. Astron. Soc. 488, 1572–1579. https://​doi.​org/​10.​1093/​mnras/​stz18​16 (2019).
172. Bernal, N., Chu, X., Kulkarni, S. & Pradler, J. Self-interacting dark matter without prejudice. Phys. Rev. D 101, 055044. https://​
doi.​org/​10.​1103/​PhysR​evD.​101.​055044 (2020).
173. Robertson, A., Massey, R. & Eke, V. What does the bullet cluster tell us about self-interacting dark matter?. Mon. Not. R. Astron.
Soc. 465, 569–587. https://​doi.​org/​10.​1093/​mnras/​stw26​70 (2016).
174. Ohnishi, A., Ueda, H., Nakano, T. Z., Ruggieri, M. & Sumiyoshi, K. Possibility of QCD critical point sweep during black hole
formation. Phys. Lett. B 704, 284–290. https://​doi.​org/​10.​1016/j.​physl​etb.​2011.​09.​018 (2011).
175. Critelli, R. et al. Critical point in the phase diagram of primordial quark-gluon matter from black hole physics. Phys. Rev. D 96,
096026. https://​doi.​org/​10.​1103/​PhysR​evD.​96.​096026 (2017).

Author contributions

I, N.M., am the only and corresponding author of the manuscript, which comes from a long and deep study and
chain of reasoning that lasted many years. This is a personal and thoughtful product of my ten-year activity in
the dark matter indirect search and phenomenology field.

Competing interests

The author declares no competing interests.

Additional information

Correspondence and requests for materials should be addressed to N.M.
Reprints and permissions information is available at www.nature.com/reprints.

Scientific Reports |

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

17
Vol.:(0123456789)

## PDF page 18

www.nature.com/scientificreports/
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in published maps and
institutional affiliations.
Open Access This article is licensed under a Creative Commons Attribution 4.0 International
License, which permits use, sharing, adaptation, distribution and reproduction in any medium or
format, as long as you give appropriate credit to the original author(s) and the source, provide a link to the
Creative Commons licence, and indicate if changes were made. The images or other third party material in this
article are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the
material. If material is not included in the article’s Creative Commons licence and your intended use is not
permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this licence, visit http://​creat​iveco​mmons.​org/​licen​ses/​by/4.​0/.
© The Author(s) 2021

Scientific Reports |
Vol:.(1234567890)

(2021) 11:22528 |

https://doi.org/10.1038/s41598-021-01814-1

18
