# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Overview
- Initial results from a study to determine the uptake rate for ALPHA® passive samplers used to measure ambient NH3 in UK climates.
- Sampling conducted at four UKEAP network sites; local duties handled by UKCEH Edinburgh, AFBI Hillsborough, and Ricardo AEA; analysis by CEH Edinburgh.
- Samplers exposed in monthly cycles starting at the beginning of each month.

## UKCEH ALPHA® Sampler Method
- Passive sampler design: citric acid-coated filter to capture NH3; protected by a white PTFE membrane; membrane oriented downwards during exposure.
- Deployment: replicate samplers mounted on shelters at ~1.5 m above ground; protective containers used for transport.
- Analysis workflow: exposed samplers extracted into deionised water and analyzed with SEAL AA3 (colorimetry) to determine ammonium concentration.
- Calculation: convert ammonium concentration to average NH3 in air using a known uptake rate of 0.0038422 m^3 h^-1 and exposure duration.

## Analysis and Uptake Rate
- Reported uptake rate used for conversions: 0.0038422 m^3 h^-1.
- Reported data flags indicate data quality concerns; full details provided in the accompanying documentation (page 4 of the report).

## Data and Quality Control
- Raw data quality assessment criteria:
  - Coefficient of variation (CV) of replicates < 15% → results considered representative (flagged as 103 if valid).
  - If results exceed calibration range but remain valid due to inability to rerun, still considered valid.
  - Missing data or metadata shown as -9999 in the relevant fields.
- Final dataset: submissions_ED_UR_NH3_2022.csv containing accepted data values with appropriate flags; columns include site name, exposure start/end dates, ammonia concentration (µg NH3 m^-3), and a data flag.
- Data units: NH3 concentration represented as micrograms per cubic metre (µg NH3 m^-3); each row corresponds to one month of data for a single site.

## Data Flags and EMEP Flags
- Data status and quality flags follow EMEP conventions, including:
  - 999: data capture missing
  - 781, 780: values affected by detection/quantification limits
  - 103: valid measurement with CV-related justification
  - 260, 654, 653, 652, 651, etc.: various contamination, boundary, or representativeness notes
  - Data status encoded alongside a descriptive reason (e.g., contamination suspected, sampling period issues, nearby emissions, etc.)
- Flags provide context for data usability and QA decisions; detailed flag meanings correspond to EMEP data flags (nilu.no).

## Dataset Contents
- The dataset contains monthly measurements per site, with fields including:
  - Site name, unique site identifier, network ID (ED_UR), measurement start/end dates and times
  - Measured ammonia concentration (µg NH3 m^-3)
  - Data capture and validity indicators, plus a data status/flag field and associated metadata
  - Month-Year field and optional comments

## Site Information
- Edinburgh uptake rate OTC
  - Start: 01/03/2020; End: ongoing
  - Latitude: 55.863150, Longitude: -3.209845; Inlet height: 1.5 m
  - Collocated with UKA00128
- Auch
  - Start: 01/03/2020; End: ongoing
  - Latitude: 55.792160, Longitude: -3.242900; Inlet height: 1.5 m
  - Collocated with UKA00451
- Hills
  - Start: 01/03/2020; End: ongoing
  - Latitude: 54.452500, Longitude: -6.083340; Inlet height: 1.5 m
  - Collocated with UKA00293
- Chilbolton
  - Start: 01/01/2021; End: ongoing
  - Latitude: 51.149617, Longitude: -1.438228; Inlet height: 1.5 m
  - Collocated with UKA00614

## Data Access and Usage
- The results support estimates of ambient NH3 concentrations across different UK locations and climates.
- Data quality and flag details are provided to guide interpretation and subsequent analyses.
- Site operator duties and collaboration are noted as part of the data collection process.