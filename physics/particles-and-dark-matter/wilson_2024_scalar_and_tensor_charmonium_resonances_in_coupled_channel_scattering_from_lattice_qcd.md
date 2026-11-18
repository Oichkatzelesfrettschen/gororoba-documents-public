Source: https://doi.org/10.1103/PhysRevLett.132.241901
PDF sha256: 46bb9ba6387a9290fd8f9a31266dc31c2727f9e21bf8867b68ff3c302f7b23e2
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of wilson_2024_scalar_and_tensor_charmonium_resonances_in_coupled_channel_scattering_from_lattice_qcd.pdf

Transcription of `wilson_2024_scalar_and_tensor_charmonium_resonances_in_coupled_channel_scattering_from_lattice_qcd.pdf` in this directory, 7 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-7 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
Editors' Suggestion

Scalar and Tensor Charmonium Resonances in Coupled-Channel
Scattering from Lattice QCD
David J. Wilson ,1,* Christopher E. Thomas ,1,† Jozef J. Dudek ,2,3,‡ and Robert G. Edwards

2,§

(for the Hadron Spectrum Collaboration)
1

DAMTP, University of Cambridge, Centre for Mathematical Sciences, Wilberforce Road, Cambridge CB3 0WA, United Kingdom
2
Thomas Jefferson National Accelerator Facility, 12000 Jefferson Avenue, Newport News, Virginia 23606, USA
3
Department of Physics, College of William and Mary, Williamsburg, Virginia 23187, USA
(Received 23 October 2023; revised 15 January 2024; accepted 29 March 2024; published 10 June 2024)
We determine J PC ¼ 0þþ and 2þþ hadron-hadron scattering amplitudes in the charmonium energy
region up to 4100 MeV using lattice QCD, a first-principles approach to QCD. Working at mπ ≈ 391 MeV,
more than 200 finite-volume energy levels are computed and these are used in extensions of the Lüscher
formalism to determine infinite-volume coupled-channel scattering amplitudes. We find that this energy
region contains a single χ c0 and a single χ c2 resonance. Both are found as pole singularities on the closest
unphysical Riemann sheet, just below 4000 MeV with widths around 70 MeV. The largest couplings are to
kinematically closed D D̄ channels in S-wave, and couplings to several decay channels consisting of pairs
of open-charm mesons are found to be large and significant in both cases. Above the ground state χ c0 , no
other scalar bound states or near-DD̄ threshold resonances are found, in contrast to several theoretical and
experimental studies.
DOI: 10.1103/PhysRevLett.132.241901

Introduction.—The experimental mapping of the spectrum of excited hadrons containing a charm-anticharm pair
has seen rapid progress in recent years. Driven initially by
the discovery of the Xð3872Þ [1], more novel observations
quickly followed, including states with an apparent fourquark nature, such as the Zc ð3900Þ [2,3]. Work to decipher
this new hadron spectroscopy, going beyond the simple cc̄
quark model, is underway [4–8]. Within the standard model
of particle physics lies quantum chromodynamics (QCD),
the theory of interacting quarks and gluons, which
describes hadrons and their interactions. While the theory
is well defined, it remains challenging to perform calculations of its spectrum owing to its strongly coupled nature.
Charm quarks are heavy enough that relativistic effects
are typically subleading, and models built using potentials
have proven successful in describing the low-lying spectrum [9–14]. These approaches work well for states below
DD̄ threshold whose lifetimes are relatively long, with
charm-anticharm annihilation and radiative transitions
being the dominant modes of decay. However, above this
point states can decay more rapidly to systems of open-

Published by the American Physical Society under the terms of
the Creative Commons Attribution 4.0 International license.
Further distribution of this work must maintain attribution to
the author(s) and the published article’s title, journal citation,
and DOI. Funded by SCOAP3.

0031-9007=24=132(24)=241901(7)

charm mesons, and the physics of coupling to decay modes,
where we treat excited states as resonances, becomes
important.
This Letter aims to address a key weakness in our present
understanding: knowledge of resonance decays from firstprinciples in QCD. We compute using lattice QCD to
determine resonance masses, widths, and decay modes. We
begin by considering what might naïvely be expected to be
relatively simple systems: isoscalar scalar and tensor
resonances in the approximation where charm-anticharm
annihilation is forbidden. This is well defined theoretically,
and well justified empirically given the modest hadronic
widths observed for states below DD̄ threshold. A summary of the general approach, which takes advantage of the
finite spatial volume of the lattice to determine scattering
amplitudes in which resonances appear, is given in a recent
review [15]. The discrete spectra extracted from correlation
functions computed using lattice QCD can be translated
into infinite-volume coupled-channel scattering amplitudes
using the Lüscher formalism [16] and extensions. The
scattering amplitudes so obtained contain resonances as
pole singularities in much the same way as experimental
analyses. The pole positions yield the masses and widths,
and the pole residues factorize into the channel couplings,
enabling partial widths to be estimated.
In this Letter, we present results for resonances found in
JPC ¼ 0þþ and 2þþ . In an accompanying longer article
[17], we give more details of our approach, and provide

241901-1

Published by the American Physical Society

## PDF page 2

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
other amplitudes extracted in this work including
JPC ¼ 3þþ , which is found to contain a χ c3 resonance,
and negative parity JPC ¼ f1; 2; 3g−þ waves which lack
strong scattering, although 2−þ contains a near-threshold
bound state. The closest previous work considering some of
these channels in Lattice QCD is Ref. [18], and a
comparison with the calculation reported on here can be
found in the longer article, Ref. [17]. The methods used
here are applicable to the JPC ¼ 1þþ χ c1 channel. Because
of the additional complications of the presence of threebody ηc ππ energy levels low in the spectrum, and the
mixing of S and D-waves, we reserve this for future study.
Computing finite-volume spectra.—We perform calculations using lattices with two degenerate dynamical light
quark flavors and a heavier dynamical strange quark
[19,20], with a light quark mass value such that
mπ ≈ 391 MeV. The valence charm quarks have the same
action as the light and strange quarks and are tuned to
approximately reproduce the physical ηc mass [21]. Three
volumes are employed corresponding to L=as ¼ f16; 20;
24g, where L is the spatial extent and as ≈ 0.12 fm is the
spatial lattice spacing. Anisotropic lattices with anisotropy
ξ ¼ as =at ≈ 3.5 are used to obtain a finer energy resolution, where at is the temporal lattice spacing. In the
computation of two-point correlation functions, all relevant
Wick contractions, including those featuring light or
strange quark annihilation, are performed efficiently using
distillation [22].
No lattice QCD study to date has considered all hadronhadron channels present in this energy region, even in the
simplifying limit where charm-anticharm annihilation is
forbidden. In this work, we compute the complete discrete
energy spectrum up to around the ψϕ threshold by using a
large number of interpolating operators with fermionbilinear (cc̄-like) and meson-meson-like structures [23].
In particular, we construct operators resembling every
relevant hadron-hadron pair with the correct quantum
numbers.
While our aim is to determine the J PC ¼ f0; 2gþþ
amplitudes, the reduced symmetry of the finite cubic lattice
volume means that scattering in multiple JP partial waves
contributes to the same finite-volume spectra, obtained in
the irreducible representations (irreps) of the cubic group
[24,25]. Parity is a good quantum number for systems
overall at rest, but it is not when the system has net
momentum. The finite-volume of the lattice imposes
quantization of momentum, ⃗p ¼ ð2π=LÞði; j; kÞ ¼ ½ijk
where i, j, k are integers, and we will compute spectra
for several values of total scattering system momentum.
Relevant hadron-hadron scattering combinations with
JPC ¼ f0; 2; 3gþþ are shown in Table I, with partial-waves
labeled by spectroscopic notation. (We do not aim to
determine any three-hadron amplitudes, but when computing the finite-volume spectra we include operators with
ηc σ-like and χ c0 σ-like structures. The corresponding

TABLE I. Hadron-hadron 2Sþ1 lJ total spin (S), orbital angular
momentum (l), and total angular momentum combinations (J)
present for J PC ¼ f0; 2; 3gþþ scattering. Those with square
brackets indicate that the corresponding operator constructions
were included, but that the scattering channel was found to be
decoupled or otherwise not relevant at these energies.
0þþ
2þþ
3þþ

ηc η; DD̄; ηc η0 ; Ds D̄s ; ψω; D D̄ ; ψϕf1S0 g
ηc η; DD̄; ½ηc η0 ;Ds D̄s f1D2 g; DD̄ ; ½Ds D̄s f3D2 g
ψω; D D̄ ; ψϕf5S2 g
DD̄ ; ψω; Ds D̄s ; ψϕf3D3 g; [ηc σf1F3 g]
ψω; D D̄ ; ½ψϕ; Ds D̄s f5D3 g

energy levels are found to be decoupled from the other
levels. A complete description is given in the companion
article [17].)
In Fig. 1 we present a selection of computed finitevolume spectra for zero overall momentum for irreps
having JPC ¼ 0þþ and 2þþ as lowest partial waves.
Additional spectra with overall nonzero momentum and
with leading JPC ¼ f1; 2; 3g−þ or 3þþ at zero momentum
are presented in Ref. [17]. In each of the three panels in the
figure a level is observed below ηc η threshold with very
little volume dependence, and these levels correspond to
the stable χ c0 ð1PÞ bound state (left), and the stable χ c2 ð1PÞ
bound state (middle, right). From ηc η threshold up to
around 3900 MeV there is a one-to-one correspondence

þ
þ
FIG. 1. Spectra in irreps ΛP ¼ Aþ
1 , E , and T 2 with zero
overall momentum, having leading J PC ¼ 0þþ , 2þþ and 2þþ
partial waves respectively. Points are the computed finite-volume
energies colored according to their dominant operator overlap,
with colors given in the key on the right. Black points have large
overlap with both cc̄-like and DD̄-like operators. Solid curves
indicate noninteracting meson-meson energies and dashed lines
indicate kinematic thresholds. Degenerate noninteracting levels
are indicated by multiple parallel curves, slightly displaced in
energy for visual clarity.

241901-2

## PDF page 3

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
between the computed energies and the levels expected in
the absence of interactions, and energy shifts from these
noninteracting levels are typically small, suggesting only
mild interaction strength. Higher up in energy there appear
to be extra levels, and more significant departures from the
noninteracting spectrum, which may be due to the presence
of one or more resonances. To draw more definite conclusions we must determine infinite-volume scattering
amplitudes, constrained by these spectra.
Scattering amplitudes.—The coupled-channel scattering
t matrix is obtained from finite-volume energies using
Lüscher’s finite-volume quantization condition [16], generalized for hadron-hadron scattering for hadrons with
arbitrary spin [26],
det½1 þ iρðEÞ · tðEÞ · ð1 þ iMðE; LÞÞ ¼ 0;

ð1Þ

where tðEÞ is the scattering t matrix, MðE; LÞ is a matrix
of known functions dependent on the volume and irrep, and
ρ is a diagonal matrix of phase-space factors, ρi ¼ 2ki =E. E
is the center-of-momentum frame energy, and ki the
momentum of each hadron in that frame for hadron-hadron
channel i.
The matrices in Eq. (1) are in the space of relevant
hadron-hadron channels and partial waves, as shown in
Table I. Since many channels contribute, tðEÞ is underconstrained at any given value of E, and it is necessary to
parametrize the energy dependence. We make use of
amplitudes of the form
½t−1 ij ¼ ð2ki Þ−li ½K −1 ij ð2kj Þ−lj þ I ij ;

ð2Þ

where K ij are the elements of a symmetric matrix that is
real for real s ¼ E2 . S-matrix (s-channel) unitarity mandates that ImI ij ¼ −ρi , while a real part can optionally be
generated through a dispersion relation as described in
Appendix B of Ref. [27].
The 0þþ and 2þþ amplitudes are determined using the
constraint provided by 90 and 86 energy levels respectively,
taken from spectra both at rest and for nonzero total
momentum. Additional levels from other irreps are used
to fix the 3þþ and negative parity waves which also
contribute to Eq. (1), leading to constraint from more than
200 levels in total. Finite-volume energy levels corresponding to the low-lying χ c0 ð1PÞ and χ c2 ð1PÞ bound states are
observed below ηc η threshold in Fig. 1, but because they do
not constrain the amplitudes in the physical scattering
region we choose not to include them when determining the
scattering amplitudes.
In J PC ¼ f0; 2; 3gþþ , amplitudes that prove to be
capable of describing the finite-volume spectra are found
to house resonance poles coupled to channels consisting
of pairs of open-charm mesons. Such poles can be
efficiently parametrized by including terms of form K ij ¼
gi gj =ðm2 − sÞ, with parameters m and fgi g, and increased

flexibility in the amplitude comes from adding a low-order
polynomial in s to this pole term. The free parameters in the
amplitudes are determined by comparing the spectrum
predicted by Eq. (1) for a given parametrization to the
lattice QCD spectra, via a χ 2 minimization [27–29].
To reduce bias from selection of a specific choice of form
for K ij, we consider a range of parametrizations, and when
quoting properties of the scattering amplitudes such as pole
positions and couplings, we take an envelope over the
range of values coming from all parametrization choices
that describe the spectra with reasonable χ 2 =N dof .
Representative examples resulting from this procedure
are shown in Fig. 2.
In both scalar and tensor cases, clear narrow peaks are
visible near 4000 MeV, likely indicating resonant behavior.
In the scalar case, the peaks in elastic DD̄ and Ds D̄s appear
at the same location, and both are distorted in their highenergy tail by the opening of the D D̄ channel. In the
tensor case, the elastic DD̄ energy dependence is sculpted
by the D-wave threshold opening only slightly below the
resonance leading to a peaking behavior at a slightly larger
energy than the peak in DD̄. No peak is seen in
tensor Ds D̄s.
Poles and interpretation.—The partial-wave t matrices
we use are analytic functions of s ¼ E2 apart from branch
cuts opening at thresholds, and poles corresponding to
bound states and resonances.
Neither the t matrices we utilize, nor the finite-volume
quantization condition [16,26] explicitly include singularities due to hadron exchange processes in the t and u
channels, such as pion exchange in DD̄ and D D̄ , which
has been highlighted recently for the related T cc ð3875Þþ
[30,31] and NN [32] scattering. Work is underway to
extend the finite-volume formalism [33] to explicitly
account for such physics.
Passing through the cuts from the real energy axis where
scattering occurs, we enter “unphysical” Riemann sheets
on which the resonance poles live. Close to a pole,
tij ∼ ci cj =ðspole − sÞ, where spole ¼ ½m − ði=2ÞΓ2 is the
location of the pole, and ci is the coupling of the pole
to channel i, which can be related to the partial width Γi for
a kinematically open channel. For the amplitudes in the
current study which describe the computed finite-volume
spectra, we find resonance poles on the “proximal sheet”
which has Im ki < 0 for kinematically open channels and
Im ki > 0 for closed channels, and which is closest to
physical scattering. (The amplitudes considered also feature poles on other, more distant, sheets that are not as
relevant for scattering at real energies.)
Investigating 0þþ , a single resonance pole with large
couplings to DD̄, Ds D̄s , and D D̄ is found on the
proximal sheet in every amplitude. Its location is
m ≈ 3995ð14Þ MeV, Γ ≈ 67ð38Þ MeV, and at this energy,
D D̄ is a closed channel, but decays are possible to DD̄
and Ds D̄s with branching fractions of approximately 40%

241901-3

## PDF page 4

PHYSICAL REVIEW LETTERS 132, 241901 (2024)

FIG. 2. Scattering amplitudes (top) for J PC ¼ 0þþ (left) and 2þþ (right). A single representative amplitude is plotted for each J PC as
ρi ρj jtij j2 , which is similar to the scattering cross section. Error bands are determined by sampling the parameter uncertainties determined
from the χ 2 minimum. Small circles on the horizontal axes mark the locations of key hadron-hadron thresholds. Energies used to
constrain the amplitudes (middle, open circles) and resonance poles (bottom) are also shown, with the pole parameters reflecting the full
uncertainty over parametrization variation, as presented in Ref. [17].

and 60% respectively. In most amplitudes which describe
the finite-volume spectra, very small couplings are found to
ψω, although in a few cases a larger value is not ruled out,
with a branching fraction no larger than 40%.
Similarly in JPC ¼ 2þþ , only a single resonance pole
appears on the proximal sheet, with large couplings to open
DD̄, DD̄ (both in D-wave), and closed D D̄ (in S-wave).
The pole has only very small couplings to Ds D̄s , ηc η,
ψω, and ψϕ, and is located at m ≈ 3961ð15Þ MeV,
Γ ≈ 65ð15Þ MeV. Poles and couplings are shown in Fig. 2.
The use of a light quark mass heavier than the physical
value, and expectations of discretization effects, precludes
direct comparison of our results with experiment. (We
discuss discretization effects further in the companion
article [17].) Nevertheless, we expect resonance properties
in the current system to have even milder dependence on
the light quark mass than for lighter hadrons [34–41], so we

can view previous experimental results and theoretical
predictions in the context of our results.
In the energy region below about 4000 MeV, our
calculation results in a state-counting consistent with cc̄
quark models [10,12], in which the lightest scalar and
tensor states are 1P configurations, and the excited states
we have observed would correspond to the 2P radial
excitations. The resonances found in this study favor
decays to open-charm D-meson pairs over closed-charm
final states, supporting the long-standing Okubo–Zweig–
Iizuka (OZI) phenomenology.
The experimental Xð3872Þ observed close to DD̄
threshold has motivated models with attraction between
the open-charm mesons mediated by pion exchange, with
enough strength to provide binding. Heavy-quark spin
symmetry then suggests similar effects may occur in
D D̄ in S-wave [42,43]. The scalar and tensor resonance

241901-4

## PDF page 5

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
poles found in the current calculation do have large
couplings to the kinematically closed S-wave D D̄ channel, but in both cases the attraction is apparently not large
enough to produce an additional state beyond the expectations of cc̄ excitations.
Our results suggest a single 0þþ resonance that might
explain both the χ c0 ð3930Þ [44] and χ c0 ð3960Þ [45] peak
structures seen in DD̄ and Ds D̄s final states, respectively.
Claims for an additional χ c0 state between 3700 and
3860 MeV appear in experiment [46], lattice [18], bound
hadron-molecule models [47], cc̄ þ DD̄ hadron-loop
dressing models [48–52], and reanalyses [53–56] of the
experimental data, although no such state is reported in
recent LHCb data [44,57]. Our calculation shows no
indication of any such additional state.
The single 2þþ resonance found in this calculation
decays to DD̄ and DD̄ , but has at most weak coupling
to Ds D̄s and closed-charm final states. This result is not in
tension with the current experimental situation, where a
χ c2 ð3930Þ has been identified in DD̄ [44,58,59]. The
Xð3915Þ seen in vector-vector ψω scattering [60] could
be attributed to either 0þþ or 2þþ, but our findings indicate
that interactions in this channel are rather weak.
Outlook.—These results at mπ ≈ 391 MeV suggest a
state counting in 0þþ and 2þþ that is not obviously
different from expectations in cc̄ pictures. To reconcile
these findings with works that find additional states at
physical pion masses, distant pole singularities that do not
impact the current analysis would be required to move
rapidly through the complex energy plane as the light quark
mass is reduced. Eliminating this possibility motivates
further calculations at lighter quark masses using the
current techniques. Three-body channels rapidly become
more important with decreasing pion mass. However, it
should be possible to consider S-wave DD̄ scattering at a
reasonable range of light quark masses.
Unifying enhancements observed in different final states
by identifying pole singularities in unitarity-respecting
scattering amplitudes has proven essential, as clearly
observed in Fig. 2 in the DD̄ and DD̄ tensor amplitudes
that have different peak locations and amplitude shapes but
arise due to a common state. Experimental candidate states
appear in production processes rather than scattering, but
such processes can also be described in terms of the
coupled-channel scattering t matrix and are constrained
by unitarity. Future lattice calculations of electroweak
production processes appear to be feasible [61–63].
Further applications of the lattice QCD approach presented in this paper will consider other near-threshold
charmonia, the Xð3872Þ channel being a particularly
interesting prospect.
Reasonable requests for data, such as energy levels and
correlations, can be directed to the authors and will be
considered in accordance with the Hadron Spectrum

Collaboration’s policy on sharing data. The software codes
Chroma [64], QUDA [65,66], QUDA-MG [67], QPhiX [68],
MG_PROTO [69], QOPQDP [70,71], and Redstar [72]
were used. Some software codes used in this project were
developed with support from the U.S. Department of
Energy, Office of Science, Office of Advanced Scientific
Computing Research and Office of Nuclear Physics,
Scientific Discovery through Advanced Computing
(SciDAC) program.
We thank our colleagues within the Hadron Spectrum
Collaboration [73], in particular Raul Briceño, Andrew
Jackura, and Arkaitz Rodas, and also acknowledge useful
discussions with Igor Danilkin, Feng-Kun Guo, Christoph
Hanhart, Sasa Prelovsek, Steve Sharpe, and Adam
Szczepaniak. D. J. W. acknowledges support from a
Royal Society University Research Fellowship. D. J. W.
and C. E. T. acknowledge support from the UK Science and
Technology Facilities Council (STFC), Grant No. ST/
T000694/1. J. J. D. acknowledges support from the U.S.
Department of Energy Contract No. DE-SC0018416 at
William & Mary, and J. J. D. and R. G. E. from Contract
No. DE-AC05-06OR23177, under which Jefferson Science
Associates, LLC, manages and operates Jefferson Lab.
Also acknowledged is support from the Exascale
Computing Project (17-SC-20-SC), a collaborative effort
of the U.S. Department of Energy Office of Science and the
National Nuclear Security Administration. This work used
the Cambridge Service for Data Driven Discovery (CSD3),
part of which is operated by the University of Cambridge
Research Computing Service [74] on behalf of the STFC
DiRAC HPC Facility [75]. The DiRAC component of
CSD3 was funded by BEIS capital funding via STFC
capital Grants No. ST/P002307/1 and No. ST/R002452/1
and STFC operations Grant No. ST/R00689X/1. Other
components were provided by Dell EMC and Intel using
Tier-2 funding from the Engineering and Physical Sciences
Research Council (capital Grant No. EP/P020259/1). This
work also used the earlier DiRAC Data Analytic system at
the University of Cambridge. This equipment was funded
by BIS National E-infrastructure capital Grant No. ST/
K001590/1, STFC capital Grants No. ST/H008861/1 and
No. ST/H00887X/1, and STFC DiRAC Operations Grant
No. ST/K00333X/1. DiRAC is part of the National EInfrastructure. This work also used clusters at Jefferson
Laboratory under the USQCD Initiative and the LQCD
ARRA project. Propagators and gauge configurations used
in this project were generated using DiRAC facilities, at
Jefferson Lab, and on the Wilkes GPU cluster at the
University of Cambridge High Performance Computing
Service, provided by Dell Inc., NVIDIA, and Mellanox,
and partly funded by STFC with industrial sponsorship
from Rolls Royce and Mitsubishi Heavy Industries. Also
used was an award of computer time provided by the U.S.
Department of Energy INCITE program and supported in

241901-5

## PDF page 6

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
part under an the Department of Energy Advanced
Scientific Computing Research program (ASCR)
Leadership Computing Challenge (ALCC) award, and
resources at: the Oak Ridge Leadership Computing
Facility, which is a DOE Office of Science User Facility
supported under Contract No. DE-AC05-00OR22725; the
National Energy Research Scientific Computing Center
(NERSC), a U.S. Department of Energy Office of Science
User Facility located at Lawrence Berkeley National
Laboratory, operated under Contract No. DE-AC0205CH11231; the Texas Advanced Computing Center
(TACC) at The University of Texas at Austin; the
Extreme
Science
and
Engineering
Discovery
Environment (XSEDE), which is supported by National
Science Foundation Grant No. ACI-1548562; and part of
the Blue Waters sustained-petascale computing project,
which is supported by the National Science Foundation
(Grants No. OCI-0725070 and No. ACI-1238993), and the
state of Illinois. Blue Waters is a joint effort of the
University of Illinois at Urbana-Champaign and its
National Center for Supercomputing Applications.

*

d.j.wilson@damtp.cam.ac.uk
c.e.thomas@damtp.cam.ac.uk
‡
dudek@jlab.org
§
edwards@jlab.org
[1] S. K. Choi et al. (Belle Collaboration), Phys. Rev. Lett. 91,
262001 (2003).
[2] M. Ablikim et al. (BESIII Collaboration), Phys. Rev. Lett.
110, 252001 (2013).
[3] Z. Q. Liu et al. (Belle Collaboration), Phys. Rev. Lett. 110,
252002 (2013); 111, 019901(E) (2013).
[4] M. R. Shepherd, J. J. Dudek, and R. E. Mitchell, Nature
(London) 534, 487 (2016).
[5] A. Esposito, A. Pilloni, and A. D. Polosa, Phys. Rep. 668, 1
(2017).
[6] F.-K. Guo, C. Hanhart, U.-G. Meißner, Q. Wang, Q. Zhao,
and B.-S. Zou, Rev. Mod. Phys. 90, 015004 (2018); 94,
029901(E) (2022).
[7] N. Brambilla, S. Eidelman, C. Hanhart, A. Nefediev, C.-P.
Shen, C. E. Thomas, A. Vairo, and C.-Z. Yuan, Phys. Rep.
873, 1 (2020).
[8] M. Albaladejo et al. (JPAC Collaboration), Prog. Part. Nucl.
Phys. 127, 103981 (2022).
[9] E. Eichten, K. Gottfried, T. Kinoshita, J. B. Kogut, K. D.
Lane, and T.-M. Yan, Phys. Rev. Lett. 34, 369 (1975); 36,
1276(E) (1976).
[10] E. Eichten, K. Gottfried, T. Kinoshita, K. D. Lane, and T.-M.
Yan, Phys. Rev. D 17, 3090 (1978); 21, 313(E) (1980).
[11] J. L. Richardson, Phys. Lett. 82B, 272 (1979).
[12] S. Godfrey and N. Isgur, Phys. Rev. D 32, 189 (1985).
[13] G. S. Bali, Phys. Rep. 343, 1 (2001).
[14] N. Brambilla, A. Pineda, J. Soto, and A. Vairo, Nucl. Phys.
566B, 275 (2000).
[15] R. A. Briceno, J. J. Dudek, and R. D. Young, Rev. Mod.
Phys. 90, 025001 (2018).
[16] M. Luscher, Nucl. Phys. B354, 531 (1991).
†

[17] D. J. Wilson, C. E. Thomas, J. J. Dudek, and R. G. Edwards,
companion paper, Phys. Rev. D 109, 114503 (2024).
[18] S. Prelovsek, S. Collins, D. Mohler, M. Padmanath, and S.
Piemonte, J. High Energy Phys. 06 (2021) 035.
[19] R. G. Edwards, B. Joo, and H.-W. Lin, Phys. Rev. D 78,
054501 (2008).
[20] H.-W. Lin et al. (Hadron Spectrum Collaboration), Phys.
Rev. D 79, 034502 (2009).
[21] L. Liu, G. Moir, M. Peardon, S. M. Ryan, C. E. Thomas, P.
Vilaseca, J. J. Dudek, R. G. Edwards, B. Joo, and D. G.
Richards (Hadron Spectrum Collaboration), J. High Energy
Phys. 07 (2012) 126.
[22] M. Peardon, J. Bulava, J. Foley, C. Morningstar, J. Dudek,
R. G. Edwards, B. Joo, H.-W. Lin, D. G. Richards, and K. J.
Juge (Hadron Spectrum Collaboration), Phys. Rev. D 80,
054506 (2009).
[23] J. J. Dudek, R. G. Edwards, and C. E. Thomas, Phys. Rev. D
86, 034031 (2012).
[24] R. C. Johnson, Phys. Lett. 114B, 147 (1982).
[25] D. C. Moore and G. T. Fleming, Phys. Rev. D 73, 014504
(2006); 74, 079905(E) (2006).
[26] R. A. Briceno, Phys. Rev. D 89, 074507 (2014).
[27] D. J. Wilson, J. J. Dudek, R. G. Edwards, and C. E. Thomas,
Phys. Rev. D 91, 054008 (2015).
[28] P. Guo, J. J. Dudek, R. G. Edwards, and A. P. Szczepaniak,
Phys. Rev. D 88, 014501 (2013).
[29] A. J. Woss, D. J. Wilson, and J. J. Dudek (Hadron Spectrum
Collaboration), Phys. Rev. D 101, 114505 (2020).
[30] M. Padmanath and S. Prelovsek, Phys. Rev. Lett. 129,
032002 (2022).
[31] M.-L. Du, A. Filin, V. Baru, X.-K. Dong, E. Epelbaum,
F.-K. Guo, C. Hanhart, A. Nefediev, J. Nieves, and Q. Wang,
Phys. Rev. Lett. 131, 131903 (2023).
[32] J. R. Green, A. D. Hanlon, P. M. Junnarkar, and H. Wittig,
Phys. Rev. Lett. 127, 242003 (2021).
[33] A. B. a. Raposo and M. T. Hansen, Proc. Sci. LATTICE2022 (2023) 051.
[34] J. Nebreda and J. R. Pelaez, Phys. Rev. D 81, 054035
(2010).
[35] D. J. Wilson, R. A. Briceno, J. J. Dudek, R. G. Edwards, and
C. E. Thomas, Phys. Rev. D 92, 094502 (2015).
[36] D. R. Bolton, R. A. Briceno, and D. J. Wilson, Phys. Lett. B
757, 50 (2016).
[37] D. J. Wilson, R. A. Briceno, J. J. Dudek, R. G. Edwards, and
C. E. Thomas, Phys. Rev. Lett. 123, 042002 (2019).
[38] R. Molina and J. Ruiz de Elvira, J. High Energy Phys. 11
(2020) 017.
[39] G. K. C. Cheung, C. E. Thomas, D. J. Wilson, G. Moir, M.
Peardon, and S. M. Ryan (Hadron Spectrum Collaboration),
J. High Energy Phys. 02 (2021) 100.
[40] L. Gayer, N. Lang, S. M. Ryan, D. Tims, C. E. Thomas, and
D. J. Wilson (Hadron Spectrum Collaboration), J. High
Energy Phys. 07 (2021) 123.
[41] A. Rodas, J. J. Dudek, and R. G. Edwards, Phys. Rev. D
109, 034513 (2024).
[42] M. Albaladejo, F. K. Guo, C. Hidalgo-Duque, J. Nieves, and
M. P. Valderrama, Eur. Phys. J. C 75, 547 (2015).
[43] V. Baru, E. Epelbaum, A. A. Filin, C. Hanhart, U.-G.
Meißner, and A. V. Nefediev, Phys. Lett. B 763, 20
(2016).

241901-6

## PDF page 7

PHYSICAL REVIEW LETTERS 132, 241901 (2024)
[44] R. Aaij et al. (LHCb Collaboration), Phys. Rev. D 102,
112003 (2020).
[45] R. Aaij et al. (LHCb Collaboration), Phys. Rev. Lett. 131,
071901 (2023).
[46] K. Chilikin et al. (Belle Collaboration), Phys. Rev. D 95,
112003 (2017).
[47] X.-K. Dong, F.-K. Guo, and B.-S. Zou, Commun. Theor.
Phys. 73, 125201 (2021).
[48] N. A. Tornqvist, Z. Phys. C 61, 525 (1994).
[49] T. Barnes, S. Godfrey, and E. S. Swanson, Phys. Rev. D 72,
054026 (2005).
[50] M. R. Pennington and D. J. Wilson, Phys. Rev. D 76,
077502 (2007).
[51] I. V. Danilkin and Y. A. Simonov, Phys. Rev. Lett. 105,
102002 (2010).
[52] P. G. Ortega, J. Segovia, D. R. Entem, and F. Fernández,
Phys. Lett. B 778, 1 (2018).
[53] F.-K. Guo and U.-G. Meissner, Phys. Rev. D 86, 091501(R)
(2012).
[54] E. Wang, W.-H. Liang, and E. Oset, Eur. Phys. J. A 57, 38
(2021).
[55] E. Wang, H.-S. Li, W.-H. Liang, and E. Oset, Phys. Rev. D
103, 054008 (2021).
[56] O. Deineka, I. Danilkin, and M. Vanderhaeghen, Phys. Lett.
B 827, 136982 (2022).
[57] R. Aaij et al. (LHCb), J. High Energy Phys. 07 (2019) 035.
[58] S. Uehara et al. (Belle Collaboration), Phys. Rev. Lett. 96,
082003 (2006).
[59] B. Aubert et al. (BABAR Collaboration), Phys. Rev. D 81,
092003 (2010).
[60] S. Uehara et al. (Belle Collaboration), Phys. Rev. Lett. 104,
092001 (2010).
[61] M. T. Hansen and S. R. Sharpe, Phys. Rev. D 86, 016007
(2012).

[62] R. A. Briceño, J. J. Dudek, and L. Leskovec, Phys. Rev. D
104, 054509 (2021).
[63] A. Radhakrishnan, J. J. Dudek, and R. G. Edwards (Hadron
Spectrum Collaboration), Phys. Rev. D 106, 114513 (2022).
[64] R. G. Edwards and B. Joo, Nucl. Phys. B Proc. Suppl. 140,
832 (2005).
[65] M. A. Clark, R. Babich, K. Barros, R. C. Brower, and C.
Rebbi, Comput. Phys. Commun. 181, 1517 (2010).
[66] R. Babich, M. A. Clark, and B. Joo, in SC 10 (Supercomputing 2010) New Orleans, Louisiana, 2010 (2010),
arXiv:1011.0024.
[67] K. Clark, B. Joo, A. Strelchenko, M. Cheng, A. Gambhir,
and R. Brower, in Proceedings of SC 16 (Supercomputing
2016) Salt Lake City, Utah, 2016 (2016).
[68] B. Joó, D. Kalamkar, K. Vaidyanathan, M. Smelyanskiy, K.
Pamnany, V. Lee, P. Dubey, and W. Watson, in Supercomputing, Lecture Notes in Computer Science Vol. 7905,
edited by J. Kunkel, T. Ludwig, and H. Meuer (Springer,
Berlin, Heidelberg, 2013), pp. 40–54.
[69] B. Joó, eMG_PROTO: A Multigrid Library for QCD,
https://github.com/JeffersonLab/mg_proto/.
[70] J. C. Osborn, R. Babich, J. Brannick, R. C. Brower, M. A.
Clark, S. D. Cohen, and C. Rebbi, Proc. Sci. LATTICE2010
(2010) 037.
[71] R. Babich, J. Brannick, R. C. Brower, M. A. Clark, T. A.
Manteuffel, S. F. McCormick, J. C. Osborn, and C. Rebbi,
Phys. Rev. Lett. 105, 201602 (2010).
[72] J. Chen, R. G. Edwards, and W. Mao, in PASC '23:
Proceedings of the Platform for Advanced Scientific Computing Conference (Association for Computing Machinery
(ACM), 2023).
[73] www.hadspec.org.
[74] www.csd3.cam.ac.uk.
[75] www.dirac.ac.uk.

241901-7
