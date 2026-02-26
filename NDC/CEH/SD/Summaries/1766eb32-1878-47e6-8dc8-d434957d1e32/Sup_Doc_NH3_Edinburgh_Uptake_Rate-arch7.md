# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Purpose: Initial results to determine uptake rate for CEH ALPHA samplers measuring NH3 in air across the UK and similar climates.
- Responsibilities: Local site operator duties by UK CEH staff and AFBI staff; analysis by CEH Edinburgh.
- Sampling plan: Samplers exposed monthly at the start of each month; first-year uptake rate not used due to COVID-19 data losses and insufficient calibration data.

## CEH ALPHA Sampler Method
- Type: Passive sampler for NH3 using a citric acid coated filter and a white PTFE membrane to capture ammonia; membrane facing downward during exposure.
- Deployment: Replicate samplers attached to a shelter on a pole at about 1.5 m above ground; protection provided by plastic containers.
- Analysis: Exposed samplers extracted into deionised water and analysed with SEAL AA3 (colorimetry) to determine ammonium concentration; concentration of NH3 in air derived using a known uptake rate (0.003241315 m3 hr-1) and exposure duration.

## Sampling and Data Processing
- Data collection: Monthly exposure periods; replicates used to improve reliability.
- Data quality checks: Raw data reviewed against quality rules; flagging applied to indicate data concerns (see Data Quality section).
- Data outputs: Final dataset NH3_Edinburgh_Uptake_Rate_2020.csv contains accepted values with appropriate flags; site names and spatial identifiers provided.
- Site information: Site names and coordinates listed (Edinburgh uptake rate OTC, Auch, Hills) with 1.5 m height and collocation details.

## Data Quality and Flags
- Flagging rules (summary):
  - Rule 1: Coefficient of variation (CV) of replicates < 15% => valid; flag 103 applied if data considered representative.
  - Rule 2: Values above calibration range but considered valid due to instrument constraints.
  - Rule 3: Missing data or metadata (-9999 placeholders) => measurements cannot be calculated.
- Data status: Each row includes a data flag indicating validity and a data capture percentage; additional EMEP/QA flags accompany the dataset.
- EMEP flags: Codes indicate data capture status, validity, and reason (e.g., 103 CV > 15%; 781, 780 for below detection or estimation; 999 for missing data; various codes for contamination or nearby activities).

## Dataset Contents and Attributes
- Final dataset: NH3_Edinburgh_Uptake_Rate_2020.csv
- Structure: One row per month per site; columns include:
  - Site name (e.g., Edinburgh uptake rate OTC, Auch, Hills)
  - Start date and end date of exposure period
  - Ammonia concentration for the exposure period (µg NH3 m-3)
  - Data flag and verification status
  - Unit id (µg NH3 m-3)
  - Month-Year and related metadata
  - Additional fields include calibration status, data capture percentage, and EMEP/QA status
- Data details: Site-level metadata (page 5) lists site identifiers and spatial identifiers; concentration values are annual/monthly averages for each exposure period.

## Spatial Information and Map-readiness
- Site locations (latitude/longitude) provided for three Edinburgh-area uptake sites:
  - Edinburgh uptake rate OTC: latitude 55.863150, longitude -3.209845, altitude/inlet height 1.5 m; collocated with UKA00128
  - Edinburgh uptake rate Auch: latitude 55.792160, longitude -3.242900, altitude 1.5 m; collocated with UKA00451
  - Edinburgh uptake rate Hills: latitude 54.452500, longitude -6.083340, altitude 1.5 m; collocated with UKA00293
- Data are suitable for GIS mapping of monthly NH3 uptake rates and integration with other spatial datasets; note the ongoing nature of data collection and that the first year is excluded from uptake-rate calculations.

## Considerations for GIS Analysts
- Use the NH3_Edinburgh_Uptake_Rate_2020.csv to map monthly NH3 concentrations by site, applying data-flag and EMEP codes to filter or annotate data quality.
- Integrate site coordinates and altitude (inlet height) for accurate spatial visualization.
- Be mindful of data gaps and flags (e.g., missing data, CV issues, or contamination indicators) that affect map reliability.
- Monitor updates to the dataset as more months are collected beyond 2020, since data collection is ongoing and the initial uptake-rate calibration year was not used.