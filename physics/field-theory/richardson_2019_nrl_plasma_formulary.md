Source: https://www.nrl.navy.mil/ppd/plasma-formulary/
PDF sha256: 037290d47c8ff043cad3c846dba42f7233037a7c9077f61343564472d8ccf31b
License: public domain in the United States (17 U.S.C. 105, a work of the United States Government)
Language: eng
Fidelity: machine-gated

# Transcription of richardson_2019_nrl_plasma_formulary.pdf

Transcription of `richardson_2019_nrl_plasma_formulary.pdf` in this directory, 72 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1, 9, 71 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 2-8, 10-70, 72 from the PDF's own text layer (pdftotext version 26.10.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

<b>2019 NRL PLASMA FORMULARY</b>
A. S. Richardson
Pulsed Power Physics Branch
Plasma Physics Division
Naval Research Laboratory
Washington, DC 20375
Supported by
The Office of Naval Research

## PDF page 2

CONTENTS
Numerical and Algebraic . . . . . . . . . . . . . . . . . . . .
Vector Identities

. . . . . . . . . . . . . . . . . . . . . . .

Differential Operators in Curvilinear Coordinates

. . . . . . . . .

3
4
6

Dimensions and Units . . . . . . . . . . . . . . . . . . . . . 10
International System (SI) Nomenclature
Metric Prefixes

. . . . . . . . . . . . . 13

. . . . . . . . . . . . . . . . . . . . . . . . 13

Physical Constants (SI) . . . . . . . . . . . . . . . . . . . . . 14
Physical Constants (cgs)

. . . . . . . . . . . . . . . . . . . . 16

Formula Conversion . . . . . . . . . . . . . . . . . . . . . . 18
Maxwell’s Equations . . . . . . . . . . . . . . . . . . . . . . 19
Electricity and Magnetism

. . . . . . . . . . . . . . . . . . . 20

Electromagnetic Frequency/Wavelength Bands
AC Circuits

. . . . . . . . . . 21

. . . . . . . . . . . . . . . . . . . . . . . . . 22

Dimensionless Numbers of Fluid Mechanics . . . . . . . . . . . . 23
Shocks

. . . . . . . . . . . . . . . . . . . . . . . . . . . 26

Fundamental Plasma Parameters
Plasma Dispersion Function

. . . . . . . . . . . . . . . . 28

. . . . . . . . . . . . . . . . . . 30

Collisions and Transport . . . . . . . . . . . . . . . . . . . . 31
Approximate Magnitudes in Some Typical Plasmas . . . . . . . . . 40
Ionospheric Parameters

. . . . . . . . . . . . . . . . . . . . 42

Solar Physics Parameters . . . . . . . . . . . . . . . . . . . . 43
Thermonuclear Fusion . . . . . . . . . . . . . . . . . . . . . 44
Relativistic Electron Beams . . . . . . . . . . . . . . . . . . . 46
Beam Instabilities . . . . . . . . . . . . . . . . . . . . . . . 48
Lasers . . . . . . . . . . . . . . . . . . . . . . . . . . . . 51
Atomic Physics and Radiation . . . . . . . . . . . . . . . . . . 53
Atomic Spectroscopy

. . . . . . . . . . . . . . . . . . . . . 59

Complex (Dusty) Plasmas

. . . . . . . . . . . . . . . . . . . 62

References . . . . . . . . . . . . . . . . . . . . . . . . . . 66
2

## PDF page 3

NUMERICAL AND ALGEBRAIC
Gain in decibels of 𝑃2 relative to 𝑃1
𝐺 = 10 log10 (𝑃2 /𝑃1 ).
To within two percent
(2𝜋)1/2 ≈ 2.5; 𝜋2 ≈ 10; 𝑒3 ≈ 20; 210 ≈ 103 .
Euler-Mascheroni constant1 𝛾 = 0.57722
Gamma Function Γ(𝑥 + 1) = 𝑥Γ(𝑥):
Γ(1/6) = 5.5663

Γ(3/5) = 1.4892

Γ(1/5) = 4.5908

Γ(2/3) = 1.3541

Γ(1/4) = 3.6256

Γ(3/4) = 1.2254

Γ(1/3) = 2.6789

Γ(4/5) = 1.1642

Γ(2/5) = 2.2182

Γ(5/6) = 1.1288

Γ(1/2) = 1.7725 = √𝜋

Γ(1)

= 1.0

Binomial Theorem (good for |𝑥| < 1 or 𝛼 = positive integer):
∞

𝛼
𝛼(𝛼 − 1) 2 𝛼(𝛼 − 1)(𝛼 − 2) 3
(1 + 𝑥)𝛼 = ∑ ( )𝑥𝑘 ≡ 1 + 𝛼𝑥 +
𝑥 +
𝑥 +…
𝑘
2!
3!
𝑘=0
Rothe-Hagen identity2 (good for all complex 𝑥, 𝑦, 𝑧 except when singular):
𝑛

𝑦
𝑥
𝑥 + 𝑘𝑧
𝑦 + (𝑛 − 𝑘)𝑧
(
)
(
)
𝑥
+
𝑘𝑧
𝑘
𝑛−𝑘
𝑦
+
(𝑛
−
𝑘)𝑧
𝑘=0
∑

=

𝑥+𝑦
𝑥 + 𝑦 + 𝑛𝑧
(
).
𝑥 + 𝑦 + 𝑛𝑧
𝑛

Newberger’s summation formula3 [good for 𝜇 nonintegral, Re (𝛼 + 𝛽) > −1]:
∞

(−1)𝑛 𝐽𝛼−𝛾𝑛 (𝑧)𝐽𝛽+𝛾𝑛 (𝑧)
𝜋
=
𝐽
(𝑧)𝐽𝛽−𝛾𝜇 (𝑧).
𝑛
+
𝜇
sin
𝜇𝜋 𝛼+𝛾𝜇
𝑛=−∞
∑

3

## PDF page 4

VECTOR IDENTITIES4
Notation: 𝑓, 𝑔, are scalars; A, B, etc., are vectors; 𝙏 is a tensor; 𝙄 is the unit
dyad.
(1)

A⋅B×C=A×B⋅C=B⋅C×A
= B×C⋅A = C⋅A×B = C×A⋅B

(2)

A × (B × C) = (C × B) × A = (A ⋅ C)B − (A ⋅ B)C

(3)

A × (B × C) + B × (C × A) + C × (A × B) = 0

(4)

(A × B) ⋅ (C × D) = (A ⋅ C)(B ⋅ D) − (A ⋅ D)(B ⋅ C)

(5)

(A × B) × (C × D) = (A × B ⋅ D)C − (A × B ⋅ C)D

(6)

∇(𝑓𝑔) = ∇(𝑔𝑓) = 𝑓∇𝑔 + 𝑔∇𝑓

(7)

∇ ⋅ (𝑓A) = 𝑓∇ ⋅ A + A ⋅ ∇𝑓

(8)

∇ × (𝑓A) = 𝑓∇ × A + ∇𝑓 × A

(9)

∇ ⋅ (A × B) = B ⋅ ∇ × A − A ⋅ ∇ × B

(10) ∇ × (A × B) = A(∇ ⋅ B) − B(∇ ⋅ A) + (B ⋅ ∇)A − (A ⋅ ∇)B
(11) A × (∇ × B) = (∇B) ⋅ A − (A ⋅ ∇)B
(12) ∇(A ⋅ B) = A × (∇ × B) + B × (∇ × A) + (A ⋅ ∇)B + (B ⋅ ∇)A
(13) ∇2 𝑓 = ∇ ⋅ ∇𝑓
(14) ∇2 A = ∇(∇ ⋅ A) − ∇ × ∇ × A
(15) ∇ × ∇𝑓 = 0
(16) ∇ ⋅ ∇ × A = 0
If 𝐞1 , 𝐞2 , 𝐞3 are orthonormal unit vectors, a second-order tensor 𝙏 can be written in the dyadic form
(17) 𝙏 = ∑

𝑖,𝑗

𝑇𝑖𝑗 𝐞𝑖 𝐞𝑗

In cartesian coordinates the divergence of a tensor is a vector with components
(18) (∇ ⋅ 𝙏)𝑖 = ∑ (∂𝑇𝑗𝑖 /∂𝑥𝑗 )
𝑗

[This definition is required for consistency with Eq. (29)]. In general
(19) ∇ ⋅ (AB) = (∇ ⋅ A)B + (A ⋅ ∇)B
4

## PDF page 5

(20) ∇ ⋅ (𝑓𝙏) = ∇𝑓 ⋅ 𝙏 + 𝑓∇ ⋅ 𝙏
Let r = i 𝑥 + j 𝑦 + k 𝑧 be the radius vector of magnitude 𝑟, from the origin to
the point 𝑥, 𝑦, 𝑧. Then
(21) ∇ ⋅ r = 3
(22) ∇ × r = 0
(23) ∇𝑟 = r/𝑟
(24) ∇(1/𝑟) = −r/𝑟3
(25) ∇ ⋅ (r/𝑟3 ) = 4𝜋𝛿(r)
(26) ∇r = 𝙄
If 𝑉 is a volume enclosed by a surface 𝑆 and 𝑑S = n𝑑𝑆, where n is the unit
normal outward from 𝑉,
(27) ∫ 𝑑𝑉∇𝑓 = ∫ 𝑑S𝑓
𝑉

𝑆

(28) ∫ 𝑑𝑉∇ ⋅ A = ∫ 𝑑S ⋅ A
𝑉

𝑆

(29) ∫ 𝑑𝑉∇ ⋅ 𝙏 = ∫ 𝑑S ⋅ 𝙏
𝑉

𝑆

(30) ∫ 𝑑𝑉∇ × A = ∫ 𝑑S × 𝐴
𝑉

𝑆
2

(31) ∫ 𝑑𝑉(𝑓∇ 𝑔 − 𝑔∇2 𝑓) = ∫ 𝑑S ⋅ (𝑓∇𝑔 − 𝑔∇𝑓)
𝑉

𝑆

(32) ∫ 𝑑𝑉(A ⋅ ∇ × ∇ × B − B ⋅ ∇ × ∇ × A)
𝑉

= ∫ 𝑑S ⋅ (B × ∇ × A − A × ∇ × B)
𝑆

If 𝑆 is an open surface bounded by the contour 𝐶, of which the line element
is 𝑑l,
(33) ∫ 𝑑S × ∇𝑓 = ∮ 𝑑l𝑓
𝑆

𝐶

5

## PDF page 6

(34) ∫ 𝑑S ⋅ ∇ × A = ∮ 𝑑l ⋅ A
𝑆

𝐶

(35) ∫(𝑑S × ∇) × A = ∮ 𝑑l × A
𝑆

𝐶

(36) ∫ 𝑑S ⋅ (∇𝑓 × ∇𝑔) = ∮ 𝑓𝑑𝑔 = − ∮ 𝑔 𝑑𝑓
𝑆

𝐶

𝐶

DIFFERENTIAL OPERATORS IN CURVILINEAR COORDINATES5
Cylindrical Coordinates (𝑟, 𝜃, 𝑧)
Differential volume
Line element
𝑑𝜏 = 𝑟 𝑑𝑟 𝑑𝜃 𝑑𝑧

𝑑𝐥 = 𝑑𝑟 𝐫 + 𝑟𝑑𝜃 𝛉 + 𝑑𝑧 𝐳

Relation to cartesian coordinates
𝑥 = 𝑟 cos 𝜃

𝐱 = cos 𝜃 𝐫 − sin 𝜃 𝛉

𝑦 = 𝑟 sin 𝜃

𝐲 = sin 𝜃 𝐫 + cos 𝜃 𝛉

𝑧=𝑧

𝐳=𝐳

Divergence
∇⋅A=
Gradient
(∇𝑓)𝑟 =

∂𝐴𝑧
1 ∂
1 ∂𝐴𝜙
(𝑟𝐴𝑟 ) +
+
𝑟 ∂𝑟
𝑟 ∂𝜙
∂𝑧
∂𝑓
;
∂𝑟

(∇𝑓)𝜙 =

1 ∂𝑓
;
𝑟 ∂𝜙

(∇𝑓)𝑧 =

Curl

∂𝐴𝜙
1 ∂𝐴𝑧
−
𝑟 ∂𝜙
∂𝑧
∂𝐴𝑟
∂𝐴𝑧
(∇ × A)𝜙 =
−
∂𝑧
∂𝑟
1 ∂𝐴𝑟
1 ∂
(𝑟𝐴𝜙 ) −
(∇ × A)𝑧 =
𝑟 ∂𝑟
𝑟 ∂𝜙
Laplacian
(∇ × A)𝑟 =

∇2 𝑓 =

6

∂𝑓
1 ∂ 2 𝑓 ∂2 𝑓
1 ∂
(𝑟 ) + 2 2 + 2
𝑟 ∂𝑟 ∂𝑟
𝑟 ∂𝜙
∂𝑧

∂𝑓
∂𝑧

## PDF page 7

Laplacian of a vector
𝐴
2 ∂𝐴𝜙
− 2𝑟
𝑟2 ∂𝜙
𝑟
𝐴𝜙
2 ∂𝐴𝑟
2
2
(∇ A)𝜙 = ∇ 𝐴𝜙 + 2
− 2
𝑟 ∂𝜙
𝑟
(∇2 A)𝑟 = ∇2 𝐴𝑟 −

(∇2 A)𝑧 = ∇2 𝐴𝑧
Components of (A ⋅ ∇)B
𝐴𝜙 ∂𝐵𝑟
𝐴𝜙 𝐵𝜙
∂𝐵𝑟
∂𝐵
+
+ 𝐴𝑧 𝑟 −
∂𝑟
𝑟 ∂𝜙
∂𝑧
𝑟
𝐴𝜙 ∂𝐵𝜙
𝐴𝜙 𝐵𝑟
∂𝐵𝜙
∂𝐵𝜙
(A ⋅ ∇B)𝜙 = 𝐴𝑟
+
+ 𝐴𝑧
+
∂𝑟
𝑟 ∂𝜙
∂𝑧
𝑟
𝐴𝜙 ∂𝐵𝑧
∂𝐵𝑧
∂𝐵𝑧
(A ⋅ ∇B)𝑧 = 𝐴𝑟
+
+ 𝐴𝑧
∂𝑟
𝑟 ∂𝜙
∂𝑧
Divergence of a tensor
𝑇𝜙𝜙
∂𝑇
1 ∂
1 ∂𝑇𝜙𝑟
(∇ ⋅ 𝙏)𝑟 =
(𝑟𝑇 ) +
+ 𝑧𝑟 −
𝑟 ∂𝑟 𝑟𝑟
𝑟 ∂𝜙
∂𝑧
𝑟
∂𝑇𝑧𝜙
𝑇𝜙𝑟
1 ∂
1 ∂𝑇𝜙𝜙
(∇ ⋅ 𝙏)𝜙 =
(𝑟𝑇 ) +
+
+
𝑟 ∂𝑟 𝑟𝜙
𝑟 ∂𝜙
∂𝑧
𝑟
∂𝑇𝑧𝑧
1 ∂
1 ∂𝑇𝜙𝑧
(∇ ⋅ 𝙏)𝑧 =
(𝑟𝑇 ) +
+
𝑟 ∂𝑟 𝑟𝑧
𝑟 ∂𝜙
∂𝑧
(A ⋅ ∇B)𝑟 = 𝐴𝑟

Spherical Coordinates (𝑟, 𝜃, 𝜙)
Differential volume
Line element
𝑑𝜏 = 𝑟2 sin 𝜃 𝑑𝑟 𝑑𝜃 𝑑𝜙

𝑑𝐥 = 𝑑𝑟 𝐫 + 𝑟𝑑𝜃 𝛉 + 𝑟 sin 𝜃𝑑𝜙 𝛟

Relation to cartesian coordinates
𝑥 = 𝑟 sin 𝜃 cos 𝜙

𝐱 = sin 𝜃 cos 𝜙 𝐫 + cos 𝜃 cos 𝜙 𝛉 − sin 𝜙 𝛟

𝑦 = 𝑟 sin 𝜃 sin 𝜙

𝐲 = sin 𝜃 sin 𝜙 𝐫 + cos 𝜃 sin 𝜙 𝛉 + cos 𝜙 𝛟

𝑧 = 𝑟 cos 𝜃

𝐳 = cos 𝜃 𝐫 − sin 𝜃 𝛉

Divergence
∇⋅A=

1 ∂ 2
1
∂
1 ∂𝐴𝜙
(𝑟 𝐴𝑟 ) +
(sin 𝜃𝐴𝜃 ) +
𝑟 sin 𝜃 ∂𝜃
𝑟 sin 𝜃 ∂𝜙
𝑟2 ∂𝑟
7

## PDF page 8

Gradient
(∇𝑓)𝑟 =
Curl

∂𝑓
;
∂𝑟

(∇𝑓)𝜃 =

1 ∂𝑓
;
𝑟 ∂𝜃

(∇𝑓)𝜙 =

1 ∂𝑓
𝑟 sin 𝜃 ∂𝜙

1
∂
1 ∂𝐴𝜃
(sin 𝜃𝐴𝜙 ) −
𝑟 sin 𝜃 ∂𝜃
𝑟 sin 𝜃 ∂𝜙
1 ∂𝐴𝑟
1 ∂
(∇ × A)𝜃 =
−
(𝑟𝐴𝜙 )
𝑟 ∂𝑟
𝑟 sin 𝜃 ∂𝜙
1 ∂
1 ∂𝐴𝑟
(∇ × A)𝜙 =
(𝑟𝐴𝜃 ) −
𝑟 ∂𝑟
𝑟 ∂𝜃
(∇ × A)𝑟 =

Laplacian
∇2 𝑓 =

∂𝑓
∂2 𝑓
1 ∂ 2 ∂𝑓
1
∂
1
(𝑟
)+ 2
(sin 𝜃 ) +
2
2
∂𝑟
∂𝜃
𝑟2 ∂𝑟
𝑟 sin 𝜃 ∂𝜃
2
𝑟 sin 𝜃 ∂𝜙

Laplacian of a vector
∂𝐴𝜙
2 cot 𝜃𝐴𝜃
2𝐴𝑟
2 ∂𝐴𝜃
2
− 2
−
− 2
𝑟2
𝑟 ∂𝜃
𝑟2
𝑟 sin 𝜃 ∂𝜙
𝐴𝜃
2 ∂𝐴𝑟
2 cos 𝜃 ∂𝐴𝜙
(∇2 A)𝜃 = ∇2 𝐴𝜃 + 2
−
−
2
2
𝑟 ∂𝜃
𝑟2 sin 𝜃 𝑟2 sin 𝜃 ∂𝜙
𝐴
∂𝐴𝑟
2
2 cos 𝜃 ∂𝐴𝜃
𝜙
+ 2
+
(∇2 A)𝜙 = ∇2 𝐴𝜙 −
2
2
𝑟2 sin 𝜃 𝑟 sin 𝜃 ∂𝜙
𝑟2 sin 𝜃 ∂𝜙
(∇2 A)𝑟 = ∇2 𝐴𝑟 −

Components of (A ⋅ ∇)B
𝐴𝜙 ∂𝐵𝑟
𝐴𝜃 𝐵𝜃 + 𝐴𝜙 𝐵𝜙
𝐴 ∂𝐵
∂𝐵𝑟
+ 𝜃 𝑟 +
−
∂𝑟
𝑟 ∂𝜃
𝑟
𝑟 sin 𝜃 ∂𝜙
cot 𝜃𝐴𝜙 𝐵𝜙
𝐴𝜙 ∂𝐵𝜃
∂𝐵𝜃
𝐴𝜃 ∂𝐵𝜃
𝐴𝜃 𝐵𝑟
+
+
−
(A ⋅ ∇B)𝜃 = 𝐴𝑟
+
∂𝑟
𝑟 ∂𝜃
𝑟
𝑟
𝑟 sin 𝜃 ∂𝜙
∂𝐵𝜙
𝐴𝜙 ∂𝐵𝜙
𝐴𝜙 𝐵𝑟
cot 𝜃𝐴𝜙 𝐵𝜃
𝐴𝜃 ∂𝐵𝜙
(A ⋅ ∇B)𝜙 = 𝐴𝑟
+
+
+
+
∂𝑟
𝑟 ∂𝜃
𝑟
𝑟
𝑟 sin 𝜃 ∂𝜙
(A ⋅ ∇B)𝑟 = 𝐴𝑟

Divergence of a tensor
(∇ ⋅ 𝙏)𝑟 =

1 ∂ 2
∂
1
(𝑟 𝑇𝑟𝑟 ) +
(sin 𝜃𝑇𝜃𝑟 )
𝑟 sin 𝜃 ∂𝜃
𝑟2 ∂𝑟
+

8

𝑇𝜃𝜃 + 𝑇𝜙𝜙
1 ∂𝑇𝜙𝑟
−
𝑟
𝑟 sin 𝜃 ∂𝜙

## PDF page 9

<math display="block">(\nabla \cdot \mathbf{T})_{\theta} = \frac{1}{r^2} \frac{\partial}{\partial r} (r^2 T_{r\theta}) + \frac{1}{r \sin \theta} \frac{\partial}{\partial \theta} (\sin \theta T_{\theta\theta})</math>
<math>+\frac{1}{r\sin\theta}\frac{\partial T_{\phi\theta}}{\partial\phi}+\frac{T_{\theta r}}{r}-\frac{\cot\theta T_{\phi\phi}}{r}</math>
<math display="block">(\nabla \cdot \mathbf{T})_{\phi} = \frac{1}{r^2} \frac{\partial}{\partial r} (r^2 T_{r\phi}) + \frac{1}{r \sin \theta} \frac{\partial}{\partial \theta} (\sin \theta T_{\theta\phi})</math>
<math>+\frac{1}{r\sin\theta}\frac{\partial T_{\phi\phi}}{\partial\phi}+\frac{T_{\phi r}}{r}+\frac{\cot\theta T_{\phi\theta}}{r}</math>
9

## PDF page 10

DIMENSIONS AND UNITS
To get the value of a quantity in Gaussian units, multiply the value expressed
in SI units by the conversion factor. Multiples of 3 in the conversion factors
result from approximating the speed of light 𝑐 = 2.9979 × 1010 cm/sec ≈
3 × 1010 cm/sec.
Dimensions
SI Units
SI Gaussian

Physical
Quantitiy

Symbol

Capacitance

𝑡2 𝑞2
ℓ
𝑚ℓ2
𝑚1/2 ℓ3/2
𝑞
𝑞
𝑡
𝑞
𝑚1/2
𝜌
ℓ3
ℓ3/2 𝑡
2
𝑡𝑞
ℓ
𝑚ℓ2 𝑡
𝑡𝑞2 1
𝜎
𝑚ℓ3 𝑡
𝑞
𝑚1/2 ℓ3/2
𝐼, 𝑖
𝑡
𝑡2
𝑞
𝑚1/2
J, j
ℓ2 𝑡 ℓ1/2 𝑡2
𝑚
𝑚
𝜌
ℓ3
ℓ3
𝑞
𝑚1/2
D
ℓ2
ℓ1/2 𝑡
𝑚ℓ 𝑚1/2
E
𝑡2 𝑞 ℓ1/2 𝑡
ℰ,
𝑚ℓ2 𝑚1/2 ℓ1/2
Emf 𝑡2 𝑞
𝑡
𝑚ℓ2 𝑚ℓ2
𝑈, 𝑊
𝑡2
𝑡2
𝑚
𝑚
𝑤, 𝜖
ℓ𝑡2
ℓ𝑡2

Charge
Charge
density
Conductance
Conductivity
Current
Current
density
Density
Displacement
Electric
field
Electromotance
Energy
Energy
Density
10

𝐶

Conversion Gaussian
Factor
Units

farad

9 × 1011

cm

coulomb

3 × 109

statcoulomb

coulomb
/m3

3 × 103

statcoulomb
/cm3

siemens

9 × 1011

cm/sec

siemens /m 9 × 109

sec−1

3 × 109

statampere

ampere /m2 3 × 105

statampere
/cm2

kg/m3

10−3

g/cm3

coulomb
/m2

12𝜋 × 105

statcoulomb
/cm2

ampere

volt/m
volt

1
× 10−4
3
1
× 10−2
3

statvolt/cm
statvolt

joule

107

erg

joule/m3

10

erg/cm3

## PDF page 11

Physical
Quantitiy

Symbol

Force

F

Frequency

𝑓, 𝜈

Impedance 𝑍
Inductance 𝐿

Dimensions
SI Units
SI Gaussian

Conversion Gaussian
Factor
Units

𝑚ℓ
𝑡2
1
𝑡
𝑚ℓ2
𝑡𝑞2
𝑚ℓ2
𝑞2

𝑚ℓ
𝑡2
1
𝑡
𝑡
ℓ
𝑡2
ℓ

newton

105

dyne

hertz

1

hertz

ℓ

ℓ

meter (m)

102

centimeter
(cm)

ampere–
turn/m

4𝜋 × 10−3

oersted

weber

108

maxwell

tesla

104

gauss

Length

ℓ

Magnetic
intensity

Magnetomotance

𝑞
ℓ𝑡
𝑚ℓ2
Φ
𝑡𝑞
𝑚
B
𝑡𝑞
𝑙2 𝑞
𝑚, 𝜇
𝑡
𝑞
M
ℓ𝑡
ℳ,
𝑞
Mmf 𝑡

𝑚1/2
ℓ1/2 𝑡
𝑚1/2 ℓ3/2
𝑡
𝑚1/2
ℓ1/2 𝑡
𝑚1/2 𝑙5/2
𝑡
𝑚1/2
ℓ1/2 𝑡
𝑚1/2 ℓ1/2
𝑡2

Mass

𝑚, 𝑀 𝑚

𝑚

𝑚ℓ
𝑡
𝑚
ℓ2 𝑡
𝑚ℓ
𝑞2

𝑚ℓ
𝑡
𝑚
ℓ2 𝑡

Magnetic
flux
Magnetic
induction
Magnetic
moment
Magnetization

H

Momentum p, P
Momentum
density
Permeability 𝜇

1

ohm
henry

1
× 10−11
9
1
× 10−11
9

sec/cm
sec2 /cm

ampere–m2 103

oersted–cm3

ampere–
turn/m

4𝜋 × 10−3

oersted

ampere–
turn

4𝜋
10

gilbert

kilogram
(kg)

103

gram (g)

kg–m/s

105

g–cm/sec

kg/m2 –s

10−1

g/cm2 –sec

henry/m

1
× 107
4𝜋

—

11

## PDF page 12

Physical
Quantitiy

Permittivity 𝜖
Polarization P
Potential

𝑉, 𝜙

Power

𝑃

Power
density
Pressure

Dimensions
SI Units
SI Gaussian

Symbol

𝑝, 𝑃

Reluctance ℛ

𝑡2 𝑞2
1
𝑚ℓ3
𝑞
𝑚1/2
2
ℓ
ℓ1/2 𝑡
𝑚ℓ2 𝑚1/2 ℓ1/2
𝑡2 𝑞
𝑡
𝑚ℓ2 𝑚ℓ2
𝑡3
𝑡3
𝑚
𝑚
ℓ𝑡3
ℓ𝑡3
𝑚
𝑚
ℓ𝑡2
ℓ𝑡2
𝑞2 1
𝑚ℓ2 ℓ
𝑚ℓ2 𝑡
𝑡𝑞2 ℓ
𝑚ℓ3
𝑡
𝑡𝑞2

Conversion Gaussian
Factor
Units

farad/m

36𝜋 × 109

—

coulomb
/m2

3 × 105

statcoulomb
/cm2

volt

1
× 10−2
3

statvolt

watt

107

erg/sec

watt/m3

10

erg/cm3 –sec

pascal

10

dyne/cm2

ampere–
4𝜋 × 10−9
turn /weber
1
ohm
× 10−11
9
1
ohm–m
× 10−9
9

cm−1

Resistance

𝑅

Resistivity

𝜂, 𝜌

Thermal
conductivity

𝜅, 𝑘

𝑚ℓ
𝑡3

𝑚ℓ
𝑡3

watt/m–deg
105
(K)

erg/cm–sec–
deg (K)

Time

𝑡

𝑡

𝑡

second (s)

1

second (sec)

𝑚ℓ
𝑡𝑞
ℓ
𝑡
𝑚
ℓ𝑡
1
𝑡
𝑚ℓ2
𝑡2

𝑚1/2 ℓ1/2
𝑡
ℓ
𝑡
𝑚
ℓ𝑡
1
𝑡
𝑚ℓ2
𝑡2

weber/m

106

gauss–cm

m/s

102

cm/sec

kg/m–s

10

poise

s−1

1

sec−1

joule

107

erg

Vector
potential

A

Velocity

v

Viscosity

𝜂, 𝜇

Vorticity

𝜁

Work

𝑊

12

sec/cm
sec

## PDF page 13

INTERNATIONAL SYSTEM (SI) NOMENCLATURE6
Physical
Quantity

Name
of Unit

Symbol
Physical Quantity
for Unit

Name
Symbol
of Unit for Unit

*length
*mass
*time
*current
*temperature
*amount of
substance
*luminous
intensity
†plane angle
†solid angle
frequency
energy
force
pressure
power
electric
charge
electric
potential

meter
kilogram
second
ampere
kelvin

m
kg
s
A
K

ohm

*SI base unit

mole

mol

candela

cd

radian
rad
steradian sr
hertz
Hz
joule
J
newton N
pascal
Pa
watt
W
coulomb C
volt

V

†Supplementary unit

electric resistance
electric
conductance
electric
capacitance
magnetic flux
magnetic
inductance
magnetic intensity
luminous flux
illuminance
‡activity (of a
radioactive
source)
§absorbed dose (of
ionizing
radiation)

Ω

siemens S
farad

F

weber

Wb

henry

H

tesla
lumen
lux

T
lm
lx

becquerel Bq

gray

Gy

‡Common non-SI unit is curie (Ci):
1 Ci = 3.7 × 1010 Bq
1 Bq = 1 decay per sec
§Common non-SI unit is rad:
100 rad = 1 Gy = 1 J / kG

METRIC PREFIXES
Multiple

Prefix

Symbol

Multiple

Prefix

Symbol

−1

deci
centi
milli
micro
nano
pico
femto
atto

d
c
m
μ
n
p
f
a

10
102
103
106
109
1012
1015
1018

deca
hecto
kilo
mega
giga
tera
peta
exa

da
h
k
M
G
T
P
E

10
10−2
10−3
10−6
10−9
10−12
10−15
10−18

13

## PDF page 14

PHYSICAL CONSTANTS (SI)7
Physical Quantitiy

Symbol

Value

𝑘
1.3807 × 10−23
𝑒
1.6022 × 10−19
𝑚𝑒
9.1094 × 10−31
𝑚𝑝
1.6726 × 10−27
𝐺
6.6726 × 10−11
ℎ
6.6261 × 10−34
ℏ = ℎ/2𝜋
1.0546 × 10−34
Speed of light in vacuum 𝑐
2.9979 × 108
Permittivity of free space 𝜖0
8.8542 × 10−12
Permeability of free space 𝜇0
4𝜋 × 10−7
Proton/electron mass ratio 𝑚𝑝 /𝑚𝑒
1.8362 × 103
Electron charge/mass ratio 𝑒/𝑚𝑒
1.7588 × 1011
𝑚𝑒4
Rydberg constant
𝑅∞ =
1.0974 × 107
8𝜖0 2 𝑐ℎ3
Bohr radius
𝑎0 =
5.2918 × 10−11
𝜖0 ℎ2 /𝜋𝑚𝑒2
Atomic cross section
𝜋𝑎0 2
8.7974 × 10−21
Classical electron radius
𝑟𝑒 = 𝑒2 /4𝜋𝜖0 𝑚𝑐2 2.8179 × 10−15
Thomson cross section
(8𝜋/3)𝑟𝑒 2
6.6525 × 10−29
Compton wavelength of
ℎ/𝑚𝑒 𝑐
2.4263 × 10−12
electron
ℏ/𝑚𝑒 𝑐
3.8616 × 10−13
Fine-structure constant
𝛼 = 𝑒2 /2𝜖0 ℎ𝑐
7.2972 × 10−3
−1
𝛼
137.038
First radiation constant
𝑐1 = 2𝜋ℎ𝑐2
3.7418 × 10−16
Second radiation constant 𝑐2 = ℎ𝑐/𝑘
1.4388 × 10−2
Stefan-Boltzmann
𝜎
5.6705 × 10−8
constant
Wavelength associated
𝜆0 = ℎ𝑐/𝑒
1.2398 × 10−6
with 1 eV
Frequency associated with 𝜈0 = 𝑒/ℎ
2.4180 × 1014
1 eV
Boltzmann constant
Elementary charge
Electron mass
Proton mass
Gravitational constant
Planck constant

14

Units
J K−1
C
kg
kg
m3 s−2 kg−1
Js
Js
m s−1
F m−1
H m−1
C kg−1
m−1
m
m2
m
m2
m
m

W m2
mK
W m−2 K−4
m
Hz

## PDF page 15

Physical Quantitiy
Wave number associated
with 1 eV
Energy associated with
with 1 eV
Energy associated with
1 m−1
Energy associated with
1 Rydberg
Energy associated with
1 Kelvin
Temperature associated
with 1 eV
Avogadro number
Faraday constant
Gas constant
Loschmidt’s number
(no. density at STP)
Atomic mass unit
Standard temperature
Atmospheric pressure
Pressure of 1 mm Hg
(1 torr)
Molar volume at STP
Molar weight of air
calorie (cal)
Gravitational acceleration

Symbol

Value

Units
5

m−1

𝑘0 = 𝑒/ℎ𝑐

8.0655 × 10

ℎ𝜈0

1.6022 × 10−19

J

ℎ𝑐

1.9864 × 10−25

J

𝑚𝑒3 /8𝜖0 2 ℎ2

13.606

eV

𝑘/𝑒

8.6174 × 10−5

eV

𝑒/𝑘

1.1604 × 104

K

𝑁𝐴
𝐹 = 𝑁𝐴 𝑒
𝑅 = 𝑁𝐴 𝑘
𝑛0

6.0221 × 1023
9.6485 × 104
8.3145
2.6868 × 1025

mol−1
C mol−1
J K−1 mol−1
m−3

𝑚ᵆ
𝑇0
𝑝0 = 𝑛0 𝑘𝑇0

1.6605 × 10−27
273.15
1.0133 × 105
1.3332 × 102

kg
K
Pa
Pa

𝑉0 = 𝑅𝑇0 /𝑝0
𝑀air

2.2414 × 10−2
2.8971 × 10−2
4.1868
9.8067

m3
kg
J
m s−2

𝑔

15

## PDF page 16

PHYSICAL CONSTANTS (CGS)7
Physical Quantitiy

Symbol

Value

Units

Boltzmann constant
Elementary charge

𝑘
𝑒

1.3807 × 10−16
4.8032 × 10−10

Electron mass
Proton mass
Gravitational constant

𝑚𝑒
𝑚𝑝
𝐺

9.1094 × 10−28
1.6726 × 10−24
6.6726 × 10−8

erg/deg (K)
statcoulomb
(statcoul)
g
g
dynecm2 /g2
erg-sec
erg-sec
cm/sec

Planck constant

ℎ
ℏ = ℎ/2𝜋
Speed of light in vacuum 𝑐
Proton/electron mass ratio 𝑚𝑝 /𝑚𝑒
Electron charge/mass ratio 𝑒/𝑚𝑒
2𝜋2 𝑚𝑒4
Rydberg constant
𝑅∞ =
𝑐ℎ3
Bohr radius
𝑎0 = ℏ2 /𝑚𝑒2
Atomic cross section
𝜋𝑎0 2
Classical electron radius
𝑟𝑒 = 𝑒2 /𝑚𝑐2
Thomson cross section
(8𝜋/3)𝑟𝑒 2
Compton wavelength of
ℎ/𝑚𝑒 𝑐
electron
ℏ/𝑚𝑒 𝑐
Fine-structure constant
𝛼 = 𝑒2 /ℏ𝑐
𝛼−1
First radiation constant
𝑐1 = 2𝜋ℎ𝑐2
Second radiation constant
Stefan-Boltzmann
constant
Wavelength associated
with 1 eV
Frequency associated with
1 eV
16

6.6261 × 10−27
1.0546 × 10−27
2.9979 × 1010
1.8362 × 103
5.2728 × 1017
1.0974 × 10

5

5.2918 × 10−9
8.7974 × 10−17
2.8179 × 10−13
6.6525 × 10−25
2.4263 × 10−10
3.8617 × 10−11
7.2972 × 10−3
137.038
3.7418 × 10−5

statcoul/g
cm−1
cm
cm2
cm
cm2
cm
cm

𝑐2 = ℎ𝑐/𝑘
𝜎

1.4388
5.6705 × 10−5

𝜆0

1.2398 × 10−4

ergcm2 /sec
cm-deg (K)
erg/cm2 sec-deg4
cm

𝜈0

2.4180 × 1014

Hz

## PDF page 17

Physical Quantitiy
Wave number associated
with 1 eV
Energy associated with
1 eV
Energy associated with
1 cm−1
Energy associated with
1 Rydberg
Energy associated with
1 deg Kelvin
Temperature associated
with 1 eV
Avogadro number
Faraday constant
Gas constant
Loschmidt’s number
(no. density at STP)
Atomic mass unit
Standard temperature
Atmospheric pressure
Pressure of 1 mm Hg
(1 torr)
Molar volume at STP
Molar weight of air
calorie (cal)
Gravitational acceleration

Symbol
𝑘0

Value
8.0655 × 10

Units
3

cm−1

1.6022 × 10−12

erg

1.9864 × 10−16

erg

13.606

eV

8.6174 × 10−5

eV

1.1604 × 104

deg (K)

𝑁𝐴
𝐹 = 𝑁𝐴 𝑒
𝑅 = 𝑁𝐴 𝑘

6.0221 × 1023
2.8925 × 1014
8.3145 × 107

𝑛0

2.6868 × 1019

mol−1
statcoul/mol
erg/degmol
cm−3

𝑚ᵆ
𝑇0
𝑝0 = 𝑛0 𝑘𝑇0

1.6605 × 10−24
273.15
1.0133 × 106
1.3332 × 103

g
deg (K)
dyne/cm2
dyne/cm2

𝑉0 = 𝑅𝑇0 /𝑝0
𝑀air

2.2414 × 104
28.971
4.1868 × 107
980.67

cm3
g
erg
cm/sec2

𝑔

17

## PDF page 18

FORMULA CONVERSION8
Here 𝛼 = 10 cm m , 𝛽 = 107 erg J−1 , 𝜖0 = 8.8542 × 10−12 F m−1 , 𝜇0 = 4𝜋 ×
10−7 H m−1 , 𝑐 = (𝜖0 𝜇0 )−1/2 = 2.9979 × 108 m s−1 , and ℏ = 1.0546 × 10−34 J s.
To derive a dimensionally correct SI formula from one expressed in Gaussian
̄ where 𝑘 ̄ is the counits, substitute for each quantity according to 𝑄̄ = 𝑘𝑄,
efficient in the second column of the table corresponding to 𝑄 (overbars denote variables expressed in Gaussian units). Thus, the formula 𝑎0̄ = ℏ2̄ /𝑚̄ 𝑒2̄
for the Bohr radius becomes 𝛼𝑎0 = (ℏ𝛽)2 /[(𝑚𝛽/𝛼2 ) (𝑒2 𝛼𝛽/4𝜋𝜖0 )], or 𝑎0 =
𝜖0 ℎ2 /𝜋𝑚𝑒2 . To go from SI to natural units in which ℏ = 𝑐 = 1 (distinguished
̂ 𝑄,̂ where 𝑘 ̂ is the coefficient corresponding to
by a circumflex), use 𝑄 = 𝑘−1
𝑄 in the third column. Thus 𝑎̂0 = 4𝜋𝜖0 ℏ2 /[( ̂
𝑚ℏ/𝑐)(𝑒2̂ 𝜖0 ℏ𝑐)] = 4𝜋/𝑚̂ 𝑒2̂ . (In
transforming from SI units, do not substitute for 𝜖0 , 𝜇0 , or 𝑐.)
2

−1

Physical Quantity

Gaussian Units to SI

Natural Units to SI

Capacitance
Charge
Charge density
Current
Current density
Electric field
Electric potential
Electric conductivity
Energy
Energy density
Force
Frequency
Inductance
Length
Magnetic induction
Magnetic intensity
Mass
Momentum
Power
Pressure
Resistance
Time
Velocity

𝛼/4𝜋𝜖0
(𝛼𝛽/4𝜋𝜖0 )1/2
(𝛽/4𝜋𝛼5 𝜖0 )1/2
(𝛼𝛽/4𝜋𝜖0 )1/2
(𝛽/4𝜋𝛼3 𝜖0 )1/2
(4𝜋𝛽𝜖0 /𝛼3 )1/2
(4𝜋𝛽𝜖0 /𝛼)1/2
(4𝜋𝜖0 )−1
𝛽
𝛽/𝛼3
𝛽/𝛼
1
4𝜋𝜖0 /𝛼
𝛼
(4𝜋𝛽/𝛼3 𝜇0 )1/2
(4𝜋𝜇0 𝛽/𝛼3 )1/2
𝛽/𝛼2
𝛽/𝛼
𝛽
𝛽/𝛼3
4𝜋𝜖0 /𝛼
1
𝛼

𝜖0 −1
(𝜖0 ℏ𝑐)−1/2
(𝜖0 ℏ𝑐)−1/2
(𝜇0 /ℏ𝑐)1/2
(𝜇0 /ℏ𝑐)1/2
(𝜖0 /ℏ𝑐)1/2
(𝜖0 /ℏ𝑐)1/2
𝜖0 −1
(ℏ𝑐)−1
(ℏ𝑐)−1
(ℏ𝑐)−1
𝑐−1
𝜇0 −1
1
(𝜇0 ℏ𝑐)−1/2
(𝜇0 /ℏ𝑐)1/2
𝑐/ℏ
ℏ−1
(ℏ𝑐2 )−1
(ℏ𝑐)−1
(𝜖0 /𝜇0 )1/2
𝑐
𝑐−1

18

## PDF page 19

MAXWELL’S EQUATIONS
Name or Description

SI

Gaussian

∂B
∂𝑡
∂D
∇×𝐇=
+𝐉
∂𝑡
∇⋅D=𝜌
∇⋅B=0

1 ∂B
𝑐 ∂𝑡
1 ∂D 4𝜋
∇×𝐇=
+
𝐉
𝑐 ∂𝑡
𝑐
∇ ⋅ D = 4𝜋𝜌
∇⋅B=0

Lorentz force on charge 𝑞

𝑞 (E + 𝐯 × B)

𝑞 (E +

Constitutive relations

D = 𝜖E
B = 𝜇𝐇

Faraday’s law
Ampère’s law
Poisson equation
[Absence of magnetic
monopoles]

∇×E=−

∇×E=−

1
𝐯 × B)
𝑐
D = 𝜖E
B = 𝜇𝐇

In a plasma, 𝜇 ≈ 𝜇0 = 4𝜋 × 10−7 H m−1 (Gaussian units: 𝜇 ≈ 1). The
permittivity satisfies 𝜖 ≈ 𝜖0 = 8.8542 × 10−12 F m−1 (Gaussian: 𝜖 ≈ 1)
provided that all charge is regarded as free. Using the drift approximation
𝐯⟂ = E × B/𝐵 2 to calculate polarization charge density gives rise to a dielectric constant 𝐾 ≡ 𝜖/𝜖0 = 1 + 36𝜋 × 109 𝜌/𝐵2 (SI) = 1 + 4𝜋𝜌𝑐2 /𝐵 2 (Gaussian),
where 𝜌 is the mass density.
The electromagnetic energy in volume 𝑉 is given by
𝑊=

1
∫ 𝑑𝑉(𝐇 ⋅ B + E ⋅ D)
2 𝑉

(SI)

=

1
∫ 𝑑𝑉(𝐇 ⋅ B + E ⋅ D)
8𝜋 𝑉

(Gaussian).

Poynting’s theorem is
∂𝑊
+ ∫ 𝐍 ⋅ 𝑑𝐒 = − ∫ 𝑑𝑉𝐉 ⋅ E,
∂𝑡
𝑆
𝑉
where 𝑆 is the closed surface bounding 𝑉 and the Poynting vector (energy
flux across 𝑆) is given by 𝐍 = E × 𝐇 (SI) or 𝐍 = 𝑐E × 𝐇/4𝜋 (Gaussian).

19

## PDF page 20

ELECTRICITY AND MAGNETISM
In the following, 𝜖 = dielectric permittivity, 𝜇 = permeability of conductor,
𝜇′ = permeability of surrounding medium, 𝜎 = conductivity, 𝑓 = 𝜔/2𝜋 =
radiation frequency, 𝜅𝑚 = 𝜇/𝜇0 and 𝜅𝑒 = 𝜖/𝜖0 . Where subscripts are used,
‘1’ denotes a conducting medium and ‘2’ a propagating (lossless dielectric)
medium. All units are SI unless otherwise specified.
Permittivity of free space
Permeability of free space
Resistance of free space
Capacity of parallel plates of area 𝐴,
separated by distance 𝑑
Capacity of concentric cylinders of
length 𝑙, radii 𝑎, 𝑏
Capacity of concentric spheres of
radii 𝑎, 𝑏
Self-inductance of wire of length 𝑙,
carrying uniform current
Mutual inductance of parallel wires
of length 𝑙, radius 𝑎, separated by
distance 𝑑
Inductance of circular loop of radius
𝑏, made of wire of radius 𝑎, carrying
uniform current
Relaxation time in a lossy medium
Skin depth in a lossy medium
Wave impedance in a lossy medium
Transmission coefficient at
conducting surface9 (good only for
𝑇 ≪ 1)
Field at distance 𝑟 from straight wire
carrying current 𝐼 (amperes)
Field at distance 𝑧 along axis from
circular loop of radius 𝑎 carrying
current 𝐼
20

𝜖0 = 8.8542 × 10−12 F m−1
𝜇0 = 4𝜋 × 10−7 H m−1
= 1.2566 × 10−6 H m−1
𝑅0 = (𝜇0 /𝜖0 )1/2 = 376.73 Ω
𝐶 = 𝜖𝐴/𝑑
𝐶 = 2𝜋𝜖𝑙/ ln(𝑏/𝑎)
𝐶 = 4𝜋𝜖𝑎𝑏/(𝑏 − 𝑎)
𝐿 = 𝜇𝑙/8𝜋
𝐿 = (𝜇′ 𝑙/4𝜋) [1 + 4 ln(𝑑/𝑎)]

𝐿 = 𝑏 {𝜇′ [ln(8𝑏/𝑎) − 2] + 𝜇/4}

𝜏 = 𝜖/𝜎
𝛿 = (2/𝜔𝜇𝜎)1/2 = (𝜋𝑓𝜇𝜎)−1/2
1/2
𝑍 = [𝜇/(𝜖 + 𝑖𝜎/𝜔)]
−4
𝑇 = 4.22 × 10 (𝑓𝜅𝑚1 𝜅𝑒2 /𝜎)1/2

𝐵𝜃 = 𝜇𝐼/2𝜋𝑟 tesla
= 0.2𝐼/𝑟 gauss (𝑟 in cm)
𝐵𝑧 = 𝜇𝑎2 𝐼/[2(𝑎2 + 𝑧2 )3/2 ]

## PDF page 21

ELECTROMAGNETIC FREQUENCY/WAVELENGTH BANDS10
Frequency Range
Designation

Lower

ULF*
VF*
ELF
VLF
LF
MF
HF
VHF
UHF
SHF†
S
G
J
H
X
M
P
K
R
EHF
Submillimeter
Infrared
Visible
Ultraviolet
X Ray
Gamma Ray

30 Hz
300 Hz
3 kHz
30 kHz
300 kHz
3 MHz
30 MHz
300 MHz
3 GHz
2.6
3.95
5.3
7.05
8.2
10.0
12.4
18.0
26.5
30 GHz
300 GHz
3 THz
430 THz
750 THz
30 PHz
3 EHz

Wavelength Range

Upper

Lower

30 Hz
300 Hz
3 kHz
30 kHz
300 kHz
3 MHz
30 MHz
300 MHz
3 GHz
30 GHz
3.95
5.85
8.2
10.0
12.4
15.0
18.0
26.5
40.0
300 GHz
3 THz
430 THz
750 THz
30 PHz
3 EHz

10 Mm
1 Mm
100 km
10 km
1 km
100 m
10 m
1m
10 cm
1 cm
7.6
5.1
3.7
3.0
2.4
2.0
1.67
1.1
0.75
1 mm
100 μm
700 nm
400 nm
10 nm
100 pm

Upper
10 Mm
1 Mm
100 km
10 km
1 km
100 m
10 m
1m
10 cm
11.5
7.6
5.7
4.25
3.7
3.0
2.4
1.67
1.1
1 cm
1 mm
100 μm
700 nm
400 nm
10 nm
100 pm

In spectroscopy the angstrom (Å) is sometimes used (1Å = 10−8 cm = 0.1 nm).
*The boundary between ULF and VF (voice frequencies) is variously defined.
†The SHF (microwave) band is further subdivided approximately as shown.11
21

## PDF page 22

AC CIRCUITS
For a resistance 𝑅, inductance 𝐿, and capacitance 𝐶 in series with a voltage
source 𝑉 = 𝑉0 exp(𝑖𝜔𝑡) (here 𝑖 = √−1), the current is given by 𝐼 = 𝑑𝑞/𝑑𝑡,
where 𝑞 satisfies
𝐿

𝑑2 𝑞
𝑑𝑞
𝑞
+𝑅
+ = 𝑉.
𝑑𝑡
𝐶
𝑑𝑡2

Solutions are 𝑞(𝑡) = 𝑞𝑠 + 𝑞𝑡 , 𝐼(𝑡) = 𝐼𝑠 + 𝐼𝑡 , where the steady state is 𝐼𝑠 =
𝑖𝜔𝑞𝑠 = 𝑉/𝑍 in terms of the impedance 𝑍 = 𝑅 + 𝑖(𝜔𝐿 − 1/𝜔𝐶) and 𝐼𝑡 = 𝑑𝑞𝑡 /𝑑𝑡.
For initial conditions 𝑞(0) ≡ 𝑞0 = 𝑞0̄ + 𝑞𝑠 , 𝐼(0) ≡ 𝐼0 , the transients can be of
three types, depending on Δ = 𝑅2 − 4𝐿/𝐶:
(a) Overdamped, Δ > 0.
𝐼 + 𝛾+ 𝑞0̄
𝐼 + 𝛾− 𝑞0̄
𝑞𝑡 = 0
exp(−𝛾− 𝑡) − 0
exp(−𝛾+ 𝑡),
𝛾+ − 𝛾−
𝛾+ − 𝛾−
𝛾 (𝐼 + 𝛾+ 𝑞 ̄0 )
𝛾 (𝐼 + 𝛾− 𝑞 ̄0 )
𝐼𝑡 = + 0
exp(−𝛾+ 𝑡) − − 0
exp(−𝛾− 𝑡).
𝛾+ − 𝛾−
𝛾+ − 𝛾−
(b) Critically damped, Δ = 0.
𝑞𝑡 = [𝑞 ̄0 + (𝐼0 + 𝛾𝑅 𝑞 ̄0 )𝑡] exp(−𝛾𝑅 𝑡),
𝐼𝑡 = [𝐼0 − (𝐼0 + 𝛾𝑅 𝑞0̄ )𝛾𝑅 𝑡] exp(−𝛾𝑅 𝑡).

(c) Underdamped, Δ < 0.
𝛾 𝑞 ̄ + 𝐼0
𝑞𝑡 = [ 𝑅 0
sin 𝜔1 𝑡 + 𝑞 ̄0 cos 𝜔1 𝑡] exp(−𝛾𝑅 𝑡),
𝜔1
𝐼𝑡 = [𝐼0 cos 𝜔1 𝑡 −

(𝜔1 2 + 𝛾𝑅 2 )𝑞 ̄0 + 𝛾𝑅 𝐼0
sin(𝜔1 𝑡)] exp(−𝛾𝑅 𝑡).
𝜔1

Here 𝛾± = (𝑅 ± Δ1/2 )/2𝐿, 𝛾𝑅 = 𝑅/2𝐿, and 𝜔1 = 𝜔0 (1 − 𝑅2 𝐶/4𝐿)1/2 , where
𝜔0 = (𝐿𝐶)−1/2 is the resonant frequency. At 𝜔 = 𝜔0 , 𝑍 = 𝑅. The quality
of the circuit is 𝑄 = 𝜔0 𝐿/𝑅. Instability results when 𝐿, 𝑅, 𝐶 are not all of the
same sign.

22

## PDF page 23

DIMENSIONLESS NUMBERS OF FLUID MECHANICS12
Name(s)

Symbol Definition

Significance

Alfvén, Kármán Al, Ka 𝑉𝐴 /𝑉

*(Magnetic force/
inertial force)1/2
Bond
Bd
(𝜌′ − 𝜌)𝐿2 𝑔/Σ Gravitational force/
surface tension
Boussinesq
B
𝑉/(2𝑔𝑅)1/2
(Inertial force/
gravitational force)1/2
Brinkman
Br
𝜇𝑉 2 /𝑘Δ𝑇
Viscous heat/conducted heat
Capillary
Cp
𝜇𝑉/Σ
Viscous force/surface tension
Carnot
Ca
(𝑇2 − 𝑇1 )/𝑇2 Theoretical Carnot cycle efficiency
Cauchy, Hooke Cy, Hk 𝜌𝑉 2 /Γ = M2 Inertial force/compressibility force
Chandrasekhar Ch
𝐵 2 𝐿2 /𝜌𝜈𝜂
Magnetic force/dissipative forces
Clausius
Cl
𝐿𝑉 3 𝜌/𝑘Δ𝑇
Kinetic energy flow rate/heat
conduction rate
2
Cowling
C
(𝑉𝐴 /𝑉)2 = Al Magnetic force/inertial force
Crispation
Cr
𝜇𝜅/Σ𝐿
Effect of diffusion/effect of surface
tension
Dean
D
𝐷3/2 𝑉/𝜈(2𝑟)1/2 Transverse flow due to
curvature/longitudinal flow
Drag coefficient 𝐶𝐷
(𝜌′ − 𝜌)𝐿𝑔/
Drag force/inertial force
𝜌′ 𝑉 2
Eckert
E
𝑉 2 /𝑐𝑝 Δ𝑇
Kinetic energy/change in thermal
energy
Ekman
Ek
(𝜈/2Ω𝐿2 )1/2 = (Viscous force/Coriolis force)1/2
(Ro/Re)1/2
Euler
Eu
Δ𝑝/𝜌𝑉 2
Pressure drop due to
friction/dynamic pressure
Froude
Fr
𝑉/(𝑔𝐿)1/2
†(Inertial force/gravitational or
𝑉/𝑁𝐿
buoyancy force)1/2
Gay–Lussac
Ga
1/𝛽Δ𝑇
Inverse of relative change in
volume during heating
Grashof
Gr
𝑔𝐿3 𝛽Δ𝑇/𝜈2
Buoyancy force/viscous force
Hall coefficient 𝐶𝐻
𝜆/𝑟𝐿
Gyrofrequency/collision frequency
Hartmann
H
𝐵𝐿/(𝜇𝜂)1/2 = (Magnetic force/dissipative
(Rm Re C)1/2 force)1/2
Knudsen
Kn
𝜆/𝐿
Hydrodynamic time/collision time
*(†) Also defined as the inverse (square) of the quantity shown.
23

## PDF page 24

Name(s)

Symbol Definition

Lewis

Le

*Thermal conduction/molecular
diffusion
Lorentz
Lo
𝑉/𝑐
Magnitude of relativistic effects
Lundquist
Lu
𝜇0 𝐿𝑉𝐴 /𝜂 =
𝐉 × 𝐁 force/resistive magnetic
Al Rm
diffusion force
Mach
M
𝑉/𝐶𝑆
Magnitude of compressibility
effects
Magnetic Mach Mm
𝑉/𝑉𝐴 = Al−1 (Inertial force/magnetic force)1/2
Magnetic
Rm
𝜇0 𝐿𝑉/𝜂
Flow velocity/magnetic diffusion
Reynolds
velocity
Newton
Nt
𝐹/𝜌𝐿2 𝑉 2
Imposed force/inertial force
Nusselt
N
𝛼𝐿/𝑘
Total heat transfer/thermal
conduction
Péclet
Pe
𝐿𝑉/𝜅
Heat convection/heat conduction
Poisseuille
Po
𝐷2 Δ𝑝/𝜇𝐿𝑉
Pressure force/viscous force
Prandtl
Pr
𝜈/𝜅
Momentum diffusion/heat
diffusion
Rayleigh
Ra
𝑔𝐻 3 𝛽Δ𝑇/𝜈𝜅 Buoyancy force/diffusion force
Reynolds
Re
𝐿𝑉/𝜈
Inertial force/viscous force
Richardson
Ri
(𝑁𝐻/Δ𝑉)2
Buoyancy effects/vertical shear
effects
Rossby
Ro
𝑉/2Ω𝐿 sin Λ Inertial force/Coriolis force
Schmidt
Sc
𝜈/𝒟
Momentum diffusion/molecular
diffusion
Stanton
St
𝛼/𝜌𝑐𝑝 𝑉
Thermal conduction loss/heat
capacity
Stefan
Sf
𝜎𝐿𝑇 3 /𝑘
Radiated heat/conducted heat
Stokes
S
𝜈/𝐿2 𝑓
Viscous damping rate/vibration
frequency
Sr
Vibration speed/flow velocity
Strouhal
𝑓𝐿/𝑉
Taylor
Ta
(2Ω𝐿2 /𝜈)2
Centrifugal force/viscous force
(Centrifugal force/viscous force)1/2
𝑅1/2 (Δ𝑅)3/2
⋅(Ω/𝜈)
Thring,
Th, Bo 𝜌𝑐𝑝 𝑉/𝜖𝜎𝑇 3
Convective heat transport/radiative
Boltzmann
heat transport
Weber
W
𝜌𝐿𝑉 2 /Σ
Inertial force/surface tension
24

𝜅/𝒟

Significance

## PDF page 25

Nomenclature:
𝐵
𝐶𝑠 , 𝑐
𝑐𝑝
𝐷 = 2𝑅
𝐹
𝑓
𝑔
𝐻, 𝐿
𝑘 = 𝜌𝑐𝑝 𝜅
𝑁 = (𝑔/𝐻)1/2
𝑅
𝑟
𝑟𝐿
𝑇
𝑉
𝑉𝐴 = 𝐵/(𝜇0 𝜌)1/2
𝛼
𝛽
Γ
Δ𝑅, Δ𝑉, Δ𝑝, Δ𝑇
𝜖
𝜂
𝜅, 𝒟
Λ
𝜆
𝜇 = 𝜌𝜈
𝜇0
𝜈
𝜌
𝜌′
Σ
𝜎
Ω

Magnetic induction
Speeds of sound, light
Specific heat at constant pressure (units m2 s−2 K−1 )
Pipe diameter
Imposed force
Vibration frequency
Gravitational acceleration
Vertical, horizontal length scales
Thermal conductivity (units kg m−1 s−2 )
Brunt–Väisälä frequency
Radius of pipe or channel
Radius of curvature of pipe or channel
Larmor radius
Temperature
Characteristic flow velocity
Alfvén speed
∂𝑇
= 𝛼Δ𝑇
Newton’s-law heat coefficient, 𝑘
∂𝑥
Volumetric expansion coefficient, 𝑑𝑉/𝑉 = 𝛽𝑑𝑇
Bulk modulus (units kg m−1 s−2 )
Imposed differences in two radii, velocities,
pressures, or temperatures
Surface emissivity
Electrical resistivity
Thermal, molecular diffusivities (units m2 s−1 )
Latitude of point on earth’s surface
Collisional mean free path
Viscosity
Permeability of free space
Kinematic viscosity (units m2 s−1 )
Mass density of fluid medium
Mass density of bubble, droplet, or moving object
Surface tension (units kg s−2 )
Stefan–Boltzmann constant
Solid-body rotational angular velocity
25

## PDF page 26

SHOCKS
At a shock front propagating in a magnetized fluid at an angle 𝜃 with respect
to the magnetic induction 𝐁, the jump conditions are 13,14
(1) 𝜌𝑈 = 𝜌 ̄𝑈̄ ≡ 𝑞;
(2) 𝜌𝑈 2 + 𝑝 + 𝐵⟂2 /2𝜇 = 𝜌 ̄𝑈̄ 2 + 𝑝 ̄ + 𝐵⟂̄ 2 /2𝜇;
(3) 𝜌𝑈𝑉 − 𝐵∥ 𝐵⟂ /𝜇 = 𝜌 ̄𝑈̄ 𝑉 ̄ − 𝐵̄∥ 𝐵̄⟂ /𝜇;
(4) 𝐵∥ = 𝐵∥̄ ;
(5) 𝑈𝐵⟂ − 𝑉𝐵∥ = 𝑈̄ 𝐵⟂̄ − 𝑉 ̄ 𝐵∥̄ ;
1 2
(6)
(𝑈 + 𝑉 2 ) + 𝑤 + (𝑈𝐵⟂2 − 𝑉𝐵∥ 𝐵⟂ )/𝜇𝜌𝑈
2
1
= (𝑈̄ 2 + 𝑉 ̄ 2 ) + 𝑤̄ + (𝑈̄ 𝐵̄⟂2 − 𝑉 ̄ 𝐵̄∥ 𝐵̄⟂ )/𝜇𝜌 ̄𝑈.̄
2
Here 𝑈 and 𝑉 are components of the fluid velocity normal and tangential to
the front in the shock frame; 𝜌 = 1/𝜐 is the mass density; 𝑝 is the pressure;
𝐵⟂ = 𝐵 sin 𝜃, 𝐵∥ = 𝐵 cos 𝜃; 𝜇 is the magnetic permeability (𝜇 = 4𝜋 in cgs
units); and the specific enthalpy is 𝑤 = 𝑒 + 𝑝𝜐, where the specific internal
energy 𝑒 satisfies 𝑑𝑒 = 𝑇𝑑𝑠 − 𝑝𝑑𝜐 in terms of the temperature 𝑇 and the
specific entropy 𝑠. Quantities in the region behind (downstream from) the
front are distinguished by a bar. If 𝐵 = 0, then15
1/2
𝑈 − 𝑈̄ = [(𝑝 ̄ − 𝑝)(𝜐 − ̄
𝜐)] ;
−1
2
(𝑝 ̄ − 𝑝)(𝜐 − 𝜐)̄
=𝑞 ;
1
(9) 𝑤̄ − 𝑤 = (𝑝 ̄ − 𝑝)(𝜐 + ̄
𝜐);
2
1
(10) 𝑒 ̄ − 𝑒 = (𝑝 ̄ + 𝑝)(𝜐 − ̄
𝜐).
2
In what follows we assume that the fluid is a perfect gas with adiabatic index
𝛾 = 1 + 2/𝑛, where 𝑛 is the number of degrees of freedom. Then 𝑝 = 𝜌𝑅𝑇/𝑚,
where 𝑅 is the universal gas constant and 𝑚 is the molar weight; the sound
2
speed is given by 𝐶𝑠 = (∂𝑝/∂𝜌)𝑠 = 𝛾𝑝𝜐; and 𝑤 = 𝛾𝑒 = 𝛾𝑝𝜐/(𝛾 − 1). For a
general oblique shock in a perfect gas the quantity 𝑋 = 𝑟−1 (𝑈/𝑉𝐴 )2 satisfies14

(7)
(8)

2

(11) (𝑋 − 𝛽/𝛼)(𝑋 − cos2 𝜃)2 = 𝑋 sin 𝜃 {[1 + (𝑟 − 1)/2𝛼] 𝑋 − cos2 𝜃} ,
1

2

where 𝑟 = ̄
𝜌/𝜌, 𝛼 = [𝛾 + 1 − (𝛾 − 1)𝑟], and 𝛽 = 𝐶𝑠 /𝑉𝐴 2 = 4𝜋𝛾𝑝/𝐵 2 .
2
The density ratio is bounded by
(12) 1 < 𝑟 < (𝛾 + 1)/(𝛾 − 1).
If the shock is normal to 𝐁 (i.e., if 𝜃 = 𝜋/2), then
2

(13) 𝑈 2 = (𝑟/𝛼) {𝐶𝑠 + 𝑉𝐴 2 [1 + (1 − 𝛾/2)(𝑟 − 1)]} ;
26

## PDF page 27

(14) 𝑈/𝑈̄ = ̄
𝐵/𝐵 = 𝑟;
(15) 𝑉 ̄ = 𝑉;
(16) 𝑝 ̄ = 𝑝 + (1 − 𝑟−1 )𝜌𝑈 2 + (1 − 𝑟2 )𝐵 2 /2𝜇.
If 𝜃 = 0, there are two possibilities: switch-on shocks, which require 𝛽 < 1
and for which
(17) 𝑈 2 = 𝑟𝑉𝐴 2 ;
(18) 𝑈̄ = 𝑉𝐴 2 /𝑈;
(19) 𝐵⟂̄ 2 = 2𝐵∥ 2 (𝑟 − 1)(𝛼 − 𝛽);
(20) 𝑉 ̄ = 𝑈̄ 𝐵⟂̄ /𝐵∥ ;
(21) 𝑝 ̄ = 𝑝 + 𝜌𝑈 2 (1 − 𝛼 + 𝛽)(1 − 𝑟−1 ),
and acoustic (hydrodynamic) shocks, for which
(22)
(23)
(24)
(25)

2

𝑈 2 = (𝑟/𝛼)𝐶𝑠 ;
𝑈̄ = 𝑈/𝑟;
𝑉 ̄ = 𝐵⟂̄ = 0;
𝑝 ̄ = 𝑝 + 𝜌𝑈 2 (1 − 𝑟−1 ).

For acoustic shocks the specific volume and pressure are related by
(26) ̄
𝜐/𝜐 = [(𝛾 + 1)𝑝 + (𝛾 − 1)𝑝]̄ / [(𝛾 − 1)𝑝 + (𝛾 + 1)𝑝]̄ .
In terms of the upstream Mach number 𝑀 = 𝑈/𝐶𝑠 ,
̄
𝜌/𝜌 = 𝜐/𝜐 ̄ = 𝑈/𝑈̄ = (𝛾 + 1)𝑀 2 /[(𝛾 − 1)𝑀 2 + 2];
𝑝/𝑝 = (2𝛾𝑀 2 − 𝛾 + 1)/(𝛾 + 1);
̄
̄ = [(𝛾 − 1)𝑀 2 + 2](2𝛾𝑀 2 − 𝛾 + 1)/(𝛾 + 1)2 𝑀 2 ;
𝑇/𝑇
𝑀̄ 2 = [(𝛾 − 1)𝑀 2 + 2]/[2𝛾𝑀 2 − 𝛾 + 1].

(27)
(28)
(29)
(30)

The entropy change across the shock is
(31) Δ𝑠 ≡ 𝑠 ̄ − 𝑠 = 𝑐𝜐 ln[( ̄
𝑝/𝑝)(𝜌/𝜌)̄ 𝛾 ],
where 𝑐𝜐 = 𝑅/(𝛾 − 1)𝑚 is the specific heat at constant volume; here 𝑅 is the
gas constant. In the weak-shock limit (𝑀 → 1),
2𝛾(𝛾 − 1) 2
16𝛾𝑅
(32) Δ𝑠 → 𝑐𝜐
(𝑀 − 1)3 ≈
(𝑀 − 1)3 .
3(𝛾 + 1)
3(𝛾 + 1)𝑚
The radius at time 𝑡 of a strong spherical blast wave resulting from the explosive release of energy 𝐸 in a medium with uniform density 𝜌 is
(33) 𝑅𝑆 = 𝐶0 (𝐸𝑡2 /𝜌)1/5 ,
where 𝐶0 is a constant depending on 𝛾. For 𝛾 = 7/5, 𝐶0 = 1.033.
27

## PDF page 28

FUNDAMENTAL PLASMA PARAMETERS
All quantities are in Gaussian cgs units except temperature (𝑇, 𝑇𝑒 , 𝑇𝑖 ) expressed in eV and ion mass (𝑚𝑖 ) expressed in units of the proton mass, 𝜇 =
𝑚𝑖 /𝑚𝑝 ; 𝑍 is charge state; 𝑘 is Boltzmann’s constant; 𝐾 is wavenumber; 𝛾 is
the adiabatic index; ln Λ is the Coulomb logarithm.
Frequencies
electron gyrofrequency
𝑓𝑐𝑒 = 𝜔𝑐𝑒 /2𝜋 = 2.80 × 106 𝐵 Hz
𝜔𝑐𝑒 = 𝑒𝐵/𝑚𝑒 𝑐 = 1.76 × 107 𝐵 rad/sec
ion gyrofrequency
𝑓𝑐𝑖 = 𝜔𝑐𝑖 /2𝜋 = 1.52 × 103 𝑍𝜇−1 𝐵 Hz
𝜔𝑐𝑖 = 𝑍𝑒𝐵/𝑚𝑖 𝑐 = 9.58 × 103 𝑍𝜇−1 𝐵 rad/sec
electron plasma frequency 𝑓𝑝𝑒 = 𝜔𝑝𝑒 /2𝜋 = 8.98 × 103 𝑛𝑒 1/2 Hz
𝜔𝑝𝑒 = (4𝜋𝑛𝑒 𝑒2 /𝑚𝑒 )1/2
= 5.64 × 104 𝑛𝑒 1/2 rad/sec
ion plasma frequency
𝑓𝑝𝑖 = 𝜔𝑝𝑖 /2𝜋
= 2.10 × 102 𝑍𝜇−1/2 𝑛𝑖 1/2 Hz
𝜔𝑝𝑖 = (4𝜋𝑛𝑖 𝑍 2 𝑒2 /𝑚𝑖 )1/2
= 1.32 × 103 𝑍𝜇−1/2 𝑛𝑖 1/2 rad/sec
electron trapping rate
𝜈𝑇𝑒 = (𝑒𝐾𝐸/𝑚𝑒 )1/2
= 7.26 × 108 𝐾 1/2 𝐸 1/2 sec−1
ion trapping rate
𝜈𝑇𝑖 = (𝑍𝑒𝐾𝐸/𝑚𝑖 )1/2
= 1.69 × 107 𝑍 1/2 𝐾 1/2 𝐸 1/2 𝜇−1/2 sec−1
electron collision rate
𝜈𝑒 = 2.91 × 10−6 𝑛𝑒 ln Λ𝑇𝑒 −3/2 sec−1
ion collision rate
𝜈𝑖 = 4.80 × 10−8 𝑍 4 𝜇−1/2 𝑛𝑖 ln Λ𝑇𝑖 −3/2 sec−1
Lengths
electron deBroglie length
classical distance of
minimum approach
electron gyroradius
ion gyroradius
electron inertial length
ion inertial length
Debye length
magnetic Debye length
28

ƛ = ℏ/(𝑚𝑒 𝑘𝑇𝑒 )1/2 = 2.76 × 10−8 𝑇𝑒 −1/2 cm
𝑒2 /𝑘𝑇 = 1.44 × 10−7 𝑇 −1 cm
𝑟𝑒 = 𝑣𝑇𝑒 /𝜔𝑐𝑒 = 2.38𝑇𝑒 1/2 𝐵−1 cm
𝑟𝑖 = 𝑣𝑇𝑖 /𝜔𝑐𝑖
= 1.02 × 102 𝜇1/2 𝑍 −1 𝑇𝑖 1/2 𝐵 −1 cm
𝑐/𝜔𝑝𝑒 = 5.31 × 105 𝑛𝑒 −1/2 cm
𝑐/𝜔𝑝𝑖 = 2.28 × 107 𝑍 −1 (𝜇/𝑛𝑖 )1/2 cm
𝜆𝐷 = (𝑘𝑇/4𝜋𝑛𝑒2 )1/2 = 7.43 × 102 𝑇 1/2 𝑛−1/2 cm
𝜆𝑀 = 𝐵/4𝜋𝑛𝑒 𝑒 = 1.66 × 108 𝐵𝑛−1
𝑒 cm

## PDF page 29

Velocities
electron thermal velocity
ion thermal velocity
ion sound velocity
Alfvén velocity

𝑣𝑇𝑒 = (𝑘𝑇𝑒 /𝑚𝑒 )1/2
= 4.19 × 107 𝑇𝑒 1/2 cm/sec
𝑣𝑇𝑖 = (𝑘𝑇𝑖 /𝑚𝑖 )1/2
= 9.79 × 105 𝜇−1/2 𝑇𝑖 1/2 cm/sec
𝐶𝑠 = (𝛾𝑍𝑘𝑇𝑒 /𝑚𝑖 )1/2
= 9.79 × 105 (𝛾𝑍𝑇𝑒 /𝜇)1/2 cm/sec
𝑣𝐴 = 𝐵/(4𝜋𝑛𝑖 𝑚𝑖 )1/2
= 2.18 × 1011 𝜇−1/2 𝑛𝑖 −1/2 𝐵 cm/sec

Dimensionless
(electron/proton mass ratio)1/2 (𝑚𝑒 /𝑚𝑝 )1/2 = 2.33 × 10−2 = 1/42.9
3

number of particles in
(4𝜋/3)𝑛𝜆𝐷 = 1.72 × 109 𝑇 3/2 𝑛−1/2
Debye sphere
Alfvén velocity/speed of light 𝑣𝐴 /𝑐 = 7.28𝜇−1/2 𝑛𝑖 −1/2 𝐵
electron plasma/gyrofrequency 𝜔𝑝𝑒 /𝜔𝑐𝑒 = 3.21 × 10−3 𝑛𝑒 1/2 𝐵−1
ratio
ion plasma/gyrofrequency ratio 𝜔𝑝𝑖 /𝜔𝑐𝑖 = 0.137𝜇1/2 𝑛𝑖 1/2 𝐵−1
thermal/magnetic energy ratio 𝛽 = 8𝜋𝑛𝑘𝑇/𝐵 2 = 4.03 × 10−11 𝑛𝑇𝐵 −2
magnetic/ion rest energy ratio 𝐵2 /8𝜋𝑛𝑖 𝑚𝑖 𝑐2 = 26.5𝜇−1 𝑛𝑖 −1 𝐵2
Miscellaneous
Bohm diffusion coefficient
transverse Spitzer resistivity

𝐷𝐵 = (𝑐𝑘𝑇/16𝑒𝐵)
= 6.25 × 106 𝑇𝐵 −1 cm2 /sec
𝜂⟂ = 1.15 × 10−14 𝑍 ln Λ𝑇 −3/2 sec
= 1.03 × 10−2 𝑍 ln Λ𝑇 −3/2 Ω cm

The anomalous collision rate due to low-frequency ion-sound turbulence is
˜/𝑘𝑇 = 5.64 × 104 𝑛𝑒 1/2 𝑊
˜/𝑘𝑇 sec−1 ,
𝜈* ≈ 𝜔𝑝𝑒 𝑊
˜ is the total energy of waves with 𝜔/𝐾 < 𝑣𝑇𝑖 .
where 𝑊
Magnetic pressure is given by
2

𝑃mag = 𝐵 2 /8𝜋 = 3.98 × 106 (𝐵/𝐵0 )2 dynes/cm = 3.93(𝐵/𝐵0 )2 atm,
where 𝐵0 = 10 kG = 1 T.
Detonation energy of 1 kiloton of high explosive is
𝑊kT = 1012 cal = 4.2 × 1019 erg = 4.2 × 1012 J.
29

## PDF page 30

PLASMA DISPERSION FUNCTION
16

Definition

(first form valid only for Im 𝜁 > 0):
+∞

𝑍(𝜁) = 𝜋−1/2 ∫
−∞

𝑖𝜁
𝑑𝑡 exp (−𝑡2 )
= 2𝑖 exp (−𝜁2 ) ∫ 𝑑𝑡 exp (−𝑡2 ) .
𝑡−𝜁
−∞

Physically, 𝜁 = 𝑥 + 𝑖𝑦 is the ratio of wave phase velocity to thermal velocity.
Differential equation:
𝑑𝑍
= −2 (1 + 𝜁𝑍) , 𝑍(0) = 𝑖𝜋1/2 ;
𝑑𝜁
Real argument (𝑦 = 0):

𝑑2 𝑍
𝑑𝑍
+ 2𝜁
+ 2𝑍 = 0.
𝑑𝜁2
𝑑𝜁

𝑥

𝑍(𝑥) = exp (−𝑥2 ) (𝑖𝜋1/2 − 2 ∫ 𝑑𝑡 exp (𝑡2 )) .
0

Imaginary argument (𝑥 = 0):
𝑍(𝑖𝑦) = 𝑖𝜋1/2 exp (𝑦2 ) [1 − erf(𝑦)] .
Power series (small argument):
𝑍(𝜁) = 𝑖𝜋1/2 exp (−𝜁2 ) − 2𝜁 (1 − 2𝜁2 /3 + 4𝜁4 /15 − 8𝜁6 /105 + ⋯) .
Asymptotic series, |𝜁| ≫ 1 (Ref. 17):
𝑍(𝜁) = 𝑖𝜋1/2 𝜎 exp (−𝜁2 ) − 𝜁−1 (1 + 1/2𝜁2 + 3/4𝜁4 + 15/8𝜁6 + ⋯) ,
where
𝜎=

⎧ 0,
1,
⎨
⎩ 2,

𝑦 > |𝑥|−1
|𝑦| < |𝑥|−1
𝑦 < −|𝑥|−1

Symmetry properties (the asterisk denotes complex conjugation):
𝑍(𝜁*) = − [𝑍(−𝜁)]*;
𝑍(𝜁*) = [𝑍(𝜁)] * + 2𝑖𝜋1/2 exp[−(𝜁*)2 ],
18

(𝑦 > 0).

Two-pole approximations (good for 𝜁 in upper half plane except when 𝑦 <
𝜋1/2 𝑥2 exp(−𝑥2 ), 𝑥 ≫ 1):
0.50 + 0.81𝑖 0.50 − 0.81𝑖
−
, 𝑎 = 0.51 − 0.81𝑖;
𝑍(𝜁) ≈
𝑎−𝜁
𝑎* + 𝜁
0.50 + 0.96𝑖 0.50 − 0.96𝑖
+
, 𝑏 = 0.48 − 0.91𝑖.
𝑍 ′ (𝜁) ≈
(𝑏 − 𝜁)2
(𝑏* + 𝜁)2
30

## PDF page 31

COLLISIONS AND TRANSPORT
Temperatures are in eV; the corresponding value of Boltzmann’s constant is 𝑘 = 1.60 ×
10−12 erg/eV; masses 𝜇, 𝜇′ are in units of the proton mass; 𝑒𝛼 = 𝑍𝛼 𝑒 is the charge of species
𝛼. All other units are cgs except where noted.

Relaxation Rates
Rates are associated with four relaxation processes arising from the interaction of test particles (labeled 𝛼) streaming with velocity v𝛼 through a background of field particles (labeled 𝛽):
𝑑v𝛼
𝛼\𝛽
slowing down
= −𝜈𝑠 v𝛼
𝑑𝑡
𝑑
𝛼\𝛽
transverse diffusion
(v − v̄ 𝛼 )2⟂ = 𝜈⟂ 𝑣𝛼 2
𝑑𝑡 𝛼
𝑑
𝛼\𝛽
parallel diffusion
(v − v̄ 𝛼 )2∥ = 𝜈∥ 𝑣𝛼 2
𝑑𝑡 𝛼
𝑑 2
𝛼\𝛽
𝑣 = −𝜈𝜖 𝑣𝛼 2 ,
energy loss
𝑑𝑡 𝛼
where 𝑣𝛼 = |𝐯𝛼 | and the averages are performed over an ensemble of test
particles and a Maxwellian field particle distribution. The exact formulas
may be written19
𝛼\𝛽

= (1 + 𝑚𝛼 /𝑚𝛽 )𝜓(𝑥𝛼\𝛽 )𝜈0 ;

𝛼\𝛽

= 2 [(1 − 1/2𝑥𝛼\𝛽 )𝜓(𝑥𝛼\𝛽 ) + 𝜓′ (𝑥𝛼\𝛽 )] 𝜈0 ;

𝛼\𝛽

= [𝜓(𝑥𝛼\𝛽 )/𝑥𝛼\𝛽 ] 𝜈0 ;

𝛼\𝛽

= 2 [(𝑚𝛼 /𝑚𝛽 )𝜓(𝑥𝛼\𝛽 ) − 𝜓′ (𝑥𝛼\𝛽 )] 𝜈0 ,

𝜈𝑠

𝜈⟂
𝜈∥
𝜈𝜖

𝛼\𝛽

𝛼\𝛽

𝛼\𝛽

𝛼\𝛽

where
𝛼\𝛽
𝜈0 = 4𝜋𝑒𝛼 2 𝑒𝛽 2 𝜆𝛼𝛽 𝑛𝛽 /𝑚𝛼 2 𝑣𝛼 3 ;
𝜓(𝑥) =

2
√𝜋

𝑥

∫ 𝑑𝑡 𝑡1/2 𝑒−𝑡 ;
0

𝜓′ (𝑥) =

𝑥𝛼\𝛽 = 𝑚𝛽 𝑣𝛼 2 /2𝑘𝑇𝛽 ;
𝑑𝜓
,
𝑑𝑥

and 𝜆𝛼𝛽 = ln Λ𝛼𝛽 is the Coulomb logarithm (see below). Limiting forms of
𝜈𝑠 , 𝜈⟂ and 𝜈∥ are given in the following table. All the expressions shown have
units cm3 sec−1 . Test particle energy 𝜖 and field particle temperature 𝑇 are
both in eV; 𝜇 = 𝑚𝑖 /𝑚𝑝 where 𝑚𝑝 is the proton mass; 𝑍 is ion charge state; in
electron–electron and ion–ion encounters, field particle quantities are distinguished by a prime. The two expressions given below for each rate hold for
31

## PDF page 32

very slow (𝑥𝛼\𝛽 ≪ 1) and very fast (𝑥𝛼\𝛽 ≫ 1) test particles, respectively.
Slow

Fast

Electron–electron
𝑒|𝑒

𝜈𝑠 /𝑛𝑒 𝜆𝑒𝑒 ≈ 5.8 × 10−6 𝑇 −3/2
𝑒|𝑒
𝜈⟂ /𝑛𝑒 𝜆𝑒𝑒 ≈ 5.8 × 10−6 𝑇 −1/2 𝜖−1
𝑒|𝑒
𝜈∥ /𝑛𝑒 𝜆𝑒𝑒 ≈ 2.9 × 10−6 𝑇 −1/2 𝜖−1

⟶ 7.7 × 10−6 𝜖−3/2
⟶ 7.7 × 10−6 𝜖−3/2
⟶ 3.9 × 10−6 𝑇𝜖−5/2

Electron–ion
𝑒|𝑖

⟶ 3.9 × 10−6 𝜖−3/2
𝜈𝑠 /𝑛𝑖 𝑍 2 𝜆𝑒𝑖 ≈ 0.23𝜇3/2 𝑇 −3/2
𝑒|𝑖
2
−4 1/2 −1/2 −1
𝜈⟂ /𝑛𝑖 𝑍 𝜆𝑒𝑖 ≈ 2.5 × 10 𝜇 𝑇
𝜖 ⟶ 7.7 × 10−6 𝜖−3/2
𝑒|𝑖
𝜈∥ /𝑛𝑖 𝑍 2 𝜆𝑒𝑖 ≈ 1.2 × 10−4 𝜇1/2 𝑇 −1/2 𝜖−1 ⟶ 2.1 × 10−9 𝜇−1 𝑇𝜖−5/2
Ion–electron
𝑖|𝑒

𝜈𝑠 /𝑛𝑒 𝑍 2 𝜆𝑖𝑒 ≈ 1.6 × 10−9 𝜇−1 𝑇 −3/2
⟶ 1.7 × 10−4 𝜇1/2 𝜖−3/2
𝑖|𝑒
2
−9 −1 −1/2 −1
𝜈⟂ /𝑛𝑒 𝑍 𝜆𝑖𝑒 ≈ 3.2 × 10 𝜇 𝑇
𝜖 ⟶ 1.8 × 10−7 𝜇−1/2 𝜖−3/2
𝑖|𝑒
2
−9 −1 −1/2 −1
𝜈∥ /𝑛𝑒 𝑍 𝜆𝑖𝑒 ≈ 1.6 × 10 𝜇 𝑇
𝜖 ⟶ 1.7 × 10−4 𝜇1/2 𝑇𝜖−5/2
Ion–ion

𝑖|𝑖′

𝜇′
𝜇′1/2
𝜈𝑠
≈ 6.8 × 10−8
(1 + ) 𝑇 −3/2
2
′2
𝜇
𝜇
𝑛𝑖′ 𝑍 𝑍 𝜆𝑖𝑖′
1
1 𝜇1/2
⟶ 9.0 × 10−8 ( + ′ ) 3/2
𝜇 𝜇 𝜖
𝑖|𝑖′
𝜈⟂
≈ 1.4 × 10−7 𝜇′1/2 𝜇−1 𝑇 −1/2 𝜖−1
𝑛𝑖′ 𝑍 2 𝑍 ′2 𝜆𝑖𝑖′
⟶ 1.8 × 10−7 𝜇−1/2 𝜖−3/2
𝑖|𝑖′

𝜈∥
≈ 6.8 × 10−8 𝜇′1/2 𝜇−1 𝑇 −1/2 𝜖−1
𝑛𝑖′ 𝑍 2 𝑍 ′2 𝜆𝑖𝑖′
⟶ 9.0 × 10−8 𝜇1/2 𝜇′−1 𝑇𝜖−5/2
In the same limits, the energy transfer rate follows from the identity
𝜈𝜖 = 2𝜈𝑠 − 𝜈⟂ − 𝜈∥ ,
except for the case of fast electrons or fast ions scattered by ions, where the
leading terms cancel. Then the appropriate forms are
𝑒|𝑖

𝜈𝜖 ⟶ 4.2 × 10−9 𝑛𝑖 𝑍 2 𝜆𝑒𝑖
[𝜖−3/2 𝜇−1 − 8.9 × 104 (𝜇/𝑇)1/2 𝜖−1 exp(−1836𝜇𝜖/𝑇)] sec−1
32

## PDF page 33

and
𝑖|𝑖′

𝜈𝜖

⟶ 1.8 × 10−7 𝑛𝑖′ 𝑍 2 𝑍 ′2 𝜆𝑖𝑖′ {𝜖−3/2 𝜇1/2 /𝜇

′

−1.1[(𝜇 + 𝜇′ )/𝜇𝜇′ ](𝜇′ /𝑇 ′ )1/2 𝜖−1 exp(−𝜇′ 𝜖/𝜇𝑇 ′ )} sec−1 .
𝛼\𝛽

In general, the energy transfer rate 𝜈𝜖 is positive for 𝜖 > 𝜖𝛼∗ and negative for
𝜖 < 𝜖𝛼∗ , where 𝑥∗ = (𝑚𝛽 /𝑚𝛼 )𝜖𝛼∗ /𝑇𝛽 is the solution of 𝜓′ (𝑥∗ ) = (𝑚𝛼 |𝑚𝛽 )𝜓(𝑥∗ ).
The ratio 𝜖𝛼∗ /𝑇𝛽 is given for a number of specific 𝛼, 𝛽 in the following table:
𝑖|𝑒

𝑒|𝑒, 𝑖|𝑖

𝑒|𝑝

𝑒|D

𝑒|T, 𝑒|He3

𝑒|He4

𝜖𝛼∗ /𝑇𝛽 : 1.5

0.98

4.8 × 10−3

2.6 × 10−3

1.8 × 10−3

1.4 × 10−3

𝛼\𝛽:

When both species are near Maxwellian, with 𝑇𝑖 ≲ 𝑇𝑒 , there are just two
characteristic collision rates. For 𝑍 = 1,
𝜈𝑒 = 2.9 × 10−6 𝑛𝜆𝑇𝑒 −3/2 sec−1 ;
𝜈𝑖 = 4.8 × 10−8 𝑛𝜆𝑇𝑖 −3/2 𝜇−1/2 sec−1 .
Temperature Isotropization
Isotropization is described by
𝑑𝑇⟂
1 𝑑𝑇∥
=−
= −𝜈𝑇𝛼 (𝑇⟂ − 𝑇∥ ),
𝑑𝑡
2 𝑑𝑡
where, if 𝐴 ≡ 𝑇⟂ /𝑇∥ − 1 > 0,
𝜈𝑇𝛼 =

2√𝜋𝑒𝛼2 𝑒𝛽2 𝑛𝛼 𝜆𝛼𝛽
3/2
𝑚1/2
𝛼 (𝑘𝑇∥ )

𝐴−2 [−3 + (𝐴 + 3)

tan−1 (𝐴1/2 )
].
𝐴1/2

−1

If 𝐴 < 0, tan−1 (𝐴1/2 )/𝐴1/2 is replaced by tanh (−𝐴)1/2 /(−𝐴)1/2 .
For 𝑇⟂ ≈ 𝑇∥ ≡ 𝑇,
𝜈𝑇𝑒 = 8.2 × 10−7 𝑛𝜆𝑇 −3/2 sec−1 ;
𝜈𝑇𝑖 = 1.9 × 10−8 𝑛𝜆𝑍 2 𝜇−1/2 𝑇 −3/2 sec−1 .
Thermal Equilibration
If the components of a plasma have different temperatures, but no relative
drift, equilibration is described by
𝑑𝑇𝛼
𝛼\𝛽
= ∑ 𝜈 ̄𝜖 (𝑇𝛽 − 𝑇𝛼 ),
𝑑𝑡
𝛽
33

## PDF page 34

where
𝛼\𝛽

𝜈 ̄𝜖

= 1.8 × 10−19

(𝑚𝛼 𝑚𝛽 )1/2 𝑍𝛼2 𝑍𝛽2 𝑛𝛽 𝜆𝛼𝛽
(𝑚𝛼 𝑇𝛽 + 𝑚𝛽 𝑇𝛼 )3/2

sec−1 .

For electrons and ions with 𝑇𝑒 ≈ 𝑇𝑖 ≡ 𝑇, this implies
𝑒|𝑖

𝑖|𝑒

𝜈 ̄𝜖 /𝑛𝑖 = 𝜈 ̄𝜖 /𝑛𝑒 = 3.2 × 10−9 𝑍 2 𝜆/𝜇𝑇 3/2 cm3 sec−1 .
Coulomb Logarithm
For test particles of mass 𝑚𝛼 and charge 𝑒𝛼 = 𝑍𝛼 𝑒 scattering off field particles of mass 𝑚𝛽 and charge 𝑒𝛽 = 𝑍𝛽 𝑒, the Coulomb logarithm is defined
as 𝜆 = ln Λ ≡ ln(𝑟max /𝑟min ). Here 𝑟min is the larger of 𝑒𝛼 𝑒𝛽 /𝑚𝛼𝛽 𝑢̄2 and
ℏ/2𝑚𝛼𝛽 𝑢,̄ averaged over both particle velocity distributions, where 𝑚𝛼𝛽 =
𝑚𝛼 𝑚𝛽 /(𝑚𝛼 + 𝑚𝛽 ) and 𝐮 = 𝐯𝛼 − 𝐯𝛽 ; 𝑟max = (4𝜋 ∑ 𝑛𝛾 𝑒𝛾2 /𝑘𝑇𝛾 )−1/2 , where
2
the summation extends over all species 𝛾 for which 𝑢̄2 < 𝑣𝑇𝛾
= 𝑘𝑇𝛾 /𝑚𝛾 . If
−1
−1
< 𝑟max ,
this inequality cannot be satisfied, or if either ̄
𝑢𝜔𝑐𝛼
< 𝑟max or ̄
𝑢𝜔𝑐𝛽
the theory breaks down. Typically 𝜆 ≈ 10–20. Corrections to the transport coefficients are 𝑂(𝜆−1 ); hence the theory is good only to ∼ 10% and fails when
𝜆 ∼ 1.
The following cases are of particular interest:
(a) Thermal electron–electron collisions
−5/4
𝜆𝑒𝑒 = 23.5 − ln(𝑛1/2
) − [10−5 + (ln 𝑇𝑒 − 2)2 /16]1/2 .
𝑒 𝑇𝑒

(b) Electron–ion collisions
1/2
−3/2
𝑇𝑖 𝑚𝑒 /𝑚𝑖 < 𝑇𝑒 < 10𝑍 2 eV;
⎧ 23 − ln (𝑛𝑒 𝑍𝑇𝑒 ) ,
1/2 −1
𝜆𝑒𝑖 = 𝜆𝑖𝑒 = 24 − ln (𝑛𝑒 𝑇𝑒 ) ,
𝑇𝑖 𝑚𝑒 /𝑚𝑖 < 10𝑍 2 eV < 𝑇𝑒 ;
⎨
1/2 −3/2 2
𝑍 𝜇) , 𝑇𝑒 < 𝑇𝑖 𝑚𝑒 /𝑚𝑖 .
⎩ 16 − ln (𝑛𝑖 𝑇𝑖

(c) Mixed ion–ion collisions
2

𝜆𝑖𝑖′ = 𝜆𝑖′ 𝑖 = 23 − ln [

𝑍𝑍 ′ (𝜇 + 𝜇′ ) 𝑛𝑖 𝑍 2
𝑛 ′ 𝑍′
+ 𝑖
(
)
′
𝜇𝑇𝑖′ + 𝜇 𝑇𝑖
𝑇𝑖
𝑇𝑖′

1/2

].

(d) Counterstreaming ions (relative velocity 𝑣𝐷 = 𝛽𝐷 𝑐) in the presence of
2
warm electrons, 𝑘𝑇𝑖 /𝑚𝑖 , 𝑘𝑇𝑖′ /𝑚𝑖′ < 𝑣𝐷
< 𝑘𝑇𝑒 /𝑚𝑒
𝜆𝑖𝑖′ = 𝜆𝑖′ 𝑖 = 43 − ln [

34

𝑍𝑍 ′ (𝜇 + 𝜇′ ) 𝑛𝑒
( )
2
𝑇𝑒
𝜇𝜇′ 𝛽𝐷

1/2

].

## PDF page 35

Fokker-Planck Equation
𝐷𝑓𝛼
∂𝑓𝛼
∂𝑓𝛼
≡
+ 𝐯 ⋅ ∇𝑓𝛼 + 𝐅 ⋅ ∇𝐯 𝑓𝛼 = (
) ,
𝐷𝑡
∂𝑡
∂𝑡 coll
where 𝐅 is an external force field. The general form of the collision integral is
(∂𝑓𝛼 /∂𝑡)coll = − ∑𝛽 ∇𝐯 ⋅ 𝐉𝛼\𝛽 , with
𝐉𝛼\𝛽 = 2𝜋𝜆𝛼𝛽

𝑒𝛼2 𝑒𝛽2
𝑚𝛼

∫ 𝑑3𝑣′ (𝑢2 𝙄 − 𝐮𝐮)𝑢−3
⋅{

1 𝛼
1 𝛽 ′
𝑓 (𝐯)∇𝐯′ 𝑓𝛽 (𝐯′ ) −
𝑓 (𝐯 )∇𝐯 𝑓𝛼 (𝐯)} ,
𝑚𝛽
𝑚𝛼

(Landau form) where 𝐮 = 𝐯′ − 𝐯 and 𝙄 is the unit dyad, or alternatively,
𝑒𝛼2 𝑒𝛽2

1
{𝑓𝛼 (𝐯)∇𝐯 𝐻(𝐯) − ∇𝐯 ⋅ [𝑓𝛼 (𝐯)∇𝐯 ∇𝐯 𝐺(𝐯)]} ,
2
𝑚2𝛼
where the Rosenbluth potentials are
𝐉𝛼\𝛽 = 4𝜋𝜆𝛼𝛽

𝐺(𝐯) = ∫ 𝑓𝛽 (𝐯′ )𝑢𝑑3𝑣′ ,
𝐻(𝐯) = (1 +

𝑚𝛼
) ∫ 𝑓𝛽 (𝐯′ )𝑢−1 𝑑3𝑣′ .
𝑚𝛽

If species 𝛼 is a weak beam (number and energy density small compared
with background) streaming through a Maxwellian plasma, then
𝐉𝛼\𝛽 = −

𝑚𝛼
1 𝛼\𝛽
𝛼\𝛽
𝜈𝑠 𝐯𝑓𝛼 − 𝜈∥ 𝐯𝐯 ⋅ ∇𝐯 𝑓𝛼
𝑚𝛼 + 𝑚𝛽
2
−

1 𝛼\𝛽 2
𝜈 (𝑣 𝙄 − 𝐯𝐯) ⋅ ∇𝐯 𝑓𝛼 .
4 ⟂

B-G-K Collision Operator
For distribution functions with no large gradients in velocity space, the FokkerPlanck collision terms can be approximated according to
𝐷𝑓𝑒
= 𝜈𝑒𝑒 (𝐹𝑒 − 𝑓𝑒 ) + 𝜈𝑒𝑖 (𝐹𝑒̄ − 𝑓𝑒 );
𝐷𝑡
𝐷𝑓𝑖
= 𝜈𝑖𝑒 (𝐹𝑖̄ − 𝑓𝑖 ) + 𝜈𝑖𝑖 (𝐹𝑖 − 𝑓𝑖 ).
𝐷𝑡
𝛼\𝛽

The respective slowing-down rates 𝜈𝑠 given in the Relaxation Rate section
above can be used for 𝜈𝛼𝛽 , assuming slow ions and fast electrons, with 𝜖 re-

35

## PDF page 36

placed by 𝑇𝛼 . (For 𝜈𝑒𝑒 and 𝜈𝑖𝑖 , one can equally well use 𝜈⟂ , and the result is
insensitive to whether the slow- or fast-test-particle limit is employed.) The
Maxwellians 𝐹𝛼 and 𝐹𝛼̄ are given by
𝐹𝛼 = 𝑛𝛼 (

𝑚𝛼
)
2𝜋𝑘𝑇𝛼

3/2

exp {− [

𝑚𝛼 (𝐯 − 𝐯𝛼 )2
]} ;
2𝑘𝑇𝛼

3/2

𝑚𝛼
𝑚 (𝐯 − 𝐯̄ 𝛼 )2
]} ,
) exp {− [ 𝛼
2𝜋𝑘𝑇̄𝛼
2𝑘𝑇̄𝛼
where 𝑛𝛼 , 𝐯𝛼 and 𝑇𝛼 are the number density, mean drift velocity, and effective temperature obtained by taking moments of 𝑓𝛼 . Some latitude in the
definition of 𝑇𝛼̄ and 𝐯̄ 𝛼 is possible;20 one choice is 𝑇𝑒̄ = 𝑇𝑖 , 𝑇𝑖̄ = 𝑇𝑒 , 𝐯̄ 𝑒 = 𝐯𝑖 ,
𝐯̄ 𝑖 = 𝐯𝑒 .
𝐹𝛼̄ = 𝑛𝛼 (

Transport Coefficients
Transport equations for a multispecies plasma:
𝑑𝛼 𝑛𝛼
+ 𝑛𝛼 ∇ ⋅ 𝐯𝛼 = 0;
𝑑𝑡
𝑑𝛼 𝐯𝛼
1
𝑚𝛼 𝑛𝛼
= −∇𝑝𝛼 − ∇ ⋅ 𝝥𝛼 + 𝑍𝛼 𝑒𝑛𝛼 [𝐄 + 𝐯𝛼 × 𝐁] + 𝐑𝛼 ;
𝑑𝑡
𝑐
3 𝑑𝛼 𝑘𝑇𝛼
𝑛
+ 𝑝𝛼 ∇ ⋅ 𝐯𝛼 = −∇ ⋅ 𝐪𝛼 − 𝝥𝛼 ∶ ∇𝐯𝛼 + 𝑄𝛼 .
2 𝛼 𝑑𝑡
𝛼
Here 𝑑 /𝑑𝑡 ≡ ∂/∂𝑡 + 𝐯𝛼 ⋅ ∇; 𝑝𝛼 = 𝑛𝛼 𝑘𝑇𝛼 , where 𝑘 is Boltzmann’s constant;
𝐑𝛼 = ∑𝛽 𝐑𝛼𝛽 and 𝑄𝛼 = ∑𝛽 𝑄𝛼𝛽 , where 𝐑𝛼𝛽 and 𝑄𝛼𝛽 are respectively the
momentum and energy gained by the 𝛼th species through collisions with the
𝛽 th ; 𝝥𝛼 is the stress tensor; and 𝐪𝛼 is the heat flow.
The transport coefficients in a simple two-component plasma (electrons and
singly charged ions) are tabulated below. Here ∥ and ⟂ refer to the directions
relative to the magnetic field 𝐁 = 𝐛𝐵; 𝐮 = 𝐯𝑒 − 𝐯𝑖 is the relative streaming
velocity; 𝑛𝑒 = 𝑛𝑖 ≡ 𝑛; 𝐣 = −𝑛𝑒𝐮 is the current; and the basic collisional times
are taken to be
3√𝑚𝑒 (𝑘𝑇𝑒 )3/2
𝑇𝑒3/2
𝜏𝑒 =
sec,
= 3.44 × 105
𝑛𝜆
4√2𝜋 𝑛𝜆𝑒4
where 𝜆 is the Coulomb logarithm, and
𝜏𝑖 =
36

3√𝑚𝑖 (𝑘𝑇𝑖 )3/2
4√𝜋𝑛 𝜆𝑒4

= 2.09 × 107

𝑇𝑖3/2 1/2
𝜇 sec.
𝑛𝜆

## PDF page 37

In the limit of large fields (𝜔𝑐𝛼 𝜏𝛼 ≫ 1, 𝛼 = 𝑖, 𝑒) the transport processes may
be summarized as follows:21𝑎,𝑏
momentum transfer R𝑒𝑖 = −R𝑖𝑒 ≡ R = R𝐮 + R𝑇 ;
𝑛𝑒
frictional force
R𝐮 =
(0.51𝐣∥ + 𝐣⟂ ); 𝜎0 = 𝑛𝑒2 𝜏𝑒 /𝑚𝑒
𝜎0
3𝑛
thermal force
R𝑇 = −0.71𝑛∇∥ (𝑘𝑇𝑒 ) −
𝐛 × ∇⟂ (𝑘𝑇𝑒 )
2𝜔𝑐𝑒 𝜏𝑒
3𝑚𝑒 𝑛𝑘
ion heating
𝑄𝑖 =
(𝑇 − 𝑇𝑖 );
𝑚𝑖 𝜏𝑒 𝑒
electron heating
𝑄𝑒 = −𝑄𝑖 − R ⋅ 𝐮;
ion heat flux
𝐪𝑖 = −𝜅∥𝑖 ∇∥ (𝑘𝑇𝑖 ) − 𝜅⟂𝑖 ∇⟂ (𝑘𝑇𝑖 ) + 𝜅∧𝑖 𝐛 × ∇⟂ (𝑘𝑇𝑖 )
𝑛𝑘𝑇𝑖 𝜏𝑖
2𝑛𝑘𝑇𝑖
5𝑛𝑘𝑇𝑖
ion thermal
𝜅∥𝑖 = 3.9
; 𝜅⟂𝑖 =
; 𝜅∧𝑖 =
2
𝑚𝑖
2𝑚𝑖 𝜔𝑐𝑖
𝑚𝑖 𝜔𝑐𝑖
𝜏𝑖
conductivities
electron heat flux

𝐪𝑒 = 𝐪𝑒𝐮 + 𝐪𝑒𝑇

frictional heat flux

𝐪𝑒𝐮 = 0.71𝑛𝑘𝑇𝑒 𝐮∥ +

thermal gradient
heat flux

3𝑛𝑘𝑇𝑒
𝐛 × 𝐮⟂
2𝜔𝑐𝑒 𝜏𝑒
𝑒
𝑒
𝑒
𝐪𝑇 = −𝜅∥ ∇∥ (𝑘𝑇𝑒 ) − 𝜅⟂ ∇⟂ (𝑘𝑇𝑒 ) − 𝜅∧𝑒 𝐛 × ∇⟂ (𝑘𝑇𝑒 )

𝑛𝑘𝑇𝑒 𝜏𝑒
𝑛𝑘𝑇𝑒
5𝑛𝑘𝑇𝑒
electron thermal
𝜅∥𝑒 = 3.2
; 𝜅⟂𝑒 = 4.7
; 𝜅∧𝑒 =
2
𝑚𝑒
2𝑚𝑒 𝜔𝑐𝑒
𝑚𝑒 𝜔𝑐𝑒
𝜏𝑒
conductivities
𝜂
𝜂
stress tensor (either 𝑥𝑥 = − 0 (𝑊𝑥𝑥 + 𝑊𝑦𝑦 ) − 1 (𝑊𝑥𝑥 − 𝑊𝑦𝑦 ) − 𝜂3 𝑊𝑥𝑦 ;
2
2
species)
𝜂0
𝜂1
𝑦𝑦 = − (𝑊𝑥𝑥 + 𝑊𝑦𝑦 ) + (𝑊𝑥𝑥 − 𝑊𝑦𝑦 ) + 𝜂3 𝑊𝑥𝑦 ;
2
2
𝜂
𝑥𝑦 = 𝑦𝑥 = −𝜂1 𝑊𝑥𝑦 + 3 (𝑊𝑥𝑥 − 𝑊𝑦𝑦 );
2
𝑥𝑧 = 𝑧𝑥 = −𝜂2 𝑊𝑥𝑧 − 𝜂4 𝑊𝑦𝑧 ;
𝑦𝑧 = 𝑧𝑦 = −𝜂2 𝑊𝑦𝑧 + 𝜂4 𝑊𝑥𝑧 ;
𝑧𝑧 = −𝜂0 𝑊𝑧𝑧
(here the 𝑧 axis is defined parallel to B);
3𝑛𝑘𝑇𝑖
6𝑛𝑘𝑇𝑖
; 𝜂2𝑖 =
;
ion viscosity
𝜂0𝑖 = 0.96𝑛𝑘𝑇𝑖 𝜏𝑖 ; 𝜂1𝑖 =
2
2
10𝜔𝑐𝑖
𝜏𝑖
5𝜔𝑐𝑖
𝜏𝑖
𝑛𝑘𝑇
𝑛𝑘𝑇
𝑖
𝑖
; 𝜂4𝑖 =
;
𝜂3𝑖 =
2𝜔𝑐𝑖
𝜔𝑐𝑖
𝑛𝑘𝑇
𝑛𝑘𝑇
electron viscosity
𝜂𝑒0 = 0.73𝑛𝑘𝑇𝑒 𝜏𝑒 ; 𝜂𝑒1 = 0.51 2 𝑒 ; 𝜂𝑒2 = 2.0 2 𝑒 ;
𝜔𝑐𝑒 𝜏𝑒
𝜔𝑐𝑒 𝜏𝑒
𝑛𝑘𝑇𝑒
𝑛𝑘𝑇𝑒
; 𝜂𝑒4 = −
.
𝜂𝑒3 = −
2𝜔𝑐𝑒
𝜔𝑐𝑒
37

## PDF page 38

For both species the rate-of-strain tensor is defined as
∂𝑣𝑗
∂𝑣
2
𝑊𝑗𝑘 =
+ 𝑘 − 𝛿𝑗𝑘 ∇ ⋅ 𝐯.
∂𝑥𝑘
∂𝑥𝑗
3
When B = 0 the following simplifications occur:
R𝐮 = 𝑛𝑒𝐣/𝜎∥ ;

R𝑇 = −0.71𝑛∇(𝑘𝑇𝑒 );

𝐪𝑖 = −𝜅∥𝑖 ∇(𝑘𝑇𝑖 );

𝐪𝑒𝐮 = 0.71𝑛𝑘𝑇𝑒 𝐮;

𝐪𝑒𝑇 = −𝜅∥𝑒 ∇(𝑘𝑇𝑒 );

𝑗𝑘 = −𝜂0 𝑊𝑗𝑘 .

For 𝜔𝑐𝑒 𝜏𝑒 ≫ 1 ≫ 𝜔𝑐𝑖 𝜏𝑖 , the electrons obey the high-field expressions and the
ions obey the zero-field expressions.
Collisional transport theory is applicable when (1) macroscopic time rates of
change satisfy 𝑑/𝑑𝑡 ≪ 1/𝜏, where 𝜏 is the longest collisional time scale, and
(in the absence of a magnetic field) (2) macroscopic length scales 𝐿 satisfy
𝐿 ≫ 𝑙, where 𝑙 = 𝑣𝜏̄ is the mean free path. In a strong field, 𝜔𝑐𝑒 𝜏 ≫ 1, condition (2) is replaced by 𝐿∥ ≫ 𝑙 and 𝐿⟂ ≫ √𝑙𝑟𝑒 (𝐿⟂ ≫ 𝑟𝑒 in a uniform field),
where 𝐿∥ is a macroscopic scale parallel to the field B and 𝐿⟂ is the smaller
of 𝐵/|∇⟂ 𝐵| and the transverse plasma dimension. In addition, the standard
transport coefficients are valid only when (3) the Coulomb logarithm satisfies 𝜆 ≫ 1; (4) the electron gyroradius satisfies 𝑟𝑒 ≫ 𝜆𝐷 , or 8𝜋𝑛𝑒 𝑚𝑒 𝑐2 ≫ 𝐵 2 ;
(5) relative drifts 𝐮 = 𝐯𝛼 − 𝐯𝛽 between two species are small compared with
the thermal velocities, i.e., 𝑢2 ≪ 𝑘𝑇𝛼 /𝑚𝛼 , 𝑘𝑇𝛽 /𝑚𝛽 ; and (6) anomalous transport processes owing to microinstabilities are negligible.
Weakly Ionized Plasmas
Collision frequency for scattering of charged particles of species 𝛼 by neutrals is
𝛼|0
𝜈𝛼 = 𝑛0 𝜎𝑠 (𝑘𝑇𝛼 /𝑚𝛼 )1/2 ,
𝛼|0

where 𝑛0 is the neutral density, 𝜎𝑠 is the cross section, typically ∼ 5 × 10−15
cm2 and weakly dependent on temperature, and (𝑇0 /𝑚0 )1/2 <
(𝑇𝛼 /𝑚𝛼 )1/2 where 𝑇0 and 𝑚0 are the temperature and mass of the neutrals.
When the system is small compared with a Debye length, 𝐿 ≪ 𝜆𝐷 , the
charged particle diffusion coefficients are
𝐷𝛼 = 𝑘𝑇𝛼 /𝑚𝛼 𝜈𝛼 ,
In the opposite limit, both species diffuse at the ambipolar rate
(𝑇 + 𝑇𝑒 )𝐷𝑖 𝐷𝑒
𝜇 𝐷 − 𝜇𝑒 𝐷𝑖
= 𝑖
,
𝐷𝐴 = 𝑖 𝑒
𝜇𝑖 − 𝜇𝑒
𝑇𝑖 𝐷𝑒 + 𝑇𝑒 𝐷𝑖

38

## PDF page 39

where 𝜇𝛼 = 𝑒𝛼 /𝑚𝛼 𝜈𝛼 is the mobility. The conductivity 𝜎𝛼 satisfies 𝜎𝛼 =
𝑛𝛼 𝑒𝛼 𝜇𝛼 .
In the presence of a magnetic field B the scalars 𝜇 and 𝜎 become tensors,
𝐉𝛼 = 𝜎 𝛼 ⋅ E = 𝜎∥𝛼 E∥ + 𝜎⟂𝛼 E⟂ + 𝜎∧𝛼 E × 𝐛,
where 𝐛 = B/𝐵 and
𝜎∥𝛼 = 𝑛𝛼 𝑒𝛼2 /𝑚𝛼 𝜈𝛼 ;
2
𝜎⟂𝛼 = 𝜎∥𝛼 𝜈𝛼2 /(𝜈𝛼2 + 𝜔𝑐𝛼
);
2
).
𝜎∧𝛼 = 𝜎∥𝛼 𝜈𝛼 𝜔𝑐𝛼 /(𝜈𝛼2 + 𝜔𝑐𝛼

Here 𝜎⟂ and 𝜎∧ are the Pedersen and Hall conductivities, respectively.

39

## PDF page 40

APPROXIMATE MAGNITUDES IN SOME TYPICAL PLASMAS
Plasma Type

3

𝜈𝑒𝑖 sec−1

𝑛 cm−3 𝑇 eV 𝜔𝑝𝑒 sec−1

𝜆𝐷 cm

𝑛𝜆𝐷

7 × 102

4 × 108 7 × 10−5

20

8 × 106 6 × 10−2

1

6 × 104

Gaseous nebula

3

10

1

2 × 10

6

Solar Corona

109

102

2 × 109

2 × 10−1 8 × 106

60

Diffuse hot
plasma

1012

102

6 × 1010

7 × 10−3 4 × 105

40

Solar atmosphere,
gas discharge

1014

1

6 × 1011

7 × 10−5

Warm plasma

1014

10

6 × 1011

2 × 10−4 8 × 102

Hot plasma

1014

102

6 × 1011

7 × 10−4 4 × 104 4 × 106

Thermonuclear
plasma

1015

104

2 × 1012

2 × 10−3 8 × 106 5 × 104

Theta pinch

1016

102

6 × 1012

7 × 10−5 4 × 103 3 × 108

Dense hot plasma

1018

102

6 × 1013

7 × 10−6 4 × 102 2 × 1010

Laser Plasma

1020

102

6 × 1014

7 × 10−7

Interstellar gas

1

40

40

2 × 109
107

2 × 1012

The diagram (facing) gives comparable information in graphical form.22

40

## PDF page 41

25
50% ionization
hydrogen plasma

(4π/3)nλ3D < 1

Laser
Plasma

20
Shock
tubes

High
pressure
arcs

Focus

Z-pinches

λi-i
λe-e > 1 cm
Fusion
reactor

log10 n (cm-3)

15
Fusion
experiments

Low
pressure
Alkali
metal
plasma

10
Glow
discharge

Flames

Solar
corona

λD > 1 cm

5

Earth
ionoshpere

Solar Wind
(1 AU)

0
−2

−1

0

1

Earth
plasma sheet

2

3

4

5

log10 T (eV)

41

## PDF page 42

IONOSPHERIC PARAMETERS23
The following tables give average nighttime values. Where two numbers are
entered, the first refers to the lower and the second to the upper portion of
the layer.
Quantity
Altitude (km)

E Region

F Region

90 − 160

160 − 500

1.5 × 1010 − 3.0 × 1010

5 × 1010 − 2 × 1011

9 × 1014

4.5 × 1015

Ion-neutral collision
frequency (sec−1 )

2 × 103 − 102

0.5 − 0.05

Ion gyro-/collision
frequency ratio 𝜅𝑖

0.09 − 2.0

4.6 × 102 − 5.0 × 103

Ion Pederson factor
𝜅𝑖 /(1 + 𝜅𝑖 2 )

0.09 − 0.5

2.2 × 10−3 − 2 × 10−4

8 × 10−4 − 0.8

1.0

Electron-neutral collision
frequency

1.5 × 104 − 9.0 × 102

80 − 10

Electron gyro-/collision
frequency ratio 𝜅𝑒

4.1 × 102 − 6.9 × 103

7.8 × 104 − 6.2 × 105

Electron Pedersen factor
𝜅𝑒 /(1 + 𝜅𝑒 2 )

2.7×10−3 −1.5×10−4

10−5 − 1.5 × 10−6

1.0

1.0

Number density (m−3 )
Height-integrated number
density (m−2 )

Ion Hall factor
𝜅𝑖 2 /(1 + 𝜅𝑖 2 )

Electron Hall factor
𝜅𝑒 2 /(1 + 𝜅𝑒 2 )
Mean molecular weight

28 − 26

22 − 16

Ion gyrofrequency (sec−1 )

180 − 190

230 − 300

Neutral diffusion
coefficient (m2 sec−1 )

30 − 5 × 103

105

The terrestrial magnetic field in the lower ionosphere at equatorial latitudes
is approximately 𝐵0 = 0.35 × 10−4 T. The earth’s radius is 𝑅𝐸 = 6371 km.
42

## PDF page 43

SOLAR PHYSICS PARAMETERS24
Parameter

Symbol

Total mass
𝑀⊙
Radius
𝑅⊙
Surface gravity
𝑔⊙
Escape speed
𝑣∞
Upward mass flux in spicules
—
Vertically integrated atmospheric density —
Sunspot magnetic field strength
𝐵max
Surface effective temperature
𝑇0
Radiant power
ℒ⊙
Radiant flux density
ℱ
Optical depth at 500 nm, measured from
𝜏5
photosphere
Astronomical unit (radius of earth’s orbit) AU
Solar constant (intensity at 1 AU)
𝑓

Value

Units
33

1.99 × 10
g
6.96 × 1010
cm
2.74 × 104
cm s−2
7
6.18 × 10
cm s−1
1.6 × 10−9 g cm−2 s−1
4.28
g cm−2
2500–3500
G
5770
K
3.83 × 1033
erg s−1
6.28 × 1010 erg cm−2 s−1
0.99
—
1.50 × 1013
cm
1.36 × 106 erg cm−2 s−1

Chromosphere and Corona25
Parameter (Units)

Quiet
Sun

Coronal
Hole

Active
Region

Chromospheric radiation losses
(erg cm−2 s−1 )
Low chromosphere
2 × 106
2 × 106
≳ 107
Middle chromosphere
2 × 106
2 × 106
107
Upper chromosphere
3 × 105
3 × 105
2 × 106
Total
4 × 106
4 × 106 ≳ 2 × 107
Transition layer pressure (dyne cm−2 )
0.2
0.07
2
Coronal temperature (K) at 1.1 R⊙
1.1 − 1.6 × 106
106
2.5 × 106
Coronal energy losses (erg cm−2 s−1 )
Conduction
2 × 105
6 × 104 105 − 107
Radiation
105
104
5 × 106
Solar Wind
≲ 5 × 104
7 × 105
< 105
Total
3 × 105
8 × 105
107
Solar wind mass loss (g cm−2 s−1 )
≲ 2 × 10−11 2 × 10−10 < 4×10−11
43

## PDF page 44

THERMONUCLEAR FUSION26
Natural abundance of isotopes:
hydrogen
𝑛D /𝑛H = 1.5 × 10−4
helium
𝑛He3 /𝑛He4 = 1.3 × 10−6
lithium
𝑛Li6 /𝑛Li7 = 0.08
Mass ratios:
𝑚𝑒 /𝑚D
(𝑚𝑒 /𝑚D )1/2
𝑚𝑒 /𝑚T
(𝑚𝑒 /𝑚T )1/2

= 2.72 × 10−4 = 1/3670
= 1.65 × 10−2 = 1/60.6
= 1.82 × 10−4 = 1/5496
= 1.35 × 10−2 = 1/74.1

Fusion reactions (branching ratios are correct for energies near the cross section peaks; a negative yield means the reaction is endothermic):27
(1a) D + D ⃗
50% T(1.01 MeV) + p(3.02 MeV)
3
(1b)
⃗
50% He (0.82 MeV) + n(2.45 MeV)
4
(2)
D + T ⃗ He (3.5 MeV) + n(14.1 MeV)
(3)
D + He3 ⃗ He4 (3.6 MeV) + p(14.7 MeV)
(4)
T + T ⃗ He4 + 2n + 11.3 MeV
4
(5a) He3 + T ⃗
51% He + p + n + 12.1 MeV
4
He
(4.8 MeV) + D(9.5 MeV)
(5b)
⃗
43%
5
(5c)
He
(1.89
MeV) + p(9.46 MeV)
⃗
6%
(6)
p + Li6 ⃗ He4 (1.7 MeV) + He3 (2.3 MeV)
4
(7a) p + Li7 ⃗
20% 2 He + 17.3 MeV
7
(7b)
⃗
80% Be + n − 1.6 MeV
(8)
D + Li6 ⃗ 2He4 + 22.4 MeV
(9)
p + B11 ⃗ 3 He4 + 8.7 MeV
(10) n + Li6 ⃗ He4 (2.1 MeV) + T(2.7 MeV)
The total cross section in barns (1 barn = 10−24 cm2 ) as a function of 𝐸, the
energy in keV of the incident particle [the first ion on the left side of Eqs. (1)–
(5)], assuming the target ion at rest, can be fitted by28𝑎
−1

𝜎𝑇 (𝐸) =

𝐴5 + [(𝐴4 − 𝐴3 𝐸)2 + 1] 𝐴2
𝐸 [exp(𝐴1 𝐸−1/2 ) − 1]

where the Duane coefficients 𝐴𝑗 for the principal fusion reactions are as follows:
44

## PDF page 45

D–D
(1a)

D–D
(1b)

D–He3
(3)

D–T
(2)

𝐴1
46.097
47.88
𝐴2
372
482
𝐴3 4.36 × 10−4 3.08 × 10−4
𝐴4
1.220
1.177
𝐴5
0
0

45.95
5.02 × 104
1.368 × 10−2
1.076
409

T–He3
(5a–c)

T–T
(4)

89.27
38.39
2.59 × 104
448
3.98 × 10−3 1.02 × 10−3
1.297
2.09
647
0

123.1
11250
0
0
0

Reaction rates 𝜎𝑣 (in cm3 sec−1 ), averaged over Maxwellian distributions:
Temperature
(keV)

D−D
(1a + 1b)

D−T
(2)

D − He3
(3)

T−T
(4)

T − He3
(5a–c)

1.0
2.0
5.0
10.0
20.0
50.0
100.0
200.0
500.0
1000.0

1.5 × 10−22
5.4 × 10−21
1.8 × 10−19
1.2 × 10−18
5.2 × 10−18
2.1 × 10−17
4.5 × 10−17
8.8 × 10−17
1.8 × 10−16
2.2 × 10−16

5.5 × 10−21
2.6 × 10−19
1.3 × 10−17
1.1 × 10−16
4.2 × 10−16
8.7 × 10−16
8.5 × 10−16
6.3 × 10−16
3.7 × 10−16
2.7 × 10−16

10−26
1.4 × 10−23
6.7 × 10−21
2.3 × 10−19
3.8 × 10−18
5.4 × 10−17
1.6 × 10−16
2.4 × 10−16
2.3 × 10−16
1.8 × 10−16

3.3 × 10−22
7.1 × 10−21
1.4 × 10−19
7.2 × 10−19
2.5 × 10−18
8.7 × 10−18
1.9 × 10−17
4.2 × 10−17
8.4 × 10−17
8.0 × 10−17

10−28
10−25
2.1 × 10−22
1.2 × 10−20
2.6 × 10−19
5.3 × 10−18
2.7 × 10−17
9.2 × 10−17
2.9 × 10−16
5.2 × 10−16

For low energies (𝑇 ≲ 25 keV) the data may be represented by
(𝜎𝑣)DD = 2.33 × 10−14 𝑇 −2/3 exp(−18.76𝑇 −1/3 ) cm3 sec−1 ;
(𝜎𝑣)DT = 3.68 × 10−12 𝑇 −2/3 exp(−19.94𝑇 −1/3 ) cm3 sec−1 ,
where 𝑇 is measured in keV.
A three-parameter model has also been developed for fusion cross-sections of
light nuclei.28𝑏
The power density released in the form of charged particles is
𝑃DD = 3.3 × 10−13 𝑛D 2 (𝜎𝑣)DD watt cm−3 (including the subsequent
prompt D–T reaction only);
𝑃DT = 5.6 × 10−13 𝑛D 𝑛T (𝜎𝑣)DT watt cm−3 ;
𝑃DHe3 = 2.9 × 10−12 𝑛D 𝑛He3 (𝜎𝑣)DHe3 watt cm−3 .
45

## PDF page 46

RELATIVISTIC ELECTRON BEAMS
2 −1/2

Here 𝛾 = (1 − 𝛽 )
is the relativistic scaling factor; quantities in analytic
formulas are expressed in SI or cgs units, as indicated; in numerical formulas,
𝐼 is in amperes (A), 𝐵 is in gauss (G), electron linear density 𝑁 is in cm−1 ,
and temperature, voltage and energy are in MeV; 𝛽𝑧 = 𝑣𝑧 /𝑐; 𝑘 is Boltzmann’s
constant.
Relativistic electron gyroradius:
𝑟𝑒 =

𝑚𝑐2 2
(𝛾 − 1)1/2 (cgs) = 1.70 × 103 (𝛾2 − 1)1/2 𝐵 −1 cm.
𝑒𝐵

Relativistic electron energy:
𝑊 = 𝑚𝑐2 𝛾 = 0.511𝛾 MeV.
Bennett pinch condition:
𝐼 2 = 2𝑁𝑘(𝑇𝑒 + 𝑇𝑖 )𝑐2 (cgs) = 3.20 × 10−4 𝑁(𝑇𝑒 + 𝑇𝑖 ) A2 .
Alfvén-Lawson limit:
𝐼𝐴 = (𝑚𝑐3 /𝑒)𝛽𝑧 𝛾 (cgs) = (4𝜋𝑚𝑐/𝜇0 𝑒)𝛽𝑧 𝛾 (SI) = 1.70 × 104 𝛽𝑧 𝛾 A.
The ratio of net current to 𝐼𝐴 is
𝐼
𝜈
= .
𝐼𝐴
𝛾
Here 𝜈 = 𝑁𝑟𝑒 is the Budker number, where 𝑟𝑒 = 𝑒2 /𝑚𝑐2 = 2.82 × 10−13 cm is
the classical electron radius. Beam electron number density is
𝑛𝑏 = 2.08 × 108 𝐽𝛽 −1 cm−3 ,
where 𝐽 is the current density in A cm−2 . For a uniform beam of radius 𝑎 (in
cm),
𝑛𝑏 = 6.63 × 107 𝐼𝑎−2 𝛽−1 cm−3 ,
and
2𝑟𝑒
𝜈
= .
𝑎
𝛾
Child’s law: (non-relativistic) space-charge-limited current density between
parallel plates with voltage drop 𝑉 (in MV) and separation 𝑑 (in cm) is
𝐽 = 2.34 × 103 𝑉 3/2 𝑑−2 A cm
46

−2

.

## PDF page 47

The saturated parapotential current (magnetically self-limited flow along
equipotentials in pinched diodes and transmission lines) is29
𝐼𝑝 = 8.5 × 103 𝐺𝛾 ln [𝛾 + (𝛾2 − 1)1/2 ] A,
where 𝐺 is a geometrical factor depending on the diode structure:
for parallel plane cathode and anode of width
𝑤
𝐺=
2𝜋𝑑
𝑤, separation 𝑑;
𝐺 = (ln

𝑅2
)
𝑅1

−1

for cylinders of radii 𝑅1 (inner) and 𝑅2 (outer);

𝑅𝑐
for conical cathode of radius 𝑅𝑐 , maximum
separation 𝑑0 (at 𝑟 = 𝑅𝑐 ) from plane anode.
𝑑0
For 𝛽 → 0 (𝛾 → 1), both 𝐼𝐴 and 𝐼𝑝 vanish.
𝐺=

The condition for a longitudinal magnetic field 𝐵𝑧 to suppress filamentation
in a beam of current density 𝐽 (in A cm−2 ) is
𝐵𝑧 > 47𝛽𝑧 (𝛾𝐽)1/2 G.
Voltage registered by Rogowski coil of minor cross-sectional area 𝐴, 𝑛 turns,
major radius 𝑎, inductance 𝐿, external resistance 𝑅 and capacitance 𝐶 (all in
SI):
externally integrated
self-integrating

𝑉 = (1/𝑅𝐶)(𝑛𝐴𝜇0 𝐼/2𝜋𝑎);
𝑉 = (𝑅/𝐿)(𝑛𝐴𝜇0 𝐼/2𝜋𝑎) = 𝑅𝐼/𝑛.

X-ray production, target with average atomic number 𝑍 (𝑉 ≲ 5 MeV):
𝜂 ≡ x-ray power/beam power = 7 × 10−4 𝑍𝑉.
X-ray dose at 1 meter generated by an e-beam normally-incident on material
with atomic number 𝑍, depositing total charge 𝑄 while the pulse voltage is
within 84% of peak (𝑉 ≥ 0.84𝑉max ):
2.8
𝐷 = 150𝑉max
𝑄𝑍 1/2 rads.

47

## PDF page 48

BEAM INSTABILITIES30
Name

Conditions

Saturation Mechanism

Electron-electron

𝑉𝑑 > 𝑉𝑒𝑗̄ , 𝑗 = 1, 2

Electron trapping until
𝑉𝑒𝑗̄ ∼ 𝑉𝑑

Buneman

𝑉𝑑 > (𝑀/𝑚)1/3 𝑉𝑖̄ ,
𝑉𝑑 > 𝑉𝑒̄

Electron trapping until 𝑉𝑒̄ ∼ 𝑉𝑑

Beam-plasma

𝑉𝑏 > (𝑛𝑝 /𝑛𝑏 )1/3 𝑉𝑏̄

Trapping of beam electrons

1/3

𝑉𝑏̄

Weak beam-plasma

𝑉𝑏 < (𝑛𝑝 /𝑛𝑏 )

Beam-plasma
(hot-electron)

𝑉𝑒̄ > 𝑉𝑏 > 𝑉𝑏̄

Quasilinear or nonlinear

Ion acoustic

𝑇𝑒 ≫ 𝑇𝑖 , 𝑉𝑑 ≫ 𝐶𝑠

Quasilinear, ion tail formation,
nonlinear scattering, or
resonance broadening.

Anisotropic
𝑇𝑒⟂ > 2𝑇𝑒∥
temperature (hydro)

Quasilinear or nonlinear
(mode coupling)

Isotropization

Ion cyclotron

𝑉𝑑 > 20𝑉𝑖̄
(for 𝑇𝑒 ≈ 𝑇𝑖 )

Ion heating

Beam-cyclotron
(hydro)

𝑉𝑑 > 𝐶𝑠

Resonance broadening

Modified two-stream
(hydro)

𝑉𝑑 < (1 + 𝛽)1/2 𝑉𝐴 ,
𝑉𝑑 > 𝐶𝑠

Trapping

Ion-ion (equal beams)

𝑈 < 2(1 + 𝛽)1/2 𝑉𝐴 Ion trapping

Ion-ion (equal beams)

𝑈 < 2𝐶𝑠

For nomenclature, see p. 50.

48

Ion trapping

## PDF page 49

Parameters of Most Unstable Mode
Name

Growth Rate

Frequency

1
𝜔
2 𝑒

0

0.9

𝜔𝑒
𝑉𝑑

0

𝑚 1/3
) 𝜔𝑒
𝑀
1/3
𝑛
𝜔𝑒 − 0.4 ( 𝑏 ) 𝜔𝑒
𝑛𝑝

𝜔𝑒
𝑉𝑑
𝜔𝑒
𝑉𝑏
𝜔𝑒
𝑉𝑏

2
𝑉
3 𝑑
2
𝑉
3 𝑏
3𝑉𝑒̄ 2
𝑉𝑏

𝑉𝑏
𝜔𝑒
𝑉𝑒̄

𝜆−1
𝐷

𝑉𝑏

Electronelectron
Buneman
Beam-plasma
Weak
beam-plasma

𝑚 1/3
) 𝜔𝑒
𝑀
1/3
𝑛
0.7 ( 𝑏 ) 𝜔𝑒
𝑛𝑝
2
𝑛𝑏 𝑉𝑏
( ) 𝜔𝑒
2𝑛𝑝 𝑉𝑏̄
0.7 (

1/2

Beam-plasma
(hot-electron)

(

𝑛𝑏
)
𝑛𝑝

𝑉𝑒̄
𝜔
𝑉𝑏 𝑒

0.4 (

𝜔𝑒

Wave
Group
Number Velocity

𝑚 1/2
) 𝜔𝑖
𝑀
Ω𝑒

𝜔𝑖

𝜆−1
𝐷

𝐶𝑠

𝜔𝑒 cos 𝜃 ∼ Ω𝑒

𝑟𝑒−1

̄
𝑉𝑒⟂

0.1Ω𝑖

1.2Ω𝑖

𝑟𝑖−1

0.7Ω𝑒

𝑛Ω𝑒

0.7𝜆−1
𝐷

1
Ω
2 𝐻

0.9Ω𝐻

1.7

1 ̄
𝑉
3 𝑖
≳ 𝑉𝑑 ;
≲ 𝐶𝑠
1
𝑉
2 𝑑

0.4Ω𝐻

0

1.2

Ion-ion
0.4𝜔𝑖
(equal beams)
For nomenclature, see p. 50.

0

Ion acoustic
Anisotropic
temperature
(hydro)
Ion cyclotron
Beam-cyclotron
(hydro)
Modified
two-stream
(hydro)
Ion-ion
(equal beams)

(

Ω𝐻
𝑉𝑑

Ω𝐻
𝑈
𝜔𝑖
1.2
𝑈

0
0

49

## PDF page 50

In the preceding tables, subscripts 𝑒, 𝑖, 𝑑, 𝑏, 𝑝 stand for “electron,” “ion,”
“drift,” “beam,” and “plasma,” respectively. Thermal velocities are denoted
by a bar. In addition, the following are used:
𝑚
𝑀
𝑉
𝑇
𝑛𝑒 , 𝑛𝑖
𝑛
𝐶𝑠 = (𝑇𝑒 /𝑀)1/2
𝜔𝑒 , 𝜔𝑖
𝜆𝐷

50

electron mass
ion mass
velocity
temperature
number density
harmonic number
ion sound speed
plasma frequency
Debye length

𝑟𝑒 , 𝑟𝑖
𝛽
𝑉𝐴
Ω𝑒 , Ω𝑖
Ω𝐻
𝑈

gyroradius
plasma/magnetic energy
density ratio
Alfvén speed
gyrofrequency
hybrid gyrofrequency,
2
Ω𝐻 = Ω𝑒 Ω𝑖
relative drift velocity of
two ion species

## PDF page 51

LASERS
System Parameters
Efficiencies and power levels are approximate.31
Wavelength
Type
CO2
CO
Holmium
Iodine
Nd-glass
Nd:YAG
Nd:YLF
Nd:YVO4
Er:YAG
*Color center
*Ti:Sapphire
Ruby
He-Ne
*Argon ion
*OPO
N2
*Dye
Kr-F
Xenon
Ytterbium fiber
Erbium fiber
Semiconductor
*Tunable sources

Power levels available (W)

(μm)

Efficiency

Pulsed

CW

10.6

0.01 − 0.02
(pulsed)
0.4
0.03† − 0.1‡
0.003
−
−
−

> 2 × 1013

> 105

5
> 109
2.06
> 107
1.315
3 × 1012
1.06
1.25 × 1015
1.064
109
1.045,
4 × 108
1.54, 1.313
1.064
−
−
2.94
−
1.5 × 105
1−4
10−3
5 × 108
0.7 − 1.5
0.4 × 𝜂𝑝
1014
−3
0.6943
< 10
1010
0.6328
10−4
−
0.45 − 0.60
10−3
5 × 104
0.3 − 10
> 0.1 × 𝜂𝑝
1010
0.3371
0.001 − 0.05
106
0.3 − 1.1
10−3
5 × 107
0.26
0.08
1012
0.175
0.02
> 108
1.05 − 1.1
0.55
5 × 107
1.534
−
7 × 106
0.375 − 1.9
> 0.5
3 × 109
†lamp-driven ‡diode-driven

> 100
80
−
−
> 104
80
> 20
−
1
150
1
1 − 50 × 10−3
150
5
−
> 100
500
−
104
100
> 103

Nd stands for Neodymium; Er stands for Erbium; Ti stands for Titanium;
YAG stands for Yttrium–Aluminum Garnet; YLF stands for Yttrium Lithium
Fluoride; YVO5 stands for Yttrium Vanadate; OPO for Optical Parametric
Oscillator; 𝜂𝑝 is pump laser efficiency.
51

## PDF page 52

Formulas
An e-m wave with 𝐤 ∥ 𝐁 has an index of refraction given by
𝑛± = [1 − 𝜔𝑝𝑒2 /𝜔(𝜔 ∓ 𝜔𝑐𝑒 )]1/2 ,
where ± refers to the helicity. The rate of change of polarization angle 𝜃 as a
function of displacement 𝑠 (Faraday rotation) is given by
𝑑𝜃/𝑑𝑠 = (𝑘/2)(𝑛− − 𝑛+ ) = 2.36 × 104 𝑁𝐵𝑓−2 cm−1 ,
where 𝑁 is the electron number density, 𝐵 is the field strength, and 𝑓 is the
wave frequency, all in cgs.
The quiver velocity of an electron in an e-m field of angular frequency 𝜔 is
𝑣0 = 𝑒𝐸max /𝑚𝜔 = 25.6𝐼 1/2 𝜆0 cm sec−1
2

in terms of the laser flux 𝐼 = 𝑐𝐸max /8𝜋, with 𝐼 in watt/cm2 , laser wavelength
𝜆0 in μm. The ratio of quiver energy to thermal energy is
2

𝑊qu /𝑊th = 𝑚𝑒 𝑣0 2 /2𝑘𝑇 = 1.81 × 10−13 𝜆0 𝐼/𝑇,
where 𝑇 is given in eV. For example, if 𝐼 = 1015 W cm−2 , 𝜆0 = 1 μm, 𝑇 =
2 keV, then 𝑊qu /𝑊th ≈ 0.1.
Pondermotive force:
ℱ = 𝑁∇⟨𝐸 2 ⟩/8𝜋𝑁𝑐 ,
where
−3
𝑁𝑐 = 1.1 × 1021 𝜆−2
0 cm .

For uniform illumination of a lens with 𝑓-number 𝐹, the diameter 𝑑 at focus
(85% of the energy) and the depth of focus 𝑙 (distance to first zero in intensity) are given by
𝑑 ≈ 2.44𝐹𝜆𝜃/𝜃𝐷𝐿

and

𝑙 ≈ ±2𝐹 2 𝜆𝜃/𝜃𝐷𝐿 .

Here 𝜃 is the beam divergence containing 85% of energy and 𝜃𝐷𝐿 is the diffraction-limited divergence:
𝜃𝐷𝐿 = 2.44𝜆/𝑏,
where 𝑏 is the aperture. These formulas are modified for nonuniform (such
as Gaussian) illumination of the lens or for pathological laser profiles.

52

## PDF page 53

ATOMIC PHYSICS AND RADIATION
Energies and temperatures are in eV; all other units are cgs except where
noted. 𝑍 is the charge state (𝑍 = 0 refers to a neutral atom); the subscript 𝑒
labels electrons. 𝑁 refers to number density, 𝑛 to principal quantum number.
Asterisk superscripts on level population densities denote local thermodynamic equilibrium (LTE). Thus 𝑁𝑛 * is the LTE number density of atoms (or
ions) in level 𝑛.
Characteristic atomic collision cross section:
(1)

𝜋𝑎0 2 = 8.80 × 10−17 cm2 .

Binding energy of outer electron in level labeled by quantum numbers 𝑛, 𝑙:
(2)

𝑍
𝐸∞
(𝑛, 𝑙) = −

𝐻
𝑍 2 𝐸∞
,
(𝑛 − Δ𝑙 )2

𝐻
where 𝐸∞
= 13.6 eV is the hydrogen ionization energy and Δ𝑙 = 0.75𝑙−5 ,
𝑙 ≳ 5, is the quantum defect.

Excitation and Decay
Cross section (Bethe approximation) for electron excitation by dipole allowed
transition 𝑚 → 𝑛 (Refs. 32, 33):
𝑓 𝑔(𝑛, 𝑚)
(3) 𝜎𝑚𝑛 = 2.36 × 10−13 𝑚𝑛
cm2 ,
𝜖Δ𝐸𝑛𝑚
where 𝑓𝑚𝑛 is the oscillator strength, 𝑔(𝑛, 𝑚) is the Gaunt factor, 𝜖 is the incident electron energy, and Δ𝐸𝑛𝑚 = 𝐸𝑛 − 𝐸𝑚 .
Electron excitation rate averaged over Maxwellian velocity distribution, 𝑋𝑚𝑛
= 𝑁𝑒 ⟨𝜎𝑚𝑛 𝑣⟩ (Refs. 34, 35):
𝑓 ⟨𝑔(𝑛, 𝑚)⟩𝑁𝑒
Δ𝐸
exp (− 𝑛𝑚 ) sec−1 ,
(4) 𝑋𝑚𝑛 = 1.6 × 10−5 𝑚𝑛
𝑇𝑒
Δ𝐸𝑛𝑚 𝑇𝑒1/2
where ⟨𝑔(𝑛, 𝑚)⟩ denotes the thermal averaged Gaunt factor (generally ∼ 1 for
atoms, ∼ 0.2 for ions).

53

## PDF page 54

Rate for electron collisional deexcitation:
(5)

𝑌𝑛𝑚 = (𝑁𝑚 */𝑁𝑛 *)𝑋𝑚𝑛 .

Here 𝑁𝑚 */𝑁𝑛 * = (𝑔𝑚 /𝑔𝑛 ) exp(Δ𝐸𝑛𝑚 /𝑇𝑒 ) is the Boltzmann relation for level
population densities, where 𝑔𝑛 is the statistical weight of level 𝑛.
Rate for spontaneous decay 𝑛 → 𝑚 (Einstein 𝐴 coefficient)34
(6)

𝐴𝑛𝑚 = 4.3 × 107 (𝑔𝑚 /𝑔𝑛 )𝑓𝑚𝑛 (Δ𝐸𝑛𝑚 )2 sec−1 .

Intensity emitted per unit volume from the transition 𝑛 → 𝑚 in an optically
thin plasma:
(7)

3

𝐼𝑛𝑚 = 1.6 × 10−19 𝐴𝑛𝑚 𝑁𝑛 Δ𝐸𝑛𝑚 watt/cm .

Condition for steady state in a corona model:
(8)

𝑁0 𝑁𝑒 ⟨𝜎0𝑛 𝑣⟩ = 𝑁𝑛 𝐴𝑛0 ,

where the ground state is labelled by a zero subscript.
Hence for a transition 𝑛 → 𝑚 in ions, where ⟨𝑔(𝑛, 0)⟩ ≈ 0.2,
3

(9)

𝑓 𝑔 𝑁 𝑁 Δ𝐸
Δ𝐸
watt
.
𝐼𝑛𝑚 = 5.1 × 10−25 𝑛𝑚 𝑚 1/2𝑒 0 ( 𝑛𝑚 ) exp (− 𝑛0 )
Δ𝐸𝑛0
𝑇𝑒
cm3
𝑔0 𝑇𝑒

Ionization and Recombination
In a general time-dependent situation the number density of the charge state
𝑍 satisfies
(10)

𝑑𝑁(𝑍)
= 𝑁𝑒 [ − 𝑆(𝑍)𝑁(𝑍) − 𝛼(𝑍)𝑁(𝑍)
𝑑𝑡
+ 𝑆(𝑍 − 1)𝑁(𝑍 − 1) + 𝛼(𝑍 + 1)𝑁(𝑍 + 1)].

Here 𝑆(𝑍) is the ionization rate. The recombination rate 𝛼(𝑍) has the form
𝛼(𝑍) = 𝛼𝑟 (𝑍) + 𝑁𝑒 𝛼3 (𝑍), where 𝛼𝑟 and 𝛼3 are the radiative and three-body
recombination rates, respectively.

54

## PDF page 55

Classical ionization cross-section36 for any atomic shell 𝑗
(11) 𝜎𝑖 = 6 × 10−14 𝑏𝑗 𝑔𝑗 (𝑥)/𝑈𝑗 2 cm2 .
Here 𝑏𝑗 is the number of shell electrons; 𝑈𝑗 is the binding energy of the ejected
electron; 𝑥 = 𝜖/𝑈𝑗 , where 𝜖 is the incident electron energy; and 𝑔 is a universal function with a minimum value 𝑔min ≈ 0.2 at 𝑥 ≈ 4.
Ionization from the ground state, averaged over Maxwellian electron distri𝑍
bution, for 0.02 ≲ 𝑇𝑒 /𝐸∞
≲ 100 (Ref. 35):
(12) 𝑆(𝑍) = 10−5

𝑍 1/2
(𝑇𝑒 /𝐸∞
)
𝐸𝑍
exp (− ∞ ) cm3 /sec,
𝑍 )3/2 (6.0 + 𝑇 /𝐸 𝑍 )
𝑇𝑒
(𝐸∞
𝑒 ∞

𝑍
where 𝐸∞
is the ionization energy.

Electron-ion radiative recombination rate (𝑒 + 𝑁(𝑍) → 𝑁(𝑍 − 1) + ℎ𝜈)
is in error ≤ 0.5% for 𝑇𝑒 /𝑍 2 ≲ 8.6 eV, by ∼ 3% for 𝑇𝑒 /𝑍 2 ≲ 86 eV, and by
∼ 31% for 𝑇𝑒 /𝑍 2 ≲ 431 eV (Ref. 37):
1/2

(13) 𝛼𝑟 (𝑍) = 5.2 × 10−14 𝑍 (

𝑍
𝐸∞
)
𝑇𝑒

[0.43 +

1
𝑍
ln(𝐸∞
/𝑇𝑒 )
2
𝑍
+ 0.469(𝐸∞
/𝑇𝑒 )−1/3 ] cm3 /sec.

For 1 eV < 𝑇𝑒 /𝑍 2 < 15 eV, this becomes approximately35
(14) 𝛼𝑟 (𝑍) = 2.7 × 10−13 𝑍 2 𝑇𝑒 −1/2 cm3 /sec.
Collisional (three-body) recombination rate for singly ionized plasma:38
(15) 𝛼3 = 8.75 × 10−27 𝑇𝑒 −4.5 cm6 /sec.
Photoionization cross section for ions in level 𝑛, 𝑙 (short-wavelength limit):
(16) 𝜎ph (𝑛, 𝑙) = 1.64 × 10−16 𝑍 5 /𝑛3 𝐾 7+2𝑙 cm2 ,
where 𝐾 is the wavenumber in Rydbergs (1 Rydberg = 1.0974 × 105 cm−1 ).

55

## PDF page 56

Ionization Equilibrium Models
Saha equilibrium:39
3/2

(17)

𝑔𝑍 𝑇𝑒
𝑁𝑒 𝑁1 *(𝑍)
𝐸𝑍 (𝑛, 𝑙)
= 6.0 × 1021 1 𝑍−1
exp (− ∞
) cm−3 ,
𝑇𝑒
𝑁𝑛 *(𝑍 − 1)
𝑔𝑛

𝑍
where 𝑔𝑍𝑛 is the statistical weight for level 𝑛 of charge state 𝑍 and 𝐸∞
(𝑛, 𝑙)
is the ionization energy of the neutral atom initially in level (𝑛, 𝑙), given by
Eq. (2).

In a steady state at high electron density,
𝑁𝑒 𝑁*(𝑍)
𝑆(𝑍 − 1)
=
,
𝛼3
𝑁*(𝑍 − 1)
is a function only of 𝑇.
(18)

Conditions for LTE:39
(a) Collisional and radiative excitation rates for a level 𝑛 must satisfy
(19) 𝑌𝑛𝑚 ≳ 10𝐴𝑛𝑚 .
(b) Electron density must satisfy
𝑍 1/2
(20) 𝑁𝑒 ≳ 7 × 1018 𝑍 7 𝑛−17/2 (𝑇/𝐸∞
) cm−3 .

Steady state condition in corona model:
𝛼𝑟
𝑁(𝑍 − 1)
(21)
=
.
𝑁(𝑍)
𝑆(𝑍 − 1)
Corona model is applicable if 40
(22) 1012 𝑡𝐼 −1 < 𝑁𝑒 < 1016 𝑇𝑒 7/2 cm−3 ,
where 𝑡𝐼 is the ionization time.

56

## PDF page 57

Radiation
Note: Energies and temperatures are in eV; all other quantities are in cgs
units except where noted. 𝑍 is the charge state (𝑍 = 0 refers to a neutral
atom); the subscript 𝑒 labels electrons. 𝑁 is number density.
Average radiative decay rate of a state with principal quantum number 𝑛 is
(23) 𝐴𝑛 = ∑ 𝐴𝑛𝑚 = 1.6 × 1010 𝑍 4 𝑛−9/2 sec.
𝑚<𝑛

Natural linewidth (Δ𝐸 in eV):
(24) Δ𝐸 Δ𝑡 = ℎ = 4.14 × 10−15 eV sec,
where Δ𝑡 is the lifetime of the line.
Doppler width:
(25) Δ𝜆/𝜆 = 7.7 × 10−5 (𝑇/𝜇)1/2 ,
where 𝜇 is the mass of the emitting atom or ion scaled by the proton mass.
Optical depth for a Doppler-broadened line:39
(26) 𝜏 = 3.52 × 10−13 𝑓𝑛𝑚 𝜆(𝑀𝑐2 /𝑘𝑇)1/2 𝑁𝐿 = 5.4 × 10−9 𝑓𝑚𝑛 𝜆(𝜇/𝑇)1/2 𝑁𝐿,
where 𝑓𝑛𝑚 is the absorption oscillator strength, 𝜆 is the wavelength, and 𝐿 is
the physical depth of the plasma; 𝑀, 𝑁, and 𝑇 are the mass, number density,
and temperature of the absorber; 𝜇 is 𝑀 divided by the proton mass. Optically thin means 𝜏 < 1.
Resonance absorption cross section at center of line:
(27) 𝜎𝜆=𝜆𝑐 = 5.6 × 10−13 𝜆2 /Δ𝜆 cm2 .
Wien displacement law (wavelength of maximum black-body emission):
(28) 𝜆max = 2.50 × 10−5 𝑇 −1 cm.
Radiation from the surface of a black body at temperature 𝑇:
2

(29) 𝑊 = 1.03 × 105 𝑇 4 watt/cm .
57

## PDF page 58

Bremsstrahlung from hydrogen-like plasma:26
3

(30) 𝑃Br = 1.69 × 10−32 𝑁𝑒 𝑇𝑒 1/2 ∑ [𝑍 2 𝑁(𝑍)] watt/cm ,
where the sum is over all ionization states 𝑍.
Bremsstrahlung optical depth:41
(31) 𝜏 = 5.0 × 10−38 𝑁𝑒 𝑁𝑖 𝑍 2 𝑔𝐿𝑇 −7/2 ,
where 𝑔 ≈ 1.2 is an average Gaunt factor and 𝐿 is the physical path length.
Inverse bremsstrahlung absorption coefficient42 for radiation of angular frequency 𝜔:
(32) 𝜅 = 3.1 × 10−7 𝑍𝑛𝑒 2 ln Λ 𝑇 −3/2 𝜔−2 (1 − 𝜔𝑝2 /𝜔2 )−1/2 cm−1 ;
here Λ is the electron thermal velocity divided by 𝑉, where 𝑉 is the larger of
𝜔 and 𝜔𝑝 multiplied by the larger of 𝑍𝑒2 /𝑘𝑇 and ℏ/(𝑚𝑘𝑇)1/2 .
Recombination (free-bound) radiation:
(33) 𝑃𝑟 = 1.69 × 10−32 𝑁𝑒 𝑇𝑒 1/2 ∑ [𝑍 2 𝑁(𝑍) (

𝑍−1
𝐸∞
3
)] watt/cm .
𝑇𝑒

Cyclotron radiation26 in magnetic field 𝐁:
3

(34) 𝑃𝑐 = 6.21 × 10−28 𝐵 2 𝑁𝑒 𝑇𝑒 watt/cm .
For 𝑁𝑒 𝑘𝑇𝑒 = 𝑁𝑖 𝑘𝑇𝑖 = 𝐵 2 /16𝜋 (𝛽 = 1, isothermal plasma),26
3

(35) 𝑃𝑐 = 5.00 × 10−38 𝑁𝑒2 𝑇𝑒2 watt/cm .
Cyclotron radiation energy loss 𝑒-folding time for a single electron:41
(36) 𝑡𝑐 ≈

9.0 × 108 𝐵−2
sec,
2.5 + 𝛾

where 𝛾 = (1 − (𝑣/𝑐)2 )−1/2 is the relativistic scaling factor.
Number of cyclotron harmonics41 trapped in a medium of finite depth 𝐿:
(37) 𝑚tr = (57𝛽𝐵𝐿)1/6 ,
where 𝛽 = 8𝜋𝑁𝑘𝑇/𝐵 2 .
Line radiation is given by summing Eq. (9) over all species in the plasma.
58

## PDF page 59

ATOMIC SPECTROSCOPY
Spectroscopic notation combines observational and theoretical elements. Observationally, spectral lines are grouped in series with line spacings which
decrease toward the series limit. Every line can be related theoretically to a
transition between two atomic states, each identified by its quantum numbers.
Ionization levels are indicated by roman numerals. Thus C I is neutral carbon, C II is singly ionized, etc. The state of a one-electron atom (hydrogen) or
ion (He II, Li III, etc.) is specified by identifying the principal quantum number 𝑛 = 1, 2, … , the orbital angular momentum 𝑙 = 0, 1, … , 𝑛 − 1, and the spin
angular momentum 𝑠 = ± 12 . The total angular momentum 𝑗 is the magnitude of the vector sum of 𝐥 and 𝐬, 𝑗 = 𝑙 ± 21 (𝑗 ≥ 12 ). The letters s, p, d, f, g, h,
i, k, l, …, respectively, are associated with angular momenta 𝑙 = 0, 1, 2, 3, 4, 5,
6, 7, 8, …. The atomic states of hydrogen and hydrogenic ions are degenerate:
neglecting fine structure, their energies depend only on 𝑛 according to
Ry𝑍 2
𝑅∞ ℎ𝑐𝑍 2 𝑛−2
=− 2 ,
1 + 𝑚/𝑀
𝑛
where ℎ is Planck’s constant, 𝑐 is the speed of light, 𝑚 is the electron mass, 𝑀
and 𝑍 are the mass and charge state of the nucleus, and
𝐸𝑛 = −

𝑅∞ = 109,737 cm−1
is the Rydberg constant. If 𝐸𝑛 is divided by ℎ𝑐, the result is in wavenumber
units. The energy associated with a transition 𝑚 → 𝑛 is given by
Δ𝐸𝑚𝑛 = Ry(1/𝑚2 − 1/𝑛2 ),
with 𝑚 < 𝑛 (𝑚 > 𝑛) for absorption (emission) lines.
For hydrogen and hydrogenic ions the series of lines belonging to the transitions 𝑚 → 𝑛 have conventional names:
Transition:

1→𝑛

2→𝑛

3→𝑛

4→𝑛

5→𝑛

6→𝑛

Name: Lyman

Balmer

Paschen Brackett

Pfund

Humphreys

Successive lines in any series are denoted 𝛼, 𝛽, 𝛾, etc. Thus the transition 1 →
3 gives rise to the Lyman-𝛽 line. Relativistic effects, quantum electrodynamic
effects (e.g., the Lamb shift), and interactions between the nuclear magnetic
moment and the magnetic field due to the electron produce small shifts and
splittings, ≲ 10−2 cm−1 ; these last are called “hyperfine structure.”
In many-electron atoms the electrons are grouped in closed and open shells,
with spectroscopic properties determined mainly by the outer shell. Shell

59

## PDF page 60

energies depend primarily on 𝑛; the shells corresponding to 𝑛 = 1, 2, 3, …
are called 𝐾, 𝐿, 𝑀, etc. A shell is made up of subshells of different angular
momenta, each labeled according to the values of 𝑛, 𝑙, and the number of
electrons it contains out of the maximum possible number, 2(2𝑙 + 1). For example, 2𝑝5 indicates that there are 5 electrons in the subshell corresponding
to 𝑙 = 1 (denoted by p) and 𝑛 = 2.
In the lighter elements the electrons fill up subshells within each shell in the
order s, p, d, etc., and no shell acquires electrons until the lower shells are
full. In the heavier elements this rule does not always hold. But if a particular subshell is filled in a noble gas, then the same subshell is filled in the
atoms of all elements that come later in the periodic table. The ground state
configurations of the noble gases are as follows:
He
Ne
Ar
Kr
Xe
Rn

1s2
1s2 2s2 2p6
1s2 2s2 2p6 3s2 3p6
1s2 2s2 2p6 3s2 3p6 3d10 4s2 4p6
1s2 2s2 2p6 3s2 3p6 3d10 4s2 4p6 4d10 5s2 5p6
1s2 2s2 2p6 3s2 3p6 3d10 4s2 4p6 4d10 4f 14 5s2 5p6 5d10 6s2 6p6

Alkali metals (Li, Na, K, etc.) resemble hydrogen; their transitions are described by giving 𝑛 and 𝑙 in the initial and final states for the single outer (valence) electron.
For general transitions in most atoms the atomic states are specified in terms
of the parity (−1)Σ𝑙𝑖 and the magnitudes of the orbital angular momentum
𝐋 = Σ𝐥𝑖 , the spin 𝐒 = Σ𝐬𝑖 , and the total angular momentum 𝐉 = 𝐋 + 𝐒,
where all sums are carried out over the unfilled subshells (the filled ones
sum to zero). If a magnetic field is present the projections 𝑀𝐿 , 𝑀𝑆 , and 𝑀
of 𝐋, 𝐒, and 𝐉 along the field are also needed. The quantum numbers satisfy
|𝑀𝐿 | ≤ 𝐿 ≤ 𝜈𝑙, |𝑀𝑆 | ≤ 𝑆 ≤ 𝜈/2, and |𝑀| ≤ 𝐽 ≤ 𝐿 + 𝑆, where 𝜈 is the number
of electrons in the unfilled subshell. Upper-case letters S, P, D, etc., stand for
𝐿 = 0, 1, 2, etc., in analogy with the notation for a single electron. For examo
ple, the ground state of Cl is described by 3p5 2 P3/2
. The first part indicates
that there are 5 electrons in the subshell corresponding to 𝑛 = 3 and 𝑙 = 1.
(The closed inner subshells 1s2 2s2 2p6 3s2 , identical with the configuration of
Mg, are usually omitted.) The symbol ‘P’ indicates that the angular momenta
of the outer electrons combine to give 𝐿 = 1. The prefix ‘2’ represents the
value of the multiplicity 2𝑆 + 1 (the number of states with nearly the same
energy), which is equivalent to specifying 𝑆 = 12 . The subscript 3/2 is the
60

## PDF page 61

value of 𝐽. The superscript ‘o’ indicates that the state has odd parity; it would
be omitted if the state were even.
The notation for excited states is similar. For example, helium has a state
1s2s 3 S1 which lies 19.72 eV (159,856 cm−1 ) above the ground state 1s2 1 S0 .
But the two “terms” do not “combine” (transitions between them do not occur) because this would violate, e.g., the quantum-mechanical selection rule
that the parity must change from odd to even or from even to odd. For electric dipole transitions (the only ones possible in the long-wavelength limit),
other selection rules are that the value of 𝑙 of only one electron can change,
and only by Δ𝑙 = ±1; Δ𝑆 = 0; Δ𝐿 = ±1 or 0; and Δ𝐽 = ±1 or 0 (but 𝐿 = 0
does not combine with 𝐿 = 0 and 𝐽 = 0 does not combine with 𝐽 = 0). Transitions are possible between the helium ground state (which has 𝑆 = 0, 𝐿 = 0,
𝐽 = 0, and even parity) and, e.g., the state 1s2p 1 Po1 (with 𝑆 = 0, 𝐿 = 1, 𝐽 = 1,
odd parity, excitation energy 21.22 eV). These rules hold accurately only for
light atoms in the absence of strong electric or magnetic fields. Transitions
that obey the selection rules are called “allowed”; those that do not are called
“forbidden.”
The amount of information needed to adequately characterize a state increases with the number of electrons; this is reflected in the notation. Thus43
′
O II has an allowed transition between the states 2p2 3p′ 2 Fo7/2 and 2p2 (1 D)3d
2
F7/2 (and between the states obtained by changing 𝐽 from 7/2 to 5/2 in either or both terms). Here both states have two electrons with 𝑛 = 2 and 𝑙 = 1;
the closed subshells 1s2 2s2 are not shown. The outer (𝑛 = 3) electron has
𝑙 = 1 in the first state and 𝑙 = 2 in the second. The prime indicates that if
the outermost electron were removed by ionization, the resulting ion would
not be in its lowest energy state. The expression (1 D) gives the multiplicity
and total angular momentum of the “parent” term, i.e., the subshell immediately below the valence subshell; this is understood to be the same in both
states. (Grandparents, etc., sometimes have to be specified in heavier atoms
o
and ions.) Another example43 is the allowed transition from 2p2 (3 P)3p 2 P1/2
o
) to 2p2 (1 D)3d′ 2 S1/2 , in which there is a “spin flip” (from antiparallel
(or 2 P3/2
to parallel) in the 𝑛 = 2, 𝑙 = 1 subshell, as well as changes from one state to
the other in the value of 𝑙 for the valence electron and in 𝐿.
The description of fine structure, Stark and Zeeman effects, spectra of highly
ionized or heavy atoms, etc., is more complicated. The most important difference between optical and X-ray spectra is that the latter involve energy
changes of the inner electrons rather than the outer ones; often several electrons participate.

61

## PDF page 62

COMPLEX (DUSTY) PLASMAS
Complex (dusty) plasmas (CDPs) contain charged microparticles (dust grains)
in addition to electrons, ions, and neutral gas. Electrostatic coupling between
the grains can vary over a wide range, so that the states of CDPs can change
from weakly coupled (gaseous) to crystalline.
Typical experimental dust properties
grain size (radius) 𝑎 ≃ 0.3 − 30 μm, mass 𝑚𝑑 ∼ 3 × 10−7 − 3 × 10−13 g, number
density (in terms of the interparticle distance) 𝑛𝑑 ∼ Δ−3 ∼ 103 − 107 cm−3 ,
temperature 𝑇𝑑 ∼ 3 × 10−2 − 102 eV.
Typical discharge (bulk) plasmas
gas pressure 𝑝 ∼ 10−2 − 1 Torr, 𝑇𝑖 ≃ 𝑇𝑛 ≃ 3 × 10−2 eV, 𝑣𝑇𝑖 ≃ 7 × 104 cm/s
(Ar), 𝑇𝑒 ∼ 0.3 − 3 eV, 𝑛𝑖 ≃ 𝑛𝑒 ∼ 108 − 1010 cm−3 , screening length 𝜆𝐷 ≃ 𝜆𝐷𝑖 ∼
20 − 200 μm, 𝜔𝑝𝑖 ≃ 2 × 106 − 2 × 107 s−1 (Ar). B fields up to 𝐵 ∼ 3 T.
Dimensionless
Havnes parameter
normalized charge
dust-dust scattering parameter
dust-plasma scattering parameter
coupling parameter
lattice parameter
particle parameter
lattice magnetization parameter

𝑃 = |𝑍|𝑛𝑑 /𝑛𝑒
𝑧 = |𝑍|𝑒2 /𝑘𝑇𝑒 𝑎
𝛽𝑑 = 𝑍 2 𝑒2 /𝑘𝑇𝑑 𝜆𝐷
𝛽𝑒,𝑖 = |𝑍|𝑒2 /𝑘𝑇𝑒,𝑖 𝜆𝐷
Γ = (𝑍 2 𝑒2 /𝑘𝑇𝑑 Δ) exp(−Δ/𝜆𝐷 )
𝜅 = Δ/𝜆𝐷
𝛼 = 𝑎/Δ
𝜇 = Δ/𝑟𝑑

Typical experimental values: 𝑃 ∼ 10−4 −102 , 𝑧 ≃ 2−4 (𝑍 ∼ 103 −105 electron
charges), Γ < 103 , 𝜅 ∼ 0.3 − 10, 𝛼 ∼ 10−4 − 3 × 10−2 , 𝜇 < 1
Frequencies
dust plasma frequency

𝜔𝑝𝑑 = (4𝜋𝑍 2 𝑒2 𝑛𝑑 /𝑚𝑑 )1/2
≃ (|𝑍|
1+𝑧

𝑃
1+𝑃

𝑚𝑖 /𝑚𝑑 )1/2 𝜔𝑝𝑖

charge fluctuation frequency

𝜔ch ≃

dust-gas friction rate
dust gyrofrequency

𝜈𝑛𝑑 ∼ 10𝑎2 𝑝/𝑚𝑑 𝑣𝑇𝑛
𝜔𝑐𝑑 = 𝑍𝑒𝐵/𝑚𝑑 𝑐

√2𝜋

(𝑎/𝜆𝐷 )𝜔𝑝𝑖

Velocities
dust thermal velocity
62

𝑇

𝑣𝑇𝑑 = (𝑘𝑇𝑑 /𝑚𝑑 )1/2 ≡ [ 𝑑

𝑚𝑖

𝑇𝑖 𝑚𝑑

1/2

]

𝑣𝑇𝑖

## PDF page 63

dust acoustic wave velocity

𝐶DA = 𝜔𝑝𝑑 𝜆𝐷
≃ (|𝑍|

𝑃
1+𝑃

1/2

𝑚𝑖 /𝑚𝑑 )

𝑣𝑇𝑖

1/2

dust Alfvén wave velocity
dust-acoustic Mach number
dust magnetic Mach number

𝑣𝐴𝑑 = 𝐵/(4𝜋𝑛𝑑 𝑚𝑑 )
𝑉/𝐶DA
𝑉/𝑣𝐴𝑑

dust lattice (acoustic) wave velocity

𝑙,𝑡
𝐶DL
= 𝜔𝑝𝑑 𝜆𝐷 𝐹𝑙,𝑡 (𝜅)

The range of the dust-lattice wavenumbers is KΔ < 𝜋. The functions 𝐹𝑙,𝑡 (𝜅)
for longitudinal and transverse waves can be approximated44,45 with accuracy < 1% in the range 𝜅 ≤ 5:
𝐹𝑙 ≃ 2.70𝜅1/2 (1 − 0.096𝜅 − 0.004𝜅2 ),

𝐹𝑡 ≃ 0.51𝜅(1 − 0.039𝜅2 ),

Lengths
frictional dissipation length
dust Coulomb radius
dust gyroradius

𝐿𝜈 = 𝑣𝑇𝑑 /𝜈𝑛𝑑
𝑅𝐶𝑒,𝑖 = |𝑍|𝑒2 /𝑘𝑇𝑒,𝑖
𝑟𝑑 = 𝑣𝑇𝑑 /𝜔𝑐𝑑

Grain Charging
The charge evolution equation is 𝑑|𝑍|/𝑑𝑡 = 𝐼𝑖 − 𝐼𝑒 . From orbital motion
limited (OML) theory46 in the collisionless limit 𝑙𝑒𝑛(𝑖𝑛) ≫ 𝜆𝐷 ≫ 𝑎:
𝑇𝑒
𝑧) .
𝑇𝑖
Grains are charged negatively. The grain charge can vary in response to spatial and temporal variations of the plasma. Charge fluctuations are always
present, with frequency 𝜔ch . Other charging mechanisms are photoemission,
secondary emission, thermionic emission, field emission, etc. Charged dust
grains change the plasma composition, keeping quasineutrality. A measure
of this is the Havnes parameter 𝑃 = |𝑍|𝑛𝑑 /𝑛𝑒 . The balance of 𝐼𝑒 and 𝐼𝑖 yields
𝐼𝑒 = √8𝜋𝑎2 𝑛𝑒 𝑣𝑇𝑒 exp(−𝑧),

𝐼𝑖 = √8𝜋𝑎2 𝑛𝑖 𝑣𝑇𝑖 (1 +

1/2

𝑇
𝑚𝑖 𝑇𝑖
) (1 + 𝑒 𝑧) [1 + 𝑃(𝑧)]
𝑚𝑒 𝑇𝑒
𝑇𝑖
When the relative charge density of dust is large, 𝑃 ≫ 1, the grain charge Z
monotonically decreases.
exp(−𝑧) = (

Forces and momentum transfer
In addition to the usual electromagnetic forces, grains in complex plasmas
63

## PDF page 64

are also subject to: gravity force 𝐅g = 𝑚𝑑 𝐠; thermophoretic force
4√2𝜋 2
(𝑎 /𝑣𝑇𝑛 )𝜅𝑛 ∇𝑇𝑛
15
(where 𝜅𝑛 is the coefficient of gas thermal conductivity); forces associated
with the momentum transfer from other species, 𝐅𝛼 = −𝑚𝑑 𝜈𝛼𝑑 𝐕𝛼𝑑 , i.e., neutral, ion, and electron drag. For collisions between charged particles, two
limiting cases are distinguished by the magnitude of the scattering parameter 𝛽𝛼 . When 𝛽𝛼 ≪ 1 the result is independent of the sign of the potential.
When 𝛽𝛼 ≫ 1, the results for repulsive and attractive interaction potentials
are different. For typical complex plasmas the hierarchy of scattering parameters is 𝛽𝑒 (∼ 0.01 − 0.3) ≪ 𝛽𝑖 (∼ 1 − 30) ≪ 𝛽𝑑 (∼ 103 − 3 × 104 ). The generic
expressions for different types of collisions are47
𝐅th = −

𝜈𝛼𝑑 = (4√2𝜋/3)(𝑚𝛼 /𝑚𝑑 )𝑎2 𝑛𝛼 𝑣𝑇𝛼 Φ𝛼𝑑
Electron-dust collisions
1
Φ𝑒𝑑 ≃ 𝑧2 Λ𝑒𝑑 ,
2

𝛽𝑒 ≪ 1

Ion-dust collisions
1

𝑧2 (𝑇𝑒 /𝑇𝑖 )2 Λ𝑖𝑑 ,
Φ𝑖𝑑 = { 2
2
2(𝜆𝐷 /𝑎)2 (ln 𝛽𝑖 + 2 ln 𝛽𝑖 + 2),

𝛽𝑖 < 5
𝛽𝑖 > 13

Dust-dust collisons
𝑧2 Λ ,
𝛽𝑑 ≪ 1
Φ𝑑𝑑 = { 𝑑 𝑑𝑑 2
(𝜆𝐷 /𝑎) [ln 4𝛽𝑑 − ln ln 4𝛽𝑑 ], 𝛽𝑑 ≫ 1
where 𝑧𝑑 ≡ 𝑍 2 𝑒2 /𝑎𝑘𝑇𝑑 .
For 𝜈𝑑𝑑 ∼ 𝜈𝑛𝑑 the complex plasma is in a two-phase state, and for 𝜈𝑛𝑑 ≫ 𝜈𝑑𝑑
we have merely tracer particles (dust-neutral gas interaction dominates). The
momentum transfer cross section is proportional to the Coulomb logarithm
Λ𝛼𝑑 when the Coulomb scattering theory is applicable. It is determined by
integration over the impact parameters, from 𝜌min to 𝜌max . 𝜌min is due to finite grain size and is given by OML theory. 𝜌max = 𝜆𝐷 for repulsive interaction (applicable for 𝛽𝛼 ≪ 1), and 𝜌max = 𝜆𝐷 (1 + 2𝛽𝛼 )1/2 for attractive
interaction (applicable up to 𝛽𝛼 < 5).

64

## PDF page 65

For repulsive interaction (electron-dust and dust-dust)
∞

Λ𝛼𝑑 = 𝑧𝛼 ∫ e−𝑧𝛼 𝑥 ln[1 + 4(𝜆𝐷 /𝑎𝛼 )2 𝑥2 ]𝑑𝑥

∞

0

− 2𝑧𝛼 ∫ e−𝑧𝛼 𝑥 ln(2𝑥 − 1)𝑑𝑥,
1

where 𝑧𝑒 = 𝑧, 𝑎𝑒 = 𝑎, and 𝑎𝑑 = 2𝑎.
For ion-dust (attraction)
∞

Λ𝑖𝑑 ≃ 𝑧 ∫ e−𝑧𝑥 ln [
0

1 + 2(𝑇𝑖 /𝑇𝑒 )(𝜆𝐷 /𝑎)𝑥
] 𝑑𝑥.
1 + 2(𝑇𝑖 /𝑇𝑒 )𝑥

For 𝜈𝑑𝑑 ≫ 𝜈𝑛𝑑 the complex plasma behaves like a one phase system (dustdust interaction dominates).
Phase Diagram of Complex Plasmas
The figure below represents different “phase states” of CDPs as functions of
the electrostatic coupling parameter Γ and 𝜅 or 𝛼, respectively. The vertical
dashed line at 𝜅 = 1 conditionally divides the system into Coulomb and
Yukawa parts. With respect to the usual plasma phase, in the diagram below the complex plasmas are “located” mostly in the strong coupling regime
(equivalent to the top left corner).
α-1=Δ/a
4

10

100

1000

I

V

log10(Γ)

2

II

0

VI
III

−2

VII

IV
−4

0.1

1

κ=Δ/λ

VIII
10

Regions I (V) represent Coulomb
(Yukawa) crystals, the crystallization
condition is48 Γ > 106(1 + 𝜅 + 𝜅2 /2)−1 .
Regions II (VI) are for Coulomb
(Yukawa) non-ideal plasmas – the characteristic range of dust-dust interaction
(in terms of the momentum transfer)
is larger than the intergrain distance
(in terms of the Wigner-Seitz radius),
(𝜎/𝜋)1/2 > (4𝜋/3)−1/3 Δ, which implies
that the interaction is essentially multiparticle.

Regions III (VII and VIII) correspond to Coulomb (Yukawa) ideal gases. The
range of dust-dust interaction is smaller than the intergrain distance and
only pair collisions are important. In addition, in the region VIII the pair
Yukawa interaction asymptotically reduces to the hard sphere limit, forming
a “Yukawa granular medium”. In region IV the electrostatic interaction is
unimportant and the system is like a usual granular medium.
65

## PDF page 66

REFERENCES
When any of the formulas and data in this collection are referenced in research publications, it is suggested that the original source be cited rather
than the Formulary. Most of this material is well known and, for all practical
purposes, is in the “public domain.” Numerous colleagues and readers, too
numerous to list by name, have helped in collecting and shaping the Formulary into its present form; they are sincerely thanked for their efforts.
Several book-length compilations of data relevant to plasma physics are available. The following are particularly useful:
• C. W. Allen, Astrophysical Quantities, 3rd edition (Athlone Press, London,
1976).
• A. Anders, A Formulary for Plasma Physics (Akademie-Verlag, Berlin,
1990).
• H. L. Anderson (Ed.), A Physicist’s Desk Reference, 2nd edition (American
Institute of Physics, New York, 1989).
• K. R. Lang, Astrophysical Formulae, 2nd edition (Springer, New York, 1980).
The books and articles cited below are intended primarily not for the purpose of giving credit to the original workers, but (1) to guide the reader to
sources containing related material and (2) to indicate where to find derivations, explanations, examples, etc., which have been omitted from this compilation. Additional material can also be found in D. L. Book, NRL Memorandum Report No. 3332 (1977).
1. See M. Abramowitz and I. A. Stegun, Eds., Handbook of Mathematical
Functions (Dover, New York, 1968), pp. 1–3, for a tabulation of some
mathematical constants not available on pocket calculators.
2. H. W. Gould, “Note on Some Binomial Coefficient Identities of Rosenbaum,” J. Math. Phys. 10, 49 (1969); H. W. Gould and J. Kaucky, “Evaluation of a Class of Binomial Coefficient Summations,” J. Comb. Theory
1, 233 (1966).
3. B. S. Newberger, “New Sum Rule for Products of Bessel Functions with
Application to Plasma Physics,” J. Math. Phys. 23, 1278 (1982); 24, 2250
(1983).
4. P. M. Morse and H. Feshbach, Methods of Theoretical Physics (McGraw-Hill
66

## PDF page 67

Book Co., New York, 1953), Vol. I, pp. 47–52 and pp. 656–666.
5. W. D. Hayes, “A Collection of Vector Formulas,” Princeton University,
Princeton, NJ, 1956 (unpublished), and personal communication (1977).
6. See Quantities, Units and Symbols, report of the Symbols Committee of the
Royal Society, 2nd edition (Royal Society, London, 1975) for a discussion
of nomenclature in SI units.
7. E. R. Cohen and B. N. Taylor, “The 1986 Adjustment of the Fundamental
Physical Constants,” CODATA Bulletin No. 63 (Pergamon Press, New
York, 1986); J. Res. Natl. Bur. Stand. 92, 85 (1987); J. Phys. Chem. Ref.
Data 17, 1795 (1988).
8. E. S. Weibel, “Dimensionally Correct Transformations between Different
Systems of Units,” Amer. J. Phys. 36, 1130 (1968).
9. J. Stratton, Electromagnetic Theory (McGraw-Hill Book Co., New York,
1941), p. 508.
10. Reference Data for Engineers: Radio, Electronics, Computer, and Communication, 7th edition, E. C. Jordan, Ed. (Sams and Co., Indianapolis, IN,
1985), Chapt. 1. These definitions are International Telecommunications Union (ITU) Standards.
11. H. E. Thomas, Handbook of Microwave Techniques and Equipment (Prentice-Hall, Englewood Cliffs, NJ, 1972), p. 9. Further subdivisions are
defined in Ref. 10, p. I–3.
12. J. P. Catchpole and G. Fulford, Ind. and Eng. Chem. 58, 47 (1966); reprinted
in recent editions of the Handbook of Chemistry and Physics (Chemical
Rubber Co., Cleveland, OH) on pp. F306–323.
13. W. D. Hayes, “The Basic Theory of Gasdynamic Discontinuities,” in Fundamentals of Gas Dynamics, Vol. III, High Speed Aerodynamics and Jet
Propulsion, H. W. Emmons, Ed. (Princeton University Press, Princeton,
NJ, 1958).
14. W. B. Thompson, An Introduction to Plasma Physics (Addison-Wesley
Publishing Co., Reading, MA, 1962), pp. 86–95.
15. L. D. Landau and E. M. Lifshitz, Fluid Mechanics, 2nd edition (AddisonWesley Publishing Co., Reading, MA, 1987), pp. 320–336.
16. The 𝑍 function is tabulated in B. D. Fried and S. D. Conte, The Plasma
67

## PDF page 68

Dispersion Function (Academic Press, New York, 1961).
17. R. W. Landau and S. Cuperman, “Stability of Anisotropic Plasmas to
Almost-Perpendicular Magnetosonic Waves,” J. Plasma Phys. 6, 495
(1971).
18. B. D. Fried, C. L. Hedrick, J. McCune, “Two-Pole Approximation for the
Plasma Dispersion Function,” Phys. Fluids 11, 249 (1968).
19. B. A. Trubnikov, “Particle Interactions in a Fully Ionized Plasma,” Reviews
of Plasma Physics, Vol. 1 (Consultants Bureau, New York, 1965), p. 105.
20. J. M. Greene, “Improved Bhatnagar–Gross–Krook Model of Electron-Ion
Collisions,” Phys. Fluids 16, 2022 (1973).
21. (a) S. I. Braginskii, “Transport Processes in a Plasma,” Reviews of Plasma
Physics, Vol. 1 (Consultants Bureau, New York, 1965), p. 205. (b) R. Balescu,
“Transport Processes in Plasma,” (North Holland Publishing, Amsterdam, 1988), p. 211.
22. J. Sheffield, Plasma Scattering of Electromagnetic Radiation (Academic
Press, New York, 1975), p. 6 (after J. W. M. Paul).
23. K. H. Lloyd and G. Härendel, “Numerical Modeling of the Drift and Deformation of Ionospheric Plasma Clouds and of their Interaction with
Other Layers of the Ionosphere,” J. Geophys. Res. 78, 7389 (1973).
24. C. W. Allen, Astrophysical Quantities, 3rd edition (Athlone Press, London,
1976), Chapt. 9.
25. G. L. Withbroe and R. W. Noyes, “Mass and Energy Flow in the Solar
Chromosphere and Corona,” Ann. Rev. Astrophys. 15, 363 (1977).
26. S. Glasstone and R. H. Lovberg, Controlled Thermonuclear Reactions (Van
Nostrand, New York, 1960), Chapt. 2.
27. References to experimental measurements of branching ratios and cross
sections are listed in F. K. McGowan, et al., Nucl. Data Tables A6, 353
(1969); A8, 199 (1970). The yields listed in the table are calculated directly from the mass defect.
28. (a) G. H. Miley, H. Towner and N. Ivich, Fusion Cross Section and Reactivities, Rept. COO-2218-17 (University of Illinois, Urbana, IL, 1974);
B. H. Duane, Fusion Cross Section Theory, in Rept. BNWL-1685 (Battelle
Pacific Northwest Laboratory, 1972); (b) X.Z. Li, Q.M. Wei, and B. Liu,
68

## PDF page 69

“A new simple formula for fusion cross-sections of light nuclei,” Nucl.
Fusion 48, 125003 (2008).
29. J. M. Creedon, “Relativistic Brillouin Flow in the High 𝜈/𝛾 Limit,” J. Appl.
Phys. 46, 2946 (1975).
30. See, for example, A. B. Mikhailovskii, Theory of Plasma Instabilities Vol. I
(Consultants Bureau, New York, 1974). The table on pp. 48–49 was compiled by K. Papadopoulos.
31. Table prepared from data compiled by J. M. McMahon (personal communication, D. Book, 1990) and A. Ting (personal communication, J.D.
Huba, 2004).
32. M. J. Seaton, “The Theory of Excitation and Ionization by Electron Impact,” in Atomic and Molecular Processes, D. R. Bates, Ed. (New York,
Academic Press, 1962), Chapt. 11.
33. H. Van Regemorter, “Rate of Collisional Excitation in Stellar Atmospheres,”
Astrophys. J. 136, 906 (1962).
34. A. C. Kolb and R. W. P. McWhirter, “Ionization Rates and Power Loss
from 𝜃-Pinches by Impurity Radiation,” Phys. Fluids 7, 519 (1964).
35. R. W. P. McWhirter, “Spectral Intensities,” in Plasma Diagnostic Techniques, R. H. Huddlestone and S. L. Leonard, Eds. (Academic Press,
New York, 1965).
36. M. Gryzinski, “Classical Theory of Atomic Collisions I. Theory of Inelastic Collision,” Phys. Rev. 138A, 336 (1965).
37. M. J. Seaton, “Radiative Recombination of Hydrogenic Ions,” Mon. Not.
Roy. Astron. Soc. 119, 81 (1959).
38. Ya. B. Zel’dovich and Yu. P. Raizer, Physics of Shock Waves and HighTemperature Hydrodynamic Phenomena (Academic Press, New York,
1966), Vol. I, p. 407.
39. H. R. Griem, Plasma Spectroscopy (Academic Press, New York, 1966).
40. T. F. Stratton, “X-Ray Spectroscopy,” in Plasma Diagnostic Techniques,
R. H. Huddlestone and S. L. Leonard, Eds. (Academic Press, New York,
1965).
41. G. Bekefi, Radiation Processes in Plasmas (Wiley, New York, 1966).
42. T. W. Johnston and J. M. Dawson, “Correct Values for High-Frequency
69

## PDF page 70

Power Absorption by Inverse Bremsstrahlung in Plasmas,” Phys. Fluids
16, 722 (1973).
43. W. L. Wiese, M. W. Smith, and B. M. Glennon, Atomic Transition Probabilities, NSRDS-NBS 4, Vol. 1 (U.S. Govt. Printing Office, Washington,
1966).
44. F. M. Peeters and X. Wu, “Wigner crystal of a screened-Coulomb-interaction
colloidal system in two dimensions”, Phys. Rev. A 35, 3109 (1987)
45. S. Zhdanov, R. A. Quinn, D. Samsonov, and G. E. Morfill, “Large-scale
steady-state structure of a 2D plasma crystal”, New J. Phys. 5, 74 (2003).
46. J. E. Allen, “Probe theory – the orbital motion approach”, Phys. Scripta
45, 497 (1992).
47. S. A. Khrapak, A. V. Ivlev, and G. E. Morfill, “Momentum transfer in
complex plasmas”, Phys. Rev. E (2004).
48. V. E. Fortov et al., “Dusty plasmas”, Phys. Usp. 47, 447 (2004).

70

## PDF page 71

<b>NOTES</b>
71

## PDF page 72

For information about careers in plasma physics at the US Naval Research
Laboratory, contact us at: PlasmaPhysicsCareers@nrl.navy.mil
The NRL Plasma Formulary is available in PDF format online at
https://www.nrl.navy.mil/ppd/content/nrl-plasma-formulary
Any questions, suggestions, comments, etc. can be directed to:
Plasma.Formulary@nrl.navy.mil
This document was typeset using XELATEX. The text and mathematics are set
using the STIX Two fonts, which were created by the Scientific and Technical
Information Exchange (STIX) font creation project. The headings are set in
Frutiger Neue LT Pro, and the monospace text in Inconsolata. The character
for the partial derivative, ∂, is from Charis SIL.

Reviewed and Approved
NRL/PU/6770--19-652
RN: 19-1231-3251
September 2019

72

Thomas A. Mehlhorn
Superintendent
Plasma Physics Division
