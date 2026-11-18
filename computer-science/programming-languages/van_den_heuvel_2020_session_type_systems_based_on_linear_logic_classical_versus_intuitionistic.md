Source: https://doi.org/10.4204/EPTCS.314.1
PDF sha256: 9b11b7be4489fa42df9426dd198bcec25792acd0d983247d5a9ec5a0c756c3bd
License: CC BY-SA, version not stated
Language: eng
Fidelity: machine-gated

# Transcription of van_den_heuvel_2020_session_type_systems_based_on_linear_logic_classical_versus_intuitionistic.pdf

Transcription of `van_den_heuvel_2020_session_type_systems_based_on_linear_logic_classical_versus_intuitionistic.pdf` in this directory, 11 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-11 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Session Type Systems based on Linear Logic:
Classical versus Intuitionistic∗
Bas van den Heuvel

Jorge A. Pérez

University of Groningen, The Netherlands

Session type systems have been given logical foundations via Curry-Howard correspondences based
on both intuitionistic and classical linear logic. The type systems derived from the two logics enforce
communication correctness on the same class of π-calculus processes, but they are significantly
different. Caires, Pfenning, and Toninho informally observed that, unlike the classical type system,
the intuitionistic type system enforces locality for shared channels, i.e. received channels cannot be
used for replicated input. In this paper, we revisit this observation from a formal standpoint. We
develop United Linear Logic (ULL), a logic encompassing both classical and intuitionistic linear logic.
Then, following the Curry-Howard correspondences for session types, we define πULL, a session type
system for the π-calculus based on ULL. Using πULL we can formally assess the difference between
the intuitionistic and classical type systems, and justify the role of locality and symmetry therein.

1

Introduction

Session types are a popular approach to typing message-passing concurrency [10, 11, 17]. They describe
communication over channels as sequences of communication actions. This way, e.g., the session type
!int.?bool.end types a channel as follows: send an integer, receive a boolean, and close the channel. Due
to its simplicity and expressiveness, the π-calculus [15, 16]—the paradigmatic model of concurrency and
interaction—is a widely used setting for studying session types.
In a line of work developed by Caires, Pfenning, Wadler, and several others, the theory of session
types has been given strong logical foundations. Caires and Pfenning discovered a Curry-Howard correspondence between a form of session types for the π-calculus and Girard’s linear logic [8]: session
types correspond to linear logic propositions, type inference rules to sequent calculus, and communication to cut reduction [2]. The resulting session type system ensures important correctness properties
for communicating processes: protocol fidelity, communication safety, deadlock freedom, and strong
normalization.
As in standard logic, there are two “schools” of linear logic: classical [8] and intuitionistic [1]. The
differences between classical and intuitionistic linear logic are known—see, e.g., [5, 12]. This dichotomy
also appears in the logical foundations of session types: while Caires and Pfenning’s correspondence
relies on intuitionistic linear logic [1], Wadler developed a correspondence based on classical linear
logic [18]. Superficial differences between the resulting type systems include the number of typing rules
(the intuitionistic system has roughly twice as many rules as the classical system) and the shape/meaning
of typing judgments (in the intuitionistic system, judgments have a rely-guarantee reading not present in
the classical system). In turn, these differences follow from the way in which each system internalizes
duality: the classical system provides a more explicit account of duality than the intuitionistic system.
∗ Work partially supported by the Netherlands Organization for Scientific Research (NWO) under the VIDI Project No.
016.Vidi.189.046 (Unifying Correctness for Communicating Software).

S. Balzer, L. Padovani (Eds.): Programming Language Approaches
to Concurrency- & Communication-cEntric Software (PLACES 2020)
EPTCS 314, 2020, pp. 1–11, doi:10.4204/EPTCS.314.1

This work is licensed under the Creative Commons
Attribution-Share Alike License.

## PDF page 2

2

Session Type Systems based on Linear Logic: Classical versus Intuitionistic

We are interested in going beyond these superficial differences, so as to establish a formal comparison
between the two type systems. This seems to us an indispensable step in consolidating the logical
foundations of message-passing concurrency. To our knowledge, the only available comparison is
informal: Caires, Pfenning, and Toninho [4] observed that a more fundamental difference concerns
the locality principle for shared channels. The principle states that received channels cannot be used
for further reception, i.e., only the output capability of channels can be sent [13]. In session-based
concurrency, shared channels define services; clients connect to services by sending a linear channel.
Locality of shared channels therefore means that received channels cannot be used to provide a service.
Well-known from a foundational perspective, locality has been promoted as a sensible principle for
distributed implementations of (object-oriented) languages based on the π-calculus [14]. The observation
in [4] is that Caires and Pfenning’s intuitionistic interpretation of session types enforces locality of
shared channels [4], whereas Wadler’s classical interpretation does not: processes that break locality are
well-typed in [18].
The existence of a class of processes that is typable in one system but not in the other immediately
frames the desired formal comparison as an expressiveness question: the type system in [18] can be
considered to be more expressive than the one in [2]. To formally examine this question, the first step is
defining a basic framework of reference in which both type systems can be objectively compared. To this
end, we build upon Girard’s Logic of Unity [9], which subsumes classical, intuitionistic and linear logic
in one system. In the same spirit, we develop United Linear Logic (ULL): a logic that subsumes classical
and intuitionistic linear logic. Following the Curry-Howard correspondence by Caires and Pfenning, we
interpret ULL as a session type system for the π-calculus, dubbed πULL. The class of πULL-typable
processes therefore contains processes induced by type systems derived from both intuitionistic and
classical interpretations of linear logic. Using πULL, we corroborate and formalize Caires, Pfenning,
and Toninho’s observation as inclusions between classes of typable processes: our technical results are
that (i) πULL precisely captures the class of processes typable under the classical interpretation and that
(ii) the class of processes typable under the intuitionistic interpretation is strictly included in πULL.
This paper is structured as follows. In Section 2 we introduce ULL, explain the Curry-Howard
interpretation as the session type system πULL, and detail the correctness properties for processes
derived by typing. Section 3 formally establishes the differences between the classical and intuitionistic
interpretations of linear logic as session type systems. Section 4 concludes the paper.

2

United Linear Logic as a Session Type System

In this section, we introduce United Linear Logic (ULL), a logic based on the linear fragment of Girard’s
Logic of Unity [9]. We present ULL as a session type system for the π-calculus [15, 16], dubbed πULL,
following the Curry-Howard correspondences established by Caires and Pfenning [2] and by Wadler [18].
Propositions / Types. Propositions in ULL correspond to session types in πULL; they are defined as
follows:
Definition 2.1. ULL propositions / πULL types are generated by the following grammar:
&

A, B ::= 1 | ⊥ | A ⊗ B | A

B | A ⊸ B | !A | ?A

Session types represent sequences of communication actions that should be performed along channels.
Table 1 gives the intuitive reading of the interpretation of propositions as session types. Note that there
are two types for reception: from classical and ⊸ from intuitionistic linear logic.
&

## PDF page 3

B. van den Heuvel, J.A. Pérez
1 and ⊥
A⊗B
A B and A ⊸ B
!A
?A

3
Close the channel
Send a channel of type A and continue as B
Receive a channel of type A and continue as B
Repeatedly provide a service of type A
Connect to a service of type A

&

Table 1: Interpretation of ULL propositions as session types
ULL does not include the additives A ⊕ B and A & B of linear logic. Although the Logic of Unity
does include these connectives, we leave them out from ULL (and πULL), because their interpretation
as session types—internal and external choice, respectively—largely coincides in many presentations
of logic-based session types. Therefore they are not particularly insightful in our formal comparison.
They can be easily accommodated in ULL, with the possibility of choosing between binary choice (as in
e.g. [2, 4]) and n-ary choice (as in e.g. [3, 18]).
Duality. The duality of ULL propositions is given in Definition 2.2. In πULL duality is reflected by the
intended reciprocity of protocols between two parties: when a process on one side of a channel sends, the
process on the opposite side must receive, and vice versa.
Definition 2.2. Duality (A⊥ ) is given by the following set of equations:

&

(A

B⊥

(!A)⊥ := ?A⊥

B)⊥ := A⊥ ⊗ B⊥

(?A)⊥ := !A⊥

It is easy to see that duality is an involution: (A⊥ )⊥ = A. As usual, we decree that A ⊸ B = A⊥
this, we can derive the relation between ⊸ and ⊗ by means of their duals:

&

(A ⊗ B)⊥ = A⊥

&

(A ⊸ B)⊥ = (A⊥

&

(A ⊗ B)⊥ := A⊥

&

1 ⊥ := ⊥
⊥⊥ := 1

B. From

B)⊥ = (A⊥ )⊥ ⊗ B⊥ = A ⊗ B⊥

B⊥ = A ⊸ B⊥

Processes. πULL is a type system for the π-calculus processes defined as follows:
Definition 2.3. Process terms are generated by the following grammar:
P, Q := 0 | [x ↔ y] | (νx)P | P | Q | x⟨y⟩.P | x(y).P|!x(y).P | x⟨⟩.0 | x().P
Process constructs for inaction 0 , channel restriction (νx)P, and parallel composition P | Q have standard
readings. The same applies to constructs for output, input, and replicated input prefixes, which are denoted
x⟨y⟩.P, x(y).P, and !x(y).P, respectively. Process [x ↔ y] denotes a forwarder that “fuses” channels x
and y. We consider also constructs x⟨⟩.00 and x().P, which specify the explicit closing of channels: their
synchronization represents the explicit de-allocation of linear resources. These constructs result from the
non-silent interpretation of 1 , which, as explained in [3], leads to a Curry-Howard correspondence that is
stronger than correspondences with silent interpretations of 1 (such as those in [2, 4]).

## PDF page 4

4

Session Type Systems based on Linear Logic: Classical versus Intuitionistic

Structural congruence. Processes can be syntactically different, but still exhibit the same behavior.
Such processes are structurally congruent, in the sense of the following definition:
Definition 2.4. Structural congruence (≡) is given by the following set of equations, where ≡α denotes equality up to capture-avoiding α-conversion, and fn(P) gives the set of free names in P, i.e. the
complement of bn(P): the names in P bound by restriction (νx) and (replicated) input x(y) and !x(y):
P|0 ≡ P

P | (Q | R) ≡ (P | Q) | R

P|Q ≡ Q|P
(νx)0 ≡ 0

[x ↔ y] ≡ [y ↔ x]
P ≡α Q =⇒ P ≡ Q

(νx)(νy)P ≡ (νy)(νx)P

x∈
/ fn(P) =⇒ P | (νx)Q ≡ (νx)(P | Q)

Computation. In a Curry-Howard correspondence, computation is related to cut reduction in the logic.
Cut reduction removes cuts from an inference tree, which reduces the size of the tree without changing
the result of the inference. In the correspondence between linear logic and the π-calculus, cut reduction is
related to communication, defined by the following reduction relation:
Definition 2.5. Reduction of process terms (→) is given by the following relation:
x⟨y⟩.P | x(z).Q → P | Q{y/z}

Q → Q′ =⇒ P | Q → P | Q′

x⟨y⟩.P|!x(z).Q → P | Q{y/z}|!x(z).Q
x⟨⟩.0 | x().Q → Q

P → Q =⇒ (νy)P → (νy)Q
P ≡ P′ ∧ P′ → Q′ ∧ Q′ ≡ Q =⇒ P → Q

P | [x ↔ y] → P{y/x}
Typing inference. The inference system of ULL is a sequent calculus with sequents of the form Γ; ∆ ⊢ Λ
in which Γ is a collection of propositions that can be indefinitely used, and ∆ and Λ collect propositions
that must be used linearly (exactly once). With respect to the Logic of Unity, we added a left rule for 1
and a right rule for ⊥, and removed rules that allow propositions to switch sides in a sequent.
πULL’s typing inference system annotates sequents with process terms and channel names to form
typing judgments of the following form:
Γ; ∆ ⊢ P :: Λ
In this interpretation, Γ (resp. ∆ and Λ), the unrestricted (resp. linear) context of P, consists of assignments
of the form x : A, where x is a channel and A is a proposition/type. In a correct inference, these contexts
together contain exactly the free channel names of the process term P. We write · to denote an empty
context. πULL’s inference rules are given in Figure 1. Note that some rules are labeled with an ‘∗’, which
we use to distinguish a class of rules to be used in the formal comparison in the next section.
Cut reduction and identity expansion. Caires, Pfenning, and Toninho [3] showed that the validity
of session type interpretations of linear logic propositions can be demonstrated by checking that cut
reductions in typing inferences do correspond to reductions of processes, as well as by showing that the
identity axiom of any type can be expanded to a larger process term with forwarding of a smaller type.
Following this approach, πULL can be shown valid for all reductions, using C UT R as well as C UT L, and
expansions, using I D R as well as I D L.
Correctness properties. As is usual for Curry-Howard correspondences for concurrency, the cut elimination property of linear logic means that πULL has the soundness/subject reduction (Theorem 2.1) and
progress (Theorem 2.2) properties.

## PDF page 5

B. van den Heuvel, J.A. Pérez

Γ; x : A ⊢ [x ↔ y] :: y : A

5

(∗ I D R)

Γ; x : A, y : A⊥ ⊢ [x ↔ y] :: ·

(I D L)

Γ; ∆ ⊢ P :: Λ, x : A
Γ; ∆′ , x : A ⊢ Q :: Λ′ ∗
( C UT R)
Γ; ∆, ∆′ ⊢ (νx)(P | Q) :: Λ, Λ′
Γ; ∆, x : A ⊢ P :: Λ
Γ; ∆′ , x : A⊥ ⊢ Q :: Λ′
(C UT L)
Γ; ∆, ∆′ ⊢ (νx)(P | Q) :: Λ, Λ′
Γ; x : A⊥ ⊢ P :: ·
Γ, u : A; ∆ ⊢ Q :: Λ
(C UT? )
Γ; ∆ ⊢ (νu)(!u(x).P | Q) :: Λ
Γ; · ⊢ P :: x : A
Γ, u : A; ∆ ⊢ Q :: Λ ∗
( C UT! )
Γ; ∆ ⊢ (νu)(!u(x).P | Q) :: Λ
Γ, u : A; ∆, x : A ⊢ P :: Λ
(∗ C OPY L)
Γ, u : A; ∆ ⊢ (νx)u⟨x⟩.P :: Λ
Γ; ∆ ⊢ P :: Λ
(∗ 1 L)
Γ; ∆, x : 1 ⊢ x().P :: Λ

Γ, u : A; ∆ ⊢ P :: Λ, x : A⊥
(C OPY R)
Γ, u : A; ∆ ⊢ (νx)u⟨x⟩.P :: Λ
Γ; · ⊢ x⟨⟩.0 :: x : 1

(∗ 1 R)

Γ; ∆ ⊢ P :: Λ
(⊥R)
Γ; ∆ ⊢ x().P :: Λ, x : ⊥

Γ; x : ⊥ ⊢ x⟨⟩.0 :: ·

(⊥L)

Γ; ∆ ⊢ P :: Λ, y : A
Γ; ∆′ ⊢ Q :: Λ′ , x : B ∗
( ⊗R)
Γ; ∆, ∆′ ⊢ (νy)x⟨y⟩.(P | Q) :: Λ, Λ′ , x : A ⊗ B
Γ; ∆, y : A, x : B ⊢ P :: Λ
(∗ ⊗L)
Γ; ∆, x : A ⊗ B ⊢ x(y).P :: Λ
Γ; ∆ ⊢ P :: Λ, x : B, y : A
( R)
Γ; ∆ ⊢ x(y).P :: Λ, x : A B
&

&

Γ; ∆, y : A ⊢ P :: Λ
Γ; ∆′ , x : B ⊢ Q :: Λ′
( L)
Γ; ∆, ∆′ , x : A B ⊢ (νy)x⟨y⟩.(P | Q) :: Λ, Λ′
&

&

Γ; ∆, y : A ⊢ P :: Λ, x : B
(∗ ⊸R)
Γ; ∆ ⊢ x(y).P :: Λ, x : A ⊸ B
Γ; ∆ ⊢ P :: Λ, y : A
Γ; ∆′ , x : B ⊢ Q :: Λ′ ∗
( ⊸L)
Γ; ∆, ∆′ , x : A ⊸ B ⊢ (νy)x⟨y⟩.(P | Q) :: Λ, Λ′
Γ; · ⊢ P :: y : A
(∗ !R)
Γ; · ⊢!x(y).P :: x : !A
Γ, u : A; ∆ ⊢ P :: Λ
(?R)
Γ; ∆ ⊢ P{x/u} :: Λ, x : ?A⊥

Γ, u : A; ∆ ⊢ P :: Λ
(∗ !L)
Γ; ∆, x : !A ⊢ P{x/u} :: Λ
Γ; y : A ⊢ P :: ·
(?L)
Γ; x : ?A ⊢!x(y).P :: ·

Figure 1: The ULL inference rules / type system

## PDF page 6

6

Session Type Systems based on Linear Logic: Classical versus Intuitionistic
Explicit closing
πCLL [4]
CP [18]
πCLLCP

No
Yes
Yes

Separate
unrestricted context
Yes
No
Yes

Identity as
forwarding
No
Yes
Yes

Table 2: Feature comparison of three session type interpretations of classical linear logic
Theorem 2.1. If Γ; ∆ ⊢ P :: Λ and P → Q, then Γ; ∆ ⊢ Q :: Λ.
Proof (sketch). By induction on the structure of the proof of P, using cut reduction.
Definition 2.6. For any process P, live(P) if and only if there are processes Q and R and channels ñ such
that P ≡ (ν ñ)(π.Q | R), where π ∈ {x⟨y⟩, x(y), x⟨⟩, x()}.
Theorem 2.2. If ·; · ⊢ P :: · and live(P), then there exists Q such that P → Q.
Proof (sketch). The liveness assumption tells us that P is a parallel composition of a process Q that is
guarded by some non-persistent communication π and some other process R. The fact that P’s proof has
an empty context allows us to infer that π.Q and R must have been composed using a C UT rule and that R
must be guarded by a prefix that is dual to π. Therefore, a reduction can take place.

3

Comparing Expressivity through United Linear Logic

πULL is a suitable framework for a rigorous comparison of the expressivity of session type systems based
on linear logic. In this section, we compare the class of processes typable in πULL to the classes of
processes typable in a classical and intuitionistic interpretation of linear logic. For this comparison to be
fair, the differences between these classes need to come only from typing, so the process languages need
to be the same. This means that our classical and intuitionistic interpretations need to type process terms
as given in the previous section, with the same features as those in πULL: explicit closing, a separate
unrestricted context, and identity as forwarding.
Our intuitionistic and classical session type interpretations of linear logic are denoted πILL and
πCLLCP , respectively. Their respective rules are given in Figure 2 and Figure 3. πILL is based on the
work by Caires, Pfenning and Toninho [3].
It is worth noticing that, because of the features we require for our type systems, we could not directly
base our classical interpretation on πCLL by Caires, Pfenning and Toninho [4] nor on Wadler’s CP [18].
Therefore, we have designed πCLLCP as a combination of features from πCLL and CP. Table 2 compares
these features in πCLL, CP and πCLLCP ; the differences are merely superficial:
• Explicit closing of sessions concerns a non-silent interpretation of 1 and ⊥ in the logic that entails
a reduction on processes (which, in turn, corresponds to cut reduction). In contrast, implicit closing
is due to a silent interpretation and corresponds to (structural) congruences in processes.
• Sequents with a separate unrestricted context are of the form P ⊢ Γ; ∆, which can also be written as
P ⊢ ∆, Γ′ where Γ′ contains only types of the form !A.
• The identity axiom can be interpreted as the forwarding process, which enables to account for
polymorphism. The forwarding process, however, is not usually present in session π-calculi.

## PDF page 7

B. van den Heuvel, J.A. Pérez

7

Γ; x : A ⊢ILL [x ↔ y] :: y : A

Γ, u : A; ∆, x : A ⊢ILL P :: z : C
(C OPY)
Γ, u : A; ∆ ⊢ILL (νx)u⟨x⟩.P :: z : C

(I D)

Γ; ∆ ⊢ILL P :: x : A
Γ; ∆′ , x : A ⊢ILL Q :: z : C
(C UT)
Γ; ∆, ∆′ ⊢ILL (νx)(P | Q) :: z : C
Γ; · ⊢ILL P :: x : A
Γ, u : A; ∆ ⊢ILL Q :: z : C
(C UT! )
Γ; ∆ ⊢ILL (νu)(!u(x).P | Q) :: z : C
Γ; ∆ ⊢ILL P :: z : C
(1 L)
Γ; ∆, x : 1 ⊢ILL x().P :: z : Z

(11 R)

Γ; · ⊢ILL x⟨⟩.0 :: x : 1

Γ; ∆ ⊢ILL P :: y : A
Γ; ∆′ ⊢ILL Q :: x : B
(⊗R)
Γ; ∆, ∆′ ⊢ILL (νy)x⟨y⟩.(P | Q) :: x : A ⊗ B

Γ; ∆, y : A, x : B ⊢ILL P :: z : C
(⊗L)
Γ; ∆, x : A ⊗ B ⊢ILL x(y).P :: z : C

Γ; ∆ ⊢ILL P :: y : A
Γ; ∆′ , x : B ⊢ILL Q :: z : C
(⊸L)
Γ; ∆, ∆′ , x : A ⊸ B ⊢ILL (νy)x⟨y⟩.(P | Q) :: z : C
Γ, u : A; ∆ ⊢ILL P :: z : C
(!L)
Γ; ∆, x : !A ⊢ILL P{x/u} :: z : C

Γ; ∆, y : A ⊢ILL P :: x : B
(⊸R)
Γ; ∆ ⊢ILL x(y).P :: x : A ⊸ B
Γ; · ⊢ILL P :: y : A
(!R)
Γ; · ⊢ILL !x(y).P :: x : !A

Figure 2: The πILL type system

[x ↔ y] ⊢CLL Γ; x : A, y : A⊥

P ⊢CLL Γ, u : A; ∆, y : A
(C OPY)
(νy)u⟨y⟩.P ⊢CLL Γ, u : A; ∆

(I D)

Q ⊢CLL Γ; ∆′ , x : A⊥
(C UT)
(νx)(P | Q)

P ⊢CLL Γ; ∆, x : A

P ⊢CLL Γ; x : A⊥
Q ⊢CLL Γ, u : A; ∆
(C UT? )
(νu)(!u(x).P | Q) ⊢CLL Γ; ∆
P ⊢CLL Γ; ∆
(⊥)
x().P ⊢CLL Γ; ∆, x : ⊥

x⟨⟩.0 ⊢CLL Γ; x : 1

(11)

P ⊢CLL Γ; ∆, y : A
Q ⊢CLL Γ; ∆′ , x : B
(⊗)
(νy)x⟨y⟩.(P | Q) ⊢CLL Γ; ∆, ∆′ , x : A ⊗ B

P ⊢CLL Γ; ∆, y : A, x : B
( )
x(y).P ⊢CLL Γ; ∆, x : A B

P ⊢CLL Γ, u : A; ∆
(?)
P{x/u} ⊢CLL Γ; ∆, x : ?A

P ⊢CLL Γ; y : A
(!)
!x(y).P ⊢CLL Γ; x : !A

&

&

Figure 3: The πCLLCP type system

## PDF page 8

8

Session Type Systems based on Linear Logic: Classical versus Intuitionistic

Judgments. Before we study the expressivity of these three systems, it is important to take note of the
difference in the forms of their typing judgments. For πULL, πCLLCP , and πILL, respectively, they are as
follows:
P ⊢CLL Γ; ∆
Γ; ∆ ⊢ILL x : A
Γ; ∆ ⊢ P :: Λ
CP
πCLL has one-sided sequents, whereas πILL has two-sided sequents (like πULL), but with exactly one
channel/type pair on the right of the turnstile. Compare, for example, πCLLCP ’s inference rule for ⊗ and
the ⊗R rules for πILL and πULL (see Figure 1):
Γ; ∆ ⊢ILL P :: y : A
Γ; ∆′ ⊢ILL Q :: x : B
P ⊢CLL Γ; ∆, y : A
Q ⊢CLL Γ; ∆′ , x : B
(⊗)
(⊗R)
(νy)x⟨y⟩.(P | Q) ⊢CLL Γ; ∆, ∆′ , x : A ⊗ B
Γ; ∆, ∆′ ⊢ILL (νy)x⟨y⟩.(P | Q) :: x : A ⊗ B
Locality. Locality is a well-known principle in concurrency research [13]. The idea is that freshly
created channels are local. Local channels are modifiable, in the sense that they can be used for inputs.
Once a channel has been transmitted to another location, it becomes non-local, and thus immutable: it
can only be used for outputs—inputs are no longer allowed. This makes locality particularly relevant for
giving formal semantics to distributed programming languages; a prime example is the join calculus [6],
whose theory relies on (and is deeply influenced by) the locality principle [7].
πILL guarantees locality for shared channels: a server can be defined using a replicated input, so the
channel on which this server would be provided cannot be received earlier in the process. Consider the
following example, taken from [4]:
(νx)(x(y).!y(z).P | (νq)x⟨q⟩.Q)

Let us attempt to find a typing for P in this process using πILL. We can apply the cut rule to split the
parallel composition, of which the left component is x(y).!y(z).P. Now, there are two rules we can apply
(read bottom-up):
Γ; ∆, y : A, x : B ⊢ILL !y(z).P :: w : C
Γ; ∆, y : A ⊢ILL !y(z).P :: x : B
(⊗L)
(⊸R)
Γ; ∆, x : A ⊗ B ⊢ILL x(y).!y(z).P :: w : C
Γ; ∆ ⊢ILL x(y).!y(z).P :: x : A ⊸ B
In both cases, the received channel y ends up on the left of the turnstile. There are no rules in πILL to
define a service on a channel on the left and there is no way to move the channel to the right. Hence, we
cannot find a typing for P in πILL. In contrast, this process can be typed in πCLLCP as follows, given
P′ ⊢CLL Γ, u : B; z : A
P = P′ {x/u}:
(!)
!y(z).P′ ⊢CLL Γ, u : B; y : !A
(?)
!y(z).P ⊢CLL Γ; y : !A, x : ?B
( )
x(y).!y(z).P ⊢CLL Γ; x : (!A) (?B)
&

&

Symmetry. The rely-guarantee distinction of πILL is what makes it enforce locality for shared channels.
The distinction is visible in πILL’s distinction between left and right in its judgments. Despite the twosidedness of its sequents, πULL can also type non-local processes. This is due to the full symmetry in the
inference rules: anything that can be done on the left of the turnstile can be done on the right. As we will
show formally in the rest of this section, this symmetry corresponds to the single-sidedness of πCLLCP :
πULL and πCLLCP can type exactly the same processes. We will also show formally that πULL, and thus
πCLLCP , can type more processes than πILL, because of the restriction of the right side of the turnstile to
exactly one channel/type pair, making πILL an asymmetrical typing system.

## PDF page 9

B. van den Heuvel, J.A. Pérez

9

Formal results. Our formal results rely on the sets of processes typable in the three typing systems,
given in Definition 3.1.
Definition 3.1. Let P denote the set of all processes induced by Definition 2.3. Then
U = {P ∈ P | ∃Γ, ∆, Λ such that Γ; ∆ ⊢ P :: Λ},
C = {P ∈ P | ∃Γ, ∆ such that P ⊢CLL Γ; ∆},
I = {P ∈ P | ∃Γ, ∆, x ∈ fn(P), A such that Γ; ∆ ⊢ILL P :: x : A}.
Our first observation is that all πULL-typable processes are πCLLCP -typable. Moreover, the reverse
is true as well. For the latter fact we need to convert a typing inference with one-sided sequents to
a two-sided system, which means that we need the ability to control the side of the turnstile specific
propositions end up on. This is taken care of by Lemma 3.1, which is an extension of [4, Prop.5.1, p.19] to
include exponential types (! and ?). The main result, Theorem 3.2, is that πCLLCP and πULL type exactly
the same processes.
Lemma 3.1. For any typing contexts Γ, ∆, Λ, Π and process P such that Γ; ∆ ⊢ P :: Λ, Π, we have
Γ; ∆, Π⊥ ⊢ P :: Λ.
Proof (sketch). By induction on the structure of the type inference tree. If the last inferred proposition is
to be moved to the left, after type inversion, the appropriate left rule can be used where a right rule was
used. Other propositions can be moved using the induction hypothesis.
Theorem 3.2. U = C.
Proof (sketch). There are two things to prove: (i) U ⊆ C, and (ii) C ⊆ U. (i) can be proven by induction
on the structure of the typing inferences. The idea is that for every rule of πULL there is an analogous
rule in πCLLCP . As for (ii), for any P such that P ⊢CLL Γ; ∆, it suffices to show that there are ∆L , ∆R = ∆
such that Γ⊥ , (∆L )⊥ ⊢ P :: ∆R . This can be done by induction on the structure of the typing inference of P.
After type inversion, the induction hypothesis can be used, which moves channel/type pairs to either side
of the turnstile. This results in many subcases, each of which can be solved with appropriate applications
of πULL rule analogous to the last used πCLLCP rule, using Lemma 3.1 in some cases.
The comparison between πULL and πILL can be done similarly. However, it is more interesting to
examine the set of inference rules. If we restrict all sequents in a πULL typing inference to have exactly
one channel/type on the right of the turnstile, we end up with a subset of usable inference rules: those
marked with an ‘∗’ in Figure 1. Upon further examination, we see that this set of rules coincides exactly
with the set of inference rules for πILL. The consequence is that πULL can type all πILL-typable processes.
Finally, any πULL/πCLLCP -typable process violating the locality principle suffices to show the second
main result, Theorem 3.3: πILL is less expressive than πULL. An important corollary of Theorem 3.2 and
Theorem 3.3 is that πILL is less expressive than πCLLCP , confirming the observation by Caires, Pfenning,
and Toninho [4].
Definition 3.2 (r-degree). The size of the right side of a πULL sequent is the sequent’s r-degree. Given
contexts Γ, ∆, Λ and process P, the ULL sequent Γ; ∆ ⊢ P :: Λ has r-degree |Λ|.

## PDF page 10

10

Session Type Systems based on Linear Logic: Classical versus Intuitionistic

Theorem 3.3. I ⊂ U.
Proof (sketch). Let
U∗ := {P ∈ U | ∃Γ, ∆, A s.t. Γ; ∆ ⊢ P :: x : A with a proof tree containing only sequents of r-degree 1}.
By induction on the structure of the typing inference, it can be shown that all processes in U∗ have typing
inferences using only those rules in Figure 1 marked with an ∗. It follows by contradiction that the
last applied rule cannot be without an ∗, and the usage of ∗-marked rules in the rest of the inference
follows from the induction hypothesis. The ∗-marked rules with r-degree 1 coincide exactly with the
typing inference rules of πILL, and so it follows that I = U∗ . Clearly, U∗ is a subset of U. Now, given
u : B; · ⊢ P :: z : A, there are several ways to type the process x(y).!y(z).P in πULL, but all of them use
sequents of r-degree different from 1, so it is not in U∗ . Hence, U∗ ⊂ U, confirming the thesis.

4

Conclusion

Using Girard’s Logic of Unity [9] as a basis, we have developed United Linear Logic as a means to
formally compare the session type systems derived from concurrent interpretations of classical and
intuitionistic linear logic. Much as Logic of Unity is a logic that encompasses classical, intuitionistic and
linear logic, the session type system interpretation of ULL (dubbed πULL), can type all πCLLCP - and
πILL-typable processes. This allows us to compare type systems based on different linear logics.
In πILL, judgments distinguish between several channels whose behavior is being relied on (on the
left of the judgment) and a single behavior provided along a designated channel (on the right). To retain
this rely-guarantee reading, πULL uses two-sided sequents in its typing inferences. However, πULL does
not distinguish between the sides of its sequents; it is fully symmetrical. This symmetry allows it to mimic
the single-sidedness of πCLLCP ’s sequents: placing a mirror besides πCLLCP ’s inference rules reveals
the inference rules of πULL. Similarly, πILL can be recovered from πULL by restricting the right side of
its sequents to exactly one channel. Not all inference rules remain usable, resulting in an asymmetrical
system that coincides exactly with πILL.
Our results formally corroborate the observation by Caires, Pfenning and Toninho: the difference
between session type systems based on classical and intuitionistic linear logic is in the enforcement
of locality [4]. πCLLCP is able to type non-local processes, because it does not distinguish between
linear channels, received or not, because of its single-sided sequents. Similarly, πULL can type non-local
processes because of its symmetry. Restricting πULL into πILL removes exactly those rules needed to
violate the locality principle. This reveals that πILL respects locality because of its asymmetry.
Acknowledgements. We are grateful to Joseph Paulus for initial discussions. We would also like to
thank the anonymous reviewers for their suggestions, which were helpful to improve the presentation.

References
[1] Andrew Barber & Gordon D. Plotkin (1996): Dual Intuitionistic Linear Logic. Technical Report ECS-LFCS96-347, University of Edinburgh, School of Informatics, Laboratory for Foundations of Computer Science,
Edinburgh.
[2] Luís Caires & Frank Pfenning (2010): Session Types as Intuitionistic Linear Propositions. In Paul Gastin &
François Laroussinie, editors: CONCUR 2010 - Concurrency Theory, Lecture Notes in Computer Science,
Springer Berlin Heidelberg, pp. 222–236, doi:10.1007/978-3-642-15375-4_16.

## PDF page 11

B. van den Heuvel, J.A. Pérez

11

[3] Luís Caires, Frank Pfenning & Bernardo Toninho (2012): Towards Concurrent Type Theory. In: Proceedings
of the 8th ACM SIGPLAN Workshop on Types in Language Design and Implementation, ACM, pp. 1–12,
doi:10.1145/2103786.2103788.
[4] Luís Caires, Frank Pfenning & Bernardo Toninho (2016): Linear Logic Propositions as Session Types.
Mathematical Structures in Computer Science 26(3), pp. 367–423, doi:10.1017/S0960129514000218.
[5] Bor-Yuh Evan Chang, Kaustuv Chaudhuri & Frank Pfenning (2003): A Judgmental Analysis of Linear
Logic. Technical Report CMU-CS-03-131R, Department of Computer Science, Carnegie Mellon University,
doi:10.1184/R1/6587498.v1.
[6] Cédric Fournet, Georges Gonthier, Jean-Jacques Levy, Luc Maranget & Didier Rémy (1996): A Calculus of
Mobile Agents. In Ugo Montanari & Vladimiro Sassone, editors: CONCUR ’96: Concurrency Theory, Lecture
Notes in Computer Science, Springer, Berlin, Heidelberg, pp. 406–421, doi:10.1007/3-540-61604-7_67.
[7] Cédric Fournet & Cosimo Laneve (2001): Bisimulations in the Join-Calculus. Theoretical Computer Science
266(1), pp. 569–603, doi:10.1016/S0304-3975(00)00283-8.
[8] Jean-Yves Girard (1987): Linear Logic. Theoretical Computer Science 50(1), pp. 1–101, doi:10.1016/03043975(87)90045-4.
[9] Jean-Yves Girard (1993): On the Unity of Logic. Annals of Pure and Applied Logic 59(3), pp. 201–217,
doi:10.1016/0168-0072(93)90093-S.
[10] Kohei Honda (1993): Types for Dyadic Interaction. In Eike Best, editor: CONCUR’93, Springer Berlin
Heidelberg, Berlin, Heidelberg, pp. 509–523, doi:10.1007/3-540-57208-2_35.
[11] Kohei Honda, Vasco T. Vasconcelos & Makoto Kubo (1998): Language Primitives and Type Discipline for
Structured Communication-Based Programming. In Chris Hankin, editor: Programming Languages and
Systems, Springer Berlin Heidelberg, Berlin, Heidelberg, pp. 122–138, doi:10.1007/BFb0053567.
[12] Olivier Laurent (2018): Around Classical and Intuitionistic Linear Logics. In: Proceedings of the 33rd
Annual ACM/IEEE Symposium on Logic in Computer Science, LICS ’18, ACM, Oxford, United Kingdom,
pp. 629–638, doi:10.1145/3209108.3209132.
[13] Massimo Merro (2000): Locality and Polyadicity in Asynchronous Name-Passing Calculi. In Jerzy Tiuryn,
editor: Foundations of Software Science and Computation Structures, Lecture Notes in Computer Science,
Springer, Berlin, Heidelberg, pp. 238–251, doi:10.1007/3-540-46432-8_16.
[14] Massimo Merro & Davide Sangiorgi (2004): On Asynchrony in Name-Passing Calculi. Mathematical
Structures in Computer Science 14(5), pp. 715–767, doi:10.1017/S0960129504004323.
[15] Robin Milner, Joachim Parrow & David Walker (1992): A Calculus of Mobile Processes, I. Information and
Computation 100(1), pp. 1–40, doi:10.1016/0890-5401(92)90008-4.
[16] Davide Sangiorgi & David Walker (2003): The Pi-Calculus: A Theory of Mobile Processes. Cambridge
University Press.
[17] Kaku Takeuchi, Kohei Honda & Makoto Kubo (1994): An Interaction-Based Language and Its Typing System.
In Costas Halatsis, Dimitrios Maritsas, George Philokyprou & Sergios Theodoridis, editors: PARLE’94
Parallel Architectures and Languages Europe, Springer Berlin Heidelberg, Berlin, Heidelberg, pp. 398–413,
doi:10.1007/3-540-58184-7_118.
[18] Philip Wadler (2012): Propositions As Sessions. In: Proceedings of the 17th ACM SIGPLAN International Conference on Functional Programming, ICFP ’12, ACM, Copenhagen, Denmark, pp. 273–286,
doi:10.1145/2364527.2364568.
