Source: https://doi.org/10.46298/LMCS-18(1:1)2022
PDF sha256: 835c7733a1681fa8c67a868d67fd1d04bc436c0f908d3e2d9238072dbff8ec22
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of olimpieri_vaux_auclair_2022_on_the_taylor_expansion_of_lambda_terms_and_the_groupoid_structure_of_their_rigid_approximants.pdf

Transcription of `olimpieri_vaux_auclair_2022_on_the_taylor_expansion_of_lambda_terms_and_the_groupoid_structure_of_their_rigid_approximants.pdf` in this directory, 31 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-31 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Logical Methods in Computer Science
Volume 18, Issue 1, 2022, pp. 1:1–1:31
https://lmcs.episciences.org/

Submitted
Published

Aug. 07, 2020
Jan. 06, 2022

ON THE TAYLOR EXPANSION OF λ-TERMS AND THE GROUPOID
STRUCTURE OF THEIR RIGID APPROXIMANTS
FEDERICO OLIMPIERI AND LIONEL VAUX AUCLAIR
Aix-Marseille Univ, CNRS, I2M, Marseille, France
e-mail address: {federico.olimpieri,lionel.vaux}@univ-amu.fr

Abstract. We show that the normal form of the Taylor expansion of a λ-term is isomorphic
to its Böhm tree, improving Ehrhard and Regnier’s original proof along three independent
directions.
First, we simplify the final step of the proof by following the left reduction strategy
directly in the resource calculus, avoiding to introduce an abstract machine ad hoc.
We also introduce a groupoid of permutations of copies of arguments in a rigid variant
of the resource calculus, and relate the coefficients of Taylor expansion with this structure,
while Ehrhard and Regnier worked with groups of permutations of occurrences of variables.
Finally, we extend all the results to a nondeterministic setting: by contrast with previous
attempts, we show that the uniformity property that was crucial in Ehrhard and Regnier’s
approach can be preserved in this setting.

1. Introduction
1.1. Quantitative semantics. The field of quantitative semantics, in the sense originally
introduced by Girard [Gir88], is currently very lively within the linear logic community and
beyond. The basic idea is to interpret λ-terms as generalized power series, associated with
analytic maps — instead of continuous maps, à la Scott. The concept predates linear logic, and
in fact it provided the foundations for it, via its simpler, qualitative counterpart: coherence
spaces [Gir87]. It was later revisited, e.g. by Lamarche [Lam92] and Hasegawa [Has02],
to provide a denotational interpretation of linear logic proofs as matrices; but the current
momentum originates in the more recent introduction by Ehrhard [Ehr05] of models of linear
logic, based on a particular class of topological vector spaces, and thus accommodating
differentiation.
In that setting, the analytic maps associated with λ-terms are also smooth maps, i.e.
they are infinitely differentiable. This led to the differential extensions of λ-calculus [ER03]
and linear logic [ER06b] by Ehrhard and Regnier. The keystone of this line of work is an
analogue of the Taylor expansion formula, which allows to translate terms (or proofs) into
2012 ACM CCS: Theory of computation Denotational semantics; Theory of computation Lambda
calculus; Theory of computation Linear logic;
Key words and phrases: lambda-calculus, Taylor expansion, nondeterminism, normalization.
This article is an extended version of the abstract [OA18] presented at Linearity & TLLA’2018.

l

LOGICAL METHODS
IN COMPUTER SCIENCE DOI:10.46298/LMCS-18(1:1)2022

© TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS
CC
⃝
Creative Commons

## PDF page 2

1:2

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

infinite linear combinations of finite approximants [ER08]: in the case of λ-calculus, those
approximants are the terms of a resource calculus, in which the copies of arguments of a
function must be provided explicitly, and then consumed linearly, instead of duplicated or
discarded during reduction.
This renewed approach to quantitative semantics served as the basis of a considerable
amount of recent work: either as a framework for denotational models accommodating linear
combinations of maps [LMMP13, Lai16, TAO17, Ong17, etc.], possibly in contexts where
sums are constrained to a particular form, such as the probabilistic setting [DE11, TAO18,
etc.]; or as a tool for characterizing computational properties of programs via those of their
approximants [MP11, PTV16a, LL19, BM20, etc.].
Indeed, by contrast with denotational semantics, resource approximants retain a dynamics,
albeit very simple and finitary: the size of terms is strictly decreasing under reduction. The
seminal result relating the reduction of λ-terms with that of their approximants is the
commutation between Taylor expansion and normalization: Ehrhard and Regnier have shown
that the Taylor expansion M ∗ of a λ-term M can always be normalized, and that its normal
form is nothing but the Taylor expansion of the Böhm tree BT (M ) of M [ER08, ER06a]. In
particular, the normal form of Taylor expansion defines a proper denotational semantics.
1.2. Contributions. Ehrhard and Regnier’s proof of the identity BT (M )∗ = NF (M ∗ ) can
be summed up as follows:
Step 1: The non-zero coefficients of resource
terms in M ∗ do not depend on M . More
∑
1
∗
precisely, we can write M = s∈T (M ) m(s)
s, where T (M ) is the support set of
Taylor expansion and m(s) is an integer coefficient depending only on the resource
term s.
Step 2: The set T (M ) is a clique for the coherence relation obtained by setting s ¨ s′ iff s
and s′ differ only by the multiplicity of arguments in applications.
Step 3: The respective supports of N F (s) and∑
N F (s′ ) are disjoint whenever s ¨ s′ and
1
′
∗
s ̸= s . Then one can set N F (M ) = s∈T (M ) m(s)
N F (s), the summands being
pairwise disjoint.
Step 4: If s is uniform, i.e. s ¨ s, and t is in the support of N F (s) (the normal form of s,
which is a finite sum of resource terms) then m(t) divides m(s) and the coefficient of
t in N F (s) is m(s)
m(t) .
∑
∗
1
Step 5: By Step 1, BT (M )∗ =
t∈T (BT (M )) m(t) t. To deduce the identity BT (M ) =
NF (M ∗ ) from the previous results, it is then sufficient to prove that t ∈ T (BT (M ))
iff there exists s ∈ T (M ) such that t is in the support of N F (s).
The first two steps are easy consequences of the definitions. For Step 3, it is sufficient to
follow a well chosen normalization strategy, and check that it preserves coherence and that
if two coherent terms share a reduct then they are equal [ER08, Section 3]. Step 4 relies
on a careful investigation of the combinatorics of substitution in the resource calculus: this
involves an elaborate argument about the structure of particular subgroups of the group
of permutations of variable occurrences [ER08, Section 4]. Finally, Ehrhard and Regnier
establish Step 5 by relating Taylor expansion with execution in an abstract machine [ER06a].
In the present work, we propose to revisit this seminal result, along three directions.
(i) We largely simplify Step 5, relying on a technique introduced by the second author [Vau17]. We consider the hereditary head reduction strategy (a slight variant of

## PDF page 3

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:3

leftmost reduction, underlying the construction of Böhm trees) and show that it can be
simulated directly in the resource calculus, through Taylor expansion. We thus avoid
the intricacies of an abstract machine with resource state.
(ii) We extend all the results to a model of nondeterminism, introduced as a formal binary
choice operator in the calculus. By contrast with previous proposals to nondeterminism
from Ehrhard [Ehr10], or Pagani, Tasson and Vaux Auclair [PTV16b, Vau17], we show
that uniformity can still be relied upon, provided one keeps track of choices in the
resource calculus: the coherence associated with nondeterministic choice is then that
of the with connective (&) of linear logic.
(iii) We analyse coefficients in the Taylor expansion by introducing a groupoid whose
objects are rigid resource terms, i.e. resource terms in which multisets of arguments
are replaced with lists, and whose isomorphisms are permutation terms, i.e. terms
equipped with permutations that act on lists of arguments. This is more in accordance
with the intuition that m(s) is the number of permutations of arguments that leave s
(or rather, any rigid representation of s) invariant: Ehrhard and Regnier rather worked
on permutations of variable occurrences, which allowed them to consider groups rather
than a groupoid.
Although we implement all three contributions together, they are essentially independent
of each other. Indeed, the simplification of Step 5 brought by our contribution (i) only
concerns the compatibility of Taylor expansion with normalization at the level of support
sets, which does not involve coefficients; and it does not rely on uniformity, so its extension
to nondeterministic superpositions is straightforward.
Moreover, while our contribution (ii) enables us to enforce the uniformity condition of
Steps 2 to 4 in presence of a choice operator, it also ensures that distinct branches of a
choice have disjoint supports in the Taylor expansion. This treatment of nondeterminism
makes it completely transparent in the computation of coefficients. In particular, one could
straightforwardly extend all steps of Ehrhard and Regnier’s proof in this setting, ceterit
paribus.
Our contribution (iii) is thus not needed for that endeavour: it only offers an alternative
viewpoint on the combinatorics of substitution and normalization in the resource calculus,
in a uniform setting. Nonetheless, we consider it to be the main contribution of the paper,
precisely because of the new light it sheds on this dynamics, which in turn reveals possible
connections with other approaches.

1.3. Scope and related works. Our contribution (i) establishes that, although it is interesting in itself, Ehrhard and Regnier’s study of the relationship between elements in the
Taylor expansion of a term and its execution in an abstract machine is essentially superfluous
for proving the commutation theorem.
Barbarossa and Manzonetto have independently proposed another technique which
amounts to show that any reduction from an element of T (M ) can be completed into a
sequence of reductions simulating a β-reduction step [BM20, Section 4.1]. The strength of
our own proposal is that, rather than a mere simulation result, we establish a commutation
on the nose: hereditary head reduction commutes with Taylor expansion, at the level of
supports. Moreover, the Böhm tree of a λ-term is the limit of its hereditary head reducts,
which ensures that this commutation extends to normalization (Step 5). The same path was
followed by Dal Lago and Leventis [LL19] for the probabilistic case. Let us mention that the

## PDF page 4

1:4

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

commutation with hereditary head reduction actually holds not only at the level of supports,
but also taking coefficients into account [Vau17], in the more general setting of the algebraic
λ-calculus [Vau09] and without any additional condition: then, whenever the convergence of
the sum defining the normal form of Taylor expansion is assured, the main commutation
theorem ensues directly. This offers an alternative to the method of Ehrhard and Regnier
that is the focus of the present paper.
As stated before, our proposal (ii) to restore uniformity in a nondeterministic setting is
valid only because the resource calculus keeps a syntactic track of choices. The corresponding
constructors are exactly those used by Tsukada, Asada and Ong [TAO17] who were interested
in identifying equivalent execution paths of nondeterministic programs, but those authors do
not mention, nor rely upon any coherence property: this forbids Steps 1 to 4 and, instead,
they depend on infinite sums of arbitrary coefficients to be well defined. By contrast, Dal
Lago and Leventis have independently proposed nearly the same solution as ours [LL19,
Section 2.2], with only a minor technical difference in the case of sums.
The previous two proposals (i) and (ii) may be considered as purely technical improvements of the state of the art in the study of Taylor expansion. What we deem to be the
most meaningful contribution of the present paper is our study of the groupoid of rigid
resource terms. This provides us with a new understanding of the coefficients in the Taylor
expansion of a term, in which we can recast the proof of the commutation theorem, especially
Step 4: apart from this change of focus, the general architecture of our approach does not
depart much from that of Ehrhard and Regnier, but we believe the obtained combinatorial
results are closer to the original intuition behind the definition of m. In fact, a notable
intermediate result (Lemma 5.11, p.24) is that the function that maps each permutation term
to the permutation it induces on the occurrences of a fixed variable is functorial: one might
understand Ehrhard and Regnier’s proof of Step 4 as the image of ours through that functor.
Moreover, our study suggests interesting connections with otherwise independent approaches
to denotational semantics based on generalized species of structures [FGHW08, TAO17] and
rigid intersection type systems [MPV18].
It is indeed most natural to compare our proposals to the line of work of Tsukada,
Asada and Ong [TAO17, TAO18]. On the one hand, Tsukada et al. thrive to develop an
abstract understanding of reduction paths in a nondeterministic λ-calculus. They are led
to consider a polyadic calculus à la Mazza [Maz12, MPV18] with syntactic markers for
nondeterministic choice, moreover obeying linearity, typing and η-expansion constraints: in
particular, in that polyadic setting, λ-abstractions bind lists of variables, each bound variable
occurring exactly once. Then, to each simple type, they associate a groupoid of intersection
types: an isomorphism in this groupoid acts on polyadic rigid terms by permuting variables
bound in abstractions and lists of arguments in applications, in such a way that terms in its
source intersection type yield terms in its target. They show that the obtained collection of
groupoids form a bicategorical model of the simply typed λY-calculus, the interpretation
being given by a polyadic rigid variant of Taylor expansion. This interpretation is moreover
isomorphic to the one obtained in generalized species of structures [FGHW08].
On the other hand, our contribution (ii) shows that Ehrhard and Regnier’s technique can
already be adapted to the same kind of nondeterminism as the one considered by Tsukada et
al., without introducing any new concept. Also, besides having markers for nondeterministic
choice, the only difference between our rigid terms and the ordinary resource terms is that
arguments are linearly ordered: we do not consider a polyadic version. In fact, the same
rigid terms were already used by Tsukada et al. as intermediate representations of resource

## PDF page 5

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:5

terms, in order to recover Ehrhard and Regnier’s commutation theorem as a by-product of
their construction [TAO17, Section VI]. Moreover, our permutation terms are similar to their
typed isomorphisms and this suggests directions for further investigations.
A natural follow-up to the present work would thus be to explore possible variations
on our groupoid of permutation terms, and in particular adapt it to a polyadic setting, also
taking free variables into account. We expect this study to yield a bicategorical model of the
pure, untyped λ-calculus, similarly induced by rigid Taylor expansion à la Tsukada–Asada–
Ong. Then potential connexions between the obtained model and the construction of various
reflexive objects in the bicategory of generalized species of structures [FGHW08, Section 6.2]
should be investigated.
Another possible route to the untyped setting, actively developed by the first author,
is to construct a category satisfying a domain-like equation in the model of generalized
species [Oli20]. The objects in this category are very much like intersection types, except
that the usual identities between types (commutativity and, possibly, idempotency) are made
explicit as morphisms, which allows to develop a bicategorical treatment of intersection type
systems.
1.4. Structure of the paper. In the very brief Section 2, we review some results from
group theory that will be useful later.
In Section 3 we extend the ordinary untyped λ-calculus with a generic nondeterministic
choice operator, and present its operational semantics, inspired from that of the algebraic
λ-calculus, as well as the corresponding notion of (non extensional) Böhm trees.
Section 4 recalls and adapts the definitions of the resource calculus and Taylor expansion.
We obtain Step 2 as a straightforward consequence of the definitions and Step 5 by showing
that the support of Taylor expansion is compatible with hereditary head reduction — this is
our contribution (i). We moreover complete Step 1, making prominent the rôle played by
permutations acting on lists of resource terms.
Section 5 is the core of the paper, developing our main contribution (iii): we introduce
the rigid version of resource terms, and the isomorphisms between them, given by permutation terms; then we explore the relationship between the groupoid thus formed and the
combinatorics of Taylor expansion. We first show that the coefficient m(s) is nothing but
the cardinality of the group of automorphisms of any rigid version of s. Then we study the
structure of permutation terms between substitutions, first in the general case, then in the
uniform case — which is allowed in our nondeterministic setting thanks to our contribution (ii). We leverage the obtained results to determine the coefficient of any resource term
in the symmetric multilinear substitution associated with a reduction step issued from a
uniform redex.
The final Section 6 builds on the study of rigid resource terms and permutation terms to
achieve Steps 3 and 4. We conclude the paper with the commutation theorem.
2. Some basic facts on groups and group actions
Let G be a group, X be a set, and write (g, a) ∈ G × X ↦→ [g]a ∈ X for a left action of G
on X. If a ∈ X, then the stabilizer of a under this action is St(a) := {g ∈ G | [g]a = a},
which is a subgroup of G (also called the isotropy group of a); and the orbit of a is the set
[G]a := {[g]a | g ∈ G} ⊆ X. If H, K ⊆ G, we write HK := {hk | h ∈ H, k ∈ K}. If f : X → Y ,
X ′ ⊆ X and Y ′ ⊆ Y we write f (X ′ ) := {f (x) | x ∈ X ′ } and f −1 (Y ′ ) := {x | f (x) ∈ Y ′ }.

## PDF page 6

1:6

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

Assuming that G is finite, the following three facts are standard results of group theory.
Fact 2.1. For any a ∈ X,
Card ([G]a) =

Card (G)
Card (St(a))

.

Proof. [Lan02, Proposition 5.1].
Fact 2.2. Let H and K be any subgroups of G. Then
Card (HK) =

Card (H)Card (K)
Card (H ∩ K)

.

Proof. [Suz82, §(3.11)].
Fact 2.3. Let f : G → H be a group homomorphism and K be a subgroup of H. Then
Card (G)
Card (f (G))
=
Card (f −1 (K))
Card (f (G) ∩ K)

.

Proof. By the theorem of correspondence under homomorphisms [Suz82, Theorem 5.5 (1)],
observing that f (G) ∩ K = f (f −1 (K)).

3. A generic nondeterministic λ calculus
3.1. λ⊕ -terms. We consider a nondeterministic version of the λ-calculus in a pure, untyped
setting. The terms are those of the pure λ-calculus, augmented with a binary operator ⊕
denoting a form of nondeterministic superposition:1
Λ⊕ ∋ M, N, P, Q ::= x | λx.M | M N | M ⊕ N.
As usual λ⊕ -terms are considered up to renaming bound variables, and we write M [N/x] for
the capture avoiding substitution of N for x in M . We give precedence to application over
abstraction, and to abstraction over ⊕, and moreover associate applications on the left, so
that we may write λx.M N P ⊕ Q for (λx.((M N )P )) ⊕ Q. We write λ⃗x.M for a term of the
form λx1 . · · · λxn .M (possibly with n = 0).
Rather than specifying the computational effect of ⊕ explicitly, by reducing M ⊕ M ′ to
either M or M ′ , we consider two reductions rules
(M ⊕ N )P → M P ⊕ N P

and

λx.(M ⊕ N ) → λx.M ⊕ λx.N

in addition to the β-reduction rule. This is in accordance with most of the literature associated
with the Taylor expansion of λ-terms [ER03, Ehr10, PTV16b, Vau17] and quantitative
denotational semantics [Ehr05], where nondeterministic choice is modelled by the sum
of denotations: rather than the current state of a nondeterministic computation, a term
1Throughout the paper, we use a self explanatory if not standard variant of BNF notation for introducing
syntactic objects: here we define the set Λ⊕ as that inductively generated by variables, λ-abstraction,
application and sum, and we will denote terms using letters among M, N, P, Q, possibly with sub- and
superscripts.

## PDF page 7

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

(λx.M )N → M [N/x]
M → M′
λx.M → λx.M ′

(M ⊕ N )P → M P ⊕ N P

M → M′
M N → M ′N

M → M′
NM → NM′

1:7

λx.(M ⊕ N ) → λx.M ⊕ λx.N

M → M′
M ⊕ N → M′ ⊕ N

M → M′
N ⊕ M → N ⊕ M′

Figure 1: Reduction rules of the λ⊕ -calculus

represents a superposition of possible results.2 In particular, this approach allows to keep
standard rewriting notions and techniques such as confluence, standardization, etc. Formally,
→ is defined inductively by the inference rules of Figure 1: we simply extend the three base
cases contextually.
Observe that neither the definition of terms nor that of reduction make the choice operator
commutative, associative nor idempotent: e.g., x ⊕ y and y ⊕ x are two distinct normal forms.
It is possible to extend the reduction relation to validate the structural properties associated
with various kinds of superpositions (plain nondeterministic choice, probabilistic choice or a
more general quantitative superposition) while retaining good rewriting properties: we refer
the reader to the work of Leventis [Lev19] for an extensive study of this approach.
By contrast, for our purposes, it is essential to keep ⊕ as a free binary operator: following
Tsukada, Asada and Ong [TAO17], we keep track of the branching structure of choices
along the reduction. This information will be reflected in the Taylor expansion to be
introduced in Section 4: this is the key to recover the uniformity property while allowing for
nondeterministic superpositions of terms.
In fact we will not really consider the reduction relation → in the present paper, and
rather focus on the hereditary head reduction strategy obtained by defining the function
L : Λ⊕ → Λ⊕ inductively as follows:
L(M ⊕ N ) := L(M ) ⊕ L(N )
L(λ⃗x.λy.(M ⊕ N )) := λ⃗x.(λy.M ⊕ λy.N )
L(λ⃗x.(M ⊕ N )P Q1 · · · Qk ) := λ⃗x.(M P ⊕ N P )Q1 · · · Qk
L(λ⃗x.yQ1 · · · Qk ) := λ⃗x.yL(Q1 ) · · · L(Qk )
L(λ⃗x.(λy.M )N Q1 · · · Qk ) := λ⃗x.M [N/y]Q1 · · · Qk

.

Observe that this definition is exhaustive because any term in Λ⊕ is either of the form
M ⊕ N or of the form λ⃗x.λy.(M ⊕ N ) or of the form λ⃗x.RQ1 · · · Qk with R = (λy.M )N or
R = (M ⊕ N )P or R = y.

2In fact, only the rule (M ⊕N )P → M P ⊕N P is really necessary in order to enable the potential redexes that
can occur if M or N is an abstraction: in the setting of quantitative semantics, term application is left-linear.
The other reduction rule can be derived in case one admits extensionality in the models or the η-rule in the
calculus (here we don’t, though): having it in the calculus means that we follow a call-by-name interpretation
of nondeterministic evaluation, which amounts to λ-abstraction being linear [ADCP+ 14]. The results of the
paper could be developed similarly without it. We chose to keep it nonetheless, because it simplifies the
underlying theory of Böhm trees and allows us to obtain Ehrhard and Regnier’s results [ER08, ER06a] as a
particular case of our own.

## PDF page 8

1:8

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

⊥≤M
M ≤ M′
λx.M ≤ λx.M ′

M ≤N
N ≤P
M ≤P

M ≤M
M ≤ M′

Vol. 18:1

N ≤ N′

M N ≤ M ′N ′

M ≤ M′

N ≤ N′

M ⊕ N ≤ M′ ⊕ N′

Figure 2: The approximation order on Λ⊥
⊕.
It should be clear that M →∗ L(M ) and that L(M ) = M whenever M is normal3 but
the converse does not necessarily hold. It can moreover be shown that any normalizable term
M reaches its normal form by repeatedly applying the function L, for instance by adapting
the standardization techniques of Leventis [Lev16, Lev19], but this is not the focus of the
present paper. Indeed, we are only interested in the construction of Böhm trees, and we rely
on the fact that the Böhm tree of a term M can be understood as the limit of the sequence
(Ln (M ))n∈N , in a sense that we detail below. In particular, M and L(M ) have the same
Böhm tree (Lemma 3.3).
3.2. Böhm trees. We first define the set Λ⊥
⊕ of term approximants as follows:
Λ⊥
⊕ ∋ M, N, P, Q ::= ⊥ | x | λx.M | M N | M ⊕ N
⊥
then we consider the least partial order ≤ ⊆ Λ⊥
⊕ × Λ⊕ that is compatible with syntactic
⊥
constructs and such that ⊥ ≤ M for each M ∈ Λ⊕ . Formally, ≤ is defined inductively by
the rules of Figure 2.
The set N ⊂ Λ⊥
⊕ of elementary Böhm trees is the least set of approximants such that:
• ⊥ ∈ N;
• λ⃗x.xN1 · · · Nn ∈ N as soon as N1 , . . . , Nn ∈ N ;4 and
• N1 ⊕ N2 ∈ N as soon as N1 , N2 ∈ N .
For each λ⊕ -term M , we construct an elementary Böhm tree N (M ) as follows:

N (M ⊕ N ) := N (M ) ⊕ N (N )
N (λ⃗x.xQ1 · · · Qk ) := λ⃗x.xN (Q1 ) · · · N (Qk )
N (M ) := ⊥

in all other cases.

Lemma 3.1. For any M ∈ Λ⊕ , N (M ) ≤ N (L(M )).
Proof. By induction on M . If M = M1 ⊕ M2 then N (M ) = N (M1 ) ⊕ N (M2 ) and L(M ) =
L(M1 ) ⊕ L(M2 ), hence N (L(M )) = N (L(M1 )) ⊕ N (L(M2 )) and we conclude by induction
hypothesis. The case M = λ⃗x.xQ1 · · · Qk is similar. Otherwise, N (M ) = ⊥ ≤ N (L(M )).
Hence for a fixed λ⊕ -term M , the sequence (N (Ln (M )))n∈N is increasing, and we call
its downwards closure in N the Böhm tree of M , which we denote by BT (M ): i.e. we set
BT (M ) := {N ∈ N | ∃n ∈ N, N ≤ N (Ln (M ))}.
3If one considers ⊕ as a nondeterministic choice operator, normalizability is meant in its must flavour
here. Indeed, we do not perform the choice within the reduction relation itself, so M ⊕ N is normal iff M
and N both are.
4Here the sequence λ⃗
x of abstractions can be empty, and we can have n = 0, in which case the body of
the term is just the head variable.

## PDF page 9

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:9

Example 3.2. Let M = Θλy.(y ⊕ x) where Θ is Turing’s fixpoint combinator, so that
L3 (M ) = M ⊕ x. We can think of BT (M ) as the infinite tree ((· · · ⊕ x) ⊕ x) ⊕ x: formally,
BT (M ) = {⊥ ⊕ nx | n ∈ N} where we define inductively M ⊕ 0N = M and M ⊕ (n + 1)N =
(M ⊕ nN ) ⊕ N .
It could be shown that Böhm trees define a denotational semantics: if M → M ′ then
BT (M ) = BT (M ′ ).5 Here we just observe that Böhm trees are invariant under hereditary
head reduction, which follows directly from the definition:
Lemma 3.3. Let M ∈ Λ⊕ . Then BT (M ) = BT (L(M )).
It will be sufficient to follow this strategy in order to establish Step 5, i.e. the qualitative
version of the commutation between normalization and the Taylor expansion of λ⊕ -terms, to
be defined in the next section.
4. Taylor expansion in a uniform nondeterministic setting
In order to define Taylor expansion, we need to introduce an auxiliary language: the resource
calculus.
4.1. Resource terms. We call resource expressions the elements of ∆⊕ ∪ ∆!⊕ , where the set
∆⊕ of resource terms and the set ∆!⊕ of resource monomials are defined by mutual induction
as follows:6
∆⊕ ∋ s, t, u, v ::= x | λx.s | ⟨s⟩t̄ | s ⊕ • | • ⊕ s

∆!⊕ ∋ s̄, t̄, ū, v̄ ::= [s1 , . . . , sn ]

and, in addition to α-equivalence, we consider resource expressions up to permutations of
terms in monomials, so that [s1 , . . . , sn ] denotes a multiset of terms. We give precedence to
application and abstraction over − ⊕ • and • ⊕ −, and we write ⟨s⟩t̄1 · · · t̄n for ⟨· · · ⟨s⟩t̄1 · · · ⟩t̄n ,
so that we may write λx.⟨s⟩t̄ ū ⊕ • for (λx.(⟨⟨s⟩t̄⟩ū)) ⊕ •. We write λ⃗x.s for a term of the form
λx1 . · · · λxn .s. We moreover write s̄ · t̄ for the multiset union of s̄ and t̄, and if s̄ = [s1 , . . . , sn ]
then we write |s̄| := n for the size of s̄; in particular |s̄| = 0 iff s̄ is the empty multiset [],
which is neutral for multiset union.
If X is a set, we write N[X] for the freely generated commutative monoid over X:
formally, this is the same as the set of finite multisets of elements of X but we choose to
consider its elements as finite linear combinations of elements of X with coefficients in N. In
(!)
(!)
the following, we write ∆⊕ for either ∆⊕ or ∆!⊕ , so that N[∆⊕ ] is either N[∆⊕ ] or N[∆!⊕ ]:
when we consider a sum E of resource expressions, we always require E to be a sum of terms
(!)
(!)
or a sum of monomials, i.e. E ∈ N[∆⊕ ]. Then we write supp(E) ⊆ ∆⊕ for the support set
of E, which is finite. We extend the syntactic constructs of the resource calculus to finite
sums of resource expressions by linearity, so that:
∑
∑n
∑
∑
• if S = ni=1 si then
, • ⊕∑
S = ni=1 • ⊕ si and S ⊕∑
• = ∑ni=1 si ⊕ •;
∑mλx.S = i=1 λx.si∑
n
m
• if moreover T̄ = j=1 t̄j then ⟨S⟩T̄ = ni=1 m
i=1
j=1 [si ] · t̄j .
j=1 ⟨si ⟩t̄j and [S] · T̄ =
5Again, this would require the adaptation of standardization techniques to λ , similar to those developed
⊕

by Leventis for the probabilistic λ-calculus [Lev19].
6Recall that the cartesian product of vector spaces is given by the disjoint union of bases: this is the
intuition behind the operators − ⊕ • and • ⊕ −, which will serve in the Taylor expansion of the operator ⊕
of Λ⊕ . Again, we leave the exact computational behavior of ⊕ unspecified, and we treat it generically as a
pairing operator (without projections): in this we follow Tsukada et al. [TAO17].

## PDF page 10

1:10 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

⟨λx.s⟩t̄ →∂ ∂x s · t̄

⟨s ⊕ •⟩t̄ →∂ ⟨s⟩t̄ ⊕ •

λx.(s ⊕ •) →∂ λx.s ⊕ •

Vol. 18:1

⟨• ⊕ s⟩t̄ →∂ • ⊕ ⟨s⟩t̄

λx.(• ⊕ s) →∂ • ⊕ λx.s

s →∂ S ′

s →∂ S ′

s̄ →∂ S̄ ′

λx.s →∂ λx.S ′

⟨s⟩t̄ →∂ ⟨S ′ ⟩t̄

⟨t⟩s̄ →∂ ⟨t⟩S̄ ′

s →∂ S ′

s →∂ S ′

s →∂ S ′

s ⊕ • →∂ S ′ ⊕ •

• ⊕ s →∂ • ⊕ S ′

[s] · t̄ →∂ [S ′ ] · t̄

Figure 3: Reduction rules of the resource calculus with sums
(!)

For any resource expression e ∈ ∆⊕ , we write nx (e) for the number of occurrences of variable
x in e. If moreover ū = [u1 , . . . , un ] ∈ ∆!⊕ , we introduce the symmetric n-linear substitution
(!)
∂x e · ū ∈ N[∆⊕ ] of ū for the variable x in e, which is informally defined as follows:
⎧ ∑
⎨
e[uσ(1) /x1 , . . . , uσ(n) /xn ] if nx (e) = n
∂x e · ū := σ∈Sn
⎩0
otherwise
where x1 , . . . , xnx (e) enumerate the occurrences of x in e.7
Formally, ∂x e · ū is defined by induction on e, setting:
⎧
⎪
if y ̸= x and n = 0
⎨y
∂x y · ū := u1 if y = x and n = 1
⎪
⎩
0
otherwise
∂x λy.s · ū := λy.(∂x s · ū)
∂x (s ⊕ •) · ū := ∂x s · ū ⊕ •
∂x (• ⊕ s) · ū := • ⊕ ∂x s · ū
∑
∂x ⟨s⟩t̄ · ū :=
⟨∂x s · ūI1 ⟩∂x t̄ · ūI2
(I1 ,I2 )∈Q2 (n)

∂x [t1 , . . . , tk ] · ū :=

∑

[∂x t1 · ūI1 , . . . , ∂x tn · ūIk ]

(I1 ,...,Ik )∈Qk (n)

where Qk (n) denotes the set of k-tuples (I1 , . . . , Ik ) of (possibly empty) pairwise disjoint
⋃
subsets of {1, . . . , n} such that kj=1 Ij = {1, . . . , n},8 and we write ū{i1 ,...,ij } := [ui1 , . . . , uij ]
whenever 1 ≤ i1 < . . . < ij ≤ n. It is easy to check that ∂x e · t̄ ̸= 0 iff nx (e) = |t̄|.
The reduction of the resource calculus is the relation from resource expressions to finite
formal sums of resource expressions induced by the rules of Figure 3: the first rule is the
counterpart of β-reduction in the resource calculus; the next four rules implement the
commutation of ⊕ with abstraction and application to a monomial; the final six rules ensure
7Enumerating the occurrences of x in e only makes sense if we fix an ordering of each monomial in e: the
rigid resource calculus to be introduced later in the paper will allow us to give a more formal account of this
intuitive presentation. For now we stick to the alternative definition given in the next paragraph.
8Note that this data is equivalent to a function {1, . . . , n} → {1, . . . , k}.

## PDF page 11

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:11

(!)

the contextuality of the resulting relation. It is extended to a binary relation on N[∆⊕ ]
by setting e + F →∂ E ′ + F whenever e →∂ E ′ . As in the case of the original resource
calculus [ER08], the reduction relation →∂ is confluent and strongly normalizing. Confluence
may be proved following the same technique as for the original resource calculus [Vau17,
Section 3.4]: we do not provide any detail, because we will soon focus on a reduction strategy,
which is functional. For strong normalization, slightly more care is needed, because the size
of expressions does not necessarily decrease under reduction:
(!)

(!)

Lemma 4.1. The reduction →∂ ⊆ N[∆⊕ ] × N[∆⊕ ] is strictly normalizing.
(!)

Proof. If e ∈ ∆⊕ , we write nλ (e) ∈ N (resp. n⊕ (e) ∈ N) for the number of abstractions
(resp. of ⊕) occurring in e. Let #⊕ (e) denote the multiset of natural numbers containing a
value n⊕ (s) for each occurrence of a subterm λx.s or ⟨s⟩t̄ in e. Formally:
#⊕ (x) := [] #⊕ (λx.s) := [n⊕ (s)] · #⊕ (s) #⊕ (s ⊕ •) := #⊕ (s) #⊕ (• ⊕ s) := #⊕ (s)
#⊕ (⟨s⟩t̄) := [n⊕ (s)] · #⊕ (s) · #⊕ (t̄)

#⊕ ([s1 , . . . , sn ]) := #⊕ (s1 ) · · · · · #⊕ (sn )

where we use the same notations for multisets as for monomials.
(!)
We first establish that, for all e ∈ ∆⊕ , t̄ ∈ ∆!⊕ and e′ ∈ supp(∂x e · t̄), we have
nλ (e′ ) = nλ (e) − 1: the proof is by a straightforward induction on e.
Then, whenever e →∂ E ′ and e′ ∈ supp(E ′ ), we have n⊕ (e′ ) = n⊕ (e), and:
(1) either nλ (e′ ) = nλ (e) − 1;
(2) or nλ (e′ ) = nλ (e), and we can write #⊕ (e) = n̄ · [n + 1] and #⊕ (e′ ) = n̄ · [n].
The proof is by induction on the derivation of e →∂ E ′ : the β-redex case holds using the
previous result on multilinear substitution to obtain (1); the other four base cases yield (2);
and each other case follows straightforwardly by the induction hypothesis.
(!)
Now, for each E = e1 + · · · + en ∈ N[∆⊕ ], we write #λ (E) = [nλ (e1 ), . . . , nλ (en )]
and #⊕ (E) = #⊕ (e1 ) · · · · · #⊕ (en ). By the previous result and the definition of →∂ on
sums of resource expressions: if E →∂ E ′ then either #λ (E) < #λ (E), or #λ (E) = #λ (E)
and #⊕ (E) < #⊕ (E), considering the multiset order. We conclude since the latter is
well-founded.
(!)

We write NF (E) for the unique normal form of E ∈ N[∆⊕ ], which is a linear operator:
∑
∑
NF ( ki=1 ei ) = ki=1 NF (ei ). As stated before, we do not focus on the reduction relation
itself, and we rather consider the hereditary head reduction strategy obtained by defining the
(!)
(!)
function L : ∆⊕ → N[∆⊕ ] inductively as follows:
L(s ⊕ •) := L(s) ⊕ •
L(λ⃗x.λy.(s ⊕ •)) := λ⃗x.(λy.s ⊕ •)

L(• ⊕ s) := • ⊕ L(s)
L(λ⃗x.λy.(• ⊕ s)) := λ⃗x.(• ⊕ λy.s)

L(λ⃗x.⟨⟨s ⊕ •⟩t̄⟩ū1 · · · ūk ) := λ⃗x.⟨⟨s⟩t̄ ⊕ •⟩ū1 · · · ūk
L(λ⃗x.⟨⟨• ⊕ s⟩t̄⟩ū1 · · · ūk ) := λ⃗x.⟨• ⊕ ⟨s⟩t̄⟩ū1 · · · ūk
L(λ⃗x.⟨y⟩s̄1 · · · s̄k ) := λ⃗x.⟨y⟩L(s̄1 ) · · · L(s̄k )
L([s1 , . . . , sk ]) := [L(s1 ), . . . , L(sk )]
L(λ⃗x.⟨λy.s⟩t̄ ū1 · · · ūk ) := λ⃗x.⟨∂y s · t̄⟩ū1 · · · ūk
∑
∑
extended to sums of resource expressions by linearity, setting L( ki=1 ei ) := ki=1 L(ei ).
Again, it should be clear that e →∗∂ L(e): if e contains a redex (i.e. the left-hand side
of any of the first five rules of Figure 3) in head position, then L(e) is obtained by firing

## PDF page 12

1:12 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

this redex; otherwise each term in a monomial argument of the head variable is reduced,
following the same strategy inductively. Moreover, e = L(e) iff e is normal: we obtain an
equivalence because →∂ is strongly normalizing on sums of resource expressions and, if e is
not normal, L(e) is obtained by firing at least one redex in e.
Due to the definition of →∂ on sums and the linearity of L, these properties extend directly:
E →∗∂ L(E) and E = L(E) iff E is normal (i.e. it is a sum of normal expressions). It moreover
(!)
follows that L is normalizing: for all E ∈ N[∆⊕ ], there is n such that Ln (E) = NF (E).
4.2. Taylor expansion of λ⊕ -terms. The Taylor expansion of a λ⊕ -term will be an infinite
linear combination of resource terms: to introduce it, we first need some preliminary notations
and results.
If X is a set, we write Q+ ⟨X⟩ for the set of possibly infinite linear combinations of
elements of X with non negative rational coefficients (in fact we could use any commutative
semifield): equivalently, Q+ ⟨X⟩ is ∑
the set of functions from X to the set of non negative
rational numbers. We write A = a∈X Aa a ∈ Q+ ⟨X⟩ and then the support set of A is
supp(A) = {a ∈ X | Aa ̸= 0}.
All the syntactic constructs of resource expressions are extended to infinite linear
combinations, componentwise:
• if S ∈ Q+ ⟨∆⊕ ⟩ then
∑
∑
∑
λx.S :=
Ss (λx.s) , S ⊕ • :=
Ss (s ⊕ •) and • ⊕ S :=
Ss (• ⊕ s) ;
s∈∆⊕

s∈∆⊕

s∈∆⊕

• if moreover T̄ ∈ Q+ ⟨∆!⊕ ⟩ then
⟨S⟩T̄ :=

∑ ∑

Ss T̄t̄ (⟨s⟩t̄) ;

s∈∆⊕ t̄∈∆!⊕

• and if S1 , . . . , Sn ∈ Q+ ⟨∆⊕ ⟩ then
[S1 , . . . , Sn ] :=

∑

n
(∏

(s1 ,...,sn )∈∆n
⊕

i=1

)
Sisi [s1 , . . . , sn ] .

Observe indeed that each of these infinite sums is finite in each component: e.g., for each
s̄ ∈ ∆!⊕ , there are finitely many tuples (s1 , . . . , sn ) ∈ ∆n⊕ such that s̄ = [s1 , . . . , sn ].
Similarly we extend syntactic constructs to sets of resource expressions:
• if S ⊆ ∆⊕ then
λx.S := {λx.s | s ∈ S} ,

S ⊕ • := {s ⊕ • | s ∈ S} and • ⊕ S := {• ⊕ s | s ∈ S} ;

• if moreover T̄ ⊆ ∆!⊕ then
⟨S⟩T̄ := {⟨s⟩t̄ | s ∈ S, t̄ ∈ T̄ } ;
• and if S1 , . . . , Sn ⊆ ∆⊕ then
[S1 , . . . , Sn ] := {[s1 , . . . , sn ] | si ∈ Si for 1 ≤ i ≤ n} .
(!)

Considering subsets of ∆⊕ as infinite linear combinations of resource expressions with
boolean coefficients, this is just a variant of the previous construction (which can be carried
out in any commutative semifield). Moreover, syntactic constructs commute with the support
function: e.g., λx.supp(S) = supp(λx.S).

## PDF page 13

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:13

Let S ∈ Q+ ⟨∆⊕ ⟩. We define S n ∈ Q+ ⟨∆!⊕ ⟩ by induction on n: S 0 = [] and S n+1 = [S]·S n .
∑
1 n
Then we define the promotion of S as the series S ! = ∞
n=0 n! S : because the supports of
S n and S p are disjoint when n ̸= p, this sum is componentwise finite. If S ⊆ ∆⊕ is a set
of terms, we may also write S ! = {[s1 , . . . , sn ] | s1 , . . . , sn ∈ S} for the set of monomials of
terms in S, so that supp(S ! ) = supp(S)! for any S ∈ Q+ ⟨∆⊕ ⟩.
We define the Taylor expansion M ∗ ∈ Q+ ⟨∆⊕ ⟩ of M ∈ Λ⊕ inductively as follows:
x∗ := x
(λx.N )∗ := λx.N ∗
(P Q)∗ := ⟨P ∗ ⟩(Q∗ )!
(P ⊕ Q)∗ := (P ∗ ⊕ •) + (• ⊕ Q∗ ) .
Note that this definition follows the one for the ordinary λ-calculus given by Ehrhard and
Regnier [ER08], in the form described in their Lemma 18. We extend it to ⊕ by encoding
the pair of vectors (P ∗ , Q∗ ) as the sum vector (P ∗ ⊕ •) + (• ⊕ Q∗ ).9
Example 4.2. We have (x ⊕ x)∗ = (x ⊕ •) + (• ⊕ x) hence
(λx.(x ⊕ x))∗ = λx.((x ⊕ •) + (• ⊕ x)) = (λx.(x ⊕ •)) + (λx.(x ⊕ •))
and
(y(x ⊕ x))∗ =

∑ 1
n∈N

n!

⟨y⟩[(x ⊕ •) + (• ⊕ x)]n =

n
∑∑
n∈N i=0

1
⟨y⟩[x ⊕ •]i · [• ⊕ x]n−i
i!(n − i)!

.

Writing T (M ) := supp(M ∗ ) for the support of Taylor expansion, we obtain:
T (x) = {x}
T (λx.N ) = λx.T (N ) = {λx.t | t ∈ T (N )}
T (P Q) = ⟨T (P )⟩T (Q)! = {⟨s⟩[t1 , . . . , tn ] | s ∈ T (P ) and t1 , . . . , tn ∈ T (Q)}
T (P ⊕ Q) = (T (P ) ⊕ •) ∪ (• ⊕ T (Q)) = {s ⊕ • | s ∈ T (P )} ∪ {• ⊕ t | t ∈ T (Q)}
∑
so that M ∗ = s∈T (M ) Ms∗ s.
We can immediately check that Step 2 still holds for our extension of Taylor expansion to
(!)
(!)
λ⊕ -terms: we prove that T (M ) is always a clique for the coherence relation ¨ ⊆ ∆⊕ × ∆⊕
inductively defined by the rules of Figure 4. The first four rules are exactly those for the
ordinary resource calculus [ER08, Section 3], while the last three rules are reminiscent of
the definition of the cartesian product of coherence spaces [Gir87, Definition 5]. Again, this
is consistent with the fact that we treat ⊕ as a pairing construct, denoting an unspecified
superposition operation.
Observe that the relation ¨ is automatically symmetric, but not reflexive: e.g., [s, t] ̸¨
[s, t] when s ̸¨ t. We say a resource expression e is uniform if e ¨ e, so that uniform
9Note that the original notion of Taylor expansion for nondeterministic λ-terms (considered as algebraic
λ-terms without coefficients) interprets nondeterministic choice directly as a sum, setting (M ⊕ N )∗ =
M ∗ + N ∗ [Ehr10, PTV16b, Vau17]. Following Tsukada, Asada and Ong [TAO17], we can recover this notion,
by erasing the markers − ⊕ • and • ⊕ −, with one caveat: in general, this might yield infinite sums of
coefficients, because a single resource term without markers may be obtained from infinitely many terms with
markers. Define for instance x ⊕ n• by
∑ analogy with Example
∑∞ 3.2: x ⊕ 0• = x and x ⊕ (n + 1)• = (x ⊕ n•) ⊕ •.
Then forgetting markers in the sum ∞
x
⊕
n•
yields
i=0
i=0 x. And it turns out that normalizing the Taylor
expansion of nondeterministic terms does yield such sums: see Example 4.6.

## PDF page 14

1:14 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

x¨x

s ¨ s′
λx.s ¨ λx.s′
s ¨ s′
s ⊕ • ¨ s′ ⊕ •

s ¨ s′
t̄ ¨ t̄′
⟨s⟩t̄ ¨ ⟨s′ ⟩t̄′
s ¨ s′
• ⊕ s ¨ • ⊕ s′

Vol. 18:1

ti ¨ tj for 1 ≤ i, j ≤ n + m
[t1 , . . . , tn ] ¨ [tn+1 , . . . , tn+m ]
s ⊕ • ¨ • ⊕ s′
(!)

Figure 4: Rules for the coherence relation on ∆⊕ .
expressions form a coherence space in the usual sense.10 We call clique any set E of resource
expressions such that e ¨ e′ for all e, e′ ∈ E. In particular, the elements of a clique are
necessarily uniform.
We obtain the expected result by a straightforward induction on λ⊕ -terms:
Theorem 4.3 (Step 2). The Taylor support T (M ) is a clique.

4.3. Multiplicity coefficients. We now generalize Step 1 in our generic nondeterministic
1
setting: we can define a multiplicity coefficient m(s) ∈ N for each s ∈ ∆⊕ so that Ms∗ = m(s)
whenever s ∈ T (M ).
Given any set X and n ∈ N, we consider the left action of the group Sn of all permutations
of {1, . . . , n} on the set X n of n-tuples, defined as follows: if ⃗a = (a1 , . . . , an ) and σ ∈ Sn
then [σ]⃗a = (aσ−1 (1) , . . . , aσ−1 (n) ). Writing [σ]⃗a = (a′1 , . . . , a′n ), we obtain a′σ(i) = ai . Let us
recall that if ⃗a ∈ X n , then the stabilizer of ⃗a is St(⃗a) = {σ ∈ Sn∏| [σ]⃗a = ⃗a}.
If ⃗s = (s1 , . . . , sn ) ∈ ∆n⊕ and S ∈ Q+ ⟨∆⊕ ⟩, we write S ⃗s = ni=1 Ssi : observe that this
does not depend on the ordering of the si ’s, so if s̄ = [s1 , . . . , sn ] ∈ ∆!⊕ , we may as well write
S s̄ = S (s1 ,...,sn ) . We obtain:
Lemma 4.4. Let S ∈ Q+ ⟨∆⊕ ⟩ and s̄ ∈ supp(S ! ). If ⃗s = (s1 , . . . , sn ) is an enumeration of
S s̄
.
s̄, i.e. [s1 , . . . , sn ] = s̄, then (S ! )s̄ =
Card (St(⃗s))
Proof. By the definition of promotion, and by linearity, we obtain
∞
∑ 1
∑
S! =
S (s1 ,...,sn ) [s1 , . . . , sn ] .
n!
n
n=0

(s1 ,...,sn )∈∆⊕

If |s̄| = n, we thus obtain:
S s̄
.
n!
Observing that {(s1 , . . . , sn ) | [s1 , . . . , sn ] = s̄} is the orbit of any enumeration of s̄ under
the action of Sn , and that Card (Sn ) = n!, we conclude by Fact 2.1.
(S ! )s̄ = Card ({(s1 , . . . , sn ) | [s1 , . . . , sn ] = s̄})

10Note that, by contrast with the coherence relation considered by Dal Lago and Leventis for the Taylor

expansion of probabilistic λ-terms [LL19], e ¨ e′ does not imply the uniformity of e nor e′ : we have
s ⊕ • ¨ • ⊕ s′ without any condition on s and s′ . We could adapt our main results with a finer coherence,
similar to theirs, requiring s ¨ s and s′ ¨ s′ for s ⊕ • ¨ • ⊕ s′ to hold: uniform expressions and cliques are
the same for both relations. Nonetheless, we find it interesting that this additional hypothesis is not needed
for Step 3.

## PDF page 15

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:15

Let s ∈ ∆⊕ . We inductively define m(s), the multiplicity coefficient of s, as follows:
m(x) := 1
⎫
m(λx.s) ⎬
:= m(s)
m(s ⊕ •)
⎭
m(• ⊕ s)
m(⟨s⟩t̄) := m(s)m(t̄)
n1

m([t1 ]

nn

· · · · · [tn ] ) :=

n
∏

ni ! m(ti )ni

i=1

assuming the ti ’s are pairwise distinct in the case of a monomial. Again, this definition extends
straightforwardly the one given by Ehrhard and Regnier for their resource calculus [ER08,
Section 2.2.1], given that − ⊕ • and • ⊕ − are both linear. Observe that, considering the
(!)
function m as a vector m ∈ Q+ ⟨∆⊕ ⟩, if ⃗s is an enumeration of s̄ then m(s̄) = ms̄ Card (St(⃗s)).
Theorem 4.5 (Step 1). Let s ∈ T (M ). Then Ms∗ =

1
.
m(s)

Proof. The only interesting case is that of an application: M = P Q. Assume s ∈ T (M ); then
s = ⟨u⟩v̄ with u ∈ T (P ) and v̄ = [v1 , . . . , vn ] ∈ T (Q)! . By definition, Ms∗ = (⟨P ∗ ⟩(Q∗ )! )⟨u⟩v̄ =
Pu∗ (Q∗ )!v̄ . Setting ⃗v = (v1 , . . . , vn ), we obtain Ms∗ = Pu∗ (Q∗ )v̄ /Card (St(⃗v )) by Lemma 4.4.
By the induction hypothesis applied to P and Q, we obtain 1/Pu∗ = m(u) and 1/Q∗vi = m(vi )
hence 1/Ms∗ = m(u)mv̄ Card (St(⃗v )) = m(u)m(v̄) = m(s).
We can as well obtain Step 4 following Ehrhard and Regnier’s study of permutations of
variables occurrences, but here we choose to depart from their approach. At this point, indeed,
we hope the reader will share our opinion that the combinatorics of Taylor expansion is more
intimately connected with the action of permutations on the enumerations of monomials
occurring in resource expressions.
In the upcoming Section 5, we propose to flesh out this viewpoint, and to recast resource
expressions as equivalence classes of their rigid (i.e. non-commutative) representatives, up to
the isomorphisms of a groupoid of permutation terms inductively defined on the syntactic
structure.
The other remaining Steps 3 and 5 are purely qualitative properties of the Taylor support.
We choose to treat also Step 3 in the rigid setting, to be introduced later, because it is
essentially a property of rigid reduction. On the other hand, the commutation of Step 5 can
be established directly.

4.4. Taylor expansion of Böhm trees. The Taylor expansion of a Böhm tree is obtained
as follows. First we extend the definition of Taylor expansion from Λ⊕⋃to Λ⊥
⊕ by adding the
inductive case ⊥∗ := 0, hence T (⊥) = ∅. Then we set T (BT (M )) := B∈BT (M ) T (B).
We can already observe that if B ∈ N and s ∈ T (B) then s is normal: indeed, the
absence of redexes is preserved by the inductive definition of Taylor expansion. It follows
that any s ∈ T (BT (M )) is normal. Moreover, it is clear that Theorem 4.5 extends to term
1
approximants, hence Bs∗ = m(s)
whenever s ∈ T (B). Thus, it makes sense to define the
∑
1
Taylor expansion of a Böhm tree as: BT (M )∗ := s∈T (BT (M )) m(s)
s.

## PDF page 16

1:16 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

Example 4.6. Recall from Example 3.2 that if we set M = Θλy.(y ⊕ x) then BT (M ) =
{⊥ ⊕ nx | n ∈ N}. Observe that T (⊥ ⊕ nx)
∑ = {(• ⊕ x) ⊕ i• | 0 ≤ i < n} so that T (BT (M )) =
{(• ⊕ x) ⊕ n• | n ∈ N} and BT (M )∗ = ∞
i=0 (• ⊕ x) ⊕ n•, because m((• ⊕ x) ⊕ n•) = 1 for
each n ∈ N.
We shall achieve Step 5 by showing that the parallel left strategy in Λ⊕ can be simulated
in the support of Taylor expansion, and that T (BT (M )) is formed by accumulating the
normal forms reached from T (M ) by this strategy.
First, we extend the operations ∂x − ·−, L(−) and NF (−) to sets of resource expressions
in the following way:
⋃ ⋃
⋃
⋃
∂x E·T̄ :=
supp(∂x e·t̄) , L(E) :=
supp(L(e)) and NF (E) :=
supp(NF (e))
e∈E t̄∈T̄

e∈E

e∈E

(!)

whenever E ⊆ ∆⊕ and T̄ ⊆ ∆⊕ .11
Lemma 4.7. Let M be a λ⊕ -term. Then L(T (M )) = T (L(M )).
Proof. The proof is the same as for λ-terms [Vau17], the case of ⊕ being direct. The base
case requires to prove that T (M [N/x]) = ∂x T (M ) · T (N )! , which is done by a straightforward
induction on M .
Lemma 4.8. Let A, B ∈ Λ⊥
⊕ . If A ≤ B then T (A) ⊆ T (B).
Proof. By straightforward induction on the derivation of A ≤ B.
Lemma 4.9. For any M ∈ Λ⊕ , T (N (M )) = {s ∈ T (M ) | s is normal}.
Proof. We have T (N (M )) ⊆ T (M ) by Lemma 4.8 and the obvious fact that N (M ) ≤ M .
We deduce the inclusion ⊆, recalling that the Taylor support of elementary Böhm trees
contains normal terms only.
Conversely, if s ∈ T (M ) and s is normal, then either M = N ⊕ P and s = t ⊕ • or
s = • ⊕ u with t ∈ T (N ) or u ∈ T (P ); or M = λ⃗x.xQ1 · · · Qk and s = λ⃗x.⟨x⟩q̄1 · · · q̄k
with q̄i ∈ T (Qi )! for 1 ≤ i ≤ k. We obtain inductively t ∈ T (N (N )) or u ∈ T (N (P )) or
q̄i ∈ T (N (Qi ))! for 1 ≤ i ≤ k, and then s ∈ T (N (M )).
Step 5 then follows, using the fact that BT (M ) is the downwards closure of {N (Ln (M )) |
n ∈ N}:
Theorem 4.10 (Step 5). Let M ∈ Λ⊕ . Then T (BT (M )) = NF (T (M )).
11In contrast with the case of syntactic constructors in Section 4.2, extending these operations to infinite

linear combinations rather than sets requires some work.
In the case of ∂x − ·−, we can show that each expression e′ is in the support of finitely many sums of the
shape ∂x e · t̄, by observing that the size of the antecedents e and t̄ is at most that of e′ [Vau17, Lemma 3.7].
Then one can exploit the fact that the redexes fired in the reduction from e to L(e) are pairwise independent,
to deduce that each e′ is in the support of finitely many sums of the shape L(e): this is a particular case of a
result established by the second author for parallel reduction [Vau17, Section 6.2].
The case of NF
∑ (−) is even more intricate because, given an infinite linear combination S of resource
terms, the sum s∈∆⊕ Ss NF (s) is not well defined in general — indeed, it is easy to find an infinite family
of resource terms, all having the same nonzero normal form. Uniformity is one solution to this issue: if
the support of S is a clique then the summands NF (s) for s ∈ supp(S) have pairwise disjoint supports.
This result is the main ingredient of Step 3: it will be our Theorem 6.8 below. For a survey of alternative
approaches we refer to the study of this subject by the second author [Vau17].

## PDF page 17

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

x◁x

a◁s
λx.a ◁ λx.s
c◁s
d⃗ ◁ t̄
⟨c⟩d⃗ ◁ ⟨s⟩t̄

a◁s
a⊕•◁s⊕•
a1 ◁ t1

···

1:17

a◁s
•⊕a◁•⊕s
an ◁ tn

(a1 , . . . , an ) ◁ [t1 , . . . , tn ]

Figure 5: Rules for the rigid representation relation
⋃
Proof. Recall that NF (T (M )) = s∈T (M ) supp(NF (s)). The proof is by double inclusion.
(⊆) Let t ∈ T (BT (M )), i.e. t ∈ T (B) for some B ∈ BT (M ). By the definition
of BT (M ), there exists n ∈ N such that B ≤ N (Ln (M )), and then by Lemma 4.8 t ∈
T (N (Ln (M ))). By Lemma 4.9, t is normal and t ∈ T (Ln (M )). By Lemma 4.7, t ∈ Ln (T (M )),
hence there exists s ∈ T (M ) such that t ∈ supp(Ln (s)). Since t is normal, t ∈ supp(NF (s)).
(⊇) If t ∈ NF (T (M )) we can fix s ∈ T (M ) such
⋃ that t ∈ supp(NF (s)). Then there
exists n ∈ N such that NF (s) = Ln (s), hence t ∈ s∈T (M ) supp(Ln (s)) = Ln (T (M )). By
Lemma 4.7, t ∈ T (Ln (M )) and since t is normal, Lemma 4.9 entails that t ∈ T (N (Ln (M ))).
By the definitions of BT (M ) and T (BT (M )), we have N (Ln (M )) ⊆ BT (M ) and then
T (N (Ln (M ))) ⊆ T (BT (M )), and we obtain t ∈ T (BT (M )).

5. The groupoid of permutations of rigid resource terms
5.1. Rigid resource terms and permutation terms. We introduce the set D of rigid
resource terms and the set D! of rigid resource monomials by mutual induction as follows:
D ∋ a, b, c, d ::= x | λx.a | ⟨a⟩⃗b | • ⊕ a | a ⊕ •

D! ∋ ⃗a, ⃗b, ⃗c, d⃗ ::= (a1 , . . . , an ) .

Rigid resource terms are considered up to renaming of bound variables: the only difference
with resource terms is that rigid monomials are ordered lists rather than finite multisets. We
write |(a1 , . . . , an )| := n, and (a1 , . . . , an ) :: (an+1 , . . . , an+m ) := (a1 , . . . , an+m ). We write
D(!) for either D or D! and call rigid resource expression any rigid term or rigid monomial.
Again, for any r ∈ D(!) , we write nx (r) for the number of free occurrences of the variable x
in r, and we use notations and priority conventions similar to those for non rigid expressions:
e.g., we may write λ⃗x.⟨a⟩⃗b ⃗c ⊕ • for (λx1 . . . . .λxn .(⟨⟨a⟩⃗b⟩⃗c)) ⊕ •.
As we have already stated, rigid resource expressions are nothing but resource expressions
for which the order of terms in monomials matter. To make this connexion formal, consider
(!)
the representation relation ◁ ⊆ D(!) × ∆⊕ defined by the rules of Figure 5. Observe that
(!)
the relation ◁ is the graph of a surjection D(!) → ∆⊕ : if r ∈ D(!) , there exists a unique
(!)
(!)
e ∈ ∆⊕ such that r ◁ e, and then we write ∥r∥ := e; and any e ∈ ∆⊕ has at least one
rigid representation r ◁ e. Moreover observe that, if ⃗a ◁ t̄ and |⃗a| = n then for any σ ∈ Sn ,
[σ]⃗a ◁ t̄, i.e. ∥[σ]⃗a∥ = ∥⃗a∥.
We now introduce a syntax for the trees of permutations that can act on monomials at
any depth in a rigid expression. The language of such permutation expressions is given as
follows:
D ∋ α, β, γ, δ ::= idx | λx.α | ⟨α⟩β̃ | α ⊕ • | • ⊕ α

D! ∋ α̃, β̃, γ̃, δ̃ ::= (σ, (α1 , . . . , αn ))

## PDF page 18

1:18 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

idx : x ∼
=x

α:a∼
= a′
λx.α : λx.a ∼
= λx.a′

α:a∼
= a′
α⊕•:a⊕•∼
= a′ ⊕ •
σ ∈ Sn
α1 : a1 ∼
= a′

σ(1)

γ:c∼
= c′

Vol. 18:1

δ : d⃗ ∼
= d⃗′

⟨γ⟩δ : ⟨c⟩d⃗ ∼
= ⟨c′ ⟩d⃗′

α:a∼
= a′
•⊕α:•⊕a∼
= • ⊕ a′
· · · αn : an ∼
= a′

σ(n)

(σ, α1 , . . . , αn ) : (a1 , . . . , an ) ∼
= (a′1 , . . . , a′n )
Figure 6: Permutation expressions as morphisms between rigid expressions
where x ranges over variables and σ ranges over Sn in the pair (σ, (α1 , . . . , αn )). In other
words, a permutation term (resp. permutation monomial ) is nothing but a rigid term (resp.
rigid monomial), with a permutation attached with each list of arguments. In general, we
will simply write (σ, α1 , . . . , αn ) for the permutation monomial (σ, (α1 , . . . , αn )).
We say ϵ ∈ D(!) maps r ∈ D(!) to r′ ∈ D(!) if the statement ϵ : r ∼
= r′ is derivable from
the rules of Figure 6. We then write r ∼
= r′ if there exists some ϵ ∈ D(!) such that ϵ : r ∼
= r′ .
∼
As a direct consequence of the definitions, we obtain that = is nothing but the equivalence
(!)
kernel of the function r ∈ D(!) ↦→ ∥r∥ ∈ ∆⊕ :
Lemma 5.1. For all r, r′ ∈ D(!) , r ∼
= r′ iff ∥r∥ = ∥r′ ∥.
The equivalence classes for ∼
= are thus exactly the sets of rigid representations of each
resource expression. We can moreover organize the permutation expressions witnessing
this equivalence relation into a groupoid, whose objects are resource expressions. Observe indeed that, for each ϵ ∈ D(!) there is exactly one pair (r, r′ ) of rigid expressions
such that ϵ : r ∼
= r′ . Given r, r′ ∈ D(!) , the set of morphisms from r to r′ is then
(!)
′
D (r, r ) = {ϵ | ϵ : r ∼
= r′ }. The composition ϵ′ ϵ ∈ D(!) (r, r′′ ) of ϵ ∈ D(!) (r, r′ ) and
ϵ′ ∈ D(!) (r′ , r′′ ) is defined by induction on the syntax of rigid resource expressions in the
obvious way: the only interesting case is that of permutation monomials, for which we set
′
′
(σ ′ , α1′ , . . . , αn′ )(σ, α1 , . . . , αn ) := (σ ′ σ, ασ(1)
α1 , . . . , ασ(n)
αn ). And the identity idr on r is
the same as r, with each variable occurrence x replaced with idx , and with the identity
permutation attached with each monomial. Inverses are also defined inductively, the key
−1
case of monomials being: (σ, α1 , . . . , αn )−1 := (σ −1 , ασ−1
−1 (1) , . . . , ασ −1 (n) ).
∏
If ⃗a = (a1 , . . . , an ) and ⃗a′ = (a′1 , . . . , a′n ), we set ⃗
D(⃗a, ⃗a′ ) := ni=1 D(ai , a′i ): with rigid
⃗ which is the free strict monoidal category
monomials as objects, we obtain a groupoid D,
∑
⃗ a, [σ −1 ]⃗a′ ): D! is the free symmetric strict monoidal
over D. Moreover, D! (⃗a, ⃗a′ ) = σ∈Sn D(⃗
category over D. We call quasi-stabilizer of ⃗a the subgroup of Sn defined by
St ∼
a) := {σ ∈ Sn | for 1 ≤ i ≤ n, ai ∼
= aσ(i) } .
= (⃗
⃗ a, [σ −1 ]⃗a) ̸= ∅.
Observe that St ∼
a) = St((∥a1 ∥, . . . , ∥an ∥)) and σ ∈ St ∼
a) iff D(⃗
= (⃗
= (⃗
Let us write D(!) (r) for the group of automorphisms of r: D(!) (r) := D(!) (r, r). Similarly,
⃗ a) := D(⃗
⃗ a, ⃗a).
we will write D(⃗
⃗ a)).
Lemma 5.2. For any ⃗a = (a1 , . . . , an ) ∈ D! , Card (D! (⃗a)) = Card (St ∼
a) × D(⃗
= (⃗

## PDF page 19

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:19

by ϵ deProof. Since D(!) is a groupoid, for any morphism ϵ : r ∼
= r′ , postcomposition
∑
(!)
(!)
′
fines a bijection from D (r) to D (r, r ). It follows that D! (⃗a) = σ∈Sn ⃗
D(⃗a, [σ −1 ]⃗a) =
∑
∏n
∑
∏n
a) × ⃗
D(⃗a).
= (⃗
∼ (⃗
∼ (⃗
σ∈St =
a)
i=1 D(ai , aσ(i) ) is in bijection with
σ∈St =
a)
i=1 D(ai ) = St ∼
We are then able to formalize the interpretation of the multiplicity of a resource term s
as the number of permutations of monomials in s leaving any of its writings a ◁ s unchanged:
(!)

Lemma 5.3. Let e ∈ ∆⊕ and let r ◁ e. Then m(e) = Card (D(!) (r)).
Proof. By induction on the structure of e. We prove the multiset case. Assume e =
s̄ and ⃗a = (a1 , . . . , an ) ◁ s̄. Then we can write s̄ = [s1 , . . . , sn ] so that ai ◁ si and
the induction hypothesis gives m(si ) = Card (D(!) (ai )) for 1 ≤ i ≤ n. Then m(e) =
∏
⃗ a)), and we conclude
Card (St((s1 , . . . , sn ))) ni=1 Card (D(!) (ai )) = Card (St ∼
a)) × Card (D(⃗
= (⃗
by Lemma 5.2.

5.2. Rigid substitution. For any r ∈ D(!) and ⃗b ∈ D! such that |⃗b| = nx (r) = n, we define
the n-linear substitution r[⃗b/x] of ⃗b for x in r inductively as follows:
x[(b)/x] := b
y[()/x] := y
(a ⊕ •)[⃗b/x] := a[⃗b/x] ⊕ •
(• ⊕ a)[⃗b/x] := • ⊕ a[⃗b/x]
(λz.a)[⃗b/x] := λz.a[⃗b/x]
⟨c⟩d⃗ [⃗b0 :: ⃗b1 /x] := ⟨c[⃗b0 /x]⟩d⃗ [⃗b1 /x]
(a1 , . . . , an )[⃗b1 :: · · · :: ⃗bn /x] := (a1 [⃗b1 /x], . . . , an [⃗bn /x]})
⃗ and
where we assume that y ̸= x, z ∈
/ {x} ∪ F V (⃗b), |⃗b| = nx (a), |⃗b0 | = nx (c), |⃗b1 | = nx (d),
⃗
|bi | = nx (ai ) for 1 ≤ i ≤ n.
Observe that this substitution is only partially defined. In order to deal with the general
case, we will use the nullary sum of rigid expressions 0 ∈ N[D(!) ]: again, we consider all
the syntactic constructs to be linear so that we may write, e.g., λx.a for a ∈ D ∪ {0} with
λx.0 = 0. We call partial rigid expressions the elements of D(!) ∪ {0}: we generally use the
same typographic conventions for partial expressions as for regular ones.
Whenever r ∈ D(!) ∪ {0} and ⃗b ∈ D! ∪ {0}, we define the rigid substitution r[⃗b/x] of ⃗b for
the variable x in r as above if r ∈ D(!) , ⃗b ∈ D! and nx (r) = |⃗b|, and set r[⃗b/x] := 0 otherwise.
This rigid version of multilinear substitution will allow us to provide a more formal
account of the intuitive definition of the symmetric multilinear substitution ∂x e · ū, given in
Section 4.1: having fixed rigid representations r ◁ e and ⃗b ◁ t̄ = [t1 , . . . , tn ] with n = nx (e),
instead of the ambiguous
∑
e[tσ(1) /x1 , . . . , tσ(n) /xn ]
σ∈Sn

we can write
∑ ∥
∥
∥r[[σ]⃗b/x]∥ .
σ∈Sn

## PDF page 20

1:20 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

To prove that this coincides with the inductive definition of ∂x e · ū, we need to study how
the elements of ⃗b are routed to subexpressions of r in the substitution r[[σ]⃗b/x].
For this, we will rely on the following constructions on permutations. First, if σ ∈ Sn
and τ ∈ Sp , we define the concatenation σ ⊗ τ ∈ Sn+p by:
(σ ⊗ τ )(i) := σ(i)

and

(σ ⊗ τ )(n + j) := n + τ (j)

for 1 ≤ i ≤ n and 1 ≤ j ≤ p. This operation is associative and, more generally, we obtain
τ1 ⊗ · · · ⊗ τn ∈ Sk1 +···+kn whenever τ1 ∈ Sk1 , . . . , τn ∈ Skn . The tensor product notation is
justified since, in the category P of natural numbers and permutations, the concatenation of
permutations defines a tensor product (which is the sum of natural numbers on objects).
Moreover, for each (I1 , . . . , In ) ∈ Qn (k), writing Ij = {ij1 , . . . , ijkj } with ij1 < · · · < ijkj ,
∑
we set γI1 ,...,In (ijl ) := l + j−1
r=1 kr : then γI1 ,...,In is the unique permutation γ ∈ Sk such that
j
the map (j, l) ↦→ γ(il ) is strictly increasing, considering the lexicographic order on ∑
pairs.
Given a weak n-composition of k, i.e. a tuple (k1 , . . . , kn ) ∈ Nn such that k = nj=1 kj ,
we write Qkn1 ,...,kn (k) for the set of those (I1 , . . . , In ) ∈ Qn (k) such that Card (Ii ) = ki for
1 ≤ i ≤ n. We obtain:
Lemma 5.4. For any weak n-composition (k1 , . . . , kn ) of k, the function
Qkn1 ,...,kn (k) ×

n
∏

Skj → Sk

j=1

((I1 , . . . , In ), (σ1 , . . . , σn )) ↦→ (σ1 ⊗ · · · ⊗ σn )γI1 ,...,In
is bijective.
Proof. The inverse function is as follows: given σ ∈ Sk , we fix Ij := {i ∈ {1, . . . , k} |
∑j−1
∑j
r=1 kr < σ(i) ≤
r=1 kr }; then, using the above notations for the elements of Ij , for
each l ∈ {1, . . . , kj }, we fix σj (l) ∈ {1, . . . , kj } to be the unique l′ such that σ(ijl ) =
∑
l′ + j−1
r=1 kr .
Now we can show that the two definitions of symmetric multilinear substitution coincide:
Lemma∥5.5. If r∥◁ e and ⃗b ◁ t̄ then nx (r) = nx (e) and |⃗b| = |t̄|. Moreover ∂x e · t̄ =
∑
⃗ ∥
∥
σ∈S ⃗ r[[σ]b/x] .
|b|

Proof. The first two identities follow directly from the definitions. If nx (r) ̸= |⃗b| then both
sides of the third identity are 0. Otherwise, it is proved by induction on r.
Let us treat the case of a monomial: write r = (a1 , . . . , an ) and e = [s1 , . . . , sn ] with
ai ◁ si for 1 ≤ i ≤ n. Then
∑
∂x e · t̄ =
[∂x s1 · t̄I1 , . . . , ∂x sn · t̄In ]
(I1 ,...,In )∈Qn (|⃗b|)

=

∑
k ,...,kn ⃗
(I1 ,...,In )∈Qn1
(|b|)

where we write ki = nx (si ) for 1 ≤ i ≤ n.

[∂x s1 · t̄I1 , . . . , ∂x sn · t̄In ]

## PDF page 21

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:21

If I ⊆ {1, . . . , |⃗b|} then we write ⃗bI = (bi1 , . . . , bik ) where i1 < · · · < ik enumerate I. By
induction hypothesis we obtain
[ ∑
]
∑
∑ ∥
∥
∥
∥
⃗
⃗
∥
∥
∥
∥
∂x e · t̄ =
a1 [[σ1 ]bI1 /x] , . . . ,
an [[σn ]bIn /x]
k ,...,kn

(I1 ,...,In )∈Qn1

∑

=

k ,...,kn

(I1 ,...,In )∈Qn1

(|⃗b|)

σ1 ∈Sk1

∑
(|⃗b|) σ1 ∈Sk1

σn ∈Skn

∑ ∥ [
]∥
∥r [σ1 ]⃗bI :: · · · :: [σn ]⃗bIn /x ∥
···
1
σn ∈Skn

and we conclude, observing that [σ1 ]⃗bI1 :: · · · :: [σn ]⃗bIn = [(σ1 ⊗ · · · ⊗ σn )γI1 ,...,In ]⃗b, hence the
families
(
)
[σ1 ]⃗bI1 :: · · · :: [σn ]⃗bIn (I ,...,I )∈Qk1 ,...,kn (|⃗b|), (σ ,...,σ )∈S ×···×S
n
n
1
1
n
k1
kn
(
)
and [σ]⃗b σ∈S coincide up to reindexing via the bijection of Lemma 5.4.
|⃗
b|

∑
Informally, everything thus works out as if [s1 , . . . , sn ] = σ∈Sn (s1 , . . . , sn ), which is to
1
be related with the n!
coefficient in the Taylor expansion, cancelling out the cardinality of
Sn . Forgetting about coefficients, we obtain:
∥
∥
Corollary 5.6. If r◁e and ⃗b◁t̄ with nx (e) = |t̄|, then supp(∂x e·t̄) = {∥r[[σ]⃗b/x]∥ | σ ∈ S|⃗b| }.
Conversely, any rigid representative of a symmetric substitution is obtained as a rigid
substitution:
Lemma 5.7. If r′ ◁ e′ ∈ supp(∂x e · t̄) then nx (e) = |t̄| and there exist r ◁ e and ⃗b ◁ t̄ such
that r′ = r[⃗b/x].
Proof. By induction on e. If e = x then t̄ = [t] for some t ∈ ∆⊕ and e′ = t. If r′ ◁ e′ = t
then we can set r = x and ⃗b = (r′ ). If e = y ̸= x then t̄ = [] and we can set r = y and ⃗b = ().
The abstraction and sum cases follow immediately from the induction hypothesis.
If e = ⟨s⟩v̄, we write t̄ = [t1 , . . . , tn ] and obtain
∑
∂x e · t̄ =
⟨∂x s · t̄I1 ⟩∂x v̄ · t̄I2 .
(I1 ,I2 )∈Q2 (n)

Then e′ = ⟨s′ ⟩v̄ ′ with s′ ∈ supp(∂x s · t̄I1 ) and v̄ ′ ∈ supp(∂x v̄ · t̄I2 ) for some (I1 , I2 ) ∈ Q2 (n).
It follows that r′ = ⟨a⟩d⃗ with a ◁ s′ and d⃗ ◁ v̄ ′ . By induction hypothesis, we obtain c1 ◁ s,
⃗b1 ◁ t̄I , ⃗c2 ◁ v̄ and ⃗b2 ◁ t̄I such that a = c1 [⃗b1 /x] and d⃗ = ⃗c2 [⃗b2 /x]. Then we conclude by
1
2
setting r = ⟨c1 ⟩⃗c2 ◁ ⟨s⟩v̄ = e and ⃗b = ⃗b1 :: ⃗b2 ◁ t̄I1 · t̄I2 = t̄.
The case of monomials is similar.

5.3. Substitution for permutation expressions. The key intermediate result for Step 4
t̄)
is the fact that if e ¨ e and e′ ∈ supp(∂x e · t̄) then (∂x e · t̄)e′ = m(e)m(
m(e′ ) : this will be
established in Lemma 5.20, which concludes the present section. With that goal in mind, and
having characterized m(e) as the cardinality of the group D(!) (r) for any r ◁ e, it becomes
essential to study how the automorphisms of r′ ◁ e′ ∈ supp(∂x e · t̄) are related with those of
some r ◁ e and ⃗b ◁ t̄: by Lemma 5.7, we can choose r and ⃗b such that r′ = r[⃗b/x]. Then it
seems natural to consider some form of substitution for permutation expressions, following
the structure of rigid substitution.

## PDF page 22

1:22 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

We define the substitution of permutation terms for a variable as follows. Given ϵ ∈
D(!) (r, r′ ) and β⃗ ∈ ⃗
D(⃗b, ⃗b′ ) with |⃗b| = nx (r), we construct ϵ[ ⃗
β/x] by induction on ϵ:
(idx )[(β)/x] := β
(idy )[()/x] := idy
⃗
⃗
:= λy.α[β/x]
(λy.α)[β/x]
(α ⊕ •)[ ⃗
β/x] := α[ ⃗
β/x] ⊕ •
⃗
⃗
:= • ⊕ α[β/x]
(• ⊕ α)[β/x]
⃗2 /x]
(⟨γ⟩δ̃)[β⃗1 :: β⃗2 /x] := ⟨γ[β⃗1 /x]⟩δ̃[β
(σ, (α1 , . . . , αn ))[β⃗1 :: · · · :: β⃗n /x] := (σ, (α1 [β⃗1 /x], . . . , αn [β⃗n /x]))
⃗ |β⃗1 | = nx (γ), |β⃗2 | = nx (δ), and |β
⃗i | = nx (αi )
where we assume that y ̸= x, z ∈
/ {x} ∪ F V (β),
for 1 ≤ i ≤ n.
D(⃗b, ⃗b′ ), the source of ϵ[ ⃗
β/x] is obviously r[⃗b/x] but describing
If ϵ ∈ D(!) (r, r′ ) and β⃗ ∈ ⃗
(!)
⃗
its target is more intricate: in general, ϵ[β/x] ̸∈ D (r[⃗b/x], r′ [⃗b′ /x]).
Example 5.8. Consider the rigid monomials ⃗a = (x, x) and ⃗b = (⟨z⟩(), ⟨z⟩(z)). Writing τ for
the unique transposition of S2 , we obtain α = (τ, idx , idx ) ∈ D! (⃗a). Let β⃗ = (id⟨z⟩() , id⟨z⟩(z) ) ∈
⃗
⃗
⃗ ⃗b). Then α[β/x]
D(
= (τ, id⟨z⟩() , id⟨z⟩(z) ), hence α[β/x]
: a[⃗b/x] ∼
= (⟨z⟩(z), ⟨z⟩()) ̸= a[⃗b/x].
β/x], we first introduce another operation
To describe the image of r[⃗b/x] through ϵ[ ⃗
on permutations. If σ ∈ Sn and τi ∈ Ski for 1 ≤ i ≤ n, we define the multiplexing
σ · (τ1 , . . . , τn ) ∈ Sk1 +···+kn by:
(
)
σ(i)−1
i−1
∑
∑
(σ · (τ1 , . . . , τn )) l +
kj := τi (l) +
kσ−1 (j)
j=1

j=1

for 1 ≤ i ≤ n and 1 ≤ l ≤ ki . Multiplexing may be described in the category P of natural
numbers and permutations, which is symmetric strict monoidal, as follows: σ · (τ1 , . . . , τn ) =
σk1 ,...,kn ◦ (τ1 ⊗ · · · ⊗ τn ) where σk1 ,...,kn is the canonical symmetry map k1 + · · · + kn →
kσ−1 (1) + · · · + kσ−1 (n) = k1 + · · · + kn associated with the left action of σ on n-ary tensor
products in P. This decomposition of multiplexing is depicted in Figure 7.
Multiplexed permutations compose as follows:
Lemma 5.9. If σ, σ ′ ∈ Sn , τi ∈ Ski and τi′ ∈ Skσ−1 (i) for 1 ≤ i ≤ n, then
( ′
)(
)
′
′
σ · (τ1′ , . . . , τn′ ) σ · (τ1 , . . . , τn ) = (σ ′ σ) · (τσ(1)
τ1 , . . . , τσ(n)
τn )
and
(

)−1
−1
σ · (τ1 , . . . , τn )
= σ −1 · (τσ−1
−1 (1) , . . . , τσ −1 (n) )

.

Proof. We detail the proof only in case the result is not obvious to the reader from the above
categorical presentation of multiplexing. Let α = σ · (τ1 , . . . , τn ) and α′ = σ ′ · (τ1′ , . . . , τn′ ).

## PDF page 23

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

k

1:23

k

⏞ ⏟⏟1
⏞
( 1 + ··· + 1 ) +

···

⏞ ⏟⏟n ⏞
+ ( 1 + ··· + 1 )

τ1

τn

σk1 ,...,kn
+ ··· + 1
( 1
⏟ ⏞⏞ ⏟ ) +

···

kσ−1 (1)

·· + 1 )
+ ( 1⏟ + ·⏞⏞
⏟
kσ−1 (n)

Figure 7: Graphical representation of σ · (τ1 , . . . , τn )

For 1 ≤ i ≤ n and 1 ≤ l ≤ ki :
( ∑
)
( σ(i)−1
)
∑
( i−1
)
′
α α
kj + l = α
kσ−1 (j) + τi (l)
′

j=1

j=1
σ ′ (σ(i))−1

=

∑

′
kσ′ ′ −1 (j) + τσ(i)
(τi (l))

(writing ki′ = kσ−1 (i) )

j=1
(σ ′ σ)(i)−1

=

∑

′
k(σ′ σ)−1 (j) + (τσ(i)
τi )(l)

j=1

which establishes the first identity. The second identity follows directly.

The action of multiplexed permutations on sequences is as follows:
Lemma 5.10. Let ⃗b, ⃗b1 , . . . , ⃗bn ∈ D! , σ ∈ Sn and τi ∈ S|⃗bi | for all i ∈ {1, . . . , n}. If
⃗b = ⃗b1 :: · · · :: ⃗bn then [σ · (τ1 , . . . , τn )]⃗b = [τσ−1 (1) ]⃗bσ−1 (1) :: · · · :: [τσ−1 (n) ]⃗bσ−1 (n) .
Proof. Again, we detail the proof only in case the result is not obvious from the categorical
∑n
presentation. Set |⃗bi | = ki , so that |⃗b| =
ki . Write ⃗b′ = [σ · (τ1 , . . . , τn )]⃗b. For
i=1 ∑
∑
n
1 ≤ p ≤ |⃗b′ | = |⃗b| = j=1 kσ−1 (j) , we can write p = i−1
j=1 kσ −1 (j) + l with i ∈ {1, . . . , n} and
∑σ−1 (i)−1
l ∈ {1, . . . , kσ−1 (i) }. Then, by Lemma 5.9, (σ · (τ1 , . . . , τn ))−1 (p) = j=1
kj + τσ−1
−1 (i) (l)
and b′ = b(σ·(τ ,...,τ ))−1 (p) = (⃗bσ−1 (i) ) −1
= ([τσ−1 (i) ]⃗bσ−1 (i) )l .
p

1

n

τ −1
σ

(i)

(l)

## PDF page 24

1:24 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

We can now define the restriction ϵ↾x ∈ Snx (r) of ϵ ∈ D(!) (r, r′ ) to the occurrences of x
in r, by induction on ϵ:
idx ↾x := id{1}
idy ↾x := id∅
⎫
(λy.α)↾x ⎬
:= α↾x
(α ⊕ •)↾x
⎭
(• ⊕ α)↾x
(⟨γ⟩δ̃)↾x := γ↾x ⊗ δ̃↾x
(σ, α1 , . . . , αn )↾x := σ · (α1 ↾x , . . . , αn ↾x )
where we assume x ̸= y. Intuitively ϵ↾x is the permutation induced by ϵ on the occurrences
x1 , . . . , xnx (r) of x in r, taken from left to right.
We recall that P denotes the category of finite cardinals and permutations. For any
variable x, we define an application Fx from D(!) to P as follows: Fx (r) := nx (r) and
Fx (α) := α↾x .
Lemma 5.11. Fx is a functor from D(!) to P.
Proof. By induction on permutation expressions. We focus on the composition condition
for the list case. Let α̃ : ⃗a = (a1 , . . . , an ) ∼
= ⃗c = (c1 , . . . , cn ).
= ⃗b = (b1 , . . . , bn ) and β̃ : ⃗b ∼
By definition α̃ = (σ, α1 , . . . , αn ) and β̃ = (τ, β1 , . . . , βn ), for some σ, τ in Sn and with
αi : ai ∼
= bσ(i) and βi : bi ∼
= cτ (i) . The composition β̃ α̃ is then defined as the isomorphism
(τ σ, βσ(1) α1 , . . . βσ(n) αn ).
We have to prove that (β̃ α̃)↾x = β̃↾x α̃↾x , that is
(
)
(τ σ) · (βσ(1) α1 )↾x , . . . , (βσ(n) αn )↾x = (τ · (β1 ↾x , . . . , βn ↾x ))(σ · (α1 ↾x , . . . , αn ↾x ))
which is a direct consequence of the inductive hypothesis, (βσ(i) αi )↾x = βσ(i) ↾x αi ↾x for
1 ≤ i ≤ n, via Lemma 5.9.
In particular, the restriction of Fx to the automorphism group of some rigid expression
r is a group homomorphism from D(!) (r) to Snx (r) : its image D(!) (r)↾x is thus a subgroup of
Snx (r) . This homomorphism will play a crucial rôle in Section 5.4.
⃗
This operator allows us to describe the image of ϵ[β/x]
as follows:
⃗ = nx (r) then ϵ[β/x]
⃗ ∈ D(
⃗
⃗ ⃗b, ⃗b′ ) with |β|
Lemma 5.12. If ϵ : r ∼
: r[⃗b/x] ∼
= r′ and β
=
′
′
⃗
r [[ϵ↾x ]b /x].
Proof. By induction on the structure of r. The interesting case is the list case. Assume
r = (a1 , . . . , an ), r′ = (a′1 , . . . , a′n ), ϵ = (σ, α1 , . . . , αn ) and β⃗ = β⃗1 :: · · · :: β⃗n , with
⃗ ⃗bi , ⃗b′ ). By
αi : ai ∼
= a′σ(i) , ⃗b = ⃗b1 :: · · · :: ⃗bn , ⃗b′ = ⃗b′1 :: · · · :: ⃗b′n , |β⃗i | = nx (ai ) and β⃗i ∈ D(
i
′
∼
⃗
⃗
⃗
definition, we have α[β/x] = (σ, α1 [β1 /x], . . . , αn [βn /x]). Since αi : ai = a , we obtain
σ(i)

αi [β⃗i /x] : ai [⃗bi /x] ∼
= a′σ(i) [[αi ↾x ]⃗b′i /x] by induction hypothesis.
We obtain
( [
]
[
])
⃗
α[β/x]
: r[⃗b/x] ∼
= a′1 [ασ−1 (1) ↾x ]⃗b′σ−1 (1) /x , . . . , a′n [ασ−1 (n) ↾x ]⃗b′σ−1 (n) /x
[
]
= r′ [ασ−1 (1) ↾x ]⃗b′σ−1 (1) :: · · · :: [ασ−1 (n) ↾x ]⃗b′σ−1 (n) /x
and we conclude by Lemma 5.10.

## PDF page 25

Vol. 18:1

x¨x

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

a ¨ a′
λx.a ¨ λx.a′
a ¨ a′
a ⊕ • ¨ a′ ⊕ •

c ¨ c′
d⃗ ¨ d⃗′
⟨c⟩d⃗ ¨ ⟨c′ ⟩d⃗′
a ¨ a′
• ⊕ s ¨ • ⊕ s′

1:25

bi ¨ bj for 1 ≤ i, j ≤ n + m
(b1 , . . . , bn ) ¨ (bn+1 , . . . , bn+m )
a ⊕ • ¨ • ⊕ a′

.

Figure 8: Rules for the coherence relation on D(!) .
5.4. The combinatorics of permutation expressions under coherent substitution.
Substitution is injective on parallel permutation expressions, in the following sense:
Lemma 5.13. Let r, r′ ∈ D(!) and ⃗b, ⃗b′ ∈ D! with |⃗b| = nx (r) and |⃗b′ | = nx (r′ ), and let
ϵ, ϵ′ ∈ D(!) (r, r′ ) and ⃗
β, β⃗ ′ ∈ ⃗
D(⃗b, ⃗b′ ). If ϵ[ ⃗
β/x] = ϵ′ [β⃗′ /x] then ϵ = ϵ′ and β⃗ = β⃗ ′ .
Proof. By a straightforward induction on the structure of r.
On the other hand, surjectivity does not hold in general, because the substitution might
⃗ ⃗b, ⃗b′ ):
enable new morphisms r[⃗b/x] ∼
= r′ [⃗b′ /x], not induced by morphisms in D(!) (r, r′ ) and D(
Example 5.14. Let a = ⟨⟨y⟩(x)⟩⟨z⟩(x), a′ = ⟨⟨x⟩(y)⟩⟨z⟩(x) and ⃗b = (y, z). Then a[⃗b/x] =
a′ [⃗b/x] but a ∼
̸= a′ .
Observe that, in the above example, ∥a∥ ̸¨ ∥a′ ∥. Indeed, in the following, we will establish
that coherence allows to restore a precise correspondence between the permutation expressions
on a substitution r[(b1 , . . . , bn )/x] and the (1 + n)-tuples of permutation expressions on r
and each of the bi ’s respectively. It will be useful to consider the coherence relation defined
on rigid expressions by the rules of Figure 8, so that r ¨ r′ iff ∥r∥ ¨ ∥r′ ∥. Then we obtain:
Lemma 5.15. Let r, r′ ∈ D(!) and ⃗b, ⃗b′ ∈ D! with |⃗b| = nx (r) and |⃗b′ | = nx (r′ ). If r ¨ r′
⃗ ⃗b, [ϵ↾−1 ]⃗b′ ) such that
then for all φ ∈ D(!) (r[⃗b/x], r′ [b⃗′ /x]) there exist ϵ ∈ D(!) (r, r′ ) and β⃗ ∈ D(
x
⃗
φ = ϵ[β/x].
Proof. By induction on the structure of r: the coherence hypothesis r ¨ r′ induces that r
and r′ are of the same syntactic nature.
If r = x then r′ = x and we can write ⃗b = (b), ⃗b′ = (b′ ) with φ : b ∼
= b′ . Then we set
′
ϵ = idx and β⃗ = (φ). If r = y ̸= x then r = y and φ = idy , and we set ϵ = idy and β⃗ = ().
The abstraction, application and sum cases follow straightforwardly from the induction
hypotheses. We detail the list case.
We have r = (a1 , . . . , an ) and r′ = (a′1 , . . . , a′m ). Since φ : r[⃗b/x] ∼
= r′ [⃗b′ /x] we must
have m = n, ⃗b = ⃗b1 :: · · · :: ⃗bn , ⃗b′ = ⃗b′1 :: · · · :: ⃗b′n and φ = (σ, γ1 , . . . , γn ) with γi ∈
D(!) (ai [⃗bi /x], a′σ(i) [⃗b′σ(i) /x]). Since r ¨ r′ we have in particular ai ¨ a′σ(i) for 1 ≤ i ≤ n.
By the induction hypothesis, we obtain γi = αi [β⃗i /x] with αi ∈ D(!) (ai , a′ ) and
σ(i)

∼ ′
⃗′
β⃗i ∈ ⃗
D(⃗bi , [αi ↾−1
x ]bσ(i) ). Then by definition ϵ := (σ, α1 , . . . , αn ) : r = r and
−1 ⃗ ′
⃗′
β⃗ := β⃗1 :: · · · :: β⃗n : ⃗b ∼
= [α1 ↾−1
x ]bσ(1) :: · · · :: [αn ↾x ]bσ(n)
−1 ⃗ ′
= [σ −1 · (ασ−1 (1) ↾−1
x , . . . , ασ −1 (n) ↾x )]b

(by Lemma 5.10)

−1
−1
and it remains only to prove that σ −1 · (ασ−1 (1) ↾−1
x , . . . , ασ −1 (n) ↾x ) = ϵ↾x , which follows
from Lemma 5.9.

## PDF page 26

1:26 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

⃗ ∈ D! (⃗b, ⃗b′ ), hence:
In particular, we obtain (ϵ↾x , β)
Corollary 5.16. If r ¨ r′ and r[⃗b/x] ∼
= r′ [b⃗′ /x] then r ∼
= r′ and ⃗b ∼
= ⃗b′ .
Given r ◁ e, ⃗b ◁ t̄ and e′ ∈ supp(∂x e · t̄) such that r[⃗b/x] ◁ e′ , we are about to determine
the coefficient of e′ in ∂x e · t̄ by enumerating the permutations σ such that r[[σ]⃗b/x] ◁ e′ , i.e.
r[[σ]⃗b/x] ∼
= r[⃗b/x]. We thus define Hx (r, ⃗b) := {σ ∈ Snx (r) | r[⃗b/x] ∼
= r[[σ]⃗b/x]} whenever
|⃗b| = nx (r).
Lemma 5.17. Let r ∈ D(!) and ⃗b ∈ D! with |⃗b| = nx (r). If r ¨ r then Hx (r, ⃗b) =
⃗
D(!) (r)↾x St ∼
= (b).
(!)
⃗
⃗ ⃗ ⃗ ⃗
Proof. Let τ ∈ St ∼
= (b): by definition, we obtain β ∈ D(b, [τ ]b). If moreover ϵ ∈ D (r) then,
⃗
by Lemma 5.12, ϵ[β/x]
∈ D(!) (r[⃗b/x], r[[ϵ↾x τ ]⃗b/x]) hence ϵ↾x τ ∈ Hx (r, ⃗b). It remains only to
⃗
⃗
show that the function (ϵ, τ ) ∈ D(!) (r) × St ∼
= (b) ↦→ ϵ↾x τ ∈ Hx (r, b) is surjective.
(!)
⃗
⃗
⃗
If σ ∈ Hx (r, b), there exists φ ∈ D (r[b/x], r[[σ]b/x]). Since r ¨ r, we can apply
−1
⃗
⃗
Lemma 5.15 and obtain ϵ ∈ D(!) (r) and β⃗ ∈ ⃗
D(⃗b, [ϵ↾−1
= (b),
x σ]b): in particular, ϵ↾x σ ∈ St ∼
−1
and we conclude since σ = ϵ↾x (ϵ↾x σ).

Our argument will moreover rely on the following construction: if |⃗b| = nx (r), we set
−1
(!)
⃗
⃗
Kx (r, ⃗b) := {ϵ ∈ D(!) (r) | ϵ↾x ∈ St ∼
= (b)} = Fx (St ∼
= (b)), which is a subgroup of D (r)
because Fx is a group homomorphism from D(!) (r) to Snx (r) by Lemma 5.11.
Lemma 5.18. Let r ∈ D(!) and ⃗b ∈ D! with |⃗b| = nx (r). If r ¨ r then Card (D(!) (r[⃗b/x])) =
⃗ ⃗b)).
Card (Kx (r, ⃗b))Card (D(
(!) ⃗
⃗
⃗
Proof. By Lemma 5.12, if ϵ ∈ D(!) (r) and β⃗ ∈ ⃗
D(⃗b, [ϵ↾−1
x ]b) then ϵ[β/x] ∈ D (r[b/x]). If
−1
⃗
⃗
moreover ϵ ∈ Kx (r, b) then ϵ↾x ∈ St ∼
= (b): as already remarked in the proof of Lemma 5.2,
−1
⃗
⃗
⃗
⃗ ⃗b)). It is thus sufficient to establish that the
this entails that Card (D(b, [ϵ↾x ]b)) = Card (D(
∑
⃗
substitution operation (ϵ, ⃗
β) ↦→ ϵ[β/x] defines a bijection from ϵ∈Kx (r,⃗b) ⃗
D(⃗b, [ϵ↾−1
x ]b) to
D(!) (r[⃗b/x]). This fact derives immediately from Lemma 5.13 (injectivity) and Lemma 5.15
(surjectivity).

Lemma 5.19. Let r ∈ D(!) and ⃗b ∈ D! with r ¨ r and |⃗b| = nx (r). Then
Card (D(!) (r))Card (D! (⃗b))
Card (Hx (r, ⃗b)) =
.
Card (D(!) (r[⃗b/x]))
(!)
⃗
Proof. Write k = nx (r). We know that St ∼
= (b) and D (r)↾x are subgroups of Sk . Lemma 5.17
and Fact 2.2 entail that
⃗
Card (D(!) (r)↾x )Card (St ∼
= (b))
Card (Hx (r, ⃗b)) =
.
⃗
Card (D(!) (r)↾x ∩ St ∼
= (b))

Using Lemma 5.18, it will thus be sufficient to prove:
⃗
Card (D(!) (r))Card (D! (⃗b))
Card (D(!) (r)↾x )Card (St ∼
= (b))
=
⃗
⃗ ⃗b))
Card (Kx (r, ⃗b))Card (D(
Card (D(!) (r)↾x ∩ St ∼
= (b))
which simplifies to
Card (D(!) (r))
Card (D(!) (r)↾x )
=
⃗
Card (Kx (r, ⃗b))
Card (D(!) (r)↾x ∩ St ∼
= (b))

## PDF page 27

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:27

by Lemma 5.2. We conclude by Fact 2.3, recalling that D(!) (r)↾x = Fx (D(!) (r)) and Kx (r, ⃗b) =
⃗
Fx−1 (St ∼
= (b)).
(!)

Lemma 5.20. Let e ∈ ∆⊕ be such that e ¨ e and let t̄ ∈ ∆!⊕ . If e′ ∈ supp(∂x e · t̄) then
m(e)m(t̄)
(∂x e · t̄)e′ =
.
m(e′ )
Proof. Let r′ ◁e′ and k = nx (e). By Lemma 5.7 there exists r◁e and ⃗b◁t̄ such that r′ = r[⃗b/x].
Then, by Lemma 5.5, (∂x e · t̄)e′ = Card ({σ ∈ Sk | r[[σ]⃗b/x] ◁ e′ }) = Card (Hx (r, ⃗b)). Then
we conclude by Lemmas 5.19 and 5.3.

6. Normalizing the Taylor expansion
In this final section we leverage our results on the groupoid of rigid expressions and permutation expressions in order to achieve Steps 3 and 4. This allows us to complete the proof of
commutation between Taylor expansion and normalization.
6.1. Normalizing resource expressions in a uniform setting. Lemma 5.20 is almost
sufficient to obtain Step 4, as it fixes the coefficients in a hereditary head reduction step
from a uniform expression:
(!)

Lemma 6.1. Let e ∈ ∆⊕ with e ¨ e. If e′ ∈ supp(L(e)) then (L(e))e′ =

m(e)
.
m(e′ )

Proof. By induction on the structure of e applying Lemma 5.20 in the redex case: observe
indeed that if e = λ⃗x.⟨λy.s⟩t̄ ū1 · · · ūk then e′ = λ⃗x.⟨v⟩ū1 · · · ūk with v ∈ supp(∂y s · t̄), and
t̄)
m(e)
m(s)m(t̄)
then (L(e))e′ = (∂y s · t̄)v = m(s)m(
and we conclude since m(e
′) =
m(v)
m(v) . All the other
cases follow directly from the induction hypothesis by multilinearity.
To iterate Lemma 6.1 along the reduction sequence to the normal form, we first need to
show that uniformity is preserved by L. As before, we prefer to focus on the rigid setting
first, and we will only consider the hereditary head reduction defined as follows:12
L(a ⊕ •) := L(a) ⊕ •

L(• ⊕ a) := • ⊕ L(a)

L(λ⃗x.λy.(a ⊕ •)) := λ⃗x.(λy.a ⊕ •) L(λ⃗x.λy.(• ⊕ a)) := λ⃗x.(• ⊕ λy.a)
L(λ⃗x.⟨⟨a ⊕ •⟩⃗b⟩⃗c1 · · · ⃗ck ) := λ⃗x.⟨⟨a⟩⃗b ⊕ •⟩⃗c1 · · · ⃗ck
L(λ⃗x.⟨⟨• ⊕ a⟩⃗b⟩⃗c1 · · · ⃗ck ) := λ⃗x.⟨• ⊕ ⟨a⟩⃗b⟩⃗c1 · · · ⃗ck
L(λ⃗x.⟨y⟩⃗a1 · · · ⃗ak ) := λ⃗x.⟨y⟩L(⃗a1 ) · · · L(⃗ak )
L((a1 , . . . , ak )) := (L(a1 ), . . . , L(ak ))
L(λ⃗x.⟨λy.a⟩⃗b ⃗c1 · · · ⃗ck ) := λ⃗x.⟨a[⃗b/y]⟩⃗c1 · · · ⃗ck
12Note that the reduction from ⟨λx.a⟩⃗b to a[⃗b/x] is not well behaved in general: its contextual extension

is not even confluent, because it forces the order in which variable occurrences are substituted. Consider for
instance the term (λx.⟨λy.⟨y⟩(x)⟩(x))(z1 , z2 ) which has two distinct normal forms: ⟨z1 ⟩z2 and ⟨z2 ⟩z1 . This
rigid calculus is thus not very interesting per se, and we only consider it as a tool to analyze the dynamics of
the resource calculus.

## PDF page 28

1:28 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

extended to partial rigid expressions by setting L(0) := 0. By an analogue of Lemma 4.1, for
any r ∈ D(!) , there exists k ∈ N such that Lk (r) is normal, and then we write NF (r) = Lk (r).
Moreover, r is in normal form iff L(r) = r.
(!)

Lemma 6.2. If e ∈ ∆⊕ then:
(1) supp(L(e)) = {∥L(r)∥ | r ◁ e and L(r) ̸= 0};
(2) supp(NF (e)) = {∥NF (r)∥ | r ◁ e and NF (r) ̸= 0}.
Proof. We first prove that r′ ◁ e′ ∈ supp(L(e)) iff there exists r ◁ e with r′ = L(r), which
gives the first result: this is done by a straightforward induction on the structure of e, using
Corollary 5.6 for the β-redex case.
Now fix k ∈ N such that NF (e) = Lk (e): by iterating the previous result, we obtain
′
r ◁ e′ ∈ supp(NF (e)) iff there exists r ◁ e with r′ = Lk (r). Then we conclude, observing
that if r′ ◁ e′ , then r′ is in normal form iff e′ is.
Lemma 6.3. If r ¨ r′ and ⃗b ¨ ⃗b′ with nx (r) = |⃗b| and nx (r′ ) = |⃗b′ | then r[⃗b/x] ¨ r′ [⃗b′ /x].
Proof. By a straightforward induction on the derivation of r ¨ r′ .
Lemma 6.4. For all r, r′ ∈ D(!) such that r ¨ r′ :
(1) if L(r) ̸= 0 and L(r′ ) ̸= 0 then L(r) ¨ L(r′ );
(2) if NF (r) ̸= 0 and NF (r′ ) ̸= 0 then NF (r) ¨ NF (r′ ).
Proof. The first item is easily established by induction on r, using Lemma 6.3 in the case of
a β-redex. Having fixed k such that both NF (r) = Lk (r) and NF (r′ ) = Lk (r′ ), the second
item follows by iterating the first one.
We have thus established that L preserves coherence of rigid expressions. It follows that
L preserves cliques of resource expressions:
(!)

Lemma 6.5. If E ⊆ ∆⊕ is a clique, then both L(E) and NF (E) are cliques.
Proof. As a direct consequence of Lemmas 6.2 and 6.4, we obtain that: if e ¨ e′ then, for all
e0 ∈ supp(L(e)) and e′0 ∈ supp(L(e′ )) (resp. e0 ∈ supp(NF (e)) and e′0 ∈ supp(NF (e′ ))), we
have e0 ¨ e′0 . The result follows straightforwardly.
Step 3 amounts to the fact that distinct coherent expressions have disjoint normal forms.
In other words, if the normal forms of two coherent expressions intersect on a common
element, then they must coincide. This result will follow from the following rigid version,
which states that coherent rigid expressions with isomorphic normal forms are isomorphic:
Lemma 6.6. For all r, r′ ∈ D(!) such that r ¨ r′ :
(1) if L(r) ∼
= L(r′ ) then r ∼
= r′ ;
′
∼
(2) if NF (r) = NF (r ) then r ∼
= r′ .
Proof. Observe that ∼
= is defined on rigid expressions only so that if, e.g., L(r) ∼
= L(r′ )
′
then in particular L(r) ̸= 0 ̸= L(r ). The first item is established by induction on r, using
Corollary 5.16 in the case of a β-redex. Having fixed k such that both NF (r) = Lk (r) and
NF (r′ ) = Lk (r′ ), the second item follows by iterating the first one, thanks to Lemma 6.4.
Note that the converse does not hold, even in the uniform case: two uniform, isomorphic
and coherent rigid expressions may yield normal forms that are not isomorphic.

## PDF page 29

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:29

Example 6.7. Consider a = ⟨λx.⟨x⟩(x)⟩(y ⊕ •, • ⊕ z) and a′ = ⟨λx.⟨x⟩(x)⟩(• ⊕ z, y ⊕ •). We
have a ¨ a′ and a ∼
= a′ but NF (a) = L(a) = ⟨y⊕•⟩(•⊕z) and NF (a′ ) = L(a′ ) = ⟨•⊕z⟩(y⊕•),
hence NF (a) ̸∼
= NF (a′ ).
(!)

Theorem 6.8 (Step 3). Let e, e′ ∈ ∆⊕ be such that e ¨ e′ . If supp(NF (e))∩supp(NF (e′ )) ̸=
∅ then e = e′ .
Proof. Let e0 ∈ supp(NF (e)) ∩ supp(NF (e′ )). By Lemma 6.2, there are r ◁ e and r′ ◁ e′ such
that e0 = ∥NF (r)∥ = ∥NF (r′ )∥. Since e ¨ e′ , we have r ¨ r′ and, since NF (r) ∼
= NF (r′ ),
′
′
∼
we obtain r = r by Lemma 6.6, hence e = e .
By Lemma 6.5, L preserves coherence; and thanks to Theorem 6.8 we can iterate
Lemma 6.1 to obtain:
(!)

Theorem 6.9 (Step 4). Let e ∈ ∆⊕ with e ¨ e and let e′ ∈ supp(N F (e)). Then
(NF (e))e′ =

m(e)
m(e′ )

.

Proof. Fix n such that NF (e) = Ln (e): since supp(NF (e)) = Ln ({e}), there exists a sequence
e0 , . . . , en such that e0 = e, en = e′ and ei ∈ supp(L(ei−1 )) for 1 ≤ i ≤ n. We prove by
induction on n that, given such a sequence, we have NF (e0 )en = m(e0 )/m(en ).
If n = 0 the result is trivial. Otherwise, Lemma 6.1 gives L(e0 )e1 = m(e0 )/m(e1 ).
Moreover, Lemma 6.5 ensures that supp(L(e0 )) is a clique, and in particular e1 ¨ e1 and the
induction hypothesis entails NF (e1 )en = m(e1 )/m(en ). Finally, since en ∈ supp(NF (e1 )),
Theorem 6.8 entails NF (e′ )en = 0 for each e′ ∈ supp(L(e0 )) \ {e1 }. We obtain
NF (e0 )en = NF (L(e0 ))en = L(e0 )e1 NF (e1 )en =

m(e0 ) m(e1 )
m(e0 )
=
m(e1 ) m(en )
m(en )

.

6.2. Commutation. By assembling all our previous results, we obtain the desired commutation theorem:
Theorem 6.10. Let M ∈ Λ⊕ . Then BT (M )∗ = NF (M ∗ ).
Proof. By Theorem 4.5
M∗ =

∑
s∈T (M )

1
s
m(s)

and by Theorem 4.3 and Theorem 6.8 we are allowed to form
∑
∑
∑
1
NF (M ∗ ) =
NF (s) =
m(s)
s∈T (M )

s∈T (M ) u∈supp(NF (s))

NF (s)u
u
m(s)

the inner sums having pairwise disjoint supports. Then, if u ∈ supp(NF (M ∗ )), there is a
(s)u
1
unique s ∈ T (M ) such that u ∈ supp(NF (s)) and we obtain NF (M ∗ )u = NF
m(s) = m(u) by
Theorem 6.9. We conclude since supp(NF (M ∗ )) = T (BT (M )) by Theorem 4.10.

## PDF page 30

1:30 TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

Vol. 18:1

Acknowledgements
This work owes much to the friendly and stimulating environment provided by the International Research Network on Linear Logic13 between the French CNRS and the Italian
INDAM.

References
+

[ADCP 14] Ali Assaf, Alejandro Díaz-Caro, Simon Perdrix, Christine Tasson, and Benoît Valiron. Call-byvalue, call-by-name and the vectorial behaviour of the algebraic λ-calculus. Logical Methods in
Computer Science, 10(4), 2014. doi:10.2168/LMCS-10(4:8)2014.
[BM20]
Davide Barbarossa and Giulio Manzonetto. Taylor subsumes scott, berry, kahn and plotkin.
Proc. ACM Program. Lang., 4(POPL):1:1–1:23, 2020. doi:10.1145/3371069.
[DE11]
Vincent Danos and Thomas Ehrhard. Probabilistic coherence spaces as a model of higherorder probabilistic computation. Information and Computation, 209(6):966–991, 2011. doi:
10.1016/j.ic.2011.02.001.
Thomas Ehrhard. Finiteness spaces. Mathematical Structures in Computer Science, 15(4), 2005.
[Ehr05]
doi:10.1017/S0960129504004645.
Thomas Ehrhard. A finiteness structure on resource terms. In LICS 2010, 2010. doi:10.1109/
[Ehr10]
LICS.2010.38.
[ER03]
Thomas Ehrhard and Laurent Regnier. The differential lambda-calculus. Theoretical Computer
Science, 309(1-3), 2003. doi:10.1016/S0304-3975(03)00392-X.
[ER06a]
Thomas Ehrhard and Laurent Regnier. Böhm trees, krivine’s machine and the taylor expansion
of lambda-terms. In CiE 2005, 2006. doi:10.1007/11780342\_20.
[ER06b]
Thomas Ehrhard and Laurent Regnier. Differential interaction nets. Theoretical Computer
Science, 364(2), 2006. doi:10.1016/j.tcs.2006.08.003.
[ER08]
Thomas Ehrhard and Laurent Regnier. Uniformity and the Taylor expansion of ordinary λ-terms.
Theoretical Computer Science, 403(2-3), 2008. doi:10.1016/j.tcs.2008.06.001.
[FGHW08] M. Fiore, N. Gambino, M. Hyland, and G. Winskel. The cartesian closed bicategory of generalised
species of structures. Journal of the London Mathematical Society, 2008. doi:10.1112/jlms/
jdm096.
[Gir87]
Jean-Yves Girard. Linear logic. Theoretical Computer Science, 50:1–102, 1987.
[Gir88]
Jean-Yves Girard. Normal functors, power series and lambda-calculus. Annals of Pure and
Applied Logic, 37(2):129, 1988.
[Has02]
Ryu Hasegawa. Two applications of analytic functors. Theoretical Computer Science, 272(12):113–175, 2002. doi:10.1016/S0304-3975(00)00349-2.
J. Laird. Fixed points in quantitative semantics. In Martin Grohe, Eric Koskinen, and Natarajan
[Lai16]
Shankar, editors, Proceedings of the 31st Annual ACM/IEEE Symposium on Logic in Computer
Science, LICS ’16, New York, NY, USA, July 5-8, 2016, pages 347–356. ACM, 2016. doi:
10.1145/2933575.2934569.
François Lamarche. Quantitative domains and infinitary algebras. Theoretical Computer Science,
[Lam92]
94(1):37–62, 1992. doi:10.1016/0304-3975(92)90323-8.
[Lan02]
S. Lang. Algebra. Graduate Texts in Mathematics. Springer New York, 2002.
[Lev16]
Thomas Leventis. Probabilistic lambda-theories. Theses, Aix-Marseille Université, December
2016. URL: https://tel.archives-ouvertes.fr/tel-01427279.
[Lev19]
Thomas Leventis. A deterministic rewrite system for the probabilistic λ-calculus. Mathematical
Structures in Computer Science, 29(10):1479–1512, 2019. doi:10.1017/S0960129519000045.
[LL19]
Ugo Dal Lago and Thomas Leventis. On the taylor expansion of probabilistic λ-terms. In
Herman Geuvers, editor, 4th International Conference on Formal Structures for Computation
and Deduction, FSCD 2019, June 24-30, 2019, Dortmund, Germany, volume 131 of LIPIcs,
pages 13:1–13:16. Schloss Dagstuhl - Leibniz-Zentrum für Informatik, 2019. doi:10.4230/LIPIcs.
FSCD.2019.13.
13http://www.linear-logic.org/

## PDF page 31

Vol. 18:1

TAYLOR EXP. OF λ-TERMS AND THE GROUPOID OF RIGID APPROXIMANTS

1:31

[LMMP13] Jim Laird, Giulio Manzonetto, Guy McCusker, and Michele Pagani. Weighted relational models
of typed lambda-calculi. In 28th Annual ACM/IEEE Symposium on Logic in Computer Science,
LICS 2013, New Orleans, LA, USA, June 25-28, 2013, pages 301–310. IEEE Computer Society,
2013. doi:10.1109/LICS.2013.36.
[Maz12]
Damiano Mazza. An infinitary affine lambda-calculus isomorphic to the full lambda-calculus. In
2012 27th Annual IEEE Symposium on Logic in Computer Science, pages 471–480, 2012.
[MP11]
Giulio Manzonetto and Michele Pagani. Böhm’s theorem for resource lambda calculus through
taylor expansion. In C.-H. Luke Ong, editor, Typed Lambda Calculi and Applications - 10th
International Conference, TLCA 2011, Novi Sad, Serbia, June 1-3, 2011. Proceedings, volume
6690 of Lecture Notes in Computer Science, pages 153–168. Springer, 2011. doi:10.1007/
978-3-642-21691-6\_14.
[MPV18]
Damiano Mazza, Luc Pellissier, and Pierre Vial. Polyadic approximations, fibrations and
intersection types. 2018. doi:10.1145/3158094.
[OA18]
Federico Olimpieri and Lionel Vaux Auclair. On the taylor expansion of λ-terms and the groupoid
structure of their rigid approximants. 2018 Joint Workshop on Linearity & Trends in Linear
Logic and Applications, 2018.
[Oli20]
Federico Olimpieri. Intersection type distributors. CoRR, abs/2002.01287, 2020. URL: https:
//arxiv.org/abs/2002.01287, arXiv:2002.01287.
[Ong17]
C.-H. Luke Ong. Quantitative semantics of the lambda calculus: Some generalisations of the
relational model. In 32nd Annual ACM/IEEE Symposium on Logic in Computer Science,
LICS 2017, Reykjavik, Iceland, June 20-23, 2017, pages 1–12. IEEE Computer Society, 2017.
doi:10.1109/LICS.2017.8005064.
[PTV16a] Michele Pagani, Christine Tasson, and Lionel Vaux. Strong normalizability as a finiteness
structure via the taylor expansion of λ-terms. In Bart Jacobs and Christof Löding, editors,
Foundations of Software Science and Computation Structures - 19th International Conference,
FOSSACS 2016, Held as Part of the European Joint Conferences on Theory and Practice of
Software, ETAPS 2016, Eindhoven, The Netherlands, April 2-8, 2016, Proceedings, volume
9634 of Lecture Notes in Computer Science, pages 408–423. Springer, 2016. doi:10.1007/
978-3-662-49630-5\_24.
[PTV16b] Michele Pagani, Christine Tasson, and Lionel Vaux. Strong normalizability as a finiteness structure via the taylor expansion of λ-terms. In FoSSaCS 2016, 2016. doi:10.1007/
978-3-662-49630-5\_24.
[Suz82]
Michio Suzuki. Group theory I. Springer-Verlag Berlin ; New York, 1982.
Takeshi Tsukada, Kazuyuki Asada, and C.-H. Luke Ong. Generalised species of rigid resource
[TAO17]
terms. In LICS 2017, 2017. doi:10.1109/LICS.2017.8005093.
[TAO18]
Takeshi Tsukada, Kazuyuki Asada, and C.-H. Luke Ong. Species, profunctors and taylor
expansion weighted by smcc: A unified framework for modelling nondeterministic, probabilistic
and quantum programs. In Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in
Computer Science, LICS ’18, pages 889–898, New York, NY, USA, 2018. ACM. doi:10.1145/
3209108.3209157.
[Vau09]
Lionel Vaux. The algebraic lambda calculus. Mathematical Structures in Computer Science,
19(5):1029–1059, 2009. doi:10.1017/S0960129509990089.
[Vau17]
Lionel Vaux. Taylor expansion, β-reduction and normalization. In CSL 2017, 2017. doi:10.
4230/LIPIcs.CSL.2017.39.

This work is licensed under the Creative Commons Attribution License. To view a copy of this
license, visit https://creativecommons.org/licenses/by/4.0/ or send a letter to Creative
Commons, 171 Second St, Suite 300, San Francisco, CA 94105, USA, or Eisenacher Strasse
2, 10777 Berlin, Germany
