Source: https://doi.org/10.46298/LMCS-18(1:28)2022
PDF sha256: 1740775b0921d51755cb5ebcc5b88b051f2ebec0bd508ba924d1b9a94f44275e
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of coquand_huber_sattler_2022_canonicity_and_homotopy_canonicity_for_cubical_type_theory.pdf

Transcription of `coquand_huber_sattler_2022_canonicity_and_homotopy_canonicity_for_cubical_type_theory.pdf` in this directory, 35 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-35 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Logical Methods in Computer Science
Volume 18, Issue 1, 2022, pp. 28:1–28:35
https://lmcs.episciences.org/

Submitted
Published

Apr. 20, 2020
Feb. 03, 2022

CANONICITY AND HOMOTOPY CANONICITY
FOR CUBICAL TYPE THEORY
THIERRY COQUAND a , SIMON HUBER a , AND CHRISTIAN SATTLER b
a

University of Gothenburg, Sweden
e-mail address: coquand@chalmers.se, simonh@fripost.org

b

Chalmers University of Technology, Sweden
e-mail address: sattler@chalmers.se

Abstract. Cubical type theory provides a constructive justification of homotopy type
theory. A crucial ingredient of cubical type theory is a path lifting operation which is
explained computationally by induction on the type involving several non-canonical choices.
We present in this article two canonicity results, both proved by a sconing argument: a
homotopy canonicity result, every natural number is path equal to a numeral, even if we take
away the equations defining the lifting operation on the type structure, and a canonicity
result, which uses these equations in a crucial way. Both proofs are done internally in a
presheaf model.

Introduction
This article is a contribution to the analysis of the computational content of the univalence
axiom [Voe14] (and higher inductive types). In previous work [ABC+ 21, BCH14, CCHM18,
CHM18, OP16], various presheaf models of this axiom have been described in a constructive
metatheory. In this formalism, the notion of fibrant type is stated as a refinement of the
path lifting operation where one not only provides one of the endpoints but also a partial lift
(for a suitable notion of partiality). This generalized form of path lifting operation is a way
to state a homotopy extension property, which was recognized very early (see e.g. [Eil39]) as
a key for an abstract development of algebraic topology. The axiom of univalence is then
captured by a suitable equivalence extension operation (the “glueing” operation), which
expresses that we can extend a partially defined equivalence of a given total codomain to a
total equivalence. These presheaf models suggest possible extensions of type theory where
we manipulate higher dimensional objects [ABC+ 21, CCHM18]. One can define a notion of
reduction and prove canonicity for this extension [Hub19]: any closed term of type N (natural
number) is convertible to a numeral. There are however several non-canonical choices when
defining the path lifting operation by induction on the type, which produce different notion
of convertibility.1 A natural question is how essential these non-canonical choices are: can it
be that a closed term of type N, defined without use of such non-canonical reduction rules,
Key words and phrases: cubical type theory, univalence, canonicity, sconing, Artin glueing.
1For instance, the definition of this operation for “glue” types is different in [CCHM18] and [OP16].

l

LOGICAL METHODS
IN COMPUTER SCIENCE

DOI:10.46298/LMCS-18(1:28)2022

© T. Coquand, S. Huber, and C. Sattler
CC
⃝
Creative Commons

## PDF page 2

28:2

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

becomes convertible to 0 for one choice and 1 for another? The main result of this article,
the homotopy canonicity theorem, implies that this cannot be the case: the value of a term is
independent of these non-canonical choices. Homotopy canonicity states that, even without
providing reduction rules for path lifting operations at type formers, we still have that any
closed term of type N is path equal to a numeral. (We cannot hope to have convertibility
anymore with these path lifting constants.) We can then see this numeral as the “value” of
the given term.
Our proof of homotopy canonicity can be seen as a proof-relevant extension of the
reducibility or computability method, going back to the work of Gödel [Göd58] and Tait [Tai67].
It is however best expressed in an algebraic setting. We first define a general notion of model,
called cubical category with families, defined as a category with families [Dyb96] with certain
special operations internal to presheaves over a category C (such as a cube category) with
respect to the parameters of an interval I and a cofibration classifier F. In this article, we will
work with models of the cubical type theory described by [CCHM18, OP16]. However, our
methods apply equally well to other versions of cubical type theories that can be presented
in a similar setting, for example [ABC+ 21].
We describe the term model and how to re-interpret the cubical presheaf models as
cubical categories with families. The computability method can then be expressed as a
general operation (called “sconing”) which applied to an arbitrary model M produces a new
model M∗ with a strict morphism M∗ → M. Homotopy canonicity is obtained by applying
this general operation to the initial model, which we conjecture to be the term model. This
construction associates to a (for simplicity, closed) type A a predicate A′ on the closed terms
|A| and each closed term u of A a proof u′ of A′ u. The main rules in the closed case are
summarized in Figure 1.
We explain next how a similar method can be used to prove canonicity (or “strict”
canonicity) when we add computation rules of filling at type formers (using as primitive the
operation of composition). Here, every closed term of type N is (strictly) equal (as opposed
to path equal) to a numeral. This was originally proved by [Hub19]. The main advantage of
the present approach is that we don’t need to define an auxiliary reduction relation, and that
it is independent of the exact choice of the equational presentation of cubical type theory.
Some extensions and variations are then described:
• Our development extends uniformly to identity types and higher inductive types (using
the methods of [CHM18]) (Subsections 5.1 and 5.2).
• Our development applies equally to the case where one treats univalence instead of glue
types as primitive (Appendix C.1). We expect that a similar sconing argument (glueing
along a global sections functor to simplicial sets) works to establish homotopy canonicity
for the initial split univalent simplicial tribe in the setting of Joyal [Joy17].
• Assuming excluded middle, a version of the simplicial set model [KL12] forms an instance of
our development, and distributive lattice cubical type theory interprets in it (Appendix D).
Using our technique, one may also reprove canonicity for ordinary Martin-Löf type theory
with inductive families in a reduction-free way.
Shulman [Shu15] proves homotopy canonicity for homotopy type theory with a truncatedness assumption using the sconing technique. This proof was one starting point for the
present work.
Two models of type theory and sconing. Since Martin Hofmann’s work [Hof97], it is
known how to interpret extensional type theory with a hierarchy of universes U0 , U1 , . . . in

## PDF page 3

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

Π(A, B)′ (w) =
Σ(A, B)′ (w) =
Path(A, a0 , a1 )′ (w) =

28:3

′
′
u′ :A′ u B u u (app(w, u))
∑
′
′
u′ :A′ (fst(w)) B (fst(w)) u (snd(w))
Pathλi A′ i (ap(w,i)) a′0 a′1
( ′
)[
′

∏

u:|A|

∏

Gluec (A, ψ ↦→ (B, w))′ (v) = Glue A (app(unglue, v))

]
ψ ↦→ (B v, (w′ .1 v, . . .))

Figure 1: These are the main rules for the computability predicate component in the sconing
models for homotopy canonicity and canonicity in the case of the global context.
The component relating to fibrancy differs between the two cases.

any presheaf model. As explained in [CCHM18, OP16, Coq18], in some class of presheaf
models, parametrised by two presheaves I (representing an abstract interval) and F (the
cofibration classifier), it is possible to define, as an internal model inside this presheaf model,
a model of type theory with a hierarchy of universes U0fib , U1fib , . . . satisfying the univalence
axiom. Both models are carried out in a constructive metalanguage. In particular, the
second model provides a computational interpretation of univalence.
This model of univalence is a model of cubical type theory where each type has a filling
operation. Univalence is then a theorem and not an axiom of cubical type theory. This filling
operation is defined by induction on the type, using a more primitive composition operation.
The basic scheme for a canonicity proof that we follow here is to associate by induction
on a type A a computability predicate A′ on the (internal) set |A| of closed elements of this
type. As explained in [Coq19], this so-called sconing interpretation for canonicity goes back
to Gödel’s notion of computability predicates [Göd58], with the crucial feature here that
these predicates are now proof-relevant. This scheme works as well for cubical type theory if
we use a metalanguage with an interval object.
We now explain in general terms and by example the differences between the homotopy
canonicity and the canonicity proofs. For the homotopy canonicity proof, we will have
A′ : |A| → Unfib , while for the canonicity proof, we will have A′ : |A| → Un with a separate
component tracking computability of composition.
∑
For the type of natural number N, for the canonicity proof, we define N′ t to be k:N t =|N|
Sk (0), where t =|N| Sk (0) is (strict) equality, and N is the constant presheaf of natural numbers.
In this case, N′ is not a fibrant family over |N |. For homotopy canonicity, we have to define
N′ t as a fibrant family over |N | (see Subsubsection 3.2.4).2
One key step in both arguments is in ensuring that the filling operation is a computable
operation. This is solved in very different ways for the two theories. For the homotopy
canonicity proof, where A′ : |A| → Unfib , we can prove directly that the filling operation is
computable without needing information on how the filling operation behaves at individual
type formers. For the canonicity proof, where A′ : |A| → Un , the filling operation is defined
in terms of a more primitive composition operation and we prove by induction on the type
that this composition operation is computable.
2This fibrant family is not simply obtained by replacing the equality t = Sk (0) by a path, as this would
|N|
not model the β-equality of the eliminator in the successor case. Instead, we should view N′ in the case of
canonicity as an indexed inductive set and then replace it by a fibrant indexed inductive set for the case of
homotopy canonicity.

## PDF page 4

28:4

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

As in [Coq19], we think that this interpretation is best described in an algebraic way,
using what is essentially a generalized algebraic presentation of type theory. The difference
with [Coq19] is that the notion of generalized algebraic theory we are using is now developed
internally to a presheaf model with an interval I and cofibration classifier F.
Setting. We work in a constructive set theory (as presented e.g. in [Acz99]) with a sufficiently
long cumulative hierarchy of Grothendieck universes. However, our constructions are not
specific to this setting and can be replayed in other constructive metatheories such as
extensional type theory. In Appendix D, we assume classical logic for the discussion of
models in simplicial sets.

1. Cubical categories with families
We first recall the notion of categories with families (cwf) [Dyb96] equipped with Π- and
Σ-types, universes, and natural number types. This notion can be interpreted in any presheaf
model. In that setting, we can consider new operations. A cubical cwf will be such a cwf in a
presheaf model with extra operations that make use of an interval object I and a cofibration
classifier F as introduced in [CHM18, OP16].
1.1. Categories with families. Categories with families form an algebraic notion of model
of type theory. In order to simplify the treatment of universes, we define them in a stratified
manner where instead of a single presheaf of types, we specify a filtration of presheaves of
“small” types.3 The length of the filtration is not essential: we have chosen ω + 1 so that we
may specify constructions just at the top level.
A category with families (cwf) consists of the following data.
• We have a category of contexts Con and substitutions Hom(∆, Γ) from ∆ to Γ in Con. The
identity substitution on Γ in Con is written id, and the composition of δ in Hom(Θ, ∆)
and σ in Hom(∆, Γ) is written σδ.
• We have a presheaf Type of types over the category of contexts. The action of σ in
Hom(∆, Γ) on a type A over Γ is written Aσ. We have a cumulative sequence of subpresheaves Typen of types of level n of Type where n is a natural number.
• We have a presheaf Elem of elements over the category of elements of Type, i.e. a set
Elem(Γ, A) for A in Type(Γ) with aσ in Elem(∆, Aσ) for a in Elem(Γ, A) and σ in Hom(∆, Γ)
satisfying evident laws.
• We have a terminal context 1, with the unique element of Hom(Γ, 1) written ().
• Given A in Type(Γ), we have a context extension Γ.A. There is a projection p in
Hom(Γ.A, Γ) and a generic term q in Elem(Γ.A, Ap). Given σ in Hom(∆, Γ), A in Type(Γ),
and a in Elem(∆, Aσ) we have a substitution extension (σ, a) in Hom(∆, Γ.A). These
operations satisfy p(σ, a) = σ, q(σ, a) = a, and (pσ, qσ) = σ. Thus, every element of
Hom(∆, Γ.A) is uniquely of the form (σ, a) with σ and a as above.
3We note that this, some might say, non-algebraic aspect of the definition does not interfere with the

otherwise algebraic character and that subsets could in principle be replaced by injections. Indeed, one can
even relax the requirement that Typen → Type is a monomorphism, at the cost of making it more tedious to
state coherence of type formers under lifting and level coercion (if desired). One can also give a version where
there is no top-level presheaf of types Type. None of these variations impact what we do in this article.

## PDF page 5

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:5

We introduce some shorthand notation related to substitution. Given σ in Hom(∆, Γ)
and A in Type(Γ), we write σ + = (σp, q) in Hom(∆.Aσ, Γ.A). Given a in Elem(Γ, A), we
write [a] = (id, a) in Hom(Γ, Γ.A). Thus, given B in Typen (Γ.A) and a in Elem(Γ, A), we
have B[a] in Type(Γ). Given furthermore b in Elem(Γ.A, B), we have b[a] in Elem(Γ, B[a]).
We extend this notation to several arguments: given ai in Elem(Γ, Ai ) for 1 ≤ i ≤ k, we
write [a1 , . . . , ak ] for [ak ][ak−1 p] · · · [a1 p . . . p] in Hom(Γ, Γ.A1 . . . . .Ak ).
Note that we could take a different equational presentation. For instance, the presentation
in [Ehr88] takes as primitive the operations σ + and [u] and defines then (σ, u) as a derived
operation (σ, u) = σ + [u]. It is a strength of the present approach to canonicity proof to be
independent of this choice.
Given a cwf as above, we define what it means to have the following type formers. In
addition to the specified laws, all specified operations are furthermore required to be stable
under substitution in the evident manner.
• Dependent products. For A in Type(Γ) and B in Type(Γ.A), we have Π(A, B) in
Type(Γ), of level n if A and B are. Given b in Elem(Γ.A, B), we have the abstraction
λ(b) in Elem(Γ, Π(A, B)). Given c in Elem(Γ, Π(A, B)) and a in Elem(Γ, A), we have the
application app(c, a) in Elem(Γ, B[a]). These operations satisfy
app(λ(b), a) = b[a],
λ(app(cp, q)) = c.
Given A and B in Type(Γ) we write A → B for Π(A, Bp).
• Dependent sums. For A in Type(Γ) and B in Type(Γ.A), we have Σ(A, B) in Type(Γ),
of level n if A and B are. Given a in Elem(Γ, A) and b in Elem(Γ, B[a]), we have the
pairing pair(a, b) in Elem(Γ, Σ(A, B)). Given c in Elem(Γ, Σ(A, B)), we have the first
projection fst(c) in Elem(Γ, A) and second projection snd(c) in Elem(Γ, B[fst(c)]). These
operations satisfy
fst(pair(a, b)) = a,
snd(pair(a, b)) = b,
pair(fst(c), snd(c)) = c.
Thus, every element of Elem(Γ, Σ(A, B)) is uniquely of the form pair(a, b) with a and b
as above.
Given A and B in Type(Γ) we write A × B for Σ(A, Bp).
• Universes. We have Un in Typen+1 (Γ) and an isomorphism Typen (Γ) ∼
= Elem(Γ, Un ),
naturally in Γ.4
• Natural numbers. We have N in Type0 (Γ) with zero 0 in Elem(Γ, N) and successor
S(n) in Elem(Γ, N) for n in Elem(Γ, N). Given P in Type(Γ.N), z in Elem(Γ, P [0]), s in
Elem(Γ.N.P, P (p, S(q))p), and n : Elem(Γ, N), we have the elimination natrec(P, z, s, n) in
Elem(Γ, P [n]) with
natrec(P, z, s, 0) = z,
natrec(P, z, s, S(n)) = s[n, natrec(P, z, s, n)].
A structured cwf is a cwf with type formers as above.
4This presents Tarski-style universes. For Russell-style universes, we would additionally demand that this

isomorphism is an identity.

## PDF page 6

28:6

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

A (strict) morphism M → N of cwfs is defined in the evident manner and consists
of a functor F : ConM → ConN and natural transformations u : TypeM → TypeN F and
v : ElemM → ElemN (F, u) such that v restricts to types of level n and the terminal context
and context extension is preserved strictly. A morphism M → N of structured cwfs
additionally preserves the operations of the above type formers. We obtain a category of
structured cwfs.
1.2. Internal language of presheaves. For the rest of the article, we fix a category C in
the lowest Grothendieck universe. As in [ABC+ 21, OP16, LOPS18], we will use the language
of extensional type theory (with subtypes) to describe constructions in the presheaf topos
over C.
In the interpretation of this language, a context is a presheaf A over C, a type B over A
is a presheaf over the category of elements of A, and an element of B is a section. A global
type is a type in the global context, i.e. a presheaf over C. Similarly, a global element of a
global type is a section of that presheaf.
For elements x and y of a type A, we have the equality type x =A y, satisfying reflection
(we allow ourselves to omit the subscript A if it is evident from the context). Given a
dependent type B over a type A, we think of
∑B as a family of types B a indexed
∏ by elements
a of A. We have the
usual
dependent
sum
B
a
and
dependent
product
a:A
a:A B
∑
∏a, with
projections of s : a:A B a written s.1 : A and s.2 : B s.1, and application ∑
of f : a:A B a
to a : A written f a. ∏
We have also the categorical pairing ⟨f, g⟩ : X → a:A B a given
f : X → A and g : x:X B (f a) and other commonly used notations. The hierarchy
of Grothendieck universes in the ambient set theory gives rise to a cumulative hierarchy
U0 , U1 , . . . , Uω of universes à la Russell. We model propositions as subtypes of a fixed type 1
with unique element tt. This implies that logically equivalent propositions are equal. We
have subuniverses Ωi ⊆ Ui of propositions for i ∈ {0, 1 . . . , ω}.
When working in this internal language, we refer to the types as “sets” to avoid ambiguity
with the types of (internal) cwfs we will be considering.
1.3. Cubical categories with families. We now work internally to presheaves over C.
We assume the following:
• an interval I : U0 with endpoints 0, 1 : I,
• an cofibration classifier consisting of F : U0 with a monomorphism [−] : F → Ω0 .5
As in [CHM18, OP16], a partial element of a set T is given by an element ϕ in F and a
function [ϕ] → T . We say that a total element v of T extends such a partial element ϕ, u if
we have [ϕ] → u tt = v. (Note that the last equation make sense because [ϕ] = tt as soon as
[ϕ] is inhabited).
Given A : I → Uω , we write hasFill(A)
for the set of operations taking as inputs ϕ in F,
∏
b ∈ {0, 1}, and a partial
section
u
in
[ϕ]
∨ (i = b) → A i and producing an extension of
i:I
∏
u to a total section in i:I A i. Given a set X and Y : X → Uω , we write Fill(X, Y ) for the
set of filling structures on Y , producing an element of hasFill(Y ◦ x) for x in I → X. Given
s∏in Fill(X, Y ) and x, ϕ, b, u as above, we write s(x, ϕ, b, u) for the resulting total section in
i:I Y (x i).
5The requirement that [−] is mono is not essential and can be relaxed. However, this comes at the cost of

making later conditions on F more tedious to state.

## PDF page 7

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:7

We now interpret the definitions of Subsection 1.1 in the internal language of the presheaf
topos. A cubical cwf is a structured cwf denoted as before that additionally has the following
cubical operations and type formers. Again, all specified operations are required to be stable
under substitution.
• Filling operation. We have fill in Fill(Type(Γ), λA Elem(Γ, A)) for Γ in Con. Let us
spell
∏ out stability under substitution: given A : I → Type(Γ), ϕ in F, b ∈ {0, 1}, u in
i:I [ϕ] ∨ (i = b) → Elem(Γ, A i), and σ in Hom(∆, Γ) and r : I, we have
(fill(A, ϕ, b, u) r)σ = fill(λi (A i)σ, ϕ, b, λi,x (u i x)σ) r.
Note that we do not include computation rules for fill at type formers. This corresponds
to our decision to treat fill as a non-canonical operation.
• Dependent path types. Given A in I → Type(Γ) with ab in Elem(Γ,
Ab) for b ∈ {0, 1},
∏
we have Path(A, a0 , a1 ) in Type(Γ), of level n if A is. Given u in i:I Elem(Γ, Ai), we have
the path abstraction ⟨⟩(u) in Elem(Γ, Path(A, u 0, u 1)). Given p in Elem(Γ, Path(A, a0 , a1 ))
and i in I, we have the path application ap(p, r) in Elem(Γ, Ai). These operations satisfy
the laws
ap(p, b) = ab ,
ap(⟨⟩(u), i) = u i,
⟨⟩(λi ap(p, i)) = p.
Thus,
every element of Elem(Γ, Path(A, a0 , a1 )) is uniquely of the form ⟨⟩(u) with u in
∏
Elem(Γ,
Ai) such that u 0 = a0 and u 1 = a1 .
i:I
Using path types, we define isContrc (A) in Type(Γ) for A in Type(Γ) as well as isEquivc
in Type(Γ.A → B) and Equivc in Type(Γ) for A, B in Type(Γ) as in [CCHM18]. (We use
a subscript here and for some other notions to distinguish them from analogous notions
defined later in a different setting in Subsection 2.2.) These notions are used in the following
type former, which extends any partially defined equivalence (given total codomain) to a
totally defined function.
• Glue types. Given A in Type(Γ), ϕ in F, T in [ϕ] → Type(Γ), and
e : [ϕ] → Elem(Γ, Equivc (T tt, A)),
we have the glueing Gluec (A, ϕ, T, e) in Type(Γ), equal to T on [ϕ] and of level n if A and
T are. We have unglue in Elem(Γ, Gluec (A, ϕ, T, e) → A) such that unglue = fst(e) tt
on [ϕ]. Given a in Elem(Γ, A) and t in [ϕ] → Elem(Γ, T ) such that app(fst(e) tt, t tt) = a
on [ϕ], we have glue(a, t) in Elem(Γ, Gluec (A, ϕ, T, e)) equal to t on [ϕ]. These operations
satisfy
app(unglue, glue(a, t)) = a,
glue(app(unglue, u), λx u) = u.
Thus, every element of Elem(Γ, Gluec (A, ϕ, T, e)) is uniquely of the form glue(a, t) with a
and t as above.
The notion of morphism of structured cwfs lifts to an evident notion of morphism of
cubical cwfs. We obtain, internally to presheaves over C, a category of cubical cwfs. We
now lift this category of cubical cwfs from the internal language to the ambient theory
by interpreting it in the global context: externally, a cubical cwf (relative to the chosen

## PDF page 8

28:8

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

base category C, interval I, and cofibration classifier F) consists of a presheaf Con over C, a
presheaf Type over the category of elements of Con, etc.
Remark 1.1. Fix a cubical cwf as above. Assume that I has a connection algebra structure
and that F forms a sublattice of Ω0 that contains the interval endpoint inclusions. As
in [CCHM18], it is then possible in the above context of the glue type former to construct an element of Elem(Γ, isEquivc [unglue]). From this, one derives an element of
Elem(Γ, iUnivalencen ) where
iUnivalencen = Π(Un , isContrc (Σ(Un , Equivc (q, qp))))
for n ≥ 0, i.e. univalence is provable. One may also show that the path type applied to
constant families I → Type(Γ) interprets the rules of identity types of Martin-Löf with
the computation rule for the eliminator J replaced by a propositional equality. Thus, we
obtain an interpretation of univalent type theory with identity types with propositional
computation in any cubical cwf.
1.4. Computational cubical categories with families. In this subsection, we consider a
variation of the notion of cubical categories with families where we replace the filling operation
by a composition operation, and where we add computation rules for this composition
operation. This version is the one used for (strict) canonicity in Section 6. The computation
rules are needed since the proof of canonicity follows closely the constructive justification
of cubical type theory. For this justification, we also have to replace the filling operation
by a composition operation. We show then that we can define a filling operation from
a composition operation and we define the composition operation on types structurally.
Since the canonicity argument, like the one in [Coq19], follows closely the structure of the
constructive justification of the model of univalence, we need to start from the composition
operation instead.
In order to simplify the notations, we assume here that the interval I also has a reversal
operation, like in [CCHM18, CHM18]. This assumption is not necessary (for instance, as
noted in [CCHM18], and indeed as we did in Subsection 1.3, we can avoid the reverse
operation at the cost of carrying around an external boolean parameter) but it simplifies
the presentation slightly.
Given A : I → Uω , we write
∏ hasComp(A) for the set of operations taking as inputs ϕ in
F with a partial section u in i:I [ϕ] ∨ (i = 0) → A i and producing an element in A 1 which
is equal to u 1 tt on ϕ. Given a set X and Y : X → Uω , we write Comp(X, Y ) for the set
of composition structures on Y , producing an element of hasComp(Y ◦ x) for x in I → X.
Given s in Comp(X, Y ) and x, ϕ, u as above, we write s(x, ϕ, u) for the resulting element in
Y (x 1).
We now change the definition of cubical cwf in two ways to obtain our notion of
computational cubical cwf.
First, we replace the filling operation by a composition operation. We have comp in
Comp(Type(Γ), λA Elem(Γ, A)) for
∏ Γ in Con together with stability under substitution: given
A : I → Type(Γ), ϕ in F, u in i:I [ϕ] ∨ (i = 0) → Elem(Γ, A i), and σ in Hom(∆, Γ) and
r : I, we have
comp(A, ϕ, u)σ = comp(λi (A i)σ, ϕ, λi,x (u i x)σ).
The filling operation is now a derived operation. We define
fill(A, ϕ, u) r = comp(Ar , ϕ, ur )

## PDF page 9

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:9

where Ar i = A (i ∧ r) and ur i = u (i ∧ r).
Second, we add suitable computation rules (equalities) for this composition operation,
structurally over types, following the computation rules in [CCHM18, CHM18]. We give the
details here for two representative examples.
• For dependent sums, we add the computation rule
comp(λi Σ(A i, B i), ψ, w) = pair(u, v)
where u = ũ 1 and v = comp(λi (B i)[ũ i], ψ, λi,x snd(w i x)) using
ũ = fill(A, ψ, λi,x fst(w i x)).
• For natural numbers, we add the computation rules
comp(λi N, ψ, λi,x 0) = 0
comp(λi N, ψ, λi,x S(v i x)) = S(comp(λi N, ψ, b, v)).

2. Two examples of cubical cwfs
In this section we give two examples of cubical cwfs: a term model and a particular cubical
cwfs formulated in a constructive metatheory, the latter with extra assumptions on I and F.

2.1. Term model. We sketch how to give a cubical cwf T built from syntax, and refer the
reader to Appendix A for more details. All our judgments will be indexed by an object X
of C and given a judgment Γ ⊢X J and f : Y → X in C we get Γf ⊢Y J f . Here, f acts on
expressions as an implicit substitution, while for substitutions on object variables we will
use explicit substitutions.
The forms of judgment are:
Γ ⊢X

Γ ⊢X A

Γ ⊢X A = B

Γ ⊢X t : A

Γ ⊢X t = u : A

σ : ∆ →X Γ

The main rules are given in the appendix. This then induces a cubical cwf T by taking,
say, the presheaf of contexts at stage X to be equivalence classes of Γ for Γ ⊢X where the
equivalence relation is judgmental equality.
Some rules are a priori infinitary, but in some cases (such as the one considered
in [CCHM18]) it is possible to present the rules in a finitary way.
This formal system expresses the laws of cubical cwfs in rule form. It defines the term
model. Following [Str91, PV07] developed in an intuitionistic framework, we conjecture that
this can be interpreted in an arbitrary cubical cwf in the usual way:
Conjecture 2.1. With chosen parameters C, I, F, the cubical cwf T is initial in the category
of cubical cwfs.
However, our canonicity result is orthogonal to this conjecture: It is a result about the
initial model, without need for an explicit description of this model as a term model.

## PDF page 10

28:10

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

2.2. Developments in presheaves over C. We now assume that I and F satisfy the
axioms presented in [OP16, Coq18]. We briefly recall them for the reader’s convenience.
The subobject F of Ω0 should define a dominance and be closed under disjunction. The
subobject classified by the map [−] : F → Ω0 should be levelwise decidable. The interval I
should have two distinct global elements 0 and 1 and connections. The interval endpoint
inclusions should be cofibrations (i.e., the equalities to 0 and 1 are coded by elements of F)
and cofibrations should be closed under universal quantification over I. Finally, the interval
I should be tiny, i.e., the exponential functor (−)I should have a right adjoint R.6 This is
for example the case if C has finite products and I is representable.
Most of the reasoning will be done in the internal language of the presheaf topos. At
certain points however, we need to consider the set of global sections of a global type F ;
we denote this by □F . We stress that statements involving □ are external, not to be
interpreted in the internal language. Crucially, the adjunction (−)I ⊣ R cannot be made
internal [LOPS18].
We write Cˆ for the category of presheaves over C. The right adjoint R is determined by
an isomorphism
ˆ RX) ≃ C(A
ˆ I , X)
C(A,
natural in A and X. Using cocontinuity in X, we may equivalently restrict to A = y(I)
where y denotes the Yoneda embedding and I is in C. Then the isomorphism becomes
(RX)(I) ≃ ˆ
C(y(I)I , X)
natural in I and X. We may modify the given right adjoint R so that this isomorphism
becomes an equality. By our smallness assumptions on C and I, we have that y(I)I lives in
the lowest Grothendieck universe in our hierarchy. It follows that R restricts to an operation
on Un for n ≥ 0.7
Pseudofunctorially in a presheaf A, the adjunction (−)I ⊣ R descends to an adjunction
between categories of families over A and AI . We record what we need from this in the rest
of our development.
Lemma 2.2. Let A be a global set and B a global family over AI . Then we have a global
family BI over A with a bijection of global elements
∏
∏
□( A′ BI ◦ f ) ≃ □( (A′ )I B ◦ f I )
natural in global f : A′ → A.
The construction (−)I may be chosen so that:
(1) if B is valued in Un for n ≥ 0, then so is BI ,
(2) the induced isomorphism (B ◦ f I )I ≃ BI ◦ f is an identity.
I
Proof. Let ηA : A
unit of the adjunction at A. We
∑→ R(A ) be the
∏ define BI (a) as the fiber
of R((−).1) : R( AI B) → R(AI ) over ηA (a). Global sections of A′ BI ◦ f I are dotted maps

6This is not part of the axioms in [OP16], but it implies connectivity of I, the first axiom in [OP16], since

left adjoints preserve colimits.
7Without our modification of R, this would only be true up to isomorphism.

## PDF page 11

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:11

making the following diagram commute:
R(
6

A′
Global sections of

∏

f

∑

AI B)



/A

ηA

R((−).1)

/ R(AI ).

(A′ )I B ◦ f are dotted maps making the following diagram commute:

7

(A′ )I

∑

AI B



fI

(−).1

/ AI .

Under transposition of the adjunction, the two are in bijection, naturally in A′ .
Recall the equivalence between maps into a presheaf and families over that presheaf.
Under this equivalence, we can regard (−)I as a functor from global families over A to global
families over AI . The above discussion then shows that (−)I is a right adjoint of (−)I .
Let examine the values of the presheaf BI over the category of elements of A. By Yoneda
and the natural bijection we have just verified, BI (I, a) is naturally isomorphic to the set of
sections of the restriction of B along aI : y(I)I → AI . By our smallness assumptions on C
and I, this is in Un if B is valued in Un (irrespective of the size of A). As in our discussion on
size preservation of R, we may modify the definition of (−)I so that the above isomorphism
becomes an identity. This validates (1) and (2).
In the above
statement,
∏
∏ the given bijection may be reduced to the case where f is an
identity: □( AI B) ≃ □( A BI ). The cost to pay is that the isomorphism BI ◦ f ≃ (B ◦ f I )I
with appropriate coherence becomes primitive (non-derived) data.
We are going to apply Lemma 2.2 in two different instances. The first instance occurs
in the following subsection and is used to build internal universes of fibrant sets, which will
be needed to prove homotopy canonicity. The second (and more complex) instance occurs
in in Subsection 6.1 and is used for interpreting types in the sconing model in the proof of
canonicity.

2.2.1. Fibrant presheaves. Recall the global family hasFill : UωI → Uω from Subsection 1.3.
Applying Lemma 2.2 to hasFill, we obtain global C :∏Uω → Uω such that naturally in a global
set X with global Y
∏ : X → Uω , global elements of x:X I hasFill(Y ◦ x) are in bijection with
global elements of x:X C(Y x). Given a global set X and global Y : X → Uω , we thus have
a logical equivalence (maps back and forth)
∏
□Fill(X, Y ) ←→ □ x:X C(Y x)
(2.1)
natural in X.8
8We record only the logical equivalence instead of an isomorphism so that it will be easier to apply our
constructions in situations where the right adjoint R fails to exist such as Appendix D. Naturality is only
used at one point below, for the forward map, to construct suitable elements of C applied to glueings.

## PDF page 12

28:12

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

∑
Note that C descends to C : Un → Un for n ≥ 0. We write Uifib = A:Ui C(A) for
i ∈ {0, 1, . . . , ω}; we call Uifib ∏
a universe of fibrant sets. Now set X = Uωfib and Y (A, c) = A
in (2.1). We trivially have □ x:X C(Y x), thus get
fill : Fill(Uωfib , λ(A,c) A).

(2.2)

This is essentially the counit of the adjunction defining C. Note that [LOPS18] use modal
extensions of type theory to perform this reasoning internal to presheaves over C.
∏
Remark 2.3. Internally, a map Fill(X, Y ) → x:X C(Y x) does not generally exist for a set
X and Y : X → Uω as for X = 1 one would derive a filling structure for any “homogeneously
fibrant”
set, which is impossible (see [OP16, Remark 5.9]). However, from (2.2) we get a map
∏
C(Y
x) → Fill(X, Y ) natural in X using closure of filling structures under substitution
x:X
(see below).
More examples of the interplay between internal and external reasoning involving
elements of C(X) will occur in Subsubsection 2.2.2 when we reason that closure of Fill under
various type formers, proven internally, transfers to corresponding closure properties of C,
proven externally.

2.2.2. Some general constructions. We recall some constructions of [CCHM18, OP16] in the
internal language.
• Given A : I →
∏ Uω and ab : Ab for b ∈ {0, 1}, dependent paths PathA a0 a1 are the set
of maps p : i:I A i such that p 0 = a0 and p 1 = a1 . We use the same notation for
non-dependent paths.
• For A : Uω , we have a set isContr(A) of witnesses of contractibility, defined using paths.
• Given A, B : Uω with f : A → B, we have the set isEquiv(f ) with elements witnessing
that f is an equivalence,
defined using contractibility of homotopy fibers. We write
∑
Equiv(A, B) = f :A→B isEquiv(f ).
• Given A : Uω , ϕ : F, B : [ϕ] → Uω , and e : [ϕ] → (B tt → A), the glueing Glue A [ϕ ↦→
(B, e)] consists of elements glue a [ϕ ↦→ b] with a : A and b : [ϕ] → B such that e.1 (b tt) = a
on [ϕ] and is defined in such a way that
Glue A [ϕ ↦→ (B, e)] = T tt,
glue a [ϕ ↦→ b] = b tt
on [ϕ]. We have a projection unglue : Glue A [ϕ ↦→ (B, e)] → A.
These operations are valued in Un if their inputs are. We further recall from [CCHM18, OP16]
basic facts about filling structures in the internal language.
• Filling structures are closed under substitution: given f : X ′ → X and Y : X → Uω , any
element of Fill(X, Y ) induces an element of Fill(X ′ , Y ◦ f ), naturally in X ′ .
• Filling structures are closed under exponentiation: given sets S, X and Y : X → Uω , any
element of Fill(X, Y ) induces an element of
∏
Fill(X S , λx s:S Y (x s)),
naturally in S.

## PDF page 13

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:13

products, this
• Filling structures are closed under Π, Σ, Path. For example, for dependent
∏
means the following. Given A : Γ → Uω with Fill(Γ, A) and B : ρ:Γ A ρ → Uω with
∑
Fill( ρ:Γ A ρ, λ(ρ,a) B ρ a), we have
∏
Fill(Γ, λρ:Γ a:A ρ B ρ a).
• The Glue set former preserves filling structures with equivalences. By this, we mean the
following. Let A : Γ → Uω and ϕ : F. For ρ in ∑
Γ and x in [ϕ], let B ρ x : Uω with a map
e ρ x : A ρ → B ρ x. Assume Fill(Γ, A) and Fill( ρ:Γ [ϕ], λ(ρ,x) B ρ tt) and that e ρ tt is an
equivalence for ρ : Γ on [ϕ]. Then we have
Fill(Γ, λρ Glue (A ρ)) [ϕ ρ ↦→ (B ρ tt, e ρ tt)]
and the map unglue ρ from the glue set to A ρ is an equivalence for ρ as above.
All of the above closure observations satisfy naturality under substitution.
Above, we have recorded closure of Fill under various set formers. From this, we use
external reasoning to deduce the corresponding closure properties for C. Specifically, we
have that C is closed under Π, Σ, Path, Glue (adding equivalence data in the case of Glue),
and that C(A) implies C(AS ) for A, S : Uω .9
We explain how this works in the example case of Π.
∏
Given (A, cA ) in Uωfib and ⟨B, cB ⟩ : A → Uωfib , we wish to show C( A B). We set
∑
∆ = (A,cA ):Uωfib A → Uωfib
for the “generic context” of the closure statement. Then the goal is a global element of
∏
∏
((A,cA ),⟨B,cB ⟩):∆ C( A B).
By (2.1), this amounts to a global element of
Fill(∆, λ((A,cA ),⟨B,cB ⟩)

∏

A B).

Now we reason internally. Since Fill is closed under dependent products, the goal reduces to
Fill(∆, λ((A,cA ),⟨B,cB ⟩) A),
∑
Fill( ((A,cA ),⟨B,cB ⟩):∆ A, λ(((A,cA ),⟨B,cB ⟩),a) B a).
Elements of these are given by Remark 2.3 since all families here are valued in fibrant sets
(as witnessed by the components cA and cB ).
Note that in the case of Glue with (A, c) : Uωfib , ϕ : F, ⟨B, d⟩ : [ϕ] → Uωfib , and
e : [ϕ] → Equiv(B tt, A), naturality of the forward map of (2.1) is needed to see that the
element c : C(Glue A [ϕ ↦→ (B, e)]) constructed in the same fashion as above for dependent
products equals d tt : C(B tt) on [ϕ].
As in [CCHM18, OP16, LOPS18], glueing shows Fill(1, Unfib ) for n ≥ 0. Using (2.1), we
conclude C(Unfib ).
Let N denote the natural number object in presheaves over C, the constant presheaf
with value the natural numbers. From [CCHM18, OP16], we have Fill(1, N). Using (2.1),
we conclude C(N).
We justify fibrant indexed inductive sets in Appendix B.
9Note that naturality in S of the latter operation is used in substitutional stability of universes in the

sconing in Section 3.

## PDF page 14

28:14

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

2.3. Standard model. Making the same assumptions on C, I, F as in Subsection 2.2, we
can now specify the standard model S of cubical type theory in the sense of the current
article as a cubical cwf (with respect to parameters C, I, F) purely using the internal language
of the presheaf topos. The cwf is induced by the family over Uωfib given by the first projection
as follows.
• The category of contexts is Uω , with Hom(∆, Γ) the functions from ∆ to Γ.
• The types over Γ are maps from Γ to Uωfib ; a type ⟨A, p⟩ is of level n if A is in Γ → Un .
This is clearly functorial in Γ.
∏
• The elements of ⟨A, p⟩ : Γ → Uωfib are ρ:Γ A ρ. This is clearly functorial in Γ.
• The terminal context is given by 1.
∑
• The context extension of Γ by ⟨A, p⟩ is given by ρ:Γ A ρ, with p, q given by projections
and substitution extension given by pairing.
We briefly go through the necessary type formers and operations, omitting evident details.
Whenever we mention an induced witness of fibrancy, this refers to the observations recorded
in Subsubsection 2.2.2.
∑
• The dependent product of ⟨A, c⟩ : Γ → Uωfib and ⟨B, d⟩ : ρ:Γ A ρ → Uωfib is
∏
⟨λρ a:A ρ B(ρ, a), e⟩
∏
where e ρ : C( a:A ρ B(ρ, a)) is induced by c ρ : C(A ρ) and d ρ a : C(B(ρ, a)) for a : A.
∑
• The dependent sum of ⟨A, c⟩ : Γ → Uωfib and ⟨B, d⟩ : ρ:Γ A ρ → Uωfib is
∑
⟨λρ a:A ρ B(ρ, a), e⟩
where e is induced by c and d.
fib is constantly
• The universe Un : Γ → Un+1
(Unfib , c)
with c : C(Unfib ) as recorded before. According to our definition of the types in S, this
universe is actually Russell-style, i.e., the evident isomorphism Typen (Γ) ∼
= Elem(Γ, Un ) is
an identity.
• The natural number type N : Γ → U0fib is constantly
(N, c)
with c : C(N) as recorded before. The zero and successor constructors and the eliminator
are given by the corresponding features of the natural number object N.
We now turn to the cubical aspects.
• The filling operation
fill : Fill(Γ → Uωfib , λ⟨A,p⟩

∏

ρ:Γ A ρ)

is derived from (2.2) by closure
under exponentiation.
∑ of filling structures ∏
• Given ⟨A, c⟩ : I → Γ →
C(A)
and
a
:
b
A:Uω
ρ:Γ A b ρ for b ∈ {0, 1}, we define
∑
Path(A, a0 , a1 ) : Γ → A:Uω C(A) as
∏
⟨ ρ:Γ Pathλi A i ρ c0 c1 ), d⟩
where d ρ : C(Pathλi A i ρ c0 c1 )) is induced by λi c i ρ. Path abstraction and application
operations are defined from those of Path.

## PDF page 15

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:15

Before defining glue types, we note that the notions isContrc and isEquivc in the cubical
cwf we are defining correspond to the notions isContr and isEquiv.
∏ For example, given a
type A : Γ → Uωfib , then the elements of isContrc (A), given by ρ:Γ isContrc (A).1 ρ, are
∏
in bijection with ρ:Γ isContr(A.1 ρ) naturally in Γ.
• Given ⟨A, c⟩ : Γ → Uωfib , ϕ : F, ⟨T, d⟩ : [ϕ] → Γ → Uωfib , and e : [ϕ] → Equivc (T tt, A), we
define Gluec (⟨A, c⟩, ϕ, ⟨T, d⟩, e) : Γ → Uωfib as
λρ (Glue (A ρ) [ϕ ↦→ (T tt ρ, (e′ tt ρ).1)], q ρ)
where e′ tt ρ : Equiv(T tt ρ, A ρ) is induced by e tt ρ and q ρ is induced by c ρ and λx d x ρ
and λx (e′ tt ρ).2.
We have thus verified the following statement.
Theorem 2.4. Assuming the parameters C, I, F satisfy the assumptions of Subsection 2.2,
the standard model S forms a cubical cwf.

3. Sconing
We make the same assumptions on our parameters C, I, F as in Subsection 2.2. In the global
context, let M be a cubical cwf (with respect to these parameters) denoted Con, Hom, . . . as
in Subsection 1.3. We assume that M is size-compatible with the standard model, by which
we mean Hom(∆, Γ) : Uω for all Γ, ∆ and Elem(Γ, A) : Ui for i ∈ {0, 1, . . . , ω} and all Γ and
A : Typei (Γ). We will then define a new cubical cwf M∗ denoted Con∗ , Hom∗ , . . ., the Artin
glueing of M with the standard model S along an (internal) global sections functor, i.e. the
sconing of M. (We refrain from referring it to as just glueing to avoid confusion with the
glue types of cubical cwfs.)
Recall from Subsection 1.3 the operation fill of M. Instantiating it to the terminal
context, we get □Fill(Type(1), λ∏A Elem(1, A)). Using the forward direction of (2.1), we thus
have an internal operation k : A:Type(1) C(Elem(1, A)).
From now on, we will work in the internal language of presheaves over C. We start by
defining a global sections operation |−| mapping contexts, types, and elements of M to
those of S.
• Given Γ : Con, we define |Γ| : Uω as the set of substitutions Hom(1, Γ). Given a substitution
σ : Hom(∆, Γ), we define |σ| : |∆| → |Γ| as |σ|ρ = σρ. This evidently defines a functor.
• Given A : Type(Γ), we define |A| : |Γ| → Uωfib as |A| ρ = (Elem(1, Aρ), k (A ρ)). This
fib
evidently natural in Γ. If A is of level
∏ n, then |A| : |Γ| → Un .
• Given a : Elem(Γ, A) we define |a| : ρ:Γ (|A| ρ).1 as |a| ρ = aρ. This is evidently natural
in Γ.
Note that |−| preserves the terminal context and context extension up to canonical isomorphism in the category of contexts. One could thus call |−| an (internal) pseudomorphism
cwfs from M to S. The sconing M∗ will be defined as essentially the Artin glueing along
this pseudomorphism, but we will be as explicit as possible and not define Artin glueing at
the level of generality of an abstract pseudomorphism.
For convenience, we also just write |A| : |Γ| → Uω instead of λρ (|A| ρ).1, implicitly
applying the first projection. We also write just |A| for |A| |()| if Γ is the terminal context.

## PDF page 16

28:16

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

3.1. Contexts, substitutions, types, and elements. We start by defining the cwf M∗ .
• A context (Γ, Γ′ ) : Con∗ consists of a context Γ : Con in M and a family Γ′ over |Γ| (which
in the context of Artin glueing should be thought of as a substitution in S from some
context to |Γ|). We think of Γ′ as a proof-relevant computability predicate. A substitution
(σ, σ ′ ) : Hom∗ ((∆, ∆′ ), (Γ, Γ′ )) consists of a substitution σ : ∆ → Γ in M and a map
∏
σ ′ : ν:|∆| ∆′ (ν) → Γ′ (σν).
This evidently has the structure of a category.
• A type (A, A′ ) : Type∗ (Γ, Γ′ ) consists of a type A : Type(Γ) in M and
∏
∏
A′ : ρ:|Γ| ρ′ :Γ′ ρ |A| ρ → Uωfib .
We think of A′ as a fibrant proof-relevant computability family on A. In the abstract
context of Artin glueing for cwfs, we should think of it as
∑
∑
A′ : Type( ρ:|Γ| ρ′ :Γ′ ρ |A| ρ)
in S. However, we choose the former as the official definition so that the construction
∗
of
universes, as we shall see later. Recalling Uωfib =
∑ M from M preserves Russell-style
′
′
X:Uω C(X), we also write ⟨A , fibA′ ⟩ instead of A if we want to directly access the family
and split off its proof of fibrancy.
The type (A, A′ ) is of level n if A and A′ are.
The action of a substitution (σ, σ ′ ) : Hom∗ ((∆, ∆′ ), (Γ, Γ′ )) on (A, A′ ) is given by
(Aσ, λν,ν ′ ,a A′ (σν) (σ ′ ν ν ′ ) a).
• An element (a, a′ ) : Elem∗ ((Γ, Γ′ ), (A, ⟨A′ , fibA′ ⟩)) consists of a : Elem(Γ, A) in M and
∏
∏
a′ : ρ:|Γ| ρ′ :Γ′ ρ A′ (ρ, ρ′ , aρ).
In the context of Artin glueing of cwfs (with types in M∗ presented correspondingly), this
should be thought of as an element
∑
a′ : Elem( ρ:|Γ| Γ′ ρ, λ(ρ,ρ′ ) A′ (ρ, ρ′ , |a| ρ))
of S.
The action of a substitution (σ, σ ′ ) : Hom∗ ((∆, ∆′ ), (Γ, Γ′ )) on the element (a, a′ ) is
given by
(aσ, λν,ν ′ a′ σν (σ ′ ν ν ′ )).
• The terminal context is given by (1, 1′ ) defined by 1′ () = 1.
• The extension in M∗ of a context (Γ, Γ′ ) by a type (A, A′ ) is given by (Γ.A, (Γ.A)′ ) where
∑
(Γ.A′ )(ρ, a) = ρ′ :Γ′ ρ (A′ ρ ρ′ a).1.
The projection p∗ : Hom∗ ((Γ, Γ′ ).(A, A′ ), (Γ, Γ′ )) is (p, p′ ) where
p′ (ρ, a) (ρ′ , a′ ) = ρ′
and the generic term q∗ : Elem((Γ, Γ′ ).(A, A′ )p∗ ) is (q, q′ ) where
q′ (ρ, a) (ρ′ , a′ ) = a′ .
The extension of (σ, σ ′ ) : Hom∗ ((∆, ∆′ ), (Γ, Γ′ )) with (a, a′ ) : Elem∗ ((∆, ∆′ ), (A, A′ )(σ, σ ′ ))
is
((σ, a), λν,ν ′ (σ ′ ν ν ′ , a′ ν ν ′ )).

## PDF page 17

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:17

3.2. Type formers and operations.
3.2.1. Dependent products. Let
(A, ⟨A′ , fibA′ ⟩) : Type∗ (Γ, Γ′ ),
(B, ⟨B ′ , fibB ′ ⟩) : Type∗ ((Γ, Γ′ ).(A, ⟨A′ , fibA′ ⟩)).
We define the dependent product
Π∗ ((A, ⟨A′ , fibA′ ⟩), (B, ⟨B ′ , fibB ′ ⟩)) = (Π(A, B), ⟨Π(A, B)′ , fibΠ(A,B)′ ⟩)
where
Π(A, B)′ (ρ, ρ′ , f ) =

∏

a:|A| ρ

∏

′
′ ′
a′ :A′ ρ ρ′ a B (ρ, a) (ρ , a ) (app(f, a))

and fibΠ(A,B)′ (ρ, ρ′ , f ) is given by closure of C under dependent product applied to (|A| ρ).2,
fibA′ ρ ρ′ a for a : |A| ρ, and fibB ′ (ρ, a) (ρ′ , a′ ) (app(f, a)) for additionally a′ : A′ ρ ρ′ a.
Given an element (b, b′ ) of (B, ⟨B ′ , d⟩)) in M∗ , we define the abstraction lam∗ (b, b′ ) =
(lam(b), lam(b)′ ) where
lam(b)′ ρ ρ′ a a′ = b′ (ρ, a) (ρ′ , a′ ).
Given elements (f, f ′ ) of Π∗ ((A, ⟨A′ , c⟩), (B, ⟨B ′ , d⟩)) and (a, a′ ) of (A, ⟨A′ , fibA′ ⟩)) in
∗
M , we define the application app∗ ((f, f ′ ), (a, a′ )) = (app(f, a), app(f, a)′ ) where
app(f, a)′ ρ ρ′ = f ′ ρ ρ′ aρ (a′ ρ ρ′ ).
3.2.2. Dependent sums. Let
(A, ⟨A′ , fibA′ ⟩) : Type∗ (Γ, Γ′ ),
(B, ⟨B ′ , fibB ′ ⟩) : Type∗ ((Γ, Γ′ ).(A, ⟨A′ , fibA′ ⟩)).
We define the dependent sum
Σ∗ ((A, ⟨A′ , fibA′ ⟩), (B, ⟨B ′ , fibB ′ ⟩)) = (Σ(A, B), ⟨Σ(A, B)′ , fibΣ(A,B)′ ⟩)
where
Σ(A, B)′ ρ ρ′ (pair(a, b)) =

∑

′
′ ′
a′ :A′ ρ ρ′ a B (ρ, a) (ρ , a ) b

and fibΣ(A,B)′ ρ ρ′ (pair(a, b)) is given by closure of C under dependent sum applied to
fibA′ ρ ρ′ a and fibB ′ (ρ, a) (ρ′ , a′ ) b.
Given elements (a, a′ ) of (A, ⟨A′ , fibA′ ⟩) and (b, b′ ) of (B, ⟨B ′ , fibB ′ ⟩)[(a, a′ )] in M∗ , we
define the pairing pair∗ ((a, a′ ), (b, b′ )) = (pair(a, b), ⟨a′ , b′ ⟩).
Given an element (pair(a, b), ⟨a′ , b′ ⟩) of Σ∗ ((A, ⟨A′ , fibA′ ⟩), (B, ⟨B ′ , fibB ′ ⟩)) in M∗ , we
define the projections fst∗ (pair(a, b), ⟨a′ , b′ ⟩) = (a, a′ ) and snd∗ (pair(a, b), ⟨a′ , b′ ⟩) = (b, b′ ).
3.2.3. Universes. We define the universe U∗n : Type∗ (Γ, Γ′ ) as U∗n = (Un , ⟨U′n , fibU′n ⟩) where
U′n ρ ρ′ A = |A| ρ → Unfib
and fibU′n ρ ρ′ A is given by C(Unfib ) and closure of C under exponentiation (note that fibrancy
of |A| ρ is not used). We have carefully chosen our definitions so that the evident natural
isomorphism Elem∗ ((Γ, Γ′ ), U∗n ) ∼
= Type∗n (Γ, Γ′ ) is an identity if the corresponding isomorphism
in Typen (Γ) ∼
= Elem(Γ, Un ) in M is an identity. Thus, Russell-style universes are preserved
by our presentation of the sconing model.

## PDF page 18

28:18

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

3.2.4. Natural numbers. As per Appendix B, we have a fibrant indexed inductive set N′ : |N| →
U0fib (where N : Type0 (1), hence |N| : U0 ) with constructors
0′ : N′ 0,
∏
S′ : n:|N| ρ N′ n → N′ (S n).
In context (Γ, Γ′ ) : Con∗ , we then define N∗ = (N, λρ,ρ′ N′ ). We have 0∗ = (0, λρ,ρ′ 0′ ) and
S∗ (n, n′ ) = (S(n), λρ,ρ′ S′ nρ n′ ) for (n, n′ ) : Elem∗ ((Γ, Γ′ ), N∗ ).
Given (P, P ′ ) : Type((Γ, Γ′ ).N∗ ) with
(z, z ′ ) : Elem∗ ((Γ, Γ′ )(P, P ′ )[0∗ ]),
(s, s′ ) : Elem∗ ((Γ, Γ′ ).N∗ .(P, P ′ ), (P, P ′ )(p, S ∗ (q))p)
and (n, n′ ) : Elem∗ ((Γ, Γ′ ), N∗ ), we define the elimination
natrec∗ ((P, P ′ ), (z, z ′ ), (s, s′ ), (n, n′ )) = (natrec(P, z, s, n), λρ,ρ′ h′ nρ (n′ ρ ρ′ ))
where
h′ :

′
′
′
+
+++ , m))
m′ :N′ m P (ρ, m) (ρ , m ) (natrec(P ρ , zρ, sρ
is given by induction on N′ with defining equations

∏

m:|N|

∏

h′ 0 0′ = z ′ ρ ρ′ ,
h′ (S(n)) (S′ n n′ ) = s′ (ρ, n, natrec(P, z, s, n)) (ρ′ , n′ , h′ n n′ ).
3.2.5. Dependent paths. Let ⟨A, A′ ⟩ : I → Type∗ (Γ, Γ′ ) and (ab , a′b ) : Elem∗ ((Γ, Γ′ ), (A b, A′ b))
for b ∈ {0, 1}. We then define
Path∗ (⟨A, A′ ⟩, (a0 , a′0 ), (a1 , a′1 )) = (Path(A, a0 , a1 ), ⟨Path(A, a0 , a1 )′ , fibPath(A,a0 ,a1 )′ ⟩)
where
Path(A, a0 , a1 )′ ρ ρ′ (⟨⟩(u)) = Pathλi (A′ i ρ ρ′ (u i)).1 (a′0 ρ ρ′ )(a′1 ρ ρ′ )
and fibPath(A,a0 ,a1 )′ ∏
ρ ρ′ (⟨⟩(u)) is closure of C under Path applied to (A′ i ρ ρ′ (u i)).2 for i : I.
′
Given ⟨u, u ⟩ : i:I Elem∗ ((Γ, Γ′ ), (A i, A′ i)), we define the path abstraction as
⟨⟩∗ (⟨u, u′ ⟩) = (⟨⟩(u), λρ,ρ′ ,i u′ i ρ ρ′ ).
Given (p, p′ ) : Elem∗ ((Γ, Γ′ ), Path∗ (⟨A, A′ ⟩, (a0 , a′0 ), (a1 , a′1 ))) and i : I, we define the
path application
ap∗ (p, i) = (ap(p, i), λρ,ρ′ u′ ρ ρ′ i).
3.2.6.
Filling operation. Given ⟨A, A′ ⟩ : I → Type∗ (Γ, Γ′ ), ϕ : F, b ∈ {0, 1}, and ⟨u, u′ ⟩ :
∏
∗
′
′
i:I [ϕ] ∨ (i = b) → Elem ((Γ, Γ ), (A i, A i)), we have to extend u to
∏
fill∗ (⟨A, A′ ⟩, ϕ, b, ⟨u, u′ ⟩) : i:I Elem∗ ((Γ, Γ′ ), (A i, A′ i)).
We define fill∗ (⟨A, A′ ⟩, ϕ, b, ⟨u, u′ ⟩) = ⟨fill(A, ϕ, b, u), fill(A, ϕ, b, u)′ ⟩ where
fill(A, ϕ, b, u)′ i ρ ρ′ : A′ i ρ ρ′ (fill(A, ϕ, b, u) i)ρ
is defined using fill from (2.2) as
fill(A, ϕ, b, u)′ i ρ ρ′ = fill(λi A′ i ρ ρ′ (fill(A, ϕ, b, u) i)ρ, ϕ, b, λi,x u′ i x ρ ρ′ ).

## PDF page 19

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:19

3.2.7. Glue types. Before defining the glueing operation in M∗ , we will develop several
lemmas relating notions such as contractibility and equivalences in M with∏the corresponding
notions of Subsection 2.2. Given f : Elem(Γ, A → B) in M, we write |f | : ρ:|Γ| |A| ρ → |B| ρ
for |f | ρ a = app(f ρ, a). This notation overlaps with the action of |−| on elements, but we
will not use that one here.
Just in this subsection, we will use the alternative definition via given left and right
homotopy inverses instead of contractible homotopy fibers of both equivalences Equivc in the
cubical cwf M and equivalences Equiv in the (current) internal language. In both settings,
there are maps back and forth to the usual definition, which are furthermore natural in the
context in the case of the cubical cwf M. The statements we will prove are then also valid
for the usual definition.
Lemma
3.1. Given f : Elem(Γ, A → B) in M with Elem(Γ, isEquivc (f )), we have
∏
isEquiv(|f
| ρ). This is natural in Γ.
ρ:|Γ|
Proof. A (left or right) homotopy inverse g : Elem(Γ, B → A) to f in M becomes a (left or
right, respectively) homotopy inverse |g| ρ to |f | ρ for ρ : |Γ|.
Lemma 3.2. Given (f, f ′ ) : Elem((Γ, Γ′ ), (A, A′ ) → (B, B ′ )) in M∗ , the following statements
are logically equivalent, naturally in (Γ, Γ′ ):
Elem((Γ, Γ′ ), isEquiv∗c (f, f ′ )),
∏
∏
∑
Elem(Γ, isEquivc (f )) × ρ:|Γ| ρ′ :Γ′ ρ isEquiv( |f | ρ f ′ ρ ρ′ ),
∏
∏
∏
Elem(Γ, isEquivc (f )) × ρ:|Γ| ρ′ :Γ′ ρ a:|A| ρ isEquiv(f ′ ρ ρ′ a)
∑
∑
∑
where |f | ρ f ′ ρ ρ′ : a:|A| ρ A′ ρ ρ′ a → b:|B| ρ B ′ ρ ρ′ b.

(3.1)
(3.2)
(3.3)

Proof. Let us only look at homotopy left inverses.
For ∑
(3.1) → (3.2), a∑homotopy left inverse (g, g ′ ) to (f, f ′ ) in M∗ gives a homotopy left
inverse |g| ρ g ′ ρ ρ′ to |f | ρ f ′ ρ ρ′ for all ρ, ρ′ .
For (3.2) → (3.3), we use Lemma 3.1 and note that a fiberwise map over an equivalence
is a fiberwise equivalence exactly if it is an equivalence on total spaces (the corresponding
statement for identity types instead of paths is [Uni13, Theorem 4.7.7]).
For (3.3) → (3.1), given a homotopy left inverse g to the equivalence f in M and a
homotopy left inverse g ′ ρ ρ′ a : B ′ ρ ρ′ (|f | a) → A′ ρ ρ′ a to f ′ ρ ρ′ a for all ρ, ρ′ , a, we use
Lemma 3.1 to transpose g ′ to the second component g ′ ρ ρ′ b : B ′ ρ ρ′ b → A′ ρ ρ′ (|g| b) for all
ρ, ρ′ , b of a homotopy left inverse (g, g ′ ) to (f, f ′ ) in M∗ .
We can now define glue types in M∗ . Let (A, A′ ) : Type(Γ, Γ′ ), ϕ : F, ⟨T, T ′ ⟩ : [ϕ] →
Type(Γ, Γ′ ), and
⟨e, e′ ⟩ : [ϕ] → Elem((Γ, Γ′ ), Equiv∗c ((T tt, T ′ tt), (A, A′ ))).
We define
Glue∗c ((A, A′ ), ϕ, ⟨T, T ′ ⟩, ⟨e, e′ ⟩) = (Gluec (A, ϕ, , T, e), ⟨G′ , fibG′ ⟩)
where
G′ ρ ρ′ (glue(a, t)) = Glue (A′ ρ ρ′ a).1 [ϕ ↦→ (T ′ tt ρ ρ′ (t tt), ((e′ tt ρ ρ′ ).1 (t tt)))]
where fibG′ ρ ρ′ (glue(a, t)) is given by closure of C under Glue applied to (A′ ρ ρ′ a).2 and
T ′ tt ρ ρ′ (t tt) on [ϕ] and the witness that (e′ tt ρ ρ′ ).1 (t tt) is an equivalence provided by the

## PDF page 20

28:20

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

direction from (3.1) to (3.3) of Lemma 3.2. We define unglue∗ = (unglue, unglue′ ) where
unglue′ ρ ρ′ (glue(a, t)) = unglue.
Given (a, a′ ) : Elem((Γ.Γ′ ), (A, A′ )) and
(t, t′ ) : [ϕ] → Elem((Γ, Γ′ ), (T tt, T ′ tt))
such that app∗ (fst∗ (e, e′ ) tt, (t, t′ ) tt) = (a, a′ ) on [ϕ], we define glue∗ ((a, a′ ), (t, t′ )) as the
pair (glue(a, t), glue(a, t)′ ) where
glue(a, t)′ ρ ρ′ = glue (a′ ρ ρ′ ) [ϕ ↦→ t′ tt ρ ρ′ ].

3.3. Main result. One checks in a mechanical fashion that the operations we have defined
above satisfy the required laws, including stability under substitution in the context (Γ, Γ′ ).
We thus obtain the following statement.
Theorem 3.3 (Sconing). Assume the parameters C, I, F satisfy the assumptions of Subsection 2.2. Then given any cubical cwf M that is size-compatible in the sense of the beginning
of Section 3, the sconing M∗ is a cubical cwf with operations defined as above. We further
have a morphism M∗ → M of cubical cwfs given by the first projection.

4. Homotopy canonicity
We fix parameters C, I, F as before. To make our homotopy canonicity result independent of
Conjecture 2.1 concerning initiality of the term model, we phrase it directly using the initial
model I, initial in the category of cubical cwfs with respect to the parameters C, I, F. Its
existence can be justified generically following [Ste19, PV07]. It is size-compatible in the
sense of Section 3: internally, HomI (∆, Γ) and ElemI (Γ, A) live in the lowest universe U0 for
all Γ, ∆, A.
Theorem 4.1 (Homotopy canonicity). Assume the parameters C, I, F satisfy the assumptions
of Subsection 2.2. In the internal language of presheaves over C, given a closed natural n :
Elem(1, N) in the initial model I, we have a numeral k : N with p : Elem(1, Path(N, n, Sk (0))).
Proof. We start the arguing reasoning externally. Using Theorem 3.3, we build the sconing
I ∗ of I. Using initiality, we obtain a section F of the cubical cwf morphism I ∗ → I.
Let us now proceed in the internal language. Recall
of Subsubsec∑ the construction
′
∗
tion 3.2.4 of natural numbers in I . We observe that n:|N| N n forms a fibrant natural
number set (in the sense of Appendix
B). It is thus homotopy equivalent to N. Under this
∑
equivalence, the first projection n:|N| N′ n → |N| implements the map sending k : N to Sk (0).
Inspecting the action of F on n : Elem(1, N), we obtain n′ : N′ n. By the preceding
paragraph, this corresponds to k : N with a path p′ : I → |N| from n to Sk (0). Now p = ⟨⟩(p′ )
is the desired witness of homotopy canonicity.

## PDF page 21

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:21

5. Extensions

5.1. Identity types. Our treatment extends to the variation of cubical cwfs that includes
identity types.
Identity types in a cubical cwf denoted as in Subsection 1.3 consist of the following
operations and laws (omitting stability under substitution), internal to presheaves over
C. Fix A in Type(Γ). Given x, y in Elem(Γ, A), we have Id(A, x, y) in Type(Γ), of level
n if A is. Given a in Elem(Γ, A), we have refl(a) in Elem(Γ, Id(A, a, a)). Given P in
Type(Γ.A.Ap.Id(App, qp, q)) and d in Elem(Γ.A, P [q, q, refl(q)]) and x, y in Elem(Γ, A) and
p in Elem(Γ, Id(A, x, y)), we have J(P, d, x, y, p) in Elem(Γ, P [x, y, p]). We have
J(P, d, a, a, refl(a)) = d[a].
We can interpret univalent type theory in any cubical cwf with identity types as per
Remark 1.1.
The standard model of Subsection 2.3 has identity type Id(⟨A, fibA ⟩, x, y) : Type(Γ) given
∏
by ρ:Γ IdA ρ (x ρ) (y ρ) using Andrew Swan’s construction of Id referenced in Appendix B.
We omit the evident description of the remaining operations.
To obtain homotopy canonicity in this setting, it suffices to extend the sconing construction M∗ of Section 3 to identity types. Given A : Type(1) and A′ : |A| → Uωfib , we define
Id′A,A′ as the fibrant indexed inductive set (as per Appendix B) over x, y : |A|, p : |Id(A, x, y)|,
x′ : A′ x, y ′ : A′ y with constructor
∏
∏
refl′ : a:|A| a′ :A′ a Id′A,A′ a a (refl(a)) a′ a′ .
Now fix (A, A′ ) : Type∗ (Γ, Γ′ ). Given ρ : |Γ|, ρ′ : Γ′ ρ, and elements (x, x′ ), (y, y ′ ) of
(A, A′ ) in M∗ , we define
Id∗ ((A, A′ ), (x, x′ ), (y, y ′ )) = (Id(A, x, y), λρ,ρ′ ,p Id′Aρ,A′ ρ ρ′ xρ yρ p (x′ ρ ρ′ ) (y ′ ρ ρ′ )).
Given an element (a, a′ ) of (A, A′ ) in M∗ , we define refl∗ (a, a′ ) = (refl(a), refl(a)′ ) where
refl(a)′ ρ ρ′ = refl′ aρ (a′ ρ ρ′ ).
The eliminator J((C, C ′ ), (d, d′ ), (x, x′ ), (y, y ′ ), (p, p′ )) is defined as
(J(C, d, x, y, p), λρ,ρ′ h′ xρ yρ pρ (x′ ρ ρ′ ) (y ′ ρ ρ′ ) (p′ ρ ρ′ ))
where
∏
∏
∏
∏
∏
h′ : x,y:|A| ρ p:|Id(A,x,y)| ρ x′ :A′ ρ′ y′ :A′ ρ′ p′ :Id′

x y p x′ y ′
Aρ,A′ ρ ρ′

P ′ (ρ, x, y, p) (ρ′ , x′ , y, p′ ) (J(P ρ+++ , dρ+ , x, y, p))
is given by induction on Id′Aρ,A′ ρ ρ′ via the clause
h′ a a (refl(a)) a′ a′ (refl′ a a′ ) = d′ (ρ, a) (ρ′ , a′ ).

## PDF page 22

28:22

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

5.2. Higher inductive types. Our treatment extends to higher inductive types [Uni13],
following the semantics presented in [CHM18]. Crucially, we have fibrant indexed higher
inductive sets in presheaves over C as we have what we would call fibrant uniformly
indexed higher inductive sets in the same fashion as in [CHM18] and fibrant identity
sets [CCHM18, OP16], mirroring the derivation of fibrant indexed inductive sets from fibrant
uniformly indexed inductive sets and fibrant identity sets recollected in Appendix B.10
Let us look at the case of the suspension operation in a cubical cwf, where Susp(A) :
Type(Γ) has constructors north, south and merid(a, i) for a : A and i : I with merid(a, 0) =
north and merid(a, 1) = south.
For the sconing model of Section 3, we define for A : Type(1) and A′ : |A| → Uωfib the
indexed higher inductive set Susp′A,A′ over |Susp(A)| with constructors
north′ : Susp′A,A′ north,
south′ : Susp′A,A′ south,
merid′ a a′ i : (Susp A)′ (merid(a, i))[i = 0 ↦→ north′ , i = 1 ↦→ south′ ]
for a : |a| and a′ : A′ a and i : I (using the notation of [CHM18]). In the above translation to
a uniformly indexed higher inductive set, the constructor north′ will for example be replaced
by
north′′ : Id|Susp(A)| u north → Susp′A,A′ u.
Given (A, A′ ) : Type∗ (Γ, Γ′ ), we then define
Susp∗ (A, A′ ) = (Susp(A), λρ,ρ′ Susp′Aρ,A′ ρ ρ′ ),
with constructors and eliminator treated as in Subsection 5.1.

6. Canonicity
The goal of this section is to show canonicity for cubical type theory, stating that any closed
term of type N is (strictly) equal to a numeral. This is a priori a stronger result than merely
homotopy canonicity. However, it requires us to add further computation rules for the filling
operation to the theory. For this purpose, we have defined in Subsection 1.4 the notion of
computational cubical cwf, modelling a modified version of cubical type theory where the
filling operation is replaced by the composition operation (filling is then a derived operation).
This is our notion of model in this section.
The main point is how to define the right notion of computability structure. Once this
is done, we can essentially construct the sconing model as in [Coq19]. If we apply this to the
initial computational cubical cwf, we get the canonicity result: any closed natural number
term is convertible to a numeral. This result was already proved in [Hub19], but like for
the proof in [Coq19], our new argument completely avoids the need to define a reduction
relation, which is quite subtle for cubical type theory in [Hub19] since it is not closed under
name substitution.
As in Subsection 1.4, we have not just connection structure on the interval, but also a
compatible reversal structure. Other than that, we make the same assumptions on the I
and F as in Subsection 2.2. Starting from an arbitrary computational cubical cwf M in the
10We stress that the use of “set” in this context refers to the types of the language of presheaves over C,

not homotopy sets.

## PDF page 23

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:23

global context satisfying size-compatibility as in Section 3, we build a new computational
cwf M∗ , the sconing of M.

6.1. Sconing model: cwf structure. The underlying category of M∗ is defined as in
Section 3. It is the Artin glueing of M along the global sections functor |−| : M → Uω .
(Recall that |Γ| is Hom(1, Γ) for Γ in Con. In particular, a context in M∗ is a pair (Γ, Γ′ )
where Γ is a context in M and Γ′ : |Γ| → Uω .)
In contrast to Section 3, we cannot view the rest of the structure M∗ as being obtained
by glueing along the pseudomorphism |−| : M → S of (computational) cubical cwfs. In
particular, we will not make use the standard model S. Rather, M∗ can be seen as the total
space of a fibration that presents a fibred version of the standard model over M. In the
definition of types, we need to track computability of the composition operation, expressed
using the right adjoint to exponentiation with I to get a fiberwise∑
notion.
For A in Type(1), we write |A| for Elem(1, A). Set Predn = A:Type(1) |A| → Un . For
λi (Ai , A′i ) in PredIω , we define Red(λi (Ai , A′i )) to be the type of operations c taking as
argument ψ in F and a family ui , u′i for [ψ] ∨ (i = 0) with ui in Ai and u′i in A′i ui and
producing an element c(ψ, u, u′ ) in A′1 (comp(A, ψ, u)) which is equal to u′1 for ψ = 1.
Proposition 6.1. We∏have R : Predω →∏Uω with, naturally in global A and B : A → Predω ,
a bijection between □( A R ◦ B) and □( AI Red ◦ B I ). For n ≥ 0, we have that R descends
to an operation R : Predn → Un .
Proof. This follows from Lemma 2.2.
∏
Proposition 6.2. Given e in i:I R(Ai , A′i ), there is an operation c(e) which, given ψ in F
and u′i in A′i ui for [ψ] ∨ (i = 0), produces an element c(e)(ψ, u, u′ ) in A′1 (comp(λi Ai , ψ, u))
which is equal to u′1 for [ψ].
∑
Proof. This follows from Proposition 6.1 by setting T = Predω R.
Remark 6.3. Define C(X) for X : Uω as in Subsubsection
2.2.1, but using composition
∏
instead of filling. As in Section 3, we have a map k : A:Type(1) C(|A|). In the same fashion
∑
∑
as above for R, one may construct C ′ over A:Uω c:C(A) A′ : A → Uω encoding that the
family A′ has “composition over c”. Then R can be defined as the restriction of C ′ along
the map induced by k. Under the equivalence between families A′ : A → Uω over A and
A : Uω with a map p : A → A, this corresponds to an element of C(A) such that p forms a
composition-preserving morphism of fibrant types, a notion defined (like C and C ′ ) using
the adjunction recorded in Lemma 2.2.
The closure properties of R under type formers proved in Subsection 6.2 and Lemma 6.6
below can be proved at the level of C ′ . This has the advantage of eliminating the dependency
on the computational cubical cwf M (in the case of natural numbers, the input is instead a
natural number algebra in fibrant types). Then the actual sconing construction can proceed
without external reasoning as in Section 3.
The sconing of the standard model for computational cwfs (defined as S in Subsection 2.3,
but using composition instead of filling) will coincide, externally, with the standard model
constructed internally in presheaves over [1] × C (where [1] is the poset with elements 0 < 1)
with interval object and cofibration classifier defined by projection to C.

## PDF page 24

28:24

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

We define Type∗ (Γ, Γ′ ) to be the set of triples (A, A′ , eA ) where A is in Type(Γ) and
′
A ρ ρ′ is in |A ρ| → Uω for ρ in |Γ| and ρ′ in Γ′ ρ and eA ρ ρ′ is in R(Aρ, A ρ ρ′ ) for ρ and ρ′
as before.
We define Elem∗ ((Γ, Γ′ ), (A, A′ , eA )) to be the set of pairs (a, a′ ) where a is in Elem(Γ, A)
and a′ ρ ρ′ is in A′ ρ ρ′ (aρ) for ρ in |Γ| and ρ′ in Γ′ ρ.
Since the elements do not make use of the last component of the triple defining a type,
the operations involving context extension are defined as in Subsection
∑ 3.1. ′For ′example, we
′
′
′
′
define (Γ, Γ ).(A, A , eA ) to be (Γ.A, (Γ.A )) where (Γ.A) (ρ, u) is ρ′ :Γ′ ρ A ρ ρ u.
6.2. Example of dependent sum types. Before explaining the example of the dependent
sum type, we need the following preliminary lemma. It intuitively says that the filling
operation is computable if the composition operation is computable.
∏
Lemma 6.4. Given e in i:I R(Ai , A′i ), the filling operation on A is “computable”: for ψ in
F and a partial family ui of elements in |Ai | together with u′i in A′i ui defined for [ψ] ∨ (i = 0),
then for any r in I we have
fill′ (A, ψ, u, u′ ) r : A′r (fill(A, ψ, u) r)
equal to u′r for [ψ] ∨ (r = 0).
∏
Proof. Given r in I, we define er in i:I R(Ai∧r , A′i∧r ) by er i = er∧i . Using Proposition 6.2,
we can define
fill′ (A, ψ, u, u′ ) r = c(er )(ψ, ur , u′r )
with ur i x = u (i ∧ r) x and u′r i x = u′ (i ∧ r) x.
∏
Given (A, A′ ) in Predω and B : Type(1.A) and B ′ : u:|A| A′ u → |B[u]| → Uω we define
Σ(A, B)′ by
∑
Σ(A, B)′ w = u′ :A′ (fst(w)) B ′ (fst(w)) u′ (snd(w)).
We then want to define an operation
∏
R(A, A′ ) → ( u:|A|,u′ :A′ u R(B[u], B ′ u u′ )) → R(Σ(A, B), Σ(A, B)′ ).
In order to do this, we consider the iterated dependent sum ∆ corresponding to the context
(A, A′ ) : Predn ,
B : Typen (A),
∏
B ′ : u:|A| A′ u → |B[u]| → Un ,
eA : R(A, A′ ),
∏
∏
eB : u:|A| u′ :A′ u R(B[u], B ′ u u′ ).
We want to build a global element of
∏

′
(A,A′ ,B,B ′ ,eA ,eB ):∆ R(Σ(A, B), Σ(A, B) ).

Using Proposition 6.1, we are reduced to show the following statement.
Proposition 6.5. There is an element of
∏

′
λi (Ai ,A′i ,Bi ,Bi′ ,eiA ,eiB ):∆I Red(λi (Σ(Ai , Bi ), Σ(Ai , Bi ) )).

## PDF page 25

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:25

′
i
′
Proof. We assume a family
∏ Ai , Ai ′ in Predn and eA in R(Aii , Ai )′ for i : I. We′ also′ have
′
Bi : Typen (Ai ) and Bi in u:|Ai | Ai u → |Bi [u]| → Un and eB u u in R(Bi [u], Bi u u ). We
also have ψ in F with pair(ai , bi ) : Σ(Ai , Bi ) and a′i in A′i ai and b′i in Bi′ ai a′i bi defined for
[ψ] ∨ (i = 0).
Given all this, we want to build

(a′1 , b′1 ) : Σ(A1 , B1 )′ (comp(Σ(A, B), ψ, (a, b))).
By the computation rule for Σ, we have
comp(Σ(A, B), ψ, (a, b)) = (comp(A, ψ, a), comp(λi B[u i], ψ, b))
where u = fill(A, ψ, a).
Using Lemma 6.4, we have u′ = fill′ (A, ψ, a, a′ ) and we define a′1 = u′ 1. We next
define eB i = eiB (u i) (u′ i), and using Proposition 6.2, we take b′1 = c(eB )(ψ, b, b′ ).
We can use these results to interpret dependent sum types in the model M∗ , following
essentially the interpretation in [Coq19].
Given (A, A′ , eA ) in Type∗ (Γ, Γ′ ) and (B, B ′ , eB ) in Type∗ ((Γ, Γ′ ).(A, A′ , eA )) we define
T, T ′ , eT where T = Σ(A, B) in Type∗ (Γ, Γ′ ).
′ in |A | → U . We also have
Given ρ and ρ′ we have A1 = Aρ in Type(1) and A′1 = A′ ρ ρ∏
1
ω
+
′
′
′
′
B1 = Bρ in Type(A1 ) and B1 uu = B (ρ, fst(w))(ρ , u ) in u:|A1 | A′1 u → |B1 [u]| → Uω
since B1 [u] = Bρ+ [u] = B(ρ, u). We can then define T ′ ρ ρ′ to be Σ(A1 , B1 )′ and use (1) to
define eT ρ ρ′ .
6.3. Natural numbers. Let N be the (internal) set of natural numbers (given by the
constant presheaf of natural numbers). We have a canonical map∑quote : N → |N| sending k
to Sk (0). We define a (non-fibrant) family N′ over |N| by N′ (t) = k:N t =|N| quote(k) (using
the strict equality on the set |N|).11
Lemma 6.6. We have an element of R(N, N′ ).
Proof. Using the adjoint definition of R in Proposition 6.1, we must build c : Red(λi (N, N′ )).
Exponentiation with I preserves external coproducts since I is tiny. Since N is a countable
coproduct of 1, it follows that any function I → N is constant (formally, factors uniquely
through I → 1).
Let ui : |N| and u′i : N′ ui for [ψ]∨(i = 0). The latter means ki : N such that ui = quote(ki )
for [ψ] ∨ (i = 0). Using the observation from the previous paragraph, there is unique k : N
such that ki = k for [ψ] ∨ (i = 0). From the equations for the composition operation on N in
a computational cubical cwf and induction on k, we get that
comp(λi N, ψ, λi,x ui ) = comp(λi N, ψ, λi,x quote(k)) = quote(k).
We are forced to set c(ψ, u, u′ ) = (k, tt).
This provides the interpretation of the type of natural numbers in the model M∗ .
We see here a key difference compared to the sconing model used for proving homotopy
canonicity: the computability predicate used in this case is not valued in fibrant sets. Note
11An isomorphic alternative is to define N′ as a (non-fibrant) indexed inductive set in the presheaf model,
with constructors of type N′ 0 and N′ n → N′ (S n) for n : |N|. Indeed, it is this approach that generalizes to
the interpretation of inductive types with parameters.

## PDF page 26

28:26

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

∑
that the family k:N |Path(N, t, quote(k))| for t : |N| is fibrant, but would not work for showing
canonicity since it does not support an interpretation of natrec.
6.4. Proof of canonicity. Starting from any computational cubical cwf M, we have built a
new model M∗ , the associated computability model, with a (strict) projection map M∗ → M.
Like in [Coq19], if we apply this to the initial model, we get that any closed term of type N
is “computable”, i.e., is strictly equal to a numeral.

Conclusion
We have given proofs of two forms of canonicity for cubical type theory. The first one is
homotopy canonicity (every closed term of type N is path equal to a numeral) in a cubical
type theory without structural computation rules for the composition operation. The second
one is canonicity (every closed term of type N is strictly equal to a numeral) in a cubical type
theory with these computation rules. While our arguments rely on an interplay between
internal and external reasoning, the main part of the first argument can be seen as happening
internally in the model of fibrant sets. The second argument can hopefully be refined to a
constructive proof of normalisation.

References
+

[ABC 21] C. Angiuli, G. Brunerie, T. Coquand, R. Harper, K.-B. Hou (Favonia), and D. R. Licata. Syntax
and models of cartesian cubical type theory. Mathematical Structures in Computer Science,
31:424–468, 2021. doi:10.1017/S0960129521000347.
[Acz99]
P. Aczel. On relating type theories and set theories. In T. Altenkirch, B. Reus, and
W. Naraschewski, editors, Types for Proofs and Programs, volume 1657 of Lecture Notes
in Computer Science, pages 1–18. Springer Verlag, Berlin, Heidelberg, New York, 1999.
doi:10.1007/3-540-48167-2_1.
[BCH14] M. Bezem, T. Coquand, and S. Huber. A model of type theory in cubical sets. In R. Matthes and
A. Schubert, editors, 19th International Conference on Types for Proofs and Programs (TYPES
2013), volume 26 of Leibniz International Proceedings in Informatics (LIPIcs), pages 107–128.
Schloss Dagstuhl–Leibniz-Zentrum fuer Informatik, 2014. doi:10.4230/LIPIcs.TYPES.2013.107.
[CCHM18] C. Cohen, T. Coquand, S. Huber, and A. Mörtberg. Cubical type theory: A constructive
interpretation of the univalence axiom. In T. Uustalu, editor, 21st International Conference on
Types for Proofs and Programs (TYPES 2015), volume 69 of Leibniz International Proceedings in
Informatics (LIPIcs). Schloss Dagstuhl–Leibniz-Zentrum fuer Informatik, 2018. doi:10.4230/
LIPIcs.TYPES.2015.5.
[CHM18] T. Coquand, S. Huber, and A. Mörtberg. On higher inductive types in cubical type theory. In
Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science, LICS ’18,
pages 255–264, New York, NY, USA, 2018. ACM. doi:10.1145/3209108.3209197.
[Coq18]
T. Coquand. A survey of constructive presheaf models of univalence. ACM SIGLOG News,
5(3):54–65, 2018. doi:10.1145/3242953.3242962.
[Coq19]
T. Coquand. Canonicity and normalization for dependent type theory. Theoretical Computer
Science, 777:184–191, 2019. doi:10.1016/j.tcs.2019.01.015.
[Dyb96]
P. Dybjer. Internal Type Theory. In Lecture Notes in Computer Science, pages 120–134. Springer
Verlag, Berlin, Heidelberg, New York, 1996. doi:10.1007/3-540-61780-9_66.
[Ehr88]
T. Ehrhard. Une sémantique catégorique des types dépendants: Application au Calcul des Constructions. Phd thesis, University Paris VII, 1988.
[Eil39]
S. Eilenberg. On the relation between the fundamental group of a space and the higher homotopy
groups. Fundamenta Mathematicae, 32(1):169–175, 1939. doi:10.4064/fm-32-1-167-175.

## PDF page 27

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:27

N. Gambino and M. Hyland. Wellfounded trees and dependent polynomial functors. In International Workshop on Types for Proofs and Programs, pages 210–225. Springer, 2003.
doi:10.1007/978-3-540-24849-1_14.
[GK13]
N. Gambino and J. Kock. Polynomial functors and polynomial monads. In Mathematical Proceedings of the Cambridge Philosophical Society, volume 154, pages 153–192. Cambridge University
Press, 2013. doi:10.1017/S0305004112000394.
[Göd58]
K. Gödel. Über eine bisher noch nicht benützte Erweiterung des finiten Standpunktes. Dialectica,
12:280–287, 1958. doi:10.1111/j.1746-8361.1958.tb01464.x.
[GS17]
N. Gambino and C. Sattler. The Frobenius condition, right properness, and uniform fibrations.
Journal of Pure and Applied Algebra, 221(12):3027–3068, 2017. doi:10.1016/j.jpaa.2017.02.
013.
P. Gabriel and M. Zisman. Calculus of fractions and homotopy theory, volume 35 of Ergebnisse
[GZ67]
der Mathematik und ihrer Grenzgebiete. Springer, 1967. doi:10.1007/978-3-642-85844-4.
M. Hofmann. Syntax and semantics of dependent types. In A.M. Pitts and P. Dybjer, editors,
[Hof97]
Semantics and logics of computation, volume 14 of Publ. Newton Inst., pages 79–130. Cambridge
University Press, Cambridge, 1997. doi:10.1007/978-1-4471-0963-1_2.
[Hub19]
S. Huber. Canonicity for cubical type theory. Journal of Automated Reasoning, 63:172–210, 2019.
doi:10.1007/s10817-018-9469-1.
[Joy17]
A. Joyal. Notes on clans and tribes, 2017.
[Kel80]
G.M. Kelly. A unified treatment of transfinite constructions for free algebras, free monoids, colimits,
associated sheaves, and so on. Bulletin of the Australian Mathematical Society, 22(1):1–83, 1980.
doi:10.1017/S0004972700006353.
[KL12]
K. Kapulkin and P. LeFanu Lumsdaine. The simplicial model of univalent foundations (after
Voevodsky). Journal of the European Mathematical Society, 23:2071–2126, 2012. doi:10.4171/
JEMS/1050.
[KV20]
K. Kapulkin and V. Voevodsky. A cubical approach to straightening. Journal of Topology,
13:1682–1700, 12 2020. doi:10.1112/topo.12173.
[LOPS18] D. R. Licata, I. Orton, A. M. Pitts, and B. Spitters. Internal universes in models of homotopy
type theory. In Hélène Kirchner, editor, 3rd International Conference on Formal Structures for
Computation and Deduction (FSCD 2018), volume 108 of Leibniz International Proceedings in
Informatics (LIPIcs), pages 22:1–22:17. Schloss Dagstuhl–Leibniz-Zentrum fuer Informatik, 2018.
doi:10.4230/LIPIcs.FSCD.2018.22.
P. LeFanu Lumsdaine and M. Shulman. Semantics of higher inductive types. Mathemati[LS20]
cal Proceedings of the Cambridge Philosophical Society, 169(1):159–208, 2020. doi:10.1017/
S030500411900015X.
[OP16]
I. Orton and A. M. Pitts. Axioms for modelling cubical type theory in a topos. In 25th EACSL
Annual Conference on Computer Science Logic (CSL 2016), volume 62 of Leibniz International
Proceedings in Informatics (LIPIcs), pages 24:1–24:19, Dagstuhl, Germany, 2016. Schloss Dagstuhl–
Leibniz-Zentrum für Informatik. doi:10.4230/LIPIcs.CSL.2016.24.
[PV07]
E. Palmgren and S. J. Vickers. Partial Horn logic and cartesian categories. Annals of Pure and
Applied Logic, 145(3):314–353, 2007. doi:10.1016/j.apal.2006.10.001.
[RS18]
E. Riehl and M. Shulman. A type theory for synthetic ∞-categories. Higher Structures, 1(1),
2018.
[Shu15]
M. Shulman. Univalence for inverse diagrams and homotopy canonicity. Mathematical Structures
in Computer Science, 25(5):1203–1277, 2015. doi:10.1017/S0960129514000565.
[Ste19]
J. Sterling. Algebraic type theory and universe hierarchies. arXiv preprint arXiv:1902.08848,
2019.
[Str91]
T. Streicher. Semantics of type theory: correctness, completeness, and independence results.
Progress in Theoretical Computer Science. Birkhäuser Basel, 1991. doi:10.2307/2275776.
[Swa16]
A. Swan. An algebraic weak factorisation system on 01-substitution sets: A constructive proof.
Journal of Logic & Analysis, 8(1):1–35, 2016. doi:10.4115/jla.2016.8.1.
[Swa17]
A. Swan. Semantics of higher inductive types, 2017. On the HoTT mailing list.
[Tai67]
W. W. Tait. Intensional interpretations of functionals of finite type I. Journal of Symbolic Logic,
32(2):198–212, 1967. doi:10.2307/2271658.
[GH03]

## PDF page 28

28:28

T. Coquand, S. Huber, and C. Sattler

[Uni13]
[Voe14]

Vol. 18:1

The Univalent Foundations Program. Homotopy Type Theory: Univalent Foundations of Mathematics. http://homotopytypetheory.org/book, Institute for Advanced Study, 2013.
V. Voevodsky. The equivalence axiom and univalent models of type theory. (Talk at CMU on
February 4, 2010). Preprint arXiv:1402.5556 [math.LO], 2014. URL: https://arxiv.org/pdf/
1402.5556.pdf.

Appendix A. Rules of the term model
We denote the objects of our base category C by X, Y, Z and its morphisms by f, g, h. In
the term model T morphisms f : Y → X act on judgments at stage X via an implicit
substitution, while for substitutions on object variables we will use explicit substitutions.
For this to make sense we first define the raw expressions as a presheaf: at stage X this is
given by
Γ, ∆ ::= ε | Γ.A
A, B, t, u, v ::= q | tσ | Un | Π(A, B) | lam(u) | app(u, v)
| Σ(A, B) | pair(u, v) | fst(u) | snd(u)
| Path(Ā, u, v) | ⟨⟩ū | ap(u, r)
| Gluec (A, ϕ, B̄, ū) | glue(v, ū) | unglue(u)
| fill(Ā, ϕ, b, ū, r) | . . .
Ā, B̄, ū, v̄ ::= (Af,r )f,r | (Af )f ∈[ϕ]
σ, τ, δ ::= p | id | στ | (σ, u) | ()
where b ∈ {0, 1}, ϕ ∈ F(X), and we skipped the constants for natural numbers. Above,
we have families of expressions, say Ā = (Af,r )f,r , whose index set ranges over certain Y ,
f : Y → X, and r ∈ I(Y ), and Af,r is a raw expression at stage Y ; likewise (Af )f ∈[ϕ](X)
consists of raw expressions Af at stage Y for f : Y → X in the sieve [ϕ] on X. (The exact
index sets will be clear from the typing rules below.) All other occurrences of r above
have r ∈ I(X). The restrictions along f : Y → X on the raw syntax then leave all the
usual cwf structure untouched, so we have qf = q and (Π(A, B))f = Π(Af, Bf ), and uses
the restrictions in I and F accordingly, e.g., (ap(u, r))f = ap(uf, rf ), and we will re-index
families according to Āf = (Agf,rf ) for Ā = (Ag,r )g,r .
To get the initial cubical cwf we in fact need more annotations to the syntax in order
to be able to define a partial interpretation (cf. [Str91, Hof97]) on the raw syntax. But to
enhance readability we suppress these annotations.
We will now describe a type system indexed by stages X. The forms of judgment are:
Γ ⊢X

Γ ⊢X A

Γ ⊢X A = B

Γ ⊢X t : A

Γ ⊢X t = u : A

σ : ∆ →X Γ

where the involved expressions are at stage X.
Remark A.1. In cubical type theory as described in [CCHM18] we did not index judgments
by objects X but allowed extending context by interval variables instead. Loosely speaking, a
judgment Γ ⊢{i1 ,...,in } J corresponds to i1 : I, . . . , in : I, Γ ⊢ J given the setting of [CCHM18].
As mentioned above we have the rule:
Γ ⊢X J
f: Y →X
Γf ⊢Y J f
At each stage we have all the usual rules valid in a cwf with Π-types, Σ-types, universes,
and natural numbers. We will present some of the rules, but skip all congruence rules.

## PDF page 29

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

ε ⊢X

Γ ⊢X
Γ ⊢X A
Γ.A ⊢X

Γ ⊢X A
Γ.A ⊢X q : Ap

Γ ⊢X A
σ : ∆ →X Γ
∆ ⊢X Aσ

Γ ⊢X t : A
Γ ⊢X A = B
Γ ⊢X t : B

Γ ⊢X A
p : Γ.A →X Γ

28:29

Γ ⊢X t : A
σ : ∆ →X Γ
∆ ⊢X tσ : Aσ
Γ ⊢X
id : Γ →X Γ

Γ ⊢X
() : Γ → ε

σ : ∆ →X Γ
τ : Θ →X ∆
στ : Θ →X Γ

σ : ∆ →X Γ
Γ ⊢X A
∆ ⊢X u : Aσ
(σ, u) : ∆ →X Γ.A
Γ.A ⊢X B
Γ ⊢X Π(A, B)

Γ.A ⊢X B
Γ.A ⊢X b : B
Γ ⊢X lam(b) : Π(A, B)

Γ ⊢X w : Π(A, B)
Γ ⊢X u : A
Γ ⊢X app(w, u) : B[u]

where we write [u] for (id, u) and σ + for (σp, q). The judgmental equalities (skipping suitable
premises, types, and contexts) are:
id σ = σ id = σ
q(σ, u) = u

(στ )δ = σ(τ δ)

(p, q) = id

(Π(A, B))σ = Π(Aσ, Bσ + )

A id = A

()σ = ()

(σ, u)δ = (σδ, uδ)

(Aσ)δ = A(σδ)

(lam(b))σ = lam(bσ + )

app(lam(b), u) = b[u]

u id = u

p(σ, u) = σ
(uσ)δ = u(σδ)

app(w, u)δ = app(wδ, uδ)

w = lam(app(wp, q))

We skip the rules for Σ-types and natural numbers as they are standard, but simply indexed
with an object X as we did for Π-types. The rules for universes are:
Γ ⊢X
Γ ⊢X Un

Γ ⊢X
Γ ⊢X Un : Un+1

Γ ⊢X A : Un
Γ ⊢X A : Un+1

Γ ⊢X A : Un
Γ ⊢X A

and we skip the rules for equality and closure under the type formers Π,Σ, natural numbers,
Path, and Gluec .
To state the rules for dependent path-types we introduce the following abbreviations.
We write Γ.I ⊢X Ā if Ā = (Af,r ) is a family indexed by Y , f : Y → X, and r ∈ I(Y ) such
that
Γf ⊢Y Af,r and Γf g ⊢Z (Af,r )g = Af g,r .
Given Γ.I ⊢X Ā we write Γ.I ⊢X ū : Ā whenever ū = (uf,r ) is a family indexed by Y ,
f : Y → X, and r ∈ I(Y ) such that
Γf ⊢Y uf,r : Af,r and Γf g ⊢Z (uf,r )g = uf g,rg : Af g,rg .

## PDF page 30

28:30

Vol. 18:1

T. Coquand, S. Huber, and C. Sattler

The rules for the dependent path type are:
Γ.I ⊢X Ā

Γ ⊢X u : AidX ,0
Γ ⊢X u : AidX ,1
Γ ⊢X Path(Ā, u, v)

Γ.I ⊢X Ā
Γ.I ⊢X ū : Ā
Γ ⊢X lam(ū) : Path(Ā, uidX ,0 , uidX ,1 )

Γ ⊢X t : Path(Ā, u, v)
r ∈ I(X)
Γ ⊢X ap(t, r) : AidX ,r
ap(lam(ū), r) = uid,r

t = lam(ap(tf, r)f,r )

(lam(ū))σ = lam((uf,r σf )f,r )

Path(Ā, u, v)σ = Path((Af,r σf )f,r , uσ, vσ)
(ap(t, r))σ = ap(tσ, r)

Note that in general these rules might have infinitely many premises. We get the nondependent path type for Γ ⊢X A by using the family Af,r := Af .
Given Γ.I ⊢X Ā and b ∈ {0, 1} we write Γ.I ⊢ϕ,b
X ū : Ā for ū = (uf,r ) a family indexed
over all Y , f : Y → X, and r ∈ I(Y ) such that either f is in the sieve [ϕ] or r = b and we
have
Γf ⊢Y uf,r : Af,r and Γf g ⊢Z (uf,r )g = uf g,rg : Af g,rg
for all g : Z → Y . The rule for the filling operation is given by:
Γ.I ⊢X Ā

ϕ ∈ F(X)
b ∈ {0, 1}
Γ.I ⊢ϕ,b
X ū : Ā
Γ ⊢Y fill(Ā, ϕ, b, ū, r) : Aid,r

r ∈ I(X)

with judgmental equality
fill(Ā, ϕ, b, ū, r) = uid,r whenever [ϕ] is the maximal sieve or r = b.
For the glueing operation we only present the formation rule; the other rules are similar
as in [CCHM18] but adapted to our setting. We write Γ ⊢ϕ
X B̄ if B̄ is a family of Bf for
f : Y → X in [ϕ] with Γf ⊢Y Bf which is compatible, i.e. Γf g ⊢Z Bf g = Bf g . In this case,
we write likewise Γ ⊢X ū : B̄ if ū is a compatible family of terms Γf ⊢Y uf : Bf .
Γ ⊢X A

ϕ ∈ F(X)
Γ ⊢ϕ
Γ ⊢ϕ
X B̄
X ū : isEquivc (B̄, A)
Γ ⊢X Gluec (A, ϕ, B̄, ū)

and the judgmental equality Gluec (A, ϕ, B̄, ū) = Bid in case [ϕ] is the maximal sieve, and
an equation for substitution.
This formal system gives rise to a cubical cwf T as follows. First, define judgmental
equality for contexts and substitutions as usual (we could also have those as primitive
judgments). Next, we define presheaves Con and Hom on C by taking, say, Con(X) equivalence
classes [Γ]∼ of Γ with Γ ⊢X modulo judgmental equality; restrictions are induced by the
(implicit) substitution: [Γ]∼ f = [Γf ]∼ . Types Type(X, [Γ]∼ ) are equivalence classes of A
with Γ ⊢X A modulo judgmental equality, and elements are defined similarly as equivalence
classes.
For type formers in T let us look at path types: we have to give an element of Type(Γ) in
a context (w.r.t. the internal language) Γ : Con, A : I → Type(Γ), u : Elem(Γ, A 0), v :
Elem(Γ, A 1). Unfolding the use of internal language, given [Γ]∼ ∈ Con(X), a compatible family [Af,r ]∼ ∈ Type(Y, [Γ]∼ f ) (for f : Y → X and r ∈ I(Y )) and elements
[u]∼ ∈ Elem([Γ]∼ , [Aid,0 ]∼ ) and [v]∼ ∈ ([Γ]∼ , [Aid,1 ]∼ ), we have to give an element of
Type(X, [Γ]∼ ), which we do by the formation rule for Path.

## PDF page 31

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:31

The remainder of the cubical cwf structure for T is defined in a similar manner, in
fact the rules are designed to reflect the laws of cubical cwfs. We conjecture that we can
follow a similar argument as in [Str91] to show that T is the initial cubical cwf. Given a
cubical cwf M over C, I, F we first have to define partial interpretations of the raw syntax
and then show that each derivable judgment has a defined interpretation in M, and for
equality judgments both sides of the equation have a defined interpretation in M and are
equal. In an intuitionistic framework, this partial interpretation should be described as an
inductively defined relation, which is shown to be functional. The partial interpretation J−K
assigns meanings to raw judgments with the following signature:
JΓ ⊢X K
Jσ : ∆ → ΓK
JΓ ⊢X AK
JΓ ⊢X u : AK

∈
∈
∈
∈

ConM (X)
HomM (X, J∆ ⊢X K, JΓ ⊢X K)
TypeM (X, JΓ ⊢X K)
ElemM (X, JΓ ⊢X K, JΓ ⊢X AK)

where among the conditions for the interpretation on the left-hand side to be defined is that
all references to the interpretation on the right-hand side are defined. This proceeds by
structural induction on the raw syntax and for JΓ ⊢X J K to be defined we assume all the
ingredients needed are already defined. E.g. for the path type JΓ ⊢X Path(Ā, u, v)K we in
particular have to assume that the assignment f, r ↦→ JΓf ⊢Y Af,r K is defined and gives rise
to a suitable input of PathM .
Appendix B. Indexed inductive sets in presheaves over C
We work in the setting of Subsection 2.2 given by presheaves over C.
Given a set I, a family A over I, a family B over i : I, an element a : A i, and a map
∏ ∏
s : i:I a:A i B i a → I,
the indexed inductive set WI,A,B,s is the initial algebra of the polynomial endofunctor [GK13]
on the (internal) category of families over I sending a family X to the family
∑
∏
JI, A, B, sK i = a:A i b:B i a X(s i a b).

Its constructive justification as an operation in the internal language of the presheaf topos
using inductive constructions of the metatheory is folklore (in a classical setting, one can
use transfinite colimits [Kel80]).12 If I, A, B are small with respect to a universe Ui with
i ∈ {0, 1, . . . , ω}, then WI,A,B,s : I → Ui .
∑
Let I, A, B now be small with respect to Uω . Given Fill(I, A) and Fill( i:I A i, λ(i,a) B i a),
we may use induction (i.e. the universal property of WI,A,B,s ) to derive an element of
Fill(I, WI,A,B,s ). As in Subsection 2.2 for dependent products, this implies (using external
reasoning) the internal statement C(WI,A,B,s i) for i : I given C(A i) for all i and C(B i a)
for all i, a. We then call WI,A,B,s a fibrant uniformly indexed inductive set. The qualifier
12An indexed inductive set in presheaves unfolds externally to an indexed inductive-recursive definition
where one defines the values at every level simultaneously with the restriction operations between levels. In
turn, this indexed inductive-recursive definition can be encoded as an indexed inductive-inductive definition,
which in turn reduces to an indexed inductive definition (which one may further reduce to an inductive
definition [GH03]). Both steps use the idea of encoding functions via their graphs. Alternatively, one can
directly transform the inductive-recursive definition to an indexed inductive definition by first omitting about
the naturality condition that mentions restriction, then define restriction recursively, and finally carve out
the elements that recursively satisfy the naturality condition.

## PDF page 32

28:32

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

uniformly indexed indicates that A is a fibrant family over I rather than a fibrant set with a
“target” map to I that indicates the target sort of the constructor sup.
Given A : Uω with Fill(1, A), we may use the technique of Andew Swan [Swa16, OP16] to
construct a (level preserving) identity set IdA a0 a1 for a0 , a1 : A (different from the equality
set a0 = a1 ) with Fill(A × A, λ(a0 ,a1 ) IdA a0 a1 )) and constructor
refla : IdA a a for a : A that
∏
has ∑
the usual elimination with respect to families P : a0 a1 :A IdA a0 a1 → Uω that satisfy
Fill( a0 a1 :A IdA a0 a1 , P ). Using external reasoning as before, one has C(IdA a0 a1 ) given
C(A), justifying calling IdA a0 a1 a fibrant identity set; using (2.2) one has elimination with
respect to families P of the previous signature with C(C a0 a1 p) for all a0 , a1 , p.
Using a folklore technique, we may use fibrant identity sets to derive fibrant indexed
inductive sets from fibrant uniformly indexed inductive sets, by which we mean the following.
fib
fib
Given
→ Uωfib with maps t : A → I and
∏ (I, fibI ) : Uω , (A, fibA ) : Uω , ⟨B, fibB ⟩ : A fib
s : a:A B a → I, we have ⟨WI,A,B,s,t , fibW ⟩ : I → Uω (we omit the subscripts to W for
readability), W living in Ui if I, A, B do, with
∏ ∏
sup : a:A f : ∏
W (t a).
b:B a W (s a b)
∏
Given ⟨P, fibP ⟩ : i:I W → Uωfib with
∏ ∏
∏
h : a:A f : ∏
(
b:B a P (s a b) (f b)) → P (t a) (sup a f ),
b:B a W (s a b)
∏ ∏
we have v : i:I w:W i P i w such that
v (t a) (sup a f ) = h a f (λb v (s a b) (f b).
Fibrant indexed inductive sets are used for the interpretation in the sconing model of
natural numbers in Section 3, higher inductive types in Subsection 5.2, and identity types in
Subsection 5.1. In practise, we will usually not bother to bring the fibrant indexed inductive
set needed into the above form and instead work explicitly with the more usual specification
in terms of a list of constructors, each taking a certain number non-recursive and recursive
arguments.13
As an example, we construct the fibrant indexed inductive set N′ needed in Section 3.
There, we have a fibrant set |N| : U0 (satisfying C(|N|)) with an element 0 : |N| and an
endofunction S : |N| → |N|. We wish
the fibrant indexed inductive set N′ : |N| → U0
∏ to define
′
′
′
′
with constructors 0 : N 0 and S : n:|N| ρ N n → N′ (S n). We let N′ be the uniformly indexed
inductive set over m : |N| with constructors
0′′ : Id|N| m 0 → N′ m,
∏
S′′ : n:|N| Id|N| m (S n) → N′ n → N′ m.
and define 0′ = 0′′ refl0 and S′ n n′ = S′′ n reflS(n) n′ . Fibrancy of Id ensures fibrancy of N′
(i.e. C(N′ n) for n : |N|). For elimination, we are given a fibrant family P n n′ for n : |N| and
n′ : N′ n with z ′ : P 0 0′ and s′ n n′ x : P (S n) (S′ n n′ ) for all n, n′ and x : P n n′ . We have to
define h′ n n′ : P n n′ for all n, n′ such that h′ 0 0′ = z ′ and h′ (S n) (S′ n n′ ) = s′ n n′ (h′ n n′ ).
We define h′ by induction on the uniformly indexed inductive set N′ and fibrant identity sets
13Note that the latter is really an instance of the former since our dependent sums, dependent products,
and finite coproducts are extensional (satisfy universal properties). Conversely, the former is an instance of
the latter with a single constructor taking a non-recursive and a recursive argument.

## PDF page 33

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:33

(using fibrancy of P ) via defining equations
h′ 0′′ refl0 = z,
h′ (Sn) (S′′ n reflS n n′ ) = s′ n n′ (h′ n n′ ).

Appendix C. Variations
C.1. Univalence as an axiom. Our treatment extends to the case where the glue types
in a cubical cwf as in Subsection 1.3 are replaced by an operation Elem(Γ, iUnivalencen )
for Γ : Con and n ≥ 0, with iUnivalencen defined in Remark 1.1.
To define this operation in the sconing model of Section 3, one first shows analogously
to Lemmas 3.1 and 3.2 that |−| preserves contractible types and that (A, A′ ) : Type∗ (Γ, Γ′ )
is contractible exactly if A is contractible and A′ ρ ρ′ a for ρ : |Γ| and ρ′ : Γ′ ρ where a : |A|
is the induced center of contraction. We have analogous statements for types of homotopy
level n ≥ 0i in M, in which case we instead have to quantify over all a : |A|.
Given (A, A′ ) : Type∗n (Γ, Γ′ ), we have show that the type
(S, S ′ ) = Σ∗ (Un , Equiv∗ (q, A))
over (Γ, Γ′ ) is contractible in M∗ . Without loss of generality, we may assume the center of
contraction of univalence in M is given by the identity equivalence. Using the observations
of the preceding paragraph, it suffices to show that
V ′ = S ′ ρ ρ′ (pair(Aρ, (lam(q), w)))
is contractible for ρ : |Γ| and ρ′ : Γ′ ρ where w denotes the canonical witness that the identity
map lam(q) on Aρ is an equivalence in M. Inhabitation is evident, and so it remains to
show propositionality. By the case of the preceding paragraph for propositions, the second
component of V ′ is a proposition, and thus we can ignore it for the current goal, which then
becomes
(∑
)
∏
′
′
′
isProp
T ′ :|A|→Un
a:|A| Equiv(T a, A ρ ρ a)
and follows from univalence in the standard model, justified by glueing.

Appendix D. Simplicial set model
Choosing for C the simplex category ∆, for I the usual interval ∆1 in simplicial sets, and
for F a small copy Ω0,dec of the sublattice of Ω0 of decidable sieves, we obtain a notion of
cubical cwf with a simplicial notion of shape.
Assume now the law of excluded middle. The above choice of C, I, F satisfies all of the
assumptions of Subsection 2.2 but one: the existence of a right adjoint to exponentiation
with I. However, except for Section 6, the only place our development makes use of this
assumption is in establishing (2.1). We will instead give a different definition of C that
still satisfies (2.1). Then the rest of our development, except for Section 6, still applies to
simplicial sets.

## PDF page 34

28:34

T. Coquand, S. Huber, and C. Sattler

Vol. 18:1

A Kan fibration structure on a family Y : X → Uω in simplicial sets consists of a choice
of diagonal fillers in all commuting squares of the form
∑
/
Λm
x:X Y x
k
9



∆m


/X

with left map a horn inclusion and right map the evident projection. Note that the
codomains of horn inclusions are representable. It follows that the presheaf of Kan fibration
structures indexed over the slice of simplicial sets over Uω is representable. Given [n] ∈ ∆
and A ∈ (Uω )n (i.e. an ω-small presheaf on ∆/[n]), we define C([n], A) as the set of Kan
fibration structures on A : ∆n → Uω . This defines a level preserving map C : Uω → Uω . Then
the representing
object of the above presheaf is given by the first projection Uωfib → Uω where
∑
fib
Uω = X:Uω C(X) is defined as before.
Let us now verify (2.1). Given a simplicial set X with Y : ∑
X → Uω , a global element of
Fill(X, Y ) corresponds to a uniform Kan fibration structure on x:X (Y x) → X in the sense
of [GS17]. A uniform Kan fibration structure induces a Kan fibration structure naturally in
X, giving the forward direction of (2.1). For the reverse direction, it suffices to give a uniform
Kan fibration structure in the generic case, i.e. a global element of Fill(Uωfib , λ(A,c) A). This
is [GS17, Theorem 8.9, part (ii)] together with the fact proved in [GZ67, Chapter IV] that
Kan fibrations lift against pushout products of interval endpoint inclusions with (levelwise
decidable) monomorphisms.14
Having verified (2.1), the rest of our development applies just as well to the case of
simplicial sets. In particular, we obtain in the standard model S of Subsection 2.3 a
version of the simplicial set model [KL12] of univalent type theory (using Subsection 5.1 for
identity types).15 As per Subsection 5.2, we furthermore obtain higher inductive types in
the simplicial set model in a way that avoids (as suggested by Andrew Swan [Swa17]) the
pitfall of fibrant replacement failing to preserve size encountered in [LS20].
Seeing simplicial sets as a full subtopos of distributive lattice cubical sets as observed
in [KV20], there is a functor from cubical cwfs with (C, I, F) = (∆, ∆1 , Ω0,dec ) to cubical
cwfs where C is the Lawvere theory of distributive lattices, I is represented by the generic
object, and F is the (small) sublattice of Ω0 generated by distributive lattice equations. The
cubical cwfs in the image of this functor satisfy a sheaf condition, which can be represented
syntactically as an operation allowing one to e.g. uniquely glue together to a type Γ ⊢{i,j} A
coherent families of types Γf ⊢X Af for f a map to X from the free distributive lattice on
symbols {i, j} such that f i ≤ f j or f j ≤ f i (compare also the tope logic of [RS18]).
Applying this functor to the simplicial set model S discussed above, we obtain an
interpretation of distributive lattice cubical type theory (with I and F as above) in the
sense of the current article (crucially, without computation rules for filling at type formers)
in simplicial sets. Thus, this cubical type theory is homotopically sound: can only derive
statements which hold for standard homotopy types.
14This is the only place where excluded middle is used, to produce a cellular decomposition in terms of
simplex boundary inclusions of such a monomorphism.
15Instead of Kan fibration structures, we can also work with the property of being a Kan fibration. Then
C is valued in propositions and we would obtain in S a version of the simplicial set model in which being a
type is truly just a property. However, choice would be needed to obtain (2.1).

## PDF page 35

Vol. 18:1

CANONICITY AND HOMOTOPY CANONICITY FOR CUBICAL TYPE THEORY

28:35

This work is licensed under the Creative Commons Attribution License. To view a copy of this
license, visit https://creativecommons.org/licenses/by/4.0/ or send a letter to Creative
Commons, 171 Second St, Suite 300, San Francisco, CA 94105, USA, or Eisenacher Strasse 2,
10777 Berlin, Germany
