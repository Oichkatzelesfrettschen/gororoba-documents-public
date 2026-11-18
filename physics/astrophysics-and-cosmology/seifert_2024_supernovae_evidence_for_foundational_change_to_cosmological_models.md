Source: https://doi.org/10.1093/mnrasl/slae112
PDF sha256: 404ddc2172887ad09cecf02f4d79efc2533581641aaf344094c516a3fe14b47c
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of seifert_2024_supernovae_evidence_for_foundational_change_to_cosmological_models.pdf

Transcription of `seifert_2024_supernovae_evidence_for_foundational_change_to_cosmological_models.pdf` in this directory, 6 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-6 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

MNRAS 537, L55–L60 (2024)

https://doi.org/10.1093/mnrasl/slae112

Supernovae evidence for foundational change to cosmological models
Antonia Seifert ,1,2 Zachary G. Lane ,1 ‹ Marco Galoppo ,1 Ryan Ridden-Harper
and David L. Wiltshire 1

1

1 School of Physical and Chemical Sciences–Te Kura Matū, University of Canterbury, Private Bag 4800, Christchurch 8140, New Zealand
2 Institut für Theoretische Physik, Universität Heidelberg, Philosophenweg 12, D-69120 Heidelberg, Germany

Accepted 2024 November 21. Received 2024 November 20; in original form 2024 July 11

We present a new, cosmologically model-independent, statistical analysis of the Pantheon+ Type Ia Supernovae spectroscopic
data set, improving a standard methodology adopted by Lane et al. We use the Tripp equation for supernova standardization
alone, thereby avoiding any potential correlation in the stretch and colour distributions. We compare the standard homogeneous
cosmological model, i.e. spatially flat  cold dark matter (CDM), and the timescape cosmology which invokes backreaction
of inhomogeneities. Timescape, while statistically homogeneous and isotropic, departs from average Friedmann–Lemaˆıtre–
Robertson–Walker evolution, and replaces dark energy by kinetic gravitational energy and its gradients, in explaining independent
cosmological observations. When considering the entire Pantheon+ sample, we find very strong evidence (ln B > 5) in favour
of timescape over CDM. Furthermore, even restricting the sample to redshifts beyond any conventional scale of statistical
homogeneity, z > 0.075, timescape is preferred over CDM with ln B > 1. These results provide evidence for a need to revisit
the foundations of theoretical and observational cosmology.
Key words: gravitation – supernovae: general – cosmological parameters – dark energy – cosmology: theory.

1 I N T RO D U C T I O N
The  cold dark matter (CDM) model, which has served as the
standard cosmological model for quarter of a century, is facing
serious challenges in light of recent results (Abbott et al. 2024;
Adame et al. 2024) and may need to be reconsidered at a fundamental
level (Di Valentino et al. 2021; Peebles 2022; Aluri et al. 2023). In
this Letter, we present definite statistical evidence that the timescape
cosmological model (Wiltshire 2007a, b, 2009) outperforms CDM
in matching Type Ia Supernovae (SNe Ia) observations. It may
provide not only a viable alternative to the standard cosmological
model, but ultimately a preferred one. This result potentially has
far-reaching consequences not only for cosmology, but also for other
key aspects of astrophysical modelling from late epochs to the early
universe.
We perform an empirical cosmologically independent analysis
within which both the CDM and timescape cosmologies may be
embedded, and thus compared via Bayesian statistics. The timescape
model is a particular implementation of Buchert’s scalar averaging scheme which incorporates backreaction of inhomogeneities
(Buchert 2000, 2001; Wiltshire 2014; Buchert, Mourier & Roy 2020).
Instead of a matter density parameter relative to average Friedmann–
Lemaˆıtre–Robertson–Walker model (as in CDM), timescape is
characterized by the void fraction, fv , which represents the fractional volume of the expanding regions of the universe made up
by voids.

⋆ E-mail: zachary.lane@pg.canterbury.ac.nz

A key ingredient of the timescape model is a particular integrability
relation for the Buchert equations: the uniform quasi-local Hubble
expansion condition. Physically, it is motivated by an extension of
Einstein’s Strong Equivalence Principle to cosmological averages at
small scales (∼ 4 – 15 Mpc) where perturbations to average isotropic
expansion and average isotropic motion cannot be observationally
distinguished (Wiltshire 2008).
In standard cosmology, differences from average FLRW expansion
are assumed to be mostly attributed to local Lorentz boosts – i.e.
peculiar velocities – of source and observer, with gravitational
potentials contributing fractional variations of ∼ 10−5 of average
expansion at galaxy and galaxy cluster scales. In timescape, the
same fractional variation can be up to ∼ 10−3 and the equivalence of
different choices of background, via the Cosmological Equivalence
Principle, means that notions of average isotropic expansion persist
well into the non-linear regime of structure formation. The signature
of the emergent kinetic spatial curvature of voids has now been
identified in cosmological simulations using full numerical general
relativity without  (Williams et al. 2024).
Both the standard cosmology and the timescape model agree
empirically on a Statistical Homogeneity Scale (SHS), typically
given as zCMB ∼ 0.033 by the two-point galaxy correlation function
(Hogg et al. 2005; Scrimgeour et al. 2012; Dam, Heinesen &
Wiltshire 2017). Timescape offers its most important tests and
predictions below the SHS, at scales where the filaments, sheets
and voids of the cosmic web are still expanding but in the non-linear
regime.
To conduct our analysis, we use the largest spectroscopically confirmed SNe Ia data set, Pantheon+ (Scolnic et al. 2022). SNe Ia have

© 2024 The Author(s).
Published by Oxford University Press on behalf of Royal Astronomical Society. This is an Open Access article distributed under the terms of the Creative
Commons Attribution License (https://creativecommons.org/licenses/by/4.0/), which permits unrestricted reuse, distribution, and reproduction in any medium,
provided the original work is properly cited.

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

ABSTRACT

## PDF page 2

L56

A. Seifert et al.

been a pillar for informing the distance ladder used for cosmological
model comparison, and have a rich history in revolutionising the field
(Riess et al. 1998; Perlmutter et al. 1999). More modern methods for
standardizing SNe Ia light curves use the SALT2 fitting algorithm
(Guy et al. 2007; Taylor et al. 2021), as used by Pantheon+, and more
recently SALT3 (Kenworthy et al. 2021) used by the Dark Energy
Survey 5-year release (DES5yr; Abbott et al. 2024). The SALT fitting
algorithms fit the distance moduli, μ, using a modified version of the
Tripp formula:

BAO analysis into the timescape cosmology requires extraction
of the BAO from galaxy clustering statistics, which has already
been implemented (Heinesen et al. 2019). However, since the ratio
of baryonic matter to non-baryonic dark matter is different from
CDM, matter model calibrations in the early universe must also be
revisited.

μ = m∗B − MB + αx1 − βc,

We determine Bayes factors, B, using the standard Jeffrey’s scale
(Kass & Raftery 1995) for model comparison, whereby | ln B| < 1
indicates no statistical preference, 1 ≤ | ln B| < 3 moderate preference, while 3 ≤ | ln B| < 5 and | ln B| ≥ 5 represent strong and very
strong preference respectively. In this Letter, positive (negative) ln B
values indicate a preference for the timescape (spatially flat CDM)
model.
Bayesian statistics have already been implemented on SNe Ia data
for cosmological analysis, originally in the SDSS one-year sample
(Kessler et al. 2009; March et al. 2011) but later extended to the
Joint Light curve Analysis (Betoule et al. 2014) sample (Nielsen,
Guffanti & Sarkar 2016; Dam et al. 2017) and more recently in the
Pantheon+ (Brout et al. 2022a, b; Scolnic et al. 2022) data set (Lane
et al. 2024).
The previous studies implemented a Bayesian hierarchical likelihood construction in the form
N
∣ ]
∏ [
∣
ˆ ∗B , xˆ1 , cˆ)i ∣ H
L≡
Pr (m

(1)

which is determined using the bolometric flux. The luminosity
distance, dL , can be calculated using the redshift of the supernovae
and suitable cosmological model parameters. Typically, these are
M0 for the spatially flat CDM model and fv0 for the timescape
cosmology.2 Thus, the distance modulus constitutes the pillar of
cosmological model comparison via supernovae analysis.
As noted in Lane et al. (2024), we omit peculiar velocity
corrections. These are typically made using FLRW geometry assumptions, making it impossible to include them while preserving
model-independence, or to perform a fair comparison. However, as
distinctions between peculiar motion and expansion are central to the
further development of timescape, the inclusion of such corrections
will be addressed in future work. We would expect such corrections to
have a small impact for low-redshift data cuts and negligible impact
for zmin taken within a statistically homogeneous regime (Carr et al.
2022). Furthermore, for the same reasons we do not include other
cosmological model and metric-dependent bias corrections, such as
Malmquist biases. Such corrections are small and cannot drive any
substantial changes to the Bayes factors since the trend with redshift
is expected to be very similar3 in both CDM and timescape.
Lane et al. (2024) already presented moderate preference in favour
of the timescape model over CDM. A similar result was also
obtained by the DES team, with zmin = 0.033, using the Akaike
Information Criterion on the DES5yr supernovae sample (Camilleri
et al. 2024). They further noted a change from 12 AIC = −1.7 (in
favour of timescape) to 12 AIC = 6.3 (in favour of spatially flat
CDM), when SNe Ia data were combined with Baryonic Acoustic
Oscillation (BAO) measurements. However, the BAO analysis of
Camilleri et al. (2024) assumes purely geometric adjustments to the
standard FLRW pipeline, using a CDM calibration of the BAO drag
epoch, which is not the case in timescape. Incorporating detailed

1 For Pantheon+, Scolnic et al. (2022) adopt values of α = 0.148 and β =

3.112, respectively, for their nominal fit.
2 See Dam et al. (2017, appendix A) for detailed comparisons of luminosity
distance calculations in the timescape and FLRW models.
3 The principal small difference occurs in the geometric homogeneous
Eddington bias (McKay 2016), leading to the potential for future tests.

MNRASL 537, L55–L60 (2024)

i=1

=

N
∏∫

∣
[
]
∣
ˆ ∗B , xˆ1 , cˆ)i ∣ (MB , x1 , c)i , H
Pr (m

i=1

∣ ]
[
× Pr (MB , x1 , c)i ∣ H dMB dx1 dc,

(3)

where the quantities which are denoted with a hat are considered to
be observed values, the true values are the quantities not denoted
by a hat, and N is the number of supernovae observations. The true
data represents the intrinsic parameters utilised explicitly in the Tripp
(Tripp 1998) relation.
Nielsen et al. (2016), Dam et al. (2017), and Lane et al. (2024)
follow the analysis of March et al. (2011) and adopt global, independent Gaussian distributions for MB , x1 , and c to determine the
probability density of the true parameters. However, both of these
simplifying assumptions are ultimately flawed. Indeed, (i) the true
values of x1 and c are expected to be highly correlated as these are
effective parameters obtained by coarse-graining the highly complex
processes behind supernovae explosions; (ii) both the distributions
of x1 and c present strong non-Gaussian features that cannot be
explained away by systematics or biases in the data. Whilst the former
always represented an overly simplifying assumption, the latter was
a reasonable assumption when it was first implemented, however, the
vast increases in observed SNe Ia have shown the second assumption
to be flawed (Hinton et al. 2019).
To overcome the faulty assumptions of the previous analyses,
a full non-Gaussian modelling of the joint distribution for x1 and
c would be required. This represents non-trivial changes in the
likelihood construction and integration, which will be addressed
in future work (in prep.). Therefore, in this Letter, we propose an
alternative approach to sidestep the issue. Our new approach builds
upon the Bayesian hierarchical likelihood construction method by
directly seeding the priors of x1 and c with the inferred values from
the SALT2 fitting algorithm (Guy et al. 2005, 2007; Taylor et al.
2021). Specifically, we define the priors over the true values for each

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

where α and β are considered constant across all redshifts1 , x1 is the
time stretch/decay parameter, c is the colour, and mB and MB are
the apparent and absolute magnitude in the rest frame of the B band
filter. Rest-frame measurements are identical for theories obeying
the Strong Equivalence Principle of general relativity – in particular,
in both the FLRW and timescape models. In our analysis, x1 , c, and
mB are taken directly from the Pantheon+ data.
The observational distance modulus from equation (1) is then
compared with the theoretical distance modulus, given by
(
)
dL
μ ≡ 25 + 5 log10
(2)
,
Mpc

2 S TAT I S T I C A L A N A LY S I S

## PDF page 3

Evidence for fundamental change in cosmology
supernovae as
(
)
∣ ]
[
Pr (MB , x1 , c)i ∣ H = N MB |M̄B , σMB δ(x1 − xˆ1,i ) δ(c − cˆi ) ,

L57

Table 1. Bayesian and frequentist priors on parameters used in
the analysis. All priors are uniform on the respective intervals
and, importantly, relatively broad for both models to ensure fair
comparison.

(4)

where the distributional error matrix
( (D) is the
) block-diagonal matrix
with each block defined as diag σM2 B , 0, 0 i , d is the 3N × 3N
statistical and systematic covariance matrix given by Lane et al.
(2024, section 2), and the residual vector X is defined by
ˆ ∗B,1 − μ1 − MB,1 + α xˆ1,1 − β cˆ1 , 0, 0, ...,
X := [m
ˆ ∗B,N − μN − MB,N + α xˆ1,N − β cˆN , 0, 0]⊺ .
m

(6)

Similarly to Dam et al. (2017) and Lane et al. (2024) we utilize
a nested Bayesian sampler PyMultiNest (Buchner et al. 2014),
which interacts with the MultiNest (Feroz & Hobson 2008; Feroz,
Hobson & Bridges 2009; Feroz et al. 2019) code to compare the
spatially flat CDM and timescape models with a tolerance of 10−3
and nlive = 800 for nine parameters. We choose the same priors as
Lane et al. (2024, table B2 & section 3) summarized in Table 1.
Finally, in our analysis we reconstruct the zCMB by applying a
boost (Fixsen et al. 1996) to the Pantheon + heliocentric redshifts,
excluding peculiar velocity corrections. We then remove all supernovae with zCMB ≤ zmin for varying redshift cuts zmin and fit the
cosmological model to the remaining supernova events. This allows
us to examine how the Bayes factor, cosmological parameters, and
Tripp parameters vary across different redshift regimes.

Parameter
fv0
M0
α
β
x1
c
MB
σ2
MB

Priors
[0.500,0.799] (2σ bound)
[0.143,0.487] (2σ bound)
[0,1]
[0,7]
[−20,20]
[−20,20]
[−20.3,18.3]
log10 (σ ) [−10,4]

3 R E S U LT S
Results for the Bayes factor, cosmological and light-curve parameters
are shown in Fig. 1.
The Bayesian comparisons are best understood by splitting the
minimum redshift cutoff used into three regimes: (i) for 0 < zmin <
0.023 we find very strong to strong evidence on the Jeffrey’s
scale (Kass & Raftery 1995) in favour of timescape over CDM;
(ii) for 0.023 ≤ zmin < 0.054 we enter the calibration regime,4
finding moderate to no significant preference for timescape; (iii) for
zmin ≥ 0.075, beyond any measure of a SHS5 , we find exclusively
moderate preference for the timescape cosmology. Notably, the logevidence, ln Z, values found here for both models are ∼10–100×
greater compared to the previous analysis by Lane et al. (2024).
Since timescape’s uniform quasi-local Hubble expansion condition holds down to scales ∼ 4 – 15 Mpc, as we decrease zmin an
increase in the Bayesian evidence favouring timescape is expected
if the model accurately captures the average cosmic expansion deep
in the non-linear regime of structure formation. Beyond the SHS,
CDM of course provides an excellent description of our Universe.
However, the evidence in favour of timescape remains small but
modest (ln B > 1) at the highest redshift cuts, zmin ≥ 0.075, pointing
to the ability of the model to describe the Universe’s expansion
history on scales greater than the SHS. This moderate evidence
(ln B > 1) can be interpreted as resulting from the integrated effects
across the redshift range zmin < z < 2.26, reflecting the 1–3 per cent
variations in the expansion history between timescape and CDM.
In comparing two models with different assumptions in the nonlinear regime, the redshift distribution of the data becomes particularly important. For example, Lane et al. (2024) found consistent
weak preference in favour of timescape using the P+580 subsample
in which data from the full sample is truncated at high and low
redshifts. While the evidence for the P+1690 sample changes
significantly of order ln B ∼ 1.5 – 2.5 in our revised analysis, the
P+580 subsample result remains consistent (Fig. 2). The discrepancy
between the results of the full data set and the subsample suggest
the need for further analysis on how the redshift distribution of
supernovae, and the probed redshift range impact evidence for
cosmological models. The uncertainty in the Bayes factor, ∼0.014,

4 This is the regime beyond which average homogeneity and isotropy are

assumed to apply to all observations. Hogg et al. (2005); Scrimgeour et al.
(2012) take this range as ≳ 70–120 h−1 Mpc (corresponding to a redshift
range of approximately 0.023–0.04).
5 The Lane et al. (2024) value z
min = 0.075 is larger than other estimates and
thus gives a robust upper bound for the SHS.

MNRASL 537, L55–L60 (2024)

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

where N (MB |M̄B , σMB ) is a normal distribution with mean value
M̄B and variance σM2 , and δ is the Dirac delta distribution. Thus, the
B
prior distribution in MB is common to all the supernovae data, while
the priors in x1 and c are supernovae specific. Therefore, our new
approach sidesteps the problem of modelling the joint distribution,
only requiring five parameters (a cosmological parameter, α, β, MB ,
and σM2 ), by assuming that the SALT2 parameters represent the
B
‘true’ parameters, i.e. the most probable values for both x1 and c for
this version of the SALT model.
Equivalently, given a single-shot inference for any physical quantity, the best guess for its true value is precisely the one inferred
through the observational procedure. The assumption of being the
most probable value introduces a caveat that it may, however,
potentially overlook astrophysical systematics inherent in the SALT2
light-curve procedure.
Our approach here has essential differences from previous methodology (Nielsen et al. 2016; Dam et al. 2017; Lane et al. 2024),
and is not merely a change of priors. Earlier work assumed that all
supernovae are drawn from ideal independent Gaussian distributions
in stretch (x1 ) and in colour (c), with mean values and standard
deviations derived from the cosmological fit. In contrast, this study
does not assume any particular statistical distribution for x1 and c,
nor do we assume these parameters follow the same ideal distribution
across the supernova sample. Instead, x1 and c are treated as fixed,
with values provided by the SALT2 fit. Taylor et al. (2021) show
through simulations that SALT2 reliably recovers input supernova
parameters. To compare this method with the previous one, we use
the same data set as Lane et al. (2024).
Therefore, by now following the same procedure as in Lane et al.
(2024), we find the likelihood to be
[
]
[
]−1/2
1
L = (2π )−3/2 det D + d
exp − X ⊺ (D + d )−1 X , (5)
2

## PDF page 4

L58

A. Seifert et al.

Figure 3. The convergence of the αx1 light-curve parameter for the spatially
flat CDM model across various redshift cuts, where x1 is the median value
from the distribution. A power-law model has been fit to the data, and the
shaded band represents within 5 per cent of the median value within the
range 0.1 ≤ zmin < 0.14 indicating when the model converges. The vertical
0.007
dotted line represents the SHSα found at zmin = 0.054+
−0.012 . The power-law
uncertainty is smaller than the plotted line.

Figure 1. The Bayes factors and Bayesian Maximum Likelihood Estimate
(MLE) parameters for the fitting parameters across different redshift cuts,
with Bayes factor uncertainties too small to display in the plot. The top
plot shows the Bayes factors, where the upper section (ln B > 1) favours
timescape, the unshaded section favours neither hypothesis and the lower
section (ln B < −1) favours CDM. The following plots show the various
0.007
MLE parameter estimates, with values beyond SHSα = 0.054+
−0.012 indicated
by the dashed vertical line.

MNRASL 537, L55–L60 (2024)

is so small that it does not influence the Jeffrey’s scale classifications
or the conclusions drawn.
The Bayes factors and Bayesian Maximum Likelihood Estimate
(MLE) parameters for different redshift cuts are shown. The top panel
shows Bayes factors with blue indicating preference for timescape,
red for CDM, and white for neither. The subsequent plots show
MLE parameter estimates, with values beyond the scale of the
statistical homogeneity (SHS) marked by the dashed vertical line.
Lane et al. (2024) introduced an additional empirical data-driven
notion of statistical homogeneity, defining SHSα from a power law
fitted to the αx1 degenerate parameter. The analogous SHSβ defined
from βc does not yield a true convergence for the analysis by Lane
et al. (2024), nor for this analysis, due to Malmquist bias not being
accounted for. While the SHSβ appears to converge below zmin ≈
0.12, this is not the case for higher redshift cuts. For the reanalysis
0.007
presented in Fig. 3 we find SHSα = 0.054+
−0.012 , which is 1.2σ greater
than the maximum value of the SHS gathered from the two-point
galaxy correlation function (Hogg et al. 2005; Scrimgeour et al.
2012) and somewhat lower but within 2.3σ of the result Lane et al.

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

Figure 2. The difference in the Bayes factors for the full P+1690 sample
and the P+580 subsample between Lane et al. (2024) and our results. For
the subsample, the results from the new analysis presented here align very
well with the results by Lane et al. (2024), while for the full sample the new
analysis greatly increases the preference in favour of timescape.

## PDF page 5

Evidence for fundamental change in cosmology

We examined including this term but found that it does not affect the
Bayes factor conclusions, with an average offset of | ln B| = 0.077
compared to the uncorrected value. Furthermore, the statistical cost
of introducing additional free parameters can be assessed by the relative Bayesian Information Criterion (BIC) statistic (Schwarz 1978;
Kass & Raftery 1995) BIC = k ln N − 2 ln Z for k free parameters,
a sample size, N , and likelihood Z. We find that independent of
cosmology the model with a mass step is strongly disfavoured
relative to the uncorrected Tripp model, with BIC = −7.90 at
zmin = 0. Furthermore, there is no significant change in the value
of the cosmological parameter, with M0 ≈ 0.0016, which is well
6 The α and β

values reported by Scolnic et al. (2022) and Lane et al.
(2024) are derived at various stages of the cosmological fitting pipeline,
and are influenced by the specific subsample used (Lane et al. 2024). Any
slight differences in cosmological parameters can be attributed to these
methodological variations and to the omission of cosmology dependent bias
corrections.
7 The relative contributions of Hubble constant uncertainty and absolute
magnitude uncertainty, respectively δH and δM , propagate according
B
[
(
)2
]1 / 2 0
to σM = δ 2 + H 5ln 10 δ 2
. This makes the two contributions
B

MB

0

H0

impossible to unravel and explains the larger uncertainty, σM , relative to
uncertainties in other parameters from the fitting (see Fig. 1).

B

within the 1σ range of our statistical and systematic uncertainties.
Thus our final results are stated without galaxy host corrections.8
4 DISCUSSION AND CONCLUSIONS
We performed a new Bayesian statistical analysis on the Pantheon+
supernovae data set, accounting for the non-Gaussian x1 and c
features of the supernovae parameter distributions. The Bayesian
evidence yields very strong to strong evidence for the timescape
model in the low-redshift regime. This late-universe result could be
expected, as the timescape models accounts for non-kinematic differential expansion on scales z ≲ 0.03 where the local inhomogeneous
structure of our nearby cosmic web most impacts measurements.
On the other hand, for samples strongly weighted by SNe Ia in the
calibration regime of the CDM model (zCMB ≈ 0.04) there is no
significant preference either way, the two models being statistically
equivalent. With a restriction to higher redshifts, well beyond any
scale of statistical homogeneity generally accepted (Lane et al. 2024),
Bayesian evidence is driven once again in favour of timescape.
Our new analysis makes fewer assumptions about any particular
statistical distribution of the data. Specifically, the likelihood function
is constructed directly from the x1 and c values obtained using
the SALT2 algorithm – values employed in most SNe Ia analyses.
The empirical SNe Ia data obtained via the cosmology independent
SALT2 fit strongly favours the timescape model over CDM.
Any astrophysical or environmental biases would likely impact
both cosmological models. Thus the strong preference for timescape
would require an extremely subtle combination of such biases for this
to be its prime cause. The largest systematic error in the Pantheon+
analysis is the standardization of the heterogeneous mix of low-z
sample light curves (Abbott et al. 2024; Lane et al. 2024). Future
improvements with the new DES5yr sample (Abbott et al. 2024)
will allow for a more homogeneous and careful selection of the
low-z sample. However, in this Letter we concentrate on the impact
of the new statistical method on cosmological model selection, and
therefore we use the same data as Lane et al. (2024).
Since timescape has the same number of free parameters as
spatially flat CDM, Bayesian evidence offers the best comparison.
To expand our results to include other popular FLRW-type alternative
cosmological models, which contain more parameters, e.g. wCDM,
we determine the BIC statistic (Schwarz 1978; Kass & Raftery
1995) for fair model comparison. For the full sample, we find that
relative to timescape CDM models with FLRW curvature are very
strongly disfavoured with BIC = −13.39, while wCDM is also
very strongly disfavoured with BIC = −11.70.
The results presented in this Letter indicate that the timescape
cosmology is not only a viable contender to the CDM framework,
but may also provide new insights to the astrophysics of modelling
SNe Ia. Timescape’s non-FLRW average evolution reveals degeneracies between cosmological parameters and empirical SNe Ia model
parameters that were already partly uncovered in earlier work (Dam
et al. 2017) but which are striking with Pantheon+, as shown by
Lane et al. (2024) and the present Letter.
8 A further reason for not including galaxy-host corrections is the observation

that the γ parameter exhibits inconsistent behaviour across different redshift
cuts for a simple mass-step function. This inconsistency most likely arises
from the heterogeneous subsamples of low-z data, as γ is well constrained
in a more statistically homogeneous sample. It is possible, but less likely,
that these fluctuations arise from other astrophysical factors explored by the
DES5yr team and recent studies (Dixon et al. 2024), but these are beyond the
scope of this Letter.

MNRASL 537, L55–L60 (2024)

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

(2024) determined. The differences with respect to the analysis in
Lane et al. (2024) derive from the lifting of the Gaussian assumption
of the underlying distributions of x1 and c.
The Bayesian analysis can be used to find the MLE of the
parameters, including the single free cosmological parameter. For
zmin cuts beyond the SHSα , (zmin ≥ 0.055), for CDM we find
M0 = 0.377 ± 0.021, within 1.2σ of the value found from the
DES5yr release (Abbott et al. 2024), and just outside of 2σ of
Pantheon+ (Brout et al. 2022a).6
In the case of timescape, we find a void fraction of, fv0 = 0.737 ±
0.029, within 2σ of the Camilleri et al. (2024) DES5yr value. Significantly, our fv0 value is also within 2σ of independent values predicted
0.041
from the Planck CMB power spectrum, fv0 = 0.695+
−0.051 (Duley,
Nazer & Wiltshire 2013); and well within 1σ of strong gravitational
lensing distance ratios, fv0 = 0.736 ± 0.099, (Harvey-Hawes &
Wiltshire 2024). We also find the evolution of the Tripp constants, α,
β, and MB with varying zmin cuts following Dam et al. (2017), Lane
et al. (2024). To avoid the underlying degeneracy between H0 and
MB , we fix H0 for both models as a nuisance parameter.7 Moreover,
although the values for the individual parameters differ between the
two statistical methods, the Tripp distance modulus, μ, changes on
average by only |(−MB + αx1 − βc)|CDM = 0.030 ± 0.019 for
redshift cuts beyond zmin = 0.054. This variation is observed when
comparing the median values of x1 and c in the Tripp methodology,
to the general Gaussian distribution fit values.
The change in μ between this work and Lane et al. (2024) is thus
not statistically significant in this regime. However, it is expected
that differences in the prior distribution cause differences in the
fitted parameters. This behaviour will be investigated further for
supernovae statistics built on skewed, non-Gaussian distributions in
future work (in prep.).
In the beams with Bias Correction method (Kessler & Scolnic
2017) a galaxy host correction is introduced with an additional
parameter, γ , defined by the mass-step
{
γ /2
if MGalaxy ≥ 1010 M⊙
γ GHost = δG.Host =
(7)
−γ /2 if MGalaxy < 1010 M⊙ .

L59

## PDF page 6

L60

A. Seifert et al.

AC K N OW L E D G E M E N T S
DLW, RRH, and ZGL are supported by the Marsden Fund administered by the Royal Society of New Zealand, Te Apārangi under grants
M1271 and M1255. RRH is also supported by Rutherford Foundation
Postdoctoral Fellowship RFT-UOC2203-PD. We are indebted to
the anonymous referee of Lane et al. (2024) for suggesting the
analysis framework. We also thank the anonymous referee of this
Letter for their constructive and insightful comments. We thank all
members of the University of Canterbury Gravity and Cosmology and
Astrophysics groups for stimulating discussions, particularly: John
Forbes, Christopher Harvey-Hawes, Morag Hills, Emma Johnson,
Shreyas Tiruvaskar, Michael Williams, and Manon van Zyl. Finally,
we wish to thank Elena Moltchanova for her precious insights into
the statistical methods employed.
DATA AVA I L A B I L I T Y
A complete set of the codes and details used for our analysis and how
to use them can be found at Seifert & Lane (2023), and the covariance
and input files are made available at Lane & Seifert (2024).
REFERENCES
Abbott T. M. C. et al., 2024, ApJ, 973, L14
Adame A. G. et al., 2024, preprint (arXiv:2404.03002)
Aluri P. K. et al., 2023, Class. Quantum Gravity, 40, 094001
Betoule M. et al., 2014, A&A, 568, A22
Brout D. et al., 2022a, ApJ, 938, 110
Brout D. et al., 2022b, ApJ, 938, 111
Buchert T., 2000, Gen. Relativ. Gravit., 32, 105
Buchert T., 2001, Gen. Relativ. Gravit., 33, 1381
Buchert T., Mourier P., Roy X., 2020, Gen. Relativ. Gravit., 52, 27
Buchner J. et al., 2014, A&A, 564, A125
Camilleri R. et al., 2024, MNRAS, 533, 2615
Carr A., Davis T. M., Scolnic D., Said K., Brout D., Peterson E. R., Kessler
R., 2022, Publ. Astron. Soc. Aust., 39, e046

Dam L. H., Heinesen A., Wiltshire D. L., 2017, MNRAS, 472, 835
Di Valentino E. et al., 2021, Class. Quantum Gravity, 38, 153001
Dixon M. et al., 2024, preprint (arXiv:2408.01001)
Duley J. A. G., Nazer M. A., Wiltshire D. L., 2013, Class. Quantum Gravity,
30, 175006
Feroz F., Hobson M. P., 2008, MNRAS, 384, 449
Feroz F., Hobson M. P., Bridges M., 2009, MNRAS, 398, 1601
Feroz F., Hobson M. P., Cameron E., Pettitt A. N., 2019, Open J. Astrophys.,
2, 1
Fixsen D. J., Cheng E. S., Gales J. M., Mather J. C., Shafer R. A., Wright E.
L., 1996, ApJ, 473, 576
Galoppo M., Wiltshire D. L., 2024, preprint (arXiv:2406.14157)
Galoppo M., Re F., Wiltshire D. L., 2024, preprint (arXiv:2408.00385)
Guy J., Astier P., Nobili S., Regnault N., Pain R., 2005, A&A, 443, 781
Guy J. et al., 2007, A&A, 466, 11
Harvey-Hawes C., Wiltshire D. L., 2024, MNRAS, 534, 3364
Heinesen A., Blake C., Li Y.-Z., Wiltshire D. L., 2019, J. Cosmol. Astropart.
Phys., 03, 003
Hinton S. R. et al., 2019, ApJ, 876, 15
Hogg D. W., Eisenstein D. J., Blanton M. R., Bahcall N. A., Brinkmann J.,
Gunn J. E., Schneider D. P., 2005, ApJ, 624, 54
Kass R. E., Raftery A. E., 1995, J. Am. Stat. Assoc., 90, 773
Kenworthy W. D. et al., 2021, ApJ, 923, 265
Kessler R., Scolnic D., 2017, ApJ, 836, 56
Kessler R. et al., 2009, ApJS, 185, 32
Lane Z. G., Seifert A., 2024, P+1690 Covariance Matrix, Zenodo. Available
at: https://doi.org/10.5281/zenodo.12729746
Lane Z. G., Seifert A., Ridden-Harper R., Wiltshire D. L., 2024, MNRAS,
536, 1752
McKay J. H., 2016, MSc thesis, Univ. Canterbury
March M. C., Trotta R., Berkes P., Starkman G. D., Vaudrevange P. M., 2011,
MNRAS, 418, 2308
Nielsen J. T., Guffanti A., Sarkar S., 2016, Sci. Rep., 6, 35596
Peebles P. J. E., 2022, Ann. Phys., 447, 169159
Perlmutter S. et al., 1999, ApJ, 517, 565
Riess A. G. et al., 1998, AJ, 116, 1009
Schwarz G., 1978, Ann. Stat., 6, 461
Scolnic D. et al., 2022, ApJ, 938, 113
Scrimgeour M. I. et al., 2012, MNRAS, 425, 116
Seifert A., Lane Z. G., 2023, Code for Supernova Analysis with Pantheon+ by
Lane et al. 2023, GitHub. Available at: https://github.com/antosft/SNe-P
antheonPlus-Analysis
Taylor G., Lidman C., Tucker B. E., Brout D., Hinton S. R., Kessler R., 2021,
MNRAS, 504, 4111
Tripp R., 1998, A&A, 331, 815
Williams M. J., Macpherson H. J., Wiltshire D. L., Stevens C., 2024, preprint
(arXiv:2403.15134)
Wiltshire D. L., 2007a, New J. Phys., 9, 377
Wiltshire D. L., 2007b, Phys. Rev. Lett., 99, 251101
Wiltshire D. L., 2008, Phys. Rev. D, 78, 084032
Wiltshire D. L., 2009, Phys. Rev. D, 80, 123512
Wiltshire D. L., 2014, in Perez Bergliaffa S., Novello M., eds, Proceedings
of the XVth Brazilian School of Cosmology and Gravitation. Cambridge
Scientific Publishers, Cambridge, UK, p. 203

This paper has been typeset from a TEX/LATEX file prepared by the author.

© 2024 The Author(s).
Published by Oxford University Press on behalf of Royal Astronomical Society. This is an Open Access article distributed under the terms of the Creative Commons Attribution License
(https://creativecommons.org/licenses/by/4.0/), which permits unrestricted reuse, distribution, and reproduction in any medium, provided the original work is properly cited.

MNRASL 537, L55–L60 (2024)

Downloaded from https://academic.oup.com/mnrasl/article/537/1/L55/7926647 by guest on 02 January 2025

Regardless of what model cosmology is to be the standard
in future, exploring more than one model is important. Indeed,
the timescape framework is consistent with new analysis of void
statistics in numerical relativity simulations using the full Einstein
equations (Williams et al. 2024). These are consistent with an
emerging kinetic spatial curvature of voids on small scales. Much
remains to be done in calibrating the dark matter fraction, primordial
sound speed and the BAO scale. However, new results are likely
to provide a robust framework for this (Galoppo & Wiltshire 2024;
Galoppo, Re & Wiltshire 2024).
Our results imply profound consequences for cosmology and
astrophysics. Indeed, a net preference for the timescape cosmology
over the standard FLRW cosmologies may point to a need for revision
of the foundations of theoretical cosmology, both ontologically and
epistemologically, to better understand inhomogeneities and their
backreaction on the average evolution of the Universe.
