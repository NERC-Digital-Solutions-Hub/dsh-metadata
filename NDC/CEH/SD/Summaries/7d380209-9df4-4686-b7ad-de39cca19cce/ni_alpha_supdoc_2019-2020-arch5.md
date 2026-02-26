# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

## Overview
- Two CSV files contain monthly NH3 concentrations for 25 NI ALPHA® sites (2019 and 2020); an additional 4 DELTA sites contributed NH3 data in 2019-2020 via the NI DELTA® Network and a co-located site allowed inter-method comparison.
- Network operated by AFBI and UKCEH, funded by DAERA.
- Data intended for model validation and calibration of NH3 concentrations (e.g., FRAME and CBED) and to support assessment of policy scenarios on NH3.

## Data collection and scope
- Monitoring method: UKCEH high-sensitivity ALPHA® passive samplers; sampling at ~1.5 m height with three replicates per measurement.
- Sampling cadence: monthly, time-integrated exposure within each calendar month.
- Analysis: NH3 captured on citric acid coating, extracted and measured as NH4+ by colorimetry; conversion to NH3 concentration uses an annual uptake rate for the sampler.
- Units and detection: NH3 concentration in µg NH3 m-3; LOD = 0.03 µg NH3 m-3.
- Spatial coverage: 25 NI ALPHA® sites (24 rural, 1 urban); coordinates withheld to two decimals for confidentiality. 25th site Hillsborough included co-located with DELTA for cross-method comparison.

## Monitoring sites and data structure
- Site information includes site_id, site_name, network_id (AFBI), measurement start/end dates, and geographic coordinates (rounded for confidentiality).
- Data are presented as time-integrated monthly concentrations per site.
- DELTA sites are reported in a companion submission; NI DELTA data are integrated for cross-method evaluation.

## Data processing and quality assurance
- Central data handling: Oracle-based AAGA database; calculations performed via a ShinyApp.
- QA/QC process in three stages:
  - Stage 1 (automatic): checks for date overlaps, monthly exposure windows, replicate precision (CV > 15%), automated flagging of anomalies, handling of missing samples (-9999 or -1), and flagging of sampling duration deviations.
  - Stage 2 (manual): review of blanks, sampling malfunctions, contamination indicators, and outliers; invalid data flagged as needed.
  - Stage 3 (expert): project scientist review considering site context, modelling expectations, year-to-year and site-to-site comparisons, and gas-aerosol relationships; final data are time-stamped with a version and status "Ratified."
- Output: final ratified dataset with calculated concentrations and data flags, stored in a standardised template.

## Data structure and metadata
- Each row represents one month of data for a single site.
- Key fields include:
  - site_id, site_name, network_id
  - parameter_id (alpha_NH3_g)
  - measurement_start_date, measurement_start_time
  - measurement_end_date, measurement_end_time
  - measurement (NH3 concentration, µg NH3 m-3)
  - Less_than (LOD flag; 0 = above LOD, 1 = below LOD)
  - verification_id (verification status)
  - Unit_id (µg m-3)
  - Data_capture (0 = missing/rejected, 100 = accepted)
  - Validity_id (1 = valid, -1 = invalid)
  - EMEP_code (data status flags)
  - MONTH, YEAR
  - Comments (manual flags)
- Data flags follow EBAS/EMEP conventions (V = valid, I = invalid, M = missing); Group classifications include missing, mechanical/chemical problems, extreme values, and co-located data indicators.
- Coordinates are provided with limited precision (2 decimals) for confidentiality.

## Data flags, provenance, and interoperability
- EBAS/EMEP flag system used to indicate data quality and issues; flags cover sampling issues, contamination, instrument problems, and data validity.
- Data are harmonised with other UK-NNAM/NAMN datasets for consistency and cross-network comparability.
- The dataset references standard methods and models (EN 17346, FRAME, CBED) and provides links to flag definitions and supporting materials.

## Access, governance, and reuse considerations
- Data are prepared for robust sharing and archival (ratified, time-stamped, version-controlled).
- The NI data include confidentiality considerations for site coordinates; data sharing should respect these restrictions and flag metadata accordingly.
- When reusing the data, practitioners should cite the NAMN/ALPHAoi methodology, QA/QC workflow, and EBAS/EMEP flag semantics to ensure proper interpretation of quality levels and limitations.

## References and resources
- EN 17346 (2020): Ambient air – Standard method for determination of NH3 using diffusive samplers.
- NAMN/ALPHA DELTA methodology and field protocols (NAMN information portal).
- FRAME, CBED modelling frameworks and deposition concentration references.
- EBAS/EMEP data flags and documentation for data quality flags.