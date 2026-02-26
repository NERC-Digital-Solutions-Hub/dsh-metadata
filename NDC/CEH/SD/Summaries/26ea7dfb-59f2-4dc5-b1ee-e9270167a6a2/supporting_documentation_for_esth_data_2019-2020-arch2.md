# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019  2020.

## Overview
- Long-term monitoring dataset from Esthwaite Tarn, Cumbria, England, with fortnightly sampling during 2019–2020.
- Measured variables (with units):
  - TEMP: surface temperature in °C
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg per litre as CaCO3
  - pH: acidity/alkalinity pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Sample basis: water integrated from 0–5 m; boat-based at buoy location (Latitude 54.364, Longitude -2.988) at deepest part of the lake; shore sampling when buoy access isn’t possible.
- Timeframe: data from January 2019 to end of 2020.

## Sampling regime and collection methods
- Fortnightly sampling as part of an ongoing long-term monitoring programme.
- Measurements taken from a boat at the buoy location; if unavailable, samples collected from shore.
- Data files include date, variable, and corresponding measurements for each sample.

## Data quality and limitations
- Data are raw and have not yet undergone quality control or calibration.
- Double entered and visually checked for accuracy.
- Missing data attributable to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.
- Some samples flagged as shore samples (Flag 2) when buoy sampling was not possible.
- Detection-limited values are indicated with a “<” sign in the Sign (if<LOD) column.

## Data structure and access
- Provided as a comma-separated values (CSV) file.
- Columns include:
  - Date
  - Description (variable name)
  - Variable (e.g., TEMP, OXYG, SECC, ALKA, etc.)
  - Value (measurements for each variable)
  - Sign (if values are below detection limit)
  - Flag (1 = buoy sample, 2 = shore sample)
- Clear definitions and descriptions accompany each variable and column.

## Use for monitoring and data management
- Supports consistent, long-term assessment of environmental health and policy performance.
- Follows standardised methods to enable comparability over time and with other datasets.
- Data structure facilitates verification, aggregation, and potential combination with related environmental datasets.
- Data management practices align with the aim of storing and making datasets accessible through appropriate data portals.

## Funding and acknowledgements
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 under the UK-SCAPE programme delivering National Capability.
- Data validation supported by NERC award NE/Y006208/1 under the ACCESS-UK programme delivering National Capability.