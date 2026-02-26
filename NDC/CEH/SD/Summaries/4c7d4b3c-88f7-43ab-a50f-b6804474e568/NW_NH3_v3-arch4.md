# Details of data structure to ' NW_NH3.csv '

## Overview
- Supplement to supporting documentation for CINAg experiments.
- Contains NH3 emissions data from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).
- 7 columns, 683 rows; daily NH3 emissions measured for 3 weeks after fertiliser applications.
- Fertiliser types: ammonium nitrate (AN), urea (U), inhibited urea (IU, Agrotain).

## Dataset contents
- NH3 emissions data across plots amended with different fertilisers.
- Measurements captured on a daily basis during the 3-week post-application period.
- Emission_rate_kghad provided per plot per day.

## Experimental context
- Wind-tunnel based NH3 measurements.
- Trials involve multiple applications: 1st and 2nd applications at 90 kg ha-1; 3rd application at 60 kg ha-1.
- Randomised block design with 4 blocks (Block: 1–4) and 16 plots (Plot: 1–16).
- Emissions measured for three fertiliser applications (N_app: 1, 2, 3).

## Data structure (columns)
- Time_Start: start datetime of sampling period.
- Time_End: end datetime of sampling period.
- N_app: application number (1, 2, or 3); denotes fertilizer type and rate.
- Block: randomised block identifier (1–4).
- Plot: plot identifier (1–16); plot size 2 × 4 m.
- Treatment: fertiliser type (AN, U, IU).
- Emission_rate_kghad: NH3 emission rate for the plot on that day (kg NH3-N ha-1 d-1).

## Data cleaning and quality
- Wind tunnel data from plot 3 (first/second application) and plot 14 (third application) failed; affected values removed and replaced with the mean of surrounding wind tunnels.
- Detection limit: 0.1 mg NH4-N L-1 used as the limit of detection.
- Negative NH3 fluxes replaced with 0.

## Missing data handling
- Mean imputation used to supply missing Day 1 data for NH3 emissions (where applicable):
  - N_app 1, Day 1, Plot 3 (no wind tunnel on Plot 3)
  - N_app 2, Day 1, Plot 2 (samples lost)
  - N_app 2, Day 1, Plot 3 (pump did not run; no gas sampled)
- Other missing data instances:
  - N_app 2, Day 19, Plot 9 (pump did not run)
  - N_app 3, Day 11, Plot 9 (pump did not run)
  - N_app 3, Day 3, Plot 14 (pump did not run)

## Data provenance and references
- This document supplements the data series described in the supporting documentation: Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Provides explicit details of the data structure for NW_NH3.csv and the data cleaning/handling steps applied.