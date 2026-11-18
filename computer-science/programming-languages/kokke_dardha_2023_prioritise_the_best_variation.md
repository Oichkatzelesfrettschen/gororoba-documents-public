Source: https://doi.org/10.46298/LMCS-19(4:28)2023
PDF sha256: 12c6f839b18d4e0bf21232f71dbc1f5cfe91ff61103c202960402b4a5245dab5
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of kokke_dardha_2023_prioritise_the_best_variation.pdf

Transcription of `kokke_dardha_2023_prioritise_the_best_variation.pdf` in this directory, 47 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-47 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Logical Methods in Computer Science
Volume 19, Issue 4, 2023, pp. 28:1–28:47
https://lmcs.episciences.org/

Submitted
Published

Dec. 18, 2021
Dec. 18, 2023

PRIORITISE THE BEST VARIATION
WEN KOKKE

AND ORNELA DARDHA

a

University of Strathclyde, Glasgow, UK
e-mail address: wen.kokke@strath.ac.uk

b

School of Computing Science, University of Glasgow, UK
e-mail address: ornela.dardha@glasgow.ac.uk

Abstract. Binary session types guarantee communication safety and session fidelity, but
alone they cannot rule out deadlocks arising from the interleaving of different sessions.
In Classical Processes (CP) [Wad14]—a process calculus based on classical linear logic—
deadlock freedom is guaranteed by combining channel creation and parallel composition
under the same logical cut rule. Similarly, in Good Variation (GV) [Wad15, LM15]—a linear
concurrent λ-calculus—deadlock freedom is guaranteed by combining channel creation and
thread spawning under the same operation, called fork.
In both CP and GV, deadlock freedom is achieved at the expense of expressivity, as
the only processes allowed are tree-structured. This is true more broadly than for CP and
GV, and it holds for all works in the research line based on Curry-Howard correspondences
between linear logic and session types, starting with Caires and Pfenning [CP10]. To
overcome the limitations of tree-structured processes, Dardha and Gay [DG18a] define
Priority CP (PCP), which allows cyclic-structured processes and restores deadlock freedom
by using priorities, in line with Kobayashi and Padovani [Kob06, Pad14].
Following PCP, we present Priority GV (PGV), a variant of GV which decouples channel
creation from thread spawning. Consequently, we type cyclic-structured processes and
restore deadlock freedom by using priorities. We show that our type system is sound by
proving subject reduction and progress. We define an encoding from PCP to PGV and
prove that the encoding preserves typing and is sound and complete with respect to the
operational semantics.

1. Introduction
Session types [Hon93, THK94, HVK98] are a type formalism that ensures communication
channels are used according to their protocols, much like, e.g., data types ensure that functions
are used according to their signature. Session types have been studied in many settings. Most
notably, they have been defined for the π-calculus [Hon93, THK94, HVK98], a foundational
calculus for communication and concurrency, and the concurrent λ-calculi [GV10], including
the main focus of our paper: Good Variation [Wad15, LM15, GV].
Key words and phrases: session types, π-calculus, functional programming, deadlock freedom, GV, CP.
Supported by the EU HORIZON 2020 MSCA RISE project 778233 “Behavioural Application Program
Interfaces” (BehAPI).

l

LOGICAL METHODS
IN COMPUTER SCIENCE

DOI:10.46298/LMCS-19(4:28)2023

© W. Kokke and O. Dardha
CC
⃝
Creative Commons

## PDF page 2

28:2

W. Kokke and O. Dardha

Vol. 19:4

GV is a concurrent λ-calculus with binary session types, where each channel is shared
between exactly two processes. Binary session types guarantee two crucial properties:
communication safety—e.g., if the protocol says to transmit an integer, you transmit an
integer—and session fidelity—e.g., if the protocol says send, you send. A third crucial
property is deadlock freedom, which ensures that processes do not have cyclic dependencies—
e.g., when two processes wait for each other to send a value. Binary session types alone are
insufficient to rule out deadlocks arising from interleaved sessions, but several additional
techniques have been developed to guarantee deadlock freedom in session-typed π-calculus
and concurrent λ-calculus.
In the π-calculus literature, there have been several developments of Curry-Howard
correspondences between session-typed π-calculus and linear logic [Gir87]: Caires and
Pfenning’s πDILL [CP10] corresponds to dual intuitionistic linear logic [Bar96], and Wadler’s
Classical Processes [Wad14, CP] corresponds to classical linear logic [Gir87, CLL]. Both
calculi guarantee deadlock freedom, which they achieve by the combination of binary session
types with a restriction on the way processes can be connected by channels: two processes
can share at most one channel, and, more generally, information transmitted between any
two processes must pass through one unique series of channels and intermediate processes.
We refer to such processes as tree-structured, because the communication graph—where
the vertices are ready processes and two vertices are connected by an edge if and only if
the corresponding processes share a channel—is a tree. For πDILL, CP, and GV, treestructure follows from a syntactic restriction: the combination of name restriction and
parallel composition into a single syntactic construct, corresponding to the logical cut.
There are many downsides to combining name restriction and parallel composition, such
as lack of modularity, difficulty typing structural congruence and formulating label-transition
semantics. GV, specifically, struggles with a complicated metatheory due to the mismatch
between its term language—where restriction and parallel composition are combined—and
its configuration language—where they are not. There have been various approaches to decoupling restriction and parallel composition. Hypersequent CP [MP18, KMP19a, KMP19b,
HCP], Hypersequent GV [FKD+ 21], and Linear Compositional Choreographies [CMS18]
decouple them, but maintain the tree-structure of processes and a correspondence to linear
logic, e.g., while the typing rules for HCP are no longer exactly the proof rules for CLL, every
typing derivations in HCP is isomorphic a proof in CLL, and vice versa. Priority CP [DG18b,
PCP] weakens the correspondence to CLL. PCP is a non-conservative extension of CLL:
every proof in CLL can be translated to a typing derivation in PCP [DP22], but PCP can
prove strictly more theorems, including (partial) bijections between several CLL connectives.
In exchange, PCP has a much more expressive language which allows cyclic-structured
processes. PCP decouples CP’s cut rule into two separate constructs: one for parallel
composition via a mix rule, and one for name restriction via a cycle rule. To restore deadlock
freedom, PCP uses priorities [Kob06, Pad14]. Priorities encode the order of actions and
rule out bad cyclic interleavings. Dardha and Gay [DG18b] prove cycle-elimination for PCP,
adapting the cut-elimination proof for classical linear logic, and deadlock freedom follows as
a corollary.
CP and GV are related via a pair of translations which satisfy simulation [LM16], and
which can be tweaked to satisfy operational correspondence. The two calculi share the same
strong guarantees. GV achieves deadlock freedom via a similar syntactic restriction: it
combines channel creation and thread spawning into a single operation, called “fork”, which

## PDF page 3

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:3

is related to the cut construct in CP. Unfortunately, as with CP, this syntactic restriction
has its downsides.
Our aim is to develop a more expressive version of GV while maintaining deadlock
freedom. While process calculi have their advantages, e.g., their succinctness compared to
concurrent λ-calculi, we chose to work with GV for several reasons. In general, concurrent
λ-calculi support higher-order functions, and have a capability for abstraction not usually
present in process calculi. Within a concurrent λ-calculus, one can derive extensions of the
communication capabilities of the language via well-understood extensions of the functional
fragment, e.g., we can derive internal/external choice from sum types. Concurrent λ-calculi,
among other languages, maintain a clear separation between the program which the user
writes and the configurations which represent the state of the system as it evaluates the
program. However, our main motivation is that results obtained for λ-calculi transfer
more easily to real-world functional programming languages. Case in point: we easily
adapted the type system of PGV to Linear Haskell [BBN+ 18], which gives us a library for
deadlock-free session-typed programming [KD21a]. The benefit of working specifically with
GV, as opposed to other concurrent λ-calculi, is its relation to CP [Wad14], and its formal
properties, including deadlock freedom.
We thus pose our research question for GV:
RQ: Can we design a more expressive GV which guarantees deadlock freedom for
cyclic-structured processes?
We follow the line of work from CP to Priority CP, and present Priority GV (PGV),
a variant of GV which decouples channel creation from thread spawning, thus allowing
cyclic-structured processes, but which nonetheless guarantees deadlock freedom via priorities.
This closes the circle of the connection between CP and GV [Wad14], and their priority-based
versions, PCP [DG18b] and PGV. We cannot straightforwardly adapt the priority typing
from PCP to PGV, as PGV adds higher-order functions. Instead, the priority typing for
PGV follow the work by Padovani and Novara [PN15].
We make the following main contributions:
(1) Priority GV. We present Priority GV (§. 2, PGV), a session-typed functional language
with priorities, and prove subject reduction (Theorem 3.5) and progress (Theorem 3.13).
We addresses several problems in the original GV language, most notably:
(a) PGV does not require the pseudo-type S ♯ ;
(b) Structural congruence is type preserving.
PGV answers our research question positively as it allows cyclic-structured binary
session-typed processes that are deadlock free.
(2) Translation from PCP to PGV. We present a sound and complete encoding of
PCP [DG18b] in PGV (§. 4). We prove the encoding preserves typing (Theorem 4.6)
and satisfies operational correspondence (Theorem 4.7 and Theorem 4.10).
To obtain a tight correspondence, we update PCP, moving away from commuting
conversions and reduction as cut elimination towards reduction based on structural
congruence, as it is standard in process calculi.
This paper is an improved and extended version of a paper published at FORTE 2021
international conference [KD21b]. We present detailed examples and complete proofs of our
technical results.

## PDF page 4

28:4

W. Kokke and O. Dardha

Example 2.1.

Vol. 19:4

Example 2.2.

let (x, x′ ) = new () in
let (y, y ′ ) = new () in

let ((), x′ ) = recv x′ in
spawn λ(). let y = send ((), y) in  ;
wait x′ ; close y
let x = send ((), x) in
let ((), y ′ ) = recv y ′ in
close x; wait y ′


let (x, x′ ) = new () in
′ ) = new () in
let (y, y

let ((), x′ ) = recv x′ in
spawn λ(). let y = send ((), y) in  ;
wait x′ ; close y
′
let ((), y ) = recv y ′ in
let x = send ((), x) in
close x; wait y ′

2. Priority GV
We present Priority GV (PGV), a session-typed functional language based on GV [Wad15,
LM15] which uses priorities à la Kobayashi and Padovani [Kob06, PN15] to enforce deadlock
freedom. Priority GV is more flexible than GV because it allows processes to share more
than one communication channel.
We illustrate this with two programs in PGV, Example 2.1 and Example 2.2. Each
program contains two processes—the main process, and the child process created by spawn—
which communicate using two channels. The child process receives a unit over the channel
x/x′ , and then sends a unit over the channel y/y ′ . The main process does one of two things:
(a) in Example 2.1, it sends a unit over the channel x/x′ , and then waits to receive a unit
over the channel y/y ′ ;
(b) in Example 2.2, it does these in the opposite order, which results in a deadlock.
PGV is more expressive than GV: Example 2.1 is typeable and guaranteed to be deadlock-free
in PGV, but is not typeable in GV [Wad14] and not guaranteed deadlock-free in GV’s
predecessor [GV10]. We believe PGV is a non-conservative extension of GV, as CP can be
embedded in a Kobayashi-style system [DP18].

2.1. Syntax of Types and Terms.
Session types. Session types (S) are defined by the following grammar:
S ::= !o T.S | ?o T.S | endo! | endo?
Session types !o T.S and ?o T.S describe the endpoints of a channel over which we send or
receive a value of type T , and then proceed as S. Types endo! and endo? describe endpoints
of a channel whose communication has finished, and over which we must synchronise before
closing the channel. Each connective in a session type is annotated with a priority o ∈ N.
Types. Types (T , U ) are defined by the following grammar:
T,U

::= T × U | 1 | T + U | 0 | T ⊸p,q U | S

Types T × U , 1, T + U , and 0 are the standard linear λ-calculus product type, unit
type, sum type, and empty type. Type T ⊸p,q U is the standard linear function type,
annotated with priority bounds p, q ∈ N ∪ {⊥, ⊤}. Every session type is also a type. Given a
function with type T ⊸p,q U , p is a lower bound on the priorities of the endpoints captured
by the body of the function, and q is an upper bound on the priority of the communications

## PDF page 5

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:5

that take place as a result of applying the function. The type of pure functions T ⊸ U , i.e.,
those which perform no communications, is syntactic sugar for T ⊸⊤,⊥ U . The lower bound
for a pure function is ⊤ as pure functions never start communicating. For similar reasons,
the upper bound for a pure function is ⊥.
We postulate that the only function types—and, consequently, sequents—that are
inhabited in PGV are pure functions and functions T ⊸p,q U for which p < q.
Typing Environments. Typing environments Γ, ∆, Θ associate types to names. Environments
are linear, so two environments can only be combined as Γ, ∆ if their names are distinct,
i.e., fv(Γ) ∩ fv(∆) = ∅.
Γ, ∆ ::= ∅ | Γ, x : T
Type Duality. Duality plays a crucial role in session types. The two endpoints of a channel
are assigned dual types, ensuring that, for instance, whenever one program sends a value on
a channel, the program on the other end is waiting to receive. Each session type S has a
dual, written S. Duality is an involutive function which preserves priorities:
!o T.S = ?o T.S

?o T.S = !o T.S

endo! = endo?

endo? = endo!

Priorities. Function pr(·) returns the smallest priority of a session type. The type system
guarantees that the top-most connective always holds the smallest priority, so we simply
return the priority of the top-most connective:
pr(!o T.S) = o

pr(?o T.S) = o

pr(endo! ) = o

pr(endo? ) = o

We extend the function pr(·) to types and typing contexts by returning the smallest
priority in the type or context, or ⊤ if there is no priority. We use ⊓ and ⊔ to denote the
minimum and maximum, respectively:
pr(T × U )
pr(T + U )
pr(T ⊸p,q U )
pr(Γ, x : A)

=
=
=
=

pr(T ) ⊓ pr(U )
pr(T ) ⊓ pr(U )
p
pr(Γ) ⊓ pr(A)

pr(1)
pr(0)
pr(S)
pr(∅)

=
=
=
=

⊤
⊤
pr(S)
⊤

Terms. Terms (L, M , N ) are defined by the following grammar:
L, M , N

K

::=
|
|
::=

x | K | λx.M | M N
() | M ; N | (M, N ) | let (x, y) = M in N
inl M | inr M | case L {inl x ↦→ M ; inr y ↦→ N } | absurd M
link | new | spawn | send | recv | close | wait

Let x, y, z, and w range over variable names. Occasionally, we use a, b, c, and d.
The term language is the standard linear λ-calculus with products, sums, and their units,
extended with constants K for the communication primitives.
Constants are best understood in conjunction with their typing and reduction rules
in Figs. 1 and 2.
Briefly, link links two endpoints together, forwarding messages from one to the other,
new creates a new channel and returns a pair of its endpoints, and spawn spawns off its
argument as a new thread.

## PDF page 6

28:6

W. Kokke and O. Dardha

Vol. 19:4

The send and recv functions send and receive values on a channel. However, since the
typing rules for PGV ensure the linear usage of endpoints, they also return a new copy of
the endpoint to continue the session.
The close and wait functions close a channel.
We use syntactic sugar to make terms more readable: we write let x = M in N in place
of (λx.N ) M , λ().M in place of λz.z; M , and λ(x, y).M in place of λz.let (x, y) = z in M .
We can recover GV’s fork as λx.let (y, z) = new () in spawn (λ().x y); z.
Internal and External Choice. Typically, session-typed languages feature constructs for
internal and external choice. In GV, these can be defined in terms of the core language, by
sending or receiving a value of a sum type [LM15]. We use the following syntactic sugar for
internal (S ⊕o S ′ ) and external (S &o S ′ ) choice and their units:
S ⊕o S ′ ≜ !o (S + S ′ ).endo+1
!
S &o S ′ ≜ ?o (S + S ′ ).endo+1
?

⊕o {} ≜ !o 0.endo+1
!
&o {} ≜ ?o 0.endo+1
?

As the syntax for units suggests, these are the binary and nullary forms of the more
common n-ary choice constructs ⊕o {li : Si }i∈I and &o {li : Si }i∈I , which one may obtain
generalising the sum types to variant types. For simplicity, we present only the binary and
nullary forms.
Similarly, we use syntactic sugar for the term forms of choice, which combine sending
and receiving with the introduction and elimination forms for the sum and empty types.
There are two constructs for binary internal choice, expressed using the meta-variable ℓ
which ranges over {inl, inr}. As there is no introduction for the empty type, there is no
construct for nullary internal choice:
select ℓ
≜ λx.let (y, z) = new in close (send (ℓ y, x)); z
offer L {inl x ↦→ M ; inr y ↦→ N } ≜
let (z, w) = recv L in wait w; case z {inl x ↦→ M ; inr y ↦→ N }
offer L {} ≜ let (z, w) = recv L in wait w; absurd z

2.2. Operational Semantics.
Configurations. Priority GV terms are evaluated as part of a configuration of processes.
Configurations are defined by the following grammar:
ϕ ::= • | ◦

C, D, E ::= ϕ M | C ∥ D | (νxx′ )C

Configurations (C, D, E) consist of threads ϕ M , parallel compositions C ∥ D, and name
restrictions (νxx′ )C. To preserve the functional nature of PGV, where programs return a
single value, we use flags (ϕ) to differentiate between the main thread, marked •, and child
threads created by spawn, marked ◦. Only the main thread returns a value. We determine
the flag of a configuration by combining the flags of all threads in that configuration:
•+◦=•

◦+•=•

◦+◦=◦

(• + • is undefined)

To distinguish between the use of ◦ to mark child threads [LM15] and the use of the
meta-variable o for priorities [DG18b], they are typeset in a different font and colour.

## PDF page 7

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:7

Values. Values (V , W ), evaluation contexts (E), thread evaluation contexts (F), and
configuration contexts (G) are defined by the following grammars:
V ,W
E

F
G

::=
::=
|
|
::=
::=

x | K | λx.M | () | (V, W ) | inl V | inr V
□ | EM | V E
E; N | (E, M ) | (V, E) | let (x, y) = E in M
inl E | inr E | case E {inl x ↦→ M ; inr y ↦→ N } | absurd E
ϕE
□ | G ∥ C | (νxy)G

Values are the subset of terms which cannot reduce further. Evaluation contexts are one-hole
term contexts, i.e., terms with exactly one hole, written □. We write E[M ] for the evaluation
context E with its hole replaced by the term M . Evaluation contexts are specifically those
one-hole term contexts under which term reduction can take place. Thread contexts are a
convenient way to lift the notion of evaluation contexts to threads. We write F[M ] for the
thread context F with its hole replaced by the term M . Configuration contexts are one-hole
configuration contexts, i.e., configurations with exactly one hole, written □. Specifically,
configuration contexts are those one-hole term contexts under which configuration reduction
can take place. The definition for G only gives the case in which the hole is in the left-most
parallel process, i.e., it only defines G ∥ C and not C ∥ G. The latter is not needed, as ∥ is
symmetric under structural congruence, though it would be harmless to add. We write G[C]
for the evaluation context G with its hole replaced by the term C.
Reduction Relation. We factor the reduction relation of PGV into a deterministic reduction
on terms (−→M ) and a non-deterministic reduction on configurations (−→C ), see Fig. 1.
+
⋆
⋆
We write −→+
M and −→C for the transitive closures, and −→M and −→C for the reflexivetransitive closures.
Term reduction is the standard call-by-value, left-to-right evaluation for GV, and only
deviates from reduction for the linear λ-calculus in that it reduces terms to values or ready
terms waiting to perform a communication action.
Configuration reduction resembles evaluation for a process calculus: E-Link, E-Send, and
E-Close perform communications, E-LiftC allows reduction under configuration contexts,
and E-LiftSC embeds a structural congruence ≡. The remaining rules mediate between the
process calculus and the functional language: E-New and E-Spawn evaluate the new and
spawn constructs, creating the equivalent configuration constructs, and E-LiftM embeds
term reduction.
Structural congruence satisfies the following axioms: SC-LinkSwap allows swapping
channels in the link process. SC-ResLink allows restriction to be applied to link which is
structurally equivalent to the terminated process, thus allowing elimination of unnecessary
restrictions. SC-ResSwap allows swapping channels and SC-ResComm states that restriction
is commutative. SC-ResExt is the standard scope extrusion rule. Rules SC-ParNil,
SC-ParComm and SC-ParAssoc state that parallel composition uses the terminated process
as the neutral element; it is commutative and associative.
While our configuration reduction is based on the standard evaluation for GV, the
increased expressiveness of PGV allows us to simplify the relation on two counts.
(i) We decompose the fork construct. In GV, fork creates a new channel, spawns a child
thread, and, when the child thread finishes, it closes the channel to its parent. In PGV,
these are three separate operations: new, spawn, and close. We no longer require

## PDF page 8

28:8

Vol. 19:4

W. Kokke and O. Dardha

E-Lam
E-Unit
E-Pair
E-Inl
E-Inr

Term reduction.
(λx.M ) V
(); M
let (x, y) = (V, W ) in M
case inl V {inl x ↦→ M ; inr y ↦→ N }
case inr V {inl x ↦→ M ; inr y ↦→ N }

−→M
−→M
−→M
−→M
−→M

M {V /x}
M
M {V /x}{W/y}
M {V /x}
N {V /y}

E-Lift

M −→M M ′
E[M ] −→M E[M ′ ]

Structural congruence.
SC-LinkSwap
SC-ResLink
SC-ResSwap
SC-ResComm
SC-ResExt
SC-ParNil
SC-ParComm
SC-ParAssoc

F[link (x, y)]
(νxy)(ϕ link (x, y))
(νxy)C
(νxy)(νzw)C
(νxy)(C ∥ D)
C ∥ ◦()
C∥D
C ∥ (D ∥ E)

≡
≡
≡
≡
≡
≡
≡
≡

F[link (y, x)]
ϕ ()
(νyx)C
(νzw)(νxy)C, if {x, y} ∩ {z, w} = ∅
C ∥ (νxy)D, if x, y ∈
/ fv(C)
C
D∥C
(C ∥ D) ∥ E

Configuration reduction.
E-Link
(νxy)(F[link (w, x)] ∥ C) −→C F[()] ∥ C{w/y}
E-New
F[new ()]
−→C (νxy)(F[(x, y)]), if x, y ∈
/ fv(F)
E-Spawn F[(spawn V )]
−→C F[()] ∥ ◦ V ()
E-Send
(νxy)(F[send (V, x)] ∥ F ′ [recv y]) −→C (νxy)(F[x] ∥ F ′ [(V, y)])
E-Close (νxy)(F[wait x] ∥ F ′ [close y])
−→C F[()] ∥ F ′ [()]
E-LiftC

C −→C C ′
G[C] −→C G[C ′ ]

E-LiftM

M −→M M ′
F[M ] −→M F[M ′ ]

E-LiftSC

C ≡ C′

C ′ −→C D′
C −→C D

D′ ≡ D

Figure 1: Operational Semantics for PGV.
that every child thread finishes by returning a terminated channel. Consequently, we
also simplify the evaluation of the link construct.
Intuitively, evaluating link causes a substitution: if we have a channel bound as
(νxy), then link (w, x) replaces all occurrences of y by w. However, in GV, link is
required to return a terminated channel, which means that the semantics for link must
create a fresh channel of type end! /end? . The endpoint of type end! is returned by
the link construct, and a wait on the other endpoint guards the actual substitution.
In PGV, evaluating link simply causes a substitution.
(ii) Our structural congruence is type preserving. Consequently, we can embed it directly
into the reduction relation. In GV, this is not the case, and subject reduction relies
on proving that if the result of rewriting via ≡ followed by reducing via −→C is an
ill-typed configuration, we can rewrite it to a well-typed configuration via ≡.

## PDF page 9

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:9

Static Typing Rules.
T-Lam

Γ, x : T ⊢q M : U

T-Var

T-Const

x : T ⊢⊥ x : T

∅ ⊢⊥ K : T

T-App

′

′

Γ ⊢p M : T ⊸p ,q U

∆ ⊢q N : T

Γ, ∆ ⊢

p⊔q⊔q ′

T-LetUnit

T-Unit

Γ ⊢⊥ λx.M : T ⊸pr(Γ),q U

Γ ⊢p M : 1

∅ ⊢⊥ () : 1

q < p′

p < pr(∆)

M N :U
∆ ⊢q N : T
p < pr(∆)
p⊔q
Γ, ∆ ⊢
M; N : T

T-Pair

Γ ⊢p M : T
∆ ⊢q N : U
p < pr(∆)
p⊔q
Γ, ∆ ⊢
(M, N ) : T × U

T-LetPair

Γ ⊢p M : T × T ′
∆, x : T , y : T ′ ⊢q N : U
p < pr(∆, T , T ′ )
Γ, ∆ ⊢p⊔q let (x, y) = M in N : U

T-Inl

T-Inr

Γ ⊢p M : T
pr(T ) = pr(U )
p
Γ ⊢ inl M : T + U

Γ ⊢p M : U
pr(T ) = pr(U )
p
Γ ⊢ inr M : T + U

T-CaseSum

Γ ⊢p L : T + T ′
∆, x : T ⊢q M : U
∆, y : T ′ ⊢q N : U
Γ, ∆ ⊢p⊔q case L {inl x ↦→ M ; inr y ↦→ N } : U

p < pr(∆)

T-Absurd

Γ ⊢p M : 0
Γ, ∆ ⊢p absurd M : T

Type Schemas for Constants.
link : S × S ⊸ 1

spawn : (1 ⊸p,q 1) ⊸ 1

new : 1 ⊸ S × S

send : T × !o T.S ⊸⊤,o S

recv : ?o T.S ⊸⊤,o T × S

close : endo! ⊸⊤,o 1

wait : endo? ⊸⊤,o 1

Runtime Typing Rules.
T-Main

Γ ⊢p M : T
Γ ⊢• • M

T-Child

Γ ⊢p M : 1
Γ ⊢◦ ◦ M

T-Res

Γ, x : S, y : S ⊢ϕ C
Γ ⊢ϕ (νxy)C

Figure 2: Typing Rules for PGV.

T-Par

Γ ⊢ϕ C

′

∆ ⊢ϕ D
′

Γ, ∆ ⊢ϕ+ϕ C ∥ D

## PDF page 10

28:10

W. Kokke and O. Dardha

Vol. 19:4

2.3. Typing Rules.

Terms Typing. Typing rules for terms are at the top of Fig. 2. Terms are typed by a
judgement Γ ⊢p M : T stating that “a term M has type T and an upper bound on its priority
p under the typing environment Γ”. Typing for the linear λ-calculus is standard. Linearity
is ensured by splitting environments on branching rules, requiring that the environment in
the variable rule consists of just the variable, and the environment in the constant and unit
rules are empty. Constants K are typed using type schemas, which hold for any concrete
assignment of types and priorities to their meta-variables. Instantiated type schemas are
embedded into typing derivations using T-Const in Fig. 2, e.g., the type schema for send
can be instantiated with o = 2, T = 1, and S = 0, and embedded using T-Const to give
the following typing derivation:

send : 1 × !2 1.0 ⊸⊤,2 0
The typing rules treat all variables as linear resources, even those of non-linear types such
as 1, though they can easily be extended to allow values with unrestricted usage [Wad14].
The only non-standard feature of the typing rules is the priority annotations. Priorities
are based on obligations/capabilities used by Kobayashi [Kob06], and simplified to single
priorities following Padovani [Pad14]. The integration of priorities into GV is adapted from
Padovani and Novara [PN15]. Paraphrasing Dardha and Gay [DG18b], priorities obey the
following two laws:
(i) an action with lower priority happens before an action with higher priority; and
(ii) communication requires equal priorities for dual actions.
In PGV, we keep track of a lower and upper bound on the priorities of a term, i.e., while
evaluating the term, when it starts communicating, and when it finishes, respectively. The
upper bound is written on the sequent and the lower bound is approximated from the typing
environment, e.g., for Γ ⊢p M : T the upper bound is p and the lower bound is at least
pr(Γ). The latter is correct because a term cannot communicate at a priority earlier than the
earliest priority amongst the channels it has access to. It is an approximation on function
terms, as these can “skip” communication by returning the corresponding channel unused.
However, linearity prevents such functions from being used in well typed configurations:
once the unused channel’s priority has passed, it can no longer be used.
Typing rules for sequential constructs enforce sequentiality, e.g., the typing for M ; N
has a side condition which requires that the upper bound of M is smaller than the lower
bound of N , i.e., M finishes before N starts. The typing rule for new ensures that both
endpoints of a channel share the same priorities. Together, these two constraints guarantee
deadlock freedom.
To illustrate this, let’s go back to the deadlocked program in Example 2.2. Crucially, it
composes the terms below in parallel. While each of these terms itself is well typed, they
impose opposite conditions on the priorities, so connecting x to x′ and y to y ′ using T-Res
is ill-typed, as there is no assignment to o and o′ that can satsify both o < o′ and o′ < o.

## PDF page 11

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:11

(We omit the priorities on end! and end? .)
′

′

y ′ : ?o 1.end? ⊢o recv y ′ : 1 × end?
o
′
x : ! 1.end! , y : end? ⊢p let x = send ((), x) in . . . : 1

o′ < o

′

x : !o 1.end! , y ′ : ?o 1.end? ⊢p let ((), y ′ ) = recv y ′ in let x = send ((), x) in . . . : 1
x′ : ?o 1.end? ⊢o recv x′ : 1 × end?
y : ! 1.end! , x′ : end? ⊢q let y = send ((), y) in . . . : 1
o′

o < o′

o′

y : ! 1.end! , x′ : ?o 1.end? ⊢q let ((), x′ ) = recv x′ in let y = send ((), y) in . . . : 1
Closures suspend communication, so T-Lam stores the priority bounds of the function
body on the function type, and T-App restores them. For instance, λx.send (x, y) is assigned
the type A ⊸o,o S, i.e., a function which, when applied, starts and finishes communicating
at priority o.
x : T ⊢⊥ x : T

x : T , y : !o T.S ⊢⊥ y : !o T.S

send : T × !o T.S ⊸⊤,o S
x : T , y : !o T.S ⊢⊥ (x, y) : T × !o T.S
x : T , y : !o T.S ⊢o send (x, y) : S
y : !o T.S ⊢⊥ λx.send (x, y) : T ⊸o,o S
For simplicity, we assume priority annotations are not inferred, but provided as an
input to type checking. However, for any term, priorities can be inferred, e.g., by using the
topological ordering of the directed graph where the vertices are the priority meta-variables
and the edges are the inequality constraints between the priority meta-variables in the typing
derivation.
Configurations Typing. Typing rules for configurations are at the bottom of Fig. 2. Configurations are typed by a judgement Γ ⊢ϕ C stating that “a configuration C with flag ϕ is well
typed under typing environment Γ”. Configuration typing is based on the standard typing
for GV. Terms are embedded either as main or as child threads. The priority bound from
the term typing is discarded, as configurations contain no further blocking actions. Main
threads are allowed to return a value, whereas child threads are required to return the unit
value. Sequents are annotated with a flag ϕ, which ensures that there is at most one main
thread.
While our configuration typing is based on the standard typing for GV, it differs on two
counts:
(i) we require that child threads return the unit value, as opposed to a terminated channel;
and
(ii) we simplify typing for parallel composition.
In order to guarantee deadlock freedom, in GV each parallel composition must split
exactly one channel of the channel pseudo-type S ♯ into two endpoints of type S and S.
Consequently, associativity of parallel composition does not preserve typing. In PGV, we
guarantee deadlock freedom using priorities, which removes the need for the channel pseudotype S ♯ , and simplifies typing for parallel composition, while restoring type preservation for
the structural congruence.

## PDF page 12

28:12

Vol. 19:4

W. Kokke and O. Dardha

T-LamUnit

z : 1 ⊢⊥ z : 1
Γ ⊢q M : T
Γ, z : 1 ⊢q z; M : T

Γ ⊢⊥ λ().M : 1 ⊸pr(Γ),q T ≜

Γ ⊢⊥ λz.z; M : 1 ⊸pr(Γ),q T

Γ ⊢q M : T

T-LamPair

Γ, x : T , y : T ′ ⊢q M : U

Γ ⊢⊥ λ(x, y).M : T × T ′ ⊸pr(Γ),q U ≜
z : T × T ′ ⊢⊥ z : T × T ′
Γ, x : T , y : T ′ ⊢q M : U
Γ, z : T × T ′ ⊢q let (x, y) = z in M : T
Γ ⊢⊥ λz.let (x, y) = z in M : T × T ′ ⊸pr(Γ),q U

T-Let

Γ ⊢p M : T
∆, x : T ⊢q N : U
p < pr(∆)
p⊔q
Γ, ∆ ⊢
let x = M in N : U
≜
∆, x : T ⊢q N : U

∆ ⊢⊥ λx.N : T ⊸pr(∆),q U
Γ ⊢p M : T
Γ, ∆ ⊢q⊔p (λx.N ) M : U

p < pr(∆)

T-Fork

∅ ⊢⊥ fork : (S ⊸p,q 1) ⊸ S ≜
(a)

∅ ⊢⊥ () : 1

∅ ⊢⊥ new () : S × S
x : S ⊸p,q 1 ⊢⊥ x : S ⊸p,q 1
y : S ⊢⊥ y : S
x : S ⊸p,q 1, y : S ⊢q x y : 1
(b)

x : S ⊸p,q 1, y : S ⊢⊥ λ().x y : 1 ⊸p,q 1
x : S ⊸p,q 1, y : S ⊢⊥ spawn (λ().x y) : 1

z : S ⊢⊥ z : S

x : S ⊸p,q 1, y : S, z : S ⊢⊥ spawn (λ().x y); z : S
x : S ⊸p,q 1 ⊢⊥ let (y, z) = new () in spawn (λ().x y); z : S
∅ ⊢⊥ λx.let (y, z) = new () in spawn (λ().x y); z : (S ⊸p,q 1) ⊸ S
(a) = new : 1 ⊸ S × S

(b) = spawn : (1 ⊸p,q 1) ⊸ 1

Figure 3: Typing Rules for Syntactic Sugar for PGV (T-LamUnit, T-LamPair, T-Let, and
T-Fork).

## PDF page 13

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:13

T-Select-Inl

pr(S) = pr(S ′ )

∅ ⊢⊥ select inl : S ⊕o S ′ ⊸⊤,o S ≜
(a)

∅ ⊢ () : 1

∅ ⊢ new () : S × S
y:S⊢y:S
x : S ⊕o S ′ ⊢ x : S ⊕o S ′

y : S ⊢ inl y : S + S ′
(c)

x : S ⊕o S ′ , y : S ⊢ (inl y, x) : (S + S ′ ) × (S ⊕o S ′ )
x : S ⊕o S ′ , y : S ⊢ send (inl y, x) : endo+1
!

(b)

x : S ⊕o S ′ , y : S ⊢ close (send (inl y, x)) : 1
z:S⊢z:S
o

′

x : S ⊕ S , y : S, z : S ⊢ close (send (inl y, x)); z : S
x : S ⊕o S ′ ⊢ let (y, z) = new () in close (send (inl y, x)); z : S
∅ ⊢ λx.let (y, z) = new () in close (send (inl y, x)); z : S ⊕o S ′ ⊸⊤,o S
(a) = new : 1 ⊸⊤,o S × S

(b) = close : endo+1
⊸⊤,o+1 1
!

(c) = send : (S + S ′ ) × (S ⊕o S ′ ) ⊸⊤,o endo+1
!

T-Select-Inr

pr(S) = pr(S ′ )

∅ ⊢⊥ select inr : S ⊕o S ′ ⊸⊤,o S ′ ≜
(a)

∅ ⊢ () : 1

∅ ⊢ new () : S ′ × S ′
y : S′ ⊢ y : S′
x : S ⊕o S ′ ⊢ x : S ⊕o S ′

y : S ′ ⊢ inr y : S + S ′
(c)
(b)

x : S ⊕o S ′ , y : S ′ ⊢ (inr y, x) : (S + S ′ ) × (S ⊕o S ′ )
x : S ⊕o S ′ , y : S ′ ⊢ send (inr y, x) : endo+1
!
x : S ⊕o S ′ , y : S ′ ⊢ close (send (inr y, x)) : 1
z : S′ ⊢ z : S′

x : S ⊕o S ′ , y : S ′ , z : S ′ ⊢ close (send (inr y, x)); z : S ′
x : S ⊕o S ′ ⊢ let (y, z) = new () in close (send (inr y, x)); z : S ′
∅ ⊢ λx.let (y, z) = new () in close (send (inr y, x)); z : S ⊕o S ′ ⊸⊤,o S ′
(a) = new : 1 ⊸⊤,o S ′ × S ′

(b) = close : endo+1
⊸⊤,o+1 1
!

(c) = send : (S + S ′ ) × (S ⊕o S ′ ) ⊸⊤,o endo+1
!

Figure 4: Typing Rules for Syntactic Sugar for PGV (T-Select-Inl and T-Select-Inr).

## PDF page 14

28:14

Vol. 19:4

W. Kokke and O. Dardha

T-Offer

Γ ⊢p L : S &o S ′ ∆, x : S ⊢q M : T ∆, y : S ′ ⊢q N : T o ⊔ p < pr(∆, S, S ′ )
Γ, ∆ ⊢o⊔p⊔q offer L {inl x ↦→ M ; inr y ↦→ N } : T
≜

(c)
(b) w : endo+1
⊢⊥ w : endo+1
?
?

w : endo+1
⊢o wait w : 1
?
z : S + S ′ ⊢⊥ z : S + S ′ ∆, x : S ⊢q M : T ∆, y : S ′ ⊢q N : T
∆, z : S + S ′ ⊢q case z {inl x ↦→ M ; inr y ↦→ N } : T

o < pr(∆, S + S ′ )

∆, z : S + S ′ , w : endo+1
⊢o⊔q wait w; case z {inl x ↦→ M ; inr y ↦→ N } : T
?
(a) Γ ⊢p L : ?o (S + S ′ ).endo+1
?

Γ ⊢o⊔p recv L : (S + S ′ ) × endo+1
(c) o ⊔ p < pr(∆)
?
o⊔p⊔q
Γ, ∆ ⊢
let (z, w) = recv L in wait w; case z {inl x ↦→ M ; inr y ↦→ N } : T
⊸⊤,o (S + S ′ ) × endo+1
(a) = recv : ?o (S + S ′ ).endo+1
?
?

⊸⊤,o 1
(b) = wait : endo+1
?

T-Offer-Absurd

Γ ⊢p L : &o {} o ⊔ p < pr(∆)
Γ, ∆ ⊢o⊔p offer L {} : T
≜
(a) Γ ⊢p L : ?o 0.endo+1
?

Γ ⊢o⊔p recv L : 0 × endo+1
?
⊢⊥ w : endo+1
(b) w : endo+1
?
?

z : 0 ⊢⊥ z : 0

⊢o wait w : 1
w : endo+1
?

∆, z : 0 ⊢⊥ absurd z : T

∆, z : 0, w : endo+1
⊢o wait w; absurd z : T
?
o⊔p
Γ, ∆ ⊢

o < pr(∆)
o ⊔ p < pr(∆)

let (z, w) = recv L in wait w; absurd z : T

(a) = recv : ?o 0.endo+1
⊸⊤,o 0 × endo+1
?
?

(b) = wait : endo+1
⊸⊤,o 1
?

Figure 5: Typing Rules for Syntactic Sugar for PGV (T-Offer and T-Offer-Absurd).
Syntactic Sugar Typing. The following typing rules given in Figs. 3 to 5, cover syntactic
sugar typing for PGV.

3. Technical Developments
3.1. Subject Reduction. Unlike with previous versions of GV, structural congruence,
term reduction, and configuration reduction are all type preserving.

## PDF page 15

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:15

We must show that substitution preserves priority constraints. For this, we prove Lemma 3.1,
which shows that values have finished all their communication, and that any priorities in
the type of the value come from the typing environment.
Lemma 3.1. If Γ ⊢p V : T , then p = ⊥, and pr(Γ) = pr(T ).
Proof. By induction on the derivation of Γ ⊢o V : T .
Case T-Var. Immediately.
x : T ⊢⊥ x : T
Case T-Const. Immediately.
∅ ⊢⊥ K : T
Case T-Lam. Immediately.
Γ, x : T ⊢q M : U
Γ ⊢⊥ λx.M : T ⊸pr(Γ),q U
Case T-Unit. Immediately.
∅ ⊢⊥ () : 1
Case T-Pair. The induction hypotheses give us p = q = ⊥, hence p ⊔ q = ⊥, and pr(Γ) =
pr(T ) and pr(∆) = pr(U ), hence pr(Γ, ∆) = pr(Γ) ⊓ pr(∆) = pr(T ) ⊓ pr(U ) = pr(T × U ).
Γ ⊢p V : T
∆ ⊢q W : U
p < pr(∆)
p⊔q
Γ, ∆ ⊢
(V, W ) : T × U
Case T-Inl. The induction hypothesis gives us p = ⊥, and pr(Γ) = pr (T ). We know
pr(T ) = pr(U ), hence pr(Γ) = pr(T + U ).
Γ ⊢p V : T
pr(T ) = pr(U )
p
Γ ⊢ inl V : T + U
Case T-Inr. The induction hypothesis gives us p = ⊥, and pr(Γ) = pr (U ). We know
pr(T ) = pr(U ), hence pr(Γ) = pr(T + U ).
Γ ⊢p V : U
pr(T ) = pr(U )
p
Γ ⊢ inr V : T + U

Lemma 3.2. If Γ, x : U ′ ⊢p M : T and Θ ⊢q V : U ′ , then Γ, Θ ⊢p M {V /x} : T .
Proof. By induction on the derivation of Γ, x : U ′ ⊢p M : T .
Case T-Var. By Lemma 3.1, q = ⊥.
{V /x}

x : U ′ ⊢⊥ x : U ′ −−−→ Θ ⊢⊥ V : U ′

## PDF page 16

28:16

Vol. 19:4

W. Kokke and O. Dardha

Case T-Lam. By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(Γ, Θ) = pr(Γ, U ′ ).
Γ, x : U ′ , y : T ⊢q M : U

Γ, Θ, y : T ⊢q M {V /x} : U
′

{V /x}

Γ, x : U ′ ⊢⊥ λy.M : T ⊸pr(Γ,U ),q U −−−→ Γ, Θ ⊢⊥ λy.M {V /x} : T ⊸pr(Γ,Θ),q U
Case T-App. There are two subcases:
Subcase x ∈ M . Immediately, from the induction hypothesis.
′

′

Γ, x : U ′ ⊢p M : T ⊸p ,q U

∆ ⊢q N : T

p < pr(∆)

q < p′

′

{V /x}

Γ, ∆, x : U ′ ⊢p⊔q⊔q M N : U
′

′

Γ, Θ ⊢p M {V /x} : T ⊸p ,q U

∆ ⊢q N : T

−−−→
q < p′

p < pr(∆)

′

Γ, ∆, Θ ⊢p⊔q⊔q (M {V /x}) N : U
Subcase x ∈ N . By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(∆, Θ) = pr(∆, U ′ ).
′

′

∆, x : U ′ ⊢q N : T

Γ ⊢p M : T ⊸p ,q U

p < pr(∆, U ′ )

q < p′

′

{V /x}

Γ, ∆, x : U ′ ⊢p⊔q⊔q M N : U
′

′

Γ ⊢p M : T ⊸p ,q U

∆, Θ ⊢q N {V /x} : T

−−−→
p < pr(∆, Θ)

q < p′

′

Γ, ∆, Θ ⊢p⊔q⊔q M (N {V /x}) : U
Case T-LetUnit. There are two subcases:
Subcase x ∈ M . Immediately, from the induction hypothesis.
Γ, x : U ′ ⊢p M : 1
∆ ⊢q N : T
p < pr(∆)
{V /x}
′ p⊔q
Γ, ∆, x : U ⊢
M; N : T
−−−→
Γ, Θ ⊢p M {V /x} : 1
∆ ⊢q N : T
p < pr(∆)
p⊔q
Γ, ∆, Θ ⊢
M {V /x}; N : T
Subcase x ∈ N . By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(∆, Θ) = pr(∆, U ′ ).
Γ ⊢p M : 1

∆, x : U ′ ⊢q N : T
p < pr(∆, U ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q M ; N : T
−−−→

Γ ⊢p M : 1

∆, Θ ⊢q N {V /x} : T
p < pr(∆, Θ)
p⊔q
Γ, ∆, Θ ⊢
M ; N {V /x} : T

Case T-Pair. There are two subcases:

## PDF page 17

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:17

Subcase x ∈ M . Immediately, from the induction hypothesis.
Γ, x : U ′ ⊢p M : T
∆ ⊢q N : U
p < pr(∆, U ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q (M, N ) : T × U
−−−→
Γ, Θ ⊢p M {V /x} : T
∆ ⊢q N : U
p < pr(∆, Θ)
p⊔q
Γ, ∆, Θ ⊢
(M {V /x}, N ) : T × U
Subcase x ∈ N . By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(∆, Θ) = pr(∆, U ′ ).
Γ ⊢p M : T
∆, x : U ′ ⊢q N : U
p < pr(∆, U ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q (M, N ) : T × U
−−−→
Γ ⊢p M : T
∆, Θ ⊢q N {V /x} : U
p < pr(∆, Θ)
p⊔q
Γ, ∆, Θ ⊢
(M, N {V /x}) : T × U
Case T-LetPair. There are two subcases:
Subcase x ∈ M . Immediately, from the induction hypothesis.
Γ, x : U ′ ⊢p M : T × T ′
∆, y : T , z : T ′ ⊢q N : U
p < pr(∆, T , T ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q let (y, z) = M in N : U
−−−→
Γ, Θ ⊢p M {V /x} : T × T ′
∆, y : T , z : T ′ ⊢q N : U
p < pr(∆, T , T ′ )
Γ, ∆, Θ ⊢p⊔q let (y, z) = M {V /x} in N : U
Subcase x ∈ N . By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(∆, Θ, T , T ′ ) = pr(∆, U ′ , T , T ′ ).
Γ ⊢p M : T × T ′

∆, x : U ′ , y : T , z : T ′ ⊢q N : U
p < pr(∆, U ′ , T , T ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q let (y, z) = M in N : U
−−−→

Γ ⊢p M : T × T ′

∆, Θ, y : T , z : T ′ ⊢q N {V /x} : U
p < pr(∆, Θ, T , T ′ )
Γ, ∆, Θ ⊢p⊔q let (y, z) = M in N {V /x} : U

Case T-Absurd.
Γ, x : U ′ ⊢p M : 0
Γ, Θ ⊢p M {V /x} : 0
{V
/x}
Γ, ∆, x : U ′ ⊢p absurd M : T −−−→ Γ, ∆, Θ ⊢p absurd M {V /x} : T
Case T-Inl.
Γ, x : U ′ ⊢p M : T
pr(T ) = pr(U )
Γ, Θ ⊢p M {V /x} : T
pr(T ) = pr(U )
{V /x}
′ p
p
Γ, x : U ⊢ inl M : T + U
−−−→
Γ, Θ ⊢ inl M {V /x} : T + U
Case T-Inr.
Γ, x : U ′ ⊢p M : U
pr(T ) = pr(U )
Γ, Θ ⊢p M {V /x} : U
pr(T ) = pr(U )
{V /x}
′ p
p
Γ, x : U ⊢ inr M : T + U
−−−→
Γ, Θ ⊢ inr M {V /x} : T + U
Case T-CaseSum. There are two subcases:

## PDF page 18

28:18

Vol. 19:4

W. Kokke and O. Dardha

Subcase x ∈ L. Immediately, from the induction hypothesis.
Γ, x : U ′ ⊢p L : T + T ′
∆, y : T ⊢q M : U
∆, z : T ′ ⊢q N : U
Γ, ∆, x : U ′ ⊢p⊔q case L {inl y ↦→ M ; inr z ↦→ N } : U

p < pr(∆)

Γ, Θ ⊢p L{V /x} : T + T ′
∆, y : T ⊢q M : U
∆, z : T ′ ⊢q N : U
Γ, ∆, Θ ⊢p⊔q case L{V /x} {inl y ↦→ M ; inr z ↦→ N } : U

{V /x}

−−−→
p < pr(∆)

Subcase x ∈ M and x ∈ N . By Lemma 3.1, pr(Θ) = pr(U ′ ), hence pr(∆, Θ, T ) =
pr(∆, U ′ , T ) and pr(∆, Θ, T ′ ) = pr(∆, U ′ , T ′ ).
Γ ⊢p L : T + T ′
∆, x : U ′ , y : T ⊢q M : U
∆, x : U ′ , z : T ′ ⊢q N : U
p < pr(∆, U ′ )
{V /x}
Γ, ∆, x : U ′ ⊢p⊔q case L {inl y ↦→ M ; inr z ↦→ N } : U
−−−→
Γ ⊢p L : T + T ′
∆, Θ, y : T ⊢q M {V /x} : U
∆, Θ, z : T ′ ⊢q N {V /x} : U
p < pr(∆, Θ)
p⊔q
Γ, ∆, Θ ⊢
case L {inl y ↦→ M {V /x}; inr z ↦→ N {V /x}} : U
We omit the cases where x ̸∈ M , as they are straightforward.
Lemma 3.3. If Γ ⊢p M : T and M −→M M ′ , then Γ ⊢p M ′ : T .
Proof. The proof closely follows the standard proof of subject reduction for the simply-typed
linear λ-calculus, as the constants are uninterpreted by the term reduction (−→M ) and
priority constraints are maintained consequence of § 3.1.
By induction on the derivation of M −→M M ′ .
Case E-Lam. By Lemma 3.2.
Γ, x : T ⊢p M : U
Γ ⊢⊥ λx.M : T ⊸pr(Γ),p U
∆ ⊢⊥ V : T
Γ, ∆ ⊢p (λx.M ) V : U
−→M Γ, ∆ ⊢p M {V /x} : U
Case E-Unit. By Lemma 3.2.
∅ ⊢⊥ () : 1
Γ ⊢p M : T
Γ ⊢p (); M : T
−→M Γ ⊢p M : T
Case E-Pair. By Lemma 3.2.
Γ ⊢⊥ V : T

∆ ⊢⊥ W : T ′

Γ, ∆ ⊢⊥ (V, W ) : T × T ′
Θ, x : T , y : T ′ ⊢p M : U
Γ, ∆, Θ ⊢ let (x, y) = (V, W ) in M : U
−→M
Γ, ∆, Θ ⊢p M {V /x}{W/y} : U

## PDF page 19

Vol. 19:4

PRIORITISE THE BEST VARIATION

Case E-Inl. By Lemma 3.2.
Γ ⊢⊥ V : T
Γ ⊢⊥ inl V : T + T ′
∆, x : T ⊢p M : U
∆, y : T ′ ⊢p N : U
Γ, ∆ ⊢p case inl V {inl x ↦→ M ; inr y ↦→ N } : U
−→M
Γ, ∆ ⊢p M {V /x} : U
Case E-Inr. By Lemma 3.2.
Γ ⊢⊥ V : T ′
Γ ⊢⊥ inr V : T + T ′
∆, x : T ⊢p M : U
∆, y : T ′ ⊢p N : U
Γ, ∆ ⊢p case inr V {inl x ↦→ M ; inr y ↦→ N } : U
−→M
Γ, ∆ ⊢p N {V /y} : U
Case E-Lift. Immediately by induction on the evaluation context E.
Lemma 3.4. If Γ ⊢ϕ C and C ≡ C ′ , then Γ ⊢ϕ C ′ .
Proof. By induction on the derivation of C ≡ C ′ .
Case SC-LinkSwap.
x : S ⊢⊥ x : S
link : S × S ⊸ 1

y : S ⊢⊥ y : S

x : S, y : S ⊢⊥ (x, y) : S × S

x : S, y : S ⊢⊥ link (x, y) : 1
··
·
Γ, x : S, y : S ⊢ϕ F[link (x, y)]
≡
y : S ⊢⊥ y : S
link : S × S ⊸ 1

x : S ⊢⊥ x : S

x : S, y : S ⊢⊥ (y, x) : S × S

x : S, y : S ⊢⊥ link (y, x) : 1
··
·
Γ, x : S, y : S ⊢ϕ F[link (y, x)]

28:19

## PDF page 20

28:20

Vol. 19:4

W. Kokke and O. Dardha

Case SC-ResLink.
x : S ⊢⊥ x : S

y : S ⊢⊥ y : S

x : S, y : S ⊢⊥ (x, y) : S × S

link : S × S ⊸ 1

x : S, y : S ⊢⊥ link (x, y) : 1
x : S, y : S ⊢ϕ ϕ link (x, y)

∅ ⊢ϕ () : 1

∅ ⊢ϕ (νxy)(ϕ link (x, y))

≡ ∅ ⊢ϕ ϕ ()

Case SC-ResSwap.
Γ, x : S, y : S ⊢ϕ C
Γ ⊢ϕ (νxy)C

Γ, x : S, y : S ⊢ϕ C
≡

Γ ⊢ϕ (νyx)C

Case SC-ResComm.
Γ, x : S, y : S, z : S ′ , w : S ′ ⊢ϕ C

Γ, x : S, y : S, z : S ′ , w : S ′ ⊢ϕ C

Γ, x : S, y : S ⊢ϕ (νzw)C

Γ, z : S ′ , w : S ′ ⊢ϕ (νxy)C

Γ ⊢ϕ (νxy)(νzw)C

Γ ⊢ϕ ⊢ (νzw)(νxy)C

≡

Case SC-ResExt.
Γ ⊢ϕ C

∆, x : S, y : S ⊢ϕ D

∆, x : S, y : S ⊢ϕ D

Γ, ∆, x : S, y : S ⊢ϕ (C ∥ D)
Γ, ∆ ⊢ϕ (νxy)(C ∥ D)

∆ ⊢ϕ (νxy)D

Γ ⊢ϕ C

Γ, ∆ ⊢ϕ C ∥ (νxy)D

≡

Case SC-ParNil.
∅ ⊢⊥ () : 1
∅ ⊢◦ ◦()

Γ ⊢ϕ C

Γ ⊢ϕ C ∥ ◦()

≡ Γ ⊢ϕ C

Case SC-ParComm.
′

Γ ⊢ϕ C

′

∆ ⊢ϕ D

∆ ⊢ϕ D

′

Γ ⊢ϕ C

′

Γ, ∆ ⊢ϕ+ϕ (C ∥ D) ≡ Γ, ∆ ⊢ϕ +ϕ (D ∥ C)
Case SC-ParAssoc.
′

′′

∆ ⊢ϕ D
Γ ⊢ϕ C

Θ ⊢ϕ E
′

′′

′

′′

∆ ⊢ϕ D
′

∆, Θ ⊢ϕ +ϕ (D ∥ E)

Γ, ∆, Θ ⊢ϕ+ϕ +ϕ C ∥ (D ∥ E)

′

Γ ⊢ϕ C

Γ, ∆ ⊢ϕ+ϕ (C ∥ D)
≡

′

′′

′′

Θ ⊢ϕ E

Γ, ∆, Θ ⊢ϕ+ϕ +ϕ (C ∥ D) ∥ E

Theorem 3.5. If Γ ⊢ϕ C and C −→C C ′ , then Γ ⊢ϕ C ′ .
Proof. By induction on the derivation of C −→C C ′ .

## PDF page 21

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:21

Case E-New.
x : S ⊢⊥ x : S
∅ ⊢⊥ () : 1

new : 1 ⊸ S × S

y : S ⊢⊥ y : S

x : S, y : S ⊢⊥ (x, y) : S × S
··
·

∅ ⊢⊥ new () : S × S
··
·

Γ, x : S, y : S ⊢ϕ F[(x, y)]

Γ ⊢ϕ F[new ()]

Γ ⊢ϕ (νxy)F[(x, y)]

−→C

Case E-Spawn.
spawn : (1 ⊸p,q 1) ⊸ 1 ∆ ⊢⊥ V : 1 ⊸p,q 1
∆ ⊢⊥ spawn V : 1
··
·
Γ, ∆ ⊢ϕ F[spawn V ]
−→C

∅ ⊢⊥ () : 1
··
·

∆ ⊢⊥ V : 1 ⊸p,q 1
∅ ⊢⊥ () : 1
∆ ⊢q V () : 1
∆ ⊢◦ ◦ (V ())

Γ ⊢ϕ F[()]

Γ, ∆ ⊢ϕ F[()] ∥ ◦ (V ())
Case E-Send. See Fig. 6.
Case E-Close.
wait : endo? ⊸⊤,o 1

y : endo? ⊢⊥ y : endo?
o o
y : end? ⊢ wait y : 1

close : endo! ⊸⊤,o 1

x : endo! ⊢⊥ x : endo!
o o
x : end! ⊢ close x : 1

··
·

··
·
Γ, x : endo! ⊢ϕ F[close x]

′

∆, y : endo? ⊢ϕ F ′ [wait y]
′

Γ, ∆, x : endo! , y : endo? ⊢ϕ+ϕ F[close x] ∥ F ′ [wait y]
′

Γ, ∆ ⊢ϕ+ϕ (νxy)(F[close x] ∥ F ′ [wait y])
−→C
∅ ⊢⊥ () : 1
··
·

∅ ⊢⊥ () : 1
··
·

Γ ⊢ϕ F[()]

∆ ⊢ϕ F ′ [()]

′

′

Γ, ∆ ⊢ϕ+ϕ F[()] ∥ F ′ [()]

Case E-LiftC. By induction on the evaluation context G.
Case E-LiftM. By Lemma 3.3.

## PDF page 22

28:22

Vol. 19:4

W. Kokke and O. Dardha

Case E-LiftSC. By Lemma 3.4.

(a)
o

(b)
ϕ+ϕ′

o

Γ, ∆, Θ, x : ! T.S, y : ? T.S ⊢

F[send (V, x)] ∥ F ′ [recv y]

′

Γ, ∆, Θ ⊢ϕ+ϕ (νxy)(F[send (V, x)] ∥ F ′ [recv y])
x : !o T.S ⊢⊥ x : !o T.S
∆ ⊢p V : T
send : T × !o T.S ⊸⊤,o S
∆, x : !o T.S ⊢p (V, x) : T × !o T.S
∆, x : !o T.S ⊢p⊔o send (V, x) : S
··
·
Γ, ∆, x : !o T.S ⊢ϕ F[send (V, x)]

(a) ≜

recv : ?o T.S ⊸⊤,o T × S

y : ?o T.S ⊢⊥ y : ?o T.S

y : ?o T.S ⊢o recv y : T × S
··
·
(b) ≜

′

Θ, y : ?o T.S ⊢ϕ F ′ [recv y]
−→C
∆ ⊢p V : T

∆, y : S ⊢⊥ y : S

x : S ⊢⊥ x : S
··
·

∆, y : S ⊢p (V, y) : T × S
··
·

Γ, x : S ⊢ϕ F[x]

∆, Θ, y : S ⊢ϕ F ′ [(V, y)]

′

′

Γ, ∆, Θ, x : S, y : S ⊢ϕ+ϕ F[x] ∥ F ′ [(V, y)]
′

Γ, ∆, Θ ⊢ϕ+ϕ (νxy)(F[x] ∥ F ′ [(V, y)])
Figure 6: Subject Reduction (E-Send)

3.2. Progress and Deadlock Freedom. PGV satisfies progress, as PGV configurations
either reduce or are in normal form. However, the normal forms may seem surprising at first,
as evaluating a well-typed PGV term does not necessarily produce just a value. If a term
returns an endpoint, then its normal form contains a thread which is ready to communicate
on the dual of that endpoint. This behaviour is not new to PGV.
Let us consider an example, adapted from Lindley and Morris [LM15], in which a term
returns an endpoint linked to an echo server. The echo server receives a value and sends it
back unchanged. Consider the program which creates a new channel, with endpoints x and

## PDF page 23

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:23

x′ , spawns off an echo server listening on x, and then returns x′ :
• let (x, x′ ) = new () in
spawn (λ().echox ); x′

echox ≜ let (y, x) = recv x in
let x = send (y, x) in close x

If we reduce the above program, we get (νxx′ )(◦ echox ∥ • x′ ). Clearly, no more
evaluation is possible, even though the configuration contains the thread ◦ echox , which is
blocked on x. In Corollary 3.14 we will show that if a term does not return an endpoint, it
must produce only a value.
Actions are terms which perform communication actions and which synchronise between
two threads.
Definition 3.6. A term acts on an endpoint x if it is send (V, x), recv x, close x, or
wait x. A term is an action if it acts on some endpoint x.
Ready terms are terms which perform communication actions, either by themselves, e.g.,
creating a new channel or thread, or with another thread, e.g., sending or receiving. It is worth
mentioning that the notion of readiness presented here is akin to live processes introduced by
Caires and Pfenning [CP10, DP22], and poised processes introduced by Pfenning and Griffith
[PG15] and later used by Balzer et al. [BP17, BTP19]. Ready processes like live/poised
processes denote processes that are ready to communicate on their providing channel.
Definition 3.7. A term L is ready if it is of the form E[M ], where M is of the form new,
spawn N , link (x, y), or M acts on x. In the latter case, we say that L is ready to act on
x or is blocked on.
Progress for the term language is standard for GV, and deviates from progress for linear
λ-calculus only in that terms may reduce to values or ready terms, where the definition of
ready terms encompasses all terms whose reduction is struck on some constant K.
Lemma 3.8. If Γ ⊢p M : T and Γ contains only session types, then: (i) M is a value;
(ii) M −→M N for some N ; or (iii) M is ready.
With “Γ contains only session types” we mean that for every x : T ∈ Γ, T is a session
type, i.e., is of the form S.
Canonical forms deviate from those for GV, in that we opt to move all ν-binders to
the top. The standard GV canonical form, alternating ν-binders and their corresponding
parallel compositions, does not work for PGV, since multiple channels may be split across a
single parallel composition.
A configuration either reduces, or it is equivalent to configuration in normal form.
Crucial to the normal form is that each term Mi is blocked on the corresponding channel xi ,
and hence no two terms act on dual endpoints. Furthermore, no term Mi can perform a
communication action by itself, since those are excluded by the definition of actions. Finally,
as a corollary, we get that well-typed terms which do not return endpoints return just a
value:
Definition 3.9. A configuration C is in canonical form if it is of the form
(νx1 x′1 ) . . . (νxn x′n )(◦ M1 ∥ · · · ∥ ◦ Mm ∥ • N ) where no term Mi is a value.
Lemma 3.10. If Γ ⊢• C, there exists some D such that C ≡ D and D is in canonical form.
Proof. We move any ν-binders to the top using SC-ResExt, discard any superfluous occurrences of ◦ () using SC-ParNil, and move the main thread to the rightmost position using
SC-ParComm and SC-ParAssoc.

## PDF page 24

28:24

W. Kokke and O. Dardha

Vol. 19:4

Definition 3.11. A configuration C is in normal form if it is of the form
(νx1 x′1 ) . . . (νxn x′n )(◦ M1 ∥ · · · ∥ ◦ Mm ∥ • V ) where each Mi is ready to act on xi .
Lemma 3.12. If Γ ⊢p L : T is ready to act on x : S ∈ Γ, then the priority bound p is some
priority o, i.e., not ⊥ or ⊤.
Proof. Let L = E[M ]. By induction on the structure of E. M has priority pr(S), and
each constructor of the evaluation context E passes on the maximum of the priorities of its
premises. No rule introduces the priority bound ⊤ on the sequent.
Theorem 3.13. If ∅ ⊢• C and C is in canonical form, then either C −→C D for some D; or
C ≡ D for some D in normal form.
Proof. Let C = (νx1 x′1 ) . . . (νxn x′n )(◦ M1 ∥ · · · ∥ ◦ Mm ∥ • N ). We apply Lemma 3.8 to each
Mi and N . If for any Mi or N we obtain a reduction Mi −→M Mi′ or N −→M N ′ , we apply
E-LiftM and E-LiftC to obtain a reduction on C. Otherwise, each term Mi is ready, and
N is either ready or a value. Pick the ready term L ∈ {M1 , . . . , Mm , N } with the smallest
priority bound.
(1) If L is a new E[new ()], we apply E-New.
(2) If L is a spawn E[spawn M ], we apply E-Spawn.
(3) If L is a link E[link (y, z)] or E[link (z, y)], we apply E-Link.
(4) Otherwise, L is ready to act on some endpoint y : S. Let y ′ : S be the dual endpoint
of y. The typing rules enforce the linear use of endpoints, so there must be a term
L′ ∈ {M1 , . . . , Mm , N } which uses y ′ . L′ must be either a ready term or a value:
(a) L′ is ready. By Lemma 3.12, the priority of L is pr(S). By duality, pr(S) = pr(S).
We cannot have L = L′ , otherwise the action on y ′ would be guarded by the action
on y, requiring pr(S) < pr(S).
The term L′ must be ready to act on y ′ , otherwise the action y ′ would be guarded
by another action with priority smaller than pr (S), which contradicts our choice of
L as having the smallest priority.
Therefore, we have two terms ready to act on dual endpoints. We apply the
appropriate reduction rule, i.e., E-Send or E-Close.
(b) L′ = N and is a value. We rewrite C to put L in the position corresponding to
the endpoint it is blocked on, using SC-ParComm, SC-ParAssoc, and optionally
SC-ResSwap. We then repeat the steps above with the term with the next smallest
priority, until either we find a reduction, or the configuration has reached the desired
normal form.
The argument based on the priority being the smallest continues to hold, since we
know that neither L nor L′ will be picked, and no other term uses y or y ′ .

Corollary 3.14. If ∅ ⊢ϕ C, C ̸−→C , and C contains no endpoints, then C ≡ ϕ V for some
value V .
An immediate consequence of Theorem 3.13 and Corollary 3.14 is that a term which
does not return an endpoint will complete all its communication actions, thus satisfying
deadlock freedom.

## PDF page 25

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:25

4. Relation to Priority CP
Thus far we have presented Priority GV (PGV) together with the relevant technical results.
We remind the reader that this line of work of adding priorities, started with Priority CP
(PCP) [DG18a] where priorities are integrated in Wadler’s Classical Processes (CP), which
is a π-calculus leveraging the correspondence of session types as linear logic propositions
[Wad12]. In his work, Wadler presents a connection (via encoding) of CP and GV. Following
that work, we sat out to understand the connection between the priority versions of CP and
GV, thus comparing PGV and PCP. Before presenting our formal results, we will revisit
PCP in the following section.

4.1. Revisiting Priority CP.
Types. Types (A, B) in PCP are based on classical linear logic propositions, and are defined
by the following grammar:
A, B ::= A ⊗o B | A `o B | 1o | ⊥o | A ⊕o B | A &o B | 0o | ⊤o
Each connective is annotated with a priority o ∈ N.
Types A ⊗o B and A `o B type the endpoints of a channel over which we send or receive
a channel of type A, and then proceed as type B. Types 1o and ⊥[o] type the endpoints of
a channel whose session has terminated, and over which we send or receive a ping before
closing the channel. These two types act as units for A ⊗o B and A `o B, respectively.
Types A ⊕o B and A &o B type the endpoints of a channel over which we can receive
or send a choice between two branches A or B. We have opted for a simplified version
of choice and followed the original Wadler’s CP [Wad14], however types ⊕ and & can be
trivially generalised to ⊕o {li : Ai }i∈I and &o {li : Ai }i∈I , respectively, as in the original PCP
[DG18b].
Types 0o and ⊤o type the endpoints of a channel over which we can send or receive a
choice between no options. These two types act as units for A ⊕o B and A &o B, respectively.

Typing Environments. Typing environments Γ, ∆ associate names to types. Environments
are linear, so two environments can only be combined as Γ, ∆ if their names are distinct,
i.e., fv(Γ) ∩ fv(∆) = ∅.
Γ, ∆ ::= ∅ | Γ, x : A

Type Duality. Duality is an involutive function on types which preserves priorities:
(1o )⊥ = ⊥o
(⊥o )⊥ = 1o

(A ⊗o B)⊥ = A⊥ `o B ⊥
(A `o B)⊥ = A⊥ ⊗o B ⊥

(0o )⊥ = ⊤o
(⊤o )⊥ = 0o

(A ⊕o B)⊥ = A⊥ &o B ⊥
(A &o B)⊥ = A⊥ ⊕o B ⊥

## PDF page 26

28:26

Vol. 19:4

W. Kokke and O. Dardha

Priorities. The function pr(·) returns smallest priority of a type. As with PGV, the type
system guarantees that the top-most connective always holds the smallest priority. The
function pr(·) returns the minimum priority of all types a typing context, or ⊤ if the context
is empty:
pr(1o ) = o
pr(⊥o ) = o

pr(A ⊗o B) = o
pr(A `o B) = o

pr(0o ) = o
pr(⊤o ) = o

pr(A ⊕o B) = o
pr(A &o B) = o

pr(∅) = ⊤ pr(Γ, x : T ) = pr(Γ) ⊓ pr(T )
Terms. Processes (P , Q) in PCP are defined by the following grammar.
P , Q ::= x↔y | (νxy)P | (P ∥ Q) | 0
| x[y].P | x[].P | x(y).P | x().P
| x ◁ inl.P | x ◁ inr.P | x ▷ {inl : P ; inr : Q} | x ▷ {}
Process x↔y links endpoints x and y and forwards communication from one to the other.
(νxy)P , (P ∥ Q) and 0 denote respectively the restriction processes where channel endpoints
x and y are bound together and with scope P , the parallel composition of processes P and
Q and the terminated process.
Processes x[y].P and x(y).P send or receive over channel x a value y and proceed as
process P . Processes x[].P and x().P send and receive an empty value—denoting the closure
of channel x, and continue as P .
Processes x ◁ inl.P and x ◁ inr.P make a left and right choice, respectively and proceed as
process P . Dually, x ▷ {inl : P ; inr : Q} offers both left and right branches, with continuations
P and Q, and x ▷ {} is the empty offer.
We write unbound send as x⟨y⟩.P , which is syntactic sugar for x[z].(y↔z ∥ P ). Alternatively, we could take x⟨y⟩.P as primitive, and let x[y].P be syntactic sugar for (νyz)(x⟨z⟩.P ).
CP takes bound sending as primitive, as it is impossible to eliminate the top-level cut in
terms such as (νyz)(x⟨z⟩.P ), even with commuting conversions. In our setting without
commuting conversions and with more permissive normal forms, this is no longer an issue,
but, for simplicity, we keep bound sending as primitive.
On Commuting Conversions. The main change we make to PCP is removing commuting
conversions. Commuting conversions are necessary if we want our reduction strategy to
correspond exactly to cut (or cycle in [DG18b]) elimination. However, as Lindley and
Morris [LM15] show, all communications that can be performed with the use of commuting
conversions, can also be performed without them, but using structural congruence.
From the perspective of process calculi, commuting conversions behave strangely. Consider the commuting conversion (κ` ) for x(y).P :
(κ` )

(νzz ′ )(x(y).P ∥ Q) =⇒ x(y).(νzz ′ )(P ∥ Q)

As a result of (κ` ), Q becomes blocked on x(y), and any actions Q was able to perform
become unavailable. Consequently, CP is non-confluent:
(νxx′ )(a(y).P ∥ (νzz ′ )(z[].0 ∥ z ′ ().Q))
=⇒+

=⇒
a(y).(νxx′ )(P ∥ (νzz ′ )(z[].0 ∥ z ′ ().Q))

a(y).(νxx′ )(P ∥ Q)

## PDF page 27

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:27

Structural congruence.
SC-LinkSwap
SC-ResLink
SC-ResSwap
SC-ResComm
SC-ResExt
SC-ParNil
SC-ParComm
SC-ParAssoc

x↔y
(νxy)x↔y
(νxy)P
(νxy)(νzw)P
(νxy)(P ∥ Q)
P ∥0
P ∥Q
P ∥ (Q ∥ R)

≡
≡
≡
≡
≡
≡
≡
≡

y↔x
0
(νyx)P
(νzw)(νxy)P
P ∥ (νxy)Q, if x, y ∈
/ fv(P )
P
Q∥P
(P ∥ Q) ∥ R

Reduction.
E-Link
E-Send
E-Close
E-Select-Inl
E-Select-Inr
E-LiftRes

(νxy)(w↔x ∥ P )
(νxy)(x[z].P ∥ x(w).Q)
(νxy)(x[].P ∥ y().Q)
(νxy)(x ◁ inl.P ∥ x ▷ {inl : Q; inr : R})
(νxy)(x ◁ inr.P ∥ x ▷ {inl : Q; inr : R})

P =⇒ P ′
(νxy)P =⇒ (νxy)P ′

E-LiftPar

P =⇒ P ′
P ∥ Q =⇒ P ′ ∥ Q

=⇒
=⇒
=⇒
=⇒
=⇒

E-LiftSC

P ≡ P′

P {w/x}
(νxy)(νzw)(P ∥ Q)
P ∥Q
(νxy)(P ∥ Q)
(νxy)(P ∥ R)
P ′ =⇒ Q′
P =⇒ Q

Q′ ≡ Q

Figure 7: Operational Semantic for PCP.
In PCP, commuting conversions break our intuition that an action with lower priority
occurs before an action with higher priority. To cite Dardha and Gay [DG18b] “if a prefix
on a channel endpoint x with priority o is pulled out at top level, then to preserve priority
constraints in the typing rules [..], it is necessary to increase priorities of all actions after
the prefix on x” by o + 1.
4.2. Operational Semantics. The operational semantics for PCP, given in Fig. 7, is defined
as a reduction relation =⇒ on processes (bottom) and uses structural congruence (top).
Each of the axioms of structural congruence corresponds to the axiom of the same name
for PGV. We write =⇒+ for the transitive closures, and =⇒⋆ for the reflexive-transitive
closures.
The reduction relation is given by a set of axioms and inference rules for context closure.
Reduction occurs under restriction. E-Link reduces a parallel composition with a link into
a substitution. E-Send is the main communication rule, where send and receive processes
sychronise and reduce to the corresponding continuations. E-Close follows the previous rule
and it closes the channel identified by endpoints x and y. E-Select-Inl and E-Select-Inr
are generalised versions of E-Send. They state respectively that a left and right selection
synchronises with a choice offering and reduces to the corresponding continuations. The
last three rules state that reduction is closed under restriction, parallel composition and
structural congruence, respectively.
4.3. Typing Rules. Figure 8 gives the typing rules for our version of PCP. A typing
judgement P ⊢ Γ states that “process P is well typed under the typing context Γ”.

## PDF page 28

28:28

Vol. 19:4

W. Kokke and O. Dardha

T-Res

T-Link

x↔A y ⊢ x : A, y : A⊥

P ⊢ Γ, x : A, y : A⊥
(νxy)P ⊢ Γ

T-Par

P ⊢Γ
Q⊢∆
P ∥ Q ⊢ Γ, ∆

T-Send

T-Close

T-Recv

T-Wait

P ⊢ Γ, y : A, x : B
o < pr(Γ, A, B)
x[y].P ⊢ Γ, x : A ⊗o B
P ⊢ Γ, y : A, x : B
o < pr(Γ, A, B)
x(y).P ⊢ Γ, x : A `o B

T-Halt

0⊢∅

P ⊢Γ
o < pr(Γ)
x[].P ⊢ Γ, x : 1o
P ⊢Γ
o < pr(Γ)
x().P ⊢ Γ, x : ⊥o

T-Select-Inl

P ⊢ Γ, x : A

o < pr(Γ, A, B)
pr(A) = pr(B)
o
x ◁ inl.P ⊢ Γ, x : A ⊕ B

T-Select-Inr

P ⊢ Γ, x : B

o < pr(Γ, A, B)
pr(A) = pr(B)
o
x ◁ inr.P ⊢ Γ, x : A ⊕ B

T-Offer

P ⊢ Γ, x : A
Q ⊢ Γ, x : B
o < pr(Γ, A, B)
x ▷ {inl : P ; inr : Q} ⊢ Γ, x : A &o B

T-Offer-Absurd

o < pr(Γ)
x ▷ {} ⊢ Γ, x : ⊤o

Figure 8: Typing Rules for PCP.

T-Link states that the link process x↔y is well typed under channels x and y having
dual types, respectively A and A⊥ . T-Res states that the restriction process (νxy)P is
well typed under typing context Γ if process P is well typed in Γ augmented with channel
endpoints x and y having dual types, respectively A and A⊥ . T-Par states that the parallel
composition of processes P and Q is well typed under the disjoint union of their respective
typing contexts. T-Halt states that the terminated process 0 is well typed in the empty
context.
T-Send and T-Recv state that the sending and receiving of a bound name y over a
channel x is well typed under Γ and x of type A ⊗o B, respectively A `o B. Priority o is
the smallest among all priorities of the types used by the output or input process, captured
by the side condition o < pr(Γ, A, B).
Rules T-Close and T-Wait type the closure of channel x and are in the same lines as
the previous two rules, requiring that the priority of channel x is the smallest among all
priorities in Γ.
T-Select-Inl and T-Select-Inr type respectively the left x ◁ inl.P and right x ◁ inr.P
choice performed on channel x. T-Offer and T-Offer-Absurd type the offering of a
choice, or empty choice, on channel x. In all the above rules the priority o of channel x is
the smallest with respect to the typing context o < pr(Γ) and types involved in the choice
o < pr(Γ, A, B).
Figure 9 shows how syntactic sugar in PCP is well typed.

## PDF page 29

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:29

T-UnboundSend

P ⊢ Γ, x : B

o < pr (Γ, A, B)

x⟨y⟩.P ⊢ Γ, x : A ⊗ B, y : A⊥
z↔A y ⊢ y : A⊥ , z : A

P ⊢ Γ, x : B

z↔ y ∥ P ⊢ Γ, x : B, y : A⊥ , z : A
A

≜

o < pr (Γ, A, B)

x[z].(z↔ y ∥ P ) ⊢ Γ, x : A ⊗ B, y : A⊥
A

Figure 9: Typing Rules for Syntactic Sugar for PCP.
Finally, since our reduction relation is a strict subset of the reduction relation in the
original [DG18b], we defer to their proof of subject reduction (Theorem 2 in [DG18b]). We
prove progress for our version of PCP, see § 4.5.
4.4. PCP and PLL. In this subsection, we highlight the connection between PCP and
linear logic. Dardha and Gay [DG18a] present PCP–consequently also PCP given in this
paper–in a way which can be viewed both as Classical Processes with restriction (T-Res)
and parallel composition (T-Par) typing rules, and as a new version of linear logic, which
they call Priority Linear Logic (PLL). PLL builds on CLL by replacing the cut rule with two
logical rules: a mix and a cycle rule—here corresponding to T-Par and T-Res, respectively.
Dardha and Gay [DG18a, §4] prove cycle-elimination, in the same lines as cut-elimination
for CLL. As a corollary of cycle-elimination for PLL, we obtain deadlock freedom for PCP
(Theorem 3 in [DG18a, §4]). In summary, PLL is an extension of CLL and the authors show
the correspondence of PCP and PLL. Notice however, that PCP is not in correspondence
with CLL itself, since processes in PCP are graphs, whether CLL induces trees.
4.5. Technical Developments.
Definition 4.1. A process acts on an endpoint x if it is x↔y, y↔x, x[y].P , x(y).P , x[].P ,
x().P , x ◁ inl.P , x ◁ inr.P , x ▷ {inl : P ; inr : Q}, or x ▷ {}. A process is an action if it acts
on some endpoint x.
Definition 4.2. A process P is in canonical form if it is either 0 or of the form
(νx1 x′1 ). . . (νxn x′n )(P1 ∥ · · · ∥ Pm ) where m > 0 and each Pj is an action.
Lemma 4.3. If P ⊢ Γ, there exists some Q such that P ≡ Q and Q is in canonical form.
Proof. If P = 0, we are done. Otherwise, we move any ν-binders to the top using SC-ResExt,
and discard any superfluous occurrences of 0 using SC-ParNil.
The proof for progress (below) follows the same reasoning by Kobayashi [Kob06] used
in the proof of deadlock freedom for closed processes (Theorem 2).
Theorem 4.4. If P ⊢ ∅, then either P = 0 or there exists a Q such that P =⇒ Q.
Proof (Sketch). This proof follows the exact same reasoning and proof sketch given by
Kobayashi in [Kob06] and later adopted by Dardha and Gay for PCP in their technical
report [DG18b].

## PDF page 30

28:30

W. Kokke and O. Dardha

Vol. 19:4

By Lemma 4.3, we rewrite P to canonical form. If the resulting process is 0, we are
done. Otherwise, it is of the form
(νx1 x′1 ). . . (νxn x′n )(P1 ∥ · · · ∥ Pm ) ⊢ ∅
where m > 0 and each Pi ⊢ Γi is an action.
Consider processes P1 ∥ · · · ∥ Pm . Among them, we pick the process with the smallest
priority pr (Γi ) for all i. Let this process be Pi and the priority of the top prefix be o. Pi acts
on some endpoint y : A ∈ Γi . We must have pr (Γi ) = pr (A) = o, since the other actions in
Pi are guarded by the action on y : A, thus satisfying law (i) of priorities.
If Pi is a link y↔z or z↔y, we apply E-Link.
Otherwise, Pi is an input/branching or output/selection action on endpoint y of type A
with priority o. Since process P is closed and consequently it respects law (ii) of priorities,
there must be a co-action y ′ of type A⊥ where y and y ′ are dual endpoints of the same
channel (by application of rule T-Res). By duality, pr (A) = pr (A⊥ ) = o. In the following
we show that: y ′ is the subject of a top level action of a process Pj with i ̸= j. This allows
for the communication among Pi and Pj to happen immediately over channel endpoints y
and y ′ .
Suppose that y ′ is an action not in a different parallel process Pj but rather of Pi itself.
That means that the action on y ′ must be prefixed by the action on y, which is top level in
Pi . To respect law (i) of priorities we must have o < o, which is absurd. This means that y ′
is in another parallel process Pj for i ̸= j.
Suppose that y ′ in Pj is not at top level. In order to respect law (i) of priorities, it
means that y ′ is prefixed by actions that are smaller than its priority o. This leads to a
contradiction because stated that o is the smallest priority. Hence, y ′ must be the subject of
a top level action.
We have two processes, acting on dual endpoints. We apply the appropriate reduction
rule, i.e., E-Send, E-Close, E-Select-Inl, or E-Select-Inr.

4.6. Correspondence between PGV and PCP. We illustrate the relation between PCP
and PGV by defining a translation L·MC from PCP processes to PGV configurations which
satisfies operational correspondence.
The translation L·MC translates PCP processes to PGV configurations by translating
as much as possible of the π-calculus constructs from PCP to the identical configuration
constructs in PGV, i.e., all top-level ν and ∥ constructs. When it encounters the first
action, it translates the remainder of the processs to a term using L·MM . The translation L·MM
translates PCP processes to PGV terms by mapping the π-calculus constructs from PCP
(e.g., ν, ∥, ·[·].·, ·[·].·, ·(·).·, etc.) to the corresponding constants in PGV (e.g., new, spawn,
send, recv, etc.). Translating a process with L·MC is the same as translating that process
with L·MM followed by several steps of configuration reduction. The translation L·M tranlates
session types from PCP to session types in PGV matching the translation on processes.
The translation on types is defined as follows:
LA ⊗o BM = !o LAM.LBM
LA ⊕o BM = LAM ⊕o LBM

LA `o BM = ?o LAM.LBM
LA &o BM = LAM &o LBM

L1o M = endo!
L0o M = ⊕o {}

L⊥o M = endo?
L⊤o M = &o {}

## PDF page 31

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:31

The translation L·MM translates processes to terms and maps the π-calculus constructs
from PCP to the corresponding constants in PGV:
Lx↔yMM

= link (x, y)

L(νxy)P MM

= let (x, y) = new () in LP MM

L0MM

= ()

LP ∥ QMM
Lx[].P MM
Lx().P MM

Lx[y].P MM

= spawn (λ().LP MM ); LQMM
= close x; LP MM
= wait x; LP MM

= let (y, z) = new () in let x = send (z, x) in LP MM

Lx(y).P MM

= let (y, x) = recv x in LP MM

Lx ◁ inr.P MM

= let x = select inr x in LP MM

Lx ◁ inl.P MM

Lx ▷ {inl : P ; inr : Q}MM
Lx ▷ {}MM

= let x = select inl x in LP MM

= offer x {inl x ↦→ LP MM ; inr x ↦→ LQMM }
= offer x {}

Unfortunately, the operational correspondence along L·MM is unsound, as it translates
ν-binders and parallel compositions to new and spawn, which can reduce to their equivalent
configuration constructs using E-New and E-Spawn. The same goes for ν-binders which are
inserted when translating bound send to unbound send. For instance, the process x[y].P is
blocked, but its translation uses new and can reduce. To address this issue, we introduce
a second translation, L·MC , which is equivalent to translating with L·MM then reducing with
E-New and E-Spawn:
L(νxy)P MC

LP ∥ QMC

= (νxy)LP MC

= LP MC ∥ LQMC

Lx[y].P MC

= (νyz)(◦ let x = send (z, x) in LP MM )

Lx ◁ inr.P MC

= (νyz)(◦ let x = close (send (inr y, x)); z in LP MM )

Lx ◁ inl.P MC
LP MC

= (νyz)(◦ let x = close (send (inl y, x)); z in LP MM )
= ◦LP MM ,

if none of the above apply

Typing environments are translated pointwise, and sequents P ⊢ Γ are translated as LΓM ⊢◦ LP MC ,
where ◦ indicates a child thread, since translated processes do not have a main thread.
The translations L·MM and L·MC preserve typing, and the latter induces a sound and complete
operational correspondence.
Lemma 4.5. If P ⊢ Γ, then LΓM ⊢p LP MM : 1.
Proof. By induction on the derivation of P ⊢ Γ.
Case T-Link, T-Res, T-Par, and T-Halt. See Fig. 10.
Case T-Close, and T-Wait. See Fig. 11.
Case T-Send. See Fig. 12.
Case T-Recv. See Fig. 13.

## PDF page 32

28:32

Vol. 19:4

W. Kokke and O. Dardha

T-Link

L·MM
x↔A y ⊢ x : A, y : A⊥ −−−→
x : LAM ⊢⊥ x : LAM

y : LAM ⊢⊥ y : LAM

x : LAM, y : LAM ⊢⊥ (x, y) : LAM × LAM

link : LAM × LAM ⊸ 1

x : LAM, y : LAM ⊢⊥ link (x, y) : 1
T-Res

P ⊢ Γ, x : A, y : A⊥
L·MM
−−−→
(νxy)P ⊢ Γ

new : 1 ⊸ LAM × LAM

∅ ⊢⊥ () : 1

∅ ⊢⊥ new () : LAM × LAM
LΓM, x : LAM, y : LAM ⊢p LP MM : 1
LΓM ⊢p let (x, y) = new () in LP MM : 1
T-Par

P ⊢Γ
Q⊢∆
L·MM
P ∥ Q ⊢ Γ, ∆
−−−→

spawn : (1 ⊸pr (Γ),p 1) ⊸ 1

LΓM ⊢p LP MM : 1

LΓM ⊢⊥ λ().LP MM : 1 ⊸pr (Γ),p 1

LΓM ⊢⊥ spawn (λ().LP MM ) : 1
LΓM, L∆M ⊢q spawn (λ().LP MM ); LQMM : 1

L∆M ⊢q LQMM : 1

T-Halt

0⊢∅

L·MM
−−−→ ∅ ⊢⊥ () : 1

Figure 10: Translation L·MM preserves typing (T-Link, T-Res, T-Par, and T-Halt).

Case T-Select-Inl, T-Select-Inr, and T-Offer. See Fig. 14.
Theorem 4.6. If P ⊢ Γ, then LΓM ⊢◦ LP MC .
Proof. By induction on the derivation of P ⊢ Γ.
Case T-Res. Immediately, from the induction hypothesis.
T-Res

Γ, x : A, y : A⊥ ⊢ P
LΓM, x : LAM, y : LBM ⊢◦ LP MC
L·MC
Γ ⊢ (νxy)P
−−−→
LΓM ⊢◦ (νxy)LP MC

## PDF page 33

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:33

T-Close

P ⊢Γ
o < pr(Γ)
L·MM
x[].P ⊢ Γ, x : 1o
−−−→

close : endo! ⊸⊤,o 1
x : endo! ⊢⊥ x : endo!
x : endo! ⊢o close x : 1
LΓM ⊢p LP MM : 1
LΓM, x : endo! ⊢o⊔p close x; LP MM : 1

o < pr(LΓM)

T-Wait

P ⊢Γ
o < pr(Γ)
L·MM
x().P ⊢ Γ, x : 1o
−−−→

wait : endo? ⊸⊤,o 1
x : endo? ⊢⊥ x : endo?
LΓM ⊢p LP MM : 1
x : endo? ⊢o wait x : 1
LΓM, x : endo? ⊢o⊔p wait x; LP MM : 1

o < pr(LΓM)

Figure 11: Translation L·MM preserves typing (T-Close and T-Wait).
T-Send

P ⊢ Γ, y : A, x : B
o < pr(Γ, A, B)
L·MM
x[y].P ⊢ Γ, x : A ⊗o B
−−−→
(a)

∅ ⊢⊥ () : 1

new : 1 ⊸ LAM × LAM

∅ ⊢⊥ new () : LAM × LAM

(b)

send : LAM × !o LAM.LBM ⊸⊤,o LBM

z : LAM ⊢⊥ x : LAM

x : !o LAM.LBM ⊢⊥ x : !o LAM.LBM

x : !o LAM.LBM, z : LAM ⊢⊥ (z, x) : LAM × !o LAM.LBM
x : !o LAM.LBM, z : LAM ⊢o send (z, x) : LBM

(b)
(a)

o

LΓM, y : LAM, x : LBM ⊢p LP MM : 1

LΓM, x : ! LAM.LBM, y : LAM, z : LAM ⊢

o⊔p

o < pr(LΓM, LAM, LBM)

let x = send (z, x) in LP MM : 1

LΓM, x : !o LAM.LBM ⊢o⊔p let (y, z) = new () in let x = send (z, x) in LP MM : 1
Figure 12: Translation L·MM preserves typing (T-Send).

## PDF page 34

28:34

W. Kokke and O. Dardha

Vol. 19:4

T-Recv

P ⊢ Γ, y : A, x : B
o < pr(Γ, A, B)
L·MM
x(y).P ⊢ Γ, x : A `o B
−−−→

(a)

recv : ?o LAM.LBM ⊸⊤,o LAM × LBM
x : ?o LAM.LBM ⊢⊥ x : ?o LAM.LBM
x : ?o LAM.LBM ⊢o recv x : LAM × LBM
LΓM, y : LAM, x : LBM ⊢p LP MM : 1
o < pr(LΓM, LAM, LBM)
o
o⊔p
LΓM, x : ? LAM.LBM, y : LAM, z : LAM ⊢
let x = recvx in LP MM : 1
(a)

Figure 13: Translation L·MM preserves typing (T-Recv).
T-Select-Inl

P ⊢ Γ, x : A
o < pr(Γ)
L·MM
x ◁ inl.P ⊢ Γ, x : A ⊕o B −−−→

select inl : LAM ⊕o LBM ⊸⊤,o LAM
x : LAM ⊕o LBM ⊢⊥ x : LAM ⊕o LBM
x : LAM ⊕o LBM ⊢o select inl x : LAM
Γ, x : LAM ⊢p LP MM : 1
o < pr(Γ)
o
o⊔p
Γ, x : LAM ⊕ LBM ⊢
let x = select inl x in LP MM : 1
T-Select-Inr

P ⊢ Γ, x : A
o < pr(Γ)
L·MM
x ◁ inr.P ⊢ Γ, x : A ⊕o B −−−→

select inr : LAM ⊕o LBM ⊸⊤,o LBM
x : LAM ⊕o LBM ⊢⊥ x : LAM ⊕o LBM
x : LAM ⊕o LBM ⊢o select inr x : LBM
Γ, x : LBM ⊢p LP MM : 1
o < pr(Γ)
o
o⊔p
Γ, x : LAM ⊕ LBM ⊢
let x = select inr x in LP MM : 1
T-Offer

P ⊢ Γ, x : A
Q ⊢ Γ, x : B
o < pr(Γ, A, B)
L·MM
x ▷ {inl : P ; inr : Q} ⊢ Γ, x : A &o B
−−−→

x : LAM &o LBM ⊢⊥ x : LAM &o LBM
LΓM, x : LAM ⊢ LP MM : 1
LΓM, x : LBM ⊢p LQMM : 1
o < pr(LΓM, LAM, LBM)
o
o⊔p
LΓM, x : LAM & LBM ⊢
offer x {inl x ↦→ LP MM ; inr x ↦→ LQMM } : 1
p

Figure 14: Translation L·MM preserves typing (T-Select-Inl, T-Select-Inr, and T-Offer).

## PDF page 35

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:35

Case T-Par. Immediately, from the induction hypotheses.
T-Par

LΓM ⊢◦ LP MC
L∆M ⊢◦ LQMC
Γ⊢P
∆⊢Q
L·MC
−−−→ LΓM, L∆M ⊢◦ LP MC ∥ LQMC
Γ, ∆ ⊢ P ∥ Q

Case *. By Lemma 4.5
LΓM ⊢p LP MM : 1
L·MC
Γ ⊢ P −−−→ LΓM ⊢◦ ◦ LP MM

Theorem 4.7. If P ⊢ Γ and LP MC −→C C, there exists a Q such that P =⇒+ Q and
C −→⋆C LQMC

Proof. By induction on the derivation of LP MC −→C C. We omit the cases which cannot
occur as their left-hand side term forms are not in the image of the translation function, i.e.,
E-New, E-Spawn, and E-LiftM.
Case E-Link.
(νxx′ )(F[link (w, x)] ∥ C) −→C F[()] ∥ C{w/x′ }

The source for link (w, x) must be w↔x. None of the translation rules introduce an evaluation context around the recursive call, hence F must be the empty context. Let P be the
source term for C, i.e., LP MC = C. Hence, we have:
=⇒

(νxx′ )(w↔x ∥ P )

P {w/x′ }

L·MC

(νxx′ )(◦ link (w, x) ∥ LP MC )

L·MC

−→+
C

=

LP MC {w/x′ }

LP {w/x′ }MC

Case E-Send.
(νxx′ )(F[send (V, x)] ∥ F ′ [recv x′ ]) −→C (νxx′ )(F[x] ∥ F ′ [(V, x′ )])
There are three possible sources for send and recv: x[y].P and x′ (y ′ ).Q; x ◁ inl.P and
x′ ▷ {inl : Q; inr : R}; or x ◁ inr.P and x′ ▷ {inl : Q; inr : R}.
Subcase x[y].P and x′ (y ′ ).Q. None of the translation rules introduce an evaluation
context around the recursive call, hence F must be ◦ let x = □ in LP MM . Similarly, F ′ must be
◦ let (y ′ , x′ ) = □ in LQMM . The value V must be an endpoint y, bound by the name restriction
(νyy ′ ) introduced by the translation. Hence, we have:
=⇒

(νxx′ )(x[y].P ∥ x′ (y ′ ).Q)

(νxx′ )(νyy ′ )(P ∥ Q)

L·MC

(νxx′ )(νyy ′ )

(

◦ let x = send (y, x) in LP MM ∥
◦ let (y ′ , x′ ) = recv x′ in LQMM

)
L·MC

≡−→+
C

(νxx′ )(νyy ′ )(◦ LP MM ∥ ◦ LQMM )

−→⋆C

(νxx′ )(νyy ′ )(LP MC ∥ LQMC )

(by Lemma 4.8)

## PDF page 36

28:36

Vol. 19:4

W. Kokke and O. Dardha

Subcase x ◁ inl.P and x′ ▷ {inl : Q; inr : R}. None of the translation rules introduce an
evaluation context around the recursive call, hence F must be

Similarly, F ′ must be

◦ let x = close □; y in LP MM .

◦ let (y ′ , x′ ) = □ in wait x′ ; case y ′

{
}
inl y ′ ↦→ LQMM ; inr y ′ ↦→ LRMM .

Hence, we have:
(νxx′ )(x ◁ inl.P ∥ x ▷ {inl : Q; inr : R})

=⇒

(νxx′ )(P ∥ Q)

L·MM

(νxx′ )

(

◦ let x = select inl x in LP MM ∥
◦ offer x′ {inl x′ ↦→ LQMM ; inr x′ ↦→ LRMM }

)
L·MC

−→+
C

(νxx′ )(◦ LP MM ∥ ◦ LQMM )

−→⋆C
(by Lemma 4.8)

(νxx′ )(LP MC ∥ LQMC )

Subcase x ◁ inr.P and x′ ▷ {inl : Q; inr : R}. None of the translation rules introduce an
evaluation context around the recursive call, hence F must be

Similarly, F ′ must be

◦ let x = close □; y in LP MM .

◦ let (y ′ , x′ ) = □ in wait x′ ; case y ′

{
}
inl y ′ ↦→ LQMM ; inr y ′ ↦→ LRMM .

Hence, we have:
(νxx′ )(x ◁ inr.P ∥ x ▷ {inl : Q; inr : R})

=⇒

(νxx′ )(P ∥ Q)

L·MM

(νxx′ )

(

◦ let x = select inr x in LP MM ∥
◦ offer x′ {inl x′ ↦→ LQMM ; inr x′ ↦→ LRMM }

)
L·MC

−→+
C

(νxx′ )(◦ LP MM ∥ ◦ LRMM )

−→⋆C
(by Lemma 4.8)

(νxx′ )(LP MC ∥ LRMC )

Case E-Close.
(νxx′ )(F[wait x] ∥ F ′ [close x′ ]) −→C F[()] ∥ F ′ [()]
The source for wait and close must be x().P and x′ [].Q.
(The translation for x ▷ {inl : P ; inr : Q} also introduces a wait, but it is blocked on
another communication, and hence cannot be the first communication on a translated term.
The translations for x ◁ inl.P and x ◁ inr.P also introduce a close, but these are similarly
blocked.)

## PDF page 37

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:37

None of the translation rules introduce an evaluation context around the recursive call,
hence F must be □; LP MM . Similarly, F ′ must be □; LQMM . Hence, we have:
(νxx′ )(x[].P ∥ x′ ().Q)

=⇒

P ∥Q

L·MM

(νxx′ )(◦ close x; LP MM ∥ ◦ wait x′ ; LQMM )

L·MC

−→+
C

◦ LP MM ∥ ◦ LQMM

−→⋆C
(by Lemma 4.8)

LP MC ∥ LQMC

Case E-LiftC. By the induction hypothesis and E-LiftC.
Case E-LiftSC. By the induction hypothesis, E-LiftSC, and Lemma 4.9.
Lemma 4.8. For any P , either:
• ◦ LP MM = LP MC ; or
⋆
• ◦ LP MM −→+
C LP MC , and for any C, if ◦ LP MM −→C C, then C −→C LP MC .
Proof. By induction on the structure of P .
Case (νxy)P . We have:
L(νxy)P MM

=
−→+
C
−→⋆C
=

◦ let (x, y) = new () in LP MM
(νxy)(◦ LP MM )
(νxy)LP MC
L(νxy)P MC

LP ∥ QMM

=
−→+
C
−→⋆C
=

◦ spawn (λ().LP MM ); LQMM
◦ LP MM ∥ ◦ LQMM
LP MC ∥ LQMC
LP ∥ QMC

Case P ∥ Q.

Case x[y].P .
Lx[y].P MM

= let (y, z) = new () in let x = send (z, x) in LP MM
−→+
(νyz)(◦ let x = send (z, x) in LP MM )
C
= Lx[y].P MC

Case x ◁ inl.P .
Lx[y].P MM

=
≜
−→+
C
=

let x = select inl x in LP MM
let x = let (y, z) = new () in close (send (inl y, x)); z in LP MM
(νyz)(◦ let x = close (send (inl y, x)); z in LP MM )
Lx[y].P MC

## PDF page 38

28:38

Vol. 19:4

W. Kokke and O. Dardha

Case x ◁ inr.P .
=
≜
−→+
C
=

Lx[y].P MM

let x = select inr x in LP MM
let x = let (y, z) = new () in close (send (inr y, x)); z in LP MM
(νyz)(◦ let x = close (send (inr y, x)); z in LP MM )
Lx[y].P MC

Case ∗. In all other cases, ◦ LP MM = LP MC .
Lemma 4.9. If P ⊢ Γ and P ≡ Q, then LP MC ≡ LQMC .
Proof. Every axiom of the structural congruence in PCP maps directly to the axiom of the
same name in PGV.
Theorem 4.10.
If P ⊢ Γ and P =⇒ Q, then LP MC −→+
C LQMC .
Proof. By induction on the derivation of P =⇒ Q.
Case E-Link.
=⇒

(νxx′ )(w↔x ∥ P )

P {w/x′ }

L·MC

(νxx′ )(◦ link (w, x) ∥ LP MC )

L·MC

−→+
C

=

LP MC {w/x′ }

LP {w/x′ }MC

Case E-Send.
=⇒

(νxx′ )(x[y].P ∥ x′ (y ′ ).Q)

(νxx′ )(νyy ′ )(P ∥ Q)

L·MM

 (
) 
let (y, y ′ ) = new () in
◦
∥
(νxx′ )  let x = send (y, x) in LP MM
′
′
′
◦ let (y , x ) = recv x in LQMM

L·MC

−→+
C

(νxx′ )(νyy ′ )(◦ LP MM ∥ ◦ LQMM )

−→⋆C
(by Lemma 4.8)

(νxx′ )(νyy ′ )(LP MC ∥ LQMC )

Case E-Close.
(νxx′ )(x[].P ∥ x′ ().Q)

=⇒

P ∥Q

L·MM

(νxx′ )(◦ close x; LP MM ∥ ◦ wait x′ ; LQMM )

L·MC

−→+
C

◦ LP MM ∥ ◦ LQMM

−→⋆C
(by Lemma 4.8)

LP MC ∥ LQMC

## PDF page 39

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:39

Case E-Select-Inl.
=⇒

(νxx′ )(x ◁ inl.P ∥ x ▷ {inl : Q; inr : R})

(νxx′ )(P ∥ Q)

L·MM

(νxx′ )

(

◦ let x = select inl x in LP MM ∥
◦ offer x′ {inl x′ ↦→ LQMM ; inr x′ ↦→ LRMM }

)
L·MC

−→+
C

(νxx′ )(◦ LP MM ∥ ◦ LQMM )

−→⋆C
(by Lemma 4.8)

(νxx′ )(LP MC ∥ LQMC )

Case E-Select-Inr.
=⇒

(νxx′ )(x ◁ inr.P ∥ x ▷ {inl : Q; inr : R})

(νxx′ )(P ∥ R)

L·MM

(νxx′ )

(

◦ let x = select inr x in LP MM ∥
◦ offer x′ {inl x′ ↦→ LQMM ; inr x′ ↦→ LRMM }

)
L·MC

−→+
C

(νxx′ )(◦ LP MM ∥ ◦ LRMM )

−→⋆C
(by Lemma 4.8)

(νxx′ )(LP MC ∥ LRMC )

Case E-LiftRes. By the induction hypothesis and E-LiftC.
Case E-LiftPar. By the induction hypotheses and E-LiftC.
Case E-LiftSC. By the induction hypothesis, E-LiftSC, and Lemma 4.9.

5. Milner’s Cyclic Scheduler
As an example of a deadlock-free cyclic process, Dardha and Gay [DG18b] introduce an
implementation of Milner’s cyclic scheduler [Mil89] in Priority CP. We reproduce that
scheduler here, and show its translation to Priority GV.
Example 5.1. A set of processes P roci , 1 ≤ i ≤ n, is scheduled to perform some tasks in
cyclic order, starting with P roc1 , ending with P rocn , and notifying P roc1 when all processes
have finished.
Our scheduler Sched consists of set of agents Agenti , 1 ≤ i ≤ n, each representing their
respective process. Each process P roci waits for the signal to start their task on a′i , and
signals completion on b′i . Each agent signals their process to start on ai , waits for their
process to finish on bi , and then signals for the next agent to continue on ci . The agent
Agent1 initiates, then waits for every other process to finish, and signals P roc1 on d. Every
other agent Agenti , 2 ≤ i ≤ n waits on c′i−1 for the signal to start. Each of the channels in
the scheduler is of a terminated type, and is merely used to synchronise.
Below is a diagram of our scheduler instantiated with three processes:

## PDF page 40

28:40

Vol. 19:4

W. Kokke and O. Dardha

optional
data transfer

P roc1
d′ a′ b′
1
1
d

a1 b1
Agent1

c′3

c1
c′1

c3
Agent3

c′2

c2

Agent2

a3
a′3
P roc3

a2
b3

b′3

a′2

b2
b′2

P roc2

∏
We implement the scheduler as follows, using I Pi to denote the parallel composition of
the processes Pi , i ∈ I, and P [Q] to denote the plugging of Q in the one-hole process-context
P . The process-contexts Pi represent the computations performed by each process P roci .
The process-contexts Qi represent any post-processing, and any possible data transfer from
P roci to P roci+1 . Finally, Q1 should contain d′ ().
Sched
Agent1
Agenti
P roci

′
′
′
′
′
≜ (νa1 a′1 ). . . (νan a′n )(νb
1 c1 ). . . (νcn cn )(νdd )
∏ 1 b1 ). . . (νbn bn )(νc
′
(P roc1 ∥ Agent1 ∥ 2≤i≤n (P roci ∥ ci−1 ().Agenti ))
≜ ai [].bi ().ci [].c′n ().d[].0
≜ ai [].bi ().ci [].0
≜ a′i ().Pi [b′i [].Qi ]

Example 5.2. The PGV scheduler has exactly the
∏ same behaviour as the PCP version
in Example 5.1. It is implemented as follows, using I Ci to denote the parallel composition
of the processes Ci , i ∈ I, and M [N ] to denote the plugging of N in the one-hole termcontext M . For simplicity, we let sched be a configuration. The terms Mi represent the
computations performed by each process proci . The terms Ni represent any post-processing,
and any possible data transfer from proci to proci+1 . Finally, N1 should contain wait d′ .
sched

agenti
proci

≜ (νa1 a′1 ) . . . (νan a′n )(νb1 b′1 ) . . . (νbn b′n )(νc1 c′1 ) . . . (νcn c′n )(νdd′ )
′
( ϕ
∏proc1 ∥ ◦ agent1 ; wait c′n ; close d
∥
2≤i≤n (◦ proci ∥ ◦ wait ci−1 ; agenti ) )
≜ close ai ; wait bi ; close ci
≜ wait a′i ; Mi [close b′i ; Ni ]

If LPi MM = Mi and LQi MM = Ni , then the translation of Sched (Example 5.1), LSched MC ,
is exactly sched (Example 5.2).

## PDF page 41

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:41

6. Related Work and Conclusion

Deadlock freedom and progress. Deadlock freedom and progress are well studied properties
in the π-calculus. For the “standard” typed π-calculus—types for channels used in input
and output, an important line of work stems from Kobayashi’s approach to deadlock freedom [Kob98], where priorities are values from an abstract poset. Kobayashi [Kob06] simplifies
the abstract poset to pairs of naturals, called obligations and capabilities. Padovani simplifies
these further to a single natural, called a priority [Pad14], and adapts obligations/capabilities
to session types [Pad13]. Later work by Kobayashi and co-authors [GKL14, KL17] address
deadlock detection for a value-passing CCS (a predecessor of the π-calculus) where the
number of nodes in a network is arbitrary, namely modelling unbounded networks. The
authors define a sound inference algorithm for their type system, which guarantees deadlock
freedom for these more complex kinds of communication networks. This type system is more
expressive than previous work by Kobayashi.
For the session-typed π-calculus, an important line of work stems from Dezani and
co-authors. In their work, Dezani et al. [DCMYD06] guarantee progress by allowing only
one active session at a time. As sessions do not interleave, consequently they do not
deadlock. Later on, Dezani et al. [DCdY07] introduce a partial order on channels, similar to
Kobayashi [Kob98] and produce a type system for progress.
Carbone and Debois [CD10] define progress for session-typed π-calculus in terms of a
catalyser, which provides the missing counterpart to a process. Intuitively, either the process
is deadlock-free in which case the catalyser is structurally congruent to the inaction process, or
if the process is “stuck” for e.g., an input process x(y).0 (using CP syntax) then the catalyser
simply provides the missing output required for communication. Carbone et al. [CDM14] use
catalysers to show that progress is a compositional form of livelock freedom and can be lifted to
session types via the encoding of session types to linear types [Kob07, DGS12, Dar14, DGS17].
In this work, Carbone et al. [CDM14] sistematise and compare different notions of liveness
properties: progress, deadlock freedom and livelock freedom. Their technique of using the
encoding of session types combined with Kobayashi’s type systems for deadlock and livelock
freedom allows for a more flexible deadlock/livelock detection. It is worth noting that
livelock freedom is a stronger property than deadlock freedom in the presence of recursion,
as the former also discards useless divergent processes; for finite processes the two properties
coincide.
Vieira and Vasconcelos [VV13] use single priorities and an abstract partial order to
guarantee deadlock freedom in a binary session-typed π-calculus and building on conversation
types, which is akin to session types.
While our work focuses on binary session types, it is worth discussing related work on
Multiparty Session Types (MPST), which describe communication among multiple agents
in a distributed setting. The line of work on MPST starts with Honda et al. [HYC08],
which guarantees deadlock freedom within a single session by design, but the property
does not hold for session interleaving. Bettini et al. [BCD+ 08] follow a technique similar to
Kobayashi’s for MPST. The main difference with our work is that we associate priorities with
communication actions, where Bettini et al. [BCD+ 08] associate them with channels. Coppo
et al. [CDPY13, CDYP16] present a deterministic, sound and complete, and compositional
type inference algorithm for an interaction type system, which is used to guarantee global
progress for processes in a calculus based on asynchronous as well as dynamically interleaved

## PDF page 42

28:42

W. Kokke and O. Dardha

Vol. 19:4

and interfered multiparty sessions. The interaction type system allows to infer causalities—
much in the line of Kobayashi’s priorities —of channels, thus guaranteeing that sessiontyped processes do not get stuck at intermediate stages of their sessions. Carbone and
Montesi [CM13] combine MPST with choreographic programming and obtain a formalism
that satisfies deadlock freedom. In the same vein as MPST, choreographic programming
specifies communication among all participants in a distributed system. While MPST target
mainly protocol descriptions, choreographies have mainly targetted implementations and
programming languages as they are suitable for describing concrete system implementations.
Deniélou and Yoshida [DY13] introduce multiparty compatibility, which generalises the
notion of duality in binary session types. They synthesise safe and deadlock-free global types–
specifying communication among all involved participants, from local session types–specifying
communication from the viewpoint of one participant. To do so, they leverage Labelled
Transition Systems (LTSs) and communicating automata. Castellani et al. [CDGH20]
guarantee livelock freedom, a stronger property than deadlock freedom, for MPST with
internal delegation, where participants in the same session are allowed to delegate tasks to
each other, and internal delegation is captured by the global type. Scalas and Yoshida [SY19]
provide a revision of the foundations for MPST, and offer a less complicated and more
general theory, by removing duality/consistency. The type systems is parametric and type
checking is decidable, but allows for a novel integration of model checking techniques. More
protocols and processes can be typed and are guaranteed to be free of deadlocks.
Neubauer and Thiemann [NT04] and Vasconcelos et al. [VRG04, VGR06] introduce
the first functional language with session types. Such works did not guarantee deadlock
freedom until GV [LM15, Wad14]. Toninho et al. [TCP12] present a translation of simplytyped λ-calculus into session-typed π-calculus, but their focus is not on deadlock freedom.
Fowler et al. [FKD+ 21] present Hypersequent GV (HGV), which is a variation of GV that
uses hyper-environments, much in the same line as Hypersequent CP, and enjoys deadlock
freedom, confluence, and strong normalisation.
Ties with logic. The correspondence between logic and types lays the foundation for functional
programming [Wad15]. Since its inception by Girard [Gir87], linear logic has been a candidate
for a foundational correspondence for concurrent programs. A correspondence with linear
π-calculus was established early on by Abramsky [Abr94] and Bellin and Scott [BS94].
Many years later, several correspondences between linear logic and the π-calculus with
binary session types were proposed. Caires and Pfenning [CP10] propose a correspondence
with dual intuitionistic linear logic, while Wadler [Wad12] proposes a correspondence with
classical linear logic. Both works guarantee deadlock freedom as a consequence of adopting
cut elimination. Building on a previous work [CP10], Toninho et al. [TCP13] present a
Curry-Howard correspondence between session types and linear logic for functional language
via linear contextual monads, which are first-class values, thus giving rise to a higher-order
session-typed language. In addition to the more standard results, the authors also prove
a global progress theorem. Qian et al. [QKB21] extend Classical Linear Logic with coexponentials, which allows to model servers receiving requests from an arbitrary set of
clients, yielding an extension to the Curry-Howard correspondence between logic and session
typed processes. Dardha and Gay [DG18b] define Priority CP by integrating Kobayashi
and Padovani’s work on priorities [Kob06, Pad14] with CP, which as described in the
introduction, weakens its ties to linear logic in exchange for expressivity. However, they
show how PCP can be also viewed as a an extension of linear logic, which they call Priority

## PDF page 43

Vol. 19:4

PRIORITISE THE BEST VARIATION

28:43

Linear Logic (PLL), and uses mix and cycle rules as opposed to the cut rule. Dardha and
Pérez [DP18, DP15, DP22] compare priorities à la Kobayashi with tree restrictions à la CP,
and show that the latter is a subsystem of the former. In addition, they give a detailed
account of comparing several type systems for deadlock freedom spanning across session
types, linear logic, and linear types. Carbone et al. [CMSY15, CLM+ 16] give a logical
view of MPST with a generalised duality. Caires and Pérez [CP16] give a presentation of
MPST in terms of binary session types and the use of a medium process which guarantee
protocol fidelity and deadlock freedom. Their binary session types are rooted in linear logic.
Ciobanu and Horne [CH15] give the first Curry-Howard correspondence between MPST and
BV [Gug07], a conservative extension of linear logic with a non-commutative operator for
sequencing. Horne [Hor20] give a system for subtyping and multiparty compatibility where
compatible processes are race free and deadlock free using a Curry-Howard correspondence,
similar to the approach in [CH15]. Balzer et al. [BP17] introduce sharing at the cost of
deadlock freedom, which they restore using worlds, an approach similar to priorities [BTP19].
Staying on sharing, Rocha and Caires [RC21] introduce an imperative feature, that of
shared mutable states into a functional language based on Curry-Howard correspondence
with linear logic. Their type system is thus able to capture programs which were not
possible in previous works. The authors prove extensive technical results, including session
fidelity, progress, confluence and normalisation. Lastly, Jacobs et al. [JBK22] present a novel
technique to guarantee deadlock freedom based on the notion of connectivity graph, which
is an abstract representation of the topology of concurrent systems, and separation logic
used to substructurally treat connectivity graph edges and labels.

Conclusion and Future Work. We answered our research question by presenting Priority
GV, a session-typed functional language which allows cyclic communication structures and
uses priorities to ensure deadlock freedom. We showed its relation to Priority CP [DG18b]
via an operational correspondence.
Our formalism so far only captures the core of GV. In future work, we plan to explore
recursion, following Lindley and Morris [LM16] and Padovani and Novara [PN15], and
sharing, following Balzer and Pfenning [BP17] or Voinea et al. [VDG19].

Acknowledgements. The authors would like to thank the anonymous reviewers for their
detailed feedback, which helped produce a more complete and polished work. Also, the
authors would like to thank Simon Fowler, April Gonçalves, and Philip Wadler for their
comments on the manuscript.

References
[Abr94]
[Bar96]
[BBN+ 18]

Samson Abramsky. Proofs as processes. Theor. Comput. Sci., 135(1):5–9, 1994. doi:10.1016/
0304-3975(94)00103-0.
Andrew Barber. Dual intuitionistic linear logic. 1996. URL: https://www.lfcs.inf.ed.ac.uk/
reports/96/ECS-LFCS-96-347/ECS-LFCS-96-347.pdf.
Jean-Philippe Bernardy, Mathieu Boespflug, Ryan R. Newton, Simon Peyton Jones, and Arnaud
Spiwack. Linear haskell: practical linearity in a higher-order polymorphic language. Proc. of
POPL, 2:1–29, 2018. doi:10.1145/3158093.

## PDF page 44

28:44

[BCD+ 08]

W. Kokke and O. Dardha

Vol. 19:4

Lorenzo Bettini, Mario Coppo, Loris D’Antoni, Marco De Luca, Mariangiola Dezani-Ciancaglini,
and Nobuko Yoshida. Global progress in dynamically interleaved multiparty sessions. In Proc.
of CONCUR, volume 5201 of Lect. Notes Comput. Sci., pages 418–433. Springer, 2008. doi:
10.1007/978-3-540-85361-9_33.
[BP17]
Stephanie Balzer and Frank Pfenning. Manifest sharing with session types. Proc. ACM Program.
Lang., 1(ICFP):37:1–37:29, 2017. doi:10.1145/3110281.
[BS94]
Gianluigi Bellin and Philip J. Scott. On the π-calculus and linear logic. Theor. Comput. Sci.,
135(1):11–65, 1994. doi:10.1016/0304-3975(94)00104-9.
[BTP19]
Stephanie Balzer, Bernardo Toninho, and Frank Pfenning. Manifest deadlock-freedom for shared
session types. In Proc. of ESOP, volume 11423 of Lect. Notes Comput. Sci., pages 611–639.
Springer, 2019. doi:10.1007/978-3-030-17184-1_22.
[CD10]
Marco Carbone and Søren Debois. A graphical approach to progress for structured communication in web services. In Proc. of ICE, volume 38 of Electron. Proc. in Theor. Comput. Sci.,
pages 13–27, 2010. doi:10.4204/EPTCS.38.4.
[CDGH20] Ilaria Castellani, Mariangiola Dezani-Ciancaglini, Paola Giannini, and Ross Horne. Global
types with internal delegation. Theor. Comput. Sci., 807:128–153, 2020. doi:10.1016/j.tcs.
2019.09.027.
[CDM14]
Marco Carbone, Ornela Dardha, and Fabrizio Montesi. Progress as compositional lock-freedom.
In Proc. of COORDINATION, volume 8459 of Lect. Notes Comput. Sci., pages 49–64. Springer,
2014. doi:10.1007/978-3-662-43376-8_4.
[CDPY13]
Mario Coppo, Mariangiola Dezani-Ciancaglini, Luca Padovani, and Nobuko Yoshida. Inference
of global progress properties for dynamically interleaved multiparty sessions. In Proc. of
COORDINATION, volume 7890 of Lect. Notes Comput. Sci., pages 45–59. Springer, 2013.
doi:10.1007/978-3-642-38493-6\_4.
[CDYP16]
Mario Coppo, Mariangiola Dezani-Ciancaglini, Nobuko Yoshida, and Luca Padovani. Global
progress for dynamically interleaved multiparty sessions. Math. Struct. Comput. Sci., 26(2):238–
302, 2016. doi:10.1017/S0960129514000188.
[CH15]
Gabriel Ciobanu and Ross Horne. Behavioural analysis of sessions using the calculus of structures.
In Proc. of PSI, volume 9609 of Lect. Notes Comput. Sci., pages 91–106. Springer, 2015.
doi:10.1007/978-3-319-41579-6_8.
Marco Carbone, Sam Lindley, Fabrizio Montesi, Carsten Schürmann, and Philip Wadler.
[CLM+ 16]
Coherence generalises duality: A logical explanation of multiparty session types. In Proc.
of CONCUR, volume 59 of LIPIcs, pages 33:1–33:15. Leibniz-Zentrum für Informatik, 2016.
doi:10.4230/LIPIcs.CONCUR.2016.33.
[CM13]
Marco Carbone and Fabrizio Montesi. Deadlock-freedom-by-design: Multiparty asynchronous
global programming. In Proc. of POPL, pages 263–274, 2013. doi:10.1145/2480359.2429101.
[CMS18]
Marco Carbone, Fabrizio Montesi, and Carsten Schürmann. Choreographies, logically. Distrib.
Comput., 31(1):51–67, 2018. doi:10.1007/978-3-662-44584-6_5.
[CMSY15]
Marco Carbone, Fabrizio Montesi, Carsten Schürmann, and Nobuko Yoshida. Multiparty
session types as coherence proofs. In Proc. of CONCUR, volume 42 of LIPIcs, pages 412–426.
Leibniz-Zentrum für Informatik, 2015. doi:10.1007/s00236-016-0285-y.
[CP10]
Luı̀s Caires and Frank Pfenning. Session types as intuitionistic linear propositions. In Proc.
of CONCUR, volume 6269 of Lect. Notes Comput. Sci., pages 222–236. Springer, 2010. doi:
10.1007/978-3-642-15375-4_16.
[CP16]
Luı́s Caires and Jorge A. Pérez. Multiparty session types within a canonical binary theory, and
beyond. In Proc. of FORTE, volume 9688 of Lect. Notes Comput. Sci., pages 74–95. Springer,
2016. doi:10.1007/978-3-319-39570-8_6.
[Dar14]
Ornela Dardha. Recursive session types revisited. In Proc. of BEAT, volume 162 of Electron.
Proc. in Theor. Comput. Sci., pages 27–34, 2014. doi:10.4204/EPTCS.162.4.
[DCdY07]
Mariangiola Dezani-Ciancaglini, Ugo de’Liguoro, and Nobuko Yoshida. On progress for structured communications. In Proc. of TGC, volume 4912 of Lect. Notes Comput. Sci., pages
257–275. Springer, 2007. doi:10.1007/978-3-540-78663-4_18.
[DCMYD06] Mariangiola Dezani-Ciancaglini, Dimitris Mostrous, Nobuko Yoshida, and Sophia Drossopoulou.
Session types for object-oriented languages. In Proc. of ECOOP, volume 4067 of Lect. Notes
Comput. Sci., pages 328–352. Springer, 2006. doi:10.1007/11785477_20.

## PDF page 45

Vol. 19:4

[DG18a]

[DG18b]

[DGS12]
[DGS17]
[DP15]

[DP18]
[DP22]
[DY13]

[FKD+ 21]

[Gir87]
[GKL14]

[Gug07]
[GV10]
[Hon93]
[Hor20]

[HVK98]

[HYC08]
[JBK22]

[KD21a]
[KD21b]

[KL17]

PRIORITISE THE BEST VARIATION

28:45

Ornela Dardha and Simon J. Gay. A new linear logic for deadlock-free session-typed processes.
In Proc. of FoSSaCS, volume 10803 of Lect. Notes Comput. Sci., pages 91–109. Springer, 2018.
doi:10.1007/978-3-319-89366-2_5.
Ornela Dardha and Simon J. Gay. A new linear logic for deadlock-free session typed processes. Extended version of [DG18a]. Available at http://www.dcs.gla.ac.uk/~ornela/publications/
DG18-Extended.pdf, 2018.
Ornela Dardha, Elena Giachino, and Davide Sangiorgi. Session types revisited. In Proc. of
PPDP, pages 139–150. ACM, 2012. doi:10.1145/2370776.2370794.
Ornela Dardha, Elena Giachino, and Davide Sangiorgi. Session types revisited. Inf. Comput.,
256:253–286, 2017. doi:10.1016/j.ic.2017.06.002.
Ornela Dardha and Jorge A. Pérez. Comparing deadlock-free session typed processes. In Proc.
of EXPRESS/SOS, volume 190 of Electron. Proc. in Theor. Comput. Sci., pages 1–15, 2015.
doi:10.4204/EPTCS.190.1.
Ornela Dardha and Jorge A. Pérez. Comparing type systems for deadlock-freedom. CoRR,
abs/1810.00635, 2018. URL: http://arxiv.org/abs/1810.00635, arXiv:1810.00635.
Ornela Dardha and Jorge A. Pérez. Comparing type systems for deadlock freedom. J. Log.
Algebraic Methods Program., 124:100717, 2022. doi:10.1016/j.jlamp.2021.100717.
Pierre-Malo Deniélou and Nobuko Yoshida. Multiparty compatibility in communicating automata: Characterisation and synthesis of global session types. In Proc. of ICALP, volume 7966
of Lect. Notes Comput. Sci., pages 174–186. Springer, 2013. doi:10.1007/978-3-642-39212-2_
18.
Simon Fowler, Wen Kokke, Ornela Dardha, Sam Lindley, and J. Garrett Morris. Separating
sessions smoothly. In Proc. of CONCUR, volume 203 of LIPIcs, pages 36:1–36:18. Schloss
Dagstuhl - Leibniz-Zentrum für Informatik, 2021. doi:10.4230/LIPIcs.CONCUR.2021.36.
Jean-Yves Girard. Linear logic. Theor. Comput. Sci., 50:1–102, 1987. doi:10.1016/
0304-3975(87)90045-4.
Elena Giachino, Naoki Kobayashi, and Cosimo Laneve. Deadlock analysis of unbounded process
networks. In Proc. of CONCUR, volume 8704 of Lect. Notes Comput. Sci., pages 63–77. Springer,
2014. doi:10.1007/978-3-662-44584-6\_6.
Alessio Guglielmi. A system of interaction and structure. ACM Trans. Comput. Log., 8(1):1,
2007. doi:10.1145/1182613.1182614.
Simon J. Gay and Vasco T. Vasconcelos. Linear type theory for asynchronous session types. J.
Funct. Program., 20(1):19–50, 2010. doi:10.1017/S0956796809990268.
Kohei Honda. Types for dyadic interaction. In Proc. of CONCUR, volume 715 of Lect. Notes
Comput. Sci., pages 509–523. Springer, 1993. doi:10.1007/3-540-57208-2_35.
Ross Horne. Session subtyping and multiparty compatibility using circular sequents. In Proc.
of CONCUR, volume 171 of LIPIcs, pages 12:1–12:22. Leibniz-Zentrum für Informatik, 2020.
doi:10.4230/LIPIcs.CONCUR.2020.12.
Kohei Honda, Vasco Thudichum Vasconcelos, and Makoto Kubo. Language primitives and type
discipline for structured communication-based programming. In Proc. of ESOP, volume 1381
of Lect. Notes Comput. Sci., pages 122–138. Springer, 1998. doi:10.1007/BFb0053567.
Kohei Honda, Nobuko Yoshida, and Marco Carbone. Multiparty asynchronous session types. In
Proc. of POPL, volume 43(1), pages 273–284. ACM, 2008. doi:10.1145/2827695.
Jules Jacobs, Stephanie Balzer, and Robbert Krebbers. Multiparty GV: functional multiparty
session types with certified deadlock freedom. Proc. ACM Program. Lang., 6(ICFP):466–495,
2022. doi:10.1145/3547638.
Wen Kokke and Ornela Dardha. Deadlock-free session types in Linear Haskell. 2021. URL:
https://arxiv.org/abs/2103.14481.
Wen Kokke and Ornela Dardha. Prioritise the best variation. In Proc. of FORTE, volume 12719
of Lect. Notes Comput. Sci., pages 100–119. Springer, 2021. doi:10.1007/978-3-030-78089-0\
_6.
Naoki Kobayashi and Cosimo Laneve. Deadlock analysis of unbounded process networks. Inf.
Comput., 252:48–70, 2017. doi:10.1016/j.ic.2016.03.004.

## PDF page 46

28:46

[KMP19a]

[KMP19b]

[Kob98]
[Kob06]
[Kob07]
[LM15]
[LM16]
[Mil89]
[MP18]
[NT04]

[Pad13]
[Pad14]
[PG15]

[PN15]

[QKB21]
[RC21]
[SY19]
[TCP12]

[TCP13]

[THK94]

[VDG19]

[VGR06]

[VRG04]

W. Kokke and O. Dardha

Vol. 19:4

Wen Kokke, Fabrizio Montesi, and Marco Peressotti. Better late than never: A fully-abstract
semantics for classical processes. Proc. ACM Program. Lang., 3(POPL), 2019. doi:10.1145/
3290337.
Wen Kokke, Fabrizio Montesi, and Marco Peressotti. Taking linear logic apart. In Proc. of
Linearity & TLLA, volume 292 of Electron. Proc. in Theor. Comput. Sci., pages 90–103. Open
Publishing Association, 2019. doi:10.4204/EPTCS.292.5.
Naoki Kobayashi. A partially deadlock-free typed process calculus. ACM Trans. Program. Lang.
Syst., 20(2):436–482, 1998. doi:10.1145/276393.278524.
Naoki Kobayashi. A new type system for deadlock-free processes. In Proc. of CONCUR, volume
4137 of Lect. Notes Comput. Sci., pages 233–247. Springer, 2006. doi:10.1007/11817949_16.
Naoki Kobayashi. Type systems for concurrent programs. 2007.
Sam Lindley and J. Garrett Morris. A semantics for propositions as sessions. In Proc. of ESOP,
pages 560–584, 2015. doi:10.1007/978-3-662-46669-8_23.
Sam Lindley and J. Garrett Morris. Talking bananas: Structural recursion for session types. In
Proc. of ICFP. ACM, 2016. doi:10.1145/2951913.2951921.
Robin Milner. Communication and Concurrency. Prentice Hall, 1989. doi:10.5555/63446.
Fabrizio Montesi and Marco Peressotti. Classical transitions. 2018. URL: https://arxiv.org/
abs/1803.01049.
Matthias Neubauer and Peter Thiemann. An implementation of session types. In Bharat
Jayaraman, editor, Proc. of PADL, volume 3057 of Lect. Notes Comput. Sci., pages 56–70.
Springer, 2004. doi:10.1007/978-3-540-24836-1\_5.
Luca Padovani. From lock freedom to progress using session types. In Proc. of PLACES, volume
137, pages 3–19. Electron. Proc. in Theor. Comput. Sci., 2013. doi:10.4204/EPTCS.137.2.
Luca Padovani. Deadlock and lock freedom in the linear π-calculus. In Proc. of CSL-LICS,
pages 72:1–72:10. ACM, 2014. doi:10.1145/2603088.2603116.
Frank Pfenning and Dennis Griffith. Polarized substructural session types. In Proc. of FoSSaCS, volume 9034 of Lect. Notes Comput. Sci., pages 3–22. Springer, 2015. doi:10.1007/
978-3-662-46678-0\_1.
Luca Padovani and Luca Novara. Types for deadlock-free higher-order programs. In Proc. of
FORTE, volume 9039 of Lect. Notes Comput. Sci., pages 3–18. Springer, 2015. doi:10.1007/
978-3-319-19195-9_1.
Zesen Qian, G. A. Kavvos, and Lars Birkedal. Client-server sessions in linear logic. Proc. of
ACM Program. Lang., 5(ICFP):1–31, 2021. doi:10.1145/3473567.
Pedro Rocha and Luı́s Caires. Propositions-as-types and shared state. Proc. ACM Program.
Lang., 5(ICFP):1–30, 2021. doi:10.1145/3473584.
Alceste Scalas and Nobuko Yoshida. Less is more: Multiparty session types revisited. Proc.
ACM Program. Lang., 3(POPL), 2019. doi:10.1145/3290343.
Bernardo Toninho, Luı́s Caires, and Frank Pfenning. Functions as session-typed processes. In
Proc. of FoSSaCS, volume 7213 of Lect. Notes Comput. Sci., pages 346–360. Springer, 2012.
doi:10.1007/978-3-642-28729-9_23.
Bernardo Toninho, Luı́s Caires, and Frank Pfenning. Higher-order processes, functions, and
sessions: A monadic integration. In Proc. of ESOP, volume 7792 of Lect. Notes Comput. Sci.,
pages 350–369. Springer, 2013. doi:10.1007/978-3-642-37036-6\_20.
Kaku Takeuchi, Kohei Honda, and Makoto Kubo. An interaction-based language and its typing
system. In Proc. of PARLE, volume 817 of Lect. Notes Comput. Sci., pages 398–413. Springer,
1994. doi:10.1007/3-540-58184-7_118.
A. Laura Voinea, Ornela Dardha, and Simon J. Gay. Resource sharing via capability-based
multiparty session types. In Proc. of IFM, volume 11918 of Lect. Notes Comput. Sci., pages
437–455. Springer, 2019. doi:10.1007/978-3-030-34968-4_24.
Vasco Thudichum Vasconcelos, Simon J. Gay, and António Ravara. Type checking a multithreaded functional language with session types. Theor. Comput. Sci., 368(1-2):64–87, 2006.
doi:10.1016/j.tcs.2006.06.028.
Vasco Vasconcelos, António Ravara, and Simon J. Gay. Session types for functional multithreading. In Proc. of CONCUR, volume 3170 of Lect. Notes Comput. Sci., pages 497–511. Springer,
2004. doi:10.1007/978-3-540-28644-8_32.

## PDF page 47

Vol. 19:4

[VV13]

[Wad12]
[Wad14]
[Wad15]

PRIORITISE THE BEST VARIATION

28:47

Hugo Torres Vieira and Vasco Thudichum Vasconcelos. Typing progress in communicationcentred systems. In Proc. of COORDINATION, volume 7890 of Lect. Notes Comput. Sci., pages
236–250. Springer, 2013. doi:10.1007/978-3-662-43376-8_10.
Philip Wadler. Propositions as sessions. In Proc. of ICFP, pages 273–286, 2012. doi:10.1145/
2398856.2364568.
Philip Wadler. Propositions as sessions. J. Funct. Program., 24(2-3):384–418, 2014. doi:10.
1017/S095679681400001X.
Philip Wadler. Propositions as types. Commun. ACM, 58(12):75–84, 2015. doi:10.1145/
2699407.

This work is licensed under the Creative Commons Attribution License. To view a copy of this
license, visit https://creativecommons.org/licenses/by/4.0/ or send a letter to Creative
Commons, 171 Second St, Suite 300, San Francisco, CA 94105, USA, or Eisenacher Strasse 2,
10777 Berlin, Germany
