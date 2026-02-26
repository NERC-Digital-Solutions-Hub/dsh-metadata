# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022.

## Overview
- Long-term, fortnightly monitoring dataset from Blelham Tarn, Cumbria, England.
- Records surface temperature, surface oxygen saturation, Secchi depth, water chemistry, and phytoplankton chlorophyll a from January 2021 to end of 2022.
- Data intended for environmental health assessment and informing policy decisions; publicly downloadable values are provided but raw data are not yet fully quality controlled.

## Sampling regime and collection methods
- Variables available (with units): 
  - TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3 per L), pH, NH4N (µg N per L), NO3N (µg N per L), PO4P (µg P per L), TOTP (µg P per L), SIO2 (µg/L), TOCA (µg/L).
- Sampling frequency: fortnightly.
- Depth/interval: integrated 0–5 m water column.
- Collection location: from a boat at a buoy at the deepest part of the lake; if buoy sampling not possible, samples taken from the shore.
- Data available to download correspond to the above variables and measurements.

## Data quality and limitations
- Data are raw and have not yet undergone formal quality control or calibration.
- Double entered and visually checked; remaining missing data attributed to weather, COVID-19 restrictions, or staff shortages.
- Some measurements may be below detection limits (signaled in data).

## Data structure and variables
- Data provided as CSV with columns:
  - Date, Description (variable name), Value (measurement), Sign(if<LOD) for below-detection indicators, Flag (sampling location).
- Flag meanings:
  - Flag = 1: sample taken at buoy location.
  - Flag = 2: sample taken from shore due to inability to access buoy.

## Data governance, access and metadata
- Data are presented with basic descriptive metadata (sampling method, depth, location, units, and detection limits).
- Metadata note: potential barriers include the need for robust metadata to verify dataset suitability for specific analyses and future data governance considerations.
- Encourages sharing of underlying data and clear data governance practices to ensure datasets meet quality and openness standards.

## Funding and governance
- Data collection funded by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE, National Capability).
- Data validation funded by NERC award NE/Y006208/1 (ACCESS-UK, National Capability).