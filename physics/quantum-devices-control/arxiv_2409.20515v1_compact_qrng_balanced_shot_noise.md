Source: https://arxiv.org/abs/2409.20515v1
PDF sha256: f276a8ecad675b33c7da1c09d3f9ca917c383c117a21ccb44d5de698d5bf90ec
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of arxiv_2409.20515v1_compact_qrng_balanced_shot_noise.pdf

Transcription of `arxiv_2409.20515v1_compact_qrng_balanced_shot_noise.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

A Compact Quantum Random Number Generator Based on Balanced Detection of
Shot Noise
Jaideep Singh ,1 Rodrigo Piera ,1 Yury Kurochkin ,1 and James A. Grieve 1

arXiv:2409.20515v1 [quant-ph] 30 Sep 2024

1

Quantum Research Centre, Technology Innovation Institute, Abu Dhabi, United Arab Emirates

Random Number Generators are critical components of modern cryptosystems. Quantum Random
Number Generators (QRNG) have emerged to provide high-quality randomness for these applications. Here we describe a scheme to extract random numbers using balanced detection of shot noise
from an LED in a commercially available off-the-shelf package. The balanced detection minimizes
classical noise contributions from the optical field, improving the isolation of the quantum noise. We
present a detailed description and analyze the performance of a QRNG that can be easily integrated
into existing systems without the requirement of custom components. The design is optimised for
manufacturability, cost, and size.

I.

INTRODUCTION

Randomness generation is an essential ingredient in many
applications, spanning cryptography [1], gaming [2], network management, fundamental physics experiments [3]
and sampling [4, 5] as a non-exhaustive list. In most of
these applications, random values must be both unpredictable and uniformly distributed: for example in quantum key distribution qubit values must be chosen in a
way that is random from the perspective of a would-be
evesdropper [6]. In post-quantum cryptography, the security strongly depends on the properties of the random
number generator, any correlations in the output pose serious security risks to the protocol [7, 8]. Randomness of
this type can only be obtained by sampling physical processes that are intrinsically unpredictable. Quantum systems have emerged as compelling candidates for this task,
as by utilising quantum random processes it is possible to
access unpredictability which does not depend upon ignorance of the system or lack of information. Devices which
embrace this approach are known as Quantum Random
Number Generators (QRNGs). Popular quantum processes for this task include phase diffusion [9–11], vacuum fluctuations [12–14] and photonic shot noise [15],
with commercial examples later developed [16, 17]. Of
these systems, photonic shot noise (sometimes labelled
“photon-counting”) schemes have emerged as particularly amenable to industrialisation [8, 16], and in this
manuscript, we describe such an effort.
Many QRNGs based on photonic shot noise do not
consider the optical field’s stability. The optical field
usually consists of both shot noise and classical noise
from sources such as thermal sources or power supply
noise, which can introduce correlations into the system
such as switching noise from power supplies or power
supply modulation by an adversary. Typically stability
is assumed from the design, however, it is hard to decouple this noise from the shot noise since they are usually
spectrally the same on the output or require active compensation.
A balanced detection approach is widely used with
lasers to reduce the classical noise in the optical field

and make low noise measurements at the shot noise
limit [18, 19]. This approach however has not been explored for LEDs in the context of QRNGs.
LEDs are widely available light sources and easy to
manufacture. These devices can be integrated and do
not require complex hardware for control. There has
been some research on LED-based QRNGs most significantly from ID quantique and recently on Perovskite
LEDs [20, 21]. The use of spatial beam splitting reduces
the complexity of using discrete components like beamsplitters. Hu et. al. demonstrated a QRNG developed
using a phototransistor optocoupler, which can be used
to drastically minimise the size, cost and complexity of
the device [22]. Optocouplers are widely available offthe-shelf components, this increases the trust for OEM
cryptography device manufacturers since they can procure parts from trusted supply chains to ensure infrastructure security.
In this work, we present a QRNG based on the balanced detection of the optical field of an LED in a linear
optocoupler device, to reduce classical noise in the system
and isolate the shot noise. We demonstrate a Quantumto-Classical noise ratio (QCNR) of greater than 30 dB, in
a device realised using entirely off-the-shelf components
widely available in the electronics supply chain, and without any non-standard manufacturing steps.

II.

THEORY

Shot noise is the statistical fluctuation of photon numbers
in an optical field due to their independent nature. Many
light sources emit photons at random times, so the exact
number of photons produced during a specific interval
cannot be accurately predicted [23]. This effect is widely
known in optical metrology, giving rise to the “shot-noise
limit”, which bounds the precision with which one can
measure optical intensity [24, 25]. Only specially prepared light fields such as amplitude-squeezed light can
overcome this limit [26]. In our scheme, we consider our
light source as trusted. The photon number statistics in
this case for shot noise are described by a Poisson distri-

## PDF page 2

2
The photocurrent produced by the photodiode will
fluctuate because of the underlying fluctuations in the
impinging photon number. Photon number fluctuations
are reflected in photocurrent fluctuations with a fidelity
determined by η. The time-varying photocurrent i(t) can
be broken into a time-independent average current < i >
and time-varying fluctuations ∆i(t)
i(t) =< i > +∆i(t)

FIG. 1: The balanced detection scheme for an LED and
two spatially separated photodiodes, such that the
Intensity of beam IP D1 and IP D2 is the same. The two
photodiodes are electrically connected in a differencing
scheme. This optical circuit is encapsulated within our
linear optocoupler device.
bution. We first describe how our scheme isolates shot
noise, before discussing how shot noise can be detected
and used for our QRNG.
As shown in Figure 1 our light source (an LED) and
photodiodes are placed in a configuration such that the
intensity falling on detectors PD1 and PD2 is approximately the same. The spatial separation divides the intensity of the optical field from the LED equally between
the two photodiodes, with some fraction of photons lost.
PD1 and PD2 are connected in a differencing scheme.
We can consider the light field from the LED to consist
of classical noise attributed to the driving current, and
quantum noise attributed to the discretisation of the light
field (shot noise). Since the classical noise is not related
to photon fluctuations it will be correlated at PD1 and
PD2, and quantum noise by definition will be uncorrelated.
It is apparent that the mean photocurrent generated
by PD1 and PD2 (denoted < i1 > and < i2 >) will
be identical, therefore < i1 > − < i2 >= ϵ, where ϵ is
small compared to the measured values and depends on
the matching of the photodiodes, and the spatial beam
shape of the LED. Classical fluctuations are therefore
suppressed from the output signal. Since the shot noise
component of the two beams is independent, the photocurrent fluctuations in i1 and i2 will be completely uncorrelated and the noise power will add
√ up at the output
(voltages will sum as root square V12 + V22 ...). The
combined shot noise in i1 and i2 must have the same
magnitude as that from a single photodiode detecting
the whole intensity from the LED. Therefore the output
of the balanced photodiode is the same as the shot noise
of the LED detected by a single photodiode [27].
For photodiode of quantum efficiency η and photon
flux Φ, the photocurrent is
P
(1)
ℏω
where e is the charge of an electron, P is the power of
the light beam, and ω is the angular frequency.
i = ηeΦ = ηe

(2)

The average value of ∆i(t) is zero but the average of
square of ∆i, < (∆i(t)2 ) >, will not be zero. If we consider a load resistor RL for the photodiode measuring
shot noise, the time-varying noise power becomes,
Pnoise (t) = (∆i(t))2 RL

(3)

for an optical field with Poisson photon number statistics.
P (n) =

n̄n −n̄
e , n = 0, 1, 2.......
n!

(4)

and
(∆n)2 = n̄

(5)

where ∆n is standard deviation in the number of photons
and n̄ is the mean. The photoelectron statistics would
also be expected to follow a Poisson distribution,
(∆N )2 =< N >

(6)

Since i(t) is proportional to the number of photoelectrons generated per second, the photocurrent variance
will satisfy,
(∆i)2 ∝< i >

(7)

It should be clear from the above relation that the
variance of current fluctuations in the photocurrent is
directly proportional to the average value of the photocurrent [25]. Since we are using a balanced scheme, the
variance of the photon number distribution impinging on
the two photodiodes sums, while the mean is reduced to
zero. Therefore at the output, we will have a distribution such that the variance would increase linearly with
a linear increase in the intensity of the optical field.
III.

EXPERIMENT AND RESULTS

We design a printed circuit board with all necessary components for the QRNG in a 25x50mm form factor as
shown in figure 2. We use this evaluation board as our
experimental setup for this section. The photodiodes
PD1 and PD2 generate a shot noise signal at the output. The bandwidth of the integrated photodiodes in
the linear optocoupler we use is 250 KHz. Shot noise
manifests as a very weak current noise signal and therefore needs high amplification and conversion to voltage
for further processing. We divide the amplification into

## PDF page 3

3
two stages to preserve the bandwidth while providing a
high gain to utilise the ADC properly. We combine a
transimpedance amplifier in the first stage with a very
high transimpedance gain and a voltage amplifier to further amplify the signal to be captured with an ADC. A
fixed offset of Vdd /2 is provided to the noise signal for optimal digitisation. We use the integrated ADC from the
microcontroller RP2040 to capture the signal. RP2040
has a 12-bit successive approximation ADC with a Maximum sampling rate of 500 KSa/s, an Effective Number
of Bits (ENOB) of 8 bits and a SNR of 53 dB [28, 29].
Since the sampling rate of the ADC is much higher than
the bandwidth of the photodiodes we configure the ADC
to run at a sub-nyquist sampling rate (100 KSa/s) to ensure independence of the sampled events (IID criterion).
It is important to recall that sampling at a rate higher or
equal to the bandwidth of the signal will lead to correlation in successive output bits and therefore running the
ADC at a lower sampling rate is required to eliminate
these correlations. The ADC then converts the analog
signal to digital codes that can then be run through an
extractor algorithm. To collect data for this manuscript,
We transfer the raw ADC codes to a computer on which
we implement a Toeplitz extractor. Note that we can run
an instance of Toeplitz extractor on the microcontroller
directly, enabling standalone operation. In this case however, the modest processing power of the RP2040 leads
to low output rate which may nevertheless be considered
sufficient for some applications.
We classify the noise signal at the output of the voltage
amplifier into two categories, quantum noise and classical noise. Quantum noise is defined here as the noise
generated by the optocoupler which corresponds to the
shot noise of the LED. Classical noise is any other noise
contribution, this includes noise such as thermal noise,
detector dark noise, and amplifier noise. For shot noise,
we characterise the output from our setup to confirm two
points:
1. The contribution of shot noise to the output signal
at the voltage amplifier is much more significant
than classical noise from the system. We quantify
this by calculating the Quantum to classical noise
ratio (QCNR), i.e. the ratio of shot noise from
the optocoupler to the overall classical noise in the
system. We also calculate the min-entropy which
is the minimum entropy of the raw signal.
2. The output distribution from the voltage amplifier
is Poissonion, important to prove that the distribution corresponds to the shot noise and that this
noise dominates the output statistics.
In Figure 3, we show the output statistics of the noise
signal captured by the oscilloscope. We capture the
statistics with the LED off(green), this is the overall classical noise in the system. We then turn on the LED of the
optocoupler and capture the statistics(blue), this is the
mixture of quantum and classical noise in the system.

Since the variance of the quantum noise is much more
significant than the classical noise, we can say that the
quantum noise in the output signal dominates. To calculate the QCNR, we use the variance of Classical noise
2
2
(σC
) and quantum noise(σQ
) and use the equation,
QCN R = 20log(

2
2
σQ,C
− σC
)
2
σC

(8)

2
where σQ,C
is the variance of the output noise signal
2
with the LED ON given in blue in Figure 3 and σC
is
the variance of the output noise signal with the LED
OFF given in green. The QCNR for our device is 32 dB.
Quantum noise in the system dominates the overall signal
at the output.
It is also important to calculate the min-entropy of
the output sequence. The min-entropy is the minimum
information-theoretic random bits in a sequence. The
minimum entropy is used to define the extraction ratio
which bounds the maximum output bits from the extractor. We use a Toeplitz extractor to extract information
theoretic random numbers from the output digital codes.
To calculate the min-entropy from the output statistics,
we use the equation,

H∞ (X) = −log2 ( max n Pr [X = x])

(9)

x∈{0,1}

It quantifies the amount of randomness of a distribution X on {0, 1}n [30–32]. The entropy of given sequence
X is determined by sample point x with maximal probability. We calculate the extraction ratio of our device to
be 7 bits for the 12-bit ADC on RP2040. Putting a sufficient clearance to this limit, we use a Toeplitz extractor
to extract 5 bits per sample.
In Figure 4, we vary the forward current of the LED
and measure the variance of the output signal. Changing the forward current of the LED linearly increases the
intensity of the optical field, since photodiodes are linear, this manifests as a linear change in the mean of the
output signal. Since we are using a balanced scheme
this mean is cancelled out electrically and we only have
access to the noise signal. For a Poisson distribution,
the variance of the output noise signal should vary linearly with the mean and therefore the forward current.
We have an onboard DAC-controlled current source that
can be controlled using the microcontroller. By linearly
stepping the DAC value, we linearly increase the forward
current. We can see in Figure 4 that the variance value
is increasing with a linear trend for three separately acquired datasets. This trend would be quadratic for super
Poissonian distribution if the classical noise in the system
dominates.
The data presented in Figure 3 is used to determine the
minimum entropy in the output sequence, and the overall QCNR. Datasets such as those plotted in Figure 4 are
further used to confirm that the distribution is in agreement with a Poissonian model. We collect 1.2 Gb of random bits and divide it into four batches of 300 Mb each

## PDF page 4

4

FIG. 2: Experimental setup, showing the photodiode connection, the amplification scheme and the ADC and
extractor for conditioning of the raw entropy stream (block diagram). We also show a photograph of our device,
with call-outs for the primary blocks. This device was used to produce all random data analysed in this manuscript.

FIG. 3: Histogram of the QRNG observed with an
oscilloscope with the current source for the LED
off(Green) and with the current source providing 70mA
of forward current to the LED(Blue). We observe that
the variance of the noise when the LED is on is
significantly larger than with the LED off.

at an acquisition rate of 181 Kb/sec of raw entropy and
then run a Toeplitz extractor on the captured data on the
computer. We note that the rate of the QRNG is limited
by the choice of ADC and microcontroller. The theoretical limit for random number generation can be calculated
for this design as 1.2 Mb/s, sampling at 250 KSa/s.
Testing randomness is known to be non-trivial, and
most tests rely on running some variation of statistical
analysis on the output of the random generator. Passing
these testing suites is necessary but insufficient to evaluate the quality of your randomness. To test the statistical randomness of the generated output we run our extracted data through the “dieharder” test suite [33] and
autocorrelation tests. The result of the dieharder test is

FIG. 4: Variance of the output noise signal for different
values of forward current to the LED. We evaluate
three cycles, varying the value of the DAC-controlled
current source from 0 to 2000 to check that the Poisson
characteristic does not change. The data supports a
linear fit (trend line), from which we confirm the
variance change is linear with the change of the mean
value of the optical field.

visualised in the KS test shown in Figure 5 [34, 35]. In
this analysis, we compare the Cumulative Density Function (CDF) of the p-values from our test to the CDF of
an ideal distribution of p-values for statistically random
data. We show that the trend for each run of the 300 Mb
file is linear, as expected for a truly uniform output. We
then compute the autocorrelation of 5 Mbit of extracted
data. This is calculated by performing a cross-correlation
of a sequence with itself, lagged bitwise. If x and y are

## PDF page 5

5
sequence with itself. Correlations within data chunks
would lead to points lying outside the three-sigma bound
for the correlation coefficients. As we increase the size
of the data to run the correlation test the value of the
correlation coefficients would also decrease.

IV.

FIG. 5: KS plot of the p-values from the output of a
dieharder test run on 900 Mbit data, divided into three
chunks and tested individually for statistical
randomness. The output of the KS test should be a
uniform distribution of p-values for truly random bit,
shown by the dotted line labelled ideal p-values.

FIG. 6: Autocorrelation function run with bitwise lag
for a sequence of 5 Mbits. The peak at 5 Mbits shows
the autocorrelation of the sequence with itself at zero
lag.

1-D arrays, the equation used for the cross-correlation is,
||x||−1

Z[k] = (x ∗ y)(k − N + 1) =

∑

xl yl−k+N −1

(10)

l=0

for k = 0, 1......., ||x||+||y||−2, where ||x|| is the length
of x, N = max(||x||, ||y||), and ym is 0 when m is outside
the range of y [36]. The result is plotted in Figure 6.
Any correlation in the sequence would show as peaks
in Figure 6. We observe only one peak corresponding
to zero lag, or alternatively the cross-correlation of the

CONCLUSIONS

We describe a scheme to generate quantum random numbers from shot noise using balanced photodetection in
commercial off-the-shelf available components. We describe a ”white-box” implementation of the QRNG, a
practical alternative to the device-independent QRNG
approach, where instead of extracting random numbers
from a black-box implementation of a trusted QRNG
manufacturer or very complicated device-independent
QRNG, the OEM manufacturer can include a reference QRNG design into their equipment with commercially available components. Following this logic, the
scheme has been optimised for low cost, small footprint (25x50mm), and ease of manufacture. We develop a
prototype QRNG device and describe experiments that
can be used to validate its operation. We further implement several methods to characterise the noise of the
system, without relying on direct access to the optical
field. We calculate the QCNR to be above 30 dB. The
raw entropy rate is 181 Kb/s. The rate of the QRNG
is sufficient for post-quantum cryptography implementation on personal devices such as laptops.
Adopting a higher bandwidth optocoupler, a faster
ADC and microcontroller we expect to increase the output rate further. By way of illustrative example, for a
1 MHz bandwidth linear optocoupler, a 750 KSa/s ADC
and a 7-bit extraction ratio, we would expect to achieve
5.25 Mbit/s of entropy. All of these components are easily available from different manufacturers within the commercial off-the-shelf electronics supply chain. We believe
that QRNG devices of the kind described here will be an
attractive option for integration into many electronicsbased platforms that currently lack a robust and reliable
entropy source.

## PDF page 6

6

[1] R. Gennaro, “Randomness in cryptography,” IEEE
Security & Privacy, vol. 4, no. 2, pp. 64–67, 2006.
[2] S. Mishra and A. Pathak, “Quantum and semiquantum lottery: strategies and advantages,” Quantum
Information Processing, vol. 22, p. 290, July 2023.
[3] X. Yuan, Z. Cao, and X. Ma, “Randomness requirement on the clauser-horne-shimony-holt bell test in the
multiple-run scenario,” Phys. Rev. A, vol. 91, p. 032111,
Mar 2015.
[4] N. Metropolis and S. Ulam, “The monte carlo method,”
Journal of the American Statistical Association, vol. 44,
no. 247, pp. 335–341, 1949. PMID: 18139350.
[5] R. M. Karp, “An introduction to randomized algorithms,” Discrete Applied Mathematics, vol. 34, no. 1,
pp. 165–201, 1991.
[6] V. Martin, J. Brito, C. Escribano, M. Menchetti,
C. White, A. Lord, F. Wissel, M. Gunkel, P. Gavignet, N. Genay, and et al., “Quantum technologies
in the telecommunications industry,” EPJ Quantum
Technology, vol. 8, no. 1, 2021.
[7] M. Stipčević, “Quantum random number generators and
their use in cryptography,” in 2011 Proceedings of the
34th International Convention MIPRO, pp. 1474–1479,
2011.
[8] M. Herrero-Collantes and J. C. Garcia-Escartin, “Quantum random number generators,” Reviews of Modern
Physics, vol. 89, Feb. 2017.
[9] M. W. Mitchell, C. Abellan, and W. Amaya, “Strong
experimental guarantees in ultrafast quantum random
number generation,” Phys. Rev. A, vol. 91, p. 012314,
Jan 2015.
[10] R. Shakhovoy, D. Sych, V. Sharoglazova, A. Udaltsov,
A. Fedorov, and Y. Kurochkin, “Quantum noise extraction from the interference of laser pulses in an optical quantum random number generator,” Opt. Express,
vol. 28, pp. 6209–6224, Mar 2020.
[11] F. Xu, B. Qi, X. Ma, H. Xu, H. Zheng, and H.-K. Lo,
“Ultrafast quantum random number generation based on
quantum phase fluctuations,” Optics Express, vol. 20,
no. 11, p. 12366, 2012.
[12] Y. Shi, B. Chng, and C. Kurtsiefer, “Random numbers from vacuum fluctuations,” Applied Physics Letters,
vol. 109, p. 041101, 07 2016.
[13] C. Bruynsteen, T. Gehring, C. Lupo, J. Bauwelinck,
and X. Yin, “100-gbit/s integrated quantum random
number generator based on vacuum fluctuations,” PRX
Quantum, vol. 4, p. 010330, Mar 2023.
[14] C. Bruynsteen, T. Gehring, C. Lupo, J. Bauwelinck,
and X. Yin, “100-gbit/s integrated quantum random
number generator based on vacuum fluctuations,” PRX
Quantum, vol. 4, no. 1, 2023.
[15] B. Sanguinetti, A. Martin, H. Zbinden, and N. Gisin,
“Quantum random number generation on a mobile
phone,” Phys. Rev. X, vol. 4, p. 031056, Sep 2014.
[16] ID Quantique SA, “Only quantum random number
generators are intrinsically random and provably
unpredictable,” Jun 2022.
Available at https:
//www.idquantique.com/random-number-generation/
products/.
[17] Quside Technologies,
“QRNG Security Chipset
QN100
Chip.”
https://quside.com/product/

quside-qn100-chipsets/, Feb 2024.
[18] G. Abbas, V. Chan, and T. Yee, “A dual-detector optical heterodyne receiver for local oscillator noise suppression,” Journal of Lightwave Technology, vol. 3, no. 5,
pp. 1110–1122, 1985.
[19] Z. Li, H. Chen, H. Pan, A. Beling, and J. C. Campbell,
“High-power integrated balanced photodetector,” IEEE
Photonics Technology Letters, vol. 21, no. 24, pp. 1858–
1860, 2009.
[20] G. Gras, A. Martin, J. W. Choi, and F. Bussières, “Quantum entropy model of an integrated quantum-randomnumber-generator chip,” Physical Review Applied,
vol. 15, no. 5, 2021.
[21] J. Argillander, A. Alarcón, C. Bao, C. Kuang, G. Lima,
F. Gao, and G. B. Xavier, “Quantum random number
generation based on a perovskite light emitting diode,”
Communications Physics, vol. 6, no. 1, 2023.
[22] Y.-Y. Hu, Y.-Y. Ding, S. Wang, Z.-Q. Yin, W. Chen,
D.-Y. He, W. Huang, B.-J. Xu, G.-C. Guo, and Z.-F.
Han, “Compact quantum random number generation using a linear optocoupler,” Optics Letters, vol. 46, no. 13,
p. 3175, 2021.
[23] G. Brida, M. Genovese, and I. Ruo Berchera, “Experimental realization of sub-shot-noise quantum imaging,”
Nature Photonics, vol. 4, p. 227–230, Feb. 2010.
[24] G. Brida, M. Genovese, and I. Ruo Berchera, “Experimental realization of sub-shot-noise quantum imaging,”
Nature Photonics, vol. 4, pp. 227–230, Apr. 2010.
[25] M. Fox, Shot noise in Photodiodes, p. 94–99. Oxford
University Press, 2013.
[26] D. F. Walls, “Squeezed states of light,” Nature, vol. 306,
pp. 141–146, Nov. 1983.
[27] M. Fox, Detection of squeezed light, p. 139–142. Oxford
University Press, 2006.
[28] M. Omo, “Introduction,” Feb 2021. Available at https:
//pico-adc.markomo.me/.
[29] Raspberry Pi, “RP2040 Datasheet A microcontroller
by Raspberry Pi.” Available at https://datasheets.
raspberrypi.com/rp2040/rp2040-datasheet.pdf.
[30] J. Y. Haw, S. M. Assad, A. M. Lance, N. H. Y. Ng,
V. Sharma, P. K. Lam, and T. Symul, “Maximization of
extractable randomness in a quantum random-number
generator,” Phys. Rev. Appl., vol. 3, p. 054004, May
2015.
[31] R. Konig, R. Renner, and C. Schaffner, “The operational
meaning of min- and max-entropy,” IEEE Transactions
on Information Theory, vol. 55, no. 9, pp. 4337–4347,
2009.
[32] Y. Dodis, R. Ostrovsky, L. Reyzin, and A. Smith, “Fuzzy
extractors: How to generate strong keys from biometrics and other noisy data,” SIAM Journal on Computing,
vol. 38, no. 1, pp. 97–139, 2008.
[33] R. G. Brown, “Dieharder: A random number test
suite.” Available at https://webhome.phy.duke.edu/
~rgb/General/dieharder.php.
[34] F. J. M. Jr., “The kolmogorov-smirnov test for goodness
of fit,” Journal of the American Statistical Association,
vol. 46, no. 253, pp. 68–78, 1951.
[35] r. Jochen Voss, “dieharder.” Available at https://
github.com/seehuhn/dieharder.
[36] P. Virtanen, R. Gommers, T. E. Oliphant, M. Haber-

## PDF page 7

7
land, T. Reddy, D. Cournapeau, E. Burovski, P. Peterson, W. Weckesser, J. Bright, S. J. van der Walt,
M. Brett, J. Wilson, K. J. Millman, N. Mayorov, A. R. J.
Nelson, E. Jones, R. Kern, E. Larson, C. J. Carey, İ. Polat, Y. Feng, E. W. Moore, J. VanderPlas, D. Laxalde,

J. Perktold, R. Cimrman, I. Henriksen, E. A. Quintero,
C. R. Harris, A. M. Archibald, A. H. Ribeiro, F. Pedregosa, P. van Mulbregt, and SciPy 1.0 Contributors,
“SciPy 1.0: Fundamental Algorithms for Scientific Computing in Python,” Nature Methods, vol. 17, pp. 261–272,
2020.
