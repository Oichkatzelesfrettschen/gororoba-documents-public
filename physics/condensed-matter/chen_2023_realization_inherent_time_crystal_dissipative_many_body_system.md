Source: see manifest row of the PDF
PDF sha256: c0b52f424351c528bb7212636eb24535519cb1610ca34ced969ba5be2a47d403
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of chen_2023_realization_inherent_time_crystal_dissipative_many_body_system.pdf

Transcription of `chen_2023_realization_inherent_time_crystal_dissipative_many_body_system.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

https://doi.org/10.1038/s41467-023-41905-3

Realization of an inherent time crystal in a
dissipative many-body system
Received: 30 October 2022

Yu-Hui Chen1,2 & Xiangdong Zhang

1,2

Accepted: 21 September 2023

1234567890():,;

1234567890():,;

Check for updates

Time crystals are many-body states that spontaneously break translation
symmetry in time the way that ordinary crystals do in space. While experimental observations have conﬁrmed the existence of discrete or continuous
time crystals, these realizations have relied on the utilization of periodic forces
or effective modulation through cavity feedback. The original proposal for
time crystals is that they would represent self-sustained motions without any
external periodicity, but realizing such purely self-generated behavior has not
yet been achieved. Here, we provide theoretical and experimental evidence
that many-body interactions can give rise to an inherent time crystalline phase.
Following a calculation that shows an ensemble of pumped four-level atoms
can spontaneously break continuous time translation symmetry, we observe
periodic motions in an erbium-doped solid. The inherent time crystal produced by our experiment is self-protected by many-body interactions and has
a measured coherence time beyond that of individual erbium ions.

Similar to ordinary crystals where atoms take periodic positions in
space, time crystals are many-body states that spontaneously recur in
time. However, a system spontaneously repeating its pattern implies
the breaking of time translation invariance, which contradicts the timeindependence of most states in conventional theory. The realization of
time crystals was ﬁrst addressed by Wilczek1,2, but subsequent no-go
theorems indicated that they could not exist in thermal equilibrium
states3–5. Nevertheless, recent advancements have led to the realization
of driven discrete time crystals6–8 in close quantum systems, characterized by oscillations at twice the driving periods9–17. Yet, the
heating associated with driving in these closed systems prevents the
persistence of time crystals. Theoretical research suggests that dissipation may overcome the heating issues18–24, leading to the observations of dissipative discrete time crystals25,26. Moreover, if the driving
becomes non-periodic and time-invariant, the studied system acquires
continuous time translation symmetry. Although the potential heating
problem of continuous driving can be worse compared to that of a
periodic force, continuous time translation symmetry can also be
spontaneously broken in dissipative systems18–24,27. Recent experimental observation has conﬁrmed the existence of continuous time
crystals in an atom-cavity system28. Like periodically driven systems,

there remains a built-in frequency stemming from the optical
cavity22,23, which introduces an effective periodic modulation.
The aforementioned discrete and continuous time crystals
depend on the imposition of external periodic constraints, such as
periodic forces or cavities, to break time translation symmetry. However, according to the spirit of the original proposal, time crystals
represent the spontaneous emergence of time-periodic motions
within time-invariant systems. These motions are inherently selftriggered and self-sustained without the need to introduce external
periodic inputs. However, creating such an inherent phase is still a
pending challenge.
Here we report in both theory and experiment that inherent time
crystals can be realized in a dissipative quantum system, which
represents built-in phases of many-body systems that do not rely on
recurring forces or cavities. By exploiting the dipole-dipole interactions within an erbium-ion ensemble, we not only observe the spontaneous breaking of continuous time translation but also the
emergence of temporal order. The resultant self-sustained motion
exhibits a period determined by the system’s parameters and is protected by many-body interactions from inner degrees of freedom.
Furthermore, the persistence of the time crystal’s oscillations reveals

1

Key Laboratory of Advanced Optoelectronic Quantum Architecture and Measurements of Ministry of Education, School of Physics, Beijing Institute of
Technology, 100081 Beijing, China. 2Beijing Key Laboratory of Nanophotonics & Ultraﬁne Optoelectronic Systems, School of Physics, Beijing Institute of
e-mail: zhangxd@bit.edu.cn
Technology, 100081 Beijing, China.

Nature Communications | (2023)14:6161

1

## PDF page 2

Article

https://doi.org/10.1038/s41467-023-41905-3

long-range time correlation beyond the coherence time of
individual ions.

Results
Theoretical model
We investigate a system consisting of a collection of four-level atoms
that are driven by a continuous-wave (CW) laser, as depicted in Fig. 1a, b.
There are a pair of Kramers doublets for both the optical ground and
excited states. The atoms possess electron spins and interact with one
another via magnetic dipole-dipole interactions. The system Hamiltonian is the sum of the Hamiltonian of individual atoms, which is given by
H sys =

X X
ð g,e δ g,i jgihgji + Δe,i jeiheji + Ωge ðri Þjgiheji + Ωge ðri Þjeihgji Þ
i
+

X

J ij

i,j jr

ij j

3

½Si  Sj  3ðSi  r^ij ÞðSj  ^rij Þ,
ð1Þ

where jgii and jeii indicate the optical ground and excited states of the
i th atom, the marks below summation g ð = 1 or 2Þ and eð = 1 or 2Þ
describe two doublets in the ground and excited states,
 δg and Δe are
the frequencies of the ground and excited states, Ωge ri is the Rabi
frequency, J ij is the strength of the dipole interactions, Si is the magnetic dipole moment of the i th atom, rij is the vector connecting two

a

spins Si and Sj , and ^rij is the corresponding unit vector. The ﬁrst term
on the right-hand side of Eq. (1) represents the optical Bloch
description of the light-matter interactions. The second accounts for
the many-body interactions between the ith and the jth atom, which
can lead to an excitation-dependent frequency shift to the ions [See
Supplementary Note 1].
Hamiltonian shown by Eq. (1) can describe various quantum
systems29–32, and is particularly relevant to erbium-doped crystals. In these crystals, the erbium ions exhibit an optical transition
of 1:5 μm, and the effective spins for both their optical ground and
excited states are S = 1=2. Due to the presence of an average
magnetic ﬁeld produced by all other erbium ions in the crystal,
the spin states experience a slight splitting. As a result, the
erbium ions can be considered as a nearly-degenerate four-level
system, as shown in Fig. 1b. When there is no light to drive the
erbium ions, all ions remain in their ground states, and the optical
resonant frequencies of neighboring ions are of no difference (as
shown at the top of Fig. 1a). However, this situation changes if
some ions are optically excited33. Generally, the magnetic dipole
moments of ions in their optical excited states differ from those
in the ground. Therefore, optically exciting an ion can instantaneously change the local magnetic ﬁeld seen by its neighboring
ions. The optical frequencies of nearby ions are thus modiﬁed as a
result of the Zeeman effect34,35, as illustrated at the bottom of

b

ground

driven open system
ρ44
ᛁ4❭
ᛁ3❭
ρ33
optical
transitions

excited

ᛁ2❭
ᛁ1❭

ΔB
c 0.252

ρnn (arb. units)

0.248
0.252

ρ22

ρ11-ρ33
ρ -ρ

0.248 22 44
0.248

0.248
0.252

0.252

population ρnn (arb. units)

0.252 e

ρ33

ρnn (arb. units)

population (arb. units)

ρ22
ρ11

0.252 d

ρ11

0.248
0.252

ρ44
0.248

loss

0

1

2
time (ms)

3

Fig. 1 | Theoretical model for realizing inherent time crystal. a Magnetic manybody interaction. Atoms in their optical ground and excited states have different
magnetic dipole moments. When atoms are optically excited, as shown by the
purple spins, they introduce local magnetic ﬁeld variance ΔB and thus change the
optical resonant frequencies of nearby atoms, as illustrated by the energy levels of
the two green spins at the bottom. b The energy structure of our four-level systems.
The coupling to their environment leads to the decay and decoherence of the
atoms. c The dynamic behaviors of the populations of the four levels. The ρnn ðt Þ

Nature Communications | (2023)14:6161

4

ρ11-ρ22
ρ11-ρ44

0.248
0.248

0.252

population ρ11 (arb. units)

oscillate according to their Rabi frequencies, resulting in a high density of lines in
the plot. The calculation begins with an initial state of an equally-populated mixedstate, that is, ρnn ð0Þ = 0:25, to better demonstrate the long-time behaviors of ρnn ðtÞ.
d Blue, the relationship between ρ11 and ρ33 ; orange, the relationship between ρ22
and ρ44 . e Blue, the relationship between ρ11 and ρ22 ; orange, the relationship
between ρ11 and ρ44 . The parameters of the calculation can be found in Supplementary Note 1.

2

## PDF page 3

Article
Fig. 1a, which in turn affects the absorption of light. Moreover,
the presence of optical spontaneous emission, spin relaxation,
and decoherence makes the erbium ions inherently an open
quantum system. The combined effect of the openness of the
quantum system and the aforementioned excitation-induced
effect can give rise to rich non-equilibrium dynamical phases27.
To explore the physical properties of the four-level erbium system, we use the Runge-Kutta method to calculate the time response of
a collection of erbium ions governed by the Hamiltonian Eq. (1). Speciﬁcally, by applying the mean-ﬁeld approximation36 and introducing
the decay and dephasing terms of the ions, we calculate the density
matrix ρðt Þ in the framework of Lindbald master equation ρ_ = Lρ, where
L is the Lindblad superoperator. The calculation process is detailed in
Method and Supplementary Note 1, and the parameters used are
typical values of erbium ions at a temperature of 4 K. The calculated
results for the population at the nth level ρnn ðt Þ, i.e., the diagonal terms
of ρðt Þ are shown in Fig. 1c.
It is shown clearly that the populations of the four-level system
(ρ11 , ρ22 , ρ33 and ρ44 ) oscillate persistently instead of relaxing to a
stationary state. In conventional systems driven by time-invariant
forces, it is widely believed that the system output is also timeinvariant in the long-time limit. In principle, the emergence of any
oscillations with frequency ω ≠ 0 indicates that the time translation
symmetry is violated. For our calculated system, since it is governed by
a time-invariant Hamiltonian Eq. (1), the corresponding outputs have
to be, if the time translation symmetry holds, time-independent in the
long-time limit. However, if the time translation symmetry is spontaneously broken, then the relaxation to stationarity is no longer guaranteed. The emergence of the persistent oscillations in Fig. 1c strongly
suggests a breaking of the time symmetry in our system. Moreover, a
Fourier analysis of the data ρnn ðt Þ in the long-time limit shows a peak at
the frequency of 46.4 kHz (see Note 2 in SI for more details), further
indicating the formation of temporal order.
To provide further clariﬁcation on the physics of the persistent
oscillation, we examine the relations between different ρnn ðt Þ in Fig. 1d,
e. While ρ11 and ρ22 are nearly-linear functions of ρ33 and ρ44 , respectively, the dependences of ρ22 and ρ44 on ρ11 show the behaviors of
limit cycles37, as shown in Fig. 1d, e. In our calculation, the ratio of the
coupling strength of the transition j1ij3i to the transition j1ij4i is
1.87:1 in the calculation. Thus, the optical ﬁeld is more likely to drive
the transition between j1i and j3i rather than that between j1i and j4i.
Consequently, the population difference of ρ11 and ρ33 is primarily
governed by the balance of optical pumping and dissipations, resulting
in the synchronization of ρ11 and ρ33 through the optical Rabi oscillation, as shown in Fig. 1d (a similar conclusion also holds for the relations of ρ22 to ρ44 and ρ22 to ρ33 ). In contrast, the presence of limit
cycles between ρ22 and ρ11 in Fig. 1e suggests that the changes of ρ11
and ρ22 are not synchronized under the same optical driving. Instead
they undergo a competing process.
It is the competition between different optical transitions that
prevent the system from reaching a stationary state. For a pure twolevel system, where there is only one possible optical transition, it is
impossible to generate a competing process by inner degrees of
freedom18,27. To observe an inherent time crystalline phase, the
energy structure of interacting atoms needs to have more than two
levels. This increased complexity allows the many-body interactions
to act as intrinsic nonlinear interactions and provide positive
feedback to the competition between different optical transitions
(see Supplementary Note 2 and 3 for more details). The interplay
between these complex processes leads to the formation of a
temporal order. Unlike the time crystals so far demonstrated, the
persistent oscillation of ρnn (Fig. 1c) in such a CW-driven four-level
system is purely self-organized, and its recurring frequency is only
determined by the coupling parameters of the system itself, suggesting that the time crystalline order is inherent.

Nature Communications | (2023)14:6161

https://doi.org/10.1038/s41467-023-41905-3

Time crystalline order
In the following, we discuss how to realize such an inherent time crystal
in experiments. We used erbium-doped yttrium orthosilicate
(Er:Y2SiO5) with a concentration of 1000 ppm, corresponding to an
average distance between erbium ions of approximately 4 nm, such
that the average magnetic dipole-dipole interactions between erbium
ions are on the order of 10 MHz (see Supplementary Note 4 for more
details). Additionally, there are two pairs of Kramer doublets separated
by an optical resonance of 1536.4 nm (one of the two 1.5 µm transitions
of erbium ions in Y2SiO538). The effective spins for both their optical
ground and excited states are S = 1=2. If no magnetic ﬁeld is applied,
the optical ground and excited states of erbium ions degenerate at two
levels. However, the spin levels experience a minor degree of splitting
due to the magnetic inﬂuence of all the other erbium ions in the crystal.
That is to say, the effective spin S = 1=2 is split into two levels with small
frequency differences O(0.1 MHz)27, which makes erbium ions a fourlevel system as shown in Fig. 1b. If we further apply a CW laser to drive
the erbium ensemble, then we can construct a system described by
Hamiltonian Eq. (1), where the excited ions can change the resonant
frequency of their neighbors as shown in Fig. 1a. Under certain conditions, the combined effect of the erbium-erbium interactions, the
driving ﬁeld and the losses of erbium ions can prevent the system from
reaching a stationary state27. A periodic motion can emerge as a result
of the inherent competition between different optical transitions.
To investigate the presence of a time crystalline order, we optically excite the erbium ensemble with a CW laser of different frequency
f l and power P in . For notational convenience, all quoted f l in this
paper are the frequencies minus 195117.17 GHz (the center frequency
of the inhomogeneous line of Er:Y2SiO5). The sample is placed in a
cryostat and cooled down to a temperature of 4 K. The light that
double-passes the sample is detected as a function of time I ðt Þ, as
illustrated in Fig. 2a. The measured I ðt Þ is determined by the sample
absorption and thus is directly related to ρðt Þ (see Supplementary
Note 1 and the literature27 for more details). If there is any oscillation in
ρðt Þ as theoretically predicted above, I ðt Þ can be utilized to monitor the
changes.
Figure 2b, c show the measured I ðt Þ as a function of time for two
different P in , where the laser frequency f l = 0:00 GHz is in resonance
with the absorption of erbium ions and the laser is switched on at t = 0
ms. When the pump power is low (P in = 3:8 mW), the erbium ensemble
absorbs most of the laser energy and gives a low output in the
detector, as shown by the gray line in Fig. 2b, c. The output I ðt Þ under
this circumstance eventually relaxes to a stationary value, as expected
for systems with time translation symmetry. However, if the pump
power is increased to P in = 4:7 mW, the I ðt Þ at the beginning is likewise
low, but becomes dynamically unstable after a delay of approximately
12 ms, as shown by the orange line in Fig. 2b. Even in the long-time limit
t ! 1, such oscillating I ðt Þ persists and has a broad-band frequency
response, with a cutoff frequency ~50 MHz27. In our system, the driving
ﬁeld is a CW laser, and the resulting Hamiltonian is time invariant as
well. The emergence of an oscillating I ðt Þ in Fig. 2b, in contrast to a
time-independent output predicted by conventional theory, clearly
suggests a non-stationary ρðt Þ and evidence that the time translation
symmetry is spontaneously broken in the erbium ensemble (see the
literature27 and Supplementary Note 5 for the persistent oscillations).
If we further increase P in = 5:2 mW, similar oscillating I ðt Þ can be
observed, as shown in Fig. 2c. More importantly, for a zoomed segment of I ðt Þ in Fig. 2c, a hidden periodic order can be identiﬁed, which
in contrast is absent in the magniﬁed view of Fig. 2b. This suggests that
a temporally recurring motion, i.e., a time crystalline order, arises if P in
is increased from 4.7 to 5.2 mW. To explicitly determine the time
crystalline order of our sample, the auto-correlation function
I ðt ÞI ðt  τ Þ corresponding to Fig. 2b, c are presented in Fig. 2d. When
the input power (P in = 3:8 mW) is low, the corresponding autocorrelation curve shows linearity, indicating the absence of
3

## PDF page 4

Article

https://doi.org/10.1038/s41467-023-41905-3

Er:YSO

intensity (arb. units)

0.6 c

0.4
17

16

-4

3.8 mW
5.2 mW
0

4 8 12 16 20
time (ms)

0.2

auto corr. (arb. units)

detector: I(t)

0

b

0.4

lens

0.2

0.6

intensity (arb. units)

a
beam splitter

0

-4

17

16

3.8 mW
4.7 mW
0

4 8 12 16 20
time (ms)

1 d

3.8 mW

0.9
4.7 mW
5.2 mW

0.8
0.7
0.6
0

0.5

1.5
1
delay (ms)

2

Fig. 2 | Inherent time crystal in an erbium ensemble. a Schematic drawing of the
experimental setup. A laser beam is input from the left side. There is a mirror at the
right end side of the Er:Y2SiO5 sample, such that the light double-passes the sample
before it hits a detector. The detector gives a time response of I ðt Þ. b Experimental
realization of broken time translation symmetry without time crystalline order. The
laser is switched on at t = 0. Gray, the measured I ðt Þ for P in = 3:8 mW; orange, the

I ðt Þ for P in = 4:7 mW. Inset, the I ðt Þ from 16 to 18 ms for P in = 4:7 mW.
c Experimental realization of broken time translation symmetry together with time
crystalline order. Gray, the measured I ðt Þ for P in = 3:8 mW; blue, the I ðt Þ for
P in = 5:2 mW. Inset, the I ðt Þ from 16 to 18 ms for P in = 5:2 mW. d Auto-correlation of
the data I ðt Þ in (b) and (c) with pump power P in as noted. The laser frequency is set
to f l = 0:00 GHz.

periodicity in I ðt Þ. Upon increasing the input power to 4.7 mW,
although the continuous time translation symmetry is broken (as
shown in Fig. 2b), the correlation curve remains linear (the orange
curve in Fig. 2d). However, at a pump of P in = 5:2 mW, a distinct periodicity can be identiﬁed, as depicted by the blue curve in Fig. 2d.
The periodic oscillation in I ðt Þ is signiﬁcantly different from the
well-known self-pulsing effect in erbium doped ﬁber lasers39–43. Selfpulsing is due to the dynamic interplay or the competition between the
gain and the losses within a laser cavity. As a result, the net gain inside
the cavity is periodically modulated and generate ﬂuctuations in the
laser output. However, our experiment did not adopt such a cavity
conﬁguration as one side of the sample was coated with an antireﬂective layer of less than 0.8% reﬂectivity. Consequently, our
observations could not have been attributed to the self-pulsing effect
in lasers. As aforementioned, the measured I ðt Þ is closely related to
ρðt Þ. Thus, the periodicity in I ðt Þ under a P in = 5:2 mW optical driving
indicates a repeating temporal order of ρðt Þ, which agrees well with the
characteristics of a time crystalline order. Together with the spontaneous breaking of time translation symmetry shown in Fig. 2b, c, and
the lack of imposed periodicity from a driving force or a cavity, the
revealed periodicity in Fig. 2c, d suggest the self-formation of an
inherent time crystalline phase.

after a delay of approximately 14 ms (see Supplementary Note 7 for
more details). This optical instability is veriﬁed by the rising nonzero
frequency components in the spectrum shown by the yellow curve in
Fig. 3a. However, the lack of peak in the spectrum of P in = 8:0 mW
suggests that periodic temporal order is still absent in I ðt Þ. When
increasing the pump power to P in = 9:5 mW, a sharp peak at 8.7 kHz
emerges, as shown by the purple curve in Fig. 3a. The emergence of
such a spectral peak depends on the pumping intensity P in and the
laser frequency f l , and its frequency is of the same as the correlation
curve peak shown in Fig. 2c. This observation suggests that although
the varying Rabi frequency due to different P in can indirectly impact
the time-crystal formation, the underlying mechanism governing the
time crystalline behavior is robust and not directly affected by the Rabi
frequency of the driving ﬁeld. Furthermore, identical time-crystalline
frequency is observed when the crystal is rotated by 0, 20, and 60
degrees, even though the crystal is highly anisotropic and the ground
state g-factors vary between 2 and 15. This result makes it clear that the
oscillating frequency is not caused by interference between two optical transitions split by the Earth’s magnetic ﬁeld or a residual magnetic
ﬁeld. In addition, our calculations indicate that while factors such as
decoherence times and lifetimes have some inﬂuence on the oscillation frequency, the frequency is mostly sensitive to the competition
between different transitions (see Supplementary Note 3).
The curves of P in = 8:0 mW and 9.3 mW indicate a transition from
a phase with broken time translation symmetry but without temporal
order to a phase of self-organized time crystalline order. However,
when the pump power was increased to 13.0 mW, the width of the
8.7 kHz peak broadened signiﬁcantly, as depicted by the blue curve in
Fig. 3a. Such behavior in the spectrum can be attributed to high-order
effects induced by a strong optical pump, where the time crystal
undergoes oscillations with a broad band of other frequencies and the
8.7 kHz temporal order becomes less distinct. This can cause an
imprecise determination of the frequency position. To observe a welldeﬁned temporal order, that is, a time crystal with a long-range

Phase transitions
The emergence of a time crystalline order as shown in Fig. 2 depends
on P in and can be observed for different laser frequencies f l . Shown in
Fig. 3a is the measured spectra of I ðt Þ for different pump power (the
pump laser is always on during the spectral measurements) and for a
different laser detuning f l = 0:50 GHz (see Supplementary Note 6 for
more details). When the pump power is low, for example, P in = 4:0
mW, no oscillating I ðt Þ can be observed in the long-time limit. The
spectral response of such a normal phase is a delta function with its
maximum at zero frequency, as shown by the gray curve in Fig. 3a.
Increasing the pump power to P in = 8:0 mW, I ðt Þ becomes unstable
Nature Communications | (2023)14:6161

4

## PDF page 5

Article

https://doi.org/10.1038/s41467-023-41905-3

13.0 mW
9.5 mW

1 b

spectrum (arb. units)

spectrum (dB)

-50 a

8.0mW
4.0 mW

-70
-90

-110
0

5
10
15
frequency (kHz)

20

0
8

exp. data
Lorentz fit
~ 82 + 30 Hz

8.5
9
9.5
frequency (kHz)

10

cross correlation
(arb. units)

1 c

0

69

71

73
delay (ms)

75

77

Fig. 3 | Phase transitions and coherence time. a Phase transitions with pumppower dependence. Measured spectra of the time crystal at different pump powers
as noted. The laser frequency is f l = 0:50 GHz. b Lorentz ﬁt of the 8.7 kHz spectral

peak of P in = 9:5 mW. c Phase noise of the inherent time crystal. The crosscorrelation F ðτ Þ shows that the periodicity of I ðt Þ remains even for 70 ms. Time
points with phase discontinuity are marked by circles.

temporal correlation or a long coherence time, it is critical to set a
proper optical driving ﬁeld.
Noting that the spectrum of P in = 9:5 mW in Fig. 3a has the narrowest linewidth, we use it to determine the coherence time of the
time crystal. The full width at half-maximum given by a Lorentz ﬁtting
is Γ = 82 ± 30 Hz (Fig. 3a), corresponding to a coherence time of
T 2 = 1=πΓ = 4 ± 2 ms, which is beyond that of individual erbium ions
(for reference, the coherence time of erbium ions in a 50 ppm
Er:Y2SiO5 at 4.2 K is on the order of 10 μs44). Ideally, periodic oscillations of a time crystal maintain phase coherence over indeﬁnitely long
periods of time45,46. Because the long-range temporal order of a time
crystal is protected by many-body interactions and its coherence is
robust to the dephasing effect of the environment.
Unlike an ideal one, our time crystal shows a ﬁnite coherence time
in the long-time limit (Fig. 3b), suggesting that its periodic oscillations
are consecutive and dephase in a time scale of ∼ 4 ms. To reveal the
dephasing on the
of I ðt Þ, we deﬁne a cross-correlation
 oscillations

function F ðτ Þ = I ðt Þr ðt  τ Þ , where r ðt Þ is a reference pulse function
oscillating with 8.7 kHz. Such that F ðτ Þ reproduces the phase information of I ðt Þ for τ = t (see Method and Supplementary Note 8 for
detailed discussions).
As an example, the consecutive periodicities of our time crystal
for the delay of 69–77 ms are shown in Fig. 3c [F ðτ Þ at other delays can
be found in Supplementary Note 9]. It is clear that the oscillations
shown in Fig. 3c can be divided into segments with temporal lengths of
~4 ms, among which phase discontinuities arise, as marked by the
circles in Fig. 3c. These phase discontinuities indicate that random
phase shifts arise at the corresponding time points, which interrupt I ðt Þ
from being a perfectly periodic signal. That is to say, the present result
is subjected to modulations from phase noise on a time scale of ms.
Note that the root-mean-square stability of the intensity of our
laser is 0.2% in ms scale, and its frequency drift, caused by temperature
ﬂuctuations, is approximately 0.2 MHz/s. These parameters are not
signiﬁcant enough to produce any noticeable effects on our system.
However, our driving laser has a phase-noise-limit linewidth of less
than 100 Hz. We then performed a calculation to estimate how phase

shifts in the driving ﬁeld affect the inherent time crystal (see Supplementary Note 10 for more details). The results show that phase perturbations in the driving can break the time crystalline oscillations into
consecutive segments similar to what is shown in Fig. 3c. Given that the
linewidths of our time crystal and that of our laser are in the same
order, together with the similar phase-modulated behaviors of our
calculated results (Supplementary Note 10) and the experimental
results (Fig. 3c), we ascribe the dephasing of our time crystal to the
phase noise of the driving laser.
Such a dephasing time, approximately 4 ms, is signiﬁcantly longer
than the coherence time of individual erbium ions in the YSO crystal44,
which suggests the protection of the crystalline order by many-body
interactions beyond the dephasing nature of individual ions. Additionally, our theory contradicts the idea that the coherence time of the
time crystal is limited by the decoherence or decay time of erbium
ions. As long as the driving ﬁeld and nonlinear interaction can disrupt
time translation symmetry, the time crystalline order remains persistent. Our experiments also show that the self-organized periodic
oscillations coexist with the intrinsic optical instability phase of erbium
ions27, meaning the time crystalline order persists even amidst irregularly oscillating instabilities as fast as ~50 MHz.
Driven dissipative systems are known to self-support periodic
motion, as demonstrated in the work of Prigogine and others47. Our
erbium system shares some essential parallels with conventional dissipative structures. Firstly, erbium ions in our system are subject to
atomic decay and dechonerence, thus forming an open quantum
system. The application of a coherent laser further drives the system
into a far-from-equilibrium state. Secondly, nonlinear erbium interactions, that is, the excitation induced frequency shift, play a crucial role
in amplifying small perturbations and driving the erbium ensemble
into a new stable dissipative order. Thirdly, the multiple-level energy
structure of erbium ions provides sufﬁcient degrees of freedom for
triggering the intrinsic competition between different optical transitions. Nonetheless, the periodic motion of erbium ions differs from
processes like the Bérnard experiment and the Belousov-Zhabotinsky
reaction, as the erbium time crystal is a many-body system governed

Nature Communications | (2023)14:6161

5

## PDF page 6

Article

https://doi.org/10.1038/s41467-023-41905-3

by a coherent driving rather than an intensity input. As a result, the
phase of the pump laser signiﬁcantly affects the time crystal, as shown
in Fig. 3 and Note 10 in SI. In addition, the conventional dissipative
structures require an external source of noise, while in our quantum
erbium ensemble, the noise is intrinsic and does not require a speciﬁc
external reference.
In conclusion, we have demonstrated in both theory and experiment that time crystal is an inherent phase of nonequilibrium manybody systems. The realization of an inherent time crystal in an
ensemble of erbium ions indicates that many-body interaction not
only can self-induce a temporal crystalline order, but also can protect it
against environmental decoherence. The self-organized periodic
oscillations are persistent and have a coherence time beyond that of
individual erbium ions. The results here pave the way to create states
of matter in a strongly correlated system. In particular, it should be
possible to use many-body interactions to create robust quantum
superposition states with long coherence times. Such phases can also
be extended to microwave-driven systems for potential applications
such as quantum metrology and quantum memories.

is a rectangle function with an open duration of T. The crosscorrelation
R + 1 function between our measured I ðt Þ and r ðt Þ is deﬁned as
F ðτ Þ = 1 I ðt Þr ðt  τ Þdt. It is already known from our experiment that
the phase noise ϕðt Þ of I ðt Þ is a slowly-varying function of time (on the
order of 1 ms), and the auto-correlation function of I ðt Þ indicates a
periodicity at the frequency of ω0 = 8.7 kHz. Note also that, as
discussed in our previous work30, I ðt Þ oscillates rapidly at frequencies
on the order of 10 MHz. By choosing
T ∼0:1 ms and ωr = 8:7 kHz,


ωr T ! 0, we obtain that
which leads
to
the
limit
that
ω
0


F ðτ Þ / cos ω0 τ + ϕðτ Þ . This result means that we can reproduce the
phase information ϕðt Þ of I ðt Þ by choosing different τ when calculating
F ðτ Þ. The time resolution is determined by T.

Methods

References

Theoretical method

1.

Due to the complex nature of many-body systems, the parameters of
H sys in Eq. (1), such as δ g,i and J i,j , vary from atom to atom. It is
impractical to calculate the response of such a system in a full quantum
way. To obtain a basic understanding of the phases of the nonequilibrium erbium ensemble, we ﬁrst disregard the inhomogeneities
by setting δ g,i  δ g , Δe,i  Δe , Ωge ðri Þ  Ωge , that is to say, the detunings and the Rabi frequencies for all erbium ions are the same. We then
apply the mean-ﬁeld approximation to our system, which means that
N
the system density matrix can be factorized ρsys = k ρk , and the
reduced density matrix of the i th atom is given by ρi = Tr≠i ðρsys Þ. The
homogeneous mean-ﬁeld Hamiltonian of our system is written as

Data availability
The experimental data supporting the ﬁndings in this paper are
included in the main article and the Supplementary Materials. The
codes can be obtained from the corresponding author upon request.
The source data generated in this study are provided in the Source
Data ﬁle.

2.
3.
4.
5.
6.
7.

H i = δ 2 σ 22 + δ 3 σ 33 + δ 4 σ 44
+ Ω13 σ 13 + Ω14 σ 14 + Ω23 σ 23 + Ω24 σ 24
ð2Þ




+ Δs ρ44 + ρ33  ρ22  ρ11 σ 33 + Δs ρ44 + ρ33  ρ22  ρ11 σ 44 ,

8.

Using this Hamiltonian, we can compute the Lindblad equation
ρ_ = Lρ and obtain the time response of a collection of erbium ions
(more details in Supplementary Note 1).

9.

Optical measurements

11.

The optical measurements are performed on an Er:Y2SiO5 sample,
which has 1000 ppm of yttrium ions replaced by erbium ions. The
resonance frequency of the erbium ions is at 1536.4 nm
(195177.17 THz), corresponding to spectroscopic site 1 (following
the literature convention for spectroscopic site assignments).
For notational convenience, all quoted laser frequencies fl in the
paper are relative frequencies, that is, the absolute frequencies
subtracted by 195117.17 GHz. One side of the sample was coated
to achieve a reﬂectivity of 98.8%, while the other end was coated
with an anti-reﬂective layer of less than 0.8% reﬂectivity. The
sample is cooled to 4.0 K by a cryostat. The intensity instability of
our laser (E15, NTK) is 2% on a 10 s scale, and the laser linewidth is
documented as less than 100 Hz.

Data analysis using cross-correlation function
A reference pulse function
with an oscillating frequency of ωr is
 
deﬁned as r ðt Þ = cos ωr t  rectðt Þ, where
8
>
< 0,
rectðt Þ = 1,
>
:
0,

if
if

t <0
0≤t≤T

if

t >T

Nature Communications | (2023)14:6161

ð3Þ

10.

12.

13.

14.
15.

16.
17.
18.

19.

Wilczek, F. Quantum time crystals. Phys. Rev. Lett. 109,
160401 (2012).
Shapere, A. & Wilczek, F. Classical time crystals. Phys. Rev. Lett.
109, 160402 (2012).
Bruno, P. Impossibility of spontaneously rotating time crystals: a NoGo theorem. Phys. Rev. Lett. 111, 070402 (2013).
Nozières, P. Time crystals: can diamagnetic currents drive a charge
density wave into rotation. Europhys. Lett. 103, 57008 (2013).
Watanabe, H. & Oshikawa, M. Absence of quantum time crystals.
Phys. Rev. Lett. 114, 251603 (2015).
Sacha, K. Modeling spontaneous breaking of time-translation
symmetry. Phys. Rev. A 91, 033617 (2015).
Khemani, V., Lazarides, A., Moessner, R. & Sondhi, S. L. Phase
structure of driven quantum systems. Phys. Rev. Lett. 116,
250401 (2016).
Else, D. V., Bauer, B. & Nayak, C. Floquet time crystals. Phys. Rev.
Lett. 117, 090402 (2016).
Zhang, J. et al. Observation of a discrete time crystal. Nature 543,
217 (2017).
Choi, S. et al. Observation of discrete time-crystalline order in a
disordered dipolar many-body system. Nature 543, 221 (2017).
Smits, J., Liao, L., Stoof, H. T. C. & van der Straten, P. Observation of
a space-time crystal in a superﬂuid quantum gas. Phys. Rev. Lett.
121, 185301 (2018).
Rovny, J., Blum, R. L. & Barrett, S. E. Observation of discrete-timecrystal signatures in an ordered dipolar many-body system. Phys.
Rev. Lett. 120, 180603 (2018).
Autti, S., Eltsov, V. B. & Volovik, G. E. Observation of a time quasicrystal and its transition to a superﬂuid time crystal. Phys. Rev. Lett.
120, 215301 (2018).
Kyprianidis, A. et al. Observation of a prethermal discrete time
crystal. Science 372, 1192 (2021).
Randall, J. et al. Many-bodylocalized discrete time crystal with a
programmable spin-based quantum simulator. Science 374,
1474 (2021).
Mi, X. et al. Time-crystalline eigenstate order on a quantum processor. Nature 601, 531 (2022).
Zhang, X. et al. Digital quantum simulation of Floquet symmetryprotected topological phases. Nature 607, 468 (2022).
Vlasov, R. A., Lemeza, A. M. & Gladush, M. G. Dynamical instabilities
of spectroscopic transitions in dense resonant media. Laser Phys.
Lett. 10, 045401 (2013).
Gong, Z., Hamazaki, R. & Ueda, M. Discrete time-crystalline order in
cavity and circuit QED systems. Phys. Rev. Lett. 120, 040404 (2018).
6

## PDF page 7

Article
20. Iemini, F. et al. Boundary time crystals. Phys. Rev. Lett. 121,
035301 (2018).
21. Bŭca, B., Tindall, J. & Jaksch, D. R. Non-stationary coherent quantum
many-body dynamics through dissipation. Nat. Commun. 10,
1730 (2019).
22. Keßler, H., Cosme, J. G., Hemmerling, M., Mathey, L. & Hemmerich,
A. Emergent limit cycles and time crystal dynamics in an atomcavity system. Phys. Rev. A 99, 053605 (2019).
23. Piazza, F. & Ritsch, H. Self-ordered limit cycles, chaos, and phase
slippage with a superﬂuid inside an optical resonator. Phys. Rev.
Lett. 115, 163601 (2015).
24. Booker, C., Bŭca, B. & Jaksch, D. Non-stationarity and dissipative
time crystals: spectral properties and ﬁnite-size effects. New J.
Phys. 22, 085007 (2020).
25. Keßler, H. et al. Observation of a dissipative time crystal. Phys. Rev.
Lett. 127, 043602 (2021).
26. Taheri, H., Matsko, A. B., Maleki, L. & Sacha, K. All-optical dissipative
discrete time crystals. Nat. Commun. 13, 848 (2022).
27. Chen, Y.-H., Horvath, S. P., Longdell, J. J. & Zhang, X. Optically
unstable phase from ion-ion interactions in an erbium-doped crystal. Phys. Rev. Lett. 126, 110601 (2021).
28. Kongkhambut, P. et al. Observation of a continuous time crystal.
Science 377, 670 (2022).
29. Karabanov, A., Rose, D. C., Köckenberger, W., Garrahan, J. P. &
Lesanovsky, I. Phase transitions in electron spin resonance under
continuous microwave driving. Phys. Rev. Lett. 119, 150402
(2017).
30. Lee, T. E., Häffner, H. & Cross, M. C. Antiferromagnetic phase
transition in a nonequilibrium lattice of Rydberg atoms. Phys. Rev. A
84, 031402 (2011).
31. Carr, C., Ritter, R., Wade, C. G., Adams, C. S. & Weatherill, K. J.
Nonequilibrium phase transition in a dilute Rydberg ensemble.
Phys. Rev. Lett. 111, 113901 (2013).
32. Ahlefeldt, R. L., McAuslan, D. L., Longdell, J. J., Manson, N. B. &
Sellars, M. J. Precision measurement of electronic ion-ion interactions between neighboring Eu3+ optical centers,. Phys. Rev. Lett. 111,
240501 (2013).
33. Mitsunaga, M., Takagahara, T., Yano, R. & Uesugi, N. Excitationinduced frequency shift probed by stimulated photon echoes
Masaharu. Phys. Rev. Lett. 68, 3216 (1992).
34. Huang, J., Zhang, J. M., Lezama, A. & Mossberg, T. W. Excess
dephasing in photon-echo experiments arising from excitationinduced electronic level shifts. Phys. Rev. Lett. 63, 78 (1989).
35. Liu, G. K. & Cone, R. L. Laser-induced instantaneous spectral diffusion in Tb3+ compounds as observed in photon-echo experiments.
Phys. Rev. B 41, 6193 (1990).
36. Diehl, S., Tomadin, A., Micheli, A., Fazio, R. & Zoller, P. Dynamical
phase transitions and instabilities in open atomic many-body systems. Phys. Rev. Lett. 105, 015702 (2010).
37. Chan, C.-K., Lee, T. E. & Gopalakrishnan, S. Limit-cycle phase in
driven-dissipative spin systems. Phys. Rev. A 91, 051601 (2015).
38. Maksimov, B. A., Kharitonov, Y. A., Ilyukhin, V. V. & Belov, N. V. The
crystal structure of yttrium oxiorthosilicate the dual function of
yttrium. Sov. Phys. Crystallogr. 15, 806 (1970).
39. Sanchez, F. & Stephan, G. General analysis of instabilities in erbiumdoped ﬁber lasers. Phys. Rev. E 53, 2110 (1996).
40. Loh, W. H. Suppression of self-pulsing behavior in erbium-doped
ﬁber lasers with resonant pumping. Opt. Lett. 21, 734 (1996).
41. Luo, L. & Chu, P. L. Suppression of self-pulsing in an erbium-doped
ﬁber laser. Opt. Lett. 22, 1174 (1997).

Nature Communications | (2023)14:6161

https://doi.org/10.1038/s41467-023-41905-3
42. Rangel-Rojo, R. & Mohebi, M. Study of the onset of self-pulsing
behaviour in an Er-doped ﬁbre laser. Opt. Commun. 137, 98 (1997).
43. El-Sherif, A. F. & King, T. A. Dynamics and self-pulsing effects in
Tm3+-doped silica ﬁbre lasers. Opt. Commun. 208, 381 (2002).
44. Thomas Böttger, C. W., Thiel, Y., Sun, R. L. & Cone Optical decoherence and spectral diffusion at 1.5 µm in Er3+:Y2SiO5 versus
magnetic ﬁeld, temperature, and Er3+ concentration. Phys. Rev. B
73, 075101 (2006).
45. Tucker, K. et al. Shattered time: Can a dissipative time crystal survive many-body correlations. New J. Phys. 20, 123003 (2018).
46. Lledó, C. & Szymańska, M. H. A dissipative time crystal with or
without Z2 symmetry breaking. New J. of Phys. 22, 075002 (2020).
47. Prigogine, I. Time, structure, and ﬂuctuations. Science 201,
777 (1978).

Acknowledgements
The authors would like to thank Zhang-Qi Yin for helpful discussions.
This work was supported by the National Natural Science Foundation of
China (Nos. 62105033 and 12174026).

Author contributions
Y.H.C. and X.Z. developed the idea, conducted the work, and prepared
the manuscript.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information The online version contains
supplementary material available at
https://doi.org/10.1038/s41467-023-41905-3.
Correspondence and requests for materials should be addressed to
Xiangdong Zhang.
Peer review information Nature Communications thanks the anonymous reviewer(s) for their contribution to the peer review of this work. A
peer review ﬁle is available.
Reprints and permissions information is available at
http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional afﬁliations.
Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as
long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons licence, and indicate if
changes were made. The images or other third party material in this
article are included in the article’s Creative Commons licence, unless
indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted
use, you will need to obtain permission directly from the copyright
holder. To view a copy of this licence, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2023

7
