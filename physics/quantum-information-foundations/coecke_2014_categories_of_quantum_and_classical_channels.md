Source: https://doi.org/10.4204/EPTCS.158.1
PDF sha256: bc99cf31842013b21a55386a6c52a52824f452b39590a1c4356021d073dbd47a
License: CC BY-NC, version not stated
Language: eng
Fidelity: machine-gated

# Transcription of coecke_2014_categories_of_quantum_and_classical_channels.pdf

Transcription of `coecke_2014_categories_of_quantum_and_classical_channels.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Categories of Quantum and Classical Channels
(extended abstract)
Bob Coecke∗

Chris Heunen†

Aleks Kissinger∗

University of Oxford, Department of Computer Science
{coecke,heunen,alek}@cs.ox.ac.uk

We introduce the CP*–construction on a dagger compact closed category as a generalisation of
Selinger’s CPM–construction. While the latter takes a dagger compact closed category and forms
its category of “abstract matrix algebras” and completely positive maps, the CP*–construction forms
its category of “abstract C*-algebras” and completely positive maps. This analogy is justified by
the case of finite-dimensional Hilbert spaces, where the CP*–construction yields the category of
finite-dimensional C*-algebras and completely positive maps.
The CP*–construction fully embeds Selinger’s CPM–construction in such a way that the objects
in the image of the embedding can be thought of as “purely quantum” state spaces. It also embeds
the category of classical stochastic maps, whose image consists of “purely classical” state spaces. By
allowing classical and quantum data to coexist, this provides elegant abstract notions of preparation,
measurement, and more general quantum channels.

1

Introduction

One of the motivations driving categorical treatments of quantum mechanics is to place classical and
quantum systems on an equal footing in a single category, so that one can study their interactions. The
main idea of categorical quantum mechanics [1] is to fix a category (usually dagger compact) whose objects are thought of as state spaces and whose morphisms are evolutions. There are two main variations.
• “Dirac style”: Objects form pure state spaces, and isometric morphisms form pure state evolutions.
• “von Neumann style”: Objects form spaces of mixed states, and morphisms form mixed quantum
evolutions, also known as quantum channels.
The prototypical example of a “Dirac style” category is FHilb, the category of finite-dimensional
Hilbert spaces and linear maps. One can pass to a “von Neumann style category” by considering the C*algebras of operators on these Hilbert spaces, with completely positive maps between them. Selinger’s
CPM–construction provides an abstract bridge from the former to the latter [18], turning morphisms in
V into quantum channels in CPM[V]. However, this passage loses the connection between quantum and
classical channels. For example, CPM[FHilb] only includes objects corresponding to the entire state
space of some quantum system, whereas we would often like to focus in subspaces corresponding to
particular classical contexts. There have been several proposals to remedy this situation, which typically
involve augmenting CPM[V] with extra objects to carry this classical structure. Section 1.1 provides an
overview.
This extended abstract1 introduces a new solution to this problem, called the CP*–construction,
which is closer in spirit to the study of quantum information using C*-algebras (see e.g. [15]). Rather than
∗ Supported by the John Templeton Foundation.
† Supported by EPSRC Fellowship EP/L002388/1.
1 A long version of this extended abstract is now available: [8].

R. Duncan and P. Panangaden (Eds.)
Quantum Physics and Logic 2012 (QPL2012)
EPTCS 158, 2014, pp. 1–14, doi:10.4204/EPTCS.158.1

c
⃝ B. Coecke, C. Heunen & A. Kissinger
This work is licensed under the Creative Commons
Attribution-Noncommercial License.

## PDF page 2

2

Categories of Quantum and Classical Channels

freely augmenting a category of quantum data with classical objects, we define a new category whose
objects are “abstract C*–algebras”, and whose morphisms are the analogue of completely positive maps.
It is then possible to construct a full embedding of the category CPM[V], whose image yields the purely
quantum channels. Furthermore, there exists another full embedding of the category Stoch[V] of classical
stochastic maps, whose image yields the purely classical channels. The remainder of the category CP∗ [V]
can be interpreted as mixed classical/quantum state spaces, which carry partially coherent quantum states,
such as degenerate quantum measurement outcomes.
/ CPM[V]

V

full, faithful

/ CP∗ [V] o

full, faithful

Stoch[V]

The paper is structured as follows. Section 2 introduces normalisable dagger Frobenius algebras.
These form a crucial ingredient to the CP*–construction, which is defined in Section 3. Sections 4
and 5 then show that the CP*–construction simultaneously generalises Selinger’s CPM–construction,
consisting of “quantum channels”, and the Stoch–construction, consisting of “classical channels”. We
then consider two examples: Section 6 shows that CP∗ [FHilb] is the category of finite- dimensional
C*-algebras and completely positive maps, and Section 7 shows that CP∗ [Rel] is the category of (small)
groupoids and inverse-respecting relations. Section 8 compares CP∗ [V] with Selinger’s extension of the
CPM–construction using split idempotents. Finally, Section 9 discusses the many possibilities this opens
up.

1.1

Related Work

Selinger introduced two approaches to add classical data to CPM[V] by either freely adding biproducts
to CPM[V] or freely splitting the †-idempotents of CPM[V] [19]. These new categories are referred to as
CPM[V]⊕ and Split† [CPM[V]], respectively.
When V = FHilb, both categories provide “enough space” to reason about classical and quantum data, as any finite-dimensional C*–algebra can be defined as a sum of matrix algebras (as in
CPM[FHilb]⊕ ) or as a certain orthogonal subspace of a larger matrix algebra (as in Split† [CPM[FHilb]]).
However, it is unclear whether the second construction captures too much: its may contain many more
objects than simply mixtures of classical and quantum state spaces [19, Remark 4.9]. On the other hand,
when V ̸= FHilb, the category CPM[FHilb]⊕ may be too small. That is, there may be interesting objects
that are not just sums of quantum objects.
For this reason, it is interesting to study CP∗ [V], as it lies between these two constructions:
CPM[V]⊕

full, faithful

/ CP∗ [V]

full, faithful

/ Split† [CPM[V]]

The first embedding is well-defined whenever V has biproducts, and the second when V satisfies a
technical axiom about square roots (see Definition 8.2). In the former case, CP∗ [V] inherits biproducts
from V, so it is possible to lift the embedding of CPM[V] by the universal property of the free biproduct
completion; this will be proved in detail in a subsequent paper. In the latter case, one can always construct
the associated dagger-idempotent of an object in CP∗ [V], and (with the assumption from Definition 8.2),
the notions of complete positivity in CP∗ [V] and Split† [CPM[V]] coincide. We provide the details of this
construction in Section 8.
A third approach by Coecke, Paquette, and Pavlovic is similar to ours in that it makes use of commutative Frobenius algebras to represent classical data [9]. As in the previous two approaches, it takes
CPM[V] and freely adds classical structure, this time by forming the comonad associated with a particular commutative Frobenius algebra and taking the Kleisli category. All such categories are then glued

## PDF page 3

B. Coecke, C. Heunen & A. Kissinger

3

together by Grothendieck construction. The CP*–construction was originally conceived as a way to
simplify this approach and overcome is limitations.

2

Abstract C*-algebras

This section defines so-called normalisable dagger Frobenius algebras, which will play a central role in
the CP*-construction of the next section. We start by recalling the notion of a Frobenius algebra. For an
introduction to dagger (compact) categories and their graphical calculus, we refer to [1, 20].
Definition 2.1. A Frobenius algebra is an object A in a monoidal category together with morphisms
depicted as
, ,
and on it satisfying the following diagrammatic equations.
=

=

=
=

=

=

=

=

Any Frobenius algebra defines a cap and a cup that satisfy the snake equation.
:=

=

:=

Definition 2.2. A Frobenius algebra is symmetric when

=

=
and

=

.

In a dagger compact category V, a dagger Frobenius algebra is a Frobenius algebra that satisfies
= ( )† and = ( )† . Their import for us starts with the following theorem.
Theorem 2.3 ([21]). Given a dagger Frobenius algebra (A,
A the structure of a C*-algebra.
(
)⋆
v†
:=
v

) in FHilb, the following operation gives

Furthermore, all finite-dimensional C*-algebras arise this way.
In light of this theorem, one might be tempted to consider dagger Frobenius algebras to be the
“correct” way to define the abstract analogue of finite-dimensional C*-algebras. However, there is one
more condition, called normalisability, that is satisfied by all dagger Frobenius algebras in FHilb, yet
not by dagger Frobenius algebras in general. Before we come to that, we introduce the notion of a central
map for a monoid.
Definition 2.4. A map z : A → A is central for a monoid when

◦ (z ⊗ 1A ) = z ◦

=

◦ (1A ⊗ z).

We call such a map central, because it corresponds uniquely to a point pz : I → A in the centre of the
monoid via left (or equivalently right) multiplication by pz .
Recall that a map g : A → A in a dagger category is positive when g = h† ◦ h for some map h. It is
called positive definite when it is a positive isomorphism. Using these conditions, we give the definition
of a normalisability as a well-behavedness property of the “loop” map
◦ .
Definition 2.5. A dagger Frobenius algebra is normalisable when there is a central, positive-definite
map z, called the normaliser and depicted as , satisfying the following diagrammatic equation.

## PDF page 4

4

Categories of Quantum and Classical Channels

=
Special dagger Frobenius algebras are normalisable dagger Frobenius algebra where z2 = 1A . Normalisable dagger Frobenius algebras are always symmetric.
Theorem 2.6. Normalisable dagger Frobenius algebras are symmetric.
Proof. The proof follows from expanding the counit and applying cyclicity of the trace (∗).

(∗)

=

=

=

=

=

=

=

Definition 2.7. An object X in a dagger compact category is positive-dimensional if there is a posiz

tive definite scalar z satisfying
X

z

=
X

. A dagger compact closed category is called
X

positive-dimensional if all its objects are.
Proposition 2.8. For a positive-dimensional dagger compact closed category V, every object of the form
A∗ ⊗ A carries a canonical normalisable dagger Frobenius algebra, given as follows.

Proof. The Frobenius axioms follow immediately from compact closure. By positive-dimensionality,
there exists a positive-definite scalar z such that (z2 ◦ TrA (1A )) ⊗ 1A = 1A . It is then possible to show that
1A∗ ⊗A ⊗ z is the normaliser.
From now on, we will always take V to be positive-dimensional.

3

The CP*–construction

This section defines the CP*–construction. In fact, defining it is easy; most work goes into proving that it
yields a dagger compact category. For the definition we need some (graphical) notation, generalising the
left and right regular actions A ↦→ End(A) given by x ↦→ x · (−) and x ↦→ (−) · x for a finite-dimensional
algebra A. More generally, for a monoid (A, ) in a compact category, define its left and right action
maps A → A∗ ⊗ A as follows.

Similarly, we can define for any comonoid left and right coaction maps. By convention, we work primarily with right action and coaction maps, and express them more succinctly as follows.
:=

:=

## PDF page 5

B. Coecke, C. Heunen & A. Kissinger

5

Definition 3.1. Let V be a dagger compact category. Objects of CP∗ [V] are normalizable dagger Frobenius algebras in V. Morphisms from (A, ) to (B, ) in CP∗ [V] are morphisms f : A → B in V such
that there exists an object X and g : A → X ⊗ B in V satisfying the following equation.

=

f

g∗

g

(1)

Composition and identities are inherited from V.
Equation (1) is called the CP*–condition. We first establish that CP∗ [V] is a well-defined category.
=

Lemma 3.2. Any symmetric Frobenius algebra satisfies

.

Proof. We can use symmetry to prove the result.

=

=

=

=

=

=

=

Lemma 3.3. Any normalisable dagger Frobenius algebra satisfies

.

Proof. Follows from Frobenius equations and a trace identity (∗) for symmetric Frobenius algebras.
(∗)

=

=

=

=

=

=

=

These lemmas can express the CP*–condition in the sometimes more convenient “convolution form”.
Proposition 3.4. Let V be a dagger compact category, (A,
Frobenius algebras, and f : A → B a morphism.

∃g.

f

=

Proof. For (⇒), apply (
For (⇐), apply ( ◦ − ◦

g∗

g

⇔

) and (B,

∃h.

f

=

) be normalisable dagger

h∗

h

◦−◦
) to both sides and use Lemma 3.3 and properties of normalisers.
) to both sides and apply Lemma 3.2.

Theorem 3.5. If V is a dagger compact category V, so is CP∗ [V].

## PDF page 6

6

Categories of Quantum and Classical Channels

in (1) does the
Proof. Identity maps 1A : (A, ) → (A, ) satisfy the CP∗ -condition: letting g =
job by Lemma 3.2, whose left-hand side is ◦ 1A ◦ .
Next, suppose f : (A, ) → (B, ) and g : (B, ) → (C, ) satisfy the CP*–condition. It then
follows from Lemma 3.3 that their composition does, too.

g

i∗

i∗

i

i

g

=

=

=

f
h∗

f

h∗

h

h

For the monoidal structure, take (A, ) ⊗ (B, ) := (A ⊗ B,
(C, ∗ ) and g : (B, ) → (D, ∗ ) satisfying (1), also f ⊗ g : (A ⊗ B,
fies the CP*–condition. This can be seen by applying the coaction of
decomposing f into h∗ , h and g into i∗ , i, as follows.
∗

∗

). For maps f : (A, ) →
) → (C ⊗ D, ∗ ∗ ) satisand the action of ∗ ∗ , then

∗
∗

f

g

=

f

g

=
i∗

h∗

h

i

As for the tensor unit, note that I := (I, ρI ) is a normalisable dagger Frobenius algebra by monoidal
coherence in V. Using this definition of ⊗ and I, the monoidal structure maps α, λ , and ρ from V
trivially satisfy the CP*–condition. Thus CP∗ [V] is a monoidal category. CP∗ [V] inherits the dagger
from V. Symmetry and dual maps in V lift to the following morphisms in CP∗ [V].
σA,B : (A ⊗ B,

) → (B ⊗ A,

)

eA∗ : (A,

) ⊗ (A∗ ,

)→I

The Frobenius identities and Lemma 3.2 establish the CP*–condition for these maps.
We refer to a morphism I → (A, ) of CP∗ [V] as a positive element of (A, ). Another way to
express the CP*–condition for a V-morphism is to say that it preserves the property of being a positive
element when applied to a some subsystem, as in the following theorem. This will be useful to connect
to the traditional notion of complete positivity of linear maps between C*-algebras.
Theorem 3.6. Let (A, ) and (B, ) be normalisable dagger Frobenius algebras and f : A → B a
morphism in a dagger compact category V. The following are equivalent:
(a) f satisfies the CP*–condition;
(b) postcomposing with f ⊗ 1C sends positive elements of (A, ) ⊗ (C,
(B, ) ⊗ (C, ) for all dagger normalisable Frobenius algebras (C,

) to positive elements of
);

## PDF page 7

B. Coecke, C. Heunen & A. Kissinger

7
) ⊗ (X ∗ ⊗ X,

(c) postcomposing with f ⊗ 1X ∗ ⊗X sends positive elements of (A,
ments of (B, ) ⊗ (X ∗ ⊗ X,
) for all objects X in V.

) to positive ele-

Proof. For (a) ⇒ (b): if ρ is a positive element of (A, ) ⊗ (C, ) and f satisfies the CP*–condition,
then so does ( f ⊗ 1C ) ◦ ρ, by Theorem 3.5. The implication (b) ⇒ (c) is trivial. Finally, for (c) ⇒ (a),
take (C, ) = (A∗ ,
). The action map
: (C, ) → (C∗ ⊗C,
) is a morphism in CP∗ [V]. As a
).
consequence of this fact and Theorem 3.5, the following is a positive element of (A, )⊗(X ∗ ⊗X,
=
ρ

So, by assumption, ( f ⊗ 1A∗ ) ◦ ρ is also a positive element. Applying white caps to both sides finishes
the proof.

f

=

g∗

⇒

g

=

f

g∗

g

See also [8, Proposition 3.4].

4

Embedding Selinger’s CPM–construction

This section will concentrate on the “purely quantum” objects in CP∗ [V], by proving that the latter embeds CPM[V] in a full, faithful, and strongly dagger symmetric monoidal way. First, we recall Selinger’s
CPM–construction [18].
Definition 4.1. For a dagger compact category V, form the dagger compact category CPM[V] as follows.
Objects are the same as those in V, and morphisms f ∈ CPM[V](A, B) are V-morphisms f : A∗ ⊗ A →
B∗ ⊗ B for which there is g : A → X ⊗ B satisfying the following condition.
=

f

g∗

g

Composition, identity maps, and ⊗ on objects are defined as in V. On morphisms, ⊗ is defined as:
D∗

A

B∗

=

B

C∗

D∗

C

g

⊗

f

A∗

C∗

D

g

f

B∗

D

C

A∗

A

B

A strongly dagger symmetric monoidal functor is a functor F along with a unitary natural isomorphism ϕA,B : F(A ⊗ B) → F(A) ⊗ F(B) satisfying several coherence properties that we have no space to
go in to. Our next theorem shows that CPM[V] is equivalent to the full subcategory of CP∗ [V] consisting
of objects of the form (A∗ ⊗ A,
). Its proof uses ∗-homomorphisms, which we first define.

## PDF page 8

8

Categories of Quantum and Classical Channels

Definition 4.2. If (A, ) and (B, ) are normalisable dagger Frobenius algebras in a dagger compact
category V, a morphism f : A → B is called a ∗-homomorphism when it satisfies the following equations.

f

f

=

f

f

=

f∗

Lemma 4.3. Let (A, ) and (B, ) be normalisable dagger Frobenius algebras in a dagger compact
category V. If f : A → B is a ∗-homomorphism, then it is a well-defined morphism in CP∗ [V].
Proof. Using the definition:
proof.

◦f◦

=(

◦

) ◦ ( f ∗ ⊗ f ). Applying Lemma 3.2 completes the

Theorem 4.4. Let V be a positive-dimensional dagger compact category. Define L : CPM[V] → CP∗ [V]
by setting L(A) := (A∗ ⊗ A,
) on objects and L( f ) = f on morphisms. Then L is a well-defined
functor that is full, faithful, and strongly dagger symmetric monoidal.
Proof. For well-definedness, we show that a V-morphism f : A∗ ⊗ A → B∗ ⊗ B is a CPM[V]-morphism
) to (B∗ ⊗ B,
). First, assume
from A to B if and only if it is a CP∗ [V]-morphism from (A∗ ⊗ A,
f ∈ CPM[V] and compose with the action and coaction of the respective algebras to see that f satisfies
the CP*–condition, as follows.

f

=

g∗

g

=

g∗

g

Conversely, if f is in CP∗ [V], then it is also in CPM[V], as follows.

f

=

g∗

g

=

g∗

g

Composition is the same in CPM[V] and CP∗ [V], so L is a functor that is furthermore full and faithful. Similarly, daggers are the same in CPM[V] and CP∗ [V], so L trivially preserves daggers. It now
suffices to show that L is strongly monoidal. Define the isomorphism ϕA,B : L(A ⊗ B) → L(A) ⊗ L(B)
as the reshuffling map (321)(4) : B∗ ⊗ A∗ ⊗ A ⊗ B → A∗ ⊗ A ⊗ B∗ ⊗ B. One can verify that this map is
a ∗-homomorphism from L(A ⊗ B) to L(A) ⊗ L(B), so it must satisfy the CP*–condition. This map is
also unitary, and it is a routine calculation to show that it satisfies the coherence equations for a strong
symmetric monoidal functor.

## PDF page 9

B. Coecke, C. Heunen & A. Kissinger

5

9

Generalised stochastic maps and measurement of quantum states

Whereas the previous section focused on “purely quantum” objects in CP∗ [V], this section looks at the
“purely classical” ones. We will define a “purely probabilistic” category Stoch[V], that by construction
embeds into CP∗ [V]. Thus objects in CP∗ [V] can be interpreted as being “combined classical and quantum”. The category Stoch[V] was first considered in [9]. It was defined in a slightly different form there,
but one can prove that this coincides with the following definition.
Definition 5.1. For a dagger compact category V, define Stoch[V] to be the full subcategory of CP∗ [V]
consisting of all commutative normalisable dagger Frobenius algebras.
The next proposition justifies why this category is that of “classical channels”. We call a morphism
f : (A, ) → (B, ) in CP∗ [V] normalised if it preserves counits: ◦ f = . Because commutative
finite-dimensional C*-algebras correspond to finite-dimensional Hilbert spaces with a choice of orthonormal basis, we can think of the latter as objects of Stoch[FHilb] [10, 2, 13]. Recall that a stochastic map
between finite-dimensional Hilbert spaces is a matrix with positive real entries whose every column sums
to one.
Proposition 5.2. Normalised morphisms in Stoch[FHilb] correspond to stochastic maps between finitedimensional Hilbert spaces.
Proof. See [15, 3.2.3 and 2.1.3].
For any Frobenius algebra (A, ) we can consider its copyable points: the morphisms p : I → A
◦ p = p ⊗ p. This is especially interesting
that are “copied” by the comultiplication, in the sense that
for commutative normalisable dagger Frobenius algebras, because in FHilb, copyable points form an
orthonormal basis for A. Writing vectors in the basis of classical points, one can show that the normalised
positive elements are precisely those vectors with positive coefficients that sum to 1. Thus, normalised
positive elements of a commutative normalisable dagger Frobenius algebra can be regarded as probability
distributions over its copyable points.
So far we have mostly looked at classical and quantum systems in isolation. But as they live together
in a category CP∗ [V], we can also consider maps between them. Consider a normalised morphism
P : L(H) → (A, ) from a quantum to a classical system. Then P† ◦ xi is a positive element of
for
each copyable point xi . Furthermore, any commutative normalisable dagger Frobenius algebra in FHilb
satisfies = ∑i xi . Since P is normalised, ∑ P† ◦xi = P† ◦ ∑ xi = P† ◦ = eH : I → H ∗ ⊗H is the cup from
the compact structure on H. Positive elements in H ∗ ⊗ H represent positive operators from H to itself,
and eH represents the identity operator. Thus the set {P† ◦ xi } corresponds to a positive operator-valued
measure (POVM). Furthermore, for any quantum state ρ (i.e. normalised positive element in L(H)), it is
straightforward to show that P ◦ ρ yields the probability distribution whose ith element is the probability
of getting outcome xi , computed via the Born rule.
The dual notion of a morphism E : (A, ) → L(H) from a classical system to a quantum system can
be thought of as a preparation. Or, more precisely, as a map carrying a classical probability distribution
over some fixed set of states to a single mixed state. Choosing a particular decomposition E ◦ ρ for a
quantum state ρ gives us a way to represent quantum ensembles. See also [16, 3.2.4].

6

Hilbert spaces

It is high time we looked at some examples. This section proves that CP∗ [FHilb] is the category of all
finite-dimensional C*-algebras and completely positive maps. The proof also illuminates Theorem 4.4.

## PDF page 10

10

Categories of Quantum and Classical Channels

Namely, CPM[FHilb] has finite-dimensional C*-factors for objects. Recall that a C*-algebra is a factor
when its centre is 1-dimensional. Finite-dimensional C*-algebras in fact enjoy an easy structure theorem:
they are finite direct sums of factors, and factors are precisely matrix algebras [12, Theorem III.1.1]. The
following lemma recalls the structure of these factors, and the subsequent proposition determines the
objects of CP∗ [FHilb].
Lemma 6.1. If H is an n-dimensional Hilbert space, then there is an isomorphism of algebras between
L(H) and Mn (C). Therefore, H ∗ ⊗ H carries C*-algebra structure; the involution is as in Theorem 2.3.
Proof. First of all, Mn (C) is a Hilbert space under the Hilbert–Schmidt inner product ⟨a | b⟩ = Tr(a† b).
It has a canonical orthonormal basis {ei j | i, j = 1, . . . , n}, where ei j is the matrix all of whose entries are
0 except the (i, j)-entry, which is 1. Pick an orthonormal basis {|1⟩, . . . , |n⟩} for H, so that {⟨i| ⊗ | j⟩ |
i, j = 1, . . . , n} forms an orthonormal basis for H ∗ ⊗ H. Then the assignment ⟨i| ⊗ | j⟩ ↦→ ei j implements a
unitary isomorphism between H ∗ ⊗ H and Mn (C). Direct computation shows that matrix multiplication
translates across this isomorphism to
on H ∗ ⊗ H. Similarly, taking the conjugate transpose of a
matrix corresponds to the involution on H ∗ ⊗ H given in Theorem 2.3.
Proposition 6.2. All dagger Frobenius algebras in FHilb are normalisable.
Proof. Let (A, , ) be a dagger Frobenius algebra in FHilb. By Theorem 2.3, it must be isomorphic
⨁
to a C*-algebra of the form k Mnk (C), giving a unitary isomorphism of the associated dagger Frobenius
(k)
algebras. Let {ei j : 0 ≤ i, j < nk } form an orthonormal basis for A. We can define
in terms of this
(k)

TrA (

(k′ )

′

′

(k)

(ei j ⊗ ei′ j′ ) = δkk δ ji ei j′ . From this, we can compute TrA (

basis as

( ′ )†
(k)
(k )
)(ei j ) = ∑ ei′ j′
i′ j′ k′

Note that

(k)

(
)
( ′ )† ′ ′
( )†
(k)
(k′ )
(k )
(k)
(k)
(k)
ei j ⊗ ei′ j′ = ∑ ei′ j′ δkk δ ji ei j′ = ∑ e j j′ ei j′ = ∑ δij = nk δij .
i′ j′ k′

(ei j ) = δij . We can now define the normaliser

satisfies TrA (

) directly.

j′

(k)

j′

(k)

as ei j ↦→ √1nk ei j : this map is invertible,

) ◦ ( )2 = , and acts by a constant scalar on each summand of A and so is central.

Combining the previous proposition with Theorem 2.3, we see that the objects of CP∗ [FHilb] are
(in 1-to-1 correspondence with) finite-dimensional C*-algebras. We now turn to the morphisms of
CP∗ [FHilb]. First, let us review what (concrete) completely positive maps between C*-algebras are.
Good references are [3, 17]. The main notion is that of a matrix algebra Mn (A) over a C*-algebra
A. Its elements are n-by-n matrices with entries in A, given C*-structure by (ai j ) · (bi j ) = ∑nk=1 aik bk j ,
(ai j )∗ = (a∗ji ), and ∥(ai j )∥ = sup{∥(ai j )x∥ | x ∈ An , ∥x∥ = 1}, where ∥(x1 , . . . , xn )∥2 = ∑ni=1 ∥x1 ∥2 . The
following well-known lemma then follows directly.
Lemma 6.3. If A is a finite-dimensional C*-algebra, then so is Mn (A). If f : A → B is a linear map, then
so is the function Mn ( f ) : Mn (A) → Mn (B) that sends (ai j ) to ( f (ai j )). If f is a ∗-homomorphism, then
so is Mn ( f ).
Definition 6.4. A linear map f : A → B between C*-algebras is positive when for every a ∈ A there exists
b ∈ B satisfying f (a∗ a) = b∗ b. It is completely positive when Mn ( f ) is positive for every n ∈ N.
For us it will be convenient to take another, well-known, viewpoint. If A and B are finite-dimensional
C*-algebras, then so is the algebraic tensor product A ⊗ B.
Lemma 6.5. Any finite-dimensional C*-algebra A has a canonical ∗-isomorphism Mn (A) ∼
= A ⊗ Mn (C).
Under this correspondence, a linear map f : A → B between C*-algebras is completely positive if and
only if f ⊗ 1Mn (C) is positive for every n ∈ N.

## PDF page 11

B. Coecke, C. Heunen & A. Kissinger

11

Proof. Borrowing notation from Lemma 6.1, the ∗-isomorphism Mn (A) → A ⊗ Mn (C) is given by
(ai j ) ↦→ ∑ni, j=1 ai j ⊗ ei j . One easily verifies that this preserves the multiplication and involution. The
second statement follows directly from Definition 6.4 by unfolding this isomorphism.
Now we have phrased the concrete notion of complete positivity in terms of tensor products with
matrix algebras (cf. Theorem 3.6), and given that matrix algebras in FHilb are precisely the algebras of
the form L(H) for some Hilbert space H, we can determine CP∗ [FHilb].
Theorem 6.6. CP∗ [FHilb] is equivalent to the category of finite-dimensional C*-algebras and completely positive maps.
Proof. Define a functor E from CP∗ [FHilb] to the category of finite-dimensional C*-algebras and completely positive maps, acting on objects as in Theorem 2.3 and as identity on morphisms.
Proposition 6.2 and Theorem 2.3 show that E is surjective on objects. Suppose f : (A, ) → (B, )
is a morphism in CP∗ [V]. Then Theorem 3.6 shows that E( f ) must be completely positive, as characterised by Lemma 6.5. Therefore E is well-defined. Conversely, any completely positive map g between
C*-algebras satisfies the CP*–condition because of Lemma 6.5, so E is full and hence an equivalence of
categories.
Remark 6.7. It follows from the previous theorem that the embedding L does not extend to an equivalence of categories because it is not essentially surjective. That is, there are finite-dimensional C*algebras, such as A = M1 (C) ⊕ M2 (C), that are not isomorphic to a factor: dim(A) = 12 + 22 = 5 ̸= n2 =
dim(Mn (C)).

7

Sets and relations

The previous section justified regarding normalisable dagger Frobenius algebras as generalised (finitedimensional) C*-algebras. This section considers CP∗ [V] for V = Rel, the category of sets and relations.
Starting with objects, we immediately see that these ‘generalised C*-algebras’ are quite different.
Proposition 7.1. All normalisable dagger Frobenius algebras in Rel are special. Therefore they are (in
1-to-1 correspondence with small) groupoids.
Proof. We have to prove that normalisability implies speciality in Rel; for this it suffices to show that
z2 = 1. Now, the normaliser z is an isomorphism. In Rel, this means it is (the graph of) a bijection. But z
is also positive, and hence self-adjoint. This means it is equal to its own inverse. Therefore z2 = 1. The
second statement now follows directly from [14, Theorem 7].
Next, we turn to determining the morphisms of CP∗ [Rel].
Definition 7.2. A relation R ⊆ Mor(G) × Mor(H) between groupoids G, H respects inverses when
gRh ⇐⇒ g−1 Rh−1 ,

gRh =⇒ 1dom(g) R1dom(h) .

(2)

Proposition 7.3. CP∗ [Rel] is (isomorphic to) the category of groupoids and relations respecting inverses.
Proof. In general, a morphism R ⊆ (X × X) × (Y ×Y ) in Rel is completely positive if and only if
(x′ , x)R(y′ , y) ⇐⇒ (x, x′ )R(y, y′ ),

(x′ , x)R(y′ , y) =⇒ (x, x)R(y, y).

(3)

## PDF page 12

12

Categories of Quantum and Classical Channels

If G and H are groupoids, corresponding to Frobenius algebras (G,

) and (H,

), and R ⊆ G × H,

= {((g, g′ ), g−1 ◦ g′ ) ∈ G3 | cod(g) = cod(g′ )},
◦R◦

= {((g, g′ ), (h, h′ )) ∈ G2 × H 2 | cod(g) = cod(g′ ), cod(h) = cod(h′ ), (g−1 ◦ g′ )R(h−1 ◦ h′ )}.

Substituting this into (3) translates precisely into (2).
We close this section by investigating the embedding L : CPM[Rel] → CP∗ [Rel]. Recall that a category is indiscrete when there is precisely one morphism between each two objects. Indiscrete categories
are automatically groupoids.
Lemma 7.4. The essential image of the embedding L : CPM[Rel] → CP∗ [Rel] is the full subcategory of
CP∗ [Rel] consisting of indiscrete (small) groupoids.
Proof. Let X be an object in CPM[Rel], that is, a set. By definition, L(X) corresponds to a groupoid with
set of morphisms X × X, and composition
{
(y1 , x2 )
if y2 = x1,
(y1 , y2 ) ◦ (x1 , x2 ) =
undefined otherwise.
We deduce that the objects of L(X) correspond to identities, i.e. pairs (x1 , x2 ) with x1 = x2 . So objects
of L(X) just correspond to elements of X. Similarly, we find that dom(x1 , x2 ) = x2 and cod(x1 , x2 ) = x1 .
Hence (x1 , x2 ) is a morphism x2 → x1 in L(X), and it is the unique such.

8

Splitting idempotents

This section compares the CP*–construction to Selinger’s second solution to the problem of classical
channels. First, recall this construction of splitting dagger idempotents [19].
Definition 8.1. Let V be a dagger category. The category Split† [V] has as objects (A, p) where p : A → A
is a morphism in V satisfying p ◦ p = p = p† ; its morphisms (A, p) → (B, q) are morphisms f : A → B in
V satisfying f = q ◦ f ◦ p.
If V is a dagger compact category, then so is Split† [V] (see [19, Proposition 3.16]). We will need the
following assumption, that is satisfied in both Rel and FHilb.
Definition 8.2. A dagger compact category V is said to have algebraic square roots when, given any
normalisable Frobenius algebra on A and any central positive definite morphism f : A → A, there exists
a central morphism g : A → A such that f = g ◦ g.
We thank the anonymous referee for pointing us towards the following proposition.
Proposition 8.3. Let V be a dagger compact category that has algebraic square roots. There is a
functor F : CP∗ [V] → Split† [CPM[V]], acting as F(A, , ) =
◦
◦ ( ⊗ ) on objects, and as
F( f ) =

◦

◦f◦

◦

on morphisms. It is full, faithful, and strongly dagger symmetric monoidal.

Proof. First, notice that p = F(A, , ) is indeed a well-defined object of Split† [CPM[V]]: clearly
p=
◦ ◦ ◦
= p† by centrality of the normaliser, p ◦ p = p follows from Lemma 3.3, and p
is completely positive by Lemma 3.2. The assumption of algebraic square roots guarantees that F( f )
is indeed a well-defined morphism in CPM[V]; by Lemma 3.3, it is in fact a well-defined morphism
in Split† [CPM[V]]. Moreover, it is easy to see that an arbitrary V-morphism h : A∗ ⊗ A → B∗ ⊗ B is a
well-defined morphism in CP∗ [V] if and only if it is a well-defined morphism in Split† [CPM[V]].

## PDF page 13

B. Coecke, C. Heunen & A. Kissinger

h

13

=

f

⇐⇒

h

=

h

Both CP∗ [V] and Split† [CPM[V]] inherit composition, identities, and daggers from V, so F is a full and
faithful functor preserving daggers. The symmetric monoidal structure in both CP∗ [V] and Split† [CPM[V]]
is similarly defined in terms of that of V, making F strongly symmetric monoidal.
Thus, when V has algebraic square roots, CP∗ [V] is equivalent to a full subcategory of Split† [CPM[V]]:
the one obtained by splitting only the idempotents of the form F(A, , ). A variation of [19, Proposition 3.16] shows that splitting any family of dagger idempotents that is closed under tensor gives a
dagger compact category, and Theorem 3.5 follows. The proof that we have written out does not need
the assumption of algebraic square roots; moreover, it more explicitly exhibits the structure of CP∗ [V] as
a category of algebras.
In summary, in sufficiently nice cases, the CP*–construction fits between the CPM–construction and
its idempotent splitting.
CPM[V]

L

/ CP∗ [V]

F

/ Split† [CPM[V]]

Both functors are strongly dagger symmetric monoidal, as well as full and faithful. Moreover, their
composition is naturally isomorphic to the canonical inclusion CPM[V] → Split† [CPM[V]]. However,
the image of the left functor does not include classical channels. Similarly, a priori there is no reason
why the right functor should be an equivalence. In particular, the middle category seems to capture the
right amount of objects, and provides a constructive way to access them.

9

Future work

Having an abstract notion of C*-algebra, (and, by extension, an abstract categorical construction placing
classical and quantum information on equal footing) opens up many avenues for exploration.
• Quantum mechanics can be characterised in information-theoretic terms [4], but this argument is
often criticised because it assumes a C*-algebraic framework from the start. The CP*–construction
can investigate to what extent this criticism is valid and improve on those foundations.
• We can now abstractly study all sorts of notions from the C*-algebraic formulation of quantum
information theory [15, 16]. For example, notions of complementarity can be translated between
abstract and concrete C*-algebras [6, 13].
• The category Stab of stabiliser quantum mechanics embeds into CP∗ [Rel], opening the door to
abstract considerations of classical simulable circuits.
• It would be good to see whether algebraic square roots are necessary for Proposition 8.3. We also
expect to find an example showing that F is not an equivalence.
• One could characterise categories of the form CP∗ [V], perhaps using environments [5, 11, 7].
• It is worth investigating to what extent our construction generalises to infinite dimension [2, 7].

## PDF page 14

14

Categories of Quantum and Classical Channels
• On the theoretical side, the CP*–construction might be (lax) monadic.
• Our construction seems related in spirit to [22]; it would be good to make connections precise.

References
[1] Samson Abramsky & Bob Coecke (2008): Categorical quantum mechanics. In: Handbook of quantum logic
and quantum structures: quantum logic, Elsevier, pp. 261–324, doi:10.1016/B978-0-444-52869-8.50010-4.
[2] Samson Abramsky & Chris Heunen (2012): H*-algebras and nonunital Frobenius algebras: first steps in
infinite-dimensional categorical quantum mechanics. Clifford Lectures 71, pp. 1–24.
[3] Rejandra Bhatia (2007): Positive definite matrices. Princeton University Press.
[4] Rob Clifton, Jeffrey Bub & Hans Halvorson (2003): Characterizing quantum theory in terms of informationtheoretic constraints. Foundations of Physics 33(11), pp. 1561–1591, doi:10.1023/A:1026056716397.
[5] Bob Coecke (2008): Axiomatic Description of Mixed States From Selinger’s CPM-construction. Electronic
Notes in Theoretical Computer Science 210, pp. 3–13, doi:10.1016/j.entcs.2008.04.014.
[6] Bob Coecke & Ross Duncan (2011): Interacting Quantum Observables: Categorical Algebra and Diagrammatics. New Journal of Physics 13, p. 043016, doi:10.1088/1367-2630/13/4/043016.
[7] Bob Coecke & Chris Heunen (2011): Pictures of complete positivity in arbitrary dimension. In: Proceedings
of QPL, pp. 29–37, doi:10.4204/EPTCS.95.4.
[8] Bob Coecke, Chris Heunen & Aleks Kissinger (2013): Categories of Classical and Quantum Channels.
arXiv:1305.3821 .
[9] Bob Coecke, Éric O. Paquette & Duško Pavlović (2010): Classical and quantum structuralism. In S. Gay &
I. Mackey, editors: Semantic Techniques in Quantum Computation, Cambridge University Press, pp. 29–69.
[10] Bob Coecke, Duško Pavlović & Jamie Vicary (2012): A new description of orthogonal bases. Mathematical
Structures in Computer Science 23(3), pp. 555–567, doi:10.1017/S0960129512000047.
[11] Bob Coecke & Simon Perdrix (2010): Environment and classical channels in categorical quantum mechanics. In: CSL’10/EACSL’10, Springer, pp. 230–244, doi:10.1007/978-3-642-15205-4 20.
[12] Kenneth R. Davidson (1991): C*-algebras by example. American Mathematical Society.
[13] Chris Heunen (2012): Complementarity in categorical quantum mechanics. Foundations of Physics 42(7),
pp. 856–873, doi:10.1007/s10701-011-9585-9.
[14] Chris Heunen, Ivan Contreras & Alberto S. Cattaneo (2012): Relative Frobenius algebras are groupoids.
Journal of Pure and Applied Algebra 217, pp. 114–124, doi:10.1016/j.jpaa.2012.04.002.
[15] Michael Keyl (2002): Fundamentals of quantum information theory. Physical Reports 369, pp. 431–548,
doi:10.1016/S0370-1573(02)00266-1.
[16] Michael Keyl & Reinhard F. Werner (2007): Channels and maps. In Dagmar Bruß & Gerd Leuchs, editors:
Lectures on Quantum Information, Wiley-VCH, pp. 73–86, doi:10.1002/9783527618637.ch5.
[17] Vern Paulsen (2002): Completely bounded maps and operators algebras. Cambridge University Press.
[18] Peter Selinger (2007): Dagger compact closed categories and completely positive maps. In: QPL, ENTCS
170, Elsevier, pp. 139–163, doi:10.1016/j.entcs.2006.12.018.
[19] Peter Selinger (2008): Idempotents in dagger categories. In: QPL, ENTCS 170, Elsevier, pp. 107–122,
doi:10.1016/j.entcs.2008.04.021.
[20] Peter Selinger (2010): A survey of graphical languages for monoidal categories. In: New Structures for
Physics, Lecture Notes in Physics 813, Springer, pp. 289–355, doi:10.1007/978-3-642-12821-9 4.
[21] Jamie Vicary (2011): Categorical formulation of finite-dimensional quantum algebras. Communications in
Mathematical Physics 304(3), pp. 765–796, doi:10.1007/s00220-010-1138-0.
[22] Jamie Vicary (2012): Higher quantum theory. Preprint, arXiv:1207.4563 .
