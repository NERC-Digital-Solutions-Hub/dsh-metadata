# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013

## Overview
- Long-term monitoring dataset from Derwent Water, Cumbria, England, covering 1990–2013.
- Fortnightly sampling of multiple limnological variables to support understanding of lake physical, chemical, and biological conditions.
- Data intended for analysis and publication, with ongoing relevance to climate and ecosystem studies.

## What data are included
- Surface temperature (TEMP) in degrees Celsius.
- Surface oxygen saturation (OXYG) in % air-saturation.
- Secchi depth (SECC) in metres (water clarity).
- Alkalinity (ALKA) in µg CaCO3 per litre.
- pH (PH).
- Ammonium (NH4N) in µg N per litre.
- Nitrate (NO3N) in µg N per litre.
- Soluble reactive phosphate (PO4P) in µg P per litre.
- Total phosphorus (TOTP) in µg P per litre.
- Dissolved reactive silicon (SIO2) in µg per litre.
- Phytoplankton chlorophyll a (TOCA) in µg per litre.

## Sampling regime
- Fortnightly sampling from a boat at the deepest part of the lake (marked buoy).
- When buoy access was not possible, samples collected from the shore (Flag 2).
- Water samples represent 0–5 m integrated depth.
- Data span August 1990 to end of 2013.

## Data quality, limitations, and caveats
- Raw data: not yet quality controlled or calibrated (except double entries from 2005 onward).
- Visual checks conducted; no formal QC applied in the dataset release.
- Gaps: March–June 2001 missing due to foot-and-mouth disease lockdown; additional missing data in 2009 due to weather.
- Some measurements below detection limits marked with a < sign in sign_if_LT_LOD.
- Metadata provide flags for sampling location (Flag 1: buoy; Flag 2: shore).

## Data structure and metadata
- File format: comma-separated values (CSV).
- Key columns:
  - Date: measurement date.
  - Variable, Description: name and unit of each measured variable (TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value, Description: measured values for each variable.
  - Sign_if_LT_LOD, Description: indicator if value is below detection limit.
  - Flag, Description: sampling location indicator (1 = buoy, 2 = shore).
- Clear documentation of measurement context and potential data gaps to enable proper interpretation and cleaning.

## Access, re-use, and transformation considerations
- Data are available as raw CSV with minimal QC; appropriate for transformation, QC, and integration with other datasets.
- Useful for analyses of long-term trends in lake temperature, chemistry, and productivity, or for cross-site comparative studies when harmonized with similar datasets.
- Provenance is documented, including methods and sampling regime, aiding reproducibility and audit trails.

## Provenance and example usage
- Several publications have used this dataset to examine climate-related and ecological questions, including:
  - The impact of climate change on physical characteristics of larger lakes in the English Lake District.
  - Catchment productivity controls on CO2 emissions from lakes.
  - Fisheries-related studies in Cumbria, including historical introductions and management considerations.
  - Broader context on lake temperature trajectories and related climate indicators.