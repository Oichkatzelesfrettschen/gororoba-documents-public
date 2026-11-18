Source: https://doi.org/10.3390/mca21020020
PDF sha256: 619580af6c77afcb2a38aa51549eff723f468ffb101fb479e00aa7999149f004
License: cc-by
Language: eng
Fidelity: machine-gated

# Transcription of kayri_2016_bayesian_regularization_levenberg_marquardt_ann.pdf

Transcription of `kayri_2016_bayesian_regularization_levenberg_marquardt_ann.pdf` in this directory, 11 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-11 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Mathematical
and Computational
Applications

Article

Predictive Abilities of Bayesian Regularization and
Levenberg–Marquardt Algorithms in Artificial Neural
Networks: A Comparative Empirical Study on
Social Data
Murat Kayri
Department of Computer Engineering, Muş Alparslan University, 49100 Muş, Turkey; muratkayri@gmail.com;
Tel.: +90 436 213 00 13
Academic Editor: Mehmet Pakdemirli
Received: 8 March 2016; Accepted: 19 May 2016; Published: 24 May 2016

Abstract: The objective of this study is to compare the predictive ability of Bayesian regularization
with Levenberg–Marquardt Artificial Neural Networks. To examine the best architecture
of neural networks, the model was tested with one-, two-, three-, four-, and five-neuron
architectures, respectively. MATLAB (2011a) was used for analyzing the Bayesian regularization and
Levenberg–Marquardt learning algorithms. It is concluded that the Bayesian regularization training
algorithm shows better performance than the Levenberg–Marquardt algorithm. The advantage
of a Bayesian regularization artificial neural network is its ability to reveal potentially complex
relationships, meaning it can be used in quantitative studies to provide a robust model.
Keywords: Bayesian regularization; Levenberg–Marquardt; neural networks; training algorithms

1. Introduction
Defining a highly accurate model for quantitative studies depends on conditions such as the
distribution of variables, the number of predictors, and the complexity of interactions between
variables. Preventing the model from defining a bias and choosing a statistical method that is robust
and can solve complex relationships are also crucial. An Artificial Neural Network (ANN) is a popular
statistical method which can explore the relationships between variables with high accuracy [1–4].
Essentially, the structure of an ANN is computer-based and consists of several simple processing
elements operating in parallel [3,5,6].
An ANN consists of three layers: input, hidden, and output layers, hence it is referred to as a
three-layer network. The input layer contains independent variables that are connected to the hidden
layer for processing. The hidden layer contains activation functions and it calculates the weights of
the variables in order to explore the effects of predictors upon the target (dependent) variables. In the
output layer, the prediction or classification process is ended and the results are presented with a small
estimation error [7,8].
In general, a backpropagation algorithm trains a feedforward network. In the training process, the
backpropagation algorithm learns associations between a specified set of input-output pairs [9]. The
backpropagation training algorithm acts as follows [7]: first, it propagates the input values forward to
a hidden layer, and then, it propagates the sensitivities back in order to make the error smaller; at the
end of the process, it updates the weights. The mathematical frame of the backpropagation algorithm
can be seen in several studies such as “Training Feedforward Networks with the Marquardt Algorithm”
by [7]. Due to the limited word count, not all of the backpropagation algorithm is presented but it can
be seen in other studies.

Math. Comput. Appl. 2016, 21, 20; doi:10.3390/mca21020020

www.mdpi.com/journal/mca

## PDF page 2

Math. Comput. Appl. 2016, 21, 20

2 of 11

In ANNs, some regularization techniques are used with the backpropagation training algorithm
to obtain a small error. This causes the network response to be smoother and less likely to overfit to
training patterns [8,10]. However, the backpropagation algorithm is slow to converge and may cause
an overfitting problem. Backpropagation algorithms that can converge faster have been developed
to overcome the convergence issue. Similarly, some regularization methods have been developed to
solve the overfitting problem in ANNs. Among regularization techniques, Levenberg–Marquardt
(LM) and Bayesian regularization (BR) are able to obtain lower mean squared errors than any other
algorithms for functioning approximation problems [11]. LM was especially developed for faster
convergence in backpropagation algorithms. Essentially, BR has an objective function that includes a
residual sum of squares and the sum of squared weights to minimize estimation errors and to achieve
a good generalized model [3,12–15].
Basically, Multilayer Perceptron Artificial Neural Network (MLPANN) or Radial Basis Function
Artificial Neural Network (RBFANN) algorithms could be examined instead of BR or LM. However,
it’s known that BR and LM have better performance than the conventional methods (MLPANN,
RBFANN) in terms of both speed and the overfitting problem; as such, the aim was to explain BR
and LM algorithms for their use with social data and compare these algorithms in terms of their
predictive abilities. There are too few studies using an Artificial Neural Network with social data.
It should be considered that “linear-non-linear relationship” or “data type” varies from case to case.
While any architecture of neural network explains the model with small error or high accuracy for
continuous variable (natural-metric data such as weight, age, amount of electric consume, temperature,
humidity, etc.), maybe this architecture is not capable of explaining the model well for a non-linear
relation or non-continuous data. As it is seen that the study contains a lot of nominal and ordinal
variables (non-continuous), it is worth studying some artificial neural networks on social data due to
different behavior of distribution.
In this study, the training algorithms of BR and LM are compared in terms of predictive ability. To
compare their respective performances, the correlation coefficient between real and predicted data is
compared via BR and LM for performance criteria, along with the sum of squared errors, which can
also be a network performance indicator.
2. Material and Methods
2.1. Data Set (Material)
The data set was composed of 2247 university students. There are 25 variables (24 predictors
and one response) in the model. The score of the target (dependent) variable was obtained from a
reflective thinking scale. This is composed of 16 items and each item is measured by using a five-level
Likert scale (1: Strongly disagree; 2: Disagree; 3: Uncertain; 4: Agree; 5: Strongly agree). The aim of the
reflective thinking scale is to measure students’ reflective thinking levels and the score varies between
16 and 80. The reliability of reflective thinking was examined with Cronbach’s Alpha, and scored 0.792.
This value shows that the reliability level of the reflective thinking scale is good. The validity of the
scale was examined with principle component analysis (exploratory factor analysis) and the result of
this analysis was within an acceptable boundary.
In this study, 24 predictors given to the students via a prepared questionnaire were used. Some of
predictors were nominal (dichotomous or multinomial), some of them were ordinal, and the rest were
continuous variables. The predictors in the model were: “1—faculty (Education, Science, Engineering,
Divinity, Economics, Health)”, “2—gender”, “3—faculty department”, “4—the graduation of the
branch from high school (social, science, linguistics, etc.)”, “5—class in department (1/2/3/4)”, “6—the
preferred department order given at the University Entrance Examination”, “7—current transcript
score”, “8—completed preschool education (yes or no)”, “9—school type graduation (science, social,
divinity, vocational, etc.)”, “10—location when growing up (village, city, small town)”, “11—degree of
mother’s education (primary, middle, high school, university, etc.)”, “12—degree of father’s education

## PDF page 3

Math. Comput. Appl. 2016, 21, 20

3 of 11

Math. Comput. Appl. 2016, 21, 20

3 of 11

(primary, middle, high school, university, etc.)”, “13—monthly income of student’s family”, “14—level
of satisfaction with the department”, “15—frequency of reading a newspaper”, “16—newspaper
reading a newspaper”, “16—newspaper sections read”, “17—number of books read”, “18—types of
sections read”, “17—number of books read”, “18—types of book read (novel, psychological, science
book read (novel, psychological, science fiction, politic, adventure, etc.”, “19—consultation with
fiction, politic, adventure, etc.”, “19—consultation with environment (friends, etc.) on any argument
environment (friends, etc.) on any argument (always/generally/sometimes/never)”, “20—taking
(always/generally/sometimes/never)”, “20—taking notes during lesson regularly”, “21—discussion
notes during lesson regularly”, “21—discussion with environment (such as friend, roommate) on any
with environment (such as friend, roommate) on any issue (always/generally/sometimes/never)”,
issue (always/generally/sometimes/never)”, “22—any scientific research carried out yet (yes/no)”,
“22—any scientific research carried out yet (yes/no)”, “23—expected lesson’s details just from teacher
“23—expected lesson’s details just from teacher (yes/no)”, “24—research anxiety score” (this score
(yes/no)”, “24—research anxiety score” (this score was taken from the Research Anxiety Scale
was taken from the Research Anxiety Scale composed of 12 items). During analysis, the independent
composed of 12 items). During analysis, the independent variables are coded from 1 to 24 in order to
variables are coded from 1 to 24 in order to build readable tables.
build readable tables.

2.2. Methods
2.2. Methods
2.2.1. Feed-Forward
Neural Networks
Networks with
with Backpropagation
Backpropagation Algorithm
Algorithm
2.2.1.
Feed-Forward Neural
In feed-forward
feed-forward neural
neural networks,
networks, otherwise
otherwise known
multilayer perceptrons,
the input
input vector
vector
In
known as
as multilayer
perceptrons, the
of
independent
variables
p
i is related to the target ti (reflective thinking score) using the architecture
of independent variables pi is related to the target ti (reflective thinking score) using the architecture
depicted in
in Figure
Figure 1.
1. This
the commonly
commonly used
the layered
layered
depicted
This figure
figure shows
shows one
one of
of the
used networks,
networks, namely,
namely, the
feed-forward
neural
network
with
one
hidden
layer.
Here
each
single
neuron
is
connected
to
those
feed-forward neural network with one hidden layer. Here each single neuron is connected to those
of aa previous
previous layer
layer through
through adaptable
adaptable synaptic
synaptic weights
[3,16]. Knowledge
set
of
weights [3,16].
Knowledge is
is usually
usually stored
stored as
as aa set
of
connection
weights.
Training
is
the
process
of
modifying
the
network
using
a
learning
mode
in
of connection weights. Training is the process of modifying the network using a learning mode in
which
an
input
is
presented
to
the
network
along
with
the
desired
output,
and
then,
the
weights
are
which an input is presented to the network along with the desired output, and then, the weights
adjusted
so so
thatthat
thethe
network
attempts
toto
produce
training
are
adjusted
network
attempts
producethe
thedesired
desiredoutput.
output.The
The weights
weights after
after training
contain
meaningful
information,
whereas
before
training
they
are
random
and
have
no
meaning
contain meaningful information, whereas before training they are random and have no meaning [17].
[17].

Figure
of an
an artificial
artificial neural
neural network.
network.
Figure 1.
1. The
The architecture
architecture of
'

The architecture
architecture of
of the
the network
network examined
examined in
in the
the study
study was
wassuch
suchthat
thatp1pi= (p
= i1(p, i1p, i2p,i2,. .…,
i24))
The
. , ppi24
i
contained values
values for
The input
input variables
variables are
contained
for 24
24 input
input (independent)
(independent) variables
variables from
from individual
individual i.i. The
are
associated
with
each
of
N
neurons
in
a
hidden
layer
by
using
weights
(w
,
k
=
1,
2,
.
.
.
,
N)
which
are
associated with each of N neurons in a hidden layer by using weights (w
kjkj, k = 1, 2, …, N) which are
specific
Mackay (2008)
(2008) [18],
specific to
to each
each independent
independent variable
variable (j)
(j) to
to neuron
neuron (k)
(k) connection.
connection. Following
Following Mackay
[18], the
the
mapping has two forms for the relationship between output t̂ tˆand independent variables:
mapping has two forms for the relationship between output
and independent variables:
´
¯
p1(q1)
p
1
q
p
1
q
p1q
1)
1
R
HiddenLayer nnk “
w(kj
pj +
`bb(k1) ;; a1k “
f=
nnk (1)
(1)
w
p
a
f
=
Σ
level
´
one
j
“
1
(1)
j =1 kj
j
k
k
level − one k
HiddenLayer k

( )

OutputLayer

( )

nk( 2) = Σ j =1wk( 2,1) a1k + b1( 2) ; tˆi = ak( 2) = f level − two nk( 2)

(2)

## PDF page 4

Math. Comput. Appl. 2016, 21, 20

4 of 11

p2q

OutputLayer nk

p2,1q 1
p 2q
p2q
ak ` b1 ; t̂i “ ak “ f level ´two

“ Σ j“1 wk

p 1q

p1q

´

p 2q

¯

nk

(2)

p1q

In the case of N neurons in the neural network, the biases are b1 , b2 ........b N . Prior to activation,
24
ř
p 1q
the input value for neuron k is bk `
wkj p j . Then an activation function f (.) (linear or nonlinear)
j “1
˜
¸
´
¯
24
ř
p 1q
p1q
is applied to the input in each neuron and v is transformed as f k bk `
wkj p j = f k nk ,
j “1

k = 1, 2, ..., N. After applying
˜ activation, the¸activated quantity is then transferred to the output layer
N
24
ř
ř
p1q
and gathered as
w1k f k bk `
wkj p j ` bp2q , where wk (k = 1, 2, . . . , N) are b(1) and b(2) bias
ki“1

j “1

parameters in the hidden and output layers. At the end of the process, this activated quantity is carried
„ N
ȷ
´
¯
ř 1
p2q
out again with function g(.) as g
wk f k p.q ` bp2q = f k nk , which then becomes the estimated
k “1

target variable (reflective thinking score) value of ti in the training data set, or t̂i [3]:
!
´
¯
)
p 1q
t̂i “ g ΣkN“1 w1k f Σ Rj“1 wkj p j ` bk
` bp2q ; j “ 1, 2...., R k “ 1, 2, ..., N

(3)

In this study, the combination activation functions (f) used are
1
2

fhidden layer (.) = linear(.) and foutput layer (.) = linear(.)
fhidden layer (.) = tangentsigmoid(.) and foutput layer (.) = linear(.)

In this study, 70% of the organized data set was used for the training set and the rest (30%) of the
data set was used for the test set.
2.2.2. Solution to the Overfitting Problem with Bayesian Regularization and Levenberg–Marquardt
Neural Networks
The main problem with implementing regularization is setting the correct values for the objective
function parameters. The Bayesian framework for neural networks is based on the probabilistic
interpretation of network parameters. That is, in contrast to conventional network training where an
optimal set of weights is chosen by minimizing an error function, the Bayesian approach involves
a probability distribution of network weights. As a result, the predictions of the network are also a
probability distribution [19,20].
In the training process, a common performance function is used for computing the distance
between real and predicted data. This function can be expressed as follows:
n

F “ ED pD|w, Mq “

1ÿ
2
pt̂i ´ ti q
N

(4)

i “1

Here, ED is the mean sum of squares of the network error; D is the training set with input-target
pairs. M is a neural network architecture that consists of a specification of the number of layers, the
number of units in each layer, and the type of activation function performed by each unit. ED is a
criterion for early stopping to avoid overfitting; it is used in MATLAB for many training algorithms.
Therefore, early stopping for regularization seems to be a very crude method for complexity control [21].
However, although the early stopping regularization can reduce the variance it increases the bias. Both
can be reduced by BR [22].
In a BR network, the regularization adds an additional term and then an objective function to
penalize large weights that may be introduced in order to obtain smoother mapping. In this case, a
gradient-based optimization algorithm is preferred for minimizing the objective [15,18,23,24];
F = βED pD|w, Mq + αEW pw|Mq

(5)

## PDF page 5

Math. Comput. Appl. 2016, 21, 20

5 of 11

In Equation (5), EW (w|M) is EW “ n1

n
ř
i “1

w2j , the sum of squares of network weights, α and β, are

hyperparameters that need to be estimated function parameters. The last term, αEW (w|M), is called
weight decay and α is also known as the decay rate. If α << β then the training algorithm will make
the errors smaller. If α >> β, training will emphasize weight size reduction at the expense of network
errors, thus producing a smoother network response [25].
After the data are taken with the Gaussian additive noise assumed in target values, the posterior
distribution of the ANN weights can be updated according to Bayes’ rule:
Ppw|D, α, β, Mq “

PpD|w, β, Mq.Ppw|α, Mq
PpD|α, β, Mq

(6)

Therefore, the BR includes a probability distribution of network weights and the network
architecture can be identified as a probabilistic framework [19]. In Equation (6), D is the training
` α ˘m{2
␣
(
sample and the prior distribution of weights is defined as Ppw|α, Mq “ 2π
exp ´ α2 w1 w . M is
the particular ANN used and w is the vector of networks weights. P(w|α, M) states our knowledge of
weights before any data is collected, P(D|w, β, M) is the likelihood function which is the probability of
the occurrence, giving the network weights. In this Bayesian framework, the optimal weights should
maximize the posterior probability P(w|D, a, P, M). Maximizing the posterior probability of w is
equivalent to minimizing the regularized objective function F = βED + aEw [25]. Consider the joint
posterior density:
PpD|α, β, MqPpα, β|Mq
Ppα, β|D, Mq “
(7)
PpD|Mq
According to MacKay (1992) [10] it is
PpD|α, β, Mq “

ZF pα, βq
PpD|w, β, MqPpw|α, Mq
“
Ppw|D, α, β, Mq
pπ{βqn{2 pπ{αqm{2

(8)

where n and m are the number of observations and total number of network parameters, respectively.
The Equation (8) (Laplace approximation) produces the following equation;
ZF pα, βq9|HMAP |

´ 12

expp´Fpw MAP qq

(9)

where HMAP is the Hessian matrix of the objective function and MAP stands for maximum a posteriori.
The Hessian matrix can be approximated as
H “ J1 J

(10)

where J is the Jacobian matrix that contains first derivatives of the network errors with respect to
network parameters. J has
»
fi
B e1 p w q

— B w1
—
— B e2 p w q
—
J “ — B w1
—
..
—
.
–

B e N pwq
B w1

B e1 p w q
B w2
B e2 p w q
B w2

..
.

B e N pwq
B w2

¨¨¨
¨¨¨
..
.
¨¨¨

B e1 p w q
B wn
B e2 p w q
B wn

..
.

B e N pwq
B wn

ffi
ffi
ffi
ffi
ffi
ffi
ffi
fl

(11)

The Gauss-Newton approximation versus the Hessian matrix ought to be used if the LM algorithm
is employed to replace the minimum of F [26], an approach that was proposed by [10]. In LM, algorithm
parameters at l iteration are updated as
”
ı´1
wl `1 “ wl ´ JT J ` µI
JT e

(12)

## PDF page 6

Math. Comput. Appl. 2016, 21, 20

6 of 11

where µ is the Levenberg’s damping factor. The µ is adjustable for each iteration and leads to
optimization. It is a popular alternative to the Gauss-Newton method of finding the minimum of a
function [27].
2.2.3. Analyses
MATLAB (2011a) was used for analyzing the BR Artificial Neural Network (BRANN) and LM
Artificial Neural Network (LMANN). To prevent overtraining, develop predictive ability, and eliminate
superiors’ effects caused by the initial values, the algorithms of BRANN and LMANN were trained
independently 10 times. In this study, the training process is stopped if: (1) it reaches the maximum
number of iterations; (2) the performance has an acceptable level; (3) the estimation error is below the
target; or (4) the LM µ parameter becomes larger than 1010 .
3. Results and Discussion
Table 1 shows some estimated parameters of the network architectures. A number of parameters
for linear BRANN with one-neuron tangent sigmoid function can be seen.
Table 1. The number of effective parameters and correlation coefficients with linear Bayesian
Regularization Artificial Neural Network (BRANN) (one-neuron).
Cross-Validation
(CV)

Sum Square of
Errors (SSE)

Effective Number
of Parameters

Sum Squared
Weights (SSW)

R-Train
(Correlation)

R-Test
(Correlation)

1. sample
2. sample
3. sample
4. sample
5. sample
6. sample
7. sample
8. sample
9. sample
10. sample

61,372.000
53,387.000
55,915.000
60,031.000
51,190.000
53,843.000
61,012.000
61,888.000
55,574.000
60,606.000

22.300
22.200
25.100
22.200
22.100
22.200
21.700
22.200
22.100
22.600

0.312
0.332
0.251
0.316
0.329
0.289
0.269
0.283
0.339
0.333

0.263
0.261
0.252
0.270
0.261
0.271
0.260
0.278
0.272
0.220

0.232
0.236
0.252
0.225
0.243
0.222
0.220
0.217
0.231
0.213

Average of 10
samples

57,481.800

22.470

0.305

0.261

0.229

It is known that the Bayesian method performs shrinkage in order to estimate the model with
the least effective number of parameters. BRANN provides shrinkage by using a penalty term
(F = βED (D|w, M) + αEW (w|M)), thereby removing the unnecessary parameters. It is also known that
LM is unable to use a penalty term to estimate a model with the least number of parameters. Indeed,
using a penalty term for shrinkage is an important advantage of a Bayesian approach. As mentioned
before, the sample was divided into 10 sub-samples by using cross-validation and the valid result was
calculated by the average of 10 sub-samples. According to this, the effective number of parameters
is 22.470 with 0.305 sum of squared weights (SSW), and the correlation coefficient between real and
predicted responses is 0.229 for the test process (0.261 for the training process).
The model was tested as non-linear (with one-neuron, two-, three-, four-, and five-neurons) and
the results are shown in Table 2. The results were calculated as the averages of the cross-validation
samples (10 runs).
As shown in Table 2, the best model has a two-neuron architecture, with 0.2505 correlation
coefficient and with 34.48 parameters. In fact, the least effective number of parameters is found with a
slight difference in one-neuron architecture, but in this case the correlation coefficient is lower than in
the two-neuron architecture. Hence, the architecture with two-neurons is more acceptable than the
one-neuron architecture.

## PDF page 7

Math. Comput. Appl. 2016, 21, 20

7 of 11

Table 2. The effective number of parameter estimations and correlation coefficients with non-linear
BRANN.

Effective Number
R-Train
R-Test 7 of 11
SSW
of Parameters
(Correlation)
(Correlation)
1 neuron
57,689.3333
22.27
0.33118
0.2671
0.2296
Table
2.
The
effective
number
of
parameter
estimations
and
correlation
coefficients
with
2 neurons
57,541.400
34.48
0.8921
0.3044
0.2505
non-linear
BRANN.
3 neurons
58,103.300
44.68
1.6879
0.3432
0.2385
4 neurons
57,127.500
62.17
2.4836
0.3666
0.2367

Math.
Comput. Appl. 2016,SSE
21, 20
Architecture

Architecture

SSE

Effective Number of
Parameters

SSW

R-Train
(Correlation)

R-Test
(Correlation)

As
shown in 57,689.3333
Table 2, the best model
has a two-neuron
architecture,
with 0.25050.2296
correlation
1 neuron
22.27
0.33118
0.2671
coefficient
and with 34.48
parameters. In
fact, the least 0.8921
effective number of
parameters is0.2505
found with
2 neurons
57,541.400
34.48
0.3044
3 neurons
44.68
0.3432 coefficient is
0.2385
a slight
difference in58,103.300
one-neuron architecture,
but in this1.6879
case the correlation
lower than
4 neurons
57,127.500
62.17
2.4836
0.3666
0.2367
in the two-neuron architecture. Hence, the architecture with two-neurons is more acceptable than the
one-neuron architecture.
After examining
examining the
theBRANN
BRANNarchitecture,
architecture,the
theLM
LMtraining
training
algorithm
was
applied
to the
data
After
algorithm
was
applied
to the
data
set
set
and
the
results
of
the
LM
training
algorithm
are
shown
in
Table
3.
Just
the
average
results
of
and the results of the LM training algorithm are shown in Table 3. Just the average results of the
the
cross-validation
cross-validation samples
samples are
are given
given for
for simplicity.
simplicity.
Table
3. The
The
the correlation
coefficients
of different
architectures
LM
Table 3.
SSESSE
andand
the correlation
coefficients
of different
architectures
with thewith
LM the
training
training
algorithm.
algorithm.

Architecture
Architecture
1-neuron
linear
1-neuron
linear
1-neuron
non-linear
1-neuron
non-linear
2-neuron
non-linear
2-neuron
non-linear
3-neuron non-linear
3-neuron non-linear
4-neuron non-linear
4-neuron non-linear

SSE
SSE
57,545.600
57,545.600
58,512.200
58,512.200
59,707.700
59,707.700
62,106.200
62,106.200
63,180.800
63,180.800

R-Train
(Correlation)
(Correlation)
R-Train
(Correlation) R-Test
R-Test
(Correlation)
0.269
0.183
0.269
0.183
0.2789
0.2047
0.2789
0.2047
0.355
0.203
0.355
0.203
0.3968
0.1971
0.3968
0.1971
0.4446
0.1933
0.4446
0.1933

Table 33 shows
shows the
thecorrelation
correlationcoefficients
coefficientsofofthe
thetraining
training
and
test
processes
with
value
of
Table
and
test
processes
with
thethe
value
of the
the
sum
of
squared
errors
(SSEs).
The
highest
correlation
coefficient
(0.2047)
was
obtained
with
sum of squared errors (SSEs). The highest correlation coefficient (0.2047) was obtained with the onethe
one-neuron
architecture.
The correlation
coefficient
LM with
algorithm
the one-neuron
neuron
architecture.
The correlation
coefficient of
the LMof the
algorithm
the with
one-neuron
nonlinear
nonlinear
model
is
lower
than
BRANN’s
two-neuron
architecture
(0.2505
correlation
coefficient).
When
model is lower than BRANN’s two-neuron architecture (0.2505 correlation coefficient). When
comparing
Tables
2 2
andand
3 it3,is it is
clearly
seen seen
that the
the of the
LMANN
SSE is SSE
higher
comparing Tables
Tables11and
and3 3oror
Tables
clearly
thatvalue
the of
value
LMANN
is
than
the
BRANN
result
due
to
the
penalty
equation
since
the
LM
training
algorithm
cannot
use
it.
higher than the BRANN result due to the penalty equation since the LM training algorithm cannot
Although
the
LM
training
algorithm
aims
to
minimize
the
sum
of
mean
squared
errors
and
has
the
use it. Although the LM training algorithm aims to minimize the sum of mean squared errors and
fastest
convergence,
the BRANN
betterisinbetter
termsin
ofterms
predictive
ability. ability.
has
the fastest
convergence,
the result
BRANNisresult
of predictive
In
Table
4
and
Figure
2,
the
correlation
coefficients
are
summarized
see the
the predictive
predictive
In Table 4 and Figure 2, the correlation coefficients are summarized in
in order
order to
to see
ability
more
clearly.
ability more clearly.

Figure 2. The predictive ability of Bayesian regularization (BR), Levenberg–Marquardt (LM), and Scale
Conjugate Gradient (SCG).

## PDF page 8

Math. Comput. Appl. 2016, 21, 20

8 of 11

Table 4. The predictive ability of BR and LM.
Training
Algorithm

Linear

Nonlinear
(One-Neuron)

Nonlinear
(Two-Neuron)

Nonlinear
(Three-Neuron)

Nonlinear
(Four-Neuron)

BR
LM

0.229
0.183

0.23
0.205

0.251
0.203

0.239
0.197

0.237
0.193

Table 4 shows that BR has the best predictive ability for both linear and nonlinear architectures.
In this empirical study, a higher SSE and a lower correlation coefficient have been obtained by the LM.
Figure 2 shows that the optimal model can be defined with two-neuron architecture in BRANN. Due to
its predictive ability, using two-neuron architecture with BRANN was shown to be more reliable and
robust. So, for clarity of the findings, the importance of the predictors was tested just with BRANN,
not with LM.
Determining the importance of independent variables with the BR training algorithm is shown
in Table 5 where the effects of predictors are revealed according to priorities. The model was tested
with one-, two-, three-, four-, and five-neuron architectures. The connection weight matrix of the
neural network can be used to assess the relative importance of the various input neurons on the
output [28,29]. The relative importance of the predictors (input factors) was calculated as below.
řh

Ij “

`

p|Wji |{

řn

˘

k“1 |Wki |q.|WOi |
řn
řh
řn
k “ 1 t i “1 p|Wki |{ k “ 1 |Wki |q.|WOi |u
i“1

(13)

where Ij is the relative importance of the input factors j for the output, n is the number of input factors,
h is the number of hidden neurons, W is the synaptic weight matrix between the input and the hidden
layer, and WO is the synaptic weight matrix between the hidden and output layers [28,30].
Table 5. The relative importance of predictors with different architectures of BRANN.
Predictors Br_1neur.
24
16
7
4
6
12
10
17
8
2
9
15
22
3
5
18
13
19
14
21
20
11
1
23

0.075826
0.069195
0.060357
0.050891
0.050532
0.048386
0.047885
0.047311
0.047199
0.046716
0.043606
0.043048
0.041268
0.040365
0.039735
0.036124
0.035587
0.033427
0.032593
0.025644
0.025484
0.021935
0.020202
0.016684

Pred.

Br_2neur.

Pred.

Br_3neur.

Pred.

Br_4 neur.

Pred.

Br_5neur.

21
16
23
8
24
10
12
2
7
18
20
1
5
9
11
6
3
15
14
4
13
17
19
22

0.14369
0.11314
0.08125
0.07418
0.07294
0.06862
0.06106
0.05554
0.04651
0.04221
0.04074
0.03932
0.02792
0.02497
0.01811
0.01616
0.0148
0.01372
0.01176
0.00903
0.00885
0.00847
0.00538
0.00162

12
16
6
21
5
19
8
24
7
1
13
20
23
4
10
17
18
11
9
14
3
2
22
15

0.12251
0.07112
0.05684
0.05631
0.0556
0.05302
0.05076
0.04671
0.04425
0.04406
0.04253
0.04133
0.04024
0.03922
0.03784
0.03607
0.03285
0.02699
0.0256
0.02197
0.01687
0.01394
0.01239
0.01097

16
5
21
12
15
1
18
11
9
3
24
20
7
8
4
6
14
23
13
17
19
10
2
22

0.1111
0.09779
0.07807
0.07447
0.06365
0.05183
0.04997
0.04395
0.04257
0.03772
0.0376
0.03522
0.03193
0.02974
0.02808
0.02513
0.02483
0.02402
0.02075
0.02022
0.019
0.01868
0.01712
0.01656

5
24
11
12
4
1
9
6
20
16
14
18
13
8
3
2
15
19
22
23
21
17
10
7

0.10333
0.08138
0.06017
0.05692
0.05661
0.05389
0.04936
0.04713
0.04578
0.04452
0.04377
0.04253
0.03518
0.03504
0.03427
0.03183
0.03038
0.02815
0.02449
0.02403
0.02313
0.01958
0.01605
0.01249

Table 5 and Figure 3 show the relative importance of 24 input neurons upon the target for BR
models. According to the findings, there is no serious difference among architectures in terms of
predictive ability. The performance of the two-neuron architecture is slightly better, however, this
difference is not significant. A model that has a complex structure cannot be explained with a single

## PDF page 9

Math. Comput. Appl. 2016, 21, 20

9 of 11

neuron in terms of revealing the relationships between predictors and target. Since complex models
are penalized in accordance with the Bayesian approach, this approach is able to explore complex
architecture [3]. All in all, the model with two-neurons is the best architecture because of the highest
importance level of predictors. According to two-neuron architecture, the most important predictor is
“Taking notes during lesson regularly”, with a relative index of 14.36%. The other important predictors
are “Section being read from newspaper”, “Expected lesson’s details just from teacher”, “Completed
preschool education”, and “Research Anxiety Score”, as can be seen in Table 5. In the architecture
with three-, four-, and five-neurons, the relative indexes are lower than the two-neuron architecture.
Math.
Comput.the
Appl.
2016,model
21, 20 should be defined with two-neurons by using BRANN in this study. 9 of 11
Therefore,
best

Figure3.3.The
Therelative
relativeimportance
importanceof
ofpredictors
predictorswith
withdifferent
differentarchitectures,
architectures, with
with BRANN.
BRANN.
Figure

4. Conclusions
Table 5. The relative importance of predictors with different architectures of BRANN.
The objective
of this Pred.
work is to
demonstrate
predictive Pred.
abilitiesBr_4
of BR
and LM
neural
network
Predictors
Br_1neur.
Br_2neur.
Pred. theBr_3neur.
neur.
Pred.
Br_5neur.
training
algorithms.
The
ability
to
predict
reflective
thinking
in
the
data
was
employed
with
24
0.075826
21
0.14369
12
0.12251
16
0.1111
5
0.10333two
16
0.069195
16
0.11314
0.07112
0.09779
24both linear
0.08138and
different
backpropagation-based
algorithms 16
(BR and
LM). The 5
model was
tested as
7
0.060357
0.08125
0.07807
0.06017
nonlinear
for BR
and LM, 23
separately.
It was 6
observed0.05684
that the 21
relationship
between 11
input and
output
4
0.050891
8
0.07418
21
0.05631
12
0.07447
12
0.05692
neurons was nonlinear. To put the best nonlinear architecture forward, the model was tested with
6
0.050532
24
0.07294
0.0556
15
0.06365
0.05661
one-neuron
architecture,
two-, three-,
four-,5 and five-neuron
architectures.
The 4best model
was
12
0.048386
10
0.06862
19
0.05302
1
0.05183
1
0.05389
obtained according to the highest correlation coefficient between predicted and real data sets. The best
10
0.047885
12
0.06106
8
0.05076
18
0.04997
9
0.04936
model
was scrutinized
by BRANN
not only by
examining
the highest
correlation
but
also examining
17
0.047311
2
0.05554
24
0.04671
11
0.04395
6
0.04713
the least
number 7of parameters.
indicators of
architecture
the SSE
8 effective
0.047199
0.04651 The7 other0.04425
9 the best
0.04257
20 were
0.04578
and SSW
for
BRANN.
2
0.046716
18
0.04221
1
0.04406
3
0.03772
16
0.04452
Between the
BRANN20and LM
training 13
methods,
the BRANN
highest 0.04377
correlation
9
0.043606
0.04074
0.04253
24 obtained
0.0376 the 14
15
0.043048
0.03932
20
0.04133 The 20
0.03522
18 showed
0.04253
coefficient
and the
lowest 1
SSE in terms
of
predictive ability.
LM training
algorithm
lower
22
0.041268
5
0.02792
23
0.04024
7
0.03193
13
0.03518
performance in terms of predictive ability. Similarly, Okut et al. (2011) [3] proved that the BR training
3
9
0.02497 in terms
4
8
0.02974
8
0.03504
algorithm
was0.040365
the most effective
method
of0.03922
predictive ability.
5
0.039735
11
0.01811
10
0.03784
4
0.02808
3
0.03427
Okut et al. (2013) [24] investigated the predictive performance of BR and scale conjugate
gradient
18
0.036124
6
0.01616
17
0.03607
6
0.02513
2
0.03183
training algorithms. In their study, they found that the BRANN gave slightly better performance, but
13
0.035587
3
0.0148
18
0.03285
14
0.02483
15
0.03038
not significantly
so. In many
studies
[8,31–33],
the BR
training algorithm
has given19either0.02815
moderate
19
0.033427
15
0.01372
11
0.02699
23
0.02402
or the14best performance
in
terms
of
comparison
with
other
training
algorithms.
BRANNs
have
0.032593
14
0.01176
9
0.0256
13
0.02075
22
0.02449
some21
important
advantages,
choice 14
and robustness
model,0.02022
choice of 23
validation
set, size
0.025644
4 such as
0.00903
0.02197 of 17
0.02403
of 20
validation effort,
and 13
optimization
of network
architecture 19
[13]. Bayesian
solve the
0.025484
0.00885
3
0.01687
0.019 methods
21 can0.02313
11
0.021935
17 and0.00847
2
0.01394
0.01868 approach.
17
0.01958
overfitting
problem
effectively
complex models
are
penalized10
in the Bayesian
In contrast
1
0.020202
19
0.00538
22
0.01239
2
0.01712
10
0.01605
to conventional network training, where an optimal set of weights is chosen by minimizing
an error
23 the Bayesian
0.016684 approach
22
0.00162 a probability
15
0.01097
22 of network
0.01656 weights
7 [21,34].
0.01249
function,
involves
distribution

4. Conclusions
The objective of this work is to demonstrate the predictive abilities of BR and LM neural network
training algorithms. The ability to predict reflective thinking in the data was employed with two
different backpropagation-based algorithms (BR and LM). The model was tested as both linear and

## PDF page 10

Math. Comput. Appl. 2016, 21, 20

10 of 11

If data type (scale, nominal, ordinal) and distribution type of any data set is similar to the current
data set then it is expected to have close results. For social data, it is possible to generalize the BRANN
performance. Because Cross-Validation sampling enhances the findings and the sample was run many
times to generalize the findings, it is concluded that among learning algorithms mentioned in this
study, the BR training algorithm has shown better performance in terms of accuracy. This, combined
with its advantage of having the potential ability to capture nonlinear relationships, means it can be
used in quantitative studies to provide a robust model.
Conflicts of Interest: The author declares no conflict of interest.

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

Alaniz, A.Y.; Sanchez, E.N.; Loukianov, A.G. Discrete-time adaptive back stepping nonlinear control via
high-order neural networks. IEEE Trans. Neural Netw. 2007, 18, 1185–1195. [CrossRef] [PubMed]
Khomfoi, S.; Tolbert, L.M. Fault diagnostic system for a multilevel inverter using a neural network.
IEEE Trans Power Electron. 2007, 22, 1062–1069. [CrossRef]
Okut, H.; Gianola, D.; Rosa, G.J.M.; Weigel, K.A. Prediction of body mass index in mice using dense molecular
markers and a regularized neural network. Genet. Res. Camb. 2011, 93, 189–201. [CrossRef] [PubMed]
Vigdor, B.; Lerner, B. Accurate and fast off and online fuzzy ARTMAP-based image classification with
application to genetic abnormality diagnosis. IEEE Trans. Neural Netw. 2006, 17, 1288–1300. [CrossRef]
[PubMed]
Gianola, D.; Okut, H.; Weigel, K.A.; Rosa, G.J.M. Predicting complex quantitative traits with Bayesian neural
networks: A case study with Jersey cows and wheat. BMC Genet. 2011, 12, 1–37. [CrossRef] [PubMed]
Moller, F.M. A scaled conjugate gradient algorithm for fast supervised learning. Neural Netw. 1993, 6, 525–533.
[CrossRef]
Hagan, M.T.; Menhaj, M.B. Training feedforward networks with the Marquardt algorithm. IEEE Trans.
Neural Netw. 1994, 5, 989–993. [CrossRef] [PubMed]
Saini, L.M. Peak load forecasting using Bayesian regularization, Resilient and adaptive backpropagation
learning based artificial neural networks. Electr. Power Syst. Res. 2008, 78, 1302–1310. [CrossRef]
Beal, M.; Hagan, M.T.; Demuth, H.B. Neural Network Toolbox™ 6 User’s Guide; The Math Works Inc.: Natick,
MA, USA, 2010; pp. 146–175.
Mackay, D.J.C. Bayesian interpolation. Neural Comput. 1992, 4, 415–447. [CrossRef]
Demuth, H.; Beale, M. Neural Network Toolbox User’s Guide Version 4; The Math Works Inc.: Natick, MA, USA,
2000; pp. 5–22.
Bishop, C.M.; Tipping, M.E. A hierarchical latent variable model for data visualization. IEEE Trans. Pattern
Anal. Mach. Intell. 1998, 20, 281–293. [CrossRef]
Burden, F.; Winkler, D. Bayesian regularization of neural networks. Methods Mol. Biol. 2008, 458, 25–44.
[PubMed]
Marwalla, T. Bayesian training of neural networks using genetic programming. Pattern Recognit. Lett. 2007,
28, 1452–1458. [CrossRef]
Titterington, D.M. Bayesian methods for neural networks and related models. Stat. Sci. 2004, 19, 128–139.
[CrossRef]
Felipe, V.P.S.; Okut, H.; Gianola, D.; Silva, M.A.; Rosa, G.J.M. Effect of genotype imputation on
genome-enabled prediction of complex traits: an empirical study with mice data. BMC Genet. 2014,
15, 1–10. [CrossRef] [PubMed]
Alados, I.; Mellado, J.A.; Ramos, F.; Alados-Arboledas, L. Estimating UV erythemal irradiance by means of
neural networks. Photochem. Photobiol. 2004, 80, 351–358. [CrossRef] [PubMed]
Mackay, J.C.D. Information Theory, Inference and Learning Algorithms; University Press: Cambridge, UK, 2008.
Sorich, M.J.; Miners, J.O.; Ross, A.M.; Winker, D.A.; Burden, F.R.; Smith, P.A. Comparison of linear
and nonlinear classification algorithms for the prediction of drug and chemical metabolism by human
UDP-Glucuronosyl transferesa isoforms. J. Chem. Inf. Comput. Sci. 2003, 43, 2019–2024. [CrossRef] [PubMed]

## PDF page 11

Math. Comput. Appl. 2016, 21, 20

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
33.
34.

11 of 11

Xu, M.; Zengi, G.; Xu, X.; Huang, G.; Jiang, R.; Sun, W. Application of Bayesian regularized BP neural
network model for trend analysis. Acidity and chemical composition of precipitation in North. Water Air
Soil Pollut. 2006, 172, 167–184. [CrossRef]
Mackay, J.C.D. Comparison of approximate methods for handling hyperparameters. Neural Comput. 1996, 8,
1–35. [CrossRef]
Kelemen, A.; Liang, Y. Statistical advances and challenges for analyzing correlated high dimensional SNP
data in genomic study for complex. Dis. Stat. Surv. 2008, 2, 43–60.
Gianola, D.; Manfredi, E.; Simianer, H. On measures of association among genetic variables. Anim. Genet.
2012, 43, 19–35. [CrossRef] [PubMed]
Okut, H.; Wu, X.L.; Rosa, G.J.M.; Bauck, S.; Woodward, B.W.; Schnabel, R.D.; Taylor, J.F.; Gianola, D.
Predicting expected progeny difference for marbling score in Angus cattle using artificial neural networks
and Bayesian regression models. Genet. Sel. Evolut. 2013, 45, 1–8. [CrossRef] [PubMed]
Foresee, F.D.; Hagan, M.T. Gauss-Newton approximation to Bayesian learning. In Proceedings of the IEEE
International Conference on Neural Networks, Houston, TX, USA, 9–12 June 1997; pp. 1930–1935.
Shaneh, A.; Butler, G. Bayesian Learning for Feed-Forward Neural Network with Application to Proteomic
Data: The Glycosylation Sites Detection of The Epidermal Growth Factor-Like Proteins Associated with
Cancer as A Case Study. In Advances in Artificial Intelligence; Canadian AI LNAI 4013; Lamontagne, L.,
Marchand, M., Eds.; Springer-Verleg: Berlin/Heiddelberg, Germany, 2006.
Souza, D.C. Neural Network Learning by the Levenberg–Marquardt Algorithm with Bayesian Regularization.
Available online: http://crsouza.blogspot.com/feeds/posts/default/webcite (accessed on 29 July 2015).
Bui, D.T.; Pradhan, B.; Lofman, O.; Revhaug, I.; Dick, O.B. Landslide susceptibility assessment in the HoaBinh
province of Vieatnam: A comparison of the Levenberg–Marqardt and Bayesian regularized neural networks.
Geomorphology 2012, 171, 12–29.
Lee, S.; Ryu, J.H.; Won, J.S.; Park, H.J. Determination and application of the weights for landslide
susceptibility mapping using an artificial neural network. Eng. Geol. 2004, 71, 289–302. [CrossRef]
Pareek, V.K.; Brungs, M.P.; Adesina, A.A.; Sharma, R. Artificial neural network modeling of a multiphase
photo degradation system. J. Photochem. Photobiol. A Chem. 2002, 149, 139–146. [CrossRef]
Bruneau, P.; McElroy, N.R. LogD7.4 modeling using Bayesian regularized neural networks assessment and
correction of the errors of prediction. J. Chem. Inf. Model. 2006, 46, 1379–1387. [CrossRef] [PubMed]
Lauret, P.; Fock, F.; Randrianarivony, R.N.; Manicom-Ramsamy, J.F. Bayesian Neural Network approach to
short time load forecasting. Energy Convers. Manag. 2008, 5, 1156–1166. [CrossRef]
Ticknor, J.L. A Bayesian regularized artificial neural network for stock market forecasting. Expert Syst. Appl.
2013, 14, 5501–5506. [CrossRef]
Wayg, Y.H.; Li, Y.; Yang, S.L.; Yang, L. An in silico approach for screening flavonoids as P-glycoprotein
inhibitors based on a Bayesian regularized neural network. J. Comput. Aided Mol. Des. 2005, 19, 137–147.
© 2016 by the author; licensee MDPI, Basel, Switzerland. This article is an open access
article distributed under the terms and conditions of the Creative Commons Attribution
(CC-BY) license (http://creativecommons.org/licenses/by/4.0/).
