# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

- Purpose and scope
  - Initial results to determine uptake rate for ALPHA® passive samplers for measuring atmospheric NH3 in UK climates.
  - Measurements conducted at four UKEAP network sites; local site operator duties shared among UKCEH, AFBI, and Ricardo AEA; analysis by CEH Edinburgh.
  - Samplers exposed in monthly cycles at the start of each month.

- UKCEH ALPHA® sampler method
  - Passive sampler using a citric acid coated filter to capture ammonia; protected by a white PTFE membrane facing downwards during exposure.
  - Exposed samplers mounted on shelters on posts at ~1.5 m above ground; replicates used for reliable NH3 estimation.
  - Samplers provided in protective plastic containers.

- Analysis workflow
  - Exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 via colorimetry.
  - NH3 in air estimated from sampler NH4+ concentration using a known uptake rate of 0.003241315 m3 h-1 and exposure duration.

- Data quality assurance and flags
  - Raw data quality assessed with predefined rules:
    - Coefficient of variation (replicates) < 15% to consider the data valid; otherwise replicates may be discarded.
    - Some samples exceed calibration range but are still deemed valid.
    - Missing data or metadata are coded as -9999 where concentration or date/time metadata are unavailable.
  - Data and metadata quality flags align with EMEP/NILU flags, enabling transparent interpretation of validity, detection limits, and data issues.
  - The final dataset (NH3_Edinburgh_Uptake_Rate_2021.csv) contains accepted values with appropriate flags; includes site identifiers and a data capture percentage.

- Dataset structure and content
  - Each row represents one month of data for a single site.
  - Columns include: site name, site unique identifier, network id, parameter type, measurement start/end dates and times, ammonia concentration (µg NH3 m-3), data capture percentage, validity flag, EMEP flag, month-year, and comments.
  - Data capture and validity statuses (e.g., verified, preliminary verified, not verified) are recorded, along with data status codes and reasons for flags.

- Site information and collocation
  - Sites: Edinburgh uptake rate OTC, Auch, Hills, Chilbolton.
  - For each site: start date of uptake rate measurement (ranging from 2020 to 2021), ongoing end date, precise latitude/longitude, 1.5 m air-inlet height, and collocation notes (e.g., collocated with UKA identifiers).

- Data governance and accessibility
  - Emphasis on data transparency, with explicit recording of metadata, replicate quality, and flagging for data validity.
  - Underlying data and flags are designed to support scrutiny, reuse, and comparability in monitoring frameworks; detailed metadata and flag explanations align with standard environmental data governance practices.
  - Data tables and flags referenced (e.g., EMEP flags) support integration with broader air quality and policy monitoring dashboards and reports.