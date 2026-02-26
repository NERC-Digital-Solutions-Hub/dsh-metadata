# Details of data structure to ' Digestate_HF_and_NW_N_concentration.csv '

## Overview
- Dataset: 90 rows, 7 columns.
- Context: Digestate wheat trial 2017 conducted at Henfaes Research Center (HF) and North Wyke (NW) with collaboration from Bangor University and Rothamsted Research.
- Measurements: Nitrogen (N) concentrations in wheat components at harvest—grain (and chaff for HF, plus straw).
- Treatments: Control (C), digestate (D), acidified digestate (AD), digestate with nitrification inhibitor (DNI), acidified digestate with nitrification inhibitor (ADNI), plus inorganic N at 75, 150, 225, and 300 kg N ha-1 (N-75, N-150, N-225, N-300).
- Columns capture location, experimental unit, treatment, and N concentrations.

## Dataset structure and columns
- Columns (7 total) with explanations and units:
  - Site: HF (Henfaes) or NW (North Wyke)
  - Plot: plot number (from which yield measurements are derived; note monthly samplings for 150 kg N ha-1 on plots 1, 19, 25, 31, and 47)
  - Block: randomised block design (1, 2, 3, 4, 5)
  - Treatment: C, D, AD, DNI, ADNI, N-75, N-150, N-225, N-300
  - Grain_concentration_g_N_kg: nitrogen concentration in grain, g N per kg
  - Chaff_concentration_g_N_kg: nitrogen concentration in chaff, g N per kg (Not measured for NW)
  - Straw_concentration_g_N_kg: nitrogen concentration in straw, g N per kg
- NA = Not Assessed

## Experimental design and plot context
- Sites and plot sizes:
  - HF: harvest area 1.2 m × 6.5 m for nitrogen addition rate treatments; 1.2 m × 14 m for C, D, AD, DNI, ADNI
  - NW: harvest area 2 m × 4.5 m for nitrogen addition rate treatments; 2 m × 9 m for C, D, AD, DNI, ADNI

## Measurement details and data constraints
- Measured components: grain (plus chaff for HF) and straw nitrogen concentrations at harvest
- Treatment mapping: explicit pairing of digestate-based treatments with varying inorganic N rates (N-75 to N-300)
- NW limitation: chaff concentration not measured (Chaff_concentration_g_N_kg = NA for NW)

## How to use the data
- Compare nitrogen partitioning across digestate treatments vs inorganic nitrogen across rates
- Analyze the impact of processing (acidification, nitrification inhibitor) on N allocation to grain, chaff, and straw
- Create data products (dashboards, pivot tables) to enable self-serve exploration by site, treatment, and N rate
- Integrate with supporting documentation to understand full experimental context and data quality considerations

## Notes for data users
- Data supplements a broader documentation set (Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)
- Be mindful of partial data (e.g., Chaff concentration not collected at NW) and targeted sampling plots for monthly measurements at the 150 kg N ha-1 rate