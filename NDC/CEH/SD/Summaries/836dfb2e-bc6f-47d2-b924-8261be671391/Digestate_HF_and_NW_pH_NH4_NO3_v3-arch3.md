# Digestate_HF_and_NW_pH_NH4_NO3_v2.csv

## Overview
- Dataset from the digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations.
- Contains soil chemistry data: pH, ammonium (NH4), and nitrate (NO3).
- Structure: 8 columns, 950 rows.

## Dataset structure
- Site: HF or NW
- Date: date when soil was sampled from the field
- Plot: experimental plot number
- Block: blocking factor (1–5) in a randomised block design
- Treatment: C (zero N control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
- Soil_pH: soil pH
- Soil_NH4_mg_kg: NH4 in mg N kg⁻¹ dry soil
- Soil_NO3_mg_kg: NO3 in mg N kg⁻¹ dry soil
- NA = Not assessed

## Experimental design and sites
- Design: randomized block with multiple plots per site
- Sites: HF (Henfaes) and NW (North Wyke)
- Plot sizes:
  - HF: 1.2 m × 6.5 m (nitrogen addition rate plots) and 1.2 m × 14 m (C, D, AD, DNI, ADNI)
  - NW: 2 m × 4.5 m (nitrogen addition rate plots) and 2 m × 9 m (C, D, AD, DNI, ADNI)

## Data provenance and context
- Supplement to supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Data originate from the 2017 digestate wheat trial at Bangor University and Rothamsted Research facilities
- Includes field sampling dates and specific treatment regimes to enable monitoring of soil chemical responses to digestate amendments

## Variables, units, and interpretation notes
- Units:
  - Soil_NH4_mg_kg: mg N per kg dry soil
  - Soil_NO3_mg_kg: mg N per kg dry soil
- Date format corresponds to field sampling dates
- NA indicates data not assessed for a given row/entry

## Considerations for monitoring and governance
- Metadata completeness: explicit column explanations and units facilitate cross-study comparability, aligning with data governance needs
- Data accessibility: dataset specifies sharing of underlying measurements (where applicable) via originators; potential barriers noted through the broader monitoring context (e.g., data silos, access timeliness)
- Data quality: clear definitions of treatments and blocking factors support reproducibility and trend analysis
- Limitations to consider: site-specific plot size differences and the 2017 time frame; ensure alignment with current monitoring objectives and metadata standards when integrating with ongoing datasets