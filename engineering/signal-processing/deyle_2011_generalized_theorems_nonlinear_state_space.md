Source: https://journals.plos.org/plosone/article/file
PDF sha256: 88517f27aa350f844b2aa7db2e622562b662152bc46af2ec9ab488cfbf0cceb5
License: CC-BY
Language: eng
Fidelity: machine (failed: characters)

# Transcription of deyle_2011_generalized_theorems_nonlinear_state_space.pdf

Transcription of `deyle_2011_generalized_theorems_nonlinear_state_space.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 3 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-2, 4-8 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Generalized Theorems for Nonlinear State Space
Reconstruction
Ethan R. Deyle, George Sugihara*
Scripps Institution of Oceanography, University of California San Diego, La Jolla, California, United States of America

Abstract
Takens’ theorem (1981) shows how lagged variables of a single time series can be used as proxy variables to reconstruct an
attractor for an underlying dynamic process. State space reconstruction (SSR) from single time series has been a powerful
approach for the analysis of the complex, non-linear systems that appear ubiquitous in the natural and human world. The
main shortcoming of these methods is the phenomenological nature of attractor reconstructions. Moreover, applied studies
show that these single time series reconstructions can often be improved ad hoc by including multiple dynamically coupled
time series in the reconstructions, to provide a more mechanistic model. Here we provide three analytical proofs that add to
the growing literature to generalize Takens’ work and that demonstrate how multiple time series can be used in attractor
reconstructions. These expanded results (Takens’ theorem is a special case) apply to a wide variety of natural systems having
parallel time series observations for variables believed to be related to the same dynamic manifold. The potential
information leverage provided by multiple embeddings created from different combinations of variables (and their lags) can
pave the way for new applied techniques to exploit the time-limited, but parallel observations of natural systems, such as
coupled ecological systems, geophysical systems, and financial systems. This paper aims to justify and help open this
potential growth area for SSR applications in the natural sciences.
Citation: Deyle ER, Sugihara G (2011) Generalized Theorems for Nonlinear State Space Reconstruction. PLoS ONE 6(3): e18295. doi:10.1371/journal.pone.0018295
Editor: Matej Oresic, Governmental Technical Research Centre of Finland, Finland
Received December 1, 2010; Accepted February 24, 2011; Published March 31, 2011
Copyright: ß 2011 Deyle, Sugihara. This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits
unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.
Funding: This work was supported by National Science Foundation (NSF) DEB1020372, NSF-NOAA CAMEO program (a partnership between the NSF and NOAA)
NA08OAR4320894/CAMEO, EPA-STAR Fellowship, Sugihara Family Trust, Deutsche Bank-Jameson Complexity Studies Fund, and the McQuown Chair in Natural
Sciences, University of California San Diego. The funders had no role in study design, data collection and analysis, decision to publish, or preparation of the
manuscript.
Competing Interests: The authors have declared that no competing interests exist.
* E-mail: gsugihara@ucsd.edu

apparent non-stationarity in correlations is one of the confounding
phenomena faced by traditional linear models that require
continual refitting and exhibit little or no predictive power.
In this paper, we present two general theorems that addresses
the problem of characterizing the coupled dynamics of nonlinear
systems using time series observations on a manifold M. A special
case of this theorem, attributed originally to Takens [12], provided
the first sketch of a mathematical proof for reconstructing a
diffeomorphic shadow manifold M’ using lags of a single time
series as coordinate axes. The basic idea, that was earlier
demonstrated by Packard, Crutchfield, Farmer, and Shaw [28]
and Crutchfield [2], is that under generic conditions, a shadow
manifold M’ can be created using time-lagged observations of M
based on a single observation function (Cartesian coordinate
variable) that is a smooth and smoothly invertible 1 : 1 mapping
with M. Subsequently, Sauer, Yorke, and Casdagli [29] provided
a definitive proof and an explicit extension of Takens’ theorem to
fractal sets; their theorems are also more powerful than the
original theorem, as they show embeddings are not just generic in
the sense of being open and dense in the set of all mappings, but in
fact almost every mapping in the sense of prevalence [30] is an
embedding (see [30] for an in-depth explanation of the advantages
of ‘‘prevalence’’ over ‘‘generic’’). The theorem was also extended
by Stark, Broomhead, Davies, and Huke [31,32] and Stark [33] to
include certain classes of stochastic systems. Practical methods for
reconstruction have also been explored, particularly to address the
presence of noise in real data (e.g. [29,34]). Casdagli et al. [35]

Introduction
A growing realization in many natural sciences is that simple
idealized notions of linearly decomposable, fixed equilibrium
systems often do not accord with reality. Rather, empirical
measurements on ecosystems, metabolic systems, financial networks, and the like suggest a more complex, but potentially more
information-rich paradigm at work [1–14]. Despite a long history
of linear methods development in the engineering sciences, natural
systems are generally not well described as sums of independent
frequencies that can be sensibly decomposed, analyzed as noninteracting, and reassembled (e.g. Fourier or spectral analysis) in
the style of traditional reductionism [15,16]. Rather, quantitative
measurements show many systems to be fundamentally nonequilibrium and unstable, in a manner more consistent with
nonlinear (state dependent) dynamics occurring on a strange
attractor manifold M, where relationships between state variables
cannot be studied independently of the overall system state
[17–27]. This emergent comprehensive view may help explain
why many natural systems, such a those mentioned above, appear
so difficult to understand and predict. Mirage correlations are
commonplace in nonlinear systems where the manifold may
contain trajectories that can temporarily exhibit positive correlations between variables for surprisingly long time periods (and in
some regions of the state space) and can subsequently and rapidly
exhibit negative correlations or no relationship in other time
periods (and other regions of M). This transient property of
PLoS ONE | www.plosone.org

1

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 2

Generalized Embedding Theorems

producing an immersion that is not an embedding. Immersions
are nonetheless a useful conceptual stepping stone for constructing
proofs about embeddings, since all embeddings are necessarily
immersions.
The Lorenz attractor, Figure 1(a), provides an excellent
example to illustrate both of these concepts. Consider two different
multivariate functions that transform the original manifold,
Wy ~(y(t),y(t{t),y(t{2t)) and Wz ~(z(t),z(t{t),z(t{2t))
where t is a small time lag as in Takens’ theorem. Both of these
functions map points on the true manifold to points on a shadow
manifold, shown in Figures 1(b) and 1(c). Examining these shadow
manifolds, it is evident that both are immersions of the Lorenz
attractor, because zooming in on a particular piece of either will
reveal that the tangent spaces have the same dimensionality as the
original. However, only Figure 1(b) is an embedding that
successfully reproduces the two lobes of the butterfly. The
reconstruction in Figure 1(c), based on lags of the z-coordinate,
fails to do so, because the two fixed points of the original attractor
have the same z-coordinate; they are mapped to the same point on
the shadow manifold, so the two lobes are stacked on top of each
other. This singularity is a consequence of a special, non-generic
symmetry in the Lorenz system that violates an assumption of
Takens’ theorem. Figure 1(d) shows an embedding based on lags
of both y- and z-coordinates and is an example of the generalized
mappings addressed in this paper.

give a thorough treatment of such techniques based on
transformations of univariate maps, showing how optimal noise
reduction can be achieved. These very important prior results all
focused on reconstruction from a single time series; however, as
proven below, they can be extended to the more practically
significant case where multiple observation functions are used to
generate M’.
Here we prove the more general case of multivariate
embeddings (embeddings using multiple time series and lags
thereof), and show how time series information can be leveraged if
multiple time series and their lags are used to construct
embeddings of M’. These theorems pave the way for more
extensive use of state space reconstruction methods in practical
applications where long time series may not be available, so that
multiple diffeomorphic embeddings may be created in factorial
fashion to more fully exploit the coupled non-redundant
information that can be extracted from multiple time series
(multiple observation functions of dynamics on a manifold) to
create predictive shadow manifolds [36]. The use of multiple time
series allows the possibility of noise reduction that exceeds the
limitations of univariate reconstructions in the presence of noise
[35].
The possibility of extending Takens’ theorem to allow lags of
multiple observation functions was mentioned in Remark 2.9 from
[29], but was not explicitly proven. The remark was also restricted
to mappings strictly formed from consecutive lags, which is not the
only possibility that needs to be considered in the multivariate
case. Given the potential importance of multivariate reconstructions, we believe a full proof is required—in particular, one that
extends the generalization to non-consecutive lags. We show how
Takens’ theorem is a special case of our more general Theorem 2
(below) and by following the structure of Takens’ original proof we
clarify the logic and highlight the restrictions and special cases
(non-generic cases) that can arise in its application to real world
systems. We then give explicit proof of a stronger version of
Remark 2.9 from Sauer et al. [29] that allows non-consecutive
lags. This third theorem is stronger than the first two in the sense
that it shows embeddings are prevalent and not just generic. For
those less familiar, we begin with a brief overview of some basic
terms and concepts used in our proofs.

Results
Two Theorems in the Style of Takens: The Generic Case
Let M be a compact manifold of dimension m. A dynamical
system is a diffeophorism w defining the trajectories or ‘‘flow’’ on
M for discrete time or a vector field X on M for continuous time.
Takens [12] proved generically that given w and M, a smooth
observation function y : M?R can be used to construct an
embedding of M in 2mz1 dimensions under the transformation
W(w,y) : M?R2mz1 where W(w,y) (x)~Sy(x),y(w(x)),y(w2 (x)), . . . ,
y(w2m (x))T. Here the components Sy(x),y(w(x)),y(w2 (x)), . . . ,
y(w2m (x))T correspond to time-lagged observations of the
dynamics on M defined by w. Notice that such mappings involve
a single distinct observation function (i.e. a single time series), and
represent a small subset in the larger set Y 2mz1 of all possible
mappings M?R2mz1 that could, for example, involve multiple
time series and their lags.
Takens explicitly refers only to the unlagged y as an observation
function, but in its most general sense an observation function is
any y : M?R. Thus, the functions y(w(x)),y(w2 (x)), . . ., corresponding to the lags of the time series are technically observation
functions as well. This bears mention, because in the more general
case of mappings W : M?R2mz1 , the observation functions
making up the components of W are not all derived from a single
time series, but can be various lags of multiple time-series. To treat
these cases, it is necessary to acknowledge that these are all
observation functions, and we will refer to distinct time series as
‘‘unlagged’’ observation functions.
For a mapping W in the larger set Y 2mz1 of all mappings
M?R2mz1 , consider the case with 2mz1 component functions
yk : M?R which are multiple unlagged observation functions of M
(i.e. multiple time series). Again, an observation function is any
function M?R that assigns a real number to each point on the
manifold M. For a mapping W : M?R2mz1 , we can think of W in
terms of its 2mz1 component functions, which correspond to the
coordinates in R2mz1 . These component functions may all be lags of
a single distinct observation function tracking a dynamical system, as
in the case of Takens, or they may be multiple observation functions,

Some Basic Concepts of Embedding Theory
Consider the classic Lorenz attractor [37] shown in Figure 1(a),
consisting of trajectories in three-dimensional space that together
define a butterfly shaped surface or manifold. For simplicity, a
manifold can be thought of as a generalized, n-dimensional surface
embedded in some higher dimensional space, where the dimension
of the manifold may be fractal (as is the case for the Lorenz
attractor). More generally, an embedding is a multivariate transformation of a manifold that resolves all trajectories on the original
manifold without crossings. That is, an embedding is globally 1 : 1
in that it resolves all singularities in trajectories that define the
manifold (singularities are points on the manifold where
trajectories cross so that future paths are not uniquely determined).
An immersion is a local embedding that may not preserve the
global topology of a manifold. Rather an immersion preserves the
topology of every local neighborhood of the original manifold, so
that each point of the tangent space of the immersed manifold has
the same dimensionality as the true manifold. Thus, an immersion
is a mapping that is 1 : 1 between any given ‘‘piece’’ of the true
manifold and the immersed manifold. However, this condition
does not guarantee that the global topology is preserved. This is
illustrated in Figure 1(c), where two different pieces of the original
manifold are mapped to the same piece of the immersed manifold,
PLoS ONE | www.plosone.org

2

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 3

Generalized Embedding Theorems
z(t)
<math>y(t-2\tau)</math>
x(t)
y(t)
(A)
(B)
<math>z(t-2\tau)</math>
z(t)
<math>y(t-\tau)</math>
y(t)
z(t)
(C)
(D)
Figure 1. Lorenz attractor with three shadow manifolds. The Lorenz attractor [37] is shown with three shadow manifolds created from lag-
coordinate transformations. The typical parameters were used: <math>\sigma = 10</math>, <math>\rho = 28</math>, and <math>\beta = 8/3</math>, giving the three coupled equations as <math>\dot{x} = 10(y - x)</math>,
<math>\dot{y}=28x-xz-y</math>, and <math>\dot{z}=xy-(8/3)z</math>. The solution was computed using a fourth order Runge-Kutta method with a time step of <math>\delta t=0.01</math>, and the time
lag used to create the shadow manifolds was <math>\tau = 8\delta t = 0.08</math>. (A) The trajectory shown in the x, y, and z coordinates of the original system reveals a
two-lobed manifold. (B) A univariate transformation using time lags of the y-coordinate, <math>\Phi = (y(t), y(t-\tau), y(t-2\tau))</math>, preserves this two-lobed structure
(and other topological properties), verifying Takens' theorem. (C) A univariate transformation using time lags of the z-coordinate,
<math>\Phi = (z(t), z(t-\tau), z(t-2\tau))</math>, does not preserve the two-lobed structure. Local neighborhoods of the original attractor are, however, preserved.
Thus, though this mapping violates a genericity assumption of the original theorem and is not an embedding, it is an immersion of the original
manifold. (D) A multivariate transformation using both the y- and z-coordinates, <math>\Phi = (y(t), y(t-\tau), z(t))</math>, fulfills the assumptions of Theorems 2 and 7.
As predicted, it also preserves the two-lobed structure of the Lorenz and is a valid embedding.
doi:10.1371/journal.pone.0018295.g001
zero" (e.g. in the sense of "shy" defined in [30]). To tackle this
as in the case of Whitney, or they may be lags of multiple observation
functions, as in Theorems 2 and 7 below.
problem, we look to the proof of Takens and see that it can be
readily generalized to the other subsets of <math>\mathcal{Y}^{2m+1}</math>, including the
The question arises whether general multivariate mappings
case of generic <math>\Phi \in \mathcal{Y}^{2m+1}</math>.
<math>\Phi(\mathbf{x}) = (y_1(\mathbf{x}), y_2(\mathbf{x}), \dots, y_{2m+1}(\mathbf{x}))</math> form legitimate embeddings.
Here we present two theorems: one that demonstrates that maps
Recall that, for a compact manifold, a mapping that is an
created from <math>2m+1</math> distinct observation functions are generically
immersion and injective is also necessarily an embedding. Thus,
embeddings and another that shows that maps created from lags of
Takens' general approach was to first show that (i) immersions are
multiple observation functions are also generically embeddings.
dense in the set of mappings <math>\{\Phi_{(\phi,\nu)}\}</math>, then that (ii) there is a dense
set of 1:1 mappings within this set of immersions. Since the set of
Both of these theorems generalize Takens' theorem for which the
component functions only involve a single observation function.
embeddings is open in the set of all possible mappings, Takens
It follows from Whitney [38] that generically <math>\Phi \in \mathcal{Y}^{2m+1}</math> is an
concludes that mappings in <math>\{\Phi_{(\phi,y)}\}</math> are generically embeddings.
embedding. Note, however, that Whitney's work does not apply to
The critical word here is "generically," meaning there can be
the specific subsets of <math>\mathcal{Y}^{2m+1}</math> involving fixed lagged relationships as
exceptions (and as explained in [30], the set of such exceptions
discussed by Takens for reconstructing attractor manifolds <math>M</math> for
doesn't necessarily have zero measure).
dynamic systems. That is, Whitney's theorem is generic and does
To demonstrate both (i) and (ii), Takens argues that even when
not address these specific subsets of <math>\mathcal{Y}^{2m+1}</math> which have "measure
the property of interest (e.g. the 1:1 property) does not hold for
PLoS ONE | www.plosone.org
March 2011 | Volume 6 | Issue 3 | e18295
3

## PDF page 4

Generalized Embedding Theorems

At each p [ Y(W )\D we know that r(x,x’)wd, so x and x0
cannot belong to the same Ui . Consequently, varying an eki or eki’
only alters the value of WSyk T at either x or x0 (respectively). In the
tangent space T p (R2mz1 |R2mz1 ), then, the direction of the
(2mz1)z(2mz1) infinitesimal changes given by the eki and eki’
are all linearly independent (indeed orthogonal) and as such span
T p (R2mz1 |R2mz1 ). Since the tangent spaces of Y(W ) and D are
at most 2m and 2mz1 dimensional, respectively,
can construct

 we 

LY
LY
and
that
a vector from a linear combination of
Leki p
Leki’ p


lies outside of both T p (Y(W )) and T p (D). Therefore, an
infinitesimal perturbation corresponding to this linear combination will move the sub-manifolds Y(W ) and D away from each
other at the point p without creating a new intersection at another
point. By keeping the size of these perturbations sufficiently small,
we ensure that we stay confined to U 0 , so that WSyk T is still an
immersion. This is a more transparent statement of the
transversality argument used in the Takens proof (1981).
Thus, we have shown that for any arbitrary set of 2mz1
observables S
yT, we can find a set of observables Syk T arbitrarily
close to S
yk T such that WSyk T is an embedding—i.e., there is a
dense set of observables fSyk Tg5Y 2mz1 such that WSyk T is an
embedding. The set of embeddings is open in the set of all
mappings, so this set is dense and open, meaning that the
embedding property is generic over all mappings.
When mappings are confined to fixed lag relationships, Takens
showed it is valid to independently perturb each component of W
at a given point of the domain by perturbing the unlagged
observation function, y, in the other parts of the domain
corresponding to neighborhoods of the lagged states w{1 (x),
w{2 (x), etc. This ensures that the perturbations to W maintain the
structure of the lag relationships and that we have not
inadvertently left the subset of interest. As we now show, this
allows the above result to be easily extended to families of maps
having component functions that are the lags of multiple
observation functions. This is the relevant case for many practical
examples where lags of multiple time series (multiple variables or
observation functions) are required to achieve a mechanistic
reconstruction of M (e.g. [20]). It also allows information on M to
be leveraged when the time series are short, as is the case in many
physical and biological problems [22,36].
Before starting the proof, however, we must clarify exactly what
the ‘‘subsets of interest’’ are. We define these sets as follows. First,
we say yq is a lag of the observable y if we can write yq ~wb (y) for
positive b. We consider the lags in the positive time direction only
to simplify notation in the proof, noting that the results apply
equally to negative lags. Let r~fr1 ,r2 , . . .g be the subset of
k~1, . . . ,2mz1 for which yr , r [ r is an unlagged observable, i.e.
yr is not a lag of another y [ Syk T. We begin with the ‘‘unlagged’’
observation functions, yr , or observation functions that are not a
lag of another observable in Syk T. Now define a set Cr for each
r [ r that contains yr and any other observation function in Syk T
which is a lag of it. That is, Cr is the set of yq [ Syk T that are lags
of yr given as yq ~wbq (yr ), where the lags bq are distinct for fixed r.
This choice of C~fCr : r [ rg and b~fbk : k~1, . . . ,2mz1g
2mz1
determine a subset Y~C,b
5Y 2mz1 containing all choices of
2mz1 observables Syk T which obey the correct lag relationships
2mz1
under a dynamical system w. Note that each element of Y~C,b
can
be identified by the dynamical system and the yr . We denote such
an element, then, as (w,Syr T).
Theorem 2. Consider a diffeomorphism w : M?M on some compact
manifold M of dimension m, along with 2mz1 observation functions
yk : M?R, smoothly; by ‘‘smooth’’ we mean at least C2 . Restrict the yk to
have the lag relationships corresponding to a collection of sets C and lags b

some particular mapping, by making an arbitrarily small
perturbation, it is possible to find a nearby mapping for which
that property holds. The key to the theorem and also to adapting it
to other sets of mappings is finding how to make these
perturbations. The proof is most straightforward for the general
case involving 2mz1 distinct observation functions (each a distinct
time series) because it is possible to perturb the component
functions of WSyk T independently. Thus we begin with this proof to
add clarity to the more powerful main theorem 2 involving lags of
multiple observation functions.
Theorem 1. Consider a compact, m-dimensional manifold M and a
set of 2mz1 observation functions Sy1 , . . . ,y2mz1 T, where yk : M?R
smoothly; by ‘‘smooth’’ we mean at least C2 . Then it is a generic property of
all possible Syk T that the mapping WSyk T : M?R2mz1 defined as
WSyk T ~ðy1 (x),y2 (x), . . . ,y2mz1 (x)Þ
is an embedding.
Proof. Consider an arbitrary set of 2mz1 observation
functions Syk T on M. We define a corresponding mapping
WSyk T [ Y 2mz1 by letting each of these 2mz1 observation
functions be one of the component functions of WSyk T . Now,
recall that an immersion is a map with a derivative that is globally
injective, i.e. 1 : 1. We denote the total derivative of a function f as
Df . If the derivative is evaluated at a particular point x in the
domain of f , we will write (Df )x , and if Df is a matrix, then we
denote the derivative at a particular point and along a particular
tangent vector v as (Df )x (v).
For any point x [ M, we can perturb the co-vectors
yk . By
(Dyk )x [ T  (M) independently by perturbing individual 
making infinitesimal perturbations at points x [ M for which
yk T
rank (DWSyk T )x vm, we can get a set of observables S
arbitrarily close to Syk T such that rank (DWSyk T )x ~m for all
x [ M—i.e., WSyk T is an immersion. Since the set of immersions is
open in the set of all mappings, there is a neighborhood
U5Y 2mz1 around this WSyk T such that every WSyk T [ U is an
immersion.
Since immersions are local embeddings, we can find a dw0
such that on the manifold, 0vr(x,x’)ƒd implies WSyk T (x)=
WSyk T (x0 ). Here we depart from Takens’ notation and let d denote
infinitesimal separations between two points on the manifold M to
avoid confusion with the later defined e which is used to perturb
the observable; r is any fixed metric on M. In fact for this fixed d,
there is a subset U 0 5U such that for any Syk T in U 0 , the associated
map WSyk T is an immersion, and r(x,x’)ƒd implies that
WSyk T (x)=WSyk T (x0 ).
Next, we show that we can find a globally 1 : 1 WSyk T [ U 0
arbitrarily close to WSyk T . To do this, we construct a finite
collection of subsets fUi gN
i~1 such that the Ui are open subsets of
M, the collection covers M, and diameter (Ui )vd for every i.
Then, we take a partition of unity fli g corresponding to these Ui ,
so that we can vary the value of any yk by an infinitesimal amount

yk ?yk zeki li without altering the value of Wyk (x) for x 6 [Ui .
We now consider the mapping Y : M|M?R2mz1 |R2mz1
defined as Y(x,x0 )~(Wyk (x),Wyk (x0 )). We define the set
W 5M|M as W ~f(x,x0 ) [ M|Mjr(x,x0 )§dg, so that (by
our choice of d), the mapping WSyk T is necessarily injective on the
complement of W in M|M. Furthermore, note that the
intersection of Y(W ) with the diagonal of R2mz1 |R2mz1 gives
the set of points f(x,x0 ) [ M|MjWyk (x)~WSyk T (x0 )g, and
therefore Y(W )\D~ 6 0 is equivalent to WSyk T injective. Our
task, then, is to perturb the manifold Y(W ) using the eki and eki’ so
that it does not intersect the diagonal manifold D.
PLoS ONE | www.plosone.org

4

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 5

Generalized Embedding Theorems

We now show that we can find a (w,S
yr T) [ U such that W(w,Syr T)
is an embedding on all of M. We first note that at points x [ M\V ,
the vectors (D
yk )x [ T  (M) can be perturbed independently, so
yT) [ U for which W(w,Syk T) is an immersion.
we can find (w,S
Because an immersion is a local embedding, there is a d such that
for x,x0 [ M, 0vr(x,x0 )vd implies that W(w,Syr T) (x)=
W(w,Syr T) (x0 ). Since the set of immersions is open in the set of
possible mappings, there is a neighborhood U 0 5U such that for
any (w,Syr T) [ U 0 , the corresponding mapping W(w,Syr T) is an
immersion. Thus, for the same d as above, 0vr(x,x0 )ƒd implies
W(w,Syr T) (x)=W(w,Syr T) (x0 ).
Now we need to show that there is a (w,Syr T) [ U 0 such that
W(w,Syr T) is also injective on M. As noted in the first proof, this is
equivalent to Y(V )\D~ 6 0 for the mapping Y : M|M?
R2mz1 |R2mz1 defined as Y(x,x0 )~(W(w,Syr T) (x),W(w,Syr T) (x0 )). If
x and x0 are both in V or r(x,x0 )ƒd, we already know that
W(w,Syr T) (x)=W(w,Syr T) (x0 ). Thus we restrict ourselves to the set
W ~fx,x0 [ M|Mjw(x,x0 )wd and not both x,x0 [ int(V )g.
To perturb the manifold Y(W ) away from D at points of
intersection, p [ Y(W )\D,
 wemust be able to find variations for
LY
which the tangent vector
is linearly independent from the
Le p
 


LY
LY
and
and lies outside of
2m tangent vectors
Lxi p
Lx’i p

T p (D). In the first proof, it was obvious that each component of Y
could be perturbed independently. Now we must be more careful.
We do this by first creating a collection of N open subsets of M,
fUi g, with the following properties:

under the dynamical system w, and impose the following generic [12,39]
properties on w:
1. The set A of periodic points with period pvmax(bk ) has finitely many
points,
2. The eigenvalues of (Dwb )x at each x in a compact neighborhood A are
distinct and not equal to 1.
2mz1
Then, for generic Syk T [ Y~C,b
, the mapping described by

W(w,Syr T) ~ðy1 (x),y2 (x), . . . ,y2mz1 (x)Þ
is an embedding.
Proof. The proof of this theorem closely follows the logic of
the previous proof and the original argument of Takens [12]. As
noted above, any perturbations to W via its component functions
2mz1
Syk T must remain within Y~C,b
(the set of observables having the
desired lag relationships under w prescribed by the Cr and the bq ).
Here we must also deal with points of M that are fixed points or
periodic under the dynamical system w, i.e. the points for which
there exists a b such that wb (x)~x (including the fixed point case,
b~1). The above proof shows that the mapping WSyk T is
generically an immersion because the co-vectors (D
yk )x [
T  (M) can be independently perturbed. This is also true for
non-periodic points where there are fixed lag relationships
between some observables, as we can perturb yr in the
neighborhood of w{bq (x) and thus perturb yq ~yr (wbq (x))
without affecting yr in the neighborhood of x.
Note that periodic points x can exist such that the period b or
some integer multiple of it, n:b, is the fixed time lag between two
observables yq1 ,yq2 [ Syk T belonging to the same Cr . Let V 5M
be a compact neighborhood : of all such points. For x [ V , the
vectors (Dyq1 )x and (D(yq1 0wn b ))x cannot necessarily
be perturbed
:
independently. Nonetheless, while yq1 (x)~yq1 (wn b (x)) for
such a
:
point, it is not generally true that (Dyq1 )x ~(D(yq1 0wn b ))x . By
assumption, for each x [ V , the eigenvalues of the (Dwb )x are
distinct and not equal to: 1. Thus, by the chain rule, it is clear that
(Dyq1 )x and (D(yq1 0wn b ))x are linearly independent. As noted
above, all the other (Dyk )x can be perturbed independently, so we
2mz1
can find a set of observables Syk T arbitrarily near Syk T in Y~C,b
for which W(w,Syr T) is an immersion on V . Note that because the set
2mz1
of immersions is open, there is an open neighborhood in Y~C,b
around this Syk T for which every set of observables in that
neighborhood gives an immersion.
We must also satisfy W(w,Syr T) injective. The proof above
relied on the ability to independently perturb the manifold
Y(W )5R2mz1 |R2mz1 at any point (x,x0 ) by an infinitesimal
amount in any coordinate direction. For a periodic point :on M
with perioid b and two observables related as yq and yq 0wn b , it is
impossible to independently perturb Y(W ) locally in : the
coordinate
yq (x) or yq (x0 ), as you also perturb yq (x)0wn b or
n :b
0
yq (x )0w . By assumption, the set V has a finite number of
2mz1
elements. For such a generic w and any set Syk T [ Y~C,b
, any
neighborhood of the Syk T will contain a set of observables S
yk T
for which the unlagged observation functions Syr T take distinct
values at each point in V .
We first perturb the yr to find an open neighborhood of
observables which give immersions when restricted to the set V .
We then further perturb the observables to find within this
neighborhood a set of observables Syk T for which W(w,Syr T) jV is
also injective and therefore an embedding (on V 5M). Since
embeddings are dense in the space of all mappings, there is a
2mz1
neighborhood U5Y~C,b
such that for all (w,Syr T) [ U, the map
W(w,Syr T) jV is an embedding.
PLoS ONE | www.plosone.org

1. The fUi g cover the closure of M\V .
2. For each bq and i~1, . . . ,N, the diameter of w{bq (Ui ) is less
than d.
3. For all choices of i,j [ f1, . . . ,Ng, the set Uj intersects with
w{bq (Ui ) for at most one bq .
4. For x and x0 such that w{b (x) [ M\|Ui for some b [ b,
x0 6 [V , and r(x,x0 )wd, no two of x,fwbq (x)g,x0 ,fwb (x0 )g
belong to the same Ui .
Take a partition of unity fli g corresponding to this fUi g.
Because of the way we constructed the fUi g, we can vary the value
of each 
yk at any point x [ M\V by an infinitesimal amount
without altering the value of the other 
yk in the neighborhood of x.
We make this explicit as follows. To perturb the yr , we take

yr ?
yr zeri li for i corresponding to x [ Ui . To perturb the other
yk (yk ~yr 0wbq for some r), we perturb 
yr ?
yr zeri li for i
corresponding to w{bq (x) [ Ui . Consider the 2mz1 perturbations,
eri , which are independent shifts at x in distinct yk . In
R2mz1 |R2mz1 , we note that each corresponding tangent vector
 
 
LY
LY
lies outside of T p (D). Note the
together with any
Leri p
Leri p
set of vectors. Since the
basis of T p (D) form a linearly independent
    !
LY
LY
dimension of span
,
is at most 2m, there must
Lxi p Lxi’ p
 
LY
that lies outside of both
be a linear combination of the
Leri p


T p (Y(W )) and T p (D), which can be used to perturb Y(W ) away
from D. By keeping variations in the eri sufficiently small, we can
find a set of Syk T such that (w,Syr T) [ U 0 and Y(x,x’)\D~ 6 0
(where Y now corresponds to the Ww,Syk T map). This pair gives a
mapping W(w,Syk T) that is both an immersion and injective, and
thus is an embedding. Because U 0 was an arbitrarily small
2mz1
neighborhood of any point in Y~C,b
, this means embeddings are
5

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 6

Generalized Embedding Theorems

2mz1
dense in Y~C,b
, and the set of embeddings is open in the set of
2mz1
mappings. Thus, the map W(w,Syr T) given by (w,Syr T) [ Y~C,b
is
generically an embedding.
Just as Takens extends the original result for discrete time to
dynamical systems in continuous time, we can extend our result as
follows:
Corollary 3. Consider a smooth vector field X on some compact
manifold M along with 2mz1 observables yk : M?R, smoothly; by
‘‘smooth’’ we mean at least C2 . Define wt as the flow on X . Suppose we
restrict the yk to have the lag relationships corresponding to a collection of sets
Cr and lags bq under the discrete dynamical system wt , where t is a constant.
We impose the following generic properties on X :

(Ap )vp=2. A sufficient condition for non-consecutive lags
is a bit more complicated. Define the constants Bpr ~
number of yq [ Cr such thatPbq ~m:pzbq’ for at least one bq’
and m [ N. Also, define Bp ~ r Bpr . A sufficient condition on the
Ap is 2:boxdim(Ap )vn{Bp .
Theorem 7. Let w be a diffeomorphism on an open subset U of Rm ,
and let A be a compact subset of U, boxdim(A)~d. Let C be
Pa collection
of sets and b a set of lag relationships as above, such that n~ r nr w2d.
Assume that for every positive integer pƒmax(fb [ bg), the set Ap of
periodic points of period p satisfies 2:boxdim(Ap )vn{Bp , and that for
each point of Ap , the Jacobian Dwp has distinct eigenvalues. Then, for almost
every set of n observation functions fyk g satisfying the given lag relationships,
the map

1. For points x such that X (x)~0, the eigenvalues of (Dwt )x are distinct
and not equal to 1.
2. No periodic integral curve of X has integer period ƒ2mz1.

W(w,Syr T) (x)~(y1 (x), . . . ,yn (x))
is an embedding on A.
Proof. Without loss of generality, assume we have ordered the
components of W(w,Syr T) with yr1 and all its lags first, then yr2 and
its lags, etc. That is,

2mz1
Then, for generic Syk T [ Y~C,b
, the mapping described by

W(wt ,Syr T) ~ðy1 (x),y2 (x), . . . ,y2mz1 (x)Þ
is an embedding.
Proof. In this case, wt is a discrete time dynamical system on
M satisfying the conditions imposed in the theorem above, and
this corollary follows directly.

b

W(w,Syr T) (x)~(yr1 (x),yr12 (x), . . . ,yr2 (x), . . . ):
To show prevalence, we find a suitable probe space (see [29]). The
infinite dimensional space for the univariate theorem is the
observation functions y : U?R, smoothly. For maps constructed
from multiple lags, this becomes the sets of sr ~size(r) unlagged
observation functions. Sauer et al. take the probe space for the
univariate theorem to be any set H of polynomials in m variables
which include all such polynomials up to degree 2n. It is now
necessary to have a set of polynomials for each of the yr . Thus, we
take the probe space for this theorem to be the Cartesian product
of sr copies of H.
Let Sh1 , . . . ,ht T be a basis for H. We want to show that for
almost all choices of sr |t coefficients ar,t , the
P map W(w,Syr T)
defined by the observation functions 
yr ~yr z ti~1 ar,i hi is an
embedding. We first demonstrate that almost every W(w,Syr T) is
1 : 1, proceeding as in the proof of Theorem 4.3 in [29].
To sensibly apply Lemma 5, we adopt the following convention:
think of W(w,Syr T) as a perturbation of W(w,Syr T) , which is the
summed effect of perturbations on each yr separately. For each
pair (r,i), r [ r and i [ f1, . . . ,tg, there is a map Wr,i : U?Rn
which is W(w,S~yr’ T) for ~
yr’ ~hi if r~r’ and 0 otherwise. The
components of Wr,i (x) are either 0PorPof the form hi (wbq (x)).
Consequently, Ww,Syr T ~Ww,Syr T z r ti~1 ar,i Wr,i (x), which
matches the structure Lemma 5.
We now check that the rank of the matrix Mx1 x2 satisfies the
conditions of Lemma 5 for each pair of distinct x1 ,x2 [ A. Note
that to avoid confusion with the previous section of this paper and
Takens’ original work, we continue to use row vectors to describe
the transformations W. However, Sauer et al. [29] prefer column
vectors, so it is necessary to use of transposes in several instances.
Thus, we have

A Theorem in the Style of Sauer et al.: The Prevalent Case
We now give an explicit proof of Remark 2.9 from [29] using
the framework constructed in their original paper, but we extend
the language to cover reconstructions using non-consecutive lags
(from multiple time series). The proof uses Lemma 4.1, 4.6, and
4.11 from [29] to show that 1 : 1 mappings and immersions are
2mz1
prevalent in the space Y~C,b
, just as Sauer et al. use Lemma 4.6 to
prove Theorem 3.3, and Lemmas 4.1 and 4.11 to prove Theorem
3.5. These lemmas are now stated (for the proofs, see their original
paper).
Lemma 4. (Originally part 2 of 4.1) Let n and k be positive integers,
x1 , . . . ,xn distinct points in Rk , u1 , . . . ,un in R, and v1 , . . . ,vn in Rk .
Then there exists a polynomial h in k variables of degree at most n such that
for i~1, . . . ,n, +h(xi )~vi .
Lemma 5. (Originally 4.6) Let A be a compact subset of Rk . Let
W0 ,W1 , . . . ,Wt : A?Rn be Lipschitz maps. For each integer r§0, let Sr
be the set of pairs x1 =x2 in A for which the n|t matrix
Mx1 x2 ~ðW1 (x1 ){W1 (x2 ), . . . ,Wt (x1 ){Wt (x2 )Þ
 r ). Define Wa ~
has rank r, and let dr ~ lower boxdim (S
P
W0 z ti~1 ai Wi : A?Rn . If dr vr for all integers r§0, then for
a~(a1 , . . . ,at ) outside a measure zero subset of Rt , the map Wa is 1 : 1.
Lemma 6. (Originally 4.11) Let A be a compact subset of a smooth
manifold embedding in Rk . Let W0 ,W1 , . . . ,Wt be a set of smooth maps from
an open neighborhood U of A to Rn . For each positive integer r, let Sr be the
subset of the unit tangent bundle S(A) such that the n|t matrix

1
Wr1 ,1 (x1 ){Wr1 ,1 (x2 )
C
B
..
C
B
.
C
B
C
B
T
C:
Mx x ~B
W
(x
){W
(x
)
r
,t
1
r
,t
2
C
B 1
1
1 2
C
B
W
(x
){W
(x
)
B r2 ,1 1
r2 ,1 2 C
A
@
..
.
0

ð(DW1 )x (v), . . . ,(DWt )x (v)Þ
 r ). Define Wa ~
has rank r, and let dr ~ lower boxdim (S
Pt
n
W0 z i~1 ai Wi : A?R . If dr vr for all integers r§0, then for
almost every a [ Rt , the map Wa is an immersion on A.
To apply these lemmas, it is necessary to restrict the dimension
of the sets of periodic orbits—that is, the sets Ap ~
fx [ A : wp (x)~xg for pvmax(fb [ bg). For the case of consecutive lags, Sauer et al. state sufficient conditions to be boxdim
PLoS ONE | www.plosone.org

Note that Mx1 x2 is a block diagonal matrix, and so it has rank
6

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 7

Generalized Embedding Theorems

the columns span Rnr . The dimension of S’ is certainly less than
2d{1, so we can safely apply Lemma 6.
Theorem 7 can be extended to continuous dynamical systems
(smooth vector fields on a manifold) by letting the flow wt of X be
w in the statement of the theorem.

equal to the sum of the rank of the blocks. Each of the sr blocks
can be rewritten as the product of two matrices, Jr and Hr , where
the entries of Hr are values of a single polynomial h and the entries
of Jr are each one of f1,0,{1g. Note, there are multiple possible
choices for Hr and Jr that give the same Mx1 x2 .
Case 1: First consider x1 and x2 that do not both lie in a periodic
orbit of integer period less than max(b). We specify Hr so that the
first nr rows, where nr is the size of the set Cr , correspond to the
hr,i (x1 ),hr,i (wbrz1 (x1 )), . . . ,hr,i (wbrznr (x1 )), and the next nr correspond to the hr,i (wbqr (x2 )). Hr is onto, so the rank of Mx1 x2 is just
the sum of the ranks of the Jr . For this case, Jr contains a copy of
Inr , and thus will
P have rank nr . The entire matrix Mx1 x2 will thus
have rank n~ r nr , which satisfies the conditions of Lemma 5.
Case 2: Now consider x1 and x2 in separate periodic orbits with
periods p1 and p2 such that 1ƒBp1 ƒBp2 and p1 ,p2 vmax(b). Hr
will have Bp1 r fewer rows corresponding to the bq1 ~m:p1 zbq2 for
some m [ N (there will also be a reduction in the number of rows
associated with Bp2 ). In this case, Jr will still
P contain the column
space of I(nr {Bp1 r ) and thus rank(J)§ r nr {Bp1 r ~n{Bp1 .
Again the Hr are onto, and so the rank of Mx1 x2 is the rank of J.
The dimension of the set S of all pairs x1 and x2 is
dim(S)~dim(Ap1 )zmax(dim(Ap2 )). By the conditions placed
on the size of the Ap , we can conclude that
dim(S)vn{Bp1 ƒdim(Mx1 x2 ), and thus that Lemma 5 applies
to this case as well.
Case 3: Finally we consider x1 and x2 in the same p-periodic
orbit, pvmax(b). Now the matrix Hr becomes more complicated,
since some of the h(z) pertaining to x2 may be equal to h(z)
pertaining to x2 . Consequently, the Jr are no longer guaranteed to
contain the column space of the identity. Each Jr does contain the
column space of an nr {Bpr dimensional matrix with 1 along the
upper diagonal and a single {1 off the diagonal in each column.
Using elementary operations, it is possible to make the first m
columns of Jr upper diagonal for some integer m§(nr {Bpr )=2.
Thus, the rank of each Jr is at least (nr {Bpr )=2 and the entire
matrix has rank(J)§(n{Bp )=2.
The dimension of the set S of all such x1 and x2 is just Ap . By
the imposed conditions, dim(S)v(n{Bp )=2ƒdim(Mx1 x2 ), and
Lemma 5 applies.
Now we want show that almost every W(w,Syr T) is an immersion.
We check that the matrix


(DWr1 ,1 )x (v)T , . . . ,(DWr1 ,t )x (v)T ,(DWr2 ,1 )x (v)T , . . .

Discussion
Theorem 1 and the more general result presented in Theorem 2
(and its corollary) were given proofs intended to follow those presented
by Takens. The original ‘‘transversality’’ argument, however, has been
replaced with what we reckon is a simpler and more direct argument.
These clarify how perturbations to the observation functions can be
constructed and highlight why 2mz1 dimensions are necessary to
have mappings that are generically embeddings. Theorem 7 is similar
to Theorem 2, but takes advantage of the more powerful framework,
built around the notion of prevalence, established by Sauer et al. [29].
It also provides more specific conditions on the periodic orbits than
Theorem 2 and thus can be applied to certain non-generic situations
that Takens’ original framework would exclude. Namely, the set of
periodic points need not be finite (as required in Takens’ original
theorem and Theorem 2), so long as the dimensionality does not
exceed the bounds stated in Theorem 7. Theorem 7 is an extension of
Remark 2.9 in [29], which we explicitly proved by determining a
sufficient restriction for the periodic orbits when the lags composing W
aren’t necessarily consecutive.
This work also develops a language to describe a wider family of
cases for reconstructing state space manifolds from multiple
observational time series to encourage wider applicability of SSR
in the natural sciences. For example, these results can be extended
to another special case of interest for reconstructions using time
derivatives [40], when multiple observation functions are available. The argument for this case is analogous to that used by
Takens [12] for the case when all the derivatives are from a single
observation function. Furthermore, these theorems validate
heuristic work using spatial lag reconstructions and mixed spatial
and temporal lag reconstructions to study spatially coupled
dynamics [41].
More importantly, in terms of future applications, Theorems
2 and 7 set the stage for practical reconstruction of state space
manifolds from multiple observation functions. This is significant in answering objections to single variable state space
reconstruction (SSR) concerning the excessive phenomenology
of lagged-coordinate embeddings [26]. These two theorems
provide proof of principle for modeling attempts of nonlinear
dynamics in the natural sciences involving multiple time series
(e.g. [20]), and lays bare the rather non-restrictive assumptions
required in such applications for building mechanistic models
from multiple time series variables. Moreover, it gives support to
the notion of using multiple embeddings as a potentially efficient
way of extracting information from time series data of limited
length, but where there are potentially many simultaneous
observations of dynamics on the same attractor manifold. By
reducing correlations in noise between the reconstructed
coordinates, these techniques should allow reconstructions to
exceed the limitations placed on univariate methods [35], as
heuristic examples have already suggested [20]. The potential
information leverage provided by multiple embeddings possible
from novel combinations of variables (and their lags) can pave
the way for a plethora of new applied techniques to exploit the
time-limited, but parallel observations of nature [36]. This
paper is intended to complement the existing literature on SSR
and help promote this potential growth area in the natural
sciences.



has full rank and thus satisfies the conditions of Lemma 6 for each
(x,v) in the tangent bundle S(A). Note that this is a block diagonal
matrix with sr blocks, so it is sufficient to show that the columns of
the ith block span the subspace Rnri for i~1, . . . ,sr . We consider
two cases.
Case 1: Consider first the subset S’ of x that are not periodic with
period pvmax(b). The entries of each block are of the form
+h(wb (x))T (Dwb )x (v). Since w is a diffeomorphism and v=0, we
know that (Dwb )x (v)=0. Furthermore, the wb (x) are distinct
points. Examining Lemma 4, it is clear that the columns span Rnr .
The dimension of S’ is at most 2d{1, so we may apply Lemma 6.
Case 2: Now consider the subset S’ of x that are periodic
with period pvmax(b). By the conditions of the theorem, (Dwb1 )x
has distinct eigenvalues from (Dwb2 )x . Therefore, +h(wb1 (x))T
(Dwb1 )x (v)=+h(wb2 (x))T (Dwb2 )x (v). Furthermore, the relationship depends on h, and again referencing Lemma 4, it is clear that

PLoS ONE | www.plosone.org

7

March 2011 | Volume 6 | Issue 3 | e18295

## PDF page 8

Generalized Embedding Theorems

Acknowledgments

Author Contributions

We wish to thank Hao Ye, James Crutchfield, John Melack, Donald
DeAngelis, Simon Levin, J. Doyne Farmer, Martin Casdagli, Tim Sauer,
Sarah Glaser, Chih-hao Hsieh, Stephen Munch and Charles Peretti,
Michael Fogarty, Alec MacCall, Andrew Rosenberg, Les Kaufman, and
Irit Altman for helpful comments and editorial advice.

Conceived and designed the experiments: ERD GS. Performed the
experiments: ERD GS. Analyzed the data: ERD GS. Contributed
reagents/materials/analysis tools: ERD GS. Wrote the paper: ERD GS.

References
21. Hsieh CH, Glaser SM, Lucas AJ, Sugihara G (2005) Distinguishing random
environmental fluctuations from ecological catastrophes for the North Pacific
Ocean. Nature 435: 336–340.
22. Hsieh CH, Anderson C, Sugihara G (2008) Extending nonlinear analysis to
short ecological time series. American Naturalist 171: 71–80.
23. Rodo X, Pascual M, Fuchs G, Faruque ASG (2002) ENSO and cholera: a
nonstationary link related to climate change? Proceedings of the National
Academy of Sciences of the United States of America 99: 12901–12906.
24. Schaffer WM (1984) Stretching and folding in lynx fur returns: evidence for a
strange attractor in nature? American Naturalist 124: 789–820.
25. Sugihara G, Grenfell B, May RM (1990) Distinguishing error from chaos in
ecological time series. Philosophical Transactions of the Royal Society of
London, Series B: Biological Science 330: 235–250.
26. Sugihara G, May RM (1990) Nonlinear forecasting as a way of distinguishing
chaos from measurement error in a data series. Nature 344: 734–741.
27. Sugihara G (1994) Nonlinear forecasting for the classification of natural time
series. Philosophical Transactions of the Royal Society of London, Series A 348:
477–495.
28. Packard NH, Crutchfield JP, Farmer JD, Shaw RS (1980) Geomtery from a time
series. Physical Review Letters 45: 712–716.
29. Sauer T, Yorke JA, Casdagli M (1991) Embedology. Journal of Statistical Physics
65: 579–616.
30. Hunt BR, Sauer T, Yorke JA (1992) Prevalence: a translation-invariant ‘‘almost
every’’ on infinite-dimensional spaces. Bulletin of the American Mathematical
Society 27: 217–238.
31. Stark J, Broomhead DS, Davies ME, Huke JP (1997) Takens embedding
theorems for forced and stochastic systems. Nonlinear Analysis: Theory,
Methods, and Applications 30: 5303–5314.
32. Stark J, Broomhead DS, Davies ME, Huke JP (2003) Delay embeddings for
forced systems: II. Stochastic forcing. Journal of Nonlinear Science 13: 519–577.
33. Stark J (1999) Delay embeddings for forced systems: I. Deterministic forcing.
Journal of Nonlinear Science 9: 255–332.
34. Gibson J, Farmer JD, Casdagli M, Eubank S (1992) An analytic approach to
practical state space reconstruction. Physica D 57: 1–30.
35. Casdagli M, Eubank S, Farmer JD, Gibson J (1991) State space reconstruction in
the presence of noise. Physica D 41: 52–98.
36. Ye H, Sugihara G, Deyle ER (2011) Leverging information from multiple time
series with ensemble state space reconstructions. In preparation.
37. Lorenz EN (1963) Deterministic nonperiodic flow. Journal of Atmospheric
Science 20: 130–141.
38. Whitney H (1936) Differentiable manifolds. Annals of Mathematics 37:
645–680.
39. Huke JP (1993) Embedding nonlinear dynamical systems, a guide to Takens’
theorem. Internal report, DRA, Malvern, UK.
40. Crutchfield JP, McNamara BS (1987) Equations of motion from a data series.
Complex Systems 1: 417.
41. Ørstavik S, Stark J (1998) Reconstruction and cross-prediction in coupled map
lattices using spatio-temporal embedding techniques. Physics Letters A 247:
145–160.

1. Casdagli M (1989) Nonlinear prediction of chaotic time series. Physica D 35:
335–356.
2. Crutchfield JP (1979) Prediction and stability in classical mechanics. Senior
thesis in physics and mathematics, University of California, Santa Cruz.
3. Farmer JD, Sidorowich JJ (1987) Predicting chaotic time series. Physical Review
Letters 59: 845–848.
4. Jenouvrier S, Weimerskirch H, Barbraud C, Park YH, Cazelles B (2005)
Evidence of a shift in the cyclicity of antarctic seabird dynamics linked to
climate. Proceedings of the Royal Society of London, Series B 272: 887–895.
5. Lo TT, Hsu HH (2010) Change in the dominant decadal patterns and the late
1980s abrupt warming in the extratropical northern hemisphere. Atmospheric
Science Letters 11: 210–215.
6. Planque B, Batten SD (2000) Calanus finmarchicus in the north atlantic: the year of
Calanus in the context of interdecadal change. ICES Journal of Marine Science
57: 1528–1535.
7. Ramanathan A, Wang C, Schreiber SL (2002) Perturbational profiling of a cellline model of tumorigenesis by using metabolic measurements. Proceedings of
the National Academy of Sciences of the United States of America 102:
5992–5997.
8. Ruelle D (1989) Chaotic evolution and strange attractors: the statistical analysis
of time series for deterministic nonlinear systems. Cambridge University Press,
Cambridge.
9. Scheffer M, Carpenter SR (2003) Catastrophic regime shifts in ecosystems:
linking theory to observation. Trends in Ecology & Evolution 18: 648–656.
10. Seth AK, Izhikevich E, Reeke GN, Edelman GM (2006) Theories and measures
of consciousness: an extended framework. Proceedings of the National Academy
of Sciences of the United States of America 103: 10799–10804.
11. Soramaki K, Bech ML, Arnold J, Glass RJ, Beyeler WE (2007) The topology of
interbank payment flows. Physica A 379: 317–333.
12. Takens F (1981) Detecting strange attractors in turbulence. In: Rand DA,
Young LS, eds. Symposium on Dynamical Systems and Turbulence. Berlin:
Springer-Verlag, volume 898 of Lecture Notes in Mathematics. pp 366–381.
13. Wagner BK, Kitami T, Gilbert TJ, Peck D, Ramanathan A, et al. (2008) Largescale chemical dissection of mitochondrial function. Nature Biotechnology 26:
343–351.
14. May RM, Levin SA, Sugihara G (2008) Complex systems: Ecology for bankers.
Nature 451: 893–895.
15. Sugihara G (2010) On early warning signs. Seed Magazine Global Reset 2010.
16. Sugihara G (2010) Nature is nonlinear. Kyoto Journal 75: 56–57.
17. Brock WA, Sayers CL (1988) Is the business cycle characterized by deterministic
chaos? Journal of Monetary Economics 22: 71–90.
18. Brock WA, Malliaris AG (1989) Differential Equations, Stability and Chaos in
Dynamic Economics, volume 27 of Advanced Textbooks in Economics. NorthHolland.
19. Brock WA, Hsieh DA, LeBaron BD (1991) Nonlinear Dynamics, Chaos, and
Instability: Statistical Theory and Economic Evidence. MIT Press, Cambridge,
Massachusettes.
20. Dixon PA, Milicich MJ, Sugihara G (1999) Episodic fluctuations in larval supply.
Science 283: 1528–1530.

PLoS ONE | www.plosone.org

8

March 2011 | Volume 6 | Issue 3 | e18295
