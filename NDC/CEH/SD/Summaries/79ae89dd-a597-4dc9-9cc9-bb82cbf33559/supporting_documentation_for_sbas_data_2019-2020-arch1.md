# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2019 to 2020

## Overview
- Ongoing fortnightly monitoring dataset for the South Basin of Windermere, Cumbria, England.
- Timeframe: January 2019 to December 2020.
- Parameters measured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH; nutrients and pigments: ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).

## Sampling regime and data scope
- Sampling frequency: fortnightly.
- Sampling location: boat measurements at the deepest part of the lake, using a marked buoy.
- Depth integration: 0–7 m for water samples.
- Data are raw and not yet quality controlled or calibrated.

## Data variables and units
- TEMP: surface temperature, °C.
- OXYG: surface oxygen saturation, % air-saturation.
- SECC: Secchi depth, m.
- ALKA: alkalinity, µg CaCO3 per L.
- pH: pH units.
- NH4N: ammonium, µg N per L.
- NO3N: nitrate, µg N per L.
- PO4P: soluble reactive phosphate, µg P per L.
- TOTP: total phosphorus, µg P per L.
- SIO2: dissolved reactive silicon, µg per L.
- TOCA: phytoplankton chlorophyll a, µg per L.
- Note: Some values may be below detection limit, indicated by a < sign in the Sign (if<LOD) column.

## Data quality and limitations
- Raw data; not yet quality controlled or calibrated.
- Data have undergone double-entry and visual checks.
- Missing data attributed to weather, COVID-19 restrictions, or staff shortages.
- Detection-limit considerations captured via a Sign (if<LOD) flag.

## Data structure and access
- Data provided as a comma-separated values (CSV) file.
- Columns: Date, Description (variable), Value, Sign (if<LOD).
- Descriptions correspond to the variables listed above.
- Data intended to be downloadable; includes metadata indicating measurement context and units.

## Data provenance and funding
- Collected under the UK-SCaPE National Capability program.
- Funded by Natural Environment Research Council award NE/R016429/1.

## Usage considerations for analysts
- Suitable for examining correlations and building predictive models across physical, chemical, and biological parameters in a freshwater system.
- Useful for assessing how surface conditions relate to nutrient status and phytoplankton chlorophyll a within the 0–7 m depth range.
- Analyses should account for:
  - Raw (unQCed) status; plan for quality control and calibration.
  - Fortnightly cadence and potential gaps due to weather or access issues.
  - Detection-limit flags for low-concentration measurements.
  - Spatial scope limited to the South Basin of Windermere; results may not generalize to other basins without additional data.
- Datasets may be combined with other environmental or meteorological data, subject to data access and format compatibility.