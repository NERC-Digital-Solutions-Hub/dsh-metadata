# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

## Overview
- Data from two CSV files: NI_ALPHA_NH3_2019.csv (2019) and NI_ALPHA_NH3_2020.csv (2020).
- Monthly atmospheric NH3 concentrations measured at 25 sites across Northern Ireland (NI) using the ALPHA® passive sampler.
- Coordinated with UKCEH DELTA® measurements at 4 sites; one site co-located for inter-comparison of ALPHA® and DELTA® NH3 concentrations.
- Network operated by the Agri-Food and Biosciences Institute (AFBI) and the UK Centre for Ecology & Hydrology (UKCEH), funded by DAERA.

## Purpose and applications
- Used for model validation and calibration of atmospheric NH3 concentrations (e.g., FRAME, CBED).
- Aims to increase confidence and reduce uncertainty in NH3 modelling to assess policy scenarios.
- Hillsborough site provides onsite NH3 data to evaluate local farm emission sources.
- Spatial distribution across NI enables comparison with atmospheric transport models and supports validation of NH3 emissions inventories.

## Experimental design and sampling regime
- 25 ALPHA® sites (24 rural, 1 urban – AFBI14: Belfast centre) chosen to improve spatial coverage and spatio-temporal data across NI.
- Monthly sampling with continuous time-integrated exposure; site operators exchange samplers on a monthly cycle.
- DELTA® sites included for cross-site completeness; NI DELTA data reported in companion submission.

## Monitoring method and measurement
- NH3 measured with UKCEH high-sensitivity ALPHA® passive samplers (citric acid-coated filters) mounted ~1.5 m above ground.
- Triplicate samplers per measurement to assess precision and contamination; samples analyzed for NH4+ and converted to NH3 concentration (µg NH3 m-3).
- Annual calibrated uptake rates used to convert exposure duration to sampled air volume:
  - 2019: 0.0031665 m3 h-1
  - 2020: 0.0031277 m3 h-1
- Limit of detection (LOD) is 0.03 µg NH3 m-3 (monthly exposures).

## Data collection, processing and quality control
- Data are stored in an Oracle-based AAGA database and processed via a ShinyApp to compute NH3 concentrations.
- Quality control follows a three-stage process:
  - Stage 1: automated checks with EBAS-like data flags (date overlaps, typical monthly duration ±5 days, replicate CV >15% flagged, outlier rejection, handling missing samples).
  - Stage 2: manual review of laboratory blanks, sampling malfunctions, outliers, and contamination indicators.
  - Stage 3: expert/project manager review considering site knowledge, expected patterns, co-located measurements, and year-to-year/site comparisons.
- Final output is a time-stamped, version-controlled ratified dataset.

## Data structure and content
- Each row represents one month of data for a single site.
- Key fields (examples):
  - site_id, site_name, network_id (AFBI), parameter_id (alpha_NH3_g)
  - measurement_start_date/time, measurement_end_date/time
  - measurement (NH3 concentration, µg NH3 m-3)
  - Less_than (flag for values below LOD)
  - verification_id (Not verified, Preliminary verified, Verified)
  - unit_id (µg m-3), data_capture (0 missing/rejected, 100 accepted), validity_id (1 valid, -1 invalid)
  - EMEP_code (data status and flags)
  - MONTH, YEAR, Comments
- Site coordinates are provided (to two decimal places for confidentiality).

## Data flags and quality status
- Data flagged using EMEP/EBAS flag system, grouped into:
  - Group 0: Valid data
  - Group 1–9: Various exceptions (invalid, missing, contamination, instrumental issues, sampling anomalies, etc.)
- Examples of flags:
  - 798, 780, 771, 654, 653, 103 (CV of replicates >15%), 652/651 (nearby activity), 620 (filter issues), 699/669 (instrument/mechanical problems)
  - 147 (value at or near detection limit with reporting), 147 if valid
  - 000: Valid measurement
- Flags align with EBAS/NAMN conventions to facilitate harmonised submissions and cross-network comparisons.

## Related standards and resources
- EN 17346 (2020): Ambient air – standard method for NH3 determination using diffusive samplers.
- NAMN/NAMN-related documentation and UKCEH protocols for ALPHA® and DELTA® NH3 monitoring.
- FRAME model and CBED deposition modeling references for NH3.
- EBAS flag list and data submission guidelines for Europe-wide comparability.

## Notes and considerations
- COVID-19 impacted sampling during Apr–Jun 2020 with extended exposure periods; such data are flagged accordingly.
- The dataset provides a comprehensive, quality-assured basis for evaluating NH3 emissions and atmospheric concentrations, with detailed provenance, QA/QC, and data flags to support reuse and model validation.