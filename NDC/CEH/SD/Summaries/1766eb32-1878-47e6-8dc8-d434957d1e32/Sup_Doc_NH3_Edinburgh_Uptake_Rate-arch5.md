# Sup_Doc_NH3_Edinburgh_Uptake_Rate

## Overview
- Study to determine uptake rate for ALPHA® samplers used to measure ammonia (NH3) in air in the UK, specifically Edinburgh Climate and Ecosystem Change (CEH) site and Hillsborough (AFBI).
- Samplers exposed monthly; first-year data not used for uptake rate due to COVID-19 data losses and insufficient points for calibration.
- Analysis workflow: passive CEH ALPHA® samplers with citric acid coated filters; NH3 captured and later analysed via SEAL AA3 colorimetry; ammonia concentration in air computed using a known uptake rate (0.003241315 m3 hr-1) and exposure duration.
- Data flagged for quality concerns; final dataset NH3_Edinburgh_Uptake_Rate_2020.csv contains accepted values with appropriate flags.

## Data Collection and Methodology
- Sampling system: replicate CEH ALPHA® samplers mounted on shelters at ~1.5 m above ground.
- Analysis: samplers extracted into deionised water and analysed by SEAL AA3; concentration of ammonium converted to NH3 in air.
- Uptake rate used to convert exposure to average air concentration.
- Data management: there is explicit flagging for data concerns; page 4 contains details of flagged data.

## Data Structure and Contents
- Final dataset: NH3_Edinburgh_Uptake_Rate_2020.csv.
- Each row represents one month of data for a single site; columns include:
  - Site name and unique site identifier
  - Network_id (RSW)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end date and start/end time (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Data flag and related fields (e.g., less than detection limit, validation status, unit id)
  - Data capture percentage and validity status
  - EMEP data status code and Month-Year
  - Comments field for data notes
- Units: ammonia concentration in µg NH3 m-3; all data capture and validity fields align with UK-AIR/EMEP conventions.

## Data Quality and Validation Rules
- Quality control applied to raw data:
  - Coefficient of variation (CV) of replicates must be less than 15% for reliable site operation; if CV > 15%, replicates may be discarded but data may still be considered valid and flagged as 103.
  - Some data may be out of calibration range but still deemed valid due to instrument failure or sample loss (flagged as valid despite range).
  - Missing data are indicated by -9999 in the measurement field or missing metadata required to compute concentrations.
- Final dataset includes only data values accepted as valid, with appropriate flags.

## Data Flags and Codes
- Data flags in the dataset indicate data quality and processing status:
  - 103: Valid measurement with CV of replicates >? Actually CV check; flagged as valid with replicates considered representative.
  - 2: Data or metadata missing or incomplete (e.g., missing calculation-ready fields).
  - 1: Verified or validated status.
  - -1: Not valid or invalid data.
- EMEP flags accompany data status to indicate measurement issues, contamination, timing of sampling, nearby activities, and other contextual factors.
  - Examples include codes indicating missing measurements, values below detection limit, estimated values, sampling period representativeness, contamination indicators (industrial, agricultural, dust, pollen, etc.), and other local influences.
- Additional EMEP data capture and validity fields accompany a numerous set of codes (e.g., 999, 781, 780, 654, 653, 652, 651, 260, 559, 558, 557, 556, 555, 553, 532) with corresponding explanations.

## Data Governance and Access
- Data are prepared for sharing on relevant data portals; dataset contents and structure are documented to enable reuse by researchers and data managers.
- Documentation includes measurement protocols, sampler details, calibration and uptake rate, quality assurance rules, and data flag definitions to support transparency and reproducibility.
- The dataset includes explicit notes on data acceptance, exclusions (e.g., first-year uptake rate not used), and site-level metadata to support discovery and proper interpretation.

## Site Information and Deployment Details
- Sites included in the Edinburgh uptake rate study:
  - Edinburgh uptake rate OTC (start 01/03/2020; end ongoing); coordinates 55.863150, -3.209845; inlet height 1.5 m; collocated with UKEAP UKA00128.
  - Edinburgh uptake rate Auch (start 01/03/2020; end ongoing); coordinates 55.792160, -3.242900; inlet height 1.5 m; collocated with UKA00451.
  - Edinburgh uptake rate Hills (start 01/03/2020; end ongoing); coordinates 54.452500, -6.083340; inlet height 1.5 m; collocated with UKA00293.
- Sampling and analysis are conducted by CEH Edinburgh (local site operator duties) and AFBI Hillsborough, with CEH Edinburgh performing the analysis.

## Key Limitations and Considerations
- First year uptake-rate calculation excluded due to data losses from COVID-19; calibration insufficient for robust uptake-rate calibration.
- Data users should consult the page-specific data flags and comments for site- and period-specific concerns about data validity or external influences.

## Provenance and Metadata Notes
- Dataset includes detailed metadata fields for traceability:
  - Site identifiers, network and parameter codes, precise exposure periods, concentration values, unit identifiers, data capture percentages, validity IDs, and EMEP/status codes.
  - Comments field captures site-specific data notes and data quality observations.
- Documentation references include the page for data contents, page 4 for data flags, page 5 for site names and spatial identifiers, and page 3 for dataset contents.