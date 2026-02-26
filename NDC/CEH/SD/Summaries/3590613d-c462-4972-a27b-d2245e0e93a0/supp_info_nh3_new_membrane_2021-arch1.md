# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

## Overview
- Study to validate a new PTFE membrane for ALPHA® passive ammonia samplers.
- Measurements collected at four UK UKEAP network sites during 2021.
- Analysis and sampling coordinated by UKCEH Edinburgh, with local site operator duties by UKCEH, AFBI Hillsborough, and Ricardo AEA Chilbolton.

## UKCEH ALPHA® Sampler Method
- Passive sampler design: citric acid coated filter captures NH3; white PTFE membrane protects the filter and allows diffusion; membrane oriented downwards during exposure.
- Sampling setup: replicates installed on poles at about 1.5 m height, sheltered, in separate containers for protection.
- Analysis workflow: exposed samplers are extracted in deionised water and measured by SEAL AA3 colorimetry to quantify ammonium; concentration in air derived using the sampler’s uptake rate and exposure duration.
- Uptake rate: new membrane uptake rate established as 0.0039701 m3 hr⁻¹ (derived from three sites; Hillsborough excluded due to unreliable exposure times).
- Exposure schedule: monthly cycles at the start of each month.

## Data Processing and Quality Assurance
- Data flagged for quality concerns; details referenced in accompanying notes.
- Raw data quality rules:
  - Coefficient of variation (CV) of replicates < 15% → data considered valid (flag 103); higher CV prompts evaluation of discarding replicates.
  - Data greater than calibration range can be valid if re-measurement wasn’t possible due to instrument issues.
  - Missing data or metadata coded as -9999.
- Final dataset: NH3_New_Membrane_2021.csv, containing accepted data values with appropriate flags. Each row represents one month’s data for a single site, including site name, dates, ammonia concentration (µg NH3 m⁻³), and a data flag.
- Data status and metadata fields include:
  - Site identifiers, network_id, parameter_id, measurement start/end dates and times.
  - Ammonia concentration and a flag indicating if below detection limit.
  - Verification status, data capture percentage, validity flag, EMEP flag codes, and Month-Year.
  - Additional comments per data row.

## Data Flags and EMEP Codes
- Data capture and validity flags indicate QA status (e.g., valid, not valid, verified).
- EMEP flag codes documented (examples):
  - 999: missing data; data capture 0; reason: missing measurement.
  - 781, 780, 654, 653, 652, etc.: various valid/invalid status reasons (e.g., below detection/quantification limits, representative sampling periods, nearby influences, contamination concerns).
- Data elements can be marked as valid or invalid with accompanying reasoning to support use in analyses.

## Site Information and Coverage
- Sites and uptake rate details:
  - Edinburgh uptake rate OTC; start 01/03/2020; end ongoing; coordinates ~55.863150, -3.209845; height 1.5 m; collocated with UKA00128.
  - Auch (Edinburgh uptake rate Auch); start 01/03/2020; end ongoing; coordinates ~55.792160, -3.242900; height 1.5 m; collocated with UKA00451.
  - Hills (Edinburgh uptake rate Hills); start 01/03/2020; end ongoing; coordinates ~54.452500, -6.083340; height 1.5 m; collocated with UKA00293.
  - Chilbolton (Edinburgh uptake rate Chilbolton); start 01/01/2021; end ongoing; coordinates ~51.149617, -1.438228; height 1.5 m; collocated with UKA00614.
- Data collection and analysis are conducted by UKCEH Edinburgh for ALPHA samplers, with collaboration from AFBI and Ricardo AEA at the respective sites.

## Data Access and Provenance
- The dataset NH3_New_Membrane_2021.csv contains monthly NH3 concentrations, site identifiers, measurement dates/times, data quality flags, and related metadata.
- The study provides a transparent record of site operations, uptake rate calculations, QA criteria, and data flag semantics to support reproducibility and further analysis.