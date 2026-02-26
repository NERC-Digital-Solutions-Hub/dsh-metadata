# NW_NH3.csv

## Overview
- Supplement to the CINAg experiments supporting documentation.
- NH3 emissions dataset from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).

## Dataset details
- 7 columns, 683 rows.
- Measurements of NH3 emissions from plots amended with ammonium nitrate (AN), urea (U), or inhibited urea (IU, agrotain).
- Wind-tunnel based emissions measured for 3 weeks following fertiliser applications.
- Daily sampling period.

## Data structure and columns
- Time_Start: Date and time at the start of the sampling period.
- Time_End: Date and time at the end of the sampling period.
- N_app: 1|2|3 denotes fertiliser application. 1st & 2nd applications were 90 kg ha-1; 3rd application 60 kg ha-1.
- Block: 1|2|3|4 blocking factor of a randomized block design.
- Plot: 1–16. Plot size 2 × 4 m.
- Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea, agrotain).
- Emission_rate_kghad: Emission rate of NH3 from the plot for 1 day, in kg NH3-N ha-1 d-1.

## Data quality and processing
- Wind tunnel anemometers on plot 3 (first and second applications) and plot 14 (third application) failed; affected values were removed and replaced with the mean of surrounding wind tunnels.
- Detection limit: 0.1 mg NH4-N L-1.
- Negative NH3 fluxes replaced with 0.

## Missing data and imputation
- Mean imputation used to provide 1st-day NH3 emissions where data were missing.
  - N_app 1, day 1, plot 3: No wind tunnel on plot 3.
  - N_app 2, day 1, plot 2: samples lost.
  - N_app 2, day 1, plot 3: pump did not run (no gas sampled).
- Other missing data due to pump failures:
  - N_app 2, day 19, plot 9.
  - N_app 3, day 11, plot 9.
  - N_app 3, day 3, plot 14.