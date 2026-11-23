Source: https://eisenbud.github.io/papers/pdfs/2024-001.pdf
PDF sha256: 6666098048874c50263f0faf7f4612399f789ee2f5079cc6cba1b6d4c3148c6a
License: CC-BY-SA-4.0
Language: eng
Fidelity: machine (failed: text-layer, display-math, repetition)

# Transcription of eisenbud_2024_hyperelliptic_curves_ulrich_sheaves_complete_intersection_two_quadrics.pdf

Transcription of `eisenbud_2024_hyperelliptic_curves_ulrich_sheaves_complete_intersection_two_quadrics.pdf` in this directory, 25 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

# **Hyperelliptic Curves and Ulrich sheaves on the complete intersection of two quadrics**

## **David Eisenbud and Frank-Olaf Schreyer**

*For Claire Voisin on the occasion of her Birthday*

**Abstract.** Using the connection between hyperelliptic curves, Clifford algebras, and smooth complete intersections *X* of two quadrics, we describe Ulrich bundles on *X* and construct some of minimal possible rank.

**Keywords.** Free resolutions, complete intersections, quadrics, Ulrich bundles, Ulrich modules, Clifford algebras

**2020 Mathematics Subject Classification.** 14J45,13D02, 13C14, 15A66, 11E88, 16D90

Received by the Editors on December 15, 2022, and in final form on May 21, 2024. Accepted on January 3, 2025.

David Eisenbud

Department of Mathematics, University of California at Berkeley and the Mathematical Sciences Research Institute, Berkeley, CA 94720, USA

*e-mail:* de@msri.org

Frank-Olaf Schreyer

Fachbereich Mathematik, Universität des Saarlandes, Campus E2 4, D-66123 Saarbrücken, Germany *e-mail:* schreyer@math.uni-sb.de

The first author was partially supported by NSF grant 2001649. This work is also a contribution to Project-ID 286237555 – TRR 195 – by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) of the second author. Part of the work was done while the authors were supported by the Simons Laufer Mathematical Sciences Institute.

## PDF page 2

## **Contents**

| 1.         | Introduction                                                                   | • | • | • | • | • | • | • | • | • | 2  |
|------------|--------------------------------------------------------------------------------|---|---|---|---|---|---|---|---|---|----|
| 2.         | Vector Bundles over a hyperelliptic curve $\emph{via}$ matrix factorizations . |   |   |   |   |   |   |   |   |   | 4  |
| 3.         | BGG for complete intersections of quadrics                                     |   |   |   |   |   |   |   |   |   | 6  |
| 4.         | Pencils of quadrics and hyperelliptic curves                                   |   |   |   |   |   |   |   |   |   | 9  |
| <b>5</b> . | Tate resolutions of $P_X$ -modules from Clifford modules                       |   |   |   |   |   |   |   |   |   | 13 |
| 6.         | Ulrich bundles of rank $2^{g-1}$                                               |   |   |   |   |   |   |   |   |   | 20 |
| D.         | forences                                                                       |   |   |   |   |   |   |   |   |   | 93 |

## 1. Introduction

Let k be an algebraically closed field of characteristic not 2. The periodicity theorem of Knörrer [Knö87] shows that the indecomposable Ulrich bundles on a smooth quadric hypersurface in  $\mathbb{P}^{2g+1}$  over k have rank  $2^{g-1}$ . In this paper we construct Ulrich bundles of the same rank  $2^{g-1}$  on every smooth complete intersection X of 2 quadrics in  $\mathbb{P}^{2g+1}$ , and we show that every Ulrich bundle has rank of the form  $r2^{g-2}$  where  $r \ge 2$  and rg is even. To prove this we use an equivalence of categories that extends Reid's famous description of the Jacobian of a hyperelliptic curve [Rei72].

Let  $X \subset \mathbb{P}^n$  be a projective scheme with homogenous coordinate ring  $P_X$ . Recall that a sheaf  $\mathcal{E}$  on X is called Ulrich if the graded module of twisted global sections  $H^0_*(\mathcal{E})$  is a maximal Cohen-Macaulay  $P_X$ -module generated in degree 0 and having linear free resolution over the coordinate ring of  $\mathbb{P}^n$ , or equivalently if  $H^i(\mathcal{E}(m)) = 0$  for all m with  $-1 \ge m \ge -\dim X$  and all i. See [ES03] for further information and examples.

Let X be the smooth complete intersection defined by two quadratic forms  $q_1, q_2$  on  $\mathbb{P}^{2g+1}$  over an algebraically closed field k of characteristic not 2.

The pencil of quadrics  $sq_1 + tq_2$ ,  $(s,t) \in \mathbb{P}^1$  becomes singular at 2g + 2 points of  $\mathbb{P}^1$ . Let E be the hyperelliptic curve with homogeneous coordinate ring  $k[s,t,y]/(y^2-f)$  branched over these points, and let E be the  $\mathbb{Z}$ -graded Clifford algebra of the form  $sq_1 + tq_2$  over k[s,t].

We give two approaches to the construction of Ulrich sheaves on X. The first makes use of three categories:

- (i) the category of coherent sheaves on E,
- (ii) the category of graded C-modules, and
- (iii) the category of coherent sheaves on X.

Categories (i) and (ii) are related by Morita equivalence, while categories (ii) and (iii) are related by a version of the Bernstein-Gel'fand-Gel'fand correspondence.

Composing these correspondences to go from (i) to (iii), we show that every Ulrich module on X has rank  $r2^{g-2}$  for some integer  $r \ge 2$ .

Following [FL10] we say that a bundle  $\mathcal{B}$  on E has the *Raynaud property* if  $H^0(C,\mathcal{B}) = H^1(C,\mathcal{B}) = 0$ . We use the fact that the center of the even Clifford algebra is the homogeneous coordinate ring of E, and that the category of coherent sheaves of modules over the sheafified even Clifford algebra  $\mathcal{C}^{\text{ev}} \cong \mathcal{E}nd_E(\mathcal{F}_U)$  is Morita equivalent to the category of coherent sheaves on E via an  $\mathcal{O}_E - \mathcal{C}^{\text{ev}}$  bundle  $\mathcal{F}_U$  defined in Section 4. With this notation, our first main theorem is the following.

## PDF page 3

**Theorem 1.1.** There is a 1-1 correspondence between Ulrich bundles on the smooth complete intersection of two quadrics  $X \subset \mathbb{P}^{2g+1}$  and bundles of the form  $\mathcal{G} \otimes \mathcal{F}_U$  with the Raynaud property on the corresponding hyperelliptic curve E. The Ulrich bundle corresponding to a rank r vector bundle  $\mathcal{G}$  has rank  $r2^{g-2}$ .

If  $\mathcal{L}$  is a line bundle on E then  $\mathcal{L} \otimes \mathcal{F}_U$  does not have the Raynaud property, so the minimal possible rank of an Ulrich sheaf on X is  $2^{g-1}$ , and Ulrich bundles of rank  $2^{g-1}$  exist.

The set of bundles  $\mathcal{G}$  such that  $\mathcal{G} \otimes \mathcal{F}_U$  has the Raynaud property forms a (possibly empty) open subset in any flat family of rank r vector bundles on E. Our second main theorem, the existence statement for r=2 is proven using a previously undiscovered property of Knörrer's matrix factorizations to give a construction of an Ulrich sheaf of the minimal possible rank,  $2^{g-1}$  on any smooth complete intersection of two quadrics in  $\mathbb{P}^{2g+1}$  and in  $\mathbb{P}^{2g+2}$ .

Based on computed examples using our package [EKS22] with Yeongrak Kim, we conjecture the following.

**Conjecture 1.2.** There exist indecomposable Ulrich bundles of rank  $r2^{g-2}$  on every smooth complete intersection of two quadrics in  $\mathbb{P}^{2g+1}$  for  $g \ge 1$  and  $r \ge 2$  if and only if  $rg \equiv 0 \mod 2$ .

By Proposition 5.11 the condition is necessary.

In Section 2 we explain the description of vector bundles on *E* in terms of matrix factorizations. In the case of line bundles, this theory can be traced through Mumford's [Mum84] to work of Jacobi [Jac46].

In Section 3 we explain the relation of categories (ii) and (iii), a form of the Bernstein–Gel'fand–Gel'fand (BGG) correspondence that holds for all complete intersections of quadrics. As far as we know this correspondence was first introduced in [BEH87], and greatly extended in [Kap89]. For the reader's convenience we review the results that we will use.

In Section 4 we establish the Morita equivalence between categories (i) and (ii). In fact every maximal (simultaneous) isotropic plane U for  $q_1$  and  $q_2$  gives rise to a Morita bundle  $\mathcal{F}_U$  and any two differ by the tensor product with a line bundle on E. This explains the well-known result of Miles Reid's thesis that the space of maximal (simultaneous) isotropic planes for  $q_1$  and  $q_2$  can be identified with the Jacobian of E.

In Section 5 we put these tools together with the theory of Tate resolutions and maximal Cohen–Macaulay approximations to establish the equivalence between Ulrich modules of rank  $r2^{g-2}$  on X and vector bundles of rank r on E that satisfy certain cohomological conditions. We show that no line bundles on E satisfy the conditions, establishing the lower bound for the rank of Ulrich modules announced above. This section was inspired by Buchweitz's famously unpublished manuscript on Koszul duality from 1986, now available at [Buc21] and by the theory of Cohen–Macaulay approximations by Auslander and Buchweitz [AB89].

It is natural to look for Ulrich bundles on X using the shape of their Tate resolutions over  $P_X$ . Theorem 5.5 is analogous to the main result on Tate resolution of coherent sheaves on  $\mathbb{P}^n$  in [EFS03]: the Betti table of the Tate resolution over the exterior algebra coincides with cohomology tables of the corresponding sheaf. In Theorem 5.5 the resolution over the exterior algebra is replaced by the Tate resolution over  $P_X$ .

In Section 6, which is independent of the rest of the paper, we give a direct construction of Ulrich modules of rank  $2^{g-1}$  on any smooth complete intersection of quadrics in  $\mathbb{P}^{2g+1}$  and  $\mathbb{P}^{2g+2}$  with the minimal possible rank,  $2^{g-1}$ . In the case g=2 the existence and minimality was established by [CKL21] with a different method.

## Historical remarks

The study of complete intersections of quadrics has a long history. The connection to vector bundles was discovered by Newstead [New68], Reid [Rei72] and Desale–Ramanan [DR76] in the 1970's. The connection with Clifford algebras and Koszul pairs was used in [BEH87] and more generally by Kapranov [Kap89] in the 1980's.

The first three sections of the paper, which take the point of view of matrix factorizations, have their roots in an unpublished manuscript by our dear friend Ragnar Buchweitz (1952–2017) and the second author

## PDF page 4

in 90's, now lost. The referee kindly pointed out to us that parts of Theorem 5.10 can be deduced from Kuznetsov's work [Kuz08], which, like the work of Kapranov [Kap89] instead takes the point of view of derived categories.

The theory of quadratic complete intersections has many guises, and appears in descriptions of certain completely integrable systems, for example in the recent paper of Claire Voisin and her coauthors [BEH<sup>+</sup>24].

## Acknowledgements

We are grateful to the referees for their many constructive comments. This paper would have been impossible without the program Macaulay2 [GS]. We thank Yeongrak Kim for working with us on the associated Macaulay2 package, distributed with the Macaulay2 program.

## 2. Vector Bundles over a hyperelliptic curve via matrix factorizations

Let E be a hyperelliptic curve of genus g and let  $\pi: E \to \mathbb{P}^1$  its double cover of  $\mathbb{P}^1$ . Let  $\mathcal{H} = \pi^* \mathcal{O}_{\mathbb{P}^1}(1)$  and let f(s,t) be the homogeneous polynomial of degree 2g+2 such that

$$R_E := k[s,t,y]/(y^2 - f) = \bigoplus_n H^0(E,\mathcal{H}^{\otimes n}),$$

so that the roots of f are the ramification points of  $\pi$  and  $y \in H^0(E, \mathcal{H}^{\otimes g+1})$ .

For a coherent sheaf G on E we denote by

$$H^i_*(\mathcal{G}) = \bigoplus_n H^i(E, \mathcal{G} \otimes \mathcal{H}^{\otimes n}).$$

Thus  $H^0_*(\mathcal{O}_E) = R_E$  and  $\pi_*$  corresponds to forgetting the y-action on  $H^0_*(\mathcal{G})$ .

**Proposition 2.1.** If  $\mathcal{L}$  is a vector bundle on E, then  $B = H^0_*(\mathcal{L})$  is a graded free module over the homogeneous coordinate ring k[s,t] of  $\mathbb{P}^1$ , and  $y:\mathcal{L}\to\mathcal{L}(g+1)$  induces a map  $\phi=H^0_*y:B\to B(g+1)$  such that  $\phi^2$  is multiplication by f; that is, a matrix factorization of f.

Furthermore, given a graded free module B corresponding to the vector bundle B on  $\mathbb{P}^1$ , and a map  $\phi: B \to B(g+1)$  with  $\phi^2 = f \cdot Id_B$ , the sheaf

$$\mathcal{L} = \operatorname{coker} (y - \phi : \pi^* \mathcal{B}(-g - 1) \longrightarrow \pi^* \mathcal{B})$$

is a vector bundle on E whose pushforward is B, and on which y induces the matrix factorization  $\phi$ . We have

$$\chi(\mathcal{B}) = \chi(\mathcal{L}), \quad \text{rk } \mathcal{B} = 2 \, \text{rk } \mathcal{L}, \quad \text{and} \quad \deg \mathcal{B} = \deg \mathcal{L} - (\text{rk } \mathcal{L})(1 + g).$$

The proof could be extended to show that the category of vector bundles on E is equivalent to the category of matrix factorizations of f over k[s,t], cf. [Eis80].

*Proof of Proposition 2.1.* The equation  $\phi^2 = f$  follows from functoriality. Conversely, if a matrix factorization  $\phi^2 = f \cdot Id_B$  is given, then  $(y - \phi, y + \phi)$  is a matrix factorization of  $y^2 - f$  over k[s, t, y]. Thus the module  $\operatorname{coker}(y - \phi)$  is a maximal Cohen–Macaulay  $R_E$ -module, and it follows that the sheaf associated to its  $\operatorname{cokernel}$  is a vector bundle on E.

The next Theorem reduces the computation of the tensor product of vector bundles on E to a syzygy computation, and will be used this way in the sequel.

**Theorem 2.2.** If  $\mathcal{L}_1$ ,  $\mathcal{L}_2$  are vector bundles on E with matrix factorizations  $\phi_i$  on the graded free k[s,t]-modules  $B_i = H^0_*(\mathcal{L}_i)$ , then

$$H^0_*(\mathcal{L}_1 \otimes \mathcal{L}_2) = \ker(\phi_1 \otimes 1 - 1 \otimes \phi_2: B_1 \otimes B_2(g+1) \longrightarrow B_1 \otimes B_2(2g+2))$$

and  $\pi_* y$  acts on  $\pi_* (\mathcal{L}_1 \otimes \mathcal{L}_2)$  with the common action of  $\phi_1 \otimes 1$  and  $1 \otimes \phi_2$ .

## PDF page 5

*Proof.* The following sequence of maps is a complex because  $y^2 = f$ :

(\*) 
$$B_1 \otimes B_2(-g-1) \xrightarrow{\phi_1 \otimes 1 - 1 \otimes \phi_2} B_1 \otimes B_2 \xrightarrow{\phi_1 \otimes 1 + 1 \otimes \phi_2} B_1 \otimes B_2(g+1) \xrightarrow{\phi_1 \otimes 1 - 1 \otimes \phi_2} B_1 \otimes B_2(2g+2)$$
  
Since the  $k[s,t]$ -module

$$\ker \left( B_1 \otimes B_2(g+1) \xrightarrow{\phi_1 \otimes 1 - 1 \otimes \phi_2} B_1 \otimes B_2(2g+2) \right)$$

is a 2<sup>nd</sup> syzygy, it is free. Thus, to prove the theorem, it suffices to show that the complex (\*) is locally exact and that the sheaf cokernel

$$\operatorname{coker}\left(\mathcal{B}_1\otimes\mathcal{B}_2(-g-1)\xrightarrow{\phi_1\otimes 1-1\otimes\phi_2}\mathcal{B}_1\otimes\mathcal{B}_2\right)$$

is  $\pi_*(\mathcal{L}_1 \otimes_E \mathcal{L}_2)$ .

For simplicity of notation we ignore the twists by powers of  $\mathcal{H}$ . Note that  $\mathcal{B}_i := \pi_*(\mathcal{L}_i)$  is the sheafification of  $B_i$ . Since  $\mathcal{L}_i$  is the cokernel of  $y - \phi_i$  we see that  $\mathcal{L}_1 \otimes_{\mathcal{E}} \mathcal{L}_2$  is the cokernel of

$$(\pi^*\mathcal{B}_1 \otimes_E \pi^*\mathcal{B}_2) \oplus (\pi^*\mathcal{B}_2 \otimes_E \pi^*\mathcal{B}_1) \xrightarrow{(y \otimes 1 - \phi_1 \otimes 1, 1 \otimes y - 1 \otimes \phi_2)} \pi^*\mathcal{B}_1 \otimes_E \pi^*\mathcal{B}_2.$$

Since the tensor products are over E, the maps  $y \otimes 1$  and  $1 \otimes y$  are equal, and are simply multiplication by y, so this says that  $\mathcal{L}_1 \otimes \mathcal{L}_2$  is the universal quotient of  $\pi^* \mathcal{B}_1 \otimes_E \pi^* \mathcal{B}_2$  on which the maps  $y, \phi_1 \otimes 1, 1 \otimes \phi_2$  all agree. Furthermore,

$$\pi_*(\pi^*\mathcal{B}_1 \otimes_E \pi^*\mathcal{B}_2) = \pi_*\pi^*(\mathcal{B}_1 \otimes_{\mathbb{P}^1} \mathcal{B}_2) = \pi_*(\mathcal{O}_E) \otimes_{\mathbb{P}^1} \mathcal{B}_1 \otimes_{\mathbb{P}^1} \mathcal{B}_2.$$

where the action of y is on the first factor only. Thus  $\pi_*(\mathcal{L}_1 \otimes \mathcal{L}_2)$  is the cokernel of

$$\phi_1 \otimes 1 - 1 \otimes \phi_2 : \mathcal{B}_1 \otimes \mathcal{B}_2 \longrightarrow \mathcal{B}_1 \otimes \mathcal{B}_2.$$

To complete the proof we must show that the sequence (\*) is locally exact. Choose a point  $x \in \mathbb{P}^1$  and denote the local ring  $\mathcal{O}_{\mathbb{P}^1,x}$  by A and the A-module  $\mathcal{B}_{i,x}$  by  $F_1 + yF_1$  where the  $F_i$  are free A-modules. The endomorphism  $\phi_i$  takes  $F_i$  to  $yF_i$  by multiplying with y, and  $yF_i$  to  $F_i$  by sending y to  $f \in A$ . In this notation, the maps  $\phi_1 \otimes 1 \pm 1 \otimes \phi_2$  may be written as block matrices of the form

$$F_{1} \otimes F_{2} \quad F_{1} \otimes yF_{2} \quad yF_{1} \otimes F_{2} \quad yF_{1} \otimes yF_{2}$$

$$F_{1} \otimes F_{2} \quad \begin{cases} 0 & \pm f & f & 0 \\ \pm 1 & 0 & 0 & f \\ yF_{1} \otimes F_{2} & 1 & 0 & 0 & \pm f \\ yF_{1} \otimes yF_{2} & 0 & 1 & \pm 1 & 0 \end{cases}$$

Modulo the maximal ideal of A both these maps have rank equal to twice the rank of  $F_1 \otimes F_2$ , so the sequence above is locally split exact, as required.

**Definition 2.3.** Let  $f(s,t) = \prod_{i=1}^{2g+2} f_i$  be a factorization of f into (necessarily distinct) linear factors, and, for  $I \subset \{1, ..., 2g+2\}$ , write  $f_I := \prod_{i \in I} f_i$ . We write  $\phi_I$  for the matrix

$$\begin{pmatrix} 0 & f_{I^c} \\ f_I & 0 \end{pmatrix} : \mathcal{O}_{\mathbb{P}^1} \left( \lceil -|I|/2 \rceil \right) \oplus \mathcal{O}_{\mathbb{P}^1} \left( \lceil -|I^c|/2 \rceil \right) \longrightarrow \mathcal{O}_{\mathbb{P}^1} \left( \lceil |I^c|/2 \rceil \right) \oplus \mathcal{O}_{\mathbb{P}^1} \left( \lceil |I|/2 \rceil \right)$$

on  $\mathbb{P}^1$  where  $I^c$  denotes the complement of I. Note that  $(\phi_I, \phi_{I^c})$  is a matrix factorization of f. Let  $\mathcal{L}_I$  be the corresponding line bundle on E, as defined in Proposition 2.1. Note that  $\mathcal{L}_I \cong \mathcal{L}_{I^c}$  and  $\mathcal{L}_{\varnothing} \cong \mathcal{O}_E$ . Write  $I\Delta J = (I \setminus J) \cup (J \setminus I)$  for the symmetric difference of I and J.

**Theorem 2.4.** *For*  $I, J \subset \{1, ..., 2g + 2\}$ 

$$\mathcal{L}_I \otimes \mathcal{L}_J \cong \begin{cases} \mathcal{L}_{I\Delta J} & \textit{if} \, |I| \cdot |J| \equiv 0 \mod 2, \ \mathcal{L}_{I\Delta J}(\mathcal{H}) & \textit{else}. \end{cases}$$

## PDF page 6

Thus the line bundles  $\mathcal{L}_I$  with |I| even are the  $2^{2g}$  two-torsion line bundles on E. The line bundles  $\mathcal{L}_I$  with |I| odd are the  $2^{2g}$  square roots of  $\mathcal{O}_E(\mathcal{H})$ .

*Proof.* In this case the matrix  $\phi_I \otimes 1 - 1 \otimes \phi_I$  has the form

$$\begin{pmatrix} 0 & f_{I^c} & -f_{J^c} & 0 \\ f_I & 0 & 0 & -f_{J^c} \\ -f_J & 0 & 0 & f_{I^c} \\ 0 & -f_I & f_I & 0 \end{pmatrix}.$$

By Theorem 2.2, its kernel is the free module  $H^0_*(\mathcal{L}_I \otimes \mathcal{L}_J)$ . Because  $J^c \setminus I^c = I \setminus J$  and  $I \setminus J^c = J \setminus I^c$  this kernel contains the free submodule B generated by the column vectors

$$\begin{pmatrix} 0 & f_{J^c \setminus I} \\ f_{I \setminus J} & 0 \\ f_{J \setminus I} & 0 \\ 0 & f_{I \setminus J^c} \end{pmatrix}.$$

These columns generate the kernel because the  $2 \times 2$  minors of B have no common factor (see [BE73, Corollary 1]).

To show that  $\mathcal{L}_I \otimes \mathcal{L}_J \cong \mathcal{L}_{I\Delta J}$  it now suffices to show that the matrix representing the action of  $\phi_1 \otimes 1$  restricted to the columns of B is

$$\begin{pmatrix} 0 & f_{(I\Delta J)^c} \\ f_{I\Delta J} & 0 \end{pmatrix}.$$

This, in turn, follows at once from the identities

$$I^c \cup (I \setminus J) = (I\Delta J) \cup (J^c \setminus I), \quad I \cup (J \setminus I) = (I\Delta J) \cup (I \setminus J^c)$$

and similarly

$$I \cup (J^c \setminus I) = (I\Delta J)^c \cup (I \setminus J), \quad I^c \cup (I \setminus J^c) = (I\Delta J)^c \cup (J \setminus I).$$

To show that  $\mathcal{L}_I \not\equiv \mathcal{L}_I$  for  $J \notin \{I, I^c\}$  are non-isomorphic, we consider the ideals generated by the entries of

$$\begin{pmatrix} 0 & f_{I^c} \\ f_I & 0 \end{pmatrix}$$
 and  $\begin{pmatrix} 0 & f_{J^c} \\ f_I & 0 \end{pmatrix}$ .

By looking at the elements of smallest degree, we see that these ideals could not be equal unless |I| = |J| = g+1. Also, in case |I| = |J| = g+1, the intersection  $I \cap J$  is non-empty since  $J \neq I^c$  and for  $i \in I \cap J$  we recover  $f_I$  as the smallest degree generator of  $(f_i) \cap (f_I, f_{I^c})$ .

There are  $2^{2g+2}/4$  unordered pairs  $\{I,I^c\}$  of even subsets of  $\{1,\ldots,2g+2\}$ . Thus we get all  $2^{2g}$  different two-torsion line bundles  $\mathcal{L}_I$  for even I. A similar argument applies to roots of  $\mathcal{H}$ .

## 3. BGG for complete intersections of quadrics

This section provides what we need of the theory of [BEH87] and [Kap89]. Let  $P_X := k[V^*]/(q_1, ..., q_c)$  be the homogeneous coordinate ring of the complete intersection  $X = Q_1 \cap \cdots \cap Q_c \subset \mathbb{P}(V^*) = \mathbb{P}^{r-1}$  of c quadrics  $Q_i = V(q_i)$  and choose a basis  $x_1, ..., x_r$  of  $V^*$ . Write  $B_\ell$  for the symmetric matrix with i, j entry

$$b_{\ell,i,j} = \frac{1}{2} (q_{\ell}(x_i + x_j) - q_{\ell}(x_i) - q_{\ell}(x_j)).$$

Let  $T = k[t_1, ..., t_c]$  denote a polynomial ring in c variables each of degree 2 and let

$$q: \left\{ \begin{array}{ccc} T \otimes V & \longrightarrow & T \\ 1 \otimes v & \longmapsto & t_1 q_1(v) + \dots + t_c q_c(v) \end{array} \right.$$

## PDF page 7

denote the corresponding family of quadratic forms over Spec*T* . Let

$$C := \left(T \otimes \left(\bigoplus_{n} V^{\otimes n}\right)\right) / (v \otimes v - q(v) \mid v \in V)$$

denote the Z-graded Clifford algebra of *q*, so that *C* is the quadratic dual of *P<sup>X</sup>* in the sense of [\[PP05\]](#page-24-5). The algebra *C* is free as a *T* -module with basis

$$e_I=e_{i_1}e_{i_2}\cdots e_{i_k}$$

where *e*1*,...,e<sup>r</sup>* is a basis of *V* dual to *x*1*,...,x<sup>r</sup>* and *I* = {*i*<sup>1</sup> < *i*<sup>2</sup> < ⋯ < *ik*} ⊂ {1*,..., r*} an ordered subset. See for example [\[Jac80,](#page-23-12) Section 4.8].

**Theorem 3.1.** *Let P<sup>X</sup> be the homogeneous coordinate ring of a complete intersection of c quadrics, and let C denote the corresponding* Z*-graded Clifford algebra. Then P<sup>X</sup> and C are a pair of Koszul dual graded algebras. In particular*

$$\operatorname{Ext}_{P_X}(k,k) \cong C \ \textit{and} \ \operatorname{Ext}_C(k,k) \cong P_X.$$

*Proof.* See [\[Sjö76\]](#page-24-6), [\[Kap89,](#page-23-5) Section 1] and [\[PP05\]](#page-24-5). □

**Corollary 3.2.** *For any graded PX-module M the module* Ext*P<sup>X</sup>* (*M,k*) *is a graded C* = Ext*P<sup>X</sup>* (*k,k*)*-module.*

The main result of this section is that for a graded *PX*-modules *M* with a linear resolution one can recover *M* from the graded *C*-module Ext*P<sup>X</sup>* (*M,k*).

If *M* is a (left) *PX*-module and *N* is a right *C*-module then we define an endomorphism of left *P<sup>X</sup>* ⊗*C*-modules

$$d: \operatorname{Hom}_k(N,M) \longrightarrow \operatorname{Hom}_k(N,M)$$

taking *φ* ∈ Hom*k*(*N ,M*) to *ψ*, where *ψ*(*n*) = ∑*<sup>i</sup> xiφ*(*nei*).

Note that

$$d^{2}(\phi)(n) = \sum_{i,j} x_{i} x_{j} \phi(ne_{i}e_{j}) = \sum_{i \leq j} x_{i} x_{j} \phi(n(e_{i}e_{j} + e_{j}e_{i})) = \sum_{i \leq j} x_{i} x_{j} \phi(n\sum_{\ell} (t_{\ell}b_{\ell,i,j}))$$

$$= \sum_{\ell} \sum_{i \leq j} b_{\ell,i,j} x_{i} x_{j} \phi(nt_{\ell}) = \sum_{\ell} q_{\ell}(x) \phi(nt_{\ell}) = 0.$$

Thus, when *N* is Z-graded, Hom*k*(*N ,M*) may be regarded as a complex of *PX*-modules

$$\operatorname{Hom}_k(N,M): \cdots \longrightarrow \operatorname{Hom}_k(N_i,M) \longrightarrow \operatorname{Hom}_k(N_{i-1},M) \longrightarrow \cdots$$

When *M* is Z-graded and *N* is a *C* −*C*-bimodule, then Hom*k*(*N ,M*) may also be regarded as a complex of right *C*-modules

$$\operatorname{Hom}_k(N,M): \cdots \longrightarrow \operatorname{Hom}_k(N,M_i) \longrightarrow \operatorname{Hom}_k(N,M_{i+1}) \longrightarrow \cdots$$

Similar statements hold for Hom*k*(*M,N*).

**Theorem 3.3.** *If the graded PX-module M has a linear free resolution, then the resolution may be written in the form*

$$\operatorname{Hom}_k(\operatorname{Ext}_{P_X}(M,k), P_X)$$

*where we view* Ext*P<sup>X</sup>* (*M,k*) *as a graded C* = Ext*P<sup>X</sup>* (*k,k*) *module, and apply the construction above.*

*Example* 3.4*.* The complex Hom*k*(*C,PX*),

$$0 \longleftarrow C_0^* \otimes_k P_X \longleftarrow C_1^* \otimes_k P_X \longleftarrow C_2^* \otimes_k P_X \longleftarrow \cdots$$

is isomorphic to the *PX*-free resolution of *k*.

## PDF page 8

Note that this statement may be deduced from [PP05, Corollary 3.2(iiM)]. Since this result plays a crucial role in the proof of Proposition 5.6, we give a proof below. For our proof we need an explicit description of the action of  $\operatorname{Ext}_{P_{\nu}}^{1}(k,k)$  on  $\operatorname{Ext}_{P_{\nu}}(M,k)$ .

To avoid keeping track of grading shifts we formulate this in case of a finitely generated module M over a Noetherian local ring R with maximal ideal  $\mathfrak{m}$ . Let  $(x_1,\ldots,x_r)$  denote minimal generators of  $\mathfrak{m}$ , and let  $e_i \in \operatorname{Ext}^1_R(k,k)$  be the extension

$$e_i : 0 \longrightarrow k \xrightarrow{x_i} E_i \longrightarrow k \longrightarrow 0$$

where  $E_i = R/(x_1, ..., x_{i-1}, x_i^2, x_{i+1}, ..., x_r)$ . Let

$$\mathbb{F}: \cdots \xrightarrow{d} F_j \xrightarrow{d} \cdots \xrightarrow{d} F_0$$

be the minimal free resolution of a finitely generated R-module M. Since the resolution F is minimal the differential d(f) of an element  $f \in F_{j+1}$  can be written in the form  $d(f) = \sum_{i=1}^{r} x_i f_i$  for  $f_i \in F_j$ .

**Lemma 3.5.** Let  $\alpha \in \operatorname{Ext}_R^j(M,k)$  be a class represented by a map  $\alpha' : F_j \to k$ . The element  $\alpha e_i \in \operatorname{Ext}_R^{j+1}(M,k)$  is then represented by the map  $\beta_i$  with  $\beta_i(f) = \alpha'(f_i)$  for  $f \in F_{j+1}$  with differential  $d(f) = \sum_{i=1}^r x_i f_i$ .

*Proof.* We compute the image of  $\alpha$  under the connecting homomorphism  $\delta$ 

$$\operatorname{Ext}_R^j(M, E_i) \longrightarrow \operatorname{Ext}_R^j(M, k) \stackrel{\delta}{\longrightarrow} \operatorname{Ext}_R^{j+1}(M, k) \longrightarrow \operatorname{Ext}_R^{j+1}(M, E_i)$$

associated to the sequence  $e_i$  above. Consider the diagram

$$F_{j+1} \xrightarrow{d} F_{j}$$

$$\beta_{i} \downarrow \qquad \alpha'' \downarrow$$

$$k \xrightarrow{x_{i}} E_{j} \xrightarrow{k} k$$

where  $\alpha''$  is a lift of  $\alpha'$  to  $E_i$ . The composition  $\alpha' \circ d$  is zero since  $\alpha'(\mathfrak{m}F_j) = 0$ . Thus  $\alpha'' \circ d$  factors over the map

$$\beta_i : \left\{ \begin{array}{ccc} F_{j+1} & \longrightarrow & k \\ f & \longmapsto & \alpha'(f_i). \end{array} \right.$$

This map is well-defined, *i.e.* independent of the choice of  $f_i$ . Indeed, if  $d(f) = \sum_{i=1}^r x_i f_i'$  is a different choice for the presentation of d(f) then  $x_i(f_i - f_i') \in (x_1, \dots, x_{i-1}, x_{i+1}, \dots x_r) F_j$  which maps to zero in  $E_i$ .

Proof of Theorem 3.3. Let

$$\mathbb{F} : \cdots \xrightarrow{d} F_i \xrightarrow{d} \cdots \xrightarrow{d} F_0$$

be the minimal graded free resolution of M as a  $P_X$ -module. Then

$$F_j \cong \overline{F}_j \otimes_k P_X$$

where  $\overline{F}_j \cong F_j/\mathfrak{m}F_j$ . If M has a linear resolution then we claim that the isomorphisms

$$\begin{cases}
F_j = \overline{F}_j \otimes P_X & \xrightarrow{\cong} & \operatorname{Hom}_k(\operatorname{Hom}_{P_X}(F_j, k), P_X) \\
\overline{f} \otimes p & \longmapsto & \{\varphi : \alpha \mapsto \alpha(f) \otimes p\}
\end{cases}$$

induce an isomorphism of complexes, *i.e.* we have to show that these maps commute with differentials of the two complexes. Let  $b_1, \ldots, b_\ell$  be a k-basis of  $\overline{F}_j$  with dual basis  $b_1^*, \ldots, b_\ell^*$  of  $\overline{F}_j^* = \operatorname{Hom}_k(\overline{F}_j, k) = \operatorname{Hom}_{P_X}(F_j, k)$ .

## PDF page 9

Consider an element *f* = *f* ⊗1 ∈ *Fj*+1. Then

$$d(f) = \sum_{i=1}^{r} \sum_{\nu=1}^{\ell} c_{i\nu} b_{\nu} \otimes x_{i} \text{ with } c_{i\nu} \in k$$

and we can take *f<sup>i</sup>* = ∑ *ℓ ν*=1 *ciνb<sup>ν</sup>* for the coefficient of *x<sup>i</sup>* as in Lemma [3.5.](#page-7-0) The map

$$\{\varphi: \alpha \mapsto \alpha(f)\} \in \operatorname{Hom}_k\left(\operatorname{Hom}_{P_X}(F_{j+1},k), P_X\right)$$

maps to

$$\{\alpha' \mapsto \sum_{i=1}^r x_i \varphi(\alpha' e_i)\} \in \operatorname{Hom}_k \left(\operatorname{Hom}_{P_X}(F_j, k), P_X\right)$$

by the definition of the differential of Hom*k*(Ext*P<sup>X</sup>* (*M,k*)*,PX*). We have

$$\sum_{i=1}^{r} x_i \varphi(\alpha' e_i) = \sum_{i=1}^{r} x_i \alpha'(f_i)$$
 (by Lemma 3.5)  
$$= \sum_{i=1}^{r} x_i \alpha'(\sum_{\nu=1}^{\ell} c_{i\nu} b_{\nu})$$

In particular, for *α* ′ = *b* ∗ *<sup>µ</sup>* we obtain *b* ∗ *<sup>µ</sup>* ↦ ∑ *r i*=1 *ciµx<sup>i</sup>* . These values coincide with the values of the image of

$$d(f) = \sum_{i=1}^{r} \sum_{\nu=1}^{\ell} c_{i\nu} b_{\nu} \otimes x_{i}$$

in 
$$\operatorname{Hom}_k\left(\operatorname{Hom}_{P_X}(F_j,k),P_X\right)$$
, since  $b_{\mu}^*(\sum_{\nu=1}^{\ell}c_{i\nu}b_{\nu})=c_{i\mu}$ .

**Corollary 3.6.** *Let N be a graded left C-module. The complex* Hom*k*(*N ,PX*) *is a resolution if and only if N* ≅ Ext*P<sup>X</sup>* (*M,k*) *up to shift where M is a PX-module with a linear resolution.*

*Proof.* If *N* ≅ Ext*P<sup>X</sup>* (*M,k*) up to shift where *M* is a *PX*-module with a linear resolution then by Theorem 2.4 the resolution of *M* is Hom*k*(*N ,PX*). Conversely, if the complex Hom*k*(*N ,PX*) is a resolution, then since it is linear we may take the module it resolves to be *M*. □

## **4. Pencils of quadrics and hyperelliptic curves**

We now specialize to the case of a smooth intersection of two quadrics in P <sup>2</sup>*g*+<sup>1</sup> with coordinate ring *P<sup>X</sup>* = *k*[*x*1*,...,x*2*g*+2]/(*q*1*,q*2). To simplify notation we write *s, t* instead of *t*1*, t*2. Let *q* = *q*(*s, t*) = *sq*<sup>1</sup> + *tq*<sup>2</sup> and let *C* = Cliff(*q*) denote the Z-graded Clifford algebra of *q*, so that *T* = *k*[*s, t*] ⊂ *C*.

As in Reid's thesis [\[Rei72\]](#page-24-1) we note that none of the quadrics in the pencil can have corank 2: for, if one of the quadrics had singular locus *L* of dimension at least 2, then *X* would be singular at *L* ∩ *X*. Further, by Bertini's Theorem the general linear combination of the two quadrics is non-singular outside the intersection. But if it were singular at a point of the intersection, then the intersection would be singular there too. Thus we may assume that one of the quadrics has full rank, and it follows that the two quadrics can be simultaneously diagonalized (see [\[Gan59,](#page-23-13) XII, Paragraph 6, Theorem 7]). Thus we may assume that the bilinear form *q*(*s, t*) = *sq*<sup>1</sup> +*tq*<sup>2</sup> is given by a diagonal matrix

$$\begin{pmatrix} f_1 & 0 \\ & \ddots \\ 0 & f_{2g+2} \end{pmatrix}$$

with entries that are pairwise coprime linear polynomials *f<sup>i</sup>* ∈ *k*[*s, t*]. As in Section [2](#page-3-0) we denote by *f* = ∏*f<sup>i</sup>* , and use the notation *f<sup>I</sup>* = ∏*i*∈*<sup>I</sup> fi* .

## PDF page 10

We write


$$C = C^{\text{ev}} \oplus C^{\text{odd}}$$

for the decomposition of the Clifford algebra into its even and odd parts. As a T = k[s, t]-module, C is free with basis  $e_I$  and

$$(4.1) e_I e_J = \epsilon(I, J) f_{I \cap J} e_{I \Delta J}.$$

with the sign  $\epsilon(I,J) = (-1)^{\sum_{i \in I} |\{j \in J | j < i\}|}$ .

Since

$$\sum_{i \in I} |\{j \in \{1, \dots, 2g+2\} \mid j < i\}| = \sum_{i \in I} (i-1)$$

and

$$\sum_{j \in \{1, \dots, 2g+2\}} |\{i \in I | i < j\}| = \sum_{i \in I} (2g+2-i) \equiv \sum_{i \in I} (i-1) \mod 2$$

for even I, we see that  $e_{\{1,\ldots,2g+2\}}$  lies in the center of the even Clifford algebra. Because

$$\sum_{i=1}^{2g+2} (i-1) = {2g+2 \choose 2} \equiv g+1 \mod 2,$$

the element  $e_{\{1,\dots,2g+2\}}$  satisfies the equation

$$e_{\{1,\ldots,2g+2\}}^2 = (-1)^{g+1} f.$$

To adjust for the sign we take  $y = (\sqrt{-1})^{g+1}e_{\{1,\dots,2g+2\}}$  as a generator of the center of the even Clifford algebra over k[s,t] so that  $y^2 = f$ . Note that the formula above for the central element y is only correct in the case of diagonal quadrics; for the general case see [Haa91, Satz 1].

Furthermore, for any I,

$$e_I e_{\{1,\dots,2g+2\}} = (-1)^{\sum_{i \in I} (i-1)} f_I e_{I^c}$$
 and  $e_{I^c} e_{\{1,\dots,2g+2\}} = (-1)^{\sum_{i \in I^c} (i-1)} f_{I^c} e_I$ .

Note that the signs in the two formulas differ by  $(-1)^{g+1}$ . Thus with  $R_E = k[s,t,y]/(y^2 - f)$  the coordinate ring of the corresponding hyperelliptic curve, the  $R_E$ -submodule of C generated by  $e_I$  and  $e_{I^c}$  coincides with  $H^0_*(\mathcal{L}_I)$  from Definition 2.3.

Notice however, that here, differently than in section 1,  $R_E$  is  $2\mathbb{Z}$ -graded as a subring of  $C^{\text{ev}}$ . Thus, since the elements of  $C^{\text{odd}}$  have odd degree, we have to twist by an odd number to obtain a non-trivial sheaf of  $\mathcal{O}_E$ -modules.

We define  $C^{\text{ev}} = \widetilde{C^{\text{ev}}}$  and  $C^{\text{odd}} = \widetilde{C^{\text{odd}}(1)}$ . Hence multiplication in C gives a map

$$C^{\mathrm{odd}}(1) \times C^{\mathrm{odd}}(1) \longrightarrow C^{\mathrm{ev}}(2)$$

which sheafifies to a map

$$\mathcal{C}^{odd} \otimes_{\mathcal{O}_E} \mathcal{C}^{odd} \longrightarrow \mathcal{C}^{ev} \otimes \pi^* \mathcal{O}_{\mathbb{P}^1}(1) = \mathcal{C}^{ev} \otimes \mathcal{H}.$$

In summary, we get the following statement.

**Proposition 4.1.** Let  $y = (\sqrt{-1})^{g+1} e_{\{1,\dots,2g+2\}}$ . The element y is in the center of  $C^{ev}$  and satisfies the equation  $y^2 = f$ , where  $f = \prod_{i=1}^{2g+2} f_i$ . If we write  $R_E = k[s,t,y]/(y^2 - f)$  then the even Clifford algebra decomposes as an  $R_E$ -module as

$$C^{\text{ev}} = \bigoplus_{\substack{\{I,I^c\}\\|I| \text{ even}}} H^0_*(\mathcal{L}_I).$$

The odd part of the Clifford algebra decomposes as a right R<sub>E</sub>-module as

$$C^{\mathrm{odd}}(1) = \bigoplus_{\substack{\{I,I^c\}\\|I|\ odd}} H^0_*(\mathcal{L}_I).$$

## PDF page 11

Moreover.

$$\mathcal{C}^{\mathrm{odd}} \cong \mathcal{O}_E(p) \otimes \mathcal{C}^{\mathrm{ev}}$$

where p is any ramification point of  $\pi: E \to \mathbb{P}^1$ .

*Proof.* This follows from Theorem 2.4. Note that since p is a ramification point we have  $\mathcal{O}_E(2p) \cong \mathcal{H}$  and the multiplication map  $\mathcal{C}^{\text{odd}} \otimes \mathcal{C}^{\text{odd}} \to \mathcal{C}^{\text{ev}} \otimes \mathcal{H}$  is compatible with the map

$$\mathcal{O}_E(p) \otimes \mathcal{O}_E(p) \longrightarrow \mathcal{O}_E(2p) \cong \pi^* \mathcal{O}_{\mathbb{P}^1}(1) = \mathcal{H}.$$

*Remark* 4.2. Notice that y and the elements of  $C^{\text{odd}}$  anti-commute by equation (4.1) applied to the case when I is a singleton and  $J = \{1, ..., 2g + 2\}$ .

The following result was proven in [Rei72].

**Lemma 4.3.** Let  $q_1, q_2$  be two quadratic forms on a 2g + 2-dimensional vector space V over k. The set of g-dimensional common isotropic subspaces of  $q_1, q_2$  is non-empty and has dimension  $\geq g$  locally at every point.

*Proof.* Let  $\mathcal{U}$  be the universal sub-bundle on the Grassmannian  $\mathbb{G} := \mathbb{G}(g,V)$ . The forms  $q_i$  define homomorphisms  $\operatorname{Sym}^2 V^* \otimes_k \mathcal{O}_{\mathbb{G}} \to \mathcal{O}_{\mathbb{G}}$ , and thus, by restriction, sections of  $\operatorname{Sym}^2(\mathcal{U}^*)$ . The set of g-dimensional common isotropic subspaces is the common zero locus of these two sections. Computing the Chern class we see that the locus is non empty and, since

$$\dim \mathbb{G}(g, V) - 2 \operatorname{rk} \operatorname{Sym}^{2}(\mathcal{U}^{*}) = g(g+2) - 2\binom{g+1}{2} = g,$$

the inequality on dimensions follows.

We return to the situation at the beginning of Section 3, with


$$P = k[x_1,...,x_{2g+2}] = \text{Sym}(V^*).$$

Let  $U \subset V$  be a g-dimensional isotropic linear subspace and denote by  $P_U = \operatorname{Sym}(U^*) = P/(U^{\perp})$  its coordinate ring, where  $U^{\perp} \subset V^*$  is the space of linear equations of the isotropic space U.

**Proposition 4.4.** Let  $G = ks \oplus kt \cong k^2$  be the space of parameters for the family of quadratic forms  $sq_1 + tq_2$ . Considered as a  $P_X$ -module,  $P_{IJ}$  has a linear free resolution. Moreover

(4.2) 
$$\operatorname{Ext}_{P_X}^{2p}(P_U,k) = \bigoplus_{i} \left( \Lambda^{2i} U^{\perp} \otimes_k \left( \operatorname{Sym}_{p-i} G \right)^* \right)^*$$

and

(4.3) 
$$\operatorname{Ext}_{P_X}^{2p+1}(P_U,k) = \bigoplus_{i} \left(\Lambda^{2i+1} U^{\perp} \otimes_k (\operatorname{Sym}_{p-i} G)^*\right)^*.$$

*Proof.* The ideal  $(U^{\perp})$  contains the 2-dimensional vector space  $G := \langle q_1, q_2 \rangle$ . This ideal is generated by a regular sequence of linear forms, and the P-free resolution of  $P_U = P/(U^{\perp})$  is thus a Koszul complex with underlying free module  $P \otimes \Lambda U^{\perp}$ . Let  $\gamma : G \to P_1 \otimes U^{\perp}$  be a map of vector spaces such that the composition of  $\gamma$  with the multiplication map


$$G \longrightarrow P_1 \otimes_k U^{\perp} \longrightarrow P_2$$

is the inclusion of G in  $P_2$ .

By [Tat57, Theorem 4], the minimal  $P_X$ -free resolution of  $P_U$  is the differential graded R-algebra

$$P_X \otimes_k \Lambda U^{\perp} \otimes (\operatorname{Sym} G^*)^*$$
.

Here  $U^{\perp}$  has internal degree 1 and homological degree 1, while  $G^*$  has internal degree 2 and homological degree 2, and the component of the differential  $G = \left(\operatorname{Sym}^1 G^*\right)^* \to P_X \otimes_k U^{\perp}$  is induced by  $\gamma$ .

## PDF page 12

This resolution is linear, and has degree *j* term

$$P_X \otimes_k \left( \bigoplus_{j=a+2b} (\Lambda^a U^{\perp}) \otimes_k (\operatorname{Sym}_b G)^* \right). \qquad \Box$$

Let  $T = \operatorname{Sym} G \cong k[s, t]$  and write

$$F_U = \operatorname{Ext}^{\operatorname{ev}}_{P_X}(P_U,k) = \bigoplus_i \left( \left( \Lambda^{2i} U^\perp \right)^* \otimes_k T(-i) \right)$$

regarded as a module over  $\operatorname{Ext}_{P_x}^{\operatorname{ev}}(k,k) = C^{\operatorname{ev}}$  via the Yoneda pairing.

**Proposition 4.5.** The sheafification  $\mathcal{F}_U$  of  $F_U$  as an  $\mathcal{O}_E$ -module is a vector bundle of  $\operatorname{rk} \mathcal{F}_U = 2^g$  and degree  $\operatorname{deg} \mathcal{F}_U = g2^{g-1}$  on E. Moreover,

$$H^0_*(\mathcal{F}_U) = Ext^{\mathrm{ev}}(P_U, k),$$

and

$$H^0_*(\mathcal{F}_U(p)) = Ext^{\text{odd}}(P_U, k).$$

*Proof.* It follows from the formulas above that the sheafification  $\mathcal{F}_U$  of  $F_U$  as an  $\mathcal{O}_E$ -module is a vector bundle of rank equal to  $\dim_k(\Lambda^{\mathrm{ev}}U^\perp)/2 = 2^g$ . Moreover

$$\deg \pi_* \mathcal{F}_U = -\sum_{i>0} i {g+2 \choose 2i} = -(g+2)2^{g-1}.$$

By Proposition 2.1,  $\mathcal{F}_U$  has degree

$$\deg \mathcal{F}_U = (g+1)\operatorname{rk} \mathcal{F}_U + \deg \pi_* \mathcal{F}_U = (g+1)2^g - (g+2)2^{g-1} = g2^{g-1}.$$

The first displayed formula is immediate from the definition of  $F_U$ , while the second follows from the equality  $C^{\text{odd}} = C^{\text{ev}}(p)$ .

**Theorem 4.6.** The endomorphism bundle of  $\mathcal{F}_U$  is isomorphic as an  $\mathcal{O}_E$ -algebra to the sheafified even Clifford algebra  $\mathcal{C}^{ev}$ ; that is,

$$\mathcal{E}nd_E(\mathcal{F}_U) \cong \mathcal{C}^{\mathrm{ev}}.$$

*Proof.* Let  $(a,b) \in \mathbb{P}^1$  be a point that is not a branch point of  $\pi$ . The algebra  $\pi_*\mathcal{C}^{\mathrm{ev}}$  is a sheaf of algebras whose fiber at (a,b) is isomorphic to the product of the fibers of  $\mathcal{C}^{\mathrm{ev}}$  at the two preimages of (a,b) in E. On the other hand, the fiber of  $\pi_*\mathcal{C}^{\mathrm{ev}}$  is the even Clifford algebra of the nonsingular quadratic form  $aq_1 + bq_2$ . Thus it is a semisimple algebra with 2-dimensional center generated over k by y. Since we have assumed that k is algebraically closed, this center is  $k \times k$ . The corresponding decomposition of the push forward of  $\mathcal{C}^{\mathrm{ev}}$  as a direct product is the unique decomposition as the product of two algebras. Thus the fibers of  $\mathcal{C}^{\mathrm{ev}}$  at points of E other than the ramification points are simple algebras by [Jac80, Theorem 4.13].

Since  $F_U$  is an  $R_E$  –  $C^{\text{ev}}$  bimodule we have an  $\mathcal{O}_E$ -algebra homomorphism

$$\phi: \mathcal{C}^{\mathrm{ev}} \longrightarrow \mathcal{E}nd_F(\mathcal{F}_{II})$$

Since the general fiber of  $\mathcal{C}^{\text{ev}}$  is simple, the kernel of this homomorphism must be torsion, and thus 0. The source and target of  $\phi$  are vector bundles of the same rank. By Proposition 4.1 the sheaf  $\mathcal{C}^{\text{ev}}$  is a sum of the degree 0 line bundles  $\mathcal{L}_I$ , and since the endomorphism bundle also has degree 0, the map is an isomorphism.

Corollary 4.7 (Morita equivalence, see [Bas68, Chapter 2]). The  $\mathcal{O}_E - \mathcal{C}^{ev}$  bimodule  $\mathcal{F}_U$  defines an equivalence of module categories

$$\begin{cases}
\mathcal{O}_E - mod & \longleftrightarrow & mod - \mathcal{C}^{ev} \\
\mathcal{L} & \longleftrightarrow & \mathcal{L} \otimes_{\mathcal{O}_E} \mathcal{F}_U \\
\mathcal{G} \otimes_{\mathcal{C}^{ev}} \mathcal{F}_U^* & \longleftrightarrow & \mathcal{G}
\end{cases}$$

where  $\mathcal{F}_U^* = \mathcal{H}om_{\mathcal{O}_E}(\mathcal{F}_U, \mathcal{O}_E)$ .

## PDF page 13

**Corollary 4.8** (Reid, 1972 [Rei72]). Let  $X = Q_1 \cap Q_2 \subset \mathbb{P}^{2g+1}$  be a smooth intersection of two quadrics and let E be the corresponding hyperelliptic curve. Let  $U_0 \subset V$  be a g-dimensional linear subspace such that  $\mathbb{P}(U_0^*) \subset X$ . Then the map

$$\varphi: \left\{ \begin{array}{ccc} \{U \in \mathbb{G}(g,V) \mid \mathbb{P}(U^*) \subset X\} & \longrightarrow & \operatorname{Pic}^0(E) \\ U & \longmapsto & \mathcal{F}_U \otimes_{\mathcal{C}^{\operatorname{ev}}} \mathcal{F}_{U_0}^* \end{array} \right.$$

is a bijection. If the ground field k has characteristic 0, it is an isomorphism.

*Proof.* By Lemma 4.3, a space  $U_0$  of dimension g such that  $\mathbb{P}(U_0^*) \subset X$  exists. We claim that  $\mathcal{F}_U \otimes_{\mathcal{C}^{\mathrm{ev}}} \mathcal{F}_{U_0}^*$  is an element of  $\mathrm{Pic}^0(E)$ . We know by Corollary 4.7 that  $\mathcal{F}_{U_0}$  and  $\mathcal{F}_U$  both define Morita equivalences. Hence  $\mathcal{L} := \mathcal{F}_U \otimes_{\mathcal{C}^{\mathrm{ev}}} \mathcal{F}_{U_0}^*$  must be an invertible object in  $\mathcal{O}_E - mod$ , hence a line bundle. This line bundle has degree 0 since  $\mathcal{F}_U \cong \mathcal{L} \otimes \mathcal{F}_{U_0}$  and both vector bundles have the same degree.

The map  $\varphi$  is injective because we can recover U from  $\mathcal{F}_U \cong \mathcal{L} \otimes \mathcal{F}_{U_0}$  as follows: by Proposition 5.6 (3) below, we can recover the  $C = \operatorname{Ext}_{P_X}(k,k)$ -module  $\operatorname{Ext}_{P_X}(P_U,k)$  from  $\mathcal{F}_U$ . The free resolution of  $P_U$ , hence  $U^{\perp}$ , can be obtained from  $\operatorname{Ext}_{P_X}(P_U,k)$  by Theorem 3.3.

Since the source and target of  $\varphi$  are projective and the target is connected, smooth, and of the same dimension as the source, the map is a surjective, hence a bijection. In case the ground field k has characteristic 0  $\varphi$  is thus an isomorphism. If k has positive characteristic it could be a purely inseperable morphism. Miles Reid proved in [Rei72, Theorem 4.8] that  $\{U \in \mathbb{G}(g,V) \mid \mathbb{P}(U^*) \subset X\}$  and  $\mathrm{Pic}^0(E)$  are isomorphic for arbitrary characteristic.

Remark 4.9. Our Macaulay2 package [EKS22] computes the action of  $Pic^0(E)$  on the space of maximal isotropic subspaces

$$\mathbb{G}(g,X) = \{ U \in \mathbb{G}(g,V) | \mathbb{P}(U^*) \subset X \}.$$

For a different approach to the group law on  $Pic^{0}(E)$  in terms of  $\mathbb{G}(g,X)$  see [Don80].

## 5. Tate resolutions of $P_X$ -modules from Clifford modules

The constructions in this section are inspired by the theory of Cohen–Macaulay approximations of Auslander and Buchweitz [AB89] and the construction of Tate resolutions as in [ES21]. Let R be a Noetherian local or graded Gorenstein ring, and let M be a finitely generated R-module. Let R be the minimal R-free resolution of R:

$$0 \longleftarrow M \longleftarrow F_0 \longleftarrow F_1 \longleftarrow F_2 \longleftarrow \cdots$$

We will use the notation  $N^* = \operatorname{Hom}_R(N,R)$  for the dual of an R-module N. If N is a maximal Cohen-Macaulay (MCM) module, that is, an R-module of depth dim R, then we have  $(N^*)^* \cong N$ , because R is Gorenstein.

The Tate resolution associated to M is a doubly infinite exact complex of free R-modules obtained as follows: The  $i^{\text{th}}$  syzygy module  $M_i = \ker(F_{i-1} \to F_{i-2})$  is an MCM module when  $i > \dim R$ , so  $M_i^* = \ker(F_i^* \to F_{i+1}^*)$  is also an MCM module.

Choose an integer  $i > \dim R$ , and let

$$\cdots \longrightarrow G_{i-2} \longrightarrow G_{i-1} \longrightarrow M_i^* \longrightarrow 0$$

be a minimal free resolution of  $M_i^*$ . The Tate resolution  $\mathbb{T}(M)$  of M is obtained by splicing the dual complex  $G^*$  with the complex  $F_i \longleftarrow F_{i+1} \longleftarrow \cdots$  to a doubly infinite complex

$$\mathbb{T}(M)$$
:  $\cdots \longleftarrow G_{i-2}^* \longleftarrow G_{i-1}^* \longleftarrow F_i \longleftarrow F_{i+1} \longleftarrow \cdots$ 

of free graded R-modules. This is an exact complex because both  $M_i = \ker(F_{i-1} \to F_{i-2})$  and  $M_i^* \cong \ker(F_i^* \to F_{i+1}^*)$  are MCM modules. Up to isomorphism this complex is independent of the choice of i and the choice of the minimal free resolutions. The dual complex  $\mathbb{T}(M)^*$  is exact as well.

## PDF page 14

*Example* 5.1. In case of a hypersurface ring R = P/(f) the Tate resolutions are the double infinite periodic complexes

$$\cdots \stackrel{\overline{\phi}}{\longleftarrow} R^n \stackrel{\overline{\psi}}{\longleftarrow} R^n \stackrel{\overline{\phi}}{\longleftarrow} R^n \stackrel{\overline{\psi}}{\longleftarrow} \cdots$$

obtained from matrix factorizations  $(\phi, \psi)$  of f, cf. [Eis80].

Remark 5.2. Auslander and Buchweitz [AB89] used Tate resolutions to define the MCM approximation of M for arbitrary Cohen-Macaulay rings. When R is Gorenstein, as in our case, we set  $M^{\text{es}} = \operatorname{coker} \left( G_1^* \to G_0^* \right)$ , the essential MCM approximation, so that  $M^{\text{es}}$  is an MCM over R. By [AB89] there is an induced map  $M^{\text{es}} \to M$  and the modules M and  $M^{\text{es}}$  have free resolutions that differ in only finitely many terms: If  $R^n \to M$  is a map from a graded free  $P_X$  module such that

$$0 \longleftarrow M \longleftarrow M^{\text{es}} \oplus R^n$$

is a surjection, then the kernel of this homomorphism has a finite free resolution of length codepth M-1. Auslander–Buchweitz define this homomorphism to be the MCM approximation of M if n is taken to be minimal.

**Proposition 5.3.** Let  $P_X = P/(q_1, ..., q_c)$  be the homogeneous coordinate ring of a complete intersection of quadrics. Let M be a  $P_X$ -module which has a linear resolution as a P-module. Then  $\operatorname{Ext}_{P_X}(M,k)$  is a  $C = \operatorname{Ext}_{P_X}(k,k)$ -module which is free as a  $k[t_1, ..., t_c]$ -module. If moreover M is a Cohen-Macaulay  $P_X$ -module of codimension  $\ell$  then the Tate resolution of M has the form

$$\cdots \longleftarrow P_X^{b_{-2}}(3) \longleftarrow P_X^{b_{-1}}(2) \longleftarrow P_X^{b_0}(1) \longleftarrow \cdots \longleftarrow P_X^{b_\ell}(-\ell+2) \longleftarrow 0$$

$$\downarrow \phi_0 \qquad \qquad \phi_1 \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi_\ell \qquad \qquad \phi$$

with  $b_{\ell-i} = a_i$  with an overlap of length  $\ell$ . The bottom row, which is a quotient complex, is the Eisenbud-Shamash resolution of M as a  $P_X$ -module, and the top row, a subcomplex, is its  $P_X$  dual.

*Proof.* As in the special case explained in the proof of Proposition 4.4, the Eisenbud–Shamash graded free resolution of M as a  $P_X$  module [Eis80, Theorem 7.2] can be constructed from a series of higher homotopies on a graded P-free resolution F of M. Because the  $q_i$  have degree 2, all the higher homotopies are linear maps, so the construction yields a minimal linear resolution of M whose underlying graded free module is a divided power algebra over  $P_X$  on C generators tensored with the underlying module of F, and this implies that  $\operatorname{Ext}_{P_X}(M,k)$  is a free module over the dual algebra,  $k[t_1,\ldots,t_C]$ .

If M is Cohen-Macaulay of codimension  $\ell$  then the  $(\ell+1)^{\text{th}}$  syzygy of M is a maximal Cohen-Macaulay module, and by [ES21] the Tate resolution of M has the given form.

In [ES21] there is an explicit description of all maps in the Tate resolution in case of a nested pair of complete intersections such as the following.

*Example* 5.4. Consider the coordinate ring  $P_U$  of a g-dimensional isotropic subspace U in the complete intersection X of two quadrics as a  $P_X$ -module. The Tate resolution  $\mathbb{T}(P_U)$  has an overlap of length  $\ell = \operatorname{codim}_X \mathbb{P}(U^*) = 2g - 1 - (g - 1) = g$ . In case g = 3 it has Betti table

$$\begin{array}{cccccccccccccccccccccccccccccccccccc$$

The vertical maps in the display of  $\mathbb{T}(P_U)$  are northwest diagonal maps in the Betti table, which are represented by matrices of quadratic forms. For example the map  $\phi_0$  as in Proposition 5.3 is given by a

## PDF page 15

$20 \times 1$  matrix of quadrics, represented in the Betti table by the northwest map from the left-most 1 on the lower to the 20 in the upper row. For arbitrary g we obtain the formulas

$$a_{2p} = \sum_{i=0}^{p} (p-i+1) {g+2 \choose 2i}$$
 and  $a_{2p+1} = \sum_{i=0}^{p} (p-i+1) {g+2 \choose 2i+1}$ 

for the ranks  $a_i$  in the lower row of the diagram above from the equations (4.2) and (4.3) in Section 4.

**Theorem 5.5.** Let  $C = Cliff(q_1, q_2)$  be the Clifford algebra over k[s,t] of a nonsingular complete intersection of two quadrics in  $\mathbb{P}^{2g+1}$ . Let N be a graded C-module that is free as a k[s,t]-module, and such that the corresponding vector bundles  $\mathcal{N}^{ev} = \widetilde{N^{ev}}$  and  $\mathcal{N}^{odd} = \widetilde{N^{odd}(1)}$  defined on the associated hyperelliptic curve E satisfies

$$\mathcal{N}^{odd} \cong \mathcal{N}^{ev} \otimes_{\mathcal{C}^{ev}} \mathcal{C}^{odd}$$
.

Let  $p \in E$  be a ramification point. There is a doubly infinite exact complex

$$\mathbb{T}(N): \cdots \longrightarrow F_i \longrightarrow F_{i+1} \longrightarrow \cdots$$

of free modules  $F_i = P_X^{a_i}(i) \oplus P_X^{b_i}(i+1)$  with Betti numbers  $a_i = h^1(\mathcal{N}^{ev}(ip))$  and  $b_i = h^0(\mathcal{N}^{ev}((i+1)p))$ . In terms of this decomposition, the complex  $\mathbb{T}(N)$  takes the form

$$\rightarrow H^{1}(\mathcal{N}^{\mathrm{ev}}) \otimes_{k} P_{X} \rightarrow H^{1}(\mathcal{N}^{\mathrm{ev}}(p)) \otimes_{k} P_{X}(1) \rightarrow H^{1}(\mathcal{N}^{\mathrm{ev}}(2p)) \otimes_{k} P_{X}(2) \rightarrow$$

$$\rightarrow H^{0}(\mathcal{N}^{\mathrm{ev}}(p)) \otimes_{k} P_{X}(p) \rightarrow H^{0}(\mathcal{N}^{\mathrm{ev}}(2p)) \otimes_{k} P_{X}(2) \rightarrow H^{0}(\mathcal{N}^{\mathrm{ev}}(3p)) \otimes_{k} P_{X}(3) \rightarrow .$$

*Proof.* We will use the notations  $x_i, e_i$  as defined in Section 3. Consider the sequence of maps

$$\cdots \xrightarrow{d} N_{i-1} \otimes_k P \xrightarrow{d} N_i \otimes_k P \xrightarrow{d} N_{i+1} \otimes_k P \xrightarrow{d} \cdots$$

defined by  $d(n \otimes_k r) = \sum_{i=1}^{2g+2} ne_i \otimes_k x_i r$ .

Computations similar to that at the beginning of Section 3 show that

$$d^2(n \otimes_k r) = \sum_{i,j} (ne_i e_j) \otimes_k (x_i x_j r) = ns \otimes_k q_1(x) r + nt \otimes_k q_2(x) r = n \otimes_{k[s,t]} (sq_1(x) + tq_2(x)) r,$$

where the last step uses the identification  $N \otimes_k P = N \otimes_{k[s,t]} P[s,t]$ .

Set  $A := N^{\text{ev}} \otimes_k P$  and  $B := N^{\text{odd}} \otimes_k P$ . The map d induces a matrix factorization

$$(A \longrightarrow B(0,1), B(0,1) \longrightarrow A(1,2))$$

of  $sq_1 + tq_2$  over the bi-graded polynomial ring  $k[s, t, x_1, ..., x_{2g+2}]$ . As in Example 5.1, this matrix factorization induces a 2-periodic resolution

$$\cdots \longrightarrow \overline{B}(-1,-1) \longrightarrow \overline{A} \longrightarrow \overline{B}(0,1) \longrightarrow \overline{A}(1,2) \longrightarrow \cdots$$

where  $\overline{A}$  and  $\overline{B}$  are restrictions of A and B to  $k[s,t,x_1,\ldots,x_{2g+2}]/(sq_1+tq_2)$ .

Sheafifying with respect to the variables (s,t) we get a doubly infinite exact complex

$$\cdots \longrightarrow \widetilde{B}(-1,-1) \longrightarrow \widetilde{A} \longrightarrow \widetilde{B}(0,1) \longrightarrow \widetilde{A}(1,2) \longrightarrow \cdots$$

of direct sums of line bundles on the hypersurface  $V(sq_1 + tq_2) \subset \mathbb{P}^1 \times \mathbb{A}^{2g+2}$ .

We define an exact complex of  $\mathcal{O}_{\mathbb{P}^1} \otimes P_X$ -modules by factoring out  $q_1$  on the set  $t \neq 0$  and  $q_2$  on the set  $s \neq 0$ , identified on the set where neither s nor t is zero with  $k\lceil s/t, t/s \rceil \otimes P/(q_1, q_2)$ .

Since the central element y of the even Clifford algebra anti-commutes with the action of the  $e_i$  on N by Remark 4.2 we may regard this also as a complex of  $\mathcal{O}_E \otimes P_X$ -modules that are box products of locally free  $\mathcal{O}_E$ -modules with graded free  $P_X$ -modules,

$$\mathbb{T}: \cdots \longrightarrow \mathcal{A}_E \boxtimes P_X \longrightarrow \mathcal{B}_E \boxtimes P_X(1) \longrightarrow \mathcal{A}_E(1) \boxtimes P_X(2) \longrightarrow \cdots$$

## PDF page 16

where use the fact that  $\mathcal{O}_E(1) \cong \mathcal{O}_E(2p)$ . Here  $\mathcal{A}_E = \mathcal{N}^{\text{ev}}$  and  $\mathcal{B}_E$  is isomorphic to

$$\mathcal{N}^{\text{odd}} = \mathcal{N}^{\text{ev}} \otimes_{\mathcal{C}^{\text{ev}}} \mathcal{C}^{\text{odd}} = \mathcal{N}^{\text{ev}}(p)$$

by Proposition 4.1, where the action of y on  $\mathcal{B}_E$  is induced by the action of -y on  $N^{\text{odd}}$ . Thus these are the vector bundles on E defined by the action of y or -y on the even and odd part of N respectively. In other words,  $\mathcal{B}_E \cong \iota^* \mathcal{N}^{\text{odd}}$ , where  $\iota: E \to E$  denotes the covering involution of  $E \to \mathbb{P}^1$ .

Let  $\rho: E \times \operatorname{Spec} P_X \to \operatorname{Spec} P_X$  denote the second projection. The desired Tate resolution  $\mathbb{T}(N)$  associated to the Clifford module N is essentially  $R\rho_*\mathbb{T}$ . Since  $\mathbb{T}$  is a complex, we get a spectral sequence, which we analyze as follows: truncate  $\mathbb{T}$  on the left to obtain a left bounded complex

$$L_i \longrightarrow \mathcal{A}_E(i) \boxtimes P_X(2i) \longrightarrow \mathcal{B}_E(i) \boxtimes P_X(2i+1) \longrightarrow \mathcal{A}_E(i+1) \boxtimes P_X(2i+2) \longrightarrow \cdots$$

and take a Čech resolution on E coming from a covering with two affine open subsets. We obtain a double complex:

The vertical homology of this double complex is a box product with the cohomology of  $A_E$  and  $B_E$  and their twists. The  $E_2$ -differentials of the spectral sequence of the double complex can be lifted to maps of the form  $H^1(A_E) \otimes P_X \to H^0(A_E(1)) \otimes P_X(2)$  on the  $E_1$ -page of the sequence. To do this, we choose k-vector space splittings h of the Čech sequence

$$(\alpha) 0 \longrightarrow H^0(\mathcal{A}_E) \longrightarrow C^0(\mathcal{A}_E) \longrightarrow C^1(\mathcal{A}_E) \longrightarrow H^1(\mathcal{A}_E) \to 0$$

and the corresponding sequences  $(\alpha_i)$  and  $(\beta_i)$  for the sheaves  $\mathcal{A}_E(i)$ 's and  $\mathcal{B}_E(i)$ 's respectively. We define the map

$$H^1(\mathcal{A}_E) \otimes P_X \longrightarrow H^0(\mathcal{A}_E(1)) \otimes P_X(2)$$

as the composition

$$H^{1}(\mathcal{A}_{E}) \otimes P_{X}$$

$$\downarrow^{h \otimes \mathrm{id}}$$

$$C^{1}(\mathcal{A}_{E}) \boxtimes P_{X} \longrightarrow C^{1}(\mathcal{B}_{E}) \boxtimes P_{X}(1)$$

$$\downarrow^{h \boxtimes \mathrm{id}}$$

$$C^{0}(\mathcal{B}_{E}) \boxtimes P_{X}(1) \longrightarrow C^{0}(\mathcal{A}_{E}(1)) \boxtimes P_{X}(2)$$

$$\downarrow^{h \otimes \mathrm{id}}$$

$$H^{0}(\mathcal{A}_{E}(1)) \otimes P_{X}(2).$$

## PDF page 17

Abusing notation we write  $\tilde{h}$  for all south arrows,  $\tilde{\partial}$  for all north arrows, and  $\varphi$  for all east arrows in the corresponding diagram

$$(4) \qquad H^{1}(\mathcal{A}_{E}(i)) \otimes P_{X}(2i) \stackrel{\varphi}{\longrightarrow} H^{1}(\mathcal{B}_{E}(i)) \otimes P_{X}(2i+1) \stackrel{\varphi}{\longrightarrow} H^{1}(\mathcal{A}_{E}(i+1)) \otimes P_{X}(2i+2)$$

$$\tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h}$$

$$C^{1}(\mathcal{A}_{E}(i)) \otimes P_{X}(2i) \stackrel{\varphi}{\longrightarrow} C^{1}(\mathcal{B}_{E}(i)) \otimes P_{X}(2i+1) \stackrel{\varphi}{\longrightarrow} C^{1}(\mathcal{A}_{E}(i+1)) \otimes P_{X}(2i+2)$$

$$\tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h}$$

$$C^{0}(\mathcal{A}_{E}(i)) \otimes P_{X}(2i) \stackrel{\varphi}{\longrightarrow} C^{0}(\mathcal{B}_{E}(i)) \otimes P_{X}(2i+1) \stackrel{\varphi}{\longrightarrow} C^{0}(\mathcal{A}_{E}(i+1)) \otimes P_{X}(2i+2)$$

$$\tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h} \qquad \tilde{\partial} \downarrow \tilde{h}$$

$$H^{0}(\mathcal{A}_{E}(i)) \otimes P_{X}(2i) \stackrel{\varphi}{\longrightarrow} H^{1}(\mathcal{B}_{E}(i)) \otimes P_{X}(2i+1) \stackrel{\varphi}{\longrightarrow} H^{0}(\mathcal{A}_{E}(i+1)) \otimes P_{X}(2i+2)$$

with four rows.

For  $\alpha \in H^1(\mathcal{A}_E) \boxtimes P_X$  we have

$$\alpha = \tilde{\partial}\tilde{h}\alpha \qquad \qquad \text{since } \partial h = \mathrm{id}_{H^1}$$

$$\Rightarrow \quad \varphi \alpha = \tilde{\partial}\varphi\tilde{h}\alpha \qquad \qquad \text{since } [\varphi,\tilde{\partial}] = 0$$

$$\Rightarrow \quad \tilde{h}\varphi\alpha = -\tilde{\partial}\tilde{h}\varphi\tilde{h}\alpha + \varphi\tilde{h}\alpha \qquad \qquad \text{since } \partial h + h\partial = \mathrm{id}_{C^1}$$

$$\Rightarrow \quad \varphi\tilde{h}\varphi\alpha = -\varphi\tilde{\partial}\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } \varphi^2 = 0$$

$$\Rightarrow \quad \varphi\tilde{h}\varphi\alpha = -\tilde{\partial}\varphi\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } [\varphi,\tilde{\partial}] = 0$$

$$\Rightarrow \quad \tilde{h}\varphi\tilde{h}\varphi\alpha = \tilde{\partial}\tilde{h}\varphi\tilde{h}\varphi\tilde{h}\alpha - \varphi\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } \partial h + h\partial = \mathrm{id}_{C^0}$$

$$\Rightarrow \quad \varphi\tilde{h}\varphi\tilde{h}\varphi\alpha = \tilde{\partial}\tilde{\mu}\varphi\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } \partial h + h\partial = \mathrm{id}_{C^0}$$

$$\Rightarrow \quad \varphi\tilde{h}\varphi\tilde{h}\varphi\alpha = \tilde{\partial}\varphi\tilde{h}\varphi\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } \varphi^2 = 0 \text{ and } [\varphi,\tilde{\partial}] = 0$$

$$\Rightarrow \quad \tilde{h}\varphi\tilde{h}\varphi\tilde{h}\varphi\alpha = \varphi\tilde{h}\varphi\tilde{h}\varphi\tilde{h}\alpha \qquad \qquad \text{since } h\partial = \mathrm{id}_{H^0}$$

$$\Rightarrow \quad (\tilde{h}\varphi\tilde{h}\varphi\tilde{h})\varphi = \varphi(\tilde{h}\varphi\tilde{h}\varphi\tilde{h}).$$

Thus with the lifted maps we obtain a double complex, whose total complex is our desired complex  $\mathbb{T}(N)$ :

$$\rightarrow H^{1}(\mathcal{A}_{E}) \otimes P_{X} \rightarrow H^{1}(\mathcal{B}_{E}) \otimes P_{X}(1) \rightarrow H^{1}(\mathcal{A}_{E}(1)) \otimes P_{X}(2)$$

$$\Rightarrow \oplus \qquad \Rightarrow \oplus \qquad \Rightarrow \oplus$$

$$\rightarrow H^{0}(\mathcal{B}_{E}) \otimes P_{X}(1) \rightarrow H^{0}(\mathcal{A}_{E}(1)) \otimes P_{X}(2) \rightarrow H^{0}(\mathcal{B}_{E}(1)) \otimes P_{X}(3).$$

The right truncated complexes are exact except at the first two position since the spectral sequence of  $(*_i)$  converges to the cohomology of  $L_i$ . Since we can take i arbitrarily large negative, the complex  $\mathbb{T}(N)$  is exact.

**Proposition 5.6.** Let M be a PX-module with a linear resolution as an P-module. Then

- (1)  $N = \operatorname{Ext}_{P_{\mathbf{x}}}(M, k)$  is a  $C = \operatorname{Ext}_{P_{\mathbf{x}}}(k, k)$ -module which is free as an k[s, t]-module.
- (2) The sheafifications  $\mathcal{N}^{\text{ev}}$  and  $\mathcal{N}^{\text{odd}} = \widetilde{N^{\text{odd}}(1)}$  satisfies

$$\mathcal{N}^{\text{odd}} \cong \mathcal{N}^{\text{ev}} \otimes_{\mathcal{C}^{\text{ev}}} \mathcal{C}^{\text{odd}}$$

- (3)  $N = H^0_*(\mathcal{N}^{\text{ev}}) \oplus H^0_*(\mathcal{N}^{\text{odd}})(-1)$  and the C-module N is determined by the  $\mathcal{C}^{\text{ev}}$ -module  $\mathcal{N}^{\text{ev}}$ .
- (4) The  $P_X$ -dual complex  $\mathbb{T}(N)^*$  is the Tate resolution  $\mathbb{T}(M)$  of M.

*Proof.* (1) Let  $0 \to F_c \to \cdots \to F_1 \to F_0 \to M \to 0$  be the linear P-resolution of M. Then by the Eisenbud-Shamash construction [Eis80, Theorem 7.2],  $\operatorname{Ext}_{P_X}(M,k) = N = N^{\operatorname{ev}} \oplus N^{\operatorname{odd}}$  is a free k[s,t]-module.

(2) We have

$$\operatorname{rk}_{k[s,t]} N^{\operatorname{ev}} = \sum_{i>0} \operatorname{rk}_{P} F_{2i}$$
 and  $\operatorname{rk}_{k[s,t]} N^{\operatorname{odd}} = \sum_{i>1} \operatorname{rk}_{P} F_{2i+1}$ .

## PDF page 18

Since  $\sum_{i=0}^{c} (-1)^i \operatorname{rk}_P F_i = 0$  the k[s,t]-modules  $N^{\operatorname{ev}}$  and  $N^{\operatorname{odd}}$  have equal rank. Theorem 3.3 shows that the minimal free  $P_X$ -resolution of M is isomorphic to  $\operatorname{Hom}_k(\operatorname{Ext}_{P_X}(M,k),P_X)$ . From this construction we see that if one of the maps

$$\operatorname{Ext}_{P_X}^i(M,k) \times \operatorname{Ext}_{P_X}^1(k,k) \longrightarrow \operatorname{Ext}_{P_X}^{i+1}(M,k)$$

were not surjective, then there would be a generator of the module  $\operatorname{Hom}_k(\operatorname{Ext}_{P_k}^{i+1}(M,k),k)$  which maps to zero in the complex. This is not possible because the complex is minimal. We conclude that the map

$$\mathcal{N}^{ev} \otimes_{\mathcal{C}^{ev}} \mathcal{C}^{odd} \longrightarrow \mathcal{N}^{odd}$$

is a surjective morphism of  $\mathcal{O}_E$ -vector bundles of the same rank and hence an isomorphism of  $\mathcal{C}^{\mathrm{ev}}$  modules.

(3) It follows that

$$\mathcal{N}^{odd} \otimes_{\mathcal{C}^{ev}} \mathcal{C}^{odd} \cong \mathcal{N}^{ev} \otimes_{\mathcal{C}^{ev}} \mathcal{C}^{odd} \otimes_{\mathcal{C}^{ev}} \mathcal{C}^{odd} \longrightarrow \mathcal{N}^{ev} \otimes \mathcal{H}$$

is also an isomorphism.

The formula for N follows because N is a free k[s,t]-module. Since  $C^{\text{ev}} = H^0_*(\mathcal{C}^{\text{ev}})$  and  $C^{\text{odd}} = H^0_*(\mathcal{C}^{\text{odd}})(-1)$  the maps above determine the maps  $N^{\text{ev}} \otimes_k C^{\text{odd}} \to N^{\text{odd}}$  and  $N^{\text{odd}} \otimes_k C^{\text{odd}} \to N^{\text{ev}}$ , and thus the C-module structure on N.

(4) By parts (1) and (2) we can apply Theorem 5.5. The dual of the  $H^0$ -strand of  $\mathbb{T}(N)$  coincides with  $\operatorname{Hom}_k(\operatorname{Ext}_{P_X}(M,k),P_X)$  by construction. Since  $\mathbb{T}(N)^*$  and  $\mathbb{T}(M)$  are exact minimal complexes which coincide for large homological degree, they are isomorphic.

*Example* 5.7. Thus in case g = 3 the Betti table

$$\begin{array}{cccccccccccccccccccccccccccccccccccc$$

of the Tate resolution of  $M = \mathbb{T}(H^0_*(\mathcal{F}_U \otimes_{\mathcal{C}^{\mathrm{ev}}} \mathcal{C}))$  has a second interpretation. It is also the cohomology table

$$(h^i(\mathcal{F}_U((j+1-i)p))_{\substack{i=0,1\\j\in\mathbb{Z}}}$$

of  $\mathcal{F}_{II}$  as a vector bundle on the hyperelliptic curve E.

**Theorem 5.8.** Let N be a C-module which is free over k[s,t] satisfying  $\mathcal{N}^{\text{odd}} \cong \mathcal{N}^{\text{ev}} \otimes_{\mathcal{C}^{\text{ev}}} \mathcal{C}^{\text{odd}}$ . Let  $\mathbb{T}(N)$  be the complex constructed in Theorem 5.5 whose terms are described by cohomology groups of  $\mathcal{A}_E = \mathcal{N}^{\text{ev}}$  and  $\mathcal{B} = \mathcal{N}^{\text{odd}}$  and their twists. The cokernel  $G_X$  of the map

$$H^1(\mathcal{B}_E(-1)) \otimes P_X(-1) \longrightarrow H^1(\mathcal{A}_E) \otimes P_X$$

which is a component of the differential  $F_{-1} \to F_0$  of  $\mathbb{T}(N)$ , is an Ulrich module if and only if  $H^1(\mathcal{B}_E)$  and  $H^0(\mathcal{B}_E)$  vanish.

*Proof.* If  $G_X$  is an Ulrich  $P_X$ -module, then it is its own MCM approximation. Hence the Tate resolution of  $G_X$  has non-overlapping strands so  $H^1(\mathcal{B}_E)$  and  $H^0(\mathcal{B}_E)$  vanish.

Conversely, if these groups vanish then  $G_X$  is a MCM module over  $P_X$  with a linear  $P_X$ -resolution, and from the form of the complex  $\mathbb{T}(N)$  we see that  $H^0(\mathcal{A}_E)$  and all terms to the left of it in the lower row must also vanish. To show that  $G_X$  is an Ulrich module we must prove that  $G_X$  has a linear resolution as a P-module

We first make the form of the  $P_X$ -resolution more explicit. The cohomological vanishing  $h^0(\mathcal{B}_E) = h^1(\mathcal{B}_E) = 0$  implies that  $\pi_*\mathcal{B}_E = \mathcal{O}_{\mathbb{P}^1}(-1)^{2r}$ , where  $r = \operatorname{rk}\mathcal{B}_E = \operatorname{rk}\mathcal{A}_E$ . Since  $\mathcal{B}(-p) \cong \mathcal{A}$  we have  $\deg \mathcal{A}_E = \deg \mathcal{B}_E - r$ . Thus  $H^0(\mathcal{A}_E) = 0$  and, by the Riemann-Roch formula,  $h^1(\mathcal{A}_E) = r$ . The form of the Tate resolution implies that the bundle  $\pi_*\mathcal{A}_E$  splits into a direct sum of copies of  $\mathcal{O}_{\mathbb{P}^1}(-1)$  and  $\mathcal{O}_{\mathbb{P}^1}(-2)$ . Indeed, there cannot be any summands of the form  $\mathcal{O}_{\mathbb{P}^1}(-d)$  with  $d \leq -3$  because there are no nonzero maps to this sheaf from  $\pi_*\mathcal{B}_E(-1) = \mathcal{O}_{\mathbb{P}^1}(-2)^{2r}$ . Hence

$$\pi_* \mathcal{A}_E = \mathcal{O}_{\mathbb{P}^1} (-1)^r \oplus \mathcal{O}_{\mathbb{P}^1} (-2)^r.$$

## PDF page 19

Since  $\pi_*\mathcal{B}_E(-1) = \mathcal{O}_{\mathbb{P}^1}(-2)^{2\operatorname{rk}\mathcal{B}_E}$  we see that  $G_X$  is defined by an  $r \times 2r$  matrix of linear forms and the  $P_X$ -free resolution of  $G_X$  has the form

$$\cdots \longrightarrow P_X^{(i+1)r}(-i) \longrightarrow \cdots \longrightarrow P_X^{2r}(-1) \stackrel{\phi_1}{\longrightarrow} P_X^r \longrightarrow G_X \longrightarrow 0.$$

We can now show that  $G_X$  has linear resolution as a P-module. Since  $G_X$  is maximal Cohen-Macaulay module over  $P_X$ , this statement can be checked after factoring out a maximal  $P_X$ -regular sequence z of linear forms in P. Note that  $P_X/zP_X$  has Hilbert function 1,2,1. The sequence z is also a regular sequence on  $G_X$  because  $G_X$  is a maximal Cohen-Macaulay module. From the resolution of  $G_X$  over  $P_X$  we see that the values of the Hilbert function of  $G_X/zG_X$  are  $r,0,0,\ldots$ ; that is,  $G_X/zG_X \cong k^r$ . As a module over P/zP this has a linear resolution, and thus  $G_X$  has a linear resolution as a P-module. Thus  $G_X$  is an Ulrich  $P_X$ -module.

Remark 5.9. The proof shows in particular that, the matrix

$$P^{2r}(-1) \xrightarrow{\phi_1} P^r$$

obtained by regarding the linear  $P_X$ -presentation of  $G_X$  as a matrix over P is a presentation matrix of  $G_X$  as a P-module.

Using the Morita equivalence between the hyperelliptic curve E and the Clifford algebra C we can make this more precise. Recall that a bundle  $\mathcal{B}$  on E has the Raynaud property if  $H^0(C,\mathcal{B}) = H^1(C,\mathcal{B}) = 0$ . We are now ready to prove parts of Theorem 1.1 from the introduction, which we repeat for the reader's convenience.

**Theorem 5.10.** There is a 1-1 correspondence between Ulrich bundles on the smooth complete intersection of two quadrics  $X \subset \mathbb{P}^{2g+1}$  and bundles with the Raynaud property on the corresponding hyperelliptic curve E of the form  $\mathcal{G} \otimes \mathcal{F}_U$ . The Ulrich bundle corresponding to a rank r vector bundle  $\mathcal{G}$  has rank  $r2^{g-2}$ .

If  $\mathcal{L}$  is a line bundle on E then  $\mathcal{L} \otimes \mathcal{F}_U$  does not have the Raynaud property, so the minimal possible rank of an Ulrich sheaf on X is  $2^{g-1}$ , and Ulrich bundles of rank  $2^{g-1}$  exist.

*Proof.* Let  $p \in E$  be a ramification point. Consider  $\mathcal{B} = \mathcal{G} \otimes \mathcal{F}_U$ ,  $\mathcal{A} = \mathcal{G}(-p) \otimes \mathcal{F}_U$  and the Clifford module  $N = \bigoplus_i H^0(\mathcal{A}(ip))$ . By Theorem 5.8  $\mathbb{T}(N)$  is the Tate resolution of the Ulrich module  $G_X = \operatorname{coker} \left(H^1(\mathcal{B}_E(-1)) \otimes P_X(-1) \to H^1(\mathcal{A}_E) \otimes P_X\right)$  if and only if  $H^0(\mathcal{B}) = H^1(\mathcal{B}) = 0$ . If  $r = \operatorname{rk} \mathcal{G}$  and the condition is satisfied then the corresponding Ulrich module  $G_X$  on X has rank  $G_X = r2^{g-2}$  since the number of generators of  $G_X$  is  $\operatorname{rk}(\mathcal{G} \otimes \mathcal{F}_U) = r2^g$ .

Conversely, suppose that M is an Ulrich module on  $P_X$ , and let  $N = \operatorname{Ext}_{P_X}(M,k)$ . This is a C-module, and thus an  $R_E$ -module which is a free k[s,t]-module by the Eisenbud-Shamash construction [Eis80, Theorem 7.2]. The odd part of its sheafification is thus of the form  $\mathcal{N}^{\operatorname{odd}} = \mathcal{G} \otimes_{\mathcal{O}_E} \mathcal{F}_U$  for some a vector bundle  $\mathcal{G}$  by Corollary 4.7, the Morita theorem. By Theorem 5.8  $\mathcal{G} \otimes_{\mathcal{O}_E} \mathcal{F}_U$  has the Raynaud property.

An Ulrich module of rank  $2^{g-2}$  would correspond to a line bundle  $\mathcal{L}$  on E such that  $\mathcal{L} \otimes \mathcal{F}_U$  has vanishing cohomology. By Corollary 4.8,  $\mathcal{L} \otimes \mathcal{F}_U = \mathcal{F}_{U'}(mp)$  for some maximal isotropic plane U' and some integer m. Thus  $\mathbb{T}(N)^*$  would be the Tate resolution of  $P_{U'}$  up to shift. But  $\mathbb{T}(P_{U'})$  has overlapping strands (in fact  $P_{U'}$  is not a MCM  $P_X$ -module).

The existence of Ulrich bundles of rank  $2^{g-1}$  is proven in Section 6.

**Proposition 5.11.** Ulrich bundles of rank  $r2^{g-2}$  on a smooth complete intersections of two quadrics in  $\mathbb{P}^{2g+1}$  do not exist if  $r \cdot g \equiv 1 \mod 2$ .

*Proof.* If  $\mathcal{G}$  is a vector bundle on E of rank r and degree d then

$$\deg(\mathcal{G}\otimes\mathcal{F}_U) = \deg\mathcal{G}\operatorname{rk}\mathcal{F}_U + \operatorname{rk}\mathcal{G}\operatorname{deg}\mathcal{F}_U = d2^g + rg2^{g-1}$$

## PDF page 20

by Proposition [4.5](#page-11-1) and

$$\chi(\mathcal{G}\otimes\mathcal{F}_U) = \deg(\mathcal{G}\otimes\mathcal{F}_U) + \operatorname{rk}(\mathcal{G}\otimes\mathcal{F}_U)(1-g) = d2^g + rg2^{g-1} + r2^g(1-g)$$

by Riemann-Roch. Thus *χ*(G ⊗ F*<sup>U</sup>* ) = 0 implies *r* ⋅ *g* ≡ 0 mod 2. □

For small *g* we constructed Ulrich bundles of rank 2 *g*−1 from sufficiently general rank 2 bundles G on *E* with our Macaulay2 package [\[EKS22\]](#page-23-2). Consider the direct sum G<sup>0</sup> = L<sup>0</sup> ⊕L*<sup>g</sup>* of two general line bundle L*<sup>i</sup>* of degree *i*. In case of *g* = 3 the cohomology table of the bundle G<sup>0</sup> ⊗ F*<sup>U</sup>* is the sum of two tables, one of which we displayed in Example [5.7](#page-17-1) in case of *g* = 3. The other is a shifted version of that table.

So in case of *g* = 3 the cohomology table of G<sup>0</sup> ⊗ F*<sup>U</sup>* has shape

$$\begin{array}{cccccccccccccccccccccccccccccccccccc$$

If for a general extension 0 → L<sup>0</sup> → G → L<sup>3</sup> → 0 the connecting homomorphisms are of maximal rank, then the cohomology table of G ⊗ F*<sup>U</sup>* has the form

⋯ 64 48 32 16 16 32 48 64 ⋯*.*

and G gives rise to an Ulrich bundle of rank 2 ⋅ 2 *g*−2 . In special cases, for small *g* we verified that this does occur with Macaulay2 [\[GS\]](#page-23-10) using our package [\[EKS22\]](#page-23-2). With the same idea we constructed Ulrich bundles of rank 3 ⋅ 2 *g*−2 in special cases for *g* = 2.

However we were not able to control the cohomology of G ⊗ F*<sup>U</sup>* theoretically well enough to prove the existence of rank 2 *<sup>g</sup>*−<sup>1</sup> Ulrich bundle for every *X*.

#### **6. Ulrich bundles of rank** 2 *g*−1

In this section we prove that a smooth complete intersection of two quadrics in P 2*g*+2 , and therefore also in P 2*g*+1 , carries an Ulrich bundle of rank 2 *g*−1 . Our construction uses the construction of Ulrich bundles on a single quadric by Knörrer, which we now review.

**Theorem 6.1** (*cf.* [\[Knö87\]](#page-24-0))**.** *The quadric q<sup>n</sup>* = ∑ *n i*=0 *xiy<sup>i</sup> has the matrix factorization* (*ϕn,ψn*) *of size* 2 *n defined recursively by ϕ*<sup>0</sup> = (*x*0)*,ψ*<sup>0</sup> = (*y*0) *and*

$$\varphi_n = \begin{pmatrix} x_n & \varphi_{n-1} \\ \psi_{n-1} & -y_n \end{pmatrix}, \quad \psi_n = \begin{pmatrix} y_n & \varphi_{n-1} \\ \psi_{n-1} & -x_n \end{pmatrix}$$

*for n* ≥ 1*.*

Let (*A,B*) = (*ϕn,ψn*) and consider the matrix factorizations

$$(A(x,y),B(x,y))$$
 and  $(A(v,w),B(v,w))$ 

of *q*(*x,y*) = ∑ *n i*=0 *xiy<sup>i</sup>* and *q*(*v,w*) = ∑ *n i*=0 *viw<sup>i</sup>* respectively over the ring *P* ∶= *k*[*x*∣*y,v*∣*w*], where *x*∣*y* denotes the catenation *x*0*,...,xn,y*0*,...,y<sup>n</sup>* and similarly for *v*∣*w*.

## **Proposition 6.2.** *Let*

$$\widetilde{q}(v,w,x,y) = \sum_{i=0}^{n} (x_i w_i + y_i v_i) = (v|w) \cdot (y|x).$$

*There is an identity*

$$(A(x,y) \quad A(v,w)) \begin{pmatrix} B(v,w) \\ B(x,y) \end{pmatrix} = \widetilde{q}(v,w,x,y) \mathrm{id}_{2^n}.$$

## PDF page 21

*Proof.* Since A(x,y) + A(y,w) = A(x+y,y+w) and B(x,y) + B(y,w) = B(x+y,y+w) we have

$$A(x+v,y+w)B(x+v,y+v) = q(x+v,y+w)id_{2^n}.$$

The mixed terms give

$$A(x,y)B(v,w) + A(v,w)B(x,y) = \widetilde{q}(v,w,x,y)\mathrm{id}_{2^n}.$$

Thus if we restrict the matrices in Proposition 6.2 to an isotropic subspace  $\Sigma$  of  $\widetilde{q}$  we get a complex and we will see that, for a sufficiently general choice of the isotropic subspace, the restriction to  $\Sigma$  is a minimal free resolution of an Ulrich module over  $P_{\Sigma}$ .

To define the isotropic subspace, let  $\Lambda$  be a skew-symmetric  $2(n+1) \times 2(n+1)$  matrix of scalars, and set

$$G_{\Lambda} = \begin{pmatrix} 0 & \mathrm{id}_{n+1} \\ \mathrm{id}_{n+1} & 0 \end{pmatrix} \Lambda.$$

We have

$$(x|y)G_{\Lambda} \cdot (y|x) = (y|x)\Lambda \cdot (y|x) = 0$$

and thus the equation  $(v|w) = (x|y)G_{\Lambda}$  defines an isotropic subspace of  $\widetilde{q}(v, w, x, y)$ .

The matrices

$$A_1 = A(x, y), B_1 = B(x, y)$$
 and  $A_2 = A((x|y)G_{\Lambda}), B_2 = B((x|y)G_{\Lambda})$ 

define matrix factorizations of  $q_1 = q(x, y)$  and  $q_2 = q((x|y)G_{\Lambda})$ ). Let

$$A_{\Lambda} = A_1 | A_2$$

be the concatenation, which is a  $2^n \times 2^{n+1}$  matrix in the 2n+2 variables  $x_0, \dots, y_n$ 

**Theorem 6.3.** For a general choice of  $\Lambda$  the ring  $k[x_0,...,y_n]/(q_1,q_2)$  is a complete intersection with isolated singularities and

$$M_{\Lambda} := \operatorname{coker} A_{\Lambda}$$

is an Ulrich module of rank  $2^{n-2}$  over this ring.

*Proof.* Set  $P = k[x_0, ..., y_n]$ . For each  $\Lambda$  we have maps

$$0 \longleftarrow M_{\Lambda} \longleftarrow P^{2^{n}} \stackrel{A_{1}}{\longleftarrow} P^{2^{n+1}}(-1) \stackrel{B_{2}}{\longleftarrow} P^{2^{n}}(-2) \longleftarrow 0.$$

By our choice of  $A_2$  and  $B_2$  this is a complex.

We claim that for a general choice of  $\Lambda$  the ideal  $(q_1, q_2)$  is a prime ideal of codimension 2 with isolated singularities. It suffices to prove this for a particular choice of  $\Lambda$ .

We will actually prove the result for matrices  $\Lambda$  of the form

$$\Lambda = \begin{pmatrix} 0 & D \\ -D & 0 \end{pmatrix}$$

where D is a diagonal matrix with entries  $d_i$  such that

$$d_0,\ldots,d_n,-d_0,\ldots,-d_n$$

are 2(n+1) different values. In this case

$$G_{\Lambda} = \begin{pmatrix} -D & 0 \\ 0 & D \end{pmatrix}, \quad A_{\Lambda} = (A(x_0, \dots, x_n, y_0, \dots, y_n) | A(-d_0 x_0, \dots - d_n x_n, d_0 y_0, \dots, d_n y_n),$$

and

$$q_2 = q_1(-d_0x_0, \dots, -d_nx_n, d_0y_0, \dots, d_ny_n) = -\sum_{i=0}^n d_i^2x_iy_i.$$

## PDF page 22

We will now show that  $V(q_1, q_2)$  is singular precisely at the coordinate points. The jacobian matrix of  $(q_1, -q_2)$  is

$$\begin{pmatrix} y_0 & y_1 & \dots & y_n & x_0 & \dots & x_n \\ d_0^2 y_0 & d_1^2 y_1 & \dots & d_n^2 y_n & d_0^2 x_0 & \dots & d_n^2 x_n \end{pmatrix}$$

The squares  $d_0^2, \ldots, d_n^2$  are pairwise distinct, since  $d_0, \ldots, d_n, -d_0, \ldots, -d_n$  are 2(n+1) distinct values by assumption. Thus the zero locus of the ideal of  $2 \times 2$  minors of the jacobian matrix is the union of the n+1 lines  $L_i = V(\bigcup_{j \neq i} \{x_j, y_j\})$  defined by those linear combinations of the two rows that do not consist of independent linear forms. These lines intersect  $V(q_1, q_2)$  in the 2n+2 coordinate points. It follows that  $(q_1, q_2)$  has codimension 2 and isolated singularities, and thus is prime.

Since each  $q_i$  is prime and  $A_i$  is part of a matrix factorization of  $q_i$ , the determinant of  $A_i$  is a power of  $q_i$ . Thus if  $\Lambda$  is general, the maximal minors of  $A_{\Lambda}$  generate an ideal of codimension at least 2, and similarly for  $B_{\Lambda}$  so the complex is exact by [BE73].

We conclude that

ann 
$$M_{\Lambda} = (q_1, q_2)$$

since any element of ann  $M_{\Lambda} \setminus (q_1, q_2)$  would lead to a support of codimension at least 3. Thus  $M_{\Lambda}$  is an Ulrich module over the ring  $P/(q_1, q_2)$  and the degree of  $M_{\Lambda}$  is  $2^n$ , so the rank of  $M_{\Lambda}$  as an  $P/(q_1, q_2)$ -module is  $2^{n-2}$ .

**Theorem 6.4.** Let k be an algebraically closed field of char  $k \neq 2$ , and  $X \subset \mathbb{P}^{2n}$  be a smooth complete intersection of two quadrics. Then X carries an Ulrich bundle of rank  $2^{n-2}$ .

**Corollary 6.5.** Let k be an algebraically closed field of char  $k \neq 2$ , and  $X \subset \mathbb{P}^{2g+1}$  be a smooth complete intersection of two quadrics. Then X carries an Ulrich bundle of rank  $2^{g-1}$ .

*Proof of Corollary 6.5.* Any smooth complete intersection in  $\mathbb{P}^{2g+1}$  is a hyperplane section of a smooth complete intersection in  $\mathbb{P}^{2g+2}$ . Taking n=g+1, the restriction of the Ulrich module constructed in Theorem 6.4 is an Ulrich module of rank  $2^{g-1}$ .

Proof of Theorem 6.4. We obtain an Ulrich module on some smooth complete intersection by restricting  $M_{\Lambda}$  from above to a general hyperplane  $H = \mathbb{P}^{2n} \subset \mathbb{P}^{2n+1}$ . The intersection will be smooth because  $V(q_1, q_2)$  has only isolated singularities. To prove that every smooth complete intersection carries an Ulrich module we need additional arguments. The complete intersection  $V(q'_1, q'_2)$  of two quadrics in  $\mathbb{P}^{2n}$  is smooth if and only if the discriminant

$$f = \text{dethess}(sq'_1 + q'_2) \in k[s]$$

of the pencil has 2n+1 distinct roots, and in that case  $q_1'$  and  $q_2'$  can be simultaneously diagonalized by the argument given at the beginning of Section 4. Thus it suffices to construct an Ulrich module M' on a the complete intersection  $V(q_1',q_2')$  whose discriminant has any given set of 2n+1 distinct roots. In the proof of Theorem 6.3 we constructed an Ulrich module for  $q_1 = \sum_{i=0}^n x_i y_i$  and  $q_2 = -\sum_{i=0}^n d_i^2 x_i y_i$  for distinct values  $d_0^2, \ldots, d_n^2$ . Since k is algebraically closed there exists an Ulrich module for  $V(\sum_{i=0}^n x_i y_i, \sum_{i=0}^n a_i x_i y_i)$  for every tuple of distinct values  $a_0, \ldots, a_n$ . The corresponding Hessian is

$$H = \begin{pmatrix} 0 & D' \\ D' & 0 \end{pmatrix} \text{ with a diagonal matrix } D' = \begin{pmatrix} s + a_0 \\ & \ddots \\ & & s + a_n \end{pmatrix}.$$

We restrict the quadrics to the subspace generated by the columns of the  $(2n+2) \times (2n+1)$  matrix of

$$B = \begin{pmatrix} 1 & & 0 \\ & \ddots & \\ 0 & & 1 \\ b_0 & \dots & b_{2n} \end{pmatrix}.$$

## PDF page 23

Setting  $\ell_i = s + a_i$  the Hessian of the restricted pencil is

$$B^{t}HB = \begin{pmatrix} & & & \ell_{n}b_{0} & \ell_{0} & & \\ & 0 & & \vdots & & \ddots & \\ & & & \ell_{n}b_{n-1} & & & \ell_{n-1} \\ \ell_{n}b_{0} & \dots & \ell_{n}b_{n-1} & 2\ell_{n}b_{n} & \ell_{n}b_{n+1} & \dots & \ell_{n}b_{2n} \\ \ell_{0} & & & \ell_{n}b_{n+1} & & & \\ & \ddots & & \vdots & & 0 & \\ & & & \ell_{n-1} & \ell_{n}b_{2n} & & \end{pmatrix}.$$

Direct computation shows that the determinant of this matrix is

$$f = (-1)^n 2h \prod_{i=0}^n \ell_i = (-1)^n 2h \prod_{i=0}^n (s + a_i)$$

with

$$h = \sum_{i=0}^{n-1} (b_i b_{i+n+1} \prod_{j \neq i} (s + a_j)) - b_n \prod_{j \neq n} (s + a_j).$$

Since the coefficients of  $\prod_{j\neq i}(s+a_j)$  are the elementary symmetric functions  $e_{i,k}$  on  $\{a_0,\ldots,a_n\}\setminus\{a_i\}$ , we obtain

(6.1) 
$$h = (b_0 b_{n+1}, \dots, b_{n-1} b_{2n}, -b_n) E \begin{pmatrix} s^n \\ \vdots \\ s \\ 1 \end{pmatrix}$$

where  $E = (e_{i,k})_{\substack{i=0,\dots,n\\k=0,\dots,n}}$ . We claim that


$$\det E = \prod_{0 \le i < j \le n} (a_i - a_j).$$

Regarding the  $a_i$ 's as variables, we see that  $\det E \in k[a_0,\ldots,a_n]$  is not identically zero, because the term  $\prod_{i=0}^{n-1} a_i^{n-i}$  occurs precisely once in the determinant as the product of the leading terms  $1,a_0,a_0a_1,\ldots,a_0a_1\ldots a_{n-1}$  of the diagonal entries. On the other hand  $(a_i-a_j)$  is a factor of  $\det E \in k[a_0,\ldots,a_n]$  because if  $a_i=a_j$  then the matrix E has two equal rows. So these linear forms are factors of  $\det E \in k[a_0,\ldots,a_n]$ , and their product coincides with  $\det E$  for degree reasons and by comparing the leading term.

Thus if the  $a_i$  are distinct, then E is invertible, and every polynomial h of degree n in k[s] can be represented in the form (6.1). In particular, we can choose  $b_0, \ldots, b_{2n} \in k$  such that the discriminant f is equal to  $\prod_{i=0}^n (s+a_i) \prod_{i=1}^n (s+c_i)$  for any 2n+1 distinct non-zero values  $a_0, \ldots, a_n, c_1, \ldots, c_n \in k$ . A smooth complete intersection of 2 quadrics in  $\mathbb{P}^{2n}$  is determined up to projective equivalence by the 2n+1 distinct roots of its discriminant, this concludes the proof.

## References

- [AB89] M. Auslander and R.-O. Buchweitz, *The homological theory of maximal Cohen-Macaulay approximations*, Mém. Soc. Math. Fr., Nouv. Sér. **38** (1989), 5–37.
- [Bas68] H. Bass, Algebraic K-theory, W. A. Benjamin, Inc., New York-Amsterdam, 1968.
- [BEH<sup>+</sup>24] A. Beauville, A. Etesse, A. Höring, J. Liu, and C. Voisin, Symmetric tensors on the intersection of two quadrics and lagrangian fibration, Moduli 1 (2024), Article ID e4.
- [BE73] D. A. Buchsbaum and D. Eisenbud, What makes a complex exact?, J. Algebra 25 (1973), 259-268.

## PDF page 24

- [BEH87] R.-O. Buchweitz, D. Eisenbud, and J. Herzog, *Cohen-Macaulay modules on quadrics*, in: *Singularities, representation of algebras, and vector bundles* (Lambrecht, 1985), Lecture Notes in Math., vol. **1273**, Springer, Berlin, 1987, pp. 58–116.
- [Buc21] R.-O. Buchweitz, *Maximal Cohen-Macaulay modules and Tate cohomology. With appendices by Luchezar L. Avramov, Benjamin Briggs, Srikanth B. Iyengar and Janina C. Letz*, Math. Surv. Monogr., vol. **262**, Providence, RI: American Mathematical Society, 2021.
- [CKL21] Y. Cho, Y. Kim, and K.-S. Lee, *Ulrich bundles on intersections of two 4-dimensional quadrics*, Int. Math. Res. Not. **2021** (2021), no. 22, 17277–17303.
- [DR76] U. V. Desale and S. Ramanan, *Classification of vector bundles of rank 2 on hyperelliptic curves*, Invent. Math. **38** (1976), 161–185.
- [Don80] R. Donagi, *Group law on the intersection of two quadrics*, Ann. Sc. Norm. Super. Pisa, Cl. Sci., IV. Ser. **7** (1980), 217–239.
- [EFS03] D. Eisenbud, G. Fløystad, and F.-O. Schreyer, *Sheaf cohomology and free resolutions over exterior algebras*, Trans. Am. Math. Soc. **355** (2003), no. 11, 4397–4426.
- [Eis80] D. Eisenbud, *Homological algebra of a complete intersection, with an application to group representations*, Trans. Am. Math. Soc. **260** (1980), 35–64.
- [EKS22] D. Eisenbud, Y. Kim, and F.-O. Schreyer, *Macaulay2 package "Clifford algebra of a pencil of quadratic forms"*, Available at [https://macaulay2.com/doc/Macaulay2/share/doc/Macaulay2/](https://macaulay2.com/doc/Macaulay2/share/doc/Macaulay2/PencilsOfQuadrics/html/index.html) [PencilsOfQuadrics/html/index.html](https://macaulay2.com/doc/Macaulay2/share/doc/Macaulay2/PencilsOfQuadrics/html/index.html), 2022.
- [ES03] D. Eisenbud and F.-O. Schreyer, *Resultants and Chow forms via exterior syzygies*, J. Amer. Math. Soc. **16** (2003), no. 3, 537–579, With an appendix by Jerzy Weyman.
- [ES21] , *Tate resolutions and MCM approximations*, in: *Commutative algebra. 150 years with Roger and Sylvia Wiegand.* Combined proceedings: second international meeting on commutative algebra and related areas, SIMCARA, Universidade de São Paulo, São Carlos, Brazil, July 22–26, 2019 and AMS special session on commutative algebra. In celebration of the 150th birthday of Roger and Sylvia Wiegand, University of Wisconsin-Madison, Wisconsin, September 14–15, 2019, Providence, RI: American Mathematical Society, 2021, pp. 35–47.
- [FL10] G. Farkas and K. Ludwig, *The Kodaira dimension of the moduli space of Prym varieties*, J. Eur. Math. Soc. ( JEMS) **12** (2010), no. 3, 755–795.
- [Gan59] F. R. Gantmacher, *The theory of matrices. Vols. 1, 2*, Chelsea Publishing Co., New York, 1959, Translated by K. A. Hirsch.
- [GS] D. R. Grayson and M. E. Stillman, *Macaulay2, a software system for research in algebraic geometry*, Available at <https://macaulay2.com>.
- [Haa91] U. Haag, *Diskriminantenalgebren quadratischer Formen. (Discriminant algebras of quadratic forms)*, Arch. Math. **57** (1991), no. 6, 546–554.
- [Jac46] C. G. J. Jacobi, *Über eine neue Methode zur Integration der hyperelliptischen Differentialgleichungen und über die rationale Form ihrer vollständigen algebraischen Integralgleichungen*, J. Reine Angew. Math. **32** (1846), 220–226.
- [Jac80] N. Jacobson, *Basic Algebra II*, San Francisco: W. H. Freeman and Company, XX, 1980.
- [Kap89] M. M. Kapranov, *On the derived category and K-functor of coherent sheaves on intersections of quadrics*, Math. USSR, Izv. **32** (1989), no. 1, 191–204.

## PDF page 25

- [Knö87] H. Knörrer, *Cohen-Macaulay modules on hypersurface singularities. I*, Invent. Math. **88** (1987), 153–164.
- [Kuz08] A. Kuznetsov, *Derived categories of quadric fibrations and intersections of quadrics*, Adv. Math. **218** (2008), no. 5, 1340–1369.
- [Mum84] D. Mumford, *Tata lectures on theta. II: Jacobian theta functions and differential equations.* With the collaboration of C. Musili, M. Nori, E. Previato, M. Stillman, and H. Umemura, Prog. Math., vol. **43**, Birkhäuser, Cham, 1984.
- [New68] P. E. Newstead, *Stable bundles of rank 2 and odd degree over a curve of genus 2*, Topology **7** (1968), 205–215.
- [PP05] A. Polishchuk and L. Positselski, *Quadratic algebras.*, Univ. Lect. Ser., vol. **37**, Providence, RI: American Mathematical Society, 2005.
- [Rei72] M. Reid, *The complete intersection of two or more quadrics*, Thesis, University of Cambridge, 1972.
- [Sjö76] G. Sjödin, *A set of generators for Extr*(*k,k*), Math. Scand. **38** (1976), 199–210.
- [Tat57] J. Tate, *Homology of Noetherian rings and local rings*, Illinois J. Math. **1** (1957), 14–27.
