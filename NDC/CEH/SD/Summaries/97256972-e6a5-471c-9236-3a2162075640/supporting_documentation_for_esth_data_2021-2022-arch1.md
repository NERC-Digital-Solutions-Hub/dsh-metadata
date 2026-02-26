# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022

## Overview
- Long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling across 2021–2022.
- Variables include surface temperature, surface oxygen, Secchi depth, alkalinity, pH, and nutrients, plus phytoplankton chlorophyll a.
- Data collected to support analyses of limnology and ecological status.

## Data Collected and Units
- Temperature (TEMP): degrees Celsius (°C).
- Surface oxygen saturation (OXYG): percent air-saturation (%).
- Secchi depth (SECC): metres (m).
- Alkalinity (ALKA): micrograms per litre as CaCO3 (µg CaCO3 L⁻¹).
- pH: no unit specified (pH unitless).
- Ammonium (NH4N): µg N L⁻¹.
- Nitrate (NO3N): µg N L⁻¹.
- Soluble reactive phosphate (PO4P): µg P L⁻¹.
- Total phosphorus (TOTP): µg P L⁻¹.
- Dissolved reactive silicon (SIO2): µg SiO2 L⁻¹.
- Phytoplankton chlorophyll a (TOCA): µg L⁻¹.
- Water samples integrated from 0 to 5 m; measurements taken from a boat at the deepest part of the lake; alternatives from shore when buoy access was not possible.

## Sampling Regime and Collection Methods
- Fortnightly sampling schedule.
- Primary sampling location: buoy at the marked location; when inaccessible, sampling from the shore.
- Timeframe: January 2021 through the end of 2022.
- Data describe surface layer measurements and integrated 0–5 m water chemistry.

## Data Structure
- Data delivered as comma-separated values (CSV).
- Columns:
  - Date: measurement date.
  - Variable, Description: name and description of the measured variable (the listed variables above).
  - Value, Description: numeric measurement for each variable.
  - Sign(if<LOD), Description: indicates if the value is below the detection limit (a "<" sign if applicable).
  - Flag, Description: 1 = sample from buoy; 2 = sample from shore (buoy visit not possible).

## Quality Control and Uncertainty
- Data are raw and not yet quality controlled or calibrated.
- Double entered and visually checked.
- Missing data caused by weather, lake access restrictions, COVID-19 restrictions, or staff shortages.
- Detection-limit indicators present where applicable.
- Sampling method notes (buoy vs shore) help interpret potential spatial variability.

## Data Availability and Access
- Provided as downloadable CSV with explicit metadata and column descriptions.
- Includes details to enable tracking of data provenance and integration with other datasets.

## Funding and Support
- Data collection funded by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Data validation funded by NERC award NE/Y006208/1 as part of the ACCESS-UK programme delivering National Capability.