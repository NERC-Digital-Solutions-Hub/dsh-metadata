# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 2014 to 2018

## Overview
- Long-term, fortnightly monitoring dataset from the North Basin of Windermere, Cumbria, England (January 2014 – end of 2018).
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg SiO2 per L), phytoplankton chlorophyll a (TOCA, µg per L).
- Data are raw and not yet quality controlled/calibrated; double entered and visually checked.
- Water samples are integrated from 0 to 7 m and collected from a boat at the deepest part of the lake using a marked buoy.

## Sampling Regime and Collection Methods
- Fortnightly sampling regime.
- Measurements collected from January 2014 to the end of 2018.
- Sampled at a single, fixed location (buoy at the deepest part of the lake).

## Data Quality, Limitations and Metadata
- Raw data; quality control and calibration have not been completed.
- Missing data attributed to weather conditions or staff shortages.
- Indicates below-detection-limit values with a "<" sign in the Sign (if<LOD) column for applicable measurements.

## Data Structure and Format
- Data provided as a comma-separated values (CSV) file.
- Columns:
  - Date: date of measurement
  - Variable, Description: names and meanings of each measured parameter (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value, Description: measured values for each variable
  - Sign (if<LOD), Description: indicates if values are below detection limit with a "<" sign
- Units as described for each variable (e.g., TEMP in °C, OXYG in % air-saturation, SECC in m, ALKA in µg CaCO3 per L, etc.).

## GIS and Data Use Implications
- Suitable for time-series visualization of lake surface parameters and water quality indicators.
- Spatial coverage is limited to a single fixed location (North Basin buoy), so spatial analyses are constrained unless combined with additional spatial datasets.
- Can be integrated with other GIS layers to map temporal trends across the basin or inter-annual comparisons.
- Useful for monitoring ecological and water quality changes over the 2014–2018 period and supporting long-term ecological analyses.

## Funding, References and Related Information
- Funding: Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Related publications and uses include: State of the Climate in 2018 (BAMS), temporal/spatial variation in fish environmental DNA, early warning indicators for ecological data, and other long-term ecological datasets.
- Overview reference: Maberly et al. (2017) on long-term ecological data and ecological informatics in the English Lake District.