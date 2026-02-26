# Experimental Design and Laboratory Incubation Method

## Overview
- Sediment from two river types (Chalk Lambourn; Sandstone Tern) collected in September 2015.
- Objective: quantify microbial metabolic activity using a resazurin-resorufin tracer and linked gas measurements (CO2, CH4) plus dissolved oxygen.
- Data collected across multiple substrate types, temperatures, and replicates to enable self-contained data analysis.

## Experimental design and treatments
- Substrates: six substrate types plus controls
  - Chalk fine, Chalk medium, Chalk coarse
  - Sandstone fine, Sandstone medium, Sandstone coarse
  - Plus control (no substrate)
- Samples: three samples from each river (total six initial samples)
- Replicates: each substrate type incubated in triplicate
- Temperature treatments: 5, 9, 15, 21, 26°C
- Experimental units: 7 substrate treatments × 3 samples × 5 temperatures × triplicates → 105 observations
- Jars: 1 L amber jars with 300 ml sediment and 500 ml ultrapure water (controls with 500 ml water only)
- Incubation duration per run: samples taken at 0 hours and after 5 hours

## Sample collection and preparation
- Sediment collection: upper 10 cm of streambeds from two rivers
- Initial processing: homogenised, sieved (0.8 cm for fine; 1.6 cm for medium and coarse)
- Storage: airtight, cold, dark until incubation

## Measurements and instrumentation
- Microbial activity tracer: resazurin-resorufin system
  - Addition: 5 ml of ~14.5–15.4 ppb resazurin added to water column at zero hours
  - Analysis: resorufin concentration as proxy for microbial activity
  - Fluorometer: GGUN-FL30 (customised for resorufin and resazurin; measurement every 10 seconds; final values averaged)
- Gas measurements
  - CO2 and CH4 concentrations: Agilent 7890A GC with flame ionisation detector
  - Methane-specific detection via methanisation of CO2 prior to GC
- Dissolved oxygen: Pyro-science Firesting fixed needle-type sensor
- Organic matter content: Loss on ignition (LOI) at 550°C after drying a sediment sub-sample
- Time points: 0 hours (baseline) and 5 hours (post-incubation)

## Calibration and quality control
- Gas chromatograph calibration: daily four-point calibration for CO2 and CH4 (zero, 1051, 525.5, 262.8 ppm); drift checks with external standard solution
  - Reported accuracy, precision, and detection limits
- Fluorometer calibration: weekly three-point calibration (zero, 100 ppb resorufin, resorufin/resazurin mix); additional standard ~93.1 ppb
  - Reported accuracy and limit of detection
- Oxygen sensor calibration: daily one-point calibration at 100% air saturation
- Documentation of references for LOI and online fluorometry methods

## Data structure and variables
- Dataset file: IncubationCO2_CH4_Resorufin_DO
- Columns (nine):
  - Temperature: incubation temperature, °C
  - Jar: jar identifier (1–21 mapping to substrate_type)
  - Substrate_Type: Chalk or Sandstone; fine, medium, coarse
  - Geology: river origin geology (Chalk or Sandstone); NA for controls
  - Organic_Matter: sediment organic matter content, percent
  - CO2: carbon dioxide production rate, mg C m^-2 h^-1
  - CH4: methane production rate, mg C m^-2 h^-1
  - Resorufin: resorufin production rate, ng resorufin per µg resazurin per hour
  - Dissolved_Oxygen: water column DO, mg L^-1
- Substrate labeling: jars 1–3 Chalk fine, 4–6 Chalk medium, 7–9 Chalk coarse, 10–12 Sandstone fine, 13–15 Sandstone medium, 16–18 Sandstone coarse, 19–21 controls
- Geology NA indicates control experiments without substrate

## Timeline and provenance
- Field sampling: September 2015 (River Lambourn and River Tern)
- Incubation experiments: 19 October 2015 – 3 December 2015
- Data capture and processing documented with calibration and methodological details

## Data interpretation and potential uses
- Compare metabolic activity across substrate types, lithology, and temperature
- Assess how organic matter content influences CO2/CH4 production and resorufin signaling
- Enable data-driven dashboards or reports for researchers and managers monitoring sediment biogeochemistry
- Facilitate reproducibility by providing explicit calibration, measurement, and processing steps

## Notes and references
- LOI methodology reference for organic matter determination
- Online fluorometry methods reference for resorufin/resazurin measurements