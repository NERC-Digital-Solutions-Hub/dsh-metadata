# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

## Aim and scope
- Initial results from a study to determine the uptake rate for ALPHA® passive samplers used to measure atmospheric NH3 across four UK sites.
- Samplers prepared and analyzed at UKCEH Edinburgh; local site operator duties performed by UKCEH, AFBI, and Ricardo AEA.
- Samplers exposed in monthly cycles at the start of each month; data produced to support consistent environmental monitoring and policy assessment.

## Methods and samplers
- UKCEH ALPHA® sampler:
  - Citric acid coated filter to capture NH3; protected by a white PTFE membrane (diffusion-controlled capture); membrane oriented downward during exposure.
  - Sampler assembled on a shelter at ~1.5 m above ground; replicated samplers used per site for reliability.
  - Exposed in monthly cycles; plastic containers provided for protection.
- Analysis:
  - Exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry.
  - Concentration in sampler converted to average NH3 concentration in air using a known uptake rate: 0.003241315 m^3 h^-1.
  - Result units: µg NH3 m^-3 for the exposure period.
- Quality control and data flags:
  - Data flagged for concerns; reviewed per the quality rules described below.
  - Raw data checked for quality and transformed into final dataset NH3_Edinburgh_Uptake_Rate_2021.csv.

## Data handling, quality assurance, and flags
- Quality rules:
  - Coefficient of variation (CV) across replicates must be < 15%; if >15%, replicates may be discarded and data assessed for validity.
  - Some data may be greater than calibration range but deemed valid due to inability to re-run; still considered valid.
  - Missing data flagged as -9999 (including missing date/time metadata).
- Final dataset:
  - NH3_Edinburgh_Uptake_Rate_2021.csv contains accepted data values with appropriate flags.
  - Structure includes: site name, exposure start/end dates, ammonia concentration for the period, and a data flag.
  - Data capture, verification, and metadata fields present; values reported as monthly averages.
- Data status and flags:
  - EMEP/Data status codes provide additional context on verification, data issues, and quality (see detailed mapping in the dataset documentation).
  - Example practical flags include valid/invalid, detection limit indicators, and notes on sampling conditions.

## Data content and dataset structure
- Dataset contents:
  - Each row represents one month of data for a single site.
  - Columns include: site name, exposure start and end dates, ammonia concentration (µg NH3 m^-3), and a data flag.
  - Additional fields include verification status, data capture percentage, and meta information such as month-year.
- Key quantitative parameter:
  - Uptake rate used for conversion: 0.003241315 m^3 h^-1.
  - Reported concentrations are averages over the specified exposure period (monthly).

## Sites and location context
- Four sites with ongoing monitoring (start_date 2020 or 2021; ongoing):
  - Edinburgh uptake rate OTC (collocated with UKA00128): lat 55.863150, lon -3.209845.
  - Edinburgh uptake rate Auch (collocated with UKA00451): lat 55.792160, lon -3.242900.
  - Edinburgh uptake rate Hills (collocated with UKA00293): lat 54.452500, lon -6.083340.
  - Edinburgh uptake rate Chilbolton (collocated with UKA00614): lat 51.149617, lon -1.438228.
- All sites use 1.5 m height sampling and maintain standardized exposure protocols to enable cross-site comparability.

## Relevance for environmental monitoring and policy
- Provides standardized, comparable NH3 concentration estimates across multiple sites and time periods.
- Aids assessment of environmental health and policy performance by offering consistent data formats, quality flags, and documented methods.
- Facilitates data sharing and reuse by providing a clear dataset structure, metadata, and flagging schema to support transparency and verification.
- Supports broader data integration by aligning with known data flags and EMEP/UK-AIR conventions for non-biased, quality-assured monitoring outputs.