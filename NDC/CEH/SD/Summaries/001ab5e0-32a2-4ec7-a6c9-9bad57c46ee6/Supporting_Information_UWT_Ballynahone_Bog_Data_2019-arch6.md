# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- Dataset from a transect of Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
- Purpose: assess potential NH3 deposition impact on ammonia-sensitive peatland; measurements relate to emissions from local poultry livestock installations.
- Local site operator: Ulster Wildlife Trust (UWT); analysis led by UK Centre for Ecology and Hydrology, Edinburgh (CEH).
- Data collection period: monthly exposure cycles using CEH ALPHA® passive samplers during 2019.

## Data collection and methods
- Instrument: CEH ALPHA® passive samplers with citric acid coated filter and PTFE membrane.
- Deployment: samplers mounted on shelters at ~1.5 m above ground; replicates used per site to estimate air concentration.
- Exposure regime: monthly cycles (beginning of each month); samples exposed from start to end dates/times recorded.
- Analysis workflow:
  - Exposed samplers are extracted into deionised water.
  - Water analyzed with SEAL AA3 colorimetric method to determine ammonia concentration.
  - Concentrations converted to average air concentration using sampler uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Data quality considerations: some samples exposed incorrectly, or lost due to weather; these are flagged and excluded from deposition estimates.

## Data processing and quality assurance
- Quality rules applied to 2019 raw data:
  - Coefficient of variation (CV) of replicate samplers: CV < 15% deemed acceptable; above 15% prompts evaluation for potential discards.
  - Missing samplers: values set to -9999.00 and flagged as invalid (-1).
  - Sampler duration anomalies: exposures longer/shorter than normal flagged as non-standard.
  - Local contamination or influences: site operator notes used to discard non-representative samplers; final site data averaged from remaining valid results.
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv containing accepted data values with appropriate flags.
- Data structure notes:
  - Each row represents one month of data for a single site.
  - Columns include site name, start and end dates, ammonia concentration (µg NH3 m-3), and a data flag.

## Dataset structure and contents
- Columns (example interpretations):
  - Site identifiers: Ballynahone bog_1 … Ballynahone bog_8
  - Start_date / End_date: 01/09/2014 to ongoing for each site
  - Latitude / Longitude: geographic coordinates for each site
  - Height of air inlet above ground: 1.5 m (consistent across sites)
  - Month-Year: period for each measurement (MMM-YY)
  - Ammonia concentration: concentration during exposure (µg NH3 m-3)
  - Data flag / Validity / Verification / Data capture: quality indicators and status codes
  - Additional fields include: network_id, parameter_id, measurement start/end dates and times, less-than flag (detection limit), verification status, unit id, EMEP/status flags
- Site information:
  - Ballynahone bog_1 through Ballynahone bog_8 with precise lat/long coordinates and consistent 1.5 m inlet height
  - All sites described as ongoing since 2014 in this dataset context

## Data flags and quality indicators
- Quality flags include:
  - Data capture percentage (documentation of how much data was captured per measurement)
  - Validity_id: 1 = valid, -1 = not valid
  - Verification: 1 = Verified, 2/3 = Preliminary/Not Verified (as per dataset nomenclature)
  - EMEP status and related subcodes indicating data status and possible issues
  - Less-than flag indicating values below detection limit (0.03 µg NH3 m-3) or below quantification limits
- Additional notes:
  - Some values may be below detection or affected by contamination; such cases are annotated with EMEP and local contamination flags as applicable
  - Data status codes (A–J) accompany data flags to describe verification and data issues

## Data accessibility and usage notes
- Final dataset file name: UWT_Ballynahone_Bog_Data_2019.csv
- Data are presented as monthly averages per site with units of µg NH3 m-3
- Considers replication-based QA to ensure reliable estimation of air concentrations
- Useful for:
  - Assessing spatial patterns of NH3 along the transect
  - Evaluating potential deposition pressure on Ballynahone Bog
  - Informing capacity for data-driven communication and policy discussions
- Users should pay attention to:
  - Exclusion of invalid or problematic samples
  - Missing data and duration anomalies
  - Local contamination notes that may affect representativeness of certain samplers

## Potential caveats and considerations for interpretation
- Some months/samples were excluded due to incorrect exposure or weather-related losses; deposition estimates rely on the remaining valid data
- CV-based quality control means replicates are crucial for reliability; high CV may reduce confidence in a given month’s value
- Data flags and EMEP codes provide context on data quality and should be consulted when integrating with other datasets or performing trend analyses