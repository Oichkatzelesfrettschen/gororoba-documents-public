Source: https://doi.org/10.1103/PhysRevD.104.126011
PDF sha256: 5959df5b62abcb300c20386b79a34b95e850c786e34aa3079dbdd23660c1ac67
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of aharony_2021_ads_from_cft_for_scalar_qed.pdf

Transcription of `aharony_2021_ads_from_cft_for_scalar_qed.pdf` in this directory, 21 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-21 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW D 104, 126011 (2021)

AdS from CFT for scalar QED
Ofer Aharony ,* Shai M. Chester,† and Erez Y. Urbach

‡

Department of Particle Physics and Astrophysics, Weizmann Institute of Science, Rehovot 7610001, Israel
(Received 23 September 2021; accepted 16 November 2021; published 10 December 2021)
We construct an explicit bulk dual in anti–de Sitter space, with couplings of order 1=N, for the SUðNÞsinglet sector of QED in d space-time dimensions (2 < d < 4) coupled to N scalar fields. We begin from
the bulk dual for the theory of N complex free scalar fields that we constructed in our previous work, and
couple this to Uð1Þ gauge fields living on the boundary in order to get the bulk dual of scalar QED (in
which the Uð1Þ gauge fields become the boundary value of the bulk vector fields). As in our previous work,
the bulk dual is nonlocal but we can write down an explicit action for it. We focus on the CFTs arising at
low energies (or, equivalently, when the Uð1Þ gauge coupling goes to infinity). For d ¼ 3 we discuss also
the addition of a Chern-Simons term for Uð1Þ, modifying the boundary conditions for the bulk gauge field.
We also discuss the generalization to QCD, with UðN c Þ gauge fields coupled to N scalar fields in the
fundamental representation (in the large N limit with fixed N c ).
DOI: 10.1103/PhysRevD.104.126011

I. INTRODUCTION AND SUMMARY
The AdS=CFT correspondence [1–3] is an equivalence
between theories of quantum gravity on asymptotically
anti–de Sitter (AdS) space in d þ 1 dimensions, and
conformal quantum field theories (CFTs) in d dimensions.
Since for d ≥ 2 we do not have any nonperturbative
definition of these quantum gravity theories, the correspondence should be viewed as providing a nonperturbative definition for these theories in terms of the
corresponding quantum field theories, whenever those
are known and well understood. In many cases of the
correspondence the gravitational theories have a classical
limit, in which the ratio of the Planck scale to the radius of
anti–de Sitter space goes to infinity, and which corresponds to a large N limit of some sort in the CFT side. In
those cases one can test the correspondence by checking
that the semiclassical expansion on the gravity side
agrees with the large N limit of the corresponding field
theories.
A derivation of the AdS=CFT correspondence requires
showing that the CFT can be rewritten as a quantum gravity
theory, in the sense that its 1=N expansion reproduces
the corresponding perturbative expansion around some
*
†
‡

ofer.aharony@weizmann.ac.il
iahs81@gmail.com
erez.urbach@weizmann.ac.il

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI. Funded by SCOAP3.

2470-0010=2021=104(12)=126011(21)

gravitational solution in AdS space. While one can often
test this for specific observables, providing such a derivation for the full theory is challenging (see [4–7] for some
recent progress in relating free d ¼ 2 symmetric orbifold
CFTs to string theory on AdS3 ). In our recent paper [8] we
provided such a derivation for the simplest case of the
AdS=CFT correspondence—the duality [9] between the
UðNÞ-singlet sector of N free complex scalar fields in d
dimensions, and a theory of higher-spin gravity on AdSdþ1 .
Our derivation in [8] followed the methods of bi-local
holography [10–15], in its Lorentz-invariant version.
We first changed variables in the CFT from the N
free scalar fields ϕI ðxÞ (I ¼ 1; …; N) to their bi-local
combinations
Gðx1 ; x2 Þ ≡

N
1X
ϕ ðx Þϕ ðx Þ;
N I¼1 I 1 I 2

ð1:1Þ

which capture all the information about UðNÞ-invariant
observables in the theory (at least in flat space). In the large
N expansion one can write down an action for Gðx1 ; x2 Þ
that reproduces the correlators of the original theory, to all
orders in 1=N (as discussed in [8], the mapping to the
bilocal variables makes sense also for finite N but it is more
subtle then, and in this paper we only discuss the theory in
the 1=N expansion). In order to map this to a theory in AdS
space, we first expanded the bi-local field Gðx1 ; x2 Þ in a
basis of eigenstates of the Euclidean conformal group
SOðd þ 1; 1Þ. We then showed that the same eigenstates
appear in the expansion of transverse traceless fields
ΦJ ðx; zÞ of spin J (J ¼ 0; 1; 2; …) living on a fixed
AdSdþ1 space, enabling a one-to-one mapping between

126011-1

Published by the American Physical Society

## PDF page 2

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

these fields and the bi-local (1.1). Using this mapping we
rewrote the action of the original theory as an action (with
coupling 1=N) for fields in AdS space. This action is
explicitly known but is nonlocal. For a specific choice of
the undetermined coefficients appearing in the mapping,
the quadratic term in the bulk can be chosen to be local.
Since the UðNÞ-singlet sector of N free scalars is conjectured [9] to be dual to Vasiliev’s high-spin gravity theory
[16–18], we believe that our action is equivalent to a gaugefixed version of this theory, in which its fields live on a
fixed AdS space-time (as in [19]); the spectrum of physical
fields is consistent with this, but the equivalence has not yet
been shown.
In this paper, we generalize this construction to the
SUðNÞ-singlet sector of scalar QED—the theory of a Uð1Þ
gauge field minimally coupled to N charged scalar fields,
for 2 < d < 4. In principle this generalization is straightforward, since on the field theory side it just involves
introducing a dynamical Uð1Þ gauge field and coupling it to
SUðNÞ-singlet combinations of the scalar fields, and we
can in principle do this also on the gravity side. On-shell,
local SUðNÞ-invariant operators (such as the ones appearing in the coupling to the gauge field) map to the boundary
values of the bulk fields on AdS space; however, the
construction above requires the off-shell mapping of the
local CFT operators to the bulk, and at first sight this seems
to be more complicated. In [8] we showed that for J ¼ 0
and d < 4 the naive on-shell mapping works also off-shell,
and we used it there to derive the dual to the critical UðNÞ
(or OðNÞ) vector model, by coupling a singlet σðxÞ to the
spin J ¼ 0 operator ϕI ðxÞϕI ðxÞ. In this paper we show that
the same is true also for J ¼ 0 and d > 4, and also for
higher values of J. This allows us to write down a simple
action for the d-dimensional Uð1Þ gauge field coupled to
the bulk fields; in fact, as may have been expected [20–24],
the Uð1Þ gauge field becomes simply the boundary value of
the (d þ 1)-dimensional vector field Φ1 ðx; zÞ. Thus, compared to the original theory of N free scalars, the description of QED just involves changing the boundary condition
for the bulk vector field Φ1 , and perhaps adding some
boundary terms for it. The boundary terms are required if
one wants to describe QED at finite coupling, but they
disappear in the low-energy limit, where QED (for
2 < d < 4) flows to a conformal field theory (at least at
large N and to all orders in 1=N [25], and perhaps also for
all finite values of N [26,27]).1 In the special case of d ¼ 3
one can also add a Chern-Simons coupling at level k; when
k=N is kept fixed in the large N limit, this coupling is
translated into a modified boundary condition for the bulk
vector field.

For d ¼ 4 − ϵ dimensions with small ϵ and any value of N,
this fixed point is weakly coupled, but this does not play a role in
our construction.
1

One application of our bulk formalism for QED would
be to find classical solutions in the bulk describing
monopole operators, and perhaps to use them to compute
their correlation functions. As we discuss below, our
formalism only includes monopole operators if there is
no Chern-Simons coupling for the Uð1Þ, and it may be
interesting to look for ways to get around this problem so
that monopoles in Chern-Simons-matter theories may also
be incorporated.
We also generalize our construction to the SUðNÞ
singlet sector of N scalar fields in the fundamental
representation of a UðN c Þ gauge field (“scalar QCD”
[28]), when N c is kept fixed in the large N limit, and for
d ¼ 3 we can again include a Chern-Simons level k. The
bulk dual is very similar to the N c ¼ 1 QED case, except
the bulk fields now transform in the adjoint representation
of UðN c Þ. Note that this limit is different from the large
N c , k and fixed λ ≡ N c =k limit considered in [29], which
is believed to also be dual to a parity breaking higher
spin bulk theory. It would be interesting to see if
the generalization of our construction to this limit just
involves changing boundary conditions, or explicitly
changes the bulk interaction terms as a function of λ
(see discussions in [23,30]). Such a generalization, as
well as the inclusion of fermions, would allow us to
similarly construct the bulk dual of ABJ theory [31] in its
higher spin limit, which could ultimately lead to a
connection to string theory and M-theory via the ABJ
triality [23,32].
Finally, our off-shell mapping allows us to construct the
bulk dual for the critical UðNÞ or OðNÞ vector model for
4 < d < 6, as discussed in [33,34]. This CFT is not
unitarity at finite N due to complex large N instantons
[35], but is unitary in the 1=N expansion. It would be
interesting to study the classical solutions corresponding to
these instantons from the bulk perspective using our
construction.
We begin in Sec. II by describing the SUðNÞ-singlet
sector of scalar QED in bi-local variables, and translating
its action to these variables. In Sec. III we review the
mapping found in [8] between the free scalar theory and the
bulk, and extend it to an off-shell mapping for local
operators in the CFT. In Sec. IV we then use this mapping
to construct the bulk dual for the SUðNÞ-singlet sector of
scalar QED, and show that it reproduces the 1=N expansion
of this theory. Finally, in Sec. V we discuss the generalization to scalar QCD.
II. SCALAR QUED IN THE BILOCAL FORMALISM
We begin in this section by discussing QED with N
charged scalars in the bilocal formalism. First we will
discuss scalar QED in the usual local formalism in a general
dimension 2 < d < 4, as well as in d ¼ 3 where we can
add a Uð1Þ Chern-Simons term with level k. We will then
review how in d ¼ 3 one can realize the restriction to

126011-2

## PDF page 3

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)

SUðNÞ-singlet fields in a local fashion, by coupling to a
non-Abelian UðNÞ Chern-Simons theory at level k0 and
taking k0 → ∞, before coupling to the Uð1Þ gauge field
of QED. Finally, we will write the path integral for
the SUðNÞ-singlet sector of scalar QED in the bilocal
language, following the discussion of free scalars in
[10,36], and perform a saddle point expansion at large
N. In the 3d case we fix κ ¼ k=N to be finite in the large
N limit.
A. The local formalism
We begin by discussing the conventional local formalism
for QED with N complex scalars ϕI on Euclidean Rd for
2 < d < 4, following [37–40]. The actions for this theory
can be assembled by starting with the (Euclidean) free
theory action
Z
S free ½ϕ ¼ dd x∂ i ϕI ðxÞ∂ i ϕI ðxÞ;
ð2:1Þ
where all repeated indices are summed, including the
upper/lower I ¼ 1; …; N indices for the fundamental/
antifundamental of the UðNÞ global symmetry, and the
i ¼ 1; …; d index for the SOðdÞ Euclidean rotations. We
can then gauge the Uð1Þ subgroup by adding a Maxwell
term with scalar couplings:
Z
S e ½ϕ; A ¼

energies). This theory is believed to flow in the IR to an
interacting CFT called the CPN−1 or Abelian Higgs model2:
S CPN−1 ½ϕ; A; σ ≡ S free ½ϕ þ S e→∞ ½ϕ; A þ S λ→∞ ½ϕ; σ;
ð2:4Þ
where e; λ → ∞ since the Maxwell term is irrelevant while
ðϕI ϕI Þ2 is relevant (near the free UV fixed point).3 In d ¼ 3,
we can generalize this CFT by adding a level k ChernSimons term
Z
S k ½A ¼ −

Z
S λ ½ϕ; σ ¼



1 2
1

I
d x − σ þ pﬃﬃﬃﬃ σϕI ϕ ;
4λ
2 N
d

G0 ðx1 ; x2 Þ ¼

ð2:2Þ

where Ai is a Uð1Þ gauge field with field strength Fij , the
Uð1Þ current is J i , the seagull term is required by gaugepﬃﬃﬃﬃ
invariance, and we rescaled e2 → e2 =N and Ai → Ai = N
for later convenience in the large N limit. This action
retains the SUðNÞ subgroup of the original UðNÞ global
symmetry, and also has a new (d − 3)-form Uð1ÞT global
symmetry generated by the Hodge dual field strength F
[41,42]. The ϕI are uncharged under Uð1ÞT , but we can
couple it to codimension-3 operators, which in d ¼ 3
become local operators called monopole operators [43].
λ
Finally, we should add a quartic coupling 4N
ðϕI ϕI Þ2 ,
which can be equivalently written by using a HubbardStratonovich field σ as
ð2:3Þ

λ
ðϕI ϕI Þ2 term. The
where integrating out σ recovers the 4N
most general UV action for a Uð1Þ gauge theory coupled to
N complex scalars with relevant couplings in 2 < d < 4 is
then given by S free þ S e þ S λ, as well as a mass term (which
we will always fine-tune to have vanishing mass at low

ik
ε A∂ A;
4πN ijl i j l

ð2:5Þ

where k ∈
Z (recall that we rescaled the gauge field by a
pﬃﬃﬃﬃ
factor of N ). Note that this term is marginal in 3d, unlike
the Maxwell term which dropped out for e → ∞.
In general the fixed point written above is strongly
coupled, but it becomes weakly coupled at large N, and it
can be studied perturbatively in a 1=N expansion. We begin
by writing down the Feynman rules for this expansion. The
propagator for ϕI is



1
Ai
Ai Ai  I
p
ﬃﬃﬃﬃ
;
dd x
F
F
þ
J
½ϕ
ϕ
þ
ϕ
ij ij
i
N I
4e2
N

Ji ½ϕ ≡ iðϕI ∂ i ϕI − ϕI ∂ i ϕI Þ;

d3 x

Γðd=2 − 1Þ
1
:
d=2
jx1 − x2 jd−2
4π

ð2:6Þ

For σ, we have the momentum space σ propagator and the
one-loop correction from the ϕ2 bubble diagram
3−d

Dσ ðpÞ ¼ −2λ;

Bϕ2 ðpÞ ¼ −jpj

d−4

21−2d π 2
;
πd
Γðd−1
2 Þsinð 2 Þ

ð2:7Þ

where the former comes from the trivial quadratic term σ 2 ,
while the latter comes from the 2p1ﬃﬃﬃ
σϕI ϕI vertex and is
N

simply G0 ðx; 0Þ2 =4 in momentum space. Since both are
OðN 0 Þ, at leading order in 1=N we need to resum an infinite
geometrical series of bubble diagrams to obtain the
effective σ propagator (see Fig. 1)

This expectation is supported by lattice data for d ¼ 3 and all
values of N [26,27], and by analytic results in the large N limit for
all values of d [25]. We will take (2.4) to be a formal definition of
the IR CFT, which should be valid for all values of d and N for
which this CFT exists.
3
At large N one can also tune λ ¼ 0 to get a different IR CFT
called the tricritical QED theory, but for d ¼ 3 it is not clear if the
fixed point exists at finite N.

126011-3

2

## PDF page 4

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

FIG. 1. Bubble diagrams contributing to the effective σ propagator hσðxÞσð0Þiλ at leading OðN 0 Þ order. Thick lines correspond to σ
contractions, and dashed lines to the scalars ϕI .

Z
hσðxÞσð0Þiλ ¼

dd p ip·x
e ½Dσ ðpÞ þ Dσ ðpÞBϕ2 ðpÞ
ð2πÞd

case, a simple family of gauges that has this property
involves an average over different gauge-fixings, which is
implemented by adding to the action the nonlocal gaugefixing term

× Dσ ðpÞ þ … þ OðN −1 Þ
Z
dd p
2λeip·x
−1
Þ:
¼−
3−d þ OðN
d
ð2πÞ
jpjd−4 21−2d π 2
1 − 2λ Γðd−1Þ sinðπdÞ
2

2

ð2:8Þ

8
R d d ∂ i Ai ðxÞ∂ j Aj ðyÞ
Γðd2Þ2
1
>
>
< 1−ζ 8πd ðd−1Þðd−2Þ d xd y jx−yj2d−4 d ≠ 3


S ζ ½A ¼
R 3 3 ∂ i Ai ðxÞ∂ j Aj ðyÞ
>
1
κ2
1
>
d xd y jx−yj2
þ
d ¼ 3;
: 1−ζ π4 64π2

In the IR CFT at λ → ∞, this becomes the propagator of a
dimension two operator:
hσðxÞσð0Þi∞ ¼

d−1
2dþ3 sinðπd
2 ÞΓð 2 Þ 1
þ OðN −1 Þ:
3
jxj4
π 2 Γðd2 − 2Þ

ð2:9Þ

For the gauge field Ai , we must fix a gauge in order to
write down its propagator. It is convenient to choose a
gauge such that the IR limit e → ∞ can be taken immediately. As discussed in [37] for the similar fermionic QED3

ð2:10Þ
where κ ≡ k=N, and we chose a different coefficient for d ¼
3 for later convenience. This arises by averaging over
different ∂ i Ai ðxÞ ¼ ωðxÞ gauges
with a nonlocal weight
R
proportional to ð1 − ζÞ−1 dd xdd yωðxÞωðyÞ=jx − yj2d−4 ,
where ζ ∈ R; the limit ζ → 1 recovers the usual Landau
gauge ∂ i Ai ¼ 0. Using this gauge-fixing term, along with
the Maxwell term in (2.2), and for d ¼ 3 the CS term in (2.5),
we can find the momentum-space gauge field propagator

8 

pi pj
>
2d−2 π d=2 ΓðdÞ pi pj
e2
>
>
< p2 δij − jpj2 þ ð1 − ζÞ Γð2−d2ÞΓðd2Þ2 jpjd
 


DMax
ij ðpÞ ¼
>
pi pj
p
>
1
1
κ
16π 2 pi pj
l
>
: p2 κ2 e2 δij − jpj2 − 2π εijl jpj2 þ ð1 − ζÞ 64κ2 þπ2 jpj3
þ
e4 4π 2

d≠3
ð2:11Þ
d ¼ 3:

The coupling J i Ai and the contact term A2i ϕ2 in (2.2) both contribute to the momentum space photon self-energy at oneloop order
Z
Bij ðpÞ ¼





Γð2 − d2ÞΓðd2Þ2 d−2
2δij ð2k þ pÞi ð2k þ pÞj
pi pj
dd k
−
¼
−
δ
;
þ
−
jpj
ij
jkj2
jk þ pj2 jkj2
jpj2
ð2πÞd
2d−2 π d=2 ΓðdÞ

ð2:12Þ

where we see that the only role of the A2i ϕ2 term is to cancel a divergence in the contribution of the Ji Ai term. As with σ, at
leading order in 1=N we need to resum an infinite geometric series of bubble diagrams to find the effective photon
propagator (see Fig. 2)

FIG. 2. Bubble diagrams contributing to the effective photon propagator hAi ðxÞAj ð0Þiζ;e;k at leading OðN 0 Þ order. Squiggly lines
correspond to photon contractions DMax
ij , and dashed lines to the scalars ϕI .

126011-4

## PDF page 5

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)

Z

dd p ip·x Max
Max
−1
e ½Dij ðpÞ þ DMax
ik ðpÞBkl ðpÞDlj ðpÞ þ … þ OðN Þ
ð2πÞd


p p
8R
e2 ðδij − i 2j Þ
pi pj
2d−2 π d=2 ΓðdÞ
dd p ip·x
jpj
>
>
e
þ Γð2−dÞΓðdÞ2 ð1 − ζÞ jpjd þ OðN −1 Þ d ≠ 3
>
Γð2−dÞΓðdÞ2 e2
< ð2πÞd
2
2
jpj2 þ d−2 2d=2 2
2
π
ΓðdÞjpj2−d
¼


p p
p
jpj
>
ð 1 þ Þðδ − i j Þ− κ ε l
>
R
>
: d3 p3 eip·x 16 e2 ijjpj jpj2 2 22π ijl jpj þ 16 2 ð1 − ζÞ pi p2j þ OðN −1 Þ
d ¼ 3;
1
κ
64κ
jpj
ð2πÞ jpj

hAi ðxÞAj ð0Þiζ;e;k ¼

ð16þ 2 Þ þ
e

1þ

4π 2

ð2:13Þ

π2

where the k label is only there for d ¼ 3. In the IR CFT at e → ∞ the expression simplifies and we obtain the momentum
space propagator

hAi ðpÞAj ð−pÞiζ;∞;k ¼

8


d−2 d=2
pi pj
>
1 2 π ΓðdÞ
>
δ
þ OðN −1 Þ d ≠ 3
−
ζ
>
ij
< jpjd−2 Γð2−dÞΓðdÞ2
jpj2
2

>
>
>
:

2

p p
pl
16ðδij −ζ i 2j Þ−128κ
π εijl jpj
jpj
1
2
jpj
1þ64κ2
π

þ OðN −1 Þ

d¼3

from which we can go to position space to get
8
x x
ðd−2−ζÞδij þ2ζ i 2j
>
ΓðdÞ
>
jxj
>
þ OðN −1 Þ
d≠3
< 2Γð2−dÞΓðdÞ3
2
jxj
2
2


hAi ðxÞAj ð0Þiζ;∞;k ¼
>
xi xj
xl
>
8
1
κ
−1
>
: π2 þ64κ2 jxj2 ð1 − ζÞδij þ 2ζ jxj2 þ 4 εijl jxj þ OðN Þ d ¼ 3:

Note that the choice of gauge in (2.10) allowed us to take
e → ∞ in the propagator, while other gauge choices such as
Rξ gauge would give superficial divergences in this limit,
which would only cancel after computing gauge-invariant
observables.
Using these Feynman rules including the resummed
propagators, we can compute correlation functions in
scalar QED, in an expansion in 1=N similar to the large
N expansion of vector models.
B. A subtlety in restricting to the singlet sector
We will be interested in the SUðNÞ singlet sector of
scalar QED. In general d, we can simply restrict to this
sector by hand, which has no nontrivial effects on Rd . For
d ¼ 3 and nonzero k, we need to be more careful. What we
actually do is first restrict the theory of N scalars to its

ð2:15Þ

UðNÞ-invariant sector, and then couple this sector to the
Uð1Þ gauge field. We can perform the restriction in a
rigorous way [44] by coupling the theory to a UðNÞ ChernSimons term at infinite level before coupling to the new
Uð1Þ gauge field, and we will use this to show that
monopole operators cannot appear in the singlet sector
(as we define it here) when k ≠ 0. Thus, for d ¼ 3 and
nonzero k our theory is not precisely the same as the
SUðNÞ-singlet sector of scalar QED (which could have
SUðNÞ-singlet monopole operators), but we will still call it
by this name. In all other cases our theory includes the full
SUðNÞ-singlet sector of scalar QED.
Let us start by considering the free theory with action
S free in d ¼ 3, with global symmetry UðNÞ. We can gauge
this UðNÞ by adding a UðNÞk0 Chern-Simons term for a
gauge field Bi , with scalar couplings:





ik0
2i J K I
I
J
J
I
J
I

K
S k0 ¼ d x − εijl Bi J ∂ j Bl I − Bi I Bj J Bl K þ Ji I Bi J þ Bi I Bi J ϕK ϕ
3
4π


Z
0
iNk
¼ d3 x −
εijl Bi ∂ j Bl þ J i Bi þ NBi Bi ϕI ϕI þ SUðNÞ terms ;
4π
Z

ð2:14Þ

3

where Bi IJ is the UðNÞ gauge field, Ji JI ≡ iðϕI ∂ i ϕJ −
ϕJ ∂ i ϕI Þ is the UðNÞ current, and in the second line we
separated out the SUðNÞ ⊂ UðNÞ terms from the Uð1Þ

BI

ð2:16Þ

gauge field Bi ≡ Ni I , which couples to the Uð1Þ current J i
defined in (2.2). The gauge-invariant operators are then all
singlets of UðNÞ, as we want, but the theory is modified by

126011-5

## PDF page 6

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

the extra Bi fields, and in particular it has new monopole
operators charged under a topological Uð1ÞT 0 global
symmetry generated by the dual of the field strength of
Bi . We can then take the k0 → ∞ limit, which on R3
removes all dynamical effects of the gauging, including the
existence of monopoles charged under the Uð1ÞT 0 , and we
obtain precisely the desired restriction to UðNÞ singlets.
From the UðNÞ-singlet sector of the free theory, we can
then get the theory we are interested in (the SUðNÞ-singlet
sector of scalar QED at level k) by adding S e→∞ , S k , and
S λ→∞ as discussed before. For k ≠ 0, monopole operators
(charged under Uð1ÞT ) carry k units of the gauge Uð1Þ
charge, and so to be gauge-invariant under the A gauging,
monopoles need to be dressed by composites of ϕI that will
cancel their Uð1Þ charge. But then the dressed monopoles
would also be charged under the original B gauging due to
the dressing. Thus, our theory includes no gauge-invariant
monopoles for k ≠ 0. For k ¼ 0, the monopole operators of
QED are uncharged under Uð1Þ, so they are allowed.
Similarly for d ≠ 3 where we have no Chern-Simons terms,
the codimension-3 monopole operators discussed above are
also allowed.

Since both S free ½G and the Jacobian include terms proportional to N, we can perform a 1=N saddle point expansion
by taking the large N limit first, where all physical
observables should be independent of the regularization
parameter V. In particular, we expand G around its large N
saddle point values given by the propagator G0 ðx1 ; x2 Þ in
(2.6) as
1
Gðx1 ; x2 Þ ¼ G0 ðx1 ; x2 Þ þ pﬃﬃﬃﬃ ηðx1 ; x2 Þ:
N

The free bilocal action (2.17) in terms of the fluctuation η
now gives (up to additive constants)
S free ½η ¼

S Jac ¼ −ðN − VÞTrðlogðGÞÞ;

ð2:17Þ

where we regularized the path integral by placing our field
theory on a lattice of V points, such that Gðx1 ; x2 Þ is a
Hermitian V × V matrix, and S Jac is the nontrivial Jacobian
(we drop all factors that do not depend on G). Note that
(2.17) is only correct for N ≥ V, which applies to the large
N expansion we consider in this paper, while for N < V
Gðx1 ; x2 Þ must obey complicated nonlinear constraints.
The continuum limit is reached by taking V → ∞,
in which case matrix
R d traces become continuum
integrals
as
TrðGÞ
≡
d xGðx; xÞ and ðGHÞðx1 ; x2 Þ≡
R d
d x3 Gðx1 ; x3 ÞHðx3 ; x2 Þ. In particular, the continuum
S free ½G may be written as
Z
S free ½G ¼ N dd x1 ∂ 1;i ∂ 2;i Gðx1 ; x2 Þjx2 ¼x1 :
ð2:18Þ

pﬃﬃﬃﬃ
N TrðG−1
0 ηÞ;

ð2:20Þ

and


1 −1
S Jac ½η ¼ −ðN − VÞ log 1 þ pﬃﬃﬃﬃ G0 η
N
∞
nþ1
X
ð−1Þ
n
n
¼−
N 1−2 TrððG−1
0 ηÞ Þ
n
n¼1

C. The bilocal formalism
We will now show how the singlet sector discussed
above can be usefully described in terms of bilocal
variables, which can then be naturally translated into the
bulk in the later sections. We start by reviewing the bilocal
formalism for the free theory with action S free in (2.1)
following [8,10,15,36]. All UðNÞ invariants of N free
scalars can be written in terms of the bilocal field (1.1).
We can then change variables in the path integral from ϕI to
G to get the partition function
Z
Z ¼ DGðx1 ; x2 Þ expð−S free ½G − S Jac ½GÞ;

ð2:19Þ

−V

∞
X
ð−1Þn
n¼1

n

n
N −2 TrððG−1
0 ηÞ Þ;
n

ð2:21Þ

where we expanded in large N. Note that the first n ¼ 1
term cancels the linear S free ½η as we expect from a saddle
point solution. We can then write down Feynman rules
where the propagator is given by the n ¼ 2 bare term in
(2.21), and we have bare n-point vertices for n ≥ 3, as well
as counterterm (multiplied by V) n-point vertices for n ≥ 1.
As shown in [8], these Feynman rules lead to the expected
correlation functions for the free theory.
We can extend the bilocal formalism to QED by simply
writing all ϕ-dependent terms in the actions we wrote above
using G as



1 2
2
S e ½G;A ¼ d x
F ðxÞþJi ½GAi ðxÞþAi ðxÞGðx;xÞ ;
4e2 ij
pﬃﬃﬃﬃ


Z
1 2
N
d
σðxÞGðx;xÞ ;
ð2:22Þ
S λ ½G;σ ¼ d x − σ ðxÞþ
4λ
2
Z

d

where we
pﬃﬃﬃﬃwrite the Uð1Þ current in terms of G as
Ji ½G ≡ i N ð∂ 2;i − ∂ 1;i ÞGðx1 ; x2 Þjx2 ¼x1 . Note that S Jac ½G
is gauge-invariant by itself, and then gauge-invariance of
the other terms works exactly the same as in the ϕ
language. We would like to now expand G around G0 in
(2.6) (which is not gauge-invariant, but is still a saddle point
in the gauge-fixing that we perform as described above)
to get

126011-6

## PDF page 7

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)


1 2
A2i ðxÞηðx; xÞ
2
pﬃﬃﬃﬃ
þ Ai ðxÞG0 ðx; xÞ ;
S e ½η; A ¼
F ðxÞ þ Ji ½ηAi ðxÞ þ J i ½G0 Ai ðxÞ þ
4e2 ij
N
pﬃﬃﬃﬃ


Z
1 2
1
N
d
σðxÞG0 ðx; xÞ ;
S λ ½η; σ ¼ d x − σ ðxÞ þ σðxÞηðx; xÞ þ
4λ
2
2
Z



dd x

ð2:23Þ

where Ji ½η ≡ ið∂ 2;i − ∂ 1;i Þηðx1 ; x2 Þjx2 ¼x1 . This includes divergent terms involving G0 ðx; xÞ and its derivatives, which are
not regularized by the lattice regulator used so far. For Sλ, we can cancel σðxÞG0 ðx; xÞ at each order with a linear term in σ
(or, equivalently, with a mass counterterm). For Se, we expect that J i ½G0  ¼ 0 in any Lorentz-invariant regularization.4 In
the following, we will simply drop the divergent terms that can be canceled in these ways, and thus define

1 2
A2i ðxÞηðx; xÞ
2
pﬃﬃﬃﬃ
þ Ai ðxÞG0 ðx; xÞ ;
S e ½η; A ≡
F ðxÞ þ Ji ½ηAi ðxÞ þ
4e2 ij
N


Z
1
1
S λ ½η; σ ≡ dd x − σ 2 ðxÞ þ σðxÞηðx; xÞ :
4λ
2
Z



dd x

Note that we have kept the counterterm A2i ðxÞG0 ðx; xÞ in
the action, because it is needed to cancel the divergence in
the contribution of Ji ½ηAi to the photon self-energy. In
particular, A2i ðxÞG0 ðx; xÞ contributes the first divergent
term in (2.12), while Ji ½ηA contributes the second term.
A2 ðxÞηðx;xÞ
The i pﬃﬃﬃ term does not contribute at leading order in

our gauge-fixed action, but generally these are not meaningful, because we are averaging over different gauge
choices in which Gðx1 ; x2 Þ corresponds to different
operators.5
III. THE AdS/CFT MAP

N

1=N, but will contribute at subleading orders. In fact, for
the CPN−1 model (2.4) we can make the field redefinition
2A2 ðxÞ
(after gauge-fixing) σðxÞ ↦ σðxÞ − pi ﬃﬃﬃ which cancels

N
A2i ðxÞηðx;xÞ
pﬃﬃﬃ
entirely
(for
λ
→
∞).
In
this
way the Feynman
N

diagrams of the theory can be packed in terms of the
effective σ and A propagators in (2.9) and (2.13), respectively.
Our action is written in a specific gauge choice discussed
above, using the nongauge-invariant bilocal variable
ηðx1 ; x2 Þ. In order to construct gauge-invariant variables,
we need to look at the limit x2 → x1 of ηðx1 ; x2 Þ to
obtain gauge-invariant local operators, or alternatively to
dress Gðx1 ; x2 Þ with a Wilson line between x1 and x2 . We
can also compute correlation functions of ηðx1 ; x2 Þ’s using
4

A gauge-invariant way of cancelling this term is to couple N
new scalars ϕ̃I to Ai with opposite charge as ϕI and large mass m.
We can then express ϕ̃I in terms of bilocals G̃ in the usual way
except the saddle point is now given by the massive free
propagator
G̃0 ðx; 0Þ ¼

Γðd=2 − 1Þ e−mjxj
;
4π d=2 jxjd−2

ð2:25Þ

In this section, we discuss the exact AdS=CFT map that
we will use in the next section to write down the bulk dual of
the SUðNÞ-singlet sector of scalar QED. We start by
reviewing the off-shell AdS=CFT map derived in [8],
which naturally acts on the CFT bilocal ηðx1 ; x2 Þ. We will
then show how this map implies that local single-trace
operators of any spin J in any dimension d also map off-shell
to the bulk in a simple way, generalizing the d < 4 and J ¼ 0
case proven in [8]. For J ¼ 1, this off-shell map will
then be used to write the bulk dual of scalar QED in the
next section.
A. Review of the bilocal map
We begin by briefly reviewing the AdS=CFT map of the
free scalar theory [8]. The map is given by expanding the
bilocal fluctuation ηðx1 ; x2 Þ on one side, and the spin J
transverse traceless AdS fields ΦJ ðx; zÞ on the other side, in
terms of the same irreducible representations (labeled by Δ,
J, y) of the conformal group, so that the exact map between
ηðx1 ; x2 Þ to ΦJ ðx; zÞ is given by the convolution of the basis
elements in each space.6

ð2:24Þ

and the J i Ai terms in the G̃ version of (2.23) come with opposite
sign. If we now take the limit m → ∞, then we see
that G̃0 ðx1 ; x2 Þ → 0 except where x1 → x2 such that G̃0 → G0 ,
so the only effect of these new scalars is to cancel the J i ½G0 Ai
term.

In the special case ζ ¼ 1 where we just have Landau gauge,
these correlation functions are meaningful, but they correspond to
some complicated nonlocal gauge-invariant operators.
6
For later convenience, we will not use the embedding space
formalism used in [8].

126011-7

5

## PDF page 8

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)
For d > 4,9 we can use the orthogonality and completeness relations of the 3-point basis, as reviewed in
Appendix A 1, to invert (3.1) and write CΔ;J ðyÞ in terms
of ηðx1 ; x2 Þ as
1 1
2 N Δ;J

d > 4∶ CΔ;J ðyÞ ¼

Z
dd x1 dd x2 ηðx1 ; x2 Þ

× hOΔ̃0 ðx1 ÞÔΔ̃0 ðx2 ÞOΔ̃;J ðyÞi;
FIG. 3. The deformation of the contour γ 0 from the principal
series ReðΔÞ ¼ d2 to include Δ ¼ 2Δ0 and exclude d − 2Δ0 , when
2Δ0 < d=2. In general we should deform the contour γ J for any
2Δ0 þ 2n þ J < d2 and n ¼ 0; 1; ….

We expand ηðx1 ; x2 Þ in the complete basis
Z
∞ Z
X
dΔ
dd yCΔ;J ðyÞhOΔ0 ðx1 Þ
ηðx1 ; x2 Þ ¼
2πi
γ
J
J¼0
× ÔΔ0 ðx2 ÞOΔ;J ðyÞi;

where Zi ≡

−

, we define x12 ≡ jx1 − x2 j, and we will

in general suppress spin indices for simplicity. The contours γ J of the Δ integrals in (3.1) go over the principal
series Δ ¼ d2 þ is for real s, except for J ¼ 0 and d < 4
where we deform the contour as shown in Fig. 3 to ensure
that the pole 2Δ0 ¼ d − 2 of the scalar single-trace operator
in the free theory appears on the same side of the contour as
the other spin J single-trace operators with scaling dimension d − 2 þ J. This expansion exists when ηðx1 ; x2 Þ
satisfies the conditions
(1) limx2 →x1 ηðx1 ; x2 Þ should be finite.
(2) At large jx1 þ x2 j (and fixed difference) ηðx1 ; x2 Þ
should decay.8
(3) At large jx1 j (or jx2 j) and fixed x2 (x1 )
ηðx1 ; x2 Þ ∼ jx1 j−2Δ0 · Power series in

ðΔ̃;JÞ
SΔ0 ;Δ0

dd y0 hOΔ;J ðyÞOΔ;J ðy0 ÞiCΔ;J ðy0 Þ; ð3:5Þ

1
:
jx1 j

ðΔ̃;JÞ

where the shadow coefficient SΔ0 ;Δ0 is given in (A4), and
the “2-point function” is defined as
0
0
I i1 i1 ðx12 Þ    I iJ iJ ðx12 Þ
i01 …i0J
i1 …iJ
hOΔ;J ðx1 ÞOΔ;J ðx2 Þi ¼
− traces;
x2Δ
12

ð3:6Þ
0

i i0

0

where I ii ≡ δii − 2 xjxjx2 . Hermiticity of ηðx1 ; x2 Þ then

implies that CΔ;J ðyÞ ¼ ð−1ÞJ CΔ̃;J ðyÞ.
For d < 4, the integral in (3.4) does not converge.
As explained in [8], we can avoid this divergence by
considering the auxiliary bilocal

η̃ðx1 ; x2 Þ ¼

 d−2 2
Γð 2 Þ
4π 2

d

∇21 ∇22 ηðx1 ; x2 Þ;

η̃ðx1 ; x2 Þ ¼

ð3:3Þ

∞
XZ
J¼0

dΔ
2πi
P:S:

Z
dd yC̃Δ;J ðyÞ

× hOΔ̃0 ðx1 ÞÔΔ̃0 ðx2 ÞOΔ;J ðyÞi;

Note that while the harmonic basis resembles a three point
function, it does not correspond to a correlator in a physical CFT,
and is simply a useful basis for conformally-covariant functions.
8
In [8], a related map was also derived for ηðx1 ; x2 Þ that do not
satisfy this condition.

ð3:7Þ

which can be expanded in the harmonic basis as

(4) ηðx1 ; x2 Þ must be smooth.
7

Z

1

ð3:1Þ

Zi1 …ZiJ − traces
1 ;…;iJ
hOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOiΔ;J
ðx3 Þi ¼ 2Δ0 −ΔþJ Δ−J Δ−J ; ð3:2Þ
x12
x13 x23
xi23
x223

where the normalization N Δ;J is given in (A2), and tildes
over dimensions denote Δ̃ ¼ d − Δ. The shadow relation
(A5) implies that only half of the coefficients CΔ;J ðyÞ are
independent along the contour γ J. We define the physical
CΔ;J ðyÞ to have ImðΔÞ ≥ 0, and then the shadow CΔ̃;J ðyÞ
are related to them by
CΔ̃;J ðyÞ ¼

where the basis elements are “3-point functions”7 of scalar
operators OΔ0 and ÔΔ0 that have the same scaling dimension Δ0 ¼ d−2
2 as a free scalar field, namely

xi13
x213

ð3:4Þ

ð3:8Þ

where the contour is now the principal series for all J, and
We expect that d ¼ 4 should be an analytic continuation of
our results for d > 4, as is generally the case in harmonic analysis
[45], but we will not discuss this case in detail.

126011-8

9

## PDF page 9

AdS FROM CFT FOR SCALAR QED
d < 4∶ C̃Δ;J ðyÞ ¼

1 1
2 N Δ;J

PHYS. REV. D 104, 126011 (2021)

Z

the boundary Rd,11 and we define the bulk shadow
coefficient

dd x1 dd x2 η̃ðx1 ; x2 Þ

× hOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ̃;J ðyÞi

ð3:9Þ

is now convergent for d < 4, unlike (3.4). The original
expansion of ηðx1 ; x2 Þ in (3.1) still holds for d < 4
provided that we identify
d < 4∶ CΔ;J ðyÞ ≡

16π d Γ2 ðd2 − Δ0 Þ
C̃Δ;J ðyÞ;
Γ2 ðΔ0 ÞλΔ;J

ð3:10Þ

where λΔ;J is the eigenvalue of the bilocal Laplacian in the
conformal basis and is given for any d by
λΔ;J ¼ ðM 2Δ;J − M 2dþJ;J ÞðM2Δ;J − M2dþJ−2;J Þ;
M 2Δ;J ≡ ΔðΔ − dÞ − J:

ð3:11Þ

In AdS space we use Poincaré coordinates
(ds2 ¼ ðdxi dxi þ dz2 Þ=z2 ), and in our formalism the metric in the bulk is fixed, with traceless transverse spin J fields
ΦJ ðx; zÞ (including a spin-two graviton) propagating on
this fixed background. We define the mapping from the
CFT to the bulk by expanding the bulk fields ΦJ ðx; zÞ in the
complete basis
Z
ΦJ ðx; zÞ ¼

dΔ
γ J 2πi

1 iJ
for a ¼ 1; …; J∶ ∇μa GiΔ;J
ðx; zjyÞμ1 μa μJ ¼ 0;

∇μ ≡ zdþ3 ∂ μ z−d−1 ;

∇2x;z ≡ zdþ1 ∂ z ðz−dþ1 ∂ z Þ þ z2 ∇2x ;

ð3:13Þ

ΓðΔ þ JÞΓ2 ðΔ̃þJ
f Δ;J
SΔ̃;J
B
2 Þ
;
¼ ðΔ̃;JÞ
¼
2 ΔþJ
f Δ̃;J S
ΓðΔ̃ þ JÞΓ ð 2 Þ

where the bulk shadow coefficient is given in (3.15). The
expansion (3.12) assumes that ΦJ ðx; zÞ decays in the small
d
z limit as z2−J in general. For J ¼ 0 and d < 4 recall that
the contour γ 0 allows the integrand to have an extra
contribution at Δ ¼ d − 2, in which case Φ0 ðx; zÞ could
decay as zd−2 . Finally, ΦJ ðx; zÞ should decay at large x,
which corresponds to ηðx1 ; x2 Þ decaying at large
jx1 þ x2 j.12
For J > 0 or d > 4, we can use the orthogonality and
completeness of the propagators to write CΔ;J ðyÞ in terms
of ΦJ ðx; zÞ as
d > 4∶ CΔ;J ðyÞ
Z d
1
d xdz
ΦJ ðx; zjyÞGΔ̃;J ðx; zjyÞ; ð3:18Þ
¼
αJ f Δ;J N Δ;J
zdþ1

GΔ;J ðx; zjyÞ ¼ zΔ−J hOΔ;J ðxÞOΔ;J ðyÞi
ð3:14Þ

where δTT
J ðxÞ denotes a delta function with 2J suppressed
lower indices for spin J traceless transverse functions on
When Δ ¼ Δ̃, as can happen for the scalar bulk field in
d ¼ 4, the second term will have a logðzÞ, which distinguishes its
scaling in z from the first term.
10

ð3:17Þ

Δ0 ;Δ0

J > 0 or

and by the z → 0 boundary condition10

TT
þ zd−Δ−J SΔ;J
B δJ ðx − yÞ þ    ;

ð3:16Þ

where μ ¼ z; 1; …; d denotes bulk spin indices that we in
general suppress for simplicity (we denote the index in the
radial direction by z, this should not be confused with the
value of the radial coordinate that we also denote by z).
See Appendix A 2 for an explicit expression for GΔ;J , as
well as the orthogonality, completeness, and shadow
relations.
The CFT shadow relation (A5) and the bulk shadow
relations (A7) imply that f Δ;J must satisfy the consistency
condition

dd yfΔ;J CΔ;J ðyÞGΔ;J ðx; zjyÞ; ð3:12Þ

ð∇2x;z − M 2Δ;J ÞGΔ;J ðx; zjyÞ ¼ 0;

ð3:15Þ

The solution to (3.13) and (3.14) is by construction transverse

Z

where we identified the bulk coefficient CΔ;J ðyÞ with the
same coefficient appearing in the bilocal expansion, up to a
multiplicative factor f Δ;J that is not fixed by conformal
symmetry. This identification implies that the contour γ J in
(3.12) is the same as the one in the bilocal expansion.
The basis elements in (3.12) are the bulk-to-boundary
propagators in AdS space, defined by the differential
equation

π 2 ΓðΔ − d2Þ
:
ðJ þ Δ − 1ÞΓðΔ − 1Þ
d

SΔ;J
B ≡

where the normalization αJ is given in (A9). This integral is
not convergent for J ¼ 0 and d < 4, but as shown in [8] it
can be replaced by the modified relation
11
For instance, when J ¼ 1 we can define δTT
1;ij ðxÞ≡
R dd p ipx
pi pj
e
ðδ
−
Þ.
ij
jpj2
ð2πÞd

126011-9

A map for nondecaying Φ0 was also derived in [8].

12

## PDF page 10

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

J ¼ 0 and d < 4∶ CΔ;0 ðyÞ
Z d
d xdz GΔ̃;0 ðx; zjyÞ
¼
zdþ1 λΔ;0 α0 f Δ;0 N Δ;0

where the AdS Laplacian is defined in (3.13).
The CFT-to-AdS map now simply follows from a
convolutionof the bulk and CFT bases, and it takes the
explicit form

× ð∇2x;z − M 2d−2;0 Þð∇2x;z − M2d;0 ÞΦ0 ðx; zÞ;

ð3:19Þ

Z
Z
Z
1
dΔ f Δ;J
d
d > 4∶ ΦJ ðx; zÞ ¼
d y dd x1 dd x2 GΔ;J ðx; zjyÞhOΔ̃0 ðx1 ÞÔΔ̃0 ðx2 ÞOΔ̃;J ðyÞiηðx1 ; x2 Þ;
2 P:S: 2πi N Δ;J
Z
Z
Z
f Δ;J
1
dΔ
d < 4∶ ΦJ ðx; zÞ ¼
dd y dd x1 dd x2
G ðx; zjyÞhOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ̃;J ðyÞi∇21 ∇22 ηðx1 ; x2 Þ;
2 γJ 2πi
λΔ;J N Δ;J Δ;J
where for d > 4 we plugged (3.4) into (3.12), while for
d < 4 we plugged (3.9) and (3.10) into (3.12). The AdS-toCFT map similarly comes from plugging (3.18) into (3.1),
and it takes the form
ηðx1 ; x2 Þ ¼

∞ Z
X
J¼0

dΔ
2πi
P:S:

Z

Z
d

d y

dd xdz GΔ̃;J ðx; zjyÞ
zdþ1 αJ N Δ;J f Δ;J

× hOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ;J ðyÞiΦJ ðx; zÞ;

dΔ
γ 0 2πi

Z

Z
dd y

× OΔ;0 ðyÞi

ε→0

dd xdz
hOΔ0 ðx1 ÞÔΔ0 ðx2 Þ
zdþ1

where ê is an arbitrary unit vector, and the bilocal differJ;ðx ;x Þ
ential operator Di1 …i1 J 2 can be found in [46] and is fixed
such that SJ ðxÞ is a conformal primary normalized with
two-point function
hSJi1 …iJ ðx1 ÞSJj1 …jJ ðx2 Þi


I j1 ði1 ðx12 Þ    I iJ ÞjJ ðx12 Þ
−
traces
;
¼ aJ
2ðd−2þJÞ
x12
I ij ≡ δij − 2

GΔ̃;0 ðx; zjyÞ
α0 N Δ;0 λΔ;0 f Δ;0

× ð∇2x;z − M 2d−2;0 Þð∇2x;z − M2d;0 ÞΦ0 ðx; zÞ;

ð3:23Þ

ð3:21Þ

where for d < 4 and J ¼ 0 we need to replace the J ¼ 0
term by
Z

J;ðx ;x Þ

SJi1 iJ ðx1 Þ ≡ limDi1 i1J 2 ηðx1 ; x2 Þjx2 ¼x1 þεê ;

ð3:20Þ

1

xi xj
;
x2

aJ ¼

π 2−d Γðd2 þ J − 1ÞΓðd þ J − 3Þ
:
2dþJ ΓðJ þ 1ÞΓðd−3
2 þ JÞ
ð3:24Þ

ð3:22Þ

For instance, for J ¼ 0, 1 we have

due to the modified expansion in (3.19).
D0;ðx1 ;x2 Þ ¼ 1;

B. Off-shell map of single-trace operators
We will now discuss how the off-shell bilocal map
reviewed above can be used to derive a simple off-shell map
for singlet local operators in the CFT. We start by reviewing
the derivation of the map for J ¼ 0 and d < 4 that was
shown in [8], and then discuss how to generalize this to
general J and d > 2.
Spin J single-trace singlet local operators SJi1 iJ ðxÞ in the
free theory are defined in terms of the bilocal as

1;ðx1 ;x2 Þ

Di

1
¼ pﬃﬃﬃﬃﬃﬃﬃﬃﬃ ð∂ i;x2 − ∂ i;x1 Þ;
2 d−2

ð3:25Þ
2

such that for J ¼ 0 we recover the coefficient a0 ¼ Γðd=2−1Þ
16π d
in the scalar 2-point function computed from (2.6), while
i
for J ¼ 1 we identify S1i ðxÞ ¼ − 2pﬃﬃﬃﬃﬃﬃ
J ½η with Ji ½η
d−2 i
defined below (2.23).
As shown in [8], we can use the expansions (3.1) and
(3.12) to show that

Z
SJi1 …iJ ðx1 Þ ¼ lim
ε→0

Z

ΦJ;i1 …iJ ðx1 ; εÞ ¼ 2


Z
ðΔ̃;JÞ Δ̃;J
∞ Z
ðê-dependentÞi1 …iJ ;ji …jJ0
dΔ 2SΔ0 ;Δ0 Ci1 …iJ ðx1 Þ X
dΔ
Δ;J0
d
;
þ
yC
ðyÞ
d
0
j1 …jJ0
2πi
ε2Δ0 þJ−Δ
ε2Δ0 þJ −Δ
γ J 2πi
J0 ¼0 γ J0

dΔ
ðΔ̃;JÞ
f Δ;J εΔ−J ½SΔ0 ;Δ0 CΔ̃;J
i1 ;…iJ ðx1 Þ þ OðεÞ:
2πi
γJ

126011-10

ð3:26Þ

## PDF page 11

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)

In general, it is difficult to perform the Δ integrals in (3.26),
since we know very little about general CΔ;J . For instance,
the contour γ J0 for d > 4 or for J 0 > 0 and d ≤ 4 is the
principal series ReðΔÞ ¼ d=2, so along this contour the
0
leading term ε2−d=2−J diverges for the free theory. To get
the finite answer for SJi1 …iJ ðx1 Þ that we expect, there must
be complicated cancellations. For d < 4 and J0 ¼ 0, however, recall that the contour γ 0 includes a deformation from
the principal series to include the pole Δ ¼ d − 2 < d=2.
Since the principal series contribution goes to zero as ε2−d=2
in this case, we know even off-shell that the only contribution as ε → 0 to the integrals in (3.26) comes from the
Δ ¼ d − 2 pole, which is the only pole on the other side of
the principal series. This yields the off-shell relation
S0 ðxÞ ≡ ηðx; xÞ ¼

1

limε2−d Φ0 ðx; εÞ;
f d−2;0 ε→0

ð3:27Þ

which in particular continues to hold under deformations of
the theory.
We can generalize this relation to general d > 2 and J
using a different argument. Consider deforming the bilocal
CFT action by SJ coupled to a source AJ as
Z
S AJ ¼ dd xAJii …iJ SJi1 …iJ :
ð3:28Þ
We can compute the VEV of ηðx1 ; x2 Þ under this deformation (in the large N limit) as
Z
J;ðx ;x Þ
hηðx1 ; x2 ÞiAJ ¼ dd yAJii …iJ ðyÞDi1 i1J 2 G0 ðx1 ; yÞG0 ðy; x2 Þ
Z
¼ aJ dd yAJii …iJ ðyÞhOΔ0 ðx1 ÞÔΔ0 ðx2 Þ
1 ;…;iJ
ðyÞi;
× Oid−2þJ;J

ð3:29Þ

where the second equality follows from the definitions
(2.6), (3.2), and (3.23). As x2 → x1 , this VEV diverges as
ðd−2þJ;JÞ
SΔ0 ;Δ0 AJ ðx1 Þ=xd−4þ2J
. At leading N → ∞, this implies
12
the off-shell singularity
limε

4−d−2J

ε→0

ηðx1 ; x2 Þjx2 ¼x1 þεê

ðd−2þJ;JÞ

¼ SΔ0 ;Δ0

aJ AJii …iJ ðx1 Þêi1 …êiJ ;

ð3:30Þ

which is singular for all d > 2 and J except J ¼ 0 for
d < 4. In the original path integral in terms of the local field
ϕI ðxÞ, each ϕI ðxÞ does not couple to the others, which
implies that the off-shell behavior of ϕI ðxÞ, and thus
ηðx1 ; x2 Þ, is independent of N, so (3.30) in fact holds for
finite N. Recall that the conditions (3.3) to expand ηðx1 ; x2 Þ
in terms of CΔ;J ðyÞ require that ηðx1 ; x2 Þ be finite as
x2 → x1 , so we must modify our AdS=CFT map in the
presence of this source for all d > 2 and J except J ¼ 0

for d < 4. We can cancel the divergence (3.30) by
modifying the contour γ J in (3.1) to include a piece around
Δ ¼ d − 2 þ J with
Cd−2þJ;J ðyÞjAJ ¼ aJ AJ ðyÞ;

ð3:31Þ

which will cancel the divergent VEV in (3.29). In the bulk,
this modification of γ J will give the VEV
Z
hΦJ ðx; zÞijAJ ¼ aJ f d−2þJ;J dd yAJ ðyÞGd−2þJ;J ðx; zjyÞ;
ð3:32Þ
which follows from modifying the contour in (3.12), and is
also what we would get by naively mapping (3.29) using
the unmodified map (3.20) and the CFT orthogonality
relation (A3). We can then take z → 0 to find the modified
off-shell bulk boundary condition
AJ ðxÞ;
limε2J−2 ΦJ ðx; εÞ ¼ aJ f d−2þJ;J Sd−2þJ;J
B
ε→0

ð3:33Þ

which follows from (3.14). We could equivalently use the
standard bulk boundary conditions and instead add to the
bulk action the source term
Z
S bulk
AJ ¼

dd xdz J
1
Aii …iJ ðxÞ
limε2−d ΦJ ðx;εÞ: ð3:34Þ
dþ1
f d−2þJ;J ε→0
z

Now, comparing (3.34) to (3.28) for general AJ ðxÞ implies
the off-shell relation
SJ ðxÞ ¼

1

limε2−d ΦJ ðx; εÞ;
f d−2þJ;J ε→0

ð3:35Þ

which for J ¼ 0 for d < 4 was what we previously showed
in (3.27), and for all other d > 2 and J follows from the
modified boundary condition argument. This off-shell map
generalizes the on-shell relation previously shown for
general d > 2 and J in [8].
IV. THE BULK DUAL OF SCALAR QED
We will now use the AdS=CFT map of the previous
section to write the action for the bulk dual of scalar QED.
We will first review the bulk action for the free and critical
UðNÞ theories, which were derived in [8]. We will then use
the off-shell map of single-trace local operators for J ¼ 0, 1
to show that the bulk QED action is given by a simple
deformation of the bulk dual of the free theory. Finally, we
will compute correlation functions in the bulk and show
that the bulk duals of the free theory and QED only differ
by the boundary conditions of the bulk J ¼ 0, 1 two-point
function, as anticipated in [20–24], where the J ¼ 1
two-point function is sensitive to the gauge-fixing in
the CFT.

126011-11

## PDF page 12

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)
Z

A. The bulk action
We start by reviewing the bulk action for the free theory,
which in the bilocal language had an infinite number of
terms given by (2.20) and (2.21). The bilocal AdS=CFT
map translates each of these terms to the bulk, where for
general f Δ;J they take a complicated nonlocal form given
explicitly in [8]. For the special choice
1

Δ̃;J 2
local
J SB
;
f Δ;J ¼ ð−1Þ Δ̃;J
SΔ0 ;Δ0

ð4:1Þ

local
J
such that f local
Δ;J f Δ̃;J ¼ ð−1Þ , the quadratic term in the bulk
action can be written in the simple local way:
ð2Þ

S free ½ΦJ  ¼

Z d
∞
X
1
d xdz
α
J¼0 J

zdþ1

ΦJ ðx; zÞð∇2x;z − M2dþJ−2;J Þ

× ð∇2x;z − M 2dþJ;J ÞΦJ ðx; zÞ;

ð4:2Þ

where for d < 4 the modified map (3.22) gives a slightly
different form for the J ¼ 0 term as shown in [8]. The
higher order terms S ðnÞ ½ΦJ  in the bulk action remain
nonlocal even for f local
Δ;J , and include explicit bulk counterterms starting with S ð1Þ ½ΦJ  that are dual to the Vdependent counterterms in (2.21).
The various deformations to the free theory discussed in
Sec. II C can then be mapped to the bulk using the off-shell
map of local operators in (3.35). For instance, the scalar
double-trace deformation in (2.25) maps to
Z
S e ½Φ0 ; Φ1 ; A ¼

∞
X


1
1
2−d
þ σðxÞ
limε Φ0 ðx; εÞ ;
2
f d−2;0 ε→0

ð4:3Þ

where σðxÞ can be thought of as living on the boundary of
AdS. When λ → 0, this defines the bulk dual of the critical
UðNÞ theory for any d > 2 such that this CFT exists, which
was argued to be (for large enough N) 2 < d < 6 in [33].13
The σðxÞ field then acts as a Lagrange multiplier in (4.3)
that sets limε→0 ε2−d Φ0 ðx; εÞ ¼ 0 off-shell, just as in the
CFT it set ηðx; xÞ ¼ 0 off-shell. Thus, the off-shell relation
(3.27) becomes trivial in the critical theory. The vanishing
of the zd−2 mode implies that Φ0 ðx; zÞ now has the same
small z boundary condition as all other J > 0 bulk fields,
namely it scales as zd=2 , which is the real part of the
principal series contour. For 2 < d < 4 this was already
discussed in [8], and here we can generalize this to d > 4
because we generalized the off-shell map for J ¼ 0
to d > 4.
For QED, we first gauge-fix the CFT by adding the term
S ζ ½A given in (2.10), where the family of possible gaugefixings is parametrized by ζ ∈ R. Since this term, as well as
the Chern-Simons term S k ½A given in (2.5) for d ¼ 3, do
not depend on η, they map trivially to the bulk such that
Ai ðxÞ now lives on the boundary of AdS, just like σ. We
then use the off-shell map (3.35) for J ¼ 0, 1 to map
S e ½η; A to the bulk to get

 pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ

1 2
A2i ðxÞΦ0 ðx; εÞ
i
2
2−d 2i d − 2
;
d x
F ðxÞ þ Ai ðxÞG0 ðx; xÞ þ lim ε
Ai ðxÞΦ1 ðx; εÞ þ pﬃﬃﬃﬃ
ε→0
f d−1;1
4e2 ij
N f d−2;0


d

iﬃﬃﬃﬃﬃﬃ
where we identified S1i ðxÞ ¼ − 2pd−2
Ji ½η, and recall that
2
the counterterm Ai ðxÞG0 ðx; xÞ is necessary to cancel
divergences in the Ai two-point function. We can then
take the limit e → ∞ to get the bulk dual scalar QED (2.4)
with bulk action:

S CPN−1 ½ΦJ ;A;σ ≡

S λ ½Φ0 ; σ ¼


1
d x − σ 2 ðxÞ
4λ
d

in the CFT it set to zero the Uð1Þ current. The z0 mode of
Φ1 then becomes dynamical, according to the off-shell
relation:
pﬃﬃﬃﬃﬃﬃﬃﬃﬃ
QEDwith k ¼ 0∶ Φi1 ðx;0Þ ¼ i2 d − 2a1 f d−1;1 Sd−1;1
Ai ðxÞ;
B
ð4:6Þ

ðnÞ

S free ½ΦJ  þ S e→∞ ½Φ0 ;Φ1 ;A þ S λ→∞

n¼1

ð4:5Þ
as well as the Chern-Simons term S k ½A for d ¼ 3 (if
desired).
Similar to the σ, Φ0 case, we can think of Ai ðxÞ
as a Lagrange multiplier that for k ¼ 0 sets
limε→0 ε2−d Φ1 ðx; εÞ ¼ 0 as an operator equation, just as

ð4:4Þ

iﬃﬃﬃﬃﬃﬃ
which is just (3.33) with J ¼ 1 and S1i ðxÞ ¼ − 2pd−2
Ji ½η.
Namely, in the bulk dual to QED, Ai ðxÞ is nothing but
the boundary value of the bulk vector field. It is convenient to write this change of boundary condition
by defining a boundary field strength for Φ1 (even
though in our formalism there is no gauge freedom for
this field) as

F μν ðxÞ ≡ limð∂ μ Φ1;ν ðx; zÞ − ∂ ν Φ1;μ ðx; zÞÞ:

The CFT is believed to be unitary only for 2 < d < 4.

13

z→0

126011-12

ð4:7Þ

## PDF page 13

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)

The boundary conditions for the free scalar theory and for QED for general d, as well as for d ¼ 3 and general k, can then be
written compactly as
free∶ F ij ðxÞ ¼ 0;
QEDd with k ¼ 0∶ F zi ðxÞ ¼ 0;
QED3 ∶ F ij ðxÞ þ

2πi
ε F ðxÞ ¼ 0;
16κ ijl zl

ð4:8Þ

where the free theory corresponds to electric boundary conditions, QED with k ¼ 0 corresponds to magnetic boundary
conditions, and QED3 for general k corresponds to mixed boundary conditions. Finally, the A2i ðxÞ term in (4.4) will also
alter the boundary behavior of Φ0 at subleading order in 1=N, according to (3.27).
B. The bulk correlation functions
We will now discuss the bulk correlation functions that follow from the bulk actions written above. For the dual of the free
theory with λ ¼ e ¼ 0, the bulk two-point functions coming from the local quadratic action (4.2) are [8]:
hΦJ ðx1 ; z1 ÞΦJ ðx2 ; z2 Þi ¼

αJ =2
ðΠTT
ðx1 ; z1 jx2 ; z2 Þ − ΠTT
dþJ;J ðx1 ; z1 jx2 ; z2 ÞÞ:
2
M dþJ;J − M 2dþJ−2;J d−2þJ;J

ð4:9Þ

Here, ΠTT
d−2þJ;J ðx1 ; z1 jx2 ; z2 Þ are the traceless transverse bulk-to-bulk propagators defined in [8] by the differential equation
TT
ð∇2x;z − M2Δ;J ÞΠTT
Δ;J ðx1 ; z1 jx2 ; z2 Þ ¼ −δ ðx1 ; z1 jx2 ; z2 Þ;

ð4:10Þ
and by the z2 → 0 boundary condition

ΠTT
Δ;J ðx1 ; z1 jx2 ; z2 Þ ¼

z2 Δ−J CΔ;J GΔ;J ðx1 ; z1 jx2 Þ þ OðzΔ−Jþ1
Þ Δ<d−Jþ4
2
Þ
Oðzd−2Jþ4
2

Δ ≥ d − J þ 4;

ð4:11Þ

where δTT is a delta function for traceless transverse functions that is defined precisely in [8], and the normalization is
CΔ;J ≡

ðJ þ Δ − 1ÞΓðΔ − 1Þ
2π 2 ΓðΔ þ 1 − d2Þ
d

ð4:12Þ

:

The solution to (4.10) and (4.11) is by construction traceless and transverse:
for a ¼ 1; …; J∶ ∇μa ΠTT
Δ;J ðx1 ; z1 jx2 ; z2 Þμ1 ;…;μa ;…;μJ jμ0 ;…;μ0J ¼ 0;
1

ΠTT
Δ;J ðx1 ; z1 jx2 ; z2 Þμ1 ;…;μa ;…;μJ jμ01 ;…;μa ;…;μ0J ¼ 0:

ð4:13Þ

The explicit propagators for Δ ≥ d − 2 þ J for J > 0, or J ¼ 0 and any Δ, were computed in [8], and are reviewed in
Appendix B 1. The massless propagators in the first term of (4.9) are identified with the physical particles dual to the
operators in our theory.14 For J > 0 they are dual to the infinite conserved currents in the CFT, and for J ¼ 0 to the
Δ ¼ d − 2 single-trace scalar. The particle with negative propagator and Δ ¼ d þ J − 2 is subleading in the z → 0 limit
(it happens to match the ghost spectrum of a certain gauge-fixing of Vasiliev’s theory [47–49], so we expect that probably
it can be interpreted as some kind of gauge-fixing-related ghost). The higher order correlation functions can be computed
using the Feynman rules for the higher order terms S ðnÞ ½η, which were shown in [8] to lead to the expected free theory
results, where all loops and counterterms cancel (this cancellation will no longer be exact in the nonfree theory we are
discussing here, but the divergences should cancel in the same way).
14

For massless propagators, the transversality constraint (4.13) can be interpreted as a bulk gauge choice in a putative bulk gauge
theory, which would be related to our bulk theory upon gauge-fixing.

126011-13

## PDF page 14

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

We can then consider the effect of the quadratic scalar deformation S λ ½Φ0 ; σ given in (4.3), which only modifies the
scalar propagator as [8]:


α0 Cd−2;0 =2 2
1
hΦ0 ðx1 ; z1 ÞΦ0 ðx2 ; z2 iλ ¼ hΦ0 ðx1 ; z1 ÞΦ0 ðx2 ; z2 Þiλ¼0 þ
2 M2 − M2
4ðf local
d;0
d−2;0
d−2 Þ
Z
× dd ydd y0 Gd−2;0 ðx1 ; z1 jyÞhσðyÞσðy0 Þiλ Gd−2;0 ðx2 ; z2 jy0 Þ þ OðN −1 Þ;
ð4:14Þ
where the σ propagator at finite λ is given in (2.8). For the critical theory at λ → ∞, the σ propagator in (2.9) becomes a
conformally invariant two-point function with scaling dimension Δ ¼ 2 þ Oð1=NÞ, so we can use the identity [50–52]


Z
d
d
d
0
0
0
TT
d yd y GΔ;0 ðx1 ;z1 jyÞhOΔ̃;0 ðyÞOΔ̃;0 ðy ÞiGΔ;0 ðx2 ;z2 jy Þ ¼ α0 N Δ;0 Δ − ðΠTT
Δ;0 ðx1 ;z1 ;x2 ;z2 Þ − ΠΔ̃;0 ðx1 ;z1 ;x2 ;z2 ÞÞ;
2
ð4:15Þ
with Δ ¼ d − 2 to compute
hΦ0 ðx1 ; z1 ÞΦ0 ðx2 ; z2 Þiλ→∞ ¼

α0 =2
−1
ðΠTT ðx1 ; z1 ; x2 ; z2 Þ − ΠTT
d;0 ðx1 ; z1 ; x2 ; z2 ÞÞ þ OðN Þ:
2
M d;0 − M2d−2;0 2;0

ð4:16Þ

We see that the physical propagator ΠTT
d−2;0 for Φ0 in the bulk dual of the free scalar theory has been replaced by the shadow
propagator ΠTT
,
which
generalizes
the
2 < d < 4 results of [8] to 2 < d < 6 (where the critical theory is defined at large N).
2;0
TT
Both ΠTT
and
Π
are
defined
by
the
same bulk differential equation (4.10), and differ only by the boundary condition
Δ;J
Δ̃;J
(4.11). Since the only difference between the free and critical bulk theories was this scalar propagator, we see that to all
orders in 1=N the only difference between the free and critical bulk theories is the boundary condition for the bulk scalar, as
TT
anticipated in [20,50,51]. As shown in [51], the modification of the free bulk Feynman rules by replacing ΠTT
d−2;0 → Π2;0
then leads to the expected bulk dual of the critical CFT for all bulk correlators, at all orders in 1=N.
Next, we consider the effect of coupling to the gauge field by adding S e ½Φ0 ; Φ1 ; A with the family of gauge-fixing terms
S ζ ½A (and for d ¼ 3 we can add also the Chern-Simons term S k ½A). The J ¼ 1 propagator is modified as

2
α1 Cd−1;1 =2
4ð2 − dÞ
hΦ1 ðx1 ; z1 ÞΦ1 ðx2 ; z2 Þiζ;e;k ¼ hΦ1 ðx1 ; z1 ÞΦ1 ðx2 ; z2 Þie¼0 þ local 2
ðf d−1;1 Þ M2dþ1;1 − M 2d−1;1
Z
× dd ydd y0 Gid−1;1 ðx1 ; z1 jyÞhAi ðyÞAj ðy0 Þiζ;e;k Gjd−1;1 ðx2 ; z2 jy0 Þ þ OðN −1 Þ;
ð4:17Þ
where we suppressed the bulk indices for simplicity, and where the gauge-fixed photon propagator is given in (2.13) for the
ζ family of gauges. Note that the bulk propagator now depends on the choice of gauge-fixing in the CFT. For the critical
theory at e → ∞, we can derive a generalization of the identity (4.15) to massless J ¼ 1 propagators15:
Z
dd ydd y0 Gd−1;1 ðx1 ; z1 jyÞijμ hAi ðyÞAi0 ðy0 Þiζ;e→∞;k Gd−1;1 ðx2 ; z2 jy0 Þi0 jμ0
3d

¼

8π 2
ðΠTT ðx1 ; z1 ; x2 ; z2 Þμjμ0 − Πζ;k
1;1 ðx1 ; z1 ; x2 ; z2 Þμjμ0 Þ:
d−2
Γð 2 ÞΓðdÞ d−1;1

ð4:18Þ

TT
Here, Πζ;k
1;1 is a traceless and transverse propagator that satisfies the same differential equation (4.9) as Πd−1;1 , but has the
alternate boundary condition

lim Πζ;k
1;1 ðx1 ;z1 ;x2 ;z2 Þ ¼

z2 →0

2 d
Γðd−2
2 ÞΓ ð2Þ

2π 2 ΓðdÞ
d

Gζ;k
1;1 ðx1 ;z1 jx2 Þ;

ð4:19Þ

where Gζ;k
1;1 ðx1 ; zjx2 Þ is a transverse bulk-to-boundary propagator that satisfies the same differential equation (3.13) as
Gd−1;1 ðx1 ; zjx2 Þ but has the alternate z → 0 boundary condition
15

A similar identity in axial gauge was derived in [23].

126011-14

## PDF page 15

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)


8
d
pi pj
π 2 ΓðdÞ R dd p ipx12
d−2
>
δij − jpj2 þ …; d ≠ 3;
e
>
< hAi ðx1 ÞAj ðx2 Þiζ;∞ − z
ð2πÞd
Γ3 ðd2Þ
ζ;k
G1;1 ðx1 ; zjx2 Þij ¼
ð4:20Þ
p p
pk
16ðδij − i 2j Þ−128κ
>
R
π εijk jpj
>
jpj
: hAi ðx1 ÞAj ðx2 Þiζ;∞;k − z d3 p3 eipx12
þ …;
d ¼ 3:
64κ2
ð2πÞ
π2

þ1

Note that we expressed δTT
1 ðx12 Þ explicitly in momentum space for d ≠ 3 for ease of comparison to d ¼ 3. Alternatively,
ζ;k
ζ;k
Π1;1 can be defined by their differential equation and the boundary condition (4.8). Explicit expressions for Πζ;k
1;1 and G1;1 are
derived in Appendix B 2, where we show that they satisfy (4.18). We can then apply (4.18) to the e → ∞ limit of (4.17) to
compute

hΦ1 ðx1 ; z1 ÞΦ1 ðx2 ; z2 Þiζ;e→∞;k ¼

α1 =2
−1
ðΠζ;k ðx1 ; z1 ; x2 ; z2 Þ − ΠTT
dþ1;1 ðx1 ; z1 ; x2 ; z2 ÞÞ þ OðN Þ:
M 2dþ1;1 − M 2d−1;1 1;1

ð4:21Þ

As in the scalar deformation, we see that the physical
propagator ΠTT
d−1;1 for Φ1 has been replaced by the shadow
propagator Πζ;k
1;1, except that now the shadow propagator
depends on the CFT gauge-fixing parameter ζ, and for
d ¼ 3 it can also have an infinite number of possible
boundary conditions, parametrized by k.
For the CPN−1 model, we saw above that we can change
variables for σðxÞ to get rid of the A2i ϕ2 term. In this way σ,
Ai couple in the bulk action (4.5) only linearly to Φ0 , Φ1
respectively. As we explained in this section, this means
that the CPN−1 bulk dual (at any order in 1=N) is the same
as the free theory bulk dual, only with the alternative
boundary conditions for both Φ0 and Φ1 . We can use this to
argue that our bulk action gives the expected correlators to
all orders in 1=N for the CPN−1 model, following the
analogous argument for the critical OðNÞ model in [51]. In
particular, already in the local description (2.4) we could
change variables for σ, which led to only linear couplings
for σ, Ai to the ϕI ’s. We can then consider the difference
between correlation functions of single-trace operators in
the CPN−1 model and in the free theory. At any order in
1=N, this difference can be written as integrals of the free
theory S0, S1i correlation functions with the effective
propagators for σ, Ai . Using (4.15) for S0 and (4.18) for
S1i , we can write the difference between the correlators as
the difference between the same Witten diagrams, only
with alternative boundary conditions for Φ0 and Φ1 .

the UðNÞ ⊂ UðNN c Þ subgroup can be translated to the
bulk just like the usual UðNÞ free scalar theory, except that
now both the UðNÞ singlet bilocals in the CFT and their
dual bulk fields are adjoints under UðN c Þ, and the terms in
the bulk action are all single traces of products of UðN c Þ
matrices. We can then construct the bulk dual of scalar
QCD by a procedure similar to the one described in the
previous sections: gauging UðN c Þ (in the CFT), fixing a
gauge convenient for the large N expansion, mapping the
UðN c Þ current (which is a UðNÞ singlet) to the bulk using
our usual CFT-to-AdS map, and coupling it to the new
UðN c Þ gauge fields. The main differences from the Abelian
case are that now the Yang-Mills and Chern-Simons terms
for UðN c Þ contain self-interactions of the UðN c Þ gauge
fields, and that the gauge-fixing now leads to ghosts (in the
adjoint of UðN c Þ) which will live on the boundary and
couple to the UðN c Þ gauge fields there.
As with QED, the resulting bulk theory is related
to the bulk dual of the free theory by a simple change
of boundary conditions for the spin one bulk field [in the
adjoint of UðN c Þ]. Note that this bulk construction is useful
for large N with fixed N c , and it does not apply to the
limit of large N c , k with fixed N, k=N c discussed
in [29,53], which is expected to have a different dual
description.

V. THE BULK DUAL OF UðN c Þ SCALAR QCD
AT FINITE N c

We would like to thank Tal Sheaffer and Tomer Solberg
for collaboration on related issues. This work was supported in part by an Israel Science Foundation center for
excellence grant (Grant No. 2289/18), by Grant
No. 2018068 from the United States-Israel Binational
Science Foundation (BSF), and by the Minerva foundation
with funding from the Federal German Ministry for
Education and Research. O. A. is the Samuel Sebba
Professorial Chair of Pure and Applied Physics. S. M. C.
is supported in part by a Zuckerman STEM leadership
fellowship.

The bulk dual of scalar QED in 2 < d < 4 with N ≫ 1
scalars that we described in the previous sections can be
easily generalized to UðN c Þ QCD in 2 < d < 4 with N ≫
1 scalars [28], for finite N c . For d ¼ 3 we can again
consider also the large Chern-Simons level k limit with
fixed κ ≡ k=N.
We start by considering a free theory of N × N c scalars
with global symmetry UðNN c Þ. The singlet sector under

ACKNOWLEDGMENTS

126011-15

## PDF page 16

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

APPENDIX A: CONFORMAL BASES
In this Appendix we review properties of the conformal bases that we use for the CFT and for the bulk fields. For the CFT
we follow [54,55], while for the bulk we follow [52].
1. Three-point function basis
The harmonic basis defined in (3.2) satisfies the completeness relation
X Z dΔ Z
1 ∞
1
dd y
hO ðx ÞÔ ðx ÞO ðyÞihOΔ̃0 ðx3 ÞÔΔ̃0 ðx4 ÞOΔ̃;J ðyÞi;
δðx13 Þδðx24 Þ ¼
2 J¼0 γJ 2πi
N Δ;J Δ0 1 Δ0 2 Δ;J

ðA1Þ

where the contour γ J was described in the main text, and the normalization factor is
3d

N Δ;J ¼

ΓðΔ − d2Þ
ΓðΔ̃ − d2Þ
π 2 ΓðJ þ 1Þ
:
2J−1 Γðd2 þ JÞ ΓðΔ − 1ÞðΔ þ J − 1Þ ΓðΔ̃ − 1ÞðΔ̃ þ J − 1Þ

ðA2Þ

The basis also satisfies the orthogonality relation
Z
dd x1 dd x2 hOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ;J ðyÞihOΔ̃0 ðx1 ÞÔΔ̃0 ðx2 ÞOΔ̃0 ;J0 ðy0 Þi


δðΔ − Δ̃0 Þ
0
TT
0
0
¼ 2πiN Δ;J δJ;J0 δðΔ − Δ ÞδJ ðy − y Þ þ
hOΔ;J ðyÞOΔ;J0 ðy Þi ;
ðΔ̃;JÞ
SΔ0 ;Δ0

ðA3Þ

where the traceless transverse delta function δTT
J was defined in the main text, and the shadow coefficient is
π 2 ΓðΔ̃ − d2ÞΓðΔ̃ þ J − 1ÞΓ2 ðΔþJ
2 Þ
d

ðΔ̃;JÞ

SΔ0 ;Δ0 ¼

ΓðΔ̃ − 1ÞΓðΔ þ JÞΓ2 ðΔ̃þJ
2 Þ

ðA4Þ

:

The reason for the second term in (A3) is because the basis elements for Δ and for Δ̃ are related by the shadow transform:
Z
1
hOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ;J ðyÞi ¼ ðΔ̃;JÞ
dd y0 hOΔ;J ðyÞOΔ;J ðy0 ÞihOΔ0 ðx1 ÞÔΔ0 ðx2 ÞOΔ̃;J ðy0 Þi:
ðA5Þ
SΔ0 ;Δ0

2. Bulk-to-boundary propagator basis
The differential equation (3.13) with boundary condition (3.14) has the explicit solution
Δ

z
GΔ;J ðx; zjyÞμ1 ;…;μJ ji1 ;…;iJ ¼
ðXμ1 ;i1 · … · XμJ ;iJ − tracesÞ;
ðx − yÞ2 þ z2

ðA6Þ

ðx−yÞ ðx−yÞ

−2ðx−yÞi
where Xi;j ¼ z−1 ðδi;j − 2 ðx−yÞi 2 þz2 j Þ, Xz;i ¼ ðx−yÞ
2 þz2 . The propagator satisfies the bulk analog of the shadow transform (A5):
Z
1
i01 …i0J
i01 …i0J 0
1 …iJ
1 …iJ
GiΔ;J
ðx; zjyÞμ1 ;…;μJ ¼ Δ̃;J dd y0 GΔ̃;J
ðx; zjy0 Þμ1 ;…;μJ hOiΔ;J
ðy0 ÞOΔ;J
ðy Þi;
ðA7Þ
SB

where SΔ̃;J
B was given in (3.15). The orthogonality relation takes the form
Z d
d xdz μ1 …μJ ji1 …iJ
i0 …i0
GΔ;J
ðx; zjx1 ÞGΔ̃10 ;J J ðx; zjx2 Þμ1 …μJ
dþ1
z
i0 …i0

J
1 …iJ
0 TT
1
¼ 2πiδðΔ − Δ̃0 ÞhOiΔ;J
ðx1 ÞOΔ;J
ðx2 ÞiSΔ̃;J
B þ 2πiδðΔ − Δ ÞδJ;i1 …ij ji0 …i0 ðx12 Þ
1

J

N Δ;J αJ
;
2

ðA8Þ

where δTT
J ðxÞ is defined in [52] as a delta function for traceless transverse spin J functions in d dimensions, N Δ;J is defined in
(A2), and

126011-16

## PDF page 17

AdS FROM CFT FOR SCALAR QED
αJ ≡

2J Γðd2 þ JÞ
π ΓðJ þ 1Þ
d
2

PHYS. REV. D 104, 126011 (2021)
ðA9Þ

:

μ ;…;μ jμ0 ;…;μ0
δTT1 J 1 J ðx; zjx0 ; z0 Þ ¼

Z

dΔ
2πi
P:S:

Z

The bulk completeness relation for traceless transverse bulk
functions is

μ ;…;μJ ji1 ;…;iJ

d

d y

where here δTT is defined in the bulk.

1
GΔ;J

1. Standard boundary conditions
The differential equation (4.10) with boundary condition
(4.11) can be formally solved using the split representation
0 0
ΠTT
Δ;J ðx; zjx ; z Þ ¼

ðx0 ; z0 jyÞ

dΔ Δ;J ðx; zjyÞGΔ̃;J
; ðB1Þ
2
2
γ J 2πi αJ N Δ;J ðM Δ;J − M Δ0 ;J Þ

where the boundary spin indices are contracted on the righthand side, while the bulk indices on both sides are implicit.
For massive propagators, i.e., Δ > d − 2 þ J or J ¼ 0, we
can close the contour and collect poles to get the explicit

g0 ðuÞ ¼

ðA10Þ

0 0
0 0
ΠTT
Δ;J ðx; zjx ; z Þ ¼ ΠΔ;J ðx; zjx ; z Þ

−

dþJ−2
X

ð2p − dÞ
2
2
M
Δ;J − M p;J
p¼d−1

× Res½ΠΔ0 ;J ðx; zjx0 ; z0 ÞΔ0 ¼p ;

ðB2Þ

where ΠΔ;J is the standard massive bulk-to-bulk propagator
whose explicit form is given by a complicated recursion
relation in [56]. For instance, the J ¼ 0 propagator is

1−d
ΠΔ;0 ðx; zjx0 ; z0 Þ ¼ CΔ;0 ð2uÞ−Δ 2 F1 Δ; Δ þ
; 2Δ
2

2
− d þ 1; − ;
ðB3Þ
u
where the chordal distance is
P
x x0 þ zz0
u¼ i i i0
;
2zz

ðB4Þ

and note that ΠTT
Δ;0 ¼ ΠΔ;0 since transversality and tracelessness are trivial for J ¼ 0. For J ¼ 1 the propagator is
0 0
ΠTT
Δ;1 ðx;zjx ;z Þμjμ0 ¼ −g0 ðuÞ∂ μ ∂ μ0 u þ g1 ðuÞ∂ μ u∂ μ0 u;

ðB5Þ

where g0 ðuÞ and g1 ðuÞ are

ðd − ΔÞΓðΔ þ 1Þu−Δ 2 F1 ðΔ; 12 ð−d þ 2Δ þ 1Þ; −d þ 2Δ þ 1; − u2Þ
π d=2 2Δþ1 ðΔ − 1Þðd − Δ − 1ÞΓð− d2 þ Δ þ 1Þ
−

g1 ðuÞ ¼

;

position-space expression

In this Appendix, we will show explicit expressions for
the bulk-to-bulk propagators discussed in the main text. We
will start by reviewing the traceless transverse propagators
ΠTT
Δ;J introduced in [8], which are defined by the differential
equation (4.10) with standard boundary condition (4.11).
These have explicit position space expressions for all J and
Δ ≥ d − 2 þ J. For J ¼ 1, we will also give the explicit
expression in momentum space. We will then consider the
J ¼ 1 propagator defined by the same differential equation (4.10) but with the alternate boundary condition (4.19),
which we will also write explicitly in momentum space.
From these momentum space expressions, we can immediately see the identity (4.18).

0G

ðx0 ; z0 jyÞ

αJ N Δ;J

APPENDIX B: BULK-TO-BULK PROPAGATORS

Z

μ0 ;…;μ0J ji1 ;…;iJ

1
ðx; zjyÞGΔ̃;J

ðu þ 1ÞΓðΔ þ 1Þu−Δ−1 2 F1 ðΔ þ 1; 12 ð−d þ 2Δ þ 1Þ; −d þ 2Δ þ 1; − u2Þ
;
π d=2 2Δþ1 ðΔ − 1Þðd − Δ − 1ÞΓð− d2 þ Δ þ 1Þ

ðu þ 1Þðd − ΔÞΓðΔ þ 1Þu−Δ−1 2 F1 ðΔ; 12 ð−d þ 2Δ þ 1Þ; −d þ 2Δ þ 1; − u2Þ
π d=2 2Δþ1 ðΔ − 1Þðu þ 2Þðd − Δ − 1ÞΓð− d2 þ Δ þ 1Þ
−

ðd þ ðu þ 1Þ2 ÞΓðΔ þ 1Þu−Δ−2 2 F1 ðΔ þ 1; 12 ð−d þ 2Δ þ 1Þ; −d þ 2Δ þ 1; − u2Þ
:
π d=2 2Δþ1 ðΔ − 1Þðu þ 2Þðd − Δ − 1ÞΓð− d2 þ Δ þ 1Þ

ðB6Þ

In the massless limit Δ → d − 2 þ J, the Δ0 ¼ d − 2 þ J pole in (B1) becomes a double pole and we get the finite result

126011-17

## PDF page 18

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)

0 0
0 0
ΠTT
d−2þJ;J ðx; zjx ; z Þ ¼ ∂ Δ ½ðΔ − d − J þ 2ÞΠΔ;J ðx; zjx ; z ÞΔ¼d−2þJ −

−

Res½ΠΔ0 ;J ðx; zjx0 ; z0 ÞΔ0 ¼d−ð2−JÞ
4 − d − 2J

dþJ−3
X

ð2p − dÞ
Res½ΠΔ0 ;J ðx; zjx0 ; z0 ÞΔ0 ¼p :
2
2
M
−
M
p;J
Δ;J
p¼d−1

ðB7Þ

For J ¼ 1, the massless propagator ΠTT
d−1;1 is the same as the position space Landau gauge propagator given in [57], which
can be explicitly checked from the definitions given here.
We will find it convenient to express ΠTT
d−1;1 in momentum space. Instead of directly transforming the known position
space expression, we can instead solve the differential equation (4.10) in momentum space. We start by writing the bulk-toboundary differential equation (3.13) in momentum space as
ðz2 ∂ 2z þ ð3 − dÞz∂ z − p2 z2 ÞGd−1;1 ðp; zÞi;j − 2izpi Gd−1;1 ðp; zÞz;j ¼ 0;
ðz2 ∂ 2z þ ð3 − dÞz∂ z − p2 z2 þ 1 − dÞGd−1;1 ðp; zÞz;j þ 2iz

d
X

pi Gd−1;1 ðp; zÞi;j ¼ 0;

ðB8Þ

i¼1

with the z → 0 boundary condition (3.14). We can solve this to get


d
d
pi pj
π 2 22−2
d
−1
z
Gd−1;1 ðp; zÞi;j ¼
ðjpjzÞ þ δi;j ðd − 2ÞK d−2
ðjpjzÞ
jpzj2
K d−4
2
2
ΓðdÞ
jpj
π 2 22−2
d
ðjpjzÞ;
jpzj2−1 · ðipj zÞK d−2
2
ΓðdÞ
d

Gd−1;1 ðp; zÞz;j ¼

d

ðB9Þ

which is the momentum space version of (A6). Next, we use transversality to rewrite (4.10) as
∂ μ ðz3−d ð∂ μ Πνρ − ∂ ν Πμρ ÞÞ ¼ −δν;ρ δðx; zjx0 ; z0 Þ þ z−d−1 ∂ ρ0 z2 ∂ ν Πd;0 ;
(
Z
3p
I d2 ðjpjzÞK d2 ðjpjz0 Þ
d
d
0
0
0
0
ip·ðx−x
Þ
Πd;0 ðx; zjx ; z Þ ¼ ðzz Þ2
e
ð2πÞ3
I d2 ðjpjz0 ÞK d2 ðjpjzÞ

z < z0
z0 < z

;

ðB10Þ

which we then write in momentum space as
∂ z ðz

−dþ3

0

0

ð∂ z Πd−1;1 ðp; z; z Þi;j − ipi Πd−1;1 ðp; z; z Þz;j ÞÞ − z

−dþ3



d
X
2
0
0
p Πd−1;1 ðp; z; z Þi;j þ pi
pk Πd−1;1 ðp; z; z Þk;j
k¼1

¼ −δi;j δðz − z0 Þ − z−dþ1 pi pj0 Πd;0 ðp; z; z0 Þ;

ðB11Þ
(
0

0 d2

Πd;0 ðp; z; z Þ ¼ ðzz Þ

I d2 ðpzÞK d2 ðpz0 Þ z < z0
I d2 ðpz0 ÞK d2 ðpzÞ z0 < z

:

ðB12Þ

We can solve this equation along with the boundary condition (4.11) and the explicit momentum space Gd−1;1 ðp; zÞ to get


pi pj
pi pj
TT
0
0 d2−1 d−2
0 d−2
0
Πd−1;1 ðp; z; z Þi;j ¼ ðzz Þ K 2 ðpz ÞI 2 ðpzÞ δi;j − 2 þ 4 ½ðzz0 Þd−1 ∂ z;z0 ððzz0 Þ−dþ1 ΠTT
d−1;1 ðp; z; z Þz;z0 Þ;
p
p
pi d−1
0
0
∂ z ðz−dþ1 ΠTT
ΠTT
d−1;1 ðp; z; z Þi;z0 ¼ i 2 z
d−1;1 ðp; z; z Þz;z0 Þ;
p
pj 0 d−1
0
0
∂ z0 ððz0 Þ−dþ1 ΠTT
ΠTT
d−1;1 ðp; z; z Þz;j ¼ −i 2 ðz Þ
d−1;1 ðp; z; z Þz;z0 Þ;
p
0
ΠTT
d−1;1 ðp; z; z Þz;z0 ¼ −

p2
ð∂ Π ðp; z; z0 ÞÞjΔ¼d−1 ;
d − 2 Δ Δ;0

ðB13Þ

where ΠΔ;0 ðp; z; z0 Þ is the scalar bulk-to-bulk propagator

126011-18

## PDF page 19

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)
(
0

ΠΔ;0 ðp; z; z Þ ¼

ðzz0 Þ2 I Δ−d2 ðjpjzÞK Δ−d2 ðjpjz0 Þ z < z0
d

ðzz0 Þ2 I Δ−d2 ðjpjz0 ÞK Δ−d2 ðjpjzÞ z > z0
d

:

ðB14Þ

2. Alternate boundary conditions for J = 1
We will now solve the differential equation (B11) with the alternate boundary conditions (4.19). We start by computing
the alternate bulk-to-boundary propagator Gζ;k
1;1 ðp; zÞ, by solving (B8) with the boundary condition (4.20) and the explicit
momentum space photon 2-point function given in the first line of (2.15), which depends on the family of gauge-fixings
parameterized by ζ ∈ R, as well as the Chern-Simons coupling k for d ¼ 3. For d ≠ 3 we get


d
d
2−d d−2 
pi pj
22−2 π 2 ΓðdÞjpj 2 z 2
4ð1 − ζÞ pi pj
d−2
d
Gζ1;1 ðp; zÞi;j ¼
K
−
ðjpjzÞ
þ
ðjpjzÞ
;
δ
zK
i;j
2
2
d − 2 jpj
p2
Γð2 − d2ÞΓðd2 − 1ÞΓ2 ðd2Þ
2 2 π 2 ΓðdÞ
2−d d
ðζ − 1Þjpj 2 z2 K d−2
ðjpjzÞpj ;
d 3 d
2
Γð2 − 2ÞΓ ð2Þ
d−2

Gζ1;1 ðp; zÞz;j ¼ i

d

ðB15Þ

while for d ¼ 3 and general k we get
pp
p
−jpjz 1 ðδi;j þ i 2j ðð1 − ζÞð1 þ pzÞ − 1ÞÞ − κ εijk k
16
2π
jpj
jpj
1 2
jpj
ð2πκ Þ2 þ ð16
Þ

e
Gζ;k
1;1 ðp; zÞi;j ¼
Gζ;k
1;1 ðp; zÞz;j ¼ i

16ð1 − ζÞ −jpjz z
p:
e
2
jpj j
1 þ ð16κ
2π Þ

ðB16Þ

We can then solve (B11) with the alternate boundary conditions (4.19) to get for d ≠ 3:


pi pj
pi pj
ζ
0
0 d2−1 d−2
0 2−d
Π1;1 ðp; z; z Þi;j ¼ ðzz Þ K 2 ðpz ÞI 2 ðpzÞ δi;j − 2 þ 4 ½ðzz0 Þd−1 ∂ z;z0 ððzz0 Þ−dþ1 Πζ1;1 ðp; z; z0 Þz;z0 Þ;
p
p
p
Πζ1;1 ðp; z; z0 Þi;z0 ¼ i 2i zd−1 ∂ z ðz−dþ1 Πζ1;1 ðp; z; z0 Þz;z0 Þ;
p
pj
Πζ1;1 ðp; z; z0 Þz;j ¼ −i 2 ðz0 Þd−1 ∂ z0 ððz0 Þ−dþ1 Πζ1;1 ðp; z; z0 Þz;z0 Þ;
p
Πζd−1;1 ðp; z; z0 Þz;z0 ¼ −

p2
4
d
ðjpjzÞK d−2
ðjpjz0 Þ; ðB17Þ
ðζ − 1Þp2 ðzz0 Þ2 K d−2
ð∂ Π ðp; z; z0 ÞÞjΔ¼d−1 þ
d
d
2
2
d − 2 Δ Δ;0
ðd − 2ÞΓð2 − 2ÞΓð2Þ

where we fixed the coefficients to match (4.19), (4.20) and (2.15).
For d ¼ 3 and general k, we instead get (demanding (4.8) as boundary conditions)
 −jpjðz0 þzÞ  2  2 


pi pj
1
e
1
κ
κ
pk
ζ;k
0
Π1;1 ðp; z; z Þi;j ¼
ε
δi;j − 2 −
−
1 2
2p ð2πκ Þ2 þ ð16
16
2π
16π ijk jpj
p
Þ


pi pj
pi pj
−jpjjz0 −zj
0
δi;j − 2
þ
½ðzz0 Þ2 ∂ z;z0 ððzz0 Þ−2 Πζ;k
þe
1;1 ðp; z; z Þz;z0 Þ
p
jpj4
pi 2
0
−2 ζ;k
0
Πζ;k
1;1 ðp; z; z Þi;z0 ¼ −i 2 z ∂ z ðz Π1;1 ðp; z; z Þz;z0 Þ
p
pj 0 2
0
0 −2 ζ;k
0
Πζ;k
1;1 ðp; z; z Þz;j ¼ i 2 ðz Þ ∂ z0 ððz Þ Π1;1 ðp; z; z Þz;z0 Þ
p

jpj 0 −jpjðzþz0 Þ
0
ζ;k
0
Π1;1 ðp; z; z Þz;z0 ¼
zz ðe
Eið2jpjzÞ þ ejpjðzþz Þ Eið−2jpjz0 ÞÞ
2
0

0

− ðe−jpjðz −zÞ Eið−2jpjzÞ þ e−jpjðz−z Þ Eið−2jpjz0 ÞÞ þ 2


1−ζ
−jpjðzþz0 Þ
:
e
2
1 þ ð16κ
2π Þ

ðB18Þ

ζ;k
0
0
Finally, the difference between ΠTT
d−1;1 ðp; z; z Þ and Π1;1 ðp; z; z Þ can be written in terms of the momentum space bulk-toboundary propagators and the effective photon propagator (2.14) as

126011-19

## PDF page 20

AHARONY, CHESTER, and URBACH

PHYS. REV. D 104, 126011 (2021)
3d

8π 2
ðΠTT ðp; z1 ; z2 Þμjμ0 − Πζ;k
Gd−1;1 ðp; z1 Þijμ hAi ðpÞA ð−pÞiζ;∞;k Gd−1;1 ð−p; z2 Þi0 jμ0 ¼ d−2
1;1 ðp; z1 ; z2 Þμjμ0 Þ;
Γð 2 ÞΓðdÞ d−1;1
i0

ðB19Þ

which gives (4.18) in position space.

[1] J. M. Maldacena, The large N limit of superconformal field
theories and supergravity, Int. J. Theor. Phys. 38, 1113
(1999); Adv. Theor. Math. Phys. 2, 231 (1998).
[2] E. Witten, Anti-de Sitter space and holography, Adv. Theor.
Math. Phys. 2, 253 (1998).
[3] S. Gubser, I. R. Klebanov, and A. M. Polyakov, Gauge
theory correlators from noncritical string theory, Phys. Lett.
B 428, 105 (1998).
[4] L. Eberhardt, M. R. Gaberdiel, and R. Gopakumar, Deriving
the AdS3 =CFT2 correspondence, J. High Energy Phys. 02
(2020) 136.
[5] A. Dei, M. R. Gaberdiel, R. Gopakumar, and B. Knighton,
Free field world-sheet correlators for AdS3, J. High Energy
Phys. 02 (2021) 081.
[6] L. Eberhardt, AdS3 =CFT2 at higher genus, J. High Energy
Phys. 05 (2020) 150.
[7] H. Bertle, A. Dei, and M. R. Gaberdiel, Stress-energy tensor
correlators from the world-sheet, J. High Energy Phys. 03
(2021) 036.
[8] O. Aharony, S. M. Chester, and E. Y. Urbach, A derivation
of AdS=CFT for vector models, J. High Energy Phys. 03
(2021) 208.
[9] I. R. Klebanov and A. M. Polyakov, AdS dual of the
critical O(N) vector model, Phys. Lett. B 550, 213
(2002).
[10] S. R. Das and A. Jevicki, Large N collective fields and
holography, Phys. Rev. D 68, 044011 (2003).
[11] R. de Mello Koch, A. Jevicki, K. Jin, and J. P. Rodrigues,
AdS4 =CFT3 Construction from collective fields, Phys. Rev.
D 83, 025006 (2011).
[12] R. de Mello Koch, A. Jevicki, J. a. P. Rodrigues, and J.
Yoon, Canonical formulation of OðNÞ vector/higher spin
correspondence, J. Phys. A 48, 105403 (2015).
[13] R. de Mello Koch, A. Jevicki, J. P. Rodrigues, and J. Yoon,
Holography as a gauge phenomenon in higher spin duality,
J. High Energy Phys. 01 (2015) 055.
[14] R. de Mello Koch, A. Jevicki, K. Jin, J. P. Rodrigues, and Q.
Ye, S ¼ 1 in O(N)/HS duality, Classical Quant. Grav. 30,
104005 (2013).
[15] R. de Mello Koch, A. Jevicki, K. Suzuki, and J. Yoon, AdS
maps and diagrams of bi-local holography, J. High Energy
Phys. 03 (2019) 133.
[16] M. A. Vasiliev, Consistent equation for interacting gauge
fields of all spins in (3 þ 1)-dimensions, Phys. Lett. B 243,
378 (1990).
[17] M. A. Vasiliev, More on equations of motion for interacting
massless fields of all spins in (3 þ 1)-dimensions, Phys.
Lett. B 285, 225 (1992).

[18] M. A. Vasiliev, Higher spin gauge theories in fourdimensions, three-dimensions, and two-dimensions, Int. J.
Mod. Phys. D 05, 763 (1996).
[19] Y. Neiman, Higher-spin gravity as a theory on a fixed (anti)
de Sitter background, J. High Energy Phys. 04 (2015) 144.
[20] I. R. Klebanov and E. Witten, AdS=CFT correspondence
and symmetry breaking, Nucl. Phys. B556, 89 (1999).
[21] E. Witten, Multitrace operators, boundary conditions, and
AdS=CFT correspondence, arXiv:hep-th/0112258.
[22] E. Witten, SL(2,Z) action on three-dimensional conformal
field theories with Abelian symmetry, in From Fields to
Strings: Circumnavigating Theoretical Physics: A
Conference in Tribute to Ian Kogan (World Scientific, 2003).
[23] C.-M. Chang, S. Minwalla, T. Sharma, and X. Yin, ABJ
triality: From higher spin fields to strings, J. Phys. A 46,
214009 (2013).
[24] M. Berkooz, A. Sever, and A. Shomer, “Double trace”
deformations, boundary conditions and space-time singularities, J. High Energy Phys. 05 (2002) 034.
[25] T. Appelquist, D. Nash, and L. C. R. Wijewardhana, Critical
Behavior in (2 þ 1)-Dimensional QED, Phys. Rev. Lett. 60,
2575 (1988).
[26] A. K. Nguyen and A. Sudbø, Topological phase fluctuations, amplitude fluctuations, and criticality in extreme typeII superconductors, Phys. Rev. B 60, 15307 (1999).
[27] K. Kajantie, M. Laine, T. Neuhaus, A. Rajantie, and K.
Rummukainen, Duality and scaling in three-dimensional
scalar electrodynamics, Nucl. Phys. B699, 632 (2004).
[28] T. Appelquist and D. Nash, Critical Behavior in (2 þ 1)Dimensional QCD, Phys. Rev. Lett. 64, 721 (1990).
[29] O. Aharony, G. Gur-Ari, and R. Yacoby, d ¼ 3 bosonic
vector models coupled to Chern-Simons gauge theories,
J. High Energy Phys. 03 (2012) 037.
[30] S. Giombi and X. Yin, The higher spin/vector model duality,
J. Phys. A 46, 214003 (2013).
[31] O. Aharony, O. Bergman, and D. L. Jafferis, Fractional M2branes, J. High Energy Phys. 11 (2008) 043.
[32] D. J. Binder, S. M. Chester, and M. Jerdee, ABJ correlators
with weakly broken higher spin symmetry, J. High Energy
Phys. 04 (2021) 242.
[33] L. Fei, S. Giombi, and I. R. Klebanov, Critical OðNÞ models
in 6 − ϵ dimensions, Phys. Rev. D 90, 025018 (2014).
[34] S. M. Chester, S. S. Pufu, and R. Yacoby, Bootstrapping
OðNÞ vector models in 4 < d < 6, Phys. Rev. D 91, 086014
(2015).
[35] S. Giombi, R. Huang, I. R. Klebanov, S. S. Pufu, and G.
Tarnopolsky, The OðNÞ model in 4 < d < 6: Instantons and
complex CFTs, Phys. Rev. D 101, 045013 (2020).

126011-20

## PDF page 21

AdS FROM CFT FOR SCALAR QED

PHYS. REV. D 104, 126011 (2021)

[36] A. Jevicki and B. Sakita, The quantum collective field
method and its application to the planar limit, Nucl. Phys.
B165, 511 (1980).
[37] S. M. Chester and S. S. Pufu, Anomalous dimensions of scalar
operators in QED3 , J. High Energy Phys. 08 (2016) 069.
[38] S. M. Chester, L. V. Iliesiu, M. Mezei, and S. S. Pufu,
Monopole operators in Uð1Þ Chern-Simons-matter theories,
J. High Energy Phys. 05 (2018) 157.
[39] S. M. Chester, Anomalous dimensions of monopole operators in scalar QED3 with Chern-Simons term, J. High
Energy Phys. 07 (2021) 034.
[40] S. Giombi, I. R. Klebanov, and G. Tarnopolsky, Conformal
QEDd , F-theorem and the ϵ expansion, J. Phys. A 49,
135403 (2016).
[41] A. Kapustin, Wilson-’t Hooft operators in four-dimensional
gauge theories and S-duality, Phys. Rev. D 74, 025005 (2006).
[42] S. M. Chester, M. Mezei, S. S. Pufu, and I. Yaakov, Monopole operators from the 4 − ϵ expansion, J. High Energy Phys.
12 (2016) 015.
[43] V. Borokhov, A. Kapustin, and X.-k. Wu, Topological
disorder operators in three-dimensional conformal field
theory, J. High Energy Phys. 11 (2002) 049.
[44] S. Giombi and X. Yin, Higher spin gauge theory and
holography: The three-point functions, J. High Energy
Phys. 09 (2010) 115.
[45] S. Caron-Huot, Analyticity in spin in conformal theories,
J. High Energy Phys. 09 (2017) 078.
[46] N. Craigie, V. Dobrev, and I. Todorov, Conformally covariant composite operators in quantum chromodynamics,
Ann. Phys. (N.Y.) 159, 411 (1985).

[47] M. R. Gaberdiel, R. Gopakumar, and A. Saha, Quantum
W-symmetry in AdS3 , J. High Energy Phys. 02 (2011) 004.
[48] M. R. Gaberdiel, D. Grumiller, and D. Vassilevich, Graviton
1-loop partition function for 3-dimensional massive gravity,
J. High Energy Phys. 11 (2010) 094.
[49] R. K. Gupta and S. Lal, Partition functions for higher-spin
theories in AdS, J. High Energy Phys. 07 (2012) 071.
[50] T. Hartman and L. Rastelli, Double-trace deformations,
mixed boundary conditions and functional determinants in
AdS=CFT, J. High Energy Phys. 01 (2008) 019.
[51] S. Giombi and X. Yin, On higher spin gauge theory
and the critical O(N) model, Phys. Rev. D 85, 086005
(2012).
[52] M. S. Costa, V. Gonçalves, and J. Penedones, Spinning AdS
propagators, J. High Energy Phys. 09 (2014) 064.
[53] S. Giombi, S. Minwalla, S. Prakash, S. P. Trivedi, S. R.
Wadia, and X. Yin, Chern-Simons theory with vector
fermion matter, Eur. Phys. J. C 72, 2112 (2012).
[54] V. K. Dobrev, G. Mack, I. T. Todorov, V. B. Petkova,
and S. G. Petrova, On the Clebsch-Gordan expansion for
the Lorentz group in n dimensions, Rep. Math. Phys. 9, 219
(1976).
[55] V. K. Dobrev, G. Mack, V. B. Petkova, S. G. Petrova, and
I. T. Todorov, Harmonic analysis on the n-dimensional
Lorentz group and its application to conformal quantum
field theory, Lect. Notes Phys. 63, 1 (1977).
[56] J. Penedones, Writing CFT correlation functions as AdS
scattering amplitudes, J. High Energy Phys. 03 (2011) 025.
[57] E. D’Hoker and D. Z. Freedman, Gauge boson exchange in
AdSðd þ 1Þ, Nucl. Phys. B544, 612 (1999).

126011-21
