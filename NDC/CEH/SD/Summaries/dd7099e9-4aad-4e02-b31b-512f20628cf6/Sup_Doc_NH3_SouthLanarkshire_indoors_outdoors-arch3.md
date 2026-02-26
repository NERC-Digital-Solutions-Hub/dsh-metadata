# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two sites in a rural area of South Lanarkshire: one indoors (hall of a dwelling) and one outdoors (garden of the same dwelling).
- Local site operator is the dwelling owner; analysis conducted by the Centre for Ecology and Hydrology Edinburgh.
- Ammonia (NH3) concentrations measured using CEH ALPHA® passive samplers in monthly exposure cycles starting at the beginning of each month.
- Site locations back onto grassland near a large dairy farm; indoor and outdoor measurements are paired for comparative assessment.

## Measurement Method
- Instrument: CEH ALPHA® passive sampler with citric acid coated filter to capture NH3; protective white PTFE membrane over the filter.
- Deployment: Replicate samplers mounted on a shelter on a pole at ~1.5 m above ground.
- Exposure: Monthly cycles; membrane facing downwards during exposure.
- Analysis: Exposed samplers extracted in deionised water; analysed by SEAL AA3 using colourimetry to determine ammonium concentration.
- Calculation: NH3 concentration in air derived from ammonium concentration using a known uptake rate of 0.003241315 m3 hr-1 and the exposure duration.
- Units: Reported as micrograms of NH3 per cubic meter of air (µg NH3 m-3).
- Data quality flags: Data flagged to indicate concerns; details provided in the data documentation (page 4).

## Data Handling and Quality Assurance
- Quality checks include:
  - Coefficient of variation (CV) of replicate samplers: CV < 15% considered valid; >15% triggers evaluation of replicate data and notes.
  - Some samples may be greater than the calibration range but deemed valid due to inability to rerun.
  - Missing data or metadata are indicated by -9999 in relevant fields.
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors.csv containing accepted data values, with appropriate flags.
- Data flags and status codes (including EMEP flags) accompany each record to indicate data capture quality, detection limits, and potential data issues.
- Dataset structure: Each row corresponds to one month of data for a single site, including site name, exposure period dates, ammonia concentration, and a data flag.

## Data Structure and Flags
- Columns include (examples):
  - Site name, unique site identifier, network id, parameter type, measurement start and end dates/times, NH3 concentration (µg NH3 m-3), detection-limit indicator, verification status, unit id, data capture percentage, validity flag, EMEP status.
  - Month-Year field indicates the exposure period (e.g., Jan-17).
- EMEP flags provide coded rationales for data status (e.g., contamination, detection limits, sampling issues, nearby influences, or valid observations despite issues).

## Site Information
- Indoor site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet above ground: 1.5 m
  - Details: Located in the hall of the dwelling
- Outdoor site:
  - Start date: 01/01/17; End date: Ongoing
  - Latitude: 55.64072; Longitude: 3.59705
  - Height of air inlet above ground: 1.5 m
  - Details: Located in the garden of the dwelling
- Both sites share the same general location coordinates and operational period, enabling indoor/outdoor comparison.