# Details of data structure to ' NW_NH3.csv '

- Overview
  - Supplement to supporting documentation for data series; dataset from grassland fertiliser trial 2016 at North Wyke Research Station (Rothamsted Research).
  - NH3 emissions measured from plots amended with ammonium nitrate (AN), urea (U), or inhibited urea (IU/agrotain); three weeks of daily sampling.

- Dataset characteristics
  - 7 columns, 683 rows.
  - Emission data represent NH3 emissions from plots per day, in kg NH3-N ha-1 d-1.

- Dataset structure (columns and meanings)
  - Time_Start: Date and time at start of sampling period.
  - Time_End: Date and time at end of sampling period.
  - N_app: 1|2|3 denotes fertiliser application; 1st & 2nd applications 90 kg ha-1, 3rd application 60 kg ha-1.
  - Block: 1|2|3|4 blocking factor of randomized block design.
  - Plot: 1–16 plot measured (plot size 2 × 4 m).
  - Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea, agrotain).
  - Emission_rate_kghad: Emission rate of NH3 from plot for 1 day, in kg NH3-N ha-1 d-1.

- Data collection and quality notes
  - Wind tunnel anemometers on plot 3 during first two applications and plot 14 during the third application failed; affected values were removed and replaced with the mean of surrounding wind tunnels.

- Detection and data cleaning
  - Limit of detection: 0.1 mg NH4-N L-1.
  - Negative NH3 fluxes replaced with 0.
  - Mean imputation used to provide day-1 NH3 emission data where missing:
    - N_app 1, day 1, plot 3 – no wind tunnel on plot 3.
    - N_app 2, day 1, plot 2 – samples lost.
    - N_app 2, day 1, plot 3 – pump did not run (no gas sampled).

- Missing data occurrences (examples)
  - N_app 2, day 19, plot 9 – pump did not run.
  - N_app 3, day 11, plot 9 – pump did not run.
  - N_app 3, day 3, plot 14 – pump did not run.

- Purpose and use
  - Structured dataset enabling analysis of NH3 emissions by fertiliser type under grassland trials; preprocessing details support data quality and reproducibility for downstream analyses.