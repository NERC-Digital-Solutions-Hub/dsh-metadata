# Sup_Doc_NH3_SouthLanarkshire_indoors&outdoors

## Overview
- Data from two sites in rural South Lanarkshire: indoor hall of a dwelling and outdoor garden area backing onto grassland of a large dairy farm.
- Analysis conducted by the Centre for Ecology and Hydrology (CEH) Edinburgh.
- Purpose: measure ammonia (NH3) in air using CEH ALPHA passive samplers, with monthly exposure cycles since 2017.
- Outputs are prepared for end-user use (e.g., dashboards, reports) with data quality flags and metadata.

## Sampling Method
- Instrument: CEH ALPHA® passive samplers with citric acid coated filters to capture NH3; protected by a white PTFE membrane facing downward.
- Deployment: replicate samplers attached to a shelter on a pole at ~1.5 m above ground; both indoor and outdoor locations operated as replicates for reliability.
- Exposure: monthly cycles at the start of each month.

## Analysis and Calculation
- Laboratory analysis: exposed samplers extracted into deionised water and analyzed by SEAL AA3 using colorimetry to determine ammonium concentration.
- Conversion: sampler ammonium concentration converted to average NH3 concentration in air using a known uptake rate of 0.003241315 m3 hr-1 and exposure duration.
- Data handling: raw data quality-checked and flagged as described below; final dataset contains accepted values with data flags.

## Data Structure and Dataset
- Final dataset: NH3_SouthLanarkshire_indoors_outdoors.csv.
- Each row represents one month of data for a single site, including:
  - Site name, network_id, parameter_id
  - Measurement start/end dates and times (exposure period)
  - Ammonia concentration (units: µg NH3 m-3)
  - Data flags and related metadata (e.g., less-than detection, verification status, unit code, data capture percentage, validity)
  - Month-Year label (MMM-YY)
- Data fields include: site identification, dates/times, concentration, detection-limit indicators, verification status, data capture percentage, EMEP flag statuses, and a final validity indicator.

## Quality Control and Validity
- Quality checks for data validity:
  - CV of replicate ALPHA samplers must be < 15% for data to be considered valid (flagged as 103 when acceptable).
  - Data exceeding calibration range may be reported as valid if re-run is not possible.
  - Missing data are indicated by -9999 in concentration or metadata fields.
- Final dataset marks each record with a validity flag (1 = valid, -1 = not valid) and includes EMEP status codes describing data status and quality issues.
- EMEP flags provide detailed reasoning for data capture and validity decisions (e.g., detection limits, contamination, sampling conditions, or proximity influences).

## Site Information
- Indoor site: located inside the hall of the dwelling; start date 01/01/17; End date: Ongoing; coordinates 55.64072, -3.59705; air-inlet height 1.5 m.
- Outdoor site: located in the garden of the dwelling; start date 01/01/17; End date: Ongoing; coordinates 55.64072, -3.59705; air-inlet height 1.5 m.
- Both sites share the same coordinates, with the indoor site described as inside the dwelling hall and the outdoor site described as the garden area adjacent to the dwelling.

## Data Availability and Notes
- Raw data have been examined and quality-assessed against the described rules; the final dataset contains accepted values with appropriate flags.
- Documentation includes detailed column descriptions, site identifiers, and metadata to support data provenance and reuse.
- The dataset supports monthly temporal analysis of NH3 air concentrations at two proximate locations with replicates to enhance reliability.