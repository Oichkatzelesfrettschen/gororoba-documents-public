Source: https://arxiv.org/abs/2510.17473v1
PDF sha256: 236bc38cfb6987e30e0a35653ccde71120a0e9b3288a5a194fa1d5419f6119dc
License: http://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine-gated

# Transcription of crnogorcev_2025_dark_matters_icrc.pdf

Transcription of `crnogorcev_2025_dark_matters_icrc.pdf` in this directory, 23 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-23 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

arXiv:2510.17473v1 [astro-ph.HE] 20 Oct 2025

The Dark Matters at ICRC 2025

Milena Crnogorčević𝑎,∗
𝑎 Stockholm University and The Oskar Klein Centre for Cosmoparticle Physics,

Alba Nova, 10691 Stockholm, Sweden

E-mail: milena.crnogorcevic@fysik.su.se

The dark matter track at ICRC 2025 showed a field in transition. Direct detection has entered
the neutrino-floor era, with XENONnT and PandaX-4T now limited by Solar neutrinos. Indirect
searches have become truly multimessenger, combining 𝛾-rays, neutrinos, cosmic rays, and radio
data under unified likelihoods and shared systematics. Non-WIMP candidates—axions, sub-GeV
particles, primordial black holes, macroscopic relics—are becoming central. Across all fronts,
progress depends as much on new detectors as on the coherence of shared data, methods, and
analysis frameworks. Here, I distill the main experimental and conceptual shifts behind these
trends, noting how assumptions have evolved since ICRC 2023 and where the next decisive
advances are likely to come.

39th International Cosmic Ray Conference (ICRC2025)
15–24 July 2025
Geneva, Switzerland

∗ Speaker

© Copyright owned by the author(s) under the terms of the Creative Commons
Attribution-NonCommercial-NoDerivatives 4.0 International License (CC BY-NC-ND 4.0).

https://pos.sissa.it/

## PDF page 2

Milena Crnogorčević

DM Rapporteur ICRC 2025

1. Introduction
“What is essential is invisible to the eye,” said the Little Prince. At ICRC 2025, close to
eighty contributions proved that dark matter still fits this description perfectly. After four decades
of increasingly sophisticated searches—spanning underground laboratories, space- and groundbased telescopes, and neutrino observatories—the field has compiled a record of steadily tightening
constraints, but no detection1 .
The ICRC 2025 showcased this evolution through 78 dark matter contributions (61 talks, 14
posters, and 3 plenaries), spanning ninety orders of magnitude in mass: from ultralight axion-like
particles (ALPs), through sub-GeV and MeV-scale candidates, the electroweak weakly interacting
massive particles (WIMPs), heavy and superheavy relics, up to primordial black holes (PBHs)
and macroscopic objects. On the experimental front, searches employed a similarly diverse set of
messengers: 𝛾-rays, neutrinos, cosmic-ray antimatter, radio emission, and direct detection. The
breadth in theoretical models and detection techniques was matched by the analytical maturity:
multi-instrument joint likelihoods are becoming standard in dwarf-galaxy searches, multimessenger strategies increasingly define the state of the art in indirect detection, and machine learning
techniques now enhance background discrimination in direct detection experiments.

Figure 1: Distribution of dark matter ICRC 2025 contributions by dark matter particle mass. The bar height
represents the number of contributions (left 𝑦-axis), with the corresponding percentage of total contributions
shown on the right 𝑦-axis. Filled segments indicate talks and dashed segments represent posters.

Compared with ICRC 2023, four shifts stand out. First, direct detection has entered the
neutrino floor era. XENONnT and PandaX-4T now detect Solar neutrinos directly, confirming
that the dominant background for WIMP searches is no longer instrumental noise but irreducible
astrophysical signals. Second, indirect searches increasingly adopt joint multi-instrument likelihoods with consistent 𝐽-factor priors and shared systematics, integrating complementary datasets
1 For comprehensive reviews of dark matter see, e.g., [1–5]. Many more exist. From here on, I reference only ICRC

2025 proceedings due to space constraints.

2

## PDF page 3

Milena Crnogorčević

DM Rapporteur ICRC 2025

under unified statistical frameworks. The first comprehensive dwarf-galaxy analysis combined
Fermi-LAT, HAWC, H.E.S.S., MAGIC, and VERITAS data—spanning 100 MeV to beyond 10 TeV
in energy coverage—and improved sensitivity by factors of 2–3 relative to any single instrument.
Third, non-WIMP candidates have moved from periphery to center: for the first time in recent
ICRC history, the plenary program devoted more space to non-WIMP scenarios than to canonical WIMPs, reflecting the field’s strategic broadening towards alternative dark matter candidates.
Fourth, and perhaps most notably, ICRC 2025 revealed a structural convergence across traditionally separate communities. Astrophysical neutrino detectors—such as IceCube—are repurposed as
precision dark matter observatories, while direct detection experiments now reach the sensitivity
required to measure the Solar neutrinos. This convergence underscores an emerging reality: while
next-generation detectors remain essential for exploring new parameter space, near-term progress
increasingly depends on collaborative infrastructure—shared analysis tools, open data, open-source
software—that enables coherent integration of diverse datasets. Given present funding constraints
and uncertain timelines for next-generation experiments, maximizing scientific return from existing
data has become not merely advantageous but essential.
This rapporteur paper is inevitably subjective and deliberately selective. Rather than cataloging results experiment by experiment, I aim to underpin structural lessons that emerge when
contributions are viewed together. My aim is to capture the field’s status as of 2025: to identify
which assumptions have shifted since ICRC 2023, which methods now define the state of the art,
and where the next decade of searches is likely to be decisive. If the last decade was defined
by steady exclusion driven largely by increasing exposure and improved control of systematics,
the present moment marks a transition: dark matter searches now depend as much on coherent,
multi-instrument analysis as on continued advances in individual sensitivity.
To reflect these shifts, the organization of this paper therefore follows physics themes rather
than instrumental categories. Section 2 reviews the evolution of direct detection and its approach
to the neutrino floor. Section 3 surveys indirect searches organized by astrophysical target—dwarf
galaxies, the Galactic Center, Galactic halo, galaxy clusters, and others—rather than by messenger
or experiment, emphasizing the genuine multimessenger nature of current indirect searches. I
provide my concluding reflections in Sec. 4.

2. Direct Detection: The Neutrino-Floor Era
Direct detection has reached a defining milestone. For the first time, liquid-xenon timeprojection chambers (TPCs) have become sensitive to coherent elastic neutrino-nucleus scattering
(CE𝜈NS) from solar 8 B neutrinos—marking the transition from noise-limited to neutrino-limited
searches.
2.1 Reaching the Neutrino Floor
At ICRC 2025, XENONnT reported a 2.73𝜎 indication of CE𝜈NS events together with an
updated WIMP limit of 𝜎SI < 1.7 × 10−47 cm2 at a dark matter mass, 𝑚 𝜒 , of 30 GeV, improving
by a factor of 1.8 over SR0 [6]. Sub-𝜇Bq/kg electron-recoil backgrounds, achieved through radon
removal, place XENONnT operation at the 𝑝 𝑝-solar-neutrino background level. PandaX-4T
independently reported a 2.64𝜎 8 B CE𝜈NS indication in 1.54 t·yr exposure, along with competitive
3

## PDF page 4

Milena Crnogorčević

DM Rapporteur ICRC 2025

constraints on axion, ALP, and dark-photon scenarios [7]. Together, these results establish that,
in the multi-GeV–TeV range, xenon experiments are no longer limited by instrumental noise or
radiogenic contamination, but by the irreducible neutrino background itself.
With CE𝜈NS now observed—or at least strongly indicated—the field of direct detection faces
two strategic directions: (i) scaling exposure and refining background modeling to statistically
separate a potential WIMP signal from CE𝜈NS, and (ii) focusing on observables that CE𝜈NS cannot
mimic, such as Migdal-induced ionization or annual modulation. This twofold direction captured
the ICRC 2025 message from large noble-liquid experiments: they now operate in the neutrinofog regime, and future progress hinges on how we navigate—and ultimately extend sensitivity
below—that limit.

Figure 2: Four decades of progress in spin-independent WIMP searches. Markers show the
spin–independent WIMP–nucleon limits from HPGe crystals, cryogenic bolometers, bubble chambers, liquid
argon, and liquid xenon experiments for 𝑚 𝜒 = 50 GeV. The dashed line marks the onset of the neutrino fog
(∼1 expected CE𝜈NS event for multi-ton-year exposures). The two faint gray bands highlight the overall
improvement of about eight orders of magnitude in sensitivity—from early HPGe/bolometer results to
current liquid–xenon limits. Adapted from [8].

Parallel progress continues in the liquid-argon program. DarkSide-20k is now under construction at the INFN Gran Sasso National Laboratory as the next-generation dual-phase liquid-argon
TPC, with a 20 t fiducial (50 t total) target, underground argon for ultra-low backgrounds, and
custom cryogenic SiPM arrays for light readout [9]. Its triggerless data acquisition system and highrate architecture are designed to reach sensitivities at—or beyond—the neutrino floor by the end
of the decade. DEAP-3600, meanwhile, presented an extended 813-day dataset with an improved
background model, upgraded hardware for further suppression, and neural-network-based event
reconstruction. The collaboration also reported a new direct measurement of the 39 Ar half-life, in
mild tension with previous nuclear data [10].
4

## PDF page 5

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 3: Observation of solar 8 B neutrinos via CE𝜈NS in XENONnT. Left: projected distributions
of best-fit signal and background components combining both science runs (SR0 and SR1). Data points
(black) are shown with Poisson error bars; the CE𝜈NS signal (green) is stacked above accidental coincidences
(purple), electronic recoils (blue), and neutrons (yellow). Right: upper panel—68% (90%) measurement
of solar 8 B neutrino flux compared with SNO, XENON1T, and PandaX-4T (2023, see updated results in
[7]); lower panel—flux-weighted CE𝜈NS cross-section measured with XENONnT, alongside COHERENT
results using different targets. Adapted from [6].

2.2 Beyond Canonical WIMPs: Sub-GeV Dark Matter
Over the past decade, direct detection experiments have expanded beyond the multi-GeV WIMP
regime to include lighter, sub-GeV dark matter. If dark matter never reached thermal equilibrium
with the Standard Model plasma, keV–GeV masses arise naturally, producing recoil energies that
are well below the sensitivity of traditional noble-liquid detectors. Probing this regime therefore
requires a fundamental shift in detector technology—from measuring nuclear recoils of tens of
keV to detecting ionization and phonon signals at the few-eV level. This shift has driven the
development of low-threshold solid-state detectors capable of counting single charge carriers, and
cryogenic crystals that measure phonons from sub-keV energy deposits. Progress in this direction
was evident at ICRC 2025, where several experiments reported stable low-threshold operation and
presented first results on sub-GeV dark matter searches.
Solid-state and cryogenic detectors. SENSEI uses silicon skipper charge-coupled devices (CCDs)
5

## PDF page 6

Milena Crnogorčević

DM Rapporteur ICRC 2025

with multiple non-destructive readouts per pixel, achieving sub-electron noise and single-electron
sensitivity [11]. The experiment targets dark-matter–electron scattering, dominant for sub-GeV
masses where nuclear recoils are suppressed. At ICRC 2025, the collaboration reported a singleelectron rate of (1.4 ± 0.1) × 10−5 e− pix−1 day−1 from the second science run—the lowest
ever recorded in silicon or any NIR/UV photodetector—and presented the first dedicated dailymodulation search using data from the MINOS tunnel at Fermilab. These results extend SENSEI’s
sensitivity to dark matter masses of 0.5–3 MeV for direct scattering and 1–3 eV for absorption
channels, constraining hidden-photon and ultralight-mediator models. A third science run with a
new cryocooler and improved background control is underway. SuperCDMS employs cryogenic
silicon and germanium detectors instrumented with transition-edge sensors to measure phonon and
ionization signals with sub-50-eV resolution. At ICRC 2025, the collaboration reported successful
commissioning of a detector tower at the Cryogenic Underground Test Facility (CUTE), demonstrating in-situ calibration and stable operation with measured baseline resolutions of 70–80 eV
for germanium targets [12]. These results validate the performance needed for the forthcoming
SNOLAB installation, which will deploy 24 detectors (30 kg total) combining high-voltage phonon
and phonon-charge technologies. Commissioning is scheduled for late 2025, with the first science
run expected in 2026, targeting dark matter masses below 10 GeV and dark-photon absorption in
the 100 eV–MeV range.
Gaseous detectors. Complementary progress comes from spherical proportional counters operated
with light noble gases. NEWS-G uses neon and helium targets to probe nuclear recoils from 0.1–
1 GeV dark matter, achieving world-leading spin-dependent proton limits in this mass range [13]. At
ICRC 2025, the collaboration presented results from He+CH4 data, reported ongoing neon analyses
using MCMC techniques, and discussed developments toward the 3 m DarkSPHERE prototype,
designed to scale target mass and extend reach to lower cross sections.
Scintillator detectors. The SABRE South experiment, now under installation at the Stawell
Underground Physics Laboratory (SUPL) in Australia, is part of the broader SABRE program,
which also includes a Northern detector at Gran Sasso in Italy, though the two installations differ
in shielding approach and deployment schedule [14]. SABRE South represents the first Southern
Hemisphere test of the long-standing DAMA/LIBRA annual-modulation claim. It employs ultrapure NaI(Tl) crystals with nat K concentrations of 4.3 ppb—three to eight times lower than other NaI
experiments—and an active liquid-scintillator veto that suppresses the 40 K background by an order
of magnitude, reaching 0.72 cpd/kg/keVee. Located 1025 m underground at SUPL, the experiment
is designed to disentangle seasonal systematics from a potential dark matter modulation. Assembly
is ongoing, with commissioning planned for early 2026; discovery or exclusion of a DAMA-like
signal is expected within roughly two years of operation.
These developments establish low-threshold direct detection as an integral part of the dark
matter landscape, extending sensitivity to previously inaccessible sub-GeV masses.
2.3 Shared Infrastructure for Neutrino and Dark Matter Searches
Astrophysical neutrino detectors are being increasingly leveraged as direct dark matter observatories
[15]. At ICRC 2025, IceCube presented the first dedicated sensitivity study to sub-GeV dark matter
produced via cosmic-ray upscattering, demonstrating that large-volume neutrino telescopes can
probe parameter space complementary to underground detectors [16]. In parallel, the RES-NOVA
6

## PDF page 7

Milena Crnogorčević

DM Rapporteur ICRC 2025

collaboration reported new projections for its cryogenic PbWO4 detector, originally designed for
supernova neutrinos, showing competitive reach for both spin-independent and spin-dependent
dark matter interactions [17]. The plenary talks further illustrated this cross-field trend: FUNK is
repurposing an Auger mirror for hidden-photon searches [18], while plans are underway to establish
a dark matter laboratory within the Bedretto underground facility—primarily built for earthquake
research [8].

Figure 4: Complementary sensitivity of neutrino detectors to dark matter. Left: IceCube 90% C.L. sensitivity to cosmic-ray upscattered sub-GeV dark matter for pseudoscalar mediators, showing complementarity
with Super-Kamiokande [16]. Right: Projected RES-NOVA sensitivity to spin-independent DM-nucleon
scattering, compared with direct detection and neutrino limits [17].

These developments exemplify a broader structural convergence: the large volume of detectors optimized for neutrino searches can be repurposed for dark matter discovery, and vice versa.
This, in my opinion, reflects more than a technical overlap—it is a pragmatic response to a tightening
funding landscape, where sustained progress increasingly depends on shared infrastructure, joint
analyses, and creative use of existing facilities. While new experiments remain essential to reach
unexplored regimes, I believe the next few years may push us to use existing instruments more
effectively—to extract new science not by expanding scale, but by expanding scope. Amid funding
pressures and shifting priorities, this evolution feels not just pragmatic but necessary.

3. Indirect Detection: The Multimessenger Era
At ICRC 2025, nearly every astrophysical target class was examined across multiple messengers—
𝛾-rays, neutrinos, cosmic-ray antimatter, and radio emission—turning what were once singlechannel searches into genuine multimessenger studies. Reflecting this shift, I organize this
section by source class rather than detection technique: dwarf galaxies, the Galactic Center, galaxy
clusters, the Sun, and others, each now constrained through complementary observations across
multiple messengers. Before turning to specific sources, however, I first highlight the observatories
present at ICRC 2025, which illustrate the large part of the current experimental landscape of
7

## PDF page 8

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 5: 𝛾-ray coverage of current and upcoming observatories presented at ICRC 2025. Present
instruments (blue) and planned facilities (magenta) together provide continuous sensitivity from tens of MeV
to multi-PeV energies. Notably, no next-generation space-based 𝛾-ray mission from ESA or NASA is
currently planned to succeed Fermi, now operating beyond its expected lifetime, likely leaving a gap in
MeV–GeV coverage in the coming decade.

indirect detection. Figures 5 and 6 summarize the 𝛾-ray and neutrino facilities discussed at the
conference, indicating their approximate energy coverage and complementarity.
3.1 The Sun
Dark matter gravitationally captured by the Sun through elastic scattering may accumulate and
annihilate in its core, producing high-energy neutrinos that escape to Earth. This channel probes
the spin-dependent WIMP–proton cross section and complements direct detection for masses above
∼10 GeV.
At ICRC 2025, IceCube presented its most sensitive all-flavor Solar dark matter search to date,
based on ten years of data and leveraging event selections originally optimized using convolutional
neural networks [19]. The analysis covers WIMP masses from 20 GeV to 10 TeV across multiple
annihilation channels, achieving world-leading sensitivity over this entire mass range for most
channels considered. The limits reach approximately 10−41 to 10−42 cm2 for spin-dependent cross
sections at 100 GeV—roughly 40 times more stringent than previous IceCube results, particularly
benefiting from full treatment of electroweak corrections at high masses. The forthcoming IceCube
Upgrade aims to extend this reach to lower masses through improved angular resolution and energy
thresholds down to 1–500 GeV.
ANTARES reported final limits using its complete 2007–2022 dataset, concluding more than
a decade of operation as the first underwater neutrino telescope [20]. The analysis uses three independent reconstruction techniques—among them a newly developed machine-learning algorithm
8

## PDF page 9

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 6: Neutrino observatories in the GeV–PeV regime. Current detectors (blue) and future extensions
(magenta) provide complementary sky coverage and energy reach.

optimized for low-energy events—and included all neutrino flavors. The results are consistent
with a null signal and achieve competitive sensitivity above 100 GeV, surpassing direct detection
constraints in the spin-dependent regime over this mass range. Its successor, the KM3NeT/ORCA
array, now under deployment, is expected to continue this program with improved low-energy
sensitivity and full flavor reconstruction, directly expanding upon ANTARES’s legacy.
A persistent limitation in these searches arises from solar atmospheric neutrinos—a flux
produced by cosmic-ray interactions in the upper solar atmosphere—which sets a natural sensitivity floor. IceCube’s TeV-scale sensitivity is already approaching this boundary, implying that
next-generation detectors such as IceCube-Gen2 and KM3NeT will soon probe this irreducible
background directly.
At 𝛾-ray energies, complementary searches target secluded dark matter scenarios, where annihilation produces long-lived mediators that decay outside the Solar surface. In these models,
the same process generating neutrinos within the Sun yields 𝛾-rays just beyond it—linking the two
messengers as probes of a common underlying physical mechanism. The Southern Wide-field
Gamma-ray Observatory (SWGO) presented updated projections using its latest instrument response functions [21], indicating sensitivity to spin-dependent cross sections down to approximately
10−46 cm2 for masses below 5 TeV—an order of magnitude improvement over current indirect limits.
3.2 The Galactic Center
The Galactic Center (GC) remains one of the most promising yet challenging regions for indirect
dark matter searches. Its high dark matter density enhances the expected annihilation signal, but
the region is also dominated by complex astrophysical foregrounds, including the diffuse emission
from cosmic-ray interactions, dense molecular gas, and unresolved sources. The long-debated GeV
9

## PDF page 10

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 7: DAMPE analysis of the GCE. Top: Integrated flux map of the GC region above 2 GeV (left)
and the corresponding spectral energy distribution (right). DAMPE reproduces the spectral shape and
normalization previously observed by Fermi-LAT, providing the first independent confirmation of the excess
in 𝛾-rays. Bottom: Likelihood profile for the generalized NFW (gNFW) inner slope 𝛾 (left) and preferred
dark matter parameters for the 𝜒 𝜒 → 𝑏 𝑏¯ channel (right), derived from 8.5 years of DAMPE data. DAMPE
countours agree with previous Fermi-LAT results (Cholis et al. 2022, Calore et al. 2015), yielding consistent
slopes (𝛾 ∼ 1.2) and cross sections (⟨𝜎𝑣⟩ ∼ 1.4 × 10−26 cm3 s−1 ). The slightly lower preferred 𝑚 𝜒 ∼ 35 GeV
compared to Fermi-LAT likely reflects DAMPE’s limited sensitivity at higher energies, which can make it
less constraining toward lower-mass dark matter models. Adapted from [27].

Galactic Center Excess (GCE) observed by Fermi-LAT has been largely reinterpreted in terms of
millisecond pulsars, yet the persistence of model-dependent residuals continues to motivate a broad
experimental effort across messengers and energy ranges.
At ICRC 2025, the first Large-Sized Telescope (LST-1) of the Cherenkov Telescope Array
Observatory (CTAO) presented updated sensitivity studies for 𝛾-ray line searches toward the GC
[22]. The analysis targets annihilation channels producing monochromatic photons (𝜒 𝜒 → 𝛾𝛾
and 𝜒 𝜒 → 𝛾𝑍) in the 1–100 TeV range. Large zenith angle observations enhance the effective
area while preserving low thresholds, enabling sensitivity improvements over previous MAGIC
and H.E.S.S. results in the multi-TeV regime. The LST-1 also emphasized a detailed treatment of
systematics in background modeling—an important step toward realizing the full CTAO potential
for spectral line searches once the full array is operational.
Complementary results now come from neutrino observatories probing the same region. Ice10

## PDF page 11

Milena Crnogorčević

DM Rapporteur ICRC 2025

Cube, using DeepCore and forthcoming Upgrade extensions, presented a dedicated GC search
across the GeV–TeV range [23]. Although neutrino channels remain less sensitive than 𝛾-rays
for leptonic annihilation modes, they offer a clean probe of hadronic final states and nonstandard
topologies. The analysis of 9.3 years of DeepCore data set world-leading limits on neutrino-line
signals and provided the first projections for the IceCube Upgrade, which is expected to improve
sensitivity below 20 GeV by an order of magnitude.
The KM3NeT collaboration expanded this program to the opposite hemisphere, combining
ORCA (optimized for 1–100 GeV) and ARCA (extending to 10 PeV) [24]. Their joint likelihood
framework—tested on configurations from 6 to 230 detector lines—delivers nearly continuous sky
coverage of the inner Galaxy. Even with partial configurations, KM3NeT reaches competitive limits
above 10 TeV and demonstrates that multi-detector synergy is rapidly becoming standard practice
in neutrino-based DM searches.
Looking ahead, the Hyper-Kamiokande collaboration, presenting in the neutrino track,
outlined prospects for detecting the astrophysical neutrino flux and for dark matter annihilation
searches toward the GC, showing potential sensitivity to the 𝜒 𝜒 → 𝜈 𝜈¯ channel in the 10–104 GeV
range and complementarity with IceCube and KM3NeT [25].
Finally, a distinctive and creative approach linked cosmic-ray ionization in the Central Molecular Zone (CMZ) to potential MeV-scale dark matter interactions [26]. This analysis connected
an otherwise unexplained astrophysical anomaly—the elevated ionization rate of the CMZ—with
low-mass dark matter capable of producing secondary electrons and positrons. Though highly
model-dependent, it exemplified the field’s growing willingness to explore noncanonical mass
regimes and multi-wavelength observables.
Outside the official dark matter track at ICRC 2025, yet nonetheless one of my favorite moments
of the conference came from DAMPE. Using 8.5 years of photon data, the collaboration presented
the first independent confirmation of the well-established Galactic Center Excess (GCE) in GeV
𝛾-rays (7.4𝜎 significance)—sixteen years after it was first observed with Fermi-LAT [27]. While
there is no doubt that the excess is genuine (Fermi’s result has been extensively scrutinized)—it is
deeply gratifying to see it re-emerge in data from an entirely independent instrument, with distinct
detection techniques and systematic uncertainties. The GCE remains well and alive, still awaiting
resolution.
3.3 The Galactic Halo
The Milky Way halo remains the most direct yet diffuse target for dark matter searches. While
its total mass distribution sets the scale for all Galactic analyses, its substructure, density profile,
and annihilation morphology shape both theoretical predictions and instrumental strategies. At
ICRC 2025, contributions spanned from high-resolution simulations of halo substructure to deep
observational searches for spectral features and antimatter signatures, underscoring the halo’s role
as a testable component of the Galactic dark matter distribution.
High resolution 𝑁-body simulations resolved subhalo tidal tracks with particle counts exceeding 107 , providing a detailed picture of how gravitational stripping shapes the surviving substructure
population [28]. Complementary magneto-hydrodynamic simulations that include gas and magnetic
feedback showed that baryonic processes can significantly suppress low-mass subhalos, leading to
11

## PDF page 12

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 8: Left: Predicted fluxes of antiprotons and antideuterons from dark matter annihilation compared
with astrophysical backgrounds and existing measurements. The GAPS long-duration balloon flights will
probe the low-energy regime (𝐸 kin ≲ 0.25 GeV/n), where astrophysical backgrounds sharply decline, enabling
nearly background-free searches for antideuterons. Right: Projected GAPS sensitivity to antihelium-3 after
three long-duration flights (red band, 95% CL), compared with expected fluxes from representative dark
matter models and astrophysical backgrounds. Adapted from [34].

more accurate predictions for the number and brightness of dark satellites potentially observable
with Fermi-LAT [29].
At smaller scales, late-time annihilations in oscillating asymmetric dark matter (OADM)
models were explored as a possible dynamical solution to the core–cusp problem [30]. In this
scenario, a small Majorana mass term reactivates particle-antiparticle annihilations during galaxy
evolution, gradually transforming cuspy NFW profiles into constant-density cores. Fits to dwarfgalaxy rotation curves indicate that this mechanism can reproduce observed density cores for
sub-GeV particle masses and cross sections of order 𝜎/𝑚 𝜒 ∼ 0.06 cm2 ,g−1 , providing a particle
physics alternative to purely baryonic feedback. From an observational standpoint, spectral searches
for monochromatic and box-like 𝛾-ray features found no evidence of dark matter annihilation.
DAMPE’s nine-year dataset and the updated 15.5-year Fermi-LAT analysis both reported null
results, with the latter improving previous limits by up to two orders of magnitude through refined
background modeling below 10 GeV [31, 32].
The search for cosmic antimatter stood out at ICRC 2025 as the part of indirect detection most
clearly oriented towards future experiments. These searches target low-energy cosmic antinuclei—
antiprotons, antideuterons, and antihelium—where, especially for the latter two, astrophysical
backgrounds drop sharply below a few hundred MeV per nucleon, making even a handful of
detected events potentially decisive. Three complementary efforts defined the state of the field:
GAPS, GRAMS, and PLASTICAMI.
The General Antiparticle Spectrometer (GAPS) collaboration presented results from its fullsystem ground campaign in Antarctica [33, 34]. GAPS employs a novel exotic-atom technique, in
which low-energy antinuclei are captured by lithium-drifted silicon detectors, de-exciting through
x-ray emission before annihilating into pions. This dual signature provides excellent particle
identification and background suppression, enabling sensitivity to antideuterons and antihelium at
12

## PDF page 13

Milena Crnogorčević

DM Rapporteur ICRC 2025

fluxes several orders of magnitude below those accessible to magnetic spectrometers. Although
seven consecutive launch attempts were weather-prevented, the payload remains integrated and
flight-ready at McMurdo Station, with its first long-duration Antarctic flight now expected in the
2025/26 season. Once launched, GAPS will extend current limits by one to two orders of magnitude,
probing fluxes predicted for ∼70 GeV WIMP annihilation and measuring the antiproton spectrum
at kinetic energies below 0.25 GeV/nucleon.
The GRAMS (Gamma-Ray and AntiMatter Survey) project advanced a complementary
concept based on a dual-purpose liquid-argon TPC [35]. GRAMS aims to bridge the long-standing
”MeV gap“ in 𝛾-ray astronomy while simultaneously searching for antideuterons and antihelium.
A successful engineering flight and J-PARC beam test demonstrated its detector performance, and
a NASA-funded prototype mission (pGRAMS) is now scheduled for early 2026. With a modular
design scalable to space deployment, GRAMS could ultimately connect MeV 𝛾-ray observations
and low-energy cosmic-ray antimatter measurements within a single instrument class.
Finally, PLASTICAMI proposed a segmented plastic-scintillator tracker optimized for identifying the unique ”two-step“ annihilation topology of stopped antideuterons in hydrogen-rich
media [36]. By timing the delayed annihilation of the surviving antinucleon following the first
annihilation, PLASTICAMI can isolate the antideuteron signature against background. Simulations show that two long-duration balloon flights could reach flux sensitivities of Φ𝑑¯ ∼ 2 ×
10−6 (m2 sr s GeV/n)−1 between 100–600 MeV/n, approaching the discovery region for several dark
matter annihilation models.
3.4 Dwarf Spheroidal Galaxies
Dwarf spheroidal galaxies (dSphs) remain benchmark targets for indirect dark matter searches.
Their extreme mass-to-light ratios, combined with minimal astrophysical backgrounds, and kinematically well-constrained dark matter distributions, make them exceptionally well-suited for testing
different dark matter models. Unlike the GC, where baryonic emission complicates interpretation,
dSphs offer a more controlled environment where systematic uncertainties are dominated by the
astrophysical 𝐽-factor rather than foreground contamination or source confusion.
A major milestone in the field was the completion of the first multi-instrument joint-likelihood
analysis, combining data from Fermi-LAT, HAWC, H.E.S.S., MAGIC, and VERITAS across
twenty dwarf galaxies [37]. First presented at ICRC 2019 and finalized this year, this effort
joined five independent likelihood datasets—spanning from 100 MeV to beyond 10 TeV—under
consistent statistical and astrophysical assumptions. The analysis explicitly combined systematics
and instrument response functions, resulting in continuous coverage across eight decades in energy.
Sensitivity is dominated by Fermi-LAT at low masses and by the Cherenkov telescopes at higher
energies, where the joint framework improves limits by factors of two to three relative to any
single instrument. For a 2 TeV WIMP annihilating into 𝜏 + 𝜏 − , the combined limit reaches ⟨𝜎𝑣⟩ ≲
3 × 10−25 cm3 s−1 . More broadly, however, this result sets a precedent for cross-facility analyses,
providing a methodological foundation for future joint searches that may also include neutrino
observatories.
Complementing this, VERITAS presented their results for the ultra-faint galaxy Ursa Major III in combination with Fermi-LAT data [38]. Rather than extending exposure or joining
likelihoods, the analysis focused on a single, extreme dark matter system with a high 𝐽-factor,
13

## PDF page 14

Milena Crnogorčević

DM Rapporteur ICRC 2025

Figure 9: Two complementary paths in dwarf-galaxy dark matter searches. Left: The joint Fermi-LAT,
HAWC, H.E.S.S., MAGIC, and VERITAS analysis [37] combines five likelihoods across eight decades in
energy, exemplifying the integration of instruments and systematics into a unified statistical framework.
Right: Fermi-LAT limits for the ultra-faint galaxy Ursa Major III [38, 39], illustrating the complementary
precision approach that targets individual, extreme systems with high inferred dark matter densities.

exploring both canonical WIMP channels and specific electroweak scenarios such as wino and
quintuplet dark matter. Ultra-faint dwarfs like Ursa Major III are becoming increasingly common
and better characterized through facilities such as Rubin LSST, enabling targeted follow-up of individual systems with high inferred dark matter densities. Although the confirmation and dynamical
characterization of such faint systems remain challenging—and some may ultimately prove less
dark matter dominated than currently assumed—their discovery continues to expand the range of
viable targets for indirect searches, allowing us to turn towards precision studies of the faintest and
most dark matter dominated systems.
In the radio domain, MeerKAT presented the deepest interferometric dark matter search in a
dwarf galaxy to date [40], targeting Reticulum II in the UHF band. The study detected no significant
emission but achieved sensitivities of 9–14 𝜇Jy/beam, improving on previous ATCA constraints by
up to an order of magnitude. For WIMP masses between 20–100 GeV annihilating into 𝑏 ¯𝑏, the
analysis excluded cross-sections above ∼10−26 cm3 s−1 . These results represent the most stringent
radio constraints obtained for a dwarf galaxy, demonstrating MeerKAT’s capability as a precision
instrument for indirect dark matter searches. The forthcoming Square Kilometre Array (SKA) is
expected to extend this reach by one to two orders of magnitude, potentially probing the thermal
relic scale in the radio band.
At the highest energies, IceCube presented its first complete dSph analysis using the muontrack channel [41]. Based on 10.4 years of data toward fifteen northern-sky dwarfs, the study
distinguishes neutrino-flavor signatures from dark-matter-induced fluxes and achieves competitive
sensitivity above 100 TeV. The stacking approach and flavor-resolved modeling make this the first
neutrino analysis of its kind, demonstrating clear complementarity with 𝛾-ray observatories in
probing heavy dark matter scenarios.
Theoretical modeling efforts presented at ICRC 2025 explored prompt and secondary emission in transition dwarf galaxies—systems that have recently ceased star formation—to distinguish
14

## PDF page 15

Milena Crnogorčević

DM Rapporteur ICRC 2025

dark-matter–induced signals from astrophysical backgrounds [42]. Using CRPropa-based simulations, these studies showed that synchrotron and inverse-Compton components imprint distinct
spatial and spectral morphologies, underscoring the diagnostic power of multi-wavelength structure
in future searches.
Taken together, these results establish dSphs as genuinely multimessenger dark matter targets. The joint likelihood 𝛾-ray framework now combines space- and ground-based observations
across eight decades in energy, while radio and neutrino analyses extend sensitivity to complementary regimes, probing secondary emission and heavy-mass scenarios inaccessible to photons
alone. At the same time, the field is branching along two complementary paths: one toward
integration, where coordinated multi-instrument analyses redefine the statistical frontier; and one
toward precision, where ultra-faint dwarfs such as Ursa Major III invite deep, system-specific consideration. As new systems are discovered and their dark matter content better constrained through
deep spectroscopic and photometric surveys, the population of dwarf galaxies continues to expand
both in number and in diversity, emerging as one of the most promising targets for testing dark
matter interactions in the coming decade.
3.5 Extragalactic Sources
Beyond the Milky Way, galaxy clusters and active galactic nuclei (AGN) provide complementary laboratories for dark matter searches. Their large gravitational potentials, extended dark matter
halos, and (often) well-characterized intracluster media allow indirect searches to test both annihilation and decay scenarios over large spatial scales. At ICRC 2025, extragalactic searches reflected
two trends: (i) refined analyses of nearby clusters as extended sources of potential annihilation
signatures, and (ii) a broad diversification of probes beyond the canonical WIMP, connecting 𝛾-ray,
radio, and multimessenger signatures across different mass regimes.
Galaxy clusters. At radio wavelengths, MeerKAT has established a new benchmark for indirect
dark matter searches through the Galaxy Cluster Legacy Survey [43]. The program analyzed 115
clusters using an image-domain pipeline capable of isolating diffuse synchrotron emission from
compact-source contamination. The resulting upper limits on leptonic annihilation channels are
amongst the most stringent to date, showing the power of radio interferometry as a complementary probe to 𝛾-ray observations. Furthermore, this work introduced a computationally efficient
alternative to traditional visibility-based analyses through injecting dark matter templates directly
into processed images. The method reduces processing time from 82 hours to roughly 3 minutes
per field on a single node—orders of magnitude faster—resolving a critical scalability challenge
for next-generation surveys such as the SKA. Complementary work in the 𝛾-ray track included a
dedicated H.E.S.S. search for dark matter signatures in the Virgo Cluster, based on 200 hours of
observations and modeling both annihilation and decay channels with substructure effects [44].
A separate Fermi–LAT analysis reported a tentative 43 GeV 𝛾-ray line feature in a stacked study
of nearby clusters, including Virgo, Fornax, and Ophiuchus [45]. The signal reaches a post-trial
significance of 3.7𝜎 for a 13-cluster sample, rising to 4.3𝜎 when restricted to the three highest𝐽 systems. Multiple consistency checks—testing the line’s monochromatic width, spatial extent
within the virial radius, and Earth-limb control regions were performed, but instrumental origins
remain under investigation. This feature appears absent in the inner Galaxy, creating tension with
standard annihilation interpretations and suggesting either more complex dark sector dynamics or
15

## PDF page 16

Milena Crnogorčević

DM Rapporteur ICRC 2025

unaccounted-for systematics. Further instrumentation effect analysis and/or verification by CTAO
or HAWC will be essential before any dark matter interpretation can be sustained.
Jetted Sources and ALP Searches. ICRC 2025 featured a strong focus on non-WIMP scenarios, particularly ALPs and their imprints in extragalactic environments. HAWC presented
two complementary studies: one analyzing TeV blazars (VER J0521+211, 1ES 0229+200, and
PG 1553+113) with updated data, extending existing constraints in the neV-scale ALP parameter
space [46]; and another based on seven years of observations of M87, employing a Monte Carlo
likelihood framework that explicitly circumvents Wilks’ theorem assumptions [47]. Both analyses
yield new limits on the photon-ALP coupling strength and illustrate the growing methodological
maturity of astrophysical ALP searches. Complementary simulations for the upcoming SWGO
indicate that five years of observations of Centaurus A could further refine ALP constraints by
detecting—or excluding—spectral distortions induced by photon–ALP mixing [48].
A separate effort modeled the interplay between dark matter and cosmic rays in relativistic jets,
introducing a multi-zone framework that accounts for jet geometry and kinematics when constraining cosmic-ray–dark-matter (CR–DM) elastic and inelastic interactions [49]. Using Markarian 421
as a representative case, the study found that jet dynamics significantly affect expected signatures,
underscoring the need for physically consistent modeling of such environments. At higher energies,
theoretical work examined the impact of photophilic ALPs in 𝛾-ray bursts (GRBs), showing that
MeV–GeV-mass ALPs could suppress GRB emission—an effect we do not observe—thereby imposing strong limits on heavy ALPs coupled to photons [50]. Finally, models connecting neutrino
production to dark matter interactions in the dense spikes surrounding supermassive black holes
explored how such regions could contribute to the observed neutrino fluxes from active galaxies
like NGC 1068, bridging multimessenger observations across neutrinos and 𝛾 rays [51].
Rather than adding more upper limits, the extragalactic program at ICRC 2025 broadened
what a dark matter search can be. Galaxy clusters showcased advances in computational pipelines
and synchrotron modeling, blazars and radio galaxies are studied as sites for ALP–photon mixing,
and jets and GRB fireballs emerged as probes of dark sector interactions across the lightest and
heaviest mass scales. In preparation for upcoming facilities such as CTAO, SWGO, and SKA, this
integration of astrophysical data handling and dark matter phenomenology promises a more direct
translation of observational signatures into particle physics insights in the coming decade.
3.6 Large Scale Structure
Large Scale Structure (LSS) entered the dark matter program at ICRC 2025 less as a background
assumption and more as a source of testable constraints. Across several contributions, cosmological
modeling and early-Universe dynamics were directly linked to the interpretation of astrophysical
searches.
Primordial black holes (PBHs) remain the most direct bridge between cosmology and astroparticle
physics. The LHAASO collaboration conducted an all-sky search for individual PBH burst events
using 3.4 years of WCDA data, finding no significant excess and setting a new upper limit on the
local burst rate density of 𝜌PBH < 181 pc−3 , yr −1 at 99% C.L., the most stringent bound to date
[52]. While still consistent with purely cosmological populations, these limits begin to challenge
models in which PBHs constitute a significant fraction of the dark matter density. Complementary
constraints came from charged-particle channels. Analyses using updated AMS-02 antiproton data
16

## PDF page 17

Milena Crnogorčević

DM Rapporteur ICRC 2025

and refined Galactic propagation models revisited antinuclei production from PBH evaporation
[53]. Incorporating lognormal PBH mass distributions and improved coalescence modeling for
antideuteron formation, these studies showed that cosmic-ray data already exclude large portions
of PBH parameter space, comparable to current 𝛾-ray limits. In effect, the cosmic-ray background
itself now functions as a probe of early-Universe structure formation.
Another study modeled the cosmic background from optical to x-ray energies, incorporating
ALP decays on LSS–averaged extragalactic background light templates [54]. By comparing with
recent cosmic-background measurements—including the New Horizons sky-brightness excess—
the study derives improved limits on the ALP–photon coupling, reaching the QCD axion band.
At smaller scales, hydrodynamical simulations such as EAGLE are directly informing indirect
searches. Analyses combining LSS-based halo realizations with dark matter spike models around
intermediate mass black holes showed how realistic substructure modifies the expected 𝛾-ray flux
in H.E.S.S. data [55, 56]. No excess consistent with annihilation was found, but the resulting limits
are amongst the strongest obtained for intermediate-mass systems and provide an astrophysically
grounded bridge between cosmological simulations and indirect 𝛾-ray searches.
Finally, IceCube extended these cosmological connections to relic particle searches, presenting
a twelve-year analysis of sub-relativistic magnetic monopoles that improves previous flux limits by
up to three orders of magnitude [57].

3.7 Macroscopic Dark Matter and Nuclearites
In this subsection, I depart slightly from the source-based organization used elsewhere and turn
to dark matter candidates in the macroscopic regime. Dark matter may also exist in composite rather
than elementary form, appearing as dense, massive objects that interact primarily through geometry
and gravity. Such candidates—including strange-quark matter nuggets, nuclearites, and other
compact macroscopic dark objects—span mass range from 1018 to 1032 GeV and could produce
meteor-like luminous tracks or measurable acoustic signatures as they traverse the atmosphere or
solid media.
The DIMS (Dark Matter and Interstellar Meteoroid Study) experiment employs a network
of high-sensitivity CMOS cameras at the Telescope Array site in Utah to identify slow, faint
luminous events consistent with nuclearite passage [58]. Over 450 hours of moonless observations
have been collected, yielding tens of thousands of meteor detections and establishing a framework
for distinguishing macroscopic dark matter candidates from conventional meteoroids through their
higher velocities, lower altitudes, and potential upward trajectories.
In space, the SQM-ISS detector [59]—approved for installation on the International Space
Station—combines scintillator and piezoelectric layers to detect both ionization and mechanical
energy deposition from slow, massive objects such as strange-quark matter, Q-balls, or PBHs.
Operating in a galactic-velocity regime (𝑣 ∼ 220 km s−1 ), the instrument aims to provide the first
orbital constraints on macroscopic compact dark matter, with projected sensitivities several orders
of magnitude beyond existing ground-based limits.
17

## PDF page 18

Milena Crnogorčević

DM Rapporteur ICRC 2025

4. Conclusions: The Dark Matters at ICRC 2025 (or, my 2¢)
We have reached a mature phase in dark matter searches2 . The field has moved beyond isolated
anomalies towards disciplined, reproducible, and statistically rigorous analyses. What began as
the WIMP paradigm has evolved into a broader framework encompassing axions, ultralight fields,
sub-GeV candidates, and macroscopic relics. These efforts are no longer parallel pursuits but parts
of a coordinated multimessenger program built on common analysis standards and shared data
infrastructure.
Key Developments
The neutrino floor is here. Direct detection experiments have reached the background set by Solar
and atmospheric neutrinos, indicated by the CE𝜈NS measurements in XENONnT and PandaX-4T.
Future gains will require both larger exposures and a deeper control of irreducible backgrounds—
understanding of backgrounds, not scale alone, will determine the next big result.
Joint analysis frameworks define the state of the art. Cross-instrument likelihoods have replaced
single-experiment limits as the measure of progress. Coordinated statistical frameworks—shared
priors, consistent background models, and open likelihoods—now drive sensitivity gains as much
as raw exposure. A host of upgraded and forthcoming facilities—DarkSide-20k, SuperCDMS,
DarkSPHERE, SABRE South, IceCube Upgrade and Gen-2, KM3NeT, SWGO, CTAO, GAPS,
GRAMS, and the SKA—will soon expand our observational reach, providing us with an unprecedented volume and diversity of data to be analyzed within cross-instrument frameworks that now
underpin the field.
The candidate space has broadened and matured. Axions, ultralight fields, sub-GeV states, and
macroscopic relics are now pursued through coordinated laboratory, astrophysical, and cosmological efforts. What began as separate niche searches has become a coherent strategy spanning more
than eighty orders of magnitude in mass.
Challenges Ahead
Still, realism tempers my optimism. Many of these advances depend on sustained support
for mid-scale experiments, theory-instrument integration, and continuity in space-based 𝛾-ray
coverage—none of which are guaranteed. Without a successor to Fermi-LAT, or a coordinated
MeV mission, the multimessenger bridge risks becoming one-sided. ICRC 2025 showed that the
field’s limitations are increasingly structural rather than technical. The decisive progress in the
coming decade is likely to depend on how effectively the community coordinates analyses across
experiments, instruments, and messengers—turning parallel efforts into a coherent framework rather
than a collection of incremental sensitivity gains.
Where does that leave us? Four decades after the modern search began, the identity of dark
matter remains unknown—but some of its absence is very well-constrained. The field’s maturity
is in itself an achievement: a demonstration that precision, patience, and shared infrastructure can
turn even the null results into scientific progress. Whether we find dark matter in two years, ten, or
fifty, I believe the discovery will trace its lineage to this very moment—when dark matter physics
2 A quiet tap on the shoulder reminding us how far the field has come.

18

## PDF page 19

Milena Crnogorčević

DM Rapporteur ICRC 2025

learned to see more by combining what it already has, and to nurture—as exemplified at ICRC
2025—the community that carries it forward.

Acknowledgments
I thank the organizers of ICRC 2025 for the opportunity to serve as Dark Matter rapporteur and
the 78 contributors whose presentations and proceedings informed this summary. Special thanks
to Tim Linden, Silvia Manconi, Michael Korsmeier, Ludwig Neste, Carlos Blanco, Isabelle John,
Pedro De la Torre Luque, Thong Nguyen, and Alexandre Adler for their insightful discussions that
shaped this rapportour paper. I additionally acknowledge the use of OpenAI’s ChatGPT to assist
with editing and proofreading of the manuscript. My work is supported by the Swedish Research
Council under contract 2022-04283 and the Swedish National Space Agency under contract 117/19.

References
[1] G. Bertone, ed., Particle Dark Matter: Observations, Models and Searches, Cambridge
University Press (2010). doi:10.1017/CBO9780511770739
[2] G. Bertone and D. Hooper, History of dark matter, Rev. Mod. Phys. 90 (2018) 045002.
doi:10.1103/RevModPhys.90.045002
[3] M. Bauer and T. Plehn, Yet Another Introduction to Dark Matter: The Particle Physics
Approach, Lecture Notes in Physics 959, Springer (2019). doi:10.1007/978-3-030-16234-4
[4] S. Profumo, An Introduction to Particle Dark Matter, Advanced Textbooks in Physics, World
Scientific (2017). doi:10.1142/q0001
[5] D. J. E. Marsh, D. Ellis, and V. F. Mehta, Dark Matter: Evidence, Theory, and Constraints,
Princeton Series in Astrophysics, Princeton University Press (2024). Publisher Link
[6] E. Angelino et al. [XENONnT Collaboration], Searching for Dark Matter and Rare Events
with XENONnT, PoS(ICRC2025)501, 465 (2025), doi:10.22323/1.501.0465
[7] Y. Tao et al. [PandaX-4T Collaboration], PandaX-4T Reaches As A Multi-purpose LXe Experiment, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva,
Switzerland, July 17, 2025. Conference Link
[8] L. Baudis, Direct Detection of Dark Matter: Status, Challenges, and Future Prospects,
Invited plenary talk at the 38th International Cosmic Ray Conference (ICRC 2025), Geneva,
Switzerland, July 22, 2025. Conference Link
[9] O. A. Taborda Pulgarin et al. [DarkSide Collaboration], The DarkSide-20k experiment,
PoS(ICRC2025)501, 532 (2025), doi:10.22323/1.501.0532
[10] A. Garai [DEAP Collaboration], Latest results and future prospects of DEAP-3600, talk
presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland,
July 17, 2025. Conference Link
19

## PDF page 20

Milena Crnogorčević

DM Rapporteur ICRC 2025

[11] A.M. Botti [SENSEI Collaboration], Latest results and prospects of the SENSEI experiment, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva,
Switzerland, July 17, 2025. Conference Link
[12] M. Elwan [SuperCDMS Collaboration], SuperCDMS Experiment at SNOLAB: Current Status
and Recent CUTE Results, PoS(ICRC2025)501, 482 (2025), doi:10.22323/1.501.0482
[13] J.-M. Coquillat [NEWS-G Collaboration], Light WIMP search with the NEWS-G experiment,
PoS(ICRC2025)501, 477 (2025), doi:10.22323/1.501.0477
[14] L. Milligan on behalf of the SABRE South Collaboration, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland, July 17, 2025. Conference
Link
[15] C. Locatelli, A. Pollmann, H. Toribuchi, and D. Zhang, Thermal Shocks as a Detection
Method for Heavy Exotic Particles in Neutrino Telescopes, PoS(ICRC2025)501, 516 (2025),
doi:10.22323/1.501.0516
[16] A. Cavicchi, G. W. de Wasseige, M. Lamoureux, J. Mauro, and F. Sala, IceCube as a Direct
Detector of Sub-GeV Dark Matter, PoS(ICRC2025)501, 475 (2025), doi:10.22323/1.501.0475
[17] N. F. Iachellini, Searching for Dark Matter with the RES-NOVA Detector, PoS(ICRC2025)501,
483 (2025), doi:10.22323/1.501.0483
[18] J. Jaeckel, Axions and ALPs: Towards Discovery and Beyond, Invited Plenary Talk, 39th International Cosmic Ray Conference (ICRC2025), Geneva, Switzerland, 22 July 2025. Conference
Link
[19] R. Abbasi et al. (IceCube
doi:10.22323/1.501.0502

Collaboration),

PoS(ICRC2025)501,

502

(2025),

[20] C. Poirè and J. García Mendéz, Indirect Dark Matter Searches Towards the Sun using the Full
ANTARES Data Set, PoS(ICRC2025)501, 515 (2025), doi:10.22323/1.501.0515
[21] M. Andrade et al., Prospects for the Detection of Dark Matter with Long-Lived Mediators
in the Sun using the Southern Wide-field Gamma-ray Observatory, PoS(ICRC2025)501, 464
(2025), doi:10.22323/1.501.0464
[22] A. Abhishek, S. Abe, T. Inada, S. Ventura, M. Doro, M. Teshima, and G. Verna [CTAO LST-1
Collaboration], Line emission search from Dark Matter annihilation in the Galactic Center
with LST-1, PoS(ICRC2025)501, 462 (2025), doi:10.22323/1.501.0462
[23] N. Chau and J. A. Aguilar [IceCube Collaboration], Dark matter searches in the Galactic Center with IceCube-DeepCore and IceCube-Upgrade, PoS(ICRC2025)501, 476 (2025),
doi:10.22323/1.501.0476
[24] A. Bariego-Quintana, A. Saina, and C. Gatius, WIMP Dark Matter Searches from the Galactic
Centre with KM3NeT, PoS(ICRC2025)501, 469 (2025), doi:10.22323/1.501.0469
20

## PDF page 21

Milena Crnogorčević

DM Rapporteur ICRC 2025

[25] E. Ramos Cascón, P. Fernández, I. Martínez-Soler, and V. Takhistov, High Energy Astrophysical Neutrino Flux and Galactic Center Dark Matter Annihilation Search with HyperKamiokande, PoS(ICRC2025)1151 (2025), https://pos.sissa.it/ICRC2025/1151
[26] P. De la Torre Luque, The CMZ anomalous ionization rate explained by MeV dark matter, talk
presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland,
July 22, 2025. Conference Link
[27] Z. Q. Shen, K. K. Duan, W. Jiang, X. Li, and X. Huang [DAMPE Collaboration],
Analysis of the Galactic diffuse emission with DAMPE, PoS(ICRC2025)501, 844 (2025),
doi:10.22323/1.501.0844
[28] A. Aguirre-Santaella, G. Ogiya, and M. A. Sánchez-Conde, A detailed characterisation of
low-mass dark matter subhalo tidal tracks via numerical simulations, talk presented at the
39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland, July 22, 2025.
Conference Link
[29] S. Porras Bedmar, M. A. Sánchez-Conde, and A. Aguirre-Santaella, Impact of baryons on the
population of galactic subhalos and implications for dark matter searches, talk presented at the
39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland, July 22, 2025.
Conference Link
[30] J. G. Mamprim, G. Gambini, L. B. Arbeletche, M. Olegario, and V. de Souza, Probing
late-time annihilations of oscillating asymmetric dark matter via rotation curves of galaxies,
PoS(ICRC2025)501, 489 (2025), doi:10.22323/1.501.0489
[31] J. M. Frieden and C. Perrina, Search for gamma-ray spectral lines from dark-matter annihilation with the DAMPE satellite, PoS(ICRC2025)501, 484 (2025), doi:10.22323/1.501.0484
[32] M. Giliberti, M. N. Mazziotta, and F. Loparco, Search for line-like and box-like features in
Galactic gamma-ray spectra as signatures of dark matter using 15+ years of Fermi-LAT data,
PoS(ICRC2025)501, 488 (2025), doi:10.22323/1.501.0488
[33] K. Aoyama, GAPS Detector Cooling System: Results from Antarctic Ground Tests,
PoS(ICRC2025)501, 466 (2025), doi:10.22323/1.501.0466
[34] A. Stoessl, Estimating the performance of the GAPS detector with muon ground testing data
from Antarctica, PoS(ICRC2025)501, 531 (2025), doi:10.22323/1.501.0531
[35] T. Aramaki, The GRAMS (Gamma-Ray and AntiMatter Survey) Project: Overview and Current Status, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025),
Geneva, Switzerland, July 19, 2025. Conference Link
[36] L. E. Ghezzer, F. Nozzoli, L. Ricci, P. Spinnato, E. Verroi, and P. Zuccon, Advancing Antideuteron Detection in Cosmic Rays: Innovations in Methods and Technologies,
PoS(ICRC2025)501, 508 (2025), doi:10.22323/1.501.0508
21

## PDF page 22

Milena Crnogorčević

DM Rapporteur ICRC 2025

[37] J. Rico et al., A Joint Gamma-ray Search for Dark Matter in Dwarf Spheroidal Galaxies
with Fermi-LAT, HAWC, H.E.S.S., MAGIC and VERITAS, PoS(ICRC2025)501, 522 (2025),
doi:10.22323/1.501.0522
[38] C. McGrath [VERITAS Collaboration], Dark Matter Searches in Dwarf Galaxies with VERITAS, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva,
Switzerland, July 18, 2025. Conference Link
[39] M. Crnogorcevic, Dark Matter from the Littlest Galaxies: Gamma-ray Insights from UltraFaint Dwarfs and IMBHs, talk presented at the 39th International Cosmic Ray Conference
(ICRC 2025), Geneva, Switzerland, July 18, 2025. Conference Link
[40] S. Semane, G. Beck, S. Makhathini, M. Regis, and G. Bernardi, Constraints on WIMP
Annihilation from MeerKAT UHF-Band Observations of Reticulum II, PoS(ICRC2025)501,
525 (2025), doi:10.22323/1.501.0525
[41] D. N. Salazar-Gallegos et al. [IceCube Collaboration], Heavy Dark Matter Annihilation Search
with IceCube Tracks, PoS(ICRC2025)501, 523 (2025), doi:10.22323/1.501.0523
[42] A. Aravinthan et al., Modeling of Dark Matter Prompt and Secondary Signatures in Dwarf
Galaxies, PoS(ICRC2025)501, 468 (2025), doi:10.22323/1.501.0468
[43] N. Lavis and G. Beck, Exploring Dark Matter in Galaxy Clusters with MeerKAT: South
Africa’s Powerful Radio Telescope at the Forefront of Astronomy, PoS(ICRC2025)501, 501
(2025), doi:10.22323/1.501.0501
[44] F. Bradascio and J.-F. Glicenstein [H.E.S.S. Collaboration], Searching for Dark
Matter Signatures in the Virgo Cluster with H.E.S.S., PoS(ICRC2025)659 (2025),
https://pos.sissa.it/ICRC2025/659
[45] Z. Shen et al., A 43 GeV Gamma-ray Line in the Nearby Galaxy Clusters?, talk presented at the
39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland, July 18, 2025.
Conference Link
[46] I. Watson, Search for Axion-like Particles Using TeV Blazar Observations with the HAWC
Observatory, PoS(ICRC2025)501, 538 (2025), doi:10.22323/1.501.0538
[47] J. Serna-Franco et al., Searching for Axion-like Particle Signatures in the M87 Spectrum with
HAWC, PoS(ICRC2025)501, 527 (2025), doi:10.22323/1.501.0527
[48] J. Serna-Franco et al., Prospects of Axion-like Particle Searches with the Southern Wide-field Gamma-ray Observatory (SWGO), PoS(ICRC2025)501, 526 (2025),
doi:10.22323/1.501.0526
[49] D. Kantzas et al., Astrophysical Jets to Constrain the Dark Matter Nature, talk presented at the
39th International Cosmic Ray Conference (ICRC 2025), Geneva, Switzerland, July 22, 2025.
Conference Link
22

## PDF page 23

Milena Crnogorčević

DM Rapporteur ICRC 2025

[50] O. Ghosh, S. Jacobsen, and T. Linden, Do Axions Put Out Gamma-Ray Bursts?,
PoS(ICRC2025)501, 487 (2025), doi:10.22323/1.501.0487
[51] P. Kivokurtseva, Neutrino Production in the Central Dark-Matter Spikes of Active Galaxies, talk presented at the 39th International Cosmic Ray Conference (ICRC 2025), Geneva,
Switzerland, July 22, 2025. Conference Link
[52] H. Jiang, X. Bi, S. Hu, and Z. Li [LHAASO Collaboration], An all-sky search for individual Primordial Black Hole burst with LHAASO, PoS(ICRC2025)501, 496 (2025),
doi:10.22323/1.501.0496
[53] L. Stefanuto, V. De Romeri, F. Donato, D. Maurin, and A. Tolino, Cosmic antimatter signatures
from primordial black holes, PoS(ICRC2025)501, 530 (2025), doi:10.22323/1.501.0530
[54] D. Horns, M. Meyer, and S. Porras Bedmar, Novel bounds on decaying axionlike particle
dark matter from the cosmic background, talk presented at the 39th International Cosmic Ray
Conference (ICRC 2025), Geneva, Switzerland, July 22, 2025. Conference Link
[55] M. Vecchi, J. Aschersleben, D. Horns, E. Moulin, and the H.E.S.S. Collaboration, Search
for dark matter around intermediate-mass black holes with the H.E.S.S. experiment,
PoS(ICRC2025)501, 534 (2025), doi:10.22323/1.501.0534
[56] M. Vecchi and M. Croisonnier, Search for gamma-ray signatures from dark matter spikes
around an intermediate-mass black hole in Omega Centauri, PoS(ICRC2025)501, 535 (2025),
doi:10.22323/1.501.0535
[57] J. Häußler et al. [IceCube Collaboration], Search for Sub-Relativistic Magnetic
Monopoles with the IceCube Neutrino Observatory, PoS(ICRC2025)501, 492 (2025),
doi:10.22323/1.501.0492
[58] F. Kajino et al. [DIMS Collaboration], DIMS (Dark matter Interstellar Meteoroid Study)
Experiment, PoS(ICRC2025)501, 529 (2025), doi:10.22323/1.501.0529
[59] Z. D. Plebaniak et al. [SQM-ISS Collaboration], Searching for Massive, Non-relativistic
Particles in Space with the SQM-ISS Detector, PoS(ICRC2025)501, 514 (2025),
doi:10.22323/1.501.0514

23
