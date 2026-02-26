# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Purpose: Report initial results from a study to determine the uptake rate for CEH ALPHA® samplers used to measure ammonia (NH3) concentrations in air, in the UK and similar climates.
- Collaboration: Sampling conducted by UK CEH Edinburgh and AFBI Hillsborough; analysis by CEH Edinburgh.
- Sampling cadence: Samplers exposed in monthly cycles at the beginning of each month.
- Year focus: Data from the first year not used for uptake rate calibration due to COVID-19-related data losses and insufficient calibration points.
- Data product: Final dataset NH3_Edinburgh_Uptake_Rate_2020.csv containing monthly NH3 concentration data per site.
- Units: NH3 concentration in air expressed as micrograms per cubic metre (µg NH3 m-3).

## Sampler Method
- Device: CEH ALPHA® passive sampler with a citric acid coated filter to capture NH3; protected by a white PTFE membrane and a down-facing orientation during exposure.
- Deployment: Replicate samplers mounted on a shelter on a pole at approximately 1.5 m above ground; protection container provided for transport/storage.
- Analysis workflow: Exposed samplers are extracted into deionised water, analysed by SEAL AA3 using colorimetry to determine ammonium concentration.
- Conversion to air concentration: Ammonia concentration in air estimated using the known uptake rate of the samplers (0.003241315 m3 h-1) and the exposure duration.
- Data quality flags: Data are flagged to indicate concerns; details are documented on page 4 of the full document.

## Data Quality and Rules
- Quality assessment framework applied to raw data:
  - CV rule: Coefficient of variation (SD/mean of replicates) < 15% indicates reliable replicates; if so, data are considered valid and flagged (103).
  - Calibration range rule: Values beyond calibration range but deemed valid due to instrument issues or inability to rerun.
  - Missing data rule: Missing measurements or metadata are indicated by -9999.
- Final dataset: NH3_Edinburgh_Uptake_Rate_2020.csv contains accepted data values with corresponding flags. Columns include site name, time period, NH3 concentration, and a data flag.
- Measurement details:
  - All concentration values are the average NH3 concentration for the specified exposure period.
  - Reported in µg NH3 m-3.
  - Each row represents one month of data for a single site.
- Dataset metadata: Alongside concentration values, the dataset includes various metadata fields (site name, unique site identifier, network_id, parameter_id, start/end dates and times, exposure period, data capture percentage, validity status, EMEP code, Month-Year, and comments).

## Dataset Structure and Content
- Main structure: One row per site per month, with associated metadata fields.
- Primary output fields:
  - Site name and unique identifiers
  - Start and end dates/times of measurement
  - Ammonia concentration for the exposure period
  - Data flag (valid/invalid and related notes)
- Additional fields (as per the document) include: network_id, parameter_id, measurement start/end dates and times, measurement value (µg NH3 m-3), less-than flag for detection limit, verification id, unit id, data capture, validity_id, EMEP code, Month-Year, and comments.
- Flags and codes:
  - Data capture and validity indicators (e.g., valid, not valid)
  - EMEP-related flags with predefined meanings (e.g., missing data, below detection limit, contamination indicators, sampling context)
  - These flags are used to annotate data quality and context for downstream use.

## Site Information
- Edinburgh uptake rate OTC
  - Start date: 01/03/2020; End date: ongoing
  - Location: Latitude 55.863150, Longitude -3.209845
  - Inlet height: 1.5 m
  - Collocated with UKEAP UKA00128
- Auch
  - Start date: 01/03/2020; End date: ongoing
  - Location: Latitude 55.792160, Longitude -3.242900
  - Inlet height: 1.5 m
  - Collocated with UKEAP UKA00451
- Hills
  - Start date: 01/03/2020; End date: ongoing
  - Location: Latitude 54.452500, Longitude -6.083340
  - Inlet height: 1.5 m
  - Collocated with UKEAP UKA00293

## Data Use and Interpretation (Data Support Perspective)
- The dataset enables self-serve access to monthly NH3 uptake-rate measurements across multiple sites, with clear QC and flagging to support reliable use.
- Structure supports aggregation and temporal analyses (monthly trends, site comparisons) while preserving detailed metadata for traceability.
- The comprehensive flag system (CV-based validity, calibration-range considerations, missing data, and EMEP-related codes) facilitates robust data quality assessment prior to analysis or policy use.