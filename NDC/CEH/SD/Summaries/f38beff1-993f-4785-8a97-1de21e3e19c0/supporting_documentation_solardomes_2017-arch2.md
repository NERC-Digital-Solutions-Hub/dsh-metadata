# Summary Description of experiment location

## Overview
- Rural site in North Wales, UK, near the sea; part of Bangor University farm.
- Eight solardomes used in 2017, each exposing plants to ozone with charcoal-filtered air; three domes heated +7°C to mimic tropical/subtropical conditions. Associated plant biomass and physiology data available only for the three heated domes.
- Ozone addition follows a weekly profile and is computer-controlled; ozone is added at night and during the day. Plants watered as needed; ozone exposure ended at different times for different species.

## Experimental Design
- Four replicate pots per species/cultivar exposed to ozone in the solardomes.
- Ozone and meteorological conditions logged continuously on an hourly basis.
- Exposure length varied by species/cultivar due to growing season differences.
- Ad-hoc measurements of stomatal conductance with concurrent soil moisture and chlorophyll content index; yield measured at experiment end.
- Species/treatment scope includes multiple wheat varieties, pearl millet varieties, several bean varieties, cowpea, and finger millet with both heated and unheated, and three ozone levels (low, medium, high).

## Treatments
- Unheated: Low ozone (35 ppb), Medium ozone (80 ppb), High ozone (115 ppb).
- Heated (+7°C): Low ozone (35 ppb), Medium ozone (80 ppb), High ozone (115 ppb).

## Data Collected and Methods
- Ozone and meteorology data logged automatically; quality assured, with gap-filling as needed. Plant physiology data collected ad-hoc with QA checks. Biomass and yield measured at the end with QA checks.
- Experimental facility: Solardomes ozone exposure system controlled by LabView; stomatal conductance via AP4 porometer; soil moisture via Delta-T theta probe; chlorophyll content via CCM-200.

## Calibration and Instrumentation
- AP4 Porometer calibrated daily per manufacturer instructions.
- Ozone analyzers calibrated by external provider.
- CCM-200 autocalibrates on startup.

## Data Resources and Structure
- Three CSV data files:
  - Plant_Physiology_2017.csv: 11 columns, 3112 rows; readings include species, treatment, pot, date/time, leaf side, stomatal conductance, PAR, leaf temperature, soil moisture, Chl Content Index.
  - Ozone_and_meteorology_2017.csv: 11 columns, 18534 rows; includes treatment, day of year, date, hour, ozone ppb, light, temperature, VPD, air pressure, wind speed (dummy), precipitation (dummy).
  - Biomass_and_Yield_2017.csv: 17 columns; yields and biomass metrics by species, treatment, and pot; includes pod/bean metrics and derived statistics.
- Blank cells indicate missing readings; a small number of measurements were missing due to QA issues.
- DO3SE model inputs used for ozone flux calculations require constant air pressure, wind speed, and precipitation values; wind speed and precipitation are generalized within the dataset (dummy values) to support model runs.

## Data Quality Control and Gap Filling
- QA procedures applied to all datasets: range checks, plausibility checks, and outlier handling.
- Gap filling protocol for ozone and canopy data:
  - Ensure 24 hourly rows per day; gaps ≤5 hours filled by averaging adjacent values.
  - Larger gaps investigated with lab notes; where appropriate, values from previous/next day used to fill (e.g., same time across days) and adjusted to preserve data patterns.
  - When no ozone was being added, a dummy value of 5 ppb used.
  - All data changes are tracked by creating a separate amended copy labeled as filled/corrected.
- Data gaps and irregular logging periods clearly documented (e.g., power failures); original data maintained with amendments in separate files.

## Data Presentation and Accessibility
- Outputs designed to be stored and uploaded to appropriate data portals; data presented in clear formats such as CSV files with standardized column headers.
- Website for facility reference: CEH Solardomes and Ozone Field Release System.

## Analytical Status and Use
- Analytical methods: No formal analysis performed on these datasets within the described resource.
- Data suitable for time-series analyses of environmental conditions and plant responses, enabling cross-dataset integration (ozone, meteorology, physiology, biomass, and yields) for monitoring environmental health and policy-relevant outputs.