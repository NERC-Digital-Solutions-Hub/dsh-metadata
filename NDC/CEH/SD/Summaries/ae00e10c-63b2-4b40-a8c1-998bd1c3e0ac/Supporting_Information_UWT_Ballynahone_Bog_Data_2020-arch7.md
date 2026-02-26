# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Overview
- Dataset from a transect through Ballynahone National Park in Northern Ireland, an Area of Special Scientific Interest (ASSI/SAC) and Ramsar site.
- Purpose: assess potential ammonia (NH3) impact on a ammonia-sensitive peatland ecosystem from local poultry livestock installations.
- Operators: Ballynahone Bog data managed by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology Edinburgh (UKCEH).
- Measurement approach: UKCEH ALPHA® passive samplers deployed along a transect at about 1.5 m above ground; samplers exposed monthly.

## Data collection and methods
- ALPHA® sampler: passive device with citric acid–coated filter to capture NH3; PTFE membrane protects filter; membrane facing downward during exposure.
- Deployment: replicate samplers mounted on shelters on posts, height ~1.5 m; replicates provide reliability.
- Analysis: exposed samplers extracted into deionised water; analysed by SEAL AA3 using colorimetry to determine ammonium concentration; concentration in air calculated using sampler uptake rate (0.003241315 m3 hr⁻¹, 2020 calibration) and exposure duration.
- Data quality checks: data flagged for concerns; key quality rules include:
  - Coefficient of variation (CV) of replicates < 15%; otherwise replicates may be adjusted or discarded; data flagged as valid (103) if representative.
  - Values greater than calibration range but deemed valid if dilution/reanalysis not possible due to instrument issues.
  - Missing data or metadata indicated by -9999 in concentration or time fields.
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv with accepted data values and appropriate flags; includes site-specific metadata and spatial identifiers.

## Data structure and content
- File name: UWT_Ballynahone_Bog_Data_2020.csv.
- Granularity: one row per site per month, capturing a single month’s data for a given site.
- Core fields (examples):
  - Site name; unique site identifier; network_id (RSW); parameter_id (alpha_NH3_g).
  - Exposure period start date/time and end date/time.
  - Ammonia concentration (µg NH3 m⁻³) for the exposure period.
  - Data flag and validity indicators (e.g., -9999 for missing data, verification status).
  - Metadata fields: Month-Year; EMEP code; data capture percentage; validity_id; various EMEP/QA flags and reasons.
- Units: concentrations are reported as micrograms of NH3 per cubic metre of air (µg NH3 m⁻³); exposure period is defined by start/end dates and times.
- Data flags and codes: include verification status, data capture, and EMEP flag codes detailing data quality or issue type (e.g., contamination, detection limits, sampling conditions).

## Quality flags and data status
- Validation flag 103: CV of replicates < 15%, considered valid.
- Flags for values outside calibration range but still valid due to instrumentation constraints.
- -9999 values indicate missing data or missing metadata required to calculate concentration.
- EMEP and site-specific flags provide context on data quality, contamination indicators, or observational conditions (e.g., detection limits, sampling period representativeness, nearby activities).

## Spatial information
- Site information for Ballynahone bog includes multiple sampling points:
  - Ballynahone bog_1 to Ballynahone bog_8.
  - Each site includes:
    - Start date: 01/09/2014; End date: Ongoing.
    - Latitude and longitude coordinates.
    - Height of air inlet above ground: 1.5 m.
- Spatial identifiers and coordinates enable GIS integration and visualization of ammonia concentrations across the transect within Ballynahone Bog.