# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2019 to 2020. Feuchtmayr, H., Clarke, M.A., De Ville, M.M., Dodd, B.A., Guyatt, H., Hunt, A.G., James, J.B., Mackay, E.B., McShane, G., Rhodes, G., Thackeray, S.J., Maberly, S.C. (2024)

## Overview
- Long-term, fortnightly monitoring dataset from Blelham Tarn, Cumbria, England.
- Measures surface temperature, surface oxygen, water clarity, water chemistry, and phytoplankton chlorophyll a (2019–2020).

## What the data contain
- Variables (with units):
  - TEMP: surface temperature, °C
  - OXYG: surface oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 per L
  - pH: pH
  - NH4N: ammonium, µg N per L
  - NO3N: nitrate, µg N per L
  - PO4P: soluble reactive phosphate, µg P per L
  - TOTP: total phosphorus, µg P per L
  - SIO2: dissolved reactive silicon, µg per L
  - TOCA: phytoplankton chlorophyll a, µg per L
- Data are provided as a CSV with columns:
  - Date, Variable, Value, Sign (if <LOD), Flag (sampling location)

## Sampling regime and collection methods
- Part of ongoing long-term monitoring; fortnightly sampling from Jan 2019 to end of 2020.
- Water samples integrated from 0–5 m depth.
- Measurements taken from a boat at the buoy at the lake’s deepest point; when inaccessible, shore samples were collected.
- Flag meanings:
  - Flag 1: sample taken at the buoy (lake location)
  - Flag 2: sample taken from shore (buoy visit not possible)

## Data structure
- Date: measurement date
- Variable: variable name (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
- Value: measured value
- Sign: indicates if value is below detection limit (<LOD)
- Flag: sampling location indicator (1 or 2)

## Quality control
- Data are raw and not yet quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Missing data attributed to weather, COVID-19 restrictions, or staff shortages.

## Temporal and spatial coverage
- Temporal: January 2019 to December 2020 (fortnightly measurements)
- Spatial: primarily a single fixed buoy location at the deepest part of Blelham Tarn; some shore samples when buoy access was not possible

## Data availability and access
- Data available to download as a CSV file with the described structure and variables.

## Limitations and considerations for GIS use
- Spatial scope is largely a single lake location; combining with other spatial datasets may require careful alignment of the buoy location with lake maps.
- Data are raw and may require quality control/calibration before high-precision GIS analyses.
- Detection-limit indicators are provided in the Sign column for below-LOD values.

## Funding
- Data collection supported by Natural Environment Research Council, award NE/R016429/1, as part of the UK-SCaPE programme delivering National Capability.