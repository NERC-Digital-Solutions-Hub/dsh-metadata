# Overview of the dataset

- Net ecosystem exchange (NEE) and methane (CH4) fluxes were measured at Mycklemossen, a hemi-boreal ombrotrophic fen in Southern Sweden, from August 2017 to September 2019.
- Measurements were taken with SkyLine2D, an automated chamber system, near-continuously; 24 measurement points across four ecotypes: sphagnum, eriophorum, heather, and open water.
- The 2018 drought year enabled comparison of fluxes between drought and nondrought years (May–September) and assessment of recovery in 2019.
- Primary data collectors and interpreters: Ben Keane, Sylvia Toet, Phil Ineson, Per Weslien, James Stockdale, and Leif Klemedtsson; contact Sylvia Toet first for inquiries.

## Site description

- Location: Mycklemossen ombrotrophic fen, approximately 100 km north of Gothenburg, Sweden (58.3673 N, 12.1686 E; ~75 m above sea level).
- Part of the Skogaryd research catchment (monitored since 2013).
- Vegetation: heather (Calluna vulgaris), sphagnum mosses (Sphagnum spp.), and sedges (Eriophorum vaginatum); water table typically maintains open water areas within the mire year-round.
- 2018 drought featured reduced rainfall, higher temperatures, and more solar radiation than 2019.

## Experimental design

- In January 2017, a transect across the mire including all vegetation types was established.
- Spatial blocks defined along the transect; within each block, 24 replicate points (6 per ecotype: sedge, heather, sphagnum, open water) were selected randomly.
- At each of 24 points, a PVC collar (inner diameter 20 cm, height 10 cm) was inserted ~2 cm below the soil surface or into the sediment at water positions.

## Greenhouse gas flux measurements

- Instrumentation: SkyLine2D automated chamber system (clear cylindrical chamber, 20 cm inner diameter, 40 cm height) on a motorised trolley; traversed ~2 m above the transect.
- Measurement process: chamber lowered onto collars to measure gas flux over ~4 minutes; full cycle ~2.5 hours with ~10 measurements per day per chamber position.
- Gas analysis: CO2 and CH4 measured using a LI-COR LI-8100 IRGA and a cavity ringdown laser (LGR UGGA-91) respectively; no chamber fan used (previous tests indicated no significant difference with/without mixing).
- Data capture: headspace gas circulated to analysers; fluxes computed by linear regression of concentration change; adjustments for area, air temperature, and gas volume; CO2 flux daylight adjustment based on light response curve to account for light attenuation by chamber material.

## Data processing

- Software: SAS 9.4 used for data manipulation and analysis; R2 check on CO2 flux (>0.9) used for initial quality control; CH4 flux regressions with P < 0.05 accepted; others treated as zero flux.
- Outlier handling: excluded fluxes defined as ±1.96 standard errors of the mean for each collar.
- Night-time overestimation: filtered using procedures from Koskinen et al. (2014) and Lai et al. (2012); fluxes where the mean CO2 concentration in the 20 s before and after chamber closure dropped by more than 25 ppm were discounted (resulting in 329 fluxes excluded).
- Data structure: dataset comprises one table with eight columns.

## Nature and units of recorded values; details of data structure

- Variables in dataset (in order):
  - DATETIME: Date and time of flux measurement; format dd:Mon:yyyy:hh:mm:ss
  - DATE: Date of measurement; format dd/mm/yyyy
  - TIME: Time of measurement; format hh:mm:ss
  - PLOT: Experimental plot number
  - ECOTYPE: Dominant vegetation type per plot (sphagnum, heather, eriophorum, or water)
  - BLOCK: Block number of the experimental design
  - CH4_flux: Methane flux (nmol m^-2 s^-1)
  - CO2_flux: Net ecosystem exchange of CO2 (µmol m^-2 s^-1)

## References and supporting literature

- Keane et al. (2018), Keane et al. (2021), Koskinen et al. (2014), Lai et al. (2012), Mosier (1989), and additional methodological sources for chamber flux calculations and data quality criteria.