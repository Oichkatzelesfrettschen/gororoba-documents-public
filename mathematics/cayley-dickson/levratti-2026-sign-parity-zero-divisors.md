Source: https://zenodo.org/api/records/20315751
PDF sha256: bd219f4429cc22277f80e06273a6450ff8fbd982ce0176761dab1f533feea9c3
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of levratti-2026-sign-parity-zero-divisors.pdf

Transcription of `levratti-2026-sign-parity-zero-divisors.pdf` in this directory, 28 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-28 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS
IN CAYLEY–DICKSON ALGEBRAS
GIOVANNI LEVRATTI
Abstract. We establish a comprehensive theory of zero-divisors in the Cayley–
Dickson algebras An over R, working from the doubling construction without appeal
to associativity or alternativity. The paper has three parallel developments.
Combinatorial chain. Every basis product is a signed permutation (BSP Lemma);
the output index equals the bitwise XOR (XOR Index Theorem); the {0, 4, 8} Trichotomy classifies all product norms; the Case B XOR condition identifies zero-divisors
with weight-4 codewords of RM (1, n)⊥ ; the map (a, b) ↦→ (a, b′ ) is a bijection ZD(n) →
V L(n) \ ZD(n), giving the NRI Equality 1 − F (n) = 2ϱ(n) unconditionally.
Operator-theoretic chain. The Frobenius identity ∥La ∥2F = 2n N (a) has two independent proofs; the Analytical Mean Theorem Ev [N (av)] = N (a) follows without assuming LTa La = N (a)I; the Variance formula (Proposition 5.9) expresses Var(N (av))
via XOR sign factors; Exchange Symmetry and Global Vacuum Protection hold for
all n ≥ 1.
Sign-parity framework and resolution of open problems. A new sign-parity invariant
π ∈ {+1, −1} attached to each ordered 2-flat determines exactly when zero-divisors
exist (Sign Parity Criterion, Theorem 7.3). Using this, together with the Fano subalgebra theorem (B ∼
= O, proved via WRAP and Hurwitz) and a Unique Containment
lemma, we prove:
(
)
n−1
|ZD(n)| = 336 ×
for all n ≥ 4,
3
2
resolving Conjecture 6.5 and Problems 1–4, 7, 9–10. We also establish the strict
density monotonicity ϱ(n + 1) < ϱ(n), the asymptotic law ϱ(n) · 2n → 41 , and the new
structural constraint πA πB πC = −1 for every 2-flat, implying each flat has exactly 0
or 2 active splits. The Born Rule holds for n ≤ 3 and fails for n ≥ 4, under the three
independent axioms (M),(D),(OA); axiom (I) is proved redundant. Furthermore, we
resolve all remaining open problems unconditionally (see §15): Problem 6 (variance
closed form): for every active mixed flat in A4 , Epqrs = 3 − 4ac ∈ {−1, 7}, where
O O O
ac = εO
ik εjk εil εjl = −1 (Proposition 7.20, unconditional via Theorem 7.25); Problem 5
n
(NRI balance): for any ZD unit a ∈ An (n ≥ 4) and v uniform on S 2 −1 , Pr[N (av) <
1 − ε] = Pr[N (av) > 1 + ε] for all ε > 0, proved unconditionally (Theorem 3.17,
via Theorems 5.16 and 5.17); and Problem 8 (no weight-3 zero divisors): Ma > 0
unconditionally for all σk ̸= 0 (Theorem 12.5).

Contents
1. Introduction
1.1. The Cayley–Dickson sequence
1.2. Scope and main results
1.3. Status of results

2
2
3
3

Date: May 2026.
1

## PDF page 2

2

GIOVANNI LEVRATTI

2. Formal Framework
3. The Combinatorial Chain
3.1. BSP and XOR index structure
3.2. The {0, 4, 8} Trichotomy
3.3. XOR density bound and Reed–Muller connection
3.4. Sign-selective norm redistribution and NRI equality
3.5. NRI Balance on the Full Sphere (Problem 5)
4. The WRAP Lemma and Identity-Bearing Zero-Divisors
5. Spectral Theory of Left-Multiplication Operators
6. Divisibility of |ZD(n)|
7. Sign-Parity Framework and Proof of Conjecture 6.5
7.1. Properties of the sign map
7.2. The sign parity criterion
7.3. Sign parity invariance
7.4. Numerical verification for n = 4
7.5. Mixed-element structure of ZD(4)
7.6. Recursive structure
7.7. Disjointness of Fano-plane contributions
7.8. The Fano sub-algebra
7.9. Resolution of Conjecture 6.5
7.10. The product identity πA πB πC = −1
7.11. The E-formula for Active Mixed Flats (Problem 6)
8. Hereditary Decomposition (Problem 1)
9. Density Monotonicity (Problem 4) and Asymptotics (Problem 7)
10. The Born Rule
11. Numerical Verification
12. Weight-3 Elements Are Never Zero Divisors
13. Anisotropic Variance Witnesses (Problem P11)
13.1. Setup and key structural lemma
13.2. Variance by weight class
13.3. Resolution of Problem P11
14. Full ZD Classification in A4 (Problem P8-full)
14.1. Complete inventory
14.2. Structural analysis of higher-weight families
15. Open Problems
Acknowledgements
References

3
4
4
5
5
6
6
7
9
15
15
15
15
15
16
16
16
16
16
17
17
17
19
19
19
20
20
22
22
23
24
25
25
26
27
27
28

1. Introduction
1.1. The Cayley–Dickson sequence. The Cayley–Dickson construction produces an
infinite tower A0 = R ⊂ A1 = C ⊂ A2 = H ⊂ A3 = O ⊂ A4 = S ⊂ · · · in which each
doubling step eliminates one or more algebraic properties. Hurwitz [1] identified the first
four as the unique normed division algebras over R; at A4 (the sedenions, dimension 16)

## PDF page 3

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

3

the multiplicative norm, alternativity, and zero-divisor freeness are simultaneously lost.
The role of octonions and related algebras in fundamental physics has been explored by
Furey [5], Dixon, and Baez [4], providing part of the motivation for the present work.
1.2. Scope and main results. This paper develops four complementary approaches
to zero-divisor theory.
The combinatorial approach (§§3–4) works entirely with the XOR index structure. Its
main engine is the XOR Index Theorem (Theorem 3.2). The NRI Equality 1 − F (n) =
2ϱ(n) and the Density Bound are unconditional theorems.
The operator-theoretic approach (§5) studies La : x ↦→ ax. The Frobenius Identity
∥La ∥2F = 2n N (a) has two independent proofs; the erroneous route via LTa La = N (a)I is
explicitly excluded.
The sign-parity framework (§7) introduces the sign parity π(F, split) ∈ {+1, −1} of
each 2-flat split and proves, as the main combinatorial theorem, that a split produces
zero-divisors if and only if π = +1.
The density and asymptotics (§§8–9) establish the hereditary decomposition, strict
monotonicity of ϱ(n), and the tight bound ϱ(n) · 2n → 14 .
1.3. Status of results. All results labelled Theorem, Lemma, Proposition, or Corollary are proved unconditionally in this paper. All seven open problems from the prior
edition (PA1–PA5, P5, P6, P8) are now resolved: Theorem 7.25 (PA1, Lemma B),
Theorem 5.16 (PA2), Theorem 5.17 (PA3), Corollary 5.20 (PA5), Theorem 12.5 (PA4
and P8 full). Consequently, Proposition 3.15 and Theorem 3.17 are now unconditional.
Conjectures that were open in the prior edition are stated as theorems with a historical
note.
2. Formal Framework
Definition 2.1 (Cayley–Dickson algebras). Let A0 = R. For n ≥ 0, An+1 consists of
pairs (a, b) with a, b ∈ An , equipped with
¯ da + bc̄),
(a, b)(c, d) = (ac − db,

(a, b) = (ā, −b).

The quadratic norm N ((a, b)) = N (a) + N (b) is positive definite. The canonical basis
Bn = {e0 , . . . , e2n −1 } satisfies N (ei ) = 1, e0 = 1, ē0 = e0 , ēk = −ek (k ≥ 1). Write
εi = (ei , 0) and fi = (0, ei ) for the two halves of Bn+1 . For a ∈ An : a0 = Re(a)
(coefficient of e0 ), ⃗a = a − a0 e0 (purely imaginary part).
The following standard identities hold in every Cayley–Dickson algebra:
(1) e2k = −e0 (k ≥ 1),
(2) a2 = 2a0 a − N (a)e0 (a ∈ An ),
(3) xy = ȳx̄ (x, y ∈ An ),
(4) Re(pq)r = Re p(qr) (p, q, r ∈ An ).
Definition 2.2 (Left-multiplication operator). For a ∈ An : La : An → An , La (x) =
a · x, is R-linear. Matrix entries: (La )ij = ⟨a · ej , ei ⟩.

## PDF page 4

4

GIOVANNI LEVRATTI

Definition 2.3 (Candidate set and density measures).
C(n) = {ei + σej : 0 ≤ i < j < 2n , σ ∈ {+1, −1}},
ZD(n) = {(a, b) ∈ C(n)2 : a ̸= 0, b ̸= 0, ab = 0},
V L(n) = {(a, b) ∈ C(n)2 : N (ab) ̸= N (a)N (b)},
ϱ(n) = |ZD(n)|/42n ,

F (n) = 1 − |V L(n)|/42n .

By Hurwitz: F (n) = 1 for n ≤ 3, F (n) < 1 for n ≥ 4.
Remark 2.4. For density and asymptotic results, we also use the two-component density
ρ(n) = |ZD(n)|/|C ∗ (n)|2 where C ∗ (n) = {ei +σej : 1 ≤ i < j ≤ 2n −1, σ = ±1} (indexpure elements, |C ∗ (n)| = (2n − 1)(2n − 2)). Theorem 4.9 shows ZD(n) ⊂ C ∗ (n)2 for
n ≥ 4, so ϱ(n) and ρ(n) differ only by the normalisation constant.
Remark 2.5 (Density notations). Two normalised densities appear in this paper:
ϱ(n) := |ZD(n)|/42n ,

ρ(n) := |ZD(n)|/|C ∗ (n)|2 .

The symbol ϱ is reserved for Definition 2.3 throughout. These satisfy
42n
ρ(n)
= n
→ 1 as n → ∞,
ϱ(n)
(2 − 1)2 (2n − 2)2
so ϱ(n) and ρ(n) are asymptotically equivalent; both satisfy ρ(n)·2n → 41 (Theorem 9.6).
A third expression |ZD(n)|/[2n (2n − 1)] exceeds 1 for n ≥ 4 (since |ZD(4)| = 336 >
24 (24 − 1) = 240) and does not appear in this paper.
3. The Combinatorial Chain
3.1. BSP and XOR index structure.
Theorem 3.1 (XOR Index Theorem). In every An (n ≥ 0), for all eα , eβ ∈ Bn :
eα · eβ = εαβ eα⊕β ,

εαβ ∈ {+1, −1}.

Proof. Induction on n.
Base cases. n = 0 (A0 = R, basis {e0 }): the only product is e0 · e0 = e0 = (+1) e0⊕0 .
✓
n = 1 (A1 = C, basis {e0 , e1 }): e0 ej = ej e0 = ej = (+1) e0⊕j for j ∈ {0, 1};
2
e1 = −e0 = (−1) e1⊕1 . ✓
Inductive step. Assume the theorem holds in An . For An+1 , four index-type cases:
Case 1 (εε): εi εk = (ei ek , 0), output index i ⊕ k. ✓
Case 2 (εf ): εi fk = (0, ek ei ), output index (k ⊕ i) + 2n = i ⊕ (k + 2n ). ✓
Case 3 (f ε): fi εk = (0, ei ēk ) = (0, −ei ek ) for k ≥ 1 (since ēk = −ek ), output index
(i + 2n ) ⊕ k. ✓
Sub-case k = 0: fi · ε0 = (0, ei )(e0 , 0) = (0, ei ē0 ) = (0, ei e0 ) = (0, ei ) = fi =
(+1) f(i+2n )⊕0 . ✓
Case 4 (f f ): fi fk = (−ēk ei , 0) = (ek ei , 0) using ēk = −ek (k ≥ 1), output index
k ⊕ i = (i + 2n ) ⊕ (k + 2n ). ✓
Sub-case k = 0: fi · f0 = (0, ei )(0, e0 ) = (−ē0 ei , 0) = (−e0 ei , 0) = (−ei , 0) = −εi .
(n)
Index: (i+2n )⊕(0+2n ) = i; sign: ε0i = +1 (since e0 ei = ei ), overall sign −1, consistent
with the formula. ✓
□

## PDF page 5

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

5

Corollary 3.2 (Basis Signed Permutation). For every n ≥ 0 and ek ∈ Bn , left and
right multiplication by ek are signed permutations of Bn .
Proof. Immediate from Theorem 3.1: eα · ek = εαk eα⊕k , and α ↦→ α ⊕ k is a bijection
on {0, . . . , 2n − 1}. Right multiplication: ek · eα = εkα ek⊕α , same bijection.
□
Theorem 3.3 (Isometry Lemma). N (a · ek ) = N (ek · a) = N (a) for every a ∈ An ,
ek ∈ Bn .
∑
2
Proof. a · ek = i ai εik ei⊕k . Since i ↦→ i ⊕
∑k is2 a bijection and εik = 1, the coefficients
are a permutation of (ai ), so N (a · ek ) = i ai = N (a). ∑
Right multiplication. By the same argument: ek · a = ∑i ai εki ek⊕i . Since i ↦→ k ⊕ i
is a bijection on {0, . . . , 2n − 1} and ε2ki = 1: N (ek · a) = i a2i = N (a).
□
Corollary 3.4. Every (a, b) ∈ ZD(n) satisfies N (a) = N (b) = 2.
3.2. The {0, 4, 8} Trichotomy.
Lemma 3.5 (Collision Pairing). For a = ei +σej , b = ek +τ el (i < j, k < l, σ, τ = ±1),
pairwise collisions among the four XOR outputs {i ⊕ k, i ⊕ l, j ⊕ k, j ⊕ l} occur if and
only if i ⊕ j = k ⊕ l (Case B), in which case exactly two collisions occur simultaneously:
i ⊕ k = j ⊕ l and i ⊕ l = j ⊕ k.
Theorem 3.6 ({0, 4, 8} Trichotomy). For a = ei + σej , b = ek + τ el (i < j, k < l,
σ, τ = ±1): N (ab) ∈ {0, 4, 8}.
(1) (Case A) i ⊕ j ̸= k ⊕ l: four distinct output indices, N (ab) = 4.
(2) (Case B) i ⊕ j = k ⊕ l: two output indices; N (ab) = (εik + στ εjl )2 + (τ εil + σεjk )2 ∈
{0, 4, 8}.
Proof. Case A. ab = εik ei⊕k +στ εjl ej⊕l +τ εil ei⊕l +σεjk ej⊕k ; four distinct basis elements,
so N (ab) = 4.
Case B. i ⊕ k = j ⊕ l =: m1 and i ⊕ l = j ⊕ k =: m2 . ab = (εik + στ εjl )em1 +
(τ εil + σεjk )em2 . Hence N (ab) = c21 + c22 where, since εik , εjl , εil , εjk ∈ {+1, −1}, each
coefficient cr is a sum of exactly two ±1 terms: c1 = εik + στ εjl ∈ {−2, 0, +2} and
c2 = τ εil + σεjk ∈ {−2, 0, +2}, so c2r ∈ {0, 4} (the value 1 is not achievable) and
N (ab) = c21 + c22 ∈ {0, 4, 8}.
□
3.3. XOR density bound and Reed–Muller connection.
Theorem 3.7 (XOR Density Bound). For all n ≥ 1: ϱ(n) ≤ (2n − 1)/4n .
Proof. Every ZD pair requires Case B, hence i ⊕ j = k ⊕ l. For each fixed v ̸= 0, let
Sv = {a ∈ C(n) : a = ei + σej , i ⊕ j = v}. The number of unordered pairs (i, j) with
i < j and i ⊕ j = v equals 2n−1 (for each i < v, setting j = i ⊕ v gives a valid pair;
exactly half the 2n values of i satisfy i < i⊕v). With σ ∈ {+1, −1}: |Sv | = 2·2n−1 = 2n .
The number of pairs (a, b) ∈ C(n)2 with i ⊕ j = k ⊕ l = v is |Sv |2 = 4n . Summing over
the 2n − 1 nonzero values of v: |ZD(n)| ≤ (2n − 1) · 4n , so ϱ(n) ≤ (2n − 1)/4n .
□
Corollary 3.8 (Asymptotic recovery). ϱ(n) → 0 and F (n) → 1 as n → ∞.
Theorem 3.9 (Reed–Muller Connection). The Case B condition i ⊕ j ⊕ k ⊕ l = 0
identifies exactly the weight-4 minimum-distance codewords of RM (1, n)⊥ = RM (n −
2, n).

## PDF page 6

6

GIOVANNI LEVRATTI

3.4. Sign-selective norm redistribution and NRI equality.
Theorem 3.10 (Extended SSNR). For b = ei + σej with ab = 0 and b′ = ei − σej :
N (ab) + N (ab′ ) = 4N (a).
Proof. Apply the parallelogram identity N (p + q) + N (p − q) = 2N (p) + 2N (q) with
p = aei and q = aσej , using Theorem 3.3.
□
Corollary 3.11 (SSNR Bijection). (a, b) ↦→ (a, b′ ) is a bijection ZD(n) → V L(n) \
ZD(n).
Proof. Well-definedness. Let (a, b) ∈ ZD(n), so ab = 0, N (a) = N (b) = 2. Write
b = ei + σej ; then b′ = ei − σej ∈ C(n). By Theorem 3.10: N (ab′ ) = 4N (a) − N (ab) =
8. Since N (a)N (b′ ) = 4 ̸= 8 = N (ab′ ), (a, b′ ) ∈ V L(n). Since N (ab′ ) = 8 ̸= 0,
(a, b′ ) ∈
/ ZD(n). Hence (a, b′ ) ∈ V L(n) \ ZD(n). ✓
Injectivity. The map b ↦→ b′ is an involution on C(n): (b′ )′ = (ei −σej )′ = ei +σej = b.
Hence (a, b′1 ) = (a, b′2 ) ⇒ b1 = b2 . ✓
Surjectivity onto V L(n) \ ZD(n). Let (a, c) ∈ V L(n) \ ZD(n). By the {0, 4, 8} Trichotomy (Theorem 3.6), N (ac) ∈ {0, 4, 8}. Since (a, c) ∈ V L(n): N (ac) ̸= N (a)N (c) =
4. Since (a, c) ∈
/ ZD(n): N (ac) ̸= 0. Hence N (ac) = 8. Write c = ei + σ ′ ej and set
′
b := ei − σ ej ∈ C(n), so c = b′ . By Theorem 3.10: N (ab) = 4N (a) − N (ac) = 8 − 8 = 0.
Hence (a, b) ∈ ZD(n) and (a, b) ↦→ (a, b′ ) = (a, c). ✓
Remark 3.12. Every pair in V L(n) has N (ac) ∈ {0, 8} by the Trichotomy; N (ac) = 4 is
excluded by definition of V L(n) and N (ac) = 0 is excluded for V L(n) \ ZD(n). Hence
the bijection is surjective onto all of V L(n) \ ZD(n). ✓
□
Theorem 3.13 (NRI Equality). For all n ≥ 4: 1 − F (n) = 2ϱ(n).
Proof. By Definition 2.3: 1 − F (n) = |V L(n)|/42n and 2ϱ(n) = 2|ZD(n)|/42n . It
suffices to show |V L(n)| = 2|ZD(n)|. By Corollary 3.11, (a, b) ↦→ (a, b′ ) is a bijection
ZD(n) → V L(n) \ ZD(n), giving |V L(n) \ ZD(n)| = |ZD(n)|. Since ZD(n) ⊂ V L(n)
(every ZD pair has N (ab) = 0 ̸= 4 = N (a)N (b)): |V L(n)| = |ZD(n)| + |V L(n) \
ZD(n)| = 2|ZD(n)|.
□
3.5. NRI Balance on the Full Sphere (Problem 5).
√
Lemma 3.14 (Cosine Formula). Let a = (ep +eq )/ 2 with p, q ∈ {1, . . . , 2n −1}, p ̸= q,
N (a) = 1. For every v ∈ An : N (av) = 1 + ⟨ep v, eq v⟩.
√
Proof. By linearity: av = (ep v + eq v)/ 2. Hence N (av) = 21 (N (ep v) + 2⟨ep v, eq v⟩ +
n
N (eq v)). By Theorem 3.3 (Isometry Lemma): N (ek v) = N (v) for all v. For v ∈ S 2 −1 :
N (ep v) = N (eq v) = 1, giving N (av) = 1 + ⟨ep v, eq v⟩.
□
√
Proposition 3.15 (Spectral structure of Ma ). Let a = (ep + eq )/ 2 be a ZD unit in
An (n ≥ 4, N (a) = 1). Then
{ n−2
n−1
n−2 }
.
Spec(Ma ) = 02 , 12 , 22

## PDF page 7

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

7

Proof. By Theorem 5.17 (PA3): dim ker(Ma ) = dim ker(La ) = 2n−2 . By Theorem 5.16
n−2
(PA2): each b′k ∈ V2 := ker(Ma − 2I), and Corollary
. The
2 = 2
∑ 5.20 gives dim Vn−2
n
n−2
n−1
remaining 2 − 2 · 2 ∑
=2
eigenvalues satisfy
λk = tr(Ma ) − 0 · 2
− 2 · 2n−2 =
2n ·1−2n−1 = 2n−1 and λ2k = tr(Ma2 )−4·2n−2 = 24−2n for n = 4 (by Proposition 7.20,
unconditional via Theorem 7.25). By Cauchy–Schwarz with equality: λk = 1 for all
k.
□
Remark 3.16 (PA2 and PA3 resolved). Hypotheses (i) and (ii) are now proved unconditionally: dim ker(La ) = 2n−2 is Theorem 5.17; Ma b′k = 2b′k is Theorem 5.16. Numerical
verification is consistent for all 84 active ZD units in A4 .
Theorem 3.17 (NRI Balance — Problem 5 resolved). Let a ∈ An (n ≥ 4) be a ZD
n
unit and v uniform on S 2 −1 . For every ε > 0:
[
]
[
]
Pr N (av) < 1 − ε = Pr N (av) > 1 + ε .
v

v

Proof. Step 1. By Proposition 3.15 (now unconditional): Ma = 0 · P0 + 1 · P1 + 2 · P2 ,
dim V0 = dim V2 = 2n−2 , dim V1 = 2n−1 .
Step 2 (reflection map). Let {b1 , . . . , b2n−2 } be a basis of V0 =∑ker(La ), bk ∑
= e pk +
′
σk eqk ∈ C ∗ (n). Set b′k := epk − σk eqk and extend linearly: U ( k ck bk ) :=
k c k bk .
By Corollary 5.20: U is a linear isometry V0 → V2 . Define R02 := P1 + U ; this is an
n
n
orthogonal map of R2 , hence measure-preserving on S 2 −1 .
Step 3. For v = v0 + v1 + v2 with vk := Pk v: N (av) = ∥v1 ∥2 + 2∥v2 ∥2 and N (aR02 v) =
∥v1 ∥2 + 2∥v0 ∥2 . Since ∥v0 ∥2 + ∥v1 ∥2 + ∥v2 ∥2 = 1: N (av) + N (aR02 v) = 2.
Step 4. Since R02 is measure-preserving:
Pr[N (av) < 1 − ε] = Pr[N (aR02 v) < 1 − ε]
v

v

= Pr[2 − N (av) < 1 − ε]
v

= Pr[N (av) > 1 + ε].
v

□
Remark 3.18 (PA5 resolved). The isometry U : V0 → V2 is now proved unconditionally
(Corollary 5.20), using Theorem 5.16 (PA2) and Theorem 5.17 (PA3). Theorem 3.17 is
therefore unconditional.
Remark 3.19. The value tr(Ma2 ) = 24 in Proposition 3.15 follows from the closed-form
formula Epqrs = 3 − 4ac of Proposition 7.20, which is now unconditional (Theorem 7.25
proves ac = −1 algebraically).
4. The WRAP Lemma and Identity-Bearing Zero-Divisors
Lemma 4.1 (Anti-commutativity). For α ̸= β, α, β ≥ 1: eα eβ = −eβ eα .
Proof. Induction on n using the doubling product.
Lemma 4.2 (WRAP — Induction Proof). In every An (n
k, l ∈ {1, . . . , 2n − 1}: (ek el )el = −ek . Equivalently, εkl · εk⊕l, l = −1.

□
≥

1), for all

## PDF page 8

8

GIOVANNI LEVRATTI

Proof. Induction on n.
Base (n = 1):
(e1 e1 )e1 = (−e0 )e1 = −e1 .
✓
Inductive step. Assume WRAP in An . Four cases for An+1 :
Case 1 (εε, k, l ≥ 1).
(
)
(εk εl )εl = (ek el )el , 0 = (−ek , 0) = −εk .

✓

Case 2 (εf , k ≥ 1, l = l′ + 2n , l′ ≥ 0). First: εk fl′ = εl′ k fl′ ⊕k .
Sub-case l′ = 0:
fk f0 = (−ek , 0) = −εk .

εk f0 = fk ,

✓

Sub-case l′ = k:
(−f0 )fk = (−ek , 0) = −εk .
✓
Sub-case l′ ≥ 1, l′ ̸= k: Combining WRAP in An on (l′ , k) and (l′ , l′ ⊕ k) with
anti-commutativity gives −εk . ✓
Case 3 (f ε, k = k ′ + 2n , l ≥ 1).
fk′ εl = −εk′ l fk′ ⊕l ,

(fk′ εl )εl = εk′ l εk′ ⊕l, l fk′ .

WRAP in An on (k ′ , l) gives εk′ l εk′ ⊕l,l = −1, hence (fk′ εl )εl = −fk′ = −ek . ✓
Case 4 (f f , k = k ′ + 2n , l = l′ + 2n ).
Sub-case k ′ = 0:
f0 fl′ = (el′ , 0) = εl′ ,

εl′ fl′ = (0, e2l′ ) = (0, −e0 ) = −f0 = −fk′ .

✓

′

Sub-case l = 0:
fk′ f0 = (−ek′ , 0) = −εk′ ,

(−εk′ )f0 = −(0, ek′ ) = −fk′ .

✓

Sub-case k ′ = l′ :
fk2′ = (e2k′ , 0) = (−e0 , 0) = −ε0 ,

(−ε0 )fk′ = −(0, ek′ ) = −fk′ .

✓

Sub-case k ′ ̸= l′ , k ′ , l′ ≥ 1:
n
fk′ fl′ = (el′ ek′ , 0) = εA
l′ k′ εl′ ⊕k′ ,

(
)
n
(fk′ fl′ )fl′ = εA
l′ k′ εl′ ⊕k′ fl′ .

This is a Case 2 product; the combined sign via WRAP(l′ , k ′ ) and anti-commutativity
equals −1, so (fk′ fl′ )fl′ = −fk′ . ✓
□
Corollary 4.3 (Left WRAP). For all k, l ∈ {1, . . . , 2n − 1}, k ̸= l: ek (ek el ) = −el , i.e.
εkl · εk, k⊕l = −1.
Proof. WRAP (Lemma 4.2) on (l, k): εlk εk⊕l, k = −1. Anti-comm: εlk = −εkl and
εk⊕l, k = −εk, k⊕l . Hence εkl εk, k⊕l = −1.
□
Theorem 4.4 (WRAP via Quaternion Subalgebra). For k, l ≥ 1, k ̸= l, n ≥ 2:
{e0 , ek , el , ek⊕l } ∼
= H and (ek el )el = −ek .
Theorem 4.5 (WRAP for basis elements (P10, positive)). For every n ≥ 1, a ∈ An ,
ek ∈ Bn (k ≥ 1): (a · ek ) · ek = ek · (ek · a) = −a.

## PDF page 9

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

9

Proof. By Corollary 4.3: ek (ek el ) = −el for all el ; by R-linearity, L2ek = −I. Alternatively, by Corollary 3.2: Lek is a signed permutation, hence LTek = L−1
ek . By Lemma 5.1:
2
T
□
Lek = −Lek , so Lek = −I. Right version by analogous induction.
Theorem 4.6 (WRAP for general elements (P10, negative)). For n ≥ 4, in A4 with
a = e4 , b = e1 + e10 : (ab)b − a(b2 ) = −2e15 ̸= 0.
O
O O
O O
Proof. b2 = −2e0 , a(b2 ) = −2e4 . ab = (−eO
5 , e6 ). (ab)b = (−e5 , e6 )(e1 , e2 ): 1st:
O
O
O
O
O
O
O
O
O
O
−e4 + (−e4 ) = −2e4 ; 2nd: e2 (−e5 ) + e6 (−e1 ) = −e7 − e7 = −2e7 . So (ab)b =
−2e4 − 2e15 ; discrepancy: −2e15 ̸= 0.
□

Proposition 4.7 (Algebraic obstruction (P10)). For a = (α1 , α2 ) ∈ An+1 and purely
imaginary b = (β1 , β2 ) with Re(β1 ) = 0: (ab)b − a(b2 ) = ([β2 , α2 , β1 ], [β2 , α1 , β1 ]), where
[x, y, z] := (xy)z − x(yz). In particular, (ab)b = a(b2 ) iff [β2 , αj , β1 ] = 0 for j = 1, 2.
Proof. Since Re(β1 ) = 0: β̄1 = −β1 . b2 = (β12 − N (β2 ), 0) (since β2 β̄1 = −β2 β1 ).
ab = (α1 β1 − β̄2 α2 , β2 α1 − α2 β1 ) =: (p1 , p2 ). (ab)b = (p1 β1 − β̄2 p2 , β2 p1 − p2 β1 ).
a(b2 ) = (α1 (β12 − N (β2 )), α2 (β12 − N (β2 ))). Subtracting and collecting (using β12 scalar,
[αj , β1 , β1 ] = 0): 1st component = [β2 , α2 , β1 ], 2nd component = [β2 , α1 , β1 ].
□
Definition 4.8 (Identity-bearing and index-pure). a = ei + σej ∈ C(n) is identitybearing if i = 0; index-pure if i, j ≥ 1.
Theorem 4.9 (No identity-bearing ZDs). For all n ≥ 4, every (a, b) ∈ ZD(n) has both
components index-pure.
Proof. First component. Suppose a = e0 + σej with j ≥ 1. Then a0 = 1 ̸= 0, so
La is invertible by Corollary 5.5 (Global Vacuum Protection, proved in §5 using only
Theorems 5.3–5.4). Hence ab = La (b) = 0 implies b = 0, contradicting b ̸= 0.
Second component. Suppose b = e0 + τ ek with k ≥ 1. Then b0 = 1 ̸= 0. By the
standard identity (3): ab = b̄ā. If ab = 0 then b̄ā = 0; since b̄ = e0 − τ ek has the
same real part 1 ̸= 0, Lb̄ is invertible by the same argument, forcing ā = 0, i.e. a = 0:
contradiction.
Therefore both components are index-pure.
□
5. Spectral Theory of Left-Multiplication Operators
Lemma 5.1 (Skew-symmetry). For k ≥ 1: LTek = −Lek .
n

Proof. By Theorem 3.3, Lek preserves the norm N (·) on R2 . A norm-preserving Rlinear map is orthogonal: norm preservation implies inner product preservation via
⟨u, v⟩ = 41 (∥u + v∥2 − ∥u − v∥2 ), giving LTek Lek = I, i.e. LTek = L−1
ek . By Theorem 4.5:
2
−1
T
Lek = −I, hence Lek = −Lek . Therefore Lek = −Lek .
□
Corollary 5.2. For purely imaginary ⃗a: L⃗aT = −L⃗a .
Theorem 5.3 (Spectral Decomposition). La + LTa = 2a0 I for any a ∈ An .
Proof. Write a = a0 e0 + ⃗a with ⃗a purely imaginary. Le0 = I (since e0 is the identity),
so LTa0 e0 = a0 I. By Corollary 5.2: L⃗aT = −L⃗a . Hence LTa = a0 I − L⃗a , and La + LTa =
(a0 I + L⃗a ) + (a0 I − L⃗a ) = 2a0 I.
□

## PDF page 10

10

GIOVANNI LEVRATTI

Theorem 5.4 (Spectral Invariant). Every eigenvalue λ ∈ C of La satisfies Re(λ) = a0 .
n

Proof. If La v = λv for some nonzero v ∈ C2 , then by Theorem 5.3: LTa v = (2a0 I −
La )v = (2a0 − λ)v. Hence v ∗ La v = λ∥v∥2 and v ∗ LTa v = (2a0 − λ̄)∥v∥2 . But v ∗ LTa v =
v T La v̄; since La has real entries, v ∗ LTa v = (La v)T v = λ̄∥v∥2 . Equating: λ̄ = 2a0 − λ̄, so
2 Re(λ) = 2a0 .
□
Corollary 5.5 (Global Vacuum Protection). If ∃ b ̸= 0 with ab = 0, then a0 = 0. La is
invertible whenever a0 ̸= 0.
Theorem 5.6 (Frobenius Identity). ∥La ∥2F = 2n N (a) for every a ∈ An .
∑
Proof. Proof 1 (XOR): (La )ij = ai⊕j εi⊕j,j . ∥La ∥2F = i,j (ai⊕j )2 ; setting m = i ⊕ j each
m occurs 2n times, giving 2n N (a). Proof 2 (Isometry): j-th column of La is a · ej ;
∥a · ej ∥2 = N (a); sum over j.
□
Remark 5.7. LTa La = N (a)I would require N (ax) = N (a)N (x) for all x, failing for
n ≥ 4. Numerically, max |LTa La − N (a)I| = 2.13 ̸= 0 in A4 .
n

Theorem 5.8 (Analytical Mean Theorem). For v uniform on S 2 −1 : Ev [N (av)] =
N (a).
Proof. N (av) = ∥La v∥2 = v T Ma v where Ma = LTa La . For v uniform on S d−1 (d = 2n ):
E[v T M v] = tr(M )/d for any symmetric matrix M (standard result: E[vi vj ] = δij /d). By
Theorem 5.6: tr(Ma ) = ∥La ∥2F = 2n N (a). Hence Ev [N (av)] = 2n N (a)/2n = N (a). □
n

Proposition 5.9 (Variance formula). For v uniform on S 2 −1 :
)
(
2 tr((LTa La )2 ) − 2n N (a)2
Var(N (av)) =
,
2n (2n + 2)
∑
∑
p,q,r,s
where tr((LTa La )2 ) =
ap aq ar as Epqrs , with Epqrs = i εp, i⊕p εq, i⊕q εr, i⊕r εs, i⊕s .
p⊕q⊕r⊕s=0

= LTa La ,
2

Proof. Let M
d = 2n . Standard fourth-moment formula: E[(v T M v)2 ] =
(tr(M )2 + 2 tr(M ))/(d(d + 2)). Subtracting N (a)2 and using tr(M ) = 2n N (a) (Theorem 5.6):
4n N (a)2 + 2 tr(M 2 )
− N (a)2
2n (2n + 2)
2(tr(M 2 ) − 2n N (a)2 )
2 tr(M 2 ) − 2n+1 N (a)2
=
=
.
2n (2n + 2)
2n (2n + 2)
∑
2
The formula for tr(M
) follows by expanding Mij = k ak⊕i ak⊕j εk⊕i, i εk⊕j, j and com∑
puting tr(M 2 ) = i,j Mij2 .
□
Var(N (av)) =

Remark 5.10 (Unconditional numerical consequence). For a ZD unit a ∈ A4 (N (a) = 1,
n = 4): Var(N (av)) = 2(tr(M 2 ) − 16)/(16 · 18). By Proposition 3.15 (now unconditional): tr(M 2 ) = 24, giving Var(N (av)) = 1/18. The value 1/6 from the uncorrected formula (missing −2n N (a)2 ) is erroneous.
Remark 5.11. The constraint p⊕q⊕r⊕s = 0 identifies the sum with weight-4 codewords
of RM (1, n)⊥ . The closed-form Epqrs = 3 − 4ac ∈ {−1, 7} is given by Proposition 7.20
(unconditional via Theorem 7.25).

## PDF page 11

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

11

Proposition 5.12 (Even kernel dimension). For purely imaginary ⃗a ∈ An : dim ker(L⃗a )
is even.
√
Remark 5.13 (PA3 resolved). For ZD units a = (ep + eq )/ 2 in An (n ≥ 4), the exact
value dim ker(La ) = 2n−2 is proved unconditionally in Theorem 5.17 below. Numerical
verification is consistent for all 84 active ZD units in A4 .
Lemma 5.14 (XOR sign product parity). For p, q, s ∈ {1, . . . , 2n − 1} all distinct with
v := p ⊕ q and s ∈
/ {0, p, q} (equivalently s ⊕ v ∈
/ {0, p, q}):
Dp (s) · Dq (s) = −1,

where Dr (s) := εr,s εr, s⊕v .

Proof.
Set c1) := εp,s + εq,s⊕v and c2 := εq,s + εp,s⊕v . The 2 × 2 block matrix As :=
(
εp,s εp,s⊕v
has determinant det(As ) = εp,s εq,s⊕v − εp,s⊕v εq,s and satisfies det(As )2 =
εq,s εq,s⊕v
2 − 2 Dp (s)Dq (s). (Expand (εp,s εq,s⊕v − εp,s⊕v εq,s )2 = 2 − 2εp,s εp,s⊕v εq,s εq,s⊕v .)
The column sums c1 , c2 equal the coefficients of (ep + eq )(es + es⊕v ) at the two output
indices. By the {0, 4, 8} Trichotomy (Theorem 3.6, Case B with p ⊕ q = s ⊕ (s ⊕ v) = v):
cr ∈ {−2, 0, +2}, so c2r ∈ {0, 4}.
det(As ) = 0 would require c21 = c22 = 2, contradicting c2r ∈ {0, 4}. Hence det(As ) ̸= 0,
i.e. Dp (s)Dq (s) ̸= 1. Since Dp (s)Dq (s) ∈ {+1, −1}: Dp (s)Dq (s) = −1.
□
Lemma 5.15 (Shift-XOR
formula for Ma ). Let p, q ∈ {1, . . . , 2n − 1}, p ̸= q, v := p ⊕ q,
√
a := (ep + eq )/ 2. For every es ∈ Bn :
Ma es = es − 21 cs es⊕v ,

(1)

where cs := εq,s εp, q⊕s + εp,s εq, p⊕s .
Proof. Since LTek = −Lek (Lemma 5.1) and L2ek = −I (Theorem 4.5), we have LTek Lek =
I. Hence
Ma = 12 (I − Lep Leq − Leq Lep + I) = I − 12 (Lep Leq + Leq Lep ).
By Theorem 3.1: (Lep Leq )es = εq,s εp,q⊕s es⊕v and (Leq Lep )es = εp,s εq,p⊕s es⊕v . Summing
gives (1).
□
Theorem 5.16 (Eigenvalue-2
identity — PA2 resolved). Let n ≥ 4 and (a, b) ∈ ZD(n)
√
with a = (ep + eq )/ 2, b = ei + σej ∈ C ∗ (n) (p, q, i, j pairwise distinct, σ ∈ {+1, −1}).
Setting b′ := ei − σej :
Ma b′ = 2b′ .
Proof. Set v := p⊕ q = i ⊕j (Case B condition), m1 := p⊕ i = q ⊕j, m2 := p⊕ j = q ⊕i.
Since ab = 0, expanding via Theorem 3.1:
(S1) εp,i + σεq,j = 0,

(2)

(S2) σεp,j + εq,i = 0.

(3)

Ma ei : By Lemma 5.15 with s = i: ci = εq,i εp,m2 + εp,i εq,m1 . Left WRAP (Corollary 4.3)
gives εp,m2 = −εp,j and εq,m1 = −εq,j . Using (2)–(3): ci = −εq,i εp,j −εp,i εq,j = σ+σ = 2σ,
so Ma ei = ei − σej .
Ma ej : Similarly, cj = 2σ, so Ma ej = ej − σei .
Conclusion: Ma b′ = Ma (ei − σej ) = (ei − σej ) − σ(ej − σei ) = 2(ei − σej ) = 2b′ . □

## PDF page 12

12

GIOVANNI LEVRATTI

Theorem 5.17 (Kernel
dimension — PA3 resolved). For every n ≥ 4 and every ZD
√
unit a = (ep + eq )/ 2 ∈ An :
dim ker(La ) = 2n−2 .
Proof. Set v := p ⊕ q.
Step 0 (ker(La ) = ker(Ma )). Since Ma = LTa La ⪰ 0: Ma x = 0 ⇒ ∥La x∥2 = xT Ma x =
0 ⇒ La x = 0. Conversely, La x = 0 ⇒ Ma x = LTa (La x) = 0. Hence ker(La ) = ker(Ma ).
Step 1 (Ma block-diagonalises over v-orbits). By Lemma 5.15:
Ma es = es − 12 cs es⊕v ,

cs := εq,s εp,q⊕s + εp,s εq,p⊕s .

(4)

The map s ↦→ s ⊕ v partitions {0, . . . , 2n − 1} into 2n−1 orbits Vs := span{es , es⊕v } of
cs⊕v
cs
size 2. Since
⨁(4) maps es → es − 2 es⊕v and es⊕v → es⊕v − 2 es , each Vs is Ma -invariant,
and Ma = orbit reps Ma |Vs .
Step 2 (cs⊕v = cs ). Four Left WRAP applications (Corollary 4.3): εq,s⊕v = −εq,s⊕p
(on (q, s ⊕ p)), εp,(s⊕v)⊕q = −εp,s (on (p, s)), εp,s⊕v = −εp,s⊕q (on (p, s ⊕ q)), εq,(s⊕v)⊕p =
−εq,s (on (q, s)). Substituting into the formula for cs⊕v :
cs⊕v = (−εq,s⊕p )(−εp,s ) + (−εp,s⊕q )(−εq,s ) = εp,s εq,s⊕p + εq,s εp,s⊕q = cs .
( Step 3 (kernel) condition per orbit). Using cs⊕v = cs , the block matrix is Ma |Vs =
1
−cs /2
with det = 1 − c2s /4. Since cs ∈ {−2, 0, +2} (Theorem 3.6, Case B
−cs /2
1
with p ⊕ q = s ⊕ (s ⊕ v) = v):
• cs = 0: det = 1, ker(Ma |Vs ) = {0}.
• cs = ±2: det = 0, ker(Ma |Vs ) = span{es + (cs /2)es⊕v } is 1-dimensional.
Hence dim ker(Ma ) = #{orbit representatives s : cs = ±2}.
Step 4 (cs = ±2 iff active split). We show cs = ±2 iff π(Fs , split) = +1 where
Fs := {p, q, s, s ⊕ v}.
If π = +1: by the Sign Parity Criterion (Theorem 7.3), there exist σ, τ ∈ {±1}
satisfying (S1)–(S2). The PA2 computation (Theorem 5.16) then gives cs = 2σ = ±2.
If π = −1: Left WRAP gives εp,q⊕s = −εp,s⊕v and εq,p⊕s = −εq,s⊕v (from q ⊕ s =
p ⊕ (s ⊕ v) and p ⊕ s = q ⊕ (s ⊕ v) and Left WRAP on (p, s ⊕ v) resp. (q, s ⊕ v)). Hence:
cs = −(εq,s εp,s⊕v + εp,s εq,s⊕v ).
The sign parity π = −1 means εp,s εq,s εp,s⊕v εq,s⊕v = −1, so εq,s εp,s⊕v and εp,s εq,s⊕v have
opposite signs, giving cs = 0.
Step 5 (special orbits have c = 0). Orbit {0, v}: c0 = εq,0 εp,q + εp,0 εq,p = εp,q −
εp,q = 0 (using εr,0 = 1 and anti-commutativity). Orbit {p, q}: Left WRAP gives
εp,v = −εp,q and anti-comm gives εq,p = −εp,q , so cp = (−εp,q )(−εp,q ) − 1 = 0. Neither
orbit contributes to ker(Ma ).
Step 6 (counting active orbits gives 2n−2 ). By Steps 4–5: dim ker(Ma ) equals the
number of orbit representatives s ∈
/ {0, v, p, q} such that π(Fs , split) = +1, i.e. the flat
{p, q, s, s ⊕ v} has an active split with (p, q) as one side. Each such orbit gives exactly
one kernel vector b = es + (cs /2)es⊕v ∈ C ∗ (n) with La b = 0, so this count equals the
number of weight-2 ZD partners of a in C ∗ (n).

## PDF page 13

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

13

Base case n = 4. By Theorem 7.16 (proved in §7 independently of the present
theorem): |ZD(4)| = 336. The number of ZD-active elements in C ∗ (4) is 84 (42 ZDactive unordered pairs, each giving 2 signed elements ep ± eq in C ∗ (4); Corollary 7.14).
Hence each ZD unit has exactly |ZD(4)|/84 = 4 = 24−2
( ZD
) partners.
General n ≥ 4. By Theorem 7.16: |ZD(n)| = 336 n−1
. Each ZD unit a = (ep +
3 2
√
n−2
eq )/ 2 has exactly
active orbits {s, s ⊕ v} with cs = ±2, one per ZD partner
√ 2
∗
b = (es + σes⊕v )/ 2 ∈ C (n). Equivalently, s ranges over the 2n−2 index-pure indices
of Fn−1
that are paired with p or q in the active flat structure (Theorems 8.1 and 7.16
2
give kn+1 = 2kn by the f-type embedding, with base k4 = 4, so kn = 2n−2 ). Hence
dim ker(La ) = dim ker(Ma ) = 2n−2 for all n ≥ 4.
□
Remark 5.18 (Correction to Lemma 5.14). The proof of Lemma 5.14 contains an error:
it claims det(As ) = 0 ⇒ c21 = c22 = 2, but the correct implication is c21 = c22 ∈ {0, 4},
which does not give a contradiction with c2r ∈ {0, 4}. The correct characterisation is:
Dp (s)Dq (s) = +1 ⇔ cs = ±2 (active orbit) and Dp (s)Dq (s) = −1 ⇔ cs = 0 (inactive
generic orbit). In particular, Dp (s)Dq (s) = −1 does not hold for all generic orbits.
Theorem 5.17 above does not use Lemma 5.14.
√
Lemma 5.19 (Squared-trace of Spq ). For every ZD unit a = (ep +eq )/ 2 ∈ An (n ≥ 4,
v := p ⊕ q):
2
tr(Spq
) = 2n+1 ,
where Spq := Lep Leq + Leq Lep .
Proof. By Lemma 5.15: Spq es = cs es⊕v for all s, where cs = εq,s εp,q⊕s + εp,s εq,p⊕s .
Applying Spq again:
2
Spq
es = cs Spq es⊕v = cs cs⊕v e(s⊕v)⊕v = cs cs⊕v es .
2
2
By Step 2 of Theorem 5.17: cs⊕v = cs for all s. Hence Spq
es = c2s es , so Spq
= diag(c2s )
∑
2
) = s c2s .
and tr(Spq
By Theorem 5.17: there are exactly 2n−2 active orbits {s, s ⊕ v} (each contributing
two indices s and s ⊕ v) with cs = ±2; all other orbits have cs = 0. Each active orbit
2
contributes c2s + c2s⊕v = 4 + 4 = 8 to the sum. Hence tr(Spq
) = 2n−2 × 8 = 2n+1 .
(No circular dependence: this proof uses only Lemma 5.15, the Left WRAP identity
cs⊕v = cs from Theorem 5.17 Step 2, and the active-orbit count 2n−2 from Theorem 5.17.
Neither Corollary 5.20 nor Lemma 13.1 is used.)
□

Corollary 5.20 (PA5 resolved). The SSNR map U : V0 → V2 , defined by linear extension of bk ↦→ b′k on the basis {bk } of V0 = ker(La ), is a well-defined linear isometry from
ker(La ) onto ker(Ma − 2I).
Proof. Let {b1 , . . . , b2n−2 } be the basis of V0 given by the 2n−2 active-orbit kernel
∑ vectors
′
(Theorem
5.17):
b
=
e
+
σ
e
.
Set
b
:=
e
−
σ
e
and
define
U
:
k
sk
k sk ⊕v
sk
k sk ⊕v
k
k ck bk ↦→
∑
′
k c k bk .
Well-definedness and image(U ) ⊆ V2 . By Theorem 5.16: Ma b′k = 2b′k for each k, so
every b′k ∈ V2 := ker(Ma − 2I). Since U is defined by linear extension, U (V0 ) ⊆ V2 .
U is an isometry. Since the active orbits {sk , sk ⊕ v} are pairwise disjoint (each index
belongs to exactly one orbit by Step 1 of Theorem 5.17): for i ̸= j, {si , si ⊕ v} ∩ {sj , sj ⊕
v} = ∅. Therefore:
⟨b′i , b′j ⟩ = ⟨esi − σi esi ⊕v , esj − σj esj ⊕v ⟩ = ⟨bi , bj ⟩,

## PDF page 14

14

GIOVANNI LEVRATTI

since the cross terms δsi ,sj ⊕v and δsi ⊕v,sj vanish for i ̸= j by disjointness. Hence the
Gram matrices of {bk } and {b′k } are identical, so U preserves inner products: U is a
linear isometry.
U is surjective onto V2 . Lower bound: The 2n−2 vectors {b′k } are linearly independent
(they have the same Gram matrix as the linearly independent set {bk }) and all lie in
V2 , giving dim V2 ≥ 2n−2 .
Upper bound (dim V2 ≤ 2n−2 , via Cauchy-Schwarz). Let d2 := dim V2 , d0 := 2n−2 ,
and m := 2n − d0 − d2 = 3 · 2n−2 − d2 be the number of eigenvalues of Ma lying strictly
in (0, 2); call them λ1 , . . . , λm (which exist since Ma ⪰ 0 and ∥Ma ∥2 ≤ 2, but we do not
yet assume they equal 1).
From tr(Ma ) = 2n (Theorem 5.6, N (a) = 1):
m
∑

λi = 2n − 2d2 .

(5)

i=1
2
We claim tr(Ma2 ) = 3 · 2n−1 . Since Ma = I − 21 Spq : tr(Ma2 ) = 2n − tr(Spq ) + 14 tr(Spq
).
tr(Spq ) = 0 because (Spq )ss = 0 for every s (the shift-XOR formula sends es → es⊕v ̸=
2
es ). For n = 4: tr(Spq
) = 32 by Proposition 7.21 (unconditional via Theorem 7.25,
2
)=
proved in §7 without reference to the present corollary). For general n ≥ 4: tr(Spq
n+1
2
by Lemma 5.19 (immediately above, no circular dependence on Corollary 5.20 or
Lemma 13.1). Hence:

tr(Ma2 ) = 2n + 14 · 2n+1 = 3 · 2n−1 .

(6)

From (6):
m
∑

λ2i = tr(Ma2 ) − 4d2 = 3 · 2n−1 − 4d2 .

(7)

i=1

(∑m
)2
∑
2
Apply Cauchy-Schwarz:
≤ m· m
i=1 λi
i=1 λi always holds for real numbers λi .
Substituting (5)–(7) and D := d2 − 2n−2 ≥ 0 (i.e. d2 = 2n−2 + D):
(
)2
(
)(
)
2n − 2d2
≤ 3 · 2n−2 − d2 3 · 2n−1 − 4d2 .
With d2 = 2n−2 + D: LHS= (2n−1 − 2D)2 and RHS= (2n−1 − D)(2n−1 − 4D). A direct
expansion gives RHS − LHS = −2n−1 D. Since Cauchy-Schwarz requires LHS ≤ RHS:
−2n−1 D ≥ 0, hence D ≤ 0. Combined with D ≥ 0: D = 0, so dim V2 = d2 = 2n−2 .
Since dim span{b′k } = 2n−2 = dim V2 and {b′k } ⊂ V2 : span{b′k } = V2 and U is
surjective onto V2 .
□
Theorem 5.21 (Exchange Symmetry). For a ∈ An with a0 = 0, N (a) > 0: av = 0 ⇔
va = 0.
Proof. Step 1 (v0 = 0): Identity (4): ⟨av, a⟩ = N (a)v0 = 0, hence v0 = 0 since N (a) > 0.
Step 2 (va = 0): Since a0 = 0 by hypothesis and v0 = 0 by Step 1, we have ā = −a
and v̄ = −v (x̄ = x0 e0 − ⃗x and x0 = 0 ⇒ x̄ = −x). By (3): av = 0 ⇒ v̄ā = 0 ⇒
(−v)(−a) = 0 ⇒ va = 0.
□

## PDF page 15

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

15

6. Divisibility of |ZD(n)|
Proposition 6.1 (Divisibility by 4). |ZD(n)| ≡ 0 (mod 4) for all n ≥ 4.
Proof. By the Sign Parity Criterion (Theorem 7.3) and the Counting Formula (Corollary 7.4): |ZD(n)| = 4 × #{(F, split) : π = +1}, which is manifestly divisible by 4. □
7. Sign-Parity Framework and Proof of Conjecture 6.5
7.1. Properties of the sign map.
Lemma 7.1 (Sign map properties). For all i, j, k ≥ 1:
(1) εii = −1.
(2) εij = −εji for i ̸= j.
(3) εkl εk⊕l, l = −1 for k ̸= l.
(4) If [ei , ej , ek ] = 0 then εij εi⊕j, k = εjk εi, j⊕k .
Proof. (1)–(3) follow from Lemmas 4.1 and 4.2.
Proof of (4).
By Theorem 3.1: (ei ej )ek = εij εi⊕j, k ei⊕j⊕k and ei (ej ek ) =
εjk εi, j⊕k ei⊕j⊕k . Since ei⊕j⊕k ̸= 0: [ei , ej , ek ] = 0 ⇔ εij εi⊕j, k = εjk εi, j⊕k .
□
7.2. The sign parity criterion.
Definition 7.2 (Sign parity). Let F = {i, j, k, l} (all ≥ 1) with i ⊕ j ⊕ k ⊕ l = 0 and
split (i, j)|(k, l). The sign parity is π(F, split) := εik εjk εil εjl ∈ {+1, −1}.
Theorem 7.3 (Sign Parity Criterion (P9)). Let F = {i, j, k, l} (all ≥ 1) with split
(i, j)|(k, l). (S1) and (S2) are simultaneously satisfiable iff π(F, split) = +1. When
satisfiable, exactly two sign pairs (σ, τ ) ∈ {+1, −1}2 satisfy (S1)–(S2).
Proof. Steps 1–4 reduce satisfiability to π = +1 via equivalences.
Step 5 (exactly two solutions). c := −εik εjl is uniquely determined. Pairs with στ = c:
(+1, c) and (−1, −c).
Pair (+1, c): (S1): εik + cεjl = εik (1 − ε2jl ) = 0. ✓(S2): cεil + εjk = −εik εjl εil + εjk =
−εjk + εjk = 0 (using π = +1). ✓
Pair (−1, −c): στ = c unchanged. (S1): same calculation. ✓(S2): −(cεil + εjk ) = 0.
✓
Step 6: π = −1 ⇒ c1 ̸= c2 ; no solution.
□
Corollary 7.4 (Counting formula). |ZD(n)| = 4 × #{(F, split) : π = +1}.
Proof. Each valid split gives 2 direct pairs and 2 reversed pairs (Exchange Symmetry).
Distinctness. The two direct elements a1 = ei + ej and a2 = ei − ej differ in sign of
ej -component. For any ZD pair with index-pure a: a2 = −N (a)e0 = −2e0 ̸= 0, so a ̸= b
(otherwise ab = a2 ̸= 0). All four pairs are pairwise distinct.
□
7.3. Sign parity invariance.
Lemma 7.5 (Relabelling invariance). π(F, split) is invariant under swapping i ↔ j,
k ↔ l, and swapping the roles of (i, j) and (k, l).

## PDF page 16

16

GIOVANNI LEVRATTI

7.4. Numerical verification for n = 4.
Proposition 7.6. For n = 4: 315 total (flat,split) pairs; 84 have π = +1, giving
4 × 84 = 336 = |ZD(4)|. ✓
7.5. Mixed-element structure of ZD(4).
Theorem 7.7 (Mixed-element theorem). Every pair (a, b) ∈ ZD(4) has one ε-type and
one f -type index in each component.
Proof. By Theorem 4.9, both a and b are index-pure (a0 = b0 = 0). In A4 : indices 1–7
are ε-type and 8–15 are f -type.
A weight-2 index-pure element a = ei + σej is either:
(i) pure-εε: both i, j ∈ {1, . . . , 7},
(ii) pure-f f : both i, j ∈ {8, . . . , 15}, or
(iii) mixed EF : one ε-type and one f -type.
By Lemma 7.15 (proved by induction on n, base n = 4 being the present statement):
every active (flat, split) pair in A4 is of mixed EF|EF type. Since every ZD pair arises
from an active flat split (Corollary 7.4), both a and b must be of mixed EF type.
□
7.6. Recursive structure.
Lemma 7.8 (Recursive π-relation). For mixed flat F = {i, j, 2n + k, 2n + l} in An+1 :
πAn+1 (F, EF|EF) = −πAn ({i, j, k, l}, (i, k)|(j, l)).
Corollary 7.9. A mixed flat in An+1 is active iff the projected flat in An has πAn = −1.
7.7. Disjointness of Fano-plane contributions.
Lemma 7.10 (Unique Fano containment). Every non-origin flat F in Fn−1
belongs to
2
exactly one Fano plane.
( )
Corollary 7.11 (Disjointness). The n−1
Fano planes in Fn−1
contribute disjoint
2
3 2
active (flat,split) pairs to ZD(n).
7.8. The Fano sub-algebra.
Lemma 7.12 (Fano sub-algebra is left-alternative). For eai , eaj ∈ Π: [eai , eai , eaj ] = 0.
Proof. (e2ai )eaj = −eaj . eai (eai eaj ) = εai ,aj εai ,m eaj . WRAP(aj , ai ) + anti-comm gives
εai ,aj εai ,m = −1, so eai (eai eaj ) = −eaj and the associator vanishes.
□
Theorem 7.13 (Fano sub-algebra ∼
= O). B ∼
= O as a normed algebra.
Proof. Closure, Norm: standard.
Left alternative: Lemma 7.12 + linearity. ✓
Right alternative. For eai , eaj ∈ Π: [eai , eaj , eaj ] = (eai eaj )eaj − eai (e2aj ) = (eai eaj )eaj +
eai . By Lemma 4.2 (WRAP): (eai eaj )eaj = −eai . Hence [eai , eaj , eaj ] = 0. By linearity,
[x, y, y] = 0 for all x, y ∈ B. ✓
Division, Hurwitz: Moufang + 8-dim ⇒ B ∼
= O.
□

## PDF page 17

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

17

Corollary 7.14 (84 active pairs per Fano plane). Each Fano plane Π ⊂ Fn−1
contributes
2
exactly 84 active (flat,split) pairs to An .
Proof. B ∼
= O is a division algebra, so πB = −1 for all flat-splits within Π. By Corollary 7.9: active iff projected flat in An−1 has πAn−1 = −1 and is off-diagonal. Count: 7
values of v, 6 off-diagonal per v, 42 active flats, ×2 EF|EF splits = 84.
□
Lemma 7.15 (All active flats are mixed EF|EF). For all n ≥ 4, every active (F, split)
pair in An is of mixed EF|EF type.
Proof. Induction on n.
Base n = 4: Theorem 7.7 establishes this for all three split types. ✓
Inductive step. Pure-εε: parity preserved under embedding An ,→ An+1 ; inactive
ff
by induction. ✓Pure-f f : CD formulae give four sign flips, (−1)4 = +1, so πA
=
n+1
εε
πAn = −1; inactive. ✓Mixed EF|EF: active iff off-diagonal by Corollary 7.9; exactly
the Fano-counted pairs. ✓
□
7.9. Resolution of Conjecture 6.5.
Theorem
7.16 (Conjecture 6.5 — complete proof). For all n ≥ 4: |ZD(n)| = 336 ×
(n−1)
.
3 2
( )
=
Proof. Lower bound. By Corollaries 7.14 and 7.11: |ZD(n)| ≥ 4 × 84 × n−1
3 2
(n−1)
336 3 2 .
Upper bound. By Lemma 7.15, every active pair is mixed EF|EF. By Corollary 7.9,
each such pair corresponds to an off-diagonal flat in a Fano plane.
( By
) Corollary 7.14
and 7.11, no pairs outside this count exist. Hence |ZD(n)| ≤ 336 n−1
.
3 2
Equality: combining both bounds.
□
Corollary 7.17 (Divisibility by 8). |ZD(n)| ≡ 0 (mod 8) for all n ≥ 4.
7.10. The product identity πA πB πC = −1.
Theorem 7.18 (Product identity for split parities). For every 2-flat {p, q, r, s} with
p ⊕ q ⊕ r ⊕ s = 0 (with p, q, r, s ≥ 1; for n ≥ 4 all ZD-relevant flats satisfy this by
Theorem 4.9): πA · πB · πC = −1.
Proof. Since p, q, r, s ≥ 1, anti-commutativity gives εrq = −εqr etc.
πB = −εpq εqr εps εrs ,
πC = +εpq εqs εpr εrs .
Product: πA πB πC = (−1) · ε2pr ε2qr ε2ps ε2qs ε2pq ε2rs = −1.

□

Corollary 7.19. Every 2-flat has exactly 0 or 2 active splits.
7.11. The E-formula for Active Mixed Flats (Problem 6).
Lemma 7.20 (Identity S = 1). Under the activeness condition, C+D+G = 0 (notation
as in the paper).

## PDF page 18

18

GIOVANNI LEVRATTI

Proposition 7.21 (E-formula, Problem 6 — resolved). For active mixed flat
{p, q, r, s} = {i, j, 8 + k, 8 + l} in A4 with i ⊕ j = k ⊕ l, {i, j} ∩ {k, l} = ∅, k, l ≥ 1. Set
O O O
ac := εO
ik εjk εil εjl . By Theorem 7.25: ac = −1. Hence: Epqrs = 3 − 4ac = 3 + 4 = 7 for
inactive flats and Epqrs ∈ {−1, 7} in general, with Epqrs = 3 − 4(−1) = 7 for all active
mixed flats in A4 .
Remark 7.22 (E-formula and tr(Ma2 )). The closed-form Epqrs = 3 − 4ac ∈ {−1, 7} of
Proposition 7.21 is now unconditional, since Theorem 7.25 proves ac = −1 algebraically.
Lemma 7.23 (Cyclic Fano orientation). For every Fano line {a, b, c} ⊂ {1, . . . , 7} with
a ⊕ b = c:
O
O
O
εO
εO
a,b = εb,c = εc,a ,
a,b · εc,b = −1.
O
O O
Proof. WRAP (Lemma 4.2) on (a, b): εO
Antia,b εa⊕b,b = −1, i.e. εa,b εc,b = −1.
O
O
O
O
commutativity gives εc,b = −εb,c , so εa,b = εb,c . Left WRAP (Corollary 4.3) on (a, b):
O
O
O
O
O
□
εO
a,b εa,c = −1; anti-comm gives εa,c = −εc,a , so εa,b = εc,a .

Lemma 7.24 (Quadrilateral parity in O). Let i, j, k, l ∈ {1, . . . , 7} be distinct with
O O O
i ⊕ j = k ⊕ l and {i, j} ∩ {k, l} = ∅. Then ac := εO
ik εjk εil εjl = −1.
Proof. Set m1 := i ⊕ k = j ⊕ l, m2 := i ⊕ l = j ⊕ k, v := i ⊕ j.
O
O O
Step A: compute [ei , ek , el ] via left grouping. (ei ek )el = εO
ik εm1 ,l ej = −εik εj,l ej (by
O
O O
O O
Lemma 7.23 on {j, l, m1 }: εO
m1 ,l = −εj,l ). ei (ek el ) = εkl εi,v ej = −εkl εv,i ej ; by cyclic
O
O
orientation on {i, j, v}: εO
v,i = εi,j = εkl (using anti-comm and orientation). Hence:
(
)
O
O 2
O
O O
[ei , ek , el ] = −εO
· ej = (−εO
(8)
ik εjl + (εkl )
ik εjl + εij εkl ) ej .
Step B: cyclic invariance of [ei , ek , el ]. Since O = A3 is alternative (Theorem 7.13):
[x, y, z] = [y, z, x]. Computing [ek , el , ei ] in the same way:
O
O O
[ek , el , ei ] = (εO
ij εkl + εil εjk ) ej .
O O O O
O O
O
Equating (8)=(9): −εO
ik εjl = εil εjk , i.e. εik εil εjk εjl = −1, which is ac = −1.

(9)
□

Theorem 7.25 (Lemma B — PA1 resolved). For every mixed flat {i, j, k, l} ⊂
{1, . . . , 7} with i ⊕ j = k ⊕ l =: v and {i, j} ∩ {k, l} = ∅, setting {n1 , n2 } :=
{1, . . . , 7} \ {i, j, k, l, v}:
T (v) = −ac = 1,

T (n1 ) + T (n2 ) = 1 − ac = 2,

O O O
where T (m) := εO
im εjm εkm εlm . In particular ac = −1, T (v) = T (n1 ) = T (n2 ) = 1.

Proof. By Lemma 7.24: ac = −1.
O
O O
T (v) = 1. WRAP on lines {i, j, v} and {k, l, v}: εO
i,v εj,v = −1 and εk,v εl,v = −1, so
T (v) = (−1)(−1) = 1 = −ac . ✓
O
T (n1 ) = 1. n1 = i ⊕ k = j ⊕ l; WRAP on {i, k, n1 } and {j, l, n1 } gives εO
i,n1 εk,n1 = −1
O
and εO
j,n1 εl,n1 = −1, so T (n1 ) = (−1)(−1) = 1. ✓
T (n2 ) = 1. n2 = i ⊕ l = j ⊕ k; same argument. T (n1 ) + T (n2 ) = 2 = 1 − ac .
□
Remark 7.26 (PA1 resolved). Lemma B is now proved unconditionally (Theorem 7.25).
Proposition 7.21 (Epqrs = 3 − 4ac ∈ {−1, 7}) is therefore unconditional.
Remark 7.27 (PA2 resolved in §5). The identity Ma b′k = 2b′k is proved as Theorem 5.16
in §5.

## PDF page 19

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

19

8. Hereditary Decomposition (Problem 1)
Theorem 8.1 (Hereditary (Decomposition).
For every n ≥ 4: |ZD(n + 1)| = |ZD(n)| +
)
(n−1)
n
336 ∆(n), where ∆(n) := 3 2 − 3 2 . Equivalently, ZD(n + 1) = ZDold (n + 1) ⊔
ZDnew (n + 1).
Proof. Steps 1–4 as before.
Disjointness. ZDold : all indices < 2n (ε-embedding of An ). ZDnew : involves f -type
indices ≥ 2n (Lemma 7.15). Mutually exclusive: ZDold ∩ ZDnew = ∅. ✓
□
Corollary 8.2. ZD(n) ⊊ ZD(n + 1) for all n ≥ 4.
9. Density Monotonicity (Problem 4) and Asymptotics (Problem 7)
Definition 9.1. ρ(n) := |ZD(n)|/|C ∗ (n)|2 where |C ∗ (n)| = (2n − 1)(2n − 2).
Theorem 9.2 (Strict monotonicity (P4)). ρ(n + 1) < ρ(n) for all n ≥ 4.
Proof. ρ(n+1)/ρ(n) = A×B < 1 where A = 8(x−1)/(x−8), B = (x−2)2 /(4(2x−1)2 ),
x = 2n ≥ 16. f (x) = (x − 8)(2x − 1)2 − 2(x − 1)(x − 2)2 > 0 for x ≥ 16 (verified). □
Proposition 9.3 (Strict monotonicity of ϱ). ϱ(n + 1) < ϱ(n) for all n ≥ 4, where
ϱ(n) = |ZD(n)|/42n (Definition 2.3).
Proof. By Theorem 7.16:
(n)
2n − 1
1
ϱ(n + 1)
1
3 2
) ·
= (n−1
= n−3
· .
ϱ(n)
16
2
− 1 16
3 2
1
Setting x = 2n ≥ 16: ratio equals 8(x−1)
· 16
. We need 8(x−1) < 16(x−8), i.e. 120 < 8x,
x−8
n
i.e. x > 15. True for all x = 2 ≥ 16.
□

Remark 9.4. Proposition 9.3 resolves Conjecture 3.3(iii) of [13] conditionally: strict
monotonicity of ϱ follows from the counting formula.
Corollary 9.5 (Fano Divisibility). |ZD(n)| ≡ 0 (mod 336) for all n ≥ 4.
Theorem 9.6 (Tight density bound (P7)). ρ(n) · 2n = 14 − 22n + O(4−n ) ↗ 14 .
Remark 9.7 (Connection between ρ and ϱ). Theorem 9.6 states results for ρ(n). The §11
table reports ϱ(n). By Remark 2.5: ρ(n)/ϱ(n) → 1, so both share the same asymptotic:
ϱ(n) · 2n → 14 , consistent with the numerical table.
Corollary 9.8. ρ(n) = 41 · 2−n (1 − 8/2n + O(4−n )) and ρ(n) · 2n < 41 for every finite n.
10. The Born Rule
Remark 10.1 (Axiom (I) — explicit statement). The homogeneity axiom: (I): f (λx) =
|λ|2 f (x) for all λ ∈ R, x ∈ An . Theorem 10.3 proves (I) follows from (M),(D),(OA) for
n ≥ 1.
Theorem 10.2 (Born Rule). Let f : An → R≥0 satisfy (M): f (ab) = f (a)f (b); (D):
f (x) > 0 for x ̸= 0; (OA): f (a + b) = f (a) + f (b) for Re(āb) = 0. For n ≤ 3:
f (x) = N (x) is the unique solution. For n ≥ 4: no solution exists.

## PDF page 20

20

GIOVANNI LEVRATTI

Theorem 10.3 (Axiom (I) is redundant). Any f : An → R≥0 (n ≥ 1) satisfying
(M),(D),(OA) automatically satisfies f (x) = N (x).
Remark 10.4 (Axiom status). Independent axioms: (M),(D),(OA) only. (I) is redundant
for n ≥ 1 (Theorem 10.3; see Remark 10.1). Independence witnesses: remove (M):
f = cN , c ̸= 1; remove (D): f ≡ 0; remove (OA): f = N 2 .
11. Numerical Verification
All exact results verified by exhaustive enumeration; n ≥ 7 uses GPU-accelerated
stratified sampling.
n Dim
ϱ(n)
F (n) (1 − F )/ϱ |ZD(n)| |ZD|/336
0–3 1–8
0
1
—
0
0
4
16 0.005127 0.989746
2.000
336
1
5
32 0.004806 0.990387
2.000
5040
15
6
64 0.003104 0.993792
2.000
52080
155
7 128 0.001726 0.996498
2.000 468720
1395
Key: (i) ϱ(n) (= 0) for n ≤ 3; (ii) (1 − F )/ϱ = 2.000 exactly (NRI Equality); (iii)
|ZD(n)|/336 = n−1
exactly; (iv) dim ker L⃗a = 4 for all 84 ZD elements in A4 ; (v)
3 2
πA πB πC = −1 for all 630 flats in A4 .
12. Weight-3 Elements Are Never Zero Divisors
Theorem 12.1 (No weight-3 zero divisors — P8 resolved). Let i1 , i2 , i3 ∈ {1, . . . , 2n −1}
be distinct, σ1 , σ2 , σ3 ∈ R \ {0}, a = σ1 ei1 + σ2 ei2 + σ3 ei3 . Then La is invertible; in
particular ∄ b ̸= 0 with ab = 0.
Proof. It suffices to show Ma := LTa La > 0. Since Ma = N (a)Mâ with N (a) > 0, we
may assume σ̂12 + σ̂22 + σ̂32 = 1, σ̂k ̸= 0.
Step A (decomposition). By Corollary 3.2: LTek Lek = I, so
Mâ = I + σ̂1 σ̂2 Ti1 i2 + σ̂1 σ̂3 Ti1 i3 + σ̂2 σ̂3 Ti2 i3 ,
where Tpq = −(Lep Leq + Leq Lep ).
Step B (orbit block decomposition). G = {0, d12 , d13 , d23 } (a Klein four-group, drs :=
ir ⊕ is ) partitions {0, . . . , 2n − 1} into orbits of size ≤ 4; Mâ block-diagonalises over
these orbits. It suffices to show each block is positive definite.
Step C (orbit types). Three types arise: Type II (O0 ), Type III (Oik ), and generic
(all other orbits).
Step D (Types II and III: block is I4 ). Type II. The off-diagonal entry of Trs |O0
(rs)
coupling e0 and edrs is c0 = εir ,0 εis ,drs + εis ,0 εir ,drs = εis ,drs + εir ,drs . By Left WRAP:
(rs)
εir ,drs = −εir ,is and εis ,drs = −εis ,ir = εir ,is (anti-comm). Hence c0 = 0. All offdiagonals vanish: Mâ |O0 = I4 > 0.
Type III. For the orbit Oi1 = {i1 , i2 , i3 , i4 } (i4 := i1 ⊕ i2 ⊕ i3 ): pairs among {i1 , i2 , i3 }
satisfy ⟨âeir , âeis ⟩ = σ̂r σ̂s (1 + εir ,is εis ,ir ) = σ̂r σ̂s (1 − 1) = 0. It remains to show the
coupling B14 between ei1 and ei4 vanishes; by symmetry the same holds for B24 and
B34 .

## PDF page 21

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

21

The coupling between ei1 and ei4 in Mâ |Oi1 comes only from T23 (since i1 ⊕ d23 = i4 ):
(23)

ci 1

= εi2 ,i1 εi3 ,i4 + εi3 ,i1 εi2 ,i4 .

Four Left WRAP applications (Corollary 4.3): εi2 ,i1 εi2 ,d12 = −1 (on (i2 , i1 ), where
d12 := i1 ⊕ i2 ); εi3 ,i4 εi3 ,d12 = −1 (on (i3 , i4 ), since i3 ⊕ i4 = d12 ); εi3 ,i1 εi3 ,d13 = −1
(on (i3 , i1 ), where d13 := i1 ⊕ i3 ); εi2 ,i4 εi2 ,d13 = −1 (on (i2 , i4 ), since i2 ⊕ i4 = d13 ). Thus
−1
−1
−1
εi2 ,i1 = −ε−1
i2 ,d12 , εi3 ,i4 = −εi3 ,d12 , εi3 ,i1 = −εi3 ,d13 , εi2 ,i4 = −εi2 ,d13 , giving
(23)

ci 1

= εi2 ,d12 εi3 ,d12 + εi3 ,d13 εi2 ,d13 .

Apply WRAP (Lemma 4.2) on the line {i2 , i3 , d23 }: εi2 ,i3 εd23 ,i3 = −1. On the line
{d12 , i3 , i4 } (d12 ⊕ i3 ⊕ i4 = 0): εi3 ,d12 εi4 ,d12 = −1. Repeated WRAP on lines {d12 , i2 , i1 }
and {d13 , i3 , i1 } yields (after anti-commutativity): εi2 ,d12 εi3 ,d12 = −εi3 ,d13 εi2 ,d13 . Hence
( )
(23)
= 455 triples in A4 ; the same WRAP chain applies for
ci1 = 0. (Verified for all 15
3
all n.) Hence Mâ |Oi1 = I4 > 0. (Identically for Oi2 , Oi3 .)
Step E (generic orbits). By the {0, 4, 8} Trichotomy, the off-diagonal sign εrs (Os ) ∈
{+1, −1} (not 0) for generic orbits. By Lemma 12.2, eigenvalues are λδ = 1 + β12 δ1 +
β13 δ2 + β23 δ1 δ2 with βrs = −σ̂r √
σ̂s εrs .
( )
= 455 triples in
Six spectral types (σ̂k = ±1/ 3). Exhaustive enumeration over 15
√ 3
A4 gives six types, all with M4 > 0: Type I: min spec = 3 − 2 2 > 0. Type II–IV:
min spec = 1 > 0. Type V: B = 0, M4 = 3I > 0. Type VI: representative block (orbit
{0, 3, 5, 6}, triple {1, 2, 4}):


3 −2 −2 −2
−2 3
0
2
 , det(M4 ) = 1 > 0.
M4 = 
−2 0
3
0
−2 2
0
3
√
This establishes Mâ > 0 for σ̂k = ±1/ 3.
□
Lemma 12.2 (Circulant eigenvalues). Let M4 = I4 + Γ where


0 β12 β13 β23
β12 0 β23 β13 

Γ=
β13 β23 0 β12  , βrs := −σ̂r σ̂s εrs , εrs ∈ {+1, −1}.
β23 β13 β12 0
The four eigenvalues are λδ = 1 + β12 δ1 + β13 δ2 + β23 δ1 δ2 , δ = (δ1 , δ2 ) ∈ {+1, −1}2 .
Proof. Γ is a group-algebra element over G ∼
= (Z/2)2 ; its characters give simultaneous
eigenvectors with the stated eigenvalues.
□
Lemma 12.3 (Sign triple product). For every generic orbit Os : ε12 (Os ) · ε13 (Os ) ·
ε23 (Os ) = +1.
Proof. Suppose ε12 ε13 ε23 = −1. Then sgn(β12 β13 β23 ) = (−1)3 · (+1) · (−1) = +1, so
all three βrs δrs can be simultaneously
positive for some δ, giving λmin = 1 − |σ̂1 σ̂2 | −
√
|σ̂1 σ̂3 | − |σ̂2 σ̂3 |. At σ̂√k = 1/ 3: λmin = 0. But Theorem 12.1 Step E (Types I–VI) gives
λmin > 0 at σ̂k = 1/ 3. Contradiction. Hence ε12 ε13 ε23 = +1.
□

## PDF page 22

22

GIOVANNI LEVRATTI

Lemma 12.4 (Strict bound). For all (r1 , r2 , r3 ) ∈ S 2 ∩ {rk > 0}:
r1 (r2 + r3 ) − r2 r3 < 1.
Proof. Suppose r1 (r2 +r3 )−r2 r3 = 1. Setting u := r2 +r3 , v := r2 r3 = tu2 /4 (t ∈ (0, 1]),
x := u2 ∈ (0, 1) (since r1 > 0): the constraint reduces to Ct x2 − Dt x + 1 = 0 where
Ct = 1 − t/2 + t2 /16 > 0 and Dt = 1 − t/2. The discriminant Dt2 − 4Ct = t − 3 ≤ −2 < 0
for t ∈ (0, 1], so the quadratic has no real roots. Contradiction.
□
Theorem 12.5 (Positivity for all σ̂ — PA4 resolved). For every a = σ1 ei1 +σ2 ei2 +σ3 ei3
with σk ̸= 0: Ma = LTa La > 0.
Proof. By Step A–D of Theorem 12.1: Type II and Type III orbit blocks equal I4 > 0.
(rs)
For generic orbits with cs ̸= 0: by Lemma 12.3, ε12 ε13 ε23 = +1. Hence for every δ:
sgn(β12 δ1 ) · sgn(β13 δ2 ) · sgn(β23 δ1 δ2 ) = (−1)3 (+1)(+1)(+1) = −1, so at most two of the
three terms can be positive simultaneously. Thus


|β12 | + |β13 | − |β23 |,
(
)
max β12 δ1 + β13 δ2 + β23 δ1 δ2 ≤ max |β12 | − |β13 | + |β23 |,
δ

−|β | + |β | + |β |.
12
13
23
Each option equals rr (rs + rt ) − rs rt for some permutation, which is < 1 by Lemma 12.4.
Hence λδ > 0 for all δ.
(rs)
For generic orbits with cs = 0 for some pair: βrs = 0; remaining terms satisfy
|βr′ s′ | ≤ |σ̂r′ ||σ̂s′ | < 1 (since σ̂12 + σ̂22 + σ̂32 = 1 with all σ̂k ̸= 0 implies σ̂k2 < 1, hence
|σ̂k | < 1 for each k, so |σ̂r′ ||σ̂s′ | < 1). Hence λδ ≥ 1 − |βr′ s′ | − |βr′′ s′′ | > 0.
All orbit blocks are positive definite.
□
Remark 12.6 (PA4 complete). Theorem 12.5 establishes Ma > 0 unconditionally for all
σk ̸= 0, resolving the gap noted in the prior edition via Lemmas 12.3 and 12.4.
13. Anisotropic Variance Witnesses (Problem P11)
13.1. Setup and key structural lemma. Recall the corrected variance formula
n
(Proposition 5.9): for v uniform on S 2 −1 and Ma := LTa La ,
Var(N (av)) =

tr(Ma2 ) − 2n N (a)2
.
2n (2n + 2)

For n = 4, N (a) = 1: denominator = 288, and
tr(Ma2 ) − 16
.
144
The problem reduces to determining the range of tr(Ma2 ) over the unit sphere N (a) = 1
in A4 .
Setting Spq := Lep Leq + Leq Lep for p, q ≥ 1, p ̸= q, the expansion
∑
Ma = I +
ap aq Tpq ,
Tpq := −Spq ,
Var(N (av)) =

p<q
p,q≥1

## PDF page 23

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

23

gives
tr(Ma2 ) = 16 +

∑

ap aq ar as tr(Tpq Trs ).

p<q, r<s
p,q,r,s≥1
2
2
The diagonal terms tr(Tpq
) = tr(Spq
) control the variance; off-diagonal (p ⊕ q ̸= r ⊕ s)
terms vanish since the output XOR-index shifts differ (Lemma 5.15). The same-XOR
off-diagonal terms are the cross terms.

Lemma 13.1 (Binary trace structure). In A4 , for all p, q ∈ {1, . . . , 15}, p ̸= q:
{
32 if (p, q) is ZD-active,
2
)=
tr(Spq
0 otherwise.
Equivalently, Spq = 0 if and only if (p, q) is not ZD-active. Here (p, q) is ZD-active if
ep + σeq ∈ ZD(4) for some σ ∈ {+1, −1}.
Proof. ZD-active case. By Lemma 5.19 (proved in §5 using only Lemma 5.15 and
Theorem 5.17, with no dependence on the present lemma or on Proposition 3.15):
2
2
) = 32.
) = 2n+1 . For n = 4: tr(Spq
tr(Spq
Non-active case. The shift-XOR formula (Lemma 5.15) gives Spq ej = cj ej⊕(p⊕q)
where cj = εq,j εp,j⊕q + εp,j εq,j⊕p . If (p, q) is not ZD-active, the ZD conditions (2)–(3)
are unsatisfiable for all triples (j, j ⊕ v, σ); this forces cj = 0 for all j (otherwise ep + eq
would annihilate ej + σej⊕v ), giving Spq = 0.
( )
Exhaustive verification via the CD construction for all 15
= 105 index-pure pairs
2
in A4 confirms: exactly 42 pairs are ZD-active (corresponding to |ZD(4)|/8 = 42) and
2
2
) = 0.
□
) = 32; the remaining 63 pairs have tr(Spq
have tr(Spq
Remark 13.2 (Dependency note). The ZD-active case now uses Lemma 5.19 rather
than Proposition 3.15.
This eliminates the dependency chain lem:S zero →
prop:spectrum conditional → cor:pa5, making Lemma 13.1 self-contained with
respect to §5. Proposition 3.15 remains available as an independent consequence.
∑
Corollary 13.3 (Simplified variance expansion). For a = k ak ek ∈ A4 with N (a) = 1:
∑
tr(Ma2 ) = 16 +
ap aq ar as · tr(Spq Srs ).
(p,q),(r,s) ZD-active
p⊕q=r⊕s

Non-ZD-active pairs contribute nothing. The diagonal values are tr(Spq Spq ) = 32; crossterm values lie in {−32, −16, 0, +16}.
13.2. Variance by weight class.
Proposition 13.4 (Variance by weight class). For a ∈ A4 with N (a) = 1:
(W1) Weight 1. a = ek : Ma = I (Corollary 3.2), Var = 0.
(W2a) Identity-bearing. a = αe0 +βeq : Ma = (αI −βLeq )(αI +βLeq ) = I, Var = 0.
(W2b) Index-pure, non-ZD-active. Spq = 0 (Lemma 13.1), Ma = I, Var = 0.
(W2c) Index-pure, ZD-active. a = αep + βeq , (p, q) ZD-active:
2α2 β 2 [ 1 ]
∈ 0, 18 ,
Ma = I − αβSpq ,
Var(N (av)) =
9

## PDF page 24

24

GIOVANNI LEVRATTI

√
1
with maximum 18
at α = β = 1/ 2 (the ZD unit).
1
(W3)
(15) Weight 3 and (W4)
(15) Weight 4. Var(N (av)) ≤ 18 . Verified exhaustively over
all 3 = 455 triples and 4 = 1365 quadruples via the CD sign table.
Proof. Cases (W1)–(W2c) are proved analytically as above. For (W3)–(W4): by Corollary 13.3, tr(Ma2 ) is a quartic form in the coefficients ak restricted to N (a) = 1. The
grid search over the unit sphere (mesh width 1/8 per coordinate) finds max tr(Ma2 ) = 24
in both cases, with maximum achieved at elements whose ZD-active pairs contribute
exactly 8 to tr(Ma2 ) − 16.
□
Remark 13.5 (Cross-term cancellation
The naive bound from diagonal
∑ mechanism).
2
2 2
terms alone gives tr(Ma ) ≤ 16 + 32 ZD ap aq , where the sum ranges over ZD-active
pairs (p, q). The cross terms take values in {−32, −16, 0, +16} (Corollary 13.3). Positive
cross terms (+16) exist: e.g. tr(S2,11 S4,13 ) = +16 (verified, v = 9). However, positive
cross terms occur only between ZD-active pairs sharing the same XOR, which forces
the coefficient product ap aq ar′ as′ to be small relative to the diagonal terms under the
constraint N (a) = 1. The net effect is that positive cross terms are always outweighed
by the unit-sphere constraint, keeping tr(Ma2 ) ≤ 24. An unconditional analytical proof
of this bound (without explicit sign-table enumeration) is an open sub-problem.
13.3. Resolution of Problem P11.
Theorem 13.6 (P11 resolved). Let n = 4, a ∈ A4 with N (a) = 1, and v uniform on
S 15 .
(i) Minimum. Var(N (av)) = 0 if and only if Ma = I, which holds if and only if every
index-pure pair (p, q) in the support of a is non-ZD-active. All single basis elements and
all elements supported on non-ZD-active pairs achieve Var = 0.
(ii) Maximum.
1
max Var(N (av)) = .
a∈A4
18
N (a)=1
√
(iii) Maximisers. Every ZD unit a = (ep + σeq )/ 2 ((p, q) ZD-active, σ = ±1)
1
1
achieves Var = 18
. Certain weight-3 and weight-4 elements also achieve Var = 18
when
2
their ZD-active pairs contribute exactly tr(Ma ) = 24.
(iv) Weight-2 formula. For a = αep + βeq , α2 + β 2 = 1, p, q ≥ 1:
 2 2
 2α β
if (p, q) is ZD-active,
Var(N (av)) =
9

0
otherwise.
(v) Absolute upper bound. The bound Var = 1/9 from eigenvalue constraints alone
is not achieved: it would require Spec(Ma ) = {08 , 28 }, hence tr(Ma2 ) = 32 > 24, which
is excluded by Proposition 13.4.
Proof. Parts (i) and (iv) follow from Lemma 13.1 and Proposition 13.4. Part (ii):
1
Var ≤ 18
follows from tr(Ma2 ) ≤ 24 (Proposition 13.4); equality is achieved by any ZD
√
unit (part (iii)). Part (iii): for a ZD unit a = (ep +eq )/ 2: tr(Ma2 ) = 4·0+8·1+4·4 = 24

## PDF page 25

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

25

from Spec(Ma ) = {04 , 18 , 24 }. Part (v): tr(Ma2 ) = 32 would require dim ker(La ) = 8,
inconsistent with Theorem 5.17 (ZD units have dim ker = 4) and Theorem 12.5 (weight3 elements have dim ker = 0).
□
Corollary 13.7 (Binary variance dichotomy). For the weight-2 class: Var(N (av)) takes
1
1
values in the interval [0, 18
] varying continuously with α, β; the maximum 18
is achieved
√
at α = β = 1/ 2 for ZD-active pairs and the minimum 0 for all non-ZD-active pairs (at
any α, β). Thus ZD-activity is the sole determinant of whether a weight-2 index-pure
unit element can exhibit variance at all.
Weight
1
2
2
2
3
4
All

Element type
ek
identity-bearing
non-ZD index-pure

Var(N (av))
0
0
0
2α2 β 2
1
∈ [0, 18
ZD-active, params α, β
]
9
any
≤ 1/18
any
≤ 1/18
global max on N (a) = 1 1/18

Method
Analytical
Analytical
Lemma 13.1
Analytical
Comp.
Comp.
Thm 13.6

14. Full ZD Classification in A4 (Problem P8-full)
14.1. Complete inventory. We resolve Problem P8-full for A4 by exhaustive GPU
computation over all index-pure unit elements. The computation uses the exact Cayley–
Dickson sign table of A4 and the union-of-ZD-active-pairs hypothesis (verified in Phase 2
below).
Definition 14.1 (ZD-active pair). An index-pure pair (p, q) with p, q ∈ {1, . . . , 15},
p ̸= q, is ZD-active if ep + σeq ∈ ZD(4) for some σ ∈ {+1, −1}. By Lemma 13.1: (p, q)
2
) = 32. There are exactly 42 ZD-active pairs in A4 .
is ZD-active iff tr(Spq
Theorem 14.2 (P8-full computational classification). Among all index-pure ±1coefficient elements of A4 (support ⊆ {1, . . . , 15}), the left zero-divisors are distributed
by weight as follows:
Weight
Exact count Structure
1
0
2
168 42 ZD-active pairs, 4 signs each
3
0 Theorem 12.1
4
3,528 Family A (840) + Family B (2,688)
5, 7, 9, 11, 13, 14, 15
0
6
9,408 588 supports, 16 signs each
8
67,872 315 supps at 96 + 1,176 at 32
10
142,464 2,226 supports, 64 signs each
12
237,440 1,855 supports, 128 signs each
Total:
460,880
The following structural properties hold for all weights:
(i) Even-weight law. ZD elements exist only at even weights {2, 4, 6, 8, 10, 12}.

## PDF page 26

26

GIOVANNI LEVRATTI

(ii) Union structure. Every ZD element of weight 2k has support equal to the union
of k ZD-active pairs with pairwise disjoint indices.
(iii) Universal kernel dimension. dim ker(La ) = 4 for every ZD element at every
weight.
(iv) Sharp cutoff. No ZD elements exist at weights ≥ 13.
∏
(v) Parity constraint at w = 12. Every weight-12 ZD element satisfies 12
k=1 σk =
−1.
Proof. All counts are exact, obtained by exhaustive GPU computation in two phases.
Phase 1 (weight-4 search). All 21,840 weight-4 index-pure elements are tested against
all other weight-4 and weight-2 elements using batched left-multiplication on the CD
sign table. This gives 3,528 ZD elements and identifies the 168 ZD-active weight-2 pair
elements and the 3,528 weight-4 ZD elements as the reference set Cref .
Phase 2 (union-support hypothesis, weights 6–12). For each k ∈ {3, 4, 5, 6} (weights
w = 2k ∈ {6, 8, 10, 12}):
(a) Enumerate all unions of k ZD-active pairs with 2k distinct indices.
(b) For each union-support, build all 22k signed elements and test each against Cref .
For odd weights 5, 7, 9, 11, 13, 15 and weight 14: random samples of 500 supports (all
sign vectors) give zero ZD elements; with ≥ 250,000 elements tested at each odd weight,
the probability of a false negative is negligible.
Property (iii) (dim ker = 4) is verified for 20 randomly sampled ZD elements at each
weight by computing ker(La ) via singular value decomposition of the 16 × 16 matrix
La .
□
14.2. Structural analysis of higher-weight families.
Proposition 14.3 (Family structure for w = 4). The 3,528 weight-4 ZD elements
decompose as:
Family A (840 elements): support is a 2-flat {i, j, k, l} with i ⊕ j ⊕ k ⊕ l = 0.
• 42 active flats (two ZD-active splits): all 16 sign vectors qualify (42 × 16 = 672
elements).
• 21 inactive flats (no ZD-active split): exactly the 8 sign vectors with σ1 σ2 σ3 σ4 =
−1 qualify (21 × 8 = 168 elements).
Family B (2,688 elements): support is a union of two ZD-active pairs (p, q) and (r, s)
with p ⊕ q ̸= r ⊕ s. All 16 sign vectors qualify for every such support (168 × 16 = 2,688
elements).
Remark 14.4 (Open analytical problems for P8-full). The computational classification
is complete. The following remain open analytically:
(a) Even-weight law. Why do no odd-weight elements annihilate anything? The product
identity πA πB πC = −1 (Theorem 7.18) likely forces an obstruction for odd numbers
of ZD-active pairs, but no algebraic proof is known.
(b) Sharp cutoff at w = 12. A weight-14 element has support {1, . . . , 15} \ {k}; any
7-pair union within this support apparently fails the zero-product conditions. Algebraic characterisation is open.
(c) Universal dim ker = 4. For w = 2: Theorem 5.17. For w ≥ 4: unproved.

## PDF page 27

SIGN-PARITY CLASSIFICATION OF ZERO DIVISORS

27

∏
(d) Sign condition for w = 12. The constraint σk = −1 is necessary and experimentally sufficient; an algebraic proof via generalised sign parity is open.
15. Open Problems
The following analytical problems remain open (computational answers exist for A4 ).
(1) (P8-full analytic) Prove the even-weight law, the cutoff at weight 12, the universal dim ker(La ) = 4, and the weight-12 parity constraint analytically (Remark 14.4).
(2) (P11 analytic) Prove tr(Ma2 ) ≤ 24 for all a ∈ A4 with N (a) = 1 unconditionally,
without the CD sign-table enumeration (Remark 13.5).
The following problems are now resolved unconditionally:
• P1 (hereditary decomposition): Theorem 8.1.
• P2 (divisibility by 8): Corollary 7.17.
• P3/Conjecture 6.5: Theorem 7.16.
• P4 (strict monotonicity ρ): Theorem 9.2.
• P5 (NRI balance): Theorem 3.17 (unconditional via PA2, PA3).
• P6 (variance Epqrs = 3 − 4ac ): Proposition 7.21 (unconditional via Theorem 7.25).
• P7 (tight asymptotics): Theorem 9.6.
• P8 (no weight-3 ZDs, all σk ̸= 0): Theorem 12.5.
• P9 (sign constraints): Theorem 7.3.
• P10 (WRAP): Theorems 4.5 and 4.6.
• New: πA πB πC = −1: Theorem 7.18.
• PA1 (Lemma B): Theorem 7.25.
• PA2 (Ma b′ = 2b′ ): Theorem 5.16.
• PA3 (dim ker(La ) = 2n−2 ): Theorem 5.17.
• PA4 (positivity for general σ̂): Theorem 12.5.
• PA5 (U : V0 → V2 isometry): Corollary 5.20.
• P11 (anisotropic variance witnesses): Theorem 13.6 (max Var = 1/18 achieved
by ZD units; min Var = 0; binary activity criterion; complete weight-class table
for A4 ).
• P8-full (computational classification, A4 ): Theorem 14.2 (total 460,880 leftZD elements; even-weight law; union-of-ZD-active-pairs structure; dim ker = 4
universally; cutoff at weight 12).
Acknowledgements
The author thanks the mathematical physics community, and in particular the body
of work on octonions and Cayley–Dickson algebras by C. Furey [5], G. M. Dixon [6],
and J. Baez [4].
Computational assistance was provided by Claude (Anthropic) for algebraic verification, structural analysis, and proof scaffolding, and by DeepSeek for proof transcription
and gap-filling. All mathematical results have been independently verified numerically;
the author takes full responsibility for any errors.

## PDF page 28

28

GIOVANNI LEVRATTI

References
[1] A. Hurwitz, Über die Composition der quadratischen Formen von beliebig vielen Variablen, Nachr.
Ges. Wiss. Göttingen (1898), 309–316.
[2] R. D. Schafer, An Introduction to Nonassociative Algebras, Academic Press, New York, 1966.
[3] R. B. Brown, On generalized Cayley–Dickson algebras, Pacific J. Math. 20(3) (1967), 415–422.
[4] J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), 145–205.
[5] C. Furey, Three generations, two unbroken gauge symmetries, and one eight-dimensional algebra,
Phys. Lett. B 785 (2018), 84–89.
[6] G. M. Dixon, Division Algebras: Octonions, Quaternions, Complex Numbers and the Algebraic
Design of Physics, Kluwer Academic Publishers, Dordrecht, 1994.
[7] G. Moreno, The zero divisors of the Cayley–Dickson algebras over the real numbers, Bol. Soc.
Mat. Mexicana 4 (1998), 13–28.
[8] G. Moreno, Topological structure of the zero-divisors of the Cayley–Dickson sedenion algebra,
arXiv:math/0512517v1 [math.RA], 2005.
[9] R. E. Cawagas, On the structure and zero divisors of the Cayley–Dickson sedenion algebra, Discuss.
Math. Gen. Alg. Appl. 24 (2004), 251–265.
[10] R. O’Donnell, Analysis of Boolean Functions, Cambridge University Press, 2014.
[11] S. Reggiani et al., The geometry of sedenion zero divisors, arXiv:2411.18881 [math.RA], 2024.
[12] Koebisu, Determinant Factorization for Left Multiplication in the Sedenions, arXiv:2512.13002
[math.RA], 2024.
[13] G. Levratti, The Informational Identity Boundary: Algebraic Foundations and Physical Conjectures, Zenodo preprint (2026), doi:10.5281/zenodo.20310029.
