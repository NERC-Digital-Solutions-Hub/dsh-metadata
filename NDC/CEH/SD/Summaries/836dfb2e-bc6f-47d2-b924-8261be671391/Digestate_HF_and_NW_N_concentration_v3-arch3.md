# Details of data structure to 'Digestate_HF_and_NW_N_concentration.csv'

## Overview
- Supplement to supporting documentation for data series related to CINAg experiments.
- Dataset: 7 columns, 90 rows from the digestate wheat trial 2017.
- Sites: Henfaes Research Center (HF) and North Wyke (NW) research station.
- Measurements: Nitrogen (N) concentrations in wheat components (grain, chaff, straw) at harvest.
- Treatments: 
  - Digestate-related (C = control, D = digestate, AD = acidified digestate, DNI = digestate with nitrification inhibitor DMPP, ADNI = acidified digestate with DMPP)
  - Inorganic N at 75, 150, 225, 300 kg N ha-1 (N-75, N-150, N-225, N-300)
- Note: Grain and chaff N concentrations measured for HF; not measured for NW.

## Dataset composition
- 90 observations (rows) across two sites.
- 7 columns describing site, plot, block, treatment, and N concentrations.
- Data derives from plots amended with varied nitrogen sources and rates, harvested for analysis of N concentration in harvest fractions.

## Data structure and variables
- Site: HF or NW (location of the trial)
- Plot: Plot identifier; all yield measurements derived from the plot except specified plots (1, 19, 25, 31, 47) used for monthly samplings at 150 kg N ha-1
- Block: Blocking factor in randomized block design (1–5)
- Treatment: C, D, AD, DNI, ADNI, and N-75, N-150, N-225, N-300
- Grain_concentration_g_N_kg: N concentration in grain at harvest (g N per kg); Not measured for NW
- Chaff_concentration_g_N_kg: N concentration in chaff at harvest (g N per kg); Not measured for NW
- Straw_concentration_g_N_kg: N concentration in straw at harvest (g N per kg)
- Units: Each concentration expressed as g N per kg; missing/not assessed values indicated as NA where applicable

## Experimental design and sampling details
- Plot sizes differ by site:
  - HF: 1.2 m × 6.5 m (harvest area) for nitrogen addition rates; 1.2 m × 14 m for C, D, AD, DNI, ADNI
  - NW: 2 m × 4.5 m (harvest area) for nitrogen addition rates; 2 m × 9 m for C, D, AD, DNI, ADNI
- Monthly sampling noted for select plots under 150 kg N ha-1 treatment
- Data integrates both digestate-based treatments and inorganic N rates to compare N uptake and distribution among grain, chaff, and straw

## Data availability and governance considerations
- Document is a supplement to broader supporting documentation; metadata and data provenance are described but users may need to consult source documents for full context.
- Uses coded treatments, requiring clear metadata mappings for reproducibility and policy monitoring.
- Not all measurements are available for NW (grain and chaff missing), which should be accounted for in analyses and dashboards.
- NA entries indicate not assessed; data cleaning and harmonisation may be required for integration with other datasets.

## Relevance to monitoring frameworks
- Provides a well-defined data structure enabling monitoring of nitrogen dynamics under different fertilisation strategies, including waste-derived digestates.
- Facilitates evaluation of environmental health implications of N management by comparing N concentrations across grain, chaff, and straw under diverse treatments.
- Supports data governance needs: explicit column definitions, units, and treatment codes aid data quality, transparency, and openness for decision-making.
- Highlights typical data challenges relevant to monitoring frameworks:
  - Data gaps (e.g., NW measurements for grain/chaff)
  - Metadata completeness and consistency
  - Need for data transformation and harmonisation for integration into dashboards or reports
  - Importance of clear documentation to communicate complex experimental results to policymakers and stakeholders