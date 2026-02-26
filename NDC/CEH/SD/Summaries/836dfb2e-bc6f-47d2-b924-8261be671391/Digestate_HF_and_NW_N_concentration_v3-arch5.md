Digestate_HF_and_NW_N_concentration.csv

## Overview
- Supplement detailing the data structure for the dataset Digestate_HF_and_NW_N_concentration.csv.
- Origin: Digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations (Bangor University and Rothamsted Research).
- Dataset characteristics: 7 columns and 90 rows.
- Focus: Nitrogen (N) concentrations in wheat components (grain, chaff, straw) at harvest under various treatments and N rates.

## Dataset structure
- Sites
  - HF: Henfaes
  - NW: North Wyke
- Plot
  - Plot number; note: plots 1, 19, 25, 31 and 47 were used for monthly samplings for the treatment 150 kg N ha-1.
- Block
  - Blocking factor with values 1–5 (randomised block design).
- Treatment
  - Digestate-related: C (control, zero N), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
  - Mineral N controls: N-75, N-150, N-225, N-300 representing NH4NO3 at 75, 150, 225, and 300 kg N ha-1.
- Grain_concentration_g_N_kg
  - Concentration of N in grain at harvest (g N kg-1). Not measured for NW.
- Chaff_concentration_g_N_kg
  - Concentration of N in chaff at harvest (g N kg-1).
- Straw_concentration_g_N_kg
  - Concentration of N in straw at harvest (g N kg-1).

## Units and special notes
- All concentration values are in g N per kg for the respective plant part.
- Not measured (NA) is indicated where applicable (e.g., grain concentration not measured for NW).

## Experimental and data collection details
- Experimental scope: Digestate-based treatments and mineral N comparison across two sites.
- Harvest material: Measurements taken from plots corresponding to the listed treatments and N rates.
- Plot sizes and harvesting areas vary by site and treatment:
  - HF: 1.2 m × 6.5 m (harvest area) for nitrogen addition rate plots; 1.2 m × 14 m for C, D, AD, DNI, ADNI plots.
  - NW: 2 m × 4.5 m (harvest area) for nitrogen addition rate plots; 2 m × 9 m for C, D, AD, DNI, ADNI plots.

## Data governance and quality considerations
- Completeness: Grain concentration data not available for NW; document explicitly in metadata to avoid misinterpretation.
- Metadata alignment: Ensure consistent naming and unit conventions across sites (HF and NW) for interoperability.
- Noted data constraints: Some plots are earmarked for monthly sampling (monthly sampling for 150 kg N ha-1); consider this in downstream analyses and documentation.
- Provenance: Ties to broader supporting documentation and data series; this file is a structure detailing how the concentration data are organized and should be interpreted within the larger dataset.