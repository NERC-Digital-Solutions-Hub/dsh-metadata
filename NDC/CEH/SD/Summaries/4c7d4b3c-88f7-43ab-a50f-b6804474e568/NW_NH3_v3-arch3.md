# This document is a supplement to the supporting documentation for data series detailed in: 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'

## Overview
- Supplements data series documentation for NH3 emissions dataset from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).
- Emissions measured over 3 weeks following fertiliser applications with daily sampling.
- Fertilisers tested: ammonium nitrate (AN), urea (U), inhibited urea (IU, agrotain).

## Dataset structure
- 7 columns, 683 rows.
- Columns and meaning:
  - Time_Start: date/time at start of sampling period
  - Time_End: date/time at end of sampling period
  - N_app: 1|2|3 denotes fertiliser application; amounts: 1st & 2nd applications 90 kg ha^-1, 3rd application 60 kg ha^-1
  - Block: 1|2|3|4 (randomised block design)
  - Plot: 1–16 (plot measured; plot size 2 × 4 m)
  - Treatment: AN|U|IU (fertiliser type)
  - Emission_rate_kghad: NH3 emission rate from plot for 1 day in kg NH3-N ha^-1 d^-1
- Data quality notes:
  - Wind tunnel anemometers on plot 3 (first two applications) and plot 14 (third application) failed; their values replaced with the mean of surrounding wind tunnels.

## Data collection and processing
- Emissions measured using wind tunnels on plots after each fertiliser application.
- Daily sampling over the 3-week period.
- Detection limit: 0.1 mg NH4-N L^-1.
- Negative NH3 flux values replaced with 0.
- Data were cleaned and adjusted where necessary (e.g., imputed/normalized values where equipment was unavailable).

## Missing data and imputation
- Day-1 NH3 emissions for some plots were missing and imputed using mean day data.
- Specific imputations noted:
  - N_app 1, day 1, plot 3: No wind tunnel on plot 3
  - N_app 2, day 1, plot 2: samples lost
  - N_app 2, day 1, plot 3: pump did not run (no gas sampled)
- Other missing entries:
  - N_app 2, day 19, plot 9: pump did not run
  - N_app 3, day 11, plot 9: pump did not run
  - N_app 3, day 3, plot 14: pump did not run

## Data provenance and governance
- Source: grassland fertiliser trial, 2016, North Wyke Research Station (Rothamsted Research).
- Document is a supplement to the main data documentation (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Describes data structure, measurement methodology, data cleaning, and imputation practices to support transparency and potential reuse for monitoring and evaluation purposes.