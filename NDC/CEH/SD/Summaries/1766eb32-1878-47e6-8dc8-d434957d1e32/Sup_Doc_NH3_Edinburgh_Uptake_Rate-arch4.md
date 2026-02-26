# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Study to determine uptake rate for CEH ALPHA® samplers prepared and analyzed at UK CEH Edinburgh for the UK and similar climates.
- Local site duties performed by CEH staff and AFBI (Hillsborough); analysis by CEH Edinburgh.
- ALPHA® samplers used to measure ammonia concentrations; first-year data not used for uptake rate due to COVID-19 data losses.

## Sampling and Analysis Method
- Passive samplers placed at about 1.5 m above ground on shelters; multiple replicates per site to improve reliability.
- Monthly exposure cycles at the beginning of each month.
- Citric acid coated filter captures NH3; sealed with a protective cap when not exposed; white PTFE membrane allows diffusion of NH3.
- Extraction in deionised water; analysis by SEAL AA3 using colorimetry to determine ammonium concentration.
- Ammonia concentration in air calculated from ammonium concentration using a known uptake rate of 0.003241315 m3 h-1 and exposure duration.

## Data Processing and Uptake Rate Calculation
- Raw data evaluated for quality; conversion to final NH3 in air for each exposure period.
- Final dataset NH3_Edinburgh_Uptake_Rate_2020.csv contains accepted values with flags.
- Data captured as monthly records per site; fields include site name, start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.

## Data Quality, Flags, and Metadata
- Data flagged to indicate concerns; criteria include:
  - Coefficient of variation (CV) < 15%: considered valid; if CV > 15%, replicates may be discarded; average result deemed representative and data flagged as valid (103).
  - Data beyond calibration range but still valid if rerun was not possible due to instrument failure or sample loss.
  - Missing data or metadata marked with -9999; missing date/time prevents calculation.
- EMEP flags provided to indicate data status, detection/quantification limits, contamination, and other local influences.
- Data are documented with detailed field descriptions (site IDs, network IDs, parameter types, dates/times, data capture percentages, validity flags, EMEP codes, Month-Year, and comments).

## Dataset Contents and Site Information
- Each row represents one month of data for a single site; columns cover:
  - Site name, unique site identifier, network_id, parameter_id
  - Measurement start/end dates and times
  - Measurement value (ammonia concentration, µg NH3 m-3)
  - Less-than flag, verification id, unit id
  - Data capture percentage, validity_id, EMEP code, Month-Year, and Comments
- Site information includes:
  - Edinburgh uptake rate OTC (coords 55.863150, -3.209845; 1.5 m inlet; collocated with UKA00128)
  - Edinburgh uptake rate Auch (coords 55.792160, -3.242900; 1.5 m inlet; collocated with UKA00451)
  - Edinburgh uptake rate Hills (coords 54.452500, -6.083340; 1.5 m inlet; collocated with UKA00293)

## Data Governance and Usage Considerations
- Data are structured for traceability: site identifiers, network IDs, measurement types, and timestamps to support discoverability and reuse.
- Metadata and flagging enable users to assess data quality and suitability for analyses and reporting.
- Collaboration across institutions supports an integrated data system for ammonia uptake studies.

## Limitations and Next Steps
- First-year uptake-rate calculation not performed due to data gaps from COVID-19; ongoing data collection and validation planned.
- Continued use of replicates and metadata-driven quality checks to ensure robust, comparable data across sites and time.