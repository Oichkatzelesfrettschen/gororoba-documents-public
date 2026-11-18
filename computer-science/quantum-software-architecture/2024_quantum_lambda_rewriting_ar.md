Source: https://arxiv.org/abs/2411.14856v2
PDF sha256: b1fd100f96b13e75af7d4531463c6cc999ad76d647c90d365850f6eb52870cb5
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of 2024_quantum_lambda_rewriting_ar.pdf

Transcription of `2024_quantum_lambda_rewriting_ar.pdf` in this directory, 26 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-26 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

A Rewriting Theory for Quantum λ-Calculus
Claudia Faggian # 
IRIF, CNRS, Université Paris Cité, France

Gaetan Lopez #
IRIF, CNRS, Université Paris Cité, France
Benoît Valiron # 
Université Paris-Saclay, CNRS, CentraleSupélec, ENS Paris-Saclay, Inria, Laboratoire Méthodes
Formelles, 91190, Gif-sur-Yvette, France

arXiv:2411.14856v2 [cs.LO] 27 Jan 2025

Abstract
Quantum lambda calculus has been studied mainly as an idealized programming language—the
evaluation essentially corresponds to a deterministic abstract machine. Very little work has been
done to develop a rewriting theory for quantum lambda calculus. Recent advances in the theory of
probabilistic rewriting give us a way to tackle this task with tools unavailable a decade ago. Our
primary focus are standardization and normalization results.
2012 ACM Subject Classification Theory of computation → Quantum computation theory; Theory
of computation → Operational semantics; Theory of computation → Equational logic and rewriting;
Theory of computation → Linear logic
Keywords and phrases quantum lambda-calculus, probabilistic rewriting, operational semantics,
asymptotic normalization, principles of quantum programming languages
Digital Object Identifier 10.4230/LIPIcs.CSL.2025.47
Related Version Extended Version: http://arxiv.org/abs/2411.14856
Funding This work has been partially funded by the French National Research Agency (ANR) by
the projects PPS ANR-19-CE48-0014, TaQC ANR-22-CE47-0012 and within the framework of “Plan
France 2030”, under the research projects EPIQ ANR-22-PETQ-0007, OQULUS ANR-23-PETQ0013, HQI-Acquisition ANR-22-PNCQ-0001 and HQI-R&D ANR-22-PNCQ-0002.

1

Introduction

Quantum computation is a model of computation in which one has access to data coded
on the state of objects governed by the law of quantum physics. Due to the unique nature
of quantum mechanics, quantum data exhibits several non-intuitive properties [37]: it is
non-duplicable, it can exist in superposition, and reading the memory exhibits a probabilistic
behavior. Nonetheless, the mathematical formalization is well-established: the state of a
quantum memory and the available manipulations thereof can be expressed within the theory
of Hilbert spaces.
Knill’s QRAM model [34] describes a generic interface for interacting with such a quantum
memory. The memory is modeled with uniquely identified quantum registers, each holding
one quantum bit— also called a qubit. The interface should make it possible to create and
discard registers and apply elementary operations on arbitrary registers. These operations
consist of unitary gates and measurements. The former are internal, local modifications of
the memory state, represented by a quantum circuit, while the latter are the operations for
reading the memory. Measurements are probabilistic operations returning a classical bit of
information.
Quantum algorithms are typically designed with a model akin to Knill’s QRAM [37].
A quantum algorithm consists of the description of a sequence of quantum operations,
© Claudia Faggian, Gaetan Lopez, Benoît Valiron;
licensed under Creative Commons License CC-BY 4.0
33rd EACSL Annual Conference on Computer Science Logic (CSL 2025).
Editors: Jörg Endrullis and Sylvain Schmitz; Article No. 47; pp. 47:1–47:26
Leibniz International Proceedings in Informatics
Schloss Dagstuhl – Leibniz-Zentrum für Informatik, Dagstuhl Publishing, Germany

## PDF page 2

47:2

A Rewriting Theory for Quantum λ-Calculus

measurements, and classical processing. The control flow is purely classical, and generally,
the algorithm’s behavior depends on the results of past measurements. An algorithm,
therefore, mixes classical processing and interaction with quantum memory in a potentially
arbitrary way: Quantum programming languages should be designed to handle it.
Quantum λ-Calculus and Linear Logics. In the last 20 years, many proposals for quantum
programming languages have emerged [28, 30, 40, 39, 8, 11]. Similar to classical languages,
the paradigm of higher-order, functional quantum programming languages have been shown
to be a fertile playground for the development of well-founded, formal quantum languages
aiming at the formal analysis of quantum programs [40, 11].
The quantum λ-calculus of Selinger&Valiron [42] lies arguably at the foundation of the
development of higher-order, quantum functional programming languages [14, 13, 38, 12, 35].
Akin to other extensions of lambda-calculus with probabilistic [17, 15, 21] or non-deterministic
behavior [16], the quantum lambda calculus extends the regular lambda calculus—core of
functional programming languages—with a set interface to manipulate a quantum memory.
Due to the properties of the quantum memory, quantum lambda-calculi should handle
non-duplicable data and probabilistic behavior.
One of the critical points that a quantum programming language should address is the
problem of the non-duplicability of quantum data. In the literature, non-duplicable data
is usually captured with tools coming from linear logic. The first approach [42, 38, 12]
consists in using types, imposing all functions to be linear by default, and with the use of a
special type !A to explicitly pinpoint duplicable objects of type A. An alternative—untyped—
approach [13, 14] considers instead an untyped lambda calculus, augmented with a special
term construct “!” and validity constraints to forbid the duplication of qubits.
Probabilistic and Infinitary Behavior. A quantum λ-calculus featuring all of quantum
computation should not only permit the manipulation of quantum register with unitary
operations but should also give the possibility to measure them, and retrieve a classical bit
of information. As the latter is a probabilistic operation, an operational semantics for a
quantum λ-calculus is inherently probabilistic. As in the non-quantum case, probabilistic
choice and unbounded recursion yield subtle behaviors.
Fair Coin. Consider the following program L, written in a mock-up ML language with
quantum features, similar to the language of [42]:
L := if

meas(Hnew) then I else Ω.

For this introduction,
we only describe its behavior informally. The term L above produces
√
2
1
a qubit in state 2 (|0⟩ + |1⟩) by creating a fresh qubit in state |0⟩ (this is the role of new),
and applying the Hadamard gate H. Measuring this qubit amounts to flipping a fair coin
with equal probability 12 . In one case, the program returns the identity function I; otherwise,
it diverges—the term Ω stands for the usual, non-terminating looping term.
The program L, therefore, uses the quantum memory only once (at the beginning of the
run of the program), and it terminates with probability 21 .

1

The reader unfamiliar with the notation should not worry, as the formal details are not essential at
this point: just retain that the state of our qubit is a superposition of two (basis) states, which play the
role of head and tail. When needed, in Sect. 3 we provide a brief introduction to the mathematical
formalism for quantum computation [37].

## PDF page 3

C. Faggian, G. Lopez, B. Valiron

47:3

Unbounded Use of Fair Coin. In the context of probabilistic behavior, unbounded loops
might terminate asymptotically: A program may terminate with probability 1, but only at
the limit (almost sure termination). A simple example suffices to illustrate this point.
Consider a quantum process R that flips a coin by creating and measuring a fresh qubit.
If the result is head, the process stops, outputting I. If the result is tail, it starts over. In
our mock-up ML, the program R is
(
)
R := letrec f x = if (meas x)then I else f (Hnew) in f (Hnew).

(1)

After n iterations, the program R is in normal form with probability 12 + 212 + · · · + 21n . Even
if the termination probability is 1, this probability of termination is not reached in a finite
number of steps but as a limit. The program in Eq. (1) is our leading example: we formalize
it in Example 4.3.
Operational Semantics of Quantum Programs. As it is customary when dealing with
choice effects, the probabilistic behavior is dealt with by fixing an evaluation strategy. Think
of tossing a (quantum) coin and duplicating the result, versus tossing the coin twice, which is
indeed one key issue at the core of confluence failure in such settings (as observed in [16, 13]).
Following the standard approach adopted for functional languages with side effects, the
evaluation strategy in quantum λ-calculi such as [42, 38, 12] is a deterministic call-by-value
strategy: an argument is reduced to a value before being passed to a function.
One aspect that has been seldom examined is however the properties of the general
reduction associated to the quantum lambda-calculus: this is the purpose of this paper.
A Rewriting Theory for the Quantum λ-Calculus. Lambda calculus has a rich, powerful
notion of reduction, whose properties are studied by a vast amount of literature. Such a general
rewriting theory provides a sound framework for reasoning about programs transformations,
such as compiler optimizations or parallel implementations, and a base on which to reason
about program equivalence. The two fundamental operational properties of lambda calculus
are confluence and standardization. Confluence guarantees that normal forms are unique,
standardization that if a normal form exists, there is a strategy that is guaranteed to terminate
in such a form.
As pioneered by Plotkin [41], standardization allows to bridge between the general
reduction (where programs transformation can be studied), and a specific evaluation strategy,
which implements the execution of an idealized programming language. Summarizing the
situation, for programming languages, there are two kinds of term rewriting: run-time
rewriting (“evaluation”) and compile-time rewriting (program transformations).
In the context of quantum lambda-calculi, the only line of research discussing rewriting
(rather than fixing a deterministic strategy) has been pursued by Dal Lago, Masini, and
Zorzi [14, 13]: working with an untyped quantum lambda-calculus, they establish confluence results (and also a form of standardization, but only for the sub-language without
measurement [13]—therefore, without the probabilistic behavior).
In this paper, we study not only confluence but also standardization and normalization
results for a quantum λ-calculus featuring measurement, and where β reduction (the engine
of λ-calculus) is fully unrestricted. Recent advances in probabilistic and monadic rewriting
theory [9, 12, 19, 33, 6, 23, 27, 32] allow us to tackle this task with a formalism and powerful
techniques unavailable a decade ago. Still, quantum rewriting is more challenging than
probabilistic rewriting because we need to manage the states of the quantum memory. The

CSL 2025

## PDF page 4

47:4

A Rewriting Theory for Quantum λ-Calculus

design of the language is, therefore, also delicate: we need to control the duplication of qubits
while allowing the full power of β-reduction.
Contributions. We can summarize the contributions of the paper as follows. These are
described in more details in Section 5, once all the necessary materials have been set up.
An untyped quantum lambda-calculus, closely inspired by [14] but re-designed to allow
for a more general reduction, now encompassing the full strength of β-reduction; validity
constraints make it quantum-compatible.
The calculus is equipped with a rich operational semantics, which is sound with respect
to quantum computation. The general reduction enables arbitrary β-reduction; surface
reduction (in the spirit of [43] and other calculi based on Linear Logic) plays the role of
an evaluation strategy.
We study the rewriting theory for the system, proving confluence of the reduction, and
standardization.
We obtain a normalization result that scales to the asymptotic case, defining a normalizing
strategy w.r.t. termination at the limit.
Missing proofs and some more technical details are given in the Appendix.

2

Setting the Scene: the Rewriting Ingredients

This section is devoted to a more detailed (but still informal) discussion of two key elements:
the style of λ-calculus we adopt, and what standardization results are about. The calculus is
then defined in Sect. 3, its operational semantics in Sect. 4; standardization and normalization
in the following sections.
Untyped Quantum λ-Calculus. Our quantum calculus is built on top of Simpson’s calculus
Λ! [43], a variant of untyped λ-calculus inspired by Girard’s Linear Logic [29]. In this choice,
we follow [14, 13, 12]. Indeed, the fine control of duplication which Λ! inherits from linear
logic makes it an ideal base for quantum computation.
The Bang operator ! plays the role of a marker for non-linear management: duplicability
and discardability of resources. Abstraction is refined into linear abstraction λx.M and nonlinear abstraction λ! x.M . The latter allows duplication of the argument, which is required
to be suspended as thunk !N , behaving as the !-box of linear logic.
▶ Example 2.1 (duplication, or not). (λx.Hx)(new) is a valid term, but (λx.⟨x, x⟩)(new)
which would duplicate the qubit created by new is not. Instead, we can validly write
(λ! x.CNOT⟨Hx, x⟩)(!new) which thunks new and then duplicate it, yielding CNOT⟨Hnew, new⟩.
Notice that this term produces an entangled pair of qubits.
In our paper, as well as in [14, 13, 12], surface reduction (i.e., no reduction is allowed in
the scope of the ! operator) is the key ingredient to allow for the coexistence of quantum bits
with duplication and erasing. Unlike previous work however, in our setting β-reduction—the
engine of λ-calculus—is unconstrained. We prove that only quantum operations needs to be
surface, making ours a conservative extension of the usual λ-calculus, with its full power.
Call-by-Value... or rather, Call-by-Push-Value. The reader may have recognized that
reduction in our calculus follows the Call-by-Push-Value paradigm, with the Bang operator
thunking a computation. In fact, Simpson’s calculus [43], more precisely the fragment
without linear abstraction, is essentially an untyped version of Call-by-Push-Value, and it

## PDF page 5

C. Faggian, G. Lopez, B. Valiron

Call-by-name λ-calculus
General reduction: (→β )
Evaluation: head (→h )
1. Head factorization:
M →∗β N iff M →∗h · →∗¬h N
2. Head normalization:
M →∗β H iff M →∗h H ′

Call-by-value λv -calculus
General reduction: (→βv )
Evaluation: weak-left (→l )
1. Weak-left factorization:
M →∗βv N iff M →∗l · →∗¬l N
2. Convergence to a value:
M →∗βv V iff M →∗l V ′

47:5

Linear λ! -calculus
General reduction: (→β! )
Evaluation: surface (→s )
1. Surface factorization:
M →∗β! N iff M →∗s · →∗¬s N
2. Surface normalization:
M →∗β! S iff M →∗s S ′

Table 1 Summarizing Standard Factorization and Normalization Results

has been extensively studied in the literature of Linear Logic also with the name of Bang
calculus [20, 31, 10], as a unifying framework which subsumes both Call-by-Name (CbN) and
Call-by-Value(CbV) calculi.
A Taste of Standardization and Normalization: Pure λ-Calculi. Termination and confluence concern the existence and the uniqueness of normal forms, which are the results of a
computation. Standardization and normalization are concerned with how to compute a given
outcome. For example, is there a strategy which guarantees termination, if possible? The
desired outcome is generally a specific kind of terms. In the classical theory of λ-calculus (à
la Barendregt), the terms of interest are head normal forms. In the Call-by-Value approach,
the terms of computational interest are values.
Classical λ-calculus. The simplest form of standardization is factorization: any reduction
sequence can be re-organized so as to first performing specific steps and then everything else.
A paradigmatic example is the head factorization theorem of classical λ-calculus (theorem
11.4.6 in [7]): every β-reduction sequence M →∗β N can be re-organized/factorized so as to
first reducing head redexes and then everything else—in symbols M →∗h · →∗¬h N .
A major consequence is head normalization, relating arbitrary β reduction with head
reduction, w.r.t. head normal forms, the terms of computational interest in classical λ-calculus.
A term M has head normal form if and only if head reduction terminates:
M →∗β H(hnf) ⇔ M →∗h H ′ (hnf)
Plotkin’s Call-by-Value. This kind of results takes its full computational meaning in Plotkin’s
[41] Call-by-Value λ-calculus The terms of interest are here values. Plotkin relates arbitary
β reduction (→βv ) and the evaluation strategy →l which only performs weak-left steps (no
reduction in the scope of abstractions), by establishing
M →∗βv V (value) ⇔ M →∗l V ′ (value)
In words: the unconstrained reduction (→βv ) returns a value if and only if the evaluation
strategy (→l ) returns a value. The proof relies on a factorization: M →∗βv N iff M →∗l · →∗¬l
N.
Simpson’s pure calculus. Standardization and Normalization results have been established
by Simpson also for its calculus Λ! [43]. Here, the evaluation strategy is surface reduction,
i.e. no reduction is allowed in the scope of a ! operator.
Summary. The table in Table 1 summarize the factorization and normalization result for
the three calculi (respectively based on β, βv , β! ) which we have discussed.

CSL 2025

## PDF page 6

47:6

A Rewriting Theory for Quantum λ-Calculus

3

Untyped Quantum λ-Calculus

Quantum lambda-calculus is an idealization of functional quantum programming language:
following Selinger and Valiron [42], it consists of a regular λ-calculus together with specific
constructs for manipulating quantum data and quantum operations. One of the problems
consists in accomodating the non-duplicability of quantum information: in a typed setting
[42] one can rely on a linear type system. In our untyped setting, we instead base our
language on Simpson’s λ-calculus [43], extended with constructs corresponding to quantum
data and quantum operations.
Due of entanglement, the state of an array of quantum bits cannot be separated into
states of individual qubits: the information is non-local. A corollary is that quantum data
cannot easily be written inside lambda-terms: unlike Boolean values or natural numbers, one
cannot put in the grammar of terms a family of constants standing for all of the possible
values a quantum bit could take. A standard procedure [42] relies on an external memory
with register identifiers used as placeholders for qubits inside the lambda-term. As they
stands for qubits, these registers are taken as non-duplicable.
In the original quantum lambda-calculus [42], regular free variables of type qubit were
used to represent registers. In this work, being untyped we prefer to consider two kinds of
variables: regular term variables, and special variables, called registers and denoted by ri
with i ∈ N, corresponding to the qubit number i in the quantum memory. The language is
also equipped with three term constructs to manipulate quantum information. The first term
construct is new, producing the allocation of a fresh qubit2 . The second term construct is
meas(ri , M0 , M1 ), corresponding to a destructive measurement of the qubit ri . The evaluation
then probabilistically continues as M0 or M1 , depending on the measure being |0⟩ or |1⟩.
Finally, assuming that the memory comes with a set of built-in unitary gates ranged over by
letters A, B, C, the term UA corresponds to a function applying the gate A to the indicated
qubits.
Raw Terms.

Formally, raw terms M, N, P, . . . are built according to the following grammar.

M, N, P ::= x | !M | λx.M | λ! x.M | M N | ri | UA | new | meas(P, M, N )

(terms Λq )

where x ranges over a countable set of variables, ri over a disjoint set of registers where i ∈ N
is called the identifier of the register, and UA over a set of build-in n-ary gates. In this paper,
we limit the arity n to be 1 or 2. Pairs do not appear as a primitive construct, but we adopt
the standard encoding, writing ⟨M, N ⟩ as sugar for λf. (f M ) N . We also use the shorthand
⟨M1 , . . . , Mn ⟩ for ⟨M1 ⟨M2 , . . .⟩⟩. The variable x is bound in both λx.P and λ! x.P . As usual,
we silently work modulo α-equivalence. Given a term of shape meas(P, M, N ), we call M
and N its branches. As usual, the set of free variables of a term M are denoted with FV(M ).
The set of registers identifiers for a term M is denoted with Reg(M ).
▶ Remark 3.1. Without any constraints, one could write terms such as ⟨r0 , r0 ⟩ or λx.⟨x, x⟩.
Both are invalid: the former since a qubit cannot be duplicated, the latter since λ-abstractions
are meant to be linear in Simpson’s calculus.
Terms Validity. To deal with the problem in Remark 3.1, we need to introduce the notions
of context and surface context, to speak of occurrences and surface occurrences of subterms.

2

Unlike the original quantum λ-calculus [42], the term new literally evaluates to a qubit.

## PDF page 7

C. Faggian, G. Lopez, B. Valiron

47:7

A context is a term with a hole. We define general contexts where the hole can appear
anywhere, and surface contexts for contexts where holes do not occur in the scope of a !
operator, nor in the branches of a meas(−, −, −). They are generated by the grammars
C ::= L M | M C | CM | λx.C | λ! x.C | meas(C, M, N ) |

(contexts)

meas(M, C, N ) | meas(M, N, C) | !C,

S ::= L M | M S | SM | λx.S | λ! x.S | meas(S, M, N ),

(surface contexts)

where L M denotes the hole of the corresponding context. The notation CLRM (or SLRM) stands
for the term where the only occurrence of a hole L M in C (or S) is replaced with the term R,
potentially capturing free variables of R.
Contexts and surface contexts allow us to formalize two notions of occurence of a subterm
T . The pair (C, T ) (resp. (S, T )) is an occurence (resp. surface occurence) of T in M whever
M = CLT M (resp. M = SLT M). By abuse of notation, we will simply speak of occurrence of a
subterm in M , the context being implicit.
We can now define a notion of valid terms, agreeing with the quantum principle of
no-cloning.
▶ Definition 3.2 ( Valid Terms, and Linearity). A term M is valid whenever
no register occurs in M more than once, and every occurrences of registers are surface;
for every subterm λx.P of M , x is linear in P , i.e. x occurs free exactly once in P and,
moreover, this occurrence of x is surface.
▶ Remark 3.3. The validity conditions for registers and linear variables do not allow us to
put registers inside branches. So for instance a term such as
λz. meas(r0 , z (UA r1 ), z (UB r1 )).
is invalid in our syntax. This function would measure r0 and performs an action on r1 based
on the result. If one cannot write such a term directly with the constraints we have set on
the language, one can however encode the corresponding behavior as follows:
(λ! f.f zr1 ) meas(r0 , !(λux.u(UA x)), !(λux.u(UB x)).
The action on the register r1 is the function f whose definition is based on the result of the
measurement of r0 .
Quantum Operations. Before diving into the definition of the notion of program, we briefly
recall here the mathematical formalism for quantum computation [37].
The basic unit of information in quantum computation is a quantum bit or qubit. The
state of a single qubit is a normalized vector of the 2-dimensional Hilbert space C2 . We
denote the standard basis of C2 as {|0⟩, |1⟩}, so that the general state of a single qubit can
be written as α|0⟩ + β|1⟩, where |α|2 + |β|2 = 1
The basic operations on quantum states are unitary operations and measurements.
A unitary operation maps an n-qubit state to an n-qubit state, and is described by a
unitary 2n × 2n -matrix. We assume that the language provides a set of built-in unitary
operations, including for example the Hadamard gate H and the controlled not gate CNOT:
1
H := √
2

(

1
1

1
−1

)

(1
CNOT :=

0
0
0

0
1
0
0

0
0
0
1

0
0
1
0

)
(2)

Measurement acts as a projection. When a qubit α|0⟩ + β|1⟩ is measured, the observed
outcome is a classical bit: either 0 or 1, with probabilities |α|2 and |β|2 , respectively. Moreover,
the state of the qubit collapses to |0⟩ (resp. |1⟩) if 0 (resp. 1) was observed.

CSL 2025

## PDF page 8

47:8

A Rewriting Theory for Quantum λ-Calculus

Programs. In order to associate quantum states to registers in lambda-terms, we introduce
the notion of program, consisting of a quantum memory and a lambda-term of Λq . A program
is closed under permutation of register identifiers.
The state of one qubit is a normalized vector in E = C2 . The state of a quantum
memory (also called qubits state in the remainder of the document) consisting of n qubits
is a normalized vector Q ∈ E n = (C2 )⊗n , the n-fold Kronecker product of E. The size of
Q is written |Q| := n. We identify a canonical basis element of E n with a string of bits
of size n, denoted with |b0 . . .bn−1 ⟩. A state Q ∈ E n is therefore in general of the form
∑
Q = b0 ,...bn−1 ∈{0,1} αb0 ...bn−1 |b0 . . .bn−1 ⟩. If σ is a permutation of {0, . . . n − 1}, we define
∑
σ(Q) as σ(Q) = b0 ,...bn−1 ∈{0,1} αb0 ...bn−1 |bσ(0) . . .bσ(n−1) ⟩.
A raw program p is then a pair [ Q; M] , where Q ∈ E n and where M is a valid term such
that Reg(M ) = {0, . . . , n − 1}. We call n the size of Q and we denote it with |Q|. If σ is a
permutation over the set {0..n − 1}, the re-indexing σ(p) of p is the pair [ σ(Q); σ(M )] where
σ(M ) is M with each occurence of ri replaced by rσ(i) .
▶ Definition 3.4 (Program). A program is an equivalence class of raw programs under
re-indexing. We identify programs with their representative elements. The set of all programs
is denoted with P.
▶ Example 3.5. The following two raw programs are equal modulo re-indexing: [ |ψ⟩ ⊗
|ϕ⟩; ⟨r0 , r1 ⟩] = [ |ϕ⟩ ⊗ |ψ⟩; ⟨r1 , r0 ⟩] . In both cases, |ψ⟩ is the first qubit in the pair and |ϕ⟩ the
second one. Re-indexing is agnostic with respect to entanglement, and we also have the raw
program [ α|00⟩ + β|01⟩ + γ|10⟩ + δ|11⟩; ⟨r0 , r1 ⟩] being a re-indexation of the raw program
[ α|00⟩ + γ|01⟩ + β|10⟩ + δ|11⟩; ⟨r1 , r0 ⟩] : they are two representative elements of the same
program.

4

Operational Semantics

The operational semantics of λ-calculus is usually formalized by means of a rewriting system.
In the setting of λ-calculus, the rewriting rules are also known as reductions.
Rewriting System. We recall that a rewriting system is a pair (A, →) consisting of a set A
and a binary relation → on A whose pairs are written t → s and called reduction steps. We
denote →∗ (resp. →= ) the transitive-reflexive (resp. reflexive) closure of →. We write t ← u
if u → t. If →1 , →2 are binary relations on A then →1 · →2 denotes their composition.
Probabilistic Rewriting.
In order to define the operational semantics of the quantum
lambda calculus, we need to formalize probabilistic reduction. We do so by means of a
rewrite system over multidistributions, adopting the monadic approach recently developed in
the literature of probabilistic rewriting (see e.g. [6, 12, 19, 23]). Reduction is here defined
not simply on programs, but on (monadic) structures representing probability distributions
over programs, called multidistributions.
The operational semantics of the language is defined by specifying the probabilistic
behavior of programs, then lifting reduction to multidistributions of programs. Let us recall
the notions.
Probability Distributions. Given a countable set Ω, a function µ : Ω → [0, 1] is a probability
∑
subdistribution if ∥µ∥ := ω∈Ω µ(ω) ≤ 1 (a distribution if ∥µ∥ = 1). Subdistributions allow
us to deal with partial results. We write D(Ω) for the set of subdistributions on Ω, equipped

## PDF page 9

C. Faggian, G. Lopez, B. Valiron

47:9

with the pointwise order on functions: µ ≤ ρ if µ(ω) ≤ ρ(ω) for all ω ∈ Ω. D(Ω) has a bottom
element (the subdistribution 0) and maximal elements (all distributions).
multidistributions. We use multidistributions [6] to syntactically represent distributions. A
multidistribution m = {{ qi pi }}i∈I on the set of programs P is a finite multiset of pairs of
∑
the form qi pi , with qi ∈]0, 1], pi ∈ P, and i qi ≤ 1. The set of all multidistributions on
P is MD(P). The sum of two multidistributions is noted +, and is simply the union of the
multisets. The product q · m of a scalar q and a multidistribution m is defined pointwise
q · {{ pi pi }}i∈I := {{ (q · pi )pi }}i∈I . We write {{ p }} for {{ 1p }}.

4.1

The Rewrite System Q

Q is the rewrite system (MD(P), ⇒) where the relation ⇒⊆ MD(P) × MD(P) is monadically
defined in two phases. First, we define one-step reductions from a program to a multidistribution. For example, if p is the program [ √12 (|0⟩ + |1⟩); meas(r0 , M, N )] , the program p reduces
in one step to {{ 12 [ |⟩; M] , 12 [ |⟩; N] }}. Then, we lift the definition of reduction to a binary
relation on MD(P), in the natural way. So for instance, reusing p above, {{ 12 p, 12 [ Q; (λx.xx)F] }}
reduces in one step to {{ 14 [|⟩; M]], 41 [|⟩; N]], 21 [Q; F F]] }}. Let us see the details.
I. Programs Reduction. We first define the reduction of a program p to a multidistribution.
The operational behavior of p is given by beta reduction, denoted with →β , and specific
rules for handling quantum operations—the corresponding reduction is denoted with →q .
Formally, the relations →β and →q (also called reduction steps) are subsets of P × MD(P)
and are defined in Fig. 2 by contextual closure of the root rules ↦→β and ↦→q , given in Fig. 1.
The relation → is then the union →β ∪ →q .
The root rules. They are given in Fig. 1. We call redex the term on the left-hand side
of a rule. Beta rules come in two flavors, the linear one (b), which does not allow for
duplication, and the non-linear one (b!), which possibly duplicate boxes (i.e. terms of shape
!M ). Quantum rules act on the qubits state, exactly implement the operation which we had
informally described in Sect. 3. Notice that the rule (m) has a probabilistic behaviour. The
qubit which has been measured can be discharged (as we actually do).
Contextual Closures. They are defined in Fig. 2. Observe that while the β rules are closed
under arbitrary contexts C, while the quantum rules are restricted to surface contexts S
(no reduction in the scope of a ! operator, nor in the branches of meas(−, −, −)). This
constraints guarantee that qubits are neither duplicated nor delated.
▶ Remark 4.1 (Reindexing). As in [42], reduction is defined on programs, which are equivalence
classes. We define the rules on a convenient representative. For example, in Fig. 1 rule (u1 )
reduces the redex UA r0 . Modulo reindexing, the same rules can be applied to any other
register.
II. Lifting. The lifting of a relation →r ⊆ P × MD(P) to a relation on multidistributions is
defined in Fig. 3. In particular, →, →β , →q , lift to ⇒, ⇒β , ⇒q , respectively.
Reduction Sequences. A ⇒-sequence (or reduction sequence) from m is a sequence m =
m0 , m1 , m2 , . . . such that mi ⇒ mi+1 for every i. We write m0 ⇒∗ m to indicate the existence of
a finite reduction sequence from m0 , and m0 ⇒k m to specify the number k of ⇒-steps. Given
a program p and m0 = {{ p }}, the sequence m0 ⇒ m1 ⇒ · · · naturally models the evaluation of
p; each mk expresses the “expected” state of the system after k steps.

CSL 2025

## PDF page 10

47:10

A Rewriting Theory for Quantum λ-Calculus

β rules

Quantum rules
(n)
(m)

(b)
(!b)

[ Q; (λx.M )N] ↦→β {{ [ Q; M {N/x}] }}
[ Q; (λ! x.M )!N] ↦→β {{ [ Q; M {N/x}] }}

(u1 )
(u2 )

[ Q; new] ↦→q {{ [ Q ⊗ |0⟩; rn] }} where |Q| = n
[ Q; meas(rn , M, N )] ↦→q {{ |α0 |2[ Q0 ; M] , |α1 |2[ Q1 ; N] }}
where Q = α0 Q0 ⊗ |0⟩ + α1 Q1 ⊗ |1⟩ and Q has n + 1 qubits
for A unary operator:
[ Q; UA r0] ↦→q {{ [ Q′ ; r0] }} where Q′ is (A ⊗ Id)Q
for A binary operator:
[Q; (UA ⟨r0 , r1 ⟩]] ↦→q {{ [Q′ ; ⟨r0 , r1 ⟩]] }} where Q′ is (A ⊗ Id)Q.

Figure 1 Root rules (↦→)
β steps
[ Q; M] ↦→β {{ [ Q; M ′] }}
[ Q; CLM M] →β {{ [ Q; CLM ′ M] }}

Quantum steps
[ Q; M] ↦→q {{ pi[ Qi ; Mi] }}
[ Q; SLM M] →q {{ pi[ Qi ; SLMi M] }}

→ := →β ∪ →q

Figure 2 Contextual closure of root rules: (→)

Validity.

Validity of terms is preserved:

▶ Proposition 4.2. If M is a valid term, and [ Q; M] → {{ pi[ Qi ; Mi] }}, then Mi is a valid
term.
Notice that the restriction of →q to surface contexts is necessary to respect the linearity of
quantum computation, avoiding duplication or deletion of qubits.
Examples. Let us see the definitions at work in a few examples. We first formalize the
recursive program from Eq. (1). Recall that H is the Hadamar gate, and I := λx.x.
▶ Example 4.3 (Flipping the quantum coin). The program in Eq. (1) can be written as
p := [ |⟩; ∆!∆] , where |⟩ is just the empty memory and ∆ := λ! x. meas(Hnew, I, x!x). A
reduction from p behaves as follows. At every reduction step, we underline the redex.
{{ [ |⟩; ∆!∆] }} ⇒ {{ [ |⟩; meas(UH new, I, ∆!∆)] }} ⇒ {{ [ |0⟩; meas(UH r0 , I, ∆!∆)] }}
√
2
1
1
[
⇒ {{
(|0⟩ + |1⟩); meas(r0 , I, ∆!∆)]] }} ⇒ {{ [|⟩; I]], [|⟩; ∆!∆]] }}
2
2
2
1
1
1
⇒ . . . ⇒ {{ [ |⟩; I] , [ |⟩; I] , [ |⟩; ∆!∆] }} ⇒ . . .
2
4
4
Notice that the first step is a non-linear β reduction. The reduction of new allocates a fresh
qubit in the memory, corresponding to the register r0 . The redex UH r0 applies the Hadamar
gate H to that qubit. The last reduction performs measurement, yielding a probabilistic
outcome.
▶ Example 4.4 (Entangled pair). Let p := [ |⟩; let ⟨x, y⟩ = UCNOT ⟨UH new, new⟩ in meas(y, I, I)x]
(where let ⟨x, y⟩ . . . is sugar for an opportune encoding). This program produces an entangled pair of qubits (notice how CNOT is applied to a pair of registers) and then measures
one of the qubits. Let us formalize its behaviour:
√
2
∗
{{ p }} ⇒
{{ [
(|0⟩ + |1⟩) ⊗ |0⟩; let ⟨x, y⟩ = UCNOT ⟨r0 , r1 ⟩ in meas(y, I, I)x] }}
s
√2
√
2
2
[
⇒ {{
|00⟩ +
|11⟩; let ⟨x, y⟩ = ⟨r0 , r1 ⟩ in meas(y, I, I)x]] }}
s
2√
2√
2
2
1
1
∗
⇒
{{ [
|00⟩ +
|11⟩; meas(r1 , I, I)r0] }} ⇒
s
s {{ [ |0⟩; Ir0] , [ |1⟩; Ir0] }}
2
2
2
2

## PDF page 11

C. Faggian, G. Lopez, B. Valiron

{{ p }} ⇒ {{ p }}

47:11

({{ pi }} ⇒ mi )i∈I
∑
{{ pi pi | i ∈ I }} ⇒
p · mi
i∈I i

p→m
{{ p }} ⇒ m

Figure 3 Lifting of →

4.2

Surface Reduction and Surface Normal Forms

So far, we have defined a very liberal notion of reduction, in which β is unrestricted—it can
validly be performed even inside a !-box. What shall we adopt as evaluation strategy?
In the setting of calculi based on linear logic, as Simpson’s calculus [43] and the Bang
calculus [20], the natural candidate is surface reduction: the restriction of beta to surface
contexts (→
s β ) plays a role akin to that of head reduction in classical λ-calculus, yielding
to similar factorization and normalization results which relate →β and s
→β (as recalled in
Table 1). The terms of interest are here surface normal forms (snf), such as x or !M .
They are the analog of values in Plotkin’s Call-by-Value λ-calculus and of head normal forms
in classical λ-calculus—such an analogy can indeed be made precise [20, 31, 10]3 .
In our setting, surface reduction and surface normal forms(snf) also play a privileged
role.
Surface Reduction. Surface steps →
s ⊆ P × MD(P) (Fig. 6) are the union →q ∪ →
s β of
quantum steps together with s
→β , i.e. the closure under surface contexts S of the β rules.
A program p is a surface normal form (snf) if p ̸→
s , i.e. no surface reduction is possible
from it.
A →-step which is not surface is noted ¬s
→ . The lifting of s
→, ¬s
→ to relations on multidistributions is denoted ⇒
,
⇒
respectively.
s ¬s
▶ Remark 4.5. Notice that ¬s
→ steps do not act on the qubits state, since they are β steps.
Strict Lifting. To guarantee normalization results (Sect. 7), we will need a stricter form of
lifting, noted ⇒
(Fig. 4), forcing a reduction step to be performed in each program of the
s
multidistribution r, if a redex exists. Clearly ⇒
⊆⇒
s .
s
p ̸→
s

p→
m
s

{{ p }} ⇒ {{ p }}

{{ p }} ⇒ m

s

s

({{ pi }} ⇒ mi )i∈I
s

{{ pi pi | i ∈ I }} ⇒
s

∑
i∈I

pi · mi

Figure 4 Strict lifting of →
s

▶ Example 4.6. We will prove that the strict lifting ⇒
guarantees to reach snf, if any exist.
s
This is obviously not the case for ⇒
s -sequences:
1
1
1
1
1
1
{{ Inew, (λ! x.x!x)!(λ! x.x!x) }} s⇒ {{ Inew, (λ! x.x!x)!(λ! x.x!x) }} s⇒ {{ Inew, (λ! x.x!x)!(λ! x.x!x) }} s⇒ . . .
2
2
2
2
2
2

3

A consequence of Girard’s translation of Call-by-Name and Call-by-Value λ-calculi into Linear Logic.

CSL 2025

## PDF page 12

47:12

A Rewriting Theory for Quantum λ-Calculus

On the Interest of Surface Normal Forms. What is the result of running a quantum
program? In general, since computation is probabilistic, the result of executing a program
will be a distribution over some outcomes of interest. A natural choice are programs of shape
p := [ Q; S] , with S in surface normal form, ensuring that at this point, the qubits state Q is a
stable piece of information (it will not further evolve in the computation). Indeed:
a program p ̸→
s (i.e. in snf) will no longer modify the qubits state.
▶ Remark 4.7. Notice instead that a program p ̸→q (no quantum step is possible) is not
necessarily done in manipulating the quantum memory. Further β reductions may unblock
further quantum steps. Think of (λ! x.CNOT⟨Hx, x⟩)(!new) from Example 2.1.

4.3

Sum-up Tables

Let us conclude the section summarizing the reduction relations at play.
Relations
P × MD(P)
→β
→
s β

Definition
contextual closure of β-rules
closure by surface context of β-rules

Lifted to MD(P) × MD(P)
⇒β
⇒
s β

Strict lifting

→q

closure by surface context of q-rules

⇒q

⇒q

→
→
s

→β ∪ →q
→
∪ →q
s β

⇒
⇒
s

⇒

→

→− s
→

¬s

¬s

⇒β
s

s

⇒

Reduction Sequences
Finite reduction sequence
m ⇒∗ n
m s⇒∗ n

there is a ⇒-sequence from m to n
there is a s⇒-sequence from m to n

m ⇒∗ n

there is a ⇒-sequence from m to n

s

5

s

Rewriting Theory for Q: Overview of the Results

We are now going to study reduction on multidistributions of programs, namely the general
reduction ⇒ (corresponding to the lifting of →) and surface reductions (corresponding to the
lifting of →
s ), and the relation between the two. Let us discuss each point.
1. The reduction ⇒ allows for unrestricted β reduction. For example, we can rewrite in the
scope of a Bang operator ! (perhaps to optimize the thunked code before copying it several
times). We prove that ⇒ is confluent, providing a general framework for rewriting theory.
This (very liberal) reduction has a foundational role, in which to study the equational
theory of the calculus and to analyze programs transformations.
2. Surface reduction ⇒
s ⊆⇒ plays the role of an evaluation strategy, in which however
the scheduling (how redexes should be fired) is not fully specified4 . For example p =

4

This is not only convenient, as it allows for parallel implementation, but it is necessary for standardization
[26]

## PDF page 13

C. Faggian, G. Lopez, B. Valiron

47:13

[ |⟩; ⟨new, Hnew⟩] has two surface redexes, enabling two different steps. We will prove (by
proving a diamond property) that surface reduction (⇒
) is "essentially deterministic"
s
in the sense that while the choice of the redex to fire is non-deterministic, the order in
which such choices are performed are irrelevant to the final result.
3. The two reductions are related by a standardization result (Thm. 6.7) stating that
∗
if m ⇒∗ n then m ⇒
· ¬s
⇒ ∗ n. Standardization is the base of normalization results,
s
concerning properties such as "program p terminates with probability p."
4. We prove that ⇒
is a normalization strategy for ⇒, namely if p may converge to surface
s
normal form with probability p using the general reduction ⇒, then ⇒
reduction must
s
converge to surface normal form with probability p. Informally, we can write that
m ⇓ p implies m ⇓s p (corresponding to the last line in Table 1). To formalize and prove
such a claim we will need more tools, because probabilistic termination is asymptotic, i.e.
it appears as a limit of a possibly infinite reduction. We treat this in Sect. 7, where we
rely on techniques from [2, 23, 24].

6

Confluence and Finitary Standardization

We first recall standard notions which we are going to use.
Confluence, Commutation, and all That (a quick recap). The relation → is confluent
if ←∗ · →∗ ⊆ →∗ · ←∗ . A stricter form is the diamond ← · → implies → · ←, which is
∗
∗
well known to imply confluence. Two relations →
←
◦ and →
• on A commute if :
◦ · →
•
∗
∗
implies →
• ·←
◦ . Confluence and factorization are both commutation properties: a relation
is confluent if it commutes with itself.
An element u ∈ A is a →-normal form if there is no t such that u → t (written u ̸→).
On normalization. In general, a term may or may not reduce to a normal form. And if it
does, not all reduction sequences necessarily lead to normal form. How do we compute a
normal form? This is the problem tackled by normalization: by repeatedly performing only
specific steps, a normal form will be computed, provided that t can reduce to any. Intuitively,
a normalizing strategy for → is a reduction strategy which, given a term t, is guaranteed to
reach normal form, if any exists.

6.1

Surface Reduction has the Diamond Property

In this section, we first prove that surface reduction (⇒
) has the diamond property:
s and ⇒
s
r⇐
s m⇒
s s implies r ⇒
s n⇐
s s (for some n)

(Diamond)

then we show that ⇒ is confluent.
Here we adapt techniques used in probabilistic rewriting [6, 22, 26]. Proving the diamond
property is however significantly harder than in the case of probabilistic λ-calculi, because we
need to take into account also the qubits state, and the corresponding registers. If a program
p = [ Q; M] has two different reductions, we need to join in one step not only the terms, but
also their qubits states, working up to re-indexing of the registers (recall that programs are
equivalence classes modulo re-indexing, see also Example 3.5). The following is an example,
just using the simple construct new. Measurement makes the situation even more delicate.

CSL 2025

## PDF page 14

47:14

A Rewriting Theory for Quantum λ-Calculus

▶ Example 6.1. Let p = [ |⟩; ⟨new, (Hnew)⟩] . The following are two different reduction
sequences
form p. The two normal forms are the same program (Def. 3.4). Here, |+⟩ :=
√
2
(|0⟩
+
|1⟩).
2
[ |⟩; ⟨new, (Hnew)⟩] →
s {{ [ |0⟩; ⟨r0 , (Hnew)⟩] }} ⇒
s {{ [ |0⟩; ⟨r0 , (Hr1 )⟩] }} ⇒
s {{ [ |0⟩ ⊗ |+⟩; ⟨r0 , r1 ⟩] }}
[ |⟩; ⟨new, (Hnew)⟩] →
s {{ [ |0⟩; ⟨new, (Hr0 )⟩] }} ⇒
s {{ [ |+⟩; ⟨new, (r0 )⟩] }} ⇒
s {{ [ |+⟩ ⊗ |0⟩; ⟨r1 , r0 ⟩] }}

The key result is the following version of diamond (commutation). The proof—quite
technical—is given in the Appendix. Recall that ⇒
⊆⇒
s .
s
▶ Lemma 6.2 (Pointed Diamond). Assume p = [Q; M]] and that M has two distinct redexes,
such that p →
n and m2 ⇒
n.
s b m1 and p →
s c m2 . Then there exists n such that m1 ⇒
sc
sb
Moreover, no term Mi in m1 = {{ pi[ Qi ; Mi] }}i∈I and no term Mj in m2 = {{ pj [ Qj ; Mj ] }}j∈J
is in snf.
◀
From the above result we obtain the diamond property.
▶ Proposition 6.3 (Diamond). Surface reductions ⇒
have the diamond property.
s and ⇒
s

◀

In its stricter form, the diamond property guarantees that the non determinism in the
choice of the redex is irrelevant—hence the reduction ⇒
is essentially deterministic. The
s
technical name for this property is Newman’s random descent [36]: no matter the choice of
the redex, all reduction sequences behave the same way, i.e. have the same length, and if
terminating, they do so in the same normal form. Formalized by Thm. 7.3, we use this fact
to establish that ⇒
is a normalizing strategy for ⇒.
s

6.2

Confluence of ⇒

We modularize the proof of confluence by using a classical technique, Hindley-Rosen lemma,
stating that if ⇒1 and ⇒2 are binary relations on the same set R, then their union ⇒1 ∪ ⇒2
is confluent if both ⇒1 and ⇒2 are confluent, and ⇒1 and ⇒2 commute.
▶ Theorem 6.4. The reduction ⇒ satisfies confluence.
Proof. The proof that ⇒β ∪ ⇒q is confluent, is easily obtained from Lemma 6.2, by using
Hindley-Rosen Lemma. We already have most of the elements: ⇒β is confluent: because →β
is; ⇒q is confluent: because it is diamond (Prop. 6.3); ⇒q and ⇒β commute: by Lemma 6.2,
we already know that ⇒q and ⇒
⇒β
s β commute, hence we only need to verify that ⇒q and ¬s
commute, which is easily done.
◀

6.3

Surface Standardization

∗
We show that any sequence ⇒∗ can be factorized as ⇒
· ¬s
⇒ ∗ (Thm. 6.7). Standardization
s

is proved via the modular technique proposed in [1], which in our notation can be stated as
follows:
∗
▶ Lemma 6.5 (Modular Factorization [1]). ⇒∗ ⊆ ⇒
· ¬s
⇒ ∗ if the following conditions hold:
s
∗
1. ⇒∗β ⊆ ⇒
⇒ β ∗ , and
s β · ¬s

2. ¬s
⇒β · ⇒
s q ⊆ ⇒
s q · ⇒β .

◀

## PDF page 15

C. Faggian, G. Lopez, B. Valiron

47:15

Condition 1. in Lemma 6.5 is immediate consequence of Simpson’s surface standardization
∗
for the Λ! calculus [43] stating that →∗β ⊆ →
→β ∗ . Condition 2. in Lemma 6.5 is obtained
s β · ¬s
from the following pointed version:
▶ Lemma 6.6. [ Q; M] ¬s
→β {{ [ Q; P] }} and [ Q; P] →q n implies [ Q; M] →q · ⇒β n.
Proof. By induction on the context S such that P = SLRM and [ Q; SLRM] →q {{ pi[ Qi ; SLRi M] }} =
n. We exploit in an essential way the fact that M and P have the same shape. The proof is
in the Appendix.
◀
By Lemmas 6.5 and 6.6, we obtain the main result of this section:
∗
▶ Theorem 6.7 (Surface Standardization). m ⇒∗ n implies m ⇒
· ¬s
⇒∗ n
s

◀

▶ Remark 6.8 (Strict vs non-strict). Please observe that standardization is stated in terms
of the non-strict lifting (⇒
could reduce more than what is desired. Dually,
s ) of →
s , as ⇒
s
normalization holds in terms of the strict lifting ⇒
, for the reasons already discussed in
s
Example 4.6.
A Reading of Surface Standardization. A program p in snf will no longer modify the
qubits state. Intuitively, p has already produced the maximal amount of quantum data that it
could possibly do. We can read Surface Standardization as follows. Assume {{ p }} ⇒∗ n where
all terms in n are in snf (we use metavariables Si , Si′ to indicate terms in snf). Standardization
guarantees that surface steps suffice to reach a multidistribution n′ whose programs have the
exact same information content as n:
{{ p }} ⇒∗ n = {{ pi[ Qi ; Si] }}i∈I

implies {{ p }} s⇒∗ n′ = {{ pi[ Qi ; Si′] }}i∈I .

∗ ′
This because Thm. 6.7 implies {{ p }} ⇒
n ¬s
⇒ ∗ n, and from n′ ¬s
⇒ ∗ n we deduce that each
s

element pi[ Qi ; Si] in n must come form an element pi[ Qi ; Si′] in n′ where Si′ is in snf and where
the qubits state Qi (and the associated probability pi ) are exactly the same.

7

Probabilistic Termination and Asymptotic Normalization

What does it mean for a program to reach surface normal form (snf)? Since measurement
makes the reduction probabilistic, we need to give a quantitative answer.
Probabilistic Termination. The probability that the system described by the multidistribution m = {{ pi[ Qi ; Mi] | i ∈ I }} is in surface normal form is expressed by a scalar
p = P(m) ∈ [0, 1] which is defined as follows:
{
∑
pi if Mi snf
P(m) =
qi
qi =
0 otherwise
i∈I

Let p = [Q; M]] and m0 = {{ p }}. Let m0 ⇒ m1 ⇒ m2 ⇒ · · · a reduction sequence. P(mk )
expresses the probability that after k steps p is in snf. The probability that p reaches snf along
the (possibly infinite) reduction sequence ⟨mn ⟩n∈N is easily defined as a limit: supn {P(mn )}.
We also say that the sequence ⟨mn ⟩n∈N converges with probability supn {P(mn )}.
▶ Example 7.1 (Recursive coin, cont. ). Consider again Example 4.3. After 4 steps, the
program terminates with probability 12 . After 4 more steps, it terminates with probability
∑∞ 1
1
1
k:1 2k = 1.
2 + 4 , and so on. At the limit, the reduction sequence converges with probability

CSL 2025

## PDF page 16

47:16

A Rewriting Theory for Quantum λ-Calculus

Convergence (Def. 7.2)
m⇓p
m ⇓s p

there is a ⇒-sequence from m which converges with probability p
there is a ⇒
-sequence from m which converges with probability p
s

m ⇊s p

there is a ⇒-sequence from m which converges with probability p
s

Figure 5 Limit of (possibly infinite) reduction sequences

7.1

Accounting for Several Possible Reduction Sequences

Since ⇒ is not a deterministic reduction, given a multidistribution m, there are several possible
reduction sequences from m, and therefore several outcomes (limits) are possible. Following
[23], we adopt the following terminology:
▶ Definition 7.2 (Limits). Given m, we write
m ⇓ p, if there exists a ⇒-sequence ⟨mn ⟩n∈N from m whose limit is p.
Lim(m, ⇒) := {p | m ⇓ p} is the set of limits of m.
JmK denotes the greatest element of Lim(m, ⇒), if any exists.

Intuitively, JpK is the best result that any ⇒-sequence from p can effectively produce. If the
set Lim(p, ⇒) has a sup α but not a greatest element (think of the open interval [0, 1)), it
means that in fact, no reduction can produce α as a limit. Notice also that, when reduction
is deterministic, from any p there is only one maximal reduction sequence, and so it is always
the case that JpK = supn {P(pn )}. Below we exploit the interplay between different rewriting
relations, and their limit; it is useful to summarize our notations in Fig. 5.

7.2

Asymptotic Normalization

Given a quantum program p, does JpK exists? If this is the case, can we define a normalizing
strategy which is guarantee to converge to JpK? The answer is positive. The main result of
this section is that such a normalizing strategy does exist, and it is ⇒
. More precisely, we
s
show that any ⇒
-reduction sequence from p converges to the same limit, which is exactly JpK.
s

We establish the following results, for any arbitrary m ∈ MD(P). Thm. 7.3 is a direct—and
the most important—consequence of the diamond property of ⇒
. The proof uses both point
s
1. and point 2. of Lemma 6.2. For Thm. 7.4, the proof relies on an abstract technique from
[24].
▶ Theorem 7.3 (Random Descent). All ⇒
-sequences from m converge to the same limit.
s

◀

▶ Theorem 7.4 (Asymptotic completeness). m ⇓ p implies m ⇊s q, with p ≤ q.

◀

Thm. 7.4 states that, for each m, if ⇒ reduction may converge to snf with probability p, then
⇒
reduction must converge to snf with probability (at least) p. Thm. 7.3 states that, for
s
each m, the limit q of strict surface reductions (⇒
) from m is unique.
s
Summing-up, the limit q of ⇒
reduction is the best convergence result that any sequence
s
from m can produce. Since ⇒
⊆⇒, then q is also the greatest element in Lim(m, ⇒), i.e.
s
JmK = q. We hence have proved the following, where item (2.) is the asymptotic analogue of
the normalization results in Table 1.
▶ Theorem 7.5 (Asymptotic normalization). For each p ∈ P, (1.) the limit Lim(p, ⇒) has a
greatest element JpK, and (2.) p ⇊s JpK.
◀

## PDF page 17

C. Faggian, G. Lopez, B. Valiron

8

47:17

Related Work and Discussion

In this paper, we propose a foundational notion of (untyped) quantum λ-calculus with a
general reduction, encompassing the full strength of β-reduction while staying compatible with
quantum constraints. We then introduce an evaluation strategy, and derive standardization
and confluence results. We finally discuss normalization of programs at the limit.
Related Works. For quantum λ-calculi without measurement, hence without probabilistic
behavior, confluence [13, 5] (and even a special form of standardization [13]) have been studied
since early work. When dealing with measurement, the analysis is far more challenging. To
our knowledge, only confluence has been studied, in pioneering work by Dal Lago, Masini
and Zorzi [14]. Remarkably, in order to deal with probabilistic and asymptotic behavior,
well before the advances in probabilistic rewriting of which we profit, the authors introduce a
very elaborated technique. Notice that in [14] reduction is non-deterministic, but restricted
to surface reduction. In our paper, their result roughly corresponds to the diamond property
of ⇒
s , together with Thm. 7.3.
No “standard” standardization results (like the classical ones we recall in Table 1) exist
in the literature for the quantum setting. Notice that the form of standardization in [13]
is a reordering of the (surface) measurement-free reduction steps, so to perform first beta
steps, then quantum steps, in agreement with the idea that a quantum computer consists
of a classical device ‘setting up’ a quantum circuit, which is then fed with an input. A
similar refinement is also possible for the corresponding fragment of our calculus (namely
measurement-free →
s ), but clearly does not scale: think of (λx.x) meas(UH new, M, N ), where
the argument of a function is guarded by a measurement.
Our term language is close to [14]. How such a calculus relate with a Call-by-Value
λ-calculus such as [42]? A first level of answer is that our setting is an untyped λ-calculus;
linear abstraction, together with well forming rules, allows for the management of quantum
data. In [42], the same role is fulfilled by the (Linear Logic based) typing system.
Despite these differences, we do expect that our results can be transferred. As already
mentioned, the redex (λ! x.M )!N reflects a Call-by-Push-Value mechanism, which in untyped
form has been extensively studied in the literature with the name of Bang calculus [20, 31, 10],
as a uniform framework to encode both Call-by-Name (CbN) and Call-by-Value (CbV).
Semantical but also syntactical properties, including confluence [20, 31] and standardization
[24, 3] are analyzed in the Bang setting, and then transferred via reverse simulation to both
CbV and CbN. More precisely, a CbV (resp. CbN) translation maps forth-and-back weak
(resp. head) reduction into surface reduction. Surface normal forms are the CbV image of
values (and the CbN image of head normal forms). Since the Bang calculus is exactly the
fragment of Simpson’s calculus [43] without linear abstraction, one may reasonably expect
that our calculus can play a similar role in the quantum setting. It seems however that a
back-and forth translation of CbV (or CbN) will need to encompass types.
A last line of works worth mentioning is the series of works based on Lineal [5, 4, 18].
However, these works differ from our approach in the sense that the λ-terms themselves are
subject to superposition: the distinction between classical and quantum data in an untyped
setting is unclear.
References
1

Beniamino Accattoli, Claudia Faggian, and Giulio Guerrieri. Factorize factorization. In
29th EACSL Annual Conference on Computer Science Logic, CSL 2021, January 25-28,

CSL 2025

## PDF page 18

47:18

A Rewriting Theory for Quantum λ-Calculus

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
16
17
18

19

2021, Ljubljana, Slovenia (Virtual Conference), volume 183 of LIPIcs, pages 6:1–6:25. Schloss
Dagstuhl - Leibniz-Zentrum für Informatik, 2021. doi:10.4230/LIPIcs.CSL.2021.6.
Zena M. Ariola and Stefan Blom. Skew confluence and the lambda calculus with letrec. Annals
of Pure and Applied Logic, 117(1):95 – 168, 2002.
Victor Arrial, Giulio Guerrieri, and Delia Kesner. The benefits of diligence. International
Joint Conference on Automated Reasoning, IJCAR 2024,, 2024.
Pablo Arrighi, Alejandro Díaz-Caro, and Benoît Valiron. The vectorial lambda-calculus.
Information and Computation, 254:105–139, 2017. doi:10.1016/j.ic.2017.04.001.
Pablo Arrighi and Gilles Dowek. Lineal: A linear-algebraic lambda-calculus. Logical Methods
in Computer Science, 13(1), 2017.
Martin Avanzini, Ugo Dal Lago, and Akihisa Yamada. On probabilistic term rewriting.
Sci. Comput. Program., 185, 2020. URL: https://doi.org/10.1016/j.scico.2019.102338,
doi:10.1016/J.SCICO.2019.102338.
Hendrik Pieter Barendregt. The Lambda Calculus – Its Syntax and Semantics, volume 103 of
Studies in logic and the foundations of mathematics. North-Holland, 1984.
Benjamin Bichsel, Maximilian Baader, Timon Gehr, and Martin T. Vechev. Silq: a high-level
quantum language with safe uncomputation and intuitive semantics. In Alastair F. Donaldson
and Emina Torlak, editors, Proceedings of the 41st ACM SIGPLAN International Conference
on Programming Language Design and Implementation, PLDI’20, pages 286–300. ACM, 2020.
doi:10.1145/3385412.3386007.
Olivier Bournez and Florent Garnier. Proving positive almost sure termination under strategies.
In Rewriting Techniques and Applications, RTA, pages 357–371, 2006.
Antonio Bucciarelli, Delia Kesner, Alejandro Ríos, and Andrés Viso. The bang calculus revisited.
Inf. Comput., 293:105047, 2023. URL: https://doi.org/10.1016/j.ic.2023.105047, doi:
10.1016/J.IC.2023.105047.
Christophe Chareton, Sébastien Bardin, Franccois Bobot, Valentin Perrelle, and Benoît Valiron.
An automated deductive verification framework for circuit-building quantum programs. In
Nobuko Yoshida, editor, Proceedings of the 30th European Symposium on Programming
Languages and Systems, ESOP 2021, volume 12648 of Lecture Notes in Computer Science,
pages 148–177. Springer, 2021. doi:10.1007/978-3-030-72019-3_6.
Ugo Dal Lago, Claudia Faggian, Benoît Valiron, and Akira Yoshimizu. The geometry of
parallelism: classical, probabilistic, and quantum effects. In Giuseppe Castagna and Andrew D.
Gordon, editors, Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming Languages, POPL 2017, Paris, France, January 18-20, 2017, pages 833–845. ACM,
2017. URL: http://dl.acm.org/citation.cfm?id=3009859, doi:10.1145/3009837.
Ugo Dal Lago, Andrea Masini, and Margherita Zorzi. On a measurement-free quantum
lambda calculus with classical control. Math. Struct. Comput. Sci., 19(2):297–335, 2009.
doi:10.1017/S096012950800741X.
Ugo Dal Lago, Andrea Masini, and Margherita Zorzi. Confluence results for a quantum
lambda calculus with measurements. Electr. Notes Theor. Comput. Sci., 270(2):251–261, 2011.
doi:10.1016/j.entcs.2011.01.035.
Ugo Dal Lago and Margherita Zorzi. Probabilistic operational semantics for the lambda
calculus. RAIRO Theor. Informatics Appl., 46(3):413–450, 2012. doi:10.1051/ita/2012012.
Ugo de’Liguoro and Adolfo Piperno. Non deterministic extensions of untyped lambda-calculus.
Inf. Comput., 122(2):149–177, 1995.
Alessandra Di Pierro, Chris Hankin, and Herbert Wiklicky. Probabilistic lambda-calculus and
quantitative program analysis. J. Log. Comput., 15(2):159–179, 2005.
Alejandro Díaz-Caro, Mauricio Guillermo, Alexandre Miquel, and Benoît Valiron. Realizability
in the unitary sphere. In Proceedings of the 34th Annual ACM/IEEE Symposium on Logic in
Computer Science, LICS’19, pages 1–13. IEEE, 2019. doi:10.1109/LICS.2019.8785834.
Alejandro Díaz-Caro and Guido Martinez. Confluence in probabilistic rewriting. Electr. Notes
Theor. Comput. Sci., 338:115–131, 2018.

## PDF page 19

C. Faggian, G. Lopez, B. Valiron

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
30

31

32

33

47:19

Thomas Ehrhard and Giulio Guerrieri. The bang calculus: an untyped lambda-calculus
generalizing call-by-name and call-by-value. In Proceedings of the 18th International Symposium
on Principles and Practice of Declarative Programming (PPDP 2016), pages 174–187. ACM,
2016. doi:10.1145/2967973.2968608.
Thomas Ehrhard, Michele Pagani, and Christine Tasson. The computational meaning of
probabilistic coherence spaces. In Proceedings of the 26th Annual IEEE Symposium on Logic
in Computer Science, LICS 2011, June 21-24, 2011, Toronto, Ontario, Canada, pages 87–96.
IEEE Computer Society, 2011. doi:10.1109/LICS.2011.29.
Claudia Faggian. Probabilistic rewriting: Normalization, termination, and unique normal
forms. In Herman Geuvers, editor, 4th International Conference on Formal Structures for
Computation and Deduction, FSCD 2019, June 24-30, 2019, Dortmund, Germany, volume 131
of LIPIcs, pages 19:1–19:25. Schloss Dagstuhl - Leibniz-Zentrum für Informatik, 2019. URL:
https://doi.org/10.4230/LIPIcs.FSCD.2019.19, doi:10.4230/LIPICS.FSCD.2019.19.
Claudia Faggian. Probabilistic rewriting and asymptotic behaviour: on termination and unique
normal forms. Log. Methods Comput. Sci., 18(2), 2022. URL: https://doi.org/10.46298/
lmcs-18(2:5)2022, doi:10.46298/LMCS-18(2:5)2022.
Claudia Faggian and Giulio Guerrieri. Factorization in call-by-name and call-by-value calculi
via linear logic. In Foundations of Software Science and Computation Structures - 24th
International Conference, FOSSACS 2021, volume 12650 of Lecture Notes in Computer
Science, pages 205–225. Springer, 2021. doi:10.1007/978-3-030-71995-1\_11.
Claudia Faggian, Gaetan Lopez, and Benoît Valiron. A rewriting theory for quantum λ-calculus.
CoRR, abs/2411.14856, 2024. URL: http://arxiv.org/abs/2411.14856.
Claudia Faggian and Simona Ronchi Della Rocca. Lambda calculus and probabilistic
computation. In 34th Annual ACM/IEEE Symposium on Logic in Computer Science,
LICS 2019, Vancouver, BC, Canada, June 24-27, 2019, pages 1–13. IEEE, 2019. doi:
10.1109/LICS.2019.8785699.
Francesco Gavazzo and Claudia Faggian. A relational theory of monadic rewriting systems, part
I. In 36th Annual ACM/IEEE Symposium on Logic in Computer Science, LICS 2021, Rome,
Italy, June 29 - July 2, 2021, pages 1–14. IEEE, 2021. doi:10.1109/LICS52264.2021.9470633.
Simon J. Gay. Quantum programming languages: survey and bibliography. Mathematical
Structures in Computer Science, 16(4):581–600, 2006. doi:10.1017/S0960129506005378.
Jean-Yves Girard. Linear logic. Theor. Comput. Sci., 50:1–102, 1987. doi:10.1016/
0304-3975(87)90045-4.
Alexander S. Green, Peter LeFanu Lumsdaine, Neil J. Ross, Peter Selinger, and Benoît Valiron.
Quipper: A scalable quantum programming language. In Hans-Juergen Boehm and Cormac
Flanagan, editors, Proceedings of the ACM SIGPLAN Conference on Programming Language
Design and Implementation, PLDI’13, pages 333–342. ACM, 2013. doi:10.1145/2491956.
2462177.
Giulio Guerrieri and Giulio Manzonetto. The bang calculus and the two Girard’s translations.
In Proceedings Joint International Workshop on Linearity & Trends in Linear Logic and
Applications (Linearity-TLLA 2018), volume 292 of EPTCS, pages 15–30, 2019. doi:10.4204/
EPTCS.292.2.
Jan-Christoph Kassing, Florian Frohn, and Jürgen Giesl. From innermost to full almost-sure
termination of probabilistic term rewriting. In Naoki Kobayashi and James Worrell, editors,
Foundations of Software Science and Computation Structures - 27th International Conference,
FoSSaCS 2024, Held as Part of the European Joint Conferences on Theory and Practice
of Software, ETAPS 2024, Luxembourg City, Luxembourg, April 6-11, 2024, Proceedings,
Part II, volume 14575 of Lecture Notes in Computer Science, pages 206–228. Springer, 2024.
doi:10.1007/978-3-031-57231-9\_10.
Maja H. Kirkeby and Henning Christiansen. Confluence and convergence in probabilistically
terminating reduction systems. In Logic-Based Program Synthesis and Transformation - 27th
International Symposium, LOPSTR 2017, pages 164–179, 2017.

CSL 2025

## PDF page 20

47:20

A Rewriting Theory for Quantum λ-Calculus

34
35

36
37
38

39

40

41
42

43

Emanuel H. Knill. Conventions for quantum pseudocode. Technical Report LAUR-96-2724,
Los Alamos National Laboratory, Los Alamos, New Mexico, US., 1996.
Dongho Lee, Valentin Perrelle, Benoît Valiron, and Zhaowei Xu. Concrete categorical model
of a quantum circuit description language with measurement. In Mikolaj Bojanczyk and
Chandra Chekuri, editors, Proceedings of the 41st IARCS Annual Conference on Foundations
of Software Technology and Theoretical Computer Science, FSTTCS 2021, volume 213 of
LIPIcs, pages 51:1–51:20, 2021. doi:10.4230/LIPIcs.FSTTCS.2021.51.
M.H.A. Newman. On theories with a combinatorial definition of equivalence. Annals of
Mathematics, 43(2), 1942.
Michael A. Nielsen and Isaac L. Chuang. Quantum Computation and Quantum Information.
Cambridge University Press, 2002.
Michele Pagani, Peter Selinger, and Benoît Valiron. Applying quantitative semantics to higherorder quantum computing. In Suresh Jagannathan and Peter Sewell, editors, Proceedings
of the 41st ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages
(POPL’14), pages 647–658. ACM, 2014. doi:10.1145/2535838.2535879.
Luca Paolini, Mauro Piccolo, and Margherita Zorzi. qPCF: higher-order languages and
quantum circuits. Journal of Automated Reasoning, 63(4):941–966, 2019. doi:10.1007/
s10817-019-09518-y.
Jennifer Paykin, Robert Rand, and Steve Zdancewic. QWIRE: a core language for quantum
circuits. In Giuseppe Castagna and Andrew D. Gordon, editors, Proceedings of the 44th ACM
SIGPLAN Symposium on Principles of Programming Languages, POPL’17, pages 846–858.
ACM, 2017. doi:10.1145/3009837.3009894.
Gordon D. Plotkin. Call-by-name, call-by-value and the lambda-calculus. Theor. Comput.
Sci., 1(2):125–159, 1975.
Peter Selinger and Benoît Valiron. A lambda calculus for quantum computation with classical
control. Mathematical Structures in Computer Science, 16:527–552, 2006. doi:10.1017/
S0960129506005238.
Alex K. Simpson. Reduction in a linear lambda-calculus with applications to operational
semantics. In Term Rewriting and Applications, 16th International Conference (RTA 2005),
volume 3467 of Lecture Notes in Computer Science, pages 219–234, 2005. doi:10.1007/
978-3-540-32033-3\_17.

APPENDIX
A

Convention for Garbage Collection.

In the definition of programs, we use the convention that the size of the memory is exactly
the number of registers manipulated in the term. The memory will grow when new qubits
are allocated, and shrink when qubits are read (see Fig. 1): the reduction perform garbage
collection on the fly.
If this makes it easy to identify identical programs, it makes the proofs a bit cumbersome.
We therefore rely for them on an equivalent representation, where a program can have
spurious qubits, as long as they are not entangled with the rest of the memory—i.e. when
measuring them would not change the state of the registers manipulated by the term. So for
instance, in this model [ |0⟩ ⊗ |ψ⟩; r1] is the same as [ ϕ; r0] .

B

Technical properties.

In all proofs we freely use the following closure property, which is immediate by definition of
context and surface context.

## PDF page 21

C. Faggian, G. Lopez, B. Valiron

47:21

▶ Fact B.1 (Closure).
[Q; M]] →β {{ [Q; M ′] }}
2.
[ Q; CLM M] →β {{ [ Q; CLM ′ M] }}

[ Q; M] →c {{ pi[ Qi ; Mi] }}
1.
[ Q; SLM M] →q {{ pi[ Qi ; SLMi M] }}

Surface closure (point 1.) also holds with →β in place of →q .
We will also use the following lemma (analog to substitutivity in [7], p.54) The proof is
straightforward.
▶ Lemma B.2 (Substitutivity). Assume [ Q; P] ∈ P and [ Q; P] → {{ pi[ Qi ; Pi] }}. Then for each
term N : [ Q; P {N/x}] → {{ pi[ Qi ; Pi {N/x}] }}
The converse also holds, and it is simply Fact B.1, that can be reformulated as follows
▶ Fact B.3. Assume [ Q; N] ∈ P, [ Q; N] →q {{ pi[ Qi ; Ni] }} and P a term such that x is linear
in P . Then [ Q; P {N/x}] →q {{ pi[ Qi ; P {Ni /x}] }}
Surface Reduction has a prominent role. We spell-out the definition.
Surface Reduction Step →
s
→
:= →
∪ →q
s
sβ

Surface Beta Step →
s β

(Surface) q-Step →q

[ Q; M] ↦→β {{ [ Q; M ′] }}

[ Q; M] ↦→q {{ pi[ Qi ; Mi] }}
[ Q; SLM M] →q {{ pi[ Qi ; SLMi M] }}

[ Q; SLM M] s
→β {{ [ Q; SLM ′ M] }}
Figure 6 Surface Reduction Steps

C

Surface Reduction has the Diamond Property

We obtain the diamond property (Prop. 6.3) from the pointed diamond, result using the
following technique (from [26]) , which allows us to work pointwise.
▶ Lemma (pointwise Criterion (FaggianRonchi19)). Let →a , →b ⊆ P × MD(P) and ⇒a , ⇒b
their lifting. To prove that ⇒a , ⇒b diamond-commute, i.e.
If p ⇒b m1 and p ⇒a m2 , then ∃r s.t. n ⇒a r and s ⇒b r.
it suffices to prove the property (#) below (stated in terms of a single program p)
(#) If p →b m1 and p →a m2 , then ∃r s.t. n ⇒a r and s ⇒b r.
The same result holds with ⇒ in place of ⇒.
The criterion together with Lemma 6.2 (Point 1.) yields
▶ Prop (6.3). Surface reduction s⇒ has the diamond property. The same holds for ⇒
.
s

CSL 2025

## PDF page 22

47:22

A Rewriting Theory for Quantum λ-Calculus

Proof of the Pointed Diamond
▶ Lemma (Pointed Diamond, Lemma 6.2). Assume p = [Q; M]] and M has two distinct
redexes, such that p →
s b m1 and p →
s c m2 . Then:
A. exists n such that m1 ⇒
n and m2 ⇒
n;
sc
sb
B. no term Mi in m1 = {{ pi[ Qi ; Mi] }}i∈I and no term Mj in m2 = {{ pj [ Qj ; Mj ] }}j∈J is a
surface normal form.
Proof. The proof technique is to go by induction on the term M such that p = [Q; M]] and
then reasonning if the reduction was quantum or beta, if needed.
M = x ; M = ri ; M =UA ; M = new ; M = !M ′
These terms has only zero or one redexes.
M = λx.M ′ ; M = λ! x.M ′
By Induction Hypothesis, we have the result for [ Q; M ′] . Finally, we have the result for p
by surface closure (Fig. 2).
Case M = meas(M0 , M1 , M2 )
p does two surface reduction by hypotheses. By definition, surface redexes are in M0 .
Then, by Induction Hypothesis, we have the result for [ Q; M0] . Finally, we have the result
for p by surface closure (Fig. 2).
Case M = M1 M2
If both redexes are in M1 (or M2 ), by Induction Hypothesis, we have the result for [ Q; M1]
(or [ Q; M2] ). Finally, we have the result for p by surface closure (Fig. 2).
We therefore focus on the cases M = M1 M2 which are not included above, thus we reason
by case analysis on the two reduction.
We distinguish three possibilities :
1. b = β and c = q
2. b = c = q
3. b = c = β
The third case is known by Simpson’s results [43].
Then we are focusing on the first and second case
1. p does one quantum reduction and one beta reduction.
We distinguish three cases, depending if M = M1 M2 is the β-redex or not.
M = M1 M2 is the β-redex, and the q-redex occurs in M1 .
Assume M1 = λ! x.P (case M1 = λx.P is similar). Then
p = [ Q; (λ! x.P )N] s
→β {{ [ Q; P {N/x}] }}
p = [ Q; (λ! x.P )N] →q {{ pi[ Qi ; (λ! x.Pi )N] }} where [ Q; P] → {{ pi[ Qi ; Pi] }}
By Lemma B.2, [ Q; P {N/x}] →q {{ pi[ Qi ; Pi {N/x}] }}.
On the other hand, {{ pi[ Qi ; (λ! x.Pi )N] }} ⇒
{{ pi[ Qi ; Pi {N/x}] }}.
sβ
M = M1 M2 is the β-redex, and the q-redex occurs in M2 .
Assume M has shape (λx.P )N (otherwise it would be a !-abstraction, and M2 would
of the form !M2′ , and the q-redex won’t be able to occur in M2 ).
P contains a single occurrence of x (since λ is a linear abstraction), which is surface,
and so P = SLxM. Thus, we have :
p = [ Q; (λx.P )N] →β {{ [ Q; SLN M] }}
p = [ Q; (λx.P )N] →q {{ pi[ Qi ; (λx.P )Ni] }} where [ Q; N] →q {{ pi[ Qi ; Ni] }}.
By surface closure (Fig. 2), [ Q; SLN M] →q {{ pi[ Qi ; SLNi M] }}. On the other hand, since
P = SLxM, then {{ pi[Qi ; (λx.P )Ni] }} ⇒
{{ pi[Q′ ; SLNi M]] }}.
sβ

## PDF page 23

C. Faggian, G. Lopez, B. Valiron

47:23

Otherwise, M1 = S′ LR1 M and M2 = S′′ LR2 M, with R1 , R2 the two redexes.
By Induction Hypothesis and by surface closure (Fig. 2), we have our result for p.
2. p does two quantum reduction with two different redexes.
Necessarily, M1 = S′ LR1 M and M2 = S′′ LR2 M, and we assume |Q| = n.
We examine the different case, for R1 , R2 ∈ {new, UA ri , meas(ri , Ri1 , Ri2 )}.
a. M1 = S′ LnewM and M2 = S′′ LnewM.
Then, invoking Notation F.3, we have by hypothesis :
p = [ Q; S′ LnewMM2] →q {{ [ ν(Q); S′ Lrn MM2] }} = m1
p = [ Q; M1 S′′ LnewM] →q {{ [ ν(Q); M1 S′′ Lrn M] }} = m2 .
Hence :
′
′′
m1 = [ ν(Q); S′ Lrn MS′′ LnewM] →
s {{ [ (ν ◦ ν)(Q); S Lrn MS Lrn+1 M] }} = n1
′
′′
m2 = [ ν(Q); S′ LnewMS′′ Lrn M] →
s {{ [ (ν ◦ ν)(Q); S Lrn+1 MS Lrn M] }} = n2

We conclude by observing that n1 = n2 because of equivalence defined in Def. 3.4.
b. M1 = S′ LUA ri M and M2 = S′′ LnewM.
Then, invoking Notation F.3, we have by hypothesis :
p = {{ [ Q; S′ LUA ri MM2] }} →q {{ [ UAi Q); S′ Lri MM2] }} = m1
p = {{ [ Q; M1 S′′ LnewM] }} →q = {{ [ ν(Q); M1 S′′ Lrn M] }} = m2
Hence :
′
′′
i
m1 = [ UAi Q; S′ Lri MS′′ LnewM] →
s {{ [ (ν ◦ UA )Q; S Lri MS Lrn M] }} = n1
′
′′
i
m2 = [ ν(Q); S′ LUA ri MS′′ Lrn M] →
s {{ [ (UA ◦ ν)Q; S Lri MS Lrn M] }} = n2

From Lemma F.4, we conclude that n1 = n2 .
c. M1 = S′ LUA ri M and M2 = S′′ LUB rj M.
From Def. 3.2, we have i ̸= j. Then, invoking Notation F.3, we have :
p = {{ [ Q; S′ LUA ri MM2] }} →q {{ [ UAi Q); S′ Lri MM2] }} = m1
p = {{ [ Q; M1 S′′ LUB rj M] }} →q = {{ [ UBj Q; M1 S′′ Lrj M] }} = m2
Hence :
j
′
′′
i
m1 = [ UAi Q; S′ Lri MS′′ LUB rj M] →
s {{ [ (UB ◦ UA )Q; S Lri MS Lrj M] }} = n1
j
′
′′
i
m2 = [ UBj Q; S′ LUA ri MS′′ Lrj M] →
s {{ [ (UA ◦ UB )Q; S Lri MS Lrj M] }} = n2

From Lemma F.4, we conclude that n1 = n2 .
d. M1 = S′ LnewM and M2 = S′′ L meas(ri , M, N )M.
By invoking Notation F.3, we have :
p = {{ [ Q; S′ LnewMM2] }} →q {{ [ ν(Q); S′ Lrn MM2] }} = m1
p = {{ [ Q; M1 S′′ L meas(ri , M, N )M] }} →q {{ ρi0 (Q) [ π0i Q; M1 S′′ LM M] , ρi1 (Q) [ π1i Q; M1 S′′ LN M] }}
We denote the last multi-distribution as m2 .
Hence,
′
′′
′
′′
i
i
i
i
m1 →
s {{ ρ0 (ν(Q)) [ (π0 ◦ ν)Q; S Lrn MS LM M] , ρ1 (ν(Q)) [ (π1 ◦ ν)Q; S Lrn MS LN M] }} = n1
′
′′
i
⋆ [ π0i Q; M1 S′′ LM M] = [ π0i Q; S′ LnewMS′′ LM M] →
s {{ [ (ν ◦ π0 )Q; S Lrn MS LM M] }} = n21

⋆ [ π1i Q; M1 S′′ LN M] = [ π1i Q; S′ LnewMS′′ LN M] s
→ {{ [ (ν ◦ π1i )Q; S′ Lrn MS′′ LN M] }} = n22 .

From Lemma F.4, we conclude that n1 = ρi0 (Q)· n21 + ρi1 (Q)· n22 .
e. M1 = S′ LUA rj M and M2 = S′′ L meas(ri , M21 , M22 )M.
From Def. 3.2, we have i ̸= j. Then, invoking Notation F.3, we have :
p = {{ [ Q; S′ LUA rj M] M2 }} →q = {{ [ UAj Q; S′ Lrj M] M2 }} = m1
p = {{ [ Q; M1 S′′ L meas(ri , M21 , M22 )M] }} →q {{ ρi0 (Q) [ π0i Q; M1 S′′ LM21 M] , ρi1 (Q) [ π1i Q; M1 S′′ LM22 M] }}
We denote the last multidistribution m2 .
Hence :

CSL 2025

## PDF page 24

47:24

A Rewriting Theory for Quantum λ-Calculus

(
)
(
)
j
j
j
′
′′
i
i
i
U
Q
[
m1 →
{
{
ρ
(π
◦U
)(Q);
S
Lr
MS
LM
M]
,
ρ
U
Q
[ (π1i ◦UAj )(Q); S′ Lrj MS′′ LM22 M] , }}
j
21
0
0
1
A
A
A
s
We denote this last multidistribution n1 .
⋆ [ π0i Q; S′ LUA rj MS′′ LM21 M] →q [ (UAj ◦ π0i )(Q); S′ Lrj MS′′ LM21 M] = n21
⋆ [ π1i Q; S′ LUA rj MS′′ LM22 M] →q [ (UAj ◦ π1i )(Q); S′ Lrj MS′′ LM22 M] = n22

From Lemma F.4, we conclude that n1 = ρi0 (Q)· n21 + ρi1 (Q)· n22 .
f. M1 = S′ L meas(ri , M11 , M12 )M and M2 = S′′ L meas(rj , M21 , M22 )M.
From Def. 3.2, we have i ̸= j. Then, invoking Notation F.3, we have :
p = {{ [ Q; S′ L meas(ri , M11 , M12 )MM2] }} →q {{ ρi0 (Q) [ π0i Q; S′ LM11 MM2] , ρi1 (Q) [ π1i Q; S′ LM12 MM2] }}
We denote this last multidistribution m1 .
p = {{ [ Q; M1 S′′ L meas(ri , M21 , M22 )M] }} →q {{ ρj0 (Q) [ π0j Q; M1 S′′ LM21 M] , ρj1 (Q) [ π1j Q; M1 S′′ LM22 M] }}
We denote this last multidistribution m2 .
Hence,
ρi0 (Q) [ π0i Q; S′ LM11 MS′′ L meas(rj , M21 , M22 )M] →
s
(
)
j
j ( i ) i
′
′′
i
[
{{ ρ0 π0 Q ρ0 (Q) (π0 ◦π0 )(Q); S LM11 MS LM21 M]], ρj1 π0i Q ρi0 (Q) [(π0j ◦π0i )(Q); S′ LM11 MS′′ LM22 M]] }}
We denote this last multidistribution m11 .
ρi1 (Q) [ π1i Q; S′ LM12 MS′′ L meas(rj , M21 , M22 )M] →
s
(
)
(
)
{{ ρj0 π1i Q ρi1 (Q) [ (π0j circπ1i )(Q); S′ LM12 MS′′ LM21 M] , ρj1 π1i Q ρi1 (Q) [ (π1j ◦π1i )(Q); S′ LM12 MS′′ LM22 M] }}
We denote this last multidistribution m12 .
ρj0 (Q) [ π0j Q; S′ L meas(ri , M11 , M12 )MS′′ LM21 M] →
s
(
(
)
)
j
j
j
′
′′
i
i
{{ ρ0 π0 Q ρ0 (Q) [ (π0 ◦π0 )(Q); S LM11 MS LM21 M] , ρi1 π0j Q ρj0 (Q) [ (π1i ◦π0j )(Q); S′ LM12 MS′′ LM21 M] }}
We denote this last multidistribution m21 .
ρj1 (Q) [π1j Q; S′ L meas(ri , M11 , M12 )MS′′ LM22 M]] s
→
(
)
(
)
j
j
j
′
′′
i
i
{{ ρ0 π1 Q ρ1 (Q) [ (π0 ◦π1 )(Q); S LM11 MS LM22 M] , ρi1 π1j Q ρj1 (Q) [ (π1i ◦π1j )(Q); S′ LM12 MS′′ LM22 M] }}
We denote this last multidistribution m22 .
From Lemma F.4, we conclude that m11 + m12 = m21 + m22 .
◀

D

Finitary Standardization

Shape Preservation. We recall a basic but key property of contextual closure. If a step →γ
is obtained by closure under non-empty context of a rule ↦→γ , then it preserves the shape
of the term. We say that T and T ′ have the same shape if both terms belong to the same
production (i.e., both terms are an application, an abstraction, a variable, a register, a term
of shape !P , new, etc).
▶ Fact D.1 (Shape preservation). Assume[ Q; M] → {{ pi[ Qi ; Mi] }}, M = CLRM, Mi = CLRi M
and that the context C is non-empty. Then (for each i), M and Mi have the same shape.
An easy-to-verify consequence is the following, stating that non-surface steps (→
¬s )
do not change the quantum memory
do not change the shape of the terms
Notice that the qubit state is unchanged by ¬s
→ steps, since it can only be a ¬s
→β step
▶ Lemma D.2 (Redexes and normal forms preservation). Assume [ Q; M] ¬s
→β {{ [ Q; M ′] }}.
1. M is a redex iff M ′ is a redex. In this case, either both are β-redexes, or both meas-redexes.
2. M is s-normal if and only if M ′ is s-normal.

## PDF page 25

C. Faggian, G. Lopez, B. Valiron

47:25

Proof of Lemma 6.6
▶ Lemma (Lemma 6.6). [ Q; M] ¬s
→β {{ [ Q; P] }} and [ Q; P] →q n implies [ Q; M] →q · ⇒β n.
Proof. By induction on the context S such that P = SLRM and [ Q; SLRM] →q {{ pi[ Qi ; SLRi M] }} =
n. We exploit in an essential way the fact that M and P have the same shape.
◀

E

Asymptotic normalization

Proof Sketch. The proof of Thm. 7.4 relies on an abstract result from the literature [24],
which here we reformulate in our setting:
▶ Lemma E.1 (Asymptotic completeness criterion [24]). Assume
i. s-factorisation: if m ⇒∗ n then m s⇒∗ · ¬s
⇒ ∗ n;
ii. ¬s-neutrality : m ¬s
⇒ m′ implies P(m) = P(m′ ).
Then:
m ⇓ p implies m ⇓s p.
Proof of 7.4. We establishing the two items below, and then compose them.
1. m ⇓ p implies m ⇓s p
2. m ⇓s p implies m ⇊s p′ , with p ≤ p′
Item (1.) holds because ⇒
s satisfies both conditions in Lemma E.1: point (i.) holds by
Thm. 6.7, point (ii.) by Lemma D.2. Item (2.) is immediate.

F

◀

Working up to re-indexing: notation and technical lemmas

In this section we spell-out how to work up to re-indexing. Recall that the rewriting system
in Sect. 4 is defined on the simplest representative of the equivalence classes : the register 0,
making it the subject of each reduction.
To compare different representative, we rely on the following technical results.
▶ Notation F.1. We summarize here some notation to relieve our next lemmas, referring to
Fig. 2 :
π0 the 0-projection on a state Q, π0 (Q) := Q0
π1 the 1-projection on a state Q, π1 (Q) := Q1
σi the permutation that swaps i to 0,
σi (i) := 0, σi (0) := i and σi (k) := k otherwise
µi the permutation that swaps i to the last integer position of a register in a state,
for example if Q has n+1 qubits, µi (i) = n
σi,j the permutation that swaps i to 0, j to 1,
σi,j (i) := 0, σi,j (0) := i, σi,j (j) := 1, σi,j (1) := j and σi,j (k) := k otherwise
Id the n-ary identity quantum gate, I|ϕ⟩ := |ϕ⟩
Recall that the program [ Q; M] denotes the same equivalence class as [ σ(Q); σ(M )] , for
any permutation σ.
▶ Lemma F.2. Let A be a unary quantum gate and B be a binary quantum gate, then we
have :
(u1) [ Q; UA ri] ↦→q {{ [ (σ −1 ◦ (A ⊗ Id) ◦ σ)Q; ri] }}
−1
(u2) [ Q; UB ⟨ri , rj ⟩] ↦→q {{ [ (σi,j
◦ (B ⊗ Id) ◦ σi,j )Q; ⟨ri , rj ⟩] }}
−1
(m) [ Q; meas(ri , M, N )] ↦→q {{ [ (µ−1
i ◦ π0 ◦ µi )Q; M] , [ (µi ◦ π1 ◦ µi )Q; N] }}

CSL 2025

## PDF page 26

47:26

A Rewriting Theory for Quantum λ-Calculus

Proof.
Proof of (u1)
Let A be a unary quantum gate. Let σ denote σi .
By definition, we have [ Q; UA ri] = [ σQ; σ(UA ri )] = [ σQ; UA r0] .
Then, it can be reduced : [ σQ; UA r0] ↦→q {{ [ ((A ⊗ Id) ◦ σ)Q; r0] }}.
Moreover, [ ((A ⊗ Id) ◦ σ)Q; r0] = [ (σ −1 ◦ (A ⊗ Id) ◦ σ)Q; σ −1 r0] = [ (σ −1 ◦ (A ⊗ Id) ◦ σ)Q; ri]
Then, we have : [ Q; UA ri] ↦→q {{ [ (σ −1 ◦ (A ⊗ Id) ◦ σ)Q; ri] }}
Proof of (u2)
Let B be a binary quantum gate. Let σ denote σi,j .
By definition, we have [ Q; (UB ⟨r0 , r1 ⟩] = [ σQ; σ(UB ri rj )] = [ σQ; (UB ⟨r0 , r1 ⟩] .
Then, it can be reduced : [σQ; (UB ⟨r0 , r1 ⟩]] ↦→q {{ [((B ⊗ Id) ◦ σ)Q; ⟨r0 , r1 ⟩]] }}.
Moreover, [ ((B ⊗ Id) ◦ σ)Q; ⟨r0 , r1 ⟩] = [ (σ −1 ◦ (B ⊗ Id) ◦ σ)Q; σ −1 (⟨r0 , r1 ⟩)] = [ (σ −1 ◦ (B ⊗
Id) ◦ σ)Q; ⟨ri , rj ⟩] . Then we have : [ Q; (UB ⟨ri , rj ⟩] ↦→q {{ [ (σ −1 ◦ (B ⊗ Id) ◦ σ)Q; ri rj ] }}
Proof of (m)
Let µ denote µi .
By definition, we have [ Q; meas(ri , M, N )] = [ µQ; µ meas(ri , M, N )] = [ µQ; meas(r0 , µM , µN )] .
Then, it can be reduced : [ µQ; meas(r0 , µM , µN )] ↦→q {{ [ (π0 ◦ µ)Q; µM] , [ (π1 ◦ µ)Q; µN] }}.
Moreover, [ (π0 ◦ µ)Q; µM] = [ (µ−1 ◦ π0 ◦ µ)Q; µ−1 µM] = [ (µ−1 ◦ π0 ◦ µ)Q; M] .
And, [ (π1 ◦ µ)Q; µN] = [ (µ−1 ◦ π1 ◦ µ)Q; µ−1 µN] = [ (µ−1 ◦ π1 ◦ µ)Q; N] .
Then we have : [ Q; meas(ri , M, N )] ↦→q {{ [ (µ−1 ◦ π0 ◦ µ)Q; M] , [ (µ−1 ◦ π1 ◦ µ)Q; N] }}.
◀
▶ Notation F.3. We write UAi for σi−1 ◦ (A ⊗ Id) ◦ σi in the first case of Lemma F.2 and
−1
UAi,j for σi,j
◦ (A ⊗ Id) ◦ σi,j in the second case.
In the third case, we write πbi for µ−1
i ◦ πb ◦ µi .
We write ρb (Q) for the probability associated to the measurement of the 0th qubit on the state
Q if the result is b, referring to Fig. 2, ρ0 (Q) = |α0 |2 and ρ1 (Q) = |α1 |2 .
We write ρib (Q) for ρb (σi Q) , (b ∈ {0, 1}), the probability associated to the measurement of
the i-th qubit on the state Q if the result is b.
We write ν the operation that initialize a qubit at the zero state,
ν(Q) = Q ⊗ |0⟩.
The next lemma is to ensure that we can retrieve the same state and probabilities, without
considering the order of the quantum reductions.
▶ Lemma F.4. In the configuration of Lemma F.2, provided that i ̸= j ̸= k ̸= l and
b, c ∈ {0, 1}:
ν ◦ UAi = UAi ◦ ν (i different from the qubit initiated)
ν ◦ UAi,j = UAi,j ◦ ν (i and j different from the qubit initiated)
ν ◦ πbi = πbi ◦ ν (i different from the qubit initiated)
UAi ◦ UBj = UBj ◦ UAi
UAk ◦ UBi,j = UBi,j ◦ UAk
UAk,l ◦ UBi,j = UBi,j ◦ UAk,l
UAi ◦ πbj = πbj ◦ UAi
UAk,l ◦ πbj = πbj ◦ UAk,l
πbi ◦ πcj = πcj ◦ πbi
ρib (νQ)
=) ρib (Q) (i different from the qubit initiated)
(
ρib UAj Q = ρib (Q)
(
)
ρib UAj,k Q = ρib (Q)
(
)
( )
ρjc (Q) × ρib πcj Q = ρjc πbi Q × ρib (Q)
