Source: https://arxiv.org/abs/2406.09971v2
PDF sha256: 60f504e38160ee835098e5033865c370798e29b5031dc56f2b8fbc5cfe5a7277
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of atlas_2024_hh_combination.pdf

Transcription of `atlas_2024_hh_combination.pdf` in this directory, 32 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-32 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANISATION FOR NUCLEAR RESEARCH (CERN)

arXiv:2406.09971v2 [hep-ex] 6 Sep 2024

Phys. Rev. Lett. 133 (2024) 101801
DOI: 10.1103/PhysRevLett.133.101801

CERN-EP-2024-160
September 9, 2024

Combination of Searches for√Higgs Boson Pair
Production in 𝒑 𝒑 Collisions at 𝒔 = 13 TeV with the
ATLAS Detector
ATLAS Collaboration

This Letter presents results from a combination of searches for Higgs boson pair production
√
using 126–140 fb−1 of proton-proton collision data at 𝑠 = 13 TeV recorded with the ATLAS
detector. At 95% confidence level (CL), the upper limit on the production rate is 2.9 times the
standard model (SM) prediction, with an expected limit of 2.4 assuming no Higgs boson pair
production. Constraints on the Higgs boson self-coupling modifier 𝜅 𝜆 = 𝜆 𝐻 𝐻 𝐻 /𝜆SM
𝐻 𝐻 𝐻 , and
the quartic 𝐻𝐻𝑉𝑉 coupling modifier 𝜅 2𝑉 = 𝑔 𝐻 𝐻𝑉𝑉 /𝑔 SM
,
are
derived
individually,
fixing
𝐻 𝐻𝑉𝑉
the other parameter to its SM value. The observed 95% CL intervals are −1.2 < 𝜅 𝜆 < 7.2
and 0.6 < 𝜅 2𝑉 < 1.5, respectively, while the expected intervals are −1.6 < 𝜅 𝜆 < 7.2 and
0.4 < 𝜅2𝑉 < 1.6 in the SM case. Constraints obtained for several interaction parameters
within Higgs effective field theory are the strongest to date, offering insights into potential
deviations from SM predictions.

© 2024 CERN for the benefit of the ATLAS Collaboration.
Reproduction of this article or parts of it is allowed as specified in the CC-BY-4.0 license.

## PDF page 2

Since the discovery of the Higgs boson (𝐻) by the ATLAS and CMS Collaborations at the Large Hadron
Collider (LHC) in 2012 [1, 2], understanding its intrinsic properties and interactions has been a priority.
The Higgs self-coupling is directly related to the shape of the Higgs scalar field potential, which is important
for understanding the mechanism of electroweak symmetry breaking and serves as an essential test of the
electroweak theory. After the symmetry breaking, the Higgs potential predicted in the standard model (SM)
can be expanded in the Higgs boson field 𝐻 near its minimum: 𝑉 (𝐻) = 12 𝑚 2𝐻 𝐻 2 + 𝜆 𝐻 𝐻 𝐻 𝑣𝐻 3 + O (𝐻 4 ),
where 𝑚 𝐻 is the Higgs boson mass and 𝑣 ≈ 246 GeV is the field’s vacuum expectation value [3]. The Higgs
SM
2
2
boson’s trilinear self-coupling 𝜆SM
𝐻 𝐻 𝐻 is equal to 𝑚 𝐻 /2𝑣 , its coupling 𝑔 𝐻𝑉𝑉 to vector bosons (𝑉 = 𝑊, 𝑍)
2 /𝑣, and its coupling 𝑔 SM to fermions is equal to 𝑚 /𝑣. The quartic coupling between two
is equal to 2𝑚 𝑉
𝑓
𝐻 𝑓 𝑓¯
SM
Higgs bosons and two vector bosons, 𝑔 SM
𝐻 𝐻𝑉𝑉 , is equal to 𝑔 𝐻𝑉𝑉 /𝑣 [3]. The production of Higgs boson pairs
(𝐻𝐻) via gluon-gluon fusion (ggF) and vector-boson fusion (VBF) provides a direct probe of 𝜆 𝐻 𝐻 𝐻 and
𝑔 𝐻 𝐻𝑉𝑉 , which affects the pair-production differential cross section at tree level. Observed (expected) 95%
confidence level (CL) upper limits on the 𝐻𝐻 production cross section have been set at 2.4 (2.9) and 3.4
(2.5) times the SM prediction by previous ATLAS [4] and CMS [5] search combinations, respectively.

Deviations from the SM can be expressed in terms of coupling modifiers 𝜅 𝑖 [6, 7] or Wilson coefficients 𝑐 𝑖
in the Higgs effective field theory (HEFT) [8, 9], as illustrated in Fig. 1. In the 𝜅 framework, the coupling
modifiers 𝜅𝜆 , 𝜅 𝑡 , 𝜅 𝑉 , and 𝜅 2𝑉 are each defined as the ratio of the Higgs boson coupling to its SM value,
e.g., 𝜅 𝜆 = 𝜆 𝐻 𝐻 𝐻 /𝜆SM
𝐻 𝐻 𝐻 . In the HEFT framework, new physics in the electroweak sector is described
through anomalous couplings of the Higgs boson. The organization of the HEFT Lagrangian is guided by
chiral perturbation theory, with the low-energy dynamics of electroweak symmetry breaking described
using a nonlinear realization of the gauge symmetry group SU(2) 𝐿 × U(1)𝑌 . One advantage of the HEFT
framework is that the anomalous single-Higgs-boson and 𝐻𝐻 couplings are defined separately, allowing
simplified 𝐻𝐻 interpretations. In the HEFT Lagrangian, ggF 𝐻𝐻 production is described at leading order
by five relevant operators, and their associated Wilson coefficients are 𝑐 𝑡𝑡 ℎ , 𝑐 𝑔𝑔ℎ , 𝑐 ℎℎℎ , 𝑐 𝑔𝑔ℎℎ , and 𝑐 𝑡𝑡 ℎℎ .
In this formalism, 𝑐 𝑡𝑡 ℎ and 𝑐 ℎℎℎ are equivalent to 𝜅 𝑡 and 𝜅𝜆 . In this analysis, 𝜅 𝑉 , 𝜅 𝑡 (𝑐 𝑡𝑡 ℎ ), and 𝑐 𝑔𝑔ℎ are
set equal to the SM predictions, because those parameters are constrained by precise measurements of
single-Higgs-boson production [5, 10].
In the SM, destructive interference between the ggF 𝐻𝐻 production diagrams in Figs. 1(a) and 1(b) makes
√
softer Higgs bosons more sensitive for constraining 𝜅 𝜆 . For 𝑚 𝐻 = 125 GeV and 𝑠 = 13 TeV proton-proton
SM (𝐻𝐻) = 31.1 +1.9 (scale + 𝑚 ) ± 0.9 (PDF + 𝛼 ) fb [11–18]
collisions, the predicted cross section is 𝜎ggF
top
s
−7.1
at next-to-next-to-leading order in 𝛼s and including and including an uncertainty related to the choice of the
virtual top-quark mass scheme [18]. The “PDF + 𝛼s ” uncertainty accounts for uncertainties in the parton
distribution functions and strong coupling constant, the “scale” uncertainty is due to the finite order of
quantum chromodynamics (QCD) calculations, and the “𝑚 top ” uncertainty is related to the top-quark mass
scheme. For SM VBF 𝐻𝐻 production, divergences in the diagrams shown in Figs. 1(d) and 1(e) cancel out
due to perturbative unitarity. If 𝜅 2𝑉 deviates from the SM prediction, this cancellation no longer occurs,
leading to a linear dependence of the cross section on the effective center-of-mass energy of the incoming
vector bosons [19]. Consequently, the Higgs bosons are expected to be more energetic in non-SM scenarios.
SM (𝐻𝐻) = 1.73 ± 0.04 fb at next-to-next-to-next-to-leading
The cross section for VBF 𝐻𝐻 production is 𝜎VBF
order in QCD [20–24].
¯ 𝑏¯ [25, 26], 𝑏 𝑏𝜏
¯ + 𝜏 − [27], 𝑏 𝑏𝛾𝛾
¯
This Letter presents a combination of results from the 𝑏 𝑏𝑏
[28], multilepton [29], and 𝑏 ¯𝑏ℓℓ + 𝐸 Tmiss [30] decay channels, probing more than half of the 𝐻𝐻 decays. The first three
analyses have been improved since the previous combination [4], and the other two are newly included.
The 𝐻𝐻 → 𝑏 ¯𝑏𝑏 𝑏¯ decay mode has the advantage of having the largest SM 𝐻𝐻 decay branching fraction
(33.9%), but it also has the largest SM background, due to the abundance of QCD multĳet events. Given its

2

## PDF page 3

g

H

g

H

g

κt (ctth )

H

H

κt
κλ
(ctth ) (chhh )

g

κt (ctth )

(a)

q

(b)

q

κV

V

κλ

q

q

H

V

H

V

H

κ2V

q

V

H

H

κV

V

H

q

H

H

V

κV
q

q

q

q

(c)

(d)

g

H

cggh

q

g

q
(e)

H

g

H

ctthh

cgghh

chhh
H

g

H

(f)

g

H

(g)

g

H

(h)

Figure 1: Leading-order Feynman diagrams showing the production of Higgs boson pairs via the ggF (a), (b), (f)–(h)
and VBF (c)–(e) processes. Each diagram is sensitive to specific coupling factors, denoted by 𝜅 𝑖 in the 𝜅 framework or
𝑐 𝑖 in the HEFT. Diagrams (a)–(e) occur in the SM predictions, while diagrams (f)–(h) manifest only when deviations
from the SM predictions are present in the coefficients 𝑐 𝑔𝑔ℎ , 𝑐 𝑔𝑔ℎℎ , or 𝑐 𝑡𝑡 ℎℎ .

capability to probe relatively high-energy Higgs bosons, both the resolved [25] and boosted topologies [26]
¯ + 𝜏 − decay mode has one of the larger
are now used to reconstruct the Higgs bosons. The 𝐻𝐻 → 𝑏 𝑏𝜏
branching fractions (7.3%) among the investigated 𝐻𝐻 decay channels and benefits from having only
moderate background contamination. In the corresponding search [27], one of the 𝜏 leptons is required
to decay hadronically, ensuring orthogonality with the 𝑏 ¯𝑏ℓℓ + 𝐸 Tmiss search. Although the 𝐻𝐻 → 𝑏 ¯𝑏𝛾𝛾
decay mode has a small branching fraction (0.26%), it has high trigger efficiency and a clean experimental
¯ + 𝜏 − [27] and 𝑏 𝑏𝛾𝛾
¯
signature. The 𝑏 𝑏𝜏
[28] analyses have been improved through optimized classification
of selected events to enhance the sensitivity to the Higgs boson couplings. Furthermore, the 𝑏 ¯𝑏𝜏 + 𝜏 −
analysis now benefits from more accurate background modeling and larger samples of simulated events.
The multilepton analysis is designed to select 𝐻𝐻 events in 𝑏 ¯𝑏𝑍 𝑍 ∗ , 𝑉𝑉 ∗𝑉𝑉 ∗ (𝑉 = 𝑊 or 𝑍), 𝑉𝑉 ∗ 𝜏 + 𝜏 − ,
𝜏 + 𝜏 − 𝜏 + 𝜏 − , 𝛾𝛾𝑉𝑉 ∗ , and 𝛾𝛾𝜏 + 𝜏 − decay channels with leptons in the final states; the total branching fraction
¯ + 𝐸 miss search targets final states arising from 𝐻𝐻 decay channels where one of
is around 6.5%. The 𝑏 𝑏ℓℓ
T
the Higgs bosons decays to a 𝑏-quark pair and the other to either a boson pair (𝑍 𝑍 ∗ , 𝑊𝑊 ∗ ) or a 𝜏-lepton
pair, which then decays to a pair of opposite-sign leptons (ℓ = 𝑒, 𝜇) and neutrinos, for a total branching
fraction of 2.9%. Depending on the analysis, the final discriminating variable can be the 𝐻𝐻 invariant mass,
the diphoton invariant mass, or the multivariate classifiers used to separate signal from background.

3

## PDF page 4

√
The analyses under consideration use the full sample of 𝑠 = 13 TeV proton-proton (𝑝 𝑝) collision data
recorded with the ATLAS detector during run 2 of the LHC. The integrated luminosity ranges from
126 to 140 fb−1 depending on the trigger selection [31]. The ATLAS experiment is a multipurpose
particle detector with a forward-backward symmetric cylindrical geometry and nearly 4𝜋 coverage in solid
angle [32–34]. A software suite [35] is used in data simulation, in the reconstruction and analysis of real
and simulated data, in detector operations, and in the trigger and data acquisition systems of the experiment.
The searches use a common set of event generators to describe ggF and VBF 𝐻𝐻 production in the 𝑝 𝑝
collisions. Reweighting methods are used to estimate the total and differential signal yields at a given value
of 𝜅 𝑖 from samples simulated for different values of 𝜅 𝜆 and 𝜅2𝑉 [4] or to estimate the particle-level 𝑚 𝐻 𝐻
distributions for alternative values of the Wilson coefficients using parameters from Ref. [36].
The results are derived from a likelihood function 𝐿(𝜶, 𝜽), where 𝜶 denotes the vector of parameters of
interest (POIs) in the statistical model and 𝜽 is a set of nuisance parameters (NPs), including systematic
uncertainty contributions and background parameters. This global likelihood function is the product
(
) of
individual search likelihoods. The profile-likelihood-ratio test statistic −2 ln Λ(𝜶, 𝜽) = −2 ln

𝐿 𝜶,𝜽ˆˆ (𝜶)
𝐿( ˆ
𝜶,𝜽ˆ)

is

used to determine the 68% and 95% CL intervals and local significance in the asymptotic approximation [37].
The CLs method [38] is utilized to derive upper limits on the 𝐻𝐻 production cross section. To evaluate the
expected limits, Asimov datasets [37] are generated, setting all NPs to their best-fit values in data and fixing
the POIs to those posited in the hypothesis under test. The event samples from the combined searches are
scrutinized for overlaps in both real and simulated data; they are found to be less than 1% in the signal
regions, and, thus, considered negligible.
Complete discussions of the systematic uncertainties considered in the individual searches are provided in
Refs. [25–30]. Correlations of these uncertainties between different searches are investigated. Uncertainties
related to the data-taking conditions, such as those associated with the integrated luminosity and the
mismodeling of the multiple 𝑝 𝑝 interactions per bunch crossing, are assumed to be correlated across the
¯ 𝑏¯ analysis [25], which
searches. An exception is the integrated luminosity uncertainty in the resolved 𝑏 𝑏𝑏
employs a different calibration version. Where applicable, uncertainties associated with physics objects
common to two or more searches are considered correlated. Correlations are also assumed for theoretical
uncertainties affecting simulated signal and background processes, such as uncertainties in the QCD scale,
proton parton distribution functions, and Higgs boson decay branching fractions. Systematic uncertainties
that significantly influence the individual searches but are strongly constrained or pulled in the data fitting
are treated as uncorrelated to prevent undue influence on the other searches. However, the impact of
treating them as correlated or uncorrelated in the combination was checked and found to be negligible.
The signal strength 𝜇 𝐻 𝐻 is defined as the ratio of the measured inclusive ggF and VBF 𝐻𝐻 production
SM
+2.1
cross section to the SM prediction 𝜎ggF
+ VBF (𝐻𝐻) = 32.8 −7.2 fb. This 𝜇 𝐻 𝐻 measure assumes that
the relative ggF and VBF production cross sections, Higgs boson decay branching fractions, and
relative kinematic distributions correspond to the SM predictions. The fit to data indicates a value of
+1.2 = 0.5 +0.9 (stat) +0.7 (syst), where “stat” and “syst” denote the statistical and systematic
𝜇 𝐻 𝐻 = 0.5−1.0
−0.8
−0.6
uncertainties, respectively. The result is compatible with the SM prediction, with a 𝑝 value of 0.64. Assuming
+1.0
+0.7
SM
+1.2
𝜎ggF + VBF (𝐻𝐻) = 𝜎ggF
+ VBF (𝐻𝐻), the expected value is 𝜇 𝐻 𝐻 = 1.0 −1.0 = 1.0 −0.9 (stat) −0.5 (syst). The
primary systematic uncertainty arises from an estimated uncertainty of 100% in modeling the radiation
of additional heavy-flavor jets in the ggF single-Higgs-boson background production process [39–43],
affecting 𝜇 𝐻 𝐻 by 25%. The observed (expected) significance of 𝜇 𝐻 𝐻 is 0.4 (1.0) standard deviations, with
respect to the hypothesis of no 𝐻𝐻 production. No significant 𝐻𝐻 signal is observed above the expected
background, and a 95% CL upper limit of 2.9 is placed on 𝜇 𝐻 𝐻 . If 𝐻𝐻 production is absent, the expected

4

## PDF page 5

ATLAS
s = 13 TeV, 126 140 fb 1
HH) = 32.8 fb

SM
ggF + VBF(

Observed limit (95% CL)
Expected limit (95% CL)
( HH = 0 hypothesis)
Expected limit ±1
Expected limit ±2

Obs.

Exp.

bb + ETmiss

10

14

Multilepton

17

11

bbbb

5.3

8.1

bb

4.0

5.0

bb +

5.9

3.3

Combined

2.9

2.4

0

5

10

15

20

25

30

35

40

95% CL upper limit on HH signal strength HH

Figure 2: Observed and expected 95% CL upper limits on the signal strength for inclusive ggF 𝐻𝐻 and VBF
¯ + 𝜏 − , 𝑏 𝑏𝛾𝛾,
¯
¯ 𝑏,
¯ multilepton and 𝑏 𝑏ℓℓ
¯ + 𝐸 miss decay channels and their statistical
𝐻𝐻 production from the 𝑏 𝑏𝜏
𝑏 𝑏𝑏
T
combination. The predicted SM cross section assumes 𝑚 𝐻 = 125 GeV. The expected limit, along with its associated
±1𝜎 and ±2𝜎 bands, is calculated for the assumption of no 𝐻𝐻 production and with all NPs profiled to the observed
data.

95% CL upper limit is 2.4, and in the SM case (𝜇 𝐻 𝐻 = 1) the expected upper limit is 3.4. The expected
¯ +𝜏−,
upper limit is 17% lower than in the previous combination [4]: 13% from improvements in the 𝑏 𝑏𝜏
𝑏 ¯𝑏𝛾𝛾 and 𝑏 ¯𝑏𝑏 𝑏¯ analyses and an additional 4% from the inclusion of the multilepton and 𝑏 ¯𝑏ℓℓ + 𝐸 Tmiss
channels. This combination provides the best expected sensitivity to the 𝐻𝐻 production cross section to
date. Figure 2 displays the limits from the individual searches and their combination [44] highlighting the
𝑏 ¯𝑏𝜏 + 𝜏 − channel as the one expected to constrain 𝜇 𝐻 𝐻 the most. The 𝑝 value for compatibility between
the 𝜇 𝐻 𝐻 value measured in the combination and those measured in the individual searches is 0.16. The
observed and expected 95% CL upper limits on 𝜎ggF + VBF (𝐻𝐻) from the combination are 86 and 71 fb,
respectively, derived in this case excluding theoretical uncertainties in the 𝐻𝐻 production cross section.
The self-coupling modifier 𝜅𝜆 is explored in the ggF and VBF 𝐻𝐻 production processes. The impact of 𝜅 𝜆
on the single-Higgs-boson background productions and the Higgs decay widths is neglected. Assuming
+2.1 , which
that other Higgs boson couplings conform to the SM predictions, a fit to data yields 𝜅 𝜆 = 3.8−3.6
+4.7
is compatible with the SM prediction, with a 𝑝 value of 0.53. The expected value of 𝜅 𝜆 is 1.0−1.5
when assuming SM 𝐻𝐻 production. The observed (expected) 95% CL interval is −1.2 < 𝜅𝜆 < 7.2
(−1.6 < 𝜅𝜆 < 7.2), representing the best expected sensitivity to the Higgs boson self-coupling to date.
The values of the test statistic as a function of 𝜅 𝜆 are shown in Fig. 3(a) for both the individual searches
and their combination, highlighting the 𝑏 ¯𝑏𝛾𝛾 channel as the most sensitive. Similarly, 𝜅 2𝑉 is explored
in the VBF 𝐻𝐻 production process. Assuming the SM predictions for other Higgs boson couplings, the
+0.22 (𝜅
+0.40
observed (expected) value is 𝜅2𝑉 = 1.02−0.23
2𝑉 = 1.00 −0.36 ). The observed (expected) 95% CL interval
is 0.6 < 𝜅 2𝑉 < 1.5 (0.4 < 𝜅 2𝑉 < 1.6). The values of the test statistic as a function of 𝜅 2𝑉 are shown in
¯ 𝑏¯ analysis as the most sensitive, mainly due to the boosted channel [26]. A
Fig. 3(b), highlighting the 𝑏 𝑏𝑏
deficit of data events in this channel results in stronger constraints on 𝜅 2𝑉 than expected. To reduce model
dependence, two-dimensional contours of −2 ln Λ in the 𝜅 2𝑉 –𝜅𝜆 plane are presented in Fig. 3(c). The 𝑝
value for compatibility of the combined measurement and the SM prediction is 0.78.

5

## PDF page 6

¯ + 𝜏 − , 𝑏 𝑏𝛾𝛾,
¯
¯ 𝑏,
¯ are
For the HEFT interpretation the three most sensitive 𝐻𝐻 decay channels, 𝑏 𝑏𝜏
and 𝑏 𝑏𝑏
combined. The VBF 𝐻𝐻 process is ignored, since it is sensitive only to 𝑐 ℎℎℎ and the predictions for this
Wilson coefficient are not available for this process. One-dimensional constraints are evaluated separately
for the coefficients 𝑐 𝑔𝑔ℎℎ and 𝑐 𝑡𝑡 ℎℎ , with all other coefficients fixed to the SM predictions. At 95% CL, the
observed interval on 𝑐 𝑔𝑔ℎℎ is −0.38 < 𝑐 𝑔𝑔ℎℎ < 0.49; if the SM value 𝑐 𝑔𝑔ℎℎ = 0 is assumed, the expected
95% CL interval is −0.36 < 𝑐 𝑔𝑔ℎℎ < 0.36. Similarly, the observed (expected) 95% CL interval on 𝑐 𝑡𝑡 ℎℎ is
−0.19 < 𝑐 𝑡𝑡 ℎℎ < 0.70 (−0.27 < 𝑐 𝑡𝑡 ℎℎ < 0.66). These represent the most stringent constraints to date on
𝑐 𝑔𝑔ℎℎ and 𝑐 𝑡𝑡 ℎℎ . The results are compatible with the SM predictions, with 𝑝 values of 0.087 and 0.16,
respectively. Figure 4 displays the two-dimensional test-statistic contours in the coefficient spaces of
(𝑐 𝑔𝑔ℎℎ , 𝑐 ℎℎℎ ), (𝑐 𝑡𝑡 ℎℎ , 𝑐 ℎℎℎ ), and (𝑐 𝑔𝑔ℎℎ , 𝑐 𝑡𝑡 ℎℎ ), with each plot fixing 𝑐 𝑡𝑡 ℎℎ , 𝑐 𝑔𝑔ℎℎ , or 𝑐 ℎℎℎ , respectively, to
its SM value. Two minima are expected because of the quadratic dependence of the cross section on the
coefficients. The 𝑝 values for compatibility of the 𝑐 𝑔𝑔ℎℎ -𝑐 ℎℎℎ , 𝑐 𝑡𝑡 ℎℎ -𝑐 ℎℎℎ , and 𝑐 𝑔𝑔ℎℎ -𝑐 𝑡𝑡 ℎℎ measurements
with the SM predictions are 0.044, 0.21 and 0.031, respectively. The relatively low 𝑝 values are primarily
¯ 𝑏¯ analysis [25], where the data-driven background modeling cannot perfectly describe the
due to the 𝑏 𝑏𝑏
background distribution in data, making non-SM signals more favorable in the fit. Because of insufficient
sensitivity, the combination does not allow simultaneous constraints to be placed on 𝑐 ℎℎℎ , 𝑐 𝑔𝑔ℎℎ , and 𝑐 𝑡𝑡 ℎℎ
in a more model-independent manner [45].
¯ +𝜏−,
In summary, this Letter presents a combination of the results of searches for 𝐻𝐻 production in the 𝑏 𝑏𝜏
miss
𝑏 ¯𝑏𝛾𝛾, 𝑏 ¯𝑏𝑏 ¯𝑏, multilepton, and 𝑏 ¯𝑏ℓℓ + 𝐸 T decay channels, utilizing the complete LHC run 2 dataset of
13 TeV proton-proton collisions recorded with the ATLAS detector. This new combination provides the best
expected sensitivities to the 𝐻𝐻 production cross section and the Higgs boson self-coupling, superseding
the results on the di-Higgs measurements of Ref. [4]. The results agree well with the SM predictions.
When using Higgs effective field theory to interpret the measurements, unprecedented constraints are
placed on the effective 𝑔𝑔𝐻𝐻 and 𝑡 𝑡¯𝐻𝐻 interactions.

6

## PDF page 7

2 ln

8
7

ATLAS

bb
bbbb
bb +

Combined
Multilepton

s = 13 TeV, 126 140 fb 1
HH combination
6 All other fixed to SM

bb + ETmiss

Obs.:
95% CL [0.6, 1.5]
Exp. (SM): 95% CL [0.4, 1.6]

5
4

95% CL

3
2
68% CL

1
0 0.5

0

0.5

1.5

2

2.5
2V

(b)

2V

(a)

1

8 ATLAS

bb
bbbb

Combined

Multilepton
s = 13 TeV, 126 140 fb 1
bb +
bb + ETmiss
6 HH combination
Obs. 95% CL
Best fit (4.3, 0.92)

Exp. (SM) 95% CL

SM prediction

4
2
0
2
5

0

5

10

15

(c)

Figure 3: Expected values (dashed lines) of the test statistic (−2 ln Λ) as functions of (a) 𝜅 𝜆 and (b) 𝜅 2𝑉 . These results
¯ (purple), 𝑏 𝑏𝜏
¯ + 𝜏 − (green), multilepton (cyan), 𝑏 𝑏𝑏
¯ 𝑏¯ (blue), and 𝑏 𝑏ℓℓ
¯ + 𝐸 miss
are shown for the decay channels 𝑏 𝑏𝛾𝛾
T
(brown), as well as their combination (black). The observed values from the combined data are depicted by solid
black lines. These results are computed with the assumption that all other Higgs boson couplings follow the SM
predictions. (c) The expected 95% CL contours in the 𝜅2𝑉 -𝜅 𝜆 plane, corresponding to the individual decay channels
and their combination, are illustrated using dashed lines. The observed contour from the combined results is depicted
by a solid black line. The SM prediction is marked by a star, and the combined best-fit value is indicated by a cross.

7

## PDF page 8

ATLAS

ctthh

cgghh

1.5

Observed 68% CL
Observed 95% CL
Best fit (6.6, -0.45)
Expected (SM) 68% CL
Expected (SM) 95% CL
SM prediction

s = 13 TeV, 126 140 fb 1

bb
+ bb + bbbb
1 HH
All other c fixed to SM
+

4
3

ATLAS

Observed 68% CL
Observed 95% CL
Best fit (-3.5, 0.74)
Expected (SM) 68% CL
Expected (SM) 95% CL
SM prediction

s = 13 TeV, 126 140 fb 1

HH bb + + bb + bbbb
All other c fixed to SM

2

0.5
1
0

0

0.5

1
2.5

0

2.5

5

7.5

10

12.5

10

chhh

5

0

ctthh

(a)

5

10

15

chhh

(b)

2

ATLAS

Observed 68% CL
Observed 95% CL
Best fit (-0.42, 0.49)
Expected (SM) 68% CL
Expected (SM) 95% CL
SM prediction

s = 13 TeV, 126 140 fb 1

+ bb + bbbb
1.5 HH bb
All other c fixed to SM
+

1
0.5
0
0.5
0.8

0.6

0.4

0.2

0

0.2

0.4

0.6

cgghh

(c)

Figure 4: Two-dimensional test-statistic contours at 68% CL (solid line) and 95% CL (dashed line) in the (a)
𝑐 𝑔𝑔ℎℎ -𝑐 ℎℎℎ , (b) 𝑐 𝑡𝑡 ℎℎ -𝑐 ℎℎℎ , and (c) 𝑐 𝑡𝑡 ℎℎ -𝑐 𝑔𝑔ℎℎ HEFT parameter spaces, with 𝑐 𝑡𝑡 ℎℎ , 𝑐 𝑔𝑔ℎℎ , and 𝑐 ℎℎℎ fixed to their
SM values, respectively. The corresponding SM expected contours are shown by the inner and outer shaded regions.
The SM prediction is indicated by the star, while the best-fit value is shown by the cross.

8

## PDF page 9

Acknowledgments—
We thank CERN for the very successful operation of the LHC and its injectors, as well as the support staff
at CERN and at our institutions worldwide without whom ATLAS could not be operated efficiently.
The crucial computing support from all WLCG partners is acknowledged gratefully, in particular from
CERN, the ATLAS Tier-1 facilities at TRIUMF/SFU (Canada), NDGF (Denmark, Norway, Sweden),
CC-IN2P3 (France), KIT/GridKA (Germany), INFN-CNAF (Italy), NL-T1 (Netherlands), PIC (Spain),
RAL (UK) and BNL (USA), the Tier-2 facilities worldwide and large non-WLCG resource providers.
Major contributors of computing resources are listed in Ref. [46].
We gratefully acknowledge the support of ANPCyT, Argentina; YerPhI, Armenia; ARC, Australia;
BMWFW and FWF, Austria; ANAS, Azerbaĳan; CNPq and FAPESP, Brazil; NSERC, NRC and CFI,
Canada; CERN; ANID, Chile; CAS, MOST and NSFC, China; Minciencias, Colombia; MEYS CR, Czech
Republic; DNRF and DNSRC, Denmark; IN2P3-CNRS and CEA-DRF/IRFU, France; SRNSFG, Georgia;
BMBF, HGF and MPG, Germany; GSRI, Greece; RGC and Hong Kong SAR, China; ISF and Benoziyo
Center, Israel; INFN, Italy; MEXT and JSPS, Japan; CNRST, Morocco; NWO, Netherlands; RCN, Norway;
MNiSW, Poland; FCT, Portugal; MNE/IFA, Romania; MESTD, Serbia; MSSR, Slovakia; ARIS and MVZI,
Slovenia; DSI/NRF, South Africa; MICINN, Spain; SRC and Wallenberg Foundation, Sweden; SERI,
SNSF and Cantons of Bern and Geneva, Switzerland; NSTC, Taipei; TENMAK, Türkiye; STFC, United
Kingdom; DOE and NSF, United States of America.
Individual groups and members have received support from BCKDF, CANARIE, CRC and DRAC,
Canada; CERN-CZ, FORTE and PRIMUS, Czech Republic; COST, ERC, ERDF, Horizon 2020, ICSCNextGenerationEU and Marie Skłodowska-Curie Actions, European Union; Investissements d’Avenir Labex,
Investissements d’Avenir Idex and ANR, France; DFG and AvH Foundation, Germany; Herakleitos, Thales
and Aristeia programmes co-financed by EU-ESF and the Greek NSRF, Greece; BSF-NSF and MINERVA,
Israel; NCN and NAWA, Poland; La Caixa Banking Foundation, CERCA Programme Generalitat de
Catalunya and PROMETEO and GenT Programmes Generalitat Valenciana, Spain; Göran Gustafssons
Stiftelse, Sweden; The Royal Society and Leverhulme Trust, United Kingdom.
In addition, individual members wish to acknowledge support from Armenia: Yerevan Physics Institute
(FAPERJ); CERN: European Organization for Nuclear Research (CERN PJAS); Chile: Agencia Nacional
de Investigación y Desarrollo (FONDECYT 1230812, FONDECYT 1230987, FONDECYT 1240864);
China: Chinese Ministry of Science and Technology (MOST-2023YFA1605700), National Natural Science Foundation of China (NSFC - 12175119, NSFC 12275265, NSFC-12075060); Czech Republic:
Czech Science Foundation (GACR - 24-11373S), Ministry of Education Youth and Sports (FORTE
CZ.02.01.01/00/22_008/0004632), PRIMUS Research Programme (PRIMUS/21/SCI/017); EU: H2020 European Research Council (ERC - 101002463); European Union: European Research Council (ERC - 948254,
ERC 101089007), Horizon 2020 Framework Programme (MUCCA - CHIST-ERA-19-XAI-00), European
Union, Future Artificial Intelligence Research (FAIR-NextGenerationEU PE00000013), Italian Center for
High Performance Computing, Big Data and Quantum Computing (ICSC, NextGenerationEU); France:
Agence Nationale de la Recherche (ANR-20-CE31-0013, ANR-21-CE31-0013, ANR-21-CE31-0022, ANR22-EDIR-0002), Investissements d’Avenir Labex (ANR-11-LABX-0012); Germany: Baden-Württemberg
Stiftung (BW Stiftung-Postdoc Eliteprogramme), Deutsche Forschungsgemeinschaft (DFG - 469666862,
DFG - CR 312/5-2); Italy: Istituto Nazionale di Fisica Nucleare (ICSC, NextGenerationEU), Ministero dell’Università e della Ricerca (PRIN - 20223N7F8K - PNRR M4.C2.1.1); Japan: Japan Society
for the Promotion of Science (JSPS KAKENHI JP22H01227, JSPS KAKENHI JP22H04944, JSPS

9

## PDF page 10

KAKENHI JP22KK0227, JSPS KAKENHI JP23KK0245); Netherlands: Netherlands Organisation for
Scientific Research (NWO Veni 2020 - VI.Veni.202.179); Norway: Research Council of Norway (RCN314472); Poland: Polish National Agency for Academic Exchange (PPN/PPO/2020/1/00002/U/00001),
Polish National Science Centre (NCN 2021/42/E/ST2/00350, NCN OPUS nr 2022/47/B/ST2/03059,
NCN UMO-2019/34/E/ST2/00393, UMO-2020/37/B/ST2/01043, UMO-2021/40/C/ST2/00187, UMO2022/47/O/ST2/00148, UMO-2023/49/B/ST2/04085); Slovenia: Slovenian Research Agency (ARIS grant
J1-3010); Spain: Generalitat Valenciana (Artemisa, FEDER, IDIFEDER/2018/048), Ministry of Science
and Innovation (MCIN & NextGenEU PCI2022-135018-2, MICIN & FEDER PID2021-125273NB,
RYC2019-028510-I, RYC2020-030254-I, RYC2021-031273-I, RYC2022-038164-I), PROMETEO and
GenT Programmes Generalitat Valenciana (CIDEGENT/2019/027); Sweden: Swedish Research Council (Swedish Research Council 2023-04654, VR 2018-00482, VR 2022-03845, VR 2022-04683, VR
2023-03403, VR grant 2021-03651), Knut and Alice Wallenberg Foundation (KAW 2018.0157, KAW
2018.0458, KAW 2019.0447, KAW 2022.0358); Switzerland: Swiss National Science Foundation (SNSF PCEFP2_194658); United Kingdom: Leverhulme Trust (Leverhulme Trust RPG-2020-004), Royal Society
(NIF-R1-231091); United States of America: U.S. Department of Energy (ECA DE-AC02-76SF00515),
Neubauer Family Foundation.

10

## PDF page 11

References
[1]

ATLAS Collaboration, Observation of a new particle in the search for the Standard Model Higgs
boson with the ATLAS detector at the LHC, Phys. Lett. B 716 (2012) 1,
arXiv: 1207.7214 [hep-ex].

[2]

CMS Collaboration,
Observation of a new boson at a mass of 125 GeV with the CMS experiment at the LHC,
Phys. Lett. B 716 (2012) 30, arXiv: 1207.7235 [hep-ex].

[3]

Particle Data Group, P. Zyla, et al., Review of Particle Physics, PTEP 2020 (2020) 083C01.

[4] ATLAS Collaboration, Constraints on the Higgs boson self-coupling from single- and double-Higgs
√
production with the ATLAS detector using 𝑝 𝑝 collisions at 𝑠 = 13 TeV,
Phys. Lett. B 843 (2023) 137745, arXiv: 2211.01216 [hep-ex].
[5]

CMS Collaboration,
A portrait of the Higgs boson by the CMS experiment ten years after the discovery,
Nature 607 (2022) 60, arXiv: 2207.00043 [hep-ex], Erratum: Nature 623 (2023) E4.

[6]

S. Heinemeyer et al., Handbook of LHC Higgs Cross Sections: 3. Higgs Properties, (2013),
arXiv: 1307.1347 [hep-ph].

[7]

D. de Florian et al.,
Handbook of LHC Higgs Cross Sections: 4. Deciphering the Nature of the Higgs Sector, (2017),
arXiv: 1610.07922 [hep-ph].

[8]

R. Alonso, M. Gavela, L. Merlo, S. Rigolin, and J. Yepes,
The effective chiral Lagrangian for a light dynamical “Higgs particle”,
Phys. Lett. B 722 (2013) 330, arXiv: 1212.3305 [hep-ph].

[9]

G. Buchalla, O. Catà, and C. Krause,
Complete electroweak chiral Lagrangian with a light Higgs at NLO, Nucl. Phys. B 880 (2014) 552,
arXiv: 1307.5017 [hep-ph].

[10]

ATLAS Collaboration, Characterising the Higgs boson with ATLAS data from Run 2 of the LHC,
(2024), arXiv: 2404.05498 [hep-ex].

[11]

S. Dawson, S. Dittmaier, and M. Spira,
Neutral Higgs-boson pair production at hadron colliders: QCD corrections,
Phys. Rev. D 58 (1998) 115012, arXiv: hep-ph/9805244.

[12]

S. Borowka et al., Higgs Boson Pair Production in Gluon Fusion at Next-to-Leading Order with
Full Top-Quark Mass Dependence, Phys. Rev. Lett. 117 (2016) 079901,
arXiv: 1604.06447 [hep-ph].

[13]

J. Baglio et al., Gluon fusion into Higgs pairs at NLO QCD and the top mass scheme,
Eur. Phys. J. C 79 (2019) 459, arXiv: 1811.05692 [hep-ph].

[14]

D. de Florian and J. Mazzitelli,
Higgs Boson Pair Production at Next-to-Next-to-Leading Order in QCD,
Phys. Rev. Lett. 111 (2013) 201801, arXiv: 1309.6594 [hep-ph].

[15]

D. Y. Shao, C. S. Li, H. T. Li, and J. Wang,
Threshold resummation effects in Higgs boson pair production at the LHC, JHEP 07 (2013) 169,
arXiv: 1301.1245 [hep-ph].

11

## PDF page 12

[16]

D. de Florian and J. Mazzitelli,
Higgs pair production at next-to-next-to-leading logarithmic accuracy at the LHC,
JHEP 09 (2015) 053, arXiv: 1505.07122 [hep-ph].

[17]

M. Grazzini et al., Higgs boson pair production at NNLO with top quark mass effects,
JHEP 05 (2018) 059, arXiv: 1803.02463 [hep-ph].

[18]

J. Baglio et al., 𝑔𝑔 → 𝐻𝐻: Combined uncertainties, Phys. Rev. D 103 (2021) 056002,
arXiv: 2008.11626 [hep-ph].

[19]

F. Bishara, R. Contino, and J. Rojo,
Higgs pair production in vector-boson fusion at the LHC and beyond, Eur. Phys. J. C 77 (2017) 481,
arXiv: 1611.03860 [hep-ph].

[20]

J. Baglio et al., The measurement of the Higgs self-coupling at the LHC: theoretical status,
JHEP 04 (2013) 151, arXiv: 1212.5581.

[21]

R. Frederix et al., Higgs pair production at the LHC with NLO and parton-shower effects,
Phys. Lett. B 732 (2014) 142, arXiv: 1401.7340 [hep-ph].

[22]

L.-S. Ling et al.,
NNLO QCD corrections to Higgs pair production via vector boson fusion at hadron colliders,
Phys. Rev. D 89 (2014) 073001, arXiv: 1401.7754 [hep-ph].

[23]

F. A. Dreyer and A. Karlberg, Vector-Boson Fusion Higgs Pair Production at N3 LO,
Phys. Rev. D 98 (2018) 114016, arXiv: 1811.07906 [hep-ph].

[24]

F. A. Dreyer and A. Karlberg,
Fully differential Vector-Boson Fusion Higgs Pair Production at Next-to-Next-to-Leading Order,
Phys. Rev. D 99 (2019) 074028, arXiv: 1811.07918 [hep-ph].
[25] ATLAS Collaboration, Search for nonresonant pair production of Higgs bosons in the 𝑏 ¯𝑏𝑏 𝑏¯ final
√
state in 𝑝 𝑝 collisions at 𝑠 = 13 TeV with the ATLAS detector, Phys. Rev. D 108 (2023) 052003,
arXiv: 2301.03212 [hep-ex].
[26]

ATLAS Collaboration, Search for pair production of boosted Higgs bosons via vector-boson fusion
¯ 𝑏¯ final state using 𝑝 𝑝 collisions at √𝑠 = 13 TeV with the ATLAS detector, (2024),
in the 𝑏 𝑏𝑏
arXiv: 2404.17193 [hep-ex].

[27]

ATLAS Collaboration,
Search for the non-resonant production of Higgs boson pairs via gluon fusion and vector-boson
¯ + 𝜏 − final state in proton-proton collisions at √𝑠 = 13 TeV with the ATLAS detector,
fusion in the 𝑏 𝑏𝜏
Phys. Rev. D 110 (2024) 032012, arXiv: 2404.12660 [hep-ex].

[28]

ATLAS Collaboration, Studies of new Higgs boson interactions through nonresonant 𝐻𝐻
√
¯
production in the 𝑏 𝑏𝛾𝛾
final state in 𝑝 𝑝 collisions at 𝑠 = 13 TeV with the ATLAS detector,
JHEP 01 (2024) 066, arXiv: 2310.12301 [hep-ex].

[29]

ATLAS Collaboration, Search for non-resonant Higgs boson pair production in final states with
√
leptons, taus, and photons in 𝑝 𝑝 collisions at 𝑠 = 13 TeV with the ATLAS detector, (2024),
arXiv: 2405.20040 [hep-ex].

[30]

ATLAS Collaboration, Search for non-resonant Higgs boson pair production in the 2𝑏 + 2ℓ + 𝐸 Tmiss
√
final state in 𝑝 𝑝 collisions at 𝑠 = 13TeV with the ATLAS detector, JHEP 02 (2024) 037,
arXiv: 2310.11286 [hep-ex].

12

## PDF page 13

[31]

ATLAS Collaboration, Performance of the ATLAS trigger system in 2015,
Eur. Phys. J. C 77 (2017) 317, arXiv: 1611.09661 [hep-ex].

[32]

ATLAS Collaboration, The ATLAS Experiment at the CERN Large Hadron Collider,
JINST 3 (2008) S08003.

[33]

ATLAS Collaboration, ATLAS Insertable B-Layer: Technical Design Report,
ATLAS-TDR-19; CERN-LHCC-2010-013, 2010,
url: https://cds.cern.ch/record/1291633, Addendum: ATLAS-TDR-19-ADD-1;
CERN-LHCC-2012-009, 2012, url: https://cds.cern.ch/record/1451888.

[34]

B. Abbott et al., Production and integration of the ATLAS Insertable B-Layer,
JINST 13 (2018) T05008, arXiv: 1803.00844 [physics.ins-det].

[35]

ATLAS Collaboration, Software and computing for Run 3 of the ATLAS experiment at the LHC,
(2024), arXiv: 2404.06335 [hep-ex].

[36]

L. Alasfar et al., Effective Field Theory descriptions of Higgs boson pair production, 2023,
arXiv: 2304.01968 [hep-ph].

[37]

G. Cowan, K. Cranmer, E. Gross, and O. Vitells,
Asymptotic formulae for likelihood-based tests of new physics, Eur. Phys. J. C 71 (2011) 1554,
arXiv: 1007.1727 [physics.data-an], Erratum: Eur. Phys. J. C 73 (2013) 2501.

[38]

A. L. Read, Presentation of search results: the 𝐶 𝐿 𝑆 technique, J. Phys. G 28 (2002) 2693.

[39]

ATLAS Collaboration,
Measurements of inclusive and differential fiducial cross-sections of 𝑡 𝑡¯ production with additional
√
heavy-flavour jets in proton–proton collisions at 𝑠 = 13 TeV with the ATLAS detector,
JHEP 04 (2019) 046, arXiv: 1811.12113 [hep-ex].

[40]

ATLAS Collaboration, Measurement of the cross-section for 𝑊 boson production in association
√
with 𝑏-jets in 𝑝 𝑝 collisions at 𝑠 = 7 TeV with the ATLAS detector, JHEP 06 (2013) 084,
arXiv: 1302.2929 [hep-ex].

[41]

ATLAS Collaboration, Study of heavy-flavor quarks produced in association with top-quark pairs at
√
𝑠 = 7 TeV using the ATLAS detector, Phys. Rev. D 89 (2014) 072012,
arXiv: 1304.6386 [hep-ex].

[42]

ATLAS Collaboration, Measurements of the Higgs boson inclusive and differential fiducial cross
√
sections in the 4ℓ decay channel at 𝑠 = 13 TeV, Eur. Phys. J. C 80 (2020) 942,
arXiv: 2004.03969 [hep-ex].

[43]

ATLAS Collaboration,
Measurements of the Higgs boson inclusive and differential fiducial cross-sections in the diphoton
√
decay channel with 𝑝 𝑝 collisions at 𝑠 = 13 TeV with the ATLAS detector, JHEP 08 (2022) 027,
arXiv: 2202.00487 [hep-ex].

[44]

The test statistic and statistical uncertainties of the signal MC samples are updated in the
¯ + 𝐸 miss result compared to Ref. [30].
𝑏 𝑏ℓℓ
T

[45]

The results in both the 𝜅 and HEFT frameworks are affected by the issue concerning the ggF 𝐻𝐻
prediction for BSM scenarios in Powheg reported in the erratum to Ref. [47]. The main effect is on
the high-𝑚 𝐻 𝐻 region and decreases the signal acceptance. The changes to resolve this issue
described in Ref. [48] are not included, to be consistent with individual channels. It was estimated
that the impact on the 95% CL limits would be smaller than 4% for 𝜅 𝜆 , negligible for 𝑐 𝑔𝑔ℎℎ , and at
most 10% for 𝑐 𝑡𝑡 ℎℎ .

13

## PDF page 14

[46]

ATLAS Collaboration, ATLAS Computing Acknowledgements, ATL-SOFT-PUB-2023-001, 2023,
url: https://cds.cern.ch/record/2869272.

[47]

G. Heinrich, J. Lang, and L. Scyboz,
SMEFT predictions for gg → hh at full NLO QCD and truncation uncertainties,
JHEP 08 (2022) 079, arXiv: 2204.13045 [hep-ph], Erratum: JHEP 10 (2023) 86.

[48]

E. Bagnaschi, G. Degrassi, and R. Gröber, Higgs boson pair production at NLO in the POWHEG
approach and the top quark mass uncertainties, Eur. Phys. J. C 83 (2023) 1054,
arXiv: 2309.10525 [hep-ph].

14

## PDF page 15

The ATLAS Collaboration
G. Aad 104 , E. Aakvaag 17 , B. Abbott 123 , S. Abdelhameed 119a , K. Abeling 56 , N.J. Abicht 50 ,
S.H. Abidi 30 , M. Aboelela 45 , A. Aboulhorma 36e , H. Abramowicz 154 , H. Abreu 153 ,
Y. Abulaiti 120 , B.S. Acharya 70a,70b,k , A. Ackermann 64a , C. Adam Bourdarios 4 ,
L. Adamczyk 87a , S.V. Addepalli 27 , M.J. Addison 103 , J. Adelman 118 , A. Adiguzel 22c ,
T. Adye 137 , A.A. Affolder 139 , Y. Afik 40 , M.N. Agaras 13 , J. Agarwala 74a,74b ,
A. Aggarwal 102 , C. Agheorghiesei 28c , F. Ahmadov 39,x , W.S. Ahmed 106 , S. Ahuja 97 ,
X. Ai 63e , G. Aielli 77a,77b , A. Aikot 166 , M. Ait Tamlihat 36e , B. Aitbenchikh 36a ,
M. Akbiyik 102 , T.P.A. Åkesson 100 , A.V. Akimov 38 , D. Akiyama 171 , N.N. Akolkar 25 ,
S. Aktas 22a , K. Al Khoury 42 , G.L. Alberghi 24b , J. Albert 168 , P. Albicocco 54 , G.L. Albouy 61 ,
S. Alderweireldt 53 , Z.L. Alegria 124 , M. Aleksa 37 , I.N. Aleksandrov 39 , C. Alexa 28b ,
T. Alexopoulos 10 , F. Alfonsi 24b , M. Algren 57 , M. Alhroob 170 , B. Ali 135 , H.M.J. Ali 93,r ,
S. Ali 32 , S.W. Alibocus 94 , M. Aliev 34c , G. Alimonti 72a , W. Alkakhi 56 , C. Allaire 67 ,
B.M.M. Allbrooke 149 , J.F. Allen 53 , C.A. Allendes Flores 140f , P.P. Allport 21 , A. Aloisio 73a,73b ,
F. Alonso 92 , C. Alpigiani 141 , Z.M.K. Alsolami 93 , M. Alvarez Estevez 101 ,
A. Alvarez Fernandez 102 , M. Alves Cardoso 57 , M.G. Alviggi 73a,73b , M. Aly 103 ,
Y. Amaral Coutinho 84b , A. Ambler 106 , C. Amelung37 , M. Amerl 103 , C.G. Ames 111 ,
D. Amidei 108 , B. Amini 55 , K.J. Amirie 158 , S.P. Amor Dos Santos 133a , K.R. Amos 166 ,
D. Amperiadou 155 , S. An85 , V. Ananiev 128 , C. Anastopoulos 142 , T. Andeen 11 , J.K. Anders 37 ,
A.C. Anderson 60 , S.Y. Andrean 48a,48b , A. Andreazza 72a,72b , S. Angelidakis 9 , A. Angerami 42 ,
A.V. Anisenkov 38 , A. Annovi 75a , C. Antel 57 , E. Antipov 148 , M. Antonelli 54 , F. Anulli 76a ,
M. Aoki 85 , T. Aoki 156 , M.A. Aparo 149 , L. Aperio Bella 49 , C. Appelt 19 , A. Apyan 27 ,
S.J. Arbiol Val 88 , C. Arcangeletti 54 , A.T.H. Arce 52 , J-F. Arguin 110 , S. Argyropoulos 55 ,
J.-H. Arling 49 , O. Arnaez 4 , H. Arnold 148 , G. Artoni 76a,76b , H. Asada 113 , K. Asai 121 ,
S. Asai 156 , N.A. Asbah 37 , R.A. Ashby Pickering 170 , K. Assamagan 30 , R. Astalos 29a ,
K.S.V. Astrand 100 , S. Atashi 162 , R.J. Atkin 34a , M. Atkinson165 , H. Atmani36f ,
P.A. Atmasiddha 131 , K. Augsten 135 , S. Auricchio 73a,73b , A.D. Auriol 21 , V.A. Austrup 103 ,
G. Avolio 37 , K. Axiotis 57 , G. Azuelos 110,ac , D. Babal 29b , H. Bachacou 138 , K. Bachas 155,o ,
A. Bachiu 35 , F. Backman 48a,48b , A. Badea 40 , T.M. Baer 108 , P. Bagnaia 76a,76b , M. Bahmani 19 ,
D. Bahner 55 , K. Bai 126 , J.T. Baines 137 , L. Baines 96 , O.K. Baker 175 , E. Bakos 16 ,
D. Bakshi Gupta 8 , L.E. Balabram Filho 84b , V. Balakrishnan 123 , R. Balasubramanian 4 ,
E.M. Baldin 38 , P. Balek 87a , E. Ballabene 24b,24a , F. Balli 138 , L.M. Baltes 64a , W.K. Balunas 33 ,
J. Balz 102 , I. Bamwidhi 119b , E. Banas 88 , M. Bandieramonte 132 , A. Bandyopadhyay 25 ,
S. Bansal 25 , L. Barak 154 , M. Barakat 49 , E.L. Barberio 107 , D. Barberis 58b,58a , M. Barbero 104 ,
M.Z. Barel 117 , T. Barillari 112 , M-S. Barisits 37 , T. Barklow 146 , P. Baron 125 ,
D.A. Baron Moreno 103 , A. Baroncelli 63a , A.J. Barr 129 , J.D. Barr 98 , F. Barreiro 101 ,
J. Barreiro Guimarães da Costa 14 , U. Barron 154 , M.G. Barros Teixeira 133a , S. Barsov 38 ,
F. Bartels 64a , R. Bartoldus 146 , A.E. Barton 93 , P. Bartos 29a , A. Basan 102 , M. Baselga 50 ,
A. Bassalat 67,b , M.J. Basso 159a , S. Bataju 45 , R. Bate 167 , R.L. Bates 60 , S. Batlamous101 ,
B. Batool 144 , M. Battaglia 139 , D. Battulga 19 , M. Bauce 76a,76b , M. Bauer 80 , P. Bauer 25 ,
L.T. Bazzano Hurrell 31 , J.B. Beacham 52 , T. Beau 130 , J.Y. Beaucamp 92 , P.H. Beauchemin 161 ,
P. Bechtle 25 , H.P. Beck 20,n , K. Becker 170 , A.J. Beddall 83 , V.A. Bednyakov 39 , C.P. Bee 148 ,
L.J. Beemster 16 , T.A. Beermann 37 , M. Begalli 84d , M. Begel 30 , A. Behera 148 , J.K. Behr 49 ,
J.F. Beirer 37 , F. Beisiegel 25 , M. Belfkir 119b , G. Bella 154 , L. Bellagamba 24b , A. Bellerive 35 ,
P. Bellos 21 , K. Beloborodov 38 , D. Benchekroun 36a , F. Bendebba 36a , Y. Benhammou 154 ,

15

## PDF page 16

K.C. Benkendorfer 62 , L. Beresford 49 , M. Beretta 54 , E. Bergeaas Kuutmann 164 , N. Berger 4 ,
B. Bergmann 135 , J. Beringer 18a , G. Bernardi 5 , C. Bernius 146 , F.U. Bernlochner 25 ,
F. Bernon 37,104 , A. Berrocal Guardia 13 , T. Berry 97 , P. Berta 136 , A. Berthold 51 , S. Bethke 112 ,
A. Betti 76a,76b , A.J. Bevan 96 , N.K. Bhalla 55 , S. Bhatta 148 , D.S. Bhattacharya 169 ,
P. Bhattarai 146 , K.D. Bhide 55 , V.S. Bhopatkar 124 , R.M. Bianchi 132 , G. Bianco 24b,24a ,
O. Biebel 111 , R. Bielski 126 , M. Biglietti 78a , C.S. Billingsley45 , Y. Bimgdi 36f , M. Bindi 56 ,
A. Bingul 22b , C. Bini 76a,76b , G.A. Bird 33 , M. Birman 172 , M. Biros 136 , S. Biryukov 149 ,
T. Bisanz 50 , E. Bisceglie 44b,44a , J.P. Biswal 137 , D. Biswas 144 , I. Bloch 49 , A. Blue 60 ,
U. Blumenschein 96 , J. Blumenthal 102 , V.S. Bobrovnikov 38 , M. Boehler 55 , B. Boehm 169 ,
D. Bogavac 37 , A.G. Bogdanchikov 38 , L.S. Boggia 130 , C. Bohm 48a , V. Boisvert 97 ,
P. Bokan 37 , T. Bold 87a , M. Bomben 5 , M. Bona 96 , M. Boonekamp 138 , C.D. Booth 97 ,
A.G. Borbély 60 , I.S. Bordulev 38 , G. Borissov 93 , D. Bortoletto 129 , D. Boscherini 24b ,
M. Bosman 13 , J.D. Bossio Sola 37 , K. Bouaouda 36a , N. Bouchhar 166 , L. Boudet 4 ,
J. Boudreau 132 , E.V. Bouhova-Thacker 93 , D. Boumediene 41 , R. Bouquet 58b,58a , A. Boveia 122 ,
J. Boyd 37 , D. Boye 30 , I.R. Boyko 39 , L. Bozianu 57 , J. Bracinik 21 , N. Brahimi 4 ,
G. Brandt 174 , O. Brandt 33 , F. Braren 49 , B. Brau 105 , J.E. Brau 126 , R. Brener 172 ,
L. Brenner 117 , R. Brenner 164 , S. Bressler 172 , G. Brianti 79a,79b , D. Britton 60 , D. Britzger 112 ,
I. Brock 25 , G. Brooĳmans 42 , E.M. Brooks 159b , E. Brost 30 , L.M. Brown 168 , L.E. Bruce 62 ,
T.L. Bruckler 129 , P.A. Bruckman de Renstrom 88 , B. Brüers 49 , A. Bruni 24b , G. Bruni 24b ,
M. Bruschi 24b , N. Bruscino 76a,76b , T. Buanes 17 , Q. Buat 141 , D. Buchin 112 , A.G. Buckley 60 ,
O. Bulekov 38 , B.A. Bullard 146 , S. Burdin 94 , C.D. Burgard 50 , A.M. Burger 37 ,
B. Burghgrave 8 , O. Burlayenko 55 , J. Burleson 165 , J.T.P. Burr 33 , J.C. Burzynski 145 ,
E.L. Busch 42 , V. Büscher 102 , P.J. Bussey 60 , J.M. Butler 26 , C.M. Buttar 60 ,
J.M. Butterworth 98 , W. Buttinger 137 , C.J. Buxo Vazquez 109 , A.R. Buzykaev 38 ,
S. Cabrera Urbán 166 , L. Cadamuro 67 , D. Caforio 59 , H. Cai 132 , Y. Cai 14,114c , Y. Cai 114a ,
V.M.M. Cairo 37 , O. Cakir 3a , N. Calace 37 , P. Calafiura 18a , G. Calderini 130 , P. Calfayan 69 ,
G. Callea 60 , L.P. Caloba84b , D. Calvet 41 , S. Calvet 41 , M. Calvetti 75a,75b , R. Camacho Toro 130 ,
S. Camarda 37 , D. Camarero Munoz 27 , P. Camarri 77a,77b , M.T. Camerlingo 73a,73b ,
D. Cameron 37 , C. Camincher 168 , M. Campanelli 98 , A. Camplani 43 , V. Canale 73a,73b ,
A.C. Canbay 3a , E. Canonero 97 , J. Cantero 166 , Y. Cao 165 , F. Capocasa 27 , M. Capua 44b,44a ,
A. Carbone 72a,72b , R. Cardarelli 77a , J.C.J. Cardenas 8 , G. Carducci 44b,44a , T. Carli 37 ,
G. Carlino 73a , J.I. Carlotto 13 , B.T. Carlson 132,p , E.M. Carlson 168,159a , J. Carmignani 94 ,
L. Carminati 72a,72b , A. Carnelli 138 , M. Carnesale 76a,76b , S. Caron 116 , E. Carquin 140f ,
I.B. Carr 107 , S. Carrá 72a , G. Carratta 24b,24a , A.M. Carroll 126 , T.M. Carter 53 ,
M.P. Casado 13,h , M. Caspar 49 , F.L. Castillo 4 , L. Castillo Garcia 13 , V. Castillo Gimenez 166 ,
N.F. Castro 133a,133e , A. Catinaccio 37 , J.R. Catmore 128 , T. Cavaliere 4 , V. Cavaliere 30 ,
N. Cavalli 24b,24a , L.J. Caviedes Betancourt23b , Y.C. Cekmecelioglu 49 , E. Celebi 83 , S. Cella 37 ,
F. Celli 129 , M.S. Centonze 71a,71b , V. Cepaitis 57 , K. Cerny 125 , A.S. Cerqueira 84a ,
A. Cerri 149 , L. Cerrito 77a,77b , F. Cerutti 18a , B. Cervato 144 , A. Cervelli 24b , G. Cesarini 54 ,
S.A. Cetin 83 , D. Chakraborty 118 , J. Chan 18a , W.Y. Chan 156 , J.D. Chapman 33 , E. Chapon 138 ,
B. Chargeishvili 152b , D.G. Charlton 21 , M. Chatterjee 20 , C. Chauhan 136 , Y. Che 114a ,
S. Chekanov 6 , S.V. Chekulaev 159a , G.A. Chelkov 39,a , A. Chen 108 , B. Chen 154 , B. Chen 168 ,
H. Chen 114a , H. Chen 30 , J. Chen 63c , J. Chen 145 , M. Chen 129 , S. Chen 89 , S.J. Chen 114a ,
X. Chen 63c , X. Chen 15,ab , Y. Chen 63a , C.L. Cheng 173 , H.C. Cheng 65a , S. Cheong 146 ,
A. Cheplakov 39 , E. Cheremushkina 49 , E. Cherepanova 117 , R. Cherkaoui El Moursli 36e ,
E. Cheu 7 , K. Cheung 66 , L. Chevalier 138 , V. Chiarella 54 , G. Chiarelli 75a , N. Chiedde 104 ,
G. Chiodini 71a , A.S. Chisholm 21 , A. Chitan 28b , M. Chitishvili 166 , M.V. Chizhov 39 ,

16

## PDF page 17

K. Choi 11 , Y. Chou 141 , E.Y.S. Chow 116 , K.L. Chu 172 , M.C. Chu 65a , X. Chu 14,114c ,
Z. Chubinidze 54 , J. Chudoba 134 , J.J. Chwastowski 88 , D. Cieri 112 , K.M. Ciesla 87a ,
V. Cindro 95 , A. Ciocio 18a , F. Cirotto 73a,73b , Z.H. Citron 172 , M. Citterio 72a , D.A. Ciubotaru28b ,
A. Clark 57 , P.J. Clark 53 , N. Clarke Hall 98 , C. Clarry 158 , J.M. Clavĳo Columbie 49 ,
S.E. Clawson 49 , C. Clement 48a,48b , Y. Coadou 104 , M. Cobal 70a,70c , A. Coccaro 58b ,
R.F. Coelho Barrue 133a , R. Coelho Lopes De Sa 105 , S. Coelli 72a , B. Cole 42 , J. Collot 61 ,
P. Conde Muiño 133a,133g , M.P. Connell 34c , S.H. Connell 34c , E.I. Conroy 129 , F. Conventi 73a,ad ,
H.G. Cooke 21 , A.M. Cooper-Sarkar 129 , F.A. Corchia 24b,24a , A. Cordeiro Oudot Choi 130 ,
L.D. Corpe 41 , M. Corradi 76a,76b , F. Corriveau 106,w , A. Cortes-Gonzalez 19 , M.J. Costa 166 ,
F. Costanza 4 , D. Costanzo 142 , B.M. Cote 122 , J. Couthures 4 , G. Cowan 97 , K. Cranmer 173 ,
L. Cremer 50 , D. Cremonini 24b,24a , S. Crépé-Renaudin 61 , F. Crescioli 130 , M. Cristinziani 144 ,
M. Cristoforetti 79a,79b , V. Croft 117 , J.E. Crosby 124 , G. Crosetti 44b,44a , A. Cueto 101 , H. Cui 98 ,
Z. Cui 7 , W.R. Cunningham 60 , F. Curcio 166 , J.R. Curran 53 , P. Czodrowski 37 ,
M.J. Da Cunha Sargedas De Sousa 58b,58a , J.V. Da Fonseca Pinto 84b , C. Da Via 103 ,
W. Dabrowski 87a , T. Dado 37 , S. Dahbi 151 , T. Dai 108 , D. Dal Santo 20 , C. Dallapiccola 105 ,
M. Dam 43 , G. D’amen 30 , V. D’Amico 111 , J. Damp 102 , J.R. Dandoy 35 , D. Dannheim 37 ,
M. Danninger 145 , V. Dao 148 , G. Darbo 58b , S.J. Das 30,ae , F. Dattola 49 , S. D’Auria 72a,72b ,
A. D’avanzo 73a,73b , C. David 34a , T. Davidek 136 , I. Dawson 96 , H.A. Day-hall 135 , K. De 8 ,
R. De Asmundis 73a , N. De Biase 49 , S. De Castro 24b,24a , N. De Groot 116 , P. de Jong 117 ,
H. De la Torre 118 , A. De Maria 114a , A. De Salvo 76a , U. De Sanctis 77a,77b , F. De Santis 71a,71b ,
A. De Santo 149 , J.B. De Vivie De Regie 61 , J. Debevc 95 , D.V. Dedovich39 , J. Degens 94 ,
A.M. Deiana 45 , F. Del Corso 24b,24a , J. Del Peso 101 , L. Delagrange 130 , F. Deliot 138 ,
C.M. Delitzsch 50 , M. Della Pietra 73a,73b , D. Della Volpe 57 , A. Dell’Acqua 37 ,
L. Dell’Asta 72a,72b , M. Delmastro 4 , P.A. Delsart 61 , S. Demers 175 , M. Demichev 39 ,
S.P. Denisov 38 , L. D’Eramo 41 , D. Derendarz 88 , F. Derue 130 , P. Dervan 94 , K. Desch 25 ,
C. Deutsch 25 , F.A. Di Bello 58b,58a , A. Di Ciaccio 77a,77b , L. Di Ciaccio 4 ,
A. Di Domenico 76a,76b , C. Di Donato 73a,73b , A. Di Girolamo 37 , G. Di Gregorio 37 ,
A. Di Luca 79a,79b , B. Di Micco 78a,78b , R. Di Nardo 78a,78b , K.F. Di Petrillo 40 ,
M. Diamantopoulou 35 , F.A. Dias 117 , T. Dias Do Vale 145 , M.A. Diaz 140a,140b ,
F.G. Diaz Capriles 25 , A.R. Didenko39 , M. Didenko 166 , E.B. Diehl 108 , S. Díez Cornell 49 ,
C. Diez Pardos 144 , C. Dimitriadi 164 , A. Dimitrievska 21 , J. Dingfelder 25 , T. Dingley 129 ,
I-M. Dinu 28b , S.J. Dittmeier 64b , F. Dittus 37 , M. Divisek 136 , B. Dixit 94 , F. Djama 104 ,
T. Djobava 152b , C. Doglioni 103,100 , A. Dohnalova 29a , J. Dolejsi 136 , Z. Dolezal 136 ,
K. Domĳan 87a , K.M. Dona 40 , M. Donadelli 84d , B. Dong 109 , J. Donini 41 ,
A. D’Onofrio 73a,73b , M. D’Onofrio 94 , J. Dopke 137 , A. Doria 73a , N. Dos Santos Fernandes 133a ,
P. Dougan 103 , M.T. Dova 92 , A.T. Doyle 60 , M.A. Draguet 129 , E. Dreyer 172 ,
I. Drivas-koulouris 10 , M. Drnevich 120 , M. Drozdova 57 , D. Du 63a , T.A. du Pree 117 ,
F. Dubinin 38 , M. Dubovsky 29a , E. Duchovni 172 , G. Duckeck 111 , O.A. Ducu 28b , D. Duda 53 ,
A. Dudarev 37 , E.R. Duden 27 , M. D’uffizi 103 , L. Duflot 67 , M. Dührssen 37 , I. Duminica 28g ,
A.E. Dumitriu 28b , M. Dunford 64a , S. Dungs 50 , K. Dunne 48a,48b , A. Duperrin 104 ,
H. Duran Yildiz 3a , M. Düren 59 , A. Durglishvili 152b , B.L. Dwyer 118 , G.I. Dyckes 18a ,
M. Dyndal 87a , B.S. Dziedzic 37 , Z.O. Earnshaw 149 , G.H. Eberwein 129 , B. Eckerova 29a ,
S. Eggebrecht 56 , E. Egidio Purcino De Souza 84e , L.F. Ehrke 57 , G. Eigen 17 , K. Einsweiler 18a ,
T. Ekelof 164 , P.A. Ekman 100 , S. El Farkh 36b , Y. El Ghazali 63a , H. El Jarrari 37 ,
A. El Moussaouy 36a , V. Ellajosyula 164 , M. Ellert 164 , F. Ellinghaus 174 , N. Ellis 37 ,
J. Elmsheuser 30 , M. Elsawy 119a , M. Elsing 37 , D. Emeliyanov 137 , Y. Enari 85 , I. Ene 18a ,
S. Epari 13 , P.A. Erland 88 , D. Ernani Martins Neto 88 , M. Errenst 174 , M. Escalier 67 ,

17

## PDF page 18

C. Escobar 166 , E. Etzion 154 , G. Evans 133a , H. Evans 69 , L.S. Evans 97 , A. Ezhilov 38 ,
S. Ezzarqtouni 36a , F. Fabbri 24b,24a , L. Fabbri 24b,24a , G. Facini 98 , V. Fadeyev 139 ,
R.M. Fakhrutdinov 38 , D. Fakoudis 102 , S. Falciano 76a , L.F. Falda Ulhoa Coelho 37 ,
F. Fallavollita 112 , G. Falsetti 44b,44a , J. Faltova 136 , C. Fan 165 , K.Y. Fan 65b , Y. Fan 14 ,
Y. Fang 14,114c , M. Fanti 72a,72b , M. Faraj 70a,70b , Z. Farazpay 99 , A. Farbin 8 , A. Farilla 78a ,
T. Farooque 109 , S.M. Farrington 53 , F. Fassi 36e , D. Fassouliotis 9 , M. Faucci Giannelli 77a,77b ,
W.J. Fawcett 33 , L. Fayard 67 , P. Federic 136 , P. Federicova 134 , O.L. Fedin 38,a , M. Feickert 173 ,
L. Feligioni 104 , D.E. Fellers 126 , C. Feng 63b , Z. Feng 117 , M.J. Fenton 162 , L. Ferencz 49 ,
R.A.M. Ferguson 93 , S.I. Fernandez Luengo 140f , P. Fernandez Martinez 13 , M.J.V. Fernoux 104 ,
J. Ferrando 93 , A. Ferrari 164 , P. Ferrari 117,116 , R. Ferrari 74a , D. Ferrere 57 , C. Ferretti 108 ,
D. Fiacco 76a,76b , F. Fiedler 102 , P. Fiedler 135 , S. Filimonov38 , A. Filipčič 95 , E.K. Filmer 1 ,
F. Filthaut 116 , M.C.N. Fiolhais 133a,133c,c , L. Fiorini 166 , W.C. Fisher 109 , T. Fitschen 103 ,
P.M. Fitzhugh138 , I. Fleck 144 , P. Fleischmann 108 , T. Flick 174 , M. Flores 34d,z ,
L.R. Flores Castillo 65a , L. Flores Sanz De Acedo 37 , F.M. Follega 79a,79b , N. Fomin 33 ,
J.H. Foo 158 , A. Formica 138 , A.C. Forti 103 , E. Fortin 37 , A.W. Fortman 18a , M.G. Foti 18a ,
L. Fountas 9,i , D. Fournier 67 , H. Fox 93 , P. Francavilla 75a,75b , S. Francescato 62 ,
S. Franchellucci 57 , M. Franchini 24b,24a , S. Franchino 64a , D. Francis37 , L. Franco 116 ,
V. Franco Lima 37 , L. Franconi 49 , M. Franklin 62 , G. Frattari 27 , Y.Y. Frid 154 , J. Friend 60 ,
N. Fritzsche 37 , A. Froch 55 , D. Froidevaux 37 , J.A. Frost 129 , Y. Fu 63a ,
S. Fuenzalida Garrido 140f , M. Fujimoto 104 , K.Y. Fung 65a , E. Furtado De Simas Filho 84e ,
M. Furukawa 156 , J. Fuster 166 , A. Gaa 56 , A. Gabrielli 24b,24a , A. Gabrielli 158 , P. Gadow 37 ,
G. Gagliardi 58b,58a , L.G. Gagnon 18a , S. Gaid 163 , S. Galantzan 154 , J. Gallagher 1 ,
E.J. Gallas 129 , B.J. Gallop 137 , K.K. Gan 122 , S. Ganguly 156 , Y. Gao 53 ,
F.M. Garay Walls 140a,140b , B. Garcia30 , C. García 166 , A. Garcia Alonso 117 ,
A.G. Garcia Caffaro 175 , J.E. García Navarro 166 , M. Garcia-Sciveres 18a , G.L. Gardner 131 ,
R.W. Gardner 40 , N. Garelli 161 , D. Garg 81 , R.B. Garg 146 , J.M. Gargan53 , C.A. Garner158 ,
C.M. Garvey 34a , V.K. Gassmann161 , G. Gaudio 74a , V. Gautam13 , P. Gauzzi 76a,76b ,
J. Gavranovic 95 , I.L. Gavrilenko 38 , A. Gavrilyuk 38 , C. Gay 167 , G. Gaycken 126 ,
E.N. Gazis 10 , A.A. Geanta 28b , C.M. Gee 139 , A. Gekow122 , C. Gemme 58b , M.H. Genest 61 ,
A.D. Gentry 115 , S. George 97 , W.F. George 21 , T. Geralis 47 , P. Gessinger-Befurt 37 ,
M.E. Geyik 174 , M. Ghani 170 , K. Ghorbanian 96 , A. Ghosal 144 , A. Ghosh 162 , A. Ghosh 7 ,
B. Giacobbe 24b , S. Giagu 76a,76b , T. Giani 117 , A. Giannini 63a , S.M. Gibson 97 , M. Gignac 139 ,
D.T. Gil 87b , A.K. Gilbert 87a , B.J. Gilbert 42 , D. Gillberg 35 , G. Gilles 117 , L. Ginabat 130 ,
D.M. Gingrich 2,ac , M.P. Giordani 70a,70c , P.F. Giraud 138 , G. Giugliarelli 70a,70c , D. Giugni 72a ,
F. Giuli 37 , I. Gkialas 9,i , L.K. Gladilin 38 , C. Glasman 101 , G.R. Gledhill 126 , G. Glemža 49 ,
M. Glisic126 , I. Gnesi 44b , Y. Go 30 , M. Goblirsch-Kolb 37 , B. Gocke 50 , D. Godin110 ,
B. Gokturk 22a , S. Goldfarb 107 , T. Golling 57 , M.G.D. Gololo 34g , D. Golubkov 38 ,
J.P. Gombas 109 , A. Gomes 133a,133b , G. Gomes Da Silva 144 , A.J. Gomez Delegido 166 ,
R. Gonçalo 133a , L. Gonella 21 , A. Gongadze 152c , F. Gonnella 21 , J.L. Gonski 146 ,
R.Y. González Andana 53 , S. González de la Hoz 166 , R. Gonzalez Lopez 94 ,
C. Gonzalez Renteria 18a , M.V. Gonzalez Rodrigues 49 , R. Gonzalez Suarez 164 ,
S. Gonzalez-Sevilla 57 , L. Goossens 37 , B. Gorini 37 , E. Gorini 71a,71b , A. Gorišek 95 ,
T.C. Gosart 131 , A.T. Goshaw 52 , M.I. Gostkin 39 , S. Goswami 124 , C.A. Gottardo 37 ,
S.A. Gotz 111 , M. Gouighri 36b , V. Goumarre 49 , A.G. Goussiou 141 , N. Govender 34c ,
R.P. Grabarczyk 129 , I. Grabowska-Bold 87a , K. Graham 35 , E. Gramstad 128 ,
S. Grancagnolo 71a,71b , C.M. Grant1,138 , P.M. Gravila 28f , F.G. Gravili 71a,71b , H.M. Gray 18a ,
M. Greco 71a,71b , M.J. Green 1 , C. Grefe 25 , A.S. Grefsrud 17 , I.M. Gregor 49 , K.T. Greif 162 ,

18

## PDF page 19

P. Grenier 146 , S.G. Grewe112 , A.A. Grillo 139 , K. Grimm 32 , S. Grinstein 13,s , J.-F. Grivaz 67 ,
E. Gross 172 , J. Grosse-Knetter 56 , L. Guan 108 , J.G.R. Guerrero Rojas 166 , G. Guerrieri 37 ,
R. Gugel 102 , J.A.M. Guhit 108 , A. Guida 19 , E. Guilloton 170 , S. Guindon 37 , F. Guo 14,114c ,
J. Guo 63c , L. Guo 49 , Y. Guo 108 , R. Gupta 132 , S. Gurbuz 25 , S.S. Gurdasani 55 ,
G. Gustavino 76a,76b , P. Gutierrez 123 , L.F. Gutierrez Zagazeta 131 , M. Gutsche 51 ,
C. Gutschow 98 , C. Gwenlan 129 , C.B. Gwilliam 94 , E.S. Haaland 128 , A. Haas 120 ,
M. Habedank 49 , C. Haber 18a , H.K. Hadavand 8 , A. Hadef 51 , S. Hadzic 112 , A.I. Hagan 93 ,
J.J. Hahn 144 , E.H. Haines 98 , M. Haleem 169 , J. Haley 124 , J.J. Hall 142 , G.D. Hallewell 104 ,
L. Halser 20 , K. Hamano 168 , M. Hamer 25 , G.N. Hamity 53 , E.J. Hampshire 97 , J. Han 63b ,
K. Han 63a , L. Han 114a , L. Han 63a , S. Han 18a , Y.F. Han 158 , K. Hanagaki 85 , M. Hance 139 ,
D.A. Hangal 42 , H. Hanif 145 , M.D. Hank 131 , J.B. Hansen 43 , P.H. Hansen 43 , D. Harada 57 ,
T. Harenberg 174 , S. Harkusha 38 , M.L. Harris 105 , Y.T. Harris 25 , J. Harrison 13 ,
N.M. Harrison 122 , P.F. Harrison170 , N.M. Hartman 112 , N.M. Hartmann 111 , R.Z. Hasan 97,137 ,
Y. Hasegawa 143 , F. Haslbeck 129 , S. Hassan 17 , R. Hauser 109 , C.M. Hawkes 21 ,
R.J. Hawkings 37 , Y. Hayashi 156 , D. Hayden 109 , C. Hayes 108 , R.L. Hayes 117 , C.P. Hays 129 ,
J.M. Hays 96 , H.S. Hayward 94 , F. He 63a , M. He 14,114c , Y. He 49 , Y. He 98 , N.B. Heatley 96 ,
V. Hedberg 100 , A.L. Heggelund 128 , N.D. Hehir 96,* , C. Heidegger 55 , K.K. Heidegger 55 ,
J. Heilman 35 , S. Heim 49 , T. Heim 18a , J.G. Heinlein 131 , J.J. Heinrich 126 , L. Heinrich 112,aa ,
J. Hejbal 134 , A. Held 173 , S. Hellesund 17 , C.M. Helling 167 , S. Hellman 48a,48b ,
R.C.W. Henderson93 , L. Henkelmann 33 , A.M. Henriques Correia37 , H. Herde 100 ,
Y. Hernández Jiménez 148 , L.M. Herrmann 25 , T. Herrmann 51 , G. Herten 55 , R. Hertenberger 111 ,
L. Hervas 37 , M.E. Hesping 102 , N.P. Hessey 159a , M. Hidaoui 36b , N. Hidic 136 , E. Hill 158 ,
S.J. Hillier 21 , J.R. Hinds 109 , F. Hinterkeuser 25 , M. Hirose 127 , S. Hirose 160 ,
D. Hirschbuehl 174 , T.G. Hitchings 103 , B. Hiti 95 , J. Hobbs 148 , R. Hobincu 28e , N. Hod 172 ,
M.C. Hodgkinson 142 , B.H. Hodkinson 129 , A. Hoecker 37 , D.D. Hofer 108 , J. Hofer 166 ,
T. Holm 25 , M. Holzbock 37 , L.B.A.H. Hommels 33 , B.P. Honan 103 , J.J. Hong 69 , J. Hong 63c ,
T.M. Hong 132 , B.H. Hooberman 165 , W.H. Hopkins 6 , M.C. Hoppesch 165 , Y. Horii 113 ,
M.E. Horstmann 112 , S. Hou 151 , A.S. Howard 95 , J. Howarth 60 , J. Hoya 6 , M. Hrabovsky 125 ,
A. Hrynevich 49 , T. Hryn’ova 4 , P.J. Hsu 66 , S.-C. Hsu 141 , T. Hsu 67 , M. Hu 18a , Q. Hu 63a ,
S. Huang 65b , X. Huang 14,114c , Y. Huang 142 , Y. Huang 102 , Y. Huang 14 , Z. Huang 103 ,
Z. Hubacek 135 , M. Huebner 25 , F. Huegging 25 , T.B. Huffman 129 , C.A. Hugli 49 ,
M. Huhtinen 37 , S.K. Huiberts 17 , R. Hulsken 106 , N. Huseynov 12,f , J. Huston 109 , J. Huth 62 ,
R. Hyneman 146 , G. Iacobucci 57 , G. Iakovidis 30 , L. Iconomidou-Fayard 67 , J.P. Iddon 37 ,
P. Iengo 73a,73b , R. Iguchi 156 , Y. Iiyama 156 , T. Iizawa 129 , Y. Ikegami 85 , N. Ilic 158 ,
H. Imam 84c , G. Inacio Goncalves 84d , M. Ince Lezki 57 , T. Ingebretsen Carlson 48a,48b ,
J.M. Inglis 96 , G. Introzzi 74a,74b , M. Iodice 78a , V. Ippolito 76a,76b , R.K. Irwin 94 , M. Ishino 156 ,
W. Islam 173 , C. Issever 19,49 , S. Istin 22a,ag , H. Ito 171 , R. Iuppa 79a,79b , A. Ivina 172 ,
J.M. Izen 46 , V. Izzo 73a , P. Jacka 134 , P. Jackson 1 , C.S. Jagfeld 111 , G. Jain 159a , P. Jain 49 ,
K. Jakobs 55 , T. Jakoubek 172 , J. Jamieson 60 , W. Jang 156 , M. Javurkova 105 , P. Jawahar 103 ,
L. Jeanty 126 , J. Jejelava 152a,y , P. Jenni 55,e , C.E. Jessiman 35 , C. Jia63b , J. Jia 148 , X. Jia 14,114c ,
Z. Jia 114a , C. Jiang 53 , S. Jiggins 49 , J. Jimenez Pena 13 , S. Jin 114a , A. Jinaru 28b ,
O. Jinnouchi 157 , P. Johansson 142 , K.A. Johns 7 , J.W. Johnson 139 , F.A. Jolly 49 ,
D.M. Jones 149 , E. Jones 49 , K.S. Jones8 , P. Jones 33 , R.W.L. Jones 93 , T.J. Jones 94 ,
H.L. Joos 56,37 , R. Joshi 122 , J. Jovicevic 16 , X. Ju 18a , J.J. Junggeburth 105 , T. Junkermann 64a ,
A. Juste Rozas 13,s , M.K. Juzek 88 , S. Kabana 140e , A. Kaczmarska 88 , M. Kado 112 ,
H. Kagan 122 , M. Kagan 146 , A. Kahn 131 , C. Kahra 102 , T. Kaji 156 , E. Kajomovitz 153 ,
N. Kakati 172 , I. Kalaitzidou 55 , C.W. Kalderon 30 , N.J. Kang 139 , D. Kar 34g , K. Karava 129 ,

19

## PDF page 20

M.J. Kareem 159b , E. Karentzos 55 , O. Karkout 117 , S.N. Karpov 39 , Z.M. Karpova 39 ,
V. Kartvelishvili 93 , A.N. Karyukhin 38 , E. Kasimi 155 , J. Katzy 49 , S. Kaur 35 , K. Kawade 143 ,
M.P. Kawale 123 , C. Kawamoto 89 , T. Kawamoto 63a , E.F. Kay 37 , F.I. Kaya 161 , S. Kazakos 109 ,
V.F. Kazanin 38 , Y. Ke 148 , J.M. Keaveney 34a , R. Keeler 168 , G.V. Kehris 62 , J.S. Keller 35 ,
A.S. Kelly98 , J.J. Kempster 149 , P.D. Kennedy 102 , O. Kepka 134 , B.P. Kerridge 137 , S. Kersten 174 ,
B.P. Kerševan 95 , L. Keszeghova 29a , S. Ketabchi Haghighat 158 , R.A. Khan 132 , A. Khanov 124 ,
A.G. Kharlamov 38 , T. Kharlamova 38 , E.E. Khoda 141 , M. Kholodenko 133a , T.J. Khoo 19 ,
G. Khoriauli 169 , J. Khubua 152b,* , Y.A.R. Khwaira 130 , B. Kibirige34g , D. Kim 6 ,
D.W. Kim 48a,48b , Y.K. Kim 40 , N. Kimura 98 , M.K. Kingston 56 , A. Kirchhoff 56 , C. Kirfel 25 ,
F. Kirfel 25 , J. Kirk 137 , A.E. Kiryunin 112 , S. Kita 160 , C. Kitsaki 10 , O. Kivernyk 25 ,
M. Klassen 161 , C. Klein 35 , L. Klein 169 , M.H. Klein 45 , S.B. Klein 57 , U. Klein 94 ,
P. Klimek 37 , A. Klimentov 30 , T. Klioutchnikova 37 , P. Kluit 117 , S. Kluth 112 , E. Kneringer 80 ,
T.M. Knight 158 , A. Knue 50 , D. Kobylianskii 172 , S.F. Koch 129 , M. Kocian 146 , P. Kodyš 136 ,
D.M. Koeck 126 , P.T. Koenig 25 , T. Koffas 35 , O. Kolay 51 , I. Koletsou 4 , T. Komarek 88 ,
K. Köneke 55 , A.X.Y. Kong 1 , T. Kono 121 , N. Konstantinidis 98 , P. Kontaxakis 57 ,
B. Konya 100 , R. Kopeliansky 42 , S. Koperny 87a , K. Korcyl 88 , K. Kordas 155,d , A. Korn 98 ,
S. Korn 56 , I. Korolkov 13 , N. Korotkova 38 , B. Kortman 117 , O. Kortner 112 , S. Kortner 112 ,
W.H. Kostecka 118 , V.V. Kostyukhin 144 , A. Kotsokechagia 37 , A. Kotwal 52 , A. Koulouris 37 ,
A. Kourkoumeli-Charalampidi 74a,74b , C. Kourkoumelis 9 , E. Kourlitis 112,aa , O. Kovanda 126 ,
R. Kowalewski 168 , W. Kozanecki 126 , A.S. Kozhin 38 , V.A. Kramarenko 38 , G. Kramberger 95 ,
P. Kramer 102 , M.W. Krasny 130 , A. Krasznahorkay 37 , A.C. Kraus 118 , J.W. Kraus 174 ,
J.A. Kremer 49 , T. Kresse 51 , L. Kretschmann 174 , J. Kretzschmar 94 , K. Kreul 19 ,
P. Krieger 158 , M. Krivos 136 , K. Krizka 21 , K. Kroeninger 50 , H. Kroha 112 , J. Kroll 134 ,
J. Kroll 131 , K.S. Krowpman 109 , U. Kruchonak 39 , H. Krüger 25 , N. Krumnack82 , M.C. Kruse 52 ,
O. Kuchinskaia 38 , S. Kuday 3a , S. Kuehn 37 , R. Kuesters 55 , T. Kuhl 49 , V. Kukhtin 39 ,
Y. Kulchitsky 38,a , S. Kuleshov 140d,140b , M. Kumar 34g , N. Kumari 49 , P. Kumari 159b ,
A. Kupco 134 , T. Kupfer50 , A. Kupich 38 , O. Kuprash 55 , H. Kurashige 86 , L.L. Kurchaninov 159a ,
O. Kurdysh 67 , Y.A. Kurochkin 38 , A. Kurova 38 , M. Kuze 157 , A.K. Kvam 105 , J. Kvita 125 ,
T. Kwan 106 , N.G. Kyriacou 108 , L.A.O. Laatu 104 , C. Lacasta 166 , F. Lacava 76a,76b ,
H. Lacker 19 , D. Lacour 130 , N.N. Lad 98 , E. Ladygin 39 , A. Lafarge 41 , B. Laforge 130 ,
T. Lagouri 175 , F.Z. Lahbabi 36a , S. Lai 56 , J.E. Lambert 168 , S. Lammers 69 , W. Lampl 7 ,
C. Lampoudis 155,d , G. Lamprinoudis102 , A.N. Lancaster 118 , E. Lançon 30 , U. Landgraf 55 ,
M.P.J. Landon 96 , V.S. Lang 55 , O.K.B. Langrekken 128 , A.J. Lankford 162 , F. Lanni 37 ,
K. Lantzsch 25 , A. Lanza 74a , M. Lanzac Berrocal 166 , J.F. Laporte 138 , T. Lari 72a ,
F. Lasagni Manghi 24b , M. Lassnig 37 , V. Latonova 134 , A. Laurier 153 , S.D. Lawlor 142 ,
Z. Lawrence 103 , R. Lazaridou170 , M. Lazzaroni 72a,72b , B. Le103 , H.D.M. Le 109 ,
E.M. Le Boulicaut 175 , L.T. Le Pottier 18a , B. Leban 24b,24a , A. Lebedev 82 , M. LeBlanc 103 ,
F. Ledroit-Guillon 61 , S.C. Lee 151 , S. Lee 48a,48b , T.F. Lee 94 , L.L. Leeuw 34c , H.P. Lefebvre 97 ,
M. Lefebvre 168 , C. Leggett 18a , G. Lehmann Miotto 37 , M. Leigh 57 , W.A. Leight 105 ,
W. Leinonen 116 , A. Leisos 155,q , M.A.L. Leite 84c , C.E. Leitgeb 19 , R. Leitner 136 ,
K.J.C. Leney 45 , T. Lenz 25 , S. Leone 75a , C. Leonidopoulos 53 , A. Leopold 147 , R. Les 109 ,
C.G. Lester 33 , M. Levchenko 38 , J. Levêque 4 , L.J. Levinson 172 , G. Levrini 24b,24a ,
M.P. Lewicki 88 , C. Lewis 141 , D.J. Lewis 4 , L. Lewitt 142 , A. Li 30 , B. Li 63b , C. Li63a ,
C-Q. Li 112 , H. Li 63a , H. Li 63b , H. Li 114a , H. Li 15 , H. Li 63b , J. Li 63c , K. Li 14 , L. Li 63c ,
M. Li 14,114c , S. Li 14,114c , S. Li 63d,63c , T. Li 5 , X. Li 106 , Z. Li 129 , Z. Li 156 , Z. Li 14,114c ,
Z. Li 63a , S. Liang 14,114c , Z. Liang 14 , M. Liberatore 138 , B. Liberti 77a , K. Lie 65c ,
J. Lieber Marin 84e , H. Lien 69 , H. Lin 108 , K. Lin 109 , R.E. Lindley 7 , J.H. Lindon 2 ,

20

## PDF page 21

J. Ling 62 , E. Lipeles 131 , A. Lipniacka 17 , A. Lister 167 , J.D. Little 69 , B. Liu 14 , B.X. Liu 114b ,
D. Liu 63d,63c , E.H.L. Liu 21 , J.B. Liu 63a , J.K.K. Liu 33 , K. Liu 63d , K. Liu 63d,63c , M. Liu 63a ,
M.Y. Liu 63a , P. Liu 14 , Q. Liu 63d,141,63c , X. Liu 63a , X. Liu 63b , Y. Liu 114b,114c , Y.L. Liu 63b ,
Y.W. Liu 63a , S.L. Lloyd 96 , E.M. Lobodzinska 49 , P. Loch 7 , T. Lohse 19 , K. Lohwasser 142 ,
E. Loiacono 49 , M. Lokajicek 134,* , J.D. Lomas 21 , J.D. Long 165 , I. Longarini 162 ,
R. Longo 165 , I. Lopez Paz 68 , A. Lopez Solis 49 , N.A. Lopez-canelas 7 , N. Lorenzo Martinez 4 ,
A.M. Lory 111 , M. Losada 119a , G. Löschcke Centeno 149 , O. Loseva 38 , X. Lou 48a,48b ,
X. Lou 14,114c , A. Lounis 67 , P.A. Love 93 , G. Lu 14,114c , M. Lu 67 , S. Lu 131 , Y.J. Lu 66 ,
H.J. Lubatti 141 , C. Luci 76a,76b , F.L. Lucio Alves 114a , F. Luehring 69 , O. Lukianchuk 67 ,
B.S. Lunday 131 , O. Lundberg 147 , B. Lund-Jensen 147,* , N.A. Luongo 6 , M.S. Lutz 37 ,
A.B. Lux 26 , D. Lynn 30 , R. Lysak 134 , E. Lytken 100 , V. Lyubushkin 39 , T. Lyubushkina 39 ,
M.M. Lyukova 148 , M.Firdaus M. Soberi 53 , H. Ma 30 , K. Ma 63a , L.L. Ma 63b , W. Ma 63a ,
Y. Ma 124 , J.C. MacDonald 102 , P.C. Machado De Abreu Farias 84e , R. Madar 41 , T. Madula 98 ,
J. Maeda 86 , T. Maeno 30 , H. Maguire 142 , V. Maiboroda 138 , A. Maio 133a,133b,133d , K. Maj 87a ,
O. Majersky 49 , S. Majewski 126 , N. Makovec 67 , V. Maksimovic 16 , B. Malaescu 130 ,
Pa. Malecki 88 , V.P. Maleev 38 , F. Malek 61,m , M. Mali 95 , D. Malito 97 , U. Mallik 81 ,
S. Maltezos10 , S. Malyukov39 , J. Mamuzic 13 , G. Mancini 54 , M.N. Mancini 27 , G. Manco 74a,74b ,
J.P. Mandalia 96 , S.S. Mandarry 149 , I. Mandić 95 , L. Manhaes de Andrade Filho 84a ,
I.M. Maniatis 172 , J. Manjarres Ramos 91 , D.C. Mankad 172 , A. Mann 111 , S. Manzoni 37 ,
L. Mao 63c , X. Mapekula 34c , A. Marantis 155,q , G. Marchiori 5 , M. Marcisovsky 134 ,
C. Marcon 72a , M. Marinescu 21 , S. Marium 49 , M. Marjanovic 123 , A. Markhoos 55 ,
M. Markovitch 67 , E.J. Marshall 93 , Z. Marshall 18a , S. Marti-Garcia 166 , J. Martin 98 ,
T.A. Martin 137 , V.J. Martin 53 , B. Martin dit Latour 17 , L. Martinelli 76a,76b , M. Martinez 13,s ,
P. Martinez Agullo 166 , V.I. Martinez Outschoorn 105 , P. Martinez Suarez 13 , S. Martin-Haugh 137 ,
G. Martinovicova 136 , V.S. Martoiu 28b , A.C. Martyniuk 98 , A. Marzin 37 , D. Mascione 79a,79b ,
L. Masetti 102 , J. Masik 103 , A.L. Maslennikov 38 , P. Massarotti 73a,73b , P. Mastrandrea 75a,75b ,
A. Mastroberardino 44b,44a , T. Masubuchi 127 , T.T. Mathew 126 , T. Mathisen 164 , J. Matousek 136 ,
J. Maurer 28b , T. Maurin 60 , A.J. Maury 67 , B. Maček 95 , D.A. Maximov 38 , A.E. May 103 ,
R. Mazini 151 , I. Maznas 118 , M. Mazza 109 , S.M. Mazza 139 , E. Mazzeo 72a,72b , C. Mc Ginn 30 ,
J.P. Mc Gowan 168 , S.P. Mc Kee 108 , C.C. McCracken 167 , E.F. McDonald 107 ,
A.E. McDougall 117 , J.A. Mcfayden 149 , R.P. McGovern 131 , R.P. Mckenzie 34g ,
T.C. Mclachlan 49 , D.J. Mclaughlin 98 , S.J. McMahon 137 , C.M. Mcpartland 94 ,
R.A. McPherson 168,w , S. Mehlhase 111 , A. Mehta 94 , D. Melini 166 , B.R. Mellado Garcia 34g ,
A.H. Melo 56 , F. Meloni 49 , A.M. Mendes Jacques Da Costa 103 , H.Y. Meng 158 , L. Meng 93 ,
S. Menke 112 , M. Mentink 37 , E. Meoni 44b,44a , G. Mercado 118 , S. Merianos 155 ,
C. Merlassino 70a,70c , L. Merola 73a,73b , C. Meroni 72a,72b , J. Metcalfe 6 , A.S. Mete 6 ,
E. Meuser 102 , C. Meyer 69 , J-P. Meyer 138 , R.P. Middleton 137 , L. Mĳović 53 ,
G. Mikenberg 172 , M. Mikestikova 134 , M. Mikuž 95 , H. Mildner 102 , A. Milic 37 ,
D.W. Miller 40 , E.H. Miller 146 , L.S. Miller 35 , A. Milov 172 , D.A. Milstead48a,48b , T. Min114a ,
A.A. Minaenko 38 , I.A. Minashvili 152b , L. Mince 60 , A.I. Mincer 120 , B. Mindur 87a ,
M. Mineev 39 , Y. Mino 89 , L.M. Mir 13 , M. Miralles Lopez 60 , M. Mironova 18a ,
M.C. Missio 116 , A. Mitra 170 , V.A. Mitsou 166 , Y. Mitsumori 113 , O. Miu 158 ,
P.S. Miyagawa 96 , T. Mkrtchyan 64a , M. Mlinarevic 98 , T. Mlinarevic 98 , M. Mlynarikova 37 ,
S. Mobius 20 , P. Mogg 111 , M.H. Mohamed Farook 115 , A.F. Mohammed 14,114c , S. Mohapatra 42 ,
G. Mokgatitswane 34g , L. Moleri 172 , B. Mondal 144 , S. Mondal 135 , K. Mönig 49 ,
E. Monnier 104 , L. Monsonis Romero166 , J. Montejo Berlingen 13 , A. Montella 48a,48b ,
M. Montella 122 , F. Montereali 78a,78b , F. Monticelli 92 , S. Monzani 70a,70c , A. Morancho Tarda 43 ,

21

## PDF page 22

N. Morange 67 , A.L. Moreira De Carvalho 49 , M. Moreno Llácer 166 , C. Moreno Martinez 57 ,
J.M. Moreno Perez23b , P. Morettini 58b , S. Morgenstern 37 , M. Morii 62 , M. Morinaga 156 ,
F. Morodei 76a,76b , L. Morvaj 37 , P. Moschovakos 37 , B. Moser 129 , M. Mosidze 152b ,
T. Moskalets 45 , P. Moskvitina 116 , J. Moss 32,j , P. Moszkowicz 87a , A. Moussa 36d ,
E.J.W. Moyse 105 , O. Mtintsilana 34g , S. Muanza 104 , J. Mueller 132 , D. Muenstermann 93 ,
R. Müller 37 , G.A. Mullier 164 , A.J. Mullin33 , J.J. Mullin131 , D.P. Mungo 158 , D. Munoz Perez 166 ,
F.J. Munoz Sanchez 103 , M. Murin 103 , W.J. Murray 170,137 , M. Muškinja 95 , C. Mwewa 30 ,
A.G. Myagkov 38,a , A.J. Myers 8 , G. Myers 108 , M. Myska 135 , B.P. Nachman 18a ,
O. Nackenhorst 50 , K. Nagai 129 , K. Nagano 85 , J.L. Nagle 30,ae , E. Nagy 104 , A.M. Nairz 37 ,
Y. Nakahama 85 , K. Nakamura 85 , K. Nakkalil 5 , H. Nanjo 127 , E.A. Narayanan 115 ,
I. Naryshkin 38 , L. Nasella 72a,72b , M. Naseri 35 , S. Nasri 119b , C. Nass 25 , G. Navarro 23a ,
J. Navarro-Gonzalez 166 , R. Nayak 154 , A. Nayaz 19 , P.Y. Nechaeva 38 , S. Nechaeva 24b,24a ,
F. Nechansky 134 , L. Nedic 129 , T.J. Neep 21 , A. Negri 74a,74b , M. Negrini 24b , C. Nellist 117 ,
C. Nelson 106 , K. Nelson 108 , S. Nemecek 134 , M. Nessi 37,g , M.S. Neubauer 165 ,
F. Neuhaus 102 , J. Neundorf 49 , J. Newell 94 , P.R. Newman 21 , C.W. Ng 132 , Y.W.Y. Ng 49 ,
B. Ngair 119a , H.D.N. Nguyen 110 , R.B. Nickerson 129 , R. Nicolaidou 138 , J. Nielsen 139 ,
M. Niemeyer 56 , J. Niermann 56 , N. Nikiforou 37 , V. Nikolaenko 38,a , I. Nikolic-Audit 130 ,
K. Nikolopoulos 21 , P. Nilsson 30 , I. Ninca 49 , G. Ninio 154 , A. Nisati 76a , N. Nishu 2 ,
R. Nisius 112 , J-E. Nitschke 51 , E.K. Nkadimeng 34g , T. Nobe 156 , T. Nommensen 150 ,
M.B. Norfolk 142 , B.J. Norman 35 , M. Noury 36a , J. Novak 95 , T. Novak 95 , L. Novotny 135 ,
R. Novotny 115 , L. Nozka 125 , K. Ntekas 162 , N.M.J. Nunes De Moura Junior 84b , J. Ocariz 130 ,
A. Ochi 86 , I. Ochoa 133a , S. Oerdek 49,t , J.T. Offermann 40 , A. Ogrodnik 136 , A. Oh 103 ,
C.C. Ohm 147 , H. Oide 85 , R. Oishi 156 , M.L. Ojeda 37 , Y. Okumura 156 ,
L.F. Oleiro Seabra 133a , I. Oleksiyuk 57 , S.A. Olivares Pino 140d , G. Oliveira Correa 13 ,
D. Oliveira Damazio 30 , J.L. Oliver 162 , Ö.O. Öncel 55 , A.P. O’Neill 20 , A. Onofre 133a,133e ,
P.U.E. Onyisi 11 , M.J. Oreglia 40 , G.E. Orellana 92 , D. Orestano 78a,78b , N. Orlando 13 ,
R.S. Orr 158 , L.M. Osojnak 131 , R. Ospanov 63a , G. Otero y Garzon 31 , H. Otono 90 , P.S. Ott 64a ,
G.J. Ottino 18a , M. Ouchrif 36d , F. Ould-Saada 128 , T. Ovsiannikova 141 , M. Owen 60 ,
R.E. Owen 137 , V.E. Ozcan 22a , F. Ozturk 88 , N. Ozturk 8 , S. Ozturk 83 , H.A. Pacey 129 ,
A. Pacheco Pages 13 , C. Padilla Aranda 13 , G. Padovano 76a,76b , S. Pagan Griso 18a ,
G. Palacino 69 , A. Palazzo 71a,71b , J. Pampel 25 , J. Pan 175 , T. Pan 65a , D.K. Panchal 11 ,
C.E. Pandini 117 , J.G. Panduro Vazquez 137 , H.D. Pandya 1 , H. Pang 15 , P. Pani 49 ,
G. Panizzo 70a,70c , L. Panwar 130 , L. Paolozzi 57 , S. Parajuli 165 , A. Paramonov 6 ,
C. Paraskevopoulos 54 , D. Paredes Hernandez 65b , A. Pareti 74a,74b , K.R. Park 42 , T.H. Park 158 ,
M.A. Parker 33 , F. Parodi 58b,58a , E.W. Parrish 118 , V.A. Parrish 53 , J.A. Parsons 42 ,
U. Parzefall 55 , B. Pascual Dias 110 , L. Pascual Dominguez 101 , E. Pasqualucci 76a ,
S. Passaggio 58b , F. Pastore 97 , P. Patel 88 , U.M. Patel 52 , J.R. Pater 103 , T. Pauly 37 ,
C.I. Pazos 161 , J. Pearkes 146 , M. Pedersen 128 , R. Pedro 133a , S.V. Peleganchuk 38 , O. Penc 37 ,
E.A. Pender 53 , S. Peng15 , G.D. Penn 175 , K.E. Penski 111 , M. Penzin 38 , B.S. Peralva 84d ,
A.P. Pereira Peixoto 141 , L. Pereira Sanchez 146 , D.V. Perepelitsa 30,ae , G. Perera 105 ,
E. Perez Codina 159a , M. Perganti 10 , H. Pernegger 37 , S. Perrella 76a,76b , O. Perrin 41 ,
K. Peters 49 , R.F.Y. Peters 103 , B.A. Petersen 37 , T.C. Petersen 43 , E. Petit 104 , V. Petousis 135 ,
C. Petridou 155,d , T. Petru 136 , A. Petrukhin 144 , M. Pettee 18a , A. Petukhov 38 , K. Petukhova 37 ,
R. Pezoa 140f , L. Pezzotti 37 , G. Pezzullo 175 , A.J. Pfleger 37 , T.M. Pham 173 , T. Pham 107 ,
P.W. Phillips 137 , G. Piacquadio 148 , E. Pianori 18a , F. Piazza 126 , R. Piegaia 31 , D. Pietreanu 28b ,
A.D. Pilkington 103 , M. Pinamonti 70a,70c , J.L. Pinfold 2 , B.C. Pinheiro Pereira 133a ,
J. Pinol Bel 13 , A.E. Pinto Pinoargote 138,138 , L. Pintucci 70a,70c , K.M. Piper 149 , A. Pirttikoski 57 ,

22

## PDF page 23

D.A. Pizzi 35 , L. Pizzimento 65b , A. Pizzini 117 , M.-A. Pleier 30 , V. Pleskot 136 , E. Plotnikova39 ,
G. Poddar 96 , R. Poettgen 100 , L. Poggioli 130 , I. Pokharel 56 , S. Polacek 136 , G. Polesello 74a ,
A. Poley 145,159a , A. Polini 24b , C.S. Pollard 170 , Z.B. Pollock 122 , E. Pompa Pacchi 76a,76b ,
N.I. Pond 98 , D. Ponomarenko 69 , L. Pontecorvo 37 , S. Popa 28a , G.A. Popeneciu 28d ,
A. Poreba 37 , D.M. Portillo Quintero 159a , S. Pospisil 135 , M.A. Postill 142 , P. Postolache 28c ,
K. Potamianos 170 , P.A. Potepa 87a , I.N. Potrap 39 , C.J. Potter 33 , H. Potti 150 , J. Poveda 166 ,
M.E. Pozo Astigarraga 37 , A. Prades Ibanez 77a,77b , J. Pretel 168 , D. Price 103 , M. Primavera 71a ,
L. Primomo 70a,70c , M.A. Principe Martin 101 , R. Privara 125 , T. Procter 60 , M.L. Proffitt 141 ,
N. Proklova 131 , K. Prokofiev 65c , G. Proto 112 , J. Proudfoot 6 , M. Przybycien 87a ,
W.W. Przygoda 87b , A. Psallidas 47 , J.E. Puddefoot 142 , D. Pudzha 55 , D. Pyatiizbyantseva 38 ,
J. Qian 108 , D. Qichen 103 , Y. Qin 13 , T. Qiu 53 , A. Quadt 56 , M. Queitsch-Maitland 103 ,
G. Quetant 57 , R.P. Quinn 167 , G. Rabanal Bolanos 62 , D. Rafanoharana 55 , F. Raffaeli 77a,77b ,
F. Ragusa 72a,72b , J.L. Rainbolt 40 , J.A. Raine 57 , S. Rajagopalan 30 , E. Ramakoti 38 ,
L. Rambelli 58b,58a , I.A. Ramirez-Berend 35 , K. Ran 49,114c , D.S. Rankin 131 , N.P. Rapheeha 34g ,
H. Rasheed 28b , V. Raskina 130 , D.F. Rassloff 64a , A. Rastogi 18a , S. Rave 102 , S. Ravera 58b,58a ,
B. Ravina 56 , I. Ravinovich 172 , M. Raymond 37 , A.L. Read 128 , N.P. Readioff 142 ,
D.M. Rebuzzi 74a,74b , G. Redlinger 30 , A.S. Reed 112 , K. Reeves 27 , J.A. Reidelsturz 174 ,
D. Reikher 126 , A. Rej 50 , C. Rembser 37 , M. Renda 28b , F. Renner 49 , A.G. Rennie 162 ,
A.L. Rescia 49 , S. Resconi 72a , M. Ressegotti 58b,58a , S. Rettie 37 , J.G. Reyes Rivera 109 ,
E. Reynolds 18a , O.L. Rezanova 38 , P. Reznicek 136 , H. Riani 36d , N. Ribaric 52 , E. Ricci 79a,79b ,
R. Richter 112 , S. Richter 48a,48b , E. Richter-Was 87b , M. Ridel 130 , S. Ridouani 36d , P. Rieck 120 ,
P. Riedler 37 , E.M. Riefel 48a,48b , J.O. Rieger 117 , M. Rĳssenbeek 148 , M. Rimoldi 37 ,
L. Rinaldi 24b,24a , P. Rincke 56,164 , T.T. Rinn 30 , M.P. Rinnagel 111 , G. Ripellino 164 , I. Riu 13 ,
J.C. Rivera Vergara 168 , F. Rizatdinova 124 , E. Rizvi 96 , B.R. Roberts 18a , S.S. Roberts 139 ,
S.H. Robertson 106,w , D. Robinson 33 , M. Robles Manzano 102 , A. Robson 60 , A. Rocchi 77a,77b ,
C. Roda 75a,75b , S. Rodriguez Bosca 37 , Y. Rodriguez Garcia 23a , A. Rodriguez Rodriguez 55 ,
A.M. Rodríguez Vera 118 , S. Roe37 , J.T. Roemer 37 , A.R. Roepe-Gier 139 , O. Røhne 128 ,
R.A. Rojas 105 , C.P.A. Roland 130 , J. Roloff 30 , A. Romaniouk 38 , E. Romano 74a,74b ,
M. Romano 24b , A.C. Romero Hernandez 165 , N. Rompotis 94 , L. Roos 130 , S. Rosati 76a ,
B.J. Rosser 40 , E. Rossi 129 , E. Rossi 73a,73b , L.P. Rossi 62 , L. Rossini 55 , R. Rosten 122 ,
M. Rotaru 28b , B. Rottler 55 , C. Rougier 91 , D. Rousseau 67 , D. Rousso 49 , A. Roy 165 ,
S. Roy-Garand 158 , A. Rozanov 104 , Z.M.A. Rozario 60 , Y. Rozen 153 , A. Rubio Jimenez 166 ,
A.J. Ruby 94 , V.H. Ruelas Rivera 19 , T.A. Ruggeri 1 , A. Ruggiero 129 , A. Ruiz-Martinez 166 ,
A. Rummler 37 , Z. Rurikova 55 , N.A. Rusakovich 39 , H.L. Russell 168 , G. Russo 76a,76b ,
J.P. Rutherfoord 7 , S. Rutherford Colmenares 33 , M. Rybar 136 , E.B. Rye 128 , A. Ryzhov 45 ,
J.A. Sabater Iglesias 57 , H.F-W. Sadrozinski 139 , F. Safai Tehrani 76a , B. Safarzadeh Samani 137 ,
S. Saha 1 , M. Sahinsoy 83 , A. Saibel 166 , M. Saimpert 138 , M. Saito 156 , T. Saito 156 ,
A. Sala 72a,72b , D. Salamani 37 , A. Salnikov 146 , J. Salt 166 , A. Salvador Salas 154 ,
D. Salvatore 44b,44a , F. Salvatore 149 , A. Salzburger 37 , D. Sammel 55 , E. Sampson 93 ,
D. Sampsonidis 155,d , D. Sampsonidou 126 , J. Sánchez 166 , V. Sanchez Sebastian 166 ,
H. Sandaker 128 , C.O. Sander 49 , J.A. Sandesara 105 , M. Sandhoff 174 , C. Sandoval 23b ,
L. Sanfilippo 64a , D.P.C. Sankey 137 , T. Sano 89 , A. Sansoni 54 , L. Santi 37,76b , C. Santoni 41 ,
H. Santos 133a,133b , A. Santra 172 , E. Sanzani 24b,24a , K.A. Saoucha 163 , J.G. Saraiva 133a,133d ,
J. Sardain 7 , O. Sasaki 85 , K. Sato 160 , C. Sauer64b , E. Sauvan 4 , P. Savard 158,ac , R. Sawada 156 ,
C. Sawyer 137 , L. Sawyer 99 , C. Sbarra 24b , A. Sbrizzi 24b,24a , T. Scanlon 98 ,
J. Schaarschmidt 141 , U. Schäfer 102 , A.C. Schaffer 67,45 , D. Schaile 111 , R.D. Schamberger 148 ,
C. Scharf 19 , M.M. Schefer 20 , V.A. Schegelsky 38 , D. Scheirich 136 , M. Schernau 162 ,

23

## PDF page 24

C. Scheulen 56 , C. Schiavi 58b,58a , M. Schioppa 44b,44a , B. Schlag 146,l , K.E. Schleicher 55 ,
S. Schlenker 37 , J. Schmeing 174 , M.A. Schmidt 174 , K. Schmieden 102 , C. Schmitt 102 ,
N. Schmitt 102 , S. Schmitt 49 , L. Schoeffel 138 , A. Schoening 64b , P.G. Scholer 35 , E. Schopf 129 ,
M. Schott 25 , J. Schovancova 37 , S. Schramm 57 , T. Schroer 57 , H-C. Schultz-Coulon 64a ,
M. Schumacher 55 , B.A. Schumm 139 , Ph. Schune 138 , A.J. Schuy 141 , H.R. Schwartz 139 ,
A. Schwartzman 146 , T.A. Schwarz 108 , Ph. Schwemling 138 , R. Schwienhorst 109 ,
F.G. Sciacca 20 , A. Sciandra 30 , G. Sciolla 27 , F. Scuri 75a , C.D. Sebastiani 94 , K. Sedlaczek 118 ,
S.C. Seidel 115 , A. Seiden 139 , B.D. Seidlitz 42 , C. Seitz 49 , J.M. Seixas 84b , G. Sekhniaidze 73a ,
L. Selem 61 , N. Semprini-Cesari 24b,24a , D. Sengupta 57 , V. Senthilkumar 166 , L. Serin 67 ,
M. Sessa 77a,77b , H. Severini 123 , F. Sforza 58b,58a , A. Sfyrla 57 , Q. Sha 14 , E. Shabalina 56 ,
A.H. Shah 33 , R. Shaheen 147 , J.D. Shahinian 131 , D. Shaked Renous 172 , L.Y. Shan 14 ,
M. Shapiro 18a , A. Sharma 37 , A.S. Sharma 167 , P. Sharma 81 , P.B. Shatalov 38 , K. Shaw 149 ,
S.M. Shaw 103 , Q. Shen 63c , D.J. Sheppard 145 , P. Sherwood 98 , L. Shi 98 , X. Shi 14 ,
S. Shimizu 85 , C.O. Shimmin 175 , J.D. Shinner 97 , I.P.J. Shipsey 129 , S. Shirabe 90 ,
M. Shiyakova 39,u , M.J. Shochet 40 , D.R. Shope 128 , B. Shrestha 123 , S. Shrestha 122,af ,
I. Shreyber 38 , M.J. Shroff 168 , P. Sicho 134 , A.M. Sickles 165 , E. Sideras Haddad 34g ,
A.C. Sidley 117 , A. Sidoti 24b , F. Siegert 51 , Dj. Sĳacki 16 , F. Sili 92 , J.M. Silva 53 ,
I. Silva Ferreira 84b , M.V. Silva Oliveira 30 , S.B. Silverstein 48a , S. Simion67 , R. Simoniello 37 ,
E.L. Simpson 103 , H. Simpson 149 , L.R. Simpson 108 , N.D. Simpson100 , S. Simsek 83 ,
S. Sindhu 56 , P. Sinervo 158 , S. Singh 158 , S. Sinha 49 , S. Sinha 103 , M. Sioli 24b,24a , I. Siral 37 ,
E. Sitnikova 49 , J. Sjölin 48a,48b , A. Skaf 56 , E. Skorda 21 , P. Skubic 123 , M. Slawinska 88 ,
V. Smakhtin172 , B.H. Smart 137 , S.Yu. Smirnov 38 , Y. Smirnov 38 , L.N. Smirnova 38,a ,
O. Smirnova 100 , A.C. Smith 42 , D.R. Smith162 , E.A. Smith 40 , J.L. Smith 103 , R. Smith146 ,
M. Smizanska 93 , K. Smolek 135 , A.A. Snesarev 38 , H.L. Snoek 117 , S. Snyder 30 ,
R. Sobie 168,w , A. Soffer 154 , C.A. Solans Sanchez 37 , E.Yu. Soldatov 38 , U. Soldevila 166 ,
A.A. Solodkov 38 , S. Solomon 27 , A. Soloshenko 39 , K. Solovieva 55 , O.V. Solovyanov 41 ,
P. Sommer 51 , A. Sonay 13 , W.Y. Song 159b , A. Sopczak 135 , A.L. Sopio 98 , F. Sopkova 29b ,
J.D. Sorenson 115 , I.R. Sotarriva Alvarez 157 , V. Sothilingam64a , O.J. Soto Sandoval 140c,140b ,
S. Sottocornola 69 , R. Soualah 163 , Z. Soumaimi 36e , D. South 49 , N. Soybelman 172 ,
S. Spagnolo 71a,71b , M. Spalla 112 , D. Sperlich 55 , G. Spigo 37 , B. Spisso 73a,73b , D.P. Spiteri 60 ,
M. Spousta 136 , E.J. Staats 35 , R. Stamen 64a , A. Stampekis 21 , E. Stanecka 88 ,
W. Stanek-Maslouska 49 , M.V. Stange 51 , B. Stanislaus 18a , M.M. Stanitzki 49 , B. Stapf 49 ,
E.A. Starchenko 38 , G.H. Stark 139 , J. Stark 91 , P. Staroba 134 , P. Starovoitov 64a , S. Stärz 106 ,
R. Staszewski 88 , G. Stavropoulos 47 , P. Steinberg 30 , B. Stelzer 145,159a , H.J. Stelzer 132 ,
O. Stelzer-Chilton 159a , H. Stenzel 59 , T.J. Stevenson 149 , G.A. Stewart 37 , J.R. Stewart 124 ,
M.C. Stockton 37 , G. Stoicea 28b , M. Stolarski 133a , S. Stonjek 112 , A. Straessner 51 ,
J. Strandberg 147 , S. Strandberg 48a,48b , M. Stratmann 174 , M. Strauss 123 , T. Strebler 104 ,
P. Strizenec 29b , R. Ströhmer 169 , D.M. Strom 126 , R. Stroynowski 45 , A. Strubig 48a,48b ,
S.A. Stucci 30 , B. Stugu 17 , J. Stupak 123 , N.A. Styles 49 , D. Su 146 , S. Su 63a , W. Su 63d ,
X. Su 63a , D. Suchy 29a , K. Sugizaki 156 , V.V. Sulin 38 , M.J. Sullivan 94 , D.M.S. Sultan 129 ,
L. Sultanaliyeva 38 , S. Sultansoy 3b , T. Sumida 89 , S. Sun 173 , O. Sunneborn Gudnadottir 164 ,
N. Sur 104 , M.R. Sutton 149 , H. Suzuki 160 , M. Svatos 134 , M. Swiatlowski 159a , T. Swirski 169 ,
I. Sykora 29a , M. Sykora 136 , T. Sykora 136 , D. Ta 102 , K. Tackmann 49,t , A. Taffard 162 ,
R. Tafirout 159a , J.S. Tafoya Vargas 67 , Y. Takubo 85 , M. Talby 104 , A.A. Talyshev 38 ,
K.C. Tam 65b , N.M. Tamir154 , A. Tanaka 156 , J. Tanaka 156 , R. Tanaka 67 , M. Tanasini 148 ,
Z. Tao 167 , S. Tapia Araya 140f , S. Tapprogge 102 , A. Tarek Abouelfadl Mohamed 109 ,
S. Tarem 153 , K. Tariq 14 , G. Tarna 28b , G.F. Tartarelli 72a , M.J. Tartarin 91 , P. Tas 136 ,

24

## PDF page 25

M. Tasevsky 134 , E. Tassi 44b,44a , A.C. Tate 165 , G. Tateno 156 , Y. Tayalati 36e,v , G.N. Taylor 107 ,
W. Taylor 159b , R. Teixeira De Lima 146 , P. Teixeira-Dias 97 , J.J. Teoh 158 , K. Terashi 156 ,
J. Terron 101 , S. Terzo 13 , M. Testa 54 , R.J. Teuscher 158,w , A. Thaler 80 , O. Theiner 57 ,
T. Theveneaux-Pelzer 104 , O. Thielmann 174 , D.W. Thomas97 , J.P. Thomas 21 , E.A. Thompson 18a ,
P.D. Thompson 21 , E. Thomson 131 , R.E. Thornberry 45 , C. Tian 63a , Y. Tian 56 ,
V. Tikhomirov 38,a , Yu.A. Tikhonov 38 , S. Timoshenko38 , D. Timoshyn 136 , E.X.L. Ting 1 ,
P. Tipton 175 , A. Tishelman-Charny 30 , S.H. Tlou 34g , K. Todome 157 , S. Todorova-Nova 136 ,
S. Todt51 , L. Toffolin 70a,70c , M. Togawa 85 , J. Tojo 90 , S. Tokár 29a , K. Tokushuku 85 ,
O. Toldaiev 69 , M. Tomoto 85,113 , L. Tompkins 146,l , K.W. Topolnicki 87b , E. Torrence 126 ,
H. Torres 91 , E. Torró Pastor 166 , M. Toscani 31 , C. Tosciri 40 , M. Tost 11 , D.R. Tovey 142 ,
I.S. Trandafir 28b , T. Trefzger 169 , A. Tricoli 30 , I.M. Trigger 159a , S. Trincaz-Duvoid 130 ,
D.A. Trischuk 27 , B. Trocmé 61 , A. Tropina39 , L. Truong 34c , M. Trzebinski 88 , A. Trzupek 88 ,
F. Tsai 148 , M. Tsai 108 , A. Tsiamis 155 , P.V. Tsiareshka38 , S. Tsigaridas 159a , A. Tsirigotis 155,q ,
V. Tsiskaridze 158 , E.G. Tskhadadze 152a , M. Tsopoulou 155 , Y. Tsujikawa 89 , I.I. Tsukerman 38 ,
V. Tsulaia 18a , S. Tsuno 85 , K. Tsuri 121 , D. Tsybychev 148 , Y. Tu 65b , A. Tudorache 28b ,
V. Tudorache 28b , A.N. Tuna 62 , S. Turchikhin 58b,58a , I. Turk Cakir 3a , R. Turra 72a ,
T. Turtuvshin 39 , P.M. Tuts 42 , S. Tzamarias 155,d , E. Tzovara 102 , F. Ukegawa 160 ,
P.A. Ulloa Poblete 140c,140b , E.N. Umaka 30 , G. Unal 37 , A. Undrus 30 , G. Unel 162 , J. Urban 29b ,
P. Urrejola 140a , G. Usai 8 , R. Ushioda 157 , M. Usman 110 , F. Ustuner 53 , Z. Uysal 83 ,
V. Vacek 135 , B. Vachon 106 , T. Vafeiadis 37 , A. Vaitkus 98 , C. Valderanis 111 ,
E. Valdes Santurio 48a,48b , M. Valente 159a , S. Valentinetti 24b,24a , A. Valero 166 ,
E. Valiente Moreno 166 , A. Vallier 91 , J.A. Valls Ferrer 166 , D.R. Van Arneman 117 ,
T.R. Van Daalen 141 , A. Van Der Graaf 50 , P. Van Gemmeren 6 , M. Van Rĳnbach 37 ,
S. Van Stroud 98 , I. Van Vulpen 117 , P. Vana 136 , M. Vanadia 77a,77b , W. Vandelli 37 ,
E.R. Vandewall 124 , D. Vannicola 154 , L. Vannoli 54 , R. Vari 76a , E.W. Varnes 7 , C. Varni 18b ,
T. Varol 151 , D. Varouchas 67 , L. Varriale 166 , K.E. Varvell 150 , M.E. Vasile 28b , L. Vaslin85 ,
G.A. Vasquez 168 , A. Vasyukov 39 , L.M. Vaughan 124 , R. Vavricka102 , T. Vazquez Schroeder 37 ,
J. Veatch 32 , V. Vecchio 103 , M.J. Veen 105 , I. Veliscek 30 , L.M. Veloce 158 , F. Veloso 133a,133c ,
S. Veneziano 76a , A. Ventura 71a,71b , S. Ventura Gonzalez 138 , A. Verbytskyi 112 ,
M. Verducci 75a,75b , C. Vergis 96 , M. Verissimo De Araujo 84b , W. Verkerke 117 ,
J.C. Vermeulen 117 , C. Vernieri 146 , M. Vessella 105 , M.C. Vetterli 145,ac , A. Vgenopoulos 102 ,
N. Viaux Maira 140f , T. Vickey 142 , O.E. Vickey Boeriu 142 , G.H.A. Viehhauser 129 , L. Vigani 64b ,
M. Vigl 112 , M. Villa 24b,24a , M. Villaplana Perez 166 , E.M. Villhauer53 , E. Vilucchi 54 ,
M.G. Vincter 35 , A. Visibile117 , C. Vittori 37 , I. Vivarelli 24b,24a , E. Voevodina 112 , F. Vogel 111 ,
J.C. Voigt 51 , P. Vokac 135 , Yu. Volkotrub 87b , J. Von Ahnen 49 , E. Von Toerne 25 ,
B. Vormwald 37 , V. Vorobel 136 , K. Vorobev 38 , M. Vos 166 , K. Voss 144 , M. Vozak 117 ,
L. Vozdecky 123 , N. Vranjes 16 , M. Vranjes Milosavljevic 16 , M. Vreeswĳk 117 , N.K. Vu 63d,63c ,
R. Vuillermet 37 , O. Vujinovic 102 , I. Vukotic 40 , I.K. Vyas 35 , S. Wada 160 , C. Wagner105 ,
J.M. Wagner 18a , W. Wagner 174 , S. Wahdan 174 , H. Wahlberg 92 , J. Walder 137 , R. Walker 111 ,
W. Walkowiak 144 , A. Wall 131 , E.J. Wallin 100 , T. Wamorkar 6 , A.Z. Wang 139 , C. Wang 102 ,
C. Wang 11 , H. Wang 18a , J. Wang 65c , P. Wang 98 , R. Wang 62 , R. Wang 6 , S.M. Wang 151 ,
S. Wang 63b , S. Wang 14 , T. Wang 63a , W.T. Wang 81 , W. Wang 14 , X. Wang 114a , X. Wang 165 ,
X. Wang 63c , Y. Wang 63d , Y. Wang 114a , Y. Wang 63a , Z. Wang 108 , Z. Wang 63d,52,63c ,
Z. Wang 108 , A. Warburton 106 , R.J. Ward 21 , N. Warrack 60 , S. Waterhouse 97 , A.T. Watson 21 ,
H. Watson 53 , M.F. Watson 21 , E. Watton 60,137 , G. Watts 141 , B.M. Waugh 98 , J.M. Webb 55 ,
C. Weber 30 , H.A. Weber 19 , M.S. Weber 20 , S.M. Weber 64a , C. Wei 63a , Y. Wei 55 ,
A.R. Weidberg 129 , E.J. Weik 120 , J. Weingarten 50 , C. Weiser 55 , C.J. Wells 49 , T. Wenaus 30 ,

25

## PDF page 26

B. Wendland 50 , T. Wengler 37 , N.S. Wenke112 , N. Wermes 25 , M. Wessels 64a , A.M. Wharton 93 ,
A.S. White 62 , A. White 8 , M.J. White 1 , D. Whiteson 162 , L. Wickremasinghe 127 ,
W. Wiedenmann 173 , M. Wielers 137 , C. Wiglesworth 43 , D.J. Wilbern123 , H.G. Wilkens 37 ,
J.J.H. Wilkinson 33 , D.M. Williams 42 , H.H. Williams131 , S. Williams 33 , S. Willocq 105 ,
B.J. Wilson 103 , P.J. Windischhofer 40 , F.I. Winkel 31 , F. Winklmeier 126 , B.T. Winter 55 ,
J.K. Winter 103 , M. Wittgen146 , M. Wobisch 99 , T. Wojtkowski61 , Z. Wolffs 117 , J. Wollrath162 ,
M.W. Wolter 88 , H. Wolters 133a,133c , M.C. Wong139 , E.L. Woodward 42 , S.D. Worm 49 ,
B.K. Wosiek 88 , K.W. Woźniak 88 , S. Wozniewski 56 , K. Wraight 60 , C. Wu 21 , M. Wu 114b ,
M. Wu 116 , S.L. Wu 173 , S. Wu 14 , X. Wu 57 , Y. Wu 63a , Z. Wu 4 , J. Wuerzinger 112,aa ,
T.R. Wyatt 103 , B.M. Wynne 53 , S. Xella 43 , L. Xia 114a , M. Xia 15 , M. Xie 63a , S. Xin 14,114c ,
A. Xiong 126 , J. Xiong 18a , D. Xu 14 , H. Xu 63a , L. Xu 63a , R. Xu 131 , T. Xu 108 , Y. Xu 15 ,
Z. Xu 53 , Z. Xu114a , B. Yabsley 150 , S. Yacoob 34a , Y. Yamaguchi 85 , E. Yamashita 156 ,
H. Yamauchi 160 , T. Yamazaki 18a , Y. Yamazaki 86 , J. Yan63c , S. Yan 60 , Z. Yan 105 ,
H.J. Yang 63c,63d , H.T. Yang 63a , S. Yang 63a , T. Yang 65c , X. Yang 37 , X. Yang 14 , Y. Yang 45 ,
Y. Yang63a , Z. Yang 63a , W-M. Yao 18a , H. Ye 114a , H. Ye 56 , J. Ye 14 , S. Ye 30 , X. Ye 63a ,
Y. Yeh 98 , I. Yeletskikh 39 , B.K. Yeo 18b , M.R. Yexley 98 , T.P. Yildirim 129 , P. Yin 42 ,
K. Yorita 171 , S. Younas 28b , C.J.S. Young 37 , C. Young 146 , C. Yu 14,114c , Y. Yu 63a ,
J. Yuan 14,114c , M. Yuan 108 , R. Yuan 63d,63c , L. Yue 98 , M. Zaazoua 63a , B. Zabinski 88 ,
E. Zaid53 , Z.K. Zak 88 , T. Zakareishvili 166 , S. Zambito 57 , J.A. Zamora Saa 140d,140b , J. Zang 156 ,
D. Zanzi 55 , O. Zaplatilek 135 , C. Zeitnitz 174 , H. Zeng 14 , J.C. Zeng 165 , D.T. Zenger Jr 27 ,
O. Zenin 38 , T. Ženiš 29a , S. Zenz 96 , S. Zerradi 36a , D. Zerwas 67 , M. Zhai 14,114c ,
D.F. Zhang 142 , J. Zhang 63b , J. Zhang 6 , K. Zhang 14,114c , L. Zhang 63a , L. Zhang 114a ,
P. Zhang 14,114c , R. Zhang 173 , S. Zhang 108 , S. Zhang 91 , T. Zhang 156 , X. Zhang 63c ,
X. Zhang 63b , Y. Zhang 63c , Y. Zhang 98 , Y. Zhang 114a , Z. Zhang 18a , Z. Zhang 63b ,
Z. Zhang 67 , H. Zhao 141 , T. Zhao 63b , Y. Zhao 139 , Z. Zhao 63a , Z. Zhao 63a ,
A. Zhemchugov 39 , J. Zheng 114a , K. Zheng 165 , X. Zheng 63a , Z. Zheng 146 , D. Zhong 165 ,
B. Zhou 108 , H. Zhou 7 , N. Zhou 63c , Y. Zhou15 , Y. Zhou 114a , Y. Zhou7 , C.G. Zhu 63b ,
J. Zhu 108 , X. Zhu63d , Y. Zhu 63c , Y. Zhu 63a , X. Zhuang 14 , K. Zhukov 69 , N.I. Zimine 39 ,
J. Zinsser 64b , M. Ziolkowski 144 , L. Živković 16 , A. Zoccoli 24b,24a , K. Zoch 62 ,
T.G. Zorbas 142 , O. Zormpa 47 , W. Zou 42 , L. Zwalinski 37 .
1 Department of Physics, University of Adelaide, Adelaide; Australia.
2 Department of Physics, University of Alberta, Edmonton AB; Canada.
3 (𝑎) Department of Physics, Ankara University, Ankara; (𝑏) Division of Physics, TOBB University of

Economics and Technology, Ankara; Türkiye.
4 LAPP, Université Savoie Mont Blanc, CNRS/IN2P3, Annecy; France.
5 APC, Université Paris Cité, CNRS/IN2P3, Paris; France.
6 High Energy Physics Division, Argonne National Laboratory, Argonne IL; United States of America.
7 Department of Physics, University of Arizona, Tucson AZ; United States of America.
8 Department of Physics, University of Texas at Arlington, Arlington TX; United States of America.
9 Physics Department, National and Kapodistrian University of Athens, Athens; Greece.
10 Physics Department, National Technical University of Athens, Zografou; Greece.
11 Department of Physics, University of Texas at Austin, Austin TX; United States of America.
12 Institute of Physics, Azerbaĳan Academy of Sciences, Baku; Azerbaĳan.
13 Institut de Física d’Altes Energies (IFAE), Barcelona Institute of Science and Technology, Barcelona;

Spain.
14 Institute of High Energy Physics, Chinese Academy of Sciences, Beĳing; China.

26

## PDF page 27

15 Physics Department, Tsinghua University, Beĳing; China.
16 Institute of Physics, University of Belgrade, Belgrade; Serbia.
17 Department for Physics and Technology, University of Bergen, Bergen; Norway.
18 (𝑎) Physics Division, Lawrence Berkeley National Laboratory, Berkeley CA; (𝑏) University of California,

Berkeley CA; United States of America.
19 Institut für Physik, Humboldt Universität zu Berlin, Berlin; Germany.
20 Albert Einstein Center for Fundamental Physics and Laboratory for High Energy Physics, University of

Bern, Bern; Switzerland.
21 School of Physics and Astronomy, University of Birmingham, Birmingham; United Kingdom.
22 (𝑎) Department of Physics, Bogazici University, Istanbul; (𝑏) Department of Physics Engineering,
Gaziantep University, Gaziantep; (𝑐) Department of Physics, Istanbul University, Istanbul; Türkiye.
23 (𝑎) Facultad de Ciencias y Centro de Investigaciónes, Universidad Antonio Nariño,
Bogotá; (𝑏) Departamento de Física, Universidad Nacional de Colombia, Bogotá; Colombia.
24 (𝑎) Dipartimento di Fisica e Astronomia A. Righi, Università di Bologna, Bologna; (𝑏) INFN Sezione di
Bologna; Italy.
25 Physikalisches Institut, Universität Bonn, Bonn; Germany.
26 Department of Physics, Boston University, Boston MA; United States of America.
27 Department of Physics, Brandeis University, Waltham MA; United States of America.
28 (𝑎) Transilvania University of Brasov, Brasov; (𝑏) Horia Hulubei National Institute of Physics and Nuclear
Engineering, Bucharest; (𝑐) Department of Physics, Alexandru Ioan Cuza University of Iasi, Iasi; (𝑑) National
Institute for Research and Development of Isotopic and Molecular Technologies, Physics Department,
Cluj-Napoca; (𝑒) National University of Science and Technology Politechnica, Bucharest; ( 𝑓 ) West
University in Timisoara, Timisoara; (𝑔) Faculty of Physics, University of Bucharest, Bucharest; Romania.
29 (𝑎) Faculty of Mathematics, Physics and Informatics, Comenius University, Bratislava; (𝑏) Department of
Subnuclear Physics, Institute of Experimental Physics of the Slovak Academy of Sciences, Kosice; Slovak
Republic.
30 Physics Department, Brookhaven National Laboratory, Upton NY; United States of America.
31 Universidad de Buenos Aires, Facultad de Ciencias Exactas y Naturales, Departamento de Física, y
CONICET, Instituto de Física de Buenos Aires (IFIBA), Buenos Aires; Argentina.
32 California State University, CA; United States of America.
33 Cavendish Laboratory, University of Cambridge, Cambridge; United Kingdom.
34 (𝑎) Department of Physics, University of Cape Town, Cape Town; (𝑏) iThemba Labs, Western
Cape; (𝑐) Department of Mechanical Engineering Science, University of Johannesburg,
Johannesburg; (𝑑) National Institute of Physics, University of the Philippines Diliman
(Philippines); (𝑒) University of South Africa, Department of Physics, Pretoria; ( 𝑓 ) University of Zululand,
KwaDlangezwa; (𝑔) School of Physics, University of the Witwatersrand, Johannesburg; South Africa.
35 Department of Physics, Carleton University, Ottawa ON; Canada.
36 (𝑎) Faculté des Sciences Ain Chock, Université Hassan II de Casablanca; (𝑏) Faculté des Sciences,
Université Ibn-Tofail, Kénitra; (𝑐) Faculté des Sciences Semlalia, Université Cadi Ayyad,
LPHEA-Marrakech; (𝑑) LPMR, Faculté des Sciences, Université Mohamed Premier, Oujda; (𝑒) Faculté des
sciences, Université Mohammed V, Rabat; ( 𝑓 ) Institute of Applied Physics, Mohammed VI Polytechnic
University, Ben Guerir; Morocco.
37 CERN, Geneva; Switzerland.
38 Affiliated with an institute covered by a cooperation agreement with CERN.
39 Affiliated with an international laboratory covered by a cooperation agreement with CERN.
40 Enrico Fermi Institute, University of Chicago, Chicago IL; United States of America.
41 LPC, Université Clermont Auvergne, CNRS/IN2P3, Clermont-Ferrand; France.

27

## PDF page 28

42 Nevis Laboratory, Columbia University, Irvington NY; United States of America.
43 Niels Bohr Institute, University of Copenhagen, Copenhagen; Denmark.
44 (𝑎) Dipartimento di Fisica, Università della Calabria, Rende; (𝑏) INFN Gruppo Collegato di Cosenza,

Laboratori Nazionali di Frascati; Italy.
45 Physics Department, Southern Methodist University, Dallas TX; United States of America.
46 Physics Department, University of Texas at Dallas, Richardson TX; United States of America.
47 National Centre for Scientific Research "Demokritos", Agia Paraskevi; Greece.
48 (𝑎) Department of Physics, Stockholm University; (𝑏) Oskar Klein Centre, Stockholm; Sweden.
49 Deutsches Elektronen-Synchrotron DESY, Hamburg and Zeuthen; Germany.
50 Fakultät Physik , Technische Universität Dortmund, Dortmund; Germany.
51 Institut für Kern- und Teilchenphysik, Technische Universität Dresden, Dresden; Germany.
52 Department of Physics, Duke University, Durham NC; United States of America.
53 SUPA - School of Physics and Astronomy, University of Edinburgh, Edinburgh; United Kingdom.
54 INFN e Laboratori Nazionali di Frascati, Frascati; Italy.
55 Physikalisches Institut, Albert-Ludwigs-Universität Freiburg, Freiburg; Germany.
56 II. Physikalisches Institut, Georg-August-Universität Göttingen, Göttingen; Germany.
57 Département de Physique Nucléaire et Corpusculaire, Université de Genève, Genève; Switzerland.
58 (𝑎) Dipartimento di Fisica, Università di Genova, Genova; (𝑏) INFN Sezione di Genova; Italy.
59 II. Physikalisches Institut, Justus-Liebig-Universität Giessen, Giessen; Germany.
60 SUPA - School of Physics and Astronomy, University of Glasgow, Glasgow; United Kingdom.
61 LPSC, Université Grenoble Alpes, CNRS/IN2P3, Grenoble INP, Grenoble; France.
62 Laboratory for Particle Physics and Cosmology, Harvard University, Cambridge MA; United States of

America.
63 (𝑎) Department of Modern Physics and State Key Laboratory of Particle Detection and Electronics,
University of Science and Technology of China, Hefei; (𝑏) Institute of Frontier and Interdisciplinary
Science and Key Laboratory of Particle Physics and Particle Irradiation (MOE), Shandong University,
Qingdao; (𝑐) School of Physics and Astronomy, Shanghai Jiao Tong University, Key Laboratory for Particle
Astrophysics and Cosmology (MOE), SKLPPC, Shanghai; (𝑑) Tsung-Dao Lee Institute, Shanghai; (𝑒) School
of Physics and Microelectronics, Zhengzhou University; China.
64 (𝑎) Kirchhoff-Institut für Physik, Ruprecht-Karls-Universität Heidelberg, Heidelberg; (𝑏) Physikalisches
Institut, Ruprecht-Karls-Universität Heidelberg, Heidelberg; Germany.
65 (𝑎) Department of Physics, Chinese University of Hong Kong, Shatin, N.T., Hong Kong; (𝑏) Department
of Physics, University of Hong Kong, Hong Kong; (𝑐) Department of Physics and Institute for Advanced
Study, Hong Kong University of Science and Technology, Clear Water Bay, Kowloon, Hong Kong; China.
66 Department of Physics, National Tsing Hua University, Hsinchu; Taiwan.
67 ĲCLab, Université Paris-Saclay, CNRS/IN2P3, 91405, Orsay; France.
68 Centro Nacional de Microelectrónica (IMB-CNM-CSIC), Barcelona; Spain.
69 Department of Physics, Indiana University, Bloomington IN; United States of America.
70 (𝑎) INFN Gruppo Collegato di Udine, Sezione di Trieste, Udine; (𝑏) ICTP, Trieste; (𝑐) Dipartimento
Politecnico di Ingegneria e Architettura, Università di Udine, Udine; Italy.
71 (𝑎) INFN Sezione di Lecce; (𝑏) Dipartimento di Matematica e Fisica, Università del Salento, Lecce; Italy.
72 (𝑎) INFN Sezione di Milano; (𝑏) Dipartimento di Fisica, Università di Milano, Milano; Italy.
73 (𝑎) INFN Sezione di Napoli; (𝑏) Dipartimento di Fisica, Università di Napoli, Napoli; Italy.
74 (𝑎) INFN Sezione di Pavia; (𝑏) Dipartimento di Fisica, Università di Pavia, Pavia; Italy.
75 (𝑎) INFN Sezione di Pisa; (𝑏) Dipartimento di Fisica E. Fermi, Università di Pisa, Pisa; Italy.
76 (𝑎) INFN Sezione di Roma; (𝑏) Dipartimento di Fisica, Sapienza Università di Roma, Roma; Italy.
77 (𝑎) INFN Sezione di Roma Tor Vergata; (𝑏) Dipartimento di Fisica, Università di Roma Tor Vergata,

28

## PDF page 29

Roma; Italy.
78 (𝑎) INFN Sezione di Roma Tre; (𝑏) Dipartimento di Matematica e Fisica, Università Roma Tre, Roma;

Italy.
79 (𝑎) INFN-TIFPA; (𝑏) Università degli Studi di Trento, Trento; Italy.
80 Universität Innsbruck, Department of Astro and Particle Physics, Innsbruck; Austria.
81 University of Iowa, Iowa City IA; United States of America.
82 Department of Physics and Astronomy, Iowa State University, Ames IA; United States of America.
83 Istinye University, Sariyer, Istanbul; Türkiye.
84 (𝑎) Departamento de Engenharia Elétrica, Universidade Federal de Juiz de Fora (UFJF), Juiz de

Fora; (𝑏) Universidade Federal do Rio De Janeiro COPPE/EE/IF, Rio de Janeiro; (𝑐) Instituto de Física,
Universidade de São Paulo, São Paulo; (𝑑) Rio de Janeiro State University, Rio de Janeiro; (𝑒) Federal
University of Bahia, Bahia; Brazil.
85 KEK, High Energy Accelerator Research Organization, Tsukuba; Japan.
86 Graduate School of Science, Kobe University, Kobe; Japan.
87 (𝑎) AGH University of Krakow, Faculty of Physics and Applied Computer Science, Krakow; (𝑏) Marian
Smoluchowski Institute of Physics, Jagiellonian University, Krakow; Poland.
88 Institute of Nuclear Physics Polish Academy of Sciences, Krakow; Poland.
89 Faculty of Science, Kyoto University, Kyoto; Japan.
90 Research Center for Advanced Particle Physics and Department of Physics, Kyushu University, Fukuoka ;
Japan.
91 L2IT, Université de Toulouse, CNRS/IN2P3, UPS, Toulouse; France.
92 Instituto de Física La Plata, Universidad Nacional de La Plata and CONICET, La Plata; Argentina.
93 Physics Department, Lancaster University, Lancaster; United Kingdom.
94 Oliver Lodge Laboratory, University of Liverpool, Liverpool; United Kingdom.
95 Department of Experimental Particle Physics, Jožef Stefan Institute and Department of Physics,
University of Ljubljana, Ljubljana; Slovenia.
96 School of Physics and Astronomy, Queen Mary University of London, London; United Kingdom.
97 Department of Physics, Royal Holloway University of London, Egham; United Kingdom.
98 Department of Physics and Astronomy, University College London, London; United Kingdom.
99 Louisiana Tech University, Ruston LA; United States of America.
100 Fysiska institutionen, Lunds universitet, Lund; Sweden.
101 Departamento de Física Teorica C-15 and CIAFF, Universidad Autónoma de Madrid, Madrid; Spain.
102 Institut für Physik, Universität Mainz, Mainz; Germany.
103 School of Physics and Astronomy, University of Manchester, Manchester; United Kingdom.
104 CPPM, Aix-Marseille Université, CNRS/IN2P3, Marseille; France.
105 Department of Physics, University of Massachusetts, Amherst MA; United States of America.
106 Department of Physics, McGill University, Montreal QC; Canada.
107 School of Physics, University of Melbourne, Victoria; Australia.
108 Department of Physics, University of Michigan, Ann Arbor MI; United States of America.
109 Department of Physics and Astronomy, Michigan State University, East Lansing MI; United States of
America.
110 Group of Particle Physics, University of Montreal, Montreal QC; Canada.
111 Fakultät für Physik, Ludwig-Maximilians-Universität München, München; Germany.
112 Max-Planck-Institut für Physik (Werner-Heisenberg-Institut), München; Germany.
113 Graduate School of Science and Kobayashi-Maskawa Institute, Nagoya University, Nagoya; Japan.
114 (𝑎) Department of Physics, Nanjing University, Nanjing; (𝑏) School of Science, Shenzhen Campus of Sun
Yat-sen University; (𝑐) University of Chinese Academy of Science (UCAS), Beĳing; China.

29

## PDF page 30

115 Department of Physics and Astronomy, University of New Mexico, Albuquerque NM; United States of

America.
116 Institute for Mathematics, Astrophysics and Particle Physics, Radboud University/Nikhef, Nĳmegen;
Netherlands.
117 Nikhef National Institute for Subatomic Physics and University of Amsterdam, Amsterdam;
Netherlands.
118 Department of Physics, Northern Illinois University, DeKalb IL; United States of America.
119 (𝑎) New York University Abu Dhabi, Abu Dhabi; (𝑏) United Arab Emirates University, Al Ain; United
Arab Emirates.
120 Department of Physics, New York University, New York NY; United States of America.
121 Ochanomizu University, Otsuka, Bunkyo-ku, Tokyo; Japan.
122 Ohio State University, Columbus OH; United States of America.
123 Homer L. Dodge Department of Physics and Astronomy, University of Oklahoma, Norman OK; United
States of America.
124 Department of Physics, Oklahoma State University, Stillwater OK; United States of America.
125 Palacký University, Joint Laboratory of Optics, Olomouc; Czech Republic.
126 Institute for Fundamental Science, University of Oregon, Eugene, OR; United States of America.
127 Graduate School of Science, Osaka University, Osaka; Japan.
128 Department of Physics, University of Oslo, Oslo; Norway.
129 Department of Physics, Oxford University, Oxford; United Kingdom.
130 LPNHE, Sorbonne Université, Université Paris Cité, CNRS/IN2P3, Paris; France.
131 Department of Physics, University of Pennsylvania, Philadelphia PA; United States of America.
132 Department of Physics and Astronomy, University of Pittsburgh, Pittsburgh PA; United States of
America.
133 (𝑎) Laboratório de Instrumentação e Física Experimental de Partículas - LIP, Lisboa; (𝑏) Departamento
de Física, Faculdade de Ciências, Universidade de Lisboa, Lisboa; (𝑐) Departamento de Física,
Universidade de Coimbra, Coimbra; (𝑑) Centro de Física Nuclear da Universidade de Lisboa,
Lisboa; (𝑒) Departamento de Física, Universidade do Minho, Braga; ( 𝑓 ) Departamento de Física Teórica y
del Cosmos, Universidad de Granada, Granada (Spain); (𝑔) Departamento de Física, Instituto Superior
Técnico, Universidade de Lisboa, Lisboa; Portugal.
134 Institute of Physics of the Czech Academy of Sciences, Prague; Czech Republic.
135 Czech Technical University in Prague, Prague; Czech Republic.
136 Charles University, Faculty of Mathematics and Physics, Prague; Czech Republic.
137 Particle Physics Department, Rutherford Appleton Laboratory, Didcot; United Kingdom.
138 IRFU, CEA, Université Paris-Saclay, Gif-sur-Yvette; France.
139 Santa Cruz Institute for Particle Physics, University of California Santa Cruz, Santa Cruz CA; United
States of America.
140 (𝑎) Departamento de Física, Pontificia Universidad Católica de Chile, Santiago; (𝑏) Millennium Institute
for Subatomic physics at high energy frontier (SAPHIR), Santiago; (𝑐) Instituto de Investigación
Multidisciplinario en Ciencia y Tecnología, y Departamento de Física, Universidad de La
Serena; (𝑑) Universidad Andres Bello, Department of Physics, Santiago; (𝑒) Instituto de Alta Investigación,
Universidad de Tarapacá, Arica; ( 𝑓 ) Departamento de Física, Universidad Técnica Federico Santa María,
Valparaíso; Chile.
141 Department of Physics, University of Washington, Seattle WA; United States of America.
142 Department of Physics and Astronomy, University of Sheffield, Sheffield; United Kingdom.
143 Department of Physics, Shinshu University, Nagano; Japan.
144 Department Physik, Universität Siegen, Siegen; Germany.

30

## PDF page 31

145 Department of Physics, Simon Fraser University, Burnaby BC; Canada.
146 SLAC National Accelerator Laboratory, Stanford CA; United States of America.
147 Department of Physics, Royal Institute of Technology, Stockholm; Sweden.
148 Departments of Physics and Astronomy, Stony Brook University, Stony Brook NY; United States of

America.
149 Department of Physics and Astronomy, University of Sussex, Brighton; United Kingdom.
150 School of Physics, University of Sydney, Sydney; Australia.
151 Institute of Physics, Academia Sinica, Taipei; Taiwan.
152 (𝑎) E. Andronikashvili Institute of Physics, Iv. Javakhishvili Tbilisi State University, Tbilisi; (𝑏) High
Energy Physics Institute, Tbilisi State University, Tbilisi; (𝑐) University of Georgia, Tbilisi; Georgia.
153 Department of Physics, Technion, Israel Institute of Technology, Haifa; Israel.
154 Raymond and Beverly Sackler School of Physics and Astronomy, Tel Aviv University, Tel Aviv; Israel.
155 Department of Physics, Aristotle University of Thessaloniki, Thessaloniki; Greece.
156 International Center for Elementary Particle Physics and Department of Physics, University of Tokyo,
Tokyo; Japan.
157 Department of Physics, Tokyo Institute of Technology, Tokyo; Japan.
158 Department of Physics, University of Toronto, Toronto ON; Canada.
159 (𝑎) TRIUMF, Vancouver BC; (𝑏) Department of Physics and Astronomy, York University, Toronto ON;
Canada.
160 Division of Physics and Tomonaga Center for the History of the Universe, Faculty of Pure and Applied
Sciences, University of Tsukuba, Tsukuba; Japan.
161 Department of Physics and Astronomy, Tufts University, Medford MA; United States of America.
162 Department of Physics and Astronomy, University of California Irvine, Irvine CA; United States of
America.
163 University of Sharjah, Sharjah; United Arab Emirates.
164 Department of Physics and Astronomy, University of Uppsala, Uppsala; Sweden.
165 Department of Physics, University of Illinois, Urbana IL; United States of America.
166 Instituto de Física Corpuscular (IFIC), Centro Mixto Universidad de Valencia - CSIC, Valencia; Spain.
167 Department of Physics, University of British Columbia, Vancouver BC; Canada.
168 Department of Physics and Astronomy, University of Victoria, Victoria BC; Canada.
169 Fakultät für Physik und Astronomie, Julius-Maximilians-Universität Würzburg, Würzburg; Germany.
170 Department of Physics, University of Warwick, Coventry; United Kingdom.
171 Waseda University, Tokyo; Japan.
172 Department of Particle Physics and Astrophysics, Weizmann Institute of Science, Rehovot; Israel.
173 Department of Physics, University of Wisconsin, Madison WI; United States of America.
174 Fakultät für Mathematik und Naturwissenschaften, Fachgruppe Physik, Bergische Universität
Wuppertal, Wuppertal; Germany.
175 Department of Physics, Yale University, New Haven CT; United States of America.
𝑎 Also Affiliated with an institute covered by a cooperation agreement with CERN.
𝑏 Also at An-Najah National University, Nablus; Palestine.
𝑐 Also at Borough of Manhattan Community College, City University of New York, New York NY; United
States of America.
𝑑 Also at Center for Interdisciplinary Research and Innovation (CIRI-AUTH), Thessaloniki; Greece.
𝑒 Also at CERN, Geneva; Switzerland.
𝑓 Also at CMD-AC UNEC Research Center, Azerbaĳan State University of Economics (UNEC);
Azerbaĳan.
𝑔 Also at Département de Physique Nucléaire et Corpusculaire, Université de Genève, Genève;

31

## PDF page 32

Switzerland.
ℎ Also at Departament de Fisica de la Universitat Autonoma de Barcelona, Barcelona; Spain.
𝑖 Also at Department of Financial and Management Engineering, University of the Aegean, Chios; Greece.
𝑗 Also at Department of Physics, California State University, Sacramento; United States of America.
𝑘 Also at Department of Physics, King’s College London, London; United Kingdom.
𝑙 Also at Department of Physics, Stanford University, Stanford CA; United States of America.
𝑚 Also at Department of Physics, Stellenbosch University; South Africa.
𝑛 Also at Department of Physics, University of Fribourg, Fribourg; Switzerland.
𝑜 Also at Department of Physics, University of Thessaly; Greece.
𝑝 Also at Department of Physics, Westmont College, Santa Barbara; United States of America.
𝑞 Also at Hellenic Open University, Patras; Greece.
𝑟 Also at Imam Mohammad Ibn Saud Islamic University; Saudi Arabia.
𝑠 Also at Institucio Catalana de Recerca i Estudis Avancats, ICREA, Barcelona; Spain.
𝑡 Also at Institut für Experimentalphysik, Universität Hamburg, Hamburg; Germany.
𝑢 Also at Institute for Nuclear Research and Nuclear Energy (INRNE) of the Bulgarian Academy of
Sciences, Sofia; Bulgaria.
𝑣 Also at Institute of Applied Physics, Mohammed VI Polytechnic University, Ben Guerir; Morocco.
𝑤 Also at Institute of Particle Physics (IPP); Canada.
𝑥 Also at Institute of Physics, Azerbaĳan Academy of Sciences, Baku; Azerbaĳan.
𝑦 Also at Institute of Theoretical Physics, Ilia State University, Tbilisi; Georgia.
𝑧 Also at National Institute of Physics, University of the Philippines Diliman (Philippines); Philippines.
𝑎𝑎 Also at Technical University of Munich, Munich; Germany.
𝑎𝑏 Also at The Collaborative Innovation Center of Quantum Matter (CICQM), Beĳing; China.
𝑎𝑐 Also at TRIUMF, Vancouver BC; Canada.
𝑎𝑑 Also at Università di Napoli Parthenope, Napoli; Italy.
𝑎𝑒 Also at University of Colorado Boulder, Department of Physics, Colorado; United States of America.
𝑎 𝑓 Also at Washington College, Chestertown, MD; United States of America.
𝑎𝑔 Also at Yeditepe University, Physics Department, Istanbul; Türkiye.
∗ Deceased

32
