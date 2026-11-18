Source: https://doi.org/10.22152/programming-journal.org/2021/5/12
PDF sha256: bf0d9b0abfd80197d627f869aade64edb671e9ccb9d6c7b5c53bc01c3400483c
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of cheung_ghica_muroya_2021_transparent_synchronous_dataflow.pdf

Transcription of `cheung_ghica_muroya_2021_transparent_synchronous_dataflow.pdf` in this directory, 55 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-55 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Transparent Synchronous Dataflow
Steven W.T. Cheunga , Dan R. Ghicaa , and Koko Muroyaa,b
a University of Birmingham
b RIMS, Kyoto University
Abstract Dataflow programming is a popular and convenient programming paradigm in systems modelling,
optimisation, and machine learning. It has a number of advantages, for instance the lacks of control flow
allows computation to be carried out in parallel as well as in distributed machines. More recently the idea of
dataflow graphs has also been brought into the design of various deep learning frameworks. They facilitate an
easy and efficient implementation of automatic differentiation, which is the heart of modern deep learning
paradigm.
Many dataflow languages are ‘modal’ in the sense that the dataflow graph is ‘constructed’ in an ambient
environment then ‘executed’ using special commands. Simulink, earlier Tensorflow, Lucid Synchrone (LS)
or Self-adjusting computation (SAC) are examples of such languages. We are interested in modal dataflow
languages in which the ambient environment is a fully fledged functional and imperative language. Such
ambient languages make creating complex and large models easier, but they raise questions of language
design, safety and efficiency.
LS provides a way to define dataflow graphs through co-recursive equations of streams. In these cases
the interesting issue is efficiency, particularly of memory utilisation. A semantically interesting question
occurs in the case of languages which allow the explicit manipulation of the dataflow graph using imperative
constructs. This is the case of early Tensorflow and imperative SAC. However the meta-programming style of
TensorFlow in which special commands are used to construct imperatively a dataflow graph was considered
awkward and error prone, and TensorFlow moved away from it. Constructing a dataflow graph imperatively
can be convenient, but both Tensorflow and SAC are unsafe, in the sense that ‘illegal’ dataflow graphs can
be constructed during the execution, which leads to unsafe behaviour. These problems can be avoided by a
judicious language design.
We present an idealised calculus for dataflow with both imperative and functional features using an abstract
machine model based on Geometry of Interaction enhanced with rewriting features (‘Dynamic GoI’). Although
the language is modal, with distinct executions for the PCF-like fragment and the DFG fragment, the syntax
of the language is uniform. So the language lacks the “metaprogramming” feel of TensorFlow and other
embedded DSL-like solutions. Concretely, any operator is used in the same way whether as a part of the host
language or the DFG. This is akin to operator overloading, except that it is realised an a purely semantic way.
Establishing a “semantic context”, defined by its history of execution, is as far as we know a novel approach
which, as we shall see, will require a novel approach to semantics.
We have also proved safety of the language and its in-principle efficiency. A prototype implementation of
the calculus is also described, as a PPX extension of the OCaml programming language.
ACM CCS 2012
Theory of computation → Operational semantics;
Keywords Semantics of programming languages, Dataflow computation, Geometry of Interaction,

Synchronous computation

The Art, Science, and Engineering of Programming
Submitted

June 21, 2020

Published

February 28, 2021

doi

10.22152/programming-journal.org/2021/5/12
© Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
This work is licensed under a “CC BY 4.0” license.
In The Art, Science, and Engineering of Programming, vol. 5, no. 3, 2021, article 12; 55 pages.

## PDF page 2

Transparent Synchronous Dataflow

1

Introduction

1.1 Background

Dataflow programming is a broad programming paradigm loosely based on the
principle that computation is organised as a graph in which data-changes to the inputs
are propagated to the outputs in a more-or-less automatic manner. Notable examples
include spreadsheets [51], system analysis and simulation [16], machine learning [1],
embedded reactive systems [28], functional reactive programming (FRP) [18] and
more.
One of the attractive features of dataflow systems is that their native mode of
operation lacks control flow, so it is inherently parallel. This makes issues such as
synchrony and (non)determinism pertinent. The parallelism of dataflow system is
transparent, with much of the event-level manipulation hidden from the programmer,
so ‘lower level’ issues such as deadlock are usually not a concern. Pure dataflow
programming is convenient, but only suitable for particular applications. So it is
more common to have dataflow-style idioms and libraries within general purpose
programming. This is the case with FRP. The language design challenge is nontrivial. When the host language is used natively to construct the dataflow graph
gross inefficiency can be a serious problem, particularly when streams of data must
be merged, which leads to explosive memory requirements. This is unavoidable in
monadic FRP, where the monad multiplication requires the merging of a stream of
streams into a single stream. Different languages deal with this problems in different
ways, for example by replacing monads with ‘arrows’ in FRP [37], by using temporal
type systems [33], or by clocking each data stream in such a way that streams can be
merged using fixed-size buffers [12].
Whereas dataflow functionality can be seamlessly integrated into a larger language (FRP for Haskell) ‘modal’ behaviour, consisting of a model-building mode and
a model-execution mode remains popular for nich languages. Simulink [16], earlier
Tensorflow [1], or Lucid Synchrone [40] are examples of such languages. These languages have two distinct modes of execution, one that constructs the dataflow model
using a more expressive host language, and one that executes the dataflow model.
An extremal example are spreadsheet programs in which the model-building mode is
usually the manual manipulation of the spreadsheet itself in the application, and the
model execution mode is the fully transparent propagation of changes whenever the
value of a spreadsheet cell is changed.
More recently, these dataflow oriented programming languages have become attractive because they facilitate an easy and efficient implementation of automatic
differentiation (AD) [27] . Most conventional AD techniques apply to so-called “straight
line code” which corresponds to ground-type recursion-free pure functional code. Because models in general have type Rn → Rn the restriction to straight-line code is not
crippling. However, in practice constructing large models of a complex graph topology,
for instance a neural network with tens of thousands of parameters, requires that the
model is created using a more expressive programming language. Only the runtime
version of the model is then straight-line code. There are some notable exceptions to

12: 2

## PDF page 3

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

the rule, for example LSTM neural networks which have a stateful model [22], but
this is a very popular programming paradigm. The straight-line-code model can be
constructed in meta-programming style in platforms such as early TensorFlow, but this
programming model is considered awkward, although very suitable for AD. Models
specified seamlessly in an expressive programming languages are a more convenient
way to program, but interaction with AD becomes much more difficult. Applying AD
to higher order languages with or without effects remains an active area of research
without definitive solutions [6].
1.2 Problem statement and contribution

Dataflow languages are extremely popular — the number of spreadsheet users alone
greatly exceeds the number of programmers of any mainstream programming language — so studying them is arguably worthwhile. Semantically, so long as such
languages are hosted inside safe languages, safety is not an issue. Safety is also not
an issue in the case of ‘pure’ dataflow languages, in which the semantic model can be
expressed denotationally via systems of recursive and co-recursive equations, such as
in the case of Lucid Synchrone [9]. In these cases the interesting issue is efficiency,
particularly of memory utilisation.
A semantically interesting question occurs in the case of languages which allow
the explicit manipulation of the dataflow graph using imperative constructs. This
is the case of Tensorflow [1] and of (imperative) self-adjusting computation (SAC)
systems such as the Incremental library for OCaml [43]. The latter, although primarily
intended for usage in high-performance computation [2], proved to be a convenient
dataflow idiom for user interfaces and web programming.
Constructing a dataflow graph imperatively can be convenient, but both TensorFlow and Incremental are unsafe, in the sense that ‘illegal’ dataflow graphs can be
constructed during the execution, which leads to unsafe behaviour. In the case of
TensorFlow it is possible for the dataflow evaluation to diverge because of cyclic
dependencies, whereas in the case of Incremental illegal dataflow graphs with cycles
cause crashes. These problems can be avoided by a judicious language design.
In this paper we propose a programming language which is:
imperative: the dataflow (computation) graph is explicitly manipulated using commands;
functional: the language includes (call-by-value) PCF [48] as a subset;
simply-typed: the type system is essentially that of PCF;
modal: the execution of the dataflow (computation) graph is also controlled by explicit
commands;
parallel: the dataflow graph is executed in parallel.
For such a programming language, establishing safety and memory efficiency are
both challenging and non-trivial problems. Our theoretical contributions are:
specification: we give a precise mathematical definition of the language using an
abstract machine, harmonising the semantics of the PCF-like language with that of
dataflow;

12: 3

## PDF page 4

Transparent Synchronous Dataflow
safety: we show that for any well-typed program the abstract machine executes

without reaching illegal states;
deterministic: we show that the parallel evaluation of the dataflow graph produces
deterministic results;
termination: moreover, we show that the execution of any recursion-free program
with dataflow terminates by reaching the final state of the abstract machine;
efficiency: we prove that no operation is ‘expensive’ in terms of time and memory
utilisation.
These technical results add up to the most important contribution of the
paper, which is one of programming language design. We demonstrated that functional
and dataflow programming, resulting in the runtime creation of straight-line-code
models, can be integrated seamlessly (syntactically and semantically), safely, and
efficiently.
Remark.

2

Synchronous Dataflow

Before technical details are provided let us try to understand the intended semantics
of the language via some simple examples. This examples, although simple, should
illustrate the versatility of the imperative style of constructing dataflow graphs. The
starting language is call-by-value PCF, a typical language combining the simply-typed
lambda calculus with arithmetic-logical operations and recursion. To it we add a new
type of Cells along with facilities for manipulating them. The distinction between the
type of cells and type of integers is more subtle than in languages with assignable state:
the nodes in the dataflow graph have type Cell whereas their inputs and outputs are
edges and have type Int. Note that in our graphs, the edges represent the dependency
relations between nodes, therefore the input of a node would be represented by its
outgoing edge (on top) while the output its incoming edge (at the bottom).
2.1 Dataflow graphs

The default mode of a program is to construct a dataflow graph, which we will describe
now. The nodes of a dataflow graph are:
Constants have a single output edge and produce the value stored in the node.
Arithmetic-logic operators have two input edges and one output edge and compute
the operation accordingly.
Contraction nodes have multiple outputs and a single input, copying their input value
to the outputs. They are labelled by a c .
If-then-else have a control input and two input branches, but behave like selectors
rather than control-flow operators.
Cells have a single input, which can modify the stored value, which is the output.
They are labelled with their current value in curly brackets.

12: 4

## PDF page 5

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

For example, the very simple dataflow graph (DFG) in
2
3
figure 1 computes the expression if y ≤ x then x else y , with
{0} {1}
variables (cells) initially x = 0, y = 1. The inputs of the
c
c
cells are connected to the constants 2 and 3, respectively. On
the first execution the DFG will produce 1 and update the
<=
cells. On any subsequent execution the DFG will produce 3.
Note that we are drawing the DFG rather unusually, with the
if
arrows indicating data dependencies rather than the dynamics
of the data flow.
Figure 1 If
The only non-obvious behaviour here is that of the if statement. In a conventional language it is a control-flow operator,
which will evaluate first the test then only one of the branches, depending on the
value of the test. In a dataflow setting both branches of the if statement compute,
with the test selecting which value is propagated further down.
Crucially, what we mean by “an execution” is a propagation
1
of values in the DFG until they either reach the output or they
reach and subsequently updated every cell at most once. This
is the sense in which the DFG is “synchronous”, much like a
{1}
digital circuit. Along computation data travels independently
c
and possibly asynchronously, but all memory cells serve as
synchronisation points. In figure 2 we can see a DFG which
produces 1s and 0s, alternately, with each execution. On each
Figure 2 Alternating
execution the memory cell is updated x ′ = 1 − x .
The drawing of the DFG is unusual in that we point the arrows in the
direction that indicates data dependencies rather than information flow. The reason
is that the actual execution of the DFG, discussed in section 3, is demand-driven,
which each DFG node first requesting data from their dependents, which request data
from their dependents, and so on. This more elaborate execution mode requires some
auxiliary nodes which we have omitted in this initial, informal, presentation.
Remark.

2.2 Graph construction and manipulation

The host language is call-by-value PCF, extended with several key new operations
used to create and manipulate DFGs:
ref : Int → Cell: create and return a new cell node in the dataflow graph initialised
with an integer value;
deref : Cell → Int: take a cell node in the dataflow graph as argument and produce an
incoming edge as result;
root : Cell → Int: take a cell node in the dataflow graph and return its outgoing edge;
link : Cell → Int → Unit: take a cell node and change its outgoing edge to the edge
given as an argument.
To construct programs it is convenient to also have more conventional assignment
and dereferencing operations for instantly changing and reading the values of cells

12: 5

## PDF page 6

Transparent Synchronous Dataflow

1
{1}

x

C

1
f

-

+

+

{i}

{1}

{0}

{0}

C

C

C

C

s

(a)

x

s

s

(b)

(c)

s

(d)

Figure 3 Informal examples

rather than just manipulating dependencies. In these operations the type Integer is
interpreted in the conventional way, as a value. This dual treatment of the type of
integers may seem ambiguous, but it is not, because each integer value can be also
seen as an immutable node in the dataflow graph. Taking the value itself or the edge
of the node means the same thing.
assign : Cell → Int → Unit: change the constant of a cell instantly;
peek : Int → Int: extract the value of a cell instantly.
Finally the command step : Int activates the computation in the dataflow graph by
updating the contents of each cell in parallel, and at most once, if its dependencies
have changed. This allows computing in dataflow graphs with cycles, provided that
each cycle contains at least one cell. In effect, the model of propagation is synchronous,
with the cells serving as synchronisation points. The command will return the number
of updated cells in an update cycle. Knowing the number of updated cells is a useful
convenience, as it will allow repeating the propagation step until the graph ‘stabilises’,
i.e. no more updates happen. This is normally possible if and only if the dataflow
graph lacks cycles.
For the purpose of examples we consider a standard ‘let’ construct as syntactic
sugar. Let us now consider a ‘hello world’ style example for dataflow computation:
state machines. A generic state machine is created in our language by a function (sm)
taking as arguments an initial value i , a transition function f , and a input x :
let sm = λi.λ f .λx.let s = ref i in link s ( f s x); deref s

Because of the way i is used as an argument to reference creation we can think of it as
a plain integer value, whereas f and x should be thought of as edges in the dataflow
graph. The resulting graph will have outgoing edges x , and incoming edge deref s.
Besides the i -initialised cell-node it will also include a special ‘contraction’ node C
so that the incoming edge can be used both as output and as cyclic dependency. The
function f will be used, during execution, to create a desired dataflow graph. The
resulting dataflow will have the general shape given in figure 3a.

12: 6

## PDF page 7

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

Let us call the function above sm and consider some simple instantiations, the
examples are also available in the online visualiser 1 :
oscillator is a state machine which alternates between 0 and 1, defined as let al t =
sm 1 (λs.λi.1 − deref s) 0. Note that the outgoing edge is not used, and 0 is a dummy
value. The created dataflow graph is represented informally in figure 3b, where
the sub-graph produced when the particular transition function was supplied now
has nodes for addition and the constant 1. The cell is initialised to 1.
sum is a state machine which accumulates the value of its inputs into the state, defined
as let sum = λx.sm 0 (λs.λi.i + deref s) x. The dataflow graph is sketched out in
figure 3c.
composite is a state machine which connects the incoming edge of the oscillator to
the outgoing edge of the accumulator, defined as let a = sum(deref al t). It can be
seen in figure 3d.
The code above only constructs the dataflow graph. To execute it we need to execute
the step command along with peek a to read the output. After one step, for example,
the first cell will change its stored value from 1 to 0, and the second one from 0 to 1.
After another step the cells will further change to 1 and 1, respectively, and so on.
Similar programs written in Lucid Synchrone and ReactiveML are shown in appendix A.
Although the language is modal, with distinct executions for the PCF-like
fragment and the DFG fragment, the syntax of the language is uniform. So the
language lacks the “metaprogramming” feel of TensorFlow and other embedded
DSL-like solutions. Concretely, any operator is used in the same way whether as a
part of the host language or the DFG. For example, when we write u + v the semantic
interpretation is able to tease out whether this is PCF addition or DFG addition. This
requires no static analysis or other syntactic solutions such as types, type classes,
operator overloading and so on. This is akin to operator overloading, except that it is
realised an a purely semantic way. Establishing a “semantic context”, defined by its
history of execution, is as far as we know a novel approach which, as we shall see,
will require a novel approach to semantics.
Remark.

2.3 Formal syntax

The calculus is an extension of the simply-typed lambda calculus with base types
integers, integer cells, and unit. Let γ ::= Int | Cell | Unit. These are the base types.
The language has simple types as defined by the grammar τ ::= γ | τ → τ. Terms are
defined by the grammar below with $ being arithmetic operations.
t ::= x | λx.t | t t | n | op | if t then t else t | rec x.t

where op ranges over arithmetic operators +, −, ×, ÷ : Int → Int → Int and the imperative operations on dataflow graphs mentioned earlier. The typing rules of the calculus
are the standard ones for the simply-typed call-by-value PCF (figure 4).
1

https://cwtsteven.github.io/TSD-visual?ex=alt/

12: 7

## PDF page 8

Transparent Synchronous Dataflow

Γ, x : τ ⊢ x : τ
Γ , x : τ ⊢ t : τ′
Γ ⊢ λx.t : τ → τ′
Figure 4

3

Γ ⊢ n : Int

Γ ⊢ op : τ

Γ ⊢ t ′ : τ → τ′ Γ ⊢ t : τ
Γ ⊢ t ′ t : τ′

Γ ⊢ t : Int Γ ⊢ t 1 : γ Γ ⊢ t 1 : γ
Γ ⊢ if t then t 1 else t 2 : γ

Γ , f : τ → τ′ ⊢ t : τ → τ′
Γ ⊢ rec f .t : τ → τ′

Typing rules

Abstract machine semantics

3.1 The Dynamic Geometry of Interaction

We will formulate the semantics of the language using a graph-rewriting abstract
machine called the Dynamic Geometry of Interaction Machine (DGoIM). An abstract
machine semantics has the desirable feature that it can allow reasoning about the
cost of computation. In fact the DGoIM machine has been shown to be optimal, in a
technical sense [4], for a variety of reduction strategies for the lambda calculus [46].
Abstract machines have been generally considered unsuitable for reasoning about
programming languages. However, the DGoIM has been used to define and reason
about the safety of ‘graph abstraction’, an exotic operation inspired by TensorFlow
which converts local state variables into function parameters [44]. A generalisation of
the DGoIM machine has also been used to reason about observational equivalence in
languages with effects [24].
The origins of the DGoIM are in token abstract machines [17] giving semantics to
linear logic proofs via the ‘Geometry of Interaction’ [25]. Using translations of lambda
calculus into its linear version these abstract machines have been also used to model
PCF and related languages [39]. These models proved to be interesting as they lead
to space-efficient compilation schemes which have been used, among other things, to
compile functional languages into circuits [23].
The motivation for a ‘dynamic’ version of the machine was that the original version
only gives an efficient model for call-by-name. To represent call-by-value not only
soundly but also efficiently the ‘token’ that traverses the machine during execution
also modifies it, thus preventing full re-evaluations of components which have been
already evaluated.
Although the graph-rewriting-based approach of the DGoIM is new, and hence it
may appear unintuitive at a first sight, it is in fact closely related to rewrites on the
abstract syntax tree of the term, with a few tweaks:
contraction: Unlike a standard AST in which variables sit in the ‘nodes’ of the tree, in
the DGoIM representation variables with the same name and the same scope are
‘joined’ using ‘contraction’ nodes. Moreover, when the binder of a variable occurs
the edges that correspond to the variable connect back to the binder. In figure 5
you can compare the conventional AST representation of λx.x x to its DGoIM
representation. The graph contains some other GoI-inspired artefacts which we
discuss below.

12: 8

## PDF page 9

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
boxes: In the same figure we can see, that the lambda term is ‘boxed’. This can be

understood as the sub-graph corresponding to the lambda term is a single entity —
for purposes of copying or deleting. This is part of the machinery that allows a
precise cost of computation to be associated with graph rewrite.
linear logic: Besides the contraction node (C ) we can also see a !-labelled node (in
grey) which is also inherited from linear logic. This node, along with ? nodes which
will be seen later, serve as interface nodes to boxes, for arguments and non-local
variables.
Graph rewriting in general can be expensive, in particular the identification of redexes as sub-graphs. In DGoIM
C
this is dealt with by making the rewriting ‘focussed’, i.e.
x
x
relative to a special node in the graph which we call ‘the
x
@
@
token’. The token will traverse the graph and trigger reλ
λ
ductions as needed. In terms of conventional abstract machines, the movement of the token along an edge, seeking
!
a redex, is akin to the ‘narrowing’ of the context in a term
abstract machine, whereas the movement against the edge,
Figure 5 AST vs DGoIM
after a reduction, corresponds to a ‘broadening’ of a termreducing abstract machine. A visualiser is also available
for demonstrating the step-by-step execution of the machine.2
The version of DGoIM machine presented here is essentially the original one, with
the following extensions:
Graph-construction: Semantics for imperative operations for constructing the dataflow
graph. These do not represent significant changes to the machine but are rather
straightforward extensions.
Graph-execution: When the ‘step’ command is executed the program changes modes of
operations, from the functional-imperative mode of execution of graph construction
to the synchronous dataflow mode of execution defined by the graph. This requires
a non-trivial enhancement of the DGoIM, primarily by enabling parallel execution.
3.2 Graph and translation

In this section we present the technical details of the DGOI machine.
A graph G is a set of nodes which are partitioned into proper nodes NodeG (or just
‘nodes’) and port nodes PortG (or just ‘ports’), and a set of directed edges connecting
ports and nodes. Every node is associated and connected with several ports and each
edge has at least one connecting port and there are no open edges. Every port is
the source of at most one edge and the target of another. We also call the source
and the target of a node the incoming port (or in-port) and the outgoing port (or
out-port) respectively. For example the +-node is connected to two out-ports and
one in-port. If a graph contains edges between two ports they are identified by an
edge homeomorphism; our graphs are quotiented by the congruence induced by edge
homeomorphisms in an appropriate category of graphs [32]. We often denote a graph
2

https://cwtsteven.github.io/TSD-visual/

12: 9

## PDF page 10

Transparent Synchronous Dataflow

<latexit sha1_base64="SHQ0ZfdGDVDGgzwpUoUdVkKu4sc=">AAAB73icbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJkdnacmRXCkp/w4kERr/6ON//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7o5RKewFvVLZr/hzkFUS5KQMOeq90le3n9A0ZtJSgcZ0Al/ZMENtORVsWuymhimkYxyyjqMSY2bCbH7vlJw7pU8GiXYlLZmrvycyjI2ZxJHrjNGOzLI3E//zOqkd3IQZlyq1TNLFokEqiE3I7HnS55pRKyaOINXc3UroCDVS6yIquhCC5ZdXSbNaCS4r1furco3kcRTgFM7gAgK4hhrcQR0aQEHAM7zCm/fovXjv3seidc3LZ07gD7zPH7aej6U=</latexit>

1

2 !(1(2 ) 1

⌘

<latexit sha1_base64="SHQ0ZfdGDVDGgzwpUoUdVkKu4sc=">AAAB73icbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJkdnacmRXCkp/w4kERr/6ON//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7o5RKewFvVLZr/hzkFUS5KQMOeq90le3n9A0ZtJSgcZ0Al/ZMENtORVsWuymhimkYxyyjqMSY2bCbH7vlJw7pU8GiXYlLZmrvycyjI2ZxJHrjNGOzLI3E//zOqkd3IQZlyq1TNLFokEqiE3I7HnS55pRKyaOINXc3UroCDVS6yIquhCC5ZdXSbNaCS4r1furco3kcRTgFM7gAgK4hhrcQR0aQEHAM7zCm/fovXjv3seidc3LZ07gD7zPH7aej6U=</latexit>

<latexit sha1_base64="216BsO9cXKL/D9qldrA8YJiACqM=">AAAB73icbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJkdnacmRXCkp/w4kERr/6ON//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7o5RKexVe6WyX/HnIKskyEkZctR7pa9uP6FpzKSlAo3pBL6yYYbacirYtNhNDVNIxzhkHUclxsyE2fzeKTl3Sp8MEu1KWjJXf09kGBsziSPXGaMdmWVvJv7ndVI7uAkzLlVqmaSLRYNUEJuQ2fOkzzWjVkwcQaq5u5XQEWqk1kVUdCEEyy+vkma1ElxWqvdX5RrJ4yjAKZzBBQRwDTW4gzo0gIKAZ3iFN+/Re/HevY9F65qXz5zAH3ifP7gij6Y=</latexit>

<latexit sha1_base64="s8UhI6OsAnPmUDzfjVa1rVvPHvs=">AAAB63icbVBNS8NAEN3Ur1q/qh69LBbBU0mqoMeCF48V7Ae0oWy2k3bp7ibsToQS+he8eFDEq3/Im//GpM1BWx8MPN6bYWZeEEth0XW/ndLG5tb2Tnm3srd/cHhUPT7p2CgxHNo8kpHpBcyCFBraKFBCLzbAVCChG0zvcr/7BMaKSD/iLAZfsbEWoeAMc2kAyIbVmlt3F6DrxCtIjRRoDatfg1HEEwUauWTW9j03Rj9lBgWXMK8MEgsx41M2hn5GNVNg/XRx65xeZMqIhpHJSiNdqL8nUqasnakg61QMJ3bVy8X/vH6C4a2fCh0nCJovF4WJpBjR/HE6EgY4yllGGDciu5XyCTOMYxZPJQvBW315nXQade+q3ni4rjVpEUeZnJFzckk8ckOa5J60SJtwMiHP5JW8Ocp5cd6dj2VrySlmTskfOJ8//+eOGg==</latexit>

Cell

Cell

r

d

!Int

!Int

<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

!Int !Int

<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

!Int

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="IpyBY97HslFsjw82STBs68xcia0=">AAACD3icbVDLTgIxFO34RHyNunRTJBrckBk00SWJG5eYyCMBQu6UAg3tTNN2TMiEP3Djr7hxoTFu3brzbyzDLBQ8TZPTc+7N7T2B5Ewbz/t2VlbX1jc2c1v57Z3dvX334LCho1gRWicRj1QrAE05C2ndMMNpSyoKIuC0GYxvZn7zgSrNovDeTCTtChiGbMAIGCv13LOkMC11xiAl9PxOwR4Rc8MEyPQxNyrnPbfolb0UeJn4GSmiDLWe+9XpRyQWNDSEg9Zt35Omm4AyjHA6zXdiTSWQMQxp29IQBNXdJN1nik+t0seDSNkbGpyqvzsSEFpPRGArBZiRXvRm4n9eOzaD627CQhkbGpL5oEHMsYnwLBzcZ4oSwyeWAFHM/hWTESggxkaYtyH4iysvk0al7F+UK3eXxSrO4sihY3SCSshHV6iKblEN1RFBj+gZvaI358l5cd6dj3npipP1HKE/cD5/AMflmx8=</latexit>

@

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

<latexit sha1_base64="EODeSM1dpGiTeNlPbex3j3ELD5U=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipWR+UK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AiG2Mpg==</latexit>

1(2

<latexit sha1_base64="216BsO9cXKL/D9qldrA8YJiACqM=">AAAB73icbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJkdnacmRXCkp/w4kERr/6ON//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7o5RKexVe6WyX/HnIKskyEkZctR7pa9uP6FpzKSlAo3pBL6yYYbacirYtNhNDVNIxzhkHUclxsyE2fzeKTl3Sp8MEu1KWjJXf09kGBsziSPXGaMdmWVvJv7ndVI7uAkzLlVqmaSLRYNUEJuQ2fOkzzWjVkwcQaq5u5XQEWqk1kVUdCEEyy+vkma1ElxWqvdX5RrJ4yjAKZzBBQRwDTW4gzo0gIKAZ3iFN+/Re/HevY9F65qXz5zAH3ifP7gij6Y=</latexit>

<latexit sha1_base64="YjziHtzyc9phwA3VBfgdXl0HLRw=">AAACDHicbVC7TgMxEPSFVwivACWNIUGiiu6OAspINJRBIg8pF0V7ji+xYvss24cURfkAGn6FhgKEaPkAOv4G51FAwlqWxjOzWu/EijNjff/by62tb2xu5bcLO7t7+wfFw6OGSTNNaJ2kPNWtGAzlTNK6ZZbTltIURMxpMx7eTPXmA9WGpfLejhTtCOhLljAC1lHdYqkcDUEp6AbRqTsi45YJULPHXAjLzuVX/FnhVRAsQAktqtYtfkW9lGSCSks4GNMOfGU7Y9CWEU4nhSgzVAEZQp+2HZQgqOmMZ8tM8LljejhJtbvS4hn7u2MMwpiRiJ1TgB2YZW1K/qe1M5tcd8ZMqsxSSeaDkoxjm+JpMrjHNCWWjxwAopn7KyYD0ECsy6/gQgiWV14FjbASXFbCu7BUxYs48ugEnaELFKArVEW3qIbqiKBH9Ixe0Zv35L14797H3JrzFj3H6E95nz93upnd</latexit>

!Int Cell

Cell

2

<latexit sha1_base64="XDCoHSLKgh+RgE0vUntXcLjjcY4=">AAAB83icbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBlwY3uKtgHdIaSSTNtaJIZkoxQhv6GGxeKuPVn3Pk3ZtpZaOuBwOGce7knJ0w408Z1v53S2vrG5lZ5u7Kzu7d/UD086ug4VYS2Scxj1QuxppxJ2jbMcNpLFMUi5LQbTm5zv/tElWaxfDTThAYCjySLGMHGSr4vsBkrkd1LMxtUa27dnQOtEq8gNSjQGlS//GFMUkGlIRxr3ffcxAQZVoYRTmcVP9U0wWSCR7RvqcSC6iCbZ56hc6sMURQr+6RBc/X3RoaF1lMR2sk8o172cvE/r5+a6CbImExSQyVZHIpSjkyM8gLQkClKDJ9agoliNisiY6wwMbamii3BW/7yKuk06t5lvfFwVWueFHWU4RTO4AI8uIYm3EEL2kAggWd4hTcndV6cd+djMVpyip1j+APn8wd24ZHU</latexit>

()

<latexit sha1_base64="l7qUFD+Ap+Lm0zOhf0IgfOIR7aE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQflilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/VuYzZ</latexit>

s

p

<latexit sha1_base64="iPTQc4GWN4Ze5khPiuuvqg80POI=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipmQzKFbfqLkDWiZeTCuRoDMpf/WHM0gilYYJq3fPcxPgZVYYzgbNSP9WYUDahI+xZKmmE2s8Wh87IhVWGJIyVLWnIQv09kdFI62kU2M6ImrFe9ebif14vNeGtn3GZpAYlWy4KU0FMTOZfkyFXyIyYWkKZ4vZWwsZUUWZsNiUbgrf68jpp16reVbXWvK7USR5HEc7gHC7Bgxuowz00oAUMEJ7hFd6cR+fFeXc+lq0FJ585hT9wPn8A0S2M1g==</latexit>

<latexit sha1_base64="MGYvqdsDx04M0mCioUDqd5bJQoE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/UNYzY</latexit>

Int

<latexit sha1_base64="a0poHv29MI5/0HI+DVy3HJiOLaE=">AAAB9HicbVBNSwMxFHzrZ61fVS+Cl2ARPJXdKuix4MVjBbcttEvJptk2NMmuSbZQlv4OLx4U8eqP8ea/MdvuQVsHAsPMe7zJhAln2rjut7O2vrG5tV3aKe/u7R8cVo6OWzpOFaE+iXmsOiHWlDNJfcMMp51EUSxCTtvh+C732xOqNIvlo5kmNBB4KFnECDZWCnoCm5ESmS+ZmfUrVbfmzoFWiVeQKhRo9itfvUFMUkGlIRxr3fXcxAQZVoYRTmflXqppgskYD2nXUokF1UE2Dz1DF1YZoChW9kmD5urvjQwLracitJN5SL3s5eJ/Xjc10W2QMZmkhkqyOBSlHJkY5Q2gAVOUGD61BBPFbFZERlhhYmxPZVuCt/zlVdKq17yrWv3huto4LeoowRmcwyV4cAMNuIcm+EDgCZ7hFd6cifPivDsfi9E1p9g5gT9wPn8AUleSUw==</latexit>

Unit

⌘

!Int
<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="s8UhI6OsAnPmUDzfjVa1rVvPHvs=">AAAB63icbVBNS8NAEN3Ur1q/qh69LBbBU0mqoMeCF48V7Ae0oWy2k3bp7ibsToQS+he8eFDEq3/Im//GpM1BWx8MPN6bYWZeEEth0XW/ndLG5tb2Tnm3srd/cHhUPT7p2CgxHNo8kpHpBcyCFBraKFBCLzbAVCChG0zvcr/7BMaKSD/iLAZfsbEWoeAMc2kAyIbVmlt3F6DrxCtIjRRoDatfg1HEEwUauWTW9j03Rj9lBgWXMK8MEgsx41M2hn5GNVNg/XRx65xeZMqIhpHJSiNdqL8nUqasnakg61QMJ3bVy8X/vH6C4a2fCh0nCJovF4WJpBjR/HE6EgY4yllGGDciu5XyCTOMYxZPJQvBW315nXQade+q3ni4rjVpEUeZnJFzckk8ckOa5J60SJtwMiHP5JW8Ocp5cd6dj2VrySlmTskfOJ8//+eOGg==</latexit>

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="SCiHxsF35CnyMeIpKKgzqwMIS9I=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3a3STsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgkfYMtwI7CYKqQwEdoLJ3dzvPKHSPI4ezDRBX9JRxEPOqLFSUw7KFbfqLkDWiZeTCuRoDMpf/WHMUomRYYJq3fPcxPgZVYYzgbNSP9WYUDahI+xZGlGJ2s8Wh87IhVWGJIyVrciQhfp7IqNS66kMbKekZqxXvbn4n9dLTXjrZzxKUoMRWy4KU0FMTOZfkyFXyIyYWkKZ4vZWwsZUUWZsNiUbgrf68jpp16reVbXWvK7USR5HEc7gHC7Bgxuowz00oAUMEJ7hFd6cR+fFeXc+lq0FJ585hT9wPn8AzKGM0w==</latexit>

<latexit sha1_base64="kNQVNiwXGiId9rXqnZFBN477O/U=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJu3azSbsboRS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBVcG9f9dgobm1vbO8Xd0t7+weFR+fikrZNMMWyxRCSqG1CNgktsGW4EdlOFNA4EdoLx3dzvPKHSPJEPZpKiH9Oh5BFn1FipGQ7KFbfqLkDWiZeTCuRoDMpf/TBhWYzSMEG17nluavwpVYYzgbNSP9OYUjamQ+xZKmmM2p8uDp2RC6uEJEqULWnIQv09MaWx1pM4sJ0xNSO96s3F/7xeZqJbf8plmhmUbLkoygQxCZl/TUKukBkxsYQyxe2thI2ooszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4Avv2Myg==</latexit>

<latexit sha1_base64="uCO/pVMTmPk3yEIZVCeXCZBUqgI=">AAAB/3icbVDNS8MwHE3n15xfVUEEL9EheBrtFPQ4EMTjBPcBWxlplm5hSVqSVBi1B/8VLx4U8eq/4c3/xrTrQTcfhDze+/3Iy/MjRpV2nG+rtLS8srpWXq9sbG5t79i7e20VxhKTFg5ZKLs+UoRRQVqaaka6kSSI+4x0/Ml15nceiFQ0FPd6GhGPo5GgAcVIG2lgHyTHaZ8jPZY8yW/fT27SdGBXnZqTAy4StyBVUKA5sL/6wxDHnAiNGVKq5zqR9hIkNcWMpJV+rEiE8ASNSM9QgThRXpLnT+GpUYYwCKU5QsNc/b2RIK7UlPtmMouo5r1M/M/rxTq48hIqolgTgWcPBTGDOoRZGXBIJcGaTQ1BWFKTFeIxkghrU1nFlODOf3mRtOs197xWv7uoNg6LOsrgCJyAM+CCS9AAt6AJWgCDR/AMXsGb9WS9WO/Wx2y0ZBU7++APrM8fpEGWXw==</latexit>

<latexit sha1_base64="s8UhI6OsAnPmUDzfjVa1rVvPHvs=">AAAB63icbVBNS8NAEN3Ur1q/qh69LBbBU0mqoMeCF48V7Ae0oWy2k3bp7ibsToQS+he8eFDEq3/Im//GpM1BWx8MPN6bYWZeEEth0XW/ndLG5tb2Tnm3srd/cHhUPT7p2CgxHNo8kpHpBcyCFBraKFBCLzbAVCChG0zvcr/7BMaKSD/iLAZfsbEWoeAMc2kAyIbVmlt3F6DrxCtIjRRoDatfg1HEEwUauWTW9j03Rj9lBgWXMK8MEgsx41M2hn5GNVNg/XRx65xeZMqIhpHJSiNdqL8nUqasnakg61QMJ3bVy8X/vH6C4a2fCh0nCJovF4WJpBjR/HE6EgY4yllGGDciu5XyCTOMYxZPJQvBW315nXQade+q3ni4rjVpEUeZnJFzckk8ckOa5J60SJtwMiHP5JW8Ocp5cd6dj2VrySlmTskfOJ8//+eOGg==</latexit>

m

<latexit sha1_base64="JQ7O+IXGKQnCywzOP7HUyj374DU=">AAAB6XicbVBNS8NAEJ3Ur1q/qh69LFbBU0mqoMeCF49V7Ae0oWy2k3bpZhN2N0IJ/QdePCji1X/kzX/jts1BWx8MPN6bYWZekAiujet+O4W19Y3NreJ2aWd3b/+gfHjU0nGqGDZZLGLVCahGwSU2DTcCO4lCGgUC28H4dua3n1BpHstHM0nQj+hQ8pAzaqz00Dvrlytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzS+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjM3iYDrpAZMbGEMsXtrYSNqKLM2HBKNgRv+eVV0qpVvctq7f6qUid5HEU4gVO4AA+uoQ530IAmMAjhGV7hzRk7L86787FoLTj5zDH8gfP5Aw68jPA=</latexit>

Cell

⌫
<latexit sha1_base64="FDznS7llVbni0+b+hTTzHTOVH/8=">AAAB6nicbVBNS8NAEJ3Ur1q/qh69LBbBU0lqQY8FLx4r2g9oQ9lsN+3SzSbsToQS+hO8eFDEq7/Im//GbZuDtj4YeLw3w8y8IJHCoOt+O4WNza3tneJuaW//4PCofHzSNnGqGW+xWMa6G1DDpVC8hQIl7yaa0yiQvBNMbud+54lrI2L1iNOE+xEdKREKRtFKD32VDsoVt+ouQNaJl5MK5GgOyl/9YczSiCtkkhrT89wE/YxqFEzyWamfGp5QNqEj3rNU0YgbP1ucOiMXVhmSMNa2FJKF+nsio5Ex0yiwnRHFsVn15uJ/Xi/F8MbPhEpS5IotF4WpJBiT+d9kKDRnKKeWUKaFvZWwMdWUoU2nZEPwVl9eJ+1a1buq1u7rlQbJ4yjCGZzDJXhwDQ24gya0gMEInuEV3hzpvDjvzseyteDkM6fwB87nD1X3jbk=</latexit>

<latexit sha1_base64="s8UhI6OsAnPmUDzfjVa1rVvPHvs=">AAAB63icbVBNS8NAEN3Ur1q/qh69LBbBU0mqoMeCF48V7Ae0oWy2k3bp7ibsToQS+he8eFDEq3/Im//GpM1BWx8MPN6bYWZeEEth0XW/ndLG5tb2Tnm3srd/cHhUPT7p2CgxHNo8kpHpBcyCFBraKFBCLzbAVCChG0zvcr/7BMaKSD/iLAZfsbEWoeAMc2kAyIbVmlt3F6DrxCtIjRRoDatfg1HEEwUauWTW9j03Rj9lBgWXMK8MEgsx41M2hn5GNVNg/XRx65xeZMqIhpHJSiNdqL8nUqasnakg61QMJ3bVy8X/vH6C4a2fCh0nCJovF4WJpBjR/HE6EgY4yllGGDciu5XyCTOMYxZPJQvBW315nXQade+q3ni4rjVpEUeZnJFzckk8ckOa5J60SJtwMiHP5JW8Ocp5cd6dj2VrySlmTskfOJ8//+eOGg==</latexit>

$

!Int

<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

⌘ ⌘ !(1(2 ) !(1(2 )

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

n
<latexit sha1_base64="Jsdndm8LHo00H+MdK7j7c46DUsk=">AAAB9XicbVDLSgMxFL1TX7W+qi7dBItQN2WmCrosuHFZwT6gHUsmvW1DM5khyShl6H+4caGIW//FnX9j2s5CWw8EDufcw705QSy4Nq777eTW1jc2t/LbhZ3dvf2D4uFRU0eJYthgkYhUO6AaBZfYMNwIbMcKaRgIbAXjm5nfekSleSTvzSRGP6RDyQecUWOlh24i+6hm4bR8Pu0VS27FnYOsEi8jJchQ7xW/uv2IJSFKwwTVuuO5sfFTqgxnAqeFbqIxpmxMh9ixVNIQtZ/Or56SM6v0ySBS9klD5urvREpDrSdhYCdDakZ62ZuJ/3mdxAyu/ZTLODEo2WLRIBHERGRWAelzhcyIiSWUKW5vJWxEFWXGFlWwJXjLX14lzWrFu6hU7y5LNZLVkYcTOIUyeHAFNbiFOjSAgYJneIU358l5cd6dj8Vozskyx/AHzucPY1SSUw==</latexit>

!Int !F

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>

<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

<latexit sha1_base64="qwmkCCdWplvKEzFyiMtXfVPNC8U=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmEsRvWG23QXwOvEK0kDleiM6l9+lFKTgNCUE6WGnpvpICdSM8phXvONgozQKRnD0FJBElBBvrh5ji+sEuE4lfYJjRfq70ROEqVmSWgnE6InatUrxP+8odHxbZAzkRkNgi4XxYZjneKiABwxCVTzmSWESmZvxXRCJKHa1lSzJXirX14nvVbTu2q2Hq4bbVzWUUVn6BxdIg/doDa6Rx3URRRl6Bm9ojfHOC/Ou/OxHK04ZeYU/YHz+QPzxpGE</latexit>

<latexit sha1_base64="8cnDkrAWRdnw8+gsb8OGvDIbEgc=">AAAB+HicbVBNS8NAFHypX7V+NOpF8LJaBE8lqYIeC170VsHaQhvKZrtpl242YXcj1JBf4sWDIl79Kd78N27aHLR1YGGYeY83O37MmdKO822VVlbX1jfKm5Wt7Z3dqr23/6CiRBLaJhGPZNfHinImaFszzWk3lhSHPqcdf3Kd+51HKhWLxL2extQL8UiwgBGsjTSwq/0Q67EM0/Q4uxU6G9g1p+7MgJaJW5AaFGgN7K/+MCJJSIUmHCvVc51YeymWmhFOs0o/UTTGZIJHtGeowCFVXjoLnqFTowxREEnzhEYz9fdGikOlpqFvJvOYatHLxf+8XqKDKy9lIk40FWR+KEg40hHKW0BDJinRfGoIJpKZrIiMscREm64qpgR38cvL5KFRd8/rjbuLWvOwqKMMR3ACZ+DCJTThBlrQBgIJPMMrvFlP1ov1bn3MR0tWsXMAf2B9/gAXNpM8</latexit>





<latexit sha1_base64="GpUah58jeuTgVaqvPNlg/vXfUGE=">AAAB7XicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJmdnaYmRXCkn/w4kERr/6PN//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7I5RKeyVyn7Fn4OskiAnZchR75W+uv2EpjGTlgo0phP4yoYZasupYNNiNzVMIR3jkHUclRgzE2bza6fk3Cl9Mki0K2nJXP09kWFszCSOXGeMdmSWvZn4n9dJ7eAmzLhUqWWSLhYNUkFsQmavkz7XjFoxcQSp5u5WQkeokVoXUNGFECy/vEqa1UpwWaneX5VrJI+jAKdwBhcQwDXU4A7q0AAKj/AMr/DmJd6L9+59LFrXvHzmBP7A+/wBjUCPAQ==</latexit>

<latexit sha1_base64="GpUah58jeuTgVaqvPNlg/vXfUGE=">AAAB7XicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJmdnaYmRXCkn/w4kERr/6PN//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7I5RKeyVyn7Fn4OskiAnZchR75W+uv2EpjGTlgo0phP4yoYZasupYNNiNzVMIR3jkHUclRgzE2bza6fk3Cl9Mki0K2nJXP09kWFszCSOXGeMdmSWvZn4n9dJ7eAmzLhUqWWSLhYNUkFsQmavkz7XjFoxcQSp5u5WQkeokVoXUNGFECy/vEqa1UpwWaneX5VrJI+jAKdwBhcQwDXU4A7q0AAKj/AMr/DmJd6L9+59LFrXvHzmBP7A+/wBjUCPAQ==</latexit>

<latexit sha1_base64="uCO/pVMTmPk3yEIZVCeXCZBUqgI=">AAAB/3icbVDNS8MwHE3n15xfVUEEL9EheBrtFPQ4EMTjBPcBWxlplm5hSVqSVBi1B/8VLx4U8eq/4c3/xrTrQTcfhDze+/3Iy/MjRpV2nG+rtLS8srpWXq9sbG5t79i7e20VxhKTFg5ZKLs+UoRRQVqaaka6kSSI+4x0/Ml15nceiFQ0FPd6GhGPo5GgAcVIG2lgHyTHaZ8jPZY8yW/fT27SdGBXnZqTAy4StyBVUKA5sL/6wxDHnAiNGVKq5zqR9hIkNcWMpJV+rEiE8ASNSM9QgThRXpLnT+GpUYYwCKU5QsNc/b2RIK7UlPtmMouo5r1M/M/rxTq48hIqolgTgWcPBTGDOoRZGXBIJcGaTQ1BWFKTFeIxkghrU1nFlODOf3mRtOs197xWv7uoNg6LOsrgCJyAM+CCS9AAt6AJWgCDR/AMXsGb9WS9WO/Wx2y0ZBU7++APrM8fpEGWXw==</latexit>

!F

<latexit sha1_base64="IpyBY97HslFsjw82STBs68xcia0=">AAACD3icbVDLTgIxFO34RHyNunRTJBrckBk00SWJG5eYyCMBQu6UAg3tTNN2TMiEP3Djr7hxoTFu3brzbyzDLBQ8TZPTc+7N7T2B5Ewbz/t2VlbX1jc2c1v57Z3dvX334LCho1gRWicRj1QrAE05C2ndMMNpSyoKIuC0GYxvZn7zgSrNovDeTCTtChiGbMAIGCv13LOkMC11xiAl9PxOwR4Rc8MEyPQxNyrnPbfolb0UeJn4GSmiDLWe+9XpRyQWNDSEg9Zt35Omm4AyjHA6zXdiTSWQMQxp29IQBNXdJN1nik+t0seDSNkbGpyqvzsSEFpPRGArBZiRXvRm4n9eOzaD627CQhkbGpL5oEHMsYnwLBzcZ4oSwyeWAFHM/hWTESggxkaYtyH4iysvk0al7F+UK3eXxSrO4sihY3SCSshHV6iKblEN1RFBj+gZvaI358l5cd6dj3npipP1HKE/cD5/AMflmx8=</latexit>

<latexit sha1_base64="IpyBY97HslFsjw82STBs68xcia0=">AAACD3icbVDLTgIxFO34RHyNunRTJBrckBk00SWJG5eYyCMBQu6UAg3tTNN2TMiEP3Djr7hxoTFu3brzbyzDLBQ8TZPTc+7N7T2B5Ewbz/t2VlbX1jc2c1v57Z3dvX334LCho1gRWicRj1QrAE05C2ndMMNpSyoKIuC0GYxvZn7zgSrNovDeTCTtChiGbMAIGCv13LOkMC11xiAl9PxOwR4Rc8MEyPQxNyrnPbfolb0UeJn4GSmiDLWe+9XpRyQWNDSEg9Zt35Omm4AyjHA6zXdiTSWQMQxp29IQBNXdJN1nik+t0seDSNkbGpyqvzsSEFpPRGArBZiRXvRm4n9eOzaD627CQhkbGpL5oEHMsYnwLBzcZ4oSwyeWAFHM/hWTESggxkaYtyH4iysvk0al7F+UK3eXxSrO4sihY3SCSshHV6iKblEN1RFBj+gZvaI358l5cd6dj3npipP1HKE/cD5/AMflmx8=</latexit>

a

l

<latexit sha1_base64="KRKwyXUtEvutNvkeZUfGqRTF1zQ=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipSQflilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz+6cYzH</latexit>

!Unit
<latexit sha1_base64="MnOPJz76imJa2Xns47PpOydHb5I=">AAAB+XicbVBNS8NAFHypX7V+Rb0IXlaL4KkkVdBjwYvHCsYW2lA22027dLMJu5tCCfknXjwo4tV/4s1/46bNQVsHFoaZ93izEyScKe0431ZlbX1jc6u6XdvZ3ds/sA+PnlScSkI9EvNYdgOsKGeCepppTruJpDgKOO0Ek7vC70ypVCwWj3qWUD/CI8FCRrA20sC2s7O8H2E9llHmCabzgV13Gs4caJW4JalDifbA/uoPY5JGVGjCsVI910m0n2GpGeE0r/VTRRNMJnhEe4YKHFHlZ/PkObowyhCFsTRPaDRXf29kOFJqFgVmsgiplr1C/M/rpTq89TMmklRTQRaHwpQjHaOiBjRkkhLNZ4ZgIpnJisgYS0y0KatmSnCXv7xKnpoN96rRfLiut07KOqpwCudwCS7cQAvuoQ0eEJjCM7zCm5VZL9a79bEYrVjlzjH8gfX5A/KDk7s=</latexit>

<latexit sha1_base64="L3w36hKZEf3CPUHXd8crJ2oG19k=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipKQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/LHYzS</latexit>

!Unit
<latexit sha1_base64="MnOPJz76imJa2Xns47PpOydHb5I=">AAAB+XicbVBNS8NAFHypX7V+Rb0IXlaL4KkkVdBjwYvHCsYW2lA22027dLMJu5tCCfknXjwo4tV/4s1/46bNQVsHFoaZ93izEyScKe0431ZlbX1jc6u6XdvZ3ds/sA+PnlScSkI9EvNYdgOsKGeCepppTruJpDgKOO0Ek7vC70ypVCwWj3qWUD/CI8FCRrA20sC2s7O8H2E9llHmCabzgV13Gs4caJW4JalDifbA/uoPY5JGVGjCsVI910m0n2GpGeE0r/VTRRNMJnhEe4YKHFHlZ/PkObowyhCFsTRPaDRXf29kOFJqFgVmsgiplr1C/M/rpTq89TMmklRTQRaHwpQjHaOiBjRkkhLNZ4ZgIpnJisgYS0y0KatmSnCXv7xKnpoN96rRfLiut07KOqpwCudwCS7cQAvuoQ0eEJjCM7zCm5VZL9a79bEYrVjlzjH8gfX5A/KDk7s=</latexit>

if

<latexit sha1_base64="JfNhHDmiXWSkW51tt1a0oYAngQE=">AAAB6nicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWNE84BkCbOT2WTIzOwy0yuEkE/w4kERr36RN//GSbIHTSxoKKq66e6KUiks+v63t7a+sbm1Xdgp7u7tHxyWjo6bNskM4w2WyMS0I2q5FJo3UKDk7dRwqiLJW9Hodua3nrixItGPOE55qOhAi1gwik566KqsVyr7FX8OskqCnJQhR71X+ur2E5YprpFJam0n8FMMJ9SgYJJPi93M8pSyER3wjqOaKm7DyfzUKTl3Sp/EiXGlkczV3xMTqqwdq8h1KopDu+zNxP+8TobxTTgROs2Qa7ZYFGeSYEJmf5O+MJyhHDtCmRHuVsKG1FCGLp2iCyFYfnmVNKuV4LJSvb8q10geRwFO4QwuIIBrqMEd1KEBDAbwDK/w5knvxXv3Phata14+cwJ/4H3+AFRyjbg=</latexit>

µ
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="cVFKnBsGJxj1VA8ZpCa2DOnYoC0=">AAAB8nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPppB06mYSZG6GEfoYbF4q49Wvc+TdO2iy09cDA4Zx7mXNPkEhh0HW/ndLG5tb2Tnm3srd/cHhUPT7pmDjVjLdZLGPdC6jhUijeRoGS9xLNaRRI3g2md7nffeLaiFg94izhfkTHSoSCUbRSfxBRnAjMRDgfVmtu3V2ArBOvIDUo0BpWvwajmKURV8gkNabvuQn6GdUomOTzyiA1PKFsSse8b6miETd+tog8JxdWGZEw1vYpJAv190ZGI2NmUWAn84hm1cvF/7x+iuGtnwmVpMgVW34UppJgTPL7yUhozlDOLKFMC5uVsAnVlKFtqWJL8FZPXiedRt27qjcermtNUtRRhjM4h0vw4AaacA8taAODGJ7hFd4cdF6cd+djOVpyip1T+APn8wfBZpF0</latexit>

⌘
<latexit sha1_base64="s8UhI6OsAnPmUDzfjVa1rVvPHvs=">AAAB63icbVBNS8NAEN3Ur1q/qh69LBbBU0mqoMeCF48V7Ae0oWy2k3bp7ibsToQS+he8eFDEq3/Im//GpM1BWx8MPN6bYWZeEEth0XW/ndLG5tb2Tnm3srd/cHhUPT7p2CgxHNo8kpHpBcyCFBraKFBCLzbAVCChG0zvcr/7BMaKSD/iLAZfsbEWoeAMc2kAyIbVmlt3F6DrxCtIjRRoDatfg1HEEwUauWTW9j03Rj9lBgWXMK8MEgsx41M2hn5GNVNg/XRx65xeZMqIhpHJSiNdqL8nUqasnakg61QMJ3bVy8X/vH6C4a2fCh0nCJovF4WJpBjR/HE6EgY4yllGGDciu5XyCTOMYxZPJQvBW315nXQade+q3ni4rjVpEUeZnJFzckk8ckOa5J60SJtwMiHP5JW8Ocp5cd6dj2VrySlmTskfOJ8//+eOGg==</latexit>

1(2
<latexit sha1_base64="YjziHtzyc9phwA3VBfgdXl0HLRw=">AAACDHicbVC7TgMxEPSFVwivACWNIUGiiu6OAspINJRBIg8pF0V7ji+xYvss24cURfkAGn6FhgKEaPkAOv4G51FAwlqWxjOzWu/EijNjff/by62tb2xu5bcLO7t7+wfFw6OGSTNNaJ2kPNWtGAzlTNK6ZZbTltIURMxpMx7eTPXmA9WGpfLejhTtCOhLljAC1lHdYqkcDUEp6AbRqTsi45YJULPHXAjLzuVX/FnhVRAsQAktqtYtfkW9lGSCSks4GNMOfGU7Y9CWEU4nhSgzVAEZQp+2HZQgqOmMZ8tM8LljejhJtbvS4hn7u2MMwpiRiJ1TgB2YZW1K/qe1M5tcd8ZMqsxSSeaDkoxjm+JpMrjHNCWWjxwAopn7KyYD0ECsy6/gQgiWV14FjbASXFbCu7BUxYs48ugEnaELFKArVEW3qIbqiKBH9Ixe0Zv35L14797H3JrzFj3H6E95nz93upnd</latexit>

!

!⌫
<latexit sha1_base64="DMxX7gVzGIigZN7Rxx9E/FS0dwY=">AAAB7XicbVDLSgNBEOz1GeMr6kXwMhoET2E3CnoMePEYwTwgWcLsZDYZMzuzzEMIS/7BiwdFvPo/3vwbJ8keNLGgoajqprsrSjnTxve/vZXVtfWNzcJWcXtnd2+/dHDY1NIqQhtEcqnaEdaUM0EbhhlO26miOIk4bUWj26nfeqJKMykezDilYYIHgsWMYOOkZnY66QrbK5X9ij8DWiZBTsqQo94rfXX7ktiECkM41roT+KkJM6wMI5xOil2raYrJCA9ox1GBE6rDbHbtBJ07pY9iqVwJg2bq74kMJ1qPk8h1JtgM9aI3Ff/zOtbEN2HGRGoNFWS+KLYcGYmmr6M+U5QYPnYEE8XcrYgMscLEuICKLoRg8eVl0qxWgstK9f6qXDvO4yjACZzBBQRwDTW4gzo0gMAjPMMrvHnSe/HevY9564qXzxzBH3ifP3Cxjug=</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?


<latexit sha1_base64="GpUah58jeuTgVaqvPNlg/vXfUGE=">AAAB7XicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJmdnaYmRXCkn/w4kERr/6PN//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7I5RKeyVyn7Fn4OskiAnZchR75W+uv2EpjGTlgo0phP4yoYZasupYNNiNzVMIR3jkHUclRgzE2bza6fk3Cl9Mki0K2nJXP09kWFszCSOXGeMdmSWvZn4n9dJ7eAmzLhUqWWSLhYNUkFsQmavkz7XjFoxcQSp5u5WQkeokVoXUNGFECy/vEqa1UpwWaneX5VrJI+jAKdwBhcQwDXU4A7q0AAKj/AMr/DmJd6L9+59LFrXvHzmBP7A+/wBjUCPAQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C

{n}
<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

-


<latexit sha1_base64="GpUah58jeuTgVaqvPNlg/vXfUGE=">AAAB7XicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWME84BkCb2TSTJmdnaYmRXCkn/w4kERr/6PN//GSbIHTSxoKKq66e6KlODG+v63t7a+sbm1Xdgp7u7tHxyWjo6bJkk1ZQ2aiES3IzRMcMkallvB2kozjCPBWtH4dua3npg2PJEPdqJYGONQ8gGnaJ3U7I5RKeyVyn7Fn4OskiAnZchR75W+uv2EpjGTlgo0phP4yoYZasupYNNiNzVMIR3jkHUclRgzE2bza6fk3Cl9Mki0K2nJXP09kWFszCSOXGeMdmSWvZn4n9dJ7eAmzLhUqWWSLhYNUkFsQmavkz7XjFoxcQSp5u5WQkeokVoXUNGFECy/vEqa1UpwWaneX5VrJI+jAKdwBhcQwDXU4A7q0AAKj/AMr/DmJd6L9+59LFrXvHzmBP7A+/wBjUCPAQ==</latexit>

Cell
<latexit sha1_base64="pvkIJE+mxvfQnxaTk5CI5LL3S8Q=">AAAB9HicbVDLSgMxFL1TX7W+qm4EN8EiuCozVdBloRuXFewD2qFk0kwbmmTGJFMoQ7/DjQtF3Pox7vwbM+0stPVA4HDOvdyTE8ScaeO6305hY3Nre6e4W9rbPzg8Kh+ftHWUKEJbJOKR6gZYU84kbRlmOO3GimIRcNoJJo3M70yp0iySj2YWU1/gkWQhI9hYye8LbMZKpA3K+XxQrrhVdwG0TrycVCBHc1D+6g8jkggqDeFY657nxsZPsTKMcDov9RNNY0wmeER7lkosqPbTReg5urTKEIWRsk8atFB/b6RYaD0TgZ3MQupVLxP/83qJCe/8lMk4MVSS5aEw4chEKGsADZmixPCZJZgoZrMiMsYKE2N7KtkSvNUvr5N2repdV2sPN5X6WV5HEc7hAq7Ag1uowz00oQUEnuAZXuHNmTovzrvzsRwtOPnOKfyB8/kDIXKSMw==</latexit>

Figure 6 Connection of edges

by G : Λ → Γ where Λ and Γ are the set of open incoming ports and outgoing ports
respectively. They are also called the incoming and outgoing interfaces.
Ports are typed (θ ::= ν | κ), with either linear types ν ::= Int | Unit | κ ⊸
κ or qualified types κ ::= !ν | Cell. We also denote qualified base types as η ::=
!Int | !Unit | !Cell. Adjacent ports have the same types, to be coherent with the wire
homeomorphism.
We often refer to a node using their labels, for example, we say a λ-node for a
node labelled by λ. Some labels are used to indicate nodes that interpret calculus
constructs: λ-node (abstraction), @-node (application), n-node (constants), s-node
(step), p-node (peek), d -node (dereference), r -node (root dependency), m-node
(memory cell creation), $-node (arithmetic operations), if-node (conditionals), µ-node
(recursion), a-node (assignment) and l -node (link). Some nodes do not correspond to
a syntactic construct but are created at runtime to represent dataflow graphs: {n}-node
(memory cell). Finally the !-node, ?-node and C -node (contraction) are markers used
to guide sub-graph copying. These infrastructure nodes are conceptually derived from
linear logic and the Geometry of Interaction (GoI) interpretation of proofs in linear
logic, particularly as used in abstract token machines for GoI. The connection of edges
via nodes must satisfies the typings in figure 6.
When drawing graphs, certain diagrammatic conventions are employed.
…
…
Ports are not represented explicitly and
=
= …
=
…
…
their labels are only shown when they
…
are not obvious. An edge with a bar at its
Figure 7 Drawing conventions
tail represents zero or more ports, while
a double-stroke edge represents a bunch
of the same nodes and ports in parallel (figure 7).
We first define the translation from type judgement of a term to graphs in figure 8
with op any unary and op′ any binary operator. The rules essentially construct the
abstract syntax graph in the way discussed earlier: joining free-variable ports via
contractions, looping free-variable back to the binders, inserting boxes around valuesub-graphs, adding linear logic token management nodes (!, ?). Note that all operations
are eta-expanded, so, for example, instead of having just a + node in the graph we
have a sub-graph corresponding to λx.λ y.x + y . Finally, the C node with no in-ports is

12: 10

## PDF page 11

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

0

[[ , x : ⌧ ` u : ⌧ ]]

JΓ ⊢ λx.u : τ → τ′ K =

[[ ` t0 : ⌧ ! ⌧ 0 ]]

JΓ ⊢ t ′ t : τ′ K =

<latexit sha1_base64="NbFxI0ly1mITswHhFRyAMxsDvgI=">AAACD3icbVDLSsNAFJ3UV42vqhvBzdTiYyElqYLiquBClwq2FpJQbibTduhMEmYmYin+gRt/xY0LRdy6deffOK1ZqPXAhTPn3Mvce8KUM6Ud59MqTE3PzM4V5+2FxaXlldLqWlMlmSS0QRKeyFYIinIW04ZmmtNWKimIkNPrsH868q9vqFQsia/0IKWBgG7MOoyANlK7tOP5ZQ/b/hkIAfu3J76GzL+JQPVwNn7s2oFfDtqlilN1xsCTxM1JBeW4aJc+/CghmaCxJhyU8lwn1cEQpGaE0zvbzxRNgfShSz1DYxBUBcPxPXd42ygR7iTSVKzxWP05MQSh1ECEplOA7qm/3kj8z/My3TkOhixOM01j8v1RJ+NYJ3gUDo6YpETzgSFAJDO7YtIDCUSbCG0Tgvv35EnSrFXdg2rt8rBS38jjKKJNtIX2kIuOUB2dowvUQATdo0f0jF6sB+vJerXevlsLVj6zjn7Bev8Ct02acA==</latexit>

[[ ` t : ⌧ ]]

<latexit sha1_base64="l9zbQEYZWImbfE6OMm0zP9yULV4=">AAACGHicbVDLSgNBEJz1GddX1IvgZTSInuJuFBRPggc9RjAq7C6hdzJJhszsLjO9kRDyGV78FS8eFPHqzb9x8jj4KmioqepmuivOpDDoeZ/O1PTM7Nx8YcFdXFpeWS2urd+YNNeM11gqU30Xg+FSJLyGAiW/yzQHFUt+G3fOh/5tl2sj0uQaexmPFLQS0RQM0Er14kEQbgfUDS9AKQi7DTBtinunIUIeatFqI2id3g+fe24Ubkf1YskreyPQv8SfkBKZoFovfoSNlOWKJ8gkGBP4XoZRHzQKJvnADXPDM2AdaPHA0gQUN1F/dNiA7lqlQZuptpUgHanfJ/qgjOmp2HYqwLb57Q3F/7wgx+ZJ1BdJliNP2PijZi4ppnSYEm0IzRnKniXAtLC7UtYGDQxtlq4Nwf998l9yUyn7h+XK1VHpbHMSR4FskR2yT3xyTM7IJamSGmHkgTyRF/LqPDrPzpvzPm6dciYzG+QHnI8vhrOetw==</latexit>

<latexit sha1_base64="dKlfGs4Mzs79L2u51/rWMz8JchY=">AAACB3icbVBNS8NAEN34WeNX1IsgyNYieCpJFRRPBQ96VLBaSEKZbLft4m4SdidCKd68+Fe8eFDEq3/Bm//Gbe1Bqw8GHu/NMDMvyaUw6PufztT0zOzcfGnBXVxaXln11tavTFZoxhssk5luJmC4FClvoEDJm7nmoBLJr5Obk6F/fcu1EVl6if2cxwq6qegIBmillrcdRuWQutEpKAXRbRtMj+JxhFC4cVSOW17Fr/oj0L8kGJMKGeO85X1E7YwViqfIJBgTBn6O8QA0Cib5nRsVhufAbqDLQ0tTUNzEg9Efd3TXKm3aybStFOlI/TkxAGVMXyW2UwH2zKQ3FP/zwgI7R/FApHmBPGXfizqFpJjRYSi0LTRnKPuWANPC3kpZDzQwtNG5NoRg8uW/5KpWDfartYuDSn1zHEeJbJEdskcCckjq5IyckwZh5J48kmfy4jw4T86r8/bdOuWMZzbILzjvXyctl3Q=</latexit>

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

@

!

<latexit sha1_base64="EODeSM1dpGiTeNlPbex3j3ELD5U=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipWR+UK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AiG2Mpg==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

[[ , f : ⌧ ! ⌧ 0 ` t : ⌧ ! ⌧ 0 ]]
<latexit sha1_base64="MT2TFy2rz2iDNfErCXzjeWF2FAw=">AAACIHicbVBNS8NAEN34WeNX1YvgZWsRPUhJVKh4EjzoUcGqkIQy2W7s4m4SdieFUvpTvPhXvHhQRG/6a9zWHurHg2Ee782wOy/OpTDoeR/OxOTU9Mxsac6dX1hcWi6vrF6ZrNCMN1gmM30Tg+FSpLyBAiW/yTUHFUt+Hd+dDPzrDtdGZOkldnMeKbhNRSIYoJWa5XoQVgLqhqegFOwmRyFCEWI2aNthpwWmTZEe0XHZjcJK1CxXvZo3BP1L/BGpkhHOm+X3sJWxQvEUmQRjAt/LMeqBRsEk77thYXgO7A5ueWBpCoqbqDc8sE+3rNKiSaZtpUiH6vhGD5QxXRXbSQXYNr+9gfifFxSYHEY9keYF8pR9P5QUkmJGB2nRltCcoexaAkwL+1fK2qCBoc3UtSH4v0/+S672av5+be/ioHq8PoqjRDbIJtkhPqmTY3JGzkmDMHJPHskzeXEenCfn1Xn7Hp1wRjtr5Aeczy+FlaE4</latexit>

JΓ , f : τ → τ′ ⊢ rec f .t : τ → τ′ K =

<latexit sha1_base64="JfNhHDmiXWSkW51tt1a0oYAngQE=">AAAB6nicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWNE84BkCbOT2WTIzOwy0yuEkE/w4kERr36RN//GSbIHTSxoKKq66e6KUiks+v63t7a+sbm1Xdgp7u7tHxyWjo6bNskM4w2WyMS0I2q5FJo3UKDk7dRwqiLJW9Hodua3nrixItGPOE55qOhAi1gwik566KqsVyr7FX8OskqCnJQhR71X+ur2E5YprpFJam0n8FMMJ9SgYJJPi93M8pSyER3wjqOaKm7DyfzUKTl3Sp/EiXGlkczV3xMTqqwdq8h1KopDu+zNxP+8TobxTTgROs2Qa7ZYFGeSYEJmf5O+MJyhHDtCmRHuVsKG1FCGLp2iCyFYfnmVNKuV4LJSvb8q10geRwFO4QwuIIBrqMEd1KEBDAbwDK/w5knvxXv3Phata14+cwJ/4H3+AFRyjbg=</latexit>

JΓ , x : τ ⊢ x : τK = C

µ
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

!

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

JΓ ⊢ if u then t 1 else t 2 : γK =

[[ ` u : Int]]

C

[[ ` t1 : ]]

<latexit sha1_base64="8hh2NUS3d/VTUzBE0UaxqJMoy2Q=">AAACEXicbVC7SgNBFJ2Nr7i+ojaCzWgQrMKuCopVwELtIpgH7C7h7mSSDJmZXWZmhbDkF2z8FRsLRWzt7PwbJ4/C14ELh3Pu5d574pQzbTzv0ynMzS8sLhWX3ZXVtfWN0uZWQyeZIrROEp6oVgyaciZp3TDDaStVFETMaTMeXIz95h1VmiXy1gxTGgnoSdZlBIyV2qXDINwLsBteghAQ3nVA93GGz3EowPSVyK+lGblRuBe1S2Wv4k2A/xJ/Rspohlq79BF2EpIJKg3hoHXge6mJclCGEU5HbphpmgIZQI8GlkoQVEf55KMRPrBKB3cTZUsaPFG/T+QgtB6K2HaOD9W/vbH4nxdkpnsW5UymmaGSTBd1M45Ngsfx4A5TlBg+tASIYvZWTPqggBgbomtD8H+//Jc0jir+ceXo5qRc3ZnFUUS7aB8dIh+doiq6QjVURwTdo0f0jF6cB+fJeXXepq0FZzazjX7Aef8Ckdibew==</latexit>

[[ ` t2 : ]]

<latexit sha1_base64="3wOe4Sll1MKrc9Htw+oy6VZqTKc=">AAACDXicbVDLSsNAFJ3UV42vqBvBzdQquCpJFRRXBRe6rGAfkIRyM522Q2eSMDMplNIfcOOvuHGhiFv37vwbp4+FVg9cOJxzL/feE6WcKe26X1ZuaXlldS2/bm9sbm3vOLt7dZVkktAaSXgimxEoyllMa5ppTpuppCAiThtR/3riNwZUKpbE93qY0lBAN2YdRkAbqeUc+0HBx3ZwA0JAMGiD6mHd8vAVDroTyQ6DQthyim7JnQL/Jd6cFNEc1ZbzGbQTkgkaa8JBKd9zUx2OQGpGOB3bQaZoCqQPXeobGoOgKhxNvxnjE6O0cSeRpmKNp+rPiREIpYYiMp0CdE8tehPxP8/PdOcyHLE4zTSNyWxRJ+NYJ3gSDW4zSYnmQ0OASGZuxaQHEog2AdomBG/x5b+kXi55Z6Xy3XmxcjCPI48O0RE6RR66QBV0i6qohgh6QE/oBb1aj9az9Wa9z1pz1nxmH/2C9fENlVWZOQ==</latexit>

<latexit sha1_base64="nHiToQFqi/CJHOS/uvlIlNjYz/k=">AAACDXicbVDLSsNAFJ3UV42vqBvBzdQquCpJFRRXBRe6rGAfkIRyM522Q2eSMDMplNIfcOOvuHGhiFv37vwbp4+FVg9cOJxzL/feE6WcKe26X1ZuaXlldS2/bm9sbm3vOLt7dZVkktAaSXgimxEoyllMa5ppTpuppCAiThtR/3riNwZUKpbE93qY0lBAN2YdRkAbqeUc+0HBx3ZwA0JAMGiD6mHdKuMrHHQnkh0GhbDlFN2SOwX+S7w5KaI5qi3nM2gnJBM01oSDUr7npjocgdSMcDq2g0zRFEgfutQ3NAZBVTiafjPGJ0Zp404iTcUaT9WfEyMQSg1FZDoF6J5a9Cbif56f6c5lOGJxmmkak9miTsaxTvAkGtxmkhLNh4YAkczcikkPJBBtArRNCN7iy39JvVzyzkrlu/Ni5WAeRx4doiN0ijx0gSroFlVRDRH0gJ7QC3q1Hq1n6816n7XmrPnMPvoF6+MblueZOg==</latexit>

JΓ ⊢ n : IntK =

<latexit sha1_base64="qwmkCCdWplvKEzFyiMtXfVPNC8U=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmEsRvWG23QXwOvEK0kDleiM6l9+lFKTgNCUE6WGnpvpICdSM8phXvONgozQKRnD0FJBElBBvrh5ji+sEuE4lfYJjRfq70ROEqVmSWgnE6InatUrxP+8odHxbZAzkRkNgi4XxYZjneKiABwxCVTzmSWESmZvxXRCJKHa1lSzJXirX14nvVbTu2q2Hq4bbVzWUUVn6BxdIg/doDa6Rx3URRRl6Bm9ojfHOC/Ou/OxHK04ZeYU/YHz+QPzxpGE</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

n

C
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

if

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

<latexit sha1_base64="e1XGP/Y0qUFcDG4XC3AO7SSqWYg=">AAAB/nicbVC7SgNBFJ2NrxhfUUubwSBYSNiNhXYGbCyjmAckS5idnU2GzGOZmRWWJWBnY6ufYCe2/oq9YOMP2Dl5FCbxwIXDOfdy7z1BzKg2rvvh5JaWV1bX8uuFjc2t7Z3i7l5Dy0RhUseSSdUKkCaMClI31DDSihVBPGCkGQwuR37zjihNpbg1aUx8jnqCRhQjY6UbGXeLJbfsjgEXiTclpYufB/p98klq3eJXJ5Q44UQYzJDWbc+NjZ8hZShmZFjoJJrECA9Qj7QtFYgT7WfjS4fwyCohjKSyJQwcq38nMsS1TnlgOzkyfT3vjcT/vHZionM/oyJODBF4sihKGDQSjt6GIVUEG5ZagrCi9laI+0ghbGw4M1u04UilKhzaZLz5HBZJo1L2TsuVa7dUhWCCPDgAh+AYeOAMVMEVqIE6wCACj+AJPDv3zovz6rxNWnPOdGYfzMB5/wU2rJs1</latexit>

op

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

JΓ ⊢ op : τK =

<latexit sha1_base64="e1XGP/Y0qUFcDG4XC3AO7SSqWYg=">AAAB/nicbVC7SgNBFJ2NrxhfUUubwSBYSNiNhXYGbCyjmAckS5idnU2GzGOZmRWWJWBnY6ufYCe2/oq9YOMP2Dl5FCbxwIXDOfdy7z1BzKg2rvvh5JaWV1bX8uuFjc2t7Z3i7l5Dy0RhUseSSdUKkCaMClI31DDSihVBPGCkGQwuR37zjihNpbg1aUx8jnqCRhQjY6UbGXeLJbfsjgEXiTclpYufB/p98klq3eJXJ5Q44UQYzJDWbc+NjZ8hZShmZFjoJJrECA9Qj7QtFYgT7WfjS4fwyCohjKSyJQwcq38nMsS1TnlgOzkyfT3vjcT/vHZionM/oyJODBF4sihKGDQSjt6GIVUEG5ZagrCi9laI+0ghbGw4M1u04UilKhzaZLz5HBZJo1L2TsuVa7dUhWCCPDgAh+AYeOAMVMEVqIE6wCACj+AJPDv3zovz6rxNWnPOdGYfzMB5/wU2rJs1</latexit>

op

JΓ ⊢ op′ : τK =

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

Figure 8

C

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

Representation of terms

the degenerate contraction (usually referred to as ‘weakening’) used to mark unused
variables in a subterm.
3.3 Machine states

As explained, the machine execution is given by an evaluation token traversing the
graph and rewriting it. To manage the process the machine also uses data, as defined
below. We call this data ‘evaluation token data’ as it can be thought of as data carried
by the token.

12: 11

## PDF page 12

Transparent Synchronous Dataflow

Definition 3.1 (Evaluation tokens). For any graph G , the state of an evaluation token
(e, d, f , S, B) consists of a port e ∈ PortG indicating the token position, a direction d, a
rewrite flag f, a computation stack S and a box stack B with
d ::= ↑ | ↓
f ::= □ | @ | if | C | ! | µ | m | p | l(i) | a(n, i) | r(i) | sp | s
S ::= □ | ⋆ : S | (λ, −) : S | (n, −) : S | (n, g) : S | (n, i) : S | ((), −) : S | if0 : S | if1 : S
B ::= □ | i : B

where i ∈ PortG .
In the definition above e denotes the current position of the token. The rewrite flag
determines the possible graph rewriting. The computation stack tracks the intermediate
results of the evaluation and the box stack tracks duplication of values. Together the
two stacks guide the transition of token. In particular the token asks the value of a
graph by having ⋆ : S as its computation stack. After traversing the graph it could
return either (λ, −) : S , (n, r) : S or ((), −) : S . The first part (λ,n,()) is the return value
while the second part indicates whether it is a cell (i ∈ PortG with i denoting the
in-port of the cell), a graph ( g ) or a normal value (−).
Definition 3.2 (Machine states). A machine state (G, δ, P) is a triplet consisting of
a graph G , an eval token δ (hereinafter referred to as the main token) and a set of
eval tokens P (hereinafter referred to as the set of prop tokens) that are used during
propagation.
We define a binary relation on machine states called transitions (G, δ, P) 7→ (G ′ , δ′ , P ′ )
which includes normal pass and rewrite transitions. We group the transitions into
pass transitions in which only the token changes, and rewrite transitions in which the
underlying graph may change.
3.4 Pass rules

The pass transitions are given in table 1. The token is at a distinguished port in the graph and the node column represents the
label of one of the two nodes of the port. The second column (‘e’)
represents whether it is an incoming (i ) or an outgoing (o) port.
We labelled the ports by its left-to-right order from zero as in figure 9. The next three columns represent the state of the direction
d , flag f , and stack S . The next column represents the new port e
visited by the token, relative to the node. The final three columns
represent the new values of the direction, flag, and stack.

<latexit sha1_base64="Ze4kDaDm69l4CoDsBpwEJVorWm8=">AAAB6nicbVBNS8NAEJ3Ur1q/qh69LBbBU0lqQY8FLx4r2g9oQ9lsJ+3SzSbsboQS+hO8eFDEq7/Im//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ7dzvPKHSPJaPZpqgH9GR5CFn1FjpgQ/cQbniVt0FyDrxclKBHM1B+as/jFkaoTRMUK17npsYP6PKcCZwVuqnGhPKJnSEPUsljVD72eLUGbmwypCEsbIlDVmovycyGmk9jQLbGVEz1qveXPzP66UmvPEzLpPUoGTLRWEqiInJ/G8y5AqZEVNLKFPc3krYmCrKjE2nZEPwVl9eJ+1a1buq1u7rlQbJ4yjCGZzDJXhwDQ24gya0gMEInuEV3hzhvDjvzseyteDkM6fwB87nD+pXjXI=</latexit>

i0

o0
<latexit sha1_base64="UjA12Zk0y4GrYma4Gb+SQSLhizY=">AAAB6nicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWNE84BkCbOT3mTI7MwyMyuEkE/w4kERr36RN//GSbIHTSxoKKq66e6KUsGN9f1vb219Y3Nru7BT3N3bPzgsHR03jco0wwZTQul2RA0KLrFhuRXYTjXSJBLYika3M7/1hNpwJR/tOMUwoQPJY86oddKD6vm9Utmv+HOQVRLkpAw56r3SV7evWJagtExQYzqBn9pwQrXlTOC02M0MppSN6AA7jkqaoAkn81On5NwpfRIr7UpaMld/T0xoYsw4iVxnQu3QLHsz8T+vk9n4JpxwmWYWJVssijNBrCKzv0mfa2RWjB2hTHN3K2FDqimzLp2iCyFYfnmVNKuV4LJSvb8q10geRwFO4QwuIIBrqMEd1KEBDAbwDK/w5gnvxXv3Phata14+cwJ/4H3+APN7jXg=</latexit>

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

<latexit sha1_base64="IGlUiIdBOLkdJXsOaEyDQg/cKio=">AAAB6nicbVBNS8NAEJ3Ur1q/qh69LBbBU0lqQY8FLx4r2g9oQ9lsJ+3SzSbsboQS+hO8eFDEq7/Im//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ7dzvPKHSPJaPZpqgH9GR5CFn1FjpgQ+8QbniVt0FyDrxclKBHM1B+as/jFkaoTRMUK17npsYP6PKcCZwVuqnGhPKJnSEPUsljVD72eLUGbmwypCEsbIlDVmovycyGmk9jQLbGVEz1qveXPzP66UmvPEzLpPUoGTLRWEqiInJ/G8y5AqZEVNLKFPc3krYmCrKjE2nZEPwVl9eJ+1a1buq1u7rlQbJ4yjCGZzDJXhwDQ24gya0gMEInuEV3hzhvDjvzseyteDkM6fwB87nD+vbjXM=</latexit>

i1

Figure 9

Node λ: If the token is at the first incoming port i1 of a λ node travelling along the

direction of the edge d =↑ the token will reverse directions d =↓ and the top of
the stack will be replaced by information that a λ node has been encountered by
placing (λ, −) at the top. For reasons of well-formedness a ⋆ must have been at
that op of S . This rule reflects the fact that a λ-term is a value which requires no
further evaluation.

12: 12

## PDF page 13

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
Node @: If the token reaches the sole incoming port i0 of an application node it will

pass through and move to its first outgoing port o1 (right out-port), reflecting the
right-to-left call-by-value evaluation. As it returns d =↓ along the same port o1 it is
passed to the zeroth outgoing port o0 (left out-port) with changed direction d =↑
and the top of the stack become ⋆. Finally as it returns d =↓ on the same port it
is passed to the incoming port i0 with d =↓ in preparation for the rewrite corresponding to application. Node that it is expected that the last value encountered
on the left side was a lambda term, since the rule expects (λ, −) at the top. The
imminence of the rewrite rule is indicated by the rewrite flag f = @.
Nodes n, (): These nodes represent values so their behaviour is quite similar to that of
the λ node, reflecting the token and placing the value on S .
Operation nodes These nodes behave similarly to @. Incoming-port tokens are propagated to the outgoing port(s). When they come back along the outgoing port the
behaviour is different according to whether they are unary or binary operators. If
they are unary the token is passed to the incoming port and the rewrite flag f is
used to indicate an imminent rewrite. If they are binary then the second outgoing
port is visited first.
Node if : This node behaves like a ternary operator, except that after returning from
the first outgoing edge the top of the stack is inspected.
Node µ: The recursion node immediately prepares the machine for a rewrite by
changing the flag to f = µ.
Node !: This node, also found in conventional GOI abstract machines, indicates that a
box is about to be processed. The rewrite rule about to be triggered is indicated by
the flag becoming f = !.
Node {n}: The cell storing value n is dealt with almost as a standard integer value.
The only difference is that the port io is also placed on top of S along with the value
n, to be possibly used by datflow graph operations.
Node C : Contraction nodes use the other stack, the box-stack, to remember along
which of the several incoming ports a token arrived so that it can return to the
same port. Moreover, the incoming port prepares a rewrite f = C , essentially the
copying of the shared term (represented as a subgraph).
Note that certain nodes, such as ?, have no associated rules because the token is never
supposed to reach them.
3.5 Rewrite rules

The pass rules only serve to set the scene for the rewrite transitions, which are given
in figure 10.
The Beta rule: The essential computational rule of the lambda calculus is the removal

of the abstraction-application pair. The second outgoing port of the application
node @ is connected to the argument, which is now re-wired to the first argument
of the subgraph G representing the function body. This is a ‘small’ beta law since

12: 13

## PDF page 14

Transparent Synchronous Dataflow

Table 1 Pass transitions

node

e

d

f

S

e

d

f

S

λ
@
@
@

i1
i0
o1
o0

↑
↑
↓
↓

□
□
□
□

⋆:S
S
X:S
(λ, −):S

i1
o1
o0
i0

↓
↑
↑
↑

□
□
□
@

(λ, −):S
S
⋆:S
⋆:S

n
()

i0
i0

↑
↑

□
□

⋆:S
⋆:S

i0
i0

↓
↓

□
□

(n, −):S
((), −):S

o0
i0
i0
i0

↑
↓
↓
↓

□
p
r(i)
m

S
(n, −):S
(n, −):S
(n, −):S

7→

For ω ∈ p, d, r, m (unary operations):
ω
p
r
m

i0
o0
o0
o0

↑
↓
↓
↓

S
(n, x):S
(n, i):S
(n, x):S

□
□
□
□

For # ∈ $ ∪ a, l (binary operations):
#
#
$
a
l

i0
o1
o0
o0
o0

↑
↓
↓
↓
↓

□
□
□
□
□

S
S
(m, −) : (n, −):S
(m, i) : (n, x):S
(m, i) : (n, x):S

o1
o0
i0
i0
i0

↑
↑
↓
↓
↓

□
□
$
a(n, i)
l(i)

S
⋆:S
($ m n, −):S
((), −):S
((), −):S

if
if
if
if

i0
o0
o0
o1

↑
↓
↓
↓

□
□
□
□

S
(0, −):S
(n ̸= 0, −):S
S

o0
o1
o2
o2

↑
↑
↑
↑

□
if
if
□

S
⋆:S
⋆:S
⋆:S

µ

i1

↑

□

S

i1

↑

µ

S

!
!

i0
o0

↑
↓

□
□

S
S

o0
i0

↑
↓

!
□

S
S

{n}

i0

↑

□

⋆:S

i0

↓

□

(n, i0 ):S

where x ∈ {−, g}
node

e

d

f

S

B

C
C

ik
o0

↑
↓

□
□

S
S

B
ik :B

12: 14

7→

e

d

f

S

B

o0
ik

↑
↓

C
□

S
S

ik :B
B

## PDF page 15

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

?

G

<latexit sha1_base64="LJnd+eo6OtQBwC7fkd492FwL+Ns=">AAAB7nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPJTTt0MgkzE6GEfoQbF4q49Xvc+TdO2yy09cDA4ZxzmXtPkAqujet+O6WNza3tnfJuZW//4PCoenzS0UmmGLZZIhLVC6hGwSW2DTcCe6lCGgcCu8Hkbu53n1BpnshHM03Rj+lI8ogzaqzUHQgbDemwWnPr7gJknXgFqUGB1rD6NQgTlsUoDRNU677npsbPqTKcCZxVBpnGlLIJHWHfUklj1H6+WHdGLqwSkihR9klDFurviZzGWk/jwCZjasZ61ZuL/3n9zES3fs5lmhmUbPlRlAliEjK/nYRcITNiagllittdCRtTRZmxDVVsCd7qyeuk06h7V/XGw3WtSYo6ynAG53AJHtxAE+6hBW1gMIFneIU3J3VenHfnYxktOcXMKfyB8/kDM9mPXw==</latexit>

G

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

Beta

@
<latexit sha1_base64="5Lioeg7oXuHwoO2nzXijjcpCTqw=">AAAB+XicbVDLSgMxFL1TX7W+Rt0IboJFcFHKTBV0WXTjsqJ9QDuUTJppQzOZIcm0lKF/4saFIm79E3f+jWk7C209cOFwzr3JvcePOVPacb6t3Nr6xuZWfruws7u3f2AfHjVUlEhC6yTikWz5WFHOBK1rpjltxZLi0Oe06Q/vZn5zRKVikXjSk5h6Ie4LFjCCtZG6tt3pRWOBpYzGpWrpsXTbtYtO2ZkDrRI3I0XIUOvaX+YJkoRUaMKxUm3XibWXYqkZ4XRa6CSKxpgMcZ+2DRU4pMpL55tP0blReiiIpCmh0Vz9PZHiUKlJ6JvOEOuBWvZm4n9eO9HBjZcyESeaCrL4KEg40hGaxYB6TFKi+cQQTCQzuyIywBITbcIqmBDc5ZNXSaNSdi/LlYerYvUkiyMPp3AGF+DCNVThHmpQBwIjeIZXeLNS68V6tz4WrTkrmzmGP7A+fwBxOpK9</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="cVFKnBsGJxj1VA8ZpCa2DOnYoC0=">AAAB8nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPppB06mYSZG6GEfoYbF4q49Wvc+TdO2iy09cDA4Zx7mXNPkEhh0HW/ndLG5tb2Tnm3srd/cHhUPT7pmDjVjLdZLGPdC6jhUijeRoGS9xLNaRRI3g2md7nffeLaiFg94izhfkTHSoSCUbRSfxBRnAjMRDgfVmtu3V2ArBOvIDUo0BpWvwajmKURV8gkNabvuQn6GdUomOTzyiA1PKFsSse8b6miETd+tog8JxdWGZEw1vYpJAv190ZGI2NmUWAn84hm1cvF/7x+iuGtnwmVpMgVW34UppJgTPL7yUhozlDOLKFMC5uVsAnVlKFtqWJL8FZPXiedRt27qjcermtNUtRRhjM4h0vw4AaacA8taAODGJ7hFd4cdF6cd+djOVpyip1T+APn8wfBZpF0</latexit>

#, @, S, B

<latexit sha1_base64="/d5qYng6uUKikK0I+z7ODsJYulc=">AAAB/XicbVDLSsNAFJ3UV62v+FgIbgaL4KKUpAq6LLpxWdE+oAllMp20QyeZOA+lhuKvuHGhiFv/w51/47TNQlsPXDiccy/33hMkjErlON9WbmFxaXklv1pYW9/Y3LK3dxqSa4FJHXPGRStAkjAak7qiipFWIgiKAkaaweBy7DfviZCUx7dqmBA/Qr2YhhQjZaSOvefpBAnBH0qevNNIkNJN6aJjF52yMwGcJ25GiiBDrWN/eV2OdURihRmSsu06ifJTJBTFjIwKnpYkQXiAeqRtaIwiIv10cv0IHhmlC0MuTMUKTtTfEymKpBxGgemMkOrLWW8s/ue1tQrP/ZTGiVYkxtNFoWZQcTiOAnapIFixoSEIC2puhbiPBMLKBFYwIbizL8+TRqXsnpQr16fF6n4WRx4cgENwDFxwBqrgCtRAHWDwCJ7BK3iznqwX6936mLbmrGxmF/yB9fkD8YyUvw==</latexit>

", ⇤, S, B

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

p

p

<latexit sha1_base64="iPTQc4GWN4Ze5khPiuuvqg80POI=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipmQzKFbfqLkDWiZeTCuRoDMpf/WHM0gilYYJq3fPcxPgZVYYzgbNSP9WYUDahI+xZKmmE2s8Wh87IhVWGJIyVLWnIQv09kdFI62kU2M6ImrFe9ebif14vNeGtn3GZpAYlWy4KU0FMTOZfkyFXyIyYWkKZ4vZWwsZUUWZsNiUbgrf68jpp16reVbXWvK7USR5HEc7gHC7Bgxuowz00oAUMEJ7hFd6cR+fFeXc+lq0FJ585hT9wPn8A0S2M1g==</latexit>

if-n

if

<latexit sha1_base64="EODeSM1dpGiTeNlPbex3j3ELD5U=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipWR+UK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AiG2Mpg==</latexit>

<latexit sha1_base64="49ffBu5PY965TVUI7lpVYb1GN8s=">AAACA3icbVDLSsNAFJ34rPUVdSO6GSyCi1KSKuiy6MZlRfuAppTJdNIOnZmEmYlSQsCNv+LGhSJu/Ql3/o2TNgttPXDhcM693HuPHzGqtON8WwuLS8srq4W14vrG5ta2vbPbVGEsMWngkIWy7SNFGBWkoalmpB1JgrjPSMsfXWV+655IRUNxp8cR6XI0EDSgGGkj9ewDL46QlOFDOfE40kPJExqkafm2fNmzS07FmQDOEzcnJZCj3rO/vH6IY06Exgwp1XGdSHcTJDXFjKRFL1YkQniEBqRjqECcqG4y+SGFx0bpwyCUpoSGE/X3RIK4UmPum87sTjXrZeJ/XifWwUU3oSKKNRF4uiiIGdQhzAKBfSoJ1mxsCMKSmlshHiKJsDaxFU0I7uzL86RZrbinlerNWam2n8dRAIfgCJwAF5yDGrgGddAAGDyCZ/AK3qwn68V6tz6mrQtWPrMH/sD6/AEnHJey</latexit>

C

", if, S, B

<latexit sha1_base64="d7+gYvO9MDtHlQL1JdLzCb1Ueyw=">AAAB/3icbVDLSgMxFM3UV62vUUEEN8EiuChlpgq6LLpxWdE+oDOUTJppQzPJmGSUMnbhr7hxoYhbf8Odf2PazkJbD1w4nHMv994TxIwq7TjfVm5hcWl5Jb9aWFvf2Nyyt3caSiQSkzoWTMhWgBRhlJO6ppqRViwJigJGmsHgcuw374lUVPBbPYyJH6EepyHFSBupY+95SYykFA+l1FN3CZJkVLopXXTsolN2JoDzxM1IEWSodewvrytwEhGuMUNKtV0n1n6KpKaYkVHBSxSJER6gHmkbylFElJ9O7h/BI6N0YSikKa7hRP09kaJIqWEUmM4I6b6a9cbif1470eG5n1IeJ5pwPF0UJgxqAcdhwC6VBGs2NARhSc2tEPeRRFibyAomBHf25XnSqJTdk3Ll+rRY3c/iyIMDcAiOgQvOQBVcgRqoAwwewTN4BW/Wk/VivVsf09aclc3sgj+wPn8AxbOVyw==</latexit>

if-z

if

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="cVFKnBsGJxj1VA8ZpCa2DOnYoC0=">AAAB8nicbVDLSsNAFL2pr1pfVZduBovgqiRV0GXBjcsK9gFtKJPppB06mYSZG6GEfoYbF4q49Wvc+TdO2iy09cDA4Zx7mXNPkEhh0HW/ndLG5tb2Tnm3srd/cHhUPT7pmDjVjLdZLGPdC6jhUijeRoGS9xLNaRRI3g2md7nffeLaiFg94izhfkTHSoSCUbRSfxBRnAjMRDgfVmtu3V2ArBOvIDUo0BpWvwajmKURV8gkNabvuQn6GdUomOTzyiA1PKFsSse8b6miETd+tog8JxdWGZEw1vYpJAv190ZGI2NmUWAn84hm1cvF/7x+iuGtnwmVpMgVW34UppJgTPL7yUhozlDOLKFMC5uVsAnVlKFtqWJL8FZPXiedRt27qjcermtNUtRRhjM4h0vw4AaacA8taAODGJ7hFd4cdF6cd+djOVpyip1T+APn8wfBZpF0</latexit>

", ⇤, S, B

<latexit sha1_base64="49ffBu5PY965TVUI7lpVYb1GN8s=">AAACA3icbVDLSsNAFJ34rPUVdSO6GSyCi1KSKuiy6MZlRfuAppTJdNIOnZmEmYlSQsCNv+LGhSJu/Ql3/o2TNgttPXDhcM693HuPHzGqtON8WwuLS8srq4W14vrG5ta2vbPbVGEsMWngkIWy7SNFGBWkoalmpB1JgrjPSMsfXWV+655IRUNxp8cR6XI0EDSgGGkj9ewDL46QlOFDOfE40kPJExqkafm2fNmzS07FmQDOEzcnJZCj3rO/vH6IY06Exgwp1XGdSHcTJDXFjKRFL1YkQniEBqRjqECcqG4y+SGFx0bpwyCUpoSGE/X3RIK4UmPum87sTjXrZeJ/XifWwUU3oSKKNRF4uiiIGdQhzAKBfSoJ1mxsCMKSmlshHiKJsDaxFU0I7uzL86RZrbinlerNWam2n8dRAIfgCJwAF5yDGrgGddAAGDyCZ/AK3qwn68V6tz6mrQtWPrMH/sD6/AEnHJey</latexit>

C

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

", if, S, B

<latexit sha1_base64="d7+gYvO9MDtHlQL1JdLzCb1Ueyw=">AAAB/3icbVDLSgMxFM3UV62vUUEEN8EiuChlpgq6LLpxWdE+oDOUTJppQzPJmGSUMnbhr7hxoYhbf8Odf2PazkJbD1w4nHMv994TxIwq7TjfVm5hcWl5Jb9aWFvf2Nyyt3caSiQSkzoWTMhWgBRhlJO6ppqRViwJigJGmsHgcuw374lUVPBbPYyJH6EepyHFSBupY+95SYykFA+l1FN3CZJkVLopXXTsolN2JoDzxM1IEWSodewvrytwEhGuMUNKtV0n1n6KpKaYkVHBSxSJER6gHmkbylFElJ9O7h/BI6N0YSikKa7hRP09kaJIqWEUmM4I6b6a9cbif1470eG5n1IeJ5pwPF0UJgxqAcdhwC6VBGs2NARhSc2tEPeRRFibyAomBHf25XnSqJTdk3Ll+rRY3c/iyIMDcAiOgQvOQBVcgRqoAwwewTN4BW/Wk/VivVsf09aclc3sgj+wPn8AxbOVyw==</latexit>

", ⇤, S, B

C
<latexit sha1_base64="qwmkCCdWplvKEzFyiMtXfVPNC8U=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmEsRvWG23QXwOvEK0kDleiM6l9+lFKTgNCUE6WGnpvpICdSM8phXvONgozQKRnD0FJBElBBvrh5ji+sEuE4lfYJjRfq70ROEqVmSWgnE6InatUrxP+8odHxbZAzkRkNgi4XxYZjneKiABwxCVTzmSWESmZvxXRCJKHa1lSzJXirX14nvVbTu2q2Hq4bbVzWUUVn6BxdIg/doDa6Rx3URRRl6Bm9ojfHOC/Ou/OxHK04ZeYU/YHz+QPzxpGE</latexit>

n
<latexit sha1_base64="SCiHxsF35CnyMeIpKKgzqwMIS9I=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3a3STsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgkfYMtwI7CYKqQwEdoLJ3dzvPKHSPI4ezDRBX9JRxEPOqLFSUw7KFbfqLkDWiZeTCuRoDMpf/WHMUomRYYJq3fPcxPgZVYYzgbNSP9WYUDahI+xZGlGJ2s8Wh87IhVWGJIyVrciQhfp7IqNS66kMbKekZqxXvbn4n9dLTXjrZzxKUoMRWy4KU0FMTOZfkyFXyIyYWkKZ4vZWwsZUUWZsNiUbgrf68jpp16reVbXWvK7USR5HEc7gHC7Bgxuowz00oAUMEJ7hFd6cR+fFeXc+lq0FJ585hT9wPn8AzKGM0w==</latexit>

m

m

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

n

<latexit sha1_base64="qwmkCCdWplvKEzFyiMtXfVPNC8U=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmEsRvWG23QXwOvEK0kDleiM6l9+lFKTgNCUE6WGnpvpICdSM8phXvONgozQKRnD0FJBElBBvrh5ji+sEuE4lfYJjRfq70ROEqVmSWgnE6InatUrxP+8odHxbZAzkRkNgi4XxYZjneKiABwxCVTzmSWESmZvxXRCJKHa1lSzJXirX14nvVbTu2q2Hq4bbVzWUUVn6BxdIg/doDa6Rx3URRRl6Bm9ojfHOC/Ou/OxHK04ZeYU/YHz+QPzxpGE</latexit>

{n}

s

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

!

<latexit sha1_base64="l7qUFD+Ap+Lm0zOhf0IgfOIR7aE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQflilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/VuYzZ</latexit>

i
#, m, (n, ) : S, B

s

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

<latexit sha1_base64="DBG4Gu6LGAZZbQNs+9xyRN5V8Ss=">AAACC3icbVDLSgMxFM3UV62vqhvBTWgRKtQyUwXFVdGNy4r2Ae1QMmmmDc0kQ5KxlKF7N/6KGxeKuPUH3Pk3pu0stPVA4HDOfeQeL2RUadv+tlJLyyura+n1zMbm1vZOdnevrkQkMalhwYRsekgRRjmpaaoZaYaSoMBjpOENrid+44FIRQW/16OQuAHqcepTjLSROtlcuyuGHEkphsWwWGhHvEvkZBjkRXhyfHlXvOpk83bJngIuEicheZCg2sl+maE4CgjXmCGlWo4dajdGUlPMyDjTjhQJER6gHmkZylFAlBtPbxnDI6N0oS+keVzDqfq7I0aBUqPAM5UB0n01703E/7xWpP0LN6Y8jDTheLbIjxjUAk6CgV0qCdZsZAjCkpq/QtxHEmFt4suYEJz5kxdJvVxyTkvl27N85SCJIw0OQQ4UgAPOQQXcgCqoAQwewTN4BW/Wk/VivVsfs9KUlfTsgz+wPn8An+6ZVQ==</latexit>

#, p, (n, ) : S, B

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="jDsqEvZVH4Kci1LICOI02rmgHUY=">AAACEXicbVBNSwJBGJ61L7Mvq0vQZUgCA5NdC4pOUpeORvkBKjI7vurg7Ow2M5uI+Be69Fe6dCiia7du/ZtmdQ+lPTDw8Dzvx7yPG3CmtG1/W4mFxaXlleRqam19Y3Mrvb1TUX4oKZSpz31Zc4kCzgSUNdMcaoEE4rkcqm7/KvKrDyAV88WdHgbQ9EhXsA6jRBuplc422v5AECn9Qa6h7kMiIZdthKINMhqJRQ4fH13c5i5b6YydtyfA88SJSQbFKLXSX2Y0DT0QmnKiVN2xA90cEakZ5TBONUIFAaF90oW6oYJ4oJqjyUVjfGiUNu740jyh8UT93TEinlJDzzWVHtE9NetF4n9ePdSd8+aIiSDUIOh0USfkWPs4ige3mQSq+dAQQiUzf8W0RySh2oSYMiE4syfPk0oh75zkCzenmeJeHEcS7aMDlEUOOkNFdI1KqIwoekTP6BW9WU/Wi/VufUxLE1bcs4v+wPr8AZ9nnA4=</latexit>

#, ⇤, (n, ) : S, B

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

{n}

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

i

C

<latexit sha1_base64="MspV0S8w6SWzX1LS8spjRy7yJcI=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmGcjOoNt+kugNeJV5IGKtEZ1b/8KKUmAaEpJ0oNPTfTQU6kZpTDvOYbBRmhUzKGoaWCJKCCfHHzHF9YJcJxKu0TGi/U34mcJErNktBOJkRP1KpXiP95Q6Pj2yBnIjMaBF0uig3HOsVFAThiEqjmM0sIlczeiumESEK1ralmS/BWv7xOeq2md9VsPVw32riso4rO0Dm6RB66QW10jzqoiyjK0DN6RW+OcV6cd+djOVpxyswp+gPn8wfyQpGD</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

i

#, ⇤, (n, i) : S, B

C

<latexit sha1_base64="MspV0S8w6SWzX1LS8spjRy7yJcI=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmGcjOoNt+kugNeJV5IGKtEZ1b/8KKUmAaEpJ0oNPTfTQU6kZpTDvOYbBRmhUzKGoaWCJKCCfHHzHF9YJcJxKu0TGi/U34mcJErNktBOJkRP1KpXiP95Q6Pj2yBnIjMaBF0uig3HOsVFAThiEqjmM0sIlczeiumESEK1ralmS/BWv7xOeq2md9VsPVw32riso4rO0Dm6RB66QW10jzqoiyjK0DN6RW+OcV6cd+djOVpxyswp+gPn8wfyQpGD</latexit>

<latexit sha1_base64="rRkN2ss//1CAV35C2NV8177jMZs=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqdnplytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzQ+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjMviYDrpAZMbGEMsXtrYSNqKLM2GxKNgRv+eVV0q5VvctqrXlVqZ/kcRThFM7gAjy4hjrcQQNawADhGV7hzXl0Xpx352PRWnDymWP4A+fzB6pljLY=</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

r'

{n}

r

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

!

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

i

<latexit sha1_base64="iG5kbfrDBlIn+v0Y9SAbLqhksE8=">AAACD3icbVDLSgMxFM34rPU16kZwEyxKC7XMVEFxVXTjsqJ9QFtKJpO2oZlkSDKWMvQP3Pgrblwo4tatO//GtJ2Fth4IHM65j9zjhYwq7Tjf1sLi0vLKamotvb6xubVt7+xWlYgkJhUsmJB1DynCKCcVTTUj9VASFHiM1Lz+9divPRCpqOD3ehiSVoC6nHYoRtpIbfu46YsBR1KKQT6WWZob5bPNiPtEjidCnj/JXd7lr9p2xik4E8B54iYkAxKU2/aXGYyjgHCNGVKq4TqhbsVIaooZGaWbkSIhwn3UJQ1DOQqIasWTe0bwyCg+7AhpHtdwov7uiFGg1DDwTGWAdE/NemPxP68R6c5FK6Y8jDTheLqoEzGoBRyHA30qCdZsaAjCkpq/QtxDEmFtIkybENzZk+dJtVhwTwvF27NMaT+JIwUOwCHIAhecgxK4AWVQARg8gmfwCt6sJ+vFerc+pqULVtKzB/7A+vwBzj2bEQ==</latexit>

#, r(i), (n, ) : S, B

<latexit sha1_base64="tTiA+V+icpMvuj14Rz9fH7LfbTU=">AAACBXicbVBNS8NAEN34WetX1Iugh2ARPJSSVEHxVPTisaL9gCaUyXbTLt1k4+5GKaEXL/4VLx4U8ep/8Oa/cdvmoK0PBh7vzTAzz48Zlcq2v425+YXFpeXcSn51bX1j09zarkueCExqmDMumj5IwmhEaooqRpqxIBD6jDT8/uXIb9wTISmPbtUgJl4I3YgGFIPSUtvcd5MYhOAPxdSVdwkIMiy6UoE4vyletM2CXbLHsGaJk5ECylBtm19uh+MkJJHCDKRsOXasvBSEopiRYd5NJIkB96FLWppGEBLppeMvhtahVjpWwIWuSFlj9fdECqGUg9DXnSGonpz2RuJ/XitRwZmX0ihOFInwZFGQMEtxaxSJ1aGCYMUGmgAWVN9q4R4IwEoHl9chONMvz5J6ueQcl8rXJ4XKbhZHDu2hA3SEHHSKKugKVVENYfSIntErejOejBfj3fiYtM4Z2cwO+gPj8wdheJhX</latexit>

{n}

", ⇤, ? : S, B

<latexit sha1_base64="OeLRYW1M+32rLS307GhLET7Z6Xc=">AAAB+XicbVDLSsNAFL2pr1pfUcGNm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg+g2JsP7brTcBZA68QtSR1KtIf2lxcmJIup0IRjpQauk2o/x1Izwum85mWKpphM8IgODBU4psrPF5vP0aVRQhQl0pTQaKH+nshxrNQsDkxnjPVYrXqF+J83yHR05+dMpJmmgiw/ijKOdIKKGFDIJCWazwzBRDKzKyJjLDHRJqyaCcFdPXmddJsN97rRfLypt87KOKpwDhdwBS7cQgseoA0dIDCFZ3iFNyu3Xqx362PZWrHKmVP4A+vzB5/ck4I=</latexit>

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

<latexit sha1_base64="iG5kbfrDBlIn+v0Y9SAbLqhksE8=">AAACD3icbVDLSgMxFM34rPU16kZwEyxKC7XMVEFxVXTjsqJ9QFtKJpO2oZlkSDKWMvQP3Pgrblwo4tatO//GtJ2Fth4IHM65j9zjhYwq7Tjf1sLi0vLKamotvb6xubVt7+xWlYgkJhUsmJB1DynCKCcVTTUj9VASFHiM1Lz+9divPRCpqOD3ehiSVoC6nHYoRtpIbfu46YsBR1KKQT6WWZob5bPNiPtEjidCnj/JXd7lr9p2xik4E8B54iYkAxKU2/aXGYyjgHCNGVKq4TqhbsVIaooZGaWbkSIhwn3UJQ1DOQqIasWTe0bwyCg+7AhpHtdwov7uiFGg1DDwTGWAdE/NemPxP68R6c5FK6Y8jDTheLqoEzGoBRyHA30qCdZsaAjCkpq/QtxDEmFtIkybENzZk+dJtVhwTwvF27NMaT+JIwUOwCHIAhecgxK4AWVQARg8gmfwCt6sJ+vFerc+pqULVtKzB/7A+vwBzj2bEQ==</latexit>

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

<latexit sha1_base64="MspV0S8w6SWzX1LS8spjRy7yJcI=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmGcjOoNt+kugNeJV5IGKtEZ1b/8KKUmAaEpJ0oNPTfTQU6kZpTDvOYbBRmhUzKGoaWCJKCCfHHzHF9YJcJxKu0TGi/U34mcJErNktBOJkRP1KpXiP95Q6Pj2yBnIjMaBF0uig3HOsVFAThiEqjmM0sIlczeiumESEK1ralmS/BWv7xOeq2md9VsPVw32riso4rO0Dm6RB66QW10jzqoiyjK0DN6RW+OcV6cd+djOVpxyswp+gPn8wfyQpGD</latexit>

m

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

r
<latexit sha1_base64="tTiA+V+icpMvuj14Rz9fH7LfbTU=">AAACBXicbVBNS8NAEN34WetX1Iugh2ARPJSSVEHxVPTisaL9gCaUyXbTLt1k4+5GKaEXL/4VLx4U8ep/8Oa/cdvmoK0PBh7vzTAzz48Zlcq2v425+YXFpeXcSn51bX1j09zarkueCExqmDMumj5IwmhEaooqRpqxIBD6jDT8/uXIb9wTISmPbtUgJl4I3YgGFIPSUtvcd5MYhOAPxdSVdwkIMiy6UoE4vyletM2CXbLHsGaJk5ECylBtm19uh+MkJJHCDKRsOXasvBSEopiRYd5NJIkB96FLWppGEBLppeMvhtahVjpWwIWuSFlj9fdECqGUg9DXnSGonpz2RuJ/XitRwZmX0ihOFInwZFGQMEtxaxSJ1aGCYMUGmgAWVN9q4R4IwEoHl9chONMvz5J6ueQcl8rXJ4XKbhZHDu2hA3SEHHSKKugKVVENYfSIntErejOejBfj3fiYtM4Z2cwO+gPj8wdheJhX</latexit>

{n}

{m}

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

!

<latexit sha1_base64="rRkN2ss//1CAV35C2NV8177jMZs=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqdnplytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzQ+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjMviYDrpAZMbGEMsXtrYSNqKLM2GxKNgRv+eVV0q5VvctqrXlVqZ/kcRThFM7gAjy4hjrcQQNawADhGV7hzXl0Xpx352PRWnDymWP4A+fzB6pljLY=</latexit>

", ⇤, ? : S, B

X

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

()
<latexit sha1_base64="rRkN2ss//1CAV35C2NV8177jMZs=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqdnplytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzQ+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjMviYDrpAZMbGEMsXtrYSNqKLM2GxKNgRv+eVV0q5VvctqrXlVqZ/kcRThFM7gAjy4hjrcQQNawADhGV7hzXl0Xpx352PRWnDymWP4A+fzB6pljLY=</latexit>

X

{n}

<latexit sha1_base64="Jsdndm8LHo00H+MdK7j7c46DUsk=">AAAB9XicbVDLSgMxFL1TX7W+qi7dBItQN2WmCrosuHFZwT6gHUsmvW1DM5khyShl6H+4caGIW//FnX9j2s5CWw8EDufcw705QSy4Nq777eTW1jc2t/LbhZ3dvf2D4uFRU0eJYthgkYhUO6AaBZfYMNwIbMcKaRgIbAXjm5nfekSleSTvzSRGP6RDyQecUWOlh24i+6hm4bR8Pu0VS27FnYOsEi8jJchQ7xW/uv2IJSFKwwTVuuO5sfFTqgxnAqeFbqIxpmxMh9ixVNIQtZ/Or56SM6v0ySBS9klD5urvREpDrSdhYCdDakZ62ZuJ/3mdxAyu/ZTLODEo2WLRIBHERGRWAelzhcyIiSWUKW5vJWxEFWXGFlWwJXjLX14lzWrFu6hU7y5LNZLVkYcTOIUyeHAFNbiFOjSAgYJneIU358l5cd6dj8Vozskyx/AHzucPY1SSUw==</latexit>

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="rRkN2ss//1CAV35C2NV8177jMZs=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqdnplytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzQ+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjMviYDrpAZMbGEMsXtrYSNqKLM2GxKNgRv+eVV0q5VvctqrXlVqZ/kcRThFM7gAjy4hjrcQQNawADhGV7hzXl0Xpx352PRWnDymWP4A+fzB6pljLY=</latexit>

r"

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

i

X

C

{n}
<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

<latexit sha1_base64="MGYvqdsDx04M0mCioUDqd5bJQoE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/UNYzY</latexit>

#, r(i), (n, ) : S, B

#, ⇤, (n, ) : S, B

X

{n}

i
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="MGYvqdsDx04M0mCioUDqd5bJQoE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/UNYzY</latexit>

<latexit sha1_base64="sgZf9P9AFoLOI6T4YN9iAEqNX+0=">AAACEHicbVDLTgIxFO3gC/GFujFx00iMmCCZQRONK6IblxjlkQAhnXKBhk5nbDsSQvgEN/6KGxca49alO//GDsxC0ZM0OTnnPnqPG3CmtG1/WYm5+YXFpeRyamV1bX0jvblVUX4oKZSpz31Zc4kCzgSUNdMcaoEE4rkcqm7/MvKr9yAV88WtHgbQ9EhXsA6jRBuplT5otP2BIFL6g1xD3YVEQi7bCEUbZDQSi9zR4flN7qKVzth5ewL8lzgxyaAYpVb600ymoQdCU06Uqjt2oJsjIjWjHMapRqggILRPulA3VBAPVHM0OWiM943Sxh1fmic0nqg/O0bEU2rouabSI7qnZr1I/M+rh7pz1hwxEYQaBJ0u6oQcax9H6eA2k0A1HxpCqGTmr5j2iCRUmwxTJgRn9uS/pFLIO8f5wvVJprgTx5FEu2gPZZGDTlERXaESKiOKHtATekGv1qP1bL1Z79PShBX3bKNfsD6+ATxQm+Q=</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

{n}

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

<latexit sha1_base64="MGYvqdsDx04M0mCioUDqd5bJQoE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipqQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/UNYzY</latexit>

#, s, (n, ) : S, B
<latexit sha1_base64="SGBWJAMJtAkMbV4GCvHzZclgWaM=">AAACCnicbVDLSgMxFM3UV62vqhvBTbQIFcYyUwXFVdGNy4r2Ae1QMplMG5rJDEnGUkrXbvwVNy4UcesXuPNvzLSz0NYDgcM595F73IhRqSzr28gsLC4tr2RXc2vrG5tb+e2dugxjgUkNhywUTRdJwignNUUVI81IEBS4jDTc/nXiNx6IkDTk92oYESdAXU59ipHSUid/0PbCAUdChANTmsV2zD0ikmGQmyfHl3fmVSdfsErWBHCe2CkpgBTVTv5Lz8RxQLjCDEnZsq1IOSMkFMWMjHPtWJII4T7qkpamHAVEOqPJKWN4pBUP+qHQjys4UX93jFAg5TBwdWWAVE/Oeon4n9eKlX/hjCiPYkU4ni7yYwZVCJNcoEcFwYoNNUFYUP1XiHtIIKx0ejkdgj178jypl0v2aal8e1ao7KVxZME+OARFYINzUAE3oApqAINH8AxewZvxZLwY78bHtDRjpD274A+Mzx9EK5ku</latexit>

m

!

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

<latexit sha1_base64="yKLwdzFZbq0IAFA/hQpoJsNP5+o=">AAACEXicbVDLSgMxFM34rPU16kZwEyxChVJmqqC4KrpxWdE+oDOUTHrbhmYyY5KxlNJfcOOvuHGhiFt37vwb08dCWw8EDufcR+4JYs6Udpxva2FxaXllNbWWXt/Y3Nq2d3YrKkokhTKNeCRrAVHAmYCyZppDLZZAwoBDNehejfzqA0jFInGn+zH4IWkL1mKUaCM17KzXjHqCSBn1cp66T4iEXNZLRBPkaCQWOcyOL25zlw074+SdMfA8cackg6YoNewvM5omIQhNOVGq7jqx9gdEakY5DNNeoiAmtEvaUDdUkBCUPxhfNMRHRmniViTNExqP1d8dAxIq1Q8DUxkS3VGz3kj8z6snunXuD5iIEw2CTha1Eo51hEfx4CaTQDXvG0KoZOavmHaIJFSbENMmBHf25HlSKeTdk3zh5jRT3J/GkUIH6BBlkYvOUBFdoxIqI4oe0TN6RW/Wk/VivVsfk9IFa9qzh/7A+vwB+4OcSg==</latexit>

m

{n}

r

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6dF+fd+Vi0Fpx85hj+wPn8AcQpjMc=</latexit>

C

<latexit sha1_base64="GPUlgkvy/ynRqXX2oiat4qLBsQY=">AAACC3icbVDLSgMxFM3UV62vqhvBTWgRKtQyUwXFVdGNy4r2Ae1QMmmmDU0yQ5KxlKF7N/6KGxeKuPUH3Pk3pu0stPVA4HDOfeQeL2RUadv+tlJLyyura+n1zMbm1vZOdnevroJIYlLDAQtk00OKMCpITVPNSDOUBHGPkYY3uJ74jQciFQ3EvR6FxOWoJ6hPMdJG6mRz7W4wFEjKYFjkxUI7El0iJ8OgKMKT48u74lUnm7dL9hRwkTgJyYME1U72ywzFESdCY4aUajl2qN0YSU0xI+NMO1IkRHiAeqRlqECcKDee3jKGR0bpQj+Q5gkNp+rvjhhxpUbcM5Uc6b6a9ybif14r0v6FG1MRRpoIPFvkRwzqAE6CgV0qCdZsZAjCkpq/QtxHEmFt4suYEJz5kxdJvVxyTkvl27N85SCJIw0OQQ4UgAPOQQXcgCqoAQwewTN4BW/Wk/VivVsfs9KUlfTsgz+wPn8AmyCZUg==</latexit>

<latexit sha1_base64="iG5kbfrDBlIn+v0Y9SAbLqhksE8=">AAACD3icbVDLSgMxFM34rPU16kZwEyxKC7XMVEFxVXTjsqJ9QFtKJpO2oZlkSDKWMvQP3Pgrblwo4tatO//GtJ2Fth4IHM65j9zjhYwq7Tjf1sLi0vLKamotvb6xubVt7+xWlYgkJhUsmJB1DynCKCcVTTUj9VASFHiM1Lz+9divPRCpqOD3ehiSVoC6nHYoRtpIbfu46YsBR1KKQT6WWZob5bPNiPtEjidCnj/JXd7lr9p2xik4E8B54iYkAxKU2/aXGYyjgHCNGVKq4TqhbsVIaooZGaWbkSIhwn3UJQ1DOQqIasWTe0bwyCg+7AhpHtdwov7uiFGg1DDwTGWAdE/NemPxP68R6c5FK6Y8jDTheLqoEzGoBRyHA30qCdZsaAjCkpq/QtxDEmFtIkybENzZk+dJtVhwTwvF27NMaT+JIwUOwCHIAhecgxK4AWVQARg8gmfwCt6sJ+vFerc+pqULVtKzB/7A+vwBzj2bEQ==</latexit>

r

<latexit sha1_base64="qYFcCaJhyNdSsvxCQuR+/vZ4GwU=">AAAB6HicbVBNS8NAEJ3Ur1q/ql4EL4tF8FSSKuix4MVjC7YW2lA220m7drMJuxuhhP4CLx4U8epP8ua/cdvmoK0PBh7vzTAzL0gE18Z1v53C2vrG5lZxu7Szu7d/UD48aus4VQxbLBax6gRUo+ASW4YbgZ1EIY0CgQ/B+HbmPzyh0jyW92aSoB/RoeQhZ9RYqcn75Ypbdecgq8TLSQVyNPrlr94gZmmE0jBBte56bmL8jCrDmcBpqZdqTCgb0yF2LZU0Qu1n80On5NwqAxLGypY0ZK7+nshopPUkCmxnRM1IL3sz8T+vm5rwxs+4TFKDki0WhakgJiazr8mAK2RGTCyhTHF7K2EjqigzNpuSDcFbfnmVtGtV77Jaa15V6id5HEU4hTO4AA+uoQ530IAWMEB4hld4cx6d

#, r(i), (n, ) : S, B

<latexit sha1_base64="tTiA+V+icpMvuj14Rz9fH7LfbTU=">AAACBXicbVBNS8NAEN34WetX1Iugh2ARPJSSVEHxVPTisaL9gCaUyXbTLt1k4+5GKaEXL/4VLx4U8ep/8Oa/cdvmoK0PBh7vzTAzz48Zlcq2v425+YXFpeXcSn51bX1j09zarkueCExqmDMumj5IwmhEaooqRpqxIBD6jDT8/uXIb9wTISmPbtUgJl4I3YgGFIPSUtvcd5MYhOAPxdSVdwkIMiy6UoE4vyletM2CXbLHsGaJk5ECylBtm19uh+MkJJHCDKRsOXasvBSEopiRYd5NJIkB96FLWppGEBLppeMvhtahVjpWwIWuSFlj9fdECqGUg9DXnSGonpz2RuJ/XitRwZmX0ihOFInwZFGQMEtxaxSJ1aGCYMUGmgAWVN9q4R4IwEoHl9chONMvz5J6ueQcl8rXJ4XKbhZHDu2hA3SEHHSKKugKVVENYfSIntErejOejBfj3fiYtM4Z2cwO+gPj8wdheJhX</latexit>

i

", ⇤, ? : S, B

C C
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

()

<latexit sha1_base64="qwmkCCdWplvKEzFyiMtXfVPNC8U=">AAAB83icbVDLSsNAFJ3UV62vqks3g0VwVZIq6LLgxmUF+4AmlMnkph06mYR5CCX0N9y4UMStP+POv3HSZqGtBwYO59zDvXPCjDOlXffbqWxsbm3vVHdre/sHh0f145OeSo2k0KUpT+UgJAo4E9DVTHMYZBJIEnLoh9O7wu8/gVQsFY96lkGQkLFgMaNEW8n3jYhAFmEsRvWG23QXwOvEK0kDleiM6l9+lFKTgNCUE6WGnpvpICdSM8phXvONgozQKRnD0FJBElBBvrh5ji+sEuE4lfYJjRfq70ROEqVmSWgnE6InatUrxP+8odHxbZAzkRkNgi4XxYZjneKiABwxCVTzmSWESmZvxXRCJKHa1lSzJXirX14nvVbTu2q2Hq4bbVzWUUVn6BxdIg/doDa6Rx3URRRl6Bm9ojfHOC/Ou/OxHK04ZeYU/YHz+QPzxpGE</latexit>

n

<latexit sha1_base64="Jsdndm8LHo00H+MdK7j7c46DUsk=">AAAB9XicbVDLSgMxFL1TX7W+qi7dBItQN2WmCrosuHFZwT6gHUsmvW1DM5khyShl6H+4caGIW//FnX9j2s5CWw8EDufcw705QSy4Nq777eTW1jc2t/LbhZ3dvf2D4uFRU0eJYthgkYhUO6AaBZfYMNwIbMcKaRgIbAXjm5nfekSleSTvzSRGP6RDyQecUWOlh24i+6hm4bR8Pu0VS27FnYOsEi8jJchQ7xW/uv2IJSFKwwTVuuO5sfFTqgxnAqeFbqIxpmxMh9ixVNIQtZ/Or56SM6v0ySBS9klD5urvREpDrSdhYCdDakZ62ZuJ/3mdxAyu/ZTLODEo2WLRIBHERGRWAelzhcyIiSWUKW5vJWxEFWXGFlWwJXjLX14lzWrFu6hU7y5LNZLVkYcTOIUyeHAFNbiFOjSAgYJneIU358l5cd6dj8Vozskyx/AHzucPY1SSUw==</latexit>

<latexit sha1_base64="XefsvhPirC/uKVcTKaU7lR0G9y4=">AAAB+XicbVDLSsNAFL2pr1pfUTeCm8EiuCpJFXRZcOOygn1AE8pkMmmHTiZhZlIooX/ixoUibv0Td/6NkzYLbT1w4XDOvTP3niDlTGnH+bYqG5tb2zvV3dre/sHhkX180lVJJgntkIQnsh9gRTkTtKOZ5rSfSorjgNNeMLkv/N6USsUS8aRnKfVjPBIsYgRrIw1t28u9TIRUFg8g4c2Hdt1pOAugdeKWpA4l2kP7ywsTksVUaMKxUgPXSbWfY6kZ4XRe8zJFU0wmeEQHhgocU+Xni83n6NIoIYoSaUpotFB/T+Q4VmoWB6YzxnqsVr1C/M8bZDq683Mm0kxTQZYfRRlHOkFFDChkkhLNZ4ZgIpnZFZExlphoE1bNhOCunrxOus2Ge91oPt7UW2dlHFU4hwu4AhduoQUP0IYOEJjCM7zCm5VbL9a79bFsrVjlzCn8gfX5A6H8k4U=</latexit>

a

a

<latexit sha1_base64="KRKwyXUtEvutNvkeZUfGqRTF1zQ=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipSQflilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz+6cYzH</latexit>

<latexit sha1_base64="Mip0N8d+lLCHamebqU0xjE7iBMQ=">AAACHnicbVDLSgMxFM3UV62vUTeCm2ARWhjLTFUUV0U3LivaB7RDyWTSNjSTGZKMpQz9Ejf+ihsXigiu9G9MH4vaeiBwOOc+co8XMSqVbf8YqaXlldW19HpmY3Nre8fc3avKMBaYVHDIQlH3kCSMclJRVDFSjwRBgcdIzevdjPzaIxGShvxBDSLiBqjDaZtipLTUMs+bftjnSIiwbyUo14y5T8RoWBIMLZofWjMSzOWtk/zVvXXdMrN2wR4DLhJnSrJginLL/NJ7cBwQrjBDUjYcO1JugoSimJFhphlLEiHcQx3S0JSjgEg3GZ83hMda8WE7FPpxBcfqbEeCAikHgacrA6S6ct4bif95jVi1L92E8ihWhOPJonbMoArhKCvoU0GwYgNNEBZU/xXiLhIIK51oRofgzJ+8SKrFgnNaKN6dZUsH0zjS4BAcgRxwwAUogVtQBhWAwRN4AW/g3Xg2Xo0P43NSmjKmPfvgD4zvX2YCoSw=</latexit>

#, a(m, i), ((), ) : S, B

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="yqAXryogLgxlTVXcD/7I/xkdckw=">AAACE3icbVDLTgIxFO3gC/GFujFx00hMwCCZQRONK6IblxjlkQAhnXKBhk5nbDsSMuEf3PgrblxojFs37vwby2Oh4EmanJxzH73HDThT2ra/rdjC4tLySnw1sba+sbmV3N4pKz+UFErU576sukQBZwJKmmkO1UAC8VwOFbd3NfIrDyAV88WdHgTQ8EhHsDajRBupmTyqt/y+IFL6/WxUV/chkTDMpuuhaIEcDcXpTPY4c3GbvWwmU3bOHgPPE2dKUmiKYjP5ZYbT0AOhKSdK1Rw70I2ISM0oh2GiHioICO2RDtQMFcQD1YjGNw3xoVFauO1L84TGY/V3R0Q8pQaeayo9ortq1huJ/3m1ULfPGxETQahB0Mmidsix9vEoINxiEqjmA0MIlcz8FdMukYRqE2PChODMnjxPyvmcc5LL35ymCnvTOOJoHx2gNHLQGSqga1REJUTRI3pGr+jNerJerHfrY1Ias6Y9u+gPrM8fKIOc3Q==</latexit>

C

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

#, ⇤, ((), ) : S, B

l

l

C

<latexit sha1_base64="L3w36hKZEf3CPUHXd8crJ2oG19k=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipKQblilt1FyDrxMtJBXI0BuWv/jBmaYTSMEG17nluYvyMKsOZwFmpn2pMKJvQEfYslTRC7WeLQ2fkwipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDWz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m5INwVt9eZ20a1XvqlprXlfqJI+jCGdwDpfgwQ3U4R4a0AIGCM/wCm/Oo/PivDsfy9aCk8+cwh84nz/LHYzS</latexit>

<latexit sha1_base64="9eZxzWLsmpyn9WuSVt2U97lNdbQ=">AAACEHicbVDLSgMxFM34rPU16kZwEyziFGqZqYLiqujGZUX7gHYomTRtQzPJkGQsZegnuPFX3LhQxK1Ld/6N6WOhrQcCh3PuI/cEEaNKu+63tbC4tLyymlpLr29sbm3bO7sVJWKJSRkLJmQtQIowyklZU81ILZIEhQEj1aB3PfKrD0QqKvi9HkTED1GH0zbFSBupaR83WqLPkZSin0uYQ7PDnNOIeYvI0UToZHMn2cu73FXTzrh5dww4T7wpyYApSk37y0zGcUi4xgwpVffcSPsJkppiRobpRqxIhHAPdUjdUI5CovxkfNAQHhmlBdtCmsc1HKu/OxIUKjUIA1MZIt1Vs95I/M+rx7p94SeUR7EmHE8WtWMGtYCjdGCLSoI1GxiCsKTmrxB3kURYmwzTJgRv9uR5UinkvdN84fYsU9yfxpECB+AQOMAD56AIbkAJlAEGj+AZvII368l6sd6tj0npgjXt2QN/YH3+AMhkmvg=</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

#, l(i), ((), ) : S, B

<latexit sha1_base64="yqAXryogLgxlTVXcD/7I/xkdckw=">AAACE3icbVDLTgIxFO3gC/GFujFx00hMwCCZQRONK6IblxjlkQAhnXKBhk5nbDsSMuEf3PgrblxojFs37vwby2Oh4EmanJxzH73HDThT2ra/rdjC4tLySnw1sba+sbmV3N4pKz+UFErU576sukQBZwJKmmkO1UAC8VwOFbd3NfIrDyAV88WdHgTQ8EhHsDajRBupmTyqt/y+IFL6/WxUV/chkTDMpuuhaIEcDcXpTPY4c3GbvWwmU3bOHgPPE2dKUmiKYjP5ZYbT0AOhKSdK1Rw70I2ISM0oh2GiHioICO2RDtQMFcQD1YjGNw3xoVFauO1L84TGY/V3R0Q8pQaeayo9ortq1huJ/3m1ULfPGxETQahB0Mmidsix9vEoINxiEqjmA0MIlcz8FdMukYRqE2PChODMnjxPyvmcc5LL35ymCnvTOOJoHx2gNHLQGSqga1REJUTRI3pGr+jNerJerHfrY1Ias6Y9u+gPrM8fKIOc3Q==</latexit>

!

#, ⇤, ((), ) : S, B

<latexit sha1_base64="JQ7O+IXGKQnCywzOP7HUyj374DU=">AAAB6XicbVBNS8NAEJ3Ur1q/qh69LFbBU0mqoMeCF49V7Ae0oWy2k3bpZhN2N0IJ/QdePCji1X/kzX/jts1BWx8MPN6bYWZekAiujet+O4W19Y3NreJ2aWd3b/+gfHjU0nGqGDZZLGLVCahGwSU2DTcCO4lCGgUC28H4dua3n1BpHstHM0nQj+hQ8pAzaqz00Dvrlytu1Z2DrBIvJxXI0eiXv3qDmKURSsME1brruYnxM6oMZwKnpV6qMaFsTIfYtVTSCLWfzS+dknOrDEgYK1vSkLn6eyKjkdaTKLCdETUjvezNxP+8bmrCGz/jMkkNSrZYFKaCmJjM3iYDrpAZMbGEMsXtrYSNqKLM2HBKNgRv+eVV0qpVvctq7f6qUid5HEU4gVO4AA+uoQ530IAmMAjhGV7hzRk7L86787FoLTj5zDH8gfP5Aw68jPA=</latexit>

<latexit sha1_base64="cYxmm5Wccyh575rbHJ8AeGAwrjU=">AAACDXicbVDLSgMxFM3UV62vUTeCm2ArVBjLTBUUV0U3LivaB7SlZDJpG5rJDEnGUob+gBt/xY0LRdy6d+ffmGlnodUDgcM595F73JBRqWz7y8gsLC4tr2RXc2vrG5tb5vZOXQaRwKSGAxaIposkYZSTmqKKkWYoCPJdRhru8CrxG/dESBrwOzUOScdHfU57FCOlpa5ZaHvBiCMhgpEVtwsTq9iOuEdEMg9y6/jo4ta67Jp5u2RPAf8SJyV5kKLaNT/1WBz5hCvMkJQtxw5VJ0ZCUczIJNeOJAkRHqI+aWnKkU9kJ55eM4GHWvFgLxD6cQWn6s+OGPlSjn1XV/pIDeS8l4j/ea1I9c47MeVhpAjHs0W9iEEVwCQa6FFBsGJjTRAWVP8V4gESCCsdYE6H4Myf/JfUyyXnpFS+Oc1X9tI4smAfHIAicMAZqIBrUAU1gMEDeAIv4NV4NJ6NN+N9Vpox0p5d8AvGxzdko5pR</latexit>

$

#, $, (n, ) : S, B

op
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="zkAxKpAMzxe8/whqt38IfiDgr5E=">AAACEnicbVDLSgMxFM3UV62vUTeCm2ARWqhlpgqKq6IblxXtA9pSMultDc1kxiRjKUO/wY2/4saFIm5dufNvTB8LbT0QOJxzH7nHCzlT2nG+rcTC4tLySnI1tba+sbllb+9UVBBJCmUa8EDWPKKAMwFlzTSHWiiB+B6Hqte7HPnVB5CKBeJWD0Jo+qQrWIdRoo3UsrONdtAXRMqgn4sb6j4iEoa5TCMSbZCjoVjkjrLnN7mLlp128s4YeJ64U5JGU5Ra9peZTSMfhKacKFV3nVA3YyI1oxyGqUakICS0R7pQN1QQH1QzHp80xIdGaeNOIM0TGo/V3x0x8ZUa+J6p9Im+U7PeSPzPq0e6c9aMmQgjDYJOFnUijnWAR/ngNpNANR8YQqhk5q+Y3hFJqDYppkwI7uzJ86RSyLvH+cL1Sbq4N40jifbRAcogF52iIrpCJVRGFD2iZ/SK3qwn68V6tz4mpQlr2rOL/sD6/AEi4Zzw</latexit>

C

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C

#, ⇤, (n, ) : S, B

F gure 10 Computat on rewr tes

it involves no copying of the argument. To anticipate a little, the copying will be
performed by the contraction nodes.
The s-ru e represents the step command wh ch evaluates the dataflow graph wh ch
will be discussed later. This rewrite, with an token exiting the incoming port d =↓
is performed after this evaluation. The dataflow evaluation leaves a value n on S
indicating that n nodes were updated, so the s-node is replaced by a constant n
value box.
The p-ru e represents the peek command which reads the value off the dataflow
graph, as pointed at by the p node, and creates an constant n valued box from it.
Note that the outgo ng port of the p node s replaced by a weaken ng C nd cat ng
that port became unreachable.
The m-ru e represents cell creation, and is executed by replacing the m node by a nn t al sed cell node The value n s retr eved off the stack n where t s augmented

12 15

## PDF page 16

Transparent Synchronous Dataflow

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C

C

Cc

", C, S, l : m : B

l

X

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="qBtqVObSvGnCKXW8IpC9CB/PhGQ=">AAAB+3icbVDLSgMxFM3UV62vsW4EN8EiuChlpgqKq2I3LivaB7RDyaSZNjTJDElGLcP8ihsXirj1R9z5N6btLLT1wIXDOfdy7z1+xKjSjvNt5VZW19Y38puFre2d3T17v9hSYSwxaeKQhbLjI0UYFaSpqWakE0mCuM9I2x/Xp377gUhFQ3GvJxHxOBoKGlCMtJH6drEXR0jK8LGc1NPyXZlfXfftklNxZoDLxM1ICWRo9O2v3iDEMSdCY4aU6rpOpL0ESU0xI2mhFysSITxGQ9I1VCBOlJfMbk/hiVEGMAilKaHhTP09kSCu1IT7ppMjPVKL3lT8z+vGOrj0EiqiWBOB54uCmEEdwmkQcEAlwZpNDEFYUnMrxCMkEdYmroIJwV18eZm0qhX3rFK9PS/VDrM48uAIHINT4IILUAM3oAGaAIMn8AxewZuVWi/Wu/Uxb81Z2cwB+APr8wcB6JOg</latexit>

C

C

m

", C, S, m : B

<latexit sha1_base64="TWs1GeWgXImfj7jhScI5uo320qw=">AAAB+XicbVBNS8NAEJ3Ur1q/ol4EL4tF8FBKUgU9FnvxWNF+QBvKZrtpl242YXdTKaH/xIsHRbz6T7z5b9y2OWjrg4HHezPMzPNjzpR2nG8rt7a+sbmV3y7s7O7tH9iHR00VJZLQBol4JNs+VpQzQRuaaU7bsaQ49Dlt+aPazG+NqVQsEo96ElMvxAPBAkawNlLPtrtJjKWMnkppbVp6KN327KJTduZAq8TNSBEy1Hv2V7cfkSSkQhOOleq4Tqy9FEvNCKfTQjdRNMZkhAe0Y6jAIVVeOr98is6N0kdBJE0Jjebq74kUh0pNQt90hlgP1bI3E//zOokObryUiTjRVJDFoiDhSEdoFgPqM0mJ5hNDMJHM3IrIEEtMtAmrYEJwl19eJc1K2b0sV+6vitWTLI48nMIZXIAL11CFO6hDAwiM4Rle4c1KrRfr3fpYtOasbOYY/sD6/AGuWpLl</latexit>

?

G

µ

G

!

µ

l

X

", C, S, B

μ

<latexit sha1_base64="JfNhHDmiXWSkW51tt1a0oYAngQE=">AAAB6nicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWNE84BkCbOT2WTIzOwy0yuEkE/w4kERr36RN//GSbIHTSxoKKq66e6KUiks+v63t7a+sbm1Xdgp7u7tHxyWjo6bNskM4w2WyMS0I2q5FJo3UKDk7dRwqiLJW9Hodua3nrixItGPOE55qOhAi1gwik566KqsVyr7FX8OskqCnJQhR71X+ur2E5YprpFJam0n8FMMJ9SgYJJPi93M8pSyER3wjqOaKm7DyfzUKTl3Sp/EiXGlkczV3xMTqqwdq8h1KopDu+zNxP+8TobxTTgROs2Qa7ZYFGeSYEJmf5O+MJyhHDtCmRHuVsKG1FCGLp2iCyFYfnmVNKuV4LJSvb8q10geRwFO4QwuIIBrqMEd1KEBDAbwDK/w5knvxXv3Phata14+cwJ/4H3+AFRyjbg=</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="JfNhHDmiXWSkW51tt1a0oYAngQE=">AAAB6nicbVDLSgNBEOz1GeMr6tHLYBA8hd0o6DHgxWNE84BkCbOT2WTIzOwy0yuEkE/w4kERr36RN//GSbIHTSxoKKq66e6KUiks+v63t7a+sbm1Xdgp7u7tHxyWjo6bNskM4w2WyMS0I2q5FJo3UKDk7dRwqiLJW9Hodua3nrixItGPOE55qOhAi1gwik566KqsVyr7FX8OskqCnJQhR71X+ur2E5YprpFJam0n8FMMJ9SgYJJPi93M8pSyER3wjqOaKm7DyfzUKTl3Sp/EiXGlkczV3xMTqqwdq8h1KopDu+zNxP+8TobxTTgROs2Qa7ZYFGeSYEJmf5O+MJyhHDtCmRHuVsKG1FCGLp2iCyFYfnmVNKuV4LJSvb8q10geRwFO4QwuIIBrqMEd1KEBDAbwDK/w5knvxXv3Phata14+cwJ/4H3+AFRyjbg=</latexit>

m
<latexit sha1_base64="mpmCrLt/syOzqr7E2KJ5U8z6k84=">AAAB/XicbVDLSgMxFM3UV62v8bEQ3ASL4KKUmSooXRW7cVnRPqAdSibNtKGZZEgySh2Kv+LGhSJu/Q93/o1pOwttPXDhcM693HuPHzGqtON8W5ml5ZXVtex6bmNza3vH3t1rKBFLTOpYMCFbPlKEUU7qmmpGWpEkKPQZafrD6sRv3hOpqOB3ehQRL0R9TgOKkTZS1z7oxBGSUjwUkuq4cFtg5bB81bXzTtGZAi4SNyV5kKLWtb86PYHjkHCNGVKq7TqR9hIkNcWMjHOdWJEI4SHqk7ahHIVEecn0+jE8MUoPBkKa4hpO1d8TCQqVGoW+6QyRHqh5byL+57VjHVx6CeVRrAnHs0VBzKAWcBIF7FFJsGYjQxCW1NwK8QBJhLUJLGdCcOdfXiSNUtE9K5ZuzvOVwzSOLDgCx+AUuOACVMA1qIE6wOARPINX8GY9WS/Wu/Uxa81Y6cw++APr8wdVNZRa</latexit>

C

?

<latexit sha1_base64="d7+gYvO9MDtHlQL1JdLzCb1Ueyw=">AAAB/3icbVDLSgMxFM3UV62vUUEEN8EiuChlpgq6LLpxWdE+oDOUTJppQzPJmGSUMnbhr7hxoYhbf8Odf2PazkJbD1w4nHMv994TxIwq7TjfVm5hcWl5Jb9aWFvf2Nyyt3caSiQSkzoWTMhWgBRhlJO6ppqRViwJigJGmsHgcuw374lUVPBbPYyJH6EepyHFSBupY+95SYykFA+l1FN3CZJkVLopXXTsolN2JoDzxM1IEWSodewvrytwEhGuMUNKtV0n1n6KpKaYkVHBSxSJER6gHmkbylFElJ9O7h/BI6N0YSikKa7hRP09kaJIqWEUmM4I6b6a9cbif1470eG5n1IeJ5pwPF0UJgxqAcdhwC6VBGs2NARhSc2tEPeRRFibyAomBHf25XnSqJTdk3Ll+rRY3c/iyIMDcAiOgQvOQBVcgRqoAwwewTN4BW/Wk/VivVsf09aclc3sgj+wPn8AxbOVyw==</latexit>

", ⇤, S, B

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="Qp5PH18w9dp/IH94ed5USX6iAjY=">AAAB+XicbVDLSsNAFJ3UV62vqBvBzWARXJSSVEGXRTcuK9pWaEKZTCft0JlJmEelhP6JGxeKuPVP3Pk3TtsstPXAhcM593LvPVHKqNKe9+0UVlbX1jeKm6Wt7Z3dPXf/oKUSIzFp4oQl8jFCijAqSFNTzchjKgniESPtaHgz9dsjIhVNxIMepyTkqC9oTDHSVuq6bmBSJGXyVAm4qdxXrrtu2at6M8Bl4uekDHI0uu5X0Euw4URozJBSHd9LdZghqSlmZFIKjCIpwkPUJx1LBeJEhdns8gk8tUoPxom0JTScqb8nMsSVGvPIdnKkB2rRm4r/eR2j46swoyI1mgg8XxQbBnUCpzHAHpUEaza2BGFJ7a0QD5BEWNuwSjYEf/HlZdKqVf3zau3uolw/yuMogmNwAs6ADy5BHdyCBmgCDEbgGbyCNydzXpx352PeWnDymUPwB87nD7Lekug=</latexit>

!

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

", µ, S, B

<latexit sha1_base64="d7+gYvO9MDtHlQL1JdLzCb1Ueyw=">AAAB/3icbVDLSgMxFM3UV62vUUEEN8EiuChlpgq6LLpxWdE+oDOUTJppQzPJmGSUMnbhr7hxoYhbf8Odf2PazkJbD1w4nHMv994TxIwq7TjfVm5hcWl5Jb9aWFvf2Nyyt3caSiQSkzoWTMhWgBRhlJO6ppqRViwJigJGmsHgcuw374lUVPBbPYyJH6EepyHFSBupY+95SYykFA+l1FN3CZJkVLopXXTsolN2JoDzxM1IEWSodewvrytwEhGuMUNKtV0n1n6KpKaYkVHBSxSJER6gHmkbylFElJ9O7h/BI6N0YSikKa7hRP09kaJIqWEUmM4I6b6a9cbif1470eG5n1IeJ5pwPF0UJgxqAcdhwC6VBGs2NARhSc2tEPeRRFibyAomBHf25XnSqJTdk3Ll+rRY3c/iyIMDcAiOgQvOQBVcgRqoAwwewTN4BW/Wk/VivVsf09aclc3sgj+wPn8AxbOVyw==</latexit>

?

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

G

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

?

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

G

!

C

", !, S, l : B

!

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

", !, S, B

!

X

", !, S, B

<latexit sha1_base64="d7+gYvO9MDtHlQL1JdLzCb1Ueyw=">AAAB/3icbVDLSgMxFM3UV62vUUEEN8EiuChlpgq6LLpxWdE+oDOUTJppQzPJmGSUMnbhr7hxoYhbf8Odf2PazkJbD1w4nHMv994TxIwq7TjfVm5hcWl5Jb9aWFvf2Nyyt3caSiQSkzoWTMhWgBRhlJO6ppqRViwJigJGmsHgcuw374lUVPBbPYyJH6EepyHFSBupY+95SYykFA+l1FN3CZJkVLopXXTsolN2JoDzxM1IEWSodewvrytwEhGuMUNKtV0n1n6KpKaYkVHBSxSJER6gHmkbylFElJ9O7h/BI6N0YSikKa7hRP09kaJIqWEUmM4I6b6a9cbif1470eG5n1IeJ5pwPF0UJgxqAcdhwC6VBGs2NARhSc2tEPeRRFibyAomBHf25XnSqJTdk3Ll+rRY3c/iyIMDcAiOgQvOQBVcgRqoAwwewTN4BW/Wk/VivVsf09aclc3sgj+wPn8AxbOVyw==</latexit>

<latexit sha1_base64="hlzuG4tXirloWPCQYnFAgGBjyLo=">AAAB+XicbVBNS8NAEJ3Ur1q/ol4EL6tF8FBKUgU9Fr14rGg/oA1ls920SzfZsLuplNB/4sWDIl79J978N27bHLT1wcDjvRlm5vkxZ0o7zreVW1ldW9/Ibxa2tnd29+z9g4YSiSS0TgQXsuVjRTmLaF0zzWkrlhSHPqdNf3g79ZsjKhUT0aMex9QLcT9iASNYG6lr250kxlKKp1J6Mik9lG66dtEpOzOgZeJmpAgZal37q9MTJAlppAnHSrVdJ9ZeiqVmhNNJoZMoGmMyxH3aNjTCIVVeOrt8gs6M0kOBkKYijWbq74kUh0qNQ990hlgP1KI3Ff/z2okOrr2URXGiaUTmi4KEIy3QNAbUY5ISzceGYCKZuRWRAZaYaBNWwYTgLr68TBqVsntRrtxfFqtHWRx5OIZTOAcXrqAKd1CDOhAYwTO8wpuVWi/Wu/Uxb81Z2cwh/IH1+QN6KJLD</latexit>

𝛿

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

", ⇤, S, B

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

!

C

C

?

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="hlzuG4tXirloWPCQYnFAgGBjyLo=">AAAB+XicbVBNS8NAEJ3Ur1q/ol4EL6tF8FBKUgU9Fr14rGg/oA1ls920SzfZsLuplNB/4sWDIl79J978N27bHLT1wcDjvRlm5vkxZ0o7zreVW1ldW9/Ibxa2tnd29+z9g4YSiSS0TgQXsuVjRTmLaF0zzWkrlhSHPqdNf3g79ZsjKhUT0aMex9QLcT9iASNYG6lr250kxlKKp1J6Mik9lG66dtEpOzOgZeJmpAgZal37q9MTJAlppAnHSrVdJ9ZeiqVmhNNJoZMoGmMyxH3aNjTCIVVeOrt8gs6M0kOBkKYijWbq74kUh0qNQ990hlgP1KI3Ff/z2okOrr2URXGiaUTmi4KEIy3QNAbUY5ISzceGYCKZuRWRAZaYaBNWwYTgLr68TBqVsntRrtxfFqtHWRx5OIZTOAcXrqAKd1CDOhAYwTO8wpuVWi/Wu/Uxb81Z2cwh/IH1+QN6KJLD</latexit>

G

G

X-!

X

l
<latexit sha1_base64="Vx6d8qdp2rh8wRL8simngwES+Cs=">AAAB+3icbVDLSgMxFM3UV62vsW4EN9EiuChlpgqKq6IblxXtA9qhZNJMG5pJhiSjlmF+xY0LRdz6I+78G9N2Ftp64MLhnHu59x4/YlRpx/m2ckvLK6tr+fXCxubW9o69W2wqEUtMGlgwIds+UoRRThqaakbakSQo9Blp+aPrid96IFJRwe/1OCJeiAacBhQjbaSeXezGEZJSPJaTw7R8V2aXVz275FScKeAicTNSAhnqPfur2xc4DgnXmCGlOq4TaS9BUlPMSFroxopECI/QgHQM5Sgkykumt6fw2Ch9GAhpims4VX9PJChUahz6pjNEeqjmvYn4n9eJdXDhJZRHsSYczxYFMYNawEkQsE8lwZqNDUFYUnMrxEMkEdYmroIJwZ1/eZE0qxX3tFK9PSvV9rM48uAAHIET4IJzUAM3oA4aAIMn8AxewZuVWi/Wu/Uxa81Z2cwe+APr8wfL3ZN9</latexit>

?
<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

C-!

?
<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

", ⇤, S, B

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

C

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

!

?

G

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

l
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

!

C

l

<latexit sha1_base64="Vx6d8qdp2rh8wRL8simngwES+Cs=">AAAB+3icbVDLSgMxFM3UV62vsW4EN9EiuChlpgqKq6IblxXtA9qhZNJMG5pJhiSjlmF+xY0LRdz6I+78G9N2Ftp64MLhnHu59x4/YlRpx/m2ckvLK6tr+fXCxubW9o69W2wqEUtMGlgwIds+UoRRThqaakbakSQo9Blp+aPrid96IFJRwe/1OCJeiAacBhQjbaSeXezGEZJSPJaTw7R8V2aXVz275FScKeAicTNSAhnqPfur2xc4DgnXmCGlOq4TaS9BUlPMSFroxopECI/QgHQM5Sgkykumt6fw2Ch9GAhpims4VX9PJChUahz6pjNEeqjmvYn4n9eJdXDhJZRHsSYczxYFMYNawEkQsE8lwZqNDUFYUnMrxEMkEdYmroIJwZ1/eZE0qxX3tFK9PSvV9rM48uAAHIET4IJzUAM3oA4aAIMn8AxewZuVWi/Wu/Uxa81Z2cwe+APr8wfL3ZN9</latexit>

", !, S, l : B

", !, S, B
<latexit sha1_base64="hlzuG4tXirloWPCQYnFAgGBjyLo=">AAAB+XicbVBNS8NAEJ3Ur1q/ol4EL6tF8FBKUgU9Fr14rGg/oA1ls920SzfZsLuplNB/4sWDIl79J978N27bHLT1wcDjvRlm5vkxZ0o7zreVW1ldW9/Ibxa2tnd29+z9g4YSiSS0TgQXsuVjRTmLaF0zzWkrlhSHPqdNf3g79ZsjKhUT0aMex9QLcT9iASNYG6lr250kxlKKp1J6Mik9lG66dtEpOzOgZeJmpAgZal37q9MTJAlppAnHSrVdJ9ZeiqVmhNNJoZMoGmMyxH3aNjTCIVVeOrt8gs6M0kOBkKYijWbq74kUh0qNQ990hlgP1KI3Ff/z2okOrr2URXGiaUTmi4KEIy3QNAbUY5ISzceGYCKZuRWRAZaYaBNWwYTgLr68TBqVsntRrtxfFqtHWRx5OIZTOAcXrqAKd1CDOhAYwTO8wpuVWi/Wu/Uxb81Z2cwh/IH1+QN6KJLD</latexit>

Figure 11 Copying rewrites

with the port i so that it can be used by other dataflow graph manipulating
operations.
The r -rules: compute the dependency (‘root’) of a graph. There are three versions of
the rule ( r, r ′ , r ′′ ) depending on whether the requested dependency is incoming to
a contraction, constant, or some other node. In all cases the token ‘jumps’ to the
incoming port of the cell, labelled by i . Note that this rule is ‘non-local’, involving
edge i located in some arbitrary point in the graph. The node which is at the nock
of the arrow is irrelevant and it is not shown.
The op-rules: compute operators by replacing the operation node with the resulting
value as returned by the token and left on S . This is very similar to how stack
machines generally evaluate operators. The outgoing ports of the operator are
detached from the graph via weakening.
The a-rule: implements assignment. A port i is left at the top of S along with a computed integer m (in the form (m, i)). The result of the assignment operation is unit
() but the value of the cell with incoming port x is updated to m.
The l -rule: implements linking. At the top of S there is a port x (tagged as l(i)). The
operation returns (), like assignment, but the outgoing port of the cell pointed at
by port i is reassigned to the second argument i of a.
The i f -rule: depending on the previous pass rule, if the token is sent to the first
branch the second branch is disconnected by linking the port to a weakening, and
vice-versa. In both cases the node if is removed.
Finally, copying rules are given in figure 11.

12: 16

## PDF page 17

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
The Cc rule: combines two consecutive m-ary and n-ary contraction nodes in a single

m + n-ary contraction node.
The C rule: (for a node X ̸= C ) resets the f flag. This is not a ‘pass’ rule, even though

the underlying graph does not change, because the token stays put. This happens
with some other rules for contraction.
The C-! rule: removes redundant ‘unary’ contractions.
The X-! rule: (for a node x ̸= C ) resets the f flag.
The δ rule: is the the main rule of the contraction node, and it leads to the copying
of the box just above it. Note that this is the main purpose of boxes, to delimit
copyable sub-graphs for copying by the contraction node.
The µ-rule: is not a contraction rule, but it is very similar. It represents the ‘unfolding’
of a recursive call by copying the body G .
3.6 Dataflow computation

In contrast to the graphs representing programs, graphs representing dataflow are
much simpler and includes only nodes for operators ($), if statements, and dereferencing (d). The pass and rewrite rules are given in table 2. To indicate the datflow-mode
for operators the flag g is placed at the top of the stack.
The d pass rule: represents the dereferencing operator, which records on the stack S
the value n stored at a cell i .
The $-operator pass rule: picks up the values of the branches m, n from the top of the
stack and replace them with the value of the operator as applied to them $ m n.
The tags x, y ∈ {−, g} but at least one should be g . This is because we want to mix
constant nodes into the dataflow graph, and they result in a − tag, whereas cells
result in a g tag. If both of them are − it means that there is a sub-graph made just
of constants, which should have been evaluated during graph construction.
The if pass rule: implements the behaviour of branching in the datflow graph. Unlike
an if statement in the graph-construction mode, which chooses one branch, in
dataflow mode both branches are evaluated and only one value is selected, as seen
in the final two rules, where X , Y represent any element of the stack.
Additionally, some of the pass rules from table 1 apply to dataflow computation as
well, unchanged (namely constants n, cells {n}, operators ω, if ↑ and !).
The if-rule for dataflow is inefficient, but it is required for soundness because of
conditional graph constructions. Consider the code:
let x = ref 1 in ref(if x < 2 then f 3 else f 4)

If only one side is evaluated then when x is possibly changed to 2 then f 4 would
need to be evaluated. So instead of rewriting the if node, because it is part of a
dataflow graph, it is left in the dataflow graph under the proviso that we always
need to evaluate both sides. An optimised version of the rule which only evaluates
one branch could be written, but it is more complicated. Moreover, the inefficiencies
introduced here do not change the asymptotic complexity of graph evaluation, as will
be seen shortly.

12: 17

## PDF page 18

Transparent Synchronous Dataflow
Table 2 Dataflow rules

node

e

d

f

S

d
$
if
if
if
if
$

o0
o0
o0
o0
o2
o2
i0

↓
↓
↓
↓
↓
↓
↓

□
$
□
□
□
□
$

(n, i):S
(m, x) : (n, y):S
(0, g):S
(n ̸= 0, g):S
X : Y : if0 :S
X : Y : if1 :S
(n, g):S

7→

e

d

f

S

i0
i0
o1
o1
i0
i0
i0

↓
↓
↑
↑
↓
↓
↓

□
$
□
□
□
□
□

(n, g):S
($ m n, g):S
⋆ : if0 :S
⋆ : if1 :S
X :S
Y :S
(n, g):S

For evaluating dataflow graphs we use a different set of tokens called prop-tokens.
Each such evaluation starts with an initial set of initial prop tokens and concludes
with a set of final prop tokens.
Definition 3.3 (Initial prop-tokens). We define the set of initial prop tokens Init P
as {(e0 , ↑, □, ⋆ : □, □), ...(en , ↑, □, ⋆ : □, □)}, where {e0 ...en } is the set of outputs of all
{n}-nodes in the graph.
Definition 3.4 (Final prop-tokens). We define the set of final prop tokens Final P (X⃗ )
as {(e0 , ↓, □, X 0 : □, □)...(en , ↓, □, X n : □, □)}, where {e0 ...en } is the set of outputs of all
{n}-nodes in the graph, X⃗ = {X 0 , ..., X n } and X 0 , ..., X n are elements of the computation
stack.
When the token hits a step node, the machine switches from evaluation mode to
propagation mode.
Definition 3.5 (Mode switching). We define the following special transitions:
1. (G, (e, ↑, □, ⋆ : S, B), ;) 7→ (G, (e, ↑, sp, ⋆ : S, B), Init P ) triggering the propagation
when e is the incoming port of an s-node , and
2. (G, (e, ↑, sp, ⋆ : S, B), Final P (X⃗ )) 7→s (G ′ , (e, ↓, s, (b, −) : S, B), ;) terminating the propagation as follows: for any {n}-node in G , let the return value of the eval token
sitting on its output be (n′ , x), then if n ̸= n′ , the {n}-node is updated to {n′ } in G ′ .
The value of b is 1 if there are updates and 0 otherwise where 1, 0 ∈ Int.
Definition 3.6 (Propagations). We define a propagation as any transition from (G, δ, P)
picking any non-final prop token to proceed using any possible transitions.
Definition 3.7 (Initial and final states). For any graph G : Λ → Γ , any e ∈ dom(Λ)
and any element X in the computation stack, we define the initial states and final
states as Init(G, e) = (G, e, ↑, □, ⋆ : □, □, ;) and Final(G, e, X ) = (G, e, ↓, □, X : □, □, ;)
respectively.
The DGOI machine executes terms by encoding them into computation graphs
according to the definitions in figure 8, where the translation of a well-typed term,
is denoted by JΓ ⊢ t : τK. An execution is any sequence of transitions starting from
the initial state. An execution is said to terminate if the execution ends with the final

12: 18

## PDF page 19

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

state, i.e. Init(G, r) 7→∗ Final(G ′ , r, X ) for some G ′ , X . An execution is said to be safe if
it terminates or at any state there is an applicable rule. They are formally defined in
appendix D.10.
Much like the language itself, the graph-rewriting semantics is bi-modal,
with pass and rewrite rules. The pass rules, even though they do not change the
underlying graph, can still change the token. By inspecting the value of the token the
semantics realises a kind of novel “semantic contextualisation” which allows certain
rules to be applied in a different way depending on the execution history of the
program. For example, operators can have either a pass or a rewriting semantics
depending on the data in the token, which records whether the operator must be
reduced or kept into a DFG graph. This is the “secret sauce” which allows operators
to behave in a contextual way without resorting to any syntactic trickery.
Remark.

3.7 Overview of type soundness proofs

In the Appendix we prove a basic theorem of the calculus, namely the Type Soundness
Theorem which states that a well-typed program will not crash.
Theorem 3.1 (Type soundness). Let G : {r : JτK} → ; = J⊢ t : τK for some closed welltyped term ⊢ t : τ. (1) If t is recursion-free then any execution from Init(G, r) terminates.
(2) Otherwise, the execution of t is at least safe.
In order to prove (1) termination, we first identify a special form of graph, dataflow
graph. Any execution that runs on them will always terminate and the graph will
remain unchanged since no rewrite ever happens. Throughout the execution, any cell
will always be connected to a dataflow graph because of the nature of call-by-value.
Therefore step-propagation always terminates and is confluent. As a result, all the
non-deterministic propagation sequences can be seen as one single transition and
thus making the machine deterministic. After that we can prove termination by using
induction on type derivation. As for (2) safety, the proof is simply a case analysis on
possible states. All the proof details can be found in appendices D.1 to D.10.
Given the formulation of the semantics as an abstract machine we can immediately
conclude that:
Theorem 3.2 (Efficiency). The following operations can be executed in linear time on the
depth of the dataflow graph: cell creation, dereferencing, peeking, linking, assignment,
root. The step operation can be executed in linear time on the depth of the dataflow
graph and on the number of cells.
3.8 A non-trivial example

We conclude with a non-trivial example, computing a stream of prime numbers
using the sieve of Eratosthenes. The code is in listing 1 and can be executed in the
visualiser.3 It is interesting to contrast our code with the same program implemented
3

https://cwtsteven.github.io/TSD-visual?ex=primes

12: 19

## PDF page 20

Transparent Synchronous Dataflow

Listing 1

A stream of prime numbers

1 let fromn = λn.let s = ref n in link s (s + 1); deref s in
2 let filter = λinp. λn.i == n || ((i % n) <> 0) in
3 let inp = fromn 2 in
4 let sieve = ref (filter inp 2) in
5 let next = λ_. step; link sieve (root sieve && (filter inp (peek inp))) in
6 let delay = ref inp in
7 let primes = if deref sieve then delay else 0 in
8 next 0; peek primes; // return 2
9 next 0; peek primes; // return 3
10 next 0; peek primes // return 0
1

1
+

+

{3} inp

{2} inp

C

C

<latexit sha1_base64="vII7JJJ5Tz/+ZzKd9RB33qH+JfU=">AAACGHicbVDLSsNAFJ34rPUVdSO6GSyCq5JUQZcFNy4r2Ac0oUwmk3bozCTMTIQQCn6HH+BWP8GduHXnF/gbTtosbOuBgcM553LnniBhVGnH+bZWVtfWNzYrW9Xtnd29ffvgsKPiVGLSxjGLZS9AijAqSFtTzUgvkQTxgJFuML4t/O4jkYrG4kFnCfE5GgoaUYy0kQb2icdMOESQiqQeUaaJ9AruwcbArjl1Zwq4TNyS1ECJ1sD+8cIYp5wIjRlSqu86ifZzJDXFjEyqXqpIgvAYDUnfUIE4UX4+vWECz40SwiiW5gkNp+rfiRxxpTIemCRHeqQWvUL8z+unOrrxc3NSqonAs0VRyqCOYVEIDKkkWLPMEIQlNX+FeIQkwqaK+S1KcyQzGU5MM+5iD8uk06i7l/XG/VWteVx2VAGn4AxcABdcgya4Ay3QBhg8gRfwCt6sZ+vd+rA+Z9EVq5w5AnOwvn4Bm8igMw==</latexit>

<latexit sha1_base64="vII7JJJ5Tz/+ZzKd9RB33qH+JfU=">AAACGHicbVDLSsNAFJ34rPUVdSO6GSyCq5JUQZcFNy4r2Ac0oUwmk3bozCTMTIQQCn6HH+BWP8GduHXnF/gbTtosbOuBgcM553LnniBhVGnH+bZWVtfWNzYrW9Xtnd29ffvgsKPiVGLSxjGLZS9AijAqSFtTzUgvkQTxgJFuML4t/O4jkYrG4kFnCfE5GgoaUYy0kQb2icdMOESQiqQeUaaJ9AruwcbArjl1Zwq4TNyS1ECJ1sD+8cIYp5wIjRlSqu86ifZzJDXFjEyqXqpIgvAYDUnfUIE4UX4+vWECz40SwiiW5gkNp+rfiRxxpTIemCRHeqQWvUL8z+unOrrxc3NSqonAs0VRyqCOYVEIDKkkWLPMEIQlNX+FeIQkwqaK+S1KcyQzGU5MM+5iD8uk06i7l/XG/VWteVx2VAGn4AxcABdcgya4Ay3QBhg8gRfwCt6sZ+vd+rA+Z9EVq5w5AnOwvn4Bm8igMw==</latexit>

inp.f ilter inp 2

<latexit sha1_base64="8xdfSfN5KA2l4OoJfWiLZo225MM=">AAACA3icbVDLSsNAFL3xWesr6kZ0M1gEVyFpBV0W3LisYB/QhDKZTNqhkwczE6GEght/xY0LRdz6E+78GydtFtp6YOBwzrncucdPOZPKtr+NldW19Y3NylZ1e2d3b988OOzIJBOEtknCE9HzsaScxbStmOK0lwqKI5/Trj++KfzuAxWSJfG9mqTUi/AwZiEjWGlpYJ64XIcDjFicWiHjigq34C5qDMyabdkzoGXilKQGJVoD88sNEpJFNFaEYyn7jp0qL8dCMcLptOpmkqaYjPGQ9jWNcUSll89umKJzrQQoTIR+sUIz9fdEjiMpJ5GvkxFWI7noFeJ/Xj9T4bWX65MyRWMyXxRmHKkEFYWggAlKFJ9ogolg+q+IjLDARFchq7oEZ/HkZdKpW07Dqt9d1prHZR0VOIUzuAAHrqAJt9CCNhB4hGd4hTfjyXgx3o2PeXTFKGeO4A+Mzx/I4JbT</latexit>

inp.f ilter inp 3

inp.f ilter inp 2
&

sieve {t}

{2} delay

0

sieve {t}

if

0

if

primes

Figure 12

{2} delay

primes

before and after next()

in a similar language, Lucid Synchrone 4 (appendix B). The main distinction is that we
use imperative commands to set up the dataflow graph, whereas in Lucid Synchrone
co-recursive stream equations are used to the same purpose. It is a matter of preference
which one of the two versions are seen as more accessible.
In listing 1, the function fromn takes an integer n and creates a stream of integers
from n. The function filter takes an input stream inp and an integer n and creates a
stream of booleans that could filter out the multiples of n (except for n itself) and
anything smaller than n from inp. This filter function is meant to create the different
layers of sieve that are used in generating prime numbers.
To implement the sieve of Eratosthenes, we first start with an input stream using
fromn 2 (named inp). A cell is then initialised with the first layer filter inp 2. The
sieve needs to expand by adding new layers of sieve in every step, without rewriting
the dataflow graph. The solution is to use the function next which unfolds a layer
after each step as shown in figure 12. Finally since sieve is a cell that depends on inp
meaning that it is always one step behind inp and thus primes = if sieve then inp else 0
would not gives the correct stream. Instead we need to create a delayed stream from
inp (delay = ref inp) in order to synchronise the input of primes, i.e. primes = if sieve
then delay else 0. Table 3 shows the first few elements of each stream.

4

https://www.di.ens.fr/~pouzet/lucid-synchrone/manual_html/manual015.html

12: 20

## PDF page 21

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
Table 3 Streams of the sieve program

4

step

0

1

2

3

4

5

6

7

···

inp
sieve
delay
primes

2
t
2
2

3
t
2
2

4
t
3
3

5
f
4
0

6
t
5
5

7
f
6
0

8
t
7
7

9
f
8
0

···
···
···
···

Experimental implementation

We have proved that TSD is efficient “in principle” by examining its abstract machine
execution. But we also want to gather some practical evidence that the mechanism
we propose is not hopelessly inefficient. For that, we implement the calculus as a
library module for OCaml (TSD), together with a PPX language extension.5 The library
serves as an embedded DSL, which is blended into the host language more seamlessly
via the language extension. Note that the semantics defined earlier is used as a
specification, and is not realised faithfully by the implementation. As such, the OCaml
implementation does not benefit fully from the potential to seamlessly integrate the
DFG and functional syntax and semantics. A full implementation based directly on
the abstract machine is a more substantial endeavour which we leave as further work.
Details of the implementation are in appendix C, where we also give comparisons
between TSD and related programming languages, both in terms of programming
style and in terms of benchmarks (appendix C.1).

5

Related work

The broadest context of our work is dataflow programming, which has been extensively studied ([31] is a relatively recent, exhaustive survey). Besides the numerous
FRP frameworks, some of the ideas we present here are particularly prominent in
functional hardware-description languages which allow (meta) programming synchronous dataflow, including in a transparent style if so desired [5]. Advances in
dataflow programming materialised into the success of notable languages such as
Lucid [53] or Lustre [28], but the influence of the dataflow style of programming was
far broader, as seen for example in the popular machine-learning library TensorFlow,
which is presented commonly as a embedded domain specific dataflow language
(EDSL) in Python [1].
We are particularly concerned with dataflow programming in a functional style, the so-called functional reactive programming [18,
30, 47, 54] which proved to be especially well suited for Haskell because of its lazy
style of computation, its expressive type system, and syntactic features which allows
the convenient design and implementation of EDSLs ([8] is a recent textbook).
Functional reactive programming

5

https://github.com/cwtsteven/TSD

12: 21

## PDF page 22

Transparent Synchronous Dataflow

FrTime [15] is a functional reactive programming language embedded into Scheme.
It also provides transparent graph creation by inserting code for operators such as
{+, -} to check in runtime if their arguments are signals or ordinary Scheme values.
This makes use of the fact that Scheme is dynamically typed. The graph creation
mechanism in TSD is very much similar but the choice of creating a graph or to
create a normal constant is captured in the rewriting rules of the node instead. It
can be seen as one of the implementation techniques of transparent graph creation.
There is also a difference to the model of change propagation between them. FrTime
embraces a push-driven implementation where signal changes are pushed to the
dataflow network immediately. On the contrary, TSD can be seen as a mixed of
push and pull implementation. For immediate dependency (without cells) they are
pull-driven and their values are recomputed on demand. Whereas for cells, they
will be updated via step which is push-driven. By having explicit step command and
pull-driven immediate dependencies, we avoid the glitch problem that arises in all
push-driven implementations. Flapjax [42] is another FRP language based on FrTime
but it is embedded into JavaScript. AmbientTalk/R [11] is another push-based reactive
programming framework similar to FrTime that is built on top of AmbientTalk. Like
FrTime, expressions in AmbientTalk/R are implicitly lifted such that graphs are created
transparently. AmbientTalk/R also supports distributed reactive programming where
reactive values can be distributed in various hosts. We are also interested in designing
a distributed model for TSD where cells can be allocated in different machines but
this is left for further investigation.
REScala [52] is an EDSL built on top of Scala that bridges between object-oriented
and function style in reactive programming. It provides two abstractions for reactive
programming, signals and events. The input of dataflow graph in REScala is called
a Var which can be set or transform to other values. Signals are created using Vars
and other signals. Whereas in TSD, cells are not just the input of a graph but it also
represents a state in the graph. The dependency of cells can also be reconfigured
using link which allows the graph to be cyclic. On the other hand, cyclic dependencies
will lead to runtime error in REScala. Moreover, change propagation in REScala is
also push-based.
A somewhat parallel but relevant line of research is the use of temporal type systems
to restrict reactive computation to (space) efficient programs [33, 34, 35]. In this
approach the type of streams remains exposed, so the programmer can write more
expressive, lower-level (in the sense of controlling events and streams) programs,
but such programs must conform to a typing discipline which guarantees certain
space-utilisation constraints. In contrast, our approach is higher-level — less expressive
but more convenient for the unsophisticated programmer. In TSD the complexity
is pushed down to the level of the abstract machine, whereas in loc. cit. a complex
temporal typing discipline is imposed on a conventional operational semantics.
Self-adjusting computation has been introduced by Acar [3]
and studied extensively in recent years. The use of SAC as a transparent dataflow
idiom, which features quite prominently in our motivating introduction, has not been
studied formally, although it has been mentioned [29] and it has been extensively
Self-adjusting computation

12: 22

## PDF page 23

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

discussed in informal fora.6 In terms of implementation, SAC is a good match for
incremental computation [49], which is a sophisticated memoisation infrastructure
which allows the re-evaluation of expressions that need to be re-evaluated, thus saving
computation (see also [50] for a survey). As most optimisations, incremental computation relies on a trade-off between saving the cost of unnecessary re-evaluations
on the one hand versus maintaining the memoisation infrastructure, which is not
free [10]. We are providing two implementations, incremental and non-incremental,
and indeed the performance gains are quite dependent on the particular application.
Also related is the significant body of work on
synchronous dataflow programming languages and their semantics (e.g. Esterel [7])
and in particular functional languages (e.g. Lucid Synchrone [13], a functional version
of Lustre [28]). These are the most similar languages to TSD, with some significant
distinctions: TSD constructs the dataflow model using imperative features, and it
does not aim at real-time execution, so it does not employ a clock calculus. Also,
TSD dataflow graphs are productive by construction, since cyclic links can only be
constructed via cells. So productivity checks are not necessary.
RML [41] is a low level synchronous extension to OCaml, consisting of a set of
primitives for sending and handling messages. We say ‘low level’ because it is very easy
to write unsafe programs in RML, e.g. two processes waiting for each other to emit a
signal. Reactive ML has in common with the TSD language the fact that they build
on the ML language, as a stand-alone compiler in their case versus a PPX extension
in ours. Our work is conceptually related to such languages in the way that SAC is
related to (asynchronous) FRP.
Synchronous dataflow languages

The DGOIM is a graph-rewriting system based on the Geometry of Interaction (GOI) [25], an interpretation of proofs in linear logic as proof
nets [26]. The GOI was formulated as a compositional operational semantics of communicating transducers and used to interpret higher-order functional programming
languages [39]. The GOI approach turned out to be particularly useful for compiling
conventional languages to unconventional architectures (such as reconfigurable circuits [23], distributed [21], or quantum architectures [36]). It has also been used to
give strikingly space-efficient compilation schemes [38] and improved time-efficiency
by incorporating graph rewriting in addition to token-passing [19, 20]. The extension of the GOI machine with simple rewriting rules, the so-called Dynamic GOI
machine has allowed the definition of an efficient (space and time) abstract machine
for CBN, CBV and lazy (a la Haskell) evaluations [45]. This flexibility and uniformity
in representing several evaluation strategies in the same machine allows a natural
specification for languages that require it, such as TSD. Moreover, the computational
intuitions of the approach combine seamlessly dataflow and higher-order features,
making it suitable for the study of languages that require it, such as TensorFlow [14,
44].
Geometry of interaction

6

See e. g. https://blog.janestreet.com/introducing-incremental/

12: 23

## PDF page 24

Transparent Synchronous Dataflow

6

Conclusion

In this paper we have introduced a new programming idiom, transparent synchronous
dataflow programming (TSD). This programming idiom is natural, allowing a highlevel of abstraction to be applied to useful synchronous algorithms.
We define TSD using the relatively new diagrammatic operational style of tokenguided graph rewriting. Although inspired by the Geometry of Interaction this dynamic
mechanism is in many a significant departure from the strictures of GOI. It is arguably
intuitive, as the graphical formalism is a natural setting for the study of dataflow,
which it neatly extends with higher-order features. Moreover, it has certain technical
advantages, such as the fine-grained management of sharing or the decomposition of
big syntactic reduction rules into atomic graph manipulations.
The calculus TSD restricts cells to ground type. In order for multi-token (parallel)
propagation to work dataflow graphs must be also pure in the sense that no rewrites
are possible. Our solution is to prevent the presence of lambda-nodes in computation
graphs. This is done for the sake of simplicity. We already know that DGOIM can be
used to give CBN evaluation on a fixed graph including lambda-nodes, so an extension
to higher-order TSD is likely to be possible. On the other hand, extensions with effects
are more problematic as the extension of DGOIM with effects, in general, is a matter
of active research.
Our PPX language extension to OCaml implementing the calculus does not take
advantage of parallel evaluation of propagation or optimisation beyond basic incrementalisation. It is mainly a proof-of-concept implementation that shows that the
ideas are implementable (even naively). But efficient implementations are high on
our agenda.
Acknowledgements

The authors want to thank Neel Krishnaswami for discussions

and encouragement.

References

[1] Martín Abadi, Paul Barham, Jianmin Chen, Zhifeng Chen, Andy Davis, Jeffrey Dean, Matthieu Devin, Sanjay Ghemawat, Geoffrey Irving, Michael Isard,
Manjunath Kudlur, Josh Levenberg, Rajat Monga, Sherry Moore, Derek Gordon Murray, Benoit Steiner, Paul A. Tucker, Vijay Vasudevan, Pete Warden,
Martin Wicke, Yuan Yu, and Xiaoqiang Zheng. “TensorFlow: A System for
Large-Scale Machine Learning”. In: 12th USENIX Symposium on Operating Systems Design and Implementation, OSDI 2016, Savannah, GA, USA, November 2-4,
2016. Edited by Kimberly Keeton and Timothy Roscoe. USENIX Association,
2016, pages 265–283. url: https://www.usenix.org/conference/osdi16/technicalsessions/presentation/abadi.
[2] Umut A. Acar, Amal Ahmed, and Matthias Blume. “Imperative self-adjusting
computation”. In: Proceedings of the 35th ACM SIGPLAN-SIGACT Symposium
on Principles of Programming Languages, POPL 2008, San Francisco, California,

12: 24

## PDF page 25

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

USA, January 7-12, 2008. Edited by George C. Necula and Philip Wadler. ACM,
2008, pages 309–322. doi: 10.1145/1328438.1328476.
[3] Umut A. Acar, Matthias Blume, and Jacob Donham. “A consistent semantics of
self-adjusting computation”. In: Journal of Functional Programming 23.3 (2013),
pages 249–292. doi: 10.1017/S0956796813000099.
[4] Beniamino Accattoli. “The Complexity of Abstract Machines”. In: Proceedings
Third International Workshop on Rewriting Techniques for Program Transformations and Evaluation, WPTE@FSCD 2016, Porto, Portugal, 23rd June 2016. 2016,
pages 1–15. doi: 10.4204/EPTCS.235.1.
[5] Christiaan Baaij, Matthijs Kooijman, Jan Kuper, Arjan Boeijink, and Marco
Gerards. “C?aSH: Structural Descriptions of Synchronous Hardware Using
Haskell”. In: 13th Euromicro Conference on Digital System Design, Architectures,
Methods and Tools, DSD 2010, 1-3 September 2010, Lille, France. Edited by
Sebastián López. IEEE Computer Society, 2010, pages 714–721. doi: 10.1109/
DSD.2010.21.
[6] Atilim Gunes Baydin, Barak A. Pearlmutter, Alexey Andreyevich Radul, and
Jeffrey Mark Siskind. “Automatic Differentiation in Machine Learning: a Survey”. In: Journal of Machine Learning Research 18 (2017), 153:1–153:43. url:
http://jmlr.org/papers/v18/17-468.html.
[7] Gérard Berry and Laurent Cosserat. “The ESTEREL Synchronous Programming Language and its Mathematical Semantics”. In: Seminar on Concurrency,
Carnegie-Mellon University, Pittsburg, PA, USA, July 9-11, 1984. Edited by Stephen
D. Brookes, A. W. Roscoe, and Glynn Winskel. Volume 197. Lecture Notes in
Computer Science. Springer, 1984, pages 389–448. doi: 10.1007/3-540-156704_19.
[8] Stephen Blackheath and Anthony Jones. Functional reactive programming. Manning Publications Company, 2016. isbn: 978-1-63343-010-5.
[9] Sylvain Boulmé and Grégoire Hamon. “Certifying Synchrony for Free”. In:
Logic for Programming, Artificial Intelligence, and Reasoning, 8th International
Conference, LPAR 2001, Havana, Cuba, December 3-7, 2001, Proceedings. 2001,
pages 495–506. doi: 10.1007/3-540-45653-8_34.
[10] Sebastian Burckhardt, Daan Leijen, Caitlin Sadowski, Jaeheon Yi, and Thomas
Ball. “Two for the price of one: a model for parallel and incremental computation”. In: Proceedings of the 26th Annual ACM SIGPLAN Conference on
Object-Oriented Programming, Systems, Languages, and Applications, OOPSLA
2011, part of SPLASH 2011, Portland, OR, USA, October 22 - 27, 2011. Edited by
Cristina Videira Lopes and Kathleen Fisher. ACM, 2011, pages 427–444. doi:
10.1145/2048066.2048101.
[11] Andoni Lombide Carreton, Stijn Mostinckx, Tom Van Cutsem, and Wolfgang De
Meuter. “Loosely-Coupled Distributed Reactive Programming in Mobile Ad
Hoc Networks”. In: Objects, Models, Components, Patterns, 48th International
Conference, TOOLS 2010, Málaga, Spain, June 28 - July 2, 2010. Proceedings.

12: 25

## PDF page 26

Transparent Synchronous Dataflow

Edited by Jan Vitek. Volume 6141. Lecture Notes in Computer Science. Springer,
2010, pages 41–60. doi: 10.1007/978-3-642-13953-6_3.
[12] Paul Caspi, Daniel Pilaud, Nicolas Halbwachs, and John Plaice. “Lustre: A
Declarative Language for Programming Synchronous Systems”. In: Conference
Record of the Fourteenth Annual ACM Symposium on Principles of Programming
Languages, Munich, Germany, January 21-23, 1987. 1987, pages 178–188. doi:
10.1145/41625.41641.
[13] Paul Caspi and Marc Pouzet. “Synchronous Kahn Networks”. In: Proceedings of
the 1996 ACM SIGPLAN International Conference on Functional Programming,
ICFP 1996, Philadelphia, Pennsylvania, USA, May 24-26, 1996. Edited by Robert
Harper and Richard L. Wexelblat. ACM, 1996, pages 226–238. doi: 10.1145/
232627.232651.
[14] Steven Cheung, Victor Darvariu, Dan R. Ghica, Koko Muroya, and Reuben
N. S. Rowe. “A Functional Perspective on Machine Learning via Programmable
Induction and Abduction”. In: Functional and Logic Programming - 14th International Symposium, FLOPS 2018, Nagoya, Japan, May 9-11, 2018, Proceedings.
2018, pages 84–98. doi: 10.1007/978-3-319-90686-7_6.
[15] Gregory H. Cooper and Shriram Krishnamurthi. “Embedding Dynamic Dataflow
in a Call-by-Value Language”. In: Programming Languages and Systems, 15th
European Symposium on Programming, ESOP 2006, Held as Part of the Joint
European Conferences on Theory and Practice of Software, ETAPS 2006, Vienna,
Austria, March 27-28, 2006, Proceedings. Edited by Peter Sestoft. Volume 3924.
Lecture Notes in Computer Science. Springer, 2006, pages 294–308. doi: 10.
1007/11693024_20.
[16] James B Dabney and Thomas L Harman. Mastering simulink. Pearson, 2004.
isbn: 978-0-13-017085-9.
[17] Vincent Danos and Laurent Regnier. “Reversible, Irreversible and Optimal
lambda-Machines”. In: Theoretical Computer Science 227.1-2 (1999), pages 79–
97. doi: 10.1016/S0304-3975(99)00049-3.
[18] Conal Elliott and Paul Hudak. “Functional Reactive Animation”. In: Proceedings
of the 1997 ACM SIGPLAN International Conference on Functional Programming
(ICFP ’97), Amsterdam, The Netherlands, June 9-11, 1997. Edited by Simon
L. Peyton Jones, Mads Tofte, and A. Michael Berman. ACM, 1997, pages 263–
273. doi: 10.1145/258948.258973.
[19] Maribel Fernández and Ian Mackie. “Call-by-Value lambda-Graph Rewriting
Without Rewriting”. In: Graph Transformation, First International Conference,
ICGT 2002, Barcelona, Spain, October 7-12, 2002, Proceedings. Edited by Andrea Corradini, Hartmut Ehrig, Hans-Jörg Kreowski, and Grzegorz Rozenberg.
Volume 2505. Lecture Notes in Computer Science. Springer, 2002, pages 75–89.
doi: 10.1007/3-540-45832-8_8.

12: 26

## PDF page 27

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

[20] Maribel Fernández and Ian Mackie. “From Term Rewriting to Generalised
Interaction Nets”. In: Programming Languages: Implementations, Logics, and
Programs, 8th International Symposium, PLILP’96, Aachen, Germany, September
24-27, 1996, Proceedings. Edited by Herbert Kuchen and S. Doaitse Swierstra.
Volume 1140. Lecture Notes in Computer Science. Springer, 1996, pages 319–
333. doi: 10.1007/3-540-61756-6_94.
[21] Olle Fredriksson and Dan R. Ghica. “Seamless Distributed Computing from the
Geometry of Interaction”. In: Trustworthy Global Computing - 7th International
Symposium, TGC 2012, Newcastle upon Tyne, UK, September 7-8, 2012, Revised
Selected Papers. Edited by Catuscia Palamidessi and Mark Dermot Ryan. Volume 8191. Lecture Notes in Computer Science. Springer, 2012, pages 34–48.
doi: 10.1007/978-3-642-41157-1_3.
[22] Felix A. Gers, Jürgen Schmidhuber, and Fred A. Cummins. “Learning to Forget: Continual Prediction with LSTM”. In: Neural Computation 12.10 (2000),
pages 2451–2471. doi: 10.1162/089976600300015015.
[23] Dan R. Ghica. “Geometry of synthesis: a structured approach to VLSI design”.
In: Proceedings of the 34th ACM SIGPLAN-SIGACT Symposium on Principles of
Programming Languages, POPL 2007, Nice, France, January 17-19, 2007. Edited
by Martin Hofmann and Matthias Felleisen. ACM, 2007, pages 363–375. doi:
10.1145/1190216.1190269.
[24] Dan R. Ghica, Koko Muroya, and Todd Waugh Ambridge. “Local Reasoning for
Robust Observational Equivalence”. 2019. arXiv: 1907.01257 [cs.PL].
[25] Jean-Yves Girard. “Geometry of Interaction 1: Interpretation of System F”.
In: Logic Colloquium ’88. Edited by R. Ferro, C. Bonotto, S. Valentini, and A.
Zanardo. Volume 127. Studies in Logic and the Foundations of Mathematics.
Elsevier, 1989, pages 221–260. doi: 10.1016/S0049-237X(08)70271-4.
[26] Jean-Yves Girard. “Linear Logic: its syntax and semantics”. In: Advances in Linear
Logic. Edited by Jean-Yves Girard, Yves Lafont, and LaurentEditors Regnier.
London Mathematical Society Lecture Note Series. Cambridge University Press,
1995, pages 1–42. doi: 10.1017/CBO9780511629150.002.
[27] Andreas Griewank. “On automatic differentiation”. In: Mathematical Programming: recent developments and applications. KTK Scientific, 1989, pages 83–107.
isbn: 978-0-7923-0490-6.
[28] Nicolas Halbwachs, Paul Caspi, Pascal Raymond, and Daniel Pilaud. “The
synchronous data flow programming language LUSTRE”. In: Proceedings of the
IEEE 79.9 (1991), pages 1305–1320. doi: 10.1109/5.97300.
[29] Matthew A. Hammer, Khoo Yit Phang, Michael Hicks, and Jeffrey S. Foster.
“Adapton: Composable, Demand-driven Incremental Computation”. In: Proceedings of the 35th ACM SIGPLAN Conference on Programming Language Design and
Implementation. PLDI ’14. Edinburgh, United Kingdom: ACM, 2014, pages 156–
166. isbn: 978-1-4503-2784-8. doi: 10.1145/2594291.2594324.

12: 27

## PDF page 28

Transparent Synchronous Dataflow

[30] Paul Hudak, Antony Courtney, Henrik Nilsson, and John Peterson. “Arrows,
Robots, and Functional Reactive Programming”. In: Advanced Functional Programming, 4th International School, AFP 2002, Oxford, UK, August 19-24, 2002,
Revised Lectures. Edited by Johan Jeuring and Simon L. Peyton Jones. Volume 2638. Lecture Notes in Computer Science. Springer, 2002, pages 159–187.
doi: 10.1007/978-3-540-44833-4_6.
[31] Wesley M. Johnston, J. R. Paul Hanna, and Richard J. Millar. “Advances in
dataflow programming languages”. In: ACM Computing Surveys 36.1 (2004),
pages 1–34. doi: 10.1145/1013208.1013209.
[32] Aleks Kissinger. “Pictures of Processes. Automated Graph Rewriting for Monoidal
Categories and Applications to Quantum Computing”. PhD thesis. St. Catherine’s College, University of Oxford, 2011. arXiv: 1203.0202 [math.CT].
[33] Neelakantan R. Krishnaswami. “Higher-order functional reactive programming
without spacetime leaks”. In: ACM SIGPLAN International Conference on Functional Programming, ICFP’13, Boston, MA, USA - September 25 - 27, 2013. 2013,
pages 221–232. doi: 10.1145/2500365.2500588.
[34] Neelakantan R. Krishnaswami and Nick Benton. “A semantic model for graphical
user interfaces”. In: Proceeding of the 16th ACM SIGPLAN international conference
on Functional Programming, ICFP 2011, Tokyo, Japan, September 19-21, 2011.
2011, pages 45–57. doi: 10.1145/2034773.2034782.
[35]

Neelakantan R. Krishnaswami, Nick Benton, and Jan Hoffmann. “Higher-order
functional reactive programming in bounded space”. In: Proceedings of the 39th
ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages,
POPL 2012, Philadelphia, Pennsylvania, USA, January 22-28, 2012. 2012, pages 45–
58. doi: 10.1145/2103656.2103665.

[36] Ugo Dal Lago, Claudia Faggian, Benoît Valiron, and Akira Yoshimizu. “The
geometry of parallelism: classical, probabilistic, and quantum effects”. In: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming
Languages, POPL 2017, Paris, France, January 18-20, 2017. 2017, pages 833–845.
doi: 10.1145/3009837.3009859.
[37] Hai Liu and Paul Hudak. “Plugging a Space Leak with an Arrow”. In: Electronic
Notes in Theoretical Computer Science 193 (2007), pages 29–45. doi: 10.1016/j.
entcs.2007.10.006.
[38] Ian Mackie. “Efficient lambda-Evaluation with Interaction Nets”. In: Rewriting
Techniques and Applications, 15th International Conference, RTA 2004, Aachen,
Germany, June 3-5, 2004, Proceedings. Edited by Vincent van Oostrom. Volume 3091. Lecture Notes in Computer Science. Springer, 2004, pages 155–169.
doi: 10.1007/978-3-540-25979-4_11.
[39] Ian Mackie. “The Geometry of Interaction Machine”. In: Conference Record of
POPL’95: 22nd ACM SIGPLAN-SIGACT Symposium on Principles of Programming
Languages, San Francisco, California, USA, January 23-25, 1995. 1995, pages 198–
208. doi: 10.1145/199448.199483.

12: 28

## PDF page 29

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

[40] Louis Mandel, Florence Plateau, and Marc Pouzet. “Lucy-n: a n-Synchronous
Extension of Lustre”. In: Mathematics of Program Construction. Edited by Claude
Bolduc, Jules Desharnais, and Béchir Ktari. Berlin, Heidelberg: Springer Berlin
Heidelberg, 2010, pages 288–309. isbn: 978-3-642-13321-3.
[41] Louis Mandel and Marc Pouzet. “ReactiveML: a reactive extension to ML”. In:
Proceedings of the 7th International ACM SIGPLAN Conference on Principles and
Practice of Declarative Programming, July 11-13 2005, Lisbon, Portugal. Edited
by Pedro Barahona and Amy P. Felty. ACM, 2005, pages 82–93. doi: 10.1145/
1069774.1069782.
[42] Leo A. Meyerovich, Arjun Guha, Jacob P. Baskin, Gregory H. Cooper, Michael
Greenberg, Aleks Bromfield, and Shriram Krishnamurthi. “Flapjax: a programming language for Ajax applications”. In: Proceedings of the 24th Annual ACM
SIGPLAN Conference on Object-Oriented Programming, Systems, Languages, and
Applications, OOPSLA 2009, October 25-29, 2009, Orlando, Florida, USA. Edited
by Shail Arora and Gary T. Leavens. ACM, 2009, pages 1–20. doi: 10.1145/
1640089.1640091.
[43] Yaron Minsky. Introducing Incremental. Jane Street Tech Blog. July 2015. url:
https://blog.janestreet.com/introducing-incremental/ (visited on 2019-05).
[44] Koko Muroya, Steven W. T. Cheung, and Dan R. Ghica. “The Geometry of
Computation-Graph Abstraction”. In: Proceedings of the 33rd Annual ACM/IEEE
Symposium on Logic in Computer Science, LICS 2018, Oxford, UK, July 09-12,
2018. Edited by Anuj Dawar and Erich Grädel. ACM, 2018, pages 749–758. doi:
10.1145/3209108.3209127.
[45] Koko Muroya and Dan R. Ghica. “The Dynamic Geometry of Interaction Machine: A Call-by-Need Graph Rewriter”. In: 26th EACSL Annual Conference on
Computer Science Logic, CSL 2017, August 20-24, 2017, Stockholm, Sweden. 2017,
32:1–32:15. doi: 10.4230/LIPIcs.CSL.2017.32.
[46] Koko Muroya and Dan R. Ghica. “The Dynamic Geometry of Interaction Machine: A Token-Guided Graph Rewriter”. In: Logical Methods in Computer
Science 15.4 (2019). url: https://lmcs.episciences.org/5882.
[47] Henrik Nilsson, Antony Courtney, and John Peterson. “Functional Reactive
Programming, Continued”. In: Proceedings of the 2002 ACM SIGPLAN Workshop
on Haskell. Haskell ’02. Pittsburgh, Pennsylvania: Association for Computing
Machinery, 2002, pages 51–64. isbn: 1-58113-605-6. doi: 10.1145/581690.581695.
[48] Gordon D. Plotkin. “LCF Considered as a Programming Language”. In: Electronic
Notes in Theoretical Computer Science 5.3 (1977), pages 223–255. doi: 10.1016/
0304-3975(77)90044-5.
[49] William Pugh and Tim Teitelbaum. “Incremental Computation via Function
Caching”. In: Conference Record of the Sixteenth Annual ACM Symposium on
Principles of Programming Languages, Austin, Texas, USA, January 11-13, 1989.
ACM Press, 1989, pages 315–328. doi: 10.1145/75277.75305.

12: 29

## PDF page 30

Transparent Synchronous Dataflow

[50] G. Ramalingam and Thomas W. Reps. “A Categorized Bibliography on Incremental Computation”. In: Conference Record of the Twentieth Annual ACM SIGPLANSIGACT Symposium on Principles of Programming Languages, Charleston, South
Carolina, USA, January 1993. Edited by Mary S. Van Deusen and Bernard Lang.
ACM Press, 1993, pages 502–510. doi: 10.1145/158511.158710.
[51] Boaz Ronen, Michael A. Palley, and Henry C. Lucas Jr. “Spreadsheet Analysis
and Design”. In: Communications of the ACM 32.1 (1989), pages 84–93. doi:
10.1145/63238.63244.
[52] Guido Salvaneschi, Gerold Hintz, and Mira Mezini. “REScala: bridging between object-oriented and functional style in reactive applications”. In: 13th
International Conference on Modularity, MODULARITY ’14, Lugano, Switzerland,
April 22-26, 2014. Edited by Walter Binder, Erik Ernst, Achille Peternier, and
Robert Hirschfeld. ACM, 2014, pages 25–36. doi: 10.1145/2577080.2577083.
[53]

William W. Wadge and Edward A. Ashcroft. LUCID, the Dataflow Programming
Language. USA: Academic Press Professional, Inc., 1985. isbn: 0-12-729650-6.

[54] Zhanyong Wan and Paul Hudak. “Functional reactive programming from first
principles”. In: Proceedings of the 2000 ACM SIGPLAN Conference on Programming Language Design and Implementation (PLDI), Vancouver, Britith Columbia,
Canada, June 18-21, 2000. Edited by Monica S. Lam. ACM, 2000, pages 242–252.
doi: 10.1145/349299.349331.

A

Program comparison with Lucid Synchrone and Zélus

Lets consider the example we give in the introduction, the sum of an alternating signal.
The example written in TSD is shown below:
1 let alt =
2 let state = ref 1 in
3 link state (1 - deref state); deref state
4 in
5
6 let sum = λinp.
7 let state = ref 0 in
8 link state (inp + deref state); deref state
9 in
10
11 let alt_sum = sum alt in ...

The Zélus implementation is remarkably similar:
1 let trans (s, i) = 1 - s
2 let node alt () = state where
3 rec state = 1 -> trans ((pre state), 0)
4
5 let plus (x, y) = x + y
6 let node sum inp = state where
7 rec state = 0 -> plus ((pre state), inp)

12: 30

## PDF page 31

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

8
9 let node alt_sum () = sum (alt ())
10 let node main () = alt_sum ()

The key distinction is the Zélus definition of the feedback loop via recursion, versus the TSD definition in which the same loop is created via assignment. Also, TSD
dataflow graphs are productive by construction, since cyclic links can only be constructed via cells. So productivity checks are not necessary.

B

Sieve of Eratosthenes in Lucid Synchrone

1 let node first x = v
2 where rec v = x fby v
3
4 let rec node sieve x =
5 let clock filter = (x mod (first x))<> 0
6 in merge filter
7
(sieve (x when filter))
8
(true fby false)
9
10 let node from n = o where rec o = n fby (o + 1)
11
12 let clock sieve = sieve (from 2)
13
14 let node primes () = (from 2) when sieve

C

Implementation

The cell is implemented as a reference storing the current value and a thunk representing the dataflow graph. The graph type corresponds to a term in the TSD calculus and
can either be a dependency Thunk, or a Cell. There is also a special if-then-else graph
IF_Thunk, as the behaviour of branching terms is different in the dataflow graph (both
branches are evaluated). The lift function embeds any standard OCaml term into
a graph term. Functions peek, step, link, assign, root work as described earlier. Notice
that the deref operation is not implemented in order to keep the syntax succinct. As a
result, the difference between a cell and a non-cell graph is not known in compile
time which could leads to runtime error when one trying to use link on these graphs.
Internally, the dataflow graph is maintained using a heterogeneous list of all cells.
The Obj module is used to overcome OCaml’s type restrictions. However, the internal
details are inaccessible to the programmer, who may use the module only via the
PPX extension [%dfg t] which translates a pure dataflow term t into a graph. By pure
dataflow, we mean that t doxes not contain ref, link, assign, root, peek nor step. These
functions are not translated and should be used outside the [%dfg t] tag. The translation
(⌜−⌝V ) is indexed by a set V of variables bounded in the [%dfg t] tag:
1 ⌜x⌝V = x (if x ∈
/ V)

12: 31

## PDF page 32

Transparent Synchronous Dataflow

2 ⌜x⌝V = Thunk (fun() -> x)} (if x ∈ V )
3 ⌜c⌝V = Thunk (fun() -> c)
4 ⌜λx.t⌝V = Thunk (fun() -> fun x -> peek (⌜t⌝V ∪{x} ))
5 ⌜t u⌝V = apply ⌜t⌝V ⌜u⌝V
6 ⌜if t1 then t2 else t3⌝V = ite t1 (fun() -> ⌜t2⌝V )(fun() -> ⌜t3⌝V )

The main helper functions are:
apply simulates the application in the TSD calculus,
ite implements the semi-strict behaviour of branching,
Their implementations are:
1 let apply t u = Thunk (fun () -> (peek t) (peek u))
2 let ite b t1 t2 =
3 let t1 = t1() in let t2 = t2() in
4 IF_Thunk (fun () -> if peek b then t1 else t2)

The incremental implementation is similar, except that a graph structure is maintained throughout the execution. Incrementalisation is accomplished by marking
certain cells as dirty and only these cells are recomputed in a step.
C.1 Benchmarks

We tested two versions of the code, with and without incrementalisation. The latter
is an optimisation in which not all cells are refreshed, but only those that need to.
We ran similar (as similar as possible) versions of the same program against Reactive
ML, JS Incremental, and Zélus. We chose the programs from the documentations of
those programming languages, presumably as representative of their strengths. The
examples were:
1. the alternating-sum automata of the introduction,
2. a large cellular automaton,
3. a long-and-thin chain of propagations,
4. a short-and-wide chain of propagations,
5. finite and infinite input response filters,
6. fold-like computations,
7. a simulation of a heating element,
8. a light controller,
9. a map-like computation,
10. a page-rank algorithm,
11. a pendulum simulation,
12. an n-body gravitational simulation,
13. and a tree propagation.
For each example we could vary the size of the graph for up to 107 nodes. The
benchmark tables are in the Appendix (appendix C.1).
RML: As a low-level language with its own compilers we expected RML to be much
faster. However, for most examples at least one of the TSD implementations had

12: 32

## PDF page 33

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

better or similar performance. RML only outperformed both TSD versions for
infinite input response filter and map.
Incremental JS: This is a highly-tuned OCaml library used in production by JaneStreet.
It does not support cyclic dependencies so most examples could not be implemented
in it. For long-and-thin and tree-like chains of propagations incremental TSD
outperformed, and for short-and-wide chains plain TSD outperformed.
Zélus: For the heater simulation and the light controller TSD was heavily outperformed
it. For the pendulum simulation Zélus was slightly faster in very large systems.
The first column represents the size of the dataflow graph. All times expressed in
milliseconds.

D

Type Soundness Proof

D.1 Conventions

In the following sections we will denote certain graph compositions by the rules below
which are borrowed from string diagrams.
For any graph G : Λ → (Γ ∪ Ψ) and any graph E : (Γ ∪ Π) → Ω, the
resulting composite graph is denoted by EG : (Λ ∪ Π) → (Ψ ∪ Ω).
Composition

For any graph G : Λ → Γ and any graph E : Π → Ω, the resulting
parallel composite graph is denoted by E ⊗ G : (Λ ∪ Π) → (Γ ∪ Ω).
Parallel composition

D.2 Environments

In this section, we identify a special form of graphs, dataflow environments, which
corresponds to dataflow graph model. We also prove termination for these graphs in
Sec. D.5.
Definition D.1 (Boxes). There is only one kind of box, the !-box shown below:

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="N9s+gPR64v1JUHgalLjR6XpLj8A=">AAAB6HicbVDLSgNBEOyNrxhfUS+Cl8EgeAq7UdBjwIMeEzAPSJYwO+lNxszOLjOzQgj5Ai8eFPHqJ3nzb5wke9DEgoaiqpvuriARXBvX/XZya+sbm1v57cLO7t7+QfHwqKnjVDFssFjEqh1QjYJLbBhuBLYThTQKBLaC0e3Mbz2h0jyWD2acoB/RgeQhZ9RYqX7XK5bcsjsHWSVeRkqQodYrfnX7MUsjlIYJqnXHcxPjT6gynAmcFrqpxoSyER1gx1JJI9T+ZH7olJxbpU/CWNmShszV3xMTGmk9jgLbGVEz1MveTPzP66QmvPEnXCapQckWi8JUEBOT2dekzxUyI8aWUKa4vZWwIVWUGZtNwYbgLb+8SpqVsndZrtSvStWTLI48nMIZXIAH11CFe6hBAxggPMMrvDmPzovz7nwsWnNONnMMf+B8/gCQoYyl</latexit>

?

G

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

Definition D.2 (Value dags). A value dag is a directed acyclic graph of !-boxes and
C -nodes.
Definition D.3 (Term graphs). A term graph is a graph that does not have any {n}nodes.

12: 33

## PDF page 34

Transparent Synchronous Dataflow

Benchmarks against RML and Zélus

Table 4

(a) alternating-sum automata

size

(b) heater simulation

TSD

inc. TSD

RML

Zélus

size

14
136
835

15
146
1463

33
306
2786

38
92
776

4

5

10
106
107

(c) light controller

size
5

10
106
107

TSD
1
1
2

10
105
106

inc. TSD

Zélus

1
2
1

28
49
234

(d) pendulum

TSD

inc. TSD

RML

Zélus

size

TSD

inc. TSD

Zélus

12
140
1301

14
138
1292

71
705
6466

30
89
648

5

85
861
8793

191
1887
21 221

88
638
6464

10
106
107
(f) planets

(e) cellular automata

size

TSD

inc. TSD

RML

size

TSD

inc. TSD

RML

2

2
4
74

2
4
88

8
897
1601

10
102
103

6
323
46 644

6
336
47 698

7
597
54 268

10
103
104

(h) IIR filter

(g) FIR filter

size

TSD

inc. TSD

RML

size

TSD

inc. TSD

RML

2

32
381
11630

226
3905
46323

32
272
7728

10
102
103

116
1243
17 765

431
8351
198 376

67
468
6465

TSD

inc. TSD

RML

2
34
462

1
14
188

2
2
23

TSD

inc. TSD

RML

1
2
13

2
2
26

2
2
2

TSD

inc. TSD

RML

2
2
10

1
2
26

2
2
2

10
103
104

(i) page rank

(j) map

size

TSD

inc. TSD

RML

size

10
102
103

1
10
2970

1
2
387

2
11
3060

3

10
104
105

(k) fold-max

(l) fold-max 2

size

TSD

inc. TSD

RML

size

2

1
170
5381

2
2
32

2
1
2

2

10
103
104

10
103
104

(m) fold-sum

(n) fold-sum 2

size

TSD

inc. TSD

RML

size

2

2
141
52 868

2
5
51

2
1
2

2

10
103
104

10
103
104

12: 34

## PDF page 35

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
Table 5 Benchmarks against JS incremental
(b) tree propagation

(a) chain of propagation

size

inc. TSD

JS Incr.

size

TSD

inc. TSD

JS Incr.

3

3
11
167
1796
2243

5
15
52
733
8222

103
104
105
106
107

2
13
121
1629
15 510

2
2
5
28
275

5
7
15
100
998

10
104
105
106
107

(c) field of propagation

size

TSD

inc. TSD

JS Incr.

103
104
105
106
107

2
8
152
1683
17 217

1
3
12
48
384

7
7
20
132
1172

Definition D.4 (Dataflow environment). A dataflow environment is the largest graph
connecting (in both direction) to all {n}-node and consisting of only {$, if, C, d}-nodes
satisfying the following conditions:
1. the out-port of any C -node is not connected to a C -node nor a !-box, and
2. the left out-port of any if-node is not connected to a !-box, and
3. at least one of the out-ports of any $-nodes is not connected to a !-box.
D.3 Query and Answer

Definition D.5 (Answer sets). We define the answer sets any e : θ as follows:
Anse:Int = {(n, −)}
Anse:Cell = {(n, e)}
¨
{(n, g)}
Anse:!Int =
{(n, −)}

if e is connected to a dataflow environment
otherwise

Anse:Unit = Anse:!Unit = {((), −)}
Anse:κ1 ⊸κ2 = Anse:!(κ1 ⊸κ2 ) = {(λ, −)}

Definition D.6 (Terminating graphs). For any graph G : Λ → ; and any port e : κ ∈
dom(Λ), (G, e) ⇓ iff there exists some G ′ such that Init(G, e) 7→∗ Final(G ′ , e, X ) for some
X ∈ Anse .
Lemma D.1 (Stack extension over transitions). For any transitions
(G, (e, d, f , S, B), ;) 7→ (G ′ , (e′ , d ′ , f ′ , S ′ , B ′ ), ;),

12: 35

## PDF page 36

Transparent Synchronous Dataflow

we also have for any Se , Be ,
(G, (e, d, f , SSe , BBe ), ;) 7→ (G ′ , (e′ , d ′ , f ′ , S ′ Se , B ′ Be ), ;)

Proof. This is proved by case analysis on all transitions.
Corollary D.1.1 (Termination extending over stacks). For any graph G : Λ → ; and
any port e : κ ∈ dom(Λ) inside G , if (G, (e, d, f , S, B), ;) 7→∗ (G ′ , (e′ , d ′ , f ′ , S ′ , B ′ ), ;) then
for any Se , Be we also have (G, (e, d, f , SSe , BBe ), ;) 7→∗ (G ′ , (e′ , d ′ , f ′ , S ′ Se , B ′ Be ), ;)
D.4 Valid States

Definition D.7 (Paths). A path is an ordered list of ports e0 ...en such that if ei , ei+1 is
the incoming and the outgoing port of same node.
Definition D.8 (Reachability). A node X is reachable from a port e if there exists a
path from e to the incoming port of X .
Definition D.9 (Evaluated in-ports). An in-port is evaluated if its reachable graph K
is an environment.
Definition D.10 (Circular requirements). A graph G satisfies the circular requirements
if all its circular paths satisfy one of the following conditions:
1. the path includes the right and left outgoing port of a λ/µ-node and all the ports
and nodes in this path are only reachable through the respective λ/µ-node,
2. the path includes a {n}-node.
Definition D.11 (Valid graphs). A graph G is valid if it satisfies all the following
conditions:
1. any !-nodes, ?-nodes, λ-nodes and µ-nodes must only appear in the form of boxes,
2. the left out-port of a λ-node or a µ-node must either be connected by a C -node
without any in-port or be reachable from its right out-port,
3. the out-port of any C -node or ?-node must be evaluated or to a ?/C -node or the
left-in-port of a λ-node or a µ-node,
4. the out-port of any {n}-node must be evaluated, and
5. it satisfies the circular requirements.
Definition D.12 (Valid positions). For any graph G , a token δ = (e, d, f , S, B) is said to
have a valid position if it satisfies all the following conditions:
1. if e is inside a !-box, it must be the out-port of the !-node which has no outer boxes,
and
2. e is not the in-port nor out-port of any ?-node.
Definition D.13 (Valid rewrite flags). For any graph G , a token δ = (e, d, f , S, B) is
said to have a valid rewrite flag if it satisfies one of the following conditions:
1. if f = @ then e must be the in-port of an @-node and d = ↑,
2. if f = if then e must be the middle/right out-port of an if-node and d = ↑,

12: 36

## PDF page 37

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

3. if f ∈ {!, C} then e must be the out-port of the respective node and d = ↑,
4. if f = µ then e must be the in-port of a µ-node and d = ↑,
5. if f ∈ {m, p, r(i), l(i), a(b, i)} then e must be the in-port of the respective node and

d = ↓,
6. if f ∈ {sp, s} then e must be the in-port of an s-node with d = ↑ or d = ↓ respectively,
7. f = □.

Definition D.14 (Valid stacks). For any graph G and any path e0 . . . en , an eval token
δ = (en , d, f , S, B) is said to have valid stacks relative to p if textvalid P’ d S B = true
where P’ is the reverse of P and isValid is defined as follows:
1 isValid :: Path -> Direction -> C-stack -> B-stack -> Boolean
2 isValid p ↑ (⋆ : S) B = validHist p S B
3 isValid (en : p) ↓ (X : S) B = X ∈ Ansen and validHist (en : p) S B
4 isValid _ _ _ _ = false
5
6 validHist :: Path -> C-stack -> B-stack -> Boolean
7 validHist [] [] [] = true
8 validHist [] _ _ = false
9 validHist (ei : p) S B =
10 if ei is the left-output of a #-node then
11
S == X : S' and X ∈ Anse′ and validHist p S' B
12
where e′ is the right-output of the #-node
13 else if ei is the middle-output of an if-node and i < n then
14
(S == if0 : S' or S == if1 : S') and validHist p S' B
15 else if ei is the right-output of an if-node and i < n then
16
S == X : S' and X ∈ Anse′ and validHist p S' B
17
where e′ is the middle-output of the if-node
18 else if ei is the output of a C-node then
19
B == ei−1 : B' and validHist p S B'
20 else
21
validHist p S B

Definition D.15 (Valid graphs relative to paths). For any graph G , any path p = e0 ...en
and token (en , d, f , X : S, B), G is valid relative to p if it satisfies the following conditions:
1. if en is the out-port of a !-node, d = ↑ and f = □ then this !-node cannot be
connected by a C -node,
2. if en is the in-port or out-port of a !-node and d = ↓ then this !-node cannot be
connected by a C -node,
3. there cannot be two consecutive ports in p being the out-port of a C -node except
when d = ↑, f = C and en is the out-port of a C -node,
4. en must not be only reachable by an λ-node or a µ-node (that is not inside a box)
from its right out-port nor its left in-port,
5. if d = ↓ then X = (n, g) if and only if en is connected to a dataflow environment.
Definition D.16 (Valid tokens). For any graph G , any path p = e0 ...en , a token
(en , d, f , S, B) is valid relative to p if it has a valid position, a valid rewrite flag, valid
stacks relative to p and G is valid relative to p.

12: 37

## PDF page 38

Transparent Synchronous Dataflow

Definition D.17 (Valid prop-tokens). A state π = (G, (e, d, f , S, B), P) has valid proptokens if it satisfies all the following conditions:
1. P can only be non-empty when f = sp,
2. every token in P must all be valid relative to a unique non-circular path starting
from a {n}-node.
Definition D.18 (Evaluated requirements). For any graph G , an eval token δ =
(e, d, f , S, B) satisfies the evaluated requirements if it satisfies the following conditions:
1. if d = ↓, f = □ and e : κ then e is evaluated,
2. if e is reachable by an if-node from the middle-out-port or the right-out-port, then

its left-out-port must be evaluated,
3. if e is reachable by an if-node from the right-out-port and f = □, then its middleout-port must be evaluated,
4. if d = ↓ and e is the in-port of an ω-node (unary operations) then its out-port must
be evaluated,
5. if e is reachable by an #-node (binary operations) or an @-node from the left-outport, then its right-out-port must be evaluated,
6. if d = ↓ and e is the in-port of a #-node then all its out-ports are evaluated, and
7. if e is the in-port of an @-node and f = @ then all its out-ports are evaluated.
Definition D.19 (Valid states). A state π = (G, δ, P) is valid if G is valid, δ is valid
relative to a non-circular path starting from an in-port of G , P is valid and it satisfies
the evaluated requirements.
Lemma D.2 (State validity preservation). For any valid state π, if π 7→ π′ then π is
also valid.
Proof. This is proved by inspecting all possible transitions one-by-one.
For pass transitions and dummy rewrites, we simply needs to check if the resulting
state has valid position, valid rewrite flags valid stacks and valid prop-tokens since
the graph does not change.
As for rewrite transitions, the trickiest part is to prove that the circular requirements
holds, i.e. no arbitrary circular path exists. For example, in the λ@-rewrite, if the
left-in-port of the λ-node is reachable from its right-out-port, an arbitrary circular path
would be form only if its left-in-port is reachable from the right-out-port of the @-node
which is impossible because all the ports in the path must be reachable through the
λ-node which means this part of the graph is isolated from the right-out-port of the
@-node. The other possible rewrite to create circular path is the l -rewrite. However
a l -rewrite will create a circular path that has a cell in it, as such it conforms to the
requirements. Other requirements are checked accordingly.
Corollary D.2.1. For any valid state π, if π 7→ π′ then π′ is also valid.

12: 38

## PDF page 39

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya
D.5 Termination of Dataflow Environments

Proposition D.3 (Termination of dataflow environments). For any valid dataflow
environments E : Λ → ; and any e ∈ dom(Λ), there exists some X ∈ Anse such that
Init(E, e) 7→∗ Final(E, e, X ) such that no rewrites occur.
Proof. This can be proved by induction on the maximum length (n) of the path from
e that stops at any {n}.
Base Case (n = 0). This case is not applicable.
Base Case (n = 1). The only case here would be a single {n}-node which terminates.
Inductive Step (n = k + 1). This is proved by case analysis on the possible nodes
connected by e.
Sub-Case e is connected to a $-node, if-node, , C -node or d -node or !-node.
These cases are similar and thus we will show the proofs for $-node. Running an
execution, we have:
G$, (e, ↑, □, ⋆ : □, □), ; 7→ G$, (e1 , ↑, □, ⋆ : □, □), ;

(1)

∗

7→ G$, (e1 , ↓, □, X : □, □), ;

(2)

7→ G$, (e2 , ↑, □, ⋆ : X : □, □), ;

(3)

7→ G$, (e2 , ↓, □, Y : X : □, □), ;

(4)

7→ G$, (e, ↓, $, (m, g) : □, □), ;

(5)

7→ G$, (e, ↓, □, (m, g) : □, □), ;

(6)

∗

From (1) to (2) and (3) to (4), since the whole graph is a dataflow environment,
therefore the at least one of the out-port must be a dataflow environment as well.
On the other hand, if the out-port is connected to a constant !-box then it obviously
comes back, there fore we apply the induction hypothesis on the remaining graph
and Cor. D.1.1. From (4) to (5) by the definition of dataflow environment, one of the
out-port must not be connected to a !-box, as such by validity, one of Y, X must be in
the form of (m, g).
D.6 Determinism

In this section we proved that propagation always terminates and produce unique
results and hence the transitions are deterministic up to equivalence of propagation
sequences. The intuition is that all the {n}-nodes are connected to a dataflow environment therefore as we have proved before that dataflow environment always
terminates and produces the same graph, thus propagation will also terminate.
Lemma D.4 (Termination of prop tokens). For any valid state (G, (r, ↑, sp, S, B), [e, ↑, ⋆ :
□, □]) where r is the in-port of an s-node, and e : κ of a {n}-node, there exists a sequence
of transitions (G, (r, ↑, sp, S, B), [e, ↑, ⋆ : □, □]) 7→∗ (G, (r, ↑, sp, S, B), [e, ↓, X : □, □]).

12: 39

## PDF page 40

Transparent Synchronous Dataflow

Proof. Since by validity, any {n}-node will always be connecting to a dataflow environment. Therefore this is simply a consequence of Prop. D.3.
Proposition D.5 (Termination of propagation). For any graph G , any possible sequences
from (G, (e, ↑, sp, S, B), Init P ) will eventually reach (G, (e, ↑, sp, S, B), Final P (X⃗ )) for some
X⃗ where e is the in-port of an s-node.
Proof. This is proved by contradiction. If the sequence does not reach the final state,
there are two possibilities: 1) the sequence is infinite or 2) the sequence reaches a
state which is not final but cannot proceed. For the first case, at least one of sequences
of a prop token is infinite which contradicts Lem. D.4. For the second case, it also
means that one of the prop token is stuck which also contradicts Lem. D.4.
Lemma D.6 (Diamond property). For any valid state (G, δ, P) if (G, δ, P) 7→ (G, δ, P ′ )
and (G, δ, P) 7→ (G, δ, P ′′ ) then there exists a valid state π such that (G, δ, P ′ ) 7→ π and
(G, δ, P ′′ ) 7→ π.
Proof. Since we have (G, δ, P) 7→ (G, δ, P ′ ) and (G, δ, P) 7→ (G, δ, P ′′ ), if the states are
produced with advancing different prop-tokens, i.e.
(G, δ, {t 1 ..t i ..t j ..t n }) 7→ (G, δ, {t 1 ..t i′ ..t j ..t n })

and
(G, δ, {t 1 ..t i ..t j ..t n }) 7→ (G, δ, {t 1 ..t i ..t ′j ..t n })

. Then we can join the two sequence into (G, δ, {t 1 ..t i′ ..t ′j ..t n }) because the transition
does not cause any race conditions.
Proposition D.7 (Confluence of propagation). For any valid state (G, δ, P), if (G, δ, P) 7→∗
(G, δ, P ′ ) and (G, δ, P) 7→∗ (G, δ, P ′′ ) then there exists a valid state (G, δ, K) such that
(G, δ, P ′ ) 7→∗ (G, δ, K) and (G, δ, P ′′ ) 7→∗ (G, δ, K).
Proof. This is a consequence of Lem. D.6.
Corollary D.7.1. There is exactly one unique final state for any sequence from (G, δ, P).
By using this corollary, all the possible propagation sequences from
(G, (e, ↑, sp, S, B), Init P )

to
(G, (e, ↑, sp, S, B), Final P (X⃗ ))

form an equivalence class.
Definition D.20 (Step-propagation transitions). We replace the transitions in Def. 3.5
by the following transitions respectively:
1. (G, (e, ↑, □, ⋆ : S, B), ;) 7→ (G, (e, ↑, sp, ⋆ : S, B), ;)

12: 40

## PDF page 41

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

2. (G, (e, ↑, sp, ⋆ : S, B), ;) 7→ (G ′′ , (e, ↓, □, (b, −) : S, B), ;) where G ′′ and b are obtained

by executing the step-propagation.
Proposition D.8 (Determinism). The machine is deterministic by replacing Def. 3.5
with Def. D.20.
Proof. This is a consequence of Prop. D.5 and Prop. D.7.
In the section below, whenever we talk about transitions, unless otherwise specifies,
we always mean the replaced set of transitions. As a result the set of prop-tokens will
always be empty, thus we will represent the machine state as only G, δ from now on.
D.7 Expansion of Contractions

In this section we proved that any graph G behaves the same way as expanding all its
outter contractions (C -nodes that are not inside a box).
Definition D.21 (U-simulation). A relation R on states is a U -simulation if it satisfies
the following conditions:
′
1. if π1 R π2 and a transition π1 7→ π′1 is possible then there exists two states π′′
1 , π2
such that π′1 7→∗ π′′1 (possibly no transitions), π2 7→ π′2 and π′′1 R π′2 ,
2. π1 R π2 then if there is no possible transition for π1 then there is no possible
transition for π2 as well,
3. if π1 R π2 , then π1 is an ending state if and only if π2 is an ending state.
Lemma D.9. For any U-simulation R if π1 R π2 and π2 7→∗ π′2 then there exists a state
π′1 such that π1 7→∗ π′1 and π′1 R π′2 .
Proof. This is proved by induction on the sequence π2 7→n π′2 .
Base Case n = 0. Then π2 = π′2 and since π1 R π2 then we can pick π′1 = π1 and
thus it is true.
Inductive Case n = k + 1. We need to show that there exists some state π′1 such that
π1 7→∗ π′1 and π′1 R π′2 . Suppose there is no possible transition from π1 then because
π1 R π2 thus there should not be any transition from π2 as well which contradicts
the assumption that π2 7→k+1 π′2 , therefore there must exists a π′1 such that π1 7→ π′1 .
As a result, because π1 R π2 there exists some π′′1 , π∗2 such that π′1 7→∗ π′′1 such that
π′′1 R π∗2 . Since 7→ is deterministic (Prop. D.8) therefore we have π2 7→ π∗2 7→k π′2 . By
using the induction hypothesis, there must exists some π∗1 such that π′′1 7→∗ π∗1 and
π∗1 R π′2 .
Lemma D.10. For any U-simulation R if π1 R+ π2 and π2 7→∗ π′2 then there exists a
state π′1 such that π1 7→∗ π′1 and π′1 R+ π′2 .
Proof. This proved by induction on n ≥ 1 for π1 Rn π2 .

12: 41

## PDF page 42

Transparent Synchronous Dataflow

Base Case n = 1. This is proved in Lem. D.9.
Inductive Case n = k + 1. We need to show that if π1 Rk π2 R π3 and π3 7→∗ π′3
then there exists some π′1 such that π1 7→∗ π′1 and π1 R+ π′1 . Since π2 R π3 by using
Lem. D.9, there exists some π′2 such that π2 7→∗ π′2 and π′2 R+ π′3 . Now by using
the induction hypothesis on k, there must exists some π′1 such that π1 7→∗ π′1 and
π′1 R+ π′2 . Thus we have π′1 R+ π′3 .
Lemma D.11. For any U-simulation R its transitive closure R+ is also a U-simulation.
Proof. We need to show that R+ satisfies the three conditions of a U-simulation.
Case (1). We need to show that if π1 R+ πe and a transition π1 7→ π′1 is possible
then there exists two states π′′1 , π′e such that π′1 7→∗ π′′1 , πe 7→ π′e and π′′1 R+ π′e .
Since there must exists a n ≥ 1 such that π1 Rn πe , therefore we can do induction
on n. When n = 1 it is trivially true because π1 R πe . When n = k + 1 then we have
π1 Rk π2 R πe . Since π1 Rk π2 and π1 7→ π′1 is possible therefore by using the induction
hypothesis, there exists two states π′′1 , π′2 such that π′1 7→∗ π′′1 , π2 7→ π′2 and π′′1 R+ π′2 .
Since π2 R πe and π2 7→ π′2 , therefore these also exists two states π′′2 and π′e such that
π′2 7→∗ π′′2 , πe 7→ π′e and π′′2 R π′e . Then by using Lem. D.10, there must exists some
′′
∗ ′′′
′′′
′′
′′′ + ′
state π′′′
1 such that π1 7→ π1 and π1 R π2 . Thus π1 R πe .
Case (2). We need to show that if π1 R+ πe and there is no possible transition from
π1 then so is πe .
Since there must exists a n ≥ 1 such that
π1 R π2 R . . . R πn−1 R πe

therefore we can do induction on n. When n = 1 we have π1 R πe and thus πe has no
possible transition. When n = k + 1 we have π1 R π2 R . . . R πk R πe . Since π1 R π2
means that π2 has no possible transitions and hence by the induction hypothesis this
is true.
Case (3). We need to show that if π1 R+ πe then π0 is an ending state if and only if
πe is an ending state.
Since there must exists a n ≥ 1 such that
π1 R π2 R . . . R πn−1 R πe

, therefore we can do induction on n. When n = 1 it is trivially true because π1 R πe .
When n = k + 1 we have π1 R π2 R . . . R πk R πe . a) π1 is an ending state implies πe
is an ending state: Since π1 R π2 means that π2 is also an ending state therefore by
the induction hypothesis, πe is also an ending state. The other direction is similar.
Lemma D.12. For any states π1 , π2 and an U-simulation R such that π1 R π2 , then
π1 7→∗ π1e ⇐⇒ π2 7→∗ π2e for some ending states π1e , π2e .

12: 42

## PDF page 43

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

Proof. For the direction π1 7→∗ π1e =⇒ π2 7→∗ π2e , it can be proved by induction on
the number of sequence π1 7→n π1e .
Base Case n = 0. Since π1 = π1e and π1 R π2 , therefore π2 is an ending state.
Inductive Step n = k + 1. We need to show that if π1 7→k+1 π1e then there must
exists an ending state π2e such that π2 7→∗ π2e .
We can factorise the sequence into π1 7→ π′1 7→k π1e . By the definition of U-simulation,
there must exists two states π′′1 and π′2 such that π′1 7→∗ π′′1 , π2 7→ π′2 and π′′1 R π′2 .
Therefore by determinism, either 1) π′′1 is an ending state which then by definition π′2
has to be an ending state or 2) π′′1 7→i π1e where i ≤ k and thus by induction hypothesis,
there must exists some state π2e such that π′2 7→∗ π2e .
For the other direction π1 7→∗ π1e ⇐= π2 7→∗ π2e , it is proved in Lem. D.9.
Definition D.22 (Replacement of contractions). We define a relation ≺ (replace by)
on graphs where ≺ = ≺m ∪ ≺c ∪ ≺i
Cf
<latexit sha1_base64="aKDSqqyIYxadlWYtOhkx3zjZE+I=">AAAB8nicbVDLSgMxFL1TX7W+qi7dBIvgqsxUQZeFblxWsA9oh5JJM21oJjMkd8Qy9DPcuFDErV/jzr8xbWehrQcCh3PuIfeeIJHCoOt+O4WNza3tneJuaW//4PCofHzSNnGqGW+xWMa6G1DDpVC8hQIl7yaa0yiQvBNMGnO/88i1EbF6wGnC/YiOlAgFo2ilXh/5k01ljXA2KFfcqrsAWSdeTiqQozkof/WHMUsjrpBJakzPcxP0M6pRMMlnpX5qeELZhI54z1JFI278bLHyjFxYZUjCWNunkCzU34mMRsZMo8BORhTHZtWbi/95vRTDWz8TKkmRK7b8KEwlwZjM7ydDoTlDObWEMi3sroSNqaYMbUslW4K3evI6adeq3lW1dn9dqZO8jiKcwTlcggc3UIc7aEILGMTwDK/w5qDz4rw7H8vRgpNnTuEPnM8fsTGRaQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e

C
m
C

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

≺m

e
C

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

C

?

h
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

≺c

!

m
C
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

?

G
h
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

…

!

?

G
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

m

?
?
G
h

!

m
C
l

≺i

G
h

!

where C f is the largest forest of C -nodes connected, and the C -node on the left-handside of ≺c has more than one in-ports.
ˆ on valid states such that for any graph
Definition D.23. We define a binary relation ≺
ˆ (G [G2 ], δ2 ) if G1 ≺ G2 where the bottom C -node is not
context G [□], (G [G1 ], δ1 ) ≺
connected by another C -node, or G1 = G2 , δ1 = δ2 , the position of the main token is
in G . Note that if C f is empty, then the only in-ports for G1 would be the in-ports of
the C -node.
ˆ is a U-simulation.
Lemma D.13. ≺

Proof. This is proved by analysing all the possible transitions one-by-one. In some of
the following cases, we will only show the part of the graph that matters.
Case when token is inside G excluding the border. If it is a pass transition or a
dummy rewrite, then we also have the exact same transition on the right-hand-side.

12: 43

## PDF page 44

Transparent Synchronous Dataflow

If it is a rewrite transition then it depends on whether it involves any of the holes. If
not then it is trivial. If yes, then it must be one of the following cases (other cases are
disproved by validity): (1)

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

G
h

(

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

k

!

, h, ↑, !, S, k : B)

C
m
C

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

l

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

C

?

?

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

G

7→ ( h !
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

k

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e

!

, h, ↑, !, S, B)

<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

C
m
C
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

vs
<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

?

G
h

(

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

k
<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

!

, h, ↑, !, S, k : B)

C
l

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

C

?

<latexit sha1_base64="s9I1xHA5Mpp41qKteb9FbOR0LvY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoDcLXjy2YGuhDWWznbRrN5uwuxFK6C/w4kERr/4kb/4bt20O2vpg4PHeDDPzgkRwbVz32ymsrW9sbhW3Szu7e/sH5cOjto5TxbDFYhGrTkA1Ci6xZbgR2EkU0igQ+BCMb2f+wxMqzWN5byYJ+hEdSh5yRo2Vmjf9csWtunOQVeLlpAI5Gv3yV28QszRCaZigWnc9NzF+RpXhTOC01Es1JpSN6RC7lkoaofaz+aFTcmaVAQljZUsaMld/T2Q00noSBbYzomakl72Z+J/XTU147WdcJqlByRaLwlQQE5PZ12TAFTIjJpZQpri9lbARVZQZm03JhuAtv7xK2rWqd1GtNS8rdZLHUYQTOIVz8OAK6nAHDWgBA4RneIU359F5cd6dj0VrwclnjuEPnM8fhumMpQ==</latexit>

G

7→ ( h !
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

k

?

G
<latexit sha1_base64="7bD4DOjZGCiApKOARe6s9kkcjGo=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69rBbBU0mqoMeCF48t2FpoQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgpr6xubW8Xt0s7u3v5B+fCoreNUMWyxWMSqE1CNgktsGW4EdhKFNAoEPgTj25n/8IRK81jem0mCfkSHkoecUWOl5mm/XHGr7hxklXg5qUCORr/81RvELI1QGiao1l3PTYyfUWU4Ezgt9VKNCWVjOsSupZJGqP1sfuiUnFtlQMJY2ZKGzNXfExmNtJ5Ege2MqBnpZW8m/ud1UxPe+BmXSWpQssWiMBXExGT2NRlwhcyIiSWUKW5vJWxEFWXGZlOyIXjLL6+Sdq3qXVZrzatKneRxFOEEzuACPLiGOtxBA1rAAOEZXuHNeXRenHfnY9FacPKZY/gD5/MHWXGMhw==</latexit>

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e

!

, h, ↑, !, S, B)

<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C
l

(2) we have C[C C] vs C[C] where the token is at the top of the highest C -node.
In this case by validity, the current execution path does not contain any in-ports or
out-ports of from the hole.
⃗ . In this case copying the upper
And (3) we have ?G![(C f )(?G!)C] vs ?G![C(?G!)]
!-box using a C -node in C f will still result in a forest of C -nodes and so it is fine.
Case when token is at the border with G1 ≺m G2 . We proved this by analysing all
the possible cases.
Sub-Cases when token is at an in-port with d = ↑ and f ̸= □. These cases
induce rewrites in the ambient graph that do not affects the hole and thus they have
one-to-one correspondence.
Sub-Case when token is at an in-port with d = ↑ and f = □. Since l cannot be
connected to another C -node therefore we have only two cases: (1)

12: 44

## PDF page 45

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e
C

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

(G [ mC ], l, ↑, □, S, B) 7→4 (G [
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

e
C

], e, ↑, C, S, l : B)

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

vs
<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

(G [

e
C

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

], l, ↑, □, S, B) 7→ (G [

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

e
C

], e, ↑, C, S, l : B)

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

and (2)

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

(

k

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

C
m
C

<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

l

e
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

4

, k, ↑, □, S, h : B) 7→ (

k

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

C
m
C

, e, ↑, C, S, k : h : B)

<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

C
h

l

C
h

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

vs
<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

e
C

<latexit sha1_base64="PzCZH4KgMDy+7iYwhPTZIxyYHrE=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipiYNyxa26C5B14uWkAjkag/JXfxizNEJpmKBa9zw3MX5GleFM4KzUTzUmlE3oCHuWShqh9rPFoTNyYZUhCWNlSxqyUH9PZDTSehoFtjOiZqxXvbn4n9dLTXjrZ1wmqUHJlovCVBATk/nXZMgVMiOmllCmuL2VsDFVlBmbTcmG4K2+vE7atap3Va01ryt1ksdRhDM4h0vw4AbqcA8NaAEDhGd4hTfn0Xlx3p2PZWvByWdO4Q+czx/AgYzL</latexit>

<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

(

k
<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

C
h
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

l

e
C
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

, l, ↑, □, S, h : B) 7→ (

k
<latexit sha1_base64="hVyIH/o/DRDyVhO8UT2MmdJ1yxY=">AAAB6HicbVBNS8NAEJ3Ur1q/qh69LBbBU0mqoMeCF48t2A9oQ9lsJ+3azSbsboQS+gu8eFDEqz/Jm//GbZuDtj4YeLw3w8y8IBFcG9f9dgobm1vbO8Xd0t7+weFR+fikreNUMWyxWMSqG1CNgktsGW4EdhOFNAoEdoLJ3dzvPKHSPJYPZpqgH9GR5CFn1FipORmUK27VXYCsEy8nFcjRGJS/+sOYpRFKwwTVuue5ifEzqgxnAmelfqoxoWxCR9izVNIItZ8tDp2RC6sMSRgrW9KQhfp7IqOR1tMosJ0RNWO96s3F/7xeasJbP+MySQ1KtlwUpoKYmMy/JkOukBkxtYQyxe2thI2poszYbEo2BG/15XXSrlW9q2qteV2pkzyOIpzBOVyCBzdQh3toQAsYIDzDK7w5j86L8+58LFsLTj5zCn/gfP4AyZmM0Q==</latexit>

l

, e, ↑, C, S, k : h : B)

C
h
<latexit sha1_base64="Y7BEP0w6VGYqi9NNiv2IlT0rGTI=">AAAB6HicbVBNS8NAEJ34WetX1aOXxSJ4KkkV9FjoxWML9gPaUDbbSbt2swm7G6GE/gIvHhTx6k/y5r9x2+agrQ8GHu/NMDMvSATXxnW/nY3Nre2d3cJecf/g8Oi4dHLa1nGqGLZYLGLVDahGwSW2DDcCu4lCGgUCO8GkPvc7T6g0j+WDmSboR3QkecgZNVZq1gelsltxFyDrxMtJGXI0BqWv/jBmaYTSMEG17nluYvyMKsOZwFmxn2pMKJvQEfYslTRC7WeLQ2fk0ipDEsbKljRkof6eyGik9TQKbGdEzVivenPxP6+XmvDOz7hMUoOSLReFqSAmJvOvyZArZEZMLaFMcXsrYWOqKDM2m6INwVt9eZ20qxXvulJt3pRrJI+jAOdwAVfgwS3U4B4a0AIGCM/wCm/Oo/PivDsfy9YNJ585gz9wPn8AjPmMqQ==</latexit>

Sub-Case when token is at an in-port and d = ↓. By validity, the only possible case
is when the token is at an in-port of the upper C -node that is not m and a transition
takes the token away from the border to G which will be the same transition for the
right-hand-side.
Sub-Case when token is at an out-port and d = ↑. It is similar to the case when
token is at the in-port with d = ↑. The possible transition would either be a rewrite of
the hole or if the upper C -node is connected by another C -node then it would be a
rewrite of those two. It can also be the case that f = □ and any possible transitions
will take the token back to the context.
Sub-Case when token is at an out-port and d = ↓. By validity, B = j : B ′ such that
j ̸= m, as such the token goes back to an in-port that is not from the lower C -node.
Case when the token is at the border of G1 ≺c G2 . We proved this by analysing
all possible cases.
Sub-Case when token is at an in-port and d = ↑. We have (1) the token is at one
of the in-ports of the bottom C -nodes, and (2) the token is at one of the in-ports of
C f . These two cases are proved similarly as the ≺c -cases.
Sub-Case when the token is at the bottom and d = ↓. By validity the token cannot
be at one of the in-ports of the C -node, so the only case is when the token is at one of
the in-ports of C f . Any possible transitions will take the token back into the ambient
graph and the right-hand-side will have the same transition.
Sub-Case when the token is at the top. By validity, the possible cases would
be that the path does not incudes the !-box nor the C -node. So it would either be
a rewrites inside the C f or a transition that takes the token back to the ambient graph.
Case when token is at the border of G1 ≺e G2 . The only possible cases are when the
token is at the bottom with d = ↑ and it follows the same idea as previous cases.

12: 45

## PDF page 46

Transparent Synchronous Dataflow

Proposition D.14. For any graphs H1 , H2 : Λ → ;, if H1 ≺+ H2 then for any e ∈ dom(Λ),
(H1 , e) ⇓ ⇐⇒ (H2 , e) ⇓ where ≺+ is the transitive closure of ≺.
ˆ + Init(H2 , e) therefore this is simply a consequence of Lem. D.13,
Proof. Since Init(H1 , e) ≺
Lem. D.11 and Lem. D.12.
D.8 Re-evaluation

Definition D.24 (Stable sequences). A sequence is stable if it does not contain any
actual rewrite transitions.
Lemma D.15 (Factorisation of stable sequences). For any graph G : ({e : κ} ∪ Λ) → ;,
if we have a stable sequence Init(G, e) 7→∗ (G, e′ , ↓, □, X : S, B) then it can be factorised
into Init(G, e) 7→∗ (G, e′ , ↑, □, ⋆ : S, B) 7→∗ (G, e′ , ↓, □, X : S, B).
Proof. This is proved by induction on the number of transitions Init(G, e) 7→n (G, e′ , ↓, □, X :
S, B).
Base Case n = 0: This is impossible since the start state must have ↑.
Inductive Case n = k + 1: Since we have Init(G, e) 7→n (G, δ) 7→ (G, e′ , ↓, □, X : S, B),
this can be proved by case analysis on the last transition. We will show the proof for
(G [$], e′ , ↓, $, (n, g) : S, B) 7→ (G [$], e′ , ↓, □, (n, g) : S, B) where e′ is the in-port of the
$-node. Since the machine is deterministic we can rewind the sequence to get
Init(G [$], e)
n

7→ (G [$], el , ↓, □, (n2 , x) : (n1 , y) : S, B)
7→ (G [$], e′ , ↓, $, (n, g) : S, B)

Now by using induction hypothesis, we also have that
Init(G [$], e)
7→∗ (G [$], e r , ↓, □, (n1 , −) : S, B)
7→ (G [$], el , ↑, □, ⋆ : (n1 , −) : S, B)
7→∗ (G [$], el , ↓, □, (n2 , x) : (n1 , y) : S, B)
7→ (G [$], e′ , ↓, $, (n, g) : S, B)

12: 46

## PDF page 47

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

Continuing the process we will get
Init(G [$], e)
∗

7→ (G [$], e′ , ↑, □, ⋆ : S, B)
7→ (G [$], e r , ↑, □, ⋆ : S, B)
7→∗ (G [$], e r , ↓, □, (n1 , −) : S, B)
7→ (G [$], el , ↑, □, ⋆ : (n1 , −) : S, B)
7→∗ (G [$], el , ↓, □, (n2 , x) : (n1 , y) : S, B)
7→ (G [$], e′ , ↓, $, (n, g) : S, B)

Lemma D.16. For any graph G : ({e : κ} ∪ Λ) → ;, if Init(G, e) 7→∗ (G, δ) 7→R (G ′ , δ′ )
where the first part is stable, then we also have a stable sequence Init(G ′ , e) 7→∗ (G ′ , δ′ ).
Proof. This is proved by case analysis on every actual rewrite transitions (G, δ) 7→R
(G ′ , δ′ ).
Case p-rewrite, r -rewrite, m-rewrite, i f -rewrite, $-rewrite, l -rewrite, a-rewrite,
@-rewrite, C -rewrite, !C -rewrites, µ-rewrite: These cases are similar and thus we
will show the proof for $-rewrite. Let G = G [$] where G is the surround context, then
we have that
Init(G [$], e)
∗

7→ (G [$], e′ , ↓, $, (n, −) : S, B)
7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′ , ↓, □, (n, −) : S, B)

where e′ is the in-port of the $-node. Rewinding the sequence and by using Lem. D.15,
we have that
Init(G [$], e)
7→∗ (G [$], e′ , ↑, □, ⋆ : S, B)
7→ (G [$], e r , ↑, □, ⋆ : S, B)
7→∗ (G [$], e r , ↓, □, (n1 , −) : S, B)
7→ (G [$], el , ↑, □, ⋆ : (n1 , −) : S, B)
7→∗ (G [$], el , ↓, □, (n2 , −) : (n1 , −) : S, B)
7→ (G [$], e′ , ↓, $, (n, −) : S, B)
7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′ , ↓, □, (n, −) : S, B)

12: 47

## PDF page 48

Transparent Synchronous Dataflow

where e r , el are the right-out-port and left-out-port of the $-node. Since replacing
the $-subgraph with a constant !-box does not affect the first part of the sequence,
therefore we can construct the following sequence
Init(G [C0 ⊗ (n!) ⊗ C0 ], e)
∗

7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′ , ↑, □, ⋆ : S, B)
7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′′ , ↑, □, ⋆ : S, B)
7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′′ , ↓, □, (n, −) : S, B)
7→ (G [C0 ⊗ (n!) ⊗ C0 ], e′ , ↓, □, (n, −) : S, B)

where e′′ is the in-port to the n-node.
Case 7→ P -rewrite: The proof is similar. We first have that
Init(G [s], e) 7→∗ (G [s], e′ , ↑, sp, ⋆ : S, B) 7→ P (G ′ , e′ , ↓, □, (b, −) : S, B)

then we want to construct a sequence
Init(G ′ , e) 7→∗ (G ′ , e′ , ↑, sp, ⋆ : S, B) 7→∗ (G ′ , e′ , ↓, □, (b, −) : S, B)

, suppose the first half of the second sequence does not lead to G ′ which means that
there exists some rewrite transitions. However since the difference between G and G ′
is that the content of some cells are changed. This would mean that this transitions
will also happen in the original sequence which draws a contradiction.
Proposition D.17. For any graph G : {e : κ} ∪ Λ → ;, if Init(G, e) 7→∗ (G ′ , δ) for some
G ′ , δ, then we also have that Init(G ′ , e) 7→∗ (G ′ , δ).
Proof. Since the sequence Init(G, e) 7→∗ (G ′ , δ) is finite, therefore this can be proved
by induction on the number (n) of actual rewrite transitions in this sequence.
Base Case n = 0: this means that there are no actual rewrites in the sequence and
therefore G = G ′ .
Inductive Step n = k + 1. First we factorise the sequence into
Init(G, e) 7→∗ (G, δ′ ) 7→R (G ′′ , δ′′ ) 7→∗ (G ′ , δ)

where 7→R denotes an actual rewrite transition.
By using Lem. D.16 on Init(G, e) 7→∗ (G, δ′ ) 7→R (G ′′ , δ′′ ), we have that Init(G ′′ , e) 7→∗
(G ′′ , δ′′ ). Since the machine is deterministic we have Init(G ′′ , e) 7→∗ (G ′′ , δ′′ ) 7→∗ (G ′ , δ)
with k rewrites transitions. Therefore by using the induction hypothesis on k, we have
that Init(G ′ , e) 7→∗ (G ′ , δ).
D.9 Termination of Recursion-free Programs

In this section, we prove that programs without recursion always terminate. The proof
of termination relies on a unary logical relation, also known as a “logical predicate”.
Definition D.25 (Logical predicate for terminating graphs). For any term graph
G : {e : κ} → Γ , the logical predicate for terminating graphs Tκ is inductively defined
on κ as follows:

12: 48

## PDF page 49

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

1. κ ∈ {!Int, !Unit, Cell}: G ∈ Tκ iff for any dataflow environment E : Λ → ; such that

Γ ⊂ Λ, (EG, e) ⇓.

2. κ = !(κ1 ⊸ κ2 ): G ∈ Tκ if
a. for any dataflow environment E : Λ → ; such that Γ ⊂ Λ, (EG, e) ⇓, and
b. for any term graph H : {e1 : κ1 } → Γ ′ such that H ∈ Tκ1 , (G ⊗ H)@ ∈ Tκ2 , and
c. for any for any dataflow environment E : Λ → ; such that Γ ⊂ Λ if there exists

some K, X such that Init(EG, e) 7→ Final(K, e, X ) and that K can be decomposed
into E ′ G ′ then for any term graph H : {e1 : κ1 } → Γ ′ such that H ∈ Tκ1 , (G ′ ⊗
H)@ ∈ Tκ2 .
Proposition D.18. For any term graphs G1 , G2 : {e : κ} → Γ , G1 ≺+ G2 implies that
G1 ∈ Tκ ⇐⇒ G2 ∈ Tκ .
Proof. This is proved by induction on κ.
Base Case κ is a ground type. To show that G1 ∈ Tκ =⇒ G2 ∈ Tκ we need to
show that for any dataflow environment E , EG2 ⇓. Since (EG1 , e) ⇓ and EG1 ≺+ EG2 ,
therefore by using Lem. D.14, (EG2 , e) ⇓.
Induction Step κ =!(κ1 ⊸ κ2 ). To show G1 ∈ Tκ =⇒ G2 ∈ Tκ we need to show
that (a) (G2 , e) ⇓, (b) for any term graph H : {e1 : κ1 } → Γ ′ such that H ∈ Tκ1 ,
(G ⊗ H)@ ∈ Tκ2 , and (c) for any dataflow environment E : Λ → ; such that Γ ⊂ Λ
if there exists some K, X such that Init(EG2 , e) 7→ Final(K, e, X ) and that K can be
decomposed into E ′ G2′ then for any term graph H : {e1 : κ1 } → Γ ′ such that H ∈ Tκ1 ,
(G2′ ⊗ H)@ ∈ Tκ2 . (a) can be proved by using similar technique as the base case. To
show (b) we simply apply the induction hypothesis on κ2 . The other direction can be
shown by similar technique. To show (c) we run a sequence from Init(EG1 , e) to get
the resulting graph EG1′ such that G1′ ≺+ G2′ because of Lem. D.9. Since G1 ∈ Tκ thus
(G1′ ⊗ H)@ ∈ Tκ2 , therefore by induction hypothesis (G2′ ⊗ H)@ ∈ Tκ2 .
Definition D.26 (Value trees). A value tree is a tree of !-boxes.
Lemma D.19. For any value tree V : {e1 : κ} → Λ, V C⃗2 ≺+ C⃗2 (V ⊗ V ).
Proof. This is proved by induction on the maximum height h of the value tree.
Base Case h = 0. This is true as C⃗2 = C⃗2 .
Base Case h = 1. This is true as V C⃗2 ≺c C⃗2 (V ⊗ V ).
Induction Step h = k + 1. We need to show that (G!)V C⃗2 ≺+ C⃗2 ((G!)V ⊗ (G!)V )
where the maximum height of V is h and (G!) is a value box. By induction hypothesis
we have (G!)V C⃗2 ≺+ (G!)C⃗2 (V ⊗ V ) ≺c C⃗2 ((G!)V ⊗ (G!)V ).
Lemma D.20. For any set of value tress V⃗ = V1 : {e1 : κ1 } → Λ1 , . . . , Vm : {em : κm } → Λm ,
V⃗ C⃗2 ≺+ C⃗2 (V⃗ ⊗ V⃗ ).
Proof. This is proved by induction on m using Lem. D.19.

12: 49

## PDF page 50

Transparent Synchronous Dataflow

Lemma D.21. For any value dag V : {e : κ} → Γ , there exists some value tree V ′ such
that V ≺+ C⃗ V ′ .
Proof. This is proved by induction on the maximum height of V using similar technique
as Lem. D.19.
Lemma D.22. For any dataflow environment E : Λ → ; and any C⃗ : Ω′ → Ω such that
Ω ⊂ Λ, there exists another dataflow environment E ′ : Λ′ → ; such that E C⃗ ≺ E ′ or E C⃗
is a dataflow environment it self.
Proof. When a C -node in C⃗ is connected to a $, if, {n}-node then it is obvious that the
resulting graph is a dataflow environment. When a C -node is connected by another
C -node, the two will be replaced by a single C -node and the resulting graph would
still be a dataflow environment.
Lemma D.23. For any term graph G : {e : κ} → Γ and any set of parallel C -nodes
C⃗ : Γ → ω,
G ∈ Tκ =⇒ C⃗ G ∈ Tκ
C⃗ G ∈ Tκ =⇒ G ∈ Tκ

(1)
(2)

where C⃗ G : {e : κ} → ω.
Proof. This is proved by induction on κ.
Base Case κ is a ground type. To show (1) we need to show that for any dataflow
environments E , (E C⃗ G, e) ⇓. First by Lem. D.22 there exists a E ′ such that E C⃗ G ≺+ E ′ G .
Since E ′ G ⇓ (by assumption) therefore by using Lem. D.14, (E C⃗ G, e) ⇓. (2) can be
shown by similar technique.
Induction Step κ =!(κ1 ⊸ κ2 ). To show (1) we need to show that (a) for any
dataflow environment E , (E C⃗ G, e) ⇓, (b) for any term graph H : {e1 : κ1 } → Γ ′ such
that H ∈ Tκ1 , (C⃗ G ⊗ H)@ ∈ Tκ2 and (c) for any dataflow environment E : Λ → ; such
that Γ ⊂ Λ if there exists some K, X such that Init(E C⃗ G, e) 7→ Final(K, e, X ) and that
K can be decomposed into E ′ G ′ then for any term graph H : {e1 : κ1 } → Γ ′ such
that H ∈ Tκ1 , (G ′ ⊗ H)@ ∈ Tκ2 . (a) can be proved by using similar technique as the
base case. To show (b) we simply apply the induction hypothesis on κ2 . For (c) since
E C⃗ ≺+ F for some F , we run a sequence from Init(F G, e) to get F ′ G ′ since G ∈ Tκ
therefore it is true (2) can be shown by similar technique.
Lemma D.24. For any term graph G : {e : κ} → Γ where κ = !(κa ⊸ κ b ) if for any V⃗
where Vi ∈ Tκi , V⃗ G ∈ Tκ , then for any V⃗ where Vi ∈ Tκi , V⃗ G@ ∈ Tκ′ .
Proof. We need to show that for any V⃗ where Vi ∈ Tκi , V⃗ G@ ∈ Tκ′ . Since by assumption
we have V⃗ G ∈ Tκ therefore by the definition of logical predicate and taking H to be
the empty graph, we have that V⃗ G@ ∈ Tκ′ .

12: 50

## PDF page 51

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

Lemma D.25 (Backward reasoning). For any term graph G : {e : κ} → Γ , if there exists
a graph G ′ : {e : κ} → Γ such that (I) for any dataflow environment E : Λ → ; such that
Γ ⊂ Λ, Init(EG, e) 7→∗ (E ′ V⃗ G ′ , δ) for some V⃗ and δ and (II) for any V⃗ such that Vi ∈ Tκi ,
V⃗ G ′ ∈ Tκ , then G ∈ T κ.
Proof. This is proved by induction on κ.
Base Case κ is a ground type. Then we only need to prove that it terminates.
Assuming a dataflow environmrnt E , because of the assumption of G , we would
have Init(EG, e) 7→ ∗(E ′ V⃗ G ′ , δ). Also by assumption we have that V⃗ G ′ ∈ Tκ and thus
(E ′ V⃗ G ′ , e) ⇓. Since the machine is deterministic (Prop. D.8), and by using Lem. D.17,
we have Init(EG, e) 7→ ∗(E ′ V⃗ G ′ , δ) 7→∗ Final(E ′′ K, e, X ) and thus this case is true.
Inductive Case κ = !(κ1 ⊸ κ2 ). To prove (a), it follows the same idea as the base
case. As for (b), we need to prove that for any term graph H : {e1 : κ1 } → Γ ′ such that
H ∈ Tκ1 , (G ⊗ H)@ ∈ Tκ2 .
Assume a dataflow environment E , we would have Init(E(G ⊗H)@, e2 ) 7→∗ (E ′ (V⃗ G ′ ⊗
H ′ )@, δ) because of the assumptions such that H ′ ∈ Tκ1 . Notice that for any changes
to E , we will always run to a graph in the form of (X ′ (Y⃗ G ′ ⊗ X ′ )@. This satisfies the
assumption (II) of the IH if we take G ′ to be G ′ @. Now by using Lem. D.24, we also
have condition (II) of the IH. Therefore we can now apply the IH on κ2 and finally
get (G ⊗ H)@ ∈ Tκ2 . (c) is obvious because any dataflow environment will take G to
V⃗ G ′ which already satisfies the logical predicate by assumption.
Lemma D.26 (Fundamental lemma). For any well-typed term Γ ⊢ t : τ which is
recursion-free, let G : {e : κ} → Γ = [[Γ ⊢ t : τ]] any set of recursion-free value trees
V⃗ = V1 : {e1 : κ1 } → Λ1 , . . . , Vm : {em : κm } → Λm such that Vi ∈ Tκi ,

V1

Vm

…
G

∈ Tκ

where V⃗ G : {e : κ} → Λ and Λ =

⋃

Λi .

Proof. This is proved by induction on the type derivation Γ ⊢ t : τ.
Base Case Γ ⊢ x : τ which means that G is empty. Since Vi ∈ Tki therefore it is true.
Base Case Γ ⊢ n : Int. In this case since V⃗ is empty we only need to show that
for any dataflow environment E : Λ → ; such that Γ ⊂ Λ, (EG, e) ⇓. The proof is
straight-forward.
Inductive Step Γ ⊢ λx.t : τ1 → τ2 . We need to show that (a) for any dataflow
environment E : Λ → ; such that Γ ⊂ Λ, (E V⃗ G, e) ⇓, (b) for any term graph H : {e1 :
κ1 } → Γ ′ such that H ∈ Tκ1 , (V⃗ G ⊗ H)@ ∈ Tκ2 and (c) for any dataflow environment E :

12: 51

## PDF page 52

Transparent Synchronous Dataflow

Λ → ; such that Γ ⊂ Λ if there exists some K, X such that Init(E V⃗ G, e) 7→ Final(K, e, X )
and that K can be decomposed into E ′ G ′ then for any term graph H : {e1 : κ1 } → Γ ′
such that H ∈ Tκ1 , (G ′ ⊗ H)@ ∈ Tκ2 .
The proof of (a) is straight-forward. In order to show (b), we assume a dataflow
environment E : Λ → ; such that Γ ∪ Γ ′ ⊂ Λ and run a sequence from Init(E(V⃗ G ⊗
H)@, e2 ):
E(V⃗ G ⊗ H)@, (e2 , ↑, □, ⋆ : □, □)
7→ E(V⃗ G ⊗ H)@, (e1 , ↑, □, ⋆ : □, □)

(1)
(2)

7→ E (V⃗ G ⊗ H ′ )@, (e1 , ↓, □, X : □, □)
7→ E ′ (V⃗ G ⊗ H ′ )@, (e, ↑, □, ⋆ : □, □)

(3)

∗ ′

(4)

7→ E (V⃗ G ⊗ H )@, (a, ↑, !, ⋆ : □, □)
7→ E ′ (V⃗ G ⊗ H ′ )@, (a, ↑, □, ⋆ : □, □)
′

(5)

′

(6)

7→ E (V⃗ G ⊗ H )@, (a, ↓, □, (λ, −) : □, □)
7→ E ′ (V⃗ G ⊗ H ′ )@, (e, ↓, □, (λ, −) : □, □)
′

′

(7)
(8)

7→ E ′ (V⃗ G ⊗ H ′ )@, (e2 , ↑, □, ⋆ : □, □)
7→ E ′ (V⃗ (?([[t]]λ)!) ⊗ H ′ )@, (e2 , ↑, □, ⋆ : □, □)

(10)

7→ E (V⃗ [[t]] ⊗ H )@, (e2 , ↑, □, ⋆ : □, □)

(11)

′

′

(9)

where G =?([[t]])λ! and a is the in-port of the λ-node. Going from (2) to (3) we apply
the condition on H ∈ Tκ1 and Cor. D.1.1 and thus H ′ is a value dag and H ′ ∈ Tκ1 . Now
by using Lem. D.21, we have H ′ ≺+ C⃗ H ∗ such that H ∗ a value tree and C⃗ H ∗ ∈ Tκ1 . By
using Lem. D.23, H ∗ ∈ Tκ1 .
Now we can use the induction hypothesis on t to get (V⃗ ⊗ H ∗ )[[t]] ∈ Tκ2 . Then
by Lem. D.23, we have that (V⃗ ⊗ C⃗ H ∗ )[[t]] ∈ Tκ2 . Thus by using Prop. D.18, we have
(V⃗ ⊗ H ′ )][[t]] ∈ Tκ2 . Therefore by using Lem. D.25, we have that (V⃗ G ⊗ H)@ ∈ Tκ2 .
For (c), it is straightforward as the resulting graph does not change and thus the
condition is proved in (b)
Inductive Step Γ ⊢ t u : τ. In this case, we need to show that V⃗ G ∈ Tκ where
G = C⃗2 ([[t]] ⊗ [[u]])@.
First by Lem. D.20 we have that V⃗ C⃗2 ([[t]] ⊗ [[u]])@ ≺+ C⃗2 (V⃗ [[t]] ⊗ V⃗ [[u]])@. There⃗ V⃗ [[t]] ⊗ V⃗ [[u]])@ ∈ Tκ . Since by induction
fore by Prop D.18, it suffices to show that C(
hypothesis on t and u, we have that (V⃗ [[t]] ⊗ V⃗ [[u]])@ ∈ Tκ and then by Lem. D.23,
we have that ⃗
C(V⃗ [[t]] ⊗ V⃗ [[u]])@ ∈ Tκ .
Base Case (Γ ⊢ op : τ). We are going to show the case for op = $ and op = link.
Sub-Case Γ ⊢ $ : Int → Int → Int. In this case, since V⃗ is empty, we need to show
that G ∈ T!(!Int⊸!Int⊸!Int) . This graph indeed terminates and result in the same graph,
therefore we only need to prove that for any H1 : {e1 : !Int} → Γ ′ , such that H1 ∈ T!Int ,
(G ⊗ H1 )@ ∈ T!(Int⊸Int) .

12: 52

## PDF page 53

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

To prove the first condition, assuming a dataflow environment E , we would have
a sequence Init(E(G ⊗ H1 )@, e2 ) 7→∗ Final(E ′ H1′ G, e2 , (λ, −)) by using the condition
of H1 such that H1′ ∈ T!Int where e2 is the in-port of the bottom @-node. Therefore
it terminates and we then need to prove that H1′ G ∈ T!(Int⊸Int) . This graph indeed
terminates and result in the same graph. Therefore we only need to prove that for any
H2 : {e3 : !Int} → Γ ′′ such that H2 ∈ T!Int , (H1′ G ⊗ H2 )@ ∈ T!Int . Since it is of ground type
therefore we only need to prove that it terminates. Assuming a dataflow environment
E we would have a sequence from Init(E(H1′ G ⊗ H2 )@, e3 ) 7→∗ (E ′ (H1′ ⊗ H2′ )$, e3 , ↓, $, X :
S, ;). Depending on the value of X , it would transit to either one of the followings:
(12)

E ′ (H1′ ⊗ H2′ )$, (e, ↓, □, (n, g) : □, □)
′

E (H1′ C ⊗ H2′ C)(n)!, (e, ↓, □, (n, −) : □, □)

(13)

Therefore we have proved that for any dataflow environment, the graph indeed
terminates. Since in the first case, e3 will be connected to a dataflow environment,
thus we take the resulting term graph to be the empty graph and thus for any dataflow
environment it terminates. As for the second case a constant always satisfies the
logical predicate.
To prove the second condition (G ⊗ H1 )@ ∈ T!(Int⊸Int) , we need to prove that for
any H2 : {e3 : !Int} → Γ ′′ such that H2 ∈ T!Int , ((G ⊗ H1 )@ ⊗ H2 )@ ∈ T!Int . The proof is
similar to the case above.
Sub-Cases Γ ⊢ link : Cell → Int → Unit and Γ ⊢ assign : Cell → Int → Unit. These
cases are similar to the $-case but also needs validity (Lem. D.2) to prove that the cell
being update exists.
Sub-Cases Γ ⊢ root : Cell → Int → Unit. This case is similar to the link-case but we
also need to argue that when the token comes back to perform the r -rewrite, it would
always be connected to a dataflow environment as such it will terminate and that the
resulting graph satisfies the logical predicate.
Inductive Step Γ ⊢ if t then t 1 else t 2 : γ. Since only ground types are allowed in
the branches, this case follows the same technique shown in the previous case.
Proposition D.27 (Termination). For any closed well-typed term − ⊢ t : τ which is
recursion-free, Init([[− ⊢ t : τ]], r) 7→∗ Final(G, r, X ) for some G, X where X ∈ Ans r and r
is the root of [[− ⊢ t : τ]].
Proof. This is just a consequence of the fundamental lemma (Lem. D.26).
D.10 Type Soundness

Proposition D.28 (Interface preservation). For any valid state (G, δ) where G : Λ → ;,
all transitions send G to another graph G ′ with the same interface, i.e.
(G : Λ → ;) ∧ (G, δ) 7→ (G ′ , δ′ ) =⇒ G ′ : Λ → ;.

Proof. All the pass transitions indeed satisfy the statement as they do not change the
shape of the graph at all. As for rewrite transitions, the proof is done by inspecting
them one-by-one.

12: 53

## PDF page 54

Transparent Synchronous Dataflow

Corollary D.28.1. For any valid state (G, δ) where G : Λ → ;, if (G, δ) 7→∗ (G ′ , δ′ ) then
G ′ : Λ → ;.
Lemma D.29. For any valid state π, either
1. π is a answer state, or
2. there exists some π′ such that π 7→ π′ .
Proof. This is proved by case analysis on all possible valid states.
Proposition D.30 (Progress). For any closed well-typed term ⊢ t : τ, if Init([[⊢ t :
τ]], r) 7→n (G, δ) for some G, δ where r is the root of [[⊢ t : τ]], then either (G, δ) is a
final state or there exists another state (G ′ , δ′ ) such that (G, δ) 7→ (G ′ , δ′ ).
Proof. Since the initial state is valid therefore this is simply the consequence of
Cor. D.2.1 and Lem. D.29.
Theorem D.31 (Type soundness). For any closed well-typed term − ⊢ t : τ, let G : {r :
[[τ]]} → ; = [[− ⊢ t : τ]] then
1. if t is recursion-free then the execution from Init(G, r) will terminate,
2. if t is with recursion then the execution from Init(G, r) will not crash.
Proof. This is just a consequence of Cor. D.28.1, Prop. D.27 and Prop. D.30.

12: 54

## PDF page 55

Steven W.T. Cheung, Dan R. Ghica, and Koko Muroya

About the authors

Steven W.T. Cheung is a PhD student at the University of Birmingham. Contact him at wtc488@cs.bham.ac.uk.
Dan R. Ghica is a Professor of Semantics of Programming Languages at the University of Birmingham. Contact him at d.r.ghica@
cs.bham.ac.uk.
Koko Muroya is an Assistant Professor at RIMS, Kyoto University.
Contact her at kmuroya@kurims.kyoto-u.ac.jp.

12: 55
