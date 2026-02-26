# Description, Experimental Design and Collection: These data represent glucosinolate concentrations collected from Brassica napus plants within FreeAir Diesel and Ozone Enrichment (FADOE) rings.

## Overview
- Datasets measure glucosinolate concentrations in Brassica napus under controlled pollution and aphid-inoculation conditions.
- Seven glucosinolates were quantified, along with aggregated totals for indolic, aliphatic, and all glucosinolates.

## Experimental design and collection details
- Field setup: FADOE rings were located in a wheat field in 2018 (lat 51.482853, lon -0.897749) and moved to an adjacent field in 2019 (lat 51.482374, lon -0.895855).
- Pollution treatments: Four treatments applied to two rings each:
  - Diesel exhaust (D)
  - Ozone (O3)
  - Diesel exhaust plus ozone (D+O3)
  - Control (CON; natural air)
- Sampling units: Each FADOE ring was assigned a ring number (Ring; Column B). Samples coded by Ring, aphid inoculation treatment, plant number, and replicate (Sample_ug_g-1_dw; Column A).
- Aphid inoculation: Plants were inoculated at five weeks with either 50 aphids, 10 aphids, or none. Leaves for glucosinolate analysis were taken from three plants from two aphid treatments: 50 aphids (Aphids_present = Yes) or no aphids (Aphids_present = No).
- Sample processing: Leaves were freeze-dried and ground to a fine powder; up to three replicate samples were analyzed per ground sample (Replicate; Column F).
- Analytical method: Glucosinolates identified and quantified by LC-MS following established protocols (references [2]).
- Data columns for glucosinolates measured:
  - Progoitrin
  - Glucoalyssin
  - Gluconapin
  - Glucobrassicanapin
  - Glucobrassicin
  - 4-methoxyglucobrassicin
  - Neoglucobrassicin
- Summary variables:
  - Indole_GLS (total indolic glucosinolates)
  - Aliphatic_GLS (total aliphatic glucosinolates)
  - Total_GLS (all glucosinolates)

## Data structure and references
- Reference methods:
  - FADOE configuration methodology and quality control: Ryalls et al., 2022 (Environmental Pollution, article 297, 118847).
  - LC-MS glucosinolate protocol: Jasper et al., 2020 (Postharvest Biology and Technology 163, 111157).
- Column references:
  - Sample_ug_g-1_dw (A)
  - Ring (B)
  - Pollutant (C)
  - Plant_ID (D)
  - Aphids_present (E)
  - Replicate (F)
  - GLS concentration columns (G–M)
  - Indole_GLS (N), Aliphatic_GLS (O), Total_GLS (P)

## Potential uses for Data Support and end-user applications
- Create self-serve dashboards comparing glucosinolate profiles across pollution treatments (D, O3, D+O3, CON) and aphid presence (Yes/No).
- Investigate how environmental stressors (air pollutants) interact with biotic stress (aphid infestation) to influence GLS composition and total GLS.
- Combine with external environmental or field metadata to explore spatial or temporal patterns (2018 vs 2019 fields).
- Data quality planning: verify sampling consistency, replicate handling, and LC-MS QC against described references to ensure reliable outputs.
- Promote outputs and gather user feedback to refine data products and support broader data use in policy or agronomic contexts.