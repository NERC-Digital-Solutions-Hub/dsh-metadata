# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022

## Overview
- Ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England, collected fortnightly from January 2021 to end-2022.
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N per L), nitrate (NO3N, µg N per L), soluble reactive phosphate (PO4P, µg P per L), total phosphorus (TOTP, µg P per L), dissolved reactive silicon (SIO2, µg per L), and phytoplankton chlorophyll a (TOCA, µg per L).
- Data are raw and not yet quality controlled or calibrated; double entered and visually checked.

## Sampling regime and collection methods
- Fortnightly sampling from Esthwaite Tarn; water samples integrated from 0–5 m depth.
- Measurements taken from a boat at the deepest part of the lake (buoy). If buoy access was not possible, samples collected from the shore.
- Data cover January 2021 through end of 2022.

## Data structure and file format
- Provided as comma-separated values (CSV).
- Columns include:
  - Date: measurement date
  - Variable, Description: name and description of each measured parameter
  - Value, Description: measured values
  - Sign(if<LOD): indicates values below detection limit with a “<” sign
  - Flag, Description: 1 = sampled at buoy; 2 = sampled from shore when buoy visit was not possible

## Variables, units, and notes
- TEMP: degree Celsius
- OXYG: % air-saturation
- SECC: metres
- ALKA: µg CaCO3 per litre
- pH: unitless
- NH4N: µg N per litre
- NO3N: µg N per litre
- PO4P: µg P per litre
- TOTP: µg P per litre
- SIO2: µg per litre
- TOCA: µg per litre
- Notes: some values below detection limit are marked with “<”; sampling sometimes not integrated (Flag 2).

## Quality control and data validity
- Raw data not yet quality controlled or calibration-adjusted.
- Quality assurance performed via double entry and visual checks.
- Missing data attributable to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.

## Data availability and access
- Dataset available for download as a CSV file with clearly defined fields, units, and flag indicators.
- Documentation includes data provenance, sampling regime, and data structure to aid discovery and reuse.

## Provenance and funding
- Data collection funded by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE programme, National Capability).
- Data validation funded by NERC award NE/Y006208/1 (ACCESS-UK programme, National Capability).