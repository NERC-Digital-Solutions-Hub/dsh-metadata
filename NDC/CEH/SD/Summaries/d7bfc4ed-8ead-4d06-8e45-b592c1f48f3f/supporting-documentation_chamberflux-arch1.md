# Carbon dioxide and methane flux response and recovery from drought in a hemiboreal ombrotrophic fen

## Overview of the dataset
- Measures net ecosystem exchange (NEE) of CO2 and fluxes of CH4 at a hemi-boreal ombrotrophic fen in southern Sweden.
- Data collected from August 2017 to September 2019 using SkyLine2D automated chamber system.
- Four ecotypes identified to assess drought response: sphagnum, eriophorum, heather, and open water.
- 2018 drought year enables comparison of fluxes between drought and non-drought years (May–September) and recovery in 2019.

## Site description
- Location: Mycklemossen, ombrotrophic fen about 100 km north of Gothenburg (58.3673 N, 12.1686 E), ~75 m above sea level.
- Part of Skogaryd research catchment; monitored since 2013.
- Vegetation: predominantly heather (Calluna vulgaris), sphagnum moss (Sphagnum spp.), sedges (Eriophorum vaginatum); high water table with open water areas year-round.
- 2018 drought: less rainfall, higher temperatures, more solar radiation than 2019.

## Experimental design
- January 2017: transect selected to include all vegetation types.
- Spatial blocks along transect; within each block, 24 random replicate points (n = 6 per ecotype: eriophorum, heather, sphagnum, open water).
- At each point: a PVC collar (inner diameter 20 cm, height 10 cm) inserted ~2 cm below soil surface or into sediment at water positions.

## Greenhouse gas flux measurements
- Instrument: SkyLine2D automated chamber system (Perspex chamber, 20 cm inner diameter, 40 cm height) on a motorised trolley.
- Operation: system visits pre-selected positions along transect; chamber lowered onto a collar for 4 minutes per measurement; cycle ~2.5 hours allowing ~10 measurements per day per chamber.
- Gas analysis: CO2 via LICOR LI-8100 IRGA; CH4 via cavity ringdown laser (CRD) system; data logged with Campbell Scientific data logger.
- Flux calculation: linear regression of gas concentration change; deadband ≥ 20 s for mixing; 90 s window for CO2 and 240 s for CH4; fluxes adjusted for area, air temperature, gas volume; daylight-hour CO2 adjustments using light response curve to account for chamber attenuation.

## Data processing and quality control
- Software: SAS 9.4 for data manipulation and analyses.
- CO2 QA: CO2 fluxes with R^2 < 0.9 discarded.
- CH4 QA: flux regressions with P < 0.05 accepted; otherwise treated as zero flux.
- Outliers: excluded if outside ±1.96 standard errors of the mean flux per collar.
- Night-time/atmospheric still conditions: filtered to avoid flux overestimation (based on established methods).
- Additional exclusion: fluxes where mean CO2 concentration before/after chamber closure dropped by >25 ppm within 20 s window (per Jarveoja et al. 2020); 329 fluxes excluded.

## Nature of recorded values and data structure
- Dataset comprises a single table with eight columns:
  - DATETIME: date-time of flux measurement (dd:mmm:yyyy:hh:mm:ss)
  - DATE: date of measurement (dd/mm/yyyy)
  - TIME: time of measurement (hh:mm:ss)
  - PLOT: experimental plot number
  - ECOTYPE: dominant vegetation type (sphagnum, heather, eriophorum, water)
  - BLOCK: block number
  - CH4_flux: methane flux (nmol m⁻² s⁻¹)
  - CO2_flux: net ecosystem exchange of CO2 (µmol m⁻² s⁻¹)

## References and methodology context
- Heinemeyer et al. (2013): evaluation of automatic ground-level flux chamber systems.
- Jarveoja et al. (2020): diel patterns in peatland respiration and temperature response.
- Keane et al. (2018): diurnal variation and light influence on gas flux measurements.
- Keane et al. (2021): carbon dioxide and methane flux response and drought recovery in the fen.
- Koskinen et al. (2014); Lai et al. (2012); Mosier (1989): related methodological considerations for chamber flux measurements and data handling.