Source: https://doi.org/10.1007/s13540-021-00010-2
PDF sha256: b19c49cd8a0e2c4ff629fb6f2964f01a4a98a2ab52e7635b01bad443a80005b4
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of georgiou_scalas_2022_bounds_for_mixing_times_finite_semi_markov_processes.pdf

Transcription of `georgiou_scalas_2022_bounds_for_mixing_times_finite_semi_markov_processes.pdf` in this directory, 15 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-15 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Fractional Calculus and Applied Analysis (2022) 25:229–243
https://doi.org/10.1007/s13540-021-00010-2
ORIGINAL PAPER

Bounds for mixing times for finite semi-Markov processes
with heavy-tail jump distribution
Nicos Georgiou1 · Enrico Scalas1
Received: 15 September 2021 / Revised: 8 November 2021 / Accepted: 30 November 2021 /
Published online: 7 February 2022
© The Author(s) 2022

Abstract
Consider a Markov chain with finite state space and suppose you wish to change
time replacing the integer step index n with a random counting process N (t). What
happens to the mixing time of the Markov chain? We present a partial reply in a
particular case of interest in which N (t) is a counting renewal process with powerlaw distributed inter-arrival times of index β. We then focus on β ∈ (0, 1), leading
to infinite expectation for inter-arrival times and further study the situation in which
inter-arrival times follow the Mittag-Leffler distribution of order β.
Keywords discrete Markov Chains · mixing times · semi-Markov processes ·
fractional Poisson process
Mathematics Subject Classification 60K15 · 60J10 · 60J27 · 33E12 · 60G22

1 Introduction
1.1 Motivation
The original motivation for this paper stems from a 2011 paper [8] where a probabilistic theory for dynamic networks was presented. In particular, given a fixed set
of vertices, an embedded Markov chain was considered on the space of all possible
graphs connecting the vertices. This discrete-time chain was then transformed into a
continuous-time chain by means of a simple time change with a counting process. In
a subsequent paper [3], we explicitly solved one of the models presented in [8]. This

B Enrico Scalas

e.scalas@sussex.ac.uk
Nicos Georgiou
n.georgiou@sussex.ac.uk

1

Department of Mathematics, University of Sussex, Falmer, Brighton BN1 9QH, UK

123

## PDF page 2

230

N. Georgiou , E. Scalas

model is equivalent to an α-delayed version of the Ehrenfest urn chain and the time
change is the fractional Poisson process [4] of renewal type [6]. At that time, we initiated a discussion on how this time change for a discrete-time discrete-space Markov
chain affects mixing times and the convergence rate to equilibrium. Below we collect
results on this point in the interesting case in which the inter-arrival times between
two consecutive transitions of the embedded chain have a power-law distribution with
index β, also covering the case in which β ∈ (0, 1) meaning that the expected value
of the waiting times is infinite. In the latter case, under an appropriate choice of the
distribution of inter-arrival times, it is possible to show that the forward Kolmogorov
equations can be replaced by a fractional version with Caputo derivative of index β
(see e.g. [3] for details in the case mentioned above and [7] for a general theory) when
the initial time of the process is a renewal point.
The starting point of our discussion is that the continuous-time probabilities pi, j (t)
of being in state j at time t, given that the process was in state i at time 0 converge
to the same equilibrium distribution as in the case of the embedded chain. Then, in
Theorem 2, we prove lower and upper bounds for the mixing time of the continuoustime chain based on the mixing time of the embedded chain and, in Theorem 3, we
specialize the result to the case in which inter-arrival times follow the Mittag-Leffler
distribution where a sharper upper bound is available. We believe these bounds can be
useful for applied scientists simulating these processes, for instance to estimate how
far from equilibrium their simulations are.
1.2 Preliminaries
Let T1 , T2 , . . . be a sequence of independent positive random variables with the meaning of inter-event times or waiting times (with common law ν) and define the partial
sum
Sn =

n
∑

Ti , n ≥ 1.

(1.1)

k=1

The sequence S1 , S2 , . . . denotes the event times at which the state of the Markov
chain X (t) attempts to change.
The embedded Markov chain is a discrete time chain X n , n ≥ 1, with state space
(0)
S. Initially we assume an initial distribution μ(0) , i.e. P{X 0 = i} = μi and the
chain evolves according to a discrete transition kernel q : S × S → [0, 1]. As
usual, since S is finite, the transition kernel may be encoded as a transition matrix
Q = (qi, j )1≤i, j≤|S | . We will be assuming the chain X n is irreducible for convenience
of the exposition. Otherwise, all theorems below can be ascribed to each irreducible
component separately. Moreover we shall also assume that the chain X n is aperiodic.
Again, this is a technical point when discussing the convergence to equilibrium, as in
the irreducible aperiodic case we have almost sure convergence to the unique invariant
measure for the discrete chain.

123

## PDF page 3

Bounds for mixing times for finite semi-Markov...

231

We couple the embedded chain X n with the process X (t) via the counting process
Nν (t) = max{n ∈ N : Sn ≤ t}

(1.2)

that gives the number of events from time 0 up to a finite time horizon t. Then we
have
X (t) = X Nν (t) = X n 11{Sn ≤ t < Sn+1 },

(1.3)

i.e. the state of the process at time t is the same as that of the embedded chain after
the last event before time t occurred.
All information about X (t) is encoded in the pairs {(X n , Tn )}n≥1 which are a
discrete-time Markov renewal process, satisfying
P{X n+1 = j, Tn+1 ≤ t|(X 0 , S0 ), . . . , (X n = i, Sn )}
= P{X n+1 = j, Tn+1 ≤ t|X n = i}.

(1.4)

X (·) is then a semi-Markov process subordinated to Nν (t) where we use “subordination” with the meaning of “time change” with an abuse of language. Under the
assumption that μ0 = δi (deterministic starting point), the temporal evolution of its
transition probabilities satisfies the forward equations
pi, j (t) = F ν (t)δi j+

∑

∫ t
qℓ, j pi,ℓ (u) f ν (t − u) du.

(1.5)

0

ℓ∈S

Above we introduced pi, j (t) = P{X (t) = j|X (0) = i}, the tail (complementary
cumulative distribution function) F ν (t) = 1 − Fν (t) and f ν (t) the Radon-Nikodym
derivative of ν with respect to Lebesgue (the probability density function if appropriate
smoothness conditions are satisfied). These equations are proved by conditioning on
the time of the last event before time t and it is implicitly assumed that at t = 0 we
have a renewal point.
A conditioning argument on the values of Nν (t) gives
pi, j (t) = F ν (t)δi j +

∞
∑

qi,(n)j P{Nν (t) = n},

(1.6)

n=1

where qi,(n)j are the n-step transitions of the embedded discrete Markov chain, namely
the entries of the n-th power of the transition matrix Q = (qi, j )1≤i, j≤|S | .
From the ergodic theorem we have that for any i, j
(n)
lim q = π j > 0.
n→∞ i, j

This is sufficient to argue the following lemma.

123

## PDF page 4

232

N. Georgiou , E. Scalas

Lemma 1 Consider the transition probabilities given by (1.6) and assume that
lim qi,(n)j = π j . Then
n→∞

lim pi, j (t) = πi .

t→∞

Proof Let N large enough so that for a given ε > 0 we have for all n > N
(n)

|qi, j − πi | < ε.
Then, substituting in (1.6) we have
pi, j (t) = F ν (t)δi j +

∞
∑

(n)

qi, j P{Nν (t) = n}

n=1

≤ F ν (t)δi j +

N
∑

qi,(n)j P{Nν (t) = n} +

∞
∑

(πi + ε)P{Nν (t) = n}

n=N +1

n=1

≤ P{Nν (t) ≤ N } + (π j + ε)P{Nν (t) > N }.
Then as t → ∞ the first probability tends to 0, while P{Nν (t) > N } → 1. Then let
ε → 0 to obtain
lim pi, j (t) ≤ π j .

t→∞

The lower bound follows in a similar manner so we omit details.

⊔
⊓

This straightforward convergence result is the starting point of this discussion. In
discrete Markov chains, there is a substantial body of literature (see [5] and references therein) examining quantitative estimates on the convergence; this information
is encapsulated in information about the mixing times of the chain, using the total
variation distance between the two measures.
1.3 Total variation distance and mixing times for discrete chains
Let F denote the σ -algebra of events of a space and μ, ν two probability measures
on this space. Then the total variation distance between two measures is defined as
∥μ − ν∥ = sup |μ(A) − ν(A)| ∈ [0, 1]
A∈F

(1.7)

and one can show that for countable spaces
∥μ − ν∥ =

123

1∑
|μ(x) − ν(x)|.
2 x

(1.8)

## PDF page 5

Bounds for mixing times for finite semi-Markov...

233

Moreover, the total variation distance between two measures can be given in terms of
a different variational formula (coupling):
∥μ − ν∥ = inf{P{X ̸= Y } : (X , Y ) is a coupling of μ and ν}.

(1.9)

Both formulas have merit, as (1.7) can be used for a lower bound, while (1.9) for upper
bounds on mixing times.
For any ε > 0, we define the mixing time Tε of a finite state, aperiodic, irreducible
Markov chain to be
{
Tε = inf n :

∑

}
(n)
∥qi,· − π· ∥ ≤ ε

.

(1.10)

i∈S
(n)

The fact that ∥qi,· − π· ∥ is non-increasing in n means that for all N > Tε we have
(N )

∥qi,· − π· ∥ ≤ ε and that Tε are non-decreasing as ε → 0. Loosely speaking, for a
given tolerance ε, the mixing time tells us how long it takes the chain to start behaving
as if it is near equilibrium.
Equation (1.9) can be used to obtain an upper bound for the mixing times the following way. First we construct a coupling between the two Markov chains, where
X 0 ∼ δi , Y0 ∼ π . Both chains evolve according to the transition matrix Q independently, until they meet at some state x, after which the chains just jump to the same
location together, again according to Q. The marginals of the pair chain (X n , Yn ) are
still those of two Markov chains, so this description is indeed the description of a
coupling between the two.
At the instant where the two independent chains meet, the pair Markov chain
(X n , Yn ) hits the set
D = {(x, x) : x ∈ S}.
Let the hitting time of this set be
τ D = inf{n : (X n , Yn ) ∈ D}.
Then, using this coupling between the chains and (1.9) one can obtain
(n)

∥qi,· − π ∥ ≤ P{X n ̸= Yn } = Pδi ⊗π {τ D > n}.
At this point the general theory of Markov chains can assist with uniform estimates
on the hitting time, irrespective of the initial measure. This can be obtained by using
the fact that the two chains act independently from another- until they meet at time
τ D - and we have
∗

sup Pμ (τ D > n) ≤ c1 e−c2 n/ℓ D , ℓ∗D = max Eδi (τ D ),
μ

i

(1.11)

123

## PDF page 6

234

N. Georgiou , E. Scalas

where c1 , c2 are uniform constants. In particular this gives the bound
(n)

∗

∥qi,· − π ∥ ≤ c1 e−c2 n/ℓ D .
Using only Q one can derive upper bounds for ℓ∗D , so we treat that as a computable
constant. Now, if, overall, the upper bound is less than ε|S|−1 for some n ε then (1.10)
implies that Tε ≤ n ε . Forcing the upper bound in the display above to be less than
ε|S|−1 we have that
n ε > Cℓ∗D (− log ε + log |S|),
which in turn gives that there exists a function f (S, Q) such that
Tε ≤ f (S, Q)| log ε|,

(1.12)

which shows us how the mixing time depends on the order of ε.
For a lower bound, the most basic method involves counting; it relies on the idea that
if the possible locations of a chain after n jumps do not cover a substantial proportion
of the state space, we cannot be close to mixing. Then one can get
Tε >

log(|S|(1 − ε))
.
log c(Q)

(1.13)

The constant c(Q) only depends on the transition matrix. Note that the lower bound
above is not necessarily close to the upper bound, and as ε → 0 it gets weaker. The
ε-order of this agrees with the upper bound when |S| ∼ ε−1 . Many further methods
exist for lower bounds, but are usually model-dependent. We briefly mention that a
suitable L 2 theory exists for reversible, aperiodic, irreducible MCs so bounds on Tε
from below are of the same order as the upper bounds,
((γ ∗ )−1 − 1)| log 2ε| < Tε < (γ ∗ )−1 c Q | log ε|,
where γ ∗ is the spectral gap of Q (the difference between 1 and the second largest
eigenvalue λ2 ).

2 Results
In this short paper, we will bound mixing times for continuous semi-Markov processes
with heavy tails for the distribution of inter-event times. Using Lemma 1 we have that
the convergence occurs (albeit more slowly than Markov chains). The global time
change we performed on the chain will be reflected in the bounds for the mixing
times, as we obtain them in terms of the mixing times of the embedded discrete chain.
At this point, we want to impose some conditions on the distribution of the interevent times we are looking at. In particular:

123

## PDF page 7

Bounds for mixing times for finite semi-Markov...

235

Assumption We assume there are two uniform constants c1 and c2 , a t0 > 0 and a
β > 0 such that
c2
c1
≤ P{T > t} ≤ β ,
tβ
t

for all t > t0 .

(2.1)

Note that we are not assuming any moments exist for the inter-event distributions
as β can be in (0, 1). In the case where moments exist, the results sharpen.
For any ε > 0 we define the mixing time for the continuous semi-Markov chain to
be
{ ∑
}
Tεcont = inf t :
∥ pi,· (t) − π· ∥ ≤ ε .
(2.2)
i∈S

By Lemma 1 we know the pi,· converge to π so the above object is finite and well
defined.
2.1 Motivating examples
Example 1 (Diagonalizable transition matrix) In this example, we make the assumption that Q is the transition matrix of an irreducible, aperiodic Markov chain and in
particular that it is diagonalisable. Let π denote the unique invariant distribution of the
Markov chain and recall that π is a left 1-eigenvector for the matrix Q and the vector
1 = (1, . . . , 1) is a right 1-eigenvector. Since Q is diagonalisable, we have that there
exists a matrix L so that L Q L −1 = D and without loss of generality we may assume
that d11 = 1 and that ℓ1 j = π j . Furthermore, by the Perron-Frobenius theorem, the
1-eigenspace has dimension 1 and therefore the first column of L −1 = (ℓ̃i j ) is a right
1-eigenvector of Q and therefore satisfies ℓ̃i1 = 1.
Then Q n = L −1 D n L and on a coordinate by coordinate computation we have
(n)
qi j =

N
∑

ℓ̃ik λnk ℓk j = π j +

∑

ℓ̃ik λnk ℓk j .

k̸=1

k=1

The eigenvalues λk remaining in the sum all have |λk | < 1, with the sum vanishing as
n grows and the n-step transitions converging to the invariant distribution.
Substituting the last relationship back in (1.6), we have
pi, j (t) = F ν (t)δi j +

∞
∑
n=1

= F ν (t)δi j +

∞
∑
n=1

(n)

qi, j P{Nν (t) = n}
(
πj +

N
∑

)
ℓ̃ik λnk ℓk j

P{Nν (t) = n}

k=2

= π j (1 − P{Nν (t) = 0}) + F ν (t)δi j +

N ∑
∞
∑

ℓ̃ik λnk P{Nν (t) = n}ℓk j

k=2 n=1

123

## PDF page 8

236

N. Georgiou , E. Scalas

= π j + (δi j − π j )F ν (t) +

N
∑

ℓ̃ik

∞
∑
( n
)
λk P{Nν (t) = n} ℓk j

k=2

= πj +

N
∑

ℓ̃ik

= πj +

n=1

)
( n
λk P{Nν (t) = n} ℓk j

n=0

k=2
N
∑

∞
∑

)
(
N (t)
ℓk j
ℓ̃ik E λk ν

k=2

= πj +

N
∑

ℓ̃ik PNν (t) (λk )ℓk j .

k=2

Particularly, the convergence to equilibrium for a finite state space process only
depends on the tails of the probability generating function of Nν (t). Then, since Nν
is an increasing process and |λk | < 1, we may bound
sup | pi, j (t) − π j | ≤ C N PNν (t) (|λ2 |).

(2.3)

j

Therefore the total variation distance as a function of time only depends on the tails
of the probability generating function.
In fact, the following rough estimate can be performed, keeping in mind that |λ2 | <
1. Let K such that |λ2 | K < ε/2,
PNν (t) (|λ2 |) = E(|λ2 | Nν (t) 1{Nν (t) > K }) + E(|λ2 | Nν (t) 1{Nν (t) ≤ K })
≤ |λ2 | K + P{Nν (t) ≤ K } ≤ ε/2 + P{Nν (t) ≤ K }.
From Lemma 2 below, the second term above decays like K 1+β t −β and modulates
t in order to make this quantity arbitrarily small.
Example 2 (Mittag-Leffler waiting times) This example is taken from [2]. When
the waiting times Ti are Mittag-Leffler with parameter β, we have that PNν (t) (λ)
= E β ((λ − 1)t β ), where E β is the Mittag-Leffler function with parameter β ∈ (0, 1].
For large t values we have that
E β ((λ − 1)t β ) ∼ Cλ,β t −β ,
and therefore
sup | pi, j (t) − π j | ≤ Cλ2 ,β N t −β .
j

The total variation distance becomes less than ε > 0, when
(
t>

123

Cλ,β,N N
ε

)1/β
.

(2.4)

## PDF page 9

Bounds for mixing times for finite semi-Markov...

237

Fig. 1 Mittag-Leffler Ehrenfest chain at (left panel) and before (right panel) the bound for Tεcont as given
in Theorem 2. The abscissae represent states and the ordinates are their empirical frequencies (blue stars).
The expected distribution is binomial and is represented by the red stars

We compute an explicit value for Cλ,β,N later, in the proof of Theorem 2.
We are now ready to state the main theorem.
emb the ε/2-mixing time for the embedded
Theorem 1 Assume (2.1). Let ε > 0 and Tε/2
chain, be given by (1.10). Then for any β > 0 we can find explicit constants C1 so
that
emb 1+1/β
)
.
Tεcont < C1 ε−1/β (Tε/2

This theorem is quite general as it makes no further assumptions on the background
chain. Moreover, as is often the case for discrete Markov chains, a lot of the sophisticated estimates on mixing times are model dependent, so a theorem like Theorem 1
can utilise those bounds directly.
In the case where the inter-event times are Mittag-Leffler distributed we can make
the upper bound sharper.
Theorem 2 Let X (t) be a finite space semi-Markov process for which the inter-event
times are Mittag-Leffler(β) distributed. Then,
emb 1/β
) .
Tεcont < C2 ε−1/β (Tε/2

In Figure 1 we see a simulation of the fractional Ehrenfest chain for times before
and at the upper bound of the mixing time in Theorem 2.
A natural question arises about lower bounds for Tεcont . These are more challenging
to obtain for the total variation distance directly. However, by defining a different
distance between the measures we can obtain also lower bounds. Let
(Ns )
− π ∥ < ε, for all s > t}.
T̃εcont = inf{t : max E∥qi,·
i

(2.5)

123

## PDF page 10

238

N. Georgiou , E. Scalas

Note that
(N )

(N )

∥ pi,· (t) − π ∥ = ∥E(qi,· t ) − π ∥ ≤ E∥qi,· t − π ∥,
and therefore if the expected value (2.5) is less than ε then the total variation distance
is small. In particular this already gives
T̃εcont > Tεcont .
Using definition (2.5), we can however find bounds for T̃εcont .
Theorem 3 Assume (2.1). Let δ > 0 and Tδemb the δ-mixing time for the embedded
chain, be given by (1.10). Then for any β > 0, and any α ∈ (0, 1) we can find explicit
constants C1 < C2 so that
1/β
emb 1+1/β
< T̃εcont < C2 ε−1/β (Tε/2
)
.
C1 ε(α−1)/β (Tεemb
α )

We are now ready to present the proofs in the next section.

3 Mixing times and equilibrium
Lemma 2 Under assumption (2.1), let K ∈ N and let t > (t0 ∨ (2c2 )1/β )K . Then,
there exists a uniform positive constant C0 so that
c1 K
C0 K 2
c2 K 1+β
C0 K 1+2β
− 2β ≤ P{Nβ (t) < K } ≤
+
.
β
β
t
t
t
t 2β

(3.1)

Proof The assumptions of the lemma guarantee that all functions below are well
defined, all constants arising from Taylor’s theorem do not depend on t and the error
of Taylor’s theorem is small. When t > (t0 ∨ (2c2 )1/β )K we have
⎧
⎨

1 − P{Nβ (t) < K } = 1 − P t <
⎩

K
∑
j=1

⎫
⎬
Tj

⎭

}

{
≥ 1 − P t < K max T j
1≤ j≤K

( {
}) K
t
t
= P T1 ≤
= 1 − P max T j >
1≤ j≤K
K
K
)}
{
(
Kβ
≥ exp K log 1 − c2 β
t
}
{
β
K
K 2β
= exp −K c2 β − K Cup c22 2β , for a uniform Cup ,
t
t
{

≥ 1 − c2

123

}

1+2β
K 1+β
2K
−
C
c
.
up
2
tβ
t 2β

(3.2)

## PDF page 11

Bounds for mixing times for finite semi-Markov...

239

For a lower bound we can write
⎧
⎫
}
{
K
⎨
⎬
∑
T j ≥ P t < max T j
P{Nβ (t) < K } = P t <
⎩
⎭
1≤ j≤K
j=1

(
c1 ) K
= 1 − (P {T1 < t}) K ≥ 1 − 1 − β
t }
{
}
{
1
1
2 1
= 1 − exp −K c1 β − K C̃low c1 2β ≥ 1 − exp −K c1 β
t
t
t
(
)2
K c1
1
≥ K c1 β − Clow
, for a uniform constant Clow . (3.3)
t
tβ
The lemma follows from (3.2) and (3.3). The last inequality on the right side of (3.1)
comes directly from the assumption.
⊔
⊓
Proof of Theorem 1 It suffices to prove that for arbitrary M < L the total variation distance between the transition probabilities and the equilibrium distribution is bounded
above, according to the following
(M)

(L)

∥ pi,· (t) − π ∥ ≤ P{Nt < M} + ∥qi,· − π ∥ + ∥qi,· − π ∥P{Nt > L}.

(3.4)

emb . By the definition of T emb ,
Assume for the moment that (3.4) holds and set M = Tε/2
ε/2
the middle term on the right-hand side of (3.4) is bounded above by ε/2. Then let
L → ∞ so that the third term vanishes.
The left-hand side is then bounded by ε -and therefore the continuous process is
emb } ≤ ε/2. By Lemma 2 this happens whenever
ε-mixed- if P{Nt < Tε/2

(
t>

2(c1 + C0 )
ε

)1/β (

emb
Tε/2

)1+1/β

emb
∨ (t0 ∨ (2c2 )1/β )Tε/2
,

and therefore
emb 1+1/β
Tεcont < C2 ε−1/β (Tε/2
)
.

(3.5)

The theorem is proven when we establish (3.4). To this end,
2∥ pi,· (t) − π ∥ =

∑

| pi, j (t) − π j |

j∈S

∣∞
∣
∞
∣ ∑∑
∑ ∣∣∑
∣
(n)
(n)
|qi, j − π j |P{Nt = n}
=
∣ (qi, j − π j )P{Nt = n}∣ ≤
∣
∣
j∈S n=0

≤ P{Nt < M} +

j∈S n=0

L
∑∑

(n)

(L)

|qi, j − π j |P{Nt = n} + 2∥qi,· − π ∥P{Nt > L}

j∈S n=M

123

## PDF page 12

240

N. Georgiou , E. Scalas
(M)

(L)

≤ P{Nt < M} + 2∥qi,· − π ∥P{M ≤ Nt ≤ L} + 2∥qi,· − π ∥P{Nt > L}.
⊔
⊓
Proof Theorem 2 When the counting process Nβ (t) has Mittag-Leffler(β) inter-event
times, we have
n̄ t = E(Nβ (t)) =

[
]
β B(β, 1/2)
tβ
−
1
,
, E(Nβ2 (t)) = n̄ t + (n̄ t )2
(1 + β)
22β−1

(3.6)

where B(·, ·) is the beta function.
As in Example 2,
pi, j (t) = F ν (t)δi j +

∞
∑

qi,(n)j P{Nν (t) = n} =

n=1

∞
∑

qi,(n)j P{Nν (t) = n}

n=0

∞
∑
∗
≤
(π j + c1 e−n/eℓ D )P{Nν (t) = n}
n=0
∗

= π j + c1 M Nν (t) (−1/eℓ∗D ) = π j + c1 E β ((e−1/eℓ D − 1)t β ).

(3.7)

Here, M Nβ (t) (s) is the moment generating function of the counting process Nβ (t),
while E β is the Mittag-Leffler function with parameter β. ℓ∗D is defined in equation
(1.11).
We will extrapolate mixing times asymptotics by forcing
∗

c1 E β ((e−1/eℓ D − 1)t β ) = c1 M Nβ (t) (−1/eℓ∗D ) < ε.
The equality between this two quantities is a beautiful fact of the Mittag-Leffler function. The derivation of the moment generating function can be found in the book [1]
and in [4].
One way to bound above the moment generating function is by
{
M Nν (t) (−1/eℓ∗D ) ≤ P Nβ (t) ≤ θ

}
tβ
∗
β
+ e−θt /e(1+β)ℓ D .
(1 + β)

(3.8)

The constant θ is to be determined so that each term above is bounded by ε/2. For the
first term we will use the Paley-Zygmound inequality. For any θ ∈ [0, 1] we have
{

tβ
P Nβ (t) ≥ θ
(1 + β)

}
≥

(1 − θ )2 E(Nβ (t))2
Var(Nβ (t)) + (1 − θ )2 E(Nβ2 (t))

=

(1 − θ )2 n̄ 2t
(
)
((1 − θ )2 + 1)n̄ t + n̄ 2t β B(β,1/2)
−
1
2β−1
2

=

123

(1 − θ )−2

(

1
)

β B(β,1/2)
−1
22β−1

+ (1 + (1 − θ )−2 )n̄ −1
t

.

## PDF page 13

Bounds for mixing times for finite semi-Markov...

241

The function β B(β,1/2)
− 1 is monotonically decreasing in β and takes values in (0, 1).
22β−1

therefore there is a unique θ ∗ (β) in (0, 1) so that (1 − θ ∗ (β))−2 ( β B(β,1/2)
− 1) = 1.
22β−1
For the particular value of θ ∗ we bound
{
θ ∗ (β)t β }
P Nβ (t) ≥
(1 + β)
(1 + (1 − θ ∗ (β))−2 )(1 + β)
(1 + (1 − θ ∗ (β))−2 )
=1−
.
≥1−
n¯t
tβ
In particular, we obtain
{

θ ∗ (β)t β
P Nβ (t) ≤
(1 + β)

}
≤

Cβ
(1 + (1 − θ ∗ (β))−2 )(1 + β)
= β.
β
t
t

(3.9)

This is a much improved bound for the probability, than the one established in Lemma
2. Impose that the upper bound in (3.9) is less than ε/2 to obtain that
(
t>

2Cβ
ε

)1/β
.

(3.10)

Similarly, set
∗

β

∗

e−θ (β)t /e(1+β)ℓ D < ε/2 ⇐⇒ t >

(

e(1 + β) ∗
2
ℓ D log
∗
θ (β)
ε

)1/β
.

(3.11)

Combine (3.10) and (3.11) in (3.8), which in turn can bound (3.7) to conclude that the
relation
}
)
(
{
e(1 + β) ∗ 2c1 1/β
ℓ
,
(3.12)
Tεcont ≤ max Cβ ,
D
θ ∗ (β)
ε
⊔
⊓

as required.

Proof of Theorem 3 Using definition (2.5), we can however find a lower bound for
T̃εcont . We have that for any M positive,
(N )

(N )

(M)

E∥qi,· t − π ∥ ≥ E(∥qi,· t − π ∥1{Nt < M}) ≥ ∥qi,· − π ∥P{Nt < M}. (3.13)
If we set M = 21 Tεemb
α , we have
}
{
1
(N )
,
E∥qi,· t − π ∥ ≥ εα P Nt < Tεemb
α
2
1−α , in order for the two
and therefore it suffices to have P{Nt < Tεemb
α /2} > ε
measures to not be close in distance (2.5). This is enough to guarantee

}
}
{
{
1
≥ ε1−α .
T̃εcont ≥ sup t : P Nt < Tεemb
α
2

123

## PDF page 14

242

N. Georgiou , E. Scalas

At this point we need to separate two cases, depending on the assumption of Lemma
2. If β < 1, then the assumption of the lemma requires
t > C(t0 , c2 , β)Tεemb
α
in order to use (3.1), while we must also have
t β > C(t0 , c2 , β)Tεemb
α ,

(3.14)

so that the lower bound in Lemma 2 is non-negative. Then
T emb
α
1/β
ε1−α < C̃(t0 , c2 , β) ε β ⇐⇒ t < C̃(t0 , c2 , β)ε(α−1)/β (Tεemb
.
α )
t

(3.15)

In order for both inequalities (3.14) and (3.15) to be satisfied, we need (modulo the
constants)
1 < ε(α−1)/β
which is true as α < 1. Therefore in the case β < 1
1/β
> C1 ε(α−1)/β (Tεemb
.
T̃εcont
α
α )

Now suppose that β ≥ 1. Then for the estimate in Lemma 2 to be meaningful (i.e. the
lower bound is strictly greater than 0), we need that t β > Tεemb
α . This is guaranteed by
the assumption of Lemma 2 and we obtain
T̃εcont
α

Lemma 2

>

1/β
C1 ε(α−1)/β (Tεemb
.
α )

Now for the upper bound in the theorem, we can repeat the arguments of Theorem
1. We have
(N )

E∥qi,· t − π ∥ =

∞
∑

(n)

∥qi,· − π ∥P{Nt = n},

n=0

and therefore bound (3.4) and all subsequent arguments work for this distance as well.
⊔
⊓
Acknowledgements Both authors were partially supported by the Dr Perry James (Jim) Browne Research
Center at the Department of Mathematics, University of Sussex.
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which
permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence,
and indicate if changes were made. The images or other third party material in this article are included
in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If
material is not included in the article’s Creative Commons licence and your intended use is not permitted

123

## PDF page 15

Bounds for mixing times for finite semi-Markov...

243

by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the
copyright holder. To view a copy of this licence, visit http://creativecommons.org/licenses/by/4.0/.

References
1. Baleanu, D., Diethelm, K., Scalas, E., Trujillo, J.J.: Fractional Calculus: Models and Numerical Methods.
World Scientific, Singapore (2016)
2. de Nigris, S., Hastir, A., Lambiotte, R.: Burstiness and fractional diffusion on complex networks. Eur.
Phys. J. B 89, Art. 114 (2016)
3. Georgiou, N., Kiss, I.Z., Scalas, E.: Solvable non-Markovian dynamic network. Phys. Rev. E 92, Art.
042801 (2015)
4. Laskin, N.: Fractional Poisson process. Commun. Nonlinear Sci, Numer. Simul. 8, 201–213 (2003)
5. Levin, D.A., Peres, Y., Wilmer, E.L.: Markov Chains and Mixing Times. American Mathematical Society
(2009)
6. Mainardi, F., Gorenflo, R., Scalas, E.: A fractional generalization of the Poisson process. Vietnam J.
Math. 32(SI), 53–64 (2004)
7. Meerschaert, M.M., Toaldo, B.: Relaxation patterns and semi-Markov dynamics. Stoch. Process. Their
Appl. 129(8), 2850–2879 (2019)
8. Raberto, M., Rapallo, F., Scalas, E.: Semi-Markov graph dynamics. Plos One 6(8), Art. e23370 (2011)
Publisher’s Note Springer Nature remains neutral with regard to jurisdictional claims in published maps
and institutional affiliations.

123
