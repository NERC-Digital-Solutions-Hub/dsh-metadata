# Details of data structure to ' NW_NH3.csv '

## Overview
- Supplement to the supporting documentation for data series detailed in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Describes the NW_NH3.csv NH3 emissions dataset from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research)
- NH3 emissions measured from plots amended with ammonium nitrate (AN), urea (U), or inhibited urea (IU) using wind tunnels
- Observations collected over 3 weeks following fertiliser applications with daily sampling

## Dataset specifics
- 7 columns, 683 rows
- Emissions dataset derived from grassland fertiliser trial 2016
- Data collection context: wind tunnel measurements on plots with different fertilisers; 3 applications

## Data structure and fields
- Time_Start: Date and time at start of sampling period
- Time_End: Date and time at end of sampling period
- N_app: 1, 2, or 3 indicating fertiliser application number
  - 1st & 2nd applications: 90 kg ha⁻¹
  - 3rd application: 60 kg ha⁻¹
- Block: Blocking factor of randomized block design (1–4)
- Plot: Plot number (1–16); plot size 2 × 4 m
- Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea, agrotain)
- Emission_rate_kghad: Emission rate of NH3 from plot for 1 day (kg NH3-N ha⁻¹ d⁻¹)

## Measurement and data quality notes
- Wind tunnel anemometers on:
  - Plot 3 during the first and second applications
  - Plot 14 during the third application
  - Failures led to removal of those values and replacement with the mean of surrounding wind tunnels
- Detection limit: 0.1 mg NH4-N L⁻¹
- Negative NH3 fluxes replaced with 0

## Missing data handling
- Mean imputation used to provide first-day data for NH3 emissions when data were missing
  - N_app 1, day 1, plot 3: No wind tunnel on plot 3
  - N_app 2, day 1, plot 2: samples lost
  - N_app 2, day 1, plot 3: pump did not run (no gas sampled)
- Additional missing data due to pump not running:
  - N_app 2, day 19, plot 9
  - N_app 3, day 11, plot 9
  - N_app 3, day 3, plot 14

## Provenance and context
- Data originate from the 2016 grassland fertiliser trial at North Wyke Research Station (Rothamsted Research)
- Documentation supplements standardized data structure and quality considerations for environmental monitoring datasets
- Emphasizes data cleaning, handling of equipment failures, detection limits, and imputation to support reliable environmental health analysis and policy-relevant monitoring

## Relevance for environmental monitoring and analysis
- Provides a standardized, QA-focused NH3 emission dataset suitable for temporal trend analysis and cross-site comparisons
- Facilitates integration with other environmental datasets by maintaining clear field definitions and data processing steps
- Supports scrutiny of environmental health performance over time through consistent measurement and documentation of data gaps and corrections