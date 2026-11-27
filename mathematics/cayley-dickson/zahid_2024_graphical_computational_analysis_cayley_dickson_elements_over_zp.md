Source: https://jcbi.org/index.php/Main/article/download/617/526
PDF sha256: 5e83a7ad9e0f0a673c04bfe57bcc1747209561df1bd47b9fd204b5e65ddb2bed
License: https://creativecommons.org/licenses/by/4.0/

# Transcription of zahid_2024_graphical_computational_analysis_cayley_dickson_elements_over_zp.pdf

Transcription of `zahid_2024_graphical_computational_analysis_cayley_dickson_elements_over_zp.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Journal of Computing & Biomedical Informatics
ISSN: 2710 - 1606
Research Article
https://doi.org/10.56979/702/2024

Volume 07 Issue 02
2024

Graphical and Computational Analysis of Cayley-Dickson Algebra Elements over
𝐙𝐩
Saba Zahid1, Muazzam Ali1*, M Usman Hashmi1, Abdul Manan1, and Affan Ahmad2
Department of Basic Sciences, Superior University, Lahore, 54000, Pakistan.
Department of Computer Science, Superior University, Lahore, 54000, Pakistan.
*Corresponding Author: Muazzam Ali. Email: muazzamali@superior.edu.pk
1

2

Received: May 23, 2024 Accepted: August 09, 2024 Published: September 01, 2024

________________________________________________________________________________________________________
Abstract: In order to determine the number of idempotent, nilpotent, and zero Divisors inside this
algebraic structure, this research work gives a thorough Study of Cayley Dickson algebra over 𝑍! .
We also look at how many unit components there are in the algebra and offer a basic method for
figuring out how many units are often present. We write pseudo code and techniques that may be
used to locate these algebraic components in order to make actual implementation easier.
Furthermore, we create a graphical depiction of the idempotent, nilpotent, zero divisor and units
using MATLAB. By utilizing these discoveries, we expand knowledge in the area of Cayley Dickson
algebras and offer an important resource for future study and application in related fields. The
computed result are useful in Time like, light like and space like.
Keywords: Cayley-Dickson Algebra; Idempotent; Nilpotent; Units; Zero Divisors.
1. Introduction
The Cayley-Dickson construction is a mathematical technique that produces a series of algebras over
a field. It was developed by Arthur Cayley and Leonard Eugene Dickson. Each algebra in this series has a
dimension that is twice as large as the one before it. These algebras, also known as Cayley Dickson algebras,
are often used in the field of mathematical physics. In order to build Cayley-Dickson algebras, a new
algebra that resembles the direct sum of an algebra with itself must first be created. The multiplication in
this new algebra is defined differently than the multiplication offered by a true direct sum, though. The
algebra also has a function called conjugation that does an involution. Composition algebras using CayleyDickson algebras are frequently used as helpful tools for a variety of mathematical and scientific inquiries.
They have shown to be helpful in researching a variety of mathematical physics problems. An element's
norm can be calculated by multiplying it by its conjugate or by taking the square root of the result. As the
Cayley-Dickson structure is used frequently, the genuine field's properties progressively disappear. Loss
of order, commutativity, and associativity are included in this. Complex numbers, which may be written
as ordered pairs of real numbers, are the equivalent of the first step in this algebraic progression.
Component-wise addition is used, and the definition of multiplication is
(𝑎, 𝑏)(𝑐, 𝑑) = (𝑎𝑐 + 𝑏𝑑, 𝑎𝑑 + 𝑏𝑐)
R. Hamilton developed quaternions (ℍ) in 1843 to expand the idea of Complex numbers into four
dimensions [4]. In terms of algebra, ℍ has a Dimension of 4 and is a division algebra (also known as a skew
field) over the real numbers (ℝ) [4, 17]. The quaternion algebra ℍ shows the following properties: it is noncommutative (changing the order of multiplication effects the outcome), associative (operation order
doesn't matter), and it is not a division ring (certain elements may not have multiplicative inverses). The
four essential components of algebra are 1, 𝑖, 𝑗 and𝑘, each of which has a unique connection and set of
characteristics.
𝑖 " = 𝑗 " = 𝑘 " = −1, 𝑖𝑗 = 𝑘 = −𝑗𝑖, 𝑗𝑘 = 𝑖 = −𝑘𝑗, 𝑘𝑖 = 𝑗 = −𝑖𝑘, 𝑖𝑗𝑘 = −1

ID : 617-0702/2024

## PDF page 2

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02
#

In [10], the researchers analyzed the finite ring$ , where 𝑝 stands for a prime number. They looked into
!

#

the ring's structure and numerous qualities that were connected to it. The structure of $ was recently
!

described in detail by Miguel and Serodio in [3, 18]. Split quaternions were introduced by Cockle in 1849
[8]. The split-quaternion algebra, abbreviated as ℍ, is an associative, non-commutative, and non-divisional
algebraic system. It is made up of four fundamental components: 1,𝑖, 𝑗 and𝑘, each of which has unique
restrictions or limitations.
𝑖 " = 1, 𝑗 " = 𝑘 " = −1, 𝑖𝑗 = 𝑘 = −𝑗𝑖, 𝑗𝑘 = −𝑖 = −𝑘𝑗, 𝑘𝑖 = 𝑗 = −𝑖𝑘, 𝑖𝑗𝑘 =
The algebraic structure known as a normed division algebra, or O, is made up of octonions. They are
the biggest algebra because they have eight dimensions, which is twice as many as quaternions. The
fundamental building block from which the octonions were deduced and expanded was the quaternion.
Inspired by William Hamilton's previous discovery of quaternions, John T. Graves first discovered the
octonions in 1843. He gave them the name "octaves" and noted them in a letter to Hamilton. However,
Graves published his conclusions formally in Graves (1845), which was published a little after Cayley's
work on the same topic. The octonions, which were independently discovered by Arthur Cayley, are also
occasionally referred to as Cayley numbers or the Cayley algebra. The early events surrounding Graves'
discovery were covered by Hamilton in his book from 1848. The octonions can be thought of as octets (or
8-tuples) of real numbers. Every octonion is a real linear combination of the unit octonions
𝑥 = 𝑞% 𝑒% + 𝑞& 𝑒& + 𝑞" 𝑒" + 𝑞' 𝑒' + 𝑞( 𝑒( + 𝑞) 𝑒) + 𝑞* 𝑒* + 𝑞+ 𝑒+
The scalar element 𝑒% is equivalent to the number 1 in octonions. Similar to how quaternions are added
and subtracted, so are octonions. Corresponding terms and their coefficients are added or subtracted. It's
trickier to multiply in octonions. So must multiply the coefficients of each phrase and add them together
to multiply two octonions. There is a multiplication table for the unit octonions so that can be better
comprehend multiplication in octonions. The output of multiplying several pairs of unit octonions is
displayed in this Table 1.
Table 1. Multiplication of Octonion
1
1
1
-1
-1
-1
-1
-1
-1
-1
Split-octonion 𝑂, are 8-dimensional non-associative algebra over field. The signature of their quadratic
forms differs, the split octonions have a split signature (4, 4)
Table 2. Multiplication of Octonions,
1
1
1
-1
-1
-1
1
1
1
1
For more description on octonions and split octonion algebra see [1, 7, 8, and 9]. Similarly, we can
define sixtonion and so on for higher dimensions since matrix multiplication usually comes after
associativity, octonions and split-octonions cannot be represented using ordinary matrices due to their
non-associative character. However, Zorn came up with a different strategy to represent them using

ID : 617-0702/2024

## PDF page 3

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02

modified matrix multiplication. The vector-matrices used in this format are 2 × 2 in size and contain both
scalars and vectors. Refer to [11, 14, 15, 19, and 20] for further in-depth details. A vector-matrix 2 × 2 of the
following form can be specified more precisely:
#⃗ #𝑤
##⃗ 𝑏 %
!𝑎 #𝑣
Where a and b are real numbers and 𝑣⃗ and :𝑤
:⃗ are vectors in ℝ. The Multiplication is define as:
(𝑎 𝑣⃗ :𝑤
:⃗ 𝑏 )(𝑎- 𝑣⃗ - :𝑤
:⃗ - 𝑏- ) = (𝑎𝑎- + 𝑣
:::⃗ ⊙ :𝑤
:⃗ - 𝑎𝑣⃗ - + 𝑏- 𝑣⃗ + :𝑤
:⃗ ⊗ :𝑤
:⃗ - 𝑎- :𝑤
:⃗ + 𝑏𝑤
::⃗ - − 𝑣⃗ ⊗ 𝑣⃗ - 𝑏𝑏- + 𝑣⃗ - ⊙ :𝑤
:⃗ )
Where ⊙ and ⊗ are simple dot product and cross product. The determinant of a vector matrix in
Zorn's vector-matrix algebra is a measurement of the scaling or volume change brought on by the matrix's
transformation. It is determined taking into account the elements of the vector-matrix using the common
determinant formula for 2x2 matrices. In Zorn's vector-matrix algebra, an 8-dimensional algebra over the
real numbers, the determinant aids in understanding the characteristics of the transformation represented
by the matrix.
#⃗ #𝑤
##⃗ 𝑏 &=𝑎𝑏 − 𝑣⃗ ⊙ :𝑤
&𝑎 #𝑣
:⃗
An element 𝑥 is regarded as idempotent in any algebra if its square 𝑥 " produces the same outcome as
𝑥 itself. When an element 𝑥 is raised to a power 𝑥 . , where 𝑛 is an integer, the outcome is 0, the element
is said to be nilpotent [15]. If there is another element y present in the same algebra such that their
multiplication (xy or yx) equals to 1, the multiplicative identity, then the element is 𝑥 categorised as a unit
in the algebra. On the other hand, if there is another element y present in the algebra such that their
multiplication (𝑥𝑦 𝑜𝑟 𝑦𝑥) equals 0 but 𝑥 ≠ 0, 𝑦 ≠ 0 then the element 𝑥 is said to have a zero divisor. In the
Cayley Dickson algebra over 𝑍! , the number of idempotent elements and zero divisors is proved in this
study [16]. It also offers the prerequisites for locating unit elements in this algebra. The study covers a
comparison of these unit elements' features inside the algebra as well as the creation of pseudocodes and
methods for computing them. This research makes good sized contributions to the observed of CayleyDickson algebras over top fields through thoroughly analyzing the algebraic residences of idempotent,
nilpotent, and 0 divisors. It offers a computational technique, such as pseudocode and strategies, to
discover and calculate these factors, facilitating practical implementation. Additionally, the graphical
illustration of algebraic components the usage of MATLAB provides a visible expertise, advancing knowhow in the area. The consequences offer a foundational framework for destiny research, mainly in
mathematical physics and higher-dimensional algebraic structures.
2. Methodology
N this have a look at, we carried out an in depth exam of the Cayley-Dickson algebra over𝑍! ., where 𝑝
is a prime number. The studies methodology concerned both analytical and computational approaches to
decide key algebraic factors including idempotent, nilpotent, zero divisors, and unit factors. The steps
followed within the method are mentioned beneath:
Algebraic Framework: We first defined the fundamental algebraic structure of Cayley-Dickson
algebras, extending from the quaternion and octonion algebras. The algebra was built using a recursive
process to double the size of the previous algebra whilst preserving certain homes, like normed
department.
Identification of Algebraic Elements: We centered on computing the variety of idempotent, nilpotent,
and zero divisor elements within the algebra. Using matrix-based totally strategies, we formulated the
situations for each of those elements. Specifically, we derived situations for idempotency.
Graphical Representation: MATLAB become hired to create graphical representations of the important
thing elements—idempotents, nilpotents, zero divisors, and unit elements. These graphs offer an intuitive
knowledge of the distribution and properties of these factors in the algebraic structure.
Proofs and Theoretical Validation: The theoretical results, which includes the quantity of idempotents
and nilpotents, have been tested the use of set up algebraic theorems. Specifically, we mentioned present
literature on matrix algebra over finite fields to corroborate our findings. The consequences had been then
generalized for Cayley-Dickson algebras of better dimensions.
This multi-faceted method, combining theoretical proofs, computational tools, and graphical
visualizations, guarantees a sturdy exploration of the Cayley-Dickson algebra over 𝑍! . Our methodology
presents a sturdy basis for similarly exploration of higher-dimensional algebras in mathematical and
physical programs.

ID : 617-0702/2024

## PDF page 4

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02

3. Results and Discussions
#
#
In this section we will prove our main results. The number of idempotent elements $ and $ " are 𝑝" +
!

!

𝑝 + 2, where 𝑥 is an odd prime. (For proof .See [3] and [6]). We will prove the result for octonions and splitoctonion over 𝑍! .
Theorem 1: Let 𝑝 be an odd prime then
𝑂
𝑂
E𝐼𝑑 G HE = E𝐼𝑑 G HE = 𝑝* + 𝑝' + 2
𝑍!
𝑍!
/
0
Proof: As$ ≅ $#×#, so in the both algebra number of idempotent are same. So, we find the number of
!

!

0

0

idempotent in $#×#. An element M of $#×#is idempotent if
!

!

𝑀" = 𝑀
(Mod p)
(1)
M (M – 1) = 0 (mod p)
(2)
(a :v⃗ :w
:⃗ b )(a − 1 :v⃗ :w
:⃗ b − 1 )(0 0 0 0 )
(3)
(a(a − 1) + :v⃗ ⊙ :w
:⃗ av:⃗ + (b − 1)v:⃗ (a − 1)w
::⃗ + bw
::⃗ b(b − 1) + :v⃗ ⊙ :w
:⃗ ) = (0 0 0 0 )
(4)
a(a − 1) + :v⃗ ⊙ :w
:⃗ = 0 (mod p)
(i)
av
:⃗ + (b − 1)v
:⃗ = 0 (mod p)
(ii)
(a − 1)w
::⃗ + bw
::⃗ = 0 (mod p)
(iii)
b(b − 1) + :v⃗ ⊙ :w
:⃗ = 0 (mod p)
(iv)
Case I: Let 𝑣⃗ = :𝑤
:⃗ = 0
Then there are only 2 possible values for a and d, so there are 4 matrices of this solution
Case II: Let 𝑣⃗ = 0, 𝑎𝑛𝑑 :𝑤
:⃗ ≠ 0 then
𝑎(𝑎 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0 (𝑚𝑜𝑑 𝑝)
(𝑎 − 1)𝑤
(𝑚𝑜𝑑 𝑝)
::⃗ + 𝑏𝑤
::⃗ = 0
𝑏(𝑏 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0
(𝑚𝑜𝑑 𝑝)
From this 𝑎 and 𝑑 have values 0 or 1, and 𝑤
::::⃗can take𝑝' − 1. So there are (𝑝' − 1) total possible
solutions.
Case III: Let 𝑣⃗ ≠ 0 𝑎𝑛𝑑 :𝑤
:⃗ = 0 then
𝑎(𝑎 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0 (𝑚𝑜𝑑 𝑝)
𝑎𝑣⃗ + (𝑏 − 1)𝑣⃗ = 0
(𝑚𝑜𝑑 𝑝)
𝑏(𝑏 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0
(𝑚𝑜𝑑 𝑝)
From this 𝑎 and 𝑑 have values 0 or 1, 𝑣⃗ can take𝑝' − 1. So there are (𝑝' − 1) total possible solutions.
Case IV: Let 𝑣⃗ ≠ :𝑤
:⃗ ≠ 0 then
𝑎𝑣⃗ + (𝑏 − 1)𝑣⃗ = 0 (𝑚𝑜𝑑 𝑝)
𝑎𝑤
::⃗ + (𝑏 − 1)𝑤
::⃗ = 0 (𝑚𝑜𝑑 𝑝)
From this we have 𝑎 + 𝑑 = 1, so there are 𝑝 possible combination but we cannot take 𝑎 = 0 and 𝑎 = 1
because this leads 𝑣⃗ ⊙ :𝑤
:⃗ so there are 𝑝' − 2 possible solutions.
𝑎(𝑎 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0 (𝑚𝑜𝑑 𝑝)
𝑏(𝑏 − 1) + 𝑣⃗ ⊙ :𝑤
:⃗ = 0
(𝑚𝑜𝑑 𝑝)
The above equations have 𝑝' − 1 possible solutions. In this case total possible solutions are (𝑝' − 1
'
)( 𝑝 − 2). Sum the all possibilities in all above cases we get 𝑝* + 𝑝' + 2.

Figure 1. Line Graph 1

ID : 617-0702/2024

## PDF page 5

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02

Corollary 2: Let 𝑝 be an odd prime then

1

W𝐼𝑑(𝐶𝐷𝐴)$! W = 𝑝12" + 𝑝 " 2& + 2
Where 𝛼 = 2. , 𝑛 = 2,3,4, …
Proof: Similar proof as theorem 2.1, Here we will consider Zorn’s vector matrix algebra(𝑎 𝑣⃗ :𝑤
:⃗ 𝑏 ),
%

where 𝑣⃗ and :𝑤
:⃗ are vectors of dimension 𝑝 # 2& .
#
The above graph the number of idempotent in for p = 3,5,7,11,13, 19. Now, the number of idempotent
elements

#
$!

and

#"
$!

$!

are 𝑝 , 𝑝 is an odd prime (for proof see [12] and [6].
"

Theorem 3: Let 𝒑 be an odd prime then

𝑂
𝑂,
E𝑛𝑖𝑙 G HE = E𝑛𝑖𝑙 G HE = 𝑝*
𝑍!
𝑍!
Proof: In [13] Fine and Herstein show that the probability that 𝑛 × 𝑛 matrix over a Galois field with 𝑝3
elements having 𝑝23. nilpotent elements. As in our case, 𝑘 = 1 and 𝑛 = 2, so the probability that 2 × 2 matrix
over 𝑍! have with 𝑝2" nilpotent elements.
𝑀
a𝑛𝑖𝑙 b 𝑍"×" ca
!
= 𝑝2"
𝑀"×"
a 𝑍 a
!
𝑀"×"
b
a𝑛𝑖𝑙 𝑍 ca
!
= 𝑝2"
𝑝5
𝑀"×"
E𝑛𝑖𝑙 G
HE = 𝑝*
𝑍!

Figure 2. Line Graph 2
Corollary 4: For 𝑝 a prime, number of nilpotent in Cayley Dickson’s algebra over 𝑍! are 𝑝12" , Where 𝛼 =
2. , 𝑛 = 2,3,4, …
Proof:
𝑀
a𝑛𝑖𝑙 b 𝑍"×" ca
!
= 𝑝2"
𝑀"×"
a 𝑍 a
!
𝑀"×"
a𝑛𝑖𝑙 b 𝑍 ca
!
= 𝑝2"
𝑝1

ID : 617-0702/2024

## PDF page 6

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02
𝑀"×"
E𝑛𝑖𝑙 G
HE = 𝑝12"
𝑍!

%

Here𝑀"×" = (𝑎 𝑣⃗ :𝑤
:⃗ 𝑏 ), where 𝑣⃗ and :𝑤
:⃗ are vectors of dimension 𝑝 # 2&
#
The above graph the number of nilpotent $ in for 𝑝 = 3,5,7,11,13, 19.
!

Theorem 5: For 𝒑 an odd prime then
E𝑛𝑖𝑙 G

𝑂
𝑂,
H ∩ 𝑛𝑖𝑙 G HE = (𝑝' + 𝑝" − 𝑝)
𝑍!
𝑍!

/

Proof: An element 𝑥 ∈ 𝑛𝑖𝑙 b c if 𝑞% = 0 and∑+67& ⬚ 𝑞6 " = 0. Similarly,
$!

∑+67& ⬚ 𝑞6 " = 0

'

(
"

'

/

𝑥 ∈ 𝑛𝑖𝑙 b " c, if 𝑞% = 0 and
$!

+

m ⬚ 𝑞6 + m ⬚ 𝑞6 = m ⬚ 𝑞6 − m ⬚ 𝑞6 "
67&

+

"

"

67(

67&

67(

m ⬚ 𝑞6 " = 𝑞(" + 𝑞)" + 𝑞*" + 𝑞+" = 0
67(

Now the above equation become the norm of quaternions or split quaternions, so this equation has
𝑝' + 𝑝" − 𝑝 see [3].
#
#
Now, for p an odd prime, the number of zero divisors in $ and $ " are 𝑝' + 𝑝" − 𝑝 (for proof
!

!

/

/

$!

$!

see [6]) and for p an odd prime, the number of zero divisors in b c and b " c are 𝑝' + 𝑝" − 𝑝 (for proof see
[5]).

Figure 3. Line Graph 3
Corollary 6: For p an odd prime then number of zero divisors in Cayley Dickson’s Algebra over 𝑍! are:
1

1

𝑝12& + 𝑝 " + 𝑝 " 2&

Where 𝛼 = 2. 𝑛 = 2,3,4, … ..
Proof: Similar proof as in [5] for octonion and split octonion over 𝑍! , Here 𝑀"×" = (𝑎 𝑣⃗ :𝑤
:⃗ 𝑏 ), where 𝑣⃗
%

and :𝑤
:⃗ are vectors of dimension 𝑝 # 2& .
Theorem 7: For p an odd prime then number of unit elements in Cayley Dickson’s Algebra over 𝑍! are
1

1

𝑝1 − n𝑝12& + 𝑝 " + 𝑝 " 2& o
Where 𝛼 = 2. 𝑛 = 2,3,4, … ..
Proof: Since we know that an element of Cayley Dickson’s algebra is either zero divisor or unit
element, total number of Cayley Disckson’s Algebra are𝑝1 , Where 𝛼 = 2. 𝑛 = 2,3,4, … .. and
%

%

2&

%

%

2&

n𝑝12& + 𝑝 # + 𝑝 # o are zero divisors, so 𝑝1 − n𝑝12& + 𝑝 # + 𝑝 # o are units elements.
#

Following graph represent the number of zero divisors of $ for 𝑝 = 3, 5,7,11
!

ID : 617-0702/2024

## PDF page 7

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02

4. Conclusions
In conclusion, 𝑥 is space-like, time-like and light-like𝑁(𝑥) < 0, 𝑁(𝑥) > 0and 𝑁(𝑥) = 0 respectively.
As we discussed the idempotent, nilpotent and zero divisor in Cayley Dickson algebra over𝑍! , as in these
elements𝑁(𝑥). We also discuss unit elements such that 𝑥𝑥 - = 1. Interesting question is to extend the work
to spacelike, time like and light like for Cayley Dickson algebra for higher dimensions. Also, we can discuss
the graph in Cayley Dickson algebra regarding to idempotents, nilpotent and zero divisors as we discuss
the graph of unit elements in algebras of quaternion over𝑍! .
Data Availability Statement: The data supporting the findings of this study are available upon request from the
corresponding author. No publicly archived datasets were used or generated during the study.
Acknowledgments: The authors would like to acknowledge the technical support provided by [institution or lab
name] and the use of MATLAB for graphical representation. Additionally, they are grateful for the constructive
feedback received from their peers.
Conflicts of Interest: The authors declare no conflict of interest. The funders had no role in the design of the study, the
collection, analyses, or interpretation of data, the writing of the manuscript, or the decision to publish the results.

ID : 617-0702/2024

## PDF page 8

Journal of Computing & Biomedical Informatics

Volume 07 Issue 02

References
1. J. C. Baez, The octonions, Bull. Amer. Math. Soc. 39 (2002), 145-205. Errata in Bull. Amer. Math. Soc. 42 (2005), 213.
Corrected version available at math. A/0105155.
2. John H. Conway and Derek A. Smith on Quaternions and Octonions: Their Geometry, Arithmetic, and Symmetry
Bull. Amer. Math. Soc. 42 (2005), 229- 243.
3.
4.
5.
6.

7.
8.
9.

C. J. Miguel and R. Serodio, On the Structure of Quaternion Rings over , International Journal of Algebra, Vol.5,
27 (2011), 1313-1325
R. Remmert et all, Numbers, Springer, 1991
Muazzam Ali, Fahad Sabah and Abdul Manan, PONTE international scientific researches journal, august (2016)
issue 72 volume 8 (308-316).
Shin Min Kang, Mobeen Munir, Abdul Rauf Nizami, Muazzam Ali and Waqas Nazeer, On Elements of Split
Quaternions over
, Global Journal of Pure and Applied Mathematics, ISSN 0973-1768 Volume 12, Number 5
(2016), pp. 4253 - 4271.
S. Susumu, Okubo, Introduction to octonions and other non-associative algebras in Physics, University of
Cambridge, ISBN 0521 47215 6 1995.
B.C Chanyal, Octonion generalization of Pauli and Dirac matrices. International Journal of Geometric Methods in
Modern Physics World Scientific. 2015.
R.D. Schafer, An Introduction to No-associative Algebras, Academic Press, New York and London, 1966.

10. M. Aristidou and A. Demetre, A Note on Quaternion Rings over , International Journal of Algebra, Vol.3, 15
(2009), 725-728.
11. Tae-il Suh Algebras formed, The Zorn vector matrix, Pacific Journal of mathematics, Vol 30 No.1, 1969.
12. Michael Aristidou, A Note on Nilpotent Elements in Quaternion Rings over , International Journal of Algebra,
Vol.6, 14,(2012), 663-666.
13. N. J. Fine, I. N. Herstein, The Probability that a Matrix be Nilpotent, Illinois Journal of Mathematics, Vol.2 (1958),
No.4A, 499-504.
14. K. McCrimmon, A taste of Jordan Algebra, ISBN 0-387-95447-3, 2004 Springer Verlag. 15. R.B. Brown, N.C. Hopkins,
Noncommutative matrix Jordan Algebras, Transaction of the American mathematical society, Vol 333, Number1,
September 1992
15. Diesl, Alexander. "Sums of commuting potent and nilpotent elements in rings." Journal of Algebra and its
Applications 22.05 (2023): 2350113.
16. Flaut, C. and Baias, A., 2024. Some Remarks Regarding Special Elements in Algebras Obtained by the Cayley–
Dickson Process over Zp. Axioms, 13(6), p.351.
17. Grau, Jose Maria, Antonio M. Oller-Marcén, and Steve Szabo. "Minimal rings related to generalized quaternion
rings." International Electronic Journal of Algebra 34.34 (2023): 88-111.
18. Wang, G., Jiang, T., Vasil’ev, V.I. and Guo, Z., 2024. On singular value decomposition for split quaternion matrices
and applications in split quaternionic mechanics. Journal of Computational and Applied Mathematics, 436,
p.115447.
19. Ren, Guangbin, and Xin Zhao. "The Explicit Twisted Group Algebra Structure of the Cayley–Dickson
Algebra." Advances in Applied Clifford Algebras 33.4 (2023): 49.
20. Chapman, A., Guterman, A., Vishkautsan, S. and Zhilina, S., 2023. Roots and critical points of polynomials over
Cayley–Dickson algebras. Communications in Algebra, 51(4), pp.1355-1369.

ID : 617-0702/2024
