# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

- Purpose and scope
  - Presents initial results from validating a new PTFE membrane for ALPHA® passive samplers used to measure atmospheric ammonia (NH3) at four UK UKEAP sites in 2021.
  - Sampling conducted in monthly exposure cycles; analysis performed at UKCEH Edinburgh with local site operators and partner staff.

- Sampling method and measurement approach
  - UKCEH ALPHA® sampler: passive device with a citric acid coated filter to capture NH3; protected by a white PTFE membrane facing downwards during exposure.
  - Samplers mounted ~1.5 m above ground on shelters; replicate samplers used per site for reliable concentration estimates.
  - Analysis: exposed samplers extracted into deionised water and analyzed by SEAL AA3 using colorimetry to determine ammonium concentration.
  - NH3 in air calculation: convert ammonium concentration to average NH3 in air using a site-specific uptake rate for the new membrane (0.0039701 m3 hr-1). Uptake rate calculated from three sites; Hillsborough excluded due to unreliable exposure times.

- Data quality, flags, and validation rules
  - Data are flagged for concerns; details provided in accompanying documentation.
  - Quality rules applied to raw data:
    - Coefficient of variation (CV) of replicate samplers: if CV < 15%, data considered valid (flag 103). If CV > 15%, replicates reviewed; still may be valid if representative.
    - Data beyond calibration range can be valid if re-measurement was not possible due to instrument issues.
    - Missing data are encoded as -9999 for the measurement or metadata fields.
  - Final dataset NH3_New_Membrane_2021.csv contains accepted measurements with appropriate data flags; includes site identifiers and spatial metadata.

- Dataset structure and contents
  - Each row corresponds to one month of data for a single site.
  - Columns cover:
    - Site identifier (site id), site name, network_id (RSW), parameter_id (alpha_NH3_g)
    - Measurement period: measurement start date/time and end date/time (exposure period)
    - Measurement: ammonia concentration (µg NH3 m-3)
    - Less than flag (below detection limit or not)
    - Verification id (data verification status)
    - Unit id (µg NH3 m-3)
    - Data capture (% of data successfully recorded)
    - Validity_id (1 = valid, -1 = not valid)
    - EMEP code (data status and flags)
    - Month-Year of measurement
    - Comments (data notes)
  - Concentrations are reported as the average NH3 concentration for the specified exposure period.

- EMEP flags and data notes
  - EMEP flag patterns are documented (e.g., data capture, validity, and reasoning for data status such as contamination, low detection, or observational considerations).
  - Flags cover issues like missing data, detection-limit related values, and various local influences (e.g., contamination, nearby activity).

- Site information and uptake-rate context
  - Four uptake-rate sites with coordinates and details:
    - Edinburgh uptake rate (OTC): start 01/03/2020; ongoing; lat 55.863150, lon -3.209845; 1.5 m inlet height; collocated with UKA00128
    - Auch uptake rate: start 01/03/2020; ongoing; lat 55.792160, lon -3.242900; 1.5 m inlet height; collocated with UKA00451
    - Hillsborough uptake rate: start 01/03/2020; ongoing; lat 54.452500, lon -6.083340; 1.5 m inlet height; collocated with UKA00293
    - Chilbolton uptake rate: start 01/01/2021; ongoing; lat 51.149617, lon -1.438228; 1.5 m inlet height; collocated with UKA00614
  - Hillsborough (Hills) excluded from uptake-rate calculations due to unreliable exposure times in many valid data periods.
  - Each site is described with its geographic coordinates and operational details for GIS linking and spatial analyses.

- Practical guidance for GIS and data users
  - Use site_id, site_name, and network_id to join NH3 data to spatial layers containing coordinates and site attributes.
  - Leverage the Month-Year field to create time-series maps and trend analyses across the four sites.
  - Consider data quality flags (e.g., CV-based 103, -9999 missing data, and EMEP/validity codes) when filtering data for map visualizations or analyses.
  - Incorporate the uptake-rate context as a spatial attribute to interpret concentration measurements in relation to membrane performance and exposure conditions.

- Endnotes and data provenance
  - Data produced by UKCEH Edinburgh with contributions from AFBI Hillsborough and Ricardo AEA Chilbolton; analysis by CEH Edinburgh.
  - The dataset and methodology document outline the data processing, quality checks, and dataset contents for reproducibility and GIS applications.