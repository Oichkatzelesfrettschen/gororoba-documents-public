Source: gororoba-open:data/output/audit/qgp-participant-reference-intake/alice-public-2018-011.pdf
PDF sha256: de4d98816c22c0991e13e1669d9d708ffea7b470b56a020bbe90e38625ef7a6c
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of alice_2018_centrality_determination_in_heavy_ion_collisions.pdf

Transcription of `alice_2018_centrality_determination_in_heavy_ion_collisions.pdf` in this directory, 28 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-28 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

EUROPEAN ORGANIZATION FOR NUCLEAR RESEARCH

ALICE-PUBLIC-2018-011

Centrality determination in heavy ion collisions
ALICE Collaboration∗

Abstract
This document describes the methods used by ALICE for the centrality determination. Specifically
it addresses the modifications implemented with respect to previous publications [1, 2], which stems
for:
– and a modification of the definition of the centrality classes, now defined according to the
simulated multiplicity distribution;
– an update of the cross-section values used for the Glauber-MC calculations;
– a modification in the parameterization of the nuclear density charge which uses a weigthed sum
of individual 2pF distributions for the proton and for the neutron;
– a uniform three-dimensional lattice to parameterize the minimum nodal separation between
nucleons;
– the total systematic uncertainty obtained by adding in quadrature the maximum/average of the
up and downward variations from all sources.

c
⃝ 2018 CERN for the benefit of the ALICE Collaboration.
Reproduction of this article or parts of it is allowed as specified in the CC-BY-4.0 license.
∗ See Appendix A for the list of collaboration members

## PDF page 2

2

1

ALICE Collaboration

Introduction

The centrality is defined as the percentile of the hadronic cross section corresponding to a particle mulT HR )
tiplicity, or an energy deposited, measured in ALICE, above a given threshold (Nch
1
c≈
σAA

∫ ∞

dσ
1
′
dNch
≈
′
T HR dN
σAA
Nch
ch

∫ E T HR
ZDC

0

dσ
′
dEZDC
.
′
dEZDC

(1)

The Glauber model is widely used to describe the dependence of Npart and Ncoll on b in p–A, d–A and
A–A collisions [3–6]. The purpose of Monte Carlo implementations of the Glauber model [7, 8] is to
compose two nuclei out of nucleons and simulate their collision process event-by-event. Geometrical
quantities are calculated by simulating many nucleus-nucleus collisions. Coupling the Glauber MC to a
model of particle production, one can calculate the produced particle multiplicity distribution that can be
compared to the experimentally measured one. Mean values of geometrical quantities are then calculated
for centrality classes defined by classifying the events according to their multiplicity.
This documents presents the ALICE methods for the centrality determination, focussing to the changes
introduced with respect to the past [1], i.e. a modification of the definition of the centrality classes, now
defined according to the simulated multiplicity distribution, an update of the cross-section values used
for the Glauber-MC calculations, as well as a modification in the parameterization of the nuclear density
charge which uses a weigthed sum of individual 2pF distributions for the proton and for the neutron, and
a uniform three-dimensional lattice to parameterize the minimum nodal separation between nucleons.
Finally the total systematic uncertainty obtained by adding in quadrature the maximum/average of the up
and downward variations from all sources. Section 2 summarizes the methods for the Glauber-MC and
the NBD-Glauber fot to the multiplicity distribution. Section 4 and Section 3 provide tables with calcu√
lated quantities for Pb–Pb collisions at sNN = 2.76 and 5.02 TeV, and the differences with previously
√
used values. Section 5 provides the values for the Xe–Xe collisions at sNN = 5.44 TeV.

2

The Glauber Monte Carlo

2.1

The nucelar charge distribution

Following [9], the first step in the Glauber Monte Carlo is to prepare a model of the two nuclei by defining
stochastically the position of the nucleons in each nucleus. The nucleon position in the 208 Pb nucleus is
determined by the nuclear density function, modeled by the functional form (modified Woods-Saxon or
2-parameter Fermi distribution):
1 + w(r/R)2
( )
ρ(r) = ρ0
(2)
1 + exp r−R
a
The parameters are based on data from low energy electron-nucleus scattering experiments [10]. Protons
and neutrons are assumed to have the same nuclear profile. The parameter ρ0 is the nucleon density,
which provides the overall normalization, not relevant for the Monte Carlo simulation, R is the radius
parameter of the 208 Pb nucleus and a is the skin thickness of the nucleus, which indicates how quickly the
nuclear density falls off near the edge of the nucleus. The additional parameter w is needed to describe
nuclei whose maximum density is reached at radii r > 0 (w = 0 for Pb). According to [11] we used a
weigthed sum of individual 2pF distributions for the proton and for the neutron with R p = 6.68 ± 0.02
and a p = 0.447 ± 0.01, Rn = 6.69 ± 0.03 and an = 0.560 ± 0.03. In the Monte Carlo procedure the radial
coordinate of a nucleon is randomly
drawn from the distribution 4πr2 ρ(r) and ρ0 is determined by the
∫
overall normalization condition ρ(r)d3 r = A. Instead of the hard-sphere exclusion distance previously
used (dmin = (0.4 ± 0.4) fm), we employ a uniform three-dimensional lattice with a minimum nodal
separation (dnode ) equivalent to dmin . It is equivalently treated with a variation of 100%, dnode = (0.4 ±
0.4) fm.

## PDF page 3

Centrality determination in heavy ion collisions

2.2

3

The nucleon-nucleon cross-section

The second step is to simulate a nuclear collision. The impact parameter b is randomly selected from
the geometrical distribution dP/db ∼ b up to a maximum bmax ≃ 20 fm > 2RPb , large enough to simulate
collisions until the interaction probability becomes zero. The nucleus-nucleus collision is treated as
a sequence of independent binary nucleon-nucleon collisions, where the nucleons travel on straightline trajectories and the inelastic nucleon-nucleon cross section is assumed to be independent of the
number of collisions a nucleon underwent previously, i.e. the same cross section is used for all successive
collisions. Two nucleons from different nuclei are assumed to collide if the relative transverse distance
between
√ centers is less than the distance corresponding to the inelastic nucleon-nucleon cross section
d<

σinel
NN /π.

The value of the cross-section σinel
NN is typically estimated by interpolation of pp data at different centerof-mass energies and from cosmic rays, and subtracting the elastic scattering cross section from the total
cross section. According to [11], we decided to adopt:
–
–
–
–

√

sNN = 2.76 TeV: σinel
NN = 61.8 ± 0.9 mb.

√

sNN = 5.02 TeV: σinel
NN = 67.6 ± 0.6 mb.

√

sNN = 5.44 TeV: σinel
NN = 68.4 ± 0.5 mb.

√

sNN = 8.16 TeV: σinel
NN = 72.5 ± 0.5 mb.

in contrast to the previously used values:
σinel
NN = 70 ± 5 mb [2].

√

sNN = 2.76 TeV: σinel
NN = 64 ± 5 mb [1];

√

sNN = 5.02 TeV:

The number of collisions Ncoll and the number of participants Npart are determined by counting, respectively, the binary nucleon collisions and the nucleons that experience at least one collision. Following
the notation in [3], the geometric nuclear overlap function T PbPb is then calculated as T PbPb = Ncoll /σinel
NN ,
and represents the effective nucleon luminosity in the collision process.
The total Pb–Pb cross section is calculated as σPbPb = Nevt (Ncoll ≥ 1)/Nevt (Ncoll ≥ 0) × πb2max , i.e. the
geometrical value corrected by the fraction of events with at least one nucleon-nucleon collision. It
amounts to
– σPbPb = (7.67 ± 0.16(syst.)) b for Pb–Pb at 5.02 TeV,
– σPbPb = (7.55 ± 0.12(syst.)) b for Pb–Pb at 2.76 TeV,
– σpPb = (2.10 ± 0.055(syst.)) b for p–Pb at 5.02 TeV,
– σpPb = (2.12 ± 0.047(syst.)) b for p–Pb at 8.16 TeV,
– σXeXe = (5.7 ± 0.2(syst.)) b for Xe–Xe at 5.44 TeV.
2.3

The NBD-Glauber fit to the multiplicity distribution

To reproduce the experimental multiplicity distribution, the Glauber Monte Carlois coupled to a model
for particle production, based on a negative binomial distribution (NBD). This use of NBD is motivated
by the fact that in minimum bias pp and pp collisions at high energy, the charged particle multiplicity
dσ/dNch has been measured over a wide range of rapidity and is well described by a NBD [12, 13].
The Glauber Monte Carlo defines, for an event with a given impact parameter b, the corresponding Npart
and Ncoll . The particle multiplicity per nucleon-nucleon collision is parametrized by a NBD. To apply

## PDF page 4

4

ALICE Collaboration

this model to any collision with a given Npart and Ncoll value we introduce the concept of “ancestors”,
i.e. independently emitting sources of particles. We assume that the number of ancestors Nancestors can
be parameterized by Nancestors = f · Npart + (1 − f ) · Ncoll . This is inspired by two-component models
[14, 15], which decompose nucleus–nucleus collisions into soft and hard interactions, where the soft
interactions produce particles with an average multiplicity proportional to Npart , and the probability for
hard interactions to occur is proportional to Ncoll .
To generate the number of particles produced per interaction, we use the negative binomial distribution
Pµ,k (n) =

Γ(n + k)
(µ/k)n
,
·
Γ(n + 1)Γ(k) (µ/k + 1)n+k

(3)

which gives the probability of measuring n hits per ancestor, where µ is the mean multiplicity per ancestor and k controls the width. For every Glauber Monte Carlo event, the NBD is sampled Nancestors times
to obtain the averaged simulated VZERO amplitude for this event, which is proportional to the number
of particles hitting the hodoscopes. The VZERO amplitude distribution is simulated for an ensemble of
events and for various values of the NBD parameters µ, k, and the Nancestors parameter f . A minimization procedure is applied to find the parameters which result in the smallest χ2 . The fit is performed for
VZERO amplitudes large enough so that the purity of the event sample and the efficiency of the event
selection is 100%. That leaves a very broad range in the amplitude values that can be fitted to extract parameters f , µ and k directly from the data. The quality of the fit is good, as the χ2 /NDF is approximately
unity for all fits. However we note that the high multiplicity tail, which is quite sensitive to fluctuations
and the detector resolution not implemented in the model, is not perfectly well described.
We can then calculate the mean number of participants ⟨Npart ⟩ and collisions ⟨Ncoll ⟩, and the mean nuclear thickness function ⟨T PbPb ⟩ for centrality classes defined by sharp cuts in the simulated VZERO
distribution. This is different to what was done in the past, where centrality classes were defined by
cuts in the impact parameter. The root mean square (RMS) of these distributions is a measure for the
magnitude of the dispersion of the quantities.
The systematic uncertainties on the mean values are obtained by independently varying the parameters
of the Glauber model within their estimated uncertainties and repeating the fit for all the parameter variations. The total systematic uncertainty is obtained by adding in quadrature the maximum/average of the
up and downward variations from all sources. Figure 1 shows the resulting variations for Pb–Pb colli√
sions at sNN = 5.02 TeV, for centrality classes defined by multiplicity or impact parameter, respectively.

3

Pb-Pb collisions at

√

sNN = 5.02 TeV

√
Figure 2 shows the distribution of V0 amplitudes for all triggered Pb–Pb collisions at sNN = 5.02 TeV
with a vertex within 10 cm, fitted by a Glauber-NBD fit.
√
Table 1 shows the geometric properties (Npart , Ncoll , T PbPb ) of Pb–Pb collisions at sNN = 5.02 TeV for
centrality classes defined by sharp cuts in the V0M multiplicity distribution, simulated with an NBDGlauber fit. The mean values, the RMS, and the systematic uncertainties are obtained with a Glauber
Monte Carlo calculation.

## PDF page 5

1.1

Glauber
MC
σinel
=67.0 mb
NN
dmin
=0.0 fm
Rp=6.66 fm
ap=0.446 fm
Rn=6.66 fm
an=0.557 fm

1.08
1.06
1.04

σinel
=68.2 mb
d NN =0.8 fm (a)
Rmin
p=6.70 fm
ap=0.448 fm
Rn=6.72 fm
an=0.563 fm

1.02

5

Npart / Ndefault
part

Npart / Ndefault
part

Centrality determination in heavy ion collisions

1.1
1.06
1.04
1.02

1

1

0.98

0.98

0.96

0.96

0.94

0.94

0.92
0.9
0

σinel
=67.0 mb
NN
inel
σNN
=68.2 mb
dnode=0.0 fm
dnode=0.8 fm
Rp=6.66 fm
Rp=6.70 fm
a p=0.446 fm
a p=0.448 fm
Rn=6.66 fm
Rn=6.72 fm
a n=0.557 fm
a n=0.563 fm

1.08

(a)

0.92
50

100

150

200

250

300

0.9
0

350

50

100

150

200

250

300

1.1

Glauber
MC
σinel
=67.0 mb
NN
dmin
=0.0 fm
Rp=6.66 fm
ap=0.446 fm
Rn=6.66 fm
an=0.557 fm

1.08
1.06
1.04

σinel
=68.2 mb
d NN =0.8 fm
Rmin
p=6.70 fm
ap=0.448 fm
Rn=6.72 fm
an=0.563 fm

(b)

1.02

1.1

σinel
=67.0 mb
NN
σinel
=68.2 mb
NN
dnode=0.0 fm
dnode=0.8 fm
Rp=6.66 fm
Rp=6.70 fm
a p=0.446 fm
a p=0.448 fm
Rn=6.66 fm
Rn=6.72 fm
a n=0.557 fm
a n=0.563 fm

1.08
1.06
1.04
1.02

1

1

0.98

0.98

0.96

0.96

0.94

0.94

0.92

0.92

0.9
0

200

400

600

800

1000

1200

1400

0.9
0

1600

200

400

600

800

1000

1200

(b)

1400

1.1

Glauber
MC
σinel
=67.0 mb
NN
dmin
=0.0 fm
Rp=6.66 fm
ap=0.446 fm
Rn=6.66 fm
an=0.557 fm

1.06
1.04

σinel
=68.2 mb
NN
dmin
=0.8 fm (c)
Rp
=6.70 fm
ap=0.448 fm
Rn=6.72 fm
an=0.563 fm

1.02

1.1

inel
σNN
=67.0 mb
σinel
=68.2 mb
NN
dnode=0.0 fm
dnode=0.8 fm
Rp=6.66 fm
Rp=6.70 fm
a p=0.446 fm
a p=0.448 fm
Rn=6.66 fm
Rn=6.72 fm
a n=0.557 fm
a n=0.563 fm

1.08
1.06
1.04
1.02

1

1

0.98

0.98

0.96

0.96

0.94

0.94

0.92

0.92

0.9
0

5

10

15

20

25

TAA

1600

Ncoll
TAA / Tdefault
AA

TAA / Tdefault
AA

Ncoll

1.08

350

Npart
Ncoll / Ndefault
coll

Ncoll / Ndefault
coll

Npart

0.9
0

5

10

15

(c)

20

25

TAA

Fig. 1: Sensitivity of Npart , Ncoll , and T PbPb to variations of parameters in the Glauber Monte Carlo model of Pb–Pb
√
collisions at sNN = 5.02 TeV for centrality classes defined by multiplicity (left) or impact parameter (right),
respectively. The gray band represents the RMS scaled by a factor 0.1 for visibility.

## PDF page 6

ALICE Collaboration

Pµ ,k x [f Npart + (1-f)N ]

10−3

10−4

coll

f = 0.801, µ = 46.4, k = 1.5

10−4

10−50

60-70%

ALICE Pb-Pb sNN = 5.02 TeV
Data
NBD-Glauber fit

70-80%

10−3

80-90%

Events (arb. units)

6

500

1000

Ratio

0
1.5

5000

10000

15000

20000

5000

10000

15000

20000

0-2.5%

2.5-5%

5-7.5%

7.5-10%

10-20%

20-30%

30-40%

40-50%

50-60%

10−5

25000

30000

35000

25000

30000

35000

1
0.50

V0M amplitude (arb. units)

Npart

Ncoll

√
Fig. 2: Distribution of the sum of amplitudes in the V0 scintillators for Pb–Pb collisions at sNN 5̄.02 TeV. The
distribution is fitted with the NBD-Glauber fit shown as a line. The inset shows a zoom of the most peripheral
region.

geo

Npart
10

geo

103

Ncoll

mult
Npart

2

mult

Ncoll
102

10

10
1.25

20

40

60

80

100

20

40

60

80

100
centrality

1.2
1.15
1.1
1.05
1
0

Ratio

Ratio

10

10

20

40

60

80

100

0

20

40

60

80

100
centrality

1.35
1.3
1.25
1.2
1.15
1.1
1.05

Fig. 3: Mean values of Npart and Ncoll for centrality classes defined by multiplicity or impact parameter, respectively.

## PDF page 7

Centrality determination in heavy ion collisions

7

√
Table 1: Geometric properties (Npart , Ncoll , T PbPb ) of Pb–Pb collisions at sNN = 5.02 TeV for centrality classes
defined by sharp cuts in the V0M multiplicity distribution, simulated with an NBD-Glauber fit. The mean values,
the RMS, and the systematic uncertainties are obtained with a Glauber Monte Carlo calculation.
Centrality
0-1%
1-2%
2-3%
3-4%
4-5%
0-2.5 %
2.5-5 %
5-7.5 %
7.5-10%
0-5 %
5-10 %
10-15 %
15-20 %
20-25 %
25-30 %
30-35 %
35-40 %
40-45 %
45-50 %
50-55 %
55-60 %
60-65 %
65-70 %
70-75 %
75-80 %
80-85 %
85-90 %
90-95 %
95-100 %
0-10 %
10-20 %
20-30 %
30-40 %
40-50 %
50-60 %
60-70 %
70-80 %
80-90 %
90-100 %
0-20%
20-40%
40-60%
60-80%
80-100%
60-100%
0-30%
30-50%

⟨Npart ⟩
401.9
393.9
384.4
373.9
362.9
395.7
371.1
344
318.4
383.4
331.2
283
241
204.1
171.7
143.2
118.4
96.58
77.68
61.28
47.39
35.7
26.23
18.63
12.8
8.481
5.433
3.309
2.241
357.3
262
187.9
130.8
87.14
54.34
30.97
15.72
6.973
2.785
309.7
159.4
70.74
23.35
4.883
14.12
269.1
109

RMS
7.55
10.2
11.7
12.5
13
11.1
14.5
14.9
14.7
17.8
19.6
18.1
16.6
15.1
13.6
12.3
11
9.76
8.6
7.49
6.49
5.53
4.66
3.9
3.14
2.45
1.83
1.22
0.536
32.1
27.2
21.6
17
13.2
9.87
6.97
4.58
2.64
1.09
56.2
34.5
20.1
9.64
2.91
11.7
74.5
26.6

(sys.)
0.46
0.496
0.752
0.762
0.738
0.481
0.738
0.927
1.15
0.568
1.03
1.13
1.22
1.33
1.36
1.49
1.2
1.08
0.793
0.9
0.753
0.734
0.448
0.329
0.205
0.171
0.0625
0.0902
0.0441
0.753
1.15
1.34
1.33
0.928
0.802
0.57
0.241
0.0729
0.0497
0.895
1.32
0.859
0.404
0.0627
0.255
0.993
1.11

⟨Ncoll ⟩
1949
1844
1755
1673
1593
1872
1654
1464
1300
1763
1382
1090
857.3
668.8
516.6
393
294.6
216.1
155.2
108.6
74.14
49.18
31.81
20
12.23
7.198
4.104
2.172
1.228
1572
973.4
592.7
343.8
185.7
91.41
40.5
16.12
5.667
1.708
1273
468.2
138.5
28.31
3.691
16
1046
264.8

RMS
87
81.3
80.8
79.9
77.6
107
95.4
88.1
81.7
149
118
97.3
83.1
70.7
59.8
50.7
42.1
34.9
27.9
21.8
16.8
12.4
8.85
6.27
4.27
2.81
1.84
1.11
0.497
233
147
100
67.8
43.9
26
13.9
6.62
2.84
0.986
357
151
59.3
16.3
2.9
17
437
97.5

(sys.)
21.1
20.1
20.3
18.8
17.8
20.4
18.5
16.8
14.8
19.4
15.7
12.3
10.5
9.21
7.32
6.51
5.12
3.83
2.91
2.61
1.74
1.37
0.763
0.502
0.253
0.236
0.0635
0.0844
0.0416
17.4
11.3
8.21
5.76
3.33
2.11
1.03
0.341
0.1
0.0474
14.1
6.92
2.7
0.68
0.0761
0.409
11.7
4.51

⟨T PbPb ⟩ (1/mbarn)
28.83
27.28
25.96
24.75
23.57
27.69
24.46
21.66
19.23
26.08
20.44
16.12
12.68
9.894
7.641
5.814
4.358
3.197
2.296
1.607
1.097
0.7275
0.4706
0.2959
0.1808
0.1065
0.06071
0.03213
0.01816
23.26
14.4
8.767
5.086
2.747
1.352
0.5992
0.2385
0.08383
0.02527
18.83
6.927
2.049
0.4188
0.0546
0.2367
15.48
3.917

RMS (1/mbarn)
1.29
1.2
1.19
1.18
1.15
1.58
1.41
1.3
1.21
2.21
1.75
1.44
1.23
1.05
0.884
0.75
0.624
0.516
0.413
0.323
0.248
0.184
0.131
0.0927
0.0632
0.0416
0.0272
0.0165
0.00735
3.45
2.18
1.49
1
0.649
0.385
0.205
0.098
0.042
0.0146
5.29
2.23
0.878
0.241
0.0429
0.251
6.47
1.44

(sys.) (1/mbarn)
0.177
0.171
0.2
0.18
0.178
0.175
0.18
0.174
0.16
0.176
0.166
0.135
0.118
0.11
0.0942
0.0917
0.073
0.0554
0.0427
0.0378
0.026
0.0207
0.012
0.0079
0.0041
0.0037
0.00126
0.00132
0.000673
0.168
0.126
0.101
0.0814
0.0486
0.0309
0.0158
0.00552
0.00178
0.000777
0.142
0.0909
0.0394
0.0106
0.00133
0.00637
0.121
0.0645

## PDF page 8

8

4

ALICE Collaboration

Pb-Pb collisions at

√

sNN = 2.76 TeV

10−3

ALICE Pb-Pb sNN = 2.76 TeV
Data
NBD-Glauber fit
Pµ ,k x [f Npart + (1-f)N ]
coll

f = 0.801, µ = 28.7, k = 1.6

Ratio

0
1.5

0-5%

5-10%

10-20%

20-30%

30-40%

10−5

40-50%

10−4

50-60%

Events (arb. units)

√
Figure 4 shows the distribution of V0 amplitudes for all triggered Pb–Pb collisions at sNN = 2.76 TeV
with a vertex within 10 cm, fitted by a Glauber-NBD fit.
√
Table 2 shows the geometric properties (Npart , Ncoll , T PbPb ) of Pb–Pb collisions at sNN = 2.76 TeV for
centrality classes defined by sharp cuts in the V0M multiplicity distribution.

2000 4000 6000 8000 10000 12000 14000 16000 18000 20000 22000

1
0.50

2000

4000

6000

8000 10000 12000 14000 16000 18000 20000 22000

V0M amplitude (arb. units)

Fig. 4: Distribution of the sum of amplitudes in the V0 scintillators for Pb–Pb collisions at
distribution is fitted with the NBD-Glauber fit shown as a line.

√

sNN 2̄.76 TeV. The

## PDF page 9

Centrality determination in heavy ion collisions

9

√
Table 2: Geometric properties (Npart , Ncoll , T PbPb ) of Pb–Pb collisions at sNN = 2.76 TeV for centrality classes
defined by sharp cuts in the V0M multiplicity distribution, simulated with an NBD-Glauber fit. The mean values,
the RMS, and the systematic uncertainties are obtained with a Glauber Monte Carlo calculation.
Centrality
0-1%
1-2%
2-3%
3-4%
4-5%
0-2.5 %
2.5-5 %
5-7.5 %
7.5-10%
0-5 %
5-10 %
10-15 %
15-20 %
20-25 %
25-30 %
30-35 %
35-40 %
40-45 %
45-50 %
50-55 %
55-60 %
60-65 %
65-70 %
70-75 %
75-80 %
80-85 %
85-90 %
90-95 %
95-100 %
0-10 %
10-20 %
20-30 %
30-40 %
40-50 %
50-60 %
60-70 %
70-80 %
80-90 %
90-100 %
0-20%
20-40%
40-60%
60-80%
80-100%
60-100%
0-30%
30-50%

⟨Npart ⟩
400.8
392.4
382.3
371.5
360.4
394.2
368.7
341.2
314.5
381.5
327.8
280.1
238.5
202.1
170.8
142.7
117.6
96.09
77.27
61.08
47.47
35.76
26.31
18.67
12.91
8.588
5.438
3.315
2.238
354.7
259.3
186.5
130.1
86.69
54.28
31.04
15.81
7.011
2.788
307
158.3
70.49
23.42
4.9
14.17
266.8
108.4

RMS
7.7
10
12
12
13
11
15
15
15
18
20
18
16
15
13
12
11
9.5
8.4
7.3
6.3
5.5
4.6
3.8
3.1
2.4
1.8
1.2
0.53
33
27
21
17
13
9.6
6.9
4.5
2.6
1.1
56
34
20
9.6
2.9
12
74
26

(sys.)
1.3
1.5
1.9
2.3
2.5
1.2
2.3
2.6
3.5
1.7
2.8
2.8
2.6
2.5
2.6
2.7
1.9
2.3
1.8
1.8
2
1.5
1.2
0.79
0.71
0.49
0.17
0.13
0.091
1.9
2.7
2.4
2.2
2
1.9
1.3
0.78
0.33
0.12
2.2
2.2
2
1
0.17
0.55
2.1
2.1

⟨Ncoll ⟩
1788
1694
1614
1537
1464
1720
1519
1345
1193
1619
1269
1004
791.1
622.3
485
370.7
279.4
204.7
148.4
104.4
71.98
48.15
31.32
19.69
12.18
7.244
4.075
2.173
1.224
1444
897.7
553.7
325
176.6
88.21
39.74
15.96
5.657
1.709
1171
439.3
132.4
27.84
3.682
15.78
965.2
250.8

RMS
79
76
76
73
72
98
88
81
76
1.4e+02
1.1e+02
89
76
64
56
47
40
32
26
21
16
12
8.7
6.1
4.1
2.8
1.8
1.1
0.49
2.1e+02
1.3e+02
91
63
41
24
13
6.4
2.8
0.97
3.3e+02
1.4e+02
55
16
2.9
17
4e+02
91

(sys.)
32
32
32
33
31
31
32
29
26
31
27
24
19
16
14
10
9.2
6.5
5.7
4.2
3.8
2.9
1.9
0.97
0.81
0.48
0.16
0.11
0.082
28
21
14
9.7
6
4
2.4
0.93
0.31
0.099
24
12
4.9
1.6
0.16
0.85
20
7.7

⟨T PbPb ⟩ (1/mbarn)
28.94
27.42
26.11
24.86
23.68
27.83
24.58
21.76
19.3
26.2
20.53
16.25
12.8
10.07
7.848
5.998
4.521
3.313
2.401
1.69
1.165
0.7792
0.5067
0.3186
0.1972
0.1172
0.06594
0.03517
0.01981
23.37
14.53
8.96
5.259
2.857
1.427
0.6431
0.2582
0.09153
0.02765
18.95
7.109
2.143
0.4505
0.05959
0.2554
15.62
4.058

RMS (1/mbarn)
1.3
1.2
1.2
1.2
1.2
1.6
1.4
1.3
1.2
2.2
1.8
1.4
1.2
1
0.91
0.76
0.65
0.52
0.42
0.33
0.25
0.19
0.14
0.098
0.066
0.045
0.029
0.018
0.008
3.5
2.2
1.5
1
0.66
0.4
0.22
0.1
0.046
0.016
5.3
2.2
0.9
0.26
0.047
0.27
6.4
1.5

(sys.) (1/mbarn)
0.29
0.26
0.29
0.31
0.27
0.26
0.29
0.23
0.23
0.27
0.23
0.23
0.18
0.16
0.19
0.15
0.14
0.088
0.082
0.06
0.056
0.045
0.031
0.016
0.013
0.0078
0.0028
0.002
0.0014
0.2
0.2
0.17
0.14
0.084
0.058
0.038
0.015
0.0051
0.0018
0.19
0.15
0.07
0.026
0.0028
0.013
0.17
0.11

## PDF page 10

10

5

ALICE Collaboration

Xe-Xe collisions at

√

sNN = 5.44 TeV

ALICE Xe-Xe sNN = 5.44 TeV
Data
NBD-Glauber fit
Pµ,k x [f N

part

+ (1-f)N ]

−3

10

10−4

coll

80-90%

f = 0.802, µ = 53.7, k = 1.0

10−4

60-70%

10

70-80%

−3

−5

0

5000

10000

500

15000

1000

1500

0-5%

10-20%

20-30%

30-40%

50-60%

10−5

40-50%

10 0

5-10%

Events (arb. units)

In the Monte Carlo Glauber calculation, the nuclear density for 129 Xe, is described by a Woods-Saxon
distribution for a deformed nucleus.
√
Figure 5 shows the distribution of V0 amplitudes for all triggered Xe–Xe collisions at sNN = 5.44 TeV
with a vertex within 10 cm, fitted by a Glauber-NBD fit.
√
Table 3 shows the geometric properties (Npart , Ncoll , T XeXe ) of Xe–Xe collisions at sNN = 5.44 TeV for
centrality classes defined by sharp cuts in the V0M multiplicity distribution.

20000

25000

V0M amplitude (arb. units)
√
Fig. 5: Distribution of the sum of amplitudes in the V0 scintillators for Xe–Xe collisions at sNN 5̄.44 TeV. The
distribution is fitted with the NBD-Glauber fit shown as a line. The inset shows a zoom of the most peripheral
region.

## PDF page 11

Centrality determination in heavy ion collisions

11

√
Table 3: Geometric properties (Npart , Ncoll , T PbPb ) of Xe–Xe collisions at sNN = 5.44 TeV for centrality classes
defined by sharp cuts in the V0M multiplicity distribution, simulated with an NBD-Glauber fit. The mean values,
the RMS, and the systematic uncertainties are obtained with a Glauber Monte Carlo calculation.
Centrality
0-2.5 %
2.5-5 %
5-7.5 %
7.5-10%
0-5%
5-10%
10-15 %
15-20 %
20-25 %
25-30 %
30-35 %
35-40 %
40-45 %
45-50 %
50-55 %
55-60 %
60-65 %
65-70 %
70-75 %
75-80 %
80-85 %
85-90 %
90-95 %
95-100 %
0-10%
10-20 %
20-30 %
30-40 %
40-50 %
50-60 %
60-70 %
70-80 %
80-90 %
90-100 %
0–20%
20–90%

⟨Npart ⟩
242.3
229.2
214.1
199.2
235.8
206.7
177.8
151.8
128.7
108.2
90.14
74.26
60.48
48.63
38.36
29.77
22.63
16.83
12.25
8.741
6.121
4.143
2.814
2.155
221.2
164.8
118.4
82.21
54.56
34.06
19.72
10.5
5.127
2.488
193
46.42

RMS
7.7
10
11
11
11
13
13
12
11
9.7
8.7
7.8
6.9
6.0
5.3
4.6
3.9
3.4
2.8
2.3
1.8
1.4
0.94
0.42
19
18
14
11
8.8
6.5
4.7
3.1
1.9
0.8
34
39

(sys.)
1.3
1.7
2.0
1.8
1.5
1.8
1.6
2.4
2.6
2.7
2.7
2.7
2.5
2.5
2.3
2.0
1.6
1.3
1.0
0.65
0.42
0.23
0.12
0.033
1.5
2.0
2.7
2.8
2.5
2.1
1.5
0.78
0.33
0.085
1.8
1.8

⟨Ncoll ⟩
1012
885.9
782.8
691.8
948.9
737.3
574.7
446.4
343.8
261.7
196.7
145.9
106.7
76.87
54.25
37.85
25.89
17.44
11.54
7.502
4.775
2.91
1.744
1.148
843.1
510.6
302.8
171.3
91.81
46.04
21.65
9.515
3.838
1.449
676.9
92.51

RMS
75
63
59
55
93
73
62
52
44
38
31
25
20
16
13
9.6
7.2
5.2
3.8
2.7
1.9
1.3
0.85
0.4
140
86
58
38
24
14
7.6
3.9
1.9
0.73
2e+02
1.1e+02

(sys.)
57
50
48
45
53
46
37
35
31
26
21
17
13
10
7.1
5.2
3.5
2.3
1.5
0.85
0.47
0.16
0.11
0.033
49
26
28
19
11
6.2
2.9
1.1
0.35
0.071
42
10

⟨T XeXe ⟩ (1/mbarn)
14.79
12.95
11.44
10.11
13.87
10.78
8.402
6.527
5.026
3.826
2.876
2.134
1.56
1.124
0.7932
0.5534
0.3785
0.255
0.1687
0.1097
0.06981
0.04255
0.0255
0.01679
12.33
7.465
4.426
2.505
1.342
0.6731
0.3166
0.1391
0.05611
0.02118
9.896
1.352

RMS (1/mbarn)
1.1
0.92
0.86
0.81
1.4
1.1
0.91
0.76
0.65
0.55
0.45
0.37
0.3
0.24
0.18
0.14
0.1
0.077
0.055
0.04
0.028
0.019
0.012
0.0058
2
1.3
0.85
0.56
0.35
0.2
0.11
0.056
0.028
0.011
2.9
1.5

(sys.) (1/mbarn)
0.85
0.71
0.70
0.65
0.78
0.67
0.54
0.51
0.45
0.39
0.31
0.25
0.19
0.15
0.11
0.078
0.052
0.035
0.021
0.013
0.0069
0.0035
0.0016
0.00049
0.71
0.52
0.42
0.28
0.17
0.091
0.043
0.017
0.0052
0.0011
0.62
0.14

## PDF page 12

mult ⟩
⟨Npart

242.3 ± 1.3
229.2 ± 1.7
214.1 ± 2.0
199.2 ± 2.8
164.8 ± 2.0
118.4 ± 2.7
82.21 ± 2.8
54.56 ± 2.5
34.06 ± 2.1
19.72 ± 1.5
10.5 ± 0.78
5.127 ± 0.33
2.488 ± 0.085

⟨Npart ⟩

geo

244 ± 1.3
229 ± 1.8
214 ± 1.9
199 ± 2.0
164 ± 2.2
118 ± 2.5
81.5± 2.5
54 ± 2.5
33.7± 2.0
19.8± 1.4
11 ± 0.71
6.28± 0.32
3.55± 0.01

Centrality

0-2.5%
2.5-5%
5-7.5%
7.5-10%
10-20%
20-30%
30-40%
40-50%
50-60%
60-70%
70-80%
80-90%
90-100%

geo

1.00702
0.999127
0.999533
0.998996
0.995146
0.996622
0.991364
0.989736
0.98943
1.00406
1.04762
1.22489
1.42685

mult ⟩
⟨Npart ⟩/ ⟨Npart

1010± 59
888 ± 54
784 ± 50
692 ± 46
509 ± 37
301 ± 28
170 ± 18
91.6± 11
46.5± 6.3
22.4± 3.1
10.5± 1.2
5.12± 0.43
2.44± 0.11

geo

⟨Ncoll ⟩
1012 ± 57
885.9 ± 50
782.8 ± 48
691.8 ± 45
510.6 ± 26
302.8 ± 28
171.3 ± 19
91.81 ± 11
46.04 ± 6.2
21.65 ± 2.9
9.515 ± 1.1
3.838 ± 0.35
1.449 ± 0.071

mult ⟩
⟨Ncoll

0.998024
1.00237
1.00153
1.00029
0.996866
0.994055
0.992411
0.997713
1.00999
1.03464
1.10352
1.33403
1.68392

geo

mult ⟩
⟨Ncoll ⟩/ ⟨Ncoll

14.8 ± 0.85
13 ± 0.78
11.5 ± 0.71
10.1 ± 0.66
7.45 ± 0.54
4.4 ± 0.39
2.49 ± 0.26
1.34 ± 0.16
0.68 ± 0.092
0.328 ± 0.045
0.154 ± 0.018
0.0749± 0.0064
0.0357± 0.0016

geo

⟨T PbPb ⟩
14.79 ± 0.84
12.95 ± 0.71
11.44 ± 0.70
10.11 ± 0.65
7.465 ± 0.52
4.426 ± 0.42
2.505 ± 0.28
1.342 ± 0.17
0.6731 ± 0.091
0.3166 ± 0.043
0.1391 ± 0.017
0.05611 ± 0.0052
0.02118 ± 0.0011

mult ⟩
⟨T PbPb

1.00068
1.00386
1.00524
0.999011
0.997991
0.994126
0.994012
0.99851
1.01025
1.03601
1.10712
1.33488
1.68555

geo

mult ⟩
⟨T PbPb ⟩/ ⟨T PbPb

12
ALICE Collaboration

## PDF page 13

Centrality determination in heavy ion collisions

6

p-Pb collisions at

√

13

sNN = 8.16 TeV

Events (arb. units)

Figure 6 shows the distribution of V0A amplitudes for all triggered p–Pb collisions with a vertex within
10 cm, fitted by a Glauber-NBD fit.

ALICE p-Pb sNN = 8.16 TeV
Data
NBD-Glauber fit

10−2

10−3
0

50

40-60%

−3

10

60-80%

80-100%

Npart x NBD (µ = 21.4, k = 0.44)

100

150

10-20%

0-5%

200

5-10%

0

20-40%

10−5

40-60%

60-80%

10−4

400

600

800

1000

V0A (Pb-side) amplitude (arb. units)
√
Fig. 6: Distribution of the sum of amplitudes in the V0A scintillators for p–Pb collisions at sNN 8̄.16 TeV. The
distribution is fitted with the NBD-Glauber fit shown as a line. The inset shows a zoom of the most peripheral
region.

√
Table 4 shows the geometric properties (Npart , Ncoll , T pPb ) of p–Pb collisions at sNN = 8.16 TeV for
centrality classes defined by sharp cuts in the V0A, V0M or CL1 multiplicity distribution, simulated with
an NBD-Glauber fit. The mean values, the RMS, and the systematic uncertainties are obtained with a
Glauber Monte Carlo calculation.
As describedd in [2], the hybrid method aims to provide an unbiased centrality estimator. It is based on
two assumptions, the first is that the event selection based on the energy deposited in the ZDC is free from
the biases due to a multiplicity selection. The second assumption is that some observables scale linearly
with Ncoll and Npart , allowing one to establish a relationship to the collision geometry. Two sets of ⟨Ncoll ⟩
mult ⟩ and ⟨N Pb−side ⟩ for each centrality bin i estimated using the energy deposited in
are calculated: ⟨Ncoll
coll
the neutron calorimeter on the Pb-going side (ZN). The first set is computed assuming that the chargedparticle multiplicity at mid-rapidity is proportional to the Npart . The second set is calculated using the
Pb-side multiplicity. A comparison of the Ncoll values obtained for the various estimators is reported
in the table. The two different sets are consistent among each other and with the values calculated for
Pb–p. The systematic uncertainties come from the uncertainty on the Ncoll for 0–100% summed with the
mult ⟩ and ⟨N Pb−side ⟩.
maximum difference between the ⟨Ncoll
coll
Figure 7 shows the distribution of the energy deposited in the Pb-going side (ZNA) calorimeter.
mult ⟩ and ⟨N Pb−side ⟩, the maximum difference among the two, and
Table 5 reports the mean values of ⟨Ncoll
coll
the total systematic uncertainty.

The T pPb values in Tab. 6 are calculated by dividing the Ncoll values by the cross-section σinel
NN . The
uncertainty is given by the quadrature sum of the maximum difference among the values calculated with

## PDF page 14

ALICE Collaboration

Events (a.u.)

14

80000
70000

ALICE p-Pb sNN = 8.16 TeV

60000
50000
40000

105

30000

Data

20000
10000
0
200 400 600 800 1000120014001600180020002200

0

5000

0-5 %

10-20 %
5-10 %

20-40 %

40-60 %

60-80 %

103

80-100 %

104

10000 15000 20000

EZN (GeV)
Fig. 7: Distribution of the energy deposited in the ZNA calorimeter.

different assumptions on the particle production mechanism, plus the uncerainty on the T pPb for 0–100%.

## PDF page 15

Centrality determination in heavy ion collisions

15

√
Table 4: Geometric properties (Npart , Ncoll , T pPb ) of p–Pb collisions at sNN = 8.16 TeV. The mean values, the
RMS, and the systematic uncertainties are obtained with a Glauber Monte Carlo calculation.
Centrality
0–100%

⟨Npart ⟩
8.118

RMS
4.8

(sys.)
0.12

⟨Ncoll ⟩
7.118

RMS
4.8

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

16.21
14.43
12.98
10.67
7.673
4.908
2.935
14.16
3.927
15.32
12.98
11.42
9.941
8.426
6.911
5.49
4.279
3.288
2.517

3.86
3.78
3.85
3.93
3.64
2.74
1.41
4.05
2.39
3.92
3.85
3.87
3.84
3.71
3.41
2.95
2.33
1.64
0.93

0.208
0.172
0.159
0.16
0.162
0.0902
0.0431
0.151
0.0523
0.179
0.159
0.164
0.147
0.153
0.153
0.115
0.0672
0.0412
0.0195

15.21
13.43
11.98
9.675
6.673
3.908
1.935
13.16
2.927
14.32
11.98
10.42
8.941
7.426
5.911
4.49
3.279
2.288
1.517

3.86
3.78
3.85
3.93
3.64
2.74
1.41
4.05
2.39
3.92
3.85
3.87
3.84
3.71
3.41
2.95
2.33
1.64
0.93

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

17.49
15.31
13.61
10.96
7.465
4.354
2.619
15.01
3.481
16.41
13.61
11.8
10.11
8.338
6.588
4.971
3.73
2.898
2.324

3.32
3.03
3.02
3.07
2.84
2.04
0.986
3.49
1.82
3.36
3.02
2.98
2.93
2.82
2.58
2.19
1.67
1.15
0.654

0.226
0.152
0.164
0.136
0.0833
0.0683
0.0153
0.161
0.0396
0.186
0.164
0.15
0.119
0.116
0.102
0.0965
0.0417
0.029
0.0193

16.49
14.31
12.61
9.957
6.465
3.354
1.619
14.01
2.481
15.41
12.61
10.8
9.106
7.338
5.588
3.971
2.73
1.898
1.324

3.32
3.03
3.02
3.07
2.84
2.04
0.986
3.49
1.82
3.36
3.02
2.98
2.93
2.82
2.58
2.19
1.67
1.15
0.654

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

17
15.01
13.38
10.81
7.475
4.495
2.709
14.7
3.636
16.02
13.38
11.66
9.982
8.301
6.693
5.153
3.887
2.995
2.388

3.54
3.32
3.36
3.44
3.18
2.31
1.12
3.71
2.04
3.58
3.36
3.35
3.33
3.22
2.95
2.52
1.92
1.31
0.749

0.353
0.282
0.187
0.166
0.191
0.143
0.113
0.24
0.0784
0.349
0.187
0.101
0.159
0.195
0.177
0.113
0.152
0.189
0.104

16
14.01
12.38
9.813
6.475
3.495
1.709
13.7
2.636
15.02
12.38
10.66
8.982
7.301
5.693
4.153
2.887
1.995
1.388

3.54
3.32
3.36
3.44
3.18
2.31
1.12
3.71
2.04
3.58
3.36
3.35
3.33
3.22
2.95
2.52
1.92
1.31
0.749

(sys.)
0.12
V0A
0.208
0.172
0.159
0.16
0.162
0.0902
0.0431
0.151
0.0523
0.179
0.159
0.164
0.147
0.153
0.153
0.115
0.0672
0.0412
0.0195
V0M
0.226
0.152
0.164
0.136
0.0833
0.0683
0.0153
0.161
0.0396
0.186
0.164
0.15
0.119
0.116
0.102
0.0965
0.0417
0.029
0.0193
CL1
0.353
0.282
0.187
0.166
0.191
0.143
0.113
0.24
0.0784
0.349
0.187
0.101
0.159
0.195
0.177
0.113
0.152
0.189
0.104

⟨T pPb ⟩ (1/mbarn)
0.09818

RMS (1/mbarn)
0.071

(sys.) (1/mbarn)
0.002

0.2098
0.1853
0.1653
0.1334
0.09204
0.0539
0.02669
0.1814
0.04037
0.1975
0.1653
0.1437
0.1233
0.1024
0.08153
0.06194
0.04522
0.03155
0.02093

0.0532
0.0521
0.0531
0.0541
0.0503
0.0378
0.0195
0.0559
0.033
0.0541
0.0531
0.0534
0.053
0.0512
0.0471
0.0407
0.0322
0.0226
0.0128

0.00243
0.00198
0.002
0.00218
0.00226
0.00116
0.000548
0.00177
0.000694
0.002
0.002
0.0021
0.00198
0.00216
0.00211
0.00155
0.000843
0.00049
0.000278

0.2275
0.1974
0.1739
0.1373
0.08917
0.04626
0.02233
0.1932
0.03422
0.2126
0.1739
0.149
0.1256
0.1012
0.07707
0.05478
0.03766
0.02618
0.01827

0.0458
0.0418
0.0417
0.0424
0.0392
0.0282
0.0136
0.0481
0.0251
0.0464
0.0417
0.0411
0.0404
0.0389
0.0356
0.0302
0.023
0.0159
0.00903

0.00271
0.00173
0.00199
0.00183
0.00128
0.000952
0.000239
0.00187
0.000535
0.00217
0.00199
0.00196
0.00169
0.00175
0.00155
0.00134
0.00059
0.000442
0.000285

0.2207
0.1932
0.1708
0.1353
0.08931
0.04821
0.02358
0.1889
0.03636
0.2072
0.1708
0.147
0.1239
0.1007
0.07853
0.05728
0.03981
0.02752
0.01914

0.0489
0.0459
0.0463
0.0475
0.0439
0.0319
0.0154
0.0511
0.0281
0.0493
0.0463
0.0462
0.0459
0.0444
0.0408
0.0347
0.0264
0.018
0.0103

0.00471
0.00371
0.00209
0.00211
0.00259
0.00197
0.00158
0.0029
0.00103
0.00457
0.00209
0.000995
0.00229
0.00263
0.00233
0.00147
0.00209
0.00263
0.00145

## PDF page 16

16

ALICE Collaboration

Table 5: ⟨Ncoll ⟩ values of p–Pb collisions at
Centrality
0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%
0–2%
2–10%
0–20%
60-100%
80–90%
0–90%

mult
Ncoll
13.4
12.5
11.5
9.81
7.09
4.28
2.05
12.9
11.5
10.4
9.21
7.82
6.37
4.93
3.63
2.53
1.58
13.9
12.7
12.2
3.17
2.53
7.71

sNN = 8.16 TeV obtained with the hybrid method.

Pb−side
Ncoll
14.2
12.9
11.8
9.77
6.83
4.09
2.10
13.6
11.8
10.5
9.09
7.58
6.09
4.69
3.48
2.51
1.70
14.7
13.3
12.7
3.10
2.51
7.70

Table 6: ⟨T pPb ⟩ values of p–Pb collisions at
Centrality
0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%
0–2%
2–10%
0–20%
60-100%
80–90%
0–90%

√

√

max diff (%)
6.0
3.2
2.5
0.4
3.7
4.3
2.4
5.4
2.5
1.0
1.3
3.1
4.4
4.9
4.1
0.8
7.6
5.4
4.5
3.9
2.2
0.8
0.1

tot sys (%)
6.2
3.6
3.1
1.7
4.1
4.6
2.9
5.7
3.0
1.8
2.0
3.4
4.6
5.1
4.4
1.7
7.7
5.6
4.8
4.3
2.8
1.9
1.7

sNN = 8.16 TeV obtained with the hybrid method.

mult
T pPb

Pb−side
T pPb

0.185
0.172
0.159
0.135
0.0978
0.0590
0.0287
0.178
0.159
0.143
0.127
0.108
0.0879
0.0680
0.0501
0.0349
0.0218
0.192
0.175
0.168
0.0437
0.0349
0.106

0.195
0.178
0.163
0.135
0.0942
0.0564
0.0294
0.188
0.163
0.145
0.125
0.105
0.0834
0.0647
0.0480
0.0346
0.0234
0.203
0.183
0.175
0.0427
0.0346
0.106

max diff (%)
6.0
3.2
2.5
0.4
3.7
4.3
2.4
5.4
2.5
1.0
1.3
3.1
4.4
4.9
4.1
0.8
7.6
5.4
4.5
3.9
2.2
0.8
0.1

tot sys (%)
6.4
3.8
3.3
2.1
4.2
4.8
3.1
5.8
3.2
2.2
2.4
3.7
4.8
5.3
4.6
2.1
7.8
5.6
4.8
4.4
3.0
1.9
1.7

## PDF page 17

Centrality determination in heavy ion collisions

7

p-Pb collisions at

√

17

sNN = 5.02 TeV

√
Table 7 shows the geometric properties (Npart , Ncoll , T pPb ) of p–Pb collisions at sNN = 5.02 TeV for
centrality classes defined by sharp cuts in the V0A, V0M or CL1 multiplicity distribution.
For the calculations with the hybrid method we use another assumption on particle production, namely
that the yield of charged high-pt particles at mid-rapidity is proportional to the number of binary NN
high−p
collisions (Ncoll ), in order to calculate the set of Ncoll t , restricted however only to the classes with the
pt -spectra were calculated, or those which can be derived with weigthed average.

## PDF page 18

18

ALICE Collaboration

√
Table 7: Geometric properties (Npart , Ncoll , T pPb ) of p–Pb collisions at sNN = 5.02 TeV. The mean values, the
RMS, and the systematic uncertainties are obtained with a Glauber Monte Carlo calculation.
Centrality
0–100%

⟨Npart ⟩
7.708

RMS
4.8

(sys.)
0.11

⟨Ncoll ⟩
6.708

RMS
4.8

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

15.1
13.47
12.18
10.09
7.42
4.884
2.982
13.23
3.93
14.29
12.18
10.76
9.451
8.075
6.755
5.437
4.306
3.365
2.571

3.77
3.7
3.78
3.84
3.57
2.73
1.47
3.94
2.38
3.82
3.78
3.8
3.77
3.64
3.38
2.93
2.37
1.72
0.995

0.747
0.687
0.612
0.472
0.272
0.0974
0.0331
0.673
0.1
0.712
0.612
0.542
0.391
0.333
0.222
0.186
0.0731
0.0628
0.0287

14.1
12.47
11.18
9.089
6.42
3.884
1.982
12.23
2.93
13.29
11.18
9.759
8.451
7.075
5.755
4.437
3.306
2.365
1.571

3.77
3.7
3.78
3.84
3.57
2.73
1.47
3.94
2.38
3.82
3.78
3.8
3.77
3.64
3.38
2.93
2.37
1.72
0.995

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

16.51
14.44
12.87
10.4
7.169
4.253
2.6
14.18
3.434
15.47
12.87
11.18
9.613
7.994
6.325
4.85
3.682
2.876
2.323

3.2
2.94
2.91
2.95
2.76
1.98
0.968
3.34
1.77
3.24
2.91
2.87
2.83
2.74
2.51
2.13
1.64
1.14
0.653

0.804
0.695
0.626
0.474
0.251
0.112
0.0373
0.69
0.0639
0.749
0.626
0.546
0.417
0.288
0.214
0.137
0.0682
0.0607
0.0248

15.51
13.44
11.87
9.396
6.169
3.253
1.6
13.18
2.434
14.47
11.87
10.18
8.613
6.994
5.325
3.85
2.682
1.876
1.323

3.2
2.94
2.91
2.95
2.76
1.98
0.968
3.34
1.77
3.24
2.91
2.87
2.83
2.74
2.51
2.13
1.64
1.14
0.653

0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–20%
60–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%

15.97
14.05
12.62
10.31
7.273
4.485
2.744
13.85
3.624
15.01
12.62
11.03
9.54
7.998
6.476
5.077
3.914
3.077
2.441

3.41
3.25
3.27
3.33
3.13
2.29
1.16
3.57
2.01
3.46
3.27
3.26
3.23
3.16
2.89
2.47
1.94
1.38
0.821

0.856
0.743
0.607
0.458
0.28
0.187
0.0863
0.678
0.128
0.773
0.607
0.529
0.42
0.324
0.241
0.249
0.208
0.157
0.105

14.97
13.05
11.62
9.312
6.273
3.485
1.744
12.85
2.624
14.01
11.62
10.03
8.54
6.998
5.476
4.077
2.914
2.077
1.441

3.41
3.25
3.27
3.33
3.13
2.29
1.16
3.57
2.01
3.46
3.27
3.26
3.23
3.16
2.89
2.47
1.94
1.38
0.821

(sys.)
0.11
V0A
0.747
0.687
0.612
0.472
0.272
0.0974
0.0331
0.673
0.1
0.712
0.612
0.542
0.391
0.333
0.222
0.186
0.0731
0.0628
0.0287
V0M
0.804
0.695
0.626
0.474
0.251
0.112
0.0373
0.69
0.0639
0.749
0.626
0.546
0.417
0.288
0.214
0.137
0.0682
0.0607
0.0248
CL1
0.856
0.743
0.607
0.458
0.28
0.187
0.0863
0.678
0.128
0.773
0.607
0.529
0.42
0.324
0.241
0.249
0.208
0.157
0.105

⟨T pPb ⟩ (1/mbarn)
0.09923

RMS (1/mbarn)
0.071

(sys.) (1/mbarn)
0.0017

0.2085
0.1845
0.1654
0.1345
0.09496
0.05745
0.02932
0.181
0.04334
0.1966
0.1654
0.1444
0.125
0.1047
0.08513
0.06564
0.04891
0.03499
0.02324

0.0557
0.0547
0.0559
0.0568
0.0529
0.0404
0.0217
0.0583
0.0353
0.0565
0.0559
0.0562
0.0557
0.0538
0.05
0.0434
0.035
0.0254
0.0147

0.00997
0.00919
0.00813
0.00624
0.00357
0.00127
0.000468
0.00898
0.00138
0.0095
0.00813
0.00715
0.00508
0.00441
0.0029
0.00258
0.00105
0.000889
0.00038

0.2294
0.1989
0.1757
0.139
0.09125
0.04812
0.02367
0.1949
0.03601
0.2141
0.1757
0.1506
0.1274
0.1035
0.07878
0.05696
0.03968
0.02775
0.01957

0.0473
0.0435
0.043
0.0437
0.0408
0.0294
0.0143
0.0494
0.0262
0.0479
0.043
0.0425
0.0418
0.0406
0.0372
0.0316
0.0243
0.0168
0.00966

0.0107
0.00922
0.00825
0.00623
0.00327
0.00151
0.000552
0.00913
0.00082
0.00997
0.00825
0.00723
0.00545
0.00373
0.00284
0.00177
0.000846
0.000879
0.000344

0.2214
0.193
0.1719
0.1377
0.0928
0.05156
0.02579
0.1901
0.03881
0.2073
0.1719
0.1483
0.1263
0.1035
0.081
0.06031
0.04311
0.03073
0.02132

0.0505
0.048
0.0483
0.0492
0.0462
0.0339
0.0172
0.0528
0.0298
0.0512
0.0483
0.0483
0.0478
0.0467
0.0428
0.0366
0.0287
0.0204
0.0121

0.0118
0.0102
0.00815
0.00599
0.0037
0.00255
0.00116
0.00913
0.00181
0.0106
0.00815
0.00707
0.00551
0.00426
0.00329
0.00353
0.00291
0.00224
0.00154

## PDF page 19

Centrality determination in heavy ion collisions

Table 8: ⟨Ncoll ⟩ values of p–Pb collisions at
Centrality
0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%
0–2%
2–10%
0–20%
60-100%
80–90%
0–90%

mult
Ncoll
11.9
11.3
10.7
9.29
6.87
4.17
2.03
11.6
10.7
9.82
8.76
7.57
6.17
4.80
3.55
2.39
1.58
12.4
11.4
11.1
3.10
2.09
6.50

high−p
Ncoll t

12.2
11.8
11.0
9.45
6.62
3.93
1.97
12.0
11.0
11.5
2.95
-

Table 9: ⟨T pPb ⟩ values of p–Pb collisions at
Centrality
0–5%
5–10%
10–20%
20–40%
40–60%
60–80%
80–100%
0–10%
10–20%
20–30%
30–40%
40–50%
50–60%
60–70%
70–80%
80–90%
90–100%
0–2%
2–10%
0–20%
60-100%
80–90%
0–90%

mult
T pPb
0.176
0.167
0.158
0.137
0.102
0.0617
0.0300
0.172
0.158
0.145
0.130
0.112
0.0913
0.0710
0.0525
0.0353
0.0234
0.183
0.169
0.164
0.0459
0.0309
0.0961

high−p
T pPb t

0.180
0.174
0.163
0.140
0.0979
0.0581
0.0291
0.178
0.163
0.170
0.0436
-

19

√

sNN = 5.02 TeV obtained with the hybrid method.

Pb−side
Ncoll
12.9
11.9
11.1
9.32
6.54
3.89
2.00
12.4
11.1
9.94
8.69
7.29
5.80
4.45
3.30
2.37
1.63
13.2
12.2
11.7
2.94
1.98
6.50

√

max diff (%)
8.4
5.3
3.7
1.7
4.8
6.9
2.9
6.9
3.7
1.2
0.8
3.7
6.0
7.3
7.0
0.8
3.2
6.4
7.0
5.4
5.2
5.3
0.0

tot sys (%)
8.6
5.5
4.1
2.4
5.1
7.1
3.3
7.1
4.1
2.0
1.8
4.0
6.2
7.5
7.2
1.8
3.6
6.6
7.2
5.6
5.4
5.5
1.6

sNN = 5.02 TeV obtained with the hybrid method.
Pb−side
T pPb
0.191
0.176
0.164
0.138
0.0967
0.0575
0.0296
0.183
0.164
0.147
0.129
0.108
0.0858
0.0658
0.0488
0.0351
0.0241
0.195
0.180
0.173
0.0435
0.0293
0.0961

max diff (%)
8.4
5.3
3.7
1.7
4.8
6.9
2.9
6.9
3.7
1.2
0.8
3.7
6.0
7.3
7.0
0.8
3.2
6.4
7.0
5.4
5.2
5.3
0.0

tot sys (%)
8.6
5.6
4.1
2.4
5.1
7.1
3.4
7.1
4.1
2.1
1.9
4.1
6.2
7.5
7.2
1.9
3.6
6.6
7.2
5.7
5.4
5.5
1.6

## PDF page 20

20

ALICE Collaboration

Acknowledgements
The ALICE Collaboration would like to thank all its engineers and technicians for their invaluable
contributions to the construction of the experiment and the CERN accelerator teams for the outstanding
performance of the LHC complex. The ALICE Collaboration gratefully acknowledges the resources
and support provided by all Grid centres and the Worldwide LHC Computing Grid (WLCG)
collaboration. The ALICE Collaboration acknowledges the following funding agencies for their support
in building and running the ALICE detector: A. I. Alikhanyan National Science Laboratory (Yerevan
Physics Institute) Foundation (ANSL), State Committee of Science and World Federation of Scientists
(WFS), Armenia; Austrian Academy of Sciences, Austrian Science Fund (FWF): [M 2467-N36] and
Nationalstiftung für Forschung, Technologie und Entwicklung, Austria; Ministry of Communications
and High Technologies, National Nuclear Research Center, Azerbaijan; Conselho Nacional de
Desenvolvimento Científico e Tecnológico (CNPq), Financiadora de Estudos e Projetos (Finep),
Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP) and Universidade Federal do Rio
Grande do Sul (UFRGS), Brazil; Ministry of Education of China (MOEC) , Ministry of Science &
Technology of China (MSTC) and National Natural Science Foundation of China (NSFC), China;
Ministry of Science and Education and Croatian Science Foundation, Croatia; Centro de Aplicaciones
Tecnológicas y Desarrollo Nuclear (CEADEN), Cubaenergía, Cuba; Ministry of Education, Youth and
Sports of the Czech Republic, Czech Republic; The Danish Council for Independent Research | Natural
Sciences, the VILLUM FONDEN and Danish National Research Foundation (DNRF), Denmark;
Helsinki Institute of Physics (HIP), Finland; Commissariat à l’Energie Atomique (CEA) and Institut
National de Physique Nucléaire et de Physique des Particules (IN2P3) and Centre National de la
Recherche Scientifique (CNRS), France; Bundesministerium für Bildung und Forschung (BMBF) and
GSI Helmholtzzentrum für Schwerionenforschung GmbH, Germany; General Secretariat for Research
and Technology, Ministry of Education, Research and Religions, Greece; National Research,
Development and Innovation Office, Hungary; Department of Atomic Energy Government of India
(DAE), Department of Science and Technology, Government of India (DST), University Grants
Commission, Government of India (UGC) and Council of Scientific and Industrial Research (CSIR),
India; Indonesian Institute of Science, Indonesia; Istituto Nazionale di Fisica Nucleare (INFN), Italy;
Institute for Innovative Science and Technology , Nagasaki Institute of Applied Science (IIST),
Japanese Ministry of Education, Culture, Sports, Science and Technology (MEXT) and Japan Society
for the Promotion of Science (JSPS) KAKENHI, Japan; Consejo Nacional de Ciencia (CONACYT) y
Tecnología, through Fondo de Cooperación Internacional en Ciencia y Tecnología (FONCICYT) and
Dirección General de Asuntos del Personal Academico (DGAPA), Mexico; Nederlandse Organisatie
voor Wetenschappelijk Onderzoek (NWO), Netherlands; The Research Council of Norway, Norway;
Commission on Science and Technology for Sustainable Development in the South (COMSATS),
Pakistan; Pontificia Universidad Católica del Perú, Peru; Ministry of Science and Higher Education,
National Science Centre and WUT ID-UB, Poland; Korea Institute of Science and Technology
Information and National Research Foundation of Korea (NRF), Republic of Korea; Ministry of
Education and Scientific Research, Institute of Atomic Physics and Ministry of Research and
Innovation and Institute of Atomic Physics, Romania; Joint Institute for Nuclear Research (JINR),
Ministry of Education and Science of the Russian Federation, National Research Centre Kurchatov
Institute, Russian Science Foundation and Russian Foundation for Basic Research, Russia; Ministry of
Education, Science, Research and Sport of the Slovak Republic, Slovakia; National Research
Foundation of South Africa, South Africa; Swedish Research Council (VR) and Knut & Alice
Wallenberg Foundation (KAW), Sweden; European Organization for Nuclear Research, Switzerland;
Suranaree University of Technology (SUT), National Science and Technology Development Agency
(NSDTA) and Office of the Higher Education Commission under NRU project of Thailand, Thailand;
Turkish Atomic Energy Agency (TAEK), Turkey; National Academy of Sciences of Ukraine, Ukraine;
Science and Technology Facilities Council (STFC), United Kingdom; National Science Foundation of

## PDF page 21

Centrality determination in heavy ion collisions

21

the United States of America (NSF) and United States Department of Energy, Office of Nuclear Physics
(DOE NP), United States of America.

References
√
[1] ALICE Collaboration, B. Abelev et al., “Centrality determination of Pb-Pb collisions at sNN =
2.76 TeV with ALICE,” Phys.Rev. C88 no. 4, (2013) 044909, arXiv:1301.4361 [nucl-ex].
[2] ALICE Collaboration, J. Adam et al., “Centrality dependence of particle production in p-Pb
√
collisions at sNN = 5.02 TeV,” Phys. Rev. C91 no. 6, (2015) 064905, arXiv:1412.6828
[nucl-ex].
[3] M. Miller, K. Reygers, S. J. Sanders, and P. Steinberg, “Glauber modeling in high energy nuclear
collisions,” Ann. Rev. Nucl. Part. Sci. 57 (2007) 205–243, arXiv:nucl-ex/0701025.
[4] R. Glauber, “Cross sections in deuterium at high energies,” Phys. Rev. 100 (1955) 242.
[5] R. Glauber, “Lectures in theoretical physics,” ed WE Brittin and LG Dunham 1 (1959) 315.
[6] R. Glauber, “Quantum optics and heavy ion physics,” Nucl. Phys. A 774 (2006) 3.
[7] A. P. T.W. Ludlam and A. Shor, “Hijet. a monte carlo event generator for p–nucleus and
nucleus–nucleus collisions,” BNL 37196 (1985) 373–381.
[8] A. Shor and R. Longacre, “Effects of secondary interactions in proton-nucleus and
nucleus-nucleus collisions using the hijet event generator,” Phys. Lett. B 218 (1989) 100.
[9] B. Alver, M. Baker, C. Loizides, and P. Steinberg, “The PHOBOS Glauber Monte Carlo,”
arXiv:0805.4411 [nucl-ex].
[10] H. De Vries, C. W. De Jager, and C. De Vries, “Nuclear charge and magnetization density
distribution parameters from elastic electron scattering,” Atom. Data Nucl. Data Tabl. 36 (1987)
495–536.
[11] C. Loizides, J. Kamin, and D. d’Enterria, “Precision Monte Carlo Glauber predictions at present
and future nuclear colliders,” arXiv:1710.07098 [nucl-ex].
[12] ALICE Collaboration, K. Aamodt et al., “First proton-proton collisions at the LHC as observed
with the ALICE detector: Measurement of the charged particle pseudorapidity density at s**(1/2)
= 900-GeV,” Eur. Phys. J. C 65 (2010) 111–125, arXiv:0911.5430 [hep-ex].
[13] ALICE Collaboration, K. Aamodt et al., “Charged-particle multiplicity measurement in
√
proton-proton collisions at s = 0.9 and 2.36 TeV with ALICE at LHC,” Eur. Phys. J. C 68 (2010)
89–108, arXiv:1004.3034 [hep-ex].
[14] D. Kharzeev, E. Levin, and M. Nardi, “Color glass condensate at the LHC: Hadron multiplicities
in p p, p A and A A collisions,” Nucl. Phys. A747 (2005) 609–629, arXiv:hep-ph/0408050.
[15] W. Deng, X. Wang, and R. Xu, “Hadron production in p + p, p + Pb and Pb + Pb collisions at the
LHC energies with HIJING2.0 model,” arXiv:1008.1841 [hep-ph].

## PDF page 22

22

A

ALICE Collaboration

The ALICE Collaboration

ALICE Collaboration
S. Acharya142 , D. Adamová97 , A. Adler75 , J. Adolfsson82 , G. Aglieri Rinella35 , M. Agnello31 ,
N. Agrawal55 , Z. Ahammed142 , S. Ahmad16 , S.U. Ahn77 , Z. Akbar52 , A. Akindinov94 ,
M. Al-Turany109 , D.S.D. Albuquerque124 , D. Aleksandrov90 , B. Alessandro60 , H.M. Alfanda7 ,
R. Alfaro Molina72 , B. Ali16 , Y. Ali14 , A. Alici26 , N. Alizadehvandchali127 , A. Alkin35 , J. Alme21 ,
T. Alt69 , L. Altenkamper21 , I. Altsybeev115 , M.N. Anaam7 , C. Andrei49 , D. Andreou92 , A. Andronic145 ,
M. Angeletti35 , V. Anguelov106 , T. Antičić110 , F. Antinori58 , P. Antonioli55 , N. Apadula81 ,
L. Aphecetche117 , H. Appelshäuser69 , S. Arcelli26 , R. Arnaldi60 , M. Arratia81 , I.C. Arsene20 ,
M. Arslandok147,106 , A. Augustinus35 , R. Averbeck109 , S. Aziz79 , M.D. Azmi16 , A. Badalà57 ,
Y.W. Baek42 , X. Bai109 , R. Bailhache69 , R. Bala103 , A. Balbino31 , A. Baldisseri139 , M. Ball44 ,
D. Banerjee4 , R. Barbera27 , L. Barioglio25 , M. Barlou86 , G.G. Barnaföldi146 , L.S. Barnby96 ,
V. Barret136 , C. Bartels129 , K. Barth35 , E. Bartsch69 , F. Baruffaldi28 , N. Bastid136 , S. Basu82,144 ,
G. Batigne117 , B. Batyunya76 , D. Bauri50 , J.L. Bazo Alba114 , I.G. Bearden91 , C. Beattie147 ,
I. Belikov138 , A.D.C. Bell Hechavarria145 , F. Bellini35 , R. Bellwied127 , S. Belokurova115 , V. Belyaev95 ,
G. Bencedi70,146 , S. Beole25 , A. Bercuci49 , Y. Berdnikov100 , A. Berdnikova106 , D. Berenyi146 ,
L. Bergmann106 , M.G. Besoiu68 , L. Betev35 , P.P. Bhaduri142 , A. Bhasin103 , I.R. Bhat103 , M.A. Bhat4 ,
B. Bhattacharjee43 , P. Bhattacharya23 , A. Bianchi25 , L. Bianchi25 , N. Bianchi53 , J. Bielčík38 ,
J. Bielčíková97 , A. Bilandzic107 , G. Biro146 , S. Biswas4 , J.T. Blair121 , D. Blau90 , M.B. Blidaru109 ,
C. Blume69 , G. Boca29 , F. Bock98 , A. Bogdanov95 , S. Boi23 , J. Bok62 , L. Boldizsár146 ,
A. Bolozdynya95 , M. Bombara39 , G. Bonomi141 , H. Borel139 , A. Borissov83,95 , H. Bossi147 , E. Botta25 ,
L. Bratrud69 , P. Braun-Munzinger109 , M. Bregant123 , M. Broz38 , G.E. Bruno108,34 , M.D. Buckland129 ,
D. Budnikov111 , H. Buesching69 , S. Bufalino31 , O. Bugnon117 , P. Buhler116 , P. Buncic35 ,
Z. Buthelezi73,133 , J.B. Butt14 , S.A. Bysiak120 , D. Caffarri92 , A. Caliva109 , E. Calvo Villar114 ,
J.M.M. Camacho122 , R.S. Camacho46 , P. Camerini24 , F.D.M. Canedo123 , A.A. Capon116 ,
F. Carnesecchi26 , R. Caron139 , J. Castillo Castellanos139 , E.A.R. Casula56 , F. Catalano31 , C. Ceballos
Sanchez76 , P. Chakraborty50 , S. Chandra142 , W. Chang7 , S. Chapeland35 , M. Chartier129 ,
S. Chattopadhyay142 , S. Chattopadhyay112 , A. Chauvin23 , C. Cheshkov137 , B. Cheynis137 , V. Chibante
Barroso35 , D.D. Chinellato124 , S. Cho62 , P. Chochula35 , P. Christakoglou92 , C.H. Christensen91 ,
P. Christiansen82 , T. Chujo135 , C. Cicalo56 , L. Cifarelli26 , F. Cindolo55 , M.R. Ciupek109 , G. ClaiII,55 ,
J. Cleymans126 , F. Colamaria54 , J.S. Colburn113 , D. Colella54 , A. Collu81 , M. Colocci35,26 ,
M. ConcasIII,60 , G. Conesa Balbastre80 , Z. Conesa del Valle79 , G. Contin24 , J.G. Contreras38 ,
T.M. Cormier98 , P. Cortese32 , M.R. Cosentino125 , F. Costa35 , S. Costanza29 , P. Crochet136 , E. Cuautle70 ,
P. Cui7 , L. Cunqueiro98 , T. Dahms107 , A. Dainese58 , F.P.A. Damas117,139 , M.C. Danisch106 , A. Danu68 ,
D. Das112 , I. Das112 , P. Das88 , P. Das4 , S. Das4 , S. Dash50 , S. De88 , A. De Caro30 , G. de Cataldo54 ,
L. De Cilladi25 , J. de Cuveland40 , A. De Falco23 , D. De Gruttola30 , N. De Marco60 , C. De Martin24 ,
S. De Pasquale30 , S. Deb51 , H.F. Degenhardt123 , K.R. Deja143 , S. Delsanto25 , W. Deng7 , P. Dhankher50 ,
D. Di Bari34 , A. Di Mauro35 , R.A. Diaz8 , T. Dietel126 , P. Dillenseger69 , Y. Ding7 , R. Divià35 ,
D.U. Dixit19 , Ø. Djuvsland21 , U. Dmitrieva64 , J. Do62 , A. Dobrin68 , B. Dönigus69 , O. Dordic20 ,
A.K. Dubey142 , A. Dubla109,92 , S. Dudi102 , M. Dukhishyam88 , P. Dupieux136 , T.M. Eder145 ,
R.J. Ehlers98 , V.N. Eikeland21 , D. Elia54 , B. Erazmus117 , F. Erhardt101 , A. Erokhin115 , M.R. Ersdal21 ,
B. Espagnon79 , G. Eulisse35 , D. Evans113 , S. Evdokimov93 , L. Fabbietti107 , M. Faggin28 , J. Faivre80 ,
F. Fan7 , A. Fantoni53 , M. Fasel98 , P. Fecchio31 , A. Feliciello60 , G. Feofilov115 , A. Fernández Téllez46 ,
A. Ferrero139 , A. Ferretti25 , A. Festanti35 , V.J.G. Feuillard106 , J. Figiel120 , S. Filchagin111 ,
D. Finogeev64 , F.M. Fionda21 , G. Fiorenza54 , F. Flor127 , A.N. Flores121 , S. Foertsch73 , P. Foka109 ,
S. Fokin90 , E. Fragiacomo61 , U. Fuchs35 , C. Furget80 , A. Furs64 , M. Fusco Girard30 , J.J. Gaardhøje91 ,
M. Gagliardi25 , A.M. Gago114 , A. Gal138 , C.D. Galvan122 , P. Ganoti86 , C. Garabatos109 ,
J.R.A. Garcia46 , E. Garcia-Solis10 , K. Garg117 , C. Gargiulo35 , A. Garibli89 , K. Garner145 , P. Gasik107 ,

## PDF page 23

Centrality determination in heavy ion collisions

23

E.F. Gauger121 , M.B. Gay Ducati71 , M. Germain117 , J. Ghosh112 , P. Ghosh142 , S.K. Ghosh4 ,
M. Giacalone26 , P. Gianotti53 , P. Giubellino109,60 , P. Giubilato28 , A.M.C. Glaenzer139 , P. Glässel106 ,
V. Gonzalez144 , L.H. González-Trueba72 , S. Gorbunov40 , L. Görlich120 , S. Gotovac36 , V. Grabski72 ,
L.K. Graczykowski143 , K.L. Graham113 , L. Greiner81 , A. Grelli63 , C. Grigoras35 , V. Grigoriev95 ,
A. GrigoryanI,1 , S. Grigoryan76 , O.S. Groettvik21 , F. Grosa60 , J.F. Grosse-Oetringhaus35 , R. Grosso109 ,
R. Guernane80 , M. Guilbaud117 , M. Guittiere117 , K. Gulbrandsen91 , T. Gunji134 , A. Gupta103 ,
R. Gupta103 , I.B. Guzman46 , R. Haake147 , M.K. Habib109 , C. Hadjidakis79 , H. Hamagaki84 ,
G. Hamar146 , M. Hamid7 , R. Hannigan121 , M.R. Haque143,88 , A. Harlenderova109 , J.W. Harris147 ,
A. Harton10 , J.A. Hasenbichler35 , H. Hassan98 , D. Hatzifotiadou55 , P. Hauer44 , L.B. Havener147 ,
S. Hayashi134 , S.T. Heckel107 , E. Hellbär69 , H. Helstrup37 , T. Herman38 , E.G. Hernandez46 , G. Herrera
Corral9 , F. Herrmann145 , K.F. Hetland37 , H. Hillemanns35 , C. Hills129 , B. Hippolyte138 ,
B. Hohlweger107 , J. Honermann145 , G.H. Hong148 , D. Horak38 , S. Hornung109 , R. Hosokawa15 ,
P. Hristov35 , C. Huang79 , C. Hughes132 , P. Huhn69 , T.J. Humanic99 , H. Hushnud112 , L.A. Husova145 ,
N. Hussain43 , D. Hutter40 , J.P. Iddon35,129 , R. Ilkaev111 , H. Ilyas14 , M. Inaba135 , G.M. Innocenti35 ,
M. Ippolitov90 , A. Isakov38,97 , M.S. Islam112 , M. Ivanov109 , V. Ivanov100 , V. Izucheev93 , B. Jacak81 ,
N. Jacazio35,55 , P.M. Jacobs81 , S. Jadlovska119 , J. Jadlovsky119 , S. Jaelani63 , C. Jahnke123 ,
M.J. Jakubowska143 , M.A. Janik143 , T. Janson75 , M. Jercic101 , O. Jevons113 , M. Jin127 , F. Jonas98,145 ,
P.G. Jones113 , J. Jung69 , M. Jung69 , A. Jusko113 , P. Kalinak65 , A. Kalweit35 , V. Kaplin95 , S. Kar7 ,
A. Karasu Uysal78 , D. Karatovic101 , O. Karavichev64 , T. Karavicheva64 , P. Karczmarczyk143 ,
E. Karpechev64 , A. Kazantsev90 , U. Kebschull75 , R. Keidel48 , M. Keil35 , B. Ketzer44 , Z. Khabanova92 ,
A.M. Khan7 , S. Khan16 , A. Khanzadeev100 , Y. Kharlov93 , A. Khatun16 , A. Khuntia120 , B. Kileng37 ,
B. Kim62 , D. Kim148 , D.J. Kim128 , E.J. Kim74 , H. Kim17 , J. Kim148 , J.S. Kim42 , J. Kim106 , J. Kim148 ,
J. Kim74 , M. Kim106 , S. Kim18 , T. Kim148 , T. Kim148 , S. Kirsch69 , I. Kisel40 , S. Kiselev94 , A. Kisiel143 ,
J.L. Klay6 , J. Klein35,60 , S. Klein81 , C. Klein-Bösing145 , M. Kleiner69 , T. Klemenz107 , A. Kluge35 ,
A.G. Knospe127 , C. Kobdaj118 , M.K. Köhler106 , T. Kollegger109 , A. Kondratyev76 , N. Kondratyeva95 ,
E. Kondratyuk93 , J. Konig69 , S.A. Konigstorfer107 , P.J. Konopka2,35 , G. Kornakov143 , S.D. Koryciak2 ,
L. Koska119 , O. Kovalenko87 , V. Kovalenko115 , M. Kowalski120 , I. Králik65 , A. Kravčáková39 ,
L. Kreis109 , M. Krivda113,65 , F. Krizek97 , K. Krizkova Gajdosova38 , M. Kroesen106 , M. Krüger69 ,
E. Kryshen100 , M. Krzewicki40 , V. Kučera35 , C. Kuhn138 , P.G. Kuijer92 , T. Kumaoka135 , L. Kumar102 ,
S. Kundu88 , P. Kurashvili87 , A. Kurepin64 , A.B. Kurepin64 , A. Kuryakin111 , S. Kushpil97 , J. Kvapil113 ,
M.J. Kweon62 , J.Y. Kwon62 , Y. Kwon148 , S.L. La Pointe40 , P. La Rocca27 , Y.S. Lai81 , A. Lakrathok118 ,
M. Lamanna35 , R. Langoy131 , K. Lapidus35 , P. Larionov53 , E. Laudi35 , L. Lautner35 , R. Lavicka38 ,
T. Lazareva115 , R. Lea24 , J. Lee135 , S. Lee148 , J. Lehrbach40 , R.C. Lemmon96 , I. León Monzón122 ,
E.D. Lesser19 , M. Lettrich35 , P. Lévai146 , X. Li11 , X.L. Li7 , J. Lien131 , R. Lietava113 , B. Lim17 ,
S.H. Lim17 , V. Lindenstruth40 , A. Lindner49 , C. Lippmann109 , A. Liu19 , J. Liu129 , I.M. Lofnes21 ,
V. Loginov95 , C. Loizides98 , P. Loncar36 , J.A. Lopez106 , X. Lopez136 , E. López Torres8 , J.R. Luhder145 ,
M. Lunardon28 , G. Luparello61 , Y.G. Ma41 , A. Maevskaya64 , M. Mager35 , S.M. Mahmood20 ,
T. Mahmoud44 , A. Maire138 , R.D. MajkaI,147 , M. Malaev100 , Q.W. Malik20 , L. MalininaIV,76 ,
D. Mal’Kevich94 , N. Mallick51 , P. Malzacher109 , G. Mandaglio33,57 , V. Manko90 , F. Manso136 ,
V. Manzari54 , Y. Mao7 , M. Marchisone137 , J. Mareš67 , G.V. Margagliotti24 , A. Margotti55 , A. Marín109 ,
C. Markert121 , M. Marquard69 , N.A. Martin106 , P. Martinengo35 , J.L. Martinez127 , M.I. Martínez46 ,
G. Martínez García117 , S. Masciocchi109 , M. Masera25 , A. Masoni56 , L. Massacrier79 ,
A. Mastroserio140,54 , A.M. Mathis107 , O. Matonoha82 , P.F.T. Matuoka123 , A. Matyja120 , C. Mayer120 ,
F. Mazzaschi25 , M. Mazzilli54 , M.A. Mazzoni59 , A.F. Mechler69 , F. Meddi22 , Y. Melikyan64 ,
A. Menchaca-Rocha72 , C. Mengke7 , E. Meninno116,30 , A.S. Menon127 , M. Meres13 , S. Mhlanga126 ,
Y. Miake135 , L. Micheletti25 , L.C. Migliorin137 , D.L. Mihaylov107 , K. Mikhaylov76,94 ,
A.N. Mishra146,70 , D. Miśkowiec109 , A. Modak4 , N. Mohammadi35 , A.P. Mohanty63 , B. Mohanty88 ,
M. Mohisin Khan16 , Z. Moravcova91 , C. Mordasini107 , D.A. Moreira De Godoy145 , L.A.P. Moreno46 ,
I. Morozov64 , A. Morsch35 , T. Mrnjavac35 , V. Muccifora53 , E. Mudnic36 , D. Mühlheim145 ,
S. Muhuri142 , J.D. Mulligan81 , A. Mulliri23,56 , M.G. Munhoz123 , R.H. Munzer69 , H. Murakami134 ,

## PDF page 24

24

ALICE Collaboration

S. Murray126 , L. Musa35 , J. Musinsky65 , C.J. Myers127 , J.W. Myrcha143 , B. Naik50 , R. Nair87 ,
B.K. Nandi50 , R. Nania55 , E. Nappi54 , M.U. Naru14 , A.F. Nassirpour82 , C. Nattrass132 , R. Nayak50 ,
S. Nazarenko111 , A. Neagu20 , L. Nellen70 , S.V. Nesbo37 , G. Neskovic40 , D. Nesterov115 , B.S. Nielsen91 ,
S. Nikolaev90 , S. Nikulin90 , V. Nikulin100 , F. Noferini55 , S. Noh12 , P. Nomokonov76 , J. Norman129 ,
N. Novitzky135 , P. Nowakowski143 , A. Nyanin90 , J. Nystrand21 , M. Ogino84 , A. Ohlson82 ,
J. Oleniacz143 , A.C. Oliveira Da Silva132 , M.H. Oliver147 , B.S. Onnerstad128 , C. Oppedisano60 , A. Ortiz
Velasquez70 , T. Osako47 , A. Oskarsson82 , J. Otwinowski120 , K. Oyama84 , Y. Pachmayer106 ,
S. Padhan50 , D. Pagano141 , G. Paić70 , J. Pan144 , S. Panebianco139 , P. Pareek142 , J. Park62 ,
J.E. Parkkila128 , S. Parmar102 , S.P. Pathak127 , B. Paul23 , J. Pazzini141 , H. Pei7 , T. Peitzmann63 ,
X. Peng7 , L.G. Pereira71 , H. Pereira Da Costa139 , D. Peresunko90 , G.M. Perez8 , S. Perrin139 , Y. Pestov5 ,
V. Petráček38 , M. Petrovici49 , R.P. Pezzi71 , S. Piano61 , M. Pikna13 , P. Pillot117 , O. Pinazza55,35 ,
L. Pinsky127 , C. Pinto27 , S. Pisano53 , M. Płoskoń81 , M. Planinic101 , F. Pliquett69 , M.G. Poghosyan98 ,
B. Polichtchouk93 , N. Poljak101 , A. Pop49 , S. Porteboeuf-Houssais136 , J. Porter81 , V. Pozdniakov76 ,
S.K. Prasad4 , R. Preghenella55 , F. Prino60 , C.A. Pruneau144 , I. Pshenichnov64 , M. Puccio35 , S. Qiu92 ,
L. Quaglia25 , R.E. Quishpe127 , S. Ragoni113 , J. Rak128 , A. Rakotozafindrabe139 , L. Ramello32 ,
F. Rami138 , S.A.R. Ramirez46 , A.G.T. Ramos34 , R. Raniwala104 , S. Raniwala104 , S.S. Räsänen45 ,
R. Rath51 , I. Ravasenga92 , K.F. Read98,132 , A.R. Redelbach40 , K. RedlichV,87 , A. Rehman21 ,
P. Reichelt69 , F. Reidt35 , R. Renfordt69 , Z. Rescakova39 , K. Reygers106 , A. Riabov100 , V. Riabov100 ,
T. Richert82,91 , M. Richter20 , P. Riedler35 , W. Riegler35 , F. Riggi27 , C. Ristea68 , S.P. Rode51 ,
M. Rodríguez Cahuantzi46 , K. Røed20 , R. Rogalev93 , E. Rogochaya76 , T.S. Rogoschinski69 , D. Rohr35 ,
D. Röhrich21 , P.F. Rojas46 , P.S. Rokita143 , F. Ronchetti53 , A. Rosano33,57 , E.D. Rosas70 , A. Rossi58 ,
A. Rotondi29 , A. Roy51 , P. Roy112 , O.V. Rueda82 , R. Rui24 , B. Rumyantsev76 , A. Rustamov89 ,
E. Ryabinkin90 , Y. Ryabov100 , A. Rybicki120 , H. Rytkonen128 , O.A.M. Saarimaki45 , R. Sadek117 ,
S. Sadovsky93 , J. Saetre21 , K. Šafařík38 , S.K. Saha142 , S. Saha88 , B. Sahoo50 , P. Sahoo50 , R. Sahoo51 ,
S. Sahoo66 , D. Sahu51 , P.K. Sahu66 , J. Saini142 , S. Sakai135 , S. Sambyal103 , V. Samsonov100,95 ,
D. Sarkar144 , N. Sarkar142 , P. Sarma43 , V.M. Sarti107 , M.H.P. Sas147,63 , J. Schambach98,121 ,
H.S. Scheid69 , C. Schiaua49 , R. Schicker106 , A. Schmah106 , C. Schmidt109 , H.R. Schmidt105 ,
M.O. Schmidt106 , M. Schmidt105 , N.V. Schmidt98,69 , A.R. Schmier132 , J. Schukraft35 , Y. Schutz138 ,
K. Schwarz109 , K. Schweda109 , G. Scioli26 , E. Scomparin60 , J.E. Seger15 , Y. Sekiguchi134 ,
D. Sekihata134 , I. Selyuzhenkov109,95 , S. Senyukov138 , J.J. Seo62 , D. Serebryakov64 , L. Šerkšnytė107 ,
A. Sevcenco68 , A. Shabanov64 , A. Shabetai117 , R. Shahoyan35 , W. Shaikh112 , A. Shangaraev93 ,
A. Sharma102 , H. Sharma120 , M. Sharma103 , N. Sharma102 , S. Sharma103 , O. Sheibani127 ,
A.I. Sheikh142 , K. Shigaki47 , M. Shimomura85 , S. Shirinkin94 , Q. Shou41 , Y. Sibiriak90 , S. Siddhanta56 ,
T. Siemiarczuk87 , D. Silvermyr82 , G. Simatovic92 , G. Simonetti35 , B. Singh107 , R. Singh88 , R. Singh103 ,
R. Singh51 , V.K. Singh142 , V. Singhal142 , T. Sinha112 , B. Sitar13 , M. Sitta32 , T.B. Skaali20 ,
M. Slupecki45 , N. Smirnov147 , R.J.M. Snellings63 , C. Soncco114 , J. Song127 , A. Songmoolnak118 ,
F. Soramel28 , S. Sorensen132 , I. Sputowska120 , J. Stachel106 , I. Stan68 , P.J. Steffanic132 ,
S.F. Stiefelmaier106 , D. Stocco117 , M.M. Storetvedt37 , L.D. Stritto30 , C.P. Stylianidis92 ,
A.A.P. Suaide123 , T. Sugitate47 , C. Suire79 , M. Suljic35 , R. Sultanov94 , M. Šumbera97 , V. Sumberia103 ,
S. Sumowidagdo52 , S. Swain66 , A. Szabo13 , I. Szarka13 , U. Tabassam14 , S.F. Taghavi107 ,
G. Taillepied136 , J. Takahashi124 , G.J. Tambave21 , S. Tang136,7 , Z. Tang130 , M. Tarhini117 ,
M.G. Tarzila49 , A. Tauro35 , G. Tejeda Muñoz46 , A. Telesca35 , L. Terlizzi25 , C. Terrevoli127 ,
G. Tersimonov3 , S. Thakur142 , D. Thomas121 , F. Thoresen91 , R. Tieulent137 , A. Tikhonov64 ,
A.R. Timmins127 , M. Tkacik119 , A. Toia69 , N. Topilskaya64 , M. Toppi53 , F. Torales-Acosta19 ,
S.R. Torres38,9 , A. Trifiró33,57 , S. Tripathy70 , T. Tripathy50 , S. Trogolo28 , G. Trombetta34 , L. Tropp39 ,
V. Trubnikov3 , W.H. Trzaska128 , T.P. Trzcinski143 , B.A. Trzeciak38 , A. Tumkin111 , R. Turrisi58 ,
T.S. Tveter20 , K. Ullaland21 , E.N. Umaka127 , A. Uras137 , G.L. Usai23 , M. Vala39 , N. Valle29 ,
S. Vallero60 , N. van der Kolk63 , L.V.R. van Doremalen63 , M. van Leeuwen92 , P. Vande Vyvre35 ,
D. Varga146 , Z. Varga146 , M. Varga-Kofarago146 , A. Vargas46 , M. Vasileiou86 , A. Vasiliev90 , O. Vázquez
Doce107 , V. Vechernin115 , E. Vercellin25 , S. Vergara Limón46 , L. Vermunt63 , R. Vértesi146 ,

## PDF page 25

Centrality determination in heavy ion collisions

25

M. Verweij63 , L. Vickovic36 , Z. Vilakazi133 , O. Villalobos Baillie113 , G. Vino54 , A. Vinogradov90 ,
T. Virgili30 , V. Vislavicius91 , A. Vodopyanov76 , B. Volkel35 , M.A. Völkl105 , K. Voloshin94 ,
S.A. Voloshin144 , G. Volpe34 , B. von Haller35 , I. Vorobyev107 , D. Voscek119 , J. Vrláková39 ,
B. Wagner21 , M. Weber116 , A. Wegrzynek35 , S.C. Wenzel35 , J.P. Wessels145 , J. Wiechula69 , J. Wikne20 ,
G. Wilk87 , J. Wilkinson109 , G.A. Willems145 , E. Willsher113 , B. Windelband106 , M. Winn139 ,
W.E. Witt132 , J.R. Wright121 , Y. Wu130 , R. Xu7 , S. Yalcin78 , Y. Yamaguchi47 , K. Yamakawa47 ,
S. Yang21 , S. Yano47,139 , Z. Yin7 , H. Yokoyama63 , I.-K. Yoo17 , J.H. Yoon62 , S. Yuan21 , A. Yuncu106 ,
V. Yurchenko3 , V. Zaccolo24 , A. Zaman14 , C. Zampolli35 , H.J.C. Zanoli63 , N. Zardoshti35 ,
A. Zarochentsev115 , P. Závada67 , N. Zaviyalov111 , H. Zbroszczyk143 , M. Zhalov100 , S. Zhang41 ,
X. Zhang7 , Y. Zhang130 , V. Zherebchevskii115 , Y. Zhi11 , D. Zhou7 , Y. Zhou91 , J. Zhu7,109 , Y. Zhu7 ,
A. Zichichi26 , G. Zinovjev3 , N. Zurlo141

Affiliation Notes
I Deceased
II Also at: Italian National Agency for New Technologies, Energy and Sustainable Economic

Development (ENEA), Bologna, Italy
III Also at: Dipartimento DET del Politecnico di Torino, Turin, Italy
IV Also at: M.V. Lomonosov Moscow State University, D.V. Skobeltsyn Institute of Nuclear, Physics,
Moscow, Russia
V Also at: Institute of Theoretical Physics, University of Wroclaw, Poland

Collaboration Institutes
1 A.I. Alikhanyan National Science Laboratory (Yerevan Physics Institute) Foundation, Yerevan,

Armenia
2 AGH University of Science and Technology, Cracow, Poland
3 Bogolyubov Institute for Theoretical Physics, National Academy of Sciences of Ukraine, Kiev,
Ukraine
4 Bose Institute, Department of Physics and Centre for Astroparticle Physics and Space Science
(CAPSS), Kolkata, India
5 Budker Institute for Nuclear Physics, Novosibirsk, Russia
6 California Polytechnic State University, San Luis Obispo, California, United States
7 Central China Normal University, Wuhan, China
8 Centro de Aplicaciones Tecnológicas y Desarrollo Nuclear (CEADEN), Havana, Cuba
9 Centro de Investigación y de Estudios Avanzados (CINVESTAV), Mexico City and Mérida, Mexico
10 Chicago State University, Chicago, Illinois, United States
11 China Institute of Atomic Energy, Beijing, China
12 Chungbuk National University, Cheongju, Republic of Korea
13 Comenius University Bratislava, Faculty of Mathematics, Physics and Informatics, Bratislava,
Slovakia
14 COMSATS University Islamabad, Islamabad, Pakistan
15 Creighton University, Omaha, Nebraska, United States
16 Department of Physics, Aligarh Muslim University, Aligarh, India
17 Department of Physics, Pusan National University, Pusan, Republic of Korea
18 Department of Physics, Sejong University, Seoul, Republic of Korea
19 Department of Physics, University of California, Berkeley, California, United States
20 Department of Physics, University of Oslo, Oslo, Norway

## PDF page 26

26

ALICE Collaboration

21 Department of Physics and Technology, University of Bergen, Bergen, Norway
22 Dipartimento di Fisica dell’Università ’La Sapienza’ and Sezione INFN, Rome, Italy
23 Dipartimento di Fisica dell’Università and Sezione INFN, Cagliari, Italy
24 Dipartimento di Fisica dell’Università and Sezione INFN, Trieste, Italy
25 Dipartimento di Fisica dell’Università and Sezione INFN, Turin, Italy
26 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Bologna, Italy
27 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Catania, Italy
28 Dipartimento di Fisica e Astronomia dell’Università and Sezione INFN, Padova, Italy
29 Dipartimento di Fisica e Nucleare e Teorica, Università di Pavia and Sezione INFN, Pavia, Italy
30 Dipartimento di Fisica ‘E.R. Caianiello’ dell’Università and Gruppo Collegato INFN, Salerno, Italy
31 Dipartimento DISAT del Politecnico and Sezione INFN, Turin, Italy
32 Dipartimento di Scienze e Innovazione Tecnologica dell’Università del Piemonte Orientale and INFN

Sezione di Torino, Alessandria, Italy
33 Dipartimento di Scienze MIFT, Università di Messina, Messina, Italy
34 Dipartimento Interateneo di Fisica ‘M. Merlin’ and Sezione INFN, Bari, Italy
35 European Organization for Nuclear Research (CERN), Geneva, Switzerland
36 Faculty of Electrical Engineering, Mechanical Engineering and Naval Architecture, University of
Split, Split, Croatia
37 Faculty of Engineering and Science, Western Norway University of Applied Sciences, Bergen,
Norway
38 Faculty of Nuclear Sciences and Physical Engineering, Czech Technical University in Prague,
Prague, Czech Republic
39 Faculty of Science, P.J. Šafárik University, Košice, Slovakia
40 Frankfurt Institute for Advanced Studies, Johann Wolfgang Goethe-Universität Frankfurt, Frankfurt,
Germany
41 Fudan University, Shanghai, China
42 Gangneung-Wonju National University, Gangneung, Republic of Korea
43 Gauhati University, Department of Physics, Guwahati, India
44 Helmholtz-Institut für Strahlen- und Kernphysik, Rheinische Friedrich-Wilhelms-Universität Bonn,
Bonn, Germany
45 Helsinki Institute of Physics (HIP), Helsinki, Finland
46 High Energy Physics Group, Universidad Autónoma de Puebla, Puebla, Mexico
47 Hiroshima University, Hiroshima, Japan
48 Hochschule Worms, Zentrum für Technologietransfer und Telekommunikation (ZTT), Worms,
Germany
49 Horia Hulubei National Institute of Physics and Nuclear Engineering, Bucharest, Romania
50 Indian Institute of Technology Bombay (IIT), Mumbai, India
51 Indian Institute of Technology Indore, Indore, India
52 Indonesian Institute of Sciences, Jakarta, Indonesia
53 INFN, Laboratori Nazionali di Frascati, Frascati, Italy
54 INFN, Sezione di Bari, Bari, Italy
55 INFN, Sezione di Bologna, Bologna, Italy
56 INFN, Sezione di Cagliari, Cagliari, Italy
57 INFN, Sezione di Catania, Catania, Italy
58 INFN, Sezione di Padova, Padova, Italy
59 INFN, Sezione di Roma, Rome, Italy
60 INFN, Sezione di Torino, Turin, Italy
61 INFN, Sezione di Trieste, Trieste, Italy
62 Inha University, Incheon, Republic of Korea
63 Institute for Gravitational and Subatomic Physics (GRASP), Utrecht University/Nikhef, Utrecht,

## PDF page 27

Centrality determination in heavy ion collisions

27

Netherlands
64 Institute for Nuclear Research, Academy of Sciences, Moscow, Russia
65 Institute of Experimental Physics, Slovak Academy of Sciences, Košice, Slovakia
66 Institute of Physics, Homi Bhabha National Institute, Bhubaneswar, India
67 Institute of Physics of the Czech Academy of Sciences, Prague, Czech Republic
68 Institute of Space Science (ISS), Bucharest, Romania
69 Institut für Kernphysik, Johann Wolfgang Goethe-Universität Frankfurt, Frankfurt, Germany
70 Instituto de Ciencias Nucleares, Universidad Nacional Autónoma de México, Mexico City, Mexico
71 Instituto de Física, Universidade Federal do Rio Grande do Sul (UFRGS), Porto Alegre, Brazil
72 Instituto de Física, Universidad Nacional Autónoma de México, Mexico City, Mexico
73 iThemba LABS, National Research Foundation, Somerset West, South Africa
74 Jeonbuk National University, Jeonju, Republic of Korea
75 Johann-Wolfgang-Goethe Universität Frankfurt Institut für Informatik, Fachbereich Informatik und
Mathematik, Frankfurt, Germany
76 Joint Institute for Nuclear Research (JINR), Dubna, Russia
77 Korea Institute of Science and Technology Information, Daejeon, Republic of Korea
78 KTO Karatay University, Konya, Turkey
79 Laboratoire de Physique des 2 Infinis, Irène Joliot-Curie, Orsay, France
80 Laboratoire de Physique Subatomique et de Cosmologie, Université Grenoble-Alpes, CNRS-IN2P3,
Grenoble, France
81 Lawrence Berkeley National Laboratory, Berkeley, California, United States
82 Lund University Department of Physics, Division of Particle Physics, Lund, Sweden
83 Moscow Institute for Physics and Technology, Moscow, Russia
84 Nagasaki Institute of Applied Science, Nagasaki, Japan
85 Nara Women’s University (NWU), Nara, Japan
86 National and Kapodistrian University of Athens, School of Science, Department of Physics , Athens,
Greece
87 National Centre for Nuclear Research, Warsaw, Poland
88 National Institute of Science Education and Research, Homi Bhabha National Institute, Jatni, India
89 National Nuclear Research Center, Baku, Azerbaijan
90 National Research Centre Kurchatov Institute, Moscow, Russia
91 Niels Bohr Institute, University of Copenhagen, Copenhagen, Denmark
92 Nikhef, National institute for subatomic physics, Amsterdam, Netherlands
93 NRC Kurchatov Institute IHEP, Protvino, Russia
94 NRC «Kurchatov»Institute - ITEP, Moscow, Russia
95 NRNU Moscow Engineering Physics Institute, Moscow, Russia
96 Nuclear Physics Group, STFC Daresbury Laboratory, Daresbury, United Kingdom
97 Nuclear Physics Institute of the Czech Academy of Sciences, Řež u Prahy, Czech Republic
98 Oak Ridge National Laboratory, Oak Ridge, Tennessee, United States
99 Ohio State University, Columbus, Ohio, United States
100 Petersburg Nuclear Physics Institute, Gatchina, Russia
101 Physics department, Faculty of science, University of Zagreb, Zagreb, Croatia
102 Physics Department, Panjab University, Chandigarh, India
103 Physics Department, University of Jammu, Jammu, India
104 Physics Department, University of Rajasthan, Jaipur, India
105 Physikalisches Institut, Eberhard-Karls-Universität Tübingen, Tübingen, Germany
106 Physikalisches Institut, Ruprecht-Karls-Universität Heidelberg, Heidelberg, Germany
107 Physik Department, Technische Universität München, Munich, Germany
108 Politecnico di Bari and Sezione INFN, Bari, Italy
109 Research Division and ExtreMe Matter Institute EMMI, GSI Helmholtzzentrum für

## PDF page 28

28

ALICE Collaboration

Schwerionenforschung GmbH, Darmstadt, Germany
110 Rudjer Bošković Institute, Zagreb, Croatia
111 Russian Federal Nuclear Center (VNIIEF), Sarov, Russia
112 Saha Institute of Nuclear Physics, Homi Bhabha National Institute, Kolkata, India
113 School of Physics and Astronomy, University of Birmingham, Birmingham, United Kingdom
114 Sección Física, Departamento de Ciencias, Pontificia Universidad Católica del Perú, Lima, Peru
115 St. Petersburg State University, St. Petersburg, Russia
116 Stefan Meyer Institut für Subatomare Physik (SMI), Vienna, Austria
117 SUBATECH, IMT Atlantique, Université de Nantes, CNRS-IN2P3, Nantes, France
118 Suranaree University of Technology, Nakhon Ratchasima, Thailand
119 Technical University of Košice, Košice, Slovakia
120 The Henryk Niewodniczanski Institute of Nuclear Physics, Polish Academy of Sciences, Cracow,
Poland
121 The University of Texas at Austin, Austin, Texas, United States
122 Universidad Autónoma de Sinaloa, Culiacán, Mexico
123 Universidade de São Paulo (USP), São Paulo, Brazil
124 Universidade Estadual de Campinas (UNICAMP), Campinas, Brazil
125 Universidade Federal do ABC, Santo Andre, Brazil
126 University of Cape Town, Cape Town, South Africa
127 University of Houston, Houston, Texas, United States
128 University of Jyväskylä, Jyväskylä, Finland
129 University of Liverpool, Liverpool, United Kingdom
130 University of Science and Technology of China, Hefei, China
131 University of South-Eastern Norway, Tonsberg, Norway
132 University of Tennessee, Knoxville, Tennessee, United States
133 University of the Witwatersrand, Johannesburg, South Africa
134 University of Tokyo, Tokyo, Japan
135 University of Tsukuba, Tsukuba, Japan
136 Université Clermont Auvergne, CNRS/IN2P3, LPC, Clermont-Ferrand, France
137 Université de Lyon, CNRS/IN2P3, Institut de Physique des 2 Infinis de Lyon , Lyon, France
138 Université de Strasbourg, CNRS, IPHC UMR 7178, F-67000 Strasbourg, France, Strasbourg, France
139 Université Paris-Saclay Centre d’Etudes de Saclay (CEA), IRFU, Départment de Physique
Nucléaire (DPhN), Saclay, France
140 Università degli Studi di Foggia, Foggia, Italy
141 Università di Brescia and Sezione INFN, Brescia, Italy
142 Variable Energy Cyclotron Centre, Homi Bhabha National Institute, Kolkata, India
143 Warsaw University of Technology, Warsaw, Poland
144 Wayne State University, Detroit, Michigan, United States
145 Westfälische Wilhelms-Universität Münster, Institut für Kernphysik, Münster, Germany
146 Wigner Research Centre for Physics, Budapest, Hungary
147 Yale University, New Haven, Connecticut, United States
148 Yonsei University, Seoul, Republic of Korea
