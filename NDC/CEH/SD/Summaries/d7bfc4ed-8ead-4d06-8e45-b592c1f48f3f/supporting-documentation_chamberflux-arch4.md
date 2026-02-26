# Overview of the dataset

- The dataset documents net ecosystem exchange (NEE) of CO2 and methane (CH4) fluxes measured at Mycklemossen, a hemi-boreal ombrotrophic fen in Southern Sweden, from August 2017 to September 2019, using an automated chamber system (SkyLine2D).
- Four ecotypes were studied: sphagnum moss (Sphagnum spp.), eriophorum, heather (Calluna vulgaris), and open water (water). A 2018 drought period is contrasted with 2019 (recovery observed in 2019).
- Primary purpose is to assess how different vegetation types respond to drought and recover, contributing to understanding of carbon and methane dynamics in peatland ecosystems.

## Site description

- Location: Mycklemossen fen, ~100 km north of Gothenburg, Sweden (approx. 58.3673 N, 12.1686 E, ~75 m a.s.l.).
- Part of the Skogaryd research catchment, monitored since 2013.
- Vegetation: dominated by heather, sphagnum moss, and Eriophorum vaginatum; high water table with persistent open water areas.
- 2018 experienced drought (lower rainfall, higher temperature and solar radiation) versus 2019 conditions.

## Experimental design

- In January 2017, a transect across all vegetation types was established; 24 measurement points (blocks) defined as 6 replicates per ecotype: eriophorum, heather, sphagnum, and water.
- Each point fitted with a PVC collar (20 cm inner diameter) inserted ~2 cm into soil/sediment.

## Greenhouse gas flux measurements

- Instrumentation: SkyLine2D automated chamber system (University of York) with a single clear chamber (20 cm diameter, 40 cm height) mounted on a motorised trolley.
- Procedure: Chamber lowers onto collar at each point to measure flux over four minutes; cycle repeats across points, cycling takes ~2.5 hours, yielding about 10 measurements per day per point.
- Gas analysis: CO2 measured with LICOR LI-8100 IRGA; CH4 measured with a cavity ring-down laser (CRD, LGR UGGA-91).
- No chamber fan; flow through analysers deemed sufficient for complete mixing.
- Data logging: Fluxes adjusted for area, air temperature, and gas volume; daylight adjustments applied to CO2 flux during daylight using a light response curve to account for chamber attenuation.

## Data processing and quality control

- Software: SAS 9.4 for data manipulation; R 2 threshold of CO2 flux used for initial QC (R2 < 0.9 discarded).
- CH4 flux: regressions with P < 0.05 accepted; otherwise treated as zero flux.
- Outliers: excluded if ±1.96 standard errors from mean flux per collar.
- Night-time/atmospheric conditions: data filtered to avoid overestimation during still air; fluxes discarded if the mean CO2 concentration before and after closure dropped by more than 25 ppm within 20 seconds.
- Result: 329 flux measurements excluded after QA.

## Nature and units of recorded values; data structure

- Dataset comprises a single table with eight columns:
  - DATETIME: date-time of flux measurement (dd:mmm:yyyy:hh:mm:ss)
  - DATE: date of measurement (dd/mm/yyyy)
  - TIME: time of measurement (hh:mm:ss)
  - PLOT: experimental plot number
  - ECOTYPE: dominant vegetation type at the plot (sphagnum, heather, eriophorum, water)
  - BLOCK: block number in the experimental design
  - CH4_flux: methane flux (nmol m^-2 s^-1)
  - CO2_flux: net ecosystem exchange of CO2 (µmol m^-2 s^-1)

## References and provenance

- Keane et al. (2018) methodological background for SkyLine2D system and chamber approach.
- Koskinen et al. (2014); Lai et al. (2012); Mosier (1989); Heinemeyer et al. (2013); Jarveoja et al. (2020); Keane et al. (2021) provide related calibration, validation, and interpretation context.
- Key data provenance: data collection and interpretation led by Ben Keane, Sylvia Toet, Phil Ineson, Per Weslien, James Stockdale, and Leif Klemedtsson; contact Sylvia Toet for data access.

## Data management considerations for Data Leaders

- Comprehensive metadata: clear variable definitions, units, ecotype labeling, and measurement protocols support discoverability and reuse.
- Data quality governance: explicit QA/QC criteria (R2 thresholds, P-values, outlier treatment) support reproducibility and auditability.
- Transparency on processing steps: detailed description of corrections (daylight adjustment, night-time adjustments, and flux filtering) aids validation and cross-study comparability.
- Limited data gaps and documentation of exclusions (329 fluxes) to understand dataset completeness.
- Potential for cross-site comparisons and integration with broader peatland datasets, given standardized structure and explicit methodology.
- Contacts and data stewardship: explicit individuals and institutions for data access facilitate collaboration and data sharing within networks.