# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2023-2024)

- A meteorological dataset collected to support the ammonia enhancement experiment at the Glencorse woodland site, near UKCEH, Edinburgh.
- Extends earlier 2021-22 measurements from the same site.

## Location and data collection setup

- Site: Glencorse woodland, near the ammonia enhancement manifold (coordinates: 55.8539°, -3.2151°, altitude ~200 m).
- Instrumentation: a 16 m mast installed next to the ammonia enhancement infrastructure; measurements taken at multiple heights and with various sensor types.
- Measured domains include atmospheric variables near and below the canopy, soil properties, and radiation/wind metrics.

## Temporal coverage and sampling cadence

- Time period: 1 January 2023 to 31 December 2024.
- Data cadence: measurements every 20 seconds; 15-minute averages computed for analysis.
- Time zone: GMT (Greenwich Mean Time).

## Data content and structure

- Dataset size: 70,176 measurements covering 41 parameters.
- Delivery format: CSV file with a long-form column structure (e.g., Timestamp, Height (m), Instrument, Description, etc.) and per-parameter columns (e.g., Rain, Throughfall, Leaf Wetness Sensor readings, Air Temperature, Relative Humidity, Soil Volumetric Water Content and Temperature, Soil Electrical Conductivity, Wind Speed/Direction, PAR, Total Solar Radiation, and various WXT sensor readings).
- Key parameter groups and examples:
  - Weather and environmental: Rain, Throughfall, leaf wetness (LWS1–LWS4), air temperature (AirT1–AirT4) near and far from canopy, relative humidity (RH1–RH4).
  - Soil measurements: Soil_VWC1/2/3, Soil_EC1/2/3, Soil_T1/2/3 at near-surface to 15 cm depths.
  - Wind and atmosphere: Wind speed (WS_Cup1–WS_Cup4), wind direction (WXT_WD1–WXT_WD2), wind-related variables at below- and above-canopy levels, below- and above-canopy air temperature (WXT_AirT1–WXT_AirT2) and humidity (WXT_RH1–WXT_RH2), barometric pressure (WXT_BP1–WXT_BP2).
  - Radiation and light: Photosynthetically Active Radiation (PAR1, PAR2), Total Solar Radiation (Total_Solar1, Total_Solar2), both below- and above-canopy.
  - Other sensor strings: LWS (Leaf Wetness Sensor) at multiple heights; Rain sensors, Throughfall measurements; canopy- vs ground-layer context.
- Data structure notes: Each row is a 15-minute record with accompanying metadata columns (e.g., Timestamp, Height, Instrument, Description) and parameter-specific fields, enabling separation of measurements by height, sensor type, and location relative to canopy.

## Quality control and data quality

- Quality assurance: Visual checks performed; obvious instrument malfunctions, incorrect datalogger programming, and power-cut effects removed.
- Gaps: Some missing data occurred during sensor replacement and maintenance periods.

## Provenance, references, and funding

- This dataset is an extension of the 2021-22 site dataset (Deshpande et al., 2024b).
- Key references:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from an ammonia enhancement experiment site, Glencorse, 2021-2022, NERC EDS Environmental Information Data Centre.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).

## GIS-oriented notes and potential uses

- Suitable for creating time-enabled map visualizations of meteorological conditions at multiple canopy heights and soil depths.
- Can be joined with ammonia concentration/deposition data and with land-cover layers to analyze spatial-temporal patterns in deposition related to wind, canopy structure, and soil moisture.
- Useful for generating height-specific rasters or cross-sections showing above- vs below-canopy dynamics, as well as soil- and leaf-level microclimate analyses.
- Considerations for GIS work:
  - Align timestamps to GMT and handle 15-minute aggregation consistently.
  - Leverage the Height (m) field to analyze vertical structure; separate below-canopy and above-canopy sensors.
  - Prepare schema-aware joins due to the dense, long-form parameter schema (clarify instrument IDs, descriptions, and units).
- Caveats: Data gaps due to sensor maintenance; ensure documentation of missing periods during analyses.