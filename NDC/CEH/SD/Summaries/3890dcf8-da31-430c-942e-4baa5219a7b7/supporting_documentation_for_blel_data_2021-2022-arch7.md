# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2021 to 2022

## Overview
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England.
- Fortnightly sampling from January 2021 to December 2022.
- Measured: surface temperature, surface oxygen, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.

## Data content and structure
- Variables and units:
  - TEMP: surface temperature (°C)
  - OXYG: surface oxygen saturation (% air-saturation)
  - SECC: Secchi depth (m)
  - ALKA: alkalinity (µg CaCO3 per L)
  - pH: pH
  - NH4N: ammonium (µg N per L)
  - NO3N: nitrate (µg N per L)
  - PO4P: soluble reactive phosphate (µg P per L)
  - TOTP: total phosphorus (µg P per L)
  - SIO2: dissolved reactive silicon (µg per L)
  - TOCA: phytoplankton chlorophyll a (µg per L)
- Data columns in CSV:
  - Date, Variable, Value, Sign(if<LOD), Flag
- Special indicators:
  - Sign(if<LOD) uses "<" to denote below detection limit.
  - Flag: 1 = sample at buoy (lake location), 2 = shore sample (buoy visit not possible).
- Sampling scope:
  - Water samples integrated from 0–5 m depth; measurements mainly taken from the buoy at the deepest part of the lake; shore samples used when buoy access was not possible.

## Sampling regime and spatial aspects
- Sampling location primarily at a marked buoy; occasional shore sampling when buoy access is not possible.
- Water samples are integrated from 0–5 m depth.
- Fortnightly cadence provides regular temporal coverage suitable for time-series mapping and trend analysis.

## Data quality and limitations
- Data are raw and not yet quality controlled or calibrated.
- Data have been double-entered and visually checked.
- Gaps/missing data due to weather, COVID-19 restrictions, or staff shortages.
- Some measurements are below detection limits (indicated by the < sign).

## GIS readiness and usage guidance
- Not immediately GIS-ready; requires cleaning and restructuring to map variables over time.
- Suggested steps for GIS workflows:
  - Convert to tidy format and standardize units if needed.
  - Create spatial points for buoy location and, where applicable, shore sampling coordinates.
  - Build time-enabled layers for each variable (or a multi-parameter layer with filters by variable).
  - Handle detection-limit indicators (<) and sampling flags (1 or 2) in attribute fields.
  - Integrate with other lake-geography datasets (basemaps, catchment boundaries).
- Data can feed map-based visualizations of spatial-temporal trends (e.g., surface temperature, oxygen, chlorophyll a) and support policy or public-facing dashboards after QA/QC.

## Provenance and funding
- Data collection supported by Natural Environment Research Council (NERC) awards NE/R016429/1 (UK-SCaPE) and NE/Y006208/1 (ACCESS-UK) as part of National Capability.
- The dataset presented here forms part of an ongoing monitoring program.