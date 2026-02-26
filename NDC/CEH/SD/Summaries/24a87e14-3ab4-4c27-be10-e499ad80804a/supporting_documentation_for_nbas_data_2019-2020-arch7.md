# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2019  - 2020.

- Overview
  - Fortnightly monitoring dataset from Windermere North Basin (Cumbria, England) covering January 2019 to end of 2020.
  - Variables include surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
  - Water samples are integrated from 0 to 7 m depth.
  - Units: TEMP (°C), OXYG (% air-saturation), SECC (m), ALKA (µg/L as CaCO3), pH (unitless), NH4N/NO3N/PO4P/TOTP/SIO2/TOCA (µg/L), with < signs indicating values below detection limits for Sign (if<LOD).

- Sampling regime
  - Sampling conducted from a boat at a buoy location (Latitude 54.397, Longitude -2.952) at the deepest part of Windermere North Basin.
  - Sampling cadence: every two weeks (fortnightly).

- Data quality and caveats
  - Data are raw and not yet quality controlled or calibrated.
  - Double-entered and visually checked; remaining gaps due to weather, COVID-19 restrictions, or staff shortages.

- Data structure and format
  - Provided as comma-separated values (CSV).
  - Columns include: Date, Variable (e.g., TEMP, OXYG, SECC, ALKA, pH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA), Description for each variable, Value, and Sign (if<LOD) indicating below-detection-limit values.
  - The dataset is organized to support GIS use, with a single sampling point (the buoy) and time-stamped measurements for multiple variables.

- Spatial and temporal context
  - Spatial: Windermere North Basin, Cumbria, England; sampling location fixed at the buoy site.
  - Temporal: Jan 2019 – 2020 (end), with fortnightly measurements.

- Intended GIS use and considerations
  - Suitable for creating time-enabled map visualisations at a fixed lake buoy point or for joining with other spatial data layers (e.g., lake basins, bathymetry).
  - Because the data are raw, users may need to apply quality control and calibration steps before analysis.
  - The presence of a “Sign (if<LOD)” column enables handling of censored data in GIS analyses.

- Data availability and funding
  - Funding for data collection: Natural Environment Research Council (NE/R016429/1) under the UK-SCAPE programme (National Capability).
  - Data validation support: Natural Environment Research Council (NE/Y006208/1) under the ACCESS-UK programme (National Capability).