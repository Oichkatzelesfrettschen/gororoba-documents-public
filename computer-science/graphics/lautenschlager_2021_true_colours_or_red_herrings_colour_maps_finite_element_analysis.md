Source: see manifest row of the PDF
PDF sha256: f6fe659e330ea226adb290c403e7d6999ff77e09a6efaf4c18b0b21ed1427799
License: CC-BY-4.0
Language: eng
Fidelity: machine (failed: characters)

# Transcription of lautenschlager_2021_true_colours_or_red_herrings_colour_maps_finite_element_analysis.pdf

Transcription of `lautenschlager_2021_true_colours_or_red_herrings_colour_maps_finite_element_analysis.pdf` in this directory, 15 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-15 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

royalsocietypublishing.org/journal/rsos

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

Research
Cite this article: Lautenschlager S. 2021 True
colours or red herrings?: colour maps for finiteelement analysis in palaeontological studies to
enhance interpretation and accessibility. R. Soc.
Open Sci. 8: 211357.
https://doi.org/10.1098/rsos.211357

True colours or red herrings?:
colour maps for finiteelement analysis in
palaeontological studies to
enhance interpretation and
accessibility
Stephan Lautenschlager
School of Geography, Earth and Environmental Sciences, University of Birmingham,
Birmingham, UK

Received: 21 August 2021
Accepted: 21 October 2021

Subject Category:
Earth and environmental science
Subject Areas:
palaeontology
Keywords:
biomechanical analysis, digital visualization,
fossils, three-dimensional models

Author for correspondence:
Stephan Lautenschlager
e-mail: s.lautenschlager@bham.ac.uk

SL, 0000-0003-3472-814X
Accessibility is a key aspect for the presentation of research
data. In palaeontology, new data is routinely obtained with
computational techniques, such as finite-element analysis
(FEA). FEA is used to calculate stress and deformation in
objects when subjected to external forces. Results are displayed
using contour plots in which colour information is used to
convey the underlying biomechanical data. The Rainbow colour
map is nearly exclusively used for these contour plots in
palaeontological studies. However, numerous studies in other
disciplines have shown the Rainbow map to be problematic due
to uneven colour representation and its inaccessibility for those
with colour vision deficiencies. Here, different colour maps
were tested for their accuracy in representing values of FEA
models. Differences in stress magnitudes (ΔS) and colour values
(ΔE) of subsequent points from the FEA models were compared
and their correlation was used as a measure of accuracy. The
results confirm that the Rainbow colour map is not well suited
to represent the underlying stress distribution of FEA models
with other colour maps showing a higher discriminative power.
As the performance of the colour maps varied with tested
scenarios/stress types, it is recommended to use different
colour maps for specific purposes.

1. Introduction
Electronic supplementary material is available
online at https://doi.org/10.6084/m9.figshare.c.
5701985.

The last two decades have witnessed a surge in the use of
computational techniques to study the anatomy and functional
© 2021 The Authors. Published by the Royal Society under the terms of the Creative
Commons Attribution License http://creativecommons.org/licenses/by/4.0/, which permits
unrestricted use, provided the original author and source are credited.

## PDF page 2

(a)

(c)

2
normal colour vision

?

protanopia-type CVD

?

Figure 1. Problems of the Rainbow colour scheme: (a) non-uniform distances between individual colours (adapted from [27]). (b)
Lack of intuitive perceptual order. (c) Rainbow colour map as seen without and with colour vision deficiency (i.e. deuteranopia and
protanopia type) and in greyscale.
morphology of fossil organisms with the aim of reconstructing their palaeobiology [1–3]. Tools for the
biomechanical analysis of fossils, such as finite-element analysis (FEA) [4,5], computational fluid
dynamics (CFD) analysis [6,7] and multibody dynamics analysis (MDA) [8], are now routinely
applied to investigate the form–function relationships of fossils. Of these, FEA has become a powerful
and ubiquitous method to test hypotheses about the functional capabilities of extinct organisms, in
particular for species for which no living analogues may exist.
Originally developed as an engineering technique, FEA predicts the deformation in objects with
complex geometries and different materials subject to external load forces. Key to the technique is the
subdivision (discretization) of the analysed object into numerous, small and geometrically simple
elements connected by shared nodes, for which the deformation calculations are subsequently
performed. This simplification allows a quick but generally accurate approximation to solve the
problem for any given object and the calculation of biologically relevant performance measures, such
as stress and strain [5]. Based on the discretization, discrete stress or strain values can be associated
with each element and node in an FEA model. For the presentation of the results, these values can be
reported quantitatively, for example as model averages or mean values [9,10], values of individually
selected elements or sections [11,12], as stress intervals [13], or using a landmark-based approach on
the deformed models [14]. However, reporting a large amount of numerical values may not intuitively
convey the observed results to the reader. Therefore, it is common practice to present FEA results
more qualitatively in the form of contour plots. For these colour-indexed ( pseudo- or false-colour)
plots, the numerical value of each element in an FEA model is represented by different colours. Such
colour coding can be a powerful tool to differentiate and convey information. Although the use of
different colour maps does not change the underlying results (e.g. stress and strain magnitudes), they
have a substantial impact on the results’ legibility and therefore accessibility of the same. This is
particularly true for the use of FEA in a comparative context, which aims to identify (subtle)
differences between models (e.g. species) [5].
Traditionally, and with very few exceptions [15–17], the colour scheme of choice for FEAs of
palaeontological and biological specimens has been (and still is) the classic Rainbow colour map. It is
based on the colours in the visible light spectrum from blue (usually lower values) via green, yellow
and orange to red (usually higher values). It is one of the most common colour schemes for data
visualization and the default option in many software toolkits. Despite its ubiquitous use and
popularity, a number of studies in the last two decades have identified considerable problems with
the Rainbow colour map [18–25]: (i) the perceived transitions between the individual colours of the
Rainbow map are not uniform [25,26], with some colours (i.e. red, green) seemingly taking up a larger
part of the colour map (figure 1a). This effect can simulate sharp transitions in sequential data,
making small variations in the underlying data appear more important [27,28]. Similarly, yellow is the
brightest colour in the Rainbow colour map. Although it is not at the extreme end of the colour map,
it tends to attract the eye more than other colours in the spectrum [25,29,30]. (ii) While ordered from
shorter (blue) to longer (red) wavelengths, the Rainbow map does not follow any naturally perceived
order. This means that in contrast with greyscale or gradient colour maps (which can be arranged
from dark to light or vice versa), there is no implicit order to the Rainbow colour map [23,26,31],
making the comparison between two relative values difficult (figure 1b). (iii) Lastly, but importantly,

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

grey scale

royalsocietypublishing.org/journal/rsos

deuteranopia-type CVD

(b)

## PDF page 3

In order to evaluate their visual effect and accessibility, different colour maps were tested for a variety
of FEA models of fossil specimens and different FEA stress measures. In addition to the traditional
Rainbow map (see also [39]), nine further, established colour maps were selected (version numbers
are provided where present): (a) The five sequential colour maps Batlow (7.0), Inferno, Parula, Viridis
and YlGnBu [25,40–43]. Sequential colour maps vary between two colours ranging from dark to
light (or vice versa) and are suitable for ordered data ranging gradually from low to high values (i.e.
ratio data with an absolute zero value) [27]. (b) The three diverging colour maps Cork (7.0), Polar and
Roma (7.0) [25,43]. Diverging colour maps range between two contrasting colours at either end
separated by a neutral colour in the middle and are suitable for interval data that can have positive
and negative values [27]. (c) As a further option, a variant of the classic Rainbow colour map known
as Turbo was included in the analysis. Although Turbo similarly consists of a sequence of colours in
the visible light spectrum, it has been suggested to represent a perceptually improved rainbow map
with a uniform luminance [44,45]. All colour maps are non-proprietary, in some cases, versioned and
available/defined via the respective references above. Not all colour maps are readily and equally
available by default in all software but can be added in most cases (see also below),
Other colour maps, such as qualitative, categorical or cyclic colour maps, were not tested as these are
not appropriate for FEA data. The colour maps tested here were selected following their use and
popularity in different applications. However, not all of the colour maps are perceptually uniform
(e.g. the difference between two colours as perceived by the human eye is proportional to the
numerical distance within the given colour space). Batlow, Cork, Inferno, Roma, Viridis and YlGnBu are
all perceptually uniform, whereas Parula, Polar, Rainbow and Turbo are not (see also [43]).
All colour maps used for this study consist of 24 individual colour values (definitions (order and HEX
colour codes) are available in the electronic supplementary material), and all outputs presented here were
generated in Abaqus and model views were saved as image files. Depending on the software, custom
colour maps can be created. In this example, all colour maps were created in Abaqus via a commandline script detailing the colour components via HEX codes individually (see the script in electronic
supplementary material). Alternatively, new colour maps (so-called spectra in Abaqus) can be created
via a tools menu and selecting successive colours via a colour picker. This process will differ for
individual software. However, specific pre-designed colour maps can be generated and accessed via
online tools, such as https://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3 [40].
Several FEA models of fossil specimens and different skeletal elements were used here to evaluate
the perceptual effects of the tested colour maps with different three-dimensional morphologies:
(a) a simplified, planar model of the mandible of the sabre-toothed cat Dinofelis cristata as used in [46]
(figure 2). This model was chosen to represent a geometrically simple morphology as used for
FEA models not derived from computed tomography (CT) or surface-based digitization methods
[47,48]. For this model, contour plots displaying the distribution of von Mises stress were chosen
as an example for ratio data. (b) A three-dimensional model of the mandible of Thrinaxodon liorhinus
representing a geometrically more complex morphology compared to the model of Dinofelis and
derived from CT scanning [49]. For the contour plots, tensile ( positive) and compressive (negative)
absolute stresses were displayed as an example for interval data. (c) A model of the skull of
the therizinosaurian dinosaur Erlikosaurus andrewsi as used in [50]. In addition to the different
contour plots displaying von Mises stress, the models were also displayed as perceived with
deuteranopia-type CVDs. For this purpose, the images were converted accordingly using Adobe
Photoshop CC 2020. (d) A model of the skull of the capitosaurian temnospondyl Parotosuchus
helgolandicus [51] representing a dorsoventrally flattened skull morphology. In addition to the

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

2. Material and methods

3

royalsocietypublishing.org/journal/rsos

the Rainbow colour map creates considerable accessibility problems for those with colour vision
deficiencies (CVDs). Approximately 5–10% of the population may suffer from some form of CVD,
such as red-green blindness (Deuteranopia), which renders data represented by the Rainbow colour
map largely unreadable [32–34]. Furthermore, similar issues arise when results using the Rainbow
colour map are converted to a greyscale format, such as for example for printing.
Given these inherent problems with the Rainbow colour scheme, several disciplines, including
oceanography [35], meteorology [36,37] and geosciences [25,38], have started to address this issue and
proposed the use of alternative colour schemes. Here, different colour maps are tested and their
effectiveness for the visualization of FEA results of palaeontological models is evaluated.

## PDF page 4

(f)

4
10

Polar
R2 = 0.578

0

R2 = 0.644

von Mises stress (MPa)

10

Batlow

10

Roma
R2 = 0.563

0

0

(h)
R2 = 0.635

von Mises stress (MPa)

10

Cork

10

Turbo
R2 = 0.664

von Mises stress (MPa)

(c)

0

0

(i)
R2 = 0.802

von Mises stress (MPa)

10

Inferno

10

Viridis
R2 = 0.787

von Mises stress (MPa)

(d)

0

0

(j)
R2 = 0.653

von Mises stress (MPa)

10

Parula

10

Ylgnbu
R2 = 0.547

0

von Mises stress (MPa)

(e)

0

Figure 2. Contour plots for different colour maps for Von Mises stress values are shown for the simplified planar mandible model of
the sabre-tooth cat Dinofelis cristata. In addition to the standard Rainbow colour map (a), nine further colour maps were tested:
Batlow (b), Cork (c), Inferno (d ), Parula (e), Polar ( f ), Roma (g), Turbo (h), Viridis (i) and YlGnBu ( j ). Grey regions in the contour
plots represent stress magnitudes beyond the applied scale limit. R 2-values are given for each colour map (see electronic
supplementary material for full correlation plots).

different contour plots displaying von Mises stress, the models were also displayed as perceived with a
protanopia-type CVD. For this purpose, the images were converted accordingly using Adobe Photoshop
CC 2020. (e) A model of a dorsal vertebra of the ornithischian dinosaur Stegosaurus stenops [47]
representing a post-cranial skeletal element. In addition to the different contour plots displaying von
Mises stress, the images of the contour plot models were also converted into greyscale using Adobe
Photoshop CC (2020) (Image -> Adjustments -> Black & White and using the default setting for
greyscale mode). (f ) A model of the manual claw of the therizinosaurian dinosaur Nothronychus
graffami [52] to illustrate the effect of colour maps against a different background colour. The
boundary conditions for these models have no direct effect on the colour map interpretation.
Therefore, please refer to the original publications for further details on the boundary conditions of
the respective models.
To quantify the discriminative power of the individual colour maps (i.e. relating individual colour
values to their respective FEA stress magnitudes), the correlation between the colour maps and stress
results of the FEA models was calculated. For consistency across the models, 20 points (i.e. elements)

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

0

(g)
von Mises stress (MPa)

(b)

royalsocietypublishing.org/journal/rsos

R2 = 0.571

von Mises stress (MPa)

10

Rainbow

von Mises stress (MPa)

(a)

## PDF page 5

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

ð2:1Þ

Similarly, the difference in colour value ΔE was determined for each colour map [53] by calculating
the Euclidean distances between two subsequent points (equation (2.2))
DE ¼ ð(L1 –L2 )2 þ (a1 –a2 )2 þ (b1 –b2 )2 Þ0:5 :

ð2:2Þ

In a final step, ΔE and ΔS were subjected to an ordinary least square regression and the R 2-value was
obtained as a measure for the discriminative power of the individual colour maps (see electronic
supplementary material).
It should be noted that Abaqus applies a shading algorithm when displaying FEA contour plots in
that it simulates an artificial light source positioned to the top left of the three-dimensional space.
To avoid the effects of artificial shadows on the colour representation, all measurements were
performed with the model exposed to the maximum light intensity (usually with models in left lateral
or dorsal view).

3. Results
Overall, 10 different colour maps were tested for their accuracy to represent the underlying stress
magnitudes of finite-element models in the form of contour plots. In addition to the default Rainbow
map, nine further colour maps were tested and the R 2-value was used as a measure for the
correlation between stress magnitudes and colour maps.
Across the different colour maps, models, stress types and visual appearances, the R 2 values range
from nearly no (R 2 = 0.008) to strong correlations (R 2 = 0.967) (table 1). No single colour map was
found to show consistently the strongest correlation for the different test settings, with rather more
nuanced variations in representative performance for the different colour maps. It is noteworthy that
the Rainbow colour map performed worse than most of the other colour maps.
For results in the form of ratio data, such as von Mises stress (figure 2; electronic supplementary
material, figure S1), the sequential colour map Inferno produced the highest correlation (R 2 = 0.802). By
contrast, the commonly used Rainbow map showed only a weak correlation (R 2 = 0.571), and only the
colour maps Roma (R 2 = 0.563) and YlGnBu (R 2 = 0.547) had a weaker performance. The rainbow
variant Turbo performed only moderately better than the classic Rainbow (R 2 = 0.664).
For interval data, such as compressive (i.e. negative) and tensile (i.e. positive) stresses plotted together
(figure 3; electronic supplementary material, figure S2), the sequential colour maps YlGnBu (R 2 = 0.967)
and Parula (R 2 = 0.959), as well as the diverging colour map Polar (R 2 = 0.934) showed the highest
correlation between stress magnitudes and colour representation. The Rainbow colour map produced a
strong, although not the highest, correlation (R 2 = 0.887), whereas Turbo performed worst in this
scenario but with still a strong correlation (R 2 = 0.852).
To test for the discriminative performance of the different colour maps when perceived with a CVD,
contour plots were converted to deuteranopia- and protanopia-type appearances (figures 4 and 5;

R. Soc. Open Sci. 8: 211357

DS ¼ stress magnitude of point 1–stress magnitude of point 2:

5

royalsocietypublishing.org/journal/rsos

along with a line across the FEA model were selected that covered the morphology evenly. Stress
magnitudes (von Mises and compressive/tensile stresses) were recorded for all sampled points. This
approach follows the practice to sample a subset of elements of an FEA model [11,12,50] to quantify
its biomechanical properties.
In the next step, the colour values for the sampled points for each tested colour map were recorded as
RGB values. Although defining colour as RGB values is a common practice for many (web-based and
digital) applications, they were specifically designed for use on monitors and do not reflect human
colour perception as the RGB colour space is not uniform [53]. A solution to this problem is using the
CIELAB (also known as CIE L a b ) colour space [54] which has been designed to be perceptually
uniform. Here, the distance between two points defining individual colours is proportional to the
perceptual difference between them [55,56]. Therefore, the collected RGB values were converted into
CIELAB colour values. The collection of the RGB colours from images of the FEA models and
subsequent conversion to CIELAB colour space was done via the convertColor function in R [57] (see
electronic supplementary material). For a colour map to represent the underlying data correctly, it
must reflect changes in magnitude between two sampled points accordingly. To test this correlation,
the absolute difference ΔS in stress magnitude was calculated for subsequent points sampled for each
model (equation (2.1)).

## PDF page 6

0.644

0.910
0.890

0.547

0.476

von Mises

tensile/compressive
deuteranopia

protanopia

greyscale

0.440

0.555

0.871
0.696

0.635

Cork

0.578

0.738

0.905
0.693

0.802

Inferno

0.360

0.642

0.959
0.460

0.653

Parula

0.348

0.458

0.934
0.604

0.578

Polar

0.086

0.564

0.887
0.504

0.571

Rainbow

0.098

0.485

0.872
0.476

0.563

Roma

R. Soc. Open Sci. 8: 211357

Batlow

Table 1. R 2-values for all tested colour maps stress and visual appearances. Score with the highest value italicized for each test setting.
Viridis
0.787
0.933
0.475
0.876
0.306

Turbo
0.664
0.852
0.117
0.717
0.008

0.500

0.670

0.967
0.511

0.547

YlGnBu

royalsocietypublishing.org/journal/rsos

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

6

## PDF page 7

(f)

(a)

Polar

–10

(g)

Batlow

Roma
tensile

stress (MPa)

tensile

stress (MPa)

compressive

(h)
Turbo
R2 = 0.852

–10

–10

(d)

10

stress (MPa)

tensile
compressive

stress (MPa)

10

tensile

R2 = 0.871

compressive

Cork

(i)
Viridis
R2 = 0.933

–10

(e)

10

stress (MPa)

tensile
compressive

stress (MPa)

10

tensile

R2 = 0.905

compressive

Inferno

–10

(j)
Ylgnbu

–10

tensile

10

R2 = 0.967
stress (MPa)

stress (MPa)

compressive

tensile

10

R2 = 0.959

compressive

Parula

–10

Figure 3. Contour plots for different colour maps for compressive and tensile stress values shown for the mandible model of the
cynodont Thrinaxodon liorhinus. In addition to the standard Rainbow colour map (a), nine further colour maps were tested: Batlow
(b), Cork (c), Inferno (d), Parula (e), Polar (f ), Roma (g), Turbo (h), Viridis (i) and YlGnBu ( j ). Grey regions in the contour plots
represent stress magnitudes beyond the applied scale limit. R 2-values are given for each colour map (see electronic supplementary
material for full correlation plots).

electronic supplementary material, figures S3 and S4). For the deuteranopia type, the sequential colour
map Batlow (R2 = 0.89) and the diverging colour map Cork (R 2 = 0.696) were found to represent the
stress data the most accurately. Again, the Rainbow colour map (R 2 = 0.504) was not able to represent
the underlying stress results fully, while Turbo showed only a very weak correlation (R 2 = 0.117). For
the protanopia-type contour plots, Viridis (R 2 = 0.876) and Inferno (R 2 = 0.738) showed high correlation
scores, whereas Polar (R 2 = 0.458) recorded only a weak correlation.

R. Soc. Open Sci. 8: 211357

–10

–10

(c)

10

R2 = 0.872

10

compressive

R2 = 0.910

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

tensile

stress (MPa)

stress (MPa)

tensile

R2 = 0.872

–10

(b)

10

R2 = 0.934

compressive

R2 = 0.887

compressive

10

royalsocietypublishing.org/journal/rsos

Rainbow

7

## PDF page 8

(f)

R2 = 0.604

0

0

0
R2 = 0.476

0

0

R2 = 0.696

5

0

(d)

von Mises stress (MPa)

5

Parula

0
R2 = 0.460

R2 = 0.117

5
R2 = 0.475

(j)

5

Ylgnbu

5

0

5

0

von Mises stress (MPa)

0

5

0

(i)
Viridis

von Mises stress (MPa)

0
R2 = 0.693

(e)

0

5
von Mises stress (MPa)

Inferno

5

von Mises stress (MPa)

0

Turbo

von Mises stress (MPa)

5

von Mises stress (MPa)

(h)

von Mises stress (MPa)

Cork

von Mises stress (MPa)

(c)

5
von Mises stress (MPa)

von Mises stress (MPa)

5

von Mises stress (MPa)

R2 = 0.890

5

Roma

0
R2 = 0.511

5
von Mises stress (MPa)

0

(g)

von Mises stress (MPa)

von Mises stress (MPa)

5

Batlow

0

5

0

Figure 4. Contour plots as seen without and with deuteranopia-type colour vision deficiency for different colour maps. Von Mises
stress are values shown for the cranium model of the dinosaur Erlikosaurus andrewsi. In addition to the standard Rainbow colour
map (a), nine further colour maps were tested: Batlow (b), Cork (c), Inferno (d ), Parula (e), Polar ( f ), Roma (g), Turbo (h), Viridis (i)
and YlGnBu ( j ). Grey regions in the contour plots represent stress magnitudes beyond the applied scale limit. R 2-values are given for
each colour map (see electronic supplementary material for full correlation plots).

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

(b)

5
von Mises stress (MPa)

0

von Mises stress (MPa)

R2 = 0.504

5
von Mises stress (MPa)

0

8

5

Polar

royalsocietypublishing.org/journal/rsos

von Mises stress (MPa)

5

Rainbow

von Mises stress (MPa)

(a)

## PDF page 9

Inferno

0

0

5

5

R2 = 0.738

(h)
Turbo

von Mises stress (MPa)

5

(i)
Viridis

0

0

5

5

(e)

von Mises stress (MPa)

von Mises stress (MPa)
5

5

R2 = 0.485

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)
5

R2 = 0.555

Roma

von Mises stress (MPa)

(d)

0

von Mises stress (MPa)

Cork

0

von Mises stress (MPa)

(c)

R2 = 0.547

(g)

0

0

5

5

R2 = 0.717

von Mises stress (MPa)

5

0

0

5

5

R2 = 0.876

0

0

5

5

0

0

0

R2 = 0.670

von Mises stress (MPa)

Ylgnbu

von Mises stress (MPa)

R2 = 0.642

von Mises stress (MPa)

parula

von Mises stress (MPa)

(j)

0

Figure 5. Contour plots as seen without and with protanopia-type colour vision deficiency for different colour maps. Von Mises
stress values are shown for the cranium model of the capitosaurian temnospondyl Parotosuchus helgolandicus. In addition to the
standard Rainbow colour map (a), nine further colour maps were tested: Batlow (b), Cork (c), Inferno (d), Parula (e), Polar ( f ), Roma
(g), Turbo (h), Viridis (i) and YlGnBu ( j ). Grey regions in the contour plots represent stress magnitudes beyond the applied scale
limit. R 2-values are given for each colour map (see electronic supplementary material for full correlation plots).
In a final analysis, contour plots were converted to greyscale and the discriminative
performance of the colour maps was tested (figure 6; electronic supplementary material, figure S5).
In this scenario, all colour maps produced only a moderate to no correlation (0.578 < R 2 < 0.008).

9

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

Batlow

0

von Mises stress (MPa)

5

(b)

R2 = 0.458

0

von Mises stress (MPa)

0

5

5

von Mises stress (MPa)

0

Polar

royalsocietypublishing.org/journal/rsos

R2 = 0.564

(f)

von Mises stress (MPa)

5

5

von Mises stress (MPa)

Rainbow

von Mises stress (MPa)

(a)

## PDF page 10

(f)

Rainbow

5

5

5

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

0

0

0

(g)

Batlow

5

0

Roma

5

5

5

5

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

R2 = 0.098

von Mises stress (MPa)

R2 = 0.476

0

0

0

0

(c)

(h)

Cork

Turbo

R2 = 0.008
5

von Mises stress (MPa)

von Mises stress (MPa)

0

0

0

5

von Mises stress (MPa)

5

von Mises stress (MPa)

R2 = 0.440
5

0

(d)

(i)

Inferno

Viridis

R2 = 0.306

5

5

5

5

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

R2 = 0.578

0

0

0

0

(e)

(j)

Parula

Ylgnbu

R2 = 0.500

R2 = 0.360

0

5
von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)
0

5

5

5

0

0

Figure 6. Contour plots as seen in full colour and greyscale for different colour maps. Von Mises stress values are shown for a
vertebra of the ornithischian dinosaur Stegosaurus stenops. In addition to the standard Rainbow colour map (a), nine further
colour maps were tested: Batlow (b), Cork (c), Inferno (d), Parula (e), Polar ( f ), Roma (g), Turbo (h), Viridis (i) and YlGnBu
( j ). Grey regions in the contour plots represent stress magnitudes beyond the applied scale limit. R 2-values are given for each
colour map (see electronic supplementary material for full correlation plots).

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

R2 = 0.348

royalsocietypublishing.org/journal/rsos

R2 = 0.086

(b)

10

Polar

von Mises stress (MPa)

(a)

## PDF page 11

The best performance was found for Inferno (R 2 = 0.578); Rainbow, Roma and Turbo showed the least
correlation (R 2 < 0.098).

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

R. Soc. Open Sci. 8: 211357

The Rainbow colour map has been a ubiquitous tool in data visualization for decades [25,37]. Engineering
techniques such as FEA, which has increasingly been used in palaeontological studies over the last 20
years, are no exception. Results from FEAs are routinely visualized in the form of contour plots using
the Rainbow colour map. Contour plots typically display von Mises stress, a common measure to
evaluate the stability of a model under loading conditions. However, as shown by the results from
this study, the Rainbow colour map correlates only poorly with the underlying von Mises stress data
(table 1 and figure 2), and its discriminative power is equally poor when perceived with different
types of CVDs (figures 4 and 5). This should not come as a surprise as the Rainbow colour map has
been considered problematic and misleading in other disciplines [18,19,22,23–25].
Other colour maps tested here performed considerably better. However, no one colour map was
found to be optimally suited for all types of stress and visual perception. For interval-type stresses,
such as compressive and tensile stresses plotted on the same model, the Rainbow colour map showed
a high correlation (table 1, figure 3) similar to or even better than the diverging colour maps in this
study. Interestingly, diverging colour maps did not necessarily perform better for interval data,
whereas sequential colour maps were not always found to show the best correlation for ratio data (i.e.
von Mises stress). Inferno, Batlow and Parula generally showed the highest discriminative power, but
not consistently so (table 1). It is noteworthy that differences in the performance were recorded when
colour maps were tested in CVD settings. The same colour maps (Inferno, Batlow and Parula, and to a
lesser degree Polar and Viridis) represented the underlying stress values reasonably well despite the
reduced colour information. However, this means that a single colour map cannot be used as a silver
bullet to perform equally well under all conditions. Similar to the alternative text describing figures,
the second set of contour plots with a different colour map could be provided in the electronic
supplementary material accessible to those with CVD. More generally, the use of specific colour maps
may have to be decided on a case to case basis using custom-made or existing colour maps (see, for
example, [38] for available colour maps). For interval-type data, other considerations than the
discriminative power (expressed as the R 2 value here) may need to be considered. For such data, the
central zero value can be an important identifier of stress-free regions in the model, which can be
recognized more easily when diverging colour maps are used.
In this context, it should be noted that the correlation analysis used here to discriminate stress/colour
changes is not perfect. Human colour perception is not uniform, often subjective and dependent on other
factors such as age and individual variation and as such does not correspond to Euclidean distances in
colour space [58]. The CIELAB colour space is an attempt to replicate human colour differentiation. As
the correlation analysis only considers absolute changes along with a trajectory, the analysis may not
record the exact correlation when non-monotonic changes on the stress scale are associated with
changes in different directions in the CIELAB space. However, this is less likely to be a problem for
the perceptually based colour maps.
The choice of an appropriate colour map may further depend on the nature of the results of an FEA.
Models spanning a wide range of stress magnitudes, but with an uneven distribution of values will be
biased towards certain regions of the colour map. This situation could result in a lower resolution of
stress (and thereby colour) values towards the lower end of the colour map to encompass the full
range of stress magnitudes present. Sequential colour maps will be a better option in such cases as
their colour gradient is expressed along with the whole range of the colour map in comparison to
divergent colour maps.
It is important to note that CVD is only one form of visual impairment and of course further
improvements for accessibility should be aimed for when considering the presentation of results from
FEA (and other analyses more broadly). The Web Content Accessibility Guidelines (WCAG) [59]
provide further recommendations to improve accessibility, including appropriate contrast ratios
between colours to allow their distinction. For example, Cork, Polar and Roma have high contrast
ratios, whereas Inferno and Viridis have poorer contrast ratios. These ratios are, of course, lower if
subsequent colours along with the gradient were to be tested, not just extreme and mid-point values.
However, this goes to show that not only the uniform sequence of colours but also the contrast
between them plays a role in making contour plots accessible.

royalsocietypublishing.org/journal/rsos

4. Discussion

11

## PDF page 12

Polar

Roma

von Mises stress (MPa)

0

5

von Mises stress (MPa)

von Mises stress (MPa)

0

12

Polar
5

0

0

5

5

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

Roma

5

von Mises stress (MPa)

Batlow

5

0

0

0

0

Turbo

5

5

von Mises stress (MPa)

von Mises stress (MPa)

von Mises stress (MPa)

Turbo

5

von Mises stress (MPa)

Cork

5

0

0

0

0

Viridis

5

5

von Mises stress (MPa)

von Mises stress (MPa)

Viridis

5
von Mises stress (MPa)

Inferno

5
von Mises stress (MPa)

Inferno

0

0

0

0

Parula
5

von Mises stress (MPa)

von Mises stress (MPa)

Ylgnbu

5

0

0

0

5
von Mises stress (MPa)

Ylgnbu
5
von Mises stress (MPa)

Parula

0

Figure 7. Contour plots are depicted in the context of different background colours for the same model and colour maps. von Mises
stress values are shown for a manual claw of the therizinosaurian dinosaur Nothronychus graffami. Grey regions in the contour plots
represent stress magnitudes beyond the applied scale limit.
This situation is further complicated in that FEA contour plots cannot be regarded in isolation but
need to be considered in the context of background and environmental settings. In the simplest of
cases, this could mean that the choice of background colour can influence the readability of the
contour plots [25,60,61] (figure 7). Especially colour maps with a large amount of dark components
can become invisible against a black background. Colourmaps with strong contrast and luminosity
(e.g. Parula, Polar) can work well in such a case. For the presentation on a white background, colour
maps with a decreasing chroma (=colour intensity), such as Batlow, Inferno and, in particular, YlGnBu
are more appropriate to convey the results [25,61,62].
Within a digital, three-dimensional environment pseudo-colouring creates a further difficulty as the
choice of colours interact with the shading and perception of spatial cues [24]. Properties such as the
number, direction and intensity of light sources, specularity (i.e. reflectiveness of a surface) and other
settings can have an impact on the appearance of colour maps as well. Further, different devices and
display technologies display colours variably and for consistent perception colour calibration would
have to be performed first.
Most FEA software allows turning off shading effects. However, this could possibly result in a
reduced perception of the model morphology, especially for flattened surfaces with low topography
(e.g. figure 5). Although not tested here, it should further be taken into consideration that different
FEA software packages may use slightly different variations/colour definitions of the Rainbow colour
map, further exacerbating comparisons between outputs from different software.

R. Soc. Open Sci. 8: 211357

Cork

royalsocietypublishing.org/journal/rsos

5

Batlow

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

Rainbow

5
Von Mises stress (MPa)

Rainbow

## PDF page 13

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

Results from this study demonstrate that the Rainbow colour map is not well suited to represent the
underlying stress distribution of FEA models. Although most of the other colour maps tested here
showed a higher discriminative power, no single colour map was found to perform consistently well
throughout all scenarios and for all stress types. It is therefore recommended that different colour
maps without data distortion are used to present results. This could mean using different colour maps
for ratio (e.g. von Mises stress) and interval data (e.g. compressive and tensile stresses). Alternatively,
the second set of contour plots with a different colour map could be provided in the electronic
supplementary material to increase accessibility.
The perception of colour is highly dependent on multiple factors, including display devices, colour
standards for display and printing, and differences in the human visual apparatus. A variety of different
colour maps displayed on different models of palaeontological specimens have been presented here. It
is hoped that the reader will use these examples alongside the quantitative evaluation as guidance for
their applications and studies. However, the tested colour maps in this study are far from exhaustive
and a variety of tools exist to access pre-designed colourmaps (see [25], Box 2).
Ethics. No ethical issues arose in the course of this study.
Data accessibility. Raw measurements and code are included in the electronic supplementary material. FEA results files are
available here: https://figshare.com/articles/dataset/FEA_models_from_True_colours_or_red_herrings_-_Colour_
maps_for_finite_element_analysis_in_palaeontological_studies_and_how_they_can_enhance_interpretation_and_
accessibility_/14905104. The data are provided in the electronic supplementary material [66].
Competing interests. I have no competing interests.
Funding. No funding source to report.
Acknowledgements. Emma Dunne and Sarah Greene kindly provided feedback on the draft manuscript. Fabio Crameri,
Melisa Morales-Garcia, Eric Snively, Claus Wilke and Achim Zeileis are thanked for constructive comments and
helpful suggestions improving earlier versions of the manuscript.

References
1.

2.

3.

Cunningham JA, Rahman IA, Lautenschlager S,
Rayfield EJ, Donoghue PC. 2014 A virtual world
of paleontology. Trends Ecol. Evol. 29, 347–357.
(doi:10.1016/j.tree.2014.04.004)
Sutton M, Rahman I, Garwood R. 2014
Techniques for virtual palaeontology. New York,
NY: John Wiley Sons.
Lautenschlager S. 2016 Reconstructing
the past: methods and techniques for
the digital restoration of fossils. R. Soc.
Open Sci. 3, 160342. (doi:10.1098/
rsos.160342)

4.

5.

6.

Rayfield EJ. 2007 Finite element analysis and
understanding the biomechanics and evolution
of living and fossil organisms. Annu. Rev. Earth
Planetary Sci. 35, 541–576. (doi:10.1146/
annurev.earth.35.031306.140104)
Bright JA. 2014 A review of paleontological
finite element models and their validity.
J. Paleontol. 88, 760–769. (doi:10.1666/13-090)
Bourke JM, Ruger Porter WM, Ridgely RC, Lyson
TR, Schachner ER, Bell PR, Witmer LM. 2014
Breathing life into dinosaurs: tackling challenges
of soft-tissue restoration and nasal airflow in

7.

8.

extinct species. Anatomical Rec. 297,
2148–2186. (doi:10.1002/ar.23046)
Rahman IA. 2017 Computational fluid dynamics
as a tool for testing functional and ecological
hypotheses in fossil taxa. Palaeontology 60,
451–459. (doi:10.1111/pala.12295)
Lautenschlager S. 2020 Multibody
dynamics analysis (MDA) as a numerical
modelling tool to reconstruct the function
and palaeobiology of extinct organisms.
Palaeontology 63, 703–715. (doi:10.1111/pala.
12501)

R. Soc. Open Sci. 8: 211357

5. Conclusion

13

royalsocietypublishing.org/journal/rsos

The eye-catching quality of the Rainbow colour map with its high luminance and contrast is likely the
reason for its continued prevalence despite its problems with data distortion. Different reasons have been
discussed in the past [24,25] for why the Rainbow colour map is still the visualization tool of choice for
many studies and applications. For finite-element models, this has likely historic reasons and it is the
default colour map in most software. Furthermore, the colour distribution of the Rainbow map has a
very strong signalling function and communicative power: cold colours (i.e. blue) are associated with
no or low stresses, whereas warm colours (i.e. yellow, red) indicate high-stress magnitudes. For von
Mises stress, high magnitudes indicate possible material failure and an association with a colour such
as red which is commonly used to convey danger is intuitive [63]. However, this concept can also be
conveyed with other colour maps such as Inferno.
A recent study has used a variety of colour maps to display the results from FEAs [64]. Similarly, for
palaeontological studies using other engineering tools, different colour maps have started to appear in
publications. CFD, an engineering technique to simulate fluid flow within or around objects, uses a
similar approach to FEA to represent data with pseudo-colour plots [7]. Although the Rainbow colour
map is routinely used to visualize CFD results, different colour maps have been used recently in some
studies [65].

## PDF page 14

9.

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

26.
27.

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

47.

48.

49.

50.

51.

52.

53.
54.

55.

56.
57.

58.

59.

Mikhailov A. 2019 Turbo, an improved rainbow
colormap for visualization. Google AI Blog. See
https://ai.googleblog.com/2019/08/turboimproved-rainbow-colormap-for.html (accessed
05.06.2021).
Reda K, Szafir DA. 2021 Rainbows revisited:
modeling effective colormap design for graphical
inference. IEEE Trans. Vis. Comput. Graph 27,
1032–1042. (doi:10.1109/TVCG.2020.3030439)
Lautenschlager S, Figueirido B, Cashmore DD,
Bendel EM, Stubbs TL. 2020 Morphological
convergence obscures functional diversity in
sabre-toothed carnivores. Proc. R. Soc. B 287,
20201818. (doi:10.1098/rspb.2020.1818)
Rahman IA, Lautenschlager S. 2017 Applications
of three-dimensional box modeling to
paleontological functional analysis. Paleontol.
Soc. Papers 22, 119–132.
Morales-García NM, Burgess TD, Hill JJ, Gill PG,
Rayfield EJ. 2019 The use of extruded finiteelement models as a novel alternative to
tomography-based models: a case study using
early mammal jaws. J. R. Soc. Interface 16,
20190674. (doi:10.1098/rsif.2019.0674)
Lautenschlager S, Gill PG, Luo ZX, Fagan MJ,
Rayfield EJ. 2018 The role of miniaturization in
the evolution of the mammalian jaw and
middle ear. Nature 561, 533–537. (doi:10.1038/
s41586-018-0521-4)
Lautenschlager S, Witmer LM, Altangerel P,
Rayfield EJ. 2013 Edentulism beaks and
biomechanical innovations in the evolution of
theropod dinosaurs. Proc. Natl Acad. Sci. USA
110, 20 657–20 662. (doi:10.1073/pnas.
1310711110)
Lautenschlager S, Witzmann F, Werneburg I.
2016 Palate anatomy and morphofunctional
aspects of interpterygoid vacuities in
temnospondyl cranial evolution. Sci. Nat. 103,
79. (doi:10.1007/s00114-016-1402-z)
Lautenschlager S. 2014 Morphological and
functional diversity in therizinosaur claws and
the implications for theropod claw evolution.
Proc. R. Soc. B 281, 20140497. (doi:10.1098/
rspb.2014.0497)
Mokrzycki WS, Tatol M. 2011 Colour differenceΔ
E-A survey. Mach. Graphics Vision 20, 383–411.
CIE Commission Intertnational de L’Eclairage.
1977 CIE recommendations on uniform color
spaces color-difference equations and metric
color terms. Color Res. Appl. 2, 5–6. (doi:10.
1002/j.1520-6378.1977.tb00102.x)
Silva S, Santos BS, Madeira J. 2011 Using
color in visualization: a survey. Comput.
Graphics 35, 320–333. (doi:10.1016/j.cag.2010.
11.015)
Kovesi P. 2015 Good colour maps: how to
design them. arXiv preprint arXiv:1509.03700.
R Core Team. 2020 R: a language and
environment for statistical computing. Vienna,
Austria: R Foundation for Statistical Computing.
See https://www.R-project.org/.
Gravesen J. 2015 The metric of colour space.
Graphical Models 82, 77–86. (doi:10.1016/j.
gmod.2015.06.005)
Caldwell B, Cooper M, Reid LG, Vanderheiden G,
Chisholm W, Slatin J, White J. 2008 Web
content accessibility guidelines (WCAG) 2.0.
WWW Consortium (W3C) 290, 1–34.

14

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

11.

25.

2016, 1–6. (doi:10.2352/ISSN.2470-1173.2016.
16.HVEI-133)
Crameri F, Shephard GE, Heron PJ. 2020 The
misuse of colour in science communication. Nat.
Commun. 11, 1–10. (doi:10.1038/s41467-01913993-7)
Wong B. 2010 Points of view: color coding. Nat.
Methods 7, 573. (doi:10.1038/nmeth0810-573)
Hattab G, Rhyne TM, Heider D. 2020 Ten simple
rules to colorize biological data visualization.
PLoS Comput. Biol. 16, e1008259. (doi:10.1371/
journal.pcbi.1008259)
Rhyne TM. 2017 Applying color theory to digital
media and visualization. In Proc. of the 2017 CHI
Conf. Extended Abstracts on Human Factors in
Computing Systems, pp. 1264–1267.
Alexander KR, Shansky MS. 1976 Influence of
hue, value, and chroma on the perceived
heaviness of colors. Percept. Psychophys. 19,
72–74. (doi:10.3758/BF03199388)
Wolfe JM, Horowitz TS. 2017 Five factors that
guide attention in visual search. Nat. Hum.
Behav. 1, 1–8. (doi:10.1038/s41562-017-0058)
Ware C. 2019 Information visualization:
perception for design. San Francisco, CA: Morgan
Kaufmann.
Sharpe LT, Stockman A, Jägle H, Nathans J.
1999 Opsin genes, cone photopigments,
color vision, and color blindness. Color Vision
3–51.
Simunovic MP. 2010 Colour vision deficiency.
Eye 24, 747–755. (doi:10.1038/eye.2009.251)
Wong B. 2011 Color blindness. Nat. Methods 8,
441–442. (doi:10.1038/nmeth.1618)
Samsel F, Petersen M, Geld T, Abram G,
Wendelberger J, Ahrens J. 2015 Colormaps that
improve perception of high-resolution ocean
data. In Proc. of the 33rd Annual ACM Conf.
Extended Abstracts on Human Factors in
Computing Systems, pp. 703–710.
Sherman-Morris K, Antonelli KB, Williams CC.
2015 Measuring the effectiveness of the
graphical communication of hurricane storm
surge threat. Weather Clim. Soc. 7, 69–82.
(doi:10.1175/WCAS-D-13-00073.1)
Stauffer R, Mayr GJ, Dabernig M, Zeileis A.
2015 Somewhere over the rainbow: how
to make effective use of colors in
meteorological visualizations. Bull. Am.
Meteorol. Soc. 96, 203–216. (doi:10.1175/
BAMS-D-13-00155.1)
Crameri F. 2018 Geodynamic diagnostics
scientific visualisation and StagLab 3.0.
Geoscient. Model Dev. 11, 2541–2562. (doi:10.
5194/gmd-11-2541-2018)
Quinan PS, Padilla LM, Creem-Regehr SH,
Meyer M. 2019 Examining implicit discretization
in spectral schemes. Comput. Graphics Forum
38, 363–374. (doi:10.1111/cgf.13695)
Harrower M, Brewer CA. 2003 ColorBrewer.org:
an online tool for selecting colour schemes for
maps. Cartographic J. 40, 27–37. (doi:10.1179/
000870403235002042)
Van der Walt S, Smith N. 2015 A better default
colormap for Matplotlib SciPy 2015.
Van der Walt S, Smith N. 2020 MPL colour
maps https://bids.github.io/colormap.
Crameri F. 2020 Scientific colour maps http://
www.fabiocrameri.ch/colourmaps.

royalsocietypublishing.org/journal/rsos

10.

Farke AA. 2008 Frontal sinuses and headbutting in goats: a finite element analysis.
J. Exp. Biol. 211, 3085–3094. (doi:10.1242/jeb.
019042)
Lautenschlager S. 2017 Functional niche
partitioning in Therizinosauria provides new
insights into the evolution of theropod
herbivory. Palaeontology 60, 375–387. (doi:10.
1111/pala.12289)
Piras P et al. 2015 Digging adaptation in
insectivorous subterranean eutherians. The
enigma of Mesoscalops montanensis unveiled by
geometric morphometrics and finite element
analysis. J. Morphol. 276, 1157–1171. (doi:10.
1002/jmor.20405)
Attard MR, Wilson LA, Worthy TH, Scofield P,
Johnston P, Parr WC, Wroe S. 2016 Moa diet fits
the bill: virtual reconstruction incorporating
mummified remains and prediction of
biomechanical performance in avian giants.
Proc. R. Soc. B 283, 20152043. (doi:10.1098/
rspb.2015.2043)
Marcé-Nogué J, De Esteban-Trivigno S, Püschel
TA, Fortuny J. 2017 The intervals method: a
new approach to analyse finite element outputs
using multivariate statistics. PeerJ 5, e3793.
(doi:10.7717/peerj.3793)
Lautenschlager S, Brassey CA, Button DJ, Barrett
PM. 2016 Decoupled form and function in
disparate herbivorous dinosaur clades. Sci. Rep.
6, 1–10. (doi:10.1038/srep26495)
Snively E, Russell A. 2002 The tyrannosaurid
metatarsus: bone strain and inferred ligament
function. Senckenbergiana Lethaea 82, 35.
(doi:10.1007/BF03043771)
Kleinteich T, Maddin HC, Herzen J, Beckmann F,
Summers AP. 2012 Is solid always best? Cranial
performance in solid and fenestrated caecilian
skulls. J. Exp. Biol. 215, 833–844. (doi:10.1242/
jeb.065979)
van der Meijden A, Kleinteich T, Coelho P. 2012
Packing a pinch: functional implications of chela
shapes in scorpions using finite element
analysis. J. Anat. 220, 423–434. (doi:10.1111/j.
1469-7580.2012.01485.x)
Herman GT, Levkowitz H. 1992 Color scales for
image data. Comput. Graphics Appl. 12, 72–80.
(doi:10.1109/38.135915)
Rogowitz BE, Treinish LA, Bryson S. 1996 How
not to lie with visualization. Comput. Phys. 10,
268–273. (doi:10.1063/1.4822401)
Brewer CA. 1997 Spectral schemes: controversial
color use on maps. Cartogr. Geogr. Information
Syst. 24, 203–220. (doi:10.1559/
152304097782439231)
Rogowitz BE, Treinish LA. 1998 Data
visualization: the end of the rainbow.
IEEE Spectr. 35, 52–59. (doi:10.1109/6.
736450)
Light A, Bartlein PJ. 2004 The end of the
rainbow? Color schemes for improved data
graphics. Eos Trans. Am. Geophys. Union 85,
385–391. (doi:10.1029/2004EO400002)
Borland D, Taylor RM. 2007 Rainbow color map
(still) considered harmful. IEEE Comput. Graph.
Appl. 27, 14–17. (doi:10.1109/MCG.2007.
323435)
Moreland K. 2016 Why we use bad color maps
and what you can do about it. Electr. Imaging

## PDF page 15

60.

64.

65.

66.

variation in cranial design. J. Exp. Biol. 224,
jeb234831. (doi:10.1242/jeb.234831)
Ferrón HG, Martínez-Pérez C, Rahman IA, Selles
de Lucas V, Botella H, Donoghue PC. 2021
Functional assessment of morphological
homoplasy in stem-gnathostomes. Proc. R. Soc.
B 288, 20202719. (doi:10.1098/rspb.2020.2719)
Lautenschlager S. 2021 True colours or red
herrings?: colour maps for finite-element
analysis in palaeontological studies to enhance
interpretation and accessibility. Figshare.

15

R. Soc. Open Sci. 8: 211357

Downloaded from https://royalsocietypublishing.org/ on 08 December 2024

62.

63.

colorspace: a toolbox for manipulating and
assessing colors and palettes. arXiv preprint
arXiv 1903.06490.
Mayhorn CB, Wogalter MS, Bell JL, Shaver EF.
2004 What does code red mean? Ergonomics
Design 12, 12–14. (doi:10.1177/1064804604
01200404)
Dutel H, Gröning F, Sharp AC, Watson PJ,
Herrel A, Ross CF, Jones ME, Evans SE,
Fagan MJ. 2021 Comparative cranial
biomechanics in two lizard species: impact of

royalsocietypublishing.org/journal/rsos

61.

Schloss KB, Gramazio CC, Silverman AT, Parker
ML, Wang AS. 2018 Mapping color to meaning
in colormap data visualizations. IEEE Trans. Vis.
Comput. Graph 25, 810–819. (doi:10.1109/
TVCG.2018.2865147)
Sibrel SC, Rathore R, Lessard L, Schloss KB. 2020
The relation between color and spatial structure
for interpreting colormap data visualizations.
J. Vis. 20, 7. (doi:10.1167/jov.20.12.7)
Zeileis A, Fisher JC, Hornik K, Ihaka R, McWhite
CD, Murrell P, Stauffer R, Wilke CO. 2019
