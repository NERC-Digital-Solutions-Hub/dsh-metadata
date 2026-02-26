# Supporting_Information_UWT_Ballynahone_Bog_Data_2020

## Overview
- Data from a transect through Ballynahone National Park in Northern Ireland, an Area of Special Scientific Interest (ASSI/SAC) and a Ramsar site.
- Purpose: assess potential adverse effects of local NH3 emissions from poultry livestock installations on Ballynahone Bog, an ammonia-sensitive peatland.
- Collected by Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.

## Methodology
- Instrument: UKCEH ALPHA® passive samplers with citric acid coated filters and PTFE membranes; deployed on shelters at ~1.5 m above ground.
- Deployment: replicate samplers at multiple sites along a bog transect; exposed in monthly cycles.
- Analysis workflow: samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetry; results converted to ambient NH3 concentration using the sampler uptake rate (0.003241315 m3 h-1, 2020 calibration) and exposure duration.
- Data handling: data flagged for quality concerns; raw data quality checked against predefined rules.

## Data structure and contents
- Final dataset: UWT_Ballynahone_Bog_Data_2020.csv.
- Each row: one month of data for a single site; columns include site name, exposure start/end dates and times, ammonia concentration (µg NH3 m-3), and a data flag.
- Key columns (descriptions):
  - Station name / unique site identifier
  - network_id
  - parameter_id (alpha_NH3_g)
  - measurement start date and start time
  - measurement end date and end time
  - measurement (ammonia concentration in µg NH3 m-3)
  - less than (flag if concentration below detection limit 0.03)
  - verification id (verification status)
  - unit id (µg NH3 m-3)
  - Data capture (percentage)
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status flag)
  - Month-Year (exposure period marker)
- Dataset scope: eight Ballynahone bog sites (bog_1 through bog_8); start date 01/09/2014; ongoing; coordinates and 1.5 m air inlet height provided for each site.

## Quality, flags, and limitations
- Data quality rules:
  - Coefficient of variation (CV) of replicates must be <15% for valid results.
  - If CV >15%, replicates reviewed; data may still be considered valid if representative.
  - Some samples exceeded calibration range; classified as valid but note instrument limitations.
  - Missing data marked as -9999 in the measurement or metadata fields.
- Data capture and validity indicators:
  - EMEP flags provide context for data quality, contamination indicators, detection limits, and other data issues.
  - Common statuses include valid measurements, missing data, or contamination/adverse local influences.
- The dataset explicitly accounts for data quality and provenance, with site metadata (names, coordinates, and sampling height) and detailed flag descriptions to enable robust interpretation.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014; End date: Ongoing
  - Latitude/Longitude and standard 1.5 m air inlet height
- Site list includes precise coordinates for accurate spatial analysis and mapping.

## Usage notes
- Concentrations are monthly averaged NH3 in air (µg NH3 m-3) for the specified exposure period.
- Interpret data with attention to quality flags (CV, calibration range, missing data) and EMEP status codes.
- Data can be used to assess spatial and temporal patterns of ammonia around Ballynahone Bog and to support assessments of potential impacts from nearby poultry operations.