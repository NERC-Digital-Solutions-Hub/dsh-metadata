# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- Study of ammonia (NH3) concentrations along a transect through Ballynahone Bog, a protected peatland within Ballynahone National Park (ASSI/SAC) and a Ramsar site in Northern Ireland.
- Motivation: assess potential NH3 impacts from local poultry livestock installations.
- Field operations managed by Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (CEH) Edinburgh.

## Data collection and methods
- Instrumentation: CEH ALPHA passive samplers using a citric acid coated filter to capture NH3; PTFE membrane protects the filter.
- Deployment: replicates mounted on shelters at approximately 1.5 m above ground; samplers exposed monthly at the start of each month.
- Analysis: exposed samplers extracted into deionised water and analyzed by SEAL AA3 for colorimetric NH3 determination; concentrations converted to ambient air concentration using uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data quality controls: raw data screened for invalid samples (e.g., weather-related loss, incorrect exposure). Data flagged where concerns exist.

## Quality assurance and data flags
- Quality rules applied to decide validity:
  - Coefficient of variation (replicates) < 15% indicates valid representative data (flag 103 when valid).
  - Missing samplers marked as -9999.00 and invalid (-1).
  - Sampler duration anomalies (long/short) flagged.
  - Local contamination or influences noted from site records; such samples may be discarded if non-representative.
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv containing accepted values with appropriate flags.
- Data issues and flags follow UK-AIR/EMEP conventions; includes:
  - Detection limits, verification status, validity, and data capture
  - EMEP status codes and reasonings for data inclusion/exclusion
  - Flags for samples below detection limit or below quantification limit, and other contextual notes (e.g., sampling period anomalies, local interference, contamination).

## Dataset contents
- Data rows: monthly NH3 concentration per site and period.
- Columns (example):
  - Site name, start date, end date
  - Ammonia concentration for exposure period (µg NH3 m-3)
  - Data flag (quality/validity indicator)
  - Unique site identifier, network_id (BE), parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times
  - Less than detection indicator, verification id, unit id (µg NH3 m-3)
  - Data capture percentage, validity_id (1 = valid, -1 = not valid)
  - EMEP code and Month-Year (mmm-yy)
- Site metadata for eight Ballynahone bog locations (Ballynahone bog_1 to Ballynahone bog_8):
  - Start date: 01/09/2014; End date: Ongoing
  - Latitude and longitude coordinates
  - Height of air inlet above ground: 1.5 m

## Spatial and temporal coverage
- Spatial: eight sampling sites arranged along a transect in Ballynahone Bog with precise geolocations provided.
- Temporal: monthly sampling cycles throughout the observation period, starting 01/09/2014 and continuing (ongoing for sites).

## GIS relevance and potential uses
- Enables map-based visualization of NH3 concentrations across the transect over time.
- Facilitates spatial analysis of ammonia exposure in a sensitive peatland ecosystem.
- Data can be overlaid with land-use, poultry operation locations, and environmental layers for impact assessments and policy discussions.
- Uses standardized identifiers, coordinates, and metadata suitable for integration into GIS workflows and data catalogs.

## Data access and preparation notes
- Final dataset aggregates validated measurements and flags, suitable for GIS-ready analyses.
- Some samples were excluded due to weather, data capture issues, or contamination; remaining data are documented with corresponding flags and notes.
- Data units: micrograms per cubic meter of air (µg NH3 m-3). Detection considerations and QC flags align with EU/EMEP conventions.