# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2021 - 2022

## Overview
- Fortnightly monitoring dataset from the South Basin of Windermere (Cumbria, England) covering Jan 2021–end of 2022.
- Variables captured: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH, ammonium (NH4N, µg N L−1), nitrate (NO3N, µg N L−1), soluble reactive phosphate (PO4P, µg P L−1), total phosphorus (TOTP, µg P L−1), dissolved reactive silicon (SIO2, µg L−1), phytoplankton chlorophyll a (TOCA, µg L−1).
- Data are raw at release (not yet quality controlled/calibrated) but double entered and visually checked.

## Sampling regime and collection methods
- Ongoing fortnightly sampling of surface water temperature, oxygen, Secchi depth, and water chemistry for the specified period.
- Water samples are integrated from 0 to 7 m.
- Measurements collected from a boat at the deepest lake location (buoy).

## Data structure and units
- Data provided as a comma-separated values (CSV) file with columns:
  - Date: date of measurement
  - Variable, Description: name and description of each variable (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value: numeric measurement for each variable
  - Sign(if<LOD), Description: indicates if a value is below detection limit with a < sign

- Units per variable:
  - TEMP: °C
  - OXYG: % air-saturation
  - SECC: m
  - ALKA: µg CaCO3 L−1
  - pH: dimensionless
  - NH4N: µg N L−1
  - NO3N: µg N L−1
  - PO4P: µg P L−1
  - TOTP: µg P L−1
  - SIO2: µg L−1
  - TOCA: µg L−1

## Quality control and limitations
- Data are raw and have not yet undergone quality control or calibration.
- Data validation has been performed via double entry and visual checks.
- Gaps/missing data attributed to weather, COVID-19 restrictions, or staff shortages.
- Some values may be below detection limits (indicated with < sign).

## Data provenance and funding
- Data collection supported by Natural Environment Research Council (NERC) grant NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Data validation supported by NERC grant NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability.

## Data availability and sharing
- Dataset provided in CSV format for download, with detailed column descriptions and unit definitions to support reuse and metadata documentation.