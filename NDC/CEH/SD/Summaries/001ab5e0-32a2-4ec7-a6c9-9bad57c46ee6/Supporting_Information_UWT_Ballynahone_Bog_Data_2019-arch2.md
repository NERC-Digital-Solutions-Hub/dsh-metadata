# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- Location and context: Ballynahone Bog field site in Ballynahone National Park, Northern Ireland; part of an Area of Special Scientific Interest (ASSI/SAC) and a Ramsar site; ammonia-sensitive peatland managed locally by Ulster Wildlife Trust (UWT).
- Purpose: monitor NH3 emissions potentially affecting the bog, with a transect sampling design along the bog.
- Responsibility: site operator duties by UWT; data analysis by UK Centre for Ecology and Hydrology (CEH) Edinburgh.
- Data scope: monthly ammonia measurements using CEH ALPHA® passive samplers; analysis and quality assurance follow standard procedures; dataset intended for environmental monitoring and policy scrutiny.

## Monitoring Method (CEH ALPHA® Sampler)
- Sampling device: CEH ALPHA® passive samplers with citric acid coated filters to capture ammonia; PTFE membrane protects the filter; sampler orientation with membrane end facing down.
- Deployment: replicates attached to a shelter on poles at about 1.5 m above ground; exposed for monthly cycles starting at the beginning of each month.
- Analysis workflow: exposed samplers extracted into deionised water; ammonia measured by SEAL AA3 colorimetric analyzer; concentrations converted to average air concentration using a known uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data quality notes: some samples were exposed incorrectly or lost due to weather; such samples are flagged and not used for deposition estimates. Final data are stored in a dataset with appropriate flags.

## Data Processing and Quality Assurance
- Quality rules applied to raw data:
  - Coefficient of variation (CV) of replicates < 15%: valid replicates averaged; otherwise evaluation and potential discarding of outliers; valid results flagged.
  - Missing samplers: coded as -9999.00 and invalid (-1).
  - sampler duration anomalies: longer or shorter exposure than usual flagged.
  - Local contamination or influences: site operator notes used to discard non-representative samplers; reported as the average of remaining results.
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv containing accepted data values with appropriate flags.
- Data structure: each row represents one month’s data for a single site; fields include site name, dates, ammonia concentration (µg NH3 m-3), and a data flag, among others.

## Dataset Structure and Content
- File name: UWT_Ballynahone_Bog_Data_2019.csv.
- Key content per row:
  - Site name, unique site identifier, network_id (BE), parameter_id (alpha_NH3_g).
  - Exposure start and end dates and times.
  - Ammonia concentration for the exposure period (units: µg NH3 m-3).
  - Flags for detection limit, verification status, data capture percentage, validity, and EMEP-related codes.
  - Month-Year of measurement (e.g., mmm-yy).
- Purpose: monthly, site-level ammonia data with metadata to support transparency and traceability.

## EMEP Flags and Data Status
- The dataset includes EMEP flags and a data status system to capture data quality and context, including:
  - Data capture percentage.
  - Validity indicators (valid/not valid) and verification status.
  - Codes indicating issues such as sampling duration irregularities, contamination, nearby activities, detection limits, and other local influences.
- These flags enable analysts to assess data reliability and to filter data for time-series analysis or policy evaluation.

## Site Information
- Ballynahone Bog sites: bog_1 through bog_8 (eight sampling locations along the transect).
- Common attributes:
  - Start date: 01/09/2014 for all sites.
  - End date: ongoing.
  - Inlet height above ground: 1.5 m.
- Geographic coordinates provided for each site, enabling spatial analyses and mapping.

## Data Management and Access
- Data are generated under established monitoring responsibilities with standardized methods to ensure comparability across sites and time.
- Datasets are stored and uploaded to appropriate portals, enabling access to underlying data and facilitating broader analyses by others for environmental health and policy performance assessment.