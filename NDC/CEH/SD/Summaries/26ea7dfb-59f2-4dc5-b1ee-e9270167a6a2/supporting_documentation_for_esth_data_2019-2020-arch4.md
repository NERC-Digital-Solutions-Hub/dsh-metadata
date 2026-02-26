# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019  2020.

## Overview
- Ongoing long-term monitoring dataset from Esthwaite Tarn (Cumbria, England), with fortnightly sampling during 2019–2020.
- Measured parameters include: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA, µg per L).
- Water samples are integrated from 0 to 5 m; occasionally, when buoy sampling was not possible, samples were taken from the shore.
- Data are raw (not yet quality controlled/calibrated) but have been double entered and visually checked. Missing data are due to weather, lake access, COVID-19 restrictions, or staff shortages.
- Location: measurements from a boat at the buoy (Latitude 54.364, Longitude -2.988), at the deepest part of the lake. Jan 2019–Dec 2020.

## Sampling Regime and Collection Methods
- Fortnightly sampling as part of long-term monitoring.
- Water samples from 0–5 m integrated; if buoy visits were not possible, shore samples were collected.
- Measurements taken at buoy location (deepest part of the lake) when possible; otherwise shore samples used.
- Data timeframe: January 2019 to end of 2020.

## Quality Control
- Data are raw and have not undergone full quality control or calibration yet.
- Validation steps performed: double entry and visual checks.
- Missing values result from weather, access restrictions, COVID-19, or staff shortages.

## Data Structure and Content
- Data provided as a comma-separated values (CSV) file with columns including:
  - Date, Description (date of measurement)
  - Variable (TEMP, OXYG, SECC, ALKA, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA)
  - Value (numeric values for each variable)
  - Sign (if <LOD, indicates below detection limit)
  - Flag (1 = buoy sample; 2 = shore sample)
- Variables and units:
  - TEMP: temperature in °C
  - OXYG: oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per L
  - pH: pH (no unit specified)
  - NH4N: ammonium in µg N per L
  - NO3N: nitrate in µg N per L
  - PO4P: soluble reactive phosphate in µg P per L
  - TOTP: total phosphorus in µg P per L
  - SIO2: dissolved reactive silicon in µg SiO2 per L
  - TOCA: phytoplankton chlorophyll a in µg per L
- Flag meanings:
  - Flag = 1: sample taken on the lake at the marked buoy location
  - Flag = 2: sample taken from the shore due to inability to visit the buoy

## Data Availability and Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK National Capability).
- Data available to download as part of ongoing long-term monitoring.

## Notes for Data Leaders
- The dataset exemplifies a multi-parameter, long-term time series with clear provenance and collection metadata, suitable for system-level data governance, user needs alignment, and cross-network data integration.
- Documentation emphasizes raw data status and pending quality control, highlighting the importance of rigorous QC before broad dissemination or integration into decision-making workflows.
- Metadata includes collection location, depth integration, and sampling constraints, facilitating proper data discovery, lineage tracking, and reproducibility across data platforms.