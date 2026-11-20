Source: see manifest row of the PDF
PDF sha256: 29dd2a3b8d952eb0a30cff7a50bfa1f30893268a974038206027e20b517a3bd2
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters, text-layer)

# Transcription of beaubois_2024_biomus_neurological_disorders_real_time_emulation_spiking_neural_network.pdf

Transcription of `beaubois_2024_biomus_neurological_disorders_real_time_emulation_spiking_neural_network.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 3, 6-7 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories; pages 1-2, 4-5, 8-14 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Article

https://doi.org/10.1038/s41467-024-48905-x

BiœmuS: A new tool for neurological
disorders studies through real-time
emulation and hybridization using
biomimetic Spiking Neural Network
Received: 31 August 2023

1234567890():,;

1234567890():,;

Accepted: 15 May 2024

Romain Beaubois 1,2,3, Jérémy Cheslet 1,2,3, Tomoya Duenki 2,3,4,5,
Giuseppe De Venuto6, Marta Carè 6,7,8, Farad Khoyratee1,
Michela Chiappalone 6,7,8, Pascal Branchereau 9, Yoshiho Ikeuchi 2,3,5 &
Timothée Levi 1

Check for updates

Characterization and modeling of biological neural networks has emerged as a
ﬁeld driving signiﬁcant advancements in our understanding of brain function
and related pathologies. As of today, pharmacological treatments for neurological disorders remain limited, pushing the exploration of promising alternative approaches such as electroceutics. Recent research in bioelectronics
and neuromorphic engineering have fostered the development of the new
generation of neuroprostheses for brain repair. However, achieving their full
potential necessitates a deeper understanding of biohybrid interaction. In this
study, we present a novel real-time, biomimetic, cost-effective and userfriendly neural network capable of real-time emulation for biohybrid experiments. Our system facilitates the investigation and replication of biophysically
detailed neural network dynamics while prioritizing cost-efﬁciency, ﬂexibility
and ease of use. We showcase the feasibility of conducting biohybrid experiments using standard biophysical interfaces and a variety of biological cells as
well as real-time emulation of diverse network conﬁgurations. We envision our
system as a crucial step towards the development of neuromorphic-based
neuroprostheses for bioelectrical therapeutics, enabling seamless communication with biological networks on a comparable timescale. Its embedded
real-time functionality enhances practicality and accessibility, amplifying its
potential for real-world applications in biohybrid experiments.

Millions of people worldwide are affected by neurological disorders
that strongly impair their cognitive and/or motor functions1. An
increasing number of technologies and solutions are currently proposed for the treatments of these diseases, whereas being limited to
curbing the progress or managing symptoms in most cases2,3.
Aside from medical treatment through chemical processes, artiﬁcial
devices are developed to improve the quality of life of individuals. To

A full list of afﬁliations appears at the end of the paper.

Nature Communications | (2024)15:5142

bring neuroprosthesis into realization, the behavior of biological neurons as well as its connection and interaction with artiﬁcial neural networks must be considered. To this end, investigation of the interaction
of neuronal cell assemblies is required to understand and reproduce a
speciﬁc behavior driven by intrinsic spontaneous activity. Additionally,
long-term replacement of damaged brain areas with artiﬁcial devices
implies understanding of their neurophysiological behaviors.

e-mail: timothee.levi@u-bordeaux.fr

1

## PDF page 2

Article
In this context, new therapeutic approaches and technologies are
needed both to promote cell survival and regeneration of local
circuits4 and restore long distance communication between disconnected brain regions and circuits5. Thus, characterization and
modeling of biological neural networks6,7 are crucial to develop the
new generation of neuroprostheses that mimics biological dynamics
and provides adaptive stimulation at biological timescale based on the
principle of electroceutics8,9.
Thanks to the new neuromorphic platforms, performing biohybrid experiments involving the bi-directional communication between
a living system and its artiﬁcial counterpart is becoming more and
more relevant not only for the development of neuromorphic biomedical devices8,9, but also to elucidate the mechanisms of information processing in the nervous system10. Recently, major progress has
been made in the ﬁeld of neuroprostheses6,7, so as neuromorphic
devices are now capable of receiving and processing input while locally
or remotely delivering their output either through electrical, chemical
or optogenetic stimulation11.
A bi-directional interaction performed according to closed-loop
architecture is mandatory to perform biohybrid experiments6. Closedloop technologies has seen signiﬁcant advancements, particularly in
the realm of adaptive, personalized therapies. A notable development
in this area is the focus on leveraging various sensing systems to enable
therapies that can deliver closed-loop (i.e. adaptive) biomimetic inputs
to dysfunctional neural circuits over time. This approach has shown
particular progress in the treatment of Parkinson’s disease where
adaptive deep brain stimulation devices that adjust stimulation parameters based on neural signals, showed improved efﬁcacy and
reduced side effects compared to traditional ﬁxed-parameter devices12
going as far as restoring functions such as walking13. Another notable
development is found in Brain-Computer Interfaces (BCIs) that have
shown major improvements in enabling real-time adjustments to
enhance system performance and user interaction based on closedloop architectures, and ﬁnding applications in prosthetic control and
rehabilitation for stroke patients14.
In the neuromorphic engineering research, SNNs are designed
using two distinct approaches: bio-inspired or biomimetic. The former
is widely used for applications such as computation and artiﬁcial
intelligence15 using accelerated time simulation of simple neuron
models. The latter uses complex neuron models operating at biological timescale to simulate neural network dynamics and/or performing
biohybrid experiments16. To perform bi-directional biohybrid experiments and develop bioelectrical therapeutic solutions for health care
like electroceutics8,9,17, real-time bio-physics interface and SNN processing are mandatory to ensure interaction at biological timescale18,19.
However, most of current solutions for biomimetic SNN simulations
are software-based tools such as NEURON20, NEST21 or Brian222 and
show signiﬁcantly high computation time, especially for complex
neuron models with synaptic plasticity. Hence, they are not suited for
real-time emulation at millisecond time scale23 differently from
hardware-based SNNs18, characterized by complex neurons and
synapses and which allow temporal accuracy of the stimulation.
Nevertheless, real-time stimulation and processing of biological data
using biomimetic Spiking Neural Network (SNN) are still quite rare24.
Hardware-based SNNs are analog or digital. Analog SNN
systems18,25,26 show lower power consumption than digital SNNs27.
Research on memristor devices as synapses has also been
explored28–30. In contrast, digital SNNs are more ﬂexible thus more
suited for prototyping while showing overall quicker design time,
hence constituting the best choice for preliminary experiments and
design of the new generation of neuroprosthetics.
The prominent SNNs hardware platforms are TrueNorth31,
BrainScaleS-232, SpiNNaker33 and Loihi34. TrueNorth uses a digital
architecture but is inspired by the principles of analog computation,
emphasizing low power consumption and parallel processing

Nature Communications | (2024)15:5142

https://doi.org/10.1038/s41467-024-48905-x

capabilities. BrainScaleS-2 is primarily using Leaky Integrate-and-Fire
(LIF) neurons for exploring learning algorithms and plasticity
mechanisms in neural networks. SpiNNaker provides real-time processing and offers ﬂexibility in simulating different network conﬁgurations and neuron models including LIF and Hodgkin-Huxley (HH)
but with a limited number of conductance-based currents. While some
of these systems present mobile versions like35 for BrainScaleS-2, most
of them primarily offer access via cloud-based services rather than
direct physical access hence limiting direct integration into embedded
closed-loop system outside of the provided server-based infrastructure. Prior work of the team36 presented a hardware-only implementation of a biomimetic SNN, but facing limitations in terms of
network conﬁguration ﬂexibility, system integration and computation
accuracy.
In this manuscript, we present BiœmuS standing for BIOmimetic
EMUlation Single compartment, an accessible low-cost platform for
real-time emulation of biomimetic SNNs characterized by detailed
biophysical models of neurons and synapses within a fully customizable network. We will also showcase the versatility and userfriendliness of BiœmuS, speciﬁcally tailored for biohybrid experiments and guaranteeing a seamless system integration between the
biological and its artiﬁcial counterpart in the context of closed-loop
applications for electroceutical treatments.

Results
Adaptable integrated real-time biomimetic SNN
The targeted low-cost platform is based on a System on a Chip (SoC)
featuring both Programmable Logic (PL, i.e. FPGA) and processors in a
Processing System (PS) part. It is capable of running up to 1024 HH
neurons with fully conﬁgurable synapses, supporting a total of 220
synapses. It features on-board monitoring and versatile external
communication options such as Ethernet, Wi-Fi, expansion PMODs
(standard peripheral module interface) and a Raspberry Pi header;
allowing different compromises for monitoring and interconnection.
The system allows real-time emulation of conﬁgurable networks as an
accessible computing unit that can integrate biohybrid experiments
with versatility (Fig. 1A).
The platform can be divided in two main parts referred to as
software and hardware as identiﬁed in Fig. 1B. The hardware corresponds to the programmable logic part computing the Spiking Neural
Network running in hard real-time at a period of 31.25 μs. The software
part includes the conﬁguration, monitoring and control running in soft
real-time, implying ﬂuctuating latency potentially larger than the
deadline that is however not inducing a failure of the system, at a
minimum period of 1 ms.
The neurons composing the SNN are modeled with high biological plausibility using the Hodgkin-Huxley (HH) paradigm37 in the Pospichil model38 implementing 6 conductance-based currents. An
injected current mimicking synaptic noise following an OrnsteinUhlenbeck process39,40 reproduces spontaneous activity by triggering
action potentials on a random basis.
All parameters of the HH model as well as the synaptic noise
parameters are tuned through the 25 parameters available from the
Python scripts (Fig. 2A). The scripts implement 4 preset neuron types
including Fast Spiking (FS), Regular Spiking (RS), Intrinsic Burst (IB)
and Low Threshold Spiking (LTS) cortical neurons and allow the user
to create new presets.
The equations of ion channel states are pre-computed and stored
in memory so that they can be easily modiﬁed to any channel dynamic
without impacting the performances of the system or limiting the
mathematical functions used. The computation of ion currents is
performed using 32-bit ﬂoating-point coding allowing emulation of
currents with different dynamics potentially smaller in comparison to
other currents like for Ca2+-based currents in IB or LTS neurons
(Fig. S10B).
2

## PDF page 3

<b>Article</b>
https://doi.org/10.1038/s41467-024-48905-x
<b>Emulation</b>
<b>User interface</b>
Monitoring
Setup
🎍 Qt
Modeling
<b>Hardware SNN</b>
<b>Biohybrid experiments</b>
B
<b>Host computer</b>
KR260 Carrier board
K26 SOM
Configuration
Processing system (PS)
•

    Configure network

Canonical Ubuntu 22.04
<math>\equiv</math>
· Generate configuration file
C++ Application

    Emulate behavior

Configure SNN from configuration file
Control SNN
<b>(4)</b>

    Collect and export data

Ò
<b>Monitoring</b>
X
SNN HH
· Monitor spike or waves
· Save spike or waves
Compute SNN neurons

    Send stimulation

Detect spikes from waveforms
Send spike activity
Display waveforms
Software : Hardware Real-time
Programmable logic (PL)
configurations displayed are exported from BiœmuS software. B BiœmuS runs on a
Fig. 1 | Overview of BiœmuS, a real-time hardware-based SNN for biophysically
carrier board integrating a System-on-Module featuring CPU in a Processing System
detailed emulation and biohybrid experiments. A BiœmuS corresponds to a
part (PS) and FPGA in a Programmable Logic part (PL). The real-time hardware
platform integrating a hardware SNN allowing user to monitor and configure. the
system through Python scripts and Qt-based GUI. The fully configurable network
biomimetic SNN is implemented in PL part and controlled through a C++ applica-
allows real-time emulation of custom network configurations that can be inte-
tion running in the PS part. The PS part runs a Canonical Ubuntu allowing standard
grated in a biohybrid experimental setup acting as a versatile biomimetic artificial
interfacing and operation. Monitoring is performed by a Qt-based GUI and setup by
neural network easily interfaced with standard biological recording units. Network
Python scripts ran either on-board or on another computer.
interface) and Raspberry Pi headers, allowing implementation of a
Neurons are connected using biomimetic synapses mimicking
AMPA, NMDA, GABA<sub>A</sub> and GABA<sub>B</sub> synaptic receptors<sup>41</sup> to allow fast and
wide range of protocols.
slow synaptic excitation or inhibition, computed using 18-bit fixed-
The on-board monitoring allows storage of all spikes and up to 16
point coding. The parameters of the synaptic models can be tuned
waveforms in a file, and also forwarding this data over Ethernet using
ZeroMQ (as depicted in Fig. 2B), an open-source networking library
similarly to the HH parameters through the Python scripts (Fig. 2A).
Synaptic connection can be established between all neurons and
widely utilized in embedded systems for its high performances and
independently weighted using the Python scripts allowing the user to
portability. Up to 8 membrane voltages of neurons can be selected at a
create custom functions to setup the connections. The generated
time and output per Digital-to-Analog Converter (DAC) plugged on
configuration file can be emulated using the Python scripts to assess
PMOD connectors. Data is moved from the PL to PS using Direct
behavior and verify membrane voltage, ion channel state equations,
Memory Access (DMA) interfaced by Advanced eXtensible Interface
internal variables and raster plot (Fig. 2A).
(AXI) using a driver, thus providing high throughput and good scaling
almost independently from the CPU load (Figs. S22, S23). The interval
To maximize compatibility and versatility, a Canonical Ubuntu is
running on the processors of the board. Compatibility and versatility
of collection and forwarding for spikes and waveforms can be set from
are important criteria, knowing that standards for communication
the application settings.
protocols interfacing biological recording units vary along with man-
A wireless setup communication for embedded applications is also
ufacturers (e.g., Serial Peripheral Interface (SPI), Ethernet, USB). In
provided via Wi-Fi using a PMOD ESP32 that plugs on PMOD connectors
addition, laboratories often have custom setups, designed to reach
for spike monitoring. It communicates directly with the PL via SPI pro-
their specific needs or inherited from prior experimental settings. The
tocol driven by an ESP32 microcontroller that is able to receive and send
selected carrier board features notably multiple USB3.0 and Ethernet
data through Wi-Fi network (Fig. 2B). This solution offers a more flexible
ports as well as expansion PMODs (standard peripheral module
approach for interconnection of the system that suits well in vivo
Nature Communications | (2024)15:5142
3

## PDF page 4

Article

https://doi.org/10.1038/s41467-024-48905-x

A

Host computer

KR260 Carrier board

SNN-HH.py

NeuronHH.py

K26 SOM
Processing system (PS)
Canonical Ubuntu 22.04

Synapses.py

SNN-HH.py

HwConfigFile.py

C++ Application

SnnEmulator.py

• Configure SNN from configuration file
• Control SNN
• Collect and export data

SNN HH

Emulate FPGA behavior

B

Programmable logic (PL)

Host computer

KR260 Carrier board

Setup
Ethernet
SSH
Spikes
Waves

Monitoring

Wifi
Scope

K26 SOM
Processing system (PS)
Canonical Ubuntu 22.04
Userspace
C++ Application
Kernel
dma proxy driver
AXI DMA

ESP32
Spikes
DAC
Waves

SNN HH

Calculation core
Spike monitoring
Waves monitoring
Programmable logic (PL)

Fig. 2 | Architecture and system integration of the platform. A Overview of
system setup from the conﬁguration ﬁle generated by Python scripts ran either onboard or on another computer. The conﬁguration ﬁle is then read by a C++ application running on Canonical Ubuntu operating system in the Processing System
(PS) part to set up the SNN in Programmable Logic (PL) part. Conﬁguration can be
emulated beforehand to predict the behavior. Example membrane voltage and
raster are exported from BiœmuS software. B Schematic of system communication.

System control is achieved through the C++ application either remotely via SSH or
directly on-board from the Ubuntu desktop. Spikes can be monitored concurrently
using Ethernet, Wi-Fi and on-board ﬁle saving. Waveforms can be monitored concurrently using Ethernet, visualization on scope by probing the Digital-to-Analog
Converter (DAC) and on-board ﬁle saving. Example membrane voltage is exported
from BiœmuS software.

applications where cables are a concern, while maintaining a low latency
and acceptable throughput. In addition, this constitutes a reusable element to build a reduced and minimal embedded version of the system
targeting a smaller hardware-only target to create an energy-efﬁcient
solution for embedded applications.
The SNN is setup from the conﬁguration ﬁle generated by Python
scripts (Fig. 2A) that is either generated directly on-board using the
Python interpreter installed on the Ubuntu operating system or on
another computer. The application controlling the system can be
launched directly on the board using the Ubuntu desktop or remotely
over SSH (Fig. 2B).
The parameters of the application are generated in JSON format in
a conﬁguration ﬁle, allowing users to easily modify parameters without
requiring code recompilation while also preserving parameters of the
run. The parameters include the addresses for ZeroMQ forwarding, the
local saving or other parameters such as the neurons to monitor
(Table S3).
The ﬁrmware can be easily updated and loaded by running bash
scripts, allowing convenient management of alternative versions
developed for a custom dedicated hardware. An external stimulation
trigger for each neuron with an independent duration is available via
ZeroMQ to easily integrate the system in closed-loop setups.

biological models using the provided Python scripts. Two examples of
network conﬁgurations are demonstrated using in vitro and in vivo
experimental models.
To offer a tangible example of network conﬁguration for neurological disorders studies, in vitro cortical organoids have been selected
as a demonstration case. Cortical organoids are three-dimensional
tissue cultures derived from stem cells widely used to investigate the
human brain properties. Thanks to their remarkable capability to
replicate speciﬁc brain areas42–44, they allow for detailed studies of
neural development and organization. Moreover, cortical organoids
demonstrate functional maturation comparable to that observed in
human, a feature not typically observed in traditional primary rat
cultures45. This unique ability to recapitulate human brain-like properties makes cortical organoids an invaluable tool for advancing our
understanding of neurodevelopmental processes and neurological
disorders.
The presented model is based on two types of structures
according to a recent study44, promoting different synaptic connections between organoids as depicted in Fig. 3A. This model constitutes
a good example to illustrate how the network can be conﬁgured
according to custom synaptic connection rules deﬁned by the user, to
align with a speciﬁc model.
The structure referred to as “single” serves to physically isolate
organoids, preventing any direct connections between them. This
conﬁguration functions as a reference model, allowing observation of
the independent activity of each organoid. On the other hand, the

Example network conﬁgurations
This section demonstrates how the Spiking Neural Network of BiœmuS
can be conﬁgured to be exploited for real-time emulation based on

Nature Communications | (2024)15:5142

4

## PDF page 5

Article

https://doi.org/10.1038/s41467-024-48905-x

A

Artificial model

Biological model
Single

Connected

B

internal synapses
(single and connected)

0

external synapses
(only connected)

Neuron index

C

50
40
30
20
10
0

synapses
per neuron

20
10

synapses
per neuron

30

Single

Connected

Time (s)

Excitatory

Inhibitory

Fig. 3 | Example network conﬁguration based on cortical organoids. A Two
structures of cortical organoids modeled using FS and RS neurons connected with
excitatory and inhibitory synaptic connection (AMPAR and GABAAR) based on
biological culture observations and their spiking activity. Synaptic connections are
promoted according to rules depending on the structure to reproduce, spatial
placement of neurons and the ratio of inhibition/excitation connection observed.
The network conﬁguration was exported from Biœmus software. B Heatmap of the
number of connection per neuron for the two structures of organoid interconnection showing internal and external synaptic connections. Internal connections correspond to the synaptic connections inside the two organoids of both

structures in a closer neighbor connection manner. External connections correspond to synaptic connections between organoids for the connected structure,
favoring synaptic connection on the exterior ring of the organoid. Heatmap are
based on an average of 40 random generations of synapses for a given XY mapping.
C Raster plot of 10-second emulated activity of a single and connected structure
using BiœmuS, highlighting network burst synchronicity for the connected structure. The spiking activity emulated corresponds to a maximum probability for
connection inside and outside the organoids of respectively 10% and 2% with 512
neurons per organoid and a 20% inhibition/excitatory neuron ratio.

“connected” organoids, or connectoid, positions organoids several
millimeters apart while facilitating constrained interconnections,
typically forming axon bundles that predominantly link neurons on the
organoid surface46,47. This setup promotes stronger and more intricate
biological activity44.
An additional Python class has been created for that speciﬁc
model to assign normally distributed XY coordinates to neurons and
generate synaptic connections based on speciﬁc rules for each structure. The synaptic connection probability inside organoids is set as a
linear function of the relative distance between neurons, where the
connection probability for the connected organoids is a linear function
of their relative distance to the center of the organoid. The connectivity map obtained, shown in Fig. 3B, presents the connectivity
map of internal and external synapses conﬁrming the synaptic connection rules. The matrix of connection and list of neurons generated
is then simply translated to hardware SNN conﬁguration by the existing software (Fig. 2A), showcasing a case of custom user script to
generate the network conﬁguration.
The two structures were emulated using 1024 neurons distributed
equally between the two organoids with a similar inhibitory/excitatory
ratio to biology44. Inhibition is modeled using FS neurons connecting
by GABAAR and excitation by RS neurons connecting by AMPAR.
While the number of neurons used is signiﬁcantly lower, the
emulation is able to reproduce from network bursts to the burst synchronization between organoids in the connected structure44 as shown
in Fig. 3C.

An additional feature of the network conﬁguration was explored
by introducing speciﬁc synaptic receptor inhibition to mimic drug
treatments, such as full antagonist to AMPAR (CNQX) and full
antagonist to GABAAR (Bicuculine) (Fig. S14). The results obtained
suggest that certain behaviors, such as epileptic seizures, could be
replicated, but would require partial receptor inhibition rather than
complete inhibition, or periodic inhibition over short durations.
The second demonstration illustrates various network conﬁgurations aimed at recapitulating the electrophysiological features of an
in vivo cortical biological network. The modeled network focuses on
the Rostral Forelimb Area (RFA) region of the rat brain with the
intention to exploit the artiﬁcial RFA to promote stimulation of the
living brain (Fig. 4A). This bio-artiﬁcial interaction aims to facilitate
adaptive intracortical microstimulation, delivered to a spared region,
the Somatosensory area (S1), via the neuromorphic biomimetic SNN,
to explore innovative strategies of open-loop electroceutical for brain
repair as in17.
The network conﬁgurations utilize up to 1024 neurons distributed
as FS neurons connecting with GABAAR for inhibition and RS neurons
connecting with AMPAR for excitation, similarly to the previous
example. However, this demonstration case introduces a network
topology in a brain-like fashion, composed by a set of clusters with a
higher density of connections within and fewer connections among
them48, as depicted in Fig. 4B. The synaptic connection rule followed a
close neighbor pattern. The parameters were swept to replicate the in
vivo recorded activity. This illustrates how the network can be

Nature Communications | (2024)15:5142

5

## PDF page 6

<b>Article</b>
https://doi.org/10.1038/s41467-024-48905-x
B
60
Number of synapses received
50
40
0
30
<b>Biological Neural Network</b>
<b>Spiking Neural Network</b>
20
(BNN)
(SNN)
<math>10^{4}</math>
<math>10^{4}</math>
<math>10^{4}</math>
Mean Firing Rate
<math>10^{3}</math>
<math>10^{3}</math>
103
All SNNs
Mean Bursting Rate (burst/min) <math>10^{\circ}</math> <math>10^{\circ}</math> <math>10^{\circ}</math> <math>10^{\circ}</math>
Mean Firing Rate (spike/s)
Best SNN
Burst Duration (ms) 10<sup>1</sup>
<math>10^{2}</math>
<math>10^{1}</math>
Mean Bursting Rate
0 0.2 0.4 0.6 0.8
<math>10^{0}</math>
10°
<math>10^{-1}</math>
<math>10^{-1}</math>
<b>Burst Duration</b>
BNN BNN
SNN
■ BNN
____BNN
SNN
SNN
10-2
10-2
<math>10^{-2}</math>
E
BNN
SNN
0.00
000
0 00
.....
.. .. .. .
. .... .. ...
Z
. . . . . . . . . . . . . . . . . . . . 
_______________________________________
::::::::::::::::::::::::::::::::::::::
:.
. . . . . . . . . . . . . . . . . . . . 
******
. . . . . . . . . . . . . . . . . . . . 
.. .. . .. . . . .
. ...
_______________________________________

. . . . . . . . . . . . . . . . . . . . 
... . .
...
Time (s)
Time (s)
5s
5s
Fig. 4 | Example network configuration based on rostral forelimb area of
configurations maximizing the similarity to the BNN group). <b>D</b> Distribution of the
rat brain. The data represented corresponds to a dataset comprising the 6 best
Mean Firing Rate (MFR), Mean Bursting Rate (MBR) and Burst Duration (BD) for the
Spiking Neural Network (SNN) among the 80 tested configurations and recordings
best SNN (977 neurons) and the 6 BNNs (282 neurons). Data are summarized in
of 6 Biological Neural Networks (BNN). A Representation of the BNN modeling
violin plots, where the outlines illustrate kernel probability density, i.e. the width of
according to a brain-like clustered network topology for the SNN. The network
the shaded area represents the proportion of the data located there. Inside, the box
configuration was exported from BiœmuS software. The rodent head was cropped
plots (grey) where the horizontal lines denote the 25th and the 75th percentile
from the work of Servier (https://creativecommons.org/licenses/by/3.0/).
values, the central white line the median value and the whiskers denote the 5th and
<b>B</b> Synaptic connectivity map showing the number of the synapses received per
the 95th percentile values. <math>p = 0.9626</math> for MFR, <math>p = 0.7944</math> for MBR, <math>p = 0.7279</math> for
neuron for the best configuration. C Radar plot comparing the fitting of the 80 SNN
BD non-parametric Mann-Whitney Rank Sum test (two-sided hypothesis test). <b>E</b> 30-
configurations to BNNs in terms of Mean Firing Rate (MFR), Mean Bursting Rate
s raster plots of the best SNN compared to the spiking activity of a
(MBR) and Burst Duration (BD). Highlighted in green are the 6 best SNNs (i.e. those
representative BNN.
configured to adapt to a different connectivity model using the pro-
configurations was chosen, i.e. those which maximized the similarity to
vided configuration scripts.
the BNNs.
A total of 80 distinct configurations were simulated, varying
The biomarkers related to these configurations were juxta-
parameters related to synaptic noise, synaptic weight, and the ratio of
posed with the biological data according to MFR, MBR and BD
inhibitory/excitatory neurons. These configurations were then com-
in Fig. 4D. No significant difference between the SNN and the
pared with the biological recordings according to three main bio-
BNN was observed for the three metrics indicating the high level of
markers, specifically Mean Firing Rate (MFR), Mean Bursting Rate
performances of our SNN in emulating the activity of the BNN.
(MBR) and Burst Duration (BD) as summarized in Figs. 4C, D. Data was
The absence of statistical significance was demonstrated by per-
forming a Mann–Whitney <i>U</i>-test (Table S5). Additionally, raster plot
collected from the RFA area (i.e. the BNN) of 6 different Long Evans
rats. Then, aforementioned metrics were computed for both the BNNs
visualization for comparison was provided in Fig. 4E, highlighting
and the 80 SNNs, to derive a grade reflecting differences between two
similarity in the spiking activity between the best SNN and one
types of networks. From the radar plot of Fig. 4C, a subset of 6 SNN
representative BNN.
Nature Communications | (2024)15:5142
6

## PDF page 7

<b>Article</b>
https://doi.org/10.1038/s41467-024-48905-x
<b>HD-MEA</b>
<b>BioemuS</b>
Host computer
2
<b>Custom Python script</b>
<b>KR260</b>
Maxwell One HD-MEA system
Vetwork
Stimulation
burst?
Network
Stimulation
burst?
excitatory neuron
▲ stimulation to BioemuS

    left organoid

inhibitory neuron
right organoid
stimulation to HD-MEA
stimulated neuron
é siet produkté a
or a law list a stack
t mid e samular
aran zaidaa
38/59
414, 501, 20
ACCOMPANY)
甲烷四唑
182
180
184
186
188
Time (s)
<b>BioemuS</b>
In-vivo stimulation
B
INTAN RHS
Fig. 5 | Prototypes of biohybrid setups integrating BiœmuS. A Closed-loop
time stamps <math>\pm 100</math> ms. The raster plot is generated from python. The experiment
interaction between connected organoids plated on HD-MEA system and single
was replicated 3 times with similar results using different detection threshold. B In
organoid emulated on BiœmuS. The network burst detected in the left organoid of
vivo stimulation driven by BiœmuS spiking activity as a model of post stroke
rehabilitation via biomimetic neural pattern stimulation. The spiking activity of the
the connectoid triggers stimulation on exterior neurons of the emulated single
organoid on BiœmuS. The network burst detected in the activity of BiœmuS trig-
SNN triggers stimulation on an in vivo culture using the INTAN RHS2116 headstage.
gers stimulation on the right organoid of the connectoid. Detection and stimulation
Electrode arrays were placed in the rostral forelimb area (RFA) and in the primary
commands are carried out in different threads. Stimulation of BiœmuS is per-
somatosensory area (S1) in the brain of adult Long-Evans rats. The experiment was
replicated 5 times and the entire dataset has been analyzed with no discrimination
formed using the external stimulation slot. BiœmuS stimulation triggers are shown
by blue triangles and stimulation to HD-MEA by red triangles. BiœmuS is running
among animals in<sup>17</sup>. The network configuration and action potentials were exported
for 180 s starting from 180 s and synchronized with HD-MEA activity from collected
from Biœmus software.
Prototypes of biohybrid experiments
Connected organoids were plated on HD-MEA to interact with an
This section presents examples of biohybrid experiments using the
artificial neural network and allow a clear delimitation between
system to interact with commonly used recording interfaces. It aims to
recording and stimulation sites. Electrodes were configured to allow
show how different network configurations of the system from single
activity recording on left and right organoids while allowing stimula-
neuron to larger network can interact with biological counterpart,
tion of the right organoid based on an activity scan and stimulation
whether in vitro or in vivo, through various interfaces.
electrodes were manually selected among the ones exhibiting the
A first demonstration case supporting the versatile integrability of
most activity (Fig. S16). A single organoid was modeled using BiœmuS
with a network of 1024 neurons emulated for 180 s. The closed-loop
the system with existing solutions for biological interfacing is a closed-
loop stimulation between BiœmuS and the new generation of HD-MEA
was controlled by a Python application running on a 'gateway' com-
(High-Density MicroElectrode Array)<sup>49</sup> (Fig. 5A). HD-MEA was selected for
puter responsible for control, activity scan and stimulation, that will be
referred to as the closed-loop software. Spiking activity of BiœmuS was
this demonstration case as a promising recording device garnering more
attention and becoming more widespread in closed-loop setups<sup>50,51</sup>.
forwarded to the gateway computer using ZeroMQ over Ethernet and
Nature Communications | (2024)15:5142
7

## PDF page 8

Article

https://doi.org/10.1038/s41467-024-48905-x
Logic

Memory
DSP

0%

10%

20%

40%

50%

Synapses

Neurons

30%

50%

60%

70%

80%

90%

100%

80%

90%

100%

Monitoring

VC

U

11

8

VP
K1

20

VP
K1

80

KR260

30%

0%

10%

Projected

20%

40%

Logic

60%

Memory

70%

DSP

Fig. 6 | Hardware resource utilization. Utilization for main modules implemented
on AMD Xilinx KR260 Robotic Starter Kit and projected on high-end evaluation
boards from AMD Xilinx (Versal Premium Series VPK120 and VPK180 Evaluation

Kits and Virtex UltraScale+ VCU118 Evaluation Kit). Logic; LUT and Flip-Flops.
Memory; total memory implemented as BRAM and URAM. DSP; number of Digital
Signal Processing (DSP) slices.

stimulation was sent using ZeroMQ on the external stimulation port of
BiœmuS. A stimulation was sent to the HD-MEA when a network burst
occurs on BiœmuS.
The closed-loop software controlling both systems records
activity of HD-MEA before and after the closed-loop for 180 s while
collecting time stamps of stimulation triggers. This experiment
showcases the potential of BiœmuS to operate as a tool to study the
impact of adaptive stimulation on a culture following the principles of
electroceutics, while highlighting its ability to adapt to a standard
biophysical interface. The beneﬁt of the user-deﬁned model through
customizable Python scripts to adapt to a speciﬁc application is also
showcased here by assigning XY coordinates to neurons to take
advantage of the spatial resolution provided by the HD-MEA.
The results obtained show that the closed-loop successfully triggers stimulation to both systems, however evaluating latencies and
handling stimulation artifacts are limitations of the experiment setup.
Precise synchronization of both systems would require additional
development such as adding Precision Timing Protocol (PTP) to synchronize both system clocks or better characterization of the latency
induced by the HD-MEA API as the latencies of BiœmuS already have
been characterized (Figs. S18, S21, S22 S23). As observed in Fig. 5A,
stimulation artifacts are captured by the Maxlab Software, hence
potentially inducing uncontrolled escalation as artifacts are considered as spiking activity.
A second type of interaction with the living thanks to the real-time
behavior of BiœmuS is to drive an open-loop in vivo stimulation by the
SNN17 as shown in Fig. 5B. This open-loop stimulation was applied to rat
brains as a neuromorphic-based open-loop set-up for neuroprosthetic
applications with the ultimate goal to be exploited in post-stroke
rehabilitation studies6,7. The spikes from neurons emulated by BiœmuS become inputs to the INTAN RHS recording/stimulation unit to
trigger stimulation in S1 (somatosensory area), to mimic the Activity
Dependent Stimulation (ADS) paradigm in which spikes from RFA
trigger stimulation in S152,53.
The spontaneous behavior of the neurons is tuned to obtain slow
or fast activities by tuning the parameters of the equation ruling the
synaptic noise17. In this setup, the latency between spike detection in
the SNN and stimulation is less than a millisecond.

Performances

Nature Communications | (2024)15:5142

The low-cost platform targeted is the AMD Xilinx Kria KR260 Robotics
Starter Kit carrier board embedding the K26 SOM by AMD Xilinx (Zynq
Ultrascale+ MPSoC architecture). This entry level platform is capable
of running 1024 neurons with 6 conductance-based currents for a total
of 220 conductance-based synapses running in hard real-time with a
time step of 31.25 μs. The system can also run on AMD Xilinx Kria
KR260 Vision Starter Kit carrier board with for only restriction the
number of PMODs, preventing concurrent use of DAC waveforms and
Wi-Fi spike monitoring. The system is also compatible with Petalinux, a
lighter operating system for AMD Xilinx targets facilitating tuning of
the Linux kernel to enable functionalities such as pre-emptive
scheduling.
While most of the memory available is used, less than 50% of the
computing capacity (Logic and Digital Signal Processing slices) of the
board is used by the system (Fig. 6). As the design is implemented on
an entry level target, the projection of the resources utilization on
larger targets suggests the possibility to run several calculation cores
in parallel (Fig. 6) as well as allowing faster emulation. The porting of
the computation core is greatly facilitated by the use of High Level
Synthesis design for computation modules allowing faster generation
of optimized hardware for a given target.
The average latency observed to send spikes through ZeroMQ is
typically under 500 μs (Fig. S23). The average latency observed for
spike monitoring through Wi-Fi using ESP32 is between 0.792 ms and
2.098 ms (Fig. S21) depending on the data collection interval. The
different paths of monitoring implemented allow ﬁnding compromises between throughput, latency and data integrity, providing a
great ﬂexibility in adapting to user requirements. Overall system
power consumption is 6.50W with 3.42W associated with the calculation core (Fig. S20).

Discussion
In this paper, we introduce BiœmuS, a low-cost, embedded, ﬂexible
and real-time biomimetic tool, which allows to perform biohybrid
experiments for real-time emulation of living systems.
Our embedded system offers a real-time, cost-effective and userfriendly solution for closed-loop applications, addressing accessibility

8

## PDF page 9

Article
challenges prevalent in current high-performance alternatives. Unlike
server-based infrastructures or complex systems like TrueNorth,
SpiNNaker and BrainScaleS-2, which can be expensive and difﬁcult to
integrate into experimental setups, our solution prioritizes simplicity
and accessibility. Notably, even software alternatives like Brian or
NEURON, despite GPU acceleration, frequently struggle to achieve the
low latencies necessary for closed-loop application.
Thanks to its straightforward setup facilitated by Python scripts, the
system becomes easily accessible to neuroscientists, ensuring they can
efﬁciently utilize its capabilities without being overwhelmed by technical
difﬁculties. Additionally, thanks to the generic Ubuntu operating system
handling communication, the system is capable of implementing a
variety of complex protocols such as USB 3.0, USB 2.0 or Ethernet while
maximizing software compatibility. Thus, our solution greatly facilitates
integration, overcoming the usual drawback of time-consuming and
technically intricate programming associated with low-level FPGA
development. While non real-time operating systems as Ubuntu induce a
discernible and ﬂuctuating latency, using PL driven interrupt and AXI
DMA allows obtaining relatively low latency about the tens of microseconds where the biological time is deﬁned to one millisecond. A tradeoff between latency and compatibility/versatility can be found by using
solutions such as data sent directly by PL through expansion PMODs or
ESP32, real-time operating system or running the application on the realtime cores of the chip. Nonetheless, direct monitoring on the PL that
drastically reduces the latency remains possible using the various connectors of the board such as PMOD interface, GPIO or SFP.
On the current target, the main bottleneck lies in the memory usage
essentially allocated for synapses weights and premultiplied rate tables
for ion channel states. Since the current target is using a preceding
architecture, more efﬁcient architectures of memory can be found in
recent larger targets such as High Bandwidth Memory (HBM) that integrates DRAM directly into the FPGA package, thus providing drastically
higher depth and bandwidth. Latest AMD Xilinx chips also incorporate
adaptive SoCs that provide signiﬁcantly higher computation power
(Fig. 6), notably with native ﬂoating-point DSP and AI engine while still
embedding a Zynq for setup and control. Hence porting a similar
architecture of SNN on these targets would signiﬁcantly increase performances and create a promising alternative to standard GPU.
While the use of a complex neuron model limits the number of
neurons that can be implemented, our system derives several beneﬁts
from this approach in various aspects. The use of the Hodgkin-Huxley
(HH) model signiﬁcantly facilitates interaction with neuroscientists, as
it relates to biophysical parameters, unlike the simpler Leaky Integrateand-Fire (LIF) or Izhikevich model. The system notably proved that the
network is able to maximize ﬁtting for speciﬁc parameters as highlighted by the rat brain network conﬁgurations or to replicate biological dynamics such as burst synchronisation between connected
organoids. Even using generic parameters of FS and RS cortical neurons from38 and less neurons that the biological counterpart, network
conﬁgurations maximizing ﬁtting for speciﬁc biomarkers could be
obtained by tuning the parameters of the network. Hence, the system
can be suited for closed-loop experiments focusing on certain biomarkers, as in17, where the primary focus is the MFR.
The open-loop in vivo biohybrid experiment promoted the use of
BiœmuS as a tool to investigate stroke rehabilitation with an electroceutic approach by providing stimulation following a biomimetic
neural pattern. The preliminary results presented in17, that show efﬁciency to increase the ﬁring activity of both RFA and S1 compared to
the pre-stimulation condition thanks to the neural biomimetic stimulation pattern, suggest that the biomimetic SNN contribute to improve
the rehabilitation. These results support the hypothesis suggesting
that a neural biomimetic pattern more effectively entrains the network
in response to stereotyped stimulation, making the population tend to
be more responsive to incoming electrical stimuli, which is in line with

Nature Communications | (2024)15:5142

https://doi.org/10.1038/s41467-024-48905-x

recent human studies54. Hence, driving stimulation from a connected
network instead of a single stochastic neuron with BiœmuS would
allow further investigation of that hypothesis and more globally of
stroke rehabilitation in an electroceutic approach by providing
activity-dependent stimulation.
The current experimental setup for the closed-loop biohybrid
experiment with the HD-MEA shows certain limitations. Nonetheless,
thanks to the architecture of BiœmuS that runs a commercial Linux,
solutions including more speciﬁc design directly controlling and
transferring the data from the HD-MEA to the hardware part for realtime processing could be considered. Furthermore, this experimental
setup beneﬁts from a facilitated tuning of the stimulation patterns or
protocols by changing the parameters of the different conﬁguration
ﬁles. The HD-MEA setup could be extended to implement closed-loop
electroceutical interventions, emulating the dynamics of neurological
disorders like Parkinson’s or ALS, ultimately aiming to restore normal
biological function.
The system has proven its ease of integration demonstrated by
the biohybrid experiments conducted on some of the most widespread biophysical interface with low-level communication protocol
(pulse on digital output) as well as complex communication protocols
(Wi-Fi and Ethernet). The ease of use and ﬂexibility also have been
particularly promoted by the examples of network conﬁgurations
showing examples of different complex networks created from customizable Python scripts (Figs. 3, 4). The experiment in Fig. 5A also
highlighted this feature by interfacing the BiœmuS to a biophysical
interface using only Python scripts. While the accurate modeling of
large network dynamics is constrained by the number of implemented
neurons, the real-time processing capability of the SNN, coupled with
interconnections at various latencies and throughputs, makes it a
valuable tool for closed-loop setups.
The presented applications demonstrate the ﬂexibility of BiœmuS
in adapting to the study of various biological processes, including the
potential for neuroprostheses replacement through closed-loop
in vitro stimulation driven by BiœmuS (Fig. 5A) and post-stroke rehabilitation through in vivo stimulation (Fig. 5B).

Methods
SNN modeling
The neurons composing the network are modeled using the HodgkinHuxley paradigm37, the most biomimetic model considering the biophysical meaningfulness as an essential criterion55. The biophysically
meaningful nature of the model being essential to relate parameters of
the models to biology. The model of cortical neuron implemented is
based on the Pospischil model38 that features 6 conductance-based
currents allowing emulation of 4 classes of cortical neurons being “fast
spiking” (FS), “regular spiking” (RS), “intrinsically bursting” (IB) and
“low-threshold spike” (LTS). A current mimicking intrinsic noise
observed in the brain following an Ornstein-Uhlenbeck process39,40 is
injected to reproduce spontaneous activity by triggering action
potentials on a biomimetic basis.
The different conductance-based synaptic receptors are modeled
using the biologically meaningful Destexhe model41 allowing emulation of AMPAR, NMDAR, GABAAR and GABABR.
The noise seeds are generated by the PS and sent through AXI
LITE to the noise generator thus allowing true random seeds as well as
ﬁxed seeds for debugging.
The computation of ion channel states is based on ‘premultiplied’
HH rate function tables similarly to56, allowing computation of each HH
variable from a single multiply and add from table values looked-up
based on the membrane voltage (Eq. (1)). This method eliminates the
FPGA-speciﬁc limitations for complex mathematical functions such as
division and exponential. A trade-off between accuracy and resource
utilization can be balanced with the size of memory implemented to

9

## PDF page 10

Article

https://doi.org/10.1038/s41467-024-48905-x

System monitoring and control

store the rate function tables (Fig. S6).
x n + 1 = r 1 ðV n Þ × x n + r 2 ðV n Þ

ð1Þ

where, xn+1 and xn are respectively the new and current value of the ion
channel state, Vn is the membrane voltage at previous time step, r1 and
r2 are the ion rate tables decoded from the membrane voltage.
Applied to common equations of ion channel states, the premultiplied tables can correspond to Eqs. (2), (3) and Eqs. (4), (5).
r 1 ðV Þ = 1  dt × ðαx ðV Þ + βx ðV ÞÞ

ð2Þ

r 2 ðV Þ = dt × α x ðV Þ

ð3Þ

dt
taux ðV Þ

ð4Þ

dt × x 1 ðV Þ
taux ðV Þ

ð5Þ

r 1 ðV Þ = 1 

r 2 ðV Þ =

where, r1 and r2 are the pre-computed rate table for ion channel states
decoded from the membrane voltage, dt the time step in ms,
taux, x∞, αx and βx the equation of the ion channel state depending
on the formalism used.
The step and range of the tables are tunable from software but the
generic rate table size is ﬁxed in hardware to 2048 (1 BRAM) that
provides a good compromise between accuracy and resource usage.
The default range is set to −76 mV to 52 mV that covers the amplitude
range for the preset neurons. Temporal discretization using a small
time step compared to the dynamics is chosen to allow numerical
solving using the Euler-Maruyama’s method.

FPGA design
In PL part, the computation core is clocked at 400 MHz, the AXI
communication to PS at 200 MHz and external components on PMOD
connectors such as DAC and ESP32 at 50 MHz. The use of multiple
clocks is justiﬁed by hardware limitations of components and blocks,
multiple clocking allows all parts of the design to work close to their
maximum to maximize performances. Crossing clock domain is handled by dual clock BRAM and FIFO for most critical signals, the
remaining signals are either handled by double ﬂip-ﬂops or extended.
The computation core is fully pipelined.
Computation of ion channels states and currents are encoded
using 32-bit ﬂoating-point. It grants good stability and accuracy to the
computation of ion channels that are critical parts of the neuron
dynamics. Since ion currents can have different dynamics potentially
smaller in comparison to other currents, ﬂoating-point coding is more
suited for most computation and especially for multiplications
(Fig. S10). Calculation of the current sum and Euler Murayama’s
method are encoded using 32-bit ﬁxed-point. Large ﬁxed-point coding
for sum operations allows to save resources and computation latency
compared to ﬂoating-point, while guaranteeing consistent accuracy.
The synaptic noise and synapses that have less critical accuracy or
perform well with ﬁxed-point coding are computed with 25 and 18 bits
ﬁxed-point encoding to ﬁt the ranges of DSP slices. The injected stimulation current only involved in the ﬁnal sum is coded using 32-bit
ﬁxed-point. Synaptic weight is coded on 14 bits and can be multiplied
by a factor speciﬁed in software to mimic a larger network behavior.
The numerical solver used is the Euler-Maruyama with a small
time step compared to the system dynamics to guaranty stability
(31.25 μs)36. To maximize performances and limit resources usage, DSP
of the boards were inferred using macros for most operations. The
model is validated using Python implementation emulating both premultiplied rates and ﬁxed-point coding.
Nature Communications | (2024)15:5142

The PS part is running the Canonical Ubuntu 22.04 for ZynqMP
architecture. The main application controlling the SNN is coded and
compiled in C++11. Setup from the PS to the PL is implemented by AXI
LITE controlled through /dev/mem in the C++ application.
Communication between the PL to PS is implemented using AXI
DMA controlled by the the C++ application using the dma_proxy driver
provided by AMD Xilinx. The application implements a thread for each
AXI DMA channel and cyclic buffers for AXI DMA transfers.
The Ethernet communication implements ZeroMQ Push-Pull
messaging pattern with a different port for each data (spikes, waveforms, and external stimulation) that can be set from the JSON
conﬁguration ﬁle.
The interval of data collection can be set from the JSON conﬁguration ﬁle from 1 ms to 255 ms for spike collection via DMA, from
3.125 ms to 15 ms for the waveforms collections. The Wi-Fi connection
is using UDP protocol and the data collection interval can be set from
2 ms to 20 ms. The spikes can be saved and stored using different
formats. Sending formats are either binary encoded (one bit per neuron) or as a cumulative sum for each neuron. Saving formats are either
binary encoded or comma separated.
The data collection interval for the spikes and waveforms through
the DMA can impact the load of the application, especially with non
binary streams that create dependence with the activity of the network. A small interval will generate more frequent write in ﬁle or frame
sending thus increasing the CPU load. The limit corresponds to a data
collection interval smaller than the writing or sending time of the
frame therefore blocking the software in a thread.
The data collection interval for Wi-Fi forwarding is limited by the
hardware and latency of the Wi-Fi protocol so as high intervals generate
too large buffers and too small interval may generate packet losses.
DMA-based monitoring can run local saving and Ethernet forwarding concurrently in most cases with large data collections interval
but may dysfunction on small intervals due to processor performances. Spikes and waveforms monitoring through DMA can run
concurrently in separate threads but may also dysfunction on small
data collection intervals due to processor performances.
Wi-Fi, DAC and DMA-based monitoring can run concurrently
without impact on performances. Bash scripts are used to compile the
software, update the ﬁrmware and launch the application.
An external stimulation controlled via Ethernet over ZeroMQ
allows to send a stimulation of a given time to a given neuron by
passing the stimulation duration for each neuron to the PL using the
AXI DMA (Fig. S4).

Network conﬁguration
Connected cortical organoids. The “single” physically separates the
organoids to prevent connection. The “connected organoids”, or
connectoid, places organoids millimeters apart while constraining the
interconnection to a channel of 150 μm width46,47. The emulation
model implements cortical neurons using FS and RS types connected
by AMPAR and GABAAR.
The synaptic connection rules for the synaptic connections inside
organoids are ruled by Eq. (6) that favors connection to neurons close
to each other normalised by the diameter of organoid. The connections between organoids are ruled by Eq. (7), relying on the location of
neurons in the organoid to promote connections in the exterior ring.

psingle = pmax × 1 

pconnectoid = pmax ×

d npre ,npost

!
ð6Þ

r org

d npre ,org pre d npost ,org post
1
×
+
2
r org pre
r org post

!
ð7Þ

10

## PDF page 11

Article

https://doi.org/10.1038/s41467-024-48905-x

where pmax is the maximum probability of connection, d is the distance, r the radius, npre and npost the pre-synaptic and post-synaptic
neurons, orgpre and orgpost the center of the pre-synaptic and postsynaptic organoids.
The recordings were performed using the MED64 system (Alpha
MED Scientiﬁc) and electrical signals were recorded at 37 °C at
20,000 Hz sampling rate. The recording noise was eliminated by bandpass ﬁlter between 0.1 and 10,000 Hz during the measurement, then
ﬁltered ofﬂine with a band-pass ﬁlter (300–3000 Hz) for spike analysis.
Spikes were considered using a threshold of ±5 σ, where σ represents
the standard deviation of the baseline noise during quiescent periods.
The characterization of the ﬁring activity was conducted using Python.
The analysis focused on Inter-Spike Interval (ISI, ms), Mean Firing Rate
(MFR, spikes/s), Inter-burst interval (IBI, ms) and burst length (ms). The
burst detection was performed according to57 using the string method
(i.e. a max inter-spike interval of 100 ms and 5 ms as minimum number
of intra-burst spikes).
Rat Rostral forelimb area. A total of six adult, male, Long-Evans rats
(weight: 300–400 g, age: 2–4 months; Charles River Laboratories,
Calco, LC, Italy) were used in this study. The experiments were conducted at the Animal Facility of the Italian Institute of Technology (IIT)
in Genova, Italy, with prior authorization granted by the Italian Ministry of Health and Animal Care (Italy: authorization n. 509/2020-PR).
For detailed surgical procedures, please refer to58.
Recording of wide-band signals from the rostral forelimb area
(RFA) and primary somatosensory area (S1) were carried out using 16channel microelectrode arrays (MEAs) (A4 × 4–5 mm-100-125-703-A16,
NeuroNexus) connected to Intan RHS headstages. These MEAs were
part of a bidirectional electrophysiology interface system equipped
with 16 stimulation/ampliﬁer channels linked to the probes.
All the preprocessing analyses of the in-vivo recordings, up to
their spike sorting, were performed in MATLAB (The MathWorks,
Natick, MA, USA). The ePhys data underwent preprocessing via a
custom MATLAB pipeline, including a 4th order elliptic bandpass ﬁlter
(300–3000 Hz) to eliminate low-frequency components. A powerbased spike detection algorithm known as Stationary Wavelet-based
Teager Energy Operator (SWTTEO)59 was employed to identify spikes
from the ﬁltered data. The SWTTEO involved two levels of Stationary
Wavelet Transform (SWT) paired with the use of the Teager Energy
Operator (TEO). The TEO outputs were smoothed, summed, and their
combination was thresholded. Subsequently, multiunits were sorted
using a mixture of skew-t distributions on PCA-extracted features,
following the approach outlined in60.
The characterization of the ﬁring activity of both the biological
and artiﬁcial neural networks was performed using Python. The analysis focused on several biomarkers including Mean Firing Rate (MFR,
spikes/s), Mean Bursting Rate (MBR, bursts/min) and Burst Duration
(BD). The burst detection was performed according to57 using the
string method (i.e. a max inter-spike interval of 100 ms and 5 ms as
minimum number of intra-burst spikes).
The comparison with biological networks was graded as the
absolute values of differences normalized considering the maximum
and minimum values of each biomarker among all conﬁgurations,
following Eq. (8):
Grade = 1 

jdif f i,m j  minðjdif f m jÞ
maxðjdif f i,m j  minðjdif f m jÞÞ

ð8Þ

where diffi,m is the i-th difference between the m-th biomarker of the
i-th BiœmuS network conﬁguration and the target value of the same
biomarker of the biological network. To evaluate statistically signiﬁcant differences, among the two conditions (SNN group vs BNN
group) we adopted the non-parametric Mann–Whitney U-test Figure.
P-values were set at 0.005.

Nature Communications | (2024)15:5142

Biohybrid experiments
Closed-loop biomimetically driven stimulation on HD-MEA. The bidirectional communication between BiœmuS and the HD-MEA system
is ensured by Python scripts running on a gateway computer that will
be referred to as the closed-loop application. The HD-MEA was conﬁgured to record from channels both from left and right organoid
based on an activity scan and to select stimulation electrodes on the
right organoid (Fig. S16). The HD-MEA is the MaxOne chip of MaxWell
Biosystems AG49.
The spiking activity of the HD-MEA and BiœmuS were collected
at a period of 1 ms. The spikes received from BiœmuS on the host
computer are analysed to detect the occurrence of a network burst.
The network burst detection is computed using a sliding window of
the total activity of the network over a period of 10 ms. Upon burst
detection, a stimulation consisting of a 500 μs pulse of amplitude
500 mV sent to the HD-MEA using custom Python script derived
from manufacturer’s templates. The stimulation was chosen
according to the values used in the work50 that proved efﬁcacy on a
similar setup.
The spikes received from the HD-MEA triggered stimulation on
BiœmuS upon detection of a network burst. The network burst of the
HD-MEA activity was calculated from a sliding window on 250 ms of
activity. The stimulation was sent through Ethernet over ZeroMQ to
the external stimulation port of BiœmuS to trigger a stimulation of
duration 3.120 ms and amplitude 0.03 mA/cm2 to neurons on the
exterior ring of the organoid.
The network burst latency was estimated to be inferior to 10 μs in
most cases (Fig. S18). The closed-loop application ran a thread for each
task of receiving spikes from HD-MEA, receiving spikes from BiœmuS,
sending stimulation to Maxwell and sending stimulation to BiœmuS.
The activity recording of the HD-MEA was controlled by the
closed-loop application. The closed-loop application sent a ﬁrst stimulation trigger to BiœmuS to start the SNN in the same time as
enabling the closed-loop. The activity of the HD-MEA was analyzed
using the script provided by the manufacturer. The spiking activity of
BiœmuS was recorded on-board. An interface executed in another
thread was displaying the summed activity of both networks along
with thresholds for visual control.
The electrode conﬁguration of the HD-MEA was exported from
the software. The XY conﬁguration of neurons, network conﬁguration
and stimulated neurons of BiœmuS were exported from the Python
scripts. Detection of bursts and spikes triggering stimulation for both
HD-MEA and BiœmuS were reconstructed from the time stamps collected. The synchronization of both activities was done from time
stamp collections with a certainty of 100 ms based on the ﬂuctuating
latency to start the recording of the HD-MEA activity.
Organoid cultures. The use of human iPS cells was approved by the
Institute of Industrial Science, The University of Tokyo and cells were
handled in accordance with approved protocols. Human iPS cells were
obtained from the Riken Cell Bank (409B2, HPS0076) and maintained
on ESC-qualiﬁed Matrigel-coated 12-well plates in mTeSR plus medium
(STEMCELL Technologies) and passaged every 5–7 days using ReLeSR
reagent (STEMCELL Technologies). Cortical connectoids were generated using previously reported protocol44. Brieﬂy, hiPSCs were dissociated using TrypLE Express and 10,000 cells per well were seeded
into U-bottom ultra-low attachment 96 well plate (Prime surface,
Sumitomo bakelite) in mTeSR plus supplemented with 10 μM of
Y-23632. 24h later, media was replaced with neural induction media
(NIM), consisting of DMEM-F12 with HEPES, 15% (v/v) knockout serum
replacement, 1% (v/v) minimal essential media non-essential amino
acids (MEM-NEAA), and 1% (v/v) Glutamax, supplemented with 100 nM
LDN-193189, 10 μM SB431542, and 5% (v/v) heat-inactivated FBS. On
day 2, NIM was replaced without the supplement of FBS and changed
every other day until day 10.
11

## PDF page 12

Article
From day 10 to 18, culture medium was replaced and changed
every other day with neural differentiation media 1 (NDM1), consisting
of 1:1 mixture of DMEM/F12 with HEPES and Neurobasal medium, 0.5%
(v/v) N2 supplement, 1% (v/v) B27 supplement without vitamin A, 1% (v/
v) Glutamax, 0.5% (v/v) MEM-NEAA, 0.25 mg/ml human insulin solution, and 1% (v/v) Penicillin/Streptomycin/Amphotericin (PSA) (Sigma,
A5955). On day 18, culture medium was replaced with neural differentiation media 2(NDM2), consisting of Neurobasal medium, 0.5% (v/
v) N2 supplement, 1% (v/v) B27 supplement with vitamin A, 1% (v/v)
Glutamax, 0.5% (v/v) MEM-NEAA, 0.25 mg/ml human insulin solution,
200 mM ascorbic acid, and 1% (v/v) PSA, supplemented with 20 ng/ml
brain derived neurotrophic factor (BDNF). On day 28, culture media
was replaced with Neural Maintenance Media (NMM) consisting of
Neurobasal Medium, supplemented with 2% (v/v) B27 supplement with
vitamin A, 1% (v/v) Glutamax, 1% (v/v) PSA and 20 ng/ml BDNF.
Cortical organoids were subjected to connectoid formation after
at least 28 days in culture. Here, a custom-made microﬂuidic device
containing two holes which are connected through a narrow channel
were bonded on a CMOS-based HD-MEA (MaxOne+, Maxwell Biosystems). Microchannel of the microﬂuidic device was coated with 2%
Matrigel (Corning) in DMEM/F12 for 1 h at room temperature (RT).
Next, coating solution is replaced with NMM and an organoid is placed
into each of the holes. Cells were kept at 37 °C and 5% CO2 and half
media change was performed every 3–4 days for the duration of cell
culture.

Data availability
All data that support the ﬁndings of this paper are presented within the
paper and the Supplementary Materials. Additional data related to this
paper may be requested from the authors. Data on animal experiments
are available under restricted access which can be obtained by contacting the authors.

Code availability
The code related to BiœmuS is available at https://github.com/
Ceramic-Blue-Tim/bioemus and includes analysis and acquisition
scripts. Due to proprietary ownership, we do not provide open access
to the code related to the HD-MEA closed-loop experiment, access
request will be evaluated on a case-by-case basis.

References
1.

World Health Organization (WHO) The Top 10 Causes Of Death.
https://www.who.int/news-room/fact-sheets/detail/the-top-10causes-of-death (2020).
2. Chin, J. H. & Vora, N. The global burden of neurologic diseases.
Neurology 83, 349–351 (2014).
3. French, B. et al. Repetitive task training for improving functional
ability after stroke. Cochrane Database Syst. Rev. 11, CD006073
(2016).
4. Farina, D. et al. Toward higher-performance bionic limbs for wider
clinical use. Nat. Biom. Eng. 7, 473–485 (2023).
5. Bouton, C. E. et al. Restoring cortical control of functional movement in a human with quadriplegia. Nature 533, 247–250 (2016).
6. Panuccio, G. et al. Progress in neuroengineering for brain repair:
new challenges and open issues. Brain Neurosci. Adv. 2,
2398212818776475 (2018).
7. Semprini, M. et al. Technological approaches for neurorehabilitation: from robotic devices to brain stimulation and beyond. Front.
Neurol. 9, 212 (2018).
8. Famm, K., Litt, B., Tracey, K. J., Boyden, E. S. & Slaoui, M. A jumpstart for electroceuticals. Nature 496, 159–161 (2013).
9. Reardon, S. Electroceuticals spark interest. Nature 511, 18 (2014).
10. Bartolozzi, C., Indiveri, G. & Donati, E. Embodied neuromorphic
intelligence. Nat. Commun. 13, 1024 (2022).

Nature Communications | (2024)15:5142

https://doi.org/10.1038/s41467-024-48905-x
11.

Christensen, D. V. et al. 2022 roadmap on neuromorphic computing
and engineering. Neuromorphic Comput. Eng. 2, 022501 (2022).
12. Rosa, M. et al. Adaptive deep brain stimulation in a freely moving
Parkinsonian patient. Mov. Disord. 30, 1003 (2015).
13. Milekovic, T. et al. A spinal cord neuroprosthesis for locomotor
deﬁcits due to Parkinson’s disease. Nat. Med. 29, 2854–2865
(2023).
14. Lebedev, M. A. & Nicolelis, M. A. Brain-machine interfaces: from
basic science to neuroprostheses and neurorehabilitation. Physiol.
Rev. 97, 767–837 (2017).
15. Tavanaei, A., Ghodrati, M., Kheradpisheh, S. R., Masquelier, T. &
Maida, A. Deep learning in spiking neural networks. Neural Netw.
111, 47–63 (2019).
16. Donati, E. & Valle, G. Neuromorphic hardware for somatosensory
neuroprostheses. Nat. Commun. 15, 556 (2024).
17. Di Florio, M. et al. Design of an experimental setup for delivering
intracortical microstimulation in vivo via spiking neural network.
Annu. Int. Conf. IEEE Eng. Med. Biol. Soc. 1–4. https://doi.org/10.
1109/EMBC40787.2023.10340907 (2023).
18. Sharifshazileh, M., Burelo, K., Sarnthein, J. & Indiveri, G. An electronic neuromorphic system for real-time detection of high frequency oscillations (hfo) in intracranial EEG. Nat. Commun. 12,
3095 (2021).
19. Corradi, F. & Indiveri, G. A neuromorphic event-based neural
recording system for smart brain-machine-interfaces. IEEE Trans.
Biomed. Circuits Syst. 9, 699–709 (2015).
20. Hines, M. L. & Carnevale, N. T. Neuron: a tool for neuroscientists.
Neuroscientist 7, 123–135 (2001).
21. Gewaltig, M.-O. & Diesmann, M. Nest (neural simulation tool).
Scholarpedia 2, 1430 (2007).
22. Stimberg, M., Brette, R. & Goodman, D. F. Brian 2, an intuitive and
efﬁcient neural simulator. Elife 8, e47314 (2019).
23. Van Albada, S. J. et al. Performance comparison of the digital
neuromorphic hardware spinnaker and the neural network simulation software nest for a full-scale cortical microcircuit model. Front.
Neurosci. 12, 291 (2018).
24. Xu, T., Xiao, N., Zhai, X., Chan, P. K. & Tin, C. Real-time cerebellar
neuroprosthetic system based on a spiking neural network model
of motor learning. J. Neural Eng. 15, 016021 (2018).
25. Qiao, N. et al. A reconﬁgurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128k synapses.
Front. Neurosci. 9, 141 (2015).
26. Donati, E., Payvand, M., Risi, N., Krause, R. & Indiveri, G. Discrimination of emg signals using a neuromorphic implementation
of a spiking neural network. IEEE Trans. Biomed. Circuits Syst. 13,
795–803 (2019).
27. Davidson, S. & Furber, S. B. Comparison of artiﬁcial and spiking
neural networks on digital hardware. Front. Neurosci. 15, 651141
(2021).
28. Serb, A. et al. Unsupervised learning in probabilistic neural networks with multi-state metal-oxide memristive synapses. Nat.
Commun. 7, 12611 (2016).
29. Serb, A., Khiat, A. & Prodromakis, T. Seamlessly fused digitalanalogue reconﬁgurable computing using memristors. Nat. Commun. 9, 2170 (2018).
30. Covi, E. et al. Analog memristive synapse in spiking networks
implementing unsupervised learning. Front. Neurosci. 10, 482
(2016).
31. Merolla, P. A. et al. A million spiking-neuron integrated circuit with a
scalable communication network and interface. Science 345,
668–673 (2014).
32. Pehle, C. et al. The brainscales-2 accelerated neuromorphic system
with hybrid plasticity. Front. Neurosci. 16, 795876 https://doi.org/
10.3389/fnins.2022.795876 (2022).

12

## PDF page 13

Article
33. Painkras, E. et al. Spinnaker: a 1-w 18-core system-on-chip for
massively-parallel neural network simulation. IEEE J. Solid-State
Circuits 48, 1943–1953 (2013).
34. Davies, M. et al. Loihi: a neuromorphic manycore processor with onchip learning. IEEE Micro 38, 82–99 (2018).
35. Stradmann, Y. et al. Demonstrating analog inference on the
brainscales-2 mobile system. IEEE Open J. Circuits Syst. 3,
252–262 (2022).
36. Khoyratee, F., Grassia, F., Saïghi, S. & Levi, T. Optimized real-time
biomimetic neural network on FPGA for bio-hybridization. Front.
Neurosci. 13, 377 (2019).
37. Hodgkin, A. & Huxley, A. A quantitative description of membrane
current and its application to conduction and excitation in nerve.
Bull. Math. Biol. 52, 25–71 (1990).
38. Pospischil, M. et al. Minimal hodgkin-huxley type models for different classes of cortical and thalamic neurons. Biol. Cybern. 99,
427–441 (2008).
39. Destexhe, A., Rudolph, M., Fellous, J. M. & Sejnowski, T. J. Fluctuating synaptic conductances recreate in vivo-like activity in neocortical neurons. Neuroscience 107, 13–24 (2001).
40. Grassia, F., Kohno, T. & Levi, T. Digital hardware implementation of a
stochastic two-dimensional neuron model. J. Physiol. Paris 110,
409–416 (2016).
41. Destexhe, A., Mainen, Z. F. & Sejnowski, T. J. Kinetic models of
synaptic transmission: from ions to network. In Methods in Neural
Modeling: From Ions To Networks (eds. Koch, C. & Segev, I.) Vol. 2
1–25 (MIT Press, Cambridge, 1998).
42. Lancaster, M. A. et al. Cerebral organoids model human brain
development and microcephaly. Nature 501, 373–379 (2013).
43. Kim, J., Koo, B.-K. & Knoblich, J. A. Human organoids: model systems for human biology and medicine. Nat. Rev. Mol. Cell Biol. 21,
571–584 (2020).
44. Osaki, T. et al. Complex activity and short-term plasticity of human
cerebral organoids reciprocally connected with axons. Nat. Commun. 15, 2945 (2024).
45. Estévez-Priego, E. et al. Long-term calcium imaging reveals functional development in hipsc-derived cultures comparable to human
but not rat primary cultures. Stem Cell Rep. 18, 205–219 (2023).
46. Kirihara, T. et al. A human induced pluripotent stem cell-derived
tissue model of a cerebral tract connecting two cortical regions.
Iscience 14, 301–311 (2019).
47. Kawada, J. et al. Generation of a motor nerve organoid with human
stem cell-derived neurons. Stem Cell Rep. 9, 1441–1449 (2017).
48. Bassett, D. S. & Bullmore, E. T. Small-world brain networks revisited.
Neuroscientist 23, 499–516 (2017).
49. Ballini, M. et al. A 1024-channel cmos microelectrode array with
26,400 electrodes for recording and stimulation of electrogenic
cells in vitro. IEEE J. Solid-State Circuits 49, 2705–2719 (2014).
50. Cai, H. et al. Brain organoid reservoir computing for artiﬁcial intelligence. Nat. Electron. 6, 1032–1039 (2023).
51. Goldwag, J. & Wang, G. Dishbrain plays pong and promises more.
Nat. Mach. Intell. 5, 568–569 (2023).
52. Guggenmos, D. J. et al. Restoration of function after brain damage
using a neural prosthesis. Proc. Natl Acad. Sci. USA 110,
21177–21182 (2013).
53. Averna, A. et al. Differential effects of open-and closed-loop intracortical microstimulation on ﬁring patterns of neurons in distant
cortical areas. Cereb. Cortex 30, 2879–2896 (2020).
54. Cottone, C. et al. A new, high-efﬁcacy, noninvasive transcranial
electric stimulation tuned to local neurodynamics. J. Neurosci. 38,
586–594 (2018).
55. Brette, R. What is the most realistic single-compartment model of
spike initiation? PLoS Comput. Biol. 11, e1004114 (2015).

Nature Communications | (2024)15:5142

https://doi.org/10.1038/s41467-024-48905-x
56. Hines, M. Efﬁcient computation of branched nerve equations. Int. J.
Bio-Med. Comput. 15, 69–76 (1984).
57. Chiappalone, M. et al. Burst detection algorithms for the analysis of
spatio-temporal patterns in cortical networks of neurons. Neurocomputing 65, 653–662 (2005).
58. Carè, M. et al. The impact of closed-loop intracortical stimulation on
neural activity in brain-injured, anesthetized animals. Bioelectron.
Med. 8, 4 (2022).
59. Lieb, F., Stark, H.-G. & Thielemann, C. A stationary wavelet
transform and a time-frequency based spike detection algorithm for extracellular recorded data. J. Neural Eng. 14,
036013 (2017).
60. Toosi, R., Akhaee, M. A. & Dehaqani, M.-R. A. An automatic spike
sorting algorithm based on adaptive spike detection and a mixture
of skew-t distributions. Sci. Rep. 11, 13925 (2021).

Acknowledgements
This work was supported by IdEx International of University of
Bordeaux (RB) and the JSPS Core-to-Core Program (RB, JC, TD;
grant number JPJSCCA20190006). In addition, this work was supported by the French National Research Agency: Project-ANR-20CE45-0005 (TL), Project-ANR-23-CE45-0001 (TL), Project-ANR-20SFRI-0001 (TL) and by CNRS INSIS through the “Biomeg” project
(RB, JC, TL). This work was also supported by the Institute for AI and
Beyond (TD, YI), JST SPRING (TD; JPMJSP2108), ANRI fellowship
(TD), AMED (YI; JP20gm1410001) and Kakenhi (YI; 20K20643). Further support for this work comes from Università Italo-Francese/
Université Franco-Italienne PHC Galileo as part of the “NEUROHYSTIM” project (RB, JC, TL, MCa, Mch). The work related to the
animal experiments and their analyses were carried out within the
framework of the project “RAISE - Robotics and AI for Socioeconomic Empowerment” and has been supported by European
Union - NextGenerationEU (GDV, MCa, Mch). We acknowledge
Landry Bailly for the synaptic connection heatmap of the organoid
emulation, Mattia Di Florio and Federico Barban for the setting-up
of the SNN-based in vivo stimulation. We also acknowledge Hu
Huaruo and Atsuhiro Nabeta for their advice and assistance on the
data acquisition from Maxwell system.

Author contributions
RB designed both the software and hardware part of the system,
developed the Python scripts, participated in the biohybrid experiments, analyzed the results and wrote the manuscript. JC participated in the development of the hardware design of the synapses,
Wi-Fi communication on ESP32. TD cultivated the organoids, performed the analysis of the data from the HD-MEA system and captured the images of the cultures. RB, JC and TD conducted the
closed-loop experiment with HD-MEA. FK contributed to previous
work that laid the foundation for this research, and provided critical
advice and guidance. GDV designed automated scripts for parameter sweeps of the RFA network conﬁgurations, developed analysis
scripts, analyzed results, and conducted emulations under supervision of MCh and MCa. MCa prepared, executed and performed the
acquisitions and the analysis of the RFA. TL supervised and participated in the design of the applications and biohybrid experiments.
TL, YI, PB and MCh supervised and advised on the biohybrid experiments and biological modeling. TL, YI, PB and MCh joined the discussion and corrected the draft manuscript. All authors discussed
and revised the ﬁnal manuscript.

Competing interests
The authors declare no competing interests.

13

## PDF page 14

Article

Additional information
Supplementary information The online version contains
supplementary material available at
https://doi.org/10.1038/s41467-024-48905-x.
Correspondence and requests for materials should be addressed to
Timothée Levi.
Peer review information Nature Communications thanks the anonymous reviewers for their contribution to the peer review of this work. A
peer review ﬁle is available.
Reprints and permissions information is available at
http://www.nature.com/reprints

https://doi.org/10.1038/s41467-024-48905-x
Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as
long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons licence, and indicate if
changes were made. The images or other third party material in this
article are included in the article’s Creative Commons licence, unless
indicated otherwise in a credit line to the material. If material is not
included in the article’s Creative Commons licence and your intended
use is not permitted by statutory regulation or exceeds the permitted
use, you will need to obtain permission directly from the copyright
holder. To view a copy of this licence, visit http://creativecommons.org/
licenses/by/4.0/.
© The Author(s) 2024

Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional afﬁliations.

1

IMS, CNRS UMR5218, Bordeaux INP, University of Bordeaux, Talence, France. 2Institute of Industrial Science, The University of Tokyo, Tokyo, Japan. 3LIMMS,
CNRS-Institute of Industrial Science, UMI 2820, The University of Tokyo, Tokyo, Japan. 4Department of Chemistry and Biotechnology, Graduate School of
Engineering, The University of Tokyo, Tokyo, Japan. 5Institute for AI and Beyond, The University of Tokyo, Tokyo, Japan. 6DIBRIS, University of Genova,
Genova, Italy. 7IRCCS Ospedale Policlinico San Martino, Genova, Italy. 8Rehab Technologies, Istituto Italiano di Tecnologia, Genova, Italy. 9INCIA, UMR5287,
CNRS, University of Bordeaux, Bordeaux, France.
e-mail: timothee.levi@u-bordeaux.fr

Nature Communications | (2024)15:5142

14
