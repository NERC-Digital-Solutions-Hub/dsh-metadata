# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022

## Overview
- Long-term fortnightly monitoring dataset at Blelham Tarn, Cumbria, England.
- Time period: January 2021 to December 2022.
- Measures physical, chemical, and biological aspects of surface water quality.

## Variables and units
- TEMP: surface temperature, °C
- OXYG: surface oxygen saturation, % air-saturation
- SECC: Secchi depth, metres
- ALKA: alkalinity, µg CaCO3 per litre
- pH: pH (dimensionless)
- NH4N: ammonium, µg N per litre
- NO3N: nitrate, µg N per litre
- PO4P: soluble reactive phosphate, µg P per litre
- TOTP: total phosphorus, µg P per litre
- SIO2: dissolved reactive silicon, µg per litre
- TOCA: phytoplankton chlorophyll a, µg per litre

## Sampling regime and data collection
- Integrated water samples from 0 to 5 m; collected from a boat at the deepest part buoy.
- If buoy inaccessible, samples taken from shore (Flag 2).
- Fortnightly sampling; data available for download as CSV with fields Date, Variable, Value, Sign(if<LOD), Flag.

## Data quality and limitations
- Data are raw and not yet quality controlled/calibrated.
- Double entered and visually checked.
- Missing data due to weather, COVID-19 restrictions, or staff shortages.
- Values below detection limit indicated with a "<" in Sign(if<LOD).

## Data structure and accessibility
- CSV format with columns: Date, Description (variable), Value, Sign(if<LOD), Flag.
- Flag meanings: 1 = buoy location; 2 = shore location when buoy visit was not possible.

## Funding and provenance
- Data collection supported by Natural Environment Research Council (NE/R016429/1) as part of UK-SCaPE National Capability.
- Data validation supported by Natural Environment Research Council (NE/Y006208/1) as part of ACCESS-UK National Capability.

## Potential analyses and considerations for analysts
- Examine correlations across physical, chemical, and biological variables.
- Model relationships and trends using the 0–5 m integrated samples.
- Handle censored data using Sign(if<LOD) flags and Shore/Buoy Flags.
- Integrate with other long-term datasets while considering local site-specific conditions.
- Acknowledge the need for further QC/calibration before formal modelling.