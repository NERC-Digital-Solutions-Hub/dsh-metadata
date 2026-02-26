# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Overview
- Data from a transect through Ballynahone National Park, an Area of Special Scientific Interest (ASSI/SAC) and Ramsar site in Northern Ireland.
- Purpose: assess NH3 emissions impacts on Ballynahone Bog, an ammonia-sensitive peatland; local operator is Ulster Wildlife Trust (UWT) and analysis is by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Sampling context: monthly exposure along a transect to measure ambient ammonia concentrations.

## Methods and Data Collection
- Sampling equipment: UKCEH ALPHA passive samplers using a citric acid coated filter and PTFE membrane; samplers mounted at ~1.5 m height on shelters.
- Replication: replicate samplers used at each site to improve reliability.
- Exposure schedule: samplers exposed in monthly cycles at the beginning of each month.
- Analysis workflow:
  - Exposed samplers extracted into deionised water.
  - Analyzed using SEAL AA3 colorimetry to determine ammonium concentration.
  - Ammonia concentration in air calculated from ammonium concentration using a calibration uptake rate of 0.003241315 m3 h-1 (2020 calibration) and exposure duration.
- Data handling:
  - Raw data quality assessed with predefined rules and data flagged if concerns arose (see Flags and Quality Assurance).

## Data Structure and Content
- Dataset: UWT_Ballynahone_Bog_Data_2020.csv
- Row structure: each row represents one month of data for a single site.
- Key columns (examples and meanings):
  - Site name, unique site identifier, network_id (RSW)
  - Parameter_id (type of measurement: alpha_NH3_g)
  - Measurement start date/time and measurement end date/time (exposure period)
  - Measurement (concentration) in micrograms per cubic metre (µg NH3 m-3)
  - Less than flag (indicates if value is below detection limit)
  - Verification id (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status and flags)
  - Month-Year (exposure period)
- Data flags:
  - 103: valid using replicates after quality checks (CV < 15%)
  - Values > calibration range may be retained if re-analysis was not possible
  - -9999 in a field indicates missing measurement or missing metadata required to compute concentration
- EMEP Flags: extensive set of codes indicating data capture status, validity, and reasons (e.g., contamination, below detection limit, sampling irregularities, nearby influences). Specific codes provide context for data quality decisions.

## Site Information
- Ballynahone bog_1 through Ballynahone bog_8
- Start date for all sites: 01/09/2014; End date: Ongoing
- Coordinates and setup:
  - Latitude and Longitude provided for each site
  - Height of air inlet above ground: 1.5 m
- Site naming and identifiers mapped to a single transect dataset for longitudinal ammonia monitoring.

## Quality Assurance and Governance
- Data provenance:
  - Data collection managed by Ulster Wildlife Trust (UWT)
  - Analysis conducted by UKCEH Edinburgh
- Quality assurance rules:
  - Coefficient of variation (replicates) calculated; CV < 15% supports validity
  - If CV > 15%, replicates may be discarded if justified; otherwise dataset flagged but may remain valid (103)
  - Some measurements may exceed calibration range; retained as valid if re-run or dilution not possible
  - Missing data indicated by -9999 and excluded from concentration calculations
- Documentation and metadata:
  - Final dataset includes explicit flags and metadata fields to support traceability and reuse
  - Detailed column descriptions and site information are included to facilitate discovery and proper interpretation

## Usage Considerations for Data Stewardship
- Ensure ongoing governance for updates: data sharing, recalibration events, and methodological updates should be captured in metadata and EMEP flags.
- Maintain linkages between site-level metadata (locations, install height) and the monthly concentration data for reproducibility.
- Be mindful of data quality flags when using the data for analysis, trend assessment, or regulatory reporting; consult the EMEP flag meanings and QA rules for interpretation.
- Document any changes in measurement methodology, uptake rates, or analysis procedures that may affect longitudinal comparability.

## Provenance and Contacts
- Operators: Ulster Wildlife Trust (site management)
- Analysis and data processing: UK Centre for Ecology and Hydrology (Edinburgh)
- Dataset reference: Ballynahone_Bog_Data_2020 (monthly NH3 concentration data with QA flags)