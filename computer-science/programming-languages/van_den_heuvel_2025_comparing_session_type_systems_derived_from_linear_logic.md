Source: https://doi.org/10.1016/j.jlamp.2024.101004
PDF sha256: 5d1c76234eb4f6f19f0ed555c24bfb19ab0a8ea7af9a121248f894c9ba6a8823
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of van_den_heuvel_2025_comparing_session_type_systems_derived_from_linear_logic.pdf

Transcription of `van_den_heuvel_2025_comparing_session_type_systems_derived_from_linear_logic.pdf` in this directory, 26 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-26 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

J. Log. Algebraic Methods Program. 142 (2025) 101004

Contents lists available at ScienceDirect

Journal of Logical and Algebraic Methods in
Programming
journal homepage: www.elsevier.com/locate/jlamp

Comparing session type systems derived from linear logic ✩
Bas van den Heuvel a,b,∗ , Jorge A. Pérez c,∗
a

HKA Karlsruhe, Karlsruhe, Germany
University of Freiburg, Freiburg, Germany
c
University of Groningen, Groningen, the Netherlands
b

A R T I C L E
Keywords:
Concurrency
Linear logic
𝜋 -calculus
Session types

I N F O

A B S T R A C T
Session types are a typed approach to message-passing concurrency, where types describe
sequences of intended exchanges over channels. Session type systems have been given strong
logical foundations via Curry-Howard correspondences with linear logic, a resource-aware logic
that naturally captures structured interactions. These logical foundations provide an elegant
framework to specify and (statically) verify message-passing processes.
In this paper, we rigorously compare diﬀerent type systems for concurrency derived from the
Curry-Howard correspondence between linear logic and session types. We address the main divide
between these type systems: the classical and intuitionistic presentations of linear logic. Over the
years, these presentations have given rise to separate research strands on logical foundations
for concurrency; the diﬀerences between their derived type systems have only been addressed
informally.
To formally assess these diﬀerences, we develop 𝜋𝖴𝖫𝖫, a session type system that encompasses
type systems derived from classical and intuitionistic interpretations of linear logic. Based on
a fragment of Girard’s Logic of Unity, 𝜋𝖴𝖫𝖫 provides a basic reference framework: we compare
existing session type systems by characterizing fragments of 𝜋𝖴𝖫𝖫 that coincide with classical and
intuitionistic formulations. We analyze the signiﬁcance of our characterizations by considering the
locality principle (enforced by intuitionistic interpretations but not by classical ones) and forms of
process composition induced by the interpretations.

1. Introduction
Establishing the correctness of message-passing programs is a central but challenging problem. Within formal methods for concurrency, session types [28,52,33] are now a consolidated approach to statically verifying safety and liveness properties of communicating
programs. Session types specify communication over channels as sequences of exchanges. This way, e.g., the session type !𝗂𝗇𝗍.?𝖻𝗈𝗈𝗅.𝖾𝗇𝖽
describes a channel’s intended protocol: send an integer, receive a boolean, and close the channel. Due to its simplicity and expressiveness, the 𝜋 -calculus [41,50]—the paradigmatic model of concurrency and interaction—is a widely used speciﬁcation language
for developing session types and establishing their basic theory. In this paper, we are interested in developing further the logical
foundations of session type systems for the 𝜋 -calculus.

✩

Work partially supported by the Dutch Research Council (NWO) under the VIDI Project No. 016.Vidi.189.046 (Unifying Correctness for Communicating Software).
* Corresponding authors.
E-mail addresses: vdheuvel@informatik.uni-freiburg.de (B. van den Heuvel), j.a.perez@rug.nl (J.A. Pérez).

https://doi.org/10.1016/j.jlamp.2024.101004
Received 26 January 2024; Received in revised form 18 July 2024; Accepted 10 August 2024
Available online 22 August 2024
2352-2208/© 2024 The Author(s).
Published by Elsevier Inc.
(http://creativecommons.org/licenses/by/4.0/).

This is an open access article under the CC BY license

## PDF page 2

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Context: linear logic and session types In a line of work developed by Caires, Pfenning, Wadler, and several others, the theory of
session types has been given ﬁrm logical foundations in the form of Curry-Howard-style correspondences. Caires and Pfenning [7]
discovered a correspondence between session types for the 𝜋 -calculus and Girard’s linear logic [23]:

⇔
⇔
⇔

session types

𝜋 -calculus processes
process communication

logical propositions
proofs
cut elimination

Based on this logical bridge, the resulting type systems simultaneously ensure important properties for processes, such as session ﬁdelity
(processes respect session types), communication safety (absence of communication errors), and progress/deadlock freedom (processes
never reach stuck states).
There are two presentations of linear logic, classical and intuitionistic, and session type systems derived from linear logic have
inherited this dichotomy. Under Curry-Howard interpretations, typing judgments and typing rules correspond to the logical sequents
and inference rules of the underlying linear logic. In both classical and intuitionistic cases, judgments assign independent session
protocols to the channels of a process. Because these judgments diﬀer between the presentations of linear logic, there are consequences
for their respective interpretations as type systems:
• Caires and Pfenning’s correspondence [7] uses an intuitionistic linear logic where judgments for process are two-sided, with zero
or many channels on the left and exactly one channel on the right. Such judgments have a convenient rely-guarantee reading:
the process relies on the behaviors described by the channels on the left to guarantee the behavior of the one channel on the right.
In this interpretation, each logical connective thus requires two rules: the right rule speciﬁes how to oﬀer a behavior, while the
left rule speciﬁes how to use a behavior.
• Wadler’s correspondence [56] uses classical linear logic, where judgments are single-sided (all channels appear on the right) and
lack a rely-guarantee reading. In this interpretation, there is only a single rule per logical connective, which makes such type
systems direct and economical.
Although the diﬀerences and relationship between intuitionistic and classical linear logic are relevant and well-known (see,
e.g., [49,6,38]), the diﬀerences between their derived session type systems have only been addressed informally. In particular, Caires
et al. [12] observe that, unlike classical interpretations, an intuitionistic interpretation guarantees locality for shared channels, i.e.,
the principle by which received channels cannot become servers (see Section 4.1). In the meantime, both interpretations have been
extended in multiple, exciting directions (see, e.g., [9,1,13,51,39,4,8,14,53,10,34,47,19,31,32]). This emergence of families of type
systems (one classical, one intuitionistic) has deepened the original dichotomy and somewhat obscured our understanding of logical
foundations of concurrency as a whole. This state of aﬀairs calls for a formal comparison between the session type systems derived
from classical and intuitionistic linear logics that goes beyond their superﬁcial diﬀerences. To us, this seems an indispensable step in
consolidating the logical foundations of message-passing concurrency.
Goal of the paper In this paper, we aim at formally comparing the session type systems derived from interpretations of intuitionistic
and classical linear logic. We are concerned with two families of type systems for the 𝜋 -calculus, which naturally induce two classes
of typable processes, namely those typable in intuitionistic and classical interpretations, respectively. These two classes are known
to largely overlap with each other; informal observations suggest that some processes are typable in a classical setting but not in an
intuitionistic setting. We are interested in determining precisely how these classes of processes relate to each other.
The key step in our approach is to deﬁne a basic framework of reference in which both type systems, intuitionistic and classical,
can be objectively compared. Girard’s Logic of Unity (LU) [24] has a similar goal: to objectively compare classical logic, intuitionistic
logic, and (classical and intuitionistic) linear logic in a single system, abstracting away from syntactical diﬀerences. It is then only
natural to use LU as a reference for our comparison. We develop 𝜋𝖴𝖫𝖫 , a session type system for the 𝜋 -calculus that subsumes classical
and intuitionistic interpretations of linear logic as session types. Based on a fragment of LU that suits our purposes (dubbed 𝖴𝖫𝖫),
the type system 𝜋𝖴𝖫𝖫 allows us to deﬁne a class of typable processes that contains processes typable in both the intuitionistic and
classical type systems.
In our approach, the type system 𝜋𝖴𝖫𝖫 provides an eﬀective framework and a yardstick for a formal comparison. Because its
typing rules encompass both classical and intuitionistic formulations, we can readily characterize their two (sub-)classes of typable
processes by considering the diﬀerent typing rules that apply in each case. Analyzing these diﬀerent portions of rules allows us to
then characterize the diﬀerences (in expressiveness/typability) between the intuitionistic and classical type systems. Moreover, these
characterizations allow us to determine how extensions to the type systems might be supported by the intuitionistic and classical
interpretations.
Contributions and outline Summing up, this paper makes the following contributions:
1. The session type system 𝜋𝖴𝖫𝖫, which is derived from a concurrent interpretation of 𝖴𝖫𝖫 (a linear fragment of LU), together with
its correctness results (Theorems 2.1 to 2.4, § 2);
2. A formal comparison between (i) the classes of processes typable under interpretations of intuitionistic and classical linear logic
and (ii) those typable in 𝜋𝖴𝖫𝖫 (§ 3). We prove that (1) 𝜋𝖴𝖫𝖫 precisely captures the class of processes typable under the classical
2

## PDF page 3

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

interpretation (Theorem 3.1), and that (2) the class of processes typable under the intuitionistic interpretation is strictly included
in 𝜋𝖴𝖫𝖫 (Theorem 3.3). Together, these two results conﬁrm the informal observation that the two interpretations induce diﬀerent
classes of processes.
3. An analysis of the signiﬁcance of our characterizations in terms of two diﬀerent aspects: the locality principle enforced by
intuitionistic interpretations, and process composition usually limited in type systems derived from linear logic in comparison to
session type systems not based on logical foundations (§ 4). This analysis corroborates and gives a formal footing to the informal
observation made in [12] concerning locality, and suitably extends it to show that intuitionistic interpretations cannot type
empty sends on previously received channels.
Finally, we draw some conclusions in Section 5.
Related work Our work can be seen as an expressiveness study on the classes of processes induced by diﬀerent type systems. Concretely, our results can be seen as providing formal evidence that session type systems derived from classical linear logic are more
expressive than those based on intuitionistic linear logic, based on the fact that the former are more permissive than the latter.
The study of the relative expressiveness of process calculi has a long, fruitful history (see, e.g. [26,45,43]). The aim is to compare
two diﬀerent process languages by deﬁning an encoding (a translation up to some correctness criteria) between them or by proving
its non-existence. Even though our aims are similar in spirit to expressiveness studies, at a technical level there are substantial
diﬀerences, because our focus is on assessing the inﬂuence that diﬀerent type systems have on the same process language—as such,
our comparisons do not rely on encodings.
Although most studies on relative expressiveness have addressed untyped process languages, some works have studied the inﬂuence
of (behavioral) types on the expressiveness of process languages—see, e.g., [16,22,15,37,44]. Salient examples are the works [18,46],
which compare type systems that enforce the deadlock-freedom and termination properties, respectively. In particular, a main result
in [18] is that (classical) linear logic induces a strict subclass of deadlock-free processes with respect to the class of typable processes
in non-logically motivated type systems. Unlike our work, the focus in [18] is on diﬀerent process languages, each with a diﬀerent
type system. This requires the deﬁnition of encodings, on processes but also on types, that abstract away from the syntactic diﬀerences
between the classes of processes induced by each typed framework.
This paper is an extended, revised version of the workshop paper [29]. We present several improvements and developments with
respect to that work. First, here we have signiﬁcantly improved the correctness results for 𝜋𝖴𝖫𝖫 (Theorems 2.1 to 2.4) and considered
branching/selection types (not studied in [29]). Also, we have reﬁned the presentation of 𝜋𝖴𝖫𝖫 in [29] with a more explicit treatment
of duality, presented in Section 2.3. Moreover, we have broadened the analysis of our comparison results in Section 4 by considering
extensions to the type system with more expressive forms of parallel composition and restriction.
2. A session type system based on LU
Girard [24] developed Logic of Unity (LU) to study and compare classical, intuitionistic, and linear logic, without having to
“change the rules of the game by, e.g., passing from one style of sequent to the other.” The idea is simple: there is one form of sequent
with an abundance of inference rules. The several logics subsumed by LU are then characterized by (possibly overlapping) subsets of
those rules.
Clearly, we ﬁnd ourselves in a similar situation: we want to compare intuitionistic and classical linear logic as session type systems,
by abstracting away from typing judgments and rules of diﬀerent forms. To this end, in this section we introduce United Linear Logic
(𝖴𝖫𝖫), a logic based on the linear fragment of LU, and present the Curry-Howard interpretation of 𝖴𝖫𝖫 as a session type system
for the 𝜋 -calculus, dubbed 𝜋𝖴𝖫𝖫, following [7,56] (§ 2.1). As we will see in Section 3, we can then characterize the session type
interpretations of intuitionistic and classical linear logic as subsets of the typing rules of 𝜋𝖴𝖫𝖫 . We also present correctness properties
common to (logically motivated) session type systems (§ 2.2). Finally, we discuss an alternative presentation of 𝜋𝖴𝖫𝖫 that has a more
explicit account of duality (§ 2.3).
2.1. The process calculus and type system
Propositions/types A session type represents a sequence of exchanges that should be performed along a channel. Propositions in
𝖴𝖫𝖫—interpreted as session types in 𝜋𝖴𝖫𝖫—are deﬁned as follows:
Deﬁnition 2.1. 𝖴𝖫𝖫 propositions/𝜋𝖴𝖫𝖫 types are generated by the following grammar:

𝐴, 𝐵 ∶∶= 𝟏 | ⊥ | 𝐴 ⊗ 𝐵 | 𝐴 ⊸ 𝐵 | ⊕{𝑖 ∶ 𝐴}𝑖∈𝐼 | &{𝑖 ∶ 𝐴}𝑖∈𝐼 | !𝐴 | ?𝐴
Table 1 gives the intuitive reading of the interpretation of propositions as session types. Some details are worth noting.
• First, receiving in 𝜋𝖴𝖫𝖫 is deﬁned using the intuitionistic connective ⊸; we will see later that ⊸ can be used to deﬁne the
classical connective —also interpreted as receiving—which is not supported by intuitionistic linear logic.

&

3

## PDF page 4

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Table 1
Interpretation of 𝖴𝖫𝖫 propositions as session types.

𝟏 and ⊥
𝐴⊗𝐵
𝐴⊸𝐵
⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼
&{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼
!𝐴
?𝐴

Close the channel
Send a channel of type 𝐴 and continue as 𝐵
Receive a channel of type 𝐴 and continue as 𝐵
Send a label 𝑖 ∈ 𝐼 and continue as 𝐴𝑖
Receive a label 𝑖 ∈ 𝐼 and continue as 𝐴𝑖
Repeatedly provide a service of type 𝐴
Connect to a service of type 𝐴

• Second, 𝜋𝖴𝖫𝖫 supports labeled 𝑛-ary branching constructs (following, e.g., Caires and Pérez in [8]). In linear logic, ⊕ and & are
binary connectives [23,25,24]. In [7,56], Caires, Pfenning, and Wadler originally interpret them as a choice between a left and
a right option. However, in session-typed 𝜋 -calculi (see, e.g., [33]) 𝑛-ary choice is standard and more convenient.
• Third, the syntax of formulas considered by Girard [24] subsumes our syntax for 𝖴𝖫𝖫 by including universal and existential
quantiﬁers and the units ⊤ and 𝟎. Our syntax does not include quantiﬁers and considers both 𝟏 and ⊥: while the interpretation
of intuitionistic linear logic by Caires and Pfenning includes 𝟏 (but not ⊤, 𝟎, or ⊥), the interpretation of classical linear logic by
Wadler considers quantiﬁers and the units 𝟏 and ⊥ (but not ⊤ or 𝟎).
Duality

The duality of 𝖴𝖫𝖫 propositions is deﬁned as follows:

Deﬁnition 2.2. Duality is a binary relation on propositions/types, denoted 𝐴⊥ , deﬁned as follows:

𝟏⊥ ∶= ⊥

(𝐴 ⊗ 𝐵)⊥ ∶= 𝐴 ⊸ 𝐵 ⊥

(⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 )⊥ ∶= &{𝑖 ∶ 𝐴⊥𝑖 }𝑖∈𝐼

(!𝐴)⊥ ∶= ?𝐴⊥

⊥⊥ ∶= 𝟏

(𝐴 ⊸ 𝐵)⊥ ∶= 𝐴 ⊗ 𝐵 ⊥

(&{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 )⊥ ∶= ⊕{𝑖 ∶ 𝐴⊥𝑖 }𝑖∈𝐼

(?𝐴)⊥ ∶= !𝐴⊥

Duality in 𝜋𝖴𝖫𝖫 reﬂects the intended reciprocity of protocols between two parties: when a process on one side of a channel sends,
the process on the opposite side must receive, and vice versa. It is easy to see that duality is an involution: (𝐴⊥ )⊥ = 𝐴.
As mentioned before, we can use duality to deﬁne in terms of ⊸: 𝐴 𝐵 ∶= 𝐴⊥ ⊸ 𝐵 ; as we will see, the rules for of classical
linear logic can be recovered from the rules for ⊸ in 𝖴𝖫𝖫 using duality. Duality also shows that ⊗ and are De Morgan-style duals
in classical linear logic:

&

&

&

&

&

(𝐴

&

(𝐴 ⊗ 𝐵)⊥ = 𝐴 ⊸ 𝐵 ⊥ = (𝐴⊥ )⊥ ⊸ 𝐵 ⊥ = 𝐴⊥

𝐵⊥

𝐵)⊥ = (𝐴⊥ ⊸ 𝐵)⊥ = 𝐴⊥ ⊗ 𝐵 ⊥

Processes The discipline of binary session types deals with concurrent processes that communicate through point-to-point channels.
The 𝜋 -calculus [41,50] oﬀers a rigorous yet expressive framework for deﬁning this discipline and establishing its fundamental properties. 𝜋𝖴𝖫𝖫 is a type system for 𝜋 -calculus processes deﬁned as follows:
Deﬁnition 2.3. Process terms are generated by the following grammar:

𝑃 , 𝑄 ∶∶= 𝟎 | (𝜈𝑥)𝑃 | 𝑃 | 𝑄 | 𝑥⟨𝑦⟩.𝑃 | 𝑥(𝑦).𝑃 | 𝑥 ⊲ 𝓁.𝑃 | 𝑥 ⊳ {𝑖 ∶ 𝑃 }𝑖∈𝐼

| !𝑥(𝑦).𝑃 | [𝑥 ↔ 𝑦] | 𝑥⟨⟩.𝑃 | 𝑥().𝑃
Process constructs for inaction 𝟎, channel restriction (𝜈𝑥)𝑃 , and parallel composition 𝑃 | 𝑄 have standard readings. The same
applies to constructs for sending, receiving, selection, branching, and replicated receive preﬁxes, which are respectively denoted
𝑥⟨𝑦⟩.𝑃 , 𝑥(𝑦).𝑃 , 𝑥 ⊲ 𝓁.𝑃 , 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 , and !𝑥(𝑦).𝑃 . Note that all these preﬁxes are blocking, which means that our process calculus
implements synchronous communication (see, e.g., [13,30,55] for interpretations of linear logic as session type systems in the asynchronous setting). Process [𝑥 ↔ 𝑦] denotes a forwarder that “fuses” channels 𝑥 and 𝑦; it is akin to the link processes used in encodings
of name passing using internal mobility [2].
We consider also constructs 𝑥⟨⟩.𝑃 and 𝑥().𝑃 , which specify the explicit closing of channels: their synchronization represents the
explicit deallocation of linear resources. We use these constructs to give a non-silent interpretation of 𝟏 and ⊥ (see § 3.1).
In (𝜈𝑦)𝑃 , 𝑥(𝑦).𝑃 , and !𝑥(𝑦).𝑃 the occurrence of 𝑦 is binding, with scope 𝑃 ; we say that 𝑦 is bound in 𝑃 . Non-bound occurrences
of names are considered free. We consistently adopt Barendregt’s naming convention: bound names are pairwise distinct and distinct
from free names. The sets of bound and free names of a process 𝑃 are denoted bn(𝑃 ) and fn(𝑃 ), respectively. We identify processes
up to consistent renaming of bound names, writing ≡𝛼 for this congruence. We write 𝑃 {𝑦∕𝑥} for the capture-avoiding substitution
of free occurrences of 𝑦 for 𝑥 in 𝑃 .
Structural congruence The following is an important notation of syntactical equivalence for 𝜋𝖴𝖫𝖫 processes.
4

## PDF page 5

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[cutAssocL]

𝑥 ∉ fn(𝑄)

[cutSymm]

(𝜈𝑥)(𝑃 | 𝑄) ≡ (𝜈𝑥)(𝑄 | 𝑃 )

𝑦 ∉ fn(𝑃 )

(𝜈𝑥)(𝑃 | (𝜈𝑦)(𝑄 | 𝑅)) ≡ (𝜈𝑦)(𝑄 | (𝜈𝑥)(𝑃 | 𝑅))

[cutAssocR]

𝑥 ∉ fn(𝑅)

𝑦 ∉ fn(𝑃 )

(𝜈𝑥)(𝑃 | (𝜈𝑦)(𝑄 | 𝑅)) ≡ (𝜈𝑦)((𝜈𝑥)(𝑃 | 𝑄) | 𝑅)
[𝛽 id]

[𝛽 close]

𝑥≠𝑦

(𝜈𝑥)(𝑃 | [𝑥 ↔ 𝑦]) → 𝑃 {𝑦∕𝑥}

(𝜈𝑥)(𝑥⟨⟩.𝟎 | 𝑥().𝑄) → 𝑄

[𝛽 send]

(𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.(𝑃1 | 𝑃2 ) | 𝑥(𝑧).𝑄) → (𝜈𝑥)(𝑃2 | (𝜈𝑦)(𝑃1 | 𝑄{𝑦∕𝑧}))
[𝛽 sel]

𝑗∈𝐼

(𝜈𝑥)(𝑥 ⊲ 𝑗.𝑃 | 𝑥 ⊳ {𝑖 ∶ 𝑄𝑖 }𝑖∈𝐼 ) → (𝜈𝑥)(𝑃 | 𝑄𝑗 )
[𝛽 serv]

[𝛽 weaken]
𝑥 ∉ fn(𝑃 )

(𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.𝑃 | !𝑥(𝑧).𝑄) → (𝜈𝑥)((𝜈𝑦)(𝑃 | 𝑄{𝑦∕𝑧}) | !𝑥(𝑧).𝑄)

(𝜈𝑥)(𝑃 | !𝑥(𝑧).𝑄) → 𝑃

[𝜅 close]

(𝜈𝑦)(𝑃 | 𝑥().𝑄) → 𝑥().(𝜈𝑦)(𝑃 | 𝑄)
[𝜅 sendR]

𝑦 ∈ fn(𝑄2 )

(𝜈𝑦)(𝑃 | (𝜈𝑧)𝑥⟨𝑧⟩.(𝑄1 | 𝑄2 )) → (𝜈𝑧)𝑥⟨𝑧⟩.(𝑄1 | (𝜈𝑦)(𝑃 | 𝑄2 ))
[𝜅 sendL]

𝑦 ∈ fn(𝑄1 )

(𝜈𝑦)(𝑃 | (𝜈𝑧)𝑥⟨𝑧⟩.(𝑄1 | 𝑄2 )) → (𝜈𝑧)𝑥⟨𝑧⟩.((𝜈𝑦)(𝑃 | 𝑄1 ) | 𝑄2 )
[𝜅 recv]

[𝜅 sel]

(𝜈𝑦)(𝑃 | 𝑥(𝑧).𝑄) → 𝑥(𝑧).(𝜈𝑦)(𝑃 | 𝑄)

(𝜈𝑦)(𝑃 | 𝑥 ⊲ 𝓁.𝑄) → 𝑥 ⊲ 𝓁.(𝜈𝑦)(𝑃 | 𝑄)

[𝜅 bra]

(𝜈𝑦)(𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 | 𝑄) → 𝑥 ⊳ {𝑖 ∶ (𝜈𝑦)(𝑃𝑖 | 𝑄)}𝑖∈𝐼
Fig. 1. Structural congruence and reduction for 𝜋𝖴𝖫𝖫.

Deﬁnition 2.4. Structural congruence is a binary relation on process terms, denoted 𝑃 ≡ 𝑄. It is deﬁned as the least congruence on
processes (i.e., closed under arbitrary process contexts) that satisﬁes the axioms in Fig. 1 (top).
The above formulation of structural congruence internalizes the conditions induced by typing (i.e., proof transformations in 𝖴𝖫𝖫),
necessary for the correctness properties proven in Section 2.2.
Computation As is usual for Curry-Howard correspondences, computation is related to cut reduction. Cuts are used in logic to combine
two proofs that contain dual propositions. As we will see, a cut in session type interpretations of linear logic entails the parallel
composition and connection of two processes. Generally, cut reduction transforms cuts into cuts on smaller types. In correspondences
between linear logic and session types, cut reduction corresponds to communication—the notion of computation in the 𝜋 -calculus,
which expresses internal behavior of processes.
The deﬁnition of the reduction relation follows. Note that, for a simpler presentation, it includes a set of rules for commuting
conversions (𝜅 -rules); an alternative presentation could treat commuting conversions as a behavioral equivalence.
Deﬁnition 2.5. Reduction is a binary relation on process terms, denoted 𝑃 → 𝑄, deﬁned in Fig. 1. It is closed under the following
rules:

𝑄 → 𝑄′
𝑃 | 𝑄 → 𝑃 | 𝑄′

[par]

𝑃 →𝑄
(𝜈𝑦)𝑃 → (𝜈𝑦)𝑄

[res]

𝑃 ≡ 𝑃′

𝑃 ′ → 𝑄′
𝑃 →𝑄

𝑄′ ≡ 𝑄

[sc]

We write →𝛽 to denote reductions that follow from 𝛽 -rules.
In this deﬁnition, Rule [𝛽 id] replaces a channel 𝑥 with a channel 𝑦 which 𝑥 is forwarded to. Rule [𝛽 close] formalizes the explicit
channel deallocation mentioned above: the synchronization between an empty send and an empty receive eﬀectively closes channel 𝑥.
5

## PDF page 6

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[idR]∗

[idL]

[𝟏R]∗

Γ; 𝑥 ∶ 𝐴 ⊢ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴

Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥ ⊢ [𝑥 ↔ 𝑦] ∶∶ ∅

Γ; ∅ ⊢ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏

[𝟏L]∗

[⊥R]

Γ; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ, 𝑥 ∶ 𝟏 ⊢ 𝑥().𝑃 ∶∶ Λ

[⊗R]∗

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴

[⊥L]

Γ; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ ⊢ 𝑥().𝑃 ∶∶ Λ, 𝑥 ∶ ⊥

Γ; 𝑥 ∶ ⊥ ⊢ 𝑥⟨⟩.𝟎 ∶∶ ∅
[⊗L]∗

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐵

Γ; Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵 ⊢ 𝑃 ∶∶ Λ

Γ; Δ, Δ′ ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵
&

&

[ L]

[ R]

Γ; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

&

Γ; Δ ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

𝐵

Γ; Δ, Δ′ , 𝑥 ∶ 𝐴

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴

Γ; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐵

Γ; Δ ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴 ⊸ 𝐵
Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴𝑗

Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢ 𝑄 ∶∶ Λ′

𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′

[⊸L]∗

[⊸R]∗

[⊕R]∗

&

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵

Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢ 𝑄 ∶∶ Λ′

Γ; Δ, Δ′ , 𝑥 ∶ 𝐴 ⊸ 𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′
[⊕L]∗

𝑗∈𝐼

Γ; Δ ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ Λ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼
[&R]∗

Γ; Δ, 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ

∀𝑖 ∈ 𝐼. Γ; Δ, 𝑥 ∶ 𝐴𝑖 ⊢ 𝑃𝑖 ∶∶ Λ

Γ; Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ Λ
[&L]∗

Γ; Δ, 𝑥 ∶ 𝐴𝑗 ⊢ 𝑃 ∶∶ Λ

∀𝑖 ∈ 𝐼. Γ; Δ ⊢ 𝑃𝑖 ∶∶ Λ, 𝑥 ∶ 𝐴𝑖

Γ; Δ ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ Λ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

𝑗∈𝐼

Γ; Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ Λ

[copyR]

[copyL]∗

[!R]∗

Γ, 𝑢 ∶ 𝐴; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐴

Γ, 𝑢 ∶ 𝐴; Δ ⊢ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

Γ, 𝑢 ∶ 𝐴; Δ ⊢ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

Γ; ∅ ⊢ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐴

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴⊥

[!L]∗

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ, 𝑥 ∶ !𝐴 ⊢ 𝑃 {𝑥∕𝑢} ∶∶ Λ

[?L]

[?R]

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ ⊢ 𝑃 {𝑥∕𝑢} ∶∶ Λ, 𝑥 ∶ ?𝐴⊥

Γ; 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ ∅

Γ; 𝑥 ∶ ?𝐴 ⊢ !𝑥(𝑦).𝑃 ∶∶ ∅

Fig. 2. The 𝜋𝖴𝖫𝖫 type system.

Rule [𝛽 send] formalizes the synchronization between a send and a corresponding receive, substituting the sent name for the received
name in the continuation of the receive. Rule [𝛽 sel] formalizes the synchronization between a selection and a branch. Rule [𝛽 serv]
allows to synchronize a client and a service; a copy of the service 𝑄 is spawned with the sent name substituted for the received name
while the replicated receive remains. Rule [𝛽 weaken] allows cleaning up a service if it has no clients.
The 𝜅 -rules reﬂect commuting conversions in linear logic, which in the process calculus allow pulling preﬁxes on free names out of
series of consecutive restrictions; as we will see, we use them such that we can state a general progress result.
Rules [par], [res], and [sc] close reduction under parallel composition, restriction and structural congruence, respectively (Definition 2.4).
Type checking The inference system of 𝖴𝖫𝖫 is a sequent calculus with sequents of the form Γ; Δ ⊢ Λ. Here, Γ, Δ and Λ denote regions
which collect propositions and obey diﬀerent structural criteria. Γ is the unrestricted region, which contains propositions that can be
indeﬁnitely used. Δ and Λ are the linear regions, which contain propositions that must be used exactly once. We write ‘∅’ to denote
an empty region. Also, we extend duality to regions: (Δ)⊥ contains exactly the duals of the propositions in Δ.
The type system for 𝜋𝖴𝖫𝖫 is an extension of 𝖴𝖫𝖫’s inference system with process and channel name annotations on sequents,
such that judgments are of the form Γ; Δ ⊢ 𝑃 ∶∶ Λ. Then, the regions Γ, Δ, and Λ denote the unrestricted resp. linear contexts of 𝑃 ,
consisting of assignments 𝑥 ∶ 𝐴 where 𝑥 is a channel name and 𝐴 is a proposition/type.
Figs. 2 and 3 give the typing rules of 𝜋𝖴𝖫𝖫, which are based directly on the linear fragment of LU in [24] (some rules are marked
with ∗, which we will refer to later).
We comment on the rules in Fig. 2. Axioms [idR] and [idL] type forwarding constructs which connect two channels of dual type.
Axioms [𝟏R] and [⊥L] type processes that close a session with an empty send after which they become inactive. Rules [⊥R] and [𝟏L]
type processes that close a session with an empty receive. These four rules deﬁne a non-silent interpretation for 𝟏 and ⊥ that entails
process communication (cf. Deﬁnition 2.5), which corresponds to cut reductions in proofs. (An alternative silent interpretation of 𝟏
and ⊥ is discussed in Section 4.2.1.)
The typing system elegantly induces processes under the internal mobility discipline, whereby only fresh channels are exchanged
in communications [48,2]. Rules [⊗R], [ L], and [⊸L] type bound sends, where one process provides the sent channel and another
independent process provides the continuation channel. Rules [⊗L], [ R], and [⊸R] type receive-preﬁxed processes. Rules [⊕R]
and [&L] type selection and rules [⊕L] and [&R] type branching.

&

&

6

## PDF page 7

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[cutRL]∗

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

[cutRR]

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

[cutLR]∗

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

Γ; Δ′ , 𝑥 ∶ 𝐴 ⊢ 𝑄 ∶∶ Λ′

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ
′

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐴

Γ; Δ, Δ′ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

′

[cutLL]

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐴⊥

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

Γ; Δ, Δ′ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

Γ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢ 𝑄 ∶∶ Λ′

Γ; Δ, Δ′ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

[cut!R]∗

[cut!L]∗

[cut?R]

[cut?L]

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ
Γ; ∅ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐴
Γ; Δ ⊢ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴
Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑄 ∶∶ Λ
Γ; Δ ⊢ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ
Γ; 𝑥 ∶ 𝐴⊥ ⊢ 𝑄 ∶∶ ∅
Γ; Δ ⊢ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

Γ; 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ∶∶ ∅
Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑄 ∶∶ Λ
Γ; Δ ⊢ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

Fig. 3. Cut-rules of the 𝜋𝖴𝖫𝖫 type system.

Our interpretation of !𝐴 and ?𝐴 as server and client behaviors follows the interpretation of classical linear logic in [12].
Rules [copyR] and [copyL] type clients that connect to a service by sending a fresh channel. Rules [!R] and [?L] allow the typing of unused services and Rules [!L] and [?R] allow adding unused services to the unrestricted context.
Fig. 3 gives a series of so-called cut-rules, that type channel connections. The number and shape of these rules is a diﬀerence with
respect to previous presentations. Rules [cutRL], [cutLR], [cutLL], and [cutRR] type pairs of processes that have a channel of
dual type in common by composing them in parallel and immediately binding their common channel. The four similar rules provide
for all possible sides the cut channel can appear on. This way, constructs for restriction and parallel composition are jointly treated.
Rules [cut!R], [cut!L], [cut?R], and [cut?R] type the connection of a service provider with potential clients; a process 𝑄 with
potential clients has a channel 𝑢 in its unrestricted context, so the rules create a service from a process 𝑃 that has a single channel 𝑥
of type dual to 𝑢’s type by preﬁxing it with replicated reception on 𝑢 (forming !𝑢(𝑥).𝑃 ) and then composing this process in parallel
with 𝑄 and binding 𝑢.
This abundance of cut-rules is derived from the generality of 𝖴𝖫𝖫 ’s judgments and necessary for proving the correctness results
presented in Section 2.2. In Section 2.3 we shall consider an alternative presentation of 𝜋𝖴𝖫𝖫 , which allows moving channels between
the left- and right-hand regions of typing judgments using duality; as we will see, in such a presentation we will be able to drastically
cut down the number of cut-rules.
Diﬀerences with LU As already mentioned, for the purposes of our formal comparison we consider a linear logic derived from LU [24]
restricted to linear connectives. The following are notable diﬀerences between our linear logic and the linear fragment of LU:
• we include a Rule [idL] which is complementary to [idR];
• we include Rules [𝟏L] and [⊥R] which are lacking in LU;
• we omit rules for ⊤ and 𝟎 (the units of & and ⊕, resp.), which are usually disregarded in session type interpretations of linear
logic (an exception is [31], which uses ⊤ and 𝟎 to give a logical account of subtyping);
• we omit rules that move propositions between the left and right linear regions using duality (in Section 2.3 we will return to
these rules);
• because the order of assumptions in typing rules makes a practical diﬀerence, we include additional symmetric cut-rules.
2.2. Correctness properties
Session type systems for the 𝜋 -calculus derived from the Curry-Howard correspondence enforce strong correctness properties for
processes, which follow directly from properties of the logic, in particular from cut elimination. This is no diﬀerent for 𝜋𝖴𝖫𝖫 . Our
ﬁrst result is the safety property of subject congruence and reduction (Theorems 2.1 and 2.2), which says that typability is consistent
across structural congruence and reductions.
Theorem 2.1 (Subject congruence). If Γ; Δ ⊢ 𝑃 ∶∶ Λ and 𝑃 ≡ 𝑄, then Γ; Δ ⊢ 𝑄 ∶∶ Λ.
Proof (Sketch). By induction on the derivation of the structural congruence. The only inductive case is the closure under arbitrary
process contexts, which follows from the IH directly. The base cases correspond to a rule in Fig. 1 (top). In each case, we infer the
typing of 𝑃 and 𝑄 from the shapes of the processes in the rule, and show that these typing inferences have identical assumptions
and conclusion. The cases of Rules [cutAssocL] and [cutAssocR] are straightforward as usual. The analysis of the more interesting
case of Rule [cutSymm] depends on the last-applied cut-rule. If the left-hand side uses, e.g., Rule [cutLR], then the right-hand side
should use Rule [cutRL]. □
Theorem 2.2 (Subject reduction). If Γ; Δ ⊢ 𝑃 ∶∶ Λ and 𝑃 → 𝑄, then Γ; Δ ⊢ 𝑄 ∶∶ Λ.
7

## PDF page 8

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Proof (Sketch). By induction on the derivation of the reduction. The cases correspond to the rules in Fig. 1 (bottom), as well as the
closure rules in Deﬁnition 2.5. In each case, we infer the typing of 𝑃 and construct one for 𝑄 from the shapes of the processes in the
rule, and show that these typing inferences have identical assumptions and conclusions. We detail two cases.
The case of Rule [𝛽 serv] serves to illustrate the need for multiple symmetric cut-rules. Suppose, for example, that the last-applied
rule is Rule [cut!R], and that the client request is derived using Rule [copyL]:

Γ, 𝑥 ∶ 𝐴; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ
[copyL]
Γ, 𝑥 ∶ 𝐴; Δ ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.𝑃 ∶∶ Λ
Γ; ∅ ⊢ 𝑄 ∶∶ 𝑧 ∶ 𝐴
Γ; Δ ⊢ (𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.𝑃 | !𝑥(𝑧).𝑄) ∶∶ Λ

[cut!R]

As per Rule [𝛽 serv], we need to identically type (𝜈𝑥)((𝜈𝑦)(𝑃 | 𝑄{𝑦∕𝑧}) | !𝑥(𝑧).𝑄) using the same assumptions as above. Had we only
had, e.g., Rules [cutRL] and [cutLL], this would not be possible. However, with the rules in Fig. 3 it is no problem. We ﬁrst have
to add 𝑥 ∶ 𝐴 into the persistent regions of the proof of the typing of 𝑄, and substitute 𝑦 for 𝑧, after which we derive the following:

Γ, 𝑥 ∶ 𝐴; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ
Γ, 𝑥 ∶ 𝐴; ∅ ⊢ 𝑄{𝑦∕𝑧} ∶∶ 𝑦 ∶ 𝐴
[cutLR]
Γ, 𝑥 ∶ 𝐴; Δ ⊢ (𝜈𝑦)(𝑃 | 𝑄{𝑦∕𝑧}) ∶∶ Λ
Γ; ∅ ⊢ 𝑄 ∶∶ 𝑧 ∶ 𝐴
Γ; Δ ⊢ (𝜈𝑥)((𝜈𝑦)(𝑃 | 𝑄{𝑦∕𝑧}) | !𝑥(𝑧).𝑄) ∶∶ Λ

[cut!R]

As another representative case, we consider Rule [𝛽 send]. We have 𝑃 = (𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.(𝑅 | 𝑆) | 𝑥(𝑧).𝑇 ) → (𝜈𝑥)(𝑆 | (𝜈𝑦)(𝑅 |
𝑇 {𝑦∕𝑧})) = 𝑄. There are multiple ways to type 𝑃 , depending on the cut-rule applied. Here, we give the example of Rule [cutR]. The
proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ looks as follows:

Γ; Δ1 ⊢ 𝑅 ∶∶ Λ1 , 𝑦 ∶ 𝐴
Γ; Δ2 ⊢ 𝑆 ∶∶ Λ2 , 𝑥 ∶ 𝐵
Γ; Δ3 , 𝑧 ∶ 𝐴, 𝑥 ∶ 𝐵 ⊢ 𝑇 ∶∶ Λ3
[⊗R]
Γ; Δ1 , Δ2 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑅 | 𝑆) ∶∶ Λ1 , Λ2 , 𝑥 ∶ 𝐴 ⊗ 𝐵
Γ; Δ3 , 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊢ 𝑥(𝑧).𝑇 ∶∶ Λ3
Γ; Δ1 , Δ2 , Δ3 ⊢ (𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩(𝑅 | 𝑆) | 𝑇 ) ∶∶ Λ1 , Λ2 , Λ3
⏟⏞⏞⏟⏞⏞⏟ ⏟⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏟⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏟ ⏟⏞⏞⏟⏞⏞⏟
𝑃

Δ

[⊗L]
[cutR]

Λ

We can then construct a proof of Γ; Δ ⊢ 𝑄 ∶∶ Λ using the assumptions in the above proof.

Γ; Δ1 ⊢ 𝑅 ∶∶ Λ1 , 𝑦 ∶ 𝐴
Γ; Δ3 , 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵 ⊢ 𝑇 {𝑦∕𝑧} ∶∶ Λ3
Γ; Δ2 ⊢ 𝑆 ∶∶ Λ2 , 𝑥 ∶ 𝐵
Γ; Δ1 , Δ3 , 𝑥 ∶ 𝐵 ⊢ (𝜈𝑦)(𝑅 | 𝑇 {𝑦∕𝑧}) ∶∶ Λ1 , Λ3
[cutR]
Γ; Δ ⊢ (𝜈𝑥)(𝑆 | (𝜈𝑦)(𝑅 | 𝑇 {𝑦∕𝑧})) ∶∶ Λ
⏟⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏟⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏞⏟

[cutR]

□

𝑄

Our next result is progress, the safety property that says that the speciﬁc form of composition and restriction in 𝜋𝖴𝖫𝖫 following
from the cut-rule enables communication, and that processes never get stuck waiting for each other:
Theorem 2.3 (Progress). If Γ; Δ ⊢ 𝑃 ∶∶ Λ and 𝑃 ≡ (𝜈𝑥)(𝑄 | 𝑅), then there exists 𝑃 ′ such that 𝑃 → 𝑃 ′ .
Proof. By induction on the size of the proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ. By Theorem 2.1, Γ; Δ ⊢ (𝜈𝑥)(𝑄 | 𝑅) ∶∶ Λ. By assumption, the last
inference of the derivation thereof is either a linear cut or an unrestricted cut.
(Case linear cut) The last-applied rule can be [cutR] or [cutL]. W.l.o.g. assume the former. By inversion of [cutR], we have a
proof 𝜋𝑄 of Γ; Δ𝑄 ⊢ 𝑄 ∶∶ Λ𝑄 , 𝑥 ∶ 𝐴 and a proof 𝜋𝑅 of Γ; Δ𝑅 , 𝑥 ∶ 𝐴 ⊢ 𝑅 ∶∶ Λ𝑅 where Δ𝑄 , Δ𝑅 = Δ and Λ𝑄 , Λ𝑅 = Λ.
If the last-applied rules in 𝜋𝑄 and 𝜋𝑅 are both on 𝑥, then we apply a 𝛽 -reduction depending on 𝐴. For example, assume 𝐴 = 𝐵 ⊗ 𝐶 .
Then the last-applied rules in 𝜋𝑄 and 𝜋𝑅 are [⊗R] and [⊗L], respectively. Hence, by Rule [𝛽 send], 𝑃 ≡ (𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.(𝑄𝑦 | 𝑄𝑥 ) |
𝑥(𝑦).𝑅′ ) → (𝜈𝑥)(𝑄𝑥 | (𝜈𝑦)(𝑄𝑦 | 𝑅′ )).
Otherwise, w.l.o.g. assume the last-applied rule not on 𝑥 is in 𝜋𝑄 . Then, if 𝑄 is a cut, by the induction hypothesis, 𝑄 → 𝑄′ , and
hence 𝑃 ≡ (𝜈𝑥)(𝑄 | 𝑅) → (𝜈𝑥)(𝑄′ | 𝑅). Otherwise, 𝑄 is preﬁxed by an action on some free channel 𝑦 which is not a free channel of 𝑅.
Hence, we apply a 𝜅 -conversion depending on the type of the channel the last-applied rule in 𝜋𝑄 works on. For example, if this rule
introduces 𝑦 ∶ 𝐵 ⊗ 𝐶 on the right, then, by Rule [𝜅⊗], 𝑃 ≡ (𝜈𝑥)((𝜈𝑧)𝑦⟨𝑧⟩.(𝑄𝑦 | 𝑄𝑧,𝑥 ) | 𝑅𝑥 ) → (𝜈𝑧)𝑦⟨𝑧⟩.((𝜈𝑥)(𝑄𝑧,𝑥 | 𝑅𝑥 ) | 𝑄𝑦 ).
(Case unrestricted cut) The last-applied rule can be [cut!] or [cut?]. W.l.o.g. assume the former. Then 𝑄 ≡ !𝑥(𝑦).𝑄′ , and,
by inversion of this rule, we have a proof 𝜋𝑄′ of Γ; ∅ ⊢ 𝑄′ ∶∶ 𝑦 ∶ 𝐴 and a proof 𝜋𝑅 of Γ, 𝑥 ∶ 𝐴; Δ ⊢ 𝑅 ∶∶ Λ. If 𝑥 ∉ fn(𝑅), then, by
Rule [𝛽 weaken], 𝑃 ≡ (𝜈𝑥)(𝑅 | !𝑥(𝑦).𝑄′ ) → 𝑅. Otherwise, the next step depends on the last-applied rule in 𝜋𝑅 .
If the last-applied rule in 𝜋𝑅 is on 𝑥, then it must be [copyR] or [copyL]. W.l.o.g. assume the former. Then 𝑅 ≡ (𝜈𝑦)𝑥⟨𝑦⟩.𝑅′ , so,
by Rule [𝛽 serv], 𝑃 ≡ (𝜈𝑥)((𝜈𝑦)𝑥⟨𝑦⟩.𝑅′ | !𝑥(𝑦).𝑄′ ) → (𝜈𝑥)((𝜈𝑦)(𝑄′ | 𝑅′ ) | !𝑥(𝑦).𝑄′ ).
Otherwise, the proof proceeds as in the last part of the case of linear cut. □
It follows from progress that closed processes are deadlock free. In a closed process, all channels are connected, except for one
channel. This remaining channel, which the process simply closes, can be seen as a barb that signals successful termination. As such,
deadlock freedom ensures that closed processes that cannot reduce are successfully terminated and thus not stuck in a deadlock. Let
us write 𝑃 ↛ to denote that there is no 𝑃 ′ such that 𝑃 → 𝑃 ′ .
8

## PDF page 9

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Theorem 2.4 (Deadlock freedom). Suppose ∅; ∅ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝟏 or ∅; 𝑧 ∶ ⊥ ⊢ 𝑃 ∶∶ ∅. If 𝑃 ↛, then 𝑃 ≡ 𝑧⟨⟩.𝟎.
Proof. Towards contradiction, assume 𝑃 ≢ 𝑧⟨⟩.𝟎. The only well-typed possibility is that 𝑃 ≡ (𝜈𝑥)(𝑄 | 𝑅). By Theorem 2.3, then
𝑃 → 𝑃 ′ . This contradicts the assumption that 𝑃 ↛, proving the thesis. □
The combination of Theorems 2.2 and 2.3 allows us to adapt existing techniques (e.g., the logical relations of [42]) to prove
termination: the liveness property that says that well-typed processes eventually stop reducing.
2.3. On duality
It may seem that there is an extensive redundancy in the system of rules in Fig. 2, caused by the two sidedness of 𝜋𝖴𝖫𝖫’s judgments:
every connective can be inferred on either side of judgments. For example, Rules [⊗R], [ L], and [⊸L] all type the send of a channel;
which rule to use depends on the side of the judgment the involved channels are on. However, there is no actual redundancy, for if
we were to omit rules for, e.g., and ⊸, it would be impossible to type a send on a previously received channel.
This abundance of typing rules in 𝜋𝖴𝖫𝖫 can be explained by its full support for duality: for every rule inferring a connective on
one side of a judgment, there is a rule for inferring the connective’s dual on the other side of a judgment. To make this duality explicit,
we deﬁne an alternative type system by restricting 𝜋𝖴𝖫𝖫’s rules to a speciﬁc fragment and adding LU’s rules for moving propositions
between sides of judgments:

&

&

Deﬁnition 2.6. The type system 𝜋𝖴𝖫𝖫↶
↷ , with judgments Γ; Δ ⊢
↶
↷ 𝑃 ∶∶ Λ, is deﬁned on the process calculus as deﬁned in Section 2.1.
Its rules are the ∗-marked rules in Fig. 2 plus the following rules:
[↶ ]

[↷ ]

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

Γ; Δ, 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ

Γ; Δ, 𝑥 ∶ 𝐴⊥ ⊢↶
↷ 𝑃 ∶∶ Λ

⊥
Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

Fortunately, in the presence of these two rules, a number of other rules become truly redundant: all rules in Fig. 2 not marked
with ∗ are admissible or derivable in 𝜋𝖴𝖫𝖫↶
↷ . Dually, Rules [↶] and [↷] are admissible in vanilla 𝜋𝖴𝖫𝖫 . The following theorem
formalizes these facts:
Theorem 2.5.
1. The rules in Figs. 2 and 3 not marked with ∗ are admissible or derivable in 𝜋𝖴𝖫𝖫↶
↷ , and
2. Rules [↶] and [↷], as given in Deﬁnition 2.6, are admissible in 𝜋𝖴𝖫𝖫.
Proof. (Item 1) Suppose given a proof of Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ. By applying induction on the structure of this proof we show that any
applications of non-∗-marked rules can be replaced with applications of ∗-marked rules in combination with uses of Rules [↶]
or [↷]. We discuss every possible last-applied rule, omitting cases of ∗-marked rules as they follow directly from the induction
hypothesis.

∙ [⊥R]

∙ [⊥L]

&

∙ [ R]

1

Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥ ⊢↶
↷ [𝑥 ↔ 𝑦] ∶∶ ∅

2

Γ; 𝑥 ∶ 𝐴 ⊢↶
↷ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴

3

⊥

Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴 ⊢↶
↷ [𝑥 ↔ 𝑦] ∶∶ ∅

1

Γ; Δ ⊢↶
↷ 𝑥().𝑃 ∶∶ Λ, 𝑥 ∶ ⊥

2

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ

3

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ with only ∗ rules

4

Γ; Δ, 𝑥 ∶ 𝟏 ⊢↶
↷ 𝑃 ∶∶ Λ

([𝟏L] on 3)

5

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ ⊥

([↷] on 4)

1

Γ; 𝑥 ∶ ⊥ ⊢↶
↷ 𝑥⟨⟩.𝟎 ∶∶ ∅

(assumption)

2

Γ; ∅ ⊢↶
↷ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏

([𝟏R])

3

Γ; 𝑥 ∶ ⊥ ⊢↶
↷ 𝑥⟨⟩.𝟎 ∶∶ ∅

([↶] on 2)

1

Γ; Δ ⊢↶
↷ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

2

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵

(assumption)
([idR])
([↶] on 2)
(assumption)
(inversion on 1)

&

∙ [idL]

𝐵

(IH on 2)

(assumption)
(inversion on 1)
9

## PDF page 10

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

3
4

∙ [cutRR]

∙ [cutLL]

⊥

([↶] twice on 3)

⊥

Γ; Δ, 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊢↶
↷ 𝑥(𝑦).𝑃 ∶∶ Λ

([⊗L] on 4)

6

Γ; Δ ⊢↶
↷ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

([↷] on 5)

1

Γ; Δ, Δ , 𝑥 ∶ 𝐴

2

Γ; Δ, 𝑦 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ

3

′
Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢↶
↷ 𝑄 ∶∶ Λ

4

Γ; Δ, 𝑦 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ with only ∗ rules

(IH on 2)

5

′
Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢↶
↷ 𝑄 ∶∶ Λ with only ∗ rules

(IH on 3)

6

⊥
Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴

([↷] on 4)

7

′
⊥
Γ; Δ′ ⊢↶
↷ 𝑄 ∶∶ Λ , 𝑥 ∶ 𝐵

([↷] on 5)

8

′
⊥
⊥
Γ; Δ, Δ′ ⊢↶
↷ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ , 𝑥 ∶ 𝐴 ⊗ 𝐵

9

Γ; Δ, Δ , 𝑥 ∶ 𝐴

1

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

′

′

&

&

∙ [?L]

Γ; Δ, 𝑦 ∶ 𝐴 , 𝑥 ∶ 𝐵 ⊢↶
↷ 𝑃 ∶∶ Λ

(IH on 2)

5

2

∙ [?R]

⊥

&

∙ [copyR]

⊥

&

∙ [ L]

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵 with only ∗ rules

𝐵

′
𝐵 ⊢↶
↷ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ

(assumption)

(inversion on 1)

𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′
↶
↷

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

([⊗R] on 6 and 7)
([↶] on 8)
(assumption)

⊥

(inversion on 1)

⊥

(IH on 2)

3

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴 with only ∗ rules

4

Γ, 𝑢 ∶ 𝐴; Δ, 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ

5

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

([copyL] on 4)

1

Γ; Δ ⊢↶
↷ 𝑃 {𝑥∕𝑢} ∶∶ Λ, 𝑥 ∶ ?𝐴

⊥

(assumption)

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ

3

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ with only ∗ rules

(IH on 2)

4

Γ; Δ, 𝑥 ∶ !𝐴 ⊢↶
↷ 𝑃 {𝑥∕𝑢} ∶∶ Λ

([!L] on 3)

([↶] on 3)

(inversion on 1)

⊥

5

Γ; Δ ⊢↶
↷ 𝑃 {𝑥∕𝑢} ∶∶ Λ, 𝑥 ∶ ?𝐴

1

Γ; 𝑥 ∶ ?𝐴 ⊢↶
↷ !𝑥(𝑦).𝑃 ∶∶ ∅

2

Γ; 𝑦 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ ∅

3

Γ; 𝑦 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ ∅ with only ∗ rules

(IH on 2)

4

⊥

([↷] on 3)

Γ; ∅ ⊢↶
↷ 𝑃 ∶∶ 𝑦 ∶ 𝐴

([↷] on 4)
(assumption)
(inversion on 1)

5

Γ; ∅ ⊢↶
↷ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐴

⊥

([!R] on 4)

6

Γ; 𝑥 ∶ ?𝐴 ⊢↶
↷ !𝑥(𝑦).𝑃 ∶∶ ∅

([↶] on 5)

1

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

2

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

3

′
⊥
Γ; Δ′ ⊢↶
↷ 𝑄 ∶∶ Λ , 𝑥 ∶ 𝐴

4

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴 with only ∗ rules

5

Γ; Δ ⊢↶
↷ 𝑄 ∶∶ Λ , 𝑥 ∶ 𝐴 with only ∗ rules

6

Γ; Δ , 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑄 ∶∶ Λ

7

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

([cutRL] on 4 and 6)

1

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

(assumption)

2

Γ; Δ, 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ

3

′
Γ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢↶
↷ 𝑄 ∶∶ Λ

4

Γ; Δ, 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Λ with only ∗ rules

′

(assumption)

↶
↷

′

⊥

′

′

(inversion on 1)

′

(IH on 3)
([↶] on 5)

′

′

(IH on 2)

↶
↷
↶
↷

(inversion on 1)

10

(IH on 2)

## PDF page 11

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

∙ [cut?R]

∙ [cut?L]

5

′
Γ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢↶
↷ 𝑄 ∶∶ Λ with only ∗ rules

(IH on 3)

6

Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

⊥

([↷] on 4)

7

′
Γ; Δ, Δ′ ⊢↶
↷ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ

1

Γ; Δ ⊢↶
↷ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ

3

Γ; 𝑥 ∶ 𝐴⊥ ⊢↶
↷ 𝑄 ∶∶ ∅

4

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑃 ∶∶ Λ with only ∗ rules

([cutRL] on 6 and 5)
(assumption)

(inversion on 1)
(IH on 2)

5

⊥

Γ; 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑄 ∶∶ ∅ with only ∗ rules

(IH on 3)

6

Γ; ∅ ⊢↶
↷ 𝑄 ∶∶ 𝑥 ∶ 𝐴

([↷] on 5)

7

Γ; Δ ⊢↶
↷ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

([cut!R] on 4 and 6)

1

Γ; Δ ⊢↶
↷ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

(assumption)

⊥

2

Γ; 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ ∅

3

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑄 ∶∶ Λ

(inversion on 1)

⊥

4

Γ; 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ ∅ with only ∗ rules

(IH on 2)

5

Γ, 𝑢 ∶ 𝐴; Δ ⊢↶
↷ 𝑄 ∶∶ Λ with only ∗ rules

(IH on 3)

6

Γ; ∅ ⊢↶
↷ 𝑃 ∶∶ 𝑥 ∶ 𝐴

7

Γ; Δ ⊢↶
↷ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

([↷] on 4)
([cut!L] on 6 and 5)

(Item 2) Suppose given a proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ, possibly with applications of Rules [↶] and [↷]. By applying induction on the
structure of this proof we show that it can be transformed to not contain any applications of [↶ ] and [↷]. We discuss every possible
last-applied rule. However, all cases except [↶] and [↷] follow directly from the induction hypothesis. Therefore, we only detail the
case of [↶]—the case of [↷] is analogous.
Since [↶] is the last-applied rule, we know the assumption is of the form Γ; Δ, 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ∶∶ Λ. By inversion, we have Γ; Δ ⊢ 𝑃 ∶∶
Λ, 𝑥 ∶ 𝐴. The idea is to move the application of [↶] up the proof tree, applied to a subterm of 𝐴. We apply the induction hypothesis
to ﬁnd a proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴 without applications of [↶] and [↷]. Typing rules leave all channels/types untouched except
the ones they work on. Therefore, we can traverse up the proof tree—remembering which steps were taken—until we encounter the
rule that introduces 𝑥 ∶ 𝐴. Note that these steps do not include applications of [↶] and [↷]. The consequence of this rule looks like
Γ′ ; Δ′ ⊢ 𝑃 ′ ∶∶ Λ′ , 𝑥 ∶ 𝐴, for some Γ′ , Δ′ , 𝑃 ′ and Λ′ . Now, we apply induction on the size of 𝐴 (with induction hypothesis denoted IH2 )
to prove Γ′ ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ′ ∶∶ Λ′ . We discuss every possible last-applied rule that introduces 𝑥 ∶ 𝐴:

∙ [idR]

∙ [𝟏R]

∙ [⊥R]

∙ [⊗R]

1

Γ′ ; 𝑦 ∶ 𝐴 ⊢ [𝑦 ↔ 𝑥] ∶∶ 𝑥 ∶ 𝐴

2

Γ ; 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐴 ⊢ [𝑦 ↔ 𝑥] ∶∶ ∅

1

Γ′ ; ∅ ⊢ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏

(assumption)

2

Γ′ ; 𝑥 ∶ ⊥ ⊢ 𝑥⟨⟩.𝟎 ∶∶ ∅

([⊥L])

1

Γ′ ; Δ′ ⊢ 𝑥().𝑃 ′ ∶∶ Λ′ , 𝑥 ∶ ⊥ without [↶]/[↷]

2

Γ ; Δ ⊢ 𝑃 ∶∶ Λ

3

Γ ; Δ , 𝑥 ∶ 𝟏 ⊢ 𝑥().𝑃 ∶∶ Λ

1

Γ ;Δ ,Δ

′
′
′

(assumption)

⊥

′

′

′

′
′

′′

(assumption)
(inversion on 1)

′
′

([idL])

([𝟏L] on 2)

′

⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 ′ | 𝑄′ ) ∶∶ Λ′ , Λ′′ , 𝑥 ∶ 𝐵 ⊗ 𝐶

without [↶]/[↷]

(assumption)

2

Γ ; Δ ⊢ 𝑃 ∶∶ Λ , 𝑦 ∶ 𝐵

3

Γ′ ; Δ′′ ⊢ 𝑄′ ∶∶ Λ′′ , 𝑥 ∶ 𝐶

4

Γ ; Δ , 𝑦 ∶ 𝐵 ⊢ 𝑃 ∶∶ Λ

5

Γ ; Δ , 𝑥 ∶ 𝐶 ⊢ 𝑄 ∶∶ Λ

([↶] on 3)

6

⊥

Γ ; Δ , 𝑦 ∶ 𝐵 ⊢ 𝑃 ∶∶ Λ without [↶]/[↷]

(IH2 on 4)

7

Γ ; Δ , 𝑥 ∶ 𝐶 ⊢ 𝑄 ∶∶ Λ without [↶]/[↷]

′

′
′
′
′

′

′

′′
′

′′

′

′

⊥

′

⊥

⊥

(inversion on 1)
([↶] on 2)

′

′

′

′′

′

′

′′

11

(IH2 on 5)

## PDF page 12

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

∙ [&R]

∙ [!R]

∙ [?R]

1

Γ′ ; Δ′ ⊢ 𝑥(𝑦).𝑃 ′ ∶∶ Λ′ , 𝑥 ∶ 𝐵 ⊸ 𝐶 without [↶]/[↷]

2

Γ′ ; Δ′ , 𝑦 ∶ 𝐵 ⊢ 𝑃 ′ ∶∶ Λ′ , 𝑥 ∶ 𝐶

3

Γ ; Δ , 𝑦 ∶ 𝐵, 𝑥 ∶ 𝐶 ⊢ 𝑃 ∶∶ Λ

4

Γ ; Δ , 𝑦 ∶ 𝐵, 𝑥 ∶ 𝐶 ⊢ 𝑃 ∶∶ Λ without [↶]/[↷]

5

Γ′ ; Δ′ , 𝑥 ∶ 𝐵 ⊗ 𝐶 ⊥ ⊢ 𝑥(𝑦).𝑃 ′ ∶; Λ′

([⊗L] on 4)

1

Γ′ ; Δ′ ⊢ 𝑥 ⊲ 𝑗.𝑃 ′ ∶∶ Λ′ , 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 without [↶]/[↷]

(assumption)

2

Γ ; Δ ⊢ 𝑃 ∶∶ Λ , 𝑥 ∶ 𝐴𝑗

3

𝑗∈𝐼

′
′

′

′
′

′

′

&

∙ [⊕R]

Γ′ ; Δ′ , Δ′′ , 𝑥 ∶ 𝐵 ⊥

𝐶 ⊥ ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 ′ | 𝑄′ ) ∶∶ Λ′ , Λ′′

⊥

′

⊥

′

&

∙ [⊸R]

8

([ L] on 8 and 9)
(assumption)
(inversion on 1)
([↶] on 2)

′
′

(IH2 on 3)

′

(inversion on 1)
⊥

4

′

Γ ; Δ , 𝑥 ∶ 𝐴𝑗 ⊢ 𝑃 ∶∶ Λ

([↶] on 3)

5

Γ′ ; Δ′ , 𝑥 ∶ 𝐴⊥𝑗 ⊢ 𝑃 ′ ∶∶ Λ′

(IH2 on 4)

6

Γ′ ; Δ′ , 𝑥 ∶ &{𝑖 ∶ 𝐴⊥𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊲ 𝑗.𝑃 ′ ∶∶ Λ′

1

Γ ; Δ ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖′ }𝑖∈𝐼 ∶∶ Λ′ , 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 without [↶]/[↷]

2

∀𝑖 ∈ 𝐼. Γ ; Δ ⊢ 𝑃𝑖′ ∶∶ Λ′ , 𝑥 ∶ 𝐴𝑖

(inversion on 1)

3

∀𝑖 ∈ 𝐼. Γ′ ; Δ′ , 𝑥 ∶ 𝐴⊥𝑖 ⊢ 𝑃𝑖′ ∶∶ Λ′

([↶] on 2)

4

∀𝑖 ∈ 𝐼. Γ′ ; Δ′ , 𝑥 ∶ 𝐴⊥𝑖 ⊢ 𝑃𝑖′ ∶∶ Λ′ without [↶]/[↷]

(IH2 on 3)

5

Γ ; Δ , 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖′ }𝑖∈𝐼 ∶∶ Λ′

([⊕L] on 4)

1

Γ ; ∅ ⊢ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐵 without [↶]/[↷]

(assumption)

2

Γ ; ∅ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐵

(inversion on 1)

3

Γ′ ; 𝑦 ∶ 𝐵 ⊥ ⊢ 𝑃 ′ ∶∶ ∅

([↶] on 2)

4

Γ ; 𝑦 ∶ 𝐵 ⊢ 𝑃 ∶∶ ∅ without [↶]/[↷]

5

Γ ; 𝑥 ∶ ?𝐵 ⊢ !𝑥(𝑦).𝑃 ∶∶ ∅

′

′

′

′

′

′

′

′

⊥

′

′

′

′

′

⊥

′

′

⊥

′

′

([&L] on 5 and 3)
(assumption)

(IH2 on 3)
([?L] on 4)

1

′

Γ ; Δ ⊢ 𝑃 {𝑥∕𝑢} ∶∶ Λ , 𝑥 ∶ ?𝐵

(assumption)

2

Γ′ , 𝑢 ∶ 𝐴⊥ ; Δ′ ⊢ 𝑃 ′ ∶∶ Λ′

(inversion on 1)

3

Γ′ ; Δ′ , 𝑥 ∶ !𝐵 ⊥ ⊢ 𝑃 ′ {𝑥∕𝑢} ∶∶ Λ′

′

′

′

([!L] on 2)

Finally, we recall the steps we have traversed up the tree and remember that they do not include applications of [↶ ] and [↷]. We
re-apply them on Γ′ ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ′ ∶∶ Λ′ , without aﬀecting 𝑥 ∶ 𝐴⊥ . Instead, they only aﬀect Γ′ , Δ′ and Λ′ to give us a proof of
Γ; Δ, 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ∶∶ Λ without applications of [↶] and [↷].
This concludes the proof of Theorem 2.5. □
3. Comparing intuitionistic and classical interpretations
In this section, we rigorously compare the class of 𝜋𝖴𝖫𝖫 -typable processes to the classes of processes typable in session type
interpretations of linear logic, in classical [12,56] and intuitionistic [7] settings. 𝜋𝖴𝖫𝖫 is an independent yardstick for this comparison,
because it is derived from 𝖴𝖫𝖫 which subsumes both linear logics by design.
We have discussed in Section 2 several design choices we made when deﬁning 𝖴𝖫𝖫 and 𝜋𝖴𝖫𝖫. Besides diﬀerences stemming from
the dichotomy between classical and intuitionistic linear logic, logically-motivated session type systems also present features induced
by certain design choices. For a fair comparison, we want to make sure that the diﬀerences come only from typing. This means that
we need to make the same design choices for both interpretations: we require explicit closing, a separate unrestricted context, and
identity as forwarding.
3.1. Session type systems derived from intuitionistic and classical linear logic
Our goal is to derive session type systems from intuitionistic and classical linear logic for the same process syntax as 𝜋𝖴𝖫𝖫 uses
(cf. Deﬁnition 2.3).
12

## PDF page 13

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[𝟏L]

[id]

[𝟏R]

Γ; 𝑥 ∶ 𝐴 ⊢ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴

Γ; ∅ ⊢ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏

[⊗R]

Γ; Δ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐴

[⊗L]

Γ; Δ′ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐵

Γ; Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵 ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, Δ′ ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ 𝑥 ∶ 𝐴 ⊗ 𝐵

Γ; Δ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐴

Γ; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐵

Γ; Δ ⊢ 𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ 𝐴 ⊸ 𝐵
[⊕R]

Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴𝑗

Γ; Δ, 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊢ 𝑥(𝑦).𝑃 ∶∶ 𝑧 ∶ 𝐶
[⊸L]

[⊸R]

[⊕L]

𝑗∈𝐼

∀𝑖 ∈ 𝐼. Γ; Δ, 𝑥 ∶ 𝐴𝑖 ⊢ 𝑃𝑖 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ 𝑧 ∶ 𝐶
[&L]

Γ; Δ, 𝑥 ∶ 𝐴𝑗 ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

∀𝑖 ∈ 𝐼. Γ; Δ ⊢ 𝑃𝑖 ∶∶ 𝑥 ∶ 𝐴𝑖

Γ; Δ ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼
[!R]

Γ, 𝑢 ∶ 𝐴; Δ ⊢ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; ∅ ⊢ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐴

Γ, 𝑢 ∶ 𝐴; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, 𝑥 ∶ !𝐴 ⊢ 𝑃 {𝑥∕𝑢} ∶∶ 𝑧 ∶ 𝐶

[cutLR]

Γ; Δ′ , 𝑥 ∶ 𝐴 ⊢ 𝑄 ∶∶ 𝑧 ∶ 𝐶

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

[!L]

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐴

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, Δ′ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ 𝑧 ∶ 𝐶
[cut!R]

𝑗∈𝐼

Γ; Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ 𝑧 ∶ 𝐶

[copy]

[cutRL]

Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢ 𝑄 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, Δ′ , 𝑥 ∶ 𝐴 ⊸ 𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ 𝑧 ∶ 𝐶

Γ; Δ ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼
[&R]

Γ; Δ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ, 𝑥 ∶ 𝟏 ⊢ 𝑥().𝑃 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ′ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐴

Γ; Δ, Δ′ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ 𝑧 ∶ 𝐶
[cut!L]

Γ; ∅ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐴

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴

Γ; Δ ⊢ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ 𝑧 ∶ 𝐶

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑄 ∶∶ 𝑧 ∶ 𝐶

Γ; Δ ⊢ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ 𝑧 ∶ 𝐶

Fig. 4. The 𝜋𝖨𝖫𝖫 type system.

The intuitionistic type system (𝜋𝖨𝖫𝖫) Fig. 4 gives the inference rules for the type system derived from intuitionistic linear logic, denoted
𝜋𝖨𝖫𝖫. Following the presentation by Caires, Pfenning, and Toninho in [11], propositions/types for the intuitionistic type system are
generated by the following grammar (a fragment of Deﬁnition 2.1):

𝐴, 𝐵 ∶∶= 𝟏 | 𝐴 ⊗ 𝐵 | 𝐴 ⊸ 𝐵 | ⊕{𝑖 ∶ 𝐴}𝑖∈𝐼 | &{𝑖 ∶ 𝐴}𝑖∈𝐼 | !𝐴
Notice how, following most presentations of intuitionistic linear logic (e.g., [25,3,38]), 𝜋𝖨𝖫𝖫 propositions do not include ⊥ and ?.
The judgment is denoted as follows:

Γ; Δ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝐶
With respect to the intuitionistic interpretation introduced in [7,12], 𝜋𝖨𝖫𝖫 features a non-silent interpretation of 𝟏, based on explicit
closure of sessions (cf. Rules [𝟏R] and [𝟏L]). We adopt this interpretation because, as explained in [11], it leads to a Curry-Howard
correspondence that is tighter than correspondences with silent interpretations (such as those in [7,12]).
A more superﬁcial diﬀerence is that 𝜋𝖨𝖫𝖫 follows standard presentations of session type systems by supporting 𝑛-ary labeled
choices; in contrast, the systems in [7,12] support binary labeled choices. We also include symmetric variants of the cut-rules, as they
are necessary for type preservation under Rule [CutSymm] of structural congruence. As expected, none of these cut-rules make use
of the duality relation in Deﬁnition 2.2.
The classical type system (𝜋𝖢𝖫𝖫⋆ ) Fig. 5 gives the inference rules for the type system derived from classical linear logic. It is based on
a combination of features from Caires, Pfenning, and Toninho’s 𝜋𝖢𝖫𝖫 in [12] and Wadler’s 𝖢𝖯 in [56]; in the following, it is denoted
𝜋𝖢𝖫𝖫⋆ . The syntax of propositions/types is exactly as in Deﬁnition 2.1. The corresponding judgment is as follows:

𝑃 ⊢ Γ; Δ
Table 2 summarizes the diﬀerences in the design choices between 𝜋𝖢𝖫𝖫, 𝖢𝖯, and 𝜋𝖢𝖫𝖫⋆ ; these diﬀerences are merely superﬁcial:
• As we have seen, an explicit closing of sessions (as in 𝖢𝖯) concerns a non-silent interpretation of the atomic propositions 𝟏 and
⊥. In contrast, 𝜋𝖢𝖫𝖫 realizes an implicit (silent) closing of sessions.
• Sequents with a separate unrestricted context (as in 𝜋𝖢𝖫𝖫) are of the form 𝑃 ⊢ Γ; Δ, which can also be written as 𝑃 ⊢ Δ, Γ′
where Γ′ contains only types of the form !𝐴.
• The identity axiom can be interpreted as the forwarding process, which enables 𝖢𝖯 to account for behavioral polymorphism
(i.e., universal and existential quantiﬁcation over propositions/session types) [56,9]. As already mentioned, forwarding is not a
typical process construct in session 𝜋 -calculi.
13

## PDF page 14

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[⊥]

[id]

[𝑥 ↔ 𝑦] ⊢ Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴
[⊗]

[𝟏 ]

𝑃 ⊢ Γ; Δ

𝑥().𝑃 ⊢ Γ; Δ, 𝑥 ∶ ⊥

⊥

𝑥⟨⟩.𝟎 ⊢ Γ; 𝑥 ∶ 𝟏

&

[ ]

𝑄 ⊢ Γ; Δ′ , 𝑥 ∶ 𝐵

𝑃 ⊢ Γ; Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵

(𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ⊢ Γ; Δ, Δ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵
[⊕]

𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴𝑗

𝑥(𝑦).𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴

[&]

𝑗∈𝐼

𝑥 ⊲ 𝑗.𝑃 ⊢ Γ; Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

∀𝑖 ∈ 𝐼. 𝑃𝑖 ⊢ Γ; Δ, 𝑥 ∶ 𝐴𝑖

[copy]

[?]

(𝜈𝑦)𝑢⟨𝑦⟩.𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

𝑃 {𝑥∕𝑢} ⊢ Γ; Δ, 𝑥 ∶ ?𝐴
𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴

!𝑥(𝑦).𝑃 ⊢ Γ; 𝑥 ∶ !𝐴
[cut?R]

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

[cut]

𝑃 ⊢ Γ; 𝑦 ∶ 𝐴

𝐵

𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ⊢ Γ; Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ, 𝑦 ∶ 𝐴

[!]

&

𝑃 ⊢ Γ; Δ, 𝑦 ∶ 𝐴

𝑄 ⊢ Γ; Δ′ , 𝑥 ∶ 𝐴⊥

(𝜈𝑥)(𝑃 | 𝑄) ⊢ Γ; Δ, Δ′
[cut?L]

𝑄 ⊢ Γ; 𝑥 ∶ 𝐴⊥

𝑃 ⊢ Γ; 𝑥 ∶ 𝐴⊥

(𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ⊢ Γ; Δ

𝑄 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

(𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ⊢ Γ; Δ

Fig. 5. The 𝜋𝖢𝖫𝖫⋆ type system.

Table 2
Feature comparison of three session type interpretations of classical linear logic.

𝜋𝖢𝖫𝖫 [12]
𝖢𝖯 [56]
𝜋𝖢𝖫𝖫⋆ (this paper)

Explicit closing

Separate unrestricted context

Identity as forwarding

No
Yes
Yes

Yes
No
Yes

No
Yes
Yes

Note that, since 𝜋𝖢𝖫𝖫⋆ typing judgments are one-sided, there is no need for symmetric cut-rules. The three cut-rules in Fig. 5 use
duality as in Deﬁnition 2.2.
3.2. Formal comparison
Now that we have presented all three systems, we start our comparison by contrasting the shape of their typing judgments:

Γ; Δ ⊢ 𝑃 ∶∶ Λ

Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴

𝑃 ⊢ Γ; Δ

In 𝜋𝖴𝖫𝖫 and 𝜋𝖨𝖫𝖫 judgments are similar, but in 𝜋𝖨𝖫𝖫 they have exactly one channel/type pair on the right. We will see that the
diﬀerence between 𝜋𝖴𝖫𝖫 and 𝜋𝖨𝖫𝖫 can be characterized by this fact alone. Judgments in 𝜋𝖢𝖫𝖫⋆ are diﬀerent from those in 𝜋𝖴𝖫𝖫
and 𝜋𝖨𝖫𝖫: they have only one linear context and both the linear and the unrestricted contexts are on the right. As we will see, our
results reﬂect this with a duality relation between the contexts of 𝜋𝖴𝖫𝖫 and 𝜋𝖢𝖫𝖫⋆ .
Our formal results rely on classes of processes typable in the three typing systems:
Deﬁnition 3.1. Let ℙ denote the set of all processes induced by Deﬁnition 2.3. Then

 = {𝑃 ∈ ℙ ∣ ∃Γ, Δ, Λ such that Γ; Δ ⊢ 𝑃 ∶∶ Λ},
 = {𝑃 ∈ ℙ ∣ ∃Γ, Δ such that 𝑃 ⊢ Γ; Δ},
 = {𝑃 ∈ ℙ ∣ ∃Γ, Δ, 𝑥, 𝐴 such that Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴}.
Our ﬁrst result is that  =  , i.e., 𝜋𝖴𝖫𝖫 is merely a two-sided representation of 𝜋𝖢𝖫𝖫⋆ .
Theorem 3.1.  =  .
We brieﬂy discuss how we prove this result. On the one hand (from left to right), if 𝑃 ∈  , there is a proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ.
By backtracking on this proof, we can use rules in 𝜋𝖢𝖫𝖫⋆ analogous to the 𝜋𝖴𝖫𝖫-rules used to generate an equivalent proof of
𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ thus showing 𝑃 ∈  . Note how the single-sidedness of 𝜋𝖢𝖫𝖫⋆ judgments requires us to move Γ and Δ to the
right-hand side using duality.
14

## PDF page 15

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

On the other hand (from right to left), if 𝑃 ∈  , there is a proof of 𝑃 ⊢ Γ; Δ. Again, by backtracking on this proof, we can use a
combination of rules similar to those used in 𝜋𝖢𝖫𝖫⋆ in combination with Rules [↶] and [↷] from Deﬁnition 2.6 to prove (Γ)⊥ ; ∅ ⊢↶
↷Δ
in 𝜋𝖴𝖫𝖫↶
↷ . Going through 𝜋𝖴𝖫𝖫↶
↷ simpliﬁes this process, since using [↶] and [↷] enables us to guarantee that all of Δ ends up
on the right-hand side of the typing judgment instead of dividing unpredictably between left and right. Note that we do have to
use duality to move Γ to the left. Since [↶] and [↷] are admissible in 𝜋𝖴𝖫𝖫 (cf. Theorem 2.5), this means we also have a proof of
(Γ)⊥ ; ∅ ⊢ Δ in 𝜋𝖴𝖫𝖫. Hence, 𝑃 ∈  .
Proof of Theorem 3.1. (  ⊆  ) Take any 𝑃 ∈  . Then, by Deﬁnition 3.1, there are Γ, Δ, Λ s.t. Γ; Δ ⊢ 𝑃 ∶∶ Λ. By showing that
this implies 𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, we have 𝑃 ∈  . We show this by induction on the structure of the proof of Γ; Δ ⊢ 𝑃 ∶∶ Λ.

2

[𝑥 ↔ 𝑦] ⊢ (Γ) ; 𝑥 ∶ 𝐴 , 𝑦 ∶ 𝐴

1

⊥

Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴 ⊢ [𝑥 ↔ 𝑦] ∶∶ ∅

2

⊥

[𝑥 ↔ 𝑦] ⊢ (Γ) ; 𝑥 ∶ 𝐴 , 𝑦 ∶ 𝐴

1

Γ; ∅ ⊢ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏
𝑥⟨⟩.𝟎 ⊢ (Γ) ; 𝑥 ∶ 𝟏

1

Γ; Δ, 𝑥 ∶ 𝟏 ⊢ 𝑥().𝑃 ∶∶ Λ

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ

&

∙ [ R]

⊥

([𝟏])
(assumption)
(inversion on 1)

⊥

𝑃 ⊢ (Γ) ; (Δ) , Λ
⊥

(IH on 2)

⊥

𝑥().𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ ⊥

1

Γ; Δ ⊢ 𝑥().𝑃 ∶∶ Λ, 𝑥 ∶ ⊥

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ

3

𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ

([⊥] on 3)
(assumption)
(inversion on 1)

⊥

(IH on 2)

⊥

4

𝑥().𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ ⊥

1

Γ; 𝑥 ∶ ⊥ ⊢ 𝑥⟨⟩.𝟎 ∶∶ ∅

([⊥] on 3)
(assumption)

⊥

2

𝑥⟨⟩.𝟎 ⊢ (Γ) ; 𝑥 ∶ 𝟏

1

Γ; Δ, Δ ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴

3

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐵

([𝟏])

′

⊥

⊥

⊥

′ ⊥

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑦 ∶ 𝐴

(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐵

6

(𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ⊢ (Γ)⊥ ; (Δ)⊥ , (Δ′ )⊥ , Λ, Λ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵

1

Γ; Δ, 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ

2

Γ; Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵 ⊢ 𝑃 ∶∶ Λ

3

𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑦 ∶ 𝐴⊥ , 𝑥 ∶ 𝐵 ⊥
⊥

′

(IH on 3)

⊥

𝑥(𝑦).𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴

1

Γ; Δ ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵

(assumption)

⊥

(IH on 2)

𝐵

⊥

𝐵

(inversion on 1)

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵
⊥

4

𝑥(𝑦).𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴

1

Γ; Δ, Δ , 𝑥 ∶ 𝐴

2

Γ; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

3

Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢ 𝑄 ∶∶ Λ′

′

([ ] on 3)
(assumption)

⊥

⊥

([⊗] on 4 and 5)

(inversion on 1)

4

⊥

(assumption)

(inversion on 1)

5

3

&

∙ [ L]

(assumption)

4

4

∙ [⊗L]

([id])

⊥

&

∙ [⊗R]

(assumption)

(IH on 2)

&

∙ [⊥L]

([id])

⊥

2

3

∙ [⊥R]

(assumption)

⊥

𝐵

𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′

&

∙ [𝟏L]

⊥

&

∙ [𝟏R]

Γ; 𝑥 ∶ 𝐴 ⊢ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴

&

∙ [idL]

1

&

∙ [IdR]

([ ] on 3)
(assumption)

(inversion on 1)
15

## PDF page 16

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑦 ∶ 𝐴⊥

(IH on 2)

5

𝑄 ⊢ (Γ)⊥ ; (Δ′ )⊥ , Λ′ , 𝑥 ∶ 𝐵 ⊥

(IH on 3)

6

(𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ⊢ (Γ)⊥ ; (Δ)⊥ , (Δ′ )⊥ , Λ, Λ′ , 𝑥 ∶ 𝐴⊥ ⊗ 𝐵 ⊥

1

Γ; Δ ⊢ 𝑥(𝑦).𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴 ⊸ 𝐵

2

Γ; Δ, 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐵

3

∙ [⊕L]

∙ [copyL]

⊥

⊥

(IH on 2)

1
2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴

3

Γ; Δ′ , 𝑥 ∶ 𝐵 ⊢ 𝑄 ∶∶ Λ′

4

𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑦 ∶ 𝐴

𝐵

([ ] on 3)

′

⊥

′ ⊥

(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐵
′

⊥

(IH on 3)

(Γ) ; (Δ) , (Δ′ )⊥ , Λ, Λ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵 ⊥

(𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ⊢

1

Γ; Δ ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ Λ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

2

∀𝑖 ∈ 𝐼. Γ; Δ ⊢ 𝑃𝑖 ∶∶ Λ, 𝑥 ∶ 𝐴𝑖

⊥

⊥

(assumption)

(inversion on 1)

6

⊥

∀𝑖 ∈ 𝐼. 𝑃𝑖 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴𝑖
⊥

([⊗] on 4 and 5)
(assumption)
(inversion on 1)

⊥

(IH on 2)

⊥

4

𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

1

Γ; Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 } ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ Λ

2

Γ; Δ, 𝑥 ∶ 𝐴𝑗 ⊢ 𝑃 ∶∶ Λ

3

𝑗∈𝐼

([&] on 3)
(assumption)

(inversion on 1)
⊥

⊥

⊥

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴𝑗
⊥

(IH on 2)

5

⊥

𝑥 ⊳ 𝑗.𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

([⊕] on 4 and 3)

1

Γ; Δ ⊢ 𝑥 ⊲ 𝑗.𝑃 ∶∶ Λ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

(assumption)

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴𝑗

3

𝑗∈𝐼

4

𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑥 ∶ 𝐴𝑗

5

𝑥 ⊲ 𝑗.𝑃 ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

1

Γ; Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼 ⊢ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ Λ

2

∀𝑖 ∈ 𝐼. Γ; Δ, 𝑥 ∶ 𝐴𝑖 ⊢ 𝑃𝑖 ∶∶ Λ

3

∙ [copyR]

⊥

Γ; Δ, Δ , 𝑥 ∶ 𝐴 ⊸ 𝐵 ⊢ (𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ∶∶ Λ, Λ′

4

∙ [⊕R]

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑦 ∶ 𝐴 , 𝑥 ∶ 𝐵
𝑥(𝑦).𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴

3

∙ [&L]

(inversion on 1)

⊥

4

5

∙ [&R]

⊥

(assumption)

&

∙ [⊸L]

⊥

([⊗] on 4 and 5)

&

∙ [⊸R]

4

⊥

(inversion on 1)

⊥

(IH on 2)
([⊕] on 4 and 3)

(inversion on 1)

⊥

⊥

∀𝑖 ∈ 𝐼. 𝑃𝑖 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴𝑖
⊥

(assumption)

⊥

(IH on 2)
⊥

4

𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

1

Γ, 𝑢 ∶ 𝐴; Δ ⊢ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

(assumption)

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴⊥

(inversion on 1)

3

𝑃 ⊢ (Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; (Δ)⊥ , Λ, 𝑥 ∶ 𝐴⊥

4

(𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ⊢ (Γ) , 𝑢 ∶ 𝐴 ; (Δ ), Λ

([copy] on 3)

1

Γ, 𝑢 ∶ 𝐴; Δ ⊢ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Λ

(assumption)

2

Γ, 𝑢 ∶ 𝐴; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

⊥

⊥

⊥

⊥

⊥

⊥

3

𝑃 ⊢ (Γ) , 𝑢 ∶ 𝐴 ; (Δ) , Λ, 𝑥 ∶ 𝐴

4

(𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ (Γ) , 𝑢 ∶ 𝐴 ; (Δ) , Λ
⊥

(IH on 2)

(inversion on 1)

⊥

⊥

([&] on 4)

⊥

16

(IH on 2)
([copy] on 3)

## PDF page 17

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

∙ [!R]

∙ [!L]

∙ [?R]

∙ [?L]

∙ [cutRL]

1

Γ; ∅ ⊢ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐴

2

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑦 ∶ 𝐴

3

⊥

𝑃 ⊢ (Γ) ; 𝑦 ∶ 𝐴

(IH on 2)

4

⊥

!𝑥(𝑦).𝑃 ⊢ (Γ) ; 𝑦 ∶ !𝐴

([!] on 3)

1

Γ; Δ, 𝑥 ∶ !𝐴 ⊢ 𝑃 {𝑥∕𝑢} ∶∶ Λ

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ

3

𝑃 ⊢ (Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; (Δ)⊥ , Λ

(IH on 2)

4

𝑃 {𝑥∕𝑢} ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑥 ∶ ?𝐴⊥

([?] on 3)

1

Γ; Δ ⊢ 𝑃 {𝑥∕𝑢} ∶∶ Λ, 𝑥 ∶ ?𝐴⊥

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ

3

𝑃 ⊢ (Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; (Δ)⊥ , Λ

(IH on 2)

4

𝑃 {𝑥∕𝑢} ⊢ (Γ)⊥ ; (Δ)⊥ , Λ, 𝑥 ∶ ?𝐴⊥

([?] on 3)

1

Γ; 𝑥 ∶ ?𝐴 ⊢ !𝑥(𝑦).𝑃 ∶∶ ∅

2

Γ; 𝑦 ∶ 𝐴 ⊢ 𝑃 ∶∶ ∅

3

⊥

𝑃 ⊢ (Γ) ; 𝑦 ∶ 𝐴

4

⊥

!𝑥(𝑦).𝑃 ⊢ (Γ) ; 𝑥 ∶ !𝐴

1

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

3

Γ; Δ′ , 𝑥 ∶ 𝐴 ⊢ 𝑄 ∶∶ Λ′

4
5

∙ [cutLR]

(assumption)
(inversion on 1)

⊥

(IH on 2)
⊥

([!] on 3)

′

⊥

⊥

⊥

′ ⊥

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴

(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐴
′

⊥

2

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

3

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐴

⊥

′

⊥

⊥

⊥

′ ⊥

(assumption)

(inversion on 1)
(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐴

(IH on 3)

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴
′

1

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

2

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴

3

Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′ , 𝑥 ∶ 𝐴⊥

(Γ) ; (Δ) , (Δ′ )⊥ , Λ, Λ′
⊥

⊥

′

⊥

⊥

⊥

′ ⊥

(assumption)

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴

(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐴
′

⊥

(𝜈𝑥)(𝑃 | 𝑄) ⊢

1

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

2

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ

3

Γ; Δ′ , 𝑥 ∶ 𝐴⊥ ⊢ 𝑄 ∶∶ Λ′

(IH on 3)

(Γ) ; (Δ) , (Δ′ )⊥ , Λ, Λ′
⊥

⊥

′

⊥

⊥

⊥

′ ⊥

([cut] on 4 and 5)

(inversion on 1)

6

6

([cut] on 4 and 5)

⊥

(𝜈𝑥)(𝑃 | 𝑄) ⊢

5

(IH on 3)

(Γ) ; (Δ) , (Δ′ )⊥ , Λ, Λ′
⊥

6

4

(assumption)

(inversion on 1)

1

5

(assumption)
(inversion on 1)

Γ; Δ, Δ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Λ, Λ′

4

(assumption)
(inversion on 1)

(𝜈𝑥)(𝑃 | 𝑄) ⊢

5

∙ [cutLL]

(inversion on 1)

6

4

∙ [cutRR]

(assumption)

([cut] on 4 and 5)
(assumption)

(inversion on 1)
⊥

(IH on 2)

𝑄 ⊢ (Γ) ; (Δ ) , Λ , 𝑥 ∶ 𝐴

(IH on 3)

𝑃 ⊢ (Γ) ; (Δ) , Λ, 𝑥 ∶ 𝐴
(𝜈𝑥)(𝑃 | 𝑄) ⊢

′

(Γ) ; (Δ) , (Δ′ )⊥ , Λ, Λ′
⊥

⊥

17

([cut] on 4 and 5)

## PDF page 18

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

∙ [cut!R]

∙ [cut!L]

∙ [cut?R]

∙ [cut?L]

1

Γ; Δ ⊢ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ

3

Γ; ∅ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐴

4

𝑃 ⊢ (Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; (Δ)⊥ , Λ

5

𝑄 ⊢ (Γ)⊥ ; 𝑥 ∶ 𝐴

6

(𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ⊢ (Γ) ; (Δ) , Λ

1

Γ; Δ ⊢ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

2

Γ; ∅ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴

3

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑄 ∶∶ Λ

4

⊥

(assumption)

(inversion on 1)
(IH on 2)
(IH on 3)
⊥

⊥

([cut?R] on 4 and 5)
(assumption)

(inversion on 1)

𝑃 ⊢ (Γ) ; 𝑥 ∶ 𝐴
⊥

(IH on 2)

⊥

⊥

5

𝑄 ⊢ (Γ) , 𝑢 ∶ 𝐴 ; (Δ) , Λ

6

(𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ⊢ (Γ) ; (Δ) , Λ

1

Γ; Δ ⊢ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Λ

2

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑃 ∶∶ Λ

3

Γ; 𝑥 ∶ 𝐴⊥ ⊢ 𝑄 ∶∶ ∅

4

𝑃 ⊢ (Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; (Δ)⊥ , Λ

5

𝑄 ⊢ (Γ)⊥ ; 𝑥 ∶ 𝐴

6

(𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ⊢ (Γ) ; (Δ) , Λ

1

Γ; Δ ⊢ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Λ

⊥

(IH on 3)
⊥

([cut?L] on 4 and 5)
(assumption)

(inversion on 1)
(IH on 2)
(IH on 3)
⊥

⊥

([cut?R] on 4 and 5)
(assumption)

⊥

2

Γ; 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ ∅

3

Γ, 𝑢 ∶ 𝐴; Δ ⊢ 𝑄 ∶∶ Λ

4

⊥

(inversion on 1)

𝑃 ⊢ (Γ) ; 𝑥 ∶ 𝐴
⊥

⊥

(IH on 2)
⊥

5

𝑄 ⊢ (Γ) , 𝑢 ∶ 𝐴 ; (Δ) , Λ

6

(𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ⊢ (Γ) ; (Δ) , Λ
⊥

(IH on 3)
⊥

([cut?L] on 4 and 5)

(  ⊆  ) Take any 𝑃 ∈  . Then, there are Γ, Δ s.t. 𝑃 ⊢ Γ; Δ. By showing that this implies (Γ) ; ∅ ⊢ 𝑃 ∶∶ Δ, we have 𝑃 ∈  . As
per the second item of Theorem 2.5, Rules [↶] and [↷] from Deﬁnition 2.6 are admissible in 𝜋𝖴𝖫𝖫. Therefore, it suﬃces to show
(Γ)⊥ ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ. We do so by induction on the structure of the proof of 𝑃 ⊢ Γ; Δ.
⊥

∙ [id]

∙ [𝟏]

∙ [⊥]

1
2

(Γ) ; 𝑥 ∶ 𝐴 ⊢↶
↷ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴

([idR])

3

⊥
(Γ)⊥ ; ∅ ⊢↶
↷ [𝑥 ↔ 𝑦] ∶∶ 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴

([↷])

1

𝑥⟨⟩.𝟎 ⊢ Γ; 𝑥 ∶ 𝟏

2

(Γ)⊥ ; ∅ ⊢↶
↷ 𝑥⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏

1

𝑥().𝑃 ⊢ Γ; Δ, 𝑥 ∶ ⊥

(assumption)

2

𝑃 ⊢ Γ; Δ

(inversion 1)

4
5

⊥

⊥

(assumption)
⊥

3

∙ [⊗]

[𝑥 ↔ 𝑦] ⊢ Γ; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥

(assumption)
([𝟏R])

⊥

(IH on 2)

⊥

([𝟏L] on 3)

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ
(Γ) ; 𝑥 ∶ 𝟏 ⊢↶
↷ 𝑥().𝑃 ∶∶ Δ
⊥

(Γ) ; ∅ ⊢↶
↷ 𝑥().𝑃 ∶∶ Δ, 𝑥 ∶ ⊥

1

(𝜈𝑦)𝑥⟨𝑦⟩.(𝑃 | 𝑄) ⊢

2

𝑃 ⊢ Γ; Δ, 𝑦 ∶ 𝐴

3

𝑄 ⊢ Γ; Δ′ , 𝑥 ∶ 𝐵

([↷] on 4)

Γ; Δ, Δ′ , 𝑥 ∶ 𝐴 ⊗ 𝐵

(assumption)

(inversion on 1)
18

## PDF page 19

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

(Γ)⊥ ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑦 ∶ 𝐴

(IH on 2)

5

′
(Γ)⊥ ; ∅ ⊢↶
↷ 𝑄 ∶∶ Δ , 𝑥 ∶ 𝐵

(IH on 3)

6

′
(Γ)⊥ ; ∅ ⊢↶
↷ (𝜈𝑦)𝑥⟨𝑦⟩(𝑃 | 𝑄) ∶∶ Δ, Δ , 𝑥 ∶ 𝐴 ⊗ 𝐵

1

𝑥(𝑦).𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴

2

𝑃 ⊢ Γ; Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵

&

3

𝐵

&

∙[ ]

4

(assumption)
(inversion on 1)

⊥

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑦 ∶ 𝐴, 𝑥 ∶ 𝐵
⊥

([⊗R] on 4 and 5)

(IH on 2)

⊥

4

(Γ) ; 𝑦 ∶ 𝐴 ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑥 ∶ 𝐵

([↶] on 3)

5

⊥
(Γ)⊥ ; ∅ ⊢↶
↷ 𝑥(𝑦).𝑃 ∶∶ Δ, 𝑥 ∶ 𝐴 ⊸ 𝐵
⏟⏟⏟

([⊸R] on 4)

𝐴 𝐵
&

∙ [⊕]

∙ [&]

1

𝑥 ⊲ 𝑗.𝑃 ⊢ Γ; Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

2

𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴𝑗

3

𝑗∈𝐼

(inversion on 1)

4

⊥

(IH on 2)

⊥

5

(Γ) ; ∅ ⊢↶
↷ 𝑥 ⊲ 𝑗.𝑃 ∶∶ Δ, 𝑥 ∶ ⊕{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

([⊕R] on 4 and 3)

1

𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ⊢ Γ; Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

(assumption)

2

∀𝑖 ∈ 𝐼. 𝑃𝑖 ⊢ Γ; Δ, 𝑥 ∶ 𝐴𝑖

3

∙ [copy]

∙ [!]

∀𝑖 ∈ 𝐼. (Γ) ; ∅ ⊢↶
↷ 𝑃𝑖 ∶∶ Δ, 𝑥 ∶ 𝐴𝑖

(IH on 2)

⊥

(Γ) ; ∅ ⊢↶
↷ 𝑥 ⊳ {𝑖 ∶ 𝑃𝑖 }𝑖∈𝐼 ∶∶ Δ, 𝑥 ∶ &{𝑖 ∶ 𝐴𝑖 }𝑖∈𝐼

([&R] on 3)

1

(𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

(assumption)

2

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ, 𝑥 ∶ 𝐴

(inversion on 1)

⊥

⊥

3

(Γ) , 𝑢 ∶ 𝐴 ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑥 ∶ 𝐴

(IH on 2)

4

(Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; 𝑥 ∶ 𝐴⊥ ⊢↶
↷ 𝑃 ∶∶ Δ

([↶] on 3)

5

(Γ)⊥ , 𝑢 ∶ 𝐴⊥ ; ∅ ⊢↶
↷ (𝜈𝑥)𝑢⟨𝑥⟩.𝑃 ∶∶ Δ

1

!𝑥(𝑦).𝑃 ⊢ Γ; 𝑥 ∶ !𝐴

2

𝑃 ⊢ Γ; 𝑦 ∶ 𝐴

([copyL] on 4)
(assumption)
(inversion on 1)

⊥

(IH on 2)

⊥

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ 𝑦 ∶ 𝐴

4

(Γ) ; ∅ ⊢↶
↷ !𝑥(𝑦).𝑃 ∶∶ 𝑥 ∶ !𝐴

([!R] on 3)

1

𝑃 {𝑥∕𝑢} ⊢ Γ; Δ, 𝑥 ∶ ?𝐴

(assumption)

2

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

3
4

∙ [cut]

(inversion on 1)

⊥

4

3

∙ [?]

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑥 ∶ 𝐴𝑗

(assumption)

⊥

(inversion on 1)

⊥

(Γ) , 𝑢 ∶ 𝐴 ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ
⊥

(Γ) ; 𝑥 ∶ !𝐴 ⊢↶
↷ 𝑃 {𝑥∕𝑢} ∶∶ Δ
(Γ) ; ∅ ⊢↶
↷ 𝑃 {𝑥∕𝑢} ∶∶ Δ, 𝑥 ∶ ?𝐴

1

(𝜈𝑥)(𝑃 | 𝑄) ⊢

2

𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴

3

𝑄 ⊢ Γ; Δ′ , 𝑥 ∶ 𝐴⊥

5
6
7

([!L] on 3)

⊥

5

4

(IH on 2)

⊥

([↷] on 4)

Γ; Δ, Δ′

(assumption)

(inversion on 1)

⊥

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ, 𝑥 ∶ 𝐴
⊥

(Γ) ; ∅ ⊢↶
↷ 𝑄 ∶∶ Δ , 𝑥 ∶ 𝐴
′

⊥

(Γ) ; 𝑥 ∶ 𝐴 ⊢↶
↷ 𝑄 ∶∶ Δ
⊥

(IH on 2)
⊥

(IH on 3)
([↶] on 5)

′

(Γ) ; ∅ ⊢ (𝜈𝑥)(𝑃 | 𝑄) ∶∶ Δ, Δ′

([cutRL] on 4 and 6)

↶
↷

19

## PDF page 20

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

∙ [cut?R]

1

(𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ⊢ Γ; Δ

2

𝑃 ⊢ Γ, 𝑢 ∶ 𝐴; Δ

3

𝑄 ⊢ Γ; 𝑥 ∶ 𝐴⊥

4
5

∙ [cut?L]

⊥

(inversion on 1)

⊥

(Γ) , 𝑢 ∶ 𝐴 ; ∅ ⊢↶
↷ 𝑃 ∶∶ Δ
⊥

(Γ) ; ∅ ⊢↶
↷ 𝑄 ∶∶ 𝑥 ∶ 𝐴

1

(𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ⊢ Γ; Δ
𝑃 ⊢ Γ; 𝑥 ∶ 𝐴

3

𝑄 ⊢ Γ, 𝑢 ∶ 𝐴; Δ
⊥

(Γ) ; ∅ ⊢↶
↷ 𝑃 ∶∶ 𝑥 ∶ 𝐴
⊥

([cut!R])
(assumption)

⊥

2

6

(IH on 3)

⊥

(Γ) ; ∅ ⊢↶
↷ (𝜈𝑢)(𝑃 | !𝑢(𝑥).𝑄) ∶∶ Δ

5

(IH on 2)

⊥

6

4

(assumption)

(inversion on 1)
⊥

(IH on 2)

⊥

(Γ) , 𝑢 ∶ 𝐴 ; ∅ ⊢↶
↷ 𝑄 ∶∶ Δ

(IH on 3)

⊥

(Γ) ; ∅ ⊢↶
↷ (𝜈𝑢)(!𝑢(𝑥).𝑃 | 𝑄) ∶∶ Δ

This concludes the proof of Theorem 3.1.

([cut!L])

□

We now turn our attention to  , the class of processes typable under the intuitionistic interpretation. The observation by Caires,
Pfenning and Toninho in [12] entails that  (𝜋𝖨𝖫𝖫-typable processes) should be a strict subset of  (𝜋𝖢𝖫𝖫⋆ -typable processes). We
formalize this fact by characterizing the intuitionistic fragment of 𝜋𝖴𝖫𝖫 (which coincides with 𝜋𝖨𝖫𝖫) by limiting its typing rules
and by showing that the class of processes typable in this fragment coincides with  (Theorem 3.2). It then follows that this class of
processes is strictly contained in  (𝜋𝖴𝖫𝖫-typable processes; Theorem 3.3). Since we have just shown that  =  , this formalizes
the fact that  is a strict subset of  .
Theorem 3.2 below formalizes two equivalent characterizations of the intuitionistic fragment of 𝜋𝖴𝖫𝖫 . One characterization is
based on the limited form of duality of 𝜋𝖨𝖫𝖫: the Rules [↶] and [↷] in Deﬁnition 2.6 may not be used. The other characterization
is based on the restricted two-sided form of 𝜋𝖨𝖫𝖫 sequents: the rules in Fig. 2 are limited to have exactly one channel/type pair on
the right. This requires the following auxiliary deﬁnition:
Deﬁnition 3.2 (𝑟-degree). The 𝑟-degree of a 𝜋𝖴𝖫𝖫 sequent Γ; Δ ⊢ 𝑃 ∶∶ Λ is the size of Λ. We say this sequent has 𝑟-degree |Λ|.
We now have:
Theorem 3.2. Given a process 𝑃 , the following are equivalent:
1. there are Γ, Δ, 𝑥 and 𝐴 such that Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴;
2. there are Γ, Δ and Λ such that Γ; Δ ⊢ 𝑃 ∶∶ Λ where all sequents in its proof have 𝑟-degree 1;
3. there are Γ, Δ and Λ such that Γ; Δ ⊢↶
↷ 𝑃 ∶∶ Λ where its proof never uses Rules [↶] and [↷].
Proof. We ﬁrst argue that items 1 and 2 are equivalent; then, we argue that items 2 and 3 imply each other:
(Equivalence of items 1 and 2) We show that restricting the sequents in 𝜋𝖴𝖫𝖫 to an 𝑟-degree of 1 entails the limitation of its rules
to a strict subset: those marked with ∗ in Fig. 2. This set of rules coincides with the set of rules for 𝜋𝖨𝖫𝖫 in Fig. 4. Hence, a proof of
typability in 𝜋𝖨𝖫𝖫 (item 1) can be replicated in 𝜋𝖴𝖫𝖫 with 𝑟-degree 1 (item 2) and vice versa. Because the proof for each rule follows
the same pattern, we only detail two cases: one without ∗ and one with ∗.
• Rule [ L] is not ∗-marked. Suppose we have a proof of typability in 𝜋𝖴𝖫𝖫 with 𝑟-degree 1 and suppose this includes an application
of [ L]. By assumption, this application’s antecedents have 𝑟-degree 1, so its consequence must have 𝑟-degree 2. This contradicts
the assumption that all sequents have 𝑟-degree 1, showing that Rule [ L] is not usable in this fragment of 𝜋𝖴𝖫𝖫.
• Rule [⊸L] is ∗-marked. By assumption, in any application of this rule its antecedents would have 𝑟-degree 1. Then, its consequence
also has 𝑟-degree 1, so this rule can be used without problems.

&

&

&

(Item 2 implies item 3) By Deﬁnition 2.6, the set of rules of 𝜋𝖴𝖫𝖫↶
↷ consists of only [↶], [↷], and the ∗-marked rules in Fig. 2.
In 𝜋𝖴𝖫𝖫↶
↷ , the only rules that alter the 𝑟-degrees in judgments are [↶] and [↷]. Hence, if these rules may not be used, proofs of
typability in 𝜋𝖴𝖫𝖫↶
↷ have a constant 𝑟-degree. Since all axioms of 𝜋𝖴𝖫𝖫↶
↷ (the ∗-marked Axioms [IdR] and [𝟏R] in Fig. 2) have 𝑟degree 1, this constant 𝑟-degree is 1. Therefore, a proof of typability in 𝜋𝖴𝖫𝖫↶
↷ without using [↶] and [↷] (item 3) can be replicated
exactly in 𝜋𝖴𝖫𝖫 with 𝑟-degree restricted to 1 (item 2).
(Item 3 implies item 2) The proof of equivalence of items 1 and 2 above shows that with 𝑟-degree 1 the only usable rules in 𝜋𝖴𝖫𝖫
are those marked with ∗ in Fig. 2. By Deﬁnition 2.6, without Rules [↶] and [↷], 𝜋𝖴𝖫𝖫↶
↷ consists only of these ∗-marked rules.
20

## PDF page 21

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Hence, a proof of typability in 𝜋𝖴𝖫𝖫 with 𝑟-degree restricted to 1 (item 2) can be replicated exactly in 𝜋𝖴𝖫𝖫↶
↷ without using [↶]
and [↷] (item 3). □
We may now state our ﬁnal result:
Theorem 3.3.  ⊊  .
Proof. Theorem 3.2 ensures that  ⊆  . To show that this inclusion is strict, we give a process 𝑃 ∈  such that 𝑃 ∉  . Assuming
a proof for 𝑢 ∶ 𝐵; ∅ ⊢ 𝑃 ′ ∶∶ 𝑧 ∶ 𝐴, let 𝑃 = 𝑥(𝑦).!𝑦(𝑧).𝑃 ′ {𝑥∕𝑢}; there are precisely three ways to prove 𝑃 ∈  : they follow from the
three ways to infer a receive in 𝜋𝖴𝖫𝖫 ([ R], [⊸R], and [⊗L]). The proofs are as follows:

&

𝑢 ∶ 𝐵; ∅ ⊢ 𝑃 ′ ∶∶ 𝑧 ∶ 𝐴

𝑢 ∶ 𝐵; ∅ ⊢ 𝑃 ′ ∶∶ 𝑧 ∶ 𝐴
[↶]
𝑢 ∶ 𝐵; 𝑧 ∶ 𝐴⊥ ⊢ 𝑃 ′ ∶∶ ∅
[?L]
𝑢 ∶ 𝐵; 𝑦 ∶ ?𝐴⊥ ⊢ !𝑦(𝑧).𝑃 ′ ∶∶ ∅
[?R]
∅; 𝑦 ∶ ?𝐴⊥ ⊢ !𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ 𝑥 ∶ ?𝐵 ⊥

[!R]

&

∅; ∅ ⊢ 𝑥(𝑦).!𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ 𝑥 ∶ (!𝐴)

[?R]

(?𝐵 ⊥ )

&

𝑢 ∶ 𝐵; ∅ ⊢ !𝑦(𝑧).𝑃 ′ ∶∶ 𝑦 ∶ !𝐴
∅; ∅ ⊢ !𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ 𝑦 ∶ !𝐴, 𝑥 ∶ ?𝐵 ⊥

[ R]

∅; ∅ ⊢ 𝑥(𝑦).!𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ 𝑥 ∶ (?𝐴⊥ ) ⊸ (?𝐵 ⊥ )

𝑢 ∶ 𝐵; ∅ ⊢ 𝑃 ′ ∶∶ 𝑧 ∶ 𝐴
[↶ ]
𝑢 ∶ 𝐵; 𝑧 ∶ 𝐴⊥ ⊢ 𝑃 ′ ∶∶ ∅
[?L]
𝑢 ∶ 𝐵; 𝑦 ∶ ?𝐴⊥ ⊢ !𝑦(𝑧).𝑃 ′ ∶∶ ∅
[!L]
∅; 𝑦 ∶ ?𝐴⊥ , 𝑥 ∶ !𝐵 ⊢ !𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ ∅
∅; 𝑥 ∶ (?𝐴⊥ ) ⊗ (!𝐵) ⊢ 𝑥(𝑦).!𝑦(𝑧).𝑃 ′ {𝑥∕𝑢} ∶∶ ∅

[⊸R]

[⊗L]

Clearly, all these proofs contain judgments of 𝑟-degree diﬀerent from 1 (ﬁrst case) or require using [↶ ]/[↷] (second and third cases).
Hence, by Theorem 3.2, 𝑃 ∉  . □
4. Analysis
Now that we have established characterizations for the intuitionistic and classical fragments of 𝜋𝖴𝖫𝖫 , we analyze the meaning of
these results and discuss possible extensions.
Our analysis is twofold. First, we consider the informal observation by Caires, Pfenning, and Toninho [12] that intuitionistic type
systems enforce the locality principle (§ 4.1); unlike the classical formulation, the intuitionistic fragment of 𝜋𝖴𝖫𝖫 (and thus 𝜋𝖨𝖫𝖫)
has a partial form of duality, which ensures that typability guarantees locality. Next, we discuss how 𝜋𝖴𝖫𝖫 can support alternative,
more expressive forms of parallel composition and restriction, and how such extensions transfer to classical or intuitionistic type
systems (§ 4.2); we will see that the complete duality of classical type systems allows for such extensions, while the rely-guarantee
reading of intuitionistic type systems cannot account for them.
4.1. Locality
Locality is a well-known principle in concurrency research [40]. The idea is that freshly created channels are local. Local channels
are mutable, in the sense that they can be used for receives. Once a channel has been transmitted to another location, it becomes
non-local, and thus immutable: it can only be used for sends—receives are no longer allowed. This makes locality particularly relevant
for giving formal semantics to distributed programming languages; a prime example is the join calculus [21], whose theory relies on
(and is deeply inﬂuenced by) the locality principle [20].
Locality also makes an appearance in other contexts. Honda and Laurent’s [27] correspondence between a typed 𝜋 -calculus and
polarized proof-nets enforces locality due to receives having negative polarity while received names may only be of positive polarity.
Also, Dal Lago et al.’s [17] typed 𝜋 -calculus with intersection types goes further: processes are hyperlocalized, meaning that there may
be no receives on free channels after a prior receive at all.
Neither the intuitionistic nor the classical interpretation guarantee full-ﬂedged locality through typing: both systems allow receives
on previously received channels. The exception is replicated receive, which is used to deﬁne a shared channel that can continuously
receive linear channels over which to perform a service. The intuitionistic interpretation guarantees locality for shared channels; in
other words, 𝜋𝖨𝖫𝖫 cannot type replicated receives on non-local channels.
The following example, taken from the work by Caires, Pfenning and Toninho [12], is typable in 𝜋𝖢𝖫𝖫⋆ but not in 𝜋𝖨𝖫𝖫:

(𝜈𝑥)(𝑥(𝑦).!𝑦(𝑧).𝑃 | (𝜈𝑞)𝑥⟨𝑞⟩.𝑄)
Consider the left process in the parallel composition, 𝑥(𝑦).!𝑦(𝑧).𝑃 . It ﬁrst receives a channel 𝑦 over channel 𝑥; then, it uses 𝑦 for
replicated receive, thus deﬁning it as a shared channel. In 𝜋𝖢𝖫𝖫⋆ , channel 𝑥 has type !𝐴 𝐵 . The intuitionistic variant of this type is
(!𝐴)⊥ ⊸ 𝐵 = ?𝐴⊥ ⊸ 𝐵 on the right of the typing judgment, and ?𝐴⊥ ⊗ 𝐵 ⊥ on the left. It is impossible to type a process with a channel
of such a type in 𝜋𝖨𝖫𝖫, because ‘?’ is not a connective in the intuitionistic system.

&

21

## PDF page 22

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

The fact that 𝜋𝖨𝖫𝖫 cannot type non-local shared channels—due to the absence of a dual for ‘!’—suggests that there should be
another kind of non-local channels that 𝜋𝖨𝖫𝖫 cannot type: there is no dual for 𝟏. Indeed, 𝜋𝖨𝖫𝖫 cannot type empty sends on previously
received channels, a feature that is not observed in [12]. The following example is typable in 𝜋𝖢𝖫𝖫⋆ but not in 𝜋𝖨𝖫𝖫:

𝑥(𝑦).𝑥().𝑦⟨⟩.𝟎
In 𝜋𝖢𝖫𝖫⋆ , the type of 𝑥 in this process is 𝟏 ⊥. The intuitionistic variant of this type is 𝟏⊥ ⊸ ⊥ = ⊥ ⊸ ⊥ on the right of the typing
judgment, and ⊥ ⊗ 𝟏 on the left. This process is not typable in 𝜋𝖨𝖫𝖫, because ⊥ is not an intuitionistic proposition and so the type
system has no rules to type ⊥ channels. We make this observation more precise by giving an alternative proof to Theorem 3.3 ( ⊊  )
based on this observation:

&

Alternative proof of Theorem 3.3. By Theorem 3.2, it is suﬃcient to give 𝑃 ∈  such that 𝑃 ∉  . Let 𝑃 ∶= 𝑥(𝑦).𝑥().𝑦⟨⟩.𝟎. There
are three ways to prove that 𝑃 ∈  :
[𝟏R]

Γ; ∅ ⊢ 𝑦⟨⟩.𝟎 ∶∶ 𝑦 ∶ 𝟏
[⊥R]
Γ; ∅ ⊢ 𝑥().𝑦⟨⟩.𝟎 ∶∶ 𝑦 ∶ 𝟏, 𝑥 ∶ ⊥
[ R]
Γ; ∅ ⊢ 𝑥(𝑦).𝑥().𝑦⟨⟩.𝟎 ∶∶ 𝑥 ∶ 𝟏 𝑥 ∶ ⊥
&

&

[⊥L]

Γ; 𝑦 ∶ ⊥ ⊢ 𝑦⟨⟩.𝟎 ∶∶ ∅
[𝟏L]
Γ; 𝑦 ∶ ⊥, 𝑥 ∶ 𝟏 ⊢ 𝑥().𝑦⟨⟩.𝟎 ∶∶ ∅
[⊗L]
Γ; 𝑥 ∶ ⊥ ⊗ 𝟏 ⊢ 𝑥(𝑦).𝑥().𝑦⟨⟩.𝟎 ∶∶ ∅

[⊥L]

Γ; 𝑦 ∶ ⊥ ⊢ 𝑦⟨⟩.𝟎 ∶∶ ∅
[⊥R]
Γ; 𝑦 ∶ ⊥ ⊢ 𝑥().𝑦⟨⟩.𝟎 ∶∶ 𝑥 ∶ ⊥
[⊸Rl]
Γ; ∅ ⊢ 𝑥(𝑦).𝑥().𝑦⟨⟩.𝟎 ∶∶ 𝑥 ∶ ⊥ ⊸ ⊥

Clearly, all these proofs contain judgments of 𝑟-degree diﬀerent from 1. Hence, by Theorem 3.2, 𝑃 ∉  .

□

Based on these two proofs for Theorem 3.3, we have corroborated Caires et al.’s observation on locality, and extended it to the
case of empty sends and receives.
Judgments, revisited As already discussed, ‘⊥’ and ‘?’ are not propositions in 𝜋𝖨𝖫𝖫; the absence of rules for them in 𝜋𝖨𝖫𝖫 is an inherent
consequence of the form of its judgments. As shown by Theorem 3.2, rules for ‘?’ and ‘⊥’ are an impossibility when judgments are
required to have exactly one assignment (channel/proposition) on the right. Theorem 3.2 also shows this is closely related to duality,
which is not total in the intuitionistic interpretation (i.e., the duals for ‘𝟏’ and ‘!’ given by Deﬁnition 2.2 are not propositions in 𝜋𝖨𝖫𝖫).
In the classical case, the type system is symmetrical (as shown by a support for [↶]/[↷]-rules), while the intuitionistic type system
is asymmetrical.
Concerning ‘⊥’, the judgmental presentation of intuitionistic linear logic in [6] deﬁnes an alternative approach, which allows
deriving ‘⊥’ as ‘multiplicative contradiction’ by using a judgmental account of possibility under which resources are used zero times.
4.2. Parallel composition and restriction
The type systems we have discussed so far are rather restrictive in terms of how processes can be composed and connected: there
is only the cut-rule which composes and connects two processes that have exactly one channel of dual type in common. Indeed, the
cut-rule jointly handles constructs for parallel composition and restriction, which contrasts with many non-logical type systems for
the 𝜋 -calculus (e.g., [36,35,54]) where parallel composition and restriction typically have a dedicated rule each.
In this section we discuss extensions to the type systems that decompose cut into two separate rules: mix for parallel composition,
and cycle for channel connection (restriction). As we will see, these notions form another clear distinction point between CurryHoward interpretations of classical and intuitionistic linear logic.
4.2.1. Independent parallel composition
Caires et al. [12] discuss an alternative form of parallel composition. In the intuitionistic interpretation, the so-called independent
parallel composition connects (i) an arbitrary process 𝑄 with (ii) a process 𝑃 with a channel of type 𝟏 on the right; it is derivable in
the silent interpretation of 𝟏, in which Axioms [𝟏R] and [⊥L] type the inactive process 𝟎 and Rules [⊥R] and [𝟏L] leave processes
untouched. This way, the rules for 𝟏 would be the following (the rules for ⊥ are similar):
[𝟏L]

[𝟏R]

Γ; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ, 𝑥 ∶ 𝟏 ⊢ 𝑃 ∶∶ Λ

Γ; ∅ ⊢ 𝟎 ∶∶ 𝑥 ∶ 𝟏

In this case, the correspondence relies on structural congruences in processes and proofs (suitably extended), rather than on
reduction. To obtain independent parallel composition, one uses Rule [cut] to connect the right channel of 𝑃 with a corresponding
(dual) channel in 𝑄, which is exposed on the left using Rule [𝟏L]:

Γ; Δ′ ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐶
Γ; Δ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝟏

Γ; Δ′ , 𝑧 ∶ 𝟏 ⊢ 𝑄 ∶∶ 𝑥 ∶ 𝐶

Γ; Δ, Δ′ ⊢ (𝜈𝑧)(𝑃 | 𝑄) ∶∶ 𝑥 ∶ 𝐶

[𝟏L]
[cutRL]

The requirement that process 𝑃 above has a channel of type 𝟏 on the right is rather restrictive: only left-rules can be used for typing,
so 𝑃 must be a process that relies on multiple behaviors but can oﬀer a behavior of type 𝟏. Related to this constraint, Caires et al. show
22

## PDF page 23

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

that in the silent interpretation Γ; Δ ⊢ 𝑃 ∶∶ 𝑥 ∶ 𝐴 implies Γ; Δ, 𝑥 ∶ 𝐴⊥ ⊢ 𝑃 ∶∶ 𝑧 ∶ 𝟏, for some fresh 𝑧, provided that 𝐴 is exponentialfree and 𝟏⊥ = 𝟏 (cf. also below) [12, Prop. 5.1]. However, this “movement” from the right to the left is only possible under the absence
of the identity axiom, which is in turn necessary when considering, e.g., behavioral polymorphism [9]. Indeed, given any type 𝐴 we
can prove ∅; 𝑥 ∶ 𝐴 ⊢ [𝑥 ↔ 𝑦] ∶∶ 𝑦 ∶ 𝐴 using the identity axiom, but there is no way to prove ∅; 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥ ⊢ [𝑥 ↔ 𝑦] ∶∶ 𝑧 ∶ 𝟏.
4.2.2. Parallel composition: mix
Girard [23] discusses an extension of linear logic that allows the combination of two independent proofs. Wadler gives a CurryHoward interpretation of this rule as the parallel composition of two processes that have no channels in common [56]. In [5], Caires
complements the extension with an axiom that types the inactive process 𝟎 with an empty context.
⋆
We now deﬁne 𝜋𝖢𝖫𝖫⋆
+ , which is 𝜋𝖢𝖫𝖫 extended with this form of parallel composition. The only change is the addition of the
following rules:
[mix]

𝑃 ⊢ Γ; Δ

𝑄 ⊢ Γ; Δ′

[empty]

𝑃 | 𝑄 ⊢ Γ; Δ, Δ′

𝟎 ⊢ Γ; ∅

We straightforwardly deﬁne 𝜋𝖴𝖫𝖫+ as a similar extension of 𝜋𝖴𝖫𝖫 by adding the following rules:
[mix]

Γ; Δ ⊢ 𝑃 ∶∶ Λ
Γ; Δ′ ⊢ 𝑄 ∶∶ Λ′
′
Γ; Δ, Δ ⊢ 𝑃 | 𝑄 ∶∶ Λ, Λ′

[empty]

Γ; ∅ ⊢ 𝟎 ∶∶ ∅

It is easy to see that Theorem 3.1—the equivalence of 𝜋𝖢𝖫𝖫⋆ and 𝜋𝖴𝖫𝖫—still holds for 𝜋𝖢𝖫𝖫⋆
+ and 𝜋𝖴𝖫𝖫+ . Following the reasoning
of Theorem 3.2—the characterization of 𝜋𝖨𝖫𝖫 in terms of 𝜋𝖴𝖫𝖫—, Rules [mix] and [empty] do not belong to the intuitionistic
fragment of 𝜋𝖴𝖫𝖫+ : Rule [empty] has 𝑟-degree 0, and if the antecedents of Rule [mix] both have 𝑟-degree 1 then its consequence
would have 𝑟-degree 2. This leads us to conclude that the more ﬂexible ways of composition induced by [mix] cannot be supported
by intuitionistic systems.
The equivalence of 𝟏 and ⊥ Caires [5] notes that, in the classical setting, Rules [mix] and [empty] make it possible to prove ⊥ ⊸ 𝟏
and 𝟏 ⊸ ⊥ (where ⊸ denotes linear implication). Hence, it is possible to consider 𝟏 and ⊥ equivalent, writing a single symbol (say, ‘∙’)
for either—very similar to the singular, self-dual type 𝖾𝗇𝖽 in standard session types. The work of Atkey et al. [1] is also relevant, as it
develops a detailed treatment of the conﬂation of ⊥ and 𝟏. Conﬂation is not always desirable: the work of Qian et al. [47] addresses
the shortcomings of considering [mix] for faithfully representing stateful client-server behaviors.
4.2.3. Channel connection: cycle
The cut-rule only allows us to connect two processes on a single channel. Although this neatly guarantees deadlock freedom, it
prevents many deadlock-free processes from being typable (see [18] for comparisons between these classes of processes). For example,
we can construct a process (𝜈𝑥)(𝜈𝑦)(𝑃 | 𝑄) where

𝑃 ∶= (𝜈𝑢)𝑥⟨𝑢⟩.(𝑦(𝑣).(𝑢().𝑣().𝟎 | 𝑦⟨⟩.𝟎) | 𝑥⟨⟩.𝟎) and
𝑄 ∶= 𝑥(𝑤).(𝜈𝑧)𝑦⟨𝑧⟩.(𝑥().𝑧⟨⟩.𝟎 | 𝑦().𝑤⟨⟩.𝟎)
This process is deadlock free, but not typable using cut.
Connecting on multiple channels at once does have the danger of introducing the circular dependencies between sessions that are
at the heart of deadlocked processes. For example, suppose that we replace 𝑃 with 𝑃 ′ , where we swap the send on 𝑥 and the receive
on 𝑦:

𝑃 ′ ∶= 𝑦(𝑣).(𝜈𝑢)𝑥⟨𝑢⟩.(𝑢().𝑣().𝟎 | 𝑦⟨⟩.𝟎 | 𝑥⟨⟩.𝟎).
Now, the composed and connected process would be stuck with 𝑃 ′ waiting for a receive on 𝑦 and 𝑄 for a receive on 𝑥.
Dardha and Gay [14] present a session type system based on classical linear logic in which they replace the cut-rule with a rule
called [cycle], which connects two channels of dual types in the same judgment. This new rule has a side-condition that allows
⋆
their type system to maintain deadlock freedom. We can deﬁne 𝜋𝖢𝖫𝖫⋆
++ as an extension of 𝜋𝖢𝖫𝖫+ with the cycle-rule. Since we are
speciﬁcally interested in this form of channel restriction, below we abstract away from Dardha and Gay’s side-condition by simply
writing 𝜙.
Note that we ﬁrst require some modiﬁcations to restriction and reduction, based on [54]. Restriction in 𝜋𝖢𝖫𝖫⋆
++ should involve
two channel names, i.e. writing (𝜈𝑥𝑦)𝑃 instead of (𝜈𝑥)𝑃 , because the involved channels appear in the same judgment and thus need
to be uniquely named. Indeed, (𝜈𝑥𝑦)𝑃 says that 𝑥 and 𝑦 are the two endpoints of the same channel in 𝑃 .
[cycle]

𝑃 ⊢ Γ; Δ, 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥
(𝜈𝑥𝑦)𝑃 ⊢ Γ; Δ

𝜙

23

## PDF page 24

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

Deﬁning 𝜋𝖴𝖫𝖫++ as a similar extension of 𝜋𝖴𝖫𝖫+ is again straightforward. Similarly to the cut-rules in Fig. 3, we add four rules that
operate on diﬀerent sides of the typing judgment:
[cycleRL]

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴
Γ; Δ ⊢ (𝜈𝑦𝑥)𝑃 ∶∶ Λ

𝜙

[cycleRR]

[cycleLR]

Γ; Δ, 𝑥 ∶ 𝐴 ⊢ 𝑃 ∶∶ Λ, 𝑦 ∶ 𝐴
Γ; Δ ⊢ (𝜈𝑥𝑦)𝑃 ∶∶ Λ

𝜙

Γ; Δ ⊢ 𝑃 ∶∶ Λ, 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥
Γ; Δ ⊢ (𝜈𝑥𝑦)𝑃 ∶∶ Λ

𝜙

[cycleLL]

Γ; Δ, 𝑥 ∶ 𝐴, 𝑦 ∶ 𝐴⊥ ⊢ 𝑃 ∶∶ Λ
Γ; Δ ⊢ (𝜈𝑥𝑦)𝑃 ∶∶ Λ

𝜙

Again, it is easy to see that Theorem 3.1 still holds for 𝜋𝖢𝖫𝖫⋆
++ and 𝜋𝖴𝖫𝖫++ . Interestingly, by virtue of Theorem 3.2, Rule [cycleLL]
is the only rule allowed in the intuitionistic fragment of 𝜋𝖴𝖫𝖫++ , because it does not aﬀect the right-hand side of the judgment (as
Λ can have 𝑟-degree 1). Unfortunately, this rule is useless for 𝜋𝖨𝖫𝖫: it requires two channels of dual types, but duality is not total in
𝜋𝖨𝖫𝖫.
Adding mix- and cycle-rules enables a more ﬂexible formulation of structural congruence, as well as more ﬂexible typing of sends.
For one, e.g., Rule [⊗R] would only require a single continuation that provides both the payload and the continuation of the send.
We can then add structural congruence rules that are found in traditional, untyped settings, such as 𝑃 | 𝑄 ≡ 𝑄 | 𝑃 and 𝑃 | 𝟎 ≡ 𝑃 .
5. Conclusion
Curry-Howard correspondences between linear logic and session types explain how linear logic can provide an ample, principled framework to conceive diﬀerent typing disciplines for message-passing processes speciﬁed in the 𝜋 -calculus. There is no single
canonical interpretation, as there are multiple interpretations, depending on design choices involving, e.g., the logical connectives
considered and their respective process operators.
In this context, this paper has pursued a very concrete goal: to formally compare the interpretations of classical and intuitionistic
linear logic as session types. The comparison results reported in Section 3 are an indispensable step to consolidating the logical
foundations of message-passing concurrency; they also have a number of relevant ramiﬁcations, as reported in Section 4.
Our technical approach to this goal relies on a fragment of Girard’s Logic of Unity (LU) [24] as a basis to develop 𝜋𝖴𝖫𝖫: a new
session type system that can type all processes typable in both 𝜋𝖢𝖫𝖫⋆ and 𝜋𝖨𝖫𝖫, which correspond to classical and intuitionistic
interpretations, respectively. The linear logic 𝖴𝖫𝖫, on which the type system 𝜋𝖴𝖫𝖫 stands, is an admittedly modest fragment of
Girard’s LU. Still, we emphasize that 𝜋𝖴𝖫𝖫 is suﬃcient for our purposes, as it gives us a fair and rigorous basis for addressing our
declared goal of comparing type systems based on diﬀerent linear logics. The development of computational interpretations for LU,
including but going beyond 𝖴𝖫𝖫 and 𝜋𝖴𝖫𝖫, is surely an interesting direction but one that lies outside the scope of our work.
In 𝜋𝖨𝖫𝖫, judgments have a particular reading in which a process relies on several channels (on the left of judgments) and guarantees
a behavior along a single designated channel (on the right). 𝜋𝖴𝖫𝖫 uses two-sided judgments as well, similar to LU. However, 𝜋𝖴𝖫𝖫
does not retain 𝜋𝖨𝖫𝖫’s rely-guarantee reading, because it does not distinguish between the sides of its sequents. The consequence
is that 𝜋𝖴𝖫𝖫 supports a full duality relation, as opposed to 𝜋𝖨𝖫𝖫. This allows 𝜋𝖴𝖫𝖫 to mimic the explicit duality in the singlesided 𝜋𝖢𝖫𝖫⋆ . On the other hand, restricting the right side of 𝜋𝖴𝖫𝖫 ’s judgments to exactly one channel—thus limiting support for
duality—characterizes a fragment of 𝜋𝖴𝖫𝖫’s typing rules that precisely coincides with 𝜋𝖨𝖫𝖫.
Our results conﬁrm the informal observation by Caires et al. [12] that the diﬀerence between session type systems based on
classical and intuitionistic linear logic is in the enforcement of locality of shared names. We have not only conﬁrmed that 𝜋𝖨𝖫𝖫
cannot type processes that do not respect locality for shared channels: a new insight obtained in this paper is that 𝜋𝖨𝖫𝖫 also forbids
empty sends on received channels. Our results show that these constraints are a consequence of the strict requirement that 𝜋𝖨𝖫𝖫’s
typing judgments must have exactly one channel/type on the right. 𝜋𝖴𝖫𝖫 and 𝜋𝖢𝖫𝖫⋆ do not have such constraints and thus fully
support duality.
Our work can be seen as providing a technical answer to long-suspected but fuzzily understood diﬀerences between intuitionistic
and classical interpretations of linear logic (here represented by 𝜋𝖨𝖫𝖫 and 𝜋𝖢𝖫𝖫⋆ , respectively) concerning the role of duality (implicit
in 𝜋𝖨𝖫𝖫, explicit in 𝜋𝖢𝖫𝖫⋆ ) and locality of shared channels (enforced by 𝜋𝖨𝖫𝖫 but not by 𝜋𝖢𝖫𝖫⋆ ). We believe it is important to give
a formal footing to this kind of informal observations. Formally stating the required comparisons is not obvious, and insightful in
itself, as implicit assumptions may emerge in the process. In this respect, we adopted 𝜋𝖴𝖫𝖫 as it provides an eﬀective yardstick for
comparisons, independent from both 𝜋𝖨𝖫𝖫 and 𝜋𝖢𝖫𝖫⋆ , and based on an already existing framework (Girard’s LU). In future work, it
would be interesting to explore other approaches towards our technical results (Theorems 3.1 and 3.3).
If one adopts the stance that a permissive type system is also an expressive one, then the results from our comparisons (notably,
the strict inclusion of 𝜋𝖨𝖫𝖫 in 𝜋𝖴𝖫𝖫) indicate that classical linear logic induces a more expressive class of typed processes than
intuitionistic linear logic. There is an alternative stance, which considers less permissive type systems as being more precise than other,
more permissive type system. The locality property for shared channels, as enforced by intuitionistic interpretations, is a case in point
here. In our view, the connection between permissiveness, expressiveness, and precision is an interesting question, which largely
depends on the value of the intended properties. Indeed, the precision of type systems derived from intuitionistic interpretations
may not be meaningful in settings/applications where locality is simply not a relevant property. On the other hand, the conditions
that make intuitionistic interpretations less permissive can always be imposed on more permissive interpretations as side-conditions,
24

## PDF page 25

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

making them more precise. Finally, as observed by Caires et al. [12], it is surely remarkable that intuitionistic interpretations of
session types precisely capture a principle such as locality of shared names, which was known and exploited in diﬀerent contexts [40]
long before these Curry-Howard interpretations were ﬁrst spelled out [7].
To conclude, we believe that LU and 𝜋𝖴𝖫𝖫 have other useful applications besides the comparison of type systems based on
vanilla linear logic; our discussion of more expressive parallel composition and channel connection in Section 4 corroborates this.
We have been able to rely on 𝜋𝖴𝖫𝖫 to study the eﬀects of mix- and cycle-rules in the intuitionistic interpretation by transferring
extensions of the classical interpretation to 𝜋𝖴𝖫𝖫 and following the methodology of our comparison results. In this case, extensions
of intuitionistic interpretations with such rules do not make sense due to the constraints of typing judgments. This makes sense from
a logical perspective: intuitionistic argumentation is based on a constructivist philosophy in which putting unrelated things together
([mix]) and then relating them later ([cycle]) may not be acceptable.
CRediT authorship contribution statement
Bas van den Heuvel: Writing – original draft, Formal analysis, Conceptualization. Jorge A. Pérez: Writing – original draft, Formal
analysis, Conceptualization.
Declaration of competing interest
The authors declare that they have no known competing ﬁnancial interests or personal relationships that could have appeared to
inﬂuence the work reported in this paper.
Acknowledgements
We are grateful to Juan C. Jaramillo, Joseph Paulus, and Revantha Ramanayake for helpful discussions. We would also like to thank
the anonymous reviewers of PLACES’20 and JLAMP for their detailed suggestions, which were helpful to improve the presentation.
References
[1] Robert Atkey, Sam Lindley, J. Garrett Morris, Conﬂation confers concurrency, in: Sam Lindley, Conor McBride, Phil Trinder, Don Sannella (Eds.), A List of
Successes That Can Change the World: Essays Dedicated to Philip Wadler on the Occasion of His 60th Birthday, in: Lecture Notes in Computer Science, Springer
International Publishing, Cham, 2016, pp. 32–55.
[2] Michele Boreale, On the expressiveness of internal mobility in name-passing calculi, Theor. Comput. Sci. 195 (2) (March 1998) 205–226.
[3] Andrew Barber, Gordon D. Plotkin, Dual Intuitionistic Linear Logic, Technical Report ECS-LFCS-96-347, University of Edinburgh, School of Informatics, Laboratory
for Foundations of Computer Science, Edinburgh, September 1996.
[4] Stephanie Balzer, Frank Pfenning, Manifest sharing with session types, Proc. ACM Program. Lang. 37 (August 2017) 37:1–37:29.
[5] Luís Caires, Types and logic, concurrency and non-determinism, Technical Report MSR-TR-2014-104, in: Essays for the Luca Cardelli Fest, Microsoft Research,
September 2014.
[6] Bor-Yuh Evan Chang, Kaustuv Chaudhuri, Frank Pfenning, A judgmental analysis of linear logic, Technical Report CMU-CS-03-131R, Department of Computer
Science, Carnegie Mellon University, November 2003.
[7] Luís Caires, Frank Pfenning, Session types as intuitionistic linear propositions, in: Paul Gastin, François Laroussinie (Eds.), CONCUR 2010 - Concurrency Theory,
in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2010, pp. 222–236.
[8] Luís Caires, Jorge A. Pérez, Linearity, control eﬀects, and behavioral types, in: Hongseok Yang (Ed.), Programming Languages and Systems, in: Lecture Notes in
Computer Science, Springer, Berlin, Heidelberg, 2017, pp. 229–259.
[9] Luís Caires, Jorge A. Pérez, Frank Pfenning, Bernardo Toninho, Behavioral polymorphism and parametricity in session-based communication, in: Matthias
Felleisen, Philippa Gardner (Eds.), Programming Languages and Systems, Springer, Berlin, Heidelberg, 2013, pp. 330–349.
[10] Luís Caires, Jorge A. Pérez, Frank Pfenning, Bernardo Toninho, Domain-aware session types, in: Fokkink Wan, Rob van Glabbeek (Eds.), 30th International
Conference on Concurrency Theory (CONCUR 2019), Dagstuhl, Germany, in: Leibniz International Proceedings in Informatics (LIPIcs), vol. 140, Schloss Dagstuhl–
Leibniz-Zentrum fuer Informatik, 2019, pp. 39:1–39:17.
[11] Luís Caires, Frank Pfenning, Bernardo Toninho, Towards concurrent type theory, in: Proceedings of the 8th ACM SIGPLAN Workshop on Types in Language
Design and Implementation, ACM, January 2012, pp. 1–12.
[12] Luís Caires, Frank Pfenning, Bernardo Toninho, Linear logic propositions as session types, Math. Struct. Comput. Sci. 26 (3) (March 2016) 367–423.
[13] Henry DeYoung, Luís Caires, Frank Pfenning, Bernardo Toninho, Cut reduction in linear logic as asynchronous session-typed communication, in: Patrick Cégielski,
Arnaud Durand (Eds.), Computer Science Logic (CSL’12) - 26th International Workshop/21st Annual Conference of the EACSL, Dagstuhl, Germany, in: Leibniz
International Proceedings in Informatics (LIPIcs), vol. 16, Schloss Dagstuhl–Leibniz-Zentrum fuer Informatik, 2012, pp. 228–242.
[14] Ornela Dardha, Simon J. Gay, A new linear logic for deadlock-free session-typed processes, in: Christel Baier, Ugo Dal Lago (Eds.), Foundations of Software
Science and Computation Structures, in: Lecture Notes in Computer Science, Springer International Publishing, 2018, pp. 91–109.
[15] Ornela Dardha, Elena Giachino, Davide Sangiorgi, Session types revisited, Inf. Comput. 256 (October 2017) 253–286.
[16] Romain Demangeon, Kohei Honda, Full abstraction in a subtyped pi-calculus with linear types, in: Joost-Pieter Katoen, Barbara König (Eds.), CONCUR 2011 –
Concurrency Theory, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2011, pp. 280–296.
[17] Ugo Dal Lago, Marc de Visme, Damiano Mazza, Akira Yoshimizu, Intersection types and runtime errors in the pi-calculus, Proc. ACM Program. Lang. 3 (POPL)
(January 2019) 7:1–7:29.
[18] Ornela Dardha, Jorge A. Pérez, Comparing type systems for deadlock freedom, J. Log. Algebraic Methods Program. 124 (January 2022) 100717.
[19] Dan Frumin, Emanuele D’Osualdo, Bas van den Heuvel, Jorge A. Pérez, A bunch of sessions: a propositions-as-sessions interpretation of bunched implications in
channel-based concurrency, Proc. ACM Program. Lang. 6 (OOPSLA2) (October 2022) 155:841–155:869.
[20] Cédric Fournet, Georges Gonthier, Jean-Jacques Levy, Luc Maranget, Didier Rémy, A calculus of mobile agents, in: Ugo Montanari, Vladimiro Sassone (Eds.),
CONCUR ’96: Concurrency Theory, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 1996, pp. 406–421.
[21] Cédric Fournet, Cosimo Laneve, Bisimulations in the join-calculus, Theor. Comput. Sci. 266 (1) (September 2001) 569–603.
25

## PDF page 26

Journal of Logical and Algebraic Methods in Programming 142 (2025) 101004

B. van den Heuvel and J.A. Pérez

[22] Simon J. Gay, Nils Gesbert, António Ravara, Session types as generic process types, in: Johannes Borgström, Silvia Crafa (Eds.), Proceedings Combined 21st
International Workshop on Expressiveness in Concurrency, EXPRESS 2014, and 11th Workshop on Structural Operational Semantics, SOS 2014, Rome, Italy, 1st
September 2014, in: EPTCS, vol. 160, 2014, pp. 94–110.
[23] Jean-Yves Girard, Linear logic, Theor. Comput. Sci. 50 (1) (January 1987) 1–101.
[24] Jean-Yves Girard, On the unity of logic, Ann. Pure Appl. Log. 59 (3) (February 1993) 201–217.
[25] Jean-Yves Girard, Yves Lafont, Linear logic and lazy computation, in: Hartmut Ehrig, Robert A. Kowalski, Giorgio Levi, Ugo Montanari (Eds.), TAPSOFT’87:
Proceedings of the International Joint Conference on Theory and Practice of Software Development, Pisa, Italy, March 23-27, 1987, Volume 2: Advanced
Seminar on Foundations of Innovative Software Development II and Colloquium on Functional and Logic Programming and Speciﬁcations (CFLP), in: Lecture
Notes in Computer Science, vol. 250, Springer, 1987, pp. 52–66.
[26] Daniele Gorla, A taxonomy of process calculi for distribution and mobility, Distrib. Comput. 23 (4) (December 2010) 273–299.
[27] Kohei Honda, Olivier Laurent, An exact correspondence between a typed pi-calculus and polarised proof-nets, Theor. Comput. Sci. 411 (22) (May 2010)
2223–2238.
[28] Kohei Honda, Types for dyadic interaction, in: Eike Best (Ed.), CONCUR’93, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 1993,
pp. 509–523.
[29] Bas van den Heuvel, Jorge A. Pérez, Session type systems based on linear logic: classical versus intuitionistic, in: Stephanie Balzer, Luca Padovani (Eds.),
Proceedings of the 12th International Workshop on Programming Language Approaches to Concurrency- and Communication-cEntric Software, Dublin, Ireland,
26th, April 2020, in: Electronic Proceedings in Theoretical Computer Science, vol. 314, Open Publishing Association, 2020, pp. 1–11.
[30] Bas van den Heuvel, Jorge A. Pérez, Deadlock freedom for asynchronous and cyclic process networks, in: Julien Lange, Anastasia Mavridou, Larisa Saﬁna, Alceste
Scalas (Eds.), Proceedings 14th Interaction and Concurrency Experience, Online, 18th, June 2021, in: Electronic Proceedings in Theoretical Computer Science,
vol. 347, Open Publishing Association, 2021, pp. 38–56.
[31] Ross Horne, Luca Padovani, A logical account of subtyping for session types, Electronic Proceedings in Theoretical Computer Science 378 (April 2023) 26–37.
[32] Bas van den Heuvel, Joseph W.N. Paulus, Daniele Nantes-Sobrinho, Jorge A. Pérez, Typed non-determinism in functional and concurrent calculi, in: Chung-Kil
Hur (Ed.), Programming Languages and Systems, in: Lecture Notes in Computer Science, Springer Nature, Singapore, 2023, pp. 112–132.
[33] Kohei Honda, Vasco T. Vasconcelos, Makoto Kubo, Language primitives and type discipline for structured communication-based programming, in: Chris Hankin
(Ed.), Programming Languages and Systems, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 1998, pp. 122–138.
[34] Wen Kokke, Fabrizio Montesi, Marco Peressotti, Better late than never: a fully-abstract semantics for classical processes, Proc. ACM Program. Lang. 24 (January
2019) 1.
[35] Naoki Kobayashi, Type systems for concurrent programs, in: Bernhard K. Aichernig, Tom Maibaum (Eds.), Formal Methods at the Crossroads. From Panacea to
Foundational Support: 10th Anniversary Colloquium of UNU/IIST, the International Institute for Software Technology of the United Nations University, Lisbon,
Portugal, March 18-20, 2002. Revised Papers, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2003, pp. 439–453.
[36] Naoki Kobayashi, Benjamin C. Pierce, David N. Turner, Linearity and the pi-calculus, ACM Trans. Program. Lang. Syst. 21 (5) (September 1999) 914–947.
[37] Dimitrios Kouzapas, Jorge A. Pérez, Nobuko Yoshida, On the relative expressiveness of higher-order session processes, Inf. Comput. 268 (October 2019) 104433.
[38] Olivier Laurent, Around classical and intuitionistic linear logics, in: Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science, LICS
’18, ACM, New York, NY, USA, 2018, pp. 629–638.
[39] Sam Lindley, J. Garrett Morris, Talking bananas: structural recursion for session types, in: Proceedings of the 21st ACM SIGPLAN International Conference on
Functional Programming, ICFP 2016, ACM, New York, NY, USA, 2016, pp. 434–447.
[40] Massimo Merro, Locality and polyadicity in asynchronous name-passing calculi, in: Jerzy Tiuryn (Ed.), Foundations of Software Science and Computation
Structures, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2000, pp. 238–251.
[41] Robin Milner, Joachim Parrow, David Walker, A calculus of mobile processes, I, Inf. Comput. 100 (1) (September 1992) 1–40.
[42] Jorge A. Pérez, Luís Caires, Frank Pfenning, Bernardo Toninho, Linear logical relations for session-based concurrency, in: Helmut Seidl (Ed.), Programming
Languages and Systems, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2012, pp. 539–558.
[43] Jorge A. Pérez, Higher-Order Concurrency: Expressiveness and Decidability Results, PhD thesis, University of Bologna, Italy, May 2010.
[44] Jorge A. Pérez, The challenge of typed expressiveness in concurrency, in: Albert Elvira, Ivan Lanese (Eds.), Formal Techniques for Distributed Objects, Components,
and Systems, in: Lecture Notes in Computer Science, Springer International Publishing, Cham, 2016, pp. 239–247.
[45] Kirstin Peters, Comparing process calculi using encodings, Electronic Proceedings in Theoretical Computer Science 300 (August 2019) 19–38.
[46] Joseph W.N. Paulus, Jorge A. Pérez, Daniele Nantes-Sobrinho, Termination in concurrency, revisited, in: Santiago Escobar, Vasco T. Vasconcelos (Eds.), International Symposium on Principles and Practice of Declarative Programming, PPDP 2023, Lisboa, Portugal, October 22-23, 2023, ACM, 2023, pp. 3:1–3:14.
[47] Zesen Qian, G.A. Kavvos, Lars Birkedal, Client-server sessions in linear logic, Proc. ACM Program. Lang. 5 (ICFP) (August 2021) 62:1–62:31.
[48] Sangiorgi Davide, Locality and interleaving semantics in calculi for mobile processes, Theor. Comput. Sci. 155 (1) (February 1996) 39–83.
[49] Harold Schellinx, Some syntactical observations on linear logic, J. Log. Comput. 1 (4) (September 1991) 537–559.
[50] Davide Sangiorgi, David Walker, The Pi-Calculus: A Theory of Mobile Processes, Cambridge University Press, October 2003.
[51] Bernardo Toninho, Luis Caires, Frank Pfenning, Corecursion and non-divergence in session-typed processes, in: Matteo Maﬀei, Emilio Tuosto (Eds.), Trustworthy
Global Computing, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 2014, pp. 159–175.
[52] Kaku Takeuchi, Kohei Honda, Makoto Kubo, An interaction-based language and its typing system, in: Costas Halatsis, Dimitrios Maritsas, George Philokyprou,
Sergios Theodoridis (Eds.), PARLE’94 Parallel Architectures and Languages Europe, in: Lecture Notes in Computer Science, Springer, Berlin, Heidelberg, 1994,
pp. 398–413.
[53] Bernardo Toninho, Nobuko Yoshida, Interconnectability of session-based logical processes, ACM Trans. Program. Lang. Syst. 40 (4) (December 2018) 17.
[54] Vasco T. Vasconcelos, Fundamentals of session types, Inf. Comput. 217 (August 2012) 52–70.
[55] Bas van den Heuvel, Correctly Communicating Software: Distributed, Asynchronous, and Beyond, PhD thesis, University of Groningen, 2024.
[56] Philip Wadler, Propositions as sessions, in: Proceedings of the 17th ACM SIGPLAN International Conference on Functional Programming, ICFP ’12, ACM, New
York, NY, USA, 2012, pp. 273–286.

26
