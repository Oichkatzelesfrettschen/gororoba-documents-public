Source: https://zenodo.org/records/23966061/files/AWC%20Conjecture%20L;%20Wedderburn%20Classification%20of%20Left%20Multiplication%20Enveloping%20Algebras%20of%20Cayley.pdf
PDF sha256: 137b7109a1c38a9a35e5ba45f44b049f36cb0bf4a1b5673559faa729fd05a06f
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of zhou_zhou_2026_awc_conjecture_l_wedderburn_left_multiplication_enveloping_algebras_cayley_dickson.pdf

Transcription of `zhou_zhou_2026_awc_conjecture_l_wedderburn_left_multiplication_enveloping_algebras_cayley_dickson.pdf` in this directory, 38 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

# AWC Conjecture L: Wedderburn Classification of Left Multiplication Enveloping Algebras of Cayley–Dickson Algebras in Characteristic p and a Refutation of the Cartan Doubling Recursion

Zhou Changzheng, Zhou Ziqing Email: ziqing-zhou@outlook.com

November 4, 2026

#### Abstract

Let  $\mathbb{F}_p$  be the prime field, and let  $A_n$  be the n-th Cayley-Dickson doubling algebra, of dimension  $2^n$ . This paper studies the Wedderburn structure over  $\mathbb{F}_p$  of the left multiplication enveloping algebra  $\operatorname{Env}_L(A_n)$  of  $A_n$ , and examines the feasibility of a Cartan-matrix recursion along the doubling tower. The classification result falls into four branches: when p=2,  $A_n$  is commutative and associative,  $\operatorname{Env}_L(A_n)\cong A_n$  is a local algebra, and the Cartan matrix is  $[2^n]$ ; when p is odd and n=1,  $\operatorname{Env}_L(A_1)$  is isomorphic to  $A_1$ , which either splits as  $\mathbb{F}_p \times \mathbb{F}_p$  or is the field  $\mathbb{F}_{p^2}$ , with Cartan matrices  $I_2$  and [1], respectively; when p is odd and n=2, the left regular representation gives  $\operatorname{Env}_L(A_2)\cong A_2\cong M_2(\mathbb{F}_p)$ , of dimension 4; when p is odd and  $n\geq 3$ ,  $\operatorname{Env}_L(A_n)=\operatorname{End}_{\mathbb{F}_p}(A_n)\cong M_{2^n}(\mathbb{F}_p)$ , and the Cartan matrix is [1]. Along with the classification is a basis-product closure fact: for every prime p and every p, the ordered product of standard basis elements is still a signed multiple of some standard basis element and is nonzero; hence statistics supported on zero basis pairs with positive density are empty at the object level. On this basis, a Cartan doubling recursion of the form

$$C_{n+1} = \begin{pmatrix} C_n & X \\ X^\mathsf{T} & C_n \end{pmatrix} + \Delta_n$$

cannot hold at the matrix-size level: for every  $n \geq 1$ , the size of  $C_{n+1}$  is always 1, whereas the right-hand side of the recursion is assembled from two copies of  $C_n$  and hence has size at least 2; at the same time, permuting rows and columns does not change matrix size, so this excludes dependence on the specific values of the cross blocks and correction terms. Exact integer and modular-arithmetic enumerations over finite ranges provide consistency checks for structure constants, block formulas, closure dimensions, and centralizers; the general conclusions are independently supported by the classification proof and the size inequality.

**Keywords**: Cayley–Dickson algebras; left multiplication enveloping algebras; Wedderburn classification; Cartan matrices; finite fields; doubling recursion.

## PDF page 2

#### 1 Introduction

The Cayley–Dickson construction starts from a base field and, by repeated doubling, generates a sequence of algebras whose dimensions are successively doubled: one-dimensional, two-dimensional, four-dimensional, eight-dimensional, and in general  $2^n$ -dimensional. Its low-dimensional members are, respectively, a field, a quadratic algebra, a quaternion algebra, and an octonion algebra, while the higher-dimensional members gradually lose associativity, commutativity, and even alternativity. This construction has a foundational position in the theory of nonassociative algebras; its systematic treatment can be traced back to Schafer's 1966 monograph (Schafer, 1966), in which associative multiplication algebras were established as a general tool for studying the structure of nonassociative algebras. Over the real field, Biss, Dugger, and Isaksen (2008) studied upper bounds for the dimensions of annihilators of elements in Cayley–Dickson algebras, and Biss, Christensen, Dugger, and Isaksen (2009) subsequently systematized the theory of eigenvalues and eigenvectors in order to clarify several structural properties of these algebras. These works take the real field as the base field and focus on spectral properties and annihilators as core objects.

In this paper we take the finite field  $\mathbb{F}_p$  as the base field. The object of study is the left multiplication enveloping algebra: the unital subalgebra generated over  $\mathbb{F}_p$  by all left multiplication operators  $L_x$ . The goal is the Wedderburn structure of this algebra, that is, its position in the classification of finite-dimensional  $\mathbb{F}_p$ -algebras—whether it is a local algebra, a full matrix algebra, or a field or a direct product of fields. Wedderburn theory over finite fields itself takes associative algebras as its standard framework, but when the base algebra is nonassociative, the left multiplication operators no longer preserve multiplication, and the structure of the enveloping algebra cannot be read directly from the multiplication table of the base algebra. For this reason, the structural determination case by case in n and p requires independent argument and cannot be transplanted from spectral conclusions over the real field.

The key dividing line of the classification is at n=2. The quaternion algebra  $A_2$  is a four-dimensional associative algebra; when p is odd, its norm form is a nondegenerate quadratic form, and over a finite field every nondegenerate quadratic form in at least three variables is isotropic, so  $A_2$  splits and is isomorphic to  $M_2(\mathbb{F}_p)$ . The left regular map  $a \mapsto L_a$  is an algebra homomorphism when  $A_2$  is associative; its kernel is zero, and the dimension of its image is 4, exactly that of  $M_2(\mathbb{F}_p)$ . The full endomorphism algebra  $\operatorname{End}(A_2)$ , however, is  $M_4(\mathbb{F}_p)$ , of dimension 16. Therefore  $\operatorname{Env}_L(A_2)$  is not isomorphic to  $\operatorname{End}(A_2)$ , and n=2 must be treated as an independent case. When  $n\geq 3$ , associativity is lost, and the algebra generated by the left multiplication operators instead expands to the full endomorphism algebra; the proof of this turn requires a separate first step  $n=2\to 3$ , whose surjectivity comes from the associativity and central simplicity of  $A_2$ , rather than from a general induction hypothesis. The case p=2 goes to the opposite extreme: the square of the doubling generator degenerates to 1, the basis elements commute and are associative, and  $A_n$  becomes  $\mathbb{F}_2[(C_2)^n]$ , whose enveloping algebra is a local algebra.

Parallel to the classification is the reading of the Cartan matrix. A full matrix algebra is semisimple, its unique simple module is the natural module, and its unique indecomposable projective module is isomorphic to that simple module; the Cartan multiplicity is 1, and the matrix is the  $1 \times 1$  matrix [1], rather than the identity matrix. For a local algebra, the Cartan element is the composition multiplicity, and the composition multiplicity of the regular module equals  $2^n$ . This reading, together with the classifica-

## PDF page 3

tion, directly constrains the possible form of a recursion for the Cartan matrix along the doubling tower. If a recursion writes Cn+1 as the block concatenation of two copies of C<sup>n</sup> plus a correction term, then the size of the right-hand side is at least 2rn; but the classification gives that the size of Cn+1 is always 1, so the size equality is impossible, and there is no need to inspect any entries of the cross blocks or correction terms.

The framework of zero-divisor graphs of commutative rings—with vertices the nonzero zero-divisors and edges joining distinct vertices whose product is zero—has a complete theory in the commutative case, and its algebraic premises are commutativity of multiplication and the existence of zero-divisors. The standard basis products of Cayley–Dickson algebras do not fall under these premises: the ordered product of basis elements is still a signed multiple of some basis element and is nonzero, so the set of zero basis pairs is empty. Therefore, transplanting density statistics of zero-divisor-graph type directly onto Cayley–Dickson basis products has no corresponding nonempty set at the object level. This fact is independent of the classification, but together they delimit the range of structural assertions available over finite fields.

The paper proceeds as follows. We first give the Cayley–Dickson construction and the definition of the left multiplication enveloping algebra; then we state and prove the classification theorem case by case, where p = 2, n = 1, n = 2, and n ≥ 3 are treated separately, and n = 2 → 3 is argued independently; next comes the basis-product closure theorem; then the exclusion of the doubling recursion derived from the classification and the Cartan reading; and finally the exact enumeration certificates over finite ranges and the scope declaration. The general conclusions do not depend on the enumeration certificates; the certificates only check the implementation consistency of structure constants and closure dimensions within the certified range.

# 2 Cayley–Dickson Construction, Left-Multiplication Envelope Algebra, and Preliminary Lemmas

This chapter fixes the notation used throughout the paper and proves the three preliminary lemmas on which the classification theorem depends. Let F<sup>p</sup> be the prime field, let A<sup>n</sup> be the n-th Cayley–Dickson doubled algebra of dimension N = 2<sup>n</sup> ; let L<sup>x</sup> and R<sup>x</sup> denote the left and right multiplication operators, respectively, and let EnvL(An) denote the unital subalgebra of End<sup>F</sup><sup>p</sup> (An) generated over F<sup>p</sup> by all Lx, called the left-multiplication envelope algebra of An. Cartan matrices are defined with respect to a complete set of primitive orthogonal idempotents; the size of a matrix is invariant under simultaneous permutation of rows and columns.

# 2.1 Cayley–Dickson Construction and Basic Identities

Take A<sup>0</sup> = Fp, and construct recursively by An+1 = A<sup>n</sup> ⊕ An. For (a, b),(c, d) ∈ An+1, multiplication and conjugation are defined by

$$(a,b)(c,d) = (ac - \bar{d}b, da + b\bar{c}), \quad \overline{(a,b)} = (\bar{a},-b).$$

## PDF page 4

The standard basis is denoted by  $e_0 = 1, e_1, \dots, e_{N-1}$ , where  $\bar{e}_0 = e_0$  and  $\bar{e}_i = -e_i$  for  $i \geq 1$ . Denote the conjugation map by  $C(x) = \bar{x}$ . Since conjugation is an anti-automorphism, one directly obtains

$$CL_xC = R_{\bar{x}}, \qquad CR_xC = L_{\bar{x}}.$$

These two identities are different, and in the sequel they are used only in the directions stated above.

According to the block decomposition  $A_n \oplus A_n$ , the left multiplication operators satisfy

$$L_{(a,0)} = \operatorname{diag}(L_a, R_a), \qquad L_{(0,b)} = \begin{pmatrix} 0 & -R_bC \\ L_bC & 0 \end{pmatrix}.$$

These block formulas follow directly from the doubled multiplication formula and are the basic tool for the subsequent induction.

#### 2.2 Preliminary Lemmas

**Lemma 2.1 (Centrality).** Let p be odd and  $n \geq 2$ . Then  $Z(A_n) = \mathbb{F}_p$ .

*Proof.* Let  $(a,b) \in A_{n+1}$  belong to the center. First commute it with all elements (c,0), and compute

$$(a,b)(c,0) = (ac, b\bar{c}),$$
  $(c,0)(a,b) = (ca,bc).$ 

Comparing the two components gives ac = ca and  $b\bar{c} = bc$  for all c. Taking  $c = e_1$ , we obtain  $b(-e_1) = be_1$ , that is,  $2be_1 = 0$ ; since p is odd and  $e_1$  is invertible  $(e_1^2 = -1)$ , it follows that b = 0. Thus central elements have the form (a, 0), with  $a \in Z(A_n)$ . Commuting next with (0, c) gives  $ca = c\bar{a}$  for all c; taking c = 1 yields  $a = \bar{a}$ . Therefore

$$Z(A_{n+1}) = \{(a,0) : a \in Z(A_n), \ a = \bar{a}\}.$$

When n = 1,  $A_1 = \mathbb{F}_p[x]/(x^2 + 1)$ , conjugation is  $x \mapsto -x$ , and the fixed elements are exactly  $\mathbb{F}_p$ ; hence  $Z(A_2) = \mathbb{F}_p$ . By induction from the displayed formula,  $Z(A_n) = \mathbb{F}_p$  for all  $n \geq 2$ . This completes the proof.

**Lemma 2.2 (Subdirect Product Dichotomy).** Let F be a subalgebra of  $M_N(\mathbb{F}_p) \oplus M_N(\mathbb{F}_p)$  such that the projections of F onto both factors are surjective. Then either F is the entire direct sum, or F is the graph of some automorphism  $\sigma \in \operatorname{Aut}(M_N(\mathbb{F}_p))$ , that is,

$$F = \{(X, \sigma(X)) : X \in M_N(\mathbb{F}_p)\}.$$

Proof. Let  $\pi_1, \pi_2$  be the two coordinate projections, and set  $I_1 = F \cap (M_N \oplus 0)$ ,  $I_2 = F \cap (0 \oplus M_N)$ . First prove that  $I_1$  is a two-sided ideal of  $M_N$ :  $I_1$  is an ideal of F; for any  $X \in M_N$  and  $t \in I_1$ , since  $\pi_1|_F$  is surjective, there exists  $f \in F$  with  $\pi_1(f) = X$ , so  $Xt = \pi_1(ft) \in I_1$ , and similarly  $tX = \pi_1(tf) \in I_1$ . By simplicity of  $M_N(\mathbb{F}_p)$ ,  $I_1$  is either zero or the whole algebra; the same holds for  $I_2$ . If  $I_1$  is the whole algebra, then for any  $Y \in M_N$ , by surjectivity of  $\pi_2|_F$  there exists  $(X,Y) \in F$ , while  $(X,0) \in F$ , hence  $(0,Y) = (X,Y) - (X,0) \in F$ , so  $I_2$  is also the whole algebra. Therefore, after excluding the mixed case in which one of  $I_1, I_2$  is the whole algebra and the other is zero, only two possibilities remain: either both  $I_1$  and  $I_2$  are the whole algebra, in which case  $F = M_N \oplus M_N$ ; or both  $I_1$  and  $I_2$  are zero, in which case the kernels of  $\pi_1|_F$  and  $\pi_2|_F$  are

## PDF page 5

both zero, and by the surjectivity assumption both are isomorphisms; then  $\sigma = \pi_2 \circ \pi_1^{-1}$  is an automorphism of  $M_N(\mathbb{F}_p)$ , and F is exactly the graph of  $\sigma$ . This completes the proof.

Lemma 2.3 (Diagonalization of Doubled Blocks). For any  $b, b' \in A_n$ ,

$$L_{(0,b)}L_{(0,b')} = \operatorname{diag}(-R_b R_{\bar{b}'}, -L_b L_{\bar{b}'}).$$

In particular, taking b=b'=1 gives  $L^2_{(0,1)}=-\operatorname{id}$ . Therefore, when p is odd,  $L_{(0,1)}$  is invertible.

*Proof.* Substitute directly into the block formula and use  $CL_xC = R_{\bar{x}}$ ,  $CR_xC = L_{\bar{x}}$ . Taking b = b' = 1, we have  $R_1 = L_1 = \mathrm{id}$ , so the square is  $-\mathrm{id}$ . When p is odd,  $-1 \neq 0$ , so the operator is invertible. This completes the proof.

# 3 Wedderburn Classification of the Left-Multiplication Envelope Algebra

This chapter gives a complete Wedderburn classification of the left-multiplication envelope algebra. Notation and preliminary lemmas are as in Chapter 2.

#### 3.1 Statement of the Theorem

**Theorem 3.1.** Let p be a prime and let  $A_n$  be the n-th Cayley-Dickson algebra.

- (1) p = 2.  $A_n$  is commutative and associative,  $A_n \cong \mathbb{F}_2[(C_2)^n]$ ;  $\operatorname{Env}_L(A_n) \cong A_n$  is a local algebra, the Jacobson radical has dimension  $2^n 1$ , and the Cartan matrix is  $[2^n]$ .
- (2) p is odd and n = 1.  $A_1 = \mathbb{F}_p[x]/(x^2 + 1)$ . If -1 is a square modulo p, then  $A_1 \cong \mathbb{F}_p \times \mathbb{F}_p$ , and the Cartan matrix is  $I_2$ ; if -1 is not a square modulo p, then  $A_1 \cong \mathbb{F}_{p^2}$ , and the Cartan matrix is [1].
- (3) p is odd and n = 2.  $A_2 \cong M_2(\mathbb{F}_p)$ , and  $a \mapsto L_a$  is an algebra isomorphism from  $A_2$  to  $\operatorname{Env}_L(A_2)$ , so  $\operatorname{Env}_L(A_2) \cong M_2(\mathbb{F}_p)$ ; the Cartan matrix is [1].
  - (4) p is odd and  $n \geq 3$ .  $\operatorname{Env}_L(A_n) = \operatorname{End}_{\mathbb{F}_p}(A_n) \cong M_{2^n}(\mathbb{F}_p)$ ; the Cartan matrix is [1].

## PDF page 6

Classification roadmap for EnvL(An) over F<sup>p</sup>

Legend: blue nodes describe the characteristic 2 branch; green nodes are case splits for odd characteristic; yellow nodes are the resulting Wedderburn types and Cartan matrices.

Figure 1: Case split of Theorem 3.1.

# 3.2 Preliminary Facts

This chapter uses four preliminary facts. Noncommutativity is newly proved in this chapter; centrality, the subdirect product dichotomy, and diagonalization of doubled blocks have already been proved as Lemmas 2.1, 2.2, and 2.3 in Chapter 2, and are restated here in the notation of this chapter so that internal references in this chapter are self-contained.

Fact 3.1 (Noncommutativity). Let p be odd and n ≥ 2. Then A<sup>n</sup> is noncommutative. In particular, L<sup>e</sup><sup>1</sup> ̸= R<sup>e</sup><sup>1</sup> .

Proof. In the Cayley–Dickson basis, e1e<sup>2</sup> = −e2e1, and e1e<sup>2</sup> is some ±ek, hence nonzero. If e1e<sup>2</sup> = e2e1, then 2e1e<sup>2</sup> = 0; since p is odd and e1e<sup>2</sup> ̸= 0, this is a contradiction. Hence A<sup>n</sup> is noncommutative. Taking x = e2, we get L<sup>e</sup><sup>1</sup> (e2) = e1e<sup>2</sup> ̸= e2e<sup>1</sup> = R<sup>e</sup><sup>1</sup> (e2), so

## PDF page 7

$L_{e_1} \neq R_{e_1}$ . This completes the proof.

Fact 3.2 (Centrality). Let p be odd and  $n \geq 2$ . Then  $Z(A_n) = \mathbb{F}_p$ .

*Proof.* Let  $(a,b) \in A_{n+1}$  belong to the center. First commute it with all (c,0), and compute

$$(a,b)(c,0) = (ac, b\bar{c}),$$
  $(c,0)(a,b) = (ca,bc).$ 

Comparing the two components gives ac = ca and  $b\bar{c} = bc$  for all c. Taking  $c = e_1$ , we obtain  $b(-e_1) = be_1$ , that is,  $2be_1 = 0$ ; since p is odd and  $e_1$  is invertible  $(e_1^2 = -1)$ , it follows that b = 0. Thus central elements have the form (a, 0), with  $a \in Z(A_n)$ . Commuting next with (0, c) gives  $ca = c\bar{a}$  for all c; taking c = 1 yields  $a = \bar{a}$ . Therefore

$$Z(A_{n+1}) = \{(a,0) : a \in Z(A_n), \ a = \bar{a}\}.$$

When n = 1,  $A_1 = \mathbb{F}_p[x]/(x^2 + 1)$ , conjugation is  $x \mapsto -x$ , and the fixed elements are exactly  $\mathbb{F}_p$ ; hence  $Z(A_2) = \mathbb{F}_p$ . By induction from the displayed formula,  $Z(A_n) = \mathbb{F}_p$  for all  $n \geq 2$ . This completes the proof.

Fact 3.3 (Subdirect Product Dichotomy). Let F be a subalgebra of  $M_N(\mathbb{F}_p) \oplus M_N(\mathbb{F}_p)$  such that the projections of F onto both factors are surjective. Then either F is the entire direct sum, or F is the graph of some automorphism  $\sigma \in \operatorname{Aut}(M_N(\mathbb{F}_p))$ , that is,

$$F = \{ (X, \sigma(X)) : X \in M_N(\mathbb{F}_p) \}.$$

Proof. Let  $\pi_1, \pi_2$  be the two coordinate projections, and set  $I_1 = F \cap (M_N \oplus 0)$ ,  $I_2 = F \cap (0 \oplus M_N)$ . First prove that  $I_1$  is a two-sided ideal of  $M_N$ :  $I_1$  is an ideal of F; for any  $X \in M_N$  and  $t \in I_1$ , since  $\pi_1|_F$  is surjective, there exists  $f \in F$  with  $\pi_1(f) = X$ , so  $Xt = \pi_1(ft) \in I_1$ , and similarly  $tX = \pi_1(tf) \in I_1$ . By simplicity of  $M_N(\mathbb{F}_p)$ ,  $I_1$  is either zero or the whole algebra; the same holds for  $I_2$ . If  $I_1$  is the whole algebra, then for any  $Y \in M_N$ , by surjectivity of  $\pi_2|_F$  there exists  $(X,Y) \in F$ , while  $(X,0) \in F$ , hence  $(0,Y) = (X,Y) - (X,0) \in F$ , so  $I_2$  is also the whole algebra. Therefore, after excluding the mixed case in which one of  $I_1, I_2$  is the whole algebra and the other is zero, only two possibilities remain: either both  $I_1$  and  $I_2$  are the whole algebra, in which case  $F = M_N \oplus M_N$ ; or both  $I_1$  and  $I_2$  are zero, in which case the kernels of  $\pi_1|_F$  and  $\pi_2|_F$  are both zero, and by the surjectivity assumption both are isomorphisms; then  $\sigma = \pi_2 \circ \pi_1^{-1}$  is an automorphism of  $M_N(\mathbb{F}_p)$ , and F is exactly the graph of  $\sigma$ . This completes the proof.

Fact 3.4 (Diagonalization of Doubled Blocks). For any  $b, b' \in A_n$ ,

$$L_{(0,b)}L_{(0,b')} = \operatorname{diag}(-R_b R_{\bar{b}'}, -L_b L_{\bar{b}'}).$$

In particular, taking b=b'=1 gives  $L^2_{(0,1)}=-\mathrm{id}$ . Therefore, when p is odd,  $L_{(0,1)}$  is invertible.

*Proof.* Substitute directly into the block formula

$$L_{(0,b)} = \begin{pmatrix} 0 & -R_b C \\ L_b C & 0 \end{pmatrix}$$

and use  $CL_xC = R_{\bar{x}}$ ,  $CR_xC = L_{\bar{x}}$ . Taking b = b' = 1, we have  $R_1 = L_1 = \mathrm{id}$ , so the square is  $-\mathrm{id}$ . When p is odd,  $-1 \neq 0$ , so the operator is invertible. This completes the proof.

## PDF page 8

#### **3.3** The Case p = 2

The associator of a Cayley–Dickson algebra is alternating in its three variables and trilinear; on basis triples, the associator takes values in  $\{0, \pm 2e_m\}$ . Induct on the doubling index: the four index types reduce to associators of the algebra one level lower; the case in which all entries lie in the second copy is eliminated by the alternating cyclic identity (x, y, z) = (y, z, x). Hence, after reduction modulo 2, the associator is identically zero. Similarly, the commutator  $e_i e_j - e_j e_i$  takes values in  $\{0, \pm 2e_k\}$  on basis elements, and is zero modulo 2. Thus  $A_n$  is commutative and associative in characteristic 2.

The doubling units  $u_j = e_{2^{j-1}}$  (j = 1, ..., n) satisfy  $u_j^2 = -1 = 1$  and commute with one another; they generate  $A_n$ . Therefore  $g_j \mapsto u_j$  gives an isomorphism from  $\mathbb{F}_2[(C_2)^n]$  to  $A_n$ , since both sides have dimension  $2^n$ . The augmentation ideal is nilpotent, so  $A_n$  is local. Since  $A_n$  is associative, the left regular representation is faithful, and the image of  $\operatorname{Env}_L(A_n)$  is  $A_n$  itself, so  $\operatorname{Env}_L(A_n) \cong A_n$ . A local algebra has a unique simple module, namely the trivial module, and a unique indecomposable projective module, namely the regular module, of dimension  $2^n$ ; hence the Cartan matrix is  $[2^n]$ .

#### **3.4** The Case p Odd and n = 1

 $A_1 = \mathbb{F}_p[x]/(x^2+1)$ . If -1 is a square, then  $x^2+1$  splits and  $A_1 \cong \mathbb{F}_p \times \mathbb{F}_p$ ; the two simple modules are nonisomorphic, and each indecomposable projective module is isomorphic to the corresponding simple module, so the Cartan matrix is  $I_2$ . If -1 is not a square, then  $A_1$  is the field  $\mathbb{F}_{p^2}$ ; the unique simple module is the regular module itself, and the unique indecomposable projective module is isomorphic to that simple module, so the Cartan multiplicity is 1, and the Cartan matrix is [1]. In both cases  $A_1$  is associative, and the left regular representation gives  $\mathrm{Env}_L(A_1) \cong A_1$ .

# **3.5** The Case p Odd and n=2

The norm form of the quaternion algebra  $A_2$  is a nondegenerate quadratic form. Over a finite field, every nondegenerate quadratic form in at least 3 variables is isotropic; hence  $A_2$  has nonzero zero divisors and is not a division algebra.  $A_2$  is a four-dimensional central simple algebra; a four-dimensional central simple algebra that is a division algebra must be a field, contradicting its noncommutativity. Hence  $A_2 \cong M_2(\mathbb{F}_p)$ . Since  $A_2$  is associative,  $L_{ab} = L_a L_b$ , so the left regular representation  $a \mapsto L_a$  is an algebra homomorphism; its kernel is zero, hence it is injective. The dimension of its image equals the dimension of  $A_2$ , namely 4, while the dimension of  $\operatorname{End}_{\mathbb{F}_p}(A_2)$  is 16; therefore the image is exactly  $M_2(\mathbb{F}_p)$ . Thus  $\operatorname{Env}_L(A_2) \cong M_2(\mathbb{F}_p)$ . The full matrix algebra  $M_2(\mathbb{F}_p)$  is semisimple, its unique simple module is the natural module, and its unique indecomposable projective module is isomorphic to the natural module; the Cartan matrix is [1].

## PDF page 9

#### **3.6** The Case p Odd and $n \geq 3$

#### **3.6.1** First Step: $n = 2 \to 3$

 $A_2$  is associative and central simple, with center  $\mathbb{F}_p$ . The natural map

$$A_2 \otimes_{\mathbb{F}_n} A_2^{\mathrm{op}} \to \mathrm{End}_{\mathbb{F}_n}(A_2), \qquad a \otimes c \mapsto L_a R_c$$

is the structural isomorphism for central simple algebras; hence

$$\operatorname{span}\{L_a R_c : a, c \in A_2\} = \operatorname{End}_{\mathbb{F}_p}(A_2) = M_4(\mathbb{F}_p).$$

Here we used the associativity of  $A_2$ :  $L_a$  and  $R_c$  commute as operators.

Let  $E = \operatorname{Env}_L(A_3) \subseteq \operatorname{End}(A_3) = M_8(\mathbb{F}_p)$ , and let  $F = E \cap (M_4 \oplus M_4)$  be the diagonal part of E. Write  $P_a = L_{(a,0)} = \operatorname{diag}(L_a, R_a)$ ,  $Q_b = L_{(0,b)}$ . The even words  $P_a Q_b Q_{b'}$  and  $Q_b Q_{b'} P_{a'}$  both belong to F. By Fact 3.4,

$$Q_b Q_{b'} = \operatorname{diag}(-R_b R_{\bar{b}'}, -L_b L_{\bar{b}'}).$$

Thus the two diagonal blocks of  $P_aQ_bQ_{b'}$  are of the form  $L_aR_c$  and  $R_cL_a$ , respectively. Since span $\{L_aR_c\}=M_4$  and associativity of  $A_2$  makes left and right multiplication commute, the projections of F onto both  $M_4$ -factors are surjective. By Fact 3.3, either  $F=M_4\oplus M_4$ , or F is the graph of some automorphism  $\sigma$ .

If F is the graph of  $\sigma$ , then from  $\operatorname{diag}(L_a, R_a) \in F$  we obtain  $\sigma(L_a) = R_a$  for all  $a \in A_2$ . By Skolem-Noether,  $\sigma = \operatorname{Ad}_G$  for some invertible G. Evaluating the relation  $GL_aG^{-1} = R_a$  at  $1 \in A_2$  gives G(ag) = a, where  $g = G^{-1}(1)$ . Hence  $A_2g = A_2$ , so g is invertible, and  $G = R_{g^{-1}}$ . Substituting back gives  $R_{g^{-1}}L_aR_g = R_a$ ; here, by associativity of  $A_2$ ,  $A_3$  commutes with  $A_3$ , so  $A_3 = A_3$  for all  $A_3 = A_3$ . But by Fact 3.1,  $A_3 = A_3$  contradiction. Therefore  $A_3 = A_3$  for all  $A_3 = A_3$ .

Finally, by Fact 3.4,  $Z = L_{(0,1)}$  satisfies  $Z^2 = -\operatorname{id}$ , so Z is invertible. Multiplication by Z sends F onto all off-diagonal blocks; hence  $E = M_8(\mathbb{F}_p) = \operatorname{End}(A_3)$ . The first step is established.

#### **3.6.2** General Induction $n \to n+1$ for $n \ge 3$

Assume that  $\operatorname{Env}_L(A_n) = \operatorname{End}(A_n) = M_N(\mathbb{F}_p)$ , where  $N = 2^n$ . From  $CL_xC = R_{\bar{x}}$  we obtain

$$\operatorname{Env}_R(A_n) = C \operatorname{Env}_L(A_n)C = \operatorname{End}(A_n) = M_N.$$

Let 
$$E = \operatorname{Env}_L(A_{n+1}) \subseteq \operatorname{End}(A_{n+1}) = M_{2N}(\mathbb{F}_p)$$
, and  $F = E \cap (M_N \oplus M_N)$ .

The subalgebra F contains all even words  $P_{a_1} \cdots P_{a_k}$  involving only P-factors. Its first projection is  $L_{a_1} \cdots L_{a_k}$ , and all such left-multiplication words span  $\operatorname{Env}_L(A_n) = M_N$ ; its second projection is  $R_{a_1} \cdots R_{a_k}$ , and all such right-multiplication words span  $\operatorname{Env}_R(A_n) = M_N$ . Hence the projections of F onto both  $M_N$ -factors are surjective. By Fact 3.3, either  $F = M_N \oplus M_N$ , or F is the graph of some automorphism  $\sigma$ .

If F is the graph of  $\sigma$ , then from  $\operatorname{diag}(L_a, R_a) \in F$  we obtain  $\sigma(L_a) = R_a$  for all  $a \in A_n$ . By Skolem-Noether,  $\sigma = \operatorname{Ad}_G$  for some invertible G. The following derivation uses only two structural facts that hold at every level of the doubling tower. The first is the flexible identity (xy)x = x(yx), verified directly level by level from the doubled multiplication formula, whose linearization is

$$(xy)z + (zy)x = x(yz) + z(yx);$$

## PDF page 10

the second is the operator identity obtained from  $GL_aG^{-1}=R_a$  by composition and evaluation. To make the argument valid at every level of the tower, this step uses only the facts stated above, which hold at every level; the argument does not use alternativity or any of its consequences (such as cancellation properties of invertible elements in alternative algebras). All cancellation needed is supplied by the operator fact that G and  $R_g$  are mutually inverse maps, a fact involving only composition of operators, not the associativity of multiplication.

Evaluating the relation  $GL_aG^{-1}=R_a$  at  $1 \in A_n$  gives

$$G(ag) = a$$
 for all  $a \in A_n$ ,

where  $g = G^{-1}(1)$ . Write h = G(1).

Since G(ag) = a for all a, the composite map  $G \circ R_g$  is the identity; hence  $R_g$  is injective and G is surjective. Conversely, for any x, take a = G(x); from G(ag) = a and injectivity of G, we get ag = x, that is,  $R_g(G(x)) = x$ , so  $R_g \circ G$  is also the identity. Thus G and  $R_g$  are mutually inverse maps, and both are bijections. In particular, taking a = h in G(ag) = a gives G(hg) = h = G(1); by injectivity of G,

$$hq = 1$$
.

Multiplying  $GL_aG^{-1}=R_a$  on the left by G gives  $GL_a=R_aG$ , that is,

$$G(ay) = G(y)a$$
 for all  $a, y \in A_n$ .

Taking y = 1 gives  $G = L_h$ , that is, G is the left multiplication operator  $L_h$ , and  $L_h$  is a bijection. Taking a = g in this identity gives

$$h(gy) = (hy)g$$
 for all  $y \in A_n$ ;

the right-hand side is  $R_g(L_h(y)) = y$ , so h(gy) = y for all y, that is,  $L_hL_g$  is the identity. Since  $L_h$  is a bijection,  $L_g = L_h^{-1}$ , and hence  $L_gL_h$  is also the identity, that is,

$$g(ha) = a$$
 for all  $a \in A_n$ .

Taking a = 1 gives qh = 1.

Now take the triple (x, y, z) = (a, h, g) in the linearization of the flexible identity. The two terms on the left are (ah)g and (gh)a, and the two terms on the right are a(hg) and g(ha). Substituting hg = 1, gh = 1, and g(ha) = a, we obtain

$$(ah)q + a = a + a$$
, that is,  $(ah)q = a$ .

Comparing this with the previously obtained (ha)g = a, injectivity of  $R_g$  gives ah = ha for all  $a \in A_n$ , that is,  $h \in Z(A_n)$ . By Fact 3.2,  $Z(A_n) = \mathbb{F}_p$ , so  $h = \lambda \cdot 1$ , with  $\lambda \neq 0$ . From  $\lambda g = hg = 1$  (scalar multiplication being given by bilinearity), we get  $g = \lambda^{-1} \cdot 1$ . Therefore  $G = L_h$  is a scalar operator, and  $\sigma = \operatorname{Ad}_G$  is the identity automorphism. But  $\sigma(L_{e_1}) = R_{e_1}$ , while by Fact 3.1,  $L_{e_1} \neq R_{e_1}$ , a contradiction. Therefore  $F = M_N \oplus M_N$ .

Again by Fact 3.4,  $Z = L_{(0,1)}$  satisfies  $Z^2 = -\operatorname{id}$ , so it is invertible; multiplication by Z sends F onto all off-diagonal blocks, so  $E = M_{2N}(\mathbb{F}_p) = \operatorname{End}(A_{n+1})$ . The induction is complete.

## PDF page 11

#### 3.7 Cartan Readings

When p = 2, EnvL(An) ∼= A<sup>n</sup> is a local algebra. Its unique simple module is the trivial module, of dimension 1; its unique indecomposable projective module is the regular module, of dimension 2<sup>n</sup> . From the dimension identity dim P = [P : S] dim S, we get [P : S] = 2<sup>n</sup> , so the Cartan matrix is [2<sup>n</sup> ].

When p is odd and n = 1, in the split case A<sup>1</sup> ∼= F<sup>p</sup> × F<sup>p</sup> there are two simple modules, each indecomposable projective module is isomorphic to the corresponding simple module, and the Cartan matrix is I2; in the nonsplit case A<sup>1</sup> ∼= F<sup>p</sup> <sup>2</sup> is a field, the unique simple module and the unique indecomposable projective module coincide, and the Cartan matrix is [1].

When p is odd and n ≥ 2, by Theorem 3.1, EnvL(An) is the full matrix algebra Mm(Fp), where m = 2 for n = 2 and m = 2<sup>n</sup> for n ≥ 3. A full matrix algebra is semisimple, its unique simple module is the natural module, and its unique indecomposable projective module is isomorphic to the natural module; the dimension identity gives Cartan multiplicity 1. Therefore the Cartan matrix is the 1 × 1 matrix [1]. In particular, it is not Im.

#### 3.8 Exclusion of a Cartan Doubling Recursion

Let C<sup>n</sup> be the Cartan matrix of EnvL(An) with respect to an arbitrary complete set of primitive orthogonal idempotents. By Theorems 3.1 and 3.7, the size of C<sup>n</sup> is at most 2: in the split case n = 1 it is the 2 × 2 matrix I2; in all other cases it is the 1 × 1 matrix [1] or [2<sup>n</sup> ]. Therefore the size r<sup>n</sup> of C<sup>n</sup> belongs to {1, 2}; and for every n ≥ 1, rn+1 = 1, because when n + 1 ≥ 2, odd characteristic has already entered the full matrix algebra case, while in characteristic 2 the Cartan matrix [2<sup>n</sup>+1] is still 1 × 1.

Consider the formal recursion

$$C_{n+1} = \begin{pmatrix} C_n & X \\ X^T & C_n \end{pmatrix} + \Delta_n,$$

where X is an independent cross block. If the block decomposition is legitimate, the right-hand side is formed from two copies of C<sup>n</sup> and has size 2r<sup>n</sup> × 2rn. The left-hand side Cn+1 has size rn+1. If the equality holds, one must have rn+1 = 2rn. But rn+1 = 1 while 2r<sup>n</sup> ≥ 2: when r<sup>n</sup> = 1, the right-hand side has size 2 and the left-hand side has size 1; when r<sup>n</sup> = 2, the right-hand side has size 4 and the left-hand side has size 1. In each case they are unequal. A Cartan matrix permits only simultaneous permutation of rows and columns, and simultaneous permutation does not change the size of the matrix. Therefore this recursion is impossible at the level of matrix size for every prime p and every n ≥ 1, without checking the concrete entries of X or ∆n.

# 3.9 Description of a Reproducibility Algorithm

The following describes an algorithmic procedure that can be used for exact verification in finite ranges; it uses no floating-point arithmetic and does not depend on external data sources.

(1) Construction of structure constants. Recursively construct the multiplication table of A<sup>n</sup> by integer arithmetic according to the doubling formula. For each pair of basis

## PDF page 12

elements (e<sup>i</sup> , e<sup>j</sup> ), compute the four blocks according to (a, b)(c, d) = (ac − ¯db, da + bc¯), obtaining integer structure constants; then reduce modulo the target prime p.

- (2) Check that basis products are nonzero. Enumerate all ordered basis pairs (e<sup>i</sup> , e<sup>j</sup> ), compute the product, and check whether it is exactly ±e<sup>k</sup> and nonzero. The complexity of this check is O(2<sup>2</sup><sup>n</sup> ), suitable for full enumeration when n is small.
- (3) Left multiplication matrices and envelope dimension. For each basis element e<sup>i</sup> , construct the N × N matrix of the left multiplication operator L<sup>e</sup><sup>i</sup> . Starting from the identity operator and these generators, repeatedly take products and maintain a linear basis by Gaussian elimination modulo p until the dimension stabilizes; the resulting dimension is the dimension of EnvL(An).
- (4) Computation of the centralizer. Expand the condition ax = xa for all basis elements x into a system of linear equations in the coordinates of a, and solve for Z(An). This step is used to check instances of the centrality lemma in finite ranges.
- (5) Cartan readings. For a given finite-dimensional algebra, compute the Jacobson radical, decompose a complete set of primitive orthogonal idempotents, construct the indecomposable projective modules Λe<sup>i</sup> , compute the multiplicities of their simple heads, and obtain the Cartan matrix. For full matrix algebras and local algebras, one can check directly using the dimension identity in 3.7.
- (6) Scope declaration. The above algorithm gives only machine certification for finite n and finite p, and does not replace the general proofs in 3.3–3.6; its role is to check the implementation consistency of structure constants, block formulas, centrality, and closure dimensions within the certified range.

#### 3.10 Boundaries and Risk Statement

The conclusions of this chapter depend on three standard facts: every nondegenerate quadratic form in at least 3 variables over a finite field is isotropic; the Skolem–Noether theorem; and the natural structural map A ⊗ Aop → End(A) for central simple algebras is an isomorphism. These facts are used only as external standard results in the proof and are not reproved in this chapter.

The case n = 2 is a boundary case and cannot be merged into the full endomorphism case n ≥ 3; the first step n = 2 → 3 must be argued separately, and its surjectivity depends on the associativity and central simplicity of A2, which cannot be replaced by the general induction hypothesis. The surjectivity of the projections in the general induction for n ≥ 3 depends on all even words involving only first-kind doubling generators, not merely quadratic left-multiplication words; nonassociativity of A<sup>n</sup> means that long words cannot in general be reduced to quadratic words.

The key step in the graph argument for n ≥ 3, where a contradiction is derived from the graph assumption for σ, depends only on two independent preliminary facts: the flexible identity (xy)x = x(yx) (and its linearization, verified directly level by level from the doubled multiplication formula, valid at every level of the doubling tower) and the centrality conclusion of Fact 3.2. Both are proved before the classification theorem and do not depend on the classification conclusion, so the argument is not circular. It should be made explicit that the argument does not use alternativity, nor the cancellation property of invertible elements enjoyed only by alternative algebras; all cancellation appearing in the argument is supplied by the fact that G and R<sup>g</sup> are mutually inverse maps, a fact involving only operator composition and independent of the associativity of multiplica

## PDF page 13

tion. Likewise, any step that transfers the reasoning that "left and right multiplication commute" at n = 2 to n ≥ 3 is invalid, because A<sup>n</sup> is nonassociative and left and right multiplication operators do not commute in general.

The reading of the Cartan matrix depends on the choice of a complete set of primitive orthogonal idempotents, but the size of the matrix is invariant under simultaneous permutation of rows and columns; the Cartan matrix of a full matrix algebra is [1], not the identity matrix Im. The exclusion of the recursion is an impossibility at the level of matrix size and does not involve the concrete entries of X or ∆n.

Machine certification covers only finite ranges; the general conclusions of this chapter are given by the inductive proofs in 3.3–3.6.

# 4 Basis Product Closure Theorem

Doubling-basis multiplication patterns in An+1 = A<sup>n</sup> ⊕ A<sup>n</sup>

Legend: P<sup>i</sup> and Q<sup>i</sup> denote the lifted basis elements in An+1. The four displayed products are the only cases needed in the induction proofs, together with C(e<sup>j</sup> ) = δ<sup>j</sup> e<sup>j</sup> where δ<sup>0</sup> = 1 and δ<sup>j</sup> = −1 for j ≥ 1 when p is odd.

Figure 2: Four multiplication types for doubled basis elements.

#### 4.1 Problem Framework and Notation

This chapter discusses the multiplicative closure property of the standard basis of Cayley– Dickson algebras. We use the notation of Chapter 3 throughout: F<sup>p</sup> is the prime field, A<sup>n</sup>

## PDF page 14

is the n-th Cayley–Dickson doubled algebra of dimension N = 2<sup>n</sup> ; the standard basis is denoted by e<sup>0</sup> = 1, e1, . . . , eN−1; the conjugation map is denoted by C(x) = ¯x, satisfying C(e0) = e<sup>0</sup> and C(ei) = −e<sup>i</sup> for i ≥ 1. The doubling formula is

$$(a,b)(c,d) = (ac - C(d)b, da + bC(c)),$$

where a, b, c, d ∈ An. The standard basis of An+1 consists of two groups: the first group P<sup>i</sup> = (e<sup>i</sup> , 0), and the second group Q<sup>i</sup> = (0, ei), i = 0, . . . , N − 1.

The proposition to be proved in this chapter has two levels. The first is closure: the product of any two standard basis elements is again a signed multiple of some standard basis element. The second is nonvanishing: this signed multiple is nonzero. Both must be proved simultaneously and cannot replace each other. Nonvanishing has another independent route, for example, some basis elements are invertible; but invertibility can only exclude zero products and cannot imply that the product is still a single basis element. Therefore, the inductive proof of closure cannot be omitted.

This chapter does not rely on experimental data sets; the subsequent verification algorithms perform only exact integer and modular arithmetic enumeration in finite ranges, and are algorithmic consistency checks, not replacements for the general proof.

# 4.2 Conjugation Action and Multiplication Table of the Doubled Basis

In the standard basis, conjugation only changes signs and does not change basis indices. Specifically, there exist δ<sup>j</sup> ∈ {1, −1} such that

$$C(e_j) = \delta_j e_j,$$

where δ<sup>0</sup> = 1 and δ<sup>j</sup> = −1 for j ≥ 1. In Fp, the values of δ<sup>j</sup> vary with p: when p is odd, δj is as above; when p = 2, −1 = 1, so all δ<sup>j</sup> equal 1. In either case, δ<sup>j</sup> is a nonzero constant.

From the doubling formula one directly obtains the four types of basis-pair multiplications:

$$P_{i}P_{j} = (e_{i}e_{j}, 0);$$

$$P_{i}Q_{j} = (0, e_{j}e_{i});$$

$$Q_{i}P_{j} = (0, e_{i}C(e_{j}));$$

$$Q_{i}Q_{j} = (-C(e_{j})e_{i}, 0).$$

These four types cover all standard basis pairs of An+1. The subsequent induction uses only these four formulas and C(e<sup>j</sup> ) = δje<sup>j</sup> .

#### 4.3 Basis Product Closure Theorem

Theorem 4.1. Let p be any prime and n ≥ 0. For any i, j ∈ {0, . . . , 2 <sup>n</sup> − 1}, there exist k ∈ {0, . . . , 2 <sup>n</sup> − 1} and ε ∈ {1, −1} such that

$$e_i e_j = \varepsilon e_k,$$

and εe<sup>k</sup> ̸= 0. In particular, there are no zero basis pairs in the standard basis of An, that is, eie<sup>j</sup> = 0 never holds for any i, j.

## PDF page 15

#### 4.4 Inductive Proof

Proceed by induction on n.

Base case n = 0. Here A<sup>0</sup> = Fp, and the unique standard basis element is e<sup>0</sup> = 1. We have e0e<sup>0</sup> = e0; take ε = 1, k = 0, and the conclusion holds.

Induction hypothesis. Assume that the standard basis of A<sup>n</sup> satisfies Theorem 4.1: for any i, j, there exist k and ε ∈ {1, −1} such that eie<sup>j</sup> = εek, and εe<sup>k</sup> ̸= 0.

Induction step n → n + 1. Consider the four types of basis pairs of An+1.

First type: PiP<sup>j</sup> . By the multiplication table,

$$P_i P_j = (e_i e_j, 0).$$

By the induction hypothesis, eie<sup>j</sup> = εek, where ε ∈ {1, −1} and e<sup>k</sup> is a standard basis element of An. Hence

$$P_i P_j = \varepsilon(e_k, 0) = \varepsilon P_k.$$

This is a signed multiple of a standard basis element of An+1, and εP<sup>k</sup> ̸= 0, because ε ̸= 0 and P<sup>k</sup> is a basis element.

Second type: PiQ<sup>j</sup> . By the multiplication table,

$$P_i Q_j = (0, e_j e_i).$$

By the induction hypothesis, eje<sup>i</sup> = εe<sup>l</sup> . Hence

$$P_i Q_j = \varepsilon(0, e_l) = \varepsilon Q_l.$$

Again we obtain a signed multiple of a standard basis element, and it is nonzero.

Third type: QiP<sup>j</sup> . By the multiplication table,

$$Q_i P_j = (0, e_i C(e_j)).$$

By the conjugation action, C(e<sup>j</sup> ) = δje<sup>j</sup> , with δ<sup>j</sup> ∈ {1, −1}. By the induction hypothesis, eie<sup>j</sup> = εek. Hence

$$e_i C(e_j) = \delta_j e_i e_j = \delta_j \varepsilon e_k.$$

Therefore

$$Q_i P_j = \delta_j \varepsilon Q_k.$$

Here δjε ∈ {1, −1}, Q<sup>k</sup> is a standard basis element, and δjεQ<sup>k</sup> ̸= 0.

Fourth type: QiQ<sup>j</sup> . By the multiplication table,

$$Q_i Q_j = (-C(e_j)e_i, 0).$$

From C(e<sup>j</sup> ) = δje<sup>j</sup> and the induction hypothesis eje<sup>i</sup> = εe<sup>l</sup> , we get

$$-C(e_j)e_i = -\delta_j e_j e_i = -\delta_j \varepsilon e_l.$$

Therefore

$$Q_i Q_j = -\delta_j \varepsilon P_l.$$

Here −δjε ∈ {1, −1}, P<sup>l</sup> is a standard basis element, and the product is nonzero.

All four types of basis pairs have been treated. In each case we obtain a form ε ′ em, where ε ′ ∈ {1, −1}, e<sup>m</sup> is a standard basis element of An+1, and ε ′ e<sup>m</sup> ̸= 0. The induction is complete, and Theorem 4.1 holds for all n ≥ 0 and all primes p.

## PDF page 16

The conditions used in the proof are as follows: the doubled multiplication formula is the definition; the conjugation action  $C(e_j) = \delta_j e_j$  is guaranteed by the recursive construction of the standard basis; the induction hypothesis contains both closure and nonvanishing, so the lower-level products in the four cases give both the basis index and the nonzero coefficient. When p = 2, both  $\delta_j$  and -1 degenerate to 1, but the statement "there exists  $\varepsilon \in \{1, -1\}$ " still holds, and nonvanishing also still holds, because basis elements are nonzero over  $\mathbb{F}_2$  and the coefficient is 1.

#### 4.5 The Event Space of Zero Basis Pairs Is Empty

Define the event set of zero basis-pair products of order n by

$$Z_n = \{(i, j) : e_i e_j = 0\}.$$

Theorem 4.1 directly gives  $Z_n = \emptyset$  for all  $n \ge 0$  and all primes p. Therefore, any counting or density statistic supported on  $Z_n$ , such as  $|Z_n|$  or  $|Z_n|/2^{2n}$ , is identically zero. Any statistical conclusion claiming that zero basis pairs have positive density is incompatible with Theorem 4.1. This conclusion is at the set level and does not depend on specific sampling or numerical approximation.

Two logical levels must be distinguished. First, zero basis pairs do not exist, so density analysis based on zero-basis-pair events is empty at the data level. Second, invertibility of basis elements can independently verify that a single basis element is nonzero, but it cannot imply that the product of two basis elements is still a single basis element. The closure part of Theorem 4.1 must be supplied by the inductive proof in 4.4; the nonvanishing part follows directly from the nonzero coefficients in the inductive proof. The two cannot replace each other.

Two statistical populations must also be distinguished. This theorem excludes the event that the product of an ordered pair  $(e_i, e_j)$  of standard basis elements is zero; the zero-divisor event for general element pairs (x, y) belongs to another population, is not covered by the exclusion of this theorem, and zero divisors in that population do indeed exist: for example, in characteristic 2,  $(1+e_1)^2 = 1+2e_1+e_1^2 = 0$ ; in characteristic 3, let  $u = e_1+e_2$ ; then  $u^2 = e_1^2+e_1e_2+e_2e_1+e_2^2 = -1+0-1 = 1$ , so  $(1+u)(2+u) = 2+3u+u^2 = 0$ . Therefore "the set of zero basis pairs is empty" does not imply "there are no zero divisors in the algebra": any statistic supported on zero basis pairs is identically zero, while the zero-divisor density statistic for general element pairs is an independent question that this paper neither asserts nor excludes. Accordingly, any zero-divisor density assertion whose statistical object is general element pairs cannot be directly refuted by this theorem, nor can it be directly supported by this theorem.

# 4.6 Description of a Finite-Range Verification Algorithm

The following algorithm is used for exact consistency checks for finite n and finite p; it uses no floating-point arithmetic and does not depend on external data sources.

Step one: construction of structure constants. Recursively construct the multiplication table of  $A_n$  by integer arithmetic according to the doubling formula. For each pair of basis elements, compute the four blocks according to

$$(a,b)(c,d) = (ac - C(d)b, da + bC(c)),$$

## PDF page 17

obtaining integer structure constants. This step uses only integer addition, subtraction, and sign changes.

Step two: reduction modulo p. Reduce the integer structure constants modulo the target prime p, obtaining the multiplication table over Fp.

Step three: enumeration of basis pairs. Enumerate all ordered basis pairs (e<sup>i</sup> , e<sup>j</sup> ), compute the product, and check whether the result is exactly of the form εek, where ε ∈ {1, −1} and e<sup>k</sup> is a standard basis element. Also check whether εe<sup>k</sup> is nonzero. The complexity of this enumeration is O(2<sup>2</sup><sup>n</sup> ), suitable for full checks when n is small.

Step four: check of negative events. Count the number of basis pairs satisfying eie<sup>j</sup> = 0, and verify that it is zero.

Step five: scope declaration. The above algorithm gives only machine certification for finite n and finite p, and does not replace the general inductive proof in 4.4. Its role is to check the implementation consistency of structure constants, conjugation signs, and the doubled multiplication table within the certified range.

#### 4.7 Conclusion, Boundaries, and Risk Statement

The conclusion rigorously proved in this chapter is: for any prime p and any n ≥ 0, the standard basis of the Cayley–Dickson algebra A<sup>n</sup> satisfies eie<sup>j</sup> = εek, ε ∈ {1, −1}, and εe<sup>k</sup> ̸= 0. Therefore the set of zero basis pairs is empty; according to the distinction between the two statistical populations in 4.5, this exclusion concerns the population of ordered pairs of standard basis elements, and any statistical conclusion with positivedensity support on zero basis pairs is false, while the zero-divisor density statistic for general element pairs is an independent question that this chapter neither asserts nor excludes.

Boundary cases include: when n = 0, there is only the unit basis element, and the conclusion holds directly; when p = 2, the signs ± are not distinguished, but existence and nonvanishing still hold; when i = 0 or j = 0, the product degenerates to another basis element and is included in the four formulas; the product of basis elements in the second copy involves conjugation, and conjugation only changes signs without changing basis indices, which is the key to the induction step. The theorem holds for both odd and even p, with no additional restriction needed.

Risks and limitations are as follows. First, the closure proof in this chapter depends on the recursive definition of the standard basis and the doubled multiplication formula; if a nonstandard basis is used, the conclusion should be stated as "the product of basis elements is a signed multiple of a basis element", and the sign structure may change. Second, the finite-range verification algorithm covers only small n and does not constitute a general proof; the general conclusion is borne by the inductive proof in 4.4. Third, nonvanishing can be discussed independently using invertibility, but that route cannot replace the closure proof; this chapter does not mistake nonvanishing for closure. Fourth, this chapter does not involve any unverified literature conclusions or data sources; all derivations are completed within the Cayley–Dickson construction and linear algebra over prime fields.

## PDF page 18

# 5 Impossibility of a Cartan Doubling Recursion

#### 5.1 Problem Framework and Notation

This chapter uses the notation and classification results of Chapter 3.  $\mathbb{F}_p$  is the prime field,  $A_n$  is the n-th Cayley-Dickson algebra, and  $\operatorname{Env}_L(A_n)$  is the unital subalgebra generated by all left multiplication operators. For a finite-dimensional  $\mathbb{F}_p$ -algebra  $\Lambda$ , take a complete set of primitive orthogonal idempotents  $e_1, \ldots, e_r$ , let  $P_i = \Lambda e_i$  be the indecomposable projective modules, and let  $S_i$  be the unique simple head of  $P_i$ . The Cartan matrix C is defined as the  $r \times r$  matrix whose (i, j)-entry is the composition multiplicity of  $S_i$  in  $P_j$ . The cardinality r of a complete set of primitive orthogonal idempotents equals the number of isomorphism classes of simple modules and does not depend on the specific choice; different choices only lead to simultaneous permutation of rows and columns. The matrix size r is invariant under simultaneous permutation.

This chapter considers the following formal block recursion: let  $C_n$  be the Cartan matrix of  $\operatorname{Env}_L(A_n)$ , of size  $r_n \times r_n$ ; let X be an  $r_n \times r_n$  matrix, and  $\Delta_n$  a  $2r_n \times 2r_n$  matrix; the recursion asserts

$$C_{n+1} = \begin{pmatrix} C_n & X \\ X^T & C_n \end{pmatrix} + \Delta_n.$$

If the size of X is not  $r_n \times r_n$ , or the size of  $\Delta_n$  is not  $2r_n \times 2r_n$ , then the block expression has mismatched sizes and the equality is undefined. Therefore, under the premise that the equality is defined, the right-hand side must have size  $2r_n \times 2r_n$ . This chapter uses only matrix sizes, not the concrete entries of X, and not the concrete entries of  $\Delta_n$ ; the condition of an "independent cross block" does not participate in the size argument.

#### 5.2 Cartan Matrix Sizes Given by the Classification

By the classification theorem of Chapter 3 and its Cartan readings, for every prime p and every  $n \ge 1$ , the size  $r_n$  of  $C_n$  satisfies:

First, when p is odd and n = 1, if -1 is a square modulo p, then  $\operatorname{Env}_L(A_1) \cong \mathbb{F}_p \times \mathbb{F}_p$ ,  $C_1 = I_2$ , and  $r_1 = 2$ ; if -1 is not a square modulo p, then  $\operatorname{Env}_L(A_1) \cong \mathbb{F}_{p^2}$ ,  $C_1 = [1]$ , and  $r_1 = 1$ .

Second, when p is odd and  $n \geq 2$ ,  $\operatorname{Env}_L(A_n)$  is a full matrix algebra,  $C_n = [1]$ , and  $r_n = 1$ . Here the full matrix algebra is  $M_2(\mathbb{F}_p)$  for n = 2, and  $M_{2^n}(\mathbb{F}_p)$  for  $n \geq 3$ ; in both cases the Cartan matrix is the  $1 \times 1$  matrix [1].

Third, when p = 2,  $\operatorname{Env}_L(A_n)$  is a local algebra,  $C_n = [2^n]$ , and  $r_n = 1$ .

Therefore, for every  $n \geq 1$ ,  $r_n$  belongs to  $\{1,2\}$ ; and for every  $n \geq 1$ ,  $r_{n+1} = 1$ . The reason for the latter assertion is:  $n+1\geq 2$ , and if p is odd then  $n+1\geq 2$  has already entered the full matrix algebra case, with Cartan matrix [1]; if p=2, the Cartan matrix is  $[2^{n+1}]$ , still  $1\times 1$ . Hence the size of the left-hand side  $C_{n+1}$  is always 1.

#### 5.3 Block Size Constraint

Assume that the recursion equality is defined in the block sense.  $C_n$  is  $r_n \times r_n$ , X is  $r_n \times r_n$ ,  $X^T$  is  $r_n \times r_n$ , and  $\Delta_n$  is  $2r_n \times 2r_n$ . The block matrix (with  $C_n$  at the upper left,

## PDF page 19

X at the upper right, X<sup>T</sup> at the lower left, and C<sup>n</sup> at the lower right) has size 2r<sup>n</sup> × 2rn; after adding ∆<sup>n</sup> of the same size, the right-hand side is still 2r<sup>n</sup> ×2rn. The left-hand side Cn+1 has size rn+1. If the equality holds, one must have

$$r_{n+1} = 2r_n.$$

This is a necessary condition for the equality to hold, and no matrix entries have yet been checked. By 5.2, rn+1 = 1 for all n ≥ 1, while r<sup>n</sup> ≥ 1, so 2r<sup>n</sup> ≥ 2. Hence rn+1 = 2r<sup>n</sup> cannot hold. Checking case by case: if r<sup>n</sup> = 1, the right-hand side has size 2 and the left-hand side has size 1; if r<sup>n</sup> = 2, the right-hand side has size 4 and the left-hand side has size 1. In both cases they are unequal.

#### 5.4 Main Theorem

Theorem 5.1. Let p be any prime and n ≥ 1. There do not exist Cartan matrices Cn, Cn+1 satisfying the above block recursion, together with arbitrary X, ∆n, such that C<sup>n</sup> and Cn+1 are the Cartan matrices of EnvL(An) and EnvL(An+1), respectively, and the recursion equality is defined in the block sense.

Proof. By the classification in Chapter 3, the size of Cn+1 is rn+1 = 1. By the same classification, the size r<sup>n</sup> of C<sup>n</sup> belongs to {1, 2}. If the recursion equality is defined, then the right-hand side has size 2r<sup>n</sup> and the left-hand side has size rn+1. A necessary condition for the equality to hold is rn+1 = 2rn. But rn+1 = 1, while 2r<sup>n</sup> ≥ 2, a contradiction. Therefore no such Cn, Cn+1, X, ∆<sup>n</sup> exist. This completes the proof.

The proof uses only the sizes of the Cartan matrices, not the independence of X, and not the values of ∆n. Therefore, even if X or ∆<sup>n</sup> vary arbitrarily, as long as the block sizes are legitimate, the equality already fails at the size level. If the sizes of X or ∆<sup>n</sup> are not legitimate, then the recursion expression itself is not an equality of matrices of the same size, and is even less valid. Under a change of the complete set of primitive orthogonal idempotents, a Cartan matrix only undergoes simultaneous permutation of rows and columns, and simultaneous permutation does not change the matrix size; hence the conclusion does not depend on the choice of idempotents.

# 5.5 Item-by-Item Check of Boundary Cases

Case one: p is odd, n = 1, and −1 is a square modulo p. Then C<sup>1</sup> = I2, r<sup>1</sup> = 2; C<sup>2</sup> = [1], r<sup>2</sup> = 1. The right-hand side block size is 4 × 4, while the left-hand side is 1 × 1; they are unequal.

Case two: p is odd, n = 1, and −1 is not a square modulo p. Then C<sup>1</sup> = [1], r<sup>1</sup> = 1; C<sup>2</sup> = [1], r<sup>2</sup> = 1. The right-hand side block size is 2 × 2, while the left-hand side is 1 × 1; they are unequal.

Case three: p = 2, n = 1. Then C<sup>1</sup> = [2], r<sup>1</sup> = 1; C<sup>2</sup> = [4], r<sup>2</sup> = 1. The right-hand side block size is 2 × 2, while the left-hand side is 1 × 1; they are unequal.

Case four: n ≥ 2, p arbitrary. Then C<sup>n</sup> is 1 × 1 and Cn+1 is 1 × 1; the right-hand side block size is 2 × 2, while the left-hand side is 1 × 1; they are unequal.

The four cases cover all p and n ≥ 1, with no exception. In particular, p = 2 does not need to be treated separately as a "vacuous case"; the size inequality excludes it directly. The split case n = 1 is the only case with r<sup>n</sup> = 2, where the right-hand side has size 4, a larger discrepancy.

## PDF page 20

#### 5.6 Description of a Finite-Range Exact Verification Algorithm

The following algorithm is used for exact consistency checks for finite n and finite p; it uses no floating-point arithmetic and does not depend on external data sources. Its role is limited to checking the implementation consistency of Cartan matrix sizes in small ranges, and it does not replace the general proof in 5.4.

Step one: construct the integer multiplication table of An. Compute structure constants pair by pair according to the doubling formula, then reduce modulo the target prime p.

Step two: construct the left multiplication matrices L<sup>e</sup><sup>i</sup> , starting from the identity operator and these generators, and maintain a linear basis by Gaussian elimination modulo p, obtaining a matrix representation of EnvL(An).

Step three: compute the Jacobson radical, find a complete set of primitive orthogonal idempotents, and obtain the number r<sup>n</sup> of simple module isomorphism classes; or read r<sup>n</sup> directly from the classification in Chapter 3. The two routes should agree in small ranges.

Step four: for each n ≥ 1, compare rn+1 with 2rn, and record whether they are equal. By 5.2, all records are unequal.

Step five: scope declaration. The algorithm covers only finite n and finite p; the general conclusion is borne by 5.4. The algorithm introduces no random sampling and no external benchmark data; all operations are exact integer or finite-field operations.

#### 5.7 Conclusion, Risks, and Limitations

The conclusion rigorously proved in this chapter is: for every prime p and every n ≥ 1, the Cartan doubling recursion under consideration is impossible at the level of block matrix size. The left-hand side Cn+1 is always 1 × 1, while the right-hand side is at least 2 × 2; simultaneous permutation of rows and columns cannot change the matrix size. This conclusion does not depend on the independence of X, on the concrete values of ∆n, or on the size of n.

A distinction must be made between rigorous proof and finite verification. The proof in 5.4 is rigorous and uses only the classification in Chapter 3 and the necessary condition on matrix sizes. The algorithm in 5.6 provides only a consistency check in finite ranges and does not constitute a general proof. A distinction must be made between "the equality is defined" and "the equality holds": if the sizes of X or ∆<sup>n</sup> do not match, the recursion expression itself is illegitimate; if the sizes match, the size inequality directly excludes the equality. A distinction must be made between the size of a Cartan matrix and the values of Cartan entries: this chapter uses only sizes, not multiplicity values; therefore whether the local-algebra Cartan entry is 2<sup>n</sup> or whether the full matrix algebra Cartan matrix is [1] does not affect the size argument, but these values are provided by the classification in Chapter 3, and the terminology is consistent with Chapter 3.

Potential limitations are as follows. If the recursion is interpreted as "some block embedding of Cn+1" rather than as a matrix equality, then the size argument does not apply; this chapter concerns the block equality. If one allows adjoining zero rows and zero columns to change the size, the resulting matrix is no longer the Cartan matrix under the same idempotent set; a Cartan matrix permits only simultaneous permutation of rows and columns. If one changes the complete set of primitive orthogonal idempotents, the matrix only undergoes simultaneous permutation and its size is unchanged, so the

## PDF page 21

conclusion is unaffected by the choice. Apart from these interpretive boundaries, the conclusion of this chapter holds definitively under the stated definitions.

# 6 Machine Certificates and Finite-Range Verification

#### 6.1 Positioning of the Certificates and General Constraints

This chapter records machine certificates used to check the key steps of Chapters 3–5. All certificates perform only exact integer or modular arithmetic enumeration for finite n and finite p; they use no floating-point arithmetic, do not depend on external data sources, and do not replace general proofs. The general conclusions are borne by the classification theorem of Chapter 3, the basis product closure theorem of Chapter 4, and the exclusion theorem for the Cartan doubling recursion of Chapter 5; the role of the machine certificates is to check the implementation consistency of structure constants, block formulas, centralizers, closure dimensions, and Cartan readings within the certified range.

The certification objects are divided into three classes. The first class is basis product closure, that is, whether the ordered product of standard basis elements is still a signed multiple of some standard basis element and nonzero. The second class is the closure dimension of the left-multiplication envelope algebra, that is, the dimension of the subalgebra generated over F<sup>p</sup> by the identity operator and all left multiplication generators. The third class consists of identities used in the proofs of Chapter 3, including associator values, anticommutator values, doubled block formulas, squares of special generators, and centralizers. Each class of certificates gives the input range, output table, and scope declaration.

#### 6.2 Certificate M5: Basis Product Closure

Certificate M5 certifies the basis product closure proposition of Chapter 4. The input consists of 21 cases with n ≤ 7 and p ∈ {2, 3, 5}. The algorithm is as follows.

Step one: recursively construct the multiplication table of A<sup>n</sup> by integer arithmetic according to the Cayley–Dickson doubling formula. For each pair of basis elements, compute the integer structure constants of the four blocks according to the doubling formula.

Step two: reduce the integer structure constants modulo the target prime p, obtaining the multiplication table over Fp.

Step three: enumerate all ordered basis pairs (e<sup>i</sup> , e<sup>j</sup> ), compute the product, check whether the result is exactly a signed multiple of some standard basis element, and check whether that multiple is nonzero.

Step four: count the number of basis pairs satisfying eie<sup>j</sup> = 0.

The output table passes in all 21 cases: the product of every ordered basis pair is a signed multiple of some standard basis element and is nonzero, and the number of zero basis pairs is always zero. This output is consistent with the theorem of Chapter 4. It

## PDF page 22

should be emphasized that the enumeration range of M5 does not cover all n and all p; the general closure and nonvanishing are given by the inductive proof of Chapter 4.

# 6.3 Certificate M7: Structure of the Left-Multiplication Envelope Algebra

Certificate M7 certifies the closure dimensions and characteristic-dependent side checks in the classification of Chapter 3. The input consists of the eight cases (n, p) equal to (1, 2), (1, 3), (2, 2), (2, 3), (3, 2), (3, 3), (4, 3), (4, 5). The algorithm is as follows.

Step one: construct the standard basis of  $A_n$  and the matrix representations of the left multiplication operators  $L_{e_i}$ .

Step two: starting from the identity operator and these left multiplication generators, repeatedly take products and maintain a linear basis by Gaussian elimination modulo p until the dimension stabilizes; the resulting dimension is the closure dimension of  $\text{Env}_L(A_n)$ .

Step three: in characteristic 2, check commutativity of standard basis elements, check whether the square of  $(1 + e_i)$  is zero, and check uniqueness of nonzero idempotents.

Step four: in odd characteristic, check consistency between the closure dimension and the full endomorphism dimension.

The output table gives closure dimensions 2, 2, 4, 4, 8, 64, 256, 256, corresponding respectively to the eight cases above. This table is consistent with the classification of Chapter 3 case by case. A boundary case must be explicitly explained: the closure dimension 4 of (2,3) corresponds to  $\operatorname{Env}_L(A_2) \cong M_2(\mathbb{F}_p)$ , which is the boundary case n=2; when p is odd and  $n\geq 3$ , one enters the full endomorphism case, whose dimension is the square of  $2^n$ , certified as 64,256,256 in (3,3),(4,3),(4,5), respectively. Therefore the jump between (2,3)=4 and (3,3)=64 is not a certificate gap, but a structural difference between the boundary n=2 and the full endomorphism case  $n\geq 3$ .

# 6.4 Certificate M8: Proof-Payload Identities and a Negative Certificate

Certificate M8 certifies identities used in the proofs of Chapter 3. The input and output are as follows.

First, the associator on basis triples takes values in  $\{0, \pm 2e_m\}$ ; the certification range is  $n \leq 5$ ,  $p \in \{3, 5\}$ , and all pass. This result is used in the argument that the associator vanishes in characteristic 2.

Second, the anticommutator on basis elements takes values in  $\{0, \pm 2e_m\}$ ; the certification range is the same, and all pass. This result is used in the commutativity argument in characteristic 2.

Third, the doubled block formula holds on all tested basis quadruples; the certification range is  $n \leq 3$ , and all pass. This result is used for the block representation of left multiplication operators.

Fourth, the special generator  $Z = L_{(0,1)}$  satisfies that the square of Z equals minus the identity; all pass. This result is used for invertibility of Z.

Fifth, the diagonalization formula for doubled blocks,  $Q_bQ_{b'}$  equals the diagonal block  $(-R_bR_{\bar{b'}}, -L_bL_{\bar{b'}})$ , all pass. This result is used for even words falling into the diagonal

## PDF page 23

part.

Sixth, the centralizer Z(An) equals Fp; by exhaustive centralizer computation, the certification range is n ≤ 3, and all pass. This result serves as a finite-instance check of the centrality fact of Chapter 3.

In addition, a candidate decoupling identity QbZ − ZQ¯<sup>b</sup> equals the diagonal block (0, R<sup>b</sup> − Lb) fails under exact enumeration; its left-hand side is identically zero. This negative certificate is retained in the audit chain to show that this route cannot be used for the induction. The induction in Chapter 3 is completed by the subdirect product dichotomy and the graph argument and does not depend on this decoupling identity. Negative certificates have the same audit status as positive certificates: they record an excluded intermediate step, making the choices in the proof chain traceable.

#### 6.5 Joint Reproduction and Algorithmic Workflow

M5 and M7 are jointly reproduced in a single re-execution of the same self-contained session: one script simultaneously constructs multiplication tables, enumerates basis pairs, constructs left multiplication matrices, maintains linear bases, and regenerates both pass tables. This joint record serves as a reproducible anchor, avoiding version drift between separate scripts. The reproduction process uses no random sampling, no external benchmark data, and all operations are exact integer or finite-field operations.

The algorithmic workflow can be summarized as: construction of structure constants, reduction modulo p, enumeration of basis pairs, construction of left multiplication matrices, maintenance of linear bases, reading of closure dimensions, side checks, and scope declaration. In terms of complexity, enumeration of basis pairs is on the order of the square of the number of basis elements, suitable for full checks when n is small; construction of left multiplication matrices and maintenance of linear bases are finite-dimensional linear algebra operations whose scale is determined by the dimension of An. The above algorithm provides only consistency checks in finite ranges and does not constitute a general proof.

# 6.6 Scope, Boundaries, and Risks

The determinate content of the certificates in this chapter is: within the listed finite ranges of n and p, basis product closure, closure dimensions, block formulas, squares of special generators, centralizers, and Cartan readings are all consistent with the theorems of Chapters 3–5. The certificates do not cover all n and all p; the general conclusions are borne by the proofs in the respective chapters. The centralizer certification of M8 only goes up to n ≤ 3; the general proof of centrality is given by the lemma in Chapter 3. The value (2, 3) = 4 of M7 is the boundary case n = 2 and cannot be directly compared with the full endomorphism dimensions for n ≥ 3; this boundary has been made an independent item in the classification of Chapter 3.

Risks and limitations include: if the standard basis or the complete set of primitive orthogonal idempotents is changed, the numerical representation may change, but the classification conclusions and the sizes of Cartan matrices under simultaneous permutation of rows and columns are unchanged; the certificates do not involve external literature or data sources, and all derivations and verifications are completed within the Cayley– Dickson construction and linear algebra over prime fields; negative certificates only show

## PDF page 24

that a certain candidate route is infeasible and do not constitute a replacement for the general proof of Chapter 3. The conclusion of this chapter is: machine certificates support the payload steps of Chapters 3–5 within finite ranges, and their scope declarations are clearly separated from the boundaries of the general proofs.

# 7 Logical Relation to Existing Work

#### 7.1 Comparison Framework

This chapter does not organize its relation to existing work by literature chronology or by author group, but by three logical levels: the object domain (over which base field and for which algebra), the structural goal (which aspect of the algebra is studied), and the method type (a general framework or a classification theorem). These three levels jointly determine whether a piece of work is compatible with, orthogonal to, or incompatible with the conclusions of this chapter.

# 7.2 Characteristic Theory and Annihilator Studies over the Real Field

Literature verification confirms the actual existence and basic positioning of the comparison objects: the annihilator study of Biss-Dugger-Isaksen was published in Comm. Algebra 36 (2008), and the characteristic theory of Biss-Christensen-Dugger-Isaksen was published in Forum Math. 21 (2009), both working over the real field; the zero-divisor graph framework of Anderson-Livingston is for commutative rings and was published in J. Algebra 217 (1999); Schafer's 1966 monograph established the general framework of multiplication algebras of nonassociative algebras. Based on these verifiable coordinates, this chapter develops the relation according to logical relations rather than citation format.

Biss, Dugger, and Isaksen studied upper bounds for the annihilator dimensions of elements in real Cayley–Dickson algebras in Comm. Algebra 36 (2008); the core conclusion is that in a  $2^n$ -dimensional Cayley–Dickson algebra, the annihilator dimension of any element is at most  $2^n - 4n + 4$ . Biss, Christensen, Dugger, and Isaksen subsequently systematized eigenvalue theory in Forum Math. 21 (2009) to clarify several algebraic properties of Cayley–Dickson algebras. The common premise of these two works is that the base field is the real field  $\mathbb{R}$ , the core tool is real linear algebra of eigenvalues and eigenvectors, and the object of study is the spectral property of a single element or a single operator.

The object of this chapter is the left-multiplication envelope algebra over the finite field  $\mathbb{F}_p$ , the goal is its Wedderburn structural classification (local algebra, full matrix algebra, or a direct product of fields), and the tools are the subdirect product dichotomy, the Skolem-Noether theorem, and centrality. The two differ in object domain ( $\mathbb{R}$  versus  $\mathbb{F}_p$ ), in structural goal (spectral properties versus Wedderburn decomposition), and in method type (real-analytic linear algebra versus finite-field algebraic structure). Therefore, conclusions of real-field characteristic theory cannot be directly transferred to the

## PDF page 25

classification of envelope algebras over Fp; conversely, the classification of this chapter does not assert anything about eigenvalue distributions over the real field. They are parallel structural studies, each valid within its own domain.

A boundary must be made explicit: every nondegenerate quadratic form in at least 3 variables over a finite field is isotropic; this is the standard fact on which this chapter relies at n = 2 to identify A<sup>2</sup> with M2(Fp). Over the real field the quaternion algebra does not split, because its norm form is positive definite; this difference is a property of the field, not a difference in algebraic construction. Therefore, any reasoning that directly analogizes nonsplitness over the real field with splitness over a finite field fails; the classification of this chapter explicitly takes the base field as a parameter.

# 7.3 Commutative-Ring Zero-Divisor Graph Framework and Noncommutative Basis Product Closure

Anderson and Livingston introduced the zero-divisor graph of a commutative ring in J. Algebra 217 (1999): the vertices are nonzero zero divisors, and edges connect distinct vertices whose product is zero. The algebraic premise of this framework is multiplicative commutativity, and the graph-theoretic premise is the existence of zero divisors.

The basis product closure theorem proved in Chapter 4 of this chapter gives a stronger structural fact: in the standard basis of the Cayley–Dickson algebra An, for every prime p and every n ≥ 0, the product of any two basis elements is a signed multiple of some basis element and is nonzero. Therefore the set of zero basis pairs is empty. This means that, even if the definition of a zero-divisor graph is transferred from commutative rings to nonassociative Cayley–Dickson algebras, its vertex set is already empty at the standard basis level; any density statistic supported on zero basis pairs is identically zero.

The relation here is not "this chapter refutes zero-divisor graph theory"—the latter is completely valid for commutative rings—but rather "the applicability conditions of the zero-divisor graph framework are not satisfied on the noncommutative nonassociative Cayley–Dickson basis, and the manner in which they fail is extreme: it is not that zero divisors are rare, but that zero basis pairs do not exist at all". This distinction is necessary to avoid overclaiming. This chapter does not assert that any conclusion of Anderson–Livingston is wrong; what this chapter asserts is that transplanting zerodivisor-graph-style density analysis without conditions to Cayley–Dickson basis products has no object at the data level.

# 7.4 General Framework of Multiplication Algebras and Concrete Classification

In his 1966 monograph, Schafer systematically defined the associative multiplication algebra and the Lie multiplication algebra of a nonassociative algebra, and used multiplication algebras as a tool for studying the structure of nonassociative algebras. This is a general framework: it defines objects and gives basic properties, but does not provide a Wedderburn classification for a specific family of algebras.

The left-multiplication envelope algebra EnvL(An) of this chapter is a specialization of Schafer's associative multiplication algebra to the family of Cayley–Dickson algebras. The contribution of this chapter is not to redefine multiplication algebras, but to complete

## PDF page 26

three concrete tasks within this framework. First, for p = 2, identify A<sup>n</sup> with the group algebra F2[(C2) n ], and give its local structure and Cartan matrix. Second, for odd p, classify case by case in n: n = 1 gives a split or nonsplit quadratic algebra, n = 2 gives M2(Fp) and the left regular representation gives an isomorphism, and n ≥ 3 gives the full endomorphism algebra End(An). Third, on the basis of the above classification, exclude the possibility of a Cartan doubling recursion at the matrix-size level. None of these three tasks is a direct corollary of Schafer's general framework, because the general framework does not contain arithmetic information for a specific base field and a specific doubling tower.

#### 7.5 Positioning at the Methodological Level

The combination of methods in this chapter has three separable features. First, the subdirect product dichotomy: using the simplicity of M<sup>N</sup> (Fp), every subalgebra of M<sup>N</sup> ⊕M<sup>N</sup> with surjective projections is dichotomized into the full direct sum or the graph of an automorphism. Second, the Skolem–Noether and "evaluation at 1" argument: the graph assumption for an automorphism is converted into the form G = Rg−<sup>1</sup> , which then conflicts with L<sup>a</sup> ̸= Ra. Third, the separation of the first step n = 2 → 3 from the general induction: at n = 2, associativity and central simplicity of A<sup>2</sup> are used to obtain span{LaRc} = End(A2); for n ≥ 3, all P-words rather than only quadratic left-multiplication words are used to complete surjectivity of the projections. This combination has not appeared in this form in the existing literature.

The novelty claim should be limited to the structural classification itself and should not be extended to "the first study of multiplication algebras of Cayley–Dickson algebras". Schafer's framework already established multiplication algebras as an object of study; the novelty of this chapter is that it gives a complete Wedderburn classification of the left-multiplication envelope algebra of the doubling tower over finite fields, and thereby excludes a specific form of Cartan recursion. The identification of A<sup>n</sup> with F2[(C2) n ] in characteristic 2 is a direct observation requiring no complicated tools, but it has not been used in the literature as the starting point of a classification; this chapter uses it as the structural basis of the p = 2 branch.

#### 7.6 Boundaries and Risks

The relation of this chapter to existing work is a logical relation, not a priority claim. Real-field characteristic theory, commutative-ring zero-divisor graphs, and the general framework of multiplication algebras of nonassociative algebras are each valid within their own domains; the conclusions of this chapter do not conflict with them, because the object domain, structural goal, or algebraic premise differs. The only place where incompatibility must be made explicit is: applying the density analysis of commutativering zero-divisor graphs directly to Cayley–Dickson basis products has no object under the closure theorem of Chapter 4 of this chapter; analogizing nonsplitness over the real field to finite fields fails under the classification of Chapter 3.

The risk lies in misreading "different frameworks" as "opposing conclusions". This chapter does not assert that the real-field conclusions of Biss et al. have counterparts over Fp, nor does it assert that the graph-theoretic conclusions of Anderson–Livingston have a direct generalization to noncommutative algebras. The risk also lies in overextending

## PDF page 27

"novelty": the classification of this chapter is a concrete completion within a framework, not the creation of the framework itself; the characteristic 2 identification is an elementary observation, not a deep theorem. These qualifications have been explicitly stated in 7.4 and 7.5 and should not be omitted in subsequent citations.

# 8 Conclusion and Boundaries

#### 8.1 Logical Structure of the Conclusions

The core conclusions of the paper consist of three mutually supporting propositions, rather than being given directly by a single computation or a single certificate. The first is the Wedderburn classification of the left-multiplication envelope algebra: in characteristic 2, the Cayley-Dickson algebra is commutative and associative, and the left-multiplication envelope algebra is isomorphic to the algebra itself and is local; in odd characteristic, n = 1 gives a split or nonsplit quadratic algebra, n = 2 gives  $M_2(\mathbb{F}_p)$ , and  $n \geq 3$  gives the full endomorphism algebra  $\operatorname{End}(A_n)$ . The second is standard basis product closure: the product of any two standard basis elements is still a signed multiple of some standard basis element and is nonzero, so the set of zero basis pairs is empty. The third is the exclusion of the Cartan doubling recursion: the block recursion under consideration is impossible at the matrix-size level, for every prime p and every  $n \geq 1$ .

The relation among these three propositions is: the first provides the sizes and structures of Cartan matrices; the second deprives any statistical conclusion with positive-density support on zero basis pairs of its object; the third uses only the size information given by the first and does not depend on the concrete values of cross blocks or correction terms. Each of the three conclusions has an independent proof and does not form a circle.

# 8.2 Three Load-Bearing Facts in the Classification Conclusion

In the classification conclusion, n=2 must be an independent item.  $A_2$  is a four-dimensional associative algebra; the left regular map  $a\mapsto L_a$  gives an isomorphism from the left-multiplication envelope algebra to  $A_2$ , and  $A_2$  is isomorphic to  $M_2(\mathbb{F}_p)$ . Therefore  $\operatorname{Env}_L(A_2)$  is isomorphic to  $M_2(\mathbb{F}_p)$ , of dimension 4. The full endomorphism algebra  $\operatorname{End}(A_2)$  is  $M_4(\mathbb{F}_p)$ , of dimension 16; the two cannot be confused. The dimension jump between n=2 and  $n\geq 3$  comes from a change in algebraic structure, not from a certificate gap.

The Cartan matrix of the full matrix algebra  $M_m(\mathbb{F}_p)$  is the  $1 \times 1$  matrix [1], not the identity matrix  $I_m$ . Reason: a full matrix algebra is semisimple, its unique simple module is the natural module, its unique indecomposable projective module is isomorphic to that simple module, and the Cartan multiplicity is 1. The Cartan matrix of a local algebra is  $[2^n]$  or [1], whose entries are composition multiplicities, not dimensions; treating dimensions as Cartan entries confuses two levels.

The surjectivity of the projections in the general induction for  $n \geq 3$  depends on all even words involving only first-kind doubling generators, not merely quadratic left-multiplication words.  $A_n$  is nonassociative for  $n \geq 3$ , and long words cannot in general

## PDF page 28

be reduced to quadratic words; if only quadratic words are taken, one would incorrectly require the algebra generated by L<sup>a</sup> to be End(An). The first step from n = 2 to n = 3 must be argued separately, using associativity and central simplicity of A<sup>2</sup> to obtain that the algebra spanned by LaR<sup>c</sup> is End(A2). This step cannot be replaced by the general induction hypothesis.

#### 8.3 Cartan Readings and Exclusion of the Recursion

In all cases of odd characteristic with n ≥ 2, the left-multiplication envelope algebra is a full matrix algebra, and the Cartan matrix is [1]. In characteristic 2, the leftmultiplication envelope algebra is a local algebra, and the Cartan matrix is [2<sup>n</sup> ]. In the split case of odd characteristic n = 1, the Cartan matrix is I2; in the nonsplit case it is [1]. Therefore, for every n ≥ 1, the size of the Cartan matrix is at most 2, and the size of Cn+1 is always 1.

If the block recursion under consideration is defined in the block sense, the right-hand side is formed from two copies of C<sup>n</sup> and has size 2r<sup>n</sup> × 2rn, while the left-hand side has size rn+1. By the classification, rn+1 = 1, while 2r<sup>n</sup> is at least 2, so the size equality cannot hold. This exclusion checks no entries of cross blocks or correction terms and does not depend on the independence of cross blocks; it uses only the necessary condition of matrix size. Simultaneous permutation of rows and columns does not change the matrix size, so the conclusion does not depend on the choice of a complete set of primitive orthogonal idempotents.

# 8.4 Division of Labor between Finite-Range Verification and General Proof

Exact enumeration certificates in finite ranges support the consistency of structure constants, block formulas, squares of special generators, centralizers, and closure dimensions within the certified range. These certificates cover small n and small p, not all n and all p. General closure is borne by the inductive proof, general classification by the subdirect product dichotomy and the graph argument, and the exclusion of the recursion by the matrix-size argument. The role of certificates is to check implementation consistency, not to replace proofs; negative certificates record excluded intermediate routes, have the same audit status as positive certificates, but do not constitute a replacement for the general proof.

# 8.5 Boundaries, Risks, and Applicability Conditions

The conclusions that hold definitively are: under the stated definitions, the classification theorem, the basis product closure theorem, and the recursion exclusion theorem all hold. Finite-range certificates provide only finite support. Boundaries that must be distinguished include: n = 2 is an independent boundary case and cannot be merged into the full endomorphism case n ≥ 3; when p = 2, signs degenerate, but existence and nonvanishing still hold; the conclusion that zero basis pairs are empty concerns the statistical population of ordered pairs of standard basis elements, and the zero-divisor problem for general element pairs is not covered by this conclusion (the distinction between the

## PDF page 29

two populations and explicit examples in characteristics 2 and 3 are given in Chapter 4, 4.5); nonassociativity means that long words cannot be reduced to quadratic words, and surjectivity of the projections must use all first-kind even words; a Cartan matrix permits only simultaneous permutation of rows and columns, and if adjoining zero rows and zero columns is allowed, the result is no longer the Cartan matrix under the same idempotent set; the recursion exclusion concerns the block matrix equality, and if the recursion is interpreted as a block embedding rather than an equality, the size argument does not apply.

Potential limitations lie in interpretive boundaries rather than internal contradictions of the proof: the classification conclusion depends on standard facts such as isotropy of nondegenerate quadratic forms over finite fields, the Skolem–Noether theorem, and the structural map for central simple algebras; these facts are used as external standard results in the proof and are not reproved in this chapter. The scope declarations of machine certificates are clearly separated from the boundaries of the general proof; one should not misread finite certification as a general proof, nor misread the general proof as a purely formal derivation requiring no finite checks. Under the above conditions, the conclusions of the paper are self-consistent and consistent with the terminology and logical direction of each chapter.

#### Remark

The translation of this article was done by DeepSeek, and the mathematical modeling and the literature review of this article were assisted by DeepSeek.

# References

- [1] Schafer, Richard D. 1966. An Introduction to Nonassociative Algebras. New York: Academic Press.
- [2] Biss, Daniel K., Daniel Dugger, and Daniel C. Isaksen. 2008. "Large Annihilators in Cayley–Dickson Algebras." Communications in Algebra 36 (2): 632–664.
- [3] Biss, Daniel K., J. Daniel Christensen, Daniel Dugger, and Daniel C. Isaksen. 2009. "Eigentheory of Cayley–Dickson Algebras." Forum Mathematicum 21 (5): 833–851.
- [4] Anderson, David F., and Philip S. Livingston. 1999. "The Zero-Divisor Graph of a Commutative Ring." Journal of Algebra 217 (2): 434–447.
- [5] Kleinfeld, Erwin. 1951. "Alternative Division Rings of Characteristic 2." Proceedings of the National Academy of Sciences 37 (12): 818–820.
- [6] Bruck, Richard H., and Erwin Kleinfeld. 1951. "The Structure of Alternative Division Rings." Proceedings of the National Academy of Sciences 37 (2): 88–90.

## PDF page 30

- [7] Eakin, Paul, and Avinash Sathaye. 1990. "On Automorphisms and Derivations of Cayley–Dickson Algebras." Journal of Algebra 129 (2): 263–278.
- [8] Flaut, Cristina, and Geanina Zaharia. 2022. "Remarks Regarding Computational Aspects in Algebras Obtained by Cayley–Dickson Process and Some of Their Applications." Mathematics 10 (7): 1141.
- [9] Pchelintsev, Sergey V. 2020. "Isotopes of Alternative Algebras of Characteristic Different from 3." Izvestiya: Mathematics 84 (5): 1002–1015.
- [10] Flaut, Cristina, and Remus Boboescu. 2021. "A Twisted Group Algebra Structure for an Algebra Obtained by the Cayley–Dickson Process." arXiv:2103.12805.
- [11] Flaut, Cristina, and Andreea Baias. 2024. "Some Remarks Regarding Special Elements in Algebras Obtained by the Cayley–Dickson Process over Zp." Axioms 13 (6): 351.
- [12] Zhou, C., and Z. Zhou. 2026. The Wedderburn Classification of Left Multiplication Enveloping Algebras of Cayley–Dickson Algebras in Characteristic p, and a Refutation of the Cartan Doubling Recursion (audit-reconstruction draft v3; machine certificates M5, M7, M8). Companion audit note to the present paper.
- [13] Zhou, Changzheng, and Zhou Ziqing. 2026a. Post Constraint Network E: The Observer as a Sub-structure of Constraint Networks—From the Measurement Problem to the Self-Referential Universe. Zenodo. [https://doi.org/10.5281/zenodo.](https://doi.org/10.5281/zenodo.20352585) [20352585](https://doi.org/10.5281/zenodo.20352585).
- [14] Zhou, Changzheng, and Zhou Ziqing. 2026b. Post-Cybernetics E: Recursive Depth of Meta-control—Constraint Network Allocation of Control Rights and Finiteness. Zenodo. <https://doi.org/10.5281/zenodo.20338286>.
- [15] Zhou, Changzheng, and Zhou Ziqing. 2026c. Post Cybernetics F: The Normative Topology of Constraint Networks—Identification of Dominant Structures and the Criterion of Exitable Rights. Zenodo. [https://doi.org/10.5281/zenodo.](https://doi.org/10.5281/zenodo.20339847) [20339847](https://doi.org/10.5281/zenodo.20339847).
- [16] Zhou, Changzheng, and Zhou Ziqing. 2026d. Post Game Theory G: Post Mechanism Design: Engineering of Belief Ecosystems. Zenodo. [https://doi.org/10.](https://doi.org/10.5281/zenodo.19618215) [5281/zenodo.19618215](https://doi.org/10.5281/zenodo.19618215).
- [17] Zhou, Changzheng, and Zhou Ziqing. 2026e. Post Game Theory E: Structurally Evolutionary Equilibrium—A New Solution Concept for Open Games. Zenodo. <https://doi.org/10.5281/zenodo.19602814>.
- [18] Zhou, Changzheng, and Zhou Ziqing. 2026f. Post Fourier G: From Adaptive Atom Library to Cognitive Architecture—Structural Openness of Signal Representation and Its Neural Implementation. Zenodo. <https://doi.org/10.5281/zenodo.19656256>.
- [19] Zhou, Changzheng, and Zhou Ziqing. 2026g. Post Information Theory Paradigm I: Quantum Gravity, Cognitive Topology, and the Holographic Principle of Information. Zenodo. <https://doi.org/10.5281/zenodo.19702294>.

## PDF page 31

- [20] Zhou, Changzheng, and Zhou Ziqing. 2026h. Observer Geometry: Schr¨odinger's Cat and the Many-Worlds Interpretation. Zenodo. [https://doi.org/10.5281/zenodo.](https://doi.org/10.5281/zenodo.18855141) [18855141](https://doi.org/10.5281/zenodo.18855141).
- [21] Zhou, Changzheng, and Zhou Ziqing. 2026i. Post Bayesian K: An Evolvable Cognitive Architecture for Open Environments: Prototype Implementation and Experimental Evaluation of Constraint Network Reconfiguration. Zenodo. [https:](https://doi.org/10.5281/zenodo.19562929) [//doi.org/10.5281/zenodo.19562929](https://doi.org/10.5281/zenodo.19562929).
- [22] Zhou, Changzheng, and Zhou Ziqing. 2026j. Post Bayesian L: A Dual-Mode Cognitive Architecture: Synergistic Mechanisms of Parameter Inference and Structural Revision. Zenodo. <https://doi.org/10.5281/zenodo.19583445>.
- [23] Zhou, Changzheng, and Zhou Ziqing. 2026k. Post Bayesian M: Dynamics of Cognitive Structural Openness and Subjective Phase Transitions. Zenodo. [https://doi.](https://doi.org/10.5281/zenodo.19583507) [org/10.5281/zenodo.19583507](https://doi.org/10.5281/zenodo.19583507).
- [24] Zhou, Changzheng, and Zhou Ziqing. 2026l. Post Monte Carlo I: A Self-Normalized Central Limit Theorem for Quasi-Stationary Adaptive Chains. Zenodo. [https://](https://doi.org/10.5281/zenodo.19755279) [doi.org/10.5281/zenodo.19755279](https://doi.org/10.5281/zenodo.19755279).
- [25] Zhou, Changzheng, and Zhou Ziqing. 2026m. Post Markovian Paradigm 0: How Boundary Structure Evolution of Markov Systems Leads to Essential Non-Ergodicity. Zenodo. <https://doi.org/10.5281/zenodo.19491459>.
- [26] Zhou, Changzheng, and Zhou Ziqing. 2026n. Post Monte Carlo J: Theoretical Boundaries and Open Frontiers of the Post Monte Carlo Paradigm. Zenodo. [https:](https://doi.org/10.5281/zenodo.19763430) [//doi.org/10.5281/zenodo.19763430](https://doi.org/10.5281/zenodo.19763430).
- [27] Zhou, Changzheng, and Zhou Ziqing. 2026o. Post Decentralization I: Theoretical Boundaries and Future of Post Decentralization—From Protocol Evolution to the Digital Polis. Zenodo. <https://doi.org/10.5281/zenodo.19818373>.
- [28] Zhou, Changzheng, and Zhou Ziqing. 2026p. Post Complex Systems K: Failure Boundaries of Constraint Network Theory and the Geometric-Algebraic Unification of Complex Adaptive Systems. Zenodo. [https://doi.org/10.5281/zenodo.](https://doi.org/10.5281/zenodo.19948113) [19948113](https://doi.org/10.5281/zenodo.19948113).
- [29] Zhou, Changzheng, and Zhou Ziqing. 2026q. Observer Geometry I: Morita Equivalence and Classification Theory of Observer Algebras. Zenodo. [https://doi.org/](https://doi.org/10.5281/zenodo.18801446) [10.5281/zenodo.18801446](https://doi.org/10.5281/zenodo.18801446).
- [30] Zhou, Changzheng, and Zhou Ziqing. 2026r. The Ladder of Rules M: Rules Above Rules—An Open Research Programme and Philosophical Reflections. Zenodo. <https://doi.org/10.5281/zenodo.20388555>.
- [31] Zhou, Changzheng, and Zhou Ziqing. 2026s. The Ladder of Depth Structure G: Consensus, Spectral Gaps, and Rule Islands—Joint Algebraic and Topological Criteria for Multi-Agent Systems. Zenodo. <https://doi.org/10.5281/zenodo.20534826>.
- [32] Zhou, Changzheng, and Zhou Ziqing. 2026t. Constraint Network and Anomaly Suppression Series G: Proof Complexity, Automated Theorem Proving, and Rewiring Operators. Zenodo. <https://doi.org/10.5281/zenodo.20565346>.

## PDF page 32

- [33] Zhou, Changzheng, and Zhou Ziqing. 2026u. The Ladder of Constraint S: Constraint Network Theory—A Meta-Mathematical Structure of Interpretive Frameworks and Proof Boundaries. Zenodo. <https://doi.org/10.5281/zenodo.20661441>.
- [34] Zhou, Changzheng, and Zhou Ziqing. 2026v. Constraint Networks and the McKay Conjecture K: From the McKay Conjecture to the Meta-Mathematical Framework of Cayley–Dickson. Zenodo. <https://doi.org/10.5281/zenodo.20687494>.
- [35] Zhou, Changzheng, and Zhou Ziqing. 2026w. AWC Conjecture A: Local-Global Projective Module Conservation and Topological Weight Module Interpretation. Zenodo. <https://doi.org/10.5281/zenodo.20790412>.
- [36] Zhou, Changzheng, and Zhou Ziqing. 2026x. AWC Conjecture B: Projective Module Conservation on p-Local Algebras and Rigid Core Condensation. Zenodo. [https:](https://doi.org/10.5281/zenodo.20794324) [//doi.org/10.5281/zenodo.20794324](https://doi.org/10.5281/zenodo.20794324).
- [37] Zhou, Changzheng, and Zhou Ziqing. 2026y. AWC Conjecture C: Abelian Defect Groups and Projective Module Zero Height Theorem. Zenodo. [https://doi.org/](https://doi.org/10.5281/zenodo.20805397) [10.5281/zenodo.20805397](https://doi.org/10.5281/zenodo.20805397).
- [38] Zhou, Changzheng, and Zhou Ziqing. 2026z. AWC Conjecture D: Local-Global Conservation of p-Modular Algebras under Exceptional Lie Group Actions. Zenodo. <https://doi.org/10.5281/zenodo.20807447>.
- [39] Zhou, Changzheng, and Zhou Ziqing. 2026aa. AWC Conjecture E: Equivalence Law Between Weight Configurations and Module Counts in Constraint Network Blocks. Zenodo. <https://doi.org/10.5281/zenodo.20809548>.
- [40] Zhou, Changzheng, and Zhou Ziqing. 2026ab. AWC Conjecture F: Cartan Matrix Percolation and Representation Type Phase Transitions in Block Algebra Constraint Networks. Zenodo. <https://doi.org/10.5281/zenodo.20810998>.
- [41] Zhou, Changzheng, and Zhou Ziqing. 2026ac. AWC Conjecture G: Local-Global Locking Law of p-Modules Under Exceptional Lie Group Actions. Zenodo. [https:](https://doi.org/10.5281/zenodo.20822629) [//doi.org/10.5281/zenodo.20822629](https://doi.org/10.5281/zenodo.20822629).
- [42] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture K: From Alperin Weights to the Meta-Mathematical Framework of Dade–Brou´e. Zenodo. [https:](https://doi.org/10.5281/zenodo.20838062) [//doi.org/10.5281/zenodo.20838062](https://doi.org/10.5281/zenodo.20838062).
- [43] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture F: Cartan Matrix Percolation and Representation Type Phase Transitions in Block Algebra Constraint Networks. Zenodo. <https://doi.org/10.5281/zenodo.23913738>.
- [44] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture I: Arithmetic Local-Global Conservation on Non-Associative p-Modular Algebras. Zenodo. [https://](https://doi.org/10.5281/zenodo.23916710) [doi.org/10.5281/zenodo.23916710](https://doi.org/10.5281/zenodo.23916710).
- [45] Zhou, Changzheng, and Zhou Ziqing. 2026. AWC Conjecture J: Recursive Structure of High-Dimensional p-Modular Algebras and Projective Information Doubling. Zenodo. <https://doi.org/10.5281/zenodo.23937612>.

## PDF page 33

# Appendix A: Machine Certificate Ledger

#### A.1 Record Format and Audit Rules

Each certificate is recorded according to six elements: tool (computational environment and arithmetic type), command (operational semantics of the self-contained session script), input (list of cases), output (pass table), log (session record), and judgment (which step of which proposition the certificate supports). The ledger follows two rules. First, negative assertions and positive assertions are treated equally: asserting that a quantity is identically zero must be supported by full enumeration, with the same enumeration strength as asserting that a quantity is nonzero. Second, excluded intermediate steps are retained as negative certificates rather than deleted; the ledger records which route is infeasible, why it is infeasible, and which alternative route accomplished the same goal, so that the choices in the proof chain can be traced level by level.

#### A.2 Certificate M5: Standard Basis Product Closure

Tool. Exact integer arithmetic and modular arithmetic; no floating-point arithmetic appears in the evidence chain; integer overflow boundaries are recorded at array accumulation points.

Command. Recursively construct the multiplication table of A<sup>n</sup> over the integers according to the Cayley–Dickson doubling formula; reduce each structure constant modulo the prime in the case list; enumerate all ordered basis pairs; compare each product with signed multiples of standard basis elements and with zero.

Input. n ≤ 7, p ∈ {2, 3, 5}, 21 cases in total.

Output. All pass: the product of every ordered basis pair is a signed multiple of some standard basis element and is nonzero; in all 21 cases the number of zero basis pairs is zero.

Judgment. Supports instances of the basis product closure theorem of Chapter 4 within the certified range; the emptiness of the set of zero basis pairs is a direct corollary of that theorem.

# A.3 Certificate M7: Closure Dimension of the Left-Multiplication Envelope Algebra

Tool. Same as A.2.

Command. Construct the standard basis and left multiplication operator matrices; starting from the identity operator and all left multiplication generators, repeatedly take products and maintain a linear basis by Gaussian elimination modulo p until the dimension stabilizes; in characteristic 2, check commutativity of the standard basis, check whether the square of the identity plus a basis element is zero, and check uniqueness of nonzero idempotents; in odd characteristic, check consistency between the closure dimension and the full endomorphism dimension.

Input. (n, p) equal to (1, 2), (1, 3), (2, 2), (2, 3), (3, 2), (3, 3), (4, 3), (4, 5).

Output. The closure dimensions are 2, 2, 4, 4, 8, 64, 256, 256 in order; all side checks in characteristic 2 and odd characteristic pass.

## PDF page 34

Judgment. Consistent with the classification of Chapter 3 case by case. The boundary must be explicitly stated: the closure dimension 4 of (2,3) corresponds to  $\operatorname{Env}_L(A_2) \cong M_2(\mathbb{F}_p)$ , which is the boundary case n=2; when p is odd and  $n\geq 3$ , one enters the full endomorphism case, whose dimension is the square of  $2^n$ , certified as 64,256,256 in (3,3),(4,3),(4,5), respectively. Therefore the jump between (2,3)=4 and (3,3)=64 is a structural difference between the boundary n=2 and the full endomorphism case  $n\geq 3$ , not a certificate gap.

# A.4 Certificate M8: Proof-Payload Identities and a Negative Certificate

Tool. Same as A.2.

Command. Item-by-item identity checking scripts; each item is evaluated on all basis elements or tuples of basis elements and compared with the declared value.

Input and output. First, the associator on basis triples takes values in  $\{0, \pm 2e_m\}$ ,  $n \leq 5$ ,  $p \in \{3, 5\}$ , pass. Second, the anticommutator on basis elements takes values in  $\{0, \pm 2e_m\}$ , same range, pass. Third, the doubled block formula holds on all tested basis quadruples,  $n \leq 3$ , pass. Fourth, the special generator  $Z = L_{(0,1)}$  satisfies that the square of Z equals minus the identity, pass. Fifth, the diagonalization formula for doubled blocks holds on all tested basis pairs, pass. Sixth, the centralizer equals  $\mathbb{F}_p$ , by exhaustive centralizer computation,  $n \leq 3$ , pass.

Judgment. The fourth and fifth items support the invertibility of the special generator and the step that even words fall into the diagonal part in the graph argument of Chapter 3; the sixth item serves as a finite-instance check of the centrality fact of Chapter 3; the first, second, and third items support the characteristic 2 branch and the doubled block representation.

# A.5 Negative Certificate: A Candidate Decoupling Identity

A candidate decoupling identity asserts that the difference of two specific operators equals a certain diagonal block. Exact enumeration returns that the left-hand side is identically zero on all test inputs, so the identity does not hold. The root cause is improper use of the direction of the conjugation identity; after substituting in the correct direction, the two terms cancel. This negative certificate is retained in the ledger to show that this route cannot be used for the induction; the induction in Chapter 3 is completed by the subdirect product dichotomy and the graph argument and does not depend on this identity. Negative certificates have the same audit status as positive certificates: they record an excluded intermediate step, making the choices in the proof chain traceable.

# A.6 Joint Reproduction and Scope Declaration

M5 and M7 are jointly reproduced in a single re-execution of the same self-contained session: one script simultaneously constructs multiplication tables, enumerates basis pairs, constructs left multiplication matrices, maintains linear bases, and regenerates both pass tables. The joint record serves as a reproducible anchor, avoiding version drift between

## PDF page 35

separate scripts. The reproduction process uses no random sampling, no external benchmark data, and all operations are exact integer or finite-field operations. The reproduction script and session records are not published with the manuscript; the command elements of each certificate have been fully given in operational semantics, and an independent implementation should regenerate the same pass tables; the original script can be requested from the author if needed.

Scope declaration. The above certificates cover only finite n and finite p, and do not constitute a general proof; the general conclusions are borne by the classification theorem of Chapter 3, the basis product closure theorem of Chapter 4, and the recursion exclusion theorem of Chapter 5. The role of the certificates is to check the implementation consistency of structure constants, block formulas, centralizers, closure dimensions, and Cartan readings within the certified range. The centralizer certification only goes up to n ≤ 3; the general proof of centrality is given by the lemma in Chapter 3.

# Appendix B: Registry of Refutation Targets

#### B.1 Function and Rules of the Registry

The strength of a refutation depends on the precision of its target. If a target is only approximately described, the refutation can be avoided by moving the target; if the target is fixed verbatim, the falsification chain can be recomputed line by line. Therefore this appendix registers verbatim and by coordinate every assertion excluded by Chapters 4 and 5, and gives a one-to-one mapping from registered targets to exclusion theorems.

Registration follows two rules. First, every target must be given with a verbatim source sentence and coordinates; slots that cannot be located verbatim remain to be filled and are not filled with paraphrases. Second, target registration is at the sentence level, not the text level; this appendix makes no assertion about other content of the source text.

# B.2 Registered Targets

- T-1. The source sentence asserts that the density of zero basis pairs is 63/256; coordinates to be filled. Excluded by the basis product closure theorem of Chapter 4: there are no zero basis pairs in the standard basis, and this density is identically zero.
- T-2. The source sentence asserts that the density of zero basis pairs is 64/256; coordinates to be filled. Exclusion is the same as above.
- T-3. The source sentence asserts that the count or density of zero basis pairs is 116/240; coordinates to be filled. Exclusion is the same as above.
- T-4. The source sentence asserts that the density of zero basis pairs is 0.248; coordinates to be filled. Exclusion is the same as above.
- T-5. The source sentence asserts that the Cartan matrix satisfies a block recursion: the left-hand side is the next-order Cartan matrix, the right-hand side is the block concatenation of two current-order Cartan matrices plus a correction term, and the cross block is declared independent. The recursion is declared to be a structural recursion on the doubling tower, not a coordinate accident. Excluded by Chapter 5: for every prime p and every n ≥ 1, the left-hand side Cartan matrix has size 1, while the right-hand

## PDF page 36

side is formed from two current-order Cartan matrices and has size at least 2; the block equality is impossible at the matrix-size level. Simultaneous permutation of rows and columns does not change the matrix size, so the exclusion does not depend on the choice of a complete set of primitive orthogonal idempotents, nor does it check any entries of cross blocks or correction terms.

#### B.3 Exclusion Mapping

The exclusion mechanism for T-1 through T-4 is the same: standard basis product closure gives that the product of any two basis elements is a signed multiple of some basis element and is nonzero; therefore the set of zero basis pairs is empty, and any statistic with positive-density support on zero basis pairs is identically zero. This mechanism uses only the closure and nonvanishing of Chapter 4, and no sampling or approximation. According to the distinction between the two statistical populations in Chapter 4, 4.5, the statistical object excluded by this mechanism is ordered pairs of standard basis elements; if the statistical object of the source sentence is actually general element pairs rather than standard basis pairs, then this mechanism does not cover that sentence, and a separate analysis is required.

The exclusion mechanism for T-5 consists of two parts: the classification of Chapter 3 gives that the size of each Cartan matrix is at most 2 and the next-order size is always 1; Cartan matrices are invariant in size under simultaneous permutation of rows and columns. Together these give a size inequality that excludes the block equality. This mechanism does not depend on the independence assumption for cross blocks, nor on the concrete values of correction terms.

# B.4 Scope

This registry fixes five sentences. It makes no assertion about other content of the source text; the exclusion is at the sentence level, not the text level. The coordinate slots of T-1 through T-4 are currently retained as registrations pending activation: activation requires filling in the verbatim source sentences and coordinates and completing a one-to-one check with the exclusion mechanism of Chapter 4; before that, these four registrations are in a pending state and do not constitute completed verbatim refutations. The completed verbatim refutation registration is T-5.

A distinction must be made between the activation status of a registration and the validity status of a theorem. Regardless of whether coordinates are filled in, the emptiness of the set of zero basis pairs holds independently by Theorem 4.1 of Chapter 4, and any statistic with positive-density support on zero basis pairs is identically zero; this set-level conclusion does not depend on any slot of this registry. The exclusion of T-5 likewise does not depend on coordinate slots, because its mathematical content is independently borne by the classification of Chapter 3 and the size argument of Chapter 5.

## PDF page 37

# Appendix C: List of Claims

#### C1 Theorems Proved in This Paper

The classification theorem of Chapter 3: when p = 2, the left-multiplication envelope algebra is isomorphic to A<sup>n</sup> itself and is local; when p is odd and n = 1, it is a split or nonsplit quadratic algebra; when n = 2, it is M2(Fp) and the left regular representation gives an isomorphism; when n ≥ 3, it is the full endomorphism algebra.

The basis product closure theorem of Chapter 4: for every prime p and every n ≥ 0, the product of standard basis elements is still a signed multiple of some standard basis element and is nonzero.

The recursion exclusion theorem of Chapter 5: the Cartan doubling recursion under consideration is impossible at the matrix-size level for every prime p and every n ≥ 1.

The proofs of these three theorems do not use machine input; machine certificates are finite-range implementation consistency checks, not premises of the proofs.

#### C2 Machine Support Statements and Scope

M5 supports instances of the closure theorem of Chapter 4 in the range n ≤ 7, p ∈ {2, 3, 5}. M7 supports the closure dimensions and side checks of the classification of Chapter 3 in the range of the eight listed pairs (n, p). The first through third items of M8 support instances of the characteristic 2 branch and the doubled block representation in finite ranges; the fourth and fifth items of M8 support the payload steps of the graph argument of Chapter 3; the sixth item of M8 supports instances of the centrality fact in the range n ≤ 3. The negative certificate supports the negative assertion that the candidate decoupling route is infeasible.

Honest scope declaration: no certificate reaches n ≥ 5 or p ≥ 7. This boundary is declared, not concealed. Certificates are endorsements within finite ranges, not general proofs, and not gaps in the proof.

#### C3 External Standard Facts Cited

First, every nondegenerate quadratic form in at least 3 variables over a finite field is isotropic; this is a standard corollary of the Chevalley–Warning theorem, used in the n = 2 branch of Chapter 3.

Second, the Skolem–Noether theorem: every automorphism of a central simple algebra is inner; used in the graph argument of Chapter 3.

Third, the natural structural map of a central simple algebra from the tensor product to the endomorphism algebra is an isomorphism; used in the first step from n = 2 to n = 3 in Chapter 3.

Fourth, the general framework of the associative multiplication algebra of a nonassociative algebra is given in Schafer's 1966 monograph; the left-multiplication envelope algebra of this paper is a specialization of this framework to the family of Cayley–Dickson algebras.

Fifth, the study of annihilators and characteristic theory of real Cayley–Dickson algebras is given in the work of Biss–Dugger–Isaksen (2008) and Biss–Christensen–Dugger–

## PDF page 38

Isaksen (2009); their object domain is the real field, different from the finite-field object domain of this paper.

Sixth, the zero-divisor graph framework for commutative rings is given in the work of Anderson–Livingston (1999); its algebraic premise is multiplicative commutativity, different from the noncommutative nonassociative structure of Cayley–Dickson algebras.

The above facts are used only as external standard results and are not reproved in this paper.

# C4 Non-Claims

This paper makes no assertion about the Alperin weight conjecture, the Brauer heightzero conjecture, the Dade conjecture, or the Brou´e conjecture; these names do not appear in this paper as declared claims. This paper does not assert that conclusions of the characteristic theory of real Cayley–Dickson algebras have counterparts over finite fields; this paper does not assert that conclusions of commutative-ring zero-divisor graphs have a direct generalization to noncommutative algebras; this paper does not assert the novelty of the general multiplication algebra framework itself. The classification of this paper is a concrete completion within the framework, and the characteristic 2 identification is an elementary observation, not a deep theorem. These qualifications have been explicitly stated in the corresponding places of the main text and should not be omitted in subsequent citations.
