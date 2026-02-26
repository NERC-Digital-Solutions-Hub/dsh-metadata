# Details of data structure to 'Digestate_HF_and_NW_pH_NH4_NO3_v2.csv'

## Overview
- Supplement describing the data structure of the dataset Digestate_HF_and_NW_pH_NH4_NO3_v2.csv.
- Dataset comprises 8 columns and 950 rows from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) research station.
- Variables cover soil pH, ammonium (NH4), and nitrate (NO3) measurements.

## Dataset contents
- Sites: HF and NW.
- Date: date soil was sampled from the field.
- Plot: experimental plot number.
- Block: blocking factor in the randomized block design (values 1–5).
- Treatment: digestate-related treatments; C = zero N control, D = digestate, AD = acidified digestate, DNI = digestate with nitrification inhibitor (DMPP), ADNI = acidified digestate with DMPP.
- Soil_pH: pH of the soil sample.
- Soil_NH4_mg_kg: ammonium content, mg N per kg dry soil.
- Soil_NO3_mg_kg: nitrate content, mg N per kg dry soil.

## Column details
- Site: HF or NW (two sites).
- Date: date of soil sampling.
- Plot: numerical plot identifier.
- Block: blocking factor in the experiment (1–5).
- Treatment: categorical treatment codes as defined above.
- Soil_pH: numerical pH value.
- Soil_NH4_mg_kg: numeric NH4 concentration (mg N kg-1 dry soil).
- Soil_NO3_mg_kg: numeric NO3 concentration (mg N kg-1 dry soil).

## Experimental design specifics
- Plot sizes:
  - At HF: 1.2 m x 6.5 m (harvest area) for nitrogen addition rate treatments; 1.2 m x 14 m for C, D, AD, DNI, ADNI.
  - At NW: 2 m x 4.5 m (harvest area) for nitrogen addition rate treatments; 2 m x 9 m for C, D, AD, DNI, ADNI.
- NA = Not assessed (some data points not recorded).

## Data context and usage
- This document is supplementary to the supporting documentation for CINAg experiments (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Provides the defined structure and units to support data cleaning, validation, and integration with other data sources.
- Useful for data support tasks such as ensuring consistency when combining with related datasets, preparing dashboards, or generating reports for end users.

## Notes
- The dataset includes instances labeled NA indicating not assessed data points.