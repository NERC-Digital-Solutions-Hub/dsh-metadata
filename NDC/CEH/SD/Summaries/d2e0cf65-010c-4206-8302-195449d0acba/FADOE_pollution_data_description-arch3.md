# FADOE_pollution.csv

## Overview
- Dataset of ambient pollutant concentrations (NOx, NO, NO2, O3) measured in the center of eight Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Experimental design includes four treatments ( diesel exhaust D; ozone O3; diesel exhaust + ozone D+O3; control CON) with two rings per treatment.
- Data intended to support assessment of pollutant exposure and inform environmental health policy decisions.

## Experimental Design and Collection/Instrumentation
- Eight rings arranged with two rings per treatment: D, O3, D+O3, CON.
- Pollutants measured at the ring center: NOx (ppb), NO (ppb), NO2 (ppb), O3 (ppb).
- Measurement cadence: every 60 seconds using an automated switching system connected to:
  - O3 analyzer: Thermo Scientific Model 49i
  - NOx analyzer: Thermo Scientific Model 42C
- Additional environmental context: wind speed and wind direction captured from four directions around the field (south, west, north, east) using four anemometers.
- Temporal metadata: Year, Date, Time stamps.
- Spatial metadata: Field coordinates provided for 2018 and 2019 (latitude/longitude).

## Data Structure and Content
- Pollutants and related columns:
  - Ozone in Column P
  - NO in Column Q
  - NO2 in Column R
  - NOx in Column S
- Treatment designation in Column E (D, O3, D+O3, CON).
- Wind data from four directional pairs:
  - South ws1/wd1 (Columns F/K)
  - West ws2/wd2 (Columns G/L)
  - North ws3/wd3 (Columns H/M)
  - East ws4/wd4 (Columns I/N)
- Time-related columns: Year (A), Date (B), Time (C).

## Temporal and Spatial Coverage
- Field located at specified coordinates with records for 2018 and 2019.
- High-frequency (1-minute) pollutant and wind observations enabling detailed exposure assessment.

## Data Quality, Metadata, and Governance Considerations
- Explicit instrumentation and measurement details support traceability and reproducibility.
- Availability of unit definitions (ppb) and instrument models facilitates data integration and standardization.
- Potential governance considerations for monitoring frameworks:
  - Need for comprehensive metadata to ensure data provenance and comparability across studies.
  - Clarity on data sharing and openness to enable reuse in policy analysis.
  - Documentation of data quality assurance steps and data transformation processes for end users.
  - Consideration of data updates, versioning, and handling of any gaps or anomalies in high-frequency time series.

## Relevance for Environmental Health Monitoring and Policy
- Provides a controlled, replicateable context to study how diesel exhaust and ozone exposures impact ambient pollutant mixtures.
- Rich temporal resolution supports evaluation of exposure-response relationships and the combined effects of multiple pollutants.
- Coupled meteorological data (wind speed/direction) enhances interpretation of dispersion and exposure patterns.
- Data can inform monitoring framework decisions on:
  - What pollutant metrics and temporal scales are most informative for policy evaluation.
  - How to structure dashboards or reports that communicate complex findings clearly.
  - What metadata and governance controls are necessary to ensure data quality and openness.