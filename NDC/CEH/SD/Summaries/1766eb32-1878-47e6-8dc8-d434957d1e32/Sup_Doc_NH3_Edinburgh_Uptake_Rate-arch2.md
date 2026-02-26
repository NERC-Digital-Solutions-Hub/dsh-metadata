# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Purpose and scope
- Report presenting initial results from a study to determine the uptake rate for CEH ALPHA samplers used to measure NH3 in air across the UK and similar climates.
- Local site operation by UK CEH and AFBI; analysis by CEH Edinburgh.
- Samplers exposed in monthly cycles; first-year data not used for uptake rate due to COVID-19-related data losses and insufficient calibration points.

## Method: CEH ALPHA sampler and analysis
- Passive sampler using a citric acid coated filter to capture NH3; protected by a white PTFE membrane.
- Exposed with the membrane end facing downwards at ~1.5 m above ground; replicates used for reliable estimation.
- Analysis: samplers extracted into deionised water, measured via SEAL AA3 colorimetry to determine ammonium concentration.
- Ammonia concentration in air calculated using the sampler uptake rate (0.003241315 m^3 h^-1) and exposure duration.
- Data are flagged to indicate quality concerns.

## Data quality and processing
- Raw data quality checks applied to determine validity.
- Key rules:
  - Coefficient of variation (CV) of replicates < 15%; if >15%, replicates may be discarded; if representative, data are valid (flag 103).
  - Samples > calibration range but still valid due to instrumentation constraints.
  - Missing data indicated by -9999 for measurement or meta data.
- Final dataset: NH3_Edinburgh_Uptake_Rate_2020.csv containing accepted values with appropriate flags; site names provided with spatial identifiers.
- Dataset contents: one row per month per site; columns include site name, start/end dates, exposure period NH3 concentration, and a data flag.
- Data status and codes include detailed Data Capture, Validity, and EMEP flags (mapping of verification status, data issues, and qualifiers).

## Dataset structure and field definitions
- Columns cover:
  - Station/site identifiers and network_id
  - Parameter_id and measurement period (start/end dates and times)
  - Measured NH3 concentration (µg NH3 m^-3)
  - Data quality indicators (detection limit flags, verification status, unit id, data capture, validity)
  - EMEP data status code and Month-Year
  - Comments
- EMEP flags provide reasons for data validity or caveats (e.g., contamination, detection limits, sampling conditions).

## Site information
- Edinburgh uptake rate sites (start date 01/03/2020; ongoing):
  - Edinburgh uptake rate OTC: latitude 55.863150, longitude -3.209845, height 1.5 m; collocated with UKA00128
  - Edinburgh uptake rate Auch: latitude 55.792160, longitude -3.242900, height 1.5 m; collocated with UKA00451
  - Edinburgh uptake rate Hills: latitude 54.452500, longitude -6.083340, height 1.5 m; collocated with UKA00293

## Data availability and usage
- Data are stored and uploaded to appropriate portals; intended to enable monitoring of environmental NH3 concentrations over time.
- Standardised approach facilitates comparison across sites and time, and supports data sharing and policy performance evaluation.
- Recognizes the value of integrating these uptake-rate datasets with other monitoring data to enhance environmental insights.