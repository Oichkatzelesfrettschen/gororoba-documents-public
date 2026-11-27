Source: https://doi.org/10.3847/2515-5172/ac9408
PDF sha256: 516d18e860bf48c9e7448f6cfcc7c5d10b3d18460263de58e24a84bbb0973491
License: CC-BY-4.0
Language: eng
Fidelity: machine-gated

# Transcription of perez_2022_breakthrough_listen_search_wow_signal.pdf

Transcription of `perez_2022_breakthrough_listen_search_wow_signal.pdf` in this directory, 4 pages; each `## PDF page` heading marks a page of the PDF.

Method: Marker 1.10.2 (surya-ocr 0.17.1 on CUDA) over the whole PDF; formulas are LaTeX between `$` signs. Display equations are machine output, so the PDF is the authority for every quotation. The earlier transcription is in this file's history.

## PDF page 1

#### **AAS-PROVIDED PDF • OPEN ACCESS**

# Breakthrough Listen Search for the WOW! Signal\*

To cite this article: Karen I. Perez et al 2022 Res. Notes AAS 6 197

Manuscript version: AAS-Provided PDF

This AAS-Provided PDF is **©** 2022 **The Author(s). Published by the American Astronomical Society**.

Original content from this work may be used under the terms of the Creative Commons Attribution 4.0 licence. Any further distribution of this work must maintain attribution to the author(s) and the title of the work, journal citation and DOI.

Everyone is permitted to use all or part of the original content in this article, provided that they adhere to all the terms of the licence <https://creativecommons.org/licences/by/4.0>

Before using any content from this article, please refer to the Version of Record on IOPscience once published for full citation and copyright details, as permissions may be required.

View the [article online](https://doi.org/10.3847/2515-5172/ac9408) for updates and enhancements.

## PDF page 2

## Breakthrough Listen Search for the WOW! Signal[∗](#page-1-0)

[Karen I. Perez,](http://orcid.org/0000-0002-6341-4548) <sup>1</sup> [Wael Farah,](http://orcid.org/0000-0002-0161-7243) <sup>2</sup> [Sofia Z. Sheikh,](http://orcid.org/0000-0001-7057-4999) <sup>2</sup> [Steve Croft,](http://orcid.org/0000-0003-4823-129X) 3, 2 [Andrew Siemion,](http://orcid.org/0000-0003-2828-7720) 3, 2, 4, 5 [Alexander W. Pollak,](http://orcid.org/0000-0002-3430-7671) 2 Bryan Brzycki,<sup>3</sup> Luigi F. Cruz,<sup>2</sup> [Daniel Czech,](http://orcid.org/0000-0002-8071-6011) <sup>3</sup> [David DeBoer,](http://orcid.org/0000-0003-3197-2294) 3 Jamie Drew,<sup>6</sup> [Vishal Gajjar,](http://orcid.org/0000-0002-8604-106X) <sup>3</sup> Michael A. Garrett,4, 7 [Howard Isaacson,](http://orcid.org/0000-0002-0531-1073) 3, 8 Matt Lebofsky,<sup>3</sup> David H. E. MacMahon,<sup>3</sup> [Pranav H. Premnath,](http://orcid.org/0000-0001-5728-4735) 2 Imke de Pater,<sup>3</sup> [Danny C. Price,](http://orcid.org/0000-0003-2783-1608) 9, 3 Sarah Schoultz,<sup>2</sup> Bart S. Wlodarczyk-Sroka,<sup>4</sup> Jill Tarter,<sup>2</sup> and S. Pete Worden<sup>6</sup>

Department of Astronomy, Columbia University, 550 West 120th Street, New York, NY 10027, USA SETI Institute, 339 Bernardo Ave Suite 200 Mountain View, CA 94043 Department of Astronomy, University of California, Berkeley, Berkeley, CA 94720 Jodrell Bank Centre for Astrophysics, Department of Physics and Astronomy, The University of Manchester, Manchester, M13 9PL, UK University of Malta, Institute of Space Sciences and Astronomy The Breakthrough Initiatives, NASA Research Park, Bld. 18, Moffett Field, CA, 94035, USA Leiden Observatory, Leiden University, PO Box 9513, 2300 RA Leiden, The Netherlands Centre for Astrophysics, University of Southern Queensland, Toowoomba, QLD, Australia 9 International Centre for Radio Astronomy Research, Curtin University, 1 Turner Ave, Bentley, WA, Australia 6104

#### ABSTRACT

[Caballero](#page-3-0) [\(2022\)](#page-3-0) identified the star 2MASS 19281982-2640123 as a potential Sun-like star from which the WOW! signal could have originated. We conducted a search for artificial narrowband (2.79 Hz / 1.91 Hz), drifting (±4 Hz s<sup>−</sup><sup>1</sup> ) technosignatures from this source using the turboSETI [\(Enriquez et al.](#page-3-1) [2017\)](#page-3-1) pipeline, from 1–2 GHz, using simultaneous multi-telescope observations with both the Robert C. Byrd Green Bank Telescope (GBT) and the newly refurbished Allen Telescope Array (ATA) on 2022 May 21. Both telescope observations had an overlap of 580 s. While blind searches using radio telescopes have been conducted in the general field of view in which the WOW! signal was first detected, this is the first time a targeted search has been done. No technosignature candidates were detected.

Keywords: radio astronomy, Search for Extraterrestrial Intelligence (SETI), technosignatures, astrobiology INTRODUCTION

The WOW! Signal was a bright anomaly detected in the radio spectrum on 1977 August 15 by the Ohio State University's Big Ear radio telescope [\(Kraus](#page-3-2) [1979\)](#page-3-2). It was observed near the 21-cm hydrogen line at 1420.4556 ± 0.005 MHz [\(Ehman](#page-3-3) [1998\)](#page-3-3), lasted for 72 seconds, and has not been redetected in subsequent observing campaigns (e.g., [Gray](#page-3-4) [1994;](#page-3-4) [Harp et al.](#page-3-5) [2020\)](#page-3-5). The telescope's two feed horn design introduces a degeneracy, such that it is not known in which horn the signal was detected.

Using data from the Gaia archive, [Caballero](#page-3-0) [\(2022\)](#page-3-0) identified a Sun-like star within the WOW! Signal region. The author used effective temperature (4450 K < Teff < 6000 K), radius (0.83 < R<sup>⊙</sup> < 1.15), and luminosity (0.34 < L<sup>⊙</sup> < 1.5) thresholds on the thousands of Gaia objects located inside the horns' span and found 38 and 28 K- and G-type stars for the positive and negative horns, respectively. Only one of these is Sun-like: 2MASS 19281982-2640123. According to Gaia DR2, this star has an estimated temperature of Teff = 5783 K, a radius of 0.9965662 R⊙, and a luminosity of 1.0007366 L<sup>⊙</sup> [\(Gaia Collaboration et al.](#page-3-6) [2016a,](#page-3-6) [2018\)](#page-3-7).

We describe observations and analysis of 2MASS 19281982-2640123 using both the GBT and the ATA as part of the Breakthrough Listen (BL) search for technosignatures [\(Worden et al.](#page-3-8) [2017;](#page-3-8) [Isaacson et al.](#page-3-9) [2017;](#page-3-9) [Gajjar et al.](#page-3-10) [2019\)](#page-3-10). Following the signal verification framework developed from BL's first signal-of-interest [\(Sheikh et al.](#page-3-11) [2020;](#page-3-11) [Smith et al.](#page-3-12) [2021\)](#page-3-12), these simultaneous observations represent an attempt to prepare for verification in the case that future candidate technosignatures are identified by either telescope individually.

Corresponding author: Karen Perez [karen.i.perez@columbia.edu](mailto: karen.i.perez@columbia.edu)

<sup>∗</sup> Dedicated to the memory of Bart S. Wlodarczyk-Sroka

## PDF page 3

#### OBSERVATIONS

### GBT

We observed 2MASS 19281982-2640123 with the GBT beginning on UT 2022 May 21 10:29:44. We observed two consecutive ABACAD cadences, where the "A" or "ON" observation was centered on the target's J2000.0 ephemeris (19<sup>h</sup> 28<sup>m</sup> 19.8<sup>s</sup> , 26◦ 40′ 12. ′′6), and the "B", "C", and "D", or "OFF" observations picked secondary sources at least 5 beam widths away from the primary target. Observations were recorded using the BL backend [\(MacMahon et al.](#page-3-13) [2018\)](#page-3-13). Raw voltage data were reduced using the standard BL data reduction pipeline [\(Lebofsky et al.](#page-3-14) [2019\)](#page-3-14).

### ATA

We observed 2MASS 19281982-2640123 with the ATA for six 5-minute pointings, beginning on UT 2022 May 21 10:40:57. We used 20 antennas and a newly-deployed beamformer backend (Farah et al., in prep.) to synthesize 2 coherent beams, one centered on the target, and another placed 0.8◦ (∼ 13× full-width half-maximum of the synthesized beam) away in both Right Ascension and Declination.

All data are available online[1](#page-2-0) . Table [1](#page-2-1) shows the observational parameters for both telescopes. The mean system temperature is determined from observations of 3C 295 for the GBT and 3C 286 for the ATA.

Table 1. Observational Parameters and Calculated Values for Both Telescopes at L-band

| Sensitivity Limits |             |            |          |             |        |                     |                |
|--------------------|-------------|------------|----------|-------------|--------|---------------------|----------------|
| Telescope          | Frequency   | Start Time | End Time | Measured    | SEFD   | 10σ Detectable Flux | 10σ EIRP limit |
|                    | Range (GHz) | (UTC)      | (UTC)    | Tsys<br>(K) | (Jy)   | Density Limit (Jy)  | (1012 W)       |
| GBT                | 0.94–2.06   | 10:29:44   | 11:32:01 | 16.9        | 8.2    | 5.6–146.3a          | 201–5261a      |
| ATA                | 1.064–1.736 | 10:40:57   | 13:29:51 | 51          | 335.1b | 189.1–415.7a        | 6800–14848a    |

aThe span of our limit, dependent on our dechirping efficiency due to signals at high drift rates spreading across multiple channels, which reduces our sensitivity. The lower bound applies to all drift rates |ν˙| ≤ 0.15 Hz/s and |ν˙| ≤ 1.82 Hz/s for the GBT and ATA, respectively, while the high bound applies to our maximum drift rate |ν˙| = 4 Hz/s.

# RESULTS AND DISCUSSION

To test our recording pipeline and sensitivity, we simultaneously observed, and detected, PSR 1932+1059 with both telescopes (figures on website). The detection signal-to-noise (S/N) ratio of the pulse profiles follows expectations based on sensitivity estimations of both telescopes, and the pulsar's flux density.

We used turboSETI to search for narrowband signals over a Doppler drift rate range of ±4 Hz s<sup>−</sup><sup>1</sup> and a S/N threshold of 10 with the high spectral resolution data products (GBT: ∼2.79 Hz / ∼18.25 s, ATA: ∼1.91 Hz / ∼1.05 s), broadly following the steps described by [Price et al.](#page-3-15) [\(2020\)](#page-3-15) and [Sheikh et al.](#page-3-11) [\(2020\)](#page-3-11). For the GBT, a continuous, celestially-localized signal associated with pointings toward 2MASS 19281982-2640123 would appear in all 3 of the ON observations and in none of the OFF observations. We do not see any signals with this behaviour: all of our 507 potential candidates appear in at least one OFF observation, which rules out spatially-isolated signals in the direction of 2MASS 19281982-2640123. For the ATA, the second beam was placed sufficiently far from the on-source (1.13◦ ) that it can be treated as an "OFF" observation; thus any potential signal from the direction of 2MASS 19281982-2640123 should only appear in the first beam. All of the ∼ 9000 events detected appeared in both beams, suggesting that they are due to local RFI.

Using 2MASS 19281982-2640123's distance of 1788+19 <sup>−</sup><sup>19</sup> light years from Gaia's DR3 [\(Gaia Collaboration et al.](#page-3-16) [2016b,](#page-3-16) [2021\)](#page-3-17), Equations 3–4 of [Enriquez et al.](#page-3-1) [\(2017\)](#page-3-1), and our calibrated system equivalent flux density (SEFD), we calculated the minimum detectable flux density for a 300 s observation using a 10σ threshold. Using [Enriquez et al.](#page-3-1) Equations

b Computed for the output of the coherent beamformer with 20 ATA antennas

<sup>1</sup> <https://seti.berkeley.edu/wow>

## PDF page 4

5–7, we derived an upper limit for the EIRP (Equivalent Isotropic Radiated Power) of a hypothetical transmitter with an intrinsically-narrow spectral width of 1 Hz (see Table [1\)](#page-2-1).

After visual inspection of our candidates, we find no trace of the WOW! signal. Using [Caballero](#page-3-0) [\(2022\)](#page-3-0)'s filtering criteria from earlier, with their more stringent temperature of 5730 K < Teff < 5830 K for Sun-like stars, there are actually a total of 8 Sun-like stars within the WOW! signal uncertainty region. Additionally, using effective temperature as the only criteria (3500 K < Teff < 6000 K), we find as many as 602 sources (262 for which radius and luminosity are known). F- and M-type stars have also been suggested as having the potential to host habitable environments [\(Tarter](#page-3-18) [et al.](#page-3-18) [2007;](#page-3-18) [Sato et al.](#page-3-19) [2014;](#page-3-19) [Shields et al.](#page-3-20) [2016\)](#page-3-20), so these cannot be ruled out. There remain a significant number of sources that are either Sun-like and/or pass the criteria for having a habitable zone, and future observations could target these in followup of the WOW! Signal.

BL is managed by the Breakthrough Initiatives, sponsored by the [Breakthrough Prize Foundation.](http://breakthroughinitiatives.org) The GBT is a facility of the NSF, operated under cooperative agreement by Associated Universities, Inc. The ATA is a facility of the SETI Institute.

#### REFERENCES

- Caballero, A. 2022, International Journal of Astrobiology, 1–8
- Ehman, J. R. 1998, The Big Ear Wow! Signal What We Know and Don't Know About It After 20 Years, Ohio State University Radio Observatory.

<http://www.bigear.org/wow20th.htm>

- Enriquez, J. E., Siemion, A., Foster, G., et al. 2017, ApJ, 849, 104
- Gaia Collaboration, Prusti, T., de Bruijne, J. H. J., et al. 2016a, A&A, 595, A1
- —. 2016b, A&A, 595, A1
- Gaia Collaboration, Brown, A. G. A., Vallenari, A., et al. 2018, A&A, 616, A1
- —. 2021, A&A, 649, A1
- Gajjar, V., Siemion, A., Croft, S., et al. 2019, in BAAS, Vol. 51, 223
- Gray, R. H. 1994, Icarus, 112, 485
- Harp, G. R., Gray, R. H., Richards, J., Shostak, G. S., & Tarter, J. C. 2020, AJ, 160, 162

- Isaacson, H., Siemion, A. P. V., Marcy, G. W., et al. 2017, PASA, 129, 054501
- Kraus, J. 1979, Cosmic Search, 1, 31
- Lebofsky, M., Croft, S., Siemion, A. P. V., et al. 2019, PASP, 131, 124505
- MacMahon, D. H. E., Price, D. C., Lebofsky, M., et al. 2018, PASP, 130, 044502
- Price, D. C., Enriquez, J. E., Brzycki, B., et al. 2020, AJ, 159, 86
- Sato, S., Cuntz, M., Guerra Olvera, C. M., Jack, D., & Schr¨oder, K.-P. 2014, International Journal of Astrobiology, 13, 244–258
- Sheikh, S. Z., Siemion, A., Enriquez, J. E., et al. 2020, arXiv e-prints, arXiv:2002.06162
- Shields, A. L., Ballard, S., & Johnson, J. A. 2016, Physics Reports, 663, 1
- Smith, S., Price, D. C., Sheikh, S. Z., et al. 2021, Nature Astronomy, 5, 1148
- Tarter, J. C., Backus, P. R., Mancinelli, R. L., et al. 2007, Astrobiology, 7, 30
- Worden, S. P., Drew, J., Siemion, A., et al. 2017, Acta Astronautica, 139, 98
