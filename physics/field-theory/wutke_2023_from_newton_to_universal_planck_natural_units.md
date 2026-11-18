Source: https://doi.org/10.1088/2399-6528/ad0090
PDF sha256: dd807d4d06a393fc2c5db8c042bf65fc8bfbe78b39dfeb4f6d4a16330a2220e0
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of wutke_2023_from_newton_to_universal_planck_natural_units.pdf

Transcription of `wutke_2023_from_newton_to_universal_planck_natural_units.pdf` in this directory, 25 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-25 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Journal of Physics
Communications

You may also like

PAPER • OPEN ACCESS

From Newton to universal Planck natural units –
disentangling the constants of nature
To cite this article: Andrew Wutke 2023 J. Phys. Commun. 7 115001

View the article online for updates and enhancements.

- Strong Feller property of the
magnetohydrodynamics system forced by
space–time white noise
Kazuo Yamazaki
- Analysis of resolution of tomographic-type
reconstruction from discrete data for a
class of distributions
Alexander Katsevich
- Stronger reverse uncertainty relation for
multiple incompatible observables
Xiao Zheng, Ai-Ling Ji and Guo-Feng
Zhang

This content was downloaded from IP address 71.84.237.76 on 25/03/2025 at 06:04

## PDF page 2

J. Phys. Commun. 7 (2023) 115001

https://doi.org/10.1088/2399-6528/ad0090

PAPER

OPEN ACCESS

From Newton to universal Planck natural units – disentangling the
constants of nature

RECEIVED

25 May 2023
REVISED

1 October 2023
ACCEPTED FOR PUBLICATION

5 October 2023
PUBLISHED

23 November 2023

Andrew Wutke
Thales Australia Limited, 7 Murray Rose Ave, Sydney Olympic Park NSW 2127, Australia
E-mail: andrew.wutke@yahoo.com.au
Keywords: ﬁne structure constant, Planck scale, rationalized system of units, fundamental constants, Stoney mass, ﬁnite electron ﬁeld
energy, metric systems

Original content from this
work may be used under
the terms of the Creative
Commons Attribution 4.0
licence.

Abstract
This study exploits a historical gap in the evolution of metric systems that resulted from the
incomplete implementation of the ‘rationalization’ concept published by Heaviside in 1893 and by
Any further distribution of
ignoring the suggestion of Maxwell in 1873 to use the simplest form of Newton’s gravitational law
this work must maintain
attribution to the
expression with no proportionality constant. Bridging this gap required deriving an experimental
author(s) and the title of
the work, journal citation Rationalized Metric System (RMS) and a corresponding Universal Planck Natural Unit System
and DOI.
(UPNUS) in [ LT ] units. The described solution combines Heaviside’s rationalization of Newton’s law
and makes the unit of mass dimensions [ L3T−2 ], as suggested by Maxwell. Consequently, the
modiﬁed Coulomb’s law, changes the unit of electric charge to the same dimensions as those of mass.
The elimination of the kilogram and ampere has a disentangling effect on the dependencies among the
constants of nature and opens new horizons. New systems have the potential to become powerful
exploratory tools in fundamental research and education because of the simpliﬁcation of the
relationships among physical quantities. Some highlights from the analyzed examples are worth
mentioning. The well-known expression for the Stoney mass (mS) when converted to RMS units is
reduced to the electron charge quantity, whereas traditional metric systems entangle the charge, speed
of light, and gravitational constant, forming an entity in the dimension of mass, as ﬁrst presented by
Stoney in 1874. Furthermore, a well-substantiated conjecture is proposed, wherein the Stoney energy
ES = mSc 2 is likely the long-sought, ﬁnite electric ﬁeld energy of the electron, and the gravitational
constant appears to be the limiting factor. In UPNUS, the most disentangled fundamental expression,
apart from the Stoney mass, is the elementary charge e ̌ as the function of the ﬁne structure constant α
 P a » 1.073476469, with e ̌ and m̌ P of the same [ L3T−2 ]
and the Planck mass m̌ P , namely e = m
dimensions in Planck units, where m̌ P = 4p.

1. Introduction
The importance of the units of measure cannot be overstated. Correctly deﬁned systems of units no matter what
they are, describe the same physical reality; however, some are more useful than others depending on needs. This
is similar to sets of lenses ranging from microscopes, through wide angle camera lenses to astronomical
telescopes. However, systems of units unlike lenses may have different number of base units of measure which
can be referred to as dimensions. The evolution of systems of units has lasted for at least four centuries, closely
aligned with the progress of physical sciences. The question often arises of how many dimensions are needed and
what choice is the best. Although no system of measure changes physical reality some can enhance or obscure the
view of natural processes. The results of this research show that the choice of units of measure can lead to new
discoveries.
The International System of Units (SI) was established in 1960 with seven base units of measure and the
corresponding deﬁnitions of fundamental constants as in [1]. These include the unperturbed ground state

© 2023 The Author(s). Published by IOP Publishing Ltd

## PDF page 3

J. Phys. Commun. 7 (2023) 115001

A Wutke

hyperﬁne transition frequency of the cesium 133 atom ΔνCs, speed of light in vacuum c, Planck constant h,
elementary charge e, Boltzmann’s constant k, Avogadro’s constant NA, and luminous efﬁcacy Kcd.
The unit of mass in the SI is the kilogram, derived from the earlier unit of weight called the ‘gramme.’ The
kilogram prototype was then deﬁned as ‘the weight of a cubic decimeter of distilled water at its temperature of
maximum density and weighed in vacuo’(Hallock [2] p.62). This prototype was replicated in the famous
platinum-iridium alloy cylinder, which served as the legal standard for the kilogram, along with the meter
standard, which were established in 1799 (Hallock [2] p.63). This historical event led to the development of the
SI we have today.
The electric charge, originally referred to as ‘the quantity of electricity’ (Everett [3] p.161), was assigned a unit
of measure in the 19th century in the Centimeter-Gramme-Second (CGS) system actively supported by Maxwell
and Thomson [4] in 1873. Before that, in 1686, Newton deﬁned the ‘quantity of matter’ as ‘arising from its
density and bulk conjunctly,’ which he also called ‘mass’ in The Mathematic Principles of Natural Philosophy [5]
(also referred to as ‘The Principia ’). According to Jammer, the concept of mass was still debated issue at the time
[6] pp.64–74. In the ﬁrst (1873) edition of J. C. Maxwell’s Treatise on Electricity and Magnetism [7], it was
suggested that the unit of mass should be deﬁned based solely on time and length units:
In the dynamical theory of astronomy, the unit of mass is deduced from the units of time and
length, combined with the fact of universal gravitation. The astronomical unit of mass is that
mass, which attracts another body, placed at the unit of distance so as to produce in that body the
unit of acceleration. In framing a universal system of units we may either deduce the unit of mass
in this way from those of length and time already deﬁned, and this we can do to a rough approximation in the present state of science; [K] If, as in the astronomical system, the unit of mass is
deﬁned with respect to its attractive power, the dimensions of [M] are [L3T−2]. For the acceleration due to the attraction of a mass m at a distance r is by the Newtonian Law m/r2 ([7] sect 5 p.4).
It is worth noting Maxwell’s preference for the simplest possible representation of physical law evident from
the absence of any gravitational constant in this citation. This is consistent with the fact that Newton’s laws of
gravitation being represented verbally, as Haug [8] points out (e.g., in Proposition LXXVI, Theorem XXXVI,
and Corollary 3 in The Principia [5]). Considering this, it is possible to infer the simplest Newton’s law
expression, consistent with Maxwell’s comments, as shown in equation (1). Newton’s law can be transformed
into the equation of mass as a function of the angular velocity ω and radius of orbit r, and the dimensions of the
mass and force emerge naturally.
FN =

MN mN
M
= mN a  2N = w 2r  MN = w 2r 3,
2
r
r

(1)

where FN, MN, and mN are the Newtonian gravitational force and masses, respectively.
In this case, the mass of an object may be referred to as the ‘Newtonian mass’ MN, which has the dimensions
of [L3T−2]. For example, if we assume that the Moon moves on a circular orbit around Earth using average
parameters derived from NASA tables [9] such that r ≈ 3.844 000 × 108 m and ω ≈ 2.661 695 × 10−6s−1, we can
calculate the Earth’s mass as MN ≈ 4.024 083 × 1014 m3s−2. This value is approximately 0.955% different from
the accurately measured Earth’s geocentric gravitational constant GM, which is 3.986 004 418 × 1014m3s−2 ±
8 × 105m3 s−2 (McCarthy [10]).
In electrostatics, the CGS Electrostatic Unit (ESU) is a derived unit of the electric charge, constructed using
the Coulomb force equation in the form proposed by Maxwell [7] pp.42–43 without any additional constants.
FECGS =

q2
.
r2

(2)

Given that the CGS-derived unit of force dimensions are [dyne] = [MLT−2] (Everett [3] p.161), we can use
dimensional analysis to derive the dimensions of the electric charge q to ﬁnd that [q] = [M1/2L3/2T−1]. However,
in SI, the CGS tradition has not been followed, and the dimensions of the electric charge and Coulomb’s law are
expressed differently.
2

FESI =

1 qSI
.
4pe0 r 2

(3)

The equation form of (3) is referred to as ‘rationalized,’ and includes the 1/4π factor, which was inﬂuenced by
Giorgi [11] and originally insisted upon by Heaviside [12]. This rationalized form of the law causes 4π to appear
in physical equations in the context of spherical electric ﬁelds but not in uniform ﬁelds. As pointed out by
Heaviside [12] p.116, the number 4π becomes ‘obtrusively prominent’ in unexpected physical contexts, leading
to the impression of it being an ‘essential part of all electric and magnetic theories.’
2

## PDF page 4

J. Phys. Commun. 7 (2023) 115001

A Wutke

Heaviside [12] p.117 criticized the form of equation (2) without the 1/4π factor, as preferred by Maxwell, for
being ‘the origin of 4π absurdity’ in the CGS framework. Heaviside concluded quoting Maxwell, that
equation (2), which is the point source central force ﬁeld law without a ‘useless and absurd factor’([12] p.118),
with the addition of 1/4π being the best approach. The addition of 1/4π indicates that the spherical surface
increases with distance r, causing a reduction in the central force ﬁeld intensity by attenuation over the growing
area; for example, as for the ﬂux of heat [12] p.119. Thus we conclude that inverse square laws without a surface
area context are, simply, a mystery. Why ‘rationalization’ has not been introduced in the SI for the law of
universal gravitation, while it was for the electric charge, as seen in equation (3), is puzzling. This would only
require scaling the gravitational constant value by multiplying it by 4π and adding the factor 1/4π in front of SI
Newton’s law expression. Following Maxwell and Heaviside, it is possible to ‘rationalize’ the metric system to
achieve consistency and simplicity by eliminating the base units of mass and charge. This approach extends to
the standard Planck unit system, referred to as the Universal Planck Natural Unit System (UPNUS). It is
demonstrated that removing two base units of the kilogram and ampere does not lead to defective systems of
units, but, on the contrary, offers a better perspective on the relations among the constants of nature and
physical quantities, and a promising platform for uniﬁcation theories.
The rationality of the absence of a base unit of mass, as advocated by Maxwell, has been repeatedly discussed
in the literature. For example, in 1914, Buckingham [13] p.373 working from a different angle, rediscovered the
previously established fact that, from three base units in mechanical systems, one can be eliminated by the other
two when the law of gravitation is under consideration. This was already in effect in astronomy; for example, in
Treatise of Celestial Mechanics by La Place [14] (Part1 Book 2 pp.27–28), where no gravitational constant appears
in the presented differential equations of gravitational motion. Buckingham [13] made a valuable contribution
to the study of physically similar systems by showing when the [LT] units only are appropriate and when not.
The reduction to two dimensions is universally valid; however, it is practically troublesome owing to the low
accuracy of the gravitational constant G. The [MLT] system is adequate when gravitational effects are negligible;
however, [M] can be regarded as a secondary unit (rather than superﬂuous), although not as the primary base
unit. In 1933, Planck [15] pp.45–46, called the [L3T−2] unit ‘astronomical mass,’ and made the remark that
‘dimensions of a physical quantity are not inherent in it, but constitute a conventional property conditioned by
the choice of the system of measurement.’ In his opinion, this was not often appreciated, causing ‘unfruitful
controversies.’
More recently, in 2002, Fiorentini, Okun, and Vysotski [16] analyzed possible ways to eliminate the base unit
of mass. One identiﬁed method is to multiply each instance of the mass unit embedded in the dimensions of the
physical quantities by G — a transformation that in their opinion results in units with no fundamental character.
This conversion is similar to one of the transformations intended for the proposed system of units, as described
in section 2.2. Fiorentini, Okun, and Vysotski [16] do not comment on electromagnetic units, as gravitation
appears to be the main focus, and they also consider the possibility of replacing mass with its equivalent
Schwarzschild radius. In 2007, Matsas et al [17] contributed to an ongoing discussion on the sufﬁcient number
of dimensional fundamental constants in nature and justiﬁed by dimensional analysis that all observables can be
represented by [LT] units only, based on their argument that ‘all we can directly measure are space and time
intervals.’ They presented a formal protocol wherein multiplying every instance of any physical quantity
involving mass by G in the respective powers reduces the system to [LT]. They included no special protocol to
eliminate the unit of charge because this was already adopted as a derived unit and included mass in the CGS
system. The charge unit is automatically resolved by the protocol, similarly to any other physical quantity. In
2008, Veneziano [18] strongly supported two as the sufﬁcient number of fundamental constants and, therefore,
two base units, from the point of view of Quantum String theory. There seems to be a disagreement regarding
what constitutes the fundamental units in [16] and [17]. Indeed, generally speaking, the term ‘fundamental’ has
various interpretations. Weinberg [19] p.249 bluntly stated that ‘the membership of a list of ‘fundamental’
constants necessarily depends on who is compiling the list.’, Matsaset et al [17] presented a detailed
argumentation concluding that ‘the number of fundamental dimensional constants is two.’ This implies that all
observables can be expressed in terms of only two basic dimensional observables. Hence, the two dimensions
[LT] are sufﬁcient for describing physical processes in the current state of knowledge.
Apart from information published in peer-reviewed journals, there have also been attempts to build the
alternative systems of units in [LT] dimensions by independent researches on the popular scientiﬁc exchange
platform ResearchGate1 based on the same foundations.
The main aim of this paper is to recognize the weight of arguments from multiple sources justifying length
and time units as being sufﬁcient and fundamental and to ‘put them to the test’ by exposing how the physical
world would look like from this perspective.
1

Richard Jowsey The Geometry of Spacetime http://doi.org/10.13140/RG.2.1.2404.2320; Randy Sorokowski The Source of Interpretation
Issues in Physics https://researchgate.net/publication/341297059_The_Source_of_Interpretation_Issues_in_Physics

3

## PDF page 5

J. Phys. Commun. 7 (2023) 115001

A Wutke

2. Rationalized metric system
In line with our argument above that two dimensions are sufﬁcient to capture the basic reality of the physical
world, in this section, we construct the Rationalized Metric System (RMS) to demonstrate the point by analyzing
the impact this system has on dependencies among the constants of nature.
The RMS is intended as a platform for fundamental research to operate in two base units of length and time,
but not as a replacement for the SI, which was perfected over a period of 60 years and currently provides a solid
foundation for most applications in science, engineering, and everyday life.
2.1. Notation and symbols
To distinguish between the same physical quantities and constant symbols in SI, RMS, and UPNUS, the RMS
symbols have dashed accents above, such that m̅ , q ̅ , e ̅ , andF ̅ are used for the mass, charge, elementary charge,
and force, respectively. The same quantities in UPNUS are m̌ , q ̌, e ̌,andF ̌. Any other ‘undecorated’ physical
quantity symbols are deemed to be in SI units unless otherwise indicated.
The meanings of the subscripts are as follows:
e – electron, as in electron radius re
P – Planck qualiﬁer, as in Planck mass mP
B – Boltzmann qualiﬁer, as in Boltzmann constant kB
S – Stoney unit qualiﬁer, as in mS
pr – proton, as in proton mass mpr
E – ‘electrical’
G – ‘gravitational’
N – ‘Newtonian’
CGS – CGS system of units
SI – International System of Units
RMS – RMS system of units.
Other non-listed subscripts are evident in the local context. Physical quantities are represented by
traditionally accepted symbols. The generic electric charge symbol is q, whereas the elementary or electron
charge is denoted by e.
Numerical data are often shown for constants of nature in three systems of units for information purposes
only, to illustrate the magnitudes of interest. The SI constant values were sourced from CODATA 2018 [20] with
reference’s precision. Combinations of constants that involve the gravitational constant G have degraded
precision owing to the low accuracy of G and are not validated as formal reference values, but may show only up
to a maximum 6 digits precision after the decimal point following the CODATA convention applied to Planck
length, time, and mass. However, the CODATA 2018 [20] gravitational constant is only certain to 5 digits G =
6.674 30 × 10−11 m3 kg−1 s−2. Recent publications claim a much higher accuracy for G (13 digits) and for the
inverse of the ﬁne structure constant α −1 (14 digits); for example, Geiger [21] pp. 1, 60.
2.2. Eliminating the kilogram
The author initially intended to reuse Newton’s law, as deduced from the original description in The Principia [5]
and prompted by Maxwell’s suggestion (page 2), as in equation (1). However, considering Heaviside’s remarks
on the central source force ﬁelds, the 1/4π factor is introduced, as follows:
FGSI = G

M2
1 M̅ 2

=
F
.
̅
G
r2
4p r 2

(4)

This makes the inverse square law intuitive. The symbol M̅ may be referred to as ‘rationalized
Newtonian mass.’
Acceleration is not affected by eliminating the kilogram; hence
M
gSI = G 2
r

and

gRMS = gSI =

1 M̅
.
4p r 2

(5)

From the above, the conversion factor from SI units to RMS units is
Ckg =

M¯
= 4pG » 8.38717 ´ 10-10m3s-2kg-1
M

4

(6)

## PDF page 6

J. Phys. Commun. 7 (2023) 115001

A Wutke

2.3. Eliminating the coulomb
We begin with the SI variant of the Coulomb’s law for use in unit conversion:
2

FESI =

1 qSI
.
4pe0 r 2

(7)

Following Heaviside’s suggestions [12], equation (2) and Maxwell’s dislike of additional factors, the chosen
RMS representation of Coulomb’s law can be expressed as
F ̅E =

1 q̅2
,
4p r 2

(8)

as required by Heaviside [12]. Given that there is no electric permittivity of the vacuum constant ε0 in RMS, the
magnetic permeability of the vacuum must be μ0=c −2, as required by Maxwell’s equations. Unlike in SI, the
permeability of the vacuum in RMS is no longer contaminated by experimental error.
The gravitational-to-electric-force ratio of the two electrons in SI is given by the following equation:
1

e2

FESI
4pe0 r 2
=
» 4.16561´1042.
me2
FGSI
G

(9)

r2

Assigning the symbol e ̅ to the elementary charge and m̅ e to its mass in the RMS, the same force ratio from
equations (4) and (8) becomes
1 e ̅2

2
F ̅E
e2
= 4p r 2 = ̅ 2 » 4.16560 ´ 1042.
1 m̅ e
F ̅G
m̅ e

(10)

4p r 2

This is a squared charge-to-mass ratio, and the charge e ̅ dimensions are [m3s−2].
From equations (9) and (10), it follows that the elementary charge in the RMS becomes
e¯ = e

4pG
» 1.55935 ´ 10-18m3s-2.
e0

(11)

The SI to RMS conversion factor for the charge quantity is
Cc =

4pG
» 9.73270 m3s-2C-1.
e0

(12)

I¯
» 9.73270 m3s-3A-1.
I

(13)

q¯
=
q

For electric current, the factor is given by
CI =

2.4. Conversion from SI to RMS
For every dimensional constant value that has a kilogram unit in non-zero power in the associated dimensional
expression, the constant must be multiplied by the value of Ckg from equation (6) to the power of the kilogram.
Additionally, for every coulomb [As] at non-zero power, the constant must be multiplied by Cc from
equation (12) to the power of the coulomb [As]. To transform to symbolic expressions instead of values, the
constant expressions from equations (6) and (12) in respective powers should be used.
It is necessary to change the dimensions of the physical quantities when converting the physical equations or
constants from SI to RMS. In SI, most quantities in mechanics and electromagnetism can be expressed in
primary fundamental units2 as [QSI] = [M αLβT γI δ]; for RMS, this is [QRMS] = [M εLζ].
The conversion scheme is as follows:

[Q SI] = [kg amb sg Ad]  [QRMS] = [mb + 3(a + d ) sg- 2a - 3d ]
For example, for the charge density dimension:
[ρESI]=[m−3s A] => [ρERMS] =[m−3+3*(0+1) s1–2* 0 –3] =>[ρERMS ] = [s−2], which is the correct dimension
of density for both the mass and charge in the RMS.
In a more complex example of the vacuum electric permittivity constant ε0,
[ε0SI]=[kg−1m−3s4A2] =>[ε0RMS]=[m−3+3*(−1+2) s4−2*(−1)−3*2] = > [ε0RMS] =[m0s0] = 1.
2

Kelvin and candela are omitted here. Kelvin remains unchanged in RMS after conversion, with only the Boltzmann constant changing the
kilogram unit accordingly.

5

## PDF page 7

J. Phys. Commun. 7 (2023) 115001

A Wutke

To convert the physical equations from the SI to the RMS form:
• Gravitational constant G is replaced by 1/4π
• Vacuum magnetic permeability constant μ0 is replaced by c −2
• Vacuum electric permittivity constant ε0 is removed.
The side effects of numerical conversions have an impact on high-accuracy calculations using RMS
constants because the gravitational constant G degrades the original precision by many orders of magnitude. The
measurements will improve in time, and possibly a new theory would provide better values for G. Recent claims
by Geiger [21] pp. 1, 60 of approximating the inverse ﬁne structure constant α −1 at 14 digits precision and G at
13 digits precision would resolve the issue, if adopted by the CODATA.
2.5. The new perception of physical quantities in the RMS
Two signiﬁcant consequences were observed after eliminating the base units of mass and charge. First, as
described further below, this allows for the emergence of new relationships within the set of fundamental
constants. Second, it logically necessitates the propagation of any changes made in RMS, to the base units on the
Planck scale. The implications of this transformation are explained in detail in the following sections.
The unit system closest to the RMS is the Heaviside–Lorentz unit system (HLU; see [22] pp.22–24 for a
summary), which constitutes one of the CGS unit subsystems (CGS-HLU). In HLU, the electromagnetic units
are uniﬁed and rationalized; however, the creators stopped short of full uniﬁcation by failing to modify the
mechanical units, including the format of Newton’s law of gravitation. The RMS bridges this gap.
The HLU has its own natural units representation, similar to the Planck system, known as the Heaviside–
Lorentz natural unit system (with c = ħ = 1). This is commonly used instead of the Planck system in Quantum
Electrodynamics research; however, it shares the same problem of inconsistent rationalization.
2.5.1. Charge-to-mass ratio
The simpliﬁcation of the electrical-to-gravitational force ratio formula is the ﬁrst immediate effect of the RMS
system that reduces the ratio to the squared charge-to-mass ratio. The large difference in strength between
electric and gravitational ﬁelds has been the subject of discussion in elementary physics courses and numerous
scientiﬁc publications, including those by Feynman [23], Dicke [24], and Wilczek [25–27]. Feynman [23] used
the example of two electrons to illustrate the problem, stating that ‘The gravitational attraction relative to the
electrical repulsion between two electrons is 1 divided by 4.17 × 1042! The question is, where does such a large
number come from? It is not accidental [K].’
For Dicke [24], ‘The fact that the strength of the gravitational interaction is so different from other
interactions might tend to strengthen the belief that it is completely different from other forces.’ He justiﬁed this
by pointing out the lack of success in 35 years of attempt to construct a uniﬁed ﬁeld theory. Frank Wilczek also
commented on the same subject, focusing on protons in his Nobel Lecture [25]. This is an interesting context;
one that is described further below in section 2.6.
From the RMS perspective, Feynman’s question can be precisely answered. The gravitational force is weak
because protons or electrons have a much smaller mass than the charge, resulting in a disparity in the
corresponding ratio of the acting forces. This explanation is straightforward, but still does not explain the
underlying fundamental reason for the difference. In the SI, an explanation such as ‘smaller mass than charge’
does not make sense because of the different dimensions of mass and charge and the common belief that they are
not comparable. Popular sources such as Wikipedia3 even state that ‘From the point of view of Planck units, this
is comparing apples with oranges, because mass and electric charge are incommensurable quantities.’
However, the assertion of incommensurability between mass and charge arising only from unit conventions
is now refuted by the RMS, which achieves seamless uniﬁcation of the gravitational mass and electric charge
without the oddities of the fractional powers of the base units, such as [q]=[g1/2cm3/2s−1], as found in the CGSESU subsystem (Everett [3] p.161).
2.5.2. Classical electron radius
The classical electron radius in SI is
re =

3

e2
,
4pe0 me c 2

Wikipedia (2023, February). Planck Units [Online]. https://en.wikipedia.org/wiki/Planck_units

6

(14)

## PDF page 8

J. Phys. Commun. 7 (2023) 115001

A Wutke

and in RMS, it is
re =

e ̅2
.
4pm̅ e c 2

(15)

The interpretation of equation (15) is straightforward: the radius can be calculated as the ratio of the square
of the electron charge to its rest mass energy, obtained from the Einstein formula, and divided by 4π (from
Heaviside rationalization). However, interpreting SI equation (14) without remembering the rationale behind
its derivations is more challenging, because we need to explain the role of ε0 beyond it being a mere unit
conversion factor, which would then contradict its status as a constant of nature. Nonetheless, the situation is
even clearer in the original CGS-ESU subsystem, where the same radius is represented as re = e 2/me c 2, with an
obvious interpretation.
Thus, a particular algebraic manipulation result is worthy of further attention. The mass and charge are
interchangeable in terms of the RMS units. We can substitute the electron mass m̄e in equation (15) in place of its
charge e ̅ and derive a type of radius, denoted rme :
rme =

1 m̅ e2
1 m̅ e
1 4pGme
Gm
=
 rme =
= 2e.
4p m̅ e c 2
4p c 2
4p c 2
c

(16)

As expected, rme is related to the radius; in this case, it is the radius of the black hole of the electron mass.
However, this is, only half of the Schwarzschild radius (SCR), which leads to the question of why?
The SCR represents the black hole size when the escape velocity of a receding object calculated along the
radius is equal to the speed of light c. In contrast, rme is the radius at which a hypothetical particle moving
tangentially to a spherical surface4 is forced onto a circular orbit at the speed of light c. This can be deduced from
the following equation, using Newton’s law:
ar =

Gme
Gm
Gme
Gme
Gm
 w 2r = 2 e  w 2r 2 =
 c2 =
 r = 2 e = rme ,
2
r
r
r
r
c

(17)

where ω denotes the angular orbital velocity. The modiﬁed radius expression (16) used in RMS applies equally to
masses of any size. Haug [28] demonstrated that 1/2 of the SCR results from limiting the escape velocity to c, by
relativistic effects. However, in SI, substituting the charge with the mass to derive the radius is not a
straightforward process. Meier [29] p.235 identiﬁed rg º GM /c 2 as ‘gravitational radius’ in the context of
rotating black holes. However, this term is most frequently used as a synonym for the Schwarzschild radius (Ince
[30] p.69). Landau and Lipshitz [31] pp.301, 309) followed the same conventions, and make a relevant remark on
‘the basis for concluding that there must be a singularity of the space-time metric and that it is therefore
impossible for bodies to exist that have a ‘radius’ (for a given mass) that is less than the gravitational radius,’
stating that ‘this conclusion would be wrong’ (p.309).
Kittel et al [32] p.402 call rg ‘gravitational length’ and also note that its derivation is arrived at via analogy with the
classical electron radius expression, which is similar to what can be seen in equation (16), where this analogy emerges
because of the commensurability of the RMS mass and charge units. The physical meaning of the appearance of rg (or
rme in equation (16)) is not immediately clear. However, the clariﬁcation is attempted in section 5.
2.5.3. Planck constant and Planck-derived constants
The Planck constant h has now been assigned an exact value in the SI system, which in turn deﬁnes the values of
other constants, such as the Planck time, length, mass, and temperature. In this study, these are collectively
referred to as the ‘Planck-derived constants.’
The RMS Planck constant h after straightforward conversion is h ̅ = h4pG. Planck [33] introduced a
temperature constant related to the Boltzmann constant, along with the time, length, and mass constants. The
Boltzmann constant has the kelvin base unit embedded within it: [kB]=[kg m2 s−2 K−1].
In RMS, the Boltzmann constant can be expressed as
k¯B = kB 4pG » 1.15797 ´ 10-32m5s-4K-1.
(18)
The RMS Planck temperature can be derived using the following expressions:
TP =

1
kB

TP = T ̅P =

4

hc 5
1
 TP̅ =
2pG
4pGkB

4pGhc 5

( )
1

2p 4p

1 2
c 2hc̅ » 1.416784 ´ 1032 ,
k ̅B

This is a classical mechanics approach.

7



(19)

## PDF page 9

J. Phys. Commun. 7 (2023) 115001

A Wutke

while the meter, second, and kelvin base units in the RMS remain unchanged. With the elimination of the
kilogram, the expressions used to calculate the Planck-derived constants have been modiﬁed using the
procedure described above on section 2.4. Consequently, the values of all Planck-derived constants, except for
the Planck mass, remained unchanged in the RMS.
Table 1 Presents the results obtained by applying RMS conversion rules to these constants.
The conversion of the Planck-derived constants to RMS yielded several ﬁndings:
Table 1. Conversion of the Planck constant and Planck-derived constants to RMS.
SI formula

RMS formula / value

Deﬁned numerically
h = 6.626 070 15 × 10−34kgm2s −1
t p = Gh5

h ̅ = h4pG
h ̅ » 5.557 399 × 10−43 m5s−3
1
t p = 2p h ̅5

Name
Planck constant
Planck time

2pc

tp ≈ 5.391 247 × 10
Planck length

lp =

mP =

1
l p = 2p
−35

mp ≈ 2.176 434 × 10
Planck temperature

kg

TP ≈ 1.416 784 × 10 K
Planck unit relations
Fine structure constant

tP2

m
(23)

P

−17

m̅ P » 1.825 413 × 10

3 −2

ms

1
2h ̅ c = k ̅ m̅ P c 2
B

(24)

TP ≈ 1.416 784 × 10 K

32

lP3

(22)
−35

2ch ̅ = 4p t 2

1
TP = k ̅ c 2
B

hc 5
2pG

(21)

s

lP3

m̅ P =
−8

−44

h̅
2c 3

lp ≈ 1.616 255 × 10

m

ch
2pG

1
TP = k
B

2c

tp ≈ 5.391 247 × 10

s

Gh
2pc 3

lp ≈ 1.616 255 × 10
Planck mass

−44

(20)

32

lP3

= GmP

tP2

e2

a = 2pe hc
0

α ≈7.297 352 5693 × 10−3

1

= 4p m̅ P

e2
e2
a = 2ch̅ ̅  a = m̅ 2
̅P

(25)
(26)

α ≈ 7.297 352 5693 × 10−3

(1) The gravitational constant G is embedded directly only in the RMS value of the Planck constant h ̅ , which
affects the other constants, except for α where G cancels out.
(2) The Planck mass expression in equation (20) is remarkably simpler than that in SI.
(3) The Planck temperature expressions are straightforward and provide immediate insight into the meaning of
temperature, which is obscured in the SI deﬁnition. Speciﬁcally, equation (24) indicates that the Planck
temperature is equivalent to the total energy of the Planck rest mass converted to the absolute temperature
scale. This relationship also holds in the SI: Tp = mP c 2 /kB.
(4) The ﬁne structure constant α, expressed by equation (26), can be readily transformed into
a=

e̅2
.
m̅ P2

(27)

(5) This highlights the coupling between the elementary charge and the Planck mass, which is universally
signiﬁcant. Therefore, α can also be regarded as the charge-to-Planck-mass coupling constant in RMS, and
it likely represents the minimum limit of the squared charge-to-mass ratio for all the charged particles.
(6) While elementary charge is a tangible physical property, Planck-derived constants have been occasionally
criticized as mathematical artifacts arising from dimensional analysis, as noted by Haug [34]. Bridgman [35]
p.101 commented on Planck’s natural units as follows:
Until some essential connection is discovered between the mechanisms which are accountable
for the gravitational constant, the velocity of light, and the quantum, it would seem that no signiﬁcance whatever should be attached to the particular size of the units deﬁned in this way,
beyond the fact that the size of such units is determined by phenomena of universal occurrence.
[35] p.101.
In contrast, equation (27) demonstrates that the gravitational constant, velocity of light, quantum (h ̅ ), and
elementary charge are intimately interconnected. Hence, the Planck mass is not an artifact, but a meaningful
constant of nature that can alternatively be deﬁned from equation (27) as
8

## PDF page 10

J. Phys. Commun. 7 (2023) 115001

A Wutke

m̅ P =

e̅
.
a

(28)

Returning to the SI, the alternative deﬁnition of the Planck mass can be obtained as
4pG
e0

4pGmP = e

a

 mP =

e
.
4pGae0

(29)

2.6. Explaining why gravity is so feeble
In his Nobel Lecture, Frank Wilczek [25] argued that measuring the proton mass in Planck units leads to the
following relationship:
m pr ~ 10-18

hc
,
G

and then in such case:
[K] it makes no sense to ask ‘Why is gravity so feeble?’ Gravity, as the primary force, just is what it
is. The right question is the one we confront here: ‘Why is the proton so light?’
However, this explanation does not fully address Feynman’s question regarding the weakness of the
gravitational force of electrons, which has puzzled physicists for several decades. Prior to the Nobel Lecture,
Wilczek shed some light on this issue in two different ways [26, 27], presenting a nondimensional constant X (or
N in [27]) that could help explain the weakness of the gravitational force.
After expanding ħ in the original X formula, it takes the form:5

NºX=

2
Gm pr

hc / 2p

X » 6 ´ 10-39.

(30)

This is also known as the gravitational coupling constant αg, as described by Silk [36] in 1977.
The magnitude of X is of a similar order as the gravitational-to-electrical force ratio; hence, it may be key to
arrive at a complete explanation. In other words, the feebleness of gravity may be due not only to the mass of the
proton being too small, but also to the smallness of the gravitational coupling constant itself. The signiﬁcance of
X is explained in as ‘the fractional contribution of gravitational binding energy to the proton’s rest mass,’ which
does not seem to directly address Feynman’s question. However, by converting X to RMS units using the Planck
mass formula from equation (23), we obtain the following relations:
X=

X̅ =

2
Gm pr

hc / 2p

2

 X̅ =

4pG Gm pr 4p

4pG hc / 2p 4p

2
2
2
m̅ pr
m̅ pr
mpr
= 2 = 2 » 5.906149 ´ 10-39.
2hc̅
m̅ P
mP

(31)

The identity of X and αg established above, X ≡ αg, reveals that X is equal to the squared ratio of the proton
mass to the Planck mass, which now closely corresponds to the context presented in the Nobel Lecture, but this
still does not directly answer Feynman’s question. The squared mass ratio in equation (31) has already been
recognized in the literature as a coupling constant of the same kind, as exempliﬁed indirectly by Burrows and
Ostriker [37] and by Haug [38], who presented an analogous expression for the electron, anticipating a deeper
meaning of that constant. A satisfactory answer to this dilemma has been found through a new meaningful
relation, by using equation (31), then applying the derived alternative deﬁnition of the Planck mass from
equation (28):
X̅ = a g =

m̅ 2pr
m̅ 2pr
=
a
» 5.906149 ´ 10-39.
e ̅2
m̅ P2

5

(32)

Note: Wilczek used index p to refer to proton mass, but, to avoid confusion with the Planck mass index P, in this study, the index ‘pr’ is used
instead.

9

## PDF page 11

J. Phys. Commun. 7 (2023) 115001

A Wutke

In the SI, it becomes:
X º ag =

2
4pGae0 m pr

e2

» 5.906149 ´ 10-39.

(33)

The simplicity of the equivalent relations among the constants of nature in the RMS is clearly demonstrated
above. In conclusion:
1. X ≡ αg is, in fact, the gravitational mass-to-charge coupling constant, which is indeed signiﬁcant in the
context of Feynman’s question, but still does not explain much more than the already derived equation (10).
2. Wilczek’s intuition in recognizing the relevance of X was correct, overcoming the constraints imposed by the
kilogram and ampere units in understanding the natural and simple relations among physical constants.
3. The weakness of the gravitational force of the proton is that it has a much smaller mass than charge, as seen in
equation (32), which results in a disparity in forces. However, there is still no complete explanation for the
magnitude of this difference because equation (32) is merely a statement of fact, and Feynman’s question
remains unanswered; thus, Wilczek’s interpretation still holds.
4. The RMS relations among the fundamental constants are generally simpler than those in SI.
2.7. Einstein gravitational constant
The Einstein gravitational constant k = 8pG /c 4, which appears in Einstein ﬁeld equations, simply reduces to
k = 2/c 4, and general relativity can be pursued within space-time dimensions [LT] for all physical quantities
involved.
2.8. Possible link between magnetic induction and gravitation
It is interesting to note that the RMS units of the magnetic ﬁeld induction, denoted B, transformed from [kg A−1
s−2] in SI to [s−1] in the RMS, whereas the units of the electric ﬁeld, denoted E, changed from [kg m s−1 A−1] to
[m s−2]. Remarkably, the dimensions of E ̅ are equivalent to those of acceleration, which are exactly the same as
those of gravitational ﬁeld g. However, B ̅ has frequency or angular velocity dimension. Two separate scenarios
involving electrons should be considered to gain insights into these unusual unit associations. Scenario 1 is
illustrated in ﬁgure 1.
Suppose that an electron moves at a scalar velocity v into a uniform magnetic ﬁeld B in the absence of an
external electric ﬁeld. In this ﬁeld, electromagnetic induction has a scalar value of Be. The initial electron path is
perpendicular to induction vector B. At the point of entry, the Lorentz force FLis assumed to be of scalar
magnitude, as described by equation (34):

Figure 1. A free electron in the magnetic ﬁeld generating Lorentz force upon entry.

10

## PDF page 12

J. Phys. Commun. 7 (2023) 115001

A Wutke

FL = evBe  F ̅L = e ̅vB ̅e .

(34)

Let us now arbitrarily set the Lorentz force value equal to the repulsive force between an electron and an
abstract elementary charge e, at the distance of the classical electron radius re. Therefore, in the RMS, we have
F ̅L =

1 e ̅2
.
4p re2

(35)

Using the classical electron radius in the RMS from equation (15), the force equation becomes
F ̅L =

m̅ e c 2
.
re

(36)

The value of v can now be set to examine the value of B ̅e , which is necessary for generating a force of
magnitude F ̅L. For simplicity let us assume that v=c. Combining equations (34) and (36) yields the following
expression:
m̅ e c 2
mc
= e ̅cB ̅e  B ̅e = ̅ e » 52.125432506340961s-1.
re
e ̅re

(37)

In independent scenario 2 shown in ﬁgure2, let us assume that an uncharged point mass equal to the mass of
the electron is in gravitational orbit around the electron at radius re and calculate the angular velocity on the
orbit.

Figure 2. The point mass of the electron mass magnitude orbiting the electron ﬁxed in space.

The central electron was assumed to be ﬁxed in space to determine the angular velocity ω. For simplicity it is
assumed that the central electron mass is stationary to avoid the complications of the two-body problem.
Applying Newton’s law, ωe can be calculated as
w e2 re = G

me
 we =
re2

G

me
» 52.125432506295360s-1.
re3

(38)

The coincidence of nearly identical numerical results can be easily noticed. The absolute difference was
calculated as we - B ̅e = 5,471 ´ 10-11; that is, val (we )» val (B ̅ e ). This numerical coincidence in the values of
the two entirely different physical quantities, raises the question of why this has occurred—is this indeed a
coincidence or could the expression be reduced to an identity? To investigate, we consider equations (37) and
(38) and examine the nondimensional ratio that should reduce to 1 without contradiction:

(
11

e̅

m̅ e c
re
m
G r 3e
e

2

) º 1.

(39)

## PDF page 13

J. Phys. Commun. 7 (2023) 115001

A Wutke

It is easy to prove that equation (39) is true if the formula re = e¯ 2/(4p m¯ e c 2) is the RMS expression for the
classical electron radius—which is indeed the case, as given by equation (15).
In short, the ﬁndings in this section give rise to two key questions: Are magnetic and electrical ﬁelds related to
the gravitational ﬁeld? Can the uncovered identity be a clue to gaining more understanding?

3. The universal planck natural unit system
In 1899, Max Planck proposed a new system of units that did not rely on arbitrary objects, which is now known
as the Planck unit system. This system involves setting the values of certain fundamental constants to
nondimensional 1, allowing them to disappear from the equations and from the concern of mathematicians.
These constants include the following:
• The speed of light, c = 1
• The gravitational constant, G = 1
• The Planck constant, h = 1
• The Boltzmann constant kB = 1.
It is now widely accepted to use the reduced constant ħ = h/2π replacing the h originally deﬁned by Planck.
The common practice of reducing physical constants to nondimensional 1 for convenience, thus making
them disappear, is sometimes criticized. Wesson [39] p.117 argued that, in cosmological research, the use of
units like G ≡ 1 and c ≡ 1 should be avoided: although ‘Mathematically it is an acceptable trick which saves
labour. Physically it represents the loss of information and leads to confusion [K].’ In addition to eliminating
base units of mass and charge, one of the aims of UPNUS is to develop a Planck scale system that retains the
dimensionality of all physical constants, regardless of their numerical values, thus avoiding the misleading side
effects mentioned above (Wesson [39] p.117).
Notably, the original Planck unit system did not include a predeﬁned elementary charge constant. However,
the Stoney unit system [40], published in 1881, introduced the idea of setting the elementary ‘unit quantity of
electricity’ value to 1, together with the speed of light and gravitational constant. (The Stoney unit system is
discussed in the context of the elimination of the base unit of mass and charge in section 4). In UPNUS, the
elementary charge naturally emerges at a speciﬁc value as a result of unit conversion, rather than by assumption.
UPNUS proposes changes to the Planck unit system such that, instead of preselecting and assigning unit
values with no dimensions to physical constants, the base units for [LT] are deﬁned only by the Planck time and
length unit symbols. Additionally, the Planck temperature becomes another base unit, and all dimensional
constants, other than the two fundamental length and time units, scale naturally.
It is worth noting that all Planck-derived constants can be directly measured using the principle of the
Cavendish apparatus in a mode similar to the measurement of Earth’s density by Cavendish [41], as described by
Haug [34]. This implies that UPNUS does not necessarily depend on the measurement of the gravitational
constant. For further details, refer to section 6.
For convenience, let us denote the Planck units for length, time, and temperature ‘lpu,’ ‘tpu,’ and ‘Tpu’
respectively. The conversion factors from meters and seconds to the Planck units are then:

m2lpu =

1
[lpu m-1]
lP

s 2tpu =

1
[tpu s-1]
tP

K 2Tpu =

1
[Tpu K-1] ,
TP

Gh
, tP =
2pc 3

Gh
1
, TP =
5
2pc
kB

(40)

where in SI:
lP =

c 5h
.
2pG

To convert a constant from RMS to UPNUS, every meter, second, or kelvin symbol in the expanded
dimensional expression must be multiplied by the corresponding factor from the set of equations (40) in the
respective powers, either symbolically or with substituted numeric values of the SI constants.
12

(41)

## PDF page 14

J. Phys. Commun. 7 (2023) 115001

A Wutke

3.1. Effects of conversion to UPNUS
3.1.1. Speed of light
Similar to the original Planck unit system, the speed of light naturally emerges as c = 1 lpu tpu-1.
3.1.2. Planck constant
For the Planck constant, which is currently deﬁned as the exact value in SI, the RMS value is contaminated by the
uncertainty of G, as shown in the expression h ̅ = 4pGh. The formal conversion of h ̅ to UPNUS using the
factors from equation (40) yields
5

m2lpu ⎞
2
-3.
5

h = 4pGh ⎛⎜
⎟  h = 8p lpu tpu
3
⎝ s 2tpu ⎠

(42)

The value of h ̌ is now the exact dimensional mathematical constant independent of G. The Planck constant h
is currently deﬁned as exact in SI.
3.1.3. Planck mass
3

m2lpu ⎞
-2.
3
m̅ P = 4pGmP  m̌ P = 4pGmP ⎛⎜
⎟  m̌ P = 4p lpu tpu
2
2
s
tpu
⎝
⎠

(43)

3.1.4. Gravitational constant
The gravitational force equation form in UPNUS is
FǦ =

1 ̌
mM̌
.
4p r 2

(44)

The constant 1/4π in the RMS is the spherical symmetry factor, following the Heaviside [12] rationalization
concept; hence, Ǧ = 1, which is nondimensional.
3.1.5. Electron mass
The conversion process results in the following:
3

m2lpu ⎞
m̅ e = 4pGme  m̌ e = 4pGme ⎛⎜
⎟
2
⎝ s 2tpu ⎠
4pme
e =
» 5.259697 ´ 10-22lpu3tpu-2.
m
mP

(45)

The accuracy of the value is affected by both the measurement errors of me and the low precision of G in mP
— the same problem as in the original Planck unit system.
3.1.6. Fine structure constant
From equation (27), the conversion of the ﬁne structure constant from the RMS formula to UPNUS yields
a=

e ̅2
e 2̌
16ap 2
= 2 =
= a.
2
4p 4p
m̅ P
m̌ P

(46)

The ﬁne structure constant emerges as an identity; therefore, it is an independent input parameter to the
system. In other words, there is no deﬁnition of α in UPNUS matching the SI deﬁnition [1] p.128.
3.1.7. Elementary (electron) charge
Using equation (11) and performing formal conversion to UPNUS, taking the factors from equation (40) results
in
ě = e

4pG ⎛ m2lpu3 ⎞
e 2p 2
.
⎜
⎟  ě =
e0 ⎝ s 2tpu 2 ⎠
e0 ch

(47)

The value of the elementary charge expression thus has dimension and is independent of G. This can be further
simpliﬁed as follows:
e2 =

e 28p 2
e2
=
2 ´ 8p 2  e2 = a16p 2 lpu6tpu-4.
e0 ch
2e0 ch

13

(48)

## PDF page 15

J. Phys. Commun. 7 (2023) 115001

A Wutke

The squared charge in the UPNUS expression has the ﬁne structure constant α built into it. The elementary
charge e
in UPNUS is then reduced to
e = 4p a » 1.073476469lpu3tpu-2,

(49)

which is as accurate as the measured ﬁne structure constant. The important points to note are as follows:
1. In UPNUS, the elementary charge value and accuracy are determined solely by the ﬁne structure constant.
2. There is an apparent logical conﬂict between the exact value of the elementary charge set to be exact in SI and
the value of the elementary charge. In UPNUS, it depends on the accuracy of α. In contrast, the Planck
constant is exact in SI and UPNUS, and no such conﬂict exists. However, this can be resolved in SI because
the constants μ0 and ε0 are both functions of α and would have to be changed accordingly when a more
accurate value of α is found, while keeping the elementary charge value unchanged in SI without
inconsistencies in values dependent on charge.
3. While the ﬁne structure constant α is nondimensional, the electric charge dimensions [lpu3 tpu−2] must be
applied explicitly to the mathematical constant 4π, which then becomes identical numerically and
dimensionally to the UPNUS Planck mass from equation (43). It is then possible to assume that the electron
charge expression can be written as
 P a » 1.073476469lpu3tpu-2.
e = m

(50)

It is risky to assign a physical entity to a coincidental numerical value, such as in equation (50), but this is
algebraically proven by straightforward transformations of the equalities in equation (46). The elementary
charge property of the real physical entity is then coupled by the universal constant a with the Planck mass.
The Planck mass among other Planck units were of ‘no signiﬁcance’ for Bridgman [35] p101, which does not
seem to be the case. The higher complexity of the equivalent and harder to interpret expression in SI,
e = 2ae0 hc , is evident.
3.1.8. Boltzmann constant and Planck temperature
Using equations (18), (24), and (40) yields
Tp =
Tp̌ =

1 2
1
c 2hc̅ = c 2mP 
k ̅B
k ̅B

1 2
c mP (K 2Tpu) = 1Tpu.
kB̅

(51)

Additionally, the Boltzmann constant transforms into
k ̅B = kB 4pG  kB̌ = k ̅B ((K 2Tpu)-1m2lpu5s2tpu-4)
kB = 4p lpu5tpu-4Tpu-1.

(52)

4. The stoney unit system in the time-space domain
In 1874, George J Stoney delivered a presentation before section A. of the British Association at the Belfast
Meeting [40] p.51, where, for the ﬁrst time in the history of physics, he introduced the natural unit system. This
was 25 years before Max Planck published a similar system based on the discovery of the quantum of action,
known as the Planck constant h.
4.1. Stoney constants conversion to RMS
The expressions for the Stoney constants presented in the original publication [40] required conversion from the
antiquated original notation and units to a more contemporary form in CGS, as can be found in the publication
of Barrow [42] p.25. When converted to SI units, they become

14

tS =

Ge 2
4pe0 c 6

lS =

Ge 2
4pe0 c 4

## PDF page 16

J. Phys. Commun. 7 (2023) 115001

A Wutke

mS =

e2
.
4pe0 G

(53)

The conversion of the above to RMS units yields
tS =

G
4pe0

lS =

G
4pe0

m¯ S =

e¯
c3

4pG
e0

=

1
4p 4p

e¯
c2

4pG
e0

=

1
4p 4p

( )
( )

( )=
( )=
e¯
c3

1 ¯e
4p c 3

e¯
c2

1 ¯e
4p c 2

4pG
e º e¯ .
e0

1
e 4pG 4pG =
4pe0 G

(54)

Stoney units differ from Planck units by the constant ratio a (Barrow [42] p.25); for example,
mS / mP =m̅ S / m̅ P =

a.

(55)

Therefore, ms  mP , lS  lP , tS  tP .
4.2. The physical meaning of the Stoney mass
The original derivation of the Stoney mass was a dimensional-analysis-based operation (Barrow [42] p.25). A
previously unforeseen assembly of the fundamental constants appeared to Stoney [40] as an entity in the unit of
mass. Equation (54) in the RMS units is an interesting result, because it indicates that the mass unexpectedly
becomes the elementary charge. Stoney mass has always been considered somewhat of a mystery and various
opinions circulate about its physical meaning and signiﬁcance. For instance, Buczyna et al [43] p.7 state that:
It is interesting to note that the Stoney mass MS[K] allows the description of the gravitational
coupling constant as a fundamental electric charge to gravitational charge ratio e /MS = G .
However, this is useful from a metrology point of view only if the Stoney mass can be identiﬁed
with some fundamental mass, which is not the case today.6
The usefulness clause is critical. In another paper, Abdukadyrov [44] states that ‘Stony mass ms separates the
macrocosm and microcosm; i.e., this mass is the minimum value for the masses of ordinary bodies and the
maximum value for the masses of elementary particles.’
The conversion to RMS proves that the Stoney mass in equation (54) is nothing but ‘the’ elementary charge
—not a mass with the magnitude of the charge in RMS units. The SI and RMS operate within the set of standard
fundamental constants. If there were indeed another unknown genuine Stoney mass entity, it would have to
appear naturally as another combination of known constants, as is the case in the RMS version of the Planck
mass: m̅ P = 2ch ̅ . Unfortunately, the Stoney mass expression in equation (54) is reduced to only one constant
e ̅ that is already known, and appears to be of the wrong kind. The charge quantity hidden in the CGS and SI
representations of the Stoney mass emerges as a mass-equivalent form of the elementary charge. The confusion
in the SI and CGS expressions in kilograms/grams is an inherent problem of these systems of units, owing to the
incommensurability of charge and mass. This is a serious problem in contemporary metric systems when the
mistaken identity of a physical constant is possible; one that has misled scientists for more than a century. It is
difﬁcult to accept that an algebraically valid combination of physical constants can yield an invalid result. There
is no space in science for paradoxes and a rational explanation can and must be found.
The combination of the constants mSc 2 is often called the Stoney energy. This can be converted into the RMS
form of e ̅c 2. This expression has energy dimensions as is the case for the electron rest mass energy mc̅ 2. To
become the elementary charge e, the elementary charge quantity should be converted from RMS back to SI in
accordance with the charge conversion rule given by equation (11).
If the mass conversion factor was used instead of that for the charge, the Stoney mass would emerge in the SI
mass units, and thus, a change in the quantity type would occur. The conversion of the standalone expression
e ̅c 2 back to SI, formally yields ec 2, which has dimensions of [m2As−1], rather than energy in [kg m2 s−2], which is
wrong and of no use. This is because it is necessary for proper conversion to anticipate the type of converted
quantity in the SI. If energy is expected, then the Stoney mass rest energy appears again, which allows us to
propose the following conjecture:
The RMS relation E ̅S = e ̅c 2 represents the same physical amount of energy as the SI Stoney
energy ES = mSc2, and this is the ﬁnite electric ﬁeld energy of the electron.
6

These expressions are valid in the CGS units.

15

## PDF page 17

J. Phys. Commun. 7 (2023) 115001

A Wutke

We prove below the equivalence of energies, but the fact that this is ‘the ﬁnite electric ﬁeld energy of the
electron’ remains to be conﬁrmed by physical theory and experimental conﬁrmation. The proof of the energy
equivalence is as follows:
When converting a product of physical quantities, we may convert each quantity separately depending on its
kind and algebraically combine all resulting dimensional expressions, or convert the entire product based on the
combined dimensions in one step. Thus far, we have converted the Stoney mass quantity to
m̅ S = 4pGmS ,

(56)

However, we can encapsulate mSc2 as the energy ES, where [ES]=[kgm2.s−2]. From the conversion rules
described in section 2.4, it follows that only the kilogram must be converted. Hence,
E¯S = 4pGES  E¯S = 4pGms c 2 = m¯ S c 2 = ¯ec 2  [E¯S] = [m5s-4] and
¯ec 2 = ERMS = ESI 4pG  ec 2

4pG

e0 = E SI 4pG  E SI = c

2

e2

4pGe0 = E S

Q.E.D.

(57)

Thus, the energy equivalence of the Stoney Energy and ﬁeld energy of the electron to and from the SI is
proven. For the second part of the conjecture, we can state that:
1. There is currently no place for a Stoney particle in the Standard Model, and the most massive stable particle is
the neutron.
2. Stoney energy in SI units ES=mSc2 is converted to in RMS units, and
3. e ̅c 2 is an exclusive property of the electron charge, and
4. e ̅ is representative of the electric ﬁeld surrounding the electron; therefore it is reasonable to expect that e ̅c 2 is the
ﬁnite energy of the electron ﬁeld, in contrast to the inﬁnite energy alternative (resulting from the application of
Coulomb’s law to the electron as a point particle), the inﬁnity which Dirac [45] pp.149,168 tried to avoid.
5. The energy of the electric ﬁeld around an electron has never been proven to be inﬁnite in any experiment.
Thus, it rests on the community of physicists to take action and to deﬁnitely prove or disprove the proposed
conjecture on theoretical and experimental grounds. The conjecture resulted only from dimensional and metric
system analyses, and cross-validation is required.
If the conjecture is validated, then we know that not only the energy of the electric ﬁeld of the electron but
also the fundamental status of the gravitational constant G is elevated to an unsuspected role of limiting the
energy of the electric ﬁeld of the electron to a ﬁnite level (although conveniently hidden inside RMS and UPNUS
base units).
The statement by Buczyna et al [43] p.7 cited on page 15 can now be validated. The Stoney mass while not
being a fundamental mass of a particle, is a handle to the electron’s ﬁnite energy, and thereby reveals that the
‘gravitational coupling constant’ described as G = e /MS in CGS units, plays a fundamental role in
determining electron properties and cannot be dispensed with, even though it acts as a unit conversion constant
between mass and charge.
4.3. The physical meaning of the Stoney length
The Stoney length ls in the RMS equation (54) can be further transformed by multiplying the numerator and
denominator of the ls expression by the symbol of elementary charge e ̅ :
ls =

1 e̅
1 e ̅2
.
=
2
4p c
4p e ̅c 2

(58)

The above equation has the same structure as equation (15) for the classical electron radius; however, the
familiar factor, e ̅c 2, the Stoney energy, replaces the electron rest mass energy, m̅ e c 2. Because equation (16)
represents the electron’s gravitational radius rg ≡ rme equal to ½ of the SCR (as discussed on page 7), if one insists
on interpreting e ̅ as the Stoney mass m̅ S having the elementary charge magnitude, then the Stoney length could be
called the ‘gravitational radius’ of the Stoney mass, being ½ of its SCR. This is well known, but we did not derive it
from the explicit application of the SCR expression. Rather, it unexpectedly emerged from the deﬁnition of the
Stoney length ls in the classical electron radius-like expression. A particle of Stoney rest mass magnitude has not
been identiﬁed, let alone has the elementary charge, yet according to Gorelik [46] referring to Weyl [47]: ‘Having
found a solution for an electrically charged point mass (also known as the Reissner—Nordström solution), Weyl
[47] introduced the length rgm = Gm/c 2(gravitational radius of mass m) and rge = e G /c 2 (gravitational
radius of the electric charge e).’7 The rge is the Stoney length in CGS units, which is, 1/2 of the Stoney mass’ SCR
7

Gorelik’s expressions are in CGS units.

16

## PDF page 18

J. Phys. Commun. 7 (2023) 115001

A Wutke

under a different name. Thus, the general relativity approach of Weyl, Reissner, and Nordström, as stated in
[46], seems relevant in studies of the electron model, which could be pursued in the RMS, UPNUS, or equivalent
systems in the [LT] domain.
4.4. Stoney unit system in [LT] dimensions
The Stoney unit system is similar to the original Planck unit system, and the conversion process is the same as
that for UPNUS, with the only difference being the magnitudes and expressions deﬁning the units. Some
highlights of these differences are presented below.
Stoney units differ from Planck units in that the ratio of their respective length, time, and mass units is a ;
for example, lS /lP = a . Therefore, lS  l p.The change in the units’ expressions propagates to UPNUS-like
expressions and constants according to the rules of algebra.

h ̌ = 8p 2  hŠ = 8p 2 / a
e ̌ = m̌ P a  eŠ º m̌ SS = 4p
m̌ e = 4pme / mP  m̌ eS = 4pme / mS ,

(59)

Where subscript S designates the Stoney scale quantities. The units are Stoney units of length and time, in place
of the Planck units of UPNUS.

5. Electron radii predicted by special relativity?
In section 2.5.2, transforming the classical electron radius formula by substituting the electron charge with its
mass in RMS units yielded ½ SCR of the electron, which is algebraically correct, yet unexpected. To clarify the
physical meaning of such manipulated results, the origin of the SI expression (14) must ﬁrst be clariﬁed. The
derivation of the classical electron radius is widely known and includes an assumption about the electron charge
spatial distribution, which so far has not yet been validated. Due to the uncertainty, the derivation from the
electron self-energy models resulted in an approximate, representative, ‘truncated’ (Jackson [48] p.589) form, by
disregarding the coefﬁcient A of the order of one, which would normally be in front of the classical expression
(14) (Rohrlich [49] pp.124–125, Kittel et al [32] pp.278–279). The stripped classical re expression is claimed to be
representative of the upper radius limit because the coefﬁcient 0 < A < 1 depends on the assumed charge
distribution in the electron. One of the calculated coefﬁcients, A = 3/5, assumes a uniform distribution of charge
in the volume of the spherical particle, but a uniform spherical surface distribution yields A = ½ (Rohrlich [49]
pp.124–125). As a matter of convention, in the classical electron radius expression, A = 1. In the search for an
explanation, given the absence of ideas about charge or mass distribution in an electron size particle, the motion
of particles while they interact through their electric/gravitational ﬁelds was investigated for clues.
An abstract simpliﬁed model was considered. In this model, two point particles interact through their
central ﬁelds. According to Newton’s Shell Theorem, for a spherical surface distribution of mass, the ﬁeld
outside the sphere is equivalent to the ﬁeld of the point mass at its center. This is also true for the electric ﬁelds.
To prevent invoking complexity beyond the scope of this study, it is better to refer to the source and test particles
with electron (or positron) mass and/or charge properties to avoid making statements about real particles. The
abstraction is in the modeling of a thought experiment where
1. A source particle is ﬁxed in a stationary inertial frame.
2. The initial test particle velocity v = 0 on an arbitrary r axis at r coordinate r0 > 0 continues in accelerated
motion toward the source owing to the attractive force of the source particle at r = 0.
3. Either particle is a point particle of mass m̅ e and may or may not have opposite charges of magnitude e ̅ .
4. In the case of charged particles, the model does not include advanced features, such as magnetic ﬁeld
generation or emission of energy in the form of radiation.
5. The model includes an elementary special relativity extension consistent with Einstein’s kinetic energy
expression [50] p.170.
6. The charged particles interact according to the RMS Coulomb force expression, irrespective of the speed of
the test charge.
7. The uncharged particles interact according to the RMS Newton force expression, irrespective of the speed of
the test mass particle.
17

## PDF page 19

J. Phys. Commun. 7 (2023) 115001

A Wutke

Approximate models of this type are available in literature. For example, Terzis [51] described a ‘simple
concise relativistic modiﬁcation of the standard Bohr model for hydrogen-like atoms.’ The key point of the
approximation is that, while the accelerating particle gains relativistic inertia with increasing velocity taken into
account, the Coulomb force expression in equation (8) remains unaffected. This is based on the assertion of
French et al [52] p.232 that ‘Coulomb’s law correctly gives the force on the test charge, for any velocity of the test
charge (however high), provided the source charge is at rest.’ This principle has also been applied to a simpliﬁed
model of gravitationally attracting uncharged particles.
Assuming that the Coulomb force and Newton force equations do not vary with fast particle motion,

F ̅ (r ) = F ̅ (r ) = -

1 e ̅2
4p r 2

1 m̅ e 2
,
4p r 2

(60)

where F ̅ (r ) is a suitable differential expression for the inertial force, r is the distance between the centers of mass of
the particles, e ̅ is the elementary charge, and m̅ e i is the magnitude of the electron mass in RMS units. This problem
can be analyzed by solving the equation of motion of the test particle in the scenario illustrated in ﬁgure 3 below.

Figure 3. Test mass attracted by stationary source mass (the same applies to oppositely charged particles).

The following time-domain equations generalized for oppositely charged and uncharged particles describe
the dynamics of the test particle in the special relativity context:
1
g (v ) =
1 - v 2/ c 2
m¯ d (g (v (t )) v (t ))
F¯ (t ) = e

dt
dv (t )

F¯ (t ) =

m¯ e c 3 dt

(c 2 - v (t ) 2 ) 2

3

.

(61)

We can change the variables in the above equation to the r domain using the well-known relation
dv (t )
d 2r (t )
dv (r )
,
=
= v (r )
2
dt
dt
dr

(62)

and the differential formula (61) (after necessary algebraic simpliﬁcations) converts to
dv (r )

F¯ (r ) =

m¯ e c 3v (r ) dr

(c 2 - v (r ) 2 )3 / 2

.

(63)

The equation of motion is now given as a static velocity distribution over the r axis of the test particle as follows:
d v (r )

m¯ e c 3v (r ) dr

2
1 m¯e
,
=
(c 2 - v (r ) 2 )3 / 2
4p r 2

18

(64)

## PDF page 20

J. Phys. Commun. 7 (2023) 115001

A Wutke

where m̅e is a placeholder for either m̅ e or e ̅ , depending on the analyzed case, and has the following analytical
solution in the implicit form:
4p m¯ e c 3r + m¯e2 (C i r - 1) c 2 - v (r )2
m¯e2 r c 2 - v (r )2

= 0,

(65)

where Ci is an integration constant. Solving this equation with respect to v(r) yields the following test particle
velocity expressions:
-16p 2m̅ e2 c 4r 2 + Ci2 m̅e4 r 2 - 2C i m̅e4 r + m̅e4

v1 (r ) =

(C i r - 1) m̅e2

v 2 (r ) = -

c

-16p 2m̅ e2 c 4r 2 + Ci2 m̅e4 r 2 - 2C i m̅e4 r + m̅e4
(C i r - 1) m̅e2

c

(66)

The integration constant Cican be calculated by setting the boundary condition to r = r0 for r0 > 0, where the
velocity is set to zero. Substituting r0 for r and equating v1(r0) = 0, or v2(r0) = 0 yields two identical sets of
expressions for both v1 and v2:
C i1 =

Ci2 = -

4p m¯ e c 2r0 + m¯e2
m¯e2 r0

4p m¯ e c 2r0 - m¯e2
m¯e2 r0

(67)

Although Ci1 is always positive for all r0 0, the constant Ci2 changes its sign and becomes zero
at r0= m¯e2/(4p m¯ e c 2).
Under the electric ﬁeld attraction when m̅e is set to e ̅ , r0 becomes the classical electron radius from equation (15).
Under gravitational attraction, when m̅e is set to m̅ e , the model works for abstract gravitating point particles
with the electron mass, and r0 = m̅ e /(4pc 2) = ½ SCR of the electron mass, as shown in equation (16).
We have now exposed the classical electron radius expression without any explicit assumption regarding the
structural charge volume or surface density, and have found ½ of the SCR for a mass under gravitational
attraction without any deliberate manipulation, as in equation (16). The more signiﬁcant consequences of this
occurrence in the integration constant can be found in the complete valid solution presented below.
Considering the case of neutral particle attraction, which has the electron mass, by substituting Ci1 and Ci2
sequentially in the expressions for v1(r) and v2(r) from equation (66), we obtain two alternative forms of the
velocity equation for each constant. Only two equations resulting from v1(r) meet the criteria for attraction from
the positive r0, such that lim v11 (r ) = -c and lim v12 (r ) = -c . Only one of these two is a unique solution for the
r0

r0

velocity, with no singularities in r Î [0, r0] for the widest possible range of positive r0. The integration constant
that does not violate the above constraints of interest when applied to v1(r), is Ci2 from equation (67). Hence,
focusing on gravitational attraction, with m̅e set to m̅ e , we obtain
v12 (r ) = -

m¯ e (r0-r ) 8pc 2r0 r + m¯ e (r0-r )
c,
4pc 2r0 r + m¯ e (r0-r )

where:
⎧ r Î [0, r0]Ç r  r0 Ç r0 > 0
lim v12 (r ) = - c .
⎨
r0
⎩

(68)

This is subject to the exclusion of singularities and discontinuities that are yet to be determined.
Two possible anomalous regions exist in the solution. One point singularity is due to the zero value of the
denominator in equation (68), and the other is an interval or intervals of discontinuity when the expression
under the rightmost square root is negative:
S1: rsng =
D1: rdisc =

- m¯ e r0
m¯ e
Ç r0 >
= 1/ 2SCR
2
4pc r0 - m¯ e
4pc 2

- m¯ e r0
m¯ e
Ç r0 <
= 1/ 4SCR
8pc 2r0 - m¯ e
8pc 2

(69)

The singularity S1 for the velocity function v12(r) allows a vast valid nonsingular range of the linear trajectory
for the initial point r0: r Î [0, r0]Ç r0 Î (1/2SCR , +¥).
19

## PDF page 21

J. Phys. Commun. 7 (2023) 115001

A Wutke

The region limited by the discontinuity condition D1 is where the initial point r0 is less than ¼ SCR away
from r = 0 on the positive side of the axis. However, exploring this case is beyond the scope of the present study.
The ½ of the SCR plays a prominent limiting role in determining the point of singularity for the trajectory on
the negative side of the r axis in the gravitational attraction model, which cannot be physically reached because it
takes inﬁnite time to arrive at r = 0, let alone to continue to r < 0. Additionally, the closest position of this
singularity S1 to the origin of the r axis at r = 0 is
lim rsng (r0)=-

r 0 +¥

m̅ e
= - 1/ 2SCR
4pc 2

(70)

The presented model can be easily applied to charged attracting particles; however, analysis of this
interesting case is beyond the scope of this study. Although in the presented model the ½ SCR naturally emerges
from relativistic effects, it fails to become the spatial limitation of the trajectory initiated at r0 Î (1/2SCR , +¥),
which would be characteristic of a spherical rigid boundary, such that particles would collide at some distance
between the mass centers. This is most likely due to the simplistic nature of the proposed model; the general
relativity approach would probably be better to make conclusive judgments.
The expression rme = m̅ e /4pc 2 from equation (16) developed by analogy is a legitimate gravitational radius
for the electron mass, similar in principle but not in value to the classical electron radius. The ‘mechanical’
replacement in equation (16) is now justiﬁed. The physical signiﬁcance of these ﬁndings for real particles is yet to
be determined using more realistic models.

6. Metric systems without G
RMS and UPNUS are promising alternatives to SI for fundamental research. Using the derived units of charge and
mass with dimensions [m3s−2], these systems reveal simpliﬁed dependencies among fundamental constants and new
forms of relationships. To fully embrace this new approach, we must break with the tradition that a mass unit must be
relative to a man-made artifact—an understanding that was problematic until the Planck constant was made exact in
SI [1]. In fact, if the gravitational constant G had never been invented, we could have adopted an RMS-like system even
in the 19th century, as discussed by Maxwell [7], via an experimental setup similar to that used by Cavendish [41] for
Earth density measurements, which could have been used to determine the mass of a practical size standard in m 3s −2.
A simpliﬁed version of this experiment designed for educational purposes was described by Kurtis [53],
demonstrating the underlying simple torsion balance principle illustrated in ﬁgure 4 below.

Figure 4. Illustration of torsion balance apparatus principle.

20

## PDF page 22

J. Phys. Commun. 7 (2023) 115001

A Wutke

In this experiment, two large balls, M, simultaneously attract two small balls, m, which are connected by a
bar of length L and suspended symmetrically on quartz ﬁbers (or a wire). This opposes the torque generated by
gravitational forces F over arm L/2, causing rotation of the bar with small balls m from the zero-torque position
toward the large balls. At equilibrium, angle θ is reached after a series of damped oscillations of period T, and the
small balls stop at a distance r from the large balls.
The formula for determining G from the setup shown in ﬁgure 4 given in [53] is
G=

2Lp 2r 2q
.
MT 2

(71)

In the RMS, equation (71) naturally yields the rationalized Newtonian mass as follows:
1
2Lp 2r 2q
8Lp 3r 2q
=
 M̅ =
2
4p
MT
T2
̅

(72)

To directly measure Newtonian mass, Haug [8] p.184 used an equivalent formula (7) that does not account
for the 1/4π factor not present in the original Newtonian law.
The masses used in the experiment must be equal pairwise to the highest possible accuracy. It is important to
note that the unit of mass in the RMS is 1.192297 × 10 9 kg, which is approximately equal to 1.9 million metric
tons. For practical purposes, it may be necessary to preselect the desired practical standard weight for the larger
balls. This is only an illustration of the principle of the measurement, which could be applied to more complex
settings and devices.

7. Discussion
Several points highlight important features of the RMS and UPNUS worth some consideration.
1. The SI has been reﬁned over several decades and is well-suited for practical purposes. However, the use of
different systems is advantageous in fundamental research at the elementary particle level. This study
introduces two systems of units that can serve as platforms for fundamental research: the RMS and the
UPNUS. These systems no longer require base units of mass and charge; instead, they use derived mass and
charge units with dimensions [L3T−2]. Through these systems, simpliﬁed dependencies among fundamental
constants emerge, along with new forms of relationships.
2. The two developed systems of units, RMS and UPNUS, are rationalized in the sense deﬁned by Heaviside
[12], leading to a simpliﬁed electric-to-gravitational force ratio as a squared charge-to-mass nondimensional
ratio. For an electron particle, this is
e ̅2
» 4.165561 ´ 1042
m̅ e2

3. With lpu, tpu, and Tpu symbols designating Planck scale units of length, time, and absolute temperature
respectively, the values of the fundamental constants in UPNUS are
a. Speed of light c = 1 lpu tpu-1
b. Planck constant h = 8p 2 lpu5tpu-3

 P = 4p lpu3tpu-2
c. Planck mass m

 P a lpu3tpu-2
d. Elementary charge e = m
 e = 4pme /mP lpu3tpu-2
e. Electron mass m
f. Planck temperature TP = 1 Tpu
g. Boltzmann constant kB = 4p lpu5tpu-4Tpu-1.
4. Some interesting relations emerged in the RMS:
a. A simpler expression for Planck mass

m̅ P =
21

2ch ̅

## PDF page 23

J. Phys. Commun. 7 (2023) 115001

A Wutke

b. The simplest disentangled RMS instance of the ﬁne structure constant expression—which we might term
the ‘charge-to-Planck mass coupling constant’—was derived as

a=

e̅2
,
m̅ P2

as opposed to the SI-equivalent format
a=

e2
.
4p Ge0 mP2

This can also be interpreted as the minimum limit of the charge-to-mass squared ratio within the set of
elementary particles. From this, the simplest disentangled expression for the elementary charge in UPNUS emerges
as
 P a » 1.073476469lpu3tpu-2,
e = m

 P = 4p lpu3tpu-2.
where the UPNUS Planck mass is m
The compact form of the above expressions appears to be the materialization of Newton’s idea put forth in
‘Rules Reasoning in Philosophy’ stated in The Principia [5] p.384 Book III: ‘Nature is pleased with simplicity, and
affects not the pomp of superﬂuous causes.’
c. The above RMS expression can be used to provide an alternative deﬁnition of the Planck mass, which can
be retroﬁtted to the SI. However, it is more complex than the RMS expression

m
¯P =

e¯
 mP =
a

1
a

e2
4p Ge0

Moreover, the SI form also shows an immediate relation to the Stoney mass, as described in section 4.1, and
then the expression
ms
mP =
,
a
becomes equally simple because the Stoney Mass expression naturally appears.
d. By utilizing the presented equations involving the Planck constant, it becomes possible to challenge certain
criticisms of Planck units as arbitrary constructs that lack real signiﬁcance. Bridgman [35] p.101 argued
that ‘No signiﬁcance whatever should be attached to the particular size of the units deﬁned.’ However, by
deﬁning the Planck mass in terms of the established alternative universal constants of nature not present
in the original deﬁnition, we can see its irreducible connection with the electron, and hence refute
Bridgman’s claims. The same cannot be said for the Stoney mass, as it converts to the elementary charge
(see the paragraph below).
e. As described in section 4.2, the simpliﬁcation power of the RMS allowed us to uncover the mistaken
identity of the Stoney mass, which is proven to be nothing but a disguised elementary charge in SI units,
while in RMS this is an identity: m
¯ S º ¯e. In contrast, the SI Planck mass expression transforms into an
irreducible and less complex fundamental combination m̅ P = 2ch ̅ .
However, the Stoney mass concept is of utmost importance because the identity m
¯ S º e¯ prompted the
conjecture presented in section 4.2 on page 15 such that m
¯ S c 2 º ¯ec 2 represents the ﬁnite energy of the electron
ﬁeld in the RMS units—which is exactly what is commonly called the Stoney energy. This should be the subject
of future research.

8. Conclusions
1. Two time and length units [LT] are sufﬁcient to describe any physical process currently described by [MLTI]
units in the SI. The author believes that the two developed systems, RMS and UPNUS, provide a clear and
logical perspective on physical quantities and constants and a useful platform for studying their dependencies.
This is proven by the full explanation of the Stoney mass as nothing but the electron charge, misrepresented
22

## PDF page 24

J. Phys. Commun. 7 (2023) 115001

A Wutke

in SI owing to the incommensurability of the mass and charge units. However, the role of the Stoney mass
concept cannot be underestimated.
2. The Stoney mass related conjecture is proposed as a ﬁtting topic for broader discussion. The Stoney energy
appears to be equal to the energy of the electric ﬁeld of the electron; however, much remains to be explored
using RMS and UPNUS for other potential applications. One such example is the unexplained interplay
between the magnetic induction and the gravitational force of the electron, as described in section 2.8.
Further research and discussion in this area may provide valuable insights and pave the way for exciting
discoveries.
3. Different perspectives on the same physical quantities could provide valuable insights and aid in
comprehending the fundamental relationships in nature.
4. At this point in time, the highest-precision computations are not possible in RMS owing to the low precision
of the gravitational constant; however, this may change in the future. The precision of the RMS, and some
UPNUS, constants is only an issue of practicality.
5. The ‘feebleness’ of gravity discussed by Frank Wilczek in his Nobel Lecture [25] should not be interpreted as a
reason to disregard its fundamental existence at small scales. Although no longer explicitly present in the
physical equations, the gravitational constant G continues to play a critical role in the proposed Rationalized
Metric System and remains an essential element that is indirectly present in most physical quantities, of which
the kilogram was one of the base units in the SI. The reintroduction of early Newtonian gravitational mass as a
derived unit renewed its signiﬁcance in modern physics. Furthermore, gravitational properties are inherently
linked not only to the hypothetical Stoney energy but also to the real energy of the physically tangible electric
ﬁeld surrounding the electron. The strength of the attractive properties of space-time and mass, as
represented by G, is critical in binding galaxies, elementary charges, and other particles as one united whole.
G still remains a crucial component in our understanding of the natural world at both the largest and smallest
scales of the universe.

Acknowledgments
The author expresses sincere gratitude to Prof. Espen Gaader Haug from the Norwegian University of Life
Sciences for providing valuable information and engaging in insightful discussions that signiﬁcantly contributed
to the scope of this study. The author would also like to thank Editage (www.editage.com) and Elite Editing
(www.eliteediting.com.au) for English language editing.

Data availability statement
There is no special data other than information included in the publication and refrenced literature. The data
that support the ﬁndings of this study are available upon reasonable request from the authors.

ORCID iDs
Andrew Wutke

https://orcid.org/0000-0002-9983-7585

References
[1] Bureau International des Poids et Mesures 2022 The International System of Units (SI) Cedex, ISBN 978-92-822-2272-0
[2] Hallock W and Treadwell H T 1906 Outlines of the Evolution of Weights and Measures and the Metric System (The Macmillan Co)
[3] Everrett J D 1891 Illustrations of the C.G.S. System of Units (Macmillan and CO.)
[4] Thomson W et al 1873 First report of the committee for the selection and nomenclature of dynamical and electrical units,’ Forty-third
Meeting of the BritishAssociation for the Advancement of Science (JOHN MURRAY) 223
[5] Newton I 1848 The Mathematic Principles of Natural Philosophy (Daniel Adee)
[6] Jammer M 1997 The Concept of Mass in Classical and Modern Phsics (Dover Publications, Inc)
[7] Maxwell J C 1873 Treatise On Electricity and Magnetism Vol 1; Preliminary: section 5 4(Clarendon)
[8] Haug E G 2022 Newton did not invent or use the so called Newton’s gravitational constant; G, it has mainly caused confusion J. Mod.
Phys. 13 179–205
[9] NASA 2021 (December) Moon Fact Sheet. [Online]. https://nssdc.gsfc.nasa.gov/planetary/factsheet/moonfact.html
[10] McCarthy D D 1992 IERS Conventions Central Bureau of IERS - Observatoire de Paris (IERS Technical Note) 21, 1996
[11] R T G 1934 The Giorgi (M.K.S.) system of units Nature 133 597–8
[12] Heaviside O 1893 Electromagnetic Theory vol 1 (The D. Van Nostrand Company) 117–27
[13] Buckingham E 1914 On physically similar systems:illustration of the use of dimensional equations Phys. Rev. 4 372–5

23

## PDF page 25

J. Phys. Commun. 7 (2023) 115001

A Wutke

[14] La Place P S 1822 A Treatise of Celestial Mechanics (Dublin: H R. Milliken) 1
[15] Planck M 1933 Introduction to Theoretical Physics vol 1 (Macmillan and Co., Limited)
[16] Fiorentini G, Okun L and Vysotsky M 2002 Is G a conversion factor or a fundamental unit? JETP Lett. 76 485
[17] Matsas G et al 2007 The number of dimensional fundamental constants [Online]. https://arxiv.org/pdf/0711.4276v2.pdf
[18] Duff J G, Okun L B and Veneziano G 2002 [Online]. https://arxiv.org/pdf/physics/0110060v3.pdf
[19] Weinberg S 1983 Overview of theoretical prospects for understanding the values of fundamental The constants of physics. (Phil. Trans.
R.Soc.) A310, 249
[20] Tiesinga E et al 2021 CODATA recommendedvalues of the fundamental constants J. Phys. Chem. Ref. Data 50 45
[21] Geiger J A 2023 Measurement quantization Int. J. Geom. Meth. Mod. Phys. 20 1,60
[22] Gyllenbok J 2018 Encyclopaedia of Historical Metrology, Weights, and Measures 1 (Springer International Publishing AG)
[23] Feynman R 1963 www.feynmanlectures.caltech.edu. [Online]. https://feynmanlectures.caltech.edu/I_07.html
[24] Dicke R H 1958 Gravity an enigma J. Wash. Acad. Sci. 48 216–9
[25] Wilczek F 2005 Nobel lecture: asymptotic freedom: from paradox to paradigm Review of Moden Physics 77 867
[26] Wilczek F 2002 Four Big Questions with Pretty Good Answers [Online] http://arxiv.org/abs/hep-ph/0201222v2
[27] Wilczek F 2001 Scaling Mount Planck I: a view from the bottom Phys. Today 54 12
[28] Haug E G 2021 New full relativistic escape velocity and new Hubble related equation Phsics Essays 34 505
[29] Meier D L 2012 Black Hole Astrophysics: The Engine Paradigm. (Springer Science & Business Media)
[30] Ince M 1997 Dictionary of Astronomy (Taylor&Francis)
[31] Landau L D and Lifshitz E M 1996 Course of Theoretical Physics vol 2 (Butterworth- Heinenann)
[32] Kittel C et al 1965 Berkley Physics Course Volume 1 Mechanics (McGraw-Hill)
[33] Planck M 1899 Über irreversible Strahlungsvorgänge Sitzungsberichte der Königlich Preußischen Akademie derWissenschaften (Königlich
Preußischen Akademie derWissenschaften) 479–80
[34] Haug E G 2022 Planck units measured totally independently of big G Open Journal of Microphysics 12 56
[35] Bridgman P W 1931 Dimensional Analysis (Yale University Press) 101
[36] Silk J 1977 Cosmogony and the magnitude of the dimensionless gravitational coupling constant Nature 265 710–11
[37] Burrows A S and Ostriker J P 2014 Astronomical reach of fundamental physics Proc. Nat. 111 2409
[38] Haug E G 2018 Newton’s and Einstein’s gravity in a new perspective for planck masses and smaller sized objects International Journal of
Astronomy and Astrophysics 8 6–23
[39] Wesson P S 1980 The application of dimensional analysis to cosmology Space Sci. Rev. 27 117
[40] Stoney G J 1883 On the Physical Units of Nature The Scientiﬁc Proceedings of the Royal Dublin Society (The Roal Dublin Society) III,
54–8
[41] Cavendish H 1798 Experiments to determine the Density of the Earth Philosophical Transactions of the Royal Society of London (the
Royal Society of London) 469–526
[42] Barrow J D 1983 Natural units before planck Q. J. R. Astron. Soc. 24 24–6
[43] Buczyna J R, Unnikrishnan C S and Gillies G T 2010 Standard and derived Planck quantities: selected analysis and derivations
arXiv:1006.3241
[44] Abdukadyrov A 2023 Theoretical calculation of the gravitational constant using the elementary charge, speed of light, Z boson mass,
and relativistic mechanics World Journal of Physics 1 42–9
[45] Dirac P A M 1938 Classical Theory of radiating electrons Proc. of the Royal Society A 148–68
[46] Gorelik G 2002 Herman weyl and large numbers in relativistic cosmology Einstein Studies in Russia. (Birkhaeuser)
[47] Weyl H 1917 Zur Gravitationstheorie Ann. Phys. 54 117–45
[48] Jackson J D 1962 Classical Electrodynamics (Wiley)
[49] Rohrlich F 2007 Classical Charged Particles (World Scientiﬁc Publishing Company)
[50] Einstein A 1989 On the electrodynamics of moving bodies The Collected Papers of Albert Einstein Volume 2 (English) (Princeton
University Press) 170
[51] Terzis F A 2008 A simple relativistic Bohr atom Eur. J. Phys. 29 735–43
[52] French A P et al 1968 Special Relativity (The MIT Introductory Physics Series) (W.W Norton Company Inc.)
[53] Kurtis R 2011 Gravity and Gravitation (eBook) (SfC Publishing Co)

24
