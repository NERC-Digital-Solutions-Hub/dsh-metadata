# Monthly atmospheric ammonia concentration data from Northern Ireland ALPHA ® Ammonia Monitoring Network, 2019-2020

- Two CSV files: NI_ALPHA_NH3_2019.csv and NI_ALPHA_NH3_2020.csv
- Source: Northern Ireland ALPHA® Ammonia Monitoring Network (NH3) with 25 sites in NI, measured monthly for 2019 and 2020
- Co-located data: NH3 data from UKCEH DELTA® method collected at 4 sites; one site co-located ALPHA® and DELTA® for inter-comparison
- Network operated by AFBI and UKCEH; funded by DAERA
- Purpose: Data used for model validation and calibration of atmospheric NH3 concentrations (e.g., FRAME) and to support deposition modelling (CBED) and policy scenario assessment

## Network and monitoring design

- 25 ALPHA® sites across Northern Ireland (24 rural, 1 urban)
- Hillsborough site included for onsite NH3 data to evaluate local farm emission sources
- 24 additional sites provide spatial coverage for comparison with atmospheric transport models
- Sites chosen to cover different emission sectors (agricultural and non-agricultural) and background conditions
- Monitoring frequency: monthly, with continuous time-integrated sampling over each period
- Site operator network managed by AFBI; sampling and exchange visits occur monthly

## Measurement method and data produced

- Instrument: UKCEH ALPHA® passive samplers (high-sensitivity for NH3)
- Sampling height: approximately 1.5 m above ground
- Sample processing: citric acid-coated filters; NH3 converted to NH4+ and analyzed by colorimetry
- Annual calibrated uptake rates used to estimate air volume sampled
  - 2019 uptake rate: 0.0031665 m3/h
  - 2020 uptake rate: 0.0031277 m3/h
- Unit of concentration: micrograms NH3 per cubic meter (µg NH3 m-3)
- Limit of detection: 0.03 µg NH3 m-3 (monthly exposures)
- Data management: stored in AAGA Oracle database; concentration calculations via ShinyApp

## Dataset structure and content

- Each row represents one site per month
- Core fields (examples):
  - site_id (e.g., AFBI01)
  - site_name (e.g., U of Ulster met station)
  - network_id (AFBI)
  - parameter_id (alpha_NH3_g)
  - measurement_start_date / measurement_start_time
  - measurement_end_date / measurement_end_time
  - measurement (NH3 concentration in µg m-3)
  - Less_than (indicator if value is below LOD)
  - verification_id (verification status)
  - Unit_id (µg m-3)
  - Data_capture (0 = missing/rejected, 100 = accepted)
  - Validity_id (1 = valid, -1 = invalid)
  - EMEP_code (data status flags)
  - MONTH / YEAR
  - Comments (site flags or notes from manual review)
- Data are time-integrated averages for the specified exposure period

## Quality control and data ratification

- Stage 1: Automated data checks in AAGA with EBAS-like flags
  - Date overlaps and calendar-month exposure windows (±5 days)
  - Replicate sample CVs; flag if CV > 15% (Flag 103) but data may remain valid with higher uncertainty
  - Outlier detection against laboratory blanks
  - Missing samples assigned -9999 and marked invalid (-1)
- Stage 2: Manual data review
  - Review laboratory blanks, sampling malfunctions, potential contamination, and other issues
  - Invalidated data flagged accordingly
  - Investigate low/high outliers and sample integrity
- Stage 3: Expert/Project manager review
  - Site knowledge, modelling context, expected temporal patterns, inter-site comparisons
  - Co-located DELTA measurements and cross-year/site comparisons considered
- Outcome: Final ratified dataset with time-stamped output and versioning; data flagged as appropriate

## Data flags and reporting

- Data flags follow EBAS/EMEP conventions; grouped as:
  - V: Valid measurement
  - I: Invalid measurement
  - M: Missing measurement
- Representative examples of flags used (summarised categories):
  - Missing or uncertain data, sampling period anomalies, or representativeness flags
  - Mechanical or chemical issues (e.g., filter or instrument problems)
  - Contamination indicators or data less accurate due to field/blank conditions
  - Values below detection limits or near limits (with appropriate notes)
- Final ratified data are stored in a standardised template, time-stamped, with version control

## GIS and data usage considerations

- Spatial coverage: 25 NI sites provide a useful grid for mapping NH3 concentrations and spatial patterns
- Coordinate precision: site coordinates reported to 2 decimal places for confidentiality
- Temporal resolution: monthly concentrations suitable for trend analysis and validation of NH3 transport and deposition models
- Applications for GIS specialists:
  - Create monthly NH3 concentration maps and identify hot spots or emission-source influences
  - Validate and calibrate atmospheric transport models (e.g., FRAME) using observed NH3
  - Support concentration-based deposition estimates (CBED) and policy scenario analyses
  - Compare ALPHA® NH3 data with co-located DELTA® measurements for cross-method validation

## References and supporting information

- EN 17346 (2020): Ambient air - Standard method for NH3 determination using diffusive samplers
- Publications on ALPHA®/DELTA® methods and NH3 monitoring
- Data submission context: EBAS data flags and UK NAMN coordination
- Frameworks and models referenced: FRAME, CBED
- Resources:
  - NAMN information and NH3 modelling portals
  - EBAS flag documentation and data submission guidelines

## Access and provenance

- Data originate from the NI ALPHA® NH3 Monitoring Network (AFBI & UKCEH)
- Processed via the AAGA database and ShinyApp for concentration calculations
- Final dataset includes all months and sites with appropriate flags and verification status
- Companion DELTA® data and cross-network comparisons are reported in related submissions