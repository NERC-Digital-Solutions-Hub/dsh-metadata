# The EMEP-WRF global model, version 4.45

## Overview
- A global chemical transport modeling framework combining the EMEP-WRF (Weather Research and Forecasting) setup with emissions data to simulate surface ozone.
- Based on the EMEP MSC-W model; WRF provides hourly 3D meteorology driving the simulations.
- Global domain at 1° x 1° resolution with 21 vertical layers (surface ~40 m to ~2 km top).
- Meteorology driven by hourly nudged GFS-FNL data; emissions from IIASA ECLIPSE v6a GAINS for 2015.
- Outputs daily mean surface ozone (6:00–18:00 local time) on a 1° grid; seasonal averages computed for the grassland growing season (mid-April to mid-July) for the UK and the USA in 2018.

## Data specifics
- Grid and timing: 1° x 1° grid; period 2018; growing-season window mid-April to mid-July; UK and USA focus.
- Variable and units: daily surface ozone concentration in parts per billion (ppb); seasonal mean values for the defined window.
- Coordinate system: Geographic Coordinate System WGS 1984; units in decimal degrees.
- Output example: seasonal mean O3_ppb per grid cell, with values ranging from 19.3 ppb to 50.9 ppb.

## Data quality and validation
- Quality assurance/quality control applied prior to analysis.
- Model validation referenced from Mills et al. (2018): comparison of model output with Global Atmosphere Watch (GAW) observations to assess performance during daily ozone peaks.
- Demonstrates the model’s ability to reproduce spatial and temporal patterns, including seasonal highs and ozone episodes.

## Data structure
- Shapefile with 1° x 1° grid cells and 5 attributes:
  - FID: Unique grid cell identifier.
  - Lon: Center longitude (decimal degrees).
  - Lat: Center latitude (decimal degrees).
  - NAME: Country designation (USA or UK).
  - O3_ppb: Daily surface ozone concentration in ppb, seasonal mean for mid-April to mid-July 2018.
- Data range: O3_ppb values between 19.3 ppb and 50.9 ppb.

## Context and references
- Key sources and related work:
  - Mills et al. (2018): model validation against GAW data and ozone dynamics.
  - Simpson et al. (2012): technical description of the EMEP MSC-W model.
  - Vieno et al. (2016): sensitivities of emissions reductions for UK PM2.5 (contextual methodological reference).

## Relevance for Analysts Monitoring the Environment
- Delivers a standardized, comparable dataset of ozone for cross-temporal and cross-regional monitoring.
- Outputs are ready for visualization (maps, charts) and further analysis, aligning with standardized monitoring practices.
- Facilitates data integration by providing a clearly defined, QA/QC’d ozone dataset that can be combined with other environmental indicators to enhance policy performance assessments.
- Addresses common challenges by enabling data reuse (beyond single-use applications) and supporting access to underlying data through structured formats and metadata.