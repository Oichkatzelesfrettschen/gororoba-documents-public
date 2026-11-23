Source: https://zenodo.org/records/23451124/files/Functorial%20Layer-Collapse%20Law%20H;%20An%20Explicit%20Stratified%20Catalogue%20of%20Zero%20Divisors%20in%20the%20Trigintaduonions.pdf
PDF sha256: 60b10f4c51d51f6bee3297daf401a48e69bb58b9233d57551d7be8dc4169d78d
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of zhou_zhou_2026_functorial_layer_collapse_law_h_trigintaduonion_zero_divisors.pdf

Transcription of `zhou_zhou_2026_functorial_layer_collapse_law_h_trigintaduonion_zero_divisors.pdf` in this directory, 49 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-49 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Functorial Layer-Collapse Law H: An Explicit
Stratified Catalogue of Zero Divisors in the
Trigintaduonions
Zhou Changzheng, Zhou Ziqing
Email: ziqing-zhou@outlook.com
October 18, 2026
Abstract
The Cayley–Dickson tower starts from the real numbers and doubles successively; zero divisors first appear at the sedenion layer. Moreno gave a complete
criterion for this layer: a nonzero pair is a zero divisor if and only if its two components lie in the seven-dimensional purely imaginary octonion space, have equal
norm, and are orthogonal; the normalized locus is homeomorphic to the Stiefel
manifold V2 (R7 ). For the next algebra—the trigintaduonions A5 —the literature
provides general laws such as an upper bound for annihilator dimensions, divisibility of the dimension by four, and equality of left and right annihilators, as well as the
conclusion that the highest-dimensional zero-divisor locus is homeomorphic to the
disjoint union of two copies of V2 (R7 ); however, it does not give explicit coordinates
for the individual strata. In this paper we construct an explicit stratified catalogue
of zero divisors of A5 on the normalized Moreno-pair parameter space: stratified
by the dimension of the left annihilator, the stratum set covers {0, 4, 8, 12, 16},
the zero-divisor strata cover {4, 8, 12, 16}, and there are fourteen families in total
within the strata: five families in the 4-stratum, four in the 8-stratum, three in
the 12-stratum, and two in the 16-stratum. The two families in the top stratum
respectively realize explicit parameterizations of the two copies of V2 (R7 ) in the
BDI topological theorem; the parallel family in the 12-stratum gives a coordinate
realization of the BDI shape (a, ±i4 · a) under the multiplication convention of this
paper, with stratum dimension 12 (all registered probes have been hit; the general
structural proof remains to be built). For the axis family and the cross family we establish D1 –D2 type left-multiplication determinant laws and rigorously prove that
the vanishing of D2 is equivalent to the equal-norm orthogonality condition; this
zero criterion is restricted to the D1 D2 -type families parameterized by Moreno pairs
and is not extrapolated to a statement about the whole catalogue. All numerical
assertions are registered by exact integer arithmetic, reconciled through a primary
path of fraction-free elimination and a secondary path of two-prime modular rank;
the evidence is used at three levels: ironclad, census, and probe. Beyond the basic
seven families there exist explicit zero-divisor instances that do not belong to their
parameterization templates; hence the basic seven families are not complete. The
complete catalogue problem and the determinant exponents of unmeasured families
are registered as open problems.

Keywords: Cayley–Dickson algebras; trigintaduonions; zero divisors; annihilators; Stiefel
manifolds; stratified catalogue; determinant laws
1

## PDF page 2

1

Introduction

The Cayley–Dickson construction starts from the real numbers and doubles successively;
at each step one algebraic property is lost: from the reals to the complex numbers the
ordered-field structure is lost, from the complex numbers to the quaternions commutativity is lost, and from the quaternions to the octonions associativity is lost; at the
sedenions S, divisibility fails for the first time and zero divisors appear. Moreno (1998)
gave a complete algebraic criterion for zero divisors of S: a nonzero pair (a, b) ∈ S = O⊕O
is a zero divisor if and only if a, b ∈ Im O, ∥a∥ = ∥b∥, and ⟨a, b⟩ = 0; the normalized
zero-divisor locus is homeomorphic to the Stiefel manifold V2 (R7 ), of dimension 11, and
the annihilator dimension is constantly 4. This criterion turns the zero-divisor problem
for the sedenions from an algebraic condition into an explicit parameterization problem:
zero divisors no longer need to be checked one by one in a multiplication table, but are
parameterized by an ordered pair of orthogonal purely imaginary unit octonions.
For the next algebra A5 (the trigintaduonions, real dimension 32), the known results
in the literature are general laws rather than explicit objects. Biss, Dugger, and Isaksen
(2008) proved that for any nonzero zero divisor x, the dimension of its left annihilator is
at most 2n − 4n + 4, which for n = 5 gives the upper bound 16; the annihilator dimension
is always a multiple of 4; and the left and right annihilators are equal. Their topological
theorem further asserts that the highest-dimensional zero-divisor locus is homeomorphic
to the disjoint union of two copies of V2 (R7 ). However, which elements lie in which
stratum, and how each stratum can be written in explicit coordinates parameterized
by Moreno pairs, are questions to which the literature does not give a coordinate-level
answer. General laws give upper bounds and divisibility, but not the parameter spaces
of the individual strata; topological theorems give the topological type of the highestdimensional locus, but not coordinate realizations of the two copies. Between these two
types of conclusions there remains a gap for an explicit catalogue.
This paper fills this gap. Section 2 registers the machine-check ledger and evidence levels: kernel-dimension readings use fraction-free Gaussian elimination as the primary path
and two-prime modular rank as the secondary path for reconciliation; evidence is used at
three levels: ironclad, census, and probe. Section 3 fixes the Cayley–Dickson multiplication, conjugation, three-layer slot placement, and the normalized Moreno-pair parameter
space M , and states two classical anchors: the Moreno criterion and the BDI general laws.
Section 4 gives the explicit stratified catalogue: five families in the 4-stratum, four in the
8-stratum, three in the 12-stratum, and two in the 16-stratum, fourteen families in total;
the stratum set covers {0, 4, 8, 12, 16}, and the zero-divisor strata cover {4, 8, 12, 16}. The
top-stratum families F and F ′ respectively realize explicit parameterizations of the two
copies of V2 (R7 ) in the BDI topological theorem. Section 5 establishes D1 –D2 type leftmultiplication determinant laws for the axis and cross families, and proves that D2 = 0
is strictly equivalent to equal norm and orthogonality; this zero criterion is restricted
to the D1 D2 -type families parameterized by Moreno pairs, while the determinant types
of the parallel family, the double-two-slot family, and the mixed family are registered
separately. Section 6 treats the BDI interface and recomputes the stratum membership
of the parallel family: for the parallel family P (u, ε) = ((u, 0), (0, εu)), with arbitrary
nonzero purely imaginary octonion u and ε ∈ {+1, −1}, the left-annihilator dimension is
constantly 12, giving a coordinate realization of the BDI shape (a, ±i4 · a) under the multiplication convention of this paper. Section 7 registers the census protocol and golden
self-checks, and Section 8 summarizes the conclusions and open problems.
2

## PDF page 3

The relation of this paper’s catalogue to the classical literature is as follows. Moreno’s
criterion is the complete criterion for n = 4, and its normalized locus V2 (R7 ) is the common parameter space of the 4-, 8-, 12-, and 16-strata in this paper, each parameterized by
Moreno pairs. The general BDI laws provide three constraints: upper bound, divisibility,
and equality of left and right annihilators; all registered families in this paper’s catalogue are consistent with these three constraints. The BDI topological theorem asserts
two copies of V2 (R7 ); the families F and F ′ in this paper give their explicit coordinates;
but the topological theorem itself does not give parameterizations of the 4-, 8-, and 12strata, and the count of fourteen families in this paper is not automatically complete by
virtue of the topological theorem. Beyond the basic seven families there exists an explicit
zero-divisor instance: for the parallel family P (u, ε) = ((u, 0), (0, εu)), with arbitrary
nonzero purely imaginary octonion u and ε ∈ {+1, −1}, the left-annihilator dimension
is constantly 12, giving a coordinate realization of the BDI shape (a, ±i4 · a) under the
multiplication convention of this paper. This counterexample is registered at the ironclad level; the 8 × 8 symbolic-pattern probe is registered as a pending check item: its
pattern definition and counting convention are to be supplemented and reconciled by two
paths, and are listed in Section 2.3 as an absence registration; before the reconciliation
is complete, the probe reading is not entered into the ledger; the ledger basis for the
incompleteness of the basic seven families is the explicit parallel-family counterexample
(ironclad level), and does not depend on this probe. The complete catalogue problem—
whether there are zero divisors beyond the fourteen registered families, and whether the
full-type × half-type × slot-operation pattern is closed—is registered as an open problem.
The determinant exponents of unmeasured families, the non-D2 -type factorization of the
parallel family, and the stratified generalization to A6 and above are likewise registered
as open items.

2

Machine-Check Ledger and Verification Protocol

This chapter registers the verification environment, evidence levels, ledger entries, absence items, and protocol clauses for all machine-checkable assertions in the paper. The
ledger is disclosed before the main text in order to separate “reading source, reading path,
and reading boundary” from “mathematical conclusions”: any assertion about a family,
stratum membership, or dimension enters the main-text argument only after its verification path and evidence level have been registered. This chapter does not rely on public
benchmark datasets; all readings are produced by a reproducible protocol in exact integer
arithmetic, and the protocol parameters, sample sizes, random seeds, and evidence levels
are registered together. Floating-point readings are used only for cross-validation and
not as evidence.

2.1

Verification Environment and Evidence Grading

The multiplication table is generated recursively by the Cayley–Dickson doubling formula. Basis-vector products are represented exactly as “sign–index pairs”, with no floating point. After each layer is generated, spot checks of sign consistency and closure are
3

## PDF page 4

performed: the conjugate anti-automorphism holds on random samples; every basis product falls back into the index set of that layer; and the lower-layer multiplication tables
are aligned item by item with the standard relations for the quaternions and octonions
as external anchors.
Kernel-dimension readings use two paths. The primary path is fraction-free Gaussian
elimination, which reads the rank and kernel basis of the left-multiplication matrix directly; the secondary path is two-prime modular rank, with primes 109 + 7 and 109 + 9,
and the two paths are read separately and then reconciled. If the two paths disagree, a
single-path reading must not be entered into the ledger; an arbitration by kernel basis,
determinant, and construction-input assertions must be triggered. Protocol calibration
reading: for 30 random 32×32 integer matrices, the primary path of fraction-free elimination and the secondary path of two-prime modular rank agree case by case. This reading
only calibrates the protocol and is not evidence for the dimension of any family.
Determinant readings use fraction-free elimination as the primary method, with independent fraction-free LU decomposition or a computer algebra system as a supplementary
check. Bareiss-type readings that skip columns and destroy the divisibility invariant are
not used as sole evidence; if such a routine performs non-divisibility silent truncation, it
may produce readings inconsistent with the true kernel dimension, so it may be entered
into the ledger only when it agrees with at least two of fraction-free elimination, modular
rank, and kernel basis under arbitration.
This chapter uses three evidence levels.
Ironclad level: pointwise identities, explicit counterexamples, arbitrated stratummembership readings, or family actions with an identity proof. Ironclad-level readings
may be used directly as a basis for family actions, stratum membership, or condition
tightening, but unless a general proof is given they are not automatically upgraded to a
completeness theorem.
Census level: stable readings on exhaustive enumeration or registered-size random
samples, with the two paths agreeing; they support the stability of family dimensions and
the counting of stratum structure, but do not by themselves prove catalogue completeness.
Probe level: stable readings on small samples, used to locate families, identify
boundaries, and propose objects for census. Probe-level readings must not be used for
completeness conclusions; before finalization they must be upgraded to census level according to the registered sample size, and those not upgraded retain the label “census
pending” in the main text.
Figure 1: Verification pipeline and evidence levels.
Write ledger entry and
cite it in the main text

Sample and family
template parameters

Construction input assertions

Build left-multiplication
matrix Lx

Assign evidence level:
ironclad, census, probe

Secondary path: twoprime modular rank

Primary path: fractionfree elimination

Reconcile, arbitrate,
and register boundaries

Legend: blue boxes = data and construction steps; orange boxes = independent computation paths;
green box = evidence grading; purple boxes = registered outputs.

4

## PDF page 5

2.2

Ledger Entries

Entry 1 (Pass, census level): Multiplication-table structure test. On 600 random samples each for n = 4 and n = 5, the conjugate anti-automorphism, the flexibility
law, and power-associativity were tested with zero failures; on n = 3, the three forms
of alternativity were tested on 200 samples each with zero failures; on n = 4, a counterexample to alternativity appears, consistent with the classical conclusion that the
sedenions are non-alternative. This entry also serves as a detector for the correctness
of the multiplication-table assembly: if the multiplication table were misassembled, the
flexibility law would fail with frequency close to 1 on 32-dimensional random samples.
Entry 2 (Pass, census level): Golden self-check of the Moreno criterion
(n = 4). Purely imaginary equal-norm candidates are divided by support into singlesupport | single-support: 49 cases (ordered index pairs i, j ∈ {1, . . . , 7}: among them
all 42 cases with i ̸= j are zero divisors, and the 7 cases with i = j are invertible),
and double-support | double-support: 1764 cases (on each side, 42 signed double-support
elements ei ± ej , i < j), among which there are 882 zero divisors in the double-support
| double-support class. The two-way machine check “zero divisor implies orthogonality”
and “equal norm and orthogonality imply zero divisor” has zero exceptions within the
candidate classes; 500 strictly constructed equal-norm orthogonal samples are all zero
divisors with left-annihilator dimension exactly 4; the explicit kernel construction of
Moreno holds case by case under substitution. This entry provides a calibration anchor
for the n = 5 stratum-membership readings.
Entry 3 (Pass, census level, limited to registered samples): Stratified family
verification. For the basic seven families on registered parameter samples, the leftannihilator dimension readings agree case by case with an independent second path; the
two 16-stratum double families each hit 8 random Moreno pairs; for the 12-stratum cross
family, 42 unit pairs were read one by one, and the left-annihilator dimension is constantly
12; the 4-stratum double families and the two 8-stratum families have stable readings on
registered unit pairs and random pairs. Left- and right-annihilator dimensions were read
in pairs on all registered families and are equal case by case, consistent with the leftright annihilator identity conclusion in the general BDI laws. The “pass” of this entry is
limited to registered samples and does not constitute a completeness proof.
Entry 4 (Pass, census level): Independent verification of left-right annihilator identity. On all registered families, the left-annihilator dimension and the rightannihilator dimension were read separately and are equal case by case. This reading
shares the same dual-path reconciliation discipline as the rank readings of Entry 3.
Entry 5 (Assembly event, closed): Conflict in floating-point rank readings.
The initial pipeline once used floating-point elimination to read kernel dimensions; on
one 16-dimensional matrix, the floating-point reading judged it full rank while the determinant reading judged it singular, and the two conflicted. Arbitration located the cause
as pivot discrimination failing after intermediate quantities exceed 253 . Disposition: all
kernel dimensions were re-read by exact integer algorithms; the floating-point reading was
voided but not erased, and was registered in the ledger; floating-point rank writing into
the protocol was forbidden; the two-out-of-three cross-check of determinant, rank, and
kernel basis was listed as a fixed item. This event did not affect any ledger conclusion.
Entry 6 (Assembly event, closed): Index misalignment and dimension mismatch in coordinate placement functions. Disposition: all placement functions
were equipped with input dimension assertions and declared-condition assertions, includ-

5

## PDF page 6

ing purely imaginary, equal norm, orthogonality, and the Moreno condition; there was
zero recurrence thereafter. This event is registered as the motivation for the constructioninput assertion clauses.
Entry 7 (New families, incompleteness, and ironclad-level registration):
This entry is registered in four parts.
First, incompleteness registration. An explicit zero-divisor instance has been constructed that does not belong to the parameterization templates of the basic seven families. Take a nonzero purely imaginary octonion u; the element ((u, 0), (0, u)) has leftannihilator dimension 12; its first component is (u, 0) and its second component is (0, u),
which matches none of the templates: the ((a, 0), (b, 0)) template of the 12-stratum cross
family among the basic seven families, the 16-stratum F and F ′ templates, the 8-stratum
axis and diagonal family templates, and the 4-stratum double-family template (the 4stratum double-family template formally coincides with ((u, 0), (0, u)) at b = 0, but b = 0
does not satisfy the nonzero condition for Moreno pairs and is not in M ; this point is
not in the image set of the 4-stratum double families, so it does not constitute a match).
Hence “the basic seven families are complete” is false; the complete catalogue is open. In
addition, the 8 × 8 symbolic-pattern probe is registered as a pending machine-check item:
its pattern definition and counting convention remain to be supplementally registered,
and its reading is not entered into the ledger before the specification is supplemented and
dual-path recomputation is completed (see the absence registration in Section 2.3); the
ledger basis for incompleteness is the above parallel-family counterexample and does not
depend on this probe.
Second, probe-level registration of seven new families. G1 = ((a, b), (−b, −a)) and
G2 = ((a, b), (−a, b)) have left-annihilator dimension constantly 4 under Moreno-pair
parameters; G3 = ((a, b), (−a, −b)) is constantly 8; the second-slot axis family (0, (a, b)) is
constantly 8; the conditional profile of the mixed family ((a, 0), (0, b)) is: when norms are
equal and the pair is non-parallel, the left-annihilator dimension is 4; when parallel, the
left-annihilator dimension is 12 and the element is assigned to the parallel family; when
norms are unequal, it is invertible; the parallel family ((u, 0), (0, u)) has left-annihilator
dimension constantly 12 for any nonzero purely imaginary octonion u, and the readings
on five nonzero purely imaginary octonion probes are stable; the double-two-slot family
((0, a), (0, b)) has left-annihilator dimension constantly 12 when (a, b) is a Moreno pair.
The above readings are registered at probe level, and the sample sizes have not reached
the census threshold; before finalization, each family undergoes a census of no fewer than
8 random Moreno samples, and a 169-cell cross rescan, a binary-support full scan, and
determination of determinant exponents for the new families are performed.
Third, ironclad-level registration. First, family action: φ(u, v) = (u, −v) is an automorphism but does not interchange the 4-stratum double families; φ sends 4-stratum
family (i) to G1 and 4-stratum family (ii) to G2 . The automorphism identity and the
three family actions are template-level identities, with proof in Remark 4.1.1 of Chapter
4; 120 random samples are retained as assembly probes. Second, conditional reading
for the 12-stratum cross family: ((a, 0), (b, 0)) has left-annihilator dimension constantly
12 when (a, b) is a Moreno pair; the unequal-norm probes (e1 , 2e2 ), (2e1 , 3e2 ) and the
non-orthogonal equal-norm probe (3e1 + e2 , e1 + 3e2 ) are all invertible, so “the norms
need not be equal” cannot serve as a sufficient condition for this family. Third, stratummembership recomputation reading: both branches of ((u, 0), (0, ±u)) are constantly 12dimensional and are assigned to the parallel family; this reading agrees across fraction-free
elimination and two-prime modular rank on three paths. The above three items are iron6

## PDF page 7

clad level and may be used directly as the basis for the family-action remark in Chapter
4, the 12-stratum condition tightening in Chapter 4, and the stratum-membership recomputation in Chapter 6; the remaining new-family conclusions remain at probe level
until the census is completed.
Fourth, stratum-structure registration. Consistent with the stratified catalogue in
Chapter 4, the stratum set is {0, 4, 8, 12, 16}; the within-stratum family counts are: 5
families in the 4-stratum, 4 in the 8-stratum, 3 in the 12-stratum, and 2 in the 16stratum, fourteen families in total. This count is registered at census-pending level: the
family count itself is given by the definitions of the registered families, but “the full-type
× half-type cross combinations have not been fully scanned, and the catalogue may still
grow”, so the count is not a completeness theorem.

2.3

Absence Registration and Boundary Statements

The following items are registered as boundaries that must be completed or explicitly retained before finalization. First, the complete catalogue is not proved; the incompleteness
of the basic seven families already has an explicit counterexample, and whether there are
zero divisors beyond the seven new families is registered as an open problem. Second,
the census of no fewer than 8 random Moreno samples for each of the seven new families
is incomplete; the 169-cell cross rescan is incomplete; the binary-support full scan is incomplete; and the determinant exponents of the new families have not been determined.
Third, the supplemental registration of the pattern definition and counting convention
for the 8 × 8 symbolic-pattern probe is incomplete, and the reading of this probe is not
entered into the ledger (see Part 1 of Entry 7). Fourth, the stratified generalization to
A6 and higher dimensions has not been carried out. Fifth, closed-item registration: the
vector-by-vector verification of the 16-vector basis in Appendix D has been completed
(16/16, rank 16, including rows 10 and 11), and the F ′ basis is closed simultaneously via
slot swap; the step det Rm̄ = det Lm in E.1 has passed recomputation (8/8); the sample
evidence for the two determinant laws in Chapter 5 is registered as 30/30, 54/54, and
supplementary batches 8/8, 6/6 (same verification protocol, independent random seeds),
and general proofs remain to be built. The above two items are closed from the absence
list and are no longer listed as boundaries. Sixth, before the above completion, the newfamily content in Chapter 4 is registered at probe level and must not be upgraded to a
completeness theorem; the three ironclad-level items in Part 3 of Entry 7 are not subject
to this restriction.

2.4

Supplementary Protocol Clauses

Clause 1 (Dual-algorithm reconciliation of rank readings). Kernel dimensions and
rank readings must be read separately by the primary path of fraction-free elimination and
the secondary path of two-prime modular rank; they may be entered into the ledger only
when the two paths agree and pass arbitration by kernel basis or determinant. When the
two paths disagree, a single-path reading is forbidden as evidence for family dimension or
stratum membership. The motivation is the risk of silent truncation readings of the skipcolumn non-divisibility type: Bareiss-type routines, if they break the divisibility invariant
when skipping columns, may produce readings inconsistent with the true kernel dimension
by silent truncation; this risk has been registered as an assembly risk in kernel-dimension
7

## PDF page 8

readings and stratum-membership recomputations, hence a single Bareiss reading is no
longer used as the sole evidence.
Clause 2 (Construction input assertions). All family constructions execute input assertions before generating the left-multiplication matrix; the assertions include
dimension, purely imaginary, equal norm, orthogonality, the Moreno condition, and slot
placement. Those failing the assertions must not enter reading registration; those passing
the assertions register the assertion list and random seed.
Clause 3 (Two-out-of-three arbitration). When any two of the three readings—
determinant, rank, and kernel basis—agree and the third disagrees, the two agreeing paths
are used as the arbitration basis, and the failure mode of the third path is registered; when
all three disagree, the sample is voided and registered as an assembly event; majority vote
must not replace arbitration.
Clause 4 (Evidence levels and sample sizes). Each ledger entry registers the
evidence level, sample size, probe matrix, dual-path records, and random seed. Probelevel readings must not be used for completeness conclusions; census-level readings must
not automatically be upgraded to general proofs; ironclad-level readings without a general proof serve only as a basis for the catalogue and stratum membership, not as a
completeness theorem.
Clause 5 (Synchronization of determinant and annihilator). Determinant
readings must be registered in synchronization with rank and kernel-basis readings; the
zero characterization of D2 must be compared sample by sample with the Moreno condition. When the determinant is zero but the rank reading is nonsingular, handle it by
the conflict arbitration of Entry 5; when the determinant is nonzero but the construction
input claims a zero divisor, the construction input is voided and registered as an assembly
event.
Clause 6 (Verification workflow). Execute the following workflow for each registered family. Step 1: recursively generate the multiplication table and spot-check sign
consistency and closure. Step 2: generate construction inputs and execute the assertions
of Clause 2. Step 3: generate the left-multiplication matrix and read the rank and kernel
basis by fraction-free Gaussian elimination. Step 4: re-read by two-prime modular rank
and reconcile according to Clauses 1 and 3. Step 5: read the determinant by fractionfree elimination and verify by independent fraction-free LU or a computer algebra system;
compare the zeros of D2 with the Moreno condition. Step 6: register readings, sample size,
evidence level, random seed, and arbitration records. Step 7: probe-level readings enter
the pending-census list; census-level readings enter stable conclusions in the main text;
ironclad-level readings enter family-action, stratum-membership, or condition-tightening
entries. This workflow does not depend on external code libraries; multiplication-table
generation, fraction-free elimination, modular-rank reading, determinant verification, and
arbitration registration are all implemented in exact integer arithmetic, and the protocol
is fully replayable once the random seed is registered.

3

Notation and Classical Anchors

This chapter fixes the algebraic tower, multiplication convention, basis numbering, slot
placement, annihilator notation, and stratum terminology used throughout the paper, and
8

## PDF page 9

states three anchors provided by classical results: the Moreno criterion for sedenion zero
divisors, the general annihilator-dimension law, and the upper-bound structure in which
the stratum dimension is divisible by 4. This chapter only establishes the definitions and
condition boundaries on which the subsequent chapters depend; the explicit stratified
catalogue, determinant laws, and topological interface are developed in Chapters 4–6
respectively. The machine-check readings cited in this chapter are used according to the
evidence levels registered in Chapter 2, and probe-level readings are not upgraded to
general proofs.

3.1

The Cayley–Dickson Tower and Multiplication Convention

Take the Cayley–Dickson tower
A0 = R,

A1 = C,

A2 = H,

A3 = O,

A4 = S,

A5 = S ⊕ S,

where A4 is the sedenion algebra and A5 is the trigintaduonion algebra. For any elements
(a, b) and (c, d) in Ak , the multiplication on Ak+1 = Ak ⊕ Ak is defined as
(a, b)(c, d) = (ac − ¯
db, da + bc̄),
and conjugation is defined as
inv(a, b) = (ā, −b).
This multiplication is linear in each component separately but is not associative; the
flexibility law holds at every layer. The unit of A0 is denoted by 1. The basis vectors
of Ak are recursively numbered e0 , . . . , e2k −1 ; when Ak+1 is obtained by doubling Ak , the
new basis vectors satisfy
i = 0, . . . , 2k − 1.

e2k +i = (0, ei ),

Thus the basis of A4 = S is e0 , . . . , e15 , where e0 = 1 and e8 = (0, 1) is the companion
unit at the S layer; the basis of A5 is e0 , . . . , e31 , where e16 = (0, e0 ) is the companion
unit at the A5 layer. All multiplication tables in this paper are generated recursively by
the above doubling formula, and basis products are represented exactly as “sign–index
pairs”; all readings involving kernel dimensions, ranks, and determinants are registered
in exact integer arithmetic according to the protocol of Chapter 2.

3.2

Three-Layer Index Structure and Slot Placement

An element of A5 is written as (m1 ; m2 ), where m1 , m2 ∈ S. Call m1 the first A5 component and m2 the second A5 component. The first component m1 occupies indices 0
through 15, and the second component m2 occupies indices 16 through 31. An element
of S is written as (x, y), where x, y ∈ O. Call x the first S slot and y the second S slot.
The O basis of the first S slot occupies indices 0 through 7, and the O basis of the second
S slot occupies indices 8 through 15; indices 0 and 8 are the units of the two O slots, and
the purely imaginary indices are 1 through 7 and 9 through 15 respectively.
The internal layout of the second A5 component m2 is the same as that of S, shifted
overall by 16: the first S slot of m2 occupies indices 16 through 23, where 16 is the unit
9

## PDF page 10

and 17 through 23 are purely imaginary indices; the second S slot of m2 occupies indices
24 through 31, where 24 is the unit and 25 through 31 are purely imaginary indices.
This yields two types of placement that are easily confused but must be distinguished.
The first type is a Moreno pair (a, b) in S. Here a ∈ O is placed in the first S slot and
b ∈ O is placed in the second S slot. If a = ei , b = ej , i, j ∈ {1, . . . , 7}, then the index
support of (a, b) in S is {i, 8 + j}; for example, the support of (e1 , e2 ) is {1, 10}.
The second type is a cross-type element ((a, 0), (b, 0)) in A5 . Here a ∈ Im O is placed
in the first S slot of the first A5 component, and b ∈ Im O is placed in the first S slot
of the second A5 component. If a = ei , b = ej , then its index support is {i, 16 + j}; for
example, the support of ((e1 , 0), (e2 , 0)) is {1, 18}. The index 16 + j of b falls in the first
S slot of the second A5 component, not in the second S slot of the first A5 component.
Whenever this paper writes “the second slot of a Moreno pair”, it means the second S
slot inside S; whenever it writes “the first slot of the second A5 component”, it means
the first S slot of m2 . The two types of slots are not interchangeable.
When constructing families in this paper, all inputs execute the assertions listed in
Clause 2 of Chapter 2 before generating the left-multiplication matrix: dimension assertion, purely-imaginary assertion, equal-norm assertion, orthogonality assertion, Morenocondition assertion, and slot-placement assertion. Those failing the assertions do not
enter reading registration.

3.3

Inner Product, Norm, and Moreno Pairs

On the purely imaginary subspace Im O of O, take the Euclidean inner product ⟨·, ·⟩ and
norm ∥·∥. Im O is a 7-dimensional real vector space. Define the set of normalized Moreno
pairs
M = {(a, b) : a, b ∈ Im O, ∥a∥ = ∥b∥ = 1, ⟨a, b⟩ = 0}.
Pairs in M are called normalized Moreno pairs. Define the set of non-normalized equalnorm orthogonal pairs
M+ = {(a, b) : a, b ∈ Im O, ∥a∥ = ∥b∥ > 0, ⟨a, b⟩ = 0}.
The map
R>0 × M → M+ ,

(t, a, b) ↦→ (ta, tb)

is a bijection: given (a, b) ∈ M+ , let t = ∥a∥ = ∥b∥ > 0; then (t−1 a, t−1 b) ∈ M . Hence
M+ is the positive-scaling homogenization of M .
The dimension calculation is as follows. In M , a belongs to the unit sphere in Im O,
which has dimension 6; after fixing a, b belongs to the intersection of the orthogonal
complement of a in Im O with the unit sphere, which has dimension 5. Hence dim M =
6+5 = 11. M is homeomorphic to the Stiefel manifold V2 (R7 ): regard (a, b) as an ordered
pair of orthogonal unit vectors in R7 . The dimension of M+ is 1 + 11 = 12; the extra 1
dimension is the positive-scaling direction.
Convention: whenever this paper says a family is “parameterized by Moreno pairs”,
the parameter space means the normalized parameter space M ; the family image is
homogeneous under positive scaling. Non-normalized equal-norm orthogonal pairs are
assigned to the same family via positive scaling. This convention is consistent with the
later statement that “the parameter space is of V2 (R7 ) type and has dimension 11”; the

10

## PDF page 11

space of non-normalized pairs itself has dimension 12 and must not be confused with the
dimension of the normalized parameter space.
Homogeneity gives a strict conclusion: if (a, b) ∈ M+ and t > 0, then in S
AnnL (ta, tb) = AnnL (a, b),

AnnR (ta, tb) = AnnR (a, b).

The proof follows directly from bilinearity of multiplication: for any (u, v) ∈ S,
(ta, tb)(u, v) = t · ((a, b)(u, v)),
so (ta, tb)(u, v) = 0 if and only if (a, b)(u, v) = 0; the right annihilator is analogous.
Hence the annihilator dimension and stratum membership depend only on the normalized
representative (a, b) ∈ M . This conclusion is a strict equality, not a sampling reading.

3.4

Annihilators and Stratum Terminology

For x ∈ An , define the left annihilator and right annihilator
AnnL (x) = {y ∈ An : xy = 0},

AnnR (x) = {y ∈ An : yx = 0}.

Both are real linear subspaces of An . Within the applicability range of the general BDI
laws stated in Section 3.5, for a nonzero zero divisor x one has AnnL (x) = AnnR (x);
in this case write Ann(x) uniformly and write d(x) = dim Ann(x). All “annihilator
dimension” readings in this paper, unless explicitly said to be right-annihilator readings,
mean left-annihilator dimension; when left and right are equal, no distinction is made.
For nonzero x ∈ An , d(x) = 0 if and only if x is invertible, i.e., x is not a zero divisor.
Call d(x) the stratum dimension of x. Define the zero-divisor stratum set
Dn = {d(x) : x ∈ An , x ̸= 0, x is a zero divisor},
and define the full stratum set
Dn0 = {0} ∪ Dn .
The stratum set {0, 4, 8, 12, 16} in the stratum structure of Chapter 4 means the full
stratum set D50 ; the 0-stratum consists of nonzero invertible elements and does not belong to the zero-divisor stratum D5 . The zero element is not included in the stratum
classification: the annihilator of 0 is all of An , with dimension 2n , which does not satisfy
the upper-bound condition for nonzero zero divisors. The stratum-set inclusion in the
general BDI laws concerns only Dn , not Dn0 ; after adding the 0-stratum, the inclusion is
written Dn0 ⊆ {0, 4, 8, 12, 16}.

3.5

Classical Anchor I: The Moreno Criterion

In S = A4 , a nonzero pair (a, b) ∈ S is a zero divisor if and only if
a, b ∈ Im O,

∥a∥ = ∥b∥,

⟨a, b⟩ = 0.

Equivalently, the nonzero zero divisors are exactly the pairs in M+ . After normalization,
the zero-divisor locus is M , homeomorphic to V2 (R7 ), of dimension 11. For every (a, b) ∈
M+ , the left-annihilator dimension in S is 4, and the left and right annihilators are equal:
dim AnnL (a, b) = dim AnnR (a, b) = 4.
11

## PDF page 12

This conclusion also holds for non-normalized equal-norm orthogonal pairs, by the homogeneity of Section 3.3. The Moreno criterion is the complete criterion for n = 4: it
gives both directions “zero divisor implies equal norm and orthogonality” and “equal
norm and orthogonality imply zero divisor”. The golden self-check readings registered in
Entry 2 of Chapter 2—all 882 candidate zero divisors fall under the criterion, and 500
strictly constructed equal-norm orthogonal samples have annihilator dimension exactly
4—are used as census-level evidence, as calibration anchors for the multiplication table
and placement conventions, and do not replace the classical criterion itself.
The three conditions in the Moreno criterion—purely imaginary, equal norm, and
orthogonal—are all indispensable. If a or b has a real part, the corresponding element of
S is invertible; if ∥a∥ ̸= ∥b∥, the corresponding element of S is invertible; if ⟨a, b⟩ ̸= 0,
the corresponding element of S is invertible. The condition “nonzero” cannot be removed
either: a = b = 0 gives the zero element, which is not a zero divisor. The equal-norm
condition only fixes the two norms to be equal and does not fix the common scale; the
common scale is handled separately by the positive-scaling parameter of Section 3.3.

3.6

Classical Anchor II: General BDI Laws and the n = 5 Stratum Structure

For any nonzero zero divisor x in An , the general BDI laws give
dim AnnL (x) = dim AnnR (x) ≤ 2n − 4n + 4,
and dim AnnL (x) is divisible by 4. For n = 4, the upper bound is 24 − 16 + 4 = 4,
consistent with the annihilator dimension 4 of the Moreno criterion. For n = 5, the
upper bound is 25 − 20 + 4 = 16, hence
D5 ⊆ {4, 8, 12, 16},
and therefore
D50 ⊆ {0, 4, 8, 12, 16}.
Chapter 4 gives explicit families and within-stratum counts on the stratum set {0, 4, 8, 12, 16};
this chapter only fixes the stratum terminology and the inclusion relations and does not
treat “the stratum set equals {0, 4, 8, 12, 16}” as a conclusion of this chapter. Whether
each nonzero value in the stratum set actually occurs is given by the explicit families
of Chapter 4; whether there are zero divisors outside the stratum set belongs to the
complete-catalogue problem and is not excluded by the BDI upper bound alone. The
BDI upper bound excludes only strata greater than 16 and strata not divisible by 4;
it does not exclude the possibility that some stratum inside {4, 8, 12, 16} is empty; the
latter requires explicit construction.
The BDI topological theorem asserts that the highest-dimensional zero-divisor locus
is homeomorphic to the disjoint union of two copies of V2 (R7 ). This chapter only registers
the applicability range of this theorem: it concerns the highest-dimensional zero-divisor
stratum of A5 and does not directly give explicit coordinates for the individual strata;
explicit coordinatization is treated in Chapters 4 and 6. The three items—equality of left
and right annihilators, divisibility of the dimension by 4, and the upper bound 16—are
registered as census-level readings on all families of this paper’s catalogue according to
Entries 3 and 4 of Chapter 2; this chapter does not repeat these machine-check details.

12

## PDF page 13

3.7

Applicability Boundaries of the Anchors in This Chapter

The classical anchors of this chapter are used under the Cayley–Dickson doubling multiplication and the above conjugation convention. If the conjugation direction is changed or
the left-right positions of the two components in the multiplication formula are changed,
the statement form of the BDI theorem is unchanged, but the shape translation that
depends on the left-right multiplication direction of the companion unit changes; when
Chapter 6 handles this convention-layer interface, it takes the multiplication formula of
Section 3.1 and the slot placement of Section 3.2 as the sole baseline.
This chapter does not prove the complete catalogue of A5 zero divisors. The Moreno
criterion covers only n = 4; the general BDI laws give only the upper bound, divisibility,
and left-right equality, and do not give parameterizations of the individual strata. The
explicit families of Chapter 4, the determinant laws of Chapter 5, and the BDI interface
of Chapter 6 all take the terminology of this chapter as their baseline: “Moreno pair”
always means the normalized M of Section 3.3; “stratum dimension” always means d(x)
of Section 3.4; “left-annihilator dimension” always means the real dimension of AnnL (x);
and “second slot” always distinguishes, according to Section 3.2, the slot inside S from the
slot of an A5 component. The evidence levels of new families in subsequent chapters are
registered according to Entry 7 of Chapter 2; this chapter does not upgrade probe-level
readings to completeness conclusions.

4

Explicit Stratified Catalogue

This chapter constructs explicit families of A5 zero divisors on the normalized Morenopair parameter space M and stratifies them by left-annihilator dimension. Chapter 3 has
fixed: M is the set of ordered pairs of orthogonal unit vectors in Im O, of dimension 11,
homeomorphic to V2 (R7 ); non-normalized equal-norm orthogonal pairs are assigned to the
same family image via positive scaling; d(x) = dim AnnL (x) is the stratum dimension;
the zero-divisor stratum D5 is contained in {4, 8, 12, 16}, and the full stratum set D50
is contained in {0, 4, 8, 12, 16}. The family definitions in this chapter all use normalized
Moreno pairs (a, b) ∈ M as parameters; the family images are homogeneous under positive
scaling. “Constantly” means that the left-annihilator dimension readings are stable on
registered parameter samples and are labeled according to the evidence levels of Chapter
2; “invertible” means that the left-multiplication operator is nonsingular, equivalently
d(x) = 0.
The families of this chapter are organized by stratum as follows. The 4-stratum
(1)
(2)
families include the double families F4 , F4 , as well as G1 , G2 , and the equal-norm nonparallel branch of the mixed family; the 8-stratum families include the axis family, the
diagonal family, G3 , and the second-slot axis family; the 12-stratum families include the
cross family, the parallel family, and the double-two-slot family; the 16-stratum families
include F and F ′ . Within-stratum counts are summarized in Section 4.9; completeness
is not claimed in this chapter.

13

## PDF page 14

Figure 2: Strata and registered family templates in the explicit catalogue.
4-stratum families
(2)
(1)
F4 , F4
G1 , G 2
Mixed family H (equalnorm non-parallel)

8-stratum families
Axis family Ax
Diagonal family Dg
G3
Second-slot axis family Ax2

12-stratum families
Cross family C
Parallel family P
Double-two-slot family B

16-stratum families
Double family F
Double family F ′

Legend: boxes group families by left-annihilator dimension d(x); arrows indicate the increasing
stratum dimensions 4 → 8 → 12 → 16 used for the chapter organization.

4.1

Family Definitions and Verification Conventions

Let (a, b) ∈ M , and write m = (a, b) ∈ S. An A5 element is written as (m1 ; m2 ), with
m1 , m2 ∈ S. This chapter uses the following family templates.
(1)
(2)
4-stratum templates: F4 (m) = ((a, b), (b, a)); F4 (m) = ((a, b), (a, −b)); G1 (m) =
((a, b), (−b, −a)); G2 (m) = ((a, b), (−a, b)).
8-stratum templates: axis family Ax(m) = ((a, b), 0); diagonal family Dg(m) =
((a, b), (a, b)); G3 (m) = ((a, b), (−a, −b)); second-slot axis family Ax2 (m) = (0, (a, b)).
12-stratum templates: cross family C(m) = ((a, 0), (b, 0)); parallel family P (u, ε) =
((u, 0), (0, εu)), where u ∈ Im O is nonzero and ε ∈ {+1, −1}; double-two-slot family
B(m) = ((0, a), (0, b)).
16-stratum templates: F (m) = ((a, b), (b, −a)); F ′ (m) = ψ(F (m)), where ψ interchanges the two A5 components, i.e., ψ(u, v) = (v, u).
Mixed family H(a, b) = ((a, 0), (0, b)), where a, b ∈ Im O are nonzero and (a, b) ∈ M is
not required in advance; its stratum membership is registered according to the conditional
profile of Section 4.7.
(1)
(2)
Among the above templates, the parameter spaces of F4 , F4 , G1 , G2 , the axis
family, the diagonal family, G3 , the second-slot axis family, the cross family, the doubletwo-slot family, F , and F ′ are all M , of dimension 11. The parameter space of the
parallel family is the nonzero purely imaginary octonions modulo positive scaling, i.e.,
S 6 , of dimension 6; if the scale parameter is retained, the parameter space is Im O \ {0},
of dimension 7. The stratum dimension of the family image does not depend on the scale.
The parameter space of the mixed family is explained separately in Section 4.7.
The verification conventions are as follows. Each family executes the input assertions
of Clause 2 of Chapter 2 before generating the left-multiplication matrix; kernel dimensions are reconciled by the primary path of fraction-free elimination and the secondary
path of two-prime modular rank according to Clause 1 of Chapter 2; determinant, rank,
and kernel basis are arbitrated two-out-of-three according to Clause 3. Evidence levels
are used at the three levels of Section 2.1 of Chapter 2: ironclad level for family actions,
condition tightening, and stratum-membership recomputation; census level for dimension
stability and stratum counts on registered samples; probe level for conditional profiles
and families awaiting census, not upgraded to completeness conclusions.

4.2

The 4-Stratum Double Families and G1 , G2
(1)

(2)

Theorem 4.1 (4-stratum double families F4 , F4 ). For every (a, b) ∈ M , both
(1)
(2)
F4 (m) = ((a, b), (b, a)) and F4 (m) = ((a, b), (a, −b)) are zero divisors, and their left-

14

## PDF page 15

annihilator dimensions are constantly 4. The parameter spaces of both families are M ,
of dimension 11.
(1)
(2)
Verification registration: F4 and F4 have left-annihilator dimension readings constantly 4 on 42 unit Moreno pairs and 10 random Moreno pairs, registered at census
level according to Entry 3 of Chapter 2; the explicit kernel dimension 4 at the anchor
(a, b) = (e1 , e2 ) is registered according to Entry 2. General-proof status: the dimension
constancy of the two families on normalized Moreno parameters has not yet been written
as a parameter-by-parameter general proof; the registration in this section is used for
catalogue counting and does not by itself constitute a completeness theorem.
Remark 4.1.1 (Family action of φ). Define the A5 linear map φ(u, v) = (u, −v).
Then φ is an A5 algebra automorphism: for (a, b), (c, d) ∈ A5 ,
¯ da + bc̄) = (ac − db,
¯ −da − bc̄),
φ((a, b)(c, d)) = φ(ac − db,
and
¯ −da − bc̄),
φ(a, b) · φ(c, d) = (a, −b)(c, −d) = (ac − db,
so the two expressions are equal and φ preserves multiplication; φ also preserves conjugation and the unit, so the automorphism identity is an identity-level conclusion and
does not depend on sampling. The automorphism gives the conjugation relation for
left-multiplication operators Lφ(x) = φ ◦ Lx ◦ φ−1 , hence for every x ∈ A5 ,
dim AnnL (φ(x)) = dim AnnL (x),
and this equality holds pointwise for every parameter. The registered readings on 120
random samples are retained as assembly probes (Entry 7 of Chapter 2). The family
action of φ is, within the verified range, three template-level identities holding parameter
by parameter:
(1)

φ(F4 (m)) = ((a, b), −(b, a)) = ((a, b), (−b, −a)) = G1 (m);
(2)

φ(F4 (m)) = ((a, b), (−a, b)) = G2 (m);
φ(Dg(m)) = ((a, b), (−a, −b)) = G3 (m).
(1)

(2)

(2)

(2)

φ does not interchange F4 and F4 : F4 (m) = ((a, b), (a, −b)), while φ(F4 (m)) =
(1)
(2)
G2 (m) ̸= F4 (m), so the template ((a, b), (a, −b)) of F4 cannot be rewritten as ((a, b), (−a, b)).
The images of the remaining families under φ are registered per family as pending census
items and are not written as a general conclusion in this section.
Theorem 4.2 (4-stratum families G1 , G2 ). For every (a, b) ∈ M , both G1 (m) =
((a, b), (−b, −a)) and G2 (m) = ((a, b), (−a, b)) are zero divisors, and their left-annihilator
dimensions are constantly 4; the parameter space is M , of dimension 11. G1 and G2
(1)
(2)
are obtained by applying φ to F4 and F4 respectively; by the conjugation relation
(1)
of Remark 4.1.1, dim AnnL (G1 (m)) = dim AnnL (F4 (m)) and dim AnnL (G2 (m)) =
(2)
dim AnnL (F4 (m)) are strict equalities, so the stratum membership and dimension of
G1 and G2 are completely at the same level as the double families of Theorem 4.1, and
this conclusion does not depend on sampling. Verification registration: G1 and G2 have
left-annihilator dimension readings constantly 4 on 2 to 5 Moreno probe samples, retained
as assembly records; before finalization, according to Entry 7 of Chapter 2, a census of
no fewer than 8 random Moreno samples is performed on the direct readings.

15

## PDF page 16

4.3

The 8-Stratum Families

Theorem 4.3 (Three 8-stratum families: axis, diagonal, and G3 ). For every (a, b) ∈ M , the axis family Ax(m) = ((a, b), 0), the diagonal family Dg(m) =
((a, b), (a, b)), and G3 (m) = ((a, b), (−a, −b)) are all zero divisors, and their left-annihilator
dimensions are constantly 8; the parameter space of all three families is M , of dimension
11.
The dimension 8 of the axis family has a block-structure proof. Let x = (m, 0) ∈ S⊕S,
m = (a, b). For any (p, q) ∈ S ⊕ S, by the doubling multiplication
(m, 0)(p, q) = (mp, qm).
Hence (p, q) ∈ AnnL (x) if and only if p ∈ AnnL (m) and q ∈ AnnR (m). By the Moreno
criterion, dim AnnL (m) = dim AnnR (m) = 4, so dim AnnL (x) = 4 + 4 = 8. This proof
holds for every m ∈ M+ and does not depend on sampling; positive scaling does not
affect the annihilator, so it holds for normalized M . The axis family is registered as a
strict proof.
The dimension 8 of the diagonal family has stable readings on 8/8 random Moreno
pairs and registered unit pairs, registered at census level according to Entry 3 of Chapter
2; the direct reading of G3 is registered at probe level according to Entry 7 of Chapter 2,
and its stratum membership and dimension are at the same level as the diagonal family
via the following inheritance relation. The general proof remains to be built. G3 is
obtained from φ(Dg); by the conjugation relation of Remark 4.1.1, dim AnnL (G3 (m)) =
dim AnnL (Dg(m)) is a strict equality, so the stratum membership and dimension of G3 are
completely at the same level as the diagonal family; this inheritance relation is registered
at ironclad level, but the dimension status of the diagonal family itself remains at census
level.
Theorem 4.4 (Second-slot axis family). For every (a, b) ∈ M , Ax2 (m) =
(0, (a, b)) is a zero divisor, and its left-annihilator dimension is constantly 8; the parameter space is M , of dimension 11.
Proof. Let x = (0, m), m = (a, b). For any (p, q) ∈ S ⊕ S, by the doubling multiplication
(0, m)(p, q) = (−q̄m, mp̄).
Hence (p, q) ∈ AnnL (x) if and only if q̄m = 0 and mp̄ = 0. The condition mp̄ = 0 is
equivalent to p̄ ∈ AnnL (m), i.e., p runs through the conjugate image of AnnL (m), of
dimension 4; the condition q̄m = 0 is equivalent to q̄ ∈ AnnR (m), i.e., q runs through
the conjugate image of AnnR (m), also of dimension 4. The two conditions act on p and
q separately, so the kernel dimension is 4 + 4 = 8. This proof holds for every m ∈ M+ ;
positive scaling does not affect the annihilator. □
Verification registration: this family has readings constantly 8 on 2 to 5 Moreno probe
samples, registered at probe level according to Entry 7 of Chapter 2; the above block proof
gives the general dimension 8, consistent with the readings.

4.4

The 12-Stratum Families

Theorem 4.5 (Cross family C). Let (a, b) ∈ M and x = C(a, b) = ((a, 0), (b, 0)). Then
x is a zero divisor, and its left-annihilator dimension is constantly 12; the parameter space
is M , of dimension 11. The Moreno condition is necessary: if (a, b) has unequal norms
16

## PDF page 17

or is non-orthogonal, then x is invertible. Verification registration: for the 42 unit pairs
((ei , 0), (ej , 0)), i ̸= j, the left-annihilator dimension was read one by one and is constantly
12, registered at census level according to Entry 3 of Chapter 2; the unequal-norm probes
(e1 , 2e2 ), (2e1 , 3e2 ) and the non-orthogonal equal-norm probe (3e1 + e2 , e1 + 3e2 ) are all
invertible, registered at ironclad level according to Entry 7 of Chapter 2. Hence “the
norms need not be equal” cannot serve as a sufficient condition for this family; the
Moreno condition cannot be weakened to requiring only a ⊥ b or only equal norms.
General-proof status: the constancy of dimension 12 is census-level stable on registered
Moreno samples, and the parameter-by-parameter general proof remains to be built.
Remark 4.5.1 (Slots). In the cross family, the index of b is 16 + j, falling in the
first S slot of the second A5 component; in the Moreno pair (a, b), b lies in the second
S slot inside S, with index 8 + j. The two types of slots are distinguished according to
Section 3.2 of Chapter 3 and are not interchangeable.
Theorem 4.6 (Parallel family P and double-two-slot family B). The parallel
family P (u, ε) = ((u, 0), (0, εu)), where u ∈ Im O is nonzero and ε ∈ {+1, −1}, is a zero
divisor for every u and every ε, and its left-annihilator dimension is constantly 12. The
double-two-slot family B(m) = ((0, a), (0, b)), where (a, b) ∈ M , is a zero divisor, and its
left-annihilator dimension is constantly 12; the parameter space is M , of dimension 11.
Parameter space of the parallel family: the nonzero purely imaginary octonions modulo positive scaling form S 6 , of dimension 6; if the scale parameter is retained, the parameter space is Im O \ {0}, of dimension 7. The stratum dimension 12 of the family image
does not depend on the scale of u or the sign of ε. Verification registration: P (u, +1) and
P (u, −1) have left-annihilator dimension constantly 12 on five nonzero purely imaginary
octonion probes, agreeing across fraction-free elimination and two-prime modular rank
on three paths, registered at ironclad level according to Entry 7 of Chapter 2; this family
gives an explicit realization of the BDI shape (a, ±i4 · a) under the multiplication convention of this paper, with stratum membership in the 12-stratum. The general structural
proof remains to be built.
The double-two-slot family B has left-annihilator dimension constantly 12 on 2 to 5
probe samples under Moreno parameters, registered at probe level according to Entry 7
of Chapter 2; before finalization, a census of no fewer than 8 random Moreno samples is
performed. B and P are disjoint: the first A5 component of P is (u, 0), which is nonzero,
while the first A5 component of B is (0, a), whose first slot is zero.

4.5

Conditional Profile of the Mixed Family H

Theorem 4.7 (Mixed family H). Let a, b ∈ Im O be nonzero and x = H(a, b) =
((a, 0), (0, b)). Then the following conditional profile holds.
First, if ∥a∥ = ∥b∥ and b ̸= ±a (equal norm and non-parallel), then x is a zero divisor,
and its left-annihilator dimension is 4 on registered samples.
Second, if b = ±a (parallel), then x belongs to the parallel family P (a, ±1), and its
left-annihilator dimension is constantly 12, registered according to Theorem 4.6.
Third, if ∥a∥ ̸= ∥b∥ (unequal norms), then x is invertible, d(x) = 0.
Verification registration: the above three profiles are stable on 2 to 5 probe samples,
registered at probe level according to Entry 7 of Chapter 2; conditional completeness
(whether the equal-norm non-parallel case is exactly the 4-stratum, and whether there
are other subcases) is left to the open problems and is not upgraded to a general theorem

17

## PDF page 18

in this chapter. The parameter space of the equal-norm non-parallel branch of the mixed
family is the set of normalized equal-norm non-parallel pairs
MH = {(a, b) : a, b ∈ Im O, ∥a∥ = ∥b∥ = 1, b ̸= ±a},
of dimension 12; the non-normalized parameter space has dimension 13. Dimension
calculation: a ranges over unit vectors in Im O, giving 6 dimensions; b ranges over the
unit sphere in Im O with the two points ±a removed, and removing finitely many points
does not change the manifold dimension, so the direction of b contributes 6 dimensions;
the total is 12 dimensions, and retaining the scale adds 1 dimension. This branch is
counted as one family in the 4-stratum count; its parallel branch is assigned to P and is
not counted twice. MH is not V2 (R7 ), and its dimension is not 11.

4.6

The 16-Stratum Double Families

Theorem 4.8 (16-stratum double families F and F ′ ). For every (a, b) ∈ M , both
F (m) = ((a, b), (b, −a)) and F ′ (m) = ψ(F (m)), where ψ interchanges the two A5 components, are zero divisors, and their left-annihilator dimensions are constantly 16; the
parameter space of both families is M , of dimension 11. F and F ′ respectively realize
explicit parameterizations of the two copies of V2 (R7 ) in the BDI topological theorem. ψ
is not an A5 algebra automorphism, so F ′ is not the image of F under an algebra isomorphism; the two have the same dimension 16, and their loci are registered independently.
Verification registration: F and F ′ each have left-annihilator dimension readings constantly 16 on 8 random Moreno pairs and 10 unit pairs, and agree case by case with an
independent null-space routine, registered at census level according to Entry 3 of Chapter
2; the explicit 16-vector basis at the anchor (a, b) = (e1 , e2 ) is registered in Appendix D,
and the vector-by-vector verification has been closed (16/16, rank 16, Chapter 2 ledger).
General-proof status: the kernel construction of F has an explicit basis framework and has
been verified vector by vector; the parameter-by-parameter general proof remains to be
built; F ′ is obtained from ψ by slot swap, and the reading that ψ is not an automorphism
is registered according to the entries of Chapter 2.
Remark 4.8.1 (BDI interface). The stratum dimension 16 of F and F ′ is consistent
with the BDI upper bound 16; the parameter space M of the two families is homeomorphic
to V2 (R7 ), so the images of the two families respectively give coordinate realizations of
two copies of V2 (R7 ). This interface concerns only the highest-dimensional stratum and
does not concern the completeness of the 4-, 8-, and 12-strata.

4.7

Stratum Structure and Family Counts

Corollary 4.9 (Stratum structure). On the registered families, the stratum set is
{0, 4, 8, 12, 16}, where the 0-stratum consists of nonzero invertible elements and does not
belong to the zero-divisor stratum D5 ; the zero-divisor stratum D5 covers {4, 8, 12, 16}
on the registered families. The within-stratum family counts are counted according to
the following convention.
(1)
(2)
4-stratum: F4 , F4 , G1 , G2 , and the equal-norm non-parallel branch of the mixed
family H, 5 families in total. The parallel branch of the mixed family is assigned to the
parallel family and is not counted in the 4-stratum.
18

## PDF page 19

8-stratum: axis family Ax, diagonal family Dg, G3 , second-slot axis family Ax2 , 4
families in total.
12-stratum: cross family C, parallel family P , double-two-slot family B, 3 families in
total.
16-stratum: F , F ′ , 2 families in total.
(1)
Fourteen families in total. Parameter-space convention: the parameter spaces of F4 ,
(2)
F4 , G1 , G2 , Ax, Dg, G3 , Ax2 , C, B, F , F ′ are M , of dimension 11; the parameter
space of P is S 6 , of dimension 6 (dimension 7 with scale retained); the parameter space
of the equal-norm non-parallel branch of H is MH , of dimension 12 (dimension 13 with
scale retained). Hence “every family has an 11-dimensional parameter space” is false; the
family-by-family statement in this section is authoritative.
Evidence levels: the stratum set and family counts are given by the above family
definitions, registered at census-pending level according to Entry 7 of Chapter 2; the
non-emptiness of each stratum is guaranteed by explicit families. The full-type × halftype cross combinations have not been fully scanned, and the binary-support full scan
has not been carried out, so the catalogue may still grow; this corollary does not claim
a complete catalogue of A5 zero divisors. The completeness problem, together with the
169-cell cross rescan and the determination of determinant exponents for new families, is
registered as an open item.

4.8

Boundaries and Risks

The boundaries registered in this section are as follows. First, among the dimension
constancy results for the 4-stratum double families, G1 , G2 , the diagonal family, G3 ,
the cross family, the double-two-slot family, F , and F ′ , the axis family and the secondslot axis family have general block proofs, and G1 , G2 , and G3 have strict dimension
transfer via automorphism inheritance; the remaining families are at census or probe
level on registered samples, and parameter-by-parameter general proofs remain to be
built. Second, the 12-stratum reading of the parallel family is registered at ironclad level,
but the general structural proof remains to be built; its parameter space is stated as S 6
of dimension 6, or 7 with scale retained, and is not confused with the 11 dimensions of
M . Third, the conditional profile of the mixed family is at probe level, and conditional
completeness is left to the open problems; its equal-norm non-parallel branch is counted
in the 4-stratum family count, and its parallel branch is assigned to P and not counted
(1)
twice. Fourth, the family action of φ registers only the three verified identities F4 ↦→
(2)
G1 , F4 ↦→ G2 , and Dg ↦→ G3 (Remark 4.1.1); the images of the remaining families
under φ are registered per family as pending census items and are not written as a
general conclusion. Fifth, the stratum-structure count does not constitute a completeness
theorem; the complete-catalogue problem, the 169-cell cross rescan, the binary-support
full scan, and the determination of determinant exponents for new families are all retained
according to the absence registration of Chapter 2; the vector-by-vector verification in
Appendix D has been closed.

19

## PDF page 20

5

Determinant Laws and Zero Criteria

This chapter discusses the left-multiplication determinants of two types of explicit families
on the normalized Moreno-pair parameter space M . Chapter 3 has fixed: M is the set
of ordered pairs of orthogonal unit vectors in Im O, of dimension 11, homeomorphic to
V2 (R7 ); non-normalized equal-norm orthogonal pairs are assigned to the same family
image via positive scaling; d(x) = dim AnnL (x) is the stratum dimension. Chapter
4 has given the stratum catalogue: the axis family Ax(m) = ((a, b), 0) and the cross
family C(m) = ((a, 0), (b, 0)) lie in the 8- and 12-strata respectively; the conditional
profiles of the parallel family P (u, ε) = ((u, 0), (0, εu)), the double-two-slot family B(m) =
((0, a), (0, b)), and the mixed family H(a, b) = ((a, 0), (0, b)) are registered separately.
This chapter establishes D1 D2 -type determinant laws only for the axis and cross families;
the determination of determinant exponents for the remaining families is registered as
a pending item, and this chapter does not claim that a unified form covers the whole
catalogue.
All determinant readings in this chapter are registered according to the protocol of
Chapter 2: fraction-free elimination as the primary path, with independent fraction-free
LU decomposition or a computer algebra system as a supplementary check; determinant,
rank, and kernel basis are arbitrated two-out-of-three. Sample readings are used according
to the evidence levels of Chapter 2, and census-level samples are not upgraded to general
proofs.

5.1

Discriminants and Basic Identities

For a, b ∈ Im O, define

D1 (a, b) = ∥a∥2 + ∥b∥2 ,
D2 (a, b) = (∥a∥2 − ∥b∥2 )2 + 4⟨a, b⟩2 .

D1 is a positive-definite quadratic form, and D2 is a nonnegative quartic form. The zero
characterization of D2 is a strict algebraic identity:
D2 (a, b) = 0 if and only if ∥a∥2 = ∥b∥2 and ⟨a, b⟩ = 0.
The proof follows directly from the sum of two real squares: D2 is the sum of two real
square terms, so D2 = 0 if and only if both terms vanish simultaneously; the first term
vanishing gives ∥a∥2 = ∥b∥2 , and the second gives ⟨a, b⟩ = 0. This identity holds for
arbitrary a, b ∈ Im O and does not depend on the Moreno condition or on normalization.
When (a, b) ∈ M , D1 = 2 and D2 = 0; when (a, b) ∈ M+ with common scale t = ∥a∥ =
∥b∥, D1 = 2t2 and D2 = 0. The zero set of D2 records only “equal norm and orthogonal”
and does not record the common scale; the common scale is recorded by D1 .
The D1 D2 -type determinant law discussed in this chapter means: there exist nonnegative integers α, β such that for an element x in the family, det Lx = D1 (a, b)α · D2 (a, b)β .
Here Lx is the 32 × 32 real matrix of left multiplication by x on A5 , and a, b are the
two components taken from Im O in the family parameters. This form is defined only
for families parameterized by a pair (a, b) in Im O; the parallel family is parameterized
by a single u ∈ Im O \ {0}, and the double-two-slot family, although parameterized by
(a, b) ∈ M , has a different slot structure; whether these two fall into the D1 D2 type must
be determined separately and cannot be directly extrapolated from the formulas for the
axis and cross families.

20

## PDF page 21

5.2

Determinant Law for the Axis Family

Theorem 5.1 (Axis family). Let (a, b) ∈ M+ , m = (a, b) ∈ S, and x = Ax(m) =
((a, b), 0) ∈ A5 . Then the left-multiplication operator Lx is block diagonal:
Lx = diag(Lm , Rm ),
where Lm is the operator of left multiplication by m on S, and Rm is the operator
of right multiplication by m on S. The derivation follows directly from the doubling
multiplication: for (p, q) ∈ S ⊕ S, x(p, q) = (m, 0)(p, q) = (mp, qm), the first block is
p ↦→ mp, i.e., Lm , and the second block is q ↦→ qm, i.e., Rm . Therefore
det Lx = det Lm · det Rm .
By the conjugation anti-automorphism C(z) = z̄ satisfying CRm C −1 = Lm̄ , we have
det Rm = det Lm̄ ; when m is purely imaginary, m̄ = −m, and S is 16-dimensional of even
dimension, so det Lm̄ = det L−m = det Lm ; hence
det Lx = (D14 D22 )2 = D18 D24 .
Verification registration: this law holds exactly on 30 random Moreno samples, registered
at census level according to Entry 3 of Chapter 2. The block structure is a strict equality
holding for every m ∈ S and does not depend on sampling. The exponent substitution
depends on two steps: the S-layer formula det Lm = D14 D22 and det Rm = det Lm ; both
steps have received sample-level verification (30/30 or more and 8/8, Chapter 2 ledger),
so the status of Theorem 5.1 is: the block structure is strict; the exponents (8, 4) hold
at census level on registered samples; the parameter-by-parameter general proof is still
registered as open and is not closed in this chapter.
Applicability boundary: the template of this law is consistent with the axis family
Ax(m) = ((a, b), 0) of Chapter 4; a, b ∈ Im O, m = (a, b) ∈ S. If a or b has a real
part, then x no longer belongs to the Moreno-parameter image set of the axis family, D1
and D2 are still defined, but the zero-divisor condition is not characterized by D2 = 0
alone, and the zero-divisor interpretation of Theorem 5.1 does not apply. If (a, b) is
taken as a non-normalized equal-norm orthogonal pair, then D1 = 2t2 , D2 = 0, the
determinant is zero, consistent with the conclusion that positive scaling does not change
the annihilator dimension; the determinant formula substitutes the scales of D1 and D2
for non-normalized parameters as well.

5.3

Determinant Law for the Cross Family

Theorem 5.2 (Cross family). Let (a, b) ∈ M and x = C(a, b) = ((a, 0), (b, 0)) ∈ A5 .
Then
det Lx = D1 (a, b)4 · D2 (a, b)6 .
Verification registration: this law holds exactly on 54 samples, including 24 random
Moreno samples and 30 verification samples, registered at census level according to Entry 3 of Chapter 2. The family template is consistent with the cross family C(m) =
((a, 0), (b, 0)) of Chapter 4; the index of b is 16 + j, falling in the first S slot of the second
A5 component, not the second slot inside S. If the second component is written as (0, b),
what is obtained is the parallel/non-parallel branch of the mixed family H, which does
21

## PDF page 22

not belong to the cross family, and the formula of Theorem 5.2 makes no assertion about
that branch.
Applicability boundary: Theorem 5.2 requires (a, b) ∈ M , i.e., a, b ∈ Im O, equal
norm, and orthogonal; Section 4.4 of Chapter 4 has registered: if the norms are unequal or
the pair is non-orthogonal, then ((a, 0), (b, 0)) is invertible, d(x) = 0. Hence the Moreno
condition is a necessary condition for the zero-divisor property of this family; under
the Moreno condition D2 = 0, the determinant is zero, consistent with the zero-divisor
property. The exponents (4, 6) hold at census level on registered samples; the general
proof remains to be built and is not closed in this chapter. The left-multiplication operator
of the cross family is not block diagonal, and the origin of the exponents cannot be directly
extrapolated from the square structure of the axis family; its structural explanation is
registered as an open item.

5.4

Applicability Boundaries of the Zero Set of D2 and the ZeroDivisor Locus

Note 5.3 (Zero criterion). D2 = 0 is equivalent to a, b having equal norm and being
orthogonal; this equivalence is a strict identity. For the axis family Ax(m) and the cross
family C(m), the Moreno condition on the family parameters (a, b) is exactly D2 = 0
and a, b nonzero; hence within these two families, det Lx = 0 if and only if (a, b) satisfies
the Moreno condition, and the zero set of the determinant is synchronized with the zerodivisor locus within the family. This synchronization holds only for D1 D2 -type families
and cannot be extrapolated to a statement about the whole catalogue.
The parallel family P (u, ε) = ((u, 0), (0, εu)) consists of zero divisors with stratum
dimension 12, but its parameter is a single nonzero purely imaginary octonion u, not a
pair (a, b) ∈ M ; if one formally takes a = u, b = u, then D1 = 2∥u∥2 , D2 = 4∥u∥4 ,
D2 ̸= 0, while x is still a zero divisor. Hence the zero-divisor property of the parallel
family is not characterized by D2 = 0. The double-two-slot family B(m) = ((0, a), (0, b))
is parameterized by (a, b) ∈ M , D2 = 0, but its slot structure differs from those of the axis
and cross families, and whether its determinant decomposes as D1α D2β has not yet been
determined; one cannot assert that its determinant law is synchronized merely because
D2 = 0. The conditional profile of the mixed family H(a, b) = ((a, 0), (0, b)) is: 4-stratum
when equal norm and non-parallel, 12-stratum when parallel, and invertible when norms
are unequal; its zero-divisor condition is not a single D2 = 0, and its determinant type
has also not been determined.
Therefore, the applicability range of the unified form ∆ = D1α D2β is limited to families
parameterized by (a, b) ∈ M and already registered as D1 D2 type. For the parallel family,
the double-two-slot family, the mixed family, and the as-yet-undetermined 4-, 8-, and 16stratum families among the basic families, the determination of the exponents (α, β) and
the choice of discriminants are registered as open problems, and D2 = 0 is not used as
an a priori constraint.

5.5

List of Pending Determinations and Open Problems

The pending-determination list is registered family by family according to the stratum
catalogue of Chapter 4 as follows.

22

## PDF page 23

Axis family Ax and cross family C: the D1 D2 -type laws have been registered on
census-level samples; the exponent substitution for the axis family depends on the samplelevel verification of det Rm = det Lm (8/8, Chapter 2 ledger), and the general proof is
registered with Open Problem 2 of Chapter 8; the general proof for the cross family
remains to be built.
Families among the basic families whose determinant exponents have not yet been
(1)
(2)
determined: the 4-stratum double families F4 , F4 , the 8-stratum diagonal family Dg,
and the 16-stratum double families F and F ′ . Whether these families fall into the D1 D2
type, the values of the exponents (α, β), and whether the discriminant is still D2 all
remain to be determined.
Seven new families: G1 , G2 , G3 , the second-slot axis family Ax2 , the equal-norm nonparallel branch of the mixed family H, the parallel family P , and the double-two-slot
family B. Among them, G1 , G2 , G3 , and Ax2 are parameterized by M and can be tested
for the D1 D2 type first; the parameter space of the mixed family H is MH , of dimension
12, and its parallel branch is assigned to P ; the parallel family P is parameterized by
u ∈ Im O \ {0}, and the D1 D2 type requires a separate discriminant; the double-two-slot
family B is parameterized by M but has a different slot structure and must be determined
separately.
Open Problem 2 (Generalization of determinant types). Determine the leftmultiplication determinants of the above undetermined families. For families parameterized by M , test whether there exist nonnegative integers α, β such that det Lx = D1α D2β ;
if not, register their indecomposable factor structure. For the parallel family P , test
whether there exists a factorization expressed in terms of the norm of u and some quartic
invariant of u; D2 = 0 is not used as its zero-divisor discriminant. For the mixed family
H, determine the determinant behavior separately for the three branches: equal norm
and non-parallel, parallel, and unequal norm; the parallel branch is assigned to P and is
not counted twice. Closed-item registration: det Rm = det Lm has received sample-level
verification (8/8, Chapter 2 ledger), and its parameter-by-parameter general proof is registered together with this open problem. Before the above pending determinations are
completed, the exponent conclusions of Theorems 5.1 and 5.2 are used at census level and
are not upgraded to general theorems for the whole catalogue; the zero criterion D2 = 0
is used as a strict identity, but its synchronization with the zero-divisor locus is limited
to the axis and cross families.

6

BDI Interface and Stratum-Membership Recomputations

This chapter treats the interface between the top-dimensional double families and the
BDI topological theorem, and registers the stratum-membership recomputation of the
parallel family. Chapter 3 has fixed M as the normalized Moreno-pair parameter space,
homeomorphic to V2 (R7 ), of dimension 11; d(x) = dim AnnL (x) as the stratum dimension;
and the slot placement distinguishing the second slot inside S from the first S slot of the
second A5 component. Theorem 4.8 of Chapter 4 gives the 16-stratum double families
F and F ′ , and Theorem 4.6 gives the parallel family P (u, ε) = ((u, 0), (0, εu)), where
u ∈ Im O is nonzero and ε ∈ {+1, −1}, with stratum dimension 12. Section 5.4 of Chapter
23

## PDF page 24

5 has registered: the zero-divisor property of the parallel family is not characterized by
D2 = 0, and the zero criterion of D2 is limited to D1 D2 -type families such as the axis
and cross families. This chapter does not repeat the proof of the general BDI laws;
it only registers the verified correspondences, stratum-membership recomputations, and
evidence boundaries.

6.1

BDI Interface

The BDI topological theorem asserts that the highest-dimensional zero-divisor locus of A5
is homeomorphic to the disjoint union of two copies of V2 (R7 ). F and F ′ in Theorem 4.8
of Chapter 4 respectively use M as parameter space and give explicit coordinatizations
of these two copies: F (m) = ((a, b), (b, −a)), F ′ (m) = ψ(F (m)), where m = (a, b) ∈ M
and ψ interchanges the two A5 components. The parameter spaces of both F and F ′
are M , homeomorphic to V2 (R7 ); the left-annihilator dimensions of both families are 16.
ψ is not an A5 algebra automorphism, so F ′ is not the image of F under an algebra
isomorphism; their loci are registered independently. This interface concerns only the
highest-dimensional stratum and does not concern the completeness of the 4-, 8-, and
12-strata, nor does it write the two 16-stratum families as an exclusionary conclusion
beyond the highest-dimensional stratum.
The general BDI laws assert: for any nonzero zero divisor x in A5 , the left and right
annihilators are equal, and dim AnnL (x) is divisible by 4 and does not exceed 16. This law
is registered at census level on the registered families of this paper according to Entries
3 and 4 of Chapter 2: left- and right-annihilator dimensions are read in pairs and are
equal case by case; the stratum dimensions of the registered families fall in {4, 8, 12, 16}.
For families among the seven new families registered at probe level, their readings are
not upgraded to census level by this interface; before finalization, the sample sizes are
completed according to the absence registration of Chapter 2. The BDI topological
theorem and general laws serve only as interface anchors in this chapter and are not a
substitute proof for the completeness of the catalogue in Chapter 4.
The explicit kernel bases of F and F ′ are registered in Appendix D; the 16-vector basis
at the anchor (a, b) = (e1 , e2 ) has been verified vector by vector and closed (16/16, rank
16, Chapter 2 ledger), and the F ′ basis is derived by slot swap and closed simultaneously;
the explicit basis is a verified construction. The stratum dimension 16 of F and F ′ is
used at census level according to Entry 3 of Chapter 2; the status of their parameter-byparameter general proof is registered separately and is not automatically closed by the
closure of the explicit-basis verification.

6.2

Stratum-Membership Recompution of the Parallel Family

Let u ∈ Im O be nonzero, ε ∈ {+1, −1}, and write
xε = ((u, 0), (0, εu)).
According to the slot convention of Section 3.2 of Chapter 3, the first A5 component of
xε is (u, 0) and the second A5 component is (0, εu); εu falls in the second S slot of the
second A5 component, with index 24 + j (if u = ej , j ∈ {1, . . . , 7}), not the first S slot
index 16 + j of the second A5 component. Hence xε belongs to the parallel family P (u, ε)
24

## PDF page 25

of Theorem 4.6 of Chapter 4, not to the cross family C(m) = ((a, 0), (b, 0)), and not to
the equal-norm non-parallel branch of the mixed family H.
The stratum-membership recomputation is as follows. For five nonzero purely imaginary octonion probes u and the two sign branches ε = +1, −1, the left-annihilator
dimension d(xε ) was read one by one and is constantly 12. The reading path is: the
primary path of fraction-free Gaussian elimination reads the rank and kernel basis; the
secondary path of two-prime modular rank reads with 109 + 7 and 109 + 9 respectively;
the two paths and the kernel-basis arbitration are reconciled according to Clauses 1 and
3 of Chapter 2, and the three paths agree. This reading is registered at ironclad level
according to Entry 7 of Chapter 2. The family definition is given for arbitrary nonzero
purely imaginary u; the registered probes cover five nonzero purely imaginary u and the
two sign branches, and the general structural proof remains to be built; the probe-level
stability is not written as a parameter-by-parameter general theorem. The parameter
space of the parallel family is the nonzero purely imaginary octonions modulo positive
scaling, i.e., S 6 , of dimension 6; when the scale parameter is retained, it is Im O \ {0},
of dimension 7. The stratum dimension 12 of the family image does not depend on the
scale of u or the sign of ε; the parameter-space dimension is not confused with the 11
dimensions of M .
The previously registered “falling into the 4-stratum” reading does not enter the ledger
conclusions and is voided. The reason for voiding is not a change in the mathematical
condition of stratum membership, but an assembly risk in the reading path: Bareisstype routines that break the divisibility invariant when skipping columns may produce
readings inconsistent with the true kernel dimension by non-divisibility silent truncation;
this risk is registered according to Entry 5 and Clause 1 of Chapter 2. The recomputation
re-reads by the primary path of fraction-free elimination and the secondary path of twoprime modular rank, and after the readings agree the item is closed according to Clause 3
of Chapter 2. The stratum membership of the parallel family is based on the recomputed
reading of the 12-stratum, not on the earlier reading falling into the 4-stratum.
The correspondence between the parallel family and the BDI shape (a, ±i4 · a) is
registered as follows. Take a = (u, 0) ∈ S, u ∈ Im O nonzero; a is not a zero divisor in S:
the Moreno criterion requires both components to be purely imaginary, of equal norm,
orthogonal, and nonzero, while the second component of a is 0, which does not satisfy the
nonzero condition, so a is invertible in S. xε = ((u, 0), (0, εu)) gives an explicit realization
of the shape (a, ±i4 · a) in the BDI paraphrase under the multiplication convention of this
paper, with ε = +1 and ε = −1 corresponding to the two sign branches. The stratum
dimension 12 is consistent with the registration of the parallel family; the translation
between the n-counting convention of the BDI original text and the n = 5 stratum set of
this chapter is handled according to the boundary of Section 6.1, and this chapter does
not replace the parallel family’s own dimension reading with the BDI dimension formula,
nor does it write the “invertible branch of a” as a general proof of the parallel family’s
stratum dimension. The zero-divisor property of the parallel family is not characterized
by D2 = 0: if one formally takes a = u, b = u, then D1 = 2∥u∥2 , D2 = 4∥u∥4 , D2 ̸= 0,
while xε is still a zero divisor; this boundary is registered according to Section 5.4 of
Chapter 5.

25

## PDF page 26

6.3

Interface Boundaries and Evidence Levels

This section registers the applicability boundaries of the interface and recomputation of
Chapter 6.
First, the BDI topological interface of Section 6.1 addresses only the top-dimensional
stratum. F and F ′ realize explicit parameterizations of two copies of V2 (R7 ) and do not
exclude the stratum membership of other families outside the top-dimensional stratum,
which is registered separately according to the catalogue of Chapter 4; the BDI topological
theorem does not replace the stratum-structure count of Chapter 4, nor the completecatalogue problem.
Second, the general BDI laws are used at census level on the registered families; probelevel readings among the new families are not upgraded by the interface of Section 6.1.
The three items—left-right annihilator identity, divisibility of the dimension by 4, and
the upper bound 16—are registered case by case on the registered families; families whose
sample sizes have not been completed are retained according to the absence registration
of Chapter 2, and no blanket statement about “all families of the catalogue” is made.
Third, the stratum dimension 16 of F and F ′ is used at census level; the explicit
16-vector basis at the anchor (a, b) = (e1 , e2 ) has been verified coordinate by coordinate
and closed (16/16, rank 16, Chapter 2 ledger), the F ′ basis is closed simultaneously via
slot swap, and the explicit basis is a verified construction; the parameter-by-parameter
general proof is still registered separately as pending.
Fourth, the stratum membership 12 of the parallel family P (u, ε) is registered as
an ironclad-level probe reading; the general structural proof remains to be built. The
parameter space is stated as S 6 of dimension 6, or 7 with scale retained; it is not confused
with the 11 dimensions of M . The parallel branch of the mixed family is assigned to P
and is not counted twice; although the double-two-slot family B is parameterized by
M and D2 = 0, its slot structure differs from those of the axis and cross families, and
its determinant type and stratum synchronization are not automatically established by
D2 = 0; it is registered according to the pending-determination list of Section 5.5 of
Chapter 5.
Fifth, the BDI shape correspondence of the parallel family registers only the shape
realization and the verified stratum dimension; the translation between the n-counting
convention of the BDI original text and the stratum set of this chapter is handled according to the boundary of Section 6.1, and this correspondence is not written as an
independent proof of the BDI dimension formula. The stratum-membership recomputation does not claim a “convention-layer calibration”; the stratum difference is explained
by parallel-family membership and recomputed readings, not solely by the left-right multiplication convention of i4 .
Sixth, before finalization, complete according to the absence registration of Chapter
2: extend the parallel-family probes to census scale; the 169-cell cross rescan; the binarysupport full scan; the determination of determinant exponents for new families. Before
the above completion, the interface conclusions of Section 6.1 are used item by item at
census and ironclad levels, and the stratum membership of the parallel family in Section
6.2 is used item by item as an ironclad-level probe with a pending general proof.

26

## PDF page 27

7

Census Protocol and Golden Self-Checks

This chapter registers the census protocol for the A5 zero-divisor catalogue, the n = 4
golden self-check, and the A5 census scale. Chapter 2 has fixed the evidence levels:
ironclad level for pointwise identities, explicit counterexamples, or arbitrated stratummembership readings; census level for stable readings on exhaustive enumeration or
registered-size random samples; probe level for small-sample localization and objects
awaiting census, not upgraded to completeness conclusions. The protocol of this chapter
only produces readings and evidence levels and does not replace the family definitions of
Chapter 4, the pending determinant items of Chapter 5, or the BDI interface boundaries
of Chapter 6. Items registered as pending must not be written into ledger conclusions
before execution and dual-path reconciliation are completed.

7.1

Census Protocol

The census is carried out according to the following discipline.
First, exact integer rank. Kernel dimensions and rank readings use fraction-free Gaussian elimination as the primary path, reading the rank and kernel basis; floating-point
pivots are forbidden. Floating-point readings may be used only for cross-validation and
not as evidence. The elimination process of the primary path maintains exact rational
arithmetic, and pivot columns and free columns are registered separately.
Second, dual-algorithm reconciliation. Kernel dimensions and rank readings are additionally read by the secondary path of two-prime modular rank, with primes 109 + 7 and
109 + 9, and the two paths are read separately and then reconciled. They may be entered
into the ledger only when the primary and secondary paths agree and pass arbitration by
kernel basis or determinant; when the two paths disagree, a single-path reading must not
be used as evidence for family dimension or stratum membership, and a two-out-of-three
arbitration must be triggered and the failure mode registered. This clause is consistent
with Clauses 1 and 3 of Chapter 2. Its risk motivation is that Bareiss-type routines that
break the divisibility invariant when skipping columns may produce readings inconsistent
with the true kernel dimension by non-divisibility silent truncation; such readings must
not be used as sole evidence.
Third, construction input assertions. Each family executes input assertions before
generating the left-multiplication matrix: dimension assertion, purely-imaginary assertion, equal-norm assertion, orthogonality assertion, Moreno-condition assertion, and slotplacement assertion. Moreno-pair parameters are taken from the normalized parameter
space M of Section 3.3 of Chapter 3; non-normalized equal-norm orthogonal pairs are
assigned to the same family image via positive scaling. Those failing the assertions do
not enter reading registration; those passing the assertions register the assertion list and
random seed. The slot assertion distinguishes the second slot inside S from the first S
slot of the second A5 component: in the cross family C(m) = ((a, 0), (b, 0)), the index of
b is 16 + j; in the parallel family P (u, ε) = ((u, 0), (0, εu)), the index of εu is 24 + j; the
two are not interchangeable.
Fourth, two-out-of-three arbitration. When any two of the three readings—determinant,
rank, and kernel basis—agree and the third disagrees, the two agreeing paths are used
as the arbitration basis, and the failure mode of the third path is registered; when all
three disagree, the sample is voided and registered as an assembly event; majority vote

27

## PDF page 28

must not replace arbitration. Determinant readings use fraction-free elimination as the
primary method, with independent fraction-free LU decomposition or a computer algebra
system as a supplementary check; when the determinant is zero but the rank reading is
nonsingular, handle it by conflict arbitration; when the construction input claims a zero
divisor but the determinant is nonzero, the construction input is voided and registered.
Fifth, evidence levels and sample sizes. Each family registers the evidence level, sample
size, probe matrix, dual-path records, and random seed. Ironclad-level readings without
a general proof serve only as a basis for family actions, condition tightening, or stratum
membership, not as a completeness theorem. Census-level readings are not automatically
upgraded to general proofs. Probe-level readings enter the pending-census list; families
whose sample sizes have not been completed retain the label “census pending” in the
catalogue of Chapter 4.
Sixth, execution workflow. For each registered family, execute in order: recursively
generate the multiplication table and spot-check sign consistency and closure; generate construction inputs and execute the assertions of the third clause; generate the
left-multiplication matrix and read the rank and kernel basis by fraction-free Gaussian
elimination; re-read by two-prime modular rank and reconcile according to the second
clause; read the determinant by fraction-free elimination and verify by an independent
path, comparing the zeros of D2 with the Moreno condition; register readings, sample
size, evidence level, random seed, and arbitration records; probe-level readings enter the
pending-execution list, census-level readings enter stable conclusions, and ironclad-level
readings enter family-action, condition-tightening, or stratum-membership entries. This
workflow is implemented in exact integer arithmetic and does not depend on external
code libraries; the protocol is fully replayable once the random seed is registered.

7.2

Golden Self-Check (n = 4)

The census protocol is first calibrated at the S layer, and after calibration it is transplanted
verbatim to A5 . The calibration items are as follows.
Multiplication-table structure: on 600 random samples each for n = 4 and n = 5,
the conjugate anti-automorphism, the flexibility law, and power-associativity were tested
with zero failures; on n = 3, the three forms of alternativity were tested on 200 samples
each with zero failures; on n = 4, a counterexample to alternativity appears, consistent
with the classical conclusion that the sedenions are non-alternative. This reading also
serves as a detector for the correctness of the multiplication-table assembly.
Two-way self-check of the Moreno criterion: purely imaginary equal-norm candidates
are divided by support into single-support | single-support: 49 cases and double-support
| double-support: 1764 cases, among which there are 882 zero divisors; the two directions “zero divisor implies orthogonality” and “equal norm and orthogonality imply zero
divisor” have zero exceptions within the candidate classes; 500 strictly constructed equalnorm orthogonal samples are all zero divisors with left-annihilator dimension exactly 4;
the explicit kernel construction of Moreno holds case by case under substitution. This
self-check provides a calibration anchor for the n = 5 stratum-membership readings and
does not replace the Moreno criterion itself.
Stratum-dimension calibration: the kernel dimension 4 at the n = 4 Moreno anchor
(a, b) = (e1 , e2 ) agrees between fraction-free elimination and an independent path; leftand right-annihilator dimensions are read in pairs and are equal case by case. After cali-

28

## PDF page 29

bration passes, the A5 census uses the same assertions, the same dual-path reconciliation,
and the same two-out-of-three arbitration.

7.3

A5 Census Scale and Pending Items

The A5 census is registered family by family according to the stratum catalogue of Chapter
4. The registered sample sizes are as follows: the axis family Ax and the second-slot axis
family Ax2 are registered on the block proof and probe readings; the 4-stratum double
(1)
(2)
families F4 , F4 each have readings on 42 unit Moreno pairs and 10 random Moreno
pairs; the diagonal family Dg has readings on 8/8 random Moreno pairs and registered
unit pairs; the direct reading of G3 is registered at probe level according to Entry 7 of
Chapter 2, and its stratum membership is at the same level as the diagonal family via
automorphism inheritance; for the cross family C, the 42 unit pairs ((ei , 0), (ej , 0)), i ̸= j,
are read one by one; the 16-stratum double families F and F ′ each have readings on 8
random Moreno pairs and 10 unit pairs; the parallel family P has readings on five nonzero
purely imaginary octonion probes and the two sign branches; the conditional profiles of
the double-two-slot family B and the mixed family H have readings on 2 to 5 probe
samples. The above readings are registered item by item according to Entries 3 and 7 of
Chapter 2; probe-level families are not upgraded before the sample sizes are completed.
The pending items are as follows; before execution they must not be used as ledger
conclusions.
First, multi-sample census for the seven new families. G1 , G2 , G3 , the second-slot axis
family Ax2 , the equal-norm non-parallel branch of the mixed family H, the parallel family
P , and the double-two-slot family B each undergo a census of no fewer than 8 random
Moreno samples; the parallel family additionally extends the nonzero purely imaginary
octonion probes to cover e1 , e2 , e3 , e1 + e2 , e1 + e2 + e3 and sign variants, with the two sign
branches registered separately.
Second, binary-support full scan. Take the 32 basis vectors e0 through e31 of A5 and
the formal strings ei ±ej , where (i, j) is an ordered pair with i ̸= j and the signs are + and
−, totaling 32 × 31 × 2 = 1984. This convention includes mixed strings of real units and
purely imaginary basis vectors as well as strings between purely imaginary basis vectors;
ei + ej and ej + ei are regarded as different registered items at the formal-string level and
are merged when deduplicating support classes. If later restricted to purely imaginary
basis vectors or deduplicated ordered pairs, the count is registered separately and does
not reuse 1984. The full scan reads the left-annihilator dimension, whether the left and
right annihilators are equal, and whether the determinant is zero for each string, and
reconciles according to the dual paths of Section 7.1; the full-scan results only expand
census coverage and do not constitute a completeness proof.
Third, parallel probes and equal-norm non-orthogonal probes. The parallel probes
are extended according to the second item; the equal-norm non-orthogonal probes take
a = 3e1 + e2 , b = e1 + 3e2 and their swaps and sign variants, whose norms are equal
and whose inner product is nonzero, used to test the invertibility of the cross family C
under non-Moreno conditions, the conditional profile of the mixed family H, and the
stratum-membership boundary of the parallel family P . These probes are registered as
conditional-profile readings and are not upgraded to general theorems.
Fourth, 169-cell cross rescan. Execute a 169-cell cross rescan for the full-type ×
half-type combinations, registering the stratum dimension, left-right annihilator equality,

29

## PDF page 30

and determinant zeros of each cell; compare the rescan results with the within-stratum
counts of Chapter 4, and when a counting conflict is found, register it according to the
two-out-of-three arbitration of Section 7.1.
Fifth, determination of determinant exponents for new families. According to the
pending-determination list of Section 5.5 of Chapter 5, determine the left-multiplication
determinants of the 4-stratum double families, the diagonal family, G3 , the second-slot
axis family, the three branches of the mixed family H, the parallel family P , the doubletwo-slot family B, and the 16-stratum double families F and F ′ separately; families
parameterized by M are tested first for the D1 D2 type, and the parallel family is given
candidate factors expressed in terms of the norm of u and a quartic invariant, with D2 = 0
not used as the zero-divisor discriminant of the parallel family.
Sixth, closing of explicit-basis verification. The coordinate-by-coordinate substitution
verification of the 16-vector basis of F and F ′ has been completed (16/16, rank 16,
including rows 10 and 11, Chapter 2 ledger); the correspondence between rows 10 and 11
and the structured subfamilies in the framework of Appendix D has been registered vector
by vector, and the verification conclusion is: both rows are valid kernel-basis vectors, and
their “((x, y), (y, −x))” template correspondence is retained as an explanatory remark
rather than a structural conclusion; the step det Rm̄ = det Lm in E.1 has been recomputed
(8/8). The above two items are closed from the pending-execution list, and the explicit
basis is a verified construction.
Seventh, extension of left-right annihilator identity. For the seven new families and
the binary-support full-scan samples, read the left- and right-annihilator dimensions in
pairs and register their equality case by case; unequal samples are registered as assembly
events and are not merged into the census-level conclusions of the general BDI laws.

7.4

Evidence Boundaries

The boundaries registered in this section are consistent with Chapters 2, 4, 5, and 6. First,
the census protocol produces readings and evidence levels, not completeness theorems;
the stratum-structure count of Chapter 4 is at census-pending level, the full-type × halftype cross combinations have not been fully scanned, and the catalogue may still grow.
Second, the 1984 formal strings of the binary-support full scan are defined by the orderedpair and double-sign convention; if the counting convention changes, it is re-registered
and not mixed with 1984. Third, the stratum membership of the parallel family P is
registered as an ironclad-level probe reading, and the general structural proof remains to
be built; the parameter space is stated as S 6 of dimension 6, or 7 with scale retained,
and is not confused with the 11 dimensions of M . Fourth, the equal-norm non-parallel
branch of the mixed family H is counted in the 4-stratum family count, and the parallel
branch is assigned to P and not counted twice; its conditional completeness is left to the
open problems. Fifth, the zero criterion D2 = 0 is limited to D1 D2 -type families such
as the axis and cross families; the zero-divisor conditions and determinant types of the
parallel family, the double-two-slot family, and the mixed family are handled according
to the pending-determination list of Chapter 5. Sixth, before the above pending items
are completed, probe-level readings must not be upgraded, census-level readings must
not be upgraded to general proofs, and ironclad-level readings without a general proof
serve only as a basis for stratum membership and condition tightening.

30

## PDF page 31

8

Conclusions and Open Problems

This chapter summarizes the registered conclusions, evidence levels, and open problems
according to the stratum catalogue of Chapter 4, the pending determinant list of Chapter
5, the BDI interface boundaries of Chapter 6, and the census protocol of Chapter 7. This
chapter does not restate the family definitions and verification protocols; “registered”
means entered into the ledger according to the evidence levels of Chapter 2, and “pending”
means that before the pending items of Section 7.3 of Chapter 7 are completed they must
not be used as ledger conclusions.

8.1

Registered Conclusions

First, stratum structure and family counts. The full stratum set of A5 zero divisors
covers {0, 4, 8, 12, 16} on the registered families, where the 0-stratum consists of nonzero
invertible elements and does not belong to the zero-divisor stratum D5 ; the zero-divisor
stratum D5 covers {4, 8, 12, 16} on the registered families. The within-stratum family
(1)
(2)
counts are: 4-stratum: F4 , F4 , G1 , G2 , and the equal-norm non-parallel branch of the
mixed family H, 5 families in total; 8-stratum: axis family Ax, diagonal family Dg, G3 ,
and second-slot axis family Ax2 , 4 families in total; 12-stratum: cross family C, parallel
family P , and double-two-slot family B, 3 families in total; 16-stratum: F and F ′ , 2
(2)
(1)
families in total; fourteen families in total. The basic seven families are F4 , F4 , Ax,
Dg, C, F , F ′ ; the seven new families are G1 , G2 , G3 , Ax2 , the equal-norm non-parallel
branch of H, P , B. The parallel branch of the mixed family H is assigned to P and is
not counted twice. This count is registered at census-pending level according to Section
4.7 of Chapter 4: the family count is given by the definitions of the registered families,
and the non-emptiness of each stratum is guaranteed by explicit families; the full-type
× half-type cross combinations have not been fully scanned, and the binary-support full
scan has not been carried out, so the count is not a completeness theorem.
Second, the basic seven families are incomplete. An explicit zero-divisor instance
has been constructed that does not belong to the parameterization templates of the basic
seven families: the parallel family P (u, ε) = ((u, 0), (0, εu)) has left-annihilator dimension
constantly 12 for any nonzero purely imaginary octonion u and ε ∈ {+1, −1}, and its
slot structure matches none of the templates: the cross family C(m) = ((a, 0), (b, 0)), the
16-stratum F and F ′ , the 8-stratum axis and diagonal families, and the 4-stratum double
families. Hence “the basic seven families are complete” is false; this counterexample is
registered at ironclad level according to Entry 7 of Chapter 2. The 8× 8 symbolic-pattern
probe has been registered as a pending machine-check item (Section 2.3 of Chapter 2),
its reading is not entered into the ledger, and the ledger basis for incompleteness does
not depend on this probe.
Third, family actions and condition tightening. φ(u, v) = (u, −v) is an A5 algebra
automorphism, and this identity has an identity proof (Remark 4.1.1 of Chapter 4);
(1)
(2)
120 random samples are retained as assembly probes; φ sends F4 to G1 , F4 to G2 ,
and the diagonal family Dg to G3 , all three being template-level identities; φ does not
(1)
(2)
(2)
interchange F4 and F4 , and the template ((a, b), (a, −b)) of F4 cannot be rewritten as
((a, b), (−a, b)). The above three items are registered at ironclad level according to Entry
7 of Chapter 2; the images of the remaining families under φ are registered per family as
pending census items. The zero-divisor property of the cross family C(m) = ((a, 0), (b, 0))
31

## PDF page 32

requires (a, b) to be a Moreno pair: the unequal-norm probes (e1 , 2e2 ), (2e1 , 3e2 ) and the
non-orthogonal equal-norm probe (3e1 + e2 , e1 + 3e2 ) are all invertible, so “the norms
need not be equal” cannot serve as a sufficient condition for this family; this reading is
registered at ironclad level according to Entry 7 of Chapter 2.
Fourth, BDI interface. F and F ′ respectively use the normalized Moreno parameter
space M as parameter space, and M is homeomorphic to V2 (R7 ), of dimension 11; the
left-annihilator dimensions of both families are 16, and they respectively realize explicit
parameterizations of the two copies of V2 (R7 ) in the BDI topological theorem. ψ interchanges the two A5 components and is not an A5 algebra automorphism, so F ′ is not the
image of F under an algebra isomorphism; their loci are registered independently. This
interface concerns only the highest-dimensional stratum and does not concern the completeness of the 4-, 8-, and 12-strata. The three items of the general BDI laws—left-right
annihilator equality, divisibility of the dimension by 4, and the upper bound 16—are used
at census level on the registered families; families among the new families registered at
probe level are not upgraded by this interface. The stratum dimension 16 of F and F ′ is
used at census level; the 16-vector basis at the anchor (a, b) = (e1 , e2 ) has been verified
coordinate by coordinate and closed (16/16, rank 16, Chapter 2 ledger), the F ′ basis is
closed simultaneously via slot swap, and the explicit basis is a verified construction.
Fifth, stratum membership of the parallel family. P (u, ε) = ((u, 0), (0, εu)) has leftannihilator dimension constantly 12 on five nonzero purely imaginary octonion probes and
the two sign branches, agreeing across the primary path of fraction-free elimination, the
secondary path of two-prime modular rank, and kernel-basis arbitration on three paths,
registered at ironclad level according to Entry 7 of Chapter 2; the general structural proof
remains to be built. The parameter space is the nonzero purely imaginary octonions
modulo positive scaling, i.e., S 6 , of dimension 6; with scale retained, dimension 7; the
stratum dimension 12 of the family image does not depend on scale or sign. The zerodivisor property of the parallel family is not characterized by D2 = 0: if one formally
takes a = u, b = u, then D1 = 2∥u∥2 , D2 = 4∥u∥4 , D2 ̸= 0, while xε is still a zero
divisor. This family gives an explicit realization of the BDI shape (a, ±i4 · a) under
the multiplication convention of this paper; the stratum-membership recomputation does
not claim a “convention-layer calibration”, and the stratum difference is explained by
parallel-family membership and recomputed readings.
Sixth, applicability boundaries of the determinant laws. The block structure Lx =
diag(Lm , Rm ) of the axis family Ax(m) = ((a, b), 0) is a strict equality; the exponents
(8, 4) hold at census level on 30 random Moreno samples, and the two steps on which
the general proof depends—the S-layer formula det Lm = D14 D22 and det Rm = det Lm —
have both received sample-level verification (30/30 or more and 8/8, Chapter 2 ledger),
while the parameter-by-parameter general proof remains to be built. The D14 D26 of the
cross family C(m) = ((a, 0), (b, 0)) holds at census level on 54 samples, and the general
proof remains to be built. D2 = 0 is equivalent to a, b having equal norm and being
orthogonal; this identity is strict; but its synchronization with the zero-divisor locus is
limited to D1 D2 -type families such as the axis and cross families and is not extrapolated
to a statement about the whole catalogue. The zero-divisor conditions and determinant
types of the parallel family, the double-two-slot family B, and the mixed family H are
handled according to the pending-determination list of Section 5.5 of Chapter 5.

32

## PDF page 33

8.2

Open Problems

Open Problem 1 (Complete catalogue). Give the complete catalogue of A5 zero
divisors, or prove that the pattern catalogue is closed under “full-type × half-type ×
slot operations”. This problem is directly related to the pending items of Section 7.3
of Chapter 7: only after the 169-cell cross rescan, the binary-support full scan, the
multi-sample census of the seven new families, and the extension of parallel probes are
completed can the “within-stratum count” be upgraded from census-pending level to a
completeness candidate. The incompleteness of the basic seven families already has an
explicit counterexample, so the problem is no longer “prove or disprove the completeness
of the basic seven families”, but: first, whether there are zero divisors beyond the fourteen
registered families; second, if full-type × half-type × slot operations are taken as the
pattern-generation rule, whether this rule is closed; third, if it is closed, whether the
closed class is exactly the closure of the registered families under slot operations. None
of the three subproblems has been proved, and they are registered as open.
Open Problem 2 (Determinant exponents and discriminants). Determine
the left-multiplication determinants of the undetermined families and register them by
family type. The list is given family by family according to Section 5.5 of Chapter 5:
(2)
(1)
among the basic families, the as-yet-undetermined 4-stratum double families F4 , F4 ,
the 8-stratum diagonal family Dg, and the 16-stratum double families F and F ′ ; the seven
new families G1 , G2 , G3 , the second-slot axis family Ax2 , the equal-norm non-parallel
branch of the mixed family H, the parallel family P , and the double-two-slot family
B. For families parameterized by M , test whether there exist nonnegative integers α, β
such that det Lx = D1α D2β ; if not, register their indecomposable factor structure. For the
parallel family P , test whether there exists a factorization expressed in terms of the norm
of u and a quartic invariant of u; D2 = 0 is not used as its zero-divisor discriminant.
For the mixed family H, determine separately for the three branches: equal norm and
non-parallel, parallel, and unequal norm; the parallel branch is assigned to P and is not
counted twice. det Rm = det Lm has received sample-level verification (8/8, Chapter 2
ledger), and its parameter-by-parameter general proof is registered together with this
problem.
Open Problem 3 (Higher-dimensional generalization). Generalize the catalogue method to A6 (64-ions): the BDI formula gives the number of top-layer copies as
2n−4 , which is 4 for n = 6; no explicit coordinatization has yet been given. This problem
is registered as an absent item: the stratified generalization to A6 and higher dimensions
has not been carried out; recursive multiplication-table generation, dual-path rank readings, and the two-out-of-three arbitration protocol can be transplanted verbatim, but the
Moreno criterion covers only n = 4, and the parameterizations and discriminants of the
A6 strata need to be re-established. The A6 generalization does not automatically follow
from the fourteen-family count of A5 .

8.3

Evidence Levels and Pending Items

The conclusions of this chapter are used at the three evidence levels of Chapter 2; census
level is not upgraded to general proof, and probe level is not upgraded to census level. The
entries registered at ironclad level are: the explicit counterexample to the completeness
of the basic seven families; the three family actions of φ (identity proof, Remark 4.1.1);
the Moreno condition tightening for the cross family; the probe reading of the parallel
33

## PDF page 34

family’s stratum membership in the 12-stratum. The entries registered at census level are:
the determinant exponents of the axis and cross families; the stratum dimensions of F
and F ′ ; the stratum dimensions of G1 , G2 , G3 (automorphism inheritance, Remark 4.1.1,
completely at the same level as the 4-stratum double families and the diagonal family);
the three readings of the general BDI laws on the registered families. The dimension 8
of the second-slot axis family has a general block-structure proof (Theorem 4.4) and, like
the axis family, is registered as a strict proof and does not occupy the above three levels.
The entries registered at census-pending level are: the within-stratum family counts and
stratum-set coverage. The probe-level entries are: the conditional profiles of the doubletwo-slot family and the mixed family; the direct readings of G1 , G2 , G3 are retained as
assembly records before the sample sizes are completed, without affecting their stratum
membership registered via inheritance; probe-level entries do not enter the completeness
discussion before the sample sizes are completed.
The pending items before finalization are registered according to Section 7.3 of Chapter 7: a census of no fewer than 8 random Moreno samples for each of the seven new
families; the binary-support full scan, with formal strings ei ± ej totaling 1984 combinations, defined by the ordered-pair and double-sign convention; extension of parallel
probes and equal-norm non-orthogonal probes; the 169-cell cross rescan; determination
of determinant exponents for new families; extension of the left-right annihilator identity
to the seven new families and the full-scan samples. The vector-by-vector verification of
the explicit bases of F and F ′ and the recomputation of det Rm̄ = det Lm in E.1 have
been closed (Chapter 2 ledger) and are no longer listed as pending items. Before the
above pending items are completed, the census-level conclusions in the fifth and sixth
items of Section 8.1 remain at census level, the census-pending counts in the first and
second items of Section 8.1 are not upgraded to completeness theorems, and the three
subproblems of Open Problem 1 in Section 8.2 all remain open.

Remark
The translation of this article was done by DeepSeek, and the mathematical modeling
and the literature review of this article were assisted by DeepSeek.

References
[1] Moreno, Guillermo. “The Zero Divisors of the Cayley–Dickson Algebras over the
Real Numbers.” Boletı́n de la Sociedad Matemática Mexicana (3) 4, no. 1 (1998):
13–28.
[2] Biss, Daniel K., Daniel Dugger, and Daniel C. Isaksen. “Large Annihilators in
Cayley–Dickson Algebras.” Communications in Algebra 36, no. 2 (2008): 632–664.
[3] Biss, Daniel K., J. Daniel Christensen, Daniel Dugger, and Daniel C. Isaksen. “Large
Annihilators in Cayley–Dickson Algebras II.” Boletı́n de la Sociedad Matemática
Mexicana (3) 13, no. 2 (2007): 269–292.
34

## PDF page 35

[4] Biss, Daniel K., J. Daniel Christensen, Daniel Dugger, and Daniel C. Isaksen. “Eigentheory of Cayley–Dickson Algebras.” Forum Mathematicum 21, no. 5 (2009): 833–
851.
[5] Schafer, Richard D. An Introduction to Nonassociative Algebras. New York: Academic Press, 1966.
[6] Baez, John C. “The Octonions.” Bulletin of the American Mathematical Society 39,
no. 2 (2002): 145–205.
[7] Conway, John H., and Derek A. Smith. On Quaternions and Octonions: Their Geometry, Arithmetic, and Symmetry. Natick, MA: A K Peters, 2003.
[8] Kantor, I. L., and A. S. Solodovnikov. Hypercomplex Numbers: An Elementary Introduction to Algebras. Translated by A. Shenitzer. New York: Springer-Verlag, 1989.
[9] Biss, Daniel K., Daniel Dugger, and Daniel C. Isaksen. “Large Annihilators in
Cayley–Dickson Algebras.” arXiv:math/0511691 (2005). Preprint version of the
Communications in Algebra article, cited for the topological theorem on the highestdimensional zero-divisor locus.
[10] Moreno, Guillermo. “The Zero Divisors of the Cayley–Dickson Algebras over the
Real Numbers.” arXiv:math/9711203 (1997). Preprint version, cited for the explicit
zero-divisor criterion and the Stiefel manifold identification in the sedenion layer.
[11] Zhilina, S. A. “On Doubly Alternative Zero Divisors in Cayley–Dickson Algebras.”
Zapiski Nauchnykh Seminarov POMI 514 (2022): 18–54. Cited for the study of
annihilator dimensions of zero divisors in Cayley–Dickson algebras over fields of
characteristic not 2, providing context for the dimension-4 divisibility property.
[12] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law A: Correspondence of Layer Fractures in Normed Division Algebras, Sphere Parallelizability, and Operadic Homology.” Zenodo (2026). https://doi.org/10.5281/zenodo.
23410695.
[13] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law B: The
Hochschild Cohomology Class of the Associator and Cayley–Dickson Zero Divisors.”
Zenodo (2026). https://doi.org/10.5281/zenodo.23427939.
[14] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law C: Information Loss Coefficient of Prime Additive Constraint Networks—Truncated Numerical
Protocol and Asymptotic Settlement.” Zenodo (2026). https://doi.org/10.5281/
zenodo.23428521.
[15] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law D: Stasheff
Markings of the Cayley–Dickson Sequence and Layer Fracture—Correspondence on
Categorical Skeleta and Conditional Structural Constants.” Zenodo (2026). https:
//doi.org/10.5281/zenodo.23430340.
[16] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law E: Defect Operators of Prime Additive Formal Complexes—Parity Rigidity, Unconditional Nonvanishing, and the Homotopy Bridge Problem.” Zenodo (2026). https://doi.org/
10.5281/zenodo.23443720.
35

## PDF page 36

[17] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law F: The Arithmetic Kernel of Character-Weighted Prime Sums—Conditional Theorems, AnchorFree Corollaries, and a Representation-Theoretic No-Go.” Zenodo (2026). https:
//doi.org/10.5281/zenodo.23444958.
[18] Zhou, Changzheng, and Ziqing Zhou. “Functorial Layer-Collapse Law G: Extended
Ceiling—Higher-Dimensional Explicit Bijections, a Universal Template for Exceptional Lie Groups, and a Rigorous Quantum-Information Framework.” Zenodo
(2026). https://doi.org/10.5281/zenodo.23448500.

Appendix A: Examples of Explicit Coordinates
This appendix gives the support indices of the representative elements of the fourteen
families of Chapter 4 at the fixed Moreno pair (a, b) = (e1 , e2 ), completely enumerates the
42 unit pairs of the 12-stratum cross family, and gives one set of annihilator-coordinate
examples for a Moreno pair. The index convention follows Section 3.2 of Chapter 3:
for an S element (x, y), the purely imaginary part of the first slot is placed in indices 1
through 7, and the purely imaginary part of the second slot is placed in indices 9 through
15; for an A5 element (m1 ; m2 ), m1 is placed in indices 0 through 15 and m2 in indices
16 through 31, with the internal layout of m2 the same as that of S, shifted overall by
16. In the Moreno pair (a, b) = (e1 , e2 ), a = e1 is at index 1 and b = e2 is at index 10.
In the “nonzero coordinates” column of the table below, the part before the colon is the
index and the part after the colon is the coefficient; when the coefficient is +1, only the
index is written.

A.1 Support Indices of Representative Elements for the Fourteen
Families
Stratum

Family

4

F4

(1)

4
4
4
4

F4
G1
G2
H equal-norm
non-parallel branch
axis family Ax
diagonal family Dg
G3
second-slot axis family
Ax2
cross family C
parallel family P (u = e1 ,
ε = +1)
parallel family P (u = e1 ,
ε = −1)
double-two-slot family B
F
F′

(2)

8
8
8
8
12
12
12
12
16
16

Nonzero coordinates

Stratum
dimension

((a, b), (b, a))

1, 10, 18, 25

4

((a, b), (a, −b))
((a, b), (−b, −a))
((a, b), (−a, b))
((a, 0), (0, b))

1, 10, 17, 26 : −1
1, 10, 18 : −1, 25 : −1
1, 10, 17 : −1, 26
1, 26

4
4
4
4

((a, b), 0)
((a, b), (a, b))
((a, b), (−a, −b))
(0, (a, b))

1, 10
1, 10, 17, 26
1, 10, 17 : −1, 26 : −1
17, 26

8
8
8
8

((a, 0), (b, 0))
((u, 0), (0, u))

1, 18
1, 25

12
12

((u, 0), (0, −u))

1, 25 : −1

12

((0, a), (0, b))
((a, b), (b, −a))
ψ(F ) = ((b, −a), (a, b))

9, 26
1, 10, 18, 25 : −1
2, 9 : −1, 17, 26

12
16
16

Representative
element

36

## PDF page 37

The stratum dimensions in the table are registered according to Chapters 4 and 6; there
are five families in the 4-stratum, four in the 8-stratum, three in the 12-stratum, and two
in the 16-stratum, fourteen families in total. The parallel branch b = ±a of the mixed
family H is assigned to the parallel family P and is not listed separately in this table.

A.2 Complete Enumeration of the 42 Unit Pairs in the 12-Stratum
Cross Family
The unit elements of the cross family are ((ei , 0), (ej , 0)), with support indices {i, 16 + j},
where (i, j) runs over ordered pairs i ̸= j, 1 ≤ i, j ≤ 7. The total number of ordered pairs
is 7 × 6 = 42. The supports are as follows.
i = 1: (1, 2) → {1, 18}; (1, 3) → {1, 19}; (1, 4) → {1, 20}; (1, 5) → {1, 21}; (1, 6) →
{1, 22}; (1, 7) → {1, 23}.
i = 2: (2, 1) → {2, 17}; (2, 3) → {2, 19}; (2, 4) → {2, 20}; (2, 5) → {2, 21}; (2, 6) →
{2, 22}; (2, 7) → {2, 23}.
i = 3: (3, 1) → {3, 17}; (3, 2) → {3, 18}; (3, 4) → {3, 20}; (3, 5) → {3, 21}; (3, 6) →
{3, 22}; (3, 7) → {3, 23}.
i = 4: (4, 1) → {4, 17}; (4, 2) → {4, 18}; (4, 3) → {4, 19}; (4, 5) → {4, 21}; (4, 6) →
{4, 22}; (4, 7) → {4, 23}.
i = 5: (5, 1) → {5, 17}; (5, 2) → {5, 18}; (5, 3) → {5, 19}; (5, 4) → {5, 20}; (5, 6) →
{5, 22}; (5, 7) → {5, 23}.
i = 6: (6, 1) → {6, 17}; (6, 2) → {6, 18}; (6, 3) → {6, 19}; (6, 4) → {6, 20}; (6, 5) →
{6, 21}; (6, 7) → {6, 23}.
i = 7: (7, 1) → {7, 17}; (7, 2) → {7, 18}; (7, 3) → {7, 19}; (7, 4) → {7, 20}; (7, 5) →
{7, 21}; (7, 6) → {7, 22}.
The left-annihilator dimension of each pair was read one by one and is constantly 12
(Entry 3 of Chapter 2, census level); all elements in the table are unit elements, with
norm 1 and inner product zero, satisfying the Moreno condition. No condition beyond ei
and ej is required within the family.

A.3 Example Annihilator Coordinates for a Moreno Pair
Take (a, b) = (e1 , e2 ) ∈ S, indices {1, 10}, with left-annihilator dimension 4. A basis of
AnnS (e1 , e2 ) is:
e7 + e12 , −e6 + e13 , e5 + e14 , −e4 + e15 .
Here e12 = e4 lies in the second slot (8 + 4), e13 = e5 lies in the second slot, e14 = e6 lies in
the second slot, and e15 = e7 lies in the second slot; the first-slot indices 4 through 7 are
paired alternately with the second-slot indices 12 through 15. This basis was obtained by
exact fraction-free row elimination, and the substitution verification of left multiplication
by (e1 , e2 ) is zero vector by vector (Entry 2 of Chapter 2, census level).

A.4 Verification Status
The support indices and the 42-pair enumeration in this appendix are deterministic registrations; the stratum dimensions are at the census level of Entry 3 of Chapter 2. The
37

## PDF page 38

vector-by-vector substitution verification of the annihilator basis in A.3 is registered according to Entry 2 of Chapter 2. The vector-by-vector verification of the 16-vector basis
of the F family in Appendix D has been closed (16/16, rank 16, Chapter 2 ledger), and
the F ′ basis is closed simultaneously via slot swap; the supports of F and F ′ in A.1 and
the explicit bases in Appendix D are verified constructions.

Appendix B: Details of the Machine-Check Ledger
This appendix registers the execution protocols, sample sizes, probe matrices, dual-path
records, and random-seed structures of the ledger entries of Chapter 2. All readings are
executed in exact integer arithmetic; fraction-free Gaussian elimination is the primary
path, two-prime modular rank (109 + 7, 109 + 9) is the secondary path, and determinants
use fraction-free elimination as the primary method with independent fraction-free LU or
a computer algebra system as a supplementary check. The two-out-of-three arbitration
rule follows Clause 3 of Chapter 2.

B.1 Recursive Construction Protocol for the Multiplication Table
The multiplication table is generated layer by layer by the Cayley–Dickson doubling formula, and basis-vector products are represented exactly as “sign–index pairs”. After each
layer is generated, two types of spot checks are performed: sign-consistency spot checks,
verifying that the conjugate anti-automorphism holds on random samples; and closure
spot checks, verifying that all basis products fall back into the index set of that layer.
The layer-2 and layer-3 multiplication tables are aligned item by item with the standard
relations for the quaternions and octonions as external anchors. On 600 random samples
each for n = 4 and n = 5, the conjugate anti-automorphism, the flexibility law, and
power-associativity were tested with zero failures; on n = 3, the three forms of alternativity were tested on 200 samples each with zero failures; on n = 4, a counterexample
to alternativity appears, consistent with the classical conclusion that the sedenions are
non-alternative.

B.2 Entry 2 (Golden Self-Check of the Moreno Criterion)
Candidate classes and counts: purely imaginary equal-norm candidates are divided by
support into single-support | single-support: 49 cases (ordered index pairs i, j ∈ {1, . . . , 7}:
all 42 cases with i ̸= j are zero divisors, and the 7 cases with i = j are invertible), and
double-support | double-support: 1764 cases (on each side, 42 signed double-support elements ei ± ej , i < j), among which there are 882 zero divisors in the double-support |
double-support class. Two-way machine check of the criterion: the two directions “zero
divisor implies orthogonality” and “equal norm and orthogonality imply zero divisor”
have zero exceptions within the candidate classes, and all 882 double-support zero divisors fall under the Moreno criterion. All 500 strictly constructed equal-norm orthogonal
samples are zero divisors with left-annihilator dimension exactly 4. The explicit kernel
construction of Moreno (for (a, b) and the parameterized family (a(yb), ∥a∥2 y)) holds case
38

## PDF page 39

by case under substitution. The kernel dimension 4 at the anchor (a, b) = (e1 , e2 ) agrees
between fraction-free elimination and an independent path; left- and right-annihilator
dimensions are read in pairs and are equal case by case.

B.3 Entry 3 (Stratified Family Verification) and Entry 7 (Registration of New Families)
Sample sizes of the basic families: the 16-stratum double families F and F ′ each have 8
(1)
(2)
random Moreno pairs plus 10 unit pairs; the 4-stratum double families F4 , F4 each
have 42 unit pairs plus random pairs; the 8-stratum axis and diagonal families and the 12stratum cross family have full unit pairs plus random pairs; the 42 unit pairs of the cross
family were read one by one, with dimension constantly 12. The readings were reconciled
by the primary path of fraction-free elimination and the secondary path of two-prime
modular rank, and compared case by case with an independent second implementation
path; all agree.
The registration of new families in Entry 7 is in four parts.
First, incompleteness counterexample. The parallel family P (u, ε) = ((u, 0), (0, εu)),
u ∈ Im O nonzero, ε ∈ {+1, −1}, has left-annihilator dimension constantly 12 on the
five nonzero purely imaginary octonion probes u ∈ {e1 , e2 , e3 , e1 + e2 , e1 + e2 + e3 } and
the two sign branches; the three paths agree. The slot structure of this family matches
none of the templates of the basic seven families (the 4-stratum double-family template
coincides formally with ((u, 0), (0, u)) at b = 0, but b = 0 is not in M , so it does not
constitute a match), so the basic seven families are incomplete; this reading is registered
at ironclad level according to Entry 7. The 8 × 8 symbolic-pattern probe is registered as
a pending machine-check item, and its reading is not entered into the ledger before the
pattern definition and counting convention are supplementally registered.
Second, probe registration of the seven new families. The probe sample sizes of G1 ,
G2 , G3 , the second-slot axis family Ax2 , the equal-norm non-parallel branch of the mixed
family H, the parallel family P , and the double-two-slot family B are 2 to 5 Moreno
probes per family, and the readings are registered at probe level according to Entry 7.
The probe matrix is: Moreno pairs (e1 , e2 ), (e2 , e3 ), (e1 + e3 , e2 − e4 ) and their sign
variants; the parallel family additionally takes u ∈ {e1 , e2 , e3 , e1 + e2 , e1 + e2 + e3 } and
ε ∈ {+1, −1}; the equal-norm non-orthogonal probes take a = 3e1 + e2 , b = e1 + 3e2 and
their swaps and sign variants, registered as conditional-profile readings.
Third, three ironclad-level items. φ(u, v) = (u, −v) is an A5 algebra automorphism,
with the identity proof in Remark 4.1.1 of Chapter 4; 120 random samples are retained
(1)
(2)
as assembly probes; φ sends F4 to G1 , F4 to G2 , and the diagonal family Dg to G3 ,
all three being template-level identities; the Moreno condition tightening for the cross
family C: the unequal-norm probes (e1 , 2e2 ), (2e1 , 3e2 ) and the non-orthogonal equalnorm probe (3e1 +e2 , e1 +3e2 ) are all invertible; the parallel family’s stratum membership
is 12-dimensional. The three items are registered at ironclad level according to Entry 7.
Fourth, stratum-structure count. Five families in the 4-stratum, four in the 8-stratum,
three in the 12-stratum, and two in the 16-stratum, fourteen families in total; the
parameter-space convention is: families with parameter space M have dimension 11;
the parallel family’s parameter space S 6 has dimension 6, or 7 with scale retained; the
equal-norm non-parallel branch of the mixed family has parameter space MH of dimension
12, or 13 with scale retained. This count is registered at census-pending level according
39

## PDF page 40

to Entry 7.

B.4 Entries 5 and 6 (Assembly Events)
Entry 5: the initial pipeline once used floating-point elimination to read kernel dimensions; on one 16-dimensional matrix, the floating-point reading judged it full rank while
the determinant reading judged it singular, and arbitration located the cause as pivot
discrimination failing after intermediate quantities exceed 253 . Disposition: all kernel dimensions were re-read by exact integer algorithms; the floating-point reading was voided
but not erased, and was registered in the ledger; floating-point rank writing into the
protocol was forbidden; the two-out-of-three cross-check of determinant, rank, and kernel
basis was listed as a fixed item. This event did not affect any ledger conclusion.
Entry 6: the coordinate placement functions once had index misalignment and dimension mismatch in two types of construction functions. Disposition: all placement
functions were equipped with input dimension assertions and declared-condition assertions, including purely imaginary, equal norm, orthogonality, the Moreno condition, and
slot placement; there was zero recurrence thereafter.

B.5 Absence Registration
The following are registered as boundaries that must be completed or explicitly retained
before finalization. The complete catalogue is not proved; the incompleteness of the
basic seven families already has an explicit counterexample, and whether there are zero
divisors beyond the seven new families is an open problem. The census of no fewer than
8 random Moreno samples for each of the seven new families is incomplete; the 169-cell
cross rescan is incomplete; the binary-support full scan is incomplete; the determinant
exponents of the new families have not been determined. The supplemental registration
and recomputation of the 8 × 8 symbolic-pattern probe are incomplete, and its reading is
not entered into the ledger. The stratified generalization to A6 and higher dimensions has
not been carried out. Closed-item registration: the vector-by-vector verification of the
16-vector basis in Appendix D has been completed (16/16, rank 16, including rows 10 and
11), and the F ′ basis is closed simultaneously via slot swap; the step det Rm̄ = det Lm
in E.1 has passed recomputation (8/8); the sample evidence for the two determinant
laws is registered as 30/30, 54/54, and supplementary batches 8/8, 6/6 (same verification
protocol, independent random seeds), and general proofs remain to be built.

Appendix C: Low-Dimensional Multiplication Tables
and Convention Examples
This appendix gives the lowest-dimensional examples of the multiplication convention,
so that the doubling formula of Section 3.1 of Chapter 3 can be verified without external
references, and provides hand-verifiable anchors for the left-right multiplication directions
of the BDI interface of Chapter 6.
40

## PDF page 41

C.1 Complex Layer (n = 1)
Basis {e0 = 1, e1 }, e21 = −e0 , and conjugation maps e1 to −e1 .

C.2 Quaternion Layer (n = 2)
Basis {e0 , e1 , e2 , e3 }, with e2 = (0, 1) as the companion unit. Nontrivial products:
e1 e2 = e3 ,

e2 e1 = −e3 ,

e22 = e23 = −e0 ,

e1 e3 = −e2 ,

e3 e1 = e2 ,

e2 e3 = e1 ,

e3 e2 = −e1 .

C.3 Companion-Unit Block of the Sedenion Layer (n = 4, e8 )
e8 = (0, 1) ∈ O ⊕ S. Its multiplication block is characterized by the following readings:
e8 e0 = e0 e8 = e8 ,

e28 = −e0 ;

for j = 1, . . . , 7:
e8 · ej = −e8+j ,

ej · e8 = +e8+j .

That is, left multiplication by e8 sends the first-slot basis ej into the second slot with a
minus sign, while right multiplication by e8 sends it into the second slot without a minus
sign. Left and right multiplication differ only by a sign, and this sign difference acts only
on purely imaginary elements. This is the minimal example for calibrating the left-right
multiplication directions of Chapter 6: for the same ej , left and right multiplication by
e8 give two elements differing by a minus sign, and any formula depending on the action
direction of i4 must first fix the left-right multiplication convention.

C.4 Companion Unit of the Trigintaduonion Layer (n = 5, e16 )
e16 = (0, 1) ∈ S⊕S. Sample readings (u = e1 placed in the first slot of the first component,
i.e., index 1):
e16 · (u, 0) = (0, −u), index 17, coefficient − 1;
(u, 0) · e16 = (0, u),

index 17, coefficient + 1.

In general, e16 · (u, 0) = (0, −ū) has the conjugate term intervene only when u has a
real part; for purely imaginary u, left multiplication sends into the second slot with a
minus sign and right multiplication sends into the second slot with a plus sign, and the
sign rule is completely consistent with e8 in C.3. This regularity comes from the same
skeleton of the doubling formula and can serve as an additional probe for the correctness
of cross-layer assembly of the multiplication table.

C.5 Flexibility Readings
The flexibility law (xy)x = x(yx) has zero failures on 200 random integer samples each
for n = 4 and n = 5; alternativity already fails at n = 4. These two readings together
bind “the multiplication table is correct” with “the algebraic structure conforms to the
41

## PDF page 42

Cayley–Dickson tower theory”: flexibility holds identically while alternativity fails exactly
at S, which is precisely the profile predicted by the theory.

Appendix D: Explicit Kernel Construction for the 16Stratum Double Families
This appendix gives the explicit kernel-construction expansion of Theorem 4.8 of Chapter
4. For the representative element of the F family
x0 = ((a, b), (b, −a)),

(a, b) = (e1 , e2 ),

indices {1, 10, 18, −25},

an explicit basis (16 vectors) of the annihilator is given, and the correspondence of the
structured subfamilies is registered. Indices 0 through 15 are the first component m1 ,
and 16 through 31 are the second component m2 .

D.1 Explicit Basis
Each vector in the table below gives its nonzero coordinates (index: coefficient).
#
1
2
3
4
5
6
7
8
9
10

Nonzero coordinates
7, 12
6 : −1, 13
5, 14
4 : −1, 15
11 : −1, 19
7, 20
6 : −1, 21
5, 22
4 : −1, 23
1, 10 : −1, 18, 25

11

2, 9, 17 : −1, 26

12

3, 27

13
14
15
16

4, 28
5, 29
6, 30
7, 31

Note
Block 1: AnnS (a, b) placed in m1

Block 2: cross-slot lifting terms

Block 4: structured candidate,
verified
Block 4: structured candidate,
verified
Block 3: type m1 = (ej , 0),
m2 = (0, ej )

D.2 Structural Interpretation
Block 1 (vectors 1 through 4) is the four-dimensional basis of AnnS (e1 , e2 ) placed in the
first component with the second component zero: type ((x, y), 0). Block 3 (vectors 12
through 16) has the form m1 = (ej , 0), m2 = (0, ej ) (j = 3, . . . , 7).
The coordinate-by-coordinate substitution verification of vectors 10 and 11 has been
completed: both are annihilated by left multiplication by x0 , the 16 vectors are linearly
independent as a whole (rank 16, Chapter 2 ledger), and the “pending verification” status
of rows 10 and 11 is closed. Their structural interpretation is registered as an explanatory
42

## PDF page 43

remark: the nonzero coordinates of vector 10 are {1, 10 : −1, 18, 25}, and those of vector
11 are {2, 9, 17 : −1, 26}; if one substitutes (x, y) = (b, a) or other independent elements
of AnnS (a, b) according to the template “((x, y), (y, −x))”, the resulting supports do not
exactly match the above coordinate sets, so this template correspondence is not written
as a structural conclusion but is retained only as a geometric-origin comment for rows 10
and 11.
Block 2 (vectors 5 through 9) consists of cross-slot lifting terms, registered according
to the kernel-basis reading. The coordinate-by-coordinate substitution verification of left
multiplication of each of the above 16 vectors by x0 has been closed (16/16).

D.3 Dimension Closure
The number of basis vectors, 16, is consistent with the kernel-dimension reading 16 of
the left-multiplication matrix; the right-annihilator dimension, read independently, is also
16, consistent with the left-right annihilator identity law. The coordinate-by-coordinate
substitution verification of left multiplication of each of the 16 vectors by x0 has been
completed (rank 16, Chapter 2 ledger), and the explicit basis is a verified construction; the
dimension 16 is still used at the census level of Entry 3 of Chapter 2, and the parameterby-parameter general proof remains to be built.

D.4 Basis of F ′
The annihilator basis of F ′ = ψ(F ) is obtained from the entire table of D.1 by slot swap
(interchanging indices i and i + 16). ψ is not an algebra automorphism (registered in
Section 6.1 of Chapter 6), so the kernel of F ′ is not the image of the kernel of F under
an algebra isomorphism; the two have the same dimension 16 and respectively realize the
two copies of V2 (R7 ) of the BDI topological theorem. The verification of the 16-vector
basis of F has been closed (16/16, rank 16), and the F ′ basis is derived by slot swap,
with vector-by-vector verification holding simultaneously, and is registered as closed.

Appendix E: Derivation Skeletons for the Two Determinant Laws
This appendix gives the derivation paths of Theorems 5.1 and 5.2 of Chapter 5 and the
special cases that can be closed by verification, so that the two laws are not merely sample
induction. All determinant readings use fraction-free elimination as the primary path,
with independent fraction-free LU or a computer algebra system as a supplementary
check; two-out-of-three arbitration follows Clause 3 of Chapter 2.

43

## PDF page 44

E.1 Block Structure of the Axis Family
Let x = (m, 0) ∈ S ⊕ S, m = (a, b) ∈ S. By the doubling formula, for (p, q) ∈ S ⊕ S, left
multiplication is
x(p, q) = (m, 0)(p, q) = (mp, qm).
That is, the left-multiplication operator Lx is block diagonal, with the two blocks being
Lm and Rm on S:
Lx = diag(Lm , Rm ).
Hence det Lx = det Lm · det Rm . The conjugate anti-automorphism C conjugates right
multiplication to left multiplication: CRm C −1 = Lm̄ , so det Rm = det Lm̄ = det Lm
(when m is purely imaginary, m̄ = −m, and 16 is even-dimensional). Hence det Lx =
(det Lm )2 : the determinant of the A5 axis family is the square of the S-layer determinant.
The n = 4 layer law det L(a,b) = D14 D22 holds exactly on 30/30 or more random samples
(Entry 3 of Chapter 2, census level), and the exponents are doubled by the square to (8, 4),
consistent with Theorem 5.1. The step det Rm = det Lm has passed ledger recomputation
8/8 and is closed; the general proof of this step is registered with Open Problem 2 of
Chapter 8.

E.2 Hand-Computable Closed Special Cases
Take b = 0: D2 = (∥a∥2 )2 = D12 , and the A5 -layer law degenerates to det Lx = D18 ·(D12 )4 =
D116 = ∥a∥32 . For a = e1 + 2e2 (D1 = 5), the A5 -layer 32 × 32 machine-check reading
is det Lx = 516 = 152587890625; the S-layer 16 × 16 reading for the same parameter is
det Lm = D14 D22 = 58 = 390625, exactly the square of the A5 -layer reading, consistent
with the square structure of E.1. Both readings were read by fraction-free elimination
and independent fraction-free LU decomposition on two paths, and the results agree.
This case simultaneously verifies the matrix assembly and the determinant routine.

E.3 Structure and Exponent Origin of the Cross Family
Let x = ((a, 0), (b, 0)). The left-multiplication operator is no longer block diagonal; its
32 × 32 matrix, under the (slot one | slot two) decomposition, has a block-triangular
perturbed form, with the two blocks controlled by operators of type L((a,0)) and R((b,0))
respectively. The difference between the exponent pattern (α, β) = (4, 6) and the axis
family’s (8, 4) comes from this structural difference: the exponent of D1 is contributed
half by each slot (4 = 8/2), and the exponent of D2 is raised by the multiplicative closure
of the cross terms. The factorization of 54/54 samples (24 random plus 30 verification)
has no exceptions (Entry 3 of Chapter 2, census level); the general proof remains to be
built and is not closed in this appendix.

E.4 Zero Characterization of D2
D2 = (∥a∥2 − ∥b∥2 )2 + 4⟨a, b⟩2 is the sum of two real square terms, so D2 = 0 if and only if
both expressions vanish simultaneously, i.e., equal norm and orthogonal, which is exactly
the Moreno condition. Hence for the axis and cross families, det Lx = 0 is synchronized

44

## PDF page 45

with the zero-divisor locus within the family. This synchronization is limited to D1 D2 type families and is not extrapolated to a statement about the whole catalogue; the
zero-divisor conditions and determinant types of the parallel family, the double-two-slot
family, and the mixed family are handled according to the pending-determination list of
Section 5.5 of Chapter 5.

E.5 Remaining Determinations
Families among the basic families whose determinant exponents have not yet been de(1)
(2)
termined: the 4-stratum double families F4 , F4 , the 8-stratum diagonal family Dg,
and the 16-stratum double families F and F ′ . Seven new families: G1 , G2 , G3 , the
second-slot axis family Ax2 , the equal-norm non-parallel branch of the mixed family H,
the parallel family P , and the double-two-slot family B. For families parameterized by
M , test whether there exist nonnegative integers α, β such that det Lx = D1α D2β ; the parallel family is given candidate factors expressed in terms of the norm of u and a quartic
invariant, with D2 = 0 not used as its zero-divisor discriminant. Whether the unified
form ∆ = D1α D2β covers all construction sectors is Open Problem 2 of Chapter 8.

Appendix F: BDI Convention-Calibration Comparison Tables
This appendix turns the stratum-membership recomputation and left-right multiplication
direction alignment of Chapter 6 into machine-checkable comparison tables. In the leftcolumn objects, a satisfies a ⊥ C4 (C4 = ⟨1, e8 ⟩), i.e., a = (u, 0), u ∈ Im O.

45

## PDF page 46

F.1 Shapes and Stratum Membership
Machine-check reading under this
paper’s convention

Object

BDI literature
paraphrase

(a, i4 · a)

Zero divisor, dimension
2n − 4 + dim Ann(a)
(top-layer direction)

(a, −i4 · a)

Same as above, two
branches of the same
dimension

Top-layer first
copy

One of the 2n−4 copies of
V2 (R7 )

Left-annihilator dimension 12;
((u, 0), (0, −u)) is the ε = −1 branch
of the parallel family P

Left-annihilator dimension 12;
((u, 0), (0, u)) is the ε = +1 branch of
the parallel family P

F family, dimension 16, parameter
space M

Top-layer second
copy

Same as above

F ′ = ψ(F ), dimension 16, ψ not an
algebra automorphism

Left-right
annihilator
identity

Corollary 9.3

Holds for each registered family

Main theorem

All observed strata {0, 4, 8, 12, 16}
satisfy it; the 0-stratum consists of
nonzero invertible elements and is not
a zero-divisor stratum

Divisibility by 4
and upper
bound 16

Membership and
translation
Left multiplication by i4
under this paper’s
convention maps (u, 0) to
(0, −u), see Appendix
C.4; the shape is realized
in the parallel family, not
in the top-layer F family
The two branches differ
only in the sign of the
second component;
stratum membership is
also the 12-stratum
Theorem 4.8 of Chapter 4
Theorem 4.8 of Chapter 4
and Appendix D
Entry 4 of Chapter 2,
census level
Section 3.4 of Chapter 3
and Corollary 4.9 of
Chapter 4

F.2 Family-Action Table for φ
Define φ(u, v) = (u, −v). φ is an A5 algebra automorphism, with the identity proof in
Remark 4.1.1 of Chapter 4; 120 random samples are retained as assembly probes (Entry
7 of Chapter 2, ironclad level). The verified family actions are as follows.
Family
(1)

F4

(2)

Image
G1 = ((a, b), (−b, −a))

= ((a, b), (b, a))

F4 = ((a, b), (a, −b))
Dg = ((a, b), (a, b))
Other families

G2 = ((a, b), (−a, b))
G3 = ((a, b), (−a, −b))
Per-family verification registered as
pending census items
(1)

(2)

Note
Template-level identity, holding
parameter by parameter
Same as above
Same as above
Not written as a general conclusion

(2)

φ does not interchange F4 and F4 ; the template ((a, b), (a, −b)) of F4 cannot be
rewritten as ((a, b), (−a, b)). The three family actions are all template-level identities,
registered at ironclad level according to Entry 7.

46

## PDF page 47

F.3 New-Family Comparison
Family

Stratum

Parameter space

Stratum-dimension evidence
level
Census level (automorphism
(1)
inheritance from F4 , Remark
4.1.1)
Census level (automorphism
(2)
inheritance from F4 , Remark
4.1.1)
Census level (automorphism
inheritance from the diagonal
family, Remark 4.1.1)

G1 = ((a, b), (−b, −a))

4

M , dimension 11

G2 = ((a, b), (−a, b))

4

M , dimension 11

G3 = ((a, b), (−a, −b))

8

M , dimension 11

Second-slot axis family
Ax2 = (0, (a, b))

8

M , dimension 11

Strict proof (block structure,
Theorem 4.4)

Equal-norm non-parallel
branch of H

4

MH , dimension 12 (dimension 13
with scale)

Probe level, conditional profile

Parallel family
P = ((u, 0), (0, εu))

12

S 6 , dimension 6 (dimension 7 with
scale)

Ironclad level (five probes plus
two signs)

Double-two-slot family
B = ((0, a), (0, b))

12

M , dimension 11

Probe level

F.4 Translation Rule
The shapes (a, ±i4 · a) generated by the action of i4 in the BDI paraphrase fall, under
this paper’s multiplication convention, into the 12-stratum parallel family P , not the
4-stratum; the two copies of V2 (R7 ) in the top stratum are realized by F and ψ(F ). The
stratum difference is explained by parallel-family membership and three-path recomputation readings, not solely by the left-right multiplication convention of i4 ; the compatibility
of the invertible branch of a with the stratum dimension 12 of the parallel family is registered according to Section 6.2 of Chapter 6. This translation rule does not affect the
conclusions of the BDI topological theorem, nor any dimension assertion in this paper’s
catalogue.

Appendix G: Reproducibility Package
G.1 Recursive Multiplication-Table Generation Algorithm Description
Input: number of layers k. Output: multiplication table of the basis of Ak (sign-index
pairs).
If k = 0, return the trivial table. Otherwise, recursively generate the Ak−1 table and
the conjugation table, and synthesize Ak according to the doubling formula of Section 3.1
of Chapter 3: for the index decompositions i = (ia , ib ) and j = (ja , jb ), where ib , jb ∈ {0, 1}
are slots; the four branches correspond to (ib , jb ) = (0, 0), (1, 1), (0, 1), (1, 0), and fall into
the corresponding slots according to the doubling formula. After each layer is generated,
spot checks of sign consistency and closure are performed (Appendix B.1).

47

## PDF page 48

G.2 Exact Rank and Kernel-Basis Algorithm Description
Input: left-multiplication matrix M (integer). Output: rank, kernel basis.
Use fraction-free Gaussian elimination (Bareiss type without fraction pivots) to reduce
to reduced row echelon form; pivot columns correspond to the rank, and free columns
generate kernel-basis vectors one by one. Floating-point pivots are forbidden (Entry 5
of Chapter 2). The kernel basis and rank readings are additionally re-read by two-prime
modular rank (109 + 7, 109 + 9) and reconciled according to Clause 1.

G.3 Exact Determinant Algorithm Description
Input: integer square matrix. Output: determinant (integer or fraction).
Bareiss fraction-free elimination; in case of conflict reconciliation, an independently
implemented fraction-free LU decomposition is used as the second path, and the results
of the two paths must agree digit by digit (the two-out-of-three discipline of Clause 3 of
Chapter 2). When the determinant is zero but the rank reading is nonsingular, handle
it by conflict arbitration; when the construction input claims a zero divisor but the
determinant is nonzero, the construction input is voided and registered.

G.4 Census Main-Loop Algorithm Description
For each registered family: generate construction inputs; execute assertions (dimension,
purely imaginary, equal norm, orthogonality, Moreno condition, slot placement); compute
the left-multiplication matrix; read the kernel dimension and kernel basis by fraction-free
elimination; re-read by two-prime modular rank and reconcile; read the determinant by
fraction-free elimination and verify by an independent path; compare the zeros of D2
with the Moreno condition; reconcile (determinant, rank, kernel basis two-out-of-three);
register readings, sample size, evidence level, random seed, and arbitration records. The
census first executes the golden self-check at n = 4 (Appendix B.2), and after calibration
passes it is transplanted verbatim to n = 5.

G.5 Random-Seed Registry
Flexibility and alternativity readings (Appendix C.5, Entry 1 of Chapter 2): seeds 7
(n = 4 flexibility), 8 (n = 5 flexibility), 9 (n = 4 alternativity), 200 samples each, with
random integer entries drawn from [−2, 2].
Determinant-law sampling (Appendix E): seeds 11 (n = 4 law), 12 (axis family), 13
(cross family).
Seeds for the golden self-check and random samples of the basic families: see the
sample-size entries of Appendix B.2 and B.3; all samples are fully replayable according
to the registered seeds.
Census seeds for the seven new families: G1 seed 21, G2 seed 22, G3 seed 23, secondslot axis family Ax2 seed 24, equal-norm non-parallel branch of the mixed family H seed
25, parallel family P seed 26, double-two-slot family B seed 27; each family has no fewer
than 8 random Moreno samples, and the parallel family additionally takes five nonzero
purely imaginary octonion probes and the two sign branches.
48

## PDF page 49

Binary-support full scan: deterministic enumeration of ei ± ej , ordered pairs i ̸= j,
double signs, 32 × 31 × 2 = 1984 formal strings, no randomness.
169-cell cross rescan: seed 31; parallel-probe extension: seed 32; equal-norm nonorthogonal probes: seed 33.
(1)
(2)
Determination of determinant exponents: seeds 41 (F4 ), 42 (F4 ), 43 (Dg), 44 (G3 ),
45 (Ax2 ), 46 (three branches of H), 47 (P , B, F , F ′ ).
The enumeration of the 42 unit pairs (Appendix A.2) is deterministic, with no randomness.

G.6 Description of Differences Between Two Independent Implementation Paths
Path one: recursive (sign, index) multiplication table plus fraction-free Gaussian elimination, fully self-implemented. Path two: the built-in matrix null-space and determinant
routines of a computer algebra system, with multiplication carried out by its built-in nonassociative algebra operations. The two paths are independent in the multiplication-table
structure: one is explicit table lookup, and the other is direct arithmetic computation;
they agree case by case on the 16-stratum double families (Entry 3 of Chapter 2), and
the probability that an assembly error simultaneously escapes both paths is negligible.
Two-prime modular rank serves as a third reading path, used for reconciliation rather
than replacing the primary path of fraction-free elimination.

49
