# Details of data structure to 'HF_NH3.csv'

- Overview
  - NH3 emissions dataset from grassland fertiliser trial (2016) at Henfaes Research Station (Bangor University).
  - 7 columns, 476 rows.
  - Measurements taken from plots amended with urea or inhibited urea (agrotain) using wind tunnels.
  - Emissions measured for 3 weeks following fertiliser applications with daily sampling.

- Data collection context
  - Emissions measured from plots with 1st and 2nd applications at 90 kg ha-1, and 3rd application at 60 kg ha-1.
  - Wind tunnel anemometers on plot 3 (1st/2nd applications) and plot 14 (3rd application) failed; corresponding values removed and replaced with the mean of surrounding wind tunnels.

- Data structure / columns
  - Time_Start: Date and time at start of sampling period
  - Time_End: Date and time at end of sampling period
  - N_app: 1|2|3 denotes fertiliser application; 1st & 2nd applications 90 kg ha-1, 3rd application 60 kg ha-1
  - Plot: 1–16; plot measured; Plot size 2 × 4 m
  - Block: 1|2|3|4; blocking factor of randomised block design
  - Treatment: AN|U|IU; N fertiliser type; AN = ammonium nitrate, U = urea, IU = inhibited urea (agrotain)
  - Emission_rate_kghad: Emission rate of NH3 from plot for 1 day; unit kg NH3-N ha-1 d-1

- Data cleaning and quality notes
  - Wind tunnel data failures on specific plots were substituted by the mean of surrounding tunnels.
  - Limit of detection: 0.1 mg NH4-N L-1.
  - Negative NH3 flux values were replaced with 0.

- Provenance and supplementary context
  - This document supplements the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
  - Data file reference: HF_NH3.csv.