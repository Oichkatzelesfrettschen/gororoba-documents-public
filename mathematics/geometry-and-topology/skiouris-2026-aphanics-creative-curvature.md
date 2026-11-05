Source: https://zenodo.org/records/22032281
PDF sha256: 3a21bfd18bbd608a14c09230595a15e4f87e4aa55a7bfcc636d7b769aeb8c549
License: CC-BY-4.0

# Transcription of skiouris-2026-aphanics-creative-curvature.pdf

Transcription of `skiouris-2026-aphanics-creative-curvature.pdf` in this directory, 41 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 3-41 from the PDF's own text layer (pdftotext version 26.10.0, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Aphanics and Creative Curvature:
A Geometric Theory of Hidden Generation
in Dialectical Cognitive Systems
Kyriakos John Skiouris
Agingo Corporation, Charlotte NC
research@agingo.com
August 2026

– v6 (pure-math core, §3–§4, rewritten)
Abstract

Cognitive and generative systems routinely face the problem of distinguishing
genuine creativity from random displacement in state space. Without a formal
distinction, controllers cannot tell whether a system is refining, hallucinating, pivoting, or genuinely creating. We introduce a geometric framework, which we term
aphanics, for systems possessing hidden generators: nonzero elements annihilated by
the system’s own internal action operator, a(p) ∈ ker(Lp ) \ {0}.
Our main results are geometric and exact. In the sedenion algebra the locus
of such observers is a smooth manifold, an R+ -cone over the homogeneous space
G2 /SU(2), over which the kernel assignment defines a rank-4 vector bundle with a
canonical metric connection. The Berry curvature of this connection admits a closed
+
polynomial form Ca,b (p) = πp (Lb G+
p La − La Gp Lb ) πp , bypassing eigenprojector
contour integrals (Theorem 3.9), and its holonomy algebra is exactly u(2) = u(1) ⊕
su(2) (Theorem 4.13, Proposition 4.15), with the central complex structure realized
by right multiplication by the Cayley–Dickson doubling generator. All basepoint
computations decompose with integer coefficients onto 't Hooft self-dual tensors, and
are certified in exact arithmetic: both the Q-centralizer dimension and the basepoint
curvature-span decomposition are exact, the latter with identically zero residual and
exact integer coefficients.
Building on this geometry we propose an operational layer for monitoring dialectical inference systems: a creative-curvature scalar κγ , a phase-transition score Φk ,
a survival-gated verified creativity score Cksurv , a seven-regime diagnostic taxonomy,
and a U(1) holonomy phase θ(Γ) over closed dialectical arcs that certifies net structural turning. The geometric results (§3–§4) are theorems; the monitoring layer (§5
onward) is a framework proposal whose empirical validation in any deployed system
is future work.

Keywords: aphanics, creative curvature, dialectical inference, Berry curvature, holonomy, geometric phase, hidden-sector dynamics, Cayley–Dickson algebras, cognitive
systems.
1

## PDF page 2

<math display="block">\mathbf{MSC:}\ 53C29,\ 17A35,\ 17A20,\ 68T01,\ 68T42</math>
<math display="inline">\mathbf{arXiv:}\ \mathrm{math.DG}\ (\mathrm{primary}),\ \mathrm{math.RA},\ \mathrm{cs.AI}</math>
2

## PDF page 3

Contents
1 Introduction

5

1.1 The Problem: Creativity Is Not Displacement . . . . . . . . . . . . . . .

5

1.2

Contributions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

5

1.3

Scope and Deliberate Omissions . . . . . . . . . . . . . . . . . . . . . . .

6

1.4

Fixed definitions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

7

1.5

Roadmap . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

7

2 Related Work

7

2.1

Information Geometry and Natural Gradient . . . . . . . . . . . . . . .

7

2.2

Geometric Deep Learning . . . . . . . . . . . . . . . . . . . . . . . . . .

8

2.3

Creativity Metrics . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

8

2.4 Topological Methods in Machine Learning . . . . . . . . . . . . . . . . .

8

2.5

Dialectical and Self-Corrective Architectures . . . . . . . . . . . . . . . .

8

2.6

Geometric Phases and Holonomy . . . . . . . . . . . . . . . . . . . . . .

9

3 The Aphanic Berry Bundle

9

3.1 The Aphanic Locus as a Smooth Manifold . . . . . . . . . . . . . . . . .

10

3.2 The Kernel Bundle . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

11

3.3 The Kernel-Projector Connection . . . . . . . . . . . . . . . . . . . . . .

11

3.4 The Berry Curvature 2-Form . . . . . . . . . . . . . . . . . . . . . . . .

12

3.5 The Closed-Form Bridge . . . . . . . . . . . . . . . . . . . . . . . . . . .

12

3.6

15

Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

4 The Algebraic Structure of Aphanic Curvature

15

4.1

Notation and the Aphanic Spectrum . . . . . . . . . . . . . . . . . . . .

16

4.2

Closed-Form Pseudoinverse and Projector . . . . . . . . . . . . . . . . .

16

4.3 The Aphanic Curvature Operator . . . . . . . . . . . . . . . . . . . . . .

17

4.4

G2 -Equivariance . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

17

4.5

Q-Centralizer Vanishing . . . . . . . . . . . . . . . . . . . . . . . . . . .

18

4.6

Proof of the Rank Theorem . . . . . . . . . . . . . . . . . . . . . . . . .

21

4.7

From Curvature Span to Holonomy . . . . . . . . . . . . . . . . . . . . .

23

4.8 The Eigenspace Mixing Trichotomy . . . . . . . . . . . . . . . . . . . . .

24

4.9

26

Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

5 Discrete Formulas

27

5.1 Turn-Angle Form . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

27

5.2

G-Metric Form . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

27

5.3

Exogenous Subtraction . . . . . . . . . . . . . . . . . . . . . . . . . . . .

28

5.4

Phase Transition Score . . . . . . . . . . . . . . . . . . . . . . . . . . . .

28

6 The State Vector

29
3

## PDF page 4

7 Verified Creativity

29

8 The Seven-Regime Taxonomy

30

9 A Holonomy Phase for Closed Arcs

31

10 Discussion

32

10.1 Relationship to Information Geometry . . . . . . . . . . . . . . . . . . .

32

10.2 The Null-Space Inversion

. . . . . . . . . . . . . . . . . . . . . . . . . .

33

10.3 Limitations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

34

11 Conclusion

34

A Expanded Proofs

36

A.1 Proof of Proposition 5.3 (Graceful Degradation) . . . . . . . . . . . . . .

36

A.2 Proof of Proposition 9.2 (Classification of Dialectical Arcs) . . . . . . .

36

B Conceptual Monitor: Pseudocode

36

C The Basepoint Table

37

C.1 Canonical kernel basis . . . . . . . . . . . . . . . . . . . . . . . . . . . .

37

C.2 The four generators in the kernel basis . . . . . . . . . . . . . . . . . . .

37

C.3 Decomposition of the nonzero curvature pairs . . . . . . . . . . . . . . .

38

C.4 Spectrum cross-check . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

39

4

## PDF page 5

1

Introduction

1.1

The Problem: Creativity Is Not Displacement

Cognitive and generative systems produce novel outputs, but novelty alone does not
distinguish genuine creativity from hallucination or random drift. Existing metrics (perplexity, compression gain, distributional divergence) measure displacement in observation
space, not structural transformation in the system’s internal geometry. A system can
move far in state space without turning. It can turn without moving. It can move and
turn while violating every constraint it was built to respect. None of these is creativity.
Creativity is turning in a way that deforms the constraint manifold itself while remaining
on it throughout.
The analogy is precise: in the Ryōan-ji rock garden in Kyoto, fifteen stones are
arranged so that from any standing position exactly fourteen are visible; the fifteenth is
hidden by the geometry of the arrangement, not by accident or deficiency. Remove it
and the composition collapses.
This paper formalizes the hidden stone. In any system with an internal action
operator Lp , there may exist generators a such that Lp · a = 0 while a ̸= 0: elements that
are annihilated by the system’s own action yet remain structurally present. We call these
aphanes generators, from the Greek aphanés (αϕανϵ́ς): the non-apparent. The study of
their dynamics, geometry, and operational consequences constitutes the framework we
present here.
The central interpretive move is a sign-flip: the kernel of Lp is conventionally treated
as a degeneracy, a locus where the operator fails. We reinterpret it as the locus of maximal
structural richness. The hidden generator is not what the system cannot do; it is what
prevents the system from collapsing into mechanical repetition. This reinterpretation has
concrete mathematical content: the hidden sector carries bundle structure, curvature,
and holonomy that provide a geometric diagnostic for structural turning.

1.2

Contributions

This paper makes six contributions, in two tiers. Contributions 1–2 are theorems, proved
in the sedenion model (Sections 3–4). Contributions 3–6 are a framework proposal:
an instrumentation layer for dialectical systems whose validity in any deployed system
requires that system to expose a hidden-sector bundle with the stated structure, and
whose empirical validation is future work.
1. The aphanic Berry bundle (Section 3; theorem): the kernel assignment p 7→
ker Lp over the aphanic locus, realized as a smooth rank-4 vector bundle with a
kernel-projector connection, whose Berry curvature is identified in closed form with
the algebraic curvature operator Ca,b (p).
2. The algebraic structure of aphanic curvature (Section 4; theorem): a closed5

## PDF page 6

form pseudoinverse and projector, G2 -equivariance, the Q-centralizer vanishing
theorem, and the rank theorem computing the curvature span, capped (Proposition 4.15) to the holonomy algebra u(2) = u(1) ⊕ su(2), and sharpened by an
eigenspace-mixing trichotomy that counts the rank.
3. Creative curvature and discrete operational formulas (Section 5): the
creative-curvature scalar κγ , its discrete turn-angle and G-metric forms, exogenous
subtraction procedures, and the phase transition score Φk .
4. The survival-gated creativity score Cksurv (Section 7): a triple product of
curvature, verification weight, and survival horizon that separates five distinct
failure modes.
5. A seven-regime operational taxonomy (Section 8): a classifier with hysteresis
that maps continuous curvature-verification trajectories to discrete operational
states.
6. The holonomy phase θ(Γ) (Section 9; proposal): a U(1) geometric holonomy
phase over closed dialectical arcs that certifies net structural turning and distinguishes turning loops from drift. It is geometric, not topological: the aphanic base
is simply connected, so θ(Γ) is curvature-driven and deformation-sensitive, not a
homotopy invariant.

1.3

Scope and Deliberate Omissions

This paper operates at the abstract geometric level. We define the aphanes generator via
the kernel of a left-multiplication operator Lp , derive curvature and a holonomy phase
from connection geometry on the resulting bundle, and establish operational formulas
for monitoring dialectical systems. The framework is motivated at this abstract level; its
v6 core (Sections 3–4) instantiates the construction concretely in the sedenion algebra S,
while the companion algebra carries the same construction up the Cayley–Dickson tower.
The downstream operational formulas (Sections 5–9) depend only on the existence and
connection geometry of the hidden sector, and may be read without committing to a
unique implementation algebra or inference architecture. This separation is deliberate.
The mathematical foundations of aphanics (the characterization of ker(Lp ), its dimension, spectral structure, and the topology of the associated bundle) are developed in
a companion paper, Algebraic Hiddenness in the Sedenion Algebra [21]. The four foundational statements the geometric core actually uses (the Two-Condition characterization
of ker(Lp ), its dimension dim Kp = 4, the 4–8–4 spectrum of Gp , and the identification
of the unit aphanic locus with G2 /SU(2)) are stated where they are used in Sections 3–4
and cited to that companion, which is published and publicly available [21]. The present
paper is not self-contained on its foundations; every foundational statement it uses is
stated, proved, and independently auditable there. Section 4.1 provides a brief sketch of
the motivating algebraic setting.
6

## PDF page 7

1.4

Fixed definitions

Although the foundations are the companion’s, the three terms this paper uses inside
formal statements are fixed here, before first such use, in the companion’s own formulation
[21].
Definition 1.1 (Aphanic element). Let p = (x, y) ∈ S under the Cayley–Dickson
identification S = O ⊕ O. Then p is aphanic if x, y ∈ Im(O) and ∥x∥ = ∥y∥ ̸= 0,
⟨x, y⟩ = 0, where ⟨·, ·⟩ and ∥ · ∥ are the standard Euclidean inner product and norm on
O∼
= R8 .
Definition 1.2 (Aphanic locus). The aphanic locus is the set of all aphanic elements
of S; its unit normalization is the homogeneous space G2 /SU(2) used throughout this
paper.
Definition 1.3 (Aphanic twist). The aphanic twist of the kernel bundle over the unit
aphanic locus is its secondary characteristic class in H 6 (G2 /SU(2); Z/2) ∼
= Z/2.
Remark 1.4. Definition 1.3 names an invariant, not a phenomenon: the twist exists as
a class whatever its value, its nonvanishing is a theorem of the companion, and the
definition deliberately does not identify the class with a holonomy character. The class
classifies the bundle and is detected by five- and six-dimensional cycles; the holonomy
phase θ(Γ) of this paper is a connection-dependent quantity on arcs, and the two are
never interchanged.

1.5

Roadmap

Section 2 surveys related work across information geometry, geometric deep learning,
creativity metrics, and topological methods. Section 3 constructs the aphanic Berry
bundle and identifies its Berry curvature with a closed-form algebraic operator. Section 4
establishes the algebraic structure of that curvature and proves the u(2) rank theorem.
Section 5 provides discrete formulas for the creative-curvature scalar. Section 6 specifies
the state vector. Section 7 defines verified creativity. Section 8 presents the regime
taxonomy. Section 9 establishes the holonomy phase. Section 10 discusses implications,
limitations, and connections. Section 11 concludes, and Appendix C tabulates the explicit
basepoint data underlying the rank theorem.

2

Related Work

2.1

Information Geometry and Natural Gradient

The idea that learning and inference have intrinsic geometric structure traces to Amari’s
information geometry [2], where the Fisher information matrix endows parameter space
with a Riemannian metric and the natural gradient [1] replaces Euclidean descent with
7

## PDF page 8

geodesic motion on the statistical manifold. Martens [15] extended this to practical
deep learning via K-FAC approximations. These methods measure curvature of the loss
landscape: how predictions change as parameters vary. Aphanics measures something
different: curvature of the hidden sector: how the structurally invisible generators rotate
as the system moves. The Fisher metric sees everything; the aphanes metric sees only
what is hidden.

2.2

Geometric Deep Learning

Bronstein et al. [6] unified CNNs, GNNs, and Transformers under the umbrella of
geometric deep learning: architectures that respect the symmetry group of their input
domain. Equivariant networks [8, 23] preserve group structure through layers. This
work focuses on visible symmetry: the group actions that transform inputs and outputs.
Aphanics addresses the complementary question: what structure is present but invisible
to the system’s own measurement operator? The hidden sector is not a latent space in
the variational autoencoder sense [14]; it is a kernel of an algebraic action, not a learned
compression.

2.3

Creativity Metrics

Boden [5] distinguished combinational, exploratory, and transformational creativity,
arguing that the third requires restructuring the conceptual space itself. Schmidhuber
[18] formalized creativity as compression progress: a system is creative when it finds
shorter descriptions of its experience. Wiggins [24] gave a formal framework for creative
systems based on search in conceptual spaces. These approaches measure what is
produced. Aphanics measures how the system turns while producing it: the geometry of
the trajectory, not the novelty of the output. Creative curvature κγ captures Boden’s
transformational creativity geometrically: the constraint manifold deforms under the
trajectory.

2.4

Topological Methods in Machine Learning

Persistent homology [7, 10] and topological data analysis extract shape invariants from
data. Rieck et al. [17] applied persistence to neural network loss surfaces. Naitzat et al.
[16] tracked topological changes through layers. These methods study the topology of
data or loss landscapes. The holonomy phase θ(Γ) in this paper is a geometric invariant
of a trajectory, a closed loop in the space of system states, not of the data itself. It
measures irreversible structural passage, not homological features of a point cloud.

2.5

Dialectical and Self-Corrective Architectures

Thesis-antithesis-synthesis as a computational paradigm has antecedents in argumentation
frameworks [9], debate-based AI alignment [12], and self-play systems [19]. Constitutional
8

## PDF page 9

AI [3] uses self-critique to improve outputs. Friston’s free-energy principle [11] provides
a complementary perspective: systems minimize surprise by maintaining generative
models, and the boundary between model and environment is itself a structural object.
The present formalism is motivated by dialectical self-correction architectures in which
each inference step generates a thesis and antithesis before synthesizing. The aphanics
framework provides the geometric infrastructure for monitoring such systems: κγ tracks
whether the dialectical process is genuinely turning or merely oscillating, and θ(Γ)
determines whether a completed arc has produced irreversible structural change.

2.6

Geometric Phases and Holonomy

The holonomy phase θ(Γ) defined in Section 9 is a geometric phase in the sense of
Berry [4]: the holonomy of a connection on a parameter-dependent eigenspace bundle
around a closed loop. Simon [20] identified Berry’s phase as the holonomy of a natural
connection on a line bundle over parameter space, and Wilczek and Zee [25] generalized
it to non-abelian gauge structure when the eigenspace is degenerate. In the algebraic
setting motivating this work, the rank-4 kernel bundle admits a canonical connection
whose holonomy algebra is exactly u(2) (Theorem 4.13, Proposition 4.15); the holonomy
phase θ(Γ) used here is its abelian U(1) component, while the SU(2) component is the
Wilczek–Zee generalization and is not used in this paper. Separately, the bundle carries a
genuine topological invariant, a nonzero Z/2 characteristic class (the “aphanic twist”) in
H 6 (G2 /SU(2); Z/2), which classifies the bundle itself and is unrelated to the loop phase
(the base is simply connected). The U(1) generator admits an explicit ambient-operator
description: it is the restriction to the kernel of right multiplication by the doubling
generator of the algebra. This identification is tower-universal across Cayley–Dickson
levels n = 2k ≥ 16 [21], so the underlying algebraic identity is not a feature of the
sedenion level alone but an inheritance from the Cayley–Dickson doubling structure itself.
We claim no holonomy statement above n = 16: the bundle, connection and curvature
used here are constructed only at the sedenion level. The framework presented here
applies geometric phase theory to cognitive systems rather than quantum mechanics: the
“parameter” is the system state, the “eigenspace” is the hidden sector ker(Lp ), and the
holonomy classifies irreversible structural transformation rather than adiabatic evolution.

3

The Aphanic Berry Bundle

This section constructs the geometric object whose holonomy algebra is computed in
§4. The aphanic locus Paph ⊂ S is a smooth real-analytic manifold; the assignment
p 7→ Kp = ker Lp defines a smooth real rank-4 vector bundle K → Paph ; and the kernelprojector prescription ∇ := π ◦d◦π defines a metric connection on K. The principal result
of the section (Theorem 3.9) identifies the resulting Berry curvature 2-form, restricted to
fibers, with the closed-form curvature operator Ca,b (p) used throughout §4.
9

## PDF page 10

Kp = ker Lp
rank 4

∇=π◦d
holonomy ∈ u(2)
F ∇ Kp = Ca,b (p)

γ
p

1
∼
Paph
= G2 /SU(2)

1
∼
Figure 1: The aphanic Berry bundle. Over each point p of the unit aphanic locus Paph
=
G2 /SU(2) sits the rank-4 kernel fiber Kp = ker Lp . The kernel-projector connection
∇ = π ◦ d (Definition 3.5) has holonomy u(2), and its curvature 2-form restricted to the
fibers coincides with the closed-form operator Ca,b (p) (Theorem 3.9).

The proof of the bridge theorem is a single application of eigenprojector perturbation
theory [13], made transparent by the closed-form representation of πp in R[Gp ] (Proposition 4.2, restated below) and three algebraic identities that follow from the universal
4–8–4 spectrum.

3.1

The Aphanic Locus as a Smooth Manifold

We retain the notation of §4: S = O ⊕ O ℓ with the canonical CD product, embeddings
ι1 , ι2 : O → S, and the Two-Condition Theorem characterizing the aphanic locus.
Proposition 3.1 (Aphanic locus is a real-analytic manifold). The aphanic locus Paph ⊂ S,
identified with {(x, y) ∈ Im(O)⊕2 : ∥x∥ = ∥y∥ > 0, ⟨x, y⟩ = 0} via p = ι1 (x) + ι2 (y), is
1
a real-analytic submanifold of S of dimension 12. The unit slice Paph
:= {p ∈ Paph :

∥p∥2 = 2} is an 11-dimensional smooth submanifold, a single G2 -orbit diffeomorphic to
1 .
G2 /SU(2) [21], and Paph is the R+ -cone over Paph

Proof. The two real-analytic constraints f1 (x, y) := ∥x∥2 − ∥y∥2 and f2 (x, y) := ⟨x, y⟩
on Im(O)⊕2 ∼
= R14 have differentials df1 = 2(x dx − y dy) and df2 = y dx + x dy. At any
(x, y) with x, y both nonzero and orthogonal, the gradients are linearly independent: the
gradient of f1 involves the components (x, −y) in the (dx, dy) basis, while the gradient of
f2 involves (y, x). Linear dependence would force x ∥ y as vectors in Im(O), contradicting
⟨x, y⟩ = 0 with ∥x∥ = ∥y∥ > 0. The regular-value theorem applies, giving codimension 2
and dimension 14 − 2 = 12. The unit slice is cut out by the additional smooth constraint
∥x∥2 + ∥y∥2 = 2, which is independent of the previous two for the same reason; this
is dimension 11, and matches the homogeneous-space description G2 /SU(2) from the
companion [21].
2
Remark 3.2. The closed-form expressions for πp and G+
p depend only on Gp and ∥p∥ ,

so the bridge identity proven in Theorem 3.9 is homogeneous of weight −2 under radial
10

## PDF page 11

scaling. Working on Paph rather than its unit slice is therefore harmless and convenient.

3.2

The Kernel Bundle

For each p ∈ Paph , the fiber Kp := ker Lp is a 4-dimensional real subspace of S [21]. The
total space
K :=



(p, v) ∈ Paph × S : v ∈ Kp

(1)

projects onto Paph by (p, v) 7→ p.
Proposition 3.3 (Kernel bundle smoothness). The projection K → Paph is a smooth
real rank-4 vector bundle, and the family of orthogonal projectors p 7→ πp is real-analytic
on Paph .
Proof. The closed-form representation of πp from Proposition 4.2 of §4.2,
πp = I −

3
1
Gp +
G2 ,
2
2∥p∥
2∥p∥4 p

(2)

2
is a polynomial in Gp = L⊤
p Lp with coefficients that are real-analytic in ∥p∥ on Paph

(where ∥p∥2 > 0). Since p 7→ Lp is linear in p, the matrix entries of Gp are quadratic
polynomials in the components of p, and (2) is real-analytic on Paph .
Smoothness of πp as a projector field upgrades the kernel assignment p 7→ Kp to a
smooth subbundle: locally on a neighborhood U of any p∗ ∈ Paph , choose four vectors
v1 , . . . , v4 ∈ Kp∗ and set wk (p) := πp vk for p ∈ U . By continuity, {wk (p)}4k=1 remains
linearly independent on a sufficiently small neighborhood, providing a smooth local frame
for K|U .
Remark 3.4 (Closed form vs. contour-integral construction). The standard route to
bundle smoothness in the eigenprojector literature constructs πp via a Riesz contour
integral of the resolvent (zI − Gp )−1 on a contour separating ker Gp from the rest of
the spectrum [13]. The polynomial representation (2) bypasses the contour entirely;
smoothness is read off algebraically. This is the same advantage exploited throughout §4:
every assertion that would ordinarily require eigendecomposition is instead a polynomial
identity in Gp .

3.3

The Kernel-Projector Connection

The bundle K inherits a fiber inner product from S: for u, v ∈ Kp , ⟨u, v⟩K := ⟨u, v⟩S .
Definition 3.5 (Kernel-projector connection). The kernel-projector connection on K is
∇ := π ◦ d,

(∇X s)(p) := πp X[s] (p),


(3)

for X ∈ Tp Paph and s : Paph → S a section of K (regarded as an S-valued function
satisfying πp s(p) = s(p)).
11

## PDF page 12

Lemma 3.6 (Metric compatibility). For sections s, t of K and tangent vector X,
X⟨s, t⟩K = ⟨∇X s, t⟩K + ⟨s, ∇X t⟩K .
Proof. Since s = πp s and t = πp t, and πp⊤ = πp ,
⟨∇X s, t⟩ + ⟨s, ∇X t⟩ = ⟨πp X[s], t⟩ + ⟨s, πp X[t]⟩ = ⟨X[s], t⟩ + ⟨s, X[t]⟩ = X⟨s, t⟩.
The connection ∇ is the standard kernel-projector (Berry) connection of a smoothly
varying subspace of a fixed inner-product space [4, 13].

3.4

The Berry Curvature 2-Form

The curvature of ∇ is the End(K)-valued 2-form F ∇ := ∇ ◦ ∇ ∈ Ω2 (Paph ; End(K)).
Lemma 3.7 (Closed-form expression for F ∇ ). Let ∂a , ∂b ∈ Tp Paph . Then
∇
Fa,b
(p) Kp = πp ∂a πp , ∂b πp πp ,



(4)



where [·, ·] is the operator commutator on End(S).
Proof. Acting on a section s of K, ∇a s = πp ∂a s. Thus
∇a ∇b s = πp ∂a (πp ∂b s) = πp (∂a πp ) (∂b s) + πp πp ∂a ∂b s.
The torsion-free curvature is the antisymmetrization in (a, b):
∇
Fa,b
s = ∇a ∇b s − ∇b ∇a s = πp (∂a πp )(∂b s) − (∂b πp )(∂a s) ,





the second-derivative terms cancelling by Schwarz. Now s = πp s, so ∂b s = (∂b πp ) s +
πp ∂b s. Substituting and using the identity πp (∂a πp ) πp = 0 (Remark 3.8, below), the
second piece vanishes and
∇
Fa,b
s = πp (∂a πp )(∂b πp ) − (∂b πp )(∂a πp ) s,





which is (4).
Remark 3.8 (Identity πp (∂πp )πp = 0). Differentiating πp2 = πp along any tangent direction a gives (∂a πp ) πp + πp (∂a πp ) = ∂a πp . Sandwiching with πp on both sides yields
2 πp (∂a πp ) πp = πp (∂a πp ) πp , hence πp (∂a πp ) πp = 0. Equivalently, ∂a πp is purely offdiagonal with respect to the decomposition S = Kp ⊕ Kp⊥ .

3.5

The Closed-Form Bridge

We now state and prove the principal theorem of §3: the Berry curvature, restricted to
fibers of K, equals the closed-form operator Ca,b (p) used throughout §4.

12

## PDF page 13

Theorem 3.9 (Closed-form bridge). For every p ∈ Paph and every pair of tangent
directions a, b ∈ Tp Paph ⊂ Im(S) (the extension of the right-hand side to all of Im(S) is
harmless by Corollary 4.11 of §4, which shows it vanishes on the normal directions),
∇
+
Fa,b
(p) Kp = Ca,b (p) = πp Lb G+
p La − La Gp Lb πp .



(5)

Proof. By Lemma 3.7,
∇
Fa,b
(p) Kp = πp (∂a πp )(∂b πp ) πp − πp (∂b πp )(∂a πp ) πp .

We compute πp (∂a πp )(∂b πp ) πp explicitly, then antisymmetrize in (a, b).
Step 1 — Eigenprojector perturbation. The standard formula for the derivative of
an isolated spectral projector [13, Ch. II §1.4], applied to the projector πp onto the zero
eigenspace of Gp , reads
+
∂a πp = − πp (∂a Gp ) G+
p − Gp (∂a Gp ) πp .

(6)

Derivation: differentiating Gp πp = 0 gives (∂a Gp ) πp + Gp (∂a πp ) = 0, hence Gp (∂a πp ) =
+
−(∂a Gp ) πp . Multiplying on the left by G+
p and using Gp Gp = I − πp projects out the

off-diagonal block (I −πp ) (∂a πp ) πp = −G+
p (∂a Gp ) πp . The transposed identity πp Gp = 0
gives the other off-diagonal block πp (∂a πp ) (I − πp ) = −πp (∂a Gp ) G+
p . Summing, and
using πp (∂a πp ) πp = 0 (Remark 3.8), gives (6).
The directional derivative of Gp = L⊤
p Lp is
⊤
∂a Gp = L⊤
a Lp + Lp La = − La Lp + Lp La



= − {La , Lp },

(7)

⊤
where the second equality uses L⊤
p = −Lp , La = −La for imaginary a, p.

Step 2 — Sandwich identities. The two terms in (6) are killed asymmetrically by
+
left- and right-multiplication by πp . From πp G+
p = Gp πp = 0 (Proposition 4.2),

πp (∂a πp ) = − πp (∂a Gp ) G+
p,

(∂b πp ) πp = − G+
p (∂b Gp ) πp .

(8)

Sandwiching the product gives
πp (∂a πp )(∂b πp ) πp = πp (∂a πp )



(∂b πp ) πp



2
= πp (∂a Gp ) (G+
p ) (∂b Gp ) πp

(9)

(the two minus signs from (8) cancel).
Step 3 — Four cross-terms; three vanish. Substituting ∂a Gp = −{La , Lp } from (7)
into (9) and expanding the product of two anticommutators gives four terms (the two

13

## PDF page 14

minus signs again cancelling):
2
πp {La , Lp } (G+
p ) {Lb , Lp } πp = πp T1 + T2 + T3 + T4 πp ,



(10)



where
2
T1 = La Lp (G+
p ) Lb Lp ,

2
T2 = La Lp (G+
p ) Lp Lb ,

2
T3 = Lp La (G+
p ) Lb Lp ,

2
T4 = Lp La (G+
p ) Lp Lb .

The boundary identity
Lp πp = πp Lp = 0

(11)

⊤ ⊤ =
holds because πp projects onto ker Lp (giving Lp πp = 0) and πp Lp = (L⊤
p πp )

(−Lp πp )⊤ = 0 for imaginary p. By inspection of the four terms in (10):
• πp T1 πp = 0: rightmost factor Lp πp vanishes.
• πp T3 πp = 0: leftmost factor πp Lp vanishes.
• πp T4 πp = 0: both outer factors vanish (either suffices).
2
• πp T2 πp : the two interior Lp factors flank (G+
p) .

Only T2 survives.
2
Step 4 — Polynomial collapse of T2 . Since (G+
p ) ∈ R[Gp ] by Proposition 4.2 and

Lp commutes with Gp (because Gp = −L2p for imaginary p, and Lp commutes with L2p ),
2
Lp commutes with (G+
p ) . Hence
2
+ 2 2
+ 2
Lp (G+
p ) Lp = (Gp ) Lp = −(Gp ) Gp .
+
The pseudoinverse identity G+
p Gp = I − πp , combined with Gp πp = 0, yields
2
+
+
+
+
(G+
p ) Gp = Gp (Gp Gp ) = Gp (I − πp ) = Gp ,

(12)

the polynomial identity advertised at the start of the proof. Substituting,
2
+
Lp (G+
p ) Lp = −Gp ,

hence

2
+
T2 = La Lp (G+
p ) Lp Lb = − La Gp Lb .



Sandwiching with πp ,
πp (∂a πp )(∂b πp ) πp = πp T2 πp = − πp La G+
p Lb πp .

14

(13)

## PDF page 15

Step 5 — Antisymmetrize. From (13),
∇
Fa,b
(p) Kp = πp (∂a πp )(∂b πp ) πp − πp (∂b πp )(∂a πp ) πp
+
= − πp La G+
p Lb πp + πp Lb Gp La πp
+
= πp Lb G+
p La − La Gp Lb πp = Ca,b (p),



which is (5).
Remark 3.10 (Numerical verification). Theorem 3.9 has been verified numerically by
central finite-difference perturbation of πp at 50 random aphanic samples, comparing
FD
Fa,b
(p) := πp δa π, δb π πp ,





1
δa π := 2ϵ
πp+ϵa − πp−ϵa ,



to the closed-form Ca,b (p). The discrepancy ∥F FD − C∥F scales as ϵ2 over four decades
ϵ ∈ [10−6 , 10−3 ], with floor at ϵ ≈ 10−5 where the residual is 1.1 × 10−10 , dominated by
eigensolver roundoff. The opposite-sign hypothesis ∥F FD +C∥F remains O(∥C∥F ) at every
ϵ, distinguishing the sign by nine orders of magnitude. The verification is reproducible
from the probe op_F2_berry_kernel_match.cpp in the supplementary archive.

3.6

Summary

The aphanic locus Paph is a smooth real-analytic manifold (Proposition 3.1). The kernel
assignment p 7→ Kp defines a smooth real rank-4 vector bundle K → Paph whose fiber
projector πp is real-analytic in p (Proposition 3.3); the latter follows from the closed-form
polynomial expression of πp in Gp rather than from any abstract eigenprojector argument.
The kernel-projector connection ∇ = π ◦ d is the natural metric connection (Lemma 3.6);
its curvature 2-form F ∇ , restricted to fibers, has the closed-form expression
∇
+
Fa,b
(p) Kp = πp Lb G+
p La − La Gp Lb πp = Ca,b (p),



the principal output of the section (Theorem 3.9). This identity is the geometric
foundation of §4: the linear span F(p) = spanR {Ca,b (p)}, computed there as a purely
algebraic object, is the pointwise curvature span of the aphanic Berry bundle. The rank
theorem of §4.6 shows this span is u(2); the holonomy-cap proposition (Proposition 4.15)
then upgrades the pointwise span to the full holonomy algebra of the kernel-projector
connection, u(2) at every point of Paph .

4

The Algebraic Structure of Aphanic Curvature

This section establishes the closed-form rank of the aphanic Berry curvature. We work
entirely within the sedenion algebra S obtained from the octonions O by canonical
recursive Cayley–Dickson doubling. The main theorem (Theorem 4.13, hereafter the

15

## PDF page 16

rank theorem) states that the curvature operator at any aphanic observer has rank four.
The proof proceeds by establishing two structural lemmas — a G2 -equivariance identity
(Lemma 4.6) and a centralizer-vanishing identity (Theorem 4.10) — and then anchoring
the count at the basepoint p0 = e1 + e10 via an explicit identification with the 't Hooft
self-dual tensor.
The technical core of the section is the closed-form Lagrange representation of the
projector and pseudoinverse (Proposition 4.2), which makes every subsequent commutator
argument purely polynomial. From that point forward the section is essentially algebra:
there are no eigendecompositions to invoke, no orbit calculus to navigate, no intermediate
spectral surgery.

4.1

Notation and the Aphanic Spectrum

We write S = O ⊕ O ℓ for the sedenion algebra, with ℓ the doubling unit and the canonical
CD product

(a, b)(c, d) = (ac − d¯b, d a + b c̄),

a, b, c, d ∈ O.

(14)

We use the embeddings ι1 , ι2 : O → S defined by ι1 (z) = (z, 0) and ι2 (z) = (0, z), so that
any sedenion decomposes uniquely as p = ι1 (x) + ι2 (y) with x, y ∈ O.
For p ∈ S, write Lp and Rp for left- and right-multiplication by p, viewed as R-linear
maps S → S. Define the Gram operator Gp := L⊤
p Lp (with respect to the standard inner
product on S), and let Kp := ker Lp with orthogonal projector πp : S → Kp .
Definition 4.1 (Aphanic observer). A nonzero p ∈ S is aphanic if Kp ̸= {0}. The
aphanic locus is denoted Paph ⊂ S.
The Two-Condition Theorem [21] characterizes the aphanic locus: p = ι1 (x) + ι2 (y)
is aphanic iff x, y ∈ Im(O), ∥x∥ = ∥y∥, and ⟨x, y⟩ = 0. For aphanic p, dim Kp = 4
universally (Result 2, op. cit.), and the spectrum of Gp is
Spec(Gp ) =

 4
0 , ∥p∥2 8 , 2∥p∥2 4 ,

(15)

the universal 4–8–4 spectrum [21]. This is the only fact about Gp ’s spectrum that the
present section requires.

4.2

Closed-Form Pseudoinverse and Projector

The minimal polynomial of Gp on S is
mGp (λ) = λ(λ − ∥p∥2 )(λ − 2∥p∥2 ),

(16)

of degree three. Hence both the Moore–Penrose pseudoinverse G+
p and the kernel projector
πp are quadratic polynomials in Gp , with coefficients fixed by Lagrange interpolation
over the three eigenvalues.
16

## PDF page 17

Proposition 4.2 (Closed-form). For every aphanic p ∈ Paph ,
3
7
Gp −
G2 ,
4
4∥p∥
4∥p∥6 p
3
1
πp = I −
Gp +
G2 .
2∥p∥2
2∥p∥4 p

G+
p =

(17)
(18)

+
In particular G+
p , πp ∈ R[Gp ], and consequently [A, Gp ] = 0 =⇒ [A, Gp ] = 0 and

[A, πp ] = 0 for any A ∈ End(S).
7
3
3
1
2
π
2
Proof. The functions f + (λ) := 4∥p∥
4 λ − 4∥p∥6 λ and f (λ) := 1 − 2∥p∥2 λ + 2∥p∥4 λ satisfy

f + (0) = 0, f + (∥p∥2 ) = 1/∥p∥2 , f + (2∥p∥2 ) = 1/(2∥p∥2 ); and f π (0) = 1, f π (∥p∥2 ) = 0,
f π (2∥p∥2 ) = 0. Both functions take the same values as G+
p and πp respectively on
Spec(Gp ); since Gp is symmetric and its minimal polynomial has distinct roots, the
operator equalities follow.
Remark 4.3. At the basepoint p0 = e1 + e10 , ∥p0 ∥2 = 2, so the coefficients specialize to
7
3 2
3
1 2
G+
p0 = 16 Gp0 − 32 Gp0 and πp0 = I − 4 Gp0 + 8 Gp0 — both with dyadic coefficients. The

dyadic structure is special to p0 but the polynomial form is universal.
+
The annihilation identity G+
p πp = πp Gp = 0 — a direct consequence of πp projecting

onto the zero eigenspace of Gp — is the mechanical hinge of every argument that follows.

4.3

The Aphanic Curvature Operator

Definition 4.4 (Curvature operator). For p ∈ Paph and a, b ∈ Im(S), the aphanic
curvature operator is
+
Ca,b (p) := πp Lb G+
p La − La Gp Lb πp ∈ End(Kp ).



(19)

The operator Ca,b (p) is skew in (a, b), bilinear in (a, b), and lives entirely in End(Kp ) ∼
=
gl(4, R). Its image, as (a, b) ranges over Im(S) ∧ Im(S), is the local Hom(Kp , Kp )-content
of the Berry curvature derived from the kernel-projector connection on the aphanic
bundle (the global construction is recalled in §31 ). The identification is exact: Ca,b (p) is
the closed-form expression of the curvature 2-form’s restriction to the kernel.

4.4

G2 -Equivariance

The exceptional group G2 = Aut(O) acts on O by algebra automorphisms. We extend
the action to S diagonally:
σ̂ ι1 (a) + ι2 (b) = ι1 (σa) + ι2 (σb),


σ ∈ G2 .

(20)

Lemma 4.5 (Diagonal lift is a sedenion automorphism). For every σ ∈ G2 , σ̂ ∈ Aut(S).
1

For this section the closed-form expression (19) is taken as the working definition; the equivalence to
the geometric curvature 2-form is proven in the indicated section.

17

## PDF page 18

Proof. Direct verification using the CD product. For a, b, c, d ∈ O,
σ̂ (a, b)(c, d) = σ(ac − d¯b), σ(d a + b c̄)




= σa σc − σd σb, σd σa + σb σc



= (σa, σb)(σc, σd) = σ̂(a, b) σ̂(c, d),
where the second equality uses σ ∈ Aut(O) (σ preserves the octonion product) and
σ(z̄) = σz (automorphisms preserve conjugation, since z̄ = −z on Im(O) and σ preserves
Im(O)).
Lemma 4.6 (G2 -equivariance of the curvature operator). For every p ∈ Paph , every
σ ∈ G2 , and every a, b ∈ Im(S),
Cσ̂a, σ̂b σ̂p = σ̂ Ca,b (p) σ̂ −1 .

(21)



Proof. By Lemma 4.5, σ̂ is an algebra automorphism of S, so Lσ̂a = σ̂ La σ̂ −1 and similarly
+ −1
for R. As σ̂ is an isometry, Gσ̂p = σ̂ Gp σ̂ −1 , and from Proposition 4.2, G+
σ̂p = σ̂ Gp σ̂

and πσ̂p = σ̂ πp σ̂ −1 (noting ∥σ̂p∥ = ∥p∥). Substituting all four conjugations into (19)
yields (21).
The aphanic locus is a single G2 -orbit (modulo scaling): for any aphanic p there
exists σ ∈ G2 and c > 0 with p = c σ̂(p0 ) [21]. Combined with the elementary scaling
identity Ca,b (c p) = c−2 Ca,b (p) (immediate from (17) and (19)), this means it suffices to
prove statements about ker C · , · (p) at p0 and transport via Lemma 4.6.

4.5

Q-Centralizer Vanishing

Definition 4.7 (Q-centralizer). For aphanic p = ι1 (x) + ι2 (y) with x, y ∈ Im(O), let
Vp := spanR {x, y} ⊂ Im(O) and define the Q-centralizer
qp := ι1 (Vp ) ⊕ Rℓ ⊕ ι2 (Vp ) ⊂ Im(S).

(22)

For aphanic p we have dim Vp = 2 (since x, y are nonzero and orthogonal), hence
dim qp = 5 universally.
Lemma 4.8 (Q-Centralizer Vanishing, basepoint form). For every a ∈ Im(S),
Ca,b (p0 ) = 0 ∀ b ∈ Im(S)

⇐⇒

[La , L2p0 ] = 0

⇐⇒

a ∈ qp 0 .

(23)

Proof. Sufficiency. Suppose [La , L2p0 ] = 0. Since p0 ∈ Im(S), L⊤
p0 = −Lp0 , so Gp0 =

18

## PDF page 19

−L2p0 and [La , Gp0 ] = 0. By Proposition 4.2, [La , G+
p0 ] = 0. Then
+
Ca,b (p0 ) = πp0 Lb G+
p0 La − La Gp0 Lb πp0



+
= πp0 Lb La G+
p0 − Gp0 La Lb πp0

(using [La , G+
p0 ] = 0)



+
= (πp0 Lb La ) (G+
p0 πp0 ) − (πp0 Gp0 ) (La Lb πp0 ) = 0,
+
since G+
p0 πp0 = πp0 Gp0 = 0.

Necessity. The two implications a ∈ qp0 ⇒ [La , L2p0 ] = 0 ⇒ Ca,· (p0 ) = 0 have
already been established (sufficiency above, and direct CD computation for the first).
To close the loop we show dim a : Ca,· (p0 ) = 0 ≤ 5, which forces equality with qp0 .


Define the linear maps
Φ : Im(S) → End(S),

Φ(a) := [La , L2p0 ],

C : Im(S) → End(Kp0 )15 ,

C(a) := Ca,ej (p0 ) j=1 .

15

Both maps have qp0 ⊆ ker Φ ⊆ ker C (the second inclusion is sufficiency above). Their
kernels are determined by the rank of the corresponding Gram matrices on the 15-element
basis {e1 , . . . , e15 } of Im(S). Direct computation (at exact rational arithmetic; coefficients
lie in Z[ 18 ]) gives
Spec ΓΦ



=

Spec ΓC



=

 5
0 , 648 , 1282 ,
 5 2 4
4

0 , 1 , 4 , 28

(24)
(25)

,

where ΓΦ and ΓC are the Gram matrices ⟨Φ(ei ), Φ(ej )⟩F and

k ⟨Cei ,ek , Cej ,ek ⟩F respec-

P

tively. Both have nullity 5. With sufficiency qp0 ⊆ ker Φ and the equal-dimension count
dim ker Φ = dim ker C = 5, all three coincide: ker C = ker Φ = qp0 .
Remark 4.9 (On the rigor of (24)–(25)). The Gram matrices have entries in Z[ 18 ] (since
the Lagrange coefficients are dyadic at p0 and the basis Lei are signed permutation
matrices). Their ranks are therefore algebraic invariants computable in exact arithmetic.
The spectra in (24)–(25) are certified by exact rational eigenvalue/multiplicity verification:
for each predicted (λ, m) pair, the rank of λI − Γ over Q is computed by fraction-free
Gaussian elimination on the integer-scaled matrix (ΓΦ directly; ΓC via the integer Gram
of 2048 · Ca,b , whose eigenvalues are 20482 times those of ΓC ), and verified to equal 15 − m.
Sum of multiplicities 5 + 8 + 2 = 15 for ΓΦ and 5 + 2 + 4 + 4 = 15 for ΓC exhausts the
spectrum. Cross-check: rank of λI − Γ at five non-eigenvalues is full (= 15) in both
cases. A reference C++ implementation using 128-bit integer arithmetic with per-row
GCD reduction is reproducible from the probe op_F1_R133_exact_arithmetic.cpp in
the supplementary archive.
Theorem 4.10 (Q-Centralizer Vanishing, global form). For every aphanic p ∈ Paph and

19

## PDF page 20

every a ∈ Im(S),
Ca,b (p) = 0 ∀ b ∈ Im(S)

⇐⇒

[La , L2p ] = 0

⇐⇒

a ∈ qp .

(26)

Proof. The implications a ∈ qp ⇒ [La , L2p ] = 0 ⇒ Ca,· (p) = 0 are global by direct algebra:
the first is a CD calculation independent of basepoint, and the sufficiency argument in
Lemma 4.8 never uses anything specific to p0 beyond the universal spectrum (15), which
holds for all aphanic p.
For the converse, write p = c · σ̂(p0 ) with σ ∈ G2 and c > 0 (transitivity of G2
on the unit-aphanic locus, modulo scaling). By Lemma 4.6 and the scaling identity
Ca,b (cq) = c−2 Ca,b (q),
Ca,· (p) = 0 ⇐⇒ Cσ̂−1 a, · (p0 ) = 0 ⇐⇒ σ̂ −1 a ∈ qp0 ⇐⇒ a ∈ σ̂(qp0 ).
It remains to identify σ̂(qp0 ) with qp . Since σ̂ commutes with ι1 , ι2 (by the diagonal
action) and fixes ℓ,
σ̂(qp0 ) = ι1 σVp0 ⊕ Rℓ ⊕ ι2 σVp0 = ι1 (Vp ) ⊕ Rℓ ⊕ ι2 (Vp ) = qp ,




using Vp = σ(Vp0 ) from p = cσ̂(p0 ).
A first consequence settles the tangent-versus-ambient quantification used in the
curvature operator and the bridge theorem of §3.
Corollary 4.11 (Normal absorption: ambient span = tangential span). The unit aphanic
locus Paph sits inside the 14-dimensional subspace ι1 (Im O) ⊕ ι2 (Im O) ⊂ Im(S), with
the R+ -cone tangent space Tp Paph of dimension 12 (Proposition 3.1). Its orthogonal
complement in the 15-dimensional Im(S) is the 3-dimensional normal space
Np = spanR ℓ, ι1 (x) − ι2 (y), ι1 (y) + ι2 (x) ,


and Np ⊂ qp . Hence Ca,b (p) = 0 whenever a ∈ Np or b ∈ Np , and
spanR Ca,b (p) : a, b ∈ Im(S)


= spanR Ca,b (p) : a, b ∈ Tp Paph .


The ambient quantification over Im(S) in Definition 4.4 and Theorem 4.13 therefore
returns the genuine Berry curvature span of the bundle, not an artifact of extending past
the tangent space.
Proof. The two real-analytic constraints cutting out the cone Paph in ι1 (Im O) ⊕ ι2 (Im O)
are f1 = ∥x∥2 − ∥y∥2 and f2 = ⟨x, y⟩, with gradients proportional to ι1 (x) − ι2 (y) and
ι1 (y) + ι2 (x) respectively (Proposition 3.1); the radial direction p = ι1 (x) + ι2 (y) is
tangent to the cone. Adjoining ℓ, which is orthogonal to the entire 14-dimensional
ι1 (Im O) ⊕ ι2 (Im O), gives the 3-dimensional Np . Each spanning vector lies in qp =
20

## PDF page 21

ι1 (Vp ) ⊕ Rℓ ⊕ ι2 (Vp ) with Vp = span{x, y}: ℓ ∈ Rℓ, and both ι1 (x) − ι2 (y) and ι1 (y) + ι2 (x)
lie in ι1 (Vp )⊕ι2 (Vp ). Theorem 4.10 then gives Ca,· (p) = 0 for a ∈ Np ⊂ qp ; skew-symmetry
of C disposes of the b slot.
The corollary that motivates the next subsection is purely structural.
Corollary 4.12 (Spectral fingerprint of the aphanic bundle). For every aphanic p, after
rescaling to ∥p∥2 = 2, the Gram matrices ΓΦ (p) and ΓC (p) have the spectra {05 , 648 , 1282 }
and {05 , 12 , 44 , 284 } respectively. The spectra are G2 -invariants of the aphanic locus.
Proof. Lemma 4.6 gives Γ(σ̂p) = σ̂ Γ(p) σ̂ −1 for either Gram matrix, hence isospectrality
across the orbit. Scaling p 7→ cp scales each Gram entry by a fixed power of c, so
isospectrality after norm normalization is automatic.

4.6

Proof of the Rank Theorem

We now state the principal result of the section.
Theorem 4.13 (Rank of the aphanic curvature). For every aphanic p ∈ Paph , the linear
span
F(p) := spanR Ca,b (p) : a, b ∈ Im(S)


⊂ End(Kp )

(27)

has dimension exactly 4.
Proof. By Lemma 4.6, F(σ̂p) = σ̂ F(p) σ̂ −1 for σ ∈ G2 , so it suffices to compute
dim F(p0 ).
Reduction by Q-centralization. By bilinearity in (a, b), F(p0 ) is spanned by


Cei ,ej (p0 ) : 1 ≤ i, j ≤ 15 . Theorem 4.10 (basepoint form) gives Cei ,ej (p0 ) = 0 whenever

ei ∈ qp0 or (by skew-symmetry) ej ∈ qp0 . With qp0 = span{e1 , e2 , e8 , e9 , e10 }, the set
of a priori nonzero pairs (i, j) is reduced to indices in the 10-element complement
I := {3, 4, 5, 6, 7, 11, 12, 13, 14, 15}.
Self-duality identities at p0 . The kernel basis {v0 , v1 , v2 , v3 } = { √12 (e7 +e12 ), √12 (−e6 +

e13 ), √12 (e5 + e14 ), √12 (−e4 + e15 )} (the Gram–Schmidt-orthonormalized kernel computation; [21]) realizes F(p0 ) as a subspace of so(Kp ) ∼
= so(4), since L⊤ = −La for a ∈ Im(S)
a
0
+
and Gp0 , πp0 are self-adjoint. The space so(4) decomposes as so(4) = so(3)+ ⊕ so(3)−
under the Hodge involution ∗ : ∧2 Kp0 → ∧2 Kp0 .

Direct computation in the {v0 , v1 , v2 , v3 } basis (Appendix C) yields the following
self-duality identities at p0 :
Ce4 ,e5 (p0 ) = Ce6 ,e7 (p0 ),

Ce4 ,e6 (p0 ) = −Ce5 ,e7 (p0 ),

Ce4 ,e7 (p0 ) = Ce5 ,e6 (p0 ),

(28)

and analogous identities on the doubled half {12, 13, 14, 15}:
Ce12 ,e13 (p0 ) = Ce4 ,e5 (p0 ),

Ce12 ,e14 (p0 ) = Ce4 ,e6 (p0 ),

21

Ce12 ,e15 (p0 ) = Ce4 ,e7 (p0 ),

(29)

## PDF page 22

(and similarly for the remaining three pairs). Identities (28) are precisely the conditions
C|e4 ∧e5 = ∗ C|e4 ∧e5 etc., witnessing F(p0 ) ⊂ so(4)+ . Identities (29) witness an octonionhalf doubling redundancy: the two imaginary halves {e4 , . . . , e7 } and {e12 , . . . , e15 }
contribute the same three self-dual generators, not six.
Generators. Define the three self-dual operators
J 1 := 12 Ce5 ,e4 (p0 ),

J 2 := 12 Ce6 ,e4 (p0 ),

J 3 := 21 Ce7 ,e4 (p0 ),

(30)

and the Fano cross-half generator
ω := Ce3 ,e11 (p0 ),

(31)

the unique nonzero Cei ,ej (p0 ) with one index in the Fano-tunneler class of Proposition 4.17.
The index ordering in the J a definitions — placing the kernel-mixing direction e4+a
before the seed direction e4 — is the convention that aligns {J 1 , J 2 , J 3 } with the standard
't Hooft self-dual tensors [22]. Direct computation gives ∥J a ∥F = ∥ω∥F = 1 and the
bracket relations
[J a , J b ] = εabc J c ,

[ω, J a ] = 0

(a, b, c ∈ {1, 2, 3}),

(32)

exhibiting span{J 1 , J 2 , J 3 } ∼
= su(2) and span{ω} as the commuting u(1) center. The
four operators are pairwise orthogonal in the Frobenius inner product, hence linearly
independent in so(4).
Span exhaustion. A complete enumeration (Appendix C, §C.3) verifies that every
Cei ,ej (p0 ) for i, j ∈ I is an integer linear combination of {J 1 , J 2 , J 3 , ω}, with all 25
nonzero pairs decomposed exactly: the residual is the identically zero integer matrix in
every case, and the coefficients are exact integers, not roundings. Hence dim F(p0 ) = 4,
certified in exact arithmetic in both directions: an exhibited nonzero 4 × 4 minor bounds
the rank below, and fraction-free row reduction of the stacked integer matrix bounds it
above. The restriction to the index set I is itself certified rather than assumed: over all
105 pairs 1 ≤ i < j ≤ 15, every pair meeting the centralizer qp0 restricts to exactly zero,
leaving exactly the 25 nonzero pairs tabulated.
Transport. By Lemma 4.6, dim F(p) = dim F(p0 ) = 4 for every p ∈ Paph .
Remark 4.14 (Relation to the self-dual Yang–Mills tensor basis). The triple {J 1 , J 2 , J 3 }
generates su(2)+ inside so(4) ∼
= su(2)+ ⊕ su(2)− , with brackets (32) matching the
standard 't Hooft self-dual tensors of four-dimensional Yang–Mills theory [22]. The
fourth generator ω commutes with the su(2)+ triple and reproduces the u(1) center
identified in [21]. Thus F(p) ∼
= u(1) ⊕ su(2) as a Lie subalgebra of so(Kp ). This computes
the pointwise curvature span; Proposition 4.15 below upgrades it to the full holonomy
algebra u(2) of the aphanic bundle.
We note only that u(2) is, up to isomorphism, the Lie algebra of the electroweak
22

## PDF page 23

gauge group. That is a coincidence of Lie-algebra type and nothing more: no metric, no
spinor bundle, no Yukawa sector, and no gauge-theoretic dynamics are supplied here,
and we make no physical claim. The comparison is offered as motivation only.

4.7

From Curvature Span to Holonomy

Theorem 4.13 computes the pointwise curvature span F(p). By the Ambrose–Singer
theorem, the holonomy algebra holp (∇) of the kernel-projector connection contains the
parallel transports of all curvature operators, giving the lower bound hol (∇) ⊇ F(p) ∼
=
p

u(2). The reverse inclusion is not automatic — transport could a priori enlarge the
span inside so(Kp ) ∼
= so(4). The following proposition supplies the cap, using only the
algebraic centrality of right multiplication by the doubling generator.
Proposition 4.15 (Parallel complex structure and holonomy cap). Let Rℓ denote right
multiplication by ℓ = e8 on S. For every aphanic p:
(i) [Rℓ , Gp ] = 0 — a Cayley–Dickson flexibility identity, algebraic and basepointindependent [21]. By Proposition 4.2 (πp ∈ R[Gp ]), [Rℓ , πp ] = 0, so Rℓ preserves
Kp and restricts to Jp := Rℓ |Kp ∈ End(Kp ).
(ii) Jp2 = − idKp (since Rℓ2 = −I for the unit imaginary ℓ) and Jp⊤ = −Jp ; thus Jp is a
∇-compatible complex structure on Kp .
(iii) Jp is ∇-parallel: Rℓ is a fixed (p-independent) ambient linear map, so d(Rℓ s) =
Rℓ ds for any section s; combined with [Rℓ , πp ] = 0 from (i), Rℓ commutes with
∇ = π ◦ d, giving ∇(Jp s) = Rℓ ∇s, i.e. ∇J = 0.
Consequently the holonomy group Holp (∇) commutes with Jp and lies in the centralizer
of Jp in SO(Kp ) ∼
= SO(4), which is U(2). Hence hol (∇) ⊆ u(2), and with the Ambrose–
p

Singer lower bound,
holp (∇) = F(p) = u(1) ⊕ su(2) = u(2).

(33)

The abelian u(1) centre is spanned by the generator ω of Theorem 4.13, which satisfies
(2ω)2 = − idKp and coincides up to sign with 12 Jp ; that is, the central factor of the
holonomy is (one half of) the restriction to Kp of right multiplication by the Cayley–
Dickson doubling generator.
Proof. Items (i)–(iii) are pointwise statements; what remains is to pass from them to
the holonomy group, which is where the cap is earned. Write g := ⟨·, ·⟩K and, for a
piecewise-smooth loop Γ based at p, let ΠΓ ∈ GL(Kp ) be parallel transport around Γ for
∇.
Step 1: ΠΓ is g-orthogonal. By Lemma 3.6, ∇ is metric. If s, t are ∇-parallel along Γ
d
then dt
⟨s, t⟩K = ⟨∇s, t⟩K + ⟨s, ∇t⟩K = 0, so g is constant along Γ and ΠΓ ∈ O(Kp , g).

23

## PDF page 24

Step 2: ΠΓ commutes with J. By (iii), ∇J = 0. Hence if s is parallel along Γ, so is Js,
since ∇(Js) = J∇s = 0. Transporting Jp s(0) therefore yields Jp s(1), i.e. ΠΓ Jp = Jp ΠΓ .
Step 3: the centralizer of Jp in O(Kp , g) is U(2). By (ii), Jp2 = − id and Jp⊤ = −Jp ,
so Jp⊤ Jp = id: Jp is a g-orthogonal complex structure, and Kp becomes a complex vector
space of complex dimension 2. The pairing
h(u, v) := ⟨u, v⟩K − i ⟨u, Jp v⟩K
is C-linear in v, satisfies h(v, u) = h(u, v) (using Jp⊤ = −Jp ), and has Re h = g. A
real-linear map that preserves g and commutes with Jp preserves h, hence is h-unitary;
conversely every h-unitary map is C-linear and g-orthogonal. Therefore


A ∈ O(Kp , g) : AJp = Jp A

= U(Kp , h) ∼
= U(2).

By Steps 1–2, Holp (∇) lies in the left-hand side. Hence Holp (∇) ⊆ U(2) and holp (∇) ⊆
u(2). No curvature estimate is used: the cap comes from the two compatibilities alone.
Step 4: equality. The Ambrose–Singer theorem gives the reverse inclusion F(p) ⊆
holp (∇), and Theorem 4.13 gives dim F(p) = 4 = dim u(2). Squeezing, 4 = dim F(p) ≤
dim holp (∇) ≤ dim u(2) = 4, which forces (33). Note that only the dimension of the
curvature span is needed here, not the stronger assertion that transported curvature
operators already exhaust holp (∇).
The ingredients are independently certified. Metric compatibility (Lemma 3.6) and
[Rℓ , Gp ] = 0 (the Rℓ centrality theorem of [21], proved symbolically for every imaginary
p) are exact and basepoint-free; with Proposition 4.2 they give [Rℓ , πp ] = 0 and hence
(i). The identities Rℓ2 = −I, Rℓ⊤ Rℓ = I and Rℓ⊤ = −Rℓ on S are exact integer matrix
identities, independent of p, and yield (ii); Rℓ is a signed permutation of the basis. The
probe op_keystone_cap certifies these in exact arithmetic, together with the centralizer
dimension dim{X ∈ so(Kp ) : [X, Jp ] = 0} = 4 and its coincidence with F(p0 ), and
confirms (i)–(ii) at thirteen exactly-aphanic basepoints, seven monomial and six not.
Remark 4.16. The cap closes the gap between “the curvature spans u(2)” and “the
holonomy is u(2).” It also identifies ω intrinsically: ω is not merely one self-dual tensor
among others but a fixed shadow of the algebra’s doubling structure. The identity
[Rℓ , Gp ] = 0 is tower-universal across Cayley–Dickson levels n = 2k ≥ 16 [21], so the
abelian factor persists up the tower (the curvature-span computation, by contrast, is
carried out here only at the sedenion level).

4.8

The Eigenspace Mixing Trichotomy

The proof of Theorem 4.13 ran cleanly because the basepoint table partitioned naturally
— five generators killed everything (Q-centralizer), and ten generators contributed. The
same partition has finer structure that explains both why the count is 4 and where the 't

24

## PDF page 25

B Fano tunnel, wt. 8

Kp
dim 4
λ=0

E2 (p)
dim 8
λ = ∥p∥2

A
wt. 2

C
wt. 2

adjacent A, C ⇒ J 1 , J 2 , J 3 (su(2))

E4 (p)
dim 4
λ = 2∥p∥2

Fano B ⇒ ω (u(1))

Figure 2: Eigenspace mixing channels at an aphanic observer. The Gram operator Gp
splits S = Kp ⊕E2 (p)⊕E4 (p) into its 0-, ∥p∥2 -, and 2∥p∥2 -eigenspaces (dimensions 4, 8, 4).
An imaginary direction a couples these blocks through the three off-diagonal channels
A, B, C of Proposition 4.17, weighted
by the squared eigenvalue gaps in ∥[La , L2p ]∥2F =

∥p∥4 2∥A∥2F + 8∥B∥2F + 2∥C∥2F . The two adjacent channels A, C generate the self-dual
triple J 1 , J 2 , J 3 (su(2)); the direct Fano tunnel B, which bypasses E2 , generates the
commuting center ω (u(1)). The rank dim F(p) = 4 counts these channels.
Hooft tensor enters geometrically.
For aphanic p, the spectrum decomposition S = Kp ⊕E2 (p)⊕E4 (p) — the eigenspaces
of Gp for eigenvalues 0, ∥p∥2 , 2∥p∥2 respectively — is preserved by every La with a ∈ qp .
For a ∈
/ qp , the operator La mixes the three eigenspaces, and the mixing is highly
constrained.
Proposition 4.17 (Eigenspace Mixing Trichotomy). For aphanic p and a ∈ Im(S),
decompose La into the nine Hom(Eµ (p), Eν (p)) blocks (µ, ν ∈ {0, 2, 4}, where E0 (p) :=
Kp ). Define the off-diagonal block norms
Aa := πKp La πE2 (p) ,

Ba := πKp La πE4 (p) ,

Ca := πE2 (p) La πE4 (p) .

Then for every a ∈ Im(S),
2



[La , L2p ] F = ∥p∥4 2 ∥Aa ∥2F + ∥Ca ∥2F





+ 8 ∥Ba ∥2F .

(34)

At the basepoint p0 , the imaginary basis directions partition into three classes:
Indices

∥A∥2F

∥B∥2F

∥C∥2F

∥[La , L2p0 ]∥2F

Centralizer qp0

{1, 2, 8, 9, 10}

0

0

0

0

Adjacent mixer

{4, 5, 6, 7, 12, 13, 14, 15}

4

0

4

64

Tunneler (Fano)

{3, 11}

0

4

0

128

Class

The same table holds for any aphanic p after relabeling qp and rescaling by ∥p∥4 .
Proof. Identity (34) is a direct computation: L2p is self-adjoint with eigenvalues {0, −∥p∥2 , −2∥p∥2 }
on {Kp , E2 , E4 } (recall Gp = −L2p for imaginary p); the squared Frobenius norm of
25

## PDF page 26

[La , L2p ] decomposes block-by-block, and only off-diagonal blocks contribute, weighted by
the squared eigenvalue gaps:
∥p∥4 (2∥A∥2 + 2∥C∥2 ) + 2 (2∥p∥2 )2 ∥B∥2 = ∥p∥4 2∥A∥2 + 8∥B∥2 + 2∥C∥2 .


The basepoint table is verified by enumeration of ∥Aei ∥F , ∥Bei ∥F , ∥Cei ∥F



for i =

1, . . . , 15 (the probe op_F1_quantization_block_structure.cpp in the supplementary
archive), and all 15 rows are certified in exact integer arithmetic by op_six_anchors_B:
the three block projectors are exact integer polynomials in Gp , certified idempotent with
traces 4, 8, 4, and every rescaling is an exact division. The weights (2, 8, 2) in the identity
above are confirmed exactly, row by row. Universality across the aphanic locus follows
from G2 -equivariance applied to each block projection (Lemma 4.6).
Remark 4.18 (Fano elements as direct K ↔ E4 tunnels). The Fano completions e3 = e1 e2
and e11 = e3 ℓ at p0 are the unique imaginary basis directions with A = C = 0 and B ̸= 0
— they mix the kernel directly with the highest eigenspace, bypassing the intermediate
E2 . This is the structural reason that the u(1) generator ω = Ce3 ,e11 (p0 ) exists as a fourth
independent operator in F(p0 ): the K ↔ E4 tunneling produces a curvature contribution
that the adjacent mixers cannot generate.
The proposition’s value is conceptual rather than technical: Theorem 4.13 can be read
off from Proposition 4.17 as the statement that the rank of F(p) equals the number of
distinct mixing channels into Kp (three from adjacent mixing, one from Fano tunneling),
exactly 4.

4.9

Summary

The closed-form representation of the curvature operator (Definition 4.4, Proposition 4.2) reduces the rank theorem to a finite-dimensional commutator question. The
G2 -equivariance lemma (Lemma 4.6) reduces it further from the 11-dimensional aphanic
locus to a single basepoint. The Q-Centralizer Vanishing Theorem (Theorem 4.10)
exhausts the basepoint count by identifying the 5-dimensional kill set qp explicitly. The
remaining 10-dimensional contribution splits, by the Eigenspace Mixing Trichotomy
(Proposition 4.17), into eight adjacent mixers and two Fano tunnelers; the self-duality
identities (28) and the octonion-half doubling (29) reduce these ten contributions to four
linearly independent generators {J 1 , J 2 , J 3 , ω}.
The u(1) ⊕ su(2) = u(2) holonomy algebra of the aphanic bundle (curvature span by
Theorem 4.13, capped to the holonomy algebra by Proposition 4.15) thus emerges from
sedenion algebra alone, without any input from differential geometry or physics.

26

## PDF page 27

5

Discrete Formulas

Section 4 described the curvature of the aphanic bundle as an operator: the u(2)-valued
Berry curvature Ca,b (p) on the kernel fibre. Monitoring a running system instead calls
for a scalar: a single number per step measuring how fast the hidden sector turns along
an actual trajectory. We now introduce that pathwise creative-curvature scalar κγ , the
operational projection of the operator-level structure of §4 onto a sampled path rather
than a new object. For computational implementation this continuous pathwise curvature
must be discretized; we provide two equivalent forms.

5.1

Turn-Angle Form

Let {ak }N
k=0 be a discrete sequence of hidden-sector representatives along a sampled
trajectory, normalized so that ∥ak ∥ = 1. Define:
Definition 5.1 (Discrete Creative Curvature).
κγ [k] = arccos ⟨ak , ak+1 ⟩ ,


(35)

the geodesic angle between successive hidden generators on the unit sphere.
This is the discrete analogue of equation (19): angular displacement per step. When
ak and ak+1 are nearly parallel, κγ [k] ≈ 0 (refinement). When they are nearly orthogonal,
κγ [k] ≈ π/2 (maximal turning).
Gauge invariance. Each ak is a unit representative chosen within the 4-dimensional
fiber Kpk , so ⟨ak , ak+1 ⟩, and hence κγ [k] as written, depends on that choice of section, i.e.
it is gauge-dependent. The section-independent quantity is the principal angle between
the kernel subspaces Kpk and Kpk+1 , equivalently the projector distance ∥πk+1 − πk ∥F
(with πk the closed-form projector of Proposition 4.2); (35) recovers the leading principal
angle once a parallel-transported section is fixed. We use the projector-distance form
wherever a gauge-invariant diagnostic is required.

5.2

G-Metric Form

A second form weights the inter-fiber step by the ambient Gram operator Gk = LTpk Lpk .
We emphasize that Gk is not a metric on the hidden sector itself: Kpk is exactly the
zero eigenspace of Gk , so Gk |Kpk = 0 (the 4–8–4 spectrum). The chord δak = ak+1 − ak ,
however, leaves Kpk , and
κγ [k] =

q

δaTk Gk δak ,

reduces, using Gk ak = 0, to κγ [k] =

δak = ak+1 − ak ,

(36)

q

aTk+1 Gk ak+1 : the energy the current Gram

operator assigns to the incoming generator. It vanishes iff ak+1 ∈ Kpk (the kernel has
27

## PDF page 28

not moved) and is non-degenerate precisely because it probes the chord between fibers,
not a metric within one.

5.3

Exogenous Subtraction

Not all hidden-sector rotation is internally generated. External perturbations (new data,
user interventions, environmental changes) can rotate ak without the system doing any
creative work. We subtract these.
Definition 5.2 (Exogenous Subtraction). Let Ek be the subspace of hidden-sector
variation attributable to exogenous input at step k. The intrinsic creative curvature is:
κint
γ [k] =

ΠE ⊥ δak
k



(37)

,

where ΠE ⊥ is orthogonal projection onto the complement of Ek .
k

Proposition 5.3 (Graceful Degradation). If Ek cannot be fully identified (rank-deficient
estimation of the exogenous subspace), then κint
γ [k] overestimates intrinsic curvature by
at most ∥ΠEk δak ∥, and in particular:
κint
γ [k] ≤ κγ [k].
The estimate is conservative: unidentified exogenous components are attributed to intrinsic
creativity, not the reverse.
Proof. By orthogonal decomposition, δak = ΠE ⊥ δak + ΠEk δak . Then ΠE ⊥ δak
k

k

≤

∥δak ∥ = κγ [k]. Equality holds when Ek = {0}, i.e., when no exogenous component is
true = Π
subtracted. The overestimate κint
γ − κγ
Ẽ ⊥ ∩Ek δak vanishes when Ẽk ⊇ Ek .
k

5.4

Phase Transition Score

Definition 5.4 (Phase Transition Score).
Φk = ϱk · κγ [k],

(38)

where ϱk is the mass of state k, a measure of the state’s influence on downstream
computation (e.g., attention weight, probability mass, or allocation fraction).
Mass-weighted curvature serves as a cheap pre-filter: high Φk flags states where a
massive (influential) component is turning rapidly, the signature of a phase transition.
Low-mass components can turn freely without systemic consequence.

28

## PDF page 29

6

The State Vector

At each step k, the curvature monitor observes the composite state vector:
xk = ak , κγ [k], Vk , ϱk , σksurv , Cksurv ,


(39)

where ak ∈ ker(Lγ(k) ) is the hidden-sector representative, κγ [k] is the discrete curvature,
Vk is the verification weight, ϱk is the mass, and σksurv ∈ {0, 1} is the survival indicator
(does the creative output persist beyond a confirmation horizon Lconfirm ?).
The hidden projection ΠA : V → ker(Lp ) extracts the component of any vector that
lies in the hidden sector. When a metric G is available on the ambient space V , the
Gram structure G|ker(Lp ) provides the pullback metric on the hidden sector.

7

Verified Creativity

Curvature alone does not distinguish creation from hallucination. A system that turns
rapidly while breaking every contract is not creative; it is unmoored. Verification provides
the second leg.
Definition 7.1 (Verification Weight). The verification weight Vk ∈ [0, 1] is the fraction
of the curvature at step k that survives dialectical verification. In a thesis-antithesissynthesis architecture:
Vk =

apost-synthesis
k
apost-thesis
k

,

the ratio of hidden-sector magnitude after synthesis to its magnitude after thesis.
Definition 7.2 (Speed Gate). The speed gate σkspeed ∈ {0, 1} prevents trivially slow
trajectories from registering as creative:
σkspeed =


1

if ∥γ̇k ∥ > vmin ,

0

otherwise.

(40)

Definition 7.3 (Survival-Gated Creativity Score). The survival-gated verified creativity
score is:
Cksurv = κγ [k] · Vk · σksurv .

(41)

The triple product gates on three independent conditions: the system must be turning
(κγ > 0), the turn must survive verification (Vk > 0), and the result must persist beyond
the confirmation horizon (σksurv = 1). Failure of any single factor zeroes the score.
Remark 7.4 (Failure Mode Separation). The score Cksurv admits exactly five failure modes,
each diagnosable from a distinct component of the triple product (Table 1). Since Cksurv
is a product of three non-negative factors, it vanishes if and only if at least one factor
vanishes. The first factor κγ vanishes in stagnation. The second Vk is low in hallucination
29

## PDF page 30

and medium in drift. The third σ surv vanishes in ephemeral sparks. The five modes are
exhaustive under the decomposition Cksurv > 0 vs. Cksurv = 0 crossed with which factor is
responsible.
Table 1: Failure mode taxonomy for Cksurv .
Mode

κγ

Vk

σ surv

Stagnation
Hallucination

≈0
>0

–
low

–
–

Ephemeral spark
Drift

>0
>0

high
med

0
1

Genuine creation

>0

high

1

8

Diagnosis
Hidden sector stationary; no structural change
Turning fails verification; unmoored from constraints
Verified turn that does not persist
Persistent but weakly verified; slow quality
erosion
Verified, persistent structural transformation

The Seven-Regime Taxonomy

The continuous quantities (κγ , Vk , Φk , Cksurv ) are mapped to seven discrete operational
regimes via threshold classification.
Table 2: Seven-regime operational taxonomy.
Regime

κγ

Vk

Φk

Cksurv

System state

1. Dormant
2. Refining
3. Exploring
4. Creating

≈0
low
med
high

–
high
med
high

low
low
med
high

0
≈0
low
high

5. Drifting
6. Hallucin.
7. Transition

med
high
spike

low
low
–

med
high
spike

low
0
–

No hidden-sector activity
Smooth exploitation within constraints
Testing constraint boundaries
Verified deformation of constraint manifold
Gradual departure from constraints
Rapid unconstrained departure
Discontinuous hidden-sector restructuring

Remark 8.1 (Pivot Detection). The transition Regime 4 → Regime 6 → Regime 4
(creation followed by brief hallucination followed by renewed creation) is a pivot: the
system temporarily loses verification while restructuring, then regains it at a new
constraint level. Pivots are desirable. The hysteresis parameter Lconfirm prevents the
monitor from penalizing pivots by requiring that regime transitions persist for at least
Lconfirm steps before triggering operational responses.
Remark 8.2 (Silent Decay). The transition Regime 2 → Regime 5, from refining to
drifting, is the most dangerous failure mode because it involves no curvature spike.
The system does not suddenly hallucinate; it gradually loses verification quality while
continuing to produce apparently normal output. This is the regime where Vk tracking
is essential and κγ alone is insufficient.
30

## PDF page 31

Remark 8.3 (Curvature Without Verification). The verification weight Vk presupposes a
verification oracle (see Limitation 4 in Section 10.3). However, the framework retains
value even when Vk is unavailable. Setting Vk = 1 (no verification), the curvature κγ
alone distinguishes stasis from motion, and the holonomy phase θ(Γ) classifies closed
loops independently of verification. The contribution of this paper is the geometric
monitoring layer; the verification interface is modular.

9

A Holonomy Phase for Closed Arcs

We now define a U(1) holonomy phase that classifies closed dialectical arcs by the net
structural turning they accumulate. We stress at the outset that this is a geometric
(holonomy) invariant, not a topological one: the aphanic base is simply connected (it is
an R+ -cone over G2 /SU(2), and π1 (G2 /SU(2)) = 0), so the phase is curvature-driven
and deformation-sensitive, not quantized by homotopy.
Let Γ : [0, 1] → Paph be a closed loop in the aphanic locus (Γ(0) = Γ(1)). Along Γ
the hidden sector ker(LΓ(t) ) varies smoothly. The real rank-4 kernel bundle carries the
∇-parallel complex structure J = Rℓ |K of Proposition 4.15, which makes each fiber a
complex space and supplies a genuine U(1) connection 1-form: for a unit section a of K,
α(X) := ⟨J a, ∇X a⟩.

(42)

The naive real expression ⟨a, ∇X a⟩ = 12 X∥a∥2 vanishes identically for a unit section; the
complex structure J is exactly what makes the abelian phase nonzero, playing the role
of the factor i in the Hermitian Berry connection.
Definition 9.1 (Holonomy phase). The holonomy phase of a closed dialectical arc Γ is
θ(Γ) =

I
Γ

α ∈ R/2πZ ∼
= U(1),

(43)

the U(1) holonomy of the connection (42) around Γ.
The phase θ(Γ) is not integer-valued or homotopy-protected. Because Paph is simply
connected, every loop is contractible and θ(Γ) varies continuously under deformation of
Γ: by Stokes it equals the enclosed abelian curvature flux, θ(Γ) =

RR

DF

∇
u(1)

for any

disk D with ∂D = Γ. It is the abelian U(1) component of the bundle’s holonomy, whose
full holonomy algebra is u(2) (Proposition 4.15); the non-abelian SU(2) component is
the Wilczek–Zee generalization and is not used here. The kernel bundle does carry a
genuine topological invariant, a nontrivial Z/2 characteristic class, the “aphanic twist”,
but it lives in H 6 (G2 /SU(2); Z/2) [21] and classifies the bundle, not individual arcs: it is
detected by five- and six-dimensional cycles, never by π1 , and is therefore unrelated to
θ(Γ).

31

## PDF page 32

Proposition 9.2 (Classification of Dialectical Arcs). Let Γ be a closed loop in the
1
aphanic locus Paph , and let κ¯γ (Γ) = |Γ|

H

Γ κγ (t) dt be the mean creative curvature. Then

exactly one of the following holds:
(i) κ¯γ = 0 and θ(Γ) = 0: Stasis loop. The hidden sector is stationary and the loop
produces no structural change.
(ii) κ¯γ > 0 and θ(Γ) = 0: Drift loop. The hidden sector rotates but returns to its
initial configuration. The system explores without transforming.
(iii) κ¯γ > 0 and θ(Γ) ̸= 0: Turning loop. The hidden sector accumulates a nonzero
net holonomy phase and does not return to its initial orientation. The arc has
enclosed nonzero curvature flux, a quantitative certificate of net structural turning.
(This is geometric, not homotopy-protected; see the proof.)
The mathematical content is concentrated in case (i): vanishing curvature implies
trivial holonomy. Cases (ii) and (iii) are definitional: they organize the operational
taxonomy by partitioning the (κ¯γ , θ(Γ)) plane.
Proof. Case (i). If κ¯γ = 0, then κγ (t) = 0 for almost all t (since κγ ≥ 0). The hidden
generator is parallel-transported: ∇γ̇ a = 0 along Γ. The connection form α = ⟨Ja, ∇γ̇ a⟩
vanishes along Γ, so θ(Γ) =

Γ 0 dt = 0.

H

Case (ii). κ¯γ > 0 implies the hidden sector rotates along Γ, but θ(Γ) = 0 in R/2πZ
means the net accumulated phase is trivial: the hidden sector returns to its initial
orientation despite moving.
Case (iii). θ(Γ) ̸= 0 means the U(1) holonomy around Γ is nontrivial: the hidden
sector does not return to its initial orientation in the complex line spanned by {a, Ja}.
By Stokes the arc encloses nonzero abelian curvature flux, θ(Γ) =

RR

DF

∇|
u(1) ̸= 0. This

is a quantitative certificate of net turning, not a discrete topological charge, and it is
not homotopy-protected: since Paph is simply connected, Γ can be contracted and θ(Γ)
driven continuously to zero as the enclosed flux shrinks. The phase records how much
curvature the arc actually swept.
Remark 9.3 (The Regime Sequence as Holonomy Instrument). The regime taxonomy of
Section 8 provides the local diagnostic (what is the system doing now?). The holonomy
phase provides the global diagnostic (what did the system accomplish over a complete
cycle?). Together they form a complete instrument: the regime sequence is the trajectory,
and θ(Γ) is its holonomy shadow.

10

Discussion

10.1

Relationship to Information Geometry

Information geometry and aphanics operate on complementary structures. The Fisher
metric measures curvature of the visible statistical manifold: how predictions change as
32

## PDF page 33

parameters vary. Creative curvature measures curvature of the hidden sector: how the
kernel of the action operator rotates as the system moves. In a system where the Fisher
metric is flat (parameters change smoothly without surprises), the creative curvature can
be large (the hidden sector restructures dramatically). The two metrics are generically
independent.
A deeper connection may exist through the null space of the Fisher matrix itself:
directions in parameter space along which the likelihood surface is flat correspond to
structural unidentifiability: parameters the data cannot see. These are precisely the
“hidden generators” from the statistical perspective. Whether the null space of the Fisher
matrix carries the same bundle structure as ker(Lp ) is an open question.

10.2

The Null-Space Inversion

The central philosophical move of aphanics, treating the null space as generative rather
than deficient, has a concrete mathematical consequence. In standard treatments,
ker(Lp ) ̸= {0} signals a singularity: the operator is non-invertible, the system is degenerate, the computation fails. Aphanics reinterprets this singularity as the locus of
maximal structural richness. The hidden sector is largest precisely where the system is
most “degenerate” in the classical sense, and this is where creative curvature is most
interesting.
The motivating algebraic setting sharpens this picture: the abelian component of
the holonomy on the hidden sector is generated by an ambient operator on the parent
algebra (Section 4.1), and the same identification recurs at every Cayley–Dickson level
where the hidden sector exists. The null-space inversion is therefore not opportunistic
relabeling but a structural discovery: the kernel inherits a measurement operator from
the algebra it sits inside, and that inherited operator (the complex structure J = Rℓ |K )
is what supplies the abelian U(1) holonomy phase in case (iii) of Proposition 9.2.
This inversion has precedent. Zero divisors in non-associative algebras were long
considered pathological; recent work has shown them to be algebraically and geometrically
rich. Singularities in algebraic geometry are the loci of maximal information density.
Phase transitions in statistical mechanics occur at parameter values where the partition
function is singular. In each case, the null space is not empty space; it is compressed
structure.
Remark 10.1 (Cross-Domain Resonances). The sign-flip from deficiency to generativity
has structural parallels across domains: Gödel’s incompleteness (the unprovable statement
is what prevents collapse into decidability), Heisenberg’s uncertainty (the non-commuting
observable is what allows conjugate properties to coexist), and Arrow’s impossibility (the
intransitive social preference is what prevents dictatorial aggregation). We do not claim
these are instances of a single mathematical theorem; the structures differ in essential
ways. We note only that the interpretive move of treating a null space as generative
rather than deficient recurs across formalisms, and that aphanics provides one concrete
33

## PDF page 34

algebraic setting where this move has precise content.

10.3

Limitations

We note six limitations of the present framework:
1. Theorem/proposal boundary. Sections 3–4 establish geometric theorems in the
sedenion model. Sections 5–9 define an instrumentation template for dialectical
systems; applying it to an actual deployed system requires that the system expose,
or approximate, a hidden-sector bundle with the stated structure. That the
templates apply to any particular running system is not established here.
2. Geometric, not topological, loop phase. The aphanic base considered here
is simply connected, so the holonomy phase θ(Γ) is not a homotopy invariant of
loops. It is a curvature-driven holonomy phase: deformation-sensitive, quantitative,
and useful as a certificate of net structural turning, but not quantized by π1 . The
only topologically protected quantity is the Z/2 class of the bundle itself (in H 6 ),
which classifies the bundle, not individual arcs.
3. Connection dependence. The holonomy phase θ(Γ) depends on the choice of
connection. The framework uses the canonical kernel-projector connection together
with the parallel complex structure J = Rℓ |K (Proposition 4.15); this is natural in
the sedenion setting but a different bundle would require its own canonical choice.
4. Exogenous estimation. The exogenous subtraction procedure (Section 5.3)
requires identifying the exogenous subspace Ek . In practice this is approximate,
and Proposition 5.3 only guarantees conservative (upward) bias. Systematic
overestimation of intrinsic curvature could lead to false-positive creativity detection.
5. Verification oracle. The verification weight Vk presupposes access to a verification
procedure. In dialectical architectures this is built in (the antithesis). In other
architectures it must be supplied externally, and the quality of Vk depends on the
quality of the oracle.
6. Computational cost. Computing κγ requires tracking the kernel of Lp at every
step, which may be expensive in high-dimensional systems. The discrete turn-angle
form (Section 5.1) is O(dim V ) per step, but the G-metric form (Section 5.2)
requires the full Gram operator.

11

Conclusion

We have introduced aphanics, the study of structurally real generators that are annihilated
by a system’s own internal action, and derived from it a geometric framework for

34

## PDF page 35

monitoring creativity in cognitive and dialectical systems. The framework rests on three
pillars:
Creative curvature κγ measures the rate at which the hidden sector rotates orthogonal
to the system trajectory. It is intrinsic, parameterization-free, and distinguishes refinement
from genuine structural turning.
Verified creativity Cksurv gates curvature on dialectical verification and temporal
persistence, separating five failure modes (stagnation, hallucination, ephemeral spark,
drift, genuine creation) from a single observable triple product.
The holonomy phase θ(Γ) classifies closed dialectical arcs by the net curvature flux
they enclose, providing a U(1) geometric (holonomy) certificate (deformation-sensitive
rather than topological, since the aphanic base is simply connected) that distinguishes
turning loops from drift.
The framework is constructive: we have provided discrete formulas, operational
taxonomies, and a failure-mode classification that can be instrumented in any system
with access to its hidden sector. The algebraic foundations that validate these tools in
a concrete setting, the sedenion algebra, are reported in a companion work [21]. The
present framework is a proposal; its ultimate value depends on the depth of that algebraic
foundation and on empirical demonstration in operational systems.

Acknowledgments
The author thanks Christopher J. Vizas, the gadfly this work needed in the oldest and
best sense of that word, and Jacob Hall, the friend who gives that word its definition.
The author also thanks the team at Agingo, who carried the daily work while this one
was being written.
Above all, the author thanks his mother, who encouraged blindly and had to watch
and worry while the proof was still being built to convey what she already knew. She
loved unconditionally, and that is the capacity this work required; she gave literature,
culture, understanding, and a safe place to think and to try.
This paper is dedicated to Karla, who has struggled the most in understanding and
given the most in trying, and to Aristotle and Louise, to show them what being is, how
to live: that we are not ridiculous; that “a lot” is often exactly what is needed; and that
when the way things are is not the way they should be, and the way they should be is
not the way they are, it is your responsibility to do something about it, or lose yourself
to it.

35

## PDF page 36

A

Expanded Proofs

A.1

Proof of Proposition 5.3 (Graceful Degradation)

Proof. Let Ek be the true exogenous subspace and Ẽk the estimated subspace. Write
exo where δaint ∈ E ⊥ and δaexo ∈ E .
δak = δaint
k
k + δak
k
k
k

The estimated intrinsic component is ΠẼ ⊥ δak . If Ẽk ⊆ Ek (underestimation of the
k

exo
exogenous subspace), then Ek⊥ ⊆ Ẽk⊥ , so ΠẼ ⊥ retains all of δaint
k plus some of δak :
k

ΠẼ ⊥ δak ≥ δaint
= κtrue
k
γ [k].
k

int
The overestimate is ΠẼ ⊥ δaexo
≤ ∥δaexo
k
k ∥. Since δak

we have κint
γ [k] ≤ κγ [k].

A.2

k

2

2
2
2
+ ∥δaexo
k ∥ = ∥δak ∥ = κγ [k] ,

Proof of Proposition 9.2 (Classification of Dialectical Arcs)

Proof. We expand the three cases from the main text. Throughout, α(X) = ⟨Ja, ∇X a⟩
is the U(1) connection (42) built from the parallel complex structure J = Rℓ |K (Proposition 4.15); the naive real form ⟨a, ∇X a⟩ = 12 X∥a∥2 vanishes identically and carries no
phase, which is precisely why J is needed.
1
Case (i): κ¯γ = 0 implies θ(Γ) = 0. Since κγ (t) ≥ 0 and κ¯γ = |Γ|

H

κγ dt = 0, we

have κγ (t) = 0 a.e., so ∇γ̇ a = 0 a.e.: a is parallel along Γ. Then α = ⟨Ja, ∇γ̇ a⟩ = 0 a.e.,
giving θ(Γ) = 0.
Case (ii): κ¯γ > 0, θ(Γ) = 0. The hidden sector rotates but the net phase

H

α = 0 in

R/2πZ. The U(1) holonomy is trivial: a returns to its initial orientation in the complex
line span{a, Ja}. The arc explores the hidden sector and returns: displacement without
net turning.
Case (iii): κ¯γ > 0, θ(Γ) ̸= 0. The U(1) holonomy exp(i α) ̸= 1: the hidden
H

generator does not return, a(Γ(1)) and a(Γ(0)) differing by the nonzero rotation angle
θ(Γ) in span{a, Ja}. By Stokes, θ(Γ) =

RR

DF

∇|
u(1) for any disk D bounding Γ, so

a nonzero phase certifies nonzero enclosed curvature flux. Because Paph is simply
connected (π1 = 0), this is not homotopy-protected: Γ can be contracted and θ(Γ)
driven continuously to 0, the flux through the shrinking disk vanishing. The phase is a
quantitative record of the curvature the arc swept, not a discrete topological charge.

B

Conceptual Monitor: Pseudocode

Algorithm 1 summarizes the curvature monitor as an eight-step procedure. No implementationspecific details (data structures, memory layout, SIMD kernels, or language-specific
constructs) are exposed.
The monitor is passive: it observes the trajectory and classifies, but does not intervene.
Intervention policies (throttle, halt, rollback) are downstream of classification and outside
36

## PDF page 37

Algorithm 1: Curvature Monitor (Conceptual)
Input: Trajectory γ, action operator L, exogenous estimator Ê, verification
oracle V, thresholds (τκ , τV , vmin , Lconfirm )
Output: Regime sequence R0 , R1 , . . .
1 for each step k do
2
Step 1: Compute ak ← unit vector in ker(Lγ(k) );
3
Step 2: Compute raw curvature κγ [k] ← arccos(⟨ak−1 , ak ⟩);
4
Step 3: Estimate exogenous subspace Ek ← Ê(k);
5

Step 4: Subtract exogenous component: κint
γ [k] ← ΠE ⊥ (ak − ak−1 ) ;
k

Step 5: Compute verification weight Vk ← V(athesis
, asynth
);
k
k
7
Step 6: Compute phase transition score Φk ← ϱk · κint
[k];
γ
8
Step 7: Compute survival-gated score Cksurv ← κint
[k]
· Vk · σksurv ;
γ
surv ; τ , τ ) with
9
Step 8: Classify regime Rk ← Classify(κint
κ V
γ , Vk , Φk , Ck
Lconfirm -step hysteresis;
10 end
6

the scope of this paper.

C

The Basepoint Table

This appendix exhibits the explicit data underlying the proof of Theorem 4.13. All entries
are computed at p0 = e1 + e10 and verified at machine precision (maximum residual
0e + 00).

C.1

Canonical kernel basis

The Gram–Schmidt-orthonormalized output of compute_kernel [21] at p0 yields
v0 = √12 (e7 + e12 ), v1 = √12 (−e6 + e13 ),

(44)

v2 = √12 (e5 + e14 ), v3 = √12 (−e4 + e15 ).
These four vectors form an orthonormal basis of Kp0 ; Lp0 vk = 0 for k = 0, 1, 2, 3.

C.2

The four generators in the kernel basis

In the {v0 , v1 , v2 , v3 } basis, the four generators of F(p0 ) defined in (30) have the explicit
matrix forms


0 − 12


1

J = 2
0

1

0





0

0

− 12

0




0

J = 1

2

0

0

0

0

1
2 ,

0 − 21

0

0

0

0

0

0

0 


0 − 12 

1
0
2

0

2

,

37




0



0

(45)

## PDF page 38



0


0

J =
0

3

1
2

0

0

0 − 21
1
2

0

0

0

− 12





0

0

0 − 12




0

ω=
0


0

1
2

− 12

0

0

0

0 


,

0 

0

1
2




0 


.

0 


(46)

0

Each is skew-symmetric of Frobenius norm one. The triple {J 1 , J 2 , J 3 } exhibits the
standard su(2)+ action on R4 (self-dual sector of so(4)), and ω is skew-symmetric with
(2ω)2 = −I: that is, 2ω is a complex structure on Kp0 (not an involution: a nonzero
real skew matrix satisfies ω 2 ⪯ 0, so ω 2 = +I is impossible). Up to sign it is the
restriction Rℓ |Kp0 of right multiplication by the Cayley–Dickson doubling generator
(Proposition 4.15), and it commutes with the triple.

C.3

Decomposition of the nonzero curvature pairs

All 25 nonzero curvature operators Cei ,ej (p0 ) with 1 ≤ i < j ≤ 15 admit unique integer
decompositions
Cei ,ej (p0 ) = c1 J 1 + c2 J 2 + c3 J 3 + cω ω,

(c1 , c2 , c3 , cω ) ∈ Z4 .

Group I — within first octonion half (i, j ∈ {4, 5, 6, 7}):
(i, j)

c1

c2

c3

cω

∥C∥F

(e4 , e5 )
(e4 , e6 )
(e4 , e7 )
(e5 , e6 )
(e5 , e7 )
(e6 , e7 )

-2
+0
+0
+0
+0
-2

+0
-2
+0
+0
+2
+0

+0
+0
-2
-2
+0
+0

+0
+0
+0
+0
+0
+0

2.000
2.000
2.000
2.000
2.000
2.000

Group II — within second octonion half (i, j ∈ {12, 13, 14, 15}):
(i, j)

c1

c2

c3

cω

∥C∥F

(e12 , e13 )
(e12 , e14 )
(e12 , e15 )
(e13 , e14 )
(e13 , e15 )
(e14 , e15 )

-2
+0
+0
+0
+0
-2

+0
-2
+0
+0
+2
+0

+0
+0
-2
-2
+0
+0

+0
+0
+0
+0
+0
+0

2.000
2.000
2.000
2.000
2.000
2.000

Group III — cross-half adjacent mixers (i ∈ {4, 5, 6, 7}, j ∈ {12, 13, 14, 15}):

38

## PDF page 39

(i, j)

c1

c2

c3

cω

∥C∥F

(e4 , e12 )
(e4 , e13 )
(e4 , e14 )
(e5 , e12 )
(e5 , e13 )
(e5 , e15 )
(e6 , e12 )
(e6 , e14 )
(e6 , e15 )
(e7 , e13 )
(e7 , e14 )
(e7 , e15 )

+0
+0
-1
+0
+0
-1
-1
+0
+0
-1
+0
+0

+0
+1
+0
+1
+0
+0
+0
+0
-1
+0
-1
+0

-1
+0
+0
+0
+1
+0
+0
+1
+0
+0
+0
-1

+1
+0
+0
+0
+1
+0
+0
+1
+0
+0
+0
+1

1.414
1.000
1.000
1.000
1.414
1.000
1.000
1.414
1.000
1.000
1.000
1.414

Group IV — Fano cross-half (e3 , e11 ):

C.4

(i, j)

c1

c2

c3

cω

∥C∥F

(e3 , e11 )

+0

+0

+0

+1

1.000

Spectrum cross-check

From the table above, the 15 × 15 Gram matrix (ΓC )ij =

k ⟨Cei ,ek (p0 ), Cej ,ek (p0 )⟩F

P

can be reconstructed in closed form: each entry is a quadratic form in the integer
coefficients (c1 , c2 , c3 , cω ) with the orthonormality relations ⟨J a , J b ⟩F = δab , ⟨J a , ω⟩F = 0,
⟨ω, ω⟩F = 1. Direct evaluation gives the spectrum
Spec(ΓC ) =

 5 2 4
0 , 1 , 4 , 284 ,

(47)

matching (25). The five zero eigenvalues correspond to the five-dimensional Q-centralizer
qp0 = span{e1 , e2 , e8 , e9 , e10 }.
This completes the proof of Theorem 4.13: the table exhibits all 25 nonzero curvature
operators as integer combinations of the four-element generating set {J 1 , J 2 , J 3 , ω}, and
the linear independence of the generating set is witnessed directly by the matrix forms
(45).

References
[1] Shun-ichi Amari. Natural gradient works efficiently in learning. Neural Computation,
10(2):251–276, 1998. doi: 10.1162/089976698300017746.
[2] Shun-ichi Amari and Hiroshi Nagaoka. Methods of Information Geometry, volume
191 of Translations of Mathematical Monographs. American Mathematical Society,
2000. doi: 10.1090/mmono/191.
39

## PDF page 40

[3] Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion,
Andy Jones, Anna Chen, Anna Goldie, Azalia Mirhoseini, Cameron McKinnon, et al.
Constitutional AI: Harmlessness from AI feedback. arXiv preprint arXiv:2212.08073,
2022.
[4] Michael V. Berry. Quantal phase factors accompanying adiabatic changes. Proceedings of the Royal Society of London A, 392(1802):45–57, 1984. doi: 10.1098/rspa.
1984.0023.
[5] Margaret A. Boden. The Creative Mind: Myths and Mechanisms. Routledge, 2nd
edition, 2004.
[6] Michael M. Bronstein, Joan Bruna, Taco Cohen, and Petar Veličković. Geometric deep learning: Grids, groups, graphs, geodesics, and gauges. arXiv preprint
arXiv:2104.13478, 2021. arXiv:2104.13478.
[7] Gunnar Carlsson. Topology and data. Bulletin of the American Mathematical
Society, 46(2):255–308, 2009. doi: 10.1090/S0273-0979-09-01249-X.
[8] Taco Cohen and Max Welling. Group equivariant convolutional networks. In
Proceedings of the 33rd International Conference on Machine Learning (ICML),
pages 2990–2999, 2016.
[9] Phan Minh Dung. On the acceptability of arguments and its fundamental role
in nonmonotonic reasoning, logic programming and n-person games. Artificial
Intelligence, 77(2):321–357, 1995. doi: 10.1016/0004-3702(94)00041-X.
[10] Herbert Edelsbrunner and John Harer. Persistent homology—a survey. Contemporary Mathematics, 453:257–282, 2008.
[11] Karl Friston. The free-energy principle: A unified brain theory? Nature Reviews
Neuroscience, 11(2):127–138, 2010. doi: 10.1038/nrn2787.
[12] Geoffrey Irving, Paul Christiano, and Dario Amodei. AI safety via debate. arXiv
preprint arXiv:1805.00899, 2018.
[13] Tosio Kato. Perturbation Theory for Linear Operators. Springer-Verlag, 1966.
[14] Diederik P. Kingma and Max Welling. Auto-encoding variational Bayes. arXiv
preprint arXiv:1312.6114, 2014.
[15] James Martens. New insights and perspectives on the natural gradient method.
Journal of Machine Learning Research, 21(146):1–76, 2020.
[16] Gregory Naitzat, Andrey Zhitnikov, and Lek-Heng Lim. Topology of deep neural
networks. Journal of Machine Learning Research, 21(184):1–40, 2020.

40

## PDF page 41

[17] Bastian Rieck, Matteo Togninalli, Christian Bock, Michael Moor, Max Horn, Thomas
Gumbsch, and Karsten Borgwardt. Neural persistence: A complexity measure for
deep neural networks using algebraic topology. In International Conference on
Learning Representations (ICLR), 2019.
[18] Jürgen Schmidhuber. Formal theory of creativity, fun, and intrinsic motivation
(1990–2010). IEEE Transactions on Autonomous Mental Development, 2(3):230–247,
2010. doi: 10.1109/TAMD.2010.2056368.
[19] David Silver, Julian Schrittwieser, Karen Simonyan, Ioannis Antonoglou, Aja Huang,
Arthur Guez, Thomas Hubert, Lucas Baker, Matthew Lai, Adrian Bolton, et al.
Mastering the game of Go without human knowledge. Nature, 550(7676):354–359,
2017. doi: 10.1038/nature24270.
[20] Barry Simon. Holonomy, the quantum adiabatic theorem, and Berry’s phase. Physical
Review Letters, 51(24):2167–2170, 1983. doi: 10.1103/PhysRevLett.51.2167.
[21] Kyriakos John Skiouris. Algebraic hiddenness in the sedenion algebra: Characterization, spectral structure, and bundle topology. Zenodo, https://doi.org/10.5281/
zenodo.22016333, 2026.
[22] Gerard ’t Hooft. Computation of the quantum effects due to a four-dimensional
pseudoparticle. Physical Review D, 14:3432–3450, 1976.
[23] Maurice Weiler and Gabriele Cesa. General E(2)-equivariant steerable CNNs. In
Advances in Neural Information Processing Systems (NeurIPS), volume 32, 2019.
[24] Geraint A. Wiggins. A preliminary framework for description, analysis and comparison of creative systems. Knowledge-Based Systems, 19(7):449–458, 2006. doi:
10.1016/j.knosys.2006.04.009.
[25] Frank Wilczek and Anthony Zee. Appearance of gauge structure in simple dynamical
systems. Physical Review Letters, 52(24):2111–2114, 1984. doi: 10.1103/PhysRevLett.
52.2111.

41
