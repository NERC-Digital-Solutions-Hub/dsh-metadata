# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2019  2020

## Overview
- Part of an ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England, with fortnightly sampling.
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 per L), pH, ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg SiO2/L), and phytoplankton chlorophyll a (TOCA, µg/L).
- Timeframe: January 2019 – end of 2020.
- Location and sampling: measurements from a boat at the buoy (Latitude 54.364, Longitude -2.988) at the deepest part of Esthwaite Water; when the buoy wasn’t accessible, shore samples were taken.
- Water samples are integrated from 0 to 5 m.

## Sampling regime and collection methods
- Fortnightly sampling cadence.
- Measurements taken from the buoy location when possible; shore sampling used as an alternative if visits to the buoy were not possible.
- All listed variables provided with corresponding units as described.

## Data quality and limitations
- Data are raw and have not yet undergone quality control or calibration.
- Data have been double-entered and visually checked.
- Missing data attributed to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.
- Detection limit issues indicated where values fall below detection (Sign (if<LOD) column).

## Data structure and fields
- Format: comma-separated values (CSV).
- Core variables (with units): TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3/L), pH (unitless), NH4N (µg N/L), NO3N (µg N/L), PO4P (µg P/L), TOTP (µg P/L), SIO2 (µg SiO2/L), TOCA (µg/L).
- Columns include: Date, Variable/Description, Value, Sign (if<LOD), and Flag.
- Flags: Flag = 1 indicates buoy-based lake sample; Flag = 2 indicates shore sample due to buoy access issues.

## Data availability and access
- Data provided as a CSV file for download; currently raw data with no QC/calibration performed yet.
- Acknowledges data has been visually checked and double-entered; remaining quality control steps are expected to occur subsequently.

## Practical considerations for data support and use
- Prepare for post-collection QC/calibration and harmonisation across the two-year span.
- Manage patchy data due to weather, access, and disruptions; use the Flag field to distinguish sampling provenance (buoy vs shore).
- Ensure proper handling of <LOD values via the Sign (if<LOD) field during analysis.
- Potential data products: time-series dashboards, cross-variable analyses, and self-serve exploration of long-term water quality and phytoplankton indicators.

## Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCAPE programme delivering National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK programme delivering National Capability).