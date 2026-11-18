Source: https://arxiv.org/abs/2507.19577v1
PDF sha256: 0b281180b96020d4a09ed666c00995b0e256558c2559a0935b5b71c2b299e8dc
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of thoss_2025_dark_objects_gw.pdf

Transcription of `thoss_2025_dark_objects_gw.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Detecting dark objects in the Solar System with Gravitational Wave observatories
Valentin Thoss∗
Universitäts-Sternwarte
Ludwig-Maximilians-Universität München
Scheinerstr. 1
81679 Munich, Germany
Max-Planck-Institut für Extraterrestrische Physik
Gießenbachstraße 1
85748 Garching, Germany and
Excellence Cluster ORIGINS
Boltzmannstraße 2
85748 Garching, Germany

arXiv:2507.19577v1 [gr-qc] 25 Jul 2025

Abraham Loeb
Astronomy Department
Harvard University
60 Garden St.
Cambridge, MA 02138, USA
(Dated: July 29, 2025)
Dark objects streaming into the solar system can be probed using gravitational wave (GW)
experiments through the perturbations that they would induce on the detector test masses. In this
work, we study the detectability of the resulting gravitational signal for a number of current and
future GW observatories. Dark matter in the form of clumps or primordial black holes with masses
in the range 107 -1011 g can be detected with the proposed DECIGO experiment.

INTRODUCTION

Gravitational wave (GW) observatories such as LIGOVirgo-KAGRA have opened a new window on the universe by their ability to detect minuscule deformations
of spacetime caused by the inspiral and merger of black
holes binaries and neutron stars [1–3]. They do so by
interfering light beams sent between the detector test
masses.
During their operation, GW experiments are subject
to a number of different noise sources, some of which
lead to movement of the test masses between which the
deformations of spacetime are measured. Such perturbations, if they are unpredictable, generally pose a limit to
the sensitivity of an experiment [4].
However, the movement of the detector test masses can
also lead to a detectable signature. In this work we are
interested in gravitational perturbations induced on the
test masses by fast transients of objects passing through
the solar system. These objects could be primordial black
holes (PBHs), making up the entire dark matter [5, 6].
However, the results from this work generally apply to
any object flying through the solar system unbound, with
velocities beyond the escape speed.
Similar analyses have been performed in the past for
the case of dark matter clumps [7–11]. However, these
studies either focused on a single detector such as LISA,
included forces beyond a pure gravitational interaction,
or did not take into account the full noise profile of
the experiments. Our contribution is twofold. On the
one hand, we provide a general way to estimate the de-

tectability of an object passing through the solar system
with any velocity, mass or distance. On the other hand,
focusing on the case of dark matter clumps, we provide
a general overview on the detectability for a number of
current and planned GW detectors. We will also pay
special attention to PBHs with a mass M < 1015 g which
have previously been ignored due to their presumed rapid
evaporation. However, recently this view has been challenged by the so-called ’memory burden’ effect [12–18]
and it is therefore worthwhile to study the scenario of
such light PBHs as well.
[19] studied the detectability of dark matter with proposed atom gradiometers. Their detectable mass window (M ∈ [106 , 1010 ] g) is similar to what we find for
the planned BBO/DECIGO experiments and their results are thus complimentary to our work. We also want
to emphasize that there have been numerous other works
on the role that dark matter clumps or primordial black
holes could have in the solar system [20–26].
Our paper is structured as follows. We first describe
how we compute the signal of the fly-by for any gravitational wave detector. In the following we investigate
detection prospects in terms of the detection volume of
each experiment as well as the interstellar mass density
that they are sensitive to.

COMPUTATION OF THE SIGNAL

An object with mass M that traverses through the
solar system with speed v will exert a gravitational force

## PDF page 2

2
on the test mass of a GW detector, leading to a timedependent acceleration
a(t) = √

GM R
R 2 + v 2 t2

3 ,

(1)

in the direction towards the point of closest encounter at
a distance of R. The spectral density of such a signal can
be computed analytically to be
a(ω) =

2GM ω
K1 (ωR/v) ,
v2

(2)

where K1 denotes the first-order modified Bessel function
of the second kind. Note that K1 (x) ≈ 1/x for x ≪ 1
and thus a(ω) = 2GM
vR for ω ≪ v/R.
For a detector with multiple test masses i, located at
positions ri , the different masses will be perturbed at
a slightly different time ti and distance of closest encounter Ri . The spectral density of the relative acceleration δaij (ω) between a pair of test masses i and j can
be computed by projection on the vector between the two
test masses ri − rj :
(
) (ri − rj )
.
δaij (ω) = ai (ω)âi − aj (ω)âj eiω∆t ·
L

(3)

Here ∆t = ti − tj is the difference between the time of
closest encounter for each detector test mass and L =
|ri − rj | is the arm length of the detector. By âi , we
denote the normalized vector pointing from the position
of the test mass to the point of closest encounter.
To gain a better understanding of Equation 3, we consider a single detector arm with two test masses. The
largest perturbation will be achieved if the compact object moves perpendicular to the axis of the detector arm,
as sketched in Figure 1. In this case ∆t = 0 and Equation 3 reduces to:
δa =

2GM ω
(K1 (ωR/v) − K1 (ω(R + L)/v))
v2

(4)

If the compact object passes within close proximity of
the test mass (R ≪ L, near-field limit), then that mass
will be perturbed much stronger than the other one and
we get to good approximation
δanear =

2GM ω
K1 (ωR/v)
v2

(5)

for the geometry depicted in Figure 1. If the distance
between the compact object and the test masses is much
larger than the detector size (R ≫ L), we only get a tidal
effect, where the perturbation is suppressed by the factor
L/R:
δatid ≈

2GM ωL
K1 (ωR/v)
Rv 2

(6)

In general, any other geometry of the encounter will
produce a smaller perturbation δa. However, a gravitational wave detector usually has more than two test

FIG. 1. Visualization of a fly-by at an impact parameter R
near a GW detector of arm length L

masses. For an L-shaped detector like LIGO with 3
test masses, the measured quantity is actually δa12 (ω) −
δa13 (ω). Here, the index 1 indicates the corner test mass
where the signals from the two arms interfere. Therefore,
the measured perturbation can in principle be larger by
up to a factor of two compared to Equation 4. It is useful
to evaluate the probability distribution p(δa(ω)) due to
the space of possible geometries of the encounter. Using
Monte-Carlo simulations we sample this distribution for
a LIGO-like ’L’-shaped detector, as well as for a triangular setup as is planned for LISA, BBO and DECIGO.
We find that the following expression gives an excellent
fit to the mean perturbation strength both for R ≪ L
and R ≫ L:
⟨δa(ω)⟩ =

2GM ωL
v 2 (αR + βL)

K1 (ωR/v)

(7)

For an L-shaped detector we obtain α = 1.3 and β = 1.76
and for a triangular shape we get α = 1.5 and β = 2.0.
The maximum deviation of the fit from the simulated
data is observed for R = L/2, when the expression above
underestimates the mean perturbation strength by a factor of ∼ 1.6. In the following, we will make use of this
expression to obtain estimates of the signal-to-noise ratio
(SNR) for existing and planned GW observatories.
To compute the spectral density of the gravitational
wave strain h(ω), we recall that h = 2δx/L. From this
and δx(ω) = δa(ω)/ω 2 we get the strain
h(ω) =

4GM
K1 (ωR/v) ,
ωv 2 (αR + βL)

(8)

which can be used to estimate the SNR for any GW experiment, as
(∫
SNR = 2

h(f )2
df
Pn (f )

)1/2
,

(9)

where Pn (ω) denotes the power spectral density of the
detector noise for the respective observatory. Note that
for the case of gravitational waves, Pn (f ) is replaced by
the spectral strain sensitivity Sn (f ). The latter usually accounts for the angular dependence of the response

## PDF page 3

3

10 -16

Pn (f)f 3 [Hz]

10 -18
10 -20

10 -3

10 -1

10 1

10 3

aLIGO
CE
ET
LISA
BBO
DECIGO

10 -14
10 -16
10 -18
10 -20

10 -22

10 -22

10 -24

10 -24

10 -26

10 -26

10 -28 -5
10

10 -3

10 -1
10 1
f [Hz]

10 3

GM
π 2 vR(αR + βL)

10 -5
10 -14

√

of the detector. In addition, it includes a frequencydependent suppression for gravitational waves with wavelengths which are comparable or smaller than the arm
length of the detector [27]. In our case this suppression is
not applicable and the angular dependence is accounted
for in the signal by the factors α and β. Therefore, we
can directly use the detector noise Pn (f ) to estimate the
SNR.
The data for our study is taken from [28] for the detectors aLIGO (design sensitivity), Einstein Telescope
(ET), LISA, Big Bang Observer (BBO) and the Decihertz Interferometer Gravitational wave Observatory
(DECIGO). For Cosmic Explorer (CE) we use the updated model for the detector noise from [29]. For the
LISA experiment we include the binary confusion noise
presented in [30] for our analysis. This stochastic background will also be relevant for the BBO/DECIGO experiments but the precise noise spectrum has not been
worked out yet and will depend on the exact detector
geometry and the ability to subtract individual sources
from the background. Therefore, as a conservative choice
we set the lower frequency limit of both detectors to
f = 3×10−3 Hz where we can expect the noise level to be
subdominant (see the dotted gray line in Figure 2). We
found that if we instead extrapolate the detector noise
to lower frequencies, including the binary noise as computed for LISA, then our results do not change much.
Only if BBO achieves lower detector noise than LISA at
frequencies f ≪ 10−3 do the detection prospects improve
notably.
In addition to the noise from the galactic binaries,
there are a plethora of other possible sources for GW
backgrounds [31, 32], from binary black holes to phase
transitions. The existence of a GW background can in
principle limit the detectability of the perturbations induced by dark objects flying through the solar system.
However, there are often large uncertainties in the estimates for the noise level of the GW backgrounds. Therefore, in our analysis we will assume that detectability is
limited only by the detector noise. The only exception
to this is the mentioned galactic foreground that is accounted for in the LISA noise curve.
The integrand in Equation 9 has the form
df /Pn (f )/f 4 = d log f /Pn (f )/f 3 for f ≪ v/R and
decreases sharply
√ for f ≫ v/R. It 2is therefore convePn (f )f 3 and h(f )f together, as the
nient to plot
latter will be constant for f ≪ v/R and the area of the
ratio between both curves will be proportional to the
SNR on a log-scaled figure.
Figure 2 shows the rescaled spectral noise of current,
planned and proposed GW observatories. This plot can
be used to easily read off the signal-to-noise ratio for
any of the experiments displayed by the area between
the signal, based on the right-side y-axis and the noise
curve. The axis have been rescaled such that the signal
will be represented by a horizontal line with an amplitude

10 -28

FIG. 2. Strain sensitivity of various existing and proposed
GW experiments. The y-axis has been rescaled such that
the signal of an encounter with given parameters M , R and
v would appear as a horizontal line for f < v/R, dropping
quickly for f > v/R. The area between it and any sensitivity
curve is proportional to the signal-to-noise ratio for that experiment. Note that in the limit of a close encounter, R < L,
the signal amplitude is dependent on the detector arm length
and must be computed for each experiment separately. The
dashed lines shows the signal for an object with M = 1010 g,
v = 300 km s−1 and R = 103 km for the detectors LISA, BBO
and DECIGO in the same colors as the strain sensitivity. The
dotted black line indicates the binary confusion noise, taken
from [30].

GM
that extends up to a frequency f = v/R
of π2 vR(αR+βL)
and drops sharply thereafter. Note that in the the limit
R ≪ L the amplitude is dependent on the arm length of
each detector and thus the signal must be computed for
each experiment individually.

As a first step, we remain agnostic about the orbital
parameters of the perturber and compute for a range of
values of M and velocity v the distance of the encounter
R to which each experiment is sensitive. We will present
the results of this in the following section.
As a second step, we study the feasibility of detecting
objects with a given interstellar mass density ρ at the
location of the solar system. If primordial black holes of
a given mass M make up all of the dark matter, they
will have ρ ∼ ρDM = 7 × 10−25 g cm−3 ≈ 0.4 GeV cm−3
and an rms velocity of v ∼ 300 km s−1 [33, 34]. While
our results apply to PBHs, they can also be used more
generally as a way to constrain any kind of interstellar
objects flying through the solar system.
Fixing the density of the perturbers implies a number
of encounters with impact parameters smaller than R

## PDF page 4

4
within a time t, given by
N=

πR2 ρvt
.
M

(10)

Therefore, the probability distribution of the distance R
to the closest encounter by Poisson statistics is
(
)
2πRρvt
πR2 ρvt
dN
=
exp −
, (11)
p(R) = p(N )
dR
M
M
which implies that the mean distance of the closest encounter to occur within a timespan t is given by
√
M
⟨Rmin ⟩ =
.
(12)
4ρvt
Using this as an estimate for the value of R, we employ
Equations 8 and 9 to evaluate the SNR for a given interstellar density ρ, mass M and velocity v of the perturbers.
Previous studies of ’burst’-like GW signals have found
SNRs of around 8 sufficient for the LIGO observatory
[35, 36]. For a lower SNR, the false alarm rate (FAR) will
be too large. Using Equation 30 from [36], we compute
the FAR for any other GW detector using the spectral
density h(ω) of the signal:
√
C2 − C21 −ξ2 /2
ξe
.
(13)
FAR =
2π
Here, ξ denotes the signal-to-noise ratio according to
Equation 9 and the Ck are defined as
∫
4
h(f )2
Ck = 2
df (2πf )k
.
(14)
ξ
Pn (f )
As the detectors considered in this work are generally
most sensitive at lower frequencies compared to LIGO,
the resulting false alarm rates are generally lower and so
is the required SNR.

DETECTION PROSPECTS

Figure 3 displays the minimum fly-by distance required
to have a signal with FAR < 10−3 yr−1 , which corresponds to SNRs between 5 and 8 for the experiments
considered. We display the detection volume as a function of the perturber mass and velocity for LISA and
DECIGO and additionally show the results for all detectors for v = 300 km s−1 .
A limitation for each GW detector is the minimum frequency fmin that it is sensitive to, as it sets the maximum
distance observable to Rmax ∼ v/fmin . For this reason,
LISA has the largest detection range for the most massive
objects due to its susceptibility at low frequencies. For
objects of smaller mass or higher velocity, where the limiting factor is the sensitivity of the experiment, DECIGO

achieves a larger detection volume due to its superior design sensitivity compared to LISA.
We note that the large detection radius for LISA in
principle opens the possibility to measure the masses
of asteroids or comets whose trajectory and velocity is
known, should they pass close enough to the detector.
The recently discovered interstellar object 3I/ATLAS
[37–39] has a minimum intersection distance with Earth’s
orbit of 0.37 AU. Assuming a mass of 1016 g, corresponding to a diameter of the nucleus of 1-2 km, the closest
approach to LISA would have to be at a distance below
0.002 AU in order to be detectable. However, there are
assumed to be many more smaller bodies, some of which
could come close enough to a GW observatory for a detection. Computing the likelihood for such an event is
left for future work.
Figure 4 shows the SNR resulting from a fixed density
of the dark objects of ρ ∼ ρDM = 7 × 10−25 g cm−3 ≈
0.4 GeV cm−3 . The distance to the perturber is set by
Equation 12. The future detectors BBO and DECIGO
show the most promising results, achieving large SNRs
for a sizable part of the parameter space, even at nonrelativistic velocities. LISA, CE and ET reach SNRs
close to or slightly above one at relativistic velocities.
However, such parameter regions are likely ruled out by
other constraints, either from structure formation in the
case of dark matter or from collisions with solar system
bodies in general.
Focusing on the case of compact objects such as PBHs
as dark matter, we adopt a velocity of v = 300 km s−1
and compute the lowest density ρ for which the closest encounter within a period of T = 10 yr produces a
signal with a false alarm rate below 10−3 yr−1 . The results are displayed in Figure 5. The curves can be easily
adopted for different periods of observation T by noting
that ρ ∼ 1/T . Our results demonstrate that the planned
BBO and DECIGO experiments will be able to probe scenarios where the dark matter is in the form of compact
objects with a mass of M ∈ [107 , 1011 ] g. It is commonly
assumed that PBHs of such masses cannot make up the
dark matter due to their rapid evaporation. However,
the so-called ’memory burden’ effect [12, 13] could significantly suppress the evaporation, opening a new window
for light PBHs as a dark matter candidate [14–17]. It is
therefore highly interesting that GW experiments could
be used to probe their existence purely by their gravitational interaction as they pass through the solar system.
By pure coincidence, DECIGO is also able to probe PBHs
of similar mass through the GW emission associated with
their formation [40].
The noise spectrum of future gravitational wave detectors has to be estimated, which implies some degree
of uncertainty. In Figure
√ 5 we show how an uncertainty
in the detector noise Pn (f ) of a factor of two affects
the resulting densities which can be probed. For lower
masses, where the detection is limited by the noise level of

## PDF page 5

5

10 4

v [km s −1 ]

LISA

c
10 4

10 8

10 8

10 6

10 6

10 4
10 2

10 0 5
10

10 2

10 10

10 15
M [g]

10 20

10 0 5
10

R [km]

DECIGO

c

10 2
10 10

10 15
M [g]

10 20

10 0

v = 300 km s −1
aLIGO
CE
ET
LISA

10 4
10 2
10 0 4
10

BBO
DECIGO

10 8

10 12

10 16

10 20

M [g]

FIG. 3. Maximum distance for which GW experiments are sensitive to a fly-by of a perturber. Left: Results for DECIGO/LISA
as a function of the mass and velocity of the perturber. Contours for R = [105 , 106 , 107 ] km are shown as black lines. Right:
Results for all GW experiments as a function of the mass of the perturber for v = 300 km s−1 . Detectability is defined as
FAR < 10−3 yr−1 .

aLIGO

c
10 4

10 4

10 2

10 4
10 1

10 2

10 0 0
10

10 2

10 5

10 10

10 15

10 20

10 0 0
10

10 2

10 5

M [g]

10 10

10 15

10 20

10 0 0
10

10 0
10 5

M [g]

LISA

c

v [km/s]

ET

c

10 15

10 20

M [g]

BBO

c

10 10

DECIGO

c

10 4

10 4

10 4

10 2

10 2

10 2

SNR

v [km/s]

CE

c

10 -1

10 -2

10 0 0
10

10 5

10 10 10 15
M [g]

10 20

10 0 0
10

10 5

10 10 10 15
M [g]

10 20

10 0 0
10

10 5

10 10 10 15
M [g]

10 20

10 -3

FIG. 4. Signal-to-noise ratio from the closest encounter expected within an observation time of ten years and for a density
ρ = ρDM = 7 × 10−25 g cm−3 . The SNR is shown for several GW experiments as a function of the mass M and velocity v of
the perturber. In the white area the SNR is lower than 10−3 . The black lines indicate the contours for which SNR = [1, 10].

√
the observatory one has ρ ∼ Pn (f ) as h(f ) ∼ 1/R ∼ ρ.
At higher masses, where the limit is set by the frequency
range of the detector, the results are not very sensitive
to the exact noise level.

Our results show that DECIGO has the greatest potential to detect perturbations from dark matter in the form
of compact objects streaming through the solar system.
We therefore study this case in more detail and relax pre-

## PDF page 6

6

10 -19

10 -24

10 -22

aLIGO
CE
ET
LISA
BBO
DECIGO

10 -23
10 -24
10 -25
10 -26 2
10

10 5

10 8

10 11
M [g]

10 14

10 17

10 20

FIG. 5. Density to which each experiment is sensitive at a
velocity of v = 300 km s−1 as expected for dark matter. The
results are obtained by requiring FAR < 10−3 yr−1 which implies SNRs between 5 and 8 for the various detectors. The
colored shaded area indicates the resulting
range implied by
√
an uncertainty in the detector noise Pn of a factor of two.
The gray shaded area corresponds to the range of the latest observational estimates of the local dark matter density
ρDM ∈ [0.3, 0.5] GeV cm−3 [33].

vious approximations. For a more accurate assessment of
detection prospects we compute the signal using Equation 3 by performing Monte Carlo simulations over the
space of possible geometries of the encounter. The velocity for each encounter is obtained by adding a random
component with vrms = 270 km s−1 to the proper motion
of of the sun around the galactic center (DM wind) with
v⊙ = 220 km s−1 [34]. We neglect the small non-isotropy
in the angular distribution of the velocity and sample the
orientation uniformly on a sphere. These simulations are
performed for a range of different masses M and densities ρ and the probability of a successful observation in
a period of T = 10 yr is determined as the fraction of
simulations for which FAR < 10−3 yr−1 is obtained.
Figure 6 shows the results. Notably, there is a wide
range of masses M for which the probability of observing
the gravitational signal is high. In other words, should
the dark matter be in the form of compact objects with
mass M ∈ [107 , 1011 ] g, there is a good chance that it
will perturb the DECIGO detector enough to lead to a
detectable signal at least once within 10 years of observation. This agrees well with the estimate presented before
in Figure 5 that is also shown as a white dashed line in
Figure 6. The non-detection of a gravitational signal of
this kind allows in principle to put constraints on the
dark matter density for the same range of masses. However, such bounds might not have a very high confidence,
less than 2 sigma based on our results.
The sensitivity to the perturbations depends on the
exact level of DECIGO’s detector noise. We highlight
this in Figure 6 by an additional dashed line which indi-

ρ [g cm −3 ]

ρ [g cm −3 ]

10 -21

90 %
75 %%
50

10 -20

80
60
40

10 -25

20
10 -26 5
10

10 7

10 9
M [g]

10 11

10 13

Detection probability in %

100

0

FIG. 6. Probability for DECIGO to detect at least one signal from the fly-by of compact objects, shown as a function
of their mass M and density ρ. We assume an observation
time of T = 10 yr. A successful detection is defined as having
FAR < 10−3 yr−1 , which roughly corresponds to SNR > 6.
The orange shaded area corresponds to the range of the latest observational estimates of the local dark matter density
ρDM ∈ [0.3, 0.5] GeV cm−3 [33]. Contours of constant probability are displayed as solid black lines. The dotted black line
indicates a contour of 50% probability given a reduction in
the detector noise level by a factor of two. The estimate from
Figure 5 for the DECIGO experiment is shown as a dashed
white line.

cates the contour for a 50% probability of observation in
a scenario where the detector noise is lower by a factor
of two. Notably, if the ’Ultimate DECIGO’ detector [41]
is realized, which is only limited by quantum noise, then
the detection prospects could increase by several orders
of magnitude. Conversely, the detection prospects can
diminish if detector noise is greater than anticipated or
in the presence of irremovable gravitational wave backgrounds. We find that a factor of 5 increase in the noise
level reduces the probability for an observable to below
50% for any mass of the perturber. Finally, we want to
note that the densities which are observable or that can
be constrained scale with observation time as ρ ∼ 1/T .

SUMMARY

We have studied the feasibility of gravitationally probing the streaming of dark objects through our solar system. The detection method relies on the perturbation
of the test masses of gravitational wave detectors, which
leads to a burst-like signal in the experiment.
We have computed the distances of encounters to
which the different types of current and future GW experiments are sensitive, which can reach several million
kilometers for LISA, BBO, and DECIGO. The main limitation of each experiment is the frequency range to which

## PDF page 7

7
it is sensitive. In order for the encounter to be detectable,
the fly-by must be sufficiently close or fast in order for
f ∼ v/R to be large enough.
If the solar system is penetrated by dark objects with a
halo density ρ ∼ ρDM then future GW experiments such
as BBO and DECIGO offer the best prospects to detect
dark matter in a mass window M ∈ [107 , 1011 ] g. Such a
scenario is highly interesting for the case of PBHs, whose
evaporation is suppressed by the ’memory burden’ effect.

ACKNOWLEDGMENTS

We want to thank Valeriya Korol, Jakob Stegmann and
Andreas Burkert for helpful comments. This research
was supported in part by the Excellence Cluster ORIGINS which is funded by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) under
Germany’s Excellence Strategy - EXC-2094 - 390783311
(for V.T.). This work was supported in part by the Black
Hole Initiative and the Galileo Project at Harvard University (for A.L.).

DATA AVAILABILITY

The numerical results presented in Figure 3 and Figure 5 are publicly accessible under https://doi.org/
10.5281/zenodo.16411495 [42]. Any other data is available upon request.

∗
vthoss@mpe.mpg.de
[1] B. P. Abbott, others (LIGO Scientific, and V. Collaborations), Observation of Gravitational Waves from a Binary
Black Hole Merger, Phys. Rev. Lett. 116, 061102 (2016).
[2] B. P. Abbott, others (LIGO Scientific, and V. Collaborations), GW170817: Observation of Gravitational Waves
from a Binary Neutron Star Inspiral, Phys. Rev. Lett.
119, 161101 (2017).
[3] R. Abbott, others (LIGO Scientific, and V. Collaborations), GWTC-3: Compact Binary Coalescences Observed by LIGO and Virgo during the Second Part of
the Third Observing Run, Physical Review X 13, 041039
(2023).
[4] B. P. Abbott, others (LIGO Scientific, and V. Collaborations), A guide to LIGO-Virgo detector noise and extraction of transient gravitational-wave signals, Classical
and Quantum Gravity 37, 055002 (2020).
[5] B. Carr, K. Kohri, Y. Sendouda, and J. Yokoyama, Constraints on primordial black holes, Reports on Progress
in Physics 84, 116902 (2021).
[6] A. Escrivà, F. Kühnel, and Y. Tada, Primordial black
holes, in Black Holes in the Era of Gravitational-Wave
Astronomy, edited by M. Arca Sedda, E. Bortolas, and
M. Spera (2024) pp. 261–377.

[7] A. W. Adams and J. S. Bloom, Direct Detection of Dark
Matter with Space-based Laser Interferometers, arXiv eprints , astro-ph/0405266 (2004).
[8] N. Seto and A. Cooray, Search for small-mass black-hole
dark matter with space-based gravitational wave detectors, Phys. Rev. D 70, 063512 (2004).
[9] M. Cerdonio, R. De Pietri, P. Jetzer, and M. Sereno, Local dark matter searches with LISA, Classical and Quantum Gravity 26, 094022 (2009).
[10] E. D. Hall, R. X. Adhikari, V. V. Frolov, H. Müller, and
M. Pospelov, Laser interferometers as dark matter detectors, Phys. Rev. D 98, 083019 (2018).
[11] S. Baum, M. A. Fedderke, and P. W. Graham, Searching
for dark clumps with gravitational-wave detectors, Phys.
Rev. D 106, 063015 (2022).
[12] G. Dvali, A Microscopic Model of Holography: Survival by the Burden of Memory, arXiv e-prints ,
arXiv:1810.02336 (2018).
[13] G. Dvali, L. Eisemann, M. Michel, and S. Zell, Black
hole metamorphosis and stabilization by memory burden,
Phys. Rev. D 102, 103523 (2020).
[14] V. Thoss, A. Burkert, and K. Kohri, Breakdown of hawking evaporation opens new mass window for primordial
black holes as dark matter candidate, Mon. Not. R. Astron. Soc. 532, 451 (2024).
[15] A. Alexandre, G. Dvali, and E. Koutsangelas, New mass
window for primordial black holes as dark matter from
the memory burden effect, Phys. Rev. D 110, 036004
(2024).
[16] G. Dvali, M. Zantedeschi, and S. Zell, Transitioning to
Memory Burden: Detectable Small Primordial Black
Holes as Dark Matter, arXiv e-prints , arXiv:2503.21740
(2025).
[17] G. Montefalcone, D. Hooper, K. Freese, C. Kelso, F. Kuhnel, and P. Sandick, Does Memory Burden Open a New
Mass Window for Primordial Black Holes as Dark Matter?, arXiv e-prints , arXiv:2503.21005 (2025).
[18] A. Dondarini, G. Marino, P. Panci, and M. Zantedeschi, The fast, the slow and the merging: probes of
evaporating memory burdened PBHs, arXiv e-prints ,
arXiv:2506.13861 (2025).
[19] L. Badurina, Y. Du, V. S. H. Lee, Y. Wang, and
K. M. Zurek, Detecting gravitational signatures of
dark matter with atom gradiometers, arXiv e-prints ,
arXiv:2505.00781 (2025).
[20] Y. Luo, S. Hanasoge, J. Tromp, and F. Pretorius, Detectable Seismic Consequences of the Interaction of a
Primordial Black Hole with Earth, Astrophys. J. 751,
16 (2012).
[21] T. X. Tran, S. R. Geller, B. V. Lehmann, and D. I. Kaiser,
Close encounters of the primordial kind: A new observable for primordial black holes as dark matter, Phys. Rev.
D 110, 063533 (2024).
[22] A. Yalinewich and M. E. Caplan, Crater morphology of
primordial black hole impacts, Mon. Not. R. Astron. Soc.
505, L115 (2021).
[23] M. E. Caplan, J. Johnston, and A. D. Santarelli, Lunar
collision rate with primordial black holes, Mon. Not. R.
Astron. Soc. 524, 1927 (2023).
[24] M. Cuadrat-Grzybowski, S. Clesse, P. Defraigne, M. Van
Camp, and B. Bertrand, Probing primordial black holes
and dark matter clumps in the Solar System with
gravimeter and Global Navigation Satellite Systems networks, Phys. Rev. D 110, 063029 (2024).

## PDF page 8

8
[25] Y.-L. Li, G.-Q. Huang, Z.-Q. Huang, and F.-W. Shu,
Detecting sublunar-mass primordial black holes with the
Earth-Moon binary system, Phys. Rev. D 107, 084019
(2023).
[26] V. Thoss and A. Burkert, Primordial Black Holes in the
Solar System, Astrophys. J. 980, 238 (2025).
[27] T. Robson, N. J. Cornish, and C. Liu, The construction
and use of LISA sensitivity curves, Classical and Quantum Gravity 36, 105011 (2019).
[28] K. Schmitz, New Sensitivity Curves for GravitationalWave Signals from Cosmological Phase Transitions,
JHEP 01, 097.
[29] K. Kuns, P. Fulda, L. Barsotti, and M. Evans, Cosmic
explorer strain sensitivity, Cosmic Explorer (2023).
[30] N. Cornish and T. Robson, Galactic binary science with
the new LISA design, in Journal of Physics Conference
Series, Journal of Physics Conference Series, Vol. 840
(IOP, 2017) p. 012024, arXiv:1703.09858 [astro-ph.IM].
[31] N. Christensen, Stochastic gravitational wave backgrounds, Reports on Progress in Physics 82, 016903
(2019).
[32] A. I. Renzini, B. Goncharov, A. C. Jenkins, and P. M.
Meyers, Stochastic Gravitational-Wave Backgrounds:
Current Detection Efforts and Future Prospects, Galaxies 10, 34 (2022).
[33] M. Cirelli, A. Strumia, and J. Zupan, Dark Matter, arXiv
e-prints , arXiv:2406.01705 (2024).
[34] K. Choi, C. Rott, and Y. Itow, Impact of the dark matter velocity distribution on capture rates in the Sun, J.
Cosmol. Astropart. Phys. 2014 (5), 049.

[35] G. Morrás, J. Garcı́a-Bellido, and S. Nesseris, Search
for black hole hyperbolic encounters with gravitational
wave detectors, Physics of the Dark Universe 35, 100932
(2022).
[36] G. Morrás, J. F. N. Siles, J. Garcı́a-Bellido, and E. R.
Morales, False alarms induced by Gaussian noise in
gravitational wave detectors, Phys. Rev. D 107, 023027
(2023).
[37] D. Z. Seligman et al., Discovery and Preliminary Characterization of a Third Interstellar Object: 3I/ATLAS,
arXiv e-prints , arXiv:2507.02757 (2025).
[38] A. Loeb, 3I/ATLAS is Smaller or Rarer than It Looks,
Research Notes of the American Astronomical Society 9,
178 (2025).
[39] C/2025 N1 (ATLAS) Orbit Parameters, JPL Small-Body
Database Accessed: 2025-07-25.
[40] W. Barker, B. Gladwyn, and S. Zell, Inflationary and
Gravitational Wave Signatures of Small Primordial Black
Holes as Dark Matter, arXiv e-prints , arXiv:2410.11948
(2024).
[41] N. Seto, S. Kawamura, and T. Nakamura, Possibility of
Direct Measurement of the Acceleration of the Universe
Using 0.1 Hz Band Laser Interferometer Gravitational
Wave Antenna in Space, Phys. Rev. Lett. 87, 221103
(2001).
[42] V. Thoss, Data for the paper ”Detecting dark objects
in the Solar System with Gravitational Wave observatories” (Thoss and Loeb, 2025), 10.5281/zenodo.16411495
(2025).
