Source: https://doi.org/10.4230/LIPIcs.FSCD.2023.5
PDF sha256: 7f832200f25c0a2297406772a2ed7caa876c6960fe3c7d7ac1b32206ef02d66e
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of uemura_2023_homotopy_type_theory_as_internal_languages_of_diagrams_of_infinity_logoses.pdf

Transcription of `uemura_2023_homotopy_type_theory_as_internal_languages_of_diagrams_of_infinity_logoses.pdf` in this directory, 19 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-19 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Homotopy Type Theory as Internal Languages of
Diagrams of ∞-Logoses
Taichi Uemura #
Stockholm University, Sweden

Abstract
We show that certain diagrams of ∞-logoses are reconstructed in internal languages of their oplax
limits via lex, accessible modalities, which enables us to use plain homotopy type theory to reason
about not only a single ∞-logos but also a diagram of ∞-logoses. This also provides a higher
dimensional version of Sterling’s synthetic Tait computability – a type theory for higher dimensional
logical relations.
2012 ACM Subject Classification Theory of computation → Type theory; Theory of computation
→ Denotational semantics; Theory of computation → Categorical semantics
Keywords and phrases Homotopy type theory, ∞-logos, ∞-topos, oplax limit, Artin gluing, modality,
synthetic Tait computability, logical relation
Digital Object Identifier 10.4230/LIPIcs.FSCD.2023.5
Related Version Full Version: https://arxiv.org/abs/2212.02444 [33]
Funding Taichi Uemura: Supported by KAW Grant “Type Theory for Mathematics and Computer
Science” investigated by Thierry Coquand and Peter LeFanu Lumsdaine.
Acknowledgements The author thanks Jonathan Sterling for useful conversations on the current
work. The author also thanks anonymous referees for corrections, comments, and suggestions.

1

Introduction

Homotopy type theory [31] is a type theory where one can do homotopy theory. It extends
Martin-Löf’s type theory [19] by the univalence axiom and higher inductive types. The former
forces types to behave like spaces rather than sets, and the latter allow us to build types
representing spaces such as spheres and tori.
An ∞-logos, also known as an ∞-topos [16, 2]1 , is another place to do homotopy theory,
among other aspects of it. An ∞-logos is an (∞, 1)-category that looks like the (∞, 1)category of spaces just as an ordinary logos is a category that looks like the category of
sets.
Homotopy type theory and ∞-logoses are closely related. Shulman [26] has shown that
any ∞-logos is presented by a structure that admits an interpretation of homotopy type
theory. In other words, homotopy type theory is an internal language of an ∞-logos. Any
theorem proved in homotopy type theory can be translated in an arbitrary ∞-logos. For
example, the proof of the Blakers-Massey connectivity theorem in homotopy type theory [10]
has led to a new generalized Blakers-Massey theorem that holds in an arbitrary ∞-logos [1].
An ∞-logos, however, does not live alone. ∞-logoses are often connected by functors
which are also connected by natural transformations. Plain homotopy type theory is, at
first sight, not sufficient to reason about a diagram of ∞-logoses, because the actions of

1

The term ∞-logos is Anel and Joyal’s terminology [2] for ∞-topos considered as an algebraic structure
rather than a geometric object. A morphism of ∞-logoses is always considered in the direction of the
inverse image functor. We use this terminology to clarify the direction of morphisms when speaking
about (co)limits of ∞-logoses.

© Taichi Uemura;
licensed under Creative Commons License CC-BY 4.0
8th International Conference on Formal Structures for Computation and Deduction (FSCD 2023).
Editors: Marco Gaboardi and Femke van Raamsdonk; Article No. 5; pp. 5:1–5:19
Leibniz International Proceedings in Informatics
Schloss Dagstuhl – Leibniz-Zentrum für Informatik, Dagstuhl Publishing, Germany

## PDF page 2

5:2

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

the functors and natural transformations are not internalized to type theory. Even worse,
it is impossible to naively internalize some diagrams: some internal adjunction leads a
contradiction [14]; there are only trivial internal idempotent comonads [25].
While there is no chance of naive internalization of such interesting but problematic
diagrams to plain homotopy type theory, some other diagrams can be internalized in a clever
way pointed out by Shulman2 . A minimal non-trivial example is a diagram consisting of two
∞-logoses and a lex, accessible functor between them in one direction. The two ∞-logoses
are lex, accessible localizations of another ∞-logos obtained by the Artin gluing for the
functor, and the functor is reconstructed by composing the inclusion from one localization
and the reflector to the other. Moreover, this reconstruction is internal to the glued ∞-logos,
because lex, accessible localizations of an ∞-logos correspond to lex, accessible modalities
in its internal language. Hence, plain homotopy type theory as an internal language of the
glued ∞-logos is sufficient to reason about the original diagram.
In this paper, we propose a class of shapes of diagrams of ∞-logoses for which the internal
reconstruction technique explained in the previous paragraph works. We call shapes in the
proposed class mode sketches. Our main result is summarized as follows. Let M be a mode
sketch. M is regarded as a presentation of an (∞, 2)-category. Then:
1. We associate to M certain axioms in type theory, one of which is to postulate some lex,
accessible modalities from which one can construct a diagram of ∞-logoses internally to
type theory (Sections 3.1 and 3.2).
2. For any diagram L indexed over M consisting of ∞-logoses and lex, accessible functors,
the oplax limit of L is an ∞-logos that satisfies the axioms associated to M, and the
diagram obtained in the internal language of the oplax limit corresponds to the original
diagram L. Conversely, any ∞-logos that satisfies the axioms associated to M is obtained
by this oplax limit construction (Theorem 48).
Recall that the oplax limit of a diagram of (∞, 1)-categories is a generalization of the Artin
gluing [35, 24].

1.1

Synthetic Tait computability

This work is closely related to Sterling’s synthetic Tait computability [29, 27]. It is a technique
of constructing logical relations using an internal language for the Artin gluing. A logos
obtained by the Artin gluing is always equipped with a distinguished proposition in its
internal language. The two lex, accessible modalities associated to the glued logos are the
open and closed modalities associated to the proposition. The fracture and gluing theorem
asserts that every type in the internal language is canonically fractured into an open type and
a closed (unary, proof-relevant) relation on it which are glued back together. The internal
language for the Artin gluing is thus a type theory with an indeterminate proposition in which
types are relations and provides a synthetic method of constructing logical relations used in
the study of type theories and programming languages. Applications include normalization
for complex type theories [28, 8].
We relate synthetic Tait computability and mode sketches. The core axiom for synthetic
Tait computability is to postulate some indeterminate propositions. Note that, although
the original synthetic Tait computability is based on extensional type theory, postulating
propositions makes sense also in homotopy type theory. We show that part of the axioms
associated to a mode sketch is equivalent to postulating a lattice of propositions (Theorem 37).

2

https://golem.ph.utexas.edu/category/2011/11/internalizing_the_external_or.html

## PDF page 3

T. Uemura

5:3

Mode sketches thus provide an alternative synthetic method of constructing logical
relations. This is also natural from Shulman’s point of view [24] that interpretations of
type theory in oplax limits are generalized logical relations. Since we work in homotopy
type theory, what we get is actually higher-dimensional logical relations, and our primary
application of mode sketches in upcoming paper(s) [34] will be normalization for ∞-type
theories introduced by Nguyen and Uemura [20] as a higher-dimensional generalization of
type theories.

1.2

Contributions

Our main result is Theorem 48: for every mode sketch M, the models of the axioms associated
to M are precisely the oplax limits of diagrams of ∞-logoses indexed over M. This allows
us to reason about a diagram of ∞-logoses in plain homotopy type theory. We also relate
mode sketches to synthetic Tait computability (Theorem 37). Mode sketches provide a
higher-dimensional version of synthetic Tait computability.
A minor result is an improvement of the fracture and gluing theorem of Rijke, Shulman, and
Spitters [22, Theorem 3.50]. It gives a construction of a canonical join of two strongly disjoint
lex modalities. We show that this construction preserves accessibility as well (Proposition 14).

1.3

Organization

In Section 2, we review the theory of modalities in homotopy type theory [22]. Our focus is
on the poset of lex, accessible modalities and on the open and closed modalities associated
to propositions.
Sections 3 and 4 are the core of the paper. We introduce the notion of a mode sketch
(Definition 25). For every mode sketch, we introduce two equivalent sets of axioms to encode
a certain diagram of universes. One postulates some lex, accessible modalities while the other
postulates a lattice of propositions. The open and closed modalities give a construction of
the former from the latter which we show is an equivalence (Theorem 37). The latter is a
higher dimensional analogue of Sterling’s synthetic Tait computability [27].
In Section 5, we give a sketch of proof of our main result (Theorem 48): for any mode
sketch, the space of ∞-logoses satisfying the axioms associated to the mode sketch is equivalent
to the space of diagrams of ∞-logoses and lex, accessible functors indexed over the mode
sketch. For reasons of space, details are not presented in this version. See [33] for full details.

1.4

Preliminaries

We assume that the reader is familiar with homotopy type theory [31]. By homotopy type
theory we mean dependent type theory with (dependent) function types, (dependent) pair
types, a unit type, identity types, univalent universes U : ⇑ U : ⇑2 U : . . . , and all higher
inductive types we need. The universe ⇑n U is usually written as Un , but the latter conflicts
with the notation for the subuniverse of modal types. The notation ⇑n U also indicates that
large types are interpreted in universe enlargements of an ∞-logos; see Section 5. We mainly
follow the HoTT Book [31] for terminologies and notations in homotopy type theory.

1.5

Related work

An earlier version of cohesive homotopy type theory [23] uses modalities in plain homotopy type
theory to internalize a series of adjunctions that arises in Lawvere’s axiomatic cohesion [13].
However, because naive internalization of adjunctions do not work well [14, 25], the

FSCD 2023

## PDF page 4

5:4

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

axiomatization is tricky and not ideal to work with. The newer version of cohesive homotopy
type theory [25] instead extends homotopy type theory by another layer of context and
new modal operators. The resulting type theory works well for axiomatic cohesion but is
complicated compared to plain homotopy type theory. It is also too optimized for axiomatic
cohesion.
A more general framework for internal diagrams is multimodal dependent type theory [9]. It
is roughly a family of type theories related to each other via modal operators and interpreted
in a diagram of presheaf categories among a more general notion of model. The shape
of diagram is specified directly by an arbitrary 2-category which is called a mode theory
in this context. Our terminology “mode sketch” is chosen to mean a sketch of a mode
theory. Multimodal dependent type theory is potentially an internal language for diagrams
of ∞-logoses, but for this one would have to rectify not only ∞-logoses but also functors and
natural transformations between them.
Our work brings back the ideas of earlier cohesive homotopy type theory [23]. Although it
might not be the best type theory, it has a lot of advantages: modalities are internal to plain
homotopy type theory, and thus all results are ready to formalize in existing proof assistants;
keeping type theory simple is also important in informal use of type theory in which the
correctness of application of inference rules is not checked by computer; the semantics is
clear, since the ∞-logos semantics of homotopy type theory is well-established [4, 3, 24, 26];
it also opens the door to internalization of more general diagrams in a uniform way, which is
the motivation for the current work.

2

Modalities in homotopy type theory

We review the theory of modalities in homotopy type theory [22]. In this section, we work
in homotopy type theory. A modality is in short a reflective subuniverse closed under pair
types.
▶ Definition 1. A subuniverse m is a a function Inm : U → ⇑ U such that Inm (A) is a
proposition for all A : U. A type A satisfying Inm (A) is called m-modal. We define a subtype
Um ⊂ U to be {A : U | Inm (A)}.
▶ Definition 2. A subuniverse m is reflective if it is equipped with functions #m : U → Um
∏
and ηm : A:U A → #m A such that that the precomposition λf.f ◦ ηm (A) : (#m A → B) →
(A → B) is an equivalence for any B : Um . Note that such a pair (#m , ηm ) is unique.
▶ Definition 3. A reflective subuniverse m is a modality if Inm is closed under pair types,
∏
∑
that is, for A : U and B : A → U, if Inm (A) and a:A Inm (B(a)), then Inm ( a:A B(a)).
An important class of modalities is accessible modalities which are roughly modalities
“presented by small data”.
▶ Definition 4. For types A, B : U, we define
(A ⊥ B) ≡ IsEquiv(λ(b : B).λ(_ : A).b).
Note that λ(b : B).λ(_ : A).b is a function of type B → (A → B). For a subuniverse m, we
define subuniverses m⊥ and ⊥ m by
Inm⊥ (B) ≡

∏

In⊥ m (A) ≡

∏

A:Um A ⊥ B
B:Um A ⊥ B.

## PDF page 5

T. Uemura

5:5

▶ Definition 5. A null generator µ consists of Iµ : U and Zµ : Iµ → U. We write NullGen
for the type of null generators. Given a null generator µ, we define a subuniverse Null(µ)
∏
by InNull(µ) (A) ≡ i:Iµ Zµ (i) ⊥ A. It is shown that Null(µ) is a modality using a higher
inductive type [22, Theorem 2.19]. A modality m is accessible if it is in the image of Null,
∑
that is, ∥ µ:NullGen m = Null(µ)∥.
Another important class of modalities is lex modalities.
▶ Definition 6. For a modality m, a type A : U is m-connected if #m A is contractible. This
is equivalent to In⊥ m (A) by [22, Corollary 1.37].
▶ Definition 7. A modality m is lex if for any m-connected type A : U, the identity type
a1 = a2 is m-connected for any a1 , a2 : A.
Modalities that are both lex and accessible are of particular importance because they
correspond to subtoposes of an ∞-topos under the interpretation of types as sheaves on the
∞-topos. From now on, we are mostly interested lex, accessible modalities, so we give them
a short name.
▶ Terminology 8. LAM is an acronym for lex, accessible modality.
Fundamental examples of LAMs are open and closed modalities which correspond to
open and closed, respectively, subtoposes.
▶ Construction 9. Let P be a proposition. We define the open modality Op(P ) by #Op(P ) A ≡
(P → A) and ηOp(P ) (A, a) ≡ λ_.a. It is lex and accessible by [22, Example 2.24 and Example
3.10]. We also define the closed modality Cl(P ) by InCl(P ) (A) ≡ (P → IsContr(A)). It is lex
and accessible by [22, Example 2.25 and Example 3.14]. Note that Cl(P ) = ⊥ Op(P ) [22,
Example 1.31].

2.1

The poset of lex, accessible modalities

We have the posets
SU ⊃ RSU ⊃ Mdl ⊃ AccMdl ⊃ LAM
of subuniverses, reflective subuniverses, modalities, accessible modalities, and lex, accessible
modalities, respectively, where all the inclusions are full. We also have the full subposet
Lex ⊂ Mdl of lex modalities. By definition, LAM = Lex ∩ AccMdl. We study the poset LAM
in more detail.
▶ Definition 10 ([22, Theorem 3.25]). Let I : U and m : I → LAM. A canonical meet
⋀
⋁
meet of m(i)’s in SU. A canonical join i:I m(i) is a LAM
i:I m(i) is a LAM that is the⋁
satisfying that a type A : U is ( i:I m(i))-connected if and only if it is m(i)-connected for all
i : I. Note that a canonical join is the join in Mdl.
▶ Example 11. The top modality Top, for which all the types are modal, is the canonical
meet of the empty family. The bottom modality Bot, for which only the contractible types
are modal, is the canonical join of the empty family.
The canonical meet of an arbitrary family of LAMs exists [22, Theorem 3.29 and Remark
3.23]. Canonical joins are less understood than canonical meets. One important case when
canonical joins exist and can be computed is the following.

FSCD 2023

## PDF page 6

5:6

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

▶ Definition 12. Let m and n be LAMs. n is strongly disjoint from m if any m-modal type
is n-connected or equivalently if m ≤ ⊥ n in SU.
▶ Proposition 13 (Fracture and gluing theorem). Let m and n be LAMs such that m ≤ ⊥ n.
1. The canonical join m ∨ n exists.
2. A type A is (m ∨ n)-modal if and only if the function ηn (A) : A → #n A has m-modal
fibers.
∑
∑
3. Um∨n ≃ A:Um B:Un A → #m B.
In the special case when m = ⊥ n, we have m ∨ n = Top.
Proof. All but the accessibility of m ∨ n are proved by Rijke, Shulman, and Spitters [22,
Theorem 3.50]. We will prove the accessibility of m ∨ n in Proposition 14 using an open
modality.
◀

2.2

Accessibility of the canonical join

Let us fill the gap in the proof of Proposition 13. This subsection is devoted to proving the
following.
▶ Proposition 14. Let m and n be LAMs such that m ≤ ⊥ n. Then the canonical join m ∨ n
(in Lex) is accessible.
We have to find a null generator for m ∨ n. A natural guess is the following.
▶ Construction 15. Let µ and ν be null generators. We define a null generator µ ⋆ ν by
Iµ⋆ν ≡ Iµ × Iν and Zµ⋆ν (i, j) ≡ Zµ (i) ⋆ Zν (j) ≡ Zµ (i) +Zµ (i)×Zν (j) Zν (j).
▶ Lemma 16. Let m and n be LAMs, and let µ and ν be null generators for m and n,
respectively. Then Zµ⋆ν (i, j) is both m-connected and n-connected for all i : Iµ and j : Iν .
Proof. Recall that a function is m-connected if its fibers are m-connected and that the class
of m-connected functions is the left class of a (stable) orthogonal factorization system [22,
Theorem 1.34]. Then the claim follows by the pushout stability and the right cancellability
of connected functions.
◀
Lemma 16 shows m ∨ n ≤ Null(µ ⋆ ν) for arbitrary accessible modalities m and n and for
arbitrary choices of µ and ν. We know neither if the other direction holds in general for
some choices of µ and ν nor if Null(µ ⋆ ν) is independent of µ and ν. Note that Finster [7]
observed that Null(µ ⋆ ν) is lex whenever Null(µ) and Null(ν) are lex. In the special case
when m ≤ ⊥ n, the idea of the proof of m ∨ n = Null(µ ⋆ ν) is to show that n is an open
modality within the subuniverse of Null(µ ⋆ ν)-modal types.
▶ Lemma 17. Let m and n be LAMs such that m ≤ ⊥ n. Then n ≤ Op(#m 0).
Proof. This is because #m 0 is n-connected by assumption.

◀

▶ Lemma 18. Let m and n be LAMs such that m ≤ ⊥ n. Suppose that µ and ν are null
generators for m and n, respectively, and that µ admits a function f : #m 0 → Iµ such that
0 ≃ Zµ (f (i)) for all i : #m 0. Then #Op(#m 0) A is n-modal for any Null(µ ⋆ ν)-modal type
A. Consequently, the canonical function #Op(#m 0) A → #n A induced by Lemma 17 is an
equivalence for any Null(µ ⋆ ν)-modal type A.

## PDF page 7

T. Uemura

5:7

Proof. We show that #Op(#m 0) A ≡ (#m 0 → A) is n-modal. Since ν is a null generator for n,
it suffices to show that Zν (j) ⊥ (#m 0 → A) for all j : Iν . This is equivalent to that Zν (j) ⊥ A
under an assumption i : #m 0. This holds since Zν (j) ≃ 0 ⋆ Zν (j) ≃ Zµ (f (i)) ⋆ Zν (j) and
since A is Null(µ ⋆ ν)-modal.
◀
▶ Lemma 19. Let m and n be LAMs such that m ≤ ⊥ n. Suppose that µ and ν are null
generators for m and n, respectively, and that ν has an element j : Iν such that Zν (j) ≃ #m 0.
Then, if a type A is Null(µ ⋆ ν)-modal and Op(#m 0)-connected, then it is m-modal.
Proof. We show that Zµ (i) ⊥ A for all i : Iµ . By the definition of ⋆, we have the following
pullback square.
≃

(Zµ (i) ⋆ #m 0 → A)
⌟
(#m 0 → A)

≃

(Zµ (i) → A)

(Zµ (i) → #m 0 → A)

Since A is Op(#m 0)-connected, the domain and codomain of the bottom function are
contractible, and thus the bottom function is an equivalence. It then follows that the top
function is also an equivalence. Since A is Null(µ ⋆ ν)-modal and since Zν (j) ≃ #m 0, we
have A ≃ (Zµ (i) ⋆ #m 0 → A) ≃ (Zµ (i) → A), and thus Zµ (i) ⊥ A.
◀

Proof of Proposition 14. Let µ and ν be null generators for m and n, respectively. Note
that adjoining a family of connected types to a null generator does not change the modality
presented by the null generator. Under an assumption i : #m 0, the empty type 0 becomes
m-connected, and thus we may assume that µ includes the type family λ(_ : #m 0).0.
Since #m 0 is n-connected by assumption, we may assume that ν includes the type family
λ(_ : 1). #m 0.
We show that Null(µ ⋆ ν) = m ∨ n. By Lemma 16, m ∨ n ≤ Null(µ ⋆ ν). For the other
direction, suppose that A is a Null(µ ⋆ ν)-modal type. By [22, Theorem 3.50], it suffices to
show that ηn (A) : A → #n A has m-modal fibers. By Lemma 18, #n A ≃ #Op(#m 0) A. Then
the fibers of ηn (A) are Op(#m 0)-connected. Since both A and #n A are Null(µ ⋆ ν)-modal,
the fibers of ηn (A) are also Null(µ ⋆ ν)-modal. Thus, by Lemma 19, ηn (A) has m-modal
fibers.
◀
As a by-product, we have the following.
▶ Corollary 20. Let m and n be LAMs such that m ≤ ⊥ n. If m ∨ n = Top, then m and n are
the closed and open, respectively, modalities associated to the proposition #m 0.
◀

3

Mode sketches

We introduce mode sketches as shapes of diagrams of subuniverses definable internally to
type theory. We work in homotopy type theory through the section.

3.1

Internal diagrams induced by modalities

We consider postulating some LAMs to encode some diagram of subuniverses. The
fundamental observation is that a pair of LAMs induces a canonical functor between them.
▶ Construction 21. Let m and n be LAMs. We define a function #nm : Un → Um to be the
restriction of #m to Un ⊂ U.

FSCD 2023

## PDF page 8

5:8

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

▶ Remark 22. We can say that #nm is a functor externally: we can construct a function
∏
n
n
A,B:Un (A → B) → (#m A → #m B) and every instance of the coherence laws. However, it
is not known how to state that #nm is a functor internally to type theory, because defining
the type of (∞, 1)-categories in plain homotopy type theory is still an open problem.
n
We have two functors #m
n : Um → Un and #m : Un → Um for every pair of LAMs m and n,
but we are often interested in only one direction. It is thus useful to cut off one direction by
postulating that m ≤ ⊥ n: by the definition of connectedness, #m
n becomes constant at the
unit type. The other direction #nm : Un → Um remains non-trivial. Therefore, a pair (m, n) of
LAMs such that m ≤ ⊥ n encodes a functor Un → Um . When n ≤ ⊥ m is also assumed, Um
and Un are considered unrelated.

Given more than two LAMs, we have canonical natural transformations between the
canonical functors.
▶ Construction 23. Let m0 , m1 , m2 be LAMs. We define
m0 ;m2
ηm
:
1

∏

m2
m1 m2
A:Um2 #m0 A → #m0 #m1 A

m0 ;m2
by ηm
(A) ≡ #m0 ηm1 (A). This family of functions is natural in the sense that for any
1
A, B : Um2 and f : A → B, we have a homotopy filling the following square.

2
#m
m0 A

m ;m2
(A)

ηm10

m

m

#m20 f

2
#m
m0 B

m2
1
#m
m0 #m1 A

m

#m10 #m21 f

m ;m2

ηm10

(B)

m2
1
#m
m0 #m1 B

Let m0 , m1 , m2 , m3 be LAMs. By naturality, the following diagram commutes.
m ;m3

3
#m
m0

ηm10

m3
1
#m
m0 #m1

m ;m3

ηm20

m3
2
#m
m0 #m2

m

m ;m3

#m10 ηm21

m ;m2
m
#m32

ηm10

m2 m3
1
#m
m0 #m1 #m2

For more than four LAMs, higher coherence laws are also satisfied. Hence, a tuple (m0 , . . . , mn )
of LAMs such that mi ≤ ⊥ mj for all i < j encodes an n-simplex with vertices Umi , edges
m
#mji : Umj → Umi for i < j, triangles
m

#mk
i

Umi

Umk

m ;mk

ηmji
m

#mji

m

Umj

#mk
j

for i < j < k, and higher homotopies.

## PDF page 9

T. Uemura

5:9

mi ;mk
Shapes other than simplices are expressed by postulating invertibility of some of ηm
’s.
j
For example, let m0 , m1 , m2 , m3 be LAMs and suppose that mi ≤ ⊥ mj for all i < j, that
m0 ;m3
m2 ≤ ⊥ m1 , and that ηm
is invertible. We have a diagram
1

Um1
m

m

#m10

m ;m3

≃ ηm10

#m31

m

Um0

Um3

#m30
m ;m3

ηm20

m

#m20

m

#m32

Um2
which is equivalent to a diagram of the form
m

Um1

m

#m31

#m10

Um0

Um3 .
m

#m20

m

Um2

#m32

We cannot, however, naively postulate some properties of the functors #nm ’s such as
conservativity, fullness, faithfulness, adjointness, and invertibility. This is because the internal
statements of these conditions are too strong due to stability under substitution, and indeed
some “no-go” theorems on internalizing properties of functors are known [14, Theorem 5.1][25,
Theorem 4.1].
m

▶ Remark 24. It is possible to postulate arbitrary properties of #mji ’s in the following way.
We first postulate a “base” LAM Base and assume Base ≤ ⊥ mi for all i. The universe UBase
is intended to be interpreted as the (∞, 1)-category of spaces, so statements in UBase will
correspond to external statements. Since #Base : U → UBase preserves finite limits, it takes
(∞, 1)-categories to (∞, 1)-categories and functors to functors. We can then postulate any
property on the induced functor #Base Umj → #Base Umi . In fact, cohesive homotopy type
theory [23] was first formulated in a similar fashion where the ♯ modality plays the role of
Base. However, since we only know that #Base Umi is an (∞, 1)-category externally, this
approach is not so convenient to work with especially for formalization in proof assistants.
For this and some other reasons, the newer version of cohesive homotopy type theory [25]
is a proper extension of homotopy type theory. Nevertheless, this adding-base approach is
attractive since it keeps type theory simple and works for any kind of diagram.

3.2

Mode sketches

We introduce mode sketches as shapes of diagrams definable by the methodology explained
in Section 3.1.
▶ Definition 25. A mode sketch M consists of the following data:
a decidable finite poset IM ;
a subset TM of triangles in IM .

FSCD 2023

## PDF page 10

5:10

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

Here, by a decidable poset we mean a poset whose ordering relation ≤ is decidable. A type
is finite if it is merely equivalent to the coproduct of n copies of 1 for some n : N [21,
Definition 16.3.1]. The identity type on a finite type is decidable [21, Remark 16.3.2]. The
strict ordering relation i < j defined as (i ≤ j) ∧ (i ̸= j) is also decidable. By a triangle in
IM we mean an ordered triple (i0 < i1 < i2 ) of elements of IM . A triangle in TM is called
thin.
▶ Remark 26. The definition of mode sketches also makes sense in the metatheory. Every
mode sketch M in the metatheory can be encoded in type theory since it is finite.
Let M be a mode sketch and m : M → LAM a function. We consider the following
axioms.
▶ Axiom A. m(i) ≤ ⊥ m(j) for any j ̸≤ i in M.
m(i );m(i2 )

▶ Axiom B. For any triangle (i0 < i1 < i2 ) : TM , the natural transformation ηm(i10)
m(i )
m(i ) m(i )
#m(i20 ) ⇒ #m(i01 ) #m(i21 ) is invertible.

▶ Axiom C. The top modality is the canonical join

⋁

:

M m.

▶ Remark 27. Assuming Axiom A, if i < j, then m(i) ≤ ⊥ m(j).
Axioms A and B are motivated by the observation made in Section 3.1. That is, when
j ̸≤ i, the functor in the direction Um(i) → Um(j) is cut off. Our intended models constructed
in Section 5 additionally satisfy Axiom C. This axiom is not so important in practical use,
since our primary aim is to draw a diagram of ∞-logoses inside homotopy type theory, but
Axiom C does nothing for this purpose. It is even better to work without Axiom C, because
Axioms A and B are stable under restriction along a full inclusion M′ ⊂ M while Axiom C
is not. Axiom C is meant to exclude models other than intended models.
▶ Remark 28. A mode sketch M is regarded as a presentation of an (∞, 2)-category. The
strict ordering relation generates 1-cells (i < j) : i → j, and the triangles (i < j < k) generate
2-cells in the direction
j

i

k.

When the triangle is thin, the corresponding 2-cell is made invertible. Longer chains
(i0 < i1 < · · · < in ) present coherence. Formally, we regard M as a scaled simplicial set [17],
one of models for (∞, 2)-categories, by taking the nerve and marking thin triangles as thin
2-simplices, and then reverse 2-cells. A function m : M → LAM satisfying Axioms A–C is
then considered as a diagram of subuniverses indexed over Mop(1,2) , the (∞, 2)-category
obtained from M by reversing the directions of 1-cells and 2-cells.
▶ Example 29. Every decidable finite poset is a mode sketch where no triangle is thin. The
(∞, 2)-category presented by it is obtained from the left adjoint of the Duskin nerve [6] by
reversing 2-cells.
▶ Example 30. The mode sketch for functors is drawn as
0

1.

## PDF page 11

T. Uemura

5:11

Axiom A asserts m(0) ≤ ⊥ m(1). Axiom B is empty since there is no triangle. Thus, we get
the following diagram.
m(1)

Um(0)

#m(0)

Um(1)

Axiom C asserts m(0) ∨ m(1) = Top.
▶ Example 31. The mode sketch for triangles is drawn as
0

2
≃
1

where “≃” indicates that the triangle is thin. Axiom A asserts m(0) ≤ ⊥ m(1), m(0) ≤ ⊥ m(2),
m(0);m(2)
and m(1) ≤ ⊥ m(2). Axiom B asserts that ηm(1)
is invertible. Thus, we have the following
commutative triangle.
m(2)

#m(0)

Um(0)
m(1)

#m(0)

Um(2)
m(2)

Um(1)

#m(1)

Axiom C asserts m(0) ∨ m(1) ∨ m(2) = Top. Notice that theorems for the mode sketch for
functors proved without Axiom C also apply to the three edges in the above diagram. To
keep this reusability, we should not assume Axiom C in practical use.

3.3

Intended models, internally

Let M be a mode sketch. We can internally see what kind of an ∞-logos is a model of M.
Here, by a model of M we mean an ∞-logos that admits an interpretation of a postulated
function m : M → LAM satisfying Axioms A–C.
▶ Example 32. Consider the case when M is the mode sketch for functors (Example 30).
m(1)
Proposition 13 implies that U ≃ Um(0)∨m(1) is the Artin gluing for the functor #m(0) : Um(1) →
Um(0) . Therefore, our intended models of M are ∞-logoses obtained by the Artin gluing.
A generalization of the Artin gluing is oplax limits. In the setting of Example 32, U fits
m(1)

#m(0)

into the following universal oplax cone over the diagram Um(0) ←−−−− Um(1) .
U
(1)
Um(0)

m(1)

#m(0)

Um(1)

An oplax cone over a diagram is a kind of cone but every triangle formed by two projections
and a functor in the diagram is only filled by a not necessarily invertible natural transformation
in the direction of Diagram (1). The universal oplax cone or oplax limit is the terminal
object in the (∞, 1)-category of oplax cones.

FSCD 2023

## PDF page 12

5:12

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

▶ Example 33. Consider the case when M is the mode sketch {0 → 1 → 2} with no thin
triangle. Iterating Proposition 13, we see that every type A : U is fractured into A0 : Um(0) ,
m(1)

m(2)

m(2)

A1 : Um(1) , A2 : Um(2) , f01 : A0 → #m(0) A1 , f02 : A0 → #m(0) A2 , f12 : A1 → #m(1) A2 , and
m(1)

m(0);m(2)

p012 : #m(0) f12 ◦ f01 = ηm(1)

(A2 ) ◦ f02 . Indeed, we have

Um(0)∨m(1)∨m(2)
≃

≃

{Proposition 13 for m(0) and m(1) ∨ m(2)}
∑
∑
A0 :Um(0)
A12 :Um(1)∨m(2) A0 → #m0 A12
{Proposition 13 for m(1) and m(2)}
∑
∑
∑
∑
A0 :Um(0)

A1 :Um(1)

A2 :Um(2)

f12 :A1 →#m(1) A2 A0 → #m(0) (A1 ×#m(1) A2 A2 )

where the pullback is taken for f12 : A1 → #m(1) A2 and ηm(1) (A2 ) : A2 → #m(1) A2 . Since
#m(0) preserves pullbacks, the component A0 → #m(0) (A1 ×#m(1) A2 A2 ) corresponds to the
components f01 , f02 , and p012 . Then U is the oplax limit of the diagram
m(2)

#m(0)

Um(0)

Um(2) .

m(0);m(2)
ηm(1)

m(1)

#m(0)

(2)
m(2)

#m(1)

Um(1)

This means that we have projections Ai : U → Um(i) for all i, natural transformations
U
Aj

Ai
fij

Um(i)

m(j)

#m(i)

Um(j)

for all i < j, and a homotopy
U
A0

Um(0)

f01

A1

m(1)

#m(0)

U
A2
f12

A0

Um(2)
m(2)

Um(1)

#m(1)

p012

=

f02

A2

m(2)

Um(0)

Um(2) ,

#m(0)
m(1)

#m(0)

m(0);m(2)
ηm(1)

Um(1)

m(2)

#m(1)

and these data form a universal oplax cone over Diagram (2).
m(0);m(2)
Let us make the triangle (0 < 1 < 2) thin so that the natural transformation ηm(1)
becomes invertible. In this setting, U is still the oplax limit of Diagram (2), but the
presentation can be simplified since the type of data (f02 , p012 ) is contractible.
For a general mode sketch M, we apply Proposition 13 for a minimal element m(i0 )
⋁
and the rest i:M\i0 m(i) and repeat this for M \ i0 to fracture types into modal types.
Examples 32 and 33 suggest that U is the oplax limit of the diagram formed by Um(i) ’s
explained in Remark 28. Thus, our intended models of M are oplax limits of ∞-logoses
indexed over the (∞, 2)-category presented by M. The formal account of this is sketched in
Section 5 and fully described in the extended version [33].

## PDF page 13

T. Uemura

4

5:13

Mode sketches and synthetic Tait computability

We give an alternative set of axioms for mode sketches and exhibit a connection between
mode sketches and synthetic Tait computability of Sterling [27]. The core axiom of synthetic
Tait computability is to postulate a proposition. The proposition induces the open and
closed modalities, and then every type is fractured into an open type equipped with a closed
type family and behaves like a logical relation. In this story, the open and closed modalities
seem more essential than the postulated proposition, so we aim to formulate synthetic Tait
computability purely in terms of modalities. We work in homotopy type theory.

4.1

Alternative mode sketch axioms

The ∞-logoses obtained by the Artin gluing can be characterized as ∞-logoses equipped with
a subterminal object; see [11, A4.5.6] for the 1-categorical case. We generalize this from the
Artin gluing to oplax limits indexed by mode sketches, internally to type theory: the type of
functions M → LAM satisfying Axioms A and C is equivalent to the type of morphisms from
the lattice of cosieves on M to the lattice Prop (Theorem 37).
▶ Definition 34. A cosieve on a decidable poset I is an upward-closed decidable subset of it.
Let coSieve(I) denote the poset of cosieves on I ordered by inclusion. Note that cosieves are
closed under finite meets and joins, so coSieve(I) is a lattice.
▶ Notation 35. For i : M, let (i ↓ M) denote the cosieve {j : M | i ≤ j} and ∂(i ↓ M) the
cosieve (i ↓ M) \ {i}.
▶ Construction 36. Let P : coSieve(M) → Prop be a function. We define a function
aP : M → LAM by aP (i) ≡ Op(P (i ↓ M)) ∧ Cl(P (∂(i ↓ M))).
▶ Theorem 37. Construction 36 is restricted to an equivalence between the following types:
1. the type of lattice morphisms P : coSieve(M) → Prop;
2. the type of functions m : M → LAM satisfying Axioms A and C.
Before giving a proof of Theorem 37, let us relate Theorem 37 to synthetic Tait
computability [29, 27, 30]. The core axiom of synthetic Tait computability is to postulate
some propositions. One can work with those propositions directly but also with the induced
open and closed modalities. Theorem 37 says that synthetic Tait computability can, in fact,
be formulated completely in terms of modalities. The simplest version of synthetic Tait
computability postulates a single proposition. The corresponding mode sketch is {0 → 1} as
follows.
▶ Example 38. Let M be the mode sketch for functors (Example 30). Then coSieve(M) =
{{}, {1}, {0, 1}} is the free lattice generated by the single element {1}. We thus have
{lattice morphisms coSieve(M) → Prop} ≃ Prop.
The rest of this subsection is devoted to the proof of Theorem 37. Because of space
constraints, technical details are omitted and found in the extended version [33]. Here we
focus on how to give an inverse construction to Construction 36. The key observation is that
canonical joins of m(i)’s exist and are well-behaved under Axiom A.
▶ Proposition 39. If a function m : M → LAM satisfies Axiom A, then the canonical join
⋁
S m exists for any decidable subset S ⊂ M.

FSCD 2023

## PDF page 14

5:14

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

⋁
Proof. By induction on the size of S. If S is empty, then ∅ m is the bottom modality.
Suppose that S is non-empty. Since M is finite, there is an element i0 minimal in S.
Then S \ {i0 } admits a canonical join by the induction hypothesis. Since i0 is minimal,
⋁
m(i0 ) ≤ ⊥ m(i) for any i : S \ {i0 } by Axiom A, and thus m(i0 ) ≤ ⊥ ( S\{i0 } m). Then we
⋁
⋁
have the canonical join S m ≡ m(i0 ) ∨ ( (S\{i0 }) m) by Proposition 13.
◀
▶ Lemma 40. Let m0 , m1 , and m2 be LAMs such that mi ≤ ⊥ mj for any i < j. Then
m0 ∨ m1 ≤ ⊥ m2 .
Proof. Let A be a (m0 ∨ m1 )-modal type. By Proposition 13, ηm1 (A) : A → #m1 A has
m0 -modal fibers. Then, by assumption, #m1 A and the fibers of ηm1 (A) are made contractible
by #m2 . Thus, #m2 A is contractible.
◀
⋁
⋁
▶ Proposition 41. If a function m : M → LAM satisfies Axiom A, then M\S m ≤ ⊥ ( S m)
for any cosieve S ⊂ M.
Proof. Since S is upward-closed, j ̸≤ i for any i : M \ S and j : S. Thus, by Axiom A,
m(i) ≤ ⊥ m(j) for any i : M \ S and j : S. The claim follows from Lemma 40 and the
construction of the canonical join in Proposition 39.
◀
Sketch of proof of Theorem 37. Let m : M → LAM be a function satisfying Axioms A
and C. We define a function φm : coSieve(M) → Prop by φm (S) ≡ #⋁
m 0 which exists by
M\S

Proposition 39. By Corollary 20 and by Proposition 41, φm (S) is the unique proposition such
⋁
⋁
that Op(φm (S)) = S m. On the other hand, we have S aP = Op(P (S)) by construction,
from which one can derive that the constructions P ↦→ aP and m ↦→ φm are mutually inverses.
We again note that technical details are omitted and found in the extended version [33].
Certain amount of calculation is needed to prove that aP : M → LAM satisfies Axioms A
and C and that φm is a lattice morphism.
◀

4.2

Logical relations as types

We have seen in Section 4.1 that synthetic Tait computability is reformulated in terms of
LAMs. The slogan of synthetic Tait computability is “logical relations as types” [29]. This is
also formulated purely in terms of LAMs.
▶ Fact 42 ([22, Theorem 3.11]). For any LAM m, the universe of m-modal types Um ≡ {A :
U | Inm (A)} is m-modal.
▶ Proposition 43 (Fracture and gluing). Let m and n be LAMs such that m ≤ ⊥ n. Then we
have an equivalence
∑
Um∨n ≃ B:Un B → Um
∑
whose right-to-left function sends a (B, A) to x:B A(x).
Proof. For any B : Un , we have
∑
A:Um A → #m B
≃
≃

{equivalence between fibrations and type families}

#m B → Um
{Fact 42}

B → Um .
Then apply Proposition 13.

◀

## PDF page 15

T. Uemura

5:15

Proposition 43 asserts that a type in Um∨n is a n-modal type equipped with a m-modal
unary (proof-relevant) relation on it, so types (in Um∨n ) are relations. More generally, for
a mode sketch M and a function m : M → LAM satisfying Axiom A, types in U⋁ m are
M
fractured into a sort of generalized relations by iterated applications of Proposition 43.
Intuitively, the ordering on M is understood as “dependency”: every type A : U⋁ m is
M

fractured into a family of type families {Am(i) }i:M such that Am(i) depends on Am(j) for all
j > i. One may also regard the underlying finite poset of M as a FOLDS signature [18].
▶ Example 44. When M is the mode sketch {0 ← 01 → 1}, we have an equivalence
∑
∑
Um(01)∨m(1)∨m(0) ≃ A0 :Um(0) A1 :Um(1) A0 → A1 → Um(01) .
▶ Example 45. When M is the mode sketch {0 → 1 → 2}, we have an equivalence
∑
∑
∏
Um(0)∨m(1)∨m(2) ≃ A2 :Um(2) A1 :A2 →Um(1) x2 A1 (x2 ) → Um(0) .
The equivalence in Proposition 43 nicely interacts with type constructors, and we derive
the logical relation translation (also called the parametricity translation) of dependent type
theory [5, 24, 32, 12] as a theorem in type theory. Let m and n be LAMs such that m ≤ ⊥ n.
Type constructors in Um∨n behave in the same way as the definition of the logical relation
translation of type constructors [12, Section 3] as follows.
Um∨n : ⇑ Um∨n corresponds (via Proposition 43) to the pair (Un , λB.B → Um ).
1 : Um∨n corresponds to the pair (1, λ_.1).
Suppose that A : Um∨n corresponds to a pair (An , Am ). Then (A → Um∨n ) : ⇑ Um∨n
corresponds to the pair
∏
(An → Un , λB. x:An Am (x) → B(x) → Um ).
Indeed,
A → Um∨n
≃

{fracture and gluing}
∑
∑
( x:An Am (x)) → ( B:Un B → Um )
∏
∑
≃
{ distributes over }
∑ ∏
∏ ∏
x
y B(x, y) → Um
B:
x:An Am (x) → Un
≃

{Un ≃ (Am (x) → Un ) since m ≤ ⊥ n}
∑
∏
B:An →Un
x Am (x) → B(x) → Um .

Suppose that A : Um∨n corresponds to a pair (An , Am ) and that B : A → Um∨n corresponds
∏
to a pair (Bn , Bm ). Then x:A B(x) : Um∨n corresponds to the pair
∏
∏ ∏
( xn :An Bn (xn ), λf. xn xm :Am (xn ) Bm (xn , xm , f (xn )))
∑
by a similar calculation to the previous clause. x:A B(x) : Um∨n corresponds to the pair
∑
∑
( xn :An Bn (xn ), λ(an , bn ). xm :Am (an ) Bm (an , xm , bn )).
Suppose that A : Um∨n corresponds to a pair (An , Am ), that a : A corresponds to a pair
(an , am ), and that a′ : A corresponds to a pair (a′n , a′m ). Then a = a′ : Um∨n corresponds
to the pair
m
(an = a′n , λp.am =A
a′m ).
p

FSCD 2023

## PDF page 16

5:16

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

Thus, any type A : Um∨n constructed using these type constructors is fractured into a
type An : Un and a type family Am : An → Um , and Am is equivalent to the logical relation
translation of An . In this sense, types in Um∨n are logical relations. The interaction of the
equivalences in Examples 44 and 45 and type constructors is similarly calculated. We thus
conclude that types in U⋁ m are generalized logical relations.
M

5

Semantics of mode sketches

We give an overview of the semantics of mode sketches in diagrams of ∞-logoses. Many
details are omitted and found in the extended version [33].
We assume that we are given Grothendieck universes U ∈ ⇑ U ∈ ⇑2 U ∈ . . .. An ∞-logos
(over U) is informally an (∞, 1)-category of U-small sheaves over a “space”. Any ∞-logos L
is embedded into its universe enlargement ⇑n L, the (∞, 1)-category of (⇑n U)-small sheaves.
Homotopy type theory is interpreted in any ∞-logos L: types in ⇑n U are interpreted as
objects in ⇑n L; terms are interpreted as morphisms. Note that, instead of choosing universes
in L, we enlarge L with respect to the fixed Grothendieck universes to interpret large types, so
there is no ambiguity in the interpretation of universes. Coherence issues in this interpretation
are solved by presenting an ∞-logos by a model category [26] and then by the local universe
method [15]. The internal language of L is the type theory obtained from homotopy type
theory by adjoining objects and morphisms in ⇑n L as types and terms, respectively.
Let M be a mode sketch. A model of M is an ∞-logos L equipped with a function
m : M → LAM in its internal language satisfying Axioms A–C. We write |M| for the
(∞, 2)-category presented by M as explained in Remark 28. Let ⇑ Cat(2) denote the (∞, 2)(2)
category of (⇑ U)-small (∞, 1)-categories. Let LogosLexAcc ⊂ ⇑ Cat(2) denote the locally full
subcategory whose 0-cells are the ∞-logoses and whose 1-cells are the accessible functors
preserving finite limits. For an (∞, 2)-category C, let C op(1,2) denote the (∞, 2)-category
obtained from C by reversing the directions of 1-cells and 2-cells.
▶ Construction 46. Let L be an ∞-logos. For a LAM m in the internal language of L, the
externalization of Um is the full subcategory of L spanned by the m-modal types. For a function
m : M → LAM from a mode sketch M in the internal language of L, the externalizations of
m(j)
m(i);m(k)
Um(i) ’s and the functions #m(i) and ηm(j)
form a functor |M|op(1,2) → ⇑ Cat(2) which
we call the externalization of the diagram {Um(i) }i:M . It turns out that this functor factors
(2)

through LogosLexAcc by verifying that the LAMs in the internal language of L correspond
to the lex, accessible localizations of L [33, Section 8].
▶ Construction 47. Let I be a small (∞, 2)-category and C : I op(1,2) → ⇑ Cat(2) a functor.
The oplax limit of C is the (∞, 1)-category opLaxLimi∈I Ci described as follows. An object
x in opLaxLimi∈I Ci consists of: an object xi ∈ Ci for any object i ∈ I; a morphism
xα : xi → Cα (xj ) for any morphism α : i → j in I; some coherence data. A morphism
u : x → y in opLaxLimi∈I Ci consists of: a morphism ui : xi → yi for any object i ∈ I; a
homotopy uα filling the square
xi

ui

xα

Cα (xj )

yi
yα

Cα (uj )

Cα (yj )

for any morphism α : i → j in I; some coherence data. See [33, Section 9] for more explicit
construction.

## PDF page 17

T. Uemura

5:17

▶ Theorem 48. For any mode sketch M, we have an equivalence between the following
spaces:
the space of models of M;
(2)
the space of functors |M|op(1,2) → LogosLexAcc .
(2)
Moreover, when a model (L, m) of M corresponds to a functor K : |M|op(1,2) → LogosLexAcc ,
the following hold.
1. L ≃ opLaxLimi∈|M| Ki
2. K is the externalization of the diagram {Um(i) }i:M in the internal language of L.
(2)

Sketch of proof. Let K : |M|op(1,2) → LogosLexAcc be a functor.
opLaxLimi∈|M| Ki . For a cosieve S on M, we define ψK (S) ∈ L by
{
ψK (S)i =

We define L =

1 if i ∈ S
0 otherwise.

The other components are uniquely determined by the universal properties of initial and
final objects. This determines a lattice morphism ψK : coSieve(M) → Prop in the internal
language of L. By Theorem 37, this corresponds to a function m : M → LAM satisfying
Axioms A and C. One can show that the induced diagram {Um(i) }i:M is interpreted as the
given diagram K, from which it follows that m also satisfies Axiom B. Thus, L is part of a
model of M. This construction is an equivalence by externalizing the argument of exhibiting
U ≃ U⋁ m as the oplax limit of the diagram {Um(i) }i:M (Section 3.3).
◀
M

References
1
2

3

4

5

6

7
8

Mathieu Anel, Georg Biedermann, Eric Finster, and André Joyal. A generalized Blakers-Massey
theorem. J. Topol., 13(4):1521–1553, 2020. doi:10.1112/topo.12163.
Mathieu Anel and André Joyal. Topo-logie. In New spaces in mathematics. Formal and
conceptual reflections, pages 155–257. Cambridge University Press, 2021. doi:10.1017/
9781108854429.007.
Peter Arndt and Krzysztof Kapulkin. Homotopy-Theoretic Models of Type Theory. In Luke
Ong, editor, Typed Lambda Calculi and Applications: 10th International Conference, TLCA
2011, Novi Sad, Serbia, June 1-3, 2011. Proceedings, pages 45–60, Berlin, Heidelberg, 2011.
Springer Berlin Heidelberg. doi:10.1007/978-3-642-21691-6_7.
Steve Awodey and Michael A. Warren. Homotopy theoretic models of identity types.
Mathematical Proceedings of the Cambridge Philosophical Society, 146(1):45–55, 2009. doi:
10.1017/S0305004108001783.
Jean-Philippe Bernardy, Patrik Jansson, and Ross Paterson. Proofs for Free: Parametricity
for Dependent Types. Journal of Functional Programming, 22(2):107–152, March 2012.
doi:10.1017/S0956796812000056.
John W. Duskin. Simplicial matrices and the nerves of weak n-categories. I. Nerves of
bicategories. Theory Appl. Categ., 9:198–308, 2001/02. CT2000 Conference (Como). URL:
http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html.
Eric Finster. A Note on Left Exact Modalities in Type Theory. URL: https://ericfinster.
github.io/files/lmhtt.pdf.
Daniel Gratzer. Normalization for Multimodal Type Theory. In Christel Baier and Dana
Fisman, editors, LICS ’22: 37th Annual ACM/IEEE Symposium on Logic in Computer Science,
Haifa, Israel, August 2 - 5, 2022, pages 2:1–2:13. ACM, 2022. doi:10.1145/3531130.3532398.

FSCD 2023

## PDF page 18

5:18

Homotopy Type Theory as Internal Languages of Diagrams of ∞-Logoses

9

10

11
12

13
14

15

16
17
18
19
20
21
22
23

24
25

26
27
28

29

Daniel Gratzer, G. A. Kavvos, Andreas Nuyts, and Lars Birkedal. Multimodal Dependent
Type Theory. Logical Methods in Computer Science, Volume 17, Issue 3, July 2021. doi:
10.46298/lmcs-17(3:11)2021.
Kuen-Bang Hou (Favonia), Eric Finster, Daniel R. Licata, and Peter LeFanu Lumsdaine. A
Mechanization of the Blakers-Massey Connectivity Theorem in Homotopy Type Theory. In
Proceedings of the 31st Annual ACM/IEEE Symposium on Logic in Computer Science, LICS
’16, pages 565–574, New York, NY, USA, 2016. ACM. doi:10.1145/2933575.2934545.
Peter T. Johnstone. Sketches of an Elephant : A Topos Theory Compendium Volume 1,
volume 43 of Oxford Logic Guides. Oxford University Press, 2002.
Marc Lasson. Canonicity of Weak ω-groupoid Laws Using Parametricity Theory. Electronic
Notes in Theoretical Computer Science, 308:229–244, 2014. doi:10.1016/j.entcs.2014.10.
013.
F. William Lawvere. Axiomatic cohesion. Theory Appl. Categ., 19:No. 3, 41–49, 2007. URL:
http://www.tac.mta.ca/tac/volumes/19/3/19-03abs.html.
Daniel R. Licata, Ian Orton, Andrew M. Pitts, and Bas Spitters. Internal Universes in Models
of Homotopy Type Theory. In Hélène Kirchner, editor, 3rd International Conference on Formal
Structures for Computation and Deduction (FSCD 2018), volume 108 of Leibniz International
Proceedings in Informatics (LIPIcs), pages 22:1–22:17, Dagstuhl, Germany, 2018. Schloss
Dagstuhl–Leibniz-Zentrum fuer Informatik. doi:10.4230/LIPIcs.FSCD.2018.22.
Peter LeFanu Lumsdaine and Michael A. Warren. The Local Universes Model: An Overlooked
Coherence Construction for Dependent Type Theories. ACM Trans. Comput. Logic, 16(3):23:1–
23:31, July 2015. doi:10.1145/2754931.
Jacob Lurie. Higher Topos Theory, volume 170 of Annals of Mathematics Studies. Princeton
University Press, 2009. URL: https://www.math.ias.edu/~lurie/papers/HTT.pdf.
Jacob Lurie. (∞, 2)-Categories and the Goodwillie Calculus I, 2009. arXiv:0905.0462v2.
Michael Makkai. First Order Logic with Dependent Sorts, with Applications to Category
Theory, 1995. URL: http://www.math.mcgill.ca/makkai/folds/foldsinpdf/FOLDS.pdf.
Per Martin-Löf. An Intuitionistic Theory of Types: Predicative Part. Studies in Logic and the
Foundations of Mathematics, 80:73–118, 1975. doi:10.1016/S0049-237X(08)71945-1.
Hoang Kim Nguyen and Taichi Uemura. ∞-type theories, 2022. arXiv:2205.00798v1.
Egbert Rijke. Introduction to Homotopy Type Theory, 2022. arXiv:2212.11082v1.
Egbert Rijke, Michael Shulman, and Bas Spitters. Modalities in homotopy type theory. Log.
Methods Comput. Sci., 16(1):Paper No. 2, 79, 2020. doi:10.23638/LMCS-16(1:2)2020.
Urs Schreiber and Michael Shulman. Quantum Gauge Field Theory in Cohesive Homotopy
Type Theory. In Ross Duncan and Prakash Panangaden, editors, Proceedings 9th Workshop
on Quantum Physics and Logic, QPL 2012, Brussels, Belgium, 10-12 October 2012, volume
158 of EPTCS, pages 109–126, 2012. doi:10.4204/EPTCS.158.8.
Michael Shulman. Univalence for inverse diagrams and homotopy canonicity. Mathematical
Structures in Computer Science, 25(05):1203–1277, 2015. doi:10.1017/s0960129514000565.
Michael Shulman. Brouwer’s fixed-point theorem in real-cohesive homotopy type theory.
Mathematical Structures in Computer Science, 28(6):856–941, 2018.
doi:10.1017/
S0960129517000147.
Michael Shulman. All (∞, 1)-toposes have strict univalent universes, 2019. arXiv:1904.
07004v2.
Jonathan Sterling. First Steps in Synthetic Tait Computability. PhD thesis, Carnegie Mellon
University, 2021. URL: https://www.jonmsterling.com/pdfs/sterling:2021:thesis.pdf.
Jonathan Sterling and Carlo Angiuli. Normalization for Cubical Type Theory. In 2021 36th
Annual ACM/IEEE Symposium on Logic in Computer Science (LICS), pages 1–15, 2021.
doi:10.1109/LICS52264.2021.9470719.
Jonathan Sterling and Robert Harper. Logical Relations as Types: Proof-Relevant
Parametricity for Program Modules. J. ACM, 68(6):41:1–41:47, 2021. doi:10.1145/3474834.

## PDF page 19

T. Uemura

30

31
32
33
34
35

5:19

Jonathan Sterling and Robert Harper.
Sheaf Semantics of Termination-Insensitive
Noninterference. In Amy P. Felty, editor, 7th International Conference on Formal Structures
for Computation and Deduction (FSCD 2022), volume 228 of Leibniz International Proceedings
in Informatics (LIPIcs), pages 5:1–5:19, Dagstuhl, Germany, 2022. Schloss Dagstuhl – LeibnizZentrum für Informatik. doi:10.4230/LIPIcs.FSCD.2022.5.
The Univalent Foundations Program. Homotopy Type Theory: Univalent Foundations of
Mathematics, 2013. URL: http://homotopytypetheory.org/book/.
Taichi Uemura. Fibred Fibration Categories. In 2017 32nd Annual ACM/IEEE Symposium on
Logic in Computer Science (LICS), pages 1–12, June 2017. doi:10.1109/LICS.2017.8005084.
Taichi Uemura. Homotopy type theory as internal languages of diagrams of ∞-logoses, 2022.
arXiv:2212.02444v1.
Taichi Uemura. Normalization and coherence for ∞-type theories, 2022. arXiv:2212.11764v1.
Gavin Wraith. Artin glueing. J. Pure Appl. Algebra, 4:345–348, 1974. doi:10.1016/
0022-4049(74)90014-0.

FSCD 2023
