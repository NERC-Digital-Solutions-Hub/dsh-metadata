# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

## Context and purpose
- Ammonia-sensitive peatland ecosystem at Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
- Monitoring motivated by concern that NH3 emissions from local poultry livestock installations may affect Ballynahone Bog.
- Local site operator: Ulster Wildlife Trust (UWT); analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.
- Objective: obtain spatially distributed ammonia concentrations along a transect through the bog to inform environmental health assessment and policy decisions.

## Measurement approach and protocol
- Instrumentation: CEH ALPHA® passive samplers using citric acid coated filters to capture NH3.
- Deployment: replicates mounted on shelters on poles at about 1.5 m above ground; samplers exposed in monthly cycles (beginning of each month).
- Analysis: samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetric analysis.
- Dose-to-air conversion: concentration in air estimated using sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Units: ammonia concentration reported in micrograms NH3 per cubic meter of air (µg NH3 m-3).

## Data quality, validation, and handling
- Data quality checks implemented to ensure reliability:
  - Coefficient of variation (replicates) threshold: CV < 15% deemed acceptable; if CV > 15%, evaluation of replicates for discarding or validation; otherwise data flagged as valid (103).
  - Missing samplers: encoded as -9999.00 and invalid (-1).
  - Sampling duration discrepancies: samplers left on for longer/shorter periods flagged.
  - Local contamination or influences: site operator notes reviewed; suspected contaminants may lead to discarding affected samples; final site data averaged from remaining valid results.
- Data flags: final dataset includes validity and quality flags per measurement; references to EMEP data status codes and detailed flagging rules.
- Data curation outcome: final dataset named UWT_Ballynahone_Bog_Data_2018.csv contains accepted data values with appropriate flags; some raw data excluded due to improper exposure or adverse weather.

## Data structure and contents
- Dataset composition: each row corresponds to one month of data for a single site; columns include:
  - Site name, start and end dates of exposure, ammonia concentration for exposure period (µg NH3 m-3), and a data flag.
  - Additional metadata fields: unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g), exposure start/end dates and times, measurement value, detection limit indicator, verification status, unit_id (µg NH3 m-3), data capture percentage, validity flag, and EMEP status code.
- File format and metadata schema are designed to support traceability from measurement to reported concentration, including the provenance and quality status of each data point.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date for all sites: 01/09/2014; End date: Ongoing.
  - Geographic coordinates and measurement context:
    - Latitude and longitude provided for each site.
    - Height of air inlet above ground: 1.5 m.
- The dataset covers data across eight transect sites within Ballynahone Bog.

## Data governance, openness, and relevance to monitoring frameworks
- Emphasis on data governance: clear procedures for data quality assurance, flagging, and sharing of underlying data where appropriate.
- Metadata completeness and data provenance are central to the monitoring framework, addressing barriers such as data gaps, inconsistent metadata, and data sharing constraints.
- The documented approach demonstrates practical implementation of:
  - Stakeholder engagement to determine useful measures.
  - Verification and validation steps to ensure data reliability.
  - Transparent reporting through structured datasets and flagging to aid interpretation and reproducibility.
- For monitoring framework considerations: highlights how to balance data quality with timely access, manage data silos, ensure metadata adequacy, and maintain data governance standards across monitoring programs.