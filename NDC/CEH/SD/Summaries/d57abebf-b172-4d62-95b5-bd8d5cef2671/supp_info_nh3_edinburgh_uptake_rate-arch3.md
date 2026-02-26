# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Overview
- Study to determine the uptake rate for ALPHA® passive samplers used to measure NH3 in air in the UK climate context.
- Field work conducted at four UKEAP network sites; local site operator duties shared among UKCEH, AFBI, and Ricardo AEA.
- Analysis performed by CEH Edinburgh; samplers exposed monthly at the start of each month.
- Final dataset provides monthly ammonia concentrations and associated metadata for each site.

## UKCEH ALPHA® sampler method
- Sampler design: citric acid–coated filter to capture NH3, protected by a white PTFE membrane; membrane oriented downward during exposure.
- Deployment: replicate samplers attached to a shelter on a pole at about 1.5 m above ground; plastic protective containers for all samplers.
- Sample processing: exposed samplers extracted into deionised water; NH3 quantified by SEAL AA3 colorimetry; results converted to air concentration using a known uptake rate (0.0038422 m3 h-1) and exposure duration.
- Exposure protocol: monthly cycles beginning at the start of each month.
- Data handling: raw data quality assessed; flagged data noted on pages 4 and in the final dataset.

## Data and outputs
- Final dataset: submissions_ED_UR_NH3_2022.csv containing accepted NH3 concentration values and appropriate data flags.
- Units: micrograms of NH3 per cubic metre of air (µg NH3 m-3).
- Dataset structure: each row represents one month of data for a single site; key columns include site name, exposure start/end dates, ammonia concentration, and data flag.
- Site identifiers and metadata are listed (e.g., site name, unique site ID, network ID, parameter type, start/end dates, capture percentage, and data status flags).

## Data quality, flags, and metadata
- Quality control rules:
  - Coefficient of variation (CV) of replicates must be < 15%; if >15%, replicates are evaluated for discard, otherwise the result is considered valid and flagged (103).
  - Values above calibration range may be deemed valid if remeasurement was not possible due to instrument issues.
  - Missing data are coded as -9999, including missing date/time metadata.
- Data flags: detailed in the dataset with flags indicating verification status, data status codes, and EMEP/QA flags (e.g., 999, 781, 780, 654, 653, 652, 651, 260, 103, etc.), providing context for data validity, contamination concerns, and local influences.
- Documentation for flags and codes is aligned with EMEP and UK-AIR data flag conventions to support traceability and auditability.

## Data governance, sharing, and stewardship
- Data capture and verification statuses documented within the dataset (e.g., verification statuses 1–3).
- Underlying data and metadata are prepared for public sharing, but public dissemination can be a barrier for some datasets within certain contexts.
- Clear data provenance: site information, collection methods, and processing steps are catalogued to support transparency and reuse.
- The dataset includes comprehensive metadata fields (dates, times, units, capture percentages, data status codes, and comments) to enable reproducibility and assessment of data quality.

## Site information
- Edinburgh uptake rate OTC: start 01/03/2020; end ongoing; coordinates 55.863150, -3.209845; inlet height 1.5 m; collocated with UKEAP UKA00128.
- Auch: start 01/03/2020; end ongoing; coordinates 55.792160, -3.242900; inlet height 1.5 m; collocated with UKEAP UKA00451.
- Hills: start 01/03/2020; end ongoing; coordinates 54.452500, -6.083340; inlet height 1.5 m; collocated with UKEAP UKA00293.
- Chilbolton: start 01/01/2021; end ongoing; coordinates 51.149617, -1.438228; inlet height 1.5 m; collocated with UKEAP UKA00614.

## Relevance for monitoring framework authors
- Demonstrates a structured approach to selecting and deploying a measurement method (passive NH3 samplers) and converting field measurements into standardized air concentrations.
- Emphasizes rigorous quality assurance and metadata management to maintain data usefulness, including: replicates, CV thresholds, calibration considerations, and clear data flags.
- Highlights challenges aligned with monitoring frameworks: data availability and access, data silos, metadata completeness, data transformation needs, and the importance of data governance and transparent sharing practices.
- Provides a concrete example of documenting data lineage, processing steps, and site-level metadata to support decision-making, reporting, and future monitoring design.