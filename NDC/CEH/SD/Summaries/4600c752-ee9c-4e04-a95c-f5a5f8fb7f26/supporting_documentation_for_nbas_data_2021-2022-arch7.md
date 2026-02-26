# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2021 -2022

## Overview
- Ongoing fortnightly monitoring dataset from Windermere North Basin, Cumbria, England (Jan 2021 – end 2022).
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), phytoplankton chlorophyll a (TOCA, µg per L).
- Sampling method: integrated water samples from 0–7 m collected from a boat at a buoy located at the deepest part of the lake.
- Location-based data suitable for GIS map-based visualisations and temporal analyses.

## Sampling regime and collection methods
- Sampling frequency: fortnightly.
- Sampling scope: surface measurements and water chemistry plus phytoplankton chlorophyll a.
- Data describe measurements taken at a single location (windermere North Basin buoy) over time (Jan 2021–2022).

## Data structure and content
- Data format: CSV file with columns:
  - Date: date of measurement.
  - Variable, Description: name and description of each measured variable (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value, Description: measured value for each variable.
  - Sign(if<LOD), Description: indicates if the value is below the detection limit (a < symbol is used).
- Measurement details:
  - TEMP: surface temperature in degrees Celsius.
  - OXYG: surface oxygen saturation in % air-saturation.
  - SECC: Secchi depth in metres.
  - ALKA: alkalinity in µg CaCO3 per litre.
  - pH: pH value (dimensionless).
  - NH4N: ammonium in µg N per litre.
  - NO3N: nitrate in µg N per litre.
  - PO4P: soluble reactive phosphate in µg P per litre.
  - TOTP: total phosphorus in µg P per litre.
  - SIO2: dissolved reactive silicon in µg per litre.
  - TOCA: phytoplankton chlorophyll a in µg per litre.
- Data availability note: raw data, not yet quality controlled or calibrated; double-entered and visually checked.
- Gaps: missing data due to weather, COVID-19 restrictions, or staff shortages.

## Quality control and limitations
- Data are raw and have not undergone full quality control or calibration.
- Validation and data integrity steps include double-entry and visual checks.
- Missing data attributed to external factors (weather, COVID-19, staff availability).

## Data provenance and funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme, National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK programme, National Capability).
- Part of a sustained monitoring program; dataset designed to support GIS-based analysis and integration with broader environmental datasets.