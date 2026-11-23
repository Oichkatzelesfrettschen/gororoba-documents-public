Source: https://eisenbud.github.io/papers/pdfs/2021-002.pdf
PDF sha256: a42c8a1245f74ef11cbb21e793cf5a605f8d5d7832b9ad544a4b4d08014d6c31
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: text-layer)

# Transcription of eisenbud_2021_layered_resolutions_cohen_macaulay_modules.pdf

Transcription of `eisenbud_2021_layered_resolutions_cohen_macaulay_modules.pdf` in this directory, 23 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

© 2021 European Mathematical Society
Published by EMS Press. This work is licensed under a CC BY 4.0 license.

David Eisenbud · Irena Peeva

# Layered resolutions of Cohen-Macaulay modules

Received January 20, 2018

**Abstract.** Let S be a Gorenstein local ring and suppose that M is a finitely generated Cohen–Macaulay S-module of codimension c. Given a regular sequence  $f_1, \ldots, f_c$  in the annihilator of M we set  $R = S/(f_1, \ldots, f_c)$  and construct *layered* S-free and R-free resolutions of M. The construction inductively reduces the problem to the case of a Cohen–Macaulay module of codimension c-1 and leads to the inductive construction of a higher matrix factorization for M. In the case where M is a sufficiently high R-syzygy of some module of finite projective dimension over S, the layered resolutions are minimal and coincide with the resolutions defined from higher matrix factorizations we described in [EP]. Our results provide a characterization of all MCM modules over a complete intersection in terms of higher matrix factorizations.

**Keywords.** Free resolutions, complete intersections, CI operators, Eisenbud operators, maximal Cohen–Macaulay modules

## 1. Introduction

Recall that if R is a local ring, then a finitely generated R-module N is called a *maximal Cohen–Macaulay module* (abbreviated MCM) if depth(N) = dim(R).

Let S be a regular local ring and suppose that M is a finitely generated Cohen–Macaulay S-module of codimension c. Given a regular sequence  $f_1, \ldots, f_c$  in the annihilator of M, so that M is a MCM  $S/(f_1, \ldots, f_c)$ -module, we construct an S-free resolution

$$\mathbf{L}\uparrow^{S}(M, f_1, \ldots, f_c),$$

and an  $R := S/(f_1, \ldots, f_c)$ -free resolution

$$\mathbf{L}\downarrow_R(M, f_1, \ldots, f_c)$$

of *M*. These resolutions are constructed through an induction on the codimension, and each of them comes with a natural filtration by subcomplexes; we call them *layered resolutions*.

D. Eisenbud: Mathematics Department, University of California at Berkeley, Berkeley, CA 94720, USA; e-mail: de@msri.org

I. Peeva: Mathematics Department, Cornell University, Ithaca, NY 14853, USA

Mathematics Subject Classification (2020): Primary 13D02, 13C14, 13H10, 14M10

## PDF page 2

The inductive construction of the resolutions follows a pattern often seen in results about complete intersections in singularity theory and algebraic geometry. It allows us to exploit the fact that we can choose the regular sequence to be in general position with respect to M. In this way we achieve minimality for high R-syzygies, and we give necessary and sufficient conditions for minimality in general.

We now explain the inductive constructions. For brevity, we will always abbreviate the phrase "maximal Cohen–Macaulay" to "MCM".

In the base case of the induction, c = 0, M is 0 and the layered resolutions are trivial. For the inductive step we think of R as a quotient,  $R = R'/(f_c)$ , where  $R' = S/(f_1, \ldots, f_{c-1})$  and consider the MCM approximation

$$\alpha: M' \oplus B_0 \twoheadrightarrow M$$

of M as an R'-module, in the sense of Auslander–Buchweitz [AB]: here  $B_0$  is a free R'-module, M' is an MCM R'-module without free summand and the kernel  $B_1$  of the surjection  $\alpha$  has finite projective dimension. In our case  $B_1$  is a free R'-module (Lemma 3.4) and we write  $\mathbf{B}^S$  for the complex of free S-modules

$$\mathbf{B}^S: B_1^S \to B_0^S$$

obtained by lifting the map  $B_1 \xrightarrow{b} B_0$  back to S. See Section 3 for details.

Layered resolution over S (Section 4)

For the layered resolution of M over S we let  $\mathbf{K}$  be the Koszul complex resolving R' as an S-module and let  $\mathbf{L}' = \mathbf{L} \uparrow^S (M', f_1, \dots, f_{c-1})$  be the layered resolution constructed earlier in the induction. There is an induced map  $B_1^S \xrightarrow{\psi} L_0'$  which, in turn, induces a map of complexes  $\mathbf{K} \otimes \mathbf{B}^S \to \mathbf{L}'$  whose mapping cone we define to be the layered S-free resolution of M with respect to  $f_1, \dots, f_c$ .

Layered resolution over R (Section 6)

One way to construct the layered resolution of M over R, is to show (Section 9) that there is a periodic exact sequence

$$\cdots \rightarrow R \otimes B_1 \rightarrow R \otimes (M' \oplus B_0) \rightarrow R \otimes B_1 \rightarrow R \otimes (M' \oplus B_0) \rightarrow M \rightarrow 0;$$

this generalizes the periodic R-free resolution for a module over a hypersurface described in [Ei1] (Corollary 9.2). In the case c=1, the module M' is zero, and the layered resolution is this periodic complex.

As M' is an MCM module over R', the complex  $R \otimes \mathbf{L} \downarrow_{R'}(M', f_1, \ldots, f_{c-1})$  is an R-free resolution of  $R \otimes M'$ . The layered resolution of M over R can be constructed from the double complex obtained by replacing  $R \otimes M'$  with  $R \otimes \mathbf{L} \downarrow_{R'}(M', f_1, \ldots, f_{c-1})$ , but it is simpler to do something a little different, explained in Section 6: Set  $\mathbf{T}' = \mathbf{L} \downarrow^{R'}(M', f_1, \ldots, f_{c-1})$ , the layered resolution constructed earlier in the induction. The

## PDF page 3

layered R-free resolution of M with respect to  $f_1, \ldots, f_c$  is obtained from  $\mathbf{T}'$  by the Shamash construction applied to the box complex

where b and  $\psi$  are the maps listed above.

## Filtrations and layers

Each of the layered resolutions has a natural filtration, whose subquotients are the layers; these will be described in Subsections 4.2 and 6.2. However the subcomplexes in the filtration are easy to describe:

Let  $R(i) := S/(f_1, ..., f_i)$ , and let M(i) be the essential MCM approximation of M over R(i) as defined in Section 3. The layered resolution  $\mathbf{L} \uparrow^S(M, f_1, ..., f_c)$  is filtered by the sequence of subresolutions:

$$\mathbf{L}\uparrow^{S}(M(1), f_1) \subset \mathbf{L}\uparrow^{S}(M(2), f_1, f_2) \subset \cdots$$

Similarly, the layered resolution  $\mathbf{L}\downarrow_R(M, f_1, \dots, f_c)$  is filtered by the sequence of sub-resolutions:

$$R \otimes \mathbf{L}\downarrow_{R(1)}(M(1), f_1) \subset R \otimes \mathbf{L}\downarrow_{R(2)}(M(2), f_1, f_2) \subset \cdots$$

# Minimality

Our criteria for the minimality of the layered resolutions is presented in Section 7. They imply that, when the residue field of S is infinite, the layered resolutions can be taken to be minimal for any sufficiently high R-syzygy of a given R-module N. The precise statement is given in Section 8.

#### Higher matrix factorizations

It is well-known that when R is a complete intersection of codimension 1 in a regular local ring, the MCM R-modules are described by matrix factorizations:

**Theorem 1.1** ([Ei1], see also [EP, Theorem 2.1.1]). Let  $0 \neq f$  be a non-zerodivisor in a regular local ring S. Set R = S/(f). A finitely generated R-module N is MCM if and only if it is a matrix factorization module, that is, N is the cokernel of a map  $d: U_1 \to U_0$  of finitely generated free modules such that there exists a homotopy for  $f_1$  on the complex

$$0 \to U_1 \stackrel{d}{\to} U_0$$
.

This simply means that  $dh = f \cdot \operatorname{Id}_{U_0}$  and  $hd = f \cdot \operatorname{Id}_{U_1}$ .

## PDF page 4

The matrix factorization is called *minimal* if both d and h have entries in the maximal ideal of S. To include all MCM modules in the result, we must allow non-minimal matrix factorizations (though only for modules with R/(f) as a summand).

In [EP] we introduced higher matrix factorizations, and showed that any sufficiently high syzygy module over a complete intersection is the module of a minimal higher matrix factorization; note that high syzygy modules are MCM. Using the theory in Section 4, we can extend this to arbitrary MCM modules and (not-necessarily minimal) higher matrix factorizations: in Section 10 we prove Theorem 10.5 which is our extension of Theorem 1.1.

**Remark.** Though the case when S is regular is our primary interest, the constructions work more generally when S is a local Gorenstein ring; this is described in the rest of the paper. In some of the results one can also do without the local hypothesis; we leave this to the interested reader.

**Notation 1.2.** Throughout the paper we will use the following conventions. Let  $(\mathbf{W}, \partial^W)$  and  $(\mathbf{Y}, \partial^Y)$  be complexes. Our sign conventions are as follows: We write  $\mathbf{W}[-a]$  for the *shifted complex* with

$$\mathbf{W}[-a]_i = \mathbf{W}_{i+a}$$

and differential  $(-1)^a \partial^W$ , in particular the complex W[-1] has differential  $-\partial^W$ . The complex  $W \otimes Y$  has differential

$$\partial_q^{W \otimes Y} = \sum_{i+i=q} ((-1)^j \partial_i^W \otimes \operatorname{Id} + \operatorname{Id} \otimes \partial_j^Y).$$

If  $\varphi : \mathbf{W}[-1] \to \mathbf{Y}$  is a map of complexes, so that  $-\varphi \partial^W = \partial^Y \varphi$ , then the *mapping cone*  $\mathbf{Cone}(\varphi)$  is the complex  $\mathbf{Cone}(\varphi) = \mathbf{Y} \oplus \mathbf{W}$  with modules

$$Cone(\varphi)_i = Y_i \oplus W_i$$

and differential

$$\begin{array}{ccc} Y_i & W_i \\ Y_{i-1} & \left( \begin{array}{ccc} \partial_i^Y & \varphi_{i-1} \\ 0 & \partial_i^W \end{array} \right). \end{array}$$

As is well-known, a free resolution over a local ring is minimal if its differentials become 0 on tensoring with the residue class field k. We extend this definition and say that a map of (possibly non-free) modules is *minimal* if it becomes 0 on tensoring with k.

## 2. Review of MCM approximations

For the reader's convenience we review the basic ideas of MCM approximations from [AB] (see also [Di] and [EP, Section 7.3]). For simplicity, we deal only with finitely generated modules over a local Gorenstein ring S.

Let P be an MCM S-module without free summands. For  $q \ge 0$ , we denote by  $\operatorname{Syz}_a^S(P)$  the q-th syzygy module of P over S. Note that P has a unique cosyzygy module

## PDF page 5

$\operatorname{Syz}_{-1}^S(P)$ , which is also MCM, defined as the dual of the first syzygy of the dual of P. Since P is MCM over a local Gorenstein ring, the first syzygy module  $\operatorname{Syz}_1^S(P)$  cannot have free summands, as one sees by reducing to the 0-dimensional case, and it follows from the description above that the cosyzygy module  $\operatorname{Syz}_{-1}^S(P)$  cannot have free summands either. This can be applied repeatedly to obtain  $\operatorname{Syz}_{-q}^S(P)$  for any  $q \geq 1$ : there exists a unique MCM q-th cosyzygy module  $P := \operatorname{Syz}_{-q}^S(P)$  without free summands such that  $P = \operatorname{Syz}_{-q}^S(P)$  (see [EP, Lemma 7.1.3]).

The essential MCM approximation of a finitely generated S-module N is by definition an MCM module  $\operatorname{App}_S(N)$  without free summands together with a map  $\phi: \operatorname{App}_S(N) \to N$  determined as follows: choose an integer  $q > \operatorname{depth} S - \operatorname{depth} N$  and set

$$\operatorname{App}_{S}(N) := \operatorname{Syz}_{-q}^{S}(\operatorname{Syz}_{q}^{S}(N)),$$

considered together with a map  $\phi$ : App<sub>S</sub>(N)  $\rightarrow$  N induced by the comparison map of the S-free resolutions of App<sub>S</sub>(N) and N. By the uniqueness of cosyzygies, this is independent of the choice of q. In particular, if N is an MCM module, we let  $\phi$ : App<sub>S</sub>(N)  $\rightarrow$  N be the inclusion of the largest non-free summand of N. The following result is [EP, Theorem 7.3.3 and Corollary 7.3.4]; we recall the proof for the reader's convenience.

**Theorem 2.1.** Let  $S \twoheadrightarrow R$  be a surjection of local Gorenstein rings, and suppose that R has finite projective dimension as an S-module. Let N be a finitely generated R-module.

(1) For any  $i \geq 0$ ,

$$App_{S}(Syz_{i}^{R}(N)) = Syz_{i}^{S}(App_{S}(N)).$$

If N is an MCM module without free summands, then the statement is also true for i < 0.

(2) If j > depth S - depth N, then

$$App_{S}(Syz_{i}^{R}(N)) = Syz_{i}^{S}(N).$$

(3)  $\operatorname{App}_{S}(\operatorname{App}_{R}(N)) = \operatorname{App}_{S}(N)$ .

*Proof.* (1) It suffices to do the cases of first syzygies and cosyzygies. Let

$$0 \to N' \to F \to N \to 0$$

be a short exact sequence, with F free as an R-module. It suffices to show that  $\operatorname{Syz}_i^S(N') = \operatorname{Syz}_{i+1}^S(N)$  for some i.

We may obtain an *S*-free resolution of *N* as the mapping cone of the induced map from the *S*-free resolution of *N'* to the *S*-free resolution of *F*; if the projective dimension of *R* as an *S*-module (and thus of *F* as an *S*-module) is *u*, it follows that  $\operatorname{Syz}_{u+1}^S(N') = \operatorname{Syz}_u^S(N)$ .

Parts (2) and (3) follow easily from (1).

## PDF page 6

# 3. Codimension-one MCM approximations

The constructions of our layered resolutions use the codimension-one case of essential MCM approximations which we describe in this section.

**Assumptions 3.1.** In the rest of the paper, we use the following notation. Let

$$S \twoheadrightarrow R' \twoheadrightarrow R$$

be surjections of local Gorenstein rings and suppose that R = R'/(f), with f a non-zerodivisor in R'. We write k for the common residue field of R, R' and S. We consider a finitely generated MCM R-module M, and we may harmlessly assume that M has no free summand as an R-module.

## 3.2. Codimension one MCM approximations

We may construct the MCM approximation of M as an R'-module in the following way. Let  $M'_2$  be the second syzygy of M as an R'-module, and let M' be the minimal second cosyzygy of  $M'_2$  as an R'-module, which is well-defined, up to isomorphism and has no free summand because R' is local and Gorenstein. In the notation of Figure 1, G is the minimal R'-free resolution of M' and the module  $M'_2$  is the common kernel of  $F'_1 \to F'_0$  and  $G_1 \to G_0$ .

**Fig. 1.** Construction of M' from a minimal resolution of M over R'.

The module M', together with the induced map  $\phi: M' \to M$ , is the *essential MCM approximation*  $App_{R'}(M)$  of M over R'.

Let

$$\xi: B_0 \to \operatorname{Coker} \phi$$

be a surjection from a free R'-module of minimal rank to Coker  $\phi$ , and let

$$\gamma: B_0 \to M$$

be a lift of this map, so that

$$\alpha := (\phi, \gamma) : M' \oplus B_0 \rightarrow M$$

is a surjection. The *MCM approximation of M* over R' is defined to be the module  $M' \oplus B_0$  or, more properly, the map  $\alpha$ .

Let

$$\beta: B_1 \to M' \oplus B_0$$

## PDF page 7

be the kernel of  $\alpha$ . We write


$$\psi: B_1 \to M', \quad b: B_1 \to B_0$$

for the components of  $\beta$ . Thus we have the short exact sequence, which we call the *MCM*-approximation sequence over R',

$$0 \to B_1 \xrightarrow{\beta = \begin{pmatrix} \psi \\ b \end{pmatrix}} M' \oplus B_0 \xrightarrow{\alpha = (\phi, \gamma)} M \to 0. \tag{3.3}$$

# **Lemma 3.4.** $B_1$ is a free R'-module.

*Proof.* By the diagram in Figure 1,  $\operatorname{Tor}_{i}^{R'}(M',k) = \operatorname{Tor}_{i}^{R'}(M,k)$  for i > 1, so the long exact sequence in  $\operatorname{Tor}_{i}^{R'}(-,k)$  obtained from (3.3) shows that  $\operatorname{Tor}_{i}^{R'}(B_{1},k) = 0$  for i > 1 and it follows that  $B_{1}$  is an R' module of finite projective dimension.

Since the depth of M is 1 less than the depth of the MCM R'-module  $M' \oplus B_0$ , the short exact sequence (3.3) implies that  $B_1$  is an MCM R'-module. It follows from the Auslander–Buchsbaum formula that  $B_1$  is free.

We will use the following proposition to derive minimality criteria for the layered resolu-

**Proposition 3.5.** The map b is minimal. The map  $\psi$  is minimal if and only if the induced map

$$k \otimes \phi : k \otimes M' \to k \otimes M$$

is a monomorphism.

*Proof.* The short exact sequence (3.3) yields a right exact sequence

$$k \otimes B_1 \xrightarrow{\binom{k \otimes \psi}{k \otimes b}} k \otimes M' \oplus k \otimes B_0 \xrightarrow{(k \otimes \phi, k \otimes \gamma)} k \otimes M \to 0.$$

By construction,  $k \otimes M$  is the direct sum of the image of  $k \otimes \phi$  and  $k \otimes \gamma$ , and  $k \otimes \gamma$  is a monomorphism. Thus the kernel of  $(k \otimes \phi, k \otimes \gamma)$  is contained in  $k \otimes M'$ , and  $k \otimes b = 0$ . It follows that  $k \otimes \psi = 0$  if and only if  $k \otimes \phi$  is a monomorphism.

# 4. The layered S-free resolution of M

We let M be a Cohen–Macaulay S-module of codimension c, and we suppose that  $f_1, \ldots, f_c$  is a regular sequence in the annihilator of M. We will now construct the layered S-free resolution  $\mathbf{L} \uparrow^S (M, f_1, \ldots, f_c)$  of M. For simplicity we work in the case where M has finite projective dimension over S. See Remark 4.3 for the changes necessary in the general case. We do this by an induction on c. Set  $R = S/(f_1, \ldots, f_c)$ . We may harmlessly assume that M has no free summands as an R-module.

In the case c=0 the module M is 0 since we have assumed that M is an MCM R-module without free summands, and we take the resolution to be 0.

## PDF page 8

For simplicity, let  $R' = S/(f_1, ..., f_{c-1})$  and let  $f = f_c$ . We now describe the inductive step. Given an S-free resolution  $\mathbf{L}'$  of the essential MCM approximation M' of M over R', we construct an S-free resolution  $\mathbf{L} \uparrow^S(\mathbf{L}', f)$  of M. In the induction, we will take  $\mathbf{L}' = \mathbf{L} \uparrow^S(M', f_1, ..., f_{c-1})$  and

$$\mathbf{L} \uparrow^{S}(M, f_{1}, \dots, f_{c}) = \mathbf{L} \uparrow^{S}(\mathbf{L}', f).$$

With notation as in Section 3, we use the MCM approximation sequence (3.3):

$$0 \to B_1 \xrightarrow{\beta = \left(\frac{\psi}{b}\right)} M' \oplus B_0 \xrightarrow{\alpha = (\phi, \gamma)} M \to 0.$$

Denote by  $\mathbf{B}^S$  the 2-term complex

$$\mathbf{B}^S: B_1^S \xrightarrow{b^S} B_0^S,$$

where  $B_1^S$  and  $B_0^S$  are free S-modules such that  $B_1^S \otimes R' = B_1$  and  $B_0^S \otimes R' = B_0$ , and  $b^S$  is any lift to S of the map  $b: B_1 \to B_0$ .

Let K be the Koszul complex resolving R' over S. Let

$$\psi^{S}_{\bullet}: \mathbf{B}^{S}[-1] \to \mathbf{L}'$$

be the map of complexes whose component  $\psi_0^S: B_1^S \to L_0'$  is a lift of the map  $\psi: B_1 \to M'$ . Choose a map of complexes

$$\Psi^S: \mathbf{K} \otimes_S \mathbf{B}^S[-1] \to \mathbf{L}'$$

extending the map  $\psi_{\bullet}^S: \mathbf{B}^S[-1] \to \mathbf{L}'$ . We define  $\mathbf{L} \uparrow^S(\mathbf{L}', f)$  to be the mapping cone of  $\Psi$ .

**Theorem 4.1.** The complex  $\mathbf{L} \uparrow^S(\mathbf{L}', f)$  is an S-free resolution of M. It is minimal if and only if  $\mathbf{L}'$  is minimal and the induced map

$$\phi \otimes k : M' \otimes k \to M \otimes k$$

is a monomorphism.

*Proof.* Neither the homology nor the minimality of the mapping cone changes if we replace  $\Psi^S$  with a homotopic map of complexes, and any two liftings of  $\psi^S_{\bullet}$  are homotopic. Minimality: Because M' is an R'-module there is a map  $\mu: \mathbf{K} \otimes \mathbf{L}' \to \mathbf{L}'$  inducing

Minimality: Because M' is an R'-module there is a map  $\mu: \mathbf{K} \otimes \mathbf{L}' \to \mathbf{L}'$  inducing the multiplication map  $R' \otimes M' \to M'$ . By the remark above, we may take  $\Psi^S$  to be the composition

$$\mathbf{K} \otimes \mathbf{B}^{S}[-1] \xrightarrow{1 \otimes \psi_{\bullet}^{S}} \mathbf{K} \otimes \mathbf{L}' \xrightarrow{\mu} \mathbf{K} \otimes \mathbf{L}'.$$

Since  $\psi_{\bullet}^S$  is 0 on  $B_0^S$ , it follows that  $\Psi^S$  is zero on  $\mathbf{K} \otimes B_0^S$ . The mapping cone of  $\Psi^S$  is minimal if and only if  $1 \otimes \psi_{\bullet}^S$  is minimal. By Proposition 3.5, this is true if and only if  $\phi \otimes k$  is a monomorphism.

## PDF page 9

Exactness: Because  $\Psi^S$  vanishes on  $\mathbf{K} \otimes B_0^S$ , the mapping cone  $\mathbf{M}(\Psi^S)$  is isomorphic to the mapping cone of the map of free resolutions,

$$\Upsilon^{S} = \begin{pmatrix} \operatorname{Id} \otimes b^{S} \\ \Psi^{S} |_{\mathbf{K} \otimes (B_{1}^{S}[-1])} \end{pmatrix} : \mathbf{K} \otimes (B_{1}^{S}[-1]) \to (\mathbf{K} \otimes (B_{0}^{S}[-1])) \oplus \mathbf{L}',$$

which extends the maps  $b^S: B_1^S \to B_0^S$  and  $(\Psi^S)_0 = \psi_0^S: B_1^S \to L_0'$ . It follows from the long exact sequence of the mapping cone that  $\mathbf{M}(\Upsilon^S)$  is a minimal S-free resolution of M.

## 4.2. Layers of the S-resolution

For  $i = 0, \ldots, c$ , let  $R(i) = S/(f_1, \ldots, f_i)$  and set

$$M(i) := \operatorname{App}_{R(i)}(M).$$

By Theorem 2.1, for i > 0 we get

$$M(i-1) = \operatorname{App}_{R(i-1)}(M) = \operatorname{App}_{R(i-1)}(M(i)).$$

It is clear from the construction that the layered resolution  $\mathbf{L} \uparrow^S (M, f_1, \dots, f_c)$  is filtered by the sequence of subresolutions

$$\cdots \subset \mathbf{L} \uparrow^{S} (M(i-1), f_1, \dots, f_{i-1}) \subset \mathbf{L} \uparrow^{S} (M(i), f_1, \dots, f_i) \subset \cdots$$

We define the i-th layer to be the quotient

$$\frac{\mathbf{L}\uparrow^{\mathcal{S}}(M(i), f_1, \dots, f_i)}{\mathbf{L}\uparrow^{\mathcal{S}}(M(i-1), f_1, \dots, f_{i-1})} = \mathbf{K}(f_1, \dots, f_{i-1}) \otimes \mathbf{B}^{\mathcal{S}}(i),$$

where  $\mathbf{K}(f_1, \dots, f_{i-1})$  is the Koszul complex on  $f_1, \dots, f_{i-1}$  and  $\mathbf{B}^S(i)$  is the S-free complex lifting the 2-term complex

$$\mathbf{B}(i): B_1(i) \to B_0(i)$$

derived from the MCM approximation sequence for M(i) as an R(i-1)-module,

$$0 \rightarrow B_1(i) \rightarrow M(i-1) \oplus B_0(i) \rightarrow M(i) \rightarrow 0$$
.

**Remark 4.3.** When M does not have finite projective dimension over S the MCM approximation of M over S is not free, and the inductive construction must start with a given free resolution  $\mathbf{P}^S$  of the essential MCM approximation  $M^S$  of M over S. In this case we write  $\mathbf{L} \uparrow^S(\mathbf{P}^S, f_1, \ldots, f_c)$  for the layered resolution over S. By Theorem 2.1(3), the essential MCM approximation of M' over S is the same as that of M. Given this, we may simply replace  $\mathbf{L} \uparrow^S(M, f_1, \ldots, f_c)$  by  $\mathbf{L} \uparrow^S(\mathbf{P}^S, f_1, \ldots, f_c)$  and  $\mathbf{L} \uparrow^S(M', f_1, \ldots, f_{c-1})$  by  $\mathbf{L} \uparrow^S(\mathbf{P}^S, f_1, \ldots, f_c)$  in the proof above. Thus in the base case, c = 0, we take  $\mathbf{L} \uparrow^S(\mathbf{P}^S, f_1, \ldots, f_c)$  to be  $\mathbf{P}^S$  itself.

**Corollary 4.4.** If the ring S is regular and the layered resolution  $\mathbf{L} \uparrow^S (M, f_1, \dots, f_c)$  is minimal, then the Betti numbers of M satisfy  $\beta_i^S(M) \geq {c \choose i}$  for all  $i \geq 0$ .

## PDF page 10

#### 5. Review of CI operators and the Shamash construction

We will make use of the CI operators ( $\equiv$  Complete Intersection operators) introduced in [Ei1, Section 1] (see also [EP, Section 4.1]) and the Shamash construction [Sh] (see also Construction 4.3.1 in [EP]). For the reader's convenience we provide a summary.

### 5.1. CI operators

Suppose that  $f_1, \ldots, f_c \in S$  is a regular sequence and  $(\mathbf{V}, \partial)$  is a complex of free modules over  $R = S/(f_1, \ldots, f_c)$ . Suppose that  $\widetilde{\mathbf{V}}$  is a lifting of  $\mathbf{V}$  to S, that is, a sequence of free modules  $\widetilde{V}_i$  and maps  $\widetilde{\partial}_{i+1} : \widetilde{V}_{i+1} \to \widetilde{V}_i$  such that  $\partial = R \otimes \widetilde{\partial}$ . Since  $\partial^2 = 0$  we can choose maps  $\widetilde{t}_j : \widetilde{V}_{i+1} \to \widetilde{V}_{i-1}$ , where  $1 \leq j \leq c$ , such that  $\widetilde{\partial}^2 = \sum_{j=1}^c f_j \widetilde{t}_j$ . We set  $t_j := R \otimes \widetilde{t}_j$ .

By [Ei1], the  $t_j$  are maps of complexes  $V[-2] \rightarrow V$  that are functorial (and thus in particular commutative) up to homotopy.

If  $(V, \partial)$  is the minimal free resolution of a finitely generated R-module N then, writing k for the residue field of S, the CI operators  $t_j$  induce well-defined, commutative maps  $\chi_j$  on  $\operatorname{Ext}_R(N, k)$ , and thus make  $\operatorname{Ext}_R(N, k)$  into a module over the polynomial ring  $k[\chi_1, \ldots, \chi_c]$ , where the variables  $\chi_j$  have degree 2. The  $\chi_j$  are also called CI operators.

For a short proof of the following result, Theorem 5.2, see [EP, Theorem 4.2.3]. A version of it was first proved by Gulliksen [Gu], who used a different construction of operators on Ext. The relations between the CI operators and various constructions of operators on Ext were explained by Avramov and Sun.

**Theorem 5.2.** Let  $f_1, \ldots, f_c$  be a regular sequence in a local ring S with residue field k, and set  $R = S/(f_1, \ldots, f_c)$ . If N is a finitely generated R-module with finite projective dimension over S, then the action of the CI operators makes  $\operatorname{Ext}_R(N, k)$  into a finitely generated  $k[\chi_1, \ldots, \chi_c]$ -module.

#### 5.3. Higher homotopies and the Shamash construction

We need only the version for a single element, due to Shamash [Sh]; the more general case of a collection of elements is treated by Eisenbud [Ei1].

**Definition 5.4.** Let **G** be a complex of finitely generated free R'-modules. A system of higher homotopies  $\sigma$  for  $f \in R'$  on **G** is a collection of maps

$$\sigma_i: \mathbf{G} \to \mathbf{G}[-2j+1]$$

for  $j = 0, 1, \ldots$  of the underlying modules such that

- $\sigma_0$  is the differential on **G**,
- the map  $\sigma_0 \sigma_1 + \sigma_1 \sigma_0$  is multiplication by f on G,
- for every  $j \ge 2$  we have  $\sum_{q=0}^{j} \sigma_q \sigma_{j-q} = 0$ .

**Proposition 5.5** ([Ei2, Sh]). If G is a free resolution of an R'-module annihilated by elements f, then there exists a system of higher homotopies on G for f.

## PDF page 11

**Construction 5.6** ([Ei1, Sh]). Suppose that ( $\mathbf{G}$ ,  $\partial$ ) is a free complex over R' with a system  $\sigma = \{\sigma_j\}$  of higher homotopies for  $f \in R'$ . We will define a new complex over R := R'/(f). We write  $R\{y\}$  for the divided power algebra over R on one variable y; that is,

$$R\{y\} \cong \operatorname{Hom}_{\operatorname{graded} R\operatorname{-modules}}(R[t], R) = \bigoplus_{i} Ry^{(i)}$$

where the  $y^{(i)}$  form the dual basis to the basis  $t^i$  of the polynomial ring R[t]. The graded module  $R\{y\} \otimes \mathbf{G}$ , where y has degree 2, becomes a free complex over R when equipped with the differentials

$$\delta:=\sum t^j\otimes\sigma_j\otimes R.$$

This complex is called the *Shamash complex* of  $(\mathbf{G}, \sigma)$  and denoted  $\mathrm{Sh}(\mathbf{G}, \sigma)$  or simply  $\mathrm{Sh}(\mathbf{G})$ .

We now record the properties of the Shamash construction that we will use. The minimality was first proven by Avramov–Gasharov–Peeva [AGP, Proposition 6.2]. See also [EP, Corollary 4.3.5], where a different proof is given.

**Proposition 5.7.** Let G be an R'-free resolution of a finitely generated module N annihilated by a non-zerodivisor f. The Shamash complex Sh(G) is a free resolution of N over R = R'/(f), and is minimal if and only if the CI-operator  $\chi$  corresponding to f acts as a monomorphism on  $Ext_R(N,k)$ . This happens if and only if

$$\operatorname{Ext}_{R'}(N,k) \cong \frac{\operatorname{Ext}_{R}(N,k)}{\chi \operatorname{Ext}_{R}(N,k)}.$$

#### **6.** The layered R-free resolution of M

We let M be a Cohen–Macaulay S-module of codimension c, and we suppose that  $f_1, \ldots, f_c$  is a regular sequence in the annihilator of M. We do this by induction on c. We will now construct the layered R-free resolution  $\mathbf{L} \downarrow_R (M, f_1, \ldots, f_c)$  of M. For simplicity we work in the case where M has finite projective dimension over S. See Remark 6.3 for the changes necessary in the general case.

In the case c=0 the module M is 0 since we have assumed that M is an MCM R-module without free summands, and we take the resolution to be 0.

For simplicity, let  $R' = R/(f_1, \ldots, f_{c-1})$  and let  $f = f_c$ . We now describe the inductive step. Given an R'-free resolution  $\mathbf{L}'$  of the essential MCM approximation M' of M over R', we construct an R-free resolution  $\mathbf{L} \downarrow_R(\mathbf{L}', f)$  of M. In the induction, we will take  $\mathbf{L}' = \mathbf{L} \downarrow_{R'}(M', f_1, \ldots, f_{c-1})$ .

With notation as in Section 3, we use the MCM approximation sequence (3.3):

$$0 \to B_1 \xrightarrow{\beta = \left( \frac{\psi}{b} \right)} M' \oplus B_0 \xrightarrow{\alpha = (\phi, \gamma)} M \to 0.$$

We write

$$\mathbf{B}: B_1 \to B_0$$

## PDF page 12

for the R'-free 2-term complex with differential b. The map  $\psi: B_1 \to M'$  lifts to a map  $\psi_0: B_1 \to L'_0$ , which in turn defines a map of complexes

$$\psi_{\bullet}: \mathbf{B}[-1] \to \mathbf{L}'$$

Let  $\mathcal{C}(\psi_0, b)$  be the mapping cone of  $\psi_{\bullet}$ , as shown in Figure 2.

Fig. 2. The box complex.

We call  $C(\psi_0, b)$  the *box complex*. We define  $\mathbf{L} \downarrow_R (\mathbf{L}', f)$  to be the Shamash complex  $\mathrm{Sh}(C(\psi_0, b))$  defined in Construction 5.6.

**Theorem 6.1.** With notation as above, the box complex  $C(\psi_0, b)$  is an R'-free resolution of M. Thus the complex  $\mathbf{L} \downarrow_R(\mathbf{L}', f)$  is an R-free resolution of M.

Further  $C(\psi_0, b)$  is minimal if and only if L' is minimal and the induced map

$$k \otimes \phi : k \otimes M' \to k \otimes M$$

is a monomorphism. Thus  $\mathbf{L}\downarrow_R(\mathbf{L}',f)$  is minimal if, in addition, the CI operator induced by the expression  $R=R'/(f_c)$  is a monomorphism on  $\operatorname{Ext}_R(M,k)$ .

*Proof.* Using the notation in Figure 2,

$$\delta := \begin{pmatrix} \partial_1 & \psi_0 \\ 0 & b \end{pmatrix}$$

is the first differential of  $C(\psi_0, b)$ . We have

Coker 
$$\delta = \operatorname{Coker}\begin{pmatrix} \psi \\ b \end{pmatrix} = M$$
.

Also, for  $i \ge 2$  we have  $H_i(\mathcal{C}(\psi_0, b)) = H_i(\mathbf{L}') = 0$ , so it is enough to show that  $\mathcal{C}(\psi_0, b)$  is exact at  $L'_1 \oplus B_1$ .

Suppose that  $(x, y) \in \text{Ker } \delta$ . It follows that by = 0 and  $\psi_0 y \in \partial_1(L'_1)$ . Composing  $\delta$  with the surjection  $L'_0 \oplus B_0 \to M' \oplus B_0$  we see that the image z of y in  $M' \oplus B_0$  is zero. Since  $z = \begin{pmatrix} \psi \\ b \end{pmatrix} y$  and the map

$$\begin{pmatrix} \psi \\ b \end{pmatrix} : B_1 \to M' \oplus B_0$$

is a monomorphism by (3.3), it follows that y = 0. Hence  $\partial_1 x = 0$ . Since L' is acyclic,  $x \in \text{Im } \partial_2$ . Thus  $\mathcal{C}(\psi_0, b)$  is exact at  $L'_1 \oplus B_1$ .

The box complex  $C(\psi_0, b)$  is minimal if and only if  $\mathbf{L}'$  is minimal and the maps  $\psi_0$  and b are minimal. By Proposition 3.5,  $\psi_0$  and b are minimal if and only if  $k \otimes \phi$  is a monomorphism.

## PDF page 13

Since  $C(\psi_0, b)$  is an R'-free resolution of M the complex  $Sh(C(\psi_0, b))$  is an R-free resolution of M. By [AGP, Proposition 6.2] (see [EP, Corollary 4.3.5] for a second proof), the minimal R-free resolution of M is obtained by applying the Shamash construction to the minimal R'-free resolution of M if and only if the CI operator  $\chi : Ext_R(M, k) \to Ext_R(M, k)$ [2] is injective.

# 6.2. Layers of the R-resolution

We use the same notation as in Subsection 4.2. It is clear from the construction that the layered resolution  $\mathbf{L}\downarrow_R(M, f_1, \dots, f_c)$  is filtered by the sequence of subcomplexes

$$\cdots \subset R \otimes \mathbf{L} \downarrow_{R(i-1)} (M(i-1), f_1, \dots, f_{i-1}) \subset R \otimes \mathbf{L} \downarrow_{R(i)} (M(i), f_1, \dots, f_i) \subset \cdots$$

which are themselves resolutions because  $f_{i+1}, \ldots, f_c$  is a regular sequence on M(i) for each i.

We define the i-th layer to be the quotient

$$\frac{R \otimes \mathbf{L} \downarrow_{R(i)}(M(i), f_1, \dots, f_i)}{R \otimes \mathbf{L} \downarrow_{R(i-1)}(M(i-1), f_1, \dots, f_{i-1})}.$$

To describe this quotient we begin with the complexes

$$\mathbf{L}' := \mathbf{L} \downarrow_{R(i-1)} (M(i-1), f_1, \dots, f_{i-1}),$$

and

$$\mathbf{B}(i): B_1(i) \to B_0(i),$$

corresponding to the essential MCM approximation M(i-1) of M over R(i-1). With notation as in Figure 2, the homotopy for  $f_i$  on the box complex  $C(\psi_0, b)$  induces a map h from  $L'_0$  to  $B_1$ , and from this we get the complex

$$\mathbf{L}'': \cdots \to R \otimes L'_1 \to R \otimes L'_0 \xrightarrow{h} R \otimes B_1(i) \xrightarrow{b} R \otimes B_0(i).$$

From the inductive construction we see that the *i*-th layer of  $\mathbf{L}\downarrow_R(M, f_1, \dots, f_c)$  is

$$R\{y\} \otimes_R \mathbf{L}''$$
.

**Remark 6.3.** The situation is an analogue to that in Remark 4.3. When M does not have finite projective dimension over S the essential MCM approximation of M over S is not 0, and the inductive construction must start with a given free resolution  $\mathbf{P}^S$  of the essential MCM approximation  $M^S$  of M over S. In this case we write  $\mathbf{L}\downarrow_R(\mathbf{P}^S, f_1, \ldots, f_c)$  for the layered resolution over R. We note that the essential MCM approximation of M' over S is the same as that of M by Theorem 2.1(3). Given this, we may simply replace  $\mathbf{L}\downarrow_R(M, f_1, \ldots, f_c)$  by  $\mathbf{L}\downarrow_R(\mathbf{P}^S, f_1, \ldots, f_c)$  and  $\mathbf{L}\downarrow_{R'}(M', f_1, \ldots, f_{c-1})$  by  $\mathbf{L}\downarrow_{R'}(\mathbf{P}^S, f_1, \ldots, f_c)$  in the proof above. Thus in the base case, c = 0, we take the layered resolution to be  $\mathbf{P}^S$  itself.

## PDF page 14

#### 7. When is $k \otimes \phi$ a monomorphism?

**Theorem 7.1.** Let P be an MCM R-module, and let  $M = \operatorname{Syz}_2^R(P)$ . Let  $\chi$  be the CI operator on  $\operatorname{Ext}_R(P,k)$  derived from the expression R = R'/(f). If the CI operator

$$\chi: \operatorname{Ext}^j_R(P,k) \to \operatorname{Ext}^{j+2}_R(P,k)$$

is injective for j=0,1, then the essential MCM approximation  $\phi:M'\to M$  of M over R' induces a monomorphism

$$k \otimes \phi : k \otimes M' \hookrightarrow k \otimes M.$$

*Proof.* Figure 3 exhibits the modules and maps that will be used. Let **F** be a minimal R-free resolution of P, so that M is the image of  $\partial_2 : F_2 \to F_1$ . Let **F**' be a lifting of **F** to R', and let  $t : \mathbf{F} \to \mathbf{F}[-2]$  denote the CI operator derived from the expression R = R'/(f).

We may define maps  $t': F'_{j+2} \to F'_j$  for  $j \le 1$  by the formula  $\partial'^2 = ft'$ . From the assumption that  $\chi: \operatorname{Ext}_R^j(P,k) \to \operatorname{Ext}_R^{j+2}(P,k)$  is a monomorphism, we see using Nakayama's Lemma that the maps  $t: F_{j+2} \to F_j$  and  $t': F'_{j+2} \to F'_j$  are surjections for  $j \le 1$ .

Fig. 3

For j = 0, 1 we set  $G_j = F'_j$ , and we define

$$G_2 = \operatorname{Ker}(F_2' \xrightarrow{t'} F_0')$$

which is free because t' is surjective. Let  $\delta: G_2 \to G_1$  be the map induced by  $\partial': F_2' \to F_1'$ . It follows at once that

**G**: 
$$G_2 \xrightarrow{\delta} G_1 \xrightarrow{\partial'} G_0$$

is a minimal R'-free complex. Let M' be the image of  $\delta: G_2 \to G_1$ , and write  $\phi: M' \to M$  for the induced map. We will show that M' is the essential MCM approximation of M over R'.

## PDF page 15

First we prove that **G** is the beginning of an R'-free resolution of P. Since  $\partial'^2 = ft'$ :  $F_2' \to F_0'$ , we see that the cokernel of  $\partial' : F_1' \to F_0'$  is annihilated by f. After tensoring with R, the cokernel is P. Thus the cokernel of  $\partial' : F_1' \to F_0'$  itself is P.

Next we prove the exactness of **G** at  $G_1$ . Suppose  $\ell_1 \in G_1 = F_1'$  goes to 0 in  $G_0 = F_0'$ . It follows from the exactness of **F** at  $F_1$  that there is an element  $\ell_2 \in F_2'$  such that  $\ell_1 - \partial' \ell_2 = f m_1'$  for some  $m_1' \in F_1'$ . The surjectivity of  $t' : F_3' \to F_1'$  shows that we may write  $f m_1' = \partial'^2 m_3'$  for some  $m_3' \in F_3'$ . Thus  $\ell_1 = \partial' (\ell_2 + \partial' m_3')$ . Since  $\partial'^2 (\ell_2 + \partial' m_3') = \partial' \ell_1 = 0$  by hypothesis, we see that  $\ell_2 + \partial' m_3' \in G_2$ , proving the exactness at  $G_1$ . This shows that  $G_2 \to G_1 \to G_0$  is the beginning of the minimal R'-free resolution of P.

It follows that  $M' = \operatorname{Syz}_2^{R'} P$ . Because  $\operatorname{depth}_{R'} P = \operatorname{depth} R' - 1$  and  $M = \operatorname{Syz}_2^R P$ , it follows from the construction in Subsection 3.2 and Theorem 2.1(3) that  $\phi : M' \to M$  is the essential MCM approximation of M over R'. Since  $G_2$  is a direct summand of  $F_2'$ , we see that the induced map  $k \otimes \phi : k \otimes M' \to k \otimes M$  is injective.

## 8. High syzygies and the criterion for minimality

Throughout this section, N denotes a finitely generated Cohen–Macaulay S-module of codimension c that has finite projective dimension as an S-module. We suppose that  $\mathbf{f} = f_1, \ldots, f_c$  is a regular sequence in the annihilator of N and write  $R = S/(f_1, \ldots, f_c)$  as usual. For  $i = 0, \ldots, c$  we set

$$R(i) := S/(f_1, \ldots, f_i);$$

in particular, R = R(c). Let  $\mathcal{R}(i) = k[\chi_1, ..., \chi_i]$  be the ring of CI operators corresponding to  $f_1, ..., f_i$ .

To prove the minimality of the layered resolutions, we will need the  $\chi_i$  to form a quasi-regular sequence on  $\operatorname{Ext}_R(N,k)$ . This can always be achieved when k is infinite. We review the relevant ideas: A sequence of elements  $h_c, \ldots, h_1$  in a ring T is said to be *quasi-regular* on a T-module E if, for each i, the annihilator of  $h_i$  in the module  $E/(h_c, \ldots, h_{i+1})E$  has finite length. The case of interest for us is that of the finitely generated graded module  $\operatorname{Ext}_R(N,k)$  over the polynomial ring  $\mathcal{R}(c)$ . In addition to the hypotheses of Section 3, we now suppose that S contains an infinite field k. Then, any sufficiently general choice of the variables  $\chi_i$  forms a quasi-regular sequence on  $\operatorname{Ext}_R(N,k)$ . More precisely, for  $g \in GL_c(k)$ , let

$$\mathbf{f}^g := (f_1, \dots, f_c)g$$

be the sequence of k-linear combinations of the  $f_i$  corresponding to g. Since the  $\chi_i$  form a dual basis to the  $f_i$ , there is an open subset  $U \subset GL_c(k)$  such that for  $g \in U$  the sequence of CI operators  $(\chi_c)_g, \ldots, (\chi_1)_g$  corresponding to  $\mathbf{f}^g$  is a quasi-regular sequence on  $\operatorname{Ext}_R(N, k)$ ; see for example [EP, Lemma 6.1.9].

For the minimality criteria we will make use of the Castelnuovo–Mumford regularity of  $\operatorname{Ext}_R(N, k)$  as an  $\mathbb{R}$ -module, defined in the usual way in terms of the top degrees of non-vanishing components of the local cohomology with respect to  $(\chi_1, \ldots, \chi_c) \subset \mathbb{R}$ .

## PDF page 16

As  $\mathcal{R}$ -modules we have

$$\operatorname{Ext}_{R}(N, k) = \operatorname{Ext}_{R}^{\operatorname{even}}(N, k) \oplus \operatorname{Ext}_{R}^{\operatorname{odd}}(N, k),$$

so the regularity is the maximum of the regularities of these two submodules (where  $\operatorname{Ext}_R^{\operatorname{odd}}(N,k)$  inherits its grading from  $\operatorname{Ext}_R(N,k)$ ). In particular, if N is not R-free then reg  $\operatorname{Ext}_R(N,k) \geq 1$  since  $\operatorname{Ext}_R(N,k)$  is not generated in degree 0.

For example, if c = 0 then R = S and  $\mathcal{R} = k$ . In this case,

$$\operatorname{reg}_{\mathcal{R}} \operatorname{Ext}_{S}(N, k) = \operatorname{reg}_{k} \operatorname{Ext}_{S}(N, k) = \max\{i \mid \operatorname{Ext}_{S}^{i}(N, k) \neq 0\} = c,$$

since we have assumed that N is Cohen–Macaulay of codimension c. In general, the invariant we will use is

$$r(\mathbf{f}, N) := \max_{2 \le i \le c} \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k).$$

**Theorem 8.1.** Let N be a finitely generated Cohen–Macaulay S-module of codimension c that has finite projective dimension as an S-module, and let  $\mathbf{f} = f_1, \ldots, f_c$  be a regular sequence in the annihilator of N. Suppose that the sequence of CI operators  $\chi_c, \chi_{c-1}, \ldots, \chi_1$  on  $\operatorname{Ext}_R(N, k)$  corresponding to  $\mathbf{f}$  is quasi-regular. If

$$n \ge 3 + \max\{c - 2, r(\mathbf{f}, N)\},\$$

and M is the n-th syzygy of N over R, then the layered resolutions of M with respect to  $\mathbf{f}$ , both over S and over R, are minimal.

*Proof.* First, by a descending induction on i we will prove that  $\chi_i, \ldots, \chi_1$  is a quasi-regular sequence on  $\operatorname{Ext}_{R(i)}(N,k)$ . For i=c this is part of our hypothesis. We may assume, by induction, that  $\chi_{i+1}, \ldots, \chi_1$  is a quasi-regular sequence on  $\operatorname{Ext}_{R(i+1)}(N,k)$ . Choose a q such that  $\chi_{i+1}$  is a non-zerodivisor on  $\operatorname{Ext}_{R(i+1)}^{\geq q}(N,k)$ . Let U be the q-th syzygy of N over R(i+1). By Proposition 5.7, we get

$$\operatorname{Ext}_{R(i)}(U,k) \cong \operatorname{Ext}_{R(i+1)}(U,k)/\chi_{i+1}\operatorname{Ext}_{R(i+1)}(U,k).$$

By Theorem 2.1,  $\operatorname{Ext}_{R(i)}^{\geq m}(U,k)[-q] = \operatorname{Ext}_{R(i)}^{\geq m}(N,k)$  for  $m \gg 0$ . Thus the  $\mathcal{R}(i)$ -modules  $\operatorname{Ext}_{R(i)}(N,k)$  and  $\operatorname{Ext}_{R(i+1)}(N,k)/\chi_{i+1}\operatorname{Ext}_{R(i+1)}(N,k)$  become isomorphic after a sufficiently high truncation, completing the induction.

As the modules N and  $\operatorname{App}_{R(i)}(N)$  have a common syzygy over R(i), we see that the modules  $\operatorname{Ext}_{R(i)}(N,k)$  and  $\operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N),k)$  become isomorphic after a sufficiently high truncation. Therefore,  $\chi_i, \ldots, \chi_1$  is a quasi-regular sequence on  $\operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N),k)$  as well.

Since n > 1, the module M is an MCM module over R with no free summands. As in 4.2, for i = 0, ..., c we set

$$M(i) = \operatorname{App}_{R(i)}(M).$$

For i > 0 we have  $M(i - 1) = \operatorname{App}_{R(i-1)}(M(i))$  by Theorem 2.1, and we write

$$\phi_i : \operatorname{App}_{R(i-1)}(M(i)) \to M(i)$$

for the essential MCM approximation map. We will show that  $k \otimes \phi_i$  is a monomorphism.

## PDF page 17

Suppose i = 1. Since both N and R have finite projective dimension over S, it follows that M has finite projective dimension as well. Therefore, M(0) = 0, so  $\phi_1 = 0$ .

Next, for i > 2, we will show that the inequality

$$n \ge 3 + \max\{c - 2, \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k)\}$$

implies that  $k \otimes \phi_i$  is a monomorphism.

Let *P* be the minimal (n-2)-th syzygy of *N* over R(i). Since  $n-2 \ge 1+c-i$ , the module *P* is an MCM module over R(i) without free summands. Note that  $\operatorname{Syz}_2^{R(i)}(P) = \operatorname{Syz}_n^{R(i)}(N)$ . By Theorem 2.1(2) this is the module M(i).

We have shown, above, that the element  $\chi_i$  is quasi-regular on the module  $\operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k)$ . Since

$$n-2 \ge 1 + \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k),$$

the largest submodule of  $\operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k)$  of finite length does not meet

$$\operatorname{Ext}_{R(i)}^{\geq n-2}(\operatorname{App}_{R(i)}(N), k) = \operatorname{Ext}_{R(i)}(P, k)[-n+2],$$

and thus  $\chi_i$  is a non-zerodivisor on  $\operatorname{Ext}_{R(i)}(P,k)$ . From Theorem 7.1 we conclude that the map

$$k \otimes \phi_i : k \otimes M(i-1) \to k \otimes M(i)$$

is a monomorphism.

We now prove the minimality of the layered resolutions of M(i) over S and over R(i) by induction on i. The case i=0 is obvious. By Theorems 4.1 and 6.1, the minimality for M(i) follows from the fact that  $k \otimes \phi_i$  is a monomorphism and the minimality of the layered resolutions of M(i-1).

**Remark 8.2.** There is a version of Theorem 8.1 that does not depend on information about the approximations  $\operatorname{App}_{R(i)}(N)$  at the expense of a slight weakening of the bound, by using

$$r'(\mathbf{f}, N) = \max_{2 \le i \le c} \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(N, k).$$

**Proposition 8.3.** We use the notation in 3.1. Let M be a finitely generated MCM R-module of codimension c that has finite projective dimension over S. Let  $\mathbf{f} = f_1, \ldots, f_c$  be a regular sequence in the annihilator of M, and  $R' = S/(f_1, \ldots, f_{c-1})$ ,  $R = R'/(f_c)$ . Denote by  $\mathcal{R}' = k[\chi_1, \ldots, \chi_{c-1}]$  the ring of CI operators corresponding to  $f_1, \ldots, f_{c-1}$ . We have

$$\operatorname{reg}_{\mathcal{R}'} \operatorname{Ext}_{R'}(\operatorname{App}_{R'}(M), k) \leq \operatorname{reg}_{\mathcal{R}'} \operatorname{Ext}_{R'}(M, k).$$

*Proof.* From the exact sequence (3.3) we get the exact sequence

$$\operatorname{Hom}_{R'}(B_1, k) \to \operatorname{Ext}_{R'}(M, k) \to \operatorname{Ext}_{R'}(\operatorname{App}_{R'}(M), k) \to 0.$$

By [Ei1], it follows that it is an exact sequence of  $\mathcal{R}'$ -modules. Thus the 0-th local cohomology of  $\operatorname{Ext}_{R'}(\operatorname{App}_{R'}(M), k)$  as an  $\mathcal{R}'$ -module is a homomorphic image of the 0-th local cohomology of  $\operatorname{Ext}_{R'}(M, k)$  as an  $\mathcal{R}'$ -module, and the higher local cohomology modules coincide, proving the desired regularity inequality.

## PDF page 18

In order to make use of the sharper estimate involving the  $r(\mathbf{f}, N)$  and thus depending on  $\operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k)$ , we would like to understand the relationship between  $\operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k)$  and  $\operatorname{reg}_{\mathcal{R}(j)} \operatorname{Ext}_{R(j)}(\operatorname{App}_{R(j)}(N), k)$ . In the examples we have tried using the Macaulay 2 package "MCMApproximations", the following question has a positive answer:

**Question 8.4.** With hypotheses as in Theorem 8.1, is it true that

$$\cdots \le \operatorname{reg}_{\mathcal{R}(i-1)} \operatorname{Ext}_{R(i-1)}(\operatorname{App}_{R(i-1)}(N), k) \le \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N), k) \le \cdots$$
  
so that the maximum is attained by  $\operatorname{reg}_{\mathcal{R}(c)} \operatorname{Ext}_{R(c)}(N, k)$ ?

Since  $\operatorname{App}_{R(0)}(N) = 0$  and  $\operatorname{App}_{R(1)}(N)$  is by definition an MCM R(1)-module without free summands, we have at least

$$0 = \operatorname{reg}_{\mathcal{R}(0)} \operatorname{Ext}_{R(0)}(\operatorname{App}_{R(0)}(N), k) \le \operatorname{reg}_{\mathcal{R}(1)} \operatorname{Ext}_{R(1)}(\operatorname{App}_{R(1)}(N), k) \le 1,$$

where the latter inequality follows from [EP, Theorem 2.1.1].

The answer to Question 8.4 is also positive for high syzygies:

**Corollary 8.5.** As in 4.2 and the proof of Theorem 8.1, for i = 0, ..., c we set  $M(i) = \operatorname{App}_{R(i)}(M)$ . With hypotheses as in Theorem 8.1, if  $M(i) \neq 0$  then

$$reg_{\mathcal{R}(i)} Ext_{R(i)}(M(i), k) = 1$$

*for every*  $i \geq 1$ .

*Proof.* We will prove the corollary by a descending induction on i. First, we discuss the base of the induction i = c. By assumption, M(c) = M is the n-th syzygy of an MCM-module N over R(c) = R and

$$n \geq 3 + \operatorname{reg}_{\mathcal{R}(c)} \operatorname{Ext}_{R(c)}(\operatorname{App}_{R(c)}(N), k).$$

It follows that

$$\operatorname{Ext}_{R(c)}(M(c), k) = \operatorname{Ext}_{R(c)}^{\geq n}(\operatorname{App}_{R(c)}(N), k)[n]$$

has the desired regularity, since if  $M(c) \neq 0$  then  $\operatorname{Ext}_{R(c)}(M(c), k)$  is generated in degrees 0 and 1.

Now, fix an i < c. Suppose  $M(i) \neq 0$ . The proof of Theorem 8.1 shows that  $\chi_i$  is regular on  $\operatorname{Ext}_{R(i)}(M(i), k)$  since  $M(i) = \operatorname{Syz}_2^{R(i)}(P)$  (where P is the module introduced in the proof of Theorem 8.1). By Proposition 5.7 it follows that

$$\operatorname{Ext}_{R(i-1)}(M(i),k) \cong \frac{\operatorname{Ext}_{R(i)}(M(i),k)}{\chi_i \operatorname{Ext}_{R(i)}(M(i),k)}.$$

Therefore,

$$\operatorname{reg}_{\mathcal{R}(i-1)} \operatorname{Ext}_{R(i-1)}(M(i), k) = \operatorname{reg}_{\mathcal{R}(i)} \operatorname{Ext}_{R(i)}(M(i), k) = 1$$

by induction hypothesis. By Proposition 8.3 we have

$$\operatorname{reg}_{\mathcal{R}(i-1)} \operatorname{Ext}_{R(i-1)}(M(i-1), k) \leq \operatorname{reg}_{\mathcal{R}(i-1)} \operatorname{Ext}_{R(i-1)}(M(i), k) = 1.$$

The regularity on the left-hand side vanishes if and only if M(i-1) = 0.

In general, we can establish a weaker inequality than the one in Question 8.4:

## PDF page 19

**Proposition 8.6.** With hypotheses as in Theorem 8.1,

$$\operatorname{reg}_{\mathcal{R}(i-1)}\operatorname{Ext}_{R(i-1)}(\operatorname{App}_{R(i-1)}(N),k) \leq 2 + \operatorname{reg}_{\mathcal{R}(i)}\operatorname{Ext}_{R(i)}(\operatorname{App}_{R(i)}(N),k).$$

*Proof.* We may assume i = c, which simplifies the notation: we write R' for R(i-1) and N' for N(i-1). Set  $r = \text{reg}_{\mathcal{R}} \text{ Ext}_R(N, k)$ , and let T be the (r+1)-st R-syzygy of N. The operator  $\chi_C$  is a non-zerodivisor on  $\text{Ext}_R(T, k)$  so, by Proposition 5.7,

$$\operatorname{Ext}_{R'}(T,k) \cong \frac{\operatorname{Ext}_{R}(T,k)}{\chi_{c}\operatorname{Ext}_{R}(T,k)}.$$

The module

$$\operatorname{Ext}_R(T,k) = \operatorname{Ext}_R^{\geq r+1}(N,k)[r+1]$$

has regularity 1 over  $\mathcal{R}$ , hence  $\operatorname{reg}_{\mathcal{R}'}\operatorname{Ext}_{R'}(T,k)=1$ .

Since T is an MCM module over R, we may apply Proposition 8.3 to get

$$\operatorname{reg}_{\mathcal{R}'} \operatorname{Ext}_{R'}(\operatorname{App}_{R'}(T), k) \leq \operatorname{reg}_{\mathcal{R}'} \operatorname{Ext}_{R'}(T, k) = 1.$$

By Theorem 2.1,  $\operatorname{App}_{R'}(T) \cong \operatorname{Syz}_{r+1}^{R'}(N')$  and so

$$\operatorname{Ext}_{R'}(\operatorname{App}_{R'}(T), k)[-r-1] = \operatorname{Ext}_{R'}^{\geq r+1}(N', k).$$

We conclude reg  $\operatorname{Ext}_{R'}^{\geq r+1}(N',k) \leq r+2$ . From the exact sequence

$$0 \to \operatorname{Ext}_{R'}^{\geq r+1}(N',k) \to \operatorname{Ext}_{R'}(N',k) \to \operatorname{Ext}_{R'}^{\leq r}(N',k) \to 0$$

we see that  $\operatorname{Ext}_{R'}(N', k)$  has regularity at most r + 2, as required.

#### 9. Generalized matrix factorization of an element

As explained in the introduction, an alternative presentation of the layered resolution over *R* could be deduced from the following generalization of a result on periodic resolutions over hypersurfaces in [Ei1].

**Theorem 9.1.** Let  $f \in A$  be an element of a commutative ring, and let

$$0 \to N_1 \xrightarrow{d} N_0 \xrightarrow{\zeta} P \to 0$$

be a short exact sequence of A-modules. If f is a non-zerodivisor on  $N_0$  and on  $N_1$  but fP=0, then there is a unique map  $h:N_0\to N_1$  such that  $dh=f*\mathrm{Id}$ . The map h is a monomorphism and satisfies  $hd=f*\mathrm{Id}$ . Further, if we write  $\overline{-}$  for  $A/(f)\otimes -$ , then the complex

$$\cdots \to \overline{N}_1 \xrightarrow{\overline{d}} \overline{N}_0 \xrightarrow{\overline{h}} \overline{N}_1 \xrightarrow{\overline{d}} \overline{N}_0 \xrightarrow{\overline{\zeta}} P \to 0$$

is exact.

*Proof.* From the left exactness of the functor Hom we see that

$$0 \to \operatorname{Hom}(N_0, N_1) \to \operatorname{Hom}(N_0, N_0) \to \operatorname{Hom}(N_0, P)$$

is exact. Since  $f * Id \in Hom(N_0, N_0)$  goes to 0 in  $Hom(N_0, P)$ , it comes from a unique map  $h \in Hom(N_0, N_1)$  with the property that dh = f \* Id.

## PDF page 20

We claim that hd = f \* Id as well. Since f is a non-zerodivisor on  $N_1$  it suffices to prove this after inverting f. However, if f is a unit then the equation dh = f \* Id shows that d is surjective. Since d is a monomorphism, it follows that d, and therefore also h, become isomorphisms on inverting f, so h can be cancelled on the right from the expression

$$hdh = h(f * Id) = (f * Id)h,$$

yielding hd = f \* Id as required.

The right exactness of  $A/(f) \otimes -$  shows that

$$\overline{N}_1 \xrightarrow{\overline{d}} \overline{N}_0 \xrightarrow{\overline{\zeta}} P \to 0$$

is exact.

To show that the infinite sequence is exact at  $\overline{N}_1$ , suppose that  $\overline{da}=0$  for some  $a\in N_1$ . Then da=fe for some  $e\in N_0$ , and so da=fe=dhe, which implies a=he. A similar argument proves exactness at  $\overline{N}_0$ .

Theorem 9.1 applies to the setting of MCM approximations, and yields:

**Corollary 9.2.** Suppose that R' is a Gorenstein ring,  $f \in R'$  a non-zerodivisor, and M an MCM module over R := R'/(f). Let (3.3) be the corresponding MCM-approximation sequence over R'. There is a unique map

$$h: M' \oplus B_0 \rightarrow B_1$$

such that  $\beta h = f * Id$ . The map h is a monomorphism and satisfies  $h\beta = f * Id$ . Further, the complex

$$\rightarrow B_1 \otimes R \xrightarrow{\beta \otimes R} (M \oplus B_0) \otimes R \xrightarrow{h \otimes R} B_1 \otimes R \xrightarrow{\beta \otimes R} (M' \oplus B_0) \otimes R \xrightarrow{\phi} M \rightarrow 0$$
of R-modules is exact.

# 10. Maximal Cohen-Macaulay modules from matrix factorization

In this section we provide a description of all MCM modules over a complete intersection. In keeping with the inductive nature of layered resolutions, we give an inductive definition of a CI matrix factorization essentially equivalent to the corresponding definitions in [EP]; see Remark 10.4.

We write  $\mathbf{K}(c-1)$  for the Koszul complex  $\mathbf{K}(f_1, \ldots, f_{c-1})$  over S on  $f_1, \ldots, f_{c-1}$ . Let  $\partial$  be its differential, and let  $\{e_i\}$  be a basis of  $\mathbf{K}(c-1)_1$  such that  $\partial(e_i) = f_i \in \mathbf{K}(c-1)_0 = S$ .

**Definition 10.1.** By an *initial homotopy h* for  $f \in S$  on a 3-term complex

$$U_2 \stackrel{d}{\rightarrow} U_1 \stackrel{d}{\rightarrow} U_0$$

we mean a map of degree 1 with components  $h: U_i \to U_{i+1}$  such that

$$dh: U_0 \rightarrow U_0, \quad dh + hd: U_1 \rightarrow U_1$$

are both multiplication by f.

## PDF page 21

**Definition 10.2.** Let S be a local ring. A CI matrix factorization complex with initial homotopies with respect to a regular sequence  $f_1, \ldots, f_c$  in S is defined as a 3-term complex of free finitely generated S-modules

$$\mathbf{U}(c): \quad U_2 \stackrel{d}{\to} U_1 \stackrel{d}{\to} U_0$$

with *initial homotopies*  $h_i$  for  $f_i$  on  $\mathbf{U}(c)$ , such that:

If c = 1 then U(1) has the form

$$\mathbf{U}(1): \quad 0 \to B_1(1) \xrightarrow{b_1} B_0(1)$$

with a homotopy  $h_1$  for multiplication by  $f_1$ . (This structure is the same as that of a matrix factorization introduced in [Ei1].)

If c > 1 then

(1)  $\mathbf{U}(c)$  has a subcomplex

$$\mathbf{U}(c-1): \quad U_2' \to U_1' \to U_0'$$

with initial homotopies  $h'_1, \ldots, h'_{c-1}$  that is a CI matrix factorization complex with respect to  $f_1, \ldots, f_{c-1}$ . Furthermore,  $\mathbf{U}(c)$  has a quotient complex  $\mathbf{U}(c)/\mathbf{U}(c-1)$  of the form

**KB**: 
$$\left(\mathbf{K}(f_1,\ldots,f_{c-1})\otimes_S\left(0\to B_1(c)\stackrel{b_c}{\longrightarrow}B_0(c)\right)\right)_{\leq 2}$$

for some complex of finitely generated free S-modules

$$0 \to B_1(c) \xrightarrow{b_c} B_0(c)$$
.

(2) With this decomposition,  $\mathbf{U}(c)$  is isomorphic to the mapping cone of a map of complexes

$$\Psi_c: \mathbf{KB}[-1] \to \mathbf{U}(c-1)$$

that vanishes on  $\mathbf{K}(c-1) \otimes B_0(c)$ , while  $\Psi_c$  restricted to the summand  $e_i \otimes B_1(c)$  is equal to  $-h_i' \psi_c$ , where  $\psi_c$  is the component of  $\Psi_c$  from  $B_1(c)$  to  $U_0' = \bigoplus_{i=1}^{c-1} B_0(c)$  (see the diagram below).

- (3) For p < c, the initial homotopy  $h_p$  is equal to  $h'_p$  when restricted to  $\mathbf{U}(c-1)$  and is equal to  $(-1)^{s+1}e_p \otimes \mathrm{Id}$  when restricted to  $\mathbf{K}(c-1) \otimes B_s(c)$ .
- (4) There exists an initial homotopy  $h_c$  for  $f_c$  on  $\mathbf{U}(c)$ .

We define the CI matrix factorization module M of  $\mathbf{U}(c)$  to be

$$M = \operatorname{Coker}(U_1 \xrightarrow{d} U_0).$$

The resulting CI matrix factorization with respect to  $f_1, \ldots, f_c$  is the pair (d, h), where d is the component of the differential in U(c) mapping

$$\bigoplus_{p=1}^{c} B_1(p) \to U_0 = \bigoplus_{p=1}^{c} B_0(p)$$

(thus, d is the collection of maps  $b_i$  and  $\psi_i$ ), and h is the collection of the components of the initial homotopies  $h_i$  mapping  $\bigoplus_{p=1}^i B_0(p) \to \bigoplus_{p=1}^i B_1(p)$ .

## PDF page 22

The following diagram may help to visualize the definition. We denote by  $\partial$  the differential in the Koszul complex, and  $U_r(c)$  is the direct sum of the modules in the r-th column:

**Remark 10.3.** The construction above is consistent with the construction preceding Theorem 4.1. The complex U(c) is the beginning of the layered resolution described in Theorem 4.1.

**Remark 10.4.** Our concepts of matrix factorizations here and in [EP] are equivalent in the sense that the following three properties are equivalent:

- (1) M is the module of a CI matrix factorization.
- (2) M is the module of a higher matrix factorization (introduced in [EP, Definition 1.2.2]).
- (3) M is the module of a strong matrix factorization (introduced in [EP, Definition 1.2.3]).

It is immediate that (1) implies (2), and that (3) implies (2). By [EP, Theorem 5.3.1], (2) implies (3). Furthermore, (2) implies that M is a MCM R-module by [EP, Corollary 3.11], and then Theorem 4.1 implies (1).

We can now state a complete analogue of Theorem 1.1:

**Theorem 10.5.** Let  $f_1, \ldots, f_c$  be a regular sequence in a regular local ring S. Set  $R = S/(f_1, \ldots, f_c)$ . A finitely generated R-module N is MCM if and only if it is a CI matrix factorization module for the sequence  $f_1, \ldots, f_c$ .

*Proof.* Suppose that N is a CI matrix factorization module. Then it is a higher matrix factorization module in the sense of [EP, Definition 1.2]. By [EP, Corollary 3.11], it follows that N is a MCM R-module.

Suppose that N is MCM. The free resolution in Theorem 4.1 implies that N is a CI matrix factorization module.

As far as minimality goes, we have

## PDF page 23

Theorem 10.6 ([\[EP,](#page-22-1) Theorem 1.4]). *Let* S *be a regular local ring with infinite residue field, and let* I ⊂ S *be an ideal generated by a regular sequence of length* c*. Set* R = S/I *, and suppose that* W *is a finitely generated* R*-module. Let* f1, . . . , f<sup>c</sup> *be a generic choice of elements minimally generating* I *. If* M *is a sufficiently high syzygy of* W *over* R*, then* M *is the module of a minimal CI matrix factorization* (d, h) *with respect to* f1, . . . , fc*. Moreover* d ⊗ R *and* h ⊗ R *are the first two differentials in the minimal free resolution of* M *over* R*.*

*Acknowledgments.* We are grateful to Alexander Pavlov for helpful observations about MCMapproximations, and to Daniel R. Grayson and Mike Stillman, the makers of Macaulay2 [\[M2\]](#page-22-9); the packages CompleteIntersectionResolutions.m2 and MaximalCohenMacaulayApproximations.m2 implement the constructions in this paper.

The work on this paper profited from the good conditions for mathematics at MSRI, and was partially supported by the National Science Foundation under Grant 0932078000. The authors are grateful to the National Science Foundation for partial support under Grants DMS-1502190 and DMS-1406062.

# References

- [AB] Auslander, M., Buchweitz, R.-O.: The homological theory of maximal Cohen–Macaulay approximations. In: Colloque en l'honneur de Pierre Samuel (Orsay, 1987), Mem. Soc. ´ Math. France (N.S.) 38, 5–37 (1989) [Zbl 0697.13005](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0697.13005&format=complete) [MR 1044344](http://www.ams.org/mathscinet-getitem?mr=1044344)
- [AGP] Avramov, L., Gasharov, V., Peeva, I.: Complete intersection dimension. Publ. Math. IHES 86, 67–114 (1997) [Zbl 0918.13008](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0918.13008&format=complete) [MR 1608565](http://www.ams.org/mathscinet-getitem?mr=1608565)
- [Di] Ding, S.: Cohen–Macaulay approximations over a Gorenstein local ring, Ph.D. Thesis, Brandeis Univ. (1990) [MR 2638535](http://www.ams.org/mathscinet-getitem?mr=2638535)
- [Ei1] Eisenbud, D.: Homological algebra on a complete intersection, with an application to group representations. Trans. Amer. Math. Soc. 260, 35–64 (1980) [Zbl 0444.13006](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0444.13006&format=complete) [MR 0570778](http://www.ams.org/mathscinet-getitem?mr=0570778)
- [Ei2] Eisenbud, D.: Enriched free resolutions and change of rings. In: Seminaire d'Alg ´ ebre ` Paul Dubreil (Paris, 1975-1976), Lecture Notes in Math. 586, Springer, 1–8 (1977) [Zbl 0352.13004](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0352.13004&format=complete) [MR 0568883](http://www.ams.org/mathscinet-getitem?mr=0568883)
- [EP] Eisenbud, D., Peeva, I.: Minimal Free Resolutions over Complete Intersections. Lecture Notes in Math. 2152, Springer (2016) [Zbl 1342.13001](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1342.13001&format=complete) [MR 3445368](http://www.ams.org/mathscinet-getitem?mr=3445368)
- [Gu] Gulliksen, T.: A change of ring theorem with applications to Poincare series and intersection ´ multiplicity. Math. Scand. 34, 167–183 (1974) [Zbl 0292.13009](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0292.13009&format=complete) [MR 0364232](http://www.ams.org/mathscinet-getitem?mr=0364232)
- [M2] Macaulay2—a system for computation in algebraic geometry and commutative algebra programmed by D. Grayson and M. Stillman, <http://www.math.uiuc.edu/Macaulay2/>
- [Sh] Shamash, J.: The Poincare series of a local ring. J. Algebra ´ 12, 453–470 (1969) [Zbl 0189.04004](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0189.04004&format=complete) [MR 0241411](http://www.ams.org/mathscinet-getitem?mr=0241411)
