# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2022

## Overview
- Purpose: Report initial results from validating a new PTFE membrane for ALPHA® passive ammonia samplers used to monitor NH3 in air across four UKEAP network sites in the UK.
- Organizations involved: UKCEH Edinburgh (analysis), local site operators UKCEH Edinburgh, AFBI Hillsborough, Ricardo AEA Chilbolton.
- Sampling cadence: Samplers exposed in monthly cycles at the start of each month.

## Method (ALPHA® Sampler and Membrane)
- Sampler design: UKCEH ALPHA® passive sampler with a citric acid coated filter to capture NH3, protected by a white PTFE membrane (diffusion barrier) facing downwards during exposure.
- Deployment: Replicate samplers mounted on a shelter on a pole at about 1.5 m above ground.
- Analysis workflow: Exposed samplers are extracted in deionised water; NH3 is measured by SEAL AA3 (colorimetry). NH3 concentration in air is derived using the sampler-specific uptake rate for the new membrane (0.0041741 m3 hr-1) and exposure duration.
- Data handling: Raw data quality-checked and flagged as needed (see Data QC).

## Data Processing and Quality Assurance
- Primary QC rule: Coefficient of variation (CV) of replicates < 15% to consider the replicate set reliable; otherwise replicates may be discarded and data flagged (result considered valid if the mean is representative).
- Calibration limitation: Some values exceed calibration range but are still considered valid when dilution/reanalysis isn’t possible due to instrument failure or sample loss.
- Missing data handling: Missing measurement identifiers or time data are recorded as -9999; these values cannot be calculated.
- Final dataset: NH3_New_Membrane_2022.csv contains accepted data values with appropriate flags; includes per-site monthly measurements with site name, exposure start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.

## Dataset Structure and Content
- Columns include: site_id, site_name, network_id (NM), parameter_id (alpha_NH3_g), measurement start/end dates and times, ammonia concentration (µg NH3 m-3), data capture percentage, verification status, unit_id (24 = µg NH3 m-3), Data status/EMEP codes, Month-Year, and Comments.
- Data status and flags: EMEP flag fields used to indicate data quality and context (see below for common examples).

## Flags and Codes
- Data capture and validity: Flags indicate whether data were captured, verified, and deemed valid or not.
- Common examples (EMEP Flags and interpretations):
  - 999: Data capture = 0; Valid/Invalid = -1; Reasoning = Missing measurement.
  - 781: Data capture = 0; Valid/Invalid = 1; Reasoning = Value below detection limit (reported as detected).
  - 780: Data capture = 0; Valid/Invalid = 1; Reasoning = Below detection or quantification limit (estimated or measured value).
  - 103: CV of replicate ALPHA samplers > 15%; Valid measurement.
  - 660–668, 647, 646, 645, 655, 652, etc.: Various contextual reasons (e.g., local influences, contamination, nearby activities) with valid measurements.
- Site-specific nuances: Flags also reflect data capture quality, local interferences (traffic, agricultural activity, industrial contamination), and sampling conditions.

## Site Information and Layout
- Sites monitored (Edinburgh uptake rate network): 
  - OTC
  - Auch
  - Hills
  - Chilbolton
- Each site details:
  - Start date: OTC, Auch, Hills (01/03/2020); Chilbolton (01/01/2021).
  - Coordinates (latitude/longitude) and 1.5 m inlet height above ground.
  - Collocated with UKEAP site codes (e.g., UKA00128, UKA00451, UKA00293, UKA00614).
  - Additional details: Uptake rate context and ongoing status; location metadata for spatial analyses.

## Roles and Responsibilities
- Data collection and site operation: UKCEH Edinburgh, AFBI Hillsborough, Ricardo AEA Chilbolton.
- Analysis: Centre for Ecology and Hydrology Edinburgh.
- Data stewardship: Final dataset compiled with a clear schema, flags, and site metadata to enable standardised analyses and portal submission.

## Key Takeaways for Monitoring and Analysis
- Standardised, replicable NH3 measurement workflow using ALPHA® samplers and a validated PTFE membrane.
- Comprehensive quality controls ensure data reliability across replicated samplers and across sites.
- Transparent data structure with explicit flags and metadata facilitates reuse, comparison, and policy-relevant interpretation.
- Four Edinburgh-area sites provide spatially distributed NH3 monitoring data within the UKEAP framework for 2022, with ongoing data collection and updates to uptake-rate parameters as membrane validation continues.