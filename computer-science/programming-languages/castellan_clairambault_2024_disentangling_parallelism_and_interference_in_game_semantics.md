Source: https://doi.org/10.46298/LMCS-20(3:24)2024
PDF sha256: 579b53e4f9aa059aee0e21ba4a13fab973ba9c35cddd68005c0aa4d92ba7ad5a
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters, repetition)

# Transcription of castellan_clairambault_2024_disentangling_parallelism_and_interference_in_game_semantics.pdf

Transcription of `castellan_clairambault_2024_disentangling_parallelism_and_interference_in_game_semantics.pdf` in this directory, 130 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-130 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Logical Methods in Computer Science
Volume 20, Issue 3, 2024, pp. 24:1–24:130
https://lmcs.episciences.org/

Submitted
Published

Jul. 13, 2021
Sep. 18, 2024

DISENTANGLING PARALLELISM AND INTERFERENCE
IN GAME SEMANTICS
a

SIMON CASTELLAN

AND PIERRE CLAIRAMBAULT

a

Inria, Univ Rennes, CNRS, IRISA
e-mail address: Simon.Castellan@inria.fr

b

CNRS, Aix Marseille Univ, LIS, Marseille, France
e-mail address: Pierre.Clairambault@cnrs.fr

b

Abstract. Game semantics is a denotational semantics presenting compositionally the
computational behaviour of various kinds of effectful programs. One of its celebrated
achievement is to have obtained full abstraction results for programming languages with a
variety of computational effects, in a single framework. This is known as the semantic cube or
Abramsky’s cube, which for sequential deterministic programs establishes a correspondence
between certain conditions on strategies (“innocence”, “well-bracketing”, “visibility”) and
the absence of matching computational effects.
Outside of the sequential deterministic realm, there are still a wealth of game semanticsbased full abstraction results; but they no longer fit in a unified canvas. In particular, Ghica
and Murawski’s fully abstract model for shared state concurrency (IA ) does not have a
matching notion of pure parallel program – we say that parallelism and interference (i.e.
state plus semaphores) are entangled. In this paper we construct a causal version of Ghica
and Murawski’s model, also fully abstract for IA . We provide compositional conditions
parallel innocence and sequentiality, respectively banning interference and parallelism, and
leading to four full abstraction results. To our knowledge, this is the first extension of
Abramsky’s semantic cube programme beyond the sequential deterministic world.

Introduction
How to prove that a program P is correct, or equivalent to P 1 ? This simple question, prerequisite for formally validating software, lies at the heart of decades of work in semantics. Its
study prompted a wealth of developments, each with its methodology and scope. Operational
semantics axiomatizes execution directly on syntax, while denotational semantics gives
meaning to programs by embedding them in a syntax-independent mathematical space.
Operational semantics is powerful and extensible, perfectly fit for formalization in a proof
assistant – it is, for instance, behind the celebrated CompCert project [Ler09]. On the other
hand, its deployment often follows from ad-hoc choices, and it is not robust to variations
in the language. It is tied to syntax and struggles with compositionality1. Denotational
Key words and phrases: Denotational semantics, game semantics, concurrent games.
1Operational semantics can be made compositional, but behind lie denotational structures: for instance,

the operational semantics behind the recent Compositional CompCert [SBCA15] “bears much in common”
(quoting the paper) with Ghica and Tzevelekos’ operational reconstruction of game semantics [GT12].

l

LOGICAL METHODS
IN COMPUTER SCIENCE

DOI:10.46298/LMCS-20(3:24)2024

© S. Castellan and P. Clairambault
CC
⃝
Creative Commons

## PDF page 2

24:2

S. Castellan and P. Clairambault

Vol. 20:3

semantics is syntax-independent, and often more principled. It is a great tool to reason
about program equivalence (two programs being equivalent if they denote the same object),
to prove general properties of languages (e.g. termination), and it comes with compositional
reasoning principles. The wider mathematical space in which programs are embedded
sometimes suggests new useful constructs (it is the birth story of Linear Logic [Gir87]). In
exchange, it is more mathematically demanding and often quite brittle: distinct fragments of
the same language may require radically different representations. Traditional denotational
semantics (e.g. Scott domains) model programs as functions, through their input/output
behaviour. Effects (e.g. state, non-determinism, etc) can be captured via monads which do
not readily combine. Though combining effects has been a driving question in denotational
semantics these past decades, it is hardly a streamlined process. For instance, though
there is significant recent research activity around domain settings supporting probabilities
and higher-order [SYW` 16, VKS19], it is unclear how they combine with non-determinism
[Gou17], let alone concurrency; nor how all these models relate together.
Game semantics [HO00, AJM00], though also denotational, takes a different approach:
instead of a function it represents a program as a strategy, a collection of (representations
of) its interactions against execution environments. Once executions are first-class citizens
(called plays) one can characterise those achievable with specific effects. This led to a wealth
of fully abstract models, rewarded in 2017 by the Alonzo Church Award (from the ACM
SIGLOG, the EATCS, the EACSL, and the Kurt Gödel Society). To cite the announcement:
“Game semantics has changed the landscape of programming language semantics by giving a unified view of the denotational universes of many different
languages. This is a remarkable achievement that was not previously thought
to be within reach.”
But are games models truly “unified”? For deterministic sequential programs, absolutely:
various degrees of control and state are indeed captured as additional conditions on one
single canvas [AM99a] – this is the semantic cube or Abramsky cube. But beyond the
sequential deterministic world, the picture is not so clear. The classic fully abstract models
for finite non-determinism [HM99], for probabilistic choice [DH00] or for parallelism [GM08]
all rely on the presence of state. Until recently, there were no fully abstract model for any
of these without state – or in the language of game semantics, there were no notions of
non-deterministic, probabilistic or parallel innocence. Following the phrasing of the title,
our understanding of these effects was entangled with state.
However, this picture is currently shifting. Recently, two notions of non-deterministic
innocence were proposed independently [CCW14, TO15] – the two settings also handling
probabilistic innocence [TO14, CCPW18]. Technically, these settings differ significantly.
But conceptually, both enrich strategies with explicit branching information. Though the
novelty may seem minor, this is in fact a major schism with respect to traditional game
semantics, in that this branching information is typically not observable. So instead of a
strategy being merely a formal description of how a program is observed by a certain type of
contexts, the model starts to carry more intensional, causal information, typically inaccessible
to the environment but which nonetheless finds its use in capturing compositionally the
computational behaviour expressible by certain programming features. This suggests that
to disentangle parallelism and state, we must adequately represent the branching structure
of parallel computation, the (non-observable) causal patterns of pure parallel programs.

## PDF page 3

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:3

Enter concurrent games. Concurrent games are a family of game semantics models
questioning in various ways the premise that the basic building block should be totally,
chronologically ordered plays. Pioneered by Melliès and others [AM99b, Mel04, MM07, FP09],
they have lately been under intense development, prompted by new definitions due to
Rideau and Winskel [RW11]. The name comes from their relationship with the so-called
true concurrency approach to concurrency theory, following which one represents causal
dependence and independence of events explicitly rather than resorting to interleavings.
Besides making concurrent games a natural target to model concurrent languages and process
calculi [CC16, CY19], it provides us with the required causal description of programs.
Contributions. We disentangle parallelism and state – or rather parallelism and interference,
which we intend to also encompass semaphores. More precisely, we provide a fully abstract
model of Idealized Parallel Algol (IA ), the paradigmatic language used in the game semantics
literature to study shared memory concurrency on top of a higher-order language. Our model
is a causal version of that of Ghica and Murawski [GM08], which additionally supports
compositional conditions of parallel innocence and sequentiality respectively eliminating
interference and parallelism. Accordingly the paper presents four full abstraction results,
following all combinations of parallelism and interference on top of the pure language PCF.
Thus this is a semantic square [AM99a], the first such result pushing Abramsky’s programme
beyond the sequential deterministic world.
Of the four full abstraction results glued together, three are classics: Hyland and Ong’s
full abstraction for PCF [HO00], Abramsky and McCusker’s full abstraction for Idealized
Algol (IA) [AM96], and Ghica and Murawski’s full abstraction for IA [GM08]. The fourth
result is a variation of the full abstraction for PCF with respect to parallel evaluation initially
presented in conference format in [CCW15] – in particular, the notion of parallel innocence
comes from there2 and was developed as part as the first author’s PhD thesis [Cas17].
These four results [HO00, AM96, GM08, CCW15] vary significantly in their technical
underpinnings. For the purposes of this paper, this left us with the task, more challenging
than anticipated, of providing the glue. Accordingly, a significant part of the paper revisits
the results of [HO00] and [AJM00] in a language closer to concurrent games, mixing ideas
from HO [HO00], AJM [AJM00] and asynchronous [Mel05] games. In doing so we hope
that this paper, gathering in a single framework several important developments of the field,
could also serve as a modern entry point to game semantics. Accordingly we wrote it with
the newcomer in mind, not assuming prior knowledge on game semantics. The development
is self-contained, with however a number of details postponed to the appendix. We also
take the time to show how our model relates to other game semantics frameworks, hopefully
helping the reader get a panoramic perspective on the field. More generally, we try to
keep the text as pedagogical as possible. This of course, has a cost in that the paper is
intimidatingly lengthy; and we hope the readers will excuse us for that.
Outline. In Section 1, we start by describing IA and its fragments. In Section 2, we
introduce our version of alternating games, its interpretation of PCF, and link with more
traditional game semantics. In Section 3, we show how (the absence of) control and state
may be captured via conditions of strategies – we present Abramsky’s cube and some of its
2The paper [CCW15] had two main contributions: a new games model called thin concurrent games, and
parallel innocence. The detailed construction of the former appears in [CCW19], but not parallel innocence.
The present paper provides, among other things, detailed proofs for the second contribution of [CCW15].

## PDF page 4

24:4

S. Castellan and P. Clairambault

Vol. 20:3

consequences. In Section 4, we present our causal fully abstract model for IA , based on
thin concurrent games. In Section 5 we develop one of the key contributions of this paper,
parallel innocence: we leverage the causal description of programs offered by thin concurrent
games to characterize the causal shapes definable with pure parallel higher-order programs.
In Section 6, we study the sequential fragment of our causal games model, and by linking it
with the sequential model of Sections 2 and 3 we show full abstraction results for IA and
PCF. Finally, in Section 7 we prove our last full abstraction result, for PCF .
1. IA and its fragments
Idealized Parallel Algol (IA ) is a higher-order, simply-typed, call-by-name concurrent
language with shared memory and semaphores. We also introduce fragments:
PCF
IA
PCF

is the fragment without interference,
is the fragment without parallelism, and
has neither interference nor parallelism.

1.1. Types. The types of IA are the following, highlighting types relative to interference.
A, B ::“ U | B | N | A Ñ B PCF
| ref | sem
+interference
Above, U is a unit type with only one value, and B and N are types for booleans and
natural numbers. In the presence of interference, ref is a type for references storing natural
numbers, while sem is for semaphores. We refer to U, B and N as ground types, and use
X, Y to range over those. Let us now give the term constructions and typing rules.
1.2. Terms and Typing. We define the terms of the language directly via typing rules.
Contexts are lists x1 : A1 , . . . , xn : An . Typing judgments have the form Γ $ M : A
with Γ a context and A a type. In addition to Figure 1, we consider present an explicit
exchange rule allowing us to permute the order of variable declarations in contexts. The
eliminator rules for basic datatypes are restricted to eliminate only to ground types – general
eliminators are defined as syntactic sugar: e.g. a conditional to ref may be obtained as
Γ$M :B
Γ $ N1 : ref
Γ $ N2 : ref
Γ $ mkvar pλx. if M pN1:“ xq pN2:“ xqq pif M !N1 !N2 q : ref
The bad variable and bad semaphore constructs mkvar and mksem are a common
occurrence in the game semantical literature. While a “good ” reference is tied to a memory
location, many game models also comprise so-called “bad variables” inhabiting ref but
not behaving as actual variables. Full abstraction results [AM96, GM08] often require a
corresponding syntactic construct mkvar allowing one to form bad variables by appending
arbitrary read and write methods3. The same holds for semaphores.
1.3. Further syntactic sugar. First of all, for any type A there is a divergence $ KA : A,
any looping program. Given Γ $ M, N : U, an equality test Γ $ M “U N : B may be defined
as M ; N ; tt. Likewise, for Γ $ M, N : B we define Γ $ M “B N : B as if M N pif N ff ttq,
and Γ $ M “N N : B similarly, with the obvious recursive program.
3Though McCusker proved that equational full abstraction holds for IA without mkvar [McC03].

## PDF page 5

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:5

PCF
Γ $ skip : U

Γ $ tt : B

Γ, x : A $ M : B
A

Γ $ λx . M : A Ñ B
Γ$M :B

Γ $ ff : B

Γ$n:N

Γ$M :AÑB
Γ$N :A
Γ$MN :B

Γ $ N1 : X
Γ $ N2 : X
Γ $ if M N1 N2 : X

Γ, x : A $ x : A

Γ$M :U
Γ$N :X
Γ $ M; N : X

Γ$M :N
Γ $ succ M : N

Γ$M :N
Γ, x : X $ M : Y
Γ$N :X
Γ $ iszero M : B
Γ $ let x “ N in M : Y
`interference
Γ $ M : ref
Γ$N :N
Γ, x : ref $ M : X
Γ $ newref x:“ n in M : X
Γ $ M:“ N : U
Γ, x : sem $ M : X
Γ $ newsem x:“ n in M : X

Γ $ M : sem
Γ $ grab M : U

Γ$M :N
Γ $ pred M : N
Γ$M :AÑA
Γ$YM :A
Γ $ M : ref
Γ $!M : N

Γ $ N : sem
Γ $ release N : U

Γ$M :U
Γ$N :U
Γ$M :NÑU
Γ$N :N
Γ $ mkvar M N : ref
Γ $ mksem M N : sem
`parallelism
Γ, x1 : X, x2 : X $ M : Y
Γ $ N1 : X
Γ $ N2 : X
ˆ
˙
x1 “ N1
Γ $ let
in M : Y
x2 “ N2
Figure 1: Typing rules for IA

We refer to constants of ground type as values; we use v to range over those, and n, b
or c to range over values of respective types N, B or U. We introduce a n-ary case construct
branching on all values of ground types. By abuse of notation, we write V Ďf X for any
finite subset of the values of ground type X. Writing V “ tv1 , . . . , vn u, we set
case M of
v1 ÞÑ N1
v2 ÞÑ N2
...
vn ÞÑ Nn

def

“

let x “ M in
if x “X v1 then N1
else if x “X v2 then N2
...
else if x “X vn then Nn
else K

of type Y in context Γ if Γ $ M : X and Γ $ Ni : Y for all 1 ď i ď n.
The let construct is crucial in this paper: as we shall see later on, strategies may evaluate
a variable once, and provide a different continuation for each possible value. This behaviour
cannot be replicated strictly without let, see Section 3.3.1 for a more detailed discussion.

## PDF page 6

24:6

Vol. 20:3

S. Castellan and P. Clairambault

1.4. Operational semantics. We recall the small-step operational semantics [GM08]. We
fix a countable set L of memory locations. A store is a partial map s : L á N with finite
domain where N stands, overloading notations, for natural numbers. Configurations of
the operational semantics are tuples xM, sy where s is a store with dompsq “ tℓ1 , . . . , ℓn u
and Σ $ M : A with Σ “ ℓ1 : ref , . . . , ℓi : ref , ℓi`1 : sem, . . . , ℓn : sem.
Reduction rules have the form xM, sy ⇝ xM 1 , s1 y where dompsq “ domps1 q; we write ⇝˚
for the reflexive transitive closure. If $ M : X, we write M ó if xM, Hy ⇝˚ xv, Hy for some
value v. We give in Figure 2 the reduction rules – there and from now on in the paper we
use the notation Z to denote the usual set-theoretic union, when it is known disjoint. For
rules which do not interact with the state, we omit the state component – it is simply left
unchanged by stateless basic reductions, and propagated upwards by stateless context rules.
1.5. Fragment languages. Besides PCF, we consider three main languages of interest:
PCF “ PCF ` parallelism
IA “ PCF ` interference
IA “ PCF ` interference ` parallelism
IA is a variant of Idealized Algol with active expressions [AM96], differing only in that it
has semaphores. This is not a significant difference, as semaphores are definable from state
in a sequential language. Likewise, IA is close to the language of [GM08]: it differs only in
that the parallelism operation is more general. For Γ $ M : U and Γ $ N : U we may define
their parallel composition Γ $ M ∥ N : U (as in [GM08]) by
ˆ
˙
x “ M
M ∥ N “ let
in skip .
y “ N
Conversely, for e.g. Γ $ N1 : N, Γ $ N2 : N and Γ, x1 : N, x2 : N $ M : A, the present
parallel let construction is definable via state and parallel composition of commands:
ˆ
˙
x1 “ N1
let
in M “ newref v1:“ 0 in
x2 “ N2
newref v2:“ 0 in pv1:“ N1 ∥ v2:“ N2 q; M r!v1 {x1 , !v2 {x2 s
1.6. Observational Equivalence and Full Abstraction. Here, L may refer to any of
the fragments above. A L-context for the judgment Γ $ A is a term Crs of L with a hole,
s.t. for any Γ $ M : A in L we have $ CrM s : U obtained by replacing the hole with M .
Two terms Γ $ M, N : A of L are L-observationally equivalent iff
M „L N

ô

for all Crs a L-context for Γ $ A,

pCrM s ó

ô

CrN s óq

We omit L when it is clear from the context. Observational equivalence is usually
regarded as the canonical equivalence on programs: L-observationally equivalent programs
are intercheangeable as long as the evaluation context is in L. Accordingly, denotational
semantics often aims to capture observational equivalence. An interpretation of programs
J´K into some mathematical universe is called fully abstract whenever
M „N

ô

JM K “ JN K

for all Γ $ M, N : A. Full abstraction is a gold standard in denotational semantics, as it
captures the best possible match between a language and its semantics, ensuring that the
denotational semantics is complete for proving equivalence between programs.

## PDF page 7

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

Basic red. for PCF
pλxA . M q N
skip; N
if b Ntt Nff
succ n
pred 0
pred pn ` 1q
iszero 0
iszero pn ` 1q
YM
let x “ v in M

⇝
⇝
⇝
⇝
⇝
⇝
⇝
⇝
⇝
⇝

M rN {xs
N
Nb
n`1
0
n
tt
ff
M pY M q
M rv{xs

Basic reductions for interference
newref x in v ⇝ v
newsem x in v ⇝ v
pmkvar M N q:“ n ⇝ M n
!pmkvar M N q ⇝ N
grabpmksem M N q ⇝ M
releasepmksem M N q ⇝ N
Interfering reductions
x!ℓ, s Z tℓ ÞÑ nuy ⇝ xn, s Z tℓ ÞÑ nuy
xℓ:“ n, s Z tℓ ÞÑ uy ⇝ xskip, s Z tℓ ÞÑ nuy
xgrabpℓq, s Z tℓ ÞÑ 0uy ⇝ xskip, s Z tℓ ÞÑ 1uy
xreleasepℓq, s Z tℓ ÞÑ nuy ⇝ xskip, s Z tℓ ÞÑ 0uy (n ą 0)

Basic reduction
ˆ for parallelism
˙
x1 “ v1
let
in M ⇝ M rv1 {x1 , v2 {x2 s
x2 “ v2
Stateless context rules
M ⇝ M1
M ⇝ M1
M ⇝ M1
1
1
MN ⇝M N
if M N1 N2 ⇝ if M N1 N2
succ M ⇝ succ M 1
M ⇝ M1
iszero M ⇝ iszero M 1

N ⇝ N1
M:“ N ⇝ M:“ N 1

M ⇝ M1
releasepM q ⇝ releasepM 1 q

M ⇝ M1
M:“ v ⇝ M 1:“ v

N1 ⇝ N11
x1 “ N1
x2 “ N2

˙

x1 “ N1
x2 “ N2
Stateful context rules

˙

let

ˆ
in M ⇝ let

x1 “ N11
x2 “ N2

˙

x1 “ N1
x2 “ N21

˙

in M

N2 ⇝ N21
ˆ

let

ˆ
in M ⇝ let

M ⇝ M1
!M ⇝ !M 1

M ⇝ M1
grabpM q ⇝ grabpM 1 q

N ⇝ N1
let x “ N in M ⇝ let x “ N 1 in M

ˆ

24:7

in M

xM rℓ{xs, s Z tℓ ÞÑ nuy ⇝ xM 1 rℓ{xs, s1 Z tℓ ÞÑ n1 uy
(ℓ P L fresh)
xnewref x:“ n in M, sy ⇝ xnewref x:“ n1 in M 1 , s1 y
xM rℓ{xs, s Z tℓ ÞÑ nuy ⇝ xM 1 rℓ{xs, s1 Z tℓ ÞÑ n1 uy
(ℓ P L fresh)
xnewsem x:“ n in M, sy ⇝ xnewsem x:“ n1 in M 1 , s1 y

Figure 2: Operational semantics of IA

## PDF page 8

24:8

q´
q`
q´
✓

Vol. 20:3

S. Castellan and P. Clairambault

✓

tt`

ff `

´

q`
✓´

q`

q´

q´

✓`

✓`

pU

q´
✓`

✓´

Figure 4: U ⊸ pU b Uq

Uq

Ñ

B
q´

q`

`

Figure 3: An affine arena

Ñ

✓´

tt`

Figure 5: An alternating play

2. Game Semantics for PCF
2.1. Games and Strategies. We present first a game semantics of PCF. Though it is
sequential, our presentation is non-standard, mixing features of AJM [AJM00], HO [HO00]
and asynchronous games [Mel05] – this is to facilitate the interplay between all the games
models involved. We skip a number of details, found in Appendix B.
Game semantics presents higher-order computation as an exchange of tokens between two
players, called “Player” and “Opponent”. Player stands for the program under evaluation –
events/moves attributed to Player are observable computational events resulting from its
execution: calls to variables, program phrases converging to a value. Opponent stands for the
execution environment. Their interaction follows rules depending on the type of the program
under scrutiny. In setting up a game semantics the first step is to extract from the type a
structure, called a game or an arena, which presents all the observable computational events
available when interacting on this type, along with their respective causal dependencies.
2.1.1. Affine arenas. We first introduce our representation of types as games in the affine
case, i.e. if any computational event can appear at most once – this is merely to first help
the reader build up intuition before handling replication.
Consider pU Ñ Uq Ñ B, where affineness implies that each argument may be called at
most once. Once a call-by-name execution on that type is initiated, the available observable
events are the following: (1) the term may directly converge to tt or ff , without evaluating
its argument; (2) it may call its argument (i.e. it evaluates to λf UÑU . M with M having f
in head position). In the case (2) the control goes back to the environment, which plays for
f : it may prompt f to return the unique value skip, or to itself call its argument. Finally,
if f calls its argument, the corresponding sub-term may reduce to a value.
Overall, these events along with their causal dependencies give rise to the diagram in
Figure 3. It is read from top to bottom, with the dashed lines representing the dependency
relation. Nodes are called moves or events, and are labeled with a polarity, ´ for events due
to the environment, and ` for events due to the program. Finally, the wiggly line between
tt` and ff ` indicates conflict: it represents the fact that only one of these two values may
be observed in one execution, whereas all the other pairs of events could conceivably appear
together. The reader may convince themselves that indeed, the diagram does represent the
observable events in a call-by-name evaluation of pU Ñ Uq Ñ B as outlined in the previous
paragraph. We insist that those are the computational events that are observable in the
interface with the environment: the program may perform internal computation; a program

## PDF page 9

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

q´

q´

✓`

tt`

Figure 6: U

q´
ff `

Figure 7: B

0`

1`

2`

...

Figure 8: N

24:9

q´
0

q´
1

q´
2

...

✓`
0

✓`
1

✓`
2

...

Figure 9: !U

in an extension of PCF with state could possibly store and read from a local variable, etc.
But those are not observable by a context, thus are not represented in the arena.
To formalize the arena as a mathematical structure, we use event structures 4:
Definition 2.1. An event structure (es) is a triple E “ p|E|, ďE , #E q, where |E| is a
(countable) set of events, ďE is a partial order called causal dependency and #E is an
irreflexive symmetric binary relation on |E| called conflict, satisfying:
finite causes: @e P |E|, resE “ te1 P |E| | e1 ďE eu is finite
conflict inheritance: @e1 #E e2 , @e2 ďE e12 , e1 #E e12 .
An event structure with polarities (esp) is an event structure A together with a
function polA : |A| Ñ t´, `u assigning to each event a polarity.
Figure 3 displays an esp. The wiggly line indicates conflict, but we will not put wiggly
lines between all conflicting pairs of events, as long as missing conflicts may be deduced by
conflict inheritance. A conflict that cannot be deduced by inheriting an earlier conflict is
called a minimal conflict. As with Figure 3, we will represent types as esps. In fact, the
event structures arising via the interpretation of types have a very restricted form. In the
definition below, we use the notation e _E e1 in an event structure E to mean immediate
causality, i.e. e ăE e1 with no other event strictly in between.
Definition 2.2. An arena is an esp pA, ďA , #A , polA q satisfying:
alternating: if a1 _A a2 , polA pa1 q ‰ polA pa2 q,
forestial: if a1 ďA a and a2 ďA a, then a1 ďA a2 or a2 ďA a1 ,
race-free: if a1 , a2 P |A| are in minimal conflict, then polA pa1 q “ polA pa2 q.
Besides, a ´-arena additionally satisfies the condition:
negative: if a P minpAq, then polA paq “ ´,
where minpAq stands for the set of minimal events of A.
Types will only yield ´-arenas, but throughout the paper we will use the general case.
Finally, though we motivated Definition 2.1 with arenas, event structures will have other
uses. Notably, from Section 4 onwards, strategies will also be event structures.
2.1.2. Basic Constructions. We give a few basic constructions on event structures and arenas
which will allow us to construct in a systematic way, from any type of PCF, a ´-arena.
We give ´-arenas for the ground types of PCF, in Figures 6, 7 and 8, using the same
notations U, B and N for the arenas as for the types. For N, even though the picture only
shows conflict between neighbours, all positive events are meant to be in pairwise conflict.
4More precisely, those are prime event structures with binary conflict.

## PDF page 10

24:10

S. Castellan and P. Clairambault

Vol. 20:3

We write 1 for the empty es, with no event. If A is an esp, we write AK for its
dual, the esp with same events, causality and conflict, but the opposite polarities, i.e.
polAK paq “ ´polA paq for all a P |A|. The simple parallel composition is defined as follows.
Definition 2.3. If E1 , E2 are two es, their simple parallel composition E1 ∥ E2 has
events:
causality:
conflict:

|E1 ∥ E2 | “ t1u ˆ |E1 | Z t2u ˆ |E2 |
pi, eq ďE1 ∥E2 pj, e1 q ô i “ j & e ďEi e1
pi, eq #E1 ∥E2 pj, e1 q ô i “ j & e #Ei e1 .

Moreover, if E1 and E2 have polarities (i.e. are esp), then E1 ∥ E2 also has polarities,
defined as polE1 ∥E2 p1, eq “ polE1 peq and polE1 ∥E2 p2, eq “ polE2 peq.
By extension, we often write X ∥ Y for the tagged disjoint union pt1u ˆ Xq Z pt2u ˆ Y q
of two sets X and Y . In the simple parallel composition of arenas A and B, the two are
side by side with no interaction. The arena A ∥ B adequately represents a tensor type
A b B where the two resources A and B may be accessed in any order – although PCF does
not have such a type, this construction will play an important role in the sequel. We also
introduce the product A1 & A2 of A1 and A2 ´-arenas, defined as for A1 ∥ A2 with conflict
pi, eq #A1 &A2 pj, e1 q ô i ‰ j _ pi “ j ^ e #Ai e1 q ,
i.e. A1 and A2 are in conflict. The constructions ∥ and & have obvious n-ary generalizations.
We also introduce another construction on arenas, the affine arrow A ⊸ B:
Definition 2.4. Let A, B be arenas with B pointed, i.e. with exactly one minimal b0 P |B|.
The affine arrow A ⊸ B has the components of AK ∥ B except for causality, set as:
ďA⊸B “ ďAK ∥B Y tpp2, b0 q, p1, aqq | a P |A|u .
This completes an interpretation of PCF types as pointed ´-arenas capturing the causal
dependency between computational events in an affine evaluation. For instance, on A Ñ B
computation starts in B, but as soon as the initial move of B has been played computation
in A may start, with polarity reversed. At this point, the reader may verify that indeed, the
arena pU ⊸ Uq ⊸ B obtained by applying these constructions is indeed the one in Figure 3.
2.1.3. General arrow. Definition 2.4 suffices for the types of PCF (which yield pointed arenas).
But we aim to show that strategies have the structure of a Seely category, a traditional
categorical model for Intuitionistic Linear Logic – and that structure includes tensors, which
do not preserve pointedness. To generalize A ⊸ B for B non-pointed, it is natural to set
one copy of A for each initial move of B. More concretely, A ⊸ B has events and polarities
|A ⊸ B| “ p∥bPminpBq AqK ∥ B ,
where minpBq is the set of minimal events of B. The order has p2, bq ď p2, b1 q iff b ďB b1 ,
p1, pb, aqq ď p1, pb1 , a1 qq iff b “ b1 and a ďA a1 , p2, bq ď p1, pb1 , aqq iff b “ b1 , and p1, pb, aqq ď
p2, b1 q never, exactly matching the arrow arena of HO games [HO00]. But having two copies
of A is in tension with affineness, so we use conflict to tame this copying. The construction
is illustrated in Figure 4, displaying the arena U ⊸ pU b Uq. There are two copies of the U
on the left, but still, linearity is guaranteed by the addition of conflict.
To define conflict, writing χA,B : |A ⊸ B| Ñ |AK ∥ B| for the obvious map, we use:

## PDF page 11

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:11

Lemma 2.5. Consider A and B two ´-arenas.
Then, there is a unique #A⊸B making A ⊸ B a ´-arena such that for all down-closed
finite x Ď |A ⊸ B|, x P C pA ⊸ Bq iff χA,B x P C pAK ∥ Bq with χA,B injective on x.
Proof. See Appendix B.1.1.

2.1.4. Playing on Arenas. Now we formulate a notion of execution, relying on the fact that
event structures support a natural notion of state or position, called configuration.
Definition 2.6. A (finite) configuration of es E is a finite set x Ď |E| which is
down-closed : @e P x, @e1 P |E|, e1 ďE e ùñ e1 P x
consistent:
@e, e1 P x, ␣pe #E e1 q .
We write C pEq for the set of finite configurations on E.
For x, y P C pEq, we write x ´Ă y if there is e P |E| such that e R x and y “ x Y teu;
´Ă is the covering relation. If x ´Ă x Y teu, we say that x enables e or extends by e,
written x $E e. Configurations of an arena represent valid execution states. We may now
leverage this to define plays, which provide a mathematical notion of execution.
Definition 2.7. An alternating play on arena A is a sequence s “ s1 . . . sn which is:
valid :
non-repetitive:
alternating:
negative:

@1 ď i ď n, ts1 , . . . , si u P C pAq ,
@1 ď i, j ď n, si “ sj ùñ i “ j ,
@1 ď i ď n ´ 1, polA psi q ‰ polA psi`1 q ,
if n ě 1, then polA ps1 q “ ´.

We write Œ-PlayspAq for the set of alternating plays on A.
The notation Œ-PlayspAq means to suggest that an alternating play has two possible
states: O if s has even length and the last move (if any) is by Player, and P otherwise:
each new move transitions between them. We denote the empty play with ε, and the prefix
ordering with Ď. In the sequel we sometimes apply Œ-Playsp´q to esps other than arenas.
Plays record individual executions, by giving a chronological account of events observed
throughout computation. For instance, Figure 5 displays a play on the arena pU ⊸ Uq ⊸ B
of Figure 3. It is also read from top to bottom. Each move corresponds to a node in Figure
3 – as each move in the arena corresponds to a given type component, the identity of each
move in Figure 5 is signified by its position under the matching type component.
2.1.5. Strategies. Given a term of type A we may, given the adequate technical machinery,
ask whether a given play describes a valid execution for that term. The play of Figure 5, for
instance, describes a valid execution for λf UÑU . f skip; tt : pU Ñ Uq Ñ B: after Opponent
starts computation, reduction immediately gets stuck with a variable f in head position.
This is an observable event, corresponding to Player calling its argument with q` . Then,
Opponent proceeds to call his argument with q´ , triggering the evaluation of the subterm
skip. This (trivially) converges to a value, which is observable and corresponds to ✓` . The
control goes back to f (Opponent), which evaluates to skip as well via observable ✓´ . This
triggers the evaluation of tt, leading to the observable tt` that terminates computation.
Figure 5 represents one possible execution of λf UÑU . f skip; tt : pU Ñ Uq Ñ B. In
general a term is represented by a strategy, which aggregates all possible executions.

## PDF page 12

24:12

Vol. 20:3

S. Castellan and P. Clairambault

q´
q`
0

Figure 10: pU Ñ Uq Ñ B with replication

q´
0,0

q´
0,1

✓`
0,0

✓`
0,1

q`
1

tt`
✓´
0

q´
1,0

q´
1,1

✓`
1,0

✓`
1,1

✓´
1

Figure 11: Configuration of !p!U ⊸ Uq ⊸ B

Definition 2.8. A alternating strategy σ : A on ´-arena A is σ Ď Œ-PlayspAq which is:
non-empty:
prefix-closed :
deterministic:
receptive:

εPσ
@s Ď s1 P σ, s P σ
`
@sa`
1 , sa2 P σ, a1 “ a2
@s P σ, sa´ P Œ-PlayspAq ùñ sa P σ

An alternating prestrategy σ : A satisfies all these conditions except for receptive.
In this definition we have started using a convention followed throughout this paper:
when introducing an event, we sometimes annotate it with a superscript to indicate its
polarity. For instance, “@sa`
1 P σ, . . . is shorthand for @sa1 P σ s.t. polpa1 q “ `, . . . ”.
We will see later on how to compute the strategy for a term. It is a strength of game
semantics that this may be done either compositionally by induction on the syntax following
the methodology of denotational semantics, or operationally via an abstract machine [GT12].
2.2. Replication and symmetry. In this paper we introduce early on the machinery for
replication. It requires a small jump in abstraction, but fixes the arenas once and for all.
2.2.1. Arenas with symmetry. Figure 3 displays the arena corresponding to affine executions5
on type pU Ñ Uq Ñ B. To go beyond affineness, we expand the arena to allow multiple calls
to arguments – for pU Ñ Uq Ñ B, we obtain an infinite arena as drawn in Figure 10.
In the picture, it seems like e.g. all moves q` are interchangeable. This is true in spirit
but every move must be a distinct event of the arena. Concretely, the expanded arena is
computed following the methodology of linear logic: the type pU Ñ Uq Ñ B is represented
by !p!U ⊸ Uq ⊸ B rather than pU ⊸ Uq ⊸ B. Here, ! is an exponential modality in the
sense of linear logic. The full definition of !A will appear in Definition 2.10, but its events
are |!A| “ N ˆ |A|, pairs pn, aq where n is called a copy index. So in reality, a precise picture
of the arena for pU Ñ Uq Ñ B with replication would be a version of Figure 10 where
some events are tagged by copy index – see Figure 11 for an example of a configuration of
!p!U ⊸ Uq ⊸ B with explicit indices pictured as grey subscripts.
Expanding the arena so opens up the way to replication without compromising the
non-repetitive condition: a strategy may replay the “same” move but with different copy
indices. But then, it is necessary to identify strategies behaving in the same way save for
5Affineness is enforced by non-repetitive in Definition 2.7. Rather than expand arenas, it is tempting to
simply lift it. For this to be sound, it becomes then necessary to include additional structure in plays: the
justification pointers. This is the choice made in HO games [HO00]. This will be detailed in Section 2.4.

## PDF page 13

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:13

the choice of copy indices. To that end, following the approach initiated in [CCW14] we
enrich arenas with a notion of symmetry, capturing reindexings between configurations.
Definition 2.9. An isomorphism family on event structure E is a set S pEq of bijections
between configurations of E, satisfying the additional conditions:
groupoid: S pEq contains identity bijections; is closed under composition and inverse.
restriction: for all θ : x » y P S pEq and x Ě x1 P C pEq,
there is a (necessarily) unique θ Ě θ1 P S pEq such that θ1 : x1 » y 1 .
extension: for all θ : x » y P S pEq, x Ď x1 P C pEq,
there is a (not necessarily unique) θ Ď θ1 P S pEq such that θ1 : x1 » y 1 .
Then pE, S pEqq is an event structure with symmetry (ess). If A has polarities
preserved by S pAq, A is an event structure with symmetry and polarities (essp).
If A is an ess, we refer to the elements of S pAq as symmetries. We write θ : x –A y to
mean that θ : x » y is a bijection such that θ P S pAq, and write x “ dompθq and y “ codpθq.
It is an easy exercise to prove that symmetries are automatically order-isomorphisms [Win07],
where configurations inherit a partially ordered structure from the causal dependency of
A. We regard isomorphism families as proof-relevant equivalence relations: they convey the
information of which configurations are interchangeable, witnessed by an explicit bijection.
From now on, arenas have an isomorphism family. It comprises only identity symmetries
on basic arenas U, B, N and 1. The previous constructions on arenas extend transparently:
AK has the same symmetries as A. The symmetries on A ∥ B are those of the form
θA ∥ θB : xA ∥ xB – yA ∥ yB
p1, aq ÞÑ p1, θA paqq
p2, bq ÞÑ p2, θB pbqq
for θA : xA –A yA and θB : xB –B yB . Those on A & B are the symmetries on A ∥ B that
are bijections between configurations of A & B, i.e. one of θA and θB must be empty. Note
that these constructions ∥ and & apply to arbitrary event structures with symmetry.
For A ⊸ B, if x, y P C pA ⊸ Bq and θ : x » y is any bijection, defining first χA,B θ as
χ´1
A,B

θ

χA,B

χA,B x » x » y » χA,B y ,
we set θ : x –A⊸B y when θ is an order-isomorphism satisfying χA,B θ : χA,B x –AK ∥B χA,B y.
The main arena construction introducing new symmetric events is the exponential:
Definition 2.10. Let A be a ´-arena. The ´-arena !A has components
events:
|!A| “ N ˆ |A|
causality: pi, aq ď!A pj, a1 q ô i “ j & a ďA a1
conflict: pi, aq #!A pj, a1 q ô i “ j & a #A a1
polarities:
pol!A pi, aq “ polA paq
along with isomorphism family comprising as symmetries those bijections of the form
θ : ∥nPN xn – ∥nPN yn
pn, aq ÞÑ pπpnq, θn aq
for some permutation π P ςpNq and some family pθn qnPN with θn : xn –A yπpnq for all n P N.

## PDF page 14

24:14

Vol. 20:3

S. Castellan and P. Clairambault

This definition applies in general to any ess. Figure 9 shows the plain esp of !U with copy
indices indicated as grey subscripts – its symmetries are all order-isomorphisms between
configurations. While !p´q does not match a type construction of PCF, we shall follow
Girard [Gir87] and define the arrow type of arenas with replication as A Ñ B “ !A ⊸ B.
2.2.2. Symmetry on plays and strategies. Symmetry will allow us to identify strategies, but it
should also affect how strategies play. In the presence of explicit copy indices, a fundamental
property is uniformity. Intuitively, a strategy is uniform if its behaviour does not depend
(up to symmetry) on the specific copy indices used by its environment.
The first step towards uniformity is to transport symmetry to plays.
Definition 2.11. Let A be an arena and s, t P Œ-PlayspAq. We say that s and t are
symmetric, written s –A t, if s and t have the same length, and we have
j
θs,t
“ tpsi , ti q | 1 ď i ď ju : ts1 , . . . , sj u –A tt1 , . . . , tj u

a symmetry in S pAq for all 1 ď j ď n; writing s “ s1 . . . sn and t “ t1 . . . tn .
Those readers familiar with AJM games may find comfort in the following fact.
Fact 2.12. For an arena A, the tuple x|A|, polA , Œ-PlayspAq, –A y is an AJM game [AJM00].
This ignores the Question/Answer labeling in AJM games, which we shall handle later
on. The proof is a straightforward exercise. For the experts, we mention that this association
of arenas to AJM games does not respect the arena constructions because constructions on
AJM games enforce local alternation, while Œ-Playsp´q does not. As in HO games [HO00],
in our presentation local alternation will only follow from the P-visibility condition.
From the connection with AJM games it seems natural to import the AJM uniformity:
Definition 2.13. For A an arena and σ, τ : A alternating prestrategies, we write σ « τ iff:
Ñ-simulation:
Ð-simulation:
Ñ-receptive:
Ð-receptive:

@sa` P σ, t P τ, s –A t ùñ Db` , tb` P τ & sa` –A tb`
@s P σ, tb` P τ, s –A t ùñ Da` , sa` P σ & sa` –A tb`
@sa´ P σ, t P τ, sa´ –A tb´ ùñ tb´ P τ
@s P σ, tb´ P τ, sa´ –A tb´ ùñ sa´ P σ

This defines a per « on prestrategies6 on A. A prestrategy σ : A is uniform iff σ « σ.
Uniformity is crucial. For the interpretation to respect β-equivalence we must identify
strategies that play the “same moves”, but with different copy indices. For instance, we
must consider equal the two strategies τ0 , τ1 : U Ñ U with unique maximal play:
τ0

:

!U
q`
0
✓´
0

⊸

U
q´

✓`

τ1

:

!U
q`
1
✓´
1

⊸

U
q´

✓`

But this quotient is risky. Let us apply both τ0 and τ1 to σ : !U with only maximal
`
play q´
0 ✓0 . Though we have yet to define composition, the application of τ0 to σ must
converge, while that of τ1 to σ must diverge. So τ0 and τ1 cannot be safely identified as
6For strategies, Ñ, Ð-receptive are subsumed by receptive. But these are necessary for uniformity to apply

to prestrategies which might not be receptive – this generalization will be used in the technical development.

## PDF page 15

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:15

`
they are distinguishable. In fact here, the culprit is σ: it is not uniform. Since q´
0 ✓0 P σ,
´ `
uniformity of σ would imply that q1 ✓1 P σ as well, breaking the counter-example.
From now on, all alternating (pre)strategies are assumed uniform.

2.3. Interpretation of PCF. The interpretation follows the methodology of denotational
semantics, resting on the fact that arenas and strategies form a category with adequate
structure. In the main text we only outline this fairly routine construction – though this
should be enough to read the paper – but the construction is detailed in Appendix B.
2.3.1. Category. The category Œ-Strat has objects ´-arenas, and morphisms the alternating
strategies (strategies for short) on A ⊸ B. The composition of σ : A ⊸ B and τ : B ⊸ C
τ dσ :A⊸C
follows the usual game semantics process of parallel interaction followed by hiding.
First, the pre-interactions are sequences u P |pA ⊸ Bq ⊸ C|˚ satisfying valid of
Definition 2.7. A pre-interaction u has three restrictions, with the following types:
u æ A, B P |A ⊸ B|˚ ,

u æ B, C P |B ⊸ C|˚ ,

u æ A, C P |A ⊸ C|˚ ,

defined in the obvious way – see Appendix B.1.2. Given prestrategies σ : A ⊸ B and
τ : B ⊸ C, an interaction u P τ f σ is a pre-interaction u P |pA ⊸ Bq ⊸ C|˚ satisfying:
u æ A, B P σ ,

u æ B, C P τ ,

u æ A, C P Œ-PlayspA ⊸ Cq .

The composition of σ and τ comprises all s P Œ-PlayspA ⊸ Cq with a witness:
τ d σ “ tu æ A, C | u P τ f σu ;
it follows that τ d σ : A ⊸ C is a prestrategy; and a strategy if σ and τ are.
Composition is associative on prestrategies, but admits identities only for strategies: the
copycat strategies. If A is a ´-arena and s P |A ⊸ A|, there are left and right restrictions
s æ l P |A|˚ ,

s æ r P |A|˚ ,

defined in the obvious way (see Appendix B.1.4). For s P Œ-PlayspA ⊸ Aq, s is a copycat play
iff (1) for all even-length prefix s1 Ď s we have s1 æ l “ s1 æ r, and (2) for all p1, pa1 , a2 qq P |s|,
if a2 P minpAq, then a1 “ a2 – a move initial on the left must be justified by the same move
on the right. Writing ccA for the set of all copycat plays, we have ccA : A ⊸ A a strategy as
required. For any strategy σ : A ⊸ B we have ccB d σ d ccA “ σ, making Œ-Strat a category.
Remark 2.14. Our model shares with AJM games [AJM00] the management of the
equivalence « on strategies. All our constructions on strategies must preserve «. For most
of them it is clear, but composition requires some care (see Appendix B.3.1). Operations on
strategies therefore lift transparently to «-equivalence classes, and one can then consider
Œ-Strat to have as morphisms «-equivalence classes of strategies (as is done in [AJM00]).
This is fine, but it does contrast with how we (also following the practice in AJM games)
often refer to specific concrete strategies as being “the interpretation of” specific terms. So
we refrain from quotienting, and consider Œ-Strat as having concrete strategies as morphisms,
and homsets Œ-StratpA, Bq additionally equipped with an equivalence relation « which all
operations preserve. This way the interpretation of terms yields concrete representatives,
but categorical laws only hold up to «. In the sequel we refer only to the plain algebraic
structures (as in “symmetric monoidal closed category”, “cartesian closed category”, etc),

## PDF page 16

24:16

S. Castellan and P. Clairambault

Vol. 20:3

with it being understood that laws for these algebraic structures only hold up to « and that
for any construction we consider, there is a proof obligation that it preserves «.
2.3.2. Further structure. If A and B are ´-arenas, their tensor is simply A b B “ A ∥ B
their parallel composition. For σ1 : A1 ⊸ B1 and σ2 : A2 ⊸ B2 , the strategy
σ1 b σ2 : A1 b A2 ⊸ B1 b B2 ,
defined via adequate restrictions (see Appendix B.2.1), plays as σ1 on A1 , B1 and σ2 on
A2 , B2 – this gives a symmetric monoidal structure, with structural isomorphisms copycat
strategies. Moreover, Œ-Strat is cartesian. Its terminal object is the empty ´-arena 1; the
product of A and B is the A & B. This forms a cartesian product: there are projections
πA : A & B ⊸ A

πB : A & B ⊸ B

acting as copycat, and for σ : C ⊸ A and τ : C ⊸ B, their pairing xσ, τ y : C ⊸ A & B is
defined simply as the as the set-theoretic union of σ and τ (modulo the obvious relabeling).
Finally, for any ´-arenas Γ, A and B, there is an iso Γ b A ⊸ B – Γ ⊸ pA ⊸ Bq, i.e.
a bijection on events preserving and respecting all structure. This yields a bijection
ΛΓ,A,B : Œ-StratpΓ b A, Bq » Œ-StratpΓ, A ⊸ Bq
between the corresponding sets of strategies. Exploiting this, we define the evaluation
evA,B “ Λ´1
A⊸B,A,B pccA⊸B q : pA ⊸ Bq b A ⊸ B ,
and the universal property for monoidal closure is then a direct verification. We conclude:
Proposition 2.15. The category Œ-Strat is cartesian and symmetric monoidal closed.

2.3.3. Exponential. On Œ-Strat, ! gives an exponential in the sense of Linear Logic [Gir87]: a
functor, with natural transformations derA : !A ⊸ A and digA : !A ⊸ !!A making p!, der, digq
a comonad. Moreover, there are natural isomorphisms mon2A,B : !A b !B ⊸ !pA & Bq and
mon0A,B : 1 ⊸ !1, satisfying the coherence laws of a Seely category [Mel09]. So the Kleisli
category Œ-Strat! is cartesian closed, and hence a model of the simply-typed λ-calculus. The
construction is routine, and follows the lines of AJM games [AJM00] – see Appendix B.3.
In the sequel, given a Seely category C and a morphism f P Cp!A, Bq, we shall write
f : P Cp!A, !Bq for its promotion, defined as !f ˝ digA – in particular, recall that Kleisli
composition of f P C! pA, Bq and g P C! pB, Cq may be defined as g ˝! f “ g ˝ f : P C! pA, Cq.
2.3.4. Recursion. Strategies on arena A may be partially ordered by inclusion; this forms a
pointed dcpo. All operations on strategies are continuous with respect to Ď.
Writing Œ-Strat! pA, Bq for the dcpo of strategies on A Ñ B “ !A ⊸ B, the operation
F

: Œ-Strat! p1, pA Ñ Aq Ñ Aq Ñ Œ-Strat! p1, pA Ñ Aq Ñ Aq
σ ÞÑ λf AÑA . f pσ f q

written in λ-calculus syntax following the cartesian closed structure of Œ-Strat! , is continuous.
Its least fixed point YA P Œ-Strat! p1, pA Ñ Aq Ñ Aq is transported to Œ-Strat! pΓ, pA Ñ
Aq Ñ Aq by composition with the terminal projection. For each σ P Œ-Strat! pΓ, A Ñ Aq,
YA σ « σ pYA σq

## PDF page 17

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

seq : !pU & Uq ⊸ U
q´
`
q0
✓´
0
q`
1
✓´
1
✓`
succ : !N ⊸

N
q´

q`
0
n´
0
pn ` 1q`

if : !pB & X & Xq ⊸ X
q´
`
q0
tt´
0
q`
1
v1´
v`
iszero : !N ⊸ B
q´
`
q0
0´
0
tt`

24:17

if : !pB & X & Xq ⊸ X
q´
`
q0
ff ´
0
q`
1
v1´
v`
iszero :

!N

⊸

B
q´

q`
0
pn ` 1q´
0

ff `

Figure 12: Basic strategies for PCF
JM ; N K
Jif M N1 N2 K
Jsucc M K
Jpred M K
Jiszero M K

“
“
“
“
“

seq d! xJM K, JN Ky
if d! xJM K, JN1 K, JN2 Ky
succ d! JM K
pred d! JM K
iszero d! JM K

pred : !N ⊸ N
q´

!N

q`
0

q`
0

0´
0

pn ` 1q´
0

⊸ N
q´

0`

Jlet x “ N in M K “ letX,Y d! xJN K, Λ! pJM Kqy
Figure 13: Interpretation of basic combinators

pred :

n`

Figure 14: Strategy for pred

so a fixed point operator up to «, as needed to interpret recursion.
It is a curiosity already in AJM games [AJM00] that the recursive equation for the
fixpoint combinator must be solved in the domain of concrete strategies, rather than «equivalence classes. To the best of our knowledge it is not known if the partial order induced
by inclusion on «-equivalence classes of strategies has the adequate completeness properties
to solve this, i.e. if the quotient of Œ-Strat and Œ-Strat! by « are dcpo-enriched categories.
2.3.5. Interpretation. Types of PCF are interpreted as ´-arenas: we set JUK “ U, JBK “ B,
JNK “ N and JA Ñ BK “ !JAK ⊸ JBK yielding˘for any type A an arena JAK. A context
Γ “ x1 : A1 , . . . , xn : An is interpreted as JΓK “ 1ďiďn JAi K. A term Γ $ M : A yields
JM K P Œ-Strat! pJΓK, JAKq .

We skip the details of the interpretation of the λ-calculus combinators, which follows the
standard interpretation of the simply-typed λ-calculus in a cartesian closed category [LS88].
We specify strategies for PCF combinators. For constants, JskipK : U, JttK : B, Jff K : B
and JnK : N are the corresponding obvious strategies replying immediately the corresponding
value. For the others the interpretation is in Figure 13, annotating strategy operations with
! to emphasize that they are in the Kleisli category Œ-Strat! . The strategies used are in
Figures 12, 14 and 15. Save for let, the diagram displays exhaustively their maximal plays,
defining them completely. For let, the strategy implements a memoization mechanism: it

## PDF page 18

24:18

!pX &

Vol. 20:3

S. Castellan and P. Clairambault

pX

q`
0
v0´

Ñ Yqq ⊸ Y
q´

q`
1
q´
1,i1
`
v1,i
1
.. .. ..
q´
1,in
`
v1,i
n

pU

Ñ

Uq

Ñ

Figure 15: Typical play of let

Uq

Ñ

B
q´

q`
0
q´
0,0

✓`
0,0

✓`
0,0

q´
0,1

q´
0,1
⇝

✓´
0
q`
1

w`

Ñ

q`
0
q´
0,0

✓`
0,1

w1´

pU

B
q´

✓`
0,1
✓´
0
q`
1

q´
1,0

q´
1,0

✓`
1,0
q´
1,1
✓`
1,1

✓`
1,0
q´
1,1
✓`
1,1
✓´
1

tt`

✓´
1

tt`

Figure 16: Pointer annotations on plays

evaluates on X obtaining a value v, which is then fed to the function argument each call,
without re-evaluating it. The play shown for let is not maximal as Opponent could play
some q´
1,in`1 after. We will see in Section 3.2 that it is fully informative: there is only one
innocent strategy that includes these plays. Finally, the interpretation of recursion is set
with JYA M K “ YA d! JM K, completing the definition.
This interpretation satisfies the main property expected of a denotational semantics:
Proposition 2.16 (Adequacy). For any $ M : U, M ó if and only if JM K ó.

Note there are only two strategies on U: the minimal tε, q´ u matching any diverging
program, and the converging tε, q´ , q´ ✓` u. For σ : U, we write σ ó if σ converges and σ ò
if σ diverges. We omit the proof which is standard using logical relations, see e.g. [HO00].
This immediately entails soundness for observational equivalence:
Corollary 2.17. Let Γ $ M, N : A be any terms of PCF. If JM K « JN K, then M „ N .

Proof. Assume JM K « JN K, and consider a context Cr´s such that CrM s ó. By Proposition
2.16, JCrM sK ó. But JCrM sK “ JCr´sK d! JM K « JCr´sK d! JN K “ JCrN sK, so CrN s ó by
Proposition 2.16. The other direction also holds, hence M „ N .
Computational adequacy is the standard to express that a model accurately describes
computation in the language. In fact in game semantics the connection with operational
semantics is much stronger, as highlighted earlier. We will elaborate on that in Section 3.
2.4. HO games. Before exploring this computational content, we highlight the connection
with HO games [HO00], based on representing plays up to symmetry as plays with pointers.
2.4.1. Plays with pointers. First, a convention. For A a ´-arena and s P Œ-PlayspAq, then
|s| P C pAq has two order structures: it is totally ordered chronologically as prescribed by
s, and has a partial order imported from ďA . When representing plays, we often annotate
them with the immediate causal dependency generating ďA . For instance, Figure 16 shows it
for s P Œ-PlayspJpU Ñ Uq Ñ BKq with |s| displayed in Figure 11. The dashed lines represent
immediate causal dependency in ďA , omitted when it coincides with juxtaposition. We call

## PDF page 19

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:19

these dashed lines pointers, going upwards from one event to its predecessor in A. As arenas
are forestial, any move has at most one pointer and only minimal events have none.
It is worth, just this once, being extremely pedantic about the representation used in
Figure 16 and others. Recall that JpU Ñ Uq Ñ BK “ !p!U ⊸ Uq ⊸ B. Accordingly,
|JpU Ñ Uq Ñ BK| “ N ˆ pN ˆ |U| ` |U|q ` |B|
with ` the tagged disjoint union A ` B “ t1u ˆ A Y t2u ˆ B, previously also written ∥. So
an event of JpU Ñ Uq Ñ BK carries a move from U or B, tags originating from the disjoint
unions and indicating one type component, and natural numbers, the copy indices. In Figure
16 the information of the moves is conveyed by the label, i.e. q´ , ✓` , etc. The tag is
conveyed by the position of the move under the corresponding type component. Finally, the
copy indices are given as a sequence in grey, with the leftmost integer corresponding to the
´
outermost !. For instance, the move q´
0,1 really stands for p1, p0, p1, p1, q qqqq.
It is often convenient to display pointers, but they are not part of the structure of plays.
If they are imported into plays, then copy indices become essentially disposable (up to –).
To make this formal, we start by defining a notion of plays with pointers on a ´-arena.
Definition 2.18. An alternating play with pointers on A is s1 . . . sn P |A|˚ which is:
alternating: @1 ď i ď n ´ 1, polA psi q ‰ polA psi`1 q ,
together with, for all 1 ď j ď n s.t. sj is non-minimal in A, the data of a pointer to some
earlier si s.t. si _A sj . We write P-Œ-PlayspAq for the set of plays with pointers on A.
The non-repetitive condition of Definition 2.7 would make pointers redundant as each
move has a unique predecessor, and the existence of pointers would boil down to the fact that
plays reach only down-closed sets of events. It is a useful exercise to show that non-repetitive
plays with pointers are in bijection with alternating plays, on arenas without conflict.
Reciprocally, since repetitions are now allowed, we may use them to represent executions
with replication even without the expansion process of Section 2.2.
2.4.2. Meager and concrete arenas. Definition 2.18 applies to arenas in the sense of Section 2.2.1, but it ignores part of their structure: it takes no account of conflict, and symmetry.
Indeed, plays with pointers originate from HO games, where arenas are much simpler:
Definition 2.19. A meager arena is a partial order with polarities pA, ďA , polA q s.t.:
alternating: if a1 _A a2 , polA pa1 q ‰ polA pa2 q,
forestial: if a1 ďA a and a2 ďA a, then a1 ďA a2 or a2 ďA a1 ,
without conflict or symmetry. A meager ´-arena additionally satisfies:
negative: if a P minpAq, then polA paq “ ´.
Clearly, Definition 2.18 applies to meager arenas. Each PCF type A may be interpreted
as a meager arena rAs, setting rUs “ U, rBs “ B, rNs “ N and rA Ñ Bs “ rAs ⊸ rBs; i.e.
as for J´K but without the ! – this is exactly the interpretation in [HO00]. The arena JAK is
then an expansion of rAs – the notion of concrete arena makes this explicit:
Definition 2.20. A concrete arena is pA, A0 , lblq with A an arena, A0 a meager arena,
lbl : |A| Ñ |A0 | ,

## PDF page 20

24:20

S. Castellan and P. Clairambault

Vol. 20:3

a labelling function, together satisfying the following additional requirements:
locally pointed: for all x P C pAq, x has at most one minimal event of each polarity,
rigid: lbl preserves minimality, and preserves immediate causality _,
transparent: for any x, y P C pAq and bijection θ : x » y,
then θ P S pAq iff θ is an order-iso preserving lbl.
We shall update this in Section 7.3.1, when further structure becomes required. Locally
pointed is phrased so as to allow non-negative arenas of the form AK ∥ B. In most cases, for
negative arenas, configurations x P C pAq will have at most one minimal event.
Every basic arena X may be regarded as the concrete arena pX, X, lblX q with lblX
the identity function. Concrete arenas support the arena constructions & and Ñ with
pA & Bq0 “ A0 b B 0 , and pA Ñ Bq0 “ A0 ⊸ B 0 . By induction, for every type A this gives
us pJAK, rAs, lblA q, a pointed concrete ´-arena with lblA simply forgetting all copy indices.
Remark 2.21. Transparent makes explicit the nature of symmetries on arenas arising from
types: as they leave all components unchanged except copy indices, they are exactly all
reindexings. This does not always hold outside the types considered here. In particular,
concrete arenas do not support b: of course condition locally pointed fails, but more
fundamentally, valid symmetries in !pA b Bq must send pi, p1, aqq and pi, p2, bqq to the same
copy index j, a non-local constraint, not reflected by condition transparent. This is why we
do not consider all arenas to be concrete: they fail to cover the full Seely category structure.
In the sequel, we only assume arenas to be concrete when it is explicitly mentioned.
2.4.3. Pointers and symmetry. Plays with pointers represent plays up to symmetry:
Proposition 2.22. Consider A a concrete arena. Then, there is a function
P : Œ-PlayspAq{–

Ñ

P-Œ-PlayspA0 q ,

injective and preserving length and prefix.
Proof. For s P Œ-PlayspAq, we first construct sÑ P P-Œ-PlayspAq by importing _A . Then,
Ppsq is obtained by applying lblA pointwise. That pointers on Ppsq are well-formed (i.e.
that if sj points to si , then si _A0 sj ) follows from lbl preserving minimality and the
immediate causal order. That P is invariant under – boils down to transparent. By
construction, P preserves length and prefix. For injectivity, take s, s1 P Œ-PlayspAq such
that Ppsq “ Pps1 q. Since P is length-preserving, s and s1 have the same length n. Consider
θ “ tpsi , s1i q | 1 ď i ď nu : |s| » |s1 |
the induced bijection. Since Ppsq “ Pps1 q, in particular s and s1 have the same pointers, so
θ is an order-isomorphism, and moreover since Ppsq “ Pps1 q again we also have lblA psi q =
lblA ps1i q for all 1 ď i ď n. Hence, θ is a symmetry, so by transparent, s – s1 as required.
However, P is not surjective. Writing A “ U Ñ B, the play s P P-Œ-PlaysprAsq set as
U
q`
✓´
✓

Ñ

B
q´
tt`

´

ff `

## PDF page 21

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:21

is not the image of any play in Œ-PlayspJAKq, for two reasons: (1) not every move is
duplicated in JAK, e.g. there there is only one copy of ✓´ for every copy of q` – this linearity
discipline is enforced by non-repetitive, which is absent in P-Œ-PlaysprAsq; and (2) likewise,
rAs and P-Œ-PlaysprAsq do not account for conflict between tt` and ff ` in JAK.
2.4.4. HO strategies. This extends to strategies. For concrete arena A and σ : A, then
Ppσq “ tPpsq | s P σu is essentially a strategy on A0 in the Hyland-Ong sense, i.e. a
prefix-closed, deterministic set of plays with pointers. We have:
Proposition 2.23. Consider A a concrete arena, and prestrategies σ, τ : JAK.
Then, σ « τ iff Ppσq “ Ppτ q.
Proof. If. Consider σ, τ : A s.t. Ppσq “ Ppτ q. For σ « τ we first check Ñ-simulation.
Consider sa` P σ, t P τ s.t. s –A t. But Ppsaq P Ppτ q, so there is t1 b1 P τ s.t. Ppt1 b1 q “
Ppsaq. Hence by Proposition 2.22, sa –A t1 b1 . So t, t1 P τ and t –A t1 , with t1 b1 P τ . By
uniformity of τ , tb P τ for some b with t1 b1 –A tb, so tb –A sa as well. The condition
Ð-simulation is symmetric. For Ñ-receptive, assume sa´ P σ, t P τ and sa´ –A tb´ . Since
Ppsa´ q P τ , there is t1 b1 P τ s.t. Ppsaq “ Ppt1 b1 q, i.e. sa –A tb. But then t1 b1 P τ and
t1 b1 –A tb, so by uniformity of τ we have tb P τ . Finally, Ð-receptive is symmetric.
Only if. Consider σ, σ 1 : A s.t. σ « σ 1 , and take Ppsq P Ppσq for some s P σ. By
induction on s, we build some s1 P σ 1 s.t. s –A s1 : for positive extensions this follows from
σ « σ 1 ; for negative extensions from the extension condition on isomorphism families and the
Ñ-receptive condition on uniformity. But then by Proposition 2.22 we have Ppsq “ Pps1 q,
so Ppσq Ď Ppσ 1 q. The argument is symmetric, so Ppσq “ Ppσ 1 q as desired.
Plays with pointers permit a presentation of strategies up to «, avoiding copy indices.
They provide the foundation for HO games [HO00], where the interpretation of types is
essentially r´s (without conflict), and plays carry pointers. We include the classical example
showing that though one may choose copy indices or pointers, one cannot avoid both.
Example 2.24. The Kierstead terms $ Kx , Ky : ppB Ñ Bq Ñ Bq Ñ B are defined as
Kx “ λF pBÑBqÑB . F pλx. F pλy. xqq ,

Ky “ λF pBÑBqÑB . F pλx. F pλy. yqq .

Their respective interpretations in Œ-Strat! have distinctive plays:
Kx

:

ppB Ñ Bq
q´
0,i
q`
0,i,j

q´
i`1,j

Ñ

Bq Ñ B´
q
q`
0

Ky

:

ppB

Ñ

Bq

Ñ

q´
0,i

q`
i`1
q`
i`1,j,0

q´
i`1,j

Bq Ñ B
q´
q`
0
q`
i`1

Here pointers are redundant, and computed from the identity of moves. In particular, in
both plays the q` “points to” the unique q´ with compatible copy indices. Mapping these
through P, we get two plays with pointers that only differ through their pointers. In HO
games, the Kierstead terms are only distinguished by pointers7. It is crucial to keep them
separate: it is a surprisingly challenging exercise to find a PCF context that separates them.
7It is necessary to go up to third-order types to find such examples. Pointers are redundant up to

second-order types, which is the starting point of algorithmic game semantics [GM03].

## PDF page 22

24:22

S. Castellan and P. Clairambault

pB

Ñ

B

Ñ

Uq

Ñ

B
q´

q`
q´
q`
q´
ff `
✓´
tt`
q´
ff `
✓´
tt`

Vol. 20:3

λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt
λf BÑBÑU . f ppf ff ff q; ttq ff ; tt

Figure 17: Illustration of the operational contents of game semantics
Plays with pointers are powerful, and indeed the game semantics literature is strongly
biaised towards HO games (as opposed to AJM games). This, however, has two costs.
Firstly, plays with pointers are not a natural inductive structure, making their manipulation
sometimes inelegant or unwieldy (so-called “pointer surgery”). Proposals have been made for
clean formalizations, e.g. through nominal sets [GG12]. Another cost is that replication is
so hard-wired into the model that it does not enjoy a clean linear decomposition. Enforcing
linearity is slightly awkward and relies on additional structure [McC98].
In this work we stick with Œ-Strat rather than adopting plays with explicit pointers.
Among other things this will ease the relationship with the forthcoming thin concurrent
games, which we do not know how to formulate with pointers in general. Besides, in Œ-Strat,
pointers can be directly obtained from the arena, and as such may be used as in HO games8.
In fact, pointers play a central role in this paper. From now on, all representations of plays
will display pointers. In contrast, we will often omit copy indices as most of the time they
convey no useful information; one can regard this convention as drawing Ppsq rather than s.
3. Sequential Computational Effects in Game Semantics
We now explore the model constructed above, introducing the traditional “semantic cube”.
The plays of a term are computed denotationally, by induction on syntax. However, given
a term, an experienced game semanticist will be able to directly list its plays, without going
through the intricate definition of the interpretation. This is because as discussed before,
plays represent the operational behaviour of the term: rather than denotationally, they
can be obtained directly from the term by operational means [DHR96, Jab15, GT12, LS14].
This is illustrated in Figure 17. Opponent moves trigger the evaluation of a subterm, which
appears boxed. The following Player move then corresponds to the head (i.e. leftmost)
8Another work blurring the lines between HO and AJM is [AJ09] where AJM games are equipped with a
function able to rebuild pointers without the need to explicitly integrate them in plays. All the data of a
game in the sense of [AJ09] can be computed from an arena in our sense, but our arenas are more primitive.

## PDF page 23

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:23

variable occurrence (or constant) of the subterm being evaluated. The pointers from Player
moves correspond to the stage where the variable in head position was abstracted, or to
the function call being returned by the value in head position. More specifically, Figure 17
represents the interaction of the term under study with the applicative context:
Crs “ rs pλxB . λy B . if x pif y skip skipq skipq
Figure 17 is strongly inspired by the Pointer Abstract Machine (PAM) [DHR96].
3.1. Well-Bracketing. Now that executions as plays are first-class citizens, independent of
programs, we may start classifying them according to the computational capabilities that
they witness. For instance, is the following play a possible execution of a term?
pU

Ñ

Uq

Ñ

B
q´

q`
q´
tt`

λf UÑU . f M
λf UÑU . f M
λf UÑU . f M
λf UÑU . tt

We argue informally why this cannot be an execution in PCF. The first action of the
term is to ask its argument, so it has the form λf UÑU . f M ; we annotate the figure with
the corresponding operational state as in Figure 17. In the last line, tt at toplevel indicates
the overall computation has terminated to tt. This is confusing, since operationally the
Opponent move in the third line corresponded to triggering the evaluation of the argument
of f . How can evaluating the argument of f cause the whole computation to terminate?
Nevertheless, this play is indeed a realistic execution, for the term
λf UÑU . callcc pλk BÑU . f pk ttq; Kq : pU Ñ Uq Ñ B
where callcc is the call-with-current-continuation primitive originating in Scheme, and
which famously may be typed with Peirce’s law [Gri90]. The precise operational semantics
of callcc will not be useful for this paper, but informally callcc M immediately calls M ,
feeding it a special function k, the “continuation”. When the continuation is called with
value v, callcc interrupts M and returns v at toplevel, breaking the call stack discipline.
Can the play above be realised without callcc (or some other control operator, as such
primitives are called)? We can show that the answer is no, by capturing plays that “respect
the call stack discipline”, and refining the whole interpretation to show that this invariant is
preserved. This is the goal of the notion of well-bracketing. First we enrich arenas:
Definition 3.1. A Question/Answer labeling on arena A is a function
λA : |A| Ñ tQ, Au
invariant under symmetry (if θ : x –A y, then for all a P x, λA paq “ λA pθpaqq) and satisfying:
question-opening: if a P |A| is minimal, then λA paq “ Q,
answer-closing:
if λA paq “ A, then a is maximal for ďA ,
answer-linear:
if λA pa1 q “ λA pa2 q “ A with a _A a1 , a2 , then a1 “ a2 or a1 #A a2 .

From now on, arenas have a Question/Answer labeling. Questions intuitively correspond
to variable calls, while Answers correspond to returns. Basic arenas are enriched as
shown in Figure 18. For other constructions the labeling is inherited transparently, with
λ!A pi, aq “ λA paq, λA1 bA2 pi, aq “ λAi paq, λA⊸B p2, bq “ λB pbq, and λA⊸B p1, pb, aqq “ λA paq.

## PDF page 24

24:24

Vol. 20:3

S. Castellan and P. Clairambault

q´,Q

q´,Q
✓`,A

q´,Q
ff `,A

tt`,A

0`,A

1`,A

2`,A

...

Figure 18: Question/Answer labeling on basic arenas
If s P Œ-PlayspAq and si is an answer, it cannot be minimal in A by question-opening.
Its antecedent in A – its justifier – must appear in s as some sj with j ă i, and is a question
by answer-closing. We say that si answers sj . If a question in s has an answer in s we say
it is answered in s. The last unanswered question of s, if any, is the pending question.
We now capture executions respecting the call stack discipline as well-bracketed plays.
Definition 3.2. Let s P Œ-PlayspAq be an alternating play.
It is well-bracketed if for all prefix taA Ď s, a answers the pending question of t.
All plays encountered in the paper until now are well-bracketed, with the exception of
the example at the beginning of Section 3.1. We can then define well-bracketed strategies:
Definition 3.3. Let σ : A be a strategy on A.
It is well-bracketed iff for all sa` P σ, if s is well-bracketed then sa is well-bracketed.
In other words, a well-bracketed strategy is never the first to break the call stack
discipline. Asking all plays to be well-bracketed is too strict, as illustrated by the play
pU

⊸

Uq

⊸

pU

⊸

Uq
q´,Q

q`,Q
q´,Q
q`,Q
✓

´,A

✓`,A
of copycat: the last move does not answer the pending question, but because Opponent
broke the normal control flow first. There is a lluf subcategory Œ-Stratwb of Œ-Strat, having
well-bracketed strategies as morphisms. The interpretation of PCF in Œ-Strat! in fact yields
only well-bracketed strategies, i.e. has target Œ-Stratwb
! . This shows that indeed, the
execution at the beginning of Section 3.1 cannot be realised in PCF.
3.2. Visibility and Innocence. Likewise, is this play a possible execution of a term?
pB

Ñ

Uq
q`

q´
ff `
q´
tt`

Ñ

U
q´

λf BÑU . f M
λf BÑU . f M
λf BÑU . f M
λf BÑU . f ff
λf BÑU . f M
λf BÑU . f tt

Again, this seems unfeasible in PCF. Again, on the right hand side we show, assuming
a term realising this play, its corresponding operational states. At the third and fifth moves,
the same subterm is being evaluated; yet we get two distinct answers. In an extension

## PDF page 25

Vol. 20:3

pB

q´
ff `
q´
tt`

Ñ

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

Uq Ñ U
q´
`
q

pU
λf BÑU . f plet x “!r in r :“ 1; px ą 0qq
λf BÑU . f plet x “!r in r :“ 1; px ą 0qq
λf BÑU . f plet x “!r in r :“ 1; px ą 0qq
λf BÑU . f ff
λf BÑU . f plet x “!r in r :“ 1; px ą 0qq
λf BÑU . f tt

Figure 19: A strategy with references

r ÞÑ 0
r ÞÑ 0
r ÞÑ 0
r ÞÑ 1
r ÞÑ 1
r ÞÑ 1

Ñ

Uq

Ñ

24:25

U
q´

q`
q´
q`
q´
✓`

Figure 20: Non P-visible play

of PCF with a primitive ` for non-deterministic choice, this play would be realisable by
λf BÑU . f ptt ` ff q. But does it make computational sense in a deterministic language?
Once more, the answer is yes: the play above describes a valid execution of the term
λf BÑU . newref r in f plet x “!r in r :“ 1; px ą 0qq : pB Ñ Uq Ñ U
in PCF extended with references: newref r in M allocates a reference r initialized to 0. We
show in Figure 19 an operational description as to how this term indeed realises this play.
Again, this cannot be realised in PCF. To show this, we give a version of innocence
[HO00], formalizing that without state, evaluating the same subterm yields the same response.
The first step is a mathematical way to state that two plays “correspond to the same subterm”,
like the two prefixes of the play of Figure 19 terminating with a q´ on the left.
The operation computing (a mathematical notion of) “current subterm” is the P-view :
Definition 3.4. Let s P Œ-PlayspAq. Its P-view is the subsequence defined by induction:
xεy
xsa` y
1 ´
xsa`
1 s a2 y
` 1 ´
xsa1 s a2 y

“
“
“
“

ε
xsya`
´
´
xsya`
if a`
1 a2
1 _A a2
´
a2
if a2 is negative minimal in A

We take the immediate prefix for P -ending plays and follow the pointer for O-ending
plays. For instance, the prefixes of length 3 and 5 of the play on Figure 19 have the same
P-view, capturing that they correspond to the same subterm. This is a powerful definition –
really, the distinguishing feature of HO games [HO00] – and it often takes newcomers a while
to digest. Interestingly, our forthcoming parallel innocence will be phrased quite differently.
But this is not yet conclusive: if s P Œ-PlayspAq, it might be that xsy R Œ-PlayspAq.
For instance, in Figure 20 we gray out moves not selected in computing the P-view of
s P Œ-PlayspAq for A “ JpU Ñ Uq Ñ UK. The subsequence of xsy in black is an alternating
sequence of |A|, but fails valid of Definition 2.7. Indeed, the “justifier” of ✓` , its immediate
dependency in A, is not selected – thus |xsy| is not down-closed. Accordingly, we say:
Definition 3.5. A play P Œ-PlayspAq is P-visible if for all prefix @t Ď s, xty P Œ-PlayspAq.
Likewise, a strategy σ : A is P-visible iff all its plays are P-visible.
So, “computing P-views never drops pointers”, or “Player always points in the P-view”.
On P-visible s P Œ-PlayspAq, the P-view always yields a well-formed (P-visible) play.
We now define innocent strategies as those that behave the same in any situation where
the same subterm is being evaluated, i.e. whose behaviour only depends on the P-view :

## PDF page 26

24:26

S. Castellan and P. Clairambault

Vol. 20:3

Definition 3.6. A P -visible alternating strategy σ : A is innocent if it satisfies:
innocence: for all sa` P σ, for all t P σ, if xsy “ xty then ta` P σ.
That ta` P Œ-PlayspAq is well-formed relies on xsy “ xty, so that the causal dependencies
of a in A appear in t9. All structural morphisms of Œ-Strat are innocent. Innocent
strategies compose – though this is infamously tricky to prove, prompting a significant line
of work investigating the structures arising from the composition of innocent strategies
[Cur98, HHM07, CD15]. We do not review here the proof of stability under composition.
The interpretation of PCF yields only innocent strategies, i.e. targets the cartesian closed
lluf subcategory Œ-Stratinn
of innocent strategies. Hence, the play at the beginning of Figure
!
3.2 cannot be realised in PCF. We also get a cartesian closed lluf subcategory Œ-Stratwb,inn
!
with well-bracketing. Finally, the weaker P-visibility is also preserved under the categorical
wb,vis
operations, forming lluf sub-cartesian closed categories Œ-Stratvis
.
! and Œ-Strat!
3.3. Full Abstraction for PCF. We have now eliminated all non PCF-definable behaviour.
We review the corresponding definability and intensional full abstraction arguments.
3.3.1. Definability. Call a P-view on arena A any s P Œ-PlayspAq invariant under P-view,
´
i.e. xsy “ s – those are exactly the s P Œ-PlayspAq such that for all ts`
i si`1 Ď s, we have
si _A si`1 , in other words Opponent always points to the previous move. We motivated
P-views as a way to address specific “subterms” of a strategy – it might therefore not be a
surprise that those are the key to reconstruct a term from an innocent strategy. We write
xxσyy “ txsy | s P σu
for the set of P-views of σ. If σ is innocent, then it is simple that xxσyy Ď σ. Moreover, σ can
then be recovered as the set of P-visible s P Œ-PlayspAq such that for all t Ď s, xty P xxσyy.
For σ : A innocent, xxσyy is not a strategy as in general it fails receptivity. It is however
easily verified to be a prestrategy – and in particular uniform. Moreover, we have:
Proposition 3.7. For σ, τ : A innocent strategies on A, we have xxσyy “ xxτ yy iff σ “ τ .
Likewise, xxσyy « xxτ yy if and only if σ « τ .
Proof. We only detail the second statement. Firstly, if σ « τ , it is direct that xxσyy « xxτ yy as
xxσyy Ď σ and xxτ yy Ď τ and the bisimulation game of Definition 2.13 preserves P-views.
If xxσyy « xxτ yy, take sa` P σ, t P τ s.t. s –A t. In particular xsy –A xty and xsya` P xxσyy.
By Ñ-extension, there is b` s.t. xtyb` P xxτ yy, so tb` P τ by innocence. This proves Ñextension, Ð-extension is symmetric and Ñ, Ð-receptivity follow by receptivity of σ, τ .
So innocent strategies have two representations: a full σ : A satisfying Definition 3.6;
or, following Proposition 3.7, the set xxσyy. Anticipating on later developments, we refer to
xxσyy as the causal presentation of σ. In traditional innocent game semantics, the forest of
P-views is called (notably by Curien [Cur06]) the meager representation, while the set of
plays is fat. Here this is misleading, because plays in xxσyy still carry explicit copy indices. In
particular xxσyy has branches matching all copyable Opponent moves, which is “fat”.
To recover the meager representation, we show:
9In traditional Hyland-Ong games based on plays with points, one would conclude the above definition
with something like “. . . then ta P σ, where a has the same pointer as in sa”, which is rarely made very
formal. Here, because pointers are derived the above definition is rigorous and self-contained.

## PDF page 27

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:27

Proposition 3.8. Consider A a concrete arena and σ, τ : A innocent strategies.
If Ppxxσyyq “ Ppxxτ yyq, then σ « τ .
Proof. Let σ, τ : JAK be innocent strategies on A and assume that Ppxxσyyq “ Ppxxτ yyq.
By Proposition 2.23, xxσyy « xxτ yy. Then, by Proposition 3.7, it follows that σ « τ .
This, at last, provides the meager representation.
These representations have distinct advantages: composition is only directly defined on
the fat representation; but it is the meager one that bridges innocent strategies and syntax
and allows definability. An innocent alternating strategy σ : A is finite iff Ppxxσyyq is finite.
Its size is simply the cardinal of that set. Definability simply follows the meager form:
Theorem 3.9. Let A be a PCF type, and σ : JAK be a finite well-bracketed innocent strategy.
Then, there is a PCF term $ M : A s.t. JM K « σ.
Proof. We describe the argument – for more details, the reader is referred to [HO00].
Without loss of generality, A has the form A1 Ñ ¨ ¨ ¨ Ñ An Ñ X where for each 1 ď i ď n,
Ai “ Ai,1 Ñ ¨ ¨ ¨ Ñ Ai,pi Ñ Xi .
We reason on xxσyy, by induction on the size of σ. If σ has no reaction to the (unique)
minimal q´ in X (i.e. σ “ tε, q´ u), any diverging term will do. Otherwise, by determinism
there is exactly one move a` s.t. q´ a` P σ. If a` is an answer v ` on X, then M is the
10
matching constant. Otherwise, a` is the initial q`
i0 in some Ai0 . The situation is drawn as
A1 Ñ . . . Ñ pAi,1 Ñ . . . Ñ Ai,pi Ñ Xi q Ñ . . . Ñ An Ñ X
q´
q`
i0
´
´
´
qi0 ,1
qi0 ,pi
v
0

with, in grey, the possible extended P-views. For each extension there is a residual substrategy.
We extract those – first, if q`
i0 immediately returns. For each value v in Xi , we form
´
xxσv yy “ tq´ s | q´ q`
i0 v s P xσyu ,

a causal innocent strategy on JAK of size strictly lesser than σ. By induction hypothesis there
is $ Mv : A with JMv K « σv . As σ is finite, there are finite many v s.t. σv is non-diverging.
´
Alternatively, for all 1 ď j ď pi0 , we consider P-views q´ q`
i0 qi0 ,j s P xxσyy where as a
´
P-view, s answers neither q`
i0 , nor q by well-bracketing. Such a P-view yields
q´
i0 ,j s P Œ-PlayspJA1 Ñ ¨ ¨ ¨ Ñ An Ñ Ai0 ,j Kq

a P-view where moves in s formerly depending on q´ in JAK are set to depend on q´
i0 ,j .
Considering all such P-views generates a causal innocent strategy of size strictly lesser than σ,
hence by induction hypothesis there is $ Mi0 ,j : A1 Ñ ¨ ¨ ¨ Ñ An Ñ Ai0 ,j s.t. JMi0 ,j K « σi0 ,j .
Finally, with all this data we may form $ M : A as
An
1
λxA
1 . . . xn . case xi0 pMi0 ,1 x1 . . . xn q . . . pMi0 ,pi0 x1 . . . xn q of
v1 ÞÑ Mv1
...
vp ÞÑ Mvp

where p is such that every σvi with i ą p is diverging. We get, as needed JM K « σ.
10Here the subscripts indicate the type component and not copy indices, which are left un-specified.

## PDF page 28

24:28

S. Castellan and P. Clairambault

Vol. 20:3

The final statement is a careful verification following the definition of the interpretation,
see [HO00]. Here, case is the syntax introduced in Section 1.3, involving the let construct.
Without that, simply iterating if constructs would yield a strategy that re-computes
xi0 pMi0 ,1 x1 . . . xn q . . . pMi0 ,pi0 x1 . . . xn q
each time it matches it against a value. This is what is done in [HO00] as their version of
PCF does not include a let construct. This yields a term that is not «-equivalent to σ, but
is nonetheless „-equivalent (see Section 1.6), which suffices for full abstraction. We prefer
the present more intensional definability result, and hence have included the let construct11.
3.3.2. Intensional full abstraction. Full abstraction of a denotational model with respect to
a language was defined in Section 1.6. Of course, Œ-Strat! is not fully abstract for PCF as it
stands. For instance, JλxU . x; xK ­« JλxU . xK: game semantics displays explicitly individual
calls to x, so we see that the term on the left hand side evaluates x twice whereas the other
evaluates it once. However, we do of course have λxU . x; x „ λxU . x; this can for instance
be deduced from them having the same interpretation in Scott domains [Plo77].
The celebrated “full abstraction for PCF” results are in fact what (following [AJM00])
we call intensional full abstraction. Fixing an interpretation J´K of PCF into a C, we set
f „g

ô

@α P CpA Ñ B, JUKq,

pα ˝ f “ α ˝ gq ,

for f, g P CpA, Bq, with f , g P Cp1, A Ñ Bq obtained via cartesian closure, and 1 the
terminal object of C. This mimics the definition of observational equivalence. We say that C
is intensionally fully abstract for PCF iff the quotiented model C „ is fully abstract.
Theorem 3.10. The model Œ-Stratwb,inn
is intensionally fully abstract for PCF.
!
Proof. Consider $ M, N : A s.t. M „ N , and assume JM K ­„ JN K, i.e. there is a test
α P Œ-Stratwb,inn
pJAK, JUKq s.t. α d! JM K ‰ α d! JN K – say w.l.o.g. that α d! JM K ó converges
!
while α d! JN K ò. One may prove (see [HO00] for details) that the corresponding interactions
expose only a finite part of α, so w.l.o.g. we can assume α finite. By Theorem 3.9, α is defined
via a PCF term, providing a context Cr´s s.t. JCrM sK “ α d! JM K and JCrN sK “ α d! JN K.
But then, we must have CrM s ó while CrN s diverges by Proposition 2.16; contradiction.
Intensional full abstraction is full abstraction for an a priori non effective quotiented
model: it does not directly provide effective tools to reason about observational equivalence.
Instead, it is a way of stating that we have faithfully captured the intensional behaviour of
programs, in the sense that the added tests in the model are not able to distinguish more –
there is no “abstraction leak”. Often, it follows from adequacy and finite definability.
Full abstraction is of course the preferred notion when the quotiented model is sufficiently
effective and the interpretation computable (i.e. effectively presentable [Plo81]). But when
it requires an undecidable quotient12, we believe it preferable to use a different terminology:
“intensional full abstraction” puts the emphasis on the model pre-quotient. In game semantics,
it is that model pre-quotient that had the most impact. In particular it then led to effective
fully abstract models for stateful languages, leveraging the results and insights above.
11An alternative is to include a primitive case evaluating its argument exactly once. The terms then
obtained via definability are easily characterised syntactically – dubbed PCF Böhm trees by Curien, and are
studied in [Cur98]. The definability process informs a concrete order-isomorphism between finite meager
innocent strategies and finite PCF Böhm trees, emphasizing that meager innocent strategies are syntax.
12For PCF this is unavoidable as observational equivalence is undecidable already for finitary PCF [Loa01].

## PDF page 29

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

w0´,Q

w1´,Q

✓`,A

✓`,A

...

wn´,Q

r´,Q

...

✓`,A

0`,A

1`,A

2`,A

...

Figure 22: ref r

Figure 21: ref w

24:29

g´,Q

rl´,Q

✓`,A

✓`,A

Figure 23: sem

3.4. Full Abstraction for IA. The exposition in Section 3.2 suggests that also without
innocence, strategies are computationally relevant for programs with mutable state. We now
focus on the game semantics of IA, namely PCF extended with interference (see Section 1).
3.4.1. Interpretation of types. With respect to PCF, IA adds the type ref of integer references,
and the type sem of semaphores. Their usual game semantic interpretation is behavioural, in
the sense that it represents how one may interact on those types: one may read a reference
or write a new value in it; and likewise one may ˘
grab a semaphore, or release it.
To capture this, we define ´-arenas: ref w “ nPN U, ref r “ N and sem “ U & U, and
set Jref K “ ref w & ref r and JsemK “ sem. Although we reuse the arena constructions for
U and N, for specific moves in these arenas we use the naming conventions of Figures 21, 22
and 23 – in Figures 21 and 22 all distinct moves in the same row are in pairwise conflict.
3.4.2. Interacting with Memory and Semaphores. The idea behind Abramsky and McCusker’s
interpretation of state is that it is not the operations of reading, writing, grabing or releasing
a semaphore that are effectful – indeed, those are just requests via the interface provided by
the ref and sem types and associated commands. The strategy for a program with free
reference or semaphore variables will simply record their accesses leaving the memory and
semaphores uninterpreted. For instance, the strategy for x : ref $ x :“ 0; !x : N includes:
!ref

⊸

N
q´

w0`
✓´
r`
42´
a play where the value read is not the value just written. The actual effectful computation
will be handled in Section 3.4.3 with the creation of new references and semaphores.
Accordingly, we set the interpretation of memory and semaphore accesses as:
JM :“ N K
J!M K
JgrabpM qK
JreleasepM qK

“
“
“
“

assign d! xJN K, JM Ky
deref d! JM K
grab d! JM K
release d! JM K

using the (innocent well-bracketed) strategies of Figures 24, 25, 26, and 27. Finally, we set
Jmkvar M N K “ xxJM K n | n P Ny, JN Ky ,

Jmksem M N K “ xJM K, JN Ky ,

where JM K n is JM K applied to the constant strategy n (using the cartesian closed structure
of Œ-Strat! ), and using implicitly the isomorphisms ref – p&nPN Uq & N and sem – U & U.
Finite definability of finite innocent well-bracketed strategies still holds – the proof (see
[AM96]) directly extends that of Theorem 3.9, using bad variables and semaphores.

## PDF page 30

24:30

Vol. 20:3

S. Castellan and P. Clairambault

!pN & ref q ⊸ U
q´
`
q0
n´
0
wn`
1
✓´
1
✓`

!ref ⊸ N
q´

!sem ⊸ U
q´

!sem ⊸ U
q´

r`
0

g0`

rl`
0

n´
0

✓´
0

✓´
0

Figure 24: assign

Figure 25: deref

✓`

n`

Figure 26: grab

✓`
Figure 27: release

Proposition 3.11. Consider A a type of IA, and σ : JAK finite innocent well-bracketed.
Then, there is a IA term $ M : A not using newref or newsem, such that JM K « σ.
3.4.3. Creation of References and Semaphores. Finally, we introduce the actual effectful
behaviour. The idea is to use non-innocent strategies celln :!ref , lockn :!sem implementing
interference. For instance, celln is a memory cell with n currently stored. When read it
returns n, and upon a write request for k P N, it acknowledges it and proceeds as cellk .
Likewise lock0 is the strategy for a free semaphore, and lockn for n ą 0 represents a semaphore
in use. Those may be simply described as the language of prefixes of the infinite trees:
IZtiu

IZtiu

`
cellIn “ r´
| wki´ ¨ ✓`
i ¨ ni ¨ celln
i ¨ cellk
IZtiu
´
`
´
I
lock0 “ gi ¨ ✓i ¨ lock1
| rli
IZtiu
´
´
`
I
lockn “ gi | rli ¨ ✓i ¨ lock0

pi R Iq
pi R Iq
pi R I, n ą 0q

where symbols are moves in !ref and !sem respectively, separated via ¨ for readability. Here,
I Ďf N collects the copy indices already used, ensuring non-repetitive. We set celln as
H
(the prefix language of) cellH
n and lockn as (the prefix language of) lockn ; it is direct that
celln :!ref and lockn :!sem. However, they are not innocent. Considering the two plays:
`
r´
0 ¨ 00 ,

`
´
`
w1´
1 ¨ ✓1 ¨ r0 ¨ 10

P

cell0 ,

´
`
´
´
`
as xr´
0 y “ xw11 ¨ ✓1 ¨ r0 y, innocence requires r0 ¨ 10 P cell0 as well, which is not the case.
Of course, it is precisely the role of cell and lock to break innocence and transfer information
across distinct copies – however, cell and lock remain P-visible in the sense of Definition 3.5.
We now complete the interpretation of IA. Consider Γ, x : ref $ M : A with

JM K P Œ-Stratwb,vis
pΓ & ref , Aq
!

omitting some brackets. Using the cartesian closed structure of Œ-Strat!wb,vis , we consider
Λ!Γ pJM Kq P Œ-Stratwb,vis p!ref , !Γ ⊸ Aq

which we compose with the memory cell. Summing up, for references and semaphores,
´1

Jnewref x:“ n in M K “ Λ!Γ pΛ!Γ pJM Kq d celln q P Œ-Stratwb,vis
pΓ, Aq
!
´1
wb,vis
!
!
pΓ, Aq .
Jnewsem x:“ n in M K “ ΛΓ pΛΓ pJM Kq d lockn q P Œ-Strat!

This concludes the interpretation of IA in Œ-Stratwb,vis . Adequacy proceeds as in [AM96],
undisturbed by the slightly different technical setting of the present paper.
Proposition 3.12 (Adequacy). For any $ M : U in IA, M ó if and only if JM K ó.

## PDF page 31

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:31

3.4.4. Full Abstraction. We now review the full abstraction result of [AM96]. The argument
revolves around a fundamental factorisation theorem, stated as follows.
Theorem 3.13 (Factorisation). Let A be a type of IA, and σ : JAK be P-visible well-bracketed.
Then, there is an innocent well-bracketed Innpσq P Œ-Stratwb,inn p!ref , JAKq such that
σ « Innpσq d cell0 ,

and Innpσq is finite if σ is finite.
Proof. For any O-ending sa´ P σ, we wish Innpσq to act like σ, but as an innocent strategy
it may only depend on xsa´ y. However, Innpσq may also access the reference, so we will
maintain the invariant that the reference contains (an encoding of) the full history, or more
precisely of Ppsq. Between xsa´ y and Ppsq, σ knows the full play (up to symmetry).
Upon being called with a´ , Innpσq reads Ppsq from the reference, then stores Ppsabq
in the reference (for sa´ b` P σ) and then plays b. See [AM96] for more details.
Finiteness of Innpσq follows the definition of finite innocent strategies from Section 3.3.1:
having finitely many (–-equivalence classes of) P-ending P-views. However, finiteness
of non-innocent strategies has not yet been defined. We define it now: a strategy in
Œ-StratpAq is finite iff the set of (–-equivalence classes of) P-ending plays of σ is finite.
Despite the common terminology, these two notions are distinct: an innocent strategy may
be finite as an innocent strategy while being non-finite as a non-innocent strategy. This
mismatch comes from the fact that these two notions both coincide with the domain-theoretic
notion of compactness, but in the distinct domains Œ-Stratwb,inn pA, Bq and Œ-Stratwb pA, Bq
(ordered by inclusion) for ´-arenas A, B. By Proposition 2.22, these statements involving
–-equivalence classes may be instead phrased with plays with pointers.
From Theorem 3.13 and Proposition 3.11 it is direct that finite definability holds for IA.
We can deduce immediately intensional full abstraction for IA, proved as Theorem 3.13.
Theorem 3.14. The model Œ-Stratwb,vis
is intensionally fully abstract for IA.
!
This is exactly as Theorem 3.10. However, in stark contrast with Theorem 3.10, for IA
the fully abstract quotient category is effectively presentable. In fact, for σ, τ : JAK,
σ„τ

ô

Ppcomppσqq “ Ppcomppτ qq

where comppσq is the set of complete plays of σ, capturing the completed executions where
both players act like P-visible well-bracketed strategies: a play is complete if it is wellbracketed, P-visible, O-visible (the dual to P-visibility, not detailed here), and such that
every question has an answer. The result follows from finite definability for IA [AM96].
This effective fully abstract model of IA is one of the most striking results of game
semantics. Observational equivalence in IA remains undecidable with bounded integers,
at fourth order without recursion [Mur03] and second-order with recursion [Ong02] (of
course, observational equivalence is obviously undecidable in the full language as it is Turingcomplete). However, the model yielded sound and complete algorithms for observational
equivalence on restricted fragments [GM03], starting the field of algorithmic game semantics.
3.5. The Semantic Cube. Abramsky’s “semantic cube”, often called the “Abramsky
cube”, starts with the observation that game semantics allows the interpretation of both
control (i.e. callcc) and state in the same model, i.e. the same category.

## PDF page 32

24:32

Vol. 20:3

S. Castellan and P. Clairambault

3.5.1. Control. We have not given the interpretation of callcc, nor the corresponding full
abstraction result [Lai97]. In fact, in the present technical setting, we cannot interpret
callcc. This is due, in part, to the added conflict in arenas for basic datatypes with respect
to standard HO games [HO00] – see Figures 6, 7, and 8. This conflict imposes that each
question can be answered at most once, which is incompatible with callcc13. In fact:
Proposition 3.15. For any PCF type A, any innocent σ : JAK is also well-bracketed.

Proof. First, any innocent σ : JAK is well-bracketed iff its P-views are well-bracketed – see
[Lai97] for a proof. Hence if σ is not well-bracketed, then there is a P-view
s1 . . . q´,Q . . . q´,Q . . . a`,A
where a answers the first q shown rather than the pending question, the second q shown.
But this second q´,Q must be the initial move of a banged sub-arena in the interpretation
of A, so we can play it again. And by innocence of σ, the following must be a play of σ:
´,Q
s1 . . . q´,Q . . . q´,Q
. . . a`,A qi`1
. . . a`,A
i

where both copies of a point to the first q´,Q , absurd by non-repetitive.
This entails that in fact, Theorem 3.10 holds for Œ-Stratinn
! . But no such coincidence
holds beyond innocent strategies: for Theorem 3.14 well-bracketing really is needed. In this
paper we have adopted an interpretation of ground types incompatible with callcc. There is
no technical obstacle to modelling callcc – one can simply drop conflicts in basic arenas and
duplicate return values – but we prefer our design, closer to linear logic and the relational
model (see Section 7.1.6). Furthermore, control operators will play no role in the present
paper beyond the exposition of the scientific context.
3.5.2. The Semantic Cube. We temporarily consider, for the sake of the discussion, a setting
with both control and state; say Murawski’s model for interference and control [Mur07],
which is essentially equivalent (modulo the representation with pointers) to ours where basic
arenas have no conflict and answers are replicated. Let us call it by Vis. There is
PCF ` interference ` control

Ñ

Vis

an adequate interpretation, so we can model a rich combination of effects; but that is not all.
Indeed, there are four (intensional) full abstraction results:
Theorem 3.16 (Semantic Cube). We have four intensional full abstraction results:
Vis
Vis ` innocence
Vis ` well-bracketing
Vis ` innocence ` well-bracketing

is fully abstract for
is fully abstract for
is fully abstract for
is fully abstract for

PCF ` interference ` control
PCF ` control
PCF ` interference
PCF

We have reviewed two cases before, namely PCF (Theorem 3.10) and PCF ` interference
(Theorem 3.14). The full abstraction result for PCF ` control is due to Laird [Lai97], while
for PCF ` interference ` control appears in Murawski14 [Mur07].
13In addition to conflicts, the incompatibility with callcc comes from the fact that our interpretation of
types only involves ! on arrows, and not on basic datatypes. To authorize control we should change e.g. the
arena B to one with replicated answers, written (in the language of tensorial logic [MT10]) as ␣!␣p1 ‘ 1q.
14Murawski uses a different primitive for control, but the difference is superficial within IA.

## PDF page 33

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:33

Figure 28: The Semantic Cube
This “Semantic Cube”, drawn in Figure 28, expresses that the conditions on strategies
capture the behaviour generated by certain computational effects; or rather the absence
of certain effects. The achievement is noteworthy, as it is famously difficult to combine
semantic accounts of computational effects. But independently of purely semantic purposes,
this provides us with a microscope to study behaviourally interactions between effects in
programming languages. We demonstrate this with the following orthogonality property15
between interference and control which nicely illustrates the strength of game semantics:
Theorem 3.17. Let $ M : A a term of PCF ` interference ` control. Assume that
p1q M „ N1 where N1 is a term of PCF ` interference,
p2q M „ N2 where N2 is a term of PCF ` control;
then M „ N where N is a term of (an infinitary extension of ) PCF.
Proof. Consider JM K : A. We have seen in Section 3.4.4 that for IA, strategies are indistinguishable iff they have the same complete plays. In the presence of control this phenomenon
gets stronger: strategies are indistinguishable iff they have the same plays [Mur07]. Hence,
JM K is an innocent well-bracketed strategy (even though M might internally use state and
control). It is approximated by a sequence of finite innocent strategies which may be defined;
but as the definability process is monotone this yields an infinitary PCF term.
There are reasons to expect that in a version of PCF such as ours with a let construct,
the innocent well-bracketed games model is intensionally universal, meaning that each
computable innocent well-bracketed strategy is definable16 – though as far as we know, this
has not been proved. With such a result, Theorem 3.17 would generalize to conclude the
existence of simply a term of PCF, rather than an infinitary term.

3.6. Towards Concurrency. The reader may rightly complain that Figure 28 is not a
“semantic cube”, only a “semantic square”. Though we focused on control and interference,
there are fully abstract models of languages featuring general references [AHM98], exceptions
15

We learnt of it from a talk by Paul Levy in 2014 [Lev14].

16Hyland and Ong have a extensional universality theorem [HO00], i.e. up to observational equivalence.

In their setting, intensional universality fails: in the absence of a let construct, the strategies obtained by
universality stutter, repeating the same move possibly many times. Intensional universality does not appear
anywhere in call-by-name, but it does in call-by-value [MT13].

## PDF page 34

24:34

Vol. 20:3

S. Castellan and P. Clairambault

pU

Ñ

Uq

Ñ

N
q´

q`
0
q´
0,0
✓´
0
✓`
0,0
1`

λf UÑU . newref r:“ 0 in f pr :“ 1q; !r
λf UÑU . newref r:“ 0 in f pr :“ 1q; !r
λf UÑU . newref r:“ 0 in f pr :“ 1q; !r
λf UÑU . newref r:“ 0 in f pr :“ 1q; !r
λf UÑU . newref r:“ 0 in f p skip q; !r
λf UÑU . newref r:“ 0 in f p skip q; 1

r ÞÑ 0
r ÞÑ 0
r ÞÑ 0
r ÞÑ 0
r ÞÑ 1
r ÞÑ 1

Figure 29: Operational content of a non-alternating play
[Lai01a], coroutines [Lai04], non-determinism [HM99], probabilistic choice [DH00], concurrency [Lai01b, GM08], and others. One imagines that the methodology above generalizes,
and that the big “syntactic hypercube” of these effects is matched by a “semantic hypercube”.
However, there is no such “semantic hypercube”: the works cited above rely on a priori
incompatible formal settings. In this paper, we present steps towards such a semantic
hypercube. More precisely we aim to disentangle parallelism and interference in the same
sense as the “Abramsky cube” disentangles control and interference, i.e. we must answer:
Question. Build a model _-Strat with notions of parallel innocence and sequentiality s.t.:
_-Strat
_-Strat ` parallel innocence
_-Strat ` sequentiality
_-Strat ` parallel innocence ` sequentiality

is fully abstract for
is fully abstract for
is fully abstract for
is fully abstract for

IA ,
PCF ,
IA ,
PCF ,

all of these being intensional full abstraction results.

The model should be fully abstract for IA , link with Œ-Stratwb,inn
and Œ-Stratwb
!
!
(respectively fully abstract for PCF and IA), but also support a notion of parallel innocence
yielding full abstraction for PCF . It is natural to start with a simple non-alternating variant
of Œ-Strat, inspired by Ghica and Murawski’s fully abstract games model for IA [GM08].
3.6.1. Non-alternating plays and strategies. We simply relax alternation in Definition 2.7.
Definition 3.18. A non-alternating play on ´-arena A is s “ s1 . . . sn which is:
valid:
@1 ď i ď n, ts1 , . . . , si u P C pAq ,
non-repetitive: @1 ď i, j ď n, si “ sj ùñ i “ j ,
negative:
n ě 1 ùñ polps1 q “ ´ .
We write ö-PlayspAq for the set of non-alternating plays on A.
The notation (inspired by template games [Mel19]), is intended to suggest that whereas
alternating plays in Œ-PlayspAq transition between two states O and P determining which
player has control, in ö-PlayspAq there is only one state, in which either player may play. The
intuition is simple: as several threads might be running in parallel, their interleaving breaks
alternation. We show in Figure 29 a non-alternating play on JpU Ñ Uq Ñ NK, using the
same conventions as previously. Resting on the same computational intuitions as before, we
show for each move a representation of the matching computational state of a term realizing
that play. The figure illustrates that even IA, a sequential language, allows non-alternating

## PDF page 35

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:35

plays, as the environment can evaluate subterms in parallel. After the third and fourth
moves, two subterms are being evaluated in parallel: r :“ 1 and !r, causing a data race.
As before, we may now define strategies as certain sets of plays.
Definition 3.19. A non-alternating strategy σ : A, is σ Ď ö-PlayspAq which is:
non-empty:
prefix-closed:
receptive:
courteous:

εPσ
@s Ď s1 P σ, s P σ
@s P σ, sa´ P ö-PlayspAq ùñ sa P σ
@sabt P σ, sb P ö-PlayspAq, ppolpbq “ ´ _ polpaq “ `q ùñ sbat P σ

A non-alternating prestrategy is only required to satisfy non-empty and prefix-closed.
Let us compare with Definition 2.8. Besides moving to non-alternating plays, we remove
determinism. Of course, this is natural since the interleaving semantics of even a pure
parallel language represents non-deterministically the choices of the scheduler. The new
condition added is courtesy, it corresponds to the saturation condition of [GM08] (the name
“courtesy” is imported from [MM07]). Courtesy expresses that the model is asynchronous.
If one has sa` b P σ, there is an execution of σ where it plays a, then we observe b (of any
polarity). But if the surrounding computing environment is asynchronous, nothing forces a
to be directly observable by Opponent – a might get stuck in a buffer, in the network, etc.
So then, courtesy imposes that σ should be stable under asynchronous delays: if sa` b P σ
and there is no dependency from a to b in the arena, then a can be postponed after b in σ.
3.6.2. Well-bracketing. We introduce well-bracketing for non-alternating strategies. In Ghica
and Murawski’s games, all plays are well-bracketed in the sense that they satisfy two
conditions, dubbed fork and wait. We adapt and introduce these conditions now.
Definition 3.20. For a ´-arena A, s P ö-PlayspAq is well-bracketed if for any s1 Ď s,
fork: if s1 “ . . . qQ . . . m with q _A m, q must be unanswered before m is played,
wait: if s1 “ . . . qQ . . . aA with q _A a, all questions justified by q must be answered.

This differs from the simple well-bracketing of alternating plays (Definition 3.2). In a
non-alternating setting it does not make sense to refer to the last unanswered question as it
might originate in a different thread than the one the Player move to be played belongs to.
Instead, this condition forces plays to follow the following protocol: a question, as long as it
is not answered, may prompt (i.e. justify) other questions. It can only be answered once
all the questions it justified are answered, and then it will not be able to justify anything
further. For instance, the play of Figure 29 is not well-bracketed: the fourth move ✓´
0
´
causes a failure to wait because it is justified by q`
,
although
the
latter
has
justified
q
as
0
0,0
´
´
of yet unanswered. If we were to permute the moves q´
0,0 and ✓0 then q0,0 would cause a
failure to fork as it would be justified by a question that is already answered.
Rather than imposing this condition on all plays, we impose it on strategies.
Definition 3.21. Let σ : A be a non-alternating strategy.
It is well-bracketed iff for all sa` P σ, if s is well-bracketed then sa is well-bracketed.
The play of Figure 29 belongs to a well-bracketed strategy: Opponent breaks wellbracketing first. This is a slight difference with Ghica and Murawski’s model: we observe all
dynamic behaviour of a program of IA , even that not reachable via a context of IA . Of

## PDF page 36

24:36

Vol. 20:3

S. Castellan and P. Clairambault

pB

Ñ

Uq

Ñ

U
q´

pB

Uq

Ñ

U
q´

q`

q`
q´
ff `

Ñ

q´
tt`

Figure 30: Two (pointer representation) of plays in a parallel innocent strategy
course, it is always possible to restrict to well-bracketed plays without cutting any Player
behaviour (i.e. the strategy is cut at Opponent extensions, not Player extensions).

3.6.3. Limitations. The proximity of non-alternating strategies to both Œ-Strat and Ghica
and Murawski’s model make them a tempting foundation for this paper. However, they
have two limitations, both subtly related to their inability to record the branching structure.
Firstly, parallel innocence requires adequate causal structures, as illustrated by the
following example. Is there a parallel innocent strategy that includes the two plays with
pointer representation in Figure 30? Is there a program of PCF that may realize both?
Traditional innocence forbids that, because in a sequential program, both plays must be
visiting the same piece of syntax and obtain the same result. In PCF though, the program
ˆ
˙
x “ f tt
BÑU
λf
. let
in x; y : pB Ñ Uq Ñ U
y “ f ff
indeed realizes these two plays, corresponding to the evaluation of distinct threads. A
deterministic innocent strategy is determined by (the pointer representation of) its P-views,
so we may see the set of P-views as a witness for innocence. Analogously, what structure
may witness that a non-alternating strategy is innocent? In fact, what is missing from the
two P-views of Figure 30 is the branching structure, keeping these two P-views apart and
recording how they are linked to each other. It has already been observed [CCW14, TO15]
that non-deterministic innocence may be defined by replacing sets of P-views, as witnesses
for innocence, with trees recording the non-deterministic branching information. Here we
must do the same, but instead record the branching structure pertaining to parallelism as
well – which plain non-alternating strategies cannot capture adequately [CC16].
Secondly, it is unclear how to endow non-alernating strategies with appropriate notions
of symmetry and uniformity as in Definition 2.13. Our attempts at generalizing Definition
2.13 ended up suffering from various pathologies, typically uniformity not being preserved
by hiding. The tension with hiding comes from a play s P τ d σ being witnessed by distinct
interactions between σ and τ – this suggests again the need for an explicitly branching
structure, as then one recovers a unique witness property. For these two reasons, we move
from plain non-alternating strategies to thin concurrent games. We will, however rely on:
Proposition 3.22. There is a symmetric monoidal closed category with products ö-Stratwb ,
with objects ´-arenas, and morphisms well-bracketed non-alternating strategies on A ⊸ B.
Proof. The constructions play a minor role in this paper and are very similar to the alternating
case, so we omit them. Some details of the construction appear in Appendix C.

## PDF page 37

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:37

These limitations call for a more intensional setting, representing explicitly the parallel
and non-deterministic branching structures. To our knowledge, the only games setting in
the literature sufficiently expressive and mature is thin concurrent games, one of the possible
enrichments with symmetry of the concurrent strategies of Rideau and Winskel [RW11].
4. Causal Full Abstraction for IA
Thin concurrent games were first introduced in [CCW15], but the detailed construction
(along with significant improvements and simplifications) is presented in [CCW19].
In this section, we start with an introduction to thin concurrent games. We omit
detailed constructions (which appear in [CCW19]), but we do attempt to give a selfcontained introduction, in particular providing required reasoning principles. Then, we
apply this setting to give a fully abstract model for IA , the causal sibling of Ghica and
Murawski’s model [GM08]. In the concurrent games literature, strategies are often referred
to as concurrent strategies. Here we prefer causal strategies to better distinguish them with
non-alternating strategies, which also represent concurrent behaviour.
4.1. Arenas and causal strategies. First, we must refine the symmetry on arenas.
4.1.1. Polarized symmetry. Arenas for causal strategies in [CCW19] require the following:
Definition 4.1. For A an arena with isomorphism family S pAq, a polarized decomposition of S pAq comprises isomorphism families S´ pAq, S` pAq included in S pAq, s.t.:
(1) If θ P S´ pAq X S` pAq, then θ is an identity bijection,
(2) If θ P S´ pAq and θ Ď´ θ1 P S pAq, then θ1 P S´ pAq,
(3) If θ P S` pAq and θ Ď` θ1 P S pAq, then θ1 P S` pAq.
where Ďp means that only (pairs of) events of polarity p are added.
If θ : x –A y and θ P S´ pAq, we write θ : x –´
A y and call θ a negative symmetry.
`
Likewise, θ : x –A y means that θ : x –A y with θ P S` pAq, called a positive symmetry.
Arenas with a polarized decomposition are thin concurrent games 17 in the sense of
[CCW19]. Intuitively, negative symmetries (resp. positive) reindex Opponent (resp. Player)
moves – though Definition 4.1 does not involve “copy indices”. By Lemma 3.19 from
[CCW19], any θ : x –A z factors uniquely as θ` ˝ θ´ , with θ` positive and θ´ negative.
4.1.2. Constructions on arenas. First we extend the arena constructions accordingly.
For U, B and N, all isomorphism families are reduced to identity bijections between
configurations. For the dual of an arena A, then for all symmetry θ : x –A y,
θ : x –`
y
AK

ô

θ : x –´
A y,

θ : x –´
y
AK

ô

θ : x –`
A y.

For parallel composition and product, the sub-symmetries are inherited as for the
full symmetry in Section 2.2.1 applying to the positive and negative isomorphism families
separately. For the arrow, for x, y P C pA ⊸ Bq and θ : x » y an order-isomorphism, we set
θ P S` pA ⊸ Bq iff χA,B θ P S` pAK ∥ Bq; and θ P S´ pA ⊸ Bq iff χA,B θ P S´ pAK ∥ Bq.
17Thin concurrent games in [CCW19] are more general, e.g. they might not be alternating or forestial.

## PDF page 38

24:38

Vol. 20:3

S. Castellan and P. Clairambault

The most interesting construction is the exponential. Recall that a symmetry in !A is
θ : ∥nPN xn – ∥nPN yn
pn, aq ÞÑ pπpnq, θn paqq
for some permutation π P ςpNq and for some family pθn qnPN with θn : xn –A yπpnq for all
n P N. First we set θ P S´ p!Aq iff for all n P N, θn : xn –´
A yπpnq . Finally, we set θ P S` p!Aq
iff for all n P N such that xn is non-empty, we have πpnq “ n, and θn : xn –`
A yn .
We recall from Section 2.2.1 our representation of configurations of !A with an example:
Example 4.2. Consider the arena o with only one (negative) move q´ , and !p!o ⊸ oq, with
set of events N ˆ pN ˆ tqu Z tquq. Following the notations of Section 2.2.1, we draw
q´
0

q´
1

q`
0,2

q`
1,4

for the configuration tp0, qq, p1, qq, p0, p2, qqq, p1, p4, qqqu, which may also be written as
∥iPt0,1u xi for x0 “ tp2, qqu and x1 “ tp4, qqu. Writing γ0,1 P ςpNq for the permutation
exhanging 0 and 1, the symmetry described by pγ0,1 , pidxi qiPt0,1u q may be represented as
q´
0

q´
1

q`
0,2

q`
1,4

–!p!o⊸oq

q´
1

q´
0

q`
1,2

q`
0,4

sending a move on one side to the move at the same spot on the other side. This reindexes
`
initial move, leaving the subsequent moves morally unchanged: q`
0,2 is sent to q1,2 , but the
first number just identifies the causal predecessor – the actual copy index, 2, is unchanged.
The symmetry above is negative. It is not positive, because γ0,1 is not the identity.
Likewise, the two symmetries represented below:
q´
0

q´
1

q`
0,2

q`
1,4

–!p!o⊸oq

q´
0

q´
1

q´
0

q´
1

q`
0,2

q`
1,5

q`
0,2

q`
1,4

–!p!o⊸oq

q´
1

q´
0

q`
1,5

q`
0,2

are respectively positive, and neither positive nor negative.
Why does !A treat differently the positive and negative isomorphism families? The permutation πp´q corresponds to reindexing the minimal events of !A. Because the exponential
construction is intended to apply to negative games, πp´q reindexes negative moves. But
symmetries in S` p!Aq can only reindex positive moves, so πp´q must be the identity. In
contrast, symmetries in S´ p!Aq can perform any reindexing on the minimal events.
This intuition is further solified by the extension of concrete arenas to these polarized
sub-isomorphism families. This will not be required until much later, so it only appears in
Section 7.3.1 – but it might still be helpful for the reader to consult it now.

## PDF page 39

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

pU

⊸

q`
|

✓`

s{
q´

D

✓`

pU

N

v6

✓

⊸

s{ /

t|
q´

´

 ' '.
 1`

 &- 0`

Figure 31: A causal strategy

_

0

⊸

Uq

q´

_

.

z"

⊸

Uq

q`

t| 0

N

t|
q´

´

 "*'. `
1

✓`

⊸

0

_ /
s{

⊸

Uq

q´

_

✓

pU

q`

24:39

t| 0

N
q´

_

✓´

✓`

 "* `

0

Figure 32: Two augmentations of Figure 31

4.1.3. Causal strategies. In contrast with traditional game models, a causal strategy is one
global object: an event structure. It presents all execution threads together, with explicit
information on how these executions relate via parallel and non-deterministic branching.
Definition 4.3. A causal prestrategy σ : A comprises an ess p|σ|, ďσ , #σ , S pσqq with
B : |σ| Ñ |A|
a function called the display map, subject to the following conditions:
for x P C pσq, Bpxq P C pAq,
for s1 , s2 P x P C pσq, if Bps1 q “ Bps2 q then s1 “ s2 ,
for θ P S pσq, Bpθq “ tpBps1 q, Bps2 qq | ps1 , s2 q P θu P S pAq,
´
´
for θ : x –σ y, and extensions x $σ s´
1 , Bpθq $S pAq pBps1 q, a2 q,
´ ´
´
´
there is a unique s´
2 P |σ| s.t. θ $S pσq ps1 , s2 q and Bps2 q “ a2 ,
`
thin: for θ : x –σ y, and extension x $σ s1 ,
` `
there is a unique extension y $σ s`
2 such that θ $S pσq ps1 , s2 q.

rule-abiding:
locally injective:
symmetry-preserving:
„-receptive:

Additionally, we say that σ is a causal strategy if it also satisfies:
negative: for s P |σ|, if s is minimal then s is negative,
courteous: for s1 _σ s2 , if polps1 q “ ` or polps2 q “ ´ then Bps1 q _A Bps2 q,
receptive: for x P C pσq, for Bpxq $A a´ ,
there is a unique x $σ s´ P C pσq such that Bpsq “ a,
As a convention, causal strategies are ranged over by symbols in bold font, as in e.g.
σ, τ . We disambiguate some notations used in the definition. First, σ implicitly comes with
polarities, imported from A as polσ psq “ polA pBpsqq. We also used the enabling relation on
isomorphism families, defined by θ $S pAq pa1 , a2 q iff pa1 , a2 q R θ and θ Z tpa1 , a2 qu P S pAq.
Conditions rule-abiding, locally injective and symmetry-preserving together amount to B
being a map of event structures with symmetry [Win07]. Conditions courteous and
receptive play the same role as in Definition 3.19. The condition „-receptive forces strategies
to treat uniformly any pairs of Opponent events symmetric in the game. Finally, thin forces
strategies to pick one canonical representative up to symmetry for positive moves. For
further explanations and discussions on those conditions, the reader is directed to [CCW19].
Causal strategies and non-alternating strategies differ fundamentally in how the concurrent behaviour is represented. While non-alternating strategies present observable execution
traces, causal strategies present the causal constraints underlying the observed behaviour.
In Figure 31, we present a causal strategy, corresponding to a linear version of Figure 29. In
this diagram and others further on, we draw σ : A by picturing the event structure σ with

## PDF page 40

24:40

S. Castellan and P. Clairambault

Vol. 20:3

events displayed as their image through Bσ . Whenever possible, we keep the convention
to draw moves under the corresponding type component. The causal dependency ďσ is
pictured via its immediate dependency relation _σ . As with arenas, we show immediate
conflicts (i.e. not inherited) as wiggly lines. As in plays, we denote by dotted lines the
immediate causal dependency in the arena A: for s P |σ|, either Bσ psq is minimal in A, or
there is a unique s1 P |σ| such that Bσ ps1 q _A Bσ psq; in which case the diagram has a dotted
line between the events representing s and s1 . Borrowing earlier terminology, we refer to s1
as the justifier of s. Finally, the symmetry S pσq is not shown at all (of course, for Figure
31 it would remain trivial). Indeed it is hard to represent, but also we regard it as not being
part of the pertinent operational structure: its mere existence witnesses uniformity.
Figure 31 presents, in one diagram, the full behaviour of the program of Figure 29 under
linear execution contexts. Drawing a strategy fully in this way is sometimes challenging. It
is often convenient to refer to – and draw – consistent fragments of a causal strategy: an
augmentation of σ is any px, ďx q where x P C pσq and ďx is the partial order inherited
from ďσ . For instance the two maximal augmentations of Figure 31 yield the diagrams
of Figure 32. In this case, the two configurations correspond to the two resolutions of the
date race described with Figure 29: if the write wins, the read yields 1 and depends on
q´ (which triggered the write). If the read wins, we read 0 and the write acknowledgment
depends on ✓´ (which triggered the read). However, this representation of a strategy via
its augmentations is partial: it forgets the explicit non-deterministic branching.
4.1.4. Non-alternating unfolding. Causal strategies generate non-alternating strategies:
Proposition 4.4. Consider A a ´-arena, and σ : A a causal strategy.
The non-alternating unfolding of σ is (with Bσ applied to plays move-by-move):
ö-Unfpσq “ Bσ pö-Playspσqq .
Thus defined, ö-Unfpσq : A is a non-alternating strategy on A.
Proof. Non-empty and prefix-closed are obvious. For receptive, take s P ö-Unfpσq s.t.
sa´ P ö-PlayspAq. By definition, there is t P ö-Playspσq s.t. s “ Bσ ptq. Thus t, written
t “ t1 . . . tn P ö-Playspσq ,
is such that for all 1 ď i ď n, tt1 , . . . , ti u P C pσq, and is also non-repetitive and negative. Let
us write x “ tt1 , . . . , tn u. Then, Bσ pxq “ ts1 , . . . , sn u P C pAq, and since sa´ P ö-PlayspAq
we have Bσ pxq $A a´ . By receptivity of σ, there is (a unique) m P |σ| such that x $σ m and
Bσ pmq “ a. It is then direct that tm P ö-Playspσq, witnessing sa P ö-Unfpσq as required.
For courteous, consider s1 abs2 P ö-Unfpσq s.t. polpaq “ ` or polpbq “ ´, and s1 b P
ö-PlayspAq. By definition, there is t1 mnt2 P ö-Playspσq s.t. s1 abs2 “ Bσ pt1 mnt2 q. We claim
that x “ |t1 n| P C pσq. We know that |t1 mn| P C pσq; so x is consistent. If it is not downclosed, necessarily m _σ n. So, by courtesy of σ, a _A b; contradicting s1 b P ö-PlayspAq.
Thus |t1 n| P C pσq from which we deduce t1 nmt2 P ö-Playspσq, so s1 bas2 P ö-Unfpσq.
For instance, the non-alternating play in Figure 29 is in the unfolding of the causal
strategy in Figure 31. This extraction of a non-alternating strategy is an instance of the usual
relationship between interleaving and “truly concurrent” models for concurrency. In this
paper this relationship will in particular allow us to import well-bracketing from ö-Stratwb .
Definition 4.5. Consider σ : A a causal strategy on ´-arena A.
We say that σ is well-bracketed if ö-Unfpσq : A is well-bracketed.

## PDF page 41

Vol. 20:3

⊸

U

q`

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

pU

U

⊸

$

Uq

q´

t| 0

_

vs

✓´
 #+

t|
q´
_

✓`

0

q`

t| 0

N
q´

q`

t| 0

vs
 #+

 "*'. `
1

Figure 33: Matching, secured

⊸

$

Uq

N

q´

✓´

´

✓`

pU

U

_

_

✓

⊸

U

24:41

t|
q´

0

_ /
s{

✓`

q`

q´

t| 0

_

✓´

✓`

 "* `

0

Figure 34: Matching, non-secured

4.2. A Category of Causal Strategies. We now start building the categorical operations
on causal strategies, aiming at a Seely category _-Strat. We first focus on composition.
For ´-arenas A and B, a causal strategy from A to B is a causal strategy
σ : AK ∥ B ,
in the sequel we also write A $ B for AK ∥ B. This is unlike for Œ-Strat and ö-Strat
introduced earlier, for which morphisms from A to B were defined as strategies on A ⊸ B.
We do this to keep close to [CCW19]. When linking with Œ-Strat and ö-Strat we shall deal
with this mismatch, but that will not cause us too much trouble18.
Composition of causal strategies is more elaborate than for play-based strategies. We
define it in several stages. Fix two causal (pre)strategies σ : A $ B and τ : B $ C.
4.2.1. Synchronization. For configurations xσ P C pσq, xτ P C pτ q, as a convention we write
σ
Bσ pxσ q “ xσ
A ∥ xB P C pA $ Bq ,

Bτ pxτ q “ xτB ∥ xτC P C pB $ Cq ,

for the corresponding projections to the game. In defining composition, the first stage is to
capture when such configurations xσ P C pσq and xτ P C pτ q may successfully synchronise.
Definition 4.6. Consider two configurations xσ P C pσq and xτ P C pτ q. They are causally
τ
compatible if (1) they are matching: xσ
B “ xB “ xB ; and (2) if the composite bijection
φxσ ,xτ

:

xσ ∥ xτC

Bσ ∥xτ
C

»

τ
xσ
A ∥ xB ∥ xC

´1
xσ
A ∥Bτ

»

τ
xσ
A ∥x ,

using local injectivity of Bσ and Bτ , is secured, in the sense that the relation
pm, nq Ÿ pm1 , n1 q

ô

m ăσ∥C m1

_

n ăA∥τ n1 ,

defined on (the graph of) φxσ ,xτ by importing causal constraints of σ and τ , is acyclic.
Two matching configurations xσ P C pσq, xτ P C pτ q agree on the state reached in B.
By local injectivity of Bσ and Bτ , this induces a bijection as above, thought of as the induced
synchronization between events of xσ and xτ that match in B. But this is not enough to
capture a sensible notion of execution: some matching pairs might not be reachable, in the
sense that σ and τ impose incompatible constraints as to the execution order. To illustrate
this we show in Figures 33 and 34 two attempted synchronizations between configurations
of the strategy of Figure 31 and the causal strategy for the identity λxU . x. In both cases,
18Plays on A ⊸ B carry more information than on A $ B, namely the justifier for initial moves in A.

With causal strategies, that information may be read back from the causal structure. See Section 4.3.2.

## PDF page 42

24:42

S. Castellan and P. Clairambault

Vol. 20:3

the configurations are matching. In Figure 33, the synchronization is successful and yields
causally compatible pairs of configurations. However, in Figure 34 the induced bijection is
not secured : the two strategies impose opposite constraints as to the order in which the two
✓ moves are to be played. Thus, this synchronization fails. For us, this will entail that the
identity λxU . x may only synchronize successfully with the augmentation of the program of
Figure 29 appearing in Figure 33 – so that the only final result is 1.
4.2.2. Interaction. But we must present the interaction of σ and τ as an event structure.
More specifically, it should be an event structure with symmetry along with a display map:
Definition 4.7. A pre-interaction on A, B, C is an ess µ “ p|µ|, ďµ , #µ , S pµqq with
B : |µ| Ñ |A ∥ B ∥ C|
a display map subject to the following conditions:
rule-abiding: for all x P C pµq, Bpxq P C pA ∥ B ∥ Cq,
locally injective: for all s1 , s2 P x P C pµq, if Bps1 q “ Bps2 q then s1 “ s2 ,
symmetry-preserving: for all θ P S pµq, Bpθq P S pA ∥ B ∥ Cq,
i.e. B : µ Ñ A ∥ B ∥ C is a map of event structures with symmetry.
An isomorphism between pre-interactions µ, ν on A, B, C is an isomorphism f : µ – ν
in the category of event structures with symmetry, commuting with the display maps, i.e.
Bν ˝ f “ Bµ . The interaction between σ and τ is a pre-interaction whose configurations
correspond exactly with pairs of causally compatible configurations xσ P C pσq, xτ P C pτ q:
Proposition 4.8. There is a pre-interaction τ f σ, the interaction of σ and τ , with
p´ f ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ and xτ are causally compatibleu » C pτ f σq
an order-iso (with causally compatible pairs ordered by component-wise inclusion) satisfying
τ
Bτ fσ pxτ f xσ q “ xσ
A ∥ xB ∥ xC

for all xσ P C pσq and xτ P C pτ q causally compatible.
In particular, any z P C pτ f σq is written uniquely as xτ f xσ for xσ P C pσq and

xτ P C pτ q. Thus, C pτ f σq may be regarded as the subset of C pσq ˆ C pτ q restricted to
those of the matching pairs which cause no deadlock. In fact, this property almost suffices
to characterise the interaction uniquely – to complete the picture, we must also consider
symmetries. Because display maps preserve symmetry, for θσ P S pσq and θτ P S pτ q,
σ
σ
Bσ pθσ q “ θA
∥ θB
,

τ
τ
Bτ pθτ q “ θB
∥ θC
,

σ “ θ τ , and causally compatible if
and we can say that θσ and θτ are matching if θB
B
dompθσ q, dompθτ q are causally compatible – or, equivalently, codpθσ q and codpθτ q are.
Taking into account symmetry, we may strengthen Proposition 4.8 to:

Proposition 4.9. There is a pre-interaction τ f σ, unique up to iso, such that there are
p´ f ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ , xτ causally compatibleu » C pτ f σq
p´ f ´q : tpθτ , θσ q P S pτ q ˆ S pσq | θσ , θτ causally compatibleu » S pτ f σq
order-isomorphisms commuting with dom and cod, and satisfying
σ
τ
Bτ fσ pθτ f θσ q “ θA
∥ θB ∥ θC

for all θσ P S pσq and θτ P S pτ q causally compatible.

## PDF page 43

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

¨
˚
˚
˚
˚
˚
˚
˚
˚
˝

pB

⊸

Uq

q`
{

tt`

q´

C

✓´

ff `

¨

)

✓`

¨

U

B

‹ ˚
˚
‹ ˚
*
‹ ˚
‹ f ˚ Cq` qx
‹ ˚ {
{#
‹ ˚ tt´
ff ´
‹ ˚
‚ ˝
 &-

q´

‹ ˚
(
‹ ˚
‹ ˚
qr pw
)
‹ ˚
‹ “ ˚ y >ql qx %
‹ ˚ ttr ff r
‹ ˚
‹ ˚
 '. ✓l  '. ✓l
‚ ˝
'.
`

B

q´ ‹

u 4

˛

⊸

U

_

s{ .
{#

˛

$

✓`

 &- ✓

⊸

U

$

 ✓r

24:43

˛
U
q´

 '. ✓

‹
‹
‹
‹
‹
‹
‹
‹
‚
r

Figure 35: Example of an interaction
Proof. Follows from the characterisation of the interaction as a pullback, whose projections
σ∥C o

Πσ

τ fσ

Πτ

/A∥τ

are maps of event structures with symmetry [CCW19] – see Appendix D.2.1 for details.
There is some redundancy in this statement: first, the action of p´f´q on configurations
coincides with that on identity symmetries. Reciprocally, one can actually prove that the
action of p´f´q on symmetries, if it exists, is uniquely determined by that on configurations –
so the fact that p´f´q extends to symmetries is property rather than structure. Nevertheless,
in the sequel, we often find convenient to perform the constructions on symmetries explicitly.
Altogether, this characterises the interaction in terms of its states and symmetries.
But there is also an alternative, event-based view: an individual event m P |τ fσ| may be
regarded as a synchronization between its projections Πσ pmq P |σ ∥ C| and Πτ pmq P |A ∥ τ |.
But we warn against the misleading idea that m P |τ f σ| is determined by these projections:
intuitively, there is one event in τ f σ for each pair ps, tq of synchronizable events, and each
distinct way to reach s and t conjointly in σ and τ . A simple example appears in Figure
35 (ignoring for now the l{r annotation and the part in grey): the final two copies of ✓
have the same projections, but a different causal history. Though we shall not unfold the
concrete construction of the interaction [CCW19], it might nonetheless help the reader to
have an idea of what its events are concretely defined to be. For xσ P C pσq and xτ P C pτ q
causally compatible, the reflexive transitive closure of Ÿ (see Definition 4.6) yields a partial
order ďxσ ,xτ on (the graph of) φxσ ,xτ . The events of τ f σ are then precisely the causally
compatible pairs pxσ , xτ q such that ďxσ ,xτ has a top element: the pair pΠσ pmq, Πτ pmqq.
In the sequel, we shall only reason on the interaction through the proxy of Proposition
4.9 and forthcoming lemmas characterizing immediate causality in the interaction. However,
to ease the flow of the exposition, those are postponed to Section 4.2.6.

4.2.3. Composition. Following the traditional methodology of game semantics, composition
is defined from interaction via hiding. We first briefly analyse the components of interactions.
The projections Πσ and Πτ project any event of τ f σ to a matching pair of an event
of σ ∥ C and an event of A ∥ τ . These projections help us classify every p P |τ f σ| into:
(1) Πσ ppq “ p1, mq with m P |σ|, and Πτ ppq “ p1, aq with a P |A|,
(2) Πσ ppq “ p1, mq with m P |σ|, and Πτ ppq “ p2, nq with n P |τ |,
(3) Πσ ppq “ p2, cq with c P |C|, and Πτ ppq “ p2, nq with n P |τ |.

## PDF page 44

24:44

S. Castellan and P. Clairambault

Vol. 20:3

In case (1), the only relevant projection is Πσ ppq “ p1, mq as Πτ ppq “ Bσ pmq. We write
pσ “ m and pτ is undefined, and we say that p occurs in A. In case (3), the only relevant
projection is Πτ ppq “ p2, nq as Πσ ppq “ Bτ pnq. We write pτ “ n and pσ is undefined, and
we say that p occurs in C. Finally, in case (2) the two projections Πσ ppq “ p1, mq and
Πτ ppq “ p2, nq are relevant, but we must have Bσ pmq “ p2, bq and Bτ ppq “ p1, bq for some
b P |B|. We write pσ “ m, pτ “ n, we say that p occurs in B and that p is synchronized.
The definition of composition consists simply in removing all synchronized events:
Definition 4.10. The composition of σ : A $ B and τ : B $ C comprises components:
|τ d σ| “ tp P |τ f σ| | p occurs in A or Cu ,
p1 ďτ dσ p2 ô p1 ďτ fσ p2 ,
p1 #τ dσ p2 ô p1 #τ fσ p2 ,
θ : x –τ dσ y ô Dθ Ď θ1 : x1 –τ fσ y 1 .
with display map Bτ dσ : |τ d σ| Ñ |A $ C| obtained as restriction of Bτ fσ .
The composition of prestrategies σ : A $ B and τ : B $ C gives data
p|τ d σ|, ďτ dσ , #τ dσ , S pτ d σq, Bτ dσ q
satisfying all the axioms of Definition 4.3 except, possibly, „-receptivity19. When composing
prestrategies, we will check „-receptivity separately – this only occurs in Section 4.4.3.
However, if σ and τ are strategies, then so is τ d σ [CCW19]. Composition is associative
up to iso (with isomorphisms between causal strategies defined as between pre-interactions
above). In Figure 35, the composition simply keeps the events in black. This means that
the composition has two conflicting positive events, both corresponding to ✓` : the model
records the point of non-deterministic branching even when it brings no observable difference.
Though this does not appear in pictures, we insist that events of τ d σ are certain events of
τ f σ. Thus an event of the composition always carries a unique causal explanation: itself.
To parallel this event-based definition of composition, there is a state-based characterization. A causally compatible pair xσ P C pσq, xτ P C pτ q is minimal if for all causally
σ
τ
τ
compatible y σ P C pσq, y τ P C pτ q with y σ Ď xσ , y τ Ď xτ with xσ
A “ yA and xC “ yC , then
xB “ yB . The same definition applies to causally compatible pairs of symmetries.
Proposition 4.11. Consider σ : A $ B, and τ : B $ C causal strategies.
There is a causal strategy τ d σ, unique up to iso, s.t. there are order-isos:
p´ d ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ , xτ minimal caus. comp.u » C pτ d σq
p´ d ´q : tpθτ , θσ q P S pτ q ˆ S pσq | θσ , θτ minimal caus. comp.u » S pτ d σq
commuting with dom and cod; s.t., for θσ P S pσq, θτ P S pτ q minimal causally compatible,
σ
τ
Bτ dσ pθτ d θσ q “ θA
∥ θC
.

The minimality requirement amounts to asking the maximal events of xσ and xτ to
occur in A or C. As events of τ d σ carry their causal witness, configurations of τ d σ
are in one-to-one correspondence with those configurations of τ f σ whose maximal events
occur in A or C – thus Proposition 4.11 follows from Proposition 4.9 (see Appendix D.2.2).
In fact, trailing Opponent moves do not matter as they are forced by receptivity and
courtesy to behave as in the game. A configuration x P C pσq is `-covered iff the top
elements of x (for ďσ ) are positive – we write x P C ` pσq. Likewise, θ P S pσq is `-covered
if dompθq (or, equivalently, codpθq) is `-covered – we write θ P S ` pσq. We have [dV20]:
19However, „-receptivity of σ and τ is required for τ f σ to form an ess [CCW19].

## PDF page 45

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:45

Lemma 4.12. Consider σ, τ : A two causal strategies. Assume there are
ψ : C ` pσq » C ` pτ q

ψ : S ` pσq » S ` pτ q

order-isomorphisms compatible with dom, cod, and display maps.
Then, σ and τ are isomorphic.
See Appendix D.2.3 for the proof. Relying on this we can finally prove:
Proposition 4.13. Consider σ : A $ B and τ : B $ C causal strategies.
Then, there is a strategy τ d σ : A $ C, unique up to iso, such that there are order-isos:
p´ d ´q : tpxτ , xσ q P C ` pτ q ˆ C ` pσq | xσ and xτ caus. comp.u » C ` pτ d σq
p´ d ´q : tpθτ , θσ q P S ` pτ q ˆ S ` pσq | θσ and θτ caus. comp.u » S ` pτ d σq
commuting with dom and cod, and s.t., for θσ P S ` pσq and θτ P S ` pτ q causally compatible,
σ
τ
Bτ dσ pθτ d θσ q “ θA
∥ θC
.

Proof. Relatively direct from Proposition 4.11 and Lemma 4.12, see Appendix D.2.3.
This is convenient as `-covered configurations of strategies often have a simpler description (see e.g. Lemma 4.19). Minimality also disappears as a causally compatible pair of
`-covered configurations is always minimal (indeed, a synchronized maximal event would
be negative for one of the players). This final characterization will be used often to prove
equalities between strategies. It is also of great use when linking with the relational model
(see Section 7.1), but also for quantitative extensions (see e.g. [CCPW18, CdV20]).
4.2.4. Congruence. What is the right equivalence between causal (pre)strategies? There are
a few options, several investigated in [CCW19]; here we use positive isomorphism:
Definition 4.14. Consider σ, τ : A two causal strategies on arena A.
A positive isomorphism φ : σ « τ is an isomorphism of ess satisfying
Bτ ˝ φ „` Bσ ,
i.e. for all x P C pσq, tpBσ psq, Bτ ˝ φpsqq | s P xu P S` pAq: the two maps are positively
symmetric. In that case we say σ and τ are positively isomorphic, and write σ « τ .
This means that σ and τ are the same up to renaming of their events. This renaming
might cause a reindexing of positive events, but it must keep the copy indices of negative
events unchanged. Crucially, positive isomorphism is preserved by composition [CCW19]:
Proposition 4.15. Consider σ, σ 1 : A $ B, τ , τ 1 : B $ C s.t. σ « σ 1 and τ « τ 1 .
Then, we have τ d σ « τ 1 d σ 1 .
The proof is fairly elaborate. Without going into details, it will be useful to have in
mind the first key step: showing that two (pre)strategies able to synchronize up to symmetry,
always also have a synchronization on the nose. More precisely, we have the following:
Proposition 4.16. Consider σ : A $ B and τ : B $ C two causal (pre)strategies.
τ
For any xσ P C pσq, xτ P C pτ q and θ : xσ
B –B xB s.t. the composite bijection is secured:
xσ ∥ xτC

Bσ ∥C

»

σ
τ
xσ
A ∥ xB ∥ xC

A∥θ∥C

–

τ
τ
xσ
A ∥ xB ∥ xC

A∥Bτ´1

»

τ
xσ
A ∥x ,

then there are y σ P C pσq and y τ P C pτ q causally compatible, along with symmetries
φσ : y σ –σ xσ ,

φτ : y τ –τ xτ ,

## PDF page 46

24:46

S. Castellan and P. Clairambault

Vol. 20:3

such that φτB ˝ θ “ φσ
B.
This follows from Lemma 3.23 in [CCW19]. Intuitively, we play S pσq and S pτ q against
each other. By „-receptivity and extension they adjust their copy indices interactively until
reaching an agreement. This is the first step to congruence, but not the only one: the
requirement that we should get a global map φ : τ d σ « τ 1 d σ 1 is in tension with the
definition of isomorphism families, which only guarantees a more local bisimulation-like
property. The mismatch is compensated by the uniqueness of extensions granted by thin,
without which congruence fails. Details are out of scope for the present paper [CCW19].
If σ « τ , there can be in principle multiple φ : σ « τ . We leave these isomorphisms to
the background, as we have not yet encountered a computational use for these. If they are
retained, then arenas, causal strategies and positive morphisms form a bicategory [Paq20].
Remark 4.17. In Definition 4.14, one could ask φ to preserve B up to arbitrary symmetry
(weak isomorphism) or even, to be itself invertible only up to symmetry (weak equivalence).
This changes the mediating morphisms, but not the resulting equivalence relation between
strategies (see Corollary 3.30 in [CCW19]). In this paper we choose positive isomorphism as
it seems natural conceptually, and because the additional positivity constraint is useful.
4.2.5. Copycat. So as to complete the categorical structure, it remains to define copycat.
Definition 4.18. For each ´-arena A, the copycat strategy ccA : A $ A is defined as:
|ccA | “ |A $ A|
BccA pi, aq “ pi, aq
pi, aq ďccA pj, a1 q ô a ăA a1 ; or a “ a1 and (polA$A pi, aq “ ´ or polAK ∥A pj, a1 q “ `)
pi, aq #ccA pj, a1 q ô a #A a1 ,
with symmetries those bijections of the form θ1 ∥ θ2 : x1 ∥ x2 –ccA y1 ∥ y2 such that
θ1 : x1 –A y1 ,

θ2 : x2 –A y2 ,

and θ1 X θ2 : x1 X x2 –A y1 X y2 .

This simplifies the usual definition [CCW19], exploiting the particular shape of arenas.
Its immediate causal links import _A on either side, along with all the pi, aq _ccA pj, aq
when polA$A pi, aq “ ´ and polA$A pj, aq “ `. In other words, ccA is an asynchronous
forwarder: it is prepared to play any positive event on one side, under the condition that the
corresponding negative event appears first on the other side. Its symmetries are inherited
from S pA $ Aq, with the constraint that they should agree on events already forwarded.
Perhaps the simplest description of copycat is through its completely forwarded states:
Lemma 4.19. Consider A any ´-arena. Then, we have:
C ` pccA q “ txA ∥ xA P C pA ∥ Aq | xA P C pAqu
S ` pccA q “ tθA ∥ θA P S pA ∥ Aq | θA P S pAqu .
Proof. Straightforward.
This foreshadows the link with relational semantics in Section 7.1: when restricted to
`-covered configurations, copycat looks like the identity relation. We may deduce:
Proposition 4.20. Composition is associative up to « on prestrategies. For any σ : A $ B,
ccB d σ d ccA « σ ,
so that ´-arenas and causal strategies form a category.

## PDF page 47

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:47

Proof. Associativity follows from Proposition 4.11 and a ternary version of causal compatibility – see also [CCW19] for a detailed proof via the universal property of the interaction
pullback. For neutrality of copycat, there is an order-isomorphism preserving display maps
C ` pccB d σq »
»
»
»

tpxccB , xσ q P C ` pccB q ˆ C ` pσq | xccB and xσ causally compatibleu
tpxccB , xσ q P C ` pccB q ˆ C ` pσq | xccB and xσ matchingu
σ
σ
σ
`
tpxσ
B ∥ xB , x q | x P C pσqu
C ` pσq ,

using first Proposition 4.13; verifying directly that securedness always holds when composing
with copycat; using Lemma 4.19. The same reasoning can be made with symmetries,
concluding that ccB d σ and σ are isomorphic by uniqueness in Proposition 4.13.
Before we develop further this categorical structure, we introduce a few useful lemmas.
4.2.6. Immediate causality in interactions. Later on, we will need some tools to reason on
the causality in τ f σ and how it relates to that in σ and τ .
Lemma 4.21. For σ : A $ B, τ : B $ C causal prestrategies, for m, m1 P |τ f σ|, if
m _τ fσ m1 , then mσ _σ m1σ , or mτ _τ m1τ , where mσ , mτ are defined whenever used.
The proof is in Appendix D.3. So in the event-based view of interaction, immediate
causal links originate in one of the components. For σ and τ strategies, one can track down
the responsible component via a polarity analysis. Of course, it is usual in game semantics
that events of τ f σ cannot sensibly be assigned a polarity in t´, `u, because σ and τ
disagree on B. A more useful notion of polarity is polτ fσ : |τ f σ| Ñ t´, l, ru given by:
polτ fσ pmq “ l
polτ fσ pmq “ r
polτ fσ pmq “ ´

if mσ is defined and polσ pmσ q “ `,
if mτ is defined and polτ pmτ q “ `,
otherwise.

As an example, we show in Figure 35 the polarities arising from this definition. Then:
Lemma 4.22. Consider σ : A $ B and τ : B $ C strategies, and m _τ fσ m1 . Then,
(1) if polτ fσ pm1 q “ l, then mσ _σ m1σ ,
(2) if polτ fσ pm1 q “ r, then mτ _τ m1τ ,
(3) if polτ fσ pm1 q “ ´, then Bτ fσ pmq _A∥B∥C Bτ fσ pm1 q .

Proof. (1) By Lemma 4.21, mσ , m1σ defined and mσ _σ m1σ – in which case we are done;
or mτ , m1τ defined and mτ _τ m1τ . Since polτ fσ pm1 q “ l, polτ pm1τ q “ ´. By courtesy,
Bτ pmτ q _B$C Bτ pm1τ q; hence m occurs in B and Bσ pmσ q _A$B Bσ pm1σ q. By Lemma A.2,
mσ ăσ m1σ , and the causality must be immediate by Lemma D.12. (2) is symmetric.
(3) Assume m1 occurs in A, the other case is symmetric. In that case only m1σ is defined,
so Lemma 4.21 entails that mσ is defined and mσ _σ m1σ . But polσ pm1σ q “ ´, so by
courtesy Bσ pmσ q _A$B Bσ pm1σ q, from which the conclusion follows.
4.3. Seely Category. Now, we turn to the different components of a Seely category.

## PDF page 48

24:48

Vol. 20:3

S. Castellan and P. Clairambault

$

U

U
q´

q` pw

b

U

⊸

U

U

q´

q´

u} 2(

q` pw

_

vs

✓´

b

U

✓`

 '. ✓`

U

q´

t| 0(

q` pw

_

and

✓´
 "*

⊸

U

b

U

q´

q´

✓`

 '. ✓`

t| 0(

_

✓´
 #+

✓`

 #+

 '. ✓`

Figure 36: Non-uniqueness of the threading pointer
4.3.1. Symmetric monoidal category with products. On ´-arenas, we keep the definitions for
Œ-Strat, enriched as in Section 4.1.2. The tensor of causal strategies is defined below:
Definition 4.23. For σ 1 : A1 $ B1 , σ 2 : A2 $ B2 causal strategies between ´-arenas, then
σ 1 b σ 2 : A1 b A2 $ B 1 b B 2
is defined as the ess σ 1 ∥ σ 2 along with display map Bσ1 bσ2 pi, sq “ pj, pi, aqq if σ i psq “ pj, aq.
Bifunctoriality is direct via Proposition 4.13. The symmetric monoidal structural
isomorphisms are provided by copycat strategies, only changing display maps:
αA,B,C : pA b Bq b C – A b pB b Cq
sA,B :
AbB – BbA

ρA : A b 1 – A
λA : 1 b A – A

satisfying up to positive iso the expected naturality and coherence laws [CCW19]. For
cartesian products, the projections π 1 : A1 & A2 $ A1 and π 2 : A1 & A2 $ A2 are relabeled
copycat strategies, while the pairing of causal strategies is defined similarly to the tensor:
Definition 4.24. Consider σ 1 : A $ B1 and τ : A $ B2 causal strategies between ´-arenas.
Then, xσ 1 , σ 2 y : A $ B1 & B2 is defined as having ess σ 1 & σ 2 , along with
Bxσ1 ,σ2 y pi, sq “ p1, aq
Bxσ1 ,σ2 y pi, sq “ p2, pi, bqq

if Bσi psq “ p1, aq
if Bσi psq “ p2, bq.

It follows from Proposition 4.13 and direct verifications that this yields binary products.

4.3.2. Monoidal closed structure. We now describe the monoidal closure.
On objects, the closure is the arrow A ⊸ B from Œ-Strat. However, for now, the
strategies on A $ B and on A ⊸ B are not in one-to-one correspondence. Indeed strategies
in A ⊸ B include a pointer for initial moves in A, while strategies in A $ B do not. This
pointer is not always unique, as illustrated in Figure 36. To cope with this we could have,
as for the play-based strategies of the previous sections, set the morphisms of our category
directly as strategies on A ⊸ B; but in this causal setting that obfuscates composition.
Instead, we restrict to strategies for which this pointer reconstruction is unique:
Definition 4.25. A causal strategy σ : A on arena A is pointed if for each s P |σ| there is
a unique event initpsq P |σ| which is minimal for ďσ and such that initpsq ďσ s.

## PDF page 49

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:49

Copycat strategies are pointed (as arenas are forestial), and pointed strategies are stable
under composition and the other operations on strategies. From now on, we consider that all
causal strategies are pointed. We write _-Strat for the category having ´-arenas as objects,
and as morphisms from A to B, the pointed causal strategies on A $ B.
For pointed strategies, the missing pointer can always be recovered uniquely:
Lemma 4.26. Let A, B and C be ´-arenas. Then, we have a bijection:
ΛA,B,C

:

_-StratpA b B, Cq

»

_-StratpA, B ⊸ Cq

Proof. The bijection only affects the display map, leaving the other components unchanged.
The non-trivial direction is from left to right. Consider σ : A b B $ C. We set:
$
if Bσ psq “ p1, p1, aqq,
& p1, aq
p2, p2, cqq
if Bσ psq “ p2, cq,
BΛpσq psq “
%
p2, p1, pc, bqqq
if Bσ psq “ p1, p2, bqq and Bσ pinitpsqq “ p2, cq.
It is a direct verification that this yields a bijection as claimed.
From this point, we may now easily wrap up the symmetric monoidal closed structure.
Proposition 4.27. The category _-Strat is symmetric monoidal closed.
Proof. First, for any ´-arenas A and B, we have A ⊸ B and an evaluation
evA,B “ Λ´1
A⊸B,A,B pccA⊸B q : pA ⊸ Bq b A $ B ,
and given σ : A b B $ C, evB,C d pΛA,B,C pσq b Bq « σ follows from a variation over the
neutrality of copycat for composition. From there, the universal property is routine.

4.3.3. The exponential. The first step is to introduce a functor ! : _-Strat Ñ _-Strat.
Definition 4.28. Consider A and B two ´-arenas, and σ : A $ B a causal strategy.
We define a strategy !σ : !A $ !B with !σ as event structure with symmetry and:
"
p1, pi, aqq
if Bσ pmq “ p1, aq,
B!σ pi, mq “
p2, pi, bqq
if Bσ pmq “ p2, bq.
It is a direct verification that this defines a causal strategy, and functoriality is proved
as for the tensor product of strategies. To complete the categorical structure, we have:
Proposition 4.29. The category _-Strat is a Seely category.
Proof. The structure presented above is completed by structural natural families of strategies:
digA : !A Ñ !!A
derA : !A Ñ A

mon2A,B : !A b !B – !pA & Bq
mon0 :
1 – !1 .

making p!, dig, derq a comonad along with the Seely isomorphisms. Those are all relabeled
copycat strategies: for instance, digA is cc!!A relabeled on the left hand side following a
bijection N ˆ N » N, derA is ccA relabeled to set events on the left hand side to copy index 0,
etc. The naturality and coherence are easily verified, exploiting again Proposition 4.13.

## PDF page 50

24:50

S. Castellan and P. Clairambault

Vol. 20:3

4.3.4. Extracting plays. In Section 4.1.4, we unfolded causal strategies to non-alternating
strategies. Here, we show that this is compatible with the categorical operations.
First, we extend the definition in Proposition 4.4 for causal strategies from A to B.
Definition 4.30. For A and B two ´-arenas, and σ : A $ B a causal strategy, we define
ö-Unfpσq “ BΛpσq pö-Playspσqq P ö-StratpA, Bq
exploiting that σ and Λpσq only differ via their display map.
This matches applying Proposition 4.4 to Λpσq : A ⊸ B obtained by monoidal closure.
Proposition 4.31. There is a symmetric monoidal closed ö-Unfp´q : _-Strat Ñ ö-Strat.
Proof. For identities, the definition of plays of the asynchronous copycat (Definition C.4)
follows the characterisation of configurations of ccA found e.g. in Lemma 3.11 in [CCRW17].
For composition, take σ : A $ B and τ : B $ C. Though τ f σ is not an esp, Definition
3.18 generalizes transparently to ö-Playspτ f σq. There are two inclusions to check:
ö-Unfpτ d σq Ď ö-Unfpτ q d ö-Unfpσq: any s P ö-Unfpτ d σq has the form BΛpτ dσq ptq
for t P ö-Playspτ d σq, which in turn can be completed to v P ö-Playspτ f σq. Then v may
be displayed to u P ö-Unfpτ q f ö-Unfpσq, witnessing s P ö-Unfpτ q d ö-Unfpσq.
ö-Unfpτ q d ö-Unfpσq Ď ö-Unfpτ d σq: any s P ö-Unfpτ q d ö-Unfpσq has a witness
u P ö-Unfpτ q f ö-Unfpσq, projecting to u æ A, B P ö-Unfpσq and u æ B, C P ö-Unfpτ q.
Those are respectively BΛpσq psσ q and BΛpτ q psτ q for sσ P ö-Playspσq and sτ P ö-Playspτ q.
Then xσ :“ |sσ | and xτ :“ |sτ | are causally compatible as u induces a linearization of the
corresponding bijection. By construction, xτ f xσ has a linearization v that displays to u;
and its restriction to visible events yields t P ö-Playspτ d σq that displays to s.
The preservation of the monoidal structure is direct; the functor is strict monoidal.
As ö-Strat does not handle symmetry, it supports no equivalence relation corresponding
to «. Nevertheless, this lets us import the stability of well-bracketing under composition.
We first generalize Definition 4.5 to well-bracketed causal strategies between ´-arenas:
Definition 4.32. Consider ´-arenas A, B, and σ : A $ B a causal strategy.
We say that σ : A $ B is well-bracketed iff ö-Unfpσq is well-bracketed.
From Propositions 3.22 and 4.31, there is an smcc with products _-Stratwb of ´-arenas
and well-bracketed causal strategies. Finally, !p´q preserves well-bracketing and the other
components for the exponential are well-bracketed, so _-Stratwb extends to a Seely category.
4.4. Interpretation of IA . We now describe the interpretation of IA in _-Stratwb
! . First
the types of IA are the same as those of IA; their interpretation does not change.

4.4.1. Interpretation of core PCF. We focus on the core PCF primitives, postponing let.
The λ-calculus primitives are interpreted following the cartesian closed structure of
_-Stratwb
! . For constants, we use the obvious strategies returning the corresponding value.
For basic PCF combinators, there are obvious causal strategies corresponding to Figures 12
and 14. For recursion, we must first define a partial order on causal strategies:

## PDF page 51

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:51

!ppX & Xq & ppX & Xq Ñ Yqq $ Y

!ppX & Xq & ppX & Xq Ñ Yqq $ Y

q´

q´

` ou %

q0

q1

_

_

v0´

nt
q`
0

` ov &

_

v0´

#

nu
q`
1

$

_

w1´

w1´
q´
3,i
_

`
v3,i

Figure 37: The prestrategy forcev,w

qx )

q´
3,j

 (/)0 q`
_3
u~ 3

_

u´
3

`
w3,j

 '

u`

Figure 38: The strategy pletX,Y

Definition 4.33. Consider A an arena, and σ, τ : A causal (pre)strategies.
We write σ Ĳ τ iff C pσq Ď C pτ q – so |σ| Ď |τ | as well – with, additionally:
(1)
(2)
(3)
(4)

for all s1 , s2 P |σ|, s1 ďσ s2 iff s1 ďτ s2 ,
for all s1 , s2 P |σ|, s1 #σ s2 iff s1 #τ s2 ,
for all x, y P C pσq and bijection θ : x » y, we have θ P S pσq iff θ P S pτ q,
for all s P |σ|, Bσ psq “ Bτ psq,

i.e. all components compatible with the inclusion.
Causal strategies on A, ordered by Ĳ, form a directed complete partial order ; however
without a least element. Indeed, strategies minimal for Ĳ still have – by receptivity – events
corresponding to the minimal events of A, but those are named arbitrarily. We solve this
as in [CCW19]: we choose one minimal causal strategy KA : A with events exactly those
negative minimal in A; induced causality, conflict, and isomorphism family; and as display
map the identity. For any σ : A, we pick σ 5 – σ : A such that KA Ĳ σ 5 , obtained by
renaming minimal events. We write DA for the pointed dcpo of causal strategies above KA .
All operations on strategies examined so far are continuous. So, the operation
F

: D1$pAÑAqÑA Ñ D1$pAÑAqÑA
σ ÞÑ pλf AÑA . f pσ f qq5 ,

in λ-calculus syntax following the cartesian closed structure of _-Stratwb
! , is continuous.
Thus it has a least fixed point YA P D1$pAÑAqÑA , i.e. such that YA “ F pYA q.
4.4.2. Interpretation of let. We give the interpretation of parallel let, as
ˆ
˙
x1 “ N1
JΓ $ let
in M : YK “ pletX,Y d! xJN1 K, JN2 K, Λ!X&X pJM Kqy .
x2 “ N2
where pletX,Y P _-Stratwb
! pX & X & ppX & Xq Ñ Yq, Yq first evaluates its two arguments X in
parallel. Once they both terminate on v and w, it calls its function argument, with xv, wy.
More formally, we first define a prestrategy “forcing” evaluation to v, w, i.e.
forcev,w : !pX & X & ppX & Xq Ñ Yqq $ Y
as in Figure 37 – only a prestrategy, not receptive to other values. Likewise,

## PDF page 52

24:52

Vol. 20:3

S. Castellan and P. Clairambault

r´
8

w4´
2

w6´
2

g0´

g1´

0`
8

✓`
2

✓`
2

✓`
0

✓`
1

_

_

r´
8
_

4`
8

x ;

_

w6´
3

_

_

 '

_

✓`
3

_

_

w7´
4

rl´
2

✓`
4

✓`
2

_

_

Figure 39: Beginning of cell0

Figure 40: Beginning of lock0

evalv,w : !pX & X & ppX & Xq Ñ Yqq $ Y
is defined by first using the cartesian closed structure of _-Stratwb
! to obtain a strategy
λxx1 , x2 , f y. f xv, wy P _-Stratwb
! pX & X & ppX & Xq Ñ Yq, Yq ,

evaluating f on xv, wy, from which evalv,w is obtained simply by removing the initial q´ . Up
to reindexing, we assume evalv,w does not use copy indices 0 and 1 on the calls to context.
Finally, this lets us define plet via the expression (the supremum refers to Ĳ):
ł
pletX,Y “
forcev,w ¨ evalv,w P _-Stratwb
! pX & X & ppX & Xq Ñ Yq, Yq
v,wPX

where the concatenation ¨ sets both maximal (negative) events of forcev,w as dependencies
for evalv,w . The full strategy is represented in Figure 38. Unlike for Figure 37, the picture
in Figure 38 is to be read as a symbolic representation. The concrete strategy pletX,Y has
patterns as in Figure 38 for all concrete values for v, w, u and copy indices i and j.
The interpretation of the sequential let can be obtained as a simplification.

4.4.3. Interpretation of interference. Now, we interpret shared state and semaphores. By
and large, it closely follows the sequential interpretation of Sections 3.4.2 and 3.4.3.
For the primitives interacting with memory and semaphores, we use the same definitions
as in Section 3.4.2, with the obvious causal strategies matching Figures 24, 25, 26, and 27.
For new references, we regard the alternating strategy celln from Section 3.4.3 as a
(sequential) event structure: its events |celln | are the non-empty plays, the causal order is
given by prefix, the conflicting pairs are all non-comparable plays. The display map
Bcelln

: |celln | Ñ !ref
sa ÞÑ a

keeps the last move. As configurations are sets of prefixes of a given play, we set S pcelln q
to comprise those bijections induced by plays s1 –A s2 symmetric on A (see Definition 2.11).
We display in Figure 39 a few early moves of cell0 , with the convention that all moves
in the same row are in pairwise conflict. In this diagram we observe that cell0 fails courtesy:
´
indeed, the immediate causal link ✓`
2 _ r8 , for instance, would be illegal for a strategy.
Note that although celln : !ref is only a prestrategy and not a strategy, we have:
Proposition 4.34. For all σ : !ref $ A, for all n P N, σ d celln : A is a strategy.

## PDF page 53

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:53

Proof. First, „-receptivity is established directly, exploiting that σ and celln do not have
non-courteous immediate causal links accross components – they are componentwise courteous
in the sense of [CCW19]. Lemma 3.36 from [CCW19] ensures that σ d celln is „-receptive.
It remains to prove σ d celln receptive and courteous. But those properties are
independent of symmetry. Without symmetry, strategies are exactly those prestrategies
invariant (up to iso) under composition with copycat [CCRW17]. But then, we compute:
ccA d pσ d celln q – pccA d σq d celln
– σ d celln ,
so by Theorem 3.20 of [CCRW17], σ d celln is receptive and courteous as required.
For semaphores, we obtain a prestrategy lockn : !sem for each n P N using essentially
the same recipe, taking as events all non-empty plays that are prefixes of an even-length
play. A beginning of lock0 is displayed in Figure 40.
The interpretation of new references and semaphores is defined as in Section 3.4.3.
4.5. Adequacy. Adequacy could be deduced from the connection with [GM08] – see
Section 4.6.2. Instead we give an independent proof, as we believe it helps build the
operational intuitions for the model. Rather than as usual relying on logical relations, we
follow an alternative route, proving first adequacy for certain finitary terms in which the
correspondence between operational and game semantics is more concrete.
4.5.1. Canonical adequacy. The sharpest link between operational and game semantics holds
factoring out recursion, higher-order, and dynamic generation of semaphores or references.
We temporarily extend IA with an explicit KA : A for every type A, interpreted by a
minimal strategy with no Player move. Take Σ an interference context, i.e. of the form
Σ “ ℓ1 : ref , . . . , ℓi : ref , ℓi`1 : sem, . . . , ℓn : sem ,
and Σ $ M : X where X P tU, B, Nu. We say M is in canonical form if it contains no
fixpoint, subterm of higher type, bad references or semaphores, newref or newsem, with
no store-independent reductions available (other than the interfering reductions of Figure 2).
To help us link operational and denotational semantics for canonical forms, we introduce
a few concepts. First, if s is a store with dompsq “ Σ as above, we interpret it as
â
â
â
â
JsK “ p
cellspℓk q q b p
lockspℓk q q : p
!ref q b p
!semq – !JΣK .
1ďkďi

i`1ďkďn

1ďkďi

i`1ďkďn

To track evolution of an interaction we use the notion of residuals.
Definition 4.35. If E is an ess and x P C pEq, the residual E{x has
|E{x| “ te P |E|zx | @e1 P x, ␣pe #E e1 qu ,
e1 ďE{x e2 ô e1 ďE e2 ,
e1 #E{x e2 ô e1 #E e2 ,
θ : y –E{x z ô θ Y idx : x Y y –E x Y z .
If E has polarities they are preserved as well and for A an arena, A{x is an arena. In
particular for !JΣK, by definition and playing Hilbert’s hotel, for any x P C p!JΣKq with as
many Player as Opponent moves, we have p!JΣKq{x – !JΣK. Residuals also apply to causal
(pre)strategies: if σ : A, then for each x P C pσq, we have σ{x : A{Bσ pxq a prestrategy.

## PDF page 54

24:54

S. Castellan and P. Clairambault

Vol. 20:3

Take Σ $ M : X in canonical form. Necessarily JXK – also written X – has a unique
minimal move q´ and JM K has a unique matching minimal move, also written q´ . We set
LM M “ JM K{tq´ u : Σ $ LXM ,

where LXM “ JXK{tq´ u, yielding a causal prestrategy in the sense of Definition 4.3.
Now, we are equipped to state the most central ingredient of our proof of adequacy.
Lemma 4.36. Consider Σ $ M : X in canonical form, and s a store with dompsq “ Σ.
Then, there is a (necessarily interfering) one-step reduction
xM, sy ⇝ xM 1 , s1 y
iff there are matching x P C pLM Mq and y P C pJsKq with two elements each, such that
LM M{x « LM 1 M : !JΣK $ LXM ,

JsK{y « Js1 K : !JΣK .

Proof. For interfering operations ℓ :“ v, !ℓ, grabpℓq or releasepℓq, it is a direct verification
by definition of the interpretation. The result then follows by induction on M .
This identifies store operations that a canonical M may perform immediately with
store s, with the minimal events of LM M f JsK that occur in Σ. It almost suffices to iterate
this to obtain adequacy for canonical terms; however interfering reductions might yield
non-canonical terms, so state operations must be interleaved with pure reductions. Write
M Ź N for pure reductions, i.e. the context closure of interference-independent reductions in
Figure 2 – these reductions leave invariant the interpretation as causal strategies. Moreover:
Lemma 4.37. Consider Σ $ M : X without fixpoint, subterm of higher type, bad references
or semaphores, newref or newsem. Then, there exists Σ $ N : X canonical with M Ź˚ N .
Moreover, for any store s with dompsq “ Σ, there is xM, sy ⇝˚ xskip, s1 y iff there is
xN, sy ⇝˚ xskip, s1 y, and the correspondence preserves the number of interfering operations.
Proof. A routine standardization argument.
Using this, we can prove adequacy for canonical terms. Intuitively, a sequence xM, sy ⇝˚
xskip, s1 y can be reproduced semantically: each interfering reduction yields by Lemma 4.36
a pair of events in LM M f JsK, while state-free reductions leave the interpretation unchanged.
Reciprocally, a successful interaction in LM M d JsK is a partially ordered set of memory
operations, which may be linearized by securedness; informing a reduction sequence.
Proposition 4.38. Consider Σ $ M : U in canonical form, and s a store with dompsq “ Σ.
Then, xM, sy ⇝˚ xskip, s1 y iff LM M d JsK has a positive move.

Proof. If. Taking x d y P LM M f JsK, we build the sequence by induction on the size of x f y.
If x f y has exactly one event, it must match ✓` in LUM. Since M is canonical, by a
case inspection on the shape of M , the only case for which LM M has a minimal positive event
in LUM is a value skip. Otherwise, since x and y are causally compatible, there is a sequence
pH, Hq ´Ă px1 , y1 q ´Ă . . . ´Ă pxn , yn q “ px, yq

of one-step extensions (for the product inclusion order) of matching xi P C pLM Mq and
yi P C pJsKq, obtained by linearization from the acyclicity of causal compatibility of x and y.
´
In particular, x1 “ tm`
1 u and y1 “ tn1 u singleton sets. By Proposition 4.13, y is `-covered,
`
so there is a (unique, by definition of JsK) n´
1 _JsK n2 , and by Lemma A.5 there is a unique
´
matching m`
1 _LM M m2 . Since n2 only depends on n1 and m2 only depends on m1 , w.l.o.g.

## PDF page 55

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

pnewref x:“ n in M q; N
M ; pnewref x:“ n in N q
if pnewref x:“ n in M q N1 N2
if N1 pnewref x:“ n in M q N2
if N1 N2 pnewref x:“ n in M q
let y “ pnewref x:“ n in M q in N
let y “ M in pnewref x:“ n in N q
f pnewref x:“ n in M q

Ñ
Ñ
Ñ
Ñ
Ñ
Ñ
Ñ
Ñ

newref x:“ n in M ; N
newref x:“ n in M ; N
newref x:“ n in if M N1 N2
newref x:“ n in if N1 M N2
newref x:“ n in if N1 N2 M
newref x:“ n in plet y “ M in N q
newref x:“ n in plet y “ M in N q
newref x:“ n in pf M q

24:55

px R fvpN qq
px R fvpM qq
px R fvpNi qq
px R fvpNi qq
px R fvpNi qq
px R fvpN qq
px R fvpM qq

where f P tsucc, pred, iszerou.
Figure 41: Commutation rules for newref
x2 “ tm1 , m2 u and y2 “ tn1 , n2 u. So, by Lemma 4.36, there is a one-step xM, sy ⇝ xM 1 , s1 y
s.t. LM M{x2 « LM 1 M and JsK{y2 « Js1 K. We may now use Lemma 4.37 to obtain M 1 Ź˚ M 2
with M 2 canonical and LM 1 M « LM 2 M. Now, removing x2 and y2 to the sequence above yields
pH, Hq ´Ă px13 , y31 q ´Ă . . . ´Ă px1n , yn1 q “ px1 , y 1 q

with x1 “ xztm1 , m2 u and y 1 “ yztn1 , n2 u, witnessing that matching x1 P C pLM 2 Mq and
y 1 P C pJs1 Kq are causally compatible, so that x1 f y 1 P C pLM 2 M f Js1 Kq. But x1 and y 1 are `covered, so x1 dy 1 P C pLM 2 MdJs1 Kq, still with a positive move in U. So xM 2 , s1 y ⇝˚ xskip, s2 y
by induction hypothesis, so xM 1 , s1 y ⇝˚ xskip, s2 y by Lemma 4.37, so xM, sy ⇝˚ xskip, s2 y.
Only if. By induction on the number of interfering operations in xM, sy ⇝˚ xskip, s2 y.
If M “ skip it is immediate. Otherwise, consider xM, sy ⇝ xM 1 , s1 y ⇝˚ xskip, s2 y. By
Lemma 4.36, there are x P C pLM Mq and y P C pJsKq matching with two elements each, with
LM M{x « LM 1 M

JsK{y « Js1 K .

x1 P C pLM 2 Mq ,

y 1 P C pJs1 Kq ,

Now, to use the induction hypothesis we convert M 1 Ź˚ M 2 to canonical form; by Lemma
4.37 we have xM 2 , sy ⇝˚ xskip, s2 y with the same number of interfering operations; and
LM 1 M « LM 2 M. So by induction hypothesis, there are `-covered and causally compatible
where x1 has an occurrence of the positive event of U; so up to renaming, x1 P C pLM M{xq
and y 1 P C pJsK{yq. Therefore, by definition of residuals, one may add back x and y to obtain
x Y x1 P C pLM Mq ,

y Y y 1 P C pJsKq ,

`-covered, causally compatible with a positive move in U, which concludes the proof.

4.5.2. Finitary adequacy. We deduce recursion-free adequacy from the canonical case.
To convert terms to canonical form, we perform state-free reductions while pushing
declarations of new references or semaphores outside. The latter is done by the commutation
rules of Figure 41, from which are missing the three rules for the parallel let, and matching
commutations for new semaphores. It is direct that these rules leave the game semantics
invariant, and preserve and reflect infinite reduction chains in the operational semantics.
Writing ” for the congruence closure of state-free reductions and commutations above:

## PDF page 56

24:56

S. Castellan and P. Clairambault

Vol. 20:3

Lemma 4.39. Consider $ M : X a recursion-free term of IA . Then, there exists
M ” new x1:“ n1 in . . . new xp:“ np in N
where each new is either newref or newsem, and Σ $ N : X is canonical.
Proof. Consider the reduction Ñ comprising the (context closure of) the commutations above
with β-reduction and the state-free reductions for mkvar and mksem. Treating ref and
sem as product types, it is easy to prove from the strong normalization of the simply-typed
λ-calculus with products that Ñ terminates. Moreover, as M has type X P tU, B, Nu, a
Ñ-normal form M Ñ˚ M 1 has no abstraction, bad variable or semaphore subterm. Thus
M 1 “ new x1:“ n1 in . . . new xp:“ np in N 1
with Σ $ N 1 : X without recursion, subterm of higher type, bad reference or semaphores,
and reference and semaphore initialization. Finally, we conclude by Lemma 4.37.
The semantics enjoy finitary adequacy:
Proposition 4.40. For any recursion-free $ M : U, we have M ó iff JM K ó.
Proof. Immediate consequence of Proposition 4.38 and Lemma 4.39.

4.5.3. Deducing adequacy. Finally, we extend the above with recursion.
Theorem 4.41 (Adequacy). For $ M : U any term of IA , M ó iff JM K ó.
Proof. As expected, we simply reason by continuity. For all type A and n P N, we set
YA0 “ λf AÑA . KA

YAn`1 “ λf AÑA . f pYAn f q ,

yielding $ YAn : pA Ñ Aq Ñ A. The n-th approximation Γ $ Mn : A of any term
Γ $ M : A of IA is obtained by replacing each Y N with Yn N . It is then routine to show
that M ó iff there is n P N such that Mn ó. Likewise, by definition of theŽ
interpretation of
recursion (see Section 4.4.1) and continuity of the interpretation, JM K “ nPN JMn K. Now:
M ó ô Dn P N, Mn ó ,
ô Dn P N, JMn K has a positive move,
ô JM K has a positive move,

using the above along with Proposition 4.40.

This continuity argument only works for may-convergence: for extensions such as
must or fair -convergence we would have to formulate a more complete correspondence
between operational and game semantics – see e.g. [Cas17] for an adequacy result for
non-deterministic PCF w.r.t. must-convergence. However, we leave this out of this paper.

4.6. Full Abstraction. Now that we have established _-Strat as an adequate model of
IA , we explore a bit further its observable operational content and prove full abstraction.

## PDF page 57

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

Ñ

U

Ñ

U

U

pU Ñ

24:57

Ñ Uq Ñ

U

U

q´
q` nu
_

✓´

$

q` ov

&

q´

_

✓´

q`
 #+ `
q
_

✓

q´ pw

´

 %,

✓

`

λxU y U . newref r:“ 0 in
Figure 42:
assume piszero !rq; x; r:“ tt
∥ assume pnot piszero !rqq; y

_

✓

`

(

t|
q´
 '

K

✓

`

0
s

✓`

w 7

_

✓´
 (

✓`

λf UÑUÑU . newref r:“ 0 in
Figure 43:
f pr :“ 1q
pskip > passume !rqq

4.6.1. Observable behaviour of causal strategies. It is clear that without quotient, the interpretation of IA in _-Strat will not be fully abstract: the model records very intensional
information that is typically not observable. We give two examples in Figures 42 and 43.
We introduce a few additional pieces of syntactic sugar. First, assume : B Ñ U is
B
λx . if x skip K which terminates on tt and diverges otherwise. We also define not : B Ñ B
as the obvious program. Finally, for any Γ $ M : A and Γ $ N : A of IA , we set
M > N “ newref x :“ 0, y :“ 0 in
px :“ 1 ∥ y :“!xq;
if piszero p!yqq M N
a non-deterministic sum Γ $ M > N : A, behaving non-deterministically as M or N .
First, Figure 42 represents the semantics of an encoding of sequential composition via
parallel composition plus shared state. In Ghica and Murawski’s model, this program has
the same interpretation as sequential composition, showing their equivalence with respect
to may-testing. In contrast, _-Strat also gives account of the limitation of this encoding:
the greyed out branch on the left corresponds to the bottom read winning the race, causing
divergence20. Likewise, Figure 43 also has an unobservable branch greyed out. The model
shows that the program may provide values for the two arguments of f independently, but
it may also provide a value for the second argument of f because f called its first argument.
In a play, an occurrence of ✓` corresponding to a value for the second argument may be
causally explained by either of the two moves, but the distinction is un-observable.
For full abstraction only the observable behaviour matters, and _-Strat clearly records
more than necessary. So we ask: what parts of a concurrent strategy are observable?
4.6.2. Non-alternating plays with pointers. We approach this question in terms which are
no surprise to the reader familiar with Ghica and Murawski’s non-alternating games: the
observable behaviour is exactly captured by certain non-alternating plays with pointers:
20This shows our model remembers some divergences, though not enough to get adequacy for must: some
divergences are lost through hiding. This can be addressed by tweaking hiding to retain those events dubbed
essential that carry divergences, see [CCHW18, Cas17] – but we shall not take this route in this paper.

## PDF page 58

24:58

S. Castellan and P. Clairambault

Vol. 20:3

Definition 4.42. A non-alternating play with pointers on A is a s1 . . . sn on |A| s.t.
negative: n ě 1 ùñ polps1 q “ ´ ,
with, for all 1 ď j ď n s.t. sj is non-minimal in A, a pointer to some earlier si such that
si _A sj . We write P-ö-PlayspAq for the set of non-alternating plays with pointers on A.

Ghica and Murawski’s model is an analogue of ö-Strat based on non-alternating plays
with pointers. A GM-strategy on meager A is a non-empty set of well-bracketed nonalternating plays with pointers (with well-bracketing defined as in Definition 3.20) satisfying
conditions analogous to Definition 3.19 (see Definitions 4 and 13 in [GM08]) and additionally
thread-independent (see Definition 17 of [GM08]). There is a cartesian closed category GM
of meager arenas and GM-strategies, supporting the interpretation of IA .
We shall build a functorial bridge between _-Strat and GM, as in Proposition 4.31, but
restricted to the cartesian closed structure as GM has no linear decomposition. We use the
concrete arenas of Section 2.20, extended in the obvious way with Question/Answer labeling.
The proof of Proposition 2.22 applies unchanged to prove:
Proposition 4.43. For any concrete arena A, there is an injective function
P : ö-PlayspAq{–

Ñ

P-ö-PlayspA0 q

preserving length, prefix, justifiers, and reflecting and preserving well-bracketing.
We consider the cartesian closed category _-Stratc with objects concrete arenas, obtained
from _-Stratwb
! by replacing all operations on arenas with those on concrete arenas.
Proposition 4.44. Consider concrete ´-arenas A, B, and σ P _-Stratwb
! pA, Bq. Then,
P-ö-Unfpσq “ tPpsq | s P ö-Unfpσ : q well-bracketedu

is a GM-strategy on A0 ⊸ B 0 . Moreover, P-ö-Unf extends to a cartesian closed functor
P-ö-Unf : _-Stratc Ñ GM

preserving the interpretation of IA .

Proof. We detail the two critical points: preservation of symmetry, and composition.
:
Symmetry. Consider σ, τ P _-Stratwb
! pA, Bq s.t. σ « τ . Then we also have Λpσ q «
Λpτ : q, i.e. there is an iso φ : σ : – τ : s.t. BΛpτ : q ˝ φ „` BΛpσ: q . Consider Ppsq P
P-ö-Unfpσq for some s P ö-UnfpΛpσ : qq. This means there is t P ö-Playspσ : q s.t. s “
BΛpσ: q ptq. But then, φptq P ö-Playspτ : q, and from BΛpτ : q ˝ φ „` BΛpσ: q it is direct that s “
BΛpσ: q ptq –A⊸B BΛpτ : q pφptqq. By Proposition 4.43, PpBΛpσ: q ptqq “ PpBΛpτ : q pφptqqq, so that
Ppsq P P-ö-Unfpτ q. The other inclusion is symmetric, so P-ö-Unfpσq “ P-ö-Unfpτ q.
wb
Composition. For σ P _-Stratwb
! pA, Bq, τ P _-Strat! pB, Cq, we must show
P-ö-Unfpτ d! σq “ P-ö-Unfpτ q d P-ö-Unfpσq ,

there are two inclusions to prove:
Ď. Consider Ppsq P P-ö-Unfpτ d! σq. Since P-ö-Unfp´q preserves positive isomorphism and by the laws of Seely categories, Ppsq P P-ö-Unfpτ : d σ : q for some
s P ö-Unfpτ : d σ : q. By Proposition 4.31, the latter is ö-Unfpτ : q d ö-Unfpσ : q. Now,
if u P ö-Unfpτ : q f ö-Unfpσ : q is a witness for s P ö-Unfpτ : q d ö-Unfpσ : q, then as σ : and
τ : are well-bracketed, it is direct that u æ A, B P ö-Unfpσ : q and u æ B, C P ö-Unfpτ : q are
well-bracketed as well. Therefore, Ppu æ A, Bq P ö-Unfpσ : q and Ppu æ B, Cq P ö-Unfpτ : q,
hence Ppuq is a witness in the sense of [GM08] for Ppsq P P-ö-Unfpτ q d P-ö-Unfpσq.

## PDF page 59

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:59

Ě. Consider now s P P-ö-Unfpτ q d P-ö-Unfpσq. There is a witness u, a sequence with
pointers on pA1 ⊸ B 1 q ⊸ C 1 , with restrictions u æ A1 , B 1 P P-ö-Unfpσq and u æ B 1 , C 1 P
P-ö-Unfpτ q – we refer to [GM08] for the definitions of restrictions of plays with pointers.
Write u æ A1 , B 1 “ Pptσ q and u æ B 1 , C 1 “ Pptτ q for tσ P ö-Unfpσ : q and tτ P ö-Unfpτ : q.
Though tσ and tτ yield plays with pointers compatible in B 1 , they might not match in B on
the nose. But by Proposition 4.43, tσ æ B –!B tτ æ B match up to symmetry. So, writing
tσ “ BΛpσ: q pv σ q

tτ “ BΛpτ : q pv τ q ,

for v σ P ö-Playspσ : q and v τ P ö-Playspτ : q, writing xσ “ |v σ | P C pσ : q and xτ “ |v τ | P
τ
C pτ : q the symmetry tσ æ B –!B tτ æ B induces θ : xσ
B –!B xB . Moreover,
xσ ∥ xτC

Bσ: ∥!C

»

σ
τ
xσ
A ∥ xB ∥ xC

!A∥θ∥!C

–

τ
τ
xσ
A ∥ xB ∥ xC

!A∥Bτ´1

»

τ
xσ
A ∥x ,

is secured, as u directly informs a total ordering of its graph compatible with σ : and τ : .
σ “ yτ .
Hence, by Proposition 4.16, there are φσ : xσ –σ: y σ and φτ : xτ –τ : y τ such that yB
B
σ
τ
σ
τ
σ
:
Transporting t and t through φ and φ , we get w P ö-Playspσ q and wτ P
ö-Playspτ : q s.t. we still have Ppwσ q “ u æ A1 , B 1 and Ppwτ q “ u æ B 1 , C 1 ; but this time
wσ æ B “ wτ æ B. Zipping them following u we obtain w P ö-Playspτ : q f ö-Playspσ : q such
that Ppw æ A, Cq “ s. But then w æ A, C P ö-Playspτ : q d ö-Playspσ : q by construction, so
in ö-Playsppτ d! σq: q by Proposition 4.31, hence s P P-ö-Unfpτ d! σq as required.
So there is a functorial unfolding from _-Strat to GM. To further factor out nonobservable behaviour, one can restrict to complete plays:
Definition 4.45. Consider A a meager ´-arena, and s P P-ö-PlayspAq.
We say that s is complete iff it is well-bracketed and all its questions have an answer.
If σ P _-Stratwb
! pA, Bq, comppσq is the subset of P-ö-Unfpσq comprising complete
plays only. The proposition above allows us to deduce (with „ defined in Section 3.3.2):
Proposition 4.46. Consider A concrete and σ, τ : A well-bracketed causal strategies. Then,
comppσq “ comppτ q

ùñ

σ„τ.

´ ` P
Proof. Consider α P _-Stratwb
! pA, Uq s.t. α d! σ ó. By Proposition 4.44, q ✓
P-ö-Unfpαq d P-ö-Unfpσq. Considering u P P-ö-Unfpαq f P-ö-Unfpσq, u æ A0 , U P
P-ö-Unfpσq. From well-bracketing of σ and α, u æ A0 is well-bracketed and complete, so
u æ A0 P comppτ q, so P-ö-Unfpαq d P-ö-Unfpτ q ó, so α d! τ ó by Proposition 4.44.

To prove the converse and link it to syntactic equivalence, we examine definability.
4.6.3. Definability of plays with pointers. As in Sections 3.3.2 and 3.4.4, full abstraction relies
on definability. While definability in IA rests on definability for finite innocent strategies,
Ghica and Murawski’s definability for IA gives directly terms realizing individual plays. For
conciseness we omit the full development, but illustrate it on a representative example.
Consider s on the left hand side of Figure 44. Naively, we want a term whose only
execution is s. But strategies satisfy courtesy, so one realizing s must also realize all
plays obtainable by adding asynchronous delays. The information from s that survives
asynchronous delays is that certain positive moves appear after earlier negative moves in s.
Together with the static causality from the arena, this yields a diagram as in the right hand

## PDF page 60

24:60

Vol. 20:3

S. Castellan and P. Clairambault

U1 Ñ pU2 Ñ U3 q Ñ U4 Ñ U5
q´
5
q`
1
q`
3
✓´
1
q´
2
q`
4
✓´
4
✓`
2

q´
5
q`
1

q`
3

`
3) 5>18 q4

✓´
1

q´
2

✓´
4

)

✓`
2

u~ 3

Figure 44: Example of definability of plays in IA
side of Figure 44, very much like a causal strategy. It is directly this diagram that Ghica and
Murawski’s finite definability reproduces. First, we ignore _-links and start with a term
λxU1 f U2 ÑU3 y U4 . px ∥ f skip ∥ yq; K ,

that performs all computational events available in s in a maximally parallel fashion, with
only causal dependency enforced by the game. The _-links are restored through the memory.
For that we define two helper functions. If M : ref , we write setpM q : U for M :“ 1, and
testpM q : U for assumepnotpiszero !M qq which converges iff !M is non-zero. Then:
¨
¨
˛ ¨
˛˛
´
´
f
psetpq
q;
testp✓
q;
2
1
ˆ
˙
´
‹‹
˚ x;
˚
‹ ˚
testp✓´
U1 U2 ÑU3 U4 ˚
4 q; ‹ ∥ ˚ testpq2 q; ‹‹ ; K
λx f
y .˝
∥˚
´
`
˝
‚‚
setp✓1 q
grabp✓2 q; ‚ ˝ y;
´
skipq
setp✓4 q
borrows the shape of the first term, signaling the _-links through memory. We use one fresh
reference (initialized to 0) for each Opponent move, which gets set to 1 when the Opponent
move occurs. Finally, we use semaphores to ensure that Opponent replications does not cause
a duplication of Player moves by prompting re-evaluation of the corresponding subterms –
so that we only obtain linearizations of the diagram on the right hand side of Figure 44.
Done systematically for arbitrary plays, this establishes [GM08]:
Proposition 4.47 (Ghica, Murawski). Consider A a type and s P P-ö-PlaysprAsq complete.
Then there is $ Ms : A Ñ U such that for all $ N : A,
s P JN KGM

ô

Ms N ó

In particular, as JN KGM is courteous, any t P JN KGM tracing a successful interaction with
Ms can be converted to s through permutations whose correctness is granted by courtesy.
Theorem 4.48. The model _-Stratwb
is intensionally fully abstract for IA .
!

Proof. Consider $ M, N : A. If JM K „ JN K, using Theorem 4.41, M „ N . Reciprocally,
assume M „ N . Seeking a contradiction, assume JM K ­„ JN K. By Proposition 4.46, there
is w.l.o.g. s P comppJM Kq where s R comppJN Kq. So, by Proposition 4.44, s P JM KGM while
s R JN KGM . Finally, by Proposition 4.47, we have Ms M ó while Ms N ò, contradiction.
As for Theorem 3.14, the resulting quotient is effective and easily described: for σ, τ : A,
σ„τ

ô

comppσq “ comppτ q .

## PDF page 61

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:61

Observational equivalence is undecidable even for the second-order fragment and without
recursion [GMO06]. Note also that without semaphores, full abstraction fails [Mur10] as
terms are closed under a stuttering behaviour which reduces their observational power.
4.7. Parallel Innocence and Sequentiality. We resume the discussion left at Section 3.6:
can we find parallel innocence and sequentiality disentangling parallelism and interference?
A subtlety is that while IA is non-deterministic, PCF and IA are both deterministic –
albeit in different senses. Non-determinism arises in IA from the interaction of parallelism
and interference so, removing either of these causes, determinism has to be reimposed as
well. Accordingly, sequentiality and parallel innocence will include determinism.
5. Parallel Innocence
We capture the causal patterns definable with pure parallel higher-order programming.
5.1. Causal determinism. The sense in which PCF is deterministic is fairly different
from Definition 2.8. For instance, after the first Opponent move, the strategy of Figure 38
has two available Player moves; but the order in which these moves are played does not
matter and will eventually reach the same result: the program is deterministic up to the
choice of the scheduler. If E is an event structure, write ConE for the set of finite consistent
sets of events, i.e. for X Ďf |E|, X P ConE iff for all e1 , e2 P X, we have ␣pe1 #σ e2 q.
We use Winskel’s definition of determinism for concurrent strategies [Win12]:
Definition 5.1. A causal strategy σ : A on arena A is causally deterministic if:
causal determinism: assume X Ďf |σ| is negatively compatible,
i.e. X´ “ ts P X | polσ psq “ ´u P Conσ . Then, X P Conσ .
This ensures that Player branching only spawns parallel threads: only Opponent may
initiate conflict. Copycat is deterministic, and deterministic strategies compose [Win12]. All
other constructions in the Seely category structure of _-Strat preserve determinism.
5.2. Parallel Innocence. What causal shapes are distinctive of pure parallel computation?
5.2.1. Pre-innocence. Pure parallel programs may spawn parallel threads, which must remain
independent in the absence of interference. Once they both terminate the program may take
new actions that depend on their results, causally “merging” them. A typical causal strategy
featuring this behaviour, for x : U, y : U $ x ∥ y : U, appears in Figure 46. The slogan is:
“Player may merge threads that he himself has spawned”.
In contrast, both diagrams of Figure 32 bear signs of interference. In the first, the answer
1` depends on q´ : the program somehow observes if the function has called its argument,
which is only possible if the argument performs some side-effect that the program observes.
In the second, ✓` depends on ✓´ ; but likewise this can only occur if the termination of the
function triggers a side-effect. In both cases, this is witnessed by Player “merging” causal
chains which forked at Opponent moves. To ban such interference, the slogan is:
“Player may not merge threads spawned by Opponent”.
To define parallel innocence, our first step is to introduce a formal notion of “thread”:

## PDF page 62

24:62

¨

Vol. 20:3

S. Castellan and P. Clairambault

pU

⊸

˚
˚
˚
˚
gcc ˚
˚
2
˚
˚ q´ u}
˝ _

⊸

Uq

˛

N

‹

q`

u~ 3

q´ ‹
‹

_

✓



´

 !)'. 1`

✓`

$
pU ⊸ Uq ⊸ N
’
’
’
’
’
’
q´
’
’
&
3

‹
‹ Ě
‹
’
3
‹
’
’
´ u~
‹
’
’
q
’
‚
_
’
’
% 

q`

u~

pU ⊸ Uq ⊸ N

,
u~
q´

3

q`

u~ 3

pU ⊸ Uq

q´

,

q`

⊸

u~ 3

_

✓´
 &- 1`

✓`

,
N /
/

/
/
/
.

q´ /
/
/

/
/
/
/
/
/
/
!* ` /
1 -

Figure 45: Maximal grounded causal chains of a causal strategy
!pU

&

$

Uq

!pU

U

&

∥

Uq

U

q´
pw
q`
0
_

✓´
0

'

q`
1

q´

s{ /

qr0 ov
_

_

✓l0

✓´
1

&

qr1
 $,

sz -

_

✓l1

 #+(/ `
✓

 $,)/ ✓r

Figure 46: A typical pre-innocent strategy

Figure 47: Partiality of views

Definition 5.2. Consider A an arena, and σ : A a causal strategy.
A grounded causal chain (gcc) in σ is ρ “ tρ1 , . . . , ρn u Ď |σ| forming
ρ1 _σ . . . _σ ρn

a chain with ρ1 minimal with respect to ďσ . We write gccpσq for the gccs in σ.
A gcc is just a set, but we write ρ “ ρ1 _σ . . . _σ ρn P gccpσq to insist on the causal
ordering inherited from ďσ . If also ρ1 _σ . . . _σ ρn _σ m P gccpσq, then we write
ρ _ m “ ρ Y tmu. Gccs are not necessarily down-closed: we show in Figure 45 all maximal
gccs of a causal strategy. Of those, the second and third omit some dependencies of 1` .
We may now make formal the idea of a strategy “only merging threads forked by Player”.
Definition 5.3. Consider A an arena. A causally deterministic σ : A is pre-innocent iff
pre-innocence: If m` P |σ| and ρ1 _ m, ρ2 _ m P gccpσq are distinct,
then their least distinct moves are positive.
As causal strategies are pointed, ρ1 and ρ2 necessarily share the same initial move.
The strategy of Figure 46 is pre-innocent. In contrast, that of Figure 31 is not – both
augmentations of Figure 32 fail pre-innocence. For instance, the second and third gccs of
Figure 45 arrive at 1` but before that, the greatest common event is q` , which is positive:
Player is merging (via 1` ) two gccs forked by Opponent, which is forbidden by pre-innocence.
It will follow later on that the sequential pre-innocent causal strategies exactly match
the standard alternating innocent strategies of Definition 3.6: sequentiality entails that there
is no Player branching. Thus separate branches always correspond to threads spawned by
Opponent, which by pre-innocence cannot interfere. The causal structure is then a forest,
matching that of P-views of Section 3.2. We postpone the details to Section 6.3.
However, it turns out that pre-innocence is incomplete for parallel strategies.

## PDF page 63

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

¨
pU

⊸

Uq

q`
_

✓`

t} 1

✓´

⊸

u~ 3

N
q´
P

24:63

˛

˚ pU ⊸ Uq ⊸ N ‹
‹
˚
‹
˚
´
˚
q ‹
‹
˚
‹
˚
u~ 3
gcc ˚
‹
`
q
‹
˚
_
‹
˚

‹
˚ ´ u} 2
´
‹
˚ q
✓
‚
˝ _ 1
}
t
)
!
`
`
✓
0

Figure 48: A gcc of a non-visible strategy, losing its pointer
5.2.2. Visibility. The problem arises as non-stability of pre-innocence under composition. A
counter-example appears in Figure 49, examined when proving compositionality of innocence.
But we can explain the issue intuitively: the definition of pre-innocence relies on gccs
which formalize a notion of thread. If that intuition is to be taken seriously, gccs should
be valid executions of standalone sequential programs. But this is not the case: Figure 48
shows a gcc where the last move answers a question that was not asked within this gcc. This
could not be a valid state of a sequential program, because the last move loses its pointer.
Visible strategies are simply those such that this does not happen.
Definition 5.4. A causal strategy σ : A is visible if for all ρ P gccpσq, Bσ pρq P C pAq.
In other words, every move in ρ points within ρ. This phrasing highlights the analogy
with Definition 3.5, i.e. “Player always points in the P-view”. It is indeed this analogy that
inspired the name21. But one must be wary: the alternating interpretation of sequential
programs with state yields sequential P-visible strategies, but their causal interpretation (as
in Figure 31) is not necessarily visible. Visibility is very restrictive, it is not clear what would
be a sensible programming primitive that would satisfy visibility but not pre-innocence.
We regard visibility as a key contribution. It has far-reaching consequences – some of
which will be introduced in the course of this paper. In fact, visibility is used more than
parallel innocence in further developments in this line of work [CCPW18, CdV20].
The following lemma captures how a gcc may be regarded as a standalone thread.
Lemma 5.5. Consider σ : A a visible causal strategy.
Then for any ρ “ ρ1 _σ . . . _σ ρn P gccpσq, Bσ pρq “ Bσ pρ1 q . . . Bσ pρn q is a P-view.

Proof. By Lemma A.3, Bσ pρq is an alternating sequence. By visibility, its prefixes are
configurations of A. So, Bσ pρq P Œ-PlayspAq. By Lemma A.4, the predecessor of a´ P Bσ pρq
for _A is its predecessor in Bσ pρq, i.e. Opponent always points to the previous move.
We may now define parallel innocent causal strategies, or just innocent for short.

Definition 5.6. Consider σ : A causally deterministic on arena A.
It is parallel innocent if it is pre-innocent and visible.
A standard innocent strategy as in Section 3.2, under its “causal” presentation, is a
forest of P-views (see Proposition 3.7), i.e. a forest of (displayed) gccs. In that light the
definition of parallel innocent strategies seems natural: they are generated no longer by a
21This, plus as in traditional game semantics, visibility is a prerequisite for a working notion of innocence.

## PDF page 64

24:64

S. Castellan and P. Clairambault

Vol. 20:3

forest of P-views, but by a directed acyclic graph of P-views with additional conflict relation.
This graph describes how threads are spawned, and then may merge, following the innocence
discipline ensuring that Player may not create interference between Opponent’s threads.
One of the main hurdles, in traditional game semantics, is to prove that innocent
strategies compose. We now tackle this problem for parallel innocent strategies.
5.3. Composition of Visibility. First, we establish compositionality of visibility.
5.3.1. Justifiers in strategies. We introduce some machinery on justifiers. Consider σ : A
a causal strategy on some ´-arena A. As for plays, the immediate causality in A endows
moves in |σ| with a notion of justifier. This extends to σ : A $ B with A and B ´-arenas:
Definition 5.7. Consider A and B ´-arenas, and σ : A $ B. Then, for all m, m1 P |σ|,
jpmq “ m1
jpmq “ initpmq

if Bσ pm1 q _pA$Bq Bσ pmq,
if Bσ pmq minimal in A,

and undefined otherwise.
This leaves the justifier undefined exactly for moves corresponding to minimal moves in
B, the initial moves. Note that assigning the justifier of m minimal in A to initpmq ensures
that the assignment of justifiers is invariant under currying. It might be helpful to the reader
to observe that a causal strategy σ : A $ B is visible iff for all ρ P gccpσq, for all m P ρ,
jpmq P ρ as well: all gccs are closed under justifiers. We mention in passing this lemma:
Lemma 5.8. Consider A, B ´-arenas and σ : A $ B a causal strategy.
Then, for any non-initial m P |σ|, we have jpmq ăσ m. Moreover, if polσ pmq “ ´, then
jpmq _σ m is its (unique) immediate predecessor.

Proof. As a map of event structures, Bσ locally reflects causality (Lemma A.2), so jpmq ăσ m
if the first clause of Definition 5.7 applies; for the other we clearly have initpmq ăσ m.
If polσ pmq “ ´, then jpmq is defined via the first clause since A is negative, and
Bσ pjpmqq _A$B Bσ pmq. Now, m has a predecessor m1 _σ m, by courtesy Bσ pm1 q _A$B
Bσ pmq, so Bσ pm1 q “ Bσ pjpmqq as A is forestial, and m1 “ jpmq by local injectivity.

5.3.2. Justifiers in interactions. We extend justifiers to interactions – consider A, B and C
three ´-arenas, and σ : A $ B and τ : B $ C causal strategies.
Definition 5.9. We define the partial function j : |τ f σ| á |τ f σ| as jpmq “ m1 if:
(1) Bτ fσ pm1 q _A∥B∥C Bτ fσ pmq, or
(2) Bτ fσ pmq is minimal in A and m1σ “ initpmσ q, or
(3) Bτ fσ pmq is minimal in B and m1τ “ initpmτ q,
and undefined otherwise. We say that m1 is the justifier of m in τ f σ.
This leaves jpmq undefined exactly if it corresponds to a minimal move in C. Clearly
the two notions of justifier are compatible, in the sense that for all m P |τ f σ|, if mσ is
defined then jpmqσ is defined and equal to jpmσ q, and likewise for τ .

## PDF page 65

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:65

5.3.3. Views of gccs. We introduce the main technical device on visible causal interactions.
We use polarities in interactions as in Section 4.2.6, and annotate events accordingly.
We also write e.g. a´,r to indicate that a has polarity ´ or r. If ρ P gccpτ f σq with last
event m, we say that ρ ends in σ if mσ is defined, and likewise for τ . We now define views
of gccs, used to project a gcc of the interaction to gccs for both strategies.
Definition 5.10. Consider σ : A $ B and τ : B $ C with A, B and C ´-arenas.
If ρ P gccpτ f σq ends in σ, we (partially) define xρyσ P gccpσq by:
xρ0 _ . . . _ ρn _ ρln`1 yσ “ xρ0 _ . . . _ ρn yσ Y tpρn`1 qσ u ,
σ “ xρ _ . . . _ ρ yσ Y tpρ
xρ0 _ . . . _ ρi _ . . . _ ρ´,r
0
i
n`1 qσ u if jpρn`1 q “ ρi in A or B ,
n`1 y
r
σ
xρ0 _ . . . _ ρi _ . . . _ ρn`1 y “ tpρn`1 qσ u
if ρn`1 minimal in B ,

undefined otherwise. For ρ P gccpτ f σq ending in τ , we (partially) define xρyτ P gccpτ q:
xρ0 _ . . . _ ρn _ ρrn`1 yτ “ xρ0 _ . . . _ ρn yτ Y tpρn`1 qτ u ,
τ “ xρ _ . . . _ ρ yτ Y tpρ
xρ0 _ . . . _ ρi _ . . . _ ρ´,l
0
i
n`1 qτ u
n`1 y

if jpρn`1 q “ ρi ;

when defined we call xρyσ P gccpσq the σ-view of ρ and xρyτ P gccpτ q the τ -view of ρ.
These definitions almost perfectly follow Definition 3.4. The last clause is only needed
for x´yσ and not x´yτ , because an initial event in C must be the first event of ρ anyway.
That this yields gccs of σ and τ rests on Lemma 4.22, and courtesy of σ and τ . The
σ-view and the τ -view are in principle only partially defined, because it may be, when
attempting to follow the opponent’s pointer, that that justifier lies outside the gcc. For
instance xρyτ , for ρ in Figure 47, is not well-defined: when attempting to compute xq´ qr0 ✓l1 yτ ,
none of the clauses apply as jp✓l1 q “ qr1 is outside ρ. The bulk of the proof of stability of
visibility under composition, is to show that this cannot happen for visible strategies:
Proposition 5.11. Let σ : A $ B and τ : B $ C be visible causal strategies.
Then, the views of gccs of τ f σ as in Definition 5.10 are always well-defined.
Proof. We prove by induction on ρ that, for all prefixes of ρ,
(1) if ρ ends in σ, then xρyσ is well-defined,
(2) if ρ ends in τ , then xρyτ is well-defined .
Assume ρ finishes in τ . If the last move has polarity ´, then either it is initial and there
is nothing to prove, or by Lemma 4.22 its justifier is its predecessor in ρ, so xρyτ P gccpτ q
follows immediately by induction hypothesis (in that case ρ does not end in σ).
If the last move has polarity r, write ρ “ ρ1 _ m _ nr . By Lemma 4.22, mτ _τ nτ , so
in particular m is in τ . By induction hypothesis, κ “ xρ1 _ myτ P gccpτ q, so
κ _ nτ “ xρyτ P gccpτ q

as well. But if ρ finishes in σ and τ (i.e. in B), we must further prove that xρyσ P gccpσq.
In that case, we observe that since xρyτ P gccpτ q and τ is visible, it follows that jpnτ q P xρyτ ,
but this entails jpnq P ρ. Hence the second clause of Definition 5.10 applies, and we conclude
by induction hypothesis. If ρ finishes in σ, the reasoning is symmetric.
From this, we are now ready to conclude:
Proposition 5.12. Let σ : A $ B and τ : B $ C be visible causal strategies.
Then, τ d σ : A $ C is also visible.

## PDF page 66

24:66

¨
U

˚
˚
˚
˚
˚ q` pw (
˚
˚ _
˚ ´
˚✓
˚
˚
˝

Vol. 20:3

S. Castellan and P. Clairambault

⊸

⊸

U

˛
U

¨

U ⊸ U ⊸ U $ pU ⊸ U ⊸ Uq ⊸ U

‹

q`
_

✓´

t| 0

˚
˚
˚
‹ ˚
'
‹ ˚
q` pw
‹ ˚
‹d˚
‹ ˚ sz .
x ; _
‹ ˚ q´ q´ ✓´ q´ s{
‹ ˚ _
_
˚ 
 #+'. ` ‹
% _
✓ ‚ ˝ ✓` pw ( ✓` qx )
✓`

˛

¨

pU ⊸ U ⊸ Uq ⊸ U

˛

‹

q´ ‹
‹

q`
q´

y >

y =

˚
‹
˚
´ ‹
q
˚
‹
‹ ˚
‹
y =
‹ ˚
‹
`
q
‹ ˚
‹
‹“˚
‹
‹ ˚ ´ s{ . ´ y =
‹
‹ ˚q
‹
‹ ˚ _ ; q
‹
‹ ˚  x
‹
‚ ˝ ✓`
‚

q´ ‹
‹

Figure 49: Failure of preservation of pre-innocence under composition
Proof. We prove by induction on ρ that for all ρ P gccpτ f σq, Bτ fσ pρq P C pA ∥ B ∥ Cq. If
ρ is empty it is clear; take ρ _ m P gccpτ f σq. By induction hypothesis, Bτ fσ pρq P C pA ∥
B ∥ Cq, we only need that the justifier of m is in ρ. We reason by cases on the polarity of m:
if it is ℓ, then by Proposition 5.11 xρ _ myσ P gccpσq. But since σ is visible, the justifier of
mσ appears in xρyσ ; so the justifier of m is in ρ. The other cases are symmetric or trivial.
Now, take ρd P gccpτ d σq. By definition of τ d σ, there is a (non-necessarily unique)
ρf P gccpτ f σq such that ρd comprises exactly those events of ρf occurring in A or C. By
the observation above, Bτ fσ pρf q P C pA ∥ B ∥ Cq, hence Bτ dσ pρd q P C pA ∥ Cq.

5.4. Composition of Innocence. We now address composition of pre-innocence.
We start this section by showing “what could go wrong”. In Figure 49, we show
a counter-example to the stability under composition of pre-innocence without visibility,
with the corresponding interaction appearing as Figure 50. Let us attempt to explain the
phenomenon, calling σ the left hand side strategy (parallel composition) and τ the right hand
side one – observe that the dotted lines include the justifications relations from Definition
5.7 rather than just those coming from the arena. Imagine that τ wants to perform an
illegal causal merge between the two argument calls of its argument of type U ⊸ U ⊸ U.
By pre-innocence it cannot do so directly. However, it can outsource the merge to σ by
linking (legally with respect to pre-innocence, but illegally with respect to visibility) the
arguments of the parallel composition to those that it wants to merge.
We shall prove that this cannot happen in the presence of visibility. Let us fix, until the
end of the section, two visible causal strategies σ : A $ B and τ : B $ C.
5.4.1. The “forking lemma”. Taking a closer look at Figure 50, we highlight the two illegally
merging gccs in the interaction: while σ is responsible for the merge, the point where these
gccs forked is external, outside the scope of σ! The next lemma, dubbed the “forking lemma”,
forbids this: it implies that visible strategies cannot unknowingly close an Opponent fork.
If ρ “ ρ1 _ . . . _ ρn is a gcc and 1 ď i ď n, ρďi is the gcc ρ1 _ . . . _ ρi . Two gccs
ρ, κ are forking iff ρ X κ ‰ H, and for all i, j, if ρi “ κj then ρďi “ κďj . If ρ, κ are two
forking gccs, we write gcepρ, κq for their greatest common event. Notice that despite the
terminology, two forking gccs can be prefix of one another and never truly go separate ways.
Lemma 5.13 (Forking lemma). Let ρ, κ P gccpτ f σq be forking gccs ending in σ, s.t.
xρyσ X xκyσ ‰ H and gcepxρyσ , xκyσ q negative (the least distinct events, if any, are positive).

## PDF page 67

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

U ⊸ U ⊸ U $ pU ⊸ U ⊸ Uq ⊸ U

q
qσ ry

+

_
'

✓τ pw

qσ

τ ou %

v6

q´

_
'

ry +

q´

w 8

qτ

✓τ pw

w 8

q´

‚ q  ,2 


q


q

‚ `  ,2
m

 ,2
q

q


_

q

‚ `  ,2
m

‚W

 ,2

✓

Figure 50: Illegal causal merge

m  ,2 ‚

m
]



]

q  ,2 ‚


q

‚W
q

τ

q  ,2 ‚


q

 ,2 

q

‚ q  ,2 

 '


q

MAJ‚

 )&- ✓σ

~ 
,2

MAJ‚

24:67

]

m
]

m  ,2 ‚

Figure 51: Merging paths in G

Then, gcepxρyσ , xκyσ q “ gcepρ, κqσ . Moreover, the symmetric property holds for τ .
Proof. We only detail the proof for σ, the proof for τ is exactly the same. We build a
directed graph G with vertices ρ Y κ, and edges the (disjoint) union of the sets:
O-edges “ tpm1 , ml2 q | jpm1 q “ m2 u
P -edges “ tpml1 , m2 q | m2 _τ fσ m1 u

where the annotation mli indicates the polarity. Each vertex is source of at most one edge,
and following edges consists exactly in computing the σ-view. If ρ and κ have the same
final move, then ρ “ κ. Otherwise, consider the two paths in G starting with these distinct
final moves. Since xρyσ X xκyσ ‰ H, these two paths must intersect – Figure 51 represents a
typical G with O-edges in blue and P -edges in red with the two typical cases.
These paths meet at a vertex of incoming degree at least 2; but vertices receive only
O-edges, or only P -edges. For the former (as in the bottom of Figure 51), then gcepxρyσ , xκyσ q
is positive, which contradicts the hypothesis. For the latter (as in the top of Figure 51), we
remark that P -edges are immediate causal links in τ f σ; and there is at most one event in
ρ Y κ causing two distinct events: if it exists, it must be gcepρ, κq.
This provides the core argument for the compositionality of pre-innocence: intuitively, if
a pre-innocent strategy merges two threads, by pre-innocence its views of these two threads
fork positively. But then the forking lemma ensures that this strategy sees the actual forking
point for these threads – which therefore cannot be due to the external Opponent.
5.4.2. Stability of pre-innocence. Now, much of the proof consists in restricting the causal
shapes in τ f σ corresponding to a causal merge in τ d σ, so that the forking lemma applies.
Proposition 5.14. Consider σ : A $ B and τ : B $ C visible causal strategies.
If σ : A $ B and τ : B $ C are pre-innocent, then so is τ d σ.
Proof. Consider m P |τ d σ| and distinct ρ1 _ m, ρ2 _ m P gccpτ d σq. W.l.o.g. assume
that whenever ρ1i “ ρ2j , ρ1ďi “ ρ2ďj – or we can change m and ρi keeping the same least distinct
events, but satisfying this property. Likewise, since ρ1 , ρ2 are distinct, we assume w.l.o.g. that
their last moves m1 P ρ1 , m2 P ρ2 are distinct – or we may replace m with an earlier causal

## PDF page 68

24:68

Vol. 20:3

S. Castellan and P. Clairambault

merge. These two causal chains ρ1 and ρ2 may be completed to κ1 _ m, κ2 _ m P gccpτ fσq
such that ρi consists exactly of the events of κi occurring in A or C. Necessarily, the greatest
visible events of κ1 and κ2 are m1 and m2 respectively. Call n the least common event of
κ1 _ m and κ2 _ m above m1 and m2 (which might not be m). The situation is:
 ,2

m1  ,2

 ,2 1
κ

n

z" 
,2
E<Gn
 ,2

m2  ,2

 ,2

m

 ,2 2
κ

p

with m1 , m2 and m visible, and no one visible in between. We reason on the polarity of n in
τ f σ. By Lemma 4.22 and since arenas are forestial, it cannot be negative, so its polarity
is either l or r. Assume it is l – the other case is symmetric. We may compute the σ-views:
xκ1ďn _ nyσ ,

xκ2ďp _ nyσ

P

gccpσq ,

respectively xκ1ďn yσ _ nσ and xκ2ďp yσ _ nσ , with xκ1ďn yσ and xκ2ďp yσ distinct as they
respectively contain κ1n and κ2p . Since σ is pointed, xκ1ďn yσ X xκ2ďp yσ ‰ H, so κ1 X κ2 ‰ H as
well. Call m1 the greatest common event of κ1 and κ2 , necessarily below m1 and m2 , then:
κ1

A:E i`1

κ11  ,2

 ,2 1
κ

i´1

 ,2

 ,2

 ,2

m1  ,2

 ,2 1
κ

n

w!
l  ,2
=G
Gn

m1
}$

κ2i`1  ,2

 ,2

m2  ,2

 ,2

m

 ,2 2
κ

p

assuming w.l.o.g. that κ1ďi “ κ2ďi (changing the beginning of κ2 if required). Summing up
some properties, ξ 1 “ κ1i`1 . . . κ1n and ξ 2 “ κ2i`1 . . . κ2p are disjoint. This entails the σ-views
xκ1ďn yσ ,

xκ2ďp yσ

P

gccpσq

are forking: they coincide on a prefix and disjoint afterwards. Indeed, since ξ 1 and ξ 2 are
disjoint, any common event appears in κ11 _ . . . _ κ1i , before which the σ-views coincide.
Now, since σ is pre-innocent, the least distinct moves m11 and m12 of xκ1ďn yσ and xκ2ďp yσ
are positive. Thus their common immediate predecessor is negative – but it is also their
greatest common event, since xκ1ďn yσ and xκ2ďp yσ are forking. So, by Lemma 5.13,
gcepxκ1ďn yσ , xκ2ďp yσ q “ gcepκ1ďn , κ2ďp qσ “ m1 ,
so m1 is negative for σ. In τ f σ, m1 is negative or in B – in both cases the least visible
events in ξ 1 and ξ 2 are positive, but those are our least distinct events of ρ1 and ρ2 .
Proposition 5.15. There is _-Stratwb,inn , a sub-Seely category of _-Stratwb having the
same objects and morphisms restricted to parallel innocent causal strategies.
Proof. Propositions 5.12 and 5.14 ensure that parallel innocent strategies compose. Stability
under tensor and pairing are immediate. It remains that structural morphisms are innocent.
We detail it for copycat. Consider A a ´-arena. We show that any pi, aq P |ccA |, pi, aq
is minimal or has exactly one predecessor for _ccA . Assume first polpi, aq “ ´. If it is not
minimal, take pj, a1 q _ccA pi, aq. Necessarily i “ j and a1 _A a, so uniqueness follows from
A forestial. If polpi, aq “ `, its unique immediate predecessor is p2 ´ i, aq. So, ccA is forestial.

## PDF page 69

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:69

Now, for visibility, consider ρ P gccpccA q. But since ccA is forestial, ρ P C pccA q, so clearly
BccA pρq “ ρ P C pA $ Aq. For parallel innocence, consider ρ1 _ccA pi, aq, ρ2 _ccA pi, aq P
gccpccA q distinct. But since ccA is forestial, ρ1 “ ρ2 , contradicting their distinctness.
5.4.3. Interpretation of PCF . We complete the interpretation. For all sequential primitives
of PCF , the corresponding strategy is forestial: as for copycat, parallel innocence follows.
Finally, the strategy pletX,Y is shown parallel innocent by direct inspection (see Figure 38).
Altogether, this yields an interpretation of PCF in _-Stratwb,inn
, and we have:
!
Corollary 5.16 (Adequacy). For $ M : U any term of PCF , M ó iff JM K_-Stratwb,inn ó.
!

Proof. Consequence of Theorem 4.41, as PCF is a sub-language of IA .
By the end of the paper, we will have established that _-Stratwb,inn is intensionally fully
abstract for PCF . However the corresponding technical development is left for last.
6. Sequentiality and Causal Full Abstraction for IA and PCF
In this section, we shall define sequentiality on _-Stratwb , then prove full abstraction results
_-Stratwb
! ` sequentiality
wb
_-Strat! ` parallel innocence ` sequentiality

is fully abstract for IA ,
is fully abstract for PCF ,

established by linking with Theorems 3.10 and 3.14 for alternating strategies.
6.1. Sequentiality. We construct the Seely category of sequential causal strategies.
6.1.1. Definition. Intuitively, a causal strategy σ : A is sequential if it unfolds gracefully to
a (deterministic) alternating strategy. That does not mean that Player never throws parallel
threads, or always acts deterministically: for instance, the strategy in Figure 31 should be
sequential and yet has certain of its configurations enabling two parallel or two conflicting
Player moves. But: as long as Opponent follows an alternating discipline, so should Player.
A play s P ö-PlayspAq is alternating if s P Œ-PlayspAq. We shall often use ö-Playsp´q
or Œ-Playsp´q on causal strategies – recall that Œ-Playspσq and ö-Playspσq are sequences
of |σ|, and must not be confused with ö-Unfpσq that includes a move-by-move projection
via the display map. We start by giving the definition of (deterministic) sequentiality:
Definition 6.1. Consider A an arena. A causal (pre)strategy σ : A is sequential if:
reachable sequentiality: for tn` P ö-Playspσq, if t P Œ-Playspσq then tn P Œ-Playspσq.
`
sequential determinism: for tn`
1 , tn2 P Œ-Playspσq, then n1 “ n2 ;
sequential visibility: every alternating s P ö-Unfpσq is P-visible.
For sequential determinism, more than merely asking that ö-Unfpσq acts deterministically on alternating plays, this condition imposes that no internal non-deterministic choice
is alternatingly reachable, even when this choice would yield no observable non-deterministic
behaviour (this is required for the forthcoming alternating projection to preserve symmetry).
Sequential visibility is perhaps puzzling, as P-visibility is usually associated not to
sequentiality, but to the absence of higher-order state [AHM98]. From a given control
point, a P-visible strategy may only call a procedure bound within the branch of the syntax

## PDF page 70

24:70

S. Castellan and P. Clairambault

Vol. 20:3

tree leading to that control point. In contrast, with higher-order state, a program may
call a procedure stored in the memory, originating from a remote program phrase outside
the current branch. This phenomenon is independent of sequentiality, but in _-Strat the
causality due to the syntax tree blurs with that due to interference. So strategies arising
from the interpretation of IA are “morally” P-visible but formalizing this is nontrivial22.
For us it is not worth the trouble as P-visibility is not required for full abstraction for IA 23.
Consequently, it suffices to reinstate it once we restrict to sequential strategies.
6.1.2. Alternating projection. We start by defining the alternating projection.
Definition 6.2. Consider A, B ´-arenas, and σ : A $ B a sequential causal (pre)strategy.
Then, we define Œ-Unfpσq “ tBΛpσq ptq | t P Œ-Playspσqu.
We shall prove that Œ-Unfpσq is an alternating (pre)strategy on A ⊸ B. The two
subtle points are that it is deterministic, and uniform – which both rest on the observation:
Lemma 6.3. Consider A, B ´-arenas, and σ : A $ B a sequential (pre)strategy.
For any s P Œ-Unfpσq, there is a unique t P Œ-Playspσq such that s “ BΛpσq ptq.
Proof. Immediate by induction, using receptivity and sequential determinism.
From this it follows that Œ-Unfpσq satisfies determinism. For uniformity, we prove:
Lemma 6.4. Consider A an arena and σ, τ : A $ B sequential causal (pre)strategies.
If σ « τ , then Œ-Unfpσq « Œ-Unfpτ q.
Proof. If σ « τ , by Definition 4.14 there is an isomorphism φ : σ – τ of ess satisfying
Bτ ˝ φ „` Bσ .
We prove by induction on sσ P Œ-Unfpσq that if sσ –A$B sτ with sτ P Œ-Unfpτ q, then
taking tσ P Œ-Playspσq and tτ P Œ-Playspτ q s.t. sσ “ BΛpσq ptσ q and sτ “ BΛpτ q ptτ q from
Lemma 6.3, we have φptσ q –τ tτ as in (the obvious generalization of) Definition 2.11.
τ ´
σ ´
For sσ empty it is clear. For sσ m´
1 P Œ-Unfpσq and s m2 P Œ-Unfpτ q with s m1 –A$B
´
´
sτ m2 , there is a unique matching tσ n1 P Œ-Playspσq. So φptσ qφpn1 q P Œ-Playspτ q, and by
τ ´
induction hypothesis φptσ q –τ tτ . Moreover, from sσ m´
1 –A s m2 and BΛpτ q ˝ φ „ BΛpσq ,
BΛpτ q pφptσ qφpn1 qq –A$B BΛpτ q ptτ n2 q ,
τ `
so φptσ qφpn1 q –τ tτ n2 by „-receptivity of τ . Now, for sσ m`
1 P Œ-Unfpσq and s m2 P
`
`
Œ-Unfpτ q with sσ m1 –A$B sτ m2 , take tσ n1 P Œ-Playspσq and tτ n2 P Œ-Playspτ q s.t.
BΛpσq ptσ n1 q “ sσ m1 and BΛpτ q ptτ n2 q “ sτ m2 . By induction hypothesis, φptσ q –τ tτ . As
the former extends with φpn1 q, by extension for S pτ q there is some (positive) n12 s.t.
φptσ qφpn1 q –τ tτ n12 but now, by reachable determinism of τ , n2 “ n12 .
The lemma follows immediately from this auxiliary proposition.

In particular, if σ : A $ B is sequential, then σ « σ via the identity isomorphism,
consequently Œ-Unfpσq « Œ-Unfpσq, i.e. Œ-Unfpσq is uniform – from here we conclude:
Proposition 6.5. Consider A, B ´-arenas, and σ : A $ B a sequential causal strategy.
Then, Œ-Unfpσq : A ⊸ B is a P-visible alternating strategy.
22This was done by Laird in the first interleaving games model [Lai01b], via explicit threading information.
23Proposition 4.47 shows that non-visible behaviour characteristic of higher-order state can be mimicked

by running several threads in parallel and using signaling via interference to jump control between them.

## PDF page 71

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:71

Figure 52: State diagram for sequential interactions
Proof. Prefix-closure and receptivity are clear. Determinism is immediate from Lemma 6.3
and sequential determinism, and uniformity is immediate from Lemma 6.4.
Finally, P-visibility is immediate by definition of sequential visibility.
6.1.3. Composition. We now focus on composition of sequential causal strategies.
We introduce some terminology. If A, B and C are ´-arenas and σ : A $ B, τ : B $ C
are causal (pre)strategies, then we define ö-Playspτ f σq as in Definition 3.18, referring
to polarities of events in t´, l, ru. If u P ö-Playspτ f σq, we write uσ P ö-Playspσq,
uτ P ö-Playspτ q, and ud P ö-Playspτ d σq for the obvious restrictions. If a play is
alternating, it is in state O if it has even-length, and in state P if it has odd length.
Many properties of causal sequentiality follow from the following crucial observation:
Lemma 6.6. Consider σ : A $ B and τ : B $ C sequential causal strategies.
Then, for any u P ö-Playspτ f σq such that ud P Œ-Playspτ d σq, we have uσ P
Œ-Playspσq and uτ P Œ-Playspτ q, and we are in one of the following three cases:
(1) uσ , uτ , ud are respectively in state O, O, O,
(2) uσ , uτ , ud are respectively in state O, P, P ,
(3) uσ , uτ , ud are respectively in state P, O, P .
Proof. By induction on u. If u is empty, this is clear. Consider um P ö-Playspτ f σq. By
induction hypothesis u is in one of cases (1), (2) and (3). We distinguish cases:
(1) Seeking a contradiction, assume m occurs in B. Then, one of mσ or mτ is positive –
say w.l.o.g. the former. By induction hypothesis, uσ is alternating in state O, so ends with
a Player move. But so, uσ m`
σ P ö-Playspσq with uσ P Œ-Playspσq, so uσ mσ P Œ-Playspσq
since σ satisfies reachable sequentiality, contradiction. So, m occurs in A or C – assume
w.l.o.g. in A. Since ud is in state O, m is negative – then, it is direct that um satisfies (3).
(2) First assume that m occurs in A. Since ud P Œ-Playspτ f σq is in state P , then m
is positive; then mσ is positive, contradicting reachable sequentiality of σ with the fact that
uσ is in state O. Similarly, if m occurs in B it has polarity r and we transition to (3), and if
m occurs in C it has polarity r and we transition to (1). (3) Symmetric to (2).
In other words, as long as the external Opponent respects the alternation discipline,
interactions follow the familiar state diagram of interactions in alternating game semantics,
shown in Figure 52. None of the interacting agents can be the first to break alternation, so the
interaction ends up fully alternating. It follows that τ d σ satisfies reachable sequentiality:
Lemma 6.7. Consider σ : A $ B, τ : B $ C sequential causal (pre)strategies.
Then, τ d σ satisfies reachable sequentiality.

## PDF page 72

24:72

S. Castellan and P. Clairambault

Vol. 20:3

Proof. Consider tn` P ö-Playspτ d σq s.t. t P Œ-Playspτ d σq. We have either nσ or nτ
defined and positive, say the former w.l.o.g.. Let us complete tn to un P ö-Playspτ f σq. We
have ud “ t P Œ-Playspτ d σq, so by may distinduish along the three cases of Lemma 6.6:
(1) If uσ , uτ , ud are in state O, O, O. By hypothesis, uσ n`
σ P ö-Playspσq. Since σ
satisfies reachable sequentiality, uσ nσ P Œ-Playspσq as well, contradicting uσ in state O.
(2) If uσ , uτ , ud are in state O, P, P , as in (1) this contradicts reachable sequentiality.
(3) If uσ , uτ , ud are in state P, O, P . With ud “ t in state P , tn P Œ-Playspτ d σq.
It also follows that τ d σ satisfies sequential determinism: Lemma 6.6 expresses that
in an alternatingly reachable interaction, only one agent has control at any point. So any
alternatingly reachable non-deterministic choice in τ d σ can be attributed to σ and τ :
Lemma 6.8. Consider σ : A $ B and τ : B $ C sequential causal (pre)strategies.
Then, τ d σ satisfies sequential determinism.
`
Proof. Consider tn`
1 , tn2 P Œ-Playspτ d σq completed to u1 n1 , u2 n2 P ö-Playspτ f σq, and
1
u the greatest common prefix of u1 n1 and u2 n2 , with u1 m1 Ď u1 n1 and u1 m2 Ď u2 n2 .
Necessarily, the visible restriction of u1 is a prefix t1 Ď t, so in particular t1 P Œ-Playspτ d σq.
We distinguish cases on Lemma 6.6 applied to u1 . For (1), m1 and m2 must both be
the next negative event appearing in t, so m1 “ m2 , contradiction. For (2), m1 and m2
1
`
both have polarity r and we have u1τ P Œ-Playspτ q, u1τ pm1 q`
τ , uτ pm2 qτ P Œ-Playspτ q. Hence
pm1 qτ “ pm2 qτ since τ satisfies sequential determinism – so m1 “ m2 by local injectivity of
the projection Πτ ; contradiction. Finally, for (3), then the reasoning is symmetric.

To conclude compositionality, we link with composition of the alternating projections:
Lemma 6.9. Consider σ : A $ B and τ : B $ C sequential causal (pre)strategies.
Then, Œ-Unfpτ d σq “ Œ-Unfpτ q d Œ-Unfpσq.
Proof. Ě . If s P Œ-Unfpτ qdŒ-Unfpσq, then it is in ö-Unfpτ qdö-Unfpσq, thus in ö-Unfpτ d
σq by Proposition 4.31. As s is alternating, we also have s P Œ-Unfpτ d σq.
Ď . If s P Œ-Unfpτ d σq, there is t P Œ-Playspτ d σq s.t. s “ BΛpτ dσq ptq completed to
v P ö-Playspτ f σq. We display v to u P ö-Unfpτ q f ö-Unfpσq s.t. u æ A, C “ s. But then,
by Lemma 6.6, vσ P Œ-Playspσq and vτ P Œ-Playspτ q, so u æ A, B and u æ B, C are actually
alternating, and u P Œ-Unfpτ q f Œ-Unfpσq. Thus, s P Œ-Unfpτ q d Œ-Unfpσq.
Proposition 6.10. There is a category _-Stratseq of ´-arenas and sequential strategies.
Moreover, there is a functor Œ-Unfp´q : _-Stratseq Ñ Œ-Stratvis , preserving «.

Proof. Category. It is straightforward that copycat is sequential. Consider σ : A $ B and
τ : B $ C sequential causal strategies. By Lemma 6.7, τ d σ satisfies reachable sequentiality.
By Lemma 6.8, it satisfies sequential determinism. By Lemma 6.9 and preservation of
P-visible alternating strategies under composition, it satisfies sequential visibility.
Functorial projection. Preservation of copycat is a direct verification. Preservation of
composition is Lemma 6.9. Preservation of symmetry is Lemma 6.4.

6.1.4. Seely category. We now show that sequential causal strategies form a Seely category.
We use the following notations, for σ : A $ B and τ : C $ D: if s P ö-Playspσ b τ q,
then sσ P ö-Playspσq and sτ P ö-Playspτ q are the corresponding restrictions, defined in the
obvious way. Stability of sequentiality under tensor uses a state analysis as in Lemma 6.6:

## PDF page 73

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:73

Lemma 6.11. Consider σ : A $ B and τ : C $ D sequential (pre)strategies. For any
s P Œ-Playspσ b τ q then sσ P Œ-Playspσq and sτ P Œ-Playspτ q. Moreover, we are in one of:
(1) sσ , sτ , s are respectively in state O, O, O,
(2) sσ , sτ , s are respectively in state O, P, P ,
(3) sσ , sτ , s are respectively in state P, O, P .
Proof. Straightforward by induction on s, using reachable sequentiality of σ and τ .
Again, this is the familiar state diagram for alternating plays on a tensor of strategies,
see e.g. [Har04]. Finally, there is a state diagram for the functorial action of the exponential
– as for tensor, if s P ö-Playsp!σq, we write si for its restriction on copy index i.
Lemma 6.12. Consider σ : A $ B be a sequential (pre)strategy.
For any s P Œ-Playsp!σq, then for any i P N, si P Œ-Playspσq; and we are in one of:
(1) s has state O, and for all i P N, si has state O,
(2) s has state P , and there exists a unique i P N such that si has state P .
Proof. Straightforward by induction on s, using reachable sequentiality of σ.
As for composition, the preservation of reachable sequentiality and sequential determinism
under composition are immediate applications. We omit the easy verifications that the
alternating projection is compatible with tensor and bang; from which – as for composition –
it follows that sequential visibility is preserved. All structural strategies involved in the Seely
category structure, being variants of copycat, are easily proved sequential. Overall, we have:
Proposition 6.13. There is a Seely category _-Stratseq of ´-arenas and sequential strategies.
Moreover, Œ-Unfp´q : _-Stratseq Ñ Œ-Stratvis preserves « and the Seely structure.
6.2. Full Abstraction for IA. Next, we fine-tune _-Stratseq to get full abstraction for IA.
6.2.1. Interpretation of IA. It only remains to prove that the interpretation of the primitives
of IA, i.e. all primitives of IA except for the parallel let, are sequential. We have:
Lemma 6.14. The strategies seq, succ, if , iszero, let, assign, deref , grab, release and the
prestrategies celln and lockn are sequential. Moreover, for each of those (pre)strategies σ,
Œ-Unfpσq is the corresponding alternating strategy from Sections 2.3.5 and 3.4.3.
Proof. Routine verification.
It follows that we have an adequate interpretation of IA as sequential strategies, and:
Proposition 6.15. For any Γ $ M : A in IA, we have JM KŒ-Stratvis “ Œ-PlayspJM K_-Stratseq q.
!

!

Proof. Straightforward by induction on the derivation Γ $ M : A.
The two adequate models of IA, Œ-Stratvis
and _-Stratseq
!
! , differ in crucial ways:
seq
_-Strat! is much more expressive, and records intensional causal information. Secondly,
in _-Stratseq
one can also read the behaviour of the program under contexts outside IA.
!
However, _-Stratseq
is not fully abstract for IA – we need to deal with well-bracketing.
!

## PDF page 74

24:74

Vol. 20:3

S. Castellan and P. Clairambault

pU

Ñ

Uq

Ñ

pU

Ñ

Uq

Ñ

q`

q´

q`

q´

✓`

U
q´

Figure 53: Definition 3.20 is weaker than Definition 3.2
6.2.2. Well-bracketing. Ideally, we would hope for an interpretation-preserving functor
Œ-Playsp´q : _-Strat!wb,seq Ñ Œ-Strat!wb,vis ,
but Definition 3.20 (for non-alternating plays) is weaker than Definition 3.2 (for alternating
plays) when applied on alternating plays, as illustrated in Figure 53. While Definition 3.2
closely follows the operational idea that calls and returns are handled by a single stack,
Definition 3.20 restricts the hierarchical relationship between calls and returns.
Fortunately, from a distinguishing test in _-Stratwb,seq one can extract a characteristic
complete (see Section 3.4.4) alternating play, which – as we shall see – is well-bracketed as
in Definition 3.2. This is due to the following lemma, a well-known observation:
Lemma 6.16. Let s P Œ-PlayspAq be P- and O-visible. Assume that s has the form
s “ ...

si

...

sj

...

where no further move points to sj . Then, no move after sj can point within si . . . sj .
Proof. By P- or O-visibility, sj`1 points strictly before si . Then no view can ever see
si`1 . . . sj – so no move can point there. Besides, si can only be seen by the player
responsible for it, so no move can point to si . A proof appears in [CH10, Lemma 5].
From this, we may easily deduce the following:
Lemma 6.17. Consider s P Œ-PlayspAq P- and O-visible where every question is answered.
Then, it is well-bracketed in the sense of Definition 3.2, and thus it is complete.
Proof. Consider s P Œ-PlayspAq complete but with a well-bracketing failure, i.e. as in:
s “ ...

qQ
1

...

qQ
2

...

aA

...

with q2 unanswered when playing a. By answer-closing, no further move can point to a.
Thus by Lemma 6.16, no further move can point to q2 , contradicting that q2 is answered.
The play of Figure 53 is well-bracketed as in Definition 3.20, but it cannot be extended
to a complete play: the two questions covered will not be adressed ever again.

6.2.3. Full abstraction. From that, we may finally conclude:
Theorem 6.18. The model _-Stratwb,seq is intensionally fully abstract for IA.

## PDF page 75

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:75

Proof. Let $ M, N : A be terms in IA, and assume that JM K ­„ JN K, i.e. there is a test
α P _-Stratwb,seq
pJAK, JUKq such that α d! JM K ‰ α d! JN K – assume w.l.o.g. that α d! JM K
!
converges while α d! JM K diverges. Writing α1 “ Œ-Unfpαq, it follows that
α1 d! JM KŒ-Stratwb,vis ó
!

α1 d! JN KŒ-Stratwb,vis ò ,
!

but α1 may not be well-bracketed as in Definition 3.3. Consider s P α1 involved in α1 d! JM K ó
– until the rest of the proof, JM K is the interpretation in Œ-Stratwb,vis
. The initial question of
!
s has an answer, thus as JM K and α1 are well-bracketed in the sense of 3.21, all its questions
are answered. It is P-visible and O-visible since both JM K and α1 are P-visible. Hence, it is
complete by Lemma 6.17 (in particular well-bracketed as in Definition 3.3).
Consider α1 restricted to (plays symmetric to) prefixes of s. Now α1 is well-bracketed as
in Definition 3.2, and it distinguishes JM K and JN K, hence M ­„ N by Theorem 3.14.

6.3. Sequential Innocence. A causal strategy σ : A is sequential innocent if it is both
sequential and parallel innocent; those form a Seely category _-Stratwb,seq,inn .
We already know that _-Stratwb,seq,inn supports an adequate interpretation of PCF.
For (intensional) full abstraction, we shall prove that Œ-Unfp´q sends sequential innocent
strategies to innocent alternating strategies as in Definition 3.6, and rely on Theorem 3.10.
6.3.1. Causal analysis of sequential innocence. First, we shall see that sequential innocent
causal strategies are really representations of the P-view forests of Section 3.2.
Lemma 6.19. Consider σ : A a sequential, parallel innocent causal strategy.
Then, σ is an O-branching alternating forest.
Proof. First, we prove that for all m P |σ|, its set of dependencies rmsσ is a total order.
Seeking a contradiction, take m1 P |σ| minimal with m1 _σ m1 and m1 _σ m2 distinct,
all within rmsσ . By minimality, rm1 sσ is a total order, i.e. a gcc. By Lemma A.3, m1 and
m2 have the same polarity, opposite of m1 . Consider ρ1 P gccpσq a gcc for m passing through
m1 _σ m1 , and ρ2 P gccpσq a gcc for m passing through m1 _σ m2 . Then ρ1 and ρ2 have
least distinct events m1 and m2 ; hence by pre-innocence m1 and m2 are positive.
Now, m1 is the only immediate dependency of m1 and m2 ; indeed if there was m2 _σ mi ,
then considering ρ1 _ mi P gccpσq passing through m2 , ρ and ρ1 would fork at some event
smaller than m1 , contradicting its minimality. Hence, rm1 s Y tmi u P C pσq for i P t1, 2u.
Also writing rm1 s for the play in Œ-Playspσq with events in the same order, we have
rm1 s, rm1 sm1 , rm1 sm2 P ö-Playspσq ,
`
1
but by Lemma A.3, rm1 sm`
1 and rm sm2 are alternating. By sequential determinism of σ,
it follows that m1 “ m2 , contradiction. So, for all m P |σ|, rmsσ is a total order.
`
´
Thus p|σ|, ďσ q is a forest. Likewise, if m´ _ m`
1 and m _ m2 in σ, by sequential
determinism and the same reasoning as above, m1 “ m2 , so σ is O-branching. Finally, as
for any causal strategy σ : A on A alternating, we have _σ is alternating as well.

Let us call a branch of sequential innocent σ : A a s “ m1 . . . mn P Œ-Playspσq s.t.
m1 _σ . . . _σ mn P gccpσq .

´
Then, Bσ psq P Œ-PlayspAq, but there is more: by courtesy of σ, if m`
i _σ mi`1 then
Bσ pmi q _A Bσ pmi`1 q, i.e. Bσ pmi`1 q points to Bσ pmi q in Bσ psq. In other words, Bσ psq is

## PDF page 76

24:76

Vol. 20:3

S. Castellan and P. Clairambault

1 q´

_

3 q´
0,0

_

4 ✓`
0,0

s{ .

2 q`
0

q´

_

 '. 7 ´
✓0
_

5 q´
0,1

_

6 ✓`
0,1
9 q´
1,0

_

t} 1

10 ✓`
1,0

8 q`
1

_

11 q´
1,1

_

12 ✓`
1,1

!*

y >

13 ✓´
1,1

_

q`
0

t| 0

]

q´
0,0

q´
0,1

✓`
0,0

✓`
0,1

]

]

$

✓´
0

) 18 q`
1
]
y >

tt` fm 

q´
1,0

q´
1,1

✓`
1,0

✓`
1,1

]

]

$

✓´
1

14 tt`

Figure 54: Innocence witness for Figure 16

Figure 55: An alternative presentation

actually a P-view, i.e. an alternating play where Opponent always points to the previous
move. One can display a sequential innocent causal strategy to a forest of P-views as
in Section 3.3.1: we have recovered, as the causal structure of sequential innocent causal
strategies, the forest of P-views xxσyy, the “causal presentation” of alternating innocent
strategies from Proposition 3.7. This connection confirms that the causal strategies of
Section 5 are generalizations of the sets of P-views of traditional innocence24.

6.3.2. P-views are the causal dependency. This gives two ways to get plays from σ : A
sequential innocent: following Section 3.3.1, by selecting those plays whose P-views appear
in the causal representation; and following Section 5, as displays of alternating plays over σ
– we must prove them identical. Figure 54 shows the augmentation explored in the play of
Jλf UÑU . f skip; f skip; ttK : JpU Ñ Uq Ñ BK

in Figure 16 – the numbers in red correspond to the order in which that augmentation is
explored. The reader should take some time to digest this picture, and in particular observe
that for each prefix of the play in Figure 16, the P-view is exactly (the display of) the branch
leading to the corresponding move in the configuration. Opponent could explore the same
configuration in a different order, corresponding to a different play with the same P-views.
On the other hand, only Opponent has any degree of freedom in this exploration: Player
has ever at most one possible move, that immediately caused by the last Opponent move25.
As an aside, in Figure 55, we give an alternative presentation of the same augmentation,
making explicit how an augmentation of a sequential innocent strategy consists is the
underlying configuration (here, Figure 11), enriched with immediate causal links. The set
of (isomorphism classes of) configurations reached is essentially the information recorded
by the relational model; so this presentation shows plainly that innocent game semantics
consist in enriching the relational model with explicit causal / temporal information.
24This shows that the causal reasoning permitted by traditional innocence, one of the main tools of

traditional game semantics, is not inherently restricted to innocence. This is a powerful observation, and
much of the subsequent line of work in concurrent games has consisted in exploring its implications.
25Different explorations of the same augmentation may be related by permuting contiguous OP pairs of
moves. Deterministic innocent strategies may be defined as those stable under the permutations of OP pairs
permitted by the arena: this is the idea behind Melliès’ presentation of innocence [Mel04].

## PDF page 77

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:77

Back to the technical development, we must prove that if σ : A is sequential innocent,
then Œ-Unfpσq is innocent as in Definition 3.6. This relies on a link between P-views and
the causal structure of σ : A, which should be expected in the light of Figure 54.
Lemma 6.20. Consider A, B ´-arenas and σ : A $ B sequential innocent.
Then, for any tm P Œ-Playspσq, we have xBΛpσq ptmqy “ BΛpσq prmsσ q.
Proof. In the statement above, we treat rmsσ as the sequence induced by its total ordering.
The crucial observation is that is tm´ n` P Œ-Playspσq, then necessarily m´ _σ n` . To
prove that, we prove by induction on t that for any t P Œ-Playspσq: (1) if t has even length,
then all maximal events of |t| P C pσq are positive; and (2) if t has odd length, then |t| P C pσq
has exactly one maximal negative event. Indeed, for tm´ P Œ-Playspσq, then t has even
length, so |t| has all its maximal events positive. But then |tm´ | has exactly one maximal
negative event, namely m´ . Likewise, for tm` P Œ-Playspσq, then |t| has exactly one maximal
negative event. Now, the immediate predecessor of m must be negative. But if it is not
maximal in |t|, this contradicts Lemma 6.19, and in particular the fact that σ is O-branching.
Therefore, the predecessor of m must be the unique maximal negative event of |t|, and |tm|
has all maximal events positive as required. Now, if tm´ n` , then |tm´ | has exactly one
maximal negative event (namely m´ ); while the maximal events of |tm´ n` | are all positive
(and comprise n` ). Hence, m´ _σ n` as required. Likewise, if t1 m` t2 n´ P Œ-Playspσq s.t.
BΛpσq pmq _A⊸B BΛpσq pnq – so xBΛpσq pt1 mt2 nqy “ xBΛpσq pt1 qyBΛpσq pmqBΛpσq pnq then we must
have m _σ n by Lemma A.4. From these two facts, the lemma is a direct verification by
induction on t.

6.3.3. Innocent alternating unfolding. From the above, we may now deduce:
Proposition 6.21. Consider A, B ´-arenas, and σ : A $ B a sequential causal strategy.
If σ is parallel innocent, then Œ-Unfpσq is innocent as in Definition 3.6.
Proof. First, we must show that Œ-Unfpσq is P-visible. In other words, we must prove that
for all s P Œ-Unfpσq, xsy P Œ-PlayspA ⊸ Bq. For the empty play there is nothing to prove;
so consider sa P Œ-Unfpσq and tm P Œ-Playspσq such that sa “ BΛpσq ptmq. Now, by Lemma
6.20, we have xsay “ BΛpσq prmsσ q, as plays – therefore xsay P Œ-PlayspA ⊸ Bq as required.
Now, we prove innocence. Let sa` , s1 P Œ-Unfpσq such that xsy “ xs1 y. By definition,
there is tm` P Œ-Playspσq and t1 P Œ-Playspσq such that sa “ BΛpσq ptmq and s1 “ BΛpσq pt1 q.
Now, by Lemma 6.20, xsay “ BΛpσq prmsσ q as plays, hence also xsy “ BΛpσq prnsσ q for
n _σ m. Again by Lemma 6.20, xs1 y “ BΛpσq prn1 sσ q for n1 the last move of t1 . Since xsy “ xs1 y,
by Lemma 6.3, rnsσ “ rn1 sσ . So, |t1 | Y tmu is down-closed. Finally, |t1 | Y tmu is negatively
compatible since |t1 | P C pσq and m is positive, hence |t1 | Y tmu is compatible as σ satisfies
causal determinism. Therefore, t1 m P Œ-Playspσq, and s1 m “ BΛpσq pt1 mq P Œ-Unfpσq.
Altogether, we have proved the following proposition:
Proposition 6.22. There is a Seely category _-Stratseq,inn of ´-arenas and sequential
strategies. Moreover, the alternating unfolding preserves « and the Seely category structure:
Œ-Unfp´q : _-Stratseq,inn Ñ Œ-Stratinn .

Proof. It suffices to prove that the functor of Proposition 6.13 sends sequential innocent
causal strategies to innocent alternating strategies, which we know by Proposition 6.21.

## PDF page 78

24:78

S. Castellan and P. Clairambault

Vol. 20:3

We are now equipped to show full abstraction for PCF.
6.3.4. Full abstraction for PCF. We show that _-Stratwb,seq,inn is fully abstract for PCF.

Theorem 6.23. The model _-Stratwb,seq,inn is intensionally fully abstract for PCF.

Proof. Let $ M, N : A be terms in PCF s.t. JM K ­„ JN K, i.e. there is α : !JAK $ U sequential
innocent and well-bracketed such that, w.l.o.g., α d! JM K ó and α d! JN K ò. Then, it follows
Œ-Unfpαq d! JM KŒ-Strat! ó ,

Œ-Unfpαq d! JN KŒ-Strat! ò ,

with Œ-Unfpαq well-bracketed by Proposition 3.15. Hence, M ­„ N by Theorem 3.10.

7. Finite Definability and Full Abstraction for PCF
We have now established the following intensional full abstraction results:
_-Stratwb
!
wb
_-Strat! ` sequentiality

_-Stratwb
! ` parallel innocence ` sequentiality

is fully abstract for IA ,
is fully abstract for IA ,
is fully abstract for PCF ,

and we are left with the one outstanding objective:

_-Stratwb
! ` parallel innocence is fully abstract for PCF .

Unfortunately, this is also the most challenging of our full abstraction results: whereas
for the others we could leverage earlier work, we must prove finite definability from scratch.
Proving finite definability for parallel innocent strategies involves many steps. In
Section 7.1, we introduce a more convenient equivalence between parallel innocent strategies,
positional equivalence. In Section 7.2 we show it suffices to consider tests that satisfy a
stronger, causal, form of well-bracketing useful for definability. In Section 7.3 we introduce a
notion of finiteness, and show that finite tests suffice. In Section 7.4, we show a factorization
result, reducing finite definability to that for first-order strategies. In Section 7.5, we conclude
the proof of finite definability. Finally, in Section 7.6, we prove intensional full abstraction
for PCF , concluding the technical contents of the paper.
7.1. The Positional Collapse. Definability will hold only with respect to positional
equivalence, a congruence amounting to an equal projection in the relational model.
7.1.1. Positions of arenas. We will observe strategies only on certain positions of arenas.
Definition 7.1. Let A be an arena, and x P C pAq.
We say that x is complete iff every question in x has an answer in x.
Complete configurations mirror the complete plays of Section 3.4.4 and onwards. In both
cases, all function calls have returned. The difference, however, is that complete plays are
sequential whereas complete configurations are not: they are a “static” snapshot presenting
all calls and returns and their hierarchical relationships, with no temporal information.
Besides, complete configurations also comprise the ad-hoc choice of copy indices for all
replicable moves. So we quotient them out via the following variation.

## PDF page 79

Vol. 20:3

¨

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

U

˚
˚
` ou %
ż ˚
˚ q_
˚ ´
˚✓
˚
˚
˚
˝

⊸

U

⊸

U

˛

¨

U

⊸

⊸

U

q´ ‹

˚
‹
˚
‹ ż ˚
‹
˚
‹
˚ ` pw (
‹“ ˚q
‹
˚ _
‹
˚ ✓´
‹
˚
‚
˝

 %, q`
_

✓´

 &-

✓`

U

˛

t| 0

_

✓´
 #+'.
✓

,
⊸

‹
‹
‹
‹
‹“
‹ ’
‹ ’
’ q`
‹ ’
’
’
‚ ’
’
’
`
%

q´ ‹
q`

$
’
U
’
’
’
’
’
’
’
’
&

24:79

✓´

U

⊸

U /
/

/
/
/
/
/
/
q´ /
.
q`
✓´

/
/
/
/
/
/
/
-

✓` /
/

Figure 56: Quotienting out evaluation order
Definition 7.2. Let A be an arena. The set of positions on A, ranged over by x, y, . . . , is:
∫A

“

tx P C pAq | x completeu{ –A .

If x P C pAq is complete, we write rxs– P ∫A for its symmetry class.
For instance, the configuration of Figure 11 is complete. The matching position is
described intuitively by removing the grey subscripts, i.e. the copy indices.
7.1.2. Positions of strategies. The positional collapse of a strategy is an explicit desequentialization, obtained by forgetting the chronological ordering of complete plays.
Definition 7.3. Consider A an arena, and σ : A a causal strategy. The positions of σ are
∫σ “ tx P ∫A | Dx P C pσq, x “ rBσ pxqs– u .
For σ : A $ B, positions are symmetry classes of parallel compositions xA ∥ xB , also
written xA ∥ xB for xA “ rxA s– , xB “ rxB s– . They correspond to pairs pxA , xB q P p∫Aqˆp∫Bq
– so ∫σ gives a relation from ∫A to ∫B; accordingly we also write pxA , xB q P ∫σ for xA ∥ xB P ∫σ.
We illustrate the construction in Figure 56: the example illustrates how, by only keeping
complete positions, the collapse forgets the evaluation order. We define:
Definition 7.4. Two causal strategies σ, τ : A are positionally equivalent iff ∫σ “ ∫τ .
We write σ ” τ to denote the fact that σ and τ are positionally equivalent.
This is a drastic quotient, identifying sequential and parallel evaluation. It will help
tremendously in our definability procedure, which will not respect the evaluation order.
Of course, the more drastic the quotient, the more challenging the corresponding proof
obligation that it is preserved by operations on strategies – and in particular by composition.
7.1.3. Deadlocks. Stability of positional equivalence by composition boils down to
∫p´q : _-Strat Ñ Rel

being functorial, where Rel is the usual category of sets and relations.
For morphisms σ P _-StratpA, Bq, we have defined ∫σ P Relp∫A, ∫Bq. But for now, this
operation has no reason to preserve composition! In fact neither inclusion holds: firstly,
∫pτ d σq Ď p∫τ q d p∫σq may fail as a complete configuration may arise through an interaction
involving a non-complete configuration on B. We shall see later on that this can be salvaged

## PDF page 80

24:80

Vol. 20:3

S. Castellan and P. Clairambault

¨

˛
⊸

U
˚
˚
˚
˚
˚
˚
˚
˚ q´ sz ˝ _

 rz ,
`

✓

$

U
q_`


✓´

s{ .

¨

N

U

‹
‹
q´ ‹
‹
‹
‹
‹
‹
‚

˚
˚
˚
˚ ` sz ˚ q_
˚ 
˚ ´
˝✓

 #+ `

0

d

˛

⊸

 %,

¨

˛

U

N

‹
q´ ‹
‹
‹
‹
‹
‹
‚

˚ ´‹
˚q ‹
˚
‹
˚
‹
˚
‹
˚
‹
˚
‹
˝
‚

“

✓`

Figure 57: Deadlocking composition of causal strategies
by restricting to well-bracketed causal strategies, ensuring that an interaction producing a
complete configuration on A $ C will only involve a complete configuration on B.
However the other direction also fails, and the diagnosis is more serious. To construct
pxA , xC q P p∫τ q d p∫σq, one provides xB P ∫B mediating for relational composition, so
pxA , xB q P ∫σ ,

pxB , xC q P ∫τ ,

τ
τ
τ
τ
i.e. with xσ P C pσq and xτ P C pτ q s.t. writing Bσ xσ “ xσ
A ∥ xB and Bτ x “ xB ∥ xC ,
σ
τ
σ
τ
σ
τ
xA P xA , xC P xC , and xB , xB P xB , so xB –B xB match up to symmetry. In other words,
we must provide a witness position that both strategies agree (up to symmetry) is reachable.
On the other hand, composition of strategies is more rigid: not only should the projections
σ
of x and xτ on B match, they should also arrive at this position in the same chronological
ordering. This is not always possible: these two notions of composition differ when interaction
triggers a causal deadlock, i.e. pairs of configurations that are matching but not secured as
in Definition 4.6. Figure 57 displays an example: the strategy obtained by composition has
no response to the initial Opponent move, while relational composition authorizes 0` .
This strikes at the heart of the difference between game and relational semantics: the
former is dynamic hence sensitive to deadlocks, while the latter is static. This of course is
what lets game semantics model languages with non-commutative effects, but for us, very
concretely, it means that positional equivalence is in general not a congruence.

7.1.4. The deadlock-free lemma. Our deus ex machina is visibility. A powerful – and at first
unexpected – consequence of visibility is that any interaction between visible strategies is
always deadlock-free. The consequence of visibility that our proof will exploit repeatedly is:
Lemma 7.5. Consider A, B ´-arenas, σ : A $ B visible, and m, m1 P |σ| s.t. m ăσ m1 .
Then, jpm1 q is comparable with m with respect to ďσ .
Proof. Since m ăσ m1 , there is ρ _ m1 P gccpσq s.t. m P ρ. If Bσ pm1 q is minimal in A,
Bσ pjpm1 qq is minimal in B, so jpm1 q is minimal for ďσ by courtesy. But since σ is pointed,
jpm1 q is the initial move of ρ, obviously comparable with m as ρ is totally ordered.
Else, by visibility jpm1 q P ρ. But ρ is totally ordered, so m, jpm1 q comparable.
We shall prove that the composition of visible causal strategies is deadlock-free. But
first, we recall the basic mechanisms of interactions between causal strategies. Consider
σ : A $ B and τ : B $ C, and configurations xσ P C pσq, and xτ P C pτ q such that, writing
σ
τ
τ
τ
σ
τ
σ
τ
Bσ xσ “ xσ
A ∥ xB and Bτ x “ xB ∥ xC , we have xB “ xB “ xB , i.e. x and x are matching.

## PDF page 81

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:81

Then, recall from Definition 4.6 the bijection arising from their synchronization:
φ

:

Bσ ∥xτ
C

xσ ∥ xτC

»

´1
xσ
A ∥Bτ

τ
xσ
A ∥ xB ∥ xC

»

τ
xσ
A ∥x ,

whose graph is equipped with a relation importing the causal dependencies from σ and τ :
pl, rq Ÿ pl1 , r1 q

ô

l ăσ∥C l1

_

r ăA∥τ r1 .

We saw in Definition 4.6 and Proposition 4.8 that pxσ , xτ q corresponds to a configuration
of the interaction τ f σ exactly when this bijection is secured, i.e. Ÿ is acyclic.
If σ : A $ B and τ : B $ C are visible, we claim that this is always the case. We reason
by contradiction: starting with a putative deadlock, we repeatedly push it down the causal
dependency of the arena, until it reaches a minimal event – but those cannot appear in a
cycle. Before giving the formal proof, we showcase the reasoning on a simplified case.
Consider a simple deadlock in φ, given by p1 “ pl1 , r1 q and p2 “ pl2 , r2 q P φ such that
l1 ăσ∥C l2 ,

r2 ăA∥τ r1 ,

an immediate causal incompatibility between p1 and p2 . In other words we have p1 Ÿ p2 and
p2 Ÿ p1 , and we use p1 Ÿσ p2 and p2 Ÿτ p1 to indicate the origin of the causal constraint.
Finally, we apply the same conventions for polarity of elements of φ as in Section 4.2.6.
The first observation (skipped here) is that w.l.o.g., the polarities are as in
Ÿσ

pr1 g

' l
p2 ,

Ÿτ

where both occur in B but not minimal in B – so we may take jppi q “ pjpli q, jpri qq. By
Lemma 7.5, l1 and jpl2 q are comparable for σ; while r2 and jpr1 q are comparable for τ . If
p1 Ÿσ jpp2 q or p2 Ÿτ jpp1 q, then we respectively have one of the cycles:
Ÿσ

1 jpp2 qr

pr1 f

Ÿτ

$

Ÿσ

pl2

pr1 d

or

2

Ÿσ

Ÿτ

& l
p

jpp1 ql q Ÿτ

so simple deadlocks between p1 and jpp2 q; or between jpp1 q and p2 . The cumulative depth in
B has decreased. The case p1 “ jpp2 q or p2 “ jpp1 q is easily discarded.
The last case has jpp2 q Ÿσ p1 and jpp1 q Ÿτ p2 . But p1 has polarity r, so by Lemma 5.8 the
only immediate dependency in σ of l1´ is jpl1 q. So jpp2 q Ÿσ p1 factors as jpp2 q Ÿσ jpp1 q Ÿσ p1 .
Symmetrically jpp1 q Ÿτ jpp2 q, so we have:
Ÿτ

jpp1 q

%

jpp2 q ,
e
Ÿσ

closer to the root of the arena. Repeating this we eventually hit an impossible simple deadlock
with a minimal event in B, finally exposing the contradiction. So visibility structures the
interaction around the dependency of the arena, giving us an effective reasoning principle.
The proof of the deadlock-free lemma is the same in essence, but challenging in form.
Firstly, cycles in Ÿ in Definition 4.6 may have arbitrary length. Secondly, in relational
composition strategies synchronize on symmetry classes of configurations rather than concrete
configurations; so we must account for synchronization through symmetry.

## PDF page 82

24:82

Vol. 20:3

S. Castellan and P. Clairambault

Lemma 7.6. Consider A, B, C ´-arenas, σ : A $ B and τ : B $ C visible causal strategies,
τ
xσ P C pσq and xτ P C pτ q with a symmetry θ : xσ
B –B xB . Then, the composite bijection
φ

:

xσ ∥ xτC

Bσ ∥xτ
C

»

σ
τ
xσ
A ∥ xB ∥ xC

τ
xσ
A ∥θ∥xC

»

τ
τ
xσ
A ∥ xB ∥ xC

´1
xσ
A ∥Bτ

»

τ
xσ
A ∥x ,

is secured, in the sense that the relation Ÿ, defined on the graph of φ with
pl, rq Ÿ pl1 , r1 q
whenever l păσ ∥ăC q l1 or r păA ∥ăτ q r1 , is acyclic26.
Proof. We use polarities l, r or ´ for elements of φ (i.e. pairs pl, rq) as in Section 4.2.6. We
say pl, rq occurs in A, B or C in the obvious sense. We use a notion of justifier of a pair
pl, rq non-minimal in B: as θ is an order-isomorphism, Bσ plq is minimal in B iff Bτ prq is. If
not, then jplq and jprq also match up to θ and pjplq, jprqq must be in φ as well – we write it
jpl, rq. Suppose now Ÿ is not secured, i.e. there is ppl1 , r1 q, . . . , pln , rn qq with
pl1 , r1 q Ÿ pl2 , r2 q Ÿ . . . Ÿ pln , rn q Ÿ pl1 , r1 q ,
written p1 Ÿ ¨ ¨ ¨ Ÿ pn Ÿ p1 – the length of this cycle is n. First, w.l.o.g. the cycle occurs
entirely in B. Assume it has minimal length. If it occurs entirely in A or C, then pli q1ďiďn
(resp. pri q1ďiďn ) is a cycle in σ (resp. τ q, absurd. So, it passes through B. Next, if e.g.
pBq

pi

pCq

pCq

pBq

Ÿ pi`1 Ÿ ¨ ¨ ¨ Ÿ pj´1 Ÿ pj

,
pBq

pBq

then it is easy to prove that ri ă ri`1 ă ¨ ¨ ¨ ă rj´1 ă rj , so that pi Ÿ pj and the cycle
can be shortened, contradicting its minimality – the same argument holds for A.
We restrict to cycles in B. The depth of pl, rq is the length of the chain of justifiers to
pl0 , r0 q minimal in B – the depth of pl0 , r0 q minimal in B is 0. The depth of the cycle is
ÿ
d“
depthpli , ri q ,
1ďiďn

and we assume w.l.o.g. the cycle minimal for the product order on pairs pn, dq. In this proof,
all arithmetic computations on indices are done modulo n (the length of the cycle).
Next, let us write pi Ÿσ pj if li păσ ∥ăC q lj and pi Ÿτ pj symmetrically. We notice that
Ÿσ and Ÿτ alternate – if not we shorten the cycle by transitivity, contradicting minimality.
We assume w.l.o.g. that p2k Ÿσ p2k`1 and p2k`1 Ÿτ p2k`2 for all k. But then, polpp2k q “ r
and polpp2k`1 q “ l so that polarity in the cycle is alternating as well. Indeed, assume e.g.
p2k`1 Ÿ pl2k`2 Ÿ p2k`3
´
´
with p2k`1 Ÿτ p2k`2 and p2k`2 Ÿσ p2k`3 . Then, r2k`1 ăA∥τ r2k`2
. From its polarity, r2k`2
cannot be minimal in B. By Lemma 5.8, it has a unique predecessor jpr2k`2 q _A∥τ r2k`2 ,
´
´
so r2k`1 ăA∥τ r2k`2
factors as r2k`1 ăA∥τ jpr2k`2 q _A∥τ r2k`2
. Accordingly, p2k`1 Ÿτ
jpp2k`2 q Ÿτ p2k`2 – but dependencies in the game are respected by both strategies, so
jpp2k`2 q Ÿσ p2k`2 . So jpp2k`2 q Ÿσ p2k`3 , and we can replace the cycle fragment with

p2k`1 Ÿ jpp2k`2 q Ÿ p2k`3
which is still in B, has the same length but strictly smaller depth, contradiction. The
symmetric argument applies for σ, so any p2k`1 has polarity l and any p2k`2 has polarity r.
26For θ an identity, this exactly means that xσ and xτ satisfy the secured condition of Definition 4.6.

## PDF page 83

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:83

Now we show the cycle cannot have an event minimal in B. Seeking a contradiction, if
pl2k`1 Ÿτ pr2k`2 Ÿσ pl2k`3
with p2k`2 minimal in B, then l2k`2 ăσ∥C l2k`3 with l2k`2 minimal in B, but then
Bσ∥C pl2k`2 q ăA∥B∥C Bσ∥C pl2k`3 q. Indeed, if Bσ∥C pl2k`2 q is minimal in B, l2k`2 is (by courtesy) minimal in σ ∥ C. Likewise, since l2k`3 occurs in B, Bσ∥C pl2k`3 q depends (for ďA∥B∥C )
on a unique Bσ∥C plq minimal in B, where l must also be minimal in σ. But since σ is pointed,
l2k`3 has a unique minimal dependency, hence l “ l2k`2 and Bσ∥C pl2k`2 q ăA∥B∥C Bσ∥C pl2k`3 q
as claimed. But then, r2k`2 ăA∥τ r2k`3 , so pl2k`1 Ÿτ pr2k`2 Ÿτ pl2k`3 and again the cycle can
be shortened by transitivity, contradicting its minimality.
Now, we have proved a minimal cycle has a canonical form where the strategies alternate,
polarity alternates, all events are in B and non-minimal. Since pr2k Ÿσ pl2k`1 , writing
p “ pl, rq “ jpp2k`1 q, we have that l “ jpl2k`1 q as well. From Lemma 7.5, we know that
l “ jpl2k`1 q is comparable with l2k in σ ∥ C (by visibility of σ). If jpl2k`1 q “ l2k , then
r2k Ÿτ r2k`1 as well. This gives p2k´1 Ÿτ p2k`2 , contradicting minimality of the cycle. So
jpl2k`1 q ‰ l2k . Similarly, jpr2k`2 q is comparable with r2k`1 in A ∥ τ , but distinct.
Assume that we have p2k Ÿσ jpp2k`1 q for some k. Since jpp2k`1 q Ÿτ p2k`1 Ÿτ p2k`2 we
can replace the cycle fragment p2k Ÿ p2k`1 Ÿ p2k`2 with the cycle fragment
p2k Ÿ jpp2k`1 q Ÿ p2k`2
which has the same length but smaller depth, absurd. So, jpp2k`1 q Ÿσ p2k for all k (sym´
metrically, jpp2k`2 q Ÿτ p2k`1 for all k). In particular, jpl2k`1 q ăσ∥C l2k
but by Lemma 5.8,
´
l2k
has a unique immediate predecessor jpl2k q. So, jpp2k`1 q Ÿσ jpp2k q for all k; and likewise
jpp2k`2 q Ÿτ jpp2k`1 q for all k. So we can replace the full cycle with
jppn q Ÿ jppn´1 q Ÿ . . . Ÿ jpp1 q Ÿ jppn q
which has the same length but smaller depth, absurd.
Despite its relatively discreet role in the development, we regard the deadlock-free lemma
as one of our main contributions. It is a powerful observation with far-reaching consequences
in linking game semantics and relational models. It also gives a lot of weight to the notion
of visibility, as a simple, well-behaved and fairly general under-approximation of innocence.
7.1.5. Preservation of composition. For preservation of the positional collapse by composition,
we need one further lemma: that any complete position is reachable by a well-bracketed play.
Lemma 7.7. Take σ : A visible well-bracketed on ´-arena A, xσ P C pσq with Bσ pxq
complete. Then, there is t P ö-Playspσq such that |t| “ xσ and Bσ ptq is well-bracketed.
Proof. The idea is simple: since σ is well-bracketed, it suffices to show that Bσ pxq is reachable
by a well-bracketed Opponent. But we can set up causal constraints forcing Opponent to be
well-bracketed, formulated as a visible causal strategy, and apply the deadlock-free lemma.
For x P C pσq s.t. Bσ pxq complete, consider xσ
A as an arena with trivial symmetry. We
σ $ U|, and ď as the order of the arena enriched with:
build τ : xσ
$
U
as
|τ
|
“
|x
τ
A
A
p2, qq´ _τ
p1, aq´,A _τ
p1, a1 q´,A _τ

p1, qq`,Q
p2, ✓q`
p1, a2 q`,A

if q is an initial question in A,
if a answers an initial question in A,
if jpa2 q _A jpa1 q,

## PDF page 84

24:84

Vol. 20:3

S. Castellan and P. Clairambault

resulting in τ visible well-bracketed. By Lemma 7.6, there is a linear ordering of |xσ
A $ U|
compatible with the constraints of both σ and τ . As both are well-bracketed, its projection
on the left gives s P ö-Unfpσq such that |s| “ xσ
A and s well-bracketed as required.
Proposition 7.8. Consider σ : A $ B and τ : B $ C causal strategies.
If σ and τ are well-bracketed and visible, then ∫pτ d σq “ p∫τ q d p∫σq.
Proof. Ď. Consider pxA , xC q P ∫pτ d σq. By definition, xA ∥ xC “ ∫pBτ dσ pxτ d xσ qq for
xτ d xσ P C pτ d σq with Bτ dσ pxτ d xσ q “ xA ∥ xC complete, and xA “ ∫xA , xC “ ∫xC .
By Lemma 7.7, there is s P ö-Unfpτ d σq well-bracketed s.t. |s| “ BΛpτ dσq pxτ d xσ q. By
Proposition 4.31, there is u P ö-Unfpτ q f ö-Unfpτ q s.t. u æ A, C “ s. Now, since σ and τ
are well-bracketed and s is well-bracketed, it is direct by induction that u is well-bracketed.
Since xA ∥ xC “ Bτ dσ pxτ d xσ q is complete, in particular the initial question has an answer
– but as u is well-bracketed, all questions in u are answered. Writing Bσ pxσ q “ xA ∥ xB and
Bτ pxτ q “ xB ∥ xC , xB is complete as well. But then, rxB s– “ xB P ∫B, so xσ witnesses
pxA , xB q P ∫σ and xτ witnesses pxB , xC q P ∫τ ; so pxA , xC q P p∫τ q d p∫σq.
Ě. Assume we have symmetry classes of complete configurations xA , xB and xC s.t.
pxA , xB q P ∫σ

pxB , xC q P ∫τ ,

σ
τ
τ
τ
so there are xσ P C pσq and xτ P C pτ q with Bσ pxσ q “ xσ
A ∥ xB , Bτ px q “ xB ∥ xC , with
σ
σ
τ
τ
σ
τ
xA P xA , xB , xB P xB , and xC P xC . In particular, there is θ : xB –B xB . Now,

φ

:

xσ ∥ xτC

Bσ ∥xτ
C

»

σ
τ
xσ
A ∥ xB ∥ xC

τ
xσ
A ∥θ∥xC

»

τ
τ
xσ
A ∥ xB ∥ xC

´1
xσ
A ∥Bτ

»

τ
xσ
A ∥x ,

is secured by Lemma 7.6. They only match up to symmetry, but by Proposition 4.16, there
σ ∥ y σ , B py τ q “ y τ ∥ y τ with y σ “ y τ –
are y σ –σ xσ and y τ –τ xτ such that Bσ py σ q “ yA
τ
B
B
C
B
B
τ
σ
σ
σ
σ P x and
so y d y P C pτ d σq. But since y –σ x and y τ –τ xτ , we also know that yA
A
τ P x still, so y τ d y σ witnesses px , x q P ∫pτ d σq as required.
yC
C
A C
So positional equivalence of well-bracketed innocent causal strategies is preserved under
composition. The other constructions pose no challenge. Altogether, we get:
Corollary 7.9. There is a Seely category _-Stratwb,vis { ” of ´-arenas and positional
equivalence classes of visible well-bracketed strategies. Finally, the canonical functor
_-Stratwb,vis Ñ _-Stratwb,vis { ”

preserves the interpretation of PCF .

7.1.6. On the relational model. The above yields a functor to Rel:
Proposition 7.10. The positional collapse defines a functor ∫p´q : _-Stratwb,vis Ñ Rel.
Proof. Composition is Proposition 7.8, while for identity it is a direct verification.

Unfortunately, this functor is not compatible with the Seely category structure. For
negative arenas A, B we do have ∫pA b Bq – p∫Aq ˆ p∫Bq; but for instance ∫pA & Bq ­–
p∫Aq ` p∫Bq because ∫pA & Bq includes the empty position, which we do not have enough
information to send to the left or to the right. Likewise, ∫p!Aq ­– Mf p∫Aq. Considering only
non-empty configurations does not solve the issue, as we lose ∫pA b Bq – p∫Aq ˆ p∫Bq.
This mismatch can be mitigated by focusing on the cartesian closed Kleisli categories.
Say that an ´-arena A is strict if all its minimal (necessarily negative) events are in pairwise

## PDF page 85

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:85

conflict – all types and contexts of PCF are interpreted as strict ´-arenas. If A is an arena,
we write ∫˝A for the set of non-empty complete positions of A. Then:
Lemma 7.11. For A, B, C, D ´-arenas with C strict there are bijections:
∫pA b Bq – p∫Aq b p∫Bq
∫˝pA ⊸ Cq – p∫Aq ˆ p∫˝Cq

∫˝pA & Bq – ∫˝A ` ∫˝B
∫p!Cq – Mf p∫˝Cq .

For B, C strict it follows that ∫˝p!B ⊸ Cq – Mf p∫˝Bq ˆ p∫˝Cq, matching relational
semantics. For any PCF type A we obtain ∫˝JAK – JAKRel – such a bijection is easily
established for ground types – so for the interpretation of PCF types, points of the web in
the relational model exactly correspond to non-empty complete symmetry classes in the
game semantics. This can be extended to an interpretation-preserving functor from games
to relations, but we leave the details to a forthcoming paper on the quantitative collapse.

7.2. Well-Bracketed Pruning. We need a sufficiently constrained description of the causal
shape of strategies so that we might replicate it syntactically. While innocence is a causal
notion, well-bracketing is not, and it leaves the causal shape too liberal. We shall now see
how via a well-bracketed pruning a more causal form of well-bracketing can be enforced.

7.2.1. Causal well-bracketing. Recall the idea of Theorem 3.9: each Player question q`
corresponds to a call to a variable x. Opponent questions pointing to q` correspond
to x calling an argument; and Opponent answers to q` correspond to x evaluating to a
return value. The crux of the definability argument is that these subsequent possibilities of
Opponent moves pointing to q` split (the causal representation of) the innocent strategy
under scrutiny into sub-strategies independent from each other – as they must be, if they
are to correspond to distinct branches of the desired syntax tree.
Parallel innocent strategies enjoy the same “splitting” property, to an extent:
Lemma 7.12. Consider A an arena, σ : A an innocent causal strategy, and q ` P |σ|.
´
`
If q ` _σ m´
1 , q _σ m2 distinct, tm P |σ| | m ěσ m1 u, tm P |σ| | m ěσ m2 u disjoint.
Proof. Obvious by pre-innocence.
Unfortunately, this is too weak. Indeed q ` in the statement above should correspond
to a syntactic variable occurrence x, so that the overall term has form Crx M1 . . . Mn s
where x has arity n, with the Mi written in PCF . As standalone pieces of syntax in a
language without interference they are indeed independent from each other (as guaranteed
semantically by Lemma 7.12), but are also independent from the context C – which Lemma
7.12 does not capture. In fact, the current conditions on strategies do not ensure this.
In Figure 58, we show a counter-example: this satisfies all the conditions for an
augmentation of a well-bracketed parallel innocent strategy. Here, q`
1 should correspond
to a variable call, and q´ should initiate the exploration of its argument, and independent
sub-term. But the subsequent Player move q`
2 , the “head variable occurrence” of the
argument sub-term, also depends on a parallel thread. This behaviour is not realizable in
PCF and should be banned before any definability attempt.
We now define which causal behaviour is deemed acceptable for PCF .

## PDF page 86

24:86

Vol. 20:3

S. Castellan and P. Clairambault

pU ⊸ Uq ⊸ U ⊸ U ⊸ U

q´

nu
q`
1

t| 0

$

q`
_

 '. q`

s{ /

q´

✓´

s{ /

2

Figure 58: Non-locality of argument sub-strategies
Definition 7.13. Consider A an arena, and σ : A parallel innocent.
We say that σ is causally well-bracketed iff it satisfies the two conditions below:
wb-threads: for every ρ P gccpσq, ρ is well-bracketed in the sense of Definition 3.2,
globular: for a diagram in σ with X “ tm1 , . . . , mn u and Y “ tn1 , . . . , np u disjoint
`

5 6? m1

m´
0

 ,2

 ,2

( ` 
,2
n

m´
n

 ,2 ´
n

(
`
6?
5m

p

1

then every question in X (resp. Y ) is answered in X (resp. Y ).
The Question/Answer labeling is implicitly imported from |A| to |σ| via Bσ – likewise,
for mQ , nA P |σ|, we say that n answers m if Bσ pmq _A Bσ pnq, i.e. Bσ pnq answers Bσ pmq.
We call such a diagram a globule. This bans directly behaviours as in Figure 58. Only
Player can merge parallel threads, and only if he is responsible for the fork (by parallel
innocence). So, polarities in the definition of globules are not restrictive. One can further
observe that globules always have Question/Answer assignments as in
`,Q

0 4< m1

m´
0

 "* `,Q

n1

 ,2

m´,A
2

 ,2

 ,2 ´,A

 ,2

n2

`,Q
m2n´1

 ,2

 ,2 ´,Q

 ,2 `,A

 ,2

n2p´1

´,A
m2n

 "* `
0 4< m

n2p

Indeed, if m1 was an answer, it would be maximal in σ (by Lemma A.7, as answers are
maximal in A) and the merge would be impossible. So m1 is a question, and by globular it has
an answer in tm1 , . . . , m2n u. By courtesy this answer depends immediately on m1 in σ and
so must be m2 . Repeating this we get the description above. Hence in causally well-bracketed
strategies, parallel threads that might merge follow a strict call/return discipline.
A variant of the proof of Proposition 5.14, relying on Lemma 5.13, shows that causal
well-bracketing composes. This was done in [CCW15] (see also [Cas17]), but it is not our
route here: we must prove full abstraction with respect to the same well-bracketing condition
used before. We shall see that the situation is similar as in Section 6.2.2: in complete
configurations, which suffice for tests, the weaker well-bracketing implies the stronger.
7.2.2. Strengthening well-bracketing. We will show that if σ : A is innocent and wellbracketed (as in Definition 4.32) and xσ P C pσq is complete (i.e. all its questions have an
answer within xσ ), then the corresponding augmentation is also causally well-bracketed –

## PDF page 87

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:87

so restricting an innocent well-bracketed σ : A to its completable part yields a positionally
equivalent, causally well-bracketed strategy; a procedure we call “well-bracketed pruning”.
On arenas arising from types, gccs of innocent strategies are already well-bracketed –
this holds even without well-bracketing. The proof is morally as for Proposition 3.15.
Lemma 7.14. Consider A a type, σ : JAK an innocent causal strategy, and ρ P gccpσq.
Then, ρ is well-bracketed in the sense of Definition 3.2.
Proof. Consider ρ “ ρ1 _ . . . _ ρn P gccpσq and assume, seeking a contradiction, that ρn
is an answer not pointing to the pending question. It follows that ρ has the form:
`,A
ρ1 _ . . . _ ρi´,Q _ . . . _ ρ`,Q
_ ρ´,Q
j
j`1 _ . . . _ ρn
´,Q
where ρ´,Q
j`1 was pending. As JAK is the interpretation of a type, ρj`1 is sibling to countably
many symmetric copies, i.e. we may write it as bk with some copy index k P N, and consider
a copy bk`1 P |σ| with both bk and bk`1 pointing to ρj . Write also m “ ρn .
Consider xσ P C pσq with ρ in xσ , w.l.o.g. we can assume that (the augmentation) xσ
has top element m. Consider any t P ö-Playspxσ q s.t. |t| “ xσ . Then t may be written as
t1 ¨ bk ¨ t2 ¨ m where without loss of generality, we may assume that all events after bk depend
on it. Because ρ is in xσ , m points in t1 . Now, by uniformity of σ, there is also some

t1 “ t1 ¨ bk`1 ¨ t12 ¨ m1 P ö-Playspσq ,
such that t –σ t1 , where (therefore) m1 points to the same move as m in t1 . There is some
y σ P C pσq such that t1 P ö-Playspy σ q, w.l.o.g. assume |t1 | “ y σ . By innocence, any causal
branching in xσ and y σ is due to Player. Next, we observe that xσ and y τ are negatively
´
σ
σ
compatible. Indeed if n´
1 P |x |, n2 P |y | are in minimal conflict in σ, then by Lemma A.8,
Bσ pn1 q and Bσ pn2 q are in minimal conflict in JAK. But by property of arenas originating from
types, this implies that n1 and n2 have the same justifier n. As moves in t2 ¨ m depend on bk
and moves in t12 ¨ m1 depend on bk`1 , by pre-innocence (Lemma 7.12) these must be disjoint,
so n appears in t1 . But again by pre-innocence, since xσ has top element m and y σ has top
element m1 , only one Opponent move can point to n in xσ ; and likewise for y σ . As t –σ t1
preserves pointers, that means that n1 and n2 must arrive at the same (chronological) index
in t, t1 , and so their display in JAK are related by a symmetry in JAK. But in arenas arising
from PCF types, no conflicting events can be related by a symmetry, contradiction.
So condition wb-threads of Definition 7.13 is automatic, even without assuming wellbracketing. However, condition globular is not automatic as illustrated by Figure 58.
We shall now prove globular on complete augmentations of well-bracketed innocent
strategies. Intuitively, the reason is simple. Consider a globule
 ,2

 ,2 ´

 ' ` 
,2
b

 ,2 ´

`

8 7A a1

a´
0

1

an

 '
`
9 7Ba

bp

in xσ . As xσ is complete, every question is eventually answered. But after the merge, it
is too late for questions in the ai s and bj s: if some b such that a ě b answers ai then by
visibility ai must appear in all its gccs; but a gcc to b may go through the bj s and avoids ai
entirely. Of course, turning this idea into a proof takes some work. First we prove:

## PDF page 88

24:88

S. Castellan and P. Clairambault

Vol. 20:3

Lemma 7.15. Consider a ´-arena A, σ : A visible well-bracketed, and xσ P C pσq complete.
For all q1´,Q P xσ , for all q2`,Q P xσ such that Bσ pq1 q _A Bσ pq2 q, we have:
q1´,Q

q2`,Q
a´,A
2

ďσ

a`,A
1

with a1 and a2 the (unique) answers to q1 and q2 .
Proof. First, a1 and a2 exist as xσ is complete, and are unique by answer-linear.
Seeking a contradiction, assume a2 ęσ a1 , i.e. a2 R ra1 sσ . As a2 R rq2 sσ , writing
y “ ra1 sσ _rq2 sσ , y P C pσq with a1 , q2 P y and a2 R y. By Lemma 7.7, there is t P ö-Playspyq
well-bracketed s.t. |t| “ y. So by wait of Definition 3.20, q2 is answered in |t| “ y. But since
a2 R y, this means q2 is answered twice in xσ , which contradicts answer-linear.
Using that, we may now formalize and complete the intuitive argument above.
Lemma 7.16. For σ : JAK well-bracketed innocent and xσ P C pσq complete, xσ is globular.
Proof. Consider a globule in xσ , i.e. a diagram
`

m´
0

- 3: m1

 ,2

 $, `  ,2
n
1

 ,2

m´
n  $,

 ,2 ´
n

`

- 3: m

p

with X “ tm1 , . . . , mn u and Y “ tn1 , . . . , np u disjoint. Seeking a contradiction, consider
´
`
´
mQ
i P X unanswered in X. First, we consider q “ jpm q. Since σ is visible, q appears in
´
´
any gcc of m, so q ďσ m0 . But hence m is a question, or a gcc like
`
´
`,A
. . . _ . . . _ q ´,Q _ . . . _ m´
0 _ m1 _ . . . _ mn _ m

fails well-bracketing as mi is unanswered, forbidden by Lemma 7.14. So m` has an answer
a´ in xσ . But q ´ also has an answer b` in xσ , and by Lemma 7.15, a´ ďσ b` . So altogether
`
´
`,Q _ a´,A _ . . . _ b`,A
. . . _ . . . _ q ´,Q _ . . . _ m´
0 _ m1 _ . . . _ mn _ m

well-bracketed by Lemma 7.14. So in m` _ a´ _ . . . _ b` , some move must answer mi ;
and in particular point to mi . But mi does not appear in the gcc . . . _ m0 _ n1 _ . . . _
np _ m _ a _ . . . _ b, contradicting visibility. Therefore, X is complete.
7.2.3. Well-bracketed pruning. For x P C pσq, write x` P C pσq for the greatest `-covered
configuration s.t. x` Ď x, obtained by removing trailing Opponent moves.
Proposition 7.17. For A a ´-arena and σ : A a well-bracketed innocent strategy, set
|comppσq| “ Ytx P C pσq | x` Ď y P C pσq completeu ,
with all other components directly inherited from σ.
Then comppσq ” σ : A is innocent, well bracketed, causally well-bracketed27.
27A strategy may well be causally well-bracketed without being well-bracketed: an example of that is a

strategy σ : U $ U that simultaneously calls its argument (but does nothing with the result) and returns.

## PDF page 89

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:89

Proof. Most conditions are immediate consequences of those from σ. The only non-trivial
property is that S pσq restricted to |comppσq| is still an isomorphism family.
First, we prove that for any θ : x1 –σ x2 , x1 P C pcomppσqq iff x2 P C pcomppσqq. Indeed,
assume x`
1 Ď y1 P C pσq complete. Then, since θ is an order-iso that preserves polarities, by
`
1
2
restriction it restricts to θ1 : x`
1 –σ x2 . Now, by extension, θ extends to θ : y1 –σ y2 for
`
2
some x2 Ď y2 . But since θ preserves the Question/Answer labeling, y2 P C pσq is complete;
hence x2 P C pcomppσqq as required. From that, it is straightforward that S pcomppσqq
comprising symmetries between configurations of comppσq is an isomorphism family.
For causal well-bracketing, comppσq satisfies wb-threads by Lemma 7.14. For globular,
taking a diagram as in Definition 7.13, m` appears in a `-covered configuration of comppσq;
hence in a complete configuration of σ. Thus, the condition follows by Lemma 7.16.
Finally, we must show σ ” comppσq – in fact, we show both have the same complete
configurations. For that, any complete x P C pσq must also be `-covered: take x P C pσq
complete. If x has a maximal negative event m´ , since x is complete, m is an answer.
But jpjpmqq is a Question answered by some a`,A in x – but then m ďσ a by Lemma 7.15,
contradicting maximality of m. Using this we conclude: clearly, any complete configuration
of comppσq is a complete configuration of σ. Reciprocally, a complete x P C pσq is `-covered,
and thus also a (complete) configuration of comppσq. So, ∫σ “ ∫comppσq.
By construction, we also have that comppσq is complete, in the following sense:
Definition 7.18. Consider A an arena, and σ : A a causal strategy.
We say that σ is complete, if for any x P C ` pσq there is x Ď y P C pσq complete.

7.3. Meager Form. As for sequential strategies, definability applies for finite strategies,
defined through a notion of meager form. But to define meager forms we will first need to
restrict to concrete arenas in the sense of Section 2.20, which we must first update.
7.3.1. Updating concrete arenas. We enrich and update Definition 2.20.
Definition 7.19. A concrete arena is pA, A0 , lbl, indq with A an arena, A0 meager arena,
lbl : |A| Ñ |A0 | ,

ind : |A| Ñ N

two functions, satisfying, additionally to the conditions of Definition 2.20, the conditions:
jointly injective: for a1 , a2 P |A|, if lblpa1 q “ lblpa2 q, indpa1 q “ indpa2 q,
and predpa1 q “ predpa2 q, then a1 “ a2 .
Q-wide: for any q1Q P |A| non-minimal, for any n P N, there is q2Q P |A|
such that lblpq1 q “ lblpq2 q, predpq1 q “ predpq2 q and indpq2 q “ n.
A-narrow: for any a´ P |A| minimal or aA P |A|, indpaq “ 0,
A-conflicting: if a1 , a2 P |A| are distinct, they are in minimal conflict iff
they are both minimal with the same polarity and copy index, or
they are both answers to the same question.
`-transparent: for θ : x –A y, then θ P S` pAq iff for all a´ P x, indpθpaqq “ indpaq.
´-transparent: for θ : x –A y, then θ P S´ pAq iff for all a` P x, indpθpaqq “ indpaq.
We call indpaq the copy index of a, and predp´q is the (unique) immediate predecessor.

## PDF page 90

24:90

S. Castellan and P. Clairambault

Vol. 20:3

In arenas for ground types, all moves have copy index 0. For A & B, the copy index
function is simply inherited. For A Ñ B, the copy index of an initial p1, pi, aqq in A is simply
i – in all other cases it is inherited. It is direct that all requirements are met.
7.3.2. Meager innocent strategies. We now introduce the causal counterpart of the meager
alternating innocent strategies of Section 3.3.1. Those are parallel innocent strategies in the
sense of Section 5, but on a restricted arena authorizing only Player replications:
Proposition 7.20. Consider A a concrete arena. Then, setting events:
|A` | “ ta1 P |A| | @a´ ďA a1 , indpaq “ 0u ,
with other components inherited from A, yields an arena A` .
Proof. All verifications are straightforward. For symmetry, if θ : x –A y with x, y P C pA` q,
then by Definition 7.19, θ P S` pAq. But likewise by Definition 7.19, for θ : x –`
A y,
`
`
x P C pA q iff y P C pA q. Together those imply that the restriction of S pAq to A`
satisfies extension – other axioms are easy. Finally, from Definition 7.19 again the polarized
isomorphism families are S` pA` q “ S pA` q, and S´ pA` q restricted to identities.
So A` is A where Opponent has only access to copy index 0. This lets us define:
Definition 7.21. Consider A a concrete arena.
A meager causal (pre)strategy on A is a causal (pre)strategy σ : A` .
As intended, this eliminates the infinity originating from Opponent repetitions. As a
side-effect, the isomorphism family of σ becomes trivial: as the only non-trivial symmetries of
A` are positive, it follows by condition thin (see Lemma 3.28 of [CCW19]) that symmetries
of σ are reduced to identities – so a meager strategy is really a plain event structure.
Any causal strategy σ : A yields a meager strategy mfpσq : A` , simply by restriction:
Proposition 7.22. Consider A a concrete arena, and σ : A any causal strategy. Setting
|mfpσq| “ tm1 P |σ| | @m´ ďσ m1 , indpBσ pmqq “ 0u
with other components inherited from σ, yields a meager causal strategy mfpσq : A` .
Proof. All conditions are straightforward verifications.
We call mfpσq : A` the meager form of σ : A. As A` is closed under positive
symmetry, it is immediate that mfp´q preserves positive isomorphism: if σ « σ 1 , then
mfpσq « mfpσ 1 q. As illustration, we show in Figure 59 the meager form of pletU,U as defined
in Section 4.4.2. Unlike Figure 38, this is now not merely a symbolic representation, but an
exhaustive display of the full event structure of the meager form. We shall see that as for
alternating innocent strategies, meager forms of parallel innocent, causally well-bracketed
strategies provide a way to give complete formal descriptions of the full infinite strategy.
Without parallel innocence, taking the meager form is a lossy operation. In Figure 60
we show a typical augmentation of the causal strategy obtained as the interpretation of
$ newref x:“ 0 in λf UÑU . f plet v “!x in x:“ 1; assume pv “N 1qq : pU Ñ Uq Ñ U ,
displaying behaviour that is lost when taking the meager form: any interference between
different copies of the same branch – a behaviour typically banned by parallel innocence.
This lets us define finiteness for parallel innocent strategies as in Section 3.3.1:

## PDF page 91

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

pU

!ppU & Uq & ppU & Uq Ñ Uqq $ U

Ñ

Ñ

Uq

q´
nt #
q`
0
_

✓´
0

✓´
1

_

✓`
3,0

qx )

q´
3,0
_

✓`
3,0

ry
q´
0,i

 (/)0 q`
_3
u~ 3

✓´
3

U
q´

nu $
q`
1
_

q´
3,0

24:91

+

q´
0,j

x :

q`
0

v6

_ v 6

 '

✓`
0,i

✓`

Figure 59: The meager form of pletU,U

Figure 60: Lossy meager form

Definition 7.23. Consider A a concrete arena, and σ : A a parallel innocent strategy.
We say that σ is finite if the set |mfpσq|` “ tm P |mfpσq| | polpmq “ `u is finite.
If σ is finite, its size is the cardinal of |mfpσq|` .
7.3.3. Finite tests suffice. The key mechanism behind the reduction to finite tests is to be
able to restrict a parallel innocent strategy following a finite subset of its meager form.
´
`
Say x P C pσq is normal iff for all m` _σ m´
1 and m _σ m2 in x, m1 “ m2 . We
show that every normal x P C pσq has a unique representative in mfpσq.
Lemma 7.24. Consider A a concrete arena, σ : A a causal strategy, and x P C pσq normal.
There is a unique mfpxq P C pmfpσqq s.t. x –σ mfpxq, and θx : x –σ mfpxq is unique.
m

Proof. Existence. By induction on x. Consider x´ÝĂ y. If m is positive, by extension there
is an extension of θx with pm, nq. As n is positive its negative dependencies are in mfpxq so
their display have copy index 0, so n P |mfpσq|. If m is negative, by extension on A, there is
Bσ θx Y tpBσ pmq, aqu : Bσ pxq Y tBσ pmqu –A Bσ pmfpxqq Y tau ,
with a characterised by indpaq, lblpaq, and predpaq. If m is an answer, so is a and by
A-narrow, indpaq “ 0. If m is a Question, we may not have indpaq “ 0. But then by Q-wide,
there is a1 P |A| s.t. predpa1 q “ predpaq, lblpa1 q “ lblpaq and indpa1 q “ 0; but we must prove
that a1 is not already in Bσ pmfpxqq. If it is, there is θx pm1 q P mfpxq s.t. Bσ pθx pm1 qq “ a1 . By
courtesy m1 and m are negative in y with the same predecessor, contradicting normality of y.
So y extends with a1 with copy index 0. By transparent, Bσ pθx q Y tpBσ pmq, a1 qu P S pAq. So,
by „-receptivity of σ, θx extends with pm, mfpmqq in σ s.t. mfpmq P |mfpσq| as required.
Uniqueness. For y1 , y2 P C pmfpσqq s.t. θ1 : x –σ y1 and θ2 : x –σ y2 , then θ “ θ2 ˝ θ1´1 :
y1 –σ y2 . But copy indices of Opponent events in Bσ y1 and Bσ y2 are 0, so by `-transparent,
Bσ θ P S` pAq. By Lemma 3.28 of [CCW19], y1 “ y2 and θ “ id, so θ1 “ θ2 .
This does not depend on parallel innocence – which comes in when transporting events:
Lemma 7.25. Consider A a concrete arena, σ : A parallel innocent, and m P |σ|.
Then, there exists a unique mfpmq P |mfpσq| such that rmsσ –σ rmfpmqsσ .

## PDF page 92

24:92

S. Castellan and P. Clairambault

Vol. 20:3

Proof. Pre-innocence exactly states that the prime configuration rmsσ is normal. Hence, by
Lemma 7.24, there is a unique y P C pmfpσqq such that rmsσ –σ y. But then, as symmetries
are order-isomorphisms, y is a prime configuration y “ rmfpmqsσ as required.
Moreover, this assignment is preserved under symmetry:
Lemma 7.26. Consider A a concrete arena, σ : A parallel innocent.
For any θ : x –σ y and m P x, mfpmq “ mfpθpmqq.
Proof. As θ is an order-iso, it restricts to rmsσ –σ rθpmqsσ . Composition with rmsσ –
rmfpmqsσ and rθpmqsσ – rmfpθpmqqsσ yields φ : rmfpmqsσ –σ rmfpθpmqqsσ , and Bσ pφq P
S` pAq by `-transparent. Hence, by Lemma 3.28 of [CCW19], φ is an identity.
From that, we may deduce the following:
Corollary 7.27. For A concrete, σ : A parallel innocent and τ Ĳ mfpσq finite,
|σ æ τ | “ tm P |σ| | mfpmq P |τ |u
with all other components inherited from σ yields a finite innocent σ æ τ : A s.t. σ æ τ Ĳ σ.
Moreover, if σ is well-bracketed (resp. causally well-bracketed), so is σ æ τ .
Proof. The only non-trivial condition, extension for S pσ æ τ q, follows from Lemma 7.26.
From that, we may finally prove that finite tests suffice.
Corollary 7.28. Consider A a concrete ´-arena, and σ 1 , σ 2 : A parallel innocent.
If there is α : !A $ U parallel innocent and well-bracketed, such that
α d! σ 1 ó ,

α d! σ 2 ò ,

there is α1 Ĳ α parallel innocent, well-bracketed, and finite, s.t. α1 d! σ 1 ó and α1 d! σ 2 ò.
Proof. Since α d! σ 1 ó, there is xα d xσ1 P C pα d σ :1 q s.t. Bα xα “ xA ∥ tq´ , ✓` u. In
particular, xα is finite. So the set X “ tmfpmq | m P xα u is finite, so there is τ Ĳ mfpαq a
finite meager strategy s.t. X Ď |τ |. By Corollary 7.27, α1 “ α æ τ : A is a finite parallel
innocent strategy s.t. α1 Ĳ α. Moreover, by construction, xα P C pα1 q with the same causal
ordering as in α, so that α1 d! σ 1 ó still. Finally, α1 d! σ 2 ó would contradict α d! σ 2 ò
since α1 Ĳ α. As ö-Playspα1 q Ď ö-Playspαq, α1 is still well-bracketed.
In fact, meager forms of parallel innocent strategies can be expanded back to the original
strategy. This is not used in the technical development, but we include it as Appendix D.5.
7.4. Factorization. We focus on finite tests. Unlike in the sequential argument of Section 3.3.1, parallel innocent strategies have no “first Player move” to reproduce first syntactically. Hence we organize our definability process differently. Its core is a factorization
result (Corollary 7.43): namely, that every finite test α : !p&Ai q $ X may be obtained as
α ” fopαq d! xxi αk,1 . . . αk,pi | i P I, k P Ki y ,

(7.1)

with fopαq a strategy on a first-order type and αk,j strictly smaller. This reduces finite
definability to that for finite first-order strategies, dealt with in Section 7.5.1.
We first extract the components mentioned in (7.1): the first-order substrategy fopαq,
and the argument substrategies αk,j . We use as illustration the strategy with typical maximal
augmentations in Figure 61. The first-order sub-strategy, in red, has events those depending
on no Opponent question besides the initial move: it is independent of Opponent’s exploration

## PDF page 93

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

!ppB Ñ Uq & ppU Ñ Bq Ñ Bqq $ B

24:93

!ppB Ñ Uq & ppU Ñ Bq Ñ Bqq $ B

q´

q´
0,i

v 5

_

tt`
0,i
q´
2,k
_

ff `
2,k

nu
q`
0

$

_

✓´
0

_
&
q` ov

v6

2

q`
1,r,0

✓´
2

✓´
1,r,0

_

u~ 3

q´
1,r

q`
1
_

u~ 3
)

_

tt´
1

q´
0,i

q`
2r`3

tt`
0,i

b1,r

v 5

_

_

) ` u 4

q´

u~ 3

b´
2r`3

nu
q`
0

$

_

✓´
0
q`
1,r,0

_

u~ 3

ff ´
1
)

_

✓´
1,r,0
 )0 tt`

u~ 3

q´
1,r

q`
1

u~ 3

q`
2r`3

(
 )0 ff `

_

) ` u~ 3

b´
2r`3

b1,r

Figure 61: A parallel innocent causally well-bracketed strategy
f :B
¨ Ñ U, g : pU Ñ Bq Ñ B $
˛
x “ f tt
ˆ
˙
‚ in pif y then pf ff ; ttq else ff q : B
u “ z
let ˝
y “ g pλz U . let
in vq
v “ gK
Figure 62: Factorization and definability for Figure 61
of the arguments, and is purely first-order. The Player questions in this first-order part play
a special role; we call them primary questions. Intuitively, they correspond to occurrences of
variables not appearing in an argument to a variable call. In Figure 61, the primary questions
`
`
are q`
0 , q1 and q2 . Depending on their type, the primary questions admit arguments that
Opponent can access by playing questions pointing to them. Parts of the strategy accessed
in this way are the argument sub-strategies – in Figure 61 there are three, respectively
´
´
prompted by (i.e. causally depending on) q´
0,i , q2,k and q1,r and colored accordingly.
The strategy of Figure 61 is exactly definable; as illustration we show the term in Figure
62, with subterms colored so as to match the four components of the strategy28.
The proof of factorization is organized as follows. In Section 7.4.1, we extract the
first-order part, and in Section 7.4.2 we reorganize it so as to be able to re-compose it better.
In Section 7.4.3, we extract the argument substrategies. In Section 7.4.4, we conclude.
7.4.1. Shallow substrategy. Consider A a type, and α : JAK well-bracketed, parallel innocent,
causally well-bracketed, finite, and complete. We call such a strategy a test strategy.
Necessarily A has the form A1 Ñ ¨ ¨ ¨ Ñ An Ñ X where Ai “ Ai,1 Ñ ¨ ¨ ¨ Ñ Ai,pi Ñ Xi .
Recall that X, Xi range over ground types, i.e. U, B and N. Up to currying, we write
α : !p&1ďiďn Ai q $ X ,
omitting semantic brackets. We often shorten the left hand side part to !p&Ai q, and reuse A
for the arena !p&Ai q $ X. Now, we start with the shallow substrategy.
28In the end, our definability process will not quite give the term of Figure 62 for the strategy of Figure 61,

but a sequential version as we do not know how to define first-order strategies in general – see Section 7.5.1.

## PDF page 94

24:94

Vol. 20:3

S. Castellan and P. Clairambault

Proposition 7.29. We define the shallow substrategy as having set of events
|shpαq| “ tm P |α| | rmsα has at most one Opponent questionu ,
and other components inherited from α. Then, shpαq : !p&Xi q $ X is a test strategy.
Proof. Write shpAq for the arena !p&Xi q $ X. First, for each m P |shpαq|, Bα pmq P |shpAq|:
indeed, the least events in |A| but not in |shpAq| are Opponent questions. For extension, as
symmetries are order-isos preserving polarities and Q/A labeling, they preserve shpαq. The
conditions for a test strategy are direct by restriction from α.
We show shpαq complete. Consider x P C ` pshpαqq. Since α is complete, there is
x Ď y P C pαq complete. In particular, there is an answer a` to the initial q´
0 . By Lemma
7.15, all moves of x are below a` for ďσ . So setting z “ rasσ , x Ď z. By Lemma 7.14, all
gccs leading to a are well-bracketed, so rasσ is complete. Finally, rasσ P C pshpαqq: indeed,
if it has a non-initial Opponent question q´ , it has an answer b` distinct from a` . But
Player answers are maximal in gccs, contradicting that any gcc can be extended to a.
This captures the red part of Figure 61. All events of shpαq are in mfpαq: the negative
dependencies of m P |shpαq| are either answers or the initial question, so by A-narrow their
display has copy index 0. Since α is finite, so is the set of positive events of shpαq.
7.4.2. The flow substrategy. We must reconstruct α using the categorical structure of _-Strat.
But as distinct Player questions in the same Xi may receive distinct argument substrategies,
we need to relabel shpαq to send those to distinct components. First we define:
Definition 7.30. A primary question of α is any q Q,` P |shpαq|. We write Q for the set
of primary questions, and Qi for the primary questions displaying to Xi .
By construction, Q “ Z1ďiďn Qi . As |shpαq| is finite, so is Q, which allows us to set:
Â
Â
Definition 7.31. The flow substrategy flowpαq : 1ďiďn qPQi Xi $ X is shpαq with
Bflowpαq pmQ,´ q
Bflowpαq pmA,` q
Bflowpαq pmQ,` q
Bflowpαq pmA,´ q

“
“
“
“

p2, aq
p2, aq
p1, pi, pm, aqqq
p1, pi, pjpmq, aqqq

if
if
if
if

Bshpαq pmQ,´ q
Bshpαq pmA,` q
Bshpαq pmQ,` q
Bshpαq pmA,´ q

“
“
“
“

p2, aq
p2, aq
p1, pj, pi, aqqq
p1, pj, pi, aqqq ,

i.e. sending each q P Q and its answers to the copy of Xi specified by indices i, q.
It is a test strategy. We show in Figure 63 the maximal augmentations of the flow
substrategy for Figure 61, tagging each component by the corresponding primary question.
7.4.3. The argument substrategies. Next, we focus on the higher-order structure, aiming to
extract the arguments to (the variable calls corresponding to) the primary questions.
Fix a primary question q P Qi . It displays to an initial event in Ai , which is:
!Ai,1 ⊸ . . . ⊸ !Ai,pi ⊸ Xi .
Argument substrategies are accessed by Opponent questions pointing to primary questions. Up to symmetry, there are pi Opponent questions pointing to q, matching the pi
arguments of Ai . From now on, if q P Qi is a primary question and q _σ mQ,´ an Opponent
question, we shall say that m is in component j if it displays to an initial move of !Ai,j .
For q P Qi and 1 ď j ď pi , we shall extract the argument sub-strategy αq,j initiated by

## PDF page 95

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

`

`

`

Uq0 b Uq2 b Bq1 $ B

Uq0 b Uq2 b Bq1 $ B

q´

q´

q` ov

&

q`

_

✓

u 4

`

q` ov

_

´

!) ` u} 2
q
_

`

&

`

q`

u 4

_

_

tt´

24:95

ff ´

✓´

!)
 )/ ff `

✓´

 '. tt`

Figure 63: Augmentations of the flow substrategy for Figure 61
Opponent questions pointing to q in component j. As the strategy provides the information
for an argument of Ai it must live in Ai,j ; but it can still access the context, so we aim for:
αq,j : !p&Ai q $ !Ai,j .
To do this, we assign to all events of α tags, as follows:
Definition 7.32. Consider m P |α|. We write:
m A shpαq ô rmsα comprises exactly one Opponent question,
m A αq,j
ô there is q _α nQ,´ in component j, such that n ďα m,

where in the second clause q P Qi a primary question, and 1 ď j ď pi .

Any m P |α| is tagged as either in shpαq or in one argument sub-strategy. Crucially,
each event receives exactly one tag – this is where our structural constraints strike in:
Lemma 7.33. Every event m P |α| receives exactly one tag following Definition 7.32.
Proof. First, each m P |α| receives at least one tag. Any rmsα contains at least one Opponent
question: the initial move. If it contains exactly one Opponent question, m A shpαq. Assume
there are at least two. Take n ďα m minimal s.t. it is a non-initial Opponent question.
Then its immediate predecessor is some q P Qi ; and so there is 1 ď j ď pi s.t. m A αq,j .
We prove that m receives at most one tag. Clearly if m A αq,j for some q P Qi and
1 ď j ď pi , there are at least two Opponent questions in rmsα so we cannot have m A shpαq.
Assume m A αq,j and m A αq1 ,j 1 for q P Qi , q 1 P Qi1 , 1 ď j ď pi and 1 ď j 1 ď pi1 . We first
show that q “ q 1 ; seeking a contradiction assume they are distinct. But q and q 1 cannot be
comparable: if q ďα q 1 , rq 1 sα has at least two Opponent questions, contradicting q 1 P |shpαq|.
Take ρ _ m, ρ1 _ m P gccpαq, respectively passing through q and q 1 . Diagrammatically:
 ,2

2 5= m1

 ,2

 ,2

q

 ,2

 ,2

mk

m0
(

n1

 ,2

 ,2 1

q

 ,2

 ,2

 #+
1 4=mk`1

 ,2

 ,2

m

np

and since q, q 1 are distinct, the diagram may be chosen with X “ tm1 , . . . , mk u and Y “
tn1 , . . . , np u disjoint. By parallel innocence m1 and n1 are positive. By Lemma A.6 so must
be mk`1 , so mk and np are negative. We have a globule as in Definition 7.13, so X and Y

## PDF page 96

24:96

!ppB Ñ Uq & ppU Ñ Bq Ñ Bqq $ B

u 4
´

nu
q`
0

$

_

✓´
0

tt`
0,i

ov
q`
2

q`
1,r,0

✓´
2

✓´
1,r,0

_

q´
2,k
ff `
2,k

_
&

v 5

_

q`
1

u~ 3

q´
q`
2r`3

)

rz ,

_

tt´
1

q1,r

_

u} 2

!ppB Ñ Uq & ppU Ñ Bq Ñ Bqq $ !pU Ñ Bq

_

u} 2
´

q0,i

_

Vol. 20:3

S. Castellan and P. Clairambault

b´
2r`3

q`
2r`3

b1,r

q´
r

_

✓´
r,0
 & $,
 `

_

) ` u~ 3

q`
r,0

x ;

br

b´
2r`3
 )0 tt`

Figure 64: Events of |αq` ,1 | of Figure 61
1

Figure 65: The corresponding aug. of αq` ,1
1

are complete, and in particular q is answered in ρ. Writing q “ mi , mi`1 must answer q.
But since m A αq,j , q _α nQu,´ ďα m where n is a negative question in component j. Then
necessarily, n “ mi`1 , or we get a contradiction with parallel innocence. Thus mi`1 is both
a question and an answer, contradiction. So, q “ q 1 . Finally, from Lemma 7.12, j “ j 1 .
This shows any m P |α| can always be attributed to exactly one of the sub-strategies
we wish to extract. Accordingly, the argument sub-strategies will be defined with events
|αq,j | “ tm P |α| | m A αq,j u ,

completed to ess by inheriting the components from α, as will be made explicit later.
The display map requires a careful reindexing of events ending up on the right hand side,
illustrated in Figures 64 and 65. For this we split |αq,j | in two subsets: on the one hand,
we have those events that depend statically, i.e. with respect to ďA (through Bα ) on the
`
´
`
primary question q – in Figure 64, those are q´
i,r , q1,r,0 , ✓1,r,0 and b1,r . On the other hand,
the remaining events must follow from new calls to variables in the context – in Figure 64,
´
those are q`
2r`3 and b2r`3 . These two subsets are treated differently when defining the new
display map: the former are left unchanged, while the latter are reindexed as in Figure 65.
We introduce notations for the canonical embeddings of the set of moves |Ai | and |Ai,j |
into |A|. More precisely, it will be convenient, for each primary question q P Qi , to write
injq p´q : |Ai | Ñ |A|
the injection adding the sequence of tags addressing Ai within A, originating from the tagged
disjoint unions involved in all arena constructions – in particular, it maps the initial move of
Ai to Bα pqq. Likewise, injq,j : |Ai,j | Ñ |A| addresses the j-th argument of q. Then:
Definition 7.34. We define a display map for αq,j by setting, for m P |αq,j |:
Bαq,j pmq “ injr paq if
Bα pmq “ injq,j paq ,
Bαq,j pmq “ Bα pmq otherwise,
where injl paq “ p1, aq and injr paq “ p2, aq.
Altogether, this lets us extract αq,j as intended:

## PDF page 97

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

xA P ∫A
xB P ∫B
xA b xB P ∫pA b Bq

xA P ∫A
xC P ∫˝C
xA ⊸ xC P ∫˝pA ⊸ Cq

x P ∫˝Ai
pi P Iq
pi, xq P ∫˝p&iPI Ai q

24:97

pxiC P ∫˝CqiPI
rxiC | i P Is P ∫!C

Figure 66: Syntax for positions for A, B, C arenas with C strict
Proposition 7.35. Consider q P Qi and 1 ď j ď pi . The argument substrategy for
q, j is p|αq,j |, ďq,j , #q,j , S pαq,j q, Bαq,j q, with components ďq,j and #q,j the restrictions of
α, S pαq,j q “ tθ X |αq,j |2 | θ P S pαqu, and Bαq,j in Definition 7.34.
Then, αq,j : !p&Ai q $ !Ai,j is well-bracketed, causally well-bracketed, parallel innocent.
Proof. A routine verification. The key point is that as symmetries of α are order-isos
displayed to symmetries of A, it follows that they preserve the tag as in Definition 7.32.
Finally, we get rid of the ! on the right hand side, using dereliction derA : !A $ A.
Proposition 7.36. Consider q P Qi and 1 ď j ď pi . Then, α‚q,j “ derAi,j d αq,j : !p&Ai q $
Ai,j is a test strategy with size strictly lesser than α.
Proof. Using Proposition 4.13, it is easy that α‚q,j is positively isomorphic to the strategy
obtained from αq,j by restricting the initial Opponent question to copy index 0. This also
informs an injection of mfpα‚q,j q into mfpαq not reaching the primary question q, from which
follows the announced size constraint.
Note αq,j is recovered from α‚q,j , via the “Bang lemma” [AJM00] (see Appendix D.4):
Lemma 7.37. For concrete arenas A, B with B pointed and σ P _-Stratp!A, !Bq,
pderB d σq: « σ .

Summing up, from the original strategy α : !p&Ai q $ X, we have now constructed:
flowpαq : b1ďiďn bqPQi Xi $ X
α‚q,j : !p&Ai q $ Ai,j

for each q P Qi and 1 ď j ď pi .

For each primary question q P Qi , we use the cartesian closed internal language to form
x1 : A1 , . . . , xn : An $ xi α‚q,1 . . . α‚q,pi : Xi .
Let us write αq : !p&Ai q $ Xi for the resulting strategy. Then, finally,
recomppαq “ flowpαq d pb1ďiďn bqPQi αq q d δ &Ai

: !p&Ai q $ X ,

(7.2)

is our candidate to reconstruct α. Here, for B an arena and n P N, we write δ B : !B $ p!Bqbn
for the obvious strategy (leaving n implicit). In the sequel we may only write δ.

7.4.4. Positions of recomppαq. We expect that recomppαq « α, but we shall only prove
recomppαq ” α – this is simpler as positions compose relationally.
To help reason on positions, we adopt a syntax presented in Figure 66, following the
bijections of Lemma 7.11. We also write xA $ xB P ∫pA $ Bq for all xA P ∫A and xB P ∫B.
We now analyse the positions of the recomposition (7.2). We start with:

## PDF page 98

24:98

Vol. 20:3

S. Castellan and P. Clairambault

Lemma 7.38. For B strict, the positions ∫δ B of δ B : !B $ p!Bqbn are exactly those
¸ ż
˜
ÿ
`
˘
xi $ b1ďiďn xi P
!B $ p!Bqbn
1ďiďn

where xi P ∫!B for all 1 ď i ď n.
By a direct variation of Lemma 4.19. Next we analyse the positions of αq for q P Qi :
Lemma 7.39. For any q P Qi , the non-empty positions ∫˝αq are exactly those of the form
˜
¸
ż
ÿ
rpi, yq,1 ⊸ . . . ⊸ yq,pi ⊸ vq qs `
xq,j $ vq P p!p&Ai q $ Xi q
1ďjďpi

where for each 1 ď j ď pi , pxq,j $ yq,j q P ∫αq,j , and for vq P ∫˝Xi .
Proof. From the laws of Seely categories, αq is positively isomorphic to the composition
!p&Ai q

pb1ďjďpi pα‚q,j q: qbJxi K

/ bp `1 !p&Ai q

δ

i

/ pb1ďjďp !Ai,j q b Ai

ev

i

/ Xi

in _-Strat. The characterisation follows from Proposition 7.8, Lemma 7.38, Lemma 7.37, and
a direct verification analogous to Lemma 7.38 for other copycat-like strategies involved.
From all those, we may characterise the positions of recomppαq as
Corollary 7.40. Non-empty positions of recomppαq are exactly those of the form
¸
˜
ż
ÿ
ÿ ÿ
xq,j $ v
P
p!p&Ai q $ Xq
rpi, yq,1 ⊸ . . . ⊸ yq,pi ⊸ vq qs `
1ďiďn qPQi1

1ďjďpi

where for all 1 ď i ď n, Qi1 is a subset of Qi , all vq are non-empty, and:
¯
´
ppxq,j $ yq,j q P ∫αq,j qqPQ1 ,1ďjďpi .
b1ďiďn bqPQi1 vq $ v P ∫˝flowpαq ,
i

Proof. Direct from Lemmas 7.38, 7.39 and Proposition 7.8.

7.4.5. Positions of α. We write C c pαq for the complete, non-empty configurations of α. If
x P C c pαq, then shpxq “ tm P x | m A shpαqu P C c pshpαqq and we write Q x “ QXx, and Qix
likewise. For each q P Qix and 1 ď j ď pi , we also´have xq,j “ tm P x | m A α¯
q,j u P C pαq,j q.
Ţ
Ţ
Ţ
From Lemma 7.33, this informs x “ shpxq Z
1ďiďn
qPQix
1ďjďpi xq,j .
We show that all complete non-empty configurations of α arise in this way:
Lemma 7.41. This yields a bijection between C c pαq and pairs px, pxq,j q1ďiďn,qPQix ,1ďjďpi q
where x P C c pshpαqq, xq,j P C pαq,j q complete for all 1 ď i ď n, q P Qix and 1 ď j ď pi .
Moreover, writing rx, pxq,j qi,q,j s “ x Z pZi,q,j xq,j q P C pαq this correspondence, we have
Bα prx, pxq,j qi,q,j sq “

´Ţ
1ďiďn

Ţ
qPQix

´“
ı¯¯
‰ ”Ţ
injq pzq,1 ⊸ . . . ⊸ zq,pi ⊸ vq q Z
Z injr pvq
1ďjďpi injl pyq,j q

where we have, for all 1 ď i ď n, q P Qix and 1 ď j ď pi :
`
˘
Bflowpαq pxq “ injl b1ďiďn bqPQix vq Z injr pvq
Bαq,j pxq,j q “ injl pyq,j q Z injr pzq,j q .

## PDF page 99

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:99

!p1 & 1 & 1 & 1 & 1q $ 1

nt
q`
0

#

_

✓´
0

5
` v

` ov &

q1

q2

✓´
1

✓´
2

_

 ( ` v 6
q3
_

✓´
3

q´

_

 ( ` v 6
q4
_

✓´
4

 &-)0 ✓`

Figure 67: An undefinable first-order strategy
Proof. From x P C c pαq, we get pshpxq, pxq,j qi,q,j q from the decomposition above. Reciprocally,
from px, pxq,j qi,q,j q we get a configuration in C c pαq as their union; it is down-closed by
construction and consistent by determinism of α (as any immediate negative conflict
originates from the arena, and hence appears in one of the components). Finally, the
characterization of the display map follows from display maps of flowpαq and αq,j .
From this we may finally conclude the proof of factorization:
Corollary 7.42. The strategies α and recomppαq are positionally equivalent.
Proof. Taking symmetry classes from Lemma 7.41, we obtain the same characterization of
non-empty complete positions of α as in Corollary 7.40.

7.4.6. Syntactic factorization. Finally, we must reformulate the result relying on the cartesian
closed structure only. The first-order substrategy fopαq P _-Strat! p&1ďiďn &qPQi Xi , Xq
is obtained in the obvious way from flowpαq using the Seely category structure. Using
Corollary 7.42, Proposition 7.36, and laws of a Seely category, we conclude:
Corollary 7.43. Any test strategy α : !p&Ai q $ X factors as a composition of test strategies
α ” fopαq d! xxi α‚q,1 . . . α‚q,pi | 1 ď i ď n, q P Qi y ,
where for all 1 ď i ď n, q P Qi and 1 ď j ď pi , α‚q,j has size strictly lesser than α.
7.5. Finite Definability. Corollary 7.43 allows us to handle the higher-order structure, it
only remains to prove definability for first-order test strategies.
7.5.1. First-order definability. Not every first-order test strategy is exactly definable in PCF .
For instance, that in Figure 67 is not series-parallel, while it is fairly easy to prove that
all PCF -definable terms on this type yield a series-parallel causal dependency. In general,
we have not yet managed to properly understand which first-order strategies are definable.
Luckily, we do not need to. Indeed, given a test α it is sufficient to find M such that JM K
is positionally equivalent from α. In PCF , without interference, the order of evaluation is
unobservable; and positional equivalence is not sensitive to it. So our definability process
will simply sequentialize α, while preserving its positions.

## PDF page 100

24:100

S. Castellan and P. Clairambault

Vol. 20:3

Consider Γ “ x1 : X1 , . . . , xn : Xn , some ground type X, and a test strategy:
α : !p&Xi q $ X .
If ∫˝α is empty, any diverging term M will satisfy ∫˝JM K “ H. Otherwise, there is some
x P C c pαq. If α has no primary question, then x “ tq0Q,´ , aA,` u, with a answering q0 – write
Bα paq “ v some answer in X. But then by determinism of α, it cannot have any other move
and α « JvK. Otherwise, if α has a primary question, it has one a P Q which is minimal,
i.e. it only depends on the initial move. But then q appears in every x P C c pαq:
Lemma 7.44. For any minimal primary question q, for any y P C c pαq, we have q P y.
Proof. By determinism, y Y tq0 , qu P C pαq. Since y is complete, there is aA,` P y such that a
answers q0 . But then, by Lemma 7.15 we have q ďα a. It follows that q P y as required.
Choose q P Qi minimal. As q appears in all non-empty complete configurations, it is
safe to first make a call to xi , then branching on the possible return values. Since α is finite,
there is a finite set V of values leading to an observable result. Now, for each v P V , we
define αpqvq the residual of α after q yields value v; and then proceed inductively. To define
this residual, our first step is to rename α to isolate this first call:
Lemma 7.45. For q P Qi minimal, there is a test strategy αpqq : !pp&i Xi q & Xi q $ X s.t.
(1) for all x $ w P ∫˝αpqq , then x “ x1 ` rpn ` 1, vqs such that x1 ` rpi, vqs $ w P ∫˝α,
(2) for all x $ w P ∫˝α, then x “ x1 ` rpi, vqs such that x1 ` rpn ` 1, vqs $ w P ∫˝αpqq .
Proof. The strategy αpqq has components as for α except the display map, which sends q and
its answers to the new component. The characterisation of positions is straightforward.
We obtain the residual αpqvq as αpqvq “ αpqq d! xder&Xi , vy : !p&Xi q $ X writing
v : !p&Xi q $ Xi the constant strategy. In order to characterize its positions, we note:
Lemma 7.46. For any v P V , the positions of xder&Xi , vy: are exactly those of the form
x $ x ` p ¨ rpn ` 1, vqs

P

∫ p!p&Xi q $ !pp&Xi q & Xi qq ,

where p ¨ rpn ` 1, vqs denotes the p-fold sum, and for any x P ∫p!p&Xi qq and p P N.
Proof. Straightforward verification.
Using this lemma, we link the positions of α and αpqvq .
Lemma 7.47. We have the following properties:
(1) for any x $ w P ∫˝α, there is x “ x1 ` rpi, vqs such that x1 $ w P ∫˝αpqvq ,
(2) for any x $ w P ∫˝αpqvq , we have x ` rpi, vqs $ w P ∫˝α.
Proof. By definition, we have αpqvq “ αpqq d xder&Xi , vy: , so by Proposition 7.8,
∫αpqvq “ ∫pαpqq q d ∫pxder&Xi , vy: q .
The lemma directly follows by Lemmas 7.45 and 7.46.
We have αpqvq a test strategy with size strictly smaller than that of α. By IH there is
x1 : X1 , . . . , xn : Xn $ Npqvq : Xi ,

## PDF page 101

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:101

for each v P V , such that JNpqvq K ” αpqvq . Finally, we define x1 : X1 , . . . , xn : Xn $ M : X as
case xi of
v1 ÞÑ Npqv1 q
v2 ÞÑ Npqv2 q
...
vp ÞÑ Npqvp q

def

“

let x “ xi in
if x “X v1 then Npqv1 q
else if x “X v2 then Npqv2 q
...
else if x “X vp then Npqvp q
else K

where V “ tv1 , . . . , vp u, using the syntactic sugar introduced in Section 1.3. Write
x1 : X1 , . . . , xn : Xn , x : Xi $ M 1 : X
for the iterated if statement, i.e. M is let x “ xi in M 1 . It remains to analyze the positions
of JM K and JM 1 K to show that JM K ” α as required. We start with the positions of JM 1 K.
Lemma 7.48. Consider x P ∫ !p&Xi q and w P ∫˝X.
Then, x $ w P ∫˝JNpqvq K iff there is p P N such that x ` p ¨ rpn ` 1, vqs $ w P ∫˝JM 1 K.
Proof. It is a direct verification, amounting to the correctness of our definition for equality
test and the usual laws for conditionals, that for any v P V we have JM 1 Kd! xder, vy “ JNpqvq K.
The claim then follows by Proposition 7.8 and Lemma 7.46.
It remains to take the interpretation of the let construction into account. Recall that
JM K

“

letXi ,X d! xπi , Λ! pJM 1 Kqy

:

!p&Xi q $ X

where letXi ,X : !pXi & p!Xi ⊸ Xqq $ X. We characterize the positions of letXi ,X as follows.
Lemma 7.49. The non-empty positions of letXi ,X are exactly those of the form
rp1, vqs ` rp2, ppp ¨ rvsq ⊸ wqqs $ w

P

∫p!pXi & p!Xi ⊸ Xqq $ Xq

for v P ∫˝Xi , w P ∫˝X, and p P N.
Proof. A direct analysis of positions reached by complete configurations of letXi ,X .
We can now wrap up, showing that JM K has the same non-empty positions as α.
Lemma 7.50. Consider x P ∫ !p&Xi q and w P ∫˝X.
Then, x $ w P ∫˝JM K iff x “ x1 ` rpi, vqs with x1 $ w P ∫˝JNpqvq K.
Proof. By Lemmas 7.48 and 7.49.
So we have JM K ” α as desired. Summing up, we have proved:
Proposition 7.51. For α : !p&Xi q $ X any test strategy, there is
x1 : X1 , . . . , x n : Xn $ M : X
a term of PCF (not using parallel evaluation) such that JM K ” α.

## PDF page 102

24:102

Vol. 20:3

S. Castellan and P. Clairambault

7.5.2. Finite definability. We may now conclude the proof of finite definability.
Corollary 7.52. Let Γ be a PCF context, A a PCF type, and α : JΓK $ JAK a test strategy.
Then, there is Γ $ M : A such that JM K ” α.
Proof. Up to currying, we write α : !p&1ďiďn Ai q $ X, writing Ai “ Ai,1 Ñ ¨ ¨ ¨ Ñ Ai,pi Ñ Xi
for 1 ď i ď n. We reason by induction on the size of α. By Corollary 7.43, α factors as
α ” fopαq d! xxi α‚q,1 . . . α‚q,pi | 1 ď i ď n, q P Qi y ,
with each Qi finite, and for 1 ď i ď n, q P Qi and 1 ď j ď pi , α‚q,j : !p&Ai q $ Ai,j a test
strategy of size strictly smaller than α. By induction hypothesis, there is
x1 : A1 , . . . , xn : An $ Nq,j : Ai,j
such that JNq,j K ” αq,j . Let us write Qi “ tqi,1 , . . . , qi,ki u. By Proposition 7.51 there is also
xq1,1 : X1 , . . . , xq1,k1 : X1 , . . . , xqn,1 : Xn , . . . , xqn,kn : Xn

$

Mfo : X

such that JMfo K ” fopαq. Then, we define the term x1 : A1 , . . . , xn : An $ M : X as
x1 : A1 , . . . , xn : An $ Mfo rxi Nqi,l ,1 . . . Nqi,l ,pi {xqi,l s : X .

Then we may finally compute
JM K “ JMfo K d! xJxi Nqi,l ,1 . . . Nqi,l ,pi K | 1 ď i ď n, qi,l P Qi y
” JMfo K d! xxi JNq,1 K . . . JNq,n K | 1 ď i ď n, q P Qi y
” fopαq d! xxi α‚q,1 . . . α‚q,pi | 1 ď i ď n, q P Qi y

using the substitution lemma for cartesian closed categories, compatibility of interpretation
with the internal language, the properties of Mfo and Nq,j and that ” is a congruence.

7.6. Full Abstraction for PCF . We may now prove our final full abstraction result.
Theorem 7.53. The model _-Strat!wb,inn is intensionally fully abstract for PCF .
Proof. Consider $ M, N : A such that M „ N , and assume that JM K ­„ JN K, i.e. there is a
test α P _-Stratwb,inn
pJAK, JUKq such that, w.l.o.g., α d! JM K ó and α d! JN K ò.
!
By Corollary 7.28, we assume α is additionally finite. We consider comppαq as defined
in Proposition 7.17. By construction it is well-bracketed, parallel innocent, and finite. By
Proposition 7.17 it is causally well-bracketed, so a test strategy. Proposition 7.17 also states
that comppαq ” α which is a congruence by Corollary 7.9, so
comppαq d! JM K ó ,

comppαq d! JN K ò .

By Corollary 7.52, there is a term x : A $ T : U such that JT K ” comppαq. Defining
the context Cr´s “ pλxA . T q r´s, it follows from the laws of cartesian closed categories that
JCrM sK “ JpλxA . T q M K « JT rM {xsK « JT K d! JM K ” comppαq d! JM K ó ,

and likewise, JCrN sK ” comppαq d! JN K. By Theorem 4.41, CrM s ó. By hypothesis M „ N ,
so CrN s ó. By Theorem 4.41 again, JCrN sK ó, hence comppαq d! JN K ó, contradiction.
We may finally answer our main question positively, with the following theorem.

## PDF page 103

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:103

supports parallel innocence and sequentiality, s.t.
Theorem 7.54. The model _-Stratwb
!

is fully abstract for IA ,
_-Stratwb
!
_-Strat!wb,inn is fully abstract for PCF ,
_-Strat!wb,seq is fully abstract for IA ,
_-Stratwb,seq,inn
is fully abstract for PCF ,
!
Thus parallel innocence exactly bans interference, and sequentiality exactly bans parallelism. Through this theorem, we have successfully disentangled parallelism and interference.
8. Conclusion

It is puzzling that disentangling parallelism and interference requires such an intricate
machinery whereas the original semantic cube arose almost “by accident” from minor
variations of the Hyland-Ong model of PCF.
Our interpretation is that computational effects may be organized in distinct categories.
Some effects, such as interference and control, bring more freedom as to how execution
and its control flow explores a piece of code. Once a sufficiently general mathematical
description of the control flow is given (such as the original Hyland-Ong setting for sequential
deterministic computation), this additional freedom may be studied and characterized. In
contrast, other effects such as non-determinism and parallelism, affect the inherent structure
of execution itself: non-determinism quite explicitly so by generating non-deterministic
branching, and parallelism in a more DAG-like fashion – we refer to both under the umbrella
name “branching effects”. What our paper demonstrates – along with earlier papers on
non-deterministic innocence [CCW14, TO15] – is that if we aim to realize fully the “unified
semantic landscape” of Abramsky’s programme, we must first deal with branching effects.
Non-branching effects should follow by characterizing the causal patterns they allow29.
What other branching effects are around? One currently at the focus of the semantics
community is probabilistic choice. By itself, the probabilistic branching structure is not
much harder than non-deterministic choice [TO14, CCPW18]. However its interaction with
non-deterministic and parallel branching is a significant challenge, and one of the remaining
scientific and technical barriers for a truly unified game semantics landscape.
Acknowledgments. First we would like to thank Glynn Winskel. Though he has not
participated in the developments in this paper per se, we rely deeply on his pioneering work
- and our subsequent collaborations - on concurrent games. We owe a lot to his insight.
This work was supported by the ANR project DyVerSe (ANR-19-CE48-0010-01); and
by Labex MiLyon (ANR-10-LABX-0070) of Université de Lyon, within the program “Investissements d’Avenir” (ANR-11-IDEX-0007), operated by the French ANR.
References
[AHM98]

[AJ09]

Samson Abramsky, Kohei Honda, and Guy McCusker. A fully abstract game semantics for general
references. In Thirteenth Annual IEEE Symposium on Logic in Computer Science, Indianapolis,
Indiana, USA, June 21-24, 1998, pages 334–344, 1998. doi:10.1109/LICS.1998.705669.
Samson Abramsky and Radha Jagadeesan. Game semantics for access control. Electr. Notes
Theor. Comput. Sci., 249:135–156, 2009. doi:10.1016/j.entcs.2009.07.088.

29The line is not always so clear between branching and non-branching effects: for instance, in a sequential

setting interference is non-branching, but in a parallel setting it generates non-deterministic choice.

## PDF page 104

24:104

S. Castellan and P. Clairambault

Vol. 20:3

Samson Abramsky, Radha Jagadeesan, and Pasquale Malacaria. Full abstraction for PCF. Inf.
Comput., 163(2):409–470, 2000. doi:10.1006/inco.2000.2930.
[AM96]
Samson Abramsky and Guy McCusker. Linearity, sharing and state: a fully abstract game
semantics for Idealized Algol with active expressions. Electron. Notes Theor. Comput. Sci.,
3:2–14, 1996. doi:10.1016/S1571-0661(05)80398-6.
[AM99a]
Samson Abramsky and Guy McCusker. Game semantics. In Computational logic, 1999.
[AM99b]
Samson Abramsky and Paul-André Melliès. Concurrent games and full completeness. In 14th
Annual IEEE Symposium on Logic in Computer Science, Trento, Italy, July 2-5, 1999, pages
431–442. IEEE Computer Society, 1999. doi:10.1109/LICS.1999.782638.
[Cas17]
Simon Castellan. Concurrent structures in game semantics. (Structures concurrentes en
sémantique des jeux). PhD thesis, University of Lyon, France, 2017. URL: https://tel.
archives-ouvertes.fr/tel-01587718.
[CC16]
Simon Castellan and Pierre Clairambault. Causality vs. interleavings in concurrent game semantics. In Josée Desharnais and Radha Jagadeesan, editors, 27th International Conference
on Concurrency Theory, CONCUR 2016, August 23-26, 2016, Québec City, Canada, volume 59 of LIPIcs, pages 32:1–32:14. Schloss Dagstuhl - Leibniz-Zentrum für Informatik, 2016.
doi:10.4230/LIPIcs.CONCUR.2016.32.
[CCHW18] Simon Castellan, Pierre Clairambault, Jonathan Hayman, and Glynn Winskel. Non-angelic
concurrent game semantics. In Christel Baier and Ugo Dal Lago, editors, Foundations of Software
Science and Computation Structures - 21st International Conference, FOSSACS 2018, Held
as Part of the European Joint Conferences on Theory and Practice of Software, ETAPS 2018,
Thessaloniki, Greece, April 14-20, 2018, Proceedings, volume 10803 of Lecture Notes in Computer
Science, pages 3–19. Springer, 2018. doi:10.1007/978-3-319-89366-2\_1.
[CCPW18] Simon Castellan, Pierre Clairambault, Hugo Paquet, and Glynn Winskel. The concurrent game
semantics of probabilistic PCF. In Proceedings of the 33rd Annual ACM/IEEE Symposium on
Logic in Computer Science, LICS 2018, Oxford, UK, July 09-12, 2018, pages 215–224, 2018.
doi:10.1145/3209108.3209187.
[CCRW17] Simon Castellan, Pierre Clairambault, Silvain Rideau, and Glynn Winskel. Games and strategies
as event structures. Logical Methods in Computer Science, 13(3), 2017. doi:10.23638/LMCS-13(3:
35)2017.
[CCW14] Simon Castellan, Pierre Clairambault, and Glynn Winskel. Symmetry in concurrent games.
In Thomas A. Henzinger and Dale Miller, editors, Joint Meeting of the Twenty-Third EACSL
Annual Conference on Computer Science Logic (CSL) and the Twenty-Ninth Annual ACM/IEEE
Symposium on Logic in Computer Science (LICS), CSL-LICS ’14, Vienna, Austria, July 14 - 18,
2014, pages 28:1–28:10. ACM, 2014. doi:10.1145/2603088.2603141.
[CCW15] Simon Castellan, Pierre Clairambault, and Glynn Winskel. The parallel intensionally fully
abstract games model of PCF. In 30th Annual ACM/IEEE Symposium on Logic in Computer
Science, LICS 2015, Kyoto, Japan, July 6-10, 2015, pages 232–243. IEEE Computer Society,
2015. doi:10.1109/LICS.2015.31.
[CCW19] Simon Castellan, Pierre Clairambault, and Glynn Winskel. Thin games with symmetry and concurrent Hyland-Ong games. Log. Methods Comput. Sci., 15(1), 2019. doi:10.23638/LMCS-15(1:
18)2019.
[CD15]
Pierre Clairambault and Peter Dybjer. Game semantics and normalization by evaluation. In
Andrew M. Pitts, editor, Foundations of Software Science and Computation Structures - 18th
International Conference, FoSSaCS 2015, Held as Part of the European Joint Conferences on
Theory and Practice of Software, ETAPS 2015, London, UK, April 11-18, 2015. Proceedings,
volume 9034 of Lecture Notes in Computer Science, pages 56–70. Springer, 2015. doi:10.1007/
978-3-662-46678-0\_4.
[CdV20]
Pierre Clairambault and Marc de Visme. Full abstraction for the quantum lambda-calculus. Proc.
ACM Program. Lang., 4(POPL):63:1–63:28, 2020. doi:10.1145/3371131.
[CH10]
Pierre Clairambault and Russ Harmer. Totality in arena games. Ann. Pure Appl. Logic, 161(5):673–
689, 2010. doi:10.1016/j.apal.2009.07.016.
[Cur98]
Pierre-Louis Curien. Abstract Böhm trees. Mathematical Structures in Computer Science, 8(6):559–
591, 1998.
[Cur06]
Pierre-Louis Curien. Notes on game semantics. 2006. Unpublished.
[AJM00]

## PDF page 105

Vol. 20:3

[CY19]

[DH00]

[DHR96]

[dV20]
[FP09]

[GG12]

[Gir87]
[GM03]
[GM08]
[GMO06]
[Gou17]
[Gri90]

[GT12]

[Har04]
[HHM07]

[HM99]

[HO00]
[Jab15]

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:105

Simon Castellan and Nobuko Yoshida. Two sides of the same coin: session types and game semantics: a synchronous side and an asynchronous side. Proc. ACM Program. Lang., 3(POPL):27:1–
27:29, 2019. doi:10.1145/3290340.
Vincent Danos and Russ Harmer. Probabilistic game semantics. In 15th Annual IEEE Symposium
on Logic in Computer Science, Santa Barbara, California, USA, June 26-29, 2000, pages 204–213.
IEEE Computer Society, 2000. doi:10.1109/LICS.2000.855770.
Vincent Danos, Hugo Herbelin, and Laurent Regnier. Game semantics & abstract machines. In
Proceedings, 11th Annual IEEE Symposium on Logic in Computer Science, New Brunswick, New
Jersey, USA, July 27-30, 1996, pages 394–405. IEEE Computer Society, 1996. doi:10.1109/
LICS.1996.561456.
Marc de Visme. Quantum Game Semantics. PhD thesis, University of Lyon, France, 2020.
Claudia Faggian and Mauro Piccolo. Partial orders, event structures and linear strategies. In
Pierre-Louis Curien, editor, Typed Lambda Calculi and Applications, 9th International Conference,
TLCA 2009, Brasilia, Brazil, July 1-3, 2009. Proceedings, volume 5608 of Lecture Notes in
Computer Science, pages 95–111. Springer, 2009. doi:10.1007/978-3-642-02273-9\_9.
Murdoch Gabbay and Dan R. Ghica. Game semantics in the nominal model. In Ulrich Berger
and Michael W. Mislove, editors, Proceedings of the 28th Conference on the Mathematical
Foundations of Programming Semantics, MFPS 2012, Bath, UK, June 6-9, 2012, volume
286 of Electronic Notes in Theoretical Computer Science, pages 173–189. Elsevier, 2012. doi:
10.1016/j.entcs.2012.08.012.
Jean-Yves Girard. Linear logic. Theor. Comput. Sci., 50:1–102, 1987. doi:10.1016/
0304-3975(87)90045-4.
Dan R. Ghica and Guy McCusker. The regular-language semantics of second-order Idealized
Algol. Theor. Comput. Sci., 309(1-3):469–502, 2003. doi:10.1016/S0304-3975(03)00315-3.
Dan R. Ghica and Andrzej S. Murawski. Angelic semantics of fine-grained concurrency. Ann.
Pure Appl. Log., 151(2-3):89–114, 2008. doi:10.1016/j.apal.2007.10.005.
Dan R. Ghica, Andrzej S. Murawski, and C.-H. Luke Ong. Syntactic control of concurrency.
Theor. Comput. Sci., 350(2-3):234–251, 2006. doi:10.1016/j.tcs.2005.10.032.
Jean Goubault-Larrecq. Isomorphism theorems between models of mixed choice. Math. Struct.
Comput. Sci., 27(6):1032–1067, 2017. doi:10.1017/S0960129515000547.
Timothy Griffin. A formulae-as-types notion of control. In Frances E. Allen, editor, Conference
Record of the Seventeenth Annual ACM Symposium on Principles of Programming Languages,
San Francisco, California, USA, January 1990, pages 47–58. ACM Press, 1990. doi:10.1145/
96709.96714.
Dan R. Ghica and Nikos Tzevelekos. A system-level game semantics. In Ulrich Berger and
Michael W. Mislove, editors, Proceedings of the 28th Conference on the Mathematical Foundations
of Programming Semantics, MFPS 2012, Bath, UK, June 6-9, 2012, volume 286 of Electronic
Notes in Theoretical Computer Science, pages 191–211. Elsevier, 2012. doi:10.1016/j.entcs.
2012.08.013.
Russ Harmer. Innocent game semantics. Lecture notes, 2004.
Russ Harmer, Martin Hyland, and Paul-André Melliès. Categorical combinatorics for innocent
strategies. In 22nd IEEE Symposium on Logic in Computer Science (LICS 2007), 10-12 July
2007, Wroclaw, Poland, Proceedings, pages 379–388, 2007. doi:10.1109/LICS.2007.14.
Russ Harmer and Guy McCusker. A fully abstract game semantics for finite nondeterminism.
In 14th Annual IEEE Symposium on Logic in Computer Science, Trento, Italy, July 2-5, 1999,
pages 422–430. IEEE Computer Society, 1999. doi:10.1109/LICS.1999.782637.
J. M. E. Hyland and C.-H. Luke Ong. On full abstraction for PCF: I, II, and III. Inf. Comput.,
163(2):285–408, 2000. doi:10.1006/inco.2000.2917.
Guilhem Jaber. Operational nominal game semantics. In Andrew M. Pitts, editor, Foundations
of Software Science and Computation Structures - 18th International Conference, FoSSaCS 2015,
Held as Part of the European Joint Conferences on Theory and Practice of Software, ETAPS
2015, London, UK, April 11-18, 2015. Proceedings, volume 9034 of Lecture Notes in Computer
Science, pages 264–278. Springer, 2015. doi:10.1007/978-3-662-46678-0\_17.

## PDF page 106

24:106

[Lai97]

[Lai01a]

[Lai01b]
[Lai04]

[Ler09]
[Lev14]
[Loa01]
[LS88]
[LS14]

[McC98]
[McC03]

[Mel03]
[Mel04]

[Mel05]

[Mel09]
[Mel19]
[MM07]

[MT10]
[MT13]

S. Castellan and P. Clairambault

Vol. 20:3

James Laird. Full abstraction for functional languages with control. In Proceedings, 12th Annual
IEEE Symposium on Logic in Computer Science, Warsaw, Poland, June 29 - July 2, 1997, pages
58–67. IEEE Computer Society, 1997. doi:10.1109/LICS.1997.614931.
James Laird. A fully abstract game semantics of local exceptions. In 16th Annual IEEE Symposium
on Logic in Computer Science, Boston, Massachusetts, USA, June 16-19, 2001, Proceedings,
pages 105–114. IEEE Computer Society, 2001. doi:10.1109/LICS.2001.932487.
James Laird. A game semantics of Idealized CSP. Electr. Notes Theor. Comput. Sci., 45:232–257,
2001.
James Laird. A calculus of coroutines. In Josep Dı́az, Juhani Karhumäki, Arto Lepistö, and
Donald Sannella, editors, Automata, Languages and Programming: 31st International Colloquium,
ICALP 2004, Turku, Finland, July 12-16, 2004. Proceedings, volume 3142 of Lecture Notes in
Computer Science, pages 882–893. Springer, 2004. doi:10.1007/978-3-540-27836-8\_74.
Xavier Leroy. Formal verification of a realistic compiler. Commun. ACM, 52(7):107–115, 2009.
doi:10.1145/1538788.1538814.
Paul Blain Levy. Transition systems over games, 2014. Talk at the Chocola seminar.
Ralph Loader. Finitary PCF is not decidable. Theor. Comput. Sci., 266(1-2):341–364, 2001.
doi:10.1016/S0304-3975(00)00194-8.
Joachim Lambek and Philip J Scott. Introduction to higher-order categorical logic, volume 7.
Cambridge University Press, 1988.
Paul Blain Levy and Sam Staton. Transition systems over games. In Joint Meeting of the TwentyThird EACSL Annual Conference on Computer Science Logic (CSL) and the Twenty-Ninth
Annual ACM/IEEE Symposium on Logic in Computer Science (LICS), CSL-LICS ’14, Vienna,
Austria, July 14 - 18, 2014, pages 64:1–64:10, 2014. doi:10.1145/2603088.2603150.
Guy McCusker. Games and full abstraction for a functional metalanguage with recursive types.
CPHC/BCS distinguished dissertations. Springer, 1998.
Guy McCusker. On the semantics of the bad-variable constructor in Algol-like languages. In
MFPS, volume 83 of Electronic Notes in Theoretical Computer Science, pages 169–186. Elsevier,
2003.
Paul-André Melliès. Asynchronous games 1: A group-theoretic formulation of uniformity. Manuscript, Available online, 2003.
Paul-André Melliès. Asynchronous games 2: The true concurrency of innocence. In Philippa
Gardner and Nobuko Yoshida, editors, CONCUR 2004 - Concurrency Theory, 15th International
Conference, London, UK, August 31 - September 3, 2004, Proceedings, volume 3170 of Lecture
Notes in Computer Science, pages 448–465. Springer, 2004. doi:10.1007/978-3-540-28644-8\
_29.
Paul-André Melliès. Asynchronous games 4: A fully complete model of propositional linear logic.
In 20th IEEE Symposium on Logic in Computer Science (LICS 2005), 26-29 June 2005, Chicago,
IL, USA, Proceedings, pages 386–395. IEEE Computer Society, 2005. doi:10.1109/LICS.2005.6.
Paul-André Melliès. Categorical semantics of linear logic. Panoramas et Synthèses, 2009.
Paul-André Melliès. Categorical combinatorics of scheduling and synchronization in game semantics. Proc. ACM Program. Lang., 3(POPL):23:1–23:30, 2019. doi:10.1145/3290336.
Paul-André Melliès and Samuel Mimram. Asynchronous games: Innocence without alternation.
In Luı́s Caires and Vasco Thudichum Vasconcelos, editors, CONCUR 2007 - Concurrency
Theory, 18th International Conference, CONCUR 2007, Lisbon, Portugal, September 3-8, 2007,
Proceedings, volume 4703 of Lecture Notes in Computer Science, pages 395–411. Springer, 2007.
doi:10.1007/978-3-540-74407-8\_27.
Paul-André Melliès and Nicolas Tabareau. Resource modalities in tensor logic. Ann. Pure Appl.
Log., 161(5):632–653, 2010. doi:10.1016/j.apal.2009.07.018.
Andrzej S. Murawski and Nikos Tzevelekos. Deconstructing general references via game semantics.
In Frank Pfenning, editor, Foundations of Software Science and Computation Structures - 16th
International Conference, FOSSACS 2013, Held as Part of the European Joint Conferences on
Theory and Practice of Software, ETAPS 2013, Rome, Italy, March 16-24, 2013. Proceedings,
volume 7794 of Lecture Notes in Computer Science, pages 241–256. Springer, 2013. doi:10.1007/
978-3-642-37075-5\_16.

## PDF page 107

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:107

Andrzej S. Murawski. On program equivalence in languages with ground-type references. In 18th
IEEE Symposium on Logic in Computer Science (LICS 2003), 22-25 June 2003, Ottawa, Canada,
Proceedings, page 108. IEEE Computer Society, 2003. doi:10.1109/LICS.2003.1210050.
[Mur07]
Andrzej S. Murawski. Bad variables under control. In Jacques Duparc and Thomas A. Henzinger,
editors, Computer Science Logic, 21st International Workshop, CSL 2007, 16th Annual Conference
of the EACSL, Lausanne, Switzerland, September 11-15, 2007, Proceedings, volume 4646 of Lecture
Notes in Computer Science, pages 558–572. Springer, 2007. doi:10.1007/978-3-540-74915-8\
_41.
Andrzej S. Murawski. Full abstraction without synchronization primitives. Electr. Notes Theor.
[Mur10]
Comput. Sci., 265:423–436, 2010. doi:10.1016/j.entcs.2010.08.025.
[Ong02]
C.-H. Luke Ong. Observational equivalence of 3rd-order Idealized Algol is decidable. In 17th IEEE
Symposium on Logic in Computer Science (LICS 2002), 22-25 July 2002, Copenhagen, Denmark,
Proceedings, pages 245–256. IEEE Computer Society, 2002. doi:10.1109/LICS.2002.1029833.
[Paq20]
Hugo Paquet. Probabilistic concurrent game semantics. PhD thesis, PhD thesis, University of
Cambridge, 2020.
Gordon D. Plotkin. LCF considered as a programming language. Theor. Comput. Sci., 5(3):223–
[Plo77]
255, 1977.
[Plo81]
Gordon D. Plotkin. Post-graduate lecture notes in advanced domain theory (incorporating the
”Pisa Notes”). Dept. of Computer Science, Univ. of Edinburgh, 1981.
[RW11]
Silvain Rideau and Glynn Winskel. Concurrent strategies. In Proceedings of the 26th Annual
IEEE Symposium on Logic in Computer Science, LICS 2011, June 21-24, 2011, Toronto, Ontario,
Canada, pages 409–418. IEEE Computer Society, 2011. doi:10.1109/LICS.2011.13.
[SBCA15] Gordon Stewart, Lennart Beringer, Santiago Cuellar, and Andrew W. Appel. Compositional CompCert. In Sriram K. Rajamani and David Walker, editors, Proceedings of the 42nd Annual ACM
SIGPLAN-SIGACT Symposium on Principles of Programming Languages, POPL 2015, Mumbai,
India, January 15-17, 2015, pages 275–287. ACM, 2015. doi:10.1145/2676726.2676985.
[SYW` 16] Sam Staton, Hongseok Yang, Frank D. Wood, Chris Heunen, and Ohad Kammar. Semantics for
probabilistic programming: higher-order functions, continuous distributions, and soft constraints.
In Martin Grohe, Eric Koskinen, and Natarajan Shankar, editors, Proceedings of the 31st Annual
ACM/IEEE Symposium on Logic in Computer Science, LICS ’16, New York, NY, USA, July
5-8, 2016, pages 525–534. ACM, 2016. doi:10.1145/2933575.2935313.
[TO14]
Takeshi Tsukada and C.-H. Luke Ong. Innocent strategies are sheaves over plays - deterministic,
non-deterministic and probabilistic innocence. CoRR, abs/1409.2764, 2014. URL: http://arxiv.
org/abs/1409.2764, arXiv:1409.2764.
[TO15]
Takeshi Tsukada and C.-H. Luke Ong. Nondeterminism in game semantics via sheaves. In 30th
Annual ACM/IEEE Symposium on Logic in Computer Science, LICS 2015, Kyoto, Japan, July
6-10, 2015, pages 220–231. IEEE Computer Society, 2015. doi:10.1109/LICS.2015.30.
Matthijs Vákár, Ohad Kammar, and Sam Staton. A domain theory for statistical probabilistic
[VKS19]
programming. Proc. ACM Program. Lang., 3(POPL):36:1–36:29, 2019. doi:10.1145/3290349.
[Win07]
Glynn Winskel. Event structures with symmetry. Electr. Notes Theor. Comput. Sci., 172:611–652,
2007.
[Win12]
Glynn Winskel. Deterministic concurrent strategies. Formal Asp. Comput., 24(4-6):647–660, 2012.
doi:10.1007/s00165-012-0235-6.
[Win13]
Glynn Winskel. Strategies as profunctors. In Frank Pfenning, editor, Foundations of Software
Science and Computation Structures - 16th International Conference, FOSSACS 2013, Held as
Part of the European Joint Conferences on Theory and Practice of Software, ETAPS 2013, Rome,
Italy, March 16-24, 2013. Proceedings, volume 7794 of Lecture Notes in Computer Science, pages
418–433. Springer, 2013. doi:10.1007/978-3-642-37075-5\_27.
[Mur03]

## PDF page 108

24:108

S. Castellan and P. Clairambault

Vol. 20:3

Appendix A. Concurrent Games Toolbox
A.1. Event Structures and Maps. We start with recalling maps of event structures.
Definition A.1. Consider E, F two es. A map of event structures from E to F is a
function f : |E| Ñ |F | satisfying the following two conditions:
valid: for all x P C pEq, we have f x P C pF q,
local injectivity: for all e1 , e2 P x P C pEq, if f e1 “ f e2 then e1 “ e2 .
If E and F are esps, a map of esps is additionally required to preserve polarities.
Lemma A.2. Consider f : E Ñ F a map of event structures, and e1 , e2 P x P C pEq.
If f pe1 q ďF f pe2 q, then e1 ďE e2 .
Proof. Seeking a contradiction, assume we do not have e1 ďE e2 . This means that e1 R re2 sE .
But re2 sE P C pEq, so f re2 sE is down-closed. Moreover, f e2 P f re2 sE , so f e1 P f re2 sE . So
there is e11 P re2 sE such that f e11 “ f e1 . Finally, re2 sE Ď x, so e1 , e11 P x P C pEq. Hence, by
local injectivity, e1 “ e11 . We deduce that e1 P re2 sE after all, contradiction.
A.2. Basic Properties of Strategies. We gather some basic properties.
Lemma A.3. Consider A an arena, σ : A a causal strategy, and m, n P |σ|.
If m _σ n, then polpmq ‰ polpnq.

Proof. If polpmq “ polpnq, then by courteous we have Bσ pmq _A Bτ pnq as well. But since
arenas are alternating, this is absurd.
Lemma A.4. Consider A an arena, σ : A a causal strategy, and m, n´ P |σ| compatible.
Then, m _σ n iff Bσ pmq _A Bσ pnq.

Proof. If. Assume Bσ pmq _A Bσ pnq. Since rnsσ P C pσq and Bσ is a map of event structures,
Bσ rnsσ P C pAq, so it is down-closed. Thus, there is m1 P rnsσ such that Bσ pm1 q “ Bσ pmq.
In particular, n cannot be minimal, so there is m2 _σ n. By courteous, since n is negative
we have Bσ pm2 q _A Bσ pnq. But A is forestial, so Bσ pm2 q “ Bσ pmq. Now, since m, n are
compatible they appear in a configuration x P C pσq, and in particular m, m2 P x. Thus,
m “ m2 by local injectivity. Only if. If m _σ n´ , then Bσ pmq _A Bσ pnq by courteous.

Lemma A.5. Consider A an arena, σ : A a causal strategy, and m´ P |σ| s.t. Bσ m
non-minimal. Then, there is a unique n _σ m.

Proof. Existence. Write a _ Bσ pmq, which is unique since A is forestial. Since rmsσ P C pσq,
we have Bσ rmsσ P C pAq, therefore it is down-closed and must contain a. Therefore, there is
n ďσ m such that Bσ pnq “ a. By Lemma A.4, we then have n _σ m as required.
Uniqueness. If n1 _σ m and n2 _σ m, by courteous Bσ n1 _A Bσ m and Bσ n2 _A Bσ m.
But then, Bσ n1 “ Bσ n2 as A is forestial. So n1 “ n2 as Bσ is locally injective.
Lemma A.6. Consider A an arena, σ : A a causal strategy, and m, n1 , n2 P |σ|.
If n1 _σ m and n2 _σ m with n1 , n2 distinct, then polpmq “ `.

Proof. Seeking a contradiction, assume polpmq “ ´. Then, by courteous, we have Bσ pn1 q _A
Bσ pmq and Bσ pn2 q _A Bσ pmq. As A is forestial, Bσ pn1 q “ Bσ pn2 q. As n1 , n2 P rmsσ P C pσq,
we have n1 “ n2 by local injectivity, contradiction.

## PDF page 109

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:109

Lemma A.7. Consider A an arena, σ : A a causal strategy, and m` P x P C pσq.
Then, m is maximal in x iff Bσ m is maximal in Bσ x.
Proof. If. Assume Bσ m is maximal in Bσ x. Seeking a contradiction, assume that m _σ n.
By Lemma A.3, polpnq “ ´. Therefore, by courteous, Bσ pmq _A Bσ pnq, contradiction.
Only if. Straightforward by Lemma A.2.
´
Lemma A.8. Consider A an arena, σ : A a causal strategy, and m´
1 , m2 P |σ|. If m1 and
m2 are in minimal conflict in σ, then Bσ pm1 q and Bσ pm2 q are in minimal conflict in A.

Proof. We first prove that Bσ pm1 q and Bσ pm2 q are in conflict. Seeking a contradiction,
assume that it is not the case. Then, as m1 and m2 are in minimal conflict, we have
Bσ prm1 sσ Y rm2 sσ q P C pAq. Hence, by receptive, there is a unique m12 P |σ| such that
rm1 sσ Y rm2 qσ $σ m12
with Bσ pm12 q “ Bσ pm2 q – where rm2 qσ “ tn P |σ| | n ăσ m2 u. But then, by Lemma A.4,
m2 is minimal in σ iff m12 is minimal in σ, and so m2 “ m12 by receptive, contradicting that
m1 #σ m2 . Otherwise, consider n _σ m2 and n1 _σ m12 . Then, by courteous,
Bσ pnq _A Bσ pm2 q ,

Bσ pn1 q _A Bσ pm12 q ,

but then Bσ pnq “ Bσ pn1 q since A is forestial. But n, n1 P rm1 sσ Y rm2 qσ P C pσq, so we must
have n “ n1 by locally injectivity. By Lemma A.5, n is the unique predecessor of m2 and
m12 . So, rnsσ $σ m2 and rnsσ $σ m12 with the same image. So m2 “ m12 , contradiction.
Finally, minimality of the conflict is obvious from that of m1 and m2 .

Appendix B. Construction of Alternating Strategies
In this second section of the appendix, we give more details on the construction of Œ-Strat.
First, a warning: quite a few superficial complications come from the general construction
A ⊸ B for B non-pointed, with morphisms from A to B being strategies on A ⊸ B. An
alternative is to only consider A ⊸ B for B strict. Then we do not have a symmetric
monoidal closed category, only an exponential ideal. This would be sufficient for the languages
considered in this paper, however, we opted to link with traditional categorical models.
B.1. Basic Categorical Structure. We start by establishing the categorical structure.
B.1.1. Arrow arena. First, we give postponed proofs on the construction of the arrow arena.
Lemma 2.5. Consider A and B two ´-arenas.
Then, there is a unique #A⊸B making A ⊸ B a ´-arena such that for all down-closed
finite x Ď |A ⊸ B|, x P C pA ⊸ Bq iff χA,B x P C pAK ∥ Bq with χA,B injective on x.
Proof. Existence. We set #A⊸B as the following relation:
p2, b1 q #A⊸B p2, b2 q
p1, pb, a1 qq #A⊸B p1, pb, a2 qq
p2, b1 q #A⊸B p1, pb2 , aqq
p1, pb1 , aqq #A⊸B p2, b2 q
p1, pb1 , a1 qq #A⊸B p1, pb2 , a2 qq

ô
ô
ô
ô
ô

b1 #B b2
a1 #A a2
b1 #B b2
b1 #B b2
pb1 #B b2 q _ pminpa1 q “ minpa2 qq _ pa1 #A a2 q ,

## PDF page 110

24:110

Vol. 20:3

S. Castellan and P. Clairambault

ε æ A, B
u rr, cs æ A, B
u rm, bsc æ A, B
u rl, asb,c æ A, B

“
“
“
“

ε
u æ A, B
pu æ A, Bq rr, bs
pu æ A, Bq rl, asb

ε æ B, C
u rr, cs æ B, C
u rm, bsc æ B, C
u rl, asb,c æ B, C

“
“
“
“

ε
pu æ B, Cq rr, cs
pu æ B, Cq rl, bsc
u æ B, C

ε æ A, C
u rr, cs æ A, C
u rm, bsc æ A, C
u rr, asb,c æ A, C

“
“
“
“

ε
pu æ A, Cq rr, cs
u æ A, C
pu æ A, Cq rl, asc

Figure 68: Restrictions of pre-interactions
where b1 , b2 are assumed distinct, all other pairs left consistent, and with minpaq the unique
minimal antecedent of a. It is routine that this conflict makes A ⊸ B a ´-arena.
Now, we check the additional condition. Consider x Ď |A ⊸ B| down-closed, written as
x “ p∥bPI xA,b q ∥ xB
where I is a subset of the minimal events of B. Then, we show that x P C pA ⊸ Bq iff
χA,B x “ pYbPI xA,b q ∥ xB P C pA $ Bq
and χA,B is injective on x. Only if is a direct verification. For if, if χA,B x P C pA ⊸ Bq
then the only possible conflict in x is of the form, with b1 #B b2 or minpa1 q “ minpa2 q:
p1, pb1 , a1 qq #A⊸B p1, pb2 , a2 qq
In the former case, by down-closure, p2, b1 q, p2, b2 q P x, contradicting χA,B x P C pA $ Bq.
In the latter case, by down-closure, p1, pb1 , minpa1 qqq, p1, pb2 , minpa2 qqq P x – but they have
the same image through χA,B , contradicting that it should be injective on x. Uniqueness
follows as with fixed events, an event structure is determined by configurations.

B.1.2. Composition. Consider fixed A, B and C three ´-arenas, and σ : A ⊸ B, τ : B ⊸ C
alternating prestrategies. Recall from the main text:
Definition B.1. A pre-interaction on A, B, C is u P |pA ⊸ Bq ⊸ C|˚ satisfying:
valid : @1 ď i ď n, ts1 , . . . , si u P C ppA ⊸ Bq ⊸ Cq
Remember that in A ⊸ B, events are either p2, bq for b P |B|, or p1, pb, aqq for b P minpBq
and a P |A|. By convention, in this section, we write rr, bs for p2, bq and rl, asb for p1, pb, aqq.
In that case, rr, bs is the unique immediate predecessor of rl, asb , i.e. its justifier. Similarly,
in pA ⊸ Bq ⊸ C, events can be p2, cq written rr, cs; p1, pc, p2, bqqq written rm, bsc ; and
p1, pc, p1, pb, aqqqq written rl, asb,c ; we respectively say that they are in C, in B, or in A.
Using this, we define in Figure 68 three restrictions of a pre-interaction u, namely
u æ A, B P |A ⊸ B|˚ , u æ B, C P |B ⊸ C|˚ , and u æ A, C P |A ⊸ C|˚ . Now we set:
Definition B.2. An interaction u P τ f σ between σ and τ is a pre-interaction u s.t.
u æ A, B P σ ,

u æ B, C P τ ,

u æ A, C P Œ-PlayspA ⊸ Cq .

The composition of σ and τ is τ d σ “ tu æ A, C | u P τ f σu.
The first step is to ensure that τ d σ is a prestrategy, and that if σ and τ are strategies,
then so is τ d σ. We start with the conditions of Definition 2.8, postponing uniformity.
Non-empty and prefix-closed follow from those on σ and τ . For deterministic, we need more
tools. The main tool to study the interaction of alternating strategies is the state analysis
of plays and interactions. Recall from Section 6.1.3 that s alternating is in state O if it has
even length, and in state P otherwise. Then, we have the following property:

## PDF page 111

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:111

Lemma B.3. If u P τ f σ, then we are in one of the following three cases:
(1) u æ A, B, u æ B, C and u æ A, C are respectively in state O, O, O.
(2) u æ A, B, u æ B, C and u æ A, C are respectively in state O, P , P .
(3) u æ A, B, u æ B, C and u æ A, C are respectively in state P , O, P .
Proof. Standard argument, direct by induction on u.
Next, we can prove the key property of the composition of alternating strategies.
Lemma B.4. Consider s P τ d σ of even length.
Then, there is a unique witness u P τ f σ such that u æ A, C “ s.
Proof. Existence is obvious by definition.
Uniqueness. Seeking a contradiction, consider u1 , u2 P τ f σ distinct such that u1 æ
A, C “ u2 æ A, C “ s. First, since s has even length, ui æ A, C is in state O, so u1 and u2
must be in state (1) of Lemma B.3. It follows that their immediate prefix cannot be in
state (1), from which it follows last move is visible (i.e. in A or C). So, u1 and u2 cannot
be comparable for the prefix order. Therefore, there is u1 maximal such that u1 Ď u1 and
u1 Ď u2 , say we have u1 m1 Ď u1 and u1 m2 Ď u2 for m1 , m2 distinct. By Lemma B.3, u1 is in
one of the states (1), (2) or (3). If it is in state (1), then the next moves m1 and m2 are in
u æ A, C “ s, so they cannot be distinct. Say u1 is in state (3) – the case (2) is similar but
simpler. Necessarily, m1 and m2 are in A or B, so that
u1 m1 æ A, B “ pu1 æ A, Bqn1

u1 m2 æ A, B “ pu1 æ A, Bqn2

are two plays of σ with even length – so that n1 “ n2 , by determinism. From the definition
of restriction, the only case where m1 ‰ m2 with n1 “ n2 is if m1 “ rl, asb,c , m2 “ rl, asb,c1
with c ‰ c1 , so n1 “ n2 “ rl, asb . Then, as u1 satisfies condition valid, this entails that their
immediate dependencies rm, bsc , rm, bsc1 P |u1 | as well – impossible since rm, bsc # rm, bsc1 .
It is then straightforward to prove that τ d σ satisfies deterministic.
Proposition B.5. We have that τ d σ : A ⊸ C is a prestrategy.
Moreover, if σ and τ are strategies, then so is τ d σ.
Proof. To obtain a prestrategy, it remains that τ d σ satisfies deterministic. Consider
`
sn`
1 , sn2 P τ d σ. Consider u1 m1 , u2 m2 P τ f σ their unique witness as given by Lemma
B.4. We reason as in Lemma B.4: if there is a diverging point between u1 m1 and u2 m2 , by
Lemma B.3 the divergence can be attributed to either σ or τ , contradicting determinism.
Now, assume that σ and τ satisfy condition receptive. Consider s P τ d σ such that
´
sm P Œ-PlayspA ⊸ Cq. More precisely, assume that m “ rpl, aqsc as the case in C is simpler.
Consider now u P τ f σ such that u æ A, C “ s; necessarily u is in state (1) of Lemma B.3.
Now, as m is negative its immediate predecessor of m in A ⊸ C is some rpl, a1 qsc in s. Since
s “ u æ A, C, it corresponds to some rpl, a1 qsb,c in u, for some b P minpBq. But then, it is
a direct verification that pu æ A, Bqrpl, aqsb P Œ-PlayspA ⊸ Bq, so pu æ A, Bqrpl, aqsb P σ by
receptive. Therefore, urpl, aqsb,c P τ f σ witnessing that sm P τ d σ as required.
Note that this argument and the prior state analysis of Lemma B.3 are also found in
the proof of composition of sequentiality for causal strategies in Section 6.1.3.

## PDF page 112

24:112

S. Castellan and P. Clairambault

Vol. 20:3

B.1.3. Associativity. We now sketch associativity, which follows standard lines, see e.g.
[Har04]. Let us fix σ : A ⊸ B, τ : B ⊸ C and δ : C ⊸ D three alternating prestrategies.
The first step is to define a notion of interaction between three strategies. First:
Definition B.6. A 3-pre-interaction on A, B, C, D is w P |ppA ⊸ Bq ⊸ Cq ⊸ D|˚ s.t.
valid : @1 ď i ď n, tw1 , . . . , wi u P C ppA ⊸ Bq ⊸ Cq ,
where w “ w1 . . . wn .
For a 3-pre-interaction w, we define w æ A, B P |A ⊸ B|˚ , w æ B, C P |B ⊸ C|˚ ,
w æ C, D P |C ⊸ D|˚ and w æ A, D P |A ⊸ D|˚ with the obvious adaptation of Figure 68.
An interaction of σ, τ and δ is a 3-pre-interaction w s.t.
w æ A, B P σ ,

w æ B, C P τ ,

w æ C, D P δ ,

w æ A, D P Œ-PlayspA ⊸ Dq ,

written w P δ f τ f σ. We have four additional restrictions w æ A, B, C P τ f σ, w æ B, C, D P
δ f τ , w æ A, C, D P δ f pτ d σq and w æ A, B, D P pδ d τ q f σ, defined in the obvious way.
Then, the key argument of associativity is the so-called “zipping lemma”:
Lemma B.7 (Zipping). Consider u P δ fpτ dσq and v P τ fσ such that u æ A, C “ v æ A, C.
Then, there is a unique w P δ f τ f σ such that w æ A, C, D “ u and w æ A, B, C “ v.
Proof. By induction on u – by Lemma B.3 the moves in B from v can be interleaved with
those in v in a unique way; likewise there is a unique way to set their dependency.
We also have the mirror image, zipping u P pδ d τ q f σ with v P δ f τ . Altogether,
Proposition B.8. We have pδ d τ q d σ “ δ d pτ d σq.
Proof. Consider s P δ d pτ d σq. It has a (unique) witness u P δ f pτ d σq. Then,
u æ A, C P τ d σ, thus there is again v P τ f σ s.t. u æ A, C “ v æ A, C. By Lemma B.7, there
is w P δ f τ f σ s.t. w æ A, C, D “ u and w æ A, D, C “ v. But then we may restrict w to
w æ B, C, D P δ f τ , so w æ B, D P δ d τ . Moreover w æ A, B P σ so w æ A, B, D P pδ d τ q f σ,
from which w æ A, D P pδ d τ q d σ. The other direction is symmetric.
Note that associativity holds for prestrategies and does not depend on receptive.
B.1.4. Identities. Fix some ´-arena A. For s P Œ-PlayspA ⊸ Aq, we define its restrictions
εæl “ ε
s rpl, aqsa1 æ l “ ps æ lq a
s rpr, aqs æ r “ s æ r

εær “ ε
s rpl, aqsa1 æ r “ s æ r
s rpr, aqs æ r “ ps æ rq a

using which we may define the identity for alternating strategies:
Definition B.9. The copycat ccA : A ⊸ A comprises all s P Œ-PlayspA ⊸ Aq s.t.
(1) for all s1 Ď s of even length, s1 æ l “ s1 æ r,
(2) for all rpl, aqsa1 P |s|, with a P minpAq, a “ a1 .
Condition (2) means that when playing a minimal event on the left hand side, copycat
justifies it with the same move on the right. Such a condition is also required in Hyland-Ong
games (though sometimes mistakenly omitted). Copycat strategies provide identities:
Proposition B.10. The ´-arenas and alternating strategies form a category Œ-Strat.
Proof. It remains that for any σ : A ⊸ B, σ “ ccB d σ d ccA , which is elementary.

## PDF page 113

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

ε æ A1 , B1
s rpl, p1, aqqsp1,bq æ A1 , B1
s rpl, p2, aqqspi,bq æ A1 , B1
s rpr, p1, bqss æ A1 , B1
s rpr, p2, bqss æ A1 , B1

“
“
“
“
“

ε
ps æ A1 , B1 q rpl, aqsb
s æ A1 , B1
ps æ A1 , B1 q rpr, bqs
s æ A1 , B1

ε æ A2 , B2
s rpl, p1, aqqspi,bq æ A1 , B1
s rpl, p2, aqqsp2,bq æ A2 , B2
s rpr, p1, bqss æ A2 , B2
s rpr, p2, bqss æ A2 , B2

“
“
“
“
“

24:113

ε
s æ A2 , B2
ps æ A2 , B2 q rpl, aqsb
s æ A2 , B2
ps æ A2 , B2 q rpr, bqs

Figure 69: Partial restrictions for the tensor
B.2. Monoidal Closed Structure. We now describe the monoidal structure.
B.2.1. Tensor product. On ´-arenas, we have defined A b B simply as A ∥ B.
For strategies, the critical step is a suitable notion of restriction. More precisely, for
A1 , A2 , B1 , B2 ´-arenas and s P Œ-PlayspA1 b A2 ⊸ B1 b B2 q, we give a partial definition
s æ A1 , B1 P |A1 ⊸ B1 |˚

s æ A2 , B2 P |A2 ⊸ B2 |˚

in Figure 69 – partial, because e.g. rpl, p1, aqqsp2,bq æ A1 , B1 is left undefined. We then set:
Definition B.11. Consider σ1 : A1 ⊸ B1 and σ2 : A2 ⊸ B2 alternating strategies. Then:
σ1 b σ2 “ ts P Œ-PlayspA1 b A2 ⊸ B1 b B2 q | @i P t1, 2u, s æ Ai , Bi P σi u ,
implying in particular that for each s P σ1 b σ2 and i P t1, 2u, s æ Ai , Bi is defined.
By definition, σ1 b σ2 satisfies non-empty and prefix-closed. As for composition, determinism involves performing a state analysis expressing that at each point, only one of σ1 or
σ2 has control. We skip the details. See e.g. [Har04] for an analogous proof, also reflected
in the proof in Section 6.1.4 that sequential causal strategies are stable under tensor.
Proposition B.12. Consider σ1 : A1 ⊸ B1 and σ2 : A2 ⊸ B2 alternating strategies.
Then, σ1 b σ2 : A1 b A2 ⊸ B1 b B2 is an alternating strategy.
Fix σ1 : A1 ⊸ B1 , σ2 : A2 ⊸ B2 , τ1 : B1 ⊸ C1 and τ2 : B2 ⊸ C2 . For w P
pτ1 b τ2 q f pσ1 b σ2 q, we first define partially w æ A1 , B1 , C1 and w æ A2 , B2 , C2 analogously
to Figure 69 – it is direct to prove that w æ A1 , B1 , C1 P τ1 f σ1 and w æ A2 , B2 , C2 P τ2 f σ2 .
Functoriality is analogous to associativity in that it relies on a zipping lemma:
Lemma B.13. Consider u1 P τ1 f σ1 , u2 P τ2 f σ2 , and s P Œ-PlayspA1 b A2 ⊸ C1 b C2 q
such that s æ A1 , C1 “ u æ A1 , C1 and s æ A2 , C2 “ u æ A2 , C2 .
Then, there is a unique w P pτ1 b τ2 q f pσ1 b σ2 q such that
s “ w æ A1 b A2 , C1 b C2 ,

s æ A1 , B1 , C1 “ u1 ,

s æ A2 , B2 , C2 “ u2 .

Proposition B.14. The construction b extends to a bifunctor
b : Œ-Strat ˆ Œ-Strat Ñ Œ-Strat .
Proof. Preservation of identities is direct. Functoriality follows by Lemma B.13
Next, we complete the symmetric monoidal structure by providing the structural natural
isomorphisms. We first introduce a few tools useful in giving a clean definition of such
structural isomorphisms, which are variants of the copycat strategy. We shall make use of
certain morphisms, called renamings, to act on strategies.

## PDF page 114

24:114

S. Castellan and P. Clairambault

Vol. 20:3

Definition B.15. A renaming from arena A to B is a function f : |A| Ñ |B| satisfying:
@x P C pAq, f x P C pBq
@a1 , a2 P x P C pAq, f a1 “ f a2 ùñ a1 “ a2
@a P |A|, polB pf aq “ polA paq
@θ P S pAq(resp. S` pAq, S´ pAq), f θ P S pBq,
(resp. S` pBq, S´ pBq)
strong-receptivity: for all θ P S pAq, for all f θ Ď´ φ P S pBq,
D!θ Ď´ θ1 P S pAq f θ1 “ φ
courtesy: @a1 _A a2 , ppolA pa1 q “ ` _ polA pa2 q “ ´q ùñ f a1 _B f a2 .

validity:
local injectivity:
polarity-preserving:
symmetry-preserving:

We write f : A Ñ B to mean that f is a renaming from A to B.
This construction is imported from [CCW19]. Then we have:

Definition B.16. Consider σ : A ⊸ B and renamings g : B Ñ B 1 , f : AK Ñ A1 K . We set
g ¨ σ ¨ f “ tg ¨ s ¨ f | s P σu : A1 ⊸ B 1
where g ¨ s ¨ f acts on s event-wise, sending rpl, aqsb to rpl, f paqqsgpbq and rpr, bqs to rpr, gpbqqs.
It is direct that g ¨ σ ¨ f is a strategy. The structural isomorphisms that we aim to define
are obtained by lifting renamings. Indeed if f : A Ñ B is a renaming, we may define
Ñ
Ý
f “ f ¨ ccA : A ⊸ B .
Ð
Ý
a renaming from copycat. Likewise, from f : B K Ñ AK we set f “ ccB ¨ f : A ⊸ B.
The main property satisfied by these constructions is the following lifting lemma.
Lemma B.17. Consider σ : A ⊸ B a strategy, and f : AK Ñ A1 K , g : B Ñ B 1 two
Ð
Ý
Ñ
renamings. Then, we have Ý
g d σ d f “ g ¨ σ ¨ f.
Proof. A direct adaptation of the neutrality of copycat under composition.
Before we put these to use to construct the symmetric monoidal structure, we deduce
a few properties of lifted strategies. In the statement below, for any renaming f : A Ñ B
which is additionally an isomorphism, then we write f K : B K Ñ AK for its inverse with
polarities reversed – it is immediate that it still satisfies the conditions of a renaming.
Proposition B.18. Lifting is a functor from the category of renamings to Œ-Strat.
Ý
Ñ
Ñ
Ý
Ñ´1 ÝÝ´1
Ý
Ñ Ð
Ý
Moreover, if f : A Ñ B is an iso, f is an iso; and we have f
“f
and f “ f K .
Proof. By Lemma B.17 and direct verifications.
With this, we may now define the structural isomorphisms for the symmetric monoidal
structure. We notice that for all arenas A, B, C, there are invertible renamings:
ρA :
Ab1
λA :
1b1
αA,B,C : pA b Bq b C
sA,B :
AbB

Ñ
Ñ
Ñ
Ñ

A
A
A b pB b Cq
BbA

where 1 is the empty arena, satisfying the coherence laws of a symmetric monoidal category.
Ý
Ñ ÝÝÝÝÑ
The required structural isomorphisms are simply obtained by lifting those as Ý
ρÑ
A , λA , αA,B,C
Ñ
and Ý
sÝ
A,B . By Proposition B.18, the required coherence diagrams are still satisfied.
Proposition B.19. The category Œ-Strat is a symmetric monoidal category.

## PDF page 115

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:115

Proof. It remains to prove naturality, easy from Proposition B.18 and direct verifications.

B.2.2. Cartesian products. Œ-Strat has cartesian products, given by & on objects.
To perform the pairing of σ1 : A ⊸ B1 and σ2 : A ⊸ B2 , we first build prestrategies
inj1 pσ1 q : A ⊸ B1 & B2 ,

inj2 pσ2 q : A ⊸ B1 & B2

defined by applying event-wise inji prpr, bqsq “ rpr, pi, bqqs, inji prpl, aqsb q “ rpl, aqspi,bq . We
obtain xσ1 , σ2 y “ inj1 pσ1 q Z inj2 pσ2 q. It is direct that this yields a bijection:
x´, ´y : Œ-StratpA, B1 q ˆ Œ-StratpA, B2 q Ñ Œ-StratpA, B1 & B2 q
The projections are pπ1 , π2 q “ x´, ´y´1 pidB1 &B2 q, and we can verify
π1 d xσ1 , σ2 y “ σ1 ,

π2 d xσ1 , σ2 y “ σ2

which is enough to complete the cartesian structure of Œ-Strat.
B.2.3. Monoidal closure. First, for ´-arenas A, B and C, there is a clear isomorphism
pA b Bq ⊸ C

–

A ⊸ pB ⊸ Cq

which, applied event-wise, yields Λp´q : Œ-StratpA b B, Cq » Œ-StratpA, B ⊸ Cq. Then,
evA,B “ Λ´1 pidA⊸B q : pA ⊸ Bq b A ⊸ B
is the evaluation strategy. It is a verification akin to the neutrality of copycat that for all
σ : A ⊸ pB ⊸ Cq, we have evA,C d pσ b Bq “ Λ´1 pσq.
Proposition B.20. Œ-Strat is a cartesian symmetric monoidal closed category.

B.3. Symmetry. We now develop the structure pertaining to symmetry.
B.3.1. Basic structure. The extension of the construction above with symmetry and uniformity unfolds essentially as in AJM games [AJM00]. We describe the main steps.
First of all, we ensure all structural morphisms are uniform. This is the purpose of:
Ñ Ý
Ý
Ñ
Lemma B.21. For A and B ´-arenas and f : A Ñ B a renaming, f « f .
Proof. Straightforward by symmetry-preserving and strong-receptivity of renamings.
Next, we show operations on strategies are compatible with «. The delicate case is
composition. Fix A, B and C ´-arenas, and write I “ pA ⊸ Bq ⊸ C. We shall give to
events of pA ⊸ Bq ⊸ C a polarity corresponding to their role in an interaction: a move m
is negative if it is in A or C and is negative for A ⊸ C, and has polarity p otherwise.
The main tool is the following lifting of Definition 2.13 to interactions:
Definition B.22. Consider σ, σ 1 : A ⊸ B and τ , τ 1 : B ⊸ C. We write τ f σ « τ 1 f σ 1 iff
Ñ-simulation:
Ð-simulation:
Ñ-receptive:
Ð-receptive:

@ump P τ f σ, v P τ 1 f σ 1 , u –I v ùñ Dnp , vn P τ 1 f σ 1 & um –I vn
@u P τ f σ, vnp P τ 1 f σ 1 , u –I v ùñ Dm, um P τ f σ & um –I vn
@um´ P τ f σ, v P τ 1 f σ 1 , um´ –I vn´ ùñ vn´ P τ 1 f σ 1
@u P τ f σ, vn´ P τ 1 f σ 1 , um´ –I vn´ ùñ um´ P τ f σ

## PDF page 116

24:116

Vol. 20:3

S. Castellan and P. Clairambault

εæi
s rpl, pi, aqqspi,bq æ i
s rpl, pj, aqqspk,bq æ i
s rpr, pi, bqqs æ i
s rpr, pj, bqqs æ i

“
“
“
“
“

ε
ps æ iq rpl, aqsb
sæi
ps æ iq rpr, bqs
sæi

pi ‰ jq
pi ‰ jq

Figure 70: Partial restrictions for !
Lemma B.23. Consider σ, σ 1 : A ⊸ B and τ , τ 1 : B ⊸ C such that σ « σ 1 and τ « τ 1 .
Then, τ f σ « τ 1 f σ 1 .
Proof. Ñ-simulation. Consider ump P τ f σ and v P τ 1 f σ 1 , s.t. u –v v. Necessarily, m is
positive for σ or τ , w.l.o.g. say σ. Again, we distinguish cases whether m is in A or B. We
consider B, which is the most interesting case – so that m “ rpm, bqsc for some c P minpCq.
We project urpm, bqsc æ A, B “ pu æ A, Bqrpr, bqs` P σ, v æ A, B P σ 1 with u æ
A, B –A⊸B v æ A, B. By Ñ-simulation for σ, there is rpr, b1 qs s.t. pv æ A, Bqrpr, b1 qs P σ 1 and
pu æ A, Bqrpr, bqs –A⊸B pv æ A, Bqrpr, b1 qs .

(B.1)

1
However, we also have pu æ B, Cqrpl, bqs´
c P τ , v æ B, C P τ . We also have u æ
B, C –B⊸C v æ B, C. Necessarily, pr, cq P |u æ B, C| and there is a symmetric pr, c1 q P |v æ
B, C|. Then, from (B.1) and the definition of symmetry on A ⊸ B and B ⊸ C,

pu æ B, Cqrpl, bqsc –B⊸C pv æ B, Cqrpl, b1 qsc1
so by receptivity, pv æ B, Cqrpl, b1 qsc1 P τ 1 . It follows that vrpm, b1 qsc1 P τ 1 f σ 1 with
urpm, bqsc –I vrpm, b1 qsc1 as required. The condition Ð-simulation is symmetric.
Finally, Ñ-receptive and Ð-receptive are similar but simpler.
Finally, we may deduce compatibility of « with composition:
Corollary B.24. Consider σ, σ 1 : A ⊸ B and τ , τ 1 : B ⊸ C such that σ « σ 1 and τ « τ 1 .
Then, τ d σ « τ 1 d σ 1 .
Proof. Direct from Lemmas B.4 and B.23.
Lemma B.4 is crucial: this fails if we do not have a unique witness. This is the main
reason why this approach to uniformity does not extend to ö-Strat. Other operations on
strategies are easily seen to be compatible with «. Therefore, considering Œ-Strat as having
as only morphisms the uniform strategies (i.e. self-equivalent for «), it is equipped with an
additional equivalence relation « with respect to which all operations are compatible.
B.4. Seely category. We now provide the last ingredients to the Seely category.
First, we need a functor ! : Œ-Strat Ñ Œ-Strat. The construction is similar to the tensor
and defined by a suitable restriction, given in Figure 70. Armed with this, we set:
Definition B.25. Consider σ : A ⊸ B an alternating strategy. Then, we set:
!σ “ ts P Œ-Playsp!A ⊸ !B | @i P N, s æ i P σu ,
implying in particular that for each s P !σ and i P N, s æ i is defined.
This is really an infinitary tensor of σ. That this yields !σ : !A ⊸ !B an alternating
strategy, along with functoriality, are as for the tensor. We skip the details.

## PDF page 117

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:117

ηA :

AK Ñ p!AqK
a ÞÑ pi, aq

seeÑ
A,B

!A b !B Ñ !pA & Bq
p1, pi, aqq ÞÑ p2i, p1, aqq
p2, pi, bqq ÞÑ p2i ` 1, p2, aqq

µA :

p!!AqK Ñ p!AqK
pi, pj, aqq ÞÑ pxi, jy, aq

seeÐ
A,B

!pA & Bq Ñ !A b !B
pi, p1, aqq ÞÑ p1, pi, aqq
pi, p2, bqq ÞÑ p2, pi, bqq

Figure 71: Comonad renamings

Figure 72: Seely renamings

Proposition B.26. The construction ! extends to a functor ! : Œ-Strat Ñ Œ-Strat.
The Seely structure also includes structural morphisms, all defined through lifting. We
define renamings in Figures 71 and 72 (with x´, ´y : N ˆ N Ñ N any bijection), set
derA “ Ð
ηÝ
!A ⊸ A
A :
Ð
digA “ µÝ
:
!A ⊸ !!A
A
ÝÝÝÑ
ÝÑ
monA,B “ seeA,B : !A b !B ⊸ !pA & Bq
ÝÝÝÐ
ÝÑ
mon´1
A,B “ seeA,B : !pA & Bq ⊸ !A b !B ,
and all coherence and naturality properties follow from Lemma B.17 with direct verifications.
A number of those only hold up to «: for instance, monA,B and mon´1
A,B are inverses up to
0
«, but not up to equality. Finally, mon : 1 ⊸ !1 is the empty strategy. Altogether:
Proposition B.27. The category Œ-Strat is a Seely category.

Appendix C. Construction of Non-Alternating Strategies
Next, we construct the category ö-Strat of ´-arenas and non-alternating strategies.
C.1. Basic Categorical Structure. We first study composition and copycat. For composition, the development is essentially a simpler version of Œ-Strat as there is no determinism
requirement. On the other hand, copycat requires slightly more care.
C.1.1. Composition. Consider fixed A, B and C three ´-arenas, and σ : A ⊸ B, τ : B ⊸ C
non-alternating prestrategies. Re-using pre-interactions and restrictions from before, we set:
Definition C.1. An interaction u P τ f σ, is a pre-interaction u such that
u æ A, B P σ ,

u æ B, C P τ ,

and we automatically have u æ A, C P ö-PlayspA ⊸ Cq.
The composition of σ and τ is τ d σ “ tu æ A, C | u P τ f σu.
It is clear this yields a non-alternating prestrategy, which only requires non-empty and
prefix-closed. In composing non-alternating (pre)strategies, there is no analogue of Lemma
B.3: all players can move anytime. The unique witness property is lost: s P τ d σ if there is
a witness u P τ f σ such that s “ u æ A, C, but u is in general not unique30.
30Causal strategies in _-Strat, with their explicit branching information, recover a unique witness property.

## PDF page 118

24:118

S. Castellan and P. Clairambault

Vol. 20:3

That composition preserves strategies will follow from Propositions C.3 and C.5.
C.1.2. Associativity. Fix σ : A ⊸ B, τ : B ⊸ C and δ : C ⊸ D non-alternating
prestrategies. As above, an interaction of σ, τ and δ is a 3-pre-interaction w P |ppA ⊸
Bq ⊸ Cq ⊸ D|˚ such that
w æ A, B P σ ,

w æ B, C P τ ,

w æ C, D P δ ,

from which it follows automatically that w æ A, D P ö-PlayspA ⊸ Dq.
Again, associativity relies on a “zipping lemma”.
Lemma C.2 (Zipping). Consider u P δ fpτ dσq and v P τ fσ such that u æ A, C “ v æ A, C.
Then, there is w P δ f τ f σ such that w æ A, C, D “ u and w æ A, B, C “ v.
Again, w is not unique. The interactions u and v impose causal constraints on |w|, and
w may be chosen as any ternary interaction respecting those. As in the alternating case
there is a mirror lemma, and associativity follows as in Proposition B.8.
Proposition C.3. We have pδ d τ q d σ “ δ d pτ d σq.
Associativity works for prestrategies, i.e. it does not rely on receptive and courteous.
C.1.3. Copycat. Non-alternating strategies are intended to model asynchronous concurrency
– accordingly, the non-alternating copycat, still written ccA : A ⊸ A, is an asynchronous
forwarder. We first describe the configurations on A $ A reached by copycat: those are
x ∥ y for x, y P C pAq, such that y Ď x, where Ď is the “Scott order” [Win13] defined as
yĎx

ô

y Ě´ x X y Ď` x

with polarities taken on A. Whenever ccA receives a negative event, it forwards it to the
other side, but asynchronously: y may contain negative events not yet forwarded to x, and
x may contain positive events (i.e. negative for A $ A) not yet forwarded to y.
But copycat plays on A ⊸ A, not on A $ A. Remember from Section 2.1.3 that there is
χA,B : pA ⊸ Bq Ñ pA $ Bq
satisfying the axioms of a map of event structures. We may set:
Definition C.4. For A any ´-arena, we set ccA to comprise all s P ö-PlayspA ⊸ Aq s.t.:
balanced: for all 1 ď i ď n, writing χA,A |s1 . . . sn | “ x ∥ y, we have y Ď x,
well-linked: for all rpl, aqsa1 , we have a “ a1 ,
where s “ s1 . . . sn .
It is direct that copycat is receptive and courteous. In fact, it turns out that receptive
and courteous are exactly the required conditions for copycat to be neutral for composition:
Proposition C.5. Consider A and B two ´-arenas, and σ : A ⊸ B a prestrategy.
Then, σ is a strategy if and only if ccB d σ d ccA “ σ.
Sketch. If. It is direct that all non-alternating prestrategies ccB d σ d ccA are receptive and
courteous. Only if. Considering w P ccB f σ f ccA , using that σ is receptive and courteous,
w can be transformed by permuting into w1 with the same outer restriction, but where all
moves are immediately forwarded by copycat. It follows that the outer restriction is in
σ.

## PDF page 119

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:119

This was noticed in [GM08], and also holds for causal strategies [RW11]. We deduce:
Corollary C.6. The ´-arenas and non-alternating strategies form a category ö-Strat.
Proof. Follows from Propositions C.3 and C.5.
C.1.4. Further structure. As for Œ-Strat, we have – with the same constructions:
Proposition C.7. ö-Strat is a cartesian symmetric monoidal closed category.
We could easily adapt the developments of Section 6.1 to show that there is a subcategory of sequential non-alternating strategies, which maps functorially to Œ-Strat (without
uniformity). However, our attempts to endow ö-Strat with symmetry failed, because of
the lack of unique witness in compositions. It seems it could be done by using a different
approach to symmetry, namely Melliès’ group-theoretic formulation of uniformity [Mel03];
this is however left for future work. We conclude this section with:
Proposition 3.22. There is a symmetric monoidal closed category with products ö-Stratwb ,
with objects ´-arenas, and morphisms well-bracketed non-alternating strategies on A ⊸ B.
Proof. It remains to prove that copycat strategies are well-bracketed and that well-bracketing
is preserved by operations on strategies, which is a routine verification.

Appendix D. Thin Concurrent Games
In this section, we give some proof for thin concurrent games. Notably, we detail the proofs
for the characterisations of configurations of interaction and composition used in this paper:
they do not appear in [CCW19], as they were elaborated more recently.
D.1. Representable functions. We investigate the functions between domains of configurations representable as maps of event structures.
D.1.1. Representable functions between configurations. We will be interested in those functions between configurations arising from maps of event structures:
Definition D.1. For A, B es, a function f : C pAq Ñ C pBq is representable if there is a
(necessarily unique) map of event structure fˆ : A Ñ B s.t. for all x P C pAq, fˆpxq “ f pxq.
Proof. For uniqueness, if f1 , f2 : A Ñ B have the same image for configurations, we have
f1 paq

f1 praqA q´ÝĂ f1 prasA q ,

f2 paq

f2 praqA q´ÝĂ f2 prasA q ,

where raqA “ ta1 P |A| | a1 ăA au.
Since f1 praqA q “ f2 praqA q and f1 prasA q “ f2 prasA q this entails f1 paq “ f2 paq.
We shall use the following characterisation of representable functions:
Lemma D.2. For A, B es, a function f : C pAq Ñ C pBq is representable iff it:
preserves the empty set: f pHq “ H
preserves covering: for x, y P C pAq, if x ´Ă y, then f pxq ´Ă f pyq
preserves unions: for x, y P C pAq, if x Y y P C pAq then f px Y yq “ f pxq Y f pyq.

## PDF page 120

24:120

Vol. 20:3

S. Castellan and P. Clairambault

Proof. If. For any a P |A|, write raqA “ rasA ztau. It is always a configuration of A, and
raqA ´Ă rasA . Because f preserves covering, there is b P |B| such that
b

f praqA q´ÝĂ f prasA q ,
i.e. f prasA q “ f praqA q Y tbu, write b “ fˆpaq.
This defines a function on events. Next, we show that its direct image of configurations
agrees with f . We first claim that for all x, y P C pAq such that x ´Ă y and y “ x Y tau, we
have f pyq “ f pxq Y tfˆpaqu as well. To prove this, consider the diagram
raqA ´Ă x1 ´Ă . . . ´Ă xn´1 ´Ă x
´Ă

´Ă

´Ă

´Ă

rasA ´Ă y1 ´Ă . . . ´Ă yn´1 ´Ă y
where, for each 1 ď i ă n, yi “ xi Y tau. Because f preserves covering and unions, f
preserves covering squares, hence by straightforward induction, for all 1 ď i ă n,
fˆpaq

f pxi q´ÝĂ f pyi q ,
so f pyq “ f pxq Y tfˆpaqu as required.
Now, we can prove that for all x P C pAq, we have f pxq “ fˆpxq. Indeed, there is
a1

an

H´ÝĂ . . . ´ÝĂ x
a covering chain, which as f preserves the empty set and by the property just above, entails
fˆpa1 q

fˆpan q

H´ÝĂ . . . ´ÝĂ f pxq ,
as well, showing that f pxq “ fˆpxq as needed. From this point it is trivial that fˆ is a map of
es: preservation of configurations follows from f : C pAq Ñ C pBq, and local injectivity from
the preservation of covering. Only if. Immediate verification.
D.1.2. Representable functions with symmetry. We extend this construction with symmetry.
Definition D.3. Let A, B be ess. A function f : C pAq Ñ C pBq is representable if there
is a (necessarily unique) map of ess fˆ : A Ñ B such that for all x P C pAq, fˆpxq “ f pxq.
As above, we give a characterization of representable functions between configurations.
Lemma D.4. Let A, B be ess. Then, a function f : C pAq Ñ C pBq is representable iff it:
preserves the empty set:
preserves covering:
preserves unions:
preserves symmetry:

f pHq “ H
for x, y P C pAq, if x ´Ă y, then f pxq ´Ă f pyq
for x, y P C pAq, if x Y y P C pAq then f px Y yq “ f pxq Y f pyq.
there is a (necessarily unique) monotone fr : S pAq Ñ S pBq
such that dom ˝ fr “ f ˝ dom and cod ˝ fr “ f ˝ cod.

Proof. If. If f satisfies the first three axioms, it is representable without symmetry. By
Lemma D.2 there is a map of event structures fˆ : A Ñ B s.t. for all x P C pAq, fˆpxq “ f pxq.
Now, assuming that f preserves symmetry, we show that actually we must have
frpθq “ tpfˆpaq, fˆpa1 qq | pa, a1 q P θu ,

## PDF page 121

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:121

i.e. fˆpθq, for all θ P S pAq. Indeed, consider a covering chain for θ, i.e. a sequence in S pAq:
pa1 ,a11 q

pa2 ,a12 q

pan ,a1n q

H “ θ0 ´ÝĂ θ1 ´ÝĂ . . . ´ÝĂ θn “ θ .
We show by induction on 0 ď i ď n that frpθi q “ fˆpθi q. First, dom ˝ frpHq “ f pHq “ H,
so frpHq “ H “ fˆpHq. For 0 ď i ď n, by IH, frpθi q “ fˆpθi q. We then have:
dompfrpθi`1 qq “ f pdompθi`1 qq
“ f pdompθi q Y tai`1 uq
“ f pdompθi qq Y tfˆpai`1 qu ,
and the symmetric reasoning shows codpfrpθi`1 qq “ codpfrpθi qq Y tfˆpa1i`1 qu as well. But
finally, we also have frpθi q Ď frpθi`1 q since fr is monotone. So we must have
frpθi`1 q “ frpθi q Y tpfˆpai`1 q, fˆpa1 qqu
i`1

“ fˆpθi q Y tpfˆpai`1 q, fˆpa1i`1 qqu
“ fˆpθi`1 q ,
as required. Now this exactly means that for all θ P S pAq we have fˆpθq P S pBq, and thus
fˆ is a map of event structures with symmetry. Only if. Obvious.
D.2. Interaction and Composition. Fix σ : A $ B and τ : B $ C (pre)strategies.
D.2.1. Interaction. First, we characterise interaction in terms of its configurations.
We start by recalling that by Lemma 3.12 of [CCW19], there is a pullback
τ fσ
Πσ

Πτ

|

"

σ∥C

A∥τ

Bσ ∥C

"

}

A∥Bτ

A∥B∥C
in the category of event structures with symmetry, the interaction pullback. First, we have:
Lemma D.5. For any x P C pτ f σq, writing
Πσ x “ xσ ∥ xτC P C pσ ∥ Cq

τ
Πτ x “ x σ
A ∥ x P C pA ∥ τ q ,

then we have xσ P C pσq and xτ P C pτ q causally compatible.
Proof. First, xσ and xτ are matching. For causal compatibility, we consider
φxσ ,xτ

:

xσ ∥ xτC

Bσ ∥xτ
C

»

τ
xσ
A ∥ xB ∥ xC

´1
xσ
A ∥Bτ

»

τ
xσ
A ∥x

from Definition 4.6, with pm, nq Ÿ pm1 , n1 q iff m ăσ∥C m1 or n ăA∥τ n1 which we must prove
acyclic. Now, the function which to c P x associates pΠσ pcq, Πτ pcqq is a bijection
ψ : x » φxσ ,xτ ,
and we now claim that for all c, c1 P x, if ψpcq Ÿ ψpc1 q, then c ăτ fσ c1 . Indeed, say c “ pm, nq
and c1 “ pm1 , n1 q, with w.l.o.g. m ăσ∥C m1 . Of course then, m “ Πσ pcq and m1 “ Πτ pc1 q.

## PDF page 122

24:122

Vol. 20:3

S. Castellan and P. Clairambault

Now, we use that Πσ is a map of event structures, and those always locally reflect causality
(Lemma A.2). Therefore, we must have c ăτ fσ c1 as required.
Therefore a cycle for Ÿ in φxσ ,xτ would induce a cycle for ăτ fσ in x, contradiction.
Proposition 4.9. There is a pre-interaction τ f σ, unique up to iso, such that there are
p´ f ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ , xτ causally compatibleu » C pτ f σq
p´ f ´q : tpθτ , θσ q P S pτ q ˆ S pσq | θσ , θτ causally compatibleu » S pτ f σq
order-isomorphisms commuting with dom and cod, and satisfying
σ
τ
Bτ fσ pθτ f θσ q “ θA
∥ θB ∥ θC

for all θσ P S pσq and θτ P S pτ q causally compatible.
Proof. Existence. We must provide the two order-isomorphisms announced. Take xσ P C pσq
and xτ P C pτ q causally compatible. By Definition 4.6, the bijection
φxσ ,xτ

:

xσ ∥ xτC

Bσ ∥xτ
C

»

τ
xσ
A ∥ xB ∥ xC

´1
xσ
A ∥Bτ

»

τ
xσ
A ∥x

is secured, i.e. the relation pm, nq Ÿ pm1 , n1 q ô m ďσ∥C m1 _ n ďA∥τ n1 defined on the
graph of φxσ ,xτ is acyclic, so its reflexive transitive closure ďxσ ,xτ is a partial order. This
turns φxσ ,xτ into an event structure, and in fact an ess with identity symmetries. Moreover,
there are obvious maps of ess
πσ : φxσ ,xτ Ñ σ ∥ C

πτ : φxσ ,xτ Ñ A ∥ τ

commuting with display maps, so by the universal property, xπσ , πτ y : φxσ ,xτ Ñ τ f σ and
xτ f xσ “ xπσ , πτ yp|φxσ ,xτ |q P C pτ f σq
concludes the definition of the action of p´ f ´q on causally compatible pairs. Reciprocally,
if x P C pτ f σq then its projections yield Πσ pxq “ xσ ∥ xτC and Πτ pxq “ xτA ∥ xτ , and by
Lemma D.5, xσ and xτ are causally compatible. Finally, for xσ and xτ causally compatible,
Πσ pxτ f xσ q “ xσ ∥ xτC

τ
Πτ pxτ f xσ q “ xσ
A ∥x

by construction and if x P C pτ f σq, x “ xτ f xσ by universal property of the pullback.
The projections are monotone, and the monotonicity of p´ f ´q follows from the universal
property. For symmetries, causal compatibility of θσ P S pσq and θτ P S pτ q amounts to
»

xτ f xσ

Πτ

»

τ
y σ ∥ yC

τ
xσ
A ∥x

–

τ
θσ ∥θC

Π´1
σ

–

xσ ∥ xτC

»

Πσ

yτ f yσ

»

Πτ

σ ∥θ τ
θA

σ ∥ yτ
yA

commuting, inducing θf : xτ f xσ » y τ f y σ . But symmetries on τ f σ are precisely
those bijections xτ f xσ » y τ f y σ projecting to S pS ∥ Cq and S pA ∥ T q as above, so
θf P S pτ f σq. Reciprocally, θf P S pτ f σq induces θσ P S pσq and θτ P S pτ q by
projections. That this yields an order-iso compatible with dom and cod is direct.
Uniqueness. Two event structures with symmetry satisfying the hypotheses obviously
have isomorphic domains of configurations (and isomorphic domains of symmetries, in
a compatible manner). But such order-isomorphisms between domains of configurations
and symmetries are automatically representable in the sense of Definition D.3. Therefore,
by Lemma D.4 the isomorphisms are generated by isomorphisms of event structures with

## PDF page 123

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:123

symmetry, as required. Preservation of display maps holds for configurations by hypothesis;
and by uniqueness in Lemma D.4, two maps of ess with the same action on configurations must
be equal. Therefore, the isomorphism commutes with display maps and is an isomorphism
of pre-interactions as required.

D.2.2. Composition. We aim to prove Propositions 4.11 and 4.13, exploiting Proposition
4.9, along with a few extra lemmas. First, we notice a connection between minimality of
causally compatible pairs and that maximal events of interactions are visible.
Lemma D.6. For xσ P C pσq and xτ P C pτ q causally compatible, they are minimal causally
compatible iff the maximal events of xτ f xσ are visible, e.g. occur in A or C.
Proof. If. Consider y σ P C pσq and y τ P C pτ q causally compatible such that y σ Ď xσ , y τ Ď
σ
τ
τ
xτ , while xσ
A “ yA and xC “ yC . Assume, seeking a contradiction, that we have yB Ă xB a
strict inclusion. Necessarily, we have y τ f y σ Ă xτ f xσ . Take m P py τ f y σ qzpxτ f xσ q,
w.l.o.g. we can assume that m is maximal for ďτ fσ in xτ f xσ . By hypothesis, m occurs in
σ
τ
τ
A or C. But this immediately contradicts the hypothesis that xσ
A “ yA and xC “ yC .
σ
τ
τ
σ
Only if. Assume x , x are minimal causally compatible, and take m P x f x maximal.
Seeking a contradiction, assume that m occurs in B. So, projecting
Πσ pxτ f xσ q “ xσ ∥ xτC ,

τ
Πτ pxτ f xσ q “ xσ
A ∥x ,

we have Πσ m “ p1, sq with s P xσ and Πτ m “ p2, tq with t P xτ . As maps of event structures
locally reflect causality (Lemma A.2), s is maximal in xσ and t is maximal in xτ . Hence,
y σ “ xσ ztsu P C pσq and y τ “ xτ zttu P C pτ q. By construction they are causally compatible
with the same projections to A and C, contradicting minimality of xσ and xτ .
We write C v pτ f σq for the configurations whose maximal events are visible and likewise
for symmetries. Then, the lemma above means that we can refine Proposition 4.9 to:
Proposition D.7. The order-isomorphisms of Proposition 4.9 restrict to
p´ f ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ and xτ minimal caus. comp.u » C v pτ f σq
p´ f ´q : tpθτ , θσ q P S pτ q ˆ S pσq | θσ and θτ minimal caus. comp.u » S v pτ f σq
Now, it remains to link configurations of τ d σ with configurations of τ f σ with
visible maximal events, and likewise for symmetries. First, we fix a few notations. Any
configuration x P C pτ f σq yields a configuration of the composition, its hiding, defined
as xÓ “ x X |τ d σ| P C pτ d σq. Reciprocally, if x P C pτ d σq is a configuration of the
composition, its witness is defined as
rxsτ fσ “ tm P |τ f σ| | Dn P x, m ďτ fσ nu P C pτ f σq .
The next point we make, is that interactions with visible maximal events are exactly
those arising as witnesses of configurations of the composition. More precisely, we have:
Lemma D.8. There are order-isomorphisms compatible with dom, cod and display maps:
p´qÓ : C v pτ f σq » C pτ d σq : r´sτ fσ
p´qÓ : S v pτ f σq » S pτ d σq : r´sτ fσ

## PDF page 124

24:124

S. Castellan and P. Clairambault

Vol. 20:3

Proof. For configurations, to x P C v pτ fσq we associate its hiding xÓP C pτ dσq. Reciprocally,
to x P C pτ d σq, we associate its witness rxsτ fσ P C v pτ f σq. Those operations preserve
inclusion, and it is an elementary verification that they are inverses.
For symmetries, any θ : x –τ fσ y must preserve visible events, so it induces by hiding
θÓ: xÓ–τ dσ yÓ
a symmetry on the composition; and hiding preserves inclusion. Reciprocally, if θ : x –τ dσ y
then by definition there is θ Ď θ1 : x1 –τ fσ y 1 . Necessarily, rxsτ fσ Ď x1 and rysτ fσ Ď y 1 .
Since θ1 is an order-iso, by restriction we may assume w.l.o.g. θ1 : rxsτ fσ –τ fσ rysτ fσ .
But the witness θ1 is unique: by Lemma 3.33 of [CCW19], if θ2 : rxsτ fσ –τ fσ rysτ fσ
is such that θ2 Ó“ θ1 Ó“ θ, then θ1 “ θ2 . So to θ : x –τ dσ y we associate this unique
θ1 : rxsτ fσ –τ fσ rysτ fσ . Monotonicity and that these operations are inverses also follow
immediately from uniqueness of the witness symmetry, i.e. Lemma 3.33 of [CCW19].
Composing the order-isomorphisms of Proposition D.7 and Lemma D.8, we get:
Proposition 4.11. Consider σ : A $ B, and τ : B $ C causal strategies.
There is a causal strategy τ d σ, unique up to iso, s.t. there are order-isos:
p´ d ´q : tpxτ , xσ q P C pτ q ˆ C pσq | xσ , xτ minimal caus. comp.u » C pτ d σq
p´ d ´q : tpθτ , θσ q P S pτ q ˆ S pσq | θσ , θτ minimal caus. comp.u » S pτ d σq
commuting with dom and cod; s.t., for θσ P S pσq, θτ P S pτ q minimal causally compatible,
σ
τ
Bτ dσ pθτ d θσ q “ θA
∥ θC
.

Proof. Existence. Direct by Proposition D.7 and Lemma D.8.
Uniqueness. As in the proof of Proposition 4.9.
This means that any configuration x P C pτ d σq may be written uniquely as xτ d xσ for

xσ P C pσq and xτ P C pτ q minimal causally compatible – note that from the construction of
the order-isomorphism in the proposition above, we then have xτ f xσ “ rxτ d xσ sτ fσ .

D.2.3. `-covered case. Finally, it remains to prove Proposition 4.13.
In essence, Proposition 4.13 is a specialization of Proposition 4.11 to strategies. Consider
therefore from now on that σ : A $ B and τ : B $ C are strategies. First of all, we show
that for `-covered configurations we can omit the minimality assumption.
Lemma D.9. Consider xσ P C ` pσq and xτ P C ` pτ q causally compatible `-covered.
Then, xσ and xτ are minimal causally compatible.
Proof. Seeking a contradiction, assume y σ and y τ are causally compatible such that y τ fy σ Ă
σ
τ
τ
τ
σ
τ
xτ fxσ with xσ
A “ yA and xC “ yC . Without loss of generality, consider m P px fx qzpy f
σ
y q maximal for ďτ fσ . By hypothesis, m occurs in B. Therefore, projecting
Πσ pmq “ p1, sq

Πτ pmq “ p2, tq ,

maximality of m in xτ fxσ entails via Lemma A.2 that s is maximal in xσ and t maximal in xτ .
But necessarily, s and t has dual polarities: w.l.o.g. say that polσ psq “ ` and polτ ptq “ ´.
So, t is negative maximal in xτ , contradicting that xτ P C ` pτ q is `-covered.
So in a synchronization between `-covered configurations, the maximal events are visible
as if they are synchronized, they will be both maximal and negative for one of the two
players. Resulting configurations of the composition are automatically `-covered:

## PDF page 125

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:125

Lemma D.10. For xσ P C ` pσq, xτ P C ` pτ q causally compatible, xτ d xσ P C ` pτ d σq.
Proof. Consider m P xτ d xσ maximal. This means that m is also maximal in xτ f xσ “
rxτ f xσ sτ fσ . Necessarily, m occurs in A or C, w.l.o.g. assume it occurs in C. Then, Πτ pmq
has the form p2, tq where using Lemma A.2, necessarily t is maximal (for ďτ ) in xτ . But
then, since xτ is `-covered, t is positive – hence, m is positive as well.
So causally compatible `-covered xσ P C ` pσq and xτ P C ` pτ q are minimal, and their
composition yields xτ d xσ P C ` pτ d σq `-covered. We prove the converse:
Lemma D.11. Consider xσ P C pσq and xτ P C pτ q minimal causally compatible.
If xτ d xσ P C ` pτ d σq is `-covered, so are xσ P C ` pσq and xτ P C ` pτ q.
Proof. Consider s P xσ maximal. Necessarily, there is a unique m P xτ f xσ such that
Πσ pmq “ p1, sq. Assume first that m is maximal in xτ f xσ . As xτ f xσ “ rxτ d xσ sτ fσ ,
if m is maximal it must be visible and maximal in xτ d xσ . Therefore, it is positive by
hypothesis, and s is positive.
Otherwise, assume m is not maximal, so there is some m _τ fσ n. By Lemma 4.22,
Πσ pmq _σ∥C Πσ pnq

or

Πτ pmq _A∥τ Πτ pnq .

If this is the former, then there is s _σ s1 with s1 P xσ , absurd by maximality of
s. If this is the latter, then two cases arise. If m occurs in A, then Πτ pmq “ p1, aq and
Πτ pnq “ p1, a1 q with a _A a1 . Likewise, Πσ pmq “ p1, sq and Πσ pnq “ p1, s1 q. But then by
Lemma A.2, we must have s ăσ s1 contradicting again the maximality of s. Finally, if m
occurs in B, then Πτ pmq “ p2, tq and Πτ pnq “ p2, t1 q with t _τ t1 . We split cases one last
time, depending on the polarity of t in τ . If t is negative, then s is positive in σ as required.
Otherwise, by courtesy of τ we must have Bτ ptq _B$C Bτ pt1 q. In particular, t1 must also
occur in B and we must have Πσ pnq “ p1, s1 q for s1 P xσ , with moreover Bσ psq _A$B Bσ ps1 q.
Therefore, again by Lemma A.2, we must have s ăσ s1 contradicting the maximality of s.
The symmetric reasoning shows that any t P xτ maximal in xτ is positive.
We are almost in position to prove Proposition 4.13 – the only missing piece is uniqueness:
Lemma 4.12. Consider σ, τ : A two causal strategies. Assume there are
ψ : C ` pσq » C ` pτ q

ψ : S ` pσq » S ` pτ q

order-isomorphisms compatible with dom, cod, and display maps.
Then, σ and τ are isomorphic.
Proof. We extend ψ to all configurations and all symmetries, and conclude via Lemma D.4.
Let x P C pσq. Consider x` P C pσq minimal such that x` Ď´ x. Necessarily, x` P
`
C pσq, so we may take ψpx` q P C ` pτ q. Now, since ψ is compatible with display maps,
Bτ pψpx` qq Ď´ Bσ pxq ,
therefore by receptivity and courtesy (see Lemma 3.13 from [CCRW17]), there is a unique
y P C pτ q such that ψpx` q Ď´ y and Bτ pyq “ Bσ pxq; we set ψpxq “ y.
We must show this extended ψ preserves inclusion; we show it preserves covering, and
distinguish the positive and negative cases. First, consider configurations in C pσq:
s`

x´ÝĂ y ,

## PDF page 126

24:126

Vol. 20:3

S. Castellan and P. Clairambault

s`

which means x` Ď´ z ´ÝĂ y ` . Now, by hypothesis ψpx` q Ď ψpy ` q, so ψpx` q Ď ψpyq.
Moreover, this inclusion must contain exactly one positive event, write it t` P ψpyqzψpx` q –
necessarily, Bτ ptq “ Bσ psq. Now, notice Bτ ptq is maximal in Bτ pψpyqq: indeed,
Bσ psq

Bτ pψpxqq “ Bσ pxq´ÝĂ Bσ pyq “ Bτ pψpyqq
by hypothesis. So, by courtesy, t is maximal in ψpyq as well. So, we have z “ ψpyqzttu P C pτ q.
Moreover, Bτ pzq “ Bτ pψpyqqztBτ ptqu “ Bσ pxq. So, ψpx` q Ď´ z with Bτ pzq “ Bσ pxq, therefore
z “ ψpxq; and ψpxq ´Ă ψpyq as required. Considering now a negative extension, i.e.
s´

x´ÝĂ y ,
it follows that x` “ y ` and ψpxq ´Ă ψpyq is immediate by receptivity. Altogether we have
ψ : C pσq Ñ C pτ q
compatible with display maps and preserving inclusion. Likewise we construct ψ ´1 : C pτ q Ñ
C pσq preserving inclusion from its action on `-covered configurations. That they are inverses
is immediate from ψ being a bijection between `-covered configurations, and receptivity.
Now, we consider the action of ψ on symmetries. If θ P S pσq, consider θ` P C pσq
minimal s.t. θ` Ď´ θ – recall that as a symmetry, θ is an order-iso preserving polarities,
so this is well-defined. Now, θ` P S ` pσq, so that we may take ψpθ` q P S ` pτ q as for
configurations. Again, since ψ is compatible with display maps, we have
Bτ pψpθ` qq Ď´ Bσ pθq .
By receptivity and courtesy of τ , there are unique extensions of dompψpθ` qq and
codpψpθ` qq to ψpdompθqq and ψpcodpθqq, projecting via Bτ to dompBσ pθqq and codpBσ pθqq
respectively. We get ψpθ` q Ď´ Ω P S pτ q by iterating „-receptivity for τ , such that
Bτ pΩq “ Bσ pθq – which characterises Ω as the composition
Bτ

Bσ pθq

Bτ

ψpdompθqq » dompBσ pθqq –A codpBσ pθqq » ψpcodpθqq ,
so a unique extension of ψpθ` q projecting to Bσ pθq – we fix ψpθq “ Ω. Monotonicity is
immediate from compatibility with dom and cod and that ψ preserves covering ´Ă on
configurations. Likewise we extend ψ ´1 to all symmetries; that ψ and ψ ´1 are inverses
follows as they preserve covering and are inverses on configurations.
We may now conclude our final characterization of composition:
Proposition 4.13. Consider σ : A $ B and τ : B $ C causal strategies.
Then, there is a strategy τ d σ : A $ C, unique up to iso, such that there are order-isos:
p´ d ´q : tpxτ , xσ q P C ` pτ q ˆ C ` pσq | xσ and xτ caus. comp.u » C ` pτ d σq
p´ d ´q : tpθτ , θσ q P S ` pτ q ˆ S ` pσq | θσ and θτ caus. comp.u » S ` pτ d σq
commuting with dom and cod, and s.t., for θσ P S ` pσq and θτ P S ` pτ q causally compatible,
σ
τ
Bτ dσ pθτ d θσ q “ θA
∥ θC
.

Proof. Existence. Simply a restriction of the isomorphisms of Proposition 4.11. By Lemma
D.9, causally compatible xσ P C ` pσq and xτ P C ` pτ q are automatically minimal, and by
Lemma D.10, xτ d xσ P C ` pτ d σq is `-covered. Reciprocally, if xτ d xσ P C ` pτ d σq is
`-covered, then by Lemma D.11, so are xσ P C ` pσq and xτ P C ` pτ q. Since the isomorphism

## PDF page 127

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:127

p´ d ´q is compatible with dom and cod and symmetries are order-isomorphisms, there
observations apply to symmetries. Uniqueness. By Lemma 4.12.

D.3. Charactering immediate causality.
Lemma 4.21. For σ : A $ B, τ : B $ C causal prestrategies, for m, m1 P |τ f σ|, if
m _τ fσ m1 , then mσ _σ m1σ , or mτ _τ m1τ , where mσ , mτ are defined whenever used.

Proof. If m _τ fσ m1 , then x “ rmsτ fσ ztm, m1 u P C pτ f σq. Then we have
x

“

xτ f xσ

m

yτ f yσ

´ÝĂ

m1

zτ f zσ

´ÝĂ

“

rmsτ fσ

in C pτ f σq, inlining the order-isomorphism of Proposition 4.8. Let us focus first on
m

xτ f xσ

yτ f yσ .

´ÝĂ

Since p´ f ´q is an order-iso, this yields a covering in the partial order of causally
compatible pairs, ordered by pairwise inclusion. By compatibility with display maps these
inclusions add exactly one event in A, in B, or in C. This yields three cases: (a) m occurs in
A, xτ “ y τ , and xσ ´Ă y σ adds one event s P |σ|; (b) m occurs in C, xσ “ y σ and xτ ´Ă y τ
adds one event t P |τ |; or (c) m occurs in B, xσ ´Ă y σ adds one event s and xτ ´Ă y τ adds
one event t with Bσ psq “ p2, bq and Bτ ptq “ p1, bq.
Now, back to considering m and m1 . If both occur in C, then we have
xτ f xσ

m

m1

y τ f xσ

´ÝĂ

´ÝĂ

z τ f xσ ,

t1

t

with xτ ´ÝĂ y τ ´ÝĂ z τ . If t ăτ t1 , then t _τ t1 and we are done. Otherwise, we also have
t1

t

xτ ´ÝĂ uτ ´ÝĂ z τ ,
and as t1 occurs in C we also have xσ and uτ causally compatible. Therefore
xτ f xσ

n1

uτ f xσ

´ÝĂ

n

´ÝĂ

z τ f xσ

for some n, n1 P |τ f σ| since ´ f ´ is an order-isomorphism, so tn, n1 u “ tm, m1 u. But
since uτ f xσ ‰ y τ f xσ we must have n “ m and n1 “ m1 , contradicting m ăτ fσ m1 .
The case where m and m1 both occur in A is symmetric. If m occurs in A and m1 in C,
xτ f xσ
s

m

xτ f z σ

´ÝĂ

m1

´ÝĂ

zτ f zσ

t

with xσ ´ÝĂ z σ and xτ ´ÝĂ z τ . But then xσ and z τ are also causally compatible, and
xτ f xσ

z τ f xσ

´Ă

´Ă

zτ f zσ

which as above contradicts m ăτ fσ m1 . The case where m occurs in C and m1 occurs in A
is symmetric. Now, assume m occurs in A and m1 occurs in B. Then we have
xτ f xσ
s

m

xτ f y σ

´ÝĂ

t1

m1

´ÝĂ

zτ f zσ

s1

where xσ ´ÝĂ y σ , xτ ´ÝĂ z τ , and y σ ´ÝĂ z σ . If s ăσ s1 , then s _σ s1 and we are done.
Otherwise, we also have xσ ´Ă uσ ´Ă z σ , uσ and z τ are also causally compatible, and
xτ f xσ

´Ă

z τ f uσ

´Ă

zτ f zσ ,

## PDF page 128

24:128

Vol. 20:3

S. Castellan and P. Clairambault

contradiction. All cases with one event occurring in B and the other in A or C are symmetric.
Finally, assume both m and m1 occur in B. In that case, we have
s1

s

xσ ´ÝĂ y σ ´ÝĂ z σ ,

and

t1

t

xτ ´ÝĂ y τ ´ÝĂ z τ .

If we have s ăσ s1 then s _σ s1 and we are done, and likewise for t _τ t1 . Otherwise,
xσ ´Ă uσ ´Ă z σ and xτ ´Ă uτ ´Ă z τ , and xτ fxσ ´Ă uτ fuσ ´Ă z τ fz σ , contradiction.
Lemma D.12. Consider m, m1 P |τ f σ| such that m _τ fσ m1 .
Then, if mσ ăσ m1σ we have mσ _σ m1σ , and likewise for τ .

Proof. If m _τ fσ m1 , then there is xτ f xσ , y τ f y σ and z τ f z σ in C pτ f σq such that
xτ f xσ

m

´ÝĂ

yτ f yσ
mσ

m1

´ÝĂ

zτ f zσ ,

m1σ

but if mσ and m1σ are defined then xσ ´ÝĂ y σ ´ÝĂ z σ . If mσ ăσ m1σ , mσ _σ m1σ .
D.4. The Bang Lemma. Now, we prove the bang lemma from AJM games [AJM00]. Fix
A and B two concrete arenas with B pointed, and σ : !A $ !B a causal strategy.
By receptive, for each i P N, there is a unique qi P minpσq such that Bσ pqi q “ p2, pi, bqq
the unique minimal move of B of copy index i. Let us write
|σ i | “ tm P |σ| | qi ďσ mu
for the set of events of σ above qi . Since σ is pointed, it follows that for i, j P N distinct, |σ i |
and |σ j | are disjoint. Likewise, since arenas are concrete, moves in immediate conflict have
the same predecessor – it follows that if m P |σ i | and n P |σ j |, the negative dependencies
of m and n are compatible, hence m and n are compatible by determinism. Therefore, we
have σ –∥iPN σ i where σ i has a structure of ess directly imported from σ. Furthermore,
σ i : !A $ B with the display map Bσi defined in the obvious way. The key argument is:
Lemma D.13. For any i, j P N, we have σ i « σ j .
Proof. We exploit Lemma D.2 and build a (necessarily representable) iso between the
domains of configurations, compatible with symmetry. Consider xi P C pσ i q, with
Bσ pxi q “ xA ∥ tiu ˆ xB .
From Definition 7.19, xA ∥ tiu ˆ xB –´
!A$!B xA ∥ tju ˆ xB with the obvious symmetry
´
θi,j . We must transport xi along this negative symmetry θi,j . By Lemma B.4 from [CCW19],
´
there are unique xj P C pσq and ψ : xi –σ xj s.t. Bσ ψ “ θ` ˝ θi,j
for some
θ` : xA ∥ tju ˆ xB –`
!A∥!B yA ∥ tju ˆ yB
where we know that j is unchanged, because of condition `-transparent of Definition 7.19.
Therefore, xj P C pσ j q as required. Monotonicity of this operation and the fact that it is
a bijection between configurations follow from the uniqueness clause for Lemma B.4 of
[CCW19]; compatibility with symmetry follows from composition with the symmetry ψ.
This induces an isomorphism of ess φ : σ i « σ j which we must still check is a positive
isomorphism. But for xi P C pσ i q, the symmetry θ` above entails
Bσi pxi q “ xA ∥ xB

φ`
`
–!A$B

yA ∥ yB “ Bσj pxj q

ensuring that the triangle commutes up to positive symmetry as required.

## PDF page 129

Vol. 20:3

DISENTANGLING PARALLELISM AND INTERFERENCE IN GAME SEMANTICS

24:129

Next we lift a positive isomorphism on one copy index to the whole strategy:
Lemma D.14. Consider A and B concrete ´-arenas with B pointed, and σ, τ : !A $ !B.
If σ 0 « τ 0 , then σ « τ .
Proof. By Lemma D.13, for i P N, σ i « σ 0 « τ 0 « τ i , we conclude by parallel composition.
We may finally deduce the bang lemma:
Lemma 7.37. For concrete arenas A, B with B pointed and σ P _-Stratp!A, !Bq,
pderB d σq: « σ .

Proof. By Proposition 4.13 and a reasoning analogous to Proposition 4.20, we have derB dσ «
σ 0 . Therefore, by Lemma D.14, for any two σ, τ : !A $ !B, if derB d σ « derB d τ , then
σ « τ . The lemma follows directly from that and the Seely category laws.

D.5. Expansion of Meager Strategies. Consider σ : A parallel innocent. We first observe
that any move m P |σ| is determined by mfpmq, along with the copy index of its negative
dependencies. An exponential slice for y P C pmfpσqq normal is an assignment of copy
indices for all negative questions of y – or more precisely,
α : y Q,´ Ñ N ,
with y Q,´ the negative questions of y. To any x P C pσq we have associated mfpxq P C pmfpσqq.
To complete mfpxq, we also associate to x an exponential slice for mfpxq:
slicepxq : pmfpxqqQ,´ Ñ N
n´ ÞÑ indpBσ pθx´1 pnqqq .
We now show how to reconstruct events of σ from mfpσq and an exponential slice.
Lemma D.15. Consider A a concrete arena, σ : A a causal strategy, and y P C pmfpσqq.
For any α : y Q,´ Ñ N, there is a unique x P C pσq such that y “ mfpxq, α “ slicepxq,
and x –σ y. Moreover, the symmetry φy : y –σ x is unique.
Proof. Same proof as for Lemma 7.24, setting up indices following α instead of 0.
Just as Lemma 7.24, for σ : A parallel innocent, Lemma D.15 can be used to assemble
an event m P |mfpσq| and an exponential slice α : rmsQ,´ Ñ N into n P |σ| s.t. mfpnq “ m
and sliceprnsσ q “ α. So together, Lemmas 7.24 and D.15 establish a bijection between |σ|
and pairs pm, αq of m P |mfpσq| and an exponential slice α : rmsQ,´
Ñ N. From this it
σ
seems clear how to reconstruct σ from mfpσq: first, we reconstruct a partial order.
Proposition D.16. For A a concrete arena and σ : A` , we define a partial order exppσq:
| exppσq| “ tpm, αq | m P |σ| ^ α : rmsQ,´
Ñ Nu
σ
pm1 , α1 q ďexppσq pm2 , α2 q ô m1 ďσ m2 ^ @n´ ďσ m1 , α1 pnq “ α2 pnq .
Then, for any σ : A, σ and exppmfpσqq are isomorphic partial orders.
Proof. Direct consequence of Lemmas 7.24 and D.15.

## PDF page 130

24:130

S. Castellan and P. Clairambault

Vol. 20:3

It remains to complete exppσq into a causal strategy. The display map is determined by
a choice of copy index for positive questions. Hence, for any mQ,` P |σ|, assume fixed some
Q,´

fm : Nrmsσ

ÑN

specifying, for each Player question, its copy index depending on indices of Opponent
questions in its causal dependency. For simplicity, we assume this choice is globally injective,
i.e. fm , fn have disjoint codomains for distinct m, n P |σ|. The resulting strategy will not
depend on the choice of the family pfm qmP|σ|Q,` up to positive isomorphism.
Proposition D.17. Consider A a concrete arena, σ : A` parallel innocent causally wellbracketed. We define a display map Bexppσq for exppσq by induction, with image
Bexppσq pmA , αq “ a ,
Bexppσq pmQ,´ , αq “ q s.t. indpqq “ αpmq ,
Bexppσq pmQ,` , αq “ q s.t. indpqq “ fm pαq ,
where a, q is the unique event of A with label lblpmq, predecessor Bexppσq pjpm, αqq with jpm, αq
defined as jpmq with slice the restriction of α, label lblpmq; satisfying the additional constraint
given. Further components are:
pm, αq #exppσq pn, βq ô m #σ n, and α and β coincide on their common domain
θ P S pexppσqq ô θ : x – y order-iso s.t. π1 “ π1 ˝ θ.
Then, exppσq : A is parallel innocent causally well-bracketed.
The only difficulty is in handling conflict. A positive iso φ : σ 1 « σ 2 directly lifts to
exppσ 1 q « exppσ 2 q, applying φ to moves while keeping copy indices unchanged. Finally:
Corollary D.18. For A a concrete arena, the operations mfp´q and expp´q yield a bijection
between (positive isomorphism classes of ) causally well-bracketed strategies on A and A` .
Proof. For σ : A` , mfpexppσqq « σ by construction. For σ : A, exppmfpσqq « σ is obtained
from the iso of Proposition D.16 and a verification that this preserves further structure.

This work is licensed under the Creative Commons Attribution License. To view a copy of this
license, visit https://creativecommons.org/licenses/by/4.0/ or send a letter to Creative
Commons, 171 Second St, Suite 300, San Francisco, CA 94105, USA, or Eisenacher Strasse 2,
10777 Berlin, Germany
