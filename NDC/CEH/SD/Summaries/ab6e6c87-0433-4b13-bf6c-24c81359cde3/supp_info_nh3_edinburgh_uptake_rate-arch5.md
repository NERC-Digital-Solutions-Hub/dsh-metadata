# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

## Overview
- Purpose: initial results to determine the uptake rate for ALPHA® samplers prepared and analysed at UKCEH Edinburgh for the UK and similar climates.
- Roles: site operators include UKCEH staff, AFBI Hillsborough staff, and Ricardo AEA staff; analysis conducted by CEH Edinburgh.
- Sampling design: passive samplers exposed in monthly cycles at the start of each month to measure NH3 concentrations in air.

## Methods

- UKCEH ALPHA® sampler
  - Composition: citric acid coated filter to capture ammonia; white PTFE membrane protects the filter; membrane faces downward during exposure.
  - Deployment: replicates attached to a shelter on a pole at ~1.5 m above ground; samplers shielded when not exposed.
  - Analysis: exposed samplers extracted into deionised water; ammonia quantified by SEAL AA3 colorimetry; results converted to average NH3 in air using a known uptake rate of 0.003241315 m³ h⁻¹ and exposure duration.
- Data processing and flags
  - Raw data quality assessed with predefined rules; some data are flagged for quality concerns.
  - Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv containing accepted data values with appropriate flags.
- Data contents
  - Each row represents one month of data for a single site; columns include site name, start/end dates, ammonia concentration (µg NH3 m⁻³), and a data flag.

## Data quality and validation

- Validation rules
  - Coefficient of variation (CV) < 15% across replicates indicates reliable replicates; if >15%, evaluation occurs and potentially discards from site/lab notes. Valid results are flagged as 103.
  - Values greater than calibration range may still be valid if re-run/dilution is not possible due to instrument failure or sample loss.
  - Missing data are indicated by -9999 in the measurement field or missing date/time metadata.
- Data flags and status
  - The dataset includes a data capture indicator and a validity flag, along with EMEP status codes (A-J) that summarize verification status, data issues, and EMEP flags.
  - EMEP flags provide standardized reasons for data adjustments or exclusions (e.g., contamination, below detection, sampling period anomalies, etc.). Examples include 103 (CV > 15% but valid) and various contamination or measurement-status codes.

## Data structure and contents

- Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv
  - Key fields:
    - Site id (unique), Site name, network_id (RSW)
    - parameter_id (alpha_NH3_g)
    - measurement start date/time and measurement end date/time
    - measurement (ammonia concentration; units: µg NH3 m⁻³)
    - less than (detection limit flag; 1 if below detection)
    - verification id (1=Verified, 2= Preliminary verified, 3=Not verified)
    - unit id (24 = µg NH3 m⁻³)
    - Data capture (percentage)
    - Validity_id (1 = valid, -1 = not valid)
    - EMEP code (data status and flags)
    - Month-Year, Comments
- Data context
  - All concentration values are average concentrations for the specified exposure period and are reported in micrograms per cubic meter (µg NH3 m⁻³).
  - The dataset includes a detailed mapping of data status through EMEP flags to support international comparability and quality assessment.

## Site information

- Edinburgh uptake rate sites (start/end dates and metadata)
  - Edinburgh uptake rate OTC (OuT? Notation): start 01/03/2020; end ongoing; coordinates 55.863150, -3.209845; inlet height 1.5 m; collocated with UKA00128.
  - Edinburgh uptake rate Auch: start 01/03/2020; end ongoing; coordinates 55.792160, -3.242900; inlet height 1.5 m; collocated with UKA00451.
  - Edinburgh uptake rate Hills: start 01/03/2020; end ongoing; coordinates 54.452500, -6.083340; inlet height 1.5 m; collocated with UKA00293.
  - Edinburgh uptake rate Chilbolton: start 01/01/2021; end ongoing; coordinates 51.149617, -1.438228; inlet height 1.5 m; collocated with UKA00614.

## Data management, sharing, and governance

- Data stewardship considerations
  - Documentation includes dataset contents, measurement methodology, QA/QC rules, and flagging procedures to ensure data are discoverable, interpretable, and reusable.
  - Data are prepared for sharing via standard portals, with explicit data flags and metadata to support correct interpretation and reuse.
  - Ongoing updates are implied through the “ongoing” end dates for sites and the monthly sampling regime, necessitating clear versioning and provenance in data catalogues.

## Notes for data users and stewards

- Use and interpretation
  - Concentrations represent average NH3 in air over defined exposure periods; uptake rate and exposure duration are used to convert to ambient NH3 values.
  - Be mindful of quality flags (CV, calibration range, missing data) and EMEP flags when analyzing temporal trends or performing inter-site comparisons.
- Metadata and governance
  - Ensure alignment with EMEP/UK-AIR conventions for flags and data status codes.
  - Maintain linkage between final data file (NH3_Edinburgh_Uptake_Rate_2021.csv) and its site metadata, including coordinates and deployment details.
  - Track data provenance and updates as sites continue ongoing measurements, including changes in operators or lab analysis workflow.