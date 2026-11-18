Source: see manifest row of the PDF
PDF sha256: 898680fdbd51cf78f714f9a3a6ec63aa5860fedc2e0d73c652a77093d1480ab2
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of balzer_2019_manifest_deadlock_freedom_shared_session_types.pdf

Transcription of `balzer_2019_manifest_deadlock_freedom_shared_session_types.pdf` in this directory, 29 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-29 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Manifest Deadlock-Freedom for Shared
Session Types
Stephanie Balzer1(B) , Bernardo Toninho2(B) , and Frank Pfenning1
1

Carnegie Mellon University, Pittsburgh, USA
balzers@cs.cmu.edu
2
NOVA LINCS, Universidade Nova de Lisboa, Lisbon, Portugal
btoninho@fct.unl.pt

Abstract. Shared session types generalize the Curry-Howard correspondence between intuitionistic linear logic and the session-typed π-calculus
with adjoint modalities that mediate between linear and shared session
types, giving rise to a programming model where shared channels must
be used according to a locking discipline of acquire-release. While this
generalization greatly increases the range of programs that can be written, the gain in expressiveness comes at the cost of deadlock-freedom, a
property which holds for many linear session type systems. In this paper,
we develop a type system for logically-shared sessions in which types capture not only the interactive behavior of processes but also constrain the
order of resources (i.e., shared processes) they may acquire. This typelevel information is then used to rule out cyclic dependencies among
acquires and synchronization points, resulting in a system that ensures
deadlock-free communication for well-typed processes in the presence of
shared sessions, higher-order channel passing, and recursive processes.
We illustrate our approach on a series of examples, showing that it rules
out deadlocks in circular networks of both shared and linear recursive
processes, while still being permissive enough to type concurrent implementations of shared imperative data structures as processes.
Keywords: Linear and shared session types · Deadlock-freedom

1

Introduction

Session types [25–27] naturally describe the interaction protocols that arise
amongst concurrent processes that communicate via message-passing. This typing discipline has been integrated (with varying static safety guarantees) into
several mainstream language such as Java [28,29], F# [43], Scala [49,50],
Go [11] and Rust [33]. Session types moreover enjoy a logical correspondence between linear logic and the session-typed π-calculus [8,9,51,55]. Languages building on this correspondence [24,52,55] not only guarantee session
Supported by NSF Grant No. CCF-1718267: “Enriching Session Types for Practical
Concurrent Programming” and NOVA LINCS (Ref. UID/CEC/04516/2019).
c
⃝ The Author(s) 2019
L. Caires (Ed.): ESOP 2019, LNCS 11423, pp. 611–639, 2019.
https://doi.org/10.1007/978-3-030-17184-1_22

## PDF page 2

612

S. Balzer et al.

ﬁdelity (i.e., type preservation) but also deadlock-freedom (i.e., global progress).
The latter is guaranteed even in the presence of interleaved sessions, which
are often excluded from the deadlock-free fragments of traditional session-typed
frameworks [20,26,27,53]. These logical session types, however, exclude programming scenarios that demand sharing of mutable resources (e.g., shared databases
or shared output devices) instead of functional resource replication.
To increase their practicality, logical session types have been extended with
manifest sharing [2]. In the resulting language, linear and shared sessions coexist, but the type system enforces that clients of shared sessions run in mutual
exclusion of each other. This separation is achieved by enforcing an acquirerelease policy, where a client of a shared session must ﬁrst acquire the session
before it can participate in it along a private linear channel. Conversely, when a
client releases a session, it gives up its linear channel and only retains a shared
reference to the session. Thus, sessions in the presence of manifest sharing can
change, or shift, between shared and linear execution modes. At the type-level,
the acquire-release policy manifests in a stratiﬁcation of session types into linear
and shared with adjoint modalities [5,47,48], connecting the two strata. Operationally, the modality shifting up from the linear to the shared layer translates
into an acquire and the one shifting down from shared to linear into a release.
Manifest sharing greatly increases the range of programs that can be written
because it recovers the expressiveness of the untyped asynchronous π-calculus [3]
while maintaining session ﬁdelity. As in the π-calculus, however, the gain in
expressiveness comes at the cost of deadlock-freedom. An illustrative example is
an implementation of the classical dining philosophers problem, shown in Fig. 1,
using the language SILLS [2] that supports manifest sharing (in this setting we
often equate a process with the session it oﬀers along a distinguished channel).
The code shows the process fork proc, implementing a session of type sfork, and
the processes thinking and eating, implementing sessions of type philosopher. We
defer the details of the typing and the deﬁnition of the session types sfork and
philosopher to Sect. 2 and focus on the programmatic working of the processes for
now. For ease of reading, we typeset shared session types and variables denoting
shared channel references in red.
A fork proc process represents a fork that can be perpetually acquired and
released. The actions accept and detach are the duals of acquire and release,
respectively, allowing a process to accept an acquire by a client and to initiate a release by a client, respectively. Process thinking has two shared channel
references as arguments, for the forks to the left and right of the philosopher,
which the process tries to acquire. If the acquire succeeds, the process recurs
as an eating philosopher with two (now) linear channel references of type lfork.
Once a philosopher is done eating, it releases both forks and recurs as a thinking
philosopher. Let’s set a table for three philosopher that share three forks, all
spawned as processes executing in parallel:
f0 ← fork proc ; f1 ← fork proc ; f2 ← fork proc ;
p0 ← thinking ← f0 , f1 ; p1 ← thinking ← f1 , f2 ; p2 ← thinking ← f2 , f0 ;

## PDF page 3

Manifest Deadlock-Freedom for Shared Session Types
fork proc : {sfork}
c
fork proc =
accept c ;
c′
c
detach c′ ;
c
fork proc

thinking : {phil
sfork, sfork}
c
thinking
left, right =
acquire left ;
left ′
acquire right ;
right ′
c
eating
left ′ , right ′ ;

613

eating : {phil
lfork, lfork}
c
eating
left ′ , right ′ =
right
release right ′ ;
left
release left ′ ;
c
thinking
left, right

Fig. 1. Dining philosophers in SILLS [2].

Infamously, this conﬁguration may deadlock because of the circular dependency
between the acquires. We can break this cycle by changing the last line to p2 ←
thinking ← f0 , f2 , ensuring that forks are acquired in increasing order.
Perhaps surprisingly, cyclic dependencies between acquire requests are not
the only source of deadlocks. Fig. 2 gives an example, deﬁning the processes
owner and contester , which both have a shared channel reference to a common
resource that can be perpetually acquired and released. Both processes acquire
the shared resource, but additionally exchange the message ping. More precisely, process owner spawns the process contester , acquires the shared resource,
and only releases the resource after having received the message ping from the
contester . Process contester , on the other hand, ﬁrst attempts to acquire the
resource and then sends the message ping to the owner. The program deadlocks
if process owner acquires the resource ﬁrst. In that case, process owner waits
for process contester to send the message ping while process contester waits to
acquire the resource held by process owner . We note that this deadlock arises
in both synchronous and asynchronous semantics.
owner : {1
sres}
o
owner
sr =
c
contester
sr ;
lr
acquire sr ;
case c of
| ping
wait c ;
sr
release lr ; close o

contester : {⊕{ping : 1}
c
contester
sr =
lr
acquire sr ;
c.ping ;
sr
release lr ;
close c

sres}

Fig. 2. Circular dependencies among acquire and synchronization actions.

In this paper, we develop a type system for manifest sharing that rules out
cycles between acquire requests and interdependencies between acquire requests
and synchronization actions, detecting the two kinds of deadlocks explained
above. In our type system, session types not only prescribe when resources must
be acquired and released, but also the range of resources that may be acquired. To
this end, we equip the type system with the notion of a world, an abstract value
at which a process resides, and type processes relative to an acyclic ordering on
worlds, akin to the partial-order based approaches of [34,37]. The contributions
of this paper are:

## PDF page 4

614

S. Balzer et al.

– a characterization of the possible forms of deadlocks that can arise in shared
session types;
– the introduction of manifest deadlock-freedom, where resource dependencies
are manifest in the type structure via world modalities;
– its elaboration in the programming language SILLS+ , resulting in a type
system, a synchronous operational semantics, and proofs of session ﬁdelity
(preservation) and a strong form of progress that excludes all deadlocks;
– the novel abstraction of green and red arrows to reason about the interdependencies between processes;
– an illustration of the concepts on various examples, including an extensive
comparison with related work.
This paper is structured as follows: Sect. 2 provides a short introduction
to manifest sharing. Sect. 3 develops the type system and dynamics of the language SILLS+ . Sect. 4 illustrates the introduced concepts on an extended example.
Sect. 5 discusses the meta-theoretical properties of SILLS+ , emphasizing progress.
Sect. 6 compares with examples of related work and identiﬁes future work. Sect. 7
discusses related work, and Sect. 8 concludes this paper.

2

Manifest Sharing

In the previous section, we have already explored the programmatic workings of
manifest sharing [2], which enforces an acquire-release policy on shared channel
references. In this section, we clarify the typing of shared processes.
A key contribution of manifest sharing is not only to support acquire-release
as a programming primitive but also to make it manifest in the type system.
Generalizing the idea of type stratiﬁcation [5,47,48], session types are partitioned
into a linear and shared layer with two adjoint modalities connecting the layers:
AS
≜ ↑SL AL
AL , BL ≜ AL ⊗ BL | ⊕{l : AL } | {l : AL } | AL ⊸ BL | ∃x :AS .BL | Πx :AS .BL | 1 | ↓SL AS

In the linear layer, we get the standard connectives of intuitionistic linear logic
(AL ⊗ BL , AL ⊸ BL , ⊕{l : AL }, {l : AL }, and 1). These connectives are extended
with the modal operator ↓SL AS , shifting down from the shared to the linear layer.
Similarly, in the shared layer, we have the operator ↑SL AL , shifting up from the
linear to the shared layer. The former translates into a release (and, dually,
detach), the latter into an acquire (and, dually, accept). As a result, we obtain
a system in which session types prescribe all forms of communication, including
the acquisition and release of shared processes.
Table 1 provides an overview of SILLS ’s session types and their operational
reading. Since SILLS is based on an intuitionistic interpretation of linear logic
session types [8], types are expressed from the point of view of the providing process with the channel along which the process provides the session behavior being
characterized by its session type. This choice avoids the explicit duality operation present in original presentations of session types [25,26] and in those based

## PDF page 5

Manifest Deadlock-Freedom for Shared Session Types

615

Table 1. Session types in SILLS and their operational meaning.

on classical linear logic [55]. Table 1 lists the points of view of the provider and
client of a given connective in the ﬁrst and second lines, respectively. Moreover,
Table 1 gives for each connective its session type before and after the message
exchange, along with their respective process terms. We can see that the process
terms of a provider and a client for a given connective come in matching pairs,
indicating that the participants’ views of the session change consistently. We
use the subscripts L and S to distinguish between linear and shared channels,
respectively.
We are now able to give the session types of the processes fork proc, thinking,
and eating deﬁned in the previous section:
lfork = ↓SL sfork
sfork = ↑SL lfork
phil = 1
The mutually recursive session types lfork and sfork represent a fork that can perpetually be acquired and released. We adopt an equi-recursive [14] interpretation
for recursive session types, silently equating a recursive type with its unfolding
and requiring types to be contractive [19].
We brieﬂy discuss the typing and the dynamics of acquire-release. The typing
and the dynamics of the residual linear connectives are standard, and we detail
them in the context of SILLS+ (see Sect. 3). As is usual for an intuitionistic

## PDF page 6

616

S. Balzer et al.

interpretation, each connective gives rise to a left and a right rule, denoting the
use and provision, respectively, of a session of the given type:
(T-↑SL R )

(T-↑SL L )

Γ ; · ⊢ PxL :: (xL : AL )

Γ, xS : ↑SL AL ; Δ, xL : AL ⊢ QxL :: (zL : CL )

Γ ⊢ xL ← accept xS ; PxL :: (xS : ↑ AL )
S
L

(T-↓

S
LR

)
Γ ⊢ PxS :: (xS : AS )

Γ ; · ⊢ xS ← detach xL ; PxS :: (xL : ↓SL AS )

Γ, xS : ↑SL AL ; Δ ⊢ xL ← acquire xS ; QxL :: (zL : CL )

(T-↓SL L )

Γ, xS : AS ; Δ ⊢ QxS :: (zL : CL )

Γ ; Δ, xL : ↓SL AS ⊢ xS ← release xL ; QxS :: (zL : CL )

The typing judgments Γ ⊢ P :: (xS : AS ) and Γ ; Δ ⊢ P :: (xL : AL ) indicate that
process P provides a session of type A along channel x, given the typing of the
channels speciﬁed in typing contexts Γ (and Δ). Γ and Δ consist of hypotheses
on the typing of shared and linear channels, respectively, where Γ is a structural
and Δ a linear context. To allow for recursive process deﬁnitions, the typing
judgment depends on a signature Σ that is populated with all process deﬁnitions prior to type-checking. The adjoint formulation precludes shared processes
from depending on linear channel references [2,47], a restriction motivated from
logic referred to as the independence principle [47]. Thus, when a shared session
accepts an acquire and shifts to linear, it starts with an empty linear context.
Operationally, the dynamics of SILLS is captured by multiset rewriting
rules [12], which denote computation in terms of state transitions between conﬁgurations of processes. Multiset rewriting rules are local in that they only mention the parts of a conﬁguration they rewrite. For acquire-release we have the
following:
(D-↑SL )
proc(aS , xL ← accept aS ; PxL ), proc(cL , xL ← acquire aS ; QxL )
−→ proc(aL , [aL /xL ] PxL ), proc(cL , [aL /xL ] QxL ), unavail(aS )
(D-↓SL )
proc(aL , xS ← detach aL ; PxS ), proc(cL , xS ← release aL ; QxS ), unavail(aS )
−→ proc(aS , [aS /xS ] PxS ), proc(cL , [aS /xS ] QxS )

Conﬁguration states are deﬁned by the predicates proc(cm , P ) and unavail(aS ).
The former denotes a running process with process term P providing along
channel cm , the latter acts as a placeholder for a shared process providing along
channel aS that is currently not available. The above rule exploits the invariant
that a process’ providing channel a can appear at one of two modes, a linear
one, aL , and a shared one, aS . While the process (i.e. the session) is linear, it
provides along aL , while it is shared, along aS . When a process shifts between
modes, it switches between the two modes of its oﬀering channel. The channel at
the appropriate mode is substituted for the variables occurring in process terms.

3

Manifest Deadlock-Freedom

In this section, we introduce our language SILLS+ , a session-typed language
that supports sharing without deadlock. We focus on SILLS+ ’s type system and
dynamics in this section and discuss its meta-theoretical properties in Sect. 5.

## PDF page 7

Manifest Deadlock-Freedom for Shared Session Types

3.1

617

Competition and Collaboration

The introduction of acquire-release, to ensure that the multiple clients of a shared
process interact with the process in mutual exclusion from each other, gives rise
to an obvious source of deadlocks, as acquire-release eﬀectively amounts to a
locking discipline. The typical approach to prevent deadlocks in that case is to
impose a partial order on the resources and to “lock-up”, i.e., to lock the resources
in ascending order. We adopted this strategy in Sect. 1 (Fig. 1) to break the cyclic
dependencies among the acquires in the dining philosophers.
In Sect. 1, however, we also considered another example (Fig. 2) and discovered that cyclic acquisitions are not the only source of deadlocks, but deadlocks
can also arise from interdependent acquisitions and synchronizations. In that
example, we can prevent the deadlock by moving the acquire past the synchronization, in either of the two processes. Whereas in a purely linear session-typed
system the sequencing of actions within a process do not aﬀect other processes,
the relative placement of acquire requests and synchronizations become relevant
in a shared session-typed system.
Based on this observation, we can divide the processes in a shared-session
discipline into competitors and collaborators. The former compete for a set of
resources, whereas the latter do not overlap in the set of resources they acquire.
For example, in the dining philosophers (Fig. 1), the philosophers p0 , p1 , and p2
compete with each other for the set of forks f0 , f1 , and f2 , whereas the process
that spawns the philosophers and the forks collaborates with either of them.
Transferring this idea to the process graph that emerges at run-time, we note
that competitors are siblings whereas collaborators stand in a parent-descendant
relationship. We illustrate this outcome on Fig. 3 that shows a possible runtime process graph for the dining philosophers. Linear processes are depicted as
solid black circles with a white identiﬁer and shared processes are depicted as
dotted ﬁlled violet circles with a black identiﬁer. Linear channels are depicted as
black lines, shared channel references as dotted violet lines with the arrow head
pointing to the shared process being acquired1 . The identiﬁers P0 , P1 , and P2
stand for the three philosophers, F0 , F1 , and F2 for the three forks, and T for
the process that sets the table. The current run-time graph depicts the scenario
in which P1 is eating, while the other two philosophers are still thinking.
Embedded in the graph is a tree that arises from the linear processes and the
linear channels connecting them. For any two nodes in this tree, the parent node
denotes the client process and the child node the providing process. We note
that the independence principle (see Sect. 2), which precludes shared processes
from depending on linear channel references, guarantees that there exists exactly
one tree in the process graph, with the linear main process as its root. The shape
of the tree changes when new processes are spawned, linear channels exchanged
(through ⊗ and ⊸), or shared processes acquired. For example, process P2 could
acquire the shared fork F0 , which then becomes a linear child process of P2 ,
should the acquire succeed. As indicated by the shared channel references, the
1

We have made sure to make the diﬀerent concepts distinguishable in greyscale mode.

## PDF page 8

618

S. Balzer et al.
Legend:

T

linear process (child: provider, parent: client)
shared process

P0

P1

linear channel

P2

shared channel reference

F1

F2
F0

Fig. 3. Run-time process graph for dining philosophers (see Fig. 1).

sibling nodes P0 , P1 , and P2 compete with each other for the nodes F0 , F1 , and
F2 , whereas the node T does not compete for any of the resources acquired by
its descendants (including F1 and F2 ). Our type system enforces this paradigm,
as we discuss in the next section.
3.2

Type System

Invariants. Having identiﬁed the notions of collaborators and competitors, our
type system must guarantee: (i) that collaborators acquire mutually disjoint sets
of resources; (ii) that competitors employ a locking-up strategy for the resources
they share; and, (iii) that competitors have released all acquired resources when
synchronizing with other competitors. Invariant (ii) rules out cyclic acquisitions
and invariants (i) and (iii) combined rule out interdependent acquisitions and
synchronizations.
To express the high-level invariants above in our type system, we introduce
the notion of a world – an abstract value that is equipped with a partial order –
and associate such a world with every process. Programmers can create worlds,
indicate the world at which a process resides at spawn time, and deﬁne an order
on worlds. Moreover, we associate with each process a range of worlds that
indicates the worlds of resources that the process may acquire. As a result, we
obtain the following typing judgments:
n
Ψ ; Γ ⊢ P :: (xS : AS [ωk ↕ω
ωl ])

(where Ψ + irreﬂexive)

n
Ψ ; Γ ; Φ; Δ ⊢ P :: (xL : AL [ωk ↕ω
ωl ])

(where Ψ + irreﬂexive)

The typing judgments reveal that we impose worlds at the judgmental level,
resulting in a hybrid system, in which the adjoint modalities for acquire-release
are complemented with world modalities that occur as syntactic objects in propon
sitions [7]. We use the notation xm : Am [ωk ↕ω
ωl ] (where m stands for S or L)
to associate worlds ωk , ωl , and ωn with a process that oﬀers a session of type
Am along channel x. World ωk denotes the world at which the process resides.

## PDF page 9

Manifest Deadlock-Freedom for Shared Session Types

619

We refer to this world as the self world. Worlds ωl and ωn indicate the range of
worlds of resources that the process may acquire, with ωl denoting the minimal
(min) world in this range and ωn the maximal (max) one.
Process terms are typed relative to the order speciﬁed in Ψ and the contexts
Γ , Φ, and Δ. As in Sect. 2, Γ is a structural context consisting of hypotheses
on the typing of variables bound to shared channel references, augmented with
world annotations. We ﬁnd it necessary to split the linear context “Δ” from
Sect. 2 into the two disjoint contexts Φ and Δ, allowing us to separate channels
that are possibly aliased (due to sharing) from those that are not, respectively.
Both Φ and Δ consist of hypotheses on the typing of variables that are bound
to linear channels, augmented with world annotations. Ψ is presupposed to be
acyclic and deﬁned as: Ψ ≜ · | Ψ ′ , ωk < ωl | Ψ ′ , ωo , where ω stands for a
concrete world w or a world variable δ. We allow Ψ to contain single worlds,
to support singletons as well as to accommodate world creation prior to order
declaration. We deﬁne the transitive closure Ψ + , yielding a strict partial order,
and the reﬂexive transitive closure Ψ ∗ , yielding a partial order.
The high-level invariants (i), (ii), and (iii) identiﬁed earlier naturally transcribe into the following invariants, which we impose on the typing judgments
above. We use the notation ⟨xm ⟩; P to denote a process term that currently
executes an action along channel xm .
1. min(parent) ≤ self(acquired child) ≤ max(parent):
∗
r
∀yL : BL [ωo ↕ω
ωp ] ∈ Φ : Ψ ⊢ ω l ≤ ω o ≤ ω n
2. max(parent) < min(child):
+
r
⊢ ω n < ωp
∀yL : BL [ωo ↕ω
ωp ] ∈ Δ ∪ Φ : Ψ
ωv
n
3. If Ψ ; Γ, xS : A[ωt ↕ωu ]; Φ; Δ ⊢ xL ← acquire xS ; QxS :: (zL : CL [ωk ↕ω
ωl ]), then
+
r
]
∈
Φ
:
Ψ
⊢
ω
<
ω
.
∀yL : BL [ωo ↕ω
o
t
ωp
n
4. If Ψ ; Γ ; Φ; Δ ⊢ ⟨xm ⟩; P :: (xL : AL [ωk ↕ω
ωl ]), then Φ = (·).
Invariants 1 and 2 ensure that, for any node in the tree, the acquired resources
reside at smaller worlds than those acquired by any descendant. As a result, the
two invariants guarantee high-level invariant (i). Invariant 3, on the other hand,
imposes a lock-up strategy on acquires and thus guarantees high-level invariant
(ii). To guarantee high-level invariant (iii), we impose Invariant 4, which forces a
process to release any acquired resources before communicating along its oﬀering
channel. Since sibling nodes cannot be directly connected by a linear channel,
the only way for them to synchronize is through a common parent. Finally, to
guarantee that world annotations are internally consistent, we require for each
n
annotation [ωk ↕ω
ωl ] that ωk < ωl ≤ ωn .
Rules. We now present select process typing rules, a complete listing is provided
in the companion technical report [4]. The only new rules with respect to the
language SILLS [2] are those pertaining to world creation and order determination. These are extra-logical judgmental rules. We allow both linear and shared
processes to create and relate worlds. Rules (T-NewL ) and (T-NewS ) create a
new world w and make it available to the continuation Qw . Rules (T-OrdL ) and
(T-OrdS ) relate two existing worlds, while preserving acyclicity of the order.

## PDF page 10

620

S. Balzer et al.
v
Ψ, w; Γ ; Φ; Δ ⊢ Qw :: (xL : AL [ωm ↕ω
ωu ])

(T-NewL )

v
Ψ ; Γ ; Φ; Δ ⊢ w ← new world; Qw :: (xL : AL [ωm ↕ω
ωu ])
v
Ψ, w; Γ ⊢ Qw :: (xS : AS [ωm ↕ω
ωu ])

v
Ψ ; Γ ⊢ w ← new world; Qw :: (xS : AS [ωm ↕ω
ωu ])

ωp , ω r ∈ Ψ
(Ψ, ωp < ωr )+ irreﬂexive
v
Ψ, ωp < ωr ; Γ ; Φ; Δ ⊢ Q :: (xL : AL [ωm ↕ω
ωu ])
v
Ψ ; Γ ; Φ; Δ ⊢ ωp < ωr ; Q :: (xL : AL [ωm ↕ω
ωu ])

ωp , ω r ∈ Ψ
(Ψ, ωp < ωr )+ irreﬂexive
v
Ψ, ωp < ωr ; Γ ⊢ Q :: (xS : AS [ωm ↕ω
ωu ])
v
Ψ ; Γ ⊢ ωp < ωr ; Q :: (xS : AS [ωm ↕ω
ωu ])

(T-NewS )

(T-OrdL )

(T-OrdS )

We now consider the typing rule for acquire, which must explicitly enforce the
various low-level invariants above. Since an acquire results in the addition of a
new child node to the executing process, the rule can interfere with Invariants 1
and 2. The ﬁrst two premises of the rule ensure that the two invariants are
preserved. Moreover, the rule has to ensure that the acquiring process is lockingup (Invariant 3), which is achieved by the third premise.
r
Ψ ∗ ⊢ ωk ≤ ωm ≤ ωn
Ψ + ⊢ ωn < ω u
∀yL : BL [ωl ↕ω
ωp ] ∈ Φ : ωl < ωm
S
ωv
ωv
n
Ψ ; Γ, xS : ↑L AL [ωm ↕ωu ]; Φ, xL : AL [ωm ↕ωu ]; Δ ⊢ QxL :: (zL : CL [ωj ↕ω
ωk ])

ωn
v
Ψ ; Γ, xS : ↑SL AL [ωm ↕ω
ωu ]; Φ; Δ ⊢ xL ← acquire xS ; QxL :: (zL : CL [ωj ↕ωk ])

(T-↑SL L )

The remaining shift rules are actually unchanged with respect to SILLS , modulo the world annotations. In particular, low-level Invariant 4 is already satisﬁed
because the conclusion of rule (T-↑SL R ) does not have a context Φ and because
the independence principle forces Φ to be empty in rule (T-↓SL R ).
v
Ψ ; Γ ; · ; · ⊢ PxL :: (xL : AL [ωm ↕ω
ωu ])
v
Ψ ; Γ ⊢ xL ← accept xS ; PxL :: (xS : ↑SL AL [ωm ↕ω
ωu ])

(T-↑SL R )

ωn
v
Ψ ; Γ, xS : AS [ωm ↕ω
ωu ]; Φ; Δ ⊢ QxS :: (zL : CL [ωj ↕ωk ])
ωn
v
Ψ ; Γ ; Φ, xL : ↓SL AS [ωm ↕ω
ωu ]; Δ ⊢ xS ← release xL ; QxS :: (zL : CL [ωj ↕ωk ])
v
Ψ ; Γ ⊢ PxS :: (xS : AS [ωm ↕ω
ωu ])
v
Ψ ; Γ ; · ; · ⊢ xS ← detach xL ; PxS :: (xL : ↓SL AS [ωm ↕ω
ωu ])

(T-↓SL L )

(T-↓SL R )

We now consider the linear connectives, starting with 1. Rule (T-1L ) reveals
that only processes that have never been acquired may be terminated. This
restriction is important to guarantee progress because existing clients of a shared
process may wait indeﬁnitely otherwise. We impose the restriction as a wellformedness condition on a session type, giving rise to a strictly equi-synchronizing
session type. The notion of an equi-synchronizing session type [2] has been
deﬁned for SILLS and guarantees that a process that has been acquired at a
type AS is released back to the type AS , should it ever be released. A strictly
equi-synchronizing session type additionally requires that an acquired resource
must be released. The corresponding rules can be found in [4]. Linearity enforces
Invariant 4 in rule (T-1R ), making sure that no linear channels are left behind.

## PDF page 11

Manifest Deadlock-Freedom for Shared Session Types
n
Ψ ; Γ ; Φ; Δ ⊢ Q :: (zL : CL [ωj ↕ω
ωk ])

ωn
v
Ψ ; Γ ; Φ; Δ, xL : 1[ωm ↕ω
ωu ] ⊢ wait xL ; Q :: (zL : CL [ωj ↕ωk ])
v
Ψ ; Γ ; · ; · ⊢ close xL :: (xL : 1[ωm ↕ω
ωu ])

621

(T-1L )

(T-1R )

Next, we consider internal and external choice. Since internal and external
choice cannot alter the linear process tree of a process graph, the rules are very
similar to the ones in SILLS . The only diﬀerences are that we get two left rules
for each connective and that the Φ-context of each right rule must be empty to
satisfy Invariant 4. The former is merely due to the tracking of possibly aliased
sessions in the Φ context. We only list rules for internal choice, those for external
choice are dual and can be found in [4].
ωn
v
(∀i) Ψ ; Γ ; Φ; Δ, xL : ALi [ωm ↕ω
ωu ] ⊢ Qi :: (zL : CL [ωj ↕ωk ])
ωn
v
Ψ ; Γ ; Φ; Δ, xL : ⊕{l : AL }[ωm ↕ω
ωu ] ⊢ case xL of l ⇒ Q :: (zL : CL [ωj ↕ωk ])
ωn
v
(∀i) Ψ ; Γ ; Φ, xL : ALi [ωm ↕ω
ωu ]; Δ ⊢ Qi :: (zL : CL [ωj ↕ωk ])
ωn
v
Ψ ; Γ ; Φ, xL : ⊕{l : AL }[ωm ↕ω
ωu ]; Δ ⊢ case xL of l ⇒ Q :: (zL : CL [ωj ↕ωk ])
v
Ψ ; Γ ; · ; Δ ⊢ P :: (xL : AL h [ωm ↕ω
ωu ])
v
Ψ ; Γ ; · ; Δ ⊢ xL .lh ; P :: (xL : ⊕{l : AL }[ωm ↕ω
ωu ])

(T-⊕L1 )
(T-⊕L2 )

(T-⊕R )

More interesting are linear channel output and input, since these alter the
linear process tree of a process graph. Moreover, additional world annotations
are needed to indicate the worlds of the channel that is exchanged. For the
r
latter we use the notation @ωl ↕ω
ωp , indicating that the exchanged channel has
the worlds ωl , ωp , and ωr for self, min, and max, respectively. To account for
induced changes in the process graph, the rules that type an input of a linear
channel must guard against any disturbance of Invariants 1 and 2. Because the
two invariants guarantee that parents do not overlap with their descendants in
terms of acquired resources, they prevent any exchange of acquired channels.
We thus restrict ⊗ and ⊸ to the exchange of channels that have not yet been
acquired. This is not a limitation since, as we will see below, shared channel
output and input are unrestricted.
Even with the above restriction in place, we still have to make sure that a
received channel satisﬁes Invariant 2. If we were to state a corresponding premise
on the receiving rules, invertibility of the rules would be disturbed. To uphold
invertibility, we impose a well-formedness condition on session types that ensures
ωv
r
for a session of type AL @ωl ↕ω
ωp ⊗BL [ωm ↕ωu ] that ωv < ωp and, analogously, for
ωr
v
a session of type AL @ωl ↕ωp ⊸ BL [ωm ↕ω
ωu ] that ωv < ωp . Session types are
checked to be well-formed upon process deﬁnition. Given type well-formedness,
we obtain the following rules for ⊸, noting that the right rule enforces Invariant 4
by requiring an empty Φ-context. The rules for ⊗ are dual.

## PDF page 12

622

S. Balzer et al.

ωn
v
Ψ ; Γ ; Φ; Δ, xL : BL [ωm ↕ω
ω ] ⊢ Q :: (zL : CL [ωj ↕ω ])
u

k

ωv
ωr
ωn
r
Ψ ; Γ ; Φ; Δ, xL : AL @ωl ↕ω
ωp ⊸ BL [ωm ↕ωu ], yL : AL [ωl ↕ωp ] ⊢ send xL yL ; Q :: (zL : CL [ωj ↕ω ])

(T-⊸L1 )

k

ωn
v
Ψ ; Γ ; Φ, xL : BL [ωm ↕ω
ω ]; Δ ⊢ Q :: (zL : CL [ωj ↕ω ])
u

k

ωv
ωr
ωn
r
Ψ ; Γ ; Φ, xL : AL @ωl ↕ω
ωp ⊸ BL [ωm ↕ωu ]; Δ, yL : AL [ωl ↕ωp ] ⊢ send xL yL ; Q :: (zL : CL [ωj ↕ω ])

(T-⊸L2 )

k

ωv
r
Ψ ; Γ ; · ; Δ, yL : AL [ωl ↕ω
ωp ] ⊢ PyL :: (xL : BL [ωm ↕ωu ])
ωv
r
Ψ ; Γ ; · ; Δ ⊢ yL ← recv xL ; PyL :: (xL : AL @ωl ↕ω
ωp ⊸ BL [ωm ↕ωu ])

(T-⊸R )

Since there are no invariants imposed on the shared context Γ , the rules
for shared channel output and input are identical to those in SILLS . The only
diﬀerences are that we have two left rules and that the Φ-context of the right rule
must be empty to satisfy Invariant 4. The former is merely due to the tracking
of possibly aliased sessions in the Φ context.
ωv
ωn
r
Ψ ; Γ, yS : AS [ωl ↕ω
ωp ]; Φ; Δ, xL : BL [ωm ↕ωu ] ⊢ QyS :: (zL : CL [ωj ↕ωk ])
ωv
ωn
r
Ψ ; Γ ; Φ; Δ, xL : ∃x:AS @ωl ↕ω
ωp . BL [ωm ↕ωu ] ⊢ yS ← recv xL ; QyS :: (zL : CL [ωj ↕ωk ])
ωv
ωn
r
Ψ ; Γ, yS : AS [ωl ↕ω
ωp ]; Φ, xL : BL [ωm ↕ωu ]; Δ ⊢ QyS :: (zL : CL [ωj ↕ωk ])
ωv
ωn
r
Ψ ; Γ ; Φ, xL : ∃x:AS @ωl ↕ω
ωp . BL [ωm ↕ωu ]; Δ ⊢ yS ← recv xL ; QyS :: (zL : CL [ωj ↕ωk ])
ωv
r
Ψ ; Γ, yS : AS [ωl ↕ω
ωp ]; · ; Δ ⊢ P :: (xL : BL [ωm ↕ωu ])
ωr
ωv
r
Ψ ; Γ, yS : AS [ωl ↕ω
ωp ]; · ; Δ ⊢ send xL yS ; P :: (xL : ∃x:AS @ωl ↕ωp . BL [ωm ↕ωu ])

(T-∃L1 )
(T-∃L2 )

(T-∃R )

We ﬁnally consider the rules for forwarding and spawning. We allow a shared
forward between processes that oﬀer the same session at the same worlds.
Because forwards have to be world-invariant, however, no well-typed program
could ever have a linear forward. The process being forwarded to must be in
either of the contexts Φ or Δ, and thus satisﬁes Invariant 2, making it impossible
for the world annotations of the forwarder and forwardee to match. We omit
linear forwarding and discuss possible future extensions in Sect. 6.
ωn
n
Ψ ; Γ, yS : AS [ωj ↕ω
ωk ] ⊢ fwd xS yS :: (xS : AS [ωj ↕ωk ])

(T-IdS )

The rules for spawning depend on the possible modes of the spawning
and spawned processes: (T-SpawnLL ) speciﬁes how a linear process can spawn
another linear process; (T-SpawnSS ) speciﬁes how a shared processes can spawn
another shared process. The rules are checked relative to a process deﬁnition
found in the signature Σ and to a world substitution mapping γ : |Ψ | → |Ψ ′ |,
such that for each δ ∈ Ψ ′ we have Ψ ⊢ γ(δ), where |Ψ | denotes the ﬁeld of
Ψ (i.e., the union of its domain and range). As usual, we lift substitution to
types γ̂(Am ), contexts γ̂(Γ ), and orders γ̂(Ψ ). Both rules ensure that, given the
mapping γ, the order Ψ of the spawning process entails the one of the process
deﬁnition (Ψ ⊢ γ̂(Ψ ′ )). The linear spawn rule (T-SpawnLL ) further enforces
Invariant 2 for the spawned child. We note that the spawned child enters the
linear context Δ in the spawning process’ continuation since no aliases to such
a process can exist at this point.

## PDF page 13

Manifest Deadlock-Freedom for Shared Session Types

ω

Δ1 = yL : BL [ωm ↕ωv
u]

ω̃

Φ1 = ỹL : B̃L [ω̃m ↕ω̃v ]
u

623

ω

Γ1 = zS : CS [ωl ↕ωr
p]

δ
(Ψ ′ ⊢ x′L : A′L [δj ↕δn ] ← XL ← Δ′ , Φ′ , Γ ′ = Px′ ,dom(Δ′ ),dom(Φ′ ),dom(Γ ′ ),Ψ ′′ ) ∈ Σ
k
L
δn
′
n
γ̂(Δ′ ) = Δ1
γ̂(Φ′ ) = Φ1
γ̂(Γ ′ ) = Γ1
Ψ ⊢ γ̂(Ψ ′ )
γ̂(AL [δj ↕δ ]) = AL [ωj ↕ω
ωk ]
k

Ψ + ⊢ ωt < ωk

ω
k
ω
ωn
Ψ ; Γ1 , Γ2 ; Φ1 , Φ2 ; Δ1 , Δ2 ⊢ xL : AL [ωj ↕ω ] ← XL ← yL , ỹL , zS ; QxL :: (zL′′ : DL [ωi ↕ωtq ])
k
′′
t
n
Ψ ; Γ1 , Γ2 ; Φ2 ; Δ2 , xL : AL [ωj ↕ω
ω ] ⊢ QxL :: (zL : DL [ωi ↕ωq ])

ω

(T-SpawnLL )

δ

(Ψ ′ ⊢ x′S : A′S [δj ↕δn ] ← XS ← Γ ′ = Px′ ,dom(Γ ′ ),Ψ ′′ ) ∈ Σ

Γ1 = zS : CS [ωl ↕ωr
p]

k

δ

n
γ̂(A′S [δj ↕δn ]) = AS [ωj ↕ω
ω ]
k

k

γ̂(Γ ′ ) = Γ1

S

Ψ ⊢ γ̂(Ψ ′ )
ω

′′
t
n
Ψ ; Γ1 , Γ2 , xS : AS [ωj ↕ω
ω ] ⊢ QxS :: (zS : DS [ωi ↕ωq ])
k

ω

′′
t
n
Ψ ; Γ1 , Γ2 ⊢ xS : AS [ωj ↕ω
ω ] ← XS ← zS ; QxS :: (zS : DS [ωi ↕ωq ])

(T-SpawnSS )

k

In the companion technical report [4], we provide a variant of rule
(T-SpawnLL ) for the case of a linear recursive tail call. Without linear forwarding, a linear tail call can no longer be implicitly “de-sugared” into a spawn and
a linear forward [2,22,52], but must be accounted for explicitly. In the report,
we also provide the rules for checking process deﬁnitions. Those rules make sure
that the process’ world order is acyclic, that the types of the providing session
and argument sessions are well-formed, and that the process satisﬁes Invariants 1
and 2.
3.3

Dining Philosophers in SILLS+

Having introduced our type system, we revisit the dining philosophers from
Sect. 1 and show how to program the example in SILLS+ , ensuring that the
program will run without deadlocks. The code is given in Fig. 4. We note the
world annotations in the signature of the process deﬁnitions. For instance,
thinking : {δ0 < δ1 , δ1 < δ2 , δ2 < δ3 ⊢ phil[δ0 ↕δδ21 ] ← sfork[δ1 ↕δδ33 ], sfork[δ2 ↕δδ33 ]; ·; ·}
indicates that, given the order δ0 < δ1 < δ2 < δ3 , process thinking provides
a session of type phil[δ0 ↕δδ21 ] and uses two shared channel references of type
sfork[δ1 ↕δδ33 ] and sfork[δ2 ↕δδ33 ]. The two · signify that neither acquired nor linear
channel references are given as arguments. The signature indicates that the two
shared fork references reside at diﬀerent worlds, such that the world of the ﬁrst
one is smaller than the one of the second.
Let’s brieﬂy convince ourselves that the two acquires in process thinking in
Fig. 4 are type-correct. For each acquire we have to show that: the world of the
resource to be acquired is within the acquiring process’ range; the max of the
acquiring process is smaller than the min of the acquired resource; and, that
the self of the acquired resource is larger than those of all already acquired
resources. We can convince ourselves that all those conditions are readily met.

## PDF page 14

624

S. Balzer et al.

Fig. 4. Deadlock-free version of dining philosophers in SILLS+ .

We note, however, that if we were to swap the two acquires, the program would
not type-check.
Let us once more set the table for three philosophers and three forks. We
execute this code in a process with world annotations [δa ↕δδbb ] such that δa < δb .
We ﬁrst create new worlds and deﬁne their order:
w1 ← new world; w2 ← new world; w3 ← new world; w4 ← new world;
δa < w1 ; δa < w2 ; δb < w1 ; w1 < w2 ; w1 < w3 ; w1 < w4 ; w2 < w3 ; w2 < w4 ; w3 < w4 ;

We then spawn the forks, each residing at a diﬀerent world, such that the max
world of a fork is higher than the self of the highest fork, ensuring Invariant 2
for the philosopher processes that we spawn afterwards:
w4
4
f1 : sfork[w1 ↕w
w4 ] ← fork proc ; f2 : sfork[w2 ↕w4 ] ← fork proc ;
w4
f3 : sfork[w3 ↕w4 ] ← fork proc ;

When we spawn the philosophers, we ensure that P0 is going to pick up fork F1
and then F2 , P1 is going to pick up F2 and then F3 , and P2 is going to pick up
F1 and then F3 .
p0 : phil[δa ↕ww21 ] ← thinking ← ·; ·; f1 , f2 ; p1 : phil[δa ↕ww32 ] ← thinking ← ·; ·; f2 , f3 ;
p2 : phil[δa ↕ww31 ] ← thinking ← ·; ·; f1 , f3 ;

We note that the deadlocking spawn
3
p2 : phil[δa ↕w
w1 ] ← thinking ← ·; ·; f3 , f1 ;

is type-incorrect since we would substitute both w1 and w3 for δ1 and w3 and w1
for δ2 , which violates the ordering constraints put in place by typing.

## PDF page 15

Manifest Deadlock-Freedom for Shared Session Types

3.4

625

Dynamics

We now give the dynamics of SILLS+ . Our current system is based on a synchronous dynamics. While this choice is more conservative, it allows us to narrow
the complexity of the problem at hand.
As in SILLS , we use multiset rewriting rules [12] to capture the dynamics of SILLS+ (see Sect. 2). Multiset rewriting rules represent computation
in terms of local state transitions between conﬁgurations of processes, only
mentioning the parts of a conﬁguration they rewrite. We use the predicates
wa
wa
proc(am , wa1 ↕wa32 , Pam ) and unavail(aS , wa1 ↕wa32 ) to deﬁne the states of a conﬁguration (see Sect. 5.1). The former denotes a process executing term P that
provides along channel am at mode m with worlds wa1 , wa2 , and wa3 for self,
min, and max, respectively. The latter acts as a placeholder for a shared process
providing along channel aS with worlds wa1 , wa2 , and wa3 for self, min, and max,
respectively, that is currently unavailable. We note that since worlds are also
run-time artifacts, they must occur as part of the state-deﬁning predicates.
Fig. 5 lists selected rules of the dynamics. Since the rules remain largely the
same as those of SILLS , apart from the world annotations that are “threaded
through” unchanged, we only discuss the rules that actually diﬀer from the
SILLS rules. The interested reader can ﬁnd the remaining rules in the companion
technical report [4].
(D-SpawnLL )
wb
wa
proc(aL , wa1 wa32 , xL : AL [wb1 wb32 ]
XL
cL , c̃L , dS ; QxL ),
!def(Ψ ′ ⊢ xL′ : A′L [δj δδnk ]
XL
Δ′ , Φ ′ , Γ ′ = PxL′ ,dom(Δ′ ),dom(Φ ′ ),dom(Γ ′ ),Ψ ′′ )
wb
proc(bL , wb1 wb32 , [bL /xL′ , cL /dom(Δ′ ), c̃L /dom(Φ ′ ), dS /dom(Γ ′ )]γ̂(PxL′ ,dom(Δ′ ),dom(Φ ′ ),dom(Γ ′ ),Ψ ′′ )),
wa
proc(aL , wa1 wa32 , [bL /xL ]QxL ),
wb
unavail(bS , wb1 wb32 ) (b fresh)
(D-New)
wa
proc(a, wa1 wa32 , w

new world; Qw )

(D-Ord)
wa
proc(a, wa1 wa32 , w < w′ ; Q)

wa

proc(a, wa1 wa32 , Qw )

(w fresh)

wa

proc(a, wa1 wa32 , Q)

Fig. 5. Selected multiset rewriting rules of SILLS+ .

Noteworthy are the rules D-New and D-Ord for creating and relating
worlds, respectively. Rule D-New creates a fresh world, which will be globally available in the conﬁguration. Rule D-Ord, on the other hand, updates the
conﬁguration’s order with the pair w < w′ . Rule D-SpawnLL , lastly, substitutes
actual worlds for world variables in the body of the spawned process, using the
substitution mapping γ deﬁned earlier. It relies on the existence of a corresponding deﬁnition predicate for each process deﬁnition contained in the signature Σ.
We note that the substitution γ in rule D-SpawnLL instantiates the appropriate
world variables in the spawned process P .

## PDF page 16

626

4

S. Balzer et al.

Extended Example: An Imperative Shared Queue

We now develop a typical imperative-style implementation of a queue that uses
a list data structure internally to store the queue’s elements and has shared
references to the front and the back of the list for concurrent dequeueing and
enqueueing, respectively. The session types for the queue and the list are2
queue AS = ↑SL {enq : Πx:AS . ↓SL queue AS ,
deq : ⊕{none : ↓SL queue AS , some : ∃x:AS . ↓SL queue AS }}
list AS = ↑SL {ins : Πx:AS . ∃y:list AS . ↓SL list AS ,
del : ⊕{none : ↓SL list AS , some : ∃x:AS . ↓SL list AS }
The list is implemented in terms of processes empty and elem, denoting the
empty list and a cons cell, respectively. We show the more interesting case of a
cons cell (Fig. 6). The queue is deﬁned by processes head (Fig. 7) and queue proc
(Fig. 8), the latter being the queue’s interface to its clients.

Fig. 6. Imperative queue – elem process.

We can now deﬁne a client (Fig. 8) for the queue, assuming existence of a
corresponding shared session type item and a process item proc oﬀering a session
of type item[δ3↕δδ44 ]. The client instantiates the queue at world δb , allowing it
to acquire resources at world w1 , which is exactly the world at which process
queue proc instantiates the list. Given that the client itself resides at world δa ,
which is smaller than the queue’s world δb , the client is allowed to acquire the
queue, which in turn will acquire the list to satisfy any requests by the client.
The example showcases a paradigmatic use of several collaborators, where
collaborators can hold resources while they “talk down” in the tree. In particular,
as illustrated in Fig. 9, the clients C1 , C2 , and C3 compete for resources at
world δb , i.e., the queue Q. On the other hand, a client Ci collaborates with the
queue Q, the list elements Li , and the items Ii , since they do not overlap in
2

We adopt polymorphism for the example without formal treatment since it is orthogonal and has been studied for session types in [23, 46].

## PDF page 17

Manifest Deadlock-Freedom for Shared Session Types

627

Fig. 7. Imperative queue – head process.

Fig. 8. Imperative queue – queue proc process and client process.

the set of resources they may acquire: a client acquires resources at δb , a queue
resources at w1 , a list resources at w2 , and an item resources at w4 , and we have
δa < δb < w1 < w2 < w3 < w4 . We note in particular that the setup prevents a
list element from acquiring its successor, forcing linear access through the queue.

5

Semantics

In this section, we discuss the meta-theoretical properties of SILLS+ , focusing on
deadlock-freedom. The companion technical report [4] provides further details.

## PDF page 18

628

S. Balzer et al.

Fig. 9. Run-time process graph for imperative queue (see Fig. 3 for legend).

5.1

Configuration Typing and Preservation

Given the hierarchy between mode S and L and the fact that shared processes
cannot depend on linear processes, we divide a conﬁguration into a shared part
Λ and a linear part Θ. We use the typing judgment Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ to
type conﬁgurations. The judgment expresses that a well-formed conﬁguration
Λ; Θ provides the shared channels in Γ and the linear channels in Φ and Δ.
A conﬁguration is type-checked relative to all shared channel references and a
global order Ψ . While type-checking is compositional insofar as each process
deﬁnition can be type-checked separately, solely relying on the process’ local
Ψ (and Γ ), at run-time, the entire order that a conﬁguration relies upon is
considered. We give the conﬁguration typing rules in Fig. 10.
Our progress theorem crucially depends on the guarantee that the Invariants 1 and 2 from Sect. 3 hold for every linear process in a conﬁguraw
tion’s tree. This is expressed by the premises Inv1 (proc(aL , wa1 ↕waa32 , PaL )) and
wa3
Inv2 (proc(aL , wa1 ↕wa2 , PaL )) in rule (T-Θ2 ), based on the Deﬁnitions 1 and 2
below that restate Invariants 1 and 2 for an entire conﬁguration. We note that
Invariant 2 is based on the set of all transitive children (i.e., descendants) of a
process. We formally deﬁne the notion of a descendant inductively over a welltyped linear conﬁguration. The interested reader can ﬁnd the deﬁnition in the
companion technical report [4].
Invariant 1 (min(parent) ≤ self(acquired child) ≤ max(parent)). If Ψ ; Γ ⊨ Θ ::
wa
Φ, Δ and for any proc(aL , wa1 ↕wa32 , PaL ) ∈ Θ such that Ψ ; Γ ; Φ1 ; Δ1 ⊢ PaL :: (aL :
w
w
AL [wa1 ↕waa32 ]), Inv1 (proc(aL , wa1 ↕waa32 , PaL )) holds if an only if for every acquired
wb3
resource bL : BL [wb1 ↕wb2 ] ∈ Φ1 it holds that Ψ ∗ ⊢ wa2 ≤ wb1 ≤ wa3 . Moreover,
wc
if PaL = xL ← acquire cS ; QxL , for a (cS : ↑SL CL [wc1 ↕wc32 ]) ∈ Γ , then, for every
wb3
acquired resource bL : BL [wb1 ↕wb2 ] ∈ Φ1 , it holds that Ψ + ⊢ wb1 < wc1 and that
Ψ ∗ ⊢ wa2 ≤ wc1 ≤ wa3 .

## PDF page 19

Manifest Deadlock-Freedom for Shared Session Types

629

Fig. 10. Conﬁguration typing

Invariant 2 (max(parent) < minima(descendants)). If Ψ ; Γ ⊨ Θ :: Φ, Δ
wa
and for any proc(aL , wa1 ↕wa32 , PaL ) ∈ Θ and that process’ descendants (Ψ ; Γ ⊨
wa
Θ :: Φ, Δ) ▷ aL = (Φ′ , Δ′ ), Inv2 (proc(aL , wa1 ↕wa32 , PaL )) holds iﬀ for every
wb
descendant bL : BL [wb1 ↕wb32 ] ∈ (Φ′ , Δ′ ) it holds that Ψ + ⊢ wa3 < wb2 .
Our preservation theorem states that Invariants 1 and 2 are preserved for
every linear process in the conﬁguration along transitions. Moreover, the theorem
expresses that the types of the providing linear channels Φ and Δ are maintained
along transitions and that new shared channels and worlds may be allocated.
The proof relies, in particular, on session types being strictly equi-synchronizing,
on a process’ type well-formedness and assurance that the process’ min world is
less than or equal to its max world.
Theorem 5.1 (Preservation). If Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ and Λ; Θ −→ Λ′ ; Θ′ ,
then Ψ ′ ; Γ ′ ⊨ Λ′ ; Θ′ :: Γ ′ ; Φ, Δ, for some Λ′ , Θ′ , Ψ ′ , and Γ ′ .
5.2

Progress

In our development so far we have distilled the two scenarios of interdependencies between processes that can lead to deadlocks: cyclic acquisitions and
interdependent acquisitions and synchronizations. This has lead to the development of a type system that ingrains the notions of competitors and collaborators,
such that the former compete for a set of resources whereas the latter do not
overlap in the set of resources they acquire. Our type system then ties these
notions to a conﬁguration’s linear process tree such that collaborators stand in a
parent-descendant relationship to each other and competitors in a sibling/cousin
relationship. In this section, we prove that this orchestration is suﬃcient to rule
out any of the aforementioned interdependencies.

## PDF page 20

630

S. Balzer et al.

To this end we introduce the notions of red and green arrows that allow us
to reason about process interdependencies in a conﬁguration’s tree. A red arrow
wb
w
points from a linear proc(aL , wa1 ↕waa32 , Q) to a linear proc(bL , wb1 ↕wb32 , P ), if the
former is attempting to acquire a resource held by the latter and, consequently, is
waiting for the latter to release that resource. A green arrow points from a linear
wb
w
proc(aL , wa1 ↕waa32 , Q) to a linear proc(bL , wb1 ↕wb32 , P ), if the former is waiting to
synchronize with the latter. We deﬁne these arrows formally as follows:
Definition 5.2 (Acquire Dependency — “Red Arrow”). Given a wellformed and well-typed conﬁguration Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ, there exists a waitingdue-to-acquire relation A(Θ) among linear processes in Θ at run-time such that
wb

wa

proc(aL , wa1 ↕wa32 , xL ← acquire cS ; QxL ) <A proc(bL , wb1 ↕wb32 , P ⟨cL ⟩)
where P ⟨cL ⟩ denotes a process term with an occurrence of channel cL .
Definition 5.3 (Synchronization Dependency — “Green Arrow”).
Given a well-formed and well-typed conﬁguration Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ, there
exists a waiting-due-to-synchronization relation S(Θ) among linear processes in
Θ at run-time such that
wa

wb

wb

w

proc(aL , wa1 ↕wa32 , ⟨bL ⟩; Q) <S proc(bL , wb1 ↕wb32 , ⟨¬bL ⟩; P )
proc(bL , wb1 ↕wb32 , ⟨bL ⟩; P ) <S proc(aL , wa1 ↕waa32 , ⟨¬bL ⟩; Q⟨bL ⟩)
where P ⟨aL ⟩ denotes a process term with an occurrence of channel bL , ⟨a⟩; P a
process term that currently executes an action along channel a, and ⟨¬a⟩; P a
process term whose currently executing action does not involve the channel a.
It may be helpful to consult Fig. 3 at this point and note the semantic difference between the violet arrows in that ﬁgure and the red arrows discussed
here. Whereas violet arrows point from the acquiring process to the resource
being acquired, red arrows point from the acquiring process to the process that
is holding the resource. Thus, violet arrows can go out of the tree, while red
arrows stay within. Given the deﬁnitions of red and green arrows, we can deﬁne
the relation W(Θ) on the conﬁguration’s tree, which contains all process pairs
that are in some way waiting for each other:
Definition 5.4 (Waiting Dependency). Given a well-formed and welltyped conﬁguration Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ, there exists a waiting relation
wa
W(Θ) among processes in Θ at run-time such that proc(aL , wa1 ↕wa32 , P ) <W
wb3
proc(bL , wb1 ↕wb2 , Q),
wa

wb

– if proc(aL , wa1 ↕wa32 , P ) <A proc(bL , wb1 ↕wb32 , Q), or
wb
wa
– if proc(aL , wa1 ↕wa32 , P ) <S proc(bL , wb1 ↕wb32 , Q).
Having deﬁned the relation W(Θ), we can now state the key lemma underlying our progress theorem, indicating that W(Θ) is acyclic in a well-formed and
well-typed conﬁguration.

## PDF page 21

Manifest Deadlock-Freedom for Shared Session Types

631

Lemma 5.5 (Acyclicity of W(Θ)). If Ψ ; Γ ⊨ Λ; Θ :: Γ ; Φ, Δ, then W(Θ) is
acyclic.
We focus on explaining the main idea of the proof here. The proof proceeds
by induction on Ψ ; Γ ⊨ Θ :: Φ, Δ, assuming for the non-empty case Ψ ; Γ ⊨
w
w
Θ, proc(aL , wa1 ↕waa32 , PaL ) :: (Φ, Δ, aL : AL [wa1 ↕waa32 ]) that W(Θ) is acyclic, by the
inductive hypothesis. We then know that there cannot exist any paths of green
and red arrows in Θ that form a cycle, and we have to show that there is no
w
way of introducing such a cyclic path by adding node proc(aL , wa1 ↕waa32 , PaL ) to
the conﬁguration Θ. In particular, the proof considers all possible new arrows
that may be introduced by adding the node and that are necessary for creating a
cycle, showing that such arrows cannot come about in a well-typed conﬁguration.
We illustrate the reasoning for the two selected cases shown in Fig. 11. Case
(a) represents a case in which process PaL is waiting to synchronize with its child
PbL while holding a resource a descendant of PbL or PbL itself wants to acquire.
However, this scenario cannot come about in a well-typed conﬁguration because
PaL and PbL are collaborators and thus cannot overlap in resources they acquire.
Case (b) represents a case in which process PaL is waiting to synchronize with
its child PbL while another child, process PcL , is waiting to synchronize with PaL .
Given acyclicity of W(Θ), a necessary condition for a cycle to form is that there
already must exist a red arrow C in the conﬁguration that connects the subtrees
in which the siblings PbL and PcL reside. However, this scenario cannot come
about in a well-typed conﬁguration because PbL and PcL are competitors, forcing
PcL or any of its descendant to release a resource before synchronizing with PaL .
These arguments are made precise in various lemmas in [4].

(a)
A

PbL

(b)

PaL

B

C

A

PcL

PaL

PbL

B

PcL
C

Fig. 11. Two prototypical cases in proof of acyclicty of W(Θ).

Given acyclicity of W(Θ), we can state and prove the following strong
progress theorem. The theorem relies on the notion of a poised process, a process currently executing an action along its oﬀering channel, and distinguishes
a conﬁguration only consisting of the top-level, linear “main” process from one
that consists of several linear processes. We use |Θ| to denote the cardinality
of Θ:

## PDF page 22

632

S. Balzer et al.
wc

Theorem 5.6 (Progress). If Ψ ; Γ ⊨ Λ; Θ :: (Γ ; cL : 1[wc1 ↕wc32 ]), then either
– Λ −→ Λ′ , for some Λ′ , or
– Λ is poised and
• if |Θ| = 1, then either Λ; Θ −→ Λ′ ; Θ′ , for some Λ′ and Θ′ , or Θ is poised,
or
• if |Θ| > 1, then Λ; Θ −→ Λ′ ; Θ′ , for some Λ′ and Θ′ .
The theorem indicates that, as long as there exist at least two linear processes
in the conﬁguration, the conﬁguration can always step. If the conﬁguration only
consists of the main process, then this process will become poised (i.e., ready to
close), once all sub-computations are ﬁnished. The proof of the theorem relies
on the acyclicity of W(Θ) and the fact that all sessions must be strictly equisynchronizing.

6

Additional Discussion

Linear Forwarding. Our current formalization does not include linear forwarding because a forward changes the process tree and thus endangers the
invariants imposed on it. This means that certain programs from the purely linear fragment may not type-check in our system. However, the correspondingly
η-expanded versions of these programs should be expressible and type-checkable
in SILLS+ . As part of future work, we want to explore the addition of the linear
forward
Ψ + ⊢ ω n < ωu
(T-IdL )
ωn
v
Ψ ; Γ ; · ; yL : AL [ωm ↕ω
ωu ] ⊢ fwd xL yL :: (xL : AL [ωj ↕ωk ])
which allows forwarding to processes that are known to not yet be aliased and
whose world annotations meet the premise Ψ + ⊢ ωn < ωu . Restricting to processes in Δ should uphold Invariant 1, while the premise of the rule should uphold
Invariant 2. However, this change will aﬀect the inner working of the proofs, the
use of inversion in particular, which might have far-reaching consequences that
need to be carefully explored.
Unbounded Process Networks and World Polymorphism. The typing
discipline presented in the previous sections, while rich enough to account for
a wide range of interesting programs, cannot type programs that spawn a statically undetermined number of shared sessions that are then to be used. For
instance, while we can easily type a conﬁguration of any given number of dining
philosophers (Sect. 3.3), we cannot type a recursive process in which the number
of philosophers (and forks) is potentially unbounded (as done in [21,38]), due to
the way worlds are created and propagated across processes.
The general issue lies in implementing a statically unbounded network of processes that interact with each other. These interactions require the processes to
be spawned at diﬀerent worlds which must be generated dynamically as needed.

## PDF page 23

Manifest Deadlock-Freedom for Shared Session Types

633

To interact with such a statically unknown number of processes uniformly, their
oﬀering channels must be stored in a list-like structure for later use. However,
in our system, recursive types have to be invariant with respect to worlds. For
r
instance, in a recursive type such as T = AL @ωl ↕ω
ωp ⊗T , the worlds ωl , ωp , ωr
are ﬁxed in the unfoldings of T . Thus, we cannot type a world-heterogeneous
list and cannot form such process networks.
Given that the issues preventing us from typing such unbounded networks
lie in problems of world invariance, the natural solution is to explore some form
of world polymorphism, where types can be parameterized by worlds which are
instantiated at a later stage. Such techniques have been studied in the context of
hybrid logical processes in [7] by considering session types of the form ∀δ.A and
∃δ.A, sessions that are parametric in the world variable δ, that is instantiated
by a concrete reachable world at runtime. While their development cannot be
mapped directly to our setting, it is a promising avenue of future work.

7

Related Work

Behavioral Type Analysis of Deadlocks. The addition of channel usage
information to types in a concurrent, message-passing setting was pioneered by
Kobayashi and Igarashi [30,34], who applied the idea to deadlock prevention
in the π-calculus and later to more general properties [31,32], giving rise to a
generic system that can be instantiated to produce a variety of concrete typing
disciplines for the π-calculus (e.g., race detection, deadlock detection, etc.).
This line of work types π-calculus processes with a simpliﬁed form of process (akin to CCS [42] terms without name restriction) that characterizes the
input/output behavior of processes. These types are augmented with abstract
data that pertain to the relative ordering of channel actions, with the type system ensuring that the transitive closure of such orderings forms a strict partial
order, ensuring deadlock-freedom (i.e., communication succeeds unless a process
diverges). Building on this, Kobayashi et al. proposed type systems that ensure
a stronger property dubbed lock-freedom [35] (i.e., communication always succeeds), and variants that are amenable to type inference [36,39]. Kobayashi [37]
extended this latter system to more accurately account for recursive processes
while preserving the existence of a type inference algorithm.
Our system draws signiﬁcant inspiration from this line of work, insofar as we
also equip types with abstract ordering data on certain communication actions,
which is then statically enforced to form a strict partial order. We note that
our SILLS+ language diﬀers suﬃciently from the pure π-calculus in terms of its
constructs and semantics to make the formulation of a direct comparison or an
immediate application of their work unclear (e.g., [37] uses replication to encode
recursive processes). Moreover, we integrate this style of order-based reasoning
with both linear and shared session typing, which interact in non-trivial ways
(especially in the presence of recursive types and recursive process deﬁnitions).
In terms of typability, enforcing session ﬁdelity can be a double-edged sword:
some examples of the works above can be transposed to SILLS+ with mostly

## PDF page 24

634

S. Balzer et al.

cosmetic changes and without making use of shared sessions (e.g., a parallel
implementation of factorial that recurses via replication but always answers on
a private channel); others are incompatible with linear sessions and require the
use of shared sessions via the acquire-release discipline, which entails a more
indirect but still arguably faithful modelling of the original π-calculus behavior;
some examples, however, cannot be easily adapted to the shared session discipline (e.g., ∗c?(x, y).x?(z).y?(z) | ∗c?(x, y).y?(z).x?(z) is typable in [37], where
x?(z) denotes input on x and ∗c?(x, y) denotes replicated input) and their transcription, while possible, would be too far removed from the original term to
be deemed a faithful representation. Recursive processes are known to produce
patterns that can be challenging to analyze using such order-based techniques.
The work of [21,38] specializes Kobayashi’s system to account for potentially
unbounded process networks with non-trivial forms of sharing. Such systems are
not typable in our work (see Sect. 6 for additional discussion on this topic).
The work of Padovani [44] develops techniques inspired by [35,37] to develop
a typing system for deadlock (and lock) freedom for the linear π-calculus where
(linear) channels must be used exactly once. By enforcing this form of linearity,
the resulting system uses only one piece of ordering data per channel usage and
can easily integrate a form of channel polymorphism that accounts for intricate
cyclic interleavings of recursive processes. The combination of manifest sharing
and linear session typing does not seem possible without the use of additional
ordering data, and the lack of single-use linear channels make the robust channel
polymorphism of [44] not feasible in our setting.
Dardha and Gay [15] recently integrated a system of Kobayashi-style orderings in a logical session π-calculus based on classical linear logic, extended with
the ability to form cyclic dependencies of actions on linear session channels
(Atkey et al. [1] study similar cycles but do not consider deadlock-freedom),
without the need for new process constructs or an acquire-release discipline.
Their work considers only a restricted form of replication common in linear logicbased works, not including recursive types nor recursive process deﬁnitions. This
reduces the complexity of their system, at the cost of expressiveness. We also
note that the cycles enabled by their system are produced by processes sharing
multiple linear names. Since linearity is still enforced, they cannot represent the
more general form of cycles that exploit shared channels, as we do.
A comparative study of session typing and Kobayashi-style systems in terms
of sharing was developed by Dardha and Pérez [16], showing that such orderbased techniques can account for sharing in ways that are out of reach of both
classical session typing and pure logic-based session typing. Our system (and
that of [15]) aims to combine the heightened power of Kobayashi-style systems
with the beneﬁts of session typing, which seems to be better suited as a typing
discipline for a high-level programming language [18].
Progress and Session Typing. To address limitations of classical binary session types, Honda et al. [27] introduced multiparty session types, where sessions
are described by so-called global types that capture the interactions between
an arbitrary number of session participants. Under some well-formedness

## PDF page 25

Manifest Deadlock-Freedom for Shared Session Types

635

constraints, global types can be used to ensure that a collection of processes
correctly implements the global behavior in a deadlock-free way. However, these
global type-based approaches do not ensure deadlock freedom in the presence of
higher-order channel passing or interleaved multiparty sessions. Coppo et al. [13]
and Bettini et al. [6] develop systems that track usage orders among interleaved
multiparty sessions, ruling out cyclic dependencies that can lead to deadlocks.
The resulting system is quite intricate, since it combines the full multiparty session theory with the order tracking mechanism, interacts negatively with recursion (essentially disallowing interleaving with recursion) and, by tracking order
at the multiparty session-level, ends up rejecting various benign conﬁgurations
that can be accounted for by our more ﬁne-grained analysis. We also highlight
the analyses of Vieira and Vasconcelos [54] and Padovani et al. [45] that are more
powerful than the approaches above, at the cost of a more complex analysis based
on conversation types [10] (themselves a partial-order based technique).
Static Analysis of Concurrent Programs. Lange et al. [40,41] develop a
deadlock detection framework applied to the Go programming language. Their
work distills CCS processes from programs which are then checked for deadlocks
by a form of symbolic execution [40] and model-checked against modal μ-calculus
formulae [41] which encode deadlock-freedom of the abstracted process (among
other properties of interest). Their abstraction introduces some distance between
the original program and the analysed process and so the analysis is sound only
for certain restricted program fragments, excluding any combination of recursion
and process spawning. Our direct approach does not suﬀer from this limitation.
de’Liguoro and Padovani [17] develop a typing discipline for deadlock-freedom
in a setting where processes exchange messages via unordered mailboxes. Their
calculus subsumes the actor model and their analysis combines both so-called
mailbox types and specialized dependency graphs to track potential cycles
between mailboxes in actor-based systems. The unordered nature of actor-based
communication introduces signiﬁcant diﬀerences wrt our work, which crucially
exploits the ordering of exchanged messages.

8

Concluding Remarks

In this paper we have developed the concept of manifest deadlock-freedom in
the context of the language SILLS+ , a shared session-typed language, showcasing
both the programming methodology and the expressiveness of our framework
with a series of examples. Deadlock-freedom of well-typed programs is established by a novel abstraction of so-called green and red arrows to reason about
the interdependencies between processes in terms of linear and shared channel
references.
In future work, we plan to address some of the limitations of the interactions
of deadlock-free shared sessions with recursion, by considering promising notions
of world polymorphism and world communication. We also plan to study the
problem of world inference and the inclusion of a linear forwarding construct.

## PDF page 26

636

S. Balzer et al.

References
1. Atkey, R., Lindley, S., Morris, J.G.: Conﬂation confers concurrency. In: Lindley, S.,
McBride, C., Trinder, P., Sannella, D. (eds.) A List of Successes That Can Change
the World. LNCS, vol. 9600, pp. 32–55. Springer, Cham (2016). https://doi.org/
10.1007/978-3-319-30936-1 2
2. Balzer, S., Pfenning, F.: Manifest sharing with session types. Proc. ACM Program.
Lang. (PACMPL) 1(ICEP), 37:1–37:29 (2017)
3. Balzer, S., Pfenning, F., Toninho, B.: A universal session type for untyped asynchronous communication. In: 29th International Conference on Concurrency Theory (CONCUR). LIPIcs, pp. 30:1–30:18. Schloss Dagstuhl - Leibniz-Zentrum fuer
Informatik (2018)
4. Balzer, S., Toninho, B., Pfenning, F.: Manifest deadlock-freedom for shared session
types. Technical report CMU-CS-19-102, Carnegie Mellon University (2019)
5. Benton, P.N.: A mixed linear and non-linear logic: proofs, terms and models. In:
Pacholski, L., Tiuryn, J. (eds.) CSL 1994. LNCS, vol. 933, pp. 121–135. Springer,
Heidelberg (1995). https://doi.org/10.1007/BFb0022251
6. Bettini, L., Coppo, M., D’Antoni, L., Luca, M.D., Dezani-Ciancaglini, M., Yoshida,
N.: Global progress in dynamically interleaved multiparty sessions. In: van Breugel,
F., Chechik, M. (eds.) CONCUR 2008. LNCS, vol. 5201, pp. 418–433. Springer,
Heidelberg (2008). https://doi.org/10.1007/978-3-540-85361-9 33
7. Caires, L., Pérez, J.A., Pfenning, F., Toninho, B.: Logic-based domain-aware session types, unpublished draft
8. Caires, L., Pfenning, F.: Session types as intuitionistic linear propositions. In:
Gastin, P., Laroussinie, F. (eds.) CONCUR 2010. LNCS, vol. 6269, pp. 222–236.
Springer, Heidelberg (2010). https://doi.org/10.1007/978-3-642-15375-4 16
9. Caires, L., Pfenning, F., Toninho, B.: Linear logic propositions as session types.
Math. Struct. Comput. Sci. 26(3), 367–423 (2016)
10. Caires, L., Vieira, H.T.: Conversation types. Theor. Comput. Sci. 411(51–52),
4399–4440 (2010)
11. Castro, D., Hu, R., Jongmans, S., Ng, N., Yoshida, N.: Distributed programming using role-parametric session types in go: statically-typed endpoint APIs
for dynamically-instantiated communication structures. PACMPL 3(POPL), 29:1–
29:30 (2019)
12. Cervesato, I., Scedrov, A.: Relating state-based and process-based concurrency
through linear logic. Inf. Comput. 207(10), 1044–1077 (2009)
13. Coppo, M., Dezani-Ciancaglini, M., Yoshida, N., Padovani, L.: Global progress for
dynamically interleaved multiparty sessions. Math. Struct. Comput. Sci. 26(2),
238–302 (2016)
14. Crary, K., Harper, R., Puri, S.: What is a recursive module? In: ACM SIGPLAN
Conference on Programming Language Design and Implementation (PLDI), pp.
50–63 (1999)
15. Dardha, O., Gay, S.J.: A new linear logic for deadlock-free session-typed processes.
In: Baier, C., Dal Lago, U. (eds.) FoSSaCS 2018. LNCS, vol. 10803, pp. 91–109.
Springer, Cham (2018). https://doi.org/10.1007/978-3-319-89366-2 5
16. Dardha, O., Pérez, J.A.: Comparing deadlock-free session typed processes. In:
EXPRESS/SOS, pp. 1–15 (2015)
17. de’Liguoro, U., Padovani, L.: Mailbox types for unordered interactions. In: 32nd
European Conference on Object-Oriented Programming, ECOOP 2018, pp. 15:1–
15:28 (2018)

## PDF page 27

Manifest Deadlock-Freedom for Shared Session Types

637

18. Gay, S.J., Gesbert, N., Ravara, A.: Session types as generic process types. In: 21st
International Workshop on Expressiveness in Concurrency and 11th Workshop on
Structural Operational Semantics, EXPRESS/SOS 2014, pp. 94–110 (2014)
19. Gay, S.J., Hole, M.: Subtyping for session types in the π-calculus. Acta Informatica
42(2–3), 191–225 (2005)
20. Gay, S.J., Vasconcelos, V.T., Ravara, A., Gesbert, N., Caldeira, A.Z.: Modular session types for distributed object-oriented programming. In: 37th ACM SIGPLANSIGACT Symposium on Principles of Programming Languages (POPL), pp. 299–
312 (2010)
21. Giachino, E., Kobayashi, N., Laneve, C.: Deadlock analysis of unbounded process
networks. In: Baldan, P., Gorla, D. (eds.) CONCUR 2014. LNCS, vol. 8704, pp.
63–77. Springer, Heidelberg (2014). https://doi.org/10.1007/978-3-662-44584-6 6
22. Gommerstadt, H., Jia, L., Pfenning, F.: Session-typed concurrent contracts. In:
Ahmed, A. (ed.) ESOP 2018. LNCS, vol. 10801, pp. 771–798. Springer, Cham
(2018). https://doi.org/10.1007/978-3-319-89884-1 27
23. Griﬃth, D.: Polarized substructural session types. Ph.D. thesis, University of Illinois at Urbana-Champaign (2016)
24. Griﬃth, D., Pfenning, F.: SILL (2015). https://github.com/ISANobody/sill
25. Honda, K.: Types for dyadic interaction. In: Best, E. (ed.) CONCUR 1993. LNCS,
vol. 715, pp. 509–523. Springer, Heidelberg (1993). https://doi.org/10.1007/3-54057208-2 35
26. Honda, K., Vasconcelos, V.T., Kubo, M.: Language primitives and type discipline
for structured communication-based programming. In: Hankin, C. (ed.) ESOP
1998. LNCS, vol. 1381, pp. 122–138. Springer, Heidelberg (1998). https://doi.org/
10.1007/BFb0053567
27. Honda, K., Yoshida, N., Carbone, M.: Multiparty asynchronous session types. In:
35th ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (POPL), pp. 273–284. ACM (2008)
28. Hu, R., Yoshida, N.: Hybrid session veriﬁcation through endpoint API generation.
In: Stevens, P., Wasowski, A. (eds.) FASE 2016. LNCS, vol. 9633, pp. 401–418.
Springer, Heidelberg (2016). https://doi.org/10.1007/978-3-662-49665-7 24
29. Hu, R., Yoshida, N.: Explicit connection actions in multiparty session types. In:
Huisman, M., Rubin, J. (eds.) FASE 2017. LNCS, vol. 10202, pp. 116–133. Springer,
Heidelberg (2017). https://doi.org/10.1007/978-3-662-54494-5 7
30. Igarashi, A., Kobayashi, N.: Type-based analysis of communication for concurrent
programming languages. In: Van Hentenryck, P. (ed.) SAS 1997. LNCS, vol. 1302,
pp. 187–201. Springer, Heidelberg (1997). https://doi.org/10.1007/BFb0032742
31. Igarashi, A., Kobayashi, N.: A generic type system for the Pi-calculus. In: Conference Record of POPL 2001: The 28th ACM SIGPLAN-SIGACT Symposium on
Principles of Programming Languages, pp. 128–141 (2001)
32. Igarashi, A., Kobayashi, N.: A generic type system for the Pi-calculus. Theor.
Comput. Sci. 311(1–3), 121–163 (2004)
33. Jespersen, T.B.L., Munksgaard, P., Larsen, K.F.: Session types for rust. In: 11th
ACM SIGPLAN Workshop on Generic Programming, WGP 2015, pp. 13–22 (2015)
34. Kobayashi, N.: A partially deadlock-free typed process calculus. In: Proceedings
of the 12th Annual IEEE Symposium on Logic in Computer Science, pp. 128–139
(1997)
35. Kobayashi, N.: A type system for lock-free processes. Inf. Comput. 177(2), 122–159
(2002)
36. Kobayashi, N.: Type-based information ﬂow analysis for the π-calculus. Acta Inf.
42(4–5), 291–347 (2005)

## PDF page 28

638

S. Balzer et al.

37. Kobayashi, N.: A new type system for deadlock-free processes. In: Baier, C.,
Hermanns, H. (eds.) CONCUR 2006. LNCS, vol. 4137, pp. 233–247. Springer,
Heidelberg (2006). https://doi.org/10.1007/11817949 16
38. Kobayashi, N., Laneve, C.: Deadlock analysis of unbounded process networks. Inf.
Comput. 252, 48–70 (2017)
39. Kobayashi, N., Saito, S., Sumii, E.: An implicitly-typed deadlock-free process calculus. In: Palamidessi, C. (ed.) CONCUR 2000. LNCS, vol. 1877, pp. 489–504.
Springer, Heidelberg (2000). https://doi.org/10.1007/3-540-44618-4 35
40. Lange, J., Ng, N., Toninho, B., Yoshida, N.: Fencing oﬀ go: liveness and safety
for channel-based programming. In: 44th ACM SIGPLAN-SIGACT Symposium
on Principles of Programming Languages (POPL), pp. 748–761. ACM (2017)
41. Lange, J., Ng, N., Toninho, B., Yoshida, N.: A static veriﬁcation framework for
message passing in go using behavioural types. In: Proceedings of the 40th International Conference on Software Engineering, ICSE 2018, Gothenburg, Sweden, 27
May–03 June 2018, pp. 1137–1148 (2018)
42. Milner, R.: A Calculus of Communicating Systems. LNCS, vol. 92. Springer,
Heidelberg (1980). https://doi.org/10.1007/3-540-10235-3
43. Neykova, R., Hu, R., Yoshida, N., Abdeljallal, F.: A session type provider: compiletime API generation of distributed protocols with reﬁnements in F#. In: Proceedings of the 27th International Conference on Compiler Construction, CC 2018, pp.
128–138 (2018)
44. Padovani, L.: Deadlock and lock freedom in the linear π-calculus. In: Computer
Science Logic - Logic in Computer Science (CSL-LICS), pp. 72:1–72:10 (2014)
45. Padovani, L., Vasconcelos, V.T., Vieira, H.T.: Typing liveness in multiparty communicating systems. In: Kühn, E., Pugliese, R. (eds.) COORDINATION 2014.
LNCS, vol. 8459, pp. 147–162. Springer, Heidelberg (2014). https://doi.org/10.
1007/978-3-662-43376-8 10
46. Pérez, J.A., Caires, L., Pfenning, F., Toninho, B.: Linear logical relations and
observational equivalences for session-based concurrency. Inf. Comput. 239, 254–
302 (2014)
47. Pfenning, F., Griﬃth, D.: Polarized substructural session types. In: Pitts, A. (ed.)
FoSSaCS 2015. LNCS, vol. 9034, pp. 3–22. Springer, Heidelberg (2015). https://
doi.org/10.1007/978-3-662-46678-0 1
48. Reed, J.: A judgmental deconstruction of modal logic, January 2009. http://www.
cs.cmu.edu/∼jcreed/papers/jdml.pdf, unpublished manuscript
49. Scalas, A., Dardha, O., Hu, R., Yoshida, N.: A linear decomposition of multiparty
sessions for safe distributed programming. In: 31st European Conference on ObjectOriented Programming, ECOOP 2017, pp. 24:1–24:31 (2017)
50. Scalas, A., Yoshida, N.: Lightweight session programming in scala. In: 30th European Conference on Object-Oriented Programming, ECOOP 2016, pp. 21:1–21:28
(2016)
51. Toninho, B.: A logical foundation for session-based concurrent computation. Ph.D.
thesis, Carnegie Mellon University and New University of Lisbon (2015)
52. Toninho, B., Caires, L., Pfenning, F.: Higher-order processes, functions, and sessions: a monadic integration. In: Felleisen, M., Gardner, P. (eds.) ESOP 2013.
LNCS, vol. 7792, pp. 350–369. Springer, Heidelberg (2013). https://doi.org/10.
1007/978-3-642-37036-6 20

## PDF page 29

Manifest Deadlock-Freedom for Shared Session Types

639

53. Vasconcelos, V.T.: Fundamentals of session types. Inf. Comput. 217, 52–70 (2012)
54. Vieira, H.T., Vasconcelos, V.T.: Typing progress in communication-centred systems. In: De Nicola, R., Julien, C. (eds.) COORDINATION 2013. LNCS, vol.
7890, pp. 236–250. Springer, Heidelberg (2013). https://doi.org/10.1007/978-3642-38493-6 17
55. Wadler, P.: Propositions as sessions. In: 17th ACM SIGPLAN International Conference on Functional Programming (ICFP), pp. 273–286. ACM (2012)

Open Access This chapter is licensed under the terms of the Creative Commons
Attribution 4.0 International License (http://creativecommons.org/licenses/by/4.0/),
which permits use, sharing, adaptation, distribution and reproduction in any medium
or format, as long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons license and indicate if changes were
made.
The images or other third party material in this chapter are included in the chapter’s
Creative Commons license, unless indicated otherwise in a credit line to the material. If
material is not included in the chapter’s Creative Commons license and your intended
use is not permitted by statutory regulation or exceeds the permitted use, you will
need to obtain permission directly from the copyright holder.
