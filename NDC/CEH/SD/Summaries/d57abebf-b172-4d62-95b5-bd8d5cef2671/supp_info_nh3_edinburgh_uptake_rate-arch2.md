# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2022

## Purpose and scope
- Report of initial results to determine the uptake rate for ALPHA samplers used to measure NH3 in air across UK climates.
- Four UK UKEAP network sites involved; local duties by UKCEH, AFBI Hillsborough, and Ricardo AEA; analysis by CEH Edinburgh.
- Samplers deployed in monthly exposure cycles at the beginning of each month; data prepared for UK-wide monitoring and comparison.

## UKCEH ALPHA sampler method
- ALPHA® passive sampler uses a citric acid coated filter to capture ammonia; protected by a white PTFE (Teflon) membrane; membrane oriented downward during exposure.
- Replicate samplers mounted on a shelter at ~1.5 m above ground to improve reliability.
- Analysis: exposed samplers extracted in deionised water; ammonia quantified by SEAL AA3 colorimetry; results converted to ambient NH3 concentration using a known uptake rate (0.0038422 m3 hr-1) and exposure duration.
- Data flagged for concerns; quality checks and flags documented (see data rules).

## Data handling and quality assurance
- Raw data quality-checked against predefined rules:
  - Coefficient of variation (CV) of replicates < 15% deemed valid; if >15%, replicates reviewed and may be discarded; valid data flagged as 103.
  - Data exceeding calibration range but considered valid if remeasurement/dilution was not possible due to instrument failure.
  - Missing data or meta-data indicated by -9999; incomplete date/time prevents calculation.
- Final dataset: submissions_ED_UR_NH3_2022.csv containing accepted values with appropriate flags; columns include site ID, site name, network_id (ED_UR), parameter_id (alpha_NH3_g), measurement start/end (dates and times), ammonia concentration (µg NH3 m-3), detection flags, verification status, unit code (24 = µg NH3 m-3), data capture %, validity, EMEP code, Month-Year, and comments.
- Data status and flags align with EMEP data flag semantics, including reasons for validity, detection limits, sampling period representativeness, contamination, and other data issues.

## Dataset contents and structure
- Each row represents one month of data for a single site; columns provide the measurement period, concentration, quality flags, and metadata.
- Site identifiers and metadata are detailed in accompanying site information and flag descriptions.

## Site information and network context
- Edinburgh uptake rate OTC: start 01/03/2020; end date ongoing; coordinates 55.863150, -3.209845; air inlet height 1.5 m; collocated with UKA00128.
- Auch: start 01/03/2020; coordinates 55.792160, -3.242900; air inlet height 1.5 m; collocated with UKA00451.
- Hills: start 01/03/2020; coordinates 54.452500, -6.083340; air inlet height 1.5 m; collocated with UKA00293.
- Chilbolton: start 01/01/2021; coordinates 51.149617, -1.438228; air inlet height 1.5 m; collocated with UKA00614.

## Data governance and accessibility
- Data are generated under a collaborative framework (UKCEH, AFBI, Ricardo AEA) with analysis by CEH Edinburgh.
- Final datasets are prepared for submission to appropriate data portals; results are designed to be stored and accessible for ongoing monitoring and policy evaluation.
- Outputs are presented in standardized formats to facilitate cross-site comparisons and policy scrutiny over time.