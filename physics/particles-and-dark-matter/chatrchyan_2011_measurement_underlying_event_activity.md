Source: https://doi.org/10.1007/JHEP09(2011)109
PDF sha256: 0975be8b3006f4d223df516db5553c0227491f79a00fb4c2772ae6139105e429
License: CC-BY-NC
Language: eng
Fidelity: machine (failed: text-layer)

# Transcription of chatrchyan_2011_measurement_underlying_event_activity.pdf

Transcription of `chatrchyan_2011_measurement_underlying_event_activity.pdf` in this directory, 31 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

RECEIVED: July 1, 2011 ACCEPTED: August 31, 2011 PUBLISHED: September 23, 2011

# Measurement of the underlying event activity at the LHC with $\sqrt{s}=7\,\mathrm{TeV}$ and comparison with $\sqrt{s}=0.9\,\mathrm{TeV}$

#### The CMS collaboration

E-mail: cms-publication-committee-chair@cern.ch

ABSTRACT: A measurement of the underlying activity in events with a jet of transverse momentum in the several GeV region is performed in proton-proton collisions at  $\sqrt{s} = 0.9$  and 7 TeV, using data collected by the CMS experiment at the LHC. The production of charged particles with pseudorapidity  $|\eta| < 2$  and transverse momentum  $p_T > 0.5 \,\text{GeV}/c$  is studied in the azimuthal region transverse to that of the leading set of charged particles forming a track-jet. A significant growth of the average multiplicity and scalar- $p_T$  sum of the particles in the transverse region is observed with increasing  $p_T$  of the leading track-jet, followed by a much slower rise above a few GeV/c. For track-jet  $p_T$  larger than a few GeV/c, the activity in the transverse region is approximately doubled with a centre-of-mass energy increase from 0.9 to 7 TeV. Predictions of several QCD-inspired models as implemented in PYTHIA are compared to the data.

**KEYWORDS:** Hadron-Hadron Scattering

## PDF page 2

| $\mathbf{C}$ | ontents                                                |    |
|--------------|--------------------------------------------------------|----|
| 1            | Introduction                                           | 1  |
| 2            | Experimental details                                   | 3  |
| 3            | Underlying event in the transverse region              | Ę  |
|              | 3.1 Hard-scale dependence                              | ţ  |
|              | 3.2 Multiplicity and transverse momentum distributions |    |
|              | 3.3 Centre-of-mass energy dependence                   | 8  |
| 4            | Summary and conclusions                                | 11 |
| $\mathbf{T}$ | he CMS collaboration                                   | 14 |

#### 1 Introduction

In hadron-hadron scatterings, the "underlying event" (UE) is defined, in the presence of a hard parton-parton scattering with large transverse momentum transfer, as any hadronic activity that is additional to what can be attributed to the hadronization of partons involved in the hard scatter and to related initial and final state QCD radiation. The UE activity is thus attributed to the hadronization of partonic constituents that have undergone multiple parton interactions (MPI), as well as to beam-beam remnants, concentrated along the beam direction. Good understanding of UE properties is important for precision measurements of standard model processes and the search for new physics at high energy. Examples are the determination of the losses of events due to isolation criteria in lepton identification, or the computation of reconstruction efficiency for processes like  $H \rightarrow \gamma \gamma$  where the vertex is given by the underlying event.

The first measurement of UE activity at the LHC, with proton-proton centre-of-mass energy  $\sqrt{s} = 0.9 \, \text{TeV}$ , has been published by CMS [1]. The present paper, which follows the same analysis procedure, reports on a measurement at  $\sqrt{s} = 7 \, \text{TeV}$ ; new measurements at  $0.9 \, \text{TeV}$  are also reported, with an event sample 30 times larger than that in ref. [1]. In this paper all measurements are fully corrected for detector effects. Details are given below. The ATLAS collaboration has reported on measurements at  $\sqrt{s} = 0.9$  and  $7 \, \text{TeV}$  [2], using slightly different analysis procedures.

The UE activity in jet production at a given centre-of-mass energy is expected to increase with the hard scale in the interaction, as defined by the transverse momentum of the jet. Events with a harder scale are indeed expected to correspond, on average, to interactions with a smaller impact parameter, a feature which in turn should enhance MPI [3, 4]. This increased activity is observed to reach a plateau for high scales, corresponding to

## PDF page 3

an MPI "saturation" effect for impact parameters selected by a sufficiently hard leading interaction. Conversely, for events with the same hard scale but taken at different values of the centre-of-mass energy, MPI activity is expected to increase with  $\sqrt{s}$  [3, 4]. The present analysis is focused on measurements that can contribute to the understanding of the UE dynamics, through the comparison of events at the same  $\sqrt{s}$  but with different hard scales, and the comparison of data with the same hard scale but with different values of  $\sqrt{s}$ .

To study the UE, it is convenient to refer to the difference in azimuthal angle,  $\Delta \phi$ , between the projections onto the plane perpendicular to the beam of the directions of the hard scatter and of any hadron in the event. With this method, the UE activity is made manifest in the "transverse" region with  $60^{\circ} < |\Delta \phi| < 120^{\circ}$ , even though it cannot in principle be uniquely separated from initial and final state radiation. In this paper, the direction of the hard scatter is identified with that of the leading "track-jet", i.e. the object with largest transverse momentum,  $p_T$ , formed using a jet algorithm applied to reconstructed tracks of particles above some minimum  $p_T$  value in the event. The leading track-jet  $p_T$  is taken as defining the hard scale in the event. An advantage of using a track-jet as a reference is that it is an experimentally well-defined object, essentially free from pileup effects. No attempt is made to refer to the corresponding parton-level objects, as this would result in additional model uncertainties. However, the track-jet is much closer to the parton-level object than the leading track. Finally, in the few GeV/c region, the value of the track-jet  $p_T$  is better defined and more stable than for calorimeter based jets, which suffer from large fluctuations.

The UE dynamics are studied through the comparison with data of models implemented in Monte Carlo (MC) simulations adopting MPI. The predictions of the models without MPI fail to reproduce the evolution of the UE observables with the scale of the interaction and with the centre-of-mass energy [5]. The predictions for inelastic events are provided here by several tunes of the PYTHIA program, versions 6.420 [3, 6] and 8.145 [7, 8]. The pre-LHC D6T tune [9, 10] of PYTHIA6, which describes the lower energy UA5 and Tevatron data, is a widely used reference that will also be used for the present analysis. The tunes DW [10] and CW [1], which were found to describe best the data at 0.9 TeV [1], will be discussed for the present 7 TeV data. The new PYTHIA6 tune, Z1 [11], includes  $p_T$  ordering of parton showers and the new PYTHIA MPI model [12]. It implements the results of the Professor tunes [13] considering the fragmentation and the coulor reconnection parameters of the AMBT1 tune [14]; preliminary CMS UE results at 7 TeV have been used to tune the parameters governing the value and the  $\sqrt{s}$  dependence of the transverse momentum cutoff that in PYTHIA regularizes the divergence of the leading order scattering amplitude as the final state parton transverse momentum  $\hat{p}_T$  approaches 0. The tune Z2 is similar to Z1, except for the transverse momentum cutoff at the nominal energy of  $\sqrt{s_0} = 1.8 \,\text{TeV}$  which is decreased by  $0.1 \,\text{GeV/c}$ . PYTHIA8 also uses the new PYTHIA MPI model, which is interleaved with parton showering. The new PYTHIA8 version 4C [15] has also been tuned to the early LHC data. The PYTHIA8 model includes soft and hard diffraction [16], whereas only soft diffraction is included in PYTHIA6; the precise description of diffraction is, however, of little relevance for the present analyses since it has been checked that the diffractive contributions are strongly suppressed by the trigger and event selection requirements, especially for large  $p_T$  values of the leading track-jet. The parton

## PDF page 4

distribution functions (PDF) used to describe the protons are the CTEQ6L1 set [\[17\]](#page-13-3) for D6T, Z2 and 4C, and CTEQ5L [\[18\]](#page-13-4) for the other simulations.

The outline of the paper is as follows. Section [2](#page-3-0) presents experimental details: brief detector description, data samples, event and track selection, track-jet reconstruction, unfolding procedure and systematic uncertainties. Section [3](#page-5-0) presents results on the transverse region dynamics: hard-scale dependence and particle spectra at <sup>√</sup> s = 7 TeV, and centreof-mass energy dependence of the transverse region dynamics. Section [4](#page-11-0) summarizes the main results of the study and draws conclusions.

## 2 Experimental details

A description of the CMS detector can be found in ref. [\[19\]](#page-13-5). The coordinate system has the origin at the nominal interaction point. The z axis is parallel to the anticlockwise beam direction; it defines the polar angle θ and the pseudorapidity η = − ln(tan(θ/2)). The azimuthal angle φ is measured in the plane transverse to the beam, from the direction pointing to the centre of the LHC ring toward the upward direction. The pixel and silicon strip tracker, immersed in the uniform 3.8 T magnetic field provided by a 6 m diameter superconducting solenoid, measures charged particle trajectories in the pseudorapidity range |η| < 2.5. The p<sup>T</sup> resolution for 1 GeV/c charged particles is between 0.7% at η = 0 and 2% at |η| = 2.5.

For this analysis, the same selection conditions apply to events and tracks at 0.9 and 7 TeV; these conditions are very similar to those at 0.9 TeV in ref. [\[1\]](#page-12-0). Minimum bias events are triggered by requiring activity in both Beam Scintillator Counters (BSC) [\[19,](#page-13-5) [20\]](#page-13-6), in coincidence with signals from both beams in the Beam Pick-up Timing for eXperiments (BPTX) devices [\[19,](#page-13-5) [21\]](#page-13-7); low-p<sup>T</sup> track-jets are recorded with a prescaled minimum bias trigger. At 7 TeV, in order to enhance the acquisition of events with a harder scale and reduce statistical fluctuations, the analysis also uses single-jet triggers.

Selected events are required to contain one and only one primary vertex, reconstructed in fits with more than four degrees of freedom, with a z coordinate within 10 cm of the centre of the 4 cm-wide beam collision region. Rejecting events with more than one primary vertex does not bias the final results, as was checked by comparing data with different pileup conditions, taken at low and high instantaneous luminosities.

Selected events are also required to contain a track-jet with p<sup>T</sup> >1 GeV/c, reconstructed with pseudorapidity |η|<2. Track-jets are defined using the SISCone algorithm [\[22\]](#page-13-8) as implemented in the FastJet package [\[23\]](#page-13-9) with a clustering radius R = p (∆φ) <sup>2</sup> + (∆η) <sup>2</sup> = 0.5. Charged particles reconstructed in the tracker with p<sup>T</sup> >0.5 GeV/c and |η|<2.5 are used to define the track-jet; this η range is wider than that used for the UE analysis (|η|<2) in order to avoid a kinematic bias.

A track is selected for the UE analysis if it is consistent with the primary vertex and is reconstructed in the pixel and silicon strip tracker with transverse momentum p<sup>T</sup> > 0.5 GeV/c and pseudorapidity |η| < 2. A high-purity reconstruction algorithm is used, which keeps low levels of misreconstructed and poorly reconstructed tracks [\[24\]](#page-13-10). To decrease contamination by secondary tracks from decays of long-lived particles and photon

## PDF page 5

|                                | √<br>s<br>= 7 TeV |         |          | √<br>s<br>= 0.9 TeV |         |          |
|--------------------------------|-------------------|---------|----------|---------------------|---------|----------|
| leading track-jet<br>pT<br>>   | 1 GeV/c           | 3 GeV/c | 20 GeV/c | 1 GeV/c             | 3 GeV/c | 20 GeV/c |
| No. selected events (×103<br>) | 18 543            | 6 674   | 19       | 5 140               | 783     | 0.25     |
| No. selected tracks (×103<br>) | 202 952           | 120 945 | 638      | 33 743              | 9 001   | 5.8      |

Table 1. Number of selected events and corresponding number of selected tracks, for three values of minimum track-jet <sup>p</sup><sup>T</sup> and for both <sup>√</sup> s = 0.9 and 7 TeV.

conversions, the distance of closest approach between the track and the primary vertex is required to be less than three times its (significantly non-Gaussian) estimated uncertainty, both in the transverse plane and along the z-axis; the uncertainty in the vertex position is also taken into account. Poorly measured tracks are removed by requiring σ(p<sup>T</sup> )/p<sup>T</sup> <5%, where σ(p<sup>T</sup> ) is the uncertainty on the p<sup>T</sup> measurement. In the selected track sample with |η| < 2, these selections result in a background level of 3%: 1% from K<sup>0</sup> S and Λ<sup>0</sup> decay products and 2% from combinatorial background, as estimated using MC simulations. The number of selected events at both centre-of-mass energies, for track-jet p<sup>T</sup> > 1, 3, and 20 GeV/c, and the corresponding number of selected tracks are given in table [1.](#page-4-0)

The distributions presented below are fully corrected for detector effects. An iterative unfolding technique [\[25\]](#page-13-11) is used, except for some cases that will be detailed below. The pythia6 MC with Z2 tune was used to correct the experimental distributions, while Z1, D6T and the default configuration of pythia 8.135 ("tune 1") were used for cross-checks and systematic uncertainty estimates. The detector response was simulated in detail using the GEANT4 package [\[26\]](#page-13-12), and simulated events were processed and reconstructed in the same manner as collision data. The simulations were found to give a very good description of all features related to detector performance that are relevant to this analysis. The unfolding procedure was tested using MC events, by comparing the genuine distributions for generated hadrons with the distributions obtained, after unfolding, from reconstructed tracks.

Systematic uncertainties on the corrected data have been studied in detail. They correspond essentially to the uncertainties described in [\[1\]](#page-12-0) taking into account the progress reported in ref. [\[24\]](#page-13-10). They include the implementation in the simulation of vertex and track selection criteria, tracker alignment and tracker material content, background contamination from K<sup>0</sup> S and Λ<sup>0</sup> production, trigger conditions, run-to-run variations of tracker and beam conditions, including the effect of pileup, and the effect of limited samples.

Using as MC input the Z1 simulation, which gives the best description of data, unfolding procedures were performed using both the Z2 and tune 1 models; the maximum discrepancies with the MC input were taken as systematic uncertainties.

Systematic uncertainties are largely independent of one another, but they are correlated among data points in each experimental distribution. They are added in quadrature to statistical uncertainties and represented in all figures.

## PDF page 6

Figure 1. Fully corrected measurements of charged particles with  $p_T > 0.5 \,\mathrm{GeV}/c$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta\phi| < 120^\circ$ , as a function of the  $p_T$  of the leading track-jet: (left) average multiplicity per unit of pseudorapidity and per radian; (centre) average scalar  $\sum p_T$  per unit of pseudorapidity and per radian; (right) ratio of the average scalar  $\sum p_T$  and the average multiplicity. Predictions of three PYTHIA tunes are compared to the data.

### 3 Underlying event in the transverse region

The hadronic activity at 7 TeV in the transverse region, for charged particles with  $p_T > 0.5 \,\text{GeV}/c$ ,  $|\eta| < 2$ , and  $60^\circ < |\Delta\phi| < 120^\circ$ , is first presented as a function of the leading trackjet  $p_T$  (section 3.1). Multiplicity and transverse momentum distributions are then reported for two minimal values, 3 and 20 GeV/c, of the leading track-jet  $p_T$  (section 3.2). Results at the two centre-of-mass energies,  $\sqrt{s} = 0.9$  and 7 TeV, are finally compared (section 3.3). Predictions from the various PYTHIA models are compared to the corrected data.

#### 3.1 Hard-scale dependence

Figure 1 presents the average multiplicity and the average scalar momentum sum in the transverse region, as a function of the leading track-jet  $p_T$ . For these distributions, full unfolding was performed in both the track-jet  $p_T$  and the studied variable, for leading track-jet  $p_T$  up to  $20 \,\text{GeV/c}$ . Bin-by-bin corrections were used at higher values of the leading track-jet  $p_T$  where the  $p_T$  dependence of the studied variables is small.

The horizontal error bars indicate the bin size; the vertical inner error bars indicate the statistical uncertainties affecting the measurements; the outer error bars represent the statistical and systematic uncertainties added in quadrature; statistical uncertainties dominate at large values of the hard scale. The same conventions and considerations apply throughout this paper.

Two regions are visible for both observables in figure 1: a fast rise for  $p_T \lesssim 8 \,\mathrm{GeV/c}$ , attributed mainly to the increase of MPI activity, followed by a plateau-like region with nearly constant average number of selected particles and a slow increase of  $\Sigma p_T$ . A similar structure is observed at 0.9 TeV (see ref. [1] and figure 5 below), the fast rise being limited in that case to the region with leading track-jet  $p_T \lesssim 4 \,\mathrm{GeV/c}$ . All PYTHIA models predict such a distinct change of the amount of activity in the transverse region as a function of the leading track-jet  $p_T$ .

## PDF page 7

Figure 2. Ratios, as a function of the leading track-jet  $p_T$ , of three MC predictions to the fully corrected measurements of charged particles with  $p_T > 0.5 \,\text{GeV}/c$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta \phi| < 120^\circ$  (cf. figure 1): (left) average multiplicity; (centre) average scalar  $\sum p_T$ ; (right) ratio of the average scalar  $\sum p_T$  and the average multiplicity. The inner bands correspond to the systematic uncertainties and the outer bands to the total experimental uncertainties (statistical and systematic uncertainties added in quadrature).

These evolutions result in a slow but continuous increase of the average  $p_T$  of the selected particles for leading track-jet  $p_T$  above a few GeV/c. This is observed in figure 1 (right plot), which is obtained from the ratio of the two profile distributions, with the relative uncertainties conservatively summed in quadrature. (A similar behaviour of the ratio can be deduced at 0.9 TeV).

The information on the quality of the data description by the different models is summarized in figure 2, which presents the ratio of the MC predictions to the measurements for the observables shown in figure 1. Statistical fluctuations in the data induce correlated fluctuations for the various MC/data ratios. Variations in the error bands are related to the unfolding procedures, and to the different sets of data collected with different triggers.

The description provided by Z1 is very good for both the average multiplicity and the average scalar momentum sum, over the full leading track-jet  $p_T$  range. For the PYTHIA8 4C tune, in the region with track-jet  $p_T < 20 \,\text{GeV/c}$  the predictions are below the data by 5% (10%) for the average charged multiplicity (average scalar  $\sum p_T$ ); for larger track-jet  $p_T$  values, the average charged multiplicity is well described but the average  $\sum p_T$  is increasingly underestimated, by up to 20%. This confirms observations reported in ref. [27]. The predictions of the Z2 tune (not shown in this paper) reveal similar trends as for PYTHIA8 4C with, however, a more uniform and more limited underestimate ( $\lesssim 10\%$ ) of the average  $\sum p_T$ .

As illustrated by D6T, the predictions of older PYTHIA6 tunes are significantly below the data in the region characterized by the fast rise of the observables (track-jet  $p_T \lesssim 8\,\mathrm{GeV/c}$ ); in the "saturation" region, tune D6T provides a good description of the average multiplicity but the average  $\sum p_T$  is largely underestimated for track-jet  $p_T > 40\,\mathrm{GeV/c}$ . In this region, DW predictions are lower than for D6T, and CW even lower, which reflects the different values of the cutoff transverse momentum and its  $\sqrt{s}$  dependence [1] (CW and the DW predictions are not shown in this paper).

## PDF page 8

The comparison with data of the MC predictions for the ratio of the average Pp<sup>T</sup> and the average multiplicity is shown in figure [2](#page-6-0) (right). The absolute value is described within 5% and the hard-scale dependence is well described by Z1. The pythia8 4C and Z2 predictions agree with Z1 in the rising region, but the normalization is up to 10% and 20% lower in the "saturation" region, respectively. For D6T, the ratio is overestimated below 30 GeV/c, and underestimated above 30 GeV/c.

## 3.2 Multiplicity and transverse momentum distributions

Figure [3](#page-8-1) presents, for charged particles in the transverse region, the normalized multiplicity distribution, the normalized Pp<sup>T</sup> distribution, and the particle p<sup>T</sup> spectrum. Events are selected with two minimal values of the leading track-jet p<sup>T</sup> : p<sup>T</sup> > 3 GeV/c (upper row) and p<sup>T</sup> >20 GeV/c (central row). For the charged multiplicity and Pp<sup>T</sup> distributions, full unfolding was performed for leading track-jet p<sup>T</sup> > 3 GeV/c, whereas for leading track-jet p<sup>T</sup> >20 GeV/c, in the "saturation" region, simpler unfolding is performed, which does not take into account the hard-scale dependence. In the latter case the unfolding procedure is found to occasionally introduce correlations between adjacent bins, which arise from statistical fluctuations in the uncorrected distributions. For the p<sup>T</sup> spectra presented in the right column of figure [3](#page-8-1) bin-by-bin corrections were applied. The correction factors are found to be mostly independent of the track-jet p<sup>T</sup> and from the centre-of-mass energy.

The distributions in figure [3](#page-8-1) are presented for a range of the variables for which the total relative uncertainty, after unfolding, does not exceed 30%. It is remarkable that the charged particle spectra extend to p<sup>T</sup> >10 GeV/c, indicating the presence of a hard component in particle production in the transverse region. The distributions for the two scale selections p<sup>T</sup> >3 GeV/c and p<sup>T</sup> >20 GeV/c are directly compared in the lower-row plots of figure [3.](#page-8-1) Growth of the UE activity with increasing hard scale is observed both through multiplicity increase and single-particle p<sup>T</sup> spectra hardening, consistent with the increase of particle average p<sup>T</sup> shown in figure [1](#page-5-2) (right). The three distributions are overall rather well described by the selected MC models over several orders of magnitude (more than 6 for the p<sup>T</sup> spectrum).

Detailed comparisons are provided in figure [4,](#page-9-0) which presents the ratio of the MC predictions to the measurements in figure [3.](#page-8-1) In the presence of a hard scale, characterized by a leading track-jet with p<sup>T</sup> >20 GeV/c (lower plots in figure [4\)](#page-9-0), the Z1, Z2, and pythia8 4C tunes describe the data well in view of the steeply falling character of the distributions. They do indeed describe all three distributions within 10 − 15% over most of the domain, except for pythia8 4C for very small values of Nch and Pp<sup>T</sup> , and for p<sup>T</sup> > 4 GeV/c. Data description by D6T is worse, especially the Pp<sup>T</sup> distribution and the p<sup>T</sup> spectrum.

The description of the data in the region with leading track-jet p<sup>T</sup> >3 GeV/c (figure [3](#page-8-1) upper plots), dominated by interactions with a soft scale, is not so good. In this domain, all tunes overestimate the contributions of events with very low multiplicity and Pp<sup>T</sup> (Nch . 4, Pp<sup>T</sup> . 4 GeV/c); the discrepancies are largest for D6T. For larger values of the observables, the predictions of Z1, Z2, and pythia8 4C are reasonably close to the data, the weak points being the description by Z1 of multiplicities between 10 and 20, and the descrip-

## PDF page 9

Figure 3. Fully corrected measurements of charged particles with  $p_T > 0.5 \,\mathrm{GeV}/c$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta\phi| < 120^\circ$ : (left) normalized multiplicity distributions; (centre) normalized scalar  $\sum p_T$  distributions; (right) particle  $p_T$  spectra. The leading track-jet is required to have  $|\eta| < 2$  and (upper row)  $p_T > 3 \,\mathrm{GeV/c}$ , or (central row)  $p_T > 20 \,\mathrm{GeV/c}$ . The plots in the lower row provide a direct comparison of the distributions for  $p_T > 3 \,\mathrm{GeV/c}$  and  $p_T > 20 \,\mathrm{GeV/c}$ . Predictions of three PYTHIA tunes are compared to the data.

tion by all tunes of the  $p_T$  spectrum in the region  $3-8\,\mathrm{GeV/c}$ . For D6T, as well as for DW and CW, the descriptions of the  $\sum p_T$  distribution and of the particle  $p_T$  spectrum are poor.

#### 3.3 Centre-of-mass energy dependence

The centre-of-mass energy dependence of the hadronic activity in the transverse region is presented in figure 5 (upper plots) as a function of the leading track-jet  $p_T$ , for  $\sqrt{s} = 0.9$  and 7 TeV. The same unfolding methodology as for figure 1 was applied for the data at  $\sqrt{s} = 0.9$  TeV, in this case with a separation between the two correction procedures at

## PDF page 10

Figure 4. Ratios of three MC predictions to the fully corrected measurements of charged particles with  $p_T > 0.5 \,\mathrm{GeV/c}$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta\phi| < 120^\circ$  (cf. figure 3): (left) multiplicity distributions; (centre) scalar  $\sum p_T$  distributions; (right) particle  $p_T$  spectra. The leading track-jet is required to have  $|\eta| < 2$  and (upper plots)  $p_T > 3 \,\mathrm{GeV/c}$ , or (lower plots)  $p_T > 20 \,\mathrm{GeV/c}$ . The inner bands correspond to the systematic uncertainties and the outer bands to the total experimental uncertainties (statistical and systematic uncertainties added in quadrature).

 $10 \,\mathrm{GeV/c}$  reflecting the narrower rising region. The large increase with  $\sqrt{s}$  of the hadronic activity in the transverse region and its hard-scale dependence is shown in the lower plots of figure 5, in the form of the ratio of the 7 TeV to the 0.9 TeV results. Here the systematic uncertainties at 0.9 and 7 TeV were conservatively combined quadratically, thus neglecting cancellation effects. The ratios, which are close to one for leading track-jet  $p_T = 1.5 \,\mathrm{GeV/c}$ , reach a factor of two for  $p_T \gtrsim 6 - 8 \,\mathrm{GeV/c}$ .

The evolution with the hard scale of the ratio of the UE activity at 7 TeV and 0.9 TeV is described by the Z1 MC. The trend is also reproduced by PYTHIA8 4C. The evolution is much too strong for D6T. The Z2 predictions at  $\sqrt{s} = 0.9$  TeV (not shown here) agree with Z1 in shape but the normalization is 5-10% too high for both observables; this trend is opposite to that observed at 7 TeV, which indicates that a less pronounced  $\sqrt{s}$  dependence of the transverse momentum cutoff should be adopted for tunes using the CTEQ6L1 PDF set than for tunes optimized for CTEQ5L. The PYTHIA8 tune 4C [15] already implements such a prescription.

The strong growth of UE activity with  $\sqrt{s}$  is also striking in the comparison of the normalized distributions of charged particle multiplicity and of scalar  $\sum p_T$  as well as in the  $p_T$  spectra, which are presented in figure 6 for events at  $\sqrt{s} = 7 \text{ TeV}$  and 0.9 TeV with

## PDF page 11

Figure 5. Fully corrected measurements of charged particles with  $p_T > 0.5 \,\text{GeV}/c$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta\phi| < 120^\circ$ : (left plots) average multiplicity, and (right plots) average scalar  $\sum p_T$ , per unit of pseudorapidity and per radian, as a function of the leading track-jet  $p_T$ , for (upper row) data at  $\sqrt{s} = 0.9 \,\text{TeV}$  and  $\sqrt{s} = 7 \,\text{TeV}$ ; (lower row) ratio of the average values at 7 TeV to the average values at 0.9 TeV. Predictions of three PYTHIA tunes are compared to the data.

Figure 6. For charged particles with  $p_T > 0.5\,\mathrm{GeV}/c$  and  $|\eta| < 2$  in the transverse region,  $60^\circ < |\Delta\phi| < 120^\circ$ , (left) normalized multiplicity distributions; (centre) normalized scalar  $\sum p_T$  distributions; (right)  $p_T$  spectra, at  $\sqrt{s} = 7\,\mathrm{TeV}$  and at  $\sqrt{s} = 0.9\,\mathrm{TeV}$ . Events with leading trackjet  $p_T > 3\,\mathrm{GeV/c}$  are selected. Predictions from tune Z1 are compared to the data.

leading track-jet  $p_T > 3 \,\mathrm{GeV/c}$ . The same unfolding methodology as for figure 3 (upper row) was applied at  $\sqrt{s} = 0.9 \,\mathrm{TeV}$ .

## PDF page 12

#### 4 Summary and conclusions

This paper presents a study of the production of charged particles with  $p_T > 0.5 \,\mathrm{GeV/c}$  and  $|\eta| < 2$  at the LHC with the CMS detector in proton-proton collisions at  $\sqrt{s} = 0.9$  and 7 TeV. Events were selected according to the hard scale of the process, provided by the transverse momentum of the leading track-jet, which extends up to  $100 \,\mathrm{GeV/c}$ . The study was done in the transverse region, defined by the difference in azimuthal angle between the leading track-jet and charged particle directions,  $60^{\circ} < |\Delta \phi| < 120^{\circ}$ , which is appropriate for the study of the underlying event. All distributions were fully corrected for detector effects.

A strong increase of the UE activity, quantified through the average multiplicity and the average scalar transverse momentum sum of charged particles in the transverse region, is observed with increasing leading track-jet  $p_T$ . At  $\sqrt{s}=7\,\mathrm{TeV}$  this fast rise is followed above  $\sim 8\,\mathrm{GeV/c}$  by a "saturation" region with nearly constant multiplicity and small  $\sum p_T$  increase. The large increase of activity in the transverse region is observed in the multiplicity distribution, in the  $\sum p_T$  distribution and in the charged particle  $p_T$  spectrum, which were studied, respectively, up to  $N_{\rm ch}=30$ ,  $\sum p_T=35\,\mathrm{GeV/c}$ , and  $p_T=14\,\mathrm{GeV/c}$ . The events at the right end of the distributions indicate the presence of a hard component in the transverse region.

By comparing data taken at  $\sqrt{s} = 0.9$  and 7 TeV, a strong growth with increasing centre-of-mass energy of the hadronic activity in the transverse region is also observed for the same value of the leading track-jet  $p_T$ .

The predictions of several tunes of the PYTHIA program version 6, in particular the new tunes Z1 and Z2, and of the new version PYTHIA8 with tune 4C have been compared to the measurements. A good description of most distributions at  $\sqrt{s} = 7 \,\text{TeV}$  and of the  $\sqrt{s}$  dependence from 0.9 to 7 TeV is provided by the Z1 tune. The predictions of the Z2 and PYTHIA8 4C tunes are also in reasonable agreement with the data.

#### Acknowledgments

We thank Mark Strikman (Penn State University) and Torbjorn Sjöstrand (Lund University) for useful discussions and for assistance in simulating theoretical models.

We wish to congratulate our colleagues in the CERN accelerator departments for the excellent performance of the LHC machine. We thank the technical and administrative staff at CERN and other CMS institutes, and acknowledge support from: FMSR (Austria); FNRS and FWO (Belgium); CNPq, CAPES, FAPERJ, and FAPESP (Brazil); MES (Bulgaria); CERN; CAS, MoST, and NSFC (China); COLCIENCIAS (Colombia); MSES (Croatia); RPF (Cyprus); Academy of Sciences and NICPB (Estonia); Academy of Finland, MEC, and HIP (Finland); CEA and CNRS/IN2P3 (France); BMBF, DFG, and HGF (Germany); GSRT (Greece); OTKA and NKTH (Hungary); DAE and DST (India); IPM (Iran); SFI (Ireland); INFN (Italy); NRF and WCU (Korea); LAS (Lithuania); CINVESTAV, CONACYT, SEP, and UASLP-FAI (Mexico); MSI (New Zealand); PAEC (Pakistan); SCSR (Poland); FCT (Portugal); JINR (Armenia, Belarus, Georgia, Ukraine, Uzbekistan); MST and MAE (Russia); MSTD (Serbia); MICINN and CPAN (Spain); Swiss Funding

## PDF page 13

Agencies (Switzerland); NSC (Taipei); TUBITAK and TAEK (Turkey); STFC (United Kingdom); DOE and NSF (USA).

Individuals have received support from the Marie-Curie programme and the European Research Council (European Union); the Leventis Foundation; the A. P. Sloan Foundation; the Alexander von Humboldt Foundation; the Associazione per lo Sviluppo Scientifico e Tecnologico del Piemonte (Italy); the Belgian Federal Science Policy Office; the Fonds pour la Formation `a la Recherche dans l'Industrie et dans l'Agriculture (FRIA-Belgium); and the Agentschap voor Innovatie door Wetenschap en Technologie (IWT-Belgium).

Open Access. This article is distributed under the terms of the Creative Commons Attribution Noncommercial License which permits any noncommercial use, distribution, and reproduction in any medium, provided the original author(s) and source are credited.

## References

- [1] CMS collaboration, V. Khachatryan et al., Measurement of the underlying event activity in proton-proton collisions at 0.9 TeV, [Eur. Phys. J.](http://dx.doi.org/10.1140/epjc/s10052-010-1453-9) C 70 (2010) 555 [[arXiv:1006.2083](http://arxiv.org/abs/1006.2083)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1006.2083).
- [2] ATLAS collaboration, G. Aad et al., Measurement of underlying event characteristics using charged particles in pp collisions at <sup>√</sup> s = 900 GeV and 7 TeV with the ATLAS detector, Phys. Rev. D 83 [\(2011\) 112001](http://dx.doi.org/10.1103/PhysRevD.83.112001) [[arXiv:1012.0791](http://arxiv.org/abs/1012.0791)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1012.0791).
- [3] T. Sj¨ostrand and M. van Zijl, Multiple parton-parton interactions in an impact parameter picture, [Phys. Lett.](http://dx.doi.org/10.1016/0370-2693(87)90722-2) B 188 (1987) 149 [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?j=PHLTA,B188,149).
- [4] L. Frankfurt, M. Strikman and C. Weiss, Transverse nucleon structure and diagnostics of hard parton-parton processes at LHC, Phys. Rev. D 83 [\(2011\) 054012](http://dx.doi.org/10.1103/PhysRevD.83.054012) [[arXiv:1009.2559](http://arxiv.org/abs/1009.2559)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1009.2559).
- [5] S. Alekhin et al., HERA and the LHC — a workshop on the implications of HERA for LHC physics: proceedings part A, [hep-ph/0601012](http://arxiv.org/abs/hep-ph/0601012) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/0601012).
- [6] T. Sj¨ostrand, S. Mrenna and P.Z. Skands, pythia 6.4 physics and manual, JHEP 05 [\(2006\)](http://dx.doi.org/10.1088/1126-6708/2006/05/026) [026](http://dx.doi.org/10.1088/1126-6708/2006/05/026) [[hep-ph/0603175](http://arxiv.org/abs/hep-ph/0603175)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/0603175).
- [7] T. Sj¨ostrand, S. Mrenna and P.Z. Skands, A brief introduction to pythia 8.1, [Comput. Phys.](http://dx.doi.org/10.1016/j.cpc.2008.01.036) Commun. 178 [\(2008\) 852](http://dx.doi.org/10.1016/j.cpc.2008.01.036) [[arXiv:0710.3820](http://arxiv.org/abs/0710.3820)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=0710.3820).
- [8] R. Corke, Multiple Interactions in pythia 8, [arXiv:0901.2852](http://arxiv.org/abs/0901.2852) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=0901.2852).
- [9] R. Field, Physics at the Tevatron, [Acta Phys. Polon.](http://th-www.if.uj.edu.pl/acta/vol39/abs/v39p2611.htm) B 39 (2008) 2611 [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?j=APPOA,B39,2611).
- [10] P. Bartalini (ed.) et al., Proceedings of the first international workshop on multiple partonic interactions at the LHC (MP I08), [arXiv:1003.4220](http://arxiv.org/abs/1003.4220) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1003.4220).
- [11] R. Field, Early LHC underlying event data — findings and surprises, [arXiv:1010.3558](http://arxiv.org/abs/1010.3558) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1010.3558).
- [12] P.Z. Skands and D. Wicke, Non-perturbative QCD effects and the top mass at the Tevatron, [Eur. Phys. J.](http://dx.doi.org/10.1140/epjc/s10052-007-0352-1) C 52 (2007) 133 [[hep-ph/0703081](http://arxiv.org/abs/hep-ph/0703081)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/0703081).
- [13] A. Buckley, H. Hoeth, H. Lacker, H. Schulz and J.E. von Seggern, Systematic event generator tuning for the LHC, [Eur. Phys. J.](http://dx.doi.org/10.1140/epjc/s10052-009-1196-7) C 65 (2010) 331 [[arXiv:0907.2973](http://arxiv.org/abs/0907.2973)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=0907.2973).

## PDF page 14

- [14] ATLAS collaboration, G. Aad et al., Charged-particle multiplicities in pp interactions measured with the ATLAS detector at the LHC, New J. Phys. 13 [\(2011\) 053033](http://dx.doi.org/10.1088/1367-2630/13/5/053033) [[arXiv:1012.5104](http://arxiv.org/abs/1012.5104)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1012.5104).
- [15] R. Corke and T. Sj¨ostrand, Interleaved parton showers and tuning prospects, [JHEP](http://dx.doi.org/10.1007/JHEP03(2011)032) 03 [\(2011\) 032](http://dx.doi.org/10.1007/JHEP03(2011)032) [[arXiv:1011.1759](http://arxiv.org/abs/1011.1759)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1011.1759).
- [16] S. Navin, Diffraction in pythia, [arXiv:1005.3894](http://arxiv.org/abs/1005.3894) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1005.3894).
- [17] J. Pumplin et al., New generation of parton distributions with uncertainties from global QCD analysis, JHEP 07 [\(2002\) 012](http://dx.doi.org/10.1088/1126-6708/2002/07/012) [[hep-ph/0201195](http://arxiv.org/abs/hep-ph/0201195)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/0201195).
- [18] CTEQ collaboration, H.L. Lai et al., Global QCD analysis of parton structure of the nucleon: CTEQ5 parton distributions, [Eur. Phys. J.](http://dx.doi.org/10.1007/s100529900196) C 12 (2000) 375 [[hep-ph/9903282](http://arxiv.org/abs/hep-ph/9903282)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/9903282).
- [19] CMS collaboration, S. Chatrchyan et al., The CMS experiment at the CERN LHC, [2008](http://dx.doi.org/10.1088/1748-0221/3/08/S08004) JINST 3 [S08004](http://dx.doi.org/10.1088/1748-0221/3/08/S08004) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?j=JINST,3,S08004).
- [20] A.J. Bell, The design and construction of the beam scintillation counter for CMS, Master's thesis, University of Canterbury, Christchurch New Zealand (2008) [\[CERN-THESIS-2009-062\]](http://cdsweb.cern.ch/record/1204301/files/CERN-THESIS-2009-062.pdf).
- [21] T. Aumeyr, Beam phase and intensity monitoring for the Compact Muon Solenoid experiment, Master's thesis, Vienna University of Technology, Vienna Austria (2008).
- [22] G.P. Salam and G. Soyez, A practical seedless infrared-safe cone jet algorithm, [JHEP](http://dx.doi.org/10.1088/1126-6708/2007/05/086) 05 [\(2007\) 086](http://dx.doi.org/10.1088/1126-6708/2007/05/086) [[arXiv:0704.0292](http://arxiv.org/abs/0704.0292)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=0704.0292).
- [23] M. Cacciari and G.P. Salam, Dispelling the N<sup>3</sup> myth for the k<sup>T</sup> jet-finder, [Phys. Lett.](http://dx.doi.org/10.1016/j.physletb.2006.08.037) B 641 [\(2006\) 57](http://dx.doi.org/10.1016/j.physletb.2006.08.037) [[hep-ph/0512210](http://arxiv.org/abs/hep-ph/0512210)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=HEP-PH/0512210).
- [24] CMS collaboration, V. Khachatryan et al., CMS tracking performance results from early LHC operation, [Eur. Phys. J.](http://dx.doi.org/10.1140/epjc/s10052-010-1491-3) C 70 (2010) 1165 [[arXiv:1007.1988](http://arxiv.org/abs/1007.1988)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1007.1988).
- [25] G. D'Agostini, A multidimensional unfolding method based on Bayes' theorem, [Nucl.](http://dx.doi.org/10.1016/0168-9002(95)00274-X) [Instrum. Meth.](http://dx.doi.org/10.1016/0168-9002(95)00274-X) A 362 (1995) 487 [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?j=NUIMA,A362,487).
- [26] GEANT4 collaboration, S. Agostinelli et al., GEANT4: a simulation toolkit, [Nucl. Instrum.](http://dx.doi.org/10.1016/S0168-9002(03)01368-8) Meth. A 506 [\(2003\) 250](http://dx.doi.org/10.1016/S0168-9002(03)01368-8) [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?j=NUIMA,A506,250).
- [27] A. Buckley et al., General-purpose event generators for LHC physics, [Phys. Rept.](http://dx.doi.org/10.1016/j.physrep.2011.03.005) 504 (2011) [145](http://dx.doi.org/10.1016/j.physrep.2011.03.005) [[arXiv:1101.2599](http://arxiv.org/abs/1101.2599)] [\[SPIRES\]](http://www-spires.slac.stanford.edu/spires/find/hep/www?eprint=1101.2599).

## PDF page 15

## The CMS collaboration

#### Yerevan Physics Institute, Yerevan, Armenia

S. Chatrchyan, V. Khachatryan, A.M. Sirunyan, A. Tumasyan

#### Institut f¨ur Hochenergiephysik der OeAW, Wien, Austria

W. Adam, T. Bergauer, M. Dragicevic, J. Er¨o, C. Fabjan, M. Friedl, R. Fr¨uhwirth, V.M. Ghete, J. Hammer<sup>1</sup> , S. H¨ansel, M. Hoch, N. H¨ormann, J. Hrubec, M. Jeitler, W. Kiesenhofer, M. Krammer, D. Liko, I. Mikulec, M. Pernicka, H. Rohringer, R. Sch¨ofbeck, J. Strauss, A. Taurok, F. Teischinger, P. Wagner, W. Waltenberger, G. Walzel, E. Widl, C.-E. Wulz

#### National Centre for Particle and High Energy Physics, Minsk, Belarus

V. Mossolov, N. Shumeiko, J. Suarez Gonzalez

#### Universiteit Antwerpen, Antwerpen, Belgium

- S. Bansal, L. Benucci, E.A. De Wolf, X. Janssen, J. Maes, T. Maes, L. Mucibello,
- S. Ochesanu, B. Roland, R. Rougny, M. Selvaggi, H. Van Haevermaet, P. Van Mechelen,
- N. Van Remortel

# Vrije Universiteit Brussel, Brussel, Belgium

F. Blekman, S. Blyweert, J. D'Hondt, O. Devroede, R. Gonzalez Suarez, A. Kalogeropoulos, M. Maes, W. Van Doninck, P. Van Mulders, G.P. Van Onsem, I. Villella

#### Universit´e Libre de Bruxelles, Bruxelles, Belgium

O. Charaf, B. Clerbaux, G. De Lentdecker, V. Dero, A.P.R. Gay, G.H. Hammad, T. Hreus, P.E. Marage, L. Thomas, C. Vander Velde, P. Vanlaer

#### Ghent University, Ghent, Belgium

V. Adler, A. Cimmino, S. Costantini, M. Grunewald, B. Klein, J. Lellouch, A. Marinov, J. Mccartin, D. Ryckbosch, F. Thyssen, M. Tytgat, L. Vanelderen, P. Verwilligen, S. Walsh, N. Zaganidis

#### Universit´e Catholique de Louvain, Louvain-la-Neuve, Belgium

- S. Basegmez, G. Bruno, J. Caudron, L. Ceard, E. Cortina Gil, J. De Favereau De Jeneret,
- C. Delaere<sup>1</sup> , D. Favart, A. Giammanco, G. Gr´egoire, J. Hollar, V. Lemaitre, J. Liao,
- O. Militaru, S. Ovyn, D. Pagano, A. Pin, K. Piotrzkowski, N. Schul

#### Universit´e de Mons, Mons, Belgium

N. Beliy, T. Caebergs, E. Daubie

#### Centro Brasileiro de Pesquisas Fisicas, Rio de Janeiro, Brazil

G.A. Alves, D. De Jesus Damiao, M.E. Pol, M.H.G. Souza

# Universidade do Estado do Rio de Janeiro, Rio de Janeiro, Brazil

W. Carvalho, E.M. Da Costa, C. De Oliveira Martins, S. Fonseca De Souza, L. Mundim, H. Nogima, V. Oguri, W.L. Prado Da Silva, A. Santoro, S.M. Silva Do Amaral, A. Sznajder

## PDF page 16

#### Instituto de Fisica Teorica, Universidade Estadual Paulista, Sao Paulo, Brazil

C.A. Bernardes<sup>2</sup> , F.A. Dias, T.R. Fernandez Perez Tomei, E. M. Gregores<sup>2</sup> , C. Lagana, F. Marinho, P.G. Mercadante<sup>2</sup> , S.F. Novaes, Sandra S. Padula

#### Institute for Nuclear Research and Nuclear Energy, Sofia, Bulgaria

N. Darmenov<sup>1</sup> , V. Genchev<sup>1</sup> , P. Iaydjiev<sup>1</sup> , S. Piperov, M. Rodozov, S. Stoykova, G. Sultanov, V. Tcholakov, R. Trayanov

#### University of Sofia, Sofia, Bulgaria

A. Dimitrov, R. Hadjiiska, A. Karadzhinova, V. Kozhuharov, L. Litov, M. Mateev, B. Pavlov, P. Petkov

#### Institute of High Energy Physics, Beijing, China

J.G. Bian, G.M. Chen, H.S. Chen, C.H. Jiang, D. Liang, S. Liang, X. Meng, J. Tao, J. Wang, J. Wang, X. Wang, Z. Wang, H. Xiao, M. Xu, J. Zang, Z. Zhang

# State Key Lab. of Nucl. Phys. and Tech., Peking University, Beijing, China

Y. Ban, S. Guo, Y. Guo, W. Li, Y. Mao, S.J. Qian, H. Teng, B. Zhu, W. Zou

#### Universidad de Los Andes, Bogota, Colombia

A. Cabrera, B. Gomez Moreno, A.A. Ocampo Rios, A.F. Osorio Oliveros, J.C. Sanabria

#### Technical University of Split, Split, Croatia

N. Godinovic, D. Lelas, K. Lelas, R. Plestina<sup>3</sup> , D. Polic, I. Puljak

#### University of Split, Split, Croatia

Z. Antunovic, M. Dzelalija

#### Institute Rudjer Boskovic, Zagreb, Croatia

V. Brigljevic, S. Duric, K. Kadija, S. Morovic

#### University of Cyprus, Nicosia, Cyprus

A. Attikis, M. Galanti, J. Mousa, C. Nicolaou, F. Ptochos, P.A. Razis

#### Charles University, Prague, Czech Republic

M. Finger, M. Finger Jr.

# Academy of Scientific Research and Technology of the Arab Republic of Egypt, Egyptian Network of High Energy Physics, Cairo, Egypt

Y. Assran<sup>4</sup> , S. Khalil<sup>5</sup> , M.A. Mahmoud<sup>6</sup>

#### National Institute of Chemical Physics and Biophysics, Tallinn, Estonia

A. Hektor, M. Kadastik, M. M¨untel, M. Raidal, L. Rebane

#### Department of Physics, University of Helsinki, Helsinki, Finland

V. Azzolini, P. Eerola, G. Fedi

#### Helsinki Institute of Physics, Helsinki, Finland

- S. Czellar, J. H¨ark¨onen, A. Heikkinen, V. Karim¨aki, R. Kinnunen, M.J. Kortelainen,
- T. Lamp´en, K. Lassila-Perini, S. Lehti, T. Lind´en, P. Luukka, T. M¨aenp¨a¨a, E. Tuominen,
- J. Tuominiemi, E. Tuovinen, D. Ungaro, L. Wendland

## PDF page 17

#### Lappeenranta University of Technology, Lappeenranta, Finland

K. Banzuzi, A. Korpela, T. Tuuva

# Laboratoire d'Annecy-le-Vieux de Physique des Particules, IN2P3-CNRS, Annecy-le-Vieux, France

D. Sillou

### DSM/IRFU, CEA/Saclay, Gif-sur-Yvette, France

- M. Besancon, S. Choudhury, M. Dejardin, D. Denegri, B. Fabbro, J.L. Faure, F. Ferri,
- S. Ganjour, F.X. Gentit, A. Givernaud, P. Gras, G. Hamel de Monchenault, P. Jarry,
- E. Locci, J. Malcles, M. Marionneau, L. Millischer, J. Rander, A. Rosowsky, I. Shreyber,
- M. Titov, P. Verrecchia

# Laboratoire Leprince-Ringuet, Ecole Polytechnique, IN2P3-CNRS, Palaiseau, France

S. Baffioni, F. Beaudette, L. Benhabib, L. Bianchini, M. Bluj<sup>7</sup> , C. Broutin, P. Busson, C. Charlot, T. Dahms, L. Dobrzynski, S. Elgammal, R. Granier de Cassagnac, M. Haguenauer, P. Min´e, C. Mironov, C. Ochando, P. Paganini, D. Sabes, R. Salerno, Y. Sirois, C. Thiebaux, B. Wyslouch<sup>8</sup> , A. Zabi

# Institut Pluridisciplinaire Hubert Curien, Universit´e de Strasbourg, Universit´e de Haute Alsace Mulhouse, CNRS/IN2P3, Strasbourg, France

J.-L. Agram<sup>9</sup> , J. Andrea, D. Bloch, D. Bodin, J.-M. Brom, M. Cardaci, E.C. Chabert, C. Collard, E. Conte<sup>9</sup> , F. Drouhin<sup>9</sup> , C. Ferro, J.-C. Fontaine<sup>9</sup> , D. Gel´e, U. Goerlach, S. Greder, P. Juillot, M. Karim<sup>9</sup> , A.-C. Le Bihan, Y. Mikami, P. Van Hove

# Centre de Calcul de l'Institut National de Physique Nucleaire et de Physique des Particules (IN2P3), Villeurbanne, France

F. Fassi, D. Mercier

# Universit´e de Lyon, Universit´e Claude Bernard Lyon 1, CNRS-IN2P3, Institut de Physique Nucl´eaire de Lyon, Villeurbanne, France

- C. Baty, S. Beauceron, N. Beaupere, M. Bedjidian, O. Bondu, G. Boudoul, D. Boumediene,
- H. Brun, J. Chasserat, R. Chierici, D. Contardo, P. Depasse, H. El Mamouni, J. Fay,
- S. Gascon, B. Ille, T. Kurca, T. Le Grand, M. Lethuillier, L. Mirabito, S. Perries, V. Sordini,
- S. Tosi, Y. Tschudi, P. Verdier

# Institute of High Energy Physics and Informatization, Tbilisi State University, Tbilisi, Georgia

D. Lomidze

#### RWTH Aachen University, I. Physikalisches Institut, Aachen, Germany

- G. Anagnostou, M. Edelhoff, L. Feld, N. Heracleous, O. Hindrichs, R. Jussen, K. Klein,
- J. Merz, N. Mohr, A. Ostapchuk, A. Perieanu, F. Raupach, J. Sammet, S. Schael,
- D. Sprenger, H. Weber, M. Weber, B. Wittmer

## PDF page 18

### RWTH Aachen University, III. Physikalisches Institut A, Aachen, Germany

- M. Ata, W. Bender, E. Dietz-Laursonn, M. Erdmann, J. Frangenheim, T. Hebbeker,
- A. Hinzmann, K. Hoepfner, T. Klimkovich, D. Klingebiel, P. Kreuzer, D. Lanske† ,
- C. Magass, M. Merschmeyer, A. Meyer, P. Papacz, H. Pieta, H. Reithler, S.A. Schmitz,
- L. Sonnenschein, J. Steggemann, D. Teyssier

#### RWTH Aachen University, III. Physikalisches Institut B, Aachen, Germany

- M. Bontenackels, M. Davids, M. Duda, G. Fl¨ugge, H. Geenen, M. Giffels, W. Haj Ahmad,
- D. Heydhausen, T. Kress, Y. Kuessel, A. Linn, A. Nowack, L. Perchalla, O. Pooth,
- J. Rennefeld, P. Sauerland, A. Stahl, M. Thomas, D. Tornier, M.H. Zoeller

#### Deutsches Elektronen-Synchrotron, Hamburg, Germany

- M. Aldaya Martin, W. Behrenhoff, U. Behrens, M. Bergholz10, A. Bethani, K. Borras,
- A. Cakir, A. Campbell, E. Castro, D. Dammann, G. Eckerlin, D. Eckstein, A. Floss-
- dorf, G. Flucke, A. Geiser, J. Hauk, H. Jung<sup>1</sup> , M. Kasemann, I. Katkov11, P. Katsas,
- C. Kleinwort, H. Kluge, A. Knutsson, M. Kr¨amer, D. Kr¨ucker, E. Kuznetsova, W. Lange,
- W. Lohmann10, R. Mankel, M. Marienfeld, I.-A. Melzer-Pellmann, A.B. Meyer, J. Mnich,
- A. Mussgiller, J. Olzem, A. Petrukhin, D. Pitzl, A. Raspereza, A. Raval, M. Rosin,
- R. Schmidt10, T. Schoerner-Sadenius, N. Sen, A. Spiridonov, M. Stein, J. Tomaszewska,
- R. Walsh, C. Wissing

#### University of Hamburg, Hamburg, Germany

- C. Autermann, V. Blobel, S. Bobrovskyi, J. Draeger, H. Enderle, U. Gebbert, K. Kaschube,
- G. Kaussen, R. Klanner, J. Lange, B. Mura, S. Naumann-Emme, F. Nowak, N. Pietsch,
- C. Sander, H. Schettler, P. Schleper, M. Schr¨oder, T. Schum, J. Schwandt, H. Stadie,
- G. Steinbr¨uck, J. Thomsen

#### Institut f¨ur Experimentelle Kernphysik, Karlsruhe, Germany

- C. Barth, J. Bauer, J. Berger, V. Buege, T. Chwalek, W. De Boer, A. Dierlamm, G. Dirkes,
- M. Feindt, J. Gruschke, C. Hackstein, F. Hartmann, M. Heinrich, H. Held, K.H. Hoffmann,
- S. Honc, J.R. Komaragiri, T. Kuhr, D. Martschei, S. Mueller, Th. M¨uller, M. Niegel,
- O. Oberst, A. Oehler, J. Ott, T. Peiffer, G. Quast, K. Rabbertz, F. Ratnikov, N. Ratnikova,
- M. Renz, C. Saout, A. Scheurer, P. Schieferdecker, F.-P. Schilling, G. Schott, H.J. Simonis, F.M. Stober, D. Troendle, J. Wagner-Kuhr, T. Weiler, M. Zeise, V. Zhukov11, E.B. Ziebarth
- Institute of Nuclear Physics "Demokritos", Aghia Paraskevi, Greece
- G. Daskalakis, T. Geralis, S. Kesisoglou, A. Kyriakis, D. Loukas, I. Manolakos, A. Markou,
- C. Markou, C. Mavrommatis, E. Ntomari, E. Petrakou

#### University of Athens, Athens, Greece

L. Gouskos, T.J. Mertzimekis, A. Panagiotou, E. Stiliaris

#### University of Io´annina, Io´annina, Greece

I. Evangelou, C. Foudas, P. Kokkas, N. Manthos, I. Papadopoulos, V. Patras, F.A. Triantis

#### KFKI Research Institute for Particle and Nuclear Physics, Budapest, Hungary

A. Aranyi, G. Bencze, L. Boldizsar, C. Hajdu<sup>1</sup> , P. Hidas, D. Horvath12, A. Kapusi, K. Krajczar13, F. Sikler<sup>1</sup> , G.I. Veres13, G. Vesztergombi<sup>13</sup>

## PDF page 19

#### Institute of Nuclear Research ATOMKI, Debrecen, Hungary

N. Beni, J. Molnar, J. Palinkas, Z. Szillasi, V. Veszpremi

#### University of Debrecen, Debrecen, Hungary

P. Raics, Z.L. Trocsanyi, B. Ujvari

# Panjab University, Chandigarh, India

S.B. Beri, V. Bhatnagar, N. Dhingra, R. Gupta, M. Jindal, M. Kaur, J.M. Kohli, M.Z. Mehta, N. Nishu, L.K. Saini, A. Sharma, A.P. Singh, J. Singh, S.P. Singh

## University of Delhi, Delhi, India

S. Ahuja, S. Bhattacharya, B.C. Choudhary, B. Gomber, P. Gupta, S. Jain, S. Jain, R. Khurana, A. Kumar, M. Naimuddin, K. Ranjan, R.K. Shivpuri

# Saha Institute of Nuclear Physics, Kolkata, India

S. Sarkar

#### Bhabha Atomic Research Centre, Mumbai, India

R.K. Choudhury, D. Dutta, S. Kailas, V. Kumar, P. Mehta, A.K. Mohanty<sup>1</sup> , L.M. Pant, P. Shukla

#### Tata Institute of Fundamental Research - EHEP, Mumbai, India

T. Aziz, M. Guchait14, A. Gurtu, M. Maity15, D. Majumder, G. Majumder, K. Mazumdar, G.B. Mohanty, A. Saha, K. Sudhakar, N. Wickramage

## Tata Institute of Fundamental Research - HECR, Mumbai, India

S. Banerjee, S. Dugad, N.K. Mondal

#### Institute for Research and Fundamental Sciences (IPM), Tehran, Iran

H. Arfaei, H. Bakhshiansohi16, S.M. Etesami, A. Fahim16, M. Hashemi, A. Jafari<sup>16</sup> , M. Khakzad, A. Mohammadi17, M. Mohammadi Najafabadi, S. Paktinat Mehdiabadi, B. Safarzadeh, M. Zeinali<sup>18</sup>

#### INFN Sezione di Bari <sup>a</sup> , Universit`a di Bari <sup>b</sup> , Politecnico di Bari <sup>c</sup> , Bari, Italy

M. Abbresciaa,b, L. Barbonea,b, C. Calabriaa,b, A. Colaleo<sup>a</sup> , D. Creanzaa,c, N. De Filippisa,c,<sup>1</sup> , M. De Palmaa,b, L. Fiore<sup>a</sup> , G. Iasellia,c, L. Lusitoa,b, G. Maggia,c, M. Maggi<sup>a</sup> , N. Mannaa,b, B. Marangellia,b, S. Mya,c, S. Nuzzoa,b, N. Pacificoa,b, G.A. Pierro<sup>a</sup> , A. Pompilia,b, G. Pugliesea,c, F. Romanoa,c, G. Rosellia,b, G. Selvaggia,b, L. Silvestris<sup>a</sup> ,

R. Trentadue<sup>a</sup> , S. Tupputia,b, G. Zito<sup>a</sup>

#### INFN Sezione di Bologna <sup>a</sup> , Universit`a di Bologna <sup>b</sup> , Bologna, Italy

G. Abbiendi<sup>a</sup> , A.C. Benvenuti<sup>a</sup> , D. Bonacorsi<sup>a</sup> , S. Braibant-Giacomellia,b, L. Brigliadori<sup>a</sup> ,

P. Capiluppia,b, A. Castroa,b, F.R. Cavallo<sup>a</sup> , M. Cuffiania,b, G.M. Dallavalle<sup>a</sup> , F. Fabbri<sup>a</sup> ,

A. Fanfania,b, D. Fasanella<sup>a</sup> , P. Giacomelli<sup>a</sup> , M. Giunta<sup>a</sup> , C. Grandi<sup>a</sup> , S. Marcellini<sup>a</sup> ,

G. Masetti<sup>b</sup> , M. Meneghellia,b, A. Montanari<sup>a</sup> , F.L. Navarriaa,b, F. Odorici<sup>a</sup> , A. Perrotta<sup>a</sup> ,

F. Primavera<sup>a</sup> , A.M. Rossia,b, T. Rovellia,b, G. Sirolia,b, R. Travaglinia,b

#### INFN Sezione di Catania <sup>a</sup> , Universit`a di Catania <sup>b</sup> , Catania, Italy

S. Albergoa,b, G. Cappelloa,b, M. Chiorbolia,b,<sup>1</sup> , S. Costaa,b, A. Tricomia,b, C. Tuvea,b

## PDF page 20

#### INFN Sezione di Firenze <sup>a</sup> , Universit`a di Firenze <sup>b</sup> , Firenze, Italy

G. Barbagli<sup>a</sup> , V. Ciullia,b, C. Civinini<sup>a</sup> , R. D'Alessandroa,b, E. Focardia,b, S. Frosalia,b , E. Gallo<sup>a</sup> , S. Gonzia,b, P. Lenzia,b, M. Meschini<sup>a</sup> , S. Paoletti<sup>a</sup> , G. Sguazzoni<sup>a</sup> , A. Tropianoa,<sup>1</sup>

#### INFN Laboratori Nazionali di Frascati, Frascati, Italy

L. Benussi, S. Bianco, S. Colafranceschi19, F. Fabbri, D. Piccolo

#### INFN Sezione di Genova, Genova, Italy

P. Fabbricatore, R. Musenich

#### INFN Sezione di Milano-Bicocca <sup>a</sup> , Universit`a di Milano-Bicocca <sup>b</sup> , Milano, Italy

A. Benagliaa,b, F. De Guioa,b,<sup>1</sup> , L. Di Matteoa,b, S. Gennai<sup>1</sup> , A. Ghezzia,b, S. Malvezzi<sup>a</sup> , A. Martellia,b, A. Massironia,b, D. Menasce<sup>a</sup> , L. Moroni<sup>a</sup> , M. Paganonia,b, D. Pedrini<sup>a</sup> , S. Ragazzia,b, N. Redaelli<sup>a</sup> , S. Sala<sup>a</sup> , T. Tabarelli de Fatisa,b

INFN Sezione di Napoli <sup>a</sup> , Universit`a di Napoli "Federico II" <sup>b</sup> , Napoli, Italy S. Buontempo<sup>a</sup> , C.A. Carrillo Montoyaa,<sup>1</sup> , N. Cavalloa,20, A. De Cosaa,b, F. Fabozzia,<sup>20</sup> , A.O.M. Iorioa,<sup>1</sup> , L. Lista<sup>a</sup> , M. Merolaa,b, P. Paolucci<sup>a</sup>

#### INFN Sezione di Padova <sup>a</sup> , Universit`a di Padova <sup>b</sup> , Universit`a di Trento (Trento) <sup>c</sup> , Padova, Italy

P. Azzi<sup>a</sup> , N. Bacchetta<sup>a</sup> , P. Bellana,b, D. Biselloa,b, A. Branca<sup>a</sup> , R. Carlina,b, P. Checchia<sup>a</sup> , M. De Mattiaa,b, T. Dorigo<sup>a</sup> , U. Dosselli<sup>a</sup> , F. Fanzago<sup>a</sup> , F. Gasparinia,b, U. Gasparinia,b , A. Gozzelino, S. Lacapraraa,21, I. Lazzizzeraa,c, M. Margonia,b, M. Mazzucato<sup>a</sup> , A.T. Meneguzzoa,b, M. Nespoloa,<sup>1</sup> , L. Perrozzia,<sup>1</sup> , N. Pozzobona,b, P. Ronchesea,b , F. Simonettoa,b, E. Torassa<sup>a</sup> , M. Tosia,b, S. Vaninia,b, P. Zottoa,b, G. Zumerlea,b

#### INFN Sezione di Pavia <sup>a</sup> , Universit`a di Pavia <sup>b</sup> , Pavia, Italy

P. Baessoa,b, U. Berzano<sup>a</sup> , S.P. Rattia,b, C. Riccardia,b, P. Torrea,b, P. Vituloa,b , C. Viviania,b

#### INFN Sezione di Perugia <sup>a</sup> , Universit`a di Perugia <sup>b</sup> , Perugia, Italy

M. Biasinia,b, G.M. Bilei<sup>a</sup> , B. Caponeria,b, L. Fan`oa,b, P. Laricciaa,b, A. Lucaronia,b,<sup>1</sup> , G. Mantovania,b, M. Menichelli<sup>a</sup> , A. Nappia,b, F. Romeoa,b, A. Santocchiaa,b, S. Taronia,b,<sup>1</sup> , M. Valdataa,b

#### INFN Sezione di Pisa <sup>a</sup> , Universit`a di Pisa <sup>b</sup> , Scuola Normale Superiore di Pisa <sup>c</sup> , Pisa, Italy

P. Azzurria,c, G. Bagliesi<sup>a</sup> , J. Bernardinia,b, T. Boccalia,<sup>1</sup> , G. Broccoloa,c, R. Castaldi<sup>a</sup> , R.T. D'Agnoloa,c, R. Dell'Orso<sup>a</sup> , F. Fioria,b, L. Fo`aa,c, A. Giassi<sup>a</sup> , A. Kraan<sup>a</sup> , F. Ligabuea,c, T. Lomtadze<sup>a</sup> , L. Martinia,22, A. Messineoa,b, F. Palla<sup>a</sup> , G. Segneri<sup>a</sup> , A.T. Serban<sup>a</sup> , P. Spagnolo<sup>a</sup> , R. Tenchini<sup>a</sup> , G. Tonellia,b,<sup>1</sup> , A. Venturia,<sup>1</sup> , P.G. Verdini<sup>a</sup>

#### INFN Sezione di Roma <sup>a</sup> , Universit`a di Roma "La Sapienza" <sup>b</sup> , Roma, Italy L. Baronea,b, F. Cavallari<sup>a</sup> , D. Del Rea,b, E. Di Marcoa,b, M. Diemoz<sup>a</sup> , D. Francia,b , M. Grassia,<sup>1</sup> , E. Longoa,b, S. Nourbakhsh<sup>a</sup> , G. Organtinia,b, F. Pandolfia,b,<sup>1</sup> , R. Paramatti<sup>a</sup> , S. Rahatloua,b, C. Rovelli<sup>1</sup>

## PDF page 21

#### INFN Sezione di Torino <sup>a</sup> , Universit`a di Torino <sup>b</sup> , Universit`a del Piemonte Orientale (Novara) <sup>c</sup> , Torino, Italy

N. Amapanea,b, R. Arcidiaconoa,c, S. Argiroa,b, M. Arneodoa,c, C. Biino<sup>a</sup> , C. Bottaa,b,<sup>1</sup> , N. Cartiglia<sup>a</sup> , R. Castelloa,b, M. Costaa,b, N. Demaria<sup>a</sup> , A. Grazianoa,b,<sup>1</sup> , C. Mariotti<sup>a</sup> , M. Maronea,b, S. Maselli<sup>a</sup> , E. Migliorea,b, G. Milaa,b, V. Monacoa,b, M. Musicha,b , M.M. Obertinoa,c, N. Pastrone<sup>a</sup> , M. Pelliccionia,b, A. Romeroa,b, M. Ruspaa,c, R. Sacchia,b , V. Solaa,b, A. Solanoa,b, A. Staiano<sup>a</sup> , A. Vilela Pereira<sup>a</sup>

#### INFN Sezione di Trieste <sup>a</sup> , Universit`a di Trieste <sup>b</sup> , Trieste, Italy

S. Belforte<sup>a</sup> , F. Cossutti<sup>a</sup> , G. Della Riccaa,b, B. Gobbo<sup>a</sup> , D. Montaninoa,b, A. Penzo<sup>a</sup>

#### Kangwon National University, Chunchon, Korea

S.G. Heo, S.K. Nam

#### Kyungpook National University, Daegu, Korea

S. Chang, J. Chung, D.H. Kim, G.N. Kim, J.E. Kim, D.J. Kong, H. Park, S.R. Ro, D. Son, D.C. Son, T. Son

# Chonnam National University, Institute for Universe and Elementary Particles, Kwangju, Korea

Zero Kim, J.Y. Kim, S. Song

# Korea University, Seoul, Korea

S. Choi, B. Hong, M.S. Jeong, M. Jo, H. Kim, J.H. Kim, T.J. Kim, K.S. Lee, D.H. Moon, S.K. Park, H.B. Rhee, E. Seo, S. Shin, K.S. Sim

#### University of Seoul, Seoul, Korea

M. Choi, S. Kang, H. Kim, C. Park, I.C. Park, S. Park, G. Ryu

#### Sungkyunkwan University, Suwon, Korea

Y. Choi, Y.K. Choi, J. Goh, M.S. Kim, E. Kwon, J. Lee, S. Lee, H. Seo, I. Yu

#### Vilnius University, Vilnius, Lithuania

M.J. Bilinskas, I. Grigelionis, M. Janulis, D. Martisiute, P. Petrov, T. Sabonis

#### Centro de Investigacion y de Estudios Avanzados del IPN, Mexico City, Mexico

H. Castilla-Valdez, E. De La Cruz-Burelo, I. Heredia-de La Cruz, R. Lopez-Fernandez,

R. Maga˜na Villalba, A. S´anchez-Hern´andez, L.M. Villasenor-Cendejas

#### Universidad Iberoamericana, Mexico City, Mexico

S. Carrillo Moreno, F. Vazquez Valencia

#### Benemerita Universidad Autonoma de Puebla, Puebla, Mexico

H.A. Salazar Ibarguen

#### Universidad Aut´onoma de San Luis Potos´ı, San Luis Potos´ı, Mexico

E. Casimiro Linares, A. Morelos Pineda, M.A. Reyes-Santos

#### University of Auckland, Auckland, New Zealand

D. Krofcheck, J. Tam

## PDF page 22

#### University of Canterbury, Christchurch, New Zealand

P.H. Butler, R. Doesburg, H. Silverwood

#### National Centre for Physics, Quaid-I-Azam University, Islamabad, Pakistan

M. Ahmad, I. Ahmed, M.I. Asghar, H.R. Hoorani, W.A. Khan, T. Khurshid, S. Qazi

# Institute of Experimental Physics, Faculty of Physics, University of Warsaw, Warsaw, Poland

G. Brona, M. Cwiok, W. Dominik, K. Doroba, A. Kalinowski, M. Konecki, J. Krolikowski

#### Soltan Institute for Nuclear Studies, Warsaw, Poland

T. Frueboes, R. Gokieli, M. G´orski, M. Kazana, K. Nawrocki, K. Romanowska-Rybinska, M. Szleper, G. Wrochna, P. Zalewski

# Laborat´orio de Instrumenta¸c˜ao e F´ısica Experimental de Part´ıculas, Lisboa, Portugal

N. Almeida, P. Bargassa, A. David, P. Faccioli, P.G. Ferreira Parracho, M. Gallinaro, P. Musella, A. Nayak, P.Q. Ribeiro, J. Seixas, J. Varela

#### Joint Institute for Nuclear Research, Dubna, Russia

I. Belotelov, P. Bunin, I. Golutvin, A. Kamenev, V. Karjavin, V. Konoplyanikov, G. Kozlov, A. Lanev, P. Moisenz, V. Palichik, V. Perelygin, S. Shmatov, V. Smirnov, A. Volodko, A. Zarubin

# Petersburg Nuclear Physics Institute, Gatchina (St Petersburg), Russia

V. Golovtsov, Y. Ivanov, V. Kim, P. Levchenko, V. Murzin, V. Oreshkin, I. Smirnov, V. Sulimov, L. Uvarov, S. Vavilov, A. Vorobyev, An. Vorobyev

#### Institute for Nuclear Research, Moscow, Russia

Yu. Andreev, A. Dermenev, S. Gninenko, N. Golubev, M. Kirsanov, N. Krasnikov, V. Matveev, A. Pashenkov, A. Toropin, S. Troitsky

#### Institute for Theoretical and Experimental Physics, Moscow, Russia

V. Epshteyn, V. Gavrilov, V. Kaftanov† , M. Kossov<sup>1</sup> , A. Krokhotin, N. Lychkovskaya, V. Popov, G. Safronov, S. Semenov, V. Stolin, E. Vlasov, A. Zhokin

#### Moscow State University, Moscow, Russia

E. Boos, M. Dubinin23, L. Dudko, A. Ershov, A. Gribushin, O. Kodolova, I. Lokhtin, A. Markina, S. Obraztsov, M. Perfilov, S. Petrushanko, L. Sarycheva, V. Savrin, A. Snigirev

#### P.N. Lebedev Physical Institute, Moscow, Russia

V. Andreev, M. Azarkin, I. Dremin, M. Kirakosyan, A. Leonidov, S.V. Rusakov, A. Vinogradov

# State Research Center of Russian Federation, Institute for High Energy Physics, Protvino, Russia

I. Azhgirey, S. Bitioukov, V. Grishin<sup>1</sup> , V. Kachanov, D. Konstantinov, A. Korablev, V. Krychkine, V. Petrov, R. Ryutin, S. Slabospitsky, A. Sobol, L. Tourtchanovitch, S. Troshin, N. Tyurin, A. Uzunian, A. Volkov

## PDF page 23

# University of Belgrade, Faculty of Physics and Vinca Institute of Nuclear Sciences, Belgrade, Serbia

P. Adzic24, M. Djordjevic, D. Krpic24, J. Milosevic

# Centro de Investigaciones Energ´eticas Medioambientales y Tecnol´ogicas (CIEMAT), Madrid, Spain

M. Aguilar-Benitez, J. Alcaraz Maestre, P. Arce, C. Battilana, E. Calvo, M. Cepeda, M. Cerrada, M. Chamizo Llatas, N. Colino, B. De La Cruz, A. Delgado Peris, C. Diez Pardos, D. Dom´ınguez V´azquez, C. Fernandez Bedoya, J.P. Fern´andez Ramos, A. Ferrando, J. Flix, M.C. Fouz, P. Garcia-Abia, O. Gonzalez Lopez, S. Goy Lopez, J.M. Hernandez, M.I. Josa, G. Merino, J. Puerta Pelayo, I. Redondo, L. Romero, J. Santaolalla, M.S. Soares, C. Willmott

#### Universidad Aut´onoma de Madrid, Madrid, Spain

C. Albajar, G. Codispoti, J.F. de Troc´oniz

## Universidad de Oviedo, Oviedo, Spain

J. Cuevas, J. Fernandez Menendez, S. Folgueras, I. Gonzalez Caballero, L. Lloret Iglesias, J.M. Vizan Garcia

# Instituto de F´ısica de Cantabria (IFCA), CSIC-Universidad de Cantabria, Santander, Spain

J.A. Brochero Cifuentes, I.J. Cabrillo, A. Calderon, S.H. Chuang, J. Duarte Campderros, M. Felcini25, M. Fernandez, G. Gomez, J. Gonzalez Sanchez, C. Jorda, P. Lobelle Pardo, A. Lopez Virto, J. Marco, R. Marco, C. Martinez Rivero, F. Matorras, F.J. Munoz Sanchez, J. Piedra Gomez26, T. Rodrigo, A.Y. Rodr´ıguez-Marrero, A. Ruiz-Jimeno, L. Scodellaro, M. Sobron Sanudo, I. Vila, R. Vilar Cortabitarte

# CERN, European Organization for Nuclear Research, Geneva, Switzerland

D. Abbaneo, E. Auffray, G. Auzinger, P. Baillon, A.H. Ball, D. Barney, A.J. Bell<sup>27</sup> , D. Benedetti, C. Bernet<sup>3</sup> , W. Bialas, P. Bloch, A. Bocci, S. Bolognesi, M. Bona, H. Breuker, K. Bunkowski, T. Camporesi, G. Cerminara, T. Christiansen, J.A. Coarasa Perez, B. Cur´e, D. D'Enterria, A. De Roeck, S. Di Guida, N. Dupont-Sagorin, A. Elliott-Peisert, B. Frisch, W. Funk, A. Gaddi, G. Georgiou, H. Gerwig, D. Gigi, K. Gill, D. Giordano, F. Glege, R. Gomez-Reino Garrido, M. Gouzevitch, P. Govoni, S. Gowdy, L. Guiducci, M. Hansen, C. Hartl, J. Harvey, J. Hegeman, B. Hegner, H.F. Hoffmann, A. Honma, V. Innocente, P. Janot, K. Kaadze, E. Karavakis, P. Lecoq, C. Louren¸co, T. M¨aki, M. Malberti, L. Malgeri, M. Mannelli, L. Masetti, A. Maurisset, F. Meijers, S. Mersi, E. Meschi, R. Moser, M.U. Mozer, M. Mulders, E. Nesvold<sup>1</sup> , M. Nguyen, T. Orimoto, L. Orsini, E. Perez, A. Petrilli, A. Pfeiffer, M. Pierini, M. Pimi¨a, D. Piparo, G. Polese, A. Racz, J. Rodrigues Antunes, G. Rolandi28, T. Rommerskirchen, M. Rovere, H. Sakulin, C. Sch¨afer, C. Schwick, I. Segoni, A. Sharma, P. Siegrist, P. Silva, M. Simon, P. Sphicas29, M. Spiropulu<sup>23</sup> , M. Stoye, M. Tadel, P. Tropea, A. Tsirou, P. Vichoudis, M. Voutilainen, W.D. Zeuner

## PDF page 24

#### Paul Scherrer Institut, Villigen, Switzerland

W. Bertl, K. Deiters, W. Erdmann, K. Gabathuler, R. Horisberger, Q. Ingram, H.C. Kaestli, S. K¨onig, D. Kotlinski, U. Langenegger, F. Meier, D. Renker, T. Rohe, J. Sibille30, A. Starodumov<sup>31</sup>

# Institute for Particle Physics, ETH Zurich, Zurich, Switzerland

- L. B¨ani, P. Bortignon, L. Caminada32, N. Chanon, Z. Chen, S. Cittolin, G. Dissertori,
- M. Dittmar, J. Eugster, K. Freudenreich, C. Grab, W. Hintz, P. Lecomte, W. Lustermann,
- C. Marchica32, P. Martinez Ruiz del Arbol, P. Meridiani, P. Milenovic33, F. Moortgat,
- C. N¨ageli32, P. Nef, F. Nessi-Tedaldi, L. Pape, F. Pauss, T. Punz, A. Rizzi, F.J. Ronga,
- M. Rossini, L. Sala, A.K. Sanchez, M.-C. Sawley, B. Stieger, L. Tauscher† , A. Thea,
- K. Theofilatos, D. Treille, C. Urscheler, R. Wallny, M. Weber, L. Wehrli, J. Weng

#### Universit¨at Z¨urich, Zurich, Switzerland

E. Aguilo, C. Amsler, V. Chiochia, S. De Visscher, C. Favaro, M. Ivova Rikova, B. Millan Mejias, P. Otiougova, C. Regenfus, P. Robmann, A. Schmidt, H. Snoek

# National Central University, Chung-Li, Taiwan

Y.H. Chang, K.H. Chen, S. Dutta, C.M. Kuo, S.W. Li, W. Lin, Z.K. Liu, Y.J. Lu, D. Mekterovic, R. Volpe, J.H. Wu, S.S. Yu

# National Taiwan University (NTU), Taipei, Taiwan

P. Bartalini, P. Chang, Y.H. Chang, Y.W. Chang, Y. Chao, K.F. Chen, W.-S. Hou, Y. Hsiung, K.Y. Kao, Y.J. Lei, R.-S. Lu, J.G. Shiu, Y.M. Tzeng, M. Wang

#### Cukurova University, Adana, Turkey

A. Adiguzel, M.N. Bakirci34, S. Cerci35, C. Dozen, I. Dumanoglu, E. Eskut, S. Girgis, G. Gokbulut, I. Hos, E.E. Kangal, A. Kayis Topaksu, G. Onengut, K. Ozdemir, S. Ozturk<sup>36</sup> , A. Polatoz, K. Sogut37, D. Sunar Cerci35, B. Tali35, H. Topakli34, D. Uzun, L.N. Vergili, M. Vergili

#### Middle East Technical University, Physics Department, Ankara, Turkey

I.V. Akin, T. Aliev, B. Bilin, S. Bilmis, M. Deniz, H. Gamsizkan, A.M. Guler, K. Ocalan, A. Ozpineci, M. Serin, R. Sever, U.E. Surat, E. Yildirim, M. Zeyrek

#### Bogazici University, Istanbul, Turkey

M. Deliomeroglu, D. Demir38, E. G¨ulmez, B. Isildak, M. Kaya39, O. Kaya39, M. Ozbek, ¨ S. Ozkorucuklu40, N. Sonmez<sup>41</sup>

# National Scientific Center, Kharkov Institute of Physics and Technology, Kharkov, Ukraine

L. Levchuk

#### University of Bristol, Bristol, United Kingdom

F. Bostock, J.J. Brooke, T.L. Cheng, E. Clement, D. Cussans, R. Frazier, J. Goldstein, M. Grimes, M. Hansen, D. Hartley, G.P. Heath, H.F. Heath, L. Kreczko, S. Metson, D.M. Newbold42, K. Nirunpong, A. Poll, S. Senkin, V.J. Smith, S. Ward

## PDF page 25

### Rutherford Appleton Laboratory, Didcot, United Kingdom

- L. Basso43, K.W. Bell, A. Belyaev43, C. Brew, R.M. Brown, B. Camanzi, D.J.A. Cockerill,
- J.A. Coughlan, K. Harder, S. Harper, J. Jackson, B.W. Kennedy, E. Olaiya, D. Petyt,
- B.C. Radburn-Smith, C.H. Shepherd-Themistocleous, I.R. Tomalin, W.J. Womersley, S.D. Worm

# Imperial College, London, United Kingdom

- R. Bainbridge, G. Ball, J. Ballin, R. Beuselinck, O. Buchmuller, D. Colling, N. Cripps,
- M. Cutajar, G. Davies, M. Della Negra, W. Ferguson, J. Fulcher, D. Futyan, A. Gilbert,
- A. Guneratne Bryer, G. Hall, Z. Hatherell, J. Hays, G. Iles, M. Jarvis, G. Karapostoli,
- L. Lyons, B.C. MacEvoy, A.-M. Magnan, J. Marrouche, B. Mathias, R. Nandi, J. Nash,
- A. Nikitenko31, A. Papageorgiou, M. Pesaresi, K. Petridis, M. Pioppi44, D.M. Raymond,
- S. Rogerson, N. Rompotis, A. Rose, M.J. Ryan, C. Seez, P. Sharp, A. Sparrow, A. Tapper,
- S. Tourneur, M. Vazquez Acosta, T. Virdee, S. Wakefield, N. Wardle, D. Wardrope,
- T. Whyntie

#### Brunel University, Uxbridge, United Kingdom

M. Barrett, M. Chadwick, J.E. Cole, P.R. Hobson, A. Khan, P. Kyberd, D. Leslie,

W. Martin, I.D. Reid, L. Teodorescu

## Baylor University, Waco, USA

K. Hatakeyama, H. Liu

#### Boston University, Boston, USA

T. Bose, E. Carrera Jarrin, C. Fantasia, A. Heister, J. St. John, P. Lawson, D. Lazic,

J. Rohlf, D. Sperka, L. Sulak

#### Brown University, Providence, USA

- A. Avetisyan, S. Bhattacharya, J.P. Chou, D. Cutts, A. Ferapontov, U. Heintz, S. Jabeen,
- G. Kukartsev, G. Landsberg, M. Luk, M. Narain, D. Nguyen, M. Segala, T. Sinthuprasith,
- T. Speer, K.V. Tsang

#### University of California, Davis, Davis, USA

- R. Breedon, M. Calderon De La Barca Sanchez, S. Chauhan, M. Chertok, J. Conway,
- P.T. Cox, J. Dolen, R. Erbacher, E. Friis, W. Ko, A. Kopecky, R. Lander, H. Liu,
- S. Maruyama, T. Miceli, M. Nikolic, D. Pellett, J. Robles, S. Salur, T. Schwarz, M. Searle,
- J. Smith, M. Squires, M. Tripathi, R. Vasquez Sierra, C. Veelken

#### University of California, Los Angeles, Los Angeles, USA

V. Andreev, K. Arisaka, D. Cline, R. Cousins, A. Deisher, J. Duris, S. Erhan, C. Farrell,

J. Hauser, M. Ignatenko, C. Jarvis, C. Plager, G. Rakness, P. Schlein† , J. Tucker, V. Valuev

#### University of California, Riverside, Riverside, USA

- J. Babb, A. Chandra, R. Clare, J. Ellison, J.W. Gary, F. Giordano, G. Hanson, G.Y. Jeng,
- S.C. Kao, F. Liu, H. Liu, O.R. Long, A. Luthra, H. Nguyen, B.C. Shen† , R. Stringer,
- J. Sturdy, S. Sumowidagdo, R. Wilken, S. Wimpenny

## PDF page 26

### University of California, San Diego, La Jolla, USA

W. Andrews, J.G. Branson, G.B. Cerati, D. Evans, F. Golf, A. Holzner, R. Kelley, M. Lebourgeois, J. Letts, B. Mangano, S. Padhi, C. Palmer, G. Petrucciani, H. Pi, M. Pieri, R. Ranieri, M. Sani, V. Sharma, S. Simon, E. Sudano, Y. Tu, A. Vartak, S. Wasserbaech<sup>45</sup> , F. W¨urthwein, A. Yagil, J. Yoo

#### University of California, Santa Barbara, Santa Barbara, USA

D. Barge, R. Bellan, C. Campagnari, M. D'Alfonso, T. Danielson, K. Flowers, P. Geffert, J. Incandela, C. Justus, P. Kalavase, S.A. Koay, D. Kovalskyi, V. Krutelyov, S. Lowette, N. Mccoll, V. Pavlunin, F. Rebassoo, J. Ribnik, J. Richman, R. Rossin, D. Stuart, W. To, J.R. Vlimant

#### California Institute of Technology, Pasadena, USA

A. Apresyan, A. Bornheim, J. Bunn, Y. Chen, M. Gataullin, Y. Ma, A. Mott, H.B. Newman, C. Rogan, K. Shin, V. Timciuc, P. Traczyk, J. Veverka, R. Wilkinson, Y. Yang, R.Y. Zhu

#### Carnegie Mellon University, Pittsburgh, USA

B. Akgun, R. Carroll, T. Ferguson, Y. Iiyama, D.W. Jang, S.Y. Jun, Y.F. Liu, M. Paulini, J. Russ, H. Vogel, I. Vorobiev

#### University of Colorado at Boulder, Boulder, USA

J.P. Cumalat, M.E. Dinardo, B.R. Drell, C.J. Edelmaier, W.T. Ford, A. Gaz, B. Heyburn, E. Luiggi Lopez, U. Nauenberg, J.G. Smith, K. Stenson, K.A. Ulmer, S.R. Wagner, S.L. Zang

#### Cornell University, Ithaca, USA

L. Agostino, J. Alexander, D. Cassel, A. Chatterjee, S. Das, N. Eggert, L.K. Gibbons, B. Heltsley, W. Hopkins, A. Khukhunaishvili, B. Kreis, G. Nicolas Kaufman, J.R. Patterson, D. Puigh, A. Ryd, E. Salvati, X. Shi, W. Sun, W.D. Teo, J. Thom, J. Thompson, J. Vaughan, Y. Weng, L. Winstrom, P. Wittich

#### Fairfield University, Fairfield, USA

A. Biselli, G. Cirino, D. Winn

#### Fermi National Accelerator Laboratory, Batavia, USA

S. Abdullin, M. Albrow, J. Anderson, G. Apollinari, M. Atac, J.A. Bakken, S. Banerjee, L.A.T. Bauerdick, A. Beretvas, J. Berryhill, P.C. Bhat, I. Bloch, F. Borcherding, K. Burkett, J.N. Butler, V. Chetluru, H.W.K. Cheung, F. Chlebana, S. Cihangir, W. Cooper, D.P. Eartly, V.D. Elvira, S. Esen, I. Fisk, J. Freeman, Y. Gao, E. Gottschalk, D. Green, K. Gunthoti, O. Gutsche, J. Hanlon, R.M. Harris, J. Hirschauer, B. Hooberman, H. Jensen, M. Johnson, U. Joshi, R. Khatiwada, B. Klima, K. Kousouris, S. Kunori, S. Kwan, C. Leonidopoulos, P. Limon, D. Lincoln, R. Lipton, J. Lykken, K. Maeshima, J.M. Marraffino, D. Mason, P. McBride, T. Miao, K. Mishra, S. Mrenna, Y. Musienko46, C. Newman-Holmes, V. O'Dell, R. Pordes, O. Prokofyev, N. Saoulidou, E. Sexton-Kennedy, S. Sharma, W.J. Spalding, L. Spiegel, P. Tan, L. Taylor, S. Tkaczyk, L. Uplegger, E.W. Vaandering, R. Vidal, J. Whitmore, W. Wu, F. Yang, F. Yumiceva, J.C. Yun

## PDF page 27

#### University of Florida, Gainesville, USA

- D. Acosta, P. Avery, D. Bourilkov, M. Chen, M. De Gruttola, G.P. Di Giovanni, D. Dobur,
- A. Drozdetskiy, R.D. Field, M. Fisher, Y. Fu, I.K. Furic, J. Gartner, B. Kim, J. Konigsberg,
- A. Korytov, A. Kropivnitskaya, T. Kypreos, K. Matchev, G. Mitselmakher, L. Muniz,
- C. Prescott, R. Remington, M. Schmitt, B. Scurlock, P. Sellers, N. Skhirtladze, M. Snowball, D. Wang, J. Yelton, M. Zakaria

# Florida International University, Miami, USA

C. Ceron, V. Gaultney, L. Kramer, L.M. Lebolo, S. Linn, P. Markowitz, G. Martinez, D. Mesa, J.L. Rodriguez

#### Florida State University, Tallahassee, USA

- T. Adams, A. Askew, J. Bochenek, J. Chen, B. Diamond, S.V. Gleyzer, J. Haas,
- S. Hagopian, V. Hagopian, M. Jenkins, K.F. Johnson, H. Prosper, L. Quertenmont,
- S. Sekmen, V. Veeraraghavan

#### Florida Institute of Technology, Melbourne, USA

M.M. Baarmand, B. Dorney, S. Guragain, M. Hohlmann, H. Kalakhety, R. Ralich, I. Vodopiyanov

#### University of Illinois at Chicago (UIC), Chicago, USA

M.R. Adams, I.M. Anghel, L. Apanasevich, Y. Bai, V.E. Bazterra, R.R. Betts, J. Callner, R. Cavanaugh, C. Dragoiu, L. Gauthier, C.E. Gerber, S. Hamdan, D.J. Hofman, S. Khalatyan, G.J. Kunde47, F. Lacroix, M. Malek, C. O'Brien, C. Silvestre, A. Smoron, D. Strom, N. Varelas

#### The University of Iowa, Iowa City, USA

- U. Akgun, E.A. Albayrak, B. Bilki, W. Clarida, F. Duru, C.K. Lae, E. McCliment, J.-
- P. Merlo, H. Mermerkaya48, A. Mestvirishvili, A. Moeller, J. Nachtman, C.R. Newsom,
- E. Norbeck, J. Olson, Y. Onel, F. Ozok, S. Sen, J. Wetzel, T. Yetkin, K. Yi

#### Johns Hopkins University, Baltimore, USA

B.A. Barnett, B. Blumenfeld, A. Bonato, C. Eskew, D. Fehling, G. Giurgiu, A.V. Gritsan, Z.J. Guo, G. Hu, P. Maksimovic, S. Rappoccio, M. Swartz, N.V. Tran, A. Whitbeck

#### The University of Kansas, Lawrence, USA

P. Baringer, A. Bean, G. Benelli, O. Grachov, R.P. Kenny Iii, M. Murray, D. Noonan, S. Sanders, J.S. Wood, V. Zhukova

#### Kansas State University, Manhattan, USA

A.F. Barfuss, T. Bolton, I. Chakaberia, A. Ivanov, S. Khalil, M. Makouski, Y. Maravin, S. Shrestha, I. Svintradze, Z. Wan

#### Lawrence Livermore National Laboratory, Livermore, USA

J. Gronberg, D. Lange, D. Wright

## PDF page 28

#### University of Maryland, College Park, USA

A. Baden, M. Boutemeur, S.C. Eno, D. Ferencek, J.A. Gomez, N.J. Hadley, R.G. Kellogg, M. Kirn, Y. Lu, A.C. Mignerey, K. Rossato, P. Rumerio, F. Santanastasio, A. Skuja, J. Temple, M.B. Tonjes, S.C. Tonwar, E. Twedt

# Massachusetts Institute of Technology, Cambridge, USA

- B. Alver, G. Bauer, J. Bendavid, W. Busza, E. Butz, I.A. Cali, M. Chan, V. Dutta, P. Everaerts, G. Gomez Ceballos, M. Goncharov, K.A. Hahn, P. Harris, Y. Kim, M. Klute, Y.-J. Lee, W. Li, C. Loizides, P.D. Luckey, T. Ma, S. Nahn, C. Paus, D. Ralph, C. Roland,
- G. Roland, M. Rudolph, G.S.F. Stephans, F. St¨ockli, K. Sumorok, K. Sung, E.A. Wenger,
- R. Wolf, S. Xie, M. Yang, Y. Yilmaz, A.S. Yoon, M. Zanetti

#### University of Minnesota, Minneapolis, USA

S.I. Cooper, P. Cushman, B. Dahmes, A. De Benedetti, P.R. Dudero, G. Franzoni, J. Haupt, K. Klapoetke, Y. Kubota, J. Mans, V. Rekovic, R. Rusack, M. Sasseville, A. Singovsky, N. Tambe

## University of Mississippi, University, USA

L.M. Cremaldi, R. Godang, R. Kroeger, L. Perera, R. Rahmat, D.A. Sanders, D. Summers

#### University of Nebraska-Lincoln, Lincoln, USA

K. Bloom, S. Bose, J. Butt, D.R. Claes, A. Dominguez, M. Eads, J. Keller, T. Kelly, I. Kravchenko, J. Lazo-Flores, H. Malbouisson, S. Malik, G.R. Snow

#### State University of New York at Buffalo, Buffalo, USA

U. Baur, A. Godshalk, I. Iashvili, S. Jain, A. Kharchilava, A. Kumar, S.P. Shipkowski, K. Smith

#### Northeastern University, Boston, USA

G. Alverson, E. Barberis, D. Baumgartel, O. Boeriu, M. Chasco, S. Reucroft, J. Swain, D. Trocino, D. Wood, J. Zhang

#### Northwestern University, Evanston, USA

A. Anastassov, A. Kubik, N. Odell, R.A. Ofierzynski, B. Pollack, A. Pozdnyakov, M. Schmitt, S. Stoynev, M. Velasco, S. Won

#### University of Notre Dame, Notre Dame, USA

- L. Antonelli, D. Berry, A. Brinkerhoff, M. Hildreth, C. Jessop, D.J. Karmgard, J. Kolb,
- T. Kolberg, K. Lannon, W. Luo, S. Lynch, N. Marinelli, D.M. Morse, T. Pearson, R. Ruchti,
- J. Slaunwhite, N. Valls, M. Wayne, J. Ziegler

#### The Ohio State University, Columbus, USA

B. Bylsma, L.S. Durkin, J. Gu, C. Hill, P. Killewald, K. Kotov, T.Y. Ling, M. Rodenburg, G. Williams

#### Princeton University, Princeton, USA

- N. Adam, E. Berry, P. Elmer, D. Gerbaudo, V. Halyo, P. Hebda, A. Hunt, J. Jones,
- E. Laird, D. Lopes Pegna, D. Marlow, T. Medvedeva, M. Mooney, J. Olsen, P. Pirou´e,
- X. Quan, H. Saka, D. Stickland, C. Tully, J.S. Werner, A. Zuranski

## PDF page 29

#### University of Puerto Rico, Mayaguez, USA

J.G. Acosta, X.T. Huang, A. Lopez, H. Mendez, S. Oliveros, J.E. Ramirez Vargas, A. Zatserklyaniy

## Purdue University, West Lafayette, USA

E. Alagoz, V.E. Barnes, G. Bolla, L. Borrello, D. Bortoletto, A. Everett, A.F. Garfinkel, L. Gutay, Z. Hu, M. Jones, O. Koybasi, M. Kress, A.T. Laasanen, N. Leonardo, C. Liu, V. Maroussov, P. Merkel, D.H. Miller, N. Neumeister, I. Shipsey, D. Silvers, A. Svyatkovskiy, H.D. Yoo, J. Zablocki, Y. Zheng

# Purdue University Calumet, Hammond, USA

P. Jindal, N. Parashar

#### Rice University, Houston, USA

C. Boulahouache, V. Cuplov, K.M. Ecklund, F.J.M. Geurts, B.P. Padley, R. Redjimi, J. Roberts, J. Zabel

## University of Rochester, Rochester, USA

- B. Betchart, A. Bodek, Y.S. Chung, R. Covarelli, P. de Barbaro, R. Demina, Y. Eshaq,
- H. Flacher, A. Garcia-Bellido, P. Goldenzweig, Y. Gotra, J. Han, A. Harel, D.C. Miner,
- D. Orbaker, G. Petrillo, D. Vishnevskiy, M. Zielinski

#### The Rockefeller University, New York, USA

A. Bhatti, R. Ciesielski, L. Demortier, K. Goulianos, G. Lungu, S. Malik, C. Mesropian, M. Yan

#### Rutgers, the State University of New Jersey, Piscataway, USA

- O. Atramentov, A. Barker, D. Duggan, Y. Gershtein, R. Gray, E. Halkiadakis, D. Hidas,
- D. Hits, A. Lath, S. Panwalkar, R. Patel, A. Richards, K. Rose, S. Schnetzer, S. Somalwar,
- R. Stone, S. Thomas

#### University of Tennessee, Knoxville, USA

G. Cerizza, M. Hollingsworth, S. Spanier, Z.C. Yang, A. York

#### Texas A&M University, College Station, USA

R. Eusebi, W. Flanagan, J. Gilmore, A. Gurrola, T. Kamon, V. Khotilovich, R. Montalvo, I. Osipenkov, Y. Pakhotin, J. Pivarski, A. Safonov, S. Sengupta, A. Tatarinov, D. Toback, M. Weinberger

#### Texas Tech University, Lubbock, USA

N. Akchurin, C. Bardak, J. Damgov, C. Jeong, K. Kovitanggoon, S.W. Lee, P. Mane, Y. Roh, A. Sill, I. Volobouev, R. Wigmans, E. Yazgan

## Vanderbilt University, Nashville, USA

E. Appelt, E. Brownson, D. Engh, C. Florez, W. Gabella, M. Issah, W. Johns, P. Kurt, C. Maguire, A. Melo, P. Sheldon, B. Snook, S. Tuo, J. Velkovska

## PDF page 30

#### University of Virginia, Charlottesville, USA

M.W. Arenton, M. Balazs, S. Boutle, B. Cox, B. Francis, R. Hirosky, A. Ledovskoy, C. Lin, C. Neu, R. Yohay

# Wayne State University, Detroit, USA

S. Gollapinni, R. Harr, P.E. Karchin, P. Lamichhane, M. Mattson, C. Milst`ene, A. Sakharov

# University of Wisconsin, Madison, USA

- M. Anderson, M. Bachtis, J.N. Bellinger, D. Carlsmith, S. Dasu, J. Efron, K. Flood,
- L. Gray, K.S. Grogg, M. Grothe, R. Hall-Wilton, M. Herndon, A. Herv´e, P. Klabbers,
- J. Klukas, A. Lanaro, C. Lazaridis, J. Leonard, R. Loveless, A. Mohapatra, F. Palmonari,
- D. Reeder, I. Ross, A. Savin, W.H. Smith, J. Swanson, M. Weinberg
- †: Deceased
- 1: Also at CERN, European Organization for Nuclear Research, Geneva, Switzerland
- 2: Also at Universidade Federal do ABC, Santo Andre, Brazil
- 3: Also at Laboratoire Leprince-Ringuet, Ecole Polytechnique, IN2P3-CNRS, Palaiseau, France
- 4: Also at Suez Canal University, Suez, Egypt
- 5: Also at British University, Cairo, Egypt
- 6: Also at Fayoum University, El-Fayoum, Egypt
- 7: Also at Soltan Institute for Nuclear Studies, Warsaw, Poland
- 8: Also at Massachusetts Institute of Technology, Cambridge, USA
- 9: Also at Universit´e de Haute-Alsace, Mulhouse, France
- 10: Also at Brandenburg University of Technology, Cottbus, Germany
- 11: Also at Moscow State University, Moscow, Russia
- 12: Also at Institute of Nuclear Research ATOMKI, Debrecen, Hungary
- 13: Also at E¨otv¨os Lor´and University, Budapest, Hungary
- 14: Also at Tata Institute of Fundamental Research HECR, Mumbai, India
- 15: Also at University of Visva-Bharati, Santiniketan, India
- 16: Also at Sharif University of Technology, Tehran, Iran
- 17: Also at Shiraz University, Shiraz, Iran
- 18: Also at Isfahan University of Technology, Isfahan, Iran
- 19: Also at Facolt`a Ingegneria Universit`a di Roma, Roma, Italy
- 20: Also at Universit`a della Basilicata, Potenza, Italy
- 21: Also at Laboratori Nazionali di Legnaro dell' INFN, Legnaro, Italy
- 22: Also at Universit`a degli studi di Siena, Siena, Italy
- 23: Also at California Institute of Technology, Pasadena, USA
- 24: Also at Faculty of Physics of University of Belgrade, Belgrade, Serbia
- 25: Also at University of California, Los Angeles, Los Angeles, USA
- 26: Also at University of Florida, Gainesville, USA
- 27: Also at Universit´e de Gen`eve, Geneva, Switzerland
- 28: Also at Scuola Normale e Sezione dell' INFN, Pisa, Italy
- 29: Also at University of Athens, Athens, Greece
- 30: Also at The University of Kansas, Lawrence, USA
- 31: Also at Institute for Theoretical and Experimental Physics, Moscow, Russia
- 32: Also at Paul Scherrer Institut, Villigen, Switzerland
- 33: Also at University of Belgrade, Faculty of Physics and Vinca Institute of Nuclear Sciences, Belgrade, Serbia

## PDF page 31

- 34: Also at Gaziosmanpasa University, Tokat, Turkey
- 35: Also at Adiyaman University, Adiyaman, Turkey
- 36: Also at The University of Iowa, Iowa City, USA
- 37: Also at Mersin University, Mersin, Turkey
- 38: Also at Izmir Institute of Technology, Izmir, Turkey
- 39: Also at Kafkas University, Kars, Turkey
- 40: Also at Suleyman Demirel University, Isparta, Turkey
- 41: Also at Ege University, Izmir, Turkey
- 42: Also at Rutherford Appleton Laboratory, Didcot, United Kingdom
- 43: Also at School of Physics and Astronomy, University of Southampton, Southampton, United Kingdom
- 44: Also at INFN Sezione di Perugia; Universit`a di Perugia, Perugia, Italy
- 45: Also at Utah Valley University, Orem, USA
- 46: Also at Institute for Nuclear Research, Moscow, Russia
- 47: Also at Los Alamos National Laboratory, Los Alamos, USA
- 48: Also at Erzincan University, Erzincan, Turkey
