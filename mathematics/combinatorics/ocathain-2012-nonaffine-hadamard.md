Source: https://doras.dcu.ie/29113/1/NonaffineHadamard.pdf
PDF sha256: 9753fda50325ac57bdc98ab5bd18c669f7482771e93a2e8d7b8ae02934ab66db
License: https://creativecommons.org/licenses/by-nc-sa/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of ocathain-2012-nonaffine-hadamard.pdf

Transcription of `ocathain-2012-nonaffine-hadamard.pdf` in this directory, 20 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-20 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Difference sets and doubly transitive actions on
Hadamard matrices
Padraig Ó Catháin ∗
School of Mathematics, Statistics and Applied Mathematics,
National University of Ireland, Galway.

February 27, 2012

Abstract
Non-affine groups acting doubly transitively on a Hadamard matrix
have been classified by Ito. Implicit in this work is a list of Hadamard
matrices with non-affine doubly transitive automorphism group. We give
this list explicitly, in the process settling an old research problem of Ito
and Leon.
We then use our classification to show that the only cocyclic Hadamard
matrices developed from a difference set with non-affine automorphism
group are those that arise from the Paley Hadamard matrices.
If H is a cocyclic Hadamard matrix developed from a difference set
then the automorphism group of H is doubly transitive. We classify all
difference sets which give rise to Hadamard matrices with non-affine doubly transitive automorphism group. A key component of this is a complete
list of difference sets corresponding to the Paley Hadamard matrices. As
part of our classification we uncover a new triply infinite family of skewHadamard difference sets. To our knowledge, these are the first skewHadamard difference sets to be discovered in non-abelian p-groups with
no exponent restriction.
As one more application of our main classification, we show that Hall’s
sextic residue difference sets give rise to precisely one cocyclic Hadamard
matrix.

∗ E-mail: p.ocathain1@nuigalway.ie

1

## PDF page 2

1

Introduction

In [27], we showed that Hadamard matrices developed from twin prime power
difference sets are not cocyclic. In this paper we generalise that result to all
‘non-affine’ (4n−1, 2n−1, n−1)-difference sets. We call a (4n−1, 2n−1, n−1)difference set affine if the automorphism group of the corresponding Hadamard
matrix has a normal elementary abelian subgroup acting regularly on the rows
of the matrix. All necessary concepts will be introduced in Sections 2 and 3. In
this paper, we address the following problems:
• We extend work of Ito to give a classification of Hadamard matrices with
non-affine doubly transitive automorphism groups.
• We observe that the classification solves an old problem of Ito and Leon
from [18].
• For each matrix in the classification we determine all associated difference
sets. In the process we uncover a previously unknown triply infinite family
of skew difference sets. This is a step towards the solution of a research
problem of Jungnickel posed in [19].
In order to discuss this paper’s concerns in more detail, we recall some
elementary definitions and concepts.
Definition 1. We say that Hadamard matrices H and H are (Hadamard)
equivalent if there exist {±1}-monomial matrices P and Q such that P HQ⊤ =
H. The automorphism group of H, Aut(H), consists of all pairs (P, Q) of {±1}monomial matrices satisfying P HQ⊤ = H. An important subgroup of Aut(H)
is PermAut(H), which consists of the (P, Q) such that P and Q are permutation
matrices.
We deal with Hadamard matrices up to equivalence. That is, any claims of
uniqueness, classification etc. are made only up to equivalence.
The following will allow us to apply deep results from the theory of permutation groups to the study of Aut(H).
Definition 2. Let X be a {±1}-monomial matrix of order n. Then X has
a unique factorization DX EX where DX is a diagonal matrix and EX is a
permutation matrix. For a Hadamard matrix H, and (P, Q) ∈ Aut(H), define
ν(P, Q) = EP .
So each automorphism (P, Q) of a Hadamard matrix H induces a permutation of the rows of H. That is, ν is a homomorphism and gives a permutation
representation of Aut(H) in the symmetric group on the rows of H. For ease
of notation, we will refer to A(H) = ν(Aut(H)) as a permutation group on
{1, 2, . . . , n} where i represents the ith row of H. We use standard permutation
group terminology for A(H). Henceforth, when A(H) has a permutation group
property, we will say that Aut(H) has this property.

2

## PDF page 3

The literature on Hadamard matrices bears witness to extensive interest in
the study of various group actions on Hadamard matrices. Among these results
is the correspondence between (4n − 1, 2n − 1, n − 1)-difference sets and regular
actions on the rows and columns of the cores of Hadamard matrices (as in
Section 2). Another correspondence associates (4n, 2, 4n, 2n)-relative difference
sets to certain induced regular actions of subgroups of Aut(H) on the rows
and columns of H. Hadamard matrices supporting this latter type of action
are called cocyclic. In this paper we deal almost entirely with the permutation
action of A(H) on the rows of H, which is not the standard action considered
in the study of cocyclic Hadamard matrices.
Definition 3. Let G be a finite group. A binary (2-)cocycle is a map ψ :
G × G → ⟨−1⟩ which obeys the following identity for all g, h, k ∈ G.
ψ (g, h) ψ (gh, k) = ψ (g, hk) ψ (h, k)
An n × n Hadamard matrix H is cocyclic if there exists a group G of order n
and a cocycle ψ : G × G → ⟨−1⟩ such that
H = [ψ (g, h)]g,h∈G ,
where rows and columns of H are indexed by the elements of G. We say that
ψ is a cocycle of H, that H is cocyclic over G, and that the extension of ⟨−1⟩
by G determined by ψ is an extension group of H.
Cocyclic Hadamard matrices possess a rich algebraic theory. For basic results, we refer the reader to [14, 25, 6]. The only result on cocyclic Hadamard
matrices which will be used in later sections is that A(H) is transitive if H is
cocyclic (see Lemma 6 of [27]). A study of Hadamard matrices supporting the
structure of both a (4n, 2, 4n, 2n)-relative difference set and a (4n−1, 2n−1, n−
1)-difference set was the original motivation of this work.
An outline of the rest of the paper follows. We begin Section 2 by recalling some further necessary definitions and results from the study of Hadamard
matrices and symmetric 2-designs. In Section 3 we classify the Hadamard matrices H with A(H) non-affine doubly transitive. Then in the following sections
we will consider in turn cocyclic development for the matrices in our classification, and difference sets associated with the matrices in the classification. We
conclude the paper with two applications of the classification result of Section
3: we show that the Hadamard matrices developed from Hall’s sextic residue
difference sets are cocyclic in only one case, and we describe a new family of
skew-Hadamard difference sets. These are the only skew difference sets giving
rise to cocyclic Hadamard matrices.

2

Hadamard matrices and related combinatorial
structures

We recall now the relationships between Hadamard matrices, symmetric designs
and difference sets. Some of the material in this section is standard.
3

## PDF page 4

Definition 4. Let V = {p1 , p2 , . . . , pv } be a set of points and let B = {b1 , b2 , . . . , bv }
be a set of subsets of V (blocks) such that the following hold:
• |bi | = k,

1≤i≤v

• |bi ∩ bj | = λ, 1 ≤ i < j ≤ v.
Then S = (V, B) is a symmetric 2-(v, k, λ) design. Define χ : V × B → {0, 1}
by χ(pi , bj ) = 1 if and only if pi ∈ bj . An incidence matrix M of S has entry
χ(pi , bj ) in its ith row and j th column. That is,
M = [χ(pi , bj )]1≤i,j≤v .
Definition 5. Let S = (V, B) be a symmetric 2-(v, k, λ) design, and let G be
the symmetric group on V . Then G has an induced action on the k-subsets of
V . The setwise stabiliser of B is the automorphism group of S, Aut(S). Any
symmetric 2-design of the form S = (V, B g ) for some g ∈ G is equivalent to S.
Let M be an incidence matrix of S. Define Aut(M) to be the set of all pairs
(P, Q) of permutation matrices such that P MQ⊤ = M. It is easily seen that
Aut(M) and Aut(S) are isomorphic.
We will rely on the following result, which relates the action of Aut(S) on
points to its action on blocks.
Theorem 6 (Theorem III.4.1, [2]). Let S be a non-trivial symmetric design,
and let G ≤ Aut(S). Then the number of orbits of G on points is equal to the
number of orbits of G on blocks.
The following lemma is standard; see e.g. Lemma I.9.3 of [2].
Lemma 7. Let S be a symmetric 2-(4n − 1, 2n − 1, n − 1) design. Define J to
be the (4n − 1) × (4n − 1) all 1s matrix, and T to be 2M − J. Let 1 be the all
1s vector of length 4n − 1. Then
(
)
1
1
H=
⊤
1
T
is a Hadamard matrix.
Proof. First, we observe that MM⊤ = nI + (n − 1)J. It follows that
T T ⊤ = (2M − J)(2M⊤ − J)
= 4MM⊤ − 2MJ − 2JM⊤ + J 2
= 4(nI + (n − 1)J) − (4n − 2)J − (4n − 2)J + (4n − 1)J
= 4nI − J.
Thus, adding an initial row and column of +1s to T gives a Hadamard matrix.

4

## PDF page 5

Remark 8. So a Hadamard matrix of order 4n exists if a symmetric 2-(4n −
1, 2n − 1, n − 1) design exists. The converse is also true: one obtains an incidence matrix for a symmetric 2-(4n − 1, 2n − 1, n − 1) design from the core of a
normalised Hadamard matrix by replacing every occurrence of −1 by 0. Notice
that the equivalence class of a symmetric 2-(4n − 1, 2n − 1, n − 1) design corresponds to a unique equivalence class of Hadamard matrices via the construction
of Lemma 7. But the equivalence operations for 2-designs are finer than those
for Hadamard matrices. So a single equivalence class of Hadamard matrices can
give rise to many inequivalent 2-designs.
In the next few results we work towards a description of Aut(S) as a subgroup
of A(H).
Lemma 9. Let H be a Hadamard matrix. Then ν(PermAut(H)) ∼
= PermAut(H).
Proof. Note that Ker(ν) consists of automorphisms of H which are diagonal
in the first component. But a diagonal permutation matrix is trivial; hence
Ker(ν) ∩ PermAut(H) = 1. The lemma follows.
Doubly transitive actions on Hadamard matrices are a central concern of
this paper. We recall Burnside’s Theorem (see e.g. Theorem XI.7.12 of [15]):
a doubly transitive permutation group is either of affine type and contains an
elementary abelian normal subgroup acting regularly, or it is almost simple.
We restrict our classification results to the non-affine case. The affine case
requires methods different to those developed here and falls outside the scope
of this paper. The non-affine doubly transitive groups which act on Hadamard
matrices have been completely classified by Ito up to permutation isomorphism.
Theorem 10 (Ito, [16]). Let H be a Hadamard matrix such that A(H) is nonaffine and doubly transitive. Then the action of A(H) is one of the following.
• A(H) ∼
= M12 in its natural action on 12 points.
• PSL2 (pk ) ⊴ A(H) acting naturally on pk + 1 points, for pk ≡ 3 mod 4,
pk ̸= 3, 11.
• A(H) ∼
= Sp6 (2) acting on 36 points.
Now we can state our main result about the relationship between actions on
designs and actions on corresponding Hadamard matrices.
Theorem 11. Let S be a symmetric 2-(4n − 1, 2n − 1, n − 1) design, and let H
be the Hadamard matrix constructed from S as in Lemma 7. Then Aut(S) ∼
=
PermAut(H).
Suppose that Aut(S) is transitive on the points of S, and denote by G the
subgroup ν(PermAut(H)) of A(H). Then G is transitive on {2, . . . , 4n} and
exactly one of the following holds.
• G is the full stabiliser of a point in A(H).
• H is Sylvester.
5

## PDF page 6

• H is of order 12.
Proof. We extend (P, Q) ∈ Aut(S) to an automorphism
((
) (
))
1
0
1
0
,
⊤
⊤
0
P
0
Q
of H, which fixes the first row and column and acts as (P, Q) on the submatrix
T . Thus Aut(S) embeds in PermAut(H). In the other direction: (P, Q) ∈
PermAut(H) must fix the unique first row and first column of 1s, and hence
restricts to an automorphism of S. So PermAut(H) ∼
= Aut(S).
It is clear that every element of G ≤ A(H) fixes the first row of H. Now
suppose that Aut(S) is transitive on the points of S. Then by Lemma 9 and
the above, G is transitive on the remaining rows of H. We show that either G
is the full stabiliser A(H)1 of 1, or H is Sylvester or of order 12.
First, we define the group
K = ⟨EQ | (P, Q) ∈ Aut(H) and ν(P, Q) ∈ A(H)1 ⟩.
Clearly K contains a subgroup isomorphic to PermAut(H) which fixes the first
column. By Theorem 6, this group is transitive on the remaining columns. So
K is either intransitive, or doubly transitive on columns. From the definition
we see that K is a covering group of A(H)1 .
If K is intransitive, then for every automorphism (P, Q) of H such that
ν(P, Q) is in A(H)1 , EQ fixes the first column of H. Thus either (P, Q) or
(−P, −Q) ∈ PermAut(H). This implies that G = A(H)1 .
Now let K be doubly transitive. Suppose that K is almost simple. But
then K ≤ A(H ⊤ ) is doubly transitive on the rows of a Hadamard matrix and
Theorem 10 applies. We consider each case in turn. The point stabiliser of
PΣL2 (q) is a subgroup of AΓL1 (q), which cannot have a transitive action on
q + 1 points. So this case does not yield an example. The point stabiliser
of Sp6 (2) is S8 , but S8 has no doubly transitive permutation representation
on 36 points. Finally, the stabiliser of a point in M12 is M11 , which has an
induced 3-transitive action on 12 points. It can be verified that this is indeed
the action of K on the columns of the Hadamard matrix of order 12. Hence
Aut(S) ∼
= PSL2 (11) in this case, which is of index 144 in M12 .
Now suppose that K is an affine group acting doubly transitively on the rows
of H ⊤ , and the kernel of ν contains soc(K), which is regular on columns. Then
soc(K) is a transitive translation group (in the sense of [21]) on the 3-design
of H ⊤ , and hence H ⊤ ∼ H is a Sylvester Hadamard matrix by Theorem 8 of
[21].
Difference sets are also naturally related to symmetric 2-designs.
Definition 12. Let G be a group of order v, and let D be a k-subset of G.
Suppose that every non-trivial element of G may be represented in the form
di d−1
j in exactly λ different ways, for di , dj ∈ D. Then D is a (v, k, λ)-difference
σ
set in G. Two difference sets D and D in G are equivalent if D = gD for some
g ∈ G and σ ∈ Aut(G).
6

## PDF page 7

Theorem 13. Suppose G contains a (v, k, λ)-difference set D. Then there
exists a symmetric 2-(v, k, λ) design on which G acts regularly. Conversely, a
symmetric 2-(v, k, λ) design on which G acts regularly corresponds to a (v, k, λ)difference set in G.
Proof. Set V = {g | g ∈ G} and B = {Dg | g ∈ G}. Then S = (V, B) is a symmetric 2-(v, k, λ) design. The right regular action of G on V gives an embedding
of G into Aut(S) as a regular subgroup.
In the other direction, suppose that S is a symmetric 2-(v, k, λ) design with
G ≤ Aut(S) acting regularly. Identify the points of S with the elements of G.
Blocks of S become subsets of G. By Theorem 6, G acts regularly on blocks.
one finds ∣that all blocks are of the form b0 g −1 for some fixed block b0 . But
∣Then
∣b0 g −1 ∩ b0 h−1 ∣ = λ for arbitrary g, h ∈ G, g ̸= h−1 implies that xi x−1 = h−1 g
j
has precisely λ solutions with xi , xj ∈ b0 . So b0 is a (v, k, λ)-difference set in G
as required.
Remark 14. If S1 and S2 are equivalent designs and G acts regularly on S1 ,
then G acts regularly on S2 . Furthermore, any difference set in G obtained
from S1 via the construction of Theorem 13 is equivalent to a difference set
obtained in the same way from S2 . Conversely, equivalent difference sets give
rise to equivalent symmetric designs via the construction of Theorem 13.
Note that Aut(S) can contain many conjugacy classes of regular subgroups
which are isomorphic as abstract groups. Let Ri (i = 1, 2) be regular subgroups
of Aut(S), and let Di be the difference set in Ri constructed as in the proof of
Theorem 13. If R1 and R2 are Aut(S)-conjugate, then there is an isomorphism
α : R1 → R2 such that α(D1 ) is equivalent to D2 . Conversely, if R1 and
R2 are isomorphic but not Aut(S)-conjugate, then there need not be such an
isomorphism α.
Definition 15. Let H be a Hadamard matrix, D a difference set and S a
symmetric design. If D and S are related as in Theorem 13, then we say that
S underlies D, or that D is over S. If H is a Hadamard matrix related to S as
in Lemma 7, then we say that H is developed from S, or that S corresponds to
H. We use the same terminology for the relationship between D and H as for
S and H.
So by Lemma 9, (the first part of) Theorem 11, and Theorem 13, we see that
a (4n − 1, 2n − 1, n − 1)-difference set in a group G corresponds in a natural way
to a Hadamard matrix H such that G is isomorphic to a subgroup of A(H)1
acting regularly on {2, . . . , 4n}. For this reason, a difference set with parameters
(4n − 1, 2n − 1, n − 1) is called Hadamard.

3

Hadamard matrices with doubly transitive automorphism groups

The relevance of doubly transitive permutation groups to the subject matter of
this paper is further exemplified by the following lemma.
7

## PDF page 8

Theorem 16 (Cf. [27], Lemma 11). Let H be a Hadamard matrix developed
from a (4n − 1, 2n − 1, n − 1)-difference set as in Lemma 7 and Theorem 13.
Then A(H) is transitive if and only if A(H) is doubly transitive.
Proof. By Lemma 7 and Theorem 13, PermAut(H) fixes the first row and column of H, and acts transitively on the remaining rows. So by Lemma 9, A(H)1
is transitive on {2, . . . , 4n}. Thus if A(H) is transitive, then it is 2-transitive.
In light of Theorem 10, it is not difficult to list all Hadamard matrices H
with A(H) non-affine doubly transitive. We do so in the remainder of this
section.
Lemma 17 (M. Hall, [10]). All Hadamard matrices of order 12 are (Hadamard)
equivalent, and for any such matrix H, A(H) ∼
= M12 acting sharply 5-transitively.
The action of Sp6 (2) in Theorem 10 is not its natural action on a 6-dimensional
F2 -vector space; rather the stabiliser of a point is a maximal subgroup isomorphic to S8 . This is the only action of Sp6 (2) that we will consider. In this action,
S8 acts primitively on the 35 remaining points. In [18], Ito and Leon construct
a Hadamard matrix H of order 36 with A(H) ∼
= Sp6 (2), and conjecture that it
is the unique such Hadamard matrix. We now observe that this is the case.
Theorem 18. Suppose that H is a Hadamard matrix with A(H) ∼
= Sp6 (2) in
its doubly transitive action on 36 points. Then H is unique (up to Hadamard
equivalence).
Proof. By Lemma 1 of [17], Ker(ν) has order 2. Thus |Aut(H)| = 2 · |Sp6 (2)| =
2, 903, 040. Now see Tables 8 and 9 of [4], where an exhaustive computer search
shows that there is a unique Hadamard matrix of order 36 with automorphism
group of order 2, 903, 040.
Remark 19. Alternatively, we may argue as follows. It may be verified, for a
Hadamard matrix H of order n, that |A(H)1 : ν(PermAut(H))| divides n. So
the automorphism group of a symmetric 2-(35, 17, 8) design corresponding to H
will have index dividing 36 in S8 . Theorem 2 of [5] states that there are four
symmetric 2-(35, 17, 8) designs with automorphisms of order 7. One of these has
S8 as its automorphism group; the others have automorphism groups of order
at most 420. By Remark 8, this gives another proof of the uniqueness of H.
This resolves the two sporadic cases of Ito. We consider now the case that
PSL2 (pk ) acts on the rows of H.
Definition 20. Let q ≡ 3 mod 4 be a prime power. Then the quadratic
residues of Fq form a difference set in the additive group of Fq . Such a difference set is known as a Paley difference set. A Paley design is the underlying
symmetric 2-design of a Paley difference set, and a Paley Hadamard matrix is
a Hadamard matrix developed from a Paley difference set (these are generally
known as Type I Paley matrices.)

8

## PDF page 9

The Paley matrices are well studied. In particular, their automorphism
groups were determined by Kantor.
Theorem 21 ([20], [7]). Let H be a Paley Hadamard matrix of order pn + 1 >
12. Then Aut(H) is an extension of C2 by PΣL2 (pn ) (that is, PSL2 (pn ) extended
by field automorphisms).
Definition 22. Let q = pn for a prime p. Then AΓL1 (q) is the group of
semilinear transformations of Fq ; that is, transformations of the type x ↦→ axσ +b
for a ∈ F∗q , b ∈ Fq and σ ∈ Aut(Fq ), where we consider Fq as a field extension
of Fp . The group AGL1 (q) is a normal subgroup of AΓL1 (q), consisting of the
transformations of the form x ↦→ ax + b.
Theorem 23. Let H be a normalised Hadamard matrix of order q + 1, for
a prime power q ≡ 3 mod 4, q > 11. Then PSL2 (q) in its natural doubly
transitive action is a normal subgroup of A(H) if and only if H is equivalent to
a Paley Hadamard matrix.
Proof. Suppose that PSL2 (q) is a normal subgroup of A(H). Then the stabiliser
of a point in A(H) contains a subgroup of index 2 in AGL1 (q). This contains
a normal elementary abelian subgroup R of order q acting regularly on the
remaining points. It is clear that R fixes a point in its action on columns. Hence,
R is a regular subgroup of Aut(S), where S is a symmetric design corresponding
to H. Thus by Theorem 13, H is developed from a difference set D in R. We
show that D is necessarily of Paley type: this guarantees that H is equivalent
to a Paley Hadamard matrix by Remarks 8 and 14.
Consider A(H)1,2 , the stabiliser of a point in A(H)1 . This has two orbits on
the remaining rows, one labelled by quadratic residues and one by non-residues.
By Bruck’s characterisation of the multipliers of a difference set ([2], Definition
VI.2.1), we have that the quadratic residues are multipliers of D. Now, by
Lemma VI.2.5 of [2], there exists a translate of D fixed by every multiplier.
This translate either consists entirely of quadratic residues or of quadratic nonresidues. In either case D is equivalent to a Paley difference set.
Conversely, by Theorem 21, if H is of order q+1 > 12, and H is equivalent to
a Paley Hadamard matrix, it is clear by Theorem 21 that PSL2 (q) ⊴ A(H).
The previous results yield the following classification.
Corollary 24. H is a Hadamard matrix such that A(H) is non-affine doubly
transitive if and only if one of the following holds.
• H is of order 12.
• H is in the unique equivalence class of Hadamard matrices of order 36 on
which Sp6 (2) acts.
• H has order greater than 12 and is equivalent to a Paley Hadamard matrix.

9

## PDF page 10

Remark 25. The (Paley) Hadamard matrices of order less than 12 are excluded
from the list of Corollary 24 because their automorphism groups are affine doubly transitive rather than non-affine. Indeed, these matrices are equivalent to
Sylvester matrices.
We note that an unpublished paper [22] of Moorhouse classifies all complex
Hadamard matrices with doubly transitive automorphism groups. Our classification agrees with his in the special case considered here.

4

Cocyclic development

Theorem 16 implies that if H is a cocyclic Hadamard matrix developed from a
difference set, then A(H) is doubly transitive. In this short section, we describe
all the groups over which the Hadamard matrices of Corollary 24 are cocyclic.
This can be achieved for any Hadamard matrix H by classifying subgroups
of the permutation automorphism group which act regularly on the rows and
columns of the expanded matrix
(
)
1 −1
⊗H
−1
1
and contain the central involution (−I, −I). This turns out to be equivalent to
classifying regular subgroups of A(H) which possess some additional properties
(specifically, the preimage in Aut(H) of such a regular subgroup must project
onto a regular permutation group on the columns of H).
We consider the sporadic cases first. The next two results were obtained using the computational techniques developed in [25] from ideas due to de Launey.
Lemma 26 ([25], Section 5.3). A Hadamard matrix of order 12 is cocyclic
over the alternating group A4 , the dihedral group of order 12 and C2 × C6 , with
extension groups SL2 (3), C3 ⋊ Q8 and C3 × Q8 respectively.
The cocyclic Hadamard matrices of order 36 are classified in [26]. The
Hadamard matrix of Ito and Leon is not contained in the classification. In
fact the Paley Type II matrix is the only cocyclic Hadamard matrix at this
order with a non-solvable automorphism group.
Lemma 27. Let H be in the unique equivalence class of Hadamard matrices of
order 36 with A(H) ∼
= Sp6 (2). Then H is not cocyclic over any group.
This leaves only the Paley Hadamard matrices to consider. The groups over
which a Paley Hadamard matrix is cocyclic have been described by de Launey
and Stafford. This result is deep, and relies on detailed knowledge about the
finite near-fields, amongst other things.
Theorem 28 ([7], Section 5). Let H be a Paley Hadamard matrix of order q+1.
Then H is cocyclic over the dihedral group of order q +1, with dicyclic extension
group. There are additional extension groups only for q ∈ {3, 7, 11, 23, 59}.
10

## PDF page 11

The additional extensions in Theorem 28 are described in Section 5 of [7].
The matrices of orders 4, 8, 12 and 24 are also discussed in Chapter 5 of [25].
There is just one additional extension group for the Paley Hadamard matrix of
order 60, namely SL2 (5).
Corollary 29. Let H be a Hadamard matrix with A(H) non-affine doubly transitive. Then H is cocyclic if and only if either H is of order 12, or H is equivalent to a Paley Hadamard matrix. In both cases all groups over which H is
cocyclic and all extension groups for H are known.

5

A classification of (4n−1, 2n−1, n−1)-difference
sets with ‘transitive extensions’

In this section, we classify up to equivalence (in the sense of Definition 12) the
(4n−1, 2n−1, n−1)-difference sets which correspond to the Hadamard matrices
of Corollary 24.
Suppose that H is a Hadamard matrix such that A(H) is non-affine doubly
transitive. Let S be a symmetric 2 − (4n − 1, 2n − 1, n − 1) design underlying H.
We may assume (by Theorem 12) that Aut(S) is transitive, so that Aut(S) ∼
=
A(H)1 by Theorem 10, or H is of order 12. Then by Theorem 13, the difference
sets corresponding to H are in bijection with the regular subgroups of A(H)1 .
Note that we do not describe all difference sets in these groups (a listing of all
difference sets in elementary abelian groups is well beyond the bounds of existing
techniques!), but only those for which the corresponding Hadamard matrix H
has A(H) non-affine doubly transitive.
To summarise: for each of the doubly transitive groups identified by Ito,
we classify the regular subgroups of a point stabiliser on the remaining points.
We choose a representative from each conjugacy class of regular subgroups and
describe the difference sets in these groups which correspond to the Hadamard
matrices of Corollary 24.
Lemma 30. Suppose that H is a Hadamard matrix of order 12. Let S be a
symmetric design corresponding to H. Then Aut(S) has precisely one conjugacy
class of regular subgroups, each of which contains the Paley difference set of that
order.
Proof. The stabiliser of a point in M12 is the simple group M11 , but the automorphism group of S is PSL2 (11). This group has a unique conjugacy class
of regular subgroups. The First Multiplier Theorem (see Theorems VI.2.6 and
VI.2.11 of [2]) allows us to settle this case by hand. We are searching for an
(11, 5, 2)-difference set in Z11 , so 3 is a multiplier. That is, any difference set in
Z11 has a translate which is fixed by the automorphism x ↦→ 3x. The orbits of
this automorphism are {1, 3, 4, 5, 9}, {2, 6, 7, 8, 10} and {0}. But the first orbit
consists precisely of the quadratic residues of F11 , so is a Paley difference set.
The second orbit also forms a difference set, which is equivalent to the first
under the inversion automorphism.
11

## PDF page 12

It is easy to show that S8 does not contain a subgroup of order 35 (no element
of order 5 commutes with an element of order 7 in S8 ). Hence in its action on
35 points, S8 does not contain a regular subgroup.
Lemma 31. Suppose that H is a Hadamard matrix of order 36, and A(H) ∼
=
Sp6 (2) acting doubly transitively. Then H is not developed from any difference
set.
Remark 32. Lemmas 27 and 31 may be compared to [27, Theorem 10].
By Corollary 24, all that remains to be considered are the Paley Hadamard
matrices. Let H be the Paley Hadamard matrix of order q + 1. Then A(H) ∼
=
PΣL2 (q), by Theorem 21. Then by Theorem 11, we see that a symmetric 2design corresponding to the Paley Hadamard matrix of order q+1 has a subgroup
of index 2 in AΓL1 (q) as its automorphism group. Thus, our first task is to
classify the regular subgroups of this automorphism group. For convenience, we
now state the main results of our investigations.
Theorem 33. Let H be the Paley Hadamard matrix of order q +1. Express q as
pnp for a prime p, and n coprime to p. Then A(H)1 has e+1 conjugacy classes
of regular subgroups. One is normal and elementary abelian, the remainder are
t
non-normal, non-abelian of exponents p2p for 0 ≤ t ≤ e − 1.
The difference sets in the abelian regular subgroups are equivalent to the
Paley difference sets. A description of the non-abelian difference sets corresponding to the Paley Hadamard matrices is given in the proof of Lemma 46.
This will complete the description of all difference sets for which the corresponding Hadamard matrix H has A(H) non-affine doubly transitive.
Corollary 34. There exists a difference set corresponding to a Hadamard matrix H with A(H) non-affine doubly transitive if and only if H is a Paley
Hadamard matrix. All such difference sets are known.
The rest of this section is devoted to a proof of Theorem 33.

5.1

The regular subgroups of AΓL1 (q)

Let K/L be a Galois field extension of degree n, with Galois group G. Then
the Normal Basis Theorem states that there exists an element of ω of K such
that ω G is a basis for K as an L-vector space. Recall that extensions of finite
fields are always Galois, with cyclic Galois group.
We will consider Fq as a field extension of Fp for the moment. Extensions of
intermediate fields are obtained by replacing the Frobenius automorphism σ by
a suitable power, and will be considered later. We now determine the regular
subgroups of AΓL1 (q) in its natural action.
Lemma 35. Suppose that q = pn and p does not divide n. Then the only regular
subgroup of AΓL1 (q) is elementary abelian and normal.

12

## PDF page 13

Proof. The subgroup T consisting of the maps x ↦→ x + a for a ∈ Fq is a regular
normal subgroup of AΓL1 (q) and is easily seen to be elementary abelian. But a
Sylow p-subgroup of AΓL1 (q) is of order q; hence T is the unique subgroup of
order q in AΓL1 (q).
We consider now the case that q = pp . (The argument for the general case is
almost identical, and is given later.) In this case, a Sylow p-subgroup of AΓL1 (q)
has order pp+1 , and a regular subgroup has order pp . By the Normal Basis Theorem, we may consider Fq as an Fp -vector space V of dimension p, on which the
Frobenius automorphism σ acts by cyclic permutation of co-ordinates. We fix
some notation: {v1 , v2 , . . . , vp } is a basis for V , AΓL1 (q) = ⟨a1 , a2 , . . . , ap , β, σ⟩
where the action of each of the generators is given by
v a i = v + vi ,

v β = bv,

viσ = vi+1 ,

with subscripts interpreted modulo p, b is a primitive element of F∗q and the action of σ is extended linearly to all of V = Fq . The subgroup G = ⟨a1 , . . . , ap , σ⟩
is a Sylow p-subgroup of AΓL1 (q). We can determine a presentation of G with
relative ease:
G = ⟨a1 , . . . , ap , σ | api = σ p = 1, [ai , aj ] = 1, aσi = ai+1 , 1 ≤ i, j ≤ p⟩ .
Remark 36. We observe that the prime subfield of Fq is fixed by σ; it is the
subspace spanned by v1 + v2 + · · · + vp .
Lemma 37. A non-trivial element of G is either fixed-point-free, or is conjugate
to an element of ⟨σ⟩ and fixes p points.
Proof. The element σ centralises p2 elements of G (namely those of the form
ax1 · · · axp σ t ), so |NG (⟨σ⟩)| = p2 and the number of distinct conjugates of ⟨σ⟩ in
G is pp+1 /p2 = pp−1 . Now σ fixes the prime subfield, so a non-trivial element
in the union U of these conjugates fixes at least p points in V . Note that
|U | = pp−1 (p − 1) + 1. Since G is transitive on V , it then follows from the
Cauchy-Frobenius formula that each non-trivial element of U fixes precisely p
points, and that G \ U is the set of fixed-point-free elements of G.
Definition 38. Let E be a multiplicatively written elementary abelian group
of order pk , with fixed minimal generating set {e1 , . . . , ek }. Then the weight of
an element of E is given by
w(ex1 1 · · · exkk ) =

k
∑

xi

mod p (0 ≤ xi ≤ p − 1).

i=1

Definition 39. Each element g of G may be expressed uniquely in the form
aσ t for some a ∈ ⟨a1 , . . . , ap ⟩ and 0 ≤ t ≤ p − 1. Define the weight w(g) of g to
be w(a). Also define the class of g to be t.
Lemma 40. The weight and class of an element of G are invariant under
conjugation by G.
13

## PDF page 14

Proof. Each quantity is preserved under conjugation by the generators of G.
Lemma 41. All conjugates of σ have weight 0. Furthermore, an element of G
of weight zero is conjugate to σ t if and only if it has class t.
Proof. The first part is immediate from Lemma 40. For the second, it suffices
to show that an element of weight zero and class t is conjugate to σ t .
By Lemma 37, σ t has pp−1 conjugates. Each of these is an element of weight
zero and class t. But there are precisely pp−1 elements in G with this property.
The result follows.
By definition ⟨a1 , . . . , ap ⟩ acts transitively on V ; hence it is a regular subgroup of G. As the next theorem shows, this is the only abelian regular subgroup.
Theorem 42. Let q = pp . Then AΓL1 (q) has two conjugacy classes of regular subgroups. In particular, all non-abelian regular subgroups are AΓL1 (q)conjugate.
Proof. Consider the subgroup
Tk = ⟨ai σ k , 1 ≤ i ≤ p⟩
of G. Note that Tk is abelian if and only if k = 0. We claim that Tk = {aσ k·w(a) |
a ∈ T0 }. To see this, let g = aσ kt and h = bσ ks for a, b ∈ T0 have weights t, s
respectively; then
−kt
gh = aσ kt bσ ks = abσ σ k(t+s)
−kt

has weight w(a) + w(bσ ) = t + s and class k(t + s). Since Tk is generated
by elements of weight 1 and class k, this implies by induction that the class of
g ∈ Tk is k · w(g), as required.
We show that each Tk is a regular subgroup of G. Let g ∈ Tk , g ̸= 1.
If w(g) ̸= 0 then g is fixed-point-free by Lemmas 31 and 34. Suppose that
w(g) = 0. Then the class of g is zero by the previous paragraph. By Lemmas
31 and 35, we see once again that g is fixed-point-free. But Tk has order pp and
acts on a set of this size: it is regular.
In the next part of the proof we establish that the Tk are the only regular
subgroups of G. Since a regular subgroup R has index p in G, R must contain
the normal subgroup
−1
−1
K = ⟨a1 a−1
2 , a2 a3 , . . . , ap−1 ap ⟩

of G that lies in every Tk . Note that |K| = pp−1 , K consists of all elements of
p−1 i
weight 0 in T0 , and T0 = ∪i=0
a1 K. If R ̸= T0 then R = ⟨as1 σ t , K⟩ for some
s t
s rs
1 ≤ s, t ≤ p − 1. But a1 σ = a1 σ where r ≡ ts−1 mod p, so that R = Tr .
Now choose any r, 1 < r ≤ p − 1. Let c ≡ r−1 mod p. Then there exists
γ ∈ ⟨β⟩ such that v γ = cv for all v ∈ V . The equalities
viγσ = (cvi )σ = cviσ = c(viσ ) = viσγ
14

## PDF page 15

and
vγ

−1

ai γ

c

= (c−1 v + vi )γ = v + cvi = v ai

imply that σ γ = σ and aγi = aci . Therefore T1γ = ⟨aci σ, 1 ≤ i ≤ p⟩ = Tr .
Finally, since a regular subgroup of AΓL1 (q) is contained in some Sylow
p-subgroup, and (as we just showed) all non-abelian regular subgroups of the
Sylow p-subgroup G are conjugate, all non-abelian regular subgroups of AΓL1 (q)
are conjugate.
Corollary 43. Suppose that F is a field of characteristic p and that K is an
extension of F . Then AΓLF (K), the group of semilinear transformations of K
fixing F , contains one conjugacy class of regular subgroups for each power of p
dividing the degree of the extension (including p0 ).
Proof. In the case that K is an extension of degree mp where p ∤ m, it suffices
to consider K as an extension of degree p over a suitable intermediate field. The
argument of the previous theorem holds with minor modifications.
Now we consider field extensions of degree pa . Here we construct a tower of
extensions, each of degree p. It is then seen that one additional conjugacy class
of regular subgroups is obtained at each level of the tower.
We recall that the automorphism group of a symmetric Paley 2-design S is of
index 2 in AΓL1 (q). So its Sylow p-subgroups are the same as those of AΓL1 (q).
Thus the conjugacy classes of regular subgroups of Aut(S) are in bijection with
those of AΓL1 (q). This completes the proof of Theorem 33.

6

Application: Skew-Hadamard difference sets

−1
Definition 44. Let D be a (v, k, λ)-difference set in G. Then D−1
∣ = {d −1 ∣| d ∈
∣
D} is also a (v, k, λ)-difference set in G. We say that D is skew if D ∩ D ∣ = 0
and G = D ∪ D−1 ∪ {1}.

It is easily seen that all skew difference sets have parameters of the form (4n−
1, 2n−1, n−1). Thus the terms ‘skew’ and ‘skew-Hadamard’ are interchangeable
when referring to difference sets. Skewness is a strong condition to impose on a
difference set and it implies several non-existence results.
Theorem 45 ([1], Theorem 4.15). The only skew difference sets in cyclic groups
are the Paley difference sets in groups of prime order.
For many years the Paley difference sets were the only known examples of
skew difference sets, and it was conjectured that they were the only examples.
Recently Ding and Yuan [8] used Dickson polynomials to construct new skew
difference sets in the additive groups of F35 and F37 . They show that these difference sets are inequivalent to the Paley ones. They conjecture that their construction produces inequivalent difference sets for all elementary abelian groups
of order 32n+1 . This paper revitalised the study of skew-Hadamard difference
sets: recent results of Feng [9] give a construction for such difference sets in
15

## PDF page 16

non-abelian groups of order p3 . Muzychuk [24] goes even further: he shows that
there are exponentially many equivalence classes of skew-Hadamard difference
sets in elementary abelian groups of order q 3 . In this section we construct the
first triply infinite family of skew difference sets inequivalent to the Paley family.
These appear to be the first known skew difference sets in non-abelian p-groups
of unbounded exponent.
Lemma 46. The group T1 as defined in the proof of Theorem 42 contains a
Hadamard difference set.
Proof. Since T1 acts regularly on the Paley design, Theorem 13 guarantees the
existence of a Hadamard difference set in T1 .
We describe the difference set explicitly. Let D be a difference set in T0 (we
can take D to be the set of quadratic residues of Fpp ). Recall that T1 = {σ w(a) a |
a ∈ T0 }. Define D1 = {σ w(a) a | a ∈ D}. Now, σ normalises T1 . Hence, σ is
a multiplier of D1 (see Lemma V I.2.4 of [2]). So there exists a translate of D1
which consists of a union of orbits of σ on T1 .
p−1 i
Express this translate of D1 as D′ 1 = ∪i=0
σ Xi . Then since σ is weight
preserving, each Xi is a union of orbits of σ. This implies that
k

k

Xi Xj−1 = Xiσ (Xj−1 )σ = (Xi Xj−1 )σ

k

for any power k of σ. Then the multiset of quotients
{σ i−j (ab−1 )σ

−j

| σ i a, σ j b ∈ D′ 1 }

represents each element of T1 equally often, because D is a difference set. Thus
D1 is a difference set in T1 .
Remark 47. Any group Tk , as a conjugate of T1 , also contains a Hadamard
difference set.
One direction of the following lemma is stated in Remark VI.8.24 of [2].
Lemma 48. Let G be a group containing a difference set D, and let M be the
associated {±1}-matrix of D. That is,
M = [χ(gi gj−1 )]gi ,gj ∈G
where the ordering of the elements of G used to index rows and columns is the
same, and where χ(g) = 1 if and only if g ∈ D. Then M + I is skew-symmetric
if and only if D is skew-Hadamard.
Proof. Suppose that (M + I)⊤ = −M − I. Then the elements of D are precisely
those for which χ(gi 1−1 ) = 1 (i.e. they correspond to positive entries in the
first row of M ). But by skew-symmetry of M + I we obtain that χ(1gi−1 ) =
−χ(gi 1−1 ), so that gi ∈ D if and only if gi−1 ∈
/ D. Hence D is skew as required.
In the other direction, observe that
[
]⊤
[
]
[
]
M ⊤ = χ(gi gj−1 ) g ,g ∈G = χ(gj gi−1 ) gi ,gj ∈G = χ((gi gj−1 )−1 ) g ,g ∈G .
i

j

i

So if D is skew-Hadamard then (M + I)⊤ = −M − I.
16

j

## PDF page 17

Theorem 49. The group T1 contains a skew-Hadamard difference set.
Proof. Since the Paley Hadamard matrices are skew, this follows from Lemmas
46 and 48.
Thus Theorem 49 furnishes a family of skew non-abelian difference sets in
e
groups of order pnp for any prime p ≡ 3 mod 4, n odd and coprime to p, and
e ≥ 1. These difference sets have not previously appeared in the literature.
To conclude this section, we observe that there are no other skew-Hadamard
difference sets for which the corresponding Hadamard matrix has a doubly transitive automorphism group.
Theorem 50. Let H be a Hadamard matrix of order greater than 8 with affine
doubly transitive automorphism group. Then H is not developed from a skewHadamard difference set.
Proof. First, suppose that H is developed from a skew-Hadamard difference
set. Then by Lemma 48, the incidence matrix for the underlying 2-design is
skew; hence any difference set corresponding to H will be equivalent to a skew
difference set.
H has order 2n for some n, and by a result of Moorhouse [22] is equivalent to
the Sylvester matrix of that order. It is well known that the underlying 2-design
S of a Sylvester Hadamard matrix is isomorphic to the point-hyperplane design
of projective n-space over F2 . Thus the automorphism group of S contains a
regular cyclic subgroup (a Singer cycle).
But if H is developed from a cyclic skew difference set then H is equivalent
to a Paley matrix, by Theorem 45. It is well known that the Paley and Sylvester
series of matrices coincide only at orders 4 and 8.
Corollary 51. Let D be a skew difference set, and H the Hadamard matrix
developed from D. Then A(H) is doubly transitive if and only if H is equivalent
to a Paley Hadamard matrix.

7

Application: Hall’s sextic residues

We use our classification of Hadamard matrices with non-affine doubly transitive
automorphism group to establish necessary and sufficient conditions for a Hall
difference set to correspond to a cocyclic Hadamard matrix.
Definition 52. Let p be a prime of the form 4n − 1 = x2 + 27 for some positive
integer x (there are no non-trivial prime powers of this form). Let F be a field
of size p, and denote by C the multiplicative group of F. Let U be the unique
subgroup of index 6 in C and denote by µ a preimage in Fp of a generator of
p−3
C/U . Then U ∪ µU ∪ µ3 U is a (p, p−1
2 , 4 ) difference set in F, which we call
a Hall difference set. The elements of this difference set are generally known as
Hall’s sextic residues.

17

## PDF page 18

Theorem 11.6.7 of [11] proves the existence of these difference sets, and
characterises them, together with the Paley difference sets, as the only ones
having the sextic residues as multipliers.
We will require the following result, claimed by Ramanujan, and later proved
by (among others) Mordell.
Theorem 53 ([23]). The only solutions of the Diophantine equation 2n = x2 +7
are n = 3, 4, 5, 7, 15.
A Hall matrix is a Hadamard matrix developed from a Hall difference set.
Theorem 54. Suppose that H is a Hall matrix of order t. Then H is cocyclic
if t = 32, and possibly if t = 131072, but not otherwise.
Proof. Suppose that H is cocyclic. By Theorem 16, A(H) is doubly transitive.
We begin with the affine case. By Theorem 53, the only solutions to the
equation 2n = 4x2 + 28 occur when n ∈ {5, 6, 7, 9, 17}. But of these values of
n, the only ones such that 2n − 1 is prime are n ∈ {5, 7, 17}. A computation in
Magma [3] reveals that the Hall matrix of order 32 is equivalent to the Sylvester
matrix of that order, and so is cocyclic (see Section 6.4.1 of [14]). Again, by
direct computation, the Hall matrix of order 128 does not have a transitive
automorphism group, and so is not cocyclic.
In the non-affine case, Theorem 33 and Corollary 34 imply that H is cocyclic
only if a Hall difference set corresponding to H is equivalent to a Paley difference
set. This does not occur (see Remark VI.8.4 of [2]).
We conclude with an application of the classification of doubly transitive
permutation groups to settle the remaining order 217 in Theorem 54.
Lemma 55. The Hall matrix H of order 131072 is not cocyclic.
Proof. First, we prove that A(H) is non-solvable. By Theorem 11.6.7 of [11],
the 6th powers in F217 −1 are multipliers of the difference set. Thus PermAut(H)
17
contains a subgroup of order 2 6−2 . Lemma 9 then implies that A(H) contains a
subgroup of this order. By Theorem XII.7.3 of [15], a solvable doubly transitive
group of degree 217 is a subgroup of AΓL1 (217 ). But this has order 17(217 )(217 −
17
1), and so cannot contain a subgroup of order 2 6−2 .
So the automorphism group of H is non-solvable. Hering has classified the
non-solvable affine doubly transitive groups (a list is given in Section 5 of [12] and
proved to be exhaustive in [13]). There are only three infinite families of doubly
transitive affine groups, and two of these are easily dispatched: both G2 (q)
and Sp2n (q) act on even dimensional vector spaces. Thus if A(H) is doubly
transitive then A(H)1 contains SL17 (2) as a normal subgroup. Recall that
SLn (2) ∼
= PGLn (2) is itself doubly transitive. Hence as a transitive extension
of A(H)1 , A(H) is triply transitive. But by Proposition 2 of [17], a Hadamard
matrix with triply transitive automorphism group is equivalent to a Sylvester
Hadamard matrix. All Singer subgroups of PSL17 (2) are conjugate, but this
yields a contradiction of Remark VI.8.4 of [2].
18

## PDF page 19

Acknowledgments
The author would like to thank Dr Dane Flannery and Dr Richard M Stafford
for their advice and support.

References
[1] Leonard D. Baumert. Cyclic difference sets. Lecture Notes in
Mathematics, Vol. 182. Springer-Verlag, Berlin, 1971.
[2] Thomas Beth, Dieter Jungnickel, and Hanfried Lenz. Design theory. Vol.
I, volume 69 of Encyclopedia of Mathematics and its Applications.
Cambridge University Press, Cambridge, second edition, 1999.
[3] W. Bosma, J. Cannon, and C. Playoust. The Magma algebra system. I.
the user language. J. of Symbolic Comput., 24:235–265, 1997.
[4] Iliya Bouyukliev, Veerle Fack, and Joost Winne. 2-(31,15,7), 2-(35,17,8)
and 2-(36,15,6) designs with automorphisms of odd prime order, and their
related Hadamard matrices and codes. Des. Codes Cryptogr.,
51(2):105–122, 2009.
[5] Dean Crnković and Sanja Rukavina. On Hadamard (35, 17, 8) designs and
their automorphism groups. J. Appl. Algebra Discrete Struct.,
1(3):165–180, 2003.
[6] Warwick de Launey and Dane Flannery. Algebraic Design Theory.
Mathematical Surveys and Monographs, vol. 175. American Mathematical
Society, Providence, RI, 2011.
[7] Warwick de Launey and Richard M. Stafford. On cocyclic weighing
matrices and the regular group actions of certain Paley matrices. Discrete
Appl. Math., 102(1-2):63–101, 2000. Coding, cryptography and computer
security (Lethbridge, AB, 1998).
[8] Cunsheng Ding and Jin Yuan. A family of skew Hadamard difference sets.
J. Combin. Theory Ser. A, 113(7):1526–1535, 2006.
[9] Tao Feng. Non-abelian skew Hadamard difference sets fixed by a
prescribed automorphism. J. Combin. Theory Ser. A, 118(1):27–36, 2011.
[10] Marshall Hall, Jr. Note on the Mathieu group M12 . Arch. Math. (Basel),
13:334–340, 1962.
[11] Marshall Hall, Jr. Combinatorial theory. Wiley-Interscience Series in
Discrete Mathematics. John Wiley & Sons Inc., New York, second
edition, 1986.

19

## PDF page 20

[12] Christoph Hering. Transitive linear groups and linear groups which
contain irreducible subgroups of prime order. Geometriae Dedicata,
2:425–460, 1974.
[13] Christoph Hering. Transitive linear groups and linear groups which
contain irreducible subgroups of prime order. II. J. Algebra,
93(1):151–164, 1985.
[14] K. J. Horadam. Hadamard matrices and their applications. Princeton
University Press, Princeton, NJ, 2007.
[15] Bertram Huppert and Norman Blackburn. Finite groups. III, volume 243
of Grundlehren der Mathematischen Wissenschaften [Fundamental
Principles of Mathematical Sciences]. Springer-Verlag, Berlin, 1982.
[16] Noboru Ito. Hadamard matrices with “doubly transitive” automorphism
groups. Arch. Math. (Basel), 35(1-2):100–111, 1980.
[17] Noboru Ito and Hiroshi Kimura. Studies on Hadamard matrices with
“2-transitive” automorphism groups. J. Math. Soc. Japan, 36(1):63–73,
1984.
[18] Noboru Ito and Jeffrey S. Leon. An Hadamard matrix of order 36. J.
Combin. Theory Ser. A, 34(2):244–247, 1983.
[19] Dieter Jungnickel. Difference sets. In Contemporary design theory,
Wiley-Intersci. Ser. Discrete Math. Optim., pages 241–324. Wiley, New
York, 1992.
[20] William M. Kantor. Automorphism groups of Hadamard matrices. J.
Comb. Theory, 6:279–281, 1969.
[21] Marion E. Kimberley. On collineations of Hadamard designs. J. London
Math. Soc. (2), 6:713–724, 1973.
[22] G. Eric Moorhouse. The 2-transitive complex Hadamard matrices.
Preprint. http://www.uwyo.edu/moorhouse/pub/complex.pdf.
[23] L. J. Mordell. The diophantine equations 2n = x2 + 7. Ark. Mat.,
4:455–460, 1962.
[24] Mikhail Muzychuk. On skew Hadamard difference sets. Arxiv.net,
1012.2089v1, 2010.
[25] Padraig Ó Catháin. Group Actions on Hadamard matrices. M. Litt.
thesis, National University of Ireland, Galway, 2008.
[26] Padraig Ó Catháin and Marc Röder. The cocyclic Hadamard matrices of
order less than 40. Des. Codes Cryptogr., 58(1):73–88, 2011.
[27] Padraig Ó Catháin and Richard M. Stafford. On twin prime power
Hadamard matrices. Cryptogr. Commun., 2(2):261–269, 2010.

20
