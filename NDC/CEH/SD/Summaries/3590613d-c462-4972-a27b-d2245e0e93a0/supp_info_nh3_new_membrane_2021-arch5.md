# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

## Overview
- Report of initial results validating a new PTFE membrane for ALPHA® ammonia samplers, prepared and analysed across UKCEH Edinburgh with local site operators from UKCEH, AFBI (Hillsborough), and Ricardo AEA (Chilbolton).
- Samplers measure NH3 in air via citric acid coated filters protected by a white PTFE membrane, deployed at ~1.5 m height in replicated units for reliability.
- Analysis is performed by SEAL AA3 colorimetry after extracting samplers into deionised water; ammonia concentration in air is derived from measured ammonium and a calculated uptake rate for the new membrane.
- Uptake rate for new membranes: 0.0039701 m3 h-1 (based on three sites; Hillsborough excluded due to unreliable exposure times).
- The dataset and accompanying metadata undergo quality assessment and flagging to indicate data quality and any issues.

## Methods and Data Processing
- UKCEH ALPHA® sampler setup:
  - Citric acid coated filter captures NH3; PTFE membrane allows diffusion; membrane oriented downwards during exposure.
  - Replicates used to improve reliability; exposed monthly at site shelters on poles.
- Analysis workflow:
  - Exposed samplers extracted into deionised water and analysed with SEAL AA3 to determine ammonium concentration.
  - Ammonia in air calculated from ammonium concentration using the new membrane uptake rate and exposure duration.
- Data documentation and structure:
  - Final dataset NH3_New_Membrane_2021.csv contains accepted data with appropriate flags.
  - Each row represents one month of data for a single site; columns include site name, exposure period start/end, ammonia concentration, and a data flag.
  - Columns cover site identifier, site name, network_id (RSW), parameter_id (alpha_NH3_g), measurement start/end dates and times, concentration, detection limit indicator, verification status, unit id, data capture percentage, validity, EMEP code, Month-Year, and comments.
- Data flags and quality rules:
  - Data flagged for various issues; key QA rules include:
    - Coefficient of Variation (CV) of replicates < 15%: considered valid (flag 103 if valid and representative).
    - Values above calibration range but deemed valid due to inability to re-run: still considered valid.
    - Missing data or missing metadata marked as -9999 (cannot calculate concentration).
  - Final dataset includes site names, spatial identifiers, and month-level records with associated data flags.
- Data capture and validity codes:
  - EMEP-related flags and data status codes define calibration, contamination, replication quality, and validity (e.g., 999: missing capture; 781/780: below detection/estimation; various codes for sampling period representativeness; 103: CV issue; 460/653/652/651: contamination or nearby activity).
  - Site data capture and validity flags provide a structured approach to data quality adjudication.

## Data Quality and Flagging
- Data have been flagged to indicate concerns; detailed flags and their meanings are provided within the dataset (including CV-based validity, calibration range status, and metadata completeness).
- Site operator and laboratory notes are used to justify retaining or discarding replicates.
- Flags also capture data capture percentage and verification status to support downstream data governance and discovery.

## Dataset Structure and Contents
- Dataset name: NH3_New_Membrane_2021.csv
- Each row: one month of data for a single site.
- Core fields:
  - Site name and unique site identifier
  - Network ID (RSW)
  - Parameter ID (alpha_NH3_g)
  - Measurement start and end dates and times
  - Ammonia concentration (µg NH3 m-3)
  - Detection limit indicator and data flag
  - Verification ID and unit ID
  - Data capture percentage
  - Validity flag (1 = valid, -1 = not valid)
  - EMEP flag codes and related narratives
  - Month-Year and optional comments
- Units: all concentration data are in micrograms of NH3 per cubic metre of air (µg NH3 m-3).

## Site Information and Uptake Rates
- Four sampling sites with uptake-rate details:
  - Edinburgh uptake rate OTC: start 01/03/2020; end ongoing; coordinates 55.863150, -3.209845; inlet height 1.5 m; collocated with UKA00128
  - Auch uptake rate: start 01/03/2020; end ongoing; coordinates 55.792160, -3.242900; inlet height 1.5 m; collocated with UKA00451
  - Hills uptake rate: start 01/03/2020; end ongoing; coordinates 54.452500, -6.083340; inlet height 1.5 m; collocated with UKA00293
  - Chilbolton uptake rate: start 01/01/2021; end ongoing; coordinates 51.149617, -1.438228; inlet height 1.5 m; collocated with UKA00614
- This uptake-rate information is used to convert sampler-derived ammonium measurements into ambient NH3 concentrations; the Hillsborough site was excluded from uptake-rate calculations due to unreliable exposure times.

## Implications for Data Stewardship
- Multi-institution collaboration across sampling, analysis, and data curation necessitates clear provenance and metadata tagging (site, network, parameter, uptake rate, and verification status).
- Detailed QA rules and EMEP flags support transparent data quality assessment and enable informed reuse.
- Metadata should capture the new membrane validation context, uptake-rate derivation, and site-specific operational notes to ensure accurate interpretation of NH3 concentrations.
- Data discovery and sharing should reference the NH3_New_Membrane_2021.csv file and its accompanying flag documentation, ensuring users understand the data flags, validity criteria, and potential limitations (e.g., calibration-range issues, CV filtering).
- Ongoing governance should maintain updated uptake-rate values and site information, particularly where new membrane validation affects uptake calculations.