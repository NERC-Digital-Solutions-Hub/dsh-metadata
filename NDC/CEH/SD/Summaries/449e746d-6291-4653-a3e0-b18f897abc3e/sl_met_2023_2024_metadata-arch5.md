# Meteorological data from Queensberry ammonia enhancement site in Sri Lanka (20232024)

## Overview
- Meteorological dataset collected to support ammonia enhancement experiments at the Queensberry Estate, Sri Lanka.
- Extends the 2022 dataset from the same site; dataset supports analysis of wind-controlled NH3 enhancement and related atmospheric processes.
- Timeframe: 1 January 2023 to 31 December 2024; data are provided in Sri Lanka Standard Time (SLST).

## Site, Instrumentation, and Data Collection
- Location: Queensberry Estate, Sri Lanka (6.9693° N, 80.5911° E; altitude 1645 m); mast extends 12 m, 5 m above canopy.
- Measurements include:
  - Atmospheric: air temperature, relative humidity, leaf wetness at four heights; wind speed, wind direction; barometric pressure; photosynthetically active radiation (PAR) and total solar radiation (below and above canopy).
  - Soil: volumetric water content (three depths), electrical conductivity, and temperature (three depths).
  - Wind and radiation sensors positioned near and above/below canopy.
- Sampling: data collected every 20 seconds; 15-minute averages computed; dataset covers 70,176 measurements across 37 parameters.
- Instrument types and positioning referenced (e.g., Vaisala HMP60; METER Environment leaf wetness sensors; HS Hyquest Solutions rainfall sensor; Vector Instruments anemometers; Skye Instruments PAR and solar sensors).
- Data description notes include that wind conditions below canopy influence the ammonia enhancement experiment.

## Quality Control and Data Cleaning
- Visual quality checks performed; obvious instrument malfunctions, datalogger programming errors, and power-cut artifacts removed.
- Gaps occur due to sensor replacements; step changes in leaf wetness measurements attributed to sensor baselines and replacement events.
- Dataset notes emphasize that sharing should respect data availability and any embargoes or proprietary constraints.

## Data Structure and File Format
- Format: CSV with 70,176 rows and 37 parameters.
- Core fields include:
  - Timestamp, Height (m), Manufacturer, Instrument, Description.
  - Parameters such as Rain, Throughfall, Leaf Wetness Sensor (LWS1–LWS4), AirT (Air Temperature; multiple depths/heights), RH (Relative Humidity; multiple layers), Soil_VWC, Soil_EC, Soil_T, WS (Wind Speed), PAR, Total_Solar, WXT_WS/WXT_WD/WXT_BP (wind, direction, barometric pressure) across below- and above-canopy contexts.
- Example row metadata indicates multi-sensor provenance and detailed descriptor text for each parameter.
- Timezone: SLST; timestamps aligned to 15-minute intervals.

## Provenance, References, and Funding
- Related publications for full methodology and results:
  - Deshpande et al. (2024a): Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments, Atmos. Environ.
  - Deshpande et al. (2024b): Meteorological data and ammonia concentration and deposition rates from Queensberry, Sri Lanka, 2022, NERC EDS Environmental Information Data Centre.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) supported facility establishment.

## Access, Licensing, and Reuse
- Data and full metadata available via the NERC EDS Environmental Information Data Centre (reference: Deshpande et al., 2024b; DOI provided in the associated record).
- The 2024a/2024b references provide the complete methodology and deposition rate analyses; use of dataset should acknowledge these sources and the funding body.

## Data Stewardship Considerations
- Governance and accessibility:
  - Dataset designed for interoperable, multi-parameter meteorological records; metadata-rich with instrument details, locations, and processing steps.
  - Ensure continued updates and documentation align with ongoing ammonia enhancement experiments.
- Metadata and standards:
  - Maintain consistent unit conventions, height descriptors, and sensor metadata to support cross-year comparisons.
  - Record any re-calibration, sensor replacements, or methodological changes that affect baseline values (noting leaf wetness baseline shifts).
- Interoperability and legacy data:
  - The dataset is an extension of 2022 measurements; maintain clear versioning and change logs to support longitudinal analyses.
  - Consider harmonizing field names and descriptions with other site datasets to facilitate data integration.
- Practical considerations:
  - Gaps due to maintenance and replacements should be documented and, where possible, annotated with reasons and timestamps.
  - Data use should respect any sharing restrictions or embargoes and reference the primary publications for full methodological context.