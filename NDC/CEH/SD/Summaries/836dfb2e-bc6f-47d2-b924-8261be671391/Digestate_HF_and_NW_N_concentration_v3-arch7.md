# Digestate_HF_and_NW_N_concentration.csv

## Overview
- Dataset of nitrogen (N) concentrations in winter wheat (grain, chaff, straw) from a 2017 digestate trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- 90 rows and 7 columns.
- Treatments include zero-N control (C), digestate (D), acidified digestate (AD), digestate with nitrification inhibitor (DNI), acidified digestate with nitrification inhibitor (ADNI), and NH4NO3 at 75, 150, 225, and 300 kg N ha-1.
- Data sourced from plots used to derive yield measurements, with some plots allocated for monthly samplings.

## Data structure (columns and units)
- Site: HF or NW (location of the plot)
- Plot: plot number (source of yield measurements; with exceptions)
- Block: block number (1–5) in a randomized block design
- Treatment: C, D, AD, DNI, ADNI, N-75, N-150, N-225, N-300
- Grain_concentration_g_N_kg: grain N concentration at harvest (g N kg-1); not measured for NW
- Chaff_concentration_g_N_kg: chaff N concentration at harvest (g N kg-1)
- Straw_concentration_g_N_kg: straw N concentration at harvest (g N kg-1)
- Note: NA indicates not assessed for a given entry; units specified as g N kg-1 where applicable

## Sites, plots, and experimental design
- Sites: HF (Henfaes) and NW (North Wyke)
- Plot structure: specific plots from which yield measurements were derived
  - Exception: plots 1, 19, 25, 31, and 47 used for monthly samplings at treatment 150 kg N ha-1
- Design: randomized blocks (Block 1–5)
- Plot sizes vary by site and treatment:
  - HF: 1.2 m × 6.5 m harvest area for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI
  - NW: 2 m × 4.5 m harvest area for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI

## Treatments and nitrogen inputs
- Digestate-related: C (control, zero N), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP)
- Mineral N references: N-75, N-150, N-225, N-300 (NH4NO3 at corresponding kg N ha-1)

## Measurement details and data quality
- Concentrations measured at harvest for grain (grain_concentration_g_N_kg), chaff (chaff_concentration_g_N_kg), and straw (straw_concentration_g_N_kg)
- Grain concentration not measured for NW
- NA entries indicate not assessed
- Data requires careful harmonization if used in GIS analyses due to site-specific plot sizes and missing NW grain data

## Provenance and context
- Year: 2017
- Experiment: digestate wheat trial
- Collaborating institutions: Henfaes Research Center (Bangor University) and Rothamsted Research (North Wyke)
- Supplement to broader supporting documentation for data series (referenced as Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)

## GIS-oriented considerations and uses
- Spatial tagging via Site, Plot, and Block enables mapping of N concentrations across fields.
- Differing plot sizes and incomplete NW grain data require careful normalization and handling of spatial resolution.
- Useful for visualizing spatial patterns of N concentration by treatment and site, and for integrating with yield or soil data.
- Data cleaning needed to address NA values, missing NW grain measurements, and potential resolution mismatches between HF and NW.