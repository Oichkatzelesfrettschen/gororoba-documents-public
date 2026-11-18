Source: see manifest row of the PDF
PDF sha256: f5ee636c06fab4c06aad5a82c678dedc8cbd1ad953d59a5963a51719cc8e988a
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of wu_2022_complex_berry_curvature_and_complex_energy_band_structures_in_non_hermitian_graphene_model.pdf

Transcription of `wu_2022_complex_berry_curvature_and_complex_energy_band_structures_in_non_hermitian_graphene_model.pdf` in this directory, 10 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-10 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

(2022) 32:39
Wu et al. AAPPS Bulletin
https://doi.org/10.1007/s43673-022-00065-0

ORIGINAL ARTICLE

AAPPS Bulletin

Open Access

Complex Berry curvature and complex
energy band structures in non‑Hermitian
graphene model
Chao Wu1,2†, Annan Fan1† and Shi‑Dong Liang1,3,4*†   

Abstract
Non-Hermitian quantum systems exhibit many novel physical properties of quantum states. We consider a non-Her‑
mtian graphene model based on the tight-binding approximation with the coupling of the graphene and the sub‑
strate. We analyze the complex energy structure of this model and its exceptional points as well as relevant topologi‑
cal invariants. We give the analytic complex Berry connection and Berry curvature in the Brillouin zone and investigate
numerically the relationships between the complex Berry curvature and the complex energy band structures. We find
that the behaviors of the complex Berry curvature depend on the complex energy band structures. The occurrence of
the peaks of both real and imaginary parts of the complex Berry curvature corresponds to the exceptional (gapless)
points in the Brillouin zone. In particular, the Dirac cone of the imaginary part of the Berry curvature occurs and corre‑
sponding to the occurrence of the flat real energy band for the non-Hermitian parameter η = 3. These results provide
some novel insights to the relationship between the non-Hermitian graphene, geometry, and topological invariants.
Keywords: Berry curvature, Non-Hermiticity, Graphene
1 Introduction
The geometric and topological methods provide new
insights to quantum systems in condensed matter physics [1–4]. It has been found that the quantum Hall and
spin Hall effects can be understood in terms of the topological states identified by the Chern classes, Z and Z2
[5–8]. These discoveries have attracted many attempts
to explore the topological phases in condensed matter
systems based on the symmetry group and homological
invariants [7, 8]. The concepts of the Berry connection
and curvature in quantum systems provide a geometric
approach to understand quantum states and their evolutions [9, 10]. The winding number and Chern number are identified the topological phases and their phase
†

Chao Wu, Annan Fan and Shi-Dong Liang contributed equally to this work.

*Correspondence: stslsd@mail.sysu.edu.cn
4

Guangdong Province Key Laboratory of Display Material and Technology,
Sun Yat-Sen University, Guangzhou 510275, China
Full list of author information is available at the end of the article

transitions [4]. Recently, these concepts ware generalized to non-Hermitian quantum systems and its holonomy interpretation [11–14]. One found that the complex
energy band structures of non-Hermitian systems show
rich physics beyond Hermitian systems. Especially the
complex band gaps and their corresponding exceptional
points associate with topological phases [13]. The complex Berry phase for non-Hermitian systems has been
proposed and applied to study the behaviors near the
exceptional point [15–17], dissipative behaviors [18, 19],
and quantum phase transition [20, 21]. In particular, the
Berry phase are generalized to the global Berry phase,
which play a role of the winding number to identify the
topological invariants in the non-Hermitian quantum
walk and dissipative bipartite lattice [21–23]. The robust
topological states promise potential applications in quantum materials and technologies [24–26].
Quantum non-Hermitian systems exhibit unconventional characteristics and potential applications [11,
24, 27–30]. In particular, non-Hermiticity of systems

© The Author(s) 2022. Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which
permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit to the
original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes were made. The images or
other third party material in this article are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line
to the material. If material is not included in the article’s Creative Commons licence and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this
licence, visit http://​creat​iveco​mmons.​org/​licen​ses/​by/4.​0/.

## PDF page 2

Wu et al. AAPPS Bulletin

(2022) 32:39

describes some dissipative phenomena, such as energy
gain or loss and non-conserved probability of electrons
appearing [31–33]. These unconventional characteristics
beyond standard quantum mechanics yield many novel
phenomena in quantum states, such as the 10-fold topological equivalent classes in Hermitian systems based on
the Altland-Zirnbauer (AZ) symmetry classification are
extended to the 38-fold topological equivalent classes due
to the additional sublattice symmetry and pseudo-Hermticity in non-Hermitian systems [12, 13]. One found that
the complex energy band gap could form a point or line
gap to preserves its topological invariants under a unitary
or Hermitian flattening transformation [13]. The energy
band gaps close to form the exceptional points and lines
as the reference points or lines associated with the topological phases [12, 13]. Moreover, the non-Hermiticity
of systems deforms the Bloch-wave behavior to yield the
skin effect for lattice models [34–37]. One introduced
the biorthogonal polarization to modify the conventional
bulk-boundary correspondence to show the zero modes
[38–40], the topological edge states, and the finite-size
effects in the non-Hermitian Su-Schrieffer-Heeger (SSH)
model [41–45]. In particular, Chen and Zhai studied the
Hall conductance of a non-Hermitian Chern insulator
and found some deviations of the quantized Chern number and the quantum Hall conductance [44–46].
In particular, one found that all eigen energies of the
non-Hermitian systems are still real if the systems have
PT (Parity-Time reversal) symmetries or pseudo-Hermitian symmetry [31, 32]. The quantum evolution driven
by non-Hermitian Hamiltonian with the PT symmetry is
faster than those driven by Hermitian Hamiltonian [47,
48], which provides a novel insight to quantum computation. Moreover, the time reversal symmetry and its relevant topological invariants have been studied extensively
and applied in electromagnetism, compact star matter
and quantum computation [49–53].
More interestingly, the quantum Hall conductance
in the Dirac model can be generalized to quantum Hall
admittance in the non-Hermitian Dirac model. Namely
the quantum Hall susceptance emerges, such as quantum Hall capacity and induction [54]. This inspires fundamental insights into non-Hermitian systems and lead
to potential applications [54]. One found that the edge
states in the complex energy band play an important role
in the topological invariants and the topological phase
transition in the non-Hermitian systems [55]. These topological invariants are associated with the velocity field of
the Bloch electrons in the Brillouin zone and connected
to the Euler index [56].
On the other hand, as a typical two-dimensional (2D)
system, graphene promises great potential applications in nanoelectronics and nanotechnology [57, 58].

Page 2 of 10

Its honeycomb lattice structure yields the Dirac cone in
its energy band structure. Graphene provides a practical
system to explore the geometric and topological properties of the Dirac model in condensed matter systems [59].
However, most of the previous theoretical works focus on
the Hermitian graphene model [59–61]. When we consider that the graphene is on a substrate in some practical
applications, there should be exist coupling between the
graphene and the substrate, which may induce the dissipative effect due to asymmetric carbons in the hexagon
lattice. Thus, these dissipative effects in the graphene may
be modeled by a non-Hermitian graphene model.
In this paper, we study the geometric and topological
features of the non-Hermitian graphene model. Firstly,
we propose a non-Hermitian Hamiltonian of graphene
based on the tight-binding approximation in the Section 2. The dissipative effects come from the coupling
of the graphene with the substrate. In Section 3, we
analyze the symmetry of this model and its relationship
with the exceptional point and topological invariants. In
Sections 4 and 5, we give analytically the complex Berry
connection and the complex Berry curvature of this nonHermitian graphene model. Then in Section 6, we investigate numerically the relationship between the complex
Berry curvature and the complex energy band structure.
Finally, we give the conclusions and outlook in Section 7.

2 Non‑Hermitian graphene model
Let us consider a honeycomb lattice, where there are two
kinds of atoms, A and B shown in Fig. 1. The graphene can
be modeled by the tight-binding approach with the equal

Fig. 1 (Color online): The honeycomb lattice, where A and B label
two different sites of the graphene

## PDF page 3

Wu et al. AAPPS Bulletin

(2022) 32:39

Page 3 of 10

on-site energies of A and B atoms. When the graphene
couples the substrate, in which A and B atoms will gain or
loss energy asymmetrically such that graphene becomes
a dissipative system. This dissipative mechanism can be
modeled by a non-Hermitian graphene model. Its Hamiltonian can be expressed as [57, 58]
∑
∑
H=
ǫA a†i ai + ǫB bi† bi − t
(a†i bj + h.c.),
(1)
i

�i,j�

where ǫA is the on-site energy of A sites, while
ǫB = ǫA − i2Ŵ is the on-site energy of B sites, and the
imaginary part describes the dissipation. When Ŵ = 0,
the Hamiltonian H reduces to the Hermitian graphene
Hamiltonian. Using Fourier transformation, we can
rewrite the Hamiltonian in the reciprocal space,
∑
H=
k† hk k
(2)
k

where k† = a†k , bk† and
)
(
ǫA − tfk
hk =
−tfk∗ ǫB
is the Hamiltonian in the reciprocal space with
(√
)
3ky a −i kx a
ikx a
fk = e
+ 2 cos
e 2
2

(3)

(4)

with a being the lattice constant of the graphene. We set
ℏ = 1 and a = 1 for convenience in the following sections. By solving the eigenequation, we can obtain the
eigenvalues
√
(5)
Ek,± = ǫA − iŴ ± t | fk |2 −η2 .

where η = Ŵt . The corresponding eigenvectors are
( −iθ
)
( −iθ
)
e k cos φ2k
−e k sin φ2k
| ψ+ � =
,
; | ψ− � =
sin φ2k
cos φ2k
(6)
and their dual eigenvectors in the dual space are
( −iθ
)
)
( −iθ
e k cos∗ φ2k
−e k sin∗ φ2k
| ψ̃+ � =
,
;
|
ψ̃
�
=
−
cos∗ φ2k
sin∗ φ2k
(7)
where cos and sin are complex functions and * means
the complex conjugated operator. We define

tan φk :=

| fk |
,
iη

(8a)

e−iθk := −

fk
.
| fk |

(8b)

It should be pointed out that studying the non-Hermitian graphene model will turn out the two-fold physical
meanings. (1) Graphene shows many interesting properties and potential applications due to its hexagonal lattice structure. When we design a quantum device based
on the graphene, the A and B atoms in graphene couple
asymmetrically to substrate which gain or lose different
energy such that the graphene becomes a non-Hermitian
systems. To understand this non-Hermitian graphene
model will help us to further design quantum devices
based on the graphene with the dissipative phenomena
[57, 58]. (2) The non-Hermitian graphene model can be
reduced to the non-Hermitian Dirac model in the low
energy domain, which involves many fundamental issues,
such as the geometric properties and topological invariants of quantum states. Actually, the non-Hermiticity of
quantum systems has attracted many attempts to understand symmetry and topological invariants [13, 62].

3 Symmetries, exceptional points, and topological
invariants
In general, all energy bands are real for Hermitian systems such that the energy band gap near Fermi energy
can be regarded topologically as a point called point gap.
However, for the non-Hermitian systems, the energy
bands could be complex such that the energy band gaps
can be classified topologically to either point or line gaps
in the complex energy plane. When the energy band gap
closes, the topological phase transition between the trivial and topological phases [13, 62].
Note that the diagonal elements of hk are neither equal
nor complex conjugated, we have
(PT )hk (PT )−1 � =hk

(9a)

ξ h†k ξ −1 � =hk ,

(9b)

where P is the parity operator and T is the time reversal
operator. ξ is a unitary and Hermitian matrix [13, 32]. In
other words, both PT and pseudo-Hermitian symmetries
do not hold for this non-Hermitian graphene model. However, with the parameters varying, the occurrence of the
exceptional points (gapless modes) at some k points in the
Brillouin zone may lead to the topological phase transition.
Let us examine the exceptional points of the
energy band structure in the Brillouin zone and their

## PDF page 4

Wu et al. AAPPS Bulletin

(2022) 32:39

Page 4 of 10

corresponding parameters, the energy band (5) gives that
the gapless modes satisfy equation | fk |2 −η2 = 0, which
yields
√
√
3ky
3ky
η2 − 1
3kx
2
(10)
+ cos
=
cos
cos
2
2
2
4
√
3k

In particular, for η = 1,√cos 2 y = 0 infers ky = ± √π
3
3k
with 0 ≤ kx ≤ 2π , or cos 2 y + cos 3k2x = 0 yields
√
3ky
2π
(11a)
±
,
kx =
3
3

√
2π
or ky = 3kx ± √ ,
3

(11b)

which implies that the line gap may occur along these
two lines in the Brillouin zone, which could be mapped
to the complex energy plane. On the other hand, by
maximizing and minimizing cosine functions in (10), the
range of η for the exceptional points (gapless) is obtained
as 1 ≤ η ≤ 3.
It should be remarked that the occurrence of the exceptional point implies the existence of the topological phase
for non-Hermitian systems even though the system does
not contain the PT and pseudo-Hermitian symmetries. In
particular, the occurrence of the exceptional point is associated with the divergence of the Berry curvature. We will
see this connection in the Section 6. Usually, the winding
number or vorticity can be identified the exceptional point
appearing inside or outside of the integral loop even for
non-Hermitian systems [62]. How to connect the topological invariants of the quantum states to the physical observables and phenomena is worth studying further.

4 Berry connection and complex Berry phase
The Berry connection can be generalized to
Aαβ := i�ψ̃α |d|ψβ � for non-Hermitian systems. The
matrix form is expressed as [21]
�
� �
�
�+ | dψ+
�+ | dψ−
ψ
ψ
� �
�
A = i �
�− | dψ+
�− | dψ−
ψ
ψ
Using the eigenvectors in (6) and (7), the Berry connection can be obtained by

1
1
(σ0 + σz cos φk − σx sin φk )dθk + σy dφk .
2
2
(12)
where σ0 = 12×2 is the identity matrix, and σx,y,z are Pauli’s matrices. The sine and cosine functions are defined by
(see (8a)),
A=

∣ ∣
∣ fk ∣
sin φk := √∣ ∣
,
∣ fk ∣ 2 − η 2

(13a)

iη
cos φk := √∣ ∣
.
∣ fk ∣ 2 − η 2

(13b)

∮
The Berry phase is defined by γ± = C A±, where A± are
the diagonal elements in (12), respectively. The loop integral means that the Berry phase depends on the cyclic
quantum evolution in the parameter (or k ) space. Using
(12), we can obtain the Berry phase,
∮
∮
1
γ± =
A± =
(1 ± cos φk )dθk ,
(14)
2 C
C
which is in general complex because the Hamiltonian is non-Hermitian. Using (8b), we have
dθk = ∇k arg(fk ) · dk , and the Berry phase can be
expressed as
∮
i
γ± =
(1 ± cos φk )∇k arg(fk ) · dk,
(15)
2 C
Note that

∂θk
fk
∂
=i
ln ∣∣ ∣∣ ,
∂kx
∂kx
fk

(16a)

∂θk
fk
∂
=i
ln ∣∣ ∣∣ ,
∂ky
∂ky
fk

(16b)

then we obtain

(

∂
∂
+j
∇k arg(fk ) = i i
∂kx
∂ky

)

fk
ln ∣∣ ∣∣ .
fk

(17)

5 Complex Berry curvature
The Berry curvature defined by F = dA plays a gauge
field for the Hermitian system. For the non-Hermitian
system, the Berry connection is generalized to complex
domain such that the Berry curvature is also generalized to complex domain. In order to give the explicit
expression of the complex Berry curvature, the Berry
connection in Eq. (12) can be rewritten as
)
1(
Aθ dθk + Aφ dφk ,
2

(18)

Aθ :=σ0 + σz cos φk − σx sin φk ,

(19)

A=
where

## PDF page 5

Wu et al. AAPPS Bulletin

(2022) 32:39

Page 5 of 10

(20)

Aφ :=σy .
Using (8a), we have

(21a)

∂φk
iη
∂ | fk |
=
2
2
∂ky | fk | −η ∂ky

(21b)

We obtain the coordinate transformation from the (θk , φ)
-space to the (kx , ky )-space.


�
�
�
�
∂ arg(fk )
∂ arg(fk )
dθk
∂k
∂ky
 dkx .
=  iη x ∂|fk |
∂|fk |
iη
dφk
dky
2
2
2
2
∂kx

|fk | −η

(23)

A = Ax dkx + Ay dky ,
where

[

]

(24a)

[
]
∂ arg(fk )
∂ | fk |
1
,
+ iPk
Ax = Aθ
2
∂ky
∂ky

(24b)

∂ arg(fk )
∂ | fk |
1
Aθ
+ iPk
2
∂kx
∂kx

with

Pk :=

(
) ∂ | fk |
∂Aθ
iη
=− (
,
)3/2 σz | fk | +σx iη
2
2
∂kx
∂kx
| fk | −η

(29a)

(
) ∂ | fk |
∂Aθ
iη
=− (
.
)3/2 σz | fk | +σx iη
2
2
∂ky
∂ky
| fk | −η

(29b)
By substituting above equations to Eq.(27), we finally
obtain the 2-form Berry curvature.

∂kx

(22)
Thus, the Berry connection in Eq. (18) can be expressed
in terms of k space

Ax =

(28b)

with (21), we get

∂φk
∂ | fk |
iη
=
,
∂kx | fk |2 −η2 ∂kx

|fk | −η

∂φk
∂Aθ
= − (σz sin φk + σx cos φk )
.
∂ky
∂ky

ησy
.
| fk |2 −η2

(25)

The z-component of Berry curvature is defined by the
2-form
)
(
∂Ay
∂Ax
−
dkx ∧ dky .
�=
(26)
∂kx
∂ky
The partial derivative of (24) is given by
2

2

𝜕Ax 1 𝜕A𝜃 𝜕 arg(f𝐤 ) 1 𝜕 arg(f𝐤 )
i 𝜕P𝐤 𝜕 ∣ f𝐤 ∣ 1 𝜕 ∣ f𝐤 ∣
=
+ A𝜃
+
+ P𝐤
,
2
2 𝜕ky 𝜕kx
2 𝜕ky 𝜕kx
𝜕ky 2 𝜕ky
𝜕kx
𝜕ky 𝜕kx

(27a)

2
𝜕 2 arg(f𝐤 )
1 𝜕A𝜃 𝜕 arg(f𝐤 )
i
i 𝜕P𝐤 𝜕 ∣ f𝐤 ∣
i 𝜕 ∣ f𝐤 ∣
=
+ A𝜃
+
+ P𝐤
.
2
2 𝜕kx 𝜕ky
2 𝜕kx 𝜕ky
𝜕kx 2 𝜕kx
𝜕ky
𝜕kx 𝜕ky

𝜕Ay

∂Pk ∂|fk |
k ∂|fk |
Note that ∂P
∂kx ∂ky − ∂ky ∂kx = 0 and

∂φk
∂Aθ
= − (σz sin φk + σx cos φk )
,
∂kx
∂kx

=

1
Fz dkx ∧ dky ,
2

(30)

where Fz = (αk σx + βk σz ) with
𝛼𝐤 = (

i𝜂 2
∣ f𝐤 ∣2 −𝜂 2

)3∕2 det Λ𝐤

𝜂 ∣ f𝐤 ∣
𝛽𝐤 = (
)3∕2 det Λ𝐤 ,
∣ f𝐤 ∣2 −𝜂 2

(31)

where



then



∂|fk |
∂|fk |
∂k
∂k
�k =  ∂ arg(fx k ) ∂ arg(fy k ) 
∂kx
∂ky

det �k =

∂ | fk | ∂ arg(fk ) ∂ | fk | ∂ arg(fk )
−
.
∂kx
∂ky
∂ky
∂kx

(32)

(33)

The complex 2-form Berry curvature can be rewritten to
the real and imaginary parts,

Fz = Fzr + iFzi ,

(34)

For | fk |2 −η2 > 0,

Fzr := (

η | fk |

)3/2 det(�k )σz ,

(35a)

)3/2 det(�k )σx .

(35b)

)3/2 det(�k )σx ,

(36a)

| fk |2 −η2

Fzi := (

η2

| fk |2 −η2

(27b)

For | fk |2 −η2 < 0,

(28a)

Fzr := (

−η2

| fk |2 −η2

## PDF page 6

Wu et al. AAPPS Bulletin

Fzi := (

η | fk |

| fk |2 −η2

(2022) 32:39

)3/2 det(�k )σz .

Page 6 of 10

(36b)

It should be remarked that the non-Hermiticity η of
the system induces the Berry curvature. When η → 0,
Fz → 0 which may be called the Berry flat. The Berry
curvature can be regarded as a 2-form non-Abelian gauge
field. Its components are represented a 2 × 2-matrix. The
real and complex components are related to the Pauli’s
matrix σx and σz in (35) and (36).

6 Relationships between complex Berry curvature
and complex energy band structure
In order to reveal the physical mechanism of the complex
Berry curvature, We analyze the relationship between the
complex Berry curvature and the energy band structure
of the non-Hermitian graphene model. It can be seen that
Fz is in general complex. At some points | fk |= η in the
Brillouin zone for given η, the real and imaginary parts of
the curvature Fzr and Fzi diverge, which corresponds to
the energy gap closing (see Eq. (5)).
We plot numerically the complex energy bands in
the Brillouin zone in Fig. 2, where we set ǫA = 0 without lose of generality. It can be seen that the energy
band structures show quite different structures with

the non-Hermitian parameter η. The real and imaginary
parts of the valence and conduction bands, Re(E± ) and
Im(E± ), are symmetric and depend on the non-Hermitian parameter η. They show three typical structures in
the parameter space.
For the parameter η = 0.5, both of Re(E± ) and Im(E± )
of the energy bands show some cave structures in the
Brillouin zone and the gaps of Re(E± ) and Im(E± ) close
in some k regions. There is a big cave of Re(E± ) in the
center (Ŵ point) of the Brillouin zone and six-half caves of
Re(E± ) located at the corner (K,K’ points) of the Brillouin
zone. For the imaginary part of the energy band, Im(E± ),
there are six small caves appearing at the corners of the
Brillouin zone. It should be noted that the caves of Re(E± )
are connected, but the caves of Im(E± ) are separated by
the flat regions in the Brillouin zone (see in Fig. 2a and
b). As η increases and reach 2, the caves of the Re(E± )
become separated and the caves of Im(E± ) become connected at η = 2 shown in Fig. 2 c and d.
When the parameter η increases further, the real part
of the energy band Re(E± ) continuously deformed into
a smaller disk and finally vanish in the Brilouin zone for
η = 3 shown in Fig. 2 e and f. The imaginary part of the
energy band Im(E± ) forms a Dirac-like cone at the Ŵ point
in the Brillouin zone. When the parameter increases

Fig. 2 (Color online): The complex energy band structures in Brillouin zone for different parameter parameters η. a, b The real and imaginary parts
of the complex energy structure in η = 0.5. c, d The real and imaginary parts of the complex energy structure in η = 2. e, f The real and imaginary
parts of the complex energy structure in η = 3. We set ǫA = 0

## PDF page 7

Wu et al. AAPPS Bulletin

(2022) 32:39

further η ≥ 3, Re(E± ) = 0, but the gap of Im(E± ) emerges
at the Ŵ point of Brillouin zone [63]. What physical phenomena observed from this complex energy structure are
worth studying further.
In general, the complex energy gap closing with the
parameter varying in the non-Hermitian systems occurs
at the exceptional degeneracy associated with the topological phase depending on the symmetry of systems,
such as the topological phase characterized by the Chern
number for quantum Hall systems or winding number
for Su-Schrieffer-Heeger model [13, 34].
In Figs. 3, 4, and 5, we plot the diagonal and off-diagonal components of the complex Berry curvature matrix
with several non-Hermitian parameters η in the Brillouin
zone. For η = 0.5 shown in Fig. 3 from a to d, we can see
that there are several small peaks of the curvature components Re(F11 ), Im(F11 ), Re(F12 ), and Im(F12 ) appearing in the Brillouin zone. The peaks for the Re(F11 ) and
Im(F12 ) are much higher than those of the Im(F11 ) and
Re(F12 ). As the parameter increases to η = 2 in Fig. 4
from a to d, the peaks of the complex components of the
curvatures become sharp and high. When the parameter
increases further to η = 3 in Fig. 5 from a to d, all peaks
of the complex curvatures return to be fat and low.

Page 7 of 10

In general, the behaviors of the complex curvature
depend on the energy band structure. The peaks of the
complex curvatures appear at the exceptional (gapless)
points | fk |2 → η2 in the Brillouin zone for given η. The
peak appearance should be associated with some physical
phenomena. This is still an open question for further study.
In principle, the non-Hermitian part of the Hamiltonian describes some dissipative or non-conserved
phenomena of systems. It can be seen that the Berry curvature plays a non-Abelian gauge field. The Berry gauge
field is observable. The Berry curvature F divergence
may provide a measurable signal to detect the quantum
phase transition in non-Hermitian systems.

7 Conclusions and outlook
Graphene as a typical 2D material has been attracted
a lot of efforts for potential applications in nanoelectronics and many attempts to explore the fundamental
issues, such as the quantum Hall conductance in the
graphene system, which is expressed in terms of the
Chern number [64, 65]. In particular, non-Hermitian
quantum systems describe dissipative phenomena,
which exhibit rich physics beyond Hermitian systems
due to their complex energy band structures [13, 33].

Fig. 3 (Color online): The complex Berry curvatures in the Brillouin zone for the parameter parameters η = 0.5. a and b are the real and imaginary
parts of the diagonal component of the complex Berry curvature F11, respectively. c and d are the real and imaginary parts of the off-diagonal
complex Berry curvature F12, respectively

## PDF page 8

Wu et al. AAPPS Bulletin

(2022) 32:39

Page 8 of 10

Fig. 4 (Color online): The complex Berry curvatures in the Brillouin zone for the parameter parameters η = 2. a and b are the real and imaginary
parts of the diagonal component of the complex Berry curvature F11, respectively. c and d are the real and imaginary parts of the off-diagonal
complex Berry curvature F12 , respectively

Fig. 5 (Color online): The complex Berry curvatures in the Brillouin zone for the parameter parameters η = 3. a and b are the real and imaginary
parts of the diagonal component of the complex Berry curvature   F11, respectively. c and d are the real and imaginary parts of the off-diagonal
complex Berry curvature F12, respectively

## PDF page 9

Wu et al. AAPPS Bulletin

(2022) 32:39

In this paper, we have considered the non-Hermitian
graphene model to describe the asymmetric coupling
between the graphene and the substrate based on the
tight-binding approximation. We have given analytically the complex Berry connection and Berry curvature
of this non-Hermitian graphene model and numerically investigated the relationship between the complex Berry curvature and the complex energy structure.
The behaviors of the complex Berry curvature depend
on the complex energy band structure and the nonHermitian parameter η. In particular, we find that some
cave structures of both real and imaginary parts of the
energy bands occur in the Brillouin zone. Interestingly,
the Dirac cone of the imaginary energy band emerges
and the flat structure of the real part of the energy band
for η = 3. These imply some hints for the topological
invariants in the non-Hermitian graphene. The complex
Berry curvature and its non-analytic behaviors in the
Brillouin zone provides a way to explore quantum phase
transition [15, 20–22]. The occurence of the peaks of the
Berry curvature corresponds to the exceptional (gapless) points. Actually, there are still some puzzles for
studying further. For example, whether the non-analytic
behaviors of the complex Berry curvature are related to
the topological invariants like quantum Hall conductance and admittance [54].
From the mathematical point of views, the complex
curvature may be related to complex geometry and complex manifold. These open a connection between theoretical physics and mathematics [66]. In particular, the
occurence of the Dirac cone of the energy bands involves
the Dirac equation, which implies the relativistic effect or
the Minkowski geometry appearing in condensed matter
systems. These results provide a novel insight to the relationship between the non-Hermitian quantum, geometry,
and topological invariants as well as their applications.
Acknowledgements
The authors thank the Grant of Scientific and Technological Projection of
Guangdong province No: 2021A1515010036. .
Authors’ contributions
The authors read and approved the final manuscript.
Funding
Not applicable.
Availability of data and materials
Not applicable.

Declarations
Ethics approval and consent to participate
The authors declare they have upheld the integrity of the scientific record.
Consent for publication
The authors give their consent for publication of this article.

Page 9 of 10

Competing interests
The authors declare that they have no competing interests.
Author details
School of Physics, Sun Yat-Sen University, Guangzhou 510275, China. 2 CAS
Key Laboratory of Theoretical Physics, Institute of Theoretical Physics, Chinese
Academy of Sciences, Beijing 100190, China. 3 State Key Laboratory of Optoe‑
lectronic Material and Technology, Sun Yat-Sen University, Guangzhou 510275,
China. 4 Guangdong Province Key Laboratory of Display Material and Technol‑
ogy, Sun Yat-Sen University, Guangzhou 510275, China.

1

Received: 19 August 2022 Accepted: 1 November 2022

References
1. C.L. Kane, Topological Band Theory and the Z2 Invariant, Chapter 1,
Topological Insulators. ed. by M. Franz, L. Molenkamp (Elsevier, New York,
Oxford, 2013)
2. M.Z. Hasan, C.L. Kane, Topological insulators, Rev. Mod. Phys. 82, 3045
(2010)
3. G. Tkachov, Topological Insulators: The Physics of Spin Helicity in Quan‑
tum Transport. (Pan Stanford Publishing, CRC PressTaylor & Francis Group,
6000 Broken Sound Parkway NW, Suite 300Boca Raton, FL 33487-2742,
2016)
4. X.-L. Qi, T.L. Hughes, S.-C. Zhang , Phys. Rev. B 78, 195424(2008); X.-L. Qi,
Y.-S. Wu, S.-C. Zhang, Topological quantization of the spin Hall effect in
two-dimensional paramagnetic semiconductors, Phys. Rev. B. 74, 085308
(2006)
5. B. Andrei Bernevig, T.L. Hughes, Topological insulators and topological
superconductors. (Princeton University Press,Princeton and Oxford,2013)
6. A.P. Schnyder, S. Ryu, A. Furusaki, A.W.W. Ludwig, Classification of topo‑
logical insulators and superconductors in three spatial dimensions, Phys.
Rev. B 78, 195125 (2008)
7. C.-K. Chiu, J.C.Y. Teo, A.P. Schnyder, S. Ryu, Classification of topological
quantum matter with symmetries, Rev. Mod. Phys. 88, 035005-1 (2016)
8. A. P. Schnyder, S. Ryu, A.P. Schnyder, A. Furusaki, A.W.W. Ludwig, Clas‑
sification of topological insulators and superconductors in three spatial
dimensions, Phys. Rev. B 78, 195125 (2008).
9. D. Chruscinski, A. Jamiolkowski, Geometric Phase in classical and quan‑
tum mechanics. (Birkhauser Press, Boston, Basel, Berlin, 2004)
10. D. Xiao, M.-C. Chang, Q. Niu, Berry phase effects on electronic properties,
Rev. Mod. Phys. 82, 1959 (2010)
11. R. El-Ganainy, K.G. Makris, M. Khajavikhan, Z.H. Musslimani, S. Rotter, D.N.
Christodoulides, Non-Hermitian physics and PT symmetry, Nat. Phys. 14,
11 (2018)
12. Z. Gong, Y. Ashida, K. Kawabata, K. Takasan, S. Higashikawa, M. Ueda,
Topological Phases of Non-Hermitian Systems, Phys. Rev. X 8, 031079
(2018)
13. K. Kawabata, K. Shiozaki, M. Ueda, M. Sato, Symmetry and Topology in
Non-Hermitian Physics, Phys. Rev. X 9, 041015 (2019)
14. H. Mehri-Dehnavi, A. Mostafazadeh, Geometric phase for non-Hermitian
Hamiltonians and its holonomy interpretation, J. Math. Phys. 49, 082105
(2008)
15. F. Keck, H.J. Korsch, S. Mossmann, Photonic topological fermi nodal
disk in non-Hermitian, J. Phys. A 36, 2125 (2003); G. Dattoli, R. Mignani,
A. Torre, Pseudo-Hermiticity versus PTPT-symmetry III: Equivalence of
pseudo-Hermiticity and the presence of antilinear symmetries J. Phys. A
23, 5795 (1990); I. Rotter, Non-Hermitian Skin Modes Induced by On-Site
Dissipations and Chiral Tunneling Effect, J. Phys. A 42, 153001 (2009)
16. W.D. Heiss, H.L. Harney, The Chirality of Exceptional Points, Eur. Phys. J.
D 17, 149 (2001); H.L. Harney, W.D. Heiss, Time reversal and exceptional
points, Eur. Phys. J. D 29, 429 (2004); W.D. Heiss, Exceptional Points – Their
Universal Occurrence and Their Physical Significance, Czech. J. Phys. 54,
1091 (2004); W.D. Heiss, Time reversal and exceptional points, Eur. Phys. J.
D7, 1 (1999)
17. A. Mondragon, E. Hernandez, Berry phase of a resonant state, J. Phys. A
29, 2567 (1996)
18. J.C. Garrison, E.M. Wright, Complex geometrical phases for dissipative
systems, Phys. Lett. A 128, 177 (1988)

## PDF page 10

Wu et al. AAPPS Bulletin

(2022) 32:39

19. M.V. Berry, Physics of nonhermitian degeneracies, Czech. J. Phys. 54, 1039
(2004)
20. A. I. Nesterov, S.G. Ovchinnikov, Geometric phases and quantum phase
transitions in open systems Phys. Rev. E 78, 015202(R) (2008); S. Massar,
Applications of the complex geometric phase for metastable systems,
Phys. Rev. A 54, 4770 (1996)
21. S.-D. Liang, G.-Y. Huang, Topological invariance and global Berry phase in
non-Hermitian systems, Phys. Rev. A 87, 012118 (2013)
22. M.S. Rudner, L.S. Levitov, Topological Transition in a Non-Hermitian Quan‑
tum Walk, Phys. Rev. Lett. 102, 065703 (2009)
23. H.-Q. Zhou, S.Y. Cho, R.H. McKenzie, Gauge Fields, Geometric Phases, and
Quantum Adiabatic Pumps, Phys. Rev. Lett. 91 186803 (2003); P.W. Brou‑
wer, Scattering approach to parametric pumping, Phys. Rev. B 58 R10135
(1998)
24. F. Tang, H.C. Po, A. Vishwanath, X. Wan, 5th Anniversary Article: Towards
Solar Methanol: Past, Present, and Future, Sci. Adv. 8, 1 (2019)
25. Lin. Zhang, Long. Zhang, S. Niu, X.-J. Liu, Dynamical classification of topo‑
logical quantum phases, Sci. Bull. 63, 1385 (2018)
26. T.O. Wehling, A.M. Black-Schaffer, A.V. Balatsky, Dirac materials, Adv. Phys.
63, 1 (2014)
27. L. Fidkowski,Entanglement Spectrum of Topological Insulators and Super‑
conductors, Phys. Rev. Lett. 104, 130502 (2010)
28. Y.C. Hu, T.L. Hughes, Absence of topological insulator phases in nonHermitian PT-symmetric Hamiltonians, Phys. Rev. B 84, 153101 (2011)
29. D. Leykam, K.Y. Bliokh, C. Huang, Y.D. Chong, F. Nori, Edge Modes, Degen‑
eracies, and Topological Numbers in Non-Hermitian Systems, Phys. Rev.
Lett. 118, 040401 (2017)
30. V.M. Martinez Alvarez, J.E. Barrios Vargas, M. Berdakin, L.E.F. Foa Torres,
Topological states of non-Hermitian systems, Eur. Phys. J. Spec. Top. 227,
1295–C1308 (2018)
31. C.M. Bender, S. Boettcher, Real Spectra in Non-Hermitian Hamiltonians
having PT Symmetry, Phys. Rev. Lett. 80, 5243 (1998); C.M. Bender, D.C.
Brody, H.F. Jones, Complex Extension of Quantum Mechanics, Phys. Rev.
Lett. 89, 270401 (2002)
32. A. Mostafazadeh, PSEUDO-HERMITIAN REPRESENTATION OF QUANTUM
MECHANICS, Int. J. Geom. Methods Mod. Phys. 7, 1191 (2010); A. Mosta‑
fazadeh, Energy observable for a quantum system with a dynamical
Hilbert space and a global geometric extension of quantum theory, Phys.
Rev. D 98, 046022 (2018); A. Mostafazadeh, Pseudo-Hermiticity versus PT
Symmetry: The Necessary Condition for the Reality of the Spectrum of a
Non-Hermitian Hamiltonian. J. Math. Phys. 43, 205-243 (2002)
33. N. Moiseyev, Non-Hermitian Quantum Mechanics (Cambridge, The
Edinburgh Building, Cambridge CB2 8RU, UK, 2011)
34. T.E. Lee, Anomalous Edge State in a Non-Hermitian Lattice. Phys. Rev. Lett.
116, 133903 (2016)
35. V.M.M. Alvarez, J.E.B. Vargas, L.E.F.F. Torres, Non-Hermitian robust edge
states in one dimension: Anomalous localization and eigenspace conden‑
sation at exceptional points, Phys. Rev. B 97, 121401(R) (2018); V.M. Martinez
Alvarez, J.E. Barrios Vargas, M. Berdakin, L.E.F. Foa Torres,Topological states of
non-Hermitian systems, Eur. Phys. J. Spec. Top. 227, 1295 (2018)
36. K. Kawabata, K. Shiozaki, M. Ueda, Anomalous helical edge states in a
non-Hermitian Chern insulator Phys. Rev. B 98, 165148 (2018)
37. T. Liu, Y.-R. Zhang, Q. Ai, Z. Gong, K. Kawabata, M. Ueda, F. Nori, SecondOrder Topological Phases in Non-Hermitian Systems, Phys. Rev. Lett. 122,
076801 (2019)
38. F.K. Kunst, E. Edvardsson, J.C. Budich, E.J. Bergholtz, Biorthogonal BulkBoundary Correspondence in Non-Hermitian Systems. Phys. Rev. Lett.
121, 026808 (2018)
39. S. Yao, Z. Wang, Edge States and Topological Invariants of Non-Hermitian
Systems, Phys. Rev. Lett. 121 086803 (2018); S. Yao, F. Song, Z. Wang, NonHermitian Chern Bands, Phys. Rev. Lett. 121, 136802 (2018)
40. K. Esaki, M. Sato, K. Hasebe, M. Kohmoto, Edge states and topological
phases in non-Hermitian systems, Phys. Rev. B 84, 205128 (2011)
41. S. Lieu, Phys. Rev. B 97, 045106 (2018); H. Jiang, C. Yang, S. Chen, Topological
invariants and phase diagrams for one-dimensional two-band non-Hermi‑
tian systems without chiral symmetry, Phys. Rev. A 98, 052116 (2018)
42. B. Zhu, R. Lu, S. Chen, PT symmetry in the non-Hermitian Su-SchriefferHeeger model with complex boundary potentials, Phys. Rev. A 89,
062102 (2014)
43. H. Jiang, C. Yang, S. Chen, Topological invariants and phase diagrams
for one-dimensional two-band non-Hermitian systems without chiral

Page 10 of 10

44.
45.
46.

47.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.

59.

60.
61.
62.
63.
64.

65.
66.

symmetry, Phys. Rev. A 98, 052116 (2018); C. Yin, H. Jiang, L. Li, L Rong, S
Chen, Geometrical meaning of winding number and its characterization
of topological phases in one-dimensional chiral non-Hermitian systems,
Phys. Rev. A 97, 052115 (2018)
F. Dangel, M. Wagner, H. Cartarius, J. Main, G. Wunner, Topological invari‑
ants in dissipative extensions of the Su-Schrieffer-Heeger model, Phys.
Rev. A 98, 013628 (2018)
R. Chen, C.-Z. Chen, B. Zhou, D.-H. Xu, Finite-size effects in non-Hermitian
topological systems, Phys. Rev. B 99, 155431 (2019)
Y. Chen, H. Zhai, Hall conductance of a non-Hermitian Chern insulator,
Phys. Rev. B 98, 245130 (2018); C. Yin, H. Jiang, L. Li, L Rong, S. Chen,
Geometrical meaning of winding number and its characterization of
topological phases in one-dimensional chiral non-Hermitian systems,
Phys. Rev. A 97, 052115 (2018)
C.M. Bender, D.C. Brody, H.F. Jones, B.K. Meister, Faster than Hermitian
Quantum Mechanics. Phys. Rev. Lett. 98, 040403 (2007)
C. Zheng, L. Hao, G.L. Long, Observation of a Fast Evolution in a ParityTime-Symmetric System. Philos. Trans. R. Soc. A. 371, 20120053 (2013)
Y.-L. Ma, M. Rho, Topology change, emergent symmetries and compact
star matter. AAPPS Bull. 31(1), 16 (2021)
S. Nakatsuji, Topological magnets-their basic science and potential appli‑
cations. AAPPS Bull. 32(1), 25 (2022)
O. Sigwarth, C. Miniatura, Time reversal and reciprocity. AAPPS Bull. 32(1),
23 (2022)
Y. Jiao et al., Optical nonreciprocal response and conversion in a TavisCummings coupling optomechanical system. Quant. Eng. 2(2), e39 (2020)
G.F. Xu, D.M. Tong, Realizing multi-qubit controlled nonadiabatic holo‑
nomic gates with connecting systems. AAPPS Bull. 32(1), 13 (2022)
A. Fan, G.-Y. Huang, L. Shi-Dong, Complex Berry curvature pair and
quantum Hall admittance in non-Hermitian systems, J. Phys. Commun. 4,
115006 (2020)
A. Fan, L. Shi-Dong, Complex energy plane and topological invariant
in non-Hermitian systems, Front. Phys. 17(3), 33501 (2022); Ann. Phys.
(Berlin) 2100520 (2021)
A. Fan, L. Shi-Dong, Zero modes of velocity field and topological invariant
in quantum torus , Results Phys. 31, 104912 (2021); Ann. Phys. (Berlin)
2100443 (2022)
E.L. Wolf, Graphene: A New Paradigm in Condensed Matter and Device
Physics. (Oxford University, 2014)
D.S.L. Abergel, V. Apalkov, J. Berashevich, K. Ziegler, Properties of gra‑
phene: a theoretical perspective, T. Chakraborty, Adv. Phys., 59 261 (2010);
S.A. Wolf, D.D. Awschalom, A. Buhrman, J.M. Daughton, S. von Molnar,
M.L. Roukes, A.Y. Chtchelkanova, D.M. Treger, Spintronics: A spin-based
electronics vision for the future, Science 294 1488 (2001)
K. Bakke, A. Yu. Petrov, C. Furtado, A Kaluza–Klein description of geometric
phases in graphene, Ann. Phys. 327, 2946 (2012); C. Furtado, F. Moraes,
A.M. de M. Carvalho, Geometric phases in graphitic cones Phys. Lett. A
372, 5368 (2008)
Y. Hatsugai, T. Fukui, H. Aoki, Topological aspects of graphene, Eur. Phys. J.
Spec. Top. 148 133 (2007); H. Aoki, M.S. Dresselhaus, Physics of graphene
(Springer, Cham Heidelberg New York Dordrecht London,2014)
H. Shen, B. Zhen, L. Fu, Topological Band Theory for Non-Hermitian Hamil‑
tonians, Phys. Rev. Lett. 120, 146402 (2018)
A. Ghatak, T. Das, New topological invariants in non-Hermitiansystems, J.
Phys. CM 113235 (2019)
We numerically investigate these cases and do not show the figures due
to the space limitation, Chao Wu, Thesis, Sun Yat-Sen University, 2016.
A. Bohm, A. Mostafazadeh, H. Koizumi, Q. Niu, 1. Zwanziger, The Geomet‑
ric Phase in Quantum Systems: Foundations, Mathematical Concepts,
and Applications in Molecular and Condensed Matter Physics (Springer,
Springer-Verlag Berlin Heidelberg New York, 2003)
Emil Prodan, Hermann Schulz-Baldes, Bulk and Boundary Invariants for
Complex Topological Insulators (Springer, 2016)
P. Bracken, Geometric Structure for Quantum Mechanics. Int. J. Theo. Phys.
42(4), 2003 (2003)

Publisher’s Note

Springer Nature remains neutral with regard to jurisdictional claims in pub‑
lished maps and institutional affiliations.
