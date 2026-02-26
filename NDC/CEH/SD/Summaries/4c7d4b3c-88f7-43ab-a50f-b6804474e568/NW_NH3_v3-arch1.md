# Details of data structure to ' NW_NH3.csv '

## Overview
- Supplements the data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- NH3 emissions dataset from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).
- Measurements from plots amended with ammonium nitrate (AN), urea (U), or inhibited urea (IU; agrotain).
- Emissions recorded for 3 weeks following fertiliser applications with daily sampling.
- Dataset: 7 columns, 683 rows.

## Dataset structure
- Time_Start: Date/time at start of sampling period
- Time_End: Date/time at end of sampling period
- N_app: 1|2|3 denotes fertiliser application; 1st & 2nd applications 90 kg ha-1, 3rd application 60 kg ha-1
- Block: 1|2|3|4 blocking factor of randomized block design
- Plot: 1–16; plot size 2 × 4 m
- Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea)
- Emission_rate_kghad: Emission rate of NH3 from plot for 1 day, in kg NH3-N ha-1 d-1

## Measurements and conditions
- Emissions measured from plots treated with AN, U, or IU.
- Daily NH3 emission data collected for 3 weeks after each application.

## Instrumentation and data adjustments
- Wind tunnel anemometers on plot 3 (first and second applications) and plot 14 (third application) failed.
- Failed anemometer values were replaced with the mean of surrounding wind tunnels.

## Detection limits and data cleaning
- Detection limit: 0.1 mg NH4-N L-1.
- Negative NH3 fluxes replaced with 0.

## Missing data handling and imputation
- Mean imputation used to provide Day 1 NH3 data where missing.
- Specific Day 1 imputation cases occurred due to:
  - N_app 1, Day 1, Plot 3: No wind tunnel on plot 3
  - N_app 2, Day 1, Plot 2: samples lost
  - N_app 2, Day 1, Plot 3: pump did not run
- Additional missing data due to pump failures on:
  - N_app 2, Day 19, Plot 9
  - N_app 3, Day 11, Plot 9
  - N_app 3, Day 3, Plot 14

## Data provenance and usage
- Data originate from the North Wyke grassland fertiliser trial (2016) and are intended for analysis of NH3 emissions under different fertiliser treatments.
- This document serves as a structural supplement to the main CINAg experiments documentation.