# Digestate_HF_and_NW_N_concentration.csv

## Overview
- A 7-column, 90-row dataset from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) with Bangor University and Rothamsted Research.
- Measures nitrogen (N) concentrations in wheat tissues (grain and chaff for HF; grain/chaff not measured for NW) at harvest.
- Treatments include: zero N control (C), digestate (D), acidified digestate (AD), digestate with nitrification inhibitor (DNI), acidified digestate with nitrification inhibitor (ADNI), and inorganic N at 75, 150, 225, and 300 kg N ha-1 (N-75, N-150, N-225, N-300).
- Purpose: explore how different digestate forms and nitrification inhibitors affect tissue N concentrations, enabling correlations and predictive insights.

## Data Structure and Columns
- Columns (7 total): 
  - Site: HF or NW
  - Plot: plot number; note that plots 1, 19, 25, 31, and 47 were used for monthly samplings for the 150 kg N ha-1 treatment
  - Block: randomised block design factor (1–5)
  - Treatment: C, D, AD, DNI, ADNI, and N-75, N-150, N-225, N-300 (NH4NO3 at specified rates)
  - Grain_concentration_g_N_kg: grain N concentration at harvest (g N kg-1); measured for HF; not measured for NW
  - Chaff_concentration_g_N_kg: chaff N concentration at harvest (g N kg-1); not measured for NW
  - Straw_concentration_g_N_kg: straw N concentration at harvest (g N kg-1)

## Experimental Design and Sampling Notes
- Sites and plot structure:
  - HF: harvest areas of 1.2 m × 6.5 m for nitrogen addition plots; 1.2 m × 14 m for C, D, AD, DNI, ADNI treatments
  - NW: harvest areas of 2.0 m × 4.5 m for nitrogen addition plots; 2.0 m × 9 m for C, D, AD, DNI, ADNI treatments
- Treatments cover both digestate forms and inorganic N at multiple rates, with and without nitrification inhibitor (DMPP)
- NA = Not Assessed (used where measurements were not taken)

## Data Use for Analysts
- Enables analysis of tissue-specific N uptake under different digestate treatments versus inorganic N.
- Supports correlation analyses and predictive modeling of N concentrations across grain, chaff, and straw.
- Data provenance linked to supporting documentation (Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf) for traceability.