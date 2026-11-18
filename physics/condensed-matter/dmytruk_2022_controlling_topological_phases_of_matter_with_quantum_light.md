Source: see manifest row of the PDF
PDF sha256: 819e74974e4a453000feed9cead91651f202168f5cf90c69af65469d85b6596d
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of dmytruk_2022_controlling_topological_phases_of_matter_with_quantum_light.pdf

Transcription of `dmytruk_2022_controlling_topological_phases_of_matter_with_quantum_light.pdf` in this directory, 9 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-9 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

ARTICLE
https://doi.org/10.1038/s42005-022-01049-0

OPEN

Controlling topological phases of matter with
quantum light

1234567890():,;

Olesia Dmytruk1 ✉ & Marco Schirò1 ✉

Controlling the topological properties of quantum matter is a major goal of condensed matter
physics. A major effort in this direction has been devoted to using classical light in the form of
Floquet drives to manipulate and induce states with non-trivial topology. A different route can
be achieved with cavity photons. Here we consider a prototypical model for topological phase
transition, the one-dimensional Su-Schrieffer-Heeger model, coupled to a single mode cavity.
We show that quantum light can affect the topological properties of the system, including the
ﬁnite-length energy spectrum hosting edge modes and the topological phase diagram. In
particular we show that depending on the lattice geometry and the strength of light-matter
coupling one can either turn a trivial phase into a topological one or viceversa using quantum
cavity ﬁelds. Furthermore, we compute the polariton spectrum of the coupled electronphoton system, and we note that the lower polariton branch disappears at the topological
transition point. This phenomenon can be used to probe the phase transition in the
Su-Schrieffer-Heeger model.

1 JEIP, UAR 3573 CNRS, Collège de France, PSL Research University, 11 Place Marcelin Berthelot, 75321 Paris, Cedex 05, France.

✉email: olesia.dmytruk@

college-de-france.fr; marco.schiro@college-de-france.fr
COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

1

## PDF page 2

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

L

ight-control of quantum materials is an emerging goal of
condensed matter physics. While traditionally light has
played the role of spectroscopic probe, recent experimental
efforts have demonstrated the possibility of inducing novel phases
of matter by selective irradiation1,2 or by coupling to cavity
ﬁelds3–7.
Topological phases of matter8,9 play an important role in this
perspective due to their robustness and their possible application
in quantum technologies. As such there has been tremendous
interest in the possibility of enhancing or inducing topological
properties in electronic system by light, a notable example being
the Floquet topological insulator10,11. Floquet-engineered topological band structure was experimentally demonstrated in a
variety of solid state materials irradiated by circularly polarized
light12,13. Similar efforts in realizing topological phases of matter
using time-modulated optical lattices have been made with
ultracold atoms14. Quantum ﬂuctuations of the light ﬁeld in a
cavity offer new possibility to probe, control and tune the properties of a material, leading for example to polaritons, hybrid
light-matter
excitations,
with
non-trivial
topological
properties15–21 or to anomalous Hall response in presence of a
circularly polarized ﬁeld22. Here we ask the question of what
happens to a topological material due to the coupling to cavity
photons. Such question is of direct experimental relevance given
the recent observation of a breakdown of topological protection
in an integer Quantum Hall system coupled to a cavity23 and can
be also explored with ultracold atoms embedded in high-ﬁnesse
resonators24,25.
A prototypical model for topological behavior in one dimension is the Su-Schrieffer-Heeger (SSH) model26, originally introduced to describe conducting electrons in polyacetylene and
which later found applications in a variety of settings27–33. The
SSH model describes a 1D dimerized chain with alternating weak
and strong nearest-neighbor hoppings and displays a topological
transition associated with a non-trivial Zak phase. The experimental realization of the SSH model has been demonstrated in
ultracold atoms34–36, graphene nanoribbons37,38 and in various
platforms for topological phenomena, from photonics39–41 to
mechanical metamaterials42.
In this work, we study the interplay of topological phases of
matter and quantum light by considering the SSH model coupled
to a single mode photonic resonator through the full gauge
invariant Peierls phase. We show that quantum ﬂuctuations of
the light ﬁeld can have dramatic effects on the topological
properties of the system and most remarkably turn a trivial
insulating phase into a topological one above a critical lightmatter coupling, with emergence of non-trivial topological edge

modes. This topological transition is possible due to the structure
of the Peierls phase, which preserves chiral symmetry and
introduces a non-trivial dependence from the lattice geometry,
similarly to the case of classical light explored in the context of
Floquet driving. Differently from the latter, however, our results
do not suffer from heating runaway problems that often plagued
Floquet engineering schemes and required high-frequency driving or tailored dissipation. Finally, when considering the limit of
an inﬁnite chain we show that the topological transition reduces
to the case of the isolated SSH model. However, photons retain
memory of the non-trivial topology of the system as we show by
computing the polariton spectrum of the hybrid system. We ﬁnd
that the lower polariton branch disappears when the hopping
amplitudes is tuned to satisfy the topological criterion. Thus,
measurements of the polariton frequencies could provide direct
access to the topological phase transition point.
Results
The Model. We consider a one-dimensional SSH model coupled
to a single mode cavity (Fig. 1). The SSH model describes spinless
electrons hopping on a one-dimensional chain composed of L
unit cells with two sublattices A and B.
The Hamiltonian reads

L 
H SSH ¼ v ∑ cyjA cjB þ cyjB cjA
j¼1
ð1Þ

L1
 w ∑ cyjþ1;A cjB þ cyjB cjþ1;A ;
j¼1

where v ≥ 0 is the intracell hopping amplitude, w ≥ 0 is intercell
hopping amplitude, and cyjμ (cjμ) are the fermionic creation
(annihilation) operators at site j and sublattice μ = A, B. As
shown in Fig. 1 the lattice constant is a0 while the intracell
distance between A and B lattice sites is b0 < a0. In absence of any
light-matter interaction the SSH model displays a well-known
topological phase transition as the ratio between the two
hoppings is tuned. In particular the ground-state of the system
is in topological phase for v < w with ﬁnite Chern number and in
a topologically trivial phase for v > w. We emphasize that in this
case the spectrum does not depend on the lattice spacing b0. The
single mode cavity Hamiltonian is given by


1
ð2Þ
H ph ¼ ωc ay a þ ;
2
where ωc is the mode frequency and a† (a) are the photon
creation (annihilation) operators satisfying [a, a†] = 1. We couple
the SSH chain to the cavity mode through the gauge invariant
Peierls substitution43–47, which amounts to dress the hoppings
amplitudes entering the SSH Hamiltonian Eq. (1) as v ! v eieA‘AB
and w ! weieA‘BA , where e is the electric charge, A ¼ A0 ða þ
ay Þ is the uniform vector potential, and ℓAB = b0, ℓBA = a0 − b0
represent respectively the distance between atoms in the same
(different) unit cell. To understand the origin of this different
renormalization we note that the Peierls substitution is
completely equivalent to applying a unitary transformation Ω
to electronic Hamiltonian47, i.e.
H ¼ H ph þ Ωy H SSH Ω;

Fig. 1 Scheme of the Su-Schrieffer-Heeger chain coupled to cavity. A onedimensional dimerized Su-Schrieffer-Heeger chain with intracell v (black
solid line) and intercell w (black dashed line) hopping amplitudes coupled
to a single mode cavity with frequency ωc. The strength of the light-matter
coupling is given by g. The lattice constant is a0, and the distance between
the sublattices A and B within the same unit cell (blue dashed square) is b0.
2

ð3Þ

where the unitary is deﬁned as
Ω¼e

ieA ∑ Rjμ cyjμ cjμ
jμ

:

ð4Þ

Here, Rjμ indicates the position of the atom in the μ = A, B
sublattice, with RjA = ja0 and RjB = ja0 + b0. Under this unitary
transformation the fermionic operators cjA, cjB acquire a site-

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

## PDF page 3

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

dependent phase (See Methods) which leads to the full lightmatter Hamiltonian of the form (setting a0 = 1)

L  g
ipﬃ b ðaþay Þ y
H ¼v ∑ e L 0
cjA cjB þ h.c.
j¼1


L1
g
ipﬃ ð1b Þðaþay Þ y
cjþ1;A cjB þ h.c.
w ∑ e L 0
j¼1


1
y
þ ωc a a þ :
2

ð5Þ

Several observations are in order here concerning this Hamiltonian. First, the two hopping integrals v, w are renormalised by
different Peierls factors due to the different distance between
atoms within the same or different unit cell. This gives an explicit
dependence of the Hamiltonian from the ratio of lattice spacing
b0, which instead is missing in equilibrium and will play a key role
in the following. Furthermore, we note that using the unitary
operator deﬁned in Eq. (4) one can write down a fully equivalent
light-matter Hamiltonian in the Dipole Gauge (see Methods).
Finally, we note that in Eqs. (4)–(5)
pﬃﬃﬃwe have rescaled light-matter
coupling g = eA0 by the factor 1= L, namely, we consider the socalled collective ultra-strong coupling regime48–51. While this
ensures that in the thermodynamic limit a single cavity mode
does not affect thermodynamic bulk properties, as we indeed are
going to recover, we show here that the topological properties, in
particular the emergence of edge modes in the ﬁnite-length
energy spectrum is strongly modiﬁed by the coupling to light.
Energy spectrum of ﬁnite-length SSH model coupled to photons. A signature of the non-trivial topology of the SSH model is
contained in its ﬁnite-length energy spectrum which hosts edge
modes exponentially localized near the boundaries52. The ﬁrst
question we address is therefore what is the fate of the edge
modes in presence of a ﬁnite coupling to the cavity mode. To this
extent we study the model within a factorized
   mean-ﬁeld ansatz
for the ground-state of the form jΨi ¼ ψ ϕ , corresponding to
neglecting correlations between the cavity modes and electrons.
This ansatz is justiﬁed in the limit of large L where electron and
photons are expected to decouple. Within this ansatz we obtain
(see Methods) a renormalised SSH model with hopping amplitudes v and w dressed by the cavity photon

L 
  
 
~ cyjA cjB þ h.c.
H mf
el ¼ ϕ H ϕ ¼ ∑ v
j¼1
ð6Þ

L1
~ cyjþ1;A cjB þ h.c. ;
 ∑ w
j¼1

where we introduced the renormalized hoppings v~ ¼
vφðg; b0 Þ; ~
w ¼ wφðg; 1  b0 Þ with the renormalization factor
 ipg‘ﬃ ðaþay Þ  
ϕ ;
ð7Þ
φðg; ‘Þ ¼ ϕe L
and a renormalised mean-ﬁeld photon Hamiltonian H mf
ph (see
Methods for the
the photonic
 complete expression). We ﬁnd 
ground state ϕ and the electronic ground-state ψ by solving
the associated mean-ﬁeld Hamiltonian self-consistently. We ﬁnd
that the renormalization factor φ(g, ℓ) is purely real, a consequence of the fact that the ground-state of the coupled electronphoton does not carry a ﬁnite current.
The ﬁnite-sized spectrum of the effective SSH model is plotted
in Fig. 2 for different values of the light-matter coupling g and the
geometrical factor b0. As expected for g = 0 we ﬁnd a topological
transition for w/v > 1, when a pair of exponentially small almost
zero modes appear in the middle of the bulk gap. Upon including
a ﬁnite light-matter coupling we see that the energy spectrum

0.2
0.1
0.0
- 0.1
- 0.2

0.6

0.8

1.0

1.2

1.4

Fig. 2 Energy spectrum of the Su-Schrieffer-Heeger chain in presence of
cavity. Energy spectrum of the Su-Schrieffer-Heeger model coupled to a
single mode cavity as a function of hopping ratio w/v. Black solid lines
correspond to zero light-matter coupling g = 0 and red dashed (blue dotdashed) lines correspond to the sublattice distance b0 = 0.8 (b0 = 0.2) and
g = 20. Other parameters are chosen as intracell hopping v = 1, number of
unit cells L = 100, lattice constant a0 = 1, cavity frequency ωc = 0.5, and
maximum number of photons Nmax = 10.

changes depending on the value of the parameter b0. In particular,
for b0 = 0.8 we see that the topological transition is pushed to
smaller values of w/v, indicating that coupling to the quantum
ﬂuctuation of the light ﬁeld favor the topological phase. On the
other hand, for b0 = 0.2, the situation is reversed and the edge
modes appear for larger values of the hopping ratio w/v. This
different behavior can be understood by looking at the different
photonic renormalization to the hopping integrals, as we are
going to discuss further below.
Topological phase diagram. We now turn to discuss the bulk
phase diagram of the coupled electron-photon system and the
emergence of topological phase transitions. To this extent we
consider a system with periodic boundary conditions and no
edges. This allows to write the Hamiltonian
space.
 in momentum

Introducing the fermionic ﬁeld ψ yk ¼ cyk;A ; cyk;B , the Peierls
Hamiltonian in the momentum space can be written in compact
form as


1
y
y
y
ð8Þ
H ¼ ∑ ψ k Hk ða; a Þψ k þ ωc a a þ ;
2
k
where we have introduced an effective single particle electronic
Hamiltonian Hk ða; ay Þ ¼ ∑α dkα ða; ay Þσ α , with σα=x,y,z Pauli
matrices. The structure ofthis Hamiltonian is encoded in the
vector dkα ¼ d kx ; d ky ; dkz , which depends on the photonic
degrees of freedom, the light-matter coupling and the ratio of
lattice spacing, and reads
dkx ¼ v cos Kb0  w cos Kð1  b0 Þ ;

ð9Þ

dky ¼ v sin Kb0  w sin Kð1  b0 Þ ;

ð10Þ

dkz ¼ 0;

ð11Þ

with K ¼ k þ pgﬃﬃL a þ ay the shifted momentum.
For topological systems such as the SSH model the chiral (or
sublattice) symmetry plays a pivotal role, protecting the existence
of a transition between two insulating phases with different
topological properties. In the language of the pseudo-spin
components used in Eq. (8) this requires that there is no mass

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

3

## PDF page 4

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

a

1.2

b 1.2

1.1

1.1

1.0

1.0

0.9

0.9

0.8
0

5

10

15

20

0.8
0

c 1.10

d 1.2

1.05

1.1

1.00

1.0

0.95

0.9

0.90
0.0

0.2

0.4

0.6

0.8

1.0

0.8

5

2000

10

4000

15

6000

8000

20

10 000

Fig. 3 Topological phase diagram of the Su-Schrieffer-Heeger model in presence of cavity. Topological phase diagram as a function of the light-matter
coupling g and hopping ratio w/v for a the sublattice distance b0 = 0.2 and b b0 = 0.8. Trivial (white area) and topological phases (a blue for b0 = 0.2 and
b red for b0 = 0.8) are separated by the phase boundary (blue and red lines) given by Eq. (13). Phase boundary is shifted to larger (smaller) values of w/v
for b0 = 0.2 (b0 = 0.8). c Topological phase diagram as a function of b0 and w/v for a ﬁxed value of the light-matter coupling g = 10. The topological phase
is entered at smaller (larger) values of w/v for b0 > 0.5 (b0 < 0.5). d Topological phase diagram as a function of the number of unit cells L and w/v for
g = 20. Phase boundary goes to w/v = 1 for large values of L for b0 = 0.2 (blue dashed line) and b0 = 0.8 (red solid line). Other parameters are ﬁxed as
intracell hopping v = 1, lattice constant a0 = 1, cavity frequency ωc = 0.5, maximum number of photons Nmax = 10, and L = 100 (except panel d).

term for the electrons in the A and B sublattices, i.e. dkz = 0. From
the structure of the Hamiltonian in momentum space we see
therefore that even in presence of quantum light, g ≠ 0, the chiral
symmetry is preserved by the Peierls substitution. This ensures
the existence of pairs of eigenstates with opposite energies.
In the purely electronic model, corresponding to g = 0, the
topological phase transition in the thermodynamic limit would
be associated with a closing and reopening of the bulk gap. For
a ﬁnite-size chain the gap remains ﬁnite and the transition
point is associated to the minimum energy gap. In presence of
light-matter coupling in the collective ultrastrong coupling
regime it is important to keep a ﬁnite L to obtain non-trivial
effects from the photons. As in the previous section, we employ
the mean-ﬁeld approach to calculate the bulk energy spectrum
in the presence of the coupling to photons (see Methods). By
solving the electronic and photonic mean-ﬁeld Hamiltonian
self-consistently, we ﬁnd that the photon renormalization to the
electronic hoppings are purely real, and the electronic bulk
energy spectrum reads
qﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
ð12Þ
~ 2  2~vw
~ cosðkÞ;
ϵk ¼ v~2 þ w
~ deﬁned before Eq. (7). The bulk energy gap is given by
with v~; w
the
value pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
of
the
dispersion
at
k = π/L,
~ 2  2~vw
~ cosðπ=LÞ. From this we see that
Δ ¼ min ϵk ¼ v~2 þ w
the phase boundary between trivial and topological phases is
~ =~v ¼ 1, i.e.
implicitly given by the equation w
wc
φðg; b0 Þ
¼
;
ð13Þ
φðg; 1  b0 Þ
v
where we emphasize how the renormalization factors depend both
on the electronic and photonic parameters, such as light-matter
coupling and cavity frequency, as well as the geometric factor b0,
through the self-consistent ground state entering Eq. (8).
Solving the photonic and electronic Hamiltonian selfconsistently we ﬁnd numerically the topological phase diagram
4

that we plot for two values of b0 in Fig. 3 (panel (a) b0 = 0.2, panel
(b) b0 = 0.8). From this we see, even more clearly, that the lightmatter coupling is able to affect the ﬁnite-size topological
structure of the system. As already observed in the ﬁnite-sized
edge spectrum, for b0 = 0.2 we see that coupling to quantum light
is energetically detrimental and the topological phase of the SSH
model is destroyed. Strikingly, we see that for b0 = 0.8 a trivial
SSH model can be turned into a topological phase by increasing
light-matter interactions. This is one of the main result of this
work which opens up the exciting possibility of controlling
topology with light. Another interesting aspect is the role played
by the geometrical factor b0 in shaping the phase diagram of the
system. As we see in Fig. 3, panel (c), also tuning b0 gives rise to
different behavior and a possible topological transition. This
suggests a comparison with the classical Floquet case28, that we
leave for the discussion.
Finally, we discuss the dependence of the critical hopping
strength wc from the size of the system L. As we show in panel (d)
of Fig. 3 upon increasing L the critical coupling approaches the
value wc = v, corresponding to the topological transition in the
absence of the cavity (g = 0). This result is consistent with the
recent literature stating that single mode cavity are not expected
to change bulk properties of the system in the thermodynamic
limit47,51,53,54.
Photonic properties. In this section, we focus on the properties
of the photonic states coupled to a ﬁnite-length SSH chain. In the
basis
  of the Fock states, the photon ground state can be written as
ϕ ¼ ∑ c jni, where n denotes the number of photons. The
n n
coefﬁcients cn could be found by calculating
   the eigenvectors of
H ψ . We ﬁnd that the
¼
ψ
the photonic Hamiltonian H mf
ph
coefﬁcients cn corresponding to odd number of photons are zero
(see inset in Fig. 4). This reﬂects a discrete symmetry of the
photonic Hamiltonian which in presence of light-matter coupling
is invariant under a ↔ − a, rather than under a fully phase

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

## PDF page 5

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

ﬂuctuations47,58. This can be written as

3.5
3.0

AðωÞ ¼ 

2.5
2.0
1.5

0.4

1.0

0.2

0.5

0

0

0.5
0.3
0.1

2

4

ð15Þ

where χ(ω) = K(ω) − 〈Jd〉 is the current-current correlation
function that is a sum of paramagnetic and diamagnetic contributions (see Methods),

0.7
0.6

1
χ 00 ðωÞðω þ ωc Þ2
;
2
2
π ðω  ωc  2ωc χ 0 ðωÞÞ2 þ ð2ωc χ 00 ðωÞÞ2

2

4

6

6

8

8

10

10

Fig. 4 Properties of photonic states coupled to the Su-Schrieffer-Heeger
chain. Expectation values 〈X2〉 (red solid line) and 〈P2〉 (black dashed line)
as a function of the light-matter coupling g for the intercell hopping w = 1. In
the absence of the coupling between the cavity and the Su-SchriefferHeeger chain, the expectation values are equal, 〈X2〉 = 〈P2〉 = 1/2. For ﬁnite
values of g, 〈X2〉 decreases and 〈P2〉 increases with increasing g, and
photonic state becomes squeezed. Inset: Photon probability density ∣cn∣2 as
a function of photon number n for g = 10. Other parameters are chosen as
number of unit cells L = 100, lattice constant a0 = 1, intracell hopping v = 1,
cavity frequency ωc = 0.5, and maximum number of photons Nmax = 10.

rotation. This symmetry is protected by the absence of an electronic current in the ground-state, and thus of superradiance,
which otherwise would generate terms linear in the photonic ﬁeld
and non-symmetric. Furthermore, as we are going to see it
implies squeezing. To this extent we introduce the position X ¼
pﬃﬃ
pﬃﬃ
a þ ay = 2 and momentum P ¼ i a  ay = 2 operators.
For a bare photonic Hamiltonian Eq. (2), the expectation values
of the X2 and P2 operators are equal, 〈X2〉 = 〈P2〉 = 1/2. However,
for a single mode photonic Hamiltonian coupled to the SSH
chain we ﬁnd that 〈P2〉 > 〈X2〉, therefore, photonic state becomes
squeezed (see Fig. 4). We can understood this behavior from the
form of the effective photonic Hamiltonian (see Methods) for
large L and from the fact that, as we said, there is no coherent
displacement induced by the electrons i.e.


1
2
y
þ r a þ ay ;
¼
ω
a
a
þ
H mf
c
ph
2

ð14Þ

where the squeezing parameter r is controlled by the renormalized kinetic energy of the SSH chain (see Methods).
Polariton spectrum as signature of topological phase transition. Finally, we conclude discussing how the light emitted from
the cavity, encoded in the photonic spectral function and measurable through transmission/reﬂection experiments55–57, contains crucial signatures of the topological phase transition in the
SSH system. The excitations of the SSH chain coupled to a cavity
mode are hybrid light-matter polariton quasiparticles whose
energies and lifetime can be read out from the photonic spectral
function. This strongly depends on the topological properties of
the underlying electronic system. Here we show in particular that
at the topological transition one polariton mode is pushed to zero
frequency and loses spectral weight, thus leaving only two peaks
in the spectral function. SpeciﬁcallyR we consider the photon
spectral function AðωÞ ¼  π1 Im dteiωt ðiθðtÞÞh aðtÞ; ay i,
dressed by the electronic system including 1/L Gaussian

Kðτ  τ 0 Þ ¼ hT c J p ðτÞJ p ðτ 0 Þi;

ð16Þ

g
J p ¼ pﬃﬃﬃ ∑ ψ yk ðw sinðkÞσ x  w cosðkÞσ y Þψ k ;
L k

ð17Þ

g2
∑ ψ y ðw cosðkÞσ x þ w sinðkÞσ y Þψ k :
L k k

ð18Þ

Jd ¼ 

We show the behavior of the photonic spectral function in the top
panel of Fig. 5. In the previous section, we have demonstrated
that in the thermodynamic limit the topological phase transition
point remains unchanged by the cavity photons even in the
(ultra)strong coupling limit and takes place when v = w. Let us
ﬁrst consider the behavior of the spectral function in the trivial
phase (v > w). In the absence of the coupling to the cavity there is
only one peak in the spectral function at ωc. Since we ﬁxed the
system parameters such that ωc is equal to the band gap 2E(k),
where E(k) is the electronic bulk energy spectrum given by Eq.
(12) in the absence of coupling to cavity, in the SSH model at
k = 0, for ﬁnite values of g the peak at ωc in the spectral function
splits into two. Moreover, there is a third peak appearing in A(ω)
coming from the band gap at k = π. Therefore, there are three
peaks in A(ω) corresponding to three polariton branches. As we
ﬁx the parameters of the SSH chain such that v = w, the lowest
polariton branch disappears. This is related to closing of the bulk
gap at k = 0 and is a direct signature of the topological phase
transition. Decreasing the intracell hopping v further the SSH
model enters the topological phase (v < w) and the lowest
polariton branch reemerges. To better illustrate the disappearance
of the polariton branch at the topological phase transition we plot
the cross section of the spectral function for a ﬁxed value of the
light-matter coupling constant g = 2 as a function of frequency in
the lower panel of Fig. 5. We note in passing that the width of the
second polariton branch is larger in the topological phase.
We provide a simple analytical argument to understand the
disappearance of the lowest polariton branch at the phase
transition. First, we note that the light-matter Hamiltonian in Eq.
(8), when written in terms of pseudo-spin operators
σ kα ¼ ψ yk σ α ψ k , takes the form of a spin-photon problem often
encountered in quantum optics. Here, however, pseudo-spins at
different k points are coupled to the same cavity mode. The
lowest excitations of the system can be then obtained from a spinwave analysis focusing on the k = 0 sector of the SSH model (see
Methods). This allows to write down an effective Hamiltonian in
terms of bosonic spin-wave modes b (b†) coupled to cavity
photons
~ k¼0 ¼ ωc ay a þ ωx by b  igwsða þ ay Þðb  by Þ
H

ð19Þ
g2
ω
2
wsða þ ay Þ  x L;
2
2
where ωx = 2∣v − w∣ and s = sign[v − w]. We ﬁnd the analytical
expression for the polariton energies by using the BogoliubovHopﬁeld transformation59

qﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
1
2
~ 2c ± ð~
ω2x þ ω
ð20Þ
ω2± ¼
ω2c  ω2x Þ þ 16g 2 ωc w2 ωx ;
2
pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
where ~
ωc ¼ ωc ðωc  2wsg 2 Þ. Next, we note that at v = w the
lower polariton branch ω− = 0 is absent, and the upper polariton


COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

5

## PDF page 6

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

Fig. 5 Photon spectral function. a–c Spectral function A(ω) (amplitude normalized by its maximum value is given by the color bar) as a function of the
light-matter coupling g and frequency ω. Red dashed line corresponds to frequency ωc and blue dot-dashed line corresponds to 2E(k = π). a Trivial phase:
intracell hopping v = 0.8 and intercell hopping w = 0.5. There are three polariton branches. b The gap at k = 0 closes for v = w = 0.5 corresponding to the
topological phase transition. There are only two polariton branches. c Topological phase, v = 0.2, w = 0.5. There are three polariton branches. The photon
frequency ωc is chosen such that ωc = 2E(k = 0) [for v ≠ w]. Other parameters are ﬁxed as ωc = 0.6 and η = 10−3. d-f Spectral function A(ω) as a function
of ω for g = 2. d There are three peaks. e There are two peaks. f There are three peaks. The lower polariton branch is absent at the topological phase
transition point.

pﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
frequency is given by ωþ ¼ ω2c  2ωc g 2 w. In agreement with
the spectral function calculations, the lower polariton branch
disappears at the phase transition point providing a way to probe
the phase transition point in the SSH model via cavity response
measurements.
Conclusions. In this work, we have shown that coupling an
electronic system to the quantum light ﬁeld of a cavity can be
used to control the topological properties of a system and most
notably to drive a topological transition with the emergence of
edge modes, even in a regime where the uncoupled system would
be topologically trivial. We have highlighted these results in the
context of paradigmatic model for topological phases of matter,
the SSH chain, that we have studied in presence of a ﬁnite coupling to a single-mode cavity encoded in the gauge-invariant
Peierls phase.
We have shown that quantum light-matter coupling does not
spoil the chiral symmetry, which protects the topological phase in
the isolated SSH chain and furthermore introduces a non-trivial
dependence from the ratio of lattice spacing which can be used as
further controlled parameter to control the phase diagram of the
system together with the light-matter coupling. Computing the
ﬁnite-length energy spectrum as well as the bulk spectrum using a
mean-ﬁeld decoupling of electrons and photons, which treats the
Peierls phase non-perturbatively, we have shown that light-matter
interaction can turn a trivial insulator into a topological one,
depending on the value of b0. Our work therefore provides a
simple and paradigmatic example of non-trivial topology induced
by quantum light. We emphasize that with respect to the largely
explored Floquet engineering schemes, where classical oscillating
light ﬁelds are used to induce non-trivial topology, our scheme
does not suffer from any heating problem, an issue which requires
in the Floquet context to assume high-frequency driving.
6

Finally, we found that in the thermodynamic limit the
topological phase transition point v = w in the SSH model is
insensitive to cavity photons. In this limit, we evaluated the
polariton spectrum of the hybrid electron-photon system that
revealed the appearance of three polariton branches for v ≠ w.
Interestingly, we noticed that the lowest polariton branch
disappears exactly at the topological phase transition point v = w,
the result which was further supported by the full analytical
solution within the effective spin-wave theory. Therefore, cavity
photons provide a way to both control and probe topological
properties of the electronic systems. In future works, it would be
interesting to consider inhomogeneous electromagnetic ﬁeld,
recently utizlized in the context of superradiance46,60,61, since a
momentum-dependent photonic operators might bring a new
ingredient to control topological properties of the material.
Methods
Gauge-ﬁxing of electrons coupled to quantum light. In this section we derive the
Peierls Hamiltonian used in the main text by means of a unitary transformation
acting on the electrons. Starting from the operator Ω deﬁned in Eq. (4) of the main
text we see that the fermionic operators transform as
Ωy ciμ Ω ¼ eieARiμ ciμ ;
where Riμ = ia0 + δμ,Bb0. Applying this unitary operator to the SSH Hamiltonian
generates an electron-photon Hamiltonian
H ¼ H ph þ Ωy H SSH Ω;
which is equivalent to a renormalization of the hopping integrals according to the
Peierls phase, i.e.
cyjA cjB ! eigðaþa Þb0 cyjA cjB ;
y

cyjþ1A cjB ! eigðaþa Þða0 b0 Þ cyjþ1A cjB ;
y

ð21Þ

ð22Þ
pﬃﬃﬃ
which reduces to the result in the main text for a0 = 1 and g ¼ g= L. Furthermore, using the same unitary operator Ω it is possible to write down the lightmatter Hamiltonian in the dipole gauge. This reads

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

## PDF page 7

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0





  
1
gb
y
 
þ cos pﬃﬃﬃ0 ða þ ay Þ
H mf
ph ¼ ψ H ψ ¼ ωc a a þ
2
L


  
  
gb
´ v ∑ ψ σ kx ψ þ sin p 0ﬃﬃﬃ ða þ ay Þ v ∑ ψ σ ky ψ
k
k
L


   
g 1  b0
pﬃﬃﬃ ða þ ay Þ w ∑ ψ σ kx ψ cosðkÞ
 cos
k
L


o
  
g 1  b0
pﬃﬃﬃ ða þ ay Þ
þ ψ σ ky ψ sinðkÞ þ sin
L
n   
o
  
´ w ∑ ψ σ kx ψ sinðkÞ  ψ σ ky ψ cosðkÞ :

H D ¼ ΩH ph Ωy þ H SSH ;
gω
H D ¼ H ph þ H SSH þ i pﬃﬃﬃc ða  ay Þ ∑ Rjμ cyjμ cjμ
jμ
L
g 2 ωc
y
y
∑ R R 0 0c c c 0 0c 0 0:
þ
L j0 jμμ0 jμ j μ jμ jμ j μ j μ

ð23Þ

Mean-ﬁeld decoupling between electrons and photons in ﬁnite-length SSH
chain coupled to photons. We provide details on the solution of the light-matter
Hamiltonian H Eq. (5) in mean
to neglecting correlations
 
  ﬁeld that corresponds
between the cavity modes ϕ and electrons ψ ,
  
jΨi ¼ ψ ϕ :
ð24Þ

k

In the thermodynamic limit, retaining only the leading terms we obtain Eq. (14)
of the main text, with a squeezing parameter r given by
   g 2 1  b0 2
g 2 b20
v ∑ ψ σ kx ψ þ
2L k
2L
n   
o
  
k

´ w ∑ ψ σ ψ cosðkÞ þ ψ σ k ψ sinðkÞ :

r ¼

As a result of the mean ﬁeld decoupling we have to solve an electronic mean ﬁeld
Hamiltonian given by Eq. (6) and a photonic mean ﬁeld Hamiltonian that reads
H mf
ph ¼



  
jj ipgﬃ b ðaþay Þ
ψ H ψ ¼ v CAB e L 0
þ h.c.


jþ1;j ipgﬃ ð1b Þðaþay Þ
 w CAB e L 0
þ h.c.


1
þ ωc ay a þ ;
2

ð25Þ

where we introduced two parameters
L

 
jj
CAB ¼ ∑ ψ cyjA cjB ψ ;

ð26Þ

L1

 
jþ1;j
CAB ¼ ∑ ψ cyjþ1;A cjB ψ :

ð27Þ

j¼1

j¼1

H mf
el ¼

h
i
  
ϕH ϕ ¼ ∑ hk σ k þ hk σ k ;
k

x x

y y

σ kα ¼ ψ yk σ α ψ k ;

ð29Þ


 
hkx ¼ ϕd kx ða; ay Þϕ ;

ð30Þ


 
hky ¼ ϕd ky ða; ay Þϕ :

ð31Þ

where we separated the different contributions to the total action S: Sph describes to
the photonic ﬁelds, Sel corresponds to the purely electronic system, and Sel-ph
describes to the electron-photon interaction,
Z β
0
0
ð38Þ
dτdτ 0 ϕ ðτÞd 1
Sph ¼ 
0 ðτ  τ Þϕðτ Þ;
0

  
ψ σ k ψ ¼ hk =ϵ ;
k

  
ψ σ ky ψ ¼ hky =ϵk ;

ð32Þ



g
dτ cos pﬃﬃﬃ ðϕðτÞ þ ϕ ðτÞÞ
L
0
h
i
´ ∑ w cosðkÞσ kx þ w sinðkÞσ ky
k

 h
i
g
þ sin pﬃﬃﬃ ðϕðτÞ þ ϕ ðτÞÞ ∑ w sinðkÞσ kx þ w cosðkÞσ ky :
k
L

Selph ¼ 

ð39Þ

k

Z β

ð40Þ

Here, ϕ ðτÞ; ϕðτÞ correspond to the photonic ﬁelds, and
0
0
d 1
0 ðτ  τ Þ ¼ δðτ  τ Þ ∂τ þ ωc :

Deﬁning
Z 0 ½ϕ; ϕ  ¼

Z





ð41Þ



D½C; C  eSel ½C;C Selph ½ϕ;ϕ ;C;C  ;

ð42Þ

the partition function can be rewritten as
Z
Z

Z ¼ D ϕ; ϕ eSph ½ϕ;ϕ  Z 0  D ϕ; ϕ eSeff ;

ð43Þ

ð33Þ

qﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
2
2
hkx þ hyx :

Similarly, the photonic mean-ﬁeld Hamiltonian reads

ð34Þ

ð44Þ

Expanding the action of the SSH model coupled to a single mode cavity up to
second order in photonic ﬁelds ϕ(τ), we arrive at
Z
~Seff ¼ 1 dτdτ 0 Φy ðτÞ D1 ðτ  τ 0 Þ  Πðτ  τ 0 Þ Φðτ 0 Þ;
ð45Þ
0
2
0
where Φy ðτÞ ¼ ϕ ðτÞ; ϕðτÞ , D1
0 ðτ  τ Þ is the bare photon Green’s function, and
Πðτ  τ 0 Þ is the polarization given by
0 2
1
2


δ log Z 0 ½Φ;Φ 
δϕ ðτÞδϕðτ 0 Þ

δ log Z 0 ½Φ;Φ 
δϕ ðτÞδϕ ðτ 0 Þ



δ2 log Z 0 ½Φ;Φ 
δϕðτÞδϕ ðτ 0 Þ

Πðτ  τ 0 Þ ¼ @ 2

where we introduced the energy of the SSH model in presence of cavity ﬁelds
ϵk ¼

0

h
i
dτdτ 0 ∑ ck;A ∂τ ck;A þ ck;B ∂τ ck;B  vσ kx ;

Seff ¼ Sph  log Z 0 :

At zero temperature, we ﬁnd for the expectation values over the electronic states
x

Sel ¼ 

Z β

where

and

x

ð36Þ

y

Photonic Green’s function—Gaussian ﬂuctuations. In this Section, we compute
the Gaussian 1/L corrections to the photon Green’s function47,58. For the sake of
simplicity we consider the SSH model with b0 = 0, since the results do not change
qualitatively with b0 in the large L limit. The partition function of the SSH model
can be written as
Z





Z ¼ D ϕ; ϕ ; C; C  eSph ½ϕ;ϕ ;C;C Sel ½C;C Selph ½ϕ;ϕ ;C;C  ;
ð37Þ

ð28Þ

where we introduced the pseudo-spin operators

x

k

We ﬁnd the electronic spectrum of the SSH model in presence of coupling to
cavity photons by solving Eqs. (6) and (25) self-consistently. In particular, we set
γ
g = 0 in H mf
el and calculate numerically CAB , where γ = jj or j, j + 1. Then we insert
γ
mf
~ . Afterwards, we insert v~ and w
~
CAB into H ph with g ≠ 0, and evaluate v~ and w
(calculated for g ≠ 0) into H mf
el and evaluate the eigenvalues of the electronic meanﬁeld Hamiltonian. We ﬁnd that the energy spectrum of the SSH chain is modiﬁed
in presence of coupling to cavity photons (Fig. 2).
Mean-ﬁeld solution of momentum space Hamiltonian. In order to obtain the
topological phase diagram we study the SSH model coupled to cavity in
momentum space. Starting from Eq. (5) and performing the Fourier transformation as cj;μ ¼ p1ﬃﬃL ∑k eikj ck;μ , we arrive at the Peierls Hamiltonian in the momentum
space given by Eq. (8). Similarly to the ﬁnite-length SSH chain, we solve Eq. (8)
within a mean ﬁeld approximation. The electronic mean-ﬁeld Hamiltonian reads

ð35Þ

δ log Z 0 ½Φ;Φ 
δϕðτÞδϕðτ 0 Þ

AjΦðτÞ¼α¼0 :

ð46Þ

Next, we ﬁnd that all four components of the polarization are equal and can be
written as


1 1
χðωÞ;
ð47Þ
ΠðωÞ ¼
1 1
where χ(ω) is the current-current correlation function deﬁned in the main text.

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

7

## PDF page 8

ARTICLE

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

Using Eqs. (16)–(18) and substitution sum with an integral, we ﬁnd the
expressions for the real
Z
g2 π
wðw  v cosðkÞÞ
χ 0 ðωÞ ¼
dk
2π π
Ek
ð48Þ

Z π 
2g 2
wðv cosðkÞ  wÞ 2
Ek
P
þ
dk
π
Ek
ω2  4E2k
π
and imaginary parts of the correlation function χ(ω)


Z
g2 π
wðv cosðkÞ  wÞ 2
χ 00 ðωÞ ¼ 
dk
2 π
Ek

ð49Þ

´ δ ω  2Ek  δ ω þ 2Ek :
Spin-wave theory for polariton spectrum. In this Section, we derive the spinwave spectrum of the polaritons. To this extent we start from Eq. (8) that we
rewrite in terms of the pseudo-spin operators deﬁned in Eq. (29). Then, considering only the momentum k = 0 and expanding to second order in g, we obtain
~ k¼0 ¼ ωc ay a  ωx σ~zk¼0 þ pgﬃﬃﬃ wsða þ ay Þ~
H
σ yk¼0
2
L
ð50Þ
g2
2
 wsða þ ay Þ σ~zk¼0 ;
2L
where ωx = 2∣v − w∣ and s = sign[v − w]. Performing Holstein—Primakoff
transformation47,62
pﬃﬃﬃ
ð51Þ
σ~yk¼0 ¼ i Lðb  by Þ;
σ~zk¼0 ¼ L  2by b;

ð52Þ

we arrive at Eq. (19). We ﬁnd analytical expression for the polariton energies Eq.
(20) by performing the Bogoliubov-Hopﬁeld transformation59.
Since we consider only k = 0 mode, it turns out that ω− always go to zero for
v ≠ w at the criticalpvalue
of the light-matter coupling
pﬃﬃﬃﬃﬃ ﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃﬃ
g c ¼ jv  wj ωc = 2vwjv  wj. We note that the same softening of the lower
polariton branch was observed in the case of the excitonic insulator coupled to light
using the Peierls substitution47 and is absent when all momentum k are taken into
account.

Data availability
Data are available upon reasonable request from the authors.

Code availability
All numerical codes in this paper are available upon reasonable request to the authors.

Received: 23 May 2022; Accepted: 19 October 2022;

References
1.

Basov, D. N., Averitt, R. D. & Hsieh, D. Towards properties on demand in
quantum materials. Nat. Mater. 16, 1077–1088 (2017).
2. Disa, A. S., Nova, T. F. & Cavalleri, A. Engineering crystal structures with
light. Nat. Phys. 17, 1087–1092 (2021).
3. Ruggenthaler, M., Tancogne-Dejean, N., Flick, J., Appel, H. & Rubio, A. From
a quantum-electrodynamical light–matter description to novel spectroscopies.
Nat. Rev. Chem. 2, 0118 (2018).
4. Schlawin, F., Kennes, D. M. & Sentef, M. A. Cavity quantum materials. arXiv
https://doi.org/10.48550/arXiv.2112.15018 (2021).
5. Garcia-Vidal, F. J., Ciuti, C. & Ebbesen, T. W. Manipulating matter by strong
coupling to vacuum ﬁelds. Science 373, eabd0336 (2021).
6. Valmorra, F. et al. Vacuum-ﬁeld-induced thz transport gap in a carbon
nanotube quantum dot. Nat. Commun. 12, 5490 (2021).
7. Bloch, J., Cavalleri, A., Galitski, V., Hafezi, M. & Rubio, A. Strongly correlated
electron–photon systems. Nature 606, 41–48 (2022).
8. Hasan, M. Z. & Kane, C. L. Colloquium: topological insulators. Rev. Modern
Phys. 82, 3045 (2010).
9. Qi, X.-L. & Zhang, S.-C. Topological insulators and superconductors. Rev.
Modern Phys. 83, 1057 (2011).
10. Oka, T. & Aoki, H. Photovoltaic Hall effect in graphene. Phys. Rev. B 79,
081406 (2009).

8

11. Lindner, N. H., Refael, G. & Galitski, V. Floquet topological insulator in
semiconductor quantum wells. Nat. Phys. 7, 490–495 (2011).
12. Wang, Y. H., Steinberg, H., Jarillo-Herrero, P. & Gedik, N. Observation of
Floquet-Bloch states on the surface of a topological insulator. Science 342,
453–457 (2013).
13. McIver, J. W. et al. Light-induced anomalous Hall effect in graphene. Nat.
Phys. 16, 38–41 (2020).
14. Cooper, N. R., Dalibard, J. & Spielman, I. B. Topological bands for ultracold
atoms. Rev. Mod. Phys. 91, 015005 (2019).
15. Karzig, T., Bardyn, C.-E., Lindner, N. H. & Refael, G. Topological polaritons.
Phys. Rev. X 5, 031001 (2015).
16. Ohm, C. & Hassler, F. Microwave readout of majorana qubits. Phys. Rev. B 91,
085406 (2015).
17. Trif, M. & Tserkovnyak, Y. Resonantly tunable majorana polariton in a
microwave cavity. Phys. Rev. Lett. 109, 257002 (2012).
18. Contamin, L. C., Delbecq, M. R., Douçot, B., Cottet, A. & Kontos, T. Hybrid
light-matter networks of majorana zero modes. npj Quant. Inform. 7, 171
(2021).
19. Méndez-Córdoba, F. P. M. et al. Rényi entropy singularities as signatures of
topological criticality in coupled photon-fermion systems. Phys. Rev. Res. 2,
043264 (2020).
20. Hübener, H. et al. Engineering quantum materials with chiral optical cavities.
Nat. Mater. 20, 438–442 (2021).
21. Rokaj, V., Penz, M., Sentef, M. A., Ruggenthaler, M. & Rubio, A. Polaritonic
hofstadter butterﬂy and cavity control of the quantized hall conductance.
Phys. Rev. B 105, 205424 (2022).
22. Wang, X., Ronca, E. & Sentef, M. A. Cavity quantum electrodynamical chern
insulator: towards light-induced quantized anomalous Hall effect in graphene.
Phys. Rev. B 99, 235156 (2019).
23. Appugliese, F. et al. Breakdown of topological protection by cavity vacuum
ﬁelds in the integer quantum Hall effect. Science 375, 1030–1034 (2022).
24. Roux, K., Konishi, H., Helson, V. & Brantut, J.-P. Strongly correlated fermions
strongly coupled to light. Nat. Commun. 11, 2974 (2020).
25. Mivehvar, F., Ritsch, H. & Piazza, F. Superradiant topological peierls insulator
inside an optical cavity. Phys. Rev. Lett. 118, 073602 (2017).
26. Su, W., Schrieffer, J. & Heeger, A. J. Solitons in polyacetylene. Phys. Rev. Lett.
42, 1698 (1979).
27. Delplace, P., Ullmo, D. & Montambaux, G. Zak phase and the existence of
edge states in graphene. Phys. Rev. B 84, 195452 (2011).
28. Gómez-León, A. & Platero, G. Floquet-Bloch theory and topology in
periodically driven lattices. Phys. Rev. Lett. 110, 200403 (2013).
29. Dal Lago, V., Atala, M. & Foa Torres, L. E. F. Floquet topological transitions in
a driven one-dimensional topological insulator. Phys. Rev. A 92, 023624
(2015).
30. Goren, T., Plekhanov, K., Appas, F. & Le Hur, K. Topological Zak phase in
strongly coupled LC circuits. Phys. Rev. B 97, 041106 (2018).
31. Downing, C. A., Sturges, T. J., Weick, G., Stobińska, M. & Martín-Moreno, L.
Topological phases of polaritons in a cavity waveguide. Phys. Rev. Lett. 123,
217401 (2019).
32. Nie, W., Antezza, M., Liu, Y.-x & Nori, F. Dissipative topological phase
transition with strong system-environment coupling. Phys. Rev. Lett. 127,
250402 (2021).
33. Pérez-González, B., Gómez-León, Á. & Platero, G. Topology detection in
cavity QED. Phys. Chem. Chem. Phys. 24, 15860–15870 (2022).
34. Atala, M. et al. Direct measurement of the zak phase in topological bloch
bands. Nat. Phys. 9, 795–800 (2013).
35. Meier, E. J., An, F. A. & Gadway, B. Observation of the topological soliton
state in the su–schrieffer–heeger model. Nat. Commun. 7, 13986 (2016).
36. de Léséleuc, S. et al. Observation of a symmetry-protected topological phase of
interacting bosons with Rydberg atoms. Science 365, 775–780 (2019).
37. Rizzo, D. J. et al. Topological band engineering of graphene nanoribbons.
Nature 560, 204–208 (2018).
38. Gröning, O. et al. Engineering of robust topological quantum phases in
graphene nanoribbons. Nature 560, 209–213 (2018).
39. Ozawa, T. et al. Topological photonics. Rev. Mod. Phys. 91, 015006 (2019).
40. Solnyshkov, D. D. et al. Microcavity polaritons for topological photonics. Opt.
Mater. Express 11, 1119–1142 (2021).
41. Kim, E. et al. Quantum electrodynamics in a topological waveguide. Phys. Rev.
X 11, 011015 (2021).
42. Huber, S. D. Topological mechanics. Nature Physics 12, 621–623 (2016).
43. Li, J. et al. Electromagnetic coupling in tight-binding models for strongly
correlated light and matter. Phys. Rev. B 101, 205140 (2020).
44. Sentef, M. A., Li, J., Künzel, F. & Eckstein, M. Quantum to classical crossover
of Floquet engineering in correlated quantum systems. Phys. Rev. Res. 2,
033033 (2020).
45. Li, J. & Eckstein, M. Manipulating intertwined orders in solids with quantum
light. Phys. Rev. Lett. 125, 217402 (2020).

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

## PDF page 9

COMMUNICATIONS PHYSICS | https://doi.org/10.1038/s42005-022-01049-0

46. Guerci, D., Simon, P. & Mora, C. Superradiant phase transition in electronic
systems and emergent topological phases. Phys. Rev. Lett. 125, 257604 (2020).
47. Dmytruk, O. & Schiró, M. Gauge ﬁxing for strongly correlated electrons
coupled to quantum light. Phys. Rev. B 103, 075131 (2021).
48. Ciuti, C., Bastard, G. & Carusotto, I. Quantum vacuum properties of the
intersubband cavity polariton ﬁeld. Phys. Rev. B 72, 115303 (2005).
49. Frisk Kockum, A., Miranowicz, A., De Liberato, S., Savasta, S. & Nori, F.
Ultrastrong coupling between light and matter. Nat. Rev. Phys. 1, 19–40 (2019).
50. Pilar, P., De Bernardis, D. & Rabl, P. Thermodynamics of ultrastrongly
coupled light-matter systems. Quantum 4, 335 (2020).
51. Eckhardt, C. J. et al. Quantum ﬂoquet engineering with an exactly solvable
tight-binding chain in a cavity. Commun. Phys. 5, 122 (2022).
52. Asbóth, J. K., Oroszlány, L. & Pályi, A. A short course on topological
insulators. Lect. Notes Phys. 919, 166 (2016).
53. Andolina, G., Pellegrino, F., Giovannetti, V., MacDonald, A. & Polini, M.
Cavity quantum electrodynamics of strongly correlated electron systems: A
no-go theorem for photon condensation. Phys. Rev. B 100, 121109 (R) (2019).
54. Amelio, I., Korosec, L., Carusotto, I. & Mazza, G. Optical dressing of the
electronic response of two-dimensional semiconductors in quantum and
classical descriptions of cavity electrodynamics. Phys. Rev. B 104, 235120 (2021).
55. Schiró, M. & Le Hur, K. Tunable hybrid quantum electrodynamics from
nonlinear electron transport. Phys. Rev. B 89, 195127 (2014).
56. Dmytruk, O., Trif, M., Mora, C. & Simon, P. Out-of-equilibrium quantum dot
coupled to a microwave cavity. Phys. Rev. B 93, 075425 (2016).
57. Cottet, A. et al. Cavity QED with hybrid nanocircuits: from atomic-like physics
to condensed matter phenomena. J. Phys. Condens. Matter 29, 433002 (2017).
58. Mazza, G. & Georges, A. Superradiant quantum materials. Phys. Rev. Lett.
122, 017401 (2019).
59. De Liberato, S. Light-matter decoupling in the deep strong coupling regime:
the breakdown of the Purcell effect. Phys. Rev. Lett.112, 016401 (2014).
60. Nataf, P., Champel, T., Blatter, G. & Basko, D. M. Rashba cavity QED: a route
towards the superradiant quantum phase transition. Phys. Rev. Lett. 123,
207402 (2019).
61. Andolina, G., Pellegrino, F., Giovannetti, V., MacDonald, A. & Polini, M.
Theory of photon condensation in a spatially varying electromagnetic ﬁeld.
Phys. Rev. B 102, 125137 (2020).
62. Lerose, A., Žunkovič, B., Marino, J., Gambassi, A. & Silva, A. Impact of
nonequilibrium ﬂuctuations on prethermal dynamical phase transitions in
long-range interacting spin chains. Phys. Rev. B 99, 045128 (2019).

ARTICLE

and from the European Research Council (ERC) under the European Union’s Horizon
2020 research and innovation programme (Grant agreement No. 101002955—
CONQUER).

Author contributions
O.D. carried out the numerical and analytical calculations. O.D. and M.S. analyzed the
data, discussed the results and wrote the manuscript.

Competing interests
The authors declare no competing interests.

Additional information
Supplementary information The online version contains supplementary material
available at https://doi.org/10.1038/s42005-022-01049-0.
Correspondence and requests for materials should be addressed to Olesia Dmytruk or
Marco Schirò.
Peer review information Communications Physics thanks Hang Xie and the other,
anonymous, reviewer(s) for their contribution to the peer review of this work. Peer
reviewer reports are available.
Reprints and permission information is available at http://www.nature.com/reprints
Publisher’s note Springer Nature remains neutral with regard to jurisdictional claims in
published maps and institutional afﬁliations.

Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing,
adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative
Commons license, and indicate if changes were made. The images or other third party
material in this article are included in the article’s Creative Commons license, unless
indicated otherwise in a credit line to the material. If material is not included in the
article’s Creative Commons license and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from
the copyright holder. To view a copy of this license, visit http://creativecommons.org/
licenses/by/4.0/.

Acknowledgements
This project has received funding from the European Union’s Horizon 2020 research and
innovation program under the Marie Skłodowska-Curie Grant Agreement No. 892800

© The Author(s) 2022

COMMUNICATIONS PHYSICS | (2022)5:271 | https://doi.org/10.1038/s42005-022-01049-0 | www.nature.com/commsphys

9
