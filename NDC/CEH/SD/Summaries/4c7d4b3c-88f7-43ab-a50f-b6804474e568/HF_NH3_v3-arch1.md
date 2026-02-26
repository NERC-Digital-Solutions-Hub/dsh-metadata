# Details of data structure to ' HF_NH3.csv '

- This document supplements the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf and details the HF_NH3.csv dataset.
- Dataset origin: grassland fertiliser trial 2016, Henfaes Research Station (Bangor University).
- Focus: NH3 emissions measured from plots amended with urea or inhibited urea (agrotain) fertilisers using wind tunnels.
- Sampling period: emissions measured for 3 weeks following fertiliser applications with daily sampling.

## Dataset overview

- 7 columns, 476 rows.
- Emissions dataset capturing NH3 flux from field plots under different fertiliser treatments.
- Measurements taken across multiple applications and plots within a randomized block design.

## Data structure and columns

- Time_Start: Date and time at the start of the sampling period.
- Time_End: Date and time at the end of the sampling period.
- N_app: Fertiliser application number (1, 2, or 3). 1st & 2nd applications at 90 kg ha-1; 3rd application at 60 kg ha-1.
- Plot: Plot identifier (1–16); each plot is 2 × 4 m.
- Block: Blocking factor (1–4) in the randomized block design.
- Treatment: Fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea/agrotain).
- Emission_rate_kghad: Emission rate of NH3 from the plot for 1 day, in kg NH3-N ha-1 d-1.

## Measurement specifics and data quality

- Wind tunnel data gaps: Anemometer failures occurred—plots 3 (first and second applications) and 14 (third application). Affected values were removed and replaced with the mean of surrounding wind tunnels.
- Detection limit: 0.1 mg NH4-N L-1 used as the limit of detection.
- Non-detects: Negative NH3 fluxes replaced with 0.

## Data handling and interpretation

- The dataset includes data cleaning steps for instrument failures and non-detects to ensure consistency.
- Emission_rate_kghad represents daily NH3-N emissions per plot under the specified fertiliser treatment and application.
- Data are suitable for comparing emission responses across fertiliser types, application events, and plot/bock combinations, with potential for time-series or mixed-effects modelling.

## Context and access

- Supplement to broader CINAg experiments documentation.
- HF_NH3.csv provides the structured data necessary for analysing NH3 emissions from the 2016 grassland fertiliser trial at Henfaes Research Station.