# Stem respiration in human-modified forests of Eastern Amazonia

## Overview
- A dataset named StemRespirationData.csv containing stem respiration measurements from trees in 20 Amazonian forest plots (each 250 x 10 m).
- Plots span a disturbance gradient prior to El Niño, categorized as undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
- Disturbance classifications based on canopy disturbance analysis (1988–2010) and field assessments of fire scars, charcoal, and logging debris.
- Data collected from June 2015 to July 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Data collection design and methods
- At least 13 trees per plot equipped with stem collars installed 20 cm above dendrometers.
- Trees stratified into five DBH classes: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, and ≥50 cm.
- PVC collars (~5 cm tall, 10 cm diameter) connected to an infrared gas analyser (EGM5) to measure stem CO2 efflux (stem respiration).
- Measurements taken every 3 months; if a tree died, its collar was removed and a new collar installed in the same size class at another suitable tree.
- Missing data are indicated as N/A with reasons documented in the notes column.

## Spatial and geographic data
- Plot coordinates are provided for plot identifiers (e.g., 112_12, 112_8, 129_10, etc.) with corresponding latitude and longitude values.
- The study area is located in Eastern Amazonia, within a microcatchment framework (~5,000 ha per catchment).
- Data structure includes fields to support geospatial mapping and integration with other spatial datasets.

## Data structure and fields
- CSV columns include:
  - Date: Date of data collection
  - Catchment: Microcatchment area (~5,000 ha) for each plot
  - Transect: Plot number within each catchment
  - Plot code: Unique code combining catchment and transect
  - Forest: Forest disturbance class before the 2015–16 El Niño
  - Fire: Whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire)
  - Tree TAG: Identifier for the individual with the collar
  - Time: Exact sampling time
  - Collar height: Height of the collar at the time of measurement
  - CO2 initial: CO2 concentration at the start of the measurement
  - CO2 final: CO2 concentration at the end of the measurement
  - Flux: Measured stem respiration flux
  - Field notes: Field processing notes for the sample

## Temporal coverage
- Time span: June 2015 to July 2018
- Sampling cadence: approximately quarterly (every 3 months)

## Disturbance and fire context
- Forest disturbance classes reflect pre-El Niño conditions (2015–16) and include primary undisturbed, logged primary, logged-and-burned primary, and secondary forests.
- Fire status per plot captured as a binary indicator for the El Niño event.

## Data quality and notes
- N/A entries indicate missing measurements; reasons are recorded in the field notes.
- If a tree died during the study, the collar was removed and re-deployed in the same size class on another suitable tree to maintain sample size.

## GIS and analysis considerations
- Enables spatial visualization of stem respiration across disturbance classes and fire history.
- Can be linked with canopy disturbance layers, fire history, and other environmental covariates for map-based analyses.
- Useful for time-series mapping of stem CO2 efflux at plot and tree levels, with attention to missing data and replacement sampling.