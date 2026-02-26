# Details of data structure to 'Digestate_HF_and_NW_pH_NH4_NO3_v2.csv'

## Overview
- Supplementary data description for the Digestate_HF_and_NW_pH_NH4_NO3_v2.csv dataset.
- 8 columns, 950 rows, from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Measures soil pH, ammonium (NH4), and nitrate (NO3).

## Dataset Structure (columns and meaning)
- Site: HF (Henfaes) or NW (North Wyke).
- Date: Date soil was sampled from the field.
- Plot: Experimental plot number.
- Block: Blocking factor in randomized block design (1–5).
- Treatment: C, D, AD, DNI, ADNI representing:
  - C = zero N control
  - D = digestate
  - AD = acidified digestate
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with DMPP
- Soil_pH: pH of soil sample.
- Soil_NH4_mg_kg: NH4 in soil, mg N per kg dry soil.
- Soil_NO3_mg_kg: NO3 in soil, mg N per kg dry soil.

## Experimental context and locations
- Year and trial: Digestate wheat trial, 2017.
- Sites:
  - HF: Henfaes Research Center
  - NW: North Wyke, Rothamsted Research collaboration
- Plot sizes (harvest areas) by site and treatment group:
  - HF: 1.2 m × 6.5 m for nitrogen addition-rate plots; 1.2 m × 14 m for C, D, AD, DNI, ADNI plots.
  - NW: 2 m × 4.5 m for nitrogen addition-rate plots; 2 m × 9 m for C, D, AD, DNI, ADNI plots.
- NA = Not assessed where data not collected.

## GIS relevance and usage considerations
- Spatial identifiers: Site, Plot, and Block enable mapping of samples to field layouts.
- Temporal aspect: Date allows time-series or trend analysis across sampling events.
- Attribute data: Soil_pH, Soil_NH4_mg_kg, Soil_NO3_mg_kg provide key soil chemistry layers for spatial analyses.
- Data integration: Units (mg N kg-1 dry soil) facilitate compatibility with soil property maps and other GIS datasets.
- Data quality: Some fields may be NA; plan for missing data handling in GIS workflows.

## Data provenance and notes
- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Dataset derived from the 2017 digestate wheat trials at HF and NW, with data on soil pH, NH4, and NO3.