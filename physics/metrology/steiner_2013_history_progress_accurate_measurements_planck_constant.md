Source: see manifest row of the PDF
PDF sha256: 3ea8453929bbed3f2c27d5cea5b3bd46fbf97c42467c07356036d9fc80974285
License: US-gov-work-public-domain
Language: eng
Fidelity: machine (failed: characters)

# Transcription of steiner_2013_history_progress_accurate_measurements_planck_constant.pdf

Transcription of `steiner_2013_history_progress_accurate_measurements_planck_constant.pdf` in this directory, 47 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-47 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Reports on Progress in Physics

Related content

REVIEW ARTICLE

History and progress on accurate measurements
of the Planck constant

- Watt balance experiments for the
determination of the Planck constant and
the redefinition of the kilogram
M Stock

To cite this article: Richard Steiner 2013 Rep. Prog. Phys. 76 016101

- Towards an electronic kilogram
Richard L Steiner, Edwin R Williams,
David B Newell et al.

View the article online for updates and enhancements.

- Progress on accurate measurement of the
Planck constant: Watt balance and
counting atoms *
Li Shi-Song, Zhang Zhong-Hua, Zhao Wei
et al.

Recent citations
- Preliminary Planck constant
measurements via UME oscillating magnet
Kibble balance
H Ahmedov et al
- Analysis of balance beam deformation in
the inertial mass measurement experiment
Zhuang Fu et al
- Two simple modifications to improve the
magnetic field profile in radial magnetic
systems
Shisong Li and Stephan Schlamminger

This content was downloaded from IP address 115.254.96.135 on 14/07/2018 at 06:54

## PDF page 2

IOP PUBLISHING

REPORTS ON PROGRESS IN PHYSICS

Rep. Prog. Phys. 76 (2013) 016101 (46pp)

doi:10.1088/0034-4885/76/1/016101

History and progress on accurate
measurements of the Planck constant
Richard Steiner1
National Institute of Standards and Technology, NIST Gaithersburg, MD 20899, USA

Received 15 June 2012, in final form 9 October 2012
Published 18 December 2012
Online at stacks.iop.org/RoPP/76/016101
Abstract
The measurement of the Planck constant, h, is entering a new phase. The CODATA 2010
recommended value is 6.626 069 57 × 10−34 J s, but it has been a long road, and the trip is not
over yet. Since its discovery as a fundamental physical constant to explain various effects in
quantum theory, h has become especially important in defining standards for electrical
measurements and soon, for mass determination. Measuring h in the International System of
Units (SI) started as experimental attempts merely to prove its existence. Many decades passed
while newer experiments measured physical effects that were the influence of h combined with
other physical constants: elementary charge, e, and the Avogadro constant, NA . As experimental
techniques improved, the precision of the value of h expanded. When the Josephson and quantum
Hall theories led to new electronic devices, and a hundred year old experiment, the absolute
ampere, was altered into a watt balance, h not only became vital in definitions for the volt and
ohm units, but suddenly it could be measured directly and even more accurately. Finally, as
measurement uncertainties now approach a few parts in 108 from the watt balance experiments
and Avogadro determinations, its importance has been linked to a proposed redefinition of a
kilogram unit of mass.
The path to higher accuracy in measuring the value of h was not always an example of
continuous progress. Since new measurements periodically led to changes in its accepted value
and the corresponding SI units, it is helpful to see why there were bumps in the road and where
the different branch lines of research joined in the effort. Recalling the bumps along this road will
hopefully avoid their repetition in the upcoming SI redefinition debates. This paper begins with a
brief history of the methods to measure a combination of fundamental constants, thus indirectly
obtaining the Planck constant. The historical path is followed in the section describing how the
improved techniques and discoveries in quantum mechanics steadily reduced the uncertainty of h.
The central part of this review describes the technical details of the watt balance technique, which
is a combination of the mechanical and electronic measurements that now determine h as a direct
result, i.e. not requiring measured values of additional fundamental constants. The first technical
section describes the basics and some of the common details of many watt balance designs. Next
is a review of the ongoing advances at the (currently) seven national metrology institutions where
these experiments are pursued. A final summary of the recent h determinations of the last two
decades shows how history keeps repeating itself; there is again a question of whether there is a
shift in the newest results, albeit at uncertainties that are many orders of magnitude less than the
original experiments. The conclusion is that there is room for further development to resolve
these differences and find new ideas for a watt balance system with a more universal application.
Since the next generation of watt balance experiments are expected to become kilogram
realization standards, the historical record suggests that there is yet a need for proof that Planck
constant results are finally reproducible at an acceptable uncertainty.
(Some figures may appear in colour only in the online journal)
This article was invited by George T Gillies.
1 Quantum Measurement Division, Physical Measurement Laboratory, US Department of Commerce. Official
contribution of the National Institute of Standards and Technology, not subject to copyright in the United States.

0034-4885/13/016101+46$88.00

1

© 2013 IOP Publishing Ltd

Printed in the UK & the USA

## PDF page 3

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Contents
1. Introduction
2. Historical background
2.1. The discovery
2.2. Results for h/e
2.3. Compiling h values—finding a discrepancy
3. Measurements in SI units and new discoveries
3.1. Josephson effect: a voltage standard
3.2. Absolute volt balance: the link to SI
3.3. The absolute ampere balance
3.4. The misinterpreted volt determinations
3.5. Quantum Hall effect: a resistance standard
3.6. Avogadro constant
3.7. The 1990 electrical units adjustment
4. Modern direct measurements of h
4.1. A direct link to h via quantum electronics
4.2. Superconducting magnetic levitation
4.3. The Joule balance
4.4. The watt balance
4.5. Deriving h in measurements using SI units
4.6. Defining kilogram mass in terms of h
5. The watt balance systems—common details
5.1. Common traits
5.2. The magnetic field
5.3. Alignment issues
5.4. Force and current mode

5.5. Voltage and velocity mode
23
5.6. Magnetic profile analysis
24
6. Individual experiments by NMI
26
6.1. NPL Great Britain 1980s—the first direct h value 26
6.2. NBS 1980s—electromagnetic solenoid,
a different approach
27
6.3. 1988 h results—NPL, NBS
27
6.4. The next generation experiments at NIST and
NPL
28
6.5. The worldwide spread of watt balance
experiments
30
7. The most recent h results: not quite a consensus
36
7.1. System reports
36
7.2. NIST 2005 and 2007
36
7.3. NPL 2007 and update 2010
37
7.4. METAS 2011
38
7.5. Avogadro 2004 and 2010
38
7.6. NRC Canada–reviving the NPL apparatus
39
7.7. National laboratory updates
39
8. Concluding remarks
40
8.1. A data summary
40
8.2. The future of h and IPK
40
8.3. An impressive history
41
Acknowledgments
42
References
42

3
4
4
4
5
6
6
6
7
8
9
10
10
11
11
11
12
13
15
15
17
17
17
18
19

Abbreviations

MSL

Laboratory and Committee names

NBS
NIM
NIST

BIPM
BNM
CCEM
CCM
CODATA
CSIRO
CPEM
ETF
KRISS
LCIE
LNE
METAS
MIKES

Bureau International des Poids et Mesures,
Paris
Bureau National de Métrologie, France
Consultative Committee for Electricity and
Magnetism
Consultative Committee for Mass and Related
Quantities
Committee on Data for Science and
Technology
Commonwealth Scientific and Industrial
Research Organisation, Australia
Conference on Precision Electromagnetic
Measurements
Facility for Electrical Engineering, University
of Zagreb, Croatia
Korea Research Institute of Standards and
Science
Laboratoire Central des Industries
Electricques, France
Laboratoire National de M’etrologie et
d’Essais, France
Swiss Federal Office of Metrology and
Accreditation, Switzerland
Center for Metrology and Accreditation,
Finland

NMI
NMIJ
NPL
NRC-INMS
OFFMET
PTB

Measurement Standards Laboratory, New
Zealand
National Bureau of Standards, United States
National Institute of Metrology, China
National Institute of Standards and
Technology, United States
National Metrology Institute, generic term
National Metrology Institute of Japan, Japan
National Physical Laboratory, Great Britain
National Research Council, Canada
Federal Office of Metrology, Switzerland
Physikalisch-Technische Bundesanstalt,
Germany

Technical Acronyms
ac
CM
dc
EMC
IPK
PZT
QHE
SI
SQUID
XRCD
2

alternating current
center of mass
direct current
electromagnetic center
International Prototype of the Kilogram
piezoelectric translator
quantum Hall effect
International System of Units
superconducting quantum interference device
X-ray crystal density, Avogadro program

## PDF page 4

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

of the 1970s and 1980s, especially in the volt, followed by
the subsequent adjustments to the volt and ohm in the SI
in 1990. Those controversies and adjustments are echoing
now in the latest h result discrepancies from the watt balance
measurements of the Planck constant and the world-wide effort
to measure the Avogadro constant NA . More research will
hopefully resolve any differences. Further, as the volt and
ohm are linked to h, the proposed SI redefinition concerning
the kilogram mass unit will certainly be affected by the results
of the ‘final measurements’ of h. Reading this history of the
occasional miscues in defining the SI units might also convey
an appreciation for the scientific and enduring clarity that
will occur after SI redefinition in terms of the fundamental
constants.
Watt balance systems are now the best methods used to
measure h. The historical record provides an understanding of
why present-day adaptations and designs on the drawing board
inherit some of the procedural conveniences or restrictions
of older experiments. New watt balance h and Avogadro
NA results are often more newsworthy of late because of
the kilogram redefinition, rather than in any new technical
achievement in resolving the 7th or 8th digit of either constant.
These are both complicated experiments. In reality they are a
combination of several individual measurement systems. The
bulk of this review will concentrate on the details specific to
the watt balance technique. Variations on the basic technique
are starting to proliferate. A joule balance technique just under
development gets a mention, as it is also based in part on the
watt balance’s precursor: the ampere balance. It is generally
accepted that there will be several watt balances operating
around the world, while there will be only one world-wide
consortium to make the Avogadro measurement, which has
its own excellent review paper. Watt balance techniques are
rapidly evolving, so even an epic tome covering every little
detail of all the watt balance experiments along with each
peripheral reference measurement system would be obsolete
upon printing. This review attempts to reduce 30 years of
watt balance development by the national metrology institutes
(NMIs) to a summary of the commonalities, a highlight of the
main differences and a rough timeline for each laboratory’s
efforts.
The watt balance technical areas covered are: source
magnets, methods of moving an induction coil, means of
measuring the electromagnetic force against the gravitational
force, misalignment errors and a summary of signal and
data analysis. Various and sometimes extensive environment
controls, such as anti-vibration, temperature control, RF
screening, etc., are significant to the work efforts, but the
technical efforts are not unique to watt balance operation,
so they are mentioned only in passing. Although each of
the several peripheral systems is crucial to the measurement,
these systems are not limiting factors to the overall uncertainty
contributions table. Interested readers are referred to review
papers on the Josephson voltage, quantum Hall resistance and
absolute gravity measurement systems. Precision frequency
standards and laser interferometry are necessarily integrated
for real time operation, but these are so commonly used in many
experiments that they are considered here as peripheral systems

1. Introduction
The Planck constant, symbolized as h, is a fundamental
physical constant that is important in quantum mechanics,
statistical mechanics, electronics and almost assuredly soon,
mass metrology. The constant started as a hypothesis
just over 100 years ago to mathematically explain how
light must have a discreteness that was not experimentally
observed. Even theoretical constants have a real value, so
numerical measurements of h within the International System
of Units (SI) [Systéme International d’Unités] were quickly
undertaken. The SI units were originally and solely based upon
artifact standards. Working with these standards sometimes
added a barrier to measuring h more precisely in SI terms.
Voltage measurements have always been very important in
determinations of h, especially in the early history of the
efforts. Eventually, length and frequency units, along with
a fundamental constant, c, the speed of light, became essential
in the measurement. Finally resistance units were needed, after
new quantum theoretical discoveries and new systems relating
to the volt and ohm intimately involved them both in today’s
best techniques. The histories of volt and ohm determinations
have been reviewed elsewhere.
In all but mass, the last of the SI artifact standards,
electronic instruments or devices already measure reference
units in terms of fundamental physical constants. The accuracy
of the Planck constant has now improved to disagreements in
the 7th digit with stated uncertainties in the 8th digit, so it is
part of the proposed redefinition of the kilogram mass unit.
Ongoing experiments measuring the value of h using mass as
a variable, by reversing the calculations, will soon overcome
this last artifact barrier to long term stability in the units. The
proposed redefinition will formalize mass as a function of
measurements against these other electronic standards. Since
mass will be defined by h and the speed of light, obtaining
a highly accurate value of the Planck constant is driving the
interest in this topic.
The path to an accurate SI value of h has not followed
a straight path of adding more digits to refine a previously
established coarser value. Measuring fundamental constants
has long had a close relation to standard references with SI
values and so these experiments have always pushed precision
beyond existing limits. The history may seem slow, since
technical improvements tend to occur leisurely over decades,
but when radically new methods or physics discoveries are
made, there are sudden jumps in the precision, sometimes
accompanied with shifts in the value. This paper will review
some of the early attempts to measure h because recurrences of
unexpected transitions from ‘accepted’ values to newer results
are more than interesting. Hopefully these lessons will provide
some wariness in leaping in these modern times to adopt a
‘final’ value for the redefinition.
Older papers have more detail on the historical
background from the late 1800s to about 1990, while more
recent review papers restrict themselves to modern technical
advances. An abbreviated review of the history here is also
meant to introduce younger researchers, and those outside
the field, to the electrical unit dissemination controversies
3

## PDF page 5

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

and, except in one case, are not specifically designed for the
watt balance. Similarly, the traceability path and calibration
of reference masses are not mentioned except to illustrate the
apparent mass changes of the International Prototype Kilogram
(IPK) copies, changes that are the major justification for the
measurement of h and the subsequent redefinition of the SI.
Concluding remarks summarize what will be by definition
the last debate on h results, although the same arguments will
continue in measuring mass references. As the speed of light
is now an assigned constant, ultimately and probably just a few
years from this writing, h will become a fundamental physical
constant with a fixed value, based on agreements between the
Avogadro effort and watt balance experiments. Watt balance
measurements of mass will then become the realization of the
kilogram unit. The practical details concerning any future
effort to maintain and disseminate the SI kilogram standard are
still under intense discussion; they are not commented upon
here. However, watt balance mass calibration systems, perhaps
soon to be called ‘electronic kilogram systems,’ will have the
same measurement concerns as in the past, so in remembering
the history and highlighting the technical details, hopefully this
paper will be an aid to future electronic mass metrologists.

Figure 1. Photoelectric effect. Photon energy knocks out electrons,
which are inhibited from traversing the gap by a voltage on the
opposite electrode.

These experiments were the earliest, although indirect,
determination of h. A value for e must be measured
independently to find h. As mentioned in the introduction,
voltage units have been historically involved in and are still
intrinsic in measuring h.
2.2. Results for h/e
The earliest reported photoelectric experiment results, those
of Hughes [5] and Richardson and Compton in 1912 [6],
were explorations into the wave versus particle nature of the
effect. They had large uncertainties of about 10% for the
values of h/e. The positive success of these early efforts
to test Einstein’s hypothesis [7] led to the belief that if the
same experimental technique was improved, it would provide
a precise measurement for the value of h. Early on, Millikan
pursued this experimental line of inquiry; in 1913 [8], he
went further and compiled his and other researchers’ data,
using various physics relationships to infer the values for
several constants, including h, e, the Avogadro constant NA
and the Boltzmann constant. For one calculation he used a
formula for the Stefan–Boltzmann constant and inserted the
radiation constant values in [9]. This inferred a value h =
6.620×10−27 erg s (10−34 J s in SI units) (a value coincidentally
within 0.1% of the modern value), presuming about 0.4%
uncertainty. The 1913 paper was the initial effort to assemble
physical constants data, eventually becoming the Committee
on Data for Science and Technology (CODATA) work of today.
Millikan’s interest and early design of a better photoelectric
experiment led to his conclusion (italics his), ‘Planck’s ‘h’
appears then to stand out in connection with photo-electric
measurements more sharply, more exactly and more certainly
than in connection with any other type of measurements thus
far made.’ Millikan’s [10] experiment resulted in a value
for h = 6.57 × 10−34 J s with a stated uncertainty of 0.5%,
obtaining an h value by combining h/e measurement with his
own evaluation of e from the famous oil drop experiment.
Several historical methods for measuring h/e and their
development were described in 1985 by Petley [11]. The
best of these methods was improved and much later became
significant in another physical constant determination, that of
NA . This new method used x-rays emitted from Coolidge tubes
[12], which produced strong x-rays from high voltages applied

2. Historical background
2.1. The discovery
The constant h originated in the year 1900 as a theoretical
concept invented, or perhaps more properly, discovered
by Max Planck [1–3].
Planck postulated that energy
is quantized, to explain why black body radiation has a
finite energy spectrum, correctly as quantum theory later
discovered. Another experiment with unexplained results
was the photoelectric effect, where electrons are ejected
from a metal surface under bombardment by electromagnetic
radiation. The unusual aspect of the effect was that the
electrons had the same energy regardless of the light intensity,
but the electron energy did change with the light’s color
or frequency. Five years after Planck’s paper, Einstein
subsequently guessed that the photoelectric effect was due to
the energy being discrete, or quantized [4]. His mathematical
relation described the discrete photon energy, E, absorbed by
or emitted from an atom as proportional by a constant, h, to
the frequency, f ,
E = hf.
(1)
Figure 1 shows a schematic experiment to investigate the
photoelectric effect. Inside a vacuum chamber, light of
different frequencies ejects electrons from a metal plate. The
energy of the electrons is found by increasing the voltage, V ,
until there is no more measured current, A. The impinging
electromagnetic light energy must exceed a work function, W ,
a characteristic of the metal. Graphing the current-stopping
voltage against the impinging light’s frequency produces a line
where the slope is the ratio h/e, where e is the elementary
charge. Equation (2) describes the relation in terms of energy
or work,
eV = hf − W.
(2)
4

## PDF page 6

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

to hot cathodes: x-ray frequency depended upon the applied
voltage, V . Initially the technique relied upon measuring the
upper frequency of the continuous x-ray emission spectrum.
The advantage of this technique over the photoelectric effect
is that the photon energy is independent of the material, i.e.
no work function is involved. Duane and Hunt [13] used the
relation eV = hf = hc/λ, where the energy of the electrons
at an applied voltage, eV, equals the energy of the x-rays with
a wavelength of λ. The wavelength was measured from Bragg
diffraction and the governing equation of λ = 2a sin θ , where
a is a grating spacing and θ the diffraction angle. The first
experiments used etched lines of a known spacing a to deflect
the x-rays, then later the lattice spacing of regularly spaced
crystal planes. As with e, a value for the speed of light, c, was
borrowed from a different experiment’s result. When using
crystal lattice spacing, this method intertwined determinations
of h/e with measurements of NA . Reviews of this early work
on measuring NA by Deslattes in 1980 [14] and Becker in
2001 [15] describe how the x-ray method became important
after independent approaches to find the wavelength of x-rays
became available from a thesis by Bäcklin in 1928 [16]. From
these early experiments, the relation for e/ h is
h/e = λmin V /c.

Figure 2. A graph of early historical values for h, relative to the
modern value (solid line). Error bars indicate relative uncertainty.
The dashed line shows generally decreasing relative uncertainties
(right axis).

However, this treatment of independently derived results
is interesting because the conclusion that the combined
uncertainty could be better than the individual uncertainties
was not agreeable to all. The question drove further research
and a new series of experimental results followed. Birge in
1929 [19] accumulated the best available data at the time to
evaluate values for h and many other fundamental physical
constants. He remarked that the uncertainty of the previous
h values derived from h/e determinations did not include an
uncertainty for the value of e. Discussions led to changes
in handling the uncertainties reported with results and the
statistics used to evaluate results from multiple sources. This
new care for analyzing independent data has now stood for
many decades, but even so, it is not always easy to exercise
caution when new experiments obtain values with excitingly
improved uncertainties, as later reports will show. Sometimes
it can take a long time to find the ‘right’ conclusion.
Birge in 1932 [20] commented on the increasing
inconsistencies between the h/e ratio measurements and other
derivations of the constants that were dependent upon and
limited by the uncertainty in the measurement of e. It is
beyond the scope of this paper to record the evolution over the
next decade of the other ratio experiments providing inferred
values for h. Jumping ahead, Birge in 1945 [21] concluded
that the oil drop method of measuring e was hampered by
inaccurate determinations of the air viscosity correction. A
reader will find an interesting discussion on the e problem
in the constants evaluation by Birge [22]. (There are other
examples of the difficulties in obtaining ever more accurate
values for the constants: a listing of the historical values of
several fundamental constants in [23] shows that historical
determinations wobble around the modern values for many
of the constants.)
With the discrepancy in h now ‘solved’, a series of
improvements to the x-ray experimental methods let Bearden
and others in 1950 [24] and 1951 [25] obtain yet higher
resolution for the values of h/e. A fundamental constants
evaluation by Bearden and Watts in 1951 [26] reported h =
6.623 63(16) × 10−34 J s, with the uncertainty of 24 parts in

(3)

λmin is the wavelength equivalent of the maximum f . The
method was limited by several procedures. The measurement
had a tendency to smooth out the lower cutoff of the xray wavelength. The referenced papers specifically describe
tracing the source tube voltage back to the Weston standard
cells as a laboratory standard reference. These lab standard
references were a step removed from SI volts, with the
traceability becoming a critical importance that will arise in
a later discussion. There was added uncertainty in measuring
the crystal lattice spacing of the diffracting materials in atomic
units and then converting into SI units.
2.3. Compiling h values—finding a discrepancy
The reported data on seven ways to infer h was accumulated
in [17]. Birge found that the x-ray method of Blake and Duane
[18] had the lowest uncertainty of about 0.17%. The multiple
results had a least square mean value for h = 6.5543(25) ×
10−34 J s and were consistent within this 0.04% uncertainty.
(The combined uncertainty of the result is expressed as the
numbers in parentheses, applied to the last few digits.) Several
assumptions were made in arguing that this uncertainty was
appropriate, including using a relation between h and e derived
from a theory of rational units. This theory proved to be
more numerology than physics, and was later abandoned. The
main argument was somewhat circular; the uniformity of the
experimental values verified the experiments. The analysis
caused a very sudden drop in the published uncertainty for
h, far smaller than the individual uncertainties implied. This
curious result is shown as the third point on the graph in figure 2.
This value was about 1% below the modern value, well outside
the combined uncertainty statement. Of course, this was only
revealed as a discrepancy at a later time.
5

## PDF page 7

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

the absolute volt measurements (discussed in the next section)
otherwise used to determine the voltage of the Weston cells.
The next step in the research was to determine a precise value
of h/2e relative to the SI. With a better evaluation of this ratio,
the changeover from artifact voltage laboratory standards to
electronic standards would mark the beginning of quantum
electrical metrology.
This determination of h/2e in SI units coincided with
a second controversy over the h value, preventing a quick
adoption of the Josephson device as a voltage standard. Similar
debates have occurred in other areas when changing from a
common artifact, a chemical formulation, or a nature-based
standard over to a newer representation. It is occurring
again with the mass redefinition. Even now, when new
quantum-based devices and electronic instruments overtake
the world’s reliance upon trusted artifact standards and long
established procedures, change can be awkward and resisted.
The independent methods to determine precise values for h,
e and h/e were not nearly as precise as the comparisons
between Weston cells and Josephson junctions for h/2e, so
there was ample incentive for some kind of change. It is
useful to note this particular voltage controversy, since it
presaged some of the present issues in comparing watt balance
results, national standard mass references and the drive for
international consistency in changing from the kilogram mass
unit artifact definition to an electronic definition based on
fundamental constants.
Before getting ahead of the story, it is necessary to
introduce two experiments that were historically linked to the
determination of the SI volt. These are the volt balance, or
electrometer, and the current balance, or absolute ampere.
Invented at about the same time in the 1830s, development
continued for over 160 years. The following sections briefly
summarize their operation.

106 . This was much closer to the modern value of h, only
a bit on the low side. With data accumulated up to 1963
in [27], the inferred value from the various indirect methods
was h = 6.625 59(16) × 10−34 J s. The uncertainty seemed to
be stuck at 24 parts in 106 .
There was hope in early 1962 that a discovery announced
in [28] and in [29] would lead to a new technique, not dependent
upon the x-ray frequency and atomic lattice measurement.
Working in parallel, the two groups discovered magnetic flux
quantization in superconductors, φo , reporting a dependence
φo = hc/(2e) in Gaussian CGS units; more familiarly, in
SI units φo = h/(2e). While the uncertainty of h had
decreased for 60 years, it had started leveling off. For a
short time, this new physical phenomenon certainly offered a
new technique for finding h/2e, perhaps with better precision
to improve on the inferred evaluations of h. However, the
electronic metrology world would soon see the first of two
new discoveries that would ultimately improve the uncertainty
of h by three orders of magnitude.

3. Measurements in SI units and new discoveries
3.1. Josephson effect: a voltage standard
A big jump in voltage measurement precision and a significant
improvement in the stability of the national volt unit
followed the discovery of the Josephson effect in 1962
[30].
A Josephson junction is a connection between
two superconductors, where the normal coherence of the
quantum wavelength in the superconductor is weakened by
a restriction or a thin resistive layer. When irradiated by
electromagnetic waves (usually microwave frequencies or
above) at a frequency, f , constant voltage steps, V , appear
across the junction as the current increases along the I –V
curve, steps of integer quantum number, n, and the relation
V = nf (h/2e).

3.2. Absolute volt balance: the link to SI

(4)

All the Planck constant determinations discussed so far needed
voltages that were traceable to the SI. One method to determine
voltage in SI units used the plate electrometer invented by Sir
William Snow Harris in 1834 [33] and improved upon with
the addition of a guarded ring by Sir William Thompson,
Lord Kelvin, in 1868 [34]. The Kelvin-type electrometer
apparatus is schematically shown in figure 3. A modern
proposal adopts this technique to determine the absolute volt
and appears in [35], pairing the electrostatic balance with
the impedance standard of a Thomson–Lampard calculable
capacitor [36] to trace the balance capacitance to SI units. The
equation describing the electrostatic measurement comes from
the electrical energy in a charged capacitor. A gravitational
force on a test mass, mg, is balanced by the electrical force
of the differential capacitance of two surfaces separated by a
distance, z, charged to a voltage, V ,
(
)
dz 1/2
V = 2mg
.
(5)
dC

The ratio h/2e is familiar as the magnetic flux quantum. This
new discovery led to about 10 years of intense testing for any
unforeseen dependences in the effect, which in turn advanced
the Josephson device fabrication. New ratio measurement
techniques with resistive dividers allowed precise comparisons
of the few millivolts generated by a Josephson junction to
the 1.018 V of a Weston standard voltage cell. Weston cells
were the laboratory flywheel unit representation for voltage.
A review of some of this research can be found in the work
by Pöpel [31] and one focusing on the National Bureau of
Standards (NBS) work in [32].
Josephson device fabrication, microwave generator
stability and frequency measurement, and voltage metrology
improved quickly to the point where the national laboratories
found it easy and reliable to use the Josephson effect to generate
known voltages. Current-biased devices with one or two
Josephson junctions could generate a voltage step at up to
5 or 10 mV with n numbers of several hundred, a width of
a few microamps, and typical microwave drive frequencies
of 10 GHz. Though comparing this small voltage with the
1.018 V of Weston cells was not easy, it was far easier than

The LCIE built such an electrostatic balance, reported by
Elnékavé and Fau in 1983 [37]. An alternative design measures
6

## PDF page 8

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

equates with the potential energy in raising a mass of Hg in
gravity. The variables are reduced to measurements of the
height of the electrode above the surface, d, the raised height
of the Hg, z, and the voltage, V . The measurement is reduced
to interferometry. Various other properties, such as the density
of mercury, and corrections for stray fields around the electrode
gap are characterized separately. The voltage equation is
V = (2ρg/ε)1/2 dz1/2 ,

(6)

where ρ is the Hg density, g is the acceleration of gravity and
ε is the permittivity of the electrode gap.
3.3. The absolute ampere balance
The second of the electrical standards experiments was the
current balance, or absolute ampere. The ampere is one of
the base SI units. Recognized since 1893, a definition within
the SI became official in 1948: ‘The ampere is that constant
current which, if maintained in two straight parallel conductors
of infinite length, of negligible circular cross-section, and
placed 1 m apart in a vacuum, would produce between these
conductors a force equal to 2 × 10−7 Newton per meter of
length’ [44]. The seemingly unusual amount of force of
2 dynes at 1 cm arises in converting from the older CGS system
(the metric system of centimeter, gram, second) to SI units.
The SI implies that the permeability of free space, µ0 , is equal
to 4π × 10−7 H m−1 . In many text books showing standard
electromagnetic equations, a conversion factor of µ0 /4π for
the magnetic units to conform with SI units is often ignored.
From the mid-19th century, the current balance provided
the link from the mechanical metric units to the volt and
ohm, continuing through most of the 20th century to establish
the SI relationships. Once again, Lord Kelvin enhanced
previous measurement methods of current-induced magnetic
force. Its early history, covering improvements by Lord
Rayleigh, Heydweiller and others, is reviewed in a paper on
the NPL ampere efforts in [45].
The ampere balance has a special place in the jigsawpuzzle-history of the Planck constant. The next generational
jump in the precision measurement of h began with the
framework built upon a long history of configurations based on
the ampere measurements at the NBS and the NPL. Different
coil configurations were used at the beginning of the 1900s
to create a torque between electromagnet coils by Guthe [46]
and Rosa [47]. One of the first improvements on the original
design used a pair of induction coils in a fixed position arranged
vertically over one another. Centered between the two was a
smaller movable coil, as in figure 5. This geometry had the
advantage of allowing the center coil to move to a position
where the vertical force was a maximum and also varied
at a minimum rate over small displacements. The ampere
measurements at the NBS reported by Rosa in 1912 [48]
used this new design; a photo of that system is shown in
figure 6. Further refinements continued at the NBS, mainly
in more careful coil winding, by Curtis and Curtis [49], then
with Driscoll and Cutkosky [50] incorporating a Pellat current
balance. These versions of the experiment had carefully wound
electromagnetic induction coils, where the dimensions were
measured as precisely as possible, for the calculation of the

Figure 3. Absolute voltage balance diagram.

Figure 4. Absolute volt electrometer diagram, with a Hg pool
instead of capacitor plates.

the change of energy in a vertically moving electrode situated
within a fixed surface, as proposed in [38]. The equation is
similar to equation (5), instead with difference measurements
of z and C from the positional change. This became
the preferred design at various laboratories, with the most
intense work reported by the PTB in Germany in [39] and
the ETF in Croatia in [40, 41]. The major drawback to this
type of experiment came from using large, heavy electrodes to
supply kilovolts of electrical potential. It could only balance
small mass references of about a gram, hindered by the large
inertial mass of the electrodes. Scaling from the extreme
experimental operating values for voltage and mass references
to SI standards, and tracing across the capacitance chain
back to the calculable capacitance standard, contributed large
uncertainties. The high voltages also make the experimental
procedure more difficult from equipment safety concerns, such
as plasma arcs.
A third alternative, a liquid electrometer configuration
suggested by Clothier in 1965 [42], was a way to avoid the
limitations of the small force relative to the heavy electrodes,
while also performing a separate capacitance measurement.
This design was the choice of CSIRO in Australia. Bego [43]
compares the design options and results. Schematically drawn
in figure 4, the area between a fixed plate and a pool of liquid
mercury forms a capacitive force region. A voltage applied
between the electrode and the Hg pool raises the liquid’s
surface. The mechanical force of the capacitance change
7

## PDF page 9

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

to determine an electrical standard volt, with occasional volt
balance checks. However, in the 1970s, there was mounting
evidence of discrepancies between the as-maintained volt of
the Weston cells and the ampere units relative to the SI. As
a result, there was a call for more attention to the ampere
balances, reported in [52].
A potential experimental improvement came in the form
of a short addendum to a chapter describing the existing
techniques for measuring the gyromagnetic ratio of the proton.
(This and several other newer experiments also provide an
inferred value for h, but their uncertainty was undercut by
other methods, so they will not be mentioned in detail.)
Kibble in 1976 [53] suggested that there is a complementary
mode to the electromagnetic force generated on an induction
coil from a current in a surrounding coil. For an induction
coil within a stable magnetic field, moving the coil with
no current induces a voltage across the coil length that
is proportional to the velocity of motion. Measuring the
voltage-to-velocity quotient would provide the magnetic field
gradient term that was previously computed to determine the
force-to-current relation between the coil and the magnetic
field. The volt/velocity quotient technique also applies to
absolute ampere experiments, replacing the difficult numerical
computation for I2 M12 /z with electronic measurements,
presumably increasing the precision of the result, and at the
very least making it an easier technique. Whether it was
originally viewed as such, or very quickly realized among the
ampere groups is not apparent in published reports, and oral
histories vary [54].
The ampere balance measured the ratio of force to current.
As discussed in a later section, the combination of the two
quotient measurements can be written as a comparison of
two different kinds of power: mechanical force multiplied by
velocity, compared to electrical voltage times current. The
ampere balance was to become a watt balance. One last
discovery was needed to make it capable of measuring h, but
that had not occurred yet in the late 1970s and early 1980s. New
watt balances were under design at the time with the intention
of solving the correlated volt and ampere discrepancies the old
fashioned way, maybe with smaller uncertainty, most probably
with an easier procedure.

Figure 5. Absolute ampere coil configuration. The central coil
interacts with the magnetic field generated by the outer coils [48].

Figure 6. Ampere balance at NBS in 1912. A mass balance is on
top and connected to a moving coil below [48].

mutual inductance between the coils at different positions,
M12 /z. The moving coil was mechanically connected to
a balance beam mass comparator. A current, I1 , is injected
into the fixed coils, and current, I2 , into the center coil,
creating an electromagnetic force to balance the force, mg, on a
reference mass from the local acceleration of gravity. Gravity
acceleration was determined in a separate measurement. The
basic equation is
mg = I1 I2 M12 /z.

3.4. The misinterpreted volt determinations
For over a hundred years, national laboratories used large banks
of 1.018 V Weston standard cells, from 40 cells up to over a
hundred, to keep a laboratory, or as-maintained, representation
of a volt unit. Similarly, the as-maintained ohm was a bank
of resistors. The laboratory volt unit reliability presumed
two things; one, that the chemistry of the standard cells was
reasonably stable, and two, that although individual Weston
cells might drift over time, the mean voltage of a large group
would be statistically more stable, especially if the best cells
were chosen for the group. The group averages of the banks
were internationally compared every few years. Since moving
the national banks themselves would disturb their chemical
equilibrium and thus their voltage, a comparison consisted only
of an indirect transfer of a few standard cells, measured against

(7)

This established the link between the ampere and the SI
units of mass, length and time. The current was actually
measured against the as-maintained volt and ohm, the
laboratory standards. Since the technique managed to have
lower uncertainties than the absolute volt experiments, current
balances became the electrical standard from 1 January 1948,
as mentioned in [51]. A partial history of current balances at
NBS/NIST is reviewed in [32].
For decades, the ampere balance results were combined
with a calculated inductor or a calculable capacitor impedance
8

## PDF page 10

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

the group. Summarized in [55] the results plotted over time
during the 1950s and 1960s of intra-laboratory comparisons of
cells showed variations of a couple of microvolts, and intercomparisons between nations by several more microvolts.
To set the volt unit properly against the SI, ampere balance
measurements were combined with separate ohm evaluations.
Originally the ohm was based upon the impedance of a
carefully wound solenoid, a technique eventually superseded
by the Thomson–Lampard calculable capacitor. Since ampere
experiments were undertaken only about once every ten years,
the as-maintained volt group average was infrequently adjusted
to match ‘absolute’ results. However, the housekeeping of the
as-maintained volt unit in each country had things under the
carpet that were anything but transparent [51]. For one, an
occasional cell that demonstrated any sudden shift in value or
drift rate was replaced to maintain the stability of the group.
If or when a nation’s group average value was adjusted during
intervening intervals was ‘hidden’ within each nation’s record
keeping books. All this dust made it difficult to evaluate
the changes in the absolute ampere from one determination
to the next. It also affected the uncertainty estimations of
any results. While the succession of ampere balance results
improved in resolution, they tended to indicate that the asmaintained volt was always high, by about 10 µV. Why this
continued to happen is not clear. Years later, there was some
second-guessing that the Weston cells were drifting faster than
the predicted rate. Others are adamant that the so called
differences were simply not significant with respect to the
uncertainties on the ampere balance results, where they were
reported as 4 to 6 parts in 106 , the 10 µV difference was within
two standard deviations. For whatever reason, the apparent
agreement of the ampere balances over time caused them to
be misinterpreted as a better value than they proved to be.
As with the apparent agreement of h results from 1919 and
then disagreement with later experimental results, a similar
controversy was brewing.
In 1966, Terrien [56] reviewed the published values for
the ampere from the NBS 1958 [49] as 1 BIPM ampere
=1.000 0140 absolute ampere, and from the NPL in Vigoureux
in 1965 [57] as 1 BIPM ampere =1.000 0084 absolute ampere,
‘with an uncertainty which might be about ±3 or 4 µA.’ Since
the BIPM ohm was considered accurate to within 1 or 2 µ,
the conclusion was that the BIPM volt was high by 11 µV
with an uncertainty of 3 or 4 µV. A new ampere value, in
agreement with previous values, was reported to the BIPM
in [58], as summarized in [59]. The BIPM adjusted their asmaintained volt down by 11 µV in 1969 with the approval of
the CIPM 1968 [60]. Except in the precision world of the
national metrology laboratories, this change hardly affected
any industry or commercial measurements.
By this time, nations had begun to use the Josephson
effect to internally monitor their volt banks. The various
national VLab units agreed to within 2 × 10−7 as implied from
a compilation of international measurements of h/2e from
1971 to 1972, related in [61]. Cohen and Taylor in the 1973
constants adjustment [62] reported a new CODATA value for
h/2e with an uncertainty of 2.7 parts in 106 . This was such
a grand improvement from h/e determinations of just 8 years

earlier that national metrology laboratories agreed to adopt
the Josephson effect as a representation of the volt. To quote
from [63],‘In principle we might even do without Weston cells,
but this is hardly ever likely to occur, because Weston cells are
much more convenient. Practical application of the Josephson
effect is not a simple matter, but it must be done. . . ’
It was done, and it would take only a little over one decade
for Josephson devices and digital voltmeters to mature enough
for automated Josephson volt systems to proliferate beyond the
major national laboratories. New theoretical ideas explained
how to link thousands of Josephson junctions together at
millimeter wave frequencies near 100 GHz. As fabrication
capabilities came to realize these designs, 1984 spawned the
next generation of Josephson voltage devices. A single device
could generate voltages at the 1 V level, as described in [64] and
in [65]. This eliminated the uncertainties associated with ratio
conversions of millivolts to the characteristic 1.018 V Weston
cell voltage. Device fabrication improvements continued,
as reviewed by Hamilton [66]. Computer automation and
digital instrumentation allowed voltage standard maintenance
to become highly accurate and very simple. By 2000, the use
of Weston cells would be mostly discontinued.
In the meantime, fundamental constants measurements
in different nations were not quite consistent. When all
nations agreed to use the Josephson effect in 1972, it was not
as an SI unit, but a representational voltage standard. The
laboratory volt unit was still called a conventional unit, VLab .
Nations did not standardize to a single value for the Josephson
constant, as recommended by Leclerc [67]. Because of the
differences between the cell bank values around the world,
different nations choose h/2e values that better agreed with
what they believed their own VLab indicated, relative to the
SI volt maintained at the BIPM. The good news was that
some of the dust under the rug was swept away, since it
was easier to compare the bookkeeping of other fundamental
constant measurements involving voltage. At least, the relative
differences between national VLab values were now stable
over time.
3.5. Quantum Hall effect: a resistance standard
While the volt controversies raged, a major discovery occurred
that was to complete the puzzle of directly measuring h via
the watt balance. Klaus von Klitzing in 1980 [68] discovered
experimental evidence for quantized resistance plateaus in
the Hall effect, thus finding a new device that could relate
fundamental constants to another electrical unit. To exhibit
the quantum Hall effect (QHE), a semiconductor device with
a very thin doped conduction layer confines electrons to orbits
within a plane, one thin enough to restrict z-axis energy states.
In a strong magnetic field, the electrons orbit in the twodimensional plane with quantized energy. With current passing
through the flat device in a strong magnetic field, the voltage as
measured transverse to the current forms constant impedance
steps in the I –V curve. The equation relating the resistance
steps, R, of the device to the ratio of h/e2 , is
R = (1/ i)(h/e2 ),
where i is a quantum number for the step.
9

(8)

## PDF page 11

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Table 1. List of inferred values for h from different measurement techniques.
Planck h value

Relative standard
uncertainty (×10−6 )

6.626 071(11) × 10−34 J s
6.626 072 9(67) × 10−34 J s
6.626 065 7(88) × 10−34 J s
6.626 068 4(36) × 10−34 J s
6.626 067 0(36) × 10−34 J s

1.6
1.0
1.3
0.54
0.63

ρ –90 (H)
ρ –90 (H)

F90
KJ
KJ

The development of QHE devices and dc resistance
metrology was likewise parallel to the early work on the
Josephson devices and voltage metrology. This history is
related in many books.

Before delving into the discussion of the watt balance and
a direct measurement of h, it is useful to note that in the
late 1980s, several of the older methods by which h could
be inferred had uncertainties approaching 1 part in 106 . The
most important one is via the Avogadro constant, NA . NA is
measured by ‘counting’ the atoms in a kilogram of silicon,
carved from a single crystal, and polished into a near perfect
sphere. The Avogadro measurement has a long history, as
reviewed by Becker in 2001 [15]. The name of this technique
has varied in publications, but its recent name is descriptive of
one part of the group of measurements. The project is generally
referred to as the x-ray crystal density (XRCD) measurement.
NA appears as a simple equation,

Ar (Si)Mu
8 d23 2 0 ρ(Si)

3.7. The 1990 electrical units adjustment

(9)

,

NIM-1995 [69]
NPL-1979 [70]
NIST-1980 [71]
NMI-1989 [72]
PTB-1991 [74]

Though dependent upon other fundamental constants, α and
R∞ have uncertainties smaller by an order of magnitude
or more than the NA part via the XRCD method, so
the combination has about the same uncertainty as direct
measurements of h via watt balance techniques.
Other indirect methods, which lead to inferred values for
the Planck constant, are through measuring the gyromagnetic
ratio of a proton in a high magnetic field, ρ –90 (H), and the
Faraday constant, F90 , as well as the earlier mentioned volt
balance, KJ = 2e/ h. Table 1 lists the CODATA 2006 values
in 1990 units for these inferred values of h.

Data from these fundamental constants measurements in the
1980s indicated that something had gone wrong with the volt
adjustment of 1969. Just prior to the input deadline for results
to contribute to the constants adjustment of 1990, absolute
volt experiments proved conclusively that the standard cell
banks were indeed in error after the adjustment. The liquid
electrometers were a significant improvement over previous
absolute volt experiments. The best measurements yet in
determining h/2e were reported in [72] and in [73]. The
conventional volt was found to be different from the SI volt
by about 8 × 10−6 with an uncertainty of 0.27 × 10−6 . This
uncertainty was determined later to have a possible error in
the reference capacitor, and so was subsequently reported
in CODATA 1998 as 0.31 × 10−6 in [74]. This offset was
further confirmed by a result from the NPL watt balance,
described in a section below. Later, using the moving vertical
electrode technique, a measurement reported in [75] agreed
with the liquid electrometer values with only a slightly better
uncertainty of 0.27 × 10−6 . These uncertainties in measuring
h/2e with the absolute volt and ampere experiments are
probably indicative of their fundamental limit [76].
Now armed with the new and improved absolute volt
measurements, the other inferred measurements of h and e, and
the NPL watt balance result for h, the volt and ohm units were
adjusted in 1990. The Josephson constant KJ = 2e/ h was
given a defined value of KJ-90 = 483.5979 × 109 Hz V−1 [77];
this time all countries adopted the assigned value. Some

where Vmol is the molar volume, a03 the atomic cell unit volume
of silicon (Si), and n the number of atoms per unit cell (8
for Si crystals). However, the component measurements are
exceedingly difficult. Vmol is determined from the molar
mass, Mmol , and the density of a Si crystal, ρ (Si). Mmol
depends on the assessment of the isotopic distribution and ρ
(Si) depends upon accounting for crystalline irregularities. The
mass of the sphere in a vacuum is compared, not automatically
easily, against a cylindrical kilogram reference standard. The
macroscopic volume requires measuring millions of linear
diameters of the sphere, accounting for surface layers of SiO
and SiO2 . The atomic cell unit volume is found from x-ray
crystal diffraction measurement of the lattice spacing of a
particular crystal plane, d2 2 0 ,√times the root sum square of
the cell’s atom number, α03 = 8d23 2 0 (220 are Miller indices
for the crystal plane of choice). Although a vast improvement
over the etched line method, measuring the lattice spacing is
still one of the more difficult aspects, just as in the early 20th
century x-ray diffraction experiments were limiting factors for
determining h/e. For Si crystal measurements, the equation
for NA showing all the variables is
NA = √

Source

NA and h is derived from combining formulae for the Rydberg
constant, R∞ = me cα 2 /2h , the fine structure constant, α, the
speed of light, c, and electron mass, me . The relation of the
Avogadro constant to the Planck constant is
√
2cα 2 Mu Ar (e)d23 2 0
.
(11)
h=
2R∞ Vm (Si)

3.6. Avogadro constant

NA = n Vmol /a03 ,

Method

(10)

where Ar (Si) is the atomic ratio of Si to C12 and Mu is the
atomic molar mass equal to 1000 kg mol−1 . A relation between
10

## PDF page 12

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

countries had to change by nearly 10 µV to adjust their VLab
unit so that it was consistent with KJ-90 . To distinguish between
the conventional unit and the SI unit, the symbol VJ-90 was
adopted to represent the volt as-maintained via the Josephson
effect.
Similar to the volt standard, there was a small difference
between various national ohm banks of resistors and the
SI ohm. The traceability to the SI provided by infrequent
measurements of the calculable capacitors with stated
uncertainties of about 2 × 10−8 had proven consistent, and
more frequent measurements using the new QHE systems
revealed only small drift rates in the resistors. In the 1990
adjustment, the ohm change was about 1 × 10−6 , an order
of magnitude below the voltage unit adjustments. A fixed
value for the von Klitzing constant RK = h/e2 was assigned
as RK-90 = 25 812.807 , where the conventional units are
90 . The dust was formally cleaned from under the rug for asmaintained electrical units, with only one set of conventional
units, now represented as V90 , 90 , and W90 .
This time the volt adjustment had effects reaching outside
the small community of national metrology laboratories and
fundamental constant experiments. The electrical instruments
available to the commercial industry in 1990 were a far cry
better than the four-figure digital and analogue electronic
instruments of 1970. Four companies were manufacturing
8-digit voltmeters with accuracy specifications within 10 µV.
Now the change also filtered down to affect the calibrations of
a considerable fraction of industry in many countries. Industry
complied with the change, but voiced concerns about how
often this was going to happen in the future. Taylor in
1987 [78] attempted to understand the volt adjustment error
of 1969, reporting how it was likely that researchers and
decision makers were fooled by the consistency of the ampere
results. As mentioned earlier in this paper, this paralleled the
presumption on the accuracy of the Planck constant results
of the 1920s. So with lessons learned, there was hope that
new methods and superior electronic measurement instruments
would further reduce uncertainties in the Planck constant while
keeping the electrical units stable. This leads to the next
sections on the experiments that are attempting to do this.

Researchers in the field soon found that a new electric
power relation, combining the Josephson effect of equation (4)
and the QHE effect of equation (8), resulted in a simple formula
for h in terms of frequency (ignoring quantum numbers),
ε 2 /R =

(f h/2e)2
= f 2 h/4.
(h/e2 )

(12)

(A switch to the symbol ε for voltage is an effort to differentiate
between voltage measurement values, volt units and velocity
symbols.) Recognition of the relation was not immediate.
From contacting people who worked in the field at the time,
and sorting through the references, there is no clear claim
of who or when a particular individual put the theoretical
equations together into the form of equation (12) to single out
h. Many relations were discussion topics among researchers
of the ampere and fundamental constants. While suspecting
that the electrical lab units were discrepant from the SI, Taylor
in 1985 [81] came close to explicitly publishing the relation,
writing out the physics relations in terms of laboratory units.
Within a year, Kose and Woger [82] put the Josephson equation
and the QHE equation together as an energy calculation and
wrote, ‘It is interesting to note that electrical energy, which
is consumed in large amounts of terawatthours per year for
one country, is today traceable to Planck’s constant and a
frequency!’ (The derivation in that paper is not exactly correct,
since it is missing the factor of 2 in the Josephson equation,
unless it was implied in a statement in the paper mentioning
h relative to ‘well known constants’. That derivation also
converts the power to energy units with a time variable, without
explaining how the time should be measured.)
Soon after, everyone agreed that a direct measurement
of h was now attainable, so interest in several experiments
intensified. Although two watt balances happened to be under
development at a convenient time to claim prominence, an
old magnetic levitation idea earned some reconsideration, and
new lines of research initiated novel developments of other
watt balances and a joule balance. However, getting a much
better h value was and still is anything but simple. At present,
the watt balances are the most advanced and numerous, and
so will dominate the following discussion. The others are
superconducting magnetic levitation and the joule balance.

4. Modern direct measurements of h
4.1. A direct link to h via quantum electronics

4.2. Superconducting magnetic levitation

It is perhaps a quirk of history that two experiments were
already planning to measure electrical power in SI units just
as a more fundamental prospect was discovered. Kibble’s
suggested alteration to ampere balances caused the NPL in
England [79] and the NBS in the United States [80] to
redesign their existing ampere balances to take advantage of
the motion mode. They had yet to complete either system
when the QHE was discovered in 1980. The QHE theory
quickly had a significant impact on fundamental constants
calculations, adding another physics relation between many
other experiments, fundamental constants and lab units. The
results of several experiments were reexamined to see what
values might be available for new determinations (as Millikan
and others had started many decades earlier).

Superconducting magnetic levitation was first described in [83]
as an alternative to the absolute ampere experiment. An
electromagnetic coil surrounding a small superconducting cup
will raise the cup by employing the perfect diamagnetic effect
of a superconductor in rejecting magnetic flux. Sometime
called a Weber balance, it had advantages in being apparently
simple and using test masses larger than the earlier ampere
balance experiments. The method and related equation are as
follows, with the electrical circuit schematic shown in figure 7.
Gravitational potential energy is measured as a force on a mass,
mg, when it is raised from a low position to a higher one,
ZH − ZL . This equates to the change in the magnetic flux
quanta corresponding to the change of current, iH − iL . The
coil current is measured as the voltage drop across a resistor, R.
11

## PDF page 13

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 7. Magnetic levitation scheme. The levitated cup on the
right is superconducting.

The self-inductance of the coil and cup assembly would need to
be calculated or measured in some way. A Josephson junction,
represented as an X in the circuit, is biased to a voltage step
proportional to the magnetic flux density in the coil, where
V = nf 0 is also a reference for the voltage (remember the
flux quantum 0 = h/2e).
An initial concern about the technique was that work
might be performed, thus changing the magnetic flux gradient
between measurements. Kibble in 1983 [106] proposed
moving the cup to measure the velocity while also measuring
the current. This method presaged the simultaneous current
and voltage measurements approach on the watt balances
of twenty years later. The adopted method used two static
positions, measuring the voltage difference across the coil
against a Josephson device, and a SQUID as an ultra-sensitive
detector of any residual current is not flowing through the
reference resistor, R. The magnetic flux energy in the coil
equals the potential energy of raising the cup,
∫ φH
i dφ − 21 (iH φH − iL φL ) = (ZH − ZL )mg.
(13)

Figure 8. Coil configuration for the Joule balance. Reproduced
with permission [170]. Copyright 2010 IEEE.

could freeze to the cup’s surface, then backfilled with He gas to
low-pressure (about 100 Pa) to keep the helium from liquefying
in the test volume, and also to reduce buoyancy and refractive
index effects. The cup is still susceptible to He gas absorption
on its surface.
There is a proposal to improve the experiment in [87].
The Center for Metrology and Accreditation (MIKES) in
Finland continues some of the research, but a comment in [88]
reasserted that trapped flux among other things would limit the
relative uncertainty at much greater than 10−8 . A follow up
proposal in [89] re-evaluates the earlier system to solve some
problems, especially the energy losses in the levitation from
tapped flux.
4.3. The Joule balance

φL

A joule balance technique for measuring h was proposed
in [90]. The schematic in figure 8 shows two coils rigidly
connected to move in unison, wired in series opposition above
and below a fixed coil. Note that this coil configuration is very
similar to the design in figure 5, of the Rayleigh coils of the
ampere balance, except here the outside coils move while the
inner coil is fixed. In a measurement, the outer coils are moved
to two positions with and without a test mass. The potential
energy change is balanced out with an electromagnetic energy
change, measured by currents in the coils. With proper design
this coil system has a mutual inductance Mz that should be
independent of small x or y displacements. The force on the
movable coil is F = (∂Mz /∂z)I1 I2 for currents injected into
the fixed coil, I1 , and movable coil, I2 .
The difference in this idea from the older ampere methods
presumes that the mutual inductance Mz can be electronically
measured with modern electronic instruments to improve the
precision over the dimensional calculations. The procedure
uses low frequency ac signals to vary the current in the fixed coil
at different frequencies while measuring the induced voltage
in the outer coils. Combined with measuring the spatial
displacement in the vertical height of the outer coils with
interferometers, this establishes a precisely known inductance
gradient along the z-axis: a measurement that was unavailable

The various measured flux densities are multiples of 0 and
i can be written as V /R = nf 0 /R. R can be written in
terms of h/e2 , thus the i terms become terms of 20 /(h/e2 ),
equaling the familiar h/4.
A projected measurement resolution of 1 × 10−6 for
this experiment was reported in [85], yet it proved to be
a very difficult experiment through several generations of
improvement. Major difficulties kept this experiment from
getting a better uncertainty than about 10 × 10−6 and it was
discontinued at the National Metrology Institute of Japan
(NMIJ) [86]. The position interferometry proved most
difficult. The unstable cup shape easily tipped or rotated,
and with the reflecting corner cube at the bottom of the cup,
below the center of mass (CM), sufficient height resolution
could not be attained over the 9 mm rise of the cup. Also, the
diamagnetic force was small, so the cup mass of about 25 g
had large scaling errors to 1 kg. Though larger than the few
grams of the absolute ampere tests, it was far smaller than the
contemporary designs of watt balances that employ 1 kg test
masses. Cups were made of phosphor-bronze covered with
the soft metal Pb, a type I superconductor needed to avoid skin
penetration by the magnetic flux. The cup and coil environment
are evacuated to a high vacuum to rid the volume of gasses that
12

## PDF page 14

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

on the former ampere balance. The ac measurement does
require extrapolating Mz to dc voltages. Setting the outer
coil to positions z1 and then z2 , and integrating the force in
equation (7), the balance equation becomes
∫ z2
(Mz1 − Mz2 )I1 I2 − mg(z1 − z2 ) =
f (z) dz, (14)
z1

where f (z) equals a residual variation in the electromagnetic
forces. This term can be made negligible by careful design and
placement, thus requiring only two positional measurements
of Mz .
Realizing Mz is a function of the magnetic flux density
gradient per current, a dimensional analysis of the term
Mz I1 I2 leads to a direct measure of h in terms of the potential
energy of the position change. An anticipated advantage
to this technique is that if the mutual inductance Mz is a
structural characteristic of the coils and can be measured with
sufficient precision, it could be more stable than trying to
maintain an external magnetic field source. Having only static
measurement modes also removes the difficult measurement
and analysis of the dynamic voltage-to-velocity quotient of
the watt balance. Long time-interval averaging of the current
measurements can reduce noise. There are also no worries
about magnetic field changes between the force and motion
modes. A disadvantage is that small forces between room
temperature coils will limit the test mass size, suggesting the
necessity of superconducting coils.

Figure 9. The watt balance scheme, a simple adaptation from the
ampere balance.

1 V drop across a standard resistor value. (3) Connect the coil
to a support mechanism that has a balancing stage so the coil
moves with a small driving force, external to the main coil.
(4) Design the balance mechanism so the coil moves nearly
vertically over as long a distance as possible, while maintaining
a constant alignment with minimal horizontal forces.
The schematic design of figure 9 represents the adopted
operation of the original ampere balances. Without test masses,
the main coil with no current is in balance with a counter
weight. In the force mode, a tare mass on the counter mass
side, of half the main test mass, is initially balanced by the
downward force of the electromagnetic force, then the current
is reversed to balance the main test mass. This reversal process
has multiple advantages. The electromagnetic applied force is
half the total gravitational force on the test mass. Current
reversals provide a means to eliminate voltage and balance
force offsets. And the symmetry of positive and negative
current magnitude means constant ohmic heating of the coil
during the weighing mode. A balance beam is a familiar
adaptation of the laboratory mass balance, and like a children’s
seesaw, allows the coil to move mostly vertically. Many of the
recent design efforts are considering novel designs to address
subtle concerns about the linearity of the motion and changing
internal forces on the mechanism when adding the test masses.

4.4. The watt balance
The third way to directly measure h, and presently the most
popular adaptation of the absolute ampere experiment, is
the watt balance. The rest of this section will develop
the details of the watt balance technique, starting with the
concept, some basic design considerations, the operating
theory of the measurements and the resulting derivation
of the Planck constant from the experiment variables.
There are measurement systems that are peripheral parts of
watt balance experiment measurements: Josephson voltage,
QHE resistance, local gravity acceleration, laser frequency
determinations and mass comparison systems. These are
familiar, as primary national laboratory calibration systems
and/or commercial systems, so will not be discussed. Their
importance is significant, since the most precise of these
calibration systems are only available at major national
metrology laboratories. This implies that watt balances, at least
the most precise ones, are not likely to be built anywhere else.
The ‘balance’ concept correspondingly applies to null
balancing of mechanical and electromagnetic forces, and
equating the computed mechanical and electromagnetic power
as measured in the experiment.
The basic recipe is
summarized into four criteria that have mutually overlapping
considerations. (1) Generate a stable magnetic field where the
flux density spatial gradient has a preferential geometry. (2)
Design for that field an induction coil operating at standard
reference values for voltage, current (resistance) and mass, for
example, generating 1 V at a convenient velocity or generating
a 10 N force for a 1 kg reference with the current producing a

4.4.1. Magnetic field specifications. This first section on
the design of the magnetic field, occurring before the basic
watt balance formulas are discussed, may seem out of place,
but understanding the modern magnetic field design simplifies
the magnetic coupling equations that follow. It is also vital in
understanding the subtleties of the two distinct data acquisition
modes: a force mode, usually static in position, and a moving
or dynamic mode. Presently they are measured at separate
times in all but one system.
The combination of the two measurement modes
eliminated the requirement from the ampere balance that the
mutual inductance of coils need be computable. Thus, a
permanent background magnetic field is used to generate a
significantly larger force by an induction coil of about the
13

## PDF page 15

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

same dimensions. However, the effects of the magnetic field
B must be characterized over a longer vertical range. All
present and proposed field sources have in common two design
goals described in [91]. As the more easily obtainable goal,
(i) the field’s effective force on the induction coil should
be independent of the induction coil’s diameter, including
construction irregularities and temperature expansion. Often
called a radial field source, this means that B has a radial
dependence of 1/r. An induction coil couples to a field
in proportion to its radius r, whether producing a force
generated by current, or a voltage induced from motion. Goal
(i) minimizes the first order dependence to r of the coil
radius. This is especially important in avoiding time dependent
variations in inductive coupling as the coil dimensions may
vary due to ohmic heating between changes in the coil’s
current. The second goal (ii) relates to the coil’s motion:
B should be uniform along the vertical travel path z.
Mathematically this means the force derivative is flat with
respect to z, or ∂F /∂z ≈ 0. A corollary to both goals implies
B (r, z, θ ) has 360◦ azimuthal symmetry, and a cylindrical
coordinate system is usually used in calculations.
Obtaining perfection for all conditions requires an
unachievable complicated design of the magnet source, so
condition (i) takes precedence. A design using opposing
magnets achieves a flat spot near the center position along
the line of travel, z0 . This position is optimum for the force,
or weighing position, conveniently minimizing the effects
from unavoidable position shifts of the coil due to mechanical
stresses or temperature contractions in the support system.
B (r, z) is generally parabolic near z0 , with the width of the
parabola partially dependent upon the cylindrical thickness of
the induction coil, r0 ± r. Typically the gradient ∂F /∂z is
flat to less than 1 part in 107 over a region 50 µm wide.
Depending upon the width of the flat region, it may be
difficult to reposition the coil to a point where the field change
is negligible. When a mass is added to the coil support structure
and balanced by the electromagnetic force, the support rods
will expand or contract by tens of micrometers due to internal
stress changes. Adjusting the angular position of the balance
arm may compensate for a coil position change, but this leads
to more severe difficulties, a problem that is explained later in
the technical descriptions of existing systems.

to a force on a coil with a current, I , within a magnetic flux
density, , dependent upon the z gradient,
Fz = mg = −I

∂
.
∂z

(15)

This equation describes an electric motor, with m, g and I
the measured variables. Computing the mutual inductance
between electromagnets derived the flux density gradient,
∂ /∂z. Bryan Kibble in 1976 [53] realized that in the
differential form of Faraday’s Law, a coil produces a voltage,
ε, when moving at a velocity ∂z/∂t = v,
ε=−

∂
∂ ∂z
∂
=−
= −v
.
∂t
∂z ∂t
∂z

(16)

This equation describes an electric generator, with ε and v the
measured variables. Assuming for now that the magnetic flux
gradient is identical between the two modes, the two equations
combine to eliminate the magnetic flux gradient, where the
results show how one experiment measures all the variables
leading to the relation between mechanical power and electrical
power,
mgvz = εI = ε2 /R,
(17)
where I is measured as the voltage drop across a reference
resistance, R.
There are complications to the constant flux density
assumption that will be mentioned later.
Also, this
original derivation glosses over the force and velocity vector
character, while voltage is a scalar. These vector alignment
considerations have their own section.
4.4.3. An integral representation. There are equivalent
integral forms for equations (15) and (16). The complete
integral form includes the explicit vector considerations in
the calculation. Some recent papers have used this in a
modified form, suggesting it also provides a clearer picture
of the magnetic coupling itself, and a convenient parameter
for setting the magnet and coil design goals. From Ampere’s
force law
∮
F =I
(dr × B )
Fz = I B(z)L.
(18)
C

By design, B has a radial direction and is azimuthally uniform,
so in the cross product with wire length dr , the integral equals
the simple product B(z) times the total wire length L. (On a
very technical point, windings in the coil may include lengths
of wire not perpendicular to the field, and the overall plane
of the windings will not be parallel to a coil’s top surface.
Such coil imperfections contribute to misalignments and are
correctable.) Only the vertical component Fz is shown on the
right equation. With perfect alignment of the magnetic field,
coil and gravity defining the z-axis, this would be the only
term.
Faraday’s law in integral form (modified to assume vertical
motion and a radial field) is
∮
ε=
B · (v × dr ) = vz B(z)L.
(19)

4.4.2. Basic watt equations—two modes. In the watt balance
technique, there has already been mention of a static mode of
current and force, and a motion mode of voltage and constant
velocity; this section adds the mathematical details. Various
theoretical formulations have described the coupling of the
electromagnetic and gravitational forces, ultimately linking
them to the quantum electronic relation of equation (12). The
differential theory is how the original form was described, and
makes the experiment calculations appear simple, but perhaps
harder to visualize. The more recent integral form descriptions
are equivalent, and have a certain convenience.
It was long recognized in the absolute ampere technique
that the differential Lorentz force equation describes a force
due to the acceleration of gravity, g, on a mass, m, as equal

C

14

## PDF page 16

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

The velocity vector is actually a combination of components
vx , vy and vz , and ωx , ωy and ωz . The cross product of vz
and dr is uniform along the entire length of the coil. The
term ωz is negligible, as it is easy to reduce to zero and is
parallel to vz for a circular coil. The cross products involving
vx , vy , ωx and ωy may not go to zero around the total length
of the coil, so any motions in those directions contribute a
voltage. Assuming those motions are minimized, then at a
position z, the vertical velocity component of the integral leads
to a voltage dependent upon the term B(z)L in the equation.
Combining equations (18) and (19) results in the same relation
as equation (17).
The convenience of this formulation is the general term
BL. Retaining the BL component rather than using the original
differential method to eliminate the flux density gradient makes
further analyses of the interaction between the current and the
magnetic field a bit clearer, and so will be used in following
sections. It is also a convenient parameter in designing a
new system, which requires decisions concerning the source
magnetic field strength and the length of wire, i.e. number of
turns. System design options include the desired voltage per
velocity, the amount of force per current, the mass of the coil
and the test weight value. The tradeoffs are understandable:
stronger field versus fewer turns, more turns versus less weight
of the coil, larger coil versus a bigger and heavier magnet.

the quantum step numbers n1,2,3 , a relation of theoretical power
with the realization becomes
h
n1 n2 (f h/2e)2
ε2
=
= n1 n2 n3 f 2 [W]
2
R
(1/n3 )(h/e )
4
2
n1 n2 n3 f
= 2
(20)
[W90 ] ,
KJ-90 RK-90
where the appropriate power units are in square brackets. The
frequency f may be considered the same in both test modes
or written separately, but it is a measured value relative to
an atomic frequency standard. The relation between the watt
units is
2
[W90 ] = (h/4)(RK−90 KJ−90
)[W].
(21)
Another way to understand the relation between SI
and 1990 units is to consider equation (17) written as
(mgv)/(ε 2 /R) ≡ 1. Were ε and R measured in relation to
constants known exactly in the SI, this relation is an identity,
since mechanical power is equal to electrical power. Normal
every day calibrations using m, g and v are in SI units, but
electrical calibrations of references and instruments for voltage
and resistance are made with V90 and 90 , respectively. Thus,
putting conventional electrical measurements into the SI units
of mechanical power measurements requires a conversion from
W90 to W, which is where equation (21) comes into play.
Combining equations (17) and (21), the complete watt balance
equation to derive the Planck constant becomes

4.5. Deriving h in measurements using SI units

mgv
4
= h.
(ε 2 /R)90 KJ2-90 RK-90

The SI as a system of units has been briefly mentioned,
and much of this paper has so far assumed that readers are
experienced with the SI, calibrations and traceability. This is
not meant to be a basic tutorial for those less familiar. However,
since several papers have discussed possible definitions for
linking an SI mass to electrical measurements and why a new
definition is needed, a bit of detail is in order. Equation (12)
shows that quantum theories when put into electric power form
result in the Planck constant h. The value of h is meaningful if it
is measured in units that are consistent, no matter how they are
measured. Measurements from the watt balance equation (17)
provide the SI basis for this relation.
In electrical calibrations, the volt unit is derived from the
Josephson effect of equation (4). The Josephson constant
KJ = 2e/ h is not known exactly in the SI, so conventional
voltage calibrations use the realization constant KJ-90 instead.
This conventional volt unit is expressed as V90 . The resistance
unit is derived from the QHE of equation (8). In the same
vein, the von Klitzing constant RK = h/e2 is not known in SI
units, so values are expressed as the conventional ohm unit,
90 . It follows that the conventional watt unit is W90 =
2
/ 90 while a true SI watt unit is W = V2 / . The
V90
volt and ohm reference source devices generate quantized, or
discrete, values, scaled in magnitude by the integer numbers
shown in quantum equations. In this derivation, these integers
eventually drop out and thus do not affect the results.
The question arises: what ‘units’ are in the experiment
results, SI or V90 , 90 and W90 ? The answer is, both. Electric
power can be formulated with the theoretical equations or
realization equations. Expanding equation (12) and keeping

(22)

It is important to understand that this measurement of h does
not depend upon any adopted values for KJ-90 and RK-90 , or any
uncertainty relative to SI in their adopted values. The Planck
constant derives from the theory underlying the Josephson and
QHE devices as the ultimate references for the volt and ohm.
The measurement would still work if the adopted values were
both set to 1. However, similar to different countries being
comfortable with Fahrenheit or Celsius temperature scales
and only converting to Kelvin when necessary, it is a great
convenience to store electrical records in the conventional
units, since the values are instantly familiar.
4.6. Defining kilogram mass in terms of h
Force and velocity are considered mechanical variables, where
the lab references are in SI units for the dimensions of time and
frequency, length and mass. Time and frequency are based
upon the definition of the second as a number of oscillations,
or the frequency, of a certain atomic transition in the cesium
atom. This particular microwave frequency is rarely used
in laboratories, but it is easy to apply it indirectly via GPS
receivers to calibrate a general frequency standard, such as the
10 MHz crystal standard. Length is defined as the wavelength
of laser light relative to the assigned constant speed of light
and the frequency of the laser. Mass is defined relative to the
artifact IPK.
Equation (22) is written as the derivation of h from
measurements made in SI units, including the IPK standard
15

## PDF page 17

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

mass units portends a problem where the electrical power
measurements are noticeably different from the mechanical
power measurements. To keep this from being a commercial
measurement problem, the volt and ohm would one day have
to be readjusted. Ah, but we have been there before! The
watt balance results are one answer to the mass problem, so
international efforts to design and improve the techniques have
become more important. After the proposed redefinition of
the SI, these systems will become the next mass standard,
whereby an expanding group of nations will maintain their
own kilogram via the unchanging quantum-based electrical
units. There are new proposals to redefine not just mass, but
the whole SI in terms of assigned value constants (no longer
italicized as variables): Planck h, speed of light c, electron
charge e and others from [93] and in [94].
There are several physics relations between mass and the
fundamental constants that have been proposed. They are
not really different, except in their applicability and ease of
understanding. As a simple derivation, remember the quantum
energy of equation (1), E = hf . Then also note the energy
equation from special relativity, E = mc2 . Equating energy
E, and with h and c as defined constants, the relation is

Figure 10. The relative drift several of the kilogram PtIr copies.
IPK is by definition the zero axis line.

mass. However, as the Josephson device became the reference
for the conventional volt unit and QHE device became the
reference for the conventional ohm unit, this relation can be
reversed so the watt balance results become a reference for
the conventional kilogram mass unit. There is a reason to do
this. Just like where the volt and ohm artifact drift caused long
term measurement problems during the pre-quantum electrical
device era, an inconsistency between the kilogram artifact mass
values now poses a question about the long term drift of the
kilogram unit with respect to the quantum-based electrical
units.
Davis [92] noted that the original copies of IPK, all 1 kg
cylinders made of 90% Pt and 10% Ir (metals platinum and
iridium) are drifting in value relative to IPK over the 120 years
since they were first compared. Excluding a few outliers, the
average of the group is gaining mass, as illustrated in figure 10.
The largest individual change of the main group is an increase
of about 50 µg per 100 years. Except for their amount of
handling and resident country (most of the copies are national
standards outside of Paris), they all have the same chemistry
and general exposure to the environment (they must be stored
in air but are kept in secure safes). It has been argued that
statistically, the group average is more representative of the true
kilogram, so therefore the IPK is losing mass. However, this
was the conceit of the previous arguments concerning Weston
standard cell groups. It is likely that all the masses, including
IPK, are undergoing a larger than apparent, plus or minus,
change in their true mass due to alterations from an analogous
chemical contaminant, and perhaps a bit of wear. (There is
a standard cleaning procedure to counteract the accumulated
dust and surface film.) The likely contaminants are airborne
pollutants of hydrocarbon or mercury; Pt readily absorbs them
both. It may also be possible that hydrocarbons are leaking
out due to contamination in the original smelting process.
So although h is assumed to be a fundamental physical
constant, unchanging in time, measurements of h in SI
units will change over the next few decades. The worst
manifestation of this worries users of the volt and ohm
units, which depend upon h.
It is relatively easy to
perform calibrations with uncertainties less than the scatter
of the mass artifact distribution, so the long term drift in

m = f h/c2 .

(23)

This simplified equation masks the complexity of the watt
balance type of measurement; it is not clear what the value
of f means for a standard mass, such as a kilogram. There
is a derivation of a similar relation showing in detail the
measurement quantities, based on [95]. Recognize that the
SI mechanical power term mgv in equation (17) can be defined
as equal to the third term of electrical power in equation (20).
The assigned constant values for h and e will equally define
KJ-90 and RK-90 . Solving for m obtains
m=

n1 n2 n3 f 2 h
.
gv
4

(24)

Here it is understood that the frequency f is now a laboratory
standard. This equation is understandable in deriving a mass
value from the watt balance measurements, but it is not
obviously equal to the watt result derivation of equation (22).
To examine whether these representations are equal and
derive a defining relation, consider the following unit analysis,
including detailed measurements that are usually implicitly
assumed in other technical papers. Start with a voltage ε
from the moving coil measured against a Josephson voltage,
ε1 = (U + n1 f1 h/2e). U is the voltmeter incremental
difference from a reference Josephson step, n1 , at a microwave
frequency f1 , e.g. 18 GHz, chosen for the convenience of the
measurement. Actually, f1 = n1f f , where f is a typical
lab reference standard frequency (e.g. 10 MHz), that is in turn
referenced to an atomic clock (e.g. GPS). The scaling multiple,
n1f , is a real number (as opposed to an integer). The quantum
integer number, n1 , can be combined with the number n1f to
include the fractional voltage (from the U ). The value n1
becomes a scaling factor relating a voltage measurement to
fundamental constants.
The same trick for the force mode applies to current
measured as a voltage drop ε across a resistor. A voltage
16

## PDF page 18

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

scale factor of n2 and the resistance scale factor n3 are also
fractions plus integer numbers from a similar treatment for
measuring another voltage and a resistance that is not an exact
multiple of the QHE step. In practice, these implicit numbers
n1,2,3 are incorporated in the reference values and stored as
real numbers in volt or resistance units. Similarly reduced
to component measurements, velocity is v = lv · (tv )−1 and
gravity acceleration is g = lg · (tg )−2 , where l is a length
measurement and t is a time measurement during the velocity
or gravity test, respectively. A velocity v is further reduced
to a measurement involving time, which is a multiple scale
factor of nv,t /f , where f is a lab reference frequency. The
wavelength, λ, and its equation for light in a vacuum at speed
c is λf = c. Any z-position length, especially as measured via
interferometry, is a multiple of wavelengths nv,l l = nv,l c/fL .
Whether the interferometer laser frequency is a known mode
of a reference iodine-stabilized laser, or the frequency of some
other laser, such as a helium–neon laser measured against a
reference laser, the laser frequency fL is a multiple of the
lab frequency f ultimately traceable to an atomic standard
such as GPS, such that fL = nL f . So now a measurement
v = (nv,l c/nL f )(nv,t nv,t f ) = nv c. This is recognizable as a
fraction nv of c, the speed of light. A similar exercise with the
length and time gives gravity acceleration as g = ng cf .
Finally, equation (25) combines the actual measurement
variables made for equation (24), including scale factors
n1 , n2 , n3 , ng , nv of an arbitrary lab frequency reference
f , but ultimately traceable to the atomic clock frequency.
The complicated middle term of the following equation can
be simplified to K measurements, a frequency reference
(traceable to SI), and the constants h and c,
m=

n1 n2 n3 f 2 h
h
= Kf 2 .
(ng cf )(nv c) 4
c

design variation (MSL) and one measuring the Planck constant
via the joule balance (NIM). Since the watt balance is a
technique undergoing intense improvements, there are five
different technical methods being practiced. Several papers
have previously reviewed many of the operational parameters
of the operational systems in the NMIs, by Eichenberger in
2003 [96] and 2009 [97].
All systems have certain things in common. (1) There
is a source magnet providing a strong, constant background
field. (2) The magnet, coil and other parts of the system must
be aligned to something, most often the gravity acceleration
vector. Misalignment corrections need to be characterized. (3)
The gravitational force on a test mass and the current in the
coil are measured together. This is usually performed while
minimizing any vertical motion, sometime referred to as a
static mode. (4) The magnetic flux density is determined as the
ratio of the measured generated voltage and the velocity of the
moving coil, often referred to as the dynamic mode. (5) Since
the magnetic field is not uniform across the z-axis motion range
of the coil, various signal processing methods fit the curve to
extract a value correlated to a certain weighing position, i.e.
to apply the best gravity acceleration value. One experiment
has attempted to measure both (4) and (5) simultaneously, but
they still are concerned with fitting the field profile.
These five components are the basics of the watt balance
techniques, and are described in the following sections.
As mentioned earlier, there are peripheral systems that are
also in common, but these will not be discussed. The
following technical discussion may be apparently obvious
to precision metrologists already working on watt balances,
but not to others outside this field, so consider this
a compromise summary touching on both the easy and
expert details. In the long run, these issues will have
to be understood by the combined physicist/electrical and
mechanical engineer/metrologist/systems programmer who
will be operating the next generation SI mass balance.

(25)

It is interesting to see that although there are three frequency
variables involved (more when including timing instruments,
lasers in position and gravity interferometers), the definition
reduces to fundamental constants h/c2 , and a linear dependence
upon the SI definition of frequency. The scale factor K
represents the combined measurement variables that are
obtained through the watt balance from units of time, length,
volt and ohm, relating a test mass m to SI kilograms units.
One day h will be defined as a fixed number, as c is already
defined, derived from h measurements against the present day
IPK. This will make IPK equal to 1 kg on that day, and subject
to drift forever after.

5.2. The magnetic field
The magnetic field source specifications were described earlier.
To summarize, fields are designed to have a radial 1/r gradient.
This is generally optimal at only one position along the line
of coil travel or along a section of travel, depending upon the
construction of the magnet. The flux density profile should
be reasonably uniform along the length of coil travel. If
there is a point of minimum slope near the middle of the coil
travel, this is a good place to conduct force measurements. A
sample magnetic profile is shown in figure 11. The shape
and size of the induction coil contributes to the magnetic
field profile. A tall and thin coil will average the vertical
field variations better but may extend into the edge field for
a faster drop off, limiting the travel range. A short and
wider coil will have a longer travel range but may have
higher order variations. It might extend outside the width
of an optimal 1/r radius, for the superconducting magnet,
or be too close and heat the permanent magnet surface. The
NIST magnet is the only superconducting solenoid; all other
sources are made of a rare earth composite, strong magnets

5. The watt balance systems—common details
5.1. Common traits
This section commences the more technically specific part of
this paper, comprising an attempt to summarize some aspects
of each operating system. Even as long as it is, it is still
only a taste of the complexity of these systems. In 2012
there are five national measurement institutions (NMIs) that
are operating watt balance experiments (NPL/NRC, NIST,
METAS, LNE and BIPM), one laboratory researching a major
17

## PDF page 19

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

procedure starts with establishing the perpendicularity of the
magnetic field with respect to gravity. No matter what the
source, tests have shown that the magnetic field is not perfectly
symmetric around 360◦ , whether from magnet construction
asymmetries or the earth’s field, so some choice for an
‘average’ vertical has to be made. Each laboratory has
specially designed instruments for measuring the field vector
relative to gravity and for adjusting the magnet to optimize the
alignment. This adjustment is time consuming, but is stable
for long periods of time, i.e. six months or longer, sometimes
showing some seasonal dependence.
An imperfectly aligned coil complicates the reality of the
simple watt power calculation of equation (17). Off-axis terms
of lateral or rotational motions of the induction coil contribute
extra forces or voltages, as identified in the Stenbakken 1996
analysis [99]. Not only are there magnetic forces that move
the coil laterally in the x- or y-direction and torque vectors,
τ , to rotate the coil around these same axes by an angle,
ω but the coil may have these motions excited from tension
in mechanical connections during the dynamic motion phase.
The more complete power, P , formulation takes the vector
nature of the force and velocity into account P = F · v + τ · ω .
For the NIST balance, tests to characterize these off axis terms
were described in [100]. It is not trivial to picture the product
terms, since the force and motion do not occur simultaneously
in most watt balance systems.
Figure 12 shows possible coil motions as they occur during
the dynamic and static modes. The two motions are not
to scale and are exaggerated. As the coil moves vertically
in figure 12(a) over a range, δz, and a time, δt, so that
vz = δz/δt, it also may have lateral velocities, vx , vy , and
angular velocities, δωx /δt, δωy /δt. The mechanical causes of
these motions are dependent upon the support and lever arm
construction. These motions contribute extra voltage to the
ratio ε/vz . If the motion is not linear over the entire vertical
run, such as a cosine term for a lever arm beam, this may add
more complications.
Figure 12(b) shows coil motions that may occur during
the ‘static’ force part of the measurement, where the coil
may still have some off z-axis motion. The causes for lateral
and angular motion of the coil are part electromagnetic, and
part mechanical. The electromagnetic aspects arise from the
alignment of the coil’s CM with respect to the magnetic field,
and also with the effective electromagnetic center (EMC). If
the coil is tilted with respect to the magnetic field, the coil will
move laterally, δXF , δYF , from forces dependent upon the
field gradients in the different directions, Fx , Fy . If the CM is
offset from the EMC, then the coil will experience torques τx ,
τy , when current is injected, leading to angular rotations, δβx ,
δβy , about the x- and y-axes, respectively. With the radial
uniformity of the magnetic field, there is negligible torque
generated around the z-axis.
Dimensional measures and bubble levels are only good
for a coarse adjustment of the coil alignment. All laboratories
use a separate X–Y displacement and tilt sensor system to
quantitatively measure these displacements. In most, the coil
is aligned by using this system to record the motion resulting
from the injecting current, while the balance is locked, then the

Figure 11. Calculated magnetic flux intensity profile along z-axis
(an example from NIST).

embedded in iron shells. Major contrasts between these two
radically different sources include: control of temperature
stability for permanent magnets versus current stabilization
for electromagnets, induction coil closeness to the temperature
sensitive magnet surfaces versus magnetic flux trapping in the
superconductor, the open versus closed coil region, costs from
cryogenic fluids or electric power for refrigerators versus single
field nature, large weight and the possible surface oxidation of
permanent magnets.
Environmental variations affect both sources. Temperature dependences for the solenoid mostly affect the current
control, mentioned in [121]. Atmospheric pressure affects the
liquid helium temperature, and liquid evaporation changes the
height of the liquid in the Dewar. Both of these cause small
dimensional changes in the solenoid. A permanent magnet
is generally very sensitive to temperature, being either heated
by the environment or the induction coil. The large mass of
this magnet system acts to ballast against sudden temperature
changes, but it may take days to achieve equilibrium after a
major change.
Nonlinear hysteresis is a potential problem for each
type of field source, but from different physics principles.
Diamagnetic effects, radio frequency pickup, or trapped flux in
a superconductor leads to excessive noise or an offset. Similar
effects from magnetic domain shifts or temperature changes
occur in permanent magnets. Field changes in the coil will
induce first and possibly second order changes in the source
field. Fast current switching will induce large field changes that
may have long relaxation times. Testing with different mass
values, that is, different induction currents, is a check for many
of these effects. A solenoid also allows some independent
checks, since its field can be more easily varied, turned off or
even reversed.
5.3. Alignment issues
5.3.1. Magnet and coil alignments. After building a watt
balance, the first order of business before recording valid data is
to perform basic alignments. The acceleration of gravity vector
defines the primary vector direction (z-axis), so the alignment
18

## PDF page 20

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 12. Coil motions causing misalignment errors. (a) Dynamic mode: lateral velocity δX/δt and angular rotation δωy /δt of the coil.
(b) Static mode, mass off F1 and on F2: lateral motion δXF 1,F 2 and δZF 1,F 2 and angular change δβy1,y2 . β0 is the angle of the coil relative to
the magnetic field, which may not be zero.

plate or when the vacuum hood is set on the view plate base.
Laser alignment procedures differ with each laboratory, not
all have automated alignment systems. Interferometer beams
are normally several millimeters in diameter to prevent edge
diffraction at the detectors and focused at infinity. Beam lines
for a small scale system may have laser travel lines that are too
short to create angular displacements wide enough to measure
by eye, so to check the beam overlap, they are often narrowed
with a pinhole. Some procedures employ deflecting mirrors
to lengthen the beam lines or direct the beams into alignment
telescopes. Checking the verticality of the X–Y axis motion
sensor system is also needed, if an optical laser system is
employed.
The optical center of the z-axis interferometer must be
aligned with the CM of the coil to avoid Abbe offset errors.
A coil will move during the vertical travel at the resonance
frequency of the swinging or tilting modes. An Abbe offset
error will cause excess recorded motion of the coil along
the z-axis correlated with the ω rotations. Methods to
adjust the reflector position (one central reflector) or calculate
a correction term (three radius reflectors) use tilting (or
swinging) of the coil to induce rotations, ωx or ωy . Uncorrected
Abbe errors create excess noise in the velocity and will
interfere with the precision analysis of the magnetic field
profile (described in following section 5.5). An Abbe offset
will also compound the errors from any real δωx,y /δt terms.

coil is translated or tilted to null the motion. An X–Y sensor
system is also useful to re-center or level the coil, or if desired,
to actively damp swinging and tilting motions in free hanging
coils. This sensor system varies with the different laboratories.
Some laboratories use a fixed location method, such as an
optical slot, to reestablish the coil to a previous position. Laser
or capacitive position-sensitive detectors usually comprise the
X–Y positioning systems.
5.3.2. Obtaining alignment corrections. Knowing the
misaligned displacement of the coil is not enough. A
misalignment correction will be proportional to the magnetic
field gradient in the appropriate direction. A useful procedure
to determine the gradients of the lateral, δFx /δx and δFy /δy,
is available if the coil can be displaced by an external
means, such as a translation table to move the entire coil and
balance beam structure, or moving the magnet. Perpendicular
displacements are needed since the magnetic field is not
azimuthally symmetric. In measuring the ratio ε/v in the
dynamic mode, this ratio is proportional to the force Fz .
If the coil is intentionally translated away from a defined
center by a known distance, such as along the x-axis, the
subsequently measured ratio (ε/v)x differs from the centered
ratio by the field gradient, proportional to δFx /δx. All
other misalignment motions should be equal and can be
ignored. Similarly, having a method to tilt the coil and perform
similar velocity measurements results in gradient values for the
torques, δτx /δβx , δτy /δβy .

5.4. Force and current mode
This mode is analogous to the absolute ampere experiment,
measuring the ratio of force to current. In all but one of
the present watt balance schemes this is a stand-alone mode,
but there are aspects that are common to all systems. The
electric circuit is shown in figure 13. Current, I , injected
into a coil with inductance, Lm , generates a vertical force to
balance the gravitational force on a test mass added to the
balance. The current is measured as the voltage drop across a
calibrated resistor, ε1 /R. A voltage standard is wired in series
opposition so that the DVM or pre-amp measures only small
voltage differences. The mechanical force is derived from the
calibrated test mass value, m, and the acceleration of gravity, g.
The best way to measure voltage (and by extension,
current) is to reverse the same current without changing other
parts of the circuit. In subtracting the results, any instrumental

5.3.3. Optical alignments. There are many concerns that are
familiar to laser optics users, but the most important is the
verticality of the interferometer laser beams recording the zaxis position of the coil. An interferometry angle misalignment
causes a cosine dependent error in any quantitative value for
the velocity along the line of coil travel. A laser misalignment
angle of 0.05 mrad contributes an error of 1.25 × 10−9 in
velocity, from the cos(x) expansion 1 − 1/2x 2 . The alignment
procedure is more tedious with multiple numbers of beams
(one central reflector versus three reflectors at the coil radius).
An extra correction to the alignment is needed if the beam
injection point originates outside the chamber and goes through
a view plate into a vacuum chamber. This angular distortion
may change due to the pressure difference across the view
19

## PDF page 21

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

meters record a baseline value for the acceleration of gravity
somewhere in the laboratory. Gravity cannot be directly
measured at the mass location once the balance apparatus
is built, so a gravity transfer meter is needed, moving from
the absolute meter locale to near the test mass location to
transfer the baseline value. There is a relative decrease in
gravity of nearly 1 × 10−6 for a 3 m vertical change of one
floor in elevation. A transfer meter is also necessary to
determine the local vertical gradient, which is approximately
−3.14 µGal cm−1 (Gal unit = cm s−2 ). A gradient correction
at the test mass locale will also be needed, since the transfer
meter may not be at the same height as the test mass. The local
gravity gradient has a slight significance in correcting for zaxis excursions or the varying CM height for differently shaped
and sized test masses. Motions of nearby large masses, such
as vacuum chamber hoods, must be accounted for. Absolute
gravity meters, be they fickle mechanical or extremely complex
atom levitation instruments, are not usually active in real
time with watt balance testing, so established tidal modeling
programs are used to calculate changes from the local baseline
value. Tidal related changes up to several parts in 107 are
applied to each force point, or each series of points, if taken
quickly enough. More than an order of magnitude smaller yet,
atmospheric pressure also affects gravity acceleration, even in
a vacuum, due to the density variations of the atmosphere above
the apparatus. Gravity variations related to ocean loading or
water table fluctuations are not negligible, but results for Planck
constant determinations average data over months to years, so
these more rapid changes are a statistical concern for a future
mass calibration system that would be expected to calibrate
masses in much shorter time frames.
For the current values, high precision reference resistors
are maintained in a constant temperature bath. Any corrections
arise from drift due to aging of the resistors, and air or oil
level pressure effects in certain resistor constructions. Resistor
values are chosen so that the voltage drop of the current is
at a high and convenient value, equal to a standard voltage
source, yet not so large that temperature or power coefficients
will contribute to ohmic heating offsets from larger current.
Newer Josephson voltage systems allow flexibility in picking
the combination of resistor value and voltage drop over the
original designs limited by 1.018 V standards. High resistance
insulation on the wires to the coil and to the resistor is
important in preventing current leakage paths, either to the
ground or in shorts across the circuit. Although leakage in the
resistance circuit is a problem, the wire insulation on the coil
windings, i.e. leakage across the coil, is not a problem, except
the insulation cannot demonstrate time dependent dielectric
adsorption.
It is hard to completely enclose the magnetic field from the
source magnet or the induction coil, so this will cause problems
of varying degrees. Ferromagnetic components in a fixed
position nearby will not directly affect the force measurement,
but may distort the field and alter the magnet alignment that was
so carefully performed before the test operation. It is important
to avoid magnetic materials in the construction of any moving
parts on the balance apparatus, since any interaction with
the field will be hysteretic and irreproducible. Poor quality

Figure 13. Equivalent circuits for measurement modes, with digital
voltmeter (DVM), voltage standard VR , moving induction coil Lm .
Static mode—resistor R, voltage drop ε1 .

offset drops out. A way to reverse currents and keep the forces
balanced is with the use of a tare weight of half the test mass
reference. To picture this, refer to a simple balance system
configuration as portrayed figure 7. The tare mass is placed
on the counter weight side of the balance arm. While the main
test mass is still off, the current to maintain the balance is
half the magnitude that would otherwise be needed to balance
the test mass directly, εoff /R. The tare weight is left in place
when placing the test mass reference onto the main coil side.
With the test mass on, the current is reversed, εon /R. Noting
that there is a sign reversal with the current, εon ≈ −εoff ,
the difference, (εon − εoff )/R, of the measurements gives a
total change of two times the individual current level. This
eliminates any residual offsets, including instrumental bias,
thermal electromotive voltages, or current needed to maintain
balance with no masses. As long as the tare mass position does
not change, its gravitational force or tension on the balance
structure drops out, so the total change of force is mg. The
result is a point F /I = mg/[(εon − εoff )/R], valid at B(z)L.
This procedural description appears simple, but not in
precision metrology. At the required accuracy of 1 part in 108 ,
certain effects are non-negligible. The next sections describe
the added complexity needed in obtaining a higher precision
value, in this case, for mg/[(εon − εoff )/R]. Addressed in the
following section are some relevant concerns involving the tare
mass type and value, changes in the acceleration of gravity,
standard resistor corrections and the magnetic susceptibility
of the test mass artifact. There is then a discussion about the
coil interaction with the source magnet, followed by a section
delving deeper into specific examples of existing balance
structures that caused unanticipated problems.
5.4.1. Force and current corrections, and mass material
properties. There are significant adjustments to the force-tocurrent ratio measurement of the force mode. As mentioned
earlier, gravity systems and corrections will not be discussed in
detail here, instead refer to a review by Faller [101] and to the
individual NMI reports for more information. Absolute gravity
20

## PDF page 22

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

stainless steel and ‘nonmagnetic’ brass are likely to become
magnetized over a long time. If the magnetic field is strong
enough, it will also affect the test mass. For this reason, several
of the experiments have tried material alternatives to highest
quality PtIr or cheaper steel.
In ending this section by mentioning adverse magnetic
interactions, it is appropriate to continue the next section on
the topic of the complications within the desirable magnetic
interaction between the magnetic field and the induction coil.

values, a bevy of tare masses must be available. A complicated
system to operate with multiple mass values in a vacuum and
yet maintain small balance offsets has not yet been built. This
may all seem trivial, but if the offset current gets out of hand, it
complicates the program feedback control and may have other
effects on the magnetic field interaction.
Placement of the main reference mass onto or off the
mass pan is one of the more difficult programming control
routines. The motion of the coil should be controlled as
tightly as possible, both as the mass is being placed and
during data acquisition. To give an idea of just how tight,
electronic feedback routines are capable of controlling the coil
position to about 10 nm for NIST and NPL, and in-air control
at 200 nm for METAS. The test mass location relative to the
coil is usually measured with a separate control and motion
drive system. For a freely rotating balance beam, once the
mass touches the pan, a finite control response in changing
the current allows some motion of the balance during the large
change of force. This motion in turn leads to mechanical stress
variations and hysteretic forces in the balance pivot, whether
knife edge or thin flexures. Coil motion is additionally hard to
control, because as the mass lands on or leaves its support, the
tension changes, the support exhibits dimension contraction
or expansion, the coil suspension rods contract or expand in
response to the force and subsequently there is a lot of motion
to control.
Faster feedback by quickly ramping the current in the coil
to the anticipated level generates a large field pulse from a
dI /dt contribution. This pulse induces a reflective shift in the
source magnet. In a related complication, a mass placement
does not reproduce the exact same motion each time. A
procedure to erase this hysteresis is a programmed movement
of the balance arm, up and down in a damped oscillation. This
relieves induced stresses and ends with a reproducible history
of pivot motion. However, in moving the coil to erase the
pivot hysteresis, there is a trade off. The fully magnetized
coil interacts strongly at the full coupling force on the source
magnet, inducing a magnetic hysteresis, which in this case
includes a sign reversal. If the feedback program can control
the position during and after mass placement to a few tens of
micrometers, then a slightly larger and controlled slow motion
effectively reduces the combined magnetic and pivot hysteretic
effects.
To alleviate some hysteresis, the balance beam could
be locked into position during mass placement, or separated
from the balance lever arm, using a mass comparator to
measure residual forces in the balance. However, the locking
or separation process can induce irreproducible mechanical
stresses itself.
It has been mentioned in passing that the source magnetic
field is not constant, as the original derivation assumed, but
instead interacts with the magnetic field of the induction
coil. To conclude this section, here is a brief discussion on
the question about the accuracy of this current measurement
procedure. The suspicion is that B(z)L in the equation
mg/[(εon − εoff )/R] = B(z)L may not equal the B(z)L term
when there is no force interaction with the coil.

5.4.2. Magnetic field interactions. In this section, the force
mode analysis is treated from the perspective of making a static
measurement. In this procedure, a current in the main coil is
servo-controlled to maintain the coil at a preferred position
within the magnetic field, normally the flat spot in the center
of the magnetic flux density profile, as seen in figure 11. This
not only puts the coil at a known position for the applicable
gravity corrections, but the static balance point also reduces
hysteretic forces from the friction and mechanical distortion in
the lever arm pivot center and multiple pivot points of the coil
and mass supports. The flatness of the profile helps the control
routine with a linear feedback and reduces noise from tiny coil
or magnet vibrations. Current recordings are usually limited
to a minute or two. Recording time is a trade-off between
quicker reversals to ensure the magnetic flux intensity drift is
treatable as linear, and longer integration times to average out
the signal noise. Reversal frequency is limited by the time it
takes to place the mass and achieve a stable position control.
This can be several minutes.
The most desirable measurement would result from a
perfect current reversal, but this cannot occur in a static
force mode. There is a base offset current due to any
amount of unbalance between the coil and its counter mass
equivalent, even without masses on the balance. Even if
the coil starts out perfectly balanced before going under the
vacuum, trapped air will evaporate once the vacuum pumping
is started, and there is likely to be a lot of it in the coil windings.
An electronically controlled, micro-adjustment system can
compensate for balance offsets, but system additions add
complexity and possibly other adverse effects, e.g., stepper
motors that use magnets and high voltage piezo-actuators may
be susceptible to vacuum arcing.
Another cause of an offset current is when the tare mass
value does not equal half the test mass value. Mass metrology
labs go to great effort to accurately compensate buoyancy in
mass comparisons. In general, an expensive weight standard
of the same density especially selected as a tare mass could be
very close to half the main test mass. However, since the tare
mass does not enter into the measurement equation, this is an
unnecessary expense. The tare mass does not need to be either
the highest quality or of a high density. Aluminum is good
for its nonmagnetic properties but its low density complicates
choosing an appropriate one. Common practice calls for using
an inexpensive balance to check the tare mass value. The large
buoyancy correction between aluminum and a more accurately
measured, high density test mass makes it difficult to find one
exactly half of the main reference. Then also, in a future system
capable of alternating among multiple and varied test mass
21

## PDF page 23

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 14. Diagram showing potential offsets caused by mechanical misalignment issues. (a) The balance aligned with tare mass on the
balance pan. (b) Main mass added to pan and balanced with force on the coil. Note the central pedestal tilt from transferring the test mass to
the pan. See text for explanation of alignment changes.

In [102], a model is presented for the general form of the
magnetic flux intensity coefficients for a permanent magnet as
B = B0 (1 + C1 I + C2 I 2 ),

offset errors. The schematic picture of figure 14 is a composite
of the NIST and NPL balance construction, but is sufficient to
illustrate common misalignments. Note how the coil connects
to the balance beam, the balance beam sets on a pedestal, and
the mass mover mechanisms also attach to the pedestal. The
coil is reasonably free to swing and tilt, and the mass pans are
also freely hanging. Although NIST uses a wheel instead of a
beam, the effects are similar.
Before commenting on the misalignment, note there is
the nice feature of a ‘loose’ system, where the mass pan is
allowed to swing. As the mass is added to the pan, it may
be off-line from the CM of the coil and support assembly. A
pan connected by a flexure or knife edge to the upper support
structure, will tilt to align its CM with the coil. Upon re-lifting
the mass, its position on the mover platform is shifted. Then
its subsequent placement on the pan is closer to the CM line.
Once centered, the coil position is stable. This self-centering
works with flat bottom masses, and thus spherical mass shapes
would have to rely on pre-centered support points.
To now focus on a second major cause of coil
misalignment, note that an off-center test mass causes the coil
to translate by dx. If the pan support flexure is off-line from
the coil CM, the test mass will always induce a translation.
Thus there can be two different causes of coil misalignment,
one influenced by the mass on/off position and another by
effects of plus/minus current-induced forces. Thus aligning
the mass pan is generally done without a current in the coil,
while aligning the coil is done without exchanging the mass,
all while the balance vertical motion is restricted.
A subtle effect that was not recognized in the
original balance designs arose from the redistribution of
the test mass and forces within the total assembly. This
small redistribution alters the properly aligned balance
configurations of figure 14(a), where at the start the inductor
coil is centered and level in the magnetic field, the balance
arm is level and the pedestal support is vertical. The tare mass
reference is on its mass pan; the reference mass is supported
on the pedestal. The length of the rods on the main coil side
is L2, from the pan support to the coil. Two different things
happen depending upon where the interferometer reflector is

(26)

where I is the current in the induction coil, B0 the unperturbed
magnetic field, with coefficients C1 for a linear response term,
and C2 for a term that does not reverse with the current.
The estimated coefficients for the NPL magnet were tested
by unbalancing the system, where the difference between the
magnitudes of −I and +I is a large δ. The total change in
current is Itot = 2I (1 + δ). C1 was extrapolated as 2 ×
10−7 mA−1 . By testing different mass values, the contribution
of C2 I 2 δ 2 was deemed less than 10 nW/W for δ less than 0.1%.
This would thus only be significant for a large tare mass plus
a balance offset difference from the desired m/2.
This model was meant to treat nonlinear terms as simply
related to the current amplitude. Whether this model is
sufficient to address more complex changes in the magnetic
field that occur due to the interaction of the two magnetic fields
and changes of the current amplitude is a subject beyond the
scope of this paper, but should be explored, especially as it
is expected that all NMI’s will eventually adopt permanent
magnet sources.
A 2004 test on the NIST system attempted to test the nature
of the source magnet under current reversal by using fixed coils
to mimic the induction coil and its current reversal forces on
the solenoid while measuring the average change of force on
the main coil. A result cited in [97] mentions a possible noncancelling term of 5×10−8 , which at the time was presumed an
effect of the diamagnetism of the superconductor. Tests with
better sensitivity later in 2005 reduced this term to 1.5 × 10−8 .
An additional test is presently being conducted with different
current magnitudes, and would be useful in comparing the
various test routines.
5.4.3. Kinematics and misalignment issues. Finally, this
discussion on the force measurement and mass placement will
conclude with a specific example of a kinematics issue that
was similar in two balance systems, but had different possible
22

## PDF page 24

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

connected. For the upper dashed line, the mirror is fixed to the
upper support connection and to the band such that, whether or
not the test mass is on the pan, there is no significant distortion
to change the length of the mirror connection relative to the
balance arm connection. The alternative is the lower dashed
line where the mirror is fixed more closely to the coil and the
length of the mirror relative to the arm connection point will
vary with the test mass placement. The length Z represents a
length between the two mirrors, equivalent to the length of the
coil support rods (which are already stretched by the tension in
balancing the tare mass, but this does not matter at this point).
The reason for placing the mass mover mechanisms on
the same support pedestal is the convenience in being able to
reposition the induction coil laterally within the magnetic field.
If all moving parts are supported on one pedestal, a translation
stage underneath will keep the movers in line with the pans.
Otherwise, translating the coil independent of the mover means
the mover-to-pan edges may no longer have enough clearance
to work properly. Most existing mover interfaces use a mass
platform on rods that extend through the center of the pan. A
robotic gripper arm and a visual placement scheme would add
complexity but be independent of changes in the pan position.
However, one problem occurs regardless of mirror
position. In figure 14(b), the main reference mass is added
to the main side pan. This transfers the mass from a lever
arm extending away from the pedestal onto the balance. The
mass redistribution adds a torque to the pedestal, which rotates
counterclockwise. The base of the pivot point, whether flexure
or knife edge flat, experiences a tilt of d . This implies a
change in the force of the pivot point from the previous massoff measurement. An easy fix is to have an extra mass on the
counter mass side and take it off the pedestal whenever the
main mass is transferred to the pan.
A second problem arises depending upon mirror
placement.
The coil rod length contracts when the
electromagnetic balancing force in the coil pushes on the
support rods to balance the added test mass. In the case
shown, the tension along L2 compresses it by dzF and shortens
the length from the original Z to Z − dzF . If the reference
mirror is affixed to the upper support, there is no change in
the control position, since the tension on the balance pivot and
drop band do not change, which is the NIST configuration.
This maintains the angle of the balance arm and pivot point.
The coil does change its position relative to the magnetic field,
so the average of the positions must be corrected relative to the
profile as measured without current.
However, if the mirror on the coil is used to restore
the coil’s position in the field, as in the NPL system,
the dzF displacement causes the balance arm to rotate
counterclockwise by angle dθ. Depending upon the materials,
the length of the support rods and the force coefficient relative
to the pivot angle, this dθ change may be large enough to
significantly alter the force within the pivot and along the
balance beam or lead to an added distortion effect.
All existing systems may have some other subtle effects
depending upon the shape of the balance arm. A straight-arm
beam will have a cosine horizontal motion, and thus a vx term
in the velocity mode. More complex motions occur if the

Figure 15. Dynamic, or motion mode circuit. The main coil has
inductance Lm . Fixed inductors Lf are wired in series opposition in
some systems.

connection to the arm is not a flexure, such as a band rolling
off a wheel or a bar rolling against the curved arm ends. Small
irregularities in the curved surface will cause localized changes
in the lever arm length. Other multiple-flexure connected arms
will have non-vertical travel that might be difficult to adjust due
to the complexity.
Another complication may arise from the practice of
placing the tare mass on the counter mass side. This method
effectively adds a net force to the balance, equal to the test
mass, and tension to the beam. Some systems avoid this by
adding a mass comparator to the coil structure and weighing
the differences between the mass and coil forces. Another
alternative not yet tried is to start with a system balanced with
the tare mass on the main mass side. Removing the tare mass
requires the same current as adding the tare to the counter mass
side. The tension on the pivot point, balance arm and support
band to the mass pan are kept equal, although the coil will still
drop a bit. Unfortunately, this procedure requires more space
on the main mass side to accommodate one complex, or two
simpler, mass movers.
There are other aspects of the force mode, but they are too
system-specific to be easily summarized. It is time to consider
the measurement that resolves the B(z0 )L term.
5.5. Voltage and velocity mode
When the coil is moved along the vertical z-axis, the motion
induces a voltage across the coil. This mode is generally
known as the dynamic mode. The electrical circuit is shown
in figure 15, where the simplest circuit uses only the same
single induction coil. Several variations of the circuit were,
or are, in use. One or two fixed coils with a total inductance
approximately equal to the main Lm may be wired in series
opposition to cancel common external ac signals. They are not
used in enclosed permanent magnets, which are more shielded
from the ac background,. The induction coil is connected to
a high impedance voltmeter, in some cases through a preamplifier, so that negligible current passes through the coil.
The ratio of the induced voltage, ε2 , to the coil velocity, v,
equals the magnetic flux B(z)L of the unperturbed source
magnet.
23

## PDF page 25

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

The NMIs have similar measurement techniques in
common. It is vital to choose a proper point for the reference
arm interferometer reflector for measuring the motion of the
coil. With a single coil, the reference mirror must be attached
to the magnet surface or else the magnet’s motion will induce
voltages uncorrelated with the coil’s motion relative to the
magnet. A reference mirror attached to fixed coils will cancel
the common motion of the magnet.
A position interferometer reads the number of fringe
crossings and these must be time stamped. The velocities
are generally calculated from the position changes in time,
recording two endpoint positions and times. The calculated
average velocity integrates over any vibrations. For Doppler
frequency measurement, the resolution is usually too low
or noisy, especially if vibrations overlay the coil’s normally
constant velocity. One proposed velocity measurement system
employs a very tight motion control scheme that also reduces
vibrations, maintaining a velocity constant to parts in 109 .
Doppler measurement can then be integrated over long time
spans to improve the precision. On most systems where large
vibrations in the coil are present, the velocity is controlled at
an average speed.
Voltage points are measured over integration periods,
where the endpoint times of these periods must be
synchronized with position points and times of the
interferometer readings. This integrated voltage averages
any vibration-induced higher frequency signals. Ideally there
is a perfect correlation between the integrated voltage and
the average velocity. In reality, the inductance-capacitance
delay time of the coil, the frequency response of the pre-amp,
the voltmeter trigger response time and the alignment of the
interferometer’s optical center with the EMC (an effect related
to the Abbé offset) will add either noise or an offset.
A magnetic flux intensity that is not uniform along the
travel length z has subtle effects depending upon whether the
coil motion is controlled to either constant velocity or constant
voltage. Constant velocity minimizes some issues, such as the
laser polarization mixing or trigger timing variations. Also,
the timing resolution may be improved by recording very
regularly occurring interferometer fringe signals. On the
other hand, controlling to a constant voltage allows a near
null voltage difference measurement between the coil and
reference standard, minimizing corrections for the gain error
and linearity of the DVM or pre-amp.
The drive mechanism itself may be a problem. Whether
electromagnetic, screw driven, or electrostatic, some form of
magnetic or electrostatic field is applied; thus stray fields can
produce extraneous offsets or noise. Mechanisms to move the
coil differ greatly and there is no consensus on which method
is superior. As long as they are well correlated, voltage and
velocity signals with higher frequency components will still
provide a low noise ε2 /v ratio. Vibrations from the drive
mechanism, or simply in the background, will induce motion
in the coil or magnet. The accuracy of the optical detection
system and the voltmeter response tends to deteriorate as the
frequency increases. And the higher vibration noise may hide
very low frequency variations along the magnetic field that
are real. Accumulating more points along the profile curve

Figure 16. Magnetic flux intensity as indicated by the profile curve
of ε/v along the line of travel, showing noise in data.

will allow characterization of short, localized flux intensity
variations, but the relatively short DVM recording periods,
typically tens of milliseconds to tenths of a second are at
the expense of digital resolution. Longer integration times
add digital resolution at the expense of smoothing over the
coarse curvature of the profile. The interferometer timing of
fringe edges is highly dependent upon the purity of the laser
detector signals. The timing of the interferometer fringing
requires below a nanosecond precision. Different schemes
have been designed to increase resolution or reduce noise, but
the resolution of a single ε2 /v ratio point for any NMI system
has yet to satisfy the requirement of determining the value of
B(z0 )L to a few parts in 108 . Thus, it is necessary to record
many points along the B(z)L profile and perform some signal
processing.
5.6. Magnetic profile analysis
The ε/v profile is recorded from consecutive pairs of motion,
one in a down direction generating a voltage of one sign,
followed by an up direction generating the opposite sign.
Since the velocity sign is also reversed, a simple average of
consecutive up/down ratios will eliminate the instrument and
thermal voltage offsets. A simple average of values sounds
simple, except there are a lot of points, all but a few at a
far distant position from the desired center, as shown in the
magnetic flux intensity profile curve of figure 16. The noise and
discrete resolution in the voltmeter and the velocity instruments
contribute a large scatter in consecutive points, on the order of
1 part in 105 . In this example, the force is recorded near the
center of the curve at 5 cm. A simple average across the curve
results in a gross error compared to the center point value where
the force measurement was recorded. Using only a single or
even a few ε2 /v ratio points that corresponds to the center
force position is much better, but not good enough to provide
sufficient precision, and all the rest of the points are useless. It
is possible to achieve a resolution of the ratio value at the force
mode center of a few parts in 108 , but a complicated signal
analysis is needed.
24

## PDF page 26

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

value. A one step analysis, fitting and averaging the center
values over multiple curves, reduces the center ratio noise by
a factor of 50. An additional factor of 10 or more is possible
from the two step curve normalizing analysis. For 10 passes
(five pairs of up/down), the noise of the ε/v ratio approaches
10−8 relative to the center ratio, typically limited by the drift
of the magnetic field.

5.6.1. Signal processing—curve fitting. It is necessary to
obtain a value for B(z0 )L at a certain position z0 . The next
step after the two simple approaches mentioned so far considers
fitting the curve to a polynomial, typically of at least 6th
order, then calculating a value for the weighing position using
the fit coefficients. This third step is better yet, and is the
usual method applied. However, this may not be the most
optimal method. From Taylor’s theorem expansion, a complex
curve can be more accurately approximated for points around
a specific origin with higher order polynomials. In the case
of B(z)L, the true function is unknown. Noise in the data
points limits the accuracy of estimating the true curve with
higher order polynomial fitting, since the fitting procedure
cannot distinguish between a simple curve with noise and a
noiseless but complex curve. Thus, by keeping the fitting
order low, the points recorded away from the center contribute
less weight to the precision of the fitting coefficients at the
center. One way to decrease the uncertainty of the simple
polynomial approximation is to average a very high number
of velocity passes. This slowly reduces the uncertainty at the
expense of taking many, many velocity sweeps. That adds
a time drift component to the overall average. Questions also
arise concerning the optimum fit order. Do small eccentricities
exist underneath the noise? When does a higher order fit simply
reflect the local noise variations?
Performing the third step mentioned above with a fourth
step is a method used at NIST to reduce the type A noise of the
calculated ε/v ratio to within the desired few parts in 108 . It
does so with a smaller group of velocity traces that converges
more rapidly than simply averaging the extrapolated fit. A
watt data point is based on a series of ε/v groups of 5–20
pairs, interspersed with 5 or so pairs of force measurements.
A twelve-hour data set is about 12 groups of force and 13
groups of velocity sets. Each one of all the velocity curves is
fit to a relatively low order of 6, 8, or 10. An average of the
fit coefficients is accumulated over all of the several hundred
velocity sweeps. The assumption, observed as valid, is that the
form of the profile for all coefficients except the zero order does
not change over long periods of time, of many days or more.
The uncertainty of the fitting coefficients is reduced from using
hundreds of curves. In the fourth step, the averaged coefficients
are used to generate a model curve. Each individual data
curve is divided by the model profile, normalized to 1 at the
central weighing position, essentially eliminating the higher
order of each curve to its zero order component. This process
of normalizing each curve over the whole range of travel
reduces each data set to a flattened line representing the residual
differences from the global average, representing an average
magnitude of the magnetic flux intensity relative to the center.
A simple average of the flattened group of points reflects a very
precise estimation of the zero order coefficient from all the
points along the trace at the immediate time of measurement.
Using all the residual points from the entire curve reduces the
uncertainty by the square root of the high number of the whole
range of residual points, not just those few near the center.
Thus the noise converges much more quickly.
In the example of figure 16, the peak-to-peak noise at the
center for one curve is approximately 10−5 relative to the ratio

5.6.2. Limits to curve fitting. Analyzing the profile data
in this way still has some uncertainty components: it does
not definitively answer the question about whether there
are eccentricities buried in the noise. Such eccentricities
could occur in the permanent magnets from the machining
roughness of the dimensional gap faces or local magnetic
domain variations in the iron shell. In a solenoid, wiring
irregularities would do the same. Thus, measuring the force
mode ratio at one point might experience a local variation
that profile averaging does not reproduce. These would be
systematic errors in extrapolating from the curve fitting values.
Arguments have been made that if the induction coil is far
(tens of cm) from the magnetic source, as is the case for
the NIST superconducting solenoid, small perturbations from
construction inconsistencies will smooth out. This may not be
the case for permanent magnets where the distance of the coil
from the gap surface is less than 1 cm. The vertical length of
the coil is usually large compared to the expected cause of local
variations, so it is also argued that sufficient averaging occurs,
especially in long coils. A large scatter in the residual ε/v
ratio data points contributes an additional statistical uncertainty
component, related to the choice of fit order. The statistical
errors in higher order fitting will limit the validity of checking
for real local variations in the interpolated center value if the
variations are dominated by the data noise.
Thermally induced dimensional variations in the magnet
cause nonlinear drift rates in the flux intensity. Accumulating
data over many day-to-day data sets should average any
errors out over time, but this time frame is not well defined.
Measurement times in recording data sets for each mode are
typically within 1–2 h, so stabilizing the source magnet to
maintain a small, linear drift over day long runs is sufficient.
Nonlinear drift rates can be large over shorter times, typically
soon after evacuation or large thermal excursions of the room
environment.
The curve fit routine can be checked by measuring the
force ratio at different positions, well beyond the flat central
slope. This is not a perfect test, since coil alignment
characterizations, and possibly gravity corrections, are no
longer optimized. Also, the profile curvature is steeper so
that the position control is more difficult and the current
noisier. And there is always the concern that the BL terms,
as interpreted from the ε/v measurements, are simply not the
same when forces are applied to the coil and magnet system.
5.6.3. Simultaneous F/I and ε/v measurement. A group at
the BIPM, reported in [137], has worked on an alternative
method to avoid nonlinear, non-canceling BL terms. If
measurements of the F /I and ε/v are made simultaneously
on the same induction coil, there is no question of whether the
25

## PDF page 27

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

BL terms are the same, whether measured with a plus, minus,
or zero current in the coil. This is difficult to do with a resistive
coil, so ultimately a single superconducting coil was the plan.
The BIPM apparatus is described later, but it is easier to
consider the somewhat different watt equations in this section.
The following derivation is slightly simplified from those
in [166], but still assumes that measurements are made on a
single coil. The force mode consists of two step measurement
of B1 L and B2 L separated in time. The cause of any possible
change in flux intensity from B1 to B2 need not be specified.
Since there is no mode where the system is operated in a
‘balanced’ mode, there is no offset current term. A plus and
minus current is still needed to eliminate thermal emf offsets
and symmetry is desirable, so a tare mass of m1 is used,
assuming m1 ≈ m/2, where m is a test mass. In the first step,
a constant current I − is injected into the coil, nearly balancing
the tare mass. Since the current does not exactly balance
this mass, a load cell records the residual force. The coil is
moved at a constant velocity, otherwise the coil acceleration
includes forces besides gravity. Referring back to the form of
equation (18), the measurement becomes
Fz = e1 − m1 g = I1− Bz1 L1 ,

Figure 17. NPL balance and magnet (left), figure 8 induction coil
(right), 1988. Reproduced with permission from [111]. Copyright
1990 BIPM.

pivot is made negligible through the static measurement mode.
Under constant motion, the pivot knife edge or flexure will
have a residual force that will show up in the weighing.
Whether this can be compensated for or corrected remains to
be examined. Similarly, heating of the coil is an energy loss
path that may affect the measurement; normally this energy
loss is dissociated in the voltage-to-velocity measurement by
zero current input and the high impedance of the DVM.
Although elegantly simple in its basic principles, all the
details of this section have revealed a sophistication and complexity that makes this experiment hard to design and operate.
With this technical background now described, it is time discuss the watt balance systems that have been built, operated
and subsequently redesigned several times. The next section
summarizes the history and operating details of the present
crop of experiments trying to measure the Planck constant.

(27)

where ei is the load cell reading. Ideally, the current is
perfectly reversed; however, the resistance may change with
temperature, so the more general term is used in the second
step, where I + is injected and the test mass added to the balance
for a measurement equation
e2 + mg − m1 g = I2+ Bz2 L2 .

(28)

Taking the difference between equation (28) and (27) gives
(e2 − e1 + mg) = I1+ Bz1 L1 − I2− Bz2 L2 .

(29)

During both steps, the voltage to velocity ratio, εn /vn =
Bzn Ln , is also measured, with the up and down values
combined to eliminate the voltmeter offset such that the time n
coincides with subscripts 1 and 2 in equation (29). Presume for
now that this is measured independently from any voltage drop
due to the current. Dividing the right side by the left, replacing
Bzn Ln with the appropriate n values of εn /vn , and scaling the
watt units with equation (21), the result is essentially identical
to equation (22)
[
]
1
4(e1 − e2 − mg)
.
(30)
h=
I1+ vε11 − I2+ vε22
RK-90 KJ2-90

6. Individual experiments by NMI
6.1. NPL Great Britain 1980s—the first direct h value
The National Physical Laboratory (NPL) of Great Britain built
the first operational watt balance, reported in [106]. This first
apparatus, shown in figure 17, operated in air. The magnetic
field was formed between opposing poles of a Fe–Co–Ni–
A1 magnet [107] generating about 0.7 T between flat, parallel
faces. The temperature coefficient was 200 µK/K, controlled
by water-cooling to within 0.03 mK. The induction coil was
two square segments of 3362 turns, wound in series opposition,
which made the combined pickup uniform across the pole
faces, essentially recording the magnetic flux cutting across
the central wire segment. Moving up and down at about
2 mm s−1 to generate about 1 V, the ε/v ratio from top to bottom
was roughly parabolic. The magnitude changed from central
minimum to the edge by about 80 parts in 106 . Since the coil
configuration was also sensitive to vibrations, the coil was hung
from a massive and stiff beam, a lever arm balancing on a knife
edge. This provided leverage for motion control and reduced
vibrations from flexing in the arm. The coil and counter mass

Importantly here, there is no assumption that the values of
Bzn Ln at different times are identical to each other.
More recently Robinson at the NPL in 2012 [179]
described a simultaneous mode technique using a coil with
bifilar winding. Each parallel winding would in turn be
used for only current or voltage measurements. The analysis
shows a promising scheme that would eliminate the problem
of changes in the magnetic flux intensity, at the expense of a
procedure and equation that is considerably more complicated
than equation (30).
One question about the simultaneous procedure will need
to be addressed. Normally the friction in the balance arm
26

## PDF page 28

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

measurements. This was originally thought to be caused by a
beat note of the coil vibration voltages with the frequency of the
chopper stabilized pre-amplifier, and/or a phase delay of the
vibration position along the 3 m length of the rods. These were
in part true, but more complicated reasons were understood
only years later.
Static and dynamic modes were interspersed over hours of
measuring time. The signal analysis at this time was treated as
an integral of the ratios over the length of travel. The ε/v ratios
were measured along the full 5.9 cm z-axis travel, analyzed
over different segments to average out endpoint effects. F /I
points were measured at a single, static position. The profile
shape was modeled on data from a separate test performing
F /I measurements at various points along the line of travel,
repeating the measurement only occasionally over many days
or weeks. A 6th order simple polynomial was used to integrate
this profile curve and combined with the values obtained from
the ε/v ratio integral. The relative scatter of data within each
mode, and of the watt data, was about 1 × 10−6 .

hung at the arm ends, also on knife edges. A tare mass was
located on the counter mass side of the arm. A current of 1 mA
in the coil supported an initial test mass of 100 g. By 1988,
the test masses were 500 g and 1 kg. Many of these design
parameters have been duplicated in some form ever since.
Position detection used a Michelson interferometer with
the reference mirror attached to the magnet and the moving
mirror to the upper side of the low section of the figure 8
induction coil. Vertical travel misalignment was adjusted by
minimizing the first order harmonic response of the coil when
forced to swing at a vertical fixed position. Misalignments
other than laser alignment are not mentioned. The noise levels
of the ε/v ratio were about 1 × 10−6 p–p (peak-peak), F /I
about 0.3 × 10−6 p–p.
The first report of a measurement of h using this new direct
method was in [108], with a stated uncertainty of 0.55 parts in
106 . As a first result on a new system, already the uncertainty
was comparable to the best of the inferred values in table 1.
6.2. NBS 1980s—electromagnetic solenoid, a different
approach

6.3. 1988 h results—NPL, NBS

At the same time, the ampere balance was being converted to
the moving coil design at the National Institute of Standards
and Technology (NIST), then known as the National Bureau
of Standards (NBS), as reported in [109]. Instead of copying
the NPL magnet, they specially designed an electromagnetic
solenoid to create a radial magnetic field for use with a circular
induction coil. This first solenoid was two main, opposing
solenoids of copper wire wound on an aluminum form, with
smaller trim coils nearer the middle. It generated a 2.9 mT
field with 8 A, with oil cooling to rid the solenoid of 3 kW
of heat. The induction coil was 4956 turns of copper wire
wound on a cylindrical fiberglass-epoxy form, with a similar,
single fixed coil wired in series opposition to reduce 60 Hz of
ac pickup. A coil velocity of 0.667 mm s−1 generated 20 mV,
while 3.33 mA current balanced 15 g. The magnetic field
profile over a 7 cm travel range was an unevenly shouldered
M-shape. One shoulder peak, relatively higher by 250 × 10−6
was 3.5 cm below the center and the other 180×10−6 at 2.5 cm
above the center.
The NBS balance arm was a 61 cm wide by 2.5 cm
thick aluminum wheel with a thick steel band welded to the
perimeter, instead of a straight lever arm as on the NPL balance.
This style of wheel balance eliminated the lateral motion
induced by the cosine-error of the lever arm, making the coil
motion inherently more vertical. The coil and the counter mass
were held from thin metal bands connected to each side of the
wheel. The wheel pivoted on a single knife edge.
The coil was supported from three rods connected to a
triple arm support, connected in turn at the center to a wire
band rotating off the wheel. The coil position was measured
by a single laser interferometer connected to this triple arm, or
spider. The retro-reflector was closely centered with the band
support. Because of the tall solenoid, aluminum rods about
3 m long connected from the spider down to the induction coil.
It was apparent from the noise in the ε/v ratio measurements
that velocity points were not perfectly correlated to voltage

Results from these two experiments were published in time
for the adjustment of the electrical units in 1989, although it
was the NPL value that had the most weight in the adjustment.
In [110], the published result was 6.626 068 21(90)×10−34 J s,
with a combined relative uncertainty of 0.13×10−6 , the details
were reported later byKibble in 1990 [111]. In [112], a reported
difference between the NBS watt and SI accepted value was
−16.69 × 10−6 with an uncertainty of 1.3 × 10−6 . (All the
values at this time showed a big discrepancy in the Josephson
constant relative to the national volt standards, varying by
country before the 1990 adjustment, as mentioned earlier.) A
report in [113] took into account the conventions in use for the
NBS Josephson constant and the as-maintained ohm relative
to SI, reporting the NBS 1988 value as 6.626 070 4(88) ×
10−34 J s.
The evaluation of the relative uncertainty between these
two labs is instructive of the knowledge of the systems at the
time. The NPL signal magnitude was by far the larger of
the two, with their stronger magnet and 1 kg masses. Their
type A uncertainty was calculated as the standard deviation
of the mean for 50 points, with each datum taken as the
average of a day’s run of about 5 points. NBS used a 100 g
test weight and also averaged daily runs of about 12 points
per 12 h run. The NBS type B uncertainties, which were
all greater than 400 nW/W, listed ‘analysis’, ‘different force
profiles’ and ‘polynomial representation of the force profile’
as the largest three. NPL reported their largest uncertainties
as ‘traceability to volt and ohm references’ at a factor of 10
less than the alignment and analysis components of NBS,
which were considered negligible by NPL. The possibility that
misalignments of the coil with respect to the magnetic field
and gravity might have an effect was mentioned by both, but
dismissed as less than the random scatter witnessed in tests
that intentionally misaligned the coils. Measurements of both
systems were performed in air, so extra type B uncertainties
were added to account for the air temperature, pressure, relative
27

## PDF page 29

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

humidity and CO2 concentration needed to calculate the air
refractive index and mass buoyancy.
By ‘coincidence’ or not, both new values of the Planck
constant were within a few tenths of a part per million of
each other. The importance for future determinations was
highlighted by the low uncertainty of the NPL value, which
implied that the worst aspects of the dimensional limitations
of the ampere balance were gone for good. During the
1980s, the maturation in electrical metrology areas (QHE
resistance standards, Josephson effect voltage standards,
digital voltmeters and desktop lab computers) vastly improved
the watt balance technique, removing many constraints on
measuring h.
The word ‘coincidence’ is purposely used here in
commenting on the closeness of the two values. As will be
related in the following sections, both watt balances underwent
numerous improvements. These enhancements would later
reduce the combined relative uncertainty by almost a factor of
5, but another decade of changing designs and learning subtle
details also led to reconsiderations of the uncertainty for these
original numbers.
6.4. The next generation experiments at NIST and NPL
6.4.1. NIST 1998—adding a superconducting solenoid.
Although the apparatus configuration was mostly the same as
the earlier set up, as shown in figure 18, a second generation
of the NIST apparatus began with major upgrades in 1989.
Exchanging the normal wire solenoid with a Nb–Ti wire
superconducting solenoid greatly increased the field strength,
reported by Olsen in 1991 [114]. A current of 5 A in the new
solenoid generated about 0.1 T of magnetic flux intensity at the
35 cm radius of the induction coil. 10 mA in the induction coil
now generated 5 N of force for the half-weight value of a 1 kg
test mass. The coil travel ranged over 8 cm, with 2 mm s−1
velocity generating 1 V. Adding trim current to one side of the
main solenoid symmetrized the field profile with respect to
the weighing center for a better M-shape. Using the same
induction coil, the ε/v ratio from top to bottom varied by
400 × 10−6 from the central minimum to shoulder height.
There was considerable research and development from
1992 to 1998. Overall, new computers and instrumentation
programming improved data recording and analysis, while also
making the system operation more reliable. Modeling in [99]
described interactions between the coil’s magnetic vector and
the background magnet source field. An X–Y measurement
system, improved to monitor the coil’s attitude in the five
degrees of motion other than the vertical translation, applied
this new alignment theory to implement significantly better
coil alignment procedures. It also helped to provide qualitative
evaluations for the misalignment correction values associated
with residual misalignments, as reported in [100].
One new alignment test was to check for force errors
introduced from irregularities in the surface of the NIST wheel.
As it was impossible to perfectly align the coil so no translation
would occur, there was a worry that a small force change might
occur if the hanging angle of the band at the contact point on
the wheel changed due to a translation. These were measured
in 1998 and found to vary by less than 10 nW/W.

Figure 18. NIST watt balance schematic 1998. One fixed coil was
used as the motion reference plane, and to wired in series opposition
to reduce 60 Hz pickup.

New systems were also installed to improve the ε/v
ratio measurements. Three interferometer retroreflectors were
attached to the coil itself and reference reflectors were attached
to the fixed coil to provide a more precise position record. A
new voltage recording procedure incorporated three DVMs,
triggered sequentially, to record many more integration points
with nearly zero dead time between each point. The fourstep BL profile curve procedure was developed to reduce the
short term scatter, all reported in [115]. Since the apparatus
was still in air, a refractometer was constructed, reported in
[116]. This system verified that improved measurements of
air pressure, temperature, relative humidity and CO2 content,
when applied to real-time calculations of the refractive index
corrections from models by Birch and Downs in 1993 [117]
and 1994 [118], were the same as those measured.
6.4.2.
NIST 1998 result. These NIST improvements
culminated in a result of h = 6.626 068 91(58) × 10−34 J s,
with a relative combined uncertainty of 87 × 10−9 , reported
in [119] and in [120]. The details of this experiment are
in [121]. The NIST 1998 value agreed with the NPL 1988
value within their respective uncertainties (with an expanded
uncertainty on the NPL value, described at the end of the next
section). At that time, the accepted viewpoint was that h had
now been well established to a low uncertainty. With the
experiment uncertainty ‘quickly’ improving, reports on the
28

## PDF page 30

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 19. NPL balance photo and schematic diagram 1997. Left: reproduced with permission from [179]. Copyright 2012 BIPM. Right:
reproduced with permission from [95]. Copyright 2009 IEEE.

uncertainties. While the NBS uncertainty was perhaps overly
large, the new coil alignment understanding proved that the
old methods of alignment had been too crude. Fortunately,
while not as negligible as thought, misalignments were not
dominant uncertainties. The NPL did not find a new source
for a systematic error. They did realize that the offset in a few
points of their 1988 data set was large and unexplainable. They
suggested an increase in the
√ standard deviation
√ of the mean for
50 points as reduced by 5 instead of the 50 as reported in
1988. This increased the NPL 1988 uncertainty by a factor of
two to 2 × 10−7 , from [74].
More NPL coil alignment procedures were reported in
[125]. Vibrations induced noise in the voltage of the motion
stage, and with the direct connection to the Josephson system,
these caused a problem in the amplifier from sudden voltage
jumps in a hysteretic junction array with discrete voltage steps
(very noise sensitive), so a new amplifier was built. The NPL
version of an X–Y position system using optical transducers
recorded the non-vertical five degrees of motion. Data taken
from years 2000 into 2002 experienced some non-repeatability.
The suspected cause was a mechanical distortion of the laser
beam path affecting the alignments, arising when the system
was pumped down to a vacuum, from [126]. Two years later, in
addition to components added to perform alignments in a new
vacuum chamber, the progress reported in [127] mentioned
many equipment failures.

status of the IPK started contemplating that these electronic
experiments would soon reach an uncertainty goal of about
2 × 10−8 , arguably what would be needed in order to consider
redefining the kilogram [92]. Unfortunately, there was perhaps
too much importance given to the coincidence of these values,
since the NIST value and uncertainty were used straight away
in CODATA in 1998 [73].
6.4.3. NPL Mark II—in vacuum, new coil design. After
their 1988 result, the NPL system also underwent considerable
changes. By 1990, construction of a new apparatus was well
underway, shown in figure 19. The lever arm for motion control
was preserved. The magnet was redesigned to incorporate a
horizontal circular coil to reduce the field interactions between
the coil and magnet in place of the figure 8 induction coil, as
related in [122]. The coils and balance apparatus were built into
a vacuum chamber. Plumbing was installed around the magnet
with the intention of controlling the magnet temperature with
water-cooling. The new coil was wound on an extended
cylinder, a borosilicate glass former complete with a spider
arm connecting structure. A single mirror as the moving
reference in a Michelson interferometer was attached to the
former structure. Motion control had advanced enough to
begin sensitive testing on the knife edges, pivot points at
the balance arm center and coil and counter mass support.
By 1994, the new system was considered completely rebuilt,
reporting the start of testing in [123].
By 1997, the system was sufficiently automated to run
consistently and produce watt data. More improvements were
listed in [124]. Better control of the room air temperature
replaced the magnet’s abandoned water-cooled stabilization.
The magnet temperature drifted very slowly, but heating from
current in the coil required several hours for the magnet
temperature to stabilize after the start of a run. Ferromagnetic
parts on the balance were replaced with phosphor bronze parts.
Test masses made of low permeability copper plated with gold
were used to avoid effects of the large stray field of the magnet.
Direct connection of the coil to a Josephson junction voltage
system reduced the voltage transfer uncertainty.
By 1998, both laboratories’ increased knowledge of the
watt balance experiment led them to reconsider their 1988

6.4.4. NIST generation three—all new and into a vacuum.
After publishing the result in 1998, NIST almost completely
rebuilt the experimental apparatus, shown in figure 20, related
in [128], and in [129]. The only reused components were
the superconducting solenoid as the magnet source, the wheel
as the lever arm and the counter mass side structure using
an electromagnet surrounding a small permanent magnet for
the velocity drive. By reusing electronic equipment for
the interferometry timing, DVM-based voltage measurements
and a current source, it allowed considerable recycling of
the complex control and measurement software for speedier
assembly. The force balance and coil were redesigned and
constructed to fit into a new vacuum chamber. A three level,
29

## PDF page 31

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

After several missteps, a new and reinforced induction
coil was wound, as in [133]. Initially, a coil was wound
and the three reflectors for the interferometer installed, but
the phase mismatch and noise that had previously plagued
voltage-to-velocity signals were suddenly severe. Testing
revealed that the coil’s large diameter of 36 cm had large flexing
modes activated by the ground vibrations. Coil number one
was replaced with new and stiffer coil number two. The
interferometer reflectors were shifted to the nodes of the flex
pattern for optimal placement, which finally brought the phases
of the two measured components into synch. Unfortunately,
the epoxy used to stiffen the coil exhibited a time-dependent
dielectric polarization leakage, adding a new problem. In a
third coil, flexing was reduced with a ceramic stiffening ring
and special care was taken to add fiberglass insulation between
wire layers, along with selecting wire with insulation that had
low polarization effects.
Coil alignment procedures were refined and were
performed more quickly and often. A stepper motor and optical
position encoder were installed for micrometer control of tare
and test mass placement. Other program changes improved the
coil position control and added safety procedures to prevent
impulsive motions from the computer feedback control. Most
aspects of the system had been characterized and regular data
acquisition had resumed, as related in [134].
The improved signal and computer control enabled finer
testing. As mentioned previously, hysteresis of the magnetic
field may be common to all sources. Early tests at NIST
were not designed to determine the nonlinear coefficient, but
did show a dominantly linear effect, a presumed diamagnetic
cause, with a residual offset at about 15 nW/W at the limit of
sensitivity of the tests. A superconductor has the possibility
of trapping flux, changing the field strength non-reversibly.
Large current changes in the solenoid induce trapped flux,
either arising from unusual power surges in the solenoid current
controller, or induced by high rates of d /dt coming from a
high dI /dt rate of current injected into the induction coil. Tests
found a hysteretic force change of 1×10−6 from a programmed
spike in the control current of 100 µA for 60 s. Normally the
solenoid current is controlled to 5 A ±50 nA. Current spikes
induced by coil motion or current ramping were reduced to less
than 100 nA with programming control, so the hysteresis effect
is equivalently 10−3 smaller. That there are numbers for these
effects illustrates the unique advantage of an electromagnet:
current can be tracked, adjusted, reversed, or turned off.
Many lessons had been learned by the NPL and the NIST
during these years. The rest of the world concurrently began
to use this experience and so watt balances proliferated. The
next section describes these new systems.

Figure 20. A schematic drawing of the NIST watt balance and coil
inside the vacuum chamber. The solenoid is not in vacuum.

dedicated room was constructed inside the small nonmagnetic
laboratory building. This room stood apart from the building
itself to reduce the transmission of vibrations to the balance. A
partial success, it isolated the room from the building vibrations
due to wind gusts, but did little to reduce floor vibrations.
Only later in 2008 when the heating and ventilation fans in the
nearby office building were replaced did the ground vibrations
decrease. The new lab room was lined with copper sheeting
as a Faraday cage.
A tripod structure supports both the chamber and the
liquid helium Dewar containing the solenoid. The coil support
structure has crossed flexures at the top and bottom of the
long connection rods. The flexures can be tightened to mimic
the complex pendulum structure of old, or loosened to allow
the coil the kinematic freedom to tilt separately from any
swing motion. Orthogonal translation platforms under a single
pedestal supporting the wheel and mass moving stages allows
for coil adjustment centering without cracking the vacuum. A
crossed flexure connects the support band to the tri-arm spider
and below that to the mass pan. The flexure components can
be translated orthogonally to ease alignment of the CM along
the line of the hanging band, mass pan and coil. The balance
component materials were closely checked during construction
to avoid brass or steel that could be magnetized in the large stray
background field. The voltage reference is a system much more
immune to noise in the circuit, a Josephson programmable
1 V source described in [130, 131]. The tungsten-alloy knife
edge and flat of the old wheel pivot were replaced with harder
ceramics, coated with diamond-like carbon to reduce knife
edge force hysteresis by a factor of 10, related in [132].

6.5. The worldwide spread of watt balance experiments
6.5.1. New participants enter the game – France, Switzerland,
and the BIPM. The next era of watt balance efforts witnessed
the entrance of other national metrology laboratories. Earliest
was in Switzerland, known at the time as the Federal Office
of Metrology, (OFMET), and later as the Swiss Federal Office
of Metrology and Accreditation (METAS), described in [135].
30

## PDF page 32

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 21. Hardware configurations: (a) left, for the velocity measurement, the seesaw mechanism can be moved up and down by passing a
current in the servo coil. The interferometer is used to measure the velocity. The current is controlled in the servo coil to ensure a constant
velocity during the motion. The voltage induced at the measurement coil is measured against an SNS Josephson voltage standard. (b) Right,
for the force measurement, the measurement coil is positioned in the suspension frame and is fed by a current that allows the mass
comparator to equilibrate. Reproduced with permission from [135]. Copyright 1999 IEEE.

and easier component modification. The induction coil was
rigidly connected to a duel seesaw mechanism, constraining
the coil’s motion to vertical over 46 mm. The velocity driver
was an electromagnet in a permanent magnet field on the
opposite side, figure 21(a), similar to the NIST design. The
mechanical separation between modes was intended to reduce
the misalignment of the coil that comes from connection to a
freely moving lever arm, figure 21(b). There would also be no
hysteresis in the force mechanism left over from the moving
mechanism.
Transferring the connection of the coil from the velocity
cross arm mechanism to a weight support mechanism requires
a mass comparator to measure residual forces. This allows
individual alignment of the velocity and the force modes, but
also complicates the overall measurement. The mass support
mechanism represented a large load on the mass comparator,
limiting the test mass to 100 g. Later changes in the mass
support mechanism freed some motion degrees of freedom to
help in alignments, reported in [145].
The initial magnet source design used strong SmCo
permanent magnets embedded within an iron yoke to enclose
the magnetic field, shown in figure 22(a). The magnetic
field was not 1/r dependent, as it was similar to the original
NPL design. Modifying the NPL design, the induction coil
consisted of two coils connected in a figure 8, but horizontally
wrapping inside and outside of the magnet. Each coil had
2000 turns. A 5 mA current produced 0.5 N force. A Fabry–
Perot interferometer used one mirror on the coil and a reference
mirror connected to the support structure. The initial magnet
design and coil had a flux intensity of 0.47 T and a roughly
parabolic profile curve.
In characterization testing related by Beer in 2001 [146],
a problem was found in the magnetic field stability. The
heating and magnetic flux intensity changes caused by the
positive and negative currents in the coil resulted in severe
hysteretic effects in the magnet, shown in figure 23 in [147].

Shortly after, in France then known as the Bureau National
de Métrologie (BNM), and later as the Laboratoire National
de Métrologie et d’Essais (LNE), started a project in 2001,
related by Gournay [136]. The Bureau International des Poids
et Mesures (BIPM) in Paris announced their entry into the field
in [137]. All these laboratories jump-started their efforts by
adopting basic watt techniques and copying many procedures
of NPL and NIST.
Other national laboratories also started watt balances, but
their efforts were based on different strategies. The National
Institute of Metrology (NIM) in China proposed their version
of a joule balance in 2006 [138]. In 2009, the Measurement
Standard Laboratory (MSL) of New Zealand made the most
radical departure. They started developing a watt balance
based on measuring the voltage/velocity ratio with small
amplitude, periodic motion and using a pressure balance for
the force measurements, as described in [139].
Beginning in 2002, the four existing watt balance teams
began to meet annually in an informal forum to discuss
technical details. Eventually others attended, including
peripheral groups cooperating with the watt balance NMI
teams, and representatives of NMIs that were contemplating
building a system. The technical meetings in part coincided
with the bi-annual Conference on Precision Electrical
Measurements (CPEM). Progress reports from the CPEM
meetings for the various laboratories can be found in the reports
of the Consultative Committee for Electricity and Magnetism
(CCEM) to the BIPM [140–144].
6.5.2. The METAS Swiss balance—designed for compactness.
The two main design goals of the METAS balance were (1)
compact size and (2) a mechanical separation of the static
weighing mode from the dynamic motion mode. Anticipating
advantages in measuring a smaller mass, they incorporated
a smaller magnet, less overall apparatus weight with higher
frequency vibration modes, smaller temperature gradients
31

## PDF page 33

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 22. Hysteresis in the magnetic flux intensity of the METAS
magnet. A velocity profile of volts/velocity U /v is recorded after
positive or negative currents are injective temporarily into the coil.
Reproduced with permission from [147]. Copyright 2003 IEEE.

Figure 24. LNE magnet design. (a) Cutaway schematic of
assembled magnet. (b) Drawing with dimensions and magnetic
material locations. Reproduced with permission from [152].
Copyright 2005 IEEE.

The dual arm, curved surface motion system was designed
to avoid the cosine error of the NPL straight arm and the surface
irregularities of the NIST wheel. New position detectors
allowed better alignment of the coil, but revealed limitations
of the motion arm design. Vertical motion was so tightly
restricted that small non-vertical motions were immediately
converted into coil lateral motion. Over time, wear between
the hardened contact surfaces increased the surface irregularity.
6.5.3. LNE balance—multi-arm linear flexure motion. In
2001 the French national measurement institution LNE entered
the watt balance game. They anticipated the eventual
redefinition of the kilogram and wanted to fashion a system
with combined relative uncertainties approaching 1 part in
108 . The main guidelines were functional in measuring values
close to standard references with the lowest SI traceable
uncertainties, and technical in separating the weighing from
the translation stage. In contrast to the METAS method of
changing the coil connection from the translation mechanism
to the weighing mechanism, LNE decided to move the mass
comparator as part of the coil translation structure.
Thermal considerations led to designing a large, axially
symmetric permanent magnet, where the magnetic source
components needed to be as far as possible from thermal and
magnetic interactions with the induction coil, in [150, 151].
The LNE magnet design is shown in figure 24 and a model
of its flux intensity profile is shown in figure 25 from [152].
Calculations showed that machining the gap face with a slight
taper created the preferred profile with a flat slope in the
middle, and kept the relative variation along the travel path
of the coil to less than 10−4 . The design model predicts that

Figure 23. View of the old (a) and new (b) magnetic circuits. In the
new design, the two poles forming the yoke carry two SmCo
permanent magnets each and are maintained together with two
trapezoidal spacers. By sliding these latter up or down, the
parallelism and width of the gap can be adjusted. Note that
permanent magnets are further away from the heat source, i.e. coil)
in the new design. Reproduced with permission from [148].
Copyright 2004 IEEE.

A better magnet was designed and installed by 2004, shown
in figure 22(b) from [148]. The magnet’s core material was
moved farther from the center and thus, farther from the coil.
The field intensity was increased to 0.56 T, but the open design
had the disadvantage of a large stray field. Improvements
included the installation of multiple laser position detectors
for coil alignment monitoring. The data scatter was reduced
by about a factor of 5, related in [149]. The new magnet
design unfortunately made alignment slightly more difficult.
Sensitivity of the force measurement cell to changes in the
alignment meant delays while waiting for the load cell to
resume stability.
32

## PDF page 34

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 26. The prototype LNE linear motion assembly. Note the
counter weights across from the flexure points. Reproduced with
permission from [155]. Copyright 2011 Elsevier.
Figure 25. Modeled profile of the LNE magnet’s flux intensity. A
straight gap produces a linear behavior. A tapered gap produces a
profile with the desired flat spot. Reproduced with permission
from [152]. Copyright 2005 IEEE.

heating effects from power dissipated in the coil will have
minimal flux variations on the magnet. Also, the magnetic
interaction between the energized coil and the magnets should
be completely reversible.
A stand-alone sensor and guiding machine was designed
for characterizing the magnetic flux intensity azimuthally
within the gap, in [153]. Subsequently constructed, along with
a magnet support system, the two can be used to align the
magnet with respect to gravity. Once alignment is determined
with the sensor machine, the surface level of the magnet will
be used to reproduce the magnet attitude in a vacuum. Models
of the misalignment forces on the coil led to a coil suspension
design with multiple pivot points to allow for tilt and translation
control of the coil, and a positioning system that could make
these adjustments to the coil, in [154].
Since one design goal included moving the mass balance
with the coil, LNE needed a mechanism strong enough to
support and move both. It also must minimize the lateral
motions. Figure 26 from [155] shows the first prototype
mechanism of multiple flexure hinges with two planes (high
and low) of three flexures in 120◦ of symmetry. Tests on the
system found it was over constrained, which made adjusting
the linearity of the motion too difficult. A second mechanism
was built, with two opposing and one orthogonally positioned
flexure hinges, as shown in figure 27, also from [155]. The
orthogonal nature of the hinges made it clearer which flexure
shims needed trimming. The resulting lateral motion was
reduced to less than 0.5 µm and rotations to less than 6 µrad
along the 75 mm travel line.
Systems using time interval techniques to measure the
phase or fringing patterns in interferometers are limited by
electronic noise, so associated groups in France developed a

Figure 27. The later version of the LNE translation stage. Counter
weights (not shown) are attached two to each flexure. Reproduced
with permission from [155]. Copyright 2011 Elsevier.

method to control and measure the velocity of the moving
coil with extremely high precision. They reasoned that if the
relative velocity could be controlled with a precision of 10−9 ,
then the velocity and position would also be that well known.
The novel control method uses a heterodyne Michelson
interferometer and a high frequency phase shifter linked to
control the Doppler frequency shift of a laser reflecting off an
object, with a combination linear motor and PZT as the coarse
and fine translation stages, described in [156, 157]. A system
was designed for operation in a magnetically sensitive region
and in a vacuum. Position detecting consists of two modulated
laser beams with Gaussian distribution wave fronts passing
through a narrow slit onto a photo detector and then a lockin amplifier demodulates the signal. It is insensitive to laser
power fluctuations in the interferometer. The resolution of a
33

## PDF page 35

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 28. A schematic diagram of the LNE assembly. Note the
mass balance comparator in the center [151]. Image courtesy
of LNE.

test system is 25 pm/(Hz)1/2 and is stable over hours, reported
in [158]. A similar position detection system, along with the
phase detection Doppler system, is also proposed for use on
the next generation METAS watt balance, in [159].
The proposed force comparator and its position are
diagramed in the center of figure 28. It is a 100 mm long
stiff aluminum-alloy to keep bending within 10 µm with a
25 N weight on each end (coil and counter weight) plus a
1 kg test mass load, and a light mass of 200 g for sensitivity.
The beam and its flexure kinematics are described in [160].
A single flexure at the pivot point connects the beam center
to the support structure, while crossed flexures connect the
pans and coil to the support structure. LNE plans to use a
sloshing liquid damping system to damp the swinging of the
mass pan, described in [161]. Angular motions of the main
flexure must be reduced as much as possible to minimize stress
related hysteresis, so mechanical stops inhibit stage motion
when placing the test mass on the pan.
Two peripheral measurement systems received extensive
attention. LNE collaborated with the NPL to design and built
a programmable bias current source, reported in [162]. This
is for variable biasing of a Josephson programmable array to
ramp and measure the voltage, as described in [163]. A newly
built laboratory room was characterized with extensive gravity
transfer measurements made across the floor and in the 2 m of
space above, referenced to a baseline established with a cold
atom gravimeter, summarized in [164, 165].
As of July 2011, the LNE has moved the vacuum
chamber into the laboratory room and is assembling the many
components in the chamber. Planck constant results may be
available sometime in 2013.

Figure 29. Schematic of the BIPM watt balance assembly.
Reproduced with permission from [168]. Copyright 2010 IEEE.

prototype system shown in figure 29, reported in [166]. The
system performs the same functions as those at other NMIs, but
looks very different. A complicated mounting of small balance
arms and flexure gimbals act as the lever arms of the balance.
They are seen at the top of the figure, connecting the electrode
plate to the induction coil and mass pan. As a constant
current in the coil nearly balances the test mass reference, any
residual forces are measured on a weighing cell at the top of
the system. The motion drive stage is an electrostatic motor
consisting of a fixed capacitive plate coupled to a movable
plate. The electrostatic motor eliminates stray magnetic fields
from electromagnetic drives of the NIST, NRC or METAS
systems, although stray electrostatic fields were discovered in
this preliminary set up. A maximum controlled velocity of only
0.2 mm s−1 is available from the weak force of the electrostatic
motor. A single interferometer reflector was connected to the
spider support of the test mass and coil, not on the coil. A
thin induction coil extends down into the gap of a permanent
magnet. A secondary non-inductive coil is wound parallel to
the main induction coil for use as a coil resistance monitor.
A preliminary result from this system was published in
2011. The value was different from CODATA in 2006 by
−4.8 × 10−6 with a relative uncertainty of 1.3 × 10−5 . The
tests were performed in air with little temperature regulation,
and many other type B uncertainty components were not
considered. The magnetic field and coil were only coarsely
aligned. The ε/v ratio was ten times noisier than the F /I
records, representing the largest of the type A uncertainty
components, as seen in figure 30 from [165]. This was mainly
due to the one-mirror interferometer and the phase mismatch

6.5.4. Simultaneous measurement of force and motion: BIPM
Paris. Work on the BIPM system, with the intent to measure
both F /I and ε/v began in 2007. While also developing a
larger system, they began testing many novel ideas with a
34

## PDF page 36

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 30. Comparison of BIPM ratio measurements. The type A
uncertainty lines around the voltage/velocity ratio are much larger
than the force/current. Reproduced with permission from [166].
Copyright 2011 IEEE.

between the mirror position and the EMC. The measurement
procedure was complicated by needing to correct the total coil
voltage for the resistive voltage drop of the current in the coil to
find the generated voltage. Part of the fairly large offset in the h
value was later suspected as an incorrectly calibrated resistance
standard, although the dominant uncertainty component was
still in the ε/v ratio. The BIPM group analyzed the data two
ways. They fitted the curves in a way similar to other labs and
also averaged individual points overall. Both methods agreed,
within the noise.
A more sophisticated system is being designed. Their
preliminary magnet had no central, zero slope region in the
B(z)L profile, and it is noteworthy that it is not necessary for
this technique. The group hopes that eventually the induction
coil and magnet will be cryogenically cooled, so there will
be many design changes from the prototype system. A new
magnet design, with construction started in 2011, incorporates
special materials for cryogenic temperatures. Shown in cross
section in figure 31, the magnet circuit is closed to reduce stray
fields, from [167]. As a result of the enclosed region, once the
coil is built into the magnet, further alignments will be difficult.
Knowing this, the group has developed a novel method
to align the coil once installed. They characterized the vector
alignment of the magnetic field with respect to the acceleration
of gravity at the center of the long solenoid, wound with a
single wire layer. The sensor is a thin metal film shaped as
spiral coil imprinted on the surface of an ultra-flat glass block.
The electrical plane of the spiral coil coincides with the flat of
the block, which in turn can be aligned with an autocollimator.
Using the characterized solenoid, a new induction coil will be
inserted into the solenoid center and aligned to the solenoid
magnetic flux intensity. A flat mirror then affixed to the
coil will recreate an equivalent level reference once the coil
is installed inside the magnet. The reproducible alignment
uncertainty is 50 µrad, similar to that obtainable with other
means in other watt balances, a technique reported in [168].
Many other improvements are planned for the entire
assembly. These include a new magnet, a vacuum chamber,
a coil support assembly with active piezoelectric level
control, a three-mirror on-the-coil interferometer system and
an automated mass exchanger. The new apparatus will

Figure 31. BIPM magnet The magnetic circuit, consisting of two
discs of Sm2 Co17 and a closed FeNi yoke. Reproduced with
permission from [167]. Copyright 2006 Inter-American Metrology
System.

Figure 32. A schematic of the Joule balance assembly. Reproduced
with permission from [170]. Copyright 2010 IEEE.

be installed in a newly constructed laboratory room, with
vibration isolated floor, temperature control and low noise
lighting. The room was extensively measured to characterize
the local acceleration of gravity at any place in the whole
volume. An absolute gravity meter will sit upon a separate
isolated floor area just outside the watt balance area. The
BIPM’s goal is to operate the watt balance at an uncertainty of
5 × 10−8 by 2015 [169].
6.5.5. Joule balance: NIM China. Since 2006, the Joule
balance concept is being tested at the NIM China. As seen in
figure 32 from [170], the balance lever arm design is similar to
35

## PDF page 37

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

the NPL. Studies have commenced on the vibration isolation
of the block under the magnet section (right side) and the
potential deformation of the lever arm under tension. They are
a studying a fixed coil electromagnet design that will achieve a
magnetic field distribution with a broad, flat profile across the
center. Two positions of equal force are needed to measure the
mutual inductance, discussed in [171].
The use of superconducting coils is anticipated for
generating larger forces. Room temperature coils have so
far been used to test the methods for measuring the mutual
inductance M12 , in [172]. Test measurements of M12 at four
different frequencies and extrapolating to 0 Hz have exhibited
a relative uncertainty just below 1 × 10−6 .
6.5.6. Oscillatory velocities: MSL New Zealand. In 2009,
Sutton [200] at the Measurement Standard Laboratory (MSL)
in New Zealand suggested an alternative to recording a slowly
varying dc voltage generated along a long travel path, to
oscillate the coil over a short range of motion to produce a
small constant frequency ac voltage instead. This significantly
reduces the apparatus’ vertical dimension. This would also
relax the magnetic field criteria requiring a large magnet
creating a uniform field over a long z range. Citing an example,
a 0.3 Hz sinusoidal oscillation at 1 mm amplitude generates a
peak 2 mm s−1 velocity. By controlling the oscillation about
the weighing point, extrapolation of the complex field profile
is reduced to measuring the frequency, f , and amplitude, A,
ε/v = ε/(2πf A).
Recording the voltage to the requisite precision requires
an ac voltage measuring technique. This is available with an
ac quantum voltmeter, described in [173]. Present research is
identifying the limitations of the ac voltage measurements. The
coil motion at the primary frequency must be very sinusoidal,
with little contribution from background vibrations. The
design goal is a signal amplitude between 1 and 10 V at about
1 Hz. An optimum aperture time for a sampling ac voltmeter is
dependent upon the settling times for the Josephson switching
junction and the preamplifier, mentioned in [174].
The unique apparatus design includes a gas-operated
pressure balance to make a precise force measurement: the
precision of a pressure balance can approach 1 part in 108 ,
in [175]. A differential pressure balance, as in figure 33
from [176], also adds a mechanical method to control the
ac motion. Driving the coil motion without also generating
stray magnetic or electrostatic fields is an advantage. It should
also maintain the linear alignments during the motion phase.
Normally in a pressure balance the piston rotates but, as it
needs a connection to the coil, this is not possible. So research
is proceeding on rotating the cylinder instead and to enclose
the balance in a vacuum chamber.

Figure 33. A proposed schematic of a pressure-balance based
system at the MSL New Zealand. Reproduced with permission
from [176]. Copyright 2010 IEEE.

those produced since 2004. The value is known to a far better
accuracy than those early days of the past century and with
equally more sophistication in the data analyses. The data is
shown as reported so readers are able to see the relative scatter
between the system. Each laboratory conducts innumerable
tests, so here are just the highlights of the reported experimental
tests. Perhaps buried somewhere in these reports there is a hint
of a solution to another problem that needs to be solved, for as
in the long history of measuring this constant, there is not yet
complete agreement on the value, at least to the desired level
of uncertainty.
7.2. NIST 2005 and 2007
After rebuilding the system in a vacuum, a result from the
new NIST system was published in [177]. The value h =
6.626 069 01(34) × 10−34 J s had a combined relative standard
uncertainty of 52 parts in 109 . (All the uncertainties quoted
here are a combined relative standard uncertainty with k = 1).
The new testing included measurements on two different mass
materials. Early data was based on two gold 500 g disks, which
had been chosen to avoid magnetic susceptibility issues within
the background magnetic field. The main part of the data was
accumulated with a PtIr kilogram cylinder fabricated in 2005
(identification number K85). The PtIr mass was assumed to
be more accurate and the Au-based data had a slightly offset
value, although both had similar scatters. The calibration of
the gold mass had an uncertainty that was about as large as the
offset value, due in part to its lower density. Even worse, gold
is such a soft material that the test mass had a large drift rate,
losing mass at a significant and irregular rate.
A significant test included reversing the solenoid’s
magnetic field during the Au-mass test run with no discernible
effect outside the data scatter, about 60 nW/W p-p. Also, force
measurements were recorded at different z-positions, testing
the magnetic flux intensity profile calculations. The wheel
was characterized for interactions between the roundness and
smoothness of the balance wheel’s surface with the coil’s

7. The most recent h results: not quite a consensus
7.1. System reports
Now that the theory of watt balance measurements and
the experiments undertaken have been summarized, this
penultimate section recounts the most recent results for h,
36

## PDF page 38

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Figure 34. NIST aggregate of daily watt data points from testing the PtIr kilogram mass K85. Error bars represent the standard deviation
(k = 1) for each day’s run of 10 to 25 points. Data averages (Avg) are reported in nW/W units with ± standard deviation of each block of
data. Reproduced with permission from [178]. Copyright 2007 IEEE.

support band, and different coil alignment configurations were
tried, with their coinciding corrections added.
A number of minor changes were made to the system in
the 2005–2006 interim. The earlier data appeared to have some
cyclical structure. This sensitivity was attributed to external
or peripheral instrument changes. Two components of the
current measurement circuit caused excessive variability. The
reference resistors in 2004–2005 suffered a small temperature
shock in each move from one lab to another for calibration, so
the procedure was changed to treat the resistor more gently,
keep them closer to 25 ◦ C and transferred more often. This
noticeably reduced the short term scatter. A more severe
problem was related to a connection wire to the resistor. Its
insulation was found to be sensitive to humidity during the
2004–2005 run, so a correction for the daily relative humidity
was applied for a partial set of the data. After the lead was
changed, the new wire had no noticeable humidity sensitivity,
and there was no significant change to the result in the second
set of data.
Two years later, there were other reductions to type B
uncertainty components. More calibration history on the
primary test mass K85 revealed its mass was increasing,
probably due to surface contamination. The drift rate was
much slower than the large rate of decrease of the gold mass,
but larger than changes in the 100-plus year old original PtIr
copies. There was an improved value for the acceleration of
gravity. Alignment techniques were refined to better center the
coil and test mass with respect to the overall CM and EMC, thus
reducing lateral motions of the coil. Calibrating the gradient
corrections applied to the coil misalignment was improved, as
was the programmed motion control of the mass placement.
A new value for 2007 was h = 6.626 068 91(24) × 10−34 J s,
with an uncertainty of 36 parts in 109 , reported in [178]. The
watt data for both studies, showing only the PtIr kilogram
tests, are shown in figure 34. There is good consistency over
several years. The 2007 value included only the data taken in
2005–2006.

Figure 35. NPL watt data, averaged by test mass group. The error
bars are the standard deviation of the averaged data sets.
Reproduced with permission from [179]. Copyright 2012 BIPM.

March 2007, shown in figure 35 from [179]. The new value
had a 66 nW/W combined relative standard uncertainty. It was
also 308 nW/W different from the NIST 2007 value.
Two sets were based on 1 kg reference weights of goldplated copper ‘A’, with a third set using a similar 1 kg weight
‘B’. Two other sets measured 500 g weights, one similar in
material to ‘A’ and ‘B’ and one a silicon cylinder, ‘C4’. Among
many tests, a key one addressed the question of nonlinear
effects within the permanent magnet by using different test
weights, implying different current settings in the coil.
By 2008, NPL watt data had been consistent for several
years, but since the average was different from the just
announced NIST value, more modifications were made [94].
The coil suspension was changed to reduce rotations about
the horizontal axis. A new oil bath containing the reference
resistors operated with better temperature regulation and
reduced the heating effects of the current within the resistors.
The main laser interferometer was changed to eliminate a
lens component that deviated the beam, which also added
an advantage of reducing the vacuum feed-through seals and
lowering the chamber pressure.
Shortly after the 2008 progress report, the mechanical
components of the older apparatus started to show their age.

7.3. NPL 2007 and update 2010
In 2007, a new NPL result was reported as h =
6.626 070 95(44) × 10−34 J s, in [102]. Five sets of data were
included in the final analysis, recorded from October 2006 to
37

## PDF page 39

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

To compound the repair work, lightning had damaged several
electronic components, reported by Robinson [180]. There
was anticipation that the older system would be replaced by the
next generation Mark III of the NPL watt balance, with designs
reported in [181]. However, the NPL had decided to shut
down the watt balance experiment and all work on the Mark
III was ceased. The existing system and peripheral equipment
would be sold and transferred to the National Research Council
(NRC) in Ottawa Canada after one last determination. By late
2009, the NPL apparatus had been disassembled and shipped
to the NRC.
The final point of NPL data was recorded in June 2009.
The last effort included tests on several more types and sizes
of reference masses. Robinson in 2012 [102] published
an extensive summary paper to describe the procedures and
uncertainty analysis of the final data sets. This ultimate
NPL value containing data from June 2006 to June 2009 was
h = 6.626 071 23(133) × 10−34 J s. This value was 42 parts in
109 higher than the original 2007 result.
In analyzing only the uncertainty contributions as
determined from the test data, the modified result was ready
for reporting an uncertainty of 36 × 10−9 . However, the NPL
in 2010 published a value with an uncertainty increased to
200 × 10−9 . An unforeseen problem was discovered during
the disassembly of the balance. This problem was alluded
to in the previous section and diagrammed in figure 14. The
coil position is controlled with reference to the interferometer
reflector on the coil. But when the test mass is placed on
the pan and the opposing electromagnetic force is applied to
the coil, the coil support rods compress. Maintaining the coil
position in turn led to a rotation of the lever arm, which is
represented in figure 14(b) as the angle dθ. A difference in the
force on a 1 kg test mass was estimated at 192 nW/W for the
correlation of the change in angle of lever arm rotation against
the known balancing force. Unfortunately, the apparatus had to
be taken apart, so testing could not determine the actual offset
value. Therefore, the reported h value included the combined
measurement uncertainties plus the estimated offset error.

Figure 36. METAS data used in the calculation of h relative to
CODATA-90 value of h90 . The small, open circles represent the
mean value of ten individual determinations (10 h periods). Closed
circles are the mean values of each block of data. All error bars are
type A standard deviation. Reproduced with permission from [182].
Copyright 2011 BIPM.

mirror on the coil limited the adjustment of the verticality of
the laser, which had to have an offset angle. Aligning the mass
comparator to horizontal was also a major contribution.
7.5. Avogadro 2004 and 2010
Although most of sections 4–6 were devoted to determining
the Planck constant via the watt balance, a value for h can
also be obtained from other constants via their relation in
equation (11), the Avogadro constant measurements. These
measurements are difficult, but a summary comparison of the
results between the two techniques is of great interest, since
the uncertainty is approaching or exceeding the watt balance
results.
Between the dates of the 1998 NIST result announcement
and the 2010 NPL result, two results arose from the Avogadro
experiments.
In 2004, the x-ray crystal measurement
consortium published a value for the Avogadro constant.
The associated Planck value from NA -2004 was h =
6.626 0762(21) × 10−34 J s in [183] and [184]. This result
had an uncertainty of 310 × 10−9 , but differed from the NPL
1988 and NIST 1998 values by about 1000 × 10−9 , as is
apparent in figure 37. After an apparent agreement between
NPL-1988, NIST-1998 and NIST-2005 (announced in 2004),
it was presumed that convergence was at hand. The different
value from the Avogadro group created an immediate incentive
to recheck everything in both types of experiments. As a
result of the new difference, the compilation in CODATA 2002
published in [185] assigned a value of h = 6.626 0693(11) ×
10−34 J s with an increased uncertainty of 1.7 × 10−7 .
The Avogadro group suspected that certain component
results had higher degrees of uncertainty than calculated.
Improvements were made in all phases of the XRCD
experiment. Acknowledging that the isotopic distribution of
natural silicon of the molar mass of the 15 natural silicon
spheres was the most probable suspect, they began a special
project to address the isotope distribution result. Two fresh
spheres were made from enhanced 99.985% 28 Si, as reported

7.4. METAS 2011
After many years of effort, METAS published a Planck value
of h = 6.626 0691(20) × 10−34 J s, with a relative uncertainty
of 290 × 10−9 . Figure 36 from [182] shows the data used to
calculate this value. The overall type A uncertainty for the
data segments is about 70 nW/W (k = 1). This scatter and
the larger per-day error bars are quite a bit larger than NPL or
NIST. It is interesting to note that the group average values are
quite stable, implying at least some long term reproducibility.
There are several contributing factors to the noise. The
test values were small, at voltages of 0.5 V and a test mass of
100 g. The measurements were made in a sealed chamber, but
not in a vacuum, compensating for the recorded atmospheric
conditions. The main type B uncertainty components were
cited in both of the F /I and the ε/v ratio measurements, the
voltage measurements and the horizontal velocity components.
A significant problem arose in the beam alignment, arising
from the compact structure of the apparatus. Using a flat
38

## PDF page 40

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

fundamental constants, hope was alive that the NPL system
could be revived. In late 2011, the NRC in Canada had
reassembled the NPL system, taken enough data and performed
some checks to release a new result. They reported an NRC2011value as h = 6.626 070 63(43) × 10−34 J s, in [189].
This value has a 65 × 10−9 uncertainty. The paper had little
information on the uncertainty contributions; the system had
not been in complete operation for a full year. Given the
previous lengths of time laboratories have spent in testing for
error sources, it must be assumed that the estimated uncertainty
is largely based upon the prior work at the NPL. Referring to
the positioning problem found as the NPL system was being
dismantled, the paper mentions, ‘It should be noted here that
the NRC result includes data from the measurement of the
effects of both the stretching of the coil support flexures under
load, and of the tilting effect on the balance support base due
to loading and unloading the mass lift’. The NPL estimations
of this possible error were much larger than the NRC results
show.
The same paper mentions a new measurement of the
isotopic distribution for the 28 Si spheres. Using other
measurements from the Avogadro consortium, but applying
the NRC determination, they have an inferred value NRC-NA 2011 for h = 6.626 070 55(21) × 10−34 J s, with 30 × 10−9
relative uncertainty.
7.7. National laboratory updates

Figure 37. Planck values since 1979, direct and inferred.

As of July 2011, METAS has suspended data acquisition on the
existing system, and is actively constructing the components
for their next generation system. In [190], they report that the
new design will use the familiar circular induction coil, move
the load cell with the coil, as does the LNE, but use a unique
13-hinge translation stage machined out of a single piece of
material. The LNE reports in [191] that they are finishing
assembly and testing individual components, especially the
dynamic motion stage. The mass comparator is being tested
separately. BIPM reports in [192] that they have an improved
magnet and have added a three-reflector interferometer onto
the coil. The next step is to get delivery of the iron shell
for the magnet, the vacuum chamber and then assemble the
new system into the specially prepared room. From [193],
NRC has evaluated the mass exchange errors discovered upon
its disassembly at the NPL. Work at NIM continues on the
joule balance; Zhang [194] reports on studies of the heating in
the induction coils and positioning of the moving coil section.
KRISS in South Korea is in the planning stage of building a
watt balance.
With all the other existing systems being rebuilt in
some aspect or another, the NIST system has continued
to operate and produce consistent results, in [195]. Tests
included different reference mass amounts and materials, in
[196]. Improvements were made on the alignment to facilitate
calibrations of correction factors, such as installing small
piezoelectric linear motors on the upper spider to tilt the coil
in a vacuum and peripheral calibrations. There were more
frequent and higher quality gravity transfers to reduce that
uncertainty component, as in [197]. The NIST system also

in [186]. When new atomic spectrometer measurements
repeatedly had discrepant results, different calibration methods
for the atomic spectrometers were developed. With novel
methods in hand, an incorrect calibration of an atomic
spectrometer in one of the laboratories was found to account for
a large change in the molar mass that also applied to the natural
silicon spheres. This discovery added an offset and raised the
uncertainty to 2.4 × 10−7 for the 2004 value, reported in [187].
Applying the estimated correction of −1200×10−9 , it created a
new NA -2004x inferred value h = 6.626 0681(16) × 10−34 J s.
This new value agreed with the previous watt values, within
an expanded uncertainty.
Armed with the two enhanced 28 Si spheres, a new
value for the Avogadro constant was published in 2010 by
Andreas in 2011 [188]. The inferred value of NA -2010 is
h = 6.626 070 14(20) × 10−34 J s. The relative uncertainty
of 30 × 10−9 is now the lowest published uncertainty on
the Planck constant h. But the story does not end here.
This value is between the NIST-2007 and the NPL-2010
values. Its agreement with the NA -2004x value is on the
high end of the uncertainties; it is not a comfortable example
of reproducibility. The value falls within the expanded
uncertainty of the NPL-2010 value, but not the uncertainty
of NIST.
7.6. NRC Canada–reviving the NPL apparatus
Within the international community, while it was sad to see
the NPL withdraw from their historical era of measuring
39

## PDF page 41

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

started to show its age in some of the components, in [198].
The old interferometer timing and current source electronics
are being replaced. Schlamminger [199] reports on the design
of a 4th generation NIST system, incorporating a permanent
magnet.

8. Concluding remarks
8.1. A data summary
With all the modern measurements of the Planck constant in
hand, what is the situation now? It is not yet possible to
definitively state ‘a conclusion’, where there is an accepted
value for h. Figure 37 shows the values for h from 1979
onward, both direct via the watt balance and for various
inferred values. Clearly the higher precision of watt balances
and Avogadro measurements have superseded even the best
of the other inferred determinations. Figure 38 includes only
the most recent watt balance and Avogadro values, plus the
proposed value from CODATA 2010. Except for the METAS2011 result and the BIPM value (not shown), the results
since 2007 imply a recent shift in the value for h. However,
examine closely the reproducibility of the laboratories. The
NPL h values and Avogadro group’s inferred h from their
NA values have shifted, well beyond their earlier uncertainty
determinations. Both experiments are acknowledged as being
performed with greater sophistication, yet some of the new
techniques are just that, i.e. new. Whether the type B
uncertainties have all been estimated correctly can only be
assured with long term reproducibility. Any group may once
again find some unexpected shift in a result.
Similar jumps in the values of other fundamental constants
have occurred over their respective histories, so this is not a
unique problem. However, the redefinition of all SI units is
anticipated and in most areas welcomed. It is certainly being
advocated and predicted to be on the horizon. The last artifact
standard of the kilogram IPK will be part of this redefinition. At
the CCEM-Working Group on the Kilogram meeting in 2010
issued a statement: ‘ (w)hen the data are deemed to be sufficient
to support a redefinition, the working group would like to move
forward with redefinition as soon as possible, ideally within a
year [143].’ This redefinition has been described as the last
assignment of the constants and their related units.
The length, time and frequency, volt and ohm metrology
communities can rightfully say that reproducibility of their
conventional unit is better than 10 parts in 109 . These same
units apply to the peripheral measurement systems needed
for modern Planck measurements. The kilogram artifacts are
also ‘peripheral’ to the watt Planck measurement, yet still
suffer as the last vestiges of the laboratory representative units,
those artifacts that were infrequently calibrated or compared.
Figure 10 is a reminder that the kilogram unit is not perfectly
defined, even if it appears to be two orders of magnitude
more stable and well known than the standard cell banks
were in the 1970s. The mass calibration community would
like an electronically derived standard with an uncertainty
equal or less than 20 parts in 109 , as stated in a BIPM 2007
report [200]. This goal seems near, with the most recently

Figure 38. Expanded plot of the best Planck values, since 1988.

expressed uncertainties hovering around 35 × 10−9 . Yet this
is almost ten times less than the discrepancies in the most
recent results for h values. Thus questions remain unanswered
or perhaps uncertainly answered. From the view on high,
where the kilogram IPK stands alone, one question stands
out in an enigmatic and circular loop: are mass calibrations
consistent and reproducible for the various materials and values
contributing to an accurate determination of h, a determination
that will in turn be used in electronic systems that will measure
mass references of various materials and masses?
8.2. The future of h and IPK
Watt balance systems have advanced experimentally, although
terming the advance ’rapid’ is debatable when looking at
time frames of 5–10 years or longer between significant
results. It is important to understand that the work is not
finished. Questions about the uncertainty analyses remain,
especially since the error contributions are becoming so
small. Is the background magnetic flux consistently stable
between measurement modes? Are its variations sufficiently
characterized between the different experimental methods and
magnets? Once redefinition occurs, how long will it take
to calibrate a mass reference in a watt balance, where some
uncertainty components are small only if they are averaged
over time frames longer than months? Is 1 year, 5 years,
or 10 years of reproducibility an adequately long enough
time for calling a measurement stable? These questions will
eventually be answered. The history of the last hundred years
40

## PDF page 42

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

has shown that disparate values do not remain forever but that
the resolution can take a long time.
Having a more stable ‘absolute mass standard’ is a good
idea. Return once more to the proposed redefinition of mass
in terms of a fundamental physical constant. On one hand, the
Avogadro relation to mass is indirect with regard to the Planck
constant, but the measurement of counting atoms is inherently
and directly related to mass. The disadvantage is that silicon
spheres are the only artifacts measured in the Avogadro
experiment and these are not easily used to disseminate the
kilogram to other laboratories. Watt balances on the other hand
are direct measurements of h and, with no affiliation to any
specific mass object, any one of several national apparatuses
will be able to measure a variety of materials and mass values.
There is no clearly defined commercial requirement pushing
greater improvements to mass calibrations, other than to keep
the volt and ohm from drifting far outside SI consistency.
As watt balances become calibration systems, even with
uncertainties of 20 × 10−9 , this should be satisfactory to the
existing mass standards community. But what may happen in
the time frame of the next hundred years?
For that question, the watt balance technique as it is
presently employed fails as a truly ‘universal’ representation of
a standardized mass unit, since a gravitational force is required
to balance against electromagnetic forces. Dick Deslattes of
NIST was quoted concerning the kilogram artifact, ‘(i)f we
wanted to communicate our knowledge of the world to some
extraterrestrial group, we could encode everything in binary,
except the kilogram,’ says Deslattes. As for the mass standard,
‘we’d have to throw it,’ as quoted in [201]. Having a mass
unit based on the Planck constant solves the communication
problem, but just who are those extraterrestrials? In free
fall space, no one can measure a kilogram with the existing
procedures on the watt balance. It is not flippant to consider
that someday those extraterrestrials will be human space
travelers, on a space station or even a colony ship to another
world. They would need mass standards and would at least
have to land, spin up or accelerate their space ship, or turn on
some futuristic gravity generator. Presuming the watt balance
system will be adopted as the future mass representation,
trying to answer this question may lead to new research.
Can this experiment, which so nicely measures h, be done
using inertial mass measurements instead of gravitational mass
determinations?
Some present and past researchers have discussed options,
but there is no simple idea that is devoid of yet another array of
alignment concerns or energy loss mechanisms. Two of these
ideas suggest moving a mass against a linear spring with a
linear motor, or just using a rotating motor, measuring the force
as a function of the sinusoidal time period changes relative to
angular momentum. If using a spring with lateral motion,
then the problem arises of how to avoid friction in maintaining
alignment, and is the elastic force of a spring more stable than
a gravitational force? When rotating a mass, how to measure
the angular momentum, especially if it requires knowing the
radius of motion of the CM of a large cylinder kilogram [202]?

Figure 39. A graph summarizing the complete history of Planck
constant determinations (dots), especially noting the decrease of
uncertainty. Error bars are the assigned uncertainty of the results.
Solid line is the modern value, dashed line shows the decreasing
uncertainties of the values (right axis).

8.3. An impressive history
As reported all through this review, the Planck constant has
been measured with ever better resolution, as illustrated in
figure 39. It has several times in its history been considered
adequately reproduced, only to find a significantly different
value a decade or more later. The first ‘established’ value was
nearly 1% (10 000 000 × 10−9 ) different from modern results.
The differences in the results along with the uncertainties have
plunged since then; now a ‘mere’ 300 × 10−9 difference exists
between recent experiments. The earlier differences were
caused by errors in peripheral experiments, i.e. the viscosity of
air, and then later in the laboratory volt and ohm representative
units and the absolute ampere. It would be pleasant if a sudden
revelation found a reason for the latest difference. However, as
every measurement segment improves, it also becomes more
complicated. As it is hard to predict an unanticipated future,
it is impossible to guess one thing to focus upon as the usual
suspect.
Some predictions about existing watt balance systems
are possible.
There is still potential for improvement
from diverse areas to address the experiment’s complexity,
labor-intensive operation and susceptibility to wear and tear.
Developments in material science suggest ways to make
mechanical parts last longer, or mass artifacts with more inert
and harder surfaces. Another generation of computers and
instrumentation programming will improve the mechanical
control and misalignment recording, as well as better modeling
of various components, such as the magnetic field and
electromagnetic interactions, mechanical micro-motions and
nano-forces, and complicated curve fitting with noise. From
its beginnings 112 years ago, h measurement science has
continued a logarithmic time improvement in the uncertainty
of the determinations by about a factor of ten every 20 years.
Bumps and a decrease in the uncertainty curve’s slope over
the last 20 years suggest it is unlikely that another factor
of 10 reduction will arrive soon, if ever. On the optimistic
side, history has shown that improvements in calibration
41

## PDF page 43

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

capabilities for standard references lead to better standards,
then to better instruments and finally full circle to further
enhanced calibrations. Perhaps this algorithm still has another
cycle for mass standards.
As a last word, it is absolutely amazing to see that
the best measurements of a purely quantum concept, the
Planck constant h, is attainable by a combination of ‘old’
classical physics involving a force balance, electromagnetic
interactions, ‘new’ quantum-based time and frequency, length
and electrical measurements. It is equally surprising that the
complications involved are surmounted even as they continue
to grow. Roughly quoting the author of the idea that triggered
research on the modern watt balance systems, Bryan Kibble
once said as he watched a presentation on one of the newer,
extremely complicated watt balance designs, ‘it all seemed so
simple when I first thought of it.’ Perhaps the same thought
occurred to Planck and Einstein.

[6] Richardson and Compton 1912 The photoelectric effect Phil.
Mag. 24 575–94
[7] Brush S G 2007 How ideas became knowledge; The
light-quantum hypothesis 1905-1935 Hist. Stud. Phys.
Biol. Sci. 37 205–46
[8] Millikan R A 1913 On the elementary charge and the
Avogadro constant Phys. Rev. 2 109–43
[9] Warburg E, Leithäuser G, Hupka E and Müller C 1913 Über
die Konstante c des Wien-Planckschen Strahlungsgesetzes
Ann. Phys. 345 609–34
[10] Millikan R A 1916 A direct photoelectric determination of
Planck’s ‘h’ Phys. Rev. 7 355
[11] Petley B W 1985 The Fundamental Physical Constants and
the Frontier of Measurement ed A E Bailey (Bristol:
Hilger/Institute of Physics Publishing) pp 106–15
[12] Coolidge W D 1913 A powerful Röntgen ray tube with a pure
electron discharge Phys. Rev. 2 409–30
[13] Duane W and Hunt F L 1915 On x-ray wavelengths Phys.
Rev. 6 166–72
[14] Destalles R D 1980 The Avogadro constant Annu. Rev. Phys.
Chem. 31 435–61
[15] Becker P 2001 History and progress in the accurate
determination of the Avogadro constant Rep. Prog. Phys.
64 1945–2008
[16] Bäcklin E 1928 Inaug. Diss Uppsala Universitets Arsskrift
[17] Birge R T 1919 The most probable value of the Planck
constant h Phys. Rev. 14 361–8
[18] Blake F C and Duane W 1917 The value of "h" as determined
by means of x-rays Phys. Rev. 10 624–37
[19] Birge R T 1929 Probable values of the general physical
constants Rev. Mod. Phys. 1 1–73
[20] Birge R T 1932 On the values of fundamental physical
constants Phys. Rev. 52 241
[21] Birge R T 1945 The 1944 values of certain atomic constants
with particular reference to the electronic charge Am. J.
Phys. 13 63–73
[22] Birge R T 1941 A new table of values of the general physical
constants Rev. Mod. Phys. 13 233–9
[23] Singh A, Mishra R K and Singh S 2011 Certain
investigations regarding variable physical constants Int. J.
Res. Rev. Appl. Sci. 6 18–29
[24] Bearden J A and Shwartz G 1950 A precision evaluation of
h/e by x-rays Phys. Rev. 79 674–84
[25] Bearden J A, Johnson F T and Watts H M 1951 A new
evaluation of h/e by x-rays Phys. Rev. 81 70–2
[26] Bearden J A and Watts H M 1951 A re-evaluation of the
fundamental atomic constants Phys. Rev. 81 73–81
[27] Cohen E R and DuMond J W M 1965 Our knowledge of the
fundamental constants of physics and chemistry in 1965
Rev. Mod. Phys. 37 537–94
[28] Deaver B S Jr and Fairbank W M 1961 experimental
evidence for quantized flux in superconducting cylinders
Phys. Rev. Lett. 7 43–6
[29] Doll R and Näbauer M 1961 Experimental proof of magnetic
flux quantization in a superconducting ring Phys. Rev. Lett.
7 51–2
[30] Josephson B 1962 Possible new effects in superconductive
tunneling Phys. Lett. 1 251–3
[31] Pöpel R 1992 The Josephson effect and voltage standards
Metrologia 29 153–74
[32] Elmquist R E, Cage M E, Tang Y-H, Jeffery A-M, Kinard J
R, Dziuba R F, Oldham N M and Williams E R 2001 The
ampere and electrical standards J. Res. Natl Inst. Stand.
Technol. 106 65–103
[33] Harris W Snow 1834 Phil. Trans. R. Soc. Lond. Part II
213–45
[34] Thomson W 1868 Report on electrometers and electrostatic
measurements Report of the 37th Meeting of the British
Association for the Advancement of Science pp 489–512

Acknowledgments
During my 17 years of doing research on the NIST watt
balance, and the 10 years before that in working on Josephson
voltage standards, it has been my pleasure to learn the
techniques from and participate in many discussions with my
NIST co-workers and the many international collaborators I’ve
met in the interim. Several deserve special mention. Peter
Mohr added some suggestions after reading through a first
draft of this paper and supplied me with hard-to-find reference
materials on fundamental constants determinations. P. Tom
Olsen and Ed Williams of NIST introduced me to the watt
balance system. Many enthusiastic discussions with the NPL
folks helped me develop an understanding of its intricacies,
with Bryan Kibble on applying the general theory and being the
custodian of so much electrical measurement history, and with
Ian Robinson on trading horror stories about maintaining and
programming the operations. Lastly but hardly least, Estefania
de Mirandes at the BIPM has been both a friendly sounding
board and an original source for bouncing around ideas about
worrisome measurement details, alternative ways to play with
the system and future visions of where it all may be headed.

References
[1] Planck M 1901 Uber das Gesetz der Energieverteilung im
Normalspektrum Ann. Phys. 4 553–63
[2] Planck M 1900 Über eine Verbesserung der Wien’schen
Spectralgleichung Verh. Dtsch. Phys. Ges. 2 202–4
Planck M 1967 On an improvement of Wien’s equation for
the spectrum (translation) The Old Quantum Theory ed D
ter Haar (New York: Pergamon) p 79
[3] Planck M 1900 Zur Theorie des Gesetzes der
Energieverteilung im Normalspectrum Verh. Dtsch. Phys.
Ges. 2 237–45
Planck M 1967 On the theory of the energy distribution law
of the normal spectrum (translation) The Old Quantum
Theory ed D ter Haar (New York: Pergamon) p 82
[4] Einstein A 1905 Über einen die Erzeugung und Verwandlung
des Lichtes betreffenden heuristischen Gesichtspunkt Ann.
Phys. 17 132–48
[5] Hughes A L 1913 On the emission velocities of
photo-electrons Phil. Trans. R. Soc. 212 205–26
42

## PDF page 44

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

[35] Ohlon R 1967 An electrostatic method for the absolute
measurement of voltage Metrologia 3 33–7
[36] Thompson A M and Lampard D G 1956 A new theorem in
electrostatics and its application to calculable standards of
capacitance Nature 177 888
[37] Elnékavé N and Fau A 1983 BIPM Com. Cns. Electricité
Doc. CCE/83-2 16
[38] Yamazaki T, Shida K and Kanno M 1972 Absolute
measurement of voltage by an electrostatic
energy-changing method IEEE Trans. Instrum. Meas.
IM-21 372–5
[39] Sienknecht V and Funck T 1986 Realization of the SI unit
volt by means of a voltage balance Metrologia 22 209–12
[40] Bego V, Butorac J and Poljancìicì K 1995 Voltage balance for
replacing the kilogram IEEE Trans. Instrum. Meas.
44 579–82
[41] Bego V, Butorac J and Ilicì D 1998 Realization of Croatian
electromagnetic prototype of the kilogram Precision
Electromagnetic Measurements Conf. Digest (CPEM
1998)( Washington, DC) pp 627–8
[42] Clothier W K 1965 A proposal for an absolute liquid
electrometer Metrologia 1 181–4
[43] Bego V 1988 Determination of the volt by means of voltage
balances Metrologia 25 127–33
[44] Report of the CIPM Resolution 2 1946 Procès-Verbaux des
Séances du CIPM 20 129–37
[45] Ayrton F E, Mather T and Smith F E 1908 A new current
weigher and a determination of the electromotive force of
the normal weston cadmium cell Phil. Trans. R. Soc. Lond.
207 463–544
[46] Guthe K E 1906 A new determination of the electromotive
force or Weston and Clarke standard cells by an absolute
electrodynamometer Bull. Bur. Stand. 2 33–70
[47] Rosa E B 1906 The Gray absolute electrodynamometer Bull.
Bur. Stand. 2 71–86
[48] Rosa E B, Dorsey N E and Miller J M 1912 A determination
of the international ampere in absolute measure Bull. Bur.
Stand. 8 269–393
[49] Curtis H L and Curtis R W 1934 An absolute determination
of the ampere Bur. Stand J. Res. 12 665–734
[50] Driscoll R L and Cutkosky R D 1958 Measurement of current
with the National Bureau of Standards current balance J.
Res. Natl Bur. Stand. 60 297–305
[51] Cohen E R and Dummond J M M 1965 Our knowledge of the
physical constants of physics and chemistry in 1965 Rev.
Mod. Phys. 4 538–94
[52] Taylor B N 1976 Is the present realization of the absolute
ampere in error? Metrologia 12 81–3
[53] Kibble B 1976 A suggestion for a different way of realizing
the ampere Atomic Masses and Fundamental Constants
vol 5, ed J H Sanders and A H Wapstra (New York:
Plenum) pp 549–51
[54] Williams E and Kibble B 2012 private communication
[55] Terrien J 1969 News from the Bureau International des Poids
et Mesures Metrologia 5 58–71
[56] Terrien J 1966 The Work of the Bureau International des
Poids et Mesures concerning electromagnetic units and
measurements IEEE Trans. Instrum. Meas. IM-15 140–5
[57] Vigoureux P 1965 A determination of the ampere Metrologia
1 3–7
[58] Driscoll R L and Olsen P T 1968 Report to Comité
Consultatif d’Electricité, Comité International des Poids
et Mesures 12th session
[59] Taylor B N, Parker W H and Langenberg D N 1969
Determination of e/ h, using macroscopic quantum phase
coherence in superconductors: implication for quantum
electrodynamics and the fundamental physical constants
Rev. Mod. Phys. 41 375–496
[60] Séances P V 1968 Com. Intl. Poids Mes. 57th Session 36 17

[61] Eicke W G Jr, Taylor B N 1972 Summary of international
comparisons of as-maintained units of voltage and values
of 2e/ h IEEE Trans. Instrum. Meas. IM-21 316
[62] Cohen E R and Taylor B N 1973 The 1973 Least-squares
adjustment of the fundamental constants J. Phys. Chem.
Ref. Data 2 663–734
[63] Terrien J 1972 Fundamental metrology Metrologia 8 99–108
[64] Niemeyer J 1987 On the development of large josephson
series arrays for voltage standards of high precision IEEE
Trans. Instrum. Meas. IM-36 252–7
[65] Hamilton C A et al 1987 The NBS Josephson array voltage
standard IEEE Trans. Instrum. Meas. IM-36 258–61
[66] Hamilton C 2000 Josephson voltage standards Rev. Sci.
Instrum. 71 3611–23
[67] Leclerc G 1973 Etalons representatifs de l’ohm et du volt
Metrologia 14 171–4
[68] von Klitzing K, Dorda G and Pepper M 1980 New method
for high accuracy determination of the fine-structure
constant based on quantized Hall resistance Phys. Rev.
Lett. 45 494–7
[69] Liu R et al 1995 A recent determination for the SI values of
γp′ and 2e/ h at NIM Acta Metrol. Sin. 16 161–8
[70] Kibble B P and Hunt G J 1979 A measurement of the
gyromagnetic ratio of the proton in a strong magnetic field
Metrologia 15 5–30
[71] Bower E and Davis R S 1980 The electrochemical equivalent
of pure silver-a value of the Faraday J. Res. Natl Bur.
Stand. 85 175–81
[72] Sloggett G J, Clothier W K and Ricketts B W 1986
Determination of 2e/ h and h/e2 in SI units Phys. Rev.
Lett. 57 3237–40
[73] Clothier W K et al 1989 A determination of the volt
Metrologia 26 9–46
[74] Mohr P J and Taylor B N 2000 CODATA recommended
values of the fundamental physical constants: 1998 Rev.
Mod. Phys. 72 351–495
[75] Funck T and Sienknecht V 1991 Determination of the volt
with the improved PTB voltage balance IEEE Trans.
Instrum. Meas. 40 158–61
[76] Flowers J 2004 The route to atomic and quantum standards
Science 306 1324–30
[77] Quinn T 1989 News from the BIPM Metrologia 26 69–74
[78] Taylor B N 1987 History of the present value of 2e/ h
commonly used for defining national units of voltage and
possible changes in national units of voltage and resistance
IEEE Trans. Instrum. Meas. IM-36 659–64
[79] Kibble B P and Robinson I A 1977 Feasibility study for a
moving-coil apparatus to relate the electrical and
mechanical SI units British National Physical Laboratory
Report DES 40
[80] Olsen P T, Cage M E, Phillips W D and Williams E R 1980
The realization of the Ampere at NBS IEEE Trans.
Instrum. Meas. IM-29 234–7
[81] Taylor B N 1985 Impact of quantized Hall resistance on the
SI electrical units and fundamental constants Metrologia
21 37–9
[82] Kose V and Wöger W 1986 Fundamental constants and units
of physics Metrologia 22 177–85
[83] Sullivan D B and Frederick N V 1977 Can superconductivity
contribute to the determination of the absolute ampere?
IEEE Trans. Magn. MAG-13 396–9
[84] Kibble B P 1983 Realizing the ampere by levitating a
superconducting mass—a suggested procedure IEEE
Trans. Instrum. Meas. IM-32 144
[85] Shiota F et al 2000 Evaluation of equilibrium trajectory of
superconducting magnetic levitation system for the future
kg unit of mass IEEE Trans. Instrum. Meas. 49 1117–21
[86] Gläser M and Borys M 2009 Precision mass measurements
Rep. Prog. Phys. 72 126101
43

## PDF page 45

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

[87] Riski K, Heikkinen P and Kajastie H 2001 Design of a
superconducting magnetic levitation system Proc. IMEKO
TC3 2001 (Istanbul) pp 239–46
[88] Kajastie H, Nummila K K and Rautiainen A 2008 Loss
measurements on superconducting Nb by a cryogenic dual
compensated calorimeter for the implementation of the
kilogram standard by the levitation mass method
Metrologia 45 68–74
[89] Kajastie H, Riski K and Satrapinski A 2009 Mass
determination with the magnetic levitation
method—proposal for a new design of electromechanical
system Metrologia 46 298–304
[90] Zhang Z, He Q and Li Z 2006 An approach for improving the
watt balance Precision Electromagnetic Measurements
Conf. Digest (CPEM2006) (Torino, Italy) pp 126–7
[91] Olsen P T, Phillips W D and Williams E R 1980 A proposed
coil system for the improved realization of the absolute
ampere J. Res. Natl Bur. Stand. 85-4 257–72
[92] Davis R 2003 The SI unit of mass Metrologia 40 299–305
[93] Quinn T J 1991 The kilogram: the present state of our
knowledge IEEE Trans. Instrum. Meas. IM-40 81–5
[94] Mills I M et al 2005 Redefintion of the kilogram: a definition
whose time has come Metrologia 42 71–80
[95] Robinson I A 2009 Towards a Final Result from the NPL
Mark II Watt Balance IEEE Trans. Instrum. Meas.
IM-58 936–41
[96] Eichenberger A, Jeckelmann B and Richard P 2003 Tracing
Planck’s constant to the kilogram by electromechanical
methods Metrologia 40 356–65
[97] Eichenberger A, Geneves G and Gournay P 2009
Determination of the Planck constant by means of a watt
balance Eur. Phys. J. Spec. Top. 172 363–83
[98] Steiner R, Newell D and Williams E 2005 Details of the 1998
watt balance experiment determining the planck constant
J. Res. Natl Inst Stand. Tecnol. 110 1–26
[99] Stenbakken G N, Steiner R L, Olsen P T and Williams E R
1996 Methods for aligning the NIST watt balance IEEE
Trans. Instrum. Meas. 45 372–7
[100] Gillespie A D et al 1997 Alignment uncertainties of the NIST
watt experiment IEEE Trans. Instrum. Meas. IM-46 605–8
[101] Faller J E 2005 The measurement of little g: a fertile ground
for precison measurement science J. Res. Natl. Inst. Stand.
Technol. 110 559–81
[102] Robinson I A and Kibble B P 2007 An initial measurement of
Planck’s constant using the NPL Mark II watt balance
Metrologia 44 427–40
[103] Picard A et al 2007 The BIPM watt balance IEEE Trans.
Instrum. Meas. IM-56 538–42
[104] Picard A et al 2011 The BIPM watt balance: improvements
and progress IEEE Trans. Instrum. Meas. IM-60 2378–86
[105] Robinson I A 2012 A simultaneous moving and weighing
technique for a watt balance at room temperature
Metrologia 49 108–12
[106] Kibble B P, Smith R C and Robinson I A 1983 The NPL
moving-coil ampere determination IEEE Trans. Instrum.
Meas. IM-32 141–3
[107] Bates L F and Spivey S 1965 The domain structure of
columax Br. J. Appl. Phys. 16 385–7
[108] Petley B W, Kibble B P and Hartland A 1987 A measurement
of the Planck constant Nature 237 605–6
[109] Olsen P T et al 1985 The NBS absolute ampere experiment
IEEE Trans. Instrum. Meas. IM-34 175–81
[110] Hartland A, Jones R G, Legg D J 1988 Document CCE/88-9
18th meeting of the CCE
[111] Kibble B P, Robinson I A and Beliss J H 1990 A realization
of the SI watt by the NPL moving-coil balance Metrologia
27 173–92
[112] Olsen P T et al 1989 A measurement of the NBS electrical
watt in SI units IEEE Trans. Instrum. Meas. IM-38 238–44

[113] Cage M E et al 1989 NBS Determination of the fine-structure
constant, and of the quantized Hall resistance and
Josephson frequency-to-voltage quotient in SI units IEEE
Trans. Instrum. Meas. IM-38 284–9
[114] Olsen P T, Tew W L 1991 Monitoring the mass standard via
the comparison of mechanical to electrical power IEEE
Trans. Instrum. Meas. IM-40 115–20
[115] Steiner R L et al 1997 The NIST watt balance: progress
toward monitoring the kilogram IEEE Trans. Instrum.
Meas. IM-46 601–4
[116] Fujii K, Williams E R, Steiner R L and Newell D B 1997 A
new refractometer by combining a variable length vacuum
cell and a double-pass Michelson interferometer IEEE
Trans. Instrum. Meas. IM-46 191–5
[117] Birch K P, Downs M J 1993 An updated Edlén equation for
the refractive index of air Metrologia 30 155–62
[118] Birch K P, Downs M J 1994 Correction to the updated Edlén
equation for the refractive index of air Metrologia
31 315–6
[119] Williams E R, Steiner R L, Newell D B and Olsen P T 1998
Accurate measurement of the Planck constant Phys. Rev.
Lett. 81 2404–7
[120] Steiner R L, Newell D B and Williams E R 1999 A result
from the NIST watt balance and an analysis of
uncertainties IEEE Trans. Instrum. Meas. IM-48 205–8
[121] Steiner R L, Newell D B and Williams E R 2005 Details of
the 1998 watt balance experiment determining the Planck
constant J. Res. Natl Inst Stand. Technol. 110-1 1–26
[122] Kibble B P, Robinson I A and Belliss J H 1990 Re-defining
the kilogram via a moving-coil apparatus Precision
Electromagnetic Measurements Conf. Digest (CPEM
1990)(Ottawa Canada) pp 178–9
[123] Robinson I A, Kibble B P and Belliss J H 1994 The NPL
moving-coil watt balance Precision Electromagnetic
Measurements Conf. Digest (CPEM 1994) (Boulder CO)
p 527
[124] Robinson I A and Kibble B P 1997 The NPL Moving-coil
apparatus for measuring Planck’s constant and monitoring
the kilogram IEEE Trans. Instrum. Meas. IM-46 596–600
[125] Robinson I A and Kibble B P 2000 Further progress in
relating the kilogram to H with the NPL watt balance
Precision Electromagnetic Measurements Conf. Digest
(CPEM 2000) (Sydney, Australia) pp 540–1
[126] Robinson I A and Kibble B P 2002 Progress in relating the
kilogram to Planck’s constant [h] with the NPL watt
balance Precision Electromagnetic Measurements Conf.
Digest (CPEM 2002) (Ottawa, Canada) pp 574–5
[127] Robinson I A and Kibble B P 2004 Progress on the NPL watt
balance: alignment and measurements Precision
Electromagnetic Measurements Conf. Digest (CPEM
2004) (London, UK) pp 54–5
[128] Newell D B, Steiner R L, Williams E R and Picard A 1998
The next generation of the NIST watt balance Precision
Electromagnetic Measurements Conf. Digest (CPEM
1998) (Washington, DC) pp 108–9
[129] Steiner R L, Newell D B, Williams E R, Liu R and Gournay P
2005 The NIST project for the electronic realization of the
kilogram IEEE Trans. Instrum. Meas. IM-54 846–9
[130] Burroughs C J, Benz S P, Hamilton C A and Harvey T E 1999
Programmable 1 V dc voltage standard IEEE Trans.
Instrum. Meas. IM-48 279–81
[131] Burroughs C J, Benz S P, Harvey T E and Hamilton C A 1999
1 volt dc programmable Josephson voltage standard IEEE
Trans. Appl. Supercond. 9 4145–9
[132] Schwarz J P et al 2001 Hysteresis and related error
mechanisms in the NIST watt balance experiment J. Res.
Natl Inst. Stand. Technol. 106 627–40
[133] Steiner R L, Newell D B, Williams E R, Liu R 2002 Status of
the NIST ‘Electronic Kilogram’ Experiment Precision
44

## PDF page 46

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

Electromagnetic Measurements Conf. Digest (CPEM
2002) (Ottawa, Canada) pp 578–9
[134] Steiner R L et al 2004 The NIST electronic realization of the
kilogram project Precision Electromagnetic Measurements
Conf. Digest (CPEM 2004) (London, UK) pp 52–3
[135] Beer B et al 1999 A Proposal for a New Moving-Coil
Experiment IEEE Trans. Instrum. Meas. 48 192–5
[136] Gournay P et al 2004 Magnetic circuit design for the BNM
watt balance experiment Precision Electromagnetic
Measurements Conf. Digest (CPEM 2004) (London, UK)
pp 510–1
[137] Picard A et al 2007 The BIPM watt balance IEEE Trans.
Instrum. Meas. 56 538–42
[138] BIPM 2007 Report of the 25th Meeting of the CCEM 8
[139] Sutton C M 2009 An oscillatory dynamic mode for a watt
balance Metrologia 46 467–72
[140] BIPM 2002 Report of the 23rd Meeting of the CCEM 98–99
[141] BIPM 2005 Report of the 24th Meeting of the CCEM 7–9
[142] BIPM 2007 Report of the 25th Meeting of the CCEM 7–9
[143] BIPM 2009 Report of the 26th Meeting of the CCEM 6–7
[144] BIPM 2011 Report of the 27th Meeting of the CCEM 6–8
[145] Eichenberger A et al 2006 Mechanical improvements in the
METAS watt balance Precision Electromagnetic
Measurements Conf. Digest (CPEM 2006) (Turin, Italy)
pp 62–3
[146] Beer W et al 2001 The OFMET watt balance: progress report
IEEE Trans. Instrum. Meas. IM-50 583–6
[147] Beer W et al 2003 Status of the METAS watt balance
experiment IEEE Trans. Instrum. Meas. IM-52 626–30
[148] Eichenberger A L et al 2004 A new magnet design for the
METAS watt balance Precision Electromagnetic
Measurements Conf. Digest (CPEM 2004) (London, UK)
pp 56–7
[149] Eichenberger A et al 2008 Reproducibility of the METAS
watt balance Precision Electromagnetic Measurements
Conf. Digest (CPEM 2008) (Boulder, CO) pp 12–13
[150] Genevès G et al 2005 The BNM watt balance project IEEE
Trans. Instrum. Meas. IM-54 850–3
[151] Genevès G 2006 The French watt balance project Proc. 2006
Simposio de Metrologia (Querétaro, Mexico) 6pp
[152] Gournay P et al 2005 Magnetic Circuit Design for the BNM
watt balance experiment IEEE Trans. Instrum. Meas.
IM-54 742–5
[153] Villar F, Gournay P, David J and Genevès G 2008 A
measuring machine for the magnetic circuit of the LNE
watt balance Precision Electromagnetic Measurements
Conf. Digest (CPEM 2008) (Boulder, CO) pp 128–9
[154] Villar F, Genevès G and David J 2010 Determination and
minimization of parasitic forces and moments in the static
step of the LNE watt balance experiment Precision
Electromagnetic Measurements Conf. Digest (CPEM
2010) (Daejeon, Korea) pp 34–5
[155] Villar F, David J and Genevès G 2011 75 mm stroke flexure
stage for the LNE watt balance experiment Precision Eng.
35 693–703
[156] Topcu S et al 2003 Heterodyne interferometric technique for
displacement control at the nanometric scale Rev. Sci.
Instrum. 74 4876–80
[157] Topcu S, Chassagne L, Haddad D and Alayii Y 2004 High
accuracy velocity control method for the French
moving-coil watt balance Rev. Sci. Instrum.
75 4824–7
[158] Haddad D, Juncar P and Genevès G 2009 Gaussian beams
and spatial modulation in nanopositioning IEEE Trans.
Instrum. Meas. IM-58 1003–9
[159] Bielsa F et al 2010 Characterization of the coil displacement
in the LNE and METAS watt balance experiments
Precision Electromagnetic Measurements Conf. Digest
(CPEM 2010) (Daejeon, Korea) pp 512–3

[160] Pinot P et al 2007 Theoretical analysis for the design of the
French watt balance experiment force comparator Rev. Sci.
Instrum. 78 095108
[161] Williams E et al 2009 Balance pan damping using rings of
tuned sloshing liquids IEEE Trans. Instrum. Meas.
IM-58 949–53
[162] Maletras F X et al 2007 A bias source for dynamic voltage
measurements with a programmable Josephson junction
array IEEE Trans. Instrum. Meas. IM-56 495–9
[163] Kieler O, Behr R, Müller F, Schulze H, Kohlmann J and
Niemeyer J 2002 Improved 1 V programmable Josephson
voltage standard using SINIS junctions Physica C
372 309–11
[164] Merlet S et al 2008 Micro-gravity investigations for the LNE
watt balance project Metrologia 45 265–74
[165] Louchet-Chauvet A et al 2010 Comparison of 3 absolute
gravimeters based on different methods for the e-MASS
project arXiv:1008.2884v2 [physics.atom-ph] 1–6
[166] Picard A et al 2011 The BIPM watt balance: improvements
and progress IEEE Trans. Instrum. Meas. IM-60 2378–86
[167] Stock M 2006 Watt balances and the future of the kilogram
INFOSIM—Informative Bulletin of the InterAmerican
Metrology System (November 2006)—OAS pp 9–13
[168] de Mirandes E et al 2011 Alignment procedure used in the
BIPM watt balance IEEE Trans. Instrum. Meas.
IM-60 2415–21
[169] Progress at BIPM Presentation 2011 Watt Balance Technical
Meeting (Bern, Switzerland)
[170] Li C, He Q and Zhang Z 2010 The balance system of Joule
balance in NIM Precision Electromagnetic Measurements
Conf. Digest (CPEM 2010) (Daejeon, Korea) pp 281–2
[171] Han B et al 2010 The magnetic system of Joule balance in
NIM Precision Electromagnetic Measurements Conf.
Digest (CPEM 2010) (Daejeon Korea) pp 526–7
[172] Zhang Z et al 2011 Recent development on the Joule balance
at NIM IEEE Trans. Instrum. Meas. IM-60 2533–8
[173] Behr R et al 2007 Direct comparison of Josephson
waveforms using an AC quantum voltmeter IEEE Trans.
Instrum. Meas. 56 235–8
[174] Christian L A, Stewart T J and Sutton C M 2010 Investigation
of ac voltage measurement requirements for an oscillatory
dynamic mode version of the watt balance Precision
Electromagnetic Measurements Conf. Digest (CPEM
2010) (Daejeon Korea) pp 151–2
[175] Sutton C M 2009 Performance aspects of gas operated
pressure balances as pressure standards Metrologia
46 655–60
[176] Sutton C M, Fitzgerald M P and Jack D G 2010 The concept
of a pressure balance based watt balance Precision
Electromagnetic Measurements Digest (CPEM 2010)
(Daejeon, Korea) pp 131–2
[177] Steiner R L, Williams E R, Newell D B and Liu R 2005
Towards an electronic kilogram: an improved
measurement of the Planck constant and electron mass
Metrologia 42 431–41
[178] Steiner R L, Williams E R, Liu R and Newell D B 2007
Uncertainty improvements of the NIST electronic
kilogram IEEE Trans. Instrum. Meas. IM-56 592–6
[179] Robinson I A 2012 Towards the redefinition of the kilogram:
a measurement of the Planck constant using the NPL Mark
II watt balance Metrologia 49 113–56
[180] Robinson I A 2010 The NPL Mark II watt balance: final
measurements at NPL Precision Electromagnetic
Measurements Conf. Digest (CPEM 2010) (Daejeon,
Korea) pp 99–100
[181] Robinson I A and Lovelock P 2006 Design of the third
generation NPL watt balance 2006 Precision
Electromagnetic Measurements Conf. Digest (CPEM
2006) (Turin, Italy) pp 124–5
45

## PDF page 47

Rep. Prog. Phys. 76 (2013) 016101

R Steiner et al

[193] Sanchez C A, Wood B M, Inglis A D and Robinson I A 2012
Determination and correction of mass exchange errors in
the NRC watt balance Precision Electromagnetic
Measurements Conf. Digest (CPEM 2012) (Washington,
DC) pp 428–9
[194] Zhang Z et al 2012 The Joule balance in progress Precision
Electromagnetic Measurements Conf. Digest (CPEM
2012) (Washington, DC) pp 432–3
[195] Steiner R L, Williams E R, Liu R and Parker B 2008
Estimating uncertainty limits in the NIST-2008 electronic
kilogram Precision Electromagnetic Measurements Conf.
Digest (CPEM 2008) (Boulder, CO) pp 10–11
[196] Steiner R et al 2010 Measurement of mass scaling and
alternate materials on the NIST electronic kilogram
system Precision Electromagnetic Measurements Conf.
Digest (CPEM 2010) (Daejeon, Korea) pp 103–4
[197] Parker B and Steiner R 2008 Reducing the uncertainty in a
measure of the acceleration of gravity for the electronic
kilogram Precision Electromagnetic Measurements Conf.
Digest (CPEM 2008) (Boulder, CO) pp 126–7
[198] Steiner R, Haddad D, Liu R and Perl E 2010 Upgrading the
NIST electronic kilogram system Precision
Electromagnetic Measurements Conf. Digest (CPEM
2010) (Daejeon, Korea) pp 32–3
[199] Schlamminger S 2012 The permanent magnet system for
NIST-4 Precision Electromagnetic Measurements Conf.
Digest (CPEM 2012) (Washington, DC) pp 334–5
[200] BIPM 2007 Report of the 10th Meeting of the CCM pp 5–6
[201] Kestenbaum D 1998 Recipe for a kilogram Science
280-5365 823–4
[202] Personal discussions with de Mirandes E, Bradley M BIPM
2009, and with Robinson I and Kibble B CPEM 2012

[182] Eichenberger A L, Baumann H and Jeanneret B 2011
Determination of the Planck constant with the METAS
watt balance Metrologia 48 133–41
[183] Becker P et al 2003 Determination of the Avogadro constant
via the silicon route Metrologia 40 271–87
[184] Fujii K et al 2005 Present state of the Avogadro constant
determination from silicon crystals with natural isotopic
compositions IEEE Trans. Intrum. Meas. IM-54 854–9
[185] Mohr P J and Taylor B N 2005 CODATA recommended
values of the fundamental constants: 2002 Rev. Mod. Phys.
77 1–107
[186] Becker P et al 2006 Large-scale production of highly
enriched 28Si for the precise determination of the
Avogadro constant Meas. Sci. Technol. 17 1854–60
[187] Valkiers S, Mana G, Fujii K and Becker P 2011 Si primary
standards for the calibration of ion-current ratios in the
molar-mass measurement of natural Si single crystals
Metrologia 48 S26–31
[188] Andreas B et al 2011 A determination of the Avogadro
constant by counting the atoms in a 28 Si crystal Phys. Rev.
Lett. 106 030801
[189] Steele A et al 2012 Reconciling Planck constant
determination via watt balance and enriched silicon
measurements at the NRC Canada Metrologia 49 L8–10
[190] Eichenberger A et al 2012 The METAS watt balance Mark II
experiment Precision Electromagnetic Measurements
Conf. Digest (CPEM 2012) (Washington, DC) pp 426–7
[191] Thomas M et al 2012 Present Status of the LNE watt balance
Precision Electromagnetic Measurements Conf. Digest
(CPEM 2012) (Washington, DC) pp 332–3
[192] Fang H et al Status of the BIPM watt balance Precision
Electromagnetic Measurements Conf. Digest (CPEM
2012) (Washington, DC) pp 424–5

46
