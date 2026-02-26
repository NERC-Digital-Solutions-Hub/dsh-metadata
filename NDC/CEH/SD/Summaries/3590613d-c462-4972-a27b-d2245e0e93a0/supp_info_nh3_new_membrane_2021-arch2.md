# Monthly ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, new membrane validation, 2021

## Overview
- Initial results from validating a new PTFE membrane for ALPHA® passive ammonia samplers.
- Study conducted at four UK UKEAP network sites in 2021, with monthly exposure cycles.
- Data preparation, analysis, and quality assurance managed by UKCEH Edinburgh and partners (AFBI Hillsborough, Ricardo AEA Chilbolton).

## Methods and approach
- Instrument and sampler: UKCEH ALPHA® passive samplers with citric acid coated filters and a PTFE membrane; membrane mounted facing downwards; exposed ~1.5 m above ground on shelters.
- Sampling design: replicate samplers deployed to improve reliability; exposed in monthly cycles at the start of each month.
- Analysis: exposed samplers eluted in deionised water; NH3 determined by SEAL AA3 colorimetric analysis; results converted to average ambient NH3 concentration using uptake rate.
- Uptake rate: new membrane uptake rate set at 0.0039701 m3 h⁻¹; calculated using data from three sites; Hillsborough excluded due to unreliable exposure times.
- Data handling: data flagged and quality assured; final dataset NH3_New_Membrane_2021.csv contains accepted values with appropriate flags; site metadata includes coordinates and collocation information.

## Data products and structure
- Final dataset: NH3_New_Membrane_2021.csv
  - Key fields include: site id, site name, network_id, parameter_id, measurement start/end dates and times, ammonia concentration (µg NH3 m⁻³), data capture %, verification status, unit id, data validity flag, EMEP/status codes, Month-Year, and comments.
- Data units and interpretation:
  - Ammonia concentration expressed as micrograms of NH3 per cubic metre of air (µg NH3 m⁻³) for the specified exposure period.
- Data flags and quality rules:
  - CV of replicates < 15% used to deem data valid; if CV > 15%, replicates reviewed or discarded.
  - Some values exceeding calibration range deemed valid due to instrument limitations or data loss.
  - Missing data indicated with -9999 in the measurement field.
  - EMEP flags provide detailed data status (e.g., verification status, data issues, and validation reasoning).
  
## Quality assurance and validation
- Data are flagged to highlight concerns; thorough QA assessed against:
  - Replicate precision (CV)
  - Calibration range considerations
  - Completeness of measurement and meta-data
- Final dataset entries are categorized as valid or not valid with corresponding reasoning codes.
- Raw data and meta-data accompany the final dataset to support traceability and re-use.

## Site information and network context
- Four sites with uptake-rate metadata and coordinates:
  - Edinburgh uptake rate: start 01/03/2020; ongoing; lat 55.863150, lon -3.209845; 1.5 m inlet height; collocated with UKEAP UKA00128.
  - Auch: start 01/03/2020; ongoing; lat 55.792160, lon -3.242900; 1.5 m inlet height; collocated with UKEAP UKA00451.
  - Hillsborough: start 01/03/2020; ongoing; lat 54.452500, lon -6.083340; 1.5 m inlet height; collocated with UKEAP UKA00293.
  - Chilbolton: start 01/01/2021; ongoing; lat 51.149617, lon -1.438228; 1.5 m inlet height; collocated with UKEAP UKA00614.
- Context: part of the UKEAP network, with uptake-rate calculations used to convert sampler results to ambient NH3 concentrations; Hillsborough data excluded from uptake-rate calculation due to timing issues.

## Data accessibility and future use
- The dataset is prepared for storage and upload to appropriate data portals, aligning with the aim of making underlying data accessible for broader use.
- The approach supports standardised, time-series monitoring of NH3 across multiple sites, enabling integration with other environmental datasets to enhance interpretation and policy analysis.