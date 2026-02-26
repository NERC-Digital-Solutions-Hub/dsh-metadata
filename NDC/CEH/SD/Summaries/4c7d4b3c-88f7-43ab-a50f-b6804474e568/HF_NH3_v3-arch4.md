# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' HF_NH3.csv '.

## What this dataset contains
- NH3 emissions dataset from grassland fertiliser trial 2016 at Henfaes Research Station (Bangor University)
- Data collected from plots amended with urea or inhibited urea (agrotain)
- Measurements taken over 3 weeks following fertiliser applications with daily sampling

## Dataset structure and fields
- 7 columns and 476 rows
- Time_Start: start date/time of sampling period
- Time_End: end date/time of sampling period
- N_app: 1, 2, or 3 indicating fertiliser application event (first two applications at 90 kg ha-1, third application at 60 kg ha-1)
- Plot: 1–16
- Block: 1–4 (randomised block design)
- Treatment: AN (ammonium nitrate), U (urea), IU (inhibited urea, agrotain)
- Emission_rate_kghad: NH3 emission rate for the day, in kg NH3-N ha-1 d-1

## Data collection and processing notes
- Wind tunnel anemometer data missing for:
  - Plot 3 during the first and second applications
  - Plot 14 during the third application
- Replaced missing/failed anemometer values with the mean of surrounding wind tunnels
- Limit of detection: 0.1 mg NH4-N L-1
- Negative NH3 flux values were set to 0

## Data quality, metadata, and standards
- Supplement to the main Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Instrument failures and data cleaning steps (replacement with means, LOD handling, and zeroing negatives) affect raw measurements
- Dataset structure and units are clearly defined to support discoverability and reuse within a broader data system
- Metadata specifics beyond the described fields (e.g., format, updates) should be aligned with the overarching data governance and standards governing HF_NH3.csv and related data series