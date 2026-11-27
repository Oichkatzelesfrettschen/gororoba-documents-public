Source: https://jcbi.org/index.php/Main/article/download/617/526
PDF sha256: 5e83a7ad9e0f0a673c04bfe57bcc1747209561df1bd47b9fd204b5e65ddb2bed
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of zahid_2024_graphical_computational_analysis_cayley_dickson_elements_over_zp.pdf

Transcription of `zahid_2024_graphical_computational_analysis_cayley_dickson_elements_over_zp.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

Journal of Computing & Biomedical Informatics Volume 07 Issue 02 ISSN: 2710 - 1606 2024

Research Article https://doi.org/10.56979/702/2024

# **Graphical and Computational Analysis of Cayley-Dickson Algebra Elements over**

**Saba Zahid1, Muazzam Ali1\*, M Usman Hashmi1, Abdul Manan1, and Affan Ahmad2**

1Department of Basic Sciences, Superior University, Lahore, 54000, Pakistan. 2Department of Computer Science, Superior University, Lahore, 54000, Pakistan. \* Corresponding Author: Muazzam Ali. Email: muazzamali@superior.edu.pk

**Received:** May 23, 2024 **Accepted:** August 09, 2024 **Published:** September 01, 2024 **\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_**

**Abstract:** In order to determine the number of idempotent, nilpotent, and zero Divisors inside this algebraic structure, this research work gives a thorough Study of Cayley Dickson algebra over ! . We also look at how many unit components there are in the algebra and offer a basic method for figuring out how many units are often present. We write pseudo code and techniques that may be used to locate these algebraic components in order to make actual implementation easier. Furthermore, we create a graphical depiction of the idempotent, nilpotent, zero divisor and units using MATLAB. By utilizing these discoveries, we expand knowledge in the area of Cayley Dickson algebras and offer an important resource for future study and application in related fields. The computed result are useful in Time like, light like and space like.

**Keywords:** Cayley-Dickson Algebra; Idempotent; Nilpotent; Units; Zero Divisors.

# **1. Introduction**

The Cayley-Dickson construction is a mathematical technique that produces a series of algebras over a field. It was developed by Arthur Cayley and Leonard Eugene Dickson. Each algebra in this series has a dimension that is twice as large as the one before it. These algebras, also known as Cayley Dickson algebras, are often used in the field of mathematical physics. In order to build Cayley-Dickson algebras, a new algebra that resembles the direct sum of an algebra with itself must first be created. The multiplication in this new algebra is defined differently than the multiplication offered by a true direct sum, though. The algebra also has a function called conjugation that does an involution. Composition algebras using Cayley-Dickson algebras are frequently used as helpful tools for a variety of mathematical and scientific inquiries. They have shown to be helpful in researching a variety of mathematical physics problems. An element's norm can be calculated by multiplying it by its conjugate or by taking the square root of the result. As the Cayley-Dickson structure is used frequently, the genuine field's properties progressively disappear. Loss of order, commutativity, and associativity are included in this. Complex numbers, which may be written as ordered pairs of real numbers, are the equivalent of the first step in this algebraic progression. Component-wise addition is used, and the definition of multiplication is

$$(a,b)(c,d) = (ac + bd,ad + bc)$$

R. Hamilton developed quaternions (ℍ) in 1843 to expand the idea of Complex numbers into four dimensions [4]. In terms of algebra, ℍ has a Dimension of 4 and is a division algebra (also known as a skew field) over the real numbers (ℝ) [4, 17]. The quaternion algebra ℍ shows the following properties: it is noncommutative (changing the order of multiplication effects the outcome), associative (operation order doesn't matter), and it is not a division ring (certain elements may not have multiplicative inverses). The four essential components of algebra are 1, , and, each of which has a unique connection and set of characteristics.

$$i^2 = j^2 = k^2 = -1$$
,  $ij = k = -ji$ ,  $jk = i = -kj$ ,  $ki = j = -ik$ ,  $ijk = -1$

## PDF page 2

In [10], the researchers analyzed the finite ring # \$! , where stands for a prime number. They looked into the ring's structure and numerous qualities that were connected to it. The structure of # \$! was recently described in detail by Miguel and Serodio in [3, 18]. Split quaternions were introduced by Cockle in 1849 [8]. The split-quaternion algebra, abbreviated as ℍ, is an associative, non-commutative, and non-divisional algebraic system. It is made up of four fundamental components: 1,, and, each of which has unique restrictions or limitations.

$$i^2 = 1, j^2 = k^2 = -1, ij = k = -ji, jk = -i = -kj, ki = j = -ik, ijk = -ik, ki = j = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk = -ik, ijk$$

The algebraic structure known as a normed division algebra, or O, is made up of octonions. They are the biggest algebra because they have eight dimensions, which is twice as many as quaternions. The fundamental building block from which the octonions were deduced and expanded was the quaternion. Inspired by William Hamilton's previous discovery of quaternions, John T. Graves first discovered the octonions in 1843. He gave them the name "octaves" and noted them in a letter to Hamilton. However, Graves published his conclusions formally in Graves (1845), which was published a little after Cayley's work on the same topic. The octonions, which were independently discovered by Arthur Cayley, are also occasionally referred to as Cayley numbers or the Cayley algebra. The early events surrounding Graves' discovery were covered by Hamilton in his book from 1848. The octonions can be thought of as octets (or 8-tuples) of real numbers. Every octonion is a real linear combination of the unit octonions

$$x = q_0 e_0 + q_1 e_1 + q_2 e_2 + q_3 e_3 + q_4 e_4 + q_5 e_5 + q_6 e_6 + q_7 e_7$$

The scalar element % is equivalent to the number 1 in octonions. Similar to how quaternions are added and subtracted, so are octonions. Corresponding terms and their coefficients are added or subtracted. It's trickier to multiply in octonions. So must multiply the coefficients of each phrase and add them together to multiply two octonions. There is a multiplication table for the unit octonions so that can be better comprehend multiplication in octonions. The output of multiplying several pairs of unit octonions is displayed in this Table 1.

**Table 1.** Multiplication of Octonion

|   | 1 |    |    |    |    |    |    |    |
|---|---|----|----|----|----|----|----|----|
| 1 | 1 |    |    |    |    |    |    |    |
|   |   | -1 |    |    |    |    |    |    |
|   |   |    | -1 |    |    |    |    |    |
|   |   |    |    | -1 |    |    |    |    |
|   |   |    |    |    | -1 |    |    |    |
|   |   |    |    |    |    | -1 |    |    |
|   |   |    |    |    |    |    | -1 |    |
|   |   |    |    |    |    |    |    | -1 |

Split-octonion , are 8-dimensional non-associative algebra over field. The signature of their quadratic forms differs, the split octonions have a split signature (4, 4)

**Table 2.** Multiplication of Octonions,

|   | 1 |    |    |    |   |   |   |   |
|---|---|----|----|----|---|---|---|---|
| 1 | 1 |    |    |    |   |   |   |   |
|   |   | -1 |    |    |   |   |   |   |
|   |   |    | -1 |    |   |   |   |   |
|   |   |    |    | -1 |   |   |   |   |
|   |   |    |    |    | 1 |   |   |   |
|   |   |    |    |    |   | 1 |   |   |
|   |   |    |    |    |   |   | 1 |   |
|   |   |    |    |    |   |   |   | 1 |

For more description on octonions and split octonion algebra see [1, 7, 8, and 9]. Similarly, we can define sixtonion and so on for higher dimensions since matrix multiplication usually comes after associativity, octonions and split-octonions cannot be represented using ordinary matrices due to their non-associative character. However, Zorn came up with a different strategy to represent them using

## PDF page 3

modified matrix multiplication. The vector-matrices used in this format are  $2 \times 2$  in size and contain both scalars and vectors. Refer to [11, 14, 15, 19, and 20] for further in-depth details. A vector-matrix  $2 \times 2$  of the following form can be specified more precisely:

$$(a \vec{v} \vec{w} b)$$

Where a and b are real numbers and  $\vec{v}$  and  $\vec{w}$  are vectors in  $\mathbb{R}$ . The Multiplication is define as:  $(a \vec{v} \vec{w} b)(a' \vec{v}' \vec{w}' b') = (aa' + \vec{v} \odot \vec{w}' a\vec{v}' + b'\vec{v} + \vec{w} \otimes \vec{w}' a'\vec{w} + b\vec{w}' - \vec{v} \otimes \vec{v}' bb' + \vec{v}' \odot \vec{w})$ 

Where  $\odot$  and  $\otimes$  are simple dot product and cross product. The determinant of a vector matrix in Zorn's vector-matrix algebra is a measurement of the scaling or volume change brought on by the matrix's transformation. It is determined taking into account the elements of the vector-matrix using the common determinant formula for 2x2 matrices. In Zorn's vector-matrix algebra, an 8-dimensional algebra over the real numbers, the determinant aids in understanding the characteristics of the transformation represented by the matrix.

$$|a \vec{v} \vec{w} b| = ab - \vec{v} \odot \vec{w}$$

An element x is regarded as idempotent in any algebra if its square  $x^2$  produces the same outcome as x itself. When an element x is raised to a power  $x^n$ , where n is an integer, the outcome is 0, the element is said to be nilpotent [15]. If there is another element y present in the same algebra such that their multiplication (xy or yx) equals to 1, the multiplicative identity, then the element is x categorised as a unit in the algebra. On the other hand, if there is another element y present in the algebra such that their multiplication  $(xy \ or \ yx)$  equals 0 but  $x \neq 0, y \neq 0$  then the element x is said to have a zero divisor. In the Cayley Dickson algebra over  $Z_p$ , the number of idempotent elements and zero divisors is proved in this study [16]. It also offers the prerequisites for locating unit elements in this algebra. The study covers a comparison of these unit elements' features inside the algebra as well as the creation of pseudocodes and methods for computing them. This research makes good sized contributions to the observed of Cayley-Dickson algebras over top fields through thoroughly analyzing the algebraic residences of idempotent, nilpotent, and 0 divisors. It offers a computational technique, such as pseudocode and strategies, to discover and calculate these factors, facilitating practical implementation. Additionally, the graphical illustration of algebraic components the usage of MATLAB provides a visible expertise, advancing knowhow in the area. The consequences offer a foundational framework for destiny research, mainly in mathematical physics and higher-dimensional algebraic structures.

#### 2. Methodology

N this have a look at, we carried out an in depth exam of the Cayley-Dickson algebra over  $Z_p$ , where p is a prime number. The studies methodology concerned both analytical and computational approaches to decide key algebraic factors including idempotent, nilpotent, zero divisors, and unit factors. The steps followed within the method are mentioned beneath:

**Algebraic Framework**: We first defined the fundamental algebraic structure of Cayley-Dickson algebras, extending from the quaternion and octonion algebras. The algebra was built using a recursive process to double the size of the previous algebra whilst preserving certain homes, like normed department.

**Identification of Algebraic** Elements: We centered on computing the variety of idempotent, nilpotent, and zero divisor elements within the algebra. Using matrix-based totally strategies, we formulated the situations for each of those elements. Specifically, we derived situations for idempotency.

**Graphical** Representation: MATLAB become hired to create graphical representations of the important thing elements—idempotents, nilpotents, zero divisors, and unit elements. These graphs offer an intuitive knowledge of the distribution and properties of these factors in the algebraic structure.

**Proofs and Theoretical Validation:** The theoretical results, which includes the quantity of idempotents and nilpotents, have been tested the use of set up algebraic theorems. Specifically, we mentioned present literature on matrix algebra over finite fields to corroborate our findings. The consequences had been then generalized for Cayley-Dickson algebras of better dimensions.

This multi-faceted method, combining theoretical proofs, computational tools, and graphical visualizations, guarantees a sturdy exploration of the Cayley-Dickson algebra over  $\mathbb{Z}_p$ . Our methodology presents a sturdy basis for similarly exploration of higher-dimensional algebras in mathematical and physical programs.

## PDF page 4

#### **3. Results and Discussions**

In this section we will prove our main results. The number of idempotent elements # \$! and #" \$! are " + + 2, where is an odd prime. (For proof .See [3] and [6]). We will prove the result for octonions and splitoctonion over !.

# **Theorem 1: Let be an odd prime then**

$$\left| Id \left( \frac{O}{Z_p} \right) \right| = \left| Id \left( \frac{O}{Z_p} \right) \right| = p^6 + p^3 + 2$$

**Proof:** As / \$! ≅ 0#×# \$! , so in the both algebra number of idempotent are same. So, we find the number of idempotent in 0#×# \$! . An element M of 0#×# \$! is idempotent if

$$M^2 = M \pmod{\mathfrak{p}} \tag{1}$$

$$M(M-1) = 0 \pmod{p} \tag{2}$$

$$(a\vec{v}\vec{w}b)(a-1\vec{v}\vec{w}b-1)(0000)$$
 (3)

$$(a(a-1) + \vec{v} \odot \vec{w} \, a\vec{v} + (b-1)\vec{v} \, (a-1)\vec{w} + b\vec{w} \, b(b-1) + \vec{v} \odot \vec{w}) = (0 \, 0 \, 0 \, 0) \tag{4}$$

$$a(a-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$
 (i)

$$a\vec{v} + (b-1)\vec{v} = 0 \pmod{p} \tag{ii}$$

$$(a-1)\vec{w} + b\vec{w} = 0 \pmod{p}$$
 (iii)

$$b(b-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$
 (iv)

Case I: Let ⃗ = ::⃗ = 0

Then there are only 2 possible values for a and d, so there are 4 matrices of this solution

Case II: Let ⃗ = 0, ::⃗ ≠ 0 then

$$a(a-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

$$(a-1)\vec{w} + b\vec{w} = 0 \qquad (mod \ p)$$

$$b(b-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

 From this and have values 0 or 1, and ::::⃗can take' − 1. So there are (' − 1) total possible solutions.

Case III: Let ⃗ ≠ 0 ::⃗ = 0 then

$$a(a-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

$$a\vec{v} + (b-1)\vec{v} = 0 \qquad (mod \ p)$$

$$b(b-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

From this and have values 0 or 1, ⃗ can take' − 1. So there are (' − 1) total possible solutions.

Case IV: Let ⃗ ≠ ::⃗ ≠ 0 then

$$a\vec{v} + (b-1)\vec{v} = 0 \pmod{p}$$

$$a\vec{w} + (b-1)\vec{w} = 0 \ (mod \ p)$$

From this we have + = 1, so there are possible combination but we cannot take = 0 and = 1 because this leads ⃗ ⊙ ::⃗ so there are ' − 2 possible solutions.

$$a(a-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

$$b(b-1) + \vec{v} \odot \vec{w} = 0 \pmod{p}$$

The above equations have ' − 1 possible solutions. In this case total possible solutions are (' − 1 )( ' − 2). Sum the all possibilities in all above cases we get \* + ' + 2.

**Figure 1.** Line Graph 1

## PDF page 5

#### Corollary 2: Let p be an odd prime then

$$\left|Id(CDA)_{Z_p}\right| = p^{\alpha-2} + p^{\frac{\alpha}{2}-1} + 2$$

Where  $\alpha = 2^n$ , n = 2,3,4,...

Proof: Similar proof as theorem 2.1, Here we will consider Zorn's vector matrix algebra  $(a \vec{v} \vec{w} b)$ , where  $\vec{v}$  and  $\vec{w}$  are vectors of dimension  $p^{\frac{\alpha}{2}-1}$ .

The above graph the number of idempotent in  $\frac{H}{Z_p}$  for p = 3,5,7,11,13, 19. Now, the number of idempotent elements  $\frac{H}{Z_p}$  and  $\frac{H_s}{Z_p}$  are  $p^2$ , p is an odd prime (for proof see [12] and [6].

# Theorem 3: Let p be an odd prime then

$$\left| nil \left( \frac{O}{Z_p} \right) \right| = \left| nil \left( \frac{O_s}{Z_p} \right) \right| = p^6$$

**Proof:** In [13] Fine and Herstein show that the probability that  $n \times n$  matrix over a Galois field with  $p^k$  elements having  $p^{-kn}$  nilpotent elements. As in our case, k = 1 and n = 2, so the probability that  $2 \times 2$  matrix over  $Z_p$  have with  $p^{-2}$ nilpotent elements.

$$\begin{split} \frac{\left| nil\left(\frac{M_{2\times 2}}{Z_p}\right) \right|}{\left| \frac{M_{2\times 2}}{Z_p} \right|} &= p^{-2} \\ \frac{\left| nil\left(\frac{M_{2\times 2}}{Z_p}\right) \right|}{p^8} &= p^{-2} \\ \left| nil\left(\frac{M_{2\times 2}}{Z_p}\right) \right| &= p^6 \end{split}$$

Figure 2. Line Graph 2

**Corollary 4:** For p a prime, number of nilpotent in Cayley Dickson's algebra over  $Z_p$  are  $p^{\alpha-2}$ , Where  $\alpha=2^n, n=2,3,4,...$ 

**Proof:** 

$$\frac{\left| nil \left( \frac{M_{2 \times 2}}{Z_p} \right) \right|}{\left| \frac{M_{2 \times 2}}{Z_p} \right|} = p^{-2}$$

$$\frac{\left| nil \left( \frac{M_{2 \times 2}}{Z_p} \right) \right|}{p^{\alpha}} = p^{-2}$$

## PDF page 6

$$\left| nil \left( \frac{M_{2 \times 2}}{Z_p} \right) \right| = p^{\alpha - 2}$$

Here  $M_{2\times 2}=(a\ \vec{v}\ \vec{w}\ b$ ), where  $\vec{v}$  and  $\vec{w}$  are vectors of dimension  $p^{\frac{\alpha}{2}-1}$ . The above graph the number of nilpotent  $\frac{H}{Z_n}$  in for p=3,5,7,11,13,19.

Theorem 5: For p an odd prime then

$$\left|nil\left(\frac{O}{Z_p}\right)\cap nil\left(\frac{O_s}{Z_p}\right)\right|=(p^3+p^2-p)$$

**Proof:** An element  $x \in nil\left(\frac{o}{z_p}\right)$  if  $q_0 = 0$  and  $\sum_{i=1}^7 \square q_i^2 = 0$ . Similarly,  $x \in nil\left(\frac{o_s}{z_p}\right)$ , if  $q_0 = 0$  and  $\sum_{i=1}^7 \square q_i^2 = 0$ 

$$\sum_{i=1}^{3} |||||q_{i}|^{2} + \sum_{i=4}^{4} |||||q_{i}|^{2} = \sum_{i=1}^{3} |||||q_{i}|^{2} - \sum_{i=4}^{7} |||||q_{i}|^{2}$$

$$\sum_{i=4}^{7} |||||q_{i}|^{2} = q_{4}^{2} + q_{5}^{2} + q_{6}^{2} + q_{7}^{2} = 0$$

Now the above equation become the norm of quaternions or split quaternions, so this equation has  $p^3 + p^2 - p$  see [3].

Now, for p an odd prime, the number of zero divisors in  $\frac{H}{z_p}$  and  $\frac{H_s}{z_p}$  are  $p^3 + p^2 - p$  (for proof see [6]) and for p an odd prime, the number of zero divisors in  $\left(\frac{o}{z_p}\right)$  and  $\left(\frac{o_s}{z_p}\right)$  are  $p^3 + p^2 - p$  (for proof see [5]).

Figure 3. Line Graph 3

**Corollary 6:** For p an odd prime then number of zero divisors in Cayley Dickson's Algebra over  $Z_p$  are:  $p^{\alpha-1}+p^{\frac{\alpha}{2}}+p^{\frac{\alpha}{2}-1}$ 

Where  $\alpha = 2^n n = 2,3,4, ...$ 

**Proof:** Similar proof as in [5] for octonion and split octonion over  $Z_p$ , Here  $M_{2\times 2}=(a\ \vec{v}\ \vec{w}\ b)$ , where  $\vec{v}$  and  $\vec{w}$  are vectors of dimension  $p^{\frac{\alpha}{2}-1}$ .

**Theorem 7:** For p an odd prime then number of unit elements in Cayley Dickson's Algebra over  $Z_p$  are

$$p^{\alpha} - \left(p^{\alpha-1} + p^{\frac{\alpha}{2}} + p^{\frac{\alpha}{2}-1}\right)$$

Where  $\alpha = 2^n \ n = 2,3,4, \dots$ .

**Proof**: Since we know that an element of Cayley Dickson's algebra is either zero divisor or unit element, total number of Cayley Disckson's Algebra are  $p^{\alpha}$ , Where  $\alpha=2^n$   $n=2,3,4,\ldots$  and  $\left(p^{\alpha-1}+p^{\frac{\alpha}{2}}+p^{\frac{\alpha}{2}-1}\right)$  are zero divisors, so  $p^{\alpha}-\left(p^{\alpha-1}+p^{\frac{\alpha}{2}}+p^{\frac{\alpha}{2}-1}\right)$  are units elements.

Following graph *represent* the number of zero divisors of  $\frac{H}{Z_p}$  for p = 3, 5, 7, 11

## PDF page 7

### **4. Conclusions**

 In conclusion, is space-like, time-like and light-like() < 0, () > 0and () = 0 respectively. As we discussed the idempotent, nilpotent and zero divisor in Cayley Dickson algebra over!, as in these elements(). We also discuss unit elements such that - = 1. Interesting question is to extend the work to spacelike, time like and light like for Cayley Dickson algebra for higher dimensions. Also, we can discuss the graph in Cayley Dickson algebra regarding to idempotents, nilpotent and zero divisors as we discuss the graph of unit elements in algebras of quaternion over!.

**Data Availability Statement:** The data supporting the findings of this study are available upon request from the corresponding author. No publicly archived datasets were used or generated during the study.

**Acknowledgments:** The authors would like to acknowledge the technical support provided by [institution or lab name] and the use of MATLAB for graphical representation. Additionally, they are grateful for the constructive feedback received from their peers.

**Conflicts of Interest:** The authors declare no conflict of interest. The funders had no role in the design of the study, the collection, analyses, or interpretation of data, the writing of the manuscript, or the decision to publish the results.

## PDF page 8

#### **References**

- 1. J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), 145-205. Errata in Bull. Amer. Math. Soc. 42 (2005), 213. Corrected version available at math. A/0105155.
- 2. John H. Conway and Derek A. Smith on Quaternions and Octonions: Their Geometry, Arithmetic, and Symmetry Bull. Amer. Math. Soc. 42 (2005), 229- 243.
- 3. C. J. Miguel and R. Serodio, On the Structure of Quaternion Rings over , International Journal of Algebra, Vol.5, 27 (2011), 1313-1325
- 4. R. Remmert et all, Numbers, Springer, 1991
- 5. Muazzam Ali, Fahad Sabah and Abdul Manan, PONTE international scientific researches journal, august (2016) issue 72 volume 8 (308-316).
- 6. Shin Min Kang, Mobeen Munir, Abdul Rauf Nizami, Muazzam Ali and Waqas Nazeer, On Elements of Split Quaternions over , Global Journal of Pure and Applied Mathematics, ISSN 0973-1768 Volume 12, Number 5 (2016), pp. 4253 - 4271.
- 7. S. Susumu, Okubo, Introduction to octonions and other non-associative algebras in Physics, University of Cambridge, ISBN 0521 47215 6 1995.
- 8. B.C Chanyal, Octonion generalization of Pauli and Dirac matrices. International Journal of Geometric Methods in Modern Physics World Scientific. 2015.
- 9. R.D. Schafer, An Introduction to No-associative Algebras, Academic Press, New York and London, 1966.
- 10. M. Aristidou and A. Demetre, A Note on Quaternion Rings over , International Journal of Algebra, Vol.3, 15 (2009), 725-728.
- 11. Tae-il Suh Algebras formed, The Zorn vector matrix, Pacific Journal of mathematics, Vol 30 No.1, 1969.
- 12. Michael Aristidou, A Note on Nilpotent Elements in Quaternion Rings over , International Journal of Algebra, Vol.6, 14,(2012), 663-666.
- 13. N. J. Fine, I. N. Herstein, The Probability that a Matrix be Nilpotent, Illinois Journal of Mathematics, Vol.2 (1958), No.4A, 499-504.
- 14. K. McCrimmon, A taste of Jordan Algebra, ISBN 0-387-95447-3, 2004 Springer Verlag. 15. R.B. Brown, N.C. Hopkins, Noncommutative matrix Jordan Algebras, Transaction of the American mathematical society, Vol 333, Number1, September 1992
- 15. Diesl, Alexander. "Sums of commuting potent and nilpotent elements in rings." Journal of Algebra and its Applications 22.05 (2023): 2350113.
- 16. Flaut, C. and Baias, A., 2024. Some Remarks Regarding Special Elements in Algebras Obtained by the Cayley– Dickson Process over Zp. Axioms, 13(6), p.351.
- 17. Grau, Jose Maria, Antonio M. Oller-Marcén, and Steve Szabo. "Minimal rings related to generalized quaternion rings." International Electronic Journal of Algebra 34.34 (2023): 88-111.
- 18. Wang, G., Jiang, T., Vasil'ev, V.I. and Guo, Z., 2024. On singular value decomposition for split quaternion matrices and applications in split quaternionic mechanics. Journal of Computational and Applied Mathematics, 436, p.115447.
- 19. Ren, Guangbin, and Xin Zhao. "The Explicit Twisted Group Algebra Structure of the Cayley–Dickson Algebra." Advances in Applied Clifford Algebras 33.4 (2023): 49.
- 20. Chapman, A., Guterman, A., Vishkautsan, S. and Zhilina, S., 2023. Roots and critical points of polynomials over Cayley–Dickson algebras. Communications in Algebra, 51(4), pp.1355-1369.
