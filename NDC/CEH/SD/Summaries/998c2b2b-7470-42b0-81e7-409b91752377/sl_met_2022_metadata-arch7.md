# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (2022)

## Overview
- Time period: 17 March 2022 to 31 December 2022; data recorded in Sri Lanka Standard Time (SLST).
- Location: Queensberry Estate, Sri Lanka; mast near the ammonia enhancement manifold (coordinates 6.9693°, 80.5911°; altitude 1645 m).
- Data type: meteorological, soil moisture, soil temperature, soil electrical conductivity, leaf wetness, wind, and radiation measurements.
- Coverage: 27,812 measurements across 37 parameters; provided as a CSV file with 15-minute summaries (derived from measurements every 20 seconds).
- Purpose: wind conditions measured below the forest canopy to control the ammonia enhancement experiment; data linked to study by Deshpande et al. (2024).

## Data collection and structure
- Instrument setup:
  - Leaf Wetness Sensors (LWS1–LWS4) at heights 0.3 m, 2.0 m, 3.6 m, and 5.6 m.
  - Air temperature and relative humidity sensors at multiple heights (e.g., 0.2 m, 2.6 m, 5.5 m, 11.3 m) to represent under-canopy, ground flora, and canopy layers.
  - Soil measurements at three depths: near surface, ~10 cm, and ~15 cm (VWC, EC, T).
  - Wind, solar radiation, and photosynthetically active radiation (PAR) sensors at below- and above-canopy layers.
  - Pressure, wind speed/direction, and environmental sensors located at multiple heights.
- Data fields:
  - Timestamp, Height (m), Instrument, Description, and related metadata (Unit, Manufacturer).
  - Example parameter groups: AirT (temperature), RH (relative humidity), Soil_VWC/EC/T (soil volumetric water content, electrical conductivity, temperature), WS_Cup (wind near surface), PAR, Total_Solar, WXT (weather transmitters) measurements.
- Units and descriptors:
  - Air temperatures in °C; relative humidity in %; soil metrics in m3/m3, dS/m, and °C; wind in m/s; PAR in µmol m−2 s−1; solar radiation in W m−2; pressure in mbar.
- Data structure details:
  - Columns include 15-minute timestamps formatted as dd/mm/yyyy hh:mm; multi-height and multi-instrument records collected in a single CSV.

## Quality control
- Visual checks performed to remove obvious instrument errors due to malfunctions, datalogger issues, and power outages.
- Some data gaps remained due to sensor replacement and other interruptions.

## GIS and analysis considerations
- Spatial scope: single measurement site (point data) suitable for time-series visualization and integration with local GIS layers (topography, land cover, vegetation) for contextual analysis.
- Multi-layer temporal data: measurements across multiple vertical layers (ground to canopy) enable 3D or stratified analyses when combined with elevation and vegetation data.
- Temporal resolution: 15-minute intervals allow high-resolution temporal mapping and aggregation to hourly/daily scales.
- Data readiness: CSV format with comprehensive metadata; ensure data cleaning for any garbled fields or inconsistencies before GIS ingestion.
- Time zone consistency: all data in SLST; align with other datasets in the project as needed.

## Access, references, and funding
- Reference for methodology and broader findings: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024 Jan; doi:10.1016/j.atmosenv.2023.120325.
- Funding: UKRI GCRF South Asian Nitrogen Hub.