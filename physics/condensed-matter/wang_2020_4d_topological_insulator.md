Source: https://doi.org/10.1038/s41467-020-15940-3
PDF sha256: 5efd4e5ab05ca6bf9773459b11fbb0a429f48c6a22fcd54f1f9dec72180039c0
License: https://creativecommons.org/licenses/by/4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of wang_2020_4d_topological_insulator.pdf

Transcription of `wang_2020_4d_topological_insulator.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

University of Birmingham

Circuit implementation of a four-dimensional
topological insulator
Wang, You; Price, Hannah M.; Zhang, Baile; Chong, Y. D.
DOI:
10.1038/s41467-020-15940-3
License:
Creative Commons: Attribution (CC BY)
Document Version
Publisher's PDF, also known as Version of record
Citation for published version (Harvard):
Wang, Y, Price, HM, Zhang, B & Chong, YD 2020, 'Circuit implementation of a four-dimensional topological
insulator', Nature Communications, vol. 11, no. 1, 2356. https://doi.org/10.1038/s41467-020-15940-3

Link to publication on Research at Birmingham portal

General rights
Unless a licence is specified above, all rights (including copyright and moral rights) in this document are retained by the authors and/or the
copyright holders. The express permission of the copyright holder must be obtained for any use of this material other than for purposes
permitted by law.
•Users may freely distribute the URL that is used to identify this publication.
•Users may download and/or print one copy of the publication from the University of Birmingham research portal for the purpose of private
study or non-commercial research.
•User may use extracts from the document in line with the concept of ‘fair dealing’ under the Copyright, Designs and Patents Act 1988 (?)
•Users may not further distribute the material nor use it for the purposes of commercial gain.
Where a licence is displayed above, please note the terms and conditions of the licence govern your use of this document.
When citing, please reference the published version.
Take down policy
While the University of Birmingham exercises care and attention in making items available there are rare occasions when an item has been
uploaded in error or has been deemed to be commercially or otherwise sensitive.
If you believe that this is the case for this document, please contact UBIRA@lists.bham.ac.uk providing details and we will remove access to
the work immediately and investigate.

Download date: 11. Mar. 2026

## PDF page 2

ARTICLE
https://doi.org/10.1038/s41467-020-15940-3

OPEN

Circuit implementation of a four-dimensional
topological insulator

1234567890():,;

You Wang1, Hannah M. Price

2, Baile Zhang

1,3 ✉ & Y. D. Chong1,3 ✉

The classiﬁcation of topological insulators predicts the existence of high-dimensional topological phases that cannot occur in real materials, as these are limited to three or fewer
spatial dimensions. We use electric circuits to experimentally implement a four-dimensional
(4D) topological lattice. The lattice dimensionality is established by circuit connections, and
not by mapping to a lower-dimensional system. On the lattice’s three-dimensional surface,
we observe topological surface states that are associated with a nonzero second Chern
number but vanishing ﬁrst Chern numbers. The 4D lattice belongs to symmetry class AI,
which refers to time-reversal-invariant and spinless systems with no special spatial symmetry. Class AI is topologically trivial in one to three spatial dimensions, so 4D is the lowest
possible dimension for achieving a topological insulator in this class. This work paves the way
to the use of electric circuits for exploring high-dimensional topological models.

1 Division of Physics and Applied Physics, School of Physical and Mathematical Sciences, Nanyang Technological University, Singapore 637371, Singapore.
2 School of Physics and Astronomy, University of Birmingham, Edgbaston, Birmingham B15 2TT, UK. 3 Centre for Disruptive Photonic Technologies, Nanyang
Technological University, Singapore 637371, Singapore. ✉email: blzhang@ntu.edu.sg; yidong@ntu.edu.sg

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

1

## PDF page 3

ARTICLE

T

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

opological insulators are materials that are insulating in the
bulk but host surface states protected by nontrivial topological features of their bulk bandstructures1,2. They are
classiﬁed according to symmetry and dimensionality3–7, with
each class having distinct and interesting properties. The celebrated two-dimensional Quantum Hall (2DQH) phase8, for
instance, has topological edge states that travel unidirectionally
on the one-dimensional (1D) edge, whereas three-dimensional
(3D) topological insulators based on spin-orbit coupling have
surface states that act like massless 2D Dirac particles. The classiﬁcation of topological insulators contains hypothetical highdimensional phases3 that cannot be realised with real materials,
since electrons only move in one, two, or three spatial dimensions. These include several types of four-dimensional Quantum
Hall (4DQH) phases, which are characterised by a 4D topological
invariant called the second Chern number and exhibit a much
richer phenomenology than the 2DQH phase9–12. In recent years,
topological phases have been implemented in a range of engineered systems including cold atom lattices13, photonic structures14, acoustic and mechanical resonators15,16, and electric
circuits17–28. Some of these platforms can realise lattices that are
hard to achieve in real materials, raising the intriguing prospect of
using them to create high-dimensional topological insulators.
Although there have been demonstrations of topological pumps
that map 4D topological lattice states onto lower-dimensional
systems29–32, there has been no experimental realisation of a 4D
topological insulator with protected surface states on a 3D
surface.
Here, we describe the implementation of a 4DQH phase using
electric circuits to access higher dimensions. Since electric circuits
are deﬁned in terms of lumped (discrete) elements and their
interconnections, lattices with genuine high-dimensional structure can be explicitly constructed by applying the appropriate
connections33–35. In this way, we experimentally implement a 4D
lattice hosting the ﬁrst realisation of a Class AI topological
insulator5,6, which has no counterpart in three or fewer spatial
dimensions.
In the symmetry-based classiﬁcation of topological phases3–7,
Class AI includes time-reversal (T) symmetric, spinless systems
that are not protected by any special spatial symmetries. Whereas
the 2DQH phase is tied to nontrivial values of the ﬁrst Chern
number, which requires T-breaking36, 4DQH phases rely on the
second Chern number, which does not9–12. Even though the
Class AI conditions are ubiquitous13,14, the class is topologically
trivial in one to three dimensions3–7. Hence, realising a Class AI
topological insulator requires going to at least 4D. We focus on a
theoretical 4D lattice model recently developed by one of the
authors37, which exhibits a nonzero second Chern number with
vanishing ﬁrst Chern numbers. Hence, we obtain the ﬁrst
observations of topological surface states that are intrinsically tied
to 4D band topology, with no connection to lower-dimensional
topological invariants.
The present approach, based on circuit connections, is distinct
from other recently-investigated methods for accessing higherdimensional models. One of the alternatives involves manipulating internal degrees of freedom, such as oscillator modes, to
act as synthetic dimensions38–52. Although there have been theoretical proposals for using synthetic dimensions to build 4D
topological lattices40,43, all experiments so far have been limited
to 1D and 2D51. Another approach involves adiabatic topological
pumping schemes, which map high-dimensional models onto
lower-dimensional setups by replacing spatial degrees of freedom
with tunable parameters29–32. As mentioned above, 2D topological pumps based on cold atoms and photonics have recently
been used to explore Class A (T-broken) 4DQH systems30,53,54.
However, topological pumps have the drawback of being
2

inherently limited to probing speciﬁc quasi-static solutions of a
high-dimensional system, without realising a genuinely highdimensional lattice. Moreover, in those experiments the second
Chern number in 4D is not truly independent of the ﬁrst Chern
numbers in 2D, which are nonzero.
Our 4D lattice is implemented using electric circuits with
carefully chosen capacitive and inductive connections. The
lattice model has two topologically distinct phases: a 4DQH
phase and a conventional (i.e. topologically trivial) 4D band
insulator, with the choice of phase governed by a parameter m
that maps to certain combinations of capacitances and inductances. Using impedance measurements that are equivalent to
ﬁnding the local density of states (LDOS), we show that the
4DQH phase hosts surface states on the 3D surface, while the
conventional insulator phase has only bulk states. By varying
the driving frequency, we show that the topological surface
states span a frequency range corresponding to a bulk bandgap,
as predicted by theory. Our experimental results also agree well
with circuit simulations. This work demonstrates that electric
circuits are a ﬂexible and practical way to realise higherdimensional lattices, paving the way for the exploration of other
previously-inaccessible topological phases.
Results
4DQH model and circuit realisation. The 4D lattice model is
shown schematically in Fig. 1a. The spatial coordinates are
denoted x, y, z, and w. The lattice contains four sublattices
labelled A, B, C and D, with sites connected by real nearest
neighbour hoppings ±J. The four bands host two pairs of Dirac
points in the Brillouin zone; each pair is the time-reversed
counterpart of the other. To control the pairs separately, longrange hoppings with amplitudes ± J 0 and ±J″ are added within
the x–z plane (these hoppings are omitted from Fig. 1a for clarity,
but are shown in Fig. 1c). Upon adding mass +m to the A and
B sites, and −m to the C and D sites, the Dirac masses
for the different Dirac point pairs close at m ¼ J 0  2J 00 and
m ¼ J 00  2J 0 . These gap closings are topological transitions, such
that, for J 00 ¼ J 0 , the second Chern number of the lower bands
is −2 (nontrivial) if jmj < 3jJ 0 j. Since T is unbroken, the ﬁrst
Chern number is always zero, so the model exhibits QH behaviour stemming purely from the second Chern number37. For
further details about the model, see Supplementary Note 1.
We take J = 1 and J 0 ¼ J 00 ¼ 2, so that the topological
transition of the bulk lattice occurs at m = ±6. We target a ﬁnite
4D lattice with six sites along the x and z directions, and two sites
along y and w. To mitigate ﬁnite-size effects, periodic boundary
conditions are applied in y and w using nearest neighbour type
connections between opposite ends of the lattice. This corresponds to sampling at ky = kw = 0 in momentum space, where
the gap closing occurs during the topological transition (see
Supplementary Note 1). Regardless of these periodic boundary
conditions, the spatial dimensionality established by the connectivity of the lattice sites is 4D33. The lattice has a total of
144 sites, of which we consider 16 to be bulk sites (deﬁned as
being more than two sites away from a surface) and 128 to be
surface sites.
The ﬁnite 4D lattice is implemented with a set of connected
printed circuit boards, shown in Fig. 1b. Each site i of the tightbinding model maps to a node on the circuit, and the mass term
maps to a circuit component of conductance −Dii connecting the
node to ground. Each hopping Jij between sites i and j maps to a
circuit element of conductance Dij connecting the nodes. We add
extra grounding components with conductance D0ii in parallel
with −Dii. If an external AC current Ii ﬂows into each node i at
frequency f, and Vi is the complex AC voltage on that node,

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

## PDF page 4

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

a

B
A

D
A

b

C

C

w
x
z
B

A

C
A

D

D

y
z
x

c

A

C

D

B

Fig. 1 Model of the 4D Quantum Hall lattice and its circuit implementation. a Schematic of the 4D tight-binding model. Each unit cell consists of four
sites labelled A–D. Hollow and ﬁlled circles respectively denote positive (m) and negative (−m) on-site masses, while yellow solid lines and blue dashes
respectively denote positive (J) and negative (−J) hoppings. b Photographs of the circuit. c Schematic of the circuit; positive (negative) masses are realised
by capacitors (inductors) connecting the sites to ground, and hoppings are realised using capacitors or inductors connecting different sites. The
components shown here are C0 = 1 nF (yellow lines), L0 = 2 mH (blue dashes), C0 ¼ 2 nF (purple curves), L0 ¼ 1 mH (green curves), and Cm = 2mC0 (grey
dashes). Each site is grounded by a set of additional circuit components (see Supplementary Note 2); for clarity, only the grounding components for two
sites (in the dashed red box) are depicted.

Kirchhoff’s law states that
I i ¼ ðDii þ D0ii ÞV i þ

X
j

Dij ðV i  V j Þ:

ð1Þ

We deﬁne Dij( f ) = iαHij( f ), where α is a positive real constant.
Then capacitances (inductances) correspond to positive (negative) real values of Hij. We require that at a reference working
frequency f = f0, the values of Hij(f0) match the desired tight-

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

3

## PDF page 5

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

a

b

3

4

4

2

2

E

Surface states

0

1

0

0
–1

–2

–2
Bulk bands

Surface concentration

2

Bulk bands

–2

–4

–4

–8 –6 –4 –2

c

0
m

2

4

6

–8

8

m = 0, E = 0

–6

–4 –2

d

0
m

2

4

6

8

–3

m = 0, E = 1

z

z
x

x

w

w

y

e

y

m = 4, E = 0

z

f

m = 8, E = 0

z
x

w

x

w

y

y

0

Max

Fig. 2 Band diagram and local density of states of the 4D lattice. a Calculated band diagram for the inﬁnite 4D lattice. The bulk bands are shown in grey.
For ∣m∣ < 6, there is a bandgap associated with nontrivial second Chern number, accompanied by topological surface states (shaded green). For ∣m∣ > 6, the
bandgap is trivial. b Calculated band diagram for 144-site lattice with periodic boundary conditions along y and w. Colours indicate the degree of surface
concentration of the energy states, as deﬁned Eq. (5). Due to ﬁnite-size effects, surface states occur at ∣m∣ ≲ 2 and the gap closing is shifted to ∣m∣ ≈ 4.
The parameters corresponding to subplots c–f are indicated with pink dots. c–f Experimentally-obtained LDOS maps for different m and E, measured at
working frequency f = f0. Surface states are observed in c, d consistent with theoretical predictions.

binding lattice Hamiltonian (see “Methods”). We then tune D0 so
that for f = f0,
X
D0ii þ
Dij ¼ iαE;
ð2Þ

m parameter. Equation (1) now becomes

for some target energy E; the required value of D0 depends on the

where Lij are the components of the circuit Laplacian L. The

j≠i

4

Ii 

X
j

Lij V j ¼ iα

X
½H ij ðf Þ  E δ ij V j ðf Þ;
j

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

ð3Þ

## PDF page 6

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

j

3
2

ð4Þ

where ψ(r) denotes the energy eigenfunction, whose magnitudes
are averaged over either surface or bulk sites. Due to the ﬁnite
lattice size, both the bulk and surface spectrum are split into subbands. The closing of the bulk gap is shifted to ∣m∣ ≈ 4, and the
surface states occur most prominently at small values of E and ∣m∣.
We now fabricate a set of circuits with parameters
m ∈ {0, 1, …, 8} and E ∈ {0, 1}. Figure 2c–f shows the measured
LDOS (at f = f0) for four representative samples. From the
experimental data, we see that the surface LDOS is high and the
bulk LDOS is low when in the topologically nontrivial bandgap
(Fig. 2c, d). For E = 0, m = 4, which corresponds roughly to the
gap-closing point, there is no signiﬁcant difference between the
surface and bulk LDOS. For E = 0, m = 8, the LDOS on all sites is
low, consistent with being in a topologically trivial bandgap.
These results also agree well with circuit simulations (see
Supplementary Note 3). The robustness of the surface states, a
feature imparted by topological protection, can be inferred from
the fact that each individual circuit component has up to 10%
deviation in its capacitance or inductance (see “Methods”). We
emphasise that the surface states cannot be explained by the ﬁrst
Chern numbers, which are necessary zero since the circuit design
is T symmetric.
To conﬁrm that the discrepancy between Fig. 2a and b is just a
ﬁnite-size effect, Fig. 3 shows calculated band edges (i.e. the pair of
eigenvalues closest to E = 0) for a series of lattices with 6, 8, 10, 14,
20, and 50 sites along both x and z (the lattices are kept two sites
wide along y and w, with periodic boundary conditions).
The colours indicate whether the eigenstate is concentrated on
the surface (red) or in the bulk (blue). As the size of the lattice
increases in x and z, the eigenvalues at large m (in the conventional
insulator regime) approach the predicted bulk band edges, while the
eigenvalues in the topological insulator regime spread over a larger
range of m corresponding to the topologically nontrivial gap.
To quantify the difference between the 4DQH and conventional insulator phases, we examine the ratio of the mean
LDOS on surface sites to the mean LDOS on bulk sites, for
different values of the mass detuning parameter m (Fig. 4a).
The ratio is derived from experimental measurements performed at f = f0, corresponding to E = 0; with increasing m, it
decreases sharply from around 4.5 in the 4DQH regime to
around 1 in the conventional insulator regime. Circuit
simulations produce results in agreement with the experimental data (Fig. 4f).
The frequency dependence of the circuit impedance is also
consistent with the spectral features of a topological insulator at
small values of m. Figure 4b–e plots the experimentally-obtained

3
2

It can be shown that Re½Z r ðf 0 Þ is, up to a scale factor, the LDOS
of the target lattice at energy E (see “Methods”). For further
details about the circuit analysis, see Supplementary Note 2.
Experimental results. Figure 2a shows the band diagram of the
inﬁnite bulk tight-binding model as a function of the mass
detuning parameter m. For ∣m∣ < 6, the system is in a 4DQH
phase, with a topologically nontrivial bandgap centred at E = 0,
which hosts topological surface states.
The band diagram for the 144-site tight-binding model is
shown in Fig. 2b. The colours of the curves indicate the degree
to which each eigenstate is concentrated on the surface, as
deﬁned by


ð5Þ
ln hjψðrÞjisurf : = hjψðrÞjibulk ;

10
4 5 7 25

1
1
E

0

0
–1

–1

Surface concentration

impedance between node r and ground is
X
Vr ¼
ðL1 Þrj I j ¼ Z r I r :

–2

–2
–10

–3
–5

0
m

5

10

Fig. 3 Band diagrams for lattices of different sizes. Eigenvalue pairs
closest to E = 0 for lattices with 6, 8, 10, 14, 20, and 50 sites along the x
and z directions (lengths labelled in the upper right corner), and two sites
along y and w (with periodic boundary conditions). Black curves show the
bulk band edges.

frequency dependence of the LDOS measure Re½Z r , averaged
over surface or bulk sites. To interpret these results, recall that the
impedance measurements probe the response at ﬁxed energy (in
this case, E = 0) of an effective Hamiltonian H(f) that depends
parametrically on the frequency f [Eq. (6)], and matches the
target tight-binding model at f = f0. For m = 0 (Fig. 4b), the
circuit exhibits a strong edge response and suppressed bulk
response at f = f0, consistent with the fact that H(f0) has a
topologically nontrivial gap at E = 0. For f ≠ f0, the effective
Hamiltonian H(f) deviates from the target model (e.g. the positive
and negative hoppings become unequal in magnitude, lifting the
band degeneracy), but remains in Class AI. So long as the gap
remains open, H(f) must possess a topologically nontrivial gap at
E = 0 associated with the same second Chern number. The
signatures of the topological bandgap persist as m is slightly
increased (Fig. 4c); upon further increasing m, the bulk gap closes
and thereafter the surface and bulk LDOS measures exhibit no
notable frequency dependent features (Fig. 4d, e). These
experimental results are in good agreement with simulations
(Fig. 4g–j).
Discussion
We have used electric circuits to implement a 4D lattice hosting a 4D
Quantum Hall phase. This is the ﬁrst experimental demonstration of
a topological lattice with a 4D structure, and of a Class AI topological
insulator. This is also the ﬁrst experimental exploration of a 4DQH
model with nontrivial second Chern number but trivial ﬁrst Chern
numbers. Using impedance measurements, we have demonstrated
that the LDOS on the 3D surface is enhanced in the 4DQH phase,
due to the presence of topological surface states, and that the
enhanced surface response spans the frequency range of the bulk
bandgap. The gap-closing associated with a topological phase transition is clearly observed, despite being shifted by ﬁnite-size effects. In
future work, it is desirable to ﬁnd ways to probe the detailed features
of the 3D surface states, which are predicted to be two robust isolated
Weyl points of the same chirality, a situation that does not occur in
lower-dimensional topological models37. The successful implementation of 4D lattices of very substantial size (144 sites) shows that
electric circuits are an excellent platform for exploring exotic band
topological effects, and a promising alternative to the synthetic
dimensions approach to realising higher-dimensional lattices51.

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

5

## PDF page 7

ARTICLE

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

a

b

c

m=0

d

m=1

e

m=4

m=8

5

〈Re[Zr ]〉 (a.u.)

Experiments

Surface/bulk ratio

6
4
3
2
1
0

2

4

6

8

f

600

600

600

400

400

400

400

200

200

200

200

Surface

0
80

0

Bulk

600

100

g
〈Re[Zr ]〉 (a.u.)

Simulations

Surface/bulk ratio

4
3
2

140

0
80

160

100

h

m=0

6
5

120

120

140

0
80

160

100

i

m=1

120

140

0
80

160

100

j

m=4

120

140

160

140

160

m=8

600

600

600

600

400

400

400

400

200

200

200

200

1
0
0

2

4

6

8

0
80

100

120

140

160

0
80

100

m

120

140

160

0
80

100

120

140

160

0
80

100

120

Frequency (kHz)

Fig. 4 Comparison of bulk and surface contributions to the LDOS. a Ratio of surface to bulk LDOS, measured at f = f0, versus m. b–e Mean values of the
LDOS measure Re½Zr  on surface and bulk sites, versus working frequency f. For these subplots, measurements were only taken over sites in the 2D plane
(y, w) = (1, 0). The reference working frequency f0 (corresponding to E = 0) is indicated by the vertical dotted line. For small m, we observe an elevated
surface LDOS measure over a range of frequencies coincident with a bulk gap. Upon increasing m, the gap closes. f–j The corresponding circuit simulation
results, obtained using the same circuit parameters and with manufacturer-supplied estimates for the capacitor and inductor resistances. The results in
f, and the solid curves and dashes in g–j, assume no disorder in the circuit components. The red and blue areas in g–j indicate the range of impedances
assuming 10% variation in individual capacitances and inductances, over 50 independent disorder realisations.

While this work was being done, we became aware of related
theoretical proposals to use circuits to realise high-dimensional
TIs55,56.
Methods
Circuit implementation and experimental procedure. The implementation of the
LC circuit, so as to map its impedance response to a target Hamiltonian, follows a
design strategy similar to recent works, which targeted different topological
models20–23,26–28. As explained in the main text, positive and negative hoppings in
the tight-binding Hamiltonian are represented by capacitors and inductors
respectively. Deﬁning the complex conductance between sites i and j as Dij = iαHij,
we take α = 2πf0C0 to map the positive nearest neighbour hopping J = 1 to capa0
0
citance C0 = 1 nF, and the long-range
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ hopping J to capacitance C ¼ 2 nF, at f =
f0. Next, setting f 0 ¼ 1=ð2π L0 C 0 Þ  113 kHz maps the negative nearest
neighbour hopping to inductance L0 = 2 mH, and the negative long-range hopping
J″ = −2 to L0 ¼ 1 mH. Each site is connected to ground by additional components
to satisfy Eq. (2); see Supplementary Note 2. The required capacitances are
obtained by connecting 1 nH capacitors (Murata GCM155R71H102KA37D) in
series or parallel, and the inductances are achieved by connecting 1 mH inductors
(Taiyo Yuden LB2518T102K).
The circuit is divided into several printed circuit boards (PCBs), stacked on top
of each other. Each PCB is divided into 6 × 6 = 36 nodes, corresponding to the
dimensions of the 4D lattice in the x–z plane (see Fig. 1c of the main text). Each x–
z lattice plane actually consists of several PCBs stacked with vertical electrical
interconnects, in order to ﬁt all the necessary circuit components.
We measure the impedance between any given node r and the common ground
by applying a 1 V sine wave of frequency f0 on that node, and measuring the
voltage Vr and the current Ir. As stated in Eq. 4, the impedance between node r and
the ground is the rth diagonal term of the inverse of the circuit Laplacian L. Using
Eq. (3), one obtains20,27
Zr ¼

X jψ ðrÞj2
i
n
;
lim
α ϵ!0 n En  E þ iϵ

ð6Þ

where ψn(r) is the n-th energy eigenstate’s amplitude on site r, and En is the
corresponding eigenenergy. Thus, if the impedance measurement is performed at
P
f = f0, then Re½Z r  ¼ ð1=παÞ n δðE  En Þ jψ n ðrÞj2 is equivalent to the lattice’s
LDOS at energy E. With resistances present, the eigenenergies in Eq. (6) acquire an
imaginary part, which has the effect of smoothing out the impedance curves (see
Supplementary Note 3).
Circuit simulations. All circuit simulations are performed with ngspice, a free
software circuit simulator. We assign to each 1 nF capacitor a 10 Ω resistance,
consistent with the resistance in the manufacturer-supplied SPICE model at
our operating frequency. For each 1 mH inductor, we assign a 24 Ω resistance
consistent with the manufacturer-provided data sheet. Each resistance is applied in
series with the corresponding capacitive or inductive element. Other sources of
resistance, such as the PCB interconnects, are much harder to characterise and
6

were thus not accounted for in the circuit simulations. To model the disorder in the
capacitors and inductors, we apply 10% uniformly-distributed disorder to each
capacitance and inductance, consistent with the stated tolerances in their data
sheets. The simulations are performed like the experiments: i.e. sine wave voltage
source is applied to each node, and the steady-state voltage and current are used to
determine the complex impedance.

Data availability
The circuit measurement data that support the ﬁndings of this study are available in DRNTU(data) with the identiﬁer “https://doi.org/10.21979/N9/KXL3TD”57.

Code availability
Ngspice and Python code used for circuit simulation and generating all plots can be
found in DR-NTU(data) with the identiﬁer “https://doi.org/10.21979/N9/KXL3TD”57.

Received: 30 January 2020; Accepted: 3 April 2020;

References
1.

Hasan, M. Z. & Kane, C. L. Colloquium: topological insulators. Rev. Mod.
Phys. 82, 3045–3067 (2010).
2. Qi, X.-L. & Zhang, S.-C. Topological insulators and superconductors. Rev.
Mod. Phys. 83, 1057–1110 (2011).
3. Altland, A. & Zirnbauer, M. R. Nonstandard symmetry classes in mesoscopic
normal-superconducting hybrid structures. Phys. Rev. B 55, 1142–1161 (1997).
4. Kitaev, A. Periodic table for topological insulators and superconductors. AIP
Conference Proceedings 1134, 22 (2009).
5. Schnyder, A. P., Ryu, S., Furusaki, A. & Ludwig, A. W. W. Classiﬁcation of
topological insulators and superconductors in three spatial dimensions. Phys.
Rev. B 78, 195125 (2008).
6. Ryu, S., Schnyder, A. P., Furusaki, A. & Ludwig, A. W. W. Topological
insulators and superconductors: tenfold way and dimensional hierarchy. N. J.
Phys. 12, 065010 (2010).
7. Chiu, C.-K., Teo, J. C. Y., Schnyder, A. P. & Ryu, S. Classiﬁcation of
topological quantum matter with symmetries. Rev. Mod. Phys. 88, 035005
(2016).
8. Klitzing, Kv, Dorda, G. & Pepper, M. New method for high-accuracy
determination of the ﬁne-structure constant based on quantized hall
resistance. Phys. Rev. Lett. 45, 494–497 (1980).
9. Avron, J., Sadun, L., Segert, J. & Simon, B. Topological invariants in fermi
systems with time-reversal invariance. Phys. Rev. Lett. 61, 1329 (1988).
10. Fröhlich, J. & Pedrini, B. New applications of the chiral anomaly. In
Mathematical Physics 2000 (eds Fokas, A., Grigoryan, A., Kibble, T. &
Zegarlinski, B.), 9–47 (Word Scientiﬁc, 2000).

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

## PDF page 8

NATURE COMMUNICATIONS | https://doi.org/10.1038/s41467-020-15940-3

11. Zhang, S.-C. A four-dimensional generalization of the quantum hall effect.
Science 294, 823–828 (2001).
12. Sugawa, S., Salces-Carcoba, F., Perry, A. R., Yue, Y. & Spielman, I. Second
chern number of a quantum-simulated non-abelian yang monopole. Science
360, 1429–1434 (2018).
13. Cooper, N. R., Dalibard, J. & Spielman, I. B. Topological bands for ultracold
atoms. Rev. Mod. Phys. 91, 015005 (2019).
14. Ozawa, T. et al. Topological photonics. Rev. Mod. Phys. 91, 015006 (2019).
15. Yang, Z. et al. Topological acoustics. Phys. Rev. Lett. 114, 114301 (2015).
16. Huber, S. D. Topological mechanics. Nat. Phys. 12, 621–623 (2016).
17. Ningyuan, J., Owens, C., Sommer, A., Schuster, D. & Simon, J. Time- and siteresolved dynamics in a topological circuit. Phys. Rev. X 5, 021031 (2015).
18. Albert, V. V., Glazman, L. I. & Jiang, L. Topological properties of linear circuit
lattices. Phys. Rev. Lett. 114, 173902 (2015).
19. Hadad, Y., Soric, J. C., Khanikaev, A. B. & Alù, A. Self-induced topological
protection in nonlinear circuit arrays. Nat. Electron. 1, 178–182 (2018).
20. Lee, C. H. et al. Topolectrical circuits. Commun. Phys. 1, 39 (2018).
21. Imhof, S. et al. Topolectrical-circuit realization of topological corner modes.
Nat. Phys. 14, 925–929 (2018).
22. Luo, K., Yu, R. & Weng, H. Topological nodal states in circuit lattice. Research
2018, 6793752 (2018).
23. Ezawa, M. Higher-order topological electric circuits and topological corner
resonance on the breathing kagome and pyrochlore lattices. Phys. Rev. B 98,
201402 (2018).
24. Wang, Y., Lang, L.-J., Lee, C. H., Zhang, B. & Chong, Y. D. Topologically
enhanced harmonic generation in a nonlinear transmission line metamaterial.
Nat. Commun. 10, 1102 (2019).
25. Lu, Y. et al. Probing the berry curvature and fermi arcs of a weyl circuit. Phys.
Rev. B 99, 020302 (2019).
26. Serra-Garcia, M., Süsstrunk, R. & Huber, S. D. Observation of quadrupole
transitions and edge mode topology in an lc circuit network. Phys. Rev. B 99,
020304 (2019).
27. Helbig, T. et al. Band structure engineering and reconstruction in electric
circuit networks. Phys. Rev. B 99, 161114 (2019).
28. Hofmann, T., Helbig, T., Lee, C. H., Greiter, M. & Thomale, R. Chiral voltage
propagation and calibration in a topolectrical chern circuit. Phys. Rev. Lett.
122, 247702 (2019).
29. Thouless, D. Quantization of particle transport. Phys. Rev. B 27, 6083 (1983).
30. Kraus, Y. E., Ringel, Z. & Zilberberg, O. Four-dimensional quantum hall effect
in a two-dimensional quasicrystal. Phys. Rev. Lett. 111, 226401 (2013).
31. Petrides, I., Price, H. M. & Zilberberg, O. Six-dimensional quantum hall
effect and three-dimensional topological pumps. Phys. Rev. B 98, 125431
(2018).
32. Lee, C. H., Wang, Y., Chen, Y. & Zhang, X. Electromagnetic response of
quantum hall systems in dimensions ﬁve and six and beyond. Phys. Rev. B 98,
094434 (2018).
33. Jukić, D. & Buljan, H. Four-dimensional photonic lattices and discrete
tesseract solitons. Phys. Rev. A 87, 013814 (2013).
34. Ezawa, M. Electric circuits for non-hermitian chern insulators. Phys. Rev. B
100, 081401 (2019).
35. Li, L., Lee, C. H. & Gong, J. Emergence and full 3d-imaging of nodal boundary
seifert surfaces in 4d topological matter. Commun. Phys. 2, 135 (2019).
36. Thouless, D. J., Kohmoto, M., Nightingale, M. P. & denNijs, M. Quantized hall
conductance in a two-dimensional periodic potential. Phys. Rev. Lett. 49,
405–408 (1982).
37. Price, H. M. Four-dimensional topological lattices without gauge ﬁelds.
Preprint at https://arxiv.org/abs/1806.05263 (2020).
38. Boada, O., Celi, A., Latorre, J. I. & Lewenstein, M. Quantum simulation of an
extra dimension. Phys. Rev. Lett. 108, 133001 (2012).
39. Celi, A. et al. Synthetic gauge ﬁelds in synthetic dimensions. Phys. Rev. Lett.
112, 043001 (2014).
40. Price, H. M., Zilberberg, O., Ozawa, T., Carusotto, I. & Goldman, N. Fourdimensional quantum hall effect with ultracold atoms. Phys. Rev. Lett. 115,
195303 (2015).
41. Mancini, M. et al. Observation of chiral edge states with neutral fermions in
synthetic hall ribbons. Science 349, 1510–1513 (2015).
42. Stuhl, B. K., Lu, H.-I., Aycock, L. M., Genkina, D. & Spielman, I. B. Visualizing
edge states with an atomic bose gas in the quantum hall regime. Science 349,
1514–1518 (2015).
43. Ozawa, T., Price, H. M., Goldman, N., Zilberberg, O. & Carusotto, I. Synthetic
dimensions in integrated photonics: from optical isolation to fourdimensional quantum hall physics. Phys. Rev. A 93, 043827 (2016).
44. Price, H. M., Zilberberg, O., Ozawa, T., Carusotto, I. & Goldman, N.
Measurement of chern numbers through center-of-mass responses. Phys. Rev.
B 93, 245113 (2016).
45. Yuan, L., Shi, Y. & Fan, S. Photonic gauge potential in a system with a
synthetic frequency dimension. Opt. Lett. 41, 741–744 (2016).

ARTICLE

46. Ozawa, T. & Carusotto, I. Synthetic dimensions with magnetic ﬁelds and local
interactions in photonic lattices. Phys. Rev. Lett. 118, 013601 (2017).
47. Price, H. M., Ozawa, T. & Goldman, N. Synthetic dimensions for cold atoms
from shaking a harmonic trap. Phys. Rev. A 95, 023607 (2017).
48. Yuan, L., Lin, Q., Xiao, M. & Fan, S. Synthetic dimension in photonics. Optica
5, 1396–1405 (2018).
49. Price, H. M., Ozawa, T. & Schomerus, H. Synthetic dimensions and
topological chiral currents in mesoscopic rings. Preprint at https://arxiv.org/
abs/1907.04231 (2020).
50. Lustig, E. et al. Photonic topological insulator in synthetic dimensions. Nature
567, 356–360 (2019).
51. Ozawa, T. & Price, H. M. Topological quantum matter in synthetic
dimensions. Nat. Rev. Phys. 1, 349–357 (2019).
52. Dutt, A. et al. A single photonic cavity with two independent physical
synthetic dimensions. Science 367, 59–64 (2020).
53. Lohse, M., Schweizer, C., Price, H. M., Zilberberg, O. & Bloch, I. Exploring 4d
quantum hall physics with a 2d topological charge pump. Nature 553, 55–58
(2018).
54. Zilberberg, O. et al. Photonic topological boundary pumping as a probe of 4d
quantum hall physics. Nature 553, 59–62 (2018).
55. Ezawa, M. Electric circuit simulations of nth -chern-number insulators in 2n
-dimensional space and their non-hermitian generalizations for arbitrary n.
Phys. Rev. B 100, 075423 (2019).
56. Yu, R., Zhao, Y. X. & Schnyder, A. P. A genuine realization of the spinless 4d
topological insulator by electric circuits. Preprint at https://arxiv.org/abs/
1906.00883 https://academic.oup.com/nsr/advance-article/doi/10.1093/nsr/
nwaa065/5820240 (2020).
57. Wang, Y. Replication data for: circuit implementation of a four-dimensional
topological insulator. https://doi.org/10.21979/N9/KXL3TD (2020).

Acknowledgements
We are grateful to C.H. Lee and T. Ozawa for helpful discussions. This work was supported
by the Singapore MOE Academic Research Fund Tier 3 Grant MOE2016-T3-1-006, Tier 1
Grants RG187/18 and RG174/16(S), and Tier 2 Grant MOE2018-T2-1-022(S). H.M.P. is
supported by the Royal Society via grants UF160112, RGF/EA/180121 and RGF/R1/180071.

Author contributions
Y.W. designed and fabricated the samples, and performed the experiments and simulations. B.Z. and Y.C. supervised the project. Y.W., H.M.P., B.Z. and Y.C. contributed to
the theoretical analysis and the writing of the paper.

Competing interest
The authors declare no competing interests.

Additional information
Supplementary information is available for this paper at https://doi.org/10.1038/s41467020-15940-3.
Correspondence and requests for materials should be addressed to B.Z. or Y.D.C.
Peer review information Nature Communications thanks Andrea Alu and Ronny
Thomale for their contribution to the peer review of this work. Peer reviewer reports are
available.
Reprints and permission information is available at http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in
published maps and institutional afﬁliations.

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative
Commons license, and indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not included in the
article’s Creative Commons license and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this license, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2020

NATURE COMMUNICATIONS | (2020)11:2356 | https://doi.org/10.1038/s41467-020-15940-3 | www.nature.com/naturecommunications

7
