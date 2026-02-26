# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022

## Overview
- Ongoing long-term monitoring dataset with fortnightly sampling at Blelham Tarn, Cumbria, England.
- Data available to download cover: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Timeframe: January 2021 to end of 2022.
- Sampling regime: integrated water samples from 0–5 m; when buoy sampling was not possible, samples taken from the shore (Flag 2).
- Data are raw and not yet quality controlled or calibrated; double entered and visually checked; missing data due to weather, COVID-19 restrictions, or staff shortages.

## Data structure and accessibility
- Format: comma separated values (CSV) with columns:
  - Date: measurement date
  - Variable: description of the measurement (one of TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: measured value
  - Sign(if<LOD): indicates if value is below detection limit (a "<" sign)
  - Flag: 1 = buoy location; 2 = shore sampling
- Data are organized per measurement date and variable, enabling cross-variable time-series analyses.

## Variables and units
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

## Data quality and limitations
- RAW data, not yet quality controlled or calibrated.
- Missing data linked to weather, COVID restrictions, or staff shortages.
- Sampling method differences: buoy-based integration vs shore sampling (Flag 2) may affect comparability; use Flag to identify shore samples.

## Practical use guidance for data exploration
- Align datasets by Date for multi-variable time-series analyses.
- Treat values with Sign(<LOD) appropriately (below detection limit handling).
- Separate analyses by sampling location (Flag 1 buoy vs Flag 2 shore) or apply consistent handling if combining.
- Use the dataset to explore temporal trends, seasonal patterns, and relationships between physical, chemical, and biological parameters.
- Suitable for creating dashboards or self-serve reports to monitor lake conditions over 2021–2022.

## Funding
- Data collection: Natural Environment Research Council award NE/R016429/1 (UK-SCaPE programme, National Capability).
- Data validation: Natural Environment Research Council award NE/Y006208/1 (ACCESS-UK programme, National Capability).