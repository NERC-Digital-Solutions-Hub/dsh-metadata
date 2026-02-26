# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- Field sites form a transect through Ballynahone National Park (Area of Special Scientific Interest/SAC and Ramsar site) in Northern Ireland.
- Local site operator: Ulster Wildlife Trust (UWT); analysis performed by the UK Centre for Ecology and Hydrology, Edinburgh.
- Purpose: monitor ammonia (NH3) concentrations due to potential emissions from nearby poultry livestock installations.
- Data year: 2019; samplers exposed monthly along the transect; data prepared for sharing with metadata and quality flags.

## Sampling method and analysis
- Instrument: CEH ALPHA® passive samplers with citric acid coated filters; capture of NH3 on a PTFE membrane.
- Deployment: replicates (to improve reliability) mounted on shelters at about 1.5 m above ground.
- Exposure: monthly cycles; samples collected in protective containers.
- Analysis workflow: exposed samplers extracted into deionised water and analyzed with SEAL AA3 colorimetric analyzer.
- Concentration calculation: ambient air concentration derived using a known uptake rate (0.003241315 m3 h-1) and the exposure duration.
- Data integrity: some samples were exposed incorrectly or lost due to weather; such data are flagged and not used for site estimates.

## Data quality and flags
- Quality checks applied to raw data:
  - Coefficient of variation (replicates) < 15% required for validity; if >15%, evaluation and potential exclusion of outliers; valid results flagged as 103 when considered representative.
  - Missing samplers: assigned -9999.00 and marked invalid (-1).
  - Sampler duration deviations: longer/shorter than monthly cycle flagged.
  - Local contamination or influences: flagged via site operator notes; affected samples may be discarded.
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv containing accepted values with appropriate flags.
- Data fields and flags (highlights):
  - Data status codes and EMEP flags accompany each record, indicating verification status, data issues, and quality reasoning.
  - Examples of flag reasoning include: contamination nearby, values below detection limits, sampling period duration deviations, and CV issues among replicates.
  - Detection limit handling: a flag indicates values below the limit of detection (0.03 µg NH3 m-3) or below quantification limits when applicable.
  
## Dataset contents and structure
- Final dataset name: UWT_Ballynahone_Bog_Data_2019.csv.
- Core data per row: site name, measurement start/end dates, measurement start/end times, ammonia concentration (µg NH3 m-3), and a data flag.
- Metadata and coding fields included:
  - Site and network identifiers (site name, unique site identifier, network_id BE).
  - Parameter_id indicating the measurement type (alpha_NH3_g).
  - Measurement period fields: start date/time and end date/time.
  - Result fields: concentration (µg NH3 m-3) and a “less than” flag for detection limit status.
  - Verification id (1 = Verified, 2 = Preliminary verified, 3 = Not verified) and unit id (24 = µg NH3 m-3).
  - Data capture percentage and Validity_id (1 = valid, -1 = not valid).
  - EMEP data status code with corresponding flags and reasoning.
  - Month-Year for the measurement period.
- The dataset uses standard QA/QC conventions to document data validity and provenance.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014; End date: Ongoing.
  - Coordinates (lat/long) provided for each site.
  - Height of air inlet above ground: 1.5 m for all sites.
- These eight sites form the transect through the bog, enabling spatial assessment of ammonia concentrations across the peatland ecosystem.

## Data governance, availability and usage
- Data stewardship: UWT operates the field sites; CEH conducts analysis, ensuring standardized methodology and documentation.
- Documentation includes a clear data quality framework, visibility of flagged data, and detailed metadata to support discovery, reuse, and interpretation.
- The final data product emphasizes transparency about data limitations (e.g., weather-related losses, sampling deviations) and provides mechanisms to exclude non-representative data from site-level estimates.
- Users should reference the accompanying metadata and flag explanations to understand data validity, detection limits, and any potential biases introduced by sampling conditions.