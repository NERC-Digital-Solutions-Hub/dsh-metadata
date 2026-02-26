# Details of data structure to 'HF_NH3.csv'

## Overview
- Supplement to the supporting documentation for CINAg experiments, detailing the NH3 emissions dataset from a 2016 grassland fertiliser trial at Henfaes Research Station (Bangor University).
- Emissions measured from plots amended with urea or inhibited urea (agrotain) using wind tunnels.
- Measurements collected over 3 weeks following fertiliser applications with daily sampling.

## Dataset contents and scope
- 7 columns, 476 rows.
- Dataset name: HF_NH3.csv.
- Emissions are NH3 fluxes from plots treated with different nitrogen fertilisers.
- Location: grassland fertiliser trial, 2016, Henfaes Research Station.

## Data columns and definitions
- Time_Start: Date and time at start of sampling period.
- Time_End: Date and time at end of sampling period.
- N_app: 1, 2, or 3 indicating fertiliser application sequence.
  - 1st & 2nd applications: 90 kg ha-1
  - 3rd application: 60 kg ha-1
- Plot: 1–16, the measured plot.
- Block: 1–4, blocking factor of randomized block design.
- Treatment: AN, U, IU
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
- Emission_rate_kghad: emission rate for NH3 from the plot for one day, in kg NH3-N ha-1 d-1.

## Measurement method and schedule
- NH3 emissions measured using wind tunnels.
- Measurements cover 3 weeks after fertiliser application.
- Daily sampling period.

## Data quality, cleaning and transformations
- Some wind tunnel anemometers failed:
  - Plot 3 during the first and second applications.
  - Plot 14 during the third application.
- Failed anemometer values were removed and replaced with the mean of surrounding wind tunnels.
- Limit of detection: 0.1 mg NH4-N L-1.
- Negative NH3 fluxes replaced with 0.

## Metadata, governance and challenges
- Document serves as a data-structure supplement to broader documentation; highlights the importance of metadata for data usability.
- Notes potential barriers such as data gaps, inconsistent metadata, and the need for clear data transformations and provenance when using the dataset for monitoring frameworks.