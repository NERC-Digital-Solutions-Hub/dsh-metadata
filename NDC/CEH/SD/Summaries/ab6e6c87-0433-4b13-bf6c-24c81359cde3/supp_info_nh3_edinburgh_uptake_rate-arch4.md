# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

## Overview
- This report presents initial measurements and processing for ammonia (NH3) using UKCEH ALPHA® passive samplers at four UKEAP network sites in 2021.
- Samplers were prepared and analyzed at UKCEH Edinburgh; local site duties performed by UKCEH, AFBI (Hillsborough), and Ricardo AEA.
- Exposure cycles were monthly, at the beginning of each month; data are intended to determine the uptake rate for the ALPHA® samplers (0.003241315 m3 h-1) and provide site-specific NH3 concentrations.

## Sampling and Analysis Method
- The UKCEH ALPHA® sampler uses a citric acid coated filter to capture ammonia, protected by a white PTFE membrane. The membrane is oriented downwards during exposure.
- Replicate samplers are deployed to improve reliability; exposed at ~1.5 m above ground on a shelter on a pole/post.
- After exposure, samplers are extracted with deionised water and analyzed by SEAL AA3 using colourimetric detection to determine ammonium concentration, then converted to an average NH3 concentration in air for the exposure period.
- Uptake rate used for conversion: 0.003241315 m3 h-1.
- Data quality flags are applied to highlight concerns (described in data handling).

## Data Handling and Quality Control
- Raw data are quality-checked using predefined rules:
  - Coefficient of Variation (CV) of replicates: CV < 15% is expected for valid results; if >15%, replicates may be discarded; data flagged as valid (103) if the average is representative.
  - Some results exceed calibration range: still considered valid if rerun/dilution was not possible due to instrument issues.
  - Missing data are marked with -9999.
- The final dataset is NH3_Edinburgh_Uptake_Rate_2021.csv, containing accepted values with appropriate data flags.
- Data flags and EMEP flags (codes and meanings) are documented; EMEP flags cover scenarios such as contamination, detection limits, sampling period duration, and data quality notes.

## Data Products and Structure
- Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv
- Data contents (per row): one month of data for a single site, including:
  - Site name, start date, end date, ammonia concentration (µg NH3 m-3)
  - Data flag (quality/validity)
  - Additional fields include verification id, unit id, data capture percentage, EMEP flag, Month-Year, and Comments
- Data columns described include:
  - Site id, Site name, network_id, parameter_id
  - measurement start date/time, measurement end date/time
  - concentration (µg NH3 m-3)
  - less than detection flag, verification id, unit id
  - Data capture, Validity_id, EMEP code, Month-Year, Comments
- Units: micrograms of NH3 per cubic meter of air (µg NH3 m-3)

## Site Information
- Edinburgh uptake rate OTC: start 01/03/2020; ongoing; lat 55.863150, lon -3.209845; inlet height 1.5 m; collocated with UKA00128
- Edinburgh uptake rate Auch: start 01/03/2020; ongoing; lat 55.792160, lon -3.242900; inlet height 1.5 m; collocated with UKA00451
- Edinburgh uptake rate Hills: start 01/03/2020; ongoing; lat 54.452500, lon -6.083340; inlet height 1.5 m; collocated with UKA00293
- Edinburgh uptake rate Chilbolton: start 01/01/2021; ongoing; lat 51.149617, lon -1.438228; inlet height 1.5 m; collocated with UKA00614

## Governance, Access, and Reuse Considerations for Data Leaders
- Data governance: multi-organization contributions (UKCEH, AFBI, Ricardo AEA) with centralized analysis at UKCEH Edinburgh; monthly exposure and replication strategy enhance reliability and traceability.
- Metadata and discoverability: detailed dataset description, field definitions, and EMEP flags support interoperability and cross-network comparisons; dataset naming communicates its Edinburgh uptake rate basis.
- Data quality and enablement of decision-making: explicit quality rules (CV threshold, calibration range handling, missing data coding) provide transparency for end users and support risk-aware use in policy or monitoring programs.
- Gaps and coordination: complexity of data capture across sites and operators; reliance on a single uptake rate constant requires ongoing validation; potential for expanding datasets with additional site coverage or extended time series.
- Opportunities for data leaders: reuse in larger air-quality assessments, cross-site benchmarking, integration with other monitoring networks, and informing improvements in passive-sampling methodologies and metadata standards.