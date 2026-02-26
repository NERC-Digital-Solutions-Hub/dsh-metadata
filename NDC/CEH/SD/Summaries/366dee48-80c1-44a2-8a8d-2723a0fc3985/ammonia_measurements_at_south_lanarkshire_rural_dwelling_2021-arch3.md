# Passive sampler ammonia measurements indoors and outdoors at a rural dwelling in South Lanarkshire, 2021

## Overview
- Study location: two sites in a rural dwelling in South Lanarkshire (indoors in hall; outdoors in garden behind a grassland/dairy farm).
- Purpose: measure ammonia (NH3) concentrations in air to support environmental health monitoring.
- Operators: dwelling owner acts as site operator; Centre for Ecology and Hydrology (UKCEH) Edinburgh conducts analysis.
- Timeframe: sampler cycles exposed monthly; site information indicates ongoing sampling since 2017 with data referenced for 2019–2020 in the final dataset description.

## Methodology and Analysis
- Instrumentation: UKCEH ALPHA® passive samplers using a citric acid coated filter to capture NH3; PTFE membrane protective layer; membrane oriented downwards during exposure.
- Deployment: replicate samplers (to improve reliability) mounted on shelters on poles at ~1.5 m above ground.
- Analysis: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetry (measures ammonium concentration).
- Quantification: ambient NH3 concentration calculated from sampler ammonium concentration using a known uptake rate of 0.003241315 m3/h and the exposure duration.
- Data quality flags: samples flagged for issues; data quality assessed according to predefined rules.

## Data Structure and Contents
- Dataset name: NH3_SouthLanarkshire_indoors_outdoors2019-2020.csv (final accepted data Value set; notes potential mismatch with 2021 title).
- Structure: each row represents one month of data for a single site; columns include:
  - Site ID, Site name, Network ID (RSW), Parameter ID (alpha_NH3_g)
  - Measurement start/end date and time
  - Measurement value ( NH3 concentration in µg NH3 m-3)
  - Flags for detection limit (below), verification status, data unit, data capture percentage, validity, and EMEP code
  - Month-Year and any Comments
- Data columns detailed in the source include: unit (µg NH3 m-3), data capture (%), validity (valid/not valid), verification status, EMEP codes, and an array of metadata fields.
- Data capture and flags: detailed flag taxonomy (e.g., 103 for valid measurement with CV <15%, various EMEP and data-status codes). Flags such as -9999 indicate missing measurements or meta data.

## Site Information
- Inside (indoors): start date 01/01/17; end date ongoing; coordinates 55.64072, -3.59705; inlet height 1.5 m; location in hall of dwelling.
- Outside (outdoors): start date 01/01/17; end date ongoing; coordinates 55.64072, -3.59705; inlet height 1.5 m; location in garden of dwelling.

## Quality Assurance, Metadata, and Data Governance
- QA criteria:
  - Coefficient of variation (replicates) < 15% to validate results; CV >15% triggers review of replicates; valid results can still be reported (flag 103).
  - Some measurements may exceed calibration range but remain valid.
  - Missing data indicated by -9999 in the data fields; partial metadata may also be missing.
- Data flags and codes:
  - Detailed EMEP flags and data status codes are provided (e.g., data capture, validity, verification status, contamination and local influence indicators).
  - A mapping of common conditions (e.g., below detection limit, observed values reported, nearby agricultural or traffic influence) is documented.
- Data governance implications:
  - The dataset emphasizes the need for high-quality metadata, access to underlying data, and data sharing to ensure transparency and reproducibility.
  - Potential barriers include data access, data silos, and the need to publicly share datasets and metadata.

## Relevance for Monitoring Frameworks
- Demonstrates a structured approach to environmental health monitoring using passive samplers with replicates to improve reliability.
- Shows end-to-end workflow: deployment, sampling cadence, laboratory analysis, data transformation to ambient concentration, and robust QA/QC with explicit data flags.
- Illustrates metadata richness and dataset documentation (field definitions, units, timing, data capture, and validation flags) essential for governance and data reuse.
- Highlights practical barriers identified by monitoring framework authors, including data access, metadata completeness, data transformation requirements, and governance for data sharing.