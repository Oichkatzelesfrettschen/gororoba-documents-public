Source: https://raw.githubusercontent.com/openai/math/7ef5c0cc5ca4b0e072b7a050fca09ab24bc6fa3a/preprints/A-quadratic-bound-for-Jacobsthals-function-September-25-2026/paper.pdf
PDF sha256: f80267eebc82a9b8905057b45b35ef8734485b2b0b7b809a3051c06240cf0b1e
License: https://www.apache.org/licenses/LICENSE-2.0 (copy in LICENSES/Apache-2.0.txt)
Language: eng
Fidelity: machine (failed: characters)

# Transcription of openai-math-021-jacobsthal-quadratic-bound.pdf

Transcription of `openai-math-021-jacobsthal-quadratic-bound.pdf` in this directory, 83 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-83 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

A quadratic bound for Jacobsthal’s function
OpenAI
September 25, 2026

Abstract
Let h(k) be the least integer such that every interval of h(k) consecutive integers
contains an integer coprime to any prescribed positive integer having at most k distinct
prime divisors. We prove h(k) ≪ k 2 /(log log(3k))2 , giving an affirmative answer to
Jacobsthal’s quadratic-bound question.

Contents
1 Introduction

2

2 Sieve and prime-distribution inputs
2.1 Small-prime counts in a progression

. . . . . . . . . . . . . . . . . . . . . . .

6
8

3 The decreasing-prime tree
3.1 The reference tree . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
3.2 Comparison after stopping . . . . . . . . . . . . . . . . . . . . . . . . . . . . .

8
11
11

4 Delay functions and the continuous path process
4.1 Future integrals for the sieve functions . . . . . . . . . . . . . . . . . . . . . .
4.2 Derivative weights and change of measure . . . . . . . . . . . . . . . . . . . .
4.3 Regeneration and invariant occupation . . . . . . . . . . . . . . . . . . . . . .
4.4 Renewal limits and uniform band estimates . . . . . . . . . . . . . . . . . . .
4.5 Visits in a prescribed even-state window . . . . . . . . . . . . . . . . . . . . .

11
12
15
17
19
22

5 Passage from harmonic paths to primes

23

6 Evaluation of the reference tree
6.1 The quadrature error above the boundary . . . . . . . . . . . . . . . . . . . .
6.2 The boundary anomaly . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
6.3 The signed correction integral . . . . . . . . . . . . . . . . . . . . . . . . . . .
6.4 A uniform local comparison . . . . . . . . . . . . . . . . . . . . . . . . . . . .

28
29
31
32
35

7 Compact errors and independent prime boxes
7.1 A recent witnessing edge . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
7.2 Bins, boxes, and regular endpoints . . . . . . . . . . . . . . . . . . . . . . . .

36
37
37

8 An inverse estimate for a witnessing edge

43

1

## PDF page 2

9 Variance after the inverse estimate
9.1 Arithmetic coordinates . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.2 Variance of independent classes . . . . . . . . . . . . . . . . . . . . . . . . . .
9.3 The effective-size alternative . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9.4 Hard endpoints and global eligibility . . . . . . . . . . . . . . . . . . . . . . .

53
53
55
56
59

10 Stops for endpoints with small effective size
10.1 Owners, tags, and a stopping rule . . . . . . . . . . . . . . . . . . . . . . . . .
10.2 The average over a large prime bin . . . . . . . . . . . . . . . . . . . . . . . .
10.3 Comparison at the actual stops . . . . . . . . . . . . . . . . . . . . . . . . . .
10.4 Almost every hard endpoint lies below a stop . . . . . . . . . . . . . . . . . .

60
61
62
67
68

11 Completion of the proof
11.1 The error budget . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
11.2 Removing the remaining divisor primes . . . . . . . . . . . . . . . . . . . . .

70
71
72

A A modular hyperbola count

74

B Elementary forms of four auxiliary estimates
B.1 The continuous Buchstab normalization . . . . . . . . . . . . . . . . . . . . .
B.2 The additive large sieve at the required order . . . . . . . . . . . . . . . . . .
B.3 A degree-uniform plane-curve intersection bound . . . . . . . . . . . . . . . .
B.4 An order bound for primes in a progression . . . . . . . . . . . . . . . . . . .

77
77
79
79
80

References

81

1

Introduction

For a positive integer n, let j(n) be the least positive integer m such that every interval of m
consecutive integers contains an integer coprime to n. Write ω(n) for the number of distinct
prime divisors of n, with ω(1) = 0, and put
h(k) = sup j(n),

k ≥ 1.

n≥1
ω(n)≤k

The starting point of the interval is arbitrary, and replacing n by the product of its distinct
prime divisors does not change j(n). Thus h(k) − 1 is the greatest length of an interval that
can be covered by the divisibility classes of at most k primes.
Jacobsthal studied this function in a series of papers beginning in 1960 [17]. Erdős
subsequently recorded Jacobsthal’s question whether h(k) ≪ k 2 [3, p. 163, equations (1) and
(3)]. In Erdős’s notation, C(k)+1 is the maximum of j(n) over integers with exactly k distinct
prime divisors. This equals our h(k): adjoining prime divisors cannot decrease j(n). We prove
the following bound, which gives an affirmative answer and a further iterated-logarithmic
saving.
Theorem 1.1. There is an absolute constant C > 0 such that
h(k) ≤ C

k2
(log log(3k))2

for every integer k ≥ 1.

All logarithms are natural. In particular the theorem gives a uniform quadratic bound
for arbitrary sets of prime divisors, with no restriction on their sizes or on the interval’s
translation.
2

## PDF page 3

Historical context and related work
The development of the upper bound is closely tied to sieve theory. Erdős observed that
Brun’s method gives h(k) ≪ k C0 for some absolute exponent C0 [3, p. 163]. Iwaniec’s work on
the error term in the linear sieve gave an estimate of order k 2 log2 k when the prime divisors
are the first k primes [14]; this primorial case is distinguished explicitly in [25, p. 329] and
[15, pp. 225–226]. Vaughan then proved the uniform estimate
)4

j(n) ≪ ω(n)2 log(2ω(n))
(

(n > 1)

[25, Theorem, p. 329]. Iwaniec’s shifted-sieve argument removed two logarithmic factors and
established h(k) ≪ k 2 log2 k for arbitrary prime sets [15, Theorem and Corollary, p. 226].
Theorem 1.1 improves this bound and, in particular, reaches the quadratic scale asked for by
Jacobsthal.
Vaughan explained the exponent 2 through the one-dimensional sieve’s restriction to
moduli near the square root of the interval length [25, p. 329]. In the usual linear-sieve
notation this appears as the vanishing of the lower function f at sieve parameter 2. Our
proof also reaches this limiting parameter. It keeps a boundary contribution that disappears
from the leading linear-sieve term, and then controls the discrepancy between this reference
calculation and the actual prescribed classes. The latter comparison requires the inverse
estimate and the stopped counts developed below; positivity of the reference calculation alone
does not give a lower bound for the original sieve.
A separate question concerns which prime sets give the largest gap. Let pk denote the
∏
kth prime and Pk = ki=1 pi . Jacobsthal suggested that j(Pk ) = h(k) for every k. Hajdu and
Saradha proved equality for k ≤ 23, but found
j(P24 ) = 234 < 236 = h(24)
[11, Theorem 1.2]. Thus the primorial extremality conjecture is distinct from the quadraticbound question, and a theorem only about j(Pk ) does not settle the uniform problem. The
computational literature reflects this distinction. Costello and Watts obtained recursive lower
bounds for the minimum number of integers coprime to Pk in an interval, and used them
to compute upper bounds for j(Pk ) [2, Theorem 4.4 and Section 5]. Ziller computed the
maximum over arbitrary prime sets through 43 prime factors [29, Section 3]. These finite
computations concern explicit values, whereas the constant in Theorem 1.1 is not made
explicit.
Primorials nevertheless give the strongest lower bounds relevant to the order of h(k).
They arise from constructions of long covered intervals, which also produce large gaps between
consecutive primes. Erdős’s account already places Rankin’s lower-bound construction beside
Brun’s polynomial upper bound [3, p. 163, equation (2)]. The later construction of Ford,
Green, Konyagin, Maynard and Tao gives
j(Pk ) ≫ k(log k)2

log log log k
log log k

(k −→ ∞)

(1.1)

[5, Section 1.1]. Indeed, their covered-interval bound at prime cutoff x is
≫ x log x log log log x/ log log x;
take x = pk and use pk ∼ k log k. Since j(Pk ) ≤ h(k), this supplies a lower bound for the
uniform maximum as well. It is an existence construction and does not assert the same lower
bound for every integer with k prime divisors. The gap between (1.1) and our upper bound
remains substantial. Vaughan suggested the stronger possible estimate j(n) ≪ε ω(n)1+ε for
n > 1 and each fixed ε > 0 [25, p. 329].
3

## PDF page 4

A quantitative covering estimate
The proof works with one prescribed residue class at each prime below a size cutoff. This is
another form of the same covering problem: for a finite prime set, the Chinese remainder
theorem supplies an integer b with b ≡ ap (mod p) at every prime in the set, and
n ̸≡ ap

(mod p) for every such p

⇐⇒

(

gcd n − b,

∏ )

p = 1.

This equivalence explains why arbitrary classes and arbitrary translations occur together; see
also [11, Lemma 2.1].
For sufficiently large real z, set
⌊

L = log z,

⌋

z2
Y =
,
L2

L
,
(log L)2
)
∏ (
1
1−
.
V0 =
p
p≤w
w=

B=

L
,
log w

(1.2)

Products indexed by a letter explicitly called prime always range over primes. The two cutoffs
separate the small primes, which are sieved inside arithmetic progressions, from the primes
in (w, z], which index the expansion used in the proof. The quantity B is the logarithmic
size of the upper cutoff in base w.
Theorem 1.2. There are absolute constants c > 0 and z0 with the following property. For
every real z ≥ z0 and every choice of a residue class ap (mod p) for each prime p ≤ z,
#{1 ≤ n ≤ Y : n ̸≡ ap

(mod p) for every p ≤ z} ≥ c

Y V0
.
B2

(1.3)

Mertens’ theorem identifies the size of this lower bound:
Y log w
Y V0
∼ e−γ
.
2
B
L2

(1.4)

The number of survivors, rather than positivity alone, permits the passage from a prime
cutoff to a bound in terms of the number of prime divisors. For sufficiently large k, if n has at
most k distinct prime divisors, apply Theorem 1.2 at a cutoff z = A0 k log k/ log log k, where
A0 is a sufficiently large fixed constant. A progression upper sieve bounds the total number
of these survivors removed by the remaining divisor primes q > z by O(k(1 + X/ log X)),
where X = Y /z. The lower bound in (1.4) dominates this loss for that choice of A0 , while
Y ≍ k 2 /(log log k)2 . Section 11 gives the comparison with constants and handles the bounded
range of k.
The quantitative estimate also relates to the interval-sieve quantity studied by Banks,
Ford and Tao [1, Sections 1.3–1.4]. They minimize the survivor count over all choices of
forbidden classes at primes up to (y/ log y)1/2 in an interval of length y. At that cutoff a
2
classical lower sieve gives a bound of order
√ y log log y/(log y) . Theorem 1.2 retains this order
of magnitude at the larger cutoff z ≍ Y log Y . The classes here are arbitrary; no random
choice of the forbidden classes is assumed in this theorem.

Outline of the argument
The proof has two parts: a reference calculation for a decreasing-prime expansion, and a
comparison with the actual residue classes. Section 3 partitions discarded integers by the
least prime at which they hit a forbidden class. Iteration gives tuples of strictly decreasing
primes. At even depths the expansion is a lower bound, and at odd depths it is an upper
4

## PDF page 5

bound. An admission rule limits the progressions retained in this expansion so that each
is long enough for an absolute upper sieve. Replacing its small-prime count by progression
coordinate length times V0 defines the reference tree.
The leading reference term is governed by the classical linear-sieve functions f, F [21,
Section 21.2.2], with the root tending to the critical parameter 2. The lower exponent
cutoff leaves a boundary contribution on the smaller scale B −2 . Each prime path has weight
equal to the reciprocal product of its primes. Replacing reciprocal-prime sums by harmonic
integrals dx/x gives a continuous reference process. To evaluate the boundary contribution,
Section 4 uses derivative weights of f, F to normalize its transitions to a probability kernel.
Its regeneration cycles give limiting occupation measures, which Section 5 transfers to prime
tuples. Section 6 then evaluates the boundary contribution and bounds the losses imposed by
the admission rule. A positive margin remains after these losses and the negative contribution
from the root’s small displacement below parameter 2.
The actual small-prime counts agree with their reference values in long progressions, by
the fundamental lemma of sieve theory. At a short progression, a large relative discrepancy
must already be visible along one of the last few edges of its path. Section 7 places these paths
in boxes in which selected prime factors vary independently. An inverse estimate in Section 8
shows that many discrepant edges force alignment with one of finitely many rationals A/D:
a prime p aligns when Dap ≡ A (mod p).
The inverse step is related to the principle that modular concentration forces algebraic
structure, developed by Helfgott and Venkatesh and by Walsh [13, 27]. Our argument uses
partial incidence constraints in a single prime bin and obtains a rational list fixed for the whole
box. It combines polynomial interpolation with Jarník’s convex-arc lattice-point argument
[18] and the pair-counting principle of Gallagher’s larger sieve [7]. Variance estimates in
Section 9 then show that a rational can account for many discrepant endpoints only when its
effective modulus and intercept are small. The pair-moment calculation is a truncated form
of mean singular-series averaging [8]; the paper proves the required uniformity and stability
under the changes of measure used here.
For the endpoints remaining after this argument, many earlier prime factors align with
the same rational. Section 10 stops their branches at suitable even nodes. The stop rule
depends on prime bins in a way that permits one aligned prime to vary over a large subset
of its bin. Averaging over that prime gives more exact survivors than the reference subtree
requires. A marked-renewal argument shows that all but an arbitrarily small amount of the
exceptional path mass reaches one of these stops.
The comparison identity (3.7) joins these parts. Proposition 6.3 supplies a positive
reference term; the inverse and variance estimates leave only the endpoints of Corollary 9.3;
and Propositions 10.5 and 10.6 supply the stopped comparison and its coverage. Section 11
bounds the total remaining discrepancy, proves Theorem 1.2, and deduces Theorem 1.1.

Conventions
The constants in the proof are absolute after the explicitly stated parameters have been
chosen. They need not be effective. Whenever a bin width ξ occurs, it is fixed before z tends
to infinity. Constants independent of sufficiently small fixed ξ do not assert uniformity for a
width ξ(z) tending to zero. This order matters in the rational-list and stopping arguments.
We use φ for Euler’s totient, τ for the divisor function, rad(m) for the product of the
distinct prime divisors of m, and ū for a multiplicative inverse in a displayed modulus. All
rationals A/D used for alignment are reduced, with D > 0.

5

## PDF page 6

2

Sieve and prime-distribution inputs

We state the forms of the classical estimates used in the proof. Appendix B supplies elementary
proofs of the Buchstab normalization, the required additive large-sieve bound and the planecurve intersection estimate, and derives the progression upper bound from the fundamental
lemma. The inverse and stopping arguments in the later sections are proved directly.
Lemma 2.1 (Fundamental lemma of the sieve). Let P be any subset of the primes at most v.
Suppose that intersection counts for bad conditions indexed by squarefree products l of primes
in P have the form
Xg(l) + rl ,
where g is multiplicative and
0 ≤ g(p) ≤

2
,
p

g(2) ≤

g(p) < 1,

1
2

if 2 ∈ P.

There are absolute constants c, C > 0 and s0 such that for s ≥ s0 the count avoiding all the
bad conditions is


X

∏

(

(1 − g(p)) 1 + O(e




) + O



−cs )


∑

l≤v s
l squarefree
p|l⇒p∈P

p∈P




τ (l)C |rl | .



(2.1)

The same statement holds for nonnegative weighted counts. A local condition that makes the
sifted set empty may instead be removed from consideration as an exactly empty case.
This is a standard dimension-two form of the fundamental lemma; see [24, Lemma 2.8,
p. S137], which records the stronger remainder sum without divisor weights and attributes
the result to [6, Corollary 6.10]. To check the uniform dimension condition here, put g(p) = 0
outside P. For p ≥ 3,
(1 − 2/p)−1 = (1 − 1/p)−2 1 + O(p−2 ) .
(

)

Mertens’ theorem therefore gives
∏

(1 − g(p))

−1

(

≤K

u≤p<v

log v
log u

)2

(2 ≤ u < v)

with an absolute K. The factor at 2 is at most 2. The sieve weights depend only on
intersections of the bad conditions, so their use is not restricted to literal divisibility conditions.
Lemma 2.2 (Prime-distribution estimates). The following estimates will be used, with
absolute constants unless fixed subscripts indicate a dependence.
(i) There is c > 0 such that
(

π(v) = li(v) + O

v −c√log v
e
,
log v
)

∏

(1 − 1/p) =

p≤v

Decreasing c absorbs harmless powers of log v.

6

√
)
e−γ (
1 + O(e−c log v ) .
log v

## PDF page 7

(ii) For every fixed A, M > 0, uniformly for q ≤ (log v)A and (a, q) = 1,
li(v)
v
+ OA,M
φ(q)
(log v)M
(

π(v; q, a) =

)

.

The implied constants may be ineffective.
(iii) For (a, q) = 1 and H/q exceeding a suitable absolute constant,
#{x < p ≤ x + H : p ≡ a

(mod q)} ≪

H
.
φ(q) log(H/q)

(iv) Uniformly for v 9/10 ≤ H ≤ v as v → ∞,
#{v − H < p ≤ v} ≥ (1 − o(1))

H
.
log v

Part (i) is the classical zero-free-region PNT together with its Mertens product consequence;
see [16], and the stronger explicit PNT error in [4]. Parts (ii) and (iii) are Siegel–Walfisz and
Brun–Titchmarsh; see the explicit statements in [9, p. 75] and [10, Theorem 1.4.4, p. 39],
respectively. Lemma B.4 derives the order bound in part (iii) from the stated sieve input and
Mertens’ formula. Part (iv) follows from the short-interval PNT of Huxley, for example in
Heath-Brown’s proof [12, Theorem, p. 1365]. To see that a fixed-exponent version suffices,
tile an interval of length at least v 9/10 by intervals ending at x of length x4/5 . Stop before
the final incomplete tile or before x < v 1/2 . The lost total length is O(v 4/5 + v 1/2 ) = o(H).
All remaining endpoints tend to infinity uniformly, so the fixed-exponent theorem sums over
the tiles. Prime powers contribute a negligible amount, and log p ≤ log v gives the stated
prime-count lower bound.
We also use the additive large sieve in the following standard form: for distinct reduced
fractions with denominators at most Q, and coefficients supported on J consecutive integers,
∣
∣2
∣
∣
∑ ∣∑
∑
∣
∣
bj e(aj/q)∣∣ ≪ (J + Q2 )
|bj |2 ,
∣
∣
∣
j
q≤Q a mod q j
∑

e(t) = e2πit .

(2.2)

(a,q)=1

See [20] and [26, Theorem 3]. Lemma B.2 proves the order bound needed here.
For the complete Kloosterman sum
(
)
∑
hu + kū
Kl(h, k; N ) =
e
N
u mod N
(u,N )=1

we use
| Kl(h, k; N )| ≪ τ (N )(h, k, N )1/2 N 1/2 .

(2.3)

This holds for arbitrary positive moduli, including prime powers, and for noncoprime or zero
frequencies; see [19, Lemma 7.1] and [16, Corollary 11.12, p. 280]. The gcd factor in (2.3)
will be retained in all completions.
The probability input is the nonarithmetic iid key renewal theorem: if positive iid
increments have finite positive mean µ, renewal measure U , and H is directly Riemann
integrable, then
∫
1
(U ∗ H)(v) −→
H(u) du.
(2.4)
µ R
We apply the usual half-line theorem after translating tests that vanish on a left half-line;
see [23, Section 2.7, Theorem 35]. The regeneration, finite-mean, nonarithmetic and directintegrability hypotheses needed here are proved in Section 4. There we also use the classical
Buchstab limit ωBu (s) → e−γ , with its independent local proof in Lemma B.1; see also [22,
Section 28.9, p. 236].
7

## PDF page 8

2.1

Small-prime counts in a progression

Lemma 2.3. Let one forbidden class be given at every prime p ≤ u, where u → ∞. Count
the points in a progression segment whose coordinate interval has real length J, and whose
∏
step is coprime to every prime p ≤ u. Put Vsm (u) = p≤u (1 − 1/p). For each fixed η > 0,
uniformly when J ≥ uη , its sifted count N satisfies
N ≪η JVsm (u).

(2.5)

There are absolute c1 , C1 > 0 and a sufficiently large fixed v0 such that, writing v = logu J,
uniformly for v ≥ v0 ,
∣
∣
∣
∣
N
−c1 v
∣
∣
.
(2.6)
∣ JV (u) − 1∣ ≤ C1 e
sm
All estimates are independent of the progression’s initial point, step and forbidden classes.
Proof. For any squarefree l supported on the small primes, the simultaneous bad conditions
specify one class of the progression coordinate modulo l. Their count is J/l + O(1), with an
absolute error independent of the step and the classes. Apply Lemma 2.1 at level J 1/2 . Its
sieve parameter is v/2, and the remainder sum is
≪ J 1/2 (1 + log J)C2
for an absolute fixed C2 . After division by JVsm (u), this is
≪ J −1/2 (1 + log J)C2 log u.
For all sufficiently large u this is at most e−c1 v uniformly for v ≥ v0 , on decreasing c1 and
increasing v0 if necessary. The relative fundamental-lemma error has the same form. This
proves (2.6).
For (2.5), sieve only by primes at most uθ , where 0 < θ < 1 is fixed sufficiently small in
terms of η. At level J 1/2 the sieve parameter is at least η/(2θ) and can therefore be made
larger than s0 . The upper fundamental lemma gives
N ≪ JVsm (uθ ) + J 1/2 (1 + log J)C2 ≪η JVsm (u),
using Mertens and J ≥ uη . The same calculation covers either endpoint convention and
nonintegral J, since each intersection still has an O(1) endpoint error.
We will repeatedly apply (2.5) to short difference pieces created by freezing an interval
length. If ξ > 0 is fixed and the coordinate length of such a piece is comparable to ξJ, with
ξJ ≥ uη , its cost is Oη (ξJVsm (u)). The constant does not depend on ξ; the threshold from
which the length inequality holds may depend on that fixed width. The same observation
applies to a specified residue subsequence of the piece.

3

The decreasing-prime tree

Fix the residue classes in Theorem 1.2, and use (1.2). Set
a⋆ =

1
,
100

x(p) =

log p
.
log w

Thus x(p) measures a prime’s exponent in base w, and 1 < x(p) ≤ B for p ∈ (w, z]. A node
is a finite tuple of strictly decreasing primes in (w, z]. Its product is denoted by d, with d = 1
for the empty tuple. Put
Jd =

Y
,
d

rd = logw Jd − a⋆ + 2,
8

µd = Jd V0 .

(3.1)

## PDF page 9

At the root, r0 = 2B − a⋆ + o(1) and the cutoff is b = B. At a nonempty node, the cutoff is
b = x(plast ), and the available primes satisfy w < p < plast . The root cutoff includes p = z
when z is prime. All subsequent cutoffs are strict.
Let Nd count integers 1 ≤ n ≤ Y that hit every prescribed class at the prime factors of
d and avoid every prescribed class at the primes at most w. Let Sd (b) impose, in addition,
avoidance at all available primes above w up to the cutoff. In particular, the survivor count in
Theorem 1.2 is S1 (B). The simultaneous hits give one class modulo d, so Lemma 2.3 applies
in its progression coordinates.
Partition the integers counted by Nd but not by Sd (b) according to their smallest bad
available prime. This gives the exact identity
Sd (b) = Nd −

∑

Sdp (x(p)).

(3.2)

p available

Although the partition uses the smallest bad prime, iteration produces decreasing prime
tuples because the child count avoids all smaller available primes.
Nodes of even length are called lower nodes, and nodes of odd length are called upper
nodes. From a lower node include every available child. From an upper node include a child
with exponent x = x(p) exactly when
r − x ≥ H(x),

H(x) = max(2x, x + 2),

(3.3)

where r is the parent’s gap. Other children are omitted.
Lemma 3.1. The alternating sum of the Nd over all included nodes is a lower bound for
S1 (B). More generally, one may stop at any prefix-free collection of included lower nodes,
use their exact counts Sd (b), and expand only the other nodes. The resulting expression is
still a lower bound for S1 (B). Every included node satisfies Jd ≥ wa⋆ .
Proof. The tree is finite because all factors are distinct primes at most z. Work upward from
its leaves. At a lower node, replacing each child by an upper bound in (3.2) gives a lower
bound. At an upper node, omitting nonnegative child counts and replacing the retained
children by lower bounds gives an upper bound. This proves the sign assertion by induction.
An exact count at a lower node is an admissible lower bound there; prefix-freeness ensures
that its descendants are not expanded as well.
At a nonroot lower node, admission gives r ≥ 2b and r ≥ b + 2. Every child exponent
satisfies 1 < x ≤ b, so its gap is at least 2. At the root, r0 − B = B − a⋆ + o(1) > 2 for large z,
giving the same conclusion for every first child. Included lower nodes also have gap exceeding
2 by their admission rule. Hence all included nodes have logw Jd = rd − 2 + a⋆ ≥ a⋆ .
Figure 1 separates the admission decision at an upper node from the later choice of lower
stops.
In particular, uniformly at included nodes,
Nd
≪a⋆ 1,
µd

∣
∣
∣ Nd
∣
−c1 logw Jd
∣
∣
∣ µ − 1∣ ≪ e
d

when logw Jd ≥ v0 .

(3.4)

The absolute upper bound remains valid on the slightly enlarged progressions with Jd ≥ wa⋆ /2
that will arise in boxes.

9

## PDF page 10

Expanded lower node d
every available child is included

p
?
Included upper node dp
test each prospective lower child


9



 q




XXX
q

′

XXX

XXX
u
XX

X
z
X

?
Included lower node dpq
chosen stop: retain
Sdpq (x(q)) exactly

Included lower node dpq ′
continue its
lower-bound expansion

q, q ′ satisfy (3.3)

Prospective child dpu
omitted by the
admission rule
u fails (3.3)

Figure 1: Admission and stopping have different roles. Only selected branches are drawn, with
q, q ′ , u < p. At the upper node, admission is the test rdp − x(v) ≥ H(x(v)) for the prospective
prime v. The omitted child dpu does not belong to the included tree. The admitted child dpq
is shown as a member of a separately chosen, prefix-free set of lower stops; its descendants
are replaced by its exact survivor count. Other included lower nodes continue to expand.
The specific stop rule is given in Section 10.

10

## PDF page 11

3.1

The reference tree

Replace Nd by µd in the unstopped tree. Divide a subtree value by its own µd , and denote
the result by Pe (r, b) or Po (r, b) according to parity. Dependence on w and on the endpoint
convention is left implicit. Since µdp = µd /p, the recursions are
Pe (r, b) = 1 −

1
Po (r − x(p), x(p)),
p
p available
∑

∑

Po (r, b) = 1 −

p available
r−x(p)≥H(x(p))

(3.5)

1
Pe (r − x(p), x(p)).
p

The reference value at the root is Y V0 Pe (r0 , B). Auxiliary starting states used below follow
the same recursions on their declared domains; no actual forbidden classes are needed to
define them.
A path’s harmonic weight is the reciprocal product of its chosen primes. Dropping all
admission restrictions shows that the sum of the weights of all decreasing-prime prefixes is
∏ (

1+

w<p≤z

1
p

)

≪ B.

(3.6)

Indeed log(1 + 1/p) = 1/p + O(p−2 ), and the reciprocal-prime sum is log B + O(1).
We also use standard paths: these keep only the admission condition r − x ≥ 2x at an
upper node. They contain all paths of the original tree and agree with it whenever the next
exponent is at least 2. The continuous harmonic model replaces reciprocal-prime sums by
dx/x, with decreasing real exponents. It will be studied first, then compared with the actual
prime paths.

3.2

Comparison after stopping

For later use, the comparison identity can be recorded explicitly. Let T be the retained
expanded nodes of a stopped tree, excluding the stop nodes, and let S be its prefix-free set of
lower stops. If Lstop is its lower-bound value, then
Lstop − Y V0 Pe (r0 , B) =

∑

(−1)ω(d) (Nd − µd )

d∈T

+

∑(

)

Sd (bd ) − µd Pe (rd , bd ) .

(3.7)

d∈S

Here a node is identified by its decreasing tuple, equivalently by its squarefree product. To
verify the identity, expand the full reference tree down to the same stops; at each stop its
remaining subtree is exactly µd Pe (rd , bd ). Thus a positive reference margin, a small sum
of retained absolute errors, and an aggregate nonnegative stopped difference will prove
Theorem 1.2.

4

Delay functions and the continuous path process

We first analyze the continuous model in which a prime exponent is chosen with harmonic
measure dx/x. The linear-sieve functions provide its benchmark, and their derivatives will
convert harmonic path weights into probability weights. We then use regeneration to evaluate
compact-endpoint sums at scale B −2 and to control their tails. These are the estimates
needed to propagate the reference tree’s boundary discrepancy.
11

## PDF page 12

4.1

Future integrals for the sieve functions

We use the classical lower and upper linear-sieve functions; see [21, Section 21.2.2]. The
future-integral and path representations needed below are developed here.
Write A = 2eγ . Define the continuous delay functions f, F by
f (s) = 0

(0 ≤ s ≤ 2),

sF (s) = A

(1 ≤ s ≤ 3),

and
(sf (s))′ = F (s − 1)

(sF (s))′ = f (s − 1)

(s > 2),

(s > 3).

These prescriptions determine the functions successively on intervals of length one. We shall
also use F (s) = A/s on 0.95 ≤ s < 1. Only at a starting lower state, and when defining its
derivative weight, we continue f below 2 by
fext (s) =

A log(s − 1)
s

(1.98 ≤ s < 2).

(4.1)

This is the same expression as the ordinary f on 2 ≤ s ≤ 4. An omitted lower child of ratio
less than 2 always has benchmark f = 0; the continuation (4.1) is not used at such a child.
Put fe = f and fo = F . The continuous benchmark at a state of type i, gap r, and cutoff
b is fi (r/b)/b. For fixed r, the delay equations give
d
db

(

fi (r/b)
b

)

=−

fi′ (r/b − 1)
,
b2

(4.2)

where i′ is the opposite type. On the right, the value at an omitted lower child is defined
to be zero, including when its formal ratio is negative. On the ordinary ranges the identity
holds for r/b > 2 at a lower state and r/b > 1 at an upper state. At an upper state the right
side is zero when r/b − 1 ≤ 2, exactly as required for an omitted lower child. Integrating with
respect to the cutoff therefore gives the standard continuous tree recurrence above exponent
2, with the boundary value at cutoff 2 left to be specified. The explicit starting extensions
satisfy the same identity in the interiors of their ranges, with one-sided derivatives at the
endpoints; the extension of f is used at the parent lower state, never at an omitted child.
The root lies at r0 /B = 2 − a⋆ /B + o(B −1 ), where the ordinary lower-sieve function
vanishes. Its continued benchmark is
fext (r0 /B)
= −a⋆ eγ B −2 + o(B −2 ),
B
′ (2) = eγ . Thus a positive reference margin must come from the finite boundary,
since fext
after its discrepancy has been propagated through all larger exponents. To evaluate that
contribution, we will use the positive derivative weights of f, F to normalize the harmonic
transitions. The first step is to establish positivity and decay in a form that justifies this
change of measure.
Let ρ be the Dickman function, determined by

ρ(u) = 1

(0 ≤ u ≤ 1),

uρ′ (u) = −ρ(u − 1)

(u > 1).

For the unextended functions put
a(s) = 1 − f (s)

(s ≥ 0),

c(s) = F (s) − 1

12

(s ≥ 1),

c0 (s) =

Aρ(s − 1)
s

(s ≥ 1).

## PDF page 13

Lemma 4.1 (Future integrals). The functions a, c are positive and satisfy, with absolute
comparison constants,
a(s) ≍ c0 (s),

a(s) + c(s) = c0 (s),
∫ ∞

sa(s) =

(s ≥ 1),

(4.3)

c(t) dt

(s ≥ 2),

(4.4)

a(t) dt

(s ≥ 1).

(4.5)

1
ρ(u)
1
≤
≤ .
2
4u
ρ(u − 1)
u

(4.6)

s−1
∫ ∞

sc(s) =

c(s) ≍ c0 (s)

s−1

For u ≥ 2,

Moreover, for each fixed λ > 0, there is Uλ such that
−

ρ′ (u)
≥λ
ρ(u)

(u ≥ Uλ ).

(4.7)

Proof. The delay equation gives the integral identity
∫ u

ρ(v) dv

uρ(u) =

(u ≥ 1).

(4.8)

u−1

For example, both sides agree at u = 1, and their derivatives agree where the delay equation
applies. The identity and the delay equation give positivity and monotonicity: a first zero of ρ
would contradict the positive integral of its immediately preceding values. Monotonicity gives
the upper bound in (4.6). Integrating first over the lower half of each of two unit intervals
gives
ρ(u − 12 )
ρ(u − 1)
ρ(u − 1)
≥
.
ρ(u) ≥
≥
1
2u
4u2
4u(u − 2 )
The upper ratio bound also shows that ρ tends to zero faster than any exponential.
The negative logarithmic derivative is at least 1. If it is at least λ on a tail, then, on a
later tail,
∫ u
1 − e−λ
ρ(v) dv ≤ ρ(u − 1)
.
λ
u−1
Equation (4.8) consequently improves the lower bound to λ/(1 − e−λ ). Iteration tends to
infinity, since this map is strictly larger than its argument and has no finite positive fixed
point. This proves (4.7).
Directly from the delay equations and the initial conditions,
F (s) − f (s) = c0 (s),

F (s) + f (s) = AωBu (s)

(s ≥ 1).

(4.9)

Here the continuous Buchstab function is determined by sωBu (s) = 1 on [1, 2] and (sωBu (s))′ =
ωBu (s − 1) above 2; its limit is stated in Section 2. For the first equality, the equation for
s(F − f ) is the negative delay equation for Aρ(s − 1); for the second, it is the Buchstab
equation with initial value A/s. We next prove the individual positivity and future integrals;
these do not follow merely by taking the difference in (4.9).
To prove these properties, we use an auxiliary absorbing chain. This chain establishes
positivity of the deficits; the harmonic-path chain will instead be defined from the derivative
weights below. For s ≥ 2, give the auxiliary chain transition density
c0 (t)
1
dt,
sc0 (s) {t≥s−1}
13

(4.10)

## PDF page 14

and absorb it on reaching [1, 2). Its normalization is
∫ ∞

∫ ∞

c0 (t) dt = A
s−1

ρ(v)
dv = Aρ(s − 1) = sc0 (s).
s−2 v + 1

The integration at infinity is justified by the decay already proved. The excess of the next
state above s − 1 has tail
ρ(s − 1 + h)
(h ≥ 0).
ρ(s − 1)
For large s, (4.7) bounds this tail by e−λh , with λ as large as desired. For λ > 1, therefore,
E(esnext | s) ≤ es−1

λ
.
λ−1

Taking λ = 2 makes this a strict contraction of V (s) = es , with factor 2/e < 1, outside a
fixed compact. Stopped drift implies almost sure return to that compact. From any state in
the compact, successive draws in [s − 1, s − 1 + 1/4] reach [1, 2) within a bounded number
of steps, with probability bounded below independently of the initial state in the compact.
The densities in these intervals have a positive compact lower bound. Repeating the attempt
after each return proves almost sure absorption.
Alternate labels a, c at every draw. At the terminal state t assign fractions 1/c0 (t) and
1 − 1/c0 (t) to the two labels, respectively. Since c0 (t) = A/t on [1, 2), both terminal fractions
lie in a fixed compact subinterval of (0, 1). The expected terminal fraction, multiplied by
c0 (s), defines positive functions a◦ (s), c◦ (s) with
a◦ + c◦ = c0 ,

a◦ , c◦ ≍ c0 ,

and terminal values a◦ = 1, c◦ = c0 − 1 on [1, 2). The first-step equations give
◦

∫ ∞

sa (s) =

◦

◦

c (t) dt,

∫ ∞

sc (s) =

s−1

a◦ (t) dt

(s ≥ 2).

s−1

In particular these functions are continuous from the right at 2.
Set U = (2 + c◦ − a◦ )/A. The last two equations imply (sU (s))′ = U (s − 1) above 2,
in integrated form, while sU (s) = 1 on [1, 2). Also U (s) → 2/A = e−γ , because a◦ , c◦ are
bounded by c0 . There can be no jump at 2 relative to the continuous Buchstab solution.
Indeed, a jump δ in sU (s) there would give a difference δH(s), where H(s) = 1/s on [2, 3]
and (sH(s))′ = H(s − 1) thereafter. The bound H ≥ 1/3 on [2, 3] persists by induction: if it
holds up to an integer n ≥ 3, then for n ≤ s ≤ n + 1,
∫ s

sH(s) = nH(n) +

H(v − 1) dv ≥ n/3 + (s − n)/3.

n

For either sign of δ ̸= 0, this contradicts U (s) − ωBu (s) → 0, using the independently proved
Buchstab limit in Lemma B.1. Thus U = ωBu . Together with a◦ + c◦ = c0 and (4.9), this
identifies a◦ = a, c◦ = c, proving (4.3) and both future integrals for s ≥ 2. ∫
Finally c(s) = A/s − 1 and a = 1 below 2. The equation at s = 2 gives 1∞ a = A − 2;
hence for 1 ≤ s ≤ 2,
∫ ∞

a(t) dt = 2 − s + A − 2 = A − s = sc(s).

s−1

This proves the remaining range of (4.5).

14

## PDF page 15

4.2

Derivative weights and change of measure

The deficits are now positive and have the required decay. We use derivatives of the sieve
functions to normalize the harmonic transitions of the standard tree.
Define
ϕe (s) = s2 f ′ (s) (s ≥ 2),
ϕo (s) = −s2 F ′ (s) (s ≥ 0.95).
At s = 2 use the right derivative, and on 1.98 ≤ s < 2 use the derivative of (4.1). The state
weight will be ϕi (r/b)/r2 ; its reciprocal at the endpoint is the factor that appears when we
convert a probability estimate back to harmonic weight. For paths from the root, this gives
the scale B −2 when the endpoint gap and ratio remain in fixed compact ranges. Put
W0 (t) =

t+1
,
t2

me (s) = s − 1,

mo (s) = max(2, s − 1).

Lemma 4.2 (Derivative weights). The derivative weights are positive and nonincreasing on
their indicated ranges. If i′ denotes the type opposite to i, then
∫ ∞

ϕi (s) =
mi (s)

W0 (t)ϕi′ (t) dt.

(4.11)

This holds also on the specified starting extensions. On a tail,
ϕe (s) ≍ ρ(s − 2),

ϕo (s) ≍ ρ(s − 2).

(4.12)

There are absolute constants C, q such that the absolute logarithmic derivatives, where they
exist, and the ratios ϕi′ (mi (s))/ϕi (s) are at most C(1 + s)q . In particular, for u, v ≤ S in the
indicated domain of the same weight, with S ≥ 3,
| log ϕi (u) − log ϕi (v)| ≤ C(1 + S)q |u − v|.
For each fixed λ > 0, the negative logarithmic derivatives of both weights are at least λ on a
sufficiently remote tail.
Proof. On the ordinary ranges the delay equations give
(

)

(

ϕe (s) = s a(s) + c(s − 1) ,

)

ϕo (s) = s c(s) + a(s − 1) .

(4.13)

The second expression uses a = 1 on [0, 1]. On the extensions, the explicit formulas are
s
ϕe (s) = A
− log(s − 1) ,
s−1
(

)

ϕo (s) = A

(0.95 ≤ s ≤ 3).

These formulas and Lemma 4.1 prove positivity. Differentiation gives
s
ϕo (s − 1)
(s − 1)2
s
ϕ′o (s) = −
ϕe (s − 1)
(s − 1)2
ϕ′e (s) = −

(s ≥ 1.98),

(4.14)

(s > 3),

(4.15)

at points of differentiability; the odd weight is constant below 3. Equation (4.13) and (4.3)
give (4.12), and in particular both weights vanish at infinity. Integrating (4.14) and (4.15)
backwards from infinity gives (4.11). For the even extension, the lower endpoint lies below 1,
where the explicitly constant odd weight gives exactly the displayed continuation. For odd
s ≤ 3, the lower endpoint is 2, so the integral is constant, as required.
On a tail, (4.6) and (4.12) give
ϕi′ (s − 1)
= O(s2 ).
ϕi (s)
15

## PDF page 16

The derivative formulas then bound the absolute logarithmic derivatives by a polynomial (in
fact O(s) on a tail). On the remaining compact ranges the explicit positive functions and
their piecewise derivatives give fixed bounds. The weights are locally absolutely continuous
by (4.11); integrating the logarithmic derivative gives the stated Lipschitz bound. Finally
the same comparison gives a positive constant times
ρ′ (s − 2)
ρ(s − 3)
s−2
−
=
sρ(s − 2)
s
ρ(s − 2)
(

)

as a lower bound for either negative logarithmic derivative on a tail. Apply (4.7).
A standard path replaces the admission condition (3.3) by r − x ≥ 2x at an upper node.
Thus it contains every path in the original tree, and the two rules agree for x ≥ 2. At a state
of type i, gap r, cutoff b, and ratio s = r/b, make a draw t with probability density
Ki (s, dt) =

W0 (t)ϕi′ (t)
1{t≥mi (s)} dt.
ϕi (s)

(4.16)

Lemma 4.2 proves that this is a probability kernel. The next exponent, gap, and ratio are
x=

r
,
t+1

r′ =

rt
,
t+1

s′ = t.

The lower support endpoint ensures x ≤ b, and the upper-to-lower transition also satisfies
s′ ≥ 2. Put g(t) = log(1 + 1/t), so r′ = re−g(t) .
The harmonic transition dx/x, after reversing orientation in t = r/x − 1, is dt/(t + 1).
Dividing this by (4.16) gives
t2
ϕi (s)
=
(t + 1)2 ϕi′ (t)

( ′ )2

r
r

ϕi (s)
.
ϕi′ (t)

Consequently, for every finite prefix,
(

original harmonic weight = probability weight

rend
rin

)2

ϕiin (sin )
.
ϕiend (send )

(4.17)

For a nonempty prefix its last exponent is x = rend /send . Since successive cutoffs are
nonincreasing, restriction of all exponents to x > ℓ is equivalent to the single arrival condition
send < rend /ℓ.

(4.18)

In the rest of this section, starts are of even type with
sin ∈ [1.99, 2.3].

(4.19)

Let (in , sn ) be the resulting infinite sequence, n = 0, 1, . . ., and put
T0 = 0,

Tn =

n
∑

g(sj ),

rn = rin e−Tn ,

xn = rn /sn

(n ≥ 1).

j=1

After two steps the state spaces are {e} × [2, ∞) and {o} × [1, ∞). Only the first odd state
can lie below 1.

16

## PDF page 17

4.3

Regeneration and invariant occupation

Call an odd state with s ≤ 3 a regenerating state; regeneration is viewed as occurring just
before its next draw. Its outgoing law is independent of s, since ϕo (s) = A and mo (s) = 2.
Lemma 4.3 (Regeneration). The time to first regeneration has an exponential moment
uniformly over (4.19). The cycles strictly after one regeneration through the next inclusive
are iid. Their lengths τ have a finite exponential moment. Their total log decrements
G=

τ
∑

g(sj )

j=1

are positive, nonarithmetic, and have a finite exponential moment for some positive parameter.
In particular 0 < EG < ∞. Each complete cycle satisfies G ≥ g(3) = log(4/3).
Proof. For sufficiently large current s, the excess of the next state over s − 1 has tail
P(snext ≥ s − 1 + h | i, s) =

ϕi (s + h)
ϕi (s)

(h ≥ 0).

Here the support minimum is s − 1 for either type, and the identity follows from (4.11).
Lemma 4.2 makes this tail at most e−λh , with any fixed large λ, outside a sufficiently large
compact. Thus V (i, s) = es satisfies
E(V (inext , snext ) | i, s) ≤ κV (i, s) + C,

κ < 1,

and the constant term can be omitted outside a larger compact. On the compact, finiteness
and uniform boundedness of the expectation follow from the superexponential tails of the
weights.
Choose a compact set C0 and α > 1 such that E(Vnext | i, s) ≤ V (i, s)/α outside C0 .
Stopping the nonnegative supermartingale αn∧σ V (in∧σ , sn∧σ ), where σ is the first entrance
to C0 , gives
Ei,s ασ ≤ V (i, s)
for starts outside C0 , by Fatou’s lemma. In particular the entrance time is almost surely
finite.
From C0 there are an integer m and a probability p > 0 such that regeneration is reached
within m steps with probability at least p, uniformly in the starting state. To see this,
whenever s > 3 choose the next state in the interval of width 1/4 immediately above its
support minimum; this lowers the state by at least 3/4. An even state with s ≤ 3 then draws
into the regenerating odd range on the same choice. All prescribed intervals lie in a fixed
compact and have uniformly positive transition probabilities.
Run such an m-step attempt, and on failure wait for the next entrance to C0 before
retrying. Let D be the duration of one failed attempt together with this return. The stopped
estimate and the uniform bound on the V -moment after the m attempted steps show that,
for some α1 > 1,
sup Ei,s [α1D 1{failure} ] < ∞.
(i,s)∈C0

For 0 < θ < 1, Hölder’s inequality bounds the same expression with α1θ by
)θ

(

sup E[α1D 1{failure} ]
C0

17

(1 − p)1−θ .

## PDF page 18

For sufficiently small θ > 0 this is less than 1. Summing over successive failed attempts proves
an exponential moment for the hitting time of regeneration from C0 , and then from (4.19).
The same reasoning applies to a return after a regenerating start: its outgoing common draw
has a bounded V -moment.
The common outgoing law proves independence and identical distribution of the complete
cycles. During a cycle all odd states are at least 1, and all even states are at least 2, so each
g(sj ) ≤ log 2. Thus the exponential moment of τ supplies an exponential moment of G for a
sufficiently small parameter. The terminal odd state lies in [1, 3], so its last decrement alone
is at least g(3) > 0.
For nonarithmeticity, consider a two-step return whose even state t lies in a fixed subinterval
of (2, 3) and whose next odd state u lies strictly between t−1 and 3. There is a two-dimensional
region of such pairs on which the joint density is positive. On that region G = g(t) + g(u)
varies continuously and has a nonzero derivative in u. Its distribution therefore has a nonzero
absolutely continuous component, and cannot be supported on an arithmetic lattice.
Lemma 4.4 (Invariant densities and cycle occupation). On the ordinary even and odd state
spaces, respectively, the finite raw invariant densities are
πe (s) = ϕe (s)

πo (s) = (1 − s−2 )ϕo (s)

(s ≥ 2),

Put

∫ 3

β=

πo (s) ds =
1

(s ≥ 1).

(4.20)

4A
.
3

For every nonnegative measurable state function Q,
E

τ
∑

Q(ij , sj ) =

j=1

1∑
β i

∫

Q(i, s)πi (s) ds.

(4.21)

In particular, if
Mg =

∑∫

πi (s)g(s) ds,

i

then EG = Mg /β, and

0 < Mg ≤ 4eγ .

(4.22)

Proof. For a new even state t ≥ 2, cancellation of the old derivative weight in the incoming
integral gives
∫ t+1
t2
(1 − s−2 ) ds =
.
t+1
1
Multiplication
by W0 (t)ϕe (t) yields πe (t). For a new odd state t ≥ 1, the corresponding
∫ t+1
integral is 2 ds = t − 1, which yields (1 − t−2 )ϕo (t). These identities prove invariance.
Finiteness follows from (4.12). On [1, 3], ϕo = A, so β = A[s + s−1 ]31 = 4A/3.
For completeness,
normalize the raw measure to a stationary probability measure µ = π/M ,
∑ ∫
where M = i πi . Start the chain with law µ. For a bounded measurable state function Q,
partition Q(in , sn ) according to the last regenerating time strictly before n. If it is n − k,
1 ≤ k ≤ n, the common outgoing law shows that this term has expectation
µ(regenerating states) E[Q(ik , sk )1{τ ≥k} ],
where the expectation on the right starts just after a regeneration. The remaining event
is that there was no regenerating time among 0, . . . , n − 1; its probability tends to zero by
Lemma 4.3 and dominated convergence over µ. Stationarity and then n → ∞ give
µ(Q) =

τ
∑
β
E
Q(ij , sj ).
M j=1

18

## PDF page 19

This proves (4.21) for bounded nonnegative Q, and truncation proves it in general. The
argument does not require an aperiodic discrete-time chain; the alternating types cause no
difficulty.
Since g(s) ≤ 1/s, (4.13) gives
Mg ≤

∫ ∞

∫ ∞

a(s) ds + 2

∫ ∞

c(s) ds +

2

1

a(s) ds.
0

The future integrals at s = 2 give 1∞ c = 2 and 1∞ a = A − 2. As a = 1 on [0, 2], the three
displayed contributions are A − 3, 4, A − 1. Their sum is 2A = 4eγ . Strict positivity is
immediate from the positive even density and g > 0. Taking Q(i, s) = g(s) in (4.21) identifies
EG.
∫

4.4

∫

Renewal limits and uniform band estimates

We use tests in the log-gap coordinate u = log r. An admissible compact test Fi (u, s) is
bounded and continuous on the extended state ranges, with support in a fixed compact
rectangle in (u, s). We also permit multiplication by indicators of fixed intervals in u or
s, and by 1{s<eu /ℓ} , where ℓ = 1 or 2. At the lower state endpoints one may first make a
continuous one-sided extension to the extended range and then apply the indicator. Finite
linear combinations of these tests are permitted. In particular, a continuous bounded test
supported in a compact positive r-window and restricted by s < r/ℓ is covered: the restriction
itself bounds s.
Proposition 4.5 (Compact occupation limit). For an admissible compact test and starts
satisfying (4.19),
lim Esin

v→∞

∑

1 ∑
Mg i R

∫ ∫

Fin (v − Tn , sn ) =

n≥0

Fi (u, s)πi (s) ds du.

(4.23)

The convergence is uniform in sin ∈ [1.99, 2.3]. The state integrals on the right use the
ordinary invariant ranges in (4.20).
Proof. First start immediately before the outgoing draw of a regeneration, and exclude that
∑
starting state from the sum. Write a complete cycle as (ij , sj )1≤j≤τ , and set Sj = jk=1 g(sk )
within the cycle. Its response to the test is
H0 (v) = E

τ
∑

Fij (v − Sj , sj ).

(4.24)

j=1

If the log-gap support of the test is contained in [a, b], then H0 (v) = 0 for v < a, since Sj ≥ 0.
Also Sj ≤ j log 2, so for v > b,
[

]

|H0 (v)| ≤ ∥F ∥∞ E τ 1{τ ≥(v−b)/ log 2} .
The exponential moment in Lemma 4.3 gives an exponentially decreasing upper bound as
v → ∞.
The function H0 is continuous, including for the permitted indicator tests. To verify this,
condition on the history before the j-th draw and on the event j ≤ τ , which is determined
before that draw. The next state t = sj has a density. Writing D = ev−Sj−1 > 0, its gap is
ev−Sj =

19

Dt
.
t+1

## PDF page 20

Equality at a fixed positive gap edge therefore specifies at most one value of t; equality at a
fixed state edge does likewise. For the arrival boundary,
t = ev−Sj /ℓ

⇐⇒

t + 1 = D/ℓ.

Thus each boundary has conditional probability zero. For any fixed number of cycle steps
dominated convergence gives continuity. The remaining steps are uniformly bounded in expectation by ∥F ∥∞ E[τ 1{τ >N } ], which tends to zero. This proves continuity of H0 . Continuity,
the vanishing left tail, and the exponential right envelope show that H0 is directly Riemann
integrable.
Let UG be the renewal measure of successive complete-cycle decrements, including the
boundary at zero:
∑
UG =
L(G1 + · · · + Gk ).
k≥0

The expectation of the complete future test from a regeneration is
∫

RF (v) =

H0 (v − y) UG (dy).

(4.25)

[0,∞)

By Lemma 4.3, G is nonarithmetic and has finite positive mean. The key renewal theorem
(2.4) therefore gives
∫
1
H0 (u) du.
RF (v) −→
EG R
Fubini is justified by the bounded test, its compact log-gap support, and Eτ < ∞. Translating
the log-gap integral within each cycle and applying (4.21) gives
τ
∑∫

1∑
H0 (u) du = E
Fij (u, sj ) du =
β i
R
j=1 R

∫

∫∫

Fi (u, s)πi (s) ds du.

Since EG = Mg /β, this is the limit in (4.23).
We record a boundedness fact needed to restore the initial segment. Every complete
cycle has decrement at least g(3) > 0. Consequently any interval of fixed length contains a
bounded number of cycle boundaries on each sample path, and
⌊

sup UG ([y, y + h]) ≤ 1 +
y∈R

h
g(3)

⌋

(h > 0).

(4.26)

The compact bound and the exponential envelope for H0 , summed over unit intervals, show
from (4.25) that supv |RF (v)| < ∞.
Now let τ0 be the first regenerating time from an allowed even start, and D0 = Tτ0 . All
initial per-step decrements are bounded by c∗ = log(1 + 1/0.98). Lemma 4.3 gives a uniform
exponential moment for τ0 , hence a uniformly tight, indeed exponentially bounded, family
of D0 ’s. The portion of the test through time τ0 tends to zero uniformly as v → ∞: a
contribution requires c∗ τ0 ≥ v − b, and its absolute size is at most ∥F ∥∞ (τ0 + 1). Conditional
on the initial history, the future after that state has expectation RF (v − D0 ). It is the same
function RF for every history, because the outgoing regenerating law is common. For a fixed
M , convergence of RF (y) as y → ∞ is uniform over y = v − d, 0 ≤ d ≤ M . Uniform tightness
of D0 and boundedness of RF then give the claimed uniform limit.
Lemma 4.6 (Uniform band bounds). For every fixed h > 0 there is Ch < ∞ with the
following properties. For any nonnegative measurable state function Q and any v ∈ R, a
regenerating start satisfies
E

∑

Q(in , sn )1{Tn ∈[v,v+h]} ≤ Ch

∑∫
i

n≥1

20

Q(i, s)πi (s) ds.

(4.27)

## PDF page 21

From an even start in (4.19), the same bound holds for the sum over n ≥ 2, uniformly in the
starting ratio. The density of the first odd state is at most
C 1{s≥0.98} ϕo (s).
In particular, uniformly in rin > 0, R > 0, and ℓ ∈ {1, 2},
E

∑ 1{R≤rn ≤eR, sn <rn /ℓ}

ϕin (sn )

n≥1

≪ R + 1.

(4.28)

Including the starting state in the last sum changes its bound by at most an absolute constant.
Proof. For a regenerating start, condition on the internal states and decrements of one fresh
cycle. Its beginning is a renewal boundary independent of that cycle. Tonelli’s theorem gives
E

∑

Q(in , sn )1{Tn ∈[v,v+h]} = E

τ
∑

Q(ij , sj )UG ([v − Sj , v + h − Sj ]).

j=1

n≥1

Apply (4.26) and then (4.21). This argument permits arbitrary nonnegative Q: it never
assumes independence of a state’s value and its internal decrement.
We next compare the initial even start to regeneration. If its ratio is s0 , the density after
two draws, on t ≥ 2, is
∫
W0 (t)ϕe (t) t+1
ps0 ,2 (t) =
W0 (u) du.
(4.29)
ϕe (s0 )
s0 −1
Starting at regeneration, the density after three draws is
W0 (t)ϕe (t)
preg,3 (t) =
A

∫ u+1

∫ t+1

W0 (y) dy du

W0 (u)

(t ≥ 2).

(4.30)

2

1

These formulas follow by canceling the intermediate derivative
weights in the successive
∫
kernels. For u ≥ 2, the inner integral in (4.30) is at least 23 W0 (y) dy > 0. Since t + 1 ≥ 3, it
follows that
∫ t+1

∫ u+1

W0 (u)
1

2

W0 (y) dy du ≫

∫ t+1

W0 (u) du ≫

2

∫ t+1
s0 −1

W0 (u) du,

uniformly for s0 ∈ [1.99, 2.3]. The
last comparison uses the bounded integral over [0.99, 2] and
∫ t+1
the positive lower bound for 2 W0 . The starting denominator ϕe (s0 ) also has a positive
compact lower bound. Thus
ps0 ,2 (t) ≤ Cpreg,3 (t)

(t ≥ 2).

(4.31)

To use this marginal comparison, the correlated elapsed decrement must be removed
explicitly. Let I = [v, v + h], C2 = 2c∗ , and C3 = 3 log 2. The initial two decrements sum to
at most C2 , so an event in I at time n ≥ 2 has, measured from state 2, a future decrement in
I2 = [v − C2 , v + h].
Condition on that state, discard the initial decrement by this enlargement, and apply (4.31).
For a path started at regeneration, its first three decrements sum to at most C3 ; a future
decrement in I2 measured from state 3 therefore gives a total decrement in
[v − C2 , v + h + C3 ].

21

## PDF page 22

The resulting expectation is bounded by a constant times the regenerating occupation sum
in this enlarged band, which is covered by (4.27). This proves the bound from even starts,
including their state at time 2, without imposing independence on the initial state and elapsed
decrement.
At step 1, the density is
W0 (s)ϕo (s)
1{s≥s0 −1} .
ϕe (s0 )
Both W0 (s) for s ≥ 0.99 and 1/ϕe (s0 ) on the allowed starts are bounded. This proves the
asserted first-step estimate.
The condition R ≤ rn ≤ eR is a band of length 1 in Tn . For n ≥ 2, use the preceding
result with
1{s<eR/ℓ}
Q(i, s) =
.
ϕi (s)
The ratios of invariant to derivative densities are 1 for the even states and 1 − s−2 ≤ 1 for
the odd states. Their integrals up to eR/ℓ are O(R + 1). The first-step density gives the
same bound by direct integration. Finally ϕe (s0 ) has a positive compact lower bound, so the
starting state’s possible contribution is O(1).
Remark 4.7. Two consequences explain the later weight scales. At an arrival with xn > ℓ and
rn ≤ K, (4.18) confines the state to a fixed compact with a positive lower endpoint. Hence
rn2 /ϕin (sn ) is bounded. Moreover, each such transition decreases the gap by more than ℓ;
there are only OK (1) such compact arrivals on one path. Formula (4.17) therefore bounds
−2
the total original harmonic weight of compact prefixes by OK (rin
). If the counted prefixes
−2
can occur only on an event A of the tilted path, the bound is OK (rin
)P(A).
Retain the restriction xn > ℓ, equivalently sn < rn /ℓ, in the following tail estimate. After
2 /ϕ (s ), a reward e−cr in original harmonic weight is r 2 e−cr /ϕ (s) in
multiplication by rin
e in
i
tilted weight. Summing (4.28) over the bands [R, eR], R ≥ K, gives a convergent upper
bound whose tail tends to zero as K → ∞, uniformly in the allowed starts. These statements
also cover a fixed bounded factor in the reward.

4.5

Visits in a prescribed even-state window

Lemma 4.8 (Marked visits). Fix b0 > 0 and ε > 0. There is a constant Cε > 10, independent
of b0 , such that, whenever b1 ≥ Cε b0 is fixed, the following event has probability at least
1 − ε − o(1) as rin → ∞, uniformly in (4.19). At a regenerating odd state with pre-draw gap
in [10b0 , b1 ], the next draw is an even arrival satisfying
s ∈ [2.08, 2.14],

x ∈ [2b0 , b1 /2].

The proof yields the smaller ratio interval [2.09, 2.13]; thus the stated ratio window has positive
slack. The arriving gap exceeds 6b0 , so, if 6b0 > K, such a visit precedes every subsequent
arrival of gap at most K.
Proof. Mark a complete regeneration cycle if its first draw lies in [2.09, 2.13]. The common
outgoing kernel gives a fixed probability
1
p=
A

∫ 2.13

W0 (t)ϕe (t) dt ∈ (0, 1).

2.09

The complete cycle objects, consisting of their state sequences and their decrements, are
iid. Consequently the spacings W between successive marked cycle beginnings are iid: each
consists of one cycle conditioned on being marked, followed by a geometric number of cycles
22

## PDF page 23

conditioned on being unmarked. More explicitly, the number N of intervening unmarked
cycles has P(N = m) = (1 − p)m p, m ≥ 0; conditional on these marks, the cycle objects
are independent with their respective conditional laws. The next marked cycle is excluded
from the preceding spacing and begins the next such block. This proves independence of the
spacings, even though a mark depends on its own cycle. It also gives
EW = E(G | marked) +

1−p
EG
E(G | unmarked) =
< ∞.
p
p

Furthermore W ≥ g(3) > 0.
From an allowed initial start, the delay D to the first marked beginning consists of the
initial segment to regeneration and a geometric number of unmarked complete cycles. The
first segment has uniformly bounded mean by Lemma 4.3; the latter sum has finite mean
by the preceding conditional-cycle description. Thus D is uniformly tight over the allowed
initial states. The spacings after that beginning are independent of the delay.
We give the required wide-interval bound using only EW < ∞. Let UW be the renewal
measure for the marked spacings, with an initial renewal at zero. The lower bound on W
gives a uniform bound C for its mass in any interval of length one. For q ≥ 0, if there is
no marked renewal in [q, q + H], some renewal at or before q has its next spacing overshoot
q + H. Independence of a renewal time and its next spacing therefore gives
P(no renewal in [q, q + H]) ≤

∫
[0,q]

P(W > q + H − t) UW (dt) ≤ C

∑

P(W > H + j).

j≥0

Changing one endpoint in the unit-interval partition only changes the harmless absolute
constant or shifts H by 1. The last quantity tends to zero as H → ∞, since W has finite
mean. It is uniform in q. For the delayed process, condition on D ≤ v and apply the same
bound with q = v − D. The additional error P(D > v) tends uniformly to zero as v → ∞.
Apply this with
(
)
v = log(rin /b1 ),
H = log b1 /(10b0 ) .
Choose H sufficiently large in terms of ε, equivalently choose b1 /b0 sufficiently large, and
then let rin → ∞. A marked beginning in this log-decrement interval has pre-draw gap
r ∈ [10b0 , b1 ]. For its marked draw t ∈ [2.09, 2.13],
10b0
r
b1
≤x=
≤
.
3.13
t+1
3.09
This lies inside [2b0 , b1 /2], and the arriving ratio is t. The new gap satisfies
r′ =

rt
2.09
≥ 10b0
> 6b0 .
t+1
3.09

Gaps strictly decrease along the path, so the last assertion follows.

5

Passage from harmonic paths to primes

We now transfer the path estimates to actual primes. Throughout this section, a standard
prime path starts at a lower state with cutoff B and gap rst = sst B, where sst ∈ [1.99, 2.3]. Its
primes decrease strictly after the first step. At the first step the upper endpoint is included;
all subsequent upper endpoints are excluded. The next exponent is required to exceed ℓ,
where ℓ ∈ {1, 2}. A lower state includes every available child, and an upper state includes
precisely the children for which r − x ≥ 2x. Thus these paths contain the paths admitted by
(3.3), and agree with them above exponent 2.
23

## PDF page 24

For a prefix p = (p1 , . . . , pm ) write
h(p) =

m
∏
1
j=1

pj

r(p) = rst −

,

m
∑

x(pj ),

s(p) =

j=1

r(p)
.
x(pm )

The empty prefix has weight 1. Sums over prefixes below include all allowed lengths, and
therefore count a path once at each of its visited states. At a nonempty prefix, x(pm ) > ℓ is
equivalent to s(p) < r(p)/ℓ.
We use the elementary consequences of (1.2)
S = (log B)2 ,

N = O(S log B) = O((log B)3 ).
(5.1)
√
In particular, every fixed power of S and N is smaller than exp(c log w) for every fixed
c > 0, eventually.
log w ∼ log B,

Lemma 5.1 (Harmonic prime measure). There are absolute positive constants C, c such that,
on any exponent interval with lower endpoint u ≥ 1/2,
1
=
p
x(p) in the interval
∑

dx
+ O(E(u)),
interval x

∫

√

E(u) = C exp(−c u log w).

(5.2)

The error is uniform in the upper endpoint and in either endpoint convention. In particular,
the total weight of all decreasing prime prefixes with exponents in (ℓ, B], with no admission
restrictions, is O(B).
Proof. Apply partial summation to the prime∫ number theorem
in Lemma 2.2, between wu
∫
and the upper endpoint. The main term is dt/(t log t) = dx/x. The √
integrated error,
including its lower-endpoint term, is bounded by a constant times exp(−c log(wu )), after
reducing c. The bound remains valid if the upper endpoint is sent to infinity in the error
integral. A change of endpoint convention contributes at most one reciprocal prime, which is
absorbed by E(u). Finally,

∑
p

h(p) =

∏

(1 + 1/p) ≤ exp 

wℓ <p≤wB



∑
wℓ <p≤w

1
≪ B.
p
B

Deleting an endpoint prime or imposing admission restrictions can only decrease this sum.
Lemma 5.2 (Removal of high states). Fix K > 0 and A > 0. The total original harmonic
weight of prefixes ending at gap at most K and having some earlier or terminal ratio greater
than S is OK,A (B −A ). More generally, for any fixed c′ > 0, the sum of h(p) exp(−c′ r(p)) over
prefixes having such a high state is OA,c′ (B −A ). Both conclusions also hold in the continuous
harmonic model, uniformly in the starting ratios under consideration.
Proof. Suppose a prefix reaches a state of gap R, cutoff b, and ratio R/b > S. Every
subsequent factor has exponent at most b. Reducing the gap below R/2 therefore requires
at least S/2 additional factors. If T = log B + O(1) is an upper bound for the remaining
harmonic intensity, the sum of weights of these continuations is at most
∑ Tj
j≥S/2

j!

.

Since S = (log B)2 , this tail is smaller than every fixed negative power of B, even after
multiplication by B. To sum over all possible high ancestors, use Lemma 5.1: their total
24

## PDF page 25

prefix weight is O(B). This argument is an upper bound even when it counts a terminal
prefix more than once.
At a high ancestor R > Sb > Sℓ. Thus a prefix ending at fixed gap K must reduce this
gap by more than half for all sufficiently large B. For the weighted assertion, prefixes which
do not do so have terminal gap greater than Sℓ/2, and their reward is O(exp(−c′ Sℓ/2)).
Their total unweighted prefix mass is O(B), so they too contribute less than every B −A . In
the continuous model, the ordered integrals of length j are bounded by T j /j!, and their total
is eT ≪ B; the proof is unchanged.
For the rest of the discrete approximation, retain only states of ratio at most S. There are
at most N = CS log B arrived-at states, with a fixed sufficiently large C. Indeed a transition
to ratio t ≤ S decreases log r by g(t) = log(1 + 1/t) ≫ 1/S. Moreover the gap at a retained
nonempty state is bounded below by 0.99ℓ, and the starting gap is O(B). This also proves
the same deterministic horizon for a continuous path up to its first exit from these conditions.
Proposition 5.3 (Coupling the tilted paths). Choose sufficiently small absolute positive
constants in the following order. For a permitted prime child of a state of type i, ratio s, and
gap r, put t = r/x(p) − 1 and give that child mass
1
q(p | r, s, i) =
p

(

t+1
t

)2

ϕi′ (t)
.
ϕi (s)

(5.3)

√
Only children with x(p) > ℓ and t ≤ S are retained. For ϵw = exp(−c2 log w) their total
mass is at most 1 + ϵw . Dividing by 1 + ϵw and assigning the remaining mass to a cemetery
state defines a killed Markov chain.
This chain can be coupled with the continuous chain (4.16), killed
√ at the first draw with
x ≤ ℓ or t > S, so that the probability of failure is at most exp(−c3 log w). On success the
chains have the same number of arrived-at states and matching exits. At corresponding states,
|s − s̃| ≤ h,

∣
∣
∣
∣
∣log r ∣ ≤ CN h,
∣
r̃ ∣

h=

1
√

⌈exp(c4 log w)⌉

.

(5.4)

All statements are uniform in sst ∈ [1.99, 2.3] and in the endpoint conventions stated above.
For a length-m retained prefix, if Pw (p) denotes its probability in the killed chain, then the
exact weight identity is
h(p) = Pw (p)(1 + ϵw )

m

(

r(p)
rst

)2

ϕe (sst )
,
ϕi (s(p))

(1 + ϵw )m = 1 + o(1).

(5.5)

Proof. Under t = r/x − 1 we have |dx/x| = dt/(t + 1). Multiplying by the non-prime part of
(5.3) gives W0 (t)ϕi′ (t)/ϕi (s), exactly the continuous transition density. Also rchild /r = t/(t+1),
so multiplication over a prefix telescopes and proves (5.5). The last assertion there follows
from m ≤ N and (5.1).
Partition the ratio axis into bins [jh, (j + 1)h). For a bin meeting the allowed next
range, temporarily extend it to the full bin when seeking an upper bound. Its corresponding
x-interval has logarithmic width comparable to h/(t + 1) and lower endpoint at least ℓ/2, for
sufficiently large w. Lemma 4.2 bounds logarithmic derivatives of the weights and backward
opposite weight ratios by fixed polynomials in S. Therefore a full interior bin has discrete
mass equal to its continuous mass with relative error
E(1/2)
O poly(S) h +
h
(

(

))

.

(5.6)

Here the first term controls variation across the bin, and the second is (5.2) divided by its
harmonic main mass. The density itself is bounded by poly(S) on any bin meeting the
25

## PDF page 26

support. There are only a bounded number of partial support bins, each with mass at most
poly(S)h. The fixed even-child boundary 2 is a mesh endpoint. Summing the interior relative
errors and the partial bin upper bounds proves that the total mass is at most 1 + ϵw , after
choosing c4 and then c2 sufficiently small.
Suppose the chains have been matched through the previous draw. Their lower support
endpoints are s − 1 or max(2, s − 1), and consequently differ by at most h. The upper
endpoint imposed by x > ℓ is r/ℓ − 1. It needs comparison only when it is at most S, up to a
mesh error; in that case r = O(S + 1), and its discrepancy is at most O((S + 1)N h). Thus a
large starting gap does not enter this support error. Ratios of the two density denominators
are 1 + O(poly(S)h). The total mass in mismatched or partial bins, together with the total
variation distance between full bin
√ labels and the discrepancy in exit probabilities after
normalization, is at most exp(−c′ log w).
Maximally couple these bin labels and the cemetery label at each step. Inside a matched
nonexit bin the two next ratios differ by at most h. Since g ′ (t) = −1/(t(t + 1)) is bounded
on the used ranges, each matched step changes the logarithmic-gap discrepancy by O(h).
Iteration up to N steps gives (5.4); a union bound and (5.1) give the stated failure probability.
Single endpoint primes have already been included in the uniform estimate (5.2). The initial
lower ratios slightly below 2 are covered by the extended derivative-weight identities in
Lemma 4.2.
The total variation coupling by itself is insufficient for rewards containing 1/ϕi (s) far out
in the ratio tail. The following pointwise majorants supply the required additional control.
Lemma 5.4 (Discrete marginal majorants). For the killed chain of Proposition 5.3, the
probability of a nonexit bin with left endpoint t at step 2 ≤ n ≤ N is bounded, with an absolute
constant, by

Chϕe (t),
n even,
(5.7)
(
)

Chϕo (t) 1 − t−2 + 3hW0 (t) , n odd.
At step 1 the bound is ChW0 (t)ϕo (t), on the slightly extended range t ≥ 0.98. The constants
are uniform in the starting ratios and in w sufficiently large.
Proof. The bin argument in the preceding proof gives the conditional upper bound
(1 + δw )hW0 (t)

ϕi′ (t)
,
ϕi (s)

δw = exp(−c′ log w),
√

(5.8)

for every feasible child bin. Division by 1 + ϵw cannot increase it. The first-step assertion
follows because the starting denominator is bounded away from zero. At the second step,
canceling the intermediate derivative weight leaves an incoming sum bounded by
C

∑

hW0 (u) ≪ log(t + 2).

sst −1≤u≤t+1+h

Since t ≥ 2 and W0 (t) log(t + 2) is bounded, this proves the even majorant at step 2.
For the induction, replacing a weight at an actual state by its value at the bin’s left
endpoint costs a relative 1 + O(poly(S)h). Given the even majorant, the incoming bins for
an odd child of left endpoint t start at 2 and end at most at t + 1 + h. Their total mesh
length is at most t − 1 + 3h. Multiplication by W0 (t) gives
W0 (t)(t − 1 + 3h) = 1 − t−2 + 3hW0 (t),

26

## PDF page 27

as required. In the reverse direction, the incoming odd bins start at 1; their bracket sums
satisfy
∑

(

h 1−u

−2

)

+ 3hW0 (u) ≤

∫ t+1

(1 − u−2 ) du + O(h log(t + 2))

1

1≤u≤t+1+h

=

t2
+ O(h log(t + 2)).
t+1

The new factor W0 (t) cancels the leading expression, and the error is O(h) for t ≥ 2. The
points 1 and 2 are mesh aligned, and the 3hW0 term covers the endpoint mesh interval
where the stationary odd factor vanishes. Each iteration enlarges the constant by at most
1 + O(δw + poly(S)h). Its product over N steps is 1 + o(1) by (5.1), completing the proof.
Proposition 5.5 (Prime occupation estimates). The following assertions hold uniformly for
sst ∈ [1.99, 2.3] and ℓ ∈ {1, 2}.
(i) For fixed K, the original harmonic mass of prefixes with terminal gap at most K is
OK (B −2 ).
(ii) Consider any selection of such compact-ending prefixes whose low-state histories imply
an event A in the killed prime chain. Their total weight is at most
CK B −2 Pw (A) + OK,A (B −A )

(5.9)

for every fixed A > 0. One may take A to be the event that at least one selected compact
prefix occurs.
(iii) For every fixed c′ > 0,
∑

lim lim sup B 2

K→∞ w→∞

′

h(p)e−c r(p) = 0.

(5.10)

p standard
r(p)>K

The same compact and tail assertions hold for continuous original harmonic weights.
(iv) Let Hi (r, s) be bounded continuous functions supported in a fixed compact positive gap
interval and a fixed compact ratio interval. Fixed interval boundaries and the indicator
s < r/ℓ are also permitted, with one-sided continuous extension before imposing that
indicator, as in Proposition 4.5. Then
2
∑
rst
h(p)Hi(p) (r(p), s(p))
ϕe (sst ) p

−→

∞
1 ∑
Mg i∈{e,o} 0

∫

∫

r2 πi (s)
dr
Hi (r, s)1s<r/ℓ ds ,
ϕi (s)
r

(5.11)

where the inner domains are s ≥ 2 for i = e and s ≥ 1 for i = o. The convergence is
uniform in the starting ratios.
Proof. Remove high-state histories by Lemma 5.2. On a remaining compact-ending prefix,
s < r/ℓ bounds the terminal ratio in a fixed compact set. The positive weights ϕi are bounded
away from zero there, so (5.5) is at most CK B −2 Pw (p). A path has at most CK visits with
gap at most K, since each exponent exceeds ℓ and thus each step decreases the gap by more
than ℓ. Summing proves (i) and (5.9). This also explains why a history exception costs its

27

## PDF page 28

tilted probability times B −2 , rather than its probability times the unrestricted original mass
O(B).
For (iii), the scaled reward after the change of measure is at most
′

r2 e−c r
C
.
ϕi (s)

(5.12)

Put KB = C ′ log log B. At a step covered by Lemma 5.4, sum first over ratio bins. Since
r > ℓs and ℓ ≥ 1, cancellation of ϕi bounds the expected reward from r > KB by a constant
times
∑
′
′
h
sup
u2 e−c u ≪ (1 + KB )3 e−c KB .
(5.13)
t=jh≥0.97

u≥max(t,KB )

Increasing C ′ makes this o(N −1 ). The first-step majorant gives the same bound, because W0
′′
is bounded on its extended range. The empty prefix contributes O(B 2 e−c B ).
On K < r ≤ KB , the Dickman lower bounds in Lemma 4.2 bound (5.12) by
exp(O(KB log(KB + 2))). Even after multiplication by N , the coupling failure contribution
is negligible, since
√
log N + O(KB log(KB + 2)) = o( log w).
On a successful coupling, the reward is bounded by
′

r̃2 e−c r̃/2
,
C
ϕi (s̃)

r̃ > K/2,

s̃ < r̃/ℓ.

Here the indicator follows from matching the nonexit arrivals, and the comparison of weights
follows from their logarithmic derivative bounds and (5.4). On a band R ≤ r̃ ≤ eR, Lemma 4.6
bounds the expected sum after cancellation of ϕi by O(R + 1). Thus this band contributes
′
at most C(R + 1)R2 e−c R/2 . Summing the geometric sequence of bands above K/2 proves
(5.10). High-state histories were already negligible by Lemma 5.2. The continuous proof uses
the same band bound directly, along with the continuous version of that lemma.
Finally, for (iv) use (5.5) with the compact test r2 Hi (r, s)/ϕi (s). The correcting factor is
uniformly 1 + o(1), and the number of compact-gap visits is bounded. Coupling therefore
transfers this test by uniform continuity. Boundary indicators cause no difficulty: the limiting
continuous occupation measure gives zero mass to their boundaries, and continuous upper
and lower approximations suffice. Continuous removal of high states is harmless as well. For
example, the drift estimate in Lemma 4.3 gives a uniformly bounded exponential moment of
the ratio at each step, so a union bound up to the low-state horizon gives O(N e−S ) = o(1)
for reaching a high state before exit. Alternatively one can use the continuous original-weight
conclusion of Lemma 5.2 on compacts. Apply Proposition 4.5 to the transferred test and use
its uniformity in the starting state. This gives (5.11) and completes the proof.

6

Evaluation of the reference tree

We now evaluate the boundary contribution left open by the continuous benchmark in
Section 4. Above exponent 2, the reference tree follows the standard admission rule. At cutoff
2, its remaining finite polynomial differs from the linear-sieve benchmark. The occupation
estimates of Section 5 transport this boundary discrepancy to the root, where it contributes
at scale B −2 .
The sign requires a separate calculation. We first compare with the full product over
the boundary exponents, whose signed contribution can be evaluated exactly. The stronger
admission rule below exponent 2 omits lower children and reduces this contribution. Expanding
28

## PDF page 29

at the first omitted child will bound the loss and leave enough positive mass to overcome the
root’s negative benchmark. The resulting lower bound is Proposition 6.3. We also obtain a
local reference estimate for the later stopped-subtree comparison.
We begin by replacing the continuous factor 1/b in the benchmark by the corresponding
prime product and controlling the resulting quadrature error. After this error is removed,
only the cutoff-2 discrepancy remains to be evaluated.
For an available cutoff b, let V (b) be the product of 1 − 1/p over the available primes
greater than w. The root cutoff includes its upper endpoint, whereas a cutoff at a previously
chosen prime excludes that prime. Write Vx for the latter product when the new prime has
exponent x. The auxiliary cutoff 2 includes the boundary primes w < p ≤ w2 . Mertens’
theorem and Lemma 5.1 give
V (b) =

)
Cw (
1 + O(E(b)) ,
b

Cw =

e−γ
−→ 1
log w V0

(b ≥ 2).

(6.1)

The formula is uniform in these endpoint conventions: excluding an endpoint prime changes
the product by 1 + O(1/p), an error absorbed by E(b).
With fe = f and fo = F as before, benchmark a state by V (b)fi (r/b). The extension of f
below 2 is used only at a starting lower state, as in Section 4. An omitted lower child always
has benchmark zero, including when its formal ratio is below the domain of the ordinary
sieve functions.

6.1

The quadrature error above the boundary

Define gi = fi − 1, with the starting extension just described, and set ge (t) = −1 whenever
the prospective lower child is omitted. At a state with cutoff b > 2, subtracting constants by
the identity
∑ Vx(p)
V (b) = V (2) −
p
2<x(p)≤b
(with the actual upper endpoint convention) gives the residual
(w)

Ri (r, b) = V (2)gi (r/2) − V (b)gi (r/b) −

Vx(p)
gi′ (r/x(p) − 1).
p
2<x(p)≤b
∑

(6.2)

The sum here includes the omitted children with their deviation −1; they are not included in
any subsequent path propagation. This convention accounts exactly for the constants of the
omitted terms.
The continuous analogue of (6.2), obtained by replacing V by Cw divided by its exponent
and the prime measure by dx/x, is zero. Subtracting the constant part from (4.2), with the
same starting extension and zero benchmark at omitted children, gives
d
db

(

gi (r/b)
b

)

=−

gi′ (r/b − 1)
.
b2

(6.3)

Integrating this identity from 2 to b proves the cancellation.
Lemma 6.1 (Summed quadrature residual). Along the standard prime paths with x > 2
from the root,
∣
∣
∑
∣ (w)
∣
h(p) ∣Ri(p) (r(p), b(p))∣ = o(B −2 ).
(6.4)
p

The same assertion is uniform for lower starting ratios in [1.99, 2.3] and starting cutoffs B
tending to infinity with the parameters of (1.2).
29

## PDF page 30

Proof. The absolute next deviation in (6.2) is nondecreasing as a function of x. Thus partial
summation on an exponent interval with lower endpoint u ≥ 2 bounds the error in replacing
∑ 1 gi′ (r/x(p) − 1)

p

x(p)

∫

by

gi′ (r/x − 1)
dx
x2

by O(E(u)D/u), where D is the maximum absolute next deviation on that interval. To justify
the variation bound despite the additional factor 1/x, use the product-variation inequality: the
total variation is at most a constant times D/u. By (6.1), replacing the products introduces
endpoint errors of the same kind and a sum error at most O((log B)E(u)D). These estimates
apply to subintervals as well, and their continuous contributions cancel by (6.3).
At a state of ratio s, all the absolute parent, boundary, and next deviations under
discussion are O(ϕi (s)). For example,
a(s) ≤ ϕe (s)/s,

c(s − 1) ≤ ϕe (s)/s,

and the analogous inequalities follow from ϕo (s) = s(c(s) + a(s − 1)) on its normal range.
Monotonicity bounds the later arguments by these earliest ones. The bounded extensions at
the initial states obey the same inequalities with an absolute constant. An omitted lower
deviation is just 1 in absolute value, which occurs where the relevant upper derivative weight
is bounded away from zero.
First restrict to histories with all ratios at most S = (log B)2 . If b ≤ (log B)4 , then
r ≤ (log B)6 , and the preceding partial summation bounds imply, for some fixed C,
(w)

r2 |Ri (r, b)|
≪ (log B)C E(2).
ϕi (s)

(6.5)

This is smaller than every negative power of log √
B.
√
4
If b > (log B) , split
the
exponent
interval
at
b.
Above
this
point
E(
b) is smaller than
√√
−A
3/2
every B : indeed
b log w ≫ (log B) . Below it every relevant next ratio is at least
√
√
s b − 1, and the boundary ratio is at least s b. The Dickman bounds from Lemma 4.2,
together with the backward-ratio bounds there, show that these deviations divided by ϕi (s)
are smaller than every B −A , uniformly for s ≤ S. One can see the uniformity by comparing
the arguments to s: their separation is at least a constant times (log B)2 , while the derivative
weights have exponentially decreasing ratios beyond any fixed compact set. Any fixed
polynomial losses are absorbed. Since r = O(B) along a path, the same assertion holds after
multiplication by r2 .
2
Apply (5.5) and sum over at most N = O((log B)3 ) steps. The starting factor ϕe (sst )/rst
−2
is O(B ), and (6.5) and its large-cutoff counterpart show that the low-state contribution to
(6.4) is o(B −2 ).
It remains to bound histories having a ratio above S. The crude bound for every residual
is O(log B), since all deviations in its definition are bounded and the total harmonic prime
sum is O(log B). We claim the sharper bound
(w)

|Ri (r, b)| = OA (B −A )

(r ≥ S/2)

(6.6)

without√ a ratio restriction. In the preceding error estimates split instead at Q =
(log B) log log B. For x ≥ Q, the PNT saving has exponent at least a constant times
(log B)(log log B)1/4 , and hence beats every B −A . For
√ x ≤ Q, each relevant argument
r/x or r/x − 1 is at least a constant times log B/ log log B. The Dickman bound
ρ(v) ≤ exp(−v log v + O(v)) makes its deviation smaller than every B −A . The endpoint
errors fall into the same alternatives. This proves (6.6).
30

## PDF page 31

The total prefix weight is O(B), so (6.6) deals with the high-history prefixes whose
terminal gaps are at least S/2. A high ancestor on the x > 2 tree has gap greater than
2S. Any remaining prefix with terminal gap below S/2 has reduced that ancestor’s gap by
more than half. The factorial-tail argument in Lemma 5.2, multiplied by the crude O(log B)
residual bound, deals with those prefixes. This completes the proof.

6.2

The boundary anomaly

For the actual discrete reference tree at cutoff 2, put
(w)

δi (r) = Pi (r, 2) − V (2)fi (r/2),

r ≥ 4 (i = e),

r ≥ 2 (i = o).

(6.7)

These domains contain every state reached when iterating the root recurrence only through
exponents x > 2. A possible first upper state arising from a starting ratio below 2 still has
gap tending to infinity, so it causes no exception.
Let Qi (r, b) denote the continuous reference polynomial, obtained from the same admission
rule by replacing prime sums by ordered integrals in dx/x, with exponents above 1. On the
displayed domains define
δi (r) = Qi (r, 2) − 12 fi (r/2).
(6.8)
Lemma 6.2 (Boundary convergence and decay). On every fixed compact subset of their
(w)
respective domains, δi converges uniformly to the continuous function δi . Uniformly for
sufficiently large w,
(w)
(6.9)
|δi (r)| + |δi (r)| ≪ exp(−cr log(r + 2)).
Proof. On a fixed compact gap interval the admitted polynomial has bounded length, because
every exponent exceeds 1. For each such length, Lemma 5.1 gives convergence of the ordered
prime sum to its harmonic integral. Ties, moving upper endpoints, and admission equalities
are confined to sets of continuous measure zero. The same argument works along any
convergent sequence of gap parameters. The continuous integrals depend continuously on
those parameters by dominated convergence, so compactness yields uniform convergence.
Also V (2) → 1/2 by (6.1).
For decay, compare the cutoff polynomial with the full product V (2). At a first omitted
lower leaf after m boundary exponents, all of which are at most 2, the failure of admission
requires m > (r − 4)/2. The total discrepancy is bounded by the sum of the weights of such
first omissions times their exact subsequent survivor product, which is at most 1. Thus it is
bounded by
∑
∑ 1
T2m
,
T2 =
= log 2 + o(1).
m!
p
2
m>(r−4)/2
w<p≤w

This is O(exp(−cr log(r + 2))). The continuous full product is exp(− 12 dx/x) = 1/2, and its
first-omission decomposition has the same bound. Finally the benchmark deviations a(r/2)
and c(r/2) have the required decay by Lemma 4.1. Combining these comparisons proves
(6.9).
∫

Iterate the difference between the reference recurrence and its benchmark only through
x > 2. At every visited state, including the root, insert its anomaly (6.7) and its residual
(6.2); propagate an insertion with the original prefix weight and sign (−1)m at depth m.
More explicitly, subtracting the benchmark from the recurrence gives its cutoff-2 anomaly
minus the child differences, plus the residual; repeated substitution gives
Pe (r0 , B) = V (B)fext (r0 /B) + Dw + o(B −2 ),

Dw =

∑
p

31

(w)

(−1)|p| h(p)δi(p) (r(p)),

(6.10)

## PDF page 32

where Lemma 6.1 bounds the residual sum absolutely.
Compact convergence in Lemma 6.2, the compact occupation limit in Proposition 5.5,
and its exponentially weighted tail estimate justify passing to the limit in Dw . The limiting
stationary densities are πe (t) = ϕe (t) and πo (t) = (1 − t−2 )ϕo (t), and the arrived-at cutoff
restriction is t < r/2. Moreover
ϕe (2)
B 2 ϕe (r0 /B)
−→
= eγ .
4
r02
Consequently
B 2 Dw
1
lim
=
w→∞
eγ
Mg

{∫ ∞

∫ r/2

2

−

4

2

∫ ∞

∫ r/2

r2 δo (r)

dr
r

(1 − t−2 ) dt

1

2

6.3

dt

r δe (r)

dr
.
r
}

(6.11)

The signed correction integral

Set y = r/2 − 1 and define
l(y) = 2Qe (2y + 2, 2)

(y ≥ 1),

u(y) = 2Qo (2y + 2, 2)

(y ≥ 0).

The even inner integral in (6.11) is y − 1; the odd inner integral is y 2 /(y + 1). Since
r dr = 4(y + 1) dy, that limit is 2I/Mg , where
∫ ∞

I=

(y 2 − 1) l(y) − f (y + 1) dy −
(

)

∫ ∞

y 2 u(y) − F (y + 1) dy.
(

)

(6.12)

0

1

All these integrals converge absolutely by (6.9).
To determine the sign of I, compare the boundary polynomials with the full survivor
product over exponents in [1, 2]. That product is 1/2, so this comparison replaces both l and
u by 1. Denote the resulting integral by Ifull . As a = 1 up to 2 and a + c = c0 , it equals
2eγ

∫ ∞ 2
y ρ(y)
0

y+1

dy −

1
−
3

∫ ∞
2

8
a(t) dt = .
3

(6.13)

Here are ∫the identities giving the last equality. The Dickman integral ∫equation holds ∫in the form
y
yρ(y) = max(0,y−1)
ρ(t) dt also below 1. Integration and Fubini give 0∞ yρ(y) dy = 0∞ ρ(y) dy.
∫
∫
The differential equation gives 0∞ ρ(y)/(y+1) dy = − 1∞ ρ′ (t) dt = 1. Thus the decomposition
y 2 /(y +1) = y −1+1/(y +1) makes the ∫first integral in (6.13) equal to 2eγ . Finally Lemma 4.1,
at
s = 1 in the identity for c, gives 0∞ a = 2eγ − 1; subtracting the interval [0, 2] gives
∫∞
γ
2 a = 2e − 3.
The actual boundary rule can only reduce this full-product contribution: a first omitted
lower leaf removes a positive term for a lower start and a negative term for an upper start.
We quantify the resulting loss by recording the first omission. Consider ordered boundary
exponents

2 ≥ x1 ≥ · · · ≥ xm ≥ 1,

Am =

m
∑

xj + x m ,

j=1

A′ =




0,

m = 1,
2,
m = 2,


A
m−2 , m ≥ 3.

For boundary exponents the stronger admission rule is rchild ≥ x + 2. Starting at gap 2y + 2,
this says 2y ≥ Am at a prospective lower child. The thresholds increase within each parity:
32

## PDF page 33

for m ≥ 3 their difference is xm−1 + 2xm − xm−2 > 0 on [1, 2], and A2 > 2. Consequently
the first omitted child occurs at even m for a lower start, and at odd m for an upper start,
exactly when
A′ /2 ≤ y < Am /2.
(6.14)
The exceptional value A′ = 2 for m = 2 expresses the lower-start domain y ≥ 1; A′ = 0 for
m = 1 expresses the upper-start domain y ≥ 0.
After this first omitted leaf, the exact full survivor product over smaller boundary
exponents is 1/xm . This follows either by the product identity or by the absolutely convergent
full inclusion– exclusion series with harmonic intensity log xm . Omitting a positive evendepth term lowers the lower polynomial; omitting a negative odd-depth term raises the upper
polynomial. These signs, the factor 2 in l, u, and integration over (6.14) give
1
Ifull − I = 2
x
m≥1 2≥x1 ≥···≥xm ≥1 m
∑∫

{

A3m − (A′ )3
Am − A ′
− 12|m
24
2

} m
∏ dxj
j=1

xj

.

(6.15)

Every term is nonnegative: its expression in braces is the integral of y 2 or y 2 − 1 on its allowed
window. The bounds below also establish convergence, so the first-omission summations and
integrals are justified by Tonelli’s theorem.
∫
Write Lm for the mth term of (6.15) and λ = log 2. The first term is L1 = 12 (2x/3) dx = 1.
For completeness we evaluate the next two terms by explicit one-dimensional reductions.
Integrating x1 first in the m = 2 term gives
∫ 2{

L2 =
1

2
16
23t
+2+ − 2
18
t
9t
(
)
}
2t 2
4
2
35
+
− + 2 log
dt = − − λ2 + 3λ.
3
t
3t
t
36
−

(6.16)

Indeed the original integrand in this case is
1
x1 x22

{

}

(x1 + 2x2 )3 − 8
− (x1 + 2x2 − 2) .
12

For m = 3, the original integrand is
(x1 + x2 + 2x3 )3 − 8x31
.
12x1 x2 x23
Integrating x1 from x2 to 2 and then x2 from x3 to 2 yields
∫ 2{

L3 =
1

2
23t
1
14
2
t
log2 + −
+ 2 + − 2 log
3
t
18
t
9t
t
}
119t 9
3
43
1
623 19
+
− +
+
dt =
− λ + λ2 .
2
216
4 2t 27t
432 12
3
(

)

(6.17)

These equalities involve∫ only elementary antiderivatives. For an explicit check of the last
integrations, put Jj,k = 12 tj−1 logk (2/t) dt. The needed values are
j
2
1
0
−1
Jj,0
3/2
1
λ
1/2
Jj,1 3/4 − λ/2 1 − λ λ2 /2 λ − 1/2

J2,2 =

3 λ λ2
− − .
4 2
2

Substitution in (6.16) and (6.17) proves the displayed formulas exactly.
33

## PDF page 34

For m ≥ 4, ordering gives
Am − A′ = xm−1 + 2xm − xm−2 ≤ 2xm ,

Am ≤ (m + 1)x,

x=

m
1 ∑
xj .
m j=1

Since A3m − (A′ )3 ≤ 3A2m (Am − A′ ), and dropping the negative even term only increases the
answer, the integrand including the factor 2/xm is at most A2m /2. This last upper bound
can be replaced by the symmetric function (m + 1)2 x 2 /2. Under the probability measure
dx/(λx) on [1, 2],
−1

Ex = λ

3
Ex =
,
2λ
2

,

2

−2

Ex = λ

1
+
m

(

3
− λ−2 .
2λ
)

Integration over the ordered region divides a symmetric integral by m!. We obtain the
rigorous tail bound
1 ∑
λm
(m + 1)2
Lm ≤
2 m≥4
m!
m≥4
∑

{

λ

−2

1
+
m

(

3
− λ−2
2λ

)}

< 0.34.

(6.18)

Here is a coarse numerical verification with strict rational margins. From 0.69 < λ < 0.70,
the expression in braces for m ≥ 4 is at most 3/(4(0.69)2 ) + 3/(8(0.69)) < 2.14. Also
∑

(m+1)2

m≥4

(
)
9
(0.70)m
8
= e0.70 (0.70)2 +3(0.70)+1 −1−4(0.70)− (0.70)2 − (0.70)3 < 0.313.
m!
2
3

For example, e0.70 < 2.014, obtained by summing its Taylor series and bounding the remaining
positive tail geometrically, already gives the last strict inequality. Their product with 1/2
is less than 0.34. The exact expressions above also give L2 < 0.66 and L3 < 0.52 on
0.69 < λ < 0.70. Therefore
I>

8
− 1 − 0.66 − 0.52 − 0.34 > 0.14.
3

(6.19)

Proposition 6.3 (Positive reference margin). At the root of the reference tree,
B 2 Pe (r0 , B)
2I
−→ −a⋆ +
> 0.02.
γ
e
Mg

(6.20)

In particular, there is an absolute cL > 0 such that B 2 Pe (r0 , B) ≥ cL for all sufficiently large
z.
Proof. The parameter definitions imply
r0 = 2B − a⋆ + 2 −

2 log L
+ o(1) = 2B − a⋆ + o(1).
log w

′ (2) = eγ , (6.1) gives
Since fext

B 2 V (B)fext (r0 /B)
−→ −a⋆ .
eγ
Equations (6.10), (6.11), and (6.12) give the limit in (6.20). Finally Mg ≤ 4eγ by (4.22). The
∑
elementary bound γ ≤ 6j=1 j −1 − log 6 < 0.66 implies eγ < 1.95. Together with a⋆ = 0.01
and (6.19), this yields
2I
0.28
−a⋆ +
> −0.01 +
> 0.02.
Mg
4(1.95)
The eventual positive constant cL follows.
34

## PDF page 35

Remark 6.4 (A sharper bound for the correction integral). The same analytic majorant gives
I > 0.2229793730 using rational arithmetic. To record the bound explicitly, put
b=

693147180559946
,
1015

(m + 1)2
tm (t) =
2m!

[(

J(t) =

517 17t 2t2
−
+
,
432
12
3

1 m−2
3 m−1
1−
t
+
t
.
m
2m
)

]

The expansion log 2 = 2 j≥0 ((2j + 1)32j+1 )−1 shows that 0.69 < λ = log 2 < b: after j = 15
the remainder is at most 2/(33 · 333 (1 − 1/9)). The exact formulas for L2 , L3 and the tail
∑
majorant (6.18) give I ≥ J(λ) − m≥4 tm (λ). Each tm is increasing, whereas J is decreasing
on [0.69, b]. For m ≥ 13,
∑

tm+1 (b)
(m + 2)2
225b
≤b
≤
< 1.
3
tm (b)
(m + 1)
2744
Indeed the remaining factor in tm (b) is 1 + (3b/2 − 1)/m, which decreases with m. Summing
the geometric remainder and evaluating the finite rational expression therefore yields
I > J(b) −

12
∑

tm (b) −

m=4

6.4

t13 (b)
222979373
>
.
1 − 225b/2744
109

A uniform local comparison

The stopped-node argument needs a different consequence of the same boundary analysis.
Its ratios lie slightly above 2, and its cutoffs lie in a large but fixed window. We need a
uniform upper comparison with f (r/b) there, rather than the signed root limit. The following
estimate permits the cutoff window to be chosen before the prime limit; its O(1/b) constant
is independent of that window.
Lemma 6.5 (Local reference estimate). For the continuous reference polynomial,
Qe (r, b) =

f (r/b)
+ O(b−2 )
b

(b −→ ∞,

2 ≤ r/b ≤ 2.22) ,

(6.21)

uniformly in the displayed ratios. On every fixed cutoff window [b0 , b1 ] with b0 sufficiently
large, the corresponding discrete estimate is
Pe (r, b)
= f (r/b) + O(1/b) + ow→∞ (1),
V (b)

b ∈ [b0 , b1 ],

2 ≤ r/b ≤ 2.22.

(6.22)

The constant in O(1/b) is absolute, the last convergence is uniform on the fixed window, and
either prime endpoint convention is allowed.
Proof. In the continuous model the benchmark is f (r/b)/b and the quadrature residual is
identically zero by (6.3). Its correction is the sum of the boundary anomalies δi along the
standard paths above 2, with parity signs. The continuous version of (4.17) supplies the
starting factor ϕe (r/b)/r2 ≪ b−2 , uniformly for r/b ∈ [2, 2.22]. The expected sum of the
absolute remaining reward R2 |δi (R)|/ϕi (s) is bounded uniformly in the start. To verify this,
use bounded compact-gap visits on a fixed compact range and, outside it, sum the unit
logarithmic gap bands from Lemma 4.6. After canceling ϕi , a band R ≤ r′ ≤ eR costs at most
a fixed polynomial in R times exp(−cR log(R + 2)), by (6.9); the resulting series converges.
The empty prefix and the explicitly bounded first step satisfy the same estimate. This proves
(6.21).
35

## PDF page 36

For fixed b ∈ [b0 , b1 ] and the indicated ratios, the starting gap is bounded and the ordered
reference polynomial has uniformly bounded length. Lemma 5.1 therefore gives uniform
convergence of the discrete polynomial to Qe : along any convergent parameter sequence, tie,
cutoff, and admission boundaries have continuous measure zero, and dominated convergence
applies to each bounded-length integral. Compactness makes this uniform on the whole
window. Endpoint inclusion or exclusion makes no difference to the limit. Finally (6.1) gives
V (b) → 1/b uniformly there. Divide the continuous estimate by 1/b, and transfer it to the
primes, to obtain (6.22).

7

Compact errors and independent prime boxes

The approximation of the original tree by its reference tree is already adequate at nodes with
large gap. At a node with bounded gap, however, a large relative error in the small-prime
sieve need not be impossible. We first locate a recent edge on which such an error is visible,
and then place the relevant tuples in boxes of independently varying primes. The width of
the boxes will be chosen last; all constants used to sum their measures must therefore be
independent of that width.
For a tuple d = p1 · · · pm , always written with p1 > · · · > pm > w, write
xj = x(pj ),

rj = r0 −

j
∑

vj = logw Jp1 ···pj = rj + a⋆ − 2.

xi ,

i=1

An endpoint means a tuple, together with its length, in the included tree of Section 3. Its
prefixes are the preceding tuples on the same branch. For a nonempty tuple its strict cutoff
is bd = xm ; the root has the weak cutoff B. For a family A of endpoints, put
∑ 1

m(A) =

d∈A

d

.

(7.1)

Different lengths are counted separately. This is the natural measure because µd = Y V0 /d.
Here is the error accounting that the construction will serve. Let S be any prefix-free
collection of included lower nodes at which the original tree is stopped, and let T be its
retained nonstopped nodes. Expanding the reference tree only as far as these stops and then
using the original tree identity gives
S1 (B) ≥ Y V0 Pe (r0 , B) +

∑(

)

Sd (bd ) − µd Pe (rd , bd ) −

d∈S

∑

|Nd − µd |.

(7.2)

d∈T

All stopped nodes have even length, so their exact-subtree corrections have a positive sign.
By Lemma 2.3 and the exponentially weighted tail estimate in Proposition 5.5,
lim lim sup

K→∞ z→∞

∑
B2
|Nd − µd | = 0.
Y V0 d included

(7.3)

rd >K

Also, for each fixed K,
∑

|Nd − µd | ≤ CK ε

d included, rd ≤K
|Nd /µd −1|≤ε

Y V0
.
B2

(7.4)

These estimates are over the full included tree, so they remain valid after any stops have
been imposed. We must control the remaining compact endpoints, at which the relative
error exceeds ε. At all included endpoints Lemma 2.3 also gives |Nd /µd − 1| ≪a⋆ 1. Thus
discarding a family A of compact endpoints costs Oa⋆ (Y V0 m(A)) in (7.2).
36

## PDF page 37

7.1

A recent witnessing edge

Lemma 7.1 (Witnessing edge). Fix K and 0 < ε < 1. One can choose a fixed K∗ > K + 10
such that, with
ε
,
He = ⌈2K∗ + 10⌉,
δ=
4He
the following holds for all sufficiently large z, uniformly in the prescribed residue classes. If
an included endpoint d has rd ≤ K and |Nd /µd − 1| > ε, then one of its last He edges, with
parent d′ and child prime u, satisfies
∣
∣
∣
′
′∣
∣Nd′ u − Nd ∣ > δ µd ,
∣
∣
u
u

x(u), logw Jd′ ≤ 2K∗ + 3,

logw Jd′ u ≥ a⋆ .

(7.5)

Proof. Choose K∗ so that Lemma 2.3 gives |Ne /µe − 1| < ε/2 whenever logw Je ≥ K∗ . Along
the given branch the numbers vj decrease strictly, by more than one at each step. Let i be
the first index for which vi < K∗ . This index exists because rd ≤ K, and it is not the first
index: v1 ≥ logw Y − B → ∞.
Every nonroot included lower node of cutoff b has both r ≥ 2b and r ≥ b + 2, by (3.3).
Its odd child of exponent x ≤ b consequently has rchild ≥ x and rchild ≥ 2. An included even
child has rchild ≥ H(x) ≥ 2x. Thus at the crossing index i, regardless of its parity,
xi ≤ ri = vi + 2 − a⋆ < K∗ + 2,

vi−1 = vi + xi < 2K∗ + 2.

All included nodes have vj ≥ a⋆ . It follows that there are fewer than He edges from the
crossing parent to d, and each of them has parent v ≤ 2K∗ + 3, exponent at most 2K∗ + 3,
and child v ≥ a⋆ .
Put ee = Ne /µe − 1. For each edge of prime u,
ed′ u − ed′ =

Nd′ u − Nd′ /u
.
µd′ /u

The error at the crossing parent has absolute value less than ε/2, whereas the final error has
absolute value greater than ε. Telescoping and the triangle inequality show that one of the
fewer than He differences has absolute value greater than ε/(2He ) > δ.

7.2

Bins, boxes, and regular endpoints

Fix for the moment 0 < ξ < 1. Partition (w, z] into right-closed bins of equal logarithmic
width, using
⌈
⌉
log(z/w)
log(z/w)
nbin =
bins,
h=
log(1 + ξ)
nbin log w
for their width in the exponent coordinate x = logw p. Thus h ≍ ξ/ log w for fixed ξ, and the
ratio of the upper and lower endpoints of a bin is at most 1 + ξ. A bin with lower endpoint
U has
ξU
n(U ) ≍
(7.6)
log U
primes, uniformly for w ≤ U < z, once z is sufficiently large depending on the fixed ξ. This
follows from Lemma 2.2; the same conclusion holds for the last bin because its logarithmic
width equals that of the others. The bin’s representative exponent is its right endpoint in
exponent coordinates.
A full box fixes a length and the ordered bin labels of all its positions. If a bin appears mj
times, choose any mj distinct primes in that bin and put them in decreasing order. Choices
in different bins are independent. Give each resulting tuple weight 1/d, and write m(B) for
37

## PDF page 38

the sum of these weights over a full box B. Equivalently, the probability measure obtained by
dividing by m(B) is a product, over its used bins, of the reciprocal-product measures on the
chosen subsets. A position has multiplicity one if its bin is used just once in the whole box.
A search bin is a bin whose lower exponent endpoint is at least w1/4 . We use the fixed
constant αmax = 1/100. For a constant αmin > 0 to be chosen below, a bin wholly contained
in [αmin B, αmax B] in exponent coordinates will be called an isolated-bin candidate. When at
least one such bin is used, designate the first such position as the isolated position; its prime
will be denoted by p.
Proposition 7.2 (Regular boxes). Fix K and K∗ > K + 10. For every ϑ > 0 there are fixed
constants Clen and αmin > 0, followed by constants ξ0 > 0 and Cth < ∞, with the following
properties. They are chosen before z tends to infinity, and Cth is independent of 0 < ξ ≤ ξ0 .
Put
∆ = 2Clen ξ.
(7.7)
For each fixed 0 < ξ ≤ ξ0 and sufficiently large z, there is a family G of regular included
endpoints with rd ≤ K such that
(

)

m {d included : rd ≤ K} \ G ≤

ϑ + Cth ∆ + oξ (1)
.
B2

(7.8)

The term oξ (1) tends to zero after all fixed parameters, including ξ, have been chosen. The
statement is uniform in the prescribed residue classes. The regular endpoints and their
covering full boxes have these additional properties.
(i) Every regular endpoint has length at most Clen log B and has an isolated position. Every
used search bin, including its isolated bin, has multiplicity one. Every position satisfying
xj ≤ 2K∗ + 3,
also has multiplicity one.
Lemma 7.1.

rj−1 ≤ 2K∗ + 5

The isolated position precedes every edge supplied by

(ii) For every nonempty even prefix of a regular endpoint,
rj − H(xj ) > 10∆.

(7.9)

Moving prime choices anywhere within their fixed bins changes any prefix gap by at
most ∆, and changes a threshold expression rj − H(xj ) by at most ∆ + 2h. In particular
the representative gaps and exponents of every regular box satisfy
rjrep ≥ H(xrep
j ) + 3∆

at every nonempty even prefix.

(7.10)

(iii) Let B be the distinct full boxes containing at least one regular endpoint. There is a
box , depending only on a fixed enlargement of the endpoint compact range
constant CK
and the allowed starting ratios, such that
∑

m(B) ≤

B∈B

box
CK
.
B2

(7.11)

In particular this constant is independent of ξ, ϑ, and the total number of boxes. Every
tuple in these boxes is a standard path from initial gap r0 + 1, ends at gap at most K + 2
for that starting gap, and has its actual final logw J ≥ 3a⋆ /4.

38

## PDF page 39

(iv) In a regular box, declare an edge a candidate if it is among the last He = ⌈2K∗ + 10⌉
positions, is after the isolated position, has multiplicity one, and can satisfy the size
bounds in (7.5) for some tuple in the box. There are at most He candidates, and
every witness for a regular endpoint is among them. Throughout the whole box of each
candidate, writing its parent as d′ = pq and its prime as u, one has
logw

Y
≤ 2K∗ + 4,
pq

logw

Y
3a⋆
≥
.
pqu
4

(7.12)

The bins for p and u have lower endpoints R and U satisfying
z αmin ≤ R ≤ z αmax ,

w ≤ U ≤ w2K∗ +4 .

(7.13)

The choices of p, q, u, and the descendants after this edge are independent under the
full-box measure. All their prime factors are disjoint. If Sq is the product of the bin
upper endpoints for the factors of q, with their specified multiplicities, then
1≤

Sq
≤ (1 + ξ)Clen log B .
q

(7.14)

(v) Every regular box has at least c7 log w search positions, for an absolute c7 > 0 and
sufficiently large z. These positions have distinct bins. All its nonsearch positions follow
all its search positions.
Proof. We first establish the exclusions leading to (7.8). The compact-history estimate in
Proposition 5.5 permits each geometric exception to be estimated in the tilted prime chain,
at a cost at most CK B −2 times its occurrence probability. Histories with a ratio exceeding
S∗ = (log B)2 cost OA (B −A ) in the original measure, by Lemma 5.2. On the remaining
histories, Proposition 5.3 compares the prime chain with the continuous chain up to
N∗ = O((log B)3 )
steps. Its failure probability tends to zero, and its matched states satisfy |s − s̃| ≤ h0 and
| log(r/r̃)| ≪ N∗ h0 , with h0 smaller than every fixed negative power of log B. These errors
remain negligible in all polynomially many opportunities below. We work with the continuous
comparison where useful, retaining the indicated slack when returning to prime paths.
Length. The iid regeneration cycles from Lemma 4.3 have finite mean length and positive
finite mean log decrement. Their exponential moments imply finite variances, so Chebyshev’s
inequality applied to the iid cycle sums gives their respective weak laws. Inverting the positive
mean decrement and bounding the last incomplete cycle then gives a positive limiting log
decrement per step in probability. Indeed, the largest length among O(log B) cycles is o(log B)
in probability by the exponential moment. The initial segment is uniformly tight for the
allowed starting ratios. Choose a fixed Clen larger than twice the reciprocal of this speed. The
probability that more than Clen log B steps occur before the accumulated decrement exceeds
log r0 + O(1) tends to zero. An included compact endpoint has rd ≥ 2, so its accumulated
decrement is at most that quantity. The coupling transfers this conclusion. The excluded
harmonic mass is o(B −2 ).
An isolated position. Put θ = αmax /4. A path from the initial gap to a fixed compact
must cross below θB. After the first step, each transition of a standard path leaves at least
half of the old gap: an even parent has next exponent at most half its gap, and an odd parent
39

## PDF page 40

with an admitted even child has next exponent at most one third of its gap. The first step
cannot itself make this crossing when z is large. Thus the crossing arrival has
.4θB ≤ r ≤ θB.
Consider the slightly enlarged gap band [.3θB, 1.1θB]. By Lemma 4.6, the probability of
any arrived-at state in this band with ratio s > T tends to zero uniformly in B as T → ∞.
Indeed the expected count is bounded by a constant times the tail integrals of the invariant
densities, together with the corresponding first-step density; all these tails tend to zero.
Choose T so that this probability costs less than ϑ/2 in units of B −2 . At the crossing
arrival with s ≤ T , its last exponent is x = r/s, so
.4θ
B ≤ x ≤ θB.
T
Choose 0 < αmin < .2θ/T . The entire bin of this factor then lies in [αmin B, αmax B] for large
z, also after the coupling errors. Designate the first such used bin. Since αmin B → ∞, its
position precedes every possible witnessing edge of Lemma 7.1. Also αmin B > w1/4 + h
eventually, so its bin is a search bin.
Repeated search bins. If two positions have the same bin label, some two adjacent
positions have that label. Write x′ for the earlier exponent, x for the next one, s = r/x′ for
the ratio at their parent, and t = r/x − 1 for the next ratio. Then
1
1
−
0 ≤ t − (s − 1) = r
x x′
(

)

≤

sh
.
x

(7.15)

For a search bin, x ≥ w1/4 . On low-state histories, the continuous comparison must therefore
draw into a neighborhood of its lower support endpoint of width at most
h
O (S∗ + 1)
+ N ∗ h0
w1/4
(

(

))

.

The densities of the kernels in (4.16) on such pieces are bounded by a polynomial in S∗ , as
proved in the prime-coupling argument. Summing this conditional probability over at most
N∗ draws gives o(1). Here every polynomial in log B is negligible compared with w1/4 , and
the same polynomials times h0 tend to zero. We discard all these repeats.
Repeated bins at a possible terminal edge. Next discard any repetition involving a
position with xj ≤ 2K∗ + 3 and rj−1 ≤ 2K∗ + 5. It suffices to compare with an adjacent
position in the same bin. If that neighbor is the preceding position, the comparing draw is
the edge at j; if it is the following position, the comparing draw is at j + 1. In either case the
parent gap is already in a fixed compact. Since all used exponents exceed 1, its ratios and
those of the comparing draw are bounded in terms of K∗ . Formula (7.15) now gives a width
OK∗ (h), enlarged under coupling to OK∗ (h + N∗ h0 ). Only boundedly many draws can have
parent gap in this compact before cutoff exit, because each such step decreases the gap by
more than 1. The kernel densities are bounded there. The probability of this exception is
consequently oξ (1). This verifies all multiplicity assertions in part (i), and every witness has
the required singleton bin because its parent r ≤ 2K∗ + 5.

40

## PDF page 41

Near-threshold even prefixes. Discard paths having a nonempty even prefix for which
0 ≤ rj − H(xj ) ≤ 10∆. This event is estimated before imposing the length restriction, so it
suffices to bound its probability by O(∆) + o(1). At its preceding odd state, let the gap be R
and the next ratio be t. Then x = R/(t + 1) and rj = Rt/(t + 1). If x ≥ 2,
rj − H(x) =

R(t − 2)
,
t+1

so the allowed ratios lie within O(∆/R) of 2. If 1 < x ≤ 2,
rj − H(x) =

R(t − 1)
− 2.
t+1

For small ∆ this confines t to a fixed neighborhood of [2, 3], and differentiation in t again
gives a derivative comparable to R. The allowed width is O(∆/R) in this case as well. Both
descriptions are valid with one-sided endpoints when the two branches meet at x = 2.
At any such draw the preceding ratio is at most t + 1, and hence is bounded by an absolute
constant. The kernel density is therefore bounded. In a unit band of log R, the number of
preceding states having this bounded ratio is deterministically bounded: each such arrived-at
state has a log decrement g(s) = log(1 + 1/s) bounded below by a positive constant. Thus
the conditional widths sum over the bands to


O ∆


∑

−j 

e

= O(∆),

j≥0

since all possible parent gaps are bounded away from zero. Coupling enlarges each ratio
width by O(N∗ h0 ); summing over the O(log B) relevant bands gives o(1). This proves the
claimed near-threshold probability bound.
Combining the exclusions with the compact-history bound proves (7.8), after increasing
Cth and using the spare part of ϑ to absorb any fixed adjustable probability costs. All density,
band, and compact-history constants were fixed independently of ξ.
Movement and representative safety.
mh ≤ Clen log B

For a tuple of the retained length,

log(1 + ξ)
≤ 2Clen ξ = ∆
log w

for sufficiently large z, since log B/ log w → 1. This bounds the movement of every prefix gap.
The function H is 2-Lipschitz, proving the threshold movement bound in part (ii). Choose ξ0
small enough that
∆ < min{a⋆ /4, 1/4} and ∆ + 2h < 1
(7.16)
for all sufficiently large z. Since also h = oξ (∆), the clearance in (7.9) leaves more than 3∆
at every representative even prefix. This proves (7.10). In particular these representative
checks depend only on the labels of the box.
The measure of the full-box enlargement. Take a box containing an original regular
endpoint, and let an arbitrary tuple in that full box be given. At every even prefix the original
tuple satisfies rj ≥ H(xj ) ≥ 2xj . Movement to the new tuple can lose at most ∆ + 2h in the
expression rj − 2xj . Increasing the initial gap from r0 to r0 + 1 therefore makes every even
prefix a valid standard admission. The odd steps impose no extra standard admission test.
The endpoint gap for this shifted start is at most K + ∆ + 1 < K + 2.

41

## PDF page 42

The actual, unshifted endpoint has v ≥ a⋆ − ∆ ≥ 3a⋆ /4. Thus all enlargements also retain
the positive length margin needed later for interval freezing.
Distinct boxes of a given length have disjoint tuple sets. Although different lengths are
counted in the sum of box measures, Proposition 5.5 bounds precisely the sum of original
weights over all standard endpoints in a fixed compact. Apply it from r0 + 1 with ending
gap at most K + 2. This start has ratio in [1.99, 2.3] for large z, just as required by that
proposition. We obtain (7.11) with a constant depending only on this fixed compact and the
starting range. No counting factor for the boxes occurs, and this constant is independent of
their width or their defining regularity parameters.
Candidate edges and independence. Every witness of a regular endpoint is among its
last He positions, lies after its isolated position, and has a singleton bin, by the preceding
arguments. Hence it is a candidate. If a candidate can satisfy the witness size bounds at one
tuple, the gap movement at another tuple is at most ∆. The first requirement in (7.16) and
∆ < 1 give (7.12). The corresponding exponent movement is at most h < 1, giving the range
for U in (7.13); the range for R follows from the definition of the isolated position.
Both the isolated bin and the candidate bin have multiplicity one. Moreover, because the
labels are ordered and the candidate bin occurs only once, no bin can contain both a factor
before that edge and a factor after it. Removing the isolated factor from the parent therefore
partitions the remaining choices into disjoint sets of bins for q, for u, and for its descendants.
Their normalized measures are independent by the product description of a full box. They
are also independent of the isolated prime. Sorting and distinctness within any other bin do
not change this conclusion. Inequality (7.14) follows by multiplying the ratio bound 1 + ξ at
every factor of q.
The number of search positions. The total exponent contributed by nonsearch positions
is at most
Clen log B (w1/4 + h) = o(w1/2 ).
(7.17)
They all occur after the search positions, by decreasing bin order. In one regular tuple in
the box, let ms be the number of search positions. Immediately after its last search factor
the gap is at most K + o(w1/2 ) ≤ w1/2 for large z. Each standard transition retains at least
one third of its preceding gap, including the first step for sufficiently large z. Since r0 ≥ B
eventually, this implies
3−ms B ≤ w1/2 ,

ms ≥

log B − 21 log w
.
log 3

Now log B/ log w → 1, so the last expression is at least c7 log w for an absolute positive c7 , for
example c7 = 1/10, once z is sufficiently large. The search labels are fixed throughout the full
box, and their multiplicities are one. This proves part (v) and completes the proposition.
Remark 7.3. Proposition 7.2 separates the adjustable exceptions from the final width choice.
After K and K∗ are fixed, one first chooses ϑ, Clen , and αmin . The bounds for full-box mass
and for compact history events are then fixed independently of ξ. Consequently a later
statement failing on a fraction at most σ of each full candidate box costs at most
σHe

∑

box −2
m(B) ≤ σHe CK
B .

B∈B

This remains true if the number of boxes grows with z or ξ. For a singleton bin, count
fractions and harmonic fractions differ by a factor at most 1 + ξ ≤ 2, so bounds conditional
42

## PDF page 43

on all other factors and measured against all primes in that bin have the same summed
interpretation. Finally ξ may be chosen sufficiently small to make Cth ∆ and all required
movement errors small. The prime-count asymptotics are only used after this fixed choice, so
their eventual thresholds may depend on ξ without changing the constant order.

8

An inverse estimate for a witnessing edge

The exceptional compact nodes will be controlled by varying the isolated prime in a regular
box. The first step identifies the only obstruction to this variation: a positive proportion of
the relevant primes must share a rational intercept. The use of modular concentration to
obtain algebraic structure is related to the inverse-sieve methods of [13, 27]. More specifically,
the small-height polynomial and prime-product strategy is related to Walsh’s algebraicity
method [28, Section 3]. The partial-incidence modular-line form needed in a prime bin,
including its uniformity across the independent boxes, is proved here rather than invoked
from that work.
Definition 8.1. A prime p aligns with a reduced rational A/D, where A ∈ Z, D ∈ N, and
gcd(A, D) = 1, if
Dap ≡ A (mod p).
This condition implies p ∤ D. For a squarefree product q of primes carrying prescribed classes,
write
∏
qE (A/D) =
ℓ.
ℓ|q
ℓ does not align with A/D

Throughout this section put
L
Z = exp
.
log L
(

)

(8.1)

As usual, all parameters other than z are fixed before taking a limit in z. In particular, a
statement valid for every sufficiently small fixed ξ > 0 allows its eventual lower threshold on
z to depend on ξ.
Fix one candidate edge in a full regular box from Theorem 7.2. Write its parent as pq,
with p the isolated prime, and denote its edge prime by u. Let P, U be their respective prime
bins, let R, U be the lower endpoints of these bins, and put
np = #P,

nu = #U.

Both bins are right-closed and have upper-to-lower endpoint ratio at most 1 + ξ. Their
logarithmic widths are comparable to ξ; hence, for each fixed ξ > 0,
np ≍

ξR
,
log R

nu ≍

ξU
.
log U

(8.2)

The constants here can be chosen uniformly for 0 < ξ ≤ 1, once z is sufficiently large
depending on ξ.
Let Q be the set of possible products q. Such a product uniquely determines its sorted
prime choices. Denote by Sq the product of the upper endpoints of its specified bins, with
the prescribed multiplicities; Sq is therefore fixed for the box. The hypotheses supplied by

43

## PDF page 44

Theorem 7.2 include
z αmin ≤ R ≤ z αmax ,

αmax =

1
,
100

w ≤ U ≤ w2K∗ +4 ,

Y
Y
3a⋆
≤ 2K∗ + 4,
logw
≥
,
pq
pqu
4
Sq
1≤
≤ (1 + ξ)Clen log B .
q
logw

(8.3)
(8.4)
(8.5)

The bins of p and u each have multiplicity one in the full box. Thus the choices of p, q, u,
and all descendants after the edge are independent in the full box, and p, u divide none of
the other products involved. In particular,
gcd(p, q) = gcd(pq, u) = 1.
Writing α = log R/L, the parent-length bounds imply
q = z 2−α+o(1) ,

Sq = z 2−α+o(1) ,

αmin ≤ α ≤ αmax .

(8.6)

All the o(1)’s in this section are uniform over boxes satisfying these fixed-parameter bounds,
for each permitted fixed ξ.
The normalized harmonic measure on the box assigns mass proportional to the reciprocal
of the product of its chosen primes. On p, q, u this is the product measure with respective
weights 1/p, 1/q, 1/u. Descendant choices may be integrated out whenever an event depends
only on p, q, u.
Proposition 8.2 (Inverse estimate for an edge). Fix the parameters in (8.3)–(8.5), the
witnessing threshold δ > 0, and 0 < σ < 1. There are constants cp > 0, a list-size bound
F < ∞, and ξinv > 0, independent of the eventual choice of fixed 0 < ξ ≤ ξinv , with the
following property for all sufficiently large z.
The full candidate box has a list A of at most F reduced rationals A/D satisfying
D ≤ RZ 10 ,

|A| ≤ Sq RZ 10 ,

#{p ∈ P : p aligns with A/D} ≥ cp np .

(8.7)

Outside a set of normalized harmonic box measure at most σ, every occurrence of
∣
∣
∣
∣
∣Npqu − Npq ∣ > δ Y V0
∣
u ∣
pqu

(8.8)

has a rational A/D ∈ A for which
DqE (A/D) ≤ RZ 10 .

p aligns with A/D,

(8.9)

The exceptional measure is relative to the whole box, rather than to the subset on which (8.8)
holds.
The proof fixes the whole-box rational list before arguing by contradiction. If too many
bad edges fail (8.9), sampling their frozen residue tests produces many parent pairs but few
permissible slopes. An integer polynomial with small coefficient height then vanishes on the
corresponding integer points. The lemma below bounds the contribution of its nonlinear
components. A remaining rational line has an intercept in the fixed list, forcing most selected
pairs on that line to satisfy (8.9) after all.
The lattice-point estimate below combines algebraic decomposition with Jarník’s convexarc argument [18, Sections 1–2]. We give the proof with explicit degree dependence because
the degree grows with the prime bin. The coefficient-independent intersection bound used in
its proof is established in Lemma B.3.
44

## PDF page 45

Lemma 8.3 (Degree-uniform nonlinear lattice-point bound). Let P ∈ R[X1 , X2 ] be nonzero
and of degree at most D0 ≥ 1, and let S ≥ 1. The number of lattice points in [0, S]2 lying on
at least one nonlinear irreducible component of P = 0, with irreducibility taken over C, is
(

)

O D04 (1 + S 2/3 ) .
The implied constant is absolute, independently of the coefficients of P . No bound is asserted
for points lying only on line components.
Proof. Consider first one nonlinear irreducible factor Q of degree d. If Q is not proportional
to a real polynomial, Q and its coefficientwise conjugate are distinct irreducible polynomials.
Every real zero of Q is a common zero, so Bézout’s theorem gives at most d2 such points.
Suppose instead that Q has been scaled to have real coefficients. Neither QX1 nor QX2
vanishes identically: otherwise irreducibility over C would force Q to be linear. Their degrees
are smaller than d, so their intersections with Q = 0 give O(d2 ) points in total. These include
all singularities and all horizontal or vertical tangencies. There are also O(d) intersections
with the boundary of the square.
On a smooth graph X2 = f (X1 ) with QX2 ̸= 0, the second derivative vanishes precisely
when
2
2
IQ = QX1 X1 QX
− 2QX1 X2 QX1 QX2 + QX2 X2 QX
= 0.
(8.10)
2
1
Indeed f ′′ = −IQ /Q3X2 on the graph. If Q ∤ IQ , Bézout’s theorem adds O(d2 ) inflection
points, because deg IQ ≤ 3d − 4. If Q | IQ , any nonspecial interior smooth graph arc has
f ′′ = 0 throughout and therefore lies on a line. Vanishing on that arc would make the line a
factor of Q, a contradiction. Thus in this latter case all real points in the square are already
among the critical or boundary points counted above.
In the remaining case, mark the abscissae of all critical, boundary, and inflection points,
together with 0, S. There are O(d2 ) marked abscissae. Between consecutive marked abscissae
the interior real zero set is a union of at most d smooth graphs extending across that
open interval. To justify extension, the implicit function theorem applies because QX2 ̸= 0;
continuation cannot end inside the interval without a critical point or an intersection with the
boundary. The bound d follows from the degree of a vertical fiber. Each graph is monotone,
and its derivative is strictly monotone, because neither QX1 nor IQ vanishes on it.
Consider the lattice points of one such graph, ordered by increasing abscissa. Consecutive
difference vectors have positive integer first coordinate and distinct slopes, by strict convexity
or strict concavity. They are therefore distinct integer vectors. Their total ℓ1 -length is at
most 2S, since both graph coordinates are monotone and range over intervals of length at
most S. There are O(T 2 ) integer vectors of ℓ1 -length at most T . Consequently m distinct
such vectors have total length ≫ m3/2 : take T to be a sufficiently small fixed multiple of
m1/2 , so that at least half of the vectors have length greater than T . It follows that this
graph contains O(1 + S 2/3 ) lattice points.
The marked vertical fibers contain at most d points each, since an identically vanishing
fiber would give a vertical line factor of Q. Summing over the O(d3 ) graphs and the marked
fibers proves the bound O(d3 (1 + S 2/3 )) for this component. Finally, sum over the distinct
nonlinear factors of P . Their degrees sum to at most D0 , so the asserted, slightly looser,
bound with D04 follows.
Proof of Theorem 8.2. The fixed whole-box list. To make the order of choices explicit,
choose an integer h1 such that
a⋆ h1
> 12,
2

45

## PDF page 46

and set

γinc
σ
β β h1
γinc
,
c5 =
β= ,
γinc =
,
cp =
.
(8.11)
16
2 4
8
32
These constants are fixed before ξ is chosen and before any failure set, cell, or sample is
selected. For each candidate box let A be the set of all reduced rationals satisfying (8.7).
This is a finite set by the height restrictions.
If two distinct list rationals A1 /D1 , A2 /D2 align at a prime, that prime divides the nonzero
determinant A1 D2 − A2 D1 . Its absolute value is at most
( )

2Sq R2 Z 20 = z 2+α+o(1) .
Every prime of P is at least z αmin . Thus two distinct rationals have at most Cαmin common
aligning primes, with a fixed constant independent of ξ. If M = #A, and mp counts the list
rationals aligning at p, Cauchy’s inequality gives
M 2 c2p np ≤

∑

m2p ≤ M np + Cαmin M (M − 1).

p∈P

Once np ≥ 2Cαmin /c2p , this implies
2
.
c2p

M≤

We may therefore take F = ⌈2/c2p ⌉. This bound is independent of ξ; the threshold on z may
depend on ξ through np .
Call a pair (p, q) structured if (8.9) holds for some member of this fixed whole-box list.
A triple (p, q, u) is called bad if its parent pair is nonstructured and (8.8) holds. Assume,
towards a contradiction, that bad triples occupy more than a σ fraction of the full harmonic
box measure. Descendants can now be integrated out.
From bad triples to sampled incidences. We will select a fixed number of edge
primes so that many nonstructured parent pairs satisfy all their frozen residue tests, while
the total number of permitted slopes over the isolated primes is small. First we restrict q to
a sufficiently large cell. For q ∈ Q, let bq ∈ [1, q] ∩ Z be its Chinese remainder theorem (CRT)
representative for the prescribed hits. Put
M0 =

∏

t,

t≤w

where the product is over primes. By the prime number theorem,
(

log M0 = O(w) = O

L
(log L)2

)

= o(log Z).

In particular M02 = Z o(1) . Partition Q into cells by a value interval of ratio at most 1 + ξ, and
by the pair (q, bq ) mod M0 . By (8.5) the number of value intervals needed is O(Clen log B + 1),
so the total number of cells is Z o(1) .
We record the cardinality bound
#Q ≥

Sq
.
Z o(1)

(8.12)

Indeed, a bin with upper endpoint Pj and multiplicity mj contains ≫ξ Pj / log Pj primes.
Even in the smallest bin this number is much larger than Clen log B, for fixed ξ > 0 and large
∑
z. If nj is its prime count and k = j mj ≤ Clen log B = O(log L), then
(
∏
j

nj
mj

)

≥

∏ (nj /2)mj
j

mj !

≥ Sq exp −Oξ ((log L)2 ) .

46

(

)

## PDF page 47

The first inequality holds once nj ≥ 2mj . In the second, the losses from log Pj , fixed bin-width
constants, and the factorials have total logarithm Oξ ((log L)2 ). Unique factorization identifies
these choices with distinct q’s. Since (log L)2 = o(log Z), this proves (8.12).
Discard cells containing fewer than Sq /Z points. They contain at most Sq Z −1+o(1) points
in total. The weights 1/q vary globally by at most (1 + ξ)k = Z o(1) , so their total normalized
harmonic mass is Z −1+o(1) = o(1). For sufficiently large z, a retained initial cell C therefore
has conditional harmonic density of bad triples at least σ/2, and
#C ≥ Sq /Z.

(8.13)

Within P, C, U each reciprocal weight varies by a factor at most 1 + ξ. As long as ξ ≤ 1,
converting their product measure to uniform counting costs at most (1 + ξ)3 ≤ 8. The count
density of bad triples in P × C × U is consequently at least β = σ/16, with β fixed in (8.11).
Freezing the parent interval. We now place the small-prime count on an interval that is
fixed as q varies within C. For fixed p ∈ P and q ∈ C, put
sp (q) = (ap − bq )q

0 ≤ sp (q) < p.

(mod p),

(8.14)

The parent hit progression is
j ≥ 0.

n = bq + q(sp (q) + pj),

The initial hit belongs to [1, pq], so the condition j ≥ 0 indexes exactly the positive hits. The
allowed j’s form an initial interval of integers whose length is Y /(pq) + O(1).
If the value range of C is contained in [Q− , Q+ ], with Q+ /Q− ≤ 1 + ξ, choose a common
initial integer interval Ip of length
Y
J = Jp =
.
pQ+
⌊

⌋

Its symmetric difference with the actual interval has length O(ξJ + 1). The classes to avoid at
primes t ≤ w on Ip depend only on p, the fixed cell residues, and the value v = sp (q) mod M0 .
This uses the invertibility of pq at every such prime. For each possible v, let m = mp,v count
the survivors on Ip for that pattern, and let me,u = mp,v;e,u count those with j ≡ e (mod u).
The upper bounds in Theorem 2.3 give, uniformly in the patterns,
m ≪ JV0 .

(8.15)

They also show that replacing intervals changes the survivor count by O(ξJV0 ), and the
count in any specified j-class modulo u by O(ξJV0 /u). For the latter assertion, enclose the
difference subsequence in an interval of length comparable to ξJ/u. By (8.4), for fixed ξ > 0
this length is eventually much larger than wa⋆ /2 ; the corresponding progression step pqu is a
unit at every prime at most w. The same reasoning applies to the unconditioned difference
interval. The upper-sieve constants are independent of fixed ξ, although the threshold at
which these lengths suffice may depend on ξ.
The edge hit selects the class
eu = eu (p, q) = (au − bq − qsp (q))pq

(mod u).

(8.16)

Choose ξinv ≤ 1 sufficiently small, depending on δ and the fixed upper-sieve constants. The
preceding replacement estimates show that (8.8) implies
|meu ,u − m/u| > δ ′
47

JV0
,
u

(8.17)

## PDF page 48

for a fixed δ ′ > 0. For example, after decreasing ξinv the choice δ ′ = δ/4 suffices. Define
Ep,u (v) to be the set of residues e mod u satisfying (8.17). These sets depend on p, the initial
cell, and v, and no independence in those variables is asserted.
The large-sieve saving. We bound the average proportion of residues passing an exceptional
test. For fixed p, v, let S ⊂ Ip be the surviving sequence, so #S = m, and put
S(θ) =

∑

exp(2πijθ).

j∈S

Additive orthogonality gives the exact identity
∑

u

u−1
∑

(me,u − m/u)2 =

|S(a/u)|2 .

(8.18)

a=1

e mod u

For prime u, all fractions a/u on the right are reduced. Fractions belonging to distinct such
primes are distinct, and the whole family is separated modulo one by at least ((1 + ξ)U )−2 ≥
(4U 2 )−1 . Lemma B.2 therefore gives
∑
u∈U

u

∑

(me,u − m/u)2 ≪ (J + U 2 )m;

e mod u

see [20, 26]. No condition other than interval support is imposed on the sequence S. Each
exceptional residue contributes more than (δ ′ JV0 )2 /u to the corresponding left side. Using
(8.15), we obtain
1 ∑ |Ep,u (v)|
(J + U 2 )m
≪
nu u∈U
u
nu (JV0 )2
≪ξ (log w)2

(

1
U
+
U
J

)

≤ w−a⋆ /2 .

(8.19)

For the last inequality, log U = OK∗ (log w), V0 ≍ 1/ log w, U ≥ w, and J/U ≫ w3a⋆ /4 . The
fixed factor depending on ξ, as well as the logarithmic factors, is absorbed between the
exponents 3a⋆ /4 and a⋆ /2 by taking z large. This proves (8.19) uniformly in p, v and the
chosen cell, in exactly the fixed-ξ sense required here.
Selecting the sampled relation. For (p, q) ∈ P × C, let f (p, q) be the fraction of u ∈ U for
which (p, q, u) is bad. Its uniform count average is at least β. At least a β/2 fraction of pairs
therefore have f (p, q) ≥ β/2: the complementary bound follows at once from 0 ≤ f ≤ 1.
Sample an ordered h1 -tuple of distinct primes u = (u1 , . . . , uh1 ) uniformly from U. For
this sample define the pair relation
{

Iu = (p, q) ∈ P × C : (p, q) is nonstructured, and
}

eui (p, q) ∈ Ep,ui (sp (q) mod M0 ) for every 1 ≤ i ≤ h1 ,
and put I(u) = #Iu /(np #C). Members of Iu will be called sampled incidences. By (8.17), a
pair for which every sampled triple is bad belongs to Iu . This implication suffices for the
lower bound on its expected density. Once nu ≥ 4h1 /β, each pair with f (p, q) ≥ β/2 has
probability at least (β/4)h1 that all sampled primes witness (8.8). Consequently
EI(u) ≥

β
2

( )h1

β
4

= γinc .

(8.20)

1
Write W = hi=1
ui and refine C by fixing (q, bq ) mod W . For any such refinement C ′ ,
′
and fixed p, let Tp (C ) ⊂ [0, p) ∩ Z consist of those integers s satisfying all the sampled tests,

∏

48

## PDF page 49

using v = s mod M0 . For a fixed v, (8.16) is an invertible affine function of s mod ui , with
coefficient −p mod ui . Its other coefficients are fixed by the refinement. Thus it restricts
s mod ui to exactly |Ep,ui (v)| residues. CRT, applied also to s ≡ v (mod M0 ), gives
|Tp (C ′ )| ≤ Kp (u),
h

Kp (u) :=

1
∑ ∏
|Ep,ui (v)|
p
+ M0 W.
M0 v mod M i=1
ui

(8.21)

0

Indeed, for each v the number of allowed residues modulo M0 W is i |Ep,ui (v)|; an interval of
length p contains at most p/(M0 W ) + 1 integers in each residue. Summing the rounding terms
over v gives at most M0 W . All CRT factors are coprime, and every sampled ui is coprime to
pq by the singleton-bin hypotheses. Crucially, the upper bound Kp (u) is independent of the
refinement centers.
For any numbers 0 ≤ tu ≤ 1, their product averaged over distinct ordered h1 -tuples is at
most
)h1
(
nhu1
1 ∑
,
(nu )h1 = nu (nu − 1) · · · (nu − h1 + 1).
tu
(nu )h1 nu u∈U
∏

The prefactor tends to one since h1 is fixed. Applying (8.19) for each p, v in (8.21) yields
E

Kp (u)
′
≤ 2w−a⋆ h1 /2 + z −c
p

(8.22)

for some fixed c′ > 0. Here M0 W = z o(1) , since h1 and the edge-bin exponent range are fixed,
whereas p ≥ z αmin . Since p/R ≤ 1 + ξ ≤ 2, the same estimates imply




1 ∑
′
Kp (u) ≪ w−a⋆ h1 /2 + z −c = o(L−6 ).
E
np R p∈P
The last step uses w = L/(log L)2 and a⋆ h1 /2 > 12. By Markov’s inequality, the probability
∑
that p Kp > np R/L6 is o(1). As 0 ≤ I(u) ≤ 1, removing those samples changes the
expectation in (8.20) by o(1). Hence there exists a sample for which
I(u) ≥ γinc /2,

∑

Kp (u) ≤

p∈P

np R
.
L6

(8.23)

Fix this sample and abbreviate its bounds by Kp .
There are at most W 2 = wO(1) = Z o(1) refined cells. Discard those with fewer than
Sq /Z 3 points. Relative to C, whose size satisfies (8.13), their total count fraction is at most
W 2 /Z 2 = o(1). Thus some remaining refinement C ′ satisfies
#C ′ ≥ Sq /Z 3
and satisfies

(8.24)

# Iu ∩ (P × C ′ )
γinc
≥
.
′
np #C
4
(

)

At least a γinc /8 = c5 fraction of its q-points consequently have at least c5 np primes p with
(p, q) ∈ Iu . Call these points rich, and let X be their set of integer points (q, bq ). We have
therefore fixed a sample, a refinement C ′ , and slope sets Tp (C ′ ) with #Tp (C ′ ) ≤ Kp . For large

49

## PDF page 50

z, their bounds are
Sq
,
Z4
(
)
#{p ∈ P : (p, q) ∈ Iu } ≥ c5 np (q, bq ) ∈ X ,
∑
np R
Kp ≤ 6 .
L
p∈P
|X | ≥

(8.25)

The point-count bound follows from (8.24); the slope sum is (8.23). Every sampled incidence
with q ∈ C ′ uses the slope sp (q) ∈ Tp (C ′ ). The constants in these bounds are precisely those
fixed in (8.11), without choosing them after the list or after the failure set.
Algebraic concentration and the fixed list. We will find a rational line containing
many rich points and show that its intercept belongs to A. Almost all sampled incidences on
that line will then be structured, giving the contradiction. First the small slope sum lets us
construct a common polynomial equation for the rich points. Put
(

R
D0 =
,
L2
⌊

⌋

N0 =

)

D0 + 2
.
2

We construct a nonzero integer polynomial P (X1 , X2 ) of total degree at most D0 that modulo
each p ∈ P vanishes identically on every line
X2 = ap − sX1 ,

s ∈ Tp (C ′ ).

The coefficients of the polynomial after substitution in a line give at most D0 + 1 homogeneous congruences. The lattice of coefficient vectors in ZN0 satisfying all these congruences
consequently has index at most

∏

p(D0 +1)|Tp

(C ′ )|

≤ exp(D0 + 1)

p∈P


∑

Kp log p .

p∈P

Dependencies among congruences can only decrease this index. Applying the pigeonhole
principle to a box of coefficient vectors, and taking the difference of two vectors in the same
lattice coset, gives a nonzero P with maximum absolute coefficient HP satisfying
log(2HP ) ≪ 1 +

1 ∑
Kp log p = O(R/L4 ) = o(R).
D0 p∈P

(8.26)

For the final equality use (8.23), np ≪ R/ log R, and log p ≍ log R. More explicitly, a
coefficient box with more vectors than the lattice index has two in the same coset; taking side
length equal to the ceiling of the index to the power 1/N0 proves the stated height bound.
All the points (q, bq ) under consideration lie in [0, Sq ]2 . If P (q, bq ) ̸= 0, then
log |P (q, bq )| ≤ log N0 + log HP + D0 log max(1, Sq ) = O(R/L) = o(R).

(8.27)

At a rich point the integer P (q, bq ) is divisible by every prime of its at least c5 np distinct
sampled incidences. Their product has logarithm at least
c5 np log R ≫ξ,c5 R.
For each fixed ξ > 0, this contradicts (8.27) unless P (q, bq ) = 0. Every point of X therefore
lies on the zero set of P .
50

## PDF page 51

Extraction of a rational line. By Theorem 8.3, the number of points of X on nonlinear
irreducible components is at most
(

)

O D04 (1 + Sq2/3 ) = o(Sq /Z 4 ).
To check this uniformly, the principal ratio is bounded by
R4 Sq−1/3 Z 4 = z (13α−2)/3+o(1) = o(1),
2/3

using α ≤ 1/100; the term without Sq
Discard any line containing fewer than

is smaller. There are at most D0 line components.
Sq
RZ 6

Nmin =

selected rich points. All discarded lines together contain at most
D0 Nmin ≤

Sq
= o(Sq /Z 4 )
L2 Z 6

such points. Vertical lines have at most one selected point because q uniquely determines bq ,
and Nmin → ∞. A line not proportional to a real line likewise has at most one real point.
Thus a remaining nonvertical real line contains N ≥ Nmin selected rich points.
Two distinct lattice points on this line give it a rational slope. It can be written
D′ bq = A′ q + B ′ ,

D′ > 0,

gcd(A′ , D′ ) = 1,

A′ , B ′ , D′ ∈ Z.

(8.28)

For its lattice points, consecutive distinct q’s differ by an integer multiple of D′ . Their bq ’s
differ by the corresponding multiple of A′ . Their coordinate ranges are at most Sq , so
D′ , |A′ | ≪

Sq
≪ RZ 6 ,
N

|B ′ | ≪ Sq RZ 6 .

(8.29)

The assertion for A′ also holds for a horizontal line, when A′ = 0, D′ = 1.
Reduce the intercept B ′ /D′ to A/D, putting
g = gcd(B ′ , D′ ),

D′ = gD,

B ′ = gA.

Reduction of (8.28) modulo g gives g | A′ q, and gcd(A′ , g) = 1; hence
g|q

at every selected point of the line.

(8.30)

If a prime ℓ | q does not divide g, division of (8.28) by g modulo ℓ gives
Dbq ≡ A

(mod ℓ).

Because bq ≡ aℓ (mod ℓ), the prime ℓ aligns with the intercept. This congruence also implies
ℓ ∤ D, since gcd(A, D) = 1. All nonaligned prime factors of q therefore divide g. As q is
squarefree and g | q, their product divides g, and
DqE (A/D) ≤ Dg = D′ ≪ RZ 6 .

(8.31)

Neither D nor D′ has been assumed squarefree. In particular, primes common to D and g
cause no difficulty in (8.31). The height bounds in (8.7) follow from (8.29) with ample room
in the additional Z 4 factors. It remains to establish the alignment-count condition for this
intercept.
51

## PDF page 52

The intercept belongs to the list. We use the pair-counting principle of Gallagher’s larger
sieve [7]; see [13, Section 2] for the difference-product argument. Ignore the isolated-bin
primes dividing D′ . There are at most
log D′
= O(1)
log R
of them by (8.29). Let Pun consist of the other primes of P that do not align with A/D =
B ′ /D′ . For p ∈ Pun , substitution of the line equation into the incidence equation gives
(A′ /D′ + s)q ≡ ap − B ′ /D′

(mod p),

s ∈ Tp (C ′ ).

The right side is nonzero because p is unaligned. Each allowed s therefore admits either no
solution or exactly one class of q mod p. Thus those of the N selected points on the line that
satisfy the sampled constraints for p occupy at most Kp classes of q mod p. Let their number
be Np , and let np,c denote the numbers in these occupied classes. Here Np counts all tested
points on the line, so it dominates the number of pairs (p, q) ∈ Iu there; the latter pairs also
require the parent to be nonstructured.
For two distinct selected points, q1 − q2 ̸= 0 and |q1 − q2 | ≤ Sq . The number of isolated-bin
primes dividing this difference is at most
log Sq
= Oαmin (1).
log R
Counting ordered equal-class pairs, with the diagonal separated, therefore gives
∑ ∑

n2p,c ≤ Cαmin N 2 +

p∈Pun c

∑

Np .

p∈Pun

Cauchy’s inequality, first over all occupied classes and primes, yields
2


∑

p∈Pun



Np  ≤ 


∑

Kp  Cαmin N 2 +

p∈P


∑

Np  .

(8.32)

p∈Pun

Use p Np ≤ np N , the good-sample bound, and N ≥ Sq /(RZ 6 ). After division by n2p N 2 ,
the right side of (8.32) is
∑

(

R
R
O
+
6
np L
N L6

)

= Oξ (L−5 ) + o(1) = o(1).

(8.33)

For the first term use (8.2) and log R ≤ L; for the second use R2 Z 6 /Sq = z 3α−2+o(1) = o(1).
Thus unaligned primes supply only o(np N ) tested pairs on the line, and hence at most this
many sampled incidences.
Each of its N selected points has at least c5 np sampled incidences by (8.25). The ignored
divisors of D′ supply at most O(N ). The remaining incidences force at least (c5 − o(1))np
primes of P to align with the intercept. Since cp = c5 /4, it satisfies the last condition in (8.7),
and hence A/D ∈ A. At every selected point of this line, (8.31) implies the required bound
DqE (A/D) ≤ RZ 10 for large z. Every tested pair on the line whose isolated prime aligns is
therefore structured. Since all members of Iu are nonstructured, the sampled incidences must
consequently come from the unaligned primes or the O(1) ignored primes; those contribute
only o(np N ) + O(N ), contradicting their lower bound c5 np N .
This contradiction proves the exceptional-fraction assertion. The constants in (8.11)
and the list bound were fixed before ξ. Only interval freezing required an upper restriction
ξ ≤ ξinv ; all losses that depend on a fixed positive ξ, including prime counts, polynomial
divisibility, and (8.33), are absorbed by taking z sufficiently large afterwards. This completes
the prescribed order of choices.
52

## PDF page 53

9

Variance after the inverse estimate

The inverse estimate leaves a fixed finite list of rational alignments in each candidate box. Fix
one rational and every endpoint factor except the isolated prime. We average over the whole
isolated bin by temporarily imposing the aligned hit class at each prime; at the primes that
actually align, this gives the original hit progression. We show that a positive fraction of these
progressions can have large small-prime sieve errors only when two arithmetic parameters of
the family are small. One controls the nonaligned factors; the other controls the translation of
the progression after the aligned factors are removed. The auxiliary probability models used
below are explicit dominating measures; we do not assume that the residue classes selected
by the actual primes are independent.

9.1

Arithmetic coordinates

Fix a candidate box from Theorem 7.2, and write P for its isolated prime bin, R for the lower
endpoint of that bin, and np = #P. Thus
z αmin ≤ R ≤ z αmax ,

np ≍

ξR
.
log R

The constants in comparisons of this form can be taken independent of sufficiently small fixed
ξ; the threshold on z may depend on ξ. Fix all prime choices in a final compact endpoint
except the isolated p ∈ P, and write
d = pqf .
Fix also one reduced rational A/D, D > 0, from the candidate list in Theorem 8.2. All of
qf , A, D remain fixed as p varies. As before, let qf,E be the product of the nonaligned prime
factors of qf , and put qf,A = qf /qf,E .
If the structured-parent conclusion of Theorem 8.2 holds, the product of the candidate
edge and the later factors is at most a fixed power of w, by the candidate parent-gap bound.
Hence, for large z,
H := Dqf,E ≤ RZ 11 ,
|A| ≤ Sq RZ 10 .
(9.1)
Here q is the product of the other factors at the candidate parent, Sq is the corresponding
product of bin upper endpoints, and
qf ≥ q,

Sq /q ≤ Z o(1) .

The additional factor Z in the bound for H absorbs any fixed power of w.
Let b ∈ [1, qf ] be the integer CRT representative of the hit conditions at the primes of qf ,
and define
(
)
|C0 |
Db − A
C0 =
,
T = max H,
.
(9.2)
qf,A
R
The numerator is divisible by every aligned factor of qf , so C0 is an integer. To see the role
of these parameters, write the hit progression at qf as n = b + qf v. Then
Dn − A = qf,A (C0 + Hv).
Thus removing the aligned factors leaves an arithmetic progression of step H and initial value
C0 . Alignment at the isolated prime will require this remaining value to be divisible by p.
The scale T measures both its step and the size of its initial value after division by a prime
in the bin p ≍ R.
We also have
(C0 , H) = 1.
(9.3)
53

## PDF page 54

Indeed, qf,A is coprime to Dqf,E . At a prime t | D, reducedness gives Db − A ≡ −A ̸≡ 0
(mod t); at a prime t | qf,E not dividing D, nonalignment gives Db − A ≡ Dat − A ̸≡ 0
(mod t). This also covers common prime divisors of D and qf,E . Prime powers in D cause no
further restriction. In particular, C0 = 0 can occur only when H = 1. The height bound gives
|C0 |
|Db − A|
1
|A|
1
Sq
=
≤ +
≤ + Z 10 ,
RH
RDqf
R RDqf
R
q
and therefore
T /H ≤ Z 12

(9.4)

for sufficiently large z.
For any p ∈ P not dividing H, temporarily impose the aligned class at p, whether or not
its actual prescribed class aligns. Since p ∤ qf , the additional hit condition is C0 + Hv ≡ 0
(mod p). There is a unique k ∈ {0, . . . , p − 1} satisfying this congruence, and all its solutions
have the form v = k + pj. Define
C0 + Hk
m0 =
.
p
Equivalently, m0 is the unique integer satisfying
m0 ∈ [C0 /p, C0 /p + H),

pm0 ≡ C0

(mod H).

(9.5)

The interval has length H, and the congruence fixes one residue modulo H, which also verifies
uniqueness in these coordinates. The resulting simultaneous hit progression is exactly
n = b + qf (k + pj),

j ≥ 0,

Dn − A = pqf,A (m0 + Hj).

(9.6)

Its initial representative belongs to [1, pqf ], so the allowable j’s in 1 ≤ n ≤ Y form an initial
integer interval of length Y /(pqf ) + O(1).
An included endpoint has Jd ≥ wa⋆ . The within-box movement of logw Jd is at most
∆, by Theorem 7.2. Taking ∆ < a⋆ /4, every endpoint choice in the full box therefore has
Jd ≥ w3a⋆ /4 . Set
⌋
⌊
Y
J=
,
J = {0, . . . , J − 1}.
(1 + ξ)Rqf
Since p ≤ (1 + ξ)R and the initial representative lies in [1, pqf ], this interval is contained in
every allowed j-interval. Its cardinality satisfies
J≍

Y
,
Rqf

J ≥ wa⋆ /2+δ0 ,

(9.7)

where, for example, one can take δ0 = a⋆ /8 for large z. The symmetric difference has length
O(ξJ + 1). An enclosing progression piece of length comparable to ξJ has, by Theorem 2.3,
at most O(ξJV0 ) small-prime survivors. For fixed ξ > 0, its length eventually exceeds wa⋆ /2 ;
this is why the slack in (9.7) is retained. The constant in this survivor bound is independent
of sufficiently small fixed ξ, although the eventual threshold may depend on it. The reference
count changes by O(ξJV0 ) as well. Consequently, when ξ is small relative to a fixed ε > 0, it
suffices to control
ε
|S − JV0 | > JV0 ,
(9.8)
2
where S counts the small-prime survivors on J .
For a prime t ≤ w, the avoidance condition on J is
{

pqf,A (m0 + Hj) ̸≡ Dat − A (mod t),
k + pj ̸≡ (at − b)qf (mod t),
54

t ∤ H,
t | H.

(9.9)

## PDF page 55

In the first line t ∤ D, so multiplication by D is reversible. In the second line qf is invertible
modulo t. All factors of qf exceed w; hence the primes t ≤ w dividing H are precisely the
small primes dividing D. Put
T0 =

∏

t,

∏

T1 =

t.

(9.10)

T0 T1 = exp(O(w)) = Ro(1) .

(9.11)

t≤w
t|H

t≤w
t∤H

Thus (T1 , HT0 ) = 1, every prime of T0 divides H, and

9.2

Variance of independent classes

The next second-moment argument is a truncated, two-point form of mean-one singular-series
averaging; compare Gallagher [8, equation (3) and Section 2]. We include the proof to
establish the uniform range of interval lengths and the stability under changes of measure
needed below.
Lemma 9.1. Choose, independently at each prime t ≤ w, one uniformly distributed forbidden
residue class. Let S count the integers in an interval J of cardinality J that avoid all these
classes. For every fixed δ > 0, uniformly for J ≥ wδ ,
E(S − JV0 )2 = o((JV0 )2 )

ES = JV0 ,

(w −→ ∞).

The assertion has the following stable version. Let µ be a finite positive measure carrying
∑
indicators Ij , j ∈ J , and let S = j Ij . Suppose, with an absolute fixed implied constant,
∫

µ(Ω) = 1 + O(ζ),

Ij dµ = V0 (1 + O(ζ)),

and, for distinct i, j, the joint probability has the upper bound
∫

Ii Ij dµ ≤ (1 + O(ζ)) Pind (Ii = Ij = 1).

Here Pind denotes the independent forbidden-class model in the first part of the lemma. A
zero probability on the right requires exact zero on the left. For 0 ≤ ζ ≤ 1/2,
∫

(S − JV0 )2 dµ ≪ ζ + o(1) (JV0 )2 ,
(

)

uniformly in the same range of J.
Proof. The single-point survival probability is V0 . For a nonzero spacing h, the pair probability
divided by V02 equals
212|h

∏ (
2<t≤w

1
1−
(t − 1)2

1
1+
.
t−2

) ∏ (
2<t≤w
t|h

)

(9.12)

At t | h the two positions have one forbidden residue between them; at t ∤ h they have two.
This proves the formula, including the parity factor.
Expand the last product in (9.12) over odd squarefree l, with coefficients
λl =

1
.
t
−
2
t|l

∏

55

## PDF page 56

For each fixed l, the triangular average of 212l|h is
∑ 2(J − h)

J2

1≤h<J

1
212l|h −→ .
l

The same average is O(1/l) for every l, J. Moreover,
∏
λl
1
=
1+
l
t(t − 2)
t>2
(

∑
l≥1
l odd and squarefree

)

< ∞.

Dominated convergence applies even though the available primes increase with w. The
limiting triangular average of (9.12) is 1, because
∏(
t>2

1
1−
(t − 1)2

1
1+
t(t − 2)

)∏(
t>2

)

= 1.

The convergence is uniform for J ≥ wδ : first truncate the convergent divisor series at fixed l,
and then use J → ∞ uniformly in this range. The diagonal contribution to ES 2 /(JV0 )2 is
1/(JV0 ) = o(1), by Mertens’ theorem. This proves the independent-model assertion.
For the stable version, sum the assumed pair upper bounds and the single-point bounds
to obtain
∫
S 2 dµ ≤ (1 + O(ζ) + o(1))(JV0 )2 .
Use also the lower bound for
∫

∫

S dµ and the upper bound for µ(Ω) in the identity

(S − JV0 )2 dµ =

∫

S 2 dµ − 2JV0

∫

S dµ + (JV0 )2 µ(Ω).

This gives the stated result without normalizing µ.

9.3

The effective-size alternative

Proposition 9.2. Fix the compact-box parameters, the inverse-estimate parameters and a
relative-error threshold ε > 0. For every fixed σ2 > 0 there is a fixed sufficiently large Cs ,
independent of sufficiently small fixed ξ, with the following property. For every candidate
box, every choice of its factors other than the isolated prime, and every rational on its fixed
candidate list for which (9.1) holds, suppose
T > w Cs .
For sufficiently large z, fewer than σ2 np primes p ∈ P both align to A/D and satisfy
|Npqf /µpqf − 1| > ε.
The estimate is uniform in the box, the fixed prime choices, the rational and the forbidden
classes. The threshold on z may depend on fixed ξ. The fraction is measured against all
primes of P.
Proof. It is enough to impose the aligned hit at every p hypothetically and bound (9.8). The
primes dividing H may be discarded: there are O(1) of them in P, since H ≤ RZ 11 , and
their fraction tends to zero. For H ≤ R4/5 , Brun–Titchmarsh controls each residue pattern
after we fix m0 : the possible primes lie in a progression of modulus HT0 T1 . The condition
that T is large then gives a long enough interval in m0 for its small-prime conditions to
have the required first and second moments. For larger H, we instead count integer pairs
(p, m0 ) on a modular hyperbola and then sieve the p-coordinate. This gives domination by
the uniform distribution on all small-prime patterns. In both ranges the target is a small
exceptional fraction among all primes of the isolated bin.
56

## PDF page 57

The range H ≤ R4/5 . As p varies in P, the coordinate m0 lies in an enclosing interval I
of length
Y1 ≍ H + ξ|C0 |/R,
(m0 , H) = 1.
(9.13)
For a fixed m0 , possible p’s lie in an interval of length at most a constant times
(

R2 H
X1 = min ξR,
|C0 |

)

,

using the first entry if C0 = 0. Indeed, C0 /p must lie in an interval of length H, while its
derivative has magnitude comparable to |C0 |/R2 on the bin. This argument is unchanged
when C0 is negative. Writing c = |C0 |/R, the two cases c ≤ H/ξ and c > H/ξ give
X1 Y1 ≪ ξRH,

Y1 ≫ ξT,

X1 ≥ R/Z O(1) .

(9.14)

The last inequality follows from (9.4); fixed factors depending on ξ are harmless here.
Specify a unit pattern for p mod T1 and an arbitrary pattern for k mod T0 . Together with
fixed m0 , these conditions specify one unit class for p modulo HT0 T1 : the condition at HT0 is
pm0 ≡ C0 + Hk

(mod HT0 ).

Both m0 and the right side are units modulo HT0 , and T1 is coprime to this modulus. In
particular,
φ(HT0 T1 ) = φ(H)T0 φ(T1 ).
Since HT0 T1 ≤ R4/5+o(1) and X1 = R1−o(1) , Brun–Titchmarsh, in the form of Theorem 2.2,
bounds the number of primes for each such choice by
≪

X1
.
log R φ(H)T0 φ(T1 )

(9.15)

We may enclose a shorter actual interval by one of the displayed upper-bound length before
applying the theorem.
Define a positive measure on choices consisting of an integer m ∈ I, (m, H) = 1, a unit
p-pattern modulo T1 , and an arbitrary k-pattern modulo T0 , as follows:
weight of each m =

H
,
φ(H)Y1

p mod T1 and k mod T0 independent and uniform. (9.16)

The number of the latter patterns is T0 φ(T1 ). Dividing (9.15) by np ≫ ξR/ log R, and using
(9.14), shows that the fraction of actual primes whose associated choices lie in any event is at
most a fixed absolute constant times the measure of that event. This constant is independent
of sufficiently small fixed ξ. Each actual prime has one associated m0 , so this upper count
introduces no missing multiplicity.
We verify the hypotheses of the stable part of Theorem 9.1 for the measure (9.16). Take
one or two fixed j’s and let νt ∈ {1, 2} be the number of their distinct residues modulo t. At
t | T0 , reducing the congruence for p modulo t shows that p mod t is already determined by
m, independently of the lift k mod t. Uniform k mod t in the second line of (9.9) therefore
gives exactly the joint factor 1 − νt /t.
At primes t | T1 , condition on the unit pattern p mod T1 . The first line of (9.9), as
a condition on m, excludes exactly νt residue classes, since H is invertible there. For a
squarefree product l of these primes, counting the intersection of its bad classes together with
(m, H) = 1 gives


Y1

∏
φ(H) ∏ νt
+ O τ (H)
νt  .
H t|l t
t|l

57

(9.17)

## PDF page 58

To see this, expand the coprimality condition over squarefree divisors of H. Each chosen
combination of classes modulo l combines with each divisor condition by CRT, because
(l, H) = 1; the interval count has error O(1). This gives both the main term and the error in
(9.17).
Fix a small ζ > 0. Apply Theorem 2.1 at level wA1 , first choosing the fixed A1 large
enough that its fundamental-lemma error is smaller than a prescribed constant times ζ. If a
local product is zero, the conditions are exactly empty and need no sieve estimate. Otherwise
the possible prime 2 has density at most 1/2, and all other densities are at most 2/t, as
required. For some fixed M > 0, chosen after A1 , the remainder sum is O(τ (H)wM ). Since
H ≪ Y1 , the elementary divisor and totient bounds give
τ (H)

H
1/4
≪ Y1 .
φ(H)

Every nonzero surviving product is ≫ (log w)−2 . Thus the relative remainder is bounded by
a constant times
τ (H)H M
−3/4 M
w (log w)2 ≪ Y1
w (log w)2
Y1 φ(H)
≪ξ wM −3Cs /4 (log w)2 = o(1),
because Y1 ≫ ξT > ξwCs and we may choose Cs > 2M + 10. Thus A1 , then M , then Cs
are fixed before the eventual choice of ξ. These estimates are uniform in the pattern, the
positions, the interval location and H; a fixed small ξ changes only the threshold on z.
After multiplication by the normalization in (9.16), the single-point and pair probabilities
thus equal their independent-model values with relative error O(ζ) + o(1), whenever those
values are nonzero. Factors at T0 are exact. The total mass is 1 + o(1), either by the same
argument with no bad classes or by the elementary count
#{m ∈ I : (m, H) = 1} = Y1 φ(H)/H + O(τ (H)).
The stable variance lemma and Chebyshev’s inequality show that the measure of (9.8) is
Oε (ζ) + o(1). Choose ζ sufficiently small in terms of σ2 , ε and the domination constant. This
proves the desired prime fraction bound in the first range.
The range R4/5 < H ≤ RZ 11 . Partition P’s real bin into equal-length blocks so that the
variation of C0 /p in each block is at most H. By (9.4), this requires at most Z O(1) = Ro(1)
blocks. For a block of length X, the possible m0 ’s lie in an interval of length Y2 ≤ 3H. We
upper count all pairs in this rectangle with a full small-prime pattern
p ≡ p0

(mod T0 ),

k ≡ k0

p ≡ p1

(mod T0 ),

(mod T1 ),

m0 ≡ m1

(mod T1 ),
(9.18)

where p0 , p1 are units and k0 , m1 are arbitrary. The number of such patterns is
Mpat = T0 φ(T0 )T1 φ(T1 ) = Ro(1) .

(9.19)

Set N = HT0 . The hyperbola congruence on this rectangle is
pm0 ≡ C0 + Hk0

(mod N ).

Its right side is a unit by (9.3).
For any squarefree l ≤ R1/10 coprime to HT1 , the completion lemma proved in the
appendix, Theorem A.1, gives the count with l | p as
XY2 φ(N )
+ O(R7/10+o(1) ).
lT12 N 2 φ(T0 )
58

(9.20)

## PDF page 59

This is uniform in the block, its location, the pattern and l. For clarity about the exponent,
the lemma’s explicit error is bounded by
N

1/2+o(1)

1/2
T0

(

X
Y2
.
1+
+
N
N
)

Since R4/5 < N ≤ R1+o(1) , X ≪ R, Y2 ≤ 3H ≤ 3N , and T0 = Ro(1) , this is in fact
O(R3/5+o(1) ). We use the weaker error in (9.20) to leave slack in subsequent sums.
Sieve the p-coordinate of this nonnegative sequence of pairs for an upper bound on primes.
Exclude primes at most Rc6 not dividing HT1 , where fixed c6 > 0 is sufficiently small, and
use level R1/10 in Theorem 2.1. The intersection density supplied by (9.20) is 1/l. The primes
dividing HT1 are already excluded from the p-coordinate by the unit conditions. The main
sieve product is at most
1
H
T1
≪
.
(9.21)
log R φ(H) φ(T1 )
Including factors of H larger than the sieve cutoff only increases this upper bound. The
fundamental-lemma parameter is (1/10)/c6 , so a fixed small choice of c6 suffices.
The weighted sum of the errors in (9.20) over l ≤ R1/10 is R4/5+o(1) , and in particular is
O(R9/10 ) for large z. Because every prime of T0 divides H, φ(N ) = φ(H)T0 . Multiplying the
main term at l = 1 by (9.21) and using Y2 ≤ 3H therefore gives, for each pattern and block,
≪

X
+ O(R9/10 ).
log R T0 φ(T0 )T1 φ(T1 )

(9.22)

There are Ro(1) blocks and Ro(1) patterns, so all error terms together are
R9/10+o(1) = o(np ).
Here division by np ≍ ξR/ log R is harmless for each fixed ξ > 0. Summing the main term
∑
over the blocks uses X ≍ ξR. Thus the fraction of actual primes associated to any set of
bad full patterns is bounded by a fixed constant times its fraction among all Mpat patterns,
plus o(1). The bound counts pairs, which is sufficient: every actual prime has exactly one m0
from (9.5).
Under independent uniform choices in (9.18), the forbidden j-classes in (9.9) are exactly
independent and uniform. Conditional on the unit patterns, use uniform k0 mod t at each
t | T0 ; at the other primes use uniform m1 mod t. The coefficients of these variables are units.
CRT supplies independence across the primes. The event (9.8) depends only on this full
pattern and on the already fixed J , qf , A, D, b. By Theorem 9.1, its uniform-pattern fraction
is o(1). The domination just proved gives the required prime fraction bound in the second
range.
Finally, the first range chose ζ, then A1 , then Cs ; the second range needs no further
increase of Cs . These choices are independent of sufficiently small fixed ξ. Choose ξ small
enough for the earlier interval freezing and then let z tend to infinity. This proves all asserted
uniformities.

9.4

Hard endpoints and global eligibility

Corollary 9.3. Fix the compact range and ε > 0. For every prescribed positive ρ, the inverse
exception parameter and then the variance exception parameter can be chosen so that, for
a fixed Cs independent of sufficiently small fixed ξ, the following holds for all sufficiently
large z. Consider the actual included regular compact endpoints covered by the full boxes of

59

## PDF page 60

Theorem 7.2. Except for a set of these endpoints of total harmonic mass at most ρB −2 , every
such bad endpoint
|Nd /µd − 1| > ε
has a witnessing candidate and a rational on that candidate’s fixed list for which the parent is
structured, the isolated prime aligns, and
Dqf,E ≤ wCs ,

|C0 |/R ≤ wCs .

(9.23)

For each such endpoint all its prime factors with exponent x(t) > Cs align to this same
rational, including the isolated prime. The rational satisfies the global bounds
D ≤ wCs ,

|A| ≤ Y wCs +2 .

(9.24)

The enlarged full boxes are used only to dominate measure: the assertion concerns the actual
included endpoints, rather than every tuple in those enlarged boxes. The exceptional mass can
be bounded before choosing ξ; only the eventual threshold on z is allowed to depend on fixed ξ.
Proof. Every actual included bad endpoint under consideration has a witness from the
bounded candidate set, by Theorems 7.1 and 7.2. For each candidate, Theorem 8.2 costs at
most a prescribed σ fraction of its full harmonic box and supplies a fixed list of at most F
rationals. Both F and the list definition are independent of the choice of the isolated prime.
To apply Theorem 9.2, fix all the other prime choices and one rational on this list. Then
H, C0 , T are fixed as p varies. If the structured-parent condition is possible in this slice, (9.1)
holds throughout the fixed slice. When T > wCs , the proposition bounds all bad aligning p’s,
and hence also those that supply the particular witness. Since the isolated bin has multiplicity
one, its prime choice is independent of all the other bin choices in full-box measure. The
weights 1/p vary by a bounded factor within this bin, uniformly for sufficiently small ξ.
Therefore the count bound σ2 np converts to at most Cσ2 of its harmonic measure, with fixed
C.
Union over the list and over the at most He candidates bounds the discarded fraction of
each full box by
He (σ + CF σ2 ).
′ B −2 , where C ′ is independent of sufficiently small
The total enlarged-box mass is at most CK
K
ξ, by Theorem 7.2. First choose σ sufficiently small; this fixes F . Then choose σ2 sufficiently
small in terms of F and ρ, and finally choose Cs from Theorem 9.2. This makes the discarded
mass at most ρB −2 , without multiplying by the number of boxes. For every remaining bad
endpoint, some structured rational has T ≤ wCs , which is (9.23).
The bound on H controls the nonaligned factors. Each nonaligned prime factor of qf
divides qf,E ≤ wCs , so it is at most wCs . The isolated prime already aligns by the structuredparent conclusion; its exponent tends to infinity, and in particular exceeds Cs . This proves
the alignment assertion. The bound on |C0 |/R controls the numerator of the rational on a
scale common to all boxes. We have b ≤ qf , qf,A ≤ qf , R ≤ p, and pqf = d ≤ Y , since these
are included endpoints with Jd > 1. Consequently,

|A| ≤ Dqf + |C0 |qf,A ≤ wCs qf (1 + R) ≤ 2Y wCs .
This implies the second inequality of (9.24) for large z; the first follows directly from (9.23).

10

Stops for endpoints with small effective size

The inverse and variance estimates leave compact endpoints whose large prime factors all
align to a rational of small effective size. We now stop the tree earlier on such branches. At
60

## PDF page 61

these stops we compare the exact survivor counts with their reference subtrees after averaging
over one large prime. All prime cutoffs at a nonempty node in this section are strict: if its
last prime is P , the local survivor count avoids the forbidden classes at the primes t < P .
Fix the exponent Cs supplied by Theorem 9.3. The parameters of the regular boxes,
including Clen , are also regarded as fixed. The bin width ξ will be chosen sufficiently small
only after the other fixed parameters of this section. As before, let h ≍ ξ/ log w be the
exponent width of a bin and put
∆ = 2Clen ξ.
The representative of a bin is its right endpoint in exponent coordinates. By Theorem 7.2,
the movement of any prefix gap within a box of length at most Clen log B is at most ∆, for
sufficiently large z.

10.1

Owners, tags, and a stopping rule

Definition 10.1. A reduced rational A/D, with D > 0, is eligible if
D ≤ wCs ,

|A| ≤ Y wCs +2 .

(10.1)

Fix a constant η > 0, to be bounded by an absolute constant below. A search bin has an
owner if some eligible rational aligns to at least a 1 − η fraction of its primes, by prime
count. The owner is that rational. Along a descending-prime path, its tag prime is the first
search-bin factor that aligns to the owner of its bin, if such a factor occurs. Its tag rational is
this owner and is retained for the rest of the path.
The owner is unique for all sufficiently large z, provided η < 1/2. Indeed, if A1 /D1 ̸=
A2 /D2 are eligible, every prime aligning to both divides the nonzero integer A1 D2 − A2 D1 ,
whose absolute value is at most
2Y w2Cs +2 = z 2+o(1) .
Consequently, in a bin with lower prime endpoint R, their common aligning primes number
at most
)
(
L
+1 .
(10.2)
O
log R
For a search bin, log R ≥ w1/4 log w, while its prime count is ≍ ξR/ log R. The bound in
(10.2) is a uniformly negligible fraction of this count. Two subsets of relative size at least
1 − η would have an intersection of relative size at least 1 − 2η, proving uniqueness. Also,
every prime of a search bin eventually exceeds every eligible denominator.
Choose fixed constants b0 , b1 with b1 > b0 , taking b0 sufficiently large compared with
Cs + 1. Further conditions on these constants will be stated below. For a prefix with bin
rep
representatives xrep
1 , . . . , xj , write
rjrep = r0 −

j
∑
rep

xi .

i=1

Definition 10.2. An included, nonempty, even node is a stop if it is the first node along its
branch satisfying all the following conditions:
(i) Its length is at most Clen log B. Its tag has been attained, the tag bin has multiplicity
one in this prefix, and every prime of the prefix aligns to its tag rational.
(ii) Every nonempty even prefix ending at position j satisfies
rjrep ≥ H(xrep
j ) + 3∆.
61

(10.3)

## PDF page 62

(iii) At the present node, its last representative exponent and representative ratio satisfy
b0 ≤ xrep
j ≤ b1 ,

2.06 ≤ rjrep /xrep
j ≤ 2.16.

(10.4)

The empty root is not subjected to (10.3).
This is a prefix-free choice of lower nodes. The rule applies to the entire included tree;
the inverse and variance exceptions classify endpoints but do not restrict this rule. The
representative safety condition ensures that varying prime choices inside their bins, while
preserving multiplicities and distinctness, preserves admission of all even prefixes by (3.3).
One may see this directly from the right-endpoint convention: the actual gap is at least the
representative gap and the actual last exponent is at most its representative. Alternatively,
the movement bound and the 2-Lipschitz property of H give the same conclusion with room
to spare. Odd children of lower nodes require no admission test.
For sufficiently small fixed ξ, every stop has actual last exponent b and actual ratio
satisfying
b0 − o(1) ≤ b ≤ b1 ,
2.04 ≤ rd /b ≤ 2.18.
(10.5)
Here and throughout this section, the eventual bounds may depend on all the fixed constants,
including ξ. The tag prime lies in a search bin, whose exponent tends to infinity. Thus it is
different from the last prime P = wb at every stop, once z is sufficiently large.

10.2

The average over a large prime bin

At a stop, we will fix all prime factors except the tag prime. The arithmetic estimate below
first lets that prime range over its whole bin, imposing the aligned hit class even where the
actual class does not align. Its lower average and absolute individual upper bound will then
permit removal of the small nonaligning subset.
For a prime P , write
)
∏(
1
,
Vall (P ) =
1−
t
t<P
where t ranges over primes.
Lemma 10.3 (Average for an aligned progression family). Fix Cs . Take b0 sufficiently large
in terms of Cs , and let b1 > b0 be fixed. For every sufficiently small fixed ξ > 0, the following
holds for all sufficiently large z. Let A/D be eligible in the sense of (10.1), let P = wb be a
prime with b ∈ [b0 − 1, b1 ], and let q ′ be a squarefree product of primes at most z whose least
prime factor is P and all of whose prime factors align to A/D. Let P be a search bin, none
of whose primes divides q ′ . Suppose that, for every p ∈ P,
Jp =

Y
,
pq ′

2.03 ≤ logP Jp ≤ 2.19.

(10.6)

Define Tp to count the integers 1 ≤ n ≤ Y satisfying Dn ≡ A (mod pq ′ ) and avoiding the
prescribed classes at every prime t < P . Then
∑

Tp ≥ .39Vall (P )

p∈P

∑

Jp .

(10.7)

p∈P

There is also an absolute constant CU , independent of Cs , b0 , b1 and of sufficiently small fixed
ξ, such that
Tp ≤ CU Jp Vall (P )
(p ∈ P).
(10.8)
Both estimates are uniform in the eligible rational, the bin, the product q ′ , and the prescribed
residue classes.
62

## PDF page 63

The lower-bound proof writes Dn − A = pq ′ m and counts integers m = ±d0 ℓ′ with
d0 ≤ P .95 and ℓ′ > P prime. The prime factors of d0 are chosen among the nonaligned
primes less than P that do not divide D. For such a prime t, divisibility of d0 by t makes the
avoidance condition automatic; otherwise one of the t − 1 unit classes for the varying prime
is forbidden. We isolate the resulting estimate before proving the arithmetic lemma. For any
subset E of the primes less than P , put
)
∏(
1
WE (d0 ) =
1−
.
(10.9)
t−1
t∈E
t∤d0

The next lemma is uniform in E, including when 2 ∈ E.
Lemma 10.4. Uniformly over all subsets E of the primes less than P ,
WE (d0 )
≥ e−γ (.94 − o(1)).
d
0
.95

∑

(10.10)

d0 ≤P
t|d0 ⇒t∈E

Proof. For t ∈ E, let Vt be independent nonnegative integer-valued random variables with
probabilities
t−2
P(Vt = 0) =
,
P(Vt = j) = t−j (j ≥ 1).
t−1
∏
These masses sum to one, and the probability that t∈E tVt = d0 is exactly WE (d0 )/d0 . This
∑
interpretation includes t = 2: the mass at zero is then zero and j≥1 2−j = 1. In particular
the zero factors in (10.9) cause no exception to the probability interpretation.
Let Ut instead have the ordinary geometric probabilities P(Ut = j) = (1 − 1/t)t−j for
j ≥ 0. For j ≥ 1,
t1−j
≥ t−j = P(Ut ≥ j).
P(Vt ≥ j) =
t−1
Couple Ut , Vt monotonically, independently over t. Their mean difference is
t
1
1
E(Vt − Ut ) =
−
=
.
(t − 1)2 t − 1
(t − 1)2
It follows that the excess log-product ZE = t∈E (Vt − Ut ) log t has uniformly bounded mean,
∑
since t log t/(t − 1)2 < ∞. Extend the independent ordinary variables to all primes t < P .
Then
∏
∏
t Ut ≤
tUt .
∑

t∈E

t<P

The latter product has mass Vall (P )/n at every integer n composed of primes below P . Every
n ≤ P .94 has this property, so
(

P

)
∏

Ut

t

≤P

.94

t<P

1
= e−γ (.94 + o(1)).
n
.94

∑

= Vall (P )

n≤P

By Markov’s inequality, P(ZE > .01 log P ) = O(1/ log P ), uniformly in E. Outside this
∏
exception the preceding event implies t∈E tVt ≤ P .95 . Subtracting the exceptional probability
proves (10.10); no independence between these last two events is required.
Proof of Theorem 10.3. Every prime in the search bin eventually exceeds both D and P . The
alignment of the prime factors of q ′ implies (D, q ′ ) = 1; hence (D, pq ′ ) = 1 for every p ∈ P.
The hypothetical hit condition and integrality of n are therefore equivalent to
A + pq ′ m
≤ Y,
pq ′ m ≡ −A (mod D).
(10.11)
D
We count a subfamily of these integers in which m has one prime factor exceeding P . Averaging
over p then imposes the remaining avoidance conditions.
Dn − A = pq ′ m,

1≤

63

## PDF page 64

A common interval for the auxiliary integer. Partition P into ⌈w2Cs +10 ⌉ equal-length
subbins in prime coordinates. In one such subbin let R′ be its lower endpoint, let V be its
length, and put
Y
s◦ = logP J ◦ .
J◦ = ′ ′ ,
Rq
Uniformly over these subbins,
V
≍ ξw−2Cs −10 ,
R′

Jp = J ◦ (1 + o(1)).

(10.12)

Let I be the intersection, over the real values of p in the subbin, of the real m-intervals
specified by the middle condition in (10.11). The endpoints of one such interval are
DY − A
.
pq ′

D−A
,
pq ′

Relative to DJ ◦ , the variation of either endpoint is at most
(

(

O ξw−2Cs −10 1 +

|A|
DY

))

= o(1),

by (10.1). Consequently
|I| = (1 − o(1))DJ ◦ .

(10.13)

The height of this interval satisfies
◦

sup |m| ≤ (D + |A|/Y )J ◦ (1 + o(1)) ≤ P s +.02 ,
m∈I

provided b0 is sufficiently large in terms of Cs . Indeed the extra factor is bounded by a
constant times wCs +2 , which is absorbed by P .02 after such a choice. All these statements
are uniform in the aligned progression family, its eligible rational, and the subbin.
Among primes t < P , distinguish those aligning to A/D from those not aligning. Let E
be the set of nonaligned primes t < P that do not divide D. We count only integers of the
form
m = ±d0 ℓ′ ,
d0 ≤ P .95 ,
t | d0 =⇒ t ∈ E,
ℓ′ > P prime,
(10.14)
with m ∈ I. Such a representation is unique: its factor d0 is less than P , while the
distinguished prime factor is greater than P . Furthermore, (m, D) = 1, since d0 has no prime
factor dividing D, and D < P < ℓ′ . If t < P aligns to A/D, then t divides neither d0 nor ℓ′ ,
so t ∤ m, exactly as required to avoid the class at this aligned prime.
For each permitted d0 , the number of integers (10.14) in I, counting both signs, is at least
(1 − o(1))

|I|
d0 (s◦ + .02) log P

.

(10.15)

Here the error tends to zero uniformly in d0 , E, and all the other data. To prove this, split I
into its positive and negative absolute-value pieces. Remove |m| < P −.02 |I|, and discard any
remaining sign piece shorter than P −.02 |I|. The total removed length is O(P −.02 |I|). After
division by d0 , every retained interval has lower endpoint at least
P −.02 |I|
◦
≥ (1 − o(1))DP s −.97 > P 1.04 ,
d0
using (10.6) and (10.13). Its length divided by its upper endpoint is at least (1 − o(1))DP −.04 ,
and hence at least P −.05 . If its upper endpoint is v, then v > P 1.04 implies
vP −.05 ≥ v 9/10 .
64

## PDF page 65

The uniform short-interval prime number theorem in Theorem 2.2 therefore applies. Every
upper endpoint has logarithm at most (s◦ + .02) log P . Summing the resulting lower bounds
for the retained sign pieces proves (10.15). In particular their prime factors automatically
exceed P .
Sieving the varying prime. Fix one of the integers m just counted. The last congruence
in (10.11) prescribes a single unit class for p modulo D. This uses (A, D) = (q ′ m, D) = 1.
For each prime t | D, increasing p by D changes the integer n by q ′ m, which is a unit modulo
t. Thus avoiding at removes exactly one of the t lifts of this base class modulo Dt. Taken
together, the remaining classes modulo
Q = D rad(D)
form a set A of φ(rad(D)) unit classes. Since φ(Q) = φ(D) rad(D), their proportion among
all unit classes modulo Q is exactly
|A|
1
= .
φ(Q)
D

(10.16)

For D = 1 this means the single unrestricted class and the same formula holds.
For t ∈ E, avoiding the original class is equivalent to
pq ′ m ̸≡ Dat − A

(mod t),

with nonzero right side. If t | d0 , this is automatic. If t ∤ d0 , then m is a unit modulo t
because ℓ′ > P , and exactly one nonzero p-class modulo t is forbidden. Thus the product of
the remaining survival factors is WE (d0 ) from (10.9). Let NI be the number of primes in the
present subbin I. We claim that for any fixed γ1 > 0, for all sufficiently large z,
NI
WE (d0 ),
(10.17)
D
uniformly in all the data. If the product vanishes, the claim is trivial. In every other case, the
restricted primes are at least 3; their sieve densities g(t) = 1/(t − 1) satisfy the hypotheses of
Theorem 2.1.
Here are the required progression and remainder bounds. Choose a fixed A2 large enough,
in terms of γ1 , to make the relative fundamental-lemma error small, and use sieve level
S = P A2 . For a squarefree intersection modulus l ≤ S on the restricted primes and one class
in A, the forbidden conditions specify a single reduced class modulo Ql, since (l, Q) = 1.
Siegel–Walfisz from Theorem 2.2 gives its count as
#{p ∈ I : p gives a local survivor for this m} ≥ (1 − γ1 )

li(R′ + V ) − li(R′ )
+ O M2
φ(Q)φ(l)

(

R′
(log R′ )M2

)

.

The exponent M2 can be any sufficiently large fixed constant. To check the modulus range,
observe that
Q ≤ w2Cs ,

|A| ≤ wCs ,

S ≤ wb1 A2 ,

log R′ ≥ w1/4 log w.

(10.18)

Thus Ql, the level, and the lift count are each bounded by fixed powers of log R′ . The
main term, for each base class, has the required multiplicative intersection density 1/φ(l) =
∏
t|l 1/(t − 1).
For completeness, let C be the fixed divisor-weight exponent in the remainder of The∑
orem 2.1. Summing over lifts and using the crude bound l≤S τ (l)C ≪ S C+1 , the total
remainder is at most
(
)
R′
C+1
OM2 |A|S
.
(log R′ )M2
65

## PDF page 66

In a nonzero case, uniformly over subsets of restricted primes,
WE (d0 ) ≫

1
.
log P

Indeed the product over all 3 ≤ t < P is of this order, by Mertens’ theorem and the convergent
positive product in the identity
1
1
1−
= 1−
t−1
t
(

)(

1
1−
.
(t − 1)2
)

Also NI ≍ V / log R′ , uniformly by the same prime number theorem, or by Siegel–Walfisz with
modulus one. Write κ = 2Cs + 10. The ratio of the displayed remainder to (NI /D)WE (d0 )
is consequently at most
(

OM2 ,ξ

D|A|wκ S C+1 log P
(log R′ )M2 −1

)

≪M2 ,ξ

w4Cs +10+(C+1)b1 A2 log P
= o(1)
(log R′ )M2 −1

on taking M2 sufficiently large in terms of the fixed constants. This also justifies subtracting
the two endpoint estimates for the short subbin. The logarithmic-integral main term can be
replaced by NI with relative error o(1). Finally use (10.16), and take the fundamental-lemma
relative error sufficiently small compared with γ1 . This proves (10.17). Its error bound is
uniform in m; large values of m change only reduced residue classes.
Summing the lower bound and bounding an individual count. For each d0 , first
count the integers m using (10.15), and for each such m count its admissible varying primes
using (10.17). A pair (p, m) determines a unique integer n by (10.11). Unique factorization
in (10.14) prevents duplicate counting for fixed p. Hence Theorem 10.4 and (10.13) give, in
one subbin,
∑
NI J ◦
Tp ≥ (1 − γ1 − o(1)) ◦
e−γ (.94 − o(1)).
(s
+
.02)
log
P
p∈I
Mertens’ theorem gives Vall (P ) ∼ e−γ / log P . We have s◦ + .02 ≤ 2.22 eventually, and
.94
> .423.
2.22
Choose γ1 as a sufficiently small absolute constant; for example γ1 = .05 leaves a limiting
coefficient greater than .402. Since Jp = J ◦ (1 + o(1)) uniformly within a subbin, summing
over all subbins proves (10.7). All relative errors used here are uniform, so the growing
number of subbins and the number of pairs (d0 , m) do not accumulate additional errors.
For the upper bound, the hit conditions give one ordinary progression of step pq ′ and
coordinate length Jp + O(1). Every sieve prime below P is coprime to this step. Apply the
upper form of Theorem 2.1 using primes up to P θ , for a sufficiently small fixed absolute
θ > 0, and a level such as P 1/2 . The relative sieve parameter is a sufficiently large absolute
constant; the summed O(1) intersection remainders are P 1/2+o(1) , whereas Jp ≥ P 2 . Mertens’
theorem gives
∏
(1 − 1/t) ≪θ Vall (P ).
t<P θ

This proves (10.8) with an absolute CU , independent of Cs , b0 , b1 and of sufficiently small ξ.

66

## PDF page 67

10.3

Comparison at the actual stops

The preceding lemma averages over every prime in a bin. To apply it to actual stops, we must
show that fixing the other prime factors leaves the entire owner-aligning subset available.
This is the role of the representative tests in the stop rule.
Proposition 10.5 (Comparison at stops). There is an absolute constant η0 > 0 with the
following property. Fix Cs and the regular-box parameters. Take 0 < η ≤ η0 , then take b0
sufficiently large in terms of Cs , and take any fixed b1 > b0 . For all sufficiently small fixed
ξ > 0 and all sufficiently large z, the stops of Theorem 10.2 satisfy
∑
d stopped

∑

Sd (x(Pd )) ≥

µd Pe (rd , x(Pd )),

(10.19)

d stopped

where Pd denotes the last prime of the tuple and both cutoffs are strict below Pd .
Proof. We first explain exactly which prime is averaged. Partition the stopped nodes by their
ordered bin labels, their tag position, and all prime choices other than the tag prime p. In a
nonempty group, let A/D be the owner of its tag bin. Then p ranges over the entire subset
of that bin aligning to A/D.
To justify this assertion, replace p by any other aligning prime in the bin. All earlier
choices remain fixed, so no earlier tag appears. At the designated position the new prime
aligns to the same owner; hence the tag position and tag rational remain unchanged. Every
subsequent all-prefix alignment test has the same truth value, since the other primes are
fixed and the replacement aligns. The representative tests, lengths, and bin multiplicities
depend only on the labels. Admission is preserved by (10.3), and the tag-bin multiplicity one
prevents a change in prime ordering or a collision with another factor. These observations
apply to each earlier prefix as well, so no earlier stop is introduced. This proves the assertion
about the entire aligning subset.
In this group put q ′ = d/p. The last prime P is a factor of q ′ and is fixed. All primes of
q ′ are at least P , and they align to A/D. First allow all primes p in the tag bin, assigning to
p the hypothetical hit class aligned to A/D. These hypothetical choices need not be actual
stops; their local counts are auxiliary. Let P denote this tag bin, and use the hypothetical
counts Tp of Theorem 10.3. On its aligning subset, Tp = Spq′ (x(P )).
For all choices of p in the tag bin, put b = x(P ) and use the gap rpq′ = logw (Y /(pq ′ ))−a⋆ +2.
Thus
rpq′
a⋆ − 2
logP Jp =
+
.
b
b
The bin labels and representative safety tests are fixed, so the movement bound applies also to
these hypothetical choices. By (10.5), after enlarging b0 if necessary, all of them satisfy (10.6).
The search bin is disjoint from the prime factors of q ′ because the tag bin has multiplicity
one. All hypotheses of Theorem 10.3 therefore hold.
For sufficiently large z, the actual cutoff lies in the fixed interval [b0 − 1, b1 ]. Applying
Theorem 6.5 on this interval, together with the product identity Vall (P ) = V0 V (b), gives
µpq′ Pe (rpq′ , b)
≤ f (rpq′ /b) + O(1/b) + o(1).
Jp Vall (P )
The constants are uniform for the fixed enlarged window [b0 − 1, b1 ] and for the ratio window
in (10.5). On that ratio window, the near-2 formula and monotonicity of f give
f (rpq′ /b) ≤ f (2.18) <

67

2(1.95)(.166)
< .30.
2.18

## PDF page 68

Here eγ < 1.95 follows, for example, from γ ≤ 6j=1 j −1 − log 6 < .66, and log(1.18) < .166
follows from log(1 + u) ≤ u − u2 /2 + u3 /3 at u = .18. Thus first choosing b0 large and
subsequently taking z large gives
∑

µpq′ Pe (rpq′ , b) ≤ .33Jp Vall (P )

(10.20)

uniformly over the group and over its hypothetical choices.
Apply (10.7) to the full tag bin. Let G be the aligning subset in the tag bin. Its complement
contains at most an η fraction of the bin primes. Since the Jp ’s vary by at most 1 + ξ within
the whole bin, for ξ ≤ 1 we have
∑

∑

Tp ≤ 2CU ηVall (P )

Jp .

p in bin

p/
∈G

Fix an absolute η0 < 1/2 so small that 2CU η0 < .05. For 0 < η ≤ η0 , subtracting this bound
from (10.7) and using (10.20) gives
∑

Spq′ (x(P )) =

p∈G

∑

Tp

p∈G

≥ .34Vall (P )

∑

Jp

p in bin

≥

∑

µpq′ Pe (rpq′ , b).

p∈G

The last inequality uses .34 > .33 and positivity of Jp ; it does not require a distribution
hypothesis for the survivors inside the owner subset. Every stopped node belongs to exactly
one of the groups considered. Summing the group inequalities proves Theorem 10.5.

10.4

Almost every hard endpoint lies below a stop

We next explain why the same stops capture all but an arbitrarily small scaled harmonic
mass of the hard compact endpoints. In what follows, the harmonic mass of a family of tuples
∑
is d 1/d.
Proposition 10.6 (Stopping hard endpoints). Fix a compact gap bound K, the regularbox parameters, the bounded candidate lists from Theorem 8.2, and the exponent Cs from
Theorem 9.3. Fix 0 < η ≤ η0 as in Theorem 10.5. For every δ > 0, take b0 sufficiently large
in terms of Cs and K, then take b1 /b0 sufficiently large in terms of the desired error, and
finally take ξ sufficiently small. For these fixed choices, the regular included hard endpoints
with rd ≤ K having no stopped prefix have harmonic mass at most
(δ + o(1))B −2 .

(10.21)

The eventual o(1) may depend on all the fixed choices. In particular, b1 and ξ are fixed before
z tends to infinity.
Proof. For a hard endpoint, Theorem 9.3 gives a rational on one of its candidate lists that
satisfies (10.1) and aligns to every path factor of exponent greater than Cs . We need two
facts about this path: its tag must be this rational, and it must have an earlier even visit
in the stop window. We establish the tag statement in the full-box product measure, and
the visit statement in the unconditioned path process. Their exceptional masses will then be
added.
68

## PDF page 69

Identifying the tag. Except for o(B −2 ) mass, the path acquires this same rational as its
tag during its search positions, as we now show.
Fix one regular full candidate box and one eligible rational A/D on its list. Each of its
search bins has multiplicity one, and Theorem 7.2 supplies at least c7 log w such bins. For
clarity, the count follows because all nonsearch factors together decrease the gap by at most
Clen log B (w1/4 + h) = o(w1/2 ).
The search factors come first and must therefore decrease the gap from r0 ≍ B ≍ w log w to
at most w1/2 . A standard transition decreases the gap by at most a bounded multiplicative
factor, including at the initial extended start. At least a constant multiple of log w search
factors is necessary.
At a hard endpoint for the chosen rational, all these search primes align to it. If none
of their bins is near-full for this rational, each of the bins has more than an η fraction of
nonaligning primes by count. For primes in [R, (1 + ξ)R], this is a harmonic fraction at least
η/(1 + ξ). The search choices are independent in the full product box, so the fraction of its
harmonic measure with all those alignments is at most
(

η
1−
1+ξ

)c7 log w

= o(1).

This bounds the relevant hard event in the full box without asserting independence after
conditioning on hardness.
Otherwise some visited search bin is near-full for this rational, which is therefore its owner.
The hard endpoint’s choice in this bin aligns to its owner, so a tag has been acquired by that
position. If the first tag is a different rational, the prime at the earlier tag position aligns
both to A/D and to the distinct eligible owner of that bin. By (10.2), its possible choices
form a uniformly negligible fraction, even after summation over Clen log B positions. Indeed
in a search bin this fraction is at most a constant, depending on fixed ξ, times
L + log R
,
R
and R ≥ exp(w1/4 log w).
There are at most the fixed list bound times the fixed candidate count such rational choices
per box. The union of the preceding exceptions therefore costs o(1) of the full candidate-box
harmonic measure. The total mass of the enlarged boxes is OK (B −2 ), independently of
sufficiently small ξ, by Theorem 7.2. Summing over the boundedly many candidates gives
a total o(B −2 ) exception. Outside it, a hard endpoint has the correct tag by the end of its
search positions.
Finding an even visit before the compact endpoint. Apply Theorem 4.8 to the
continuous standard path. For any prescribed probability error ε1 > 0, with b0 fixed, choosing
b1 /b0 sufficiently large ensures, uniformly from the allowed starting ratios as the initial gap
tends to infinity, an even arrival with ratio in [2.08, 2.14] and last exponent in [2b0 , b1 /2],
except with probability at most ε1 + o(1). The proof of that lemma marks the first draw
from an odd regeneration when its ratio lies in [2.09, 2.13], using a pre-draw gap in [10b0 , b1 ].
In particular the arrival has the stronger interior margins
10b0
b1
≤x≤
,
3.13
3.09

2.09 ≤ s ≤ 2.13.

The choice of b1 depends on the probability budget and fixed b0 , not on z or on ξ.
69

(10.22)

## PDF page 70

Use Theorem 5.3 for standard prime paths with lower exponent cutoff 1. Actual included
paths are a subset of these standard paths; their rules agree above exponent 2. High-ratio
histories ending in the fixed compact window have negligible scaled mass by Theorem 5.2.
On the remaining histories the coupling matches states and exits, with a failure probability
tending to zero. The interior margins in (10.22) therefore give the asserted slightly wider
visit windows on matched prime paths.
This visit lies in the segment being compared whenever the matched prime history ends
in the compact window. In fact its arrival gap is at least a fixed multiple of b0 . Taking b0
sufficiently large relative to K, that gap exceeds the matched compact endpoint gap. Since
gaps decrease along the path, a raw continuous marked visit cannot occur after this endpoint.
Matching exits puts the visit before any cutoff exit as well. Thus the coupling cannot lose
the needed visit merely by stopping the compared segment at the compact endpoint.
The compact-history event estimate in Theorem 5.5 now bounds the harmonic mass of
compact endpoints missing such a visit by
CK (ε1 + o(1))B −2 + o(B −2 ),
where CK depends on the fixed compact window and the starting bounds, not on the later
bin width. Choose ε1 sufficiently small in terms of δ/CK , and choose b1 accordingly.
Verifying the stop conditions. Consider a regular hard endpoint with the correct tag
and with this even visit. Every factor up to the visit has exponent at least the visit’s last
exponent, which exceeds Cs by the choice of b0 . Hence all these factors align to its tag
rational. Its search positions have already passed: their lower exponents are at least w1/4 ,
whereas the visit exponent is bounded by fixed b1 . The tag is therefore attained by the visit,
and its bin has multiplicity one. The visit-prefix length is at most the regular endpoint length
Clen log B.
By regularity, every earlier nonempty even prefix, including the visit, has actual margin
greater than 10∆ in the admission test. The representative movement is at most ∆, and
changing the last exponent changes H by at most 2h. For sufficiently large z, the representative
margin is consequently at least 10∆ − ∆ − 2h > 3∆. Thus (10.3) holds. Finally the ratio
and exponent slack in the visit windows, the prefix movement bound, and a sufficiently small
fixed ξ imply (10.4). All stop conditions hold at this visit. The branch has therefore stopped
there or earlier.
Combining the o(B −2 ) incorrect-tag exception with the arbitrarily small missing-visit
mass proves (10.21).
The order of choices in these two propositions is worth making explicit. The constant CU
in (10.8) is absolute, so the owner threshold η can be fixed before either stop-window endpoint.
The choice of b0 absorbs Cs , the local reference error, the interval-height margin, and the
compact gap range. Only the ratio b1 /b0 must then be enlarged to make the marked-visit
error as small as desired. Afterwards ξ is chosen for representative movements and all earlier
freezing conditions. Every progression modulus and prime-sieve level used here remains a
fixed power of log R′ for these choices, however large the fixed b1 is. The corresponding
asymptotic thresholds may therefore wait until this final fixed ξ has been chosen.

11

Completion of the proof

We now combine the estimates, keeping the order of constants explicit. This first proves
Theorem 1.2; the deduction of Theorem 1.1 then uses only an upper sieve.

70

## PDF page 71

11.1

The error budget

Proof of Theorem 1.2. By Proposition 6.3, there is an absolute cL > 0 such that
Pe (r0 , B) ≥

cL
B2

(11.1)

for all sufficiently large z. Let Cabs be an absolute constant such that
|Nd /µd − 1| ≤ Cabs
at every included node; this follows from (3.4).
For nodes with large gap, the relative error in (3.4) is O(e−crd ) after a fixed lower threshold
on rd . The tail estimate in Proposition 5.5 permits us to choose a fixed K so large that
∑

|Nd − µd | ≤

d included
rd >K

cL Y V0
8 B2

(11.2)

eventually. Standard paths contain the included paths, so the nonnegative tail estimate
applies. This choice depends only on the fixed reference margin and the absolute small-prime
error constants.
The same proposition gives a constant CK for the total harmonic mass of nodes with
rd ≤ K. Choose ε > 0 such that εCK < cL /8. The compact nodes with relative error at most
ε then contribute at most
∑

|Nd − µd | ≤

d included
rd ≤K
|Nd /µd −1|≤ε

cL Y V0
.
8 B2

(11.3)

It remains to deal with compact nodes having relative error greater than ε. Fix a target
β > 0 so small that
cL
Cabs β <
.
(11.4)
8
We claim that the stopped tree can be chosen so that the retained bad compact nodes have
total harmonic mass at most β/B 2 . The following choices give this claim without requiring
any constant to be chosen again at an earlier stage.
First use Lemma 7.1 to fix a larger threshold K∗ , a positive edge-discrepancy threshold,
and a fixed maximum number He of candidate positions. Choose the adjustable regularity
exceptions in Proposition 7.2 small enough to cost less than a prescribed small fraction of
β/B 2 . This fixes the path-length bound and the isolated-prime interval. For the moment
leave the exception for near-threshold even prefixes to the eventual choice of bin width.
′ /B 2 , with C ′ indeThe enlarged regular boxes have total harmonic mass at most CK
K
pendent of sufficiently small fixed ξ. Choose the exception fraction σ in Proposition 8.2
sufficiently small that
′
He CK
σ
is less than another prescribed small fraction of β. The inverse proposition now fixes a
positive alignment fraction and a list bound F , independently of the eventual sufficiently
small fixed width. Each list is attached to its entire candidate box.
Next choose the variance exception fraction in Proposition 9.2 small enough relative to
′ , F and β. A prime-count fraction in the isolated bin converts to a harmonic fraction
He , CK
at a bounded absolute cost. After this conversion and the finite unions over candidates and
list elements, the total variance exception costs another prescribed small fraction of β/B 2 .
The variance proposition fixes a constant Cs . Corollary 9.3 then shows that all remaining bad
71

## PDF page 72

compact endpoints have a hard rational satisfying the global eligibility bounds and alignment
of every factor with exponent greater than Cs .
Choose the absolute owner threshold η required by Proposition 10.5. Choose b0 sufficiently
large in terms of Cs and K and for the local reference and prime estimates in that proposition.
Finally choose b1 /b0 sufficiently large that Proposition 10.6 bounds the hard endpoints that
remain outside stopped subtrees by the remaining allocated small fraction of β/B 2 . This
uses the marked-visit estimate with a prescribed failure probability, as well as the vanishing
owner and wrong-tag exceptions for the fixed candidate lists.
All constants except the bin width have now been fixed. Choose a fixed ξ > 0 sufficiently
small for the interval-freezing errors, candidate-size slack, representative stopping margins
and all earlier small-width requirements. In particular, the near-threshold exception, of cost
O(∆) + o(1) in the compact-history probability measure with ∆ = 2Clen ξ, can be made as
small as the error budget requires. Then take z sufficiently large for every preceding fixed
choice. Asymptotic bounds whose thresholds depend on ξ are used only at this final stage.
The sum of all these finitely many allocated costs is at most β/B 2 , proving the claim.
More explicitly, after removing the regularity exceptions, every retained bad endpoint has a
witnessing edge. Outside the inverse exceptions it has an alignment in the fixed list. Outside
the variance exceptions it is hard. Outside the hard-stopping exceptions it lies in a stopped
subtree and is therefore not retained. This exhausts the cases. Fractional exceptions are
′ /B 2 , not the number of boxes.
summed using He CK
The claim and (11.4) show that retained bad compact nodes contribute at most
(cL /8)Y V0 /B 2 in absolute error. Together with (11.2) and (11.3), this gives
∑

|Nd − µd | ≤

d∈T

3cL Y V0
8 B2

(11.5)

for the retained expanded nodes of the chosen stopped tree. Proposition 10.5 gives
∑(

)

Sd (bd ) − µd Pe (rd , bd ) ≥ 0.

d∈S

Apply (3.7), Lemma 3.1 and (11.1). We obtain
3
Y V0
cL Y V0
S1 (B) ≥ 1 −
cL 2 ≥
.
8
B
2 B2
(

)

Every constant is independent of the prescribed residue classes. This proves Theorem 1.2.

11.2

Removing the remaining divisor primes

The factor log w in the survivor estimate allows a cutoff smaller than k log k. We choose it so
that the loss from the at most k remaining divisor primes is a fixed fraction of the surviving
count.
Proof of Theorem 1.1. By Theorem 1.2 and Mertens’ formula, there is an absolute c0 > 0
such that, for every sufficiently large real z, every assignment of one forbidden class at each
prime p ≤ z leaves at least
Y log w
c0
(11.6)
L2
integers in [1, Y ]. Indeed, V0 /B 2 ∼ e−γ log w/L2 .
Let k be sufficiently large, put ℓ = log k and M = log log k, and take
z = A0

k log k
,
log log k
72

(11.7)

## PDF page 73

where the absolute constant A0 > 1 will be fixed below, before k tends to infinity. With the
parameters of (1.2),
L ∼ ℓ,

Y ∼ A20

log w ∼ M,

k2
,
M2

X :=

Y
k
∼ A0
,
z
ℓM

log X ∼ ℓ.

(11.8)

In particular z → ∞ and X → ∞ for every such fixed A0 .
Let n be any positive integer with ω(n) ≤ k, and let the given interval of Y consecutive
integers begin at an arbitrary integer a. Represent its integers as a + j − 1, 1 ≤ j ≤ Y . For
each prime p | n with p ≤ z, prescribe the forbidden class
j ≡1−a

(mod p).

At the other primes p ≤ z, prescribe any class. The estimate (11.6) counts integers that avoid
every divisor prime at most z, together with these additional restrictions.
Fix a prime divisor q > z of n. Its divisibility class has at most 1 + Y /q ≤ 1 + X
representatives in the coordinate interval. Enclose them in a progression segment whose
coordinate length is ⌈X⌉ + 2. Fix a sufficiently small absolute θ > 0 and sieve this segment
by primes at most X θ . This cutoff is below z for large k, the step q is invertible modulo
every sieve prime, and the integers already counted in (11.6) avoid its prescribed class there.
Lemma 2.3 and Mertens’ formula therefore give
(

#{these survivors divisible by q} ≤ C1 1 +

X
log X

)

(11.9)

for an absolute C1 , uniform in q, A0 , the classes, and the translation once the displayed
length conditions hold. More explicitly, the enclosing coordinate length is comparable to X
and at least (X θ )1/(2θ) for large X, so the fixed exponent upper bound in Lemma 2.3 applies.
Enclosing a shorter or empty progression only increases the count; in particular the argument
also covers q > Y .
There are at most k such further divisor primes. For each fixed A0 , (11.8) gives
k(1 + X/ log X)
1
=
+ o(1).
2
Y log w/L
A0

(11.10)

For the second term in the numerator, the quotient is kL2 /(z log X log w) → 1/A0 ; the
term k is negligible since Y log w/L2 ≍A0 k 2 /(ℓ2 M ). Choose once and for all A0 > 2C1 /c0 .
Equations (11.9) and (11.10) then show that fewer than the number in (11.6) are removed,
for all sufficiently large k. At least one integer in the original interval is therefore coprime to
n.
This argument is uniform in the prime divisors of n and in every integer a, including
negative starting points and intervals containing zero. Prime multiplicities do not enter. The
length estimate in (11.8), with A0 now absolute, gives
h(k) ≪

k2
k2
≪
(log log k)2
(log log(3k))2

for all sufficiently large k, since log log(3k)/ log log k → 1.
To include the remaining finitely many values of k, suppose n has r ≤ k distinct prime
divisors. Inclusion–exclusion gives at least
m

∏(
p|n

1
1−
p

)

− 2r ≥

73

m
− 2k
k+1

## PDF page 74

coprime integers in every interval of m consecutive integers. For the product bound, order
∏
the distinct primes as p1 < · · · < pr and use pj ≥ j + 1 to obtain rj=1 (1 − 1/pj ) ≥ 1/(r + 1).
This also covers r = 0 with the empty product equal to one. The integer mk = (k + 1)2k + 1
consequently bounds h(k) for each remaining k. The maximum of
mk (log log(3k))2
k2
over this finite set, together with the constant already obtained for large k, supplies one
absolute constant C such that h(k) ≤ Ck 2 /(log log(3k))2 for every integer k ≥ 1.

A

A modular hyperbola count with residue restrictions

The large-modulus case of Proposition 9.2 requires a rectangle count with a congruence
restriction on the unit coordinate of a modular hyperbola. We give the completion argument
with an explicit error, retaining multiplicities when an interval is longer than the modulus.
Lemma A.1 (Completion with a unit residue restriction). Let H, T0 , T1 be positive integers
such that H ≥ 2, T0 is squarefree, every prime divisor of T0 divides H, and (T1 , HT0 ) = 1.
Put N = HT0 . Let C0 ∈ Z satisfy (C0 , H) = 1, and prescribe the residue pattern
p0 ∈ (Z/T0 Z)× ,

p1 ∈ (Z/T1 Z)× ,

k0 ∈ Z/T0 Z,

m1 ∈ Z/T1 Z.

(A.1)

The residue classes modulo 1 have their usual unique interpretation. Let I, J be bounded real
intervals of lengths X, Y2 ≥ 0, with either endpoint independently included or excluded. For a
positive integer l with (l, HT1 ) = 1, let Cl be the number of integer pairs (p, m) satisfying
p ∈ I,
p ≡ p0

(mod T0 ),

m ∈ J,

p ≡ p1

l | p,

(mod T1 ),

pm ≡ C0 + Hk0

m ≡ m1

(mod T1 ),

(A.2)

(mod N ).

Here p is an integer variable, without a primality condition. Uniformly in all these data,
√
XY2 φ(N )
X
Y2
Cl = 2 2
+
+ O τ (N )2 log2 (2N ) N T0 1 +
lN
N
lT1 N φ(T0 )
(

(

))

,

(A.3)

with an absolute implied constant.
In particular, suppose that R → ∞ and the data range uniformly over families satisfying
R4/5 < H ≤ RZ 11 ,

X ≪ R,

Y2 ≤ 3H,

Z, T0 , T1 = Ro(1) .

(A.4)

Then, uniformly over all the patterns and intervals above and all squarefree l ≤ R1/10 with
(l, HT1 ) = 1,
(
)
XY2 φ(N )
+ O R3/5+o(1) .
Cl = 2 2
(A.5)
lT1 N φ(T0 )
Thus the same assertion holds with error O(R7/10+o(1) ). Uniformity in the last two assertions
means that the upper bounds represented by Ro(1) in (A.4) hold uniformly over the family;
equivalently, for every δ > 0 the error in (A.5) is Oδ (R3/5+δ ) for sufficiently large R in that
family. No lower bound for X/l is required.
Proof. Write en (t) = exp(2πit/n). We use the classical complete Kloosterman estimate, in
the form recorded in [19, Lemma 7.1]:
Kl(a, b; n) :=

∑

| Kl(a, b; n)| ≪ τ (n)n1/2 (a, b, n)1/2 .

en (au + bū),

(A.6)

u mod n
(u,n)=1

This bound permits arbitrary composite n and arbitrary integer frequencies, including zero
frequencies. The inverse ū is taken modulo n.
74

## PDF page 75

Changing the first coordinate. Choose a representative of k0 and put c = C0 + Hk0
modulo N . The integers H and N have the same prime support. Since (C0 , H) = 1, it follows
that (c, N ) = 1. The hypothesis on l also implies (l, N T1 ) = 1. On setting p = lv, define
c′ = c¯l (mod N ),
a1 = p1 ¯l (mod T1 ).

U = X/l,
V = Y2 ,
¯
a0 = p0 l (mod T0 ),

Every inverse here is taken in its indicated modulus. The interval Il = {x/l : x ∈ I} has
length U and the induced endpoint conventions. The pairs now satisfy
v ∈ Il ,

v ≡ a1
v ≡ a0

m ∈ J,

(mod T1 ),

vm ≡ c

(mod T0 ),

m ≡ m1
′

(mod T1 ),

(mod N ).

In particular v and m are automatically units modulo N .
Fourier weights and their divisor-weighted sums. For h, k mod N , define the unnormalized weights
A(h) =

∑

eN (−hv),

∑

B(k) =

v∈Il ∩Z
v≡a1 (T1 )

eN (−km).

(A.7)

m∈J∩Z
m≡m1 (T1 )

These are sums over the integers in the progressions, so a residue modulo N is counted with
its full multiplicity. They therefore apply unchanged when U or V exceeds N . Counting the
progressions gives
A(0) = U/T1 + O(1),

B(0) = V /T1 + O(1).

(A.8)

For a nonzero residue h mod N , let |h|N = minj∈Z |h + jN |. A geometric-progression sum,
with ratio eN (−hT1 ) ̸= 1, gives
|A(h)|, |B(h)| ≪

N
|hT1 |N

(h ̸≡ 0 (mod N )).

(A.9)

The right side is independent of the number of complete periods and of the locations of the
intervals.
Multiplication by T1 permutes the nonzero residues modulo N and preserves their greatest
common divisors with N . Thus
∑ (r, N )1/2
(h, N )1/2
=
|hT1 |N
|r|N
h̸=0 (N )
r̸=0 (N )
∑

≤

∑

d1/2

d|N

1
|r|
N
r̸=0 (N )
∑

(A.10)

d|r

≪ log(2N )

∑

d−1/2 ≤ τ (N ) log(2N ).

d|N
−1 ∑

−1
Indeed the inner sum is at most 2d
1≤j≤N/(2d) j , with a harmless possible overcount of
the midpoint. Without the gcd weight the corresponding sum is O(log(2N )). In conjunction
with (A.9), this proves

∑
h̸=0 (N )

|A(h)| ≪ N log(2N ),

∑

|A(h)|(h, N )1/2 ≪ N τ (N ) log(2N ),

h̸=0 (N )

and the identical estimates with B in place of A.
75

(A.11)

## PDF page 76

Define

Completion with the unit restriction.
∑

S(h, k) =

eN (hu + kc′ ū).

u mod N
(u,N )=1
u≡a0 (T0 )

Fourier inversion, with the multiplicities in (A.7), gives the exact identity
Cl =

∑
1
A(h)B(k)S(h, k).
2
N h,k mod N

(A.12)

For example, summing A(h)eN (hu)/N over h counts all allowed integers v ≡ u (mod N ),
which verifies the normalization directly.
Orthogonality modulo T0 also gives the exact formula
S(h, k) =

1 ∑
eT (−ja0 ) Kl(h + jH, kc′ ; N ).
T0 j mod T 0

(A.13)

0

The average over j does not cost a factor T0 in the following absolute bounds. When k ̸= 0
(mod N ), the fact that (c′ , N ) = 1 and (A.6) give
√
k ̸= 0 (mod N ),
(A.14)
|S(h, k)| ≪ τ (N ) N (k, N )1/2 ,
uniformly also when h = 0. For h ̸= 0 and k = 0, observe that
(h + jH, N ) ≤ T0 (h, N ).

(A.15)

In fact any common divisor of h + jH and N divides T0 h, because T0 H = N , and (T0 h, N ) ≤
T0 (h, N ). Consequently
|S(h, 0)| ≪ τ (N ) N T0 (h, N )1/2 ,
√

h ̸= 0

(mod N ).

(A.16)

If a shift h + jH vanishes modulo N , it is still covered by (A.15); no shifted zero frequency is
omitted. No squarefreeness of H or N has been used.
At the two original zero frequencies,
S(0, 0) =

φ(N )
,
φ(T0 )

φ(N ) = T0 φ(H).

(A.17)

For the first equality, reduction from the units modulo N onto the units modulo T0 is surjective
with equal fibers. Explicitly, if ta exactly divides H and t | T0 , then the local modulus in
N is ta+1 , and every unit modulo t has ta unit lifts. At a prime of H outside T0 there is no
prescribed local class. The Chinese remainder theorem proves the first equality. The same
prime-power calculation gives the second.
The four frequency cases.

The contribution of h = k = 0 to (A.12) is

A(0)B(0)φ(N )
U V φ(N )
U +V +1
= 2 2
+O
,
2
N φ(T0 )
N
T1 N φ(T0 )
(

)

(A.18)

where (A.8) handles every endpoint convention. This is the stated main term since U V =
XY2 /l.
For h ̸= 0, k ̸= 0, use (A.14) and (A.11). The total absolute contribution is
√
√
)(
)
τ (N ) N (
2
≪
N
log(2N
)
N
τ
(N
)
log(2N
)
=
τ
(N
)
N log2 (2N ).
N2
76

## PDF page 77

For h = 0, k ̸= 0, the same argument with the zero weight retained gives
≪ A(0)τ (N )2 N −1/2 log(2N ).
For h ̸= 0, k = 0, instead use (A.16); this contribution is
1/2

≪ B(0)τ (N )2 T0 N −1/2 log(2N ).
Finally, A(0) ≪ U/T1 + 1 and B(0) ≪ V /T1 + 1. These three estimates and the rounding
term in (A.18) are all bounded by the error displayed in (A.3). This proves the general
assertion, with an absolute implied constant.
The size range needed in the variance argument.
R4/5 < N ≤ R1+o(1) ,

Under (A.4),

Y2 ≤ 3N.

The elementary divisor bound τ (N ) = N o(1) and T0 = Ro(1) turn the explicit error into
Ro(1)

(√

X/l
Y2
N+√ +√
N
N

)

≪ R1/2+o(1) + R3/5+o(1) = R3/5+o(1) .

The estimate uses only l ≥ 1, and is therefore uniform throughout the asserted sieve range.
It also holds for shorter blocks and for arbitrarily translated intervals. This proves (A.5) and
completes the proof.
Remark A.2. In the application, R ≥ z αmin with fixed αmin > 0, Z = exp(L/ log L), and
T0 =

∏

t,

T1 =

t≤w
t|H

∏

t.

t≤w
t∤H

Then log(T0 T1 ) = O(w) = o(log R) and log Z = o(log R), uniformly in the isolated bin. Thus
the uniform family conditions in (A.4) follow from the parameters of the main argument. A
fixed bin-width parameter may affect the point at which these asymptotics apply, but it does
not enter the absolute constant in (A.3).

B

Elementary forms of four auxiliary estimates

We give the versions of four classical estimates needed in the proof. The Buchstab normalization follows directly from its delay equation; the large-sieve and plane-curve bounds need
only elementary integration and elimination. The progression upper bound is a consequence
of Lemma 2.1 and Mertens’ product formula. In particular, the last argument retains the
fundamental lemma as an input.

B.1

The continuous Buchstab normalization

The normalization used in Lemma 4.1 is the classical one; see [22, Section 28.9, p. 236].
The following proof uses only the continuous delay equation, independently of the positivity
argument for the sieve functions.
Lemma B.1. Let ω : [1, ∞) → R be the continuous function determined by
uω(u) = 1

(1 ≤ u ≤ 2),

(uω(u))′ = ω(u − 1)

(u > 2).

Then ω(u) → e−γ as u → ∞, where γ = limn→∞ (Hn − log n) and Hn =
77

∑n

j=1 1/j.

## PDF page 78

Proof. Successive integration on unit intervals constructs a unique positive continuous function,
locally absolutely continuous and with bounded one-sided derivatives on each such interval.
For u > 2 its equation gives, almost everywhere,
uω ′ (u) = ω(u − 1) − ω(u) = −

∫ u

ω ′ (v) dv.

(B.1)

u−1

Put Mn = ess supn<u<n+1 |ω ′ (u)|. These quantities are finite by the construction, and M1 ≤ 1.
For every integer n ≥ 2, (B.1) implies
Mn ≤

1
max(Mn−1 , Mn ).
n

If Mn > Mn−1 this inequality forces Mn = 0, a contradiction; otherwise it gives Mn ≤ Mn−1 /n.
Thus Mn ≤ 1/n!. In particular ω ′ is integrable on [1, ∞), so ω is bounded and has a finite
limit, say ℓ.
It remains to determine ℓ. For t > 0 define
∫ ∞

W (t) =

ω(u)e−tu du.

1

Boundedness justifies differentiation and integration by parts. The derivative of uω(u) is zero
on (1, 2); integrating it on [1, ∞), including the boundary value at 1, gives
−e−t − tW ′ (t) =

∫ ∞

ω(u − 1)e−tu du = e−t W (t).

2

Since W (t) → 0 as t → ∞, solving this differential equation yields
(∫
∞ e−s

1 + W (t) = exp

t

s

)

ds .

(B.2)

The constant in this formula can be evaluated without a Tauberian argument. Integration by
parts shows that
∫ ∞ −s
e
t

s

Moreover,

−t

ds + log t = (1 − e ) log t +

∫ ∞

e−s log s ds.

t

∫ ∞

e−s log s ds = −γ.

(B.3)

0

For an elementary verification, substitution s = nv and integration of the geometric sum give
∫ n

(1 − s/n)n log s ds =

0

)
n (
log n − Hn+1 .
n+1

Indeed,
1 1 − (1 − v)n+1
1
Hn+1
dv = −
.
n+1 0
v
n+1
0
The integrands in the first identity, extended by zero for s > n, are bounded in absolute value
by e−s | log s|. Dominated convergence proves (B.3). Consequently (B.2) gives tW (t) → e−γ
as t ↓ 0. On the other hand, substituting v = tu and using bounded convergence gives

∫ 1

∫

(1 − v)n log v dv = −

∫ ∞

tW (t) =

ω(v/t)e−v dv −→ ℓ.

t

This identifies ℓ = e−γ .
This derivation supplies precisely the independently normalized limit needed to rule out a
jump at 2 in the proof of Lemma 4.1. It makes no use of the auxiliary Markov chain or of
the future-integral identities proved there.
78

## PDF page 79

B.2

The additive large sieve at the required order

The sharp large sieve is due to Montgomery and Vaughan [20]; see also [26]. The following
separated-arcs argument gives the order of (2.2) that is used in the inverse estimate.
Lemma B.2. Let x1 , . . . , xR ∈ R/Z have pairwise circular distance at least δ, where 0 < δ ≤ 1.
Let J ≥ 1 be an integer. If complex coefficients bj are supported on J consecutive integers,
then
∣
∣
∣2
R ∣∣∑
∑
∑
∣
∣
bj e(jxr )∣∣ ≪ (J + δ −1 )
|bj |2
∣
∣
∣
r=1 j
j

with an absolute implied constant. Hence (2.2) holds for every real Q ≥ 1.
Proof. Shifting the frequencies multiplies their sum by a complex number of modulus one.
∑
2
We may therefore write T (x) = J−1
j=0 bj e(jx) and f (x) = |T (x)| . Let Ir be the arc of length
δ centred at xr . Their interiors are disjoint. For t ∈ Ir , the fundamental theorem of calculus
along that arc gives
∫
|f ′ (x)| dx.

f (xr ) ≤ f (t) +

Ir

Average over t ∈ Ir and sum over r to obtain
∑
r

f (xr ) ≤ δ −1

∫ 1

|T (x)|2 dx +

∫ 1

0

|f ′ (x)| dx.

0

Since |f ′ | ≤ 2|T ′ ||T |, Cauchy–Schwarz and Parseval give
∫ 1

|f ′ (x)| dx ≤ 2∥T ′ ∥2 ∥T ∥2 ≤ 4π(J − 1)

0

J−1
∑

|bj |2 .

j=0

This proves the asserted estimate. Distinct reduced fractions modulo one with denominators
at most Q have circular distance at least Q−2 : subtracting two such fractions, or subtracting
an integer from their difference, leaves a nonzero integer numerator over the product of their
denominators. Apply the estimate with δ = Q−2 . When there is just one fraction, the same
arc argument applies directly.

B.3

A degree-uniform plane-curve intersection bound

The appeals to Bézout’s theorem in Lemma 8.3 require a bound uniform in both degrees and
coefficients. Here is the needed affine form, proved by the elementary resultant argument.
Only distinct points are counted; multiplicities are unnecessary.
Lemma B.3. Let F, G ∈ C[X, Y ] be nonzero polynomials of respective total degrees m, n ≥ 1,
with no common nonconstant factor. Then they have at most mn common zeros in C2 .
Proof. First choose linear coordinates in which the coefficients of Y m in F and Y n in G are
nonzero constants. Such coordinates exist: choose the direction of the Y -axis outside the
zeros of the two highest homogeneous parts. Each part excludes only finitely many directions
in the projective line. Scaling the polynomials makes these leading coefficients one.
Put K = C(X). The two polynomials are coprime in K[Y ]. Indeed, clearing denominators
in a common factor and removing common factors of its coefficients would give a common
polynomial factor in C[X, Y ]. This is the elementary Gauss lemma: the product of two
polynomials whose coefficients have no common divisor again has coefficients with no common
divisor, as follows by reduction modulo any irreducible divisor in C[X].
79

## PDF page 80

Consider the linear map over K
(A, B) ↦−→ AF + BG,

degY A < n,

degY B < m,

(B.4)

with target the polynomials of Y -degree less than m + n. It is injective: from AF = −BG
and coprimality, F divides B, forcing B = 0 and then A = 0. Its matrix in monomial bases
is the Sylvester matrix. Its determinant R(X) is a nonzero polynomial. If (x, y) is a common
zero, every polynomial in the image of the specialized map at X = x vanishes at Y = y. That
image is a proper subspace, so R(x) = 0. There are finitely many such x, and each fiber
contains finitely many points because F (x, Y ) is monic of degree m. Thus the common zero
set is finite.
Now choose linear coordinates once more so that the X-coordinates of those finitely many
points are distinct and both leading coefficients in Y remain nonzero constants. The first
condition excludes the finitely many directions joining pairs of common zeros; the second
excludes the directions on which either highest homogeneous part vanishes. A direction
satisfying both exists. Repeat the construction of R in these coordinates.
We claim that deg R ≤ mn. Write
F =

m
∑

fk (X)Y k ,

G=

k=0

n
∑

gk (X)Y k ,

deg fk ≤ m − k,

deg gk ≤ n − k.

k=0

View the rows of the Sylvester matrix as the coefficients of Y i F for 0 ≤ i < n and Y j G for
0 ≤ j < m; label its columns by Y k , 0 ≤ k < m + n. An entry from row Y i F and column Y k
has degree at most m + i − k; an entry from row Y j G has degree at most n + j − k. Every
nonzero term of the determinant uses each row and column once, so its degree is at most
n−1
∑

m−1
∑

m+n−1
∑

i=0

j=0

k=0

(m + i) +

(n + j) −

k = mn.

Every common zero gives a distinct root of the nonzero polynomial R. This proves the
bound.
For clarity, the coprimality conditions in Lemma 8.3 can now be checked directly. An
irreducible factor Q of degree d ≥ 2 that is not proportional to a real polynomial is coprime
to its coefficientwise conjugate. Both partial derivatives of Q are nonzero: independence of
one variable would force an irreducible polynomial over C to be linear. Their smaller degrees
make them coprime to Q, giving at most d(d − 1) intersections for each derivative; a nonzero
constant derivative has no common zeros with Q. The same lemma applies to the inflection
polynomial (8.10) when it is nonzero and not divisible by Q, since its degree is at most 3d − 4;
a nonzero constant inflection polynomial has no zeros. If it is divisible by Q, every nonspecial
smooth real graph arc has second derivative zero and lies on a line. Restricting Q to that
line would then give a univariate polynomial vanishing on an interval, hence identically; the
line would be a factor of Q. This excludes such an arc and is exactly the alternative used in
that proof.

B.4

An order bound for primes in a progression

Brun–Titchmarsh gives a sharper constant than we need; see [10, Theorem 1.4.4]. We derive
the order bound in Lemma 2.2(iii) from the fundamental lemma, in the form recorded in [24,
Lemma 2.8], and Mertens’ formula. Working in progression coordinates keeps the remainder
independent of the modulus.

80

## PDF page 81

Lemma B.4. There are absolute constants C, J0 > 0 such that, for every integer q ≥ 1,
every integer a with (a, q) = 1, and every real x and H > 0 with J = H/q ≥ J0 ,
#{x < p ≤ x + H : p ≡ a

(mod q)} ≤ C

H
.
φ(q) log(H/q)

Proof. Write the progression as a + qj, with j in the real interval
(x − a)/q < j ≤ (x + H − a)/q
of length J. Fix an absolute s ≥ s0 sufficiently large that θ = 1/(2s) < 1/2, and put v = J θ
and D = J 1/2 = v s . For every prime p ≤ v not dividing q, divisibility of a + qj by p specifies
exactly one forbidden class of j modulo p. For a squarefree product l of these primes, the
Chinese remainder theorem therefore gives the intersection count
J/l + O(1),
with an absolute error independent of x, a, q, l. Apply Lemma 2.1 with X = J and g(p) = 1/p
on this prime set. If N counts the surviving coordinates, it gives
N ≪J

∏

(1 − 1/p) + D(1 + log D)C2

(B.5)

p≤v
p∤q

for an absolute constant C2 . To justify the remainder explicitly, let C1 be the divisor-weight
exponent in (2.1) and choose an integer k ≥ 2C1 . On squarefree l, τ (l)C1 ≤ τk (l), where τk (l)
counts ordered factorizations of l into k positive integers. Summing by the first k − 1 factors
gives

∑

τk (l) ≤ D 

l≤D

∑ 1

d
d≤D

k−1


≤ D(1 + log D)k−1 .

In particular, the remainder in (B.5) has no dependence on q.
Mertens’ formula gives, for large J,
∏

(1 − 1/p) =

p≤v
p∤q

∏

(1 − 1/p)

p≤v

∏

(1 − 1/p)−1 ≪

p|q
p≤v

1
q
1
q
≪
.
log v φ(q)
log J φ(q)

Every prime in the progression that exceeds v is among the survivors. The primes at most v
contribute at most v further points, regardless of q. Thus the desired prime count is at most
N +v ≪

Jq
+ J 1/2 (1 + log J)C2 + J θ .
φ(q) log J

The last two terms are O(J/ log J) for all sufficiently large J, uniformly in q. Since q/φ(q) ≥ 1,
they are absorbed by the first term. Substituting J = H/q completes the proof.

References
[1] William Banks, Kevin Ford, and Terence Tao. Large prime gaps and probabilistic models. Inventiones Mathematicae, 233(3):1471–1518, 2023. Corrected version:
arXiv:1908.08613v3 (2025). https://arxiv.org/abs/1908.08613v3.
[2] Fintan Costello and Paul Watts. An upper bound on Jacobsthal’s function. Mathematics of Computation, 84(293):1389–1399, 2015.
https://doi.org/10.1090/
S0025-5718-2014-02896-2.
81

## PDF page 82

[3] P. Erdős. On the integers relatively prime to n and on a number-theoretic function
considered by Jacobsthal. Mathematica Scandinavica, 10:163–170, 1962. https://doi.
org/10.7146/math.scand.a-10523.
[4] Andrew Fiori, Habiba Kadiri, and Joshua Swidinsky. Sharper bounds for the error
term in the prime number theorem. Research in Number Theory, 9(3), 2023. Article
63. https://doi.org/10.1007/s40993-023-00454-w. Author version https://arxiv.
org/abs/2206.12557v2.
[5] Kevin Ford, Ben Green, Sergei Konyagin, James Maynard, and Terence Tao. Long gaps
between primes. Journal of the American Mathematical Society, 31(1):65–105, 2018.
https://doi.org/10.1090/jams/876.
[6] John Friedlander and Henryk Iwaniec. Opera de Cribro, volume 57 of American Mathematical Society Colloquium Publications. American Mathematical Society, Providence,
RI, 2010. https://doi.org/10.1090/coll/057.
[7] P. X. Gallagher. A larger sieve. Acta Arithmetica, 18:77–81, 1971. https://doi.org/
10.4064/aa-18-1-77-81.
[8] P. X. Gallagher. On the distribution of primes in short intervals. Mathematika, 23(1):4–9,
1976. https://doi.org/10.1112/S0025579300016442.
[9] Andrew Granville and K. Soundararajan. The distribution of prime numbers. Undated
draft. https://dms.umontreal.ca/~andrew/PDF/PretendBook050111.pdf. Accessed
September 25, 2026.
[10] Andrew Granville and K. Soundararajan. Multiplicative number theory: The pretentious
approach. Draft, 2014. https://dms.umontreal.ca/~andrew/PDF/Book.To2.5.pdf.
Disproof of a conjecture of Jacobsthal.
Math[11] L. Hajdu and N. Saradha.
ematics of Computation, 81(280):2461–2471, 2012.
https://doi.org/10.1090/
S0025-5718-2012-02581-6.
[12] D. R. Heath-Brown. Prime numbers in short intervals and a generalized Vaughan identity.
Canadian Journal of Mathematics, 34(6):1365–1377, 1982. https://doi.org/10.4153/
CJM-1982-095-9.
[13] H. A. Helfgott and A. Venkatesh. How small must ill-distributed sets be? In Analytic
Number Theory: Essays in Honour of Klaus Roth, pages 224–234. Cambridge University
Press, Cambridge, 2009. https://webusers.imj-prg.fr/~harald.helfgott/texts/
howsmall.pdf.
[14] Henryk Iwaniec. On the error term in the linear sieve. Acta Arithmetica, 19(1):1–30,
1971. https://doi.org/10.4064/aa-19-1-1-30.
[15] Henryk Iwaniec. On the problem of Jacobsthal. Demonstratio Mathematica, 11(1):225–
231, 1978. https://doi.org/10.1515/dema-1978-0121.
[16] Henryk Iwaniec and Emmanuel Kowalski. Analytic Number Theory, volume 53 of
American Mathematical Society Colloquium Publications. American Mathematical Society,
Providence, RI, 2004. https://doi.org/10.1090/coll/053.
[17] Ernst Jacobsthal. Über Sequenzen ganzer Zahlen, von denen keine zu n teilerfremd ist.
I–III. Norske Vidensk. Selsk. Forh. Trondheim, 33:117–139, 1960.
82

## PDF page 83

[18] Vojtěch Jarník. Über die Gitterpunkte auf konvexen Kurven. Mathematische Zeitschrift,
24:500–518, 1926. https://dml.cz/handle/10338.dmlcz/500690.
[19] Jared Duker Lichtman. Primes in arithmetic progressions to large moduli, and shifted
primes without large prime factors. Preprint, arXiv:2211.09641v1, 2022. https://arxiv.
org/abs/2211.09641v1.
[20] H. L. Montgomery and R. C. Vaughan. The large sieve. Mathematika, 20(2):119–134,
1973. https://doi.org/10.1112/S0025579300004708.
[21] Hugh L. Montgomery and Robert C. Vaughan. Multiplicative number theory II: Primes
and sieves. Undated author draft. https://personal.science.psu.edu/rcv4/571s25/
montgomery-vaughanII.pdf. Accessed September 25, 2026.
[22] Hugh L. Montgomery and Robert C. Vaughan. Multiplicative number theory III. Undated draft. https://personal.science.psu.edu/rcv4/571s25/Vol3.pdf. Accessed
September 25, 2026.
[23] Richard Serfozo. Basics of Applied Stochastic Processes. Probability and Its Applications.
Springer, Berlin, Heidelberg, 2009. https://doi.org/10.1007/978-3-540-89332-5.
[24] Efthymios Sofos. Gaps between prime divisors and analogues in Diophantine geometry.
Glasgow Mathematical Journal, 65(S1):S129–S147, 2023. https://doi.org/10.1017/
S0017089522000398.
[25] R. C. Vaughan. On the order of magnitude of Jacobsthal’s function. Proceedings of
the Edinburgh Mathematical Society, 20(4):329–331, 1977. https://doi.org/10.1017/
S0013091500026560.
[26] Robert C. Vaughan. Math 571, chapter 5: The large sieve. Lecture notes, February
2025. Dated February 20, 2025. https://personal.science.psu.edu/rcv4/571s25/
Class571-05.pdf.
[27] Miguel N. Walsh. The inverse sieve problem in high dimensions. Duke Mathematical Journal, 161(10):2001–2022, 2012. https://doi.org/10.1215/00127094-1645788;
author version https://arxiv.org/abs/1105.1551v2.
[28] Miguel N. Walsh. The algebraicity of ill-distributed sets. Geometric and Functional
Analysis, 24(3):959–967, 2014. https://arxiv.org/abs/1307.0259.
[29] Mario Ziller. New computational results on a conjecture of Jacobsthal. Preprint,
arXiv:1903.11973v2, 2019. https://arxiv.org/abs/1903.11973v2.

83
