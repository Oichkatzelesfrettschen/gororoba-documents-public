Source: https://doi.org/10.3390/cryst14020194
PDF sha256: ff0a1df41e6c392eaea3958052e1831a22b1fc44c1a5461e21ae9ea977e25e25
License: cc-by
Language: eng
Fidelity: machine-gated

# Transcription of clawson_2024_fibonacci_icosagrid_to_e8_part_ii.pdf

Transcription of `clawson_2024_fibonacci_icosagrid_to_e8_part_ii.pdf` in this directory, 16 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-16 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

crystals
Article

From the Fibonacci Icosagrid to E8 (Part II): The Composite
Mapping of the Cores
Richard Clawson * , Fang Fang

and Klee Irwin

Quantum Gravity Research, Los Angeles, CA 90290, USA; fang@quantumgravityresearch.org (F.F.);
klee@quantumgravityresearch.org (K.I.)
* Correspondence: richard@quantumgravityresearch.org; Tel.: +1-310-574-6927

Abstract: This paper is part of a series that describes the Fibonacci icosagrid quasicrystal (FIG) and its
relation to the E8 root lattice. The FIG was originally constructed to represent the intersection points
of an icosahedrally symmetric collection of planar grids in three dimensions, with the grid spacing of
each following a Fibonacci chain. It was found to be closely related to a five-fold compound of 3D
sections taken from the 4D Elser–Sloane quasicrystal (ESQC), which is derived via a cut-and-project
process from E8 . More recently, a direct cut-and-project from E8 has been found which yields the FIG
(presented in another paper of this series). The present paper focuses not on the full quasicrystal, but
on the relationship between the root polytope of E8 (Gosset’s 421 polytope) and the core polyhedron
generated in the FIG, a compound of 20 tetrahedra referred to simply as a 20-Group. In particular, the
H3 symmetry of the FIG can be seen as a five-fold or “golden” composition of tetrahedral symmetry
(referring to the characteristic appearance of the golden ratio). This is shown to mirror a connection
between tetrahedral and five-fold symmetries present in the 421 . Indeed, the rotations that connect
tetrahedra contained within the 421 are shown to induce, in a certain natural way, the tetrahedron
orientations in the 20-Group.
Keywords: quasicrystals; aperiodic order; periodic order; E8; Elser–Sloane quasicrystal; Gosset
polytope; Gosset 421 ; 600-cell; 24-cell; compound of five cuboctahedra; icosahedral symmetry; H3
symmetry; H4 symmetry; isoclinic rotations; Fibonacci; icosagrid; tetrahedron 20-Group; 20G
Citation: Clawson, R.; Fang, F.; Irwin,
K. From the Fibonacci Icosagrid to E8
(Part II): The Composite Mapping of
the Cores. Crystals 2024, 14, 194.
https://doi.org/10.3390/
cryst14020194
Academic Editors: Zaky A. Zaky
and Zhaketov Vladimir
Received: 1 January 2024
Revised: 10 February 2024
Accepted: 11 February 2024
Published: 15 February 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/
4.0/).

1. Introduction
Quasicrystals, whose early study was inspired by decision theory [1,2] and simple
mathematical curiostiy [3], later became a major area of research in material science [4–9] and
have found applications in areas as wide-ranging as high-energy physics [10,11], conformal
field theory [12] quantum computing [13–15], and biology [16–18]. Two of the most common
methods for mathematically constructing quasicrystals, the dual multigrid (or generalized
dual) method and the cut-and-project (or direct project, or model set) construction, provide
theoretical foundations and many tools for their study [6,19]. They help elucidate links
between symmetries in different numbers of dimensions and, of particular interest in the
present work, the connections between crystallographic and non-crystallographic symmetries.
The Fibonacci multigrid method is a variation of the common dual multigrid method,
wherein the spacing of the grid planes is a Fibonacci chain rather than periodic, and the
quasicrystal vertices are intersection points of these planes as they occur directly in the
grid space, rather than being dual-space vertices (which correspond to tiles in the grid
space) [6,20]. For non-crystallographic point symmetries such as H2 (pentagonal) and
H3 (icosahedral), the regular grids have intersection points that are arbitrarily close to
each other, but the Fibonacci spacing resolves this to provide finite minimal spacing, and
therefore a discrete Fourier spectrum. In Part I of this series, Fang and Irwin have studied
an H3 version [21,22], referred to as the Fibonacci icosagrid (FIG), and have shown that
it is closely related to sections of the Elser–Sloane quasicrystal (ESQC), a 4D quasicrystal
derived by direct cut-and-project from the E8 root lattice [23].

Crystals 2024, 14, 194. https://doi.org/10.3390/cryst14020194

https://www.mdpi.com/journal/crystals

## PDF page 2

Crystals 2024, 14, 194

2 of 16

The fact that this H3 quasicrystal was related to the ESQC was not entirely surprising,
since the ESQC has H4 symmetry and is known to contain H3 symmetric cross-sections [24].
Somewhat more surprising, perhaps, was the fact that the relationship with the FIG was
not based on such a cross-section, but on a tetrahedrally symmetric cross-section which was
then compounded 5-fold in 3D. This is related to the fact that the icosagrid itself can be seen
as a 5-fold compound of tetragrids, just as the vertices of a dodecahedron (icosahedrally
symmetric) are given by a compound of five tetrahedra (Figure 1). (Throughout this paper,
we shall often identify a polytope or compound with its vertices when we think this will
not cause confusion; in certain cases in which we need to draw attention to the facets and
distinguish between, for example, a compound and its convex hull, we will make that
explicit.) This connection between a crystallographic and a non-crystallographic symmetry
in the same dimension is intriguing, leading one group of researchers to call octahedral
symmetry “latent” in icosahedral polyhedra, and vice versa [25].

Figure 1. Dodecahedron, as compound of five tetrahedra.

As a matter of fact, the vertex equivalence of the compound of five tetrahedra with the
dodecahedron leads one to suppose one might take any tetrahedral crystal and compound
it in the same way to achieve an icosahedral quasicrystal. Given a tetrahedrally symmetric
cross-section of the ESQC (as identified by Sadoc and Mosseri [24]), it would be straightforward to construct a compound 3D quasicrystal. Such a construction, however, would seem
unrelated to the ESQC itself, as it originates solely from the 5-fold compounding process
familiar in three dimensions.
Further investigation, however, uncovered a remarkable connection. The FIG’s core
polyhedron is the 20-Group (20G), a group of 20 regular tetrahedra sharing a single vertex,
twisted so that each one shares a face plane with each of its three neighbors (Figure 2b).
The core polytope of the ESQC is the 600-cell, whose facet cells are regular tetrahedra; a
single vertex of the 600-cell is shared by 20 tetrahedral cells, and this is referred to as a
vertex cap. It was found [26] that the 20G and the 600-cell vertex cap can each be obtained
via transformation of the fully symmetric arrangement of 20 regular tetrahedra in 3D
(Figure 2a)—the 20G through a chiral twisting, and the 600-cell vertex cap by curving into
the fourth dimension. Moreover, for each tetrahedron, the curving rotation is precisely the
four-dimensional dual of the twisting rotation.

(a)

(b)

Figure 2. Twenty tetrahedra sharing a single vertex. (a) Full icosahedral symmetry, with gaps between
tetrahedral faces. (b) The 20G: twisted, with chiral icosahedral symmetry (right-handed). No gaps
between tetrahedral faces.

## PDF page 3

Crystals 2024, 14, 194

3 of 16

In brief, then, the vertex cap of the ESQC’s 600-cell seems to induce the FIG’s 20G by
an isoclinic rotation in order to both flatten and twist it. This suggests that the structure
within the ESQC itself can be seen, at least in part, to naturally induce the 3D compounding
of tetrahedral sections to form an icosahedral quasicrystal.
Following this line of thinking, and recalling that the ESQC is derived from E8 , one
wonders if E8 itself might in some sense imply the 3D compounding of tetrahedral quasicrystals to generate icosahedral ones. One is encouraged, in a general sense, by the deep
connections between E8 and H-symmetric quasicrystals [27–29]. Regarding the specific
question of compounding tetrahedral symmetries, it is of note that the FIG’s 20G has the
same vertices as the well-known compound of five cuboctahedra (C5C) (more on this below); such a compound may be thought to be vaguely reminiscent of the 5-fold arrangement
of 24-cells (with their cuboctahedral equators) found in Sadoc and Mosseri’s discrete Hopf
fibration of the E8 root polytope, which they used in their construction of the ESQC [24].
In fact, study of the 24-cell Hopf fibers in the E8 root polytope reveals a related 5-fold
symmetry, and shows how the Elser–Sloane projection space (ES space) arises naturally as
the 4D space most symmetrically oriented with respect to those fibers. It is therefore the
implicit space for a projection that preserves their 5-fold symmetry, projecting them into a
600-cell. Likewise, exploration of the ESQC’s 600-cell as a compound of the five 24-cells
does indeed reveal how it naturally induces the compounding of tetrahedral sections into
icosahedral symmetry. The details are presented in the following sections.
2. E8 and the Elser-Sloane Projection Space
The structure of a cut-and-project quasicrystal depends heavily on the orientation of
the projection space with respect to the parent lattice. In some cases, this may be fairly
arbitrary, or chosen for some desired outcome in the quasicrystal, as there is no inherent
motivation in the lattice itself. Such is the case with the prototypical cut-and-project
example, the construction of the 1D Fibonacci chain from the Z2 lattice [6]. In this case, the
projection space is a line whose angle with the nearer lattice vector is arctan φ1 , which does
√
not emerge naturally from any symmetry or property of Z2 . (Here, φ = 12 (1 + 5) is the
golden ratio.) In contrast to this, the ESQC’s projection from E8 occurs in a projection space
implied by a symmetry of E8 itself, as seen most easily in the Hopf fibration of Sadoc and
Mosseri’s construction [24]. This, in turn, follows Manton’s discrete Hopf fibrations [30].
The symmetries of E8 can be seen in its root polytope, the semiregular Gosset 421 ,
whose vertices all lie on the circumscribing S7 —that is, the 421 may be seen as a discretized
S7 . The Hopf fibration of this decomposes it into S3 fibers over an S4 base, and its orientation
can be chosen so that the fibers partition the 240 vertices of the 421 into 10 sets of 24, where
each set constitutes the vertices of a 24-cell discretizing a distinct S3 fiber (recall that the
24-cell has not only 24 facets, but also 24 vertices). Mapped to the base S4 , these 10 fibers
become the 10 vertices of a 5D orthoplex. With a convenient choice of axes, these lie at
(±1, 0, 0, 0, 0) and all permutations thereof. This is analogous to a unit-radius octahedron
in 3D, with its six vertices at permutations of (±1, 0, 0).
We come now to the symmetry that makes the ES projection space special. In the
5D embedding space of the base S4 , there is a family of directions which are maximally
symmetric with respect to the five axes, these being (±1, ±1, ±1, ±1, ±1) (32 such directions
in total). Each makes the same angle with all five axes, and hence the same angle (or
its supplement) with all 10 vertices of the 421 ’s 5-orthoplex base. The analog in 3D is
easily visualized, where (1, 1, 1) (or any sign permutation) makes the same angle with
each axis, and so is the most symmetric direction with respect to the vertices of the axisaligned octahedron.
√
Inverting the Hopf fibration, (1, 1, 1, 1, 1)/ 5 is a base point whose preimage in 8D
is a certain S3 fiber of the 421 ’s S7 . This fiber does not itself contain any vertices of the
421 , since those are all accounted for in the 10 24-cells, preimages of the actual 5-orthoplex
points. It is, rather, the fiber most symmetrically oriented with respect to those 24-cells. Its
4D span makes the same angle (or its complement) with the 4D spans of each 24-cell. This,

## PDF page 4

Crystals 2024, 14, 194

4 of 16

then, is the ES projection space, the 4D subspace maximally symmetric with respect to the
24-cell fibers of the 421 .
Of course, there is some degeneracy here due to the high degree of symmetry: as
noted, there are 32 distinct vector directions in 5D that are equally symmetric with respect
to the 5-orthoplex vertices, and any of their preimages are equally symmetric with respect
to the 24-cells. Hence, using any one of them as the projection space yields the same 4D
quasicrystal, so the choice is arbitrary in the ESQC construction. Henceforth,
we fix our
√
projection space to be that corresponding to base point P = (1, 1, 1, 1, 1)/ 5.
Here, we review two key properties of the Hopf fibration. First, Hopf fibers are Clifford
parallels, in the sense that between two fibers, all points in one fiber are the same distance
(within the 7-sphere) from the other fiber. Another way to say this is to recall that between
any two 4D subspaces of R8 , there are in general four characteristic angles, but between the
4D spaces of two Hopf fibers, all four angles are the same. Thus, we may speak of “the”
angle between Hopf fibers. Second, this angle between fibers is just half the angle between
their images in the base. Therefore, considering the 5-orthoplex vertices as the images of
our 24-cells, we can identify the angles between fibers, as well as between each fiber and
the ES space.
The ES space makes the same angle θ A with five of the 24-cells, labeled A1 –A5 , and the
complement of that angle with the other five, B1 –B5 , so that we have a natural partitioning
of our 24-cells into two sets of five. 2θ A is found by the inner product of the ES image P with
the images of the Ai , permutations of (−1, 0, 0, 0, 0): cos 2θ A = − √1 , or cos θ A = √ 1
5

φ +2

(where again, φ is the golden ratio, and we have used its special properties to reduce that
expression). The angle between the ES space and each Bi is θ B = π2 − θ A : cos θ B = sin θ A =
√ φ . Incidentally, tan θ B = φ1 , so it is the same angle as used to make the Fibonacci chain
φ +2

from Z2 .
To determine the angles between the various 24-cells, we look at the 5-orthoplex itself.
Every vertex is π2 rad from every other except the one lying opposite it on the same axis,
from which it is π. In 8D, therefore, every 24-cell is π4 rad from every other except one,
from which it is π2 . This gives another natural partitioning of the 24-cells, this time into
five pairs, with the members of a pair being mutually orthogonal. We label the pairs with
indices 1–5, so Ai ⊥ Bi .
In the base S4 , one can find a 5-fold rotation which fixes P and cyclically permutes the
images of the Ai , as well as those of the Bi . This is related to a 5-fold isoclinic rotation of
the 600-cell which cycles the projections of these 24-cells, as described below.
3. ESQC Projection
The Ai 24-cells all make the same angle θ A with the ES space. When the 421 is projected
to this space, therefore, they all project to spherical shells of the same radius, which is to say
that they all project to the same shell. Together on this shell, they give the 120 vertices of a
600-cell. Note that upon projection, a 24-cell is rescaled but otherwise undistorted because
all four dimensions of its space make the same angle with the (also 4D) ES space. Thus,
the 600-cell vertices can be seen as a compound of five 24-cells. The same holds for the Bi ,
but they are projected from a smaller angle, so they form a larger 600-cell. Henceforth, we
focus on a the 600-cell projected from the Ai and its decomposition into five 24-cells.
The 600-cell is preserved under a group of isoclinic rotations, following congruent
polygons in mutually orthogonal planes, these being either decagons, hexagons or squares.
Certain subgroups of the rotations preserve individual 24-cells, while others take each
of the five 24-cells to another. Indeed, the 600-cell can be generated from one 24-cell
by repeated applications of a single isoclinic 2π
5 rotation, each generating a new 24-cell
disjoint from the previous ones until the fifth, which returns to the original with each vertex
restored to its original position. These 24-cells are the projected fibers from the 421 , and the
rotation is a projection of the 5-fold rotation of its 24-cell fibers mentioned above. Indeed,
considering the 24-cell fibers in 8D, this 4D isoclinic rotation cycles their components within
the ES space, while there is a corresponding isoclinic rotation in the perpendicular space;

## PDF page 5

Crystals 2024, 14, 194

5 of 16

these two rotations together comprise exactly that 8D rotation which cycles the Ai and Bi .
2π
(Curiously, the rotation in the perpendicular space has angle 6π
5 instead of 5 , though it
still has period 5.) This construction can be carried out with either left- or right-isoclinic
rotations, producing compounds which we respectively label left and right. They share the
initial 24-cell, but otherwise represent distinct partitionings of the 600-cell. This chirality
will turn out to play a key role in inducing the icosahedral symmetry.
A 24-cell has 3D equatorial cross-sections that are cuboctahedra, and in the following
sections, we will focus on how cuboctahedra in different 24-cells are oriented with respect
to each other, and how the isoclinic rotations bring them into different relationships. We
will show in particular how applying right-isoclinic (left-isoclinic) rotations to cuboctahedra
of a left (right) compound of 24-cells induces the compounding of tetrahedral symmetries
into an icosahedral symmetry—the creation of the C5C, which contains the FIG’s 20G.
4. 24-Cells and Cuboctahedra in the 600-Cell
We represent the vertices of the 600-cell with unit quaternions as described by Moody
and Patera [27] and Sadoc and Mosseri [24]. To begin with, we choose a facet-centered
orientation with respect to the quaternion identity. We partition the vertices into a left
compound of five 24-cells, with the first 24-cell T0 likewise facet-centered; its 24 coordinates
are given by
{
}
1
S
T0 = √ (±1, ±1, 0, 0) ,
(1)
2
where the coordinate list represents quaternion coordinates for {1, i, j, k} and the superscript S indicates the symmetric group, i.e., all permutations of the given coordinates.
(Note that the permutations with zero in the first coordinate give a cuboctahedron.) Onesided quaternion multiplication is always isoclinic, and the remaining 24-cells are found
through left-isoclinic rotations of the first, multiplying on the left by powers of a certain
unit quaternion,
1
r T = √ (−1, 2φ − 1, 1, 1), r T r T∗ = 1
8
Ti = riT T0 , i ∈ {0, 1, 2, 3, 4}
T≡

⋃

Ti .

(2)
(3)
(4)

i

The notation in the second line is to be understood as multiplying each vertex in T0
by riT , and the union T is the full 600-cell. (Note that the i in riT is an exponent, not a
superscripted index).
We now define a second 600-cell F as a compound of the five (normalized) 24-cells
dual to the Ti , so that the Fi have their vertices along the facet normals of the Ti . The first is
{
}
1
F0 = (±1, 0, 0, 0)S , (±1, ±1, ±1, ±1) ,
(5)
2
and the rest are again given by left isoclinic rotations,
1
r F = ( , φ, 1, 0)
φ
Fi = riF T0 ,

(6)

i ∈ {0, 1, 2, 3, 4}

(7)

⋃

(8)

F≡

Fi .

i

Of course, F and T are related by an isoclinic rotation,
T = r TF F,

1
r TF = √ (1, 1, 0, 0).
2

(9)

## PDF page 6

Crystals 2024, 14, 194

6 of 16

F is a closed quaternion group, the icosians, isomorphic to the binary icosahedral group;
F0 is a subgroup, the unit Hurwitz quaternions, isomorphic to the binary tetrahedral
group [28]. One may already see, in this group structure, the inherent compounding of
tetrahedral symmetries into icosahedral symmetry.
F and T are dual as compounds, since each 24-cell is self-dual; just as the vertices of Fk
are the facet normals of Tk , so the vertices of Tk are the facet normals of Fk . But this applies
only when T and F are taken as compounds of 24-cells: taken as 600-cells, T and F are not
dual, since each has 600 facet normals, of which only 120 are vertices of the other.
The set F is important here, as facet normals of those 24-cells in T, because in a given
24-cell, parallel to each facet is a cuboctahedral equator, and it is these cuboctahedra that
we wish to study under rotations. The facets of a single 24-cell come in 12 parallel pairs
(on opposite sides of the polytope), so it has 12 such equators, each living in a 3D subspace
defined by the facet normal. If we choose one cuboctahedron from each 24-cell in the
compound T and rotate them all together into a single target 3D space, what would they
look like?
This depends, of course, on the specific rotations used. There are two criteria which
seem most natural. The first is that the rotation from each initial 3D subspace to the target
space should be direct, i.e., the rotation plane should be defined by the normals of the
two spaces, and hence the rotation angle will simply be the angle between those normals.
The next is that the rotation should be isoclinic, since isoclinic rotations are so integral to
the symmetries of the 600-cell and the 24-cell. This means the direct initial-to-target-space
rotation will be accompanied by a rotation of the same angle in the dual plane, orthogonal
to both their normals. This plane will lie within both spaces; indeed, it is their unique plane
of intersection. Our two criteria still leave open the question of whether the rotation would
be left- or right-isoclinic, and we will find that each is meaningful in its own way.
A third factor, which would obviously (one initially supposed) affect how the cuboctahedra look after such a rotation, is which specific cuboctahedra are selected to begin
with—as mentioned, there are 12 to choose from in each 24-cell. The surprising result of
this study is that it does not matter: all the cuboctahedra from a given 24-cell converge to
the same image under their respective rotations of the previous paragraph. Indeed, under
the left-isoclinic rotations, even the ones from different 24-cells all converge into one, so
that there is only a single image for all 60 cuboctahedra. Under the right-isoclinic rotation,
those from the five 24-cells map respectively to members of the C5C. These results are
demonstrated in the next section.
First, however, a comment on the C5C itself. From any polyhedron, an icosahedrally
symmetric compound can be constructed simply by choosing icosahedral symmetry axes
with some fixed orientation relative to the polyhedron, and then applying the symmetry
operations to create more copies of the polyhedron [31]. Icosahedral symmetry has axes of
5-fold, 3-fold, and 2-fold symmetry, and in general, all these symmetries must be applied.
The C5C is a special case, however, wherein compounding around a single 5-fold axis
generates a figure with full icosahedral symmetry. This is due to the inherent connection
between tetrahedral and icosahedral symmetries (illustrated by the fact that the regular
dodecahedron can be partitioned into the vertices of five regular tetrahedra).
In the cuboctahedron, there are planes with a certain implicit 5-fold symmetry. Specifically, a plane through the centroid and containing the center of any square face may
be oriented so that its intersections with the cuboctahedron edges are all equally spaced
(Figure 3). The vectors from the centroid to these edge intersections are then at intervals of
π
π
5 . Moreover, the two square face centers contained in this plane are also 5 from the nearest
edge-intersections, so that the normalized vectors of edge intersections and face centers in
this plane give the vertices of a regular decagon (a more detailed explanation and proof are
provided in Appendix A). Compounding by 5-fold rotations around this plane’s normal
(Figure 4) generates the C5C, which also has the requisite 2-fold and 3-fold symmetries (as
well as 5-fold around other axes) that are needed for full icosahedral symmetry.

## PDF page 7

Crystals 2024, 14, 194

7 of 16

Figure 3. Cuboctahedron with implicit 5-fold plane. The plane contains a square-face-center vector
(indicated by a red dot) and edge intersections (indicated by green dots). With the plane oriented so
that the edge intersections are equally spaced, the edge intersections and the face centers are at angles
of kπ/5. The plane’s normal provides an axis for 5-fold compounding which creates full icosahedral
symmetry (Figure 4).

Figure 4. Compounding of cuboctahedra by rotations in 3D to make the C5C. Successive images
include successive copies of the cuboctahedron, each rotated by an extra multiple of 2π
5 around a
5-fold axis (cyan), which is the plane-normal identified in Figure 3. The last image is the full C5C,
with icosahedral symmetry (most easily seen in its convex hull, shown later in Figure 8c).

5. Rotations to a Single Cuboctahedron or to the C5C
To understand the effect of rotating cuboctahedra from different 24-cells into the same
3D space, we first look at a related question, which is how the different cuboctahedra can be
generated by rotations from a single cuboctahedron in one space. We begin with a theorem
about the left-isoclinic rotations on the compound of five 24-cells.
Theorem 1. Taking T as a compound of 24-cells (that is, considering the 24-cell facets, not the
600-cell facets), a left-isoclinic rotation that takes any one facet to any other will preserve the 24-cell
partitioning; that is, the rotation may permute 24-cells, or permute vertices within 24-cells, but it
will not mix vertices from distinct pre-rotation 24-cells into the same post-rotation 24-cell.
Proof. T is the orbit of T0 under the cyclic action of r T , where each rotation creates a new
24-cell disjoint from the previous ones, until r5T returns T0 back to itself. Repeated actions
of r T on the set must preserve the partitioning, since the first cycle creates the partitions
and the action is cyclic.
Under powers of r T , the orbit of an initial facet f of T0 is a set of five facets, one in
each of the Tk , and the orbits of distinct T0 facets are disjoint. Therefore, to take f to any
facet g in Tk , one may first internally rotate T0 , taking f to the f ′ in T0 that has g in its orbit;
one then simply applies r Tk . Since both r T and the internal rotation of T0 preserve the 24-cell
partitioning, the total rotation does as well.
It remains now to show that every rotation transferring one facet to another is equivalent to such a pair of rotations. But the facet normals of T are the vertices of F, hence the
icosian group. All rotations between these are given by left- and right-multiplication by
the members of the group. Furthermore, left-isoclinic rotations form a closed subgroup.
Now, suppose h f = g, while g is in the orbit of f ′ , i.e., r Tk f ′ = g. Suppose also that h′ is a
rotation that stabilizes T0 , such that h′ f = f ′ . Then, r Tk h′ f = g = h f , and multiplication on

## PDF page 8

Crystals 2024, 14, 194

8 of 16

the right by f −1 yields r Tk h′ = h. Thus, any left-isoclinic rotation h of the group can indeed
be decomposed into an internal rotation h′ of the initial 24-cell followed by a power of r T ,
which therefore preserves the partitioning of the Tk .
With this theorem, we show how quaternion rotations can take any facet in one 24-cell
to any facet in any other 24-cell while preserving the 24-cell partitioning.
In T0 , we define the primary normal n0 , the primary cuboctahedron C0 , and the target 3D
space V for the rotations,
n0 ≡ (1, 0, 0, 0)

(10)

C0 ≡ (0, (±1, ±1, 0)S )

(11)

V ≡ Span(C0 ).

(12)

where the notation in (11) for the cuboctahedron vertices should be self-explanatory (recalling that the S refers to permutations). Note that n0 is normal to C0 and V, as well as to the
T0 facet (1, (±1, 0, 0)S ), whereby it is a vertex of F0 .
Now, let q be a unit quaternion that rotates n0 to a facet normal n1 in T1 , i.e., to
a vertex of F1 . Regarding these rotations, a few comments are in order. As mentioned
previously, rotation by one-sided quaternionic multiplication is isoclinic, so that q rotates
in the n0 n1 -plane as well as in its dual plane. With respect to applying q on the left, we
have the following variations. Since q∗ q = 1, applying q∗ on the left is of course the inverse
rotation, giving the opposite rotation in both planes. Applying n0−1 qn0 = q on the right
may be called the n0 -converse of q; it gives the same rotation in the n0 n1 -plane, but the
opposite rotation in the dual plane. Applying n0−1 q∗ n0 = q∗ on the right might be called
the n0 -contraverse, giving the opposite rotation in the n0 n1 -plane, but the same rotation in
the dual plane. Thus,
n1 ≡ qn0

(13)

∗

q n1 = n0
qhq∗ ̸= h,

(14)
general quaternion h

qn0 q∗ = q∗ qn0 = n0 ,

special case n0 .

(15)
(16)

The converse and contraverse are defined with respect to a specific quaternion, here,
n0 ; in this case, they have particularly simple expressions, since n0 commutes with any q.
According to Theorem 1, left multiplication by q or q∗ preserves the 24-cell groupings
of the Fk , and so it will preserve their duals, Tk . This does not apply to right multiplication:
it still preserves the complete F, since that is the icosian group, but it may mix the 24-cells,
so it is not guaranteed to preserve their duals. Another way to think of this is to note that
since multiplication on the right preserves F as a vertex set, it preserves the 600 facets of
its convex hull as well, but the vertices of T are just a subset of that, and so they are not
necessarily preserved.
Since left multiplication by q takes n0 to n1 , and since it preserves the 24-cells, it will
also take C0 to C1 , the cuboctahedron in T1 normal to n1 ,
C1 = qC0 .

(17)

But q is precisely one of the two natural rotations we identified in Section 4—it is
isoclinic, and the n0 n1 -plane is one of its invariant planes, since qn0 = n0 q. And trivially,
its inverse is the natural rotation that takes n1 to n0 , and will take C1 to C0 ,
C0 = q∗ C1 .

(18)

Thus, if we rotate the 3D space of C1 to the target space V, the left-natural rotation
will take C1 exactly to C0 , and the same argument applies to any of the cuboctahedra we
choose in any of the 24-cells. Initially, thinking of rotating an arbitrary cuboctahedron of

## PDF page 9

Crystals 2024, 14, 194

9 of 16

one 24-cell into the 3D space of some cuboctahedron in another 24-cell, it was not at all
obvious that the two would end up exactly coinciding, but when viewed in light of the
isoclinic construction by r T and of Theorem 1, this becomes almost trivial.
We come now to the other natural rotation, the right-isoclinic one. Let
C1′ = C1 q∗ = qC0 q∗ .

(19)

Then, where is C1′ ? First, we know that this will live with C0 in V, since q∗ returns
n1 to n0 whether it acts on the right or the left. (Equivalently, one notes that two-sided
multiplication by a unit quaternion and its conjugate rotates vectors in the 3D space normal
to (1, 0, 0, 0).) Second, the angle of q is the angle between n1 and n0 ; these are two vertices
of the 600-cell F, and an exhaustive check of the angles between vertex vectors shows them
all to be multiples of either π5 , π3 , or π2 . The two-sided rotation by q and q∗ gives twice that
2π
angle, so it will be a multiple of 2π
5 , 3 , or π. These are the angles of icosahedral symmetry.
Indeed, since left and right multiplication preserve the vertices of F, it must preserve
their projection into V, which, as the vertex-first projection of a 600-cell, is icosahedrally
symmetric. Thus, C1′ will be a rotation of C0 around an icosahedral axis, either 5-fold, 3-fold,
or 2-fold, according as the rotation angle from n1 to n0 is 10-fold, 6-fold, or 4-fold.
What we see here is that the vertices of the original compound of five 24-cells project
as a facet-first 600-cell to tetrahedral symmetry (like the cuboctahedra), but that the facet
normals project as a vertex-first 600-cell, with icosahedral symmetry; and that the converse
isoclinic rotation which preserves the icosahedral symmetry of the facets must compound
the cuboctahedra vertices in the correct way to give them icosahedral symmetry as well.
Finally, we note that there are, for example, six axes of 5-fold symmetry, and so from
the above considerations, different cuboctahedra in T1 whose 3D spaces make mπ
5 angles
with V could, in principle, end up within V but in different orientations, rotated relative
to C0 around different 5-fold axes. However, this is not the case. According to Theorem 1,
with p some internal isoclinic symmetry of T0 ,
q = rT p

(20)

C1′ = qC0 q∗ = r T pC0 p∗ r T∗ .

(21)

But pC0 p∗ = C0 , since p preserves T0 , while the two-sided quaternion action preserves
n0 , and therefore also preserves the equator normal to n0 . The vertices of C0 will be
permuted, but the cuboctahedron as a whole is preserved. Hence,
C1′ = r T C0 r T∗ .

(22)

This is remarkable: C1′ does not actually depend on q, but only on r T , i.e., it does not
depend on the choice of cuboctahedron within T1 , but only on the fact that it comes from
T1 . Thus, all cuboctahedra of T1 , under their natural respective right-isoclinic rotations into
V, converge to the same cuboctahedron, just as they did under their respective left isoclinic
rotations. In the left case, they all converge to C0 , while in the right case, they converge to
some orientation rotated from C0 in an icosahedrally symmetric way. The same reasoning
applies to cuboctahedra of each of the Tk , with each being rotated by successive powers of
r T , so that the four final cuboctahedra, together with C0 , form the icosahedrally symmetric
compound of five cuboctahedra.
Figure 5 illustrates this, showing cuboctahedra from five different 24-cells rotated
into V with varying amounts of their respective dual rotations (parameterized by α). The
top and bottom rows show different arbitrary choices of initial cuboctahedra. One sees
that under the direct rotation of each cuboctahedron to the primary space V, with no dual
rotation (α = 0, Figure 5c), they combine into an irregular jumble, with no non-trivial
symmetry. Including each rotation’s dual, however, to make it isoclinic, one sees the
compounds converge to a single cuboctahedron (α = +1, left-isoclinic, Figure 5e) or to the
icosahedrally symmetric C5C (α = −1, right-isoclinic, Figure 5a). This happens irrespective

## PDF page 10

Crystals 2024, 14, 194

10 of 16

of which cuboctahedral equator is chosen from each 24-cell to begin with, as illustrated by
the two rows: under the direct rotations (Figure 5c) they are completely different, but under
the isoclinic rotations (Figure 5a,e) they become the same. A manipulable visualization of
this is available in the supplementary material.

(a) α = −1

(b) α = −0.96

(c) α = 0

(d) α = +0.94

(e) α = +1

Figure 5. Compounding of cuboctahedra to make a C5C, by isoclinic rotations in 4D from five
cuboctahedral equators in five respective 24-cells of the 600-cell (as a compound of five 24-cells).
The initial cuboctahedron within each 24-cell is chosen arbitrarily; the top and bottom rows here
show different choices. Each cuboctahedron is rotated directly into the 3-space V of the primary
cubodctahedron (also chosen arbitrarily), which is the space visualized in the images. In addition,
each is rotated in the dual plane (hence, entirely within V) by a fraction α of the direct rotation angle,
so that at α = ±1, the rotation becomes left(right)-isoclinic. At α = 0 (c), one sees an irregular jumble
of cuboctahedra which depends on the initial choice of 24-cell equators, but as α approaches ±1, they
approach their pristine positions, converging to either a single cuboctahedron (α = +1, (e)) or a C5C
(α = −1, (a)), independent of which initial cuboctahedron is chosen within each 24-cell. Manipulable
visualization is available in the supplementary materials.

From these considerations—the naturalness of the chosen rotations, and the independence of the outcome from the specific choice of initial cuboctahedra—we feel justified in
saying that the 600-cell, as a compound of five 24-cells, naturally induces the compounding of tetrahedral symmetries to icosahedral symmetry, as typified by the compound of
five cuboctahedra.
The C5C and the 20G
We have seen in the previous section that the ESQC induces the C5C, and have
elsewhere alluded to the connection between the C5C and the FIG’s 20G. To make this connection explicit, we first construct what we refer to as a 4-Group (4G). On a cuboctahedron,
following Figure 6, we select a disjoint set of four triangular faces (no shared vertices). We
then create four tetrahedra by joining each triangle vertex to the cuboctahedron’s centroid
and discarding cuboctahedron edges that do not belong to these tetrahedra. Since the
circumradius of the cuboctahedron equals its edge length, the tetrahedra are regular.
Now, to construct the 20G, one combines five of these 4Gs using the same compounding process used to create the C5C—see Figure 7, which follows the same process as
Figure 4 and yields a left-handed 20G. This process, as we have shown, comes from the
compounding of 24-cells to make up the 600-cell, which in turn comes from the 5-fold
fibration of 24-cells of the A group in the Gosset 421 . (Note that in Figure 6 one could
have chosen the alternate set of triangular faces to make the 4G; doing so would have
yielded the right-handed 20G seen in Figure 2b. The choice of which to call “left” and
“right’ is somewhat arbitrary here, but we note that if one points one’s left thumb along
the compounding axis in Figure 7, then one’s fingers wrap in the direction that appears to

## PDF page 11

Crystals 2024, 14, 194

11 of 16

follow the pointing of the nearest tetrahedral vertices, so we call this one “left”.) Since a
single 4G has the same convex hull as a single cuboctahedron (Figure 6), compounding it
5-fold in the same manner as the C5C yields a set of vertices with the same convex hull as
the C5C (Figure 8).

Figure 6. 4-Group (4G) of regular tetrahedra with shared vertex, constructed in a cuboctahedron.

Figure 7. Compounding of 4Gs by rotations in 3D to make the left-handed 20G. Successive images
include successive copies of the 4G, each rotated by an extra multiple of 2π
5 around a 5-fold axis
(cyan), which is the plane-normal identified in Figure 3. The last image is the full 20G, with chiral
icosahedral symmetry. Compare the compounding of cuboctahedra to create the C5C in Figure 4.

(a) 20G

(b) C5C

(c) Convex hull of both

Figure 8. The convex hull of the 20G is the same as that of the C5C. This is because the vertices of a
4G (aside from the centroid) are the same as those of a cuboctahedron (Figure 6).

6. Conclusions
We have shown how the root polytope of E8 , the Gosset 421 , contains two sets of 24-cell
fibers in 5-fold symmetry. This symmetry induces the ES space as the most symmetric
(with respect to this fibration) for projection, and the 24-cells of each set then project to a
respective 5-fold compound of 24-cells, with the vertices of a 600-cell, the core polytope
of the ESQC. Isoclinically rotating an arbitrarily chosen cuboctahedral equator from each
24-cell into the space of one cuboctahedron then naturally induces the 5-fold compounding
which creates the 20G, which is the core polytope of the FIG. Thus, there is a natural one-toone correspondence between the five group-A 24-cells in the Gosset 421 , the five 24-cells in a
600-cell, and the five 4Gs (or cuboctahedra) in a 20G (or cuboctahedron 5-compound), these
being the respective core polytopes of E8 , the ESQC, and the FIG. While it is well known
that E8 yields H3 symmetry via a direct projection method, we have now seen that it also
does so via a naturally induced compounding, which generates icosahedral quasicrystals
from its tetrahedral symmetries. The FIG can be understood from both viewpoints. (The
direct cut-and-project to this icosahedral symmetry is to be presented in another paper in
this series [32]).

## PDF page 12

Crystals 2024, 14, 194

12 of 16

Supplementary Materials: The following supporting information can be downloaded at: https://www.
mdpi.com/article/10.3390/cryst14020194/s1, Mathematica Notebook S1: “Gosset 4Gs to 20Gs.nb” (with
supporting packages). The notebook contains a manipulable visualization, and can be viewed using the
free Wolfram Player, https://www.wolfram.com/player/ (accessed on 9 February 2024).
Author Contributions: Initial conceptualization, K.I.; further conceptualization and initial investigation, F.F.; final conceptualization, investigation, and formal analysis, R.C.; software and visualization,
R.C.; writing, R.C.; supervision, F.F. All authors have read and agreed to the published version of
the manuscript.
Funding: This research received no external funding.
Data Availability Statement: Data are contained within the article and supplementary materials.
Acknowledgments: The authors would like to thank Raymond Aschheim and Dugan Hammock
for their valuable discussions and insights. Ray in particular first showed us the 5-fold rotation of
24-cells within the Gosset polytope.
Conflicts of Interest: The authors declare no conflicts of interest.

Abbreviations
The following abbreviations are used in this manuscript:
FIG
ES
ESQC
C5C
20G
4G

Fibonacci icosagrid quasicrystal.
Elser–Sloane.
Elser–Sloane quasicrystal.
Compound of five cuboctahedra.
20-Group; a group of 20 regular tetrahedra with one shared vertex, chirally twisted.
4-Group; a group of 4 regular tetrahedra with one shared vertex, tetrahedrally arranged.

Appendix A. Cuboctahedron’s 10-Fold Symmetry
The cuboctahedron contains a certain implicit 10-fold symmetry, which lies around
the axis that is used to create the compound of five cuboctahedra (C5C).
Appendix A.1. Description
In a regular cuboctahedron, we begin with a vector f from the origin through one of
the square face centers, and a plane containing this vector. Note where the plane intersects
the successive edges of the cuboctahedron, as illustrated in Figure A1 for a few plane
orientations. Then, we rotate the plane about f until the consecutive edge intersections
are equally spaced, as indicated in Figure A1c with the green dots. That spacing is then at
2π
angular intervals of 2π
10 . Moreover, f itself is also in the 10 spacing, with the unit vectors in
that plane heading toward the edges, and the square face centers form a complete decagon,
as shown in Figure A2.

## PDF page 13

Crystals 2024, 14, 194

13 of 16

f

f

f

f

c

(b)

(a)

(c)

(d)

Figure A1. Cuboctahedron with plane containing face-center vector f, rotated at different angles.
(a) Plane perpendicular to upper square edge, passing through vertex c. (b–d) As the plane is rotated
more and more, the intersection with the triangular face gets shorter, while the intersection with the
square face gets longer. In (c) it is at the balanced angle, such that the two are equal.

f
u
g
a

b
v
c

d

w
Plane P

Figure A2. Cuboctahedron with 10-fold symmetry plane P and decagonal set of vectors. P contains
the square-face-center vector f, as well as edge-intersection vectors u, v, and w (edge intersections
themselves are indicated by green dots). Vectors a, b, and c are vertices of a single triangular face,
while d and g are two of the vertices adjacent to that triangle.

Appendix A.2. Demonstration
Theorem A1. A plane containing a cuboctahedron’s 4-fold symmetry axis can be oriented so that
its intersections with the cuboctahedron edges, together with this axis, have decagonal symmetry,
lying at angular intervals of 2π
10 in the plane (Figure A2).
Proof. On a regular cuboctahedron, the vertex vectors of a single triangular face serve as a
basis for expressing the other vertices. Their linear combinations are also convenient for
constructing the 10 vectors of a regular decagon. Referring to Figure A2, we will use three
such vertices, a, b, and c, as well as vertices d and g adjacent to said triangle. Some very
basic elements of geometric algebra are used as a convenient algebraic tool for the proof
(see the work of Hestenes for an introduction), but the basic idea should be sufficiently
clear that one can follow it even without any knowledge of geometric algebra.
The vertex vectors to a triangular face are the edges of a regular tetrahedron, so they
make π3 angles with each other. Consequently, if we scale our cuboctahedron so the vertices
are unit vectors, then their mutual inner products are all 21 ,
a2 = b2 = c2 = 1

(A1)

a · b = b · c = a · c = 12 .

(A2)

## PDF page 14

Crystals 2024, 14, 194

14 of 16

Hence
ab = 2a · b − ba = 1 − ba

(A3)

and similarly for bc and ac.
Vector d in the figure is the inversion of b through the line of c, and likewise, g is the
inversion of c through b,
d = cbc = c(1 − cb) = c − b

(A4)

g = bcb = b(1 − bc) = b − c

(A5)

Let P be a plane containing the vector f. Define u, v, and w to be non-normalized
vectors in the directions of the respective intersections of P with successive edges of the
cuboctahedron, as indicated by the yellow dots in Figure. Then, u lies in the ab plane, v in
the ac plane, and w in the cd plane. Formally,
u = αa + βb

(A6)

v = δa + γc

(A7)

w = δd + γc

(A8)

for some non-negative scalars α, β, γ, and δ. Note that the symmetry of the way plane P
passes through the ac and dc edges ensures that the scalar coefficients on w are the same
as those on v, as shown. It is convenient to require u, v, and w to have the same norm,

(αa + βb)2 = (δa + γc)2
α2 + β2 + αβ = γ2 + δ2 + γδ,

(A9)

where we have made use of (A1). At this point, we do not specify what that norm should
be, so we have one free parameter.
The vectors u, v, and w all lie in plane P. As per the prescription in Appendix A.1
above, we now require that the angle from u to v is the same as that from v to w, or
u∧v = v∧w

(A10)

0 = v ∧ (u + w)

= (δa + γc) ∧ (αa + βb + δd + γc)
= (δa + γc) ∧ (αa + βb + δ(c − b) + γc)
= a ∧ b δ( β − δ) + c ∧ b γ( β − δ) + a ∧ c(δ2 + δγ − αγ).

(A11)

The three bivectors are linearly independent, so each must vanish separately. Moreover,
by inspection, we clearly see that for these angles to match, P cannot pass through the
vertices a, b, c, or d, so we assume forthwith that α, β, γ, and δ do not vanish. Together
with the non-negativity condition (after Equation (A6)), this means they are all positive.
Then, from the first two bivectors in (A11), β = δ. Before going on to the third bivector,
we substitute this into the norm equality (A9) and find
α2 + αβ = γ2 + γβ

(α + γ)(α − γ) = β(γ − α)
α = γ or α + γ = − β.

(A12)

The second solution is invalid, since α, β, and γ must be positive, so α = γ. This can
be substituted into the a ∧ c coefficient of (A11),
δ2 + δα − α2 = 0,

(A13)

## PDF page 15

Crystals 2024, 14, 194

15 of 16

or, letting α = µδ,
δ2 + µδ2 − µ2 δ2 = 0

(A14)

1 + µ = µ2 .

(A15)

√
This is the golden equation, whose positive solution is φ = 12 (1 + 5). We have found,
therefore, that β = δ and γ = α = φδ. Specifying our free parameter by choosing δ = 1, the
expressions (A6) for u, v, and w become
u = φa + b

(A16)

v = a + φc

(A17)

w = d + φc.

(A18)

The squared norm of these vectors is 1 + φ2 + ϕ = 2φ2 . Normalizing them, we can
find their angle,
cos θ =

u·v
( φa + b) · (a + φc)
=
2
2φ
2φ2

φ + 12 φ2 + 12 + 12 φ
φ + φ2
=
2
2φ
2φ2
φ
= ,
2

=

(A19)

or

2π
(A20)
10
where we have reduced the expression using the familiar properties of φ inherent in (A15).
′
The next step is√
to find the angle
√ θ between u and f = a + g. Note a · g = a · (b − c) =
1
1
2
2
a + g = 2. Then,
2 − 2 = 0, so | f | =
θ=

( φa + b) · (a + g)
u·f
cos θ ′ = √ √ =
2φ
2φ 2
1
1
φ+ 2 + 2
φ
=
=
2φ
2

(A21)
(A22)

or

2π
(A23)
10
where we have created another reduction using the golden properties of φ. Hence, the
normalized f, u, v, and w give consecutive vertices of a regular decagon, and based on the
symmetry of the construction, it is clear that the vectors directed toward the remaining face
center and edge intersections complete the decagon.
θ′ =

Remark A1. The 3-fold symmetries of H3 . A similar construction can be used to find new
3-fold symmetries. Of course, the cuboctahedron already has four axes of 3-fold symmetry—the face
normals of the triangular faces—but H3 has ten 3-fold axes. The other six can be found from the
cuboctahedron, just as the 5-fold axes were found. We begin the construction the same way, but
ignore the intersection of plane P with the first edge, between vertices a and b. We rotate P until
the angle between face center f and the edge ac intersection is the same as the angle between the
edge ac and edge dc intersections. The angle is then θ = π2 − θ/2, hence θ = π3 .
That plane of vectors is a new 3-fold symmetry plane, not for this cuboctahedron (which by
itself does not have icosahedral symmetry), but for the C5C of which this is a member.

## PDF page 16

Crystals 2024, 14, 194

16 of 16

References
1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.

18.
19.
20.
21.

22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.

Wang, H. Proving theorems by pattern recognition—II. Bell Syst. Tech. J. 1961, 40, 1–41. [CrossRef]
Berger, R. The Undecidability of the Domino Problem; Memoirs of the American Mathematical Society, American Mathematical
Society: Providence, RI, USA, 1966.
Penrose, R. Pentaplexity A Class of Non-Periodic Tilings of the Plane. Math. Intell. 1979, 2, 32–37. [CrossRef]
Levine, D.; Steinhardt, P.J. Quasicrystals: A new class of ordered structures. Phys. Rev. Lett. 1984, 53, 2477. [CrossRef]
Levine, D.; Steinhardt, P.J. Quasicrystals. I. Definition and structure. Phys. Rev. B 1986, 34, 596. [CrossRef] [PubMed]
Socolar, J.E.; Steinhardt, P.J. Quasicrystals. II. Unit-cell configurations. Phys. Rev. B 1986, 34, 617. [CrossRef] [PubMed]
Macià, E. Alloy Quasicrystals: Perspectives and Some Open Questions at Forty Years. Symmetry 2023, 15, 2139. [CrossRef]
Léonard, J. A kicked quasicrystal. Nat. Phys. 2024, 1–2. [CrossRef]
Shi, A.; Peng, Y.; Jiang, J.; Peng, Y.; Peng, P.; Chen, J.; Chen, H.; Wen, S.; Lin, X.; Gao, F.; et al. Observation of Topological Corner
State Arrays in Photonic Quasicrystals. Laser Photonics Rev. 2024, 2300956 [CrossRef]
Qiu, Z.; Nitta, M. Quasicrystals in QCD. J. High Energy Phys. 2023, 2023, 170. [CrossRef]
Koca, M.; Koca, N.O.; Al-Siyabi, A. SU(5) grand unified theory, its polytopes and 5-fold symmetric aperiodic tiling. Int. J. Geom.
Methods Mod. Phys. 2018, 15, 1850056, [CrossRef]
Boyle, L.; Dickens, M.; Flicker, F. Conformal Quasicrystals and Holography. Phys. Rev. X 2020, 10, 011009. [CrossRef]
Wang, Y.; Lu, Y.H.; Gao, J.; Sun, K.; Jiao, Z.Q.; Tang, H.; Jin, X.M. Quantum Topological Boundary States in Quasi-Crystals. Adv.
Mater. 2019, 31, 1905624, [CrossRef] [PubMed]
Gardiner, J. Biological quasicrystals and the golden mean: relevance to quantum computation. NeuroQuantology 2021, 19, 273–284.
[CrossRef]
Koç, R.; Haciibrahimoǧlu, M.Y.; Koca, M. Coxeter groups A4, B4 and D4 for two-qubit systems. Pramana 2013, 81, 247–260.
[CrossRef]
Macià, E. Aperiodic crystals in biology. J. Phys. Condens. Matter 2022, 34, 123001. [CrossRef] [PubMed]
Sahoo, D.; Peterca, M.; Imam, M.R.; Partridge, B.E.; Xiao, Q.; Percec, V. Conformationally flexible dendronized cyclotetraveratrylenes (CTTV)s self-organize a large diversity of chiral columnar, Frank-Kasper and quasicrystal phases. Giant 2022, 10, 100096.
[CrossRef]
Dechant, P.P.; Wardman, J.; Keef, T.; Twarock, R. Viruses and fullerenes—Symmetry as a common thread? Acta Crystallogr. Sect. A
2014, 70, 162–167. [CrossRef] [PubMed]
Baake, M.; Grimm, U. Aperiodic Order; Cambridge University Press: Cambridge, UK, 2013.
Boyle, L.; Steinhardt, P.J. Coxeter pairs, Ammann patterns, and Penrose-like tilings. Phys. Rev. B 2022, 106, 144113. [CrossRef]
Irwin, K.; Fang, F. An Icosahedral Quasicrystal and E8 Derived Quasicrystals. 2016. Eprint Article. Available online:
https://www.researchgate.net/publication/315553243_An_Icosahedral_Quasicrystal_and_E8_Derived_Quasicrystals (accessed
9 February 2024).
Fang, F.; Irwin, K. From the Fibonacci Icosagrid to E8 (Part I): The Fibonacci Icosagrid, an H3 Quasicrystal. Crystals 2024, 14.
[CrossRef]
Elser, V.; Sloane, N.J.A. A highly symmetric four-dimensional quasicrystal. J. Phys. A 1987, 20, 6161–6168. [CrossRef]
Sadoc, J.; Mosseri, R. The E8 lattice and quasicrystals. J. Non-Cryst. Solids 1993, 153, 247–252. [CrossRef]
Echeverría, J.; Casanova, D.; Llunell, M.; Alemany, P.; Alvarez, S. Molecules and crystals with both icosahedral and cubic
symmetry. Chem. Commun. 2008, 2717–2725. [CrossRef]
Fang, F.; Clawson, R.; Irwin, K. Closing Gaps in Geometrically Frustrated Symmetric Clusters: Local Equivalence between
Discrete Curvature and Twist Transformations. Mathematics 2018, 6, 89. [CrossRef]
Moody, R.V.; Patera, J. Quasicrystals and icosians. J. Phys. A Math. Gen. 1993, 26, 2829. [CrossRef]
Koca, M.; Koc, R.; Al-Barwani, M. Noncrystallographic Coxeter group H4 in E8. J. Phys. A Math. Gen. 2001, 34, 11201. [CrossRef]
Baez, J.C. From the Icosahedron to E8. arXiv 2017, arXiv:1712.06436.
Manton, N.S. Connections on discrete fibre bundles. Commun. Math. Phys. 1987, 113, 341–351. [CrossRef]
Skilling, J. Uniform compounds of uniform polyhedra. Math. Proc. Camb. Philos. Soc. 1976, 79, 447–457. [CrossRef]
Clawson, R.; Fang, F.; Irwin, K. From the Fibonacci Icosagrid to E8 (Part III): The direct cut-and-project mapping. Original research
article, Manuscript in Preparation for Publication.

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
