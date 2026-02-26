# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

## Overview
- Study to validate a new PTFE membrane for UKCEH ALPHA® passive samplers to measure atmospheric ammonia (NH3).
- Conducted across four UKEAP network sites; sampling and analysis coordinated by UKCEH Edinburgh with AFBI Hillsborough and Ricardo AEA Chilbolton.
- Monthly exposure cycles; aim to support long-term environmental health monitoring and data-driven policy evaluation.

## Methods

- ALPHA® sampler design
  - Passive sampler using a citric acid coated filter to capture NH3; protected by a white PTFE membrane.
  - Membrane oriented downward during exposure.
  - Replicate samplers deployed for each site to improve reliability.
  - Exposure conducted at ~1.5 m above ground on a shelter, mounted on a pole.
- Analysis
  - Exposed samplers are extracted in deionised water and analysed with SEAL AA3 colorimetry to quantify ammonium.
  - Ambient NH3 concentration calculated using the sampler uptake rate for the new membrane: 0.0039701 m3 h-1.
  - Hillsborough site excluded from uptake-rate calculations due to unreliable exposure times.
- Sampling cadence and site responsibilities
  - Monthly cycles beginning of each month.
  - Local site operators and UKCEH staff manage field duties; UKCEH Edinburgh handles analysis.

## Data quality, processing and flags

- Data quality assessment
  - Raw data reviewed against quality rules; data flagged where concerns exist (details in accompanying pages).
  - Final dataset NH3_New_Membrane_2021.csv contains accepted values with appropriate data flags.
- Quality control criteria
  - Coefficient of variation (CV) of replicates < 15% generally indicates reliable replication; if CV > 15% and data are still deemed representative, results may be flagged as valid (103).
  - Values above calibration range may still be valid if instrument issues prevented re-analysis.
  - Missing data or metadata are indicated with -9999; datasets include notes on data capture and validity.
- Dataset structure
  - Columns include: site id, site name, network_id, parameter_id, measurement start/end dates and times, concentration (µg NH3 m-3), less-than flag, verification id, unit id, Data capture, Validity_id, EMEP code, Month-Year, Comments.
- Data status and flags
  - EMEP flag codes and UK AIR-derived flags (e.g., 999, 781, 780, 654, 653, 652, 651, 260, 103) documented with meanings such as missing data, below detection limit, data quality issues, representativeness of sampling period, or other contextual notes.
  - Data capture and validity indicators accompany each record to support data governance and traceability.

## Dataset and site information

- Site information (uptake rates and coordinates)
  - Edinburgh uptake rate (OTC) sites with start date 01/03/2020 and ongoing end date; coordinates and height details (1.5 m).
  - Auch uptake rate with start date 01/03/2020; coordinates and height details (1.5 m).
  - Hills uptake rate with start date 01/03/2020; coordinates and height details (1.5 m).
  - Chilbolton uptake rate with start date 01/01/2021; coordinates and height details (1.5 m).
  - All sites are collocated with UKEAP identifiers (UKA000128, UKA00451, UKA00293, UKA00614 respectively).

## Data governance and sharing considerations

- Emphasizes data provenance, QA/QC, and metadata completeness to support transparency in environmental health monitoring.
- Data are flagged and documented to aid auditors and policy-makers in assessing data quality, comparability, and suitability for trend analysis.
- Clear data structure and standardized flagging (including EMEP codes) facilitate integration with broader monitoring frameworks and reporting systems.

## Implications for monitoring frameworks

- The validation of a new sampling membrane enhances comparability and reliability of NH3 air concentration measurements across time and sites, informing policy evaluation of ammonia pollution.
- The study demonstrates rigorous QA/QC practices, explicit metadata, and structured data flags—key components for robust monitoring frameworks.
- The detailed documentation of uptake rates, calibration, site-specific details, and data status supports reproducibility and transparent decision-making in environmental health monitoring programs.