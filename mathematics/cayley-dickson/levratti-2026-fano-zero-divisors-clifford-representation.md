Source: https://zenodo.org/records/20445208/files/A%20CLIFFORD%20REPRESENTATION%20OF%20THE%20FANO%20ZERO-DIVISORS_v1.pdf
PDF sha256: ad1fcadd82fcd3b3b3924d8f06a440c525e7bd8eed9a4ab4128b748546b368d5
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of levratti-2026-fano-zero-divisors-clifford-representation.pdf

Transcription of `levratti-2026-fano-zero-divisors-clifford-representation.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

Image check: pages 2-4 were compared against their rendered page images; pages 2-4 were rewritten from the image, with figure contents described in brackets and every change named in a transcriber's note on its page.

## PDF page 1

### A CLIFFORD REPRESENTATION OF THE FANO ZERO-DIVISORS

#### GIOVANNI LEVRATTI

ABSTRACT. We construct an explicit map  $\rho: \mathrm{ZD}^*(4) \to \mathrm{Cliff}(0,7)$  from the 84 active zero-divisors of the sedenion algebra  $A_4$  into the Clifford algebra  $\mathrm{Cliff}(0,7) \cong M_8(\mathbb{R})$ ; see [7] for the general theory of Clifford algebras. The map is defined by  $\rho(e_p + \sigma e_{8+k}) := L_{e_p}^{\mathcal{O}}$ , where  $L_{e_p}^{\mathcal{O}}$  denotes left-multiplication by  $e_p$  in the octonions  $\mathcal{O} = A_3$ . We prove three exact properties: (i)  $\mathrm{GL}(3, \mathbb{F}_2)$ -equivariance; (ii) anti-commutation  $\{\rho(A), \rho(B)\} = 0$  for every ZD pair, via the distinct  $\varepsilon$ -index theorem (proved algebraically); and (iii) the Fano reflection identity  $\rho(e_p)\rho(e_r)\rho(e_t) = \varepsilon_{p,r,t} R_{\{0,p,r,t\}}$  for every Fano line  $\{p,r,t\}$ . A remark records the precise relation between these results and a naïve "Cliff(8), Pauli-weight-4" formulation originally proposed. All results are verified computationally for n=4,5,6,7.

#### Contents

| 1. Introduction                                | ] |  |
|------------------------------------------------|---|--|
| Notation                                       | 2 |  |
| 2. Structural Preliminaries                    | 2 |  |
| 2.1. Active zero-divisors                      | 2 |  |
| 2.2. The distinct $\varepsilon$ -index theorem | 2 |  |
| 3. The Clifford Generators                     | 3 |  |
| 4. The Representation                          | 3 |  |
| 5. Main Theorems                               | 3 |  |
| 5.1. Anti-commutation                          | 3 |  |
| 5.2. $GL(3, \mathbb{F}_2)$ -equivariance       | 3 |  |
| 5.3. Fano reflection identity                  | 4 |  |
| 6. Comparison with the Original Desiderata     | 5 |  |
| 6.1. Connection to Paper 5 stabilizer codes    | 5 |  |
| 7. Discussion                                  | 7 |  |
| 7.1. Geometric meaning of the Fano reflection  | 7 |  |
| 7.2. Connection to the sign-parity framework   | 7 |  |
| 7.3. Verified extension to $n \leq 7$          | 7 |  |
| Appendix A. Numerical Verification             | 7 |  |
| Acknowledgements                               | 8 |  |
| References                                     |   |  |

### 1. Introduction

The Sign-Parity Classification [1] established that every ZD pair  $(A, B) \in \text{ZD}(4)$  has the form  $A = e_p + \sigma e_{8+k}$ ,  $B = e_r + \tau e_{8+l}$  with indices satisfying the Fano-plane incidence structure. The present paper asks whether this combinatorial structure can be encoded as an algebraic representation in a Clifford algebra.

Date: May 29, 2026.

<sup>2020</sup> Mathematics Subject Classification. 17A35, 15A66, 05B25, 81P10.

Key words and phrases. Cayley–Dickson algebras, zero-divisors, octonions, Clifford algebras, Fano plane,  $GL(3, \mathbb{F}_2)$ .

## PDF page 2

The answer is yes, and the construction is unexpectedly clean: it uses nothing beyond the octonion left-multiplication operators L O ek , which are the standard generators of Cliff(0, 7).

Notation. We write $A_n$ for the Cayley–Dickson algebra of dimension $2^n$ over $\mathbb{R}$, with $A_3 = \mathcal{O}$ (octonions) and $A_4 = \mathbb{S}$ (sedenions). Basis elements are $e_0 = 1, e_1, \dots, e_{2^n-1}$, with

$$e_i \cdot e_j = \varepsilon_{ij} \, e_{i \oplus j}, \quad \varepsilon_{ij} \in \{+1, -1\},$$

where ⊕ denotes bitwise XOR; see [\[6\]](#page-7-4) for the general theory of non-associative algebras. The Fano plane PG(2, $\mathbb{F}_2$) is identified with $\mathbb{F}_2^3 \setminus \{0\} = \{1, \dots, 7\}$; its seven lines are $\{p, r, t\}$ with $p \oplus r \oplus t = 0$.

The ε-index of an active element $A = e_p + \sigma e_{8+k}$ is $p \in \{1, \dots, 7\}$, i.e. the index of its octonion component.

# 2. Structural Preliminaries

# 2.1. Active zero-divisors.

Definition 2.1. An element $A \in A_4$ is active if $A = e_p + \sigma e_{8+k}$ for some $p \in \{1, \dots, 7\}$, $k \in \{1, \dots, 7\}$, $\sigma \in \{+1, -1\}$, and there exists $B \neq 0$ with $AB = 0$. Write $\mathrm{ZD}^*(4)$ for the set of active elements.

From [\[1\]](#page-7-3): $|\mathrm{ZD}^*(4)| = 84$ and $|\mathrm{ZD}(4)| = 336$ ordered ZD pairs.

2.2. The distinct ε-index theorem. The following theorem is the structural core of the construction.

Theorem 2.2 (Distinct ε-indices). Let $(A, B) \in \mathrm{ZD}(n)$ with $A = e_p + \sigma_A e_{N+k}$ and $B = e_r + \sigma_B e_{N+l}$, where $N = 2^{n-1}$. Then $p \neq r$. Moreover, every ordered pair $(p, r)$ with $p \neq r$ and $p, r \in \{1, \dots, N-1\}$ arises as the ε-indices of some ZD pair.

Proof. We prove both assertions algebraically.

Distinct ε-indices. Suppose for contradiction that p = r.

Step 1 (XOR forces k = l). By the {0, 4, 8} Trichotomy([\[1\]](#page-7-3), Theorem 3.6, Case B), A · B = 0 requires

$$p \oplus (N+k) \oplus r \oplus (N+l) = 0.$$

Since $(N + k) \oplus (N + l) = k \oplus l$ (the leading bits $2^{n-1}$ cancel), this gives $p \oplus r = k \oplus l$. With $p = r$: $k \oplus l = 0$, hence $k = l$.

Step 2 (Direct product). With $p = r$ and $k = l$, using $e_p^2 = e_{N+k}^2 = -e_0$ and anticommutativity $\varepsilon_{N+k,p} = -\varepsilon_{p,N+k}$:

$$A \cdot B = e_p^2 + \sigma_B \,\varepsilon_{p,N+k} \,e_{p \oplus (N+k)} + \sigma_A \,\varepsilon_{N+k,p} \,e_{p \oplus (N+k)} + \sigma_A \sigma_B \,e_{N+k}^2$$
$$= -(1 + \sigma_A \sigma_B) \,e_0 + (\sigma_B - \sigma_A) \,\varepsilon_{p,N+k} \,e_{p \oplus (N+k)}.$$

Step 3 (Contradiction). For A · B = 0 both coefficients must vanish:

- $e_0$ coefficient: $1 + \sigma_A \sigma_B = 0 \Rightarrow \sigma_A \sigma_B = -1 \Rightarrow \sigma_A \neq \sigma_B$.
- $e_{p \oplus (N+k)}$ coefficient: $(\sigma_B - \sigma_A)\, \varepsilon_{p,N+k} = 0$. Since $\varepsilon_{p,N+k} \neq 0$: $\sigma_B = \sigma_A$.

These two conditions contradict each other, so $A \cdot B \neq 0$ whenever $p = r$.

All 42 pairs appear. Given any ordered pair (p, r) with p ≠ r and p, r ∈ {1, . . . , 7}, set t := p ⊕ r ∈ {1, . . . , 7} (nonzero since p ≠ r). By the {0, 4, 8} Trichotomy, any ZD pair with ε-indices (p, r) satisfies k ⊕ l = t; pick any k ∈ {1, . . . , 7} with k ≠ t and set l := k ⊕ t ∈ {1, . . . , 7}. By the Sign-Parity Criterion([\[1\]](#page-7-3), Theorem 7.16), among the four (σA, σB) ∈ {+1, −1} 2 choices for the flat {p, N + k, r, N + l}, at least one

<!-- Transcriber's note: page rewritten from the page image. The machine reading set the subscripts of $A_n$, $e_p$, $e_{8+k}$, $e_{N+k}$, $\sigma_A$, $\sigma_B$ and $\mathrm{ZD}^*(4)$ as superscripts or ran them into the text, wrote $2^{n-1}$ as `2<sup>n</sup>−<sup>1</sup>` and $e_p^2$ as `e 2 <sup>p</sup>`; those sentences are set in mathematics as printed, and every not-equal sign is $\neq$. -->

## PDF page 3

has sign-parity +1, yielding a ZD pair  $(e_p + \sigma_A e_{N+k}, e_r + \sigma_B e_{N+l})$  with  $\varepsilon$ -indices exactly (p, r).

Remark 2.3. The map  $A \mapsto \varepsilon(A) = p$  separates every ZD pair: ZD adjacency implies  $\varepsilon(A) \neq \varepsilon(B)$ .

#### 3. The Clifford Generators

The octonion left-multiplication operators are defined by

$$L_{e_k}^{\mathcal{O}} \colon \mathcal{O} \to \mathcal{O}, \quad x \mapsto e_k \cdot x.$$

As  $8 \times 8$  real matrices they satisfy  $\{L_{e_i}^{\mathcal{O}}, L_{e_j}^{\mathcal{O}}\} = -2\delta_{ij}I_8$  for all  $i, j \in \{1, \dots, 7\}$ , making them the seven generators of  $\text{Cliff}(0,7) \cong M_8(\mathbb{R})$ ; see [7] for the general theory of Clifford algebras.

**Lemma 3.1.** For every  $i, j \in \{1, ..., 7\}$  with  $i \neq j$ :  $L_{e_i}^{\mathcal{O}} L_{e_j}^{\mathcal{O}} + L_{e_j}^{\mathcal{O}} L_{e_i}^{\mathcal{O}} = 0$ .

*Proof.* Immediate from $\{L_{e_i}, L_{e_j}\} = -2\delta_{ij}I_8$. $\square$

Remark 3.2 (Non-associativity warning). Because the octonions are not associative,  $L_{e_i}^{\mathcal{O}} \circ L_{e_j}^{\mathcal{O}} \neq L_{e_i \cdot e_j}^{\mathcal{O}}$  in general as matrix composition. The product  $L_i L_j$  is a Clifford bivector of grade 2, not a grade-1 generator.

#### 4. The Representation

**Definition 4.1.** Define  $\rho: \mathrm{ZD}^*(4) \to \mathrm{Cliff}(0,7) = M_8(\mathbb{R})$  by

$$\rho(e_p + \sigma e_{8+k}) := L_{e_p}^{\mathcal{O}}.$$

Remark 4.2. The map depends only on the  $\varepsilon$ -index p: it is constant on each of the 7 fibers  $\{A \in \mathrm{ZD}^*(4) : \varepsilon(A) = p\}.$ 

### 5. Main Theorems

### 5.1. Anti-commutation.

**Theorem 5.1** (Anti-commutation). For every ZD pair  $(A, B) \in ZD(4)$ :

$$\{\rho(A), \, \rho(B)\} = 0.$$

*Proof.* Let  $A = e_p + \sigma e_{8+k}$  and  $B = e_r + \tau e_{8+l}$ . By Theorem 2.2,  $p \neq r$ . Therefore

$$\{\rho(A), \rho(B)\} = \{L_{e_p}^{\mathcal{O}}, L_{e_r}^{\mathcal{O}}\} = -2\delta_{pr} I_8 = 0.$$

### 5.2. $GL(3, \mathbb{F}_2)$ -equivariance.

**Theorem 5.2** (GL(3,  $\mathbb{F}_2$ )-equivariance). For every  $g \in GL(3, \mathbb{F}_2)$  acting on  $\{1, \ldots, 7\} = \mathbb{F}_2^3 \setminus \{0\}$ :

$$\rho(g \cdot A) = g \cdot \rho(A),$$

where the right-hand action permutes the generators  $\{L_{e_1}, \ldots, L_{e_7}\}$  by index.

Proof. The  $\varepsilon$ -index satisfies  $\varepsilon(g \cdot A) = g(\varepsilon(A))$  since g acts on the octonion component. Since  $GL(3, \mathbb{F}_2) \cong PSL(2,7)$  is a subgroup of  $G_2 = Aut(\mathcal{O})$  (see [5], §4.1), every  $g \in GL(3, \mathbb{F}_2)$  acts on  $\{e_1, \ldots, e_7\}$  as an octonion automorphism. The induced map  $\varphi(g) \colon L_{e_i} \mapsto L_{e_{g(i)}}$  satisfies  $\{L_{e_{g(i)}}, L_{e_{g(j)}}\} = -2\delta_{g(i),g(j)}I_8 = -2\delta_{ij}I_8$ , hence is an automorphism of Cliff(0,7). The automorphism group  $GL(3,\mathbb{F}_2) \cong PSL(2,7)$  and its action on the Fano geometry are studied in detail in [2].

<!-- Transcriber's note: page rewritten from the page image. In Lemma 3.1 and Remark 3.2 the machine reading wrote $e_i$ where the page prints $e_j$; the formula of the proof of Lemma 3.1 is inline as printed. -->

## PDF page 4

### 5.3. Fano reflection identity.

**Definition 5.3.** For a Fano line  $\{p, r, t\}$  (with  $p \oplus r \oplus t = 0$ ), the Fano 4-flat is  $F = \{0, p, r, t\} \subset \{0, \dots, 7\}$ . The Fano reflection is

$$R_F := 2P_F - I_8 = \operatorname{diag}(\chi_F(j))_{j=0}^7, \quad \chi_F(j) = \begin{cases} +1 & j \in F, \\ -1 & j \notin F. \end{cases}$$

Note  $R_F^2 = I_8$  (involution).

We need two preparatory lemmas.

**Lemma 5.4** ( $\varepsilon$ -identity). For every Fano line  $\{p, r, t\}$ :  $\varepsilon_{p, r, t} := \text{sign}(e_p \cdot (e_r \cdot e_t)) = -\varepsilon_{rt}$ .

Proof. Since  $r \oplus t = p$ :  $e_r \cdot e_t = \varepsilon_{rt} \cdot e_p$ . Hence  $e_p \cdot (e_r \cdot e_t) = \varepsilon_{rt} \cdot (e_p \cdot e_p) = \varepsilon_{rt} \cdot (-1) = -\varepsilon_{rt}$ .  $\square$ 

**Lemma 5.5** (Line sign consistency). For every Fano line  $\{p, r, t\}$ , let  $\alpha := \varepsilon_{rt}$ . Then  $\varepsilon_{pr} = \varepsilon_{tp} = \alpha$ .

Proof. WRAP(p, r) with  $p \oplus r = t$ :  $\varepsilon_{pr} \cdot \varepsilon_{t,r} = -1$ . Since  $\varepsilon_{t,r} = -\varepsilon_{rt} = -\alpha$ :  $\varepsilon_{pr}(-\alpha) = -1$ , so  $\varepsilon_{pr} = \alpha$ . WRAP(r, p) with  $r \oplus p = t$ :  $\varepsilon_{rp} \cdot \varepsilon_{t,p} = -1$ . Since  $\varepsilon_{rp} = -\varepsilon_{pr} = -\alpha$ :  $(-\alpha)\varepsilon_{tp} = -1$ , so  $\varepsilon_{tp} = \alpha$ .

**Theorem 5.6** (Fano Reflection Identity). For every Fano line  $\{p, r, t\}$ :

$$L_{e_p}^{\mathcal{O}} \, L_{e_r}^{\mathcal{O}} \, L_{e_t}^{\mathcal{O}} \; = \; \varepsilon_{p,r,t} \, R_F \; = \; -\varepsilon_{rt} \, R_F,$$

where  $F = \{0, p, r, t\}$ .

*Proof.* Set  $\alpha := \varepsilon_{rt}$ , so  $\varepsilon_{p,r,t} = -\alpha$  (Lemma 5.4).

**Step 1 (Diagonal form).** Since  $p \oplus r \oplus t = 0$ , the operator  $G := L_{e_p} L_{e_r} L_{e_t}$  acts on each basis vector  $e_j$  as  $e_p \cdot (e_r \cdot (e_t \cdot e_j)) = \lambda_j e_j$ , where

$$\lambda_j = \varepsilon_{tj} \, \varepsilon_{r,\, t \oplus j} \, \varepsilon_{p,\, r \oplus t \oplus j}.$$

Hence G is diagonal.

Step 2 ( $j \in F$ , four sub-cases). Write  $\alpha = \varepsilon_{pr} = \varepsilon_{tp} = \varepsilon_{rt}$  (Lemma 5.5). We show  $\lambda_j = -\alpha$  for each  $j \in \{0, p, r, t\}$ .

- j = 0:  $\lambda_0 = \varepsilon_{t,0} \cdot \varepsilon_{r,t} \cdot \varepsilon_{p,p} = 1 \cdot \alpha \cdot (-1) = -\alpha . \checkmark$
- j = p:  $t \oplus p = r$  and  $r \oplus t \oplus p = 0$  (Fano), so  $\lambda_p = \varepsilon_{tp} \cdot \varepsilon_{r,r} \cdot \varepsilon_{p,0} = \alpha \cdot (-1) \cdot 1 = -\alpha . \checkmark$
- j = r:  $t \oplus r = p$  and  $r \oplus t \oplus r = t$  (Fano), so  $\lambda_r = \varepsilon_{tr} \cdot \varepsilon_{r,p} \cdot \varepsilon_{p,t}$ . Now  $\varepsilon_{tr} = -\alpha$ ,  $\varepsilon_{rp} = -\alpha$  (anti-commutativity), and WRAP(p, t) with  $p \oplus t = r$  gives  $\varepsilon_{pt} \cdot \varepsilon_{rt} = -1$ , so  $\varepsilon_{pt} = -\alpha$ . Hence  $\lambda_r = (-\alpha)(-\alpha)(-\alpha) = -\alpha^3 = -\alpha$ .
- j = t:  $t \oplus t = 0$  and  $r \oplus t \oplus t = r$ , so  $\lambda_t = \varepsilon_{tt} \cdot \varepsilon_{r,0} \cdot \varepsilon_{p,r} = (-1) \cdot 1 \cdot \alpha = -\alpha.$

Thus  $\lambda_i = -\alpha = \varepsilon_{p,r,t}$  for all  $j \in F$ .

Step 3 (Lo-flat:  $j \notin F$ ). For  $j \in \{1, ..., 7\} \setminus \{p, r, t\}$ , the indices j, p, r, t are all distinct and all lie in  $\{1, ..., 7\}$ , so  $L_j$  anti-commutes with each of  $L_p, L_r, L_t$ :

$$L_j G = L_j L_p L_r L_t = (-L_p L_j) L_r L_t = L_p L_r L_j L_t = -L_p L_r L_t L_j = -G L_j.$$

Hence  $\{L_j, G\} = 0$ . Since  $G = \operatorname{diag}(\lambda_0, \dots, \lambda_7)$ , this gives  $\lambda_{j \oplus l} = -\lambda_l$  for every l. Setting l = 0:  $\lambda_i = -\lambda_0 = -(-\alpha) = \alpha = -\varepsilon_{p,r,t}$ .

**Conclusion.** G has eigenvalue  $-\alpha = \varepsilon_{p,r,t}$  on span(F) and eigenvalue  $+\alpha = -\varepsilon_{p,r,t}$  on the lo-flat, so  $G = \varepsilon_{p,r,t} R_F$ .

Corollary 5.7.  $\Gamma_{prt} := L_{e_p} L_{e_r} L_{e_t}$  is an involution:  $\Gamma_{prt}^2 = I_8$ .

*Proof.* $\Gamma_{prt}^2 = \varepsilon_{p,r,t}^2 R_F^2 = I_8$. $\square$

<!-- Transcriber's note: page compared with the page image. The formula of the proof of Corollary 5.7 is inline as printed; the rest matches the image. -->

## PDF page 5

### 6. Comparison with the Original Desiderata

Remark 6.1 (Comparison with the Cliff(8) formulation). The construction was originally framed as a map  $\rho$ : ZD\*(4)  $\rightarrow$  Cliff(8) =  $M_{16}(\mathbb{R})$  satisfying four properties: (a) GL(3,  $\mathbb{F}_2$ )-equivariance, (b) "Pauli weight = 4", (c)  $\{\rho(A), \rho(B)\} = 0$  for ZD pairs, and (d)  $\rho(e_A)\rho(e_B)\rho(e_C) = -I_{16}$  for covering triples. The construction above differs in the following exact ways.

Target algebra. Our  $\rho$  maps into  $\text{Cliff}(0,7) = M_8(\mathbb{R})$  (7 generators). The proposed  $\text{Cliff}(8) = M_{16}(\mathbb{R})$  (8 generators) admits a natural embedding  $M_8 \hookrightarrow M_{16}$  via  $M \mapsto M \otimes I_2$ , but this adds no structure relevant to the zero-divisor problem. Cliff(0,7) is the correct and minimal target.

Pauli weight. In Cliff(0,7) acting on  $(\mathbb{R}^2)^{\otimes 3}$  (3 qubits), the generators  $L_{e_k}$  have Pauli-decomposition weight at most 3. The condition "weight = 4" was predicated on a 4-qubit target and is not a natural invariant of the zero-divisor structure.

Triple product identity. The property  $\rho(e_A)\rho(e_B)\rho(e_C) = -I_{16}$  was overly strong. The correct identity (Theorem 5.6) gives  $\Gamma_{prt} = \varepsilon_{p,r,t} R_F$ , a Fano reflection, not a scalar multiple of the identity. Since  $\pi_A \pi_B \pi_C = -1$  for every 2-flat ([1], Theorem 7.18), this encodes exactly the sign constraint of the Sign-Parity framework.

The exact properties of  $\rho$  are summarised in Table 1.

|     | Property         | Original formulation                       | Exact result                                              |
|-----|------------------|--------------------------------------------|-----------------------------------------------------------|
| (1) | Equivariance     | $\mathrm{GL}(3,\mathbb{F}_2)$ -equivariant | proved (same)                                             |
| (2) | Triple product   | $=-I_{16}$                                 | $= \varepsilon_{prt} R_F$ (Fano reflection)               |
| (3) | Anti-commutation | $\{\rho(A), \rho(B)\} = 0$ for ZD pairs    | proved (same)                                             |
| (4) | Pauli weight     | =4  in Cliff(8)                            | $\mathbf{dropped} \; (\mathrm{wrong} \; \mathrm{target})$ |

Table 1. Original desiderata vs. exact results.

# 6.1. Connection to Paper 5 stabilizer codes.

Remark 6.2 (Pauli decomposition and Fano duality). Pauli decomposition. Each  $L_{e_k}^{\mathcal{O}} \in M_8(\mathbb{R})$ , viewed as an operator on 3 qubits (dim =  $2^3 = 8$ ), decomposes as

$$L_{e_k}^{\mathcal{O}} = \frac{-i}{2} \sum_{j=1}^{4} s_j^{(k)} P_j^{(k)}, \quad s_j^{(k)} \in \{+1, -1\},$$

with all four coefficients of equal magnitude  $\frac{1}{2}$ . This is forced by the Frobenius identity  $\|L_{e_k}^{\mathcal{O}}\|_F^2 = 8$  (since  $L_{e_k}^{\mathcal{O}}$  is an isometry of  $\mathbb{R}^8$ , hence orthogonal:  $(L_{e_k}^{\mathcal{O}})^{\mathsf{T}} L_{e_k}^{\mathcal{O}} = I_8$ , giving  $\mathrm{Tr}(I_8) = 8$ ), which requires  $\sum_P |c_{k,P}|^2 = 1 = 4 \cdot \frac{1}{4}$ .

## PDF page 6

The explicit decompositions are

$$\begin{split} L_{e_1}^{\mathcal{O}} &= \tfrac{-i}{2} \big( \mathtt{IIY} + \mathtt{IZY} + \mathtt{ZIY} - \mathtt{ZZY} \big), \\ L_{e_2}^{\mathcal{O}} &= \tfrac{-i}{2} \big( \mathtt{IYI} + \mathtt{IYZ} - \mathtt{ZYI} + \mathtt{ZYZ} \big), \\ L_{e_3}^{\mathcal{O}} &= \tfrac{-i}{2} \big( \mathtt{IXY} + \mathtt{IYX} - \mathtt{ZXY} + \mathtt{ZYX} \big), \\ L_{e_4}^{\mathcal{O}} &= \tfrac{-i}{2} \big( -\mathtt{YII} + \mathtt{YIZ} + \mathtt{YZI} + \mathtt{YZZ} \big), \\ L_{e_5}^{\mathcal{O}} &= \tfrac{-i}{2} \big( -\mathtt{XIY} + \mathtt{XZY} + \mathtt{YIX} + \mathtt{YZX} \big), \\ L_{e_6}^{\mathcal{O}} &= \tfrac{-i}{2} \big( \mathtt{XYI} - \mathtt{XYZ} + \mathtt{YXI} + \mathtt{YXZ} \big), \\ L_{e_7}^{\mathcal{O}} &= \tfrac{-i}{2} \big( \mathtt{XXY} - \mathtt{XYX} + \mathtt{YXX} - \mathtt{YYY} \big). \end{split}$$

The X-part encodes the Fano points. For every  $k \in \{1, ..., 7\}$ , all four Pauli strings in the decomposition of  $L_{e_k}^{\mathcal{O}}$  share the same X-part (positions where X or Y appears), and this X-part equals the binary representation of k in  $\mathbb{F}_2^3$ :

$$\mathrm{x\text{-}part}\big(L_{e_k}^{\mathcal{O}}\big) \ = \ \mathrm{bin}(k) \ \in \ \mathbb{F}_2^3 \setminus \{0\}.$$

This gives a canonical bijection  $e_k \leftrightarrow \text{bin}(k)$  between the 7 octonion generators and the 7 points of  $PG(2, \mathbb{F}_2)$ .

The 8 anti-commuting single-Pauli selections. An exhaustive search over all  $4^7 = 16\,384$  ways of selecting one Pauli string per generator from its four components shows that exactly 8 selections satisfy  $\{\tilde{\rho}(e_i), \tilde{\rho}(e_j)\} = 0$  for all 21 pairs  $i \neq j$ . These 8 selections share the same fixed X-parts and differ only in which Z-correction is chosen from the 4-element coset  $\{I, Z\}^{\otimes 3}$ .

**Triple products and Fano duality.** For every one of the 8 valid selections, and for every Fano line  $\{p, r, t\}$ , the triple product equals

$$\tilde{\rho}(e_p)\,\tilde{\rho}(e_r)\,\tilde{\rho}(e_t) = \phi_{p,r,t}\cdot Q_{\{p,r,t\}}, \qquad \phi_{p,r,t}\in\{+i,-i\},$$

where  $Q_{\{p,r,t\}} \in \{I,Z\}^{\otimes 3}$  is a specific non-identity Z-type Pauli string, the same for all 8 selections. The assignment  $\{p,r,t\} \mapsto Q_{\{p,r,t\}}$  is a bijection from the 7 Fano lines to the 7 nonzero elements of  $\{I,Z\}^{\otimes 3} \cong \mathbb{F}_2^3 \setminus \{0\}$ , and coincides with the *projective duality* of  $PG(2,\mathbb{F}_2)$ : the dual (in the combinatorial sense) of each Fano line.

The twisted group algebra is the octonions. Define the cocycle  $c_{\text{oct}}(\text{bin}(i), \text{bin}(j)) := \varepsilon_{ij}$  (the octonion sign table of [1]). The twisted group algebra  $\mathbb{C}[(\mathbb{Z}/2)^3]^{c_{\text{oct}}}$  with multiplication  $u_{\alpha} \cdot u_{\beta} = c_{\text{oct}}(\alpha, \beta) u_{\alpha \oplus \beta}$  is non-associative and its left-regular representation sends  $u_{\text{bin}(k)} \mapsto L_{e_k}^{\mathcal{O}}$ . This algebra is therefore isomorphic to the octonions  $\mathcal{O}$  themselves: the twisted group algebra construction recovers the original representation, not a new one.

The cocycle condition fails on non-Fano triples. The map  $c_{\text{oct}}$  is not a group 2-cocycle: the cocycle identity  $c(\alpha, \beta) c(\alpha \oplus \beta, \gamma) = c(\alpha, \beta \oplus \gamma) c(\beta, \gamma)$  fails for exactly the 28 non-collinear triples in PG(2,  $\mathbb{F}_2$ ). The 7 Fano lines satisfy it — these are precisely the triples for which both parenthesisations of the triple product agree:  $(u_p \cdot u_r) \cdot u_t = u_p \cdot (u_r \cdot u_t) = \varepsilon_{p,r,t} \cdot u_0$ . The failure on non-Fano triples is the octonion associator.

The fundamental obstruction. Every Pauli string squares to +I, while  $L_{e_k}^2 = -I$  in Cliff (0,7). This group-theoretic mismatch is the precise obstruction: no assignment of single Pauli strings to the generators of  $\mathcal{O}$  can reproduce the octonion multiplication, even projectively.

**Open problem (Paper 8).** The Fano duality  $\{p, r, t\} \mapsto Q_{\{p, r, t\}}$  identified above is the duality between X-type and Z-type stabilizers in the CSS codes of [4]. Establishing this correspondence as a theorem — and determining whether the non-Fano failure of

## PDF page 7

the cocycle condition has a code-theoretic interpretation — is the natural problem for a subsequent paper.

#### 7. Discussion

- 7.1. Geometric meaning of the Fano reflection. The operator  $R_F = 2P_F - I_8$  acting on  $\mathcal{O} = \mathbb{R}^8$  is the reflection fixing the Fano 4-flat  $F = \{0, p, r, t\}$  and negating its orthogonal complement (the lo-flat). The sub-algebra  $\mathbb{H}_{prt} := \text{span}\{e_0, e_p, e_r, e_t\} \cong \mathbb{H}$  (quaternions) is a Cayley–Dickson subalgebra of  $\mathcal{O}$ , and  $R_F$  is its grading involution: the  $\mathbb{Z}/2\mathbb{Z}$ -grading of  $\mathcal{O}$  with even part  $\mathbb{H}_{prt}$  and odd part its orthocomplement. Thus  $\Gamma_{prt} = L_{e_p}L_{e_r}L_{e_t}$  is the *chirality element* of the quaternionic subalgebra associated to the Fano line  $\{p, r, t\}$ .
- 7.2. Connection to the sign-parity framework. The Fano reflection identity provides a Clifford-algebraic realisation of the sign-parity discriminant. The octonion triple sign  $\varepsilon_{p,r,t}$  coincides with  $\pi(F,\operatorname{split})$  for the corresponding 2-flat in  $A_4$  ([1], Definition 7.2), bridging the sign-parity classification of Paper 1 with the present Clifford representation. The ZD zeta function of [3], whose poles encode the four division-algebra thresholds, acquires a Clifford-algebraic interpretation through this bridge: the residue at each pole corresponds to the count of Fano triples acting via  $\Gamma_{prt}$ .
- 7.3. Verified extension to  $n \leq 7$ . The construction  $\rho(A) = L_{\varepsilon(A)}^{\mathcal{O}}$  and all three main theorems extend to all  $n \geq 4$ , with  $\rho$  defined on the EF-type active elements of  $ZD^*(n)$ .

**Theorem 7.1** (Extension to  $n \le 7$ ). For every  $n \in \{4, 5, 6, 7\}$ :

- (1) All EF-type ZD pairs of  $A_n$  have distinct  $\varepsilon$ -indices (Theorem 2.2).
- (2)  $\{\rho(A), \rho(B)\}=0$  for all EF-type ZD pairs (Theorem 5.1).
- (3)  $L_{e_p}L_{e_r}L_{e_t} = \varepsilon_{p,r,t} R_F$  for all 7 Fano lines (Theorem 5.6).

Proof. Items (2) and (3) concern only the  $A_3$  structure and are independent of n. Item (1) is verified computationally for  $n \leq 7$  (Appendix A). The algebraic proof for all n follows by induction on the hereditary decomposition ([1], Theorem 8.1): every EF-type ZD pair in  $A_{n+1}$  arises from an EF-type ZD pair in  $A_n$  under the Cayley-Dickson embedding, which preserves the  $\varepsilon$ -index structure.

### APPENDIX A. NUMERICAL VERIFICATION

All theorems were verified computationally for n=4,5,6,7 using Python/NumPy on an AMD Ryzen Threadripper 2950X (16 physical cores).  $GL(3,\mathbb{F}_2)$ -equivariance (Theorem 5.2) was additionally verified in GAP 4.15.

**ZD counts by block type.** Active elements of  $A_n$  are classified as EF (one component in the E-block  $\{1, \ldots, 2^{n-1} - 1\}$ , one in the F-block  $\{2^{n-1}, \ldots, 2^n - 1\}$ ), EE (both in E), or FF (both in F). EE and FF pairs are zero-divisors inherited from the embedded copy of  $A_{n-1}$  ([1], Theorem 8.1); the map  $\rho$  is defined on EF-type elements.

**Theorem 2.2** (distinct  $\varepsilon$ -indices): 0 failures among EF-type ZD pairs at every n.

**Theorem 5.6** (Fano Reflection Identity):  $||L_{e_p}L_{e_r}L_{e_t} - \varepsilon_{p,r,t}R_F||_{\max} = 0$  for all 7 Fano lines, verified independently of n.

**Theorem 5.2** (GL(3,  $\mathbb{F}_2$ )-equivariance): verified in GAP 4.15 by constructing the permutation group

$$G = \langle \sigma_1, \sigma_2 \rangle \subset \operatorname{Sym}(\{1, \dots, 7\})$$

with  $\sigma_1 = (2\ 6)(3\ 7)$  and  $\sigma_2 = (1\ 4\ 2)(3\ 5\ 6)$ . GAP confirms |G| = 168,  $G \cong PSL(2,7)$ , G is 2-transitive on  $\{1,\ldots,7\}$ , and all 7 Fano lines are preserved by all 168 elements of G.

## PDF page 8

| n | dim | EF      | EE     | FF     | Cross   | Total   | Expected | Time   |
|---|-----|---------|--------|--------|---------|---------|----------|--------|
| 4 | 16  | 336     | —      | —      | —       | 336     | 336      | <0.1 s |
| 5 | 32  | 3,696   | 336    | 336    | 672     | 5,040   | 5,040    | <1 s   |
| 6 | 64  | 31,920  | 5,040  | 5,040  | 10,080  | 52,080  | 52,080   | 1 s    |
| 7 | 128 | 260,400 | 52,080 | 52,080 | 104,160 | 468,720 | 468,720  | 58 s   |

Table 2. ZD pair counts by block type for An, n = 4, . . . , 7. EF: one index in each block (new pairs); EE/FF: both indices in the same block (inherited from An−1); Cross: pairs involving one inherited and one new EF element (= EE+FF). Expected total: |ZD(n)| = 336 n−1 3 2 .

# Acknowledgements

The author thanks Claude (Anthropic) for extensive assistance with algebraic verification, proof development, and LATEX editing throughout this work and the companion papers.

# References

- [1] G. Levratti, Sign-Parity Classification of Zero Divisors in Cayley–Dickson Algebras, Zenodo preprint (2026), [doi:10.5281/zenodo.20315751.](https://doi.org/10.5281/zenodo.20315751)
- [2] G. Levratti, Zero-Divisors in Cayley–Dickson Algebras: Fano Geometry, Automorphisms, and the Weil Zeta Function, Zenodo preprint (2026), [doi:10.5281/zenodo.20417859.](https://doi.org/10.5281/zenodo.20417859)
- [3] G. Levratti, Sign Structure, Automorphism Groups, and the ZD Zeta Function of Cayley–Dickson Algebras, Zenodo preprint (2026), [doi:10.5281/zenodo.20397587.](https://doi.org/10.5281/zenodo.20397587)
- [4] G. Levratti, Active Stabilizers in Reed–Muller CSS Codes from Cayley–Dickson Zero-Divisors, Zenodo preprint (2026), [doi:10.5281/zenodo.20431754.](https://doi.org/10.5281/zenodo.20431754)
- [5] J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), 145–205.
- [6] R. D. Schafer, An Introduction to Nonassociative Algebras, Academic Press, New York, 1966.
- [7] I. R. Porteous, Clifford Algebras and the Classical Groups, Cambridge University Press, 1995.

Independent Researcher, Modena, Italy Email address: giovanni.levratti.research@gmail.com
