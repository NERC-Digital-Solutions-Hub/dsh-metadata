# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2021 -2022.

## Overview
- Part of an ongoing long-term monitoring dataset from Esthwaite Tarn, Cumbria, England.
- Fortnightly sampling conducted in 2021–2022.
- Variables included: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH, ammonium (NH4N, µg N/L), nitrate (NO3N, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), phytoplankton chlorophyll a (TOCA, µg/L).

## Sampling regime and collection methods
- Water samples are integrated from 0 to 5 m depth.
- Measurements collected from a boat at a buoy located at the deepest part of the lake; when not possible, samples from the shore were collected during visits.
- If shore sampling occurred, water samples were not integrated (Flag 2).
- Sampling period covers January 2021 through end of 2022.

## Data structure and file format
- Data provided as a comma-separated values (CSV) file with:
  - Date: measurement date.
  - Variable: name of the measured variable (TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - Value: measured value for each variable.
  - Sign(if<LOD): indicates if the value is below the detection limit (<).
  - Flag: 1 = sample taken at buoy location; 2 = sample taken from shore.
- Units: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg CaCO3/L), pH (unitless), NH4N/NO3N/PO4P/TOTP/SIO2/TOCA (various µg/L or µg P/L as specified).

## Quality control and limitations
- Data are raw and not yet quality controlled or calibrated.
- Data validation performed via double entry and visual checks.
- Missing data attributed to weather, lake access restrictions, COVID-19 restrictions, or staff shortages.

## Spatial and temporal coverage
- Location: fixed at buoy at the deepest part of Esthwaite Water (with occasional shore sampling).
- Temporal coverage: January 2021 – December 2022, with fortnightly sampling cadence (approximately 26 samples per year).

## Considerations for GIS and map-based data products
- The dataset is suitable for time-series and spatial visualization at a fixed monitoring station; may require georeferencing of buoy/shore locations for mapping.
- Prepare QA/QC steps before GIS use due to raw data status and detection-limit indicators.
- Handle detection-limit signs (<) appropriately when mapping or performing analyses.
- When combining multiple variables, consider restructuring the CSV into separate layers or time-series tables per variable for efficient GIS integration.
- Be mindful of the distinction between buoy (Flag 1) and shore (Flag 2) samples when assessing spatial accuracy.

## Funding and provenance
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 (UK-SCaPE, delivering National Capability).
- Data validation supported by NERC award NE/Y006208/1 (ACCESS-UK, delivering National Capability).