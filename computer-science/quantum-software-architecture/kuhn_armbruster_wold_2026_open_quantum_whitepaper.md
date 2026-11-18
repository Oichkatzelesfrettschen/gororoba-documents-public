Source: https://zenodo.org/records/22103261
PDF sha256: bb03da991063359c5435994ac6598852c45c90adbc52adb739e32e081c0d1f69
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of kuhn_armbruster_wold_2026_open_quantum_whitepaper.pdf

Transcription of `kuhn_armbruster_wold_2026_open_quantum_whitepaper.pdf` in this directory, 8 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-8 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Open Quantum: An Open Infrastructure Layer for Quantum
Computing
Ryan Kuhn

Omar Armbruster

Bob Wold

Quantum Rings Inc.
Boulder, CO, USA
ryan.kuhn@quantumrings.com

Quantum Rings Inc.
Boulder, CO, USA
omar.armbruster@quantumrings.com

Quantum Rings Inc.
Boulder, CO, USA
bob.wold@quantumrings.com

August 2026
DOI: 10.5281/zenodo.22103261

Abstract
Open Quantum is a platform that provides researchers and developers with access to quantum processing units (QPUs) from multiple hardware providers through a unified API and native integrations
with widely used quantum programming frameworks, including Qiskit and PennyLane. The platform
is operated by Quantum Rings—a team best known for their large-scale quantum circuit simulation—in
partnership with qBitTensor Labs, which operates a decentralized quantum-compute network on the
Bittensor protocol. Open Quantum offers two execution tiers: Public Compute, in which circuits are
routed through the decentralized network, with free or subsidized access in exchange for the user’s consent to the retention and study of execution data; and Private Compute, in which circuits execute on
directly managed infrastructure and are deleted after execution. This paper describes the platform’s
architecture and execution model; the identity and verification mechanisms that connect a permissionless incentive network to metered quantum hardware; and the consented, cross-vendor corpus of real
quantum workloads that the public tier accumulates, from which the platform will publish aggregate
analyses beginning at the close of Summer 2026.

1

Introduction

Quantum Rings is best known for their work on
large-scale quantum simulation, which they have
pursued since 2023 through the development of the
Quantum Rings SDK: users can execute hundreds
of logical qubits and millions of gate operations
with high fidelity, all on consumer-grade classical
hardware [1]. They first demonstrated their expertise in quantum simulation by simulating Google’s
2019 quantum supremacy circuits on a classical
computer with 32 GB of memory, achieving a
record-breaking linear cross-entropy benchmarking (XEB) score of 0.622 [2]. They later revisited
this experiment, running the same simulation on a
single NVIDIA A100 GPU in 1:15:36, representing a 6.95 × 107 speedup compared to Google’s

Quantum computing promises solutions to problems in optimization, cryptography, and simulation that are intractable for classical computers.
However, the high cost and limited availability of
quantum processing units (QPUs), as well as the
costly classical hardware requirements needed to
run large-scale quantum simulators, have restricted
access to a select few institutions and corporations. Accessing QPUs and simulators from a new
provider also tends to require migrating algorithms
and learning new systems and frameworks. These
limitations have inhibited the growth of the quantum industry as a whole.
1

## PDF page 2

original classical prediction [3].
Open Quantum, launched in late 2025, extends this work from simulation to physical hardware. The platform provides access to QPUs from
providers including IonQ, Rigetti, IQM, and AQT
through a single API [4], with native plugins for
the Qiskit [6] and PennyLane [7] frameworks and
an integration with the qBraid development environment, so that existing programs target physical
hardware with minimal modification.
The platform’s Public Compute tier is offered
in partnership with qBitTensor Labs [8], operator of the Quantum Compute subnet (SN48) on
the blockchain-based Bittensor network. The subnet’s incentive mechanism allows participating capacity providers to price circuit execution below
the list price of equivalent direct access, which
is what enables the platform’s subsidized public
tier. This paper is a revised edition of the launch
white paper [5], updated to describe the platform
as deployed. It covers the platform’s execution
model and architecture (Sections 2 and 3), the
Open Quantum EDGE appliance for QPU operators (Section 4), the integration with the decentralized network (Section 5), the cross-vendor corpus
of quantum workloads that the public tier accumulates (Section 6), and the platform’s broader aims
(Section 7).

2

IonQ

Qiskit
PennyLane

Open Quantum
SDK

qBraid SDK

Open Quantum
cloud

Rigetti
IQM
AQT
Operator QPUs
via EDGE

Figure 1: Many frameworks, many QPUs, one
API. Programs written in Qiskit, PennyLane, or the
qBraid environment reach any supported QPU—from
providers including IonQ, Rigetti, IQM, and AQT, or
operator systems connected through Open Quantum
EDGE—with no vendor-specific integration.

Target audiences span traditional users, such as
quantum researchers, academics, software developers, and enterprises, but also extend to students,
enthusiasts, and innovators from adjacent fields,
making quantum experimentation accessible without prohibitive costs.

2.1

Execution tiers

Every job is submitted under one of two execution
plans.
Public Compute: Circuits are routed through
the decentralized network operated by qBitTensor
Labs. Access is free or subsidized: the incentive
mechanism of Section 5 sustains pricing below the
list price of equivalent direct access, and renewable no-cost credits allow a researcher or student to
run circuits on physical QPUs without payment. In
exchange, users consent to the retention and study
of circuit and job data, which is used to improve
calibration, scheduling, and platform performance
and accumulates as the corpus described in Section 6; analyses from it are published only in aggregate, anonymized form. The platform’s terms
require attribution to the platform in publications
resulting from work on the public tier; this paper
is the canonical reference for that purpose.
Private Compute: Circuits execute on directly
managed infrastructure operated through trusted,
identified execution partners. Circuits and results
are excluded from aggregate analysis, submitted
circuits are deleted after execution, and jobs queue

The Open Quantum Platform

Open Quantum enables users to run quantum circuits on QPUs through a single API, eliminating the complexities of multi-vendor integrations:
one account, one credential scheme, and one job
model across all supported backends. Figure 1
summarizes this model—programs written in any
supported framework reach any supported QPU
through the same interface.

2

## PDF page 3

on dedicated capacity. This tier is intended for proprietary workloads and production use.
Access is metered through prepaid credits of
two kinds: Spark credits, granted at no cost on a
renewing schedule and valid on Public Compute
only, and Full credits, which are purchased and apply to either tier.

2.2

paid submissions are guarded by explicit spend
confirmation and a per-job cost cap.
Delegated authorization for third parties: External applications integrate through the same
identity layer as the platform’s own clients. Open
Quantum exposes a standard OpenID Connect
authorization-code flow (with PKCE), through
which a user authorizes a third-party application—
the qBraid environment, for example—to submit
jobs on the user’s behalf without ever sharing credentials with it. Access is consent-scoped and revocable: an application receives only the scopes
granted at consent (job submission, or additionally
account management for provisioning a new user’s
organization), access tokens are short-lived, refresh tokens rotate on use, and a user may revoke an
individual application’s authorization at any time
without affecting their other sessions. This allows
development environments, notebooks, and workflow tools to offer Open Quantum execution as a
native capability while the platform retains a single point of identity, consent, and audit.

Interfaces

Users interact with the platform through a web portal or programmatically:
• Core SDK: a pip-installable Python package
(openquantum-sdk) providing job preparation,
submission, status polling, result retrieval, and
per-job calibration-snapshot download. Circuits are accepted as OpenQASM 2.0 or 3.0,
detected automatically.

• Qiskit plugin:
implements the Qiskit
BackendV2 interface with SamplerV2 and
EstimatorV2 primitives, and publishes perbackend transpilation targets (native gate sets,
connectivity, timing) so that Qiskit’s transpiler
compiles directly to each device. Code written 2.3 Hardware backends
against the standard primitive interfaces runs
The platform currently connects to trapped-ion
without modification.
systems from IonQ and AQT and superconduct• PennyLane plugin:
registers a native ing systems from Rigetti and IQM; the available
openquantum.device usable with the standard QPUs are listed in Table 1, with the short codes
qml.device interface, including parameter- used to address them from the SDK and frameshift differentiation for variational workloads work plugins. Each system links to its detail page,
and support for counts, expectation-value, vari- where full specifications are maintained. For every backend, the platform publishes the device’s
ance, probability, and sample measurements.
constraint metadata and its most recent calibra• qBraid integration: jobs may be submitted di- tion data, which users can download through the
rectly from the qBraid environment, which ad- portal or the SDK; completed jobs may additionditionally provides cross-framework transpila- ally carry a calibration snapshot taken at execution
tion from other circuit representations.
time. Backend availability evolves as providers
• MCP server: a local Model Context Proto- and systems are added.
col [9] server (openquantum-mcp), built on the
core SDK, exposes the platform to AI agents
and agentic development environments. An
agent can discover backends and credit balances, prepare a job and inspect its credit quote
before any spend, submit circuits, poll for completion, and retrieve results and calibration data.
Credentials remain on the user’s machine, and

Table 1: QPU backends available on the platform at the
time of writing, with their platform short codes. Each
system links to its detail page at www.openquantum.
com/providers.

3

## PDF page 4

System
IonQ Forte-1
IonQ Forte Enterprise
Rigetti Cepheus-1
IQM Emerald
IQM Garnet
AQT IBEX Q1

3

ity they own or procure, serving the public
tier. Directly managed agents, operated through
trusted, identified execution partners, serve the
private tier. Operators can also connect systems
they run themselves through Open Quantum
EDGE (Section 4). In every case, new hardware is onboarded by adding backend metadata
and deploying an agent, without change to the
platform core.

Qubits Backend short code
36
36
108
54
20
12

ionq:forte-1
ionq:forte-ent
rigetti:cepheus-1-108q
iqm:emerald
iqm:garnet
aqt:ibex-q1

Platform Architecture

The platform separates user-facing scheduling
from hardware-facing execution, with asynchronous queues between the two, so that clients,
platform services, and execution sites scale independently.

• Isolation: Private Compute jobs are dispatched
only to directly managed execution sites; circuit
data is handled only by the platform and its vetted execution partners, and results return only
through the platform’s storage path.

• Submission and preparation: A client submits a circuit through the portal or an SDK. The
circuit is stored in object storage and a preparation task is queued. A background worker
validates the program, converts between OpenQASM versions (2.0 and 3.0) where a backend requires it, checks the circuit against the
target backend’s advertised constraints (qubit
count, native operations, supported features),
and computes a price quote for each available
execution plan and queue priority. The user—
or the SDK, automatically—selects a plan, at
which point credits are reserved and the job enters the submission queue.

4

Open Quantum EDGE

A quantum computer is rarely a single system.
In practice it is a collection of loosely coupled
subsystems—control electronics and pulse-level
software, calibration and error-suppression tooling, cryogenic and environmental monitoring—
each with its own interface, and none designed
to be exposed to outside users. Open Quantum
EDGE is an appliance that installs inside the operator’s laboratory or data center and integrates with
these components directly. To the outside world, it
represents the instrument as a single, clean system
on Open Quantum (Figure 2): jobs arrive as OpenQASM against the device’s published constraints,
execute through the local control stack, and return
results and calibration snapshots through the platform’s standard job model. Like every execution
agent (Section 3), the appliance connects outward
only—no inbound connections into the facility are
required—and the operator retains full control of
the instrument.
The appliance also carries the operational side
of running a quantum system. It surfaces detailed
telemetry from the dilution refrigerator and from
the qubit controller through the platform, giving
the operator live visibility into the instrument’s
state. Operators can schedule reserved windows,
during which only designated organizations may
access the system, and recurring maintenance windows, during which the backend is withdrawn from
scheduling entirely.

• Execution: Execution follows a pull model.
Authenticated execution agents poll the platform’s execution service for work destined for
their backend; the platform never opens connections into a provider’s network. A claimed
execution is delivered as a compact descriptor
containing a presigned reference to the circuit
in object storage; the agent retrieves the circuit,
executes it on the target device, and uploads results (and, where supported, a calibration snapshot taken at execution time) back to object storage. Failed executions are retried a bounded
number of times before the job is marked failed
and credits are refunded.
• Execution sites: Two kinds of agents execute jobs. Miners on the SN48 network (Section 5) operate agents backed by QPU capac4

## PDF page 5

5

An EDGE-connected system may be listed privately or publicly. Listed privately, the device
is visible only to the operator’s own organizations, giving in-house researchers the platform’s
standard interfaces—Qiskit, PennyLane, the Open
Quantum SDK—over their own hardware, alongside the other backends they already use. Listed
publicly, spare capacity is offered to the platform’s
users at a price the operator sets. Listing visibility is distinct from the execution tiers of Section 2: a listing governs who can discover and submit to the device, while the execution plan chosen
per job governs its pricing and data handling, so
jobs on a publicly listed system may still run under Private Compute plans. Sold capacity creates
a stream of income for the operator, which accumulates as platform credits that the operator’s researchers can spend on the other systems available
through Open Quantum, or which can be remitted
as revenue. Idle capacity thus converts into either
reach—time on other modalities and devices—or
income, while local users retain priority on their
own machine.

Decentralized Compute in Partnership with qBitTensor Labs

The public tier’s pricing derives from the platform’s integration with the Bittensor ecosystem,
a decentralized network in which independent
subnets coordinate incentives with the TAO token [10]. Open Quantum’s Public Compute
is powered by the Quantum Compute subnet
(SN48), operated by qBitTensor Labs (https://
www.qbittensorlabs.com) [8], a company building quantum solutions within the Bittensor ecosystem. SN48 creates a two-sided market: demand
arrives as circuits submitted through Open Quantum’s API, and supply is provided by miners operating QPU capacity. Public jobs pass from the
platform to qBitTensor Labs, whose validators assign each job to a suitable miner; the miner coordinates execution with the hardware provider,
and results return along the same path (Figure 3).
Because miners additionally earn TAO emissions
in proportion to their assessed contribution, they
can price execution below the list price of equivalent direct access; this subsidy is what sustains the
public tier’s below-list pricing and no-cost credit
grants.

operator facility (lab / data center)

Control electronics

5.1
Calibration &
error suppression

Identity and authorization

Open Quantum
EDGE

The subnet’s participants are pseudonymous by design, while metered quantum hardware requires
Cryogenics &
accountable access. The integration bridges the
telemetry
two with a token exchange: a miner or validaone backend
tor signs a request with its Bittensor hotkey; the
platform verifies the signature, checks that the key
Open Quantum cloud
is currently registered on the subnet by consulting the metagraph, distinguishes validators by their
on-chain permit, and only then issues a scoped,
Private listing
Public marketplace short-lived OAuth2 token for the platform’s execuoperator’s organizations
credits or revenue
tion APIs. Requests carry timestamps that expire
within minutes.
Figure 2: Open Quantum EDGE. The appliance installs in the operator’s facility, integrates with the components of the QPU system, and represents the instrument as a single backend through Open Quantum. The
operator lists the system privately, for their own organizations, or publicly on the marketplace, where execution accrues income as platform credits or remitted
revenue.

5.2

Execution integrity

Two mechanisms tie the permissionless supply side
to genuine quantum execution.
Onboarding verification: Capacity admitted to
the network is vetted before it serves jobs: each
5

## PDF page 6

5.3

backend must be shown to be backed by a physical QPU from an identified hardware provider,
with its device metadata (modality, qubit count,
native operations, calibration characteristics) validated against the provider’s published specifications.
Closed-loop job verification: Every job carries a
verifiable execution trail. Because executions terminate at identified providers, the platform reconciles each reported execution against the provider’s
job records, confirming that the circuit was in fact
submitted to, and executed on, the reported device.
A job is complete only when this loop closes; discrepancies are surfaced before results are trusted or
capacity is credited.
The subnet’s incentive layer complements
these checks: validators express their assessment
of each miner’s delivered capacity as on-chain
weights, which determine the miner’s share of
TAO emissions, so sustained poor performance reduces a miner’s reward without requiring any centrally administered penalty.

qBitTensor Labs also operates Enigma (SN63),
a challenge platform that accumulates prize
pools for adversarial problems in the same
problem domain—including staged RSA-factoring
milestones—with solutions published openly once
claimed. Enigma is complementary to SN48: one
funds standing quantum capacity, the other funds
targeted attacks on the assumptions that capacity
and its verification rest on.

6

results

qBitTensor Labs
SN48
jobs
s

ht
weig

Bittensor chain

results

Validators
jobs

weights → emissions
TAO
em

ission

s

job-record
reconciliation

results

Miners

jobs

A Public Corpus of Quantum
Workloads

The public tier trades free and subsidized execution for consent to study the resulting data.
That exchange accumulates a resource the field
has lacked: a consented, cross-vendor record of
real quantum workloads. For each public job the
platform retains the submitted circuit itself, together with execution metadata (target backend,
shot count, timing through the pipeline) and, where
supported, a calibration snapshot of the device
taken at execution time. Private-tier jobs are excluded entirely. Commercially sensitive work is
the work most likely to run private, so the corpus over-represents exploratory, educational, and
benchmarking use relative to the network as a
whole, and analyses drawn from it must be read
with that selection in mind.
Most accounts of what quantum computing is
used for rest on surveys and self-declared intent.
A workload corpus permits measurement instead:
the composition of submitted work by algorithm
family, recognized structurally from the circuits
rather than from a form field; the distribution of
circuit width and depth over time; how demand distributes across the devices, modalities, and price
points of a heterogeneous fleet; and how queueing
and execution time behave across systems.
The same corpus is a natural substrate for machine learning. Circuits labeled by structural family form training data for circuit classification;
circuit–result pairs from devices with attached calibration snapshots support learned noise models
and error-mitigation strategies; and submission

Open Quantum platform
public jobs

Related subnet work

results

Hardware providers
QPUs

Figure 3: Execution and incentives on SN48. Public
jobs pass from the platform to qBitTensor Labs and on
through validators to miners, which execute them on
provider QPUs; results return along the same path, and
the platform reconciles each execution against the hardware provider’s job records before the job closes. Independently, validators publish weights on-chain, which
set each miner’s share of TAO emissions.

6

## PDF page 7

traces from the platform’s MCP interface (Section 2) capture some of the earliest examples of
AI agents preparing and submitting quantum workloads without a human in the loop. Because the
corpus spans vendors and modalities, datasets derived from it carry a heterogeneity that no singlevendor source can offer.
The data gathered to date has reached critical
mass, and beginning at the close of Summer 2026
the platform will publish seasonal aggregate analyses of network traffic as Open Quantum Insights:
workload composition, circuit-shape trends, and
system-level performance, reported in anonymized
aggregate. Individual circuits, results, and identities are never published in these reports.

interfaces in front, a provider-abstracted execution
pipeline in the middle, and a verified, incentivealigned supply network behind it. That composition also yields, as a byproduct of its consentbased public tier, a growing cross-vendor record of
how quantum hardware is actually used. Publishing what that record shows, beginning with the first
seasonal analyses at the close of Summer 2026,
is part of the contribution the platform intends to
make.

Acknowledgments

The authors extend gratitude to the qBitTensor
Labs team and Bittensor community for their
pioneering work in decentralized quantum
computing. Special thanks to partners, including
7 Goals and Aims
Rigetti, IonQ, IQM, AQT, qBraid, AWS, Qblox,
Open Quantum’s aim is to broaden access to quan- Q-CTRL, Maybell Quantum, and Elevate
tum computing:
Quantum, for their resources and collaboration.
• Access: Lower the cost and integration barriers
to running programs on physical quantum hardware, for institutions and individuals alike.

References
[1] Quantum Rings Inc., “Quantum Rings SDK:
Large Scale Quantum Simulation,”
www.quantumrings.com, accessed August
2026.

• Sustainability: Through Bittensor’s incentive
mechanisms, reward contributed quantum capacity so that below-list public-tier pricing is
sustained by the network’s own economics
rather than by indefinite subsidy or centralized
funding.

[2] Venkateswaran Kasirajan, Torey Battelle,
and Bob Wold, Empowering Large Scale
Quantum Circuit Development: Effective
Simulation of Sycamore Circuits,
arXiv:2411.12131 [quant-ph] (2024).
https://arxiv.org/abs/2411.12131

• Measurement: Publish aggregate analyses
from the public corpus (Section 6) so that the
field’s actual usage, and not just its forecasts, is
visible to researchers, hardware providers, and
the industry at large.

[3] Bob Wold and Venkateswaran Kasirajan,
Revisiting Quantum Supremacy: Simulating
Sycamore-Class Circuits Using Hybrid
CPU/GPU HPC Workloads,
arXiv:2512.07311 [quant-ph] (2025).
https://arxiv.org/abs/2512.07311

The long-term vision is quantum computing as accessible as cloud computing is today.

8

Conclusion

[4] Open Quantum Platform, “Quantum
Computing for All,”
www.openquantum.com, accessed August
2026.

Open Quantum combines low-cost, uniform access
to quantum hardware with a decentralized incentive layer that sustains that access economically.
The platform’s contribution is less any single component than the composition: standard framework
7

## PDF page 8

[5] Bob Wold, Omar Armbruster, and Ryan
Kuhn, Open Quantum: Democratizing
Access to Quantum Computing Resources,
Open Quantum launch white paper,
November 2025.
https://www.openquantum.com/
whitepaper.2025-11.pdf

[8] qBitTensor Labs, “Quantum Computing
Subnets on TAO,”
https://www.qbittensorlabs.com,
accessed August 2026.
[9] Anthropic, “Model Context Protocol,”
https://modelcontextprotocol.io,
accessed August 2026.

[6] Ali Javadi-Abhari et al., Quantum
computing with Qiskit, arXiv:2405.08810
[quant-ph] (2024).

[10] Y. Rao, “Bittensor: A Peer-to-Peer
Intelligence Market,” Bittensor White Paper,
[Online]. Available:
https://bittensor.com/whitepaper.
Accessed: August 2026.

[7] Ville Bergholm et al., PennyLane:
Automatic differentiation of hybrid
quantum-classical computations,
arXiv:1811.04968 [quant-ph] (2018).

8
