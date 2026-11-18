Source: see manifest row of the PDF
PDF sha256: 360effa663c6fa6a52a8b023f55a059becef4e3c204ac35741049c5854fe398e
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of hsieh_2024_fault_detection_in_harmonic_drive_using_multi_sensor_data_fusion_and_gravitational_search_algorithm.pdf

Transcription of `hsieh_2024_fault_detection_in_harmonic_drive_using_multi_sensor_data_fusion_and_gravitational_search_algorithm.pdf` in this directory, 15 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-15 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

Fault Detection in Harmonic Drive Using Multi-Sensor Data
Fusion and Gravitational Search Algorithm
Nan-Kai Hsieh 1

and Tsung-Yu Yu 2,3, *
1

2

3

*

Department of Automatic Control Engineering, Feng Chia University, Taichung City 407, Taiwan;
nkhsieh@fcu.edu.tw
Ph.D. Program of Electrical and Communications Engineering, Feng Chia University,
Taichung City 407, Taiwan
Department of Computer Science and Information Engineering, National Taichung University of Science and
Technology, Taichung 411030, Taiwan
Correspondence: karlyu@nutc.edu.tw

Abstract: This study proposes a fault diagnosis method for harmonic drive systems based on multisensor data fusion and the gravitational search algorithm (GSA). As a critical component in robotic
arms, harmonic drives are prone to failures due to wear, less grease, or improper loading, which can
compromise system stability and production efficiency. To enhance diagnostic accuracy, the research
employs wavelet packet decomposition (WPD) and empirical mode decomposition (EMD) to extract
multi-scale features from vibration signals. These features are subsequently fused, and GSA is used to
optimize the high-dimensional fused features, eliminating redundant data and mitigating overfitting.
The optimized features are then input into a support vector machine (SVM) for fault classification,
with K-fold cross-validation used to assess the model’s generalization capabilities. Experimental
results demonstrate that the proposed diagnosis method, which integrates multi-sensor data fusion
with GSA optimization, significantly improves fault diagnosis accuracy compared to methods using
single-sensor signals or unoptimized features. This improvement is particularly notable in multi-class
fault scenarios. Additionally, GSA’s global search capability effectively addresses overfitting issues
caused by high-dimensional data, resulting in a diagnostic model with greater reliability and accuracy
across various fault conditions.
Citation: Hsieh, N.-K.; Yu, T.-Y. Fault
Detection in Harmonic Drive Using

Keywords: fault diagnosis; harmonic drive; gravitational search algorithm (GSA)

Multi-Sensor Data Fusion and
Gravitational Search Algorithm.
Machines 2024, 12, 831. https://
doi.org/10.3390/machines12120831
Academic Editors: Hongrui Cao and
Ahmed Abu-Siada
Received: 10 October 2024
Revised: 13 November 2024
Accepted: 20 November 2024
Published: 21 November 2024

Copyright: © 2024 by the authors.
Licensee MDPI, Basel, Switzerland.
This article is an open access article
distributed under the terms and
conditions of the Creative Commons
Attribution (CC BY) license (https://
creativecommons.org/licenses/by/
4.0/).

1. Introduction
With the rapid development of industrial automation and the ever-growing demand
for efficiency [1], many companies have introduced robotic arms to achieve automated production, further accelerating the demand for these systems. In the fields of manufacturing
and precision machining, the application of robotic arms has become increasingly vital,
particularly in enhancing production efficiency, precision, and stability. At the core of these
systems is the harmonic drive, a key component that enables the realization of such goals.
Harmonic drives, known for their high reduction ratios, high torque, and precision, are
widely used in various joints of robotic arms, playing a critical role in improving overall
system performance. Their integration into robotic systems has significantly boosted the
capabilities and reliability of automated processes in industries where accuracy and stability
are paramount.
As mechanical equipment operates for extended periods, factors such as wear and
tear or improper human operation gradually increase the risk of unexpected failures. Andrea et al. [2] summarized common failure types in rotating machinery, identifying issues
such as improper loading, insufficient lubrication, gear wear, and tooth breakage. These
failures not only reduce the operational efficiency of robotic arms but can also lead to
financial losses during production and even cause severe industrial safety incidents. To

Machines 2024, 12, 831. https://doi.org/10.3390/machines12120831

https://www.mdpi.com/journal/machines

## PDF page 2

Machines 2024, 12, 831

2 of 15

improve the reliability and stability of rotating machinery, various novel fault diagnosis
methods have been proposed in recent years [3,4]. Common fault detection techniques
for rotating machinery include vibration analysis [5,6], current monitoring [7–9], noise
detection [10], and temperature monitoring [11,12]. Currently, most existing research remains focused on using single-sensor signals, such as vibration or current signals, for
fault diagnosis. While these methods have achieved some success in single-fault mode
scenarios, the increasing complexity of mechanical systems has exposed the limitations of
single-sensor approaches. Specifically, they struggle to fully capture the intricate features
present in multiple fault modes, leading to a decline in diagnostic accuracy. To address
this issue, multi-sensor signal fusion technologies [13,14] have recently been applied in
the field of fault diagnosis, yielding significant advancements, particularly in detecting
issues like bearing defects and insufficient lubrication [15–18]. Multi-sensor fusion can
effectively enhance diagnostic accuracy and reliability, providing more comprehensive
diagnostic information for mechanical fault detection. However, extracting useful faultrelated features from these multi-source signals remains a critical challenge. To overcome
this, various signal processing methods have been developed to extract key features from
complex mechanical vibration signals. Common frequency-domain analysis methods, such
as Fourier transform (FT) [19] and time-frequency analysis (TFA) [20] methods, including
wavelet transform (WT) [21], wavelet packet decomposition (WPD), empirical mode decomposition (EMD) [22], empirical wavelet transform (EWT) [23], and discrete wavelet
transform (DWT) [24], have been widely used in fault diagnosis for mechanical systems,
demonstrating their efficacy in detecting defects in critical components like bearings [25,26]
and gears [27]. Through these methods, potential faults in harmonic drives can be more
accurately identified and predicted, enabling computation time condition monitoring (CM)
and fault detection and diagnosis (FDD) for robotic arms [28,29]. Although multi-sensor
fusion provides more dimensions of diagnostic information, it also poses several challenges
in practical applications. First, the feature shape and scale inconsistency between different
sensor signals may lead to imbalance issues during data fusion, potentially affecting model
performance. Additionally, the increased number of features results in high-dimensional
data, raising computational complexity. If the selected features during the fusion process
fail to represent the fault modes accurately, noise could be introduced, thus reducing diagnostic accuracy. Therefore, choosing appropriate feature extraction methods is crucial for
overcoming these challenges.
Therefore, WPD and EMD were selected for multi-level feature extraction from vibration signals, as both methods excel in handling non-stationary signals and can extract
fault-related high-frequency and low-frequency features across different frequency domains [30–32]. To enhance diagnostic accuracy, we utilized the gravitational search algorithm (GSA) [33–35] to optimize the fused features, capitalizing on its distinct advantages
for this application. GSA models the behavior of masses under gravitational attraction,
where solutions with better fitness attract others, facilitating a rapid and effective convergence toward the global optimum. This process makes GSA particularly adept at handling
high-dimensional and complex datasets, as it efficiently explores vast solution spaces without becoming trapped in local optima. Its capacity to dynamically adjust search parameters
based on fitness ensures reliable feature optimization, making it a highly effective choice for
enhancing diagnostic accuracy and computational efficiency in fault detection tasks [36,37].
Initially, WPD and EMD were used to extract multi-level features from vibration signals,
followed by feature fusion, and the fused features were then optimized using GSA. The
optimized features were input into a machine-learning model, significantly improving
fault diagnosis accuracy [38,39]. This approach effectively addresses redundant features
and feature inconsistency issues during the fusion process and demonstrates superior
performance in fault diagnosis. The contributions of this paper are as follows:
1.

The proposed method integrates feature fusion with GSA optimization. By fusing decomposed features and applying optimization, we demonstrate through experiments
that the method effectively reduces overfitting in high-dimensional data. Furthermore,

## PDF page 3

Machines 2024, 12, 831

experiments that the method eﬀectively reduces overfitting in high-dimensional
data. Furthermore, by optimizing feature selection, it eliminates the interference
3 of of
15
redundant features, significantly improving diagnostic accuracy across multiple fault
modes.
2. Multi-sensor
vibration
data of harmonic
drivesthe
were
collected of
under
variousfeatures,
operatby optimizing
feature selection,
it eliminates
interference
redundant
ing
conditions.
It
was
verified
that
the
diagnostic
model,
after
feature
fusion
and
GSA
significantly improving diagnostic accuracy across multiple fault modes.
optimization,
achieved
significantly
higher
accuracy
compared
to
models
using
only
2.
Multi-sensor vibration data of harmonic drives were collected under various operating
data
fusion. It was verified that the diagnostic model, after feature fusion and GSA
conditions.
3. The
experimental
results show
that the
feature
fusion
methods
FEMD
optimization,
achieved
significantly
higher
accuracy
compared
toFWPD
modelsand
using
only
improved
the accuracy and stability of fault diagnosis. After applying GSA for feadata
fusion.
FWPD+GSA
combination
a high diagnostic
accuracy.
3. ture
The optimization,
experimentalthe
results
show that
the featureachieved
fusion methods
FWPD and
FEMD
improved the
accuracy
and deep
stability of
fault [42–45],
diagnosis.
After
applying
GSA for
Machine
learning
[9,40,41],
learning
and
transfer
learning
[46]feature
have
optimization,
FWPD+GSA
combination
achieved a
high and
diagnostic
accuracy.
shown
remarkable the
potential
in advancing
fault diagnosis
accuracy
adaptability
across
diﬀerent
datasets
and systems.
These
oﬀer
enhanced
precision in
identifying
nuMachine
learning
[9,40,41],
deepmethods
learning
[42–45],
and transfer
learning
[46] have
anced
features and
allow
to fault
generalize
eﬀectively
across
conditions,
shownfault
remarkable
potential
in models
advancing
diagnosis
accuracy
and varied
adaptability
across
making
essential
in These
predictive
maintenance
equipment
health
managedifferentthem
datasets
and tools
systems.
methods
offer and
enhanced
precision in
identifying
nuanced
fault features
and allow
models to
generalize
effectively
across
variediagnosis.
conditions,
ment.
Currently,
there are
numerous
diagnostic
methods in
the field
of fault
It
making
themthat
essential
infusion,
predictive
maintenance
and
equipment
healthcan
management.
is
proposed
after tools
feature
combining
it with
GSA
optimization
eﬀectively
Currently,
are numerous
diagnostic
methods
in and
the field
of fault
diagnosis.drive
It is
extract
keythere
features,
thereby improving
the
accuracy
reliability
of harmonic
proposed
that after
featurethe
fusion,
combining
with
optimization
can
effectively
fault
diagnosis.
Moreover,
proposed
methoditcan
be GSA
eﬀectively
applied in
fault
predicextract
key
features, health
thereby improving
theThe
accuracy
and of the
reliability
of is
harmonic
drive
tion
and
equipment
management.
structure
paper
presented
asfault
foldiagnosis.
Moreover,
the the
proposed
can be
effectively
in fault
prediction
lows:
Section 2
introduces
fault method
diagnosis
framework
we applied
employed,
which
includes
and
equipment
structure
of the
presented asSection
follows:
EMD and
WPD health
signal management.
decomposition,The
feature
fusion,
andpaper
GSA is
optimization.
3
Section
2
introduces
the
fault
diagnosis
framework
we
employed,
which
includes
EMD
and
discusses the experimental setup for fault diagnosis. Section 4 presents the fault diagnosis
WPD signal decomposition,
feature
fusion, and
GSA optimization.
Section
3 discusses
the
experiments
used to evaluate
the proposed
method.
Finally, Section
5 provides
the conexperimental
setup
for
fault
diagnosis.
Section
4
presents
the
fault
diagnosis
experiments
clusion.
used to evaluate the proposed method. Finally, Section 5 provides the conclusion.
2. Enhanced Harmonic Drive Fault Diagnosis Framework
2. Enhanced Harmonic Drive Fault Diagnosis Framework
Five types of faults were established for harmonic drives in this research, including
Five types of faults were established for harmonic drives in this research, including
improper load (IL), less grease (LG), gear wear (GW), bearing damage (B), and gear fracimproper load (IL), less grease (LG), gear wear (GW), bearing damage (B), and gear fracture
ture (GF). The research applied WPD and EMD, combined with data fusion techniques,
(GF). The research applied WPD and EMD, combined with data fusion techniques, to
to enrich the diversity of features in fault diagnosis. GSA was then used to obtain optienrich the diversity of features in fault diagnosis. GSA was then used to obtain optimized
mized features, further enhancing the X- and Y-axes vibration signals. Finally, machine
features, further enhancing the X- and Y-axes vibration signals. Finally, machine learning
learning was employed for fault classification (Figure 1).
was employed for fault classification (Figure 1).

Figure 1.
1. Enhanced
Enhanced harmonic
harmonic drive
drive fault
fault diagnosis
diagnosis framework
framework diagram.
diagram.
Figure

1.
1.
2.
3.
2.

The research process is divided into three main stages:
The research process is divided into three main stages:
Signal processing stage, where signal decomposition is performed using WPD and EMD.
Signal processing stage, where signal decomposition is performed using WPD and
Data fusion and optimized feature extraction stage.
EMD.
Classifier training stage, where the feature dataset is evaluated using a support vector
Data
fusion
and optimized
feature
extraction
stage.
machine
(SVM)
combined with
K-fold
cross-validation

First, vibration signals along the X- and Y-axes were collected using accelerometers.
To extract key fault features, WPD and EMD signal decomposition methods were employed to obtain decomposed features, which were then fused for both the X- and Y-axes.
Subsequently, GSA was used to optimize the vibration features. After signal decomposi-

## PDF page 4

machine (SVM) combined with K-fold cross-validation

Machines 2024, 12, 831

First, vibration signals along the X- and Y-axes were collected using accelerometers.
To extract key fault features, WPD and EMD signal decomposition methods were employed to obtain decomposed features, which were then fused for both the X- and Y-axes.
Subsequently, GSA was used to optimize the vibration features. After signal decomposi4 of 15
tion, the fused features from the X- and Y-axes were optimized using GSA, resulting in
optimized features. These optimized features could then be used for model training and
fault
diagnosis.
tion, the
fused features from the X- and Y-axes were optimized using GSA, resulting in
×
During the
signal
decomposition
analysis
process,
𝐷 ∈
represent
optimized
features.
These
optimized and
features
could then
belet
used
forℝmodel
training the
and
raw
faultvibration
diagnosis.signals, where 𝑁 denotes the number of samples and 𝐿 denotes the
× N represent
During
thesample
signal in the
decomposition
analysis
Dv ∈
R Lv
the
length of
each
vibrationand
signal.
The process,
signals let
were
then
subjected
to proraw
vibration
signals, where
N denotes the number of samples and Lv denotes the length
cessing
and analysis
accordingly.
of each sample in the vibration signal. The signals were then subjected to processing and
analysis
2.1.
Signalaccordingly.
Processing Stage
2.1.1. Feature Extraction Using WPD
2.1. Signal Processing Stage
raw vibration
signals
nonlinear in nature, making it diﬃcult to rely solely on
2.1.1.The
Feature
Extraction
Usingare
WPD
a single vibration signal for fault diagnosis. Therefore, feature extraction is a necessary
The raw vibration signals are nonlinear in nature, making it difficult to rely solely on
and critical step in the fault diagnosis process. In this study, WPD is applied to the fault
a single vibration signal for fault diagnosis. Therefore, feature extraction is a necessary
diagnosis of harmonic drives. By decomposing the signals into components of diﬀerent
and critical step in the fault diagnosis process. In this study, WPD is applied to the fault
frequencies, WPD reveals the time-frequency characteristics of the signals. The goal is to
diagnosis of harmonic drives. By decomposing the signals into components of different
extract key fault features from both high-frequency and low-frequency signals.
frequencies, WPD reveals the time-frequency characteristics of the signals. The goal is to
When a raw signal is decomposed using WPD up to the third level, it is divided into
extract key fault features from both high-frequency and low-frequency signals.
2, 4, and 8 nodes in the first, second, and third layers, respectively. The wavelet packet
When a raw signal is decomposed using WPD up to the third level, it is divided into
decomposition
coeﬃcients within each node contain diverse fault-related information
2, 4, and 8 nodes in the first, second, and third layers, respectively. The wavelet packet
across
diﬀerent
(both
high
and
low frequencies),
as shown information
in Figure 2.
decomposition frequency
coefficientsbands
within
each
node
contain
diverse fault-related
Additionally,
diﬀerent
decomposition
levels
varying
information
related
faults.2.
across different
frequency
bands (both
highcontain
and low
frequencies),
as shown
into
Figure
Relying
solely
on
the
wavelet
decomposition
at
a
single
level
to
extract
features
makes
it
Additionally, different decomposition levels contain varying information related to faults.
challenging
to
determine
which
level
contains
the
most
valuable
information,
and
it
is
Relying solely on the wavelet decomposition at a single level to extract features makes
diﬃcult
to capture
the fault characteristics
of the signal
fully.
Therefore,
to extractand
richer
it challenging
to determine
which level contains
the most
valuable
information,
it is
fault
information,
it
is
essential
to
derive
vibration
signal
features
from
diﬀerent
levels
of
difficult to capture the fault characteristics of the signal fully. Therefore, to extract richer
WPD. The
steps forit is
WPD
featureto derive
extraction are
described
follows:
Step 1:
Use WPD
fault
information,
essential
vibration
signal as
features
from
different
levelstof
decompose
vibration
obtain are
wavelet
packetas follows:
decomposition
coeﬃcients
WPD.
The the
steps for
WPDsignal
featureand
extraction
described
Step 1: Use
WPD at
to
diﬀerent
decomposition
levels.
Each
level
of
WPD
is
denoted
by
𝑑
𝑛
,
where
𝑖
repre,
decompose the vibration signal and obtain wavelet packet decomposition coefficients at
sents
a node
at a specific levels.
level, 𝑗Each
represents
high
or low
within
different
decomposition
level ofthe
WPD
is (H)
denoted
by(L)
di,jfrequency
i represents
[n], where part
each
node,
and
𝑛
indicates
the
signal
components
contained
in
each
node.
Step
2:each
For
a node at a specific level, j represents the high (H) or low (L) frequency part within
each
decomposition
level,
wavelet packet
decomposition
coeﬃcients
ofeach
the
node, and [
n] indicates
thecalculate
signal the
components
contained in
each node. Step
2: For
raw signal
for each
node.
Therefore,
thepacket
maximum
decomposition
level 𝑁,ofthe
decomposition
level,
calculate
the with
wavelet
decomposition
coefficients
thetotal
raw
numberforofeach
features
signal
sample
be computed
as (2level
+ 2N,+the
2 +
2 +
⋯+
signal
node. for a
Therefore,
with
the can
maximum
decomposition
total
)number
0
1
2
3
N
2of)features
× 1.
for a signal sample can be computed as (2 + 2 + 2 + 2 + · · · + 2
× 1.

Figure 2. Three-layered wavelet packet decomposition process diagram.

2.1.2. Feature Extraction Using EMD
The decomposition process of EMD begins by detecting the local maxima and minima
(negative peaks) within the signal. Then, interpolation is performed on the detected
maxima and minima to obtain the upper and lower envelopes of the signal waveform.
Afterward, the instantaneous mean line at each time point is calculated from the upper and
lower envelopes. By subtracting the instantaneous mean from the signal waveform and

## PDF page 5

Machines 2024, 12, 831

5 of 15

repeating this process, the decomposition continues until the conditions for an intrinsic
mode function (IMF) are satisfied. The steps for feature extraction using empirical mode
decomposition (EMD) are described as follows: Step 1: Identify all the local maxima and
minima of the raw vibration signal Dv (t). Using cubic spline function interpolation, fit the
upper envelope emax (t) based on the maxima and the lower envelope emin (t) based on the
minima. The mean of the upper and lower envelopes, m1 (t), is then calculated as shown in
Equation (1):
emax (t) + emin (t)
m1 ( t ) =
(1)
2
Step 2: Identify the components of the IMF by ensuring that two conditions are met
for the IMF definition. After satisfying these conditions, subtract the mean m1 (t) from the
original vibration signal sequence Dv (t) to obtain a new signa p11 (t), which removes the
low-frequency component. This is represented by Equation (2):
p11 (t) = Dv (t) − m1 (t)

(2)

If Equation (2) does not meet the two conditions for the definition of an IMF after the
first iteration, additional iterations are performed. After k iterations, if the conditions of
the IMF are satisfied, the first-order IMF component of the original vibration signal can be
expressed as shown in Equation (3):
c1 (t) = I MF1 (t) = p1k (t)

(3)

By subtracting the first IMF component c1 (t) from the original vibration signal sequence, the new signal r11 (t), which has removed the high-frequency component, can be
obtained. This is represented by Equation (4):
r11 (t) = Dv (t) − c1 (t)

(4)

After iterating Equation (4), the process continues until rn (t) becomes a constant. The
original vibration signal can then be decomposed using EMD and expressed as follows in
Equation (5):
n

Dv ( t ) = ∑ c i ( t ) + r n ( t )

(5)

i =1

2.1.3. Comparison of Time Complexity for Signal Processing Methods
In the signal processing stage, two different signal decomposition methods were
selected: WPD and EMD. Each method has its strengths and weaknesses in the feature
extraction process, and the differences in their time complexities directly affect the computational efficiency of the overall system.

•

•

WPD: The time complexity of WPD is O( NlogN ), where N is the length of the signal. Since wavelet decomposition involves multi-level frequency decomposition, this
method is computationally efficient for processing long-duration signals, making it
suitable for multi-scale signal analysis.
EMD: The time complexity of EMD is ( TEMD · N ), where TEMD represents the number of EMD iterations, and N represents the signal length. Because EMD relies on
repeated interpolation of the signal’s local maxima and minima, the computational
load increases significantly as the complexity of the signal rises. This results in EMD
having a higher time complexity compared to WPD, particularly when dealing with
more intricate signals.

2.2. Feature Signal Enhancement Stage
After the original vibration signal Dv ∈ R Lv × N undergoes feature extraction using
WPD and EMD, the resulting vibration decomposition features are denoted as Wv ∈ RDv × N .

## PDF page 6

Machines 2024, 12, 831

6 of 15

2.2.1. Data Fusion
After feature extraction, the X-axis and Y-axis vibration decomposition features are
represented as Wv ∈ RDv × N X and Wv ∈ RDv × N Y , respectively. In this stage, a direct concatenation method is employed to perform multi-sensor data fusion. This process results in
a new high-dimensional fused vibration feature Fv ∈ RDv × N Z , as shown in Equation (6):

Fv ∈ RDv × N Z = Wv ∈ RDv × N X

⨁

Wv ∈ RDv × N Y

(6)

When extending Equation (6) to accommodate k sensors, the fused vibration feature
becomes a concatenation of the decomposition features from all k sensors. This can be
expressed as shown in Equation (7):

Fv ∈ RDv × N Z = Wv ∈ RDv × N X_1

⨁

Wv ∈ RDv × N X_2 · · ·

⨁

Wv ∈ RDv × N X ∈ R(n1+n2+···+nk)× N

(7)

2.2.2. Gravitational Search Algorithm
After obtaining the fused vibration features Fv ∈ RDv × N , GSA is used to optimize
the features. In the GSA optimization process, each solution is considered a mass-bearing
object, and the entire set of solutions forms a system of objects that attract each other in
the search space. The mass of each solution is determined by its fitness function value: the
higher the fitness, the greater the mass. The solutions attract each other based on the laws
of gravity, and this gravitational force guides the movement and dynamics of the solutions
during the search process. In summary, GSA offers three major advantages in this study:
(1) Global Search Capability: GSA is designed based on the laws of gravity, which allows
for global exploration within the search space. This helps to avoid being trapped in local
optima and increases the likelihood of finding the global optimum solution. (2) Adaptive
Search Behavior: GSA dynamically adjusts parameters such as gravitational constant and
acceleration, which enhances the optimization efficiency. For instance, applying GSA to the
vibration decomposition features Fv ∈ RDv × N , the mass function of the i-th vibration fusion
feature in the t-th iteration, 𝒻vM i (t), is given by Equation (8). (3) Key Parameters in GSA:
Two critical parameters in GSA, the initial gravitational value G0 and the decay coefficient α,
play an essential role in the algorithm’s performance. As time progresses, the gravitational
value decreases according to Equation (13), which indicates that the gravitational force is
larger in the early stages, facilitating stronger global search capabilities. As the number
of iterations increases, the gravitational value gradually decreases, helping the algorithm
perform finer local searches in later stages. This design effectively prevents the algorithm
from prematurely converging to a local optimum during the global search phase and
maintains stability throughout the convergence process.
𝒻vM i (t) =

qi ( t ) =

qi ( t )
N
∑ j =1 q j ( t )

f iti (t) − worst(t)
best(t) − worst(t)

(8)

(9)

The mass function for the i-th solution is given in Equation (9), where best and worst
represent the highest and lowest fitness values, respectively, in the current iteration. This
helps in determining the relative importance of each solution in the search process. The
fitness function is calculated as shown in Equation (10):
n (
)2
f it( x ) = ∑ xi − x j

(10)

i̸= j

In this method, xi and x j represent two neighboring points in the same space. The
squared distance between these two points is considered as the fitness function. The goal

## PDF page 7

Machines 2024, 12, 831

7 of 15

of using the squared distance is to amplify small differences, which helps in separating
classes. Next, the gravitational force is calculated as shown in Equation (11):
𝒻v _Fijd (t) = G (t)

𝒻v _Mi (t)𝒻v _M j (t) d
( x j (t) − xid (t))
Rij (t) + ε

(11)

where G(t) is the gravitational constant that decreases over time; Rij (t) is the Euclidean distance
between i and j. ε is a small constant to avoid division by zero; and i, j ∈ {1, 2, 3, . . . , N }
and i ̸= j, with d = 1, 2, 3, . . . , D represent the d-th dimension of the vibration feature.
The force exerted on the i-th individual along the d-th dimension at iteration t is given by
Equation (12):
𝒻v _Fid (t) =

N

∑

rand j Fijd (t)

(12)

j∈k best , j̸=i

To reduce the time complexity caused by the high dimensionality during fusion,
we adapt the gravitational constant G (t) in Equation (10) to an adaptive gravitational
calculation to save computational resources, as shown in Equation (13):
(
)
t
G (t) = G0 ·exp −α·
(13)
Tmax
G (t) is the gravitational constant at iteration t-th; G0 is the initial gravitational constant
(a positive constant); α is the gravitational decay factor; t is the current iteration number;
and Tmax and is the maximum number of iterations.
The velocity update Equation (14) and position update Equation (15) are given
as follows:
Dv vid (t + 1) = r × Dv vid (t) + Dv aid (t)
(14)
Dv xid (t + 1) = Dv xid (t) + Dv vid (t + 1)

(15)

GSA Optimization Process for Fused Features: Initialization: Randomly initialize
the positions of individuals in the population and set the initial velocity to zero. Fitness
Calculation: Use the fitness calculation formula Equation (9), where the Euclidean distance
between adjacent variables is treated as the fitness function. Mass and Gravity Calculation:
Update the mass of each individual based on fitness values and compute the gravitational
force using Equations (11) and (13). This directs the search towards a better set of features.
Acceleration and Velocity Calculation: Update the acceleration and velocity using the
gravitational force and the respective formulas. Position Update: With the updated velocity,
calculate the new position for the next iteration using Equation (15). This process ensures
that the optimization through GSA refines the fused features to maximize the effectiveness
of fault diagnosis by iteratively searching for the optimal solution.
2.2.3. Time Complexity of the Optimization Algorithm
In the feature optimization process, we employed the GSA to handle the selection and
optimization of high-dimensional data features.
The iterations refers to the maximum number of iterations the algorithm can perform,
population size indicates the number of solutions in the solution set, and dimension represents the dimensionality of the feature space. Compared to particle swarm optimization
(PSO) and the genetic algorithm (GA), GSA can maintain strong global search capabilities
even with fewer iterations. More specifically, under the same feature space dimensionality,
GSA demonstrates a robust ability to explore the global solution space. Even with a smaller
number of iterations and a reduced population size, GSA can still reach the global optimum.
Therefore, compared to other optimization algorithms, such as PSO and GA, GSA offers a
more stable and faster convergence while maintaining global search capabilities.

## PDF page 8

Machines 2024, 12, 831

8 of 15

PSO has a time complexity similar to that of GSA, but it is more prone to becoming
trapped in local optima, especially in high-dimensional spaces. PSO often requires more
iterations to escape local optima and find a global solution.
GA updates solutions in each iteration through selection, crossover, and mutation
operations. While GA can maintain population diversity, its convergence speed is slower,
particularly when the chromosome length increases, which leads to a significant rise in
computational complexity.
In contrast, GSA can achieve the global optimum with fewer iterations, making it
particularly suitable for dealing with high-dimensional data and nonlinear problems. This
advantage makes GSA highly efficient for complex data optimization tasks. In summary,
GSA provides a unique balance between efficient global exploration and quick convergence,
which sets it apart from PSO and GA. Its ability to reach the global optimum with fewer
iterations and smaller population sizes makes it ideal for high-dimensional and nonlinear
data scenarios.
To further reduce the computational resource waste during high-dimensional data
processing, we introduced adaptive gravitational calculation (Equation (13)), which dynamically adjusts the gravitational force throughout the iterative process. This approach
minimizes unnecessary computational overhead. The adaptive gravitational force is adjusted based on the current iteration; as the number of iterations increases, the gravitational
value gradually decreases. This allows for broader global exploration in the early stages of
the optimization, followed by finer local search as the algorithm converges.
2.3. SVM and K-Fold Cross-Validation
This study categorizes the failure modes of harmonic drives (Table 1) and then uses
the GSA-optimized vibration features to train a SVM for classification tasks. The strength
of SVM lies in its robust ability to separate data in high-dimensional spaces, making
it particularly suitable for datasets that are not linearly separable. SVM can effectively
handle high-dimensional data and performs well in small sample sizes. It offers strong
generalization capabilities and accuracy for classification tasks with low noise and clear
boundaries, making it ideal for identifying various health conditions of harmonic drives.
During the training of the SVM fault classifier, the process begins by extracting multilevel features from the signals of various fault types. These features are then fused, followed
by optimization using GSA. The optimized features are subsequently input into the SVM
to obtain the final classification results.
Table 1. Fault types and causes for harmonic drives.
Fault Model

Gear Wear

Less Grease

Gear Fracture

Improper Load

Bearing Damage

Fault Cause

Excessive shaft
misalignment, high
surface roughness

Excessive or less
grease

Overloading,
misuse

Excessive load

Bearing ball wear

To achieve a fair evaluation of the model, K-fold cross-validation was adopted for
model training in this research. In the K-fold cross-validation process, the original dataset
is randomly divided into K equally proportioned subsets. In each training iteration, K − 1
subsets are selected as the training set, and the remaining subset is used as the test set for
validation. This process is repeated K times, ensuring that each subset serves as the test
set in different iterations. Finally, the test results from all iterations are combined for a
comprehensive analysis, providing a more robust and reliable evaluation of the model’s
performance. This approach effectively reduces the risk of overfitting and enhances the
model’s generalization ability.

## PDF page 9

3.1. Experimental Setup
Figure 3a illustrates the custom-designed test apparatus for the sixth-axis harmonic
drive, which aims to simulate the operation of the sixth axis in a real robotic arm. The
9 of 15
setup consists of three main units:

Machines 2024, 12, 831

1.

Harmonic Drive Unit: This unit uses a harmonic drive to mimic the motion of the
robotic arm’s sixth axis. It comprises an ECM-B3M-C20604 servo motor and a har3. Experimental Study
monic drive with a reduction ratio of 100.
custom
test The
setupservo
was motor
designed
simulateby
theanharmonic
drive of the
axis
of
2. A
Control
Unit:
is to
controlled
ASD-B3-0421-L
servosixth
drive
cona robotic
arm,
and
data
collection
was
performed
using
this
test
apparatus
(Figure
3a,b).
troller to manage the motor’s operation.
This Data
setupAcquisition
allowed usUnit:
to gather
relevantUSB-2405
vibrationdevice
and operational
undervibration
various
3.
The ADLink
is employeddata
to collect
fault data
conditions,
providing
a
controlled
environment
for
evaluating
the
performance
of the
from the X- and Y-axes.
proposed fault diagnosis method.

(a)

(c)

(b)

(d)

(e)

(f)

Figure
Figure 3.
3. (a)
(a) Experimental
Experimental setup;
setup; (b)
(b) schematic
schematic of
of the
the sixth
sixth axis;
axis; (c)
(c) gear
gear wear;
wear; (d)
(d) bearing
bearing damage;
damage;
(e) improper load; (f) gear fracture.
(e) improper load; (f) gear fracture.

accurately
detect the health status of the harmonic drive, we manually simulated
3.1. To
Experimental
Setup
six common
operating
including one
condition
and five
singleFigure 3a illustratesconditions,
the custom-designed
testnormal
apparatus
for the (N)
sixth-axis
harmonic
point
conditions:
gear the
wear
(GW) of
(Figure
3c), axis
bearing
damage
(Figure
3d),
drive, fault
which aims
to simulate
operation
the sixth
in a real
robotic(B)
arm.
The setup
consists of three main units:
1.

2.
3.

Harmonic Drive Unit: This unit uses a harmonic drive to mimic the motion of the
robotic arm’s sixth axis. It comprises an ECM-B3M-C20604 servo motor and a harmonic drive with a reduction ratio of 100.
Control Unit: The servo motor is controlled by an ASD-B3-0421-L servo drive controller to manage the motor’s operation.
Data Acquisition Unit: The ADLink USB-2405 device is employed to collect vibration
data from the X- and Y-axes.

To accurately detect the health status of the harmonic drive, we manually simulated
six common operating conditions, including one normal condition (N) and five single-point
fault conditions: gear wear (GW) (Figure 3c), bearing damage (B) (Figure 3d), improper load
(IL) (Figure 3e), gear fracture (GF) (Figure 3f), and less grease (LG). For precise verification
of the harmonic drive’s health, vibration data were collected at a sampling rate of 51.2 kHz
for all six operating conditions. Additionally, 170 samples were gathered at a rotational
speed of 2400 rpm, with each sample having a duration of 1 s (Table 2). The time-domain
profiles of signals from different health conditions are similar, making it quite challenging
to distinguish between these states based solely on raw measured signals. Therefore,
signal processing algorithms are required to extract effective fault features. During the
model training phase, 5-fold cross-validation was adopted. The dataset was randomly and
uniformly divided into five subsets. One subset was randomly selected as the test set, and
the remaining four were used as the training set. This process was repeated five times, with

## PDF page 10

Machines 2024, 12, 831

pling rate of 51.2 kHz for all six operating conditions. Additionally, 170 samples were
gathered at a rotational speed of 2400 rpm, with each sample having a duration of 1 s
(Table 2). The time-domain profiles of signals from diﬀerent health conditions are similar,
making it quite challenging to distinguish between these states based solely on raw measured signals. Therefore, signal processing algorithms are required to extract eﬀective10fault
of 15
features. During the model training phase, 5-fold cross-validation was adopted. The dataset was randomly and uniformly divided into five subsets. One subset was randomly
selected
as the
test set,
the remaining
four
were used
as of
thethese
training
set. This
each subset
serving
asand
the test
set once. The
average
result
five tests
wasprocess
used as
was
repeated
five times,
with
each subset
serving as
the 4).
test set once. The average result
the final
evaluation
of the
model’s
performance
(Figure
of these five tests was used as the final evaluation of the model’s performance (Figure 4.).
Table 2. Number of original data entries for vibration signals.
Table 2. Number of original data entries for vibration signals.
Model Type
Signal Type

Model Type
N, GF, GW, IL, LG, B
N, GF, GW, IL, LG, B

Signal Type
Vibration
Vibration

Total

Total
170
170

Figure4.4.K-fold
K-foldcross-validation
cross-validationdiagram.
diagram.
Figure

3.2.Experimental
ExperimentalProcedure
Procedure
3.2.
Step1:1:Collect
Collectvibration
vibrationsignals
signalsfrom
fromthe
theharmonic
harmonicdrive
driveunder
undersix
sixfault
faultmodels:
models:nornor•• Step
mal gear, gear wear, gear fracture, less grease, bearing damage, and improper load. The
mal gear, gear wear, gear fracture, less grease, bearing damage, and improper load.
signals are then decomposed using WPD and EMD to obtain decomposition features.
The signals are then decomposed using WPD and EMD to obtain decomposition fea•
Step 2: Fuse the decomposition feature matrices from both the X-axis and Y-axis.
tures.
•
Step 3(a): Perform SVM classification on the fused features, applying 5-fold cross•
Step 2: Fuse the decomposition feature matrices from both the X-axis and Y-axis.
validation to ensure fairness in training.
•
Step 3(a): Perform SVM classification on the fused features, applying 5-fold cross•
Step 3(b): Optimize the fused features using GSA, PSO, and GA, and compute the
validation to ensure fairness in training.
computation time performance of each method.
•
Step 3(b): Optimize the fused features using GSA, PSO, and GA, and compute the
•
Step 4: Use the optimized features from step 3(b) for SVM classification, again employcomputation time performance of each method.
ing 5-fold cross-validation to ensure fair training.
•
Step 4: Use the optimized features from step 3(b) for SVM classification, again employing
5-foldExperiment
cross-validation to ensure fair training.
4. Data
Analysis
The raw vibration signals are nonlinear, making it challenging to rely on a single
4. Data Analysis Experiment
signal for fault diagnosis. Therefore, feature extraction is a necessary and crucial step
Thefault
rawdiagnosis
vibration process.
signals are
nonlinear,
making it challenging
relyemployed
on a single
in the
Two
signal decomposition
methodsto
were
to
signal
for
fault
diagnosis.
Therefore,
feature
extraction
is
a
necessary
and
crucial
step
in
extract key features: WPD; the propose method further decomposes the signal into
highthe
fault diagnosis
process. Two
signal decomposition
methods
were employed
to extract
frequency
and low-frequency
components.
Its significant
advantage
lies in its multi-scale
key
features:
WPD; the
propose
method
further
decomposes
signal
into making
high-fre-it
analysis
capability,
which can
capture
features
across
different the
frequency
ranges,
quency
andsuitable
low-frequency
components.
Its EMD
significant
advantage
lies inthe
itslocal
multi-scale
especially
for time-frequency
analysis.
begins by
detecting
maxima
analysis
capability,
capture
featuresthese
acrosspoints
diﬀerent
frequency
ranges,
making
and
minima
of thewhich
signalcan
and
interpolating
to form
the upper
and
lower
itenvelopes
especiallyof the
suitable
forwaveform.
time-frequency
analysis.
EMD begins
detecting the
signal
From these
envelopes,
the by
instantaneous
meanlocal
line
at each time point is calculated. This process is repeated until the conditions for the IMF
are met.
4.1. Computational Complexity Analysis
A combination of WPD and EMD methods was employed alongside optimization
algorithms such as GSA, PSO, and GA to validate the proposed WPD-GSA diagnostic
framework. However, a common drawback of data fusion is the potential for imbalanced
data and high-dimensional issues, which can lead to increased computational complexity
and a significant waste of computational resources.

## PDF page 11

Machines 2024, 12, 831

11 of 15

4.2. Performance Evaluation
The proposed method first extracts features from vibration signals for different axes
and operating conditions using WPD and EMD. Then, the extracted features from the X-axis
and Y-axis are fused, followed by feature optimization using GSA. For a comprehensive
comparison, we evaluated WPD, EMD, and their fused versions, FWPD and FEMD. Finally,
GSA was applied to optimize the fused features FWPD and FEMD. In this section, we
compare the diagnostic performance of WPD, EMD, FWPD, and FEMD and the results
after applying different optimization algorithms to the signal features. According to the
experimental results, Table 3 shows the diagnostic performance of various methods. The
performance of WPD and EMD is inferior to that of the fused FWPD and FEMD. However,
as the feature dimensionality increases, the time complexity also rises significantly.
The experimental results in Figure 5 indicate that whether using WPD or EMD alone
or after feature fusion with FWPD and FEMD, the accuracy and diagnostic performance
differ. Both WPD and EMD exhibited classification errors in certain fault types, particularly
in distinguishing between gear fracture and gear wear, where the similarities in features
led to higher misclassification rates. However, after feature fusion (FWPD and FEMD) and
optimization, these errors were significantly reduced. To address this issue, we introduced
different optimization algorithms. The results in Figure 6 show that GSA significantly
outperforms GA and PSO in terms of diagnostic accuracy. Specifically, FWPD combined
with GSA achieved an accuracy of 93.3%, while FWPD+GA and FWPD+PSO achieved
80.76% and 76.6%, respectively. Although GA improved accuracy, its computation time
was much higher than that of GSA, highlighting GSA’s potential for computation-time
applications. Figure 7 demonstrates the performance of different methods in terms of
computation time processing. GSA not only improved diagnostic accuracy but also maintained lower computational resource consumption, making it more practical for industrial
applications. Notably, in the FWPD+GSA combination, the classification accuracy for gear
fracture and gear wear improved substantially, indicating that GSA optimization of fused
features effectively mitigates feature similarity issues and enhances diagnostic accuracy. As
shown in Figure 6, the diagnostic performance after feature fusion is improved compared
to using WPD or EMD individually. However, with feature fusion, the dimensionality
increases, leading to a noticeable rise in time complexity. To further enhance diagnostic
accuracy and reduce the waste of computational resources, we employed optimization
algorithms for feature selection. With the inclusion of GSA, accuracy and other performance
metrics improved significantly, with the FWPD+GSA combination outperforming all other
methods in all tests.
Table 3. Performance evaluation of different diagnostic methods.
Methods
EMD (X-axis)
EMD (Y-axis)
WPD (X-axis)
WPD (Y-axis)
FEMD
FEMD+GSA
FEMD+GA
FEMD+PSO
FWPD
FWPD+GSA
FWPD+GA
FWPD+PSO

Vibration
ACC

PC

RC

F1

Computation Time

52.6
35.6
68.6
55.0
65.0
88.5
78.6
82.3
73.3
93.3
80.76
76.6

52.2
40.5
69.7
55.2
75.8
89.7
79.3
83.7
75.1
94.5
82.2
78.1

56.6
35.6
68.6
55.0
65.0
88.5
78.3
82.5
73.3
93.3
80.7
76.6

50.6
33.7
88.6
54.4
64.84
86.9
77.5
82.5
71.7
92.9
80.4
77.0

104.11(S)
92.66(S)
15.6(S)
15.87(S)
228.67(S)
1306.02(S)
2151.39(S)
1839.63(S)
28.35(S)
267.95(S)
1040.46(S)
530.33(S)

## PDF page 12

FEMD+GA
FEMD+PSO
FWPD
FWPD+GSA
FWPD+GA
FWPD+PSO

Machines 2024, 12, 831

78.6
82.3
73.3
93.3
80.76
76.6

79.3
83.7
75.1
94.5
82.2
78.1

78.3
82.5
73.3
93.3
80.7
76.6

77.5
82.5
71.7
92.9
80.4
77.0

(a)

(b)

(c)

(d)

2151.39(S)
1839.63(S)
28.35(S)
267.95(S)
1040.46(S)
530.33(S)

12 of 15

Figure 5. Accuracy comparison chart for diﬀerent optimization methods. (a) FWPD, (b)
FWPD+GSA, (c) FEMD, (d) FEMD+GSA.
(c) FEMD, (d) FEMD+GSA.

Figure 5. Accuracy comparison chart for different optimization methods. (a) FWPD, (b) 13 of
FWPD+GSA,
Machines 2024, 12, x FOR PEER REVIEW
16

Figure 6.
6. Accuracy
Accuracy comparison
Figure
comparisonchart.
chart.

However, although the optimization methods GSA, PSO, and GA improved diagnostic performance, their computation times increased significantly. In comparison, the diagnostic method using GSA achieved high accuracy while maintaining relatively low computational overhead. Based on the experimental results, the proposed WPD-GSA diagnostic framework eﬀectively enhances fault diagnosis accuracy. Moreover, compared to

## PDF page 13

Machines 2024, 12, 831

13 of 15

Figure 6. Accuracy comparison chart.

However,
theoptimization
optimizationmethods
methodsGSA,
GSA,
PSO,
and
improved
diagHowever, although the
PSO,
and
GAGA
improved
diagnosnostic
performance,
computation
times
increased
significantly.
comparison,
the
tic
performance,
theirtheir
computation
times
increased
significantly.
In In
comparison,
the diagdiagnostic
method
using
GSA
achieved
high
accuracy
while
maintaining
relatively
low
nostic method using GSA achieved high accuracy while maintaining relatively low comcomputational
overhead.
Based
onexperimental
the experimental
results,
the proposed
WPD-GSA
putational overhead.
Based
on the
results,
the proposed
WPD-GSA
diagdiagnostic
framework
effectively
enhances
fault
diagnosis
accuracy.
Moreover,
compared
nostic framework eﬀectively enhances fault diagnosis accuracy. Moreover, compared
to
to
other
optimizationmethods,
methods,GSA
GSAdemonstrates
demonstrateslower
lower computational
computational load,
other
optimization
load, highlighting
highlighting
its
its potential
potential for
for practical
practicalapplications.
applications.

Figure7.
7. Computation
Computation time
time comparison
comparison of
ofdifferent
diﬀerentmethods.
methods.
Figure

5. Conclusions
Conclusions
5.
This
presents aamulti-sensor
multi-sensordata
datafusion
fusionmethod
method
enhanced
WPD
This research presents
enhanced
by by
WPD
andand
the
the
GSA
fault
diagnosis
harmonic
drives.
industrial
equipment
such as
robotic
GSA
for for
fault
diagnosis
in in
harmonic
drives.
As As
industrial
equipment
such as
robotic
arms
arms
increasingly
complex,
thefor
need
for more
accurate
diagnosis
in critical
growsgrows
increasingly
complex,
the need
more
accurate
fault fault
diagnosis in
critical
compocomponents
like
harmonic
drives
has
become
more
pressing.
Single-sensor
data
often
nents like harmonic drives has become more pressing. Single-sensor data often lackslacks
sufsufficient
information
accurate
detection,
so this
research
improves
diagnostic
ficient
information
for for
accurate
faultfault
detection,
so this
research
improves
diagnostic
accuaccuracy
employing
multi-sensor
fusion.
Specifically,
WPD
was
used
decompose
racy
by by
employing
multi-sensor
datadata
fusion.
Specifically,
WPD
was
used
to to
decompose
XX-axisand
andY-axis
Y-axisvibration
vibrationsignals,
signals,extracting
extractingmulti-scale
multi-scalehighhigh-and
andlow-frequency
low-frequency features.
axis
After
from
both
axes,
GSA
waswas
applied
to to
optimize
the the
high-dimensional
Afterfusing
fusingthe
thefeatures
features
from
both
axes,
GSA
applied
optimize
high-dimenfused
features.
Experimental
results
showed
that
feature
fusion
significantly
enhanced
disional fused features. Experimental results showed that feature fusion significantly enagnostic
accuracy
compared
to
using
WPD
or
empirical
mode
decomposition
(EMD)
alone.
hanced diagnostic accuracy compared to using WPD or empirical mode decomposition
Through
multiple
experiments,
study demonstrated
effectiveness
feature fusion
(EMD) alone.
Through
multiplethe
experiments,
the study the
demonstrated
theofeﬀectiveness
of
methods, with FWPD and FEMD improving both diagnostic accuracy and stability. The
FWPD+GSA combination achieved the highest diagnostic accuracy at 93.3%, surpassing
WPD+GA (80.76%) and FWPD+PSO (76.6%). GSA’s global search capability and efficiency
enabled it to maintain high accuracy with a lower computational burden, offering good
convergence speed and computation time performance. However, while feature fusion improves diagnostic accuracy, it also increases computational load. GSA effectively mitigates
this by reducing redundant features and minimizing overfitting risks through adaptive
gravity. In contrast, GA and PSO, although improving accuracy, require significantly more
computation time, particularly GA, which struggles with high-dimensional data.
Author Contributions: Methodology, T.-Y.Y.; Investigation, N.-K.H.; Writing—original draft, T.-Y.Y.
All authors have read and agreed to the published version of the manuscript.
Funding: This research received no external funding.
Data Availability Statement: Data are contained within the article.
Conflicts of Interest: The authors declare no conflict of interest.

## PDF page 14

Machines 2024, 12, 831

14 of 15

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

IFR International Federation of Robotics. World Robotics 2023 Report: Asia Ahead of Europe and the Americas. Available online:
https://ifr.org/ifr-press-releases/news/world-robotics-2023-report-asia-ahead-of-europe-and-the-americas (accessed on 29
November 2023).
Raviola, A.; De Martin, A.; Guida, R.; Jacazio, G.; Mauro, S.; Sorli, M. Harmonic drive gear failures in industrial robots applications:
An overview. In Proceedings of the PHM Society European Conference, Virtual, 28 June–2 July 2021; p. 11.
Li, Q. RUL estimation for rolling bearings using augmented quaternion-based least mean P-power with correntropy induced
metric under framework of sparsity. IEEE/ASME Trans. Mechatron. 2022, 28, 976–989. [CrossRef]
Zio, E. Prognostics and Health Management (PHM): Where are we and where do we (need to) go in theory and practice. Reliab.
Eng. Syst. Saf. 2022, 218, 108119. [CrossRef]
Medoued, A.; Mordjaoui, M.; Soufi, Y.; Sayad, D. Induction machine bearing fault diagnosis based on the axial vibration analytic
signal. Int. J. Hydrogen Energy 2016, 41, 12688–12695. [CrossRef]
Cui, L.; Yan, L.; Zhao, D. Instantaneous Frequency Estimation-Based Order Tracking for Bearing Fault Diagnosis Under Strong
Noise. IEEE Sens. J. 2023, 23, 30940–30949. [CrossRef]
Paskalovski, S.; Digalovski, M. Simulation models for induction machine protection analysis. Int. J. Inf. Technol. Secur. 2022, 14,
63–74.
Hou, X.; Du, F.; Huang, K.; Qiu, J.; Zhong, X. A Current-Based Fault Diagnosis Method for Rotating Machinery with Limited
Training Samples. IEEE Trans. Instrum. Meas. 2023, 72, 3530414. [CrossRef]
Raouf, I.; Lee, H.; Kim, H.S. Mechanical fault detection based on machine learning for robotic RV reducer using electrical current
signature analysis: A data-driven approach. J. Comput. Des. Eng. 2022, 9, 417–433. [CrossRef]
Wang, T.; Liang, M.; Li, J.; Cheng, W.; Li, C. Bearing fault diagnosis under unknown variable speed via gear noise cancellation
and rotational order sideband identification. Mech. Syst. Signal Process. 2015, 62, 30–53. [CrossRef]
Visnadi, L.B.; de Castro, H.F. Influence of bearing clearance and oil temperature uncertainties on the stability threshold of
cylindrical journal bearings. Mech. Mach. Theory 2019, 134, 57–73. [CrossRef]
Choudhary, A.; Goyal, D.; Letha, S.S. Infrared Thermography-Based Fault Diagnosis of Induction Motor Bearings Using Machine
Learning. IEEE Sens. J. 2021, 21, 1727–1734. [CrossRef]
Cui, X.; Wu, Y.; Zhang, X.; Huang, J.; Wong, P.K.; Li, C. A novel fault diagnosis method for rotor-bearing system based on
instantaneous orbit fusion feature image and deep convolutional neural network. IEEE/ASME Trans. Mechatron. 2022, 28,
1013–1024. [CrossRef]
Xia, M.; Li, T.; Xu, L.; Liu, L.; De Silva, C.W. Fault diagnosis for rotating machinery using multiple sensors and convolutional
neural networks. IEEE/ASME Trans. Mechatron. 2017, 23, 101–110. [CrossRef]
Kumar, P.; Raouf, I.; Kim, H.S. Transfer learning for servomotor bearing fault detection in the industrial robot. Adv. Eng. Softw.
2024, 194, 103672. [CrossRef]
Kibrete, F.; Engida Woldemichael, D.; Shimels Gebremedhen, H. Multi-Sensor data fusion in intelligent fault diagnosis of rotating
machines: A comprehensive review. Measurement 2024, 232, 114658. [CrossRef]
AlShorman, O.; Irfan, M.; Abdelrahman, R.e.B.; Masadeh, M.; Alshorman, A.; Sheikh, M.A.; Saad, N.; Rahman, S. Advancements
in condition monitoring and fault diagnosis of rotating machinery: A comprehensive review of image-based intelligent techniques
for induction motors. Eng. Appl. Artif. Intell. 2024, 130, 107724. [CrossRef]
Fang, R.; Liu, Z.; Peng, C.; Yang, Y.; Zhang, S. Fault diagnosis of inter-turn short circuit in turbogenerator rotor windings based
on vibration-current signal fusion. Energy Rep. 2023, 9, 316–323. [CrossRef]
Gan, C.; Wu, J.; Yang, S.; Hu, Y.; Cao, W.; Si, J. Fault diagnosis scheme for open-circuit faults in switched reluctance motor drives
using fast Fourier transform algorithm with bus current detection. IET Power Electron. 2016, 9, 20–30. [CrossRef]
Gao, Z.; Cecati, C.; Ding, S.X. A survey of fault diagnosis and fault-tolerant techniques—Part I: Fault diagnosis with model-based
and signal-based approaches. IEEE Trans. Ind. Electron. 2015, 62, 3757–3767. [CrossRef]
Habbouche, H.; Benkedjouh, T.; Zerhouni, N. Intelligent prognostics of bearings based on bidirectional long short-term memory
and wavelet packet decomposition. Int. J. Adv. Manuf. Technol. 2021, 114, 145–157. [CrossRef]
Babu, T.N.; Devendiran, S.; Aravind, A.; Rakesh, A.; Jahzan, M. Fault diagnosis on journal bearing using empirical mode
decomposition. Mater. Today Proc. 2018, 5, 12993–13002. [CrossRef]
Wang, D.; Zhao, Y.; Yi, C.; Tsui, K.-L.; Lin, J. Sparsity guided empirical wavelet transform for fault diagnosis of rolling element
bearings. Mech. Syst. Signal Process. 2018, 101, 292–308. [CrossRef]
Yan, R.; Shang, Z.; Xu, H.; Wen, J.; Zhao, Z.; Chen, X.; Gao, R.X. Wavelet transform for rotary machine fault diagnosis: 10 years
revisited. Mech. Syst. Signal Process. 2023, 200, 110545. [CrossRef]
de Azevedo, H.D.M.; Araújo, A.M.; Bouchonneau, N. A review of wind turbine bearing condition monitoring: State of the art
and challenges. Renew. Sustain. Energy Rev. 2016, 56, 368–379. [CrossRef]
Chudzik, A.; Warda, B. Effect of radial internal clearance on the fatigue life of the radial cylindrical roller bearing. Eksploat. I
Niezawodn. 2019, 21, 211–219. [CrossRef]
Karabacak, Y.E.; Gürsel Özmen, N.; Gümüşel, L. Intelligent worm gearbox fault diagnosis under various working conditions
using vibration, sound and thermal features. Appl. Acoust. 2022, 186, 108463. [CrossRef]

## PDF page 15

Machines 2024, 12, 831

28.
29.

30.
31.
32.
33.
34.
35.
36.

37.
38.
39.
40.
41.
42.
43.
44.
45.
46.

15 of 15

Han, T.; Liu, C.; Yang, W.; Jiang, D. A novel adversarial learning framework in deep convolutional neural network for intelligent
diagnosis of mechanical faults. Knowl. -Based Syst. 2019, 165, 474–487. [CrossRef]
Irfan, M.; Althobiani, F.; Alwadie, A.S.; Zaffar, M.; Abbass, A.; Glowacz, A.; Ghonaim, S.M.; Abdushkour, H.; Rahman,
S.; Alshorman, O. Condition monitoring of water pump bearings using ensemble classifier. Adv. Mech. Eng. 2022, 14,
16878132221089170. [CrossRef]
Dameshghi, A.; Refan, M.H. Wind turbine gearbox condition monitoring and fault diagnosis based on multi-sensor information
fusion of SCADA and DSER-PSO-WRVM method. Int. J. Model. Simul. 2019, 39, 48–72. [CrossRef]
Lei, Y.; Lin, J.; He, Z.; Zuo, M.J. A review on empirical mode decomposition in fault diagnosis of rotating machinery. Mech. Syst.
Signal Process. 2013, 35, 108–126. [CrossRef]
Sun, H.; Zi, Y.; He, Z. Wind turbine fault detection using multiwavelet denoising with the data-driven block threshold. Appl.
Acoust. 2014, 77, 122–129. [CrossRef]
Rashedi, E.; Nezamabadi-Pour, H.; Saryazdi, S. GSA: A gravitational search algorithm. Inf. Sci. 2009, 179, 2232–2248. [CrossRef]
Rashedi, E.; Rashedi, E.; Nezamabadi-pour, H. A comprehensive survey on gravitational search algorithm. Swarm Evol. Comput.
2018, 41, 141–158. [CrossRef]
Ding, S.; Hao, M.; Cui, Z.; Wang, Y.; Hang, J.; Li, X. Application of multi-SVM classifier and hybrid GSAPSO algorithm for fault
diagnosis of electrical machine drive system. ISA Trans. 2023, 133, 529–538. [CrossRef] [PubMed]
Precup, R.-E.; David, R.-C.; Petriu, E.M.; Radac, M.-B.; Preitl, S. Adaptive GSA-based optimal tuning of PI controlled servo
systems with reduced process parametric sensitivity, robust stability and controller robustness. IEEE Trans. Cybern. 2014, 44,
1997–2009. [CrossRef] [PubMed]
Eappen, G.; Shankar, T. Hybrid PSO-GSA for energy efficient spectrum sensing in cognitive radio network. Phys. Commun. 2020,
40, 101091. [CrossRef]
Hooda, H.; Verma, O.P. Fuzzy clustering using gravitational search algorithm for brain image segmentation. Multimed. Tools Appl.
2022, 81, 29633–29652. [CrossRef]
Zamfirache, I.A.; Precup, R.-E.; Roman, R.-C.; Petriu, E.M. Reinforcement Learning-based control using Q-learning and gravitational search algorithm with experimental validation on a nonlinear servo system. Inf. Sci. 2022, 583, 99–120. [CrossRef]
Raouf, I.; Lee, H.; Noh, Y.R.; Youn, B.D.; Kim, H.S. Prognostic health management of the robotic strain wave gear reducer based
on variable speed of operation: A data-driven via deep learning approach. J. Comput. Des. Eng. 2022, 9, 1775–1788. [CrossRef]
Das, O.; Bagci Das, D.; Birant, D. Machine learning for fault analysis in rotating machinery: A comprehensive review. Heliyon
2023, 9, e17584. [CrossRef]
Raouf, I.; Kumar, P.; Soo Kim, H. Deep learning-based fault diagnosis of servo motor bearing using the attention-guided feature
aggregation network. Expert Syst. Appl. 2024, 258, 125137. [CrossRef]
Siddique, M.F.; Ahmad, Z.; Ullah, N.; Kim, J. A Hybrid Deep Learning Approach: Integrating Short-Time Fourier Transform and
Continuous Wavelet Transform for Improved Pipeline Leak Detection. Sensors 2023, 23, 8079. [CrossRef] [PubMed]
Zhu, Z.; Lei, Y.; Qi, G.; Chai, Y.; Mazur, N.; An, Y.; Huang, X. A review of the application of deep learning in intelligent fault
diagnosis of rotating machinery. Measurement 2023, 206, 112346. [CrossRef]
Siddique, M.F.; Ahmad, Z.; Kim, J.-M. Pipeline leak diagnosis based on leak-augmented scalograms and deep learning. Eng. Appl.
Comput. Fluid Mech. 2023, 17, 2225577. [CrossRef]
Raouf, I.; Kumar, P.; Lee, H.; Kim, H.S. Transfer Learning-Based Intelligent Fault Detection Approach for the Industrial Robotic
System. Mathematics 2023, 11, 945. [CrossRef]

Disclaimer/Publisher’s Note: The statements, opinions and data contained in all publications are solely those of the individual
author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to
people or property resulting from any ideas, methods, instructions or products referred to in the content.
