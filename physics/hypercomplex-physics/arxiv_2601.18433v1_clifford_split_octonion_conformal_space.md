Source: https://arxiv.org/abs/2601.18433v1
PDF sha256: 74111b6e4be468583efae99f8700c5f5427b50fd46e41945dd90a84175809289
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of arxiv_2601.18433v1_clifford_split_octonion_conformal_space.pdf

Transcription of `arxiv_2601.18433v1_clifford_split_octonion_conformal_space.pdf` in this directory, 162 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 2, 4, 8, 10, 13-14, 142, 153, 162 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1, 3, 5-7, 9, 11-12, 15-141, 143-152, 154-161 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

arXiv:2601.18433v1 [math-ph] 26 Jan 2026

Massless Representations in Conformal
Space and Their de Sitter (dS) Restrictions
The Split-Octonionic Fabric of Inflationary Field Dynamics

Jean-Pierre Gazeau
Université Paris Cité, CNRS, Astroparticule et Cosmologie, F-75013 Paris, France
and
Faculty of Mathematics, University of Białystok, 15-245 Białystok, Poland
gazeau@apc.in2p3.fr

Hamed Pejhan
Institute of Mathematics and Informatics, Bulgarian Academy of Sciences, Acad.
G. Bonchev Str. Bl. 8, 1113 Sofia, Bulgaria
pejhan@math.bas.bg

Ivan Todorov
INRNE, Bulgarian Academy of Sciences, Tsarigradsko Chaussee 72, BG-1784
Sofia, Bulgaria

Draft monograph / preprint. Submitted to arXiv and under consideration by
Cambridge University Press.

January 27, 2026

## PDF page 2



## PDF page 3

This monograph is dedicated to the memory
of Professor Ivan Todorov (1933-2025),
whose profound contributions to theoretical
and mathematical physics and invaluable
guidance were instrumental in shaping this
research. We deeply regret his passing on
February 14, 2025, during the preparation of
this work. Grounded in his insights and notes,
this study reflects his enduring impact on the
field. His legacy will continue to inspire
generations of physicists and mathematicians.

## PDF page 4



## PDF page 5

Preface

At the dawn of our Universe, during the inflationary epoch, spacetime underwent a
brief but dramatic burst of quasi-exponential expansion. In this extreme regime, all
quantum fields were effectively massless, and their dynamics were dictated by the
intertwined structures of de Sitter (dS) and conformal symmetries. These symmetries
constrained the primordial quantum fluctuations, which ultimately seeded the largescale structure of the cosmos we observe today. Understanding the mathematical
fabric of these massless (conformal) fields is therefore central not only to fundamental
physics but also to modern cosmology, shedding light on the quantum origin of
cosmic structures and the near-scale invariance of primordial perturbations.
“...as time goes on, it becomes increasingly evident that the rules which the mathematician
finds interesting are the same as those which Nature has chosen.”
— Paul Dirac (1939)

This profound insight from Paul Dirac perfectly encapsulates the spirit of this
volume, which explores the elegant mathematical structures underlying massless
elementary systems — “free” fields or particles — in dS spacetime. dS spacetime, the
maximally symmetric solution of Einstein’s equations with a positive cosmological
constant Λ, is a manifold of constant positive curvature that models an exponentially
expanding Universe and closely approximates the large-scale geometry of our present
cosmos.
This volume is part of a broader research program dedicated to developing a
mathematically rigorous, representation-theoretic framework for elementary systems
in dS spacetime. In line with Wigner’s fundamental principle — that quantum
elementary systems correspond to unitary irreducible representations (UIRs) of
the underlying spacetime symmetry group — quantum elementary systems in dS
spacetime are identified with (projective) UIRs of the dS relativity group SO0 (4, 1)
or its universal covering group Sp(2, 2)  Spin(4, 1). Wigner originally formulated
this classification within the flat Minkowski setting, where rest mass 𝑚 and spin 𝑠
of a system serve as the fundamental invariants labeling the corresponding UIR of
the Poincaré group ISL(2, C) — the relativity group of flat Minkowski spacetime.
Introducing a constant curvature into spacetime is the sole mechanism by which

vii

## PDF page 6

viii

Preface

Poincaré symmetry is deformed, giving rise to the dS and anti-dS symmetry groups;
in this curved context, the notion of mass is replaced by a curvature-dependent
energy parameter, while spin remains a discrete invariant.
Within this robust representation-theoretic framework, and building on concepts
developed in the earlier volume, The de Sitter (dS) group and its representations
(2nd ed., Springer, Cham, Switzerland, 2024), this work delves more deeply into
the mathematical structures underlying dS massless elementary systems. Fully selfcontained, it places particular emphasis on the interplay between massless conformal
representations and their restrictions to dS spacetime, with Clifford algebras serving
as a unifying algebraic framework throughout.
Beyond Wigner’s foundational framework, it has long been recognized that the
massless nature of elementary systems is intimately tied to deeper symmetry principles — most notably, conformal symmetry. At the heart of this symmetry lies
the conformal group U(2, 2) — the U(1)-extended form of SU(2, 2)  SO(4, 2)
— whose unitary representations encompass a rich variety of elementary systems.
Among these, the massless representations, commonly called ladder representations, form a distinguished subclass, ideally suited for describing physically relevant
massless systems. First studied by Mack and Todorov in the late 1960s, these representations exhibit the striking property of remaining irreducible when restricted
to the quantum-mechanical Poincaré subgroup ISL(2, C). In this limit, they yield
the well-known Poincaré massless representations, characterized by vanishing rest
mass and quantized helicity. These representations form the natural framework for
describing lightlike — or massless — elementary systems in Minkowski spacetime
and serve as a conceptual springboard for investigating their counterparts in more
general geometric settings.
This volume undertakes a detailed study of the restriction of massless (ladder)
conformal representations to dS spacetime. Specifically, it considers the embedding
of SO0 (4, 1) into the conformal group U(2, 2) via its universal covering Sp(2, 2).
Within this framework, we analyze the restriction of conformal ladder representations to dS symmetry, emphasizing the persistence of their irreducibility and its
implications for the structure of massless fields in curved geometries.
A defining feature of this work, which sets it apart from earlier studies, is the
use of Clifford algebras — specifically 𝔠𝔩(4, 2) — as the primary framework, rather
than U(2, 2) directly. Through a Clifford-split-octonion construction, 8-component
Majorana spinors are realized explicitly in a geometrically enriched form. Conceptually, this embeds spinorial degrees of freedom within an 8-dimensional composition
algebra governed by alternativity (via the Moufang identities). Left-multiplication
by split-octonion units yields coherent operators realizing the Majorana gamma matrices, fusing algebraic, spinorial, and geometric structures, and exposing a deep link
between spinor geometry and the underlying composition-algebraic structure.
Within this framework, the conformal Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) emerges
naturally from the commutators of bivectors in the even subalgebra 𝔠𝔩 even (4, 2) 
𝔠𝔩(4, 1), while the Clifford pseudoscalar generates the central 𝔲(1), producing the
full conformal Lie algebra 𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1). This construction provides
direct access to the full conformal group U(2, 2) entirely within the Clifford alge-

## PDF page 7

Preface

ix

bra, with exponentials of the Lie algebra elements — which generate the group —
admitting finite-series representations intrinsic to the Clifford framework. Likewise,
the formalism accommodates the dS Lie algebra 𝔰𝔬(4, 1) and its universal covering
group Sp(2, 2), so that all fundamental Lie group-theoretic operations — exponentiation, inversion, multiplication, and spinorial action — are performed entirely
within the Clifford framework, making computations both explicit and conceptually
transparent. Moreover, the split-octonion realization unifies spinorial and tensorial
representations, allowing the explicit construction of ladder operators, Casimir invariants, and invariant bilinear forms for massless fields of arbitrary helicity.
In short, by situating the spinors within the rich architecture of split-octonions,
the framework uncovers deep and previously hidden correspondences between
dS/conformal symmetries and alternative and exceptional algebraic structures, suggesting a conceptual unity underlying the organization of massless fields in curved
spacetime.
The methods developed here are designed to be both rigorous and accessible. Graduate students are guided step by step through the algebraic, geometric,
and representation-theoretic tools, while advanced researchers are provided with
concrete techniques and fresh perspectives for explicit computations and theoretical explorations. By integrating spinorial, tensorial, and group-theoretic structures
within a single algebraic setting, the monograph bridges multiple domains — from
higher-spin physics, conformal geometry, and quantum field theory (QFT) in curved
spacetimes, to string theory, holography, and cosmological modeling.
In this way, the work serves simultaneously as a pedagogical guide, a technical reference, and a conceptual resource. It clarifies how symmetry, curvature, and
algebraic structure converge in the theory of massless fields, and it highlights the
conceptual role of the split-octonion realization as a unifying structure that connects
spinorial geometry, algebraic formalism, and the representation theory of massless conformal systems, pointing toward new directions for both mathematical and
physical research.
Paris, France and Białystok, Poland
Sofia, Bulgaria
Sofia, Bulgaria

Jean-Pierre Gazeau
Hamed Pejhan
Ivan Todorov

## PDF page 8



## PDF page 9

Acknowledgements

The authors would like to express their sincere gratitude to Mrs. Boriana Todorov,
spouse and legal representative of the late Professor Ivan Todorov, for her understanding, support, and cooperation throughout the preparation of this monograph.
Her gracious assistance in facilitating the posthumous inclusion of Professor Todorov
as a co-author has been invaluable, and we deeply appreciate her encouragement and
kindness during this difficult period.
Hamed Pejhan is supported by:
1. The National Science Fund, Ministry of Education and Science of Bulgaria,
under contract KP-06-N92/2.
2. The Bulgarian Ministry of Education and Science, Scientific Programme “Enhancing the Research Capacity in Mathematical Sciences (PIKOM)”, No. DO167/05.05.2022.

xi

## PDF page 10



## PDF page 11

Contents

1

An Overview of Conformal Massless Elementary Systems and
Wigner’s Vision in de Sitter (dS) Geometry . . . . . . . . . . . . . . . . . . . . . . . 1
1.1 Conformal Symmetry in Historical Perspective and the Legacy of
Ivan Todorov . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1
1.2 Wigner’s (Massless) Elementary Systems: Continuity under
Curvature-Induced Deformations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4
1.2.1 Wigner’s Elementary Systems . . . . . . . . . . . . . . . . . . . . . . . . . 4
1.2.2 Wigner’s Massless Elementary Systems . . . . . . . . . . . . . . . . . 6
1.2.3 Wigner’s Theory in de Sitter (dS) Spacetime: From
Quantum Structure to Cosmological Dynamics . . . . . . . . . . . 6
1.2.4 Research Objectives . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 7
1.2.5 Layout, Main Notational Conventions, and Comprehensive
References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 9
1.3 Brief on de Sitter (dS) Relativity: Symmetry Group, Lie Algebra,
and Unitary Irreducible Representations (UIRs) . . . . . . . . . . . . . . . . . 13
1.3.1 Symmetry Group and Lie Algebra . . . . . . . . . . . . . . . . . . . . . . 14
1.3.2 Unitary Irreducible Representations (UIRs) . . . . . . . . . . . . . . 15

2

Majorana Representation of the Conformal Clifford Algebra
𝖈𝖑(4, 2) and its Chiral Counterpart . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.1 Composition Algebras, Cayley-Dickson Construction, and
Moufang Identities . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.1.1 Complex Numbers . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.1.2 Quaternions: Extending the Complex Numbers . . . . . . . . . . .
2.1.3 (Split) Octonions: Beyond Associativity . . . . . . . . . . . . . . . . .
2.2 Conformal Clifford Algebra 𝔠𝔩(4, 2) Generated by Left
Multiplication of Imaginary Split-Octonion Units . . . . . . . . . . . . . . . .
2.3 Diagonalizing the Complex Structure of 𝔠𝔩(4, 2) in Spinor Space:
Insight from the 𝔠𝔩(2) Case . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.3.1 The 𝔠𝔩(2) Case as a Prototype . . . . . . . . . . . . . . . . . . . . . . . . . .

19
20
23
23
25
29
35
39

xiii

## PDF page 12

xiv

Contents

2.4

Unitary Transformation from Real to a Diagonal Compact Cartan
Basis of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.4.1 Operator Transformation in the Majorana Basis . . . . . . . . . . .
2.4.2 Changing the Basis: From Majorana to Chiral . . . . . . . . . . . .
2.4.3 Adjustment of Notation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.5 Appendix: A Mnemonic Matrix Rule for (Split) Octonionic
Multiplication . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
2.6 Appendix: Realization( of the Conformal
Group
)
U(2, 2)  SU(2, 2)
 SO(4, 2) × U(1) in the
Clifford Algebra 𝔠𝔩(4, 2) and its Action on Spinors . . . . . . . . . . . . . . .
2.7 Appendix: Maximal Compact Subalgebra of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) . . .
2.8 Appendix: Diagonal Inner Products of Real Matrices Representing
Imaginary Split-Octonion Units . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

42
48
51
55
56

57
60
61

3

Ladder Representation of 𝖚(2, 2) as a Quantized 4-dimensional
Realization . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63
3.1 Invariant Bilinear Form in the Space of 𝔠𝔩(4, 2) Spinors . . . . . . . . . . 63
3.2 Isomorphism of 𝔠𝔩(4, 1) with the Even Part of 𝔠𝔩(4, 2): 4 × 4
Matrix Realization of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) . . . . . . . . . . . . . . . . . . . . . . 67
3.3 Positive Energy Ladder
Representations
of
(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩(4, 2)
Describing Massless Particles of Any Helicity . . . . . . . . . . . . . . . . . . 70
3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex
Algebra . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 101
3.4.1 Free Massless Scalar Field . . . . . . . . . . . . . . . . . . . . . . . . . . . . 108
3.5 4-dimensional Conformal Vertex Algebra . . . . . . . . . . . . . . . . . . . . . . 111
3.6 Appendix: Upper Bound on 𝔰𝔲(2) Spins from the 𝔰𝔬(4) Casimir . . . 119
3.7 Appendix: de Sitter (dS) Massless Unitary Irreducible
Representations (UIRs) . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 120
3.8 Appendix: Compactified Minkowski Space as a Shilov Boundary . . 122
3.9 Appendix: The Lie Algebra 𝔰𝔬(4, 2) and its Euclidean 𝔰𝔬(5, 1)
Counterpart; the 𝑧-Picture of the 𝔰𝔬(4, 2) Generators . . . . . . . . . . . . . 123

4

Conformal Massless Low Helicity Fields and their de Sitter (dS)
Spacetime Restriction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 129
4.1 Ladder Vertex Operator Construction of the Scalar Field . . . . . . . . . . 129
4.2 Conformal Massless Scalar Field in de Sitter (dS) Space . . . . . . . . . . 133
4.3 Appendix: On the Commutator (4.42) . . . . . . . . . . . . . . . . . . . . . . . . . 138
References . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 140

Glossary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 145
Index . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 147

## PDF page 13

<b>Acronyms</b>
<b>CFT</b> Conformal Field Theory
dS de Sitter
EdS Euclidean de Sitter
IR Irreducible Representation
<b>QFT</b> Quantum Field Theory
<b>UIR</b> Unitary Irreducible Representation
<b>UPEIR</b> Unitary Positive Energy Irreducible Representation
<math>\mathbf{x}\mathbf{v}</math>

## PDF page 14



## PDF page 15

Chapter 1

An Overview of Conformal Massless Elementary
Systems and Wigner’s Vision in de Sitter (dS)
Geometry

Abstract This chapter sets the stage for the monograph by outlining its central
motivations, thematic scope, and methodological framework. It places the study of
conformal massless elementary systems — “free” fields or particles — within both a
historical and conceptual context, tracing the influence of Ivan Todorov’s pioneering
work and the enduring significance of Wigner’s principles for the classification of
elementary systems. By emphasizing the interplay between representation theory,
conformal invariance, and the geometry of de Sitter (dS) spacetime, the chapter
provides a conceptual roadmap for analyzing massless elementary systems in cosmologically significant settings. It also establishes key conventions and notational
standards, ensuring consistency throughout the text. Serving as both an introduction and a conceptual guide, this chapter prepares readers for the deeper algebraic,
geometric, and physical developments in the subsequent chapters.

1.1 Conformal Symmetry in Historical Perspective and the
Legacy of Ivan Todorov
Conformal symmetry — the invariance of physical systems under transformations
that preserve angles while not necessarily preserving distances — has occupied a
foundational role in the development of theoretical physics. Its conceptual origins
trace back to the early twentieth century, when mathematicians and physicists began the systematic study of transformations preserving local geometric structures,
thereby establishing the algebraic and geometric groundwork for modern symmetry
principles in both quantum field theory (QFT) and relativity. The recognition that
geometry can enforce structural constraints on physical laws elevated symmetry to
the status of a unifying paradigm across diverse domains of physics.
In the 1930s, Cartan’s pioneering work [1] on differential geometry provided a
rigorous framework for analyzing symmetries on curved manifolds, introducing concepts such as torsion, curvature, and moving frames. While Cartan did not explicitly
formulate conformal symmetry in physics, his formalism later supplied essential ge1

## PDF page 16

1 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry
2

ometric and algebraic machinery for its systematic study. Concurrently, Weyl’s 1918
proposal [2] of scale invariance, further developed during the 1920s and 1930s, highlighted the profound interplay between geometry and physical law, foreshadowing
the systematic consideration of local angle-preserving and scale transformations in
theoretical physics.
By the 1950s and early 1960s, the mathematical study of unitary representations
of Lie groups, particularly the Poincaré group, had been advanced through the foundational work of Wigner, who classified elementary particles as unitary irreducible
representations (UIRs) of spacetime symmetries [3], and by Newton and Wigner’s
analysis of relativistic localization [4]. Further progress was made by V. Bargmann in
his classification of Lorentz group representations [5], and by Gel’fand and Naimark
in their systematic treatment of representations of classical groups [6]. Building on
these foundations, mathematicians such as Segal [7] and Mackey [8] developed the
theory of induced representations and harmonic analysis on groups, while HarishChandra [9] established the general representation theory of semisimple Lie groups.
These developments clarified the classification of massive and Poincaré massless
representations — including helicity states and the more exotic continuous-spin
cases — and provided representation-theoretic tools that were later extended to
larger symmetry groups, notably the conformal group, as in the rigorous treatment
by Gel’fand, Minlos, and Shapiro [10] and later in the field-theoretic constructions
of Mack and Salam [11].
Building on algebraic and representation-theoretic foundations, Fronsdal’s seminal 1978 work [12] provided a systematic formulation of free massless higherspin fields in a Poincaré-invariant framework. His construction introduced the nowstandard gauge-invariant Fronsdal equations, giving consistent field equations for
totally symmetric particles of arbitrary spin. Although originally formulated in flat
spacetime, this framework laid the foundation for later developments that extended
higher-spin fields to (anti-)dS backgrounds and to conformal higher-spin theories.
These advances were part of a broader trend in the 1970s and 1980s in which conformal symmetry emerged as a unifying principle across diverse areas of theoretical
physics, including conformal field theory (CFT), string theory, the study of critical
phenomena in statistical mechanics, and higher-spin gauge theories.
As this conceptual and algebraic framework took shape, the late 1960s marked a
pivotal phase in the study of conformal symmetry, featuring one of the first systematic
investigations of massless representations and the introduction of ladder representations of the conformal group [13]. Spearheaded by the landmark collaboration
between Gerhard Mack and Ivan Todorov, this program demonstrated how Poincaré
massless representations could be consistently extended to the conformal group.
The resulting algebraic framework provided a mathematically rigorous characterization of massless elementary systems and established a bridge between conventional
flat-space QFT and its conformally extended formulations. This formalism subsequently became foundational for the precise treatment of massless quantum fields in
both Minkowski and curved spacetimes, underpinning later developments in CFT,
higher-spin theories, and the study of critical phenomena in statistical mechanics.

## PDF page 17

1.1 Conformal Symmetry in Historical Perspective and the Legacy of Ivan Todorov

3

It was within this evolving historical landscape that Ivan Todorov (1933-2025)
emerged as a leading figure whose contributions bridged the realms of rigorous
mathematics and theoretical physics. Born in Sofia, Todorov earned his MSc in
Physics from Sofia University in 1956. He then pursued his PhD at the Joint Institute
for Nuclear Research (JINR) in Dubna, completing his thesis in 1960 under the
supervision of the renowned theoretical physicist Nikolai N. Bogoliubov [14, 15].
His early research at JINR and at the Institute for Advanced Study in Princeton laid
the foundation for his seminal contributions. Todorov advanced the axiomatic and
algebraic foundations of QFT and developed a mathematically precise understanding
of CFTs, making the ladder representation program and its applications in conformal
symmetry a central part of his lasting legacy.

Fig. 1.1 Professor Ivan Todorov (1933-2025), whose pioneering contributions to CFT, ladder
representations, and massless quantum systems profoundly shaped mathematical physics.

Beyond his seminal collaboration with Nikolaj N. Bogoliubov and Gerhard Mack,
Todorov worked with distinguished scientists such as Valentine Bargmann, Louis
Michel, Claude Itzykson, and Victor Kac, thereby enriching the theoretical understanding of symmetries and advancing the dialogue between algebraic structures
and physical intuition [16]. Throughout his career, he consistently emphasized the
foundational role of group-theoretical methods, forging deep connections between
Lie algebra representations, conformal transformations, and the structural analysis
of QFT. His extensive body of work includes influential monographs, most notably
General principles of quantum field theory [17], Introduction to axiomatic quantum
field theory [18], and Harmonic analysis: on the 𝑛-dimensional Lorentz group and
its application to conformal quantum field theory [19], co-authored with N.N. Bogoliubov and collaborators, which remain indispensable references for researchers.
Equally significant were Todorov’s integrity, his dedication to mentorship, and his
sustained efforts to foster international collaboration. He played a leading role in
organizing conferences and advanced schools that brought together Eastern and
Western physicists during politically challenging times, thereby strengthening the
global community of mathematical physics [20].

## PDF page 18

1 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry
4

This monograph is dedicated to the memory of Professor Ivan Todorov, whose
profound contributions and guidance were instrumental in shaping this work. Drawing extensively on his insights, notes, and foundational studies, it reflects his enduring
impact on the field. Todorov’s legacy continues to inspire generations of physicists
and mathematicians, exemplifying the integration of rigorous mathematics with deep
physical understanding that he championed throughout his career.

1.2 Wigner’s (Massless) Elementary Systems: Continuity under
Curvature-Induced Deformations
In modern theories of elementary systems — whether field-theoretic or phenomenological — their formulation, and in particular their interpretation, fundamentally rely
on the concepts of energy, momentum, mass, and spin, which emerge from invariance under the Poincaré group, the relativity group of flat Minkowski spacetime. It
is, however, widely acknowledged that such theories cannot ultimately rest solely
on this symmetry. A fully consistent framework must respect the broader principle
of general covariance, reflecting Einstein’s vision of spacetime as a Riemannian
manifold.
Beyond the familiar flat Minkowski setting, the absence of nontrivial motion
groups in generic curved backgrounds makes the direct extension of these fundamental notions highly nontrivial, if not impossible. In this context, the common
suggestion to merely generalize fundamental equations — such as the Klein-Gordon
or Dirac equations — to fully covariant forms misses the deeper issue; it addresses
only the formal structure, not the conceptual foundation. Indeed, modern theories of
elementary systems are not primarily concerned with differential equations per se,
but with the deeper symmetry principles that underlie them.
This is precisely where Wigner’s principle — particularly, its remarkable continuity under curvature-induced deformations — proves essential, providing a robust and
conceptually coherent framework for extending the classification and understanding
of elementary systems from flat Minkowski spacetime to curved dS and anti-dS
spacetimes.

1.2.1 Wigner’s Elementary Systems
In the field-theoretic formulation of elementary systems, the foundational works of
Eugene Wigner [3, 4] established that the principles of special relativity impose
symmetry requirements on the laws of nature — most notably, invariance under the
Poincaré group in flat Minkowski spacetime.
Within the flat Minkowski framework, quantum elementary systems are identified with (projective) UIRs of the Poincaré group (or one of its coverings) [3, 4].
Each such representation is uniquely characterized by two invariant quantities: the

## PDF page 19

1.2 Wigner’s (Massless) Elementary Systems: Continuity under Curvature-Induced Deformations
5

rest mass 𝑚 and the spin 𝑠 of the system. These invariants not only encode the
system’s fundamental physical properties but also reflect the symmetry structure of
the underlying Minkowski spacetime.
Remarkably, introducing a constant curvature into spacetime yields the unique
natural and continuous deformation of Poincaré symmetry group. This deformation
gives rise to the dS and anti-dS groups of motion. The corresponding dS and antidS spacetimes [21, 22] — maximally symmetric solutions of Einstein’s equations
with, respectively, positive and negative cosmological constant Λ — thereby acquire
a privileged status as the only curved backgrounds in which Wigner’s symmetrybased definition of elementary systems admits a meaningful generalization. In these
settings, elementary systems are once again described by UIRs of the relevant spacetime symmetry groups. As in the flat case, these representations are classified by two
invariants — the spin and a characteristic mass or energy scale — thus preserving
the core structural features of Wigner’s original framework.

Fig. 1.2 Schematic illustration of the relationships among the Poincaré, de Sitter (dS), and anti-de
Sitter (anti-dS) groups as subgroups of the conformal group. Both dS and anti-dS groups contract
to the Poincaré group in the flat (zero-curvature) limit Λ → 0. Conversely, for nonzero curvature,
the dS and AdS groups can be regarded as deformations of the Poincaré group. The conformal
group provides a unifying framework encompassing all three.

## PDF page 20

1 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry
6

1.2.2 Wigner’s Massless Elementary Systems
Beyond Wigner’s foundational framework, it has long been established that the
massless nature of elementary systems is intimately connected to deeper symmetry
principles — most notably, conformal symmetry [12, 13, 23, 24, 25]. This symmetry
is not merely auxiliary structures but constitutes intrinsic aspects of massless field
dynamics, manifesting both at the level of representation theory and in the behavior
of field equations under spacetime transformations.
In the flat Minkowski setting, massless elementary systems correspond to UIRs of
the Poincaré group with vanishing mass and discrete helicity — commonly referred
to as Poincaré massless representations. A result of fundamental significance, due to
Mack and Todorov [13, 25], establishes that each such representation admits a unique
extension to a UIR of the conformal group SU(2, 2)  SO(4, 2), or more generally
its U(1)-extended form U(2, 2); these conformal UIRs are commonly called ladder
representations. This framework furnishes a canonical and rigorous link between
masslessness and conformal symmetry, so that any quantum system realizing a
Poincaré massless representation necessarily carries a well-defined conformal action.
A parallel and equally deep structure is present in constant-curvature spacetimes.
In dS and anti-dS geometries, the natural analogues of Poincaré massless representations are those UIRs of the respective symmetry groups whose unique conformal
extensions are massless (ladder) representations. In representation-theoretic terms,
these conformal extensions match the conformal extensions obtained from the massless Poincaré side, meaning that:
The massless ⇐⇒ conformal correspondence
survives passage from flat spacetime to dS and anti-dS backgrounds,
the only difference being that in dS the energy sign is undefined,
while in anti-dS helicity is ambiguous.

1.2.3 Wigner’s Theory in de Sitter (dS) Spacetime: From Quantum
Structure to Cosmological Dynamics
This work focuses on massless (ladder) representations in conformal space, and in
particular on their restriction to 3 + 1-dimensional dS spacetime, whose symmetry
structure governs both the earliest [26] and asymptotic [27, 28] stages of cosmic evolution. During the inflationary epoch (≈ 10−36 to 10−32 seconds after the Big Bang),
when the Universe underwent rapid quasi-exponential expansion, the Hubble scale
vastly exceeded all intrinsic mass scales, rendering all elementary systems effectively
massless. In this regime, dS symmetry together with conformal symmetry provides
the natural framework for their consistent description. Inflationary (massless) elementary systems are realized through ladder representations of the conformal group
U(2, 2), which, upon restriction to the dS subgroup Sp(2, 2), rigorously encode the

## PDF page 21

1.2 Wigner’s (Massless) Elementary Systems: Continuity under Curvature-Induced Deformations
7

quantum degrees of freedom of these fields. This representation-theoretic structure
underlies the near-scale invariance of primordial fluctuations that seeded cosmic
structure and, more generally, furnishes a canonical, symmetry-based classification
of inflationary quantum states via UIRs.
Moreover, at late times, observations of distant Type Ia supernovae [27, 28]
reveal that the Universe is accelerating, a phenomenon attributed to “dark energy”.
A small, positive cosmological constant Λ naturally models this acceleration, making
dS geometry both the vacuum state and the asymptotic attractor of the Universe.
Accordingly, dS spacetime remains a central arena for QFT in curved backgrounds, offering deep insights at the interface of quantum physics, gravity, and
cosmology. Across both early- and late-time cosmology, massless systems governed by conformal symmetry form a unifying thread. Ladder representations of
U(2, 2) provide a coherent and mathematically precise description of massless field
dynamics, encompassing both the inflationary quantum fluctuations that seeded cosmic structure and the behavior of fields in the late-time accelerated Universe. This
representation-theoretic framework thus directly links quantum symmetries to observable cosmological phenomena, highlighting their continuous and fundamental
role throughout cosmic evolution.

1.2.4 Research Objectives
Motivated by the considerations described above, this monograph forms part of a
broader program (see Ref. [29] and references therein) to develop a mathematically
rigorous, representation-theoretic account of elementary systems in dS spacetime
grounded in Wigner’s principle. The present work concentrates on the conceptually
rich realm of massless elementary systems in dS spacetime and their intimate relation to conformal symmetry. Although the embedding SO0 (4, 1) ↩→ U(2, 2) (via
the covering Sp(2, 2)) is well known, the representation-theoretic and physical consequences of this embedding — particularly for massless (ladder) representations —
deserve a focused, algebraically explicit treatment.
Rather than remaining solely within an abstract group framework based on U(2, 2)
(as already studied in Ref. [13]), this study adopts the conformal Clifford algebra
𝔠𝔩(4, 2) as the primary algebraic language. Far beyond a mere change of notation,
the Clifford framework provides concrete spinorial and geometric tools, sharpening
both conceptual understanding and practical computations. Concretely, we construct
an explicit real-matrix representation of 𝔠𝔩(4, 2) on 8-component Majorana spinors
via an embedding rooted in the alternative composition split-octonion algebra.
Interpreting the 8 split-octonion units as left-regular multiplication operators on
the split-octonion space produces an algebra of linear endomorphisms naturally
realized as 8 × 8 real matrices. By virtue of alternativity — encapsulated by the
Moufang identities — left multiplication by a suitably chosen set of 6 of the 8 splitoctonion units yields a coherent and internally consistent system of operators which
furnishes a realization of the 8-component Majorana gamma matrices associated with

## PDF page 22

1 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry
8

𝔠𝔩(4, 2). Since composition of endomorphisms is strictly associative, the Clifford
relations are faithfully reproduced in this setting, and one thereby obtains a canonical
associative matrix representation of 𝔠𝔩(4, 2). The resulting embedding, however, is
not an algebra homomorphism in the strict sense; in general, 𝐿 𝐴𝐵 ≠ 𝐿 𝐴 𝐿 𝐵 , reflecting
the intrinsic nonassociativity of the underlying octonionic product.
This is indeed a deliberate, conceptual choice. The alternative split-octonionic
embedding preserves the intrinsic multiplicative relations of the composition algebra while furnishing a geometrically natural — and strikingly economical — route
to the real gamma matrices and spinor multiplications employed throughout this
work. More than a mere calculational convenience, the construction unifies algebraic, spinorial, and geometric structures into a single framework, directly tying the
spinorial degrees of freedom to the deeper architecture of the composition algebra.
This split-octonionic realization also furnishes a unified framework in which
both the conformal and dS Lie algebras, together with their groups, are embedded
explicitly within 𝔠𝔩(4, 2). The conformal algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) arises from
commutators of bivectors in the even subalgebra 𝔠𝔩 even (4, 2)  𝔠𝔩(4, 1), and the
Clifford pseudoscalar generates the central 𝔲(1), yielding the full conformal Lie
algebra 𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1). On the other hand, exponentiating these generators produces invertible group elements of U(2, 2). Similarly, the dS Lie algebra
𝔰𝔬(4, 1) appears as a subalgebra whose exponentials generate elements of Sp(2, 2).
Since the exponential power series converges within the finite-dimensional Clifford
algebra and, for bivectors, reduces to closed ‘cos/sin’ or ‘cosh/sinh’ forms, every
group operation — including multiplication, inversion, and action on spinors —
occurs entirely within the Clifford framework. This structure provides an explicit,
efficient, and fully representation-theoretic platform for computing invariant bilinear
forms, ladder operators, spectra, and other quantities, keeping both conformal and
dS symmetries manifest and fully intertwined, with the conformal structure realized
in a way that is simultaneously algebraic and spinorial. Moreover, 𝔠𝔩(4, 2) naturally
accommodates both spinorial and tensorial representations, so the same algebraic
machinery describes fields of arbitrary helicity. This unification simplifies the construction of ladder representations and the explicit realization of their restrictions to
dS symmetry.
In short, by grounding the spinorial construction in the rich structure of splitoctonions, the framework furnishes a unified, explicit, and computationally powerful toolbox for the study of massless conformal systems. At the same time, it points
toward deeper algebraic connections — notably to alternative and exceptional structures — that may underlie the organization of massless fields in curved spacetime.
In this context, the concrete objectives of the project are therefore:
1. To construct an explicit Majorana representation of 𝔠𝔩(4, 2) on 8-component
spinors using the split-octonion algebra — naturally embedding the full conformal Lie algebra 𝔲(2, 2) — and relating it to the chiral basis; the Majorana (real)
basis and the chiral basis are two distinct realizations of the same real Clifford
algebra, requiring no complexification.
2. To construct and classify massless ladder (positive-energy) representations of
U(2, 2) using the explicit Majorana-split-octonionic realization of 𝔠𝔩(4, 2).

## PDF page 23

1.2 Wigner’s (Massless) Elementary Systems: Continuity under Curvature-Induced Deformations
9

3. To analyze the restriction of these representations to the dS group Sp(2, 2) 
SO0 (4, 1), demonstrating the continuity of Wigner-type classification under
curvature and computing invariant structures such as Casimirs, bilinear forms,
and lowest-weight data.

1.2.5 Layout, Main Notational Conventions, and Comprehensive
References
1.2.5.1 Layout
To achieve our goal, the remainder of this monograph is organized as follows:
1. The remainder of this chapter offers a concise overview of dS relativity, including
the dS group and its manifold, the corresponding Lie algebra, and the quantum
framework formulated in terms of dS UIRs.
2. Chap. 2 constructs an explicit Majorana representation of the conformal Clifford
algebra 𝔠𝔩(4, 2) using split-octonions, providing a geometrically transparent
framework for the internal symmetries of the conformal Lie algebra 𝔲(2, 2):
(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩(4, 2) .
It introduces a unitary transformation to the chiral basis, in which the Cartan
elements of the maximal compact subalgebra of 𝔰𝔲(2, 2) are diagonal simultaneously with the 𝔲(1) generator defined by the 𝔠𝔩(4, 2) volume form, and
systematically derives inner-product relations among matrices. These results
provide a coherent, geometrically grounded framework for the study of massless
conformal systems in flat Minkowski spacetime as well as in curved dS and
anti-dS spacetimes.
3. Chap. 3 develops a rigorous framework for positive-energy ladder representations of the conformal Lie algebra 𝔲(2, 2), realized as quantized models of
massless fields with arbitrary helicity in 4-dimensional Minkowski, dS, and
anti-dS spacetimes. The construction is based on an invariant bilinear form on
the Majorana-spinor space of 𝔠𝔩(4, 2) and an explicit 4 × 4 spinorial matrix
realization arising from the isomorphism 𝔠𝔩 even (4, 2)  𝔠𝔩(4, 1), providing a
concrete geometric and computational foundation for conformal symmetry, ladder operators, and spectral analysis. The resulting lowest-weight representations
are classified by conformal energy and helicity, remain irreducible upon restriction to the dS subalgebra 𝔰𝔭(2, 2)  𝔰𝔬(4, 1), and admit an embedding into
4-dimensional conformal vertex algebras that exposes their analytic structure,
Casimir invariants, and a unified treatment of massless conformal systems in
both flat and curved settings.
4. Chap. 4 constructs low-helicity conformal massless fields, focusing on the zerohelicity case in dS spacetime. Massless scalar fields are formulated via laddertype vertex operators with Bose operators and zero modes, ensuring correct

## PDF page 24

10 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry

lowest-energy states and canonical two-point function, with analytic properties
established in a precompact tube domain. The construction restricts fields from
6-dimensional conformal space to 4-dimensional dS spacetime using homogeneous light-cone functions, capturing gauge freedom and relating Euclidean
and Minkowski-type coordinates via Weyl rescaling. The conformally invariant
6-dimensional two-point function then projects onto dS spacetime, reproducing
the standard massless scalar two-point function.

Fig. 1.3 Nested hierarchy of algebraic structures illustrating the relationships among Clifford and
Lie algebras relevant to the conformal and spin groups in signature (4, 2). The full Clifford algebra
𝔠𝔩 (4, 2) contains its even subalgebra 𝔠𝔩 even (4, 2)  𝔠𝔩 (4, 1), which in turn includes the Lie algebra
𝔲 (2, 2)  𝔰𝔲 (2, 2) ⊕ 𝔲 (1). The special unitary algebra 𝔰𝔲 (2, 2) is isomorphic to the conformal
algebra 𝔰𝔬 (4, 2) and contains the dS subalgebra 𝔰𝔭(2, 2)  𝔰𝔬 (4, 1).

1.2.5.2 Main Notational Conventions
Our main notational conventions are:
1. Throughout this monograph, we adopt natural units by setting 𝑐 = ℏ = 1, where
𝑐 denotes the speed of light and ℏ the Planck constant.
2. We use the symbol ‘1’ to denote the identity element within the relevant algebraic framework. In composition algebras, it represents the distinguished unit
element that preserves the norm under multiplication; for complex numbers,
quaternions, and (split) octonions, ‘1’ indicates the multiplicative identity. In
matrix representations, it corresponds to the identity matrix of the appropriate
dimension, with indices added when necessary for clarity. In Clifford algebras,
‘1’ serves as the unit element, ensuring closure under multiplication. The precise
interpretation of ‘1’ depends on the specific context in which it appears.

## PDF page 25

1.2 Wigner’s (Massless) Elementary Systems: Continuity under Curvature-Induced Deformations
11

3. We use the ‘ ’ symbol to denote the complex conjugate, while ‘∗ ’ denotes
quaternionic or octonionic conjugation and, depending on context — particularly
in matrix representations — also the Hermitian conjugate; for a matrix 𝔐, one
has:
( )⊤
𝔐∗ = 𝔐 ,
where ‘⊤ ’ denotes transposition.
4. We adopt the following conventions for the split-octonion units and their associated indices:
a. The set of split-octonion units is denoted by:
𝐴 and/or 𝐵 = 1 , 𝒌 , 𝚤 , 𝚥 , ℓ𝚤 , 𝚥ℓ , ℓ𝒌 , ℓ .
b. The subset:
𝜈 and/or 𝜇 = 𝚤 , 𝚥 , ℓ𝚤 , 𝚥ℓ , ℓ𝒌 , ℓ .

(1.1)

It must be emphasized, however, that the symbols 𝐴, 𝐵 (and hence the
indices 𝜈, 𝜇) have a dual interpretation depending on context. They may
represent actual split-octonion units in the algebra, or serve merely as labels or indices for the corresponding operators or matrix representations
(𝐿 𝐴, 𝑆 𝐴𝐵 , 𝐸 𝐴𝐵 , 𝐷 𝐴𝐵 , 1 𝐴𝐵 , 𝑚 𝜇 , 𝑚 𝜇𝜈 , Γ𝜇 , Γ𝜇𝜈 , 𝛾 𝜇 , 𝛾 𝜇𝜈 , . . . ), with no octonionic meaning. In the latter case, whenever it aids readability without compromising clarity, we adopt a streamlined notation by representing the indices 𝜈
and/or 𝜇, respectively, as:
𝜈 and/or 𝜇 = 0 (:= 𝚤) ,

5 (:= 𝚥) ,

1 (:= ℓ𝚤) ,

2 (:= 𝚥ℓ) ,

3 (:= ℓ𝒌) ,

4 (:= ℓ) .

We denote any subset of indices 𝜈 and/or 𝜇, typically 1, 2, 3, 4, by 𝑖, 𝑗. Nevertheless, each symbol should be interpreted according to its context. This dual
interpretation is discussed in Sect. 2.2, Eqs. (2.60)-(2.62).
5. In the context of the chiral representation, we denote:
𝑎 ± and/or 𝑏 ± = 1ˆ𝒌 ± , ˆ
05± , ˆ
12± , ˆ
34± .
For clarity and conciseness, we shall, where appropriate, employ a simplified
numeric labeling in Chaps. 3 and 4 as:
(
)
𝑎 := 𝑎 + = 1 := 1ˆ𝒌 + ,

(
)
2 := ˆ
05+ ,

(
)
3 := ˆ
12+ ,

(
)
4 := ˆ
34+ .

Note that 𝑎, 𝑏 have a fundamentally different meaning from 𝑖, 𝑗.
6. We denote indices 0, 1, 2, 3, 4 by Greek letters 𝛼, 𝛽, . . . , and indices 0, 1, 2, 3 by
dotted letters ¤
𝜇, ¤𝜈, . . . .

## PDF page 26

12 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry

7. The framework of this monograph rests on the mostly positive metric signature,
which will serve as our convention from the outset.
8. Throughout this monograph, the symbol ‘’ denotes an isomorphism (or homomorphism) between algebras or groups. By a slight abuse of notation, the
same symbol is also used to indicate a homeomorphism or continuous homomorphism between groups or topological spaces. Whenever the precise nature
of the correspondence is relevant, it will be explicitly stated in the text.
9. In this monograph, various operators are represented as block-diagonal matrices
assembled from finite-dimensional matrix blocks (typically 2 × 2 or 4 × 4). To
describe such objects unambiguously, we use the following notation:
a. Direct-sum notation: For any ordered list of matrices (𝑀1 , 𝑀2 , . . . , 𝑀𝑛 ),
we write:
⨁(
)
𝑀1 + 𝑀2 + · · · + 𝑀𝑛 := 𝑀1 ⊕ 𝑀2 ⊕ · · · ⊕ 𝑀𝑛 ,
(1.2)
for the block-diagonal matrix whose diagonal blocks, in the order listed, are
𝑀1 , 𝑀2 , . . . , 𝑀𝑛 . For example:

⨁(

𝑀1 + 𝑀2 + 𝑀3 + 𝑀4

)

𝑀1 0 0 0
©
ª
­ 0 𝑀2 0 0 ®
=®.
­ 0 0 𝑀3 0 ®
« 0 0 0 𝑀4 ¬

(1.3)

A minus sign in the list indicates
⨁ ( literal multiplication of
) the corresponding
block by −1; for instance,
𝑀1 − 𝑀2 + 𝑀3 + 𝑀4 places −𝑀2 in the
second block. This convention allows expressions such as:
⨁(
)
(1.4)
𝑆1 ( 𝚥ℓ) + 𝑆 𝚥 ℓ − 𝑆𝚤 (ℓ𝒌 ) + 𝑆𝒌 (ℓ𝚤)
to be written compactly and without ambiguity.
b. Commutativity up to isomorphism: For finite-dimensional matrices 𝑀 and
𝑁, the direct sum is not strictly commutative as a matrix identity. The two
block arrangements differ only by a permutation of components, so that:
⨁(
⨁(
)
)
𝑀 + 𝑁 := 𝑀 ⊕ 𝑁  𝑁 ⊕ 𝑀 =:
𝑁+𝑀 ,
(1.5)
where “” denotes isomorphism via conjugation by an appropriate permutation matrix.
In the present context, however, the blocks are arranged such that their order
does not affect the resulting operator. That is, for the matrices considered
here, the direct sum is literally commutative:
⨁(
⨁(
)
)
𝑀 + 𝑁 := 𝑀 ⊕ 𝑁 = 𝑁 ⊕ 𝑀 =:
𝑁+𝑀 .
(1.6)
and blocks may be reordered freely without changing the outcome.

## PDF page 27

1.3 Brief on de Sitter (dS) Relativity: Symmetry Group, Lie Algebra, and Unitary Irreducible Representations (UIRs)
13

1.2.5.3 Comprehensive List of References
We conclude this section with a comprehensive list of references pertinent to the
discussion above:
1. For extensions of Wigner’s seminal idea to Galilean systems, see Inönü [30],
Lévy-Leblond [31], and Voisin [32]. Subsequent extensions to dS and anti-dS
systems were developed by Gürsey [33] and Fronsdal [34, 35], respectively.
More recent studies in this context include [29, 36, 37].
2. For the classification of all ten possible relativities connected via three types of
contraction, based on symmetry principles and physically motivated assumptions — namely, isotropy of space, parity and time-reversal as group automorphisms, and noncompactness of boosts — see Ref. [38] by Bacry and LévyLeblond. In Ref. [39], emphasizing abstract group-theoretic methods, these results were rigorously established through inverse contraction, i.e., deformation.
3. For the notion of “masslessness” and its interplay with conformal symmetry,
see, in addition to the references cited above, Refs. [40, 41, 42, 43, 44, 45,
46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64], which
provide further details and, in particular, elucidate the structure in dS and anti-dS
spacetimes.
4. For the pivotal role of dS spacetime in the formulation of consistent QFTs in
curved backgrounds, as well as its fundamental significance for quantum gravity
and cosmology, providing a natural laboratory for exploring horizon effects,
vacuum structure, and semiclassical phenomena, see Refs. [65, 66, 67, 68, 69,
70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81].
5. For a deeper understanding of composition algebras — including the (split)octonion algebra — encompassing their structural properties, classification,
and broad range of applications in mathematics and theoretical physics, particularly in connection with division algebras, spinor constructions, and symmetry
structures, the reader is referred to Refs. [82, 83, 84, 85, 86, 87, 88, 89].
6. A rigorous treatment of free quantum fields and their vacuum two-point functions is developed in the work of Segal; see in particular Ref. [90]. Analytic and
harmonic perspectives related to tube-domain realizations and the kernel structures underlying two-point correlators can be found in the monograph of Hua
[91]. Connections between representation theory and analytic function theory
on symmetric spaces, which provide a broader geometric framework for such
correlation functions, are explored in the seminal work of Piatetski-Shapiro [92].

1.3 Brief on de Sitter (dS) Relativity: Symmetry Group, Lie
Algebra, and Unitary Irreducible Representations (UIRs)
For future reference and to ensure internal consistency, this section provides a concise
overview of dS relativity, covering the dS group and its manifold, the corresponding

## PDF page 28

14 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry

Lie algebra, and their quantum counterparts — the dS UIRs that characterize elementary systems in dS spacetime. For a more comprehensive and detailed treatment,
readers are directed to the companion monograph [29] and the references therein.

1.3.1 Symmetry Group and Lie Algebra
As noted earlier, dS spacetime is the unique maximally symmetric solution to Einstein’s equations with a positive cosmological constant Λ. Its topology is given by
R1 × S3 , reflecting that the manifold admits a global foliation by Cauchy hypersurfaces diffeomorphic to S3 . No canonical choice of temporal direction exists; the
R1 factor merely parametrizes the leaves of this foliation. Geometrically, it is a
globally hyperbolic Lorentzian manifold with constant positive curvature, uniquely
characterized by a curvature radius 𝑅, which sets the fundamental length scale of
the spacetime and governs both its geometric and group-theoretic properties.
The dS manifold admits a convenient representation as a hyperboloid embedded
in a 4 + 1-dimensional Minkowski spacetime R4,1 , and is defined by:
{
}
dS := 𝑥 = (𝑥 𝛼 ) ∈ R4,1 ; (𝑥) 2 := 𝑥 · 𝑥 = 𝜂 𝛼𝛽 𝑥 𝛼 𝑥 𝛽 = 𝑅 2 ,
(1.7)
where 𝛼, 𝛽 = 0, 1, 2, 3, 4, the coordinates 𝑥 𝛼 are Cartesian, and the ambient
Minkowski metric 𝜂 𝛼𝛽 has the signature (−, +, +, +, +).
Remark 1.1 In this monograph, as already mentioned, we adopt a mostly positive
metric signature, departing from the convention used in the previous monograph
[29]. Far from being a mere change of notation, this choice is motivated by a deeper
conceptual reason; it allows for a consistent embedding of all subsequent group and
algebraic constructions into the alternative split-octonion algebra, a point that will
be clarified naturally at the appropriate places throughout the exposition.
□
Remark 1.2 From a cosmological perspective, the curvature radius 𝑅 is typically
associated with the inverse of the Hubble parameter H, modulo a factor accounting
for physical dimensions:
√︂
3
1
= .
(1.8)
𝑅=
Λ H
The Hubble parameter H quantifies the exponential expansion rate of the spatial
sections in dS spacetime.
□
The dS relativity group SO0 (4, 1) — or its universal covering group Sp(2, 2)
— is a ten-parameter group of linear transformations acting on the ambient
4 + 1-dimensional Minkowski spacetime R4,1 . These transformations preserve the
quadratic form (𝑥) 2 = 𝜂 𝛼𝛽 𝑥 𝛼 𝑥 𝛽 , maintain unit determinant, and preserve the orientation of the “time” coordinate 𝑥 0 . A standard realization of the corresponding Lie
algebra 𝔰𝔬(4, 1)  𝔰𝔭(2, 2) is given by the linear span of ten Killing vector fields:

## PDF page 29

1.3 Brief on de Sitter (dS) Relativity: Symmetry Group, Lie Algebra, and Unitary Irreducible Representations (UIRs)
15

𝐾 𝛼𝛽 = 𝑥 𝛼 𝜕𝛽 − 𝑥 𝛽 𝜕𝛼 ,

(1.9)

where 𝜕𝛼 := 𝜕/𝜕𝑥 𝛼 .

1.3.2 Unitary Irreducible Representations (UIRs)
At the representation level, the ten dS Killing vectors (1.9) correspond to (essentially) self-adjoint operators 𝐽 𝛼𝛽 acting on a Hilbert space of (spinor-)tensor-valued
functions on the dS manifold (1.7), square-integrable with respect to a dS-invariant
inner product of Klein-Gordon type (or a suitable alternative):
𝐾 𝛼𝛽

↦−→

𝐽 𝛼𝛽 = 𝑀 𝛼𝛽 + 𝑆 𝛼𝛽 ,

(1.10)

where the orbital part is defined by 𝑀 𝛼𝛽 = −i(𝑥 𝛼 𝜕𝛽 − 𝑥 𝛽 𝜕𝛼 ), while the spinorial
part 𝑆 𝛼𝛽 acts on the indices of the (spinor-)tensor-valued functions according to a
specific permutation scheme [29].
In this context, there are two Casimir operators:
quadratic ;

1
C2𝔰𝔭(2,2) = − 𝐽 𝛼𝛽 𝐽 𝛼𝛽 ,
2

(1.11)

quartic ;

C4𝔰𝔭(2,2) = −𝑊 𝛼 𝑊 𝛼 ,

(1.12)

where the 𝑊 𝛼 , as the dS counterpart of the Pauli-Lubanski operator, is given by 𝑊 𝛼 =
− 18 𝜀 𝛼𝛽𝛾𝜌 𝛿 𝐽 𝛽𝛾 𝐽 𝜌 𝛿 , while 𝜀 𝛼𝛽𝛾𝜌 𝛿 is the five-dimensional totally antisymmetric LeviCivita symbol. These Casimir operators commute with all generator representatives
𝐽 𝛼𝛽 , and hence, act like constants on all states in a certain dS UIR. Therefore, the
eigenvalues assumed by the Casimir operators can be utilized to classify UIRs of the
dS group. In the Dixmier notation [93], these eigenvalues are expressed in terms of
two dS-invariant parameters, 𝑝 ∈ Z ≥0 /2 and 𝑞 ∈ C, as follows:
⟨

⟩
C2𝔰𝔭(2,2) = −𝑝( 𝑝 + 1) − (𝑞 + 1) (𝑞 − 2) ,

(1.13)

⟩
C4𝔰𝔭(2,2) = −𝑝( 𝑝 + 1)𝑞(𝑞 − 1) .

(1.14)

⟨

Thus, the pair of dS-invariant parameters ( 𝑝, 𝑞) provides a complete characterization
of the UIRs of the dS group. The classification naturally decomposes according to
the admissible domains of these parameters, leading to three distinguished series of
dS UIRs — principal, complementary, and discrete — as reviewed below (see Refs.
[93, 94, 29]).
Remark 1.3 The Casimir eigenvalues remain invariant under the transformation
𝑞 ↦−→ 1 − 𝑞. In other words, the representations labeled by the pairs ( 𝑝, 𝑞) and

## PDF page 30

16 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry

( 𝑝, 1 − 𝑞) possess identical Casimir spectra. By definition, such representations are
said to be Weyl equivalent.
□

1.3.2.1 Principal Series Representations
ps

Principal series representations 𝑈𝑠,𝜈 are specified by ( 𝑝 = 𝑠, 𝑞 = 12 + i𝜈), where
the label 𝑝 = 𝑠 is to be understood as the spin. One must distinguish two separate
families:
1. Integer-spin representations, with 𝑠 = 0, 1, 2, . . . and 𝜈 ∈ R.
2. Half-integer-spin representations, with 𝑠 = 21 , 32 , 25 , . . . and 𝜈 ∈ R − {0}.
ps

The principal UIRs 𝑈𝑠,𝜈 , in the Poincaré contraction limit (𝑅 → ∞, or equivalently Λ → 0), reduce to the positive- and negative-energy Wigner massive UIRs of
≷ and characterized by spin 𝑠 and
the Poincaré group, respectively denoted by P𝑠,𝑚
mass 𝑚 > 0 [95]; symbolically:
ps

𝑈𝑠,𝜈

−→
𝑅→∞

>
<
P𝑠,𝑚
⊕ P𝑠,𝑚
.

(1.15)

In this sense, the dS principal UIRs are identified as dS “massive” representations.
ps

Remark 1.4 The apparent splitting of a dS principal (massive) UIR 𝑈𝑠,𝜈 into a direct
≷ (corresponding to positive- and negativesum of two Poincaré massive UIRs P𝑠,𝑚
energy sectors) can be circumvented either by choosing suitable global dS modes
— namely, the dS plane waves defined in the relevant analyticity tube domains [96]
(see also [29]) — or by carrying out the contraction within the framework of a
causality-preserving dS semigroup [97]. On this basis, one obtains:
ps

𝑈𝑠,𝜈

−→
𝑅→∞

>
P𝑠,𝑚
.

(1.16)
□

1.3.2.2 Complementary Series Representations
cs are specified by ( 𝑝 = 𝑠, 𝑞 = 1 + 𝜈),
Complementary series representations 𝑈𝑠,𝜈
2
where, once again, the parameter 𝑝 = 𝑠 is interpreted as the spin. Two distinct
subclasses arise:

1. Scalar representations, with 𝑠 = 0 and 𝜈 ∈ R satisfying 0 < |𝜈| < 32 .
2. Spinorial representations, with 𝑠 = 1, 2, 3, . . . and 𝜈 ∈ R satisfying 0 < |𝜈| < 21 .
From the standpoint of a Minkowskian observer, the only complementary series
UIR of genuine physical significance is the scalar representation 𝑈 cs
1 , i.e., ( 𝑝 =
𝑠=0,𝜈= 2

0, 𝑞 = 1). This representation admits a unique extension (denoted by ‘↩→’) to the
≷
conformal group massless UIRs C±1,0,0
. This extension is equivalent to the conformal

## PDF page 31

1.3 Brief on de Sitter (dS) Relativity: Symmetry Group, Lie Algebra, and Unitary Irreducible Representations (UIRs)
17
≷
extension of the massless scalar UIRs of the Poincaré group P0,0
, corresponding
respectively to positive and negative energies [40, 25]:
>
>
>
C1,0,0
C1,0,0
←↪ P0,0
−→
⊕
⊕
𝑈 cs1 ↩→ ⊕
0, 2

𝑅→∞

<
C−1,0,0

(1.17)

<
< .
C−1,0,0
←↪ P0,0

In this sense, the scalar representation 𝑈 cs1 is identified as “massless”.
0, 2

Remark 1.5 As already mentioned, conformal invariance, in the strict grouptheoretical sense, involves massless (ladder) series representations (and their lowest
limits) of (the universal covering of) the conformal group, or its double covering
SO(4, 2), or its fourfold covering SU(2, 2). The relevant conformal UIRs are denoted
by CE≷◦ ,j ,j , where E◦ represents the lowest positive or highest negative conformal
𝐿 𝑅
energy, and (j 𝐿 , j𝑅 ) ∈ Z ≥0 /2 × Z ≥0 /2 label the SU(2) × SU(2) representations.
This will be discussed in detail in Chap. 3; in particular, see the arguments given in
Remark 3.12.
□

1.3.2.3 Discrete Series Representations
Discrete series representations are denoted by Π ±𝑝,𝑞 , with each representation
specified by the parameter pair ( 𝑝, 𝑞). In the symmetric case Π ±𝑝=𝑠,𝑞=𝑠 , with
𝑠 = 12 , 1, 32 , . . . , the parameter 𝑝 = 𝑠 labels the absolute value of the helicity while
the superscript ‘±’ indicates its sign, corresponding to the two helicity states ‘±𝑠’;
for later reference, we denote the helicity by 𝜆 := ±𝑠 = ± 12 , ±1, ± 32 , . . . . [For an
in-depth examination of the concept of helicity, see Chap. 3; in particular, consult the
arguments presented in Remark 3.12 and Appendix 3.7.] Within the discrete series,
two subclasses can be identified:
1. Nonsquare-integrable scalar cases, with 𝑝 = 1, 2, . . . and 𝑞 = 0.
2. Spinorial cases, with 𝑝 = 21 , 1, 32 , . . . and 𝑞 = 𝑝, 𝑝 − 1, . . . , 1 or 12 (𝑞 > 0); the
subclass with 𝑞 = 21 is not square integrable.
From the Minkowskian viewpoint, the physically relevant discrete series UIRs
are precisely the symmetric cases Π ±𝑝=𝑠, 𝑞=𝑠 , with 𝑠 = 12 , 1, 32 , . . . , that lie at the
lower limit of the discrete series. These representations admit a unique extension to
massless (ladder) UIRs of the conformal group; this conformal extension coincides,
in a precise representation-theoretic sense, with the conformal uplift of the massless
Poincaré UIRs of helicity 𝜆 = ±𝑠 [40, 25]:
+ ↩→
Π𝑠,𝑠

>
>
>
C𝑠+1,𝑠,0
C𝑠+1,𝑠,0
←↪ P𝑠,0
⊕
−→
⊕
⊕
𝑅→∞
<
C−𝑠−1,𝑠,0

<
< ,
C−𝑠−1,𝑠,0
←↪ P𝑠,0

(1.18)

## PDF page 32

18 An Overview of Conformal Massless Elementary Systems and Wigner’s Vision in de Sitter (dS) Geometry

− ↩→
Π𝑠,𝑠

>
>
>
C𝑠+1,0,𝑠
C𝑠+1,0,𝑠
←↪ P−𝑠,0
⊕
−→
⊕
⊕
𝑅→∞
<
C−𝑠−1,0,𝑠

(1.19)

<
<
C−𝑠−1,0,𝑠
←↪ P−𝑠,0
.

Accordingly, the UIRs Π ±𝑝=𝑠, 𝑞=𝑠 , with 𝑠 = 21 , 1, 32 , . . . , are conventionally referred
to as “massless” representations with helicity 𝜆 = ±𝑠.
Remark 1.6 For later reference — and by including the scalar (zero-helicity; 𝜆 = 0)
massless case (1.17) — the eigenvalues of the quadratic Casimir of the dS Lie
algebra 𝔰𝔭(2, 2) associated with the dS massless UIRs, with helicity 𝜆 = ±𝑠 =
0, ± 12 , ±1, ± 23 , . . . , are:
⟨

⟩
(
)
(
)
C2𝔰𝔭(2,2) 𝑝=𝑠=𝑞 = −2 𝑠2 − 1 = −2 𝜆2 − 1 .

(1.20)

## PDF page 33

Chapter 2

Majorana Representation of the Conformal
Clifford Algebra 𝖈𝖑(4, 2) and its Chiral
Counterpart

Abstract This chapter presents an explicit Majorana representation of the conformal
Clifford algebra 𝔠𝔩(4, 2) on 8-component real spinors, drawing on the rich algebraic
structure of the split-octonions — an 8-dimensional composition algebra constructed
via the Cayley-Dickson process. The discussion begins with a clear and systematic
overview of the number systems, which naturally leads to the octonions; complex
numbers and quaternions. Particular emphasis is placed on the Moufang identities,
which capture alternativity, a relaxed form of associativity that remains fully compatible with spinor calculus. In the split-octonion setting, alternativity coexists with
nonassociativity, creating a subtle but well-controlled framework in which spinorial
multiplications retain internal coherence. By exploiting left multiplication by a suitably chosen set of 6 of the 7 imaginary split-octonion units, the chapter develops
a real-matrix representation of 𝔠𝔩(4, 2) that is both geometrically transparent and
ideally suited to the Majorana formalism. This construction provides a unified algebraic framework for the internal symmetries of the conformal Lie algebra 𝔲(2, 2)
and naturally realizes the embedding chain:
(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩(4, 2) ,
where the 𝔠𝔩(4, 2) pseudoscalar (volume form) generates the 𝔲(1) center of 𝔲(2, 2).
Building on this foundation, the chapter investigates the complex structure inherent in 𝔠𝔩(4, 2) and its action on spinor space, using the simpler 𝔠𝔩(2) case as an
instructive prototype. We emphasize that the Majorana (real) basis and the chiral
basis are merely two alternative bases of the same real Clifford algebra; no complexification is required. Exploiting this insight, a unitary transformation is constructed
that maps the real-matrix basis of 𝔠𝔩(4, 2) to the chiral basis, in which the Cartan
elements of the maximal compact subalgebra of 𝔰𝔲(2, 2), together with the 𝔲(1)
generator defined by the 𝔠𝔩(4, 2) volume form, assume a diagonal form. These results furnish a coherent, geometrically grounded framework for the study of massless
conformal systems, applicable in flat Minkowski spacetime as well as in curved de
Sitter (dS) and anti-dS spacetimes.

19

## PDF page 34

20 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart

2.1 Composition Algebras, Cayley-Dickson Construction, and
Moufang Identities
A composition algebra 𝔄, defined over the real numbers R, is a finite-dimensional
real vector space endowed with the following structures:
1. Norm form: A nondegenerate symmetric bilinear form ⟨·, ·⟩ ; 𝔄 × 𝔄 ↦−→ R,
which satisfies the following properties:
a. Symmetry, meaning that ⟨𝑥, 𝑦⟩ = ⟨𝑦, 𝑥⟩, for all 𝑥, 𝑦 ∈ 𝔄.
b. Nondegeneracy, implying that the map 𝑥 ↦−→ ⟨𝑥, ·⟩ is injective. [In other
words, if ⟨·, ·⟩ is a nondegenerate bilinear form on 𝔄 and ⟨𝑥, 𝑦⟩ = ⟨𝑥 ′ , 𝑦⟩,
for all 𝑦 ∈ 𝔄, then 𝑥 = 𝑥 ′ . To see this, let 𝑧 = 𝑥 − 𝑥 ′ . Then, for all 𝑦 ∈ 𝔄, we
have ⟨𝑧, 𝑦⟩ = ⟨𝑥, 𝑦⟩ − ⟨𝑥 ′ , 𝑦⟩ = 0. By the nondegeneracy of ⟨·, ·⟩, we obtain
𝑧 = 0, and hence, 𝑥 = 𝑥 ′ .]
This bilinear form induces a quadratic form:
𝑁 (𝑥) := ⟨𝑥, 𝑥⟩ ,

(2.1)

referred to as the “norm” on 𝔄.
2. Bilinear product: A bilinear product ⋄ ; 𝔄 × 𝔄 ↦−→ 𝔄, denoted by 𝑥 ⋄ 𝑦 =: 𝑥𝑦,
satisfying the norm composition property:
𝑁 (𝑥𝑦) = 𝑁 (𝑥)𝑁 (𝑦) ,

(2.2)

for all 𝑥, 𝑦 ∈ 𝔄. [This multiplicative property guarantees that every nonzero element in 𝔄 has a well-defined inverse, making composition algebras particularly
valuable in physics and geometry for modeling norm-preserving transformations, such as rotations and symmetry operations. Since rotations are inherently
reversible, the existence of inverses ensures that applying a rotation and then
its inverse restores an object to its original position. Moreover, this property
ensures that multiplication in the algebra preserves norms; for any two elements
𝑥, 𝑦 ∈ 𝔄, their product 𝑥𝑦 satisfies 𝑁 (𝑥𝑦) = 𝑁 (𝑥)𝑁 (𝑦), meaning multiplication
does not alter the individual norms but only affects orientation.]
3. Unit element: A distinguished element 1 ∈ 𝔄 (the unit), satisfying 1𝑥 = 𝑥 1 = 𝑥,
for all 𝑥 ∈ 𝔄. From the above, it is clear that 𝑁 ( 1) = 1. Subsequently, for each
𝜚 ∈ R (i.e., the members of the field), we have 𝑁 ( 𝜚 1) = 𝜚 2 .
Considering the above, one can readily verify the following identity:
⟨𝑥, 𝑦⟩ =

)
1(
𝑁 (𝑥 + 𝑦) − 𝑁 (𝑥) − 𝑁 (𝑦) ,
2

(2.3)

for all 𝑥, 𝑦 ∈ 𝔄, which expresses the bilinear form ⟨·, ·⟩ in terms of the quadratic
norm 𝑁. As a direct consequence of this identity, together with the norm composition
property (2.2), it follows that:

## PDF page 35

2.1 Composition Algebras, Cayley-Dickson Construction, and Moufang Identities

⟨𝑧𝑥, 𝑧𝑦⟩ = ⟨𝑥𝑧, 𝑦𝑧⟩ = 𝑁 (𝑧)⟨𝑥, 𝑦⟩ ,

21

(2.4)

again, for all 𝑥, 𝑦, 𝑧 ∈ 𝔄. The identity (2.4) then immediately yields:
⟨𝑥, 𝑦⟩⟨𝑧, 𝑤⟩ =

)
1(
⟨𝑥𝑧, 𝑦𝑤⟩ + ⟨𝑥𝑤, 𝑦𝑧⟩ ,
2

(2.5)

for all 𝑥, 𝑦, 𝑧, 𝑤 ∈ 𝔄. To establish the latter identity, using Eq. (2.4), it suffices to
expand the right-hand side:
⟨𝑥𝑧, 𝑦𝑤⟩ + ⟨𝑥𝑤, 𝑦𝑧⟩ = ⟨𝑥(𝑧 + 𝑤), 𝑦(𝑧 + 𝑤)⟩ − ⟨𝑥𝑧, 𝑦𝑧⟩ − ⟨𝑥𝑤, 𝑦𝑤⟩
= 𝑁 (𝑧 + 𝑤)⟨𝑥, 𝑦⟩ − 𝑁 (𝑧)⟨𝑥, 𝑦⟩ − 𝑁 (𝑤)⟨𝑥, 𝑦⟩
(
)
= ⟨𝑥, 𝑦⟩ 𝑁 (𝑧 + 𝑤) − 𝑁 (𝑧) − 𝑁 (𝑤) = 2⟨𝑥, 𝑦⟩⟨𝑧, 𝑤⟩ .

(2.6)

On the other hand, substituting 𝑦 by 1 and 𝑧 by 𝑥 into Eq. (2.5), and applying
(2.4), we obtain:
⟨𝑥, 1⟩⟨𝑥, 𝑤⟩ =

)
1( 2
⟨𝑥 , 𝑤⟩ + 𝑁 (𝑥)⟨𝑤, 1⟩ ,
2

(2.7)

or equivalently:
⟩
⟨ 2
𝑥 + 𝑁 (𝑥) 1 − 2⟨𝑥, 1⟩ 𝑥 , 𝑤 = 0 .

(2.8)

Then, the nondegeneracy of the bilinear form ⟨·, ·⟩ ensures that every element 𝑥 in
the composition algebra 𝔄 satisfies the following second-order equation:
𝑥 2 − Tr(𝑥) 𝑥 + 𝑁 (𝑥) 1 = 0 ,
where Tr(𝑥) denotes the trace in the composition algebra 𝔄, defined by:
(
)
Tr(𝑥) = 2⟨𝑥, 1⟩ ∈ R .

(2.9)

(2.10)

By employing Eq. (2.5) alongside the symmetric property of the bilinear form ⟨·, ·⟩,
it follows that the trace satisfies the symmetry property:
Tr(𝑥𝑦) = 2⟨𝑥𝑦, 1⟩ = 4⟨𝑥, 1⟩⟨𝑦, 1⟩ − 2⟨𝑥, 𝑦⟩

= 4⟨𝑦, 1⟩⟨𝑥, 1⟩ − 2⟨𝑦, 𝑥⟩ = 2⟨𝑦𝑥, 1⟩ = Tr(𝑦𝑥) ,

(2.11)

for all 𝑥, 𝑦 ∈ 𝔄.
Within this framework, the Cayley-Dickson conjugate of an element 𝑥 ∈ 𝔄 is
defined by:
𝑥 ∗ := Tr(𝑥) 1 − 𝑥 .

(2.12)

Utilizing this identity, one readily verifies that:
Tr(𝑥 + 𝑦) = Tr(𝑥) + Tr(𝑦) ,

(2.13)

## PDF page 36

22 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart

for all 𝑥, 𝑦 ∈ 𝔄.
By substituting Tr(𝑥) from Eq. (2.12) into (2.9), we derive the following explicit
form for the norm on 𝔄:
𝑁 (𝑥) = 𝑥 ∗ 𝑥 .

(2.14)

Using the materials mentioned above — specifically Eqs. (2.3) and (2.11)-(2.14),
one readily verifies that the Cayley-Dickson conjugation satisfies the following key
properties:
Additivity ;

(𝑥 + 𝑦) ∗ = 𝑥 ∗ + 𝑦 ∗ ,

(2.15)

(𝑥 ∗ ) ∗ = 𝑥 ,

(2.16)

Involution ;
Norm preservation ;

𝑁 (𝑥) = 𝑥 ∗ 𝑥 = 𝑥𝑥 ∗ = 𝑁 (𝑥 ∗ ) ,

Multiplication reversal ;

(𝑥𝑦) ∗ = 𝑦 ∗ 𝑥 ∗ .

(2.17)
(2.18)

While the first three identities follow almost immediately from the relations mentioned above, establishing the latter requires further clarification:
(𝑥𝑦) ∗ = Tr(𝑥𝑦) 1 − 𝑥𝑦

= 4⟨𝑦, 1⟩⟨𝑥, 1⟩ 1 − 2⟨𝑦, 𝑥⟩ 1 − 𝑥𝑦
(
)
= Tr(𝑦)Tr(𝑥) 1 − 𝑁 (𝑦 + 𝑥) − 𝑁 (𝑦) − 𝑁 (𝑥) 1 − 𝑥𝑦
(
)
= Tr(𝑦)Tr(𝑥) 1 − (𝑦 + 𝑥) (𝑦 + 𝑥) ∗ − 𝑦𝑦 ∗ − 𝑥𝑥 ∗ 1 − 𝑥𝑦
( ∗
)
= Tr(𝑦)Tr(𝑥) 1 − 𝑥 𝑦 + 𝑦 − 𝑦𝑥 ∗
(
)
(
)
= Tr(𝑦)Tr(𝑥) 1 − 𝑥 Tr(𝑦) 1 − 𝑦 Tr(𝑥) 1 − 𝑥
(
)(
)
= Tr(𝑦) 1 − 𝑦 Tr(𝑥) 1 − 𝑥 = 𝑦 ∗ 𝑥 ∗ .

(2.19)

A fundamental result, known as the Hurwitz theorem, constrains the possible
dimensions of composition algebras over R. These algebras can only exist in dimensions 1, 2, 4, and 8. The corresponding cases are:
1. The real numbers R, which are both commutative and associative.
2. The complex numbers C, which are also commutative and associative.
3. The quaternions H, which are noncommutative but retain associativity.
4. The octonions O, which are neither commutative nor associative.
As already mentioned, these algebras serve as essential tools in mathematics and
physics, particularly in areas requiring norm-preserving transformations, such as
symmetry operations and rotations.
To ensure this manuscript is self-contained, the following subsections will delve
deeper into the structure and properties of the complex numbers, quaternions, and
octonions, providing a comprehensive overview of their defining characteristics.

## PDF page 37

2.1 Composition Algebras, Cayley-Dickson Construction, and Moufang Identities

23

2.1.1 Complex Numbers
The complex numbers C ∋ 𝑧 = 1𝑧 0 + i𝑧 1 =: 𝑧 0 + i𝑧 1 are defined in terms of
their real components 𝑧 0 , 𝑧1 ∈ R. The real and imaginary units are denoted by
1 = 11 + i0 =: 1 and i, respectively, with the property that i2 = −1. This structure
forms a (commutative and associative) composition algebra over the real numbers
when equipped with:
1. Real bilinear form:
⟨
⟩
⟨𝑧, 𝑤⟩ = 𝑧0 + i𝑧 1 , 𝑤0 + i𝑤1 = 𝑧0 𝑤0 + 𝑧 1 𝑤1 ,

(2.20)

for any 𝑧, 𝑤 ∈ C (𝑧0 , 𝑧1 , 𝑤0 , 𝑤1 ∈ R). The above bilinear form induces the
quadratic norm 𝑁 (𝑧) = (𝑧 0 ) 2 + (𝑧 1 ) 2 . Moreover, considering Eqs. (2.10) and
(2.12), the above bilinear form yields:
𝑧 = 𝑧0 + i𝑧 1 = 𝑧0 − i𝑧 1 ,
where the ‘ ’ symbol denotes the complex conjugate.
2. Multiplication operation:
(
)(
) (
)
(
)
𝑧𝑤 = 𝑧0 + i𝑧 1 𝑤0 + i𝑤1 = 𝑧0 𝑤0 − 𝑧 1 𝑤1 + i 𝑧 0 𝑤1 + 𝑧 1 𝑤0 ,

(2.21)

(2.22)

again, for any 𝑧, 𝑤 ∈ C (𝑧 0 , 𝑧1 , 𝑤0 , 𝑤1 ∈ R). Employing this identity, it is easy to
show that 𝑁 (𝑧) = 𝑧 𝑧 = 𝑧 𝑧 = 𝑁 (𝑧).
The product of two (arbitrary) complex numbers 𝑧 and 𝑤 satisfies the norm
composition property:
𝑁 (𝑧𝑤) = 𝑁 (𝑧)𝑁 (𝑤) .

(2.23)

To explicitly verify this, observe that:
(
)2 (
)2
𝑁 (𝑧𝑤) = 𝑧0 𝑤0 − 𝑧 1 𝑤1 + 𝑧 0 𝑤1 + 𝑧 1 𝑤0
(
)(
)
= (𝑧0 ) 2 + (𝑧 1 ) 2 (𝑤0 ) 2 + (𝑤1 ) 2 = 𝑁 (𝑧)𝑁 (𝑤) .

(2.24)

This multiplicative property establishes that the complex numbers form a composition algebra, where the multiplication is both commutative and associative.

2.1.2 Quaternions: Extending the Complex Numbers
Building on the properties of complex numbers, quaternions are a 4-dimensional
extension of the number system. Introduced by William Rowan Hamilton in 1843,
quaternions are defined as numbers of the form:

## PDF page 38

24 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart

{
H = 𝑞 = 1𝑞 0 + 𝚤𝑞 1 + 𝚥𝑞 2 + 𝒌𝑞 3
}
=: 𝑞 0 + 𝚤𝑞 1 + 𝚥𝑞 2 + 𝒌𝑞 3 ; 𝑞 0 , 𝑞 1 , 𝑞 2 , 𝑞 3 ∈ R ,

(2.25)

where 1 = 11 + 𝚤0 + 𝚥0 + 𝒌0 =: 1 is the real unit element, and 𝚤, 𝚥, 𝒌 are the
quaternion imaginary units. These units obey the following defining multiplication
rules:
𝚤 𝚥 = − 𝚥𝚤 = 𝒌 ,

𝚥 𝒌 = −𝒌 𝚥 = 𝚤 ,

𝒌𝚤 = −𝚤 𝒌 = 𝚥 ,

(2.26)

1𝚤 = 𝚤 1 = 𝚤 , 1 𝚥 = 𝚥 1 = 𝚥 , 1 𝒌 = 𝒌 1 = 𝒌 ,

(2.27)

(𝚤) 2 = ( 𝚥) 2 = ( 𝒌) 2 = −1 =: −1 .

(2.28)

Then, the multiplication of two quaternions 𝑞 and 𝑝 reads as:
(
)(
)
𝑞 𝑝 = 1𝑞 0 + 𝚤𝑞 1 + 𝚥𝑞 2 + 𝒌𝑞 3 1 𝑝 0 + 𝚤 𝑝 1 + 𝚥 𝑝 2 + 𝒌 𝑝 3
(
)
= 1 𝑞0 𝑝0 − 𝑞1 𝑝1 − 𝑞2 𝑝2 − 𝑞3 𝑝3
(
)
+ 𝚤 𝑞0 𝑝1 + 𝑞1 𝑝0 + 𝑞2 𝑝3 − 𝑞3 𝑝2
(
)
+ 𝚥 𝑞0 𝑝2 + 𝑞2 𝑝0 + 𝑞3 𝑝1 − 𝑞1 𝑝3
(
)
+ 𝒌 𝑞0 𝑝3 + 𝑞3 𝑝0 + 𝑞1 𝑝2 − 𝑞2 𝑝1 ,

(2.29)

where 𝑞 0 , . . . , 𝑞 3 , 𝑝 0 , . . . , 𝑝 3 ∈ R. The above explanation makes it evident that
quaternion multiplication, while associative, is not commutative.
Under the conjugation, the imaginary units of the quaternion behave as:
(𝚤) ∗ = −𝚤 ,

( 𝚥) ∗ = − 𝚥 ,

( 𝒌) ∗ = −𝒌 ,

and, of course,

( 1) ∗ = 1 =: 1 . (2.30)

Then, the squared norm of a quaternion 𝑞 is given by:
( )2 ( )2 ( )2 ( )2
𝑁 (𝑞) = 𝑞 ∗ 𝑞 = 𝑞𝑞 ∗ = 𝑞 0 + 𝑞 1 + 𝑞 2 + 𝑞 3 ,

(2.31)

and, subsequently, the inverse of a nonzero quaternion 𝑞 by:
𝑞 −1 =

𝑞∗
.
𝑁 (𝑞)

(2.32)

The latter identity is a clear consequence of the multiplicative property of the composition algebras we discussed earlier.

## PDF page 39

2.1 Composition Algebras, Cayley-Dickson Construction, and Moufang Identities

25

2.1.3 (Split) Octonions: Beyond Associativity
The octonions O and split octonions OS are 8-dimensional, noncommutative, and
nonassociative composition algebras over the real numbers R. They are constructed
via the Cayley-Dickson process by extending the quaternions H with an additional
imaginary unit ℓ. The defining property of this unit distinguishes the octonions O
from their split counterpart OS :


{
 −1 =: −1

O (S) = 𝑜 = 𝑞 + ℓ 𝑝 ; 𝑞, 𝑝 ∈ H , and (ℓ) 2 =

 +1 =: +1


for 𝑜 ∈ O }
,

(2.33)

for 𝑜 ∈ OS

where O (S) denotes either O or OS . Note that, by definition, the term “imaginary
unit” refers to an element whose square is −1. However, in the context of the splitoctonions OS , the extra unit ℓ — satisfying (ℓ) 2 = +1 — is also commonly (though
imprecisely) referred to as an imaginary unit, by abuse of notation.
The (split)-octonion algebras are endowed with the following operations for all
𝑞 1 , 𝑝 1 , 𝑞 2 , 𝑝 2 ∈ H:
1. Addition:
(

) (
) (
)
(
)
𝑞1 + ℓ 𝑝1 + 𝑞2 + ℓ 𝑝2 = 𝑞1 + 𝑞2 + ℓ 𝑝1 + 𝑝2 .

(2.34)

2. Multiplication: Obeying the norm composition property (2.2), the product of
two octonions reads as:1
(
)(
)
(
)
𝑞 1 + ℓ 𝑝 1 𝑞 2 + ℓ 𝑝 2 = 𝑞 1 𝑞 2 + (ℓ) 2 𝑝 2 𝑝 ∗1 + ℓ 𝑞 ∗1 𝑝 2 + 𝑞 2 𝑝 1 .
(2.35)
3. Conjugation:
(𝑞 + ℓ 𝑝) ∗ = 𝑞 ∗ − ℓ 𝑝 ,

(hence ℓ ∗ = −ℓ) .

(2.36)

Note that, considering the anticommutativity of conjugation with respect to multiplication (see Eq. (2.18)), this identity directly implies the following essential
relations:
𝑝∗ℓ = ℓ 𝑝 ,

(2.37)

for all 𝑝 ∈ H, which highlight the interplay between the quaternionic components
and the additional imaginary unit ℓ.
Using the octonionic conjugation (2.36) and the multiplication rule (2.35), the
norm of a (split) octonion can be expressed as:
𝑁 (𝑞 + ℓ 𝑝) = (𝑞 + ℓ 𝑝) (𝑞 + ℓ 𝑝) ∗ = 𝑁 (𝑞) − (ℓ) 2 𝑁 ( 𝑝) ,

1 For a mnemonic matrix rule for (split) octonionic multiplication, see Appendix 2.5.

(2.38)

## PDF page 40

26 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart

where, as we already discussed, 𝑁 (𝑞) = 𝑞𝑞 ∗ = 𝑞 ∗ 𝑞 is the quaternionic norm. This
leads to the following key distinctions:
1. For the octonions O, where (ℓ) 2 = −1 =: −1, the norm is positive-definite:
𝑁 (𝑞 + ℓ 𝑝) = 𝑁 (𝑞) + 𝑁 ( 𝑝) .

(2.39)

This makes O a division algebra, as every nonzero element is invertible.
2. For the split octonions OS , where (ℓ) 2 = +1 =: +1, the norm is indefinite (with
the signature (4, 4)):
𝑁 (𝑞 + ℓ 𝑝) = 𝑁 (𝑞) − 𝑁 ( 𝑝) .

(2.40)

The indefinite norm allows for zero divisors, preventing the algebra from forming
a division algebra.

2.1.3.1 Alternativity
It must be emphasized that the resulting (split) octonion algebras are nonassociative
and, more precisely, are classified as alternative algebras. While (split) octonions are
not associative, their alternativity ensures that certain partial forms of associativity
are preserved when elements are repeated. In particular:
𝑜(𝒏 𝑜) = (𝑜 𝒏)𝑜 ,

(2.41)

𝑜∗ (𝒏 𝑜) = (𝑜 ∗ 𝒏)𝑜 ,

(2.42)

for all 𝒏, 𝑜 ∈ O (S) . Furthermore, the (split) octonions adhere to the key left, right,
and central Ruth Moufang identities [82], which are given respectively as:
(
)
𝑜 𝒎 (𝑜 𝒏) = (𝑜 𝒎 𝑜)𝒏 ,
(2.43)
(

)
(𝒎 𝑜) 𝒏 𝑜 = 𝒎(𝑜 𝒏 𝑜) ,

(2.44)

(𝑜 𝒎) (𝒏 𝑜) = 𝑜(𝒎 𝒏)𝑜 ,

(2.45)

for all 𝒎, 𝒏, 𝑜 ∈ O (S) .
By invoking the quaternion imaginary units 𝚤, 𝚥, and 𝒌, let us revisit the (split)
octonion definition (2.33). The structure naturally extends to include seven distinct
imaginary units, which we can explicitly enumerate as:
(
)
𝚤, 𝚥, 𝒌, ℓ, ℓ𝚤, 𝚥ℓ = −ℓ 𝚥 , ℓ𝒌 .
(2.46)

## PDF page 41

2.1 Composition Algebras, Cayley-Dickson Construction, and Moufang Identities

27

These units, together with the real unit 1 = 1 + 𝚤0 + 𝚥0 + . . . + ℓ𝒌0 =: 1, form
the full basis of the (split) octonions. Their interplay reflects the noncommutative
and nonassociative nature of the algebra, while satisfying the alternativity properties
given in Eqs. (2.41)-(2.45). Specifically, the multiplication rules governing these
units can be systematically derived from the general structure provided in Eq. (2.35).
For the split octonions OS relevant to our study, we have the following convenient
multiplication table:

𝚤

𝚥

𝒌

ℓ

ℓ𝚤

𝚥ℓ

ℓ𝒌

1

1
1

𝚤

𝚥

𝒌

ℓ

ℓ𝚤

𝚥ℓ

ℓ𝒌

𝚤

𝚤

−1

𝒌

−𝚥

−ℓ𝚤

ℓ

ℓ𝒌

− 𝚥ℓ

𝚥

𝚥

−𝒌

−1

𝚤

𝚥ℓ

ℓ𝒌

−ℓ

−ℓ𝚤

𝒌

𝒌

𝚥

−𝚤

−1

−ℓ𝒌

𝚥ℓ

−ℓ𝚤

ℓ

ℓ

ℓ

ℓ𝚤

− 𝚥ℓ

ℓ𝒌

1

𝚤

−𝚥

𝒌

ℓ𝚤

ℓ𝚤

−ℓ

−ℓ𝒌

− 𝚥ℓ

−𝚤

1

−𝒌

−𝚥

𝚥ℓ

𝚥ℓ

−ℓ𝒌

ℓ

ℓ𝚤

𝚥

𝒌

1

−𝚤

ℓ𝒌

ℓ𝒌

𝚥ℓ

ℓ𝚤

−ℓ

−𝒌

𝚥

𝚤

1

𝑥 ⋄ 𝑦 := 𝑥𝑦

(2.47)
Keeping the focus specifically on the split-octonion algebra relevant to our study,
three complementary remarks are in order:
Remark 2.1 We observe that:
1. The seven imaginary split-octonion units are mutually anticommutative.
2. These anticommutative imaginary split-octonion units can be expressed in terms
of the product of the three basic elements 𝚤, 𝚥, and ℓ.
□
Remark 2.2 Analogous to the identities given in Eq. (2.41)-(2.45), any pairs of
different imaginary split-octonion units generate an 8-dimensional associative group:
1. The pair (𝚤, 𝚥) generates the quaternion subalgebra:
{
}
± 𝚤, ± 𝚥, ±𝒌, ±1 ,

(2.48)

which is associative by construction. For example:
𝚤( 𝚥 𝒌) = (𝚤 𝚥) 𝒌 .

(2.49)

2. Any other pair of distinct imaginary units likewise generates an associative subalgebra of split-octonions. For instance, the pair (𝚤, 𝚥ℓ) generates the subalgebra:

## PDF page 42

28 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart

{

}
± 𝚤, ± 𝚥ℓ, ±ℓ𝒌, ±1 ,

(2.50)

which is again associative. For instance:
(
) (
)
𝚤 ( 𝚥ℓ) (ℓ𝒌) = 𝚤( 𝚥ℓ) (ℓ𝒌) .

(2.51)

Note: Three imaginary units are said to be independent if they do not belong to an
associative subalgebra of the Moufang loop of OS units. For example, the aforementioned three basic elements 𝚤, 𝚥, and ℓ are independent as:
(
)
(
)
(𝚤) ( 𝚥) ℓ ≠ 𝚤 ( 𝚥) (ℓ) .
(2.52)
□
Remark 2.3 As an extension of Moufang’s theorem (see Ref. [98]), the loop generated by any three independent elements — for example, 𝚤, 𝚥, and ℓ — indeed forms a
“modified” associative finite subalgebra. The corresponding “modified” associative
law differs from the standard one by an overall sign, which encodes the nonassociative (in the usual sense) character of the three independent units. For instance, the
nonequality in Eq. (2.52) explicitly reads:
(
)
(
)
(𝚤) ( 𝚥) ℓ = −𝚤 ( 𝚥) (ℓ) .
(2.53)
Thus, for any triple of independent (and therefore nonassociative) imaginary splitoctonion units, Moufang’s theorem guarantees that seemingly nonintuitive identities
can be derived systematically via the “modified” associative law. As a further illustrative case, let us examine the independent generators ℓ, 𝒌, and 𝚤:
(
)
(
)
(ℓ) ( 𝒌) 𝚤 = −ℓ ( 𝒌) (𝚤) = −ℓ 𝚥 = 𝚥ℓ ,
(2.54)
⏟
⏞⏞
⏟
by “modified” associative law

which is fully consistent with the multiplication table in (2.47).
Summary: Any triple of imaginary split-octonion units is either nonindependent,
and therefore fully associative, or independent, and thus “modified” associative,
with the modification differing from standard associativity by an overall sign. This
precisely expresses the principle of alternativity that characterizes the split-octonion
algebra.
□
Proposition 2.1 As a direct consequence of the preceding Remarks, for all 𝒎, 𝒏 ∈
OS \{1} and 𝑜 ∈ OS , one has:
𝒎(𝒏 𝑜) =



 −𝒏(𝒎 𝑜)


 𝒎2 𝑜


for

𝒎≠𝒏

for

𝒎=𝒏

.

(2.55)

Proof — Step I (first case, with nonindependent (associative) units). If 𝒎, 𝒏, 𝑜
(with 𝒎 ≠ 𝒏) belong to a nonindependent subalgebra, we have:

## PDF page 43

2.2 Conformal Clifford Algebra 𝔠𝔩 (4, 2) Generated by Left Multiplication of Imaginary Split-Octonion Units
29

𝒎(𝒏 𝑜) = (𝒎 𝒏) 𝑜

(by standard associative law)

= (−𝒏 𝒎) 𝑜

(by anticommutativity of imaginary units)

= −𝒏(𝒎 𝑜)

(again, by standard associative law) .

(2.56)

— Step II (first case, with independent (nonassociative) units). If 𝒎, 𝒏, 𝑜 (with
𝒎 ≠ 𝒏) form an independent triple, invoking the “modified” associative law from
Remark 2.3, we get:
𝒎(𝒏 𝑜) = −(𝒎 𝒏) 𝑜

(by “modified” associative law)

= −(−𝒏 𝒎) 𝑜
= −𝒏(𝒎 𝑜)

(by anticommutativity of imaginary units)
(again, by “modified” associative law) .

(2.57)

— Step III (second case). When 𝒎 = 𝒏, the result follows immediately from
alternativity. Indeed, any pair of split-octonion units generates an associative subalgebra — a direct consequence of Remark 2.2. Therefore:
𝒎(𝒎 𝑜) = (𝒎 𝒎) 𝑜 = 𝒎 2 𝑜 .
This identity generalizes straightforwardly to repeated multiplications:
(
)
(
)
𝒎 . . . 𝒎(𝒎 𝑜) . . . = 𝒎 𝑟 𝑜 .
⏟ ⏞⏞ ⏟

(2.58)

(2.59)

𝑟 times

As a direct consequence (setting 𝑜 = 1), powers of a single split-octonion unit are
fully associative and therefore well-defined, ensuring that all such repeated products
are unambiguous.
From the preceding results, it follows that Eq. (2.55) is valid.
□

2.2 Conformal Clifford Algebra 𝖈𝖑(4, 2) Generated by Left
Multiplication of Imaginary Split-Octonion Units
Let us define the operators 𝐿 𝐴 representing left multiplication by split-octonion units
𝐴 acting on the split-octonion algebra OS :
𝐿 𝐴 𝑥 := 𝐴 𝑥 .

(2.60)

This definition carries the intrinsic split-octonion multiplication (right-hand side)
into a corresponding matrix realization (left-hand side). The symbols 𝐴 and 𝑥 therefore play a dual role in Eq. (2.60); on the right-hand side, they are elements of the
split-octonion algebra, while on the left-hand side 𝐴 functions purely as an index
labelling a 8 × 8 matrix operator and 𝑥 is treated as a 8-component column vector

## PDF page 44

30 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

representing a Dirac-Majorana spinor. Readers should always interpret each symbol
according to its position in (2.60). More specifically:
1. On the right-hand side of (2.60), the symbols 𝐴 and 𝑥 are to be interpreted
strictly as elements of the split-octonion algebra:
{
{
}}
𝑥 ∈ OS = Span 𝐴 ; 𝐴 = 1, 𝒌, 𝜈, with 𝜈 ∈ 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌, ℓ . (2.61)
2. On the left-hand side of (2.60), by contrast, 𝐴 solely plays the role of an index
labelling the associated 8 × 8 matrix operator 𝐿 𝐴; no octonionic interpretation is attached to 𝐴 in this position. Correspondingly, 𝑥 is interpreted as an
8-component Dirac-Majorana spinor, obtained by identifying OS  R8 with respect to the basis above. Each 𝐿 𝐴 acts linearly on this spinor space. Accordingly,
the operators 𝐿 𝐴 can be enumerated as:
{
}
𝐿 𝐴 = 𝐿 1 , 𝐿 𝒌 , 𝐿 𝜈 , with 𝜈 ∈ 0 := 𝚤, 5 := 𝚥, 1 := ℓ𝚤, 2 := 𝚥ℓ, 3 := ℓ𝒌, 4 := ℓ .
(2.62)
Remark 2.4 We emphasize that the map 𝐴 ↦−→ 𝐿 𝐴 is not an algebra homomorphism. While the product 𝐴 ⋄ 𝐵 := 𝐴𝐵, with 𝐴, 𝐵 = 1, 𝒌, 𝜈 ∈ {𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ},
is nonassociative (more precisely, alternative), the matrix product 𝐿 𝐴 𝐿 𝐵 is associative.
In fact, all nested products of operators 𝐿 𝐴 are interpreted as successive left
multiplications on 𝑥 ∈ Span{ 𝐴}. This convention ensures that, despite the intrinsic
nonassociativity of the split-octonions, expressions of the form:
𝐿 𝐴 𝐿 𝐵 𝐿 𝐶 𝑥 = (𝐿 𝐴 𝐿 𝐵 ) (𝐿 𝐶 𝑥)
= (𝐿 𝐴 𝐿 𝐵 𝐿 𝐶 ) 𝑥
= 𝐿 𝐴 (𝐿 𝐵 𝐿 𝐶 ) 𝑥
..
.
(
)
(
)
= 𝐿 𝐴 𝐿 𝐵 (𝐿 𝐶 𝑥) = 𝐴 𝐵(𝐶 𝑥)

(2.63)

are fully unambiguous and well-defined. Of course, for brevity, parentheses may occasionally be omitted in such expressions, although their presence is always implied
by definition.
Consequently, we have 𝐿 𝐴 𝐿 𝐵 ≠ 𝐿 𝐴𝐵 , since 𝐿 𝐴 𝐿 𝐵 𝑥 = 𝐴(𝐵 𝑥) while 𝐿 𝐴𝐵 𝑥 =
( 𝐴𝐵) 𝑥. Nevertheless, in the sequel, we adopt the convenient notation 𝐿 𝐴 𝐿 𝐵 =: 𝐿 𝐴𝐵 ,
which is always understood to mean 𝐿 𝐴𝐵 𝑥 = 𝐴(𝐵 𝑥).
□
Let us now denote 6 of the 8 operators 𝐿 𝐴, when 𝐴 = 𝜈 = 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ or
simply 𝐴 = 𝜈 = 0, 5, 1, 2, 3, 4, by 𝑚 𝜈 := 𝐿 𝜈 . By construction, the set of elements 𝑚 𝜈
generates the conformal Clifford algebra 𝔠𝔩(4, 2) — more precisely, its embedding
into the alternative-split-octonion algebra. Specifically, these elements satisfy the
following anticommutation relations:

## PDF page 45

2.2 Conformal Clifford Algebra 𝔠𝔩 (4, 2) Generated by Left Multiplication of Imaginary Split-Octonion Units
31

{

}
𝑚𝜇, 𝑚𝜈 𝑥 = 𝑚𝜇𝑚𝜈 𝑥 + 𝑚𝜈 𝑚𝜇 𝑥
= 𝜇(𝜈 𝑥) + 𝜈(𝜇 𝑥)
{
𝜇(𝜈 𝑥) − 𝜇(𝜈 𝑥) = 0
=
2𝜇2 𝑥
= 2𝜂 𝜇𝜈 𝑥 ,

for
for

𝜇≠𝜈
𝜇=𝜈

(from Proposition 2.1)

(from Table (2.47)) ,

(2.64)

where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), while the metric 𝜂 𝜇𝜈 (with 𝜇, 𝜈 =
0, 5, 1, 2, 3, 4) has the signature (−, −, +, +, +, +), corresponding to the 4 + 2dimensional Minkowski-like space R4,2 .
Notably, the generators 𝑚 𝜈 admit a matrix representation in which each generator
can be expressed as a direct sum of either (only) 2 × 2 symmetric matrices 𝑆 𝐴𝐵
(𝑆 𝐴𝐵 = 𝑆 𝐵 𝐴) or 2 × 2 antisymmetric matrices 𝐸 𝐴𝐵 (𝐸 𝐴𝐵 = −𝐸 𝐵𝐴). Specifically:
1. The four generators 𝑚 𝑖 , with 𝑖 = ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ (or more conveniently, as indices,
𝑖 = 1, 2, 3, 4), each satisfying (according to Proposition 2.1, Remark 2.4, and
Table (2.47)):
(
)
(𝑚 𝑖 ) 2 𝑥 = (𝑚 𝑖 𝑚 𝑖 ) 𝑥 = 𝑖 𝑖(𝑥) = (𝑖) 2 𝑥 = +1 𝑥 ,
(2.65)
can be expressed in terms of the 2 × 2 symmetric matrices 𝑆 𝐴𝐵 as follows:
⨁(
)
(
)
𝑚 1 𝑥 := 𝑚 ℓ𝚤 𝑥 = ℓ𝚤 𝑥 =
𝑆1 (ℓ𝚤) − 𝑆𝚤 ℓ − 𝑆 𝚥 (ℓ𝒌 ) − 𝑆𝒌 ( 𝚥ℓ) 𝑥 ,
⨁
(𝑆11 − 𝑆04 − 𝑆53 − 𝑆𝒌2 ) 𝑥 ,
(2.66)
=
⨁(
)
(
)
𝑚 2 𝑥 := 𝑚 𝚥ℓ 𝑥 = 𝚥ℓ 𝑥 =
𝑆1 ( 𝚥ℓ) + 𝑆 𝚥 ℓ − 𝑆𝚤 (ℓ𝒌 ) + 𝑆𝒌 (ℓ𝚤) 𝑥 ,
⨁
(𝑆12 + 𝑆54 − 𝑆03 + 𝑆𝒌1 ) 𝑥 ,
(2.67)
=
⨁(
)
(
)
𝑚 3 𝑥 := 𝑚 ℓ𝒌 𝑥 = ℓ𝒌 𝑥 =
𝑆1 (ℓ𝒌 ) − 𝑆𝒌 ℓ + 𝑆 𝚥 (ℓ𝚤) + 𝑆𝚤 ( 𝚥ℓ) 𝑥 ,
⨁
(𝑆13 − 𝑆𝒌4 + 𝑆51 + 𝑆02 ) 𝑥 ,
(2.68)
=
⨁(
(
)
)
𝑚 4 𝑥 := 𝑚 ℓ 𝑥 = ℓ 𝑥 =
𝑆1ℓ + 𝑆𝚤 (ℓ𝚤) − 𝑆 𝚥 ( 𝚥ℓ) + 𝑆𝒌 (ℓ𝒌 ) 𝑥 ,
⨁
(𝑆14 + 𝑆01 − 𝑆52 + 𝑆𝒌3 ) 𝑥 ,
(2.69)
=
where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), for the convention
Sect. 1.2.5.2, and:
(
)
𝑆 𝐴𝐵 𝑥 = 𝑆 𝐵𝐴 𝑥 := 𝐴 𝛿 𝐵𝑥 + 𝐵 𝛿 𝐴𝑥 ,

⨁

(. . . ), see
(2.70)

## PDF page 46

32 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

for all 𝐴, 𝐵 = 1, 𝒌, 𝜈 ∈ {𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ} (or more conveniently, as indices,
𝜈 ∈ {0, 5, 1, 2, 3, 4}). Evidently, the matrices 𝑚 𝑖 (𝑖 = 1, 2, 3, 4), of square +1,
are symmetric by their very construction. Note that the above equations can be
easily verified by substituting 𝑥 with any of the split-octonion units (and in fact
with all of them) and consulting the multiplication table (2.47).
2. The two remaining generators 𝑚 0 and 𝑚 5 , each satisfying (𝑚 0 ) 2 = (𝑚 5 ) 2 = −1,
can be written in terms of 2 × 2 antisymmetric matrices 𝐸 𝐴𝐵 as follows:
⨁(
(
)
)
𝑚 0 𝑥 := 𝑚𝚤 𝑥 = 𝚤 𝑥 =
𝐸𝚤1 + 𝐸 𝒌 𝚥 + 𝐸 ℓ (ℓ𝚤) + 𝐸 (ℓ𝒌 ) ( 𝚥ℓ) 𝑥
⨁
(𝐸 01 + 𝐸 𝒌5 + 𝐸 41 + 𝐸 32 ) 𝑥 ,
=
(2.71)
⨁(
(
)
)
𝑚 5 𝑥 := 𝑚 𝚥 𝑥 = 𝚥 𝑥 =
𝐸 𝚥1 + 𝐸𝚤𝒌 − 𝐸 (ℓ𝚤) (ℓ𝒌 ) + 𝐸 ( 𝚥ℓ)ℓ 𝑥
⨁
(𝐸 51 + 𝐸 0𝒌 − 𝐸 13 + 𝐸 24 ) 𝑥 ,
=
(2.72)
where, again, 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), for the convention
see Sect. 1.2.5.2, and:
(
)
𝐸 𝐴𝐵 𝑥 = −𝐸 𝐵𝐴 𝑥 := 𝐴 𝛿 𝐵𝑥 − 𝐵 𝛿 𝐴𝑥 ,

⨁

(. . . ),

(2.73)

for all 𝐴, 𝐵 = 1, 𝒌, 𝜈 ∈ {𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ} or more conveniently, as indices,
𝜈 ∈ {0, 5, 1, 2, 3, 4} (see Eqs. (2.60)-(2.62)). Evidently, the matrices 𝑚 0 and 𝑚 5 ,
of square −1, are skewsymmetric by construction. Again, the above equations
can be verified by substituting 𝑥 with any of the split-octonion units (and in fact
with all of them).
Remark 2.5 In terms of the standard 2 × 2 Weyl matrix basis 𝑒 𝐴𝐵 , defined as the
matrix with entry ‘1’ at the intersection of the 𝐴-th row and 𝐵-th column and
‘0’ elsewhere (for all indices 𝐴, 𝐵 independently ranging over the eight values
1, 𝒌, 𝜈 ∈ {𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ}; see Eqs. (2.60)-(2.62)), and characterized by the
multiplication rule:
𝑒 𝐴𝐵 𝑒𝐶𝐷 = 𝛿 𝐵𝐶 𝑒 𝐴𝐷 ,

(2.74)

the above 𝐸 𝐴𝐵 and 𝑆 𝐴𝐵 (𝐴 ≠ 𝐵) assume, respectively, the following forms:
𝐸 𝐴𝐵 = 𝑒 𝐴𝐵 − 𝑒 𝐵𝐴 ,

(2.75)

𝑆 𝐴𝐵 = 𝑒 𝐴𝐵 + 𝑒 𝐵𝐴 .

(2.76)

For the latter use, we additionally define:
𝑆 𝐴𝐵 𝑆 𝐴𝐵 = −𝐸 𝐴𝐵 𝐸 𝐴𝐵 = 𝑒 𝐴𝐴 + 𝑒 𝐵𝐵 =: 1 𝐴𝐵 ,

(2.77)

## PDF page 47

2.2 Conformal Clifford Algebra 𝔠𝔩 (4, 2) Generated by Left Multiplication of Imaginary Split-Octonion Units
33

𝐸 𝐴𝐵 𝑆 𝐴𝐵 = 𝑒 𝐴𝐴 − 𝑒 𝐵𝐵 =: 𝐷 𝐴𝐵 .

(2.78)

We also notice that the following relations hold:
𝑆 𝐴𝐵 = 𝐷 𝐴𝐵 𝐸 𝐴𝐵 = −𝐸 𝐴𝐵 𝐷 𝐴𝐵 ,

(2.79)

𝐸 𝐴𝐵 = 𝐷 𝐴𝐵 𝑆 𝐴𝐵 = −𝑆 𝐴𝐵 𝐷 𝐴𝐵 .

(2.80)
□

Remark 2.6 From
discussion, it is straightforward to verify that the map( the above
)
ping 𝜈 ↦−→ 𝐿 𝜈 =: 𝑚 𝜈 does not respect the Cayley conjugation (2.12). While according to (2.12), 𝜈 ∗ = −𝜈 for all 𝜈 = 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ (as indices 𝜈 = 0, 5, 1, 2, 3, 4;
see Eqs. (2.60)-(2.62)), only matrices 𝑚 0 and 𝑚 5 are anti-Hermitian; specifically, we
have:
)
( ( )
⊤
(2.81)
𝑚 0∗ = 𝑚 0 = 𝑚 0⊤ = −𝑚 0 , 𝑚 5∗ = −𝑚 5 , while 𝑚 𝑖∗ = 𝑚 𝑖 ,
for all 𝑖 = 1, 2, 3, 4. Equivalently, in a more concise form:
𝑚 ∗𝜈 = 𝑚 2𝜈 𝑚 𝜈 .

(2.82)
□

Let us introduce the following skewsymmetric product:
]
(
)
1[
𝑚 𝜇𝜈 𝑥 = −𝑚 𝜈 𝜇 𝑥 := 𝑚 𝜇 , 𝑚 𝜈 𝑥
2
)
1(
= 𝜇(𝜈 𝑥) − 𝜈(𝜇 𝑥)
2
= 𝜇(𝜈 𝑥) (from Proposition 2.1)
=: 𝑚 𝜇 𝑚 𝜈 𝑥 ,

(2.83)

where 𝑥 ∈ Span{ 𝐴} and 𝜇, 𝜈 = 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ or simply, as indices, 𝜇, 𝜈 =
0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)), such that 𝜇 ≠ 𝜈 since 𝑚 𝜇𝜇 = 0. These 15
operators 𝑚 𝜇𝜈 span the 8-dimensional realization of the isometry Lie algebra associated with the Clifford algebra 𝔠𝔩(4, 2), namely, 𝔰𝔲(2, 2)  𝔰𝔬(4, 2).2 Specifically,
the generators 𝑚 𝜇𝜈 satisfy the following commutation relations:
[

]
(
)
𝑚 𝜇𝜈 , 𝑚 𝜆𝜎 𝑥 = 2 𝜂 𝜈𝜆 𝑚 𝜇 𝜎 − 𝜂 𝜇𝜆 𝑚 𝜈 𝜎 − 𝜂 𝜈 𝜎 𝑚 𝜇𝜆 + 𝜂 𝜇 𝜎 𝑚 𝜈𝜆 𝑥 ,

(2.84)

where again 𝑥 ∈ Span{ 𝐴} and 𝜇, 𝜈, 𝜆, 𝜎 = 0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)),
such that 𝜇 ≠ 𝜈 and 𝜆 ≠ 𝜎. This confirms that the generators 𝑚 𝜇𝜈 form a well-defined
representation of the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) within the Clifford framework.
2 For the extension of this construction to the group level, see Appendix 2.6.

## PDF page 48

34 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

The above commutation relation can be readily verified by extending Proposition 2.1
and referring to the multiplication table (2.47):
[
]
𝑚 𝜇𝜈 , 𝑚 𝜆𝜎 𝑥 = 𝑚 𝜇𝜈 𝑚 𝜆𝜎 𝑥 − 𝑚 𝜆𝜎 𝑚 𝜇𝜈 𝑥
= 𝑚 𝜇 𝑚 𝜈 𝑚𝜆 𝑚 𝜎 𝑥 − 𝑚𝜆 𝑚 𝜎 𝑚 𝜇 𝑚 𝜈 𝑥
( (
( (
))
))
= 𝜇 𝜈 𝜆(𝜎 𝑥) − 𝜆 𝜎 𝜇(𝜈 𝑥)
( (
( (
))
))


𝜇
𝜈
𝜆(𝜎
𝑥)
−
𝜇
𝜈
𝜆(𝜎
𝑥)
=0
for 𝜇 ≠ 𝜈 ≠ 𝜆 ≠ 𝜎





(
)
(
)
(
)


𝜈 2 𝜇(𝜎 𝑥) + 𝜈 2 𝜇(𝜎 𝑥) = 2𝜈 2 𝜇(𝜎 𝑥)
for 𝜇 ≠ 𝜈 = 𝜆 ≠ 𝜎





(
)
(
)
(
)
= −𝜇2 𝜈(𝜎 𝑥) − 𝜇2 𝜈(𝜎 𝑥) = −2𝜇2 𝜈(𝜎 𝑥)
for 𝜈 ≠ 𝜇 = 𝜆 ≠ 𝜎



(
)
(
)
(
)



−𝜈 2 𝜇(𝜆 𝑥) − 𝜈 2 𝜇(𝜆 𝑥) = −2𝜈 2 𝜇(𝜆 𝑥)
for 𝜇 ≠ 𝜈 = 𝜎 ≠ 𝜆





 𝜇2 ( 𝜈(𝜆 𝑥) ) + 𝜇2 ( 𝜈(𝜆 𝑥) ) = 2𝜇2 ( 𝜈(𝜆 𝑥) )
for 𝜈 ≠ 𝜇 = 𝜎 ≠ 𝜆

(
)
(
)
(
)
(
)
= 2𝜂 𝜈𝜆 𝜇(𝜎 𝑥) − 2𝜂 𝜇𝜆 𝜈(𝜎 𝑥) − 2𝜂 𝜈 𝜎 𝜇(𝜆 𝑥) + 2𝜂 𝜇 𝜎 𝜈(𝜆 𝑥)
(
)
(
)
(
)
(
)
= 2𝜂 𝜈𝜆 𝑚 𝜇 𝑚 𝜎 𝑥 − 2𝜂 𝜇𝜆 𝑚 𝜈 𝑚 𝜎 𝑥 − 2𝜂 𝜈 𝜎 𝑚 𝜇 𝑚 𝜆 𝑥 + 2𝜂 𝜇 𝜎 𝑚 𝜈 𝑚 𝜆 𝑥
)
(
= 2 𝜂 𝜈𝜆 𝑚 𝜇 𝜎 − 𝜂 𝜇𝜆 𝑚 𝜈 𝜎 − 𝜂 𝜈 𝜎 𝑚 𝜇𝜆 + 𝜂 𝜇 𝜎 𝑚 𝜈𝜆 𝑥 .
(2.85)
Remark 2.7 The generators 𝑚 𝜇𝜈 are orthogonal, under the trace product, to all 𝐿 𝐴:
Tr(𝑚 𝜇𝜈 𝑚 𝜆 ) = 0 ,

(2.86)

Tr(𝑚 𝜇𝜈 𝐿 𝒌 ) = 0 ,

(2.87)

Tr(𝑚 𝜇𝜈 𝐿 1 ) = 0 ,

(2.88)

where 𝐴 = 1, 𝒌, 𝜈 and 𝜇, 𝜈, 𝜆 = 0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)). These results
follow directly from the standard properties (2.11) and (2.13) of the trace.
□
Remark 2.8 The matrices 𝑚 𝑖 , with 𝑖 = ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ or more conveniently, as indices, 𝑖 = 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)), form the Clifford subalgebra 𝔠𝔩(4) ⊂
𝔠𝔩(4, 2), whose associated isometry Lie algebra is 𝔰𝔬(4). The generators of this Lie
algebra are given by:
𝑚𝑖 𝑗

(

]
)
1[
= −𝑚 𝑗𝑖 := 𝑚 𝑖 , 𝑚 𝑗 = 𝑚 𝑖 𝑚 𝑗 ,
2

(2.89)

where 𝑖, 𝑗 = 1, 2, 3, 4, while 𝑖 ≠ 𝑗 (since 𝑚 𝑖𝑖 = 0). They satisfy the following
commutation relations:
[
]
(
)
𝑚 𝑖 𝑗 , 𝑚 𝑙𝑘 = 2 𝜂 𝑗𝑙 𝑚 𝑖𝑘 − 𝜂𝑖𝑙 𝑚 𝑗 𝑘 − 𝜂 𝑗 𝑘 𝑚 𝑖𝑙 + 𝜂𝑖𝑘 𝑚 𝑗𝑙 ,
(2.90)

## PDF page 49

2.3 Diagonalizing the Complex Structure of 𝔠𝔩 (4, 2) in Spinor Space: Insight from the 𝔠𝔩 (2) Case
35

where the metric 𝜂𝑖 𝑗 has signature (+, +, +, +), corresponding to the 4-dimensional
Euclidean space R4 . Additionally, employing Proposition 2.1, Remark 2.4, and the
multiplication table (2.47), it is straightforward to verify that:
)
( (
( )2
(
)2
(
)
(
))
𝑚 𝑖 𝑗 𝑥 = 𝑚 𝑖 𝑚 𝑗 𝑥 = 𝑚 𝑖 𝑚 𝑗 𝑚 𝑖 𝑚 𝑗 𝑥 = 𝑖 𝑗 𝑖 ( 𝑗 𝑥)
= −𝜂𝑖𝑖 𝜂 𝑗 𝑗 𝑥 = −1 𝑥 ,
(2.91)
where again 𝑖, 𝑗 = 1, 2, 3, 4, while 𝑖 ≠ 𝑗.

□

Remark 2.9 It is remarkable that, while the product of any three independent imaginary OS units is generally nonassociative, the product of all six 𝜈 = 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ
is associative; that is:
( (
))
( (
( ) ((
)(
))
))
= 𝚤 𝚥 (ℓ𝚤) ( 𝚥ℓ) (ℓ𝒌)ℓ = . . . = −𝒌 .
(2.92)
𝚤 𝚥 ℓ𝚤 𝚥ℓ ℓ𝒌 (ℓ)
It defines the real 𝔠𝔩(4, 2) pseudoscalar (or volume form) 𝑀 (4, 2):
(
)
𝐿 𝚤 𝐿 𝚥 𝐿 ℓ𝚤 𝐿 𝚥ℓ 𝐿 ℓ𝒌 𝐿 ℓ =: 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 𝑚 4 = 𝐿 −𝒌 =: 𝑀 (4, 2) = 𝐸 .

(2.93)

Note that:
1. This significant observation — that the product of the six imaginary OS units 𝜈
is associative — was first made in Cohl Furey’s dissertation [99].
2. The sign in Eq. (2.92) (or (2.93)) defines an orientation in R4,2 . This orientation
is reversed by any odd permutation of the elements and preserved by any even
permutation.
(
)
3. Since 𝐸 2 = 𝑀 2 (4, 2) = −1, the 𝔠𝔩(4, 2) pseudoscalar defines a complex structure on the 8-dimensional spinor space, a topic we will explore in more detail
later.
4. There are three pairs of OS units whose product equals −𝒌, specifically (ℓ𝚤) ( 𝚥ℓ) =
(ℓ𝒌)ℓ = 𝚥𝚤 = −𝒌. One notices that the corresponding (commuting!) matrices
𝑚 12 , 𝑚 34 , and 𝑚 50 = −𝑚 05 are trace-orthogonal to each other as well as to 𝐸.
This will also be discussed in more detail later.
□

2.3 Diagonalizing the Complex Structure of 𝖈𝖑(4, 2) in Spinor
Space: Insight from the 𝖈𝖑(2) Case
We observe that the 𝔠𝔩(4, 2) pseudoscalar (volume form) 𝐸 = 𝑀 (4, 2) generates the
𝔲(1) center of:3
3 For the extension of this construction to the group level, see Appendix 2.6.

## PDF page 50

36 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩(4, 2) ,
(2.94)
(
)
meaning that it commutes with every generator 𝑚 𝜇𝜈 = −𝑚 𝜈 𝜇 of 𝔰𝔲(2, 2) 
𝔰𝔬(4, 2):
[
]
(
)
𝑚 𝜇𝜈 = 𝑚 𝜇 𝑚 𝜈 , 𝐸 = 0 ,
(2.95)
for all 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)); to verify this commutation
relation, using Proposition 2.1, it suffices to follow a procedure analogous to that
described in Eq. (2.85). Thus, any representation
space
(
) 𝔖 of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2),
spanned by the fifteen 8 × 8 matrices 𝑚 𝜇𝜈 = −𝑚 𝜈 𝜇 , necessarily decomposes into
eigenspaces of 𝐸.
As an anti-Hermitian — and in particular real skewsymmetric — matrix, the
𝔠𝔩(4, 2) volume form 𝐸 = 𝑀 (4, 2) reads as:
( (
( (
))
))
( (
( (
))
))
𝐸 𝑥 = 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 𝑥)
= 𝚤 𝚥 ℓ𝚤 𝚥ℓ ℓ𝒌 (ℓ 𝑥)
=

⨁

(𝐸 1𝒌 + 𝐸 05 + 𝐸 12 + 𝐸 34 ) 𝑥 , (2.96)

where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)). For the convention
1.2.5.2.

⨁

(. . . ), see Sect.

Remark 2.10 Rather than directly computing the matrix realization of the volume
form 𝐸 = 𝑀 (4, 2) as carried out above — i.e., by substituting 𝑥 with any of the
split-octonion units (and in fact with all of them) and consulting the multiplication
table (2.47), one may employ a more refined approach by invoking the associativity
property established in Remark (2.9); this second approch will be of particular utility
in subsequent arguments. Specifically, by means of the associativity property (2.92),
Eq. (2.96) can be recast in the following form:
( (
( (
))
))
( (
( (
))
))
𝐸 𝑥 = 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 𝑥)
= 𝚤 𝚥 ℓ𝚤 𝚥ℓ ℓ𝒌 (ℓ 𝑥)
[ ( (

(

(

= 𝚤 𝚥 ℓ𝚤 𝚥ℓ ℓ𝒌 (ℓ)

))

))]
𝑥

(as discussed below!)

= −𝒌𝑥
⨁
(𝐸 1𝒌 + 𝐸 05 + 𝐸 12 + 𝐸 34 ) 𝑥 , (2.97)
=
again, for 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)). The passage to the second line
is immediate when choosing 𝑥 = 1( . To further
illustrate its validity, let us instead
)
consider the nontrivial case 𝑥 = 𝒌 = 𝚤 𝚥 . Then, we obtain:

## PDF page 51

2.3 Diagonalizing the Complex Structure of 𝔠𝔩 (4, 2) in Spinor Space: Insight from the 𝔠𝔩 (2) Case
37

(

(

(

(

𝐸 (𝚤 𝚥) = 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 (𝚤 𝚥))
⏟⏞⏞⏟

))

))

[ (
)] )
( (
))
= 𝚤 𝚥 ℓ𝚤 𝚥ℓ ℓ𝒌 ℓ (𝚤 𝚥)
(

=𝑥

(
by Remarks 2.9 and 2.1

=𝚤 𝚥

[

)] )
( (
(
))
(𝚤 𝚥) ℓ𝚤 𝚥ℓ ℓ𝒌 (ℓ)

by Remark 2.9

(
)
= 𝚤 𝚥 [−𝒌]

by quaternion associativity and Remark 2.1

= − 𝒌 (𝚤 𝚥) .
⏟⏞⏞⏟

(2.98)

=𝑥

All remaining cases can be justified analogously by the same procedure.

□

We note that 𝐸 = 𝑀 (4, 2) is diagonalizable only over a complex basis, with
eigenvalues ±i, since:
𝐸 2 𝑥 = 𝑀 2 (4, 2) 𝑥 = −𝒌 (−𝒌 𝑥) = ( 𝒌) 2 𝑥 = −1 𝑥 ,

(2.99)

according to the preceding discussion and Proposition 2.1 and of course Remark
2.4.4 Then, in view of Eq. (2.95), any representation space 𝔖 of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2)
splits into two 4-dimensional chiral subspaces:
𝔖 = 𝔖+ ⊕ 𝔖− ,

(2.100)

(
)
where the complex-conjugate semispinor chiral subspaces 𝔖± = 𝔖∓ consist of
eigenvectors of 𝐸 with eigenvalues ±i, respectively; this point will be discussed
explicitly later.
Remark 2.11 Completing the discussion begun by Eq. (2.95),
note first
that the
(
)
pseudoscalar 𝐸 lies in the center of 𝔲(2, 2)  𝔰𝔲(2,
2)

𝔰𝔬(4,
2)
⊕
𝔲(1).
In
(
)
particular, it commutes with every generator 𝑚 𝜇𝜈 = −𝑚 𝜈 𝜇 of 𝔰𝔲(2, 2). As a
4 It is perhaps worthwhile noting that a real skewsymmetric matrix, such as 𝐸 (that is, 𝐸 ⊤ = −𝐸),

is not fully diagonalizable over R. However, if the matrix has an even dimension, it can be brought
to a block-diagonal form via an orthogonal transformation. This property is clearly illustrated by
the matrix representation (2.96) of 𝐸:
0 1
© −1 0
ª
®
®
.
®
..
Eq. (2.96) = ­,
®
®
0 1®
−1 0¬8×8
«
where each of the four 2 × 2 blocks corresponds to a pair of imaginary eigenvalues ±i. In contrast,
over C, 𝐸 is fully diagonalizable via a similarity transformation 𝑇:
𝑇 −1 𝐸𝑇 = diag(+i, −i, +i, −i, +i, −i, +i, −i) .
This confirms that full diagonalization is only possible on a complex basis. The matrix remains
8 × 8 in dimension, but it is now fully diagonal over C. For further details, see Ref. [100].

## PDF page 52

38 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

result, the eigenspaces 𝔖± of 𝐸, respectively with eigenvalues ±i (to be shown
explicitly later), are separately invariant under 𝔰𝔲(2, 2). We will see that each 𝔖± in
fact carries an irreducible 𝔰𝔲(2, 2) representation.
On the other hand, because 𝐸 itself also generates the central 𝔲(1) factor in 𝔲(2, 2)
and acts on each 𝔖± by a fixed scalar, the full algebra 𝔲(2, 2) likewise preserves these
subspaces. Thus, the 8-dimensional 𝔲(2, 2)-module splits cleanly into two invariant
4-dimensional pieces, 𝔖 = 𝔖+ ⊕ 𝔖− . Each 𝔖± furnishes an irreducible semispinor
representation of 𝔲(2, 2).
□
In the sequel, we will systematically present the similarity transformation that
simultaneously diagonalizes the 𝔲(1) generator 𝐸 (2.96) along with a traceorthogonal basis5 of the Cartan elements of the maximal compact Lie subalgebra
𝔰𝔬(2) ⊕ 𝔰𝔬(4) ⊂ 𝔰𝔬(4, 2):6
⨁
(𝐸 𝒌 1 − 𝐸 05 + 𝐸 12 + 𝐸 34 ) 𝑥 ,
𝑚 05 𝑥 = 𝑚 0 (𝑚 5 𝑥) = 𝚤( 𝚥 𝑥) =
(2.101)
𝑚 12 𝑥 = 𝑚 1 (𝑚 2 𝑥) = ℓ𝚤( 𝚥ℓ 𝑥) =

⨁

(𝐸 1𝒌 − 𝐸 05 + 𝐸 12 − 𝐸 34 ) 𝑥 ,

(2.102)

𝑚 34 𝑥 = 𝑚 3 (𝑚 4 𝑥) = ℓ𝒌 (ℓ 𝑥) =

⨁

(𝐸 1𝒌 − 𝐸 05 − 𝐸 12 + 𝐸 34 ) 𝑥 ,

(2.103)

where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)). Again, for the convention
Sect. 1.2.5.2. Note that:

⨁

(. . . ), see

1. These equations can be readily checked by substituting 𝑥 with any (indeed, with
each) of the split-octonion units and referring to the multiplication table (2.47).
2. The product of the three Cartan elements (2.101)-(2.103) reconstructs the Clifford pseudoscalar (2.96), which serves as the generator of the 𝔲(1) center of
𝔲(2, 2).
(
)2
3. Since the matrices 𝑚 𝜇𝜈 (2.101)-(2.103) are skewsymmetric, with 𝑚 𝜇𝜈 = −1,7
they have pure imaginary eigenvalues.
4. These matrices can be diagonalized simultaneously with the complex structure
𝐸 (2.96), in a complex chiral basis, since:
[
[
]
[
]
] [
]
𝑚 05 , 𝑚 12 = 𝑚 12 , 𝑚 34 = · · · = 𝑚 05 , 𝐸 = · · · = 𝑚 34 , 𝐸 = 0 . (2.104)
We shall discuss this diagonalization procedure in detail in the next section.

5 See Remark 2.7.
6 For the structure of the maximal compact subalgebra of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2), see Appendix 2.7.
7 This identity can be verified by a procedure analogous to that used in Eq. (2.91).

## PDF page 53

2.3 Diagonalizing the Complex Structure of 𝔠𝔩 (4, 2) in Spinor Space: Insight from the 𝔠𝔩 (2) Case
39

2.3.1 The 𝖈𝖑(2) Case as a Prototype
Since all four (commuting) 8×8 skewsymmetric matrices 𝐸 (2.96), 𝑚 05 (2.101), 𝑚 12
(2.102), and 𝑚 34 (2.103) can be expressed as direct sums of 2×2 skewsymmetric matrices ±𝐸 𝐴𝐵 for the same set of index pairs 𝐴, 𝐵 = 1, 𝒌, 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ or more
conveniently 𝐴, 𝐵 = 1, 𝒌, 0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)), the simultaneous
diagonalization problem of 𝐸, 𝑚 05 , 𝑚 12 , and 𝑚 34 reduces to a 2-dimensional case
within the framework of the Clifford algebra 𝔠𝔩(2) := 𝔠𝔩(2, 0).8 The 𝔠𝔩(2) Majorana
(or real) basis {𝑚 1 , 𝑚 2 } and the chiral one {𝜎1 , 𝜎2 } can be chosen, respectively, as:
(
𝑚 1 = 𝜎3 =

)
1 0
,
0 −1

(
𝑚 2 = 𝜎1 =
=⇒

01
10

)

(
)
0 1
,
𝜖 = 𝑀 (2) := 𝑚 1 𝑚 2 = i𝜎2 =
−1 0
⏟
⏞⏞
⏟

(2.105)

corresponding volume form

(
𝜎1 ,

𝜎2 = −i𝜖

=⇒

𝜔(2) := 𝜎1 𝜎2
⏟
⏞⏞
⏟

= i𝜎3 =

)
i 0
.
0 −i

(2.106)

corresponding volume form

Here, we must emphasize that {𝑚 1 , 𝑚 2 } and {𝜎1 , 𝜎2 } are two bases in the same
real Clifford algebra 𝔠𝔩(2); no complexification is needed. As a matter of fact, the
following unitary similarity transformation relates them:
𝜎𝜈¤ = 𝑉 𝑚 𝜈¤ 𝑉 −1 ,

𝜈¤ = 1, 2 ,

(2.107)

with:9

8 This algebra represents the lowest-dimensional member of the signature-two Clifford algebras

𝔠𝔩 (𝑛 + 1, 𝑛 − 1), 𝑛 = 1, 2, . . . , in Cartan’s classification.
9 Note that the Pauli matrices satisfy the algebraic identity:
𝜎𝑖 𝜎 𝑗 = 𝛿𝑖 𝑗 1 + i𝜀𝑖 𝑗 𝑘 𝜎𝑘 ,
where 𝑖, 𝑗, 𝑘 = 1, 2, 3, 𝛿𝑖 𝑗 is the Kronecker delta and 𝜀𝑖 𝑗 𝑘 is the Levi-Civita symbol. From this,
it follows that:
𝜎 2𝑛
𝑗 = 1,

𝜎 2𝑛+1
= 𝜎𝑗 ,
𝑗

for all 𝑛 ∈ N. Using these properties, the matrix exponential of any Pauli matrix takes the form:
(∞
)
(∞
)
∞
∑︁ (−i𝜃 ) 2𝑘
∑︁ (−i𝜃 ) 2𝑘+1
∑︁ (−i𝜃 ) 𝑛 𝜎 𝑛𝑗
=
1+
𝜎 𝑗 = cos 𝜃 1 − i sin 𝜃 𝜎 𝑗 ,
𝑒 −i𝜃 𝜎 𝑗 =
𝑛!
(2𝑘 )!
(2𝑘 + 1)!
𝑘=0
𝑘=0
𝑛=0
which is valid for any 𝑗 = 1, 2, 3 and 𝜃 ∈ R.

## PDF page 54

40 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2
𝜋

𝜋

)
1(
1 − i𝜎1 − 𝜖 − i𝜎3
2(
)
1 1 − i −1 − i
=
,
2 1−i 1+i

𝑉 = 𝑒 − 4 𝜖 𝑒 −i 4 𝜎3 =

𝑉𝑉 ∗ = 𝑉 ∗𝑉 = 1

=⇒

𝑉 ∗ = 𝑉 −1 ,

(2.108)

where, in the present context, the superscript ‘∗ ’ denotes the Hermitian conjugate,
⊤
defined as 𝑉 ∗ = 𝑉 = 𝑉 ⊤ , with the ‘ ’ symbol representing the complex conjugate,
⊤
and the superscript
( + ) ‘ ’ indicating the transpose.
( +)
𝜉
𝜓
Let 𝜉 = − denote the Majorana (real) spinors, and 𝜓 = − = 𝑉 𝜉 the chiral
𝜉
𝜓
spinors in the context of the 𝔠𝔩(2). We then observe that the right- and left-handed
components, denoted by 𝜓 ± , of the chiral spinor satisfy:
(
1 ± 𝜎3 )
𝜓,
(2.109)
𝜓± =
2
and, more importantly:
(
)
𝜔(2) 𝜓 ± = i𝜎3 𝜓 ± = ±i𝜓 ± .

(2.110)

Then, 𝜔(2) naturally plays the role of the “chirality operator”, distinguishing the
right- from the left-handed spinor components.
The reality of the Majorana spinor 𝜉 is encapsulated in the requirement that any
unitary transformation, 𝜓 = 𝑉 𝜉, preserves its invariance under charge conjugation
— denoted by the superscript ‘𝑐 ’ — so that the charge conjugate of the transformed
spinor coincides with itself, 𝜓 𝑐 = 𝜓. By definition, the charge conjugate of a spinor
is given by:
𝜓 𝑐 := 𝐶 𝜓 ,

(2.111)

where the charge conjugation matrix 𝐶 naturally swaps 𝜓 + and 𝜓 − , preserving the
chirality structure. To ensure consistency, 𝐶 must satisfy the following condition:
𝐶 𝜎 𝜈¤ = 𝜎𝜈¤ 𝐶 ,

𝜈¤ = 1, 2 .

(2.112)

The former identity implies that 𝐶 should commute with the real 𝔠𝔩(2) generators and
anticommute with the imaginary ones. We notice that the matrix 𝐶 = 𝜚2 𝜎1 satisfies
this condition for any choice of the phase factor 𝜚 2 ; the reason for the exponent ‘2’
in 𝜚2 will be clarified in the sequel (see the convention given above Eq. (2.119)).
Considering the unitary basis transformation defined by the matrix 𝑉, such that
𝜓𝑉 = 𝑉𝜓 and 𝜎𝜈𝑉¤ = 𝑉 𝜎𝜈¤ 𝑉 −1 , Eq. (2.111) becomes:
Eq. (2.111) : 𝜓 𝑐 = 𝐶 𝜓

=⇒

)⊤
(
𝜓𝑉𝑐 = 𝐶𝑉 𝜓 𝑉 = 𝐶𝑉 𝑉 𝜓 = 𝐶𝑉 𝑉 −1 𝜓 .
(2.113)

## PDF page 55

2.3 Diagonalizing the Complex Structure of 𝔠𝔩 (4, 2) in Spinor Space: Insight from the 𝔠𝔩 (2) Case
41

On the other hand, as previously mentioned, the reality condition of the Majorana
spinor 𝜉 ensures that under any unitary transformation 𝜓 = 𝑉 𝜉, we have:
)
(
)
(
)
(
=⇒ 𝜓𝑉𝑐 = 𝑉 𝐶 𝜓 .
𝜓 𝑐 = 𝐶 𝜓 = 𝜓 , and similarly 𝜓𝑉𝑐 = 𝜓𝑉 = 𝑉 𝜓
(2.114)
Equating the two expressions for 𝜓𝑉𝑐 , we obtain:
(
)⊤
𝐶𝑉 𝑉 −1 𝜓 = 𝑉 𝐶 𝜓 .

(2.115)

Since this must hold for all 𝜓, the corresponding transformation law for the charge
conjugation matrix follows:
𝐶𝑉 = 𝑉 𝐶 𝑉 ⊤ .

(2.116)

In the original (Majorana or real) basis 𝜉, however, the charge conjugation matrix
𝐶 is simply the identity matrix, so that:
𝜉𝑐 = 𝜉 .

(2.117)

We then apply the transformation law (2.116) for the charge conjugation matrix to
determine 𝐶𝑉 for 𝜓 = 𝑉 𝜉. This yields:
𝜋

𝜋

𝜋

𝐶𝑉 = 𝑉 𝑉 ⊤ = 𝑒 − 4 𝜖 𝑒 −i 2 𝜎3 𝑒 4 𝜖 = −i𝜎1 ,

(2.118)

which is consistent with the structure of the Majorana spinor under the new basis.
Notably, for any 𝜚 ∈ C satisfying 𝜚 𝜚 = 1, the matrix 𝑈 = 𝜚𝑉 retains the same
intertwining properties as 𝑉 in Eqs. (2.107) and (2.108). Choosing 𝜚 = 𝑒 i 𝜋/4 , we
obtain:
(
) ( ) ( +)
1 1 −i 𝜉 +
𝜓
i 𝜋4
𝑈 = 𝑒 𝑉 =⇒ 𝑈𝜉 = √
(2.119)
− = 𝜓− ,
1
i
𝜉
2
with:
)
1 (
𝜓 ± = √ 𝜉 + ∓ i𝜉 − ,
2

and 𝐶𝑈 = 𝑈𝑈 ⊤ = 𝜎1 .

(2.120)

More generally, the involutivity property (𝜓 𝑐 ) 𝑐 = 𝜓 implies that the charge conjugation matrix must satisfy 𝐶𝐶 = 1.
(
)
Remark 2.12 The reduced U(1) representation 𝑒 i𝜑 ∈ U(1), 𝜉 ± ↦−→ 𝑒 ±i𝜑/2 𝜉 ± corresponds to a real rotation in the (𝜎1 , 𝜎2 )-plane:
𝑒

i𝜎3 𝜑2

𝜎1 𝑒

−i𝜎3 𝜑2

)
0 𝑒 i𝜑
= −i𝜑
= cos 𝜑 𝜎1 − sin 𝜑 𝜎2 ,
𝑒
0
(

(2.121)

## PDF page 56

42 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2
𝜑

𝜑

𝑒 i𝜎3 2 𝜎2 𝑒 −i𝜎3 2 =

(

)
−i𝑒 i𝜑
= sin 𝜑 𝜎1 + cos 𝜑 𝜎2 .
i𝑒 −i𝜑 0
0

(2.122)
□

Remark 2.13 It can be visualized that (2.108) and hence (2.119) generate a finite
cyclic group. Indeed, we have:
𝑉 2 = −𝑉 ∗ = −𝑉 −1

=⇒

𝑉 3 = −1

and 𝑈 24 = 1 .

(2.123)
□

We shall see that the transformation relating the Majorana (real) and chiral basis
of 𝔠𝔩(4, 2), the case of interest, obeys the same relations.

2.4 Unitary Transformation from Real to a Diagonal Compact
Cartan Basis of 𝖘𝖚(2, 2)  𝖘𝖔(4, 2)
Outline of this section: Diagonalizing the complex structure generated by the volume
form 𝐸 = 𝑀 (4, 2) (2.96) of 𝔠𝔩(4, 2), we split the spinor space 𝔖 ( R8 ) into two
complex conjugate, chiral subspaces 𝔖+ and 𝔖− , each carrying a 4-dimensional
(complex)
( irreducible) representation (IR) of the conformal Lie algebra 𝔰𝔲(2, 2) 
𝔰𝔬(4, 2) ⊂ 𝔠𝔩(4, 2) and thus also the corresponding IR of 𝔲(2, 2); see Remark
2.11 for this latter point, while a more systematic discussion of these representations
will be given in the next chapter. The resulting chiral basis of 8 × 8 complex matrices
— the complex counterpart of the 8 × 8 real matrices 𝑚 0 , 𝑚 5 , 𝑚 1 , . . . , 𝑚 4 , namely:
Γ0 := Γ𝚤 ,

Γ5 := Γ 𝚥 ,

Γ1 := Γℓ𝚤 ,

Γ2 := Γ 𝚥ℓ ,

Γ3 := 𝐿 ℓ𝒌 ,

and

Γ4 := Γℓ ,
(2.124)

can be further restricted by diagonalizing a Cartan basis among the 𝔰𝔲(2, 2) 
𝔰𝔬(4, 2) generators:
Γ𝜇𝜈 :=

]
1[
Γ𝜇 , Γ𝜈 ,
2

(2.125)

where 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4 (see Eq. (2.60)-(2.62)). There are two types of such bases:
(
)
1. One, that belongs to the Lie algebra (𝔰𝔬(2) ⊕ 𝔰𝔬(4))  𝔲(1) ⊕ 𝔰𝔲(2) ⊕ 𝔰𝔲(2)
of the maximal compact subgroup S U(2) × U(2) of SU(2, 2).
2. Another one that involves generators like Γ03 and Γ45 on noncompact boost
transformations.
Here, we shall restrict attention to the compact Cartan basis with generators Γ05 ,
Γ12 , and Γ34 — the chiral counterpart of 𝑚 05 (2.101), 𝑚 12 (2.102), and 𝑚 34 (2.103),
respectively.

## PDF page 57

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
43

Let us begin by noting that the product of each pair of the real matrices 𝑚 05 , 𝑚 12 ,
and 𝑚 34 gives rise to the (Hermitian) volume forms of either 𝔠𝔩(2, 2) or 𝔠𝔩(4, 0).
These volume forms are diagonal and commute with each individual 𝐸 𝐴𝐵 appearing
in (2.96) and (2.101)-(2.103). Indeed, we have:
( (
(
)
)) ⨁
𝑀12 (2, 2) 𝑥 = 𝑚 05 (𝑚 12 𝑥) = 𝚤 𝚥 ℓ𝚤( 𝚥ℓ 𝑥) =
( 11𝒌 − 105 − 112 + 134 ) 𝑥 ,
(2.126)
( (
(
)
)) ⨁
𝑀34 (2, 2) 𝑥 = 𝑚 05 (𝑚 34 𝑥) = 𝚤 𝚥 ℓ𝒌 (ℓ 𝑥) =
( 11𝒌 − 105 + 112 − 134 ) 𝑥 ,
(2.127)
( (
(
)
)) ⨁
𝑀 (4, 0) 𝑥 = 𝑚 12 (𝑚 43 𝑥) = ℓ𝚤 𝚥ℓ ℓ(ℓ𝒌 𝑥) =
( 11𝒌 + 105 − 112 − 134 ) 𝑥 ,
(2.128)
where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)) and the 1 𝐴𝐵⨁represents the unit 2 × 2
matrices defined in Eq. (2.77). Again, for the convention
(. . . ), see Sect. 1.2.5.2.
The above results can be verified by substituting 𝑥 with any of the split-octonion
units (and in fact with all of them) and consulting the multiplication table (2.47).
Regarding the above construction, we observe that:
1. The following relation holds:
(
)
𝑀 (4, 0) 𝑥 = 𝑀12 (2, 2) 𝑀34 (2, 2) 𝑥 .

(2.129)

To verify this relation, it is sufficient — by Proposition 2.1 — to follow a
procedure analogous to that in Eq. (2.85).
2. The Lorentz 𝔠𝔩(3, 1) volume form is:
( (
(
)
))
𝐸 𝐿 𝑥 = 𝑀 (3, 1) 𝑥 = 𝑚 03 (𝑚 12 𝑥) = 𝚤 ℓ𝒌 ℓ𝚤( 𝚥ℓ 𝑥)
⨁
=
(𝐸 11 − 𝐸 04 + 𝐸 53 − 𝐸 2𝒌 ) 𝑥 , (2.130)
where, once again, it can be verified by substituting 𝑥 with any of the splitoctonion units (see Eqs. (2.60)-(2.62)) and consulting the multiplication table
(2.47). We observe that the aforementioned volume forms 𝑀12 (2, 2) and 𝑀 (4, 0)
do not commute with the Lorentz one 𝑀 (3, 1):
[
]
[
]
𝑀12 (2, 2), 𝑀 (3, 1) 𝑥 ≠ 0 , and 𝑀 (4, 0), 𝑀 (3, 1) 𝑥 ≠ 0 .
(2.131)
Once again, verification of these results reduces — by Proposition 2.1 — to
following a procedure analogous to that in Eq. (2.85).

## PDF page 58

44 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

Happily, there exists a third-order10 diagonal element 𝐷 ∈ 𝔠𝔩(4, 2) that anticommutes with the Cartan elements 𝑚 05 , 𝑚 12 , and 𝑚 34 of the maximal compact
Lie subalgebra 𝔰𝔬(2) ⊕ 𝔰𝔬(4) ⊂ 𝔰𝔬(4, 2), and consequently commutes with the
fourth-order diagonal volume forms given in Eq. (2.126)-(2.128):
(
)
(
) ⨁
𝐷 𝑥 = 𝑚 5 𝑚 4 (𝑚 2 𝑥) = 𝚥 ℓ ( 𝚥ℓ 𝑥) =
(𝐷 1𝒌 − 𝐷 05 − 𝐷 12 − 𝐷 34 ) 𝑥
⨁
=
( 11,5,2,4 − 1𝒌,0,1,3 ) 𝑥
,
⏟
⏞⏞
⏟
as a by-product of Sect. 1.2.5.2 (see Eq. (1.6))

(2.132)
such that:
{

[

}
{
}
{
}
{
}
𝐷, 𝑚 05 𝑥 = 𝐷, 𝑚 12 𝑥 = 𝐷, 𝑚 34 𝑥 = 𝐷, 𝐸 𝑥 = 0 ,

(2.133)

]
[
]
[
]
𝐷, 𝑀12 (2, 2) 𝑥 = 𝐷, 𝑀34 (2, 2) 𝑥 = 𝐷, 𝑀 (2, 2) 𝑥 = 0 ,

(2.134)

where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), 𝐷 𝐴𝐵 denotes the 2 × 2 matrices defined
in Eq. (2.78), while 1 𝐴,𝐵,𝐶,𝐷 represents the 4 × 4 identity matrix corresponding
to its indices. To verify relation (2.132), one simply substitutes 𝑥 with any of the
split-octonion units (and in fact with all of them) and refers to the multiplication
table (2.47). The verification of the (anti)commutation relations, however, relies on
Proposition 2.1 and proceeds analogously to the method outlined in Eq. (2.85).
Remark 2.14 In connection with the above, we note that:
1. The representation of (2.132) as a sum of 2 × 2 diagonal matrices 𝐷 𝐴𝐵 is not
unique. Actually, as a by-product of the discussion in Sect. 1.2.5.2 (in particular,
Eq. (1.6)), we may write, for instance:
⨁(
) ⨁(
)
𝐷 1𝒌 − 𝐷 05 =
𝐷 10 − 𝐷 𝒌5 ,
⨁(
) ⨁(
)
𝐷 12 + 𝐷 34 =
𝐷 14 − 𝐷 23 , etc.
(2.135)
2. Besides the representation of (2.132), it is important to emphasize that the choice
of the third-order diagonal matrix 𝐷 = 𝑚 5 𝑚 4 𝑚 2 in (2.132) is not unique either.
This choice corresponds to triples of imaginary split-octonion units that gener10 The Clifford algebra 𝔠𝔩 (𝑙, 𝑟 ) admits a natural basis for its 2𝑛=𝑙+𝑟 -dimensional vector space,
consisting of all possible products of its distinct anticommuting generators 𝑚1 , . . . , 𝑚𝑛 . These
basis elements can be systematically arranged according to the standard grading of the associated
Grassmann algebra Λ⊗ = Λ0 ⊕ Λ1 ⊕ · · · ⊕ Λ𝑛 , where each subspace Λ 𝑘 consists of all products
of exactly 𝑘 distinct generators 𝑚, while Λ0 corresponds to the identity element
1 (i.e., no 𝑚( )
𝑛
𝑘
generators at all). The dimension of Λ is given by the binomial coefficient
, which counts the
𝑘
number of ways to choose 𝑘 generators from 𝑛. We refer informally to elements of Λ 𝑘 as elements
of order 𝑘.

## PDF page 59

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
45

ate an associative subalgebra within the larger, nonassociative algebra of split
octonions. For a more detailed discussion, see Appendix 2.8.
□
Remark 2.15 (necessity of the operator 𝐷 and resolution of the degeneracy)
Let 𝔖  R8 be the spinor representation space of 𝔲(2, 2) ⊂ 𝔠𝔩(4, 2). We have
already introduced the four mutually commuting 8 × 8 skewsymmetric operators:
𝐸 (see Eq. (2.96)) ,

𝑚 05 (Eq. (2.101)) ,

𝑚 12 (Eq. (2.102)) ,

𝑚 34 (Eq. (2.103)) ,
(2.136)

where 𝐸 generates the 𝔲(1) center of 𝔲(2, 2), and 𝑚 05 , 𝑚 12 , and 𝑚 34 form a traceorthogonal Cartan basis of the maximal compact subalgebra 𝔰𝔬(2) ⊕ 𝔰𝔬(4) ⊂
𝔰𝔬(4, 2), such that:
1. Each operator can be expressed as a direct sum of four 2 × 2 skewsymmetric
blocks ±𝐸 𝐴𝐵 , with the same set of index pairs 𝐴, 𝐵 = 1, 𝒌, 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌, ℓ or
more conveniently 𝐴, 𝐵 = 1, 𝒌, 0, 5, 1, 2, 3, 4 (see Eqs. (2.60)-(2.62)). That is:
⨁
⨁
±𝐸 𝐴𝐵 , . . . ,
(2.137)
±𝐸 𝐴𝐵 , 𝑚 05 =
𝐸=
𝐴,𝐵

𝐴,𝐵

where each block acts independently.
2. The joint eigenspace of a given quadruple of eigenvalues (𝜇 𝐸 , 𝜇05 , 𝜇12 , 𝜇34 ):
{
E(𝜇 𝐸 , 𝜇1 , 𝜇2 , 𝜇3 ) := 𝑣 ∈ 𝔖 ; 𝐸𝑣 = 𝜇 𝐸 𝑣 , 𝑚 05 𝑣 = 𝜇05 𝑣 ,
}
𝑚 12 𝑣 = 𝜇12 𝑣 , 𝑚 34 𝑣 = 𝜇34 𝑣 ,
(2.138)
is then 2-dimensional over R (see footnote 4). Indeed, each 2 × 2 block 𝐸 𝐴𝐵
corresponds to exactly one eigenvalue quadruple and the 2-dimensionality arises
because each block is spanned by two independent vectors, for example:
( )
( )
1
1
𝑣1 =
, 𝑣2 =
.
(2.139)
1
−1
However, there is no canonical way to distinguish these individual vectors (say 𝑣1
and 𝑣2 ) inside this joint eigenspace using 𝐸, 𝑚 05 , 𝑚 12 , and 𝑚 34 alone, producing
an intrinsic twofold degeneracy.
To resolve this degeneracy, one requires an extra operator that acts within each
2-dimensional joint eigenspace and distinguishes the two vectors. This operator is
indeed the third-order Clifford element 𝐷 ∈ 𝔠𝔩(4, 2) (see Eq. (2.132)), which satisfies
the anticommutation relations (2.133). Since 𝐷 anticommutes with 𝐸, 𝑚 05 , 𝑚 12 , and
𝑚 34 , its action on any vector 𝑣 in a joint eigenspace with eigenvalues 𝜇 𝑋 satisfies:
𝑋 (𝐷𝑣) = −𝐷 (𝑋𝑣) = −𝜇 𝑋 (𝐷𝑣) ,

for

𝑋 = 𝐸 , 𝑚 05 , 𝑚 12 , 𝑚 34 ,

(2.140)

## PDF page 60

46 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

where 𝜇 𝑋 are the eigenvalues of 𝑣 under 𝑋. Since each joint eigenspace defines a
2-dimensional invariant plane under the action of 𝐸, 𝑚 05 , 𝑚 12 , 𝑚 34 , flipping the signs
of all eigenvalues does not move a vector outside this plane. Consequently, 𝐷𝑣 lies
in the same 2-dimensional joint eigenspace as 𝑣, but is linearly independent of 𝑣; if
𝐷𝑣 were proportional to 𝑣, i.e., 𝐷𝑣 = 𝛼𝑣 for some nonzero scalar 𝛼, then acting with
any 𝑋 = 𝐸, 𝑚 05 , 𝑚 12 , 𝑚 34 would yield 𝜇 𝑋 = −𝜇 𝑋 , forcing 𝜇 𝑋 = 0, which does not
occur for the nontrivial 2 × 2 blocks under consideration. Therefore, 𝐷 automatically
generates a second independent vector in each joint eigenspace, completely resolving
the intrinsic twofold degeneracy. Concretely, 𝐷 acts like a Pauli-𝜎3 operator within
each 2 × 2 block, splitting the two states into eigenvectors with distinct eigenvalues:
(
)( ) ( )
1 0 1
1
𝐷 𝐴𝐵 𝑣1 =
=
= 𝑣2 ,
(2.141)
0 −1 1
−1
(
)( ) ( )
1 0
1
1
𝐷 𝐴𝐵 𝑣2 =
=
= 𝑣1 .
(2.142)
0 −1 −1
1
In addition, 𝐷 commutes (see Eq. (2.134)) with all fourth-order volume forms
𝑀12 (2, 2) (2.126), 𝑀34 (2, 2) (2.127), and 𝑀 (4, 0) (2.128), ensuring that it preserves
the previously obtained block decomposition.
Accordingly, after including 𝐷, the extended set of (anti)commuting operators:
}
{
𝐸, 𝑚 05 , 𝑚 12 , 𝑚 34 , 𝐷
(2.143)
provides a complete, nondegenerate labeling of the spinor basis of 𝔖.

□

Proposition 2.2 The operators 𝐸 (2.96), 𝐷 (2.132), and their product 𝑆 := 𝐷 𝐸
obey the same multiplication laws as their 2 × 2 matrix components (see Remark
2.5):
⨁(
)
𝑆 = 𝐷 𝐸 = −𝐸 𝐷 =
𝑆1𝒌 − 𝑆05 − 𝑆12 − 𝑆34 ,
(2.144)
𝐷 𝑆 = −𝑆 𝐷 = 𝐸 ,

𝐷 2 = 𝑆 2 = 18 = −𝐸 2 ,

and

(2.145)

generating a representation of the 𝔠𝔩(2) algebra. Here, 18 denotes the 8 × 8 identity
matrix. [We note that the labels of the indices of 𝐷 and 𝑆 will change in the chiral
basis.]
Proof Let us rewrite the above identities explicitly, one by one, by substituting the
operators 𝐸 (2.96) and 𝐷 (2.132) as they act from the left on 𝑥 ∈ Span{ 𝐴} (see Eqs.
(2.60)-(2.62)):
1. We begin with Eq. (2.144):
[ [

[

(

(

(

(

𝑆 𝑥 = 𝐷 (𝐸 𝑥) = 𝑚 5 𝑚 4 𝑚 2 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 𝑥)

))

)) ] ] ]
.

(2.146)

## PDF page 61

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
47

Applying Proposition 2.1 in the same way as Eq. (2.85), and consulting with the
miltiplication table (2.47), we find:
(
)
(
)
𝑆 𝑥 = 𝐷 (𝐸 𝑥) = −𝑚 0 𝑚 1 (𝑚 3 𝑥) = −𝚤 ℓ𝚤(ℓ𝒌 𝑥)
⨁
=
(𝑆1𝒌 − 𝑆05 − 𝑆12 − 𝑆34 ) 𝑥 .
(2.147)
For the convention
obtain:

⨁

(. . . ), see Sect. 1.2.5.2. Following a similar procedure, we

(
)
(
)
𝑆 𝑥 = −𝐸 (𝐷 𝑥) = −𝑚 0 𝑚 1 (𝑚 3 𝑥) = −𝚤 ℓ𝚤(ℓ𝒌 𝑥)
⨁
=
(𝑆1𝒌 − 𝑆05 − 𝑆12 − 𝑆34 ) 𝑥 .

(2.148)

Therefore, Eq. (2.144) follows.
2. Proceeding analogously, we find 𝐷 𝑆 = −𝑆 𝐷 = 𝐸; in particular:
( (
))
( (
))
𝐷 (𝑆 𝑥) = −𝑚 5 𝑚 4 𝑚 2 𝑚 0 𝑚 1 (𝑚 3 𝑥)
(

(

(

(

= 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 𝑥)

))

))
= 𝐸𝑥,

(2.149)

= 𝐸𝑥.

(2.150)

and:
(

(

(

(

))

(

(

))

−𝑆(𝐷 𝑥) = 𝑚 0 𝑚 1 𝑚 3 𝑚 5 𝑚 4 (𝑚 2 𝑥)
(

(

= 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 (𝑚 4 𝑥)

))
))

3. Lastly, by a similar argument, the second identity in Eq. (2.145) follows trivially:
𝐷 (𝐷 𝑥) = 𝑆(𝑆 𝑥) = 18 = −𝐸 (𝐸 𝑥) .

(2.151)
□

We now have all the ingredients to define the 𝔠𝔩(4, 2) analogue of the similarity
transformation (2.108) (or, more generally, (2.119)) corresponding to the 𝔠𝔩(2) case,
which simultaneously diagonalizes the 𝔲(1) generator 𝐸 (2.96) of the conformal
Lie algebra 𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1) and the trace-orthogonal Cartan elements
𝑚 05 (2.101), 𝑚 12 (2.102), and 𝑚 34 (2.103) of the maximal compact subalgebra
𝔰𝔬(2) ⊕ 𝔰𝔬(4) ⊂ 𝔰𝔬(4, 2)  𝔰𝔲(2, 2). The corresponding unitary transformation 𝑈
explicitly reads as:

## PDF page 62

48 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

𝜚 ∈ C,

𝑈 = 𝜚𝑉 ,
𝑉=𝑒

− 𝜋4 𝐸

𝑒

−i 𝜋4 𝐷

=

𝜚𝜚 = 1 ,
1
( 1 − i𝑆 − 𝐸 − i𝐷) ,
2

(
) 1
𝑉 ∗ = 𝑉 −1 = ( 1 + i𝑆 + 𝐸 + i𝐷) = −𝑉 2
2

=⇒

𝑉 3 = −18 ,

(2.152)

where, by construction, we have:
𝑈𝑈 ∗ = 𝑈 ∗𝑈 = 18 = 𝑉 ∗𝑉 = 𝑉𝑉 ∗ .

(2.153)

Note that the phase factor is chosen as 𝜚 = 𝑒 i 𝜋/4 so that the corresponding chargeconjugation matrix 𝐶 is real; this point will be clarified later.
To achieve our goal of simultaneous diagonalization of the aforementioned operators, there are two (semi)equivalent approaches:
−1 ,
1. First, we transform the operators and let the conjugated versions 𝑈𝐸𝑈
{
−1
𝑈𝑚 05𝑈 , . . . act on the original Majorana (real) basis 𝐴 = 1, 𝒌, 𝜈 ∈ 0 :=
}
𝚤, 5 := 𝚥, 1 := ℓ𝚤, 2 := 𝚥ℓ, 3 := ℓ𝒌 , 4 := ℓ .
2. Second, we leave the operators in their original form but instead transform the
basis, working with 𝑈 −1 𝐴, i.e., the chiral basis.

The two procedures are equivalent in the sense that the resulting matrix realizations
are similar; however, the meaning of the indices differs in each case. In what follows,
we present both approaches explicitly, beginning with the first.

2.4.1 Operator Transformation in the Majorana Basis
Under the linear operator 𝑈, the volume form 𝑀 (4, 2) = 𝐸 (2.96) transforms as:
(
)
𝜔(4, 2) = 𝑈 𝑀 (4, 2) 𝑈 −1 = 𝑉 𝑀 (4, 2) 𝑉 −1
(
)
= 𝑈 𝐸 𝑈 −1 = 𝑉 𝐸 𝑉 −1
𝜋

𝜋

𝜋

𝜋

= 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝐸 𝑒 i 4 𝐷 𝑒 4 𝐸
𝜋

𝜋

𝜋

= 𝐸 𝑒 − 4 𝐸 𝑒i 2 𝐷 𝑒 4 𝐸
= 12 𝐸 (1 − 𝐸) (i𝐷) (1 + 𝐸)
= i𝐸 𝐷 𝐸 = i𝐷 .

(2.154)

To obtain the above result, we consider the left multiplication on the split-octonion
units and invoke Proposition 2.2. Under the action of 𝜔(4, 2) on the split-octonion
units — namely, on the Majorana basis — the operator assumes the diagonal matrix
form (up to a factor of ‘i’) given in Eq. (2.132):
⨁
)
(
𝜔(4, 2) 𝑥 = 𝑈 𝐸 𝑈 −1 𝑥 = i𝐷 𝑥 = i
(𝐷 1𝒌 − 𝐷 05 − 𝐷 12 − 𝐷 34 ) 𝑥 , (2.155)

## PDF page 63

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
49

⨁
where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)). For the convention
(. . . ), refer to
Sect. 1.2.5.2.
We observe that the operator 𝐷 (2.132) commutes with the factors 𝑚 𝜇′ , for
𝜇′ = 5, 4, 2, while it anticommutes with the remaining factors 𝑚 𝜈 ′ , for 𝜈 ′ = 0, 1, 3.
By contrast, the operator 𝐸 anticommutes with all 𝑚 𝜈 , for 𝜈 = 0, 5, 1, 2, 3, 4. These
properties can once again be readily justified by substituting the operators as they act
from the left on 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), and then invoking Proposition
2.1 together with an argument analogous to that in Eq. (2.85); see also the proof
of Proposition 2.2. With these observations in hand and using Proposition 2.2, we
obtain:
(
)
Γ𝜇′ = 𝑈 𝑚 𝜇′ 𝑈 −1 = 𝑉 𝑚 𝜇′ 𝑉 −1
𝜋

𝜋

𝜋

𝜋

= 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝑚 𝜇′ 𝑒 i 4 𝐷 𝑒 4 𝐸
𝜋

= 𝑚 𝜇′ 𝑒 2 𝐸
= 𝑚 𝜇′ 𝐸 ,

for

𝜇′ = 5, 4, 2 ,

(2.156)

(
)
Γ𝜈 ′ = 𝑈 𝑚 𝜈 ′ 𝑈 −1 = 𝑉 𝑚 𝜈 ′ 𝑉 −1
𝜋

𝜋

𝜋

𝜋

= 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝑚 𝜈 ′ 𝑒 i 4 𝐷 𝑒 4 𝐸
𝜋

𝜋

𝜋

= 𝑚 𝜈′ 𝑒 4 𝐸 𝑒i 2 𝐷 𝑒 4 𝐸
= 12 𝑚 𝜈 ′ (1 + 𝐸) (i𝐷) (1 + 𝐸)
= i𝑚 𝜈 ′ 𝐷 ,

for

𝜈 ′ = 0, 1, 3 ,

(2.157)

and:
(
)
Γ𝜇′ 𝜈 ′ = 𝑈 𝑚 𝜇′ 𝜈 ′ 𝑈 −1 = 𝑉 𝑚 𝜇′ 𝜈 ′ 𝑉 −1
𝜋

𝜋

𝜋

𝜋

= 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝑚 𝜇′ 𝜈 ′ 𝑒 i 4 𝐷 𝑒 4 𝐸
𝜋

𝜋

𝜋

= 𝑚 𝜇′ 𝜈 ′ 𝑒 − 4 𝐸 𝑒 i 2 𝐷 𝑒 4 𝐸
= 12 𝑚 𝜇′ 𝜈 ′ (1 − 𝐸) (i𝐷) (1 + 𝐸)
= i𝑚 𝜇′ 𝜈 ′ 𝑆 ,

while

𝜇′ = 5, 4, 2 ,

and

𝜈 ′ = 0, 1, 3 ,

(2.158)

but, when 𝜇′ and 𝜈 ′ simultaneously belong to either 0, 1, 3 or 5, 4, 2, we have:
)
(
Γ𝜇′ 𝜈 ′ = 𝑈 𝑚 𝜇′ 𝜈 ′ 𝑈 −1 = 𝑉 𝑚 𝜇′ 𝜈 ′ 𝑉 −1
𝜋

𝜋

𝜋

𝜋

= 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝑚 𝜇′ 𝜈 ′ 𝑒 i 4 𝐷 𝑒 4 𝐸
= 𝑚 𝜇′ 𝜈 ′ ,

while

𝜇′ , 𝜈 ′ = 5, 4, 2 ,

or

𝜇′ , 𝜈 ′ = 0, 1, 3 .

(2.159)

Using Eqs. (2.158) and (2.148), together with Proposition 2.1 and the multiplication table (2.47) — in a manner analogous to the proof of Proposition 2.2 —
one verifies that the transformed versions of the skew-symmetric Cartan matrices
𝑚 05 , 𝑚 12 , and 𝑚 34 (see Eqs. (2.101)-(2.103)) in the Majorana (real) basis assume,

## PDF page 64

50 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

respectively, the following diagonal forms:
( (
)
(
(
))
−1 )
Γ05 𝑥 = 𝑈 𝑚 05 𝑈
𝑥 = i𝑚 05 𝑆 𝑥 = −i𝑚 0 𝑚 5 𝑚 0 𝑚 1 (𝑚 3 𝑥)
(
)
= −i𝑚 5 𝑚 1 (𝑚 3 𝑥)
(
)
= −i 𝚥 ℓ𝚤 (ℓ𝒌 𝑥)
⨁(
)
=i
− 𝐷 1𝒌 + 𝐷 05 − 𝐷 12 − 𝐷 34 𝑥 ,
(2.160)
)
( (
(
))
(
−1 )
Γ12 𝑥 = 𝑈 𝑚 12 𝑈
𝑥 = i𝑚 12 𝑆 𝑥 = −i𝑚 1 𝑚 2 𝑚 0 𝑚 1 (𝑚 3 𝑥)
(
)
= −i𝑚 2 𝑚 0 (𝑚 3 𝑥)
(
)
= −i 𝚥ℓ 𝚤 (ℓ𝒌 𝑥)
⨁(
)
=i
𝐷 1𝒌 + 𝐷 05 − 𝐷 12 + 𝐷 34 𝑥 , (2.161)
( (
)
(
(
))
−1 )
Γ34 𝑥 = 𝑈 𝑚 34 𝑈
𝑥 = i𝑚 34 𝑆 𝑥 = −i𝑚 3 𝑚 4 𝑚 0 𝑚 1 (𝑚 3 𝑥)
(
)
= i𝑚 4 𝑚 0 (𝑚 1 𝑥)
(
)
= iℓ 𝚤 (ℓ𝚤 𝑥)
⨁(
)
=i
𝐷 1𝒌 + 𝐷 05 + 𝐷 12 − 𝐷 34 𝑥 , (2.162)
⨁
where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)). Again, for the convention
(. . . ), see
Sect. 1.2.5.2.
Moreover, one can show that the product of these diagonal matrices reproduces
𝜔(4, 2) (2.154):
(
)
(
)
Γ05 Γ12 Γ34 𝑥 = 𝑈 𝐸 𝑈 −1 𝑥 = 𝜔(4, 2) 𝑥 ,
(2.163)
and, utilizing the standard properties (2.11) and (2.13) of the trace, that the four 8 × 8
matrices (2.155) and (2.160)-(2.162) are trace orthogonal:
(
)
(
)
(
)
(
)
𝑇 Γ05 Γ12 = 𝑇 Γ05 Γ34 = 𝑇 Γ12 Γ34 = · · · = 𝑇 Γ12 𝐷 = 0 .
(2.164)
We observe further that the diagonal volume forms (2.126)-(2.128) of the Clifford
subalgebras 𝔠𝔩(2, 2) and 𝔠𝔩(4, 0) remain unchanged (up to the meaning of the indices)
under the similarity transformation.

## PDF page 65

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
51

2.4.2 Changing the Basis: From Majorana to Chiral
Now, we turn to the second approach, namely, keeping the operators in their original
form while transforming the basis, that is, working with:
)
1
= 𝑈 −1 1 = √ ( 1 + i𝒌) ,
2

𝑛ˆ

1𝒌 −

(

)
1
= i𝑈 −1 𝚥 = √ (𝚤 + i 𝚥) ,
2

𝑛ˆ

(

)
1
= i𝑈 −1 𝚥ℓ = √ (ℓ𝚤 + i 𝚥ℓ) ,
2

𝑛ˆ

(

)
1
= i𝑈 −1 ℓ = √ (ℓ𝒌 + iℓ) ,
2

𝑛ˆ

𝑛ˆ

1𝒌 +

𝑛ˆ

(

(

05+

𝑛ˆ

(

12+

𝑛ˆ

34+

(

05 −

12 −

(

34 −

)
1
= 𝑈 −1 𝒌 = √ ( 1 − i𝒌) = 𝑛 ˆ ,
1𝒌 +
2
(2.165)
)
1
= i𝑈 −1 𝚤 = √ (𝚤 − i 𝚥) = 𝑛 ˆ ,
05+
2
(2.166)
)
1
= i𝑈 −1 ℓ𝚤 = √ (ℓ𝚤 − i 𝚥ℓ) = 𝑛 ˆ ,
12+
2
(2.167)

)
1
= i𝑈 −1 ℓ𝒌 = √ (ℓ𝒌 − iℓ) = 𝑛 ˆ .
34+
2
(2.168)
𝜋

To drive the above results, it suffices to substitute 𝑈 = 𝑒 i 4 𝑉, taking into account
Eqs. (2.152), (2.144), (2.132), and (2.96). For the complex rescaling of 𝑛 ˆ , 𝑛 ˆ ,
05± 12±
and 𝑛 ˆ by ‘i’, see Remark 2.16.
34±
The above transformed basis spans the chiral space 𝔖, which, by construction,
decomposes into two complex-conjugate semispinor chiral subspaces 𝔖± :
{
}
(2.169)
𝔖± = Span 𝑛 𝑎± ; 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝔖± = 𝔖∓ .
1𝒌 ±

05±

12±

34±

Notably, each chiral subspace is totally isotropic; that is, for all 𝑛 𝑎± , 𝑛𝑏 ∈ 𝔖± , the
±
bilinear form defined in (2.3) satisfies:
⟩
⟨
⟩
⟨
𝑛 𝑎+ , 𝑛 𝑏+ = 0 = 𝑛 𝑎 − , 𝑛 𝑏 − ,
(2.170)
so that every vector has zero norm and all vectors within the same subspace are mutually orthogonal. It is important to emphasize that this property holds independently
for 𝔖+ and 𝔖− , while in general the bilinear form between vectors from different
subspaces does not need to vanish. Actually, explicit calculations show that:11

11 Note that the star ‘∗ ’ on 𝑛

𝑎 denotes octonionic conjugation, which reverses the sign of the
imaginary units of OS but leaves the complex scalar i ∈ C unchanged. Accordingly, the resulting
norm differs from that with respect to which the similarity transformation 𝑈 is unitary.

## PDF page 66

52 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

𝑛ˆ , 𝑛ˆ

⟩

(
)
1
= 𝑁 𝑛 ˆ = 𝑛 ˆ 𝑛∗ˆ = (1 + i𝒌) (1 − i𝒌) = 0 ,
1𝒌 +
1𝒌 + 1𝒌 + 2

(2.171)

⟨

⟩

(
)
1
= 𝑁 𝑛 ˆ = 𝑛 ˆ 𝑛∗ˆ = − (𝚤 + i 𝚥) (𝚤 + i 𝚥) = 0 ,
05+
05+ 05+
2

(2.172)

⟨

1𝒌 +

1𝒌 +

𝑛ˆ , 𝑛ˆ
05+

05+

𝑛ˆ , 𝑛ˆ

⟩

(
)
1
= 𝑁 𝑛 ˆ = 𝑛 ˆ 𝑛∗ˆ = − (ℓ𝚤 + i 𝚥ℓ) (ℓ𝚤 + i 𝚥ℓ) = 0 ,
12+
12+ 12+
2

(2.173)

⟨

⟩

(
)
1
= 𝑁 𝑛 ˆ = 𝑛 ˆ 𝑛∗ˆ = − (ℓ𝒌 + iℓ) (ℓ𝒌 + iℓ) = 0 ,
34+
34+ 34+
2

(2.174)

⟨

12+

12+

𝑛ˆ , 𝑛ˆ
34+

34+

moreover, employing Eq. (2.3), we have:
⟨

⟨

⟩

𝑛ˆ , 𝑛ˆ
1𝒌 +

05+

𝑛ˆ , 𝑛ˆ
12+

⟩

05+

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
05+
05+
1𝒌 +
1𝒌 +
2
)
1 (
= 𝑁 𝑛ˆ + 𝑛ˆ
05+
1𝒌 +
2
)(
)∗
1(
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
05+
05+
1𝒌 +
2 1𝒌 +
)(
)
1(
= ( 1 + 𝚤) + i( 𝒌 + 𝚥) ( 1 − 𝚤) − i( 𝒌 + 𝚥) = 0 ,
4
=

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
12+
12+
05+
05+
2
)
1 (
= 𝑁 𝑛ˆ + 𝑛ˆ
12+
05+
2
(
)(
)∗
1
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
12+
05+
05+
2 12+
)(
)
1(
= − (ℓ𝚤 + 𝚤) + i( 𝚥ℓ + 𝚥) (ℓ𝚤 + 𝚤) + i( 𝚥ℓ + 𝚥) = 0 ,
4

=

and so forth:
⟨
⟩ ⟨
⟩ ⟨
⟩ ⟨
⟩
𝑛 ˆ , 𝑛 ˆ = 𝑛 ˆ , 𝑛 ˆ = 𝑛ˆ , 𝑛 ˆ = 𝑛ˆ , 𝑛 ˆ = · · · = 0 .
34+

(2.175)

34+

05+

12+

1𝒌 +

12+

1𝒌 +

34+

(2.176)

(2.177)

As naturally expected, the set of basis vectors {𝑛 𝑎− } satisfies orthogonality relations
analogous to those of its complex-conjugate counterpart {𝑛 𝑎+ }:
⟨

⟨

⟨
⟩ ⟨
⟩ ⟨
⟩
= 𝑛ˆ , 𝑛ˆ = 𝑛ˆ , 𝑛ˆ = 𝑛ˆ , 𝑛ˆ = 0,

(2.178)

⟨
⟩ ⟨
⟩ ⟨
⟩
= 𝑛 ˆ , 𝑛 ˆ = 𝑛ˆ , 𝑛 ˆ = 𝑛ˆ , 𝑛 ˆ = · · · = 0 .

(2.179)

𝑛ˆ , 𝑛ˆ
1𝒌 −

1𝒌 −

𝑛ˆ , 𝑛ˆ

⟩

34 −

05 −

⟩

05 −

34 −

12 −

12 −

05 −

1𝒌 −

12 −

12 −

34 −

1𝒌 −

34 −

34 −

## PDF page 67

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
53

In this construction, the only nonzero inner products are (see again Eq. (2.3)):
⟨

𝑛ˆ , 𝑛ˆ
1𝒌 −

1𝒌 +

⟨

⟩

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
1𝒌 −
1𝒌 +
1𝒌 −
1𝒌 +
2
)
1 (
= 𝑁 𝑛ˆ + 𝑛ˆ
1𝒌 +
1𝒌 −
2
)(
)∗
1(
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
1𝒌 + 1𝒌 −
1𝒌 +
2 1𝒌 −
)(
)
1(
= ( 1 + 1) + i(−𝒌 + 𝒌) ( 1 + 1) + i( 𝒌 − 𝒌) = 1 ,
4
=

𝑛ˆ , 𝑛ˆ
05 −

⟨

⟨

05+

𝑛ˆ , 𝑛ˆ
12 −

⟩

12+

𝑛ˆ , 𝑛ˆ
34 −

⟩

34+

⟩

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
05 −
05+
05 −
05+
2
(
)
1
= 𝑁 𝑛ˆ + 𝑛ˆ
05 −
05+
2
)(
)∗
1(
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
05+
05 −
05+
2 05−
)(
)
1(
= (𝚤 + 𝚤) + i(0) − (𝚤 + 𝚤) + i(0) = 1 ,
4

(2.180)

=

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
12 −
12+
12 −
12+
2
)
1 (
= 𝑁 𝑛ˆ + 𝑛ˆ
12 −
12+
2
)(
)∗
1(
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
12
12
12
12
−
+
−
+
2
)(
)
1(
= 2ℓ𝚤 + i(0) − 2ℓ𝚤 + i(0) = −1 ,
4

(2.181)

=

)
(
)
(
))
1( (
𝑁 𝑛ˆ + 𝑛ˆ − 𝑁 𝑛ˆ − 𝑁 𝑛ˆ
34 −
34+
34 −
34+
2
(
)
1
= 𝑁 𝑛ˆ + 𝑛ˆ
34 −
34+
2
)(
)∗
1(
= 𝑛ˆ + 𝑛ˆ 𝑛ˆ + 𝑛ˆ
34+
34 −
34+
2 34−
)(
)
1(
= 2ℓ𝒌 + i(0) − 2ℓ𝒌 + i(0) = −1 .
4

(2.182)

=

(2.183)

Remark 2.16 In light of the foregoing discussion, it is worth emphasizing that the
complex rescaling of the null vectors 𝑛 ˆ , 𝑛 ˆ , and 𝑛 ˆ by the factor ‘i’ is prescribed
34±
05± 12±
in such a way as to ensure the validity of the identities (2.180)-(2.183). This rescaling
corresponds to a rotation in the complex plane and leaves the underlying geometric
structure invariant.
□

## PDF page 68

54 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

Taking the above into account, we now examine the matrix realization of the 𝔲(1)
generator 𝐸 (2.96) of the conformal Lie algebra 𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1), expressed
with respect to the chiral basis. This yields a form analogous to 𝜔(4, 2) (2.155), but
with a different interpretation of the indices:
⨁(
)
𝐸𝑦=i
𝐷 1ˆ𝒌 + 1ˆ𝒌 − + 𝐷 05
ˆ + 34
ˆ − 𝑦 =: i𝐷 𝑦 = 𝜔(4, 2) 𝑦 ,
ˆ + 05
ˆ − + 𝐷 12
ˆ + 12
ˆ − + 𝐷 34
⏟
⏞⏞
⏟
by abuse of notation!

(2.184)
⨁

where 𝑦 ∈ Span{𝑛 𝑎± }. For the convention
(. . . ), see Sect. 1.2.5.2. This result
can be easily checked by substituting 𝑦 with any of the zero-norm basis vectors 𝑛 𝑎±
(in fact, by substituting each one individually). Just to clarify the point, let us set
𝑦 = 𝑛 ˆ . Then, employing Eqs. (2.166), (2.154), and (2.155), we obtain:
05+

(
)
(
)
( )
(
)
𝐸 𝑛 ˆ = 𝐸 i𝑈 −1 𝚥 = i𝑈 −1 𝑈 𝐸 𝑈 −1 𝚥 = i𝑈 −1 i 𝚥 = i 𝑛 ˆ ,
05+

05+

(2.185)

which is consistent with Eq. (2.184). In this context, one observes that the chiral
(isotropic) subspaces 𝔖± (2.169) are precisely the eigenspaces of 𝜔(4, 2) (2.184)
corresponding to the eigenvalues ±i, respectively. That is:
𝜔(4, 2) 𝔖± = ±i 𝔖± .

(2.186)

Similarly, one verifies that the skewsymmetric Cartan matrices 𝑚 05 , 𝑚 12 , and 𝑚 34
(see Eqs. (2.101)-(2.103)) in their original forms assume the following diagonal
representations in the chiral basis, analogous to those in Eqs. (2.160)-(2.162), but
with a different interpretation of the indices:
⨁(
)
𝑚 05 𝑦 = i
− 𝐷 1ˆ𝒌 + 1ˆ𝒌 − − 𝐷 05
=: Γ05 𝑦
,
ˆ + 05
ˆ − + 𝐷 12
ˆ + 12
ˆ − + 𝐷 34
ˆ + 34
ˆ− 𝑦
⏟ ⏞⏞ ⏟
by abuse of notation!

(2.187)

𝑚 12 𝑦 = i

⨁(

)
𝐷 1ˆ𝒌 + 1ˆ𝒌 − − 𝐷 ˆ
ˆ − + 𝐷 12
ˆ+ ˆ
ˆ + 34
ˆ− 𝑦
12 − − 𝐷 34
05+ 05

=: Γ12 𝑦
⏟ ⏞⏞ ⏟

,

by abuse of notation!

(2.188)

𝑚 34 𝑦 = i

⨁(

)
𝐷 1ˆ𝒌 + 1ˆ𝒌 − − 𝐷 ˆ
ˆ − − 𝐷 12
ˆ+ ˆ
ˆ + 34
ˆ− 𝑦
12 − + 𝐷 34
05+ 05

=: Γ34 𝑦
⏟ ⏞⏞ ⏟

,

by abuse of notation!

(2.189)

## PDF page 69

2.4 Unitary Transformation from Real to a Diagonal Compact Cartan Basis of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
55

⨁
where 𝑦 ∈ Span{𝑛 𝑎± } and see Sect. 1.2.5.2 for the convention on
(. . . ). These
relations can be readily verified by following the same procedure outlined above (see
Eq. (2.185)).
With the above in mind, and analogously to the 𝔠𝔩(2) case (see Sect. 2.3.1), the
following relations hold for the chiral spinor 𝜓:
)
( +)
(
1±𝐷
𝜓
𝜓 = 𝜓±
𝜓 = − = 𝑈 𝜉 , 𝐷±𝜓 =
𝜓
2
=⇒

(𝜓 𝑐 ) 𝑐 = 𝜓

𝜔(4, 2) 𝜓 ± = ±i 𝜓 ± ;

=⇒

𝜓𝑐 = 𝐶 𝜓 ,

𝐶 𝐶 = 1 ; 𝐶 = 𝑈𝑈 ⊤ ,

where 𝐶 Γ𝜈 = Γ𝜈 𝐶 ,
(2.190)

(𝐶Majorana = 1) .

(2.191)

Finally, repeating the analysis for 𝔠𝔩(2) leading to (2.120), we find the phase
factor 𝜚 relating 𝑈 and 𝑉 in (2.152) can be again fixed in a way to make the charge
conjugation matrix 𝐶 real. Specifically, one obtains:
𝜋

𝜋

𝜋

𝜋

𝐶𝑉 = 𝑉𝑉 ⊤ = 𝑒 − 4 𝐸 𝑒 −i 4 𝐷 𝑒 −i 4 𝐷 𝑒 4 𝐸 = −i𝐷𝐸 = −i𝑆 .

(2.192)

Note that 𝐷 ⊤ = 𝐷 and 𝐸 ⊤ = −𝐸. For 𝜚 = 𝑒 i 𝜋/4 (that is, 𝑈 = 𝑒 i 𝜋/4𝑉), this relation
yields:
𝐶𝑈 = 𝐶𝑈 = 𝑈𝑈 ⊤ = 𝑆 .

(2.193)

2.4.3 Adjustment of Notation
From this point forward, we adopt the compact chiral basis of isotropic vectors,
defined as:
𝜉 1 1 + 𝜉 𝒌 𝒌 = 𝜓 1𝒌 + 𝑛 ˆ + 𝜓 1𝒌 − 𝑛 ˆ ,
ˆ

where

1𝒌 +

ˆ

1𝒌 −

1
𝑛 ˆ = √ ( 1 ± i𝒌) ,
1𝒌 ±
2

)
1 (
ˆ
𝜓 1𝒌 ± = √ 𝜉 1 ∓ i𝜉 𝒌 ,
2

(2.194)

)
1 (
ˆ
𝜓 12± = √ 𝜉 1 ∓ i𝜉 2 ,
2

(2.195)

𝜉 1 ℓ𝚤 + 𝜉 2 𝚥ℓ = 𝜓 12+ 𝑛 ˆ + 𝜓 12− 𝑛 ˆ ,
ˆ

ˆ

12+

where

12 −

1
𝑛 ˆ = √ (ℓ𝚤 ± i 𝚥ℓ) ,
12±
2

and similar expression for 𝑛 ˆ , 𝑛 ˆ , 𝜓 05± , and 𝜓 34± . Again, the vectors 𝑛 𝑎+ ,
ˆ

05±

34±

ˆ

with 𝑎 + = 1ˆ𝒌 + , ˆ
05+ , ˆ
12+ , ˆ
34+ , form an isotropic basis consisting( of eigenvec)
tors of 𝜔(4, 2) with eigenvalue +i. Their complex conjugates 𝑛 𝑎− = 𝑛 𝑎+ , with

## PDF page 70

56 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

𝑎 − = 1ˆ𝒌 − , ˆ
05− , ˆ
12− , ˆ
34− , correspondingly form an isotropic basis with eigenvalue
−i. That is:
(𝜔(4, 2) ∓ i1) 𝑛 𝑎± = 0 ,

(2.196)

⟩
( )
𝑛 𝑎± , 𝑛 𝑎± = 𝑁 𝑛 𝑎± = 𝑛 𝑎± 𝑛∗𝑎± = 0 ,

(2.197)

where:
⟨

⟨

⟩
𝑛 𝑎− , 𝑛𝑏+ = 𝜖 𝑎 𝛿 𝑎𝑏 ,

(2.198)

with 𝜖 ˆ = 𝜖 ˆ = 1 = −𝜖 ˆ = −𝜖 ˆ .
1𝒌

05

12

34

2.5 Appendix: A Mnemonic Matrix Rule for (Split) Octonionic
Multiplication
This appendix develops a mnemonic matrix formulation following the methodology
recently outlined in Ref. [101]. We consider a (split) octonion expressed in CayleyDickson form:
𝑜 = 𝑞 + ℓ𝑝 ,

𝑞, 𝑝 ∈ H ,

(ℓ) 2 = ±1 .

(2.199)

The multiplication of two (split) octonions is given by Eq. (2.35); for convenience,
we reproduce it here:
(
)(
)
(
)
𝑞 1 + ℓ 𝑝 1 𝑞 2 + ℓ 𝑝 2 = 𝑞 1 𝑞 2 + (ℓ) 2 𝑝 2 𝑝 ∗1 + ℓ 𝑞 ∗1 𝑝 2 + 𝑞 2 𝑝 1 .
(2.200)
To each octonion, we associate the matrix:
(
)
𝑞 (ℓ) 2 𝑝 ∗
𝑀 (𝑜) =
.
𝑝
𝑞∗

(2.201)

A direct computation yields:
2

↶
∗

©𝑞 𝑞 + (ℓ) 𝑝 1 𝑝 2
𝑀 (𝑜 1 ) 𝑀 (𝑜 2 ) = ­ 1 2
↶
∗
« 𝑝1 𝑞2 + 𝑞1 𝑝2

↶

(ℓ) 2 𝑞 1 𝑝 ∗2 + (ℓ) 2 𝑝 ∗1 𝑞 ∗2 ª
®,
↶
2
∗
∗
∗
(ℓ) 𝑝 1 𝑝 2 + 𝑞 1 𝑞 2 ¬

(2.202)

where the symbol ‘↶’ indicates reversal of the order of multiplication. Remarkably,
this matrix product reproduces the octonionic multiplication once these reversed
products are replaced by their adjoint counterparts, thereby recovering Eq. (2.200)
(or Eq. (2.35)).

## PDF page 71

2.6 Appendix: Realization of the Conformal Group U(2, 2)  SU(2, 2)

(

)
 SO(4, 2) ×U(1) in the Clifford Algebra 𝔠𝔩 (4, 2) and its Action on

Inspection of Eq. (2.202) reveals a clear mnemonic pattern: in each block of the
matrix product, the terms naturally split into two contributions — one involving the
quaternionic product in standard (right) order, denoted 𝑅, and one in reversed (left)
order, denoted 𝐿. This separation provides a convenient guide for reconstructing the
octonionic multiplication from the matrix representation:
upper row ;

𝑅+𝐿

and

𝐿 + 𝑅,

(2.203)

lower row ;

𝐿+𝑅

and

𝑅+𝐿.

(2.204)

left column ;

𝑅+𝐿

and

𝐿 + 𝑅,

(2.205)

right column ;

𝐿+𝑅

and

𝑅+𝐿.

(2.206)

Equivalently:

In this way, the octonion multiplication table manifests as a highly structured block
arrangement of quaternionic products, with only half of the terms appearing in
reversed order. The matrix representation 𝑀 (𝑜) thus provides a compact and practical
mnemonic for the non-associative octonionic product, offering a clear framework
for navigating the inherent non-associativity.

2.6 Appendix: Realization
Group
( of the Conformal
)
U(2, 2)  SU(2, 2)  SO(4, 2) × U(1) in the Clifford
Algebra 𝖈𝖑(4, 2) and its Action on Spinors
Using the Clifford-algebraic framework developed ( in this chapter,
) the unitaryconformal group U(2, 2) — equivalently SU(2, 2)  SO(4, 2) × U(1) — admits a concrete realization in the real Clifford algebra 𝔠𝔩(4, 2), specifically within
its even subalgebra 𝔠𝔩 even (4, 2). In this realization, the bivectors of the even subalgebra generate the conformal Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2), while the Clifford
pseudoscalar (volume element)
( provides the
) 1-dimensional central 𝔲(1) component,
so that 𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1). This unified Clifford-algebraic
setting naturally produces both the conformal Lorentz group SO(4, 2) and its spin
representation SU(2, 2) directly from the Clifford algebra’s multiplicative structure,
with the central U(1) factor realized as internal phase rotations generated by the
pseudoscalar. In this way, the full U(2, 2) group emerges naturally from the Cliffordalgebraic framework. We clarify this construction here.
To clarify the underlying structure, we present a step-by-step derivation leading
to the explicit construction. The even Clifford subalgebra 𝔠𝔩 even (4, 2) is given by:
{
𝔠𝔩 even (4, 2) = Span 1 , 𝑚 𝜇𝜈 := 𝑚 𝜇 𝑚 𝜈 , 𝑚 𝜇 𝑚 𝜈 𝑚 𝜚 𝑚 𝜎 , 𝐸 := 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 𝑚 4
}
;0≤𝜇<𝜈<𝜚<𝜎≤5 ,
(2.207)

## PDF page 72

58 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

such that:
1. The 6 operators 𝑚 𝜇 represent left multiplication by the 6 imaginary split{
}
octonion units 0 := 𝚤, 5 := 𝚥, 1 := ℓ𝚤, 2 := 𝚥ℓ, 3 := ℓ𝒌, 4 := ℓ , as defined
in Eqs. (2.60)-(2.62), and they satisfy the Clifford anticommutation relations
(2.64).
[
]
2. The Lie algebra generated by the 15 bivectors 𝑚 𝜇𝜈 := 12 𝑚 𝜇 , 𝑚 𝜈 = 𝑚 𝜇 𝑚 𝜈
coincides with the conformal Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) (see Eq. (2.85)).
We therefore identify the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) as embedded in the
even Clifford subalgebra 𝔠𝔩 even (4, 2) via:
{
}
𝔰𝔲(2, 2) ↩→ Span 𝑚 𝜇𝜈 ⊂ 𝔠𝔩 even (4, 2) .
(2.208)
Each 𝑚 𝜇𝜈 acts on the real 8-dimensional spinor space 𝔖 = Span{ 𝐴} through
left multiplication (see Eqs. (2.60)-(2.62) and Remark 2.4).
3. The Clifford pseudoscalar (volume form) 𝐸 := 𝑚 0 𝑚 5 𝑚 1 𝑚 2 𝑚 3 𝑚 4 commutes with every bivector 𝑚 𝜇𝜈 (see Eq. (2.95)) and therefore generates the
1-dimensional center of the algebra, corresponding to the 𝔲(1) factor in 𝔲(2, 2).
Then, combining this central element with the conformal sector generated by
𝑚 𝜇𝜈 , one obtains the full Lie algebra:
𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩 even (4, 2) .

(2.209)

Any element of the group U(2, 2) can be expressed naturally by exponentiating a
linear combination of the bivectors 𝑚 𝜇𝜈 and the pseudoscalar 𝐸:12
1

(2.210)
U(2, 2) ∋ ˜
𝑅(𝑋, 𝜔0 𝐸) = 𝑒 2 𝑋+𝜔0 𝐸 ,
(
)
∑
with 𝑋 ∈ 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) = 𝜇<𝜈 𝜔 𝜇𝜈 𝑚 𝜇𝜈 , while 𝜔 𝜇𝜈 , 𝜔0 ∈ R. Since 𝐸
commutes with all 𝑚 𝜇𝜈 , this expression factorizes:13
1

1

˜
𝑅(𝑋,
𝜔0 ) = 𝑒 2 𝑋 𝑒 𝜔0 𝐸 = 𝑒 𝜔0 𝐸 𝑒 2 𝑋 ,

(2.211)

thereby realizing the direct product structure U(2, 2)  SU(2, 2) × U(1).
In this regard, it is important to emphasize that:
1. Expanding the exponential as a power series yields:

12 Note that the factor ‘ 1 ’ ensures the correct spinorial form of conformal transformations. In
2

Clifford algebra, bivectors generate rotations and boosts with twice the physical angle when acting
1

on vectors; including ‘ 12 ’ adjusts this so that 𝑒 2 𝑋 gives the proper single-angle rotation on spinors,
as required by the double-cover relation Spin(4, 2)  SU(2, 2).
[
]
13 For matrices or Lie algebra elements 𝑀 and 𝑁 , 𝑒 𝑀+𝑁 = 𝑒 𝑀 𝑒 𝑁 if 𝑀, 𝑁 = 0; otherwise
𝑒 𝑀 𝑒 𝑁 = 𝑒 𝐿 with 𝐿 given by the Baker-Campbell-Hausdorff series.

## PDF page 73

2.6 Appendix: Realization of the Conformal Group U(2, 2)  SU(2, 2)

(

)
 SO(4, 2) ×U(1) in the Clifford Algebra 𝔠𝔩 (4, 2) and its Action on

∞ ( 1 )𝑛 ∞
∑︁
∑︁ (𝜔0 𝐸 ) 𝑚
1
1
𝑋+𝜔0 𝐸
𝑋 𝜔0 𝐸
2𝑋
2
2
=𝑒 𝑒
=
𝑒
.

𝑛!
𝑛=0

(2.212)

𝑚!
𝑚=0

Each term in this series is a product of an even number of Clifford generators and
therefore belongs to the even subalgebra 𝔠𝔩 even (4, 2). Moreover, since 𝔠𝔩 even (4, 2)
is finite-dimensional, the series converges within this subalgebra, ensuring that the
exponential (the group element) remains entirely inside 𝔠𝔩 even (4, 2). Specifically:
a. From Proposition 2.1 and of course Remark 2.4, we recall that all powers
(𝐸) 𝑛 = (𝐿 −𝒌 ) 𝑛 are well-defined and unambiguous. Exploiting this fact together with the identity 𝐸 2 = −1 (see Eq. (2.99)), the exponential of the
central element can be computed explicitly:
𝑒 𝜔0 𝐸 =

∞
∑︁
(𝜔0 𝐸) 𝑚

=

∞
∑︁
(−1) 𝑚 (𝜔0 ) 2𝑚

(2𝑚)!

𝑚!

1+

𝑚=0

𝑚=0

∞
∑︁
(−1) 𝑚 (𝜔0 ) 2𝑚+1
𝑚=0

(2𝑚 + 1)!

= cos 𝜔0 1 + sin 𝜔0 𝐸 ,

𝐸

(2.213)

so that 𝜔0 plays the role of the internal U(1) phase angle.
b. Similarly,
(
) 𝑛 invoking Proposition 2.1 and Remark 2.4, all powers of the form
𝑚 𝜇 𝑚 𝜈 are well-defined and unambiguous. Exploiting this property, together with the fact that each bivector 𝑚 𝜇𝜈 = 𝑚 𝜇 𝑚 𝜈 squares to:14
(

𝑚 𝜇𝜈

)2

= −𝜂 𝜇𝜇 𝜂 𝜈𝜈 1 = ±1 ,

(2.214)

the exponential of the bivector component admits the power series expansion:

 cos

1
1
𝑒 2 𝑋 = 𝑒 2 𝜔 𝜇𝜈 𝑚𝜇𝜈 =


𝜔 𝜇𝜈
2

1 + sin 𝜔2𝜇𝜈 𝑚 𝜇𝜈


 cosh 𝜔 𝜇𝜈 1 + sinh 𝜔 𝜇𝜈 𝑚
𝜇𝜈

2
2

(

𝑚 𝜇𝜈

)2

(

𝑚 𝜇𝜈

)2

= −1
,
= +1
(2.215)

with each term lying in the even subalgebra 𝔠𝔩 even (4, 2).
2. The inverse of any group element follows directly from the exponential structure:
1

1

1

𝑅˜ −1 (𝑋, 𝜔0 ) = 𝑒 − 2 𝑋− 𝜔0 𝐸 = 𝑒 − 2 𝑋 𝑒 − 𝜔0 𝐸 = 𝑒 − 𝜔0 𝐸 𝑒 − 2 𝑋 .

(2.216)

3. Because the even subalgebra is closed under multiplication, the product of any
two such elements again yields an element of the same form:
˜ ′′ , 𝜔′′ ) ∈ 𝔠𝔩 even (4, 2) .
˜
˜ ′ , 𝜔′ ) = 𝑅(𝑋
𝑅(𝑋,
𝜔0 ) 𝑅(𝑋
0
0

(2.217)

Accordingly, the exponential construction realizes U(2, 2) entirely within 𝔠𝔩 even (4, 2).

14 This identity can be verified by a procedure analogous to that used in Eq. (2.91).

## PDF page 74

60 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

4. Finally, the associativity required for the group law is ensured by the associativity
of operator composition, which holds by construction as explained in Remark
2.4.
Remark 2.17 For a more tangible visualization of the SU(2, 2) group structure, we
conclude this appendix by exhibiting a 2 × 2-matrix realization of SU(2, 2) in terms
of complex quaternionic components:
{
( )
𝑎𝑏
SU(2, 2) = 𝑔 =
; det(𝑔) = 1 , 𝐽 𝑔 † 𝐽 = 𝑔 −1 ,
𝑐𝑑
(
)
}
1 0
with 𝐽 = 2
and 𝑎, 𝑏, 𝑐, 𝑑 ∈ H ⊗ C  Mat(2, C) .
0 −12
(2.218)
For a detailed account of complex quaternions and their matrix realization, we refer
to Ref. [37].
□

2.7 Appendix: Maximal Compact Subalgebra of
𝖘𝖚(2, 2)  𝖘𝖔(4, 2)
The maximal compact subalgebra of 𝔰𝔲(2, 2) is given by:
}
(
) {
𝔰 𝔲(2) ⊕ 𝔲(2) = (𝑋, 𝑌 ) ∈ 𝔲(2) ⊕ 𝔲(2) ; Tr(𝑋 + 𝑌 ) = Tr(𝑋) + Tr(𝑌 ) = 0 .
(2.219)
Each 𝔲(2) factor admits the decomposition:
𝔲(2)  𝔰𝔲(2) ⊕ 𝔲(1) .

(2.220)

Let 𝔰𝔲(2) 𝐿 and 𝔰𝔲(2) 𝑅 denote the special unitary parts of the left and right 𝔲(2)
factors, respectively, in (2.219). The two corresponding 𝔲(1) generators, denoted 𝑍 𝐿
and 𝑍 𝑅 , represent the scalar (central) components of the two 𝔲(2) summands.
The tracelessness condition Tr(𝑋) + Tr(𝑌 ) = 0 implies that 𝑍 𝐿 and 𝑍 𝑅 are not
independent, but satisfy the linear constraint:
𝑍𝐿 + 𝑍𝑅 = 0 .

(2.221)

As a consequence, the center of the maximal compact subalgebra is 1-dimensional
and generated by the single 𝔲(1) element
𝑍 := 𝑍 𝐿 − 𝑍 𝑅 .
Accordingly, the maximal compact subalgebra of 𝔰𝔲(2, 2) reads as:

(2.222)

## PDF page 75

2.8 Appendix: Diagonal Inner Products of Real Matrices Representing Imaginary Split-Octonion Units
61

(
)
𝔰 𝔲(2) ⊕ 𝔲(2)  𝔰𝔲(2) ⊕ 𝔰𝔲(2) ⊕ 𝔲(1) ,
or, equivalently, in terms of real Lie algebras:
(
)
𝔰 𝔲(2) ⊕ 𝔲(2)  𝔰𝔬(4) ⊕ 𝔰𝔬(2) .

(2.223)

(2.224)

At the group level, the corresponding maximal compact subgroup of SU(2, 2) is:
}
(
) {
𝑆 U(2) × U(2) = (𝑔 𝐿 , 𝑔 𝑅 ) ∈ U(2) × U(2) ; det(𝑔 𝐿 𝑔 𝑅 ) = det(𝑔 𝐿 ) det(𝑔 𝑅 ) = 1 .
(2.225)
Each factor admits the local decomposition:
U(2) 

SU(2) × 𝑈 (1)
,
Z2

(2.226)

where the quotient by Z2 is generated by the element (−12 , −1), which acts trivially
on all representations and enforces the determinant constraint globally.
Substituting this decomposition into the product U(2) 𝐿 × U(2) 𝑅 , the defining
unimodularity condition det(𝑔 𝐿 ) det(𝑔 𝑅 ) = 1 relates the two central U(1) phases
via:
𝑒 i( 𝜃𝐿 +𝜃𝑅 ) = 1 ,

(2.227)

where 𝑒 i𝜃𝐿 and 𝑒 i𝜃𝑅 denote the phase rotations associated with U(1) 𝐿 and U(1) 𝑅 ,
respectively. This condition removes the overall (diagonal) combination of the two
U(1) phases, leaving a single residual U(1) generated by the relative phase 𝑒 i( 𝜃𝐿 − 𝜃𝑅 ) .
Accounting for this shared central identification yields the global structure:
(
) SU(2) 𝐿 × SU(2) 𝑅 × U(1)
,
𝑆 U(2) × U(2) 
Z2

(2.228)

where the Z2 quotient is generated by the element (−12 , −12 , −1), which acts trivially
on all representations and enforces the determinant constraint globally.

2.8 Appendix: Diagonal Inner Products of Real Matrices
Representing Imaginary Split-Octonion Units
{
}
Proposition 2.3 The product 𝑚 𝜇 𝑚 𝜈 𝑚 𝜆 , where 𝜇, 𝜈, 𝜆 ∈ 𝚤, 𝚥, ℓ𝚤, 𝚥ℓ, ℓ𝒌 , ℓ , is a
diagonal 8×8 matrix iff (𝜇, 𝜈, 𝜆) is an associative triple belonging to a split-octonion
subalgebra such that their product is the unit octonion:
𝜇 𝜈 𝜆 = (𝜇 𝜈) 𝜆 = 𝜇 (𝜈 𝜆) = 1

⇐⇒

diagonal

𝑚 𝜇 𝑚 𝜈 𝑚𝜆 .

(2.229)

## PDF page 76

62 Majorana Representation of the Conformal Clifford Algebra 𝔠𝔩 (4, 2) and its Chiral Counterpart
2

Proof For any split octonion 𝑥 and 𝜇, 𝜈, 𝜆 satisfying (2.229), we have the following
identity, up to a sign (see Remark 2.3):
𝑚 𝜈 (𝑚 𝜆 𝑥)

= 𝜈(𝜆 𝑥) = (𝜈 𝜆) 𝑥 =
⏟
⏞⏞
⏟

(𝑚 𝜈 𝑚 𝜆 ) 𝑥 .

(2.230)

clarification omitted henceforth for simplicity!

Expanding this relation, again up to a sign, we obtain:
(
)
(
)
𝑚 𝜇 𝑚 𝜈 (𝑚 𝜆 𝑥) = 𝑚 𝜇 (𝑚 𝜈 𝑚 𝜆 ) 𝑥 =
(𝑚 𝜇 𝑚 𝜈 𝑚 𝜆 ) 𝑥 = 𝑥
⏟
⏞⏞
⏟

.

(2.231)

since ( 𝜇 𝜈 𝜆) 𝑥 = 1 𝑥 by Eq. (2.229)

This proves the proposition (=⇒) and also tells us that the diagonal elements of
the matrix 𝑚 𝜇 𝑚 𝜈 𝑚 𝜆 are 1, up to a sign. The inverse statement (⇐=) of the above,
however, follows from Moufang’s theorem (see Remark 2.2).
Here are two examples that differ from 𝐷 = 𝑚 𝚥 𝑚 ℓ 𝑚 𝚥ℓ = 𝑚 5 𝑚 4 𝑚 2 (2.132):
(
)
(
) ⨁
𝐷 ′ 𝑥 = 𝑚 0 𝑚 2 (𝑚 3 𝑥) = 𝚤 𝚥ℓ(ℓ𝒌 𝑥) =
(𝐷 1𝒌 + 𝐷 05 − 𝐷 12 + 𝐷 34 ) 𝑥 , (2.232)
(
)
(
) ⨁
𝐷 ′′ 𝑥 = 𝑚 5 𝑚 1 (𝑚 3 𝑥) = 𝚥 ℓ𝚤(ℓ𝒌 𝑥) =
(𝐷 1𝒌 − 𝐷 05 + 𝐷 12 + 𝐷 34 ) 𝑥 ,
(2.233)
where
⨁ 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)) and see Sect. 1.2.5.2 for the convention
on
(. . . ).
□

## PDF page 77

Chapter 3

Ladder Representation of 𝖚(2, 2) as a Quantized
4-dimensional Realization

Abstract This chapter develops a rigorous framework for positive-energy ladder
representations of the conformal Lie algebra:
(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩(4, 2) ,
realized as quantized models of massless fields with arbitrary helicity in 4dimensional Minkowski, de Sitter (dS), and anti-dS spacetimes. The construction is
founded on an invariant bilinear form in the Majorana-spinor space of 𝔠𝔩(4, 2), establishing the geometric basis
theory. Through the isomorphism
( for the representation
)
𝔠𝔩 even (4, 2)  𝔠𝔩(4, 1) ⊃ 𝔰𝔲(2, 2) , an explicit 4 × 4 matrix realization is introduced, encoding conformal symmetry in a computationally tractable spinorial form.
This provides the foundation for the systematic construction of ladder operators,
spectral analysis, and conformally covariant field operators.
The representations appear as lowest-weight modules characterized by conformal
energy and helicity, giving a full classification of massless conformal fields under
𝔲(2, 2). In particular, restriction to the dS subalgebra 𝔰𝔭(2, 2)  𝔰𝔬(4, 1) — a central
focus of this study — preserves irreducibility, thereby capturing the notion of masslessness in this curved background. Embedding these modules into 4-dimensional
conformal vertex algebras reveals their analytic structure, including operator product
expansions and modular properties. The Casimir invariants are explicitly computed,
clarifying their role in the spectrum, while the correspondence between 𝔰𝔬(4, 2) and
its Euclidean form 𝔰𝔬(5, 1) completes a unified algebraic framework for the study of
massless conformal systems in both flat and curved settings.

3.1 Invariant Bilinear Form in the Space of 𝖈𝖑(4, 2) Spinors
Note: Having clarified in the preceding chapter the Majorana realization of the
conformal Clifford algebra 𝔠𝔩(4, 2) and its subalgebras — implemented via left
multiplication by imaginary split-octonion units on the split-octonion algebra —

63

## PDF page 78

64

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

along with their chiral realizations, we shall henceforth streamline the notation and
present only the resulting formulas.
In the preceding chapter, we showed that the 8-dimensional Majorana (real) vector
space of 𝔠𝔩(4, 2) spinors, spanned by the split-octonion units, naturally carries the
structure of a composition algebra — nonassociative but alternative. In particular,
it can be equipped with a real-valued trace, a Cayley-Dickson conjugation, a factorizable quadratic norm 𝑁 (𝜉), and an associated nondegenerate symmetric bilinear
form ⟨𝜉, 𝜂⟩ such that:
(
)
𝑁 (𝜉) = 𝜉𝜉 ∗ = 𝜉 ∗ 𝜉
= (𝜉1 ) 2 + (𝜉𝒌 ) 2 + (𝜉0 ) 2 + (𝜉5 ) 2 − (𝜉1 ) 2 − (𝜉2 ) 2 − (𝜉3 ) 2 − (𝜉4 ) 2 ,

(3.1)

where 𝜉 = 𝜉 1 1 + 𝜉 𝒌 𝒌 + 𝜉 0 𝚤 + 𝜉 5 𝚥 + 𝜉 1 ℓ𝚤 + 𝜉 2 𝚥ℓ + 𝜉 3 ℓ𝒌 + 𝜉 4 ℓ ∈ OS , while the star
‘∗ ’ changes the sign of the imaginary OS units, and according to Eq. (2.3):
)
1(
𝑁 (𝜉 + 𝜂) − 𝑁 (𝜉) − 𝑁 (𝜂)
2
)
1( ∗
= 𝜉𝜂 + 𝜂𝜉 ∗
2
= 𝜉1 𝜂1 + 𝜉𝒌 𝜂𝒌 + 𝜉0 𝜂0 + 𝜉5 𝜂5 − 𝜉1 𝜂1 − 𝜉2 𝜂2 − 𝜉3 𝜂3 − 𝜉4 𝜂4 . (3.2)

⟨𝜉, 𝜂⟩ = ⟨𝜂, 𝜉⟩ =

Recall
that, throughout this work, we employ the }simplified index notation 𝜈 ∈
{
0 := 𝚤, 5 := 𝚥, 1 := ℓ𝚤, 2 := 𝚥ℓ, 3 := ℓ𝒌, 4 := ℓ . This construction yields two
inequivalent 8-dimensional spinor representations of Spin(4, 4), arising from left
and right multiplication by split-octonion units, together with a third 8-dimensional
vector representation. The three are tied together by an invariant trilinear (“Yukawa”)
form, which manifests the triality symmetry of the Lie algebra 𝐷 4 (see Refs. [102,
103], for more details).
We now reproduce the inner product (3.2) in the chiral (complex) basis of the
generators Γ𝜈 of 𝔠𝔩(4, 2). The basis generators satisfy the anticommutation relations:
{
}
Γ𝜇 , Γ𝜈 = 2𝜂 𝜇𝜈 ,
(3.3)
which follow directly from Eq. (2.64). Their behaviour under Hermitian conjugation
is given by:
Γ𝜈∗ = Γ𝜈2 Γ𝜈

=⇒

Γ0∗ = −Γ0 ,
Γ5∗ = −Γ5 ,
Γ𝑖∗ = Γ𝑖 ,

(𝑖 = 1, 2, 3, 4) .

(3.4)

This is indeed a direct consequence of Eqs. (2.81) and (2.82); in a real basis Γ𝜈 = 𝑚 𝜈 ,
𝑚 ∗𝜈 stands for the transposed 𝑚 ⊤𝜈 of 𝑚 𝜈 . With the above in mind, let us first determine
a unitary element 𝐵 of 𝔠𝔩(4, 2) satisfying:

## PDF page 79

3.1 Invariant Bilinear Form in the Space of 𝔠𝔩 (4, 2) Spinors

Γ𝜈∗ 𝐵 = −𝐵 Γ𝜈

=⇒

65

Γ0 𝐵 = 𝐵 Γ0 ,
Γ5 𝐵 = 𝐵 Γ5 ,

⇓

Γ𝑖 𝐵 = −𝐵 Γ𝑖 ,

∗
Γ𝜇𝜈
𝐵 = −𝐵 Γ𝜇𝜈

=⇒

(𝑖 = 1, 2, 3, 4) ,

Γ05 𝐵 = 𝐵 Γ05 ,
Γ12 𝐵 = 𝐵 Γ12 ,
Γ34 𝐵 = 𝐵 Γ34 ,
⇓
[

]
𝐵, 𝜔(4, 2) = 0 .

(3.5)

{ }
Recall that 𝜔(4, 2) is the 𝔠𝔩(4, 2) volume form in the basis Γ𝜈 (see Eq. (2.163)),
while the bivector generators Γ𝜇𝜈 are defined in Eq. (2.125).
Remark 3.1 In the chiral basis of 𝔠𝔩(4, 2), the Clifford generators Γ𝜈 are not all antiHermitian with respect to ordinary Hermitian conjugation (see Eq. (3.4)); this reflects
the mixed Hermiticity properties induced by the Clifford relations in signature (4, 2).
As a result, the standard inner product fails to be compatible with the requirement
that the generators Γ𝜇𝜈 of the conformal algebra 𝔰𝔬(4, 2) act as anti-Hermitian
operators.1 Indeed, with respect to the standard inner product:
⟨𝜓, 𝜙⟩std = 𝜓 ∗ 𝜙 ,

(3.6)

one finds:
( ∗ )∗
∗
⟨𝜓, Γ𝜇𝜈 𝜙⟩std = 𝜓 ∗ Γ𝜇𝜈 𝜙 = Γ𝜇𝜈
𝜓 𝜙 = ⟨Γ𝜇𝜈
𝜓, 𝜙⟩std = ⟨±Γ𝜇𝜈 𝜓, 𝜙⟩std ,

(3.7)

where the sign depends on the specific bivector generator Γ𝜇𝜈 under consideration.
Thus, the generators Γ𝜇𝜈 are not uniformly anti-Hermitian with respect to (3.6),
obstructing the construction of a unitary representation in the chiral basis.2
To remedy this, one introduces a unitary element 𝐵 ∈ 𝔠𝔩(4, 2) and defines a
∗ 𝐵 = −𝐵 Γ
modified notion of adjoint by imposing Γ𝜈∗ 𝐵 = −𝐵 Γ𝜈 , and hence Γ𝜇𝜈
𝜇𝜈
(see Eq. (3.5)). This condition allows one to define a new inner product:
⟨𝜓, 𝜙⟩ 𝐵 = 𝜓 ∗ 𝐵 𝜙 ,

(3.8)

1 Let ( H , ⟨·, ·⟩ ) be a complex inner product space and let 𝑋 be a linear operator on H . The

adjoint 𝑋 † of 𝑋 (with respect to ⟨·, ·⟩) is defined by the relation:
⟨ 𝜓, 𝑋 𝜙⟩ = ⟨𝑋 † 𝜓, 𝜙⟩ ,

for all

𝜓, 𝜙 ∈ H .

The operator 𝑋 is said to be Hermitian if 𝑋 † = 𝑋 and anti-Hermitian if 𝑋 † = −𝑋. These notions
depend explicitly on the chosen inner product. In particular, when the inner product is modified, the
corresponding adjoint changes accordingly. Only in the special case of the standard inner product
⊤
does the adjoint 𝑋 † coincide with ordinary Hermitian conjugation 𝑋 ∗ := 𝑋 .
2 For a unitary representation on a Hilbert space, it is necessary that the generators 𝑋 of the Lie
algebra be anti-Hermitian with respect to the chosen inner product, ensuring that their exponentials
𝑒 𝛼𝑋 ( 𝛼 ∈ R) are unitary operators and hence that the group representation is unitary.

## PDF page 80

66

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

with respect to which the generators Γ𝜇𝜈 act anti-Hermitian. Indeed:
(
(
)∗
∗ )
⟨𝜓, Γ𝜇𝜈 𝜙⟩ 𝐵 = 𝜓 ∗ 𝐵 Γ𝜇𝜈 𝜙 = 𝜓 ∗ − Γ𝜇𝜈
𝐵 𝜙 = − Γ𝜇𝜈 𝜓 𝐵 𝜙 = ⟨−Γ𝜇𝜈 𝜓, 𝜙⟩ 𝐵 ,
(3.9)
showing explicitly that Γ𝜇𝜈 is anti-Hermitian with respect to (3.8). Consequently,
the associated one-parameter subgroups of the conformal group are represented by
unitary operators on the Hilbert space, guaranteeing the unitarity of the representation.
Finally, requiring that 𝐵 commute with the Clifford volume form 𝜔(4, 2) ensures
that the inner product respects the chirality decomposition of the spinor space. In
particular, left- and right-handed sectors remain orthogonal, and the action of the
bivector generators Γ𝜇𝜈 preserves each chiral sector. In this way, the element 𝐵
provides a canonical and algebraically consistent framework for realizing unitary
positive-energy irreducible representations (UPEIRs) of the conformal algebra in
the chiral Clifford basis.
Note: For the sake of notational simplicity, we shall henceforth drop the subscripts
‘std’ and ‘𝐵’ from the inner product, as the relevant choice will always be clear from
the context.
□
Remarkably, there exists such a Hermitian unitary 𝐵 ∈ 𝔠𝔩(4, 2) determined by
the above properties up to sign. It turns out that the resulting 𝐵 coincides with the
𝔠𝔩(4, 0) pseudo scalar:
𝐵 = 𝑀 (4, 0) = 𝑚 12 𝑚 43 = 𝑈 𝑚 12 𝑚 43 𝑈 −1 = 𝑈 𝑚 12 𝑈 𝑈 −1 𝑚 43 𝑈 −1 = Γ12 Γ43 .
⏟
⏞⏞
⏟
since [𝑚12 𝑚43 , 𝑈 ] = 0

(3.10)
[
]
The commutation relation 𝑚 12 𝑚 43 , 𝑈 = 0 can be verified straightforwardly by
substituting the explicit form of the unitary transformation 𝑈 from Eq. (2.152),
making use of Eqs. (2.96), (2.132), and (2.148), and referring to Proposition 2.1.
Then, the Hermitian unitary operator 𝐵 admits a diagonal form both in the Majorana
basis (see Eq. (2.128)):
(
)
(
) ⨁
𝐵 𝑥 = 𝐵∗ 𝑥 = 𝑚 12 (𝑚 43 𝑥) = Γ12 Γ43 𝑥 =
( 11,𝒌,5,0 − 12,1,4,3 ) 𝑥 , (3.11)
and in the compact chiral basis (following the procedure described in Eq. (2.185)):
(
)
(
) ⨁(
)
𝐵 𝑦 = 𝐵∗ 𝑦 = 𝑚 12 (𝑚 43 𝑦) = Γ12 Γ43 𝑦 =
11ˆ𝒌 + ,1ˆ𝒌 − , ˆ
− 112
ˆ +, ˆ
ˆ− 𝑦 ,
12 − , ˆ
34+ , 34
05+ , ˆ
05 −
(3.12)
where 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), 𝑦 ∈ Span{𝑛 𝑎± } (see Eq. (2.169) and
⨁
Sect. 2.4.3), and consult Sect. 1.2.5.2 for the convention concerning
(. . . ). We
observe that:

## PDF page 81

3.2 Isomorphism of 𝔠𝔩 (4, 1) with the Even Part of 𝔠𝔩 (4, 2): 4×4 Matrix Realization of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
67

𝐵 2 𝑥 = 18 𝑥 ,

(and similarly on 𝑦) .

(3.13)

The sign is fixed by (𝐵 − 1) 18 = 0, to preserve the spinor equal to the real unit 1 of
OS .
Remarkably, we see that, for the Majorana (real) spinors 𝜉 and 𝜂, the Hermitian
form (3.11) reproduces the scalar product (3.2):
⟨𝜉, 𝜂⟩ = 𝜉 𝐴 𝐵 𝐴𝐵 𝜂 𝐵 ,

(3.14)

{
}
where 𝐴, 𝐵 = 1, 𝒌, 𝜈 ∈ 0 := 𝚤, 5 := 𝚥, 1 := ℓ𝚤, 2 := 𝚥ℓ, 3 := ℓ𝒌, 4 := ℓ
(see Eq. (2.60)-(2.62)). Similarly, in the space of 4-component pure chiral spinors3
ˆ
ˆ
ˆ
ˆ
𝜓 + = 𝜓 1𝒌 + 𝑛 ˆ + 𝜓 05+ 𝑛 ˆ + 𝜓 12+ 𝑛 ˆ + 𝜓 34+ 𝑛 ˆ displayed in the compact chiral
34+
12+
05+
1𝒌 +
basis (see Sect. 2.4.3), where:
( √
)
ˆ
ˆ
𝜓 1𝒌 + := 2 𝜓 1𝒌 + = 𝜉 1 − i𝜉 𝒌 ,
)
( √
ˆ
ˆ
𝜓 05+ := 2 𝜓 05+ = 𝜉 0 − i𝜉 5 ,
( √
)
ˆ
ˆ
𝜓 12+ := 2 𝜓 12+ = 𝜉 1 − i𝜉 2 ,
)
( √
ˆ
ˆ
𝜓 34+ := 2 𝜓 34+ = 𝜉 3 − i𝜉 4 ,
(3.15)
the Hermitian form (3.12) also allows us to reproduce the quadratic norm (3.1):
ˆ + 05+
ˆ + 12+
ˆ + 34+
𝜓 𝑎+ 𝐵 𝑎+ 𝑏+ 𝜓 𝑏+ = 𝜓 1ˆ𝒌 + 𝜓 1𝒌 + + 𝜓 05
𝜓 − 𝜓 34
𝜓
𝜓 − 𝜓 12
ˆ

ˆ

ˆ

ˆ

= 𝜉12 + (𝜉𝒌 ) 2 + (𝜉0 ) 2 + (𝜉5 ) 2 − (𝜉1 ) 2 − (𝜉2 ) 2 − (𝜉3 ) 2 − (𝜉4 ) 2
= 𝜉𝜉 ∗ = 𝜉 ∗ 𝜉 = 𝑁 (𝜉) = ⟨𝜉, 𝜉⟩ ,

(3.16)

ˆ+ , while 𝜓 stands for the complex conjugate of 𝜓.
where 𝑎 + , 𝑏 + = 1ˆ𝒌 + , ˆ
05+ , ˆ
12+ , 34

3.2 Isomorphism of 𝖈𝖑(4, 1) with the Even Part of 𝖈𝖑(4, 2): 4 × 4
Matrix Realization of 𝖘𝖚(2, 2)  𝖘𝖔(4, 2)
It looks natural to view the de Sitter (dS) Clifford algebra 𝔠𝔩(4, 1) as a Clifford
subalgebra of the conformal one 𝔠𝔩(4, 2). It turns out, however, to be advantageous
to use the known isomorphism between the even part of 𝔠𝔩(4, 2), denoted here by
𝔠𝔩 even (4, 2), and the irreducible realization C[4] of 𝔠𝔩(4, 1). Specifically, we identify
the 4 × 4-matrix realization of the generators 𝛾 𝛼 (𝛼 = 0, 1, 2, 3, 4) of 𝔠𝔩(4, 1) with
the projected “boosts” Γ 𝛼5 of the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2):

3 For reviews on Cartan simple (or Chevalley pure) 8-spinors, see Refs. [104, 105]

## PDF page 82

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

68

𝛾𝑖 := 𝛾𝑖5 = Γ𝑖5 𝐷 + ,

and

𝛾 0 := 𝛾05 = Γ05 𝐷 + ,

(3.17)

and

Γ 𝛼5 = Γ 𝛼 Γ5 ,

(3.18)

where:
𝐷+ =

1+𝐷
2

,

with 𝛼 = 0, 1, 2, 3, 4 and 𝑖 = 1, 2, 3, 4, while 𝐷 + is the projection operator on 𝔖+ ;
that is:
𝐷 + 𝔖 =: 𝔖+ ,

(3.19)

where we recall that in the chiral (complex) basis (2.169) (see also Eqs. (2.165)(2.168)):
{
}
{ }
𝔖 = Span 𝑛 𝑎± ; 𝑛 𝑎± = 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , and 𝔖+ = Span 𝑛 𝑎+ , (3.20)
1𝒌 ±

05±

12±

34±

and in the Majorana (real) basis (2.60)-(2.62) (for connection with the above basis,
see again Eqs. (2.165)-(2.168)):
{
}
{
}
𝔖 = Span 𝐴 : 𝐴 = 1, 𝒌, 0, 5, 1, 2, 3, 4 , and 𝔖+ = Span 1, 5, 2, 4 .
(3.21)
Moreover, for the definitions of 𝐷 in the chiral (complex) and Majorana (real) bases,
respectively, see Eqs. (2.184) and (2.132).
Remark 3.2 Some remarks on the map Γ 𝛼5 ↦−→ 𝛾 𝛼 (3.17) are as follows:
1. The above realization of the generators 𝛾 𝛼 of the dS Clifford algebra 𝔠𝔩(4, 1) 
𝔠𝔩 even (4, 2) follows from the identities:
{
} {
}
[
] [
]
Γ 𝛼5 , Γ𝛽5 = Γ 𝛼 , Γ𝛽 = 2𝜂 𝛼𝛽 , and Γ 𝛼5 , Γ𝛽5 = Γ 𝛼 , Γ𝛽 ,
(3.22)
where 𝜂 𝛼𝛽 = diag(−, +, +, +, +), with 𝛼, 𝛽 = 0, 1, 2, 3, 4. These relations show
that the matrix Γ5 drops out of both the anticommutation and commutation relations among the projected generators Γ 𝛼5 . Consequently the projected “boosts”
Γ 𝛼5 obey the same Clifford 𝔠𝔩(4, 1) and Lie algebra 𝔰𝔬(4, 1) relations as the
Γ 𝛼 . Hence, one can consistently regard Γ 𝛼5 as an 8 × 8-matrix representation of
𝔠𝔩(4, 1), and define the 4 × 4 matrices 𝛾𝑖 := Γ𝑖5 𝐷 + and 𝛾 0 := Γ05 𝐷 + , which provide a 4 × 4-matrix representation of 𝔠𝔩(4, 1) (and therefore of the corresponding
Lie algebra 𝔰𝔬(4, 1)).
2. Obviously, the map Γ 𝛼5 ↦−→ 𝛾 𝛼 (3.17) does not respect the Z2 grading of
𝔠𝔩(4, 2). The Clifford algebra 𝔠𝔩(4, 2) is naturally Z2 -graded, meaning it has an
even and odd part:
𝔠𝔩(4, 2) = 𝔠𝔩 even (4, 2) ⊕ 𝔠𝔩 odd (4, 2) .

(3.23)

By definition, the even subalgebra 𝔠𝔩 even (4, 2) consists of elements that can be
expressed as products of an even number of generators Γ𝜈 , while the odd subspace

## PDF page 83

3.2 Isomorphism of 𝔠𝔩 (4, 1) with the Even Part of 𝔠𝔩 (4, 2): 4×4 Matrix Realization of 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2)
69

𝔠𝔩 odd (4, 2) consists of elements formed from an odd number of generators. The
mapping in question explicitly interchanges even and odd elements, sending even
elements of 𝔠𝔩(4, 2) to odd elements of 𝔠𝔩(4, 1) and vice versa. As a result, it fails
to preserve the Z2 grading.
3. As a benefit of this 4 × 4 matrix realization of 𝔠𝔩(4, 1)  𝔠𝔩 even (4, 2), the 𝔠𝔩(4, 1)
is found to have the constant value ‘i’, which corresponds to the eigenvalue of
𝜔(4, 2) on the chiral subspace 𝔖+ :4
w(4, 1) 𝑦 := 𝛾05 𝛾15 𝛾25 𝛾35 𝛾45 𝑦
= Γ05 Γ15 Γ25 Γ35 Γ45 𝐷 + 𝑦
= Γ05 Γ12 Γ34 𝐷 + 𝑦
= 𝜔(4, 2) 𝐷 + 𝑦
= i1 𝐷 + 𝑦 ,

(3.24)

where 𝑦 ∈ Span{𝑛 𝑎± } and 1 is the unit operator in the totally isotropic space 𝔖+
spanned by the null vectors 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ .
1𝒌 + 05+ 12+ 34+
The significance of this result, and in particular the sense in which it constitutes a
genuine benefit of the present realization, merits a brief clarification. In general,
the Clifford pseudoscalar of 𝔠𝔩(4, 1) is central but need not act as a fixed scalar
on a spinor module, and its value typically depends on representation-dependent
conventions. In the present realization, however, w(4, 1) is identified with the
conformal volume element 𝜔(4, 2) restricted to the chiral subspace 𝔖+ ; since
𝜔(4, 2) is a Casimir invariant of 𝔰𝔬(4, 2), its action is fixed, yielding w(4, 1) = i1.
Thus, the 4 × 4 representation of 𝔠𝔩(4, 1) is automatically irreducible, and its
complex structure is canonically inherited from conformal chirality rather than
imposed by hand.
□
We proceed to displaying the 4 × 4-matrix realization of the relevant physical
operators of 𝔠𝔩 even (4, 2) ⊃ 𝔰𝔬(4, 2) ⊃ 𝔰𝔬(4, 1). To begin with, the 4-dimensional
projection of the Hermitian form 𝐵 (see Eq. (3.11) and (3.12)) is:
⨁
B 𝑥 := 𝐵 𝐷 + 𝑥 =
( 115 − 124 ) 𝐷 + 𝑥 ,
(3.25)
B 𝑦 := 𝐵 𝐷 + 𝑦 =

⨁(

11ˆ𝒌 + 05
ˆ + 34
ˆ + 𝐷+ 𝑦 ,
ˆ + − 112
)

(3.26)

in the Majorana 𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)) and chiral 𝑦 ∈ Span{𝑛 𝑎± }
⨁
bases, respectively. Sect. 1.2.5.2 provides the convention for (. . . ). The (diagonal)
Cartan elements of the maximal compact subalgebra 𝔰𝔬(2) ⊕ 𝔰𝔬(4) of the 𝔰𝔬(4, 2)
— specifically, in the chiral basis — are obtained respectively by projecting (2.187),
(2.188), and (2.189):
⨁(
)
(
)
𝛾05 𝑦 = Γ05 𝐷 + 𝑦 = i
𝐷 12
(3.27)
ˆ𝒌 + + 𝐷 34
ˆ + 𝐷 + 𝑦 = −iB 𝑦 ,
ˆ + 05
ˆ +1
4 Note that 𝜔 (4, 2) can be identified with the third-order Casimir invariant of 𝔰𝔬 (4, 2).

## PDF page 84

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

70

𝛾12 𝑦 = Γ12 𝐷 + 𝑦 = i

⨁(

𝛾34 𝑦 = Γ34 𝐷 + 𝑦 = i

⨁(

)
𝐷 1ˆ𝒌 + ˆ
+ 𝐷ˆ
12+ ˆ
34+ 𝐷 + 𝑦 ,
05+
)
𝐷 1ˆ𝒌 + ˆ
− 𝐷 12
ˆ+ ˆ
34+ 𝐷 + 𝑦 ,
05+

reproducing 𝜔(4, 2) = i1 (see Eq. (2.163)) and similar to Eq. (3.12):
⨁(
)
B 𝑦 = 𝛾12 𝛾43 𝑦 = Γ12 Γ43 𝐷 + 𝑦 =
11ˆ𝒌 + 05
ˆ + 34
ˆ + 𝐷+ 𝑦 .
ˆ + − 112

(3.28)

(3.29)

(3.30)

Remark 3.3 The inner product (3.16) couples the 4-dimensional
pure
)
( conformal
)
(
chiral spinors 𝜓 + in 𝔖+ to their complex conjugate 𝜓 − = 𝜓 + in 𝔖− = 𝔖+ ; the
4-dimensional representations of 𝔰𝔬(4, 1) ⊂ 𝔰𝔬(4, 2) in the chiral subspaces 𝔖+ and
𝔖− are equivalent. The covariant transformation of charge conjugation 𝜓 ↦−→ 𝜓 𝑐
(2.190), however, requires returning to the reducible 8-dimensional spinors. In this
setting, the commutant of the reducible Γ 𝛼𝛽 -realization of the dS Lie algebra 𝔰𝔬(4, 1)
is generated by the volume form 𝜔(4, 1) and Γ5 . In the Majorana basis, where
𝑥 ∈ Span{ 𝐴} (see Eqs. (2.60)-(2.62)), these read as:
𝜔(4, 1) 𝑥 = Γ05 Γ15 Γ25 Γ35 Γ45 𝑥 = Γ05 Γ12 Γ34 𝑥 = 𝜔(4, 2) 𝑥 = i𝐷 𝑥 ,
Eq. (2.156) ;

Γ5 𝑥 = 𝑚 5 𝐸 𝑥 = 𝑚 0 𝑚 1 𝑚 2 𝑚 3 𝑚 4 𝑥 =

⨁

(3.31)

(𝐸 10 + 𝐸 5𝒌 − 𝐸 14 − 𝐸 23 ) 𝑥 .
(3.32)

Note that i𝐷 and Γ5 generate a 𝔰𝔲(2) Lie algebra.

□

3.3 Positive Energy Ladder
Representations
of
(
)
𝖚(2, 2)  𝖘𝖚(2, 2)  𝖘𝖔(4, 2) ⊕ 𝖚(1) ⊂ 𝖈𝖑(4, 2) Describing
Massless Particles of Any Helicity
We now present an updated treatment of the 1969 construction [13] of irreducible
massless representations of the (U(1)-extended) conformal group U(2, 2), framed
within the context of the 𝔠𝔩(4, 2) semispinors developed in the preceding sections.
An intermediate step toward this construction was given in Ref. [106], where the Lie
algebra 𝔲(2, 2) was embedded in 𝔠𝔩(4, 1).
The idea is to view the components of the conformal chiral semispinors 𝜓 + ,
denoted here by 𝜑 and its Dirac conjugate 𝜑
˜ = 𝜑∗ B, as bosonic creation and annihi5
lation operators. More precisely, we postulate that 𝜑 ∈ 𝔖+ and 𝜑
˜ ∈ 𝔖− satisfy the
canonical commutation relations:
[ 𝑎 𝑎′ ]
[ 𝑎
]
[
]
𝜑 ,𝜑
= 0,
𝜑 ,𝜑
˜𝑎′ = 𝛿 𝑎𝑎′ ,
𝜑
˜𝑎 , 𝜑
˜𝑎′ = 0 ,
(3.33)
5 See Ref. [13] for references to earlier work on such representations, including the 1962 book by B.

Kursunoglu, which is now recognized as a key reference in the field alongside more recent sources.

## PDF page 85

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

where
𝜑
˜𝑎′ )= 𝜑∗𝑏 B𝑏𝑎′ , with 𝑎, 𝑎 ′ , 𝑏 = 1ˆ𝒌 + , ˆ
05+ , ˆ
12+ , ˆ
34+ (see Sect. 2.4.3), and
(
B = 𝐵 𝐷 + is the 4-dimensional (reduced) Hermitian form (3.26).
One can construct two series of unitary irreducible representations (UIRs) of the
𝔲(2, 2) Lie algebra with the “second-quantized” ladder operators:
𝐽 𝜇𝜈 =

)
1(
𝜑
˜ 𝛾 𝜇𝜈 𝜑 ,
2

or, more explicitly,

𝐽 𝜇𝜈 =

)
1 (
𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 𝜑 𝑏 ,
2

(3.34)

where 𝑎, 𝑏 = 1ˆ𝒌 + , ˆ
05+ , ˆ
12+ , ˆ
34+ , while 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4, 𝛾 𝜇𝜈 = −𝛾 𝜈 𝜇 , and:
(
)
𝛾𝑖5 =: 𝛾𝑖 = Γ𝑖5 𝐷 + ,

and

(
)
𝛾05 =: 𝛾 0 = Γ05 𝐷 + ,

(3.35)

and hence (as a consequence of Proposition 2.1):
𝛾𝑖 𝑗 = 𝛾𝑖5 𝛾 𝑗5 ,

and

𝛾0𝑖 = 𝛾05 𝛾𝑖5 ,

(3.36)

where 𝑖, 𝑗 = 1, 2, 3, 4.
Remark 3.4 The bilinear operators 𝐽 𝜇𝜈 introduced in Eq. (3.34) furnish an explicit
realization of the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) acting on the spinor space:6
˜ 𝛾 𝜇𝜈 𝜑
1. Algebra closure and commutation relations: The bilinears 𝐽 𝜇𝜈 = 12 𝜑
form a closed representation of the Lie algebra 𝔰𝔬(4, 2), as they satisfy the same
commutation relations as the matrix-valued generators 21 𝛾 𝜇𝜈 :

6 It is important to note that the Lie algebra 𝔲 (2, 2)  𝔰𝔲 (2, 2)

(

)
 𝔰𝔬 (4, 2) ⊕ 𝔲 (1) ⊂ 𝔠𝔩 (4, 2)
contains, in addition to the “second-quantized” conformal generators 𝐽𝜇𝜈 ∈ 𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2),
a central 𝔲 (1) generator, which commutes with all elements of the algebra. In the setting involving
the “second-quantized” ladder operators, we denote this central element by C1 . A more detailed
discussion of this point will be given later; see Eq. (3.64) and the subsequent discussion.

## PDF page 86

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

72

[

] 1[
]
𝐽 𝜇𝜈 , 𝐽𝜆𝜎 =
𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 𝜑 𝑏 , 𝜑
˜𝑐 (𝛾𝜆𝜎 ) 𝑑𝑐 𝜑 𝑑
4
[
]
]
1[
1
= 𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 𝜑 𝑏 , 𝜑
˜𝑐 (𝛾𝜆𝜎 ) 𝑑𝑐 𝜑 𝑑 +
𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 , 𝜑
˜𝑐 (𝛾𝜆𝜎 ) 𝑑𝑐 𝜑 𝑏 𝜑 𝑑
4
4⏟
⏟
⏞⏞
⏟
⏞⏞
⏟
=0

= 𝛿𝑐𝑏 (𝛾𝜆𝜎 ) 𝑑𝑐

[
] 1
[
]
1
˜𝑐 (𝛾𝜆𝜎 ) 𝑑𝑐 𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 𝜑 𝑏 , 𝜑 𝑑 + 𝜑
˜𝑐 (𝛾𝜆𝜎 ) 𝑑𝑐 𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 , 𝜑 𝑑 𝜑 𝑏
+ 𝜑
4
⏟ ⏞⏞ ⏟ 4
⏟
⏞⏞
⏟
=0

=

= − 𝛿𝑎𝑑 (𝛾𝜇𝜈 ) 𝑏𝑎

1
𝜑
˜ (𝛾 𝜇𝜈 ) 𝑏𝑎 (𝛾𝜆𝜎 ) 𝑑𝑏 − (𝛾𝜆𝜎 ) 𝑏𝑎 (𝛾 𝜇𝜈 ) 𝑑𝑏 𝜑 𝑑
4 𝑎
⏟
⏞⏞
⏟
(

)

by reassigning the dummy indices

]
1 [
= 𝜑
˜ 𝛾 𝜇𝜈 , 𝛾𝜆𝜎 𝜑
4
)
1 (
˜ 𝜂 𝜈𝜆 𝛾 𝜇 𝜎 − 𝜂 𝜇𝜆 𝛾 𝜈 𝜎 − 𝜂 𝜈 𝜎 𝛾 𝜇𝜆 + 𝜂 𝜇 𝜎 𝛾 𝜈𝜆 𝜑
= 𝜑
2
(
)
= 𝜂 𝜈𝜆 𝐽 𝜇 𝜎 − 𝜂 𝜇𝜆 𝐽𝜈 𝜎 − 𝜂 𝜈 𝜎 𝐽 𝜇𝜆 + 𝜂 𝜇 𝜎 𝐽𝜈𝜆 ,

(3.37)

where, again, 𝜂 𝜇𝜈 is the mostly ‘+’ metric tensor in R4,2 . Note that to derive the
identity above, we make use of the following formula:
[ 𝐴𝐵, 𝐶𝐷] = 𝐴[𝐵, 𝐶]𝐷 + [ 𝐴, 𝐶]𝐵𝐷 + 𝐶 𝐴[𝐵, 𝐷] + 𝐶 [ 𝐴, 𝐷]𝐵 .

(3.38)

2. Chirality preservation: The full set {𝛾 𝜇𝜈 } preserves chirality, since each 𝛾 𝜇𝜈
[
]
commutes with the “chirality matrix” 𝜔(4, 2), that is 𝛾 𝜇𝜈 , 𝜔(4, 2) = 0 (see also
Eqs. (2.186) and (2.190)). Specifically, we have:
(
)
(
)
(
)
𝜔(4, 2) 𝛾 𝜇𝜈 𝜑 = 𝛾 𝜇𝜈 𝜔(4, 2)𝜑 = +i 𝛾 𝜇𝜈 𝜑 ,
(3.39)
(

)
(
)
(
)
𝜑
˜ 𝛾 𝜇𝜈 𝜔(4, 2) = 𝜑
˜ 𝜔(4, 2) 𝛾 𝜇𝜈 = −i 𝜑
˜ 𝛾 𝜇𝜈 ,

(3.40)

(
)
(
)
meaning that each chiral subspace 𝔖+ = Span{𝜑} or 𝔖− = Span{ 𝜑
˜}
is invariant under the action of 𝛾 𝜇𝜈 . Therefore, the bilinear operators 𝐽 𝜇𝜈 =
1
˜ 𝛾 𝜇𝜈 𝜑) are well-defined on each chiral subspace, in the sense that 𝛾 𝜇𝜈 does not
2 (𝜑
mix the chiralities, yielding a closed representation of 𝔰𝔬(4, 2) on each subspace.
3. Faithfulness of the chiral spinor representation: The chiral spinor representation
of 𝔰𝔬(4, 2), obtained by restricting the action of the matrices 𝛾 𝜇𝜈 to either 𝔖+
or 𝔖− is not only closed under commutation but also faithful. This can be seen
from the following observations:
a. Each chiral spinor subspace 𝔖± is a 4-dimensional complex vector space.
Therefore, the algebra of all linear operators on it, End(𝔖± ), is isomorphic to
Mat(4, C) and has complex dimension 16.

## PDF page 87

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

b. The 15 antisymmetric matrices 𝛾 𝜇𝜈 , obtained by restricting to a fixed chiral subspace, are linearly independent and satisfy the 𝔰𝔬(4, 2) Lie algebra
commutation relations.
Therefore, the image of the representation of 𝔰𝔬(4, 2) on either 𝔖+ or 𝔖− is a
15-dimensional subalgebra of End(𝔖± ). Since the kernel of the map is trivial,
the representation is injective, establishing a one-to-one correspondence between
the elements of 𝔰𝔬(4, 2) and their images in End(𝔖± ), and thus confirming the
faithfulness of the representation.
Note: This key fact will be illustrated explicitly in the realization presented in
Eqs. (3.99)-(3.114).
Note: If the chiral spinor representation on either 𝔖+ or 𝔖− were not faithful, then
distinct elements of 𝔰𝔬(4, 2) could act identically on the corresponding subspace.
˜ 𝛾 𝜇𝜈 𝜑) would generate only a smaller algebra
In that case, the bilinears 𝐽 𝜇𝜈 = 21 ( 𝜑
— either the quotient of 𝔰𝔬(4, 2) by the kernel of the representation, or, in certain
realizations, a proper subalgebra corresponding to a restricted set of generators.
In other words, part of the Lie algebra would be “invisible” to the spinors, and the
representation would effectively “forget” that portion of the algebraic structure.
□
From now on, we focus on a series of the U(2, 2) representations characterized by
7
a lowest weight state, treated as a “Fock vacuum”
|0SO(4)
(
) ⟩ that transforms as a singlet
under the maximal compact subgroup S U(2) × U(2)  SO(4) × U(1) of SU(2, 2),
more specifically under the SO(4) factor, and such that the conformal Hamiltonian
𝐻 8 (i.e., the U(1) generator of the subgroup) is bounded from below:
𝐻 := i𝐽05 =

) 1(
)
1(
𝜑
˜ i𝛾05 𝜑 = 𝜑
˜ i𝛾 0 𝜑 ⩾ 1 ,
2
2

and

(𝐻 − 1) |0SO(4) ⟩ = 0 . (3.41)

The identification of |0SO(4) ⟩ with a “Fock vacuum” presupposes singling out the
creation and annihilation:
P+ 𝜑 |0SO(4) ⟩ = 0 = 𝜑
˜ P− |0SO(4) ⟩ ,

where

P± =

1±B
2

.

(3.42)

Note: A second series of U(2, 2) representations arises, corresponding to highestweight ladder representations, in which the conformal Hamiltonian is negative definite. This situation occurs when the roles of the projectors P+ and P− are interchanged. However, this case will not be considered in the present work.
To make the subsequent discussion more transparent, we shall display a realization
of the 4 × 4 matrices 𝛾𝑖 (with 𝑖 = 1, 2, 3, 4) in accord with the construction (3.17). It
follows from Eqs. (2.190), (2.192), and (2.148) that:

7 In physics and mathematics — especially in group theory, quantum mechanics, and representation

theory — a singlet means a state or object that transforms trivially under the action of a group.
8 Its significance was recognized early on by Irving Segal (1918-1998) albiet in a rather speculative
context [107].

## PDF page 88

74

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

𝐶 Γ𝜈 = Γ𝜈 𝐶 ,

with 𝐶 = −i𝑆 = i𝑚 0 𝑚 1 𝑚 3 ,

(3.43)

for 𝜈 = 0, 5, 1, 2, 3, 4. On the other hand, from Eq. (2.156) and (2.157), we have,
respectively:
Γ𝜇 ′ = 𝑚 𝜇 ′ 𝐸 ,

for

𝜇′ = 5, 4, 2 ,

Γ𝜈 ′ = i𝑚 𝜈 ′ 𝐷 ,

for

𝜈 ′ = 0, 1, 3 .

(3.44)

By Proposition 2.2 and in fact its natural extension, we obtain:
Γ𝜇 ′ 𝐶 = 𝐶 Γ𝜇 ′

=⇒

Γ𝜇 ′ = Γ𝜇 ′ ,

for

𝜇′ = 5, 4, 2 ,

Γ𝜈 ′ 𝐶 = −𝐶 Γ𝜈 ′

=⇒

Γ𝜈 ′ = −Γ𝜈 ′ ,

for

𝜈 ′ = 0, 1, 3 .

(3.45)

These results imply that the 8 × 8 matrices Γ2 , Γ4 , and Γ5 are real, whereas Γ0 , Γ1 ,
and Γ3 are purely imaginary. Correspondingly, we find:
𝛾0 = −𝛾0 ,

𝛾𝑖 = (−1) 𝑖 𝛾𝑖 ,

and

(3.46)

where 𝑖 = 1, 2, 3, 4.
Proposition 3.1 With the above in mind, and under the aforementioned convention
— namely, the basis ordered as 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ — we introduce the following
1𝒌 + 05+ 12+ 34+
4 × 4 matrix representations for the 𝛾-matrices:
(
)
(
)
𝜎 0
𝛾0 = −𝛾 0 := −𝛾05 = i𝜎3 ⊗ 𝜎0 = i 0
= iB ,
(3.47)
0 −𝜎0
(

)
0 E𝑖
𝛾𝑖 := 𝛾𝑖5 = ∗
,
E𝑖 0

𝑖 = 1, 2, 3, 4 ,

(3.48)

where:
(

)
01
E1 = i𝜎1 = i
,
10
(
)
0 −i
E2 = i𝜎2 = i
,
i 0
(
)
1 0
E3 = i𝜎3 = i
,
0 −1
( )
10
E4 = 𝜎0 =
= 12 ,
01

(3.49)

with E𝑖 representing a set of matrices that mirror the algebraic structure of quaternionic units but with crucial sign differences. Specifically, they obey a twisted
quaternionic algebra — sometimes referred to as the “opposite” or “conjugatequaternionic” system — in which the products of the imaginary units acquire an

## PDF page 89

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

overall sign flip compared to the standard quaternion multiplication rules; this reversal, highlighted below using quotation marks (‘−’). This subtle modification leads
to the following algebraic relations:
(E1 ) 2 = (E2 ) 2 = (E3 ) 2 = −E4 ,
E1 E2 = −E2 E1 = ‘−’E3 ,
E2 E3 = −E3 E2 = ‘−’E1 ,
E3 E1 = −E1 E3 = ‘−’E2 ,
E1 E4 = E4 E1 = E1 ,
E2 E4 = E4 E2 = E2 ,
E3 E4 = E4 E3 = E3 ,
∗
E1 = −E1 , E2∗ = −E2 ,
E3∗ = −E3 , E4∗ = E4 .

(3.50)

Correspondingly, the 8 × 8 Γ-matrices are set to be:
Γ0 = 𝜎1 ⊗ 𝛾 0 ,
)
0 −1
𝜖 =
,
1 0

Γ5 = 𝜖 ⊗ 14 ,

𝜖 = i𝜎2 ,

Γ𝑖 = 𝜎1 ⊗ 𝛾𝑖 ,

𝑖 = 1, 2, 3, 4 .

∗

∗

(

(3.51)

Here, and before proceeding any further, it is perhaps worth noting that the above
realization of E1 , . . . , E4 as the “opposite” or “conjugate-quaternionic” structure is
not unique. For example, one may equally identify them with the quaternion basis
elements 𝚤, − 𝚥, 𝒌, 1, respectively.
Proof (consistency check). The consistency of the above setup is ensured by the
fact that all algebraic relations within each realization — namely, among the 𝛾 and
among the Γ matrices — are explicitly satisfied. For example:
1. Recalling that the basis used in the matrix representations (3.47) and (3.48) is
ordered as 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , one readily verifies that the matrix realization of
1𝒌 + 05+ 12+ 34+
𝛾05 in (3.47) precisely coincides with that given in (3.27).
2. The matrix representations given in (3.47) and (3.48) for 𝛾0 := −𝛾05 and 𝛾𝑖 := 𝛾𝑖5
(𝑖 = 1, 2, 3, 4) satisfy the commutation relations of the Lie algebra 𝔰𝔲(2, 2) 
𝔰𝔬(4, 2) — more specifically, those of the subalgebra 𝔰𝔬(4, 1) ⊂ 𝔰𝔬(4, 2); for
instance, we have:
(
)
[
]
E 0
𝛾15 , 𝛾25 = 2 3
= 2𝛾12 , (see Eq. (3.28)) ,
(3.52)
0 E3
(
)
[
]
E 0
𝛾35 , 𝛾45 = 2 3
= 2𝛾34 , (see Eq. (3.29)) .
(3.53)
0 −E3
3. In view of the above, one can further verify that:

## PDF page 90

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

76

(
w(4, 1) = 𝛾05 𝛾12 𝛾34 = −i

𝜎0 0
0 −𝜎0

)(

E3 0
0 E3

)(

)
E3 0
= i14 ,
0 −E3

(3.54)

or similarly considering the realization given in (3.51):
𝜔(4, 2) = Γ0 Γ5 Γ1 . . . Γ4 = i𝜎3 ⊗ 14 = i𝐷 ,

(𝐷 = 𝜎3 ⊗ 14 ) ,

(3.55)

which is compatible with (3.24).
4. The Γ-matrices (3.51) satisfy the anticommutation relations of the Clifford algebra
𝔠𝔩(4, 2), namely:
{
}
Γ𝜇 , Γ𝜈 = 2𝜂 𝜇𝜈 1 ,
(3.56)
where, as before, the indices run over 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4, and the metric is
𝜂 𝜇𝜈 = diag(−1, −1, +1, +1, +1, +1).
5. Lastly, with the above setup, one verifies that:
𝛾𝑖5 = Γ𝑖5 𝐷 + = Γ𝑖 Γ5 𝐷 + = 𝛾𝑖 ,

𝛾05 = Γ05 𝐷 + = Γ0 Γ5 𝐷 + = 𝛾 0 . (3.57)

and

□
In the B-diagonal basis, ordered as 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ , 𝑛 ˆ (see Eq. (3.47)), we
1𝒌 + 05+ 12+ 34+
implement (3.42) by introducing two types of creation and annihilation operators 𝔞
(resp. 𝔞 ∗ ) and 𝔟 (resp. 𝔟∗ ):
( )
(
)
𝔞
𝜑 = ∗ , and 𝜑
˜ = 𝜑∗ B = 𝔞 ∗ −𝔟 ,
(3.58)
𝔟
where:9
(
)
𝔞 = 𝔞 𝐴 ; 𝐴 = 1, 2 ,

and

(
)
𝔞 ∗ = 𝔞 ∗𝐴 ; 𝐴 = 1, 2 ,

(3.59)

(
)
𝔟 = 𝔟 𝐵 ; 𝐵 = 1, 2 ,

and

(
)
𝔟∗ = 𝔟∗𝐵 ; 𝐵 = 1, 2 ,

(3.60)

such that the nonvanishing canonical commutation relations, consistent with those
in Eq. (3.33), are:
[ 𝐴′ ∗ ]
[ 𝐵′ ∗ ]
′
𝐵′
𝔞 , 𝔞 𝐴 = 𝛿 𝐴𝐴 ,
𝔟 , 𝔟𝐵 = 𝛿𝐵
.
(3.61)
Moreover, consistent with Eq. (3.42), we have:
𝔞 𝐴 |0SO(4) ⟩ = 𝔟 𝐵 |0SO(4) ⟩ = 0 ,

⟨0SO(4) |𝔞 ∗𝐴 = ⟨0SO(4) |𝔟∗𝐵 = 0 .

(3.62)

On this basis, the conformal Hamiltonian
𝐻 (3.41)
(
) — namely, the U(1) generator
of the maximal compact subgroup S U(2) × U(2)  SO(4) × U(1) of SU(2, 2) —
9 It is clear that the index 𝐴 here must be distinguished from the one previously used to label the

set of split-octonion units (see Eqa. (2.60)-(2.62)).

## PDF page 91

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

takes the explicit form:
𝐻 = i𝐽05 =

) 1(
) 1(
)
1(
𝜑
˜ i𝛾05 𝜑 = 𝜑
˜ i𝛾 0 𝜑 = 𝔞 ∗ 𝔞 + 𝔟 𝔟∗
2
2
2
)
1(
= 𝔞 1∗ 𝔞 1 + 𝔞 2∗ 𝔞 2 + 𝔟1 𝔟∗1 + 𝔟2 𝔟∗2 , (3.63)
2

which explicitly satisfies (𝐻 − 1) |0SO(4) ⟩ = 0.
For an
( irreducible) representation (IR) of U(2, 2), the Lie algebra 𝔲(2, 2) 
𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) includes, in addition to the conformal generators
𝐽 𝜇𝜈 ∈ 𝔰𝔲(2, 2)  𝔰𝔬(4, 2), a central 𝔲(1) generator which commutes with all elements of the algebra. We denote this central element by C1 , which takes the explicit
form:10
C1 = 𝜑
˜ 𝜑 = 𝔞 ∗ 𝔞 − 𝔟 𝔟∗ = 𝔞 ∗ 𝔞 − (𝔟∗ 𝔟 + 2) .

(3.64)

Following steps analogous to those used in deriving Eq. (3.37), one readily verifies
that:
[
]
𝐽 𝜇𝜈 , C1 = 0 ,
(3.65)
for all 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4. It is important to emphasize that the “second-quantized”
ladder operator C1 (which belongs to 𝔲(2, 2) but not to 𝔰𝔲(2, 2)) serves as the
representative of the pseudoscalar (volume form) of 𝐸 = 𝑀 (4, 2), as defined in Eq.
(2.96), within this framework.
The normal ordering in (3.64) ensures that C1 is a Hermitian operator with a
well-defined spectrum. Since the bosonic operators 𝑁𝔞 := 𝔞 ∗ 𝔞 and 𝑁𝔟 := 𝔟∗ 𝔟, which
act on the Fock space, are number operators with non-negative integer eigenvalues,
their difference has integer eigenvalues in the Fock space realization. Thus, we can
write:
{
}
1
(3.66)
𝔞 ∗ 𝔞 − 𝔟∗ 𝔟 =: 2𝜆 , with 𝜆 ∈ Z = 0, ± 12 , ±1, . . . .
2
Substituting into Eq. (3.64), we obtain:
C1 = 𝜑
˜ 𝜑 = 𝔞 ∗ 𝔞 − 𝔟 𝔟∗ = 𝔞 ∗ 𝔞 − 𝔟∗ 𝔟 − 2 =: 2(𝜆 − 1) ∈ Z .

(3.67)

Notably, this quantized parameter 𝜆 plays a fundamental role in classifying the
UPEIRs of 𝔲(2, 2), and will later be identified as the “hilicity” — the conformal
analog of helicity — characterizing massless conformal particles in 4 dimensions
[13].

10 At this point, it is important to emphasize a subtle but significant detail:

[

] [
] [
] [
]
𝔟, 𝔟∗ = 𝔟1 + 𝔟2 , 𝔟∗1 + 𝔟∗2 = 𝔟1 , 𝔟∗1 + 𝔟2 , 𝔟∗2 = 2 .

## PDF page 92

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

78

Remark 3.5 The fact that C1 assumes a fixed integer value in any IR of 𝔲(2, 2)
reflects a deeper principle rooted in the representation theory of Lie groups, as
outlined in the following steps:
1. The generator C1 lies in the center of 𝔲(2, 2), as it commutes with all elements
of the algebra.
2. By Schur’s lemma, in any IR of 𝔲(2, 2), such a central operator must act as a
scalar multiple of the identity.
3. Therefore, in an IR of 𝔲(2, 2), all states are eigenstates of C1 with a fixed eigenvalue.
4. To ensure that this representation lifts to a single-valued representation 𝑈 of the
Lie group U(2, 2) (and not just of its algebra), the exponential of the central
generator must be well-defined and single-valued:11
𝑈 (𝜃) = 𝑒 i𝜃 C1 ,

with 𝑈 (𝜃 + 2𝜋) = 𝑈 (𝜃) .

(3.68)

This periodicity condition requires:
𝑒 2i 𝜋 C1 = 1

=⇒

C1 ∈ Z .

(3.69)

Hence, in any IR of 𝔲(2, 2), the eigenvalue of the central generator C1 must be
an integer.
□
Proposition 3.2 The higher-order Casimir invariants of the ladder-type UPEIRs of
𝔰𝔲(2, 2) are polynomial functions of the parameter 𝜆, which labels the eigenvalue of
the central 𝔲(1) generator C1 of 𝔲(2, 2). It turns out that this is also true for the dS
subalgebra 𝔰𝔭(2, 2) ⊂ 𝔰𝔲(2, 2). In fact, invariants of 𝔰𝔭(2, 2) and 𝔰𝔲(2, 2) are both
integer multiplies of:
𝐽 𝛼5 𝐽 𝛼5 =

1
(C1 ) 2 + C1 = (𝜆 − 1) 2 + 2(𝜆 − 1) = (𝜆 − 1) (𝜆 + 1) = 𝜆2 − 1 , (3.70)
4

such that:
1
C2𝔰𝔭(2,2) = − 𝐽 𝛼𝛽 𝐽 𝛼𝛽 = −2(𝜆2 − 1) ,
2

(3.71)

and:
1
1
C2𝔰𝔲 (2,2) = − 𝐽 𝜇𝜈 𝐽 𝜇𝜈 = − 𝐽 𝛼𝛽 𝐽 𝛼𝛽 −𝐽 𝛼5 𝐽 𝛼5 = −3(𝜆2 − 1) ,
2
2
⏟ ⏞⏞ ⏟

(3.72)

𝔰𝔭(2,2)

= C2

where 𝛼, 𝛽 = 0, 1, 2, 3, 4 and 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4.

11 The presence of ‘i’ in the exponent, together with the Hermiticity of
(
)∗

representation 𝑈 ( 𝜃 ) is unitary; 𝑈 ( 𝜃 ) 𝑈 ( 𝜃 )

= 1.

C1 , ensures that the

## PDF page 93

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

This proposition reflects a general feature of IRs, where Casimir operators act as
scalars determined by the representation labels. As already pointed out, physically,
𝜆 plays the role of a helicity-like quantum number, so these Casimir eigenvalues
encode invariant properties of massless conformal fields classified by helicity 𝜆.
Proof — Step I (proof of Eq. (3.72)). Starting with Eq. (3.72), we observe that the
proof rests on the following essential tensor identity:
(𝛾 𝜇𝜈 ) 𝑏𝑎 (𝛾 𝜇𝜈 ) 𝑑𝑐 = A 𝛿 𝑑𝑎 𝛿 𝑏𝑐 + B 𝛿 𝑏𝑎 𝛿 𝑑𝑐 ,

(3.73)

[
]
where A and B are constants to be determined and 𝛾 𝜇𝜈 = 12 𝛾 𝜇 , 𝛾 𝜈 . Let us first
justify the validity of this ansatz.
In even-dimensional spaces of dimension d (as in our case, d = 6), the Dirac
spinor representation has dimension 𝑁 = 2d/2 , so the space of all 𝑁 × 𝑁 matrices
acting on spinors has dimension 𝑁 2 = 2d . The corresponding Clifford algebra
provides a natural basis for this matrix space. Strictly speaking, it consists of the
antisymmetrized products of gamma matrices:
{
}
1, 𝛾 𝜇 , 𝛾 𝜇𝜈 , 𝛾 𝜇𝜈𝜌 , . . . , 𝛾 𝜇1 ...𝜇d ,
(3.74)
which are linearly independent and span the entire space of operators∑
on spinor
( ) space;
one observes that the number of independent elements in this set is d𝑘=0 d𝑘 = 2d =
𝑁 2 , exactly matching the dimension of the matrix space. Consequently, any matrix
𝑀 acting on spinors can be expressed as a linear combination of the corresponding
Clifford basis elements:
𝑀 = 𝑎 1 + 𝑏 𝜇 𝛾 𝜇 + 𝑐 𝜇𝜈 𝛾 𝜇𝜈 + . . . ,

(3.75)

for some coefficients 𝑎, 𝑏 𝜇 , 𝑐 𝜇𝜈 , · · · ∈ C.
With these observations in mind, let us now return to the expression:
(𝛾 𝜇𝜈 ) 𝑏𝑎 (𝛾 𝜇𝜈 ) 𝑑𝑐 ,

(3.76)

which, by the preceding discussion, must be expressible as a linear combination of
the basis elements of the corresponding Clifford algebra, that is, 𝔠𝔩(4, 2). Because
the Lorentz indices 𝜇, 𝜈 are fully contracted, the resulting object must be a Lorentz
scalar. This rules out any terms involving uncontracted gamma matrices such as 𝛾 𝜇 ,
𝛾 𝜇𝜈𝜌 , etc., which would transform as Lorentz tensors and hence violate the scalar
nature of the left-hand side. On the other hand, the spinor-index structure of the
right-hand side must also be built from Lorentz-invariant tensors in spinor space. In
the absence of additional invariant structures (e.g., a charge-conjugation matrix 𝐶 or
chirality projectors; as in our setup12 ), the only such invariant tensors are Kronecker
deltas:
𝛿 𝑏𝑎 ,

𝛿 𝑑𝑐 ,

𝛿 𝑑𝑎 ,

𝛿 𝑏𝑐 .

12 Recall that we work with IRs of the conformal algebra realized on the chiral subspace 𝔖

(3.77)
+.

## PDF page 94

80

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

Out of these, the combinations 𝛿 𝑑𝑎 𝛿 𝑏𝑐 and 𝛿 𝑏𝑎 𝛿 𝑑𝑐 are linearly independent and span
the space of Lorentz-invariant rank-(2, 2) spinor tensors.
Finally, note that the left-hand side is symmetric under the simultaneous exchange
(𝑎 ↔ 𝑐, 𝑏 ↔ 𝑑). This symmetry must be preserved by the right-hand side. Indeed,
both 𝛿 𝑑𝑎 𝛿 𝑏𝑐 and 𝛿 𝑏𝑎 𝛿 𝑑𝑐 are symmetric under this exchange:
(𝑎↔𝑐, 𝑏↔𝑑)

𝛿 𝑑𝑎 𝛿 𝑏𝑐 −−−−−−−−−−→ 𝛿 𝑏𝑐 𝛿 𝑑𝑎 = 𝛿 𝑑𝑎 𝛿 𝑏𝑐 ,
(𝑎↔𝑐, 𝑏↔𝑑)

𝛿 𝑏𝑎 𝛿 𝑑𝑐 −−−−−−−−−−→ 𝛿 𝑑𝑐 𝛿 𝑏𝑎 = 𝛿 𝑏𝑎 𝛿 𝑑𝑐 .

(3.78)

(3.79)

This confirms that no additional index structures are needed, and the ansatz used in
the expansion (3.73) is the most general form consistent with Lorentz invariance and
spinor symmetry.
With the expansion (3.73) established, we now aim to determine the constants A
and B. To this end, we make use of standard trace identities of the Clifford algebra in
d dimensions (applicable to both odd and even d; here d = 6). The general identity
in d dimensions, for spinors of dimension 𝑁 (here 𝑁 = 413 ), reads:
(
)
d(d − 1)
,
Tr 𝛾 𝜇𝜈 𝛾 𝜇𝜈 = 𝑁
2

with

𝜇 < 𝜈,

(3.80)

0 ≤ 𝜇 < 𝜈 ≤ 5.

(3.81)

where for 𝔰𝔬(4, 2), with d = 6 and 𝑁 = 4, is:
(
)
6×5
Tr 𝛾 𝜇𝜈 𝛾 𝜇𝜈 = 4
= 60 ,
2

with

Keeping this in mind, let us proceed by taking two traces of (3.73):
1. Contract 𝑎 = 𝑑, 𝑏 = 𝑐:
60 = 16A + 4B .

(3.82)

0 = 4A + 16B ,

(3.83)

2. Contract 𝑎 = 𝑏, 𝑐 = 𝑑:

)
(
)
(
since Tr 𝛾 𝜇𝜈 = Tr 21 [𝛾 𝜇 , 𝛾 𝜈 ] = 0 (see Eqs. (2.11) and (2.13)).
Accordingly, we obtain A = 4 and B = −1, and hence:
(𝛾 𝜇𝜈 ) 𝑏𝑎 (𝛾 𝜇𝜈 ) 𝑑𝑐 = 4 𝛿 𝑑𝑎 𝛿 𝑏𝑐 − 𝛿 𝑏𝑎 𝛿 𝑑𝑐 .

(3.84)

Equipped with the above expansion, together with Eqs. (3.33) and (3.34), we are
now in a position to establish Eq. (3.72) rigorously:

13 Since we focus exclusively on the IR of 𝔰𝔬 (4, 2) realized on the chiral subspace 𝔖 .
+

## PDF page 95

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

− C2𝔰𝔲 (2,2) =

∑︁
1 𝜇𝜈
𝐽 𝐽 𝜇𝜈 =
𝐽 𝜇𝜈 𝐽 𝜇𝜈
2
0≤ 𝜇<𝜈 ≤5
)
1 ( 𝜇𝜈 ) (
𝜑
˜𝛾 𝜑 𝜑
˜ 𝛾 𝜇𝜈 𝜑
4
)(
)
1(
𝜑
˜𝑎 (𝛾 𝜇𝜈 ) 𝑏𝑎 𝜑 𝑏 𝜑
˜𝑐 (𝛾 𝜇𝜈 ) 𝑑𝑐 𝜑 𝑑
=
4
)
(
)(
)(
1
= 𝜑
˜𝑎 𝜑 𝑏 𝜑
˜𝑐 𝜑 𝑑 𝛿 𝑑𝑎 𝛿 𝑏𝑐 − 𝛿 𝑏𝑎 𝛿 𝑑𝑐
4
(
) 1
˜𝑎 𝜑 𝑎 ) ( 𝜑
˜𝑐 𝜑 𝑐 )
= 𝜑
˜𝑎 𝜑 𝑏 𝜑
˜𝑏 𝜑 𝑎 − ( 𝜑
4
(
)
[
]
1
= 𝜑
˜𝑎 𝜑
˜𝑏 𝜑 𝑏 𝜑 𝑎 + 𝜑
˜𝑎 𝜑 𝑏 , 𝜑
˜𝑏 𝜑 𝑎 − ( 𝜑
˜𝑎 𝜑 𝑎 ) ( 𝜑
˜𝑐 𝜑 𝑐 )
4
⏟ ⏞⏞ ⏟
=

= 𝛿𝑏𝑏 = 4

[
]
1
= 𝜑
˜𝑏 𝜑 𝑏 ( 𝜑
˜𝑎 𝜑 𝑎 ) + 𝜑
˜𝑏 𝜑
˜𝑎 , 𝜑 𝑏 𝜑 𝑎 + 4 ( 𝜑
˜𝑎 𝜑 𝑎 ) − ( 𝜑
˜𝑎 𝜑 𝑎 ) ( 𝜑
˜𝑐 𝜑 𝑐 )
4
⏟ ⏞⏞ ⏟
(

)

= − 𝛿𝑎𝑏

3(

)

𝜑
˜𝑏 𝜑 𝑏 ( 𝜑
˜𝑎 𝜑 𝑎 ) + 3 ( 𝜑
˜𝑎 𝜑 𝑎 )
)
1
2
= 3 (C1 ) + C1 = 3(𝜆2 − 1) .
4

=

4(

(3.85)

— Step II (proof of Eq. (3.71)). Here, we turn our attention to the second identity
stated in the proposition, namely Eq. (3.71). To begin, and in analogy with expression
(3.34), we express 𝐽 𝛼𝛽 in terms of spinor bilinears as:
𝐽 𝛼𝛽 =

)
1(
𝜑
˜ 𝛾 𝛼𝛽 𝜑 ,
2

𝛾 𝛼𝛽 =

]
1[
𝛾 𝛼 , 𝛾𝛽 .
2

(3.86)

Under this identification, the generators 𝐽 𝛼𝛽 form a closed and complete set for the
Lie algebra 𝔰𝔭(2, 2)  𝔰𝔬(4, 1), as can be demonstrated using arguments analogous
to those in Remark 3.4.
It is important to emphasize that in odd-dimensional spaces of dimension d (for
example, d = 5, relevant for the dS case), the Clifford algebra, just as in the evendimensional case discussed earlier, provides a complete basis for 𝑁 × 𝑁 matrices
acting on spinor space, where 𝑁 = 2 ⌊d/2⌋ . This basis consists of the antisymmetrized
products of gamma matrices (see Eq. (3.74)). Consequently, any spinor-valued matrix
can be expanded in terms of this basis. However, unlike in even dimensions, there
is no chirality operator in odd dimensions, so the corresponding representation is
irreducible by construction.
Following the same reasoning as in the previous step, we perform the expansion:
(𝛾 𝛼𝛽 ) 𝑏𝑎 (𝛾 𝛼𝛽 ) 𝑑𝑐 = A ′ 𝛿 𝑑𝑎 𝛿 𝑏𝑐 + B ′ 𝛿 𝑏𝑎 𝛿 𝑑𝑐 ,

(3.87)

## PDF page 96

82

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

where, again, A ′ and B ′ are constants to be determined. We take two traces of
(3.87):
1. Contract 𝑎 = 𝑑, 𝑏 = 𝑐:
40 = 16A ′ + 4B ′ ,

(3.88)

where we have used Eq. (3.80), with d = 5 and 𝑁 = 4.
2. Contract 𝑎 = 𝑏, 𝑐 = 𝑑:
0 = 4A ′ + 16B ′ .

(3.89)

We find A ′ = 38 and B ′ = − 23 , and hence:
(𝛾 𝜇𝜈 ) 𝑏𝑎 (𝛾 𝜇𝜈 ) 𝑑𝑐 =

8 𝑎 𝑐 2 𝑎 𝑐
𝛿 𝛿 − 𝛿 𝛿 .
3 𝑑 𝑏 3 𝑏 𝑑

(3.90)

Then, the proof of Eq. (3.71) proceeds as follows:
− C2𝔰𝔭(2,2) =

∑︁
1 𝛼𝛽
𝐽 𝐽 𝛼𝛽 =
𝐽 𝛼𝛽 𝐽 𝛼𝛽
2
0≤ 𝛼<𝛽≤4
)
1 ( 𝛼𝛽 ) (
𝜑
˜𝛾 𝜑 𝜑
˜ 𝛾 𝛼𝛽 𝜑
=
4
)
)(
1(
=
𝜑
˜𝑎 (𝛾 𝛼𝛽 ) 𝑏𝑎 𝜑 𝑏 𝜑
˜𝑐 (𝛾 𝛼𝛽 ) 𝑑𝑐 𝜑 𝑑
4
)
)(
)(
2(
1 𝑎 𝑐
𝑏
𝑑
𝑎 𝑐
=
𝜑
˜𝑎 𝜑
𝜑
˜𝑐 𝜑
𝛿𝑑 𝛿𝑏 − 𝛿𝑏 𝛿𝑑
3
4
(following analogous steps to those in Eq. (3.85))
(
)
2
1
2
= × 3 (C1 ) + C1 = 2(𝜆2 − 1) .
(3.91)
3
4

— Step III (proof of Eq. (3.70)). Finally, we turn to Eq. (3.70). We have the
following expansion:
𝐽 𝛼5 =

)
1(
𝜑
˜ 𝛾 𝛼5 𝜑 ,
2

(3.92)

which follows directly from Eqs. (3.34) and (3.86) by construction. As in the previous
steps, the proof proceeds with the key expansion:
(𝛾 𝛼5 ) 𝑏𝑎 (𝛾 𝛼5 ) 𝑑𝑐 = A ′′ 𝛿 𝑑𝑎 𝛿 𝑏𝑐 + B ′′ 𝛿 𝑏𝑎 𝛿 𝑑𝑐 ,

(3.93)

where, once again, A ′′ and B ′′ denote constants to be determined. To fix their values,
we take two independent traces of Eq. (3.93):
1. Contract 𝑎 = 𝑑, 𝑏 = 𝑐:

## PDF page 97

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

20 = 16A ′′ + 4B ′′ ,

(3.94)

where, to obtain the left-hand side, we have used Eq. (2.13) together with the
results established earlier in this proof; that is:
(
)
(
)
Tr 𝛾 𝛼5 𝛾 𝛼5 = Tr 𝛾 𝜇𝜈 𝛾 𝜇𝜈 − 𝛾 𝛼𝛽 𝛾 𝛼𝛽
(
)
(
)
= Tr 𝛾 𝜇𝜈 𝛾 𝜇𝜈 − Tr 𝛾 𝛼𝛽 𝛾 𝛼𝛽 = 60 − 40 = 20 ,
(3.95)
with 0 ≤ 𝜇 < 𝜈 ≤ 5 and 0 ≤ 𝛼 < 𝛽 ≤ 4.
2. Contract 𝑎 = 𝑏, 𝑐 = 𝑑:
0 = 4A ′′ + 16B ′′ .

(3.96)

We have A ′′ = 34 and B ′′ = − 13 , and hence:
(𝛾 𝛼5 ) 𝑏𝑎 (𝛾 𝛼5 ) 𝑑𝑐 =

4 𝑎 𝑐 1 𝑎 𝑐
𝛿 𝛿 − 𝛿 𝛿 .
3 𝑑 𝑏 3 𝑏 𝑑

(3.97)

The proof of Eq. (3.70) then unfolds as follows:
𝐽 𝛼5 𝐽 𝛼5 =

4
∑︁
𝛼=0

)
1 ( 𝛼5 ) (
𝜑
˜𝛾 𝜑 𝜑
˜ 𝛾 𝛼5 𝜑
4
)(
)
1(
𝜑
˜𝑎 (𝛾 𝛼5 ) 𝑏𝑎 𝜑 𝑏 𝜑
˜𝑐 (𝛾 𝛼5 ) 𝑑𝑐 𝜑 𝑑
=
4
)
)(
)(
1(
1 𝑎 𝑐
𝑏
𝑑
𝑎 𝑐
=
𝜑
˜𝑎 𝜑
𝜑
˜𝑐 𝜑
𝛿𝑑 𝛿𝑏 − 𝛿𝑏 𝛿𝑑
3
4

𝐽 𝛼5 𝐽 𝛼5 =

(following analogous steps to those in Eq. (3.85))
(
)
1
1
2
= × 3 (C1 ) + C1 = (𝜆2 − 1) .
(3.98)
3
4
□
Remark 3.6 It is worth noting that the dS (quadratic) Casimir C2𝔰𝔭(2,2) = −2(𝜆2 − 1)

(3.71), derived within a rigorous Clifford-algebraic framework, provides a clear explanation of the observation made by Barut and Böhm in 1970 [40] using a conventional group-theoretic analysis of the conformal group. Restricting the ladder-type
UPEIRs of the conformal algebra to the dS subalgebra, the Casimir invariant (3.71)
coincides exactly with the quadratic Casimir eigenvalues of the dS group associated with the so-called massless representations (see Eq. (1.20)). By adopting the
conformal Clifford algebra 𝔠𝔩(4, 2) as the primary algebraic framework, this formulation not only reproduces these results but also provides a geometrically enriched,
unified treatment of algebraic, spinorial, and conformal structures, facilitating the
construction and analysis of massless ladder representations and their restriction to
dS symmetry. This picture will be clarified further in the sequel.
□

## PDF page 98

84

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

We now revisit the “second-quantized” ladder generators of the 𝔰𝔲(2, 2) Lie
˜ 𝛾 𝜇𝜈 𝜑) (3.34), by providing an explicit and consistent
algebra, defined by 𝐽 𝜇𝜈 = 12 ( 𝜑
matrix realization of these generators. To this end, we employ Eq. (3.36), along with
the matrix representation of the 𝛾-matrices given in Proposition 3.1. Our analysis
begins with the elements of the (diagonal) Cartan subalgebra:
(
)( )
(
)
( ∗
) E1 E2∗ 0
𝔞
2 𝐽12 = 𝜑
˜ 𝛾12 𝜑 = 𝜑
˜ 𝛾15 𝛾25 𝜑 = 𝔞 −𝔟
0 E1∗ E2 𝔟∗
(
)
(
)
= 𝔞 ∗ E1 E2∗ 𝔞 − 𝔟 E1∗ E2 𝔟∗
)
(
= i 𝔞 1∗ 𝔞 1 − 𝔞 2∗ 𝔞 2 −𝔟1 𝔟∗1 + 𝔟2 𝔟∗2 = i(𝐻1 + 𝐻3 ) ,
⏟ ⏞⏞ ⏟ ⏟ ⏞⏞ ⏟
=: 𝐻1

=: 𝐻3

(3.99)
(
)( )
(
)
(
) E3 E4∗ 0
𝔞
2 𝐽34 = 𝜑
˜ 𝛾34 𝜑 = 𝜑
˜ 𝛾35 𝛾45 𝜑 = 𝔞 ∗ −𝔟
0 E3∗ E4 𝔟∗
(
)
(
)
= 𝔞 ∗ E3 E4∗ 𝔞 − 𝔟 E3∗ E4 𝔟∗
)
(
= i 𝔞 1∗ 𝔞 1 − 𝔞 2∗ 𝔞 2 + 𝔟1 𝔟∗1 − 𝔟2 𝔟∗2 = i(𝐻1 − 𝐻3 ) ,
⏟ ⏞⏞ ⏟ ⏟ ⏞⏞ ⏟
=: 𝐻1

=: −𝐻3

(3.100)
(
)( )
(
) −i𝜎0 0
𝔞
2 𝐽05 = 𝜑
˜ 𝛾05 𝜑 = 𝔞 ∗ −𝔟
0 i𝜎0 𝔟∗
(
)
= −i 𝔞 ∗ 𝔞 + 𝔟𝔟∗
(
)
= −i 𝔞 1∗ 𝔞 1 + 𝔞 2∗ 𝔞 2 + 𝔟1 𝔟∗1 +𝔟2 𝔟∗2 = −i(𝐻1 + 2𝐻2 + 𝐻3 ) , (3.101)
⏟ ⏞⏞ ⏟
=: 𝐻2

where we recall that:
( ∗)
( 1)
𝔟
𝔞
∗
𝔞 := 2 , 𝔟 := ∗1 ,
𝔟2
𝔞

and

(
)
𝔞 ∗ := 𝔞 1∗ 𝔞 2∗ ,

)
(
𝔟 := 𝔟1 𝔟2 .

(3.102)

Next, we turn our attention to the remaining elements of the algebra:
(
)( )
(
)
(
) 0 −iE1 𝔞
2 𝐽01 = 𝜑
˜ 𝛾01 𝜑 = 𝜑
˜ 𝛾05 𝛾15 𝜑 = 𝔞 ∗ −𝔟
iE1∗ 0
𝔟∗
( ∗
)
= −i 𝔟 E1 𝔞 + 𝔞 ∗ E1 𝔟∗
= −𝔟2 𝔞 1 − 𝔟1 𝔞 2 + 𝔞 2∗ 𝔟∗1 + 𝔞 1∗ 𝔟∗2 ,

(3.103)

## PDF page 99

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

(
)( )
(
)
(
) 0 −iE2 𝔞
2 𝐽02 = 𝜑
˜ 𝛾02 𝜑 = 𝜑
˜ 𝛾05 𝛾25 𝜑 = 𝔞 ∗ −𝔟
iE2∗ 0
𝔟∗
)
( ∗
= −i 𝔟 E2 𝔞 + 𝔞 ∗ E2 𝔟∗
(
)
= −i 𝔟2 𝔞 1 − 𝔟1 𝔞 2 − 𝔞 2∗ 𝔟∗1 + 𝔞 1∗ 𝔟∗2 ,

(

2 𝐽03 = 𝜑
˜ 𝛾03 𝜑 = 𝜑
˜ 𝛾05 𝛾35

(

2 𝐽04 = 𝜑
˜ 𝛾04 𝜑 = 𝜑
˜ 𝛾05 𝛾45

)

)

(3.104)

(
)( )
( ∗
) 0 −iE3 𝔞
𝔞
−𝔟
𝜑=
iE3∗ 0
𝔟∗
( ∗
)
= −i 𝔟 E3 𝔞 + 𝔞 ∗ E3 𝔟∗
= −𝔟1 𝔞 1 + 𝔟2 𝔞 2 + 𝔞 1∗ 𝔟∗1 − 𝔞 2∗ 𝔟∗2 ,

(3.105)

)( )
(
( ∗
) 0 −iE4 𝔞
𝜑 = 𝔞 −𝔟
iE4∗ 0
𝔟∗
( ∗
)
= −i 𝔟 E4 𝔞 + 𝔞 ∗ E4 𝔟∗
(
)
= −i 𝔟1 𝔞 1 + 𝔟2 𝔞 2 + 𝔞 1∗ 𝔟∗1 + 𝔞 2∗ 𝔟∗2 ,

(3.106)

(
)( )
(
)
(
) E1 E3∗ 0
𝔞
2 𝐽13 = 𝜑
˜ 𝛾13 𝜑 = 𝜑
˜ 𝛾15 𝛾35 𝜑 = 𝔞 ∗ −𝔟
0 E1∗ E3 𝔟∗
(
)
(
)
= 𝔞 ∗ E1 E3∗ 𝔞 − 𝔟 E1∗ E3 𝔟∗

(

2 𝐽14 = 𝜑
˜ 𝛾14 𝜑 = 𝜑
˜ 𝛾15 𝛾45

)

= 𝔞 2∗ 𝔞 1 − 𝔞 1∗ 𝔞 2 − 𝔟2 𝔟∗1 + 𝔟1 𝔟∗2 ,

(3.107)

(
)( )
( ∗
) E1 E4∗ 0
𝔞
𝜑 = 𝔞 −𝔟
0 E1∗ E4 𝔟∗
(
)
(
)
= 𝔞 ∗ E1 E4∗ 𝔞 − 𝔟 E1∗ E4 𝔟∗
(
)
= i 𝔞 2∗ 𝔞 1 + 𝔞 1∗ 𝔞 2 + 𝔟2 𝔟∗1 + 𝔟1 𝔟∗2 ,

(3.108)

(
)
2 𝐽15 = 𝜑
˜ 𝛾15 𝜑 = 𝔞 ∗ −𝔟

(

0 E1
E1∗ 0

)( )
𝔞
𝔟∗

= −𝔟 E1∗ 𝔞 + 𝔞 ∗ E1 𝔟∗
(
)
= i 𝔟2 𝔞 1 + 𝔟1 𝔞 2 + 𝔞 2∗ 𝔟∗1 + 𝔞 1∗ 𝔟∗2 ,
(
)( )
(
)
(
) E2 E3∗ 0
𝔞
2 𝐽23 = 𝜑
˜ 𝛾23 𝜑 = 𝜑
˜ 𝛾25 𝛾35 𝜑 = 𝔞 ∗ −𝔟
0 E2∗ E3 𝔟∗
)
(
)
(
= 𝔞 ∗ E2 E3∗ 𝔞 − 𝔟 E2∗ E3 𝔟∗
(
)
= i 𝔞 2∗ 𝔞 1 + 𝔞 1∗ 𝔞 2 − 𝔟2 𝔟∗1 − 𝔟1 𝔟∗2 ,

(3.109)

(3.110)

## PDF page 100

86

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

(
)( )
(
)
(
) E2 E4∗ 0
𝔞
2 𝐽24 = 𝜑
˜ 𝛾24 𝜑 = 𝜑
˜ 𝛾25 𝛾45 𝜑 = 𝔞 ∗ −𝔟
0 E2∗ E4 𝔟∗
(
)
(
)
= 𝔞 ∗ E2 E4∗ 𝔞 − 𝔟 E2∗ E4 𝔟∗
= −𝔞 2∗ 𝔞 1 + 𝔞 1∗ 𝔞 2 − 𝔟2 𝔟∗1 + 𝔟1 𝔟∗2 ,

(
)
2 𝐽25 = 𝜑
˜ 𝛾25 𝜑 = 𝔞 ∗ −𝔟

(

0 E2
E2∗ 0

(3.111)

)( )
𝔞
𝔟∗

= −𝔟 E2∗ 𝔞 + 𝔞 ∗ E2 𝔟∗
= −𝔟2 𝔞 1 + 𝔟1 𝔞 2 − 𝔞 2∗ 𝔟∗1 + 𝔞 1∗ 𝔟∗2 ,

(
)
2 𝐽35 = 𝜑
˜ 𝛾35 𝜑 = 𝔞 ∗ −𝔟

(

0 E3
E3∗ 0

)( )
𝔞
𝔟∗

= −𝔟 E3∗ 𝔞 + 𝔞 ∗ E3 𝔟∗
(
)
= i 𝔟1 𝔞 1 − 𝔟2 𝔞 2 + 𝔞 1∗ 𝔟∗1 − 𝔞 2∗ 𝔟∗2 ,

(
)
2 𝐽45 = 𝜑
˜ 𝛾45 𝜑 = 𝔞 ∗ −𝔟

(

(3.112)

0 E4
E4∗ 0

(3.113)

)( )
𝔞
𝔟∗

= −𝔟 E4∗ 𝔞 + 𝔞 ∗ E4 𝔟∗
= −𝔟1 𝔞 1 − 𝔟2 𝔞 2 + 𝔞 1∗ 𝔟∗1 + 𝔞 2∗ 𝔟∗2 .

(3.114)

The above results render the anti-Hermitian nature of 𝐽 𝜇𝜈 manifest:
𝐽 𝜇𝜈 = −(𝐽 𝜇𝜈 ) ∗ .

(3.115)

To define the unitary ladder representations of 𝔲(2, 2)  𝔰𝔲(2, 2) ⊕ 𝔲(1), we
introduce the standars Chevalley-Cartan basis of 𝔰𝔲(2, 2):
𝐸𝑎 = 𝜑
˜𝑎 𝜑 𝑎+1 ;

𝐸 1 = 𝔞 1∗ 𝔞 2 ,

𝐸 2 = 𝔞 2∗ 𝔟∗1 ,

𝐸 3 = −𝔟1 𝔟∗2 ,

(3.116)

𝐹𝑎 = 𝜑
˜𝑎+1 𝜑 𝑎 ;

𝐹1 = 𝔞 2∗ 𝔞 1 ,

𝐹2 = −𝔟1 𝔞 2 ,

𝐹3 = −𝔟2 𝔟∗1 ,

(3.117)

𝐻 𝑎 = [𝐸 𝑎 , 𝐹𝑎 ] = 𝜑
˜𝑎 𝜑 𝑎 − 𝜑
˜𝑎+1 𝜑 𝑎+1 ;
⏟
⏞⏞
⏟
by Eq. (3.38)

𝐻1 = 𝔞 1∗ 𝔞 1 − 𝔞 2∗ 𝔞 2 ,
𝐻2 = 𝔞 2∗ 𝔞 2 + 𝔟1 𝔟∗1 ,
𝐻3 = 𝔟2 𝔟∗2 − 𝔟1 𝔟∗1 ,

(3.118)

where 𝐸 𝑎 , 𝐹𝑎 , and 𝐻 𝑎 denote the raising, lowering (see Remark 3.9), and (diagonal)
Cartan operators of 𝔰𝔲(2, 2), respectively. We actually observe that:

## PDF page 101

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

[𝐻 𝑎 , 𝐻𝑏 ] = 0 ,

(3.119)

[𝐸 𝑎 , 𝐹𝑏 ] = 𝛿 𝑎𝑏 𝐻 𝑎 ,

(3.120)

[𝐻 𝑎 , 𝐸 𝑏 ] = +𝐴 𝑎𝑏 𝐸 𝑏 ;

[𝐻1 , 𝐸 1 ] = +2 𝐸 1 ,
[𝐻1 , 𝐸 2 ] = − 𝐸 2 ,
[𝐻1 , 𝐸 3 ] = 0 ,
[𝐻2 , 𝐸 1 ] = − 𝐸 1 ,
[𝐻2 , 𝐸 2 ] = +2 𝐸 2 ,
[𝐻2 , 𝐸 3 ] = − 𝐸 3 ,
[𝐻3 , 𝐸 1 ] = 0 ,
[𝐻3 , 𝐸 2 ] = − 𝐸 2 ,
[𝐻3 , 𝐸 3 ] = +2 𝐸 3 ,

[𝐻 𝑎 , 𝐹𝑏 ] = −𝐴 𝑎𝑏 𝐹𝑏 ;

(3.121)

[𝐻1 , 𝐹1 ] = −2 𝐹1 ,
[𝐻1 , 𝐹2 ] = + 𝐹2 ,
[𝐻1 , 𝐹3 ] = 0 ,
[𝐻2 , 𝐹1 ] = + 𝐹1 ,
[𝐻2 , 𝐹2 ] = −2 𝐹2 ,
[𝐻2 , 𝐹3 ] = + 𝐹3 ,
[𝐻3 , 𝐹1 ] = 0 ,
[𝐻3 , 𝐹2 ] = + 𝐹2 ,
[𝐻3 , 𝐹3 ] = −2 𝐹3 .

(3.122)

Note that 𝐴 𝑎𝑏 is called the Cartan matrix of the algebra:
+2 −1 0
©
ª
𝐴 𝑎𝑏 = ­−1 +2 −1® .
« 0 −1 +2¬

(3.123)

Remark 3.7 In the Chevalley-Cartan basis of 𝔰𝔲(2, 2) introduced above, it is manifest that the central 𝔲(1) generator C1 = 𝔞 ∗ 𝔞 − 𝔟 𝔟∗ (3.64) of the full 𝔲(2, 2) algebra
lies outside the 𝔰𝔲(2, 2) subalgebra, since it cannot be expressed as a linear combination of the Chevalley-Cartan generators of 𝔰𝔲(2, 2).
□
(
)
Remark 3.8 The maximal compact subalgebra 𝔰 𝔲(2) ⊕ 𝔲(2)  𝔰𝔲(2) ⊕ 𝔰𝔲(2) ⊕
𝔲(1) of 𝔰𝔲(2, 2) (see Appendix 2.7) can be explicitly realized by the following set
of generators:
1. 𝔰𝔲(2) 𝐿 subalgebra: This acts on the 𝔞-oscillators and is generated by (the
Schwinger realization [108]):

## PDF page 102

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

88



𝐽 ( 𝐿) := 𝐸 1 = 𝔞 1∗ 𝔞 2 ,

 +

𝐽−( 𝐿) := 𝐹1 = 𝔞 2∗ 𝔞 1 ,


 𝐽 ( 𝐿) := 1 𝐻1 = 1 (𝔞 ∗ 𝔞 1 − 𝔞 ∗ 𝔞 2 ) .
2
2
 3
1
2

(3.124)

These satisfy the standard 𝔰𝔲(2) commutation relations:
[ ( 𝐿) ( 𝐿) ]
𝐽3 , 𝐽±
= ±𝐽±(𝐿) ,

[ (𝐿) (𝐿) ]
𝐽+ , 𝐽−
= 2𝐽3(𝐿) .

(3.125)

The corresponding quadratic Casimir form is:
𝐽+(𝐿) 𝐽−(𝐿) + 𝐽−(𝐿) 𝐽+(𝐿)
2
)
(
)
1( ∗ 1
= 𝔞 1 𝔞 + 𝔞 2∗ 𝔞 2 𝔞 1∗ 𝔞 1 + 𝔞 2∗ 𝔞 2 + 2
4
=: j 𝐿 (j 𝐿 + 1) ,
2

C2𝔰𝔲 (2) 𝐿 = 𝐽3(𝐿) +

(3.126)

where we have defined the number operator 𝑁𝔞 = 𝔞 ∗ 𝔞 = 𝔞 1∗ 𝔞 1 + 𝔞 2∗ 𝔞 2 = 2j 𝐿 ,
with j 𝐿 ∈ 12 Z ≥0 .
2. 𝔰𝔲(2) 𝑅 subalgebra: This acts on the 𝔟-oscillators and is generated by:


𝐽 (𝑅) := 𝐸 3 = −𝔟1 𝔟∗2 ,

 +

𝐽−(𝑅) := 𝐹3 = −𝔟2 𝔟∗1 ,


 𝐽 (𝑅) := 1 𝐻3 = − 1 (𝔟1 𝔟∗ − 𝔟2 𝔟∗ ) .
2
2
 3
1
2

(3.127)

These also satisfy the canonical 𝔰𝔲(2) commutation relations:
[ (𝑅) (𝑅) ]
𝐽3 , 𝐽±
= ±𝐽±(𝑅) ,

[ (𝑅) (𝑅) ]
𝐽+ , 𝐽−
= 2𝐽3(𝑅) .

(3.128)

The corresponding quadratic Casimir form is:
)(
)
1( ∗ 1
𝔟1 𝔟 + 𝔟∗2 𝔟2 𝔟∗1 𝔟1 + 𝔟∗2 𝔟2 + 2
4
=: j𝑅 (j𝑅 + 1) ,

C2𝔰𝔲 (2) 𝑅 =

(3.129)

where we have defined the number operator 𝑁𝔟 = 𝔟∗ 𝔟 = 𝔟∗1 𝔟1 + 𝔟∗2 𝔟2 = 2j𝑅 , with
j𝑅 ∈ 12 Z ≥0 .
3. 𝔲(1) center: The 𝔲(1) center of the maximal compact subalgebra is generated by
the conformal Hamiltonian 𝐻 (3.63):
𝐻 :=

)
) 1(
1(
𝐻1 + 2𝐻2 + 𝐻3 = 𝔞 1∗ 𝔞 1 + 𝔞 2∗ 𝔞 2 + 𝔟1 𝔟∗1 + 𝔟2 𝔟∗2 .
2
2

(3.130)

This central element commutes with all the 𝔰𝔲(2) 𝐿 and 𝔰𝔲(2) 𝑅 generators:
[

] [
] [
] [
]
𝐻, 𝐽±( 𝐿) = 𝐻, 𝐽3(𝐿) = 𝐻, 𝐽±(𝑅) = 𝐻, 𝐽3(𝑅) = 0 .

(3.131)

## PDF page 103

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

□
Remark 3.9 Before proceeding, let us clarify in what sense the operators 𝐸 𝑎 and 𝐹𝑎
are called raising and lowering operators for representations of 𝔰𝔲(2, 2). Let |W⟩ be
a weight vector defined by:
𝐻 𝑎 |W⟩ = W𝑎 |W⟩ ,

(3.132)

with weight components W = (W1 , W2 , W3 ) corresponding to the Cartan generators 𝐻1 , 𝐻2 , and 𝐻3 ; since the Cartan elements commute, they are simultaneously
diagonalizable, and thus admit a common eigenbasis. Consider the action of 𝐹𝑏 on
|W⟩. Using the commutation relation [𝐻 𝑎 , 𝐹𝑏 ] = −𝐴 𝑎𝑏 𝐹𝑏 , we find:
(
) (
)
𝐻 𝑎 𝐹𝑏 |W⟩ = [𝐻 𝑎 , 𝐹𝑏 ] + 𝐹𝑏 𝐻 𝑎 |W⟩
(3.133)
(
)
= − 𝐴 𝑎𝑏 𝐹𝑏 + W𝑎 𝐹𝑏 |W⟩
(3.134)
(
)
= W𝑎 − 𝐴 𝑎𝑏 𝐹𝑏 |W⟩ .
(3.135)
This shows that 𝐹𝑏 |W⟩ is again a weight vector, whose weight component is shifted
as:
W𝑎

↦−→

W𝑎 − 𝐴 𝑎𝑏 .

(3.136)

Equivalently, the total weight vector transforms as:
𝐹𝑏 |W⟩

⟩
W − 𝛼𝑏 ,

↦−→

(3.137)

where the simple root 𝛼𝑏 is given by the 𝑏-th column of the Cartan matrix 𝐴 𝑎𝑏 ;
explicitly, 𝛼1 = (2, −1, 0) ⊤ , 𝛼2 = (−1, 2, −1) ⊤ , and 𝛼3 = (0, −1, 2) ⊤ .
Similarly, the operator 𝐸 𝑏 acts as a raising operator, shifting the weight vector
upward by the corresponding simple root:
⟩
𝐸 𝑏 |W⟩ ∝ W + 𝛼𝑏 ,
(3.138)
□

where 𝛼𝑏 is the simple root associated with 𝐸 𝑏 .

Given the above, we define the lowest weight state |LW𝜆 ⟩ of the UPEIR of 𝔰𝔲(2, 2)
(with a given helicity 𝜆) as:
(
)
|LW𝜆 ⟩ =: |LW𝜆≥0 ⟩ = (𝔞 2∗ ) 2𝜆 |0SO(4) ⟩ , for 𝜆 ≥ 0 ,
(
)
|LW𝜆 ⟩ =: |LW𝜆<0 ⟩ = (𝔟∗1 ) −2𝜆 |0SO(4) ⟩ , for 𝜆 < 0 .
(3.139)
This state is annihilated by all lowering operators 𝐹𝑎 (see Eqs. (3.61) and (3.62)):
𝐹𝑎 |LW𝜆 ⟩ = 0 ,

for

𝑎 = 1, 2, 3 .

(3.140)

## PDF page 104

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

90

Moreover, |LW𝜆 ⟩ is an eigenstate of the conformal Hamiltonian 𝐻 (3.130) (see also
(3.63)) with eigenvalue:
E◦ := 1 + |𝜆| ,

with 𝜆 ∈

1
Z,
2

(3.141)

so that:
(𝐻 − E◦ )|LW𝜆 ⟩ = 0 .

(3.142)

This eigenvalue — the “lowest conformal energy” (or conformal dimension) —
serves to label the lowest weight state |LW𝜆 ⟩ of the representation.14
Remark 3.10 One verifies that the lowest weight state (3.139) transforms in the
spin-𝑠 = 𝜆 representation of 𝔰𝔲(2) 𝐿 and is a singlet under 𝔰𝔲(2) 𝑅 for positive
helicity 𝜆 ≥ 0, whereas for negative helicity 𝜆 < 0 it transforms in the spin-𝑠 = |𝜆|
representation of 𝔰𝔲(2) 𝑅 and is a singlet under 𝔰𝔲(2) 𝐿 ; specifically:
C2𝔰𝔲 (2) 𝐿 |LW𝜆≥0 ⟩ = 𝑠(𝑠 + 1)|LW𝜆≥0 ⟩ ,

and

C2𝔰𝔲 (2) 𝑅 |LW𝜆≥0 ⟩ = 0 ,
𝐽+(𝑅) |LW𝜆≥0 ⟩ = 0 ,
𝐽−(𝑅) |LW𝜆≥0 ⟩ = 0 ,
𝐽3(𝑅) |LW𝜆≥0 ⟩ = 0 ,

(3.143)

while:
C2𝔰𝔲 (2) 𝐿 |LW𝜆<0 ⟩ = 0 ,

and

C2𝔰𝔲 (2) 𝑅 |LW𝜆<0 ⟩ = 𝑠(𝑠 + 1)|LW𝜆<0 ⟩ ,

𝐽+( 𝐿) |LW𝜆≥0 ⟩ = 0 ,
𝐽−( 𝐿) |LW𝜆≥0 ⟩ = 0 ,
𝐽3( 𝐿) |LW𝜆≥0 ⟩ = 0 .

(3.144)
□

The entire one-particle Hilbert space H𝜆(1) carrying the UPEIR of 𝔰𝔲(2, 2) is then
generated by the successive action of the raising operators 𝐸 𝑎 on this lowest weight
state |LW𝜆 ⟩, uniquely characterized (up to the helicity sign) by the lowest conformal
energy E◦ . This iterative construction naturally endows H𝜆(1) with a hierarchical
structure, since the action of the raising operators 𝐸 𝑎 increases the eigenvalue of the
conformal Hamiltonian 𝐻 in discrete steps (see Remark 3.9). Consequently, H𝜆(1)
(
)
is foliated into the finite-dimensional15 eigenspaces HE(1) := ker(𝐻 − E ) ⊂ H𝜆(1)
of the conformal Hamiltonian 𝐻, each satisfying:
14 In the special case of a free massless scalar field (helicity 𝜆 = 0), the lowest weight state is

simply denoted by |LW𝜆=0 ⟩ =: |0SO(4) ⟩, and the corresponding eigenvalue equation (3.142) reduces
to (3.41), indicating that the lowest conformal energy (or dimension) is E◦ = 1.
15 See Eq. (3.150).

## PDF page 105

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

(𝐻 − E )|𝑊⟩ = 0 ,

for all

|𝑊⟩ ∈ HE(1) ,

where the spectrum of 𝐻 in this representation is given by:
{
}
E = |𝜆| + 𝑛 ; 𝑛 = 1, 2, 3, . . . ,

(3.145)

(3.146)

with E◦ = 1 + |𝜆| as the lowest value. This construction furnishes a transparent
realization of the UPEIR in terms of conformal energy levels and, importantly,
shows that every UPEIR of 𝔰𝔲(2, 2) — in particular the one-particle Hilbert space
H𝜆(1) of a free massless conformal field of definite helicity 𝜆 ∈ 12 Z — is completely
characterized by the lowest eigenvalue E◦ of the conformal Hamiltonian (up to the
sign of the helicity parameter 𝜆), just as its lowest weight state |LW𝜆 ⟩ is. This point
is discussed further in Remark 3.12.
(
)
Remark 3.11 It is important to emphasize that each eigenspace HE(1) ⊂ H𝜆(1)
is not invariant under the full conformal Lie algebra 𝔰𝔲(2, 2); rather, it is invariant
under the subalgebra 𝔰𝔬(4). This is because the conformal
Hamiltonian
𝐻 generates
(
)
the 𝔲(1) center of the maximal compact subalgebra 𝔰 𝔲(2) ⊕ 𝔲(2)  𝔰𝔬(4) ⊕ 𝔲(1),
and therefore commutes with the 𝔰𝔬(4) generators but not with the entire algebra
𝔰𝔲(2, 2). Consequently, the action of 𝔰𝔬(4) preserves each eigenspace HE(1) of
𝐻; strictly speaking, each HE(1) carries a (generally reducible) finite-dimensional
representation of 𝔰𝔬(4). Proposition 3.4, and in particular the third step of its proof,
provides a more detailed analysis of this structure.
□
Accordingly, a discrete, compact basis can be constructed for the Hilbert space
H𝜆(1) of massless one-particle states with helicity 𝜆, consisting of simultaneous
eigenstates of the conformal Hamiltonian 𝐻 (3.130) and of the Casimir operator
C2𝔰𝔬 (4) associated with the 𝔰𝔬(4) Lie subalgebra. The physical, positive-definite
Casimir invariant of 𝔰𝔬(4) (⊂ 𝔰𝔬(4, 1) ⊂ 𝔰𝔬(4, 2)) is found to be:
C2𝔰𝔬 (4) = C2𝔰𝔲 (2) 𝐿 + C2𝔰𝔲 (2) 𝑅
1
1
= 𝔞 ∗ 𝔞(𝔞 ∗ 𝔞 + 2) + 𝔟∗ 𝔟(𝔟∗ 𝔟 + 2)
4
4
)
1( ∗
∗ 2
=
(𝔞 𝔞 + 𝔟𝔟 ) + (𝔞 ∗ 𝔞 − 𝔟𝔟∗ ) (𝔞 ∗ 𝔞 − 𝔟𝔟∗ + 4)
8 ⏟ ⏞⏞ ⏟ ⏟
⏞⏞
⏟
= 4𝐻 2

)
1(
= E 2 + 𝜆2 − 1 ,
2

= C1 ( C1 +4)

(3.147)

hence:
) 1(
)
= j 𝐿 (j 𝐿 + 1) + j𝑅 (j𝑅 + 1) = E 2 + 𝜆2 − 1 ≥ |𝜆| (|𝜆| + 1) . (3.148)
2
(
)
From the above relation, it follows that j 𝐿 , j𝑅 ∈ 21 Z ≥0 satisfy the bound (see
Appendix 3.6):
C2𝔰𝔬 (4)

(

## PDF page 106

92

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

j𝐿 , j𝑅 ≤ E − 1 .

(3.149)

Note that the dimension of the eigenspace HE(1) ⊂ H𝜆(1) of 𝐻, which carries a
representation of 𝔰𝔬(4) and corresponds to the eigenvalue E , is given by:
(
)
d HE(1) = (2j 𝐿 + 1) (2j𝑅 + 1) .

(3.150)

Remark 3.12 Taking all of the above into account, the states within each 𝔰𝔲(2, 2)
UPEIR space H𝜆(1) are labeled by three (half-)integers: E , which labels the 𝔰𝔬(4)invariant eigenspaces HE(1) of the conformal Hamiltonian 𝐻 that foliate the full
Hilbert space H𝜆(1) ; and j 𝐿 and j𝑅 , which label the states within each such
eigenspace HE(1) , corresponding to a finite-dimensional (generally reducible) representation of 𝔰𝔬(4):
{
H𝜆(1) = Span |E , j 𝐿 , j𝑅 ⟩ ; E = |𝜆| + 1, |𝜆| + 2, . . . ,
}
(3.151)
j 𝐿 , j𝑅 ∈ 21 Z ≥0 ≤ E − 1 .
In this context, by construction, the 𝔰𝔲(2, 2) UPEIR space is fully generated by
repeated action of the raising operators 𝐸 𝑎 on the lowest weight state:
|LW𝜆 ⟩ = |E◦ , j 𝐿 , j𝑅 ⟩ ,

(3.152)

which has lowest conformal energy E◦ = 1 + |𝜆|, and is accordingly denoted by:
H𝜆(1) =: CE>◦ ,j𝐿 ,j𝑅 .

(3.153)

Note that the superscript ‘> ’ indicates that the representations CE>◦ ,j ,j are charac𝐿 𝑅
terized by the positivity of the conformal energy, meaning that the spectrum of 𝐻 is
bounded from below (see Eq. (3.41)).
Although this point has already been noted, it is appropriate to scrutinize, within
the above labelling, that the lowest weight state |E◦ , j 𝐿 , j𝑅 ⟩, which furnishes the
full Hilbert space H𝜆(1) , is itself uniquely specified by its conformal energy E◦ , up
to the sign of the helicity parameter 𝜆. In particular, for a given E◦ (and hence a
fixed |𝜆|), there exist two distinct configurations of (j 𝐿 , j𝑅 ), each corresponding to
one of the two possible helicity signs, which give rise to two inequivalent realizations of the corresponding UPEIR, distinguished as positive- and negative-helicity
representations.
To render this dependence explicit, we impose relation (3.148) on the lowest
weight state |E◦ , j 𝐿 , j𝑅 ⟩, yielding:
j 𝐿 (j 𝐿 + 1) + j𝑅 (j𝑅 + 1) = |𝜆|(|𝜆| + 1) .

(3.154)

For a given E◦ (and hence a fixed |𝜆|), this equation — consistent with Remark 3.10
— admits only two possible choices for the lowest weight state |E◦ , j 𝐿 , j𝑅 ⟩:

## PDF page 107

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

⟩
|E◦ , j 𝐿 , j𝑅 ⟩ = |E◦ , E◦ − 1, 0⟩ = |𝜆| + 1, |𝜆|, 0 ,

(3.155)

⟩
|E◦ , j 𝐿 , j𝑅 ⟩ = |E◦ , 0, E◦ − 1⟩ = |𝜆| + 1, 0, |𝜆| ,

(3.156)

where:
1. The first choice (3.155) specifies the positive helicity UPEIR of 𝔰𝔲(2, 2) and is
denoted by:
>
>
C |𝜆|+1,
|𝜆|,0 =: C𝑠+1,𝑠,0 ,

with

|𝜆| =: 𝑠 .

(3.157)

The positivity of the helicity follows from the fact that the lowest weight state
|𝑠 +1, 𝑠, 0⟩ in this representation transforms in the spin-𝑠 representation of 𝔰𝔲(2) 𝐿
and is a singlet under 𝔰𝔲(2) 𝑅 (see Remark 3.10).
2. The second choice (3.155), however, specifies the 𝔰𝔲(2, 2) UPEIR with negative
helicity, in which the lowest weight state is annihilated by the same lowering operators, but with the roles of SU(2) 𝐿 and SU(2) 𝑅 exchanged. This representation
is usually denoted as:
>
>
C |𝜆|+1,0,
|𝜆| =: C𝑠+1,0,𝑠 ,

with

|𝜆| =: 𝑠 .

(3.158)

The negative helicity arises from the fact that the lowest weight state |𝑠 + 1, 0, 𝑠⟩
in this representation transforms in the spin-𝑠 representation of 𝔰𝔲(2) 𝑅 and is a
singlet under 𝔰𝔲(2) 𝐿 (see, again, Remark 3.10).
Thus, for each fixed lowest conformal energy E◦ , and hence for fixed |𝜆| = 𝑠, there
>
is a unique positive-helicity 𝔰𝔲(2, 2) UPEIR C𝑠+1,0,𝑠
and a corresponding negative>
helicity UPEIR C𝑠+1,𝑠,0 , related by exchanging the 𝔰𝔲(2) 𝐿 and 𝔰𝔲(2) 𝑅 roles in the
lowest weight state.
With this labelling, in the zero-helicity (𝜆 = 0) case, the lowest weight state
|LW𝜆=0 ⟩ =: |0SO(4) ⟩ is identified with |1, 0, 0⟩. It is perhaps worthwhile noting that
(1)
the zero-helicity space H𝜆=0
— corresponding to the representation at the very
bottom of the ladder representations, with j 𝐿 = j𝑅 = 0 and 𝜆 = 0 — coincides with
the state space of the non-relativistic, regularized hydrogen atom. This connection
was first uncovered in the 1960s through the study of spectrum-generating algebras.
Note: For a detailed account of how the conformal massless (ladder) UPEIR
restricts to the dS case, see Appendix 3.7.
□
Remark 3.13 From the construction above, one immediately observes a key identity
that will prove useful in the sequel. Specifically, for any helicity parameter 𝜆 in the
lowest weight state, one has:
(
)
E◦ − j 𝐿 + j 𝑅 = 1 .
(3.159)
This relation naturally extends to all descendant states as:
(
)
E − j 𝐿 + j𝑅 ∈ Z>0 .

(3.160)

## PDF page 108

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

94

Indeed, all descendant states are obtained by repeated action of the raising operators
𝐸 𝑎 on the lowest weight state, which increases the eigenvalue of the conformal
Hamiltonian 𝐻 in discrete steps. Moreover, such actions leave the integer or halfinteger nature of j 𝐿 + j𝑅 invariant. This latter observation can be viewed as a
by-product of the discussion in Appendix 3.7, in particular Eq. (3.292).
□
Remark 3.14 In this setting, the corresponding ladder representations of the extended conformal algebra 𝔲(2, 2) = 𝔰𝔲(2, 2) ⊕ 𝔲(1) are constructed as direct sums
of the UPEIRs H𝜆(1) =: CE>◦ ,j ,j of 𝔰𝔲(2, 2), each specified by a fixed helicity
𝐿 𝑅
𝜆 ∈ 21 Z:
⨁
H𝜆(1) .
(3.161)
H (1) =
1
𝜆∈ 2 Z

The additional 𝔲(1) generator endows H (1) with a natural 𝔲(1)-grading by helicity
and coherently couples the graded sectors into a single IR of 𝔲(2, 2). States in the
𝔲(2, 2) 1-particle space H (1) are therefore labelled by the helicity 𝜆 together with
the usual energy and spin quantum numbers:
{
H (1) = Span |𝜆, E , j 𝐿 , j𝑅 ⟩ ; 𝜆 ∈ 12 Z ,
E = |𝜆| + 1, |𝜆| + 2, . . . ,
}
j 𝐿 , j𝑅 ∈ 12 Z ≥0 ≤ E − 1 .

(3.162)
□

The momentum generator 𝑝 𝜇¤ ( 𝜇¤ = 0, 1, 2, 3) of the Poincaré subalgebra of 𝔲(2, 2)
is verified to have zero square, thus corresponding to massless particles:
𝑝 𝜇¤ :=

(
)
1
𝜑
˜ 𝛾 1 + 𝛾4 𝜑
2 𝜇¤

=⇒

𝑝 𝜇¤ 𝑝 𝜇¤ = (⃗𝑝 ) 2 − ( 𝑝 0 ) 2 = 0 ,

(3.163)

where ⃗𝑝 := ( 𝑝 1 , 𝑝 2 , 𝑝 3 ) and (⃗𝑝 ) 2 := ( 𝑝 1 ) 2 + ( 𝑝 2 ) 2 + ( 𝑝 3 ) 2 . This is proven in Ref.
[13], using a realization of 𝛾 matrices with 𝛾4 — rather than B — diagonal. Here,
we instead adopt a complex-variable formulation of 4-dimensional conformal space,
providing a unified treatment of both dS and Minkowski cases.
Proposition 3.3 Let us introduce the complex translation operators 𝑇𝑖 and the special conformal generators 𝐶𝑖 , both naturally suited to the ladder formalism and
characterized by a vanishing four-square:
𝑇𝑖 = 𝜑
˜ P+ 𝛾 𝑖 P − 𝜑 = 𝔞 ∗ E 𝑖 𝔟 ∗ ,
𝐶𝑖

(

)
= 𝑇𝑖∗ = 𝔟 E𝑖∗ 𝔞 ,

(3.164)
(3.165)

where 𝑖 = 1, 2, 3, 4 and the operators E𝑖 are defined in Eq. (3.49). They satisfy:

## PDF page 109

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

(
𝑖

𝑇 𝑇𝑖

=

4
∑︁

)
𝑖

𝑇 𝑇𝑖 = 0 = 𝐶 𝑖 𝐶𝑖 .

(3.166)

𝑖=1

Note that this proposition will be complemented by Proposition 3.4, which specifically justifies the naming of the complex translation operators 𝑇𝑖 and the special
conformal generators 𝐶𝑖 .
Proof — Step I (the role of 𝜖 = i𝜎2 as a spinor metric). In 2-component spinor
formalism, the antisymmetric tensor 𝜖 𝐴𝐵 (𝜖 𝐴𝐵 = −𝜖 𝐵𝐴, with 𝐴, 𝐵 = 1, 2) — given
explicitly by:
(
)
(
)
0 1
0 −1
𝐴𝐵
∗
∗
𝜖 𝐴𝐵 = i𝜎2 =
, 𝜖
= (𝜖 𝐴𝐵 ) = (i𝜎2 ) =
, 𝜖 𝐴𝐶 𝜖𝐶 𝐵 = 𝛿 𝐵𝐴 ,
−1 0
1 0
(3.167)
— plays the distinguished role of a spinor metric, enabling one to raise and lower
spinor indices:
𝜓 𝐴 = 𝜖 𝐴𝐵 𝜓 𝐵 ,
Thus, if 𝜓 𝐴 =

𝜓 𝐴 = 𝜖 𝐴𝐵 𝜓 𝐵 .

(3.168)

) ( 1) ( 2 )
𝜓
𝜓
=
.
𝜓2
−𝜓 1

(3.169)

( 1)
𝜓
, then:
𝜓2
(

0 1
𝜓 𝐴 = 𝜖 𝐴𝐵 𝜓 =
−1 0
𝐵

This structure is essential both algebraically and geometrically, for the following
reasons:
1. Antisymmetry and fermionic bilinears: The antisymmetry of 𝜖 𝐴𝐵 guarantees that
spinor contractions like 𝜓 𝐴 𝜒 𝐴 = 𝜓 𝐴 𝜖 𝐴𝐵 𝜒 𝐵 are antisymmetric under exchange
𝜓 𝐴 𝜒 𝐴 = −𝜒 𝐴𝜓 𝐴. This antisymmetry is a necessary condition when dealing with
Grassmann-valued spinor fields (as in quantum field theory (QFT)), ensuring that
bilinear quantities obey the correct statistics for fermions.
2. Invariant tensor under SL(2, C): The matrix 𝜖 𝐴𝐵 is, up to a nonzero scalar
multiple, the unique nondegenerate, antisymmetric rank-2 tensor invariant under
the action of SL(2, C) — the double cover of the proper, orthochronous Lorentz
group. It satisfies the identity:
(𝑆𝜖 𝑆 ⊺ ) 𝐴𝐵 = 𝜖 𝐴𝐵 ,

for all

𝑆 ∈ SL(2, C) ,

(3.170)

thereby ensuring that spinor index raising and lowering, as well as Lorentzinvariant contractions, are preserved under transformations of the spinor representation.

## PDF page 110

96

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

( )
01
3. Why 𝜎1 and 𝜎3 fail: The other Pauli matrices, namely 𝜎1 =
and
10
(
)
1 0
𝜎3 =
are symmetric and do not yield antisymmetric spinor bilinears.
0 −1
For instance:
𝜓 𝐴 (𝜎1 ) 𝐴𝐵 𝜒 𝐵 = 𝜒 𝐴 (𝜎1 ) 𝐴𝐵 𝜓 𝐵 ,

(3.171)

which is symmetric, violating the required antisymmetry for fermionic contractions. Moreover, these matrices are not invariant under SL(2, C) transformations
and hence do not define Lorentz-invariant inner products on spinor space.
— Step II ((E𝑖 ) 𝐵𝐴 and (E𝑖 ) 𝐴𝐵 ). Recall that the Pauli matrices and 𝜎0 read as:
( )
(
)
(
)
( )
01
0 −i
1 0
10
(𝜎1 ) 𝐵𝐴 =
, (𝜎2 ) 𝐵𝐴 =
, (𝜎3 ) 𝐵𝐴 =
, (𝜎0 ) 𝐵𝐴 =
.
10
i 0
0 −1
01
(3.172)
Then, the associated mixed-index tensors (“conjugate” quaternions) (E𝑖 ) 𝐵𝐴 are:
{
(E𝑖 ) 𝐵𝐴 :=

i(𝜎𝑖 ) 𝐵𝐴 ,

for 𝑖 = 1, 2, 3 ,

(𝜎0 ) 𝐵𝐴 ,

for 𝑖 = 4 .

(3.173)

Given the above, the bispinor tensors (E𝑖 ) 𝐴𝐵 are defined by:
(E𝑖 ) 𝐴𝐵 = 𝜖 𝐴𝐶 (E𝑖 )𝐶𝐵 .

(3.174)

— Step III (four essential expansions). As a by-product of the proof of Proposition 3.2, we put forward the following essential identity:
𝐶
𝐴 𝐶
(E𝑖 ) 𝐵𝐴 (E 𝑖∗ ) 𝐷
= A 𝛿 𝐵𝐴 𝛿𝐶
𝐷 + B 𝛿𝐷 𝛿 𝐵 ,

(3.175)

where, again, A and B are constants to be determined. We take two traces of the
above expansion:
1. Contract 𝐴 = 𝐷, 𝐵 = 𝐶:
8 = 2A + 4B .

(3.176)

4 = 4A + 2B .

(3.177)

2. Contract 𝐴 = 𝐵, 𝐶 = 𝐷:

We obtain A = 0 and B = 2, and therefore the first expansion takes the form:
𝐶
𝐴 𝐶
(E𝑖 ) 𝐵𝐴 (E 𝑖∗ ) 𝐷
= 2 𝛿𝐷
𝛿𝐵 .

(3.178)

Using the spinor metric 𝜖, we immediately deduce the second essential expansion:

## PDF page 111

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

(
)(
)
¤
𝐶¤
(E𝑖 ) 𝐴𝐵 (E 𝑖∗ )𝐶𝐷 = 𝜖 𝐴𝐵 (E𝑖 ) 𝐵𝐵¤ 𝜖𝐶 𝐶¤ (E 𝑖∗ ) 𝐷
(
)(
)
¤
𝐵 𝐶¤
= 𝜖 𝐴𝐵 𝜖𝐶 𝐶¤ 2 𝛿 𝐷
𝛿 𝐵¤
(
)(
)
¤
𝐵
= 𝜖 𝐴𝐵 𝜖𝐶 𝐵¤ 2 𝛿 𝐷
( )(
)
𝐵
𝐵
.
= 𝛿𝐶𝐴 2 𝛿 𝐷
= 2 𝛿𝐶𝐴 𝛿 𝐷

(3.179)

The third expansion can be viewed as:
′ 𝐴 𝐶
𝐶
= A ′ 𝛿 𝐵𝐴 𝛿𝐶
(E𝑖 ) 𝐵𝐴 (E 𝑖 ) 𝐷
𝐷 + B 𝛿𝐷 𝛿 𝐵 ,

(3.180)

where, again, A ′ and B ′ are constants to be determined. We consider two traces of
the above expansion:
1. Contract 𝐴 = 𝐷, 𝐵 = 𝐶:
−4 = 2A ′ + 4B ′ .

(3.181)

4 = 4A ′ + 2B ′ .

(3.182)

2. Contract 𝐴 = 𝐵, 𝐶 = 𝐷:

We find A ′ = −B ′ = 2, and hence we have:
𝐴 𝐶
𝐶
(E𝑖 ) 𝐵𝐴 (E 𝑖 ) 𝐷
= 2 𝛿 𝐵𝐴 𝛿𝐶
𝐷 − 2 𝛿𝐷 𝛿 𝐵 .

(3.183)

Again employing the spinor metric 𝜖, we find the fourth expansion:
(
)(
)
¤
¤
𝐷
(E𝑖 ) 𝐴𝐵 (E 𝑖 ) 𝐶𝐷 = 𝜖 𝐴𝐵 (E𝑖 ) 𝐵𝐵¤ 𝜖 𝐶 𝐶 (E 𝑖 )𝐶
¤
(
)(
)
¤
¤
𝐵 𝐷
𝐵 𝐷
= 𝜖 𝐴𝐵 𝜖 𝐶 𝐶 2 𝛿 𝐵
𝛿
−
2
𝛿
𝛿
¤ 𝐶¤
𝐶¤ 𝐵¤
= 2 𝜖 𝐴𝐵 𝜖 𝐶𝐷 − 2 𝜖 𝐴𝐷 𝜖 𝐶 𝐵
= 2 𝜖 𝐴𝐶 𝜖 𝐵𝐷 .

(3.184)

The latter equality, namely 𝜖 𝐴𝐵 𝜖 𝐶𝐷 − 𝜖 𝐴𝐷 𝜖 𝐶 𝐵 = 𝜖 𝐴𝐶 𝜖 𝐵𝐷 , may require some
clarification. Let us compute both sides for specific (nontrivial) values:
1. 𝐴 = 2, 𝐵 = 1, 𝐶 = 1, 𝐷 = 2:
𝜖 21 𝜖 12 − 𝜖 22 𝜖 11 = 𝜖 21 𝜖 12 ,
⏟ ⏞⏞ ⏟

checked!

(3.185)

checked!

(3.186)

=0

2. 𝐴 = 2, 𝐵 = 2, 𝐶 = 1, 𝐷 = 1:
𝜖 22 𝜖 11 − 𝜖 21 𝜖 12 = 𝜖 21 𝜖 21 ,
⏟ ⏞⏞ ⏟
=0

## PDF page 112

98

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

— Step IV (proof of Eq. (3.166)). Taking into account all preceding results —
particularly Eq. (3.184) — we conclude that:
(
)
𝑇 𝑖 𝑇𝑖 = 𝔞 ∗ E 𝑖 𝔟∗ (𝔞 ∗ E𝑖 𝔟∗ )
(
)(
)
∗
= 𝔞 ∗𝐴 (E 𝑖 ) 𝐴𝐵 𝔟∗𝐵 𝔞𝐶
(E𝑖 ) 𝐶𝐷 𝔟∗𝐷
(
) ( ∗ ∗ ) ( 𝐴𝐶 𝐵𝐷 )
= 𝔞 ∗𝐴 𝔟∗𝐵 𝔞𝐶
𝔟𝐷 2 𝜖 𝜖
(
)(
)
∗
= 2 𝔞 ∗𝐴 𝜖 𝐴𝐶 𝔞𝐶
𝔟∗𝐵 𝜖 𝐵𝐷 𝔟∗𝐷
(
)
= 2 𝔞 1∗ 𝜖 11 𝔞 1∗ + 𝔞 1∗ 𝜖 12 𝔞 2∗ + 𝔞 2∗ 𝜖 21 𝔞 1∗ + 𝔞 2∗ 𝜖 22 𝔞 2∗ (. . . ) = 0 .
(3.187)
⏟
⏞⏞
⏟ ⏟⏞⏞⏟
=0

=0

□
Proposition 3.4 Let 𝐽 𝜇𝜈 = 12 ( 𝜑
˜ 𝛾 𝜇𝜈 𝜑) denote the “second-quantized” generators
of the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2), as defined in Eqs. (3.99)-(3.114). By taking suitable linear combinations of these generators, we construct an alternative
(Schwinger [108]) realization of the Lie algebra that is naturally adapted to the
so-called conformal compact basis:16
complex translations ; 𝑇𝑖 := + (𝐽𝑖5 + i𝐽0𝑖 ) = 𝔞 ∗ E𝑖 𝔟∗ ,
special conformal transformations ; 𝐶𝑖 := − (𝐽𝑖5 − i𝐽0𝑖 ) = 𝔟 E𝑖∗ 𝔞 ,
1
conformal Hamiltonian ; 𝐻 := i𝐽05 = (𝔞 ∗ 𝔞 + 𝔟 𝔟∗ ) ,
2
angular momentum-like operators ; 𝐽𝑖 𝑗 , 𝑖, 𝑗 = 1, 2, 3, 4 .

(3.188)
(3.189)
(3.190)
(3.191)

These operators generate a closed realization of the Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2),
satisfying the canonical commutation relations:
[
]
𝐻, 𝐽𝑖 𝑗 = 0 ,
(3.192)
(
)
4
[
]
]
1 ∑︁ [
𝐶𝑖 , 𝑇 𝑗 = 2𝐻 𝛿𝑖 𝑗 − 2𝐽𝑖 𝑗 ,
=⇒ 𝐻 =
𝐶𝑖 , 𝑇𝑖 ,
(3.193)
8 𝑖=1
(
)
[
]
(
)
(
)
𝐻, 𝑇𝑖 = 𝑇𝑖 ,
=⇒ 𝐻 𝑇𝑖 |W⟩ = 𝑇𝑖 𝐻|W⟩ + 𝑇𝑖 |W⟩ ,
(3.194)
(
)
[
]
(
)
(
)
𝐻, 𝐶𝑖 = − 𝐶𝑖 ,
=⇒ 𝐻 𝐶𝑖 |W⟩ = 𝐶𝑖 𝐻|W⟩ − 𝐶𝑖 |W⟩ .
(3.195)

16 It is straightforward to verify the relation:

𝐶𝑖

(

)
(
)
= − ( 𝐽𝑖5 − i𝐽0𝑖 ) = 𝑇𝑖∗ = ( 𝐽𝑖5 + i𝐽0𝑖 ) ∗ ,

which follows directly from the anti-Hermitian property (3.115) of the generators 𝐽𝜇𝜈 . This identity
reflects the underlying symmetry (3.165) between the operators 𝐶𝑖 and 𝑇𝑖 , and will play a key role
in the structure of the corresponding Lie algebra representations.

## PDF page 113

(
)
3.3 Positive Energy Ladder Representations of 𝔲 (2, 2)  𝔰𝔲 (2, 2)  𝔰𝔬 (4, 2) ⊕𝔲 (1) ⊂ 𝔠𝔩 (4, 2) Describing Massless Particles of Any Helici

In this representation of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2), the generators 𝑇𝑖 and 𝐶𝑖 act by construction as ladder operators, raising and lowering the eigenvalues of the conformal
Hamiltonian 𝐻, respectively. In particular, from the latter canonical commutation
relation, it follows that the lowering operators 𝐶𝑖 annihilate the lowest weight state
|LW𝜆 ⟩, which is an eigenstate of 𝐻 with eigenvalue E◦ := 1 + |𝜆| (see Eq. (3.142)):
𝐶𝑖 |LW𝜆 ⟩ = 0 .

(3.196)

The commutation relation (3.192) implies that the operators 𝐽𝑖 𝑗 , which generate
the maximal compact subalgebra 𝔰𝔬(4)  𝔰𝔲(2) 𝐿 ⊕ 𝔰𝔲(2) 𝑅 , leave invariant the
eigenspaces HE(1) of the conformal Hamiltonian 𝐻, as noted before. In a particularly
significant case, the operators 𝐽𝑖 𝑗 act on the lowest weight state in the zero-helicity
(𝜆 = 0) case as follows:
𝐽𝑖 𝑗 |LW𝜆=0 ⟩ =: 𝐽𝑖 𝑗 |0SO(4) ⟩ = 0 .

(3.197)

This condition explicitly demonstrates that the zero-helicity lowest weight state
|LW𝜆=0 ⟩ =: |0SO(4) ⟩ transforms as a singlet under the maximal compact subgroup
SO(4), justifying its designation as a “Fock vacuum” with respect to this subgroup
(see Eq. (3.41) and the accompanying discussion). Of course, it should not be confused with the unique conformally invariant zero-energy vacuum state |0U(2,2) ⟩, which
is invariant under the full conformal group U(2, 2) and will be introduced later in
the context of the complete conformal field theory (CFT) construction.
Note that the identities stated in the above proposition can be proven either
within the oscillator (or twistor) realization (3.99)-(3.114) of the generators or independently, based on the intrinsic algebraic relations (3.37) among the 𝐽 𝜇𝜈 entities
involved. For pedagogical clarity, we present below a proof that seeks to strike a
balance between these two approaches, highlighting in each case the method that
offers the more instructive perspective.
Proof — Step I (proof of the commutation relations (3.193)). The commutation
relations presented above can be readily derived from the known algebraic properties
(3.37) of the generators 𝐽 𝜇𝜈 . Nevertheless, it is instructive to verify them explicitly
within the oscillator (or twistor) realization (3.99)-(3.114) of the generators. As an
illustration, let us consider (3.193).
By employing Eq. (3.38) in combination with the previously established decompositions, we obtain the following commutation relations between the operators 𝐶𝑖
and 𝑇 𝑗 :

## PDF page 114

100

[

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

] [
]
𝐶𝑖 , 𝑇 𝑗 = 𝔟 𝐴 (E𝑖∗ ) 𝐴𝐵 𝔞 𝐵 , 𝔞 ∗𝐸 (E 𝑗 ) 𝐸𝐷 𝔟∗𝐷
[
]
[
]
= 𝔟 𝐴 (E𝑖∗ ) 𝐴𝐵 𝔞 𝐵 , 𝔞 ∗𝐸 (E 𝑗 ) 𝐸𝐷 𝔟∗𝐷 + 𝔟 𝐴, 𝔞 ∗𝐸 (E 𝑗 ) 𝐸𝐷 (E𝑖∗ ) 𝐴𝐵 𝔞 𝐵 𝔟∗𝐷
⏟
⏞⏞
⏟
⏟
⏞⏞
⏟
𝐵 ( E ) 𝐸𝐷
= ( E𝑖∗ ) 𝐴𝐵 𝛿𝐸
𝑗

+ 𝔞 ∗𝐸 (E 𝑗 ) 𝐸𝐷 𝔟 𝐴

[

=0

(E𝑖∗ ) 𝐴𝐵 𝔞 𝐵 , 𝔟∗𝐷

⏟

⏞⏞

]

+ 𝔞 ∗𝐸 (E 𝑗 ) 𝐸𝐷

⏟

=0

[ 𝐴 ∗] ∗
𝔟 , 𝔟 𝐷 (E𝑖 ) 𝐴𝐵 𝔞 𝐵
⏟ ⏞⏞ ⏟
𝐴
= 𝛿𝐷

= 𝔟 E𝑖∗ E 𝑗 𝔟∗ + 𝔞 ∗ E 𝑗 E𝑖∗ 𝔞
= 2𝐻 𝛿𝑖 𝑗 − 2𝐽𝑖 𝑗 .

(3.198)

Regarding the derivation of the last line, note that E 𝑗 E𝑖∗ = E𝑖∗ E 𝑗 = 1, when 𝑖 = 𝑗,
and E 𝑗 E𝑖∗ = −E𝑖 E ∗𝑗 , when 𝑖 ≠ 𝑗 (recall that 𝑖, 𝑗 = 1, 2, 3, 4).
Proceeding analogously to the steps outlined above, with Eq. (3.38) in mind, the
remaining commutation relations (3.192), (3.194), and (3.195) follow directly within
the oscillator (or twistor) realization (3.99)-(3.114).
— Step II (proof of (3.196)). Using a procedure analogous to that described in
Remark 3.9, the proof of Eq. (3.196) follows directly from the commutation relation
(3.195). On the other hand, employing the oscillator (or twistor) realization (3.99)(3.114) of the generators, together with the definition (3.62), immediately leads to
Eq. (3.196).
— Step III (proof of (3.197)). Eq. (3.197) can be straightforwardly verified
through the (relevant) matrix realization (3.99)-(3.114), in conjunction with (3.62).
We, however, choose to present an alternative — and arguably more illustrative —
proof that relies purely on the algebraic relations intrinsic to the generators.
We begin with the conformal Hamiltonian 𝐻 and the angular momentum-like
generators 𝐽𝑖 𝑗 , which satisfy the commutation relation [𝐻, 𝐽𝑖 𝑗 ] = 0 (3.192). This
relation implies that each 𝐽𝑖 𝑗 preserves the eigenspaces HE(1) ⊂ H𝜆(1) of 𝐻 (3.145);
that is:
𝐽𝑖 𝑗 ;

HE(1) ↦−→ HE(1) .

(3.199)

In particular, this invariance extends to the zero-helicity, lowest-energy eigenspace
HE(1)
, which contains solely (up to an overall scalar factor) the lowest weight state
◦
|LW𝜆=0 ⟩ =: |0SO(4) ⟩ =: |1, 0, 0⟩. As a matter of fact, as can be deduced from Eq.
(3.150) for j 𝐿 = 0 = j𝑅 , this eigenspace is 1-dimensional. It then naturally follows
that the action of 𝐽𝑖 𝑗 on this state must take the form:
𝐽𝑖 𝑗 |LW𝜆=0 ⟩ = 𝛼𝑖 𝑗 |LW𝜆=0 ⟩ ,

(3.200)

for some scalar coefficients 𝛼𝑖 𝑗 ∈ C.
The generators 𝐽𝑖 𝑗 span the compact subalgebra 𝔰𝔬(4)  𝔰𝔲(2) 𝐿 ⊕ 𝔰𝔲(2) 𝑅 , and
therefore act as angular momentum operators. In any unitary representation, they
are represented by traceless anti-Hermitian matrices. On the 1-dimensional space
HE(1)
, the only possible linear operators are scalar multiples of the identity. Imposing
◦

## PDF page 115

3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex Algebra

101

tracelessness forces the scalar to vanish. Hence, the only consistent possibility is:
𝛼𝑖 𝑗 = 0

=⇒

𝐽𝑖 𝑗 |LW𝜆=0 ⟩ =: 𝐽𝑖 𝑗 |0SO(4) ⟩ = 0 ,

(3.201)

which shows that |LW𝜆=0 ⟩ =: 𝐽𝑖 𝑗 |0SO(4) ⟩ transforms trivially — i.e., as a singlet —
under the maximal compact subgroup generated by 𝐽𝑖 𝑗 .
□

3.4 Complex Analytic Picture: Globally Conformal Invariant
Vertex Algebra
In terms of the homogeneous coordinates R4,2 ∋ 𝜁 = (𝜁 𝜇 ; 𝜇 = 0, 5, 1, 2, 3, 4) over
the Dirac quadric 𝑄 [23]:
(
)
4
∑︁
𝑖
2
𝑄 ; 𝜁 𝜁𝑖 :=
(𝜁𝑖 ) = (𝜁0 ) 2 + (𝜁5 ) 2 > 0 ,
𝑖=1

𝜁 ∼ 𝜚𝜁 ,

𝜚 ∈ R \ {0} ,

with

(3.202)

the complex coordinates 𝑧 𝑖 , on the compactified Minkowski space17 :
𝑀 compact 

S3 × S1
 U(2) ,
Z2

(3.203)

are defined by [109]:
𝑧𝑖 =

𝜁𝑖
,
𝜁 5 − i𝜁 0

𝑖 = 1, . . . , 4 .

(3.204)

One notes that:
𝜁𝑖 = 𝜁 𝑖

(

)
=⇒ 𝑧𝑖 = 𝑧𝑖 ,

𝜁 𝑘 = −𝜁 𝑘 ,

for

for 𝑖 = 1, . . . , 4 ,

(3.205)

𝑘 = 0, 5 ,

(3.206)

𝑧𝑖
𝜁𝑖
=
∈ R,
𝑧𝑗
𝜁𝑗
(
𝑧 · 𝑧 :=

4
∑︁

(3.207)

)
𝑧𝑖 𝑧𝑖 = 1 ,

(3.208)

𝑖=1

17 The identification of the conformal compactification of Minkowski space with the Shilov bound-

ary of the associated Hermitian symmetric domain is recalled in Appendix 3.8.

## PDF page 116

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

102

(
2

(𝑧) = 𝑧 · 𝑧 :=

4
∑︁

)
𝑖

𝑧 𝑧𝑖 =

𝑖=1

𝜁 𝑖 𝜁𝑖
(𝜁 5 + i𝜁 0 ) (𝜁 5 − i𝜁 0 )
=
(𝜁 5 − i𝜁 0 ) (𝜁 5 − i𝜁 0 )
(𝜁 5 − i𝜁 0 ) (𝜁 5 − i𝜁 0 )
=

(𝜁 5 + i𝜁 0 )
=: 𝑒 2i𝜏 , (3.209)
(𝜁 5 − i𝜁 0 )

where 𝜏 ∈ R is called “conformal time”.
The condition 𝑧 · 𝑧 = 1 constrains 𝑧 to lie on the 3-sphere S3 ⊂ C4 , while the
complex phase of (𝑧) 2 = 𝑧 · 𝑧 = 𝑒 2i𝜏 naturally parametrizes a circle S1 . Together,
these properties show that, locally, the complex coordinates 𝑧 describe the product
space S3 × S1 . Globally, the projective identification 𝜁 ∼ −𝜁 induces the equivalence
𝑧 ∼ −𝑧, pairing antipodal points on this product. As a result, the compactified
Minkowski space inherits the topology S3 × S1 /Z2  U(2), capturing both the
spherical and circular structure together with the discrete Z2 identification arising
from projectivity.
The complex variables 𝑧𝑖 are related to the real Minkowski spacetime 𝑀  R3,1
coordinates 𝑥 𝜇¤ ( 𝜇¤ = 0, 1, 2, 3) by a complex conformal transformation:
𝑔𝑐 ;

𝑀  R3,1

S3 × S1
 U(2) ,
Z2

(3.210)

)
1 − (𝑥) 2
⃗𝑥
, 𝑧4 =
∈ 𝑀 compact ,
Ω(𝑥)
2Ω(𝑥)

(3.211)

↦−→

𝑀 compact 

which explicitly reads as:
(
𝑔𝑐 (𝑥 ∈ 𝑀) = 𝑧 = ⃗𝑧 =

where ⃗𝑧 = (𝑧1 , 𝑧2 , 𝑧3 ), ⃗𝑥 = (𝑥 1 , 𝑥 2 , 𝑥 3 ), (𝑥) 2 = 𝑥 𝜇¤ 𝑥 𝜇¤ = (⃗𝑥 ) 2 − (𝑥 0 ) 2 , and:
Ω(𝑥) =

1 + (𝑥) 2
− i𝑥 0 .
2

(3.212)

With the above definition, one checks that 𝑧 · 𝑧 = 1 and (𝑧) 2 = 𝑒 2i𝜏 . Moreover, we
observe that:
(
)
4
∑︁
(d𝑥) 2
2
𝑖
(d𝑧) = :=
d𝑧 d𝑧 𝑖 = 2
,
(3.213)
Ω (𝑥)
𝑖=1
)2
(
(𝑥 − 𝑦) 2
.
(𝑧 − 𝑢) 2 = 𝑔𝑐 (𝑥) − 𝑔𝑐 (𝑦) =
Ω(𝑥) Ω(𝑦)
⏟⏞⏞⏟ ⏟⏞⏞⏟
=: 𝑧

(3.214)

=: 𝑢

Equation (3.213) implies that the pullback of the flat metric in 𝑧-space is conformally
equivalent to the Minkowski metric in 𝑥-space, thereby establishing conformality in
the infinitesimal (local) sense. Hence, the map 𝑔𝑐 is locally conformal. On the other
hand, Eq. (3.214) demonstrates that causal structure and angular relationships are

## PDF page 117

3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex Algebra

103

preserved up to a position-dependent scale factor, confirming that 𝑔𝑐 is globally
conformal as well.
To give meaning to quantum fields depending on complex variables, we recall
U(2,2)
ˆ
some properties of the vector-valued distribution 𝜙(𝑥)|0
⟩ which follow from the
basic assumptions (Wightman assumptions) of relativistic QFT [110, 111].
Theorem 3.1 We recall:
U(2,2)
ˆ
1. Wightman axioms imply that the (ket-)vector-valued distribution 𝜙(𝑥)|0
⟩,
U(2,2)
ˆ
where 𝜙 is a relativistic quantum field and |0
⟩ is the Poincaré-invariant18
vacuum vector, arises as the boundary value (𝑦 → 0) — in the distributional
sense — of an analytic (ket-)vector-valued function defined in the forward tube
𝔗+:
{
}
ˆ + i𝑦)|0U(2,2) ⟩ , for (𝑥 + i𝑦) ∈ 𝔗 + = 𝑥 + i𝑦 ; 𝑥, 𝑦 ∈ R3,1 , 𝑦 0 > |⃗𝑦| ,
𝜙(𝑥

(3.215)
√︁
where ⃗𝑦 = (𝑦 1 , 𝑦 2 , 𝑦 3 ) and |⃗𝑦| = (𝑦 1 ) 2 + (𝑦 2 ) 2 + (𝑦 3 ) 2 .
2. The rational complex coordinate transformation 𝑔𝑐 , mapping the complexified
Minkowski space 𝑀C  C3,1 onto the complexified Euclidean space 𝐸 C  C4 :
𝑀C  C3,1

𝑔𝑐 ;

↦−→

𝐸 C  C4 ,

(3.216)

is regular (holomorphic) on the forward tube 𝔗 + and maps it into:
𝑔𝑐 ;

𝔗 + ⊂ 𝑀C

↦−→

𝔗 precompact
⊂ 𝐸C ,
+

(3.217)

which explicitly reads:
{

precompact

𝑔𝑐 (𝔗 + ) = 𝔗 +

)}
1(
22
= 𝑧 ∈ C ; (𝑧) < 1, 𝑧 · 𝑧 <
. (3.218)
1 + (𝑧)
2
4

2

Note that 𝔗 precompact
is a precompact domain19 in 𝐸 C . Furthermore, this transforma+
tion preserves the form of Eqs. (3.213) and (3.214) under analytic continuation.
18 It is important to clarify that throughout this work, we denote by |0U(2,2) ⟩ the unique vacuum

state of the theory. In the setting of CFT, this vacuum is invariant under the full conformal group
U(2, 2), and in particular under its Poincaré subgroup. In the broader context of QFT, |0U(2,2) ⟩
refers to the Poincaré-invariant vacuum defined within the Wightman framework, characterized by
translation invariance and the spectral condition. In theories with exact conformal symmetry, these
two notions are compatible and in fact coincide. Accordingly, it is natural and consistent to use the
same notation for both.
19 The domain 𝔗 precompact is, by construction, an open subset of C4 . Since it is open, it is not closed,
+
and therefore not compact (in finite-dimensional spaces, compactness is equivalent to closedness
and boundedness). Nevertheless, 𝔗 precompact
is bounded, being entirely contained within the open
+
unit ball. Consequently, its closure lies inside the closed unit ball, which is compact. Thus, while
the set itself is not compact, its closure is compact, and the set is therefore referred to as precompact
(or relatively compact).

## PDF page 118

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

104

3. The tube domain 𝔗 + and its image 𝔗 precompact
are each invariant under real confor+
mal transformations20 [112]. The closure 𝑀 compact of the precompact image of 𝑀
in 𝐸 C has the form:
{
( 4
)
}
∑︁
𝑀 compact = 𝑧 = 𝑟𝑒 i𝜏 ; 𝑟 = (𝑟 𝑖 , 𝑖 = 1, . . . , 4) ∈ R4 , 𝜏 ∈ R , (𝑟) 2 =
(𝑟 𝑖 ) 2 = 1
𝑖=1

S3 × S1

.
Z2

(3.219)

Note that 𝑧 remains invariant under the change of coordinates (𝑟, 𝜏) ↦−→ (−𝑟, 𝜏 +
𝜋).
Proof — Step I (the proof of 1). The proof of (1) relies on the spectrum condition
(energy positivity and Poincaré invariance) and standard properties of the Laplace
transform of tempered distributions [110, 111].
By the Wightman axioms, the state ˆ
𝜙(𝑥)|0U(2,2) ⟩ defines a vector-valued tempered
distribution on R3,1 . In particular, its Fourier transform exists in the sense of tempered
distributions and has support contained in the closed forward light cone:
{
}
𝑉+ := 𝑝 ∈ R3,1 ; 𝑝 0 ≥ 0 , ( 𝑝 0 ) 2 − (⃗𝑝 ) 2 ≥ 0 .
(3.220)
This is the content of the spectrum condition, which follows from energy positivity
and Poincaré invariance.
3,1
We now apply the Laplace transform to this
√︁ distribution. For any 𝑦 ∈ R , with
0
1
2
3
1
2
2
2
3
2
𝑦 > |⃗𝑦| (where ⃗𝑦 = (𝑦 , 𝑦 , 𝑦 ) and |⃗𝑦| = (𝑦 ) + (𝑦 ) + (𝑦 ) ), we define the
complex spacetime point as 𝑧 = 𝑥 + i𝑦, and consider the (ket-)vector-valued function
as:
∫
𝜇¤
ˆ
𝜙(𝑧)|0U(2,2) ⟩ :=
𝑒 −i 𝑝𝜇¤ 𝑧 ˆ
𝜙( 𝑝)|0U(2,2) ⟩ d𝑝 ,
(3.221)
𝑉+

where ˆ
𝜙( 𝑝)|0U(2,2) ⟩ denotes the Fourier transform of ˆ
𝜙(𝑥)|0U(2,2) ⟩ and 𝜇¤ = 0, 1, 2, 3.
Since 𝑝 0 ≥ |⃗𝑝 | ≥ 0 and 𝑦 0 > |⃗𝑦|, and by Cauchy-Schwarz inequality:
−|⃗𝑝 | |⃗𝑦| ≤ ⃗𝑝 · ⃗𝑦 = 𝑝 1 𝑦 1 + 𝑝 2 𝑦 2 + 𝑝 3 𝑦 3 ≤ |⃗𝑝 | |⃗𝑦| ,

(3.222)

(
)
(
)
Im 𝑝 𝜇¤ 𝑧 𝜇¤ ≤ −𝑝 0 𝑦 0 + |⃗𝑝 | |⃗𝑦| ≤ − 𝑝 0 𝑦 0 − |⃗𝑦| ≤ 0 ,
⏟⏞⏞⏟ ⏟ ⏞⏞ ⏟

(3.223)

we have:

≥0

>0

20 Without assuming conformal invariance of underlying QFT (a fact noted earlier by V. Glaser,

unpublished), 𝔗 precompact
is a homogeneous space of the conformal
group;
+
(
) the stabilizer subgroup
of 𝑧 = 0 ∈ 𝔗 precompact
is the maximal compact subgroup S U(2) × U(2) ⊂ SU(2, 2).
+

## PDF page 119

3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex Algebra
𝜇¤

𝜇¤

105
𝜇¤

which ensures that the exponential factor 𝑒 −i 𝑝𝜇¤ 𝑧 = 𝑒 −i 𝑝𝜇¤ 𝑥 𝑒 𝑝𝜇¤ 𝑦 decays exponentially
in 𝑝. As a result, the} integral converges for all 𝑧 ∈ 𝔗 + , where
{
U(2,2)
ˆ
𝔗 + := 𝑧 ∈ C4 ; Im 𝑧 = 𝑦, 𝑦 0 > |⃗𝑦| . Thus, 𝜙(𝑧)|0
⟩ defines a well-defined, analytic vector-valued function in the forward tube 𝔗 + .
On the other hand, by standard results on the Laplace transform of tempered
distributions with support in the forward light cone (see, e.g., [110, 111]), the
U(2,2)
U(2,2)
ˆ
ˆ
analytic function 𝜙(𝑧)|0
⟩ admits the original distribution 𝜙(𝑥)|0
⟩ as its
boundary value in the distributional sense as 𝑦 → 0 within 𝔗 + . That is, for any
smooth test function 𝑓 (𝑥) with compact support in 𝑀  R3,1 , one has:
∫
∫
U(2,2)
U(2,2)
ˆ
ˆ
lim
𝑓 (𝑥) 𝜙(𝑥 + i𝑦)|0
⟩ d𝑥 =
𝑓 (𝑥) 𝜙(𝑥)|0
⟩ d𝑥 . (3.224)
𝑦→0, 𝑦 0 >|⃗
𝑦|

R3,1

R3,1

U(2,2)
ˆ
This establishes that 𝜙(𝑥)|0
⟩ arises as the boundary value of the analytic function
U(2,2)
ˆ
𝜙(𝑧)|0
⟩ from the forward tube 𝔗 + . This completes the proof.
— Step II (the proof of 2). The proof of the second item follows from a direct
calculation [109, 113]. As an illustration, let us focus on the first part of the statement
— namely, the regularity of the conformal map:
)
(
1 − (𝑤) 2
1 + (𝑤) 2
⃗𝑤
, 𝑧4 =
, Ω(𝑤) =
− i𝑤0 ,
𝑔𝑐 ; 𝑤 ↦−→ 𝑧 = ⃗𝑧 =
Ω(𝑤)
2Ω(𝑤)
2
(3.225)

{
}
on the forward tube 𝔗 + = 𝑤 := 𝑥 + i𝑦 ; 𝑥, 𝑦 ∈ R3,1 , 𝑦 0 > |⃗𝑦| . The map 𝑔𝑐 is
regular (holomorphic) on 𝔗 + provided that its denominator never vanishes there;
in other words, regularity of 𝑔𝑐 on the forward tube requires that Ω(𝑤) ≠ 0 for all
𝑤 ∈ 𝔗+.
Suppose, for contradiction, that Ω(𝑤) = 0 at some 𝑤 ∈ 𝔗 + :
Ω(𝑤) =

1 + (𝑤) 2
1 + (𝑥 + i𝑦) 2
− i𝑤0 =
− i(𝑥 0 + i𝑦 0 )
2
2
1 + (𝑥) 2 − (𝑦) 2
=
+ 𝑦 0 − i(𝑥 0 − 𝑥 · 𝑦) = 0 .
2

(3.226)

This implies that:
Re Ω(𝑤) =

1 + (𝑥) 2 − (𝑦) 2
+ 𝑦0 = 0
2

=⇒

(
)2
(𝑥) 2 = − 1 + 𝑦 0 + |⃗𝑦| 2 ,
(
)
⇓ since 𝑦 0 > |⃗𝑦| ≥ 0
(𝑥 0 ) 2 > |⃗𝑥 | 2 ≥ 0 ,

and:

(3.227)

## PDF page 120

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

106

Im Ω(𝑤) = 𝑥 0 − 𝑥 · 𝑦 = 0

𝑥 0 = 𝑥 · 𝑦 = −𝑥 0 𝑦 0 + ⃗𝑥 · ⃗𝑦

=⇒

⇓
0(

)
𝑥 1 + 𝑦 0 = ⃗𝑥 · ⃗𝑦
(
)
⇓ by Cauchy-Schwarz inequality (3.222)
(
)
− |⃗𝑥 | |⃗𝑦| ≤ 𝑥 0 1 + 𝑦 0 ≤ |⃗𝑥 | |⃗𝑦| .
(3.228)
The latter inequality evidently contradicts the conditions 𝑦 0 > |⃗𝑦| ≥ 0 and
(𝑥 0 ) 2 > |⃗𝑥 | 2 ≥ 0. Hence, the assumption Ω(𝑤) = 0 is invalid, and the conformal transformation 𝑔𝑐 is therefore regular (holomorphic) over the entire forward
tube 𝔗 + .
— Step III (the proof of 3). The map 𝑔𝑐 ; 𝑥 ↦−→ 𝑧 = 𝑟𝑒 i𝜏 , where (𝑟) 2 = 1, was
originally proposed [109, 112] as a (generalized) Cayley map from the Lie algebra
𝔲(2) to the group U(2):
𝑔𝑐 ; 𝔯 = 𝑥 𝑗 E ∗𝑗 + i𝑥 0 ∈ 𝔰𝔲(2) ⊕ 𝔲(1)  𝔲(2)
↦−→

𝑧 := 𝑧 𝑗 E ∗𝑗 =

1+𝔯
=: 𝑟𝑒 i𝜏 ∈ U(2) ,
1−𝔯

(3.229)

where, in accord with the notational conventions established in Proposition 3.1, the
symbols E ∗𝑗 ( 𝑗 = 1, 2, 3) denote the standard imaginary quaternionic units, which
satisfy (E ∗𝑗 ) 2 = E1∗ E2∗ E3∗ = −E4∗ = −1. The scalar i ∈ C, representing the complex
imaginary unit with i2 = −1, is assumed to commute with all E ∗𝑗 ( 𝑗 = 1, 2, 3, 4), i.e.,
[ ∗]
i, E 𝑗 = 0. On this basis, by multiplying both the numerator and the denominator
1+𝔯
of (1 + 𝔯)/(1 − 𝔯) by 1 + 𝔯 = 1 + 𝑥 𝑗 E ∗𝑗 − i𝑥 0 ,21 one verifies that 𝑧 := 𝑧 𝑗 E ∗𝑗 = 1−𝔯
is indeed equivalent to (3.211). Keeping this equivalence in mind, one readily finds
1+𝔯
that 𝑧 · 𝑧 = 1 and (𝑧) 2 = 𝑒 2i𝜏 , which together justify 𝑧 := 1−𝔯
= 𝑟𝑒 i𝜏 ∈ U(2).
□
ˆ
Remark 3.15 Importantly, the corresponding bra-vector-valued function ⟨0U(2,2) | 𝜙(𝑥)
is analytic in the backward tube 𝔗 − — complex conjugate to 𝔗 + :
(
) {
}
⟨0U(2,2) | ˆ
𝜙(𝑥 + i𝑦) , is analytic in 𝔗 − = 𝔗 + = 𝑥 + i𝑦 ; 𝑥, 𝑦 ∈ R4 , 𝑦 0 < −|⃗𝑦| .
(3.230)
The backward tube 𝔗 precompact
can also be defined in the 𝑧-picture as the image of 𝔗 −
−
under the map 𝑔𝑐 (3.211):
𝑔𝑐 ;

𝔗 − ⊂ 𝑀C  C3,1

↦−→

𝔗 precompact
⊂ 𝐸 C  C4 .
−

(3.231)
□

Remark 3.16 The bra and ket vectors ⟨0U(2,2) | ˆ
𝜙(𝑥) and ˆ
𝜙(𝑥)|0U(2,2) ⟩, respectively, are
ill-defined for real spacetime points 𝑥. They are only meaningful as vector-valued
distributions — that is, they become well-defined only after smearing ˆ
𝜙(𝑥) with a
21 Note that 𝔯𝔯 = − ( 𝑥 ) 2 .

## PDF page 121

3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex Algebra

107

suitable test function. In particular, this distributional nature is reflected in vacuum
expectation values of field products, such as the Wightman two-point function:
𝑊 (𝑧1 , 𝑧2 ) = ⟨0U(2,2) | ˆ
𝜙(𝑧 1 ) ˆ
𝜙(𝑧2 )|0U(2,2) ⟩ ,

(3.232)

where 𝑧 𝑗 = 𝑥 𝑗 + i𝑦 𝑗 , with 𝑗 = 1, 2. The two-point function 𝑊 (𝑧1 , 𝑧2 ) is naturally
defined on complexified spacetime and possesses different (complex conjugate)
analyticity domains in its first (𝑧 1 ) and second (𝑧 2 ) arguments.
□
Proposition 3.5 A conformal conjugation in 𝐸 C  C4 is defined by:
↦−→

𝑧

𝑧∗ :=

𝑧
.
(𝑧) 2

(3.233)

This conformal conjugation interchanges the precompact forward and backward
tubes:
𝑧 ∈ 𝔗 precompact
±

⇐⇒

𝑧∗ ∈ 𝔗 precompact
,
∓

(3.234)

and leaves the compactified Minkowski space 𝑀 compact pointwise invariant:
𝑧∗ = 𝑧 ,

for any

𝑧 ∈ 𝑀 compact .

(3.235)

In fact, the conformal conjugation acts as the identity on 𝑀 compact .
Proof — Step I (interchanging the tubes). Let 𝑧 ∈ 𝔗 precompact
, i.e., there exists
+
𝑥 + i𝑦 ∈ 𝔗 + (with 𝑥, 𝑦 ∈ 𝑀  R3,1 and 𝑦 0 > |⃗𝑦|), such that:
𝑧 = 𝑔𝑐 (𝑥 + i𝑦) .

(3.236)

We need to show:
𝑧∗ = (

𝑔𝑐 (𝑥 + i𝑦)
) 2 = 𝑔𝑐 (𝑥 − i𝑦) ,
𝑔𝑐 (𝑥 + i𝑦)

(3.237)

where, by construction, (𝑥 − i𝑦) ∈ 𝔗 + = 𝔗 − , and hence 𝑔𝑐 (𝑥 − i𝑦) ∈ 𝔗 precompact
. This
−
follows from a direct computation using the explicit form:
)
(
⃗𝑥 ± i⃗𝑦 1 − (𝑥 ± i𝑦) 2
𝑔𝑐 (𝑥 ± i𝑦) =
,
,
(3.238)
Ω±
2Ω±
2

where Ω± := 1+( 𝑥±i𝑦)
− i(𝑥 0 ± i𝑦 0 ). The converse direction follows similarly by
2
reversing the sign of i𝑦.
— Step II (𝑧∗ = 𝑧 iff 𝑧 ∈ 𝑀 compact ). This follows immediately from the realization
(3.219), valid for all 𝑧 ∈ 𝑀 compact .
□
Remark 3.17 If we define 𝑥 4 := −i𝑥 0 and reinterpret 𝑔𝑐 as a map between two
Euclidean spaces, i.e., (⃗𝑥 , 𝑥4 ) ↦−→ (⃗𝑧, 𝑧 4 ), then the inverse map 𝑧 ↦−→ 𝑥 retains the

## PDF page 122

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

108

same functional form as (3.211):
𝑔𝑐−1 (𝑧) = 𝑥 =

(
⃗𝑥 =

)
1 − (𝑧) 2
⃗𝑧
, 𝑥4 =
,
Ω(𝑧)
2Ω(𝑧)

(3.239)

2

where Ω(𝑧) = 1+(𝑧)
+ 𝑧 4 . We actually have:
2
(
)
𝑔𝑐−1 𝑔𝑐 (𝑥) = 𝑥 .

(3.240)
□

3.4.1 Free Massless Scalar Field
ˆ
We now reformulate the theory of the free massless scalar field 𝜙(𝑥),
whose two-point
3,1
function in Minkowski spacetime 𝑀  R is given by:
∫ −i ( ⃗𝑝 ·⃗𝑥 − | ⃗𝑝 | 𝑥 0 )
12
12
𝑒
1
ˆ 1 ) 𝜙(𝑥
ˆ 2 )⟩0 =
d3 ⃗𝑝 ,
⟨𝜙(𝑥
(
) =
3
0
2
2
2
(2𝜋) 2|⃗𝑝 |
(2𝜋) (⃗𝑥12 ) − (𝑥 12 − i0)
(3.241)
0 = 𝑥 0 − 𝑥 0 and ⃗
where 𝑥12 = 𝑥1 − 𝑥 2 (that is, 𝑥12
𝑥12 = ⃗𝑥 1 − ⃗𝑥 2 ) and 𝑝 0 = |⃗𝑝 | =
1
2
√︃
2
2
2
𝑝 1 + 𝑝 2 + 𝑝 3 is the energy of a free massless scalar field. We reinterpret this
theory in terms of a conformal vertex operator:

)
2𝜋 ˆ (
ˆ
𝜙(𝑧) :=
𝜙 𝑥 = 𝑔𝑐 (𝑧) ,
Ω(𝑧)

(3.242)

which defines a scalar field of conformal dimension22 E = 1 on the conformally
compactified Minkowski space 𝑀 compact .
22 The “conformal dimension” (also called “scaling dimension”) E of a field 𝜙 ( 𝑥 ) is defined by its

transformation under dilations (scale transformations) of the spacetime coordinates:
𝑥 𝜇¤

↦ −→

𝑥 ′ 𝜇¤ = 𝜚𝑥 𝜇¤ ,
=⇒

𝜙 ( 𝑥)

𝜚 > 0,
↦ −→

𝜙 ′ ( 𝑥 ′ ) ∼ 𝜙 ( 𝑥 ′ ) = 𝜚 −E 𝜙 ( 𝑥 ) .

Note that, in the last expression, the “prime” on the field is omitted by convention (𝜙 ′ ( 𝑥 ′ ) ∼ 𝜙 ( 𝑥 ′ )),
and the field is understood to be the transformed one, identified by its transformed coordinate. This
transformation rule ensures that correlation functions and the action remain consistent with scale
invariance. For a∫free, massless scalar field in 4-dimensional spacetime, conformal invariance of
the kinetic term 𝑑 4 𝑥 (𝜕𝜇¤ ˆ
𝜙) 2 fixes E = 1; see also footnote 14. In our case, the field 𝜙ˆ (𝑧) :=
(
)
2𝜋 ˆ
ˆ
Ω(𝑧) 𝜙 𝑔𝑐 (𝑧) is defined as a conformally rescaled version of the free scalar field 𝜙 ( 𝑥 ), where
𝑥 = 𝑔𝑐 (𝑧) is a conformal map from the compactified coordinates 𝑧 to Minkowski coordinates 𝑥.
1
The factor Ω(𝑧)
ensures that 𝜙ˆ (𝑧) transforms as a primary scalar field of conformal dimension
E = 1 under conformal transformations in the compactified coordinates.

## PDF page 123

3.4 Complex Analytic Picture: Globally Conformal Invariant Vertex Algebra

109

Remarkably, the two-point function of the transformed field ˆ
𝜙(𝑧) has essentially
the same form as (3.241), up to a conformally invariant factor. Specifically, by
starting from the original two-point function (3.241) and considering the conformal
transformation (3.239) together with the corresponding conformal distance relation
(analogous to (3.214)), we obtain:
⟨ (
)⟩
) (
𝜙ˆ 𝑥1 = 𝑔𝑐 (𝑧) 𝜙ˆ 𝑥2 = 𝑔𝑐 (𝑢) 0 =
=

1
1
(
)
(2𝜋) 2 𝑔𝑐 (𝑧) − 𝑔𝑐 (𝑢) 2
1 Ω(𝑧) Ω(𝑢)
.
(2𝜋) 2 (𝑧 − 𝑢) 2

(3.243)

(
)
2𝜋 ˆ
Then, to obtain the two-point function of the rescaled field ˆ
𝜙(𝑧) = Ω(𝑧)
𝜙 𝑔𝑐 (𝑧) ,
we multiply the above expression by the corresponding factors:
)(
)
(
)⟩
) (
2𝜋 ⟨ ˆ (
2𝜋
𝜙 𝑔𝑐 (𝑧) 𝜙ˆ 𝑔𝑐 (𝑢) 0
𝑾 (𝑧, 𝑢) := ⟨0U(2,2) | ˆ
𝜙(𝑧) ˆ
𝜙(𝑢)|0U(2,2) ⟩ =
Ω(𝑧) Ω(𝑢)
1
.
(3.244)
=
(𝑧 − 𝑢) 2
One notes that 𝑾 (𝑧, 𝑢) incorporates the conformal weight, thereby ensuring the
correct transformation behavior under conformal mappings.
ˆ 1)
It is important to emphasize that the asymmetry between the two factors 𝜙(𝑥
2
ˆ
and 𝜙(𝑥2 ), manifested through the presence of (· · · − i0) (or, equivalently, through
the support of the Fourier transform) in (3.241), persists in the analytic (𝑧-)picture
— though it is no longer apparent in the notation used in (3.244). Strictly speaking,
the function 𝑾 (𝑧, 𝑢) is analytic for 𝑢 ∈ 𝔗 precompact
and 𝑧 ∈ 𝔗 precompact
, where 𝔗 precompact
+
+
−
is the bounded domain defined in (3.218) that contains the origin (𝑢 = 0), and
𝔗 precompact
— implicitly defined by Eqs. (3.233) and (3.234) — is an unbounded
−
domain surrounding the point at infinity.
This reformulation sets the stage for introducing and illustrating the fundamental structures of a higher-dimensional conformal vertex algebra. Through explicit
computations, it reveals several unexpected features of the familiar free scalar field
theory.
Proposition 3.6 The conformal conjugation map (3.233) extends naturally to field
(1)
operators and to vectors in the Hilbert space H𝜆=0
of zero-helicity, massless oneparticle states, by defining:
)∗
1 ˆ ∗
ˆ
𝜙(𝑧)
=
𝜙(𝑧 ) .
(3.245)
(𝑧) 2
(
)∗
Proof To derive (3.245), we interpret the conjugated operator ˆ
𝜙(𝑧) as arising
from ˆ
𝜙(𝑧) via the conformal inversion.
— Step I (conformal inversion and Weyl scaling). Conformal inversion reads
as:
(

)∗
(
)∗
U(2,2)
ˆ
ˆ
𝜙(𝑧)|0
⟩ = ⟨0U(2,2) | 𝜙(𝑧)
,

where

(

## PDF page 124

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

110

↦−→

𝑧

𝑧˘ :=

𝑧
.
(𝑧) 2

(3.246)

The conformal conjugation map (3.233) can thus be understood as the composition
of complex conjugation with conformal inversion:
𝑧∗ = 𝑧˘ = 𝑧˘ =

𝑧
.
(𝑧) 2

(3.247)

The inversion
map (3.246) is conformal in the sense that the squared line element
∑
(d𝑧) 2 = 4𝑖=1 d𝑧 𝑖 d𝑧 𝑖 is rescaled by a Weyl factor. This can be seen by explicitly
computing the differential of 𝑧˘𝑖 :
𝑧˘𝑖 =

𝑧𝑖
(𝑧) 2

=⇒

d𝑧˘𝑖 =

d𝑧 𝑖
𝑧𝑖 d(𝑧) 2
−
( 2)2 ,
(𝑧) 2
(𝑧)

(3.248)

∑
∑
where 𝑖 = 1, 2, 3, 4. Since (𝑧) 2 = 4𝑗=1 𝑧 𝑗 𝑧 𝑗 , it follows that d(𝑧) 2 = 2 4𝑗=1 𝑧 𝑗 d𝑧 𝑗 .
Substituting this into (3.248) yields:
)
( 𝑗
∑
4
4
∑︁
2𝑧𝑖 4𝑗=1 𝑧 𝑗 d𝑧 𝑗 ∑︁
𝛿𝑖
d𝑧 𝑖
2𝑧 𝑖 𝑧 𝑗
𝑗
d𝑧˘𝑖 =
−
−
=
d𝑧
=:
𝜏𝑖 d𝑧 𝑗 , (3.249)
𝑗
( 2)2
( 2)2
2
(𝑧) 2
(𝑧)
(𝑧)
(𝑧)
𝑗=1
𝑗=1
where:
𝑗

𝑗
𝜏𝑖 :=

2𝑧 𝑖 𝑧 𝑗
−
(
)2 ,
(𝑧) 2
(𝑧) 2
𝛿𝑖

satisfying

4
∑︁

𝑗
𝑗
𝜏𝑘 𝜏𝑖𝑘 = (

𝛿𝑖
)2 .

(3.250)

(d𝑧) 2
)2 .
(𝑧) 2

(3.251)

𝑘=1

(𝑧) 2

Using the above, we compute the transformed line element:
(d𝑧˘) 2 =

4
∑︁

4
∑︁

d𝑧˘𝑖 d𝑧˘𝑖 =

𝑖=1

𝜏 𝑖𝑗 𝜏𝑖𝑘 d𝑧 𝑗 d𝑧 𝑘

𝑖, 𝑗,𝑘=1

= (

1
(𝑧)

∑︁

)
2 2

𝛿 𝑘𝑗 d𝑧 𝑗 d𝑧 𝑘 = (

𝑗,𝑘

(
)2
Thus, inversion rescales the metric by the Weyl factor 1/ (𝑧) 2 , confirming that
𝑧 ↦−→ 𝑧˘ is indeed a conformal transformation.
— Step II (application to the field operator). Under the inversion map (3.246),
a scalar primary field of conformal dimension E = 1 transforms as (see footnote
22):
ˆ
𝜙(𝑧)
Equivalently:

↦−→

ˆ 𝑧˘) = (𝑧) 2 𝜙(𝑧)
ˆ .
𝜙(

(3.252)

## PDF page 125

3.5 4-dimensional Conformal Vertex Algebra

111

1 ˆ
ˆ
𝜙(𝑧)
=
𝜙( 𝑧˘) .
(3.253)
(𝑧) 2
)∗
(
𝜙(𝑧) , we apply the above rule to the
To define the conjugated field operator ˆ
complex conjugated coordinate 𝑧 ↦−→ 𝑧˘ = 𝑧∗ = 𝑧/(𝑧) 2 , yielding (3.245):
)∗
(
1 ˆ ∗
𝜙(𝑧) .
𝜙(𝑧 ) =: ˆ
2
(𝑧)

(3.254)

This expression reflects both the geometric action of the conformal conjugation
map and the conformal transformation law of the scalar field, with the prefactor
accounting for the field’s conformal weight E = 1.
□
Using (3.244) and (3.245), one readily verifies that the vector-valued function
U(2,2)
ˆ
𝜙(𝑧)|0
⟩ has a finite positive norm squared for 𝑧 ∈ 𝔗 precompact
:
+
1
1
2
ˆ
𝜙(𝑧)|0U(2,2) ⟩ =
⟨0U(2,2) | ˆ
𝜙(𝑧∗ ) ˆ
𝜙(𝑧)|0U(2,2) ⟩ =
< ∞.
(𝑧) 2
1 − 2𝑧 · 𝑧 + (𝑧) 2 (𝑧) 2
(3.255)
Note that, for all 𝑧 ∈ 𝔗 precompact
, one has 2𝑧 · 𝑧 < 1 + (𝑧) 2 (𝑧) 2 (see Eq. (3.218)). The
+
quantity on the right-hand side of (3.255) coincides (up to normalization) with the
U(2, 2)-invariant Bergman reproducing kernel on 𝔗 precompact
.
+

3.5 4-dimensional Conformal Vertex Algebra
QFT is primarily concerned with the vacuum representation of products of quantum
fields. The algebra of globally conformally invariant fields — such as free massless
fields and their operator product expansions — fits naturally into the framework of
a 4-dimensional (or higher) vertex algebra, as developed in Ref. [114] and further
summarized in Section 4.3 of Ref. [115]. This formalism not only generalizes the
structure of field products beyond perturbation theory but also offers a more natural
and conceptually unified perspective than the explicit classification of individual
UPEIRs. We now proceed to outline its key features.
The states of the theory span a (pre-)Hilbert space23 H that carries a (reducible)
unitary representation 𝑈 of the conformal group U(2, 2), featuring a unique con23 A “pre-Hilbert space” is a complex vector space equipped with a positive-definite inner product,

but not necessarily complete with respect to the induced norm. Its completion yields a Hilbert
space. In many QFT settings — especially CFT — the natural space of states is first defined as a
dense subspace of a Hilbert space, typically consisting of finite-energy or polynomially bounded
states. This subspace suffices for algebraic constructions, such as operator products and the action
of symmetry generators, and is often referred to as a pre-Hilbert space. The completion is then
required to rigorously establish limits and convergence. Thus, the term “pre-Hilbert space” reflects
whether one is working directly with the dense, physically meaningful subspace or with its Hilbert
space completion, depending on the level of mathematical rigor required.

## PDF page 126

112

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

formally invariant vacuum state. This conformally invariant vacuum |0U(2,2) ⟩ is the
unique normalized lowest weight state in H that is invariant under the full conformal
group U(2, 2). Explicitly, the vacuum satisfies:
𝑈 (𝑔)|0U(2,2) ⟩ = |0U(2,2) ⟩ ,

𝑔 ∈ U(2, 2) .

for all

(3.256)

Proposition 3.7 — (spectral decomposition of the conformal Hamiltonian). Let
H be a (pre-)Hilbert space carrying a (possibly reducible) unitary positive-energy
representation of the conformal group U(2, 2), and let 𝐻 := i𝐽05 (3.190) (see also
(3.193)) denote the conformal Hamiltonian, which is essentially self-adjoint and
bounded from below. Then:
1. The spectrum of 𝐻 is purely discrete and non-negative:
}
{
Spec(𝐻) = E ∈ R ≥0 ; E = 0, 1, 23 , 2, . . . ,

(3.257)

where each eigenvalue E has finite multiplicity.
2. The space H decomposes into a direct sum of (finite-dimensional) eigenspaces
HE of the conformal Hamiltonian 𝐻:
⨁
H =
HE , such that (𝐻 − E )HE = 0 .
(3.258)
E ∈Spec(𝐻 )

3. The conformally invariant vacuum |0U(2,2) ⟩ spans the lowest-energy (1-dimensional)
eigenspace:
HE =0 = C |0U(2,2) ⟩ .

(3.259)

4. Each eigenspace HE is generally not invariant under the full conformal group
U(2, 2); rather, it is preserved only by the maximal compact subgroup Spin(4).
This can be seen as a consequence of Proposition 3.4, particularly as established
in Step III of its proof. More precisely, each HE carries a (generally reducible)
finite-dimensional representation of Spin(4)  SO(4). The central element −14 ∈
Spin(4) acts on states in HE by multiplication with their parity, given by:
(−1) 2(j𝐿 +j𝑅 ) = (−1) 2E ∈

{

}
− 1, +1 .

(3.260)

This identity follows directly from Remark 3.13.
In this construction,
the fields 𝜙ˆ of the theory
(
) are represented by infinite power
2
2
series in (𝑧) := (𝑧1 ) + (𝑧 2 ) 2 + (𝑧 3 ) 2 + (𝑧 4 ) 2 with harmonic polynomial coefficients:
∑︁ ∑︁ (
)𝑛
ˆ
𝜙(𝑧) =
(𝑧) 2 𝜙ˆ𝑛,𝑚 (𝑧) ,
(3.261)
𝑛∈Z 𝑚∈Z ≥0

such that:

## PDF page 127

3.5 4-dimensional Conformal Vertex Algebra

113

𝜙ˆ𝑛,𝑚 ( 𝜚𝑧) = 𝜚 𝑚 𝜙ˆ𝑛,𝑚 (𝑧) ,
Δ𝜙ˆ𝑛,𝑚 (𝑧) :=

for

𝜚 > 0,

4
∑︁

𝜕2 ˆ
𝜙 𝑛,𝑚 (𝑧) = 0 .
𝜕𝑧2𝑖
𝑖=1

(3.262)
(3.263)

Restricting attention to quantum fields 𝜙ˆ and 𝜓ˆ of definite parity, we assign to
each field a parity degree P 𝜙ˆ , P 𝜓ˆ ∈ {0, 1}, defined by:
𝜙(𝑧)|0U(2,2) ⟩
𝜙(𝑧)|0U(2,2) ⟩ := (−1) 2𝐻 ˆ
(−1) P ˆ
U(2,2)
ˆ
= (−1) 2E 𝜙(𝑧)|0
⟩
U(2,2)
ˆ
= ± 𝜙(𝑧)|0
⟩.

(3.264)

This reflects the field’s transformation under the central element −14 ∈ Spin(4).
The sign ‘±’ determines the intrinsic parity of the field; even-parity (bosonic) fields
correspond to P = 0, and odd-parity (fermionic) fields to P = 1. As discussed
below, this assignment endows the fields with a Z2 grading that enters the strong
(Huygens) locality condition, governing whether fields commute or anticommute in
the graded operator algebra.
The strong (Huygens) locality condition assumes:24
(

(𝑧 − 𝑢) 2

)𝑁 (

)
ˆ
ˆ
ˆ 𝜓(𝑢)
ˆ
𝜙(𝑧)
= 0,
𝜙(𝑧)
− (−1) P 𝜙ˆ P 𝜓ˆ 𝜓(𝑢)

(3.265)

(
)𝑁
for some sufficiently large integer 𝑁. The prefactor (𝑧 − 𝑢) 2
ensures that the
expression vanishes in the coincident limit 𝑧 → 𝑢 and encodes the allowed singularity
structure in the operator product expansion. For a concrete example of this singular
behavior, see Eq. (3.244).
Proposition 3.8 The strong (or Huygens) locality condition (3.265), valid for some
sufficiently large integer 𝑁, reflects the fact that any pair of mutually nonisotropic
(non-null) points (𝑧, 𝑢) — that is, with (𝑧 − 𝑢) 2 ≠ 0 — belongs to a single orbit of the
conformal group SU(2, 2) acting on compactified Minkowski space. In this global
setting, the invariant notion is not spacelike versus timelike separation, but rather
the null/non-null distinction.
Before turning to the proof, let us clarify the conceptual role of this condition. In flat Minkowski spacetime, strong (Huygens) locality is nothing more than
the operator-algebraic expression of microcausality; fields either commute or anticommute when evaluated at spacelike separated arguments. This interpretation is
24 In the strong (Huygens) locality condition, the parity degrees determine the exchange symmetry:

1. If both fields are bosonic (P 𝜙ˆ = P 𝜓ˆ = 0): (−1) 0×0 = +1, then the fields commute.
2. If both fields are fermionic (P 𝜙ˆ = P 𝜓ˆ = 1): (−1) 1×1 = −1, then the fields anticommute.
3. If one field is bosonic and the other fermionic (P 𝜙ˆ = 0, P 𝜓ˆ = 1 or vice versa): (−1) 0×1 =
(−1) 1×0 = +1, then the fields commute.

## PDF page 128

114

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

unambiguous, since the local conformal group preserves the causal type of separation vectors, and hence the distinction between spacelike and timelike pairs is sharp
(see the proof below).
After conformal compactification, however, the situation changes essentially. The
global conformal group SU(2, 2) preserves null separations exactly, but no longer
preserves the spacelike/timelike distinction; under compactified conformal transformations, a spacelike pair may be mapped to a timelike one (see the proof below).
What remains invariant is therefore only the null versus non-null classification. In
this global setting, the strong locality condition must be reinterpreted: it is not “locality” in the conventional causal sense, but rather a conformally covariant regularity
requirement on operator products. Concretely, it guarantees that graded commutators vanish (up to their prescribed short-distance singularities) throughout the full
conformal orbit of non-null pairs under SU(2, 2).
When restricted back to the Minkowski patch, this broader condition reduces
precisely to the familiar microcausality principle, thereby reconciling the local and
global viewpoints.
Proof A rigorous proof of this proposition can be found in Ref. [114]. Here, however,
we outline an alternative approach that serves certain illustrative or pedagogical
purposes.
— Step I (transitive action of the conformal group on non-null point pairs
in Minkowski spacetime). Let 𝑀  R3,1 denote flat Minkowski spacetime, whose
conformal group is locally isomorphic to SU(2, 2). This group acts transitively on
the set of ordered point pairs (𝑥, 𝑦) ∈ R3,1 × R3,1 with (𝑥 − 𝑦) 2 ≠ 0, provided the
causal type of the separation vector is fixed (spacelike or timelike). We elaborate on
this point below.
Let (𝑥, 𝑦) and (𝑥 ′ , 𝑦 ′ ) be two such pairs with (𝑥 − 𝑦) 2 ≠ 0 ≠ (𝑥 ′ − 𝑦 ′ ) 2 , and
with the same causal type. We construct a conformal transformation 𝑔˜ 𝑐 mapping
𝑥 ↦−→ 𝑥 ′ and 𝑦 ↦−→ 𝑦 ′ . Since the conformal group includes translations, Lorentz
transformations, dilations, and special conformal transformations, we can actually
realize such a conformal transformation as a composition of elementary operations;
specifically:
1. Translate 𝑥 to the origin by 𝑇𝑥 ( 𝐴) = 𝐴 − 𝑥, which maps the original pair (𝑥, 𝑦) to
(0, 𝑟), where 𝑟 = 𝑦 − 𝑥. Note( that,)as assumed in the proposition, 𝑟 ≠ 0.
2. Similarly, define 𝑟 ′ = 𝑦 ′ − 𝑥 ′ ≠ 0 , so that the target pair (𝑥 ′ , 𝑦 ′ ) becomes (0, 𝑟 ′ )
after translation by 𝑥 ′ .
√︂
3. Apply a dilation 𝐷 𝜚 ( 𝐴) = 𝜚 𝐴 with scale factor 𝜚 =

(𝑟 ′ ) 2
(𝑟 ) 2

> 0. Then, the

rescaled vector 𝜚𝑟 has the same invariant length as 𝑟 ′ .
4. Since 𝑟 and 𝑟 ′ are both non-null and of the same causal type, there exists a Lorentz
transformation Λ ∈ SO(3, 1) such that Λ( 𝜚𝑟) = 𝑟 ′ ; recall that the Lorentz group
SO(3, 1) preserves the Minkowski norm and causal character.
′
5. Undo the translation of the target pair by applying 𝑇𝑥−1
′ ( 𝐴) = 𝐴 + 𝑥 .
Then, the complete transformation, which maps spacelike (respectively timelike)
pairs to spacelike (respectively timelike) pairs, is:

## PDF page 129

3.5 4-dimensional Conformal Vertex Algebra

115

(
)
′
𝑔˜ 𝑐 ( 𝐴) = 𝑇𝑥−1
′ ◦ Λ ◦ 𝐷 𝜚 ◦ 𝑇𝑥 ( 𝐴) = Λ 𝜚( 𝐴 − 𝑥) + 𝑥 ,

(3.266)

satisfying:
𝑔˜ 𝑐 (𝑥) = 𝑥 ′ ,

𝑔˜ 𝑐 (𝑦) = 𝑦 ′ .

(3.267)

— Step II (extension to compactified
Minkowski space). We now invoke the
( )
conformal compactification, 𝑔𝑐 𝑀 = 𝑀 compact , where the globally defined map 𝑔𝑐 is
specified in Eq. (3.211), with its inverse given in Eq. (3.239). Let:
𝑧 = 𝑔𝑐 (𝑥) ,

𝑧 ′ = 𝑔𝑐 (𝑥 ′ ) ,

𝑢 = 𝑔𝑐 (𝑦) ,

𝑢 ′ = 𝑔𝑐 (𝑦 ′ ) .

(3.268)

Under the globally defined map 𝑔𝑐 (3.211) (or similarly its reverse (3.239)), the
squared interval transforms according to (3.214):
(𝑧 − 𝑢) 2 =

(𝑥 − 𝑦) 2
,
Ω(𝑥) Ω(𝑦)

(3.269)

where the Weyl factors Ω(𝑥) and Ω(𝑦) are generally complex (not strictly positive!).
Consequently, unlike the local map 𝑔˜ 𝑐 introduced above, the global transformation
𝑔𝑐 does not preserve the causal type of a pair of points; it preserves only the non-null
separation:
(𝑥 − 𝑦) 2 ≠ 0

⇐⇒

(𝑧 − 𝑢) 2 ≠ 0 .

(3.270)

Nevertheless, even though the global map 𝑔𝑐 does not preserve the spacelike or
timelike character of vectors, the conformal group still acts transitively on the set of
mutually non-isotropic (non-null) point pairs in 𝑀 compact :
(𝑧, 𝑢)
⏟⏞⏞⏟

𝑔𝑐−1 (3.239)

↦−→

(𝑥, 𝑦)

𝑔˜ 𝑐

↦−→

(𝑥 ′ , 𝑦 ′ )

𝑔𝑐 (3.211)

↦−→

(𝑧 ′ , 𝑢 ′ ) . (3.271)
⏟ ⏞⏞ ⏟
(𝑧 ′ −𝑢′ ) 2 ≠ 0

(𝑧−𝑢) 2 ≠ 0

— Step III (conclusion/implications for strong locality). The strong locality
condition (3.265) reflects the conformal orbit structure in the following sense. For
fields ˆ
𝜙(𝑧) and ˆ
𝜓(𝑢), the graded (anti-)commutator:
)
(
ˆ
𝜓(𝑢) ˆ
𝜙(𝑧)
(3.272)
𝜙(𝑧) ˆ
𝜓(𝑢) − (−1) P 𝜙ˆ P 𝜓ˆ ˆ
is not identically zero for general configurations, but the condition:
(

(𝑧 − 𝑢) 2

)𝑁 (

)
... = 0

(3.273)

is required to be smooth and covariant under SU(2, 2) on the domain where (𝑧−𝑢) 2 ≠
(
)𝑁
0. The prefactor (𝑧 − 𝑢) 2 therefore plays two complementary roles:

## PDF page 130

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

116

1. Regularization of singularities: It removes the divergences that occur in the
coincidence limit 𝑧 → 𝑢, ensuring a well-defined operator product expansion.
2. Uniformity across the conformal orbit: Because all non-null pairs (𝑧, 𝑢) belong
to a single conformal orbit, the prefactor guarantees that the (anti-)commutator
vanishes consistently on the entire orbit, enforcing compatibility with the global
conformal symmetry.
Thus, the strong locality condition encodes a fundamental geometric and algebraic
feature of CFT: it manifests conformal invariance at the level of the operator algebra,
imposing global constraints on field (anti-)commutators in accordance with the orbit
structure of compactified Minkowski space. When restricted to the Minkowski patch,
this condition reduces to the familiar microcausality principle, ensuring that fields
commute or anticommute at spacelike separation.
□
Proposition 3.9 The essence of the theory of conformal vertex algebra is contained
in the following statements [115]:
1. The expansion ˆ
𝜙(𝑧)|0U(2,2) ⟩ contains no negative powers of (𝑧) 2 . That is, any
term in the field ˆ
𝜙(𝑧) (see Eq. (3.261)) involving negative powers of (𝑧) 2 — and
hence singular at the origin — must annihilate the conformally invariant vacuum
|0U(2,2) ⟩.
2. Every local component 𝜙ˆ𝑖 (𝑧) is uniquely determined by the vector |𝑣𝑖 ⟩, defined
as:
|𝑣𝑖 ⟩ := 𝜙ˆ𝑖 (0) |0U(2,2) ⟩ ,

such that

(−1) P 𝜙ˆ |𝑣𝑖 ⟩ = (−1) 2𝐻 |𝑣𝑖 ⟩ .

(3.274)

ˆ
3. If |𝑣⟩ := 𝜙(0)
|0U(2,2) ⟩ is an eigenstate of the conformal Hamiltonian 𝐻 with
eigenvalue E , i.e., (𝐻 − E ) |𝑣⟩ = 0, then E is identified with the scaling dimension
ˆ In the case of free (massless) fields, E coincides with the canonical
of the field 𝜙.
dimension of the field: E = 1 for a massless scalar field (see footnote 14 and
22); E = 23 for a Weyl spinor field with helicity 𝜆 = ± 12 ; more generally, E
increases with spin, following the free-field scaling dimension. Conversely, a field
with E = 12 would represent a subcanonical scaling dimension, incompatible with
unitarity and in violation of Wightman’s Hilbert space positivity condition.
ˆ
4. If |𝑣⟩ := 𝜙(0)
|0U(2,2) ⟩ is the lowest-energy state within an irreducible subrepresentation of the conformal group (i.e., a lowest weight state), then it is annihilated by all special conformal generators 𝐶𝑖 |𝑣⟩ = 0 (see Proposition 3.4). Such
states are referred to as quasiprimary in Ref. [115], adopting terminology from
2-dimensional CFT, where the notion originates.
U(2,2)
ˆ
5. For every vector
|𝑣⟩
⟩ (of definite parity P), there exists a unique
(
) := 𝜙(0) |0
local field Y |𝑣⟩, 𝑧 (of parity P), such that:
(
)
(
)
Y |𝑣⟩, 𝑧 |0U(2,2) ⟩ = 𝑒 𝑧·𝑇 |𝑣⟩ =⇒ Y |𝑣⟩, 𝑧 = 0 |0U(2,2) ⟩ = |𝑣⟩ ,
(3.275)
where 𝑧 ·𝑇 :=

∑4

(

𝑖
𝑖=1 𝑧 𝑇𝑖 , and Y |𝑣⟩, 𝑧

)

obeys the conformal covariance conditions:

[
(
)]
(
)
𝑇𝑖 , Y |𝑣⟩, 𝑧 = 𝑇𝑖(𝑧) Y |𝑣⟩, 𝑧 ,

(3.276)

## PDF page 131

3.5 4-dimensional Conformal Vertex Algebra

[

117

(
)]
(
)
(
)
𝐶𝑖 , Y |𝑣⟩, 𝑧 = − 𝐶𝑖(𝑧) Y |𝑣⟩, 𝑧 − 2𝑧 𝑖 Y 𝐻|𝑣⟩, 𝑧
(
)
(
)
+ 2𝑧 𝑗 Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + Y 𝐶𝑖 |𝑣⟩, 𝑧 ,

(3.277)

(
)]
(
)
(
)
𝐻, Y |𝑣⟩, 𝑧 = −𝐻 (𝑧) Y |𝑣⟩, 𝑧 + Y 𝐻|𝑣⟩, 𝑧 ,

(3.278)

(
)]
(
)
(
)
𝐽𝑖 𝑗 , Y |𝑣⟩, 𝑧 = 𝐽𝑖(𝑧)
𝑗 Y |𝑣⟩, 𝑧 + Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 ,

(3.279)

[

[

where 𝑇𝑖(𝑧) = 𝜕𝑖 := 𝜕𝑧𝜕 𝑖 , 𝐶𝑖(𝑧) = −(𝑧) 2 𝜕𝑖 + 2𝑧 𝑖 (𝑧 · 𝜕), 𝐻 (𝑧) = −𝑧 · 𝜕, and
𝐽𝑖(𝑧)
𝑗 = 𝑧 𝑖 𝜕 𝑗 −𝑧 𝑗 𝜕𝑖 are the conformal Lie algebra generators realized as differential
operators acting on compactified Minkowski space 𝑀 compact  (S3 ×S1 )/Z2  U(2)
(see Appendix 3.9).
Proof (consistency check — not a formal proof)
U(2,2)
ˆ
— Step I (the absence of negative
⟩). The absence of nega( powers
) U(2,2)in 𝜙(𝑧) |0
U(2,2)
tive powers in ˆ
𝜙(𝑧) |0
⟩ = Y |𝑣⟩, 𝑧 |0
⟩ can be directly understood from its
behavior under the action (3.278) of the conformal Hamiltonian 𝐻:
[
(
)]
(
(
))
(
)
𝐻, Y |𝑣⟩, 𝑧 |0U(2,2) ⟩ = 𝑧 · 𝜕Y |𝑣⟩, 𝑧 |0U(2,2) ⟩ + Y 𝐻|𝑣⟩, 𝑧 |0U(2,2) ⟩
(
)
= (2𝑛 + 𝑚 + E ) Y |𝑣⟩, 𝑧 |0U(2,2) ⟩ ,
(3.280)
⏟
⏞⏞
⏟
=: E𝑛,𝑚

(
)
ˆ
where (2𝑛 + 𝑚) denotes the total homogeneity degree of Y |𝑣⟩, 𝑧 = 𝜙(𝑧)
(see the
expansion (3.261)) and E is the eigenvalue of 𝐻 on |𝑣⟩ (i.e., the conformal energy
of the state).
If we now assume that |𝑣⟩ is a lowest weight state, i.e., it is annihilated by all
special conformal generators 𝐶𝑖 , then E = E◦ is the minimal eigenvalue of 𝐻. For
such states, and for sufficiently small 𝑚 (in particular for 𝑚 = 0), terms with 𝑛 < 0
would imply the existence of states with energy below E = E◦ , contradicting the
unitarity requirement of energy bounded below. Thus, to avoid producing lowerenergy states, any term with 𝑛 < 0 must annihilate the vacuum; that is:
( 2) 𝑛
(𝑧) 𝜙ˆ𝑛,𝑚 (𝑧) |0U(2,2) ⟩ = 0 , for all 𝑛 < 0 .
(3.281)
— Step II (verification of conformal covariance). We now examine whether the
vertex operators introduced in Eqs. (3.276)-(3.279) are consistent with the canonical
commutation relation of the conformal Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) (see Eqs.
(3.192)-(3.195)):

## PDF page 132

118

[[

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

] (
)] [ [
(
)]] [ [
(
)]]
𝐻, 𝑇𝑖 , Y |𝑣⟩, 𝑧 = 𝐻, 𝑇𝑖 , Y |𝑣⟩, 𝑧
− 𝑇𝑖 , 𝐻, Y |𝑣⟩, 𝑧
[
(
)] [
(
)
(
)]
= 𝐻, 𝑇𝑖(𝑧) Y |𝑣⟩, 𝑧 − 𝑇𝑖 , −𝐻 (𝑧) Y |𝑣⟩, 𝑧 + Y 𝐻|𝑣⟩, 𝑧
[
[
(
)]
(
)] [
(
)]
= 𝑇𝑖(𝑧) 𝐻 , Y |𝑣⟩, 𝑧 + 𝐻 (𝑧) 𝑇𝑖 , Y |𝑣⟩, 𝑧 − 𝑇𝑖 , Y 𝐻|𝑣⟩, 𝑧
(
(
)
(
))
= 𝑇𝑖(𝑧) − 𝐻 (𝑧) Y |𝑣⟩, 𝑧 + Y 𝐻|𝑣⟩, 𝑧
(
)
(
)
+ 𝐻 (𝑧) 𝑇𝑖(𝑧) Y |𝑣⟩, 𝑧 − 𝑇𝑖(𝑧) Y 𝐻|𝑣⟩, 𝑧
[
] (
)
= 𝐻 (𝑧) , 𝑇𝑖(𝑧) Y |𝑣⟩, 𝑧
(
)
= 𝑇𝑖(𝑧) Y |𝑣⟩, 𝑧
[
(
)]
= 𝑇𝑖 , Y |𝑣⟩, 𝑧 .
(3.282)

To derive this relation, we have used the Jacobi identity:
[
] [
] [
]
[ 𝐴, 𝐵], 𝐶 = 𝐴, [𝐵, 𝐶] − 𝐵, [ 𝐴, 𝐶] .
Proceeding along the same path, we obtain:

(3.283)

## PDF page 133

3.6 Appendix: Upper Bound on 𝔰𝔲 (2) Spins from the 𝔰𝔬 (4) Casimir

[[

119

] (
[
)] [ [
(
)]] [
(
)]]
𝐻, 𝐶𝑖 , Y |𝑣⟩, 𝑧 = 𝐻, 𝐶𝑖 , Y |𝑣⟩, 𝑧
− 𝐶𝑖 , 𝐻, Y |𝑣⟩, 𝑧
[
(
)
(
)
= 𝐻, −𝐶𝑖(𝑧) Y |𝑣⟩, 𝑧 − 2𝑧 𝑖 Y 𝐻|𝑣⟩, 𝑧
(
)
(
)]
+ 2𝑧 𝑗 Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + Y 𝐶𝑖 |𝑣⟩, 𝑧
[
(
)
(
)]
− 𝐶𝑖 , −𝐻 (𝑧) Y |𝑣⟩, 𝑧 + Y 𝐻|𝑣⟩, 𝑧
[
[
(
)]
(
)]
= −𝐶𝑖(𝑧) 𝐻, Y |𝑣⟩, 𝑧 − 2𝑧 𝑖 𝐻, Y 𝐻|𝑣⟩, 𝑧
[
(
)] [
(
)]
+ 2𝑧 𝑗 𝐻, Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + 𝐻, Y 𝐶𝑖 |𝑣⟩, 𝑧
[
(
)] [
(
)]
+ 𝐻 (𝑧) 𝐶𝑖 , Y |𝑣⟩, 𝑧 − 𝐶𝑖 , Y 𝐻|𝑣⟩, 𝑧
(
(
)
(
))
= −𝐶𝑖(𝑧) − 𝐻 (𝑧) Y |𝑣⟩, 𝑧 + Y 𝐻|𝑣⟩, 𝑧
(
(
)
(
))
− 2𝑧 𝑖 − 𝐻 (𝑧) Y 𝐻|𝑣⟩, 𝑧 + Y 𝐻 2 |𝑣⟩, 𝑧
(
(
)
(
))
+ 2𝑧 𝑗 − 𝐻 (𝑧) Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + Y 𝐻𝐽𝑖 𝑗 |𝑣⟩, 𝑧
(
(
)
(
))
+ − 𝐻 (𝑧) Y 𝐶𝑖 |𝑣⟩, 𝑧 + Y 𝐻𝐶𝑖 |𝑣⟩, 𝑧
(
(
)
(
)
+ 𝐻 (𝑧) − 𝐶𝑖(𝑧) Y |𝑣⟩, 𝑧 − 2𝑧 𝑖 Y 𝐻|𝑣⟩, 𝑧
(
)
(
))
+ 2𝑧 𝑗 Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + Y 𝐶𝑖 |𝑣⟩, 𝑧
(
(
)
(
)
− − 𝐶𝑖(𝑧) Y 𝐻|𝑣⟩, 𝑧 − 2𝑧 𝑖 Y 𝐻 2 |𝑣⟩, 𝑧
(
)
(
))
+ 2𝑧 𝑗 Y 𝐽𝑖 𝑗 𝐻|𝑣⟩, 𝑧 + Y 𝐶𝑖 𝐻|𝑣⟩, 𝑧
] (
] (
[
) [
)
= 𝐶𝑖(𝑧) , 𝐻 (𝑧) Y |𝑣⟩, 𝑧 + 2𝑧𝑖 , 𝐻 (𝑧) Y 𝐻|𝑣⟩, 𝑧
[
] (
)
(
)
− 2𝑧 𝑗 , 𝐻 (𝑧) Y 𝐽𝑖 𝑗 |𝑣⟩, 𝑧 + Y [𝐻, 𝐶𝑖 ] |𝑣⟩, 𝑧
[
(
)]
= − 𝐶𝑖 , Y |𝑣⟩, 𝑧 ,
(3.284)

and similarly, one also verifies that:
[
[[
] (
[
)]
(
)]
(
)]
𝐶𝑖 , 𝑇 𝑗 , Y |𝑣⟩, 𝑧 = 2𝛿𝑖 𝑗 𝐻, Y |𝑣⟩, 𝑧 − 2 𝐽𝑖 𝑗 , Y |𝑣⟩, 𝑧 .

(3.285)
□

3.6 Appendix: Upper Bound on 𝖘𝖚(2) Spins from the 𝖘𝖔(4)
Casimir
Proposition 3.10 Let C2𝔰𝔬 (4) be the quadratic Casimir of 𝔰𝔬(4)  𝔰𝔲(2) 𝐿 ⊕ 𝔰𝔲(2) 𝑅 :
C2𝔰𝔬 (4) = j 𝐿 (j 𝐿 + 1) + j𝑅 (j𝑅 + 1) ,

j𝐿 , j𝑅 ∈

1
Z ≥0 .
2

(3.286)

## PDF page 134

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

120

Assume:
C2𝔰𝔬 (4) =

)
1( 2
E + 𝜆2 − 1 ,
2

(
)
E = |𝜆| + 𝑛 ≥ 1 ,

𝜆∈

1
Z,
2

and

𝑛 ∈ Z>0 .
(3.287)

Then, we have:
j𝐿 , j𝑅 ≤ E − 1 .

(3.288)

Proof Using j𝑅 (j𝑅 + 1) ≥ 0, we have:
j 𝐿 (j 𝐿 + 1) ≤

1 2
(E + 𝜆2 − 1)
2

=⇒

j𝐿 ≤

√
−1 + 2E 2 + 2𝜆2 − 1
.
2

(3.289)

Since E ≥ 1, one checks:
√
−1 + 2E 2 + 2𝜆2 − 1
≤ E − 1,
(3.290)
2
(
)
because squaring gives the identity 0 ≤ 2 (E − 1) 2 − 𝜆2 . The same argument holds
for j𝑅 .
□

3.7 Appendix: de Sitter (dS) Massless Unitary Irreducible
Representations (UIRs)
We begin again with the conformal Lie algebra 𝔰𝔲(2, 2)  𝔰𝔬(4, 2) and its “second˜ 𝛾 𝜇𝜈 𝜑), with 𝜇, 𝜈 = 0, 1, 2, 3, 4, 5 (see Eq.
quantized” ladder generators 𝐽 𝜇𝜈 = 12 ( 𝜑

## PDF page 135

3.7 Appendix: de Sitter (dS) Massless Unitary Irreducible Representations (UIRs)

121

(3.34)). In this context, one may obtain the dS algebra by restricting attention to the
generators 𝐽 𝛼𝛽 , with 𝛼, 𝛽 = 0, 1, 2, 3, 4, and discarding the generators 𝐽 𝛼5 ; this yields
a 10-dimensional subalgebra isomorphic to 𝔰𝔭(2, 2)  𝔰𝔬(4, 1). In particular, the
conformal Hamiltonian 𝐻 = i𝐽05 does not belong to the dS subalgebra and therefore
cannot serve as a global energy operator or as an energy label E for dS UIRs; dS
representations are not classified by a global energy eigenvalue in the same way as
anti-dS representations (see Ref. [29]).
The maximal compact subalgebra of the dS algebra is 𝔰𝔬(4)  𝔰𝔲(2) 𝐿 ⊕ 𝔰𝔲(2) 𝑅 ,
generated by 𝐽𝑖 𝑗 with 𝑖, 𝑗 = 1, 2, 3, 4. Every state in a dS UIR can be labeled by
the compact quantum numbers (j 𝐿 , j𝑅 ), where again j 𝐿 and j𝑅 are the familiar
SU(2) spins associated with the left and right SU(2) factors [93]. We now proceed
to elaborate on the structure and interpretation of these labels.
A multiplet will denote the collection of states |j 𝐿 , j𝑅 ; 𝑚 𝐿 , 𝑚 𝑅 ⟩ transforming
irreducibly under 𝑆U(2) 𝐿 × 𝑆U(2) 𝑅 with fixed (j 𝐿 , j𝑅 ), where 𝑚 𝐿 = −j 𝐿 , . . . , j 𝐿
and 𝑚 𝑅 = −j𝑅 , . . . , j𝑅 label the magnetic quantum numbers. The dimension d of
such a multiplet is (2j 𝐿 + 1) (2j𝑅 + 1) (see Eq. (3.150)). The compact generators 𝐽𝑖 𝑗
act within each multiplet, mixing the magnetic quantum numbers while preserving
the total spins (j 𝐿 , j𝑅 ).
The remaining generators 𝐽0𝑖 (with 𝑖 = 1, . . . , 4), which span the noncompact
directions of 𝔰𝔬(4, 1), act between multiplets. Their commutation relations with the
compact generators are:
[
] (
)
𝐽𝑖 𝑗 , 𝐽0𝑘 = 𝜂 𝑗 𝑘 𝐽0𝑖 − 𝜂𝑖𝑘 𝐽0 𝑗 ,
(3.291)
which shows that the operators 𝐽0𝑖 transform in the vector (4-dimensional) representation of the compact group SO(4). Under the homomorphism SO(4)

)
(
SU(2) 𝐿 × SU(2) 𝑅 , this 4-vector corresponds to the bi-spinor representation 12 , 12 ,
(1 1)
with dimension d 2 , 2 = (1 + 1) (1 + 1) = 4.
When 𝐽0𝑖 acts on a compact multiplet (j 𝐿 , j𝑅 ) it therefore produces states in the
tensor product:
(
)
(
) (
)
(j 𝐿 , j𝑅 ) ⊗ 12 , 12 = j 𝐿 + 12 , j𝑅 + 12 ⊕ j 𝐿 + 12 , j𝑅 − 12
(
) (
)
⊕ j 𝐿 − 12 , j𝑅 + 12 ⊕ j 𝐿 − 12 , j𝑅 − 12 ,
(3.292)
with the obvious convention that any term with a negative spin is omitted. Thus, the
noncompact generators connect up to four neighboring SO(4) multiplets; repeated
application of the noncompact generators builds a “tower of multiplets” which,
together with the action of the compact algebra, spans the full UIR Hilbert space.
Remark 3.18 The foregoing “tower of SO(4) multiplets” picture is the natural description for the dS discrete-series type representations (those admitting lowest or
highest weight with respect to the compact subalgebra). For the dS principal-series
and complementary-series representations, the structure is different (continuous labels arise and the decomposition into compact multiplets must be handled with the
appropriate spectral-theoretic tools), so the seed-multiplet construction should be
understood in the appropriate representational context.
□

## PDF page 136

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

122

In summary, a dS UIR decomposes into a (generally countable) collection of
SO(4) multiplets (j 𝐿 , j𝑅 ). The compact generators 𝐽𝑖 𝑗 act within each multiplet,
whereas the noncompact generators
) 𝐽0𝑖 link multiplets according to the Clebsch(
Gordan decomposition with 21 , 12 ; there is no analogue of a globally conserved
energy label as in anti-dS space.
For the dS massless UIRs, the structure simplifies. As a direct consequence of the
preceding discussion, the full Hilbert space is generated from a chiral seed multiplet:
(j 𝐿 , j𝑅 ) = (𝑠, 0)

or

(0, 𝑠) ,

with

𝑠 := |𝜆| = 0, 21 , 1, . . . ,

(3.293)

where the helicity is encoded in the chirality of the seed multiplet (see Remark 3.10):
(𝑠, 0)

−→

(helicity + 𝑠) ,

(0, 𝑠)

−→

(helicity − 𝑠) .

(3.294)

In Dixmier’s notation [93], the corresponding massless dS representations are
written as:
+
Π𝑠,𝑠

−
Π𝑠,𝑠
,

and

(3.295)

respectively. Here, the general Dixmier labels Π ±𝑝,𝑞 may be read off from the SO(4)content of the representation; one convenient characterization is:
𝑝 :=

inf

(j 𝐿 ,j 𝑅 ) ∈spec

j𝐿 − j𝑅 ,

𝑞 :=

sup

j𝐿 + j𝑅 ,

(3.296)

(j 𝐿 ,j 𝑅 ) ∈spec

where the infimum and supremum are taken over the set of compact multiplets
(j 𝐿 , j𝑅 ) occurring in the UIR. [Equivalently, the parameters 𝑝 and 𝑞 can be extracted
from the eigenvalues of the dS quadratic and quartic Casimir operators; see the
discussions in Sect. 1.3.] For the massless case generated by a chiral seed (𝑠, 0) or
± ; the superscript ‘±’
(0, 𝑠), one indeed has 𝑝 = 𝑞 = 𝑠, whence the notation Π𝑠,𝑠
records the helicity sign (chirality) of the seed multiplet.

3.8 Appendix: Compactified Minkowski Space as a Shilov
Boundary
The conformal compactification of 4-dimensional Minkowski space:
𝑀 compact 

S3 × S 1
Z2

(3.297)

(with the 3-sphere factor being the familiar compact space sometimes noted for its
exceptional rigidity in higher-dimensional calibrated geometry — see the classical
real S3 ⊂ S7 problem about minimal associative 3-spheres in the 7-sphere [116]) admits a natural interpretation as the Shilov boundary of a classical bounded symmetric
domain associated with the conformal group [117, 118, 119].

## PDF page 137

3.9 Appendix: The Lie Algebra 𝔰𝔬 (4, 2) and its Euclidean 𝔰𝔬 (5, 1) Counterpart; the 𝑧-Picture of the 𝔰𝔬 (4, 2) Generators
123

Indeed, the conformal group SO(4, 2) is locally isomorphic to SU(2, 2), and there
are two equivalent realizations of the corresponding Hermitian symmetric space. On
the one hand, SU(2, 2) acts transitively on the Cartan domain of type I:
𝐷 I2,2 =

SU(2, 2)
),
S U(2) × U(2)
(

(3.298)

whose Shilov boundary is canonically identified with U(2). Using the standard
topological identification:
U(2) 

S3 × S1
,
Z2

(3.299)

one recovers 𝑀 compact as this Shilov boundary.
On the other hand, via the isomorphism SU(2, 2) ≃ SO(4, 2), the same symmetric
space can be realized as the Cartan domain of type IV (the Lie ball):
𝐷 IV
4 = (

SO(4, 2)
),
SO(2) × SO(4)

(3.300)

whose Shilov boundary is the projectivized null cone in R4,2 . This boundary is
precisely the conformal compactification of Minkowski space.
Thus, depending on the chosen realization, 𝑀 compact appears either as:
1. The Shilov boundary of the type-I domain 𝐷 I2,2 , or equivalently
2. The Shilov boundary of the type-IV domain 𝐷 IV
4 .
Both descriptions are canonically equivalent and reflect the dual realizations of the
conformal symmetric space associated with SO(4, 2).

3.9 Appendix: The Lie Algebra 𝖘𝖔(4, 2) and its Euclidean
𝖘𝖔(5, 1) Counterpart; the 𝒛-Picture of the 𝖘𝖔(4, 2) Generators
In the context of the present study, it is natural to introduce the 𝑧-picture realization of
the conformal generators acting on compactified Minkowski space 𝑀 compact  (S3 ×
S1 )/Z2  U(2). Specifically, we consider the infinitesimal translation generators
𝑇𝑖 (3.188), the special conformal transformations 𝐶𝑖 (3.189), and the conformal
Hamiltonian 𝐻 (3.190) (see also (3.193)), as realized via differential operators in
the complex coordinate variables 𝑧𝑖 = 𝑧𝑖 ∈ 𝑀 compact , with 𝑖 = 1, 2, 3, 4, introduced in
Eqs. (3.204)-(3.211).
To achieve this goal, we consider functions defined on Dirac’s projective quadric
P𝑄, which arises by projectivizing P the null cone 𝑄 (3.202) in R4,2 :

P𝑄 := 𝑄/R>0 ,

(3.301)

## PDF page 138

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

124

with:
{
}
𝑄 := 𝜁 ∈ R4,2 \ 0 ; (𝜁) 2 := 𝜂 𝜇𝜈 𝜁 𝜇 𝜁 𝜈 = 0 = Eq. (3.202) ,

(3.302)

where 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4 and the ambient metric 𝜂 𝜇𝜈 on R4,2 has signature
(−, −, +, +, +, +).
Some fundamental properties of Dirac’s projective quadric P𝑄 and related structures are as follows:
1. Null directions in R4,2 : P𝑄 consists of all null directions (rays) through the
origin in R4,2 . Concretely, two nonzero null vectors 𝜁 and 𝜁 ′ are considered
equivalent if they differ by a positive scalar:
𝜁 ∼ 𝜚𝜁 ,

𝜚 ∈ R>0 .

where

(3.303)

Each equivalence class corresponds to a single point on the projectivized light
cone, capturing the direction of the vector while ignoring its length.
2. Topology and conformal compactification: The resulting space P𝑄 is a compact, 4-dimensional manifold. Topologically, it is homeomorphic to (S3 ×S1 )/Z2 .
This identification arises from the null condition 𝜁 2 = 0, which imposes that
the spatial components (𝜁1 , . . . , 𝜁4 ) and the temporal components (𝜁0 , 𝜁5 ) lie
on spheres of equal radius — that is, 𝜁12 + · · · + 𝜁42 = 𝜁02 + 𝜁52 — thus defining
S3 and S1 , respectively. The Z2 quotient reflects the projectivization of null directions, identifying antipodal points along each ray via 𝜁 ∼ −𝜁. Consequently,
P𝑄 serves as the conformal compactification of Minkowski spacetime:

P𝑄



(S3 × S1 )/Z2
⏟ ⏞⏞ ⏟



𝑀 compact .

(3.304)

 U(2)

3. Embedding of Minkowski space: To complete the foregoing, Minkowski spacetime 𝑀  R3,1 can be embedded in P𝑄 in terms of the (dimensionless, homogeneous) coordinates as follows:
𝑥 𝜇¤ =

𝜁 𝜇¤
,
𝜁5 + 𝜁4

=⇒

𝜇¤ = 0, 1, 2, 3

(𝑥) 2 := 𝑥 𝜇¤ 𝑥 𝜇¤ = (

𝜁 𝜇¤ 𝜁 𝜇¤
𝜁5 + 𝜁

) =
4 2

(𝜁 5 ) 2 − (𝜁 4 ) 2
𝜁5 − 𝜁4
= 5
. (3.305)
( 5
)
2
𝜁 + 𝜁4
𝜁 + 𝜁4

The consistency of the above relations is verified by substituting 𝑥 𝜇¤ and (𝑥) 2 , as
given above, into Eq. (3.211), which yields Eq. (3.204).
4. Action of the conformal group SO(4, 2): The conformal group acts linearly on
the ambient space R4,2 , preserving the null cone 𝑄. This action descends naturally to the projectivized cone P𝑄, inducing a well-defined projective action on
compactified Minkowski space. Concretely, the Lie algebra 𝔰𝔬(4, 2) is realized
on Dirac’s projective quadric by first-order differential operators of the form:

## PDF page 139

3.9 Appendix: The Lie Algebra 𝔰𝔬 (4, 2) and its Euclidean 𝔰𝔬 (5, 1) Counterpart; the 𝑧-Picture of the 𝔰𝔬 (4, 2) Generators
125

(
)
𝑋 𝜇𝜈 = −𝑋𝜈 𝜇 = 𝜁 𝜇 𝜕𝜈 − 𝜁 𝜈 𝜕𝜇 ,

𝜕𝜇 :=

𝜕
,
𝜕𝜁 𝜇

(3.306)

which satisfy the commutation relations (3.37). In this way, Dirac’s projective
quadric furnishes a natural geometric stage for the global action of the conformal
group, making manifest the realization of conformal symmetry on compactified
Minkowski space.
5. Generators of translations and special conformal transformations: The Lie
algebra 𝔰𝔬(4, 2), defined via differential operators acting on smooth functions
over Minkowski spacetime, is generated by the infinitesimal translations and
special conformal transformations. Specifically, the infinitesimal translations
are given by:
i𝑝 𝜇¤ = 𝜕𝜇¤ :=

𝜕
,
𝜕𝑥 𝜇¤

(3.307)

where 𝑝 𝜇¤ denotes the 4-momentum. The special conformal generators are defined as:
i𝑘 𝜇¤ = (𝑥) 2 𝜕𝜇¤ − 2𝑥 𝜇¤ (𝑥 · 𝜕) .

(3.308)

The Lie brackets of these generators generate the full conformal Lie algebra,
including the Lorentz transformations 𝑥 𝜇¤ 𝜕𝜈¤ − 𝑥 𝜈¤ 𝜕𝜇¤ and the dilatation operator
𝑥 · 𝜕. In particular, the commutator between translation and special conformal
generators reads:
[
]
(
)
i𝑘 𝜈¤ , i𝑝 𝜇¤ = 2 𝜂 𝜇¤ 𝜈¤ (𝑥 · 𝜕) − 2 𝑥 𝜇¤ 𝜕𝜈¤ − 𝑥 𝜈¤ 𝜕𝜇¤ .
(3.309)
We recall our mostly ‘+’ convention for the metric signature in R4,2 ; 𝜂11 = · · · =
𝜂44 = +1, while 𝜂00 = 𝜂55 = −1. The vector fields i𝑝 𝜇¤ and i𝑘 𝜇¤ are related to the
generators 𝑋 𝜇𝜈 (3.306) by:
i𝑝 𝜇¤ = 𝑋 ¤𝜇5 − 𝑋 ¤𝜇4 ,

i𝑘 𝜇¤ = 𝑋 ¤𝜇5 + 𝑋 ¤𝜇4 .

(3.310)

This follows from the relations (for 𝑥 𝜈¤ given by (3.305)):
𝜁 5 𝛿 𝜈𝜇¤¤

𝜁 𝜇¤ 𝜁 𝜈¤

1 + (𝑥) 2 𝜈¤
𝛿 𝜇¤ − 𝑥 𝜇¤ 𝑥 𝜈¤ ,
2

(3.311)

𝜁 4 𝛿 𝜈𝜇¤¤
𝜁 𝜇¤ 𝜁 𝜈¤
(𝑥) 2 − 1 𝜈¤
𝑋 ¤𝜇4 𝑥 𝜈¤ = − 4
−
=
𝛿 𝜇¤ − 𝑥 𝜇¤ 𝑥 𝜈¤ .
(
)
2
2
𝜁 + 𝜁5
𝜁4 + 𝜁5

(3.312)

𝑋 ¤𝜇5 𝑥 𝜈¤ =

𝜁4 + 𝜁

− (
5

𝜁4 + 𝜁

) =
5 2

Note: Regarding the above calculations, it is worthwhile to highlight a subtle
point here:

## PDF page 140

3 Ladder Representation of 𝔲 (2, 2) as a Quantized 4-dimensional Realization

126

𝜕𝜇¤ 𝑥 𝜈¤ =

𝜕𝜇¤ 𝑥 𝜈¤ =

𝜕 𝜈¤
𝑥 = 𝛿 𝜈𝜇¤¤ ,
𝜕𝑥 𝜇¤

)
𝜕
𝜕 (
𝜌¤
𝑥 𝜈¤ =
𝜂 𝜈¤ 𝜌¤ 𝑥 𝜌¤ = 𝜂 𝜈¤ 𝜌¤ 𝛿 𝜇¤ = 𝜂 𝜈¤ 𝜇¤ = 𝜂 𝜇¤ 𝜈¤ .
𝜇
¤
𝜇
¤
𝜕𝑥
𝜕𝑥

(3.313)

(3.314)

6. Huygens principle and propagation along null directions: In Minkowski spacetime, the Huygens principle for massless fields asserts that wave propagation is
strictly supported on null directions. If a scalar field 𝜙(𝑥) satisfies the massless
wave equation:
□𝜙(𝑥) = 𝜂 𝜇¤ 𝜈¤ 𝜕𝜇¤ 𝜕𝜈¤ 𝜙(𝑥) = 0 ,

(3.315)

then a compactly supported disturbance at a spacetime point 𝑥 ◦ propagates
exclusively along the light cone (𝑥 − 𝑥 ◦ ) 2 = 0. In particular, the solution exhibits
no tail inside the cone: the field vanishes identically both inside and outside the
null hypersurface determined by 𝑥◦ . Hence, the causal propagation of massless
signals is completely governed by null directions.
Within the projective framework, this principle admits a natural geometric formulation. Each point 𝜁 ∈ P𝑄 encodes a null direction in spacetime and thus
determines a lightlike ray along which massless disturbances propagate. Via the
homogeneous embedding (3.305), the ambient null condition 𝜁 2 = 0 projects
precisely onto the spacetime light-cone condition (𝑥 −𝑥 ◦ ) 2 = 0. Families of such
rays generate wavefronts, while caustics arise at points where the projection from
P𝑄 to spacetime fails to be regular, namely:
det

𝜕𝑥 𝜇¤
= 0,
𝜕𝜃 𝑖

(3.316)

with 𝜃 𝑖 parametrizing the ray family. Since P𝑄 is compact and carries a natural
action of the conformal group, this description is global and conformally invariant, providing a robust geometric framework for analyzing the propagation
and focusing of massless perturbations, notably in cosmological and inflationary
applications.
With the above material in mind, we now return to our main
intro( objective:
)
ducing the 𝑧-picture of the 𝔰𝔬(4, 2) generators. The variables 𝑧 𝑖 = 𝑧 𝑖 (3.204) are
covariantly transformed by the generators i𝑋0𝜌 and 𝑋𝜌𝜌′ , with 𝜌, 𝜌 ′ = 1, 2, 3, 4, 5,
which span a real form SO(5, 1) of the complexified of SO(4, 2). Explicitly, we have:
𝜕
,
𝜕𝑧 𝑖
𝐶𝑖(𝑧) = − (𝑋𝑖5 − i𝑋0𝑖 ) = −(𝑧) 2 𝜕𝑖 + 2𝑧 𝑖 (𝑧 · 𝜕) ,
𝑇𝑖(𝑧) = + (𝑋𝑖5 + i𝑋0𝑖 ) = 𝜕𝑖 ,

since:

𝜕𝑖 :=

(3.317)
(3.318)

## PDF page 141

3.9 Appendix: The Lie Algebra 𝔰𝔬 (4, 2) and its Euclidean 𝔰𝔬 (5, 1) Counterpart; the 𝑧-Picture of the 𝔰𝔬 (4, 2) Generators
127

𝜁 5 𝛿𝑖

𝑗

1 + (𝑧) 2 𝑗
𝛿𝑖 − 𝑧 𝑖 𝑧 𝑗 ,
2

(3.319)

𝜁𝑖 𝜁 𝑗
1 − (𝑧) 2 𝑗
i𝑋0𝑖 𝑧 = − 5
+
𝛿𝑖 + 𝑧 𝑖 𝑧 𝑗 ,
=
(
)
2
2
𝜁 − i𝜁 0
𝜁 5 − i𝜁 0

(3.320)

𝑋𝑖5 𝑧 𝑗 =

𝜁 5 − i𝜁

− (
0

𝜁𝑖 𝜁 𝑗
𝜁 5 − i𝜁

) =
0 2

i𝜁 0 𝛿𝑖

𝑗

𝑗

with 𝑖, 𝑗 = 1, 2, 3, 4. Moreover, we have:
𝐻 (𝑧) = i𝑋05 = −𝑧 · 𝜕 ,

since

i𝑋05 𝑧 𝑗 =

−𝜁 𝑗
𝜁 5 − i𝜁 0

𝐽𝑖(𝑧)
𝑗 = 𝑋𝑖 𝑗 = 𝑧 𝑖 𝜕 𝑗 − 𝑧 𝑗 𝜕𝑖 .

= −𝑧 𝑗 ,

(3.321)

(3.322)

In direct analogy with the commutation relations given in Eqs. (3.192), (3.193),
(3.194), and (3.195), it is observed that:
[ (𝑧) (𝑧) ]
(3.323)
𝐻 , 𝐽𝑖 𝑗 = 0 ,
[ (𝑧) (𝑧) ]
(3.324)
= 2𝐻 (𝑧) 𝛿𝑖 𝑗 − 2𝐽𝑖(𝑧)
𝐶𝑖 , 𝑇 𝑗
𝑗 ,
[ (𝑧) (𝑧) ]
𝐻 , 𝑇𝑖
= 𝑇𝑖(𝑧) ,
(3.325)
[ (𝑧) (𝑧) ]
(𝑧)
𝐻 , 𝐶𝑖
= − 𝐶𝑖 .
(3.326)

## PDF page 142



## PDF page 143

Chapter 4

Conformal Massless Low Helicity Fields and
their de Sitter (dS) Spacetime Restriction

Abstract This chapter presents a systematic construction of low-helicity conformal
massless fields, with particular emphasis on the zero-helicity case in de Sitter (dS)
spacetime. It begins by formulating the massless scalar field in terms of ladder-type
vertex operators built from Bose creation and annihilation operators, supplemented
by zero-mode operators that ensure the correct lowest-energy states and reproduce
the canonical two-point functions. The analytic structure of these operators is established within a precompact tube domain, ensuring convergence of the corresponding
harmonic polynomial expansions.
Subsequently, it describes the restriction of conformal massless fields from the
6-dimensional conformal space to 4-dimensional dS spacetime, emphasizing the role
of homogeneous functions on the light cone and the associated gauge freedom. The
construction elucidates the relation between Euclidean coordinates in the analytically continued half-space and Minkowski-type coordinates, highlighting the Weyl
rescaling that connects the conformally flat metric to the standard dS metric.
Finally, the chapter demonstrates how the 6-dimensional conformally invariant
two-point functions project naturally onto dS spacetime, yielding the standard dS
two-point functions for massless scalar fields. These results provide a rigorous framework for understanding the interplay between conformal symmetry, low helicity
fields, and their geometric realization in curved spacetimes.

4.1 Ladder Vertex Operator Construction of the Scalar Field
ˆ
In order to write down the free massless scalar field 𝜙(𝑧)
in terms of Bose creation
and annihilation operators (3.62), we need yet another pair of zero-mode operators
𝜒 and 𝜒∗ intertwining |0U(2,2) ⟩ and |LW𝜆=0 ⟩ =: |0SO(4) ⟩ = |1, 0, 0⟩, such that:
𝜒|0U(2,2) ⟩ = 0 = ⟨0U(2,2) | 𝜒∗ ,

(4.1)

129

## PDF page 144

130

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

𝜒∗ |0U(2,2) ⟩ = |1, 0, 0⟩ ,
[

]
𝜒, 𝜒∗ = 1 ,

and

⟨1, 0, 0| = ⟨0U(2,2) | 𝜒 ,

(4.2)

]
[
]
𝜒 (∗) , 𝜑 𝑎 = 0 = 𝜒 (∗) , 𝜑
˜𝑏 ,

(4.3)

and
[

for 𝜒 (∗) = 𝜒 or 𝜒∗ .
Proposition 4.1 The vertex operator:
)
(
(
)
𝜒
ˆ
𝑒 𝑧˘ ·𝐶 ,
𝜙(𝑧) = 𝒀 |1, 0, 0⟩, 𝑧 = 𝑒 𝑧·𝑇 𝜒∗ +
(𝑧) 2

(4.4)

where 𝑧˘𝑖 := 𝑧𝑖 /(𝑧) 2 , 𝑇𝑖 = 𝔞 ∗ E𝑖 𝔟∗ , and 𝐶𝑖 = (𝑇𝑖 ) ∗ = 𝔟 E𝑖∗ 𝔞, with 𝑖 = 1, . . . , 4,
satisfies all properties of a free massless scalar field and reproduces the two-point
function (3.244). In practice, the absence of negative powers of (𝑧) 2 in the power
U(2,2)
ˆ
seires expansion of 𝜙(𝑧)|0
⟩ (asserted by the first statement of Proposition 3.9)
is quaranteed by:
1. The presence of the zero-modes 𝜒 and 𝜒∗ in (4.4).
2. The fact that |1, 0, 0⟩ is a minimal-energy state in the conformally invariant zero(1)
helicity subspace H𝜆=0
⊂ H ; in particular, 𝑧˘ · 𝐶 |1, 0, 0⟩ = 0, or, more precisely,
𝐶𝑖 |1, 0, 0⟩ = 0.
Remark 4.1 In this context, before proceeding with the proof, it is important to
emphasize that the vacuum state |0U(2,2) ⟩ is conformally invariant, meaning that it is
annihilated by all infinitesimal generators of the conformal Lie algebra 𝔲(2, 2); the
explicit form of these generators can be found in Chap. 3. Explicitly:
𝐻|0U(2,2) ⟩ = 𝑇𝑖 |0U(2,2) ⟩ = 𝐶𝑖 |0U(2,2) ⟩ = 𝐽𝑖 𝑗 |0U(2,2) ⟩ = C1 |0U(2,2) ⟩ = 0 ,
where 𝑖, 𝑗 = 1, . . . , 4.

(4.5)
□

Proof We begin with some basic steps, illustrating along the way the advantages of
the analytic 𝑧-picture:
1. While the basic properties of the 𝑥-space two-point function and the vectorvalued distribuation ˆ
𝜙(𝑥)|0U(2,2) ⟩ require using a singular Fourier transformation
— involving 𝜃 ( 𝑝 0 )𝛿( 𝑝 2 ) (see Eq. (3.241)), ˆ
𝜙(𝑧)|0U(2,2) ⟩ is an analytic vector
precompact
valued function in 𝔗 +
, whose (discrete!) energy spectrum is displayed by
its (convergent) expression in homogeneous harmonic polynomials:
(
)
U(2,2)
ˆ
𝜙(𝑧)|0
⟩ = Y |1, 0, 0⟩, 𝑧 |0U(2,2) ⟩
)
(
𝜒
= 𝑒 𝑧·𝑇 𝜒∗ +
𝑒 𝑧˘ ·𝐶 |0U(2,2) ⟩
(𝑧) 2
∞
∑︁
(𝑧 · 𝑇) 𝑛
= 𝑒 𝑧·𝑇 |1, 0, 0⟩ =
|1, 0, 0⟩ ,
(4.6)
𝑛!
𝑛=0

## PDF page 145

4.1 Ladder Vertex Operator Construction of the Scalar Field

131

where:
Δ (𝑧 · 𝑇) 𝑛 =

4
∑︁
𝜕2

𝜕𝑧2𝑖
𝑖=1

(𝑧 · 𝑇) 𝑛 = 𝑛(𝑇 · 𝜕) (𝑇 · 𝑧) 𝑛−1 = 𝑛(𝑛 − 1) (𝑇) 2 (𝑇 · 𝑧) 𝑛−2 = 0 ,
(4.7)

∑
since (𝑇) 2 = 4𝑖=1 𝑇 𝑖 𝑇𝑖 = 0 (see Proposition 3.3).
2. The expected two-point function (3.244) is harmonic in both 𝑧 and 𝑢 and can be
expressed in terms of the generating function of the Gegenbauer polynomials C1𝑛 :
∞
1
1
1 ∑︁
1
=
=
H𝑛 ( 𝑧˘, 𝑢) ,
(𝑧 − 𝑢) 2
(𝑧) 2 1 + ( 𝑧˘) 2 (𝑢) 2 − 2𝑧˘ · 𝑢
(𝑧) 2 𝑛=0

(4.8)

where:
𝑛

H𝑛 ( 𝑧˘, 𝑢) =

)
[2] (
∑︁
𝑛−𝑘
𝑘

(

(2𝑧˘ · 𝑢) 𝑛−2𝑘 −( 𝑧˘) 2 (𝑢) 2

)𝑘

(

= ( 𝑧˘) 2 (𝑢) 2

) 𝑛2

(
C1𝑛 √︁

𝑘=0

3. Applying the commutation relation (3.285), we find:
( [
]
] (
[
))
(
)
ˆ
ˆ
𝐶𝑖 , 𝑇 𝑗 𝜙(𝑢)
= 𝐶𝑖 , 𝑇 𝑗 Y |1, 0, 0⟩, 𝑢 = 2 𝐻 𝛿𝑖 𝑗 − 𝐽𝑖 𝑗 𝜙(𝑢)
.

𝑧˘ · 𝑢

)
.

( 𝑧˘) 2 (𝑢) 2
(4.9)

(4.10)

Moreover, from Proposition 3.4, we have:
𝐻|1, 0, 0⟩ = |1, 0, 0⟩ ,

𝐽𝑖 𝑗 |1, 0, 0⟩ = 0 .

(4.11)

Accordingly, we obtain:
⟨1, 0, 0|

( 𝑧˘ · 𝐶) 𝑛 (𝑢 · 𝑇) 𝑛
|1, 0, 0⟩ = H𝑛 ( 𝑧˘, 𝑢) .
𝑛!
𝑛!

(4.12)

Let us examine the above identity, for some small values of 𝑛:
a. If 𝑛 = 0, then:
⟨1, 0, 0|1, 0, 0⟩ = 1 = H0 ( 𝑧˘, 𝑢) .
b. If 𝑛 = 1, then:

(4.13)

## PDF page 146

132

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

𝑧˘𝑖 𝑢 𝑗 ⟨1, 0, 0| 𝐶𝑖 𝑇 𝑗 |1, 0, 0⟩ = 𝑧˘𝑖 𝑢 𝑗 ⟨1, 0, 0| [𝐶𝑖 , 𝑇 𝑗 ] |1, 0, 0⟩
⏟
⏞⏞
⏟
= 2 𝛿𝑖 𝑗

+ 𝑧˘𝑖 𝑢 𝑗 ⟨1, 0, 0| 𝑇 𝑗 𝐶𝑖 |1, 0, 0⟩
⏟ ⏞⏞ ⏟
=0

= 2( 𝑧˘ · 𝑢) = H1 ( 𝑧˘, 𝑢) .

(4.14)

Now, equipped with the vertex operator expression (4.4), we proceed to verify
that it reproduces the correct two-point function explicitly:
⟨0U(2,2) | ˆ
𝜙(𝑧) ˆ
𝜙(𝑢) |0U(2,2) ⟩ =

1
.
(𝑧 − 𝑢) 2

(4.15)

First, recalling Eq. (4.6), we have:
𝜙(𝑧) ˆ
𝜙(𝑢)|0U(2,2) ⟩ = ⟨0U(2,2) | ˆ
𝜙(𝑧) 𝑒 𝑢·𝑇 |1, 0, 0⟩ .
⟨0U(2,2) | ˆ

(4.16)

Next, we plug in the vertex operator ˆ
𝜙(𝑧) and obtain:
(
)
𝜒
⟨0U(2,2) | ˆ
𝜙(𝑧) ˆ
𝜙(𝑢)|0U(2,2) ⟩ = ⟨0U(2,2) |𝑒 𝑧·𝑇 𝜒∗ +
𝑒 𝑧˘ ·𝐶 𝑒 𝑢·𝑇 |1, 0, 0⟩
(𝑧) 2
1
⟨1, 0, 0| 𝑒 𝑧˘ ·𝐶 𝑒 𝑢·𝑇 |1, 0, 0⟩
=
(𝑧) 2
∞
1 ∑︁ 1
=
⟨1, 0, 0|( 𝑧˘ · 𝐶) 𝑛 (𝑢 · 𝑇) 𝑚 |1, 0, 0⟩ .
(𝑧) 2 𝑛,𝑚=0 𝑛!𝑚!
(4.17)
The above expression is nonvanishing only when 𝑛 = 𝑚. In that case, using the basic
materials derived previously, we immediately find:
∞
1 ∑︁ 1
U(2,2)
ˆ 𝜙(𝑢)|0
ˆ
⟨0U(2,2) | 𝜙(𝑧)
⟩=
⟨1, 0, 0|( 𝑧˘ · 𝐶) 𝑛 (𝑢 · 𝑇) 𝑛 |1, 0, 0⟩
(𝑧) 2 𝑛=0 (𝑛!) 2

=

∞
1 ∑︁
1
.
H𝑛 ( 𝑧˘, 𝑢) =
2
(𝑧) 𝑛=0
(𝑧 − 𝑢) 2

(4.18)
□

Remark 4.2 It follows from the Hilbert space (or Wightman) positivity condition
(3.255) (see also Eq. (4.8)) that H𝑛 (𝑧, 𝑧) > 0, for (𝑧) 2 ≠ 0 and for all 𝑛 = 0, 1, 2, . . . .
Moreover, one can write:
(
)
𝑧·𝑧
𝑛
𝑛
2 𝑛 1
H𝑛 (𝑧, 𝑧) = (𝑧) C𝑛
≥ (𝑧) 2 C1𝑛 (1) = (𝑧) 2 (𝑛 + 1) > 0 ,
(4.19)
(𝑧) 2

## PDF page 147

4.2 Conformal Massless Scalar Field in de Sitter (dS) Space

133

since C1𝑛 (𝑥) ≥ C1𝑛 (1), for 𝑥 > 1.

□

Remark 4.3 The biharmonic polynomial H𝑛 (𝑧, 𝑢) (that is, Δ𝑧 H𝑛 (𝑧, 𝑢) = 0 =
Δ𝑢 H𝑛 (𝑧, 𝑢)) is the unique harmonic in 𝑧 extension of the monomial (2𝑧·𝑢) 𝑛 originally
defined (and harmonic in 𝑢) for (𝑧) 2 = 0 (see Example 2.6 in Ref. [120]).
□
Remark 4.4 It follows from (3.245) and (3.255) that the bra lowest energy oneparticle (zero helicity) state ⟨1, 0, 0| is:
(
)
(
)
𝜒
1 ( U(2,2) ˆ ∗ )
1
∗
U(2,2)
𝑧 ∗ ·𝑇
𝑧˘ ∗ ·𝐶
𝜒 + ∗ 2 𝑒
⟨0
|𝑒
lim
⟨0
| 𝜙(𝑧 ) = lim
𝑧→0 (𝑧) 2
𝑧→0 (𝑧) 2
(𝑧 )
)
(
1
1
= lim
⟨1, 0, 0| ∗ 2 𝑒 𝑧·𝐶
𝑧→0 (𝑧) 2
(𝑧 )
)
(
( 2)2
∞
∑︁
(𝑧)
1
(𝑧 · 𝐶) 𝑛
= lim
⟨1, 0, 0|
𝑛!
𝑧→0 (𝑧) 2
(𝑧) 2
𝑛=0
= ⟨1, 0, 0| ,

(4.20)

or, alternatively, upon replacing 𝑧 by 𝑧∗ = 𝑧˘ = (𝑧)𝑧 2 :
lim (𝑧)
𝑧→∞

2 (

⟨0

U(2,2)

(
)
(
)
)
𝜒
2
U(2,2)
𝑧·𝑇
𝑧˘ ·𝐶
∗
ˆ
| 𝜙(𝑧) = lim (𝑧) ⟨0
|𝑒
𝑒
𝜒 +
𝑧→∞
(𝑧) 2
(
)
1 𝑧˘ ·𝐶
= lim (𝑧) 2 ⟨1, 0, 0|
𝑒
𝑧→∞
(𝑧) 2
∞ (
)𝑛)
∑︁
1 1( 𝑧
⟨1, 0, 0|
= lim (𝑧) 2
·
𝐶
𝑧→∞
(𝑧) 2 𝑛! (𝑧) 2
𝑛=0
= ⟨1, 0, 0| .

(4.21)
□

4.2 Conformal Massless Scalar Field in de Sitter (dS) Space
The 4-dimensional dS spacetime (1.7) can be embedded in the Dirac quadric 𝑄
(3.202) as its intersection with the hyperplane 𝜁 5 = 𝑅:
}
⋂ {
dS = 𝑄
𝜁5 = 𝑅 > 0
{
}
4
∑︁
0
𝑖
2
2
2
2
= 𝜁 = −𝜁0 , 𝜁 = 𝜁𝑖 , 𝑖 = 1, 2, 3, 4 ; (𝜁) =
(𝜁𝑖 ) − (𝜁0 ) = 𝑅 .
𝑖=1

(4.22)
Accordingly, the Euclidean de Sitter (EdS) half-space is defined as follows:

## PDF page 148

134

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

{
0

EdS = 𝜁 = i𝜁 𝛽 , 𝜁 𝛽 > 0 ,

4
∑︁

}
2

2

(𝜁𝑖 ) + (𝜁 𝛽 ) = 𝑅

2

𝑖=1

{
}
(
)
= 𝜁 = 𝜁 𝛽 > 0, 𝜁1 , . . . , 𝜁4 ∈ S4𝑅 .

(4.23)

Remark 4.5 In this context, a few points merit further clarification:
1. The real (dimensionless) Cartesian coordinates of the EdS half-space, defined in
Eq. (4.23), are connected to the analytically continued versions of the coordinates
𝑧𝑖 introduced in Eq. (3.204). Specifically, setting:
(
)
𝜁 5 = 𝑅 > 0 , and 𝜁 𝛽 = 𝑅 tanh 𝛽 > 0
=⇒ 𝛽 > 0 ,
(4.24)
we have:
𝑧𝑖 =

𝜅𝜁𝑖
𝜁𝑖
=
,
𝑅 + 𝜁𝛽
1 + 𝜅𝜁 𝛽

(4.25)

where 𝜅 = 𝑅1 denotes the scalar curvature of EdS  S4𝑅 . It then follows that (𝑧) 2
is obtained as an analytic continuation of (3.209):
)
(
4
∑︁
𝑅 − 𝜁𝛽
1 − 𝜅𝜁 𝛽
𝑖
2
𝑧 𝑧𝑖 =
(𝑧) :=
=
= 𝑒 −2𝛽 .
(4.26)
𝑅
+
𝜁
1
+
𝜅𝜁
𝛽
𝛽
𝑖=1
Note that 𝜅𝜁 𝛽 = tanh 𝛽, with 𝛽 > 0. From this realization, one can observe that:
a. Given the equation above and the strict positivity of 𝛽, it follows immediately
that:
)
(
(4.27)
(𝑧) 2 = 𝑧 · 𝑧 = 𝑒 −2𝛽 < 1 ,
and also one can readily check that:
𝑧·𝑧<

)
1(
2
1 + (𝑧) 2 ,
2

(4.28)

This demonstrates that EdS half space (4.23) lies within the intersection of
the hyperplane 𝜁 5 = 𝑅 (with )the tube domain 𝔗 precompact
(3.218), where the
+
vector-valued function 𝜙ˆ 𝑧(𝜁) |0U(2,2) ⟩ is analytic.
b. The label 𝛽 in the imaginary time coordinate i𝜁 𝛽 is chosen to evoke the
1
Boltzmann factor 𝛽 = 𝐾𝑇
, where 𝑇 denotes the absolute temperature and 𝐾
is the Boltzmann constant. This choice reflects the fact that the analytically
continued two-point function of the field ˆ
𝜙(𝜁)|0⟩ admits an interpretation as
a thermal correlation function (see [115], particularly Sect. 7). In this context,
𝛽 can be understood as a real continuation of the imaginary proper time i𝜏,
where 𝜏 is the physical proper time (compare Eqs. (3.209) and (4.26)).

## PDF page 149

4.2 Conformal Massless Scalar Field in de Sitter (dS) Space

135

2. The metric form (d𝑧) 2 is related by a (Weyl) conformal factor to the manifestly
O(5)-invariant quadratic (d𝜁) 2 = (d𝜁𝑖 ) 2 + (d𝜁 𝛽 ) 2 :
) (
)
(
𝜁𝑖
𝜁𝑖
d
(d𝑧) 2 = d
𝑅 + 𝜁𝛽
𝑅 + 𝜁𝛽
(
)(
)
𝑖
(d𝜁 𝛽 ) 𝜁 𝑖
(d𝜁 𝛽 ) 𝜁𝑖
d𝜁
d𝜁𝑖
=
−
−
𝑅 + 𝜁 𝛽 (𝑅 + 𝜁 𝛽 ) 2 𝑅 + 𝜁 𝛽 (𝑅 + 𝜁 𝛽 ) 2
)
(
(
)
𝜁 𝑖 𝜁𝑖 = 𝑅 2 − (𝜁 𝛽 ) 2
2𝜁 𝑖 d𝜁𝑖
1
2
2
(d𝜁 𝛽 ) −
= (
d𝜁 𝛽
) 2 (d𝜁𝑖 ) +
𝑅 + 𝜁𝛽
(𝑅 + 𝜁 𝛽 ) 2
𝑅 + 𝜁𝛽
(
)
(
(
))
d(𝜁𝑖 ) 2 = d 𝑅 2 − (𝜁 𝛽 ) 2
𝑅 − 𝜁𝛽
1
2
2
= (
d𝜁 𝛽
) 2 (d𝜁𝑖 ) + 𝑅 + 𝜁 (d𝜁 𝛽 ) −
𝑅 + 𝜁𝛽
𝛽
𝑅 + 𝜁𝛽
(
)
1
1
2
2
2
(4.29)
= (
) 2 (d𝜁𝑖 ) + (d𝜁 𝛽 ) = (
) 2 (d𝜁) ,
𝑅 + 𝜁𝛽
𝑅 + 𝜁𝛽
and hence:
(

(d𝜁) 2

)
= (d𝜁𝑖 ) 2 + (d𝜁 𝛽 ) 2 = Ω2 (𝑧) (d𝑧) 2 ,
2𝑅
.
1 + (𝑧) 2

Ω(𝑧) := 𝑅 + 𝜁 𝛽 =

with

(4.30)

Note that summation over the repeated index ‘𝑖’ from 1 to 4 is assumed throughout.
3. Coming back to the real dS spacetime with Lorentzian signature, we can express
the Minkowski coordinate 𝑥 𝜇¤ (of dimension of length) in terms of the O(4, 1)
covariant vector 𝜁 (4.22) by the following relations:
𝜅𝑥 𝜇¤ =

𝜁 𝜇¤
𝜅𝜁 𝜇¤
=
𝑅 + 𝜁4 1 + 𝜅𝜁4

=⇒

𝜅 2 (𝑥) 2

(

) 1 − 𝜅𝜁
4
:= 𝜅 2 𝑥 𝜇¤ 𝑥 𝜇¤ =
,
1 + 𝜅𝜁4

(4.31)

where, again, 𝜇¤ = 0, 1, 2, 3. Then, in complex analogy with (4.29), we have:1
(
)
(d𝜁) 2 = (d𝜁 𝜇¤ ) 2 + (d𝜁4 ) 2 = Ω2 (𝑥) (d𝑥 𝜇¤ ) 2 ,
with

Ω(𝑥) := 1 + 𝜅𝜁4 =

2
.
1 + 𝜅 2 (𝑥) 2

(4.32)

4. The expression (4.29) and (4.32) involve different small curvature (𝑅 → ∞ or
𝜅 → 0) limits:
a. EdS case: For 𝜁 𝛽 ≈ 𝑅 (or 𝜅𝜁 𝛽 ≈ 1) and hence |𝜁𝑖 | ≪ 𝑅, we have:
i. Eqs. (4.25) and (4.26), respectively, imply that |𝑧 𝑖 | and (𝑧) 2 ≪ 1.
1 The Weyl factor Ω

FHH ( 𝑥 ) =

(

2

1 + 𝜅4 ( 𝑥 ) 2

) −1

of Ref. [121] differes from ours by the factor 14 in
𝜇¤

2𝜁
front of 𝜅 2 ( 𝑥 ) 2 ; it can be reproduced by substituting (4.31) by 𝑥 𝜇¤ = 1+𝜅
𝜁4 .

## PDF page 150

136

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

ii. From Eqs. (4.31), (4.25), and (4.26), we obtain:
𝜅 2 (𝑥) 2 =

1 − 𝜅𝜁4 1 + (𝑧) 2 − 2𝑧 4
=
≈ 1 − 4𝑧 4 ≈ 1 .
1 + 𝜅𝜁4 1 + (𝑧) 2 + 2𝑧 4

(4.33)

iii. From Eqs. (4.30), (4.25), and (4.26), the Euclidean O(5)-invariant metric
(d𝜁) 2 approaches:
(
)
(d𝜁) 2 := (d𝜁𝑖 ) 2 + (d𝜁 𝛽 ) 2
−→ 4𝑅 2 (d𝑧 𝑖 ) 2 ≫ (d𝑧𝑖 ) 2 .
(4.34)
b. dS case: For 𝜁4 ≈ 𝑅 (or 𝜅𝜁4 ≈ 1) and hence |𝜁 𝜇¤ | ≪ 𝑅, we have:
i. Eq. (4.31) implies that |𝑥 𝜇¤ | and (𝑥) 2 ≪ 1.
ii. From Eqs. (4.26) and (4.31), we obtain:
(𝑧) 2 =

1 + 𝜅 2 (𝑥) 2 − 2𝜅𝑥 𝛽
1 − 𝜅𝜁 𝛽
=
≈ 1 − 4𝜅𝑥 𝛽 ≈ 1 ,
1 + 𝜅𝜁 𝛽
1 + 𝜅 2 (𝑥) 2 + 2𝜅𝑥 𝛽

(4.35)

where 𝑥 0 := i𝑥 𝛽 .
iii. From Eqs. (4.32) and (4.31), the Euclidean O(5)-invariant metric (d𝜁) 2
approaches:
(
)
(d𝜁) 2 := (d𝜁 𝜇¤ ) 2 + (d𝜁4 ) 2
−→ 4(d𝑥 𝜇¤ ) 2 .
(4.36)
□
We now proceed to write down the field (wave) equation and the two-point
function for a conformal (massless) scalar field in (E)dS space.
Working in conformal space — without imposing the dS constraint 𝜁 5 = 𝑅 —
Dirac [23] demonstrated that solutions 𝜙(𝜁) to the manifestly invariant 6-dimensional
d’Alembert equation:
□6 𝜙(𝜁) = 0 ,

with

□6 =

4
∑︁
𝜕2

−
2

𝑖=1

𝜕𝜁𝑖

𝜕2
𝜕2
−
,
𝜕𝜁02 𝜕𝜁52

(4.37)

are only well-defined on the light cone (𝜁) 2 = 0, if 𝜙 is homogeneous of degree −1.
Specifically, if 𝜙(𝜁) satisfies the homogeneity condition:
𝜙( 𝜚𝜁) = 𝜚 𝑑 𝜙(𝜁) ,

for all

𝜚 > 0,

(4.38)

then the equation □6 𝜙 = 0 defines a conformally invariant field only on the quadric
(𝜁) 2 = 0 provided that 𝑑 = −1.
This requirement arises from a subtle invariance:
1. Since the physical field 𝜙(𝜁) is defined only on the cone (𝜁) 2 = 0, it can be freely
modified by adding terms proportional to (𝜁) 2 , without affecting its restriction
to the cone; that is:

## PDF page 151

4.2 Conformal Massless Scalar Field in de Sitter (dS) Space

𝜙(𝜁)

↦−→

137

𝜙(𝜁) + (𝜁) 2 𝝓(𝜁) ,

(4.39)

where the new field 𝝓(𝜁) is assumed to be homogeneous of degree 𝑑 − 2:
𝝓( 𝜚𝜁) = 𝜚 𝑑−2 𝝓(𝜁) ,

for all

𝜚 > 0.

(4.40)

2. To ensure that the gauge-transformed function 𝜙(𝜁) + (𝜁) 2 𝝓(𝜁) still satisfies
d’Alembert equation (4.37) on the cone, we require that:
(
)
= 0.
(4.41)
□6 (𝜁) 2 𝝓(𝜁)
2
(𝜁 ) =0

This condition holds only if 𝑑 = −1. The reason follows from the commutator
(see Appendix 4.3):
)
(
[
]
𝜕
(4.42)
□𝑛 , (𝜁) 2 = 2 𝑛 + 2𝜁 𝜇 𝜇 =: 2 (𝑛 + 2𝜁 · 𝜕) ,
𝜕𝜁
which yields (see derivation in footnote2 ):
(
)
(
)
□𝑛=6 (𝜁) 2 𝝓
= 2 6 + 2(𝑑 − 2) 𝝓 = 0
2

⇐⇒

( 𝜁 ) =0

𝑑 = −1 .

(4.43)

′ , 𝜁 ′5 = 𝑅), where (𝜁 ) 2 = 𝑅 2 = (𝜁 ′ ) 2
For 𝜁D = (𝜁dS , 𝜁D5 = 𝑅) and 𝜁D′ = (𝜁dS
dS
dS
D
2
′
2
and (𝜁D ) = 0 = (𝜁D ) , it is natural to expect that a conformally invariant two-point
function on dS spacetime (see, for instance, Ref. [49]3 ) can be recovered from the
manifestly invariant one defined on the 6-dimensional light cone. In this setting, the
corresponding two-point function takes the form:

2 For any sufficiently smooth function 𝑓 (𝜁 ), from the commutator (4.42), we have:

(
)
𝜕𝑓
□𝑛 ( 𝜁 ) 2 𝑓 = 2𝑛 𝑓 + 4𝜁 𝜇
+ (𝜁 ) 2 □𝑛 𝑓 ,
𝜕𝜁 𝜇
so that, on the cone ( 𝜁 ) 2 = 0, it simplifies to:
(
)
□𝑛 ( 𝜁 ) 2 𝑓
2

(𝜁 ) =0

= 2𝑛 𝑓 + 4𝜁 · 𝜕 𝑓 .

Now, if 𝑓 = 𝝓 is homogeneous of degree 𝑑 − 2, then 𝜁 · 𝜕𝝓 = (𝑑 − 2)𝝓, and thus:
(
)
(
)
□𝑛 ( 𝜁 ) 2 𝝓
= 2𝑛 + 4(𝑑 − 2) 𝝓 .
2
(𝜁 ) =0

In 𝑛 = 6 dimensions, this vanishes only when 𝑑 = −1.
3 In Ref. [49], the metric signature is chosen to be mostly negative, in contrast to the convention
adopted in this manuscript. As a result, certain terms in the corresponding two-point function differ
from ours by a sign.

## PDF page 152

138

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction
′
𝑊 (𝜁dS , 𝜁dS
) := 𝑊 (𝜁D , 𝜁D′ )

𝜁D5 =𝑅=𝜁D′5

1

=
(2𝜋)

(
2

𝜁D − 𝜁D′

)2

𝜁D5 =𝑅=𝜁D′5

1

=

(

′
8𝜋 2 𝑅 2 − 𝜁dS · 𝜁dS

).

(4.44)

This is simply the pullback of the conformally invariant 6-dimensional two-point
function onto the 5-dimensional dS hyperboloid (𝜁dS ) 2 = 𝑅 2 . Note that, the twopoint function 𝑊 (𝜁D , 𝜁D′ ) is manifestly homogeneous of degree −1 in 𝜁D′ ; that is:
𝑊 (𝜁D , 𝜚𝜁D′ ) =

1
(2𝜋)

(
2

) =

2
𝜁D − 𝜚𝜁D′

(2𝜋) 2

(

1
) = 𝜚 −1𝑊 (𝜁D , 𝜁D′ ) ,
−2𝜚 𝜁D · 𝜁D′
(4.45)

and, by symmetry, it is also homogeneous of degree −1 in 𝜁D . Moreover, it satisfies
the 6-dimensional wave equation:
□6 𝑊 (𝜁D , 𝜁D′ ) = 0 .

(4.46)

4.3 Appendix: On the Commutator (4.42)
We compute the action of the commutator (4.42) on a test function 𝑓 (𝜁):
[
]
(
)
(
)
□𝑛 , (𝜁) 2 𝑓 = □𝑛 (𝜁) 2 𝑓 − (𝜁) 2 □𝑛 𝑓 = 𝜂 𝜇𝜈 𝜕𝜇 𝜕𝜈 (𝜁) 2 𝑓 − (𝜁) 2 □𝑛 𝑓 ,

(4.47)

where 𝜇, 𝜈 = 0, 5, 1, 2, 3, 4 and the metric 𝜂 𝜇𝜈 has the signature (−, −, +, +, +, +).
First, we employ the product rule:
(
) (
)
𝜕𝜈 (𝜁) 2 𝑓 = 𝜕𝜈 (𝜁) 2 𝑓 + (𝜁) 2 𝜕𝜈 𝑓 ,
((
)
(
)
)
𝜕𝜇 𝜕𝜈 (𝜁) 2 𝑓 = 𝜕𝜇 𝜕𝜈 (𝜁) 2 𝑓 + (𝜁) 2 𝜕𝜈 𝑓
(
)
(
)
(
)
= 𝜕𝜇 𝜕𝜈 (𝜁) 2 𝑓 + 𝜕𝜈 (𝜁) 2 𝜕𝜇 𝑓 + 𝜕𝜇 (𝜁) 2 𝜕𝜈 𝑓 + (𝜁) 2 𝜕𝜇 𝜕𝜈 𝑓 ,
(4.48)
where 𝜕𝜇 := 𝜕𝜁𝜕 𝜇 , and then, we use 𝜕𝜇 (𝜁) 2 = 2𝜂 𝜇 𝜍 𝜁 𝜍 and 𝜕𝜇 𝜕𝜈 (𝜁) 2 = 2𝜂 𝜇𝜈 .
Substituting into the full expression yields:
(
)
(
)
𝜂 𝜇𝜈 𝜕𝜇 𝜕𝜈 (𝜁) 2 𝑓 = 𝜂 𝜇𝜈 2𝜂 𝜇𝜈 𝑓 + 2𝜂 𝜈 𝜍 𝜁 𝜍 𝜕𝜇 𝑓 + 2𝜂 𝜇 𝜍 𝜁 𝜍 𝜕𝜈 𝑓 + (𝜁) 2 𝜕𝜇 𝜕𝜈 𝑓
= 2𝑛 𝑓 + 4𝜁 𝜇 𝜕𝜇 𝑓 + (𝜁) 2 □𝑛 𝑓 .
Thus, we obtain the commutator:

(4.49)

## PDF page 153

4.3 Appendix: On the Commutator (4.42)
139
<math display="block">\left[\Box_n, (\zeta)^2\right] f = 2nf + 4\zeta \cdot \partial f.</math>
(4.50)

## PDF page 154

140

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

References
1. É. Cartan, Leçons sur la géométrie des espaces de Riemann, Gauthier-Villars (1928).
2. H. Weyl, Gravitation und elektrizität, In Das Relativitätsprinzip: Eine Sammlung von Abhandlungen (pp. 147-159), Wiesbaden: Vieweg+ Teubner Verlag (1918).
3. E.P. Wigner, On unitary representations of the inhomogeneous Lorentz group, Ann, Math.,
40, 149 (1939).
4. T.D. Newton, E.P. Wigner, Localized states for elementary particles, Rev. Mod. Phys., 21, 400
(1949).
5. V. Bargmann, Irreducible unitary representations of the Lorentz group, Ann. Math., 48(3),
568-640 (1947).
6. I.M. Gel’fand, M.A. Naimark, Unitary representations of the Lorentz group, Izv. Akad. Nauk
SSSR Ser. Mat., 11, 5, 411–504 (1947).
7. I.E. Segal, A class of operator algebras which are determined by groups, Duke Math. J., 18,
221-265, 1951.
8. G.W. Mackey, Induced Representations of Groups and Quantum Mechanics, J. Math. Phys.,
(1950) — Series of papers developing induced representation theory and applications to
massless fields.
9. Harish-Chandra, Plancherel formula for the 2 × 2 real unimodular group, Proceedings of the
National Academy of Sciences, 38(4), 337-342 (1952); Representations of a semisimple Lie
group on a Banach space. I, Transactions of the American Mathematical Society, 185-243
(1953); Representations of semisimple Lie groups. II, Transactions of the American Mathematical Society, 26-65 (1954); Representations of semisimple Lie groups. III. Transactions
of the American Mathematical Society, 234-253 (1954); On the Plancherel Formula for the
Right-Invariant Functions on a Semisimple Lie Group, Proceedings of the National Academy
of Sciences, 40(3), 200-204 (1954).
10. I.M. Gel’fand, R.A. Minlos, and Z.Y. Shapiro, Representations of the Rotation and Lorentz
Groups and their Applications, Courier Dover Publications (1963).
11. G. Mack, A. Salam, Finite-component field representations of the conformal group, Ann.
Phys., 53(1), 174-202 (1969).
12. C. Fronsdal, Massless fields with integer spin, Phys. Rev. D, 18(10), 3624 (1978).
13. G. Mack, I. Todorov, Irreducibility of the ladder representations of U(2, 2) when restricted
to the Poincaré subgroup, J. Math. Phys. 10, 2078 (1969).
14. Ivan T. Todorov (1933-2025) https://www.ihes.fr/en/todorov-en/?utm
15. Ivan Todorov, Biography and Contributions, Museum of the Bulgarian Academy of Sciences,
http://museum.issp.bas.bg/m11-itodorov.html, accessed September 2025.
16. IHES, Tribute to Ivan Todorov, Institut des Hautes Études Scientifiques, https://www.ihes.
fr/en/tribute-todorov/, accessed September 2025.
17. N.N. Bogoliubov, A.A. Logunov, A.I. Oksak, and I. Todorov, General principles of quantum
field theory, (Vol. 10), Springer Science and Business Media (2012).
18. N.N. Bogoliubov, A.A. Logunov, and I. Todorov, Introduction to axiomatic quantum field
theory (1975).
19. V.K. Dobrev, G. Mack, V.B. Petkova, S.G. Petrova, I. Todorov, Harmonic analysis: on the
𝑛-dimensional Lorentz group and its application to conformal quantum field theory, Berlin,
Heidelberg: Springer Berlin Heidelberg (1977).
20. CERN
Courier,
Ivan
Todorov
1933-2025,
https://cerncourier.com/a/
ivan-todorov-1933-2025/, accessed September 2025.
21. W. De Sitter, On the relativity of inertia. Remarks concerning Einstein’s latest hypothesis,
Proc. Kon. Ned. Acad. Wet 19.2, 1217 (1917).
22. E.P. Wigner, Some remarks on the infinite de Sitter space, Proc. Natl. Acad. Sci. USA 36, 184
(1950).
23. P.A.M. Dirac, Wave Equations in Conformal Space, Ann. Math., 37, 429-442 (1936).

## PDF page 155

References

141

24. G. Mack, A. Salam, Finite-Component Field Representations of the Conformal Group, Ann.
Phys., 53, 174-202 (1969).
25. G. Mack, All unitary ray representations of the conformal group SU(2, 2) with positive energy,
Commun. Math. Phys. 55, 1 (1977).
26. A. Linde, Particle Physics and Inflationary Cosmology, Harwood Academic Publishers, Chur
(1990).
27. A.G. Riess et al., Observational evidence from supernovae for an accelerating universe and
a cosmological constant, Astronomical J., 116, 1009 (1998).
28. S. Perlmutter et al., Measurements of Ω and Λ from 42 high-redshift supernovae, Astrophys.
J., 517-565 (1999).
29. M. Enayati, J.-P. Gazeau, H. Pejhan, A. Wang, The de Sitter (dS) Group and its Representations
(2nd edition), Springer, Cham, Switzerland (2024).
30. E. Inönü, E.P. Wigner, Representations of the Galilei group, Nuovo Cimento, 9, 705 (1952).
31. J.M. Lévy-Leblond, Galilei group and nonrelativistic quantum mechanics, J. Math. Phys., 4,
776 (1963).
32. J. Voisin, On some unitary representations of the Galilei group I. Irreducible representations,
J. Math. Phys. 6, 1519 (1965); and On the unitary representations of the Galilei group. II.
Two-particle systems, J. Math. Phys., 6, 1822 (1965).
33. F. Gürsey, T.D. Lee, Spin 1/2 wave equation in de-Sitter space, Proc. Natl. Acad. Sci. USA,
40, 179 (1963).
34. C. Fronsdal, Elementary particles in a curved space, Rev. Mod. Phys., 37, 221 (1965).
35. C. Fronsdal, Elementary particles in a curved space. II, Phys. Rev. D, 10, 589 (1974).
36. R. Aldrovandi, J.P.B. Almeida, J.G. Pereira, de Sitter special relativity, Class. Quant. Grav.,
24.6, 1385 (2007).
37. M. Enayati, J.-P. Gazeau, M.A. del Olmo, H. Pejhan, Anti-de Sitterian “massive” elementary
systems and their Minkowskian and Newton-Hooke contraction limits, J. Math. Phys., 66,
053501 (2025).
38. H. Bacry, J.M. Levy-Leblond, Possible kinematics, J. Math. Phys., 9, 1605 (1968).
39. M. Levy-Nahas, Deformation and contraction of Lie algebras, J. Math. Phys., 8, 1211 (1967).
40. A.O. Barut, A. Böhm, Reduction of a class of O(4, 2) representations with respect to SO(4, 1)
and SO(3, 2), J. Math. Phys., 11.10, 2938-2945 (1970).
41. E. Angelopoulos, M. Flato, C. Fronsdal, D. Sternheimer, Massless particles, conformal group,
and de Sitter universe, Phys. Rev. D 23, 1278 (1981).
42. B. Binegar, C. Fronsdal, W. Heidenreich, Conformal Q.E.D., J. Math. Phys., 24, 2828-2846
(1983).
43. V.K. Dobrev, V.B. Petkova. All positive energy unitary irreducible representations of extended
conformal supersymmetry, Phys. Lett. B 162, 127-132 (1985).
44. M. Flato, C. Fronsdal, J.-P. Gazeau, Masslessness and light-cone propagation in 3 + 2 de Sitter
and 2 + 1 Minkowski spaces, Phys. Rev. D 33, 415 (1986).
45. T.P. Branson, Group Representations Arising from Lorentz Conformal Geometry, J. Funct.
Anal., 74, 199-291 (1987).
46. J.-P. Gazeau, M. Hans, R. Murenzi, Invariant bilinear forms on 3 + 2 de Sitter space, Class.
Quant. Grav., 6, 329 (1989).
47. P. Francesco, P. Mathieu, D. Sénéchal, Conformal field theory, Springer Science Business
Media (1997).
48. E. Angelopoulos, M. Laoues, Masslessness in 𝑛-dimensions, Rev. Math. Phys., 10.03, 271-299
(1998).
49. T. Garidi, J.-P. Gazeau, S. Rouhani, M.V. Takook, “Massless” vector field in de Sitter universe,
J. Math. Phys. 49, 032501 (2008).
50. A. Jadczyk, Conformally compactified Minkowski space: Myths and facts, Prespacetime Journal, 3(2) (2012).
51. H. Pejhan, S. Rahbardehghan, Covariant and infrared-free graviton two-point function in de
Sitter spacetime. II, Phys. Rev. D, 94, 104030 (2016).

## PDF page 156

142

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

52. H. Pejhan, S. Rahbardehghan, Covariant and infrared-free graviton two-point function in de
Sitter spacetime, Phys. Rev. D, 93, 044016 (2016).
53. K. Bamba, S. Rahbardehghan, H. Pejhan, Vacuum states for gravitons field in de Sitter space,
Phys. Rev. D, 96, 106009 (2017).
54. H. Pejhan, K. Bamba, S. Rahbardehghan, M. Enayati, Massless spin-2 field in de Sitter space,
Phys. Rev. D, 98, 045007 (2018).
55. H. Pejhan, M. Enayati, J.-P. Gazeau, A. Wang, Gupta-Bleuler quantization for linearized
gravity in de Sitter spacetime, Phys. Rev. D, 100, 066012 (2019).
56. H. Pejhan, S. Rahbardehghan, M. Enayati, K. Bamba, A. Wang, ‘Hidden’ symmetry of linearized gravity in de Sitter space, Phys. Lett. B, 795, 220 (2019).
57. J.-P. Gazeau, H. Pejhan, Covariant quantization of the partially massless graviton field in de
Sitter spacetime, Phys. Rev. D, 108, 065012 (2023).
58. V.A. Letsios, (Non-) unitarity of strictly and partially massless fermions on de Sitter space,
JHEP, 2023(5), 1-34 (2023).
59. G. Şengör, Searching for discrete series representations at the late-time boundary of de Sitter,
International Workshop LIE THEORY AND ITS APPLICATIONS IN PHYSICS. Singapore:
Springer Nature Singapore, (2023).
60. J.-P. Gazeau, H. Pejhan, Unified framework for graviton, partially massless graviton, and
photon fields in de Sitter spacetime under the conformal symmetry, Phys. Rev. D, 111. 105003
(2025).
61. J.-P. Gazeau, H. Pejhan, A misleading naming convention: de Sitter ‘tachyonic’ scalar fields,
Found. Phys., 55, 8 (2025).
62. M. Botshekananfard, E.B Güraksın, and G. Şengör, Ladder operators of the de Sitter algebra,
arXiv preprint arXiv:2510.05735 (2025).
63. K. Farnsworth, K. Hinterbichler, S. Saha, Hidden conformal symmetry of the discrete series
scalars in dS2 , Phys. Rev. D, 111(10), 105002 (2025).
64. E. Huguet, J. Queva, J. Renaud, FLRW embeddings in R𝑛+2 , differential geometry and conformal photon propagator, arXiv preprint arXiv:2512.10901 (2025).
65. T.S. Bunch, P.C.W. Davies, Quantum field theory in de Sitter space: renormalization by
point-splitting, Proc. R. Soc. Lond. A, 360, 117 (1978).
66. N.D. Birrell, P.C.W. Davies, Quantum Fields in Curved Space, Cambridge University Press,
(1984).
67. B. Allen, Vacuum states in de Sitter space, Phys. Rev. D, 32, 3136 (1985).
68. J. Bros, J.-P. Gazeau, U. Moschella, Quantum field theory in the de Sitter universe, Phys. Rev.
Lett., 73, 1746 (1994).
69. J. Bros, U. Moschella, Two-point functions and quantum fields in de Sitter universe, Rev. Math.
Phys., 08, 327 (1996).
70. J. Bros, H. Epstein, U. Moschella, Analyticity properties and thermal effects for general
quantum field theory on de Sitter space-time, Commun. Math. Phys., 196, 535 (1998).
71. J. Bros, H. Epstein, U. Moschella, The lifetime of a massive particle in a de Sitter universe,
JCAP 003, 02 (2008).
72. D. Marolf, I.A. Morrison, Infrared stability of de Sitter QFT: Results at all orders, Phys. Rev.
D, 84(4), 044040 (2011).
73. J.-P. Gazeau, H. Pejhan, Matter-antimatter (a)symmetry in de Sitter Universe, EPL., 148 59001
(2024).
74. T. Basile, E. Joung, K. Mkrtchyan, and M. Mojaza, Spinor-helicity representations of particles
of any mass in dS4 and AdS4 spacetimes. Phys. Rev. D, 109(12), 125003 (2024).
75. J. Penedones, K. Salehi Vaziri, Z. Sun, Hilbert space of Quantum Field Theory in de Sitter
spacetime, Phys. Rev. D, 111(4), 045001 (2025).
76. A. Higuchi, V.A. Letsios, Unitary rigid supersymmetry for the chiral graviton and chiral
gravitino in de Sitter spacetime, arXiv preprint arXiv:2503.04515 (2025).
77. M. Kaplan, D. Marolf, X. Yu, and Y. Zhao, De Sitter quantum gravity and the emergence of
local algebras, JHEP, 2025(4), 1-47 (2025).

## PDF page 157

References

143

78. P. Dey, Z. Huang, and A. Lipstein, de Sitter locality from conformal field theory, arXiv preprint
arXiv:2508.15627 (2025).
79. S.B. Giddings, Quantum gravity observables: observation, algebras, and mathematical structure, arXiv preprint arXiv:2505.22708 (2025).
80. M. Cirafici, Gravitational algebras and applications to nonequilibrium physics, Universe,
11(1), 24 (2025).
81. H. Verlinde, M. Zhang, SYK correlators from 2D Liouville-de Sitter gravity, JHEP, 2025(5),
1-28 (2025).
82. G. Roos, Exceptional symmetric domains, in Bruce Guilling et al. (ed), Symmetries in Complex
Analysis, AMS, Contemporary Math., 468, 157-189 (2008); arXiv:0801.4076.
83. M. Dubois-Violette, Exceptional quantum geometry and particle physics, Nucl. Phys., 912,
426-444 (2016).
84. I. Todorov, S. Drenska, Composition algebras, exceptional Jordan algebra and related groups,
JGSP, 46, 59-93 (2017).
85. I. Todorov, S. Drenska, Octonions, exceptional Jordan algebra, and the role of the group F4
in particle physics, Adv. in Appl. Clifford Alg., 28, 82 (2018).
86. W.D. Smith, Quaternions, octonions, and now, 16-ons, and 2n-ons; New kinds of numbers,
Book, under review for publication (2004).
87. J. Baez, The octonions, Bull. Amer. Math. Soc., 39:2, 145-205, (2002); Errata, ibid., 42, 213
(2005); math/0105155v4 [math.RA].
88. J. Baez, The tenfold way; for a brief overview see Notices Amer. Math. Soc. 67:10, 1599-1601
(2020); arXiv:2011.14234; see also Ten-fold way in nLab (April 2023).
89. I. Todorov, Octonion internal space algebra for the Standard Model, Universe 9(5), 222 (2023).
90. I.E. Segal, Mathematical problems of relativistic physics, American Mathematical Soc., Vol.
2 (1963).
91. L.K. Hua, Harmonic Analysis of Functions of Several Complex Variables in the Classical
Domains, American Mathematical Society, Providence, R.I., (1963).
92. I.I. Piatetski-Shapiro, Automorphic Functions and the Geometry of Classical Domains, Gordon
and Breach (1969).
93. J. Dixmier, Représentations intégrables du groupe de De Sitter, Bull. Soc. Math. Fr., 89, 9
(1961).
94. R. Takahashi, Sur les représentations unitaires des groupes de Lorentz généralisés, Bull. Soc.
Math. Fr., 91, 289 (1963).
95. J. Mickelsson, J. Niederle, Contractions of representations of de Sitter groups, Commun.
Math. Phys., 27, 167 (1972).
96. T. Garidi, E. Huguet, J. Renaud, de Sitter waves and the zero curvature limit, Phys. Rev. D,
67, 124028 (2003).
97. M. Mizony, 3 Semi-groupes de causalité et formalisme hilbertien de la mécanique quantique,
Publ. Dep. Math. Lyon 3B, 47 (1984).
98. M. Stener, Moufang Loops: General theory and visualization of non-associative Moufang
loops of order 16, Uppsala University Thesis (2016).
99. C. Furey, Standard model physics from an algebra? arXiv:1611.09182 (2016).
100. K. Krasnov, Geometry of Spin(10) symmetry breaking, arXiv:2209.05088v2 (see Sect. 2.7).
101. J.-P. Gazeau, A Mnemonic Matrix Rule for (Split) Octonionic Multiplication and its Extension
to the Cayley-Dickson Tower, arXiv preprint arXiv:2512.22134 (2025).
102. I. Yokota, Exceptional Lie groups, arXiv: 0902.0431 (2009).
103. S.R. Bryant, Notes on spinors in low dimensions, arXiv: 2011.05568 (2020).
104. P. Budinich, A. Trautman, The Spinorial Chessboard, Trieste Notes in Physics, Springer
(1988); Fock space description of simple spinors, J. Math. Phys., 30, 2125-2131 (1989).
105. M. Dubois-Violette, Complex structures and the Elie Cartan approach to the theory of spinors,
Spinors, Twistors, Clifford Algebras and Quantum Deformations: Proceedings of the Second
Max Born Symposium held near Wrocław, Poland, September (1992). Dordrecht: Springer
Netherlands (1993).
106. I. Todorov, The lure of conformal symmetry, Bulg. J. Phys., 46, 117-133 (2019).

## PDF page 158

144

4 Conformal Massless Low Helicity Fields and their de Sitter (dS) Spacetime Restriction

107. I.E. Segal, Covariant chronogeometry and extreme distances. III Macro-micro relations, Int.
J. Theor. Phys., 21, 851-869 (1982).
108. J. Schwinger, Angular momentum, In Quantum Mechanics: Symbolism of Atomic Measurements (pp. 149-181). Berlin, Heidelberg: Springer Berlin Heidelberg (1952).
109. I. Todorov, Infinite dimensional Lie algebras in conformal QFT models, in: A.O. Barut, H.D.
Doebner (eds.), Conformal Groups and Related Symmetries. Physical Results and Mathematical Background, Lecture Notes in Physics 261, pp. 387-443, Springer, Berlin (1986).
110. N.N. Bogoliubov, A.A. Logunov, A.I. Oksak, I.T. Todorov, General Principles of Quantum
Field Theory, Kluwer, Dordrecht et al., (1990); Russian original (1987).
111. R.F. Streater, A.S. Wightman, PCT, Spin and Statistics, and All That, Princeton University
Press (2000).
112. A. Uhlmann, Remarks on the future tube, Acta Phys. Pol., 24, 293 (1963); ibid. pp. 295-296.
113. N.M. Nikolov, Vertex algebras in higher dimensions and globally conformal invariant quantum field theory, Commun. Math. Phys., 253, 283-322 (2005); hep-th/030723.
114. N.M. Nikolov, I.T. Todorov, Rationality of conformally invariant local correlation functions on
compactified Minkowski space, Commun. Math. Phys., 218, 417-436 (2001); hep-th/0009004.
115. N.M. Nikolov, I. Todorov, Lectures on elliptic functions and modular forms in conformal field
theory, math-ph/0412039v2 (2005).
116. J.-P. Gazeau, The Language of Spheres in Physics, Universe, 10.3, 117 (2024).
117. S. Helgason, Differential geometry, Lie groups, and symmetric spaces, Vol. 80. Academic
Press (1979).
118. R. Penrose, W. Rindler, Spinors and space-time, Vol 2; Spinor and twistor methods in spacetime geometry. Vol. 2, Cambridge University Press (1984).
119. J. Faraut, A. Korányi, Analysis on symmetric cones, Oxford University Press (1994).
120. V. Bargmann, I. Todorov, Spaces of analytic functions on a complex cone as carriers for the
symmetric tensor representations of SO(𝑛), J. Math. Phys. 18, 1141-1148 (1977).
121. K. Farnsworth, K. Hinterbichler, O. Hulik, Scale and conformal invariance in (A)dS, Phys.
Rev. D, 110, 045011 (2024).

## PDF page 159

Glossary

Glossary of Clifford and Lie algebras used in the monograph, with precise nesting
and isomorphisms:
1. 𝔠𝔩(4, 2) is the 64-dimensional real associative Clifford algebra generated by 𝑚 𝜇 ,
𝜇 = 0, 5, 1, 2, 3, 4, as:
{
𝔠𝔩(4, 2) = span 1, 𝑚 𝜇 , 𝑚 𝜇𝜈 := 𝑚 𝜇 𝑚 𝜈 (𝜇 < 𝜈), 𝑚 𝜇 𝑚 𝜈 𝑚 𝜌 (𝜇 < 𝜈 < 𝜌), . . . ,
}
𝐸 := 𝑚 0 𝑚 5 𝑚 1 . . . 𝑚 4 ,
(4.51)
subject to the Clifford relations:
{
}
𝑚 𝜇 , 𝑚 𝜈 = 𝑚 𝜇 𝑚 𝜈 + 𝑚 𝜈 𝑚 𝜇 = 2𝜂 𝜇𝜈 1 ,

𝜂 𝜇𝜈 = diag(−1, −1, +1, +1, +1, +1) .
(4.52)

(
)
2. The even Clifford algebra 𝔠𝔩 even (4, 2)  𝔠𝔩(4, 1) is:
{
𝔠𝔩 even (4, 2) = span 1, 𝑚 𝜇𝜈 := 𝑚 𝜇 𝑚 𝜈 (𝜇 < 𝜈), 𝑚 𝜇 𝑚 𝜈 𝑚 𝜌 𝑚 𝜎 (𝜇 < 𝜈 < 𝜌 < 𝜎),
}
𝐸 := 𝑚 0 𝑚 5 𝑚 1 . . . 𝑚 4 ,
(4.53)
i.e., the 32-dimensional real subalgebra spanned by all products of an even
number of the generators 𝑚 𝜇 .
3. The bivectors 𝑚 𝜇𝜈 are closed under commutator and provide a spinorial realization of the conformal Lie algebra:
{
}
(
)
𝔰𝔲(2, 2)  𝔰𝔬(4, 2) = span 𝑚 𝜇𝜈 := 𝑚 𝜇 𝑚 𝜈 ⊂ 𝔠𝔩 even (4, 2) ,
(4.54)
[
]
with the Lie bracket given by 𝑚 𝜇𝜈 , 𝑚 𝜌 𝜎 computed inside 𝔠𝔩 even (4, 2).

145

## PDF page 160

146

Glossary

4. The pseudoscalar 𝐸 := 𝑚 0 𝑚 5 𝑚 1 . . . 𝑚 4 commutates with all bivectors 𝑚 𝜇𝜈
(
)
generating 𝔰𝔲(2, 2)
 𝔰𝔬(4, 2) . Hence, 𝐸 spans the central 𝔲(1) in the
extended conformal Lie algebra:
(
)
𝔲(2, 2)  𝔰𝔲(2, 2)  𝔰𝔬(4, 2) ⊕ 𝔲(1) ⊂ 𝔠𝔩 even (4, 2) .
(4.55)
(
)
5. The de Sitter (dS) algebra is realized as the subalgebra of 𝔰𝔲(2, 2)  𝔰𝔬(4, 2)
that preserves a fixed “5-direction” in the 6-dimensional space. Specifically:
{
}
(
)
𝔰𝔬(4, 1)  𝔰𝔭(2, 2) = span 𝑚 𝛼𝛽 := 𝑚 𝛼 𝑚 𝛽 ; 𝛼, 𝛽 = 0, 1, 2, 3, 4
⊂ 𝔰𝔲(2, 2) ⊂ 𝔠𝔩 even (4, 2) ,

(4.56)

with commutator taken inside 𝔠𝔩 even (4, 2). These bivectors 𝑚 𝛼𝛽 satisfy the
𝔰𝔬(4, 1) Lie algebra relations and provide a spinorial realization of the corresponding dS group Spin(4, 1)  Sp(2, 2).

## PDF page 161

Index

A
Algebra
Alternative
Clifford
Composition
Vertex
B
Basis
Cartan
Chiral
Majorana
Real
C
Conjugate
Cayley-Dickson
Charge
Complex
Hermitian
Octonionic
Cosmological Constant
E
Elementary System
Massless
Energy
Conformal
F
Field
Massless
Massless Scalar
Form
Bilinear

Volume
G
Group
Poincaré
Conformal
de Sitter
H
Hamiltonian
Conformal
Helicity
O
Octonion
Split
Operator
Annihilation
Casimir
Creation
Ladder
Lowering
Raising
Self-adjoint
Vertex
P
Parity
Q
Quaternion
R
Representation

147

## PDF page 162

148
Index
Ladder
Majorana
Massless
Subalgebra
Maximal Compact
<math>\mathbf{S}</math>
Space
<math>\mathbf{T}</math>
Conformal
Two-point function
de Sitter
Transformation
Euclidean
Similarity
Hilbert
Unitary
Minkowski
Compactified Minkowski
<math>\mathbf{V}</math>
Spin<br>Spinor<br>Chiral
Vacuum
Fock
