Source: see manifest row of the PDF
PDF sha256: 0661c5296d36a3c01e7604fa24c41d676789525f20177aeabea9bdc91f05cf29
License: CC-BY-3.0
Language: eng
Fidelity: machine (failed: repetition)

# Transcription of westhoff_zehe_2013_maximum_entropy_production_conceptual_hydrological_models.pdf

Transcription of `westhoff_zehe_2013_maximum_entropy_production_conceptual_hydrological_models.pdf` in this directory, 17 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-17 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Hydrology and
Earth System
Sciences

Open Access

Ocean Science

Open Access

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013
www.hydrol-earth-syst-sci.net/17/3141/2013/
doi:10.5194/hess-17-3141-2013
© Author(s) 2013. CC Attribution 3.0 License.

cess

Model Development

Solid Earth

M. C. Westhoff and E. Zehe

Open Access

Maximum entropy production:
can it be used to constrain conceptual hydrological models?

The Cryosphere

Correspondence to: M. C. Westhoff (martijn.westhoff@kit.edu)

Received: 20 September 2012 – Published in Hydrol. Earth Syst. Sci. Discuss.: 9 October 2012
Revised: 26 June 2013 – Accepted: 2 July 2013 – Published: 5 August 2013

Abstract. In recent years, optimality principles have been
proposed to constrain hydrological models. The principle of
maximum entropy production (MEP) is one of the proposed
principles and is subject of this study. It states that a steady
state system is organized in such a way that entropy production is maximized. Although successful applications have
been reported in literature, generally little guidance has been
given on how to apply the principle. The aim of this paper
is to use the maximum power principle – which is closely
related to MEP – to constrain parameters of a simple conceptual (bucket) model. Although, we had to conclude that
conceptual bucket models could not be constrained with respect to maximum power, this study sheds more light on how
to use and how not to use the principle. Several of these issues have been correctly applied in other studies, but have
not been explained or discussed as such.
While other studies were based on resistance formulations,
where the quantity to be optimized is a linear function of the
resistance to be identified, our study shows that the approach
also works for formulations that are only linear in the logtransformed space. Moreover, we showed that parameters describing process thresholds or influencing boundary conditions cannot be constrained. We furthermore conclude that,
in order to apply the principle correctly, the model should be
(1) physically based; i.e. fluxes should be defined as a gradient divided by a resistance, (2) the optimized flux should
have a feedback on the gradient; i.e. the influence of boundary conditions on gradients should be minimal, (3) the temporal scale of the model should be chosen in such a way that
the parameter that is optimized is constant over the modelling
period, (4) only when the correct feedbacks are implemented
the fluxes can be correctly optimized and (5) there should

Open Access

Department of Hydrology, Institute for Water and River Basin Management, Karlsruhe Institute of Technology – KIT,
Kaiserstr. 12, 76131 Karlsruhe, Germany

be a trade-off between two or more fluxes. Although our application of the maximum power principle did not work, and
although the principle is a hypothesis that should still be thoroughly tested, we believe that the principle still has potential
in advancing hydrological science.

1

Introduction

Traditionally, hydrology is concerned with predicting extremes or water balances for water resources management.
But the simplified model structures induce errors, while
model parameters are often calibrated on an observed integrated catchment response (often discharge). In recent years,
optimality based principles have been suggested to be able to
better estimate model parameters and thus model behaviour
(e.g. McDonnell et al., 2007; Kleidon and Schymanski, 2008;
Clark et al., 2011; Schaefli et al., 2011; Thompson et al.,
2011).
The basic idea of optimality principles is that nature organizes itself in such a way that its functioning is optimal under given external forcing during steady state conditions. This can be simulated by taking into account competition between different plant species or trade-offs between
fluxes that are driven by different gradients. This competition should then be translated into an objective function.
For example, Rodriguez-Iturbe et al. (1999), Porporato et al.
(2001) and Caylor et al. (2009) minimized water stress as
the objective function for vegetation in (semi-)arid areas.
Maximum transpiration and minimal water and oxygen stress
have been used by Brolsma and Bierkens (2007), who simulated the competition between two vegetation species, while

Published by Copernicus Publications on behalf of the European Geosciences Union.

## PDF page 2

3142

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

Schymanski et al. (2009b) optimized net carbon profit under
given environmental conditions. Another proposed organizing principle is the maximum entropy production principle
(MEP) (McDonnell et al., 2007; Kleidon and Schymanski,
2008; Kleidon, 2009, 2010a,b; Zehe and Sivapalan, 2009;
Schaefli et al., 2011). However, in the hydrological community it remained – so far – mainly on the visionary level.
The above mentioned studies are just a few examples
of optimality based models (mainly) in ecohydrology. For
a more extensive review, the reader is referred to e.g.
Schymanski et al. (2009a).
Several different optimality principles have been used so
far, and the question is which one to use. Paik and Kumar
(2010) stated that many optimality principles are useful,
but that MEP has at least a physical background. Although
the physical background of MEP is still under debate, (e.g.
Dewar, 2009, suggests that MEP is rather a statistical principle, where the state of MEP is just the most probable one), it
seems a useful principle, and many of the proposed objective
functions are related to MEP (Dewar, 2010). It is also the objective function used in this study (in which we use it as a
physical principle).
The principle of MEP relies on the fact that a gradient
drives a flux, while the same flux depletes the gradient. This
has been clearly shown by Paltridge (1979) and Lorenz et al.
(2001) who used the principle to explain the observed atmospheric movement from the Equator to the poles for planetary systems. Dewar (2010) showed how MEP could be used
for plant optimization at different scales, but a comparison
with observations was missing. A more hydrological application was formulated by Kleidon and Schymanski (2008),
who used the principle to describe the partitioning between
runoff and evaporation, but they also did not test their theory
with observations. Schymanski et al. (2010) used a simple
2-box model and MEP to predict pattern formation of vegetation in semiarid regions, which gave similar results as the
large-scale distributed model of Klausmeier (1999).
Comparison with observations has been done by Zehe
et al. (2010), who used the principle of maximum energy dissipation (which is equivalent to MEP) to explain the observed
larger density of worm burrows at the foot of the hillslope
compared to the hill top. However, they were not able to explain the total number of observed worm burrows.
Another example was illustrated by Porada et al. (2011),
who used MEP to constrain parameters for a physically based
model based on multiple 1-D columns to simulate the water balance of the largest 35 catchments on Earth. Two parameters were constrained with respect to MEP; namely, resistance for root water uptake by maximizing entropy produced by rootwater uptake and hydraulic conductivity by
maximizing entropy produced by baseflow. Subsequently
they ranked the different hydrological processes with respect
to the produced entropy. They found that transpiration has
the strongest contribution to annual average entropy production. However, limited guidance was given on why only two
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

parameters were constrained with the MEP principle, or why
entropy production of only certain fluxes were optimized
(and not the entropy produced by the entire system). Also,
comparison between observed and simulated fluxes was only
in terms of the long-term average water balance. Their work
was a key motivation for our work, in which we use a conceptual bucket model that is easy to constrain to reproduce
and predict rainfall runoff response, but appeared not so easy
to constrain with respect to MEP.
Thus, so far, MEP has been suggested as a promising
method in hydrology, but optimized model structures have
not been extensively tested against observations: the added
value of MEP for parameter estimation has not been explored
yet. The aim of this paper is to use the MEP principle (although we used the equivalent maximum power principle) to
constrain parameters of a bucket model. Guidance is given
on which parameters can possibly be constrained with MEP
and if these optimal parameter values indeed lead to realistic
model performance. We start with constraining each parameter individually, and progressively try to constrain two or
more parameters at a time.
This study reveals two main problems of using MEP to
constrain conceptual models. The first is that most conceptual models are based on a set of connected (non-)linear
reservoirs where outgoing fluxes only depend on the state
of its reservoir of origin, which reduces the possibility for
process interactions and trade-offs between fluxes. The second problem is that several fluxes in conceptual hydrological models are not driven by potential gradients, which is
of prime importance for calculating entropy production or
power produced by these fluxes.

2

Short introduction to MEP

In this section we give a short introduction to MEP, with an
emphasis to the application of this article. For a more detailed
and fundamental description of MEP, the reader is referred
to e.g. Kondepudi (2008), Kleidon (2010b) or Kleidon et al.
(2013).
The second law of thermodynamics states that entropy
cannot be consumed but only produced. This is the case during irreversible processes that cannot be reversed in time. For
isolated systems this implies that the system evolves to a state
of maximum entropy, which, for gases and fluids, implies
perfect mixing. Perfect mixing means depletion of all gradients: the system is in a state of maximum disorder.
Open systems may, however, exchange energy and mass
with their environment. Organized structures may form and
persist when incoming fluxes provide the necessary free energy and entropy is exported to the environment. Persistent exchange of energy flows through the system requires
a persistent macroscale driving gradient that spans across the
entire system. The Bernard cell (Prigogine, 1989) but also
planet Earth (Kleidon, 2010b) are prominent examples. The
www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 3

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
fluxes along such macroscale gradients would deplete their
driving gradient if there would be no external forcing. In the
Bernard cell this is the heating at the bottom and cooling at
the top of the cell. In planet Earth this is planetary energy exchange (the poles receive less radiation input than the Equator). The MEP principle now states that such an open system
in steady state is structured in such a way that it maximizes
entropy production. In case of no external forcing this implies that the system reaches thermodynamic equilibrium as
fast as possible.
In the remainder of this paper we use the principle of maximum power, which is closely related to MEP. Following
Kleidon et al. (2013), we start with expressing the internal
energy dU [J] as
∑
dU = d (T S) − d (pV ) +
d (Mk 8k ) ,
(1)

Peff

k

Rearranging Eq. (2) and dividing it by a change in time dt,
yields
(3)

Since 8k dMk /dt is a flux times a gradient (which is power),
power is proportional to entropy production and maximizing
one is the same as maximizing the other.
Model set-up

For the MEP principle to work the system should be in steady
state. We therefore focused on the average yearly water balance, which we assume to reflect steady state partitioning of
rainfall into hydrological fluxes (Kleidon et al., 2013). We
used a simple bucket model to which we applied the maximum power principle. The model used is in accordance with
several bucket models such as e.g. the HYMOD conceptual
watershed model (Moore, 1985), the HBV model (Lindström
et al., 1997), the GR4J model (Perrin et al., 2003) or the SUPERFLEX model environment (Fenicia et al., 2011) which
all have been successful in reproducing discharge in many
hydrological settings.

www.hydrol-earth-syst-sci.net/17/3141/2013/

SM

FCSmax

G

S1

Qd

Q0

L

Q1

S

2

Q

2

where T is absolute temperature [K], S in entropy [J K−1 ],
p is pressure [N m−2 ], V is volume [m3 ], Mk is the mass
of matter within the system [kg] and 8k its corresponding
chemical potential (or energy level) [m2 s−2 ]. If we now consider a steady state, so that dU = 0, dT = 0 (we neglected
effects from sensible heating/cooling of the soil, as temperature gradients do not drive water fluxes in the subsurface),
dp = 0, dV = 0, d8k = 0 and incoming fluxes equal outgoing fluxes, then Eq. (1) can be simplified to
∑
dU = 0 = T dS +
8k dMk .
(2)

3

Ea

Smax

k

1∑
dMk
dS
=
−8k
.
dt
T k
dt

3143

Fig. 1. Model set-up. For meaning of the variables, see Sect. 3.

Testing the MEP hypothesis using a bucket model implied
two main difficulties. The first was to design a soil moisture accounting scheme that is simple but nevertheless based
on interpretable parameters (see Sect. 3.1). The second was
to define proper descriptions of driving gradients since most
bucket models do not account for the real gradients that drive
these fluxes in an explicit manner. The used expressions for
the driving gradients were thus not always derived from first
principles, but they were constructed on plausible reasoning. An intensive discussion on the gradients is added in
Sect. 6.2.1.
All fluxes in the model are described in m s−1 per unit
area giving power the unit of W m−2 . The model was run
on a hourly time step and solved with an implicit numerical
scheme.
3.1

Unsaturated zone

The model is similar to the HBV model with the difference
that the fast runoff reservoir is now fed directly from the unsaturated zone. (Fig. 1). For simplicity we assumed no snowfall and interception. The water balance of the bucket is given
by
dSM
= Peff − Ea − Qd − G,
dt

(4)

where SM is the water storage in the bucket [m], Peff and Ea
are the effective rainfall (the precipitation that actually infiltrates into the soil) [m s−1 ] and actual evapotranspiration
[m s−1 ] and Qd and G are the overland flow [m s−1 ] and
groundwater percolation [m s−1 ], while t is time [s]. Actual
evaporation and its driving gradient are given by

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 4

3144

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

a

b

5

2

W/m ]

2

W/m ]

−4

P [10

−4

3

P [10

2
1

4
3
2
1

0

0

500

50

Qerr [mm/year]

Qerr [mm/year]

6
5

4

0
−500
−2

10

−1

0

10

1

10

2

10

0
−50
−100

3

10

0

10

0.2

0.4

β [−]

c

0.6

0.8

1

F [−]
C

d

6

4

2
1
0

Qerr [mm/year]

Qerr [mm/year]

0
−20
−40
−10

10

−8

10

5

−6

10
Ks [−]

−4

−2

10

10

0
−100
−200
−300
200

400

600

800
Smax [−]

1000

1200

PQ

2

W/m ]

1

Ptot
4

d

3

PG

−4

P [10

2

0

20

e

3

2

W/m ]

−4

P [10

2

3

P [10

4

−4

W/m ]

5

2

PE

a

Qerr [mm/year]

1
0
400
200
0
−200
0

0.1

0.2
0.3
albedo [−]

0.4

0.5

Fig. 2. Sensitivity of (a) β, (b) FC , (c) Ks , (d) Smax and (e) albedo to power of the different fluxes leaving the unsaturated zone and associated
mass balance error for the HJ Andrews watershed 2. Total power is plotted in blue, power by Qd in light cyan, power by G in red and power
by Ea in dark cyan. The dotted and dashed lines represent two different parameter sets (see Table 1).

(
Ea = Epot min

)
SM
,1 ,
Smax FC

(5)

∇Ea = es − ea ,
where Epot is the potential evaporation [m s−1 ], determined
with the Penman formula (Monteith, 1981). Note that the
albedo [−] is treated as a calibration parameter: a large
albedo means more reflection of solar radiation leading to
less potential evaporation. Smax is the maximum storage of
the bucket [m], and FC is the field capacity [−]. Although
this is not a soil physical field capacity, this parameter can
be interpreted in a soil physical sense. Soils with high clay
content store a large amount of water against gravity. Hence,
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

FC should be close to 0.8. Sandy soils have a low field capacity, thus FC should be around 0.1. ∇Ea is the gradient driving
evaporation [N m−2 ] and es and ea are the saturated and actual water vapour pressure [N m−2 ], where ea = H es , with
H being relative humidity [−]. Thus, the driving gradient is
defined as the water vapour demand of the atmosphere.
Overland flow and its driving gradient are given by
(
)
SM β
Qd = Peff
,
(6)
Smax
(
)
ρg
SM β
∇Qd =
SM
,
η
Smax

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 5

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
where β is a scaling parameter accounting for the catchment
heterogeneity of the depth of the unsaturated soil [−] and
∇Qd is the gradient [N m−2 ] driving Qd , while ρ, g and η are
the water density [kg m−3 ], gravitational acceleration [m s−2 ]
and soil porosity [−], respectively. The driving gradient is
thus derived as the potential energy multiplied by the scaling
factor (SM /Smax )β . Reasoning for this scaling factor is that
we interpreted Qd as fast runoff from the hillslope, where
saturation starts at the bottom of the slope. The value of β
determines which fraction of the hillslope is saturated for a
certain value of SM . The driving gradient is thus expressed
as a sort of weighted average of these potential energies.
Groundwater percolation and its driving gradient are given
by
)
(
SM β
for SM > Smax FC ,
(7)
G = Ks
Smax
ρg
max (0, SM − Smax FC ) ,
∇G =
η
where ∇G is the gradient driving G [N m−2 ], and Ks is the
hydraulic conductivity of the soil [m s−1 ]. Note that the driving gradient is expressed as a potential gradient above field
capacity, and that, though being simple, this conceptualization of percolation can be parameterized in a manner that is
consistent with soil physics. For instance a sandy soil has
a high Ks , around values of 10−4 m s−1 , in combination with
a small value of FC which leads to a physically consistent
behaviour of percolation and direct runoff production. The
opposite is true for finer grained soils.
3.2

Fast runoff reservoir

The water balance for the fast runoff reservoir (middle bucket
in Fig. 1) is given by
dS1
= Qd − Q0 − Q1 .
dt

(8)

The fluxes and driving gradients of Q0 and Q1 [m s−1 ] are
given by
Q0 = max (S1 − L, 0) k0 ,
ρg
∇Q0 =
max (S1 − L, 0) ,
η
Q1 = S1 k1 ,
ρg
∇Q1 =
S1 ,
η

(9)

(10)

where S1 is the storage height [m], L is the storage threshold
level [m] above which Q0 becomes active and k0 and k1 are
the reservoir constants [s−1 ]. The driving gradients are both
given as a potential energy.

www.hydrol-earth-syst-sci.net/17/3141/2013/

3.3

3145
Slow runoff reservoir

The water balance for the slow runoff reservoir (lowest
bucket in Fig. 1) is given by
dS2
= G − Q2 ,
dt

(11)

where Q2 [m s−1 ] is given by
Q2 = S2 k2 ,
ρg
∇Q2 =
S2 ,
η

(12)

where S2 is the storage height [m] and k2 is the reservoir
constant [s−1 ].
4

Data and calibration procedure

We applied the model to two different watersheds: the
first is watershed 02 of the HJ Andrews experimental forest (OR, USA, latitude 44◦ 12′ 43.254′′ N, longitude
122◦ 14′ 41.554′′ W). For a detailed description of the watershed the reader is referred to e.g. Rothacher (1965);
Rothacher et al. (1967) or Tague and Band (2001). Here we
give only a short description.
The watershed has a surface area of 60 ha with elevations
ranging from 545 to 1070 m, and a mean slope of 30 %. The
catchment is completely forested, primarily by mature Douglas fir. The underlying bedrock is volcanic material from
the Oligocene to lower Miocene which is overlain by a thick
layer of weathered, unconsolidated material of generally high
porosity (∼ 0.6) and hydraulic conductivity (∼ 90 m day−1 )
(Tague and Band, 2001).
Winters are generally cool and wet, while summers are
warm and dry. Precipitation over the study period ranges
from 1300 to 3000 mm yr−1 with a mean of 2222 mm yr−1 .
Mean runoff is 1380 mm yr−1 . In general, there is no seasonal snow pack in winter, but daily to weekly snow accumulation does occur.
We used meteorological data from the PRIMET (primary
meteorological) station located 900 m from the site (latitude
44◦ 12′ 42.8148′′ N, longitude 122◦ 15′ 21.3876′′ W; Daly and
McKee, 2011). The data set contains air temperature, solar radiation, relative humidity, precipitation and wind speed
on a 1 h time step. Discharge was taken from Johnson and
Rothacher (2009), also at an hourly time step. For our model
we used the time series from 14 September 1994 to 20 August 2006, of which the first 11 months were used as warming
up period.
The second watershed is the upper half of the Weiherbach
catchment in southwestern Germany. The watershed drains
an area of 3.5 km2 with gentle slopes characterized by a typical loess soil catena formed by erosion with soil depths ranging between 15 and 30 m. At the foot of the hillslopes the soil
consists of moist but drained Colluvisols while in the upper
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 6

3146

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

hillslope sections drier Calcaric Regosols are found. Porosity
of the soils is in the order of 0.3–0.4 with hydraulic conductivities ranging between 0.26 and 3.4 m day−1 (Zehe et al.,
2006). The total catchment area used for cultivation of agricultural crops or pasture is 95 %, 4 % is forested and 1 % is
paved area. Runoff is dominated by a relative constant baseflow combined with short peaks of Hortonian overland flow.
The climate is semi humid with an average annual
precipitation of 800 mm yr−1 , average annual runoff of
150 mm yr−1 , and annual potential evapotranspiration of
775 mm yr−1 . For this study, we used discharge data
from gauge Menzingen (latitude 49◦ 08′ 09.63′′ N, longitude
8◦ 44′ 44.51′′ E) and air temperature, solar radiation, relative humidity, precipitation and wind speed were measured
within the catchment. All measuring intervals were ≤ 1 h. For
this study we used the time series from 1 November 1990 to
1 November 1996, of which the first 12 months were used as
warming up period.
In a first step, we varied only one parameter (while all
other parameters were arbitrarily chosen) and determined the
power of each flux. Because no feedbacks were implemented
between the different reservoirs, we could analyse each reservoir separately. For the unsaturated zone, we compared the
simulated cumulative∑
yearly fluxes
∑ with the observed one,
expressed as Qerr = Qobs − (Qd + G) [mm yr−1 ]. If
the landscape is shaped according to maximum power, and
the model appropriately represents for the energy conversions associated with partitioning of rainfall into evaporation,
and fast and slow runoff components, a maximum in power
should correspond with Qerr ≈ 0.
To compare simulations of the fast and slow runoff reservoirs with observations, we nevertheless combined the three
fluxes Q0 , Q1 and Q2 to be able to compare it with the complete runoff time series. These runoff reservoirs are fed by
fluxes from the unsaturated zone, which we parameterized
in such a way that the long-term water balance is closed
(Qerr ≈ 0).
In a second step we only took those parameters that could
be constrained in the first step and varied two of these parameters at the same time, provided that the two parameters parameterize the same reservoir. Again, the power of each flux
was determined and the model output was compared with
observations in the same way as in the first step.
5

Results

5.1

Constraining one free parameter

In our first step, we tried to constrain one parameter at a time
while keeping all other parameters constant.
5.1.1

Unsaturated zone

For the unsaturated zone, results for two different parameter sets are shown (Figs. 2, 3, solid and dashed lines; the
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

parameter values for each run are listed in Table 1). For the
HJ Andrews (Fig. 2), the shown simulations are done with
parameter sets that resulted in a closed water balance that coincides with maximum power along a range of β (panel a):
for the solid lines this is maximum power in G (PG ), and for
the dashed line this corresponds to maximum power in Qd
(PQd ) and in total power (Ptot ). Note, however, that in many
other combinations of the fixed parameters, a closed water
balance did not coincide with maximum power in any of the
fluxes and since parameters for these kind of models can often not be directly measured in the field, the values of each
fixed parameter are in principle arbitrary.
Most power was produced by either G or Qd . Power produced by Ea (PEa ) was relatively small and insensitive over
the parameter spaces. The reason for this is that none of the
parameters influenced the gradient driving Ea and no feedback between the flux (Ea ) and its driving gradient (∇Ea )
was implemented in the used model set-up. In contrary to
the model of Porada et al. (2011), conceptual models do not
account for the capillary rise and the associated power in this
flux.
For the parameters FC , Smax and albedo, power is maximum at the boundaries of the parameter space (Fig. 2b, d, e),
which means they could not be constrained with respect to
power. Nevertheless, two parameters do result in maxima in
power, namely β and Ks (Fig. 2a, c).
β results in both maximum power by G (for large β) and
maximum power by Qd (for small β): both fluxes that are
directly influenced by β. For β larger than 50, the water balance becomes insensitive, which is due to the fact that for
such a large β the water level (SM ) should be so close to the
maximum water level (Smax ) to produce direct runoff that it
practically functions as a binary threshold where β becomes
insensitive. Such a large β represents a catchment with a uniform soil depth.
Along Ks , a maximum in power by G appeared. But with
the chosen fixed parameters, the water balance is rather insensitive over the full range of Ks , which is caused by the
relatively large value of FC . Although we tested many different combinations of fixed parameters for which a maximum in power along Ks appeared (results not shown here),
we could not find a parameter set at which a closed water
balance coincided with a maximum in power at the observed
value (by Tague and Band, 2001) of Ks = 1 × 10−3 m s−1 .
For the Weiherbach catchment we could only find a β
where a closed water balance corresponded with a maximum
in PG (Fig. 3a), while a maximum in PQd always corresponded with a large error in the water balance: in the shown
case this error is −362 mm yr−1 , which is almost half of the
yearly rainfall. Nevertheless we used this optimum value for
β as fixed parameter when testing the other parameters.
Similar to the results of the HJ Andrews, maxima in power
could only be found for β (Fig. 3a) and for Ks (Fig. 3c). However, for the latter this is not always the case (see solid line in
Fig. 3c). This happens when the fixed parameters are chosen
www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 7

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

a 0.5

b

0.5

P [10−4 W/m2]

0.4

0.3
0.2

0.3
0.2

0.1

0.1

0
200

0
Qerr [mm/year]

Qerr [mm/year]

P [10−4 W/m2]

0.4

3147

0
−200
−400
−600
−2

10

−1

0

10

1

10

2

10

3

10

0
−200
−400
−600
0

10

0.2

0.4

β [−]

0.6

0.8

1

FC [−]

c 0.5

d

0.8

P [10−4 W/m2]

0.3
0.2

0.6
0.4

0.1

0.2

0
200

0
Qerr [mm/year]

Qerr [mm/year]

P [10−4 W/m2]

0.4

0
−200
−10

10

−8

10

e 0.5

−6

10
Ks [−]

−4

−2

10

0
−200
−400
200

10

600

800
1000
Smax [−]

1200

1400

Ptot

0.4
P [10−4 W/m2]

400

PQ

d

0.3

PG

0.2

PE

a

0.1

Qerr [mm/year]

0
0
−100
−200
−300
0

0.1

0.2
0.3
albedo [−]

0.4

0.5

Fig. 3. Sensitivity of (a) β, (b) FC , (c) Ks , (d) Smax and (e) albedo to power of the different fluxes leaving the unsaturated zone and associated
mass balance error for the Weiherbach catchment. Total power is plotted in blue, power by Qd in light cyan, power by G in red and power
by Ea in dark cyan. The dotted and dashed lines represent two different parameter sets (see Table 1).

in such a way that the water level will never be larger than
the threshold FC Smax that should be exceeded to get groundwater percolation G. In these cases, Ks is insensitive. What
is also striking is that when G = 0, the error in the water balance is rather insensitive for Smax (Fig. 3d). This means that
for larger values of Smax , Qd remains almost constant, while
power only increases due to the larger gradient driving Qd .
Contrary to the model results of HJ Andrews is that in
many cases most power is produced by evaporation (PEa ),
while power produced by G is always small and power produced by Qd is only in some cases large. But the latter cases
correspond with a large error in the water balance. The main
reason for these results is that the runoff coefficient is rather
www.hydrol-earth-syst-sci.net/17/3141/2013/

low (< 20 %) meaning that the evaporative flux is relatively
large, leading to large power by Ea .
5.1.2

Fast runoff reservoir

We followed the same procedure for the fast runoff reservoir.
Since the fast runoff reservoir is fed by Qd from the unsaturated zone, the unsaturated zone had to be parameterized as
well. Here, we focus only on results from HJ Andrews because for the Weiherbach catchment the maximum in PQd
only existed for large water balance errors, making results
for the fast runoff reservoir by definition unreliable, while
the maximum in PG only appeared for Qd = 0, meaning that
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 8

3148

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

Table 1. Parameter sets used for each model run.

Fig. 2 – solid line∗∗
Fig. 2 – dashed line∗∗
Fig. 3 – solid line∗∗
Fig. 3 – dashed line∗∗
Fig. 4a1 – solid line
Fig. 4a1 – dashed line
Fig. 4a2 – solid line
Fig. 4a2 – dashed line
Fig. 4a3 – solid line
Fig. 4a3 – dashed line
Fig. 4b1 – solid line
Fig. 4b1 – dashed line
Fig. 4b2 – solid line
Fig. 4b2 – dashed line
Fig. 4b3 – solid line
Fig. 4b3 – dashed line
Fig. 5 – solid line
Fig. 5 – dashed line
Fig. 6a
Fig. 6b
Fig. 7a
Fig. 7b
Fig. 7c
Fig. 7d

β
[−]

FC
[−]

Ks
[m s−1 ]

Smax
[mm]

albedo
[−]

63.1
0.71
0.25
3.98
63.1
63.1
63.1
63.1
63.1
63.1
0.71
0.71
0.71
0.71
0.71
0.71
63.1
0.71

0.6
0.7
0.6
0
0.6
0.6
0.6
0.6
0.6
0.6
0.7
0.7
0.7
0.7
0.7
0.7
0.6
0.7
0.6
0.7
0.6
0.6
0.7
0.7

1 × 10−6
1 × 10−7
1 × 10−6
1 × 10−3
1 × 10−6
1 × 10−6
1 × 10−6
1 × 10−6
1 × 10−6
1 × 10−6
1 × 10−7
1 × 10−7
1 × 10−7
1 × 10−7
1 × 10−7
1 × 10−7
1 × 10−6
1 × 10−7

800
1200
800
500
800
800
800
800
800
800
1200
1200
1200
1200
1200
1200
800
1200
8 00
1200
800
800
1200
1200

0.43
0.05
0.43
0.05
0.43
0.43
0.43
0.43
0.43
0.43
0.05
0.05
0.05
0.05
0.05
0.05
0.43
0.05
0.43
0.05
0.43
0.43
0.05
0.05

63.1
63.1
0.71
0.71

1 × 10−6
1 × 10−6
1 × 10−7
1 × 10−7

L
[mm]

k0
[s−1 ]

0.5
0.1
50
100
50
50

50
100
50
50
50
50

50
100
50
100

0.1
0.5
0.5
0.1

0.1
0.5
0.1
0.1

k1
[s−1 ]

0.1
0.02
0.02
0.1

0.1
0.02
0.02
0.1

k2∗
[s−1 ]

0.01
0.01
0.01
0.01
0.01
0.01
0.01
0.01
0.01
0.01
0.01
0.01

0.2
0.2

0.01
0.01
0.01
0.01

Catchment
HJ-Andrews
HJ-Andrews
Weiherbach
Weiherbach
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews
HJ-Andrews

∗ The slow runoff reservoir was added to be able to compare simulated runoff with the observed one. ∗∗ All parameters were fixed, except the one varied along

the x axis.

no water flows into the fast runoff reservoir. The latter case
is, however, consistent with the way the catchment functions.
For the HJ Andrews, the chosen parameter sets for the
unsaturated zone came from the solid and dashed line in
Fig. 2a, where a closed water balance coincides with maximum power for G (solid line in Fig. 2a and panels a1 –a3
in Fig. 4) or Qd (dashed line in Fig. 2a and panels b1 –b3 in
Fig. 4). For both cases we showed again results of two sets
of fixed parameters (see Table 1).
For parameter L, which represents the threshold above
which Q0 becomes active, no maximum in power occurs
(Fig. 4a1 , b1 ). For large values of L, power only tops off
and becomes flat. This is due to the fact that, given certain
forcing and reservoir constants (k0 and k1 ), the water level in
the reservoir will have a certain maximum. If L is larger than
this water level, it has no influence on the fluxes anymore and
thus no influence on the power either.
For k0 and k1 , a maximum in power is observed in the corresponding fluxes: thus a maximum in PQ0 for k0 (Fig. 4a2 ,
b2 ) and in PQ1 for k1 (Fig. 4a3 , b3 ). Note that a maximum
in power in panels a1 –a3 are an order of magnitude smaller
than in panel b1 –b3 : this is due to the fact that the input flux
Q0 is much smaller for panels a1 –a3 .

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

Besides the maxima in power by the Q0 and Q1 , a maximum in total power (Ptot ) only appears (but not always) for
k1 (Fig. 4a3 , b3 ) and the location of this maximum is always
close to the location of maximum power by Q1 . This is not
strange, since PQ1 is for most cases larger than PQ0 . Only
when the water level becomes sufficiently higher than threshold L (which only occurs for small values of k1 ), PQ0 may
become larger than PQ1 .
The link to observations is made by looking at the Nash–
Sutcliffe model efficiency (NSE) of simulated vs. observed
discharge. To do this properly, total runoff should be compared which means that runoff by the slow runoff reservoir
should also be added. Therefore, we gave k2 the arbitrary
value of 0.02 s−1 . Note that this value has little influence for
the simulations in panels b1 –b3 , since G (the flux flowing to
the slow runoff reservoir) is only about 2 % of Qd : thus 98 %
of the total runoff is produced by the fast runoff reservoir.
For most cases, the maximum in power is far away from
the maximum in NSE. Only for one (shown) case the two
correspond (Fig. 4b3 , dashed line). Although the variation in
NSE is rather small over the full parameter space, this parameter set may be an optimal one. However, this may also
be a coincidence (see Sect. 6.1).

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 9

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

b1

0.15

P [10−4 W/m2]

P [10−4 W/m2]

a1 0.2
0.1
0.05

0.5

0

2
1.5
1
0.5
0
1

NSE [−]

NSE [−]

0
1

3149

0

100

200

300

0.5

0

400

0

100

200

−1

a2 0.2

400

b2 2.5
2

0.15

P [10−4 W/m2]

P [10−4 W/m2]

300

L [s−1]

L [s ]

0.1
0.05

1.5
1
0.5
0
1

NSE [−]

NSE [−]

0
1

0.5

0

0

0.2

0.4

0.6

0.8

0.5

0

1

0

0.2

0.4

k0 [s−1]

0.6

0.8

a3 0.1

0

b3 0.8

P

tot

P [10−4 W/m2]

0.06
0.04

0

0
1

0
1

0

0.2

0.4

0.6

0.8

1

−1

k1 [s ]

PQ

0.4
0.2

0.5

PQ

0.6

0.02

NSE [−]

NSE [−]

P [10−4 W/m2]

0.08

0

1

k [s−1]

1

0.5

0

0

0.2

0.4

0.6

0.8

1

k1 [s−1]

Fig. 4. Sensitivity of (1) L, (2) k0 and (3) k1 to power of the different fluxes leaving the fast runoff reservoir and associated mass balance
error for the HJ Andrews watershed 2. The input flux (Qd ) for simulations in panels a1 –a3 are derived from the point of maximum power in
G of the solid line in Fig. 2a, while the input flux for simulations in panels b1 –b3 are derived from the point of maximum power in Qd of
the dashed line in Fig. 2a. Total power is plotted in blue, power by Q0 in light cyan and power by Q0 in red. The dotted and dashed lines
represent two different parameter sets (see Table 1).

5.1.3

Slow runoff reservoir

The same procedure was also followed for the slow runoff
reservoir, albeit that this reservoir has only one parameter
and one flux leaving the reservoir. This reservoir is fed by G
coming from the unsaturated zone and the presented results
were obtained with the same two unsaturated zone scenarios
as for the fast runoff reservoir (see also Table 1). Although
we found a maximum in PG that corresponded to a closed
water balance for the Weiherbach catchment, we only show
www.hydrol-earth-syst-sci.net/17/3141/2013/

results from the HJ Andrews because results from both catchments are similar for this reservoir.
The obtained power by Q2 is at its maximum at the lower
end of k2 (Fig. 5). When thinking this over, this is not surprising, since the maximum power principle assumes a steady
state system, meaning that on average G = Q2 . This means
that the flux is fixed and that power is only influenced by the
driving gradient. Thus the smaller k2 is, the larger the gradient should be to obtain a large enough flux. Power is thus
maximum at the asymptote k2 → 0. This asymptote vanishes

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 10

3150

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

25

location where the “ridges” of the surface plots of the two
fluxes intersected.
We did the same here, and combined the two parameters that showed an optimum; i.e. β and Ks for the unsaturated zone (Fig. 6) and k0 and k1 for the fast runoff reservoir
(Fig. 7). If the approach of Porada et al. (2011) works here,
the intersect of the two ridges should coincide with a closed
water balance for the unsaturated zone and maximum NSE
for the fast runoff reservoir.
Also here, we focus only on results from the HJ Andrews,
because no reliable optimum for PQd could be found for the
Weiherbach catchment.

P [10−4 W/m2]

20
15
10
5

NSE [−]

0
1
0.5
0
−3
10

5.2.1
−2

10

−1

10

0

10

10

k2 [s−1]

Fig. 5. Sensitivity of k2 to power by flux Q2 that leaves the slow
runoff reservoir and the corresponding Nash–Sutcliffe model efficiency (NSE) for the HJ Andrews watershed 2. The input flux (G)
for the solid line was derived from the point of maximum power in
G of the solid line in Fig. 2a, while the input flux for the dashed line
was derived from the point of maximum power in Qd of the dashed
line in Fig. 2a (see Table 1 for the used parameters). The fast runoff
reservoir was also parameterized to be able to determine the NSE
of the total outflow.

when there are more fluxes leaving the reservoir, since Q2 is
then not fixed anymore.
When comparing these results with observed discharge,
maximum NSE occurs at relatively large values of k2 . Although the NSE is also influenced by the other reservoirs,
the low NSE for small values of k2 comes from the fact that
smaller k2 values lead to more constant outflow, meaning that
at maximum power (limk2 →0 ) the outgoing flux Q2 is completely constant.
5.2

Constraining two free parameters

For both the unsaturated zone and the fast runoff reservoir,
there were two parameters that showed a maximum in power.
For the unsaturated zone, we found several parameter sets
where a closed water balance coincided with a maximum in
power along one variable, and also for the fast runoff reservoir we found a parameter set where maximum NSE coincided with maximum power. However, this approach means
that only one parameter per submodule can be constrained
with the maximum power principle while the other parameters should be chosen in another manner.
Porada et al. (2011) proposed a method to be able to
constrain two parameters with respect to entropy production. They created surface plots with on the x and y axis
the two parameters and on the z axis the entropy produced
by the two fluxes that were controlled by the two parameters. They concluded that the optimal parameters were the
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

Unsaturated zone

1

For the unsaturated zone, this resulted in both local and
global maxima in total power (Ptot ) and power produced by
Qd (PQd ), a global maximum in power produced by G (PG )
and an almost flat surface in power produced by evaporation
(PEa ). PQd is characterized by a ridge at β ≈ 0.5 where Ks
is insensitive, while at the largest values of β power is maximum for the smallest values of Ks . This edge of the parameter space coincides with the global maximum in power.
For the first parameter set (Fig. 6a; see Table 1 for the used
parameters), the water balance is closed for β larger than 50,
which corresponds with the global maximum in Ptot , PQd
and PG . However, the global maxima of PQd and PG are located at opposite ends of the parameter range of Ks (panels a2
and a3 ). Also, the “ridges”, as used by Porada et al. (2011), do
not intersect: for PQd , the ridge only exists for Ks > 1×10−8
m s−1 (for smaller values a ridge exists along the full range of
β at Ks = 1 × 10−10 m s−1 , which is the edge of the parameter space), while for β < 1, no maximum in PG exists anymore (PG = 0). The point where the ridges almost overlap is
around Ks = 1 × 10−8 m s−1 and β = 0.5, but here the water
balance is far from being closed (Qerr = −283 mm yr−1 ).
For different values of Smax , FC and albedo, the surfaces of
the plots are similar to those created with the first parameter
set (Fig. 6b; see Table 1 for the used parameters). The main
difference is that the water balance is now closed around the
ridge in PQd . Thus the point where the ridges almost overlap coincides with a closed water balance. Following the approach of Porada et al. (2011), this should be the optimal
parameter set.
5.2.2

Fast runoff reservoir

As input to the fast runoff reservoir we used the same two
time series of Qd as in Sect. 5.1, of which the second is simulated with parameters close to the optimum defined after the
approach of Porada et al. (2011). For each of the two time series of Qd , results are shown for two different values of L:
Fig. 7a and b for the first time series and Fig. 7c and d for the
second, while k0 and k1 were varied. However, the different
values of L have only a minor effect.

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 11

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

P [10

0
3
10

[mm/year]

6
3

W/m ]

err

2

Q

Ptot

500

2

−4

10

β [−]

2

−2

−10

10

10

0

−7

10

10
10

−4

10

−7

10

a2

0
3
10

10

0

β [−]

K [m/s]
s

10
−2

−10

10

P

10

2

3

W/m ]

−4

2

W/m ]

−4

6

P [10

2

−4

10

β [−]

a

0
3
10

10

0

2

−10

10

10

0

−7

10

10
−2

10

−4

10

−7

10

β [−]

K [m/s]
s

10
−2

−10

10

10

K [m/s]
s

3
P

0
3
10

2
−4

3

W/m ]

6

P [10

2

G

P [10

W/m ]

−4

G

3

2

−4

10

a4

2

−10

10

10

0

−7

10

10
−2

10

−4

10

−7

10

β [−]

0
3
10

10

0

β [−]

Ks [m/s]

10
−2

P

b4

2

3

W/m ]

−4

a

6

P [10

2

W/m ]

−4

Ks [m/s]

E

P [10

0
3
10

10

P

a

3

−10

10

E

6

b

3

P
6

b2

d

P [10

0
3
10

s

Q

d

3

K [m/s]

P

Q

6

b1

Ptot

P [10

2
−4

3

W/m ]

6

0

−4

−500

a1

3151

2

−4

10

10

0
−2

−10

10

−4

10
−7

10

10
10

2

10

0

−7

10

β [−]

0
3
10

β [−]

Ks [m/s]

10
−2

10

−10

10

Ks [m/s]

Fig. 6. Sensitivity of β and Ks to power of the different fluxes leaving the unsaturated zone of the HJ Andrews watershed 2. Sensitivities for
two different sets of the parameters FC , Smax and albedo are shown (panels a, b; see Table 1 for the used parameters). The colour coding
shows the average error in the yearly water balance (Qerr ).

Although the “ridges” in panels 2 and 3 are sometimes difficult to see they do exist. The intersect of the ridges in PQ0
and PQ1 are always at values of k0 and k1 that are smaller
than 1 × 10−2 s−1 , where the NSE is relatively low. This also
applies for the case where Qd is (close to) optimal (Fig. 7c,
d). We can thus state that even if the unsaturated zone can be
correctly constrained by using the maximum power principle, it does not seem to work for the fast runoff reservoir.

www.hydrol-earth-syst-sci.net/17/3141/2013/

6

Discussion

The question of whether MEP and maximum power are indeed fundamental principles – such as the first or second
law of thermodynamics – is still under debate. Nevertheless,
several authors already showed their potential (e.g. Kleidon
and Schymanski, 2008; Schymanski et al., 2010; Zehe et al.,
2010; Porada et al., 2011; Kleidon et al., 2013), but generally little guidance was given on how to use the principle. For example, Kleidon and Schymanski (2008) set up a
simple model to illustrate how MEP could be used to estimate the resistance for root water uptake. Although they did
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 12

3152

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
0

a

0.2 0.4 0.6 0.8

b

tot

−1

10 −1
1

−1

10 −1

−1

2

−1

c2

P [10−4 W/m2]

10
5
0
−3
10
−2
10
−1
10

c3

Ptot

−1

10 −1

k1 [s−1]

−2

10

10
5
0
−3
10
−2
10
−1
−3
10
10

PQ

1

−1

10 −1

−2

10

10
5
0
−3
10
−2
10
−1
−3
10
10

PQ

2

−1

10 −1

1

−1

10 −1

−2

10

k0 [s ]

10
5
0
−3
10
−2
10
−1
−3
10
10
k1 [s−1]

−2

10

k0 [s ]

b3

PQ

2

−1

10 −1

−2

10

k0 [s ]

d1

Ptot

−1

10 −1

−2

10

d2

k [s ]
0

PQ

1

−1

10 −1

k1 [s−1]

k0 [s ]

b2

PQ

k1 [s−1]

0

−2

10

k0 [s ]

k1 [s−1]

k [s ]

k1 [s−1]

10
5
0
−3
10
−2
10
−1
10

−2

10

1
0.5
0
−3
10
−2
10
−1
−3
10
10

k0 [s ]

k1 [s−1]

−1

10 −1

−1

P [10−4 W/m2]

PQ

10 −1

tot

k1 [s ]

P [10−4 W/m2]

P [10−4 W/m2]

P [10−4 W/m2]
P [10−4 W/m2]

10
5
0
−3
10
−2
10
−1
10

−2

10

1
0.5
0
−3
10
−2
10
−1
−3
10
10

k0 [s ]

k1 [s−1]

c1

P [10−4 W/m2]

PQ

P

k1 [s−1]

k0 [s ]

k1 [s ]

1
0.5
0
−3
10
−2
10
−1
10

−2

10

1
0.5
0
−3
10
−2
10
−1
−3
10
10

P [10−4 W/m2]

1
0.5
0
−3
10
−2
10
−1
10

a3

P

k1 [s−1]

P [10−4 W/m2]

a2

NSE [−]

P [10−4 W/m2]

1
0.5
0
−3
10
−2
10
−1
10

P [10−4 W/m2]

1

P [10−4 W/m2]

1

−2

10

d3

k0 [s ]

PQ

2

−1

10 −1

−2

10

k0 [s ]

Fig. 7. Sensitivity of k0 and k1 to power of the different fluxes leaving the fast runoff reservoir of the HJ Andrews watershed 2. Two different
time series of the input flux Qd were used (one for panels a and b and one for c and d) and for two different values of L (see Table 1 for the
used parameters). The colour coding shows the NSE of the simulated runoff.

apply the principle in a correct way, they mainly stressed that
the principle works because there is a trade-off between a
flux and its gradient, but they did not explain explicitly that
there should also be a trade-off between two or more fluxes
– which is clearly demonstrated with our model results of
the slow runoff reservoir, where power is maximum at the
asymptote of k2 → 0 s−1 .
Also the study of Porada et al. (2011), which provides a
major motivation for the present study, applied and tested
MEP in a sophisticated manner to large catchments; however,
some of their findings were reported in a confusing or imprecise manner: they reported produced entropy by all fluxes,

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

while they only constrained two parameters of two different
fluxes using MEP. Thus only the produced entropy of these
two fluxes were relevant for their aim to constrain parameters of their hydrological model. This left room for this study
in which we tried to use the maximum power principle to
constrain a conceptual bucket model. During this exercise
we were confronted with the questions of what exactly we
should optimize, and if the model used was appropriate to
apply the principle.

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 13

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
6.1

What should and what can we optimize?

All of the above mentioned studies constrained a resistance
(or conductance) of a flux by maximizing entropy production
(or power) of that flux. But they neither explained clearly
why they only focused on resistances, nor did they explain
why they maximized entropy production of single fluxes (as
opposed to MEP of the whole system).
The answer of why only resistances were constrained is at
first glance rather simple: because resistances can mathematically be optimized with MEP (the word mathematically is
essential here, because mathematical optimum is not necessarily the same as the optimal structure or state of the real
world system). In this study we also showed that resistances
(or in our case conductances) could be constrained with respect to power, but we also showed in this study that β could
(at least mathematically) be constrained as well. Where resistances influence fluxes in a linear manner, the influence of
β on the flux is only linear in the log-transformed space. We
consider this as an important finding, since this may broaden
the applicability of MEP; for example, the soil moisture retention curve is also non-linear, and could thus be a candidate
to be (partly) parameterized using the MEP principle.
Parameters describing a process threshold (e.g. Smax , FC
and L) or parameters that influence boundary conditions
(e.g. albedo) could, on the other hand, not be constrained.
The reason that process thresholds cannot be constrained is
that a threshold only influences the driving gradient: a lower
threshold leads to a larger driving gradient of the flux that is
controlled by the threshold (see e.g. Fig. 4a1 , b1 , light cyan
lines). As a consequence, these parameters that cannot be
constrained with respect to power should, if they cannot be
directly measured in the field, be estimated in another way.
In this research we estimated them by constraining them in
such a way that the water balance was closed.
For the unsaturated zone this reduced the amount of behavioural parameter sets significantly, but did not lead to a
unique solution. However, when we added the runoff reservoirs, we did find a unique solution where a maximum
in power by Q1 corresponded with a maximum in NSE
(Fig. 4b3 ). Although this looks promising at first sight, we
believe it is rather coincidence than an inevitable result of
our approach. Because why does this optimum only appear
when optimizing β and k1 ? And how should one know on the
beforehand that one should optimize these two parameters, as
opposed to optimizing Ks and k0 ?
The reason why only entropy production of single fluxes
are maximized can be answered in a similar way: because
only then a maximum exists. But this question goes a little
deeper: we believe that if natures strives to a state of maximum power, nature strives to a state of maximum in total
power. Now let us consider the approach of Porada et al.
(2011). They constrained two parameters (resistance of two
different fluxes) at the same time and considered the intersect of the “ridges” of produced entropy by the two different
www.hydrol-earth-syst-sci.net/17/3141/2013/

3153

fluxes as the optimal one. In their model, produced entropy
by one flux was two orders of magnitude higher than produced entropy by the other flux. Thus the question arises,
why does nature not maximize entropy production by the first
flux? This may lead to lower entropy production by the second flux, but since this was two orders of magnitude smaller,
total entropy production will still be larger. However, if this
reasoning would be applied, entropy production by the first
flux would be maximum at the border of the surface plot,
meaning that no maximum exists. The results of our own
model show the same: the (global) maximum in total power
is often at the edge of the parameter space and can thus not be
optimized. This is especially clear in Fig. 7, panels 1, where
maximum total power is produced by the smallest values of
k0 and k1 . This is due to the fact that there is no feedback
implemented in the model that limits the power (or entropy
production) when there are two free parameters. Thus, we
cannot mathematically maximize total power and we come
back to the simple first answer: it is a mathematical issue.
This is in our opinion not strange, because if we want to
maximize total power, we should take all processes into account; at all spatial and temporal scales. This includes erosion, continental uplift, power created by biota, dissipation
of energy into heat, etc. But our models are simplifications
and many processes are considered constant at the temporal
or spatial scale of our model (e.g. continental uplift) or function as boundary conditions (e.g. potential evaporation).
The question is thus: does nature acts in a similar way,
where a fast process considers a slow process as constant and
where processes that are not (or to a minimum) influenced
by other processes see the other processes as boundary conditions? If this is indeed the case, maximizing power of single fluxes is indeed correct and the approach of Porada et al.
(2011) is a clever way to constrain two parameters simultaneously. However, although Porada et al. (2011) reported seemingly good results with their approach, they still reported differences in mean long-term observed and simulated runoff
of up to 300 % for temperate climates (estimated from their
Fig. 5b) which is for hydrological models too large (although
this difference may also be caused by other aspects).
Thus, to conclude, maximizing total power (or entropy
production) is practically impossible since all processes and
feedbacks should be taken into account, while maximizing
power of single fluxes show at least mathematically an optimum. But it still has to be foreseen if nature indeed behaves
like this.
6.2

How to apply the candidate principle?

In this study we applied the maximum power principle to
a conceptual bucket model and we found maxima in power
for several different parameter sets, of which one parameter set also coincided with a maximum in NSE. Also when
constraining two parameters simultaneously (with the approach of Porada et al., 2011) we found an optimum for the
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 14

3154

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

unsaturated zone that maximized power and had a closed
water balance. However, applying the same method for the
fast runoff reservoir, the parameters that were optimal with
respect to power were far from optimal with respect to reproducing observed discharge (Fig. 7). This means that the
mathematical optima we found, did not reflect the catchment
functioning.
Therefore we conclude that either the maximum power hypothesis is not valid or the model is not suitable for testing
the hypothesis. If we assume for now that the principle is
correct, our model is thus not suitable. This means that conversions of energies associated with rainfall runoff processes
are not represented in a feasible manner: conceptual models
have not been developed for this issue, but with the aim to
reproduce runoff.
Nevertheless, by applying the principle to our model we
gained more insight in how the principle should be applied
and why other authors applied the principle in the way they
did. We will discuss the following issues: (1) thermodynamic consistency; i.e. fluxes should be described as gradients divided by resistances, and (2) system boundaries and
feedbacks.
6.2.1

Flux = gradient divided by resistance

To be consistent with thermodynamic principles, each flux in
the model should be defined as a gradient divided by a resistance (or multiplied by a conductance), and power is then the
flux times the gradient; thus power is the gradient squared
divided by the resistance. In this way the flux has a feedback
to its gradient (as stressed by e.g. Kleidon and Schymanski,
2008); i.e. a larger flux depletes the gradient faster, and, consequently, the flux will be smaller. The resistance is then
treated as the unknown that can be constrained with the MEP
principle.
Our model concept is often not consistent with thermodynamics. An obvious one is Qd . Of course, SM is part of the
driving gradient, but as long as it does not rain, Qd and SM
have no connection at all, let alone a feedback. The reason
that this flux could be optimized is because the equation was
non-linear.
Although Ks could also be constrained, the formulation of G was not consistent either: where Ks is the
conductance, the force that drives the flux ((SM /Smax )β )
is not the same as the defined driving gradient (∇G =
ρg/η max (0, SM − Smax FC )). Power is thus not described as
a conductance times a gradient squared.
The fluxes leaving the fast runoff reservoir were described
in a consistent manner, where the gradient is only scaled by
ρg/η to get the correct units for power. However, the formulation of the flux and gradient is a description of a conceptual
linear reservoir. The real world gradient is different as well as
the depletion of the gradient: the runoff from the fast runoff
reservoir can be interpreted as overland flow or rapid subsurface flow. For these flows, the real-world driving gradient
Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

is thus the slope of the surface or of the subsurface lateral
flow network (influenced by e.g. bedrock topography). The
depletion of this real-world gradient is thus not so much the
depletion of the water level (as in the linear reservoir), but
mainly the depletion of the slope by erosion. This is a much
slower process and can often be considered constant over the
timescale of the modelling period. The optimum parameters
for our linear reservoir model will thus be totally different
than the real-world resistances. We may thus conclude that
the maximum power principle (or MEP) cannot be applied to
conceptual models, due to their lack of realism.
Taking a better look at the study of Porada et al. (2011),
we learned that although they calculate entropy production
of surface runoff and river discharge, they did not optimize
these fluxes. The fluxes they did optimize were rootwater uptake and baseflow which was actually the partitioning of soil
water into transpiration and runoff, while they did not partition total runoff into different runoff components (probably
because of the above mentioned reason that depletion of the
driving gradient is a too slow process).
Another flux that we aimed to parameterize with the maximum power principle is evaporation Ea . However, to do this
properly, this flux should also be described as a gradient divided by a resistance, which was not the case in our model
set-up. The main parameter that influenced evaporation was
the albedo, which only influences the potential evaporation.
As shown in Figs. 2e and 3e this parameter could not be constrained and potential evaporation should thus be treated as a
boundary condition.
6.2.2

System boundaries and feedbacks

Since we cannot model all processes and feedbacks at all
scales, the boundaries of the model are important. Boundary
conditions should be chosen carefully as well as the feedbacks in the model. Both depend on the spatial and temporal
scale of the model and on the notion that the system should
be at (or at least close to) steady state. The maximum time
span of the model is influenced by the process described by
the optimized parameter. This is because the optimized parameter should be constant for the whole modelling period.
In this study we took the average yearly water balance as
timescale. We thus implicitly assumed that the soil structure
and vegetation pattern is constant over the 11 yr of simulation
and that it has enough memory not to be significantly influenced during rain storms or dry spells. Unless information
is available about periodicity of certain parameters, this is
the best one can do and we believe that the yearly timescale
is defensible as appropriate timescale for this study. However, other systems require other timescales; for example,
for arable land that is ploughed seasonally, a better timescale
may be a single rainstorm (e.g. Zehe et al., 2010) and to estimate long-term erosion rates much longer timescales are
needed (e.g. Kleidon et al., 2013).

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 15

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
Besides the appropriate timescale, also the spatial extent
of the model is important. The choice of where to define the
boundaries of a system directly influences the feedbacks that
can be implemented and thus the parameters that can be constrained. A good discussion on this topic can also be found
in Kleidon and Schymanski (2008). However, they stated that
“MEP may still be applicable to systems where parts of the
boundary conditions are fixed [such as] the Bernard convection”. But this may only be true when the boundary conditions are truly not influenced by the system. Fluxes that depend directly on the boundary conditions are likely not to be
optimized correctly.
If we consider for example evaporation, the chemical potential (or energy level) of the atmospheric water demand,
as defined by both Kleidon and Schymanski (2008) and Porada et al. (2011), is highly sensitive for relative humidity: it
uses the normal logarithm of relative humidity. It is now enticing to use observed relative humidity for this, since this is
widely measured in the field. However, doing this, degrades
the atmospheric water demand to a boundary condition that
is not influenced by the evaporative flux and, more important,
standard observed relative humidity is measured at a certain
height (usually one to a few metres) above ground surface. At
this height above ground surface, relative humidity can easily be around 50% making the chemical potential extremely
negative. But in the very thin boundary layer above the leaf
or water surface the air is much closer to saturation. Due to
the high sensitivity to relative humidity this leads to large errors in the gradient that drives evaporation. Thus one should
find a way to properly simulate the relative humidity of this
thin boundary layer, where the boundary condition (with observed relative humidity) is far enough from this boundary
layer.
An example of a feedback that may not be presented correctly can be found in Zehe et al. (2010). They showed that
the density of worm burrows that create macropores (enhancing infiltration) should, in a thermodynamic sense, be higher
at the foot of the hillslope than at the top, which is in accordance with observations. However, what they do not discuss
in detail is that a higher density of worm burrows results in a
higher production of entropy during rainfall events. The optimum is thus an infinite number of worm burrows, which is
of course not possible. The reason for this model behaviour
is that no negative feedback on the persistence of the worm
burrows or on the total worm population was implemented.
This example shows that only processes that have the correct
feedbacks can be optimized and we recognize that this may
be extremely difficult for ecological processes such as in this
example.

7

3155

Conclusions

Several authors already showed the potential of maximum
entropy production (MEP) – and closely related to that the
principle of maximum power (as is used in this study) – to
constrain parameters of hydrological models. Although success is reported, little guidance was given on how to apply the
principle. This lack of guidance makes it more likely that the
principle will be applied in an incorrect manner: in fact, we
did that in this study in which we aimed to constrain a conceptual bucket model using the maximum power principle.
Although we were able to find optimum parameter values
that coincided with a closed water balance, a closer analysis
made us conclude that we could not constrain our model parameters in a meaningful manner. Thus either the MEP principle does not hold, or our model concept is not suitable, and
we believe that the latter is the case. Nevertheless, this study
may be useful since we believe that learning from mistakes
and failures is an effective way to learn and it may prevent
others from making similar mistakes (see also Andréassian
et al., 2010).
Due to the fact that our model had three reservoirs which
all functioned in a different way, this study sheds more light
on how the principle works; maybe not always in connection to the real world, but definitely in a mathematical sense.
We found that, besides the fact that resistances could be
optimized, also parameters that are only linear in the logtransformed space may potentially be optimized. This finding is interesting since it may offer possibilities to constrain
parameters describing the soil moisture retention curve.
We made a clear distinction between mathematical optima
and the optimum real world catchment structure, and discussed that only when the model reflects the catchment in
enough detail the two may be the same (if the MEP hypothesis indeed holds). We therefore believe that a model should
be physically based (where “enough detail” may differ from
case to case) to be constrained with this principle. This means
that
1. fluxes should be defined as a gradient divided by a resistance and this gradient should be a real world gradient
(as opposed to that of a simple linear reservoir).
2. the optimized flux should have a feedback on the gradient; i.e. the influence of boundary conditions on gradients should be minimal.
3. the temporal scale of the model should be chosen in
such a way that the parameter that is constrained is constant over the modelling period.
4. only when the correct feedbacks are implemented the
fluxes can be optimized; this may be difficult and may
require knowledge from other disciplines such as ecology or biology.

www.hydrol-earth-syst-sci.net/17/3141/2013/

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

## PDF page 16

3156

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models

5. there should be a trade-off between two or more fluxes.
This follows directly from the fact that the principle
only holds for systems in steady state, meaning that incoming fluxes equal outgoing fluxes.
Furthermore, we would like to stress that with this study
we do not claim that the MEP principle does not work, but we
showed that applying the principle is not as straightforward
as it may seem. Only if it is applied it in a correct way, while
having the correct physics, one will be able to test the MEP
principle. If that point is reached, and if the MEP principle
still holds, it would mean a big step forward in the hydrological science.

Acknowledgements. We would like to thank the editor as well as
Bettina Schaefli and two anonymous reviewers for their useful
comments which improved the manuscript significantly. Data sets
were provided by the HJ Andrews Experimental Forest research
program, funded by the National Science Foundation’s Long-Term
Ecological Research Program (DEB 08-23380), US Forest Service
Pacific Northwest Research Station, and Oregon State University.
The service charges for this open access publication
have been covered by a Research Centre of the
Helmholtz Association.
Edited by: M. Sivapalan

References
Andréassian, V., Perrin, C., Parent, E., and Bárdossy, A.: The
Court of Miracles of Hydrology: can failure stories contribute to hydrological science?, Hydrolog. Sci. J., 55, 849–856,
doi:10.1080/02626667.2010.506050, 2010.
Brolsma, R. J. and Bierkens, M. F. P.: Groundwater-soil
water-vegetation dynamics in a temperate forest ecosystem along a slope, Water Resour. Res., 43, W01414,
doi:10.1029/2005WR004696, 2007.
Caylor, K. K., Scanlon, T. M., and Rodriguez-Iturbe, I.: Ecohydrological optimization of pattern and processes in water-limited
ecosystems: a trade-off-based hypothesis, Water Resour. Res.,
45, W08407, doi:10.1029/2008WR007230, 2009.
Clark, M. P., Kavetski, D., and Fenicia, F.: Pursuing the method of
multiple working hypotheses for hydrological modeling, Water
Resour. Res., 47, W09301, doi:10.1029/2010WR009827, 2011.
Daly, C. and McKee, W.: Meteorological data from benchmark stations at the Andrews Experimental Forest, Long-Term Ecological
Research, Forest Science Data Bank, Corvallis, OR, [Database],
available at: http://andrewsforest.oregonstate.edu/data/abstract.
cfm?dbcode=MS001, last access: 22 November 2011.
Dewar, R. C.: Maximum entropy production as an inference algorithm that translates physical assumptions into macroscopic
predictions: don’t shoot the messenger, Entropy, 11, 931–944,
doi:10.3390/e11040931, 2009.
Dewar, R. C.: Maximum entropy production and plant optimization theories, Philos. T. Roy. Soc. B, 365, 1429–1435,
doi:10.1098/rstb.2009.0293, 2010.

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013

Fenicia, F., Kavetski, D., and Savenije, H. H. G.: Elements of a
flexible approach for conceptual hydrological modeling: 1. Motivation and theoretical development, Water Resour. Res., 47,
W11510, doi:10.1029/2010WR010174, 2011.
Johnson, S. and Rothacher, J.: Stream discharge in gaged watersheds at the Andrews Experimental Forest. Long-Term
Ecological Research, Forest Science Data Bank, Corvallis,
OR [Database], available at: http://andrewsforest.oregonstate.
edu/data/abstract.cfm?dbcode=HF004 (last access: 22 November 2011), 2009.
Klausmeier, C. A.: Regular and irregular patterns
in semiarid vegetation, Science, 284, 1826–1828,
doi:10.1126/science.284.5421.1826, 1999.
Kleidon, A.: Nonequilibrium thermodynamics and maximum entropy production in the Earth system, Naturwissenschaften, 96,
653–677, doi:10.1007/s00114-009-0509-x, 2009.
Kleidon, A.: A basic introduction to the thermodynamics of
the Earth system far from equilibrium and maximum entropy production, Philos. T. Roy. Soc. B, 365, 1303–1315,
doi:10.1098/rstb.2009.0310, 2010a.
Kleidon, A.: Life, hierarchy, and the thermodynamic machinery of planet Earth, Phys. Life Rev., 7, 424–460,
doi:10.1016/j.plrev.2010.10.002, 2010b.
Kleidon, A. and Schymanski, S.: Thermodynamics and optimality
of the water budget on land: a review, Geophys. Res. Lett., 35,
L20404, doi:10.1029/2008GL035393, 2008.
Kleidon, A., Zehe, E., Ehret, U., and Scherer, U.: Thermodynamics, maximum power, and the dynamics of preferential river flow
structures at the continental scale, Hydrol. Earth Syst. Sci., 17,
225–251, doi:10.5194/hess-17-225-2013, 2013.
Kondepudi, D.: Introduction to modern thermodynamics, Wiley,
2008.
Lindström, G., Johansson, B., Persson, M., Gardelin, M., and
Bergström, S.: Development and test of the distributed
HBV-96 hydrological model, J. Hydrol., 201, 272–288,
doi:10.1016/S0022-1694(97)00041-3, 1997.
Lorenz, R. D., Lunine, J. I., Withers, P. G., and McKay, C. P.: Titan,
Mars and Earth: entropy production by latitudinal heat transport,
Geophys. Res. Lett., 28, 415–418, doi:10.1029/2000gl012336,
2001.
McDonnell, J., Sivapalan, M., Vaché, K., Dunn, S., Grant, G.,
Haggerty, R., Hinz, C., Hooper, R., Kirchner, J., Roderick, M.,
Selker, J., and Weiler, M.: Moving beyond heterogeneity and process complexity: a new vision for watershed hydrology, Water
Resour. Res., 43, W07301, doi:10.1029/2006WR005467, 2007.
Monteith, J. L.: Evaporation and surface temperature, Q. J. Roy.
Meteorol. Soc., 107, 1–27, doi:10.1002/qj.49710745102, 1981.
Moore, R. J.: The probability-distributed principle and runoff production at point and basin scales, Hydrolog. Sci. J., 30, 273–297,
doi:10.1080/02626668509490989, 1985.
Paik, K. and Kumar, P.: Optimality approaches to describe characteristic fluvial patterns on landscapes, Philos. T. Roy. Soc. B, 365,
1387–1395, doi:10.1098/rstb.2009.0303, 2010.
Paltridge, G. W.: Climate and thermodynamic systems of maximum
dissipation, Nature, 279, 630–631, doi:10.1038/279630a0, 1979.
Perrin, C., Michel, C., and Andréassian, V.: Improvement of a parsimonious model for streamflow simulation, J. Hydrol., 279, 275–
289, doi:10.1016/S0022-1694(03)00225-7, 2003.

www.hydrol-earth-syst-sci.net/17/3141/2013/

## PDF page 17

M. C. Westhoff and E. Zehe: MEP to constrain conceptual models
Porada, P., Kleidon, A., and Schymanski, S. J.: Entropy production
of soil hydrological processes and its maximisation, Earth Syst.
Dynam., 2, 179–190, doi:10.5194/esd-2-179-2011, 2011.
Porporato, A., Laio, F., Ridolfi, L., and Rodriguez-Iturbe, I.:
Plants in water-controlled ecosystems: active role in hydrologic
processes and response to water stress: III. Vegetation water
stress, Adv. Water Resour., 24, 725–744, doi:10.1016/S03091708(01)00006-9, 2001.
Prigogine, I.: What is entropy?, Naturwissenschaften, 76, 1–8,
doi:10.1007/BF00368303, 1989.
Rodriguez-Iturbe, I., D’Odorico, P., Porporato, A., and Ridolfi, L.:
On the spatial and temporal links between vegetation, climate, and soil moisture, Water Resour. Res., 35, 3709–3722,
doi:10.1029/1999WR900255, 1999.
Rothacher, J.: Streamflow from small watersheds on the western
slope of the Cascade Range of Oregon, Water Resour. Res., 1,
125–134, doi:10.1029/WR001i001p00125, 1965.
Rothacher, J., Dyrness, C. T., and Fredriksen, R. L.: Hydrologic and
related characteristics of three small watersheds in the Oregon
Cascades, US Department of Agriculture, US Forest Service, Pacific Northwest Research Station, Portland, Oregon, USA, 1967.
Schaefli, B., Harman, C. J., Sivapalan, M., and Schymanski, S. J.:
HESS Opinions: Hydrologic predictions in a changing environment: behavioral modeling, Hydrol. Earth Syst. Sci., 15, 635–
646, doi:10.5194/hess-15-635-2011, 2011.
Schymanski, S. J., Kleidon, A., and Roderick, M. L.: Ecohydrological optimality, in: Encyclopedia of Hydrological Sciences,
edited by: Anderson, M. G., vol. 1, John Wiley & Sons Ltd.,
doi:10.1002/0470848944.hsa319, 2009a.

www.hydrol-earth-syst-sci.net/17/3141/2013/

3157

Schymanski, S. J., Sivapalan, M., Roderick, M. L., Hutley, L. B.,
and Beringer, J.: An optimality-based model of the dynamic
feedbacks between natural vegetation and the water balance,
Water Resour. Res., 45, W01412, doi:10.1029/2008WR006841,
2009b.
Schymanski, S. J., Kleidon, A., Stieglitz, M., and Narula, J.: Maximum entropy production allows a simple representation of heterogeneity in semiarid ecosystems, Philos. T. Roy. Soc. B, 365,
1449–1455, doi:10.1098/rstb.2009.0309, 2010.
Tague, C. L. and Band, L. E.: Evaluating explicit and implicit routing for watershed hydro-ecological models of forest hydrology
at the small catchment scale, Hydrol. Process., 15, 1415–1439,
doi:10.1002/hyp.171, 2001.
Thompson, S., Harman, C., Troch, P., Brooks, P., and Sivapalan, M.: Spatial scale dependence of ecohydrologically mediated water balance partitioning: a synthesis framework for
catchment ecohydrology, Water Resour. Res., 47, W00J03,
doi:10.1029/2010WR009998, 2011.
Zehe, E. and Sivapalan, M.: Threshold behaviour in hydrological systems as (human) geo-ecosystems: manifestations, controls, implications, Hydrol. Earth Syst. Sci., 13, 1273–1297,
doi:10.5194/hess-13-1273-2009, 2009.
Zehe, E., Lee, H., and Sivapalan, M.: Dynamical process upscaling
for deriving catchment scale state variables and constitutive relations for meso-scale process models, Hydrol. Earth Syst. Sci.,
10, 981–996, doi:10.5194/hess-10-981-2006, 2006.
Zehe, E., Blume, T., and Blöschl, G.: The principle of maximum
energy dissipation: a novel thermodynamic perspective on rapid
water flow in connected soil structures, Philos. T. Roy. Soc. B,
365, 1377–1386, doi:10.1098/rstb.2009.0308, 2010.

Hydrol. Earth Syst. Sci., 17, 3141–3157, 2013
