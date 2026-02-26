# Nitrous oxide and methane fluxes from different understory treatments in Oil Palm plantations in Riau, Indonesia 2018-2019

## Overview
- Study quantifies greenhouse gas emissions (N2O, CH4, CO2) under three understory vegetation management treatments in mature oil palm plantations in Riau, Indonesia.
- Part of the BEFTA programme, aiming to inform management practices and policy (e.g., RSPO) to reduce environmental impact.
- Data disponibilized under Open Government Licence with accompanying metadata and citations.

## Experimental design
- Location: mature oil palm plantations in Ujung Tanjung Estate and Kandista, Sumatra.
- Plots: 18 plots (2.25 ha each) across two estates; arranged in six replicate blocks, with three understory treatments per block.
- Treatments:
  - Normal complexity: standard herbicide use on understory vegetation.
  - Reduced complexity: highly destructive, herbicide spraying of all understory vegetation.
  - Enhanced complexity: conservation treatment; no understory herbicide spraying and limited understory cutting.
- Replication: six blocks per plantation, nine plots per understory treatment across both estates.
- Measurements: 54 static chambers (six per plot) used to monitor CH4, N2O, and CO2; sampling Oct 2018–Sep 2019, typically over a two-day window each month.

## Field collection methods
- Chamber setup: 40 cm diameter collars inserted to ~7 cm depth; lids sealed to create airtight sampling.
- Sampling: 0, 15, 30, 45 minutes inside incubation; 100 mL gas samples drawn and stored for analysis.
- Auxiliary data: soil moisture measured around each chamber (via Theta probe at 7 cm depth).
- Permits: data collection covered by Indonesian research permits (RISTEK numbers provided).

## Laboratory analysis and calibration
- Instrumentation: Agilent 7890B GC with μECD for N2O and FID for CH4/CO2.
- Calibration: four-point mixed-gas standards analyzed after ~every 20 samples.
- Flux estimation: RCFlux R package applied to compute fluxes using six regression models; the best-fit model selected for each gas and chamber.
- Units and reporting: fluxes reported as micromoles per square meter per second (μmol m−2 s−1) with 95% confidence intervals.

## Data outputs and structure
- BEFTA_GHG_RCflux.csv
  - Per-chamber flux estimates for each sampling event (monthly Oct 2018–Sep 2019) across CH4, N2O, CO2.
  - Columns include: gasName, flux estimates from six methods, best-fit flux, 95% CI bounds, model fit statistics (adjR2), year, month, day, chamber, treatment, block_number, location details, soil_moisture, chamber dimensions, area, volume, coordinates, and elevation.
- BEFTA_chambers.csv
  - Details for all 54 chambers: BEFTA_code, treatment, block_number, year_planted, chamber ID, in/out circle status, location details, latitude, longitude, elevation.
- Data quality: QC includes visual checks of regression fits; unreliable samples flagged; most flux estimates use the best-fit linear or nonlinear model.

## Usage and implications
- Enables analysis of how understory management influences soil greenhouse gas fluxes in oil palm systems.
- Provides a standardized data platform (with metadata) to support cross-site comparisons, environmental assessments, and policy guidance for sustainable palm oil cultivation.
- Facilitates reproducibility and future modelling of GHG dynamics under different understory and management scenarios.

## Access and citation
- Data accessible under Open Government Licence at the provided DOI.
- Citation required: Drewer, J.; White, S.; Sionita, R.; Pujianto, P. (2020). Nitrous oxide and methane fluxes from different understory treatments in oil palm plantations in Riau, Indonesia 2018-2019. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/378f028d-ab04-4fa5-a5ca-61f78ea0adb0