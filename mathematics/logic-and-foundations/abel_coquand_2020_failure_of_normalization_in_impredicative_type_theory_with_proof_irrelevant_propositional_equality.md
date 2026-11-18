Source: https://doi.org/10.23638/LMCS-16(2:14)2020
PDF sha256: a7279158c5d217cf2fe1657a27856d2aec60337123d9b58eb77d3dfd18bc3de5
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of abel_coquand_2020_failure_of_normalization_in_impredicative_type_theory_with_proof_irrelevant_propositional_equality.pdf

Transcription of `abel_coquand_2020_failure_of_normalization_in_impredicative_type_theory_with_proof_irrelevant_propositional_equality.pdf` in this directory, 5 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-5 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Logical Methods in Computer Science
Volume 16, Issue 2, 2020, pp. 14:1–14:5
https://lmcs.episciences.org/

Submitted
Published

Feb. 03, 2020
Jun. 30, 2020

FAILURE OF NORMALIZATION IN IMPREDICATIVE TYPE THEORY
WITH PROOF-IRRELEVANT PROPOSITIONAL EQUALITY
ANDREAS ABEL AND THIERRY COQUAND
Department for Computer Science and Engineering, Chalmers and Gothenburg University
e-mail address: {andreas.abel,thierry.coquand}@cse.gu.se

Abstract. Normalization fails in type theory with an impredicative universe of propositions and a proof-irrelevant propositional equality. The counterexample to normalization is
adapted from Girard’s counterexample against normalization of System F equipped with a
decider for type equality. It refutes Werner’s normalization conjecture published in LMCS
[Wer08].

Introduction
Type theories with an impredicative universe Prop of propositions, such as the Calculus of
Constructions [CH88], lose the normalization property in the presence of a proof-irrelevant
propositional equality = : Π A : Type. A → A → Prop with the standard elimination
principle. The loss of normalization is facilitated already by a coercion function with a
reduction rule
cast : Π A B : Prop. A =Prop B → A → B
cast A A e x ▷ x
that does not inspect the equality proof e : A =Prop A but only checks whether the endpoints
are (definitionally) equal.
The failure of normalization refutes a conjecture by Werner [Wer08, Conjecture 3.14].
Consistency and canonicity is not at stake; thus, the situation is comparable to type theory
with equality reflection [ML84b, ML84a], aka Extensional Type Theory. At the moment, it
is unclear whether the use of impredicativity is essential to break normalization; predicative
type theory might be able to host a proof-irrelevant propositional equality [Abe09] while
retaining normalization.
Key words and phrases: impredicativity, normalization, proof-irrelevance, propositional equality.

l

LOGICAL METHODS
IN COMPUTER SCIENCE

DOI:10.23638/LMCS-16(2:14)2020

c A. Abel and T. Coquand
⃝
CC
⃝
Creative Commons

## PDF page 2

14:2

A. Abel and T. Coquand

Vol. 16:2

Counterexample to Normalization
We employ the usual impredicative definition of absurdity ⊥ and negation ¬A and a derived
definition of truth ⊤:
⊥ : Prop
¬
: Prop → Prop
⊤ : Prop
⊥ = Π A : Prop. A
¬A = A → ⊥
⊤ = ¬⊥
The presence of cast allows us to define self-application under the assumption that all
propositions all equal. The self-application term ω refutes this assumption.
δ
: ⊤
ω
: ¬Π A B : Prop. A =Prop B
δz = z⊤z
ω h A = cast ⊤ A (h ⊤ A) δ
Impredicativity is exploited in δ when applying z : ⊥ to type ⊤ = ⊥ → ⊥ so that it can be
applied to z again. The type of δ is ⊤ which we cast to A thanks to the assumption h that
all propositions are equal.
We build a non-normalizing term Ω by applying ω to itself through δ, reminiscent of
the shortest diverging term in untyped λ-calculus.
Ω
: ¬Π A B : Prop. A =Prop B
Ω h = δ (ω h)
Thanks to the reduction rule of cast, term Ω h reduces to itself:
Ω h = δ (ω h)
▷ ω h ⊤ (ω h)
= cast ⊤ ⊤ (h ⊤ ⊤) δ (ω h) ▷ δ (ω h)
= Ωh
Thus, normalization is lost in the presence of a hypothesis (free variable) h. As a consequence,
normalization that proceeds under λ-abstraction can diverge. This means that equality of
open terms cannot be decided just by normalization.
The counterexample can be implemented in Werner’s type theory with proof-irrelevance
[Wer08], refuting the normalization conjecture (3.14). We implement cast as instance of
Werner’s more general equality elimination rule:
: Π A : Type. Π P : A → Type. Π a b : A. P a → a =A b → P b
Eq rec
Eq rec A P a b x e ▷ x
if a = b
cast A B e x
= Eq rec Prop (λ a:A. Prop) A B x e
The term Ω also serves as counterexample to normalization in the theorem prover Lean
[dMKA+ 15], version 3.4.2 [Mic19].
def False := ∀ A : Prop, A
def Not
:= λ A, A → False
def True := Not False
def delta :
def omega :
def Omega :

True
:= λ z, z True z
Not (∀ A B : Prop, A = B) := λ h A, cast (h True A) delta
Not (∀ A B : Prop, A = B) := λ h, delta (omega h)

Infinite reduction can now be triggered with the command #reduce Omega, which diverges.

## PDF page 3

Vol. 16:2

NORMALIZATION FAILS FOR IMPREDICATIVE PROOF-IRRELEVANT EQUALITY

14:3

A Counterexample Using Propositional Extensionality
The counterexample of the last section used the absurd assumption that all proposition are
equal. The following counterexample utilizes just the axiom of propositional extensionality,
propext, which is a default axiom of Lean. In fact, the weaker statement tautext, which
states the equality of true propositions, is sufficient.
propext : Π A B : Prop. (A ↔ B) → A =Prop B
tautext : Π A B : Prop. A → B → A =Prop B
The counterexample uses the standard impredicative definition of truth,
⊤ = Π A : Prop. A → A
and a cast from ⊤ → ⊤ to A, which are both tautologies under the assumption a : A.
id, δ : ⊤ → ⊤
ω, Ω
: ⊤
id x = x
ω A a = cast (⊤ → ⊤) A (tautext (⊤ → ⊤) A id a) δ
δz
= z (⊤ → ⊤) id z
Ω
= δω
These definitions can be directly replayed in Lean 3.4.2 with the standard prelude, yielding
a non-normalizing term Omega.
def tautext {A B : Prop} (a : A) (b : B)
: A = B
:= propext (iff.intro (λ _, b) (λ _, a))
def True : Prop
:= ∀ A : Prop, A → A
def delta : True → True := λ z : True, z (True → True) id z
def omega : True
:= λ A a, cast (tautext id a) delta
def Omega : True
:= delta omega
Note that term Omega is closed with respect the standard axioms of Lean, and does not even
have a weak head normal form.
Related Work and Conclusions
The cast operator is inspired by Girard’s operator J : Π A B : Prop. A → B with reduction
rule J A A M ▷ M that destroys the normalization property of System F [Gir71, HM99].
In contrast to J, our cast also requires a proof of equality of A and B, but this proof is not
inspected and thus does not block reduction if it is non-canonical. Thus, the simple lie that
all propositions are equal is sufficient to trigger divergence.
Historically, the Automath system AUT-4 is maybe the first type-theoretic proof assistant
to feature proof-irrelevant propositions [dB94]. The terminology used by de Bruijn is fourth
degree identification, where proofs are expressions considered to have degree 4, propositions
and values degree 3, types and Prop degree 2, and the universe Type of types degree 1.
Lean’s type theory [Car19] features an impredicative universe of proof-irrelevant propositions which hosts both propositional equality and the accessibility predicate [Acz77, 1.2].
As both may be eliminated into computational universes, decidability of definitional equality
is lost, as demonstrated by Carneiro [Car19] for the case of accessibility. As a consequence,
typing is not decidable.
The type-theoretic proof assistants Agda and Coq have recently [GCST19] been equipped
with a proof-irrelevant universe of propositions (“strict Prop”). In this universe, propositional
equality can be defined, but cannot be eliminated into types that are not strict propositions

## PDF page 4

14:4

A. Abel and T. Coquand

Vol. 16:2

themselves. Under this restriction, Gilbert [Gil19, 4.3] formally proved normalization and
decidability of type checking for the predicative case.
Several open problems remain:
(1) Does the theory with impredicative strict Prop have normalization and decidability of
type checking as well?
(2) Does the addition of Werner’s rule, while destroying proof normalization, preserve
decidability of conversion and type checking? (Since proofs are irrelevant for equality,
they need not be normalized during type checking.)
(3) Does Werner’s rule preserve normalization in the predicative case? (Our counterexamples
make use of impredicativity.)
Acknowledgments. The authors acknowledge support by the Swedish Research Council
(Vetenskapsrådet) under grants 2014-04864 Termination Certificates for Dependently-Typed
Programs and Proofs via Refinement Types and 2017-04064 Syntax and Semantics of Univalent Type Theory. Our research group is part of the EU Cost Action CA15123 The European
research network on types for programming and verification (EUTypes). We thank Mario
Carneiro for contributing the original Lean implementation of the first counterexample.
References
[Abe09]

Andreas Abel. Extensional normalization in the logical framework with proof irrelevant equality.
In Olivier Danvy, editor, Workshop on Normalization by Evaluation, affiliated to LiCS 2009,
Los Angeles, 15 August 2009, 2009.
[Acz77]
Peter Aczel. An introduction to inductive definitions. In Jon Barwise, editor, Handbook of
Mathematical Logic, volume 90 of Studies in Logic and the Foundations of Mathematics, pages
739–782. Elsevier, 1977.
[Car19]
Mario Carneiro. The type theory of Lean. Master’s thesis, Department of Philosophy, Carnegie
Mellon University, 2019.
Thierry Coquand and Gérard P. Huet. The calculus of constructions. Information and Compu[CH88]
tation, 76(2/3):95–120, 1988.
[dB94]
N.G. de Bruijn. Some extensions of Automath: The AUT-4 family. In R.P. Nederpelt, J.H.
Geuvers, and R.C. de Vrijer, editors, Selected Papers on Automath, volume 133 of Studies in
Logic and the Foundations of Mathematics, pages 283–288. Elsevier, 1994.
[dMKA+ 15] Leonardo Mendonça de Moura, Soonho Kong, Jeremy Avigad, Floris van Doorn, and Jakob von
Raumer. The Lean theorem prover (system description). In Amy P. Felty and Aart Middeldorp,
editors, Automated Deduction - CADE-25 - 25th International Conference on Automated
Deduction, Berlin, Germany, August 1-7, 2015, Proceedings, volume 9195 of Lecture Notes in
Computer Science, pages 378–388. Springer, 2015.
[GCST19] Gaëtan Gilbert, Jesper Cockx, Matthieu Sozeau, and Nicolas Tabareau. Definitional proofirrelevance without K. Proceedings of the ACM on Programming Languages, 3(POPL):3:1–3:28,
2019.
[Gil19]
Gaëtan Gilbert. A type theory with definitional proof-irrelevance. PhD thesis, École Nationale
Supérieure Mines-Télécom Atlantique, 2019.
[Gir71]
Jean-Yves Girard. Une extension de l’interprétation de Gödel à l’analyse, et son application
à l’élimination des coupures dans l’analyse et la théorie des types. In J. E. Fenstad, editor,
Proceedings of the Second Scandinavian Logic Symposium (Univ. Oslo, 1970), volume 63 of
Studies in Logic and the Foundations of Mathematics, pages 63–92. Elsevier, 1971.
[HM99]
Robert Harper and John C. Mitchell. Parametricity and variants of Girard’s J operator.
Information Processing Letters, 70(1):1–5, 1999.
[Mic19]
Microsoft Research. Lean theorem prover, 2019. Version 3.4.2.

## PDF page 5

Vol. 16:2

NORMALIZATION FAILS FOR IMPREDICATIVE PROOF-IRRELEVANT EQUALITY

[ML84a]

Per Martin-Löf. Constructive mathematics and computer programming. volume 312, pages
501–518. The Royal Society, 1984.
Per Martin-Löf. Intuitionistic Type Theory. Bibliopolis, 1984.
Benjamin Werner. On the strength of proof-irrelevant type theories. Logical Methods in Computer
Science, 4(3), 2008.

[ML84b]
[Wer08]

14:5

This work is licensed under the Creative Commons Attribution License. To view a copy of this
license, visit https://creativecommons.org/licenses/by/4.0/ or send a letter to Creative
Commons, 171 Second St, Suite 300, San Francisco, CA 94105, USA, or Eisenacher Strasse
2, 10777 Berlin, Germany
