# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

## Overview
- Location and context: Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland; ammonia-sensitive peatland managed by Ulster Wildlife Trust (UWT).
- Purpose: assess potential NH3 emissions from local poultry livestock installations and their impact on the bog ecosystem.
- Institutions: field sampling by UWT; analysis by Centre for Ecology and Hydrology (CEH) Edinburgh.

## Sampling Methodology
- Instrument: CEH ALPHA® passive samplers with citric acid–coated filter and PTFE membrane; sampler height ~1.5 m above ground; replicas used per site.
- Deployment: samplers exposed in monthly cycles at the beginning of each month along a transect through the bog.
- Analysis: exposed samplers extracted into deionised water; analyzes with SEAL AA3 colorimetric method to determine ammonia concentration.
- Calculation: sampler concentration converted to average air concentration using uptake rate of 0.003241315 m3/h and exposure duration.
- Data quality notes: some raw samples were exposed incorrectly or lost due to weather; these are flagged and not used in deposition estimates.

## Data Processing and Quality Assurance
- Final dataset: UWT_Ballynahone_Bog_Data_2018.csv containing accepted values with appropriate flags.
- Quality rules:
  - CV rule: coefficient of variation (SD/mean) of replicates < 15%; if met, data considered valid with a 103 flag; if CV > 15%, replicates may be discarded and data evaluated further.
  - Missing samplers: represented as -9999.00 and flagged as invalid (-1).
  - Sampler duration: durations longer/shorter than normal flagged accordingly.
  - Local contamination/influences: noted via site record cards; affected samplers may be discarded or adjusted; final site data is the average of remaining results.
- Data status and metadata: final dataset includes site identifiers, exposure period, ammonia concentration (µg NH3 m-3), and a data flag. Detailed fields include measurement start/end dates and times, detection status, verification status, unit identifiers, data capture percentage, and EMEP status codes.

## Dataset Structure and Flags
- Dataset name: UWT_Ballynahone_Bog_Data_2018.csv.
- Core content per row: site name, start date, end date, ammonia concentration for exposure period (µg NH3 m-3), and a data flag.
- Metadata fields (examples): unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g), measurement start/end dates and times, less-than indicator (detection limit), verification id (Not verified / Preliminary verified / Verified), unit id (24 = µg NH3 m-3), data capture percentage, validity_id (1 = valid, -1 = not valid), EMEP code (data status).
- EMEP flags: codes describe data quality issues (e.g., missing data, below detection limit, contamination, sampling duration anomalies, CV issues). These provide context for why a value may be invalid or treated with caution.

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8: eight monitoring sites.
- Common attributes: start_date 01/09/2014; end_date ongoing; height of air inlet 1.5 m.
- Coordinates (examples): 
  - bog_1: 54.82223827, -6.67860685
  - bog_2: 54.82303694, -6.67686906
  - bog_3: 54.82331637, -6.67530382
  - bog_4: 54.82396942, -6.67339952
  - bog_5: 54.82446239, -6.67000651
  - bog_6: 54.82514962, -6.67946104
  - bog_7: 54.82165647, -6.67468906
  - bog_8: 54.816161, -6.655967
- All sites share a standard exposure height and are part of a transect through the bog for spatially resolved NH3 monitoring.

## Data Availability and Usage Notes
- Data are suitable for analysing spatial and temporal patterns of ambient ammonia concentrations at local scale within Ballynahone Bog.
- Useful for correlating NH3 exposure with nearby poultry operations, meteorological data, or ecosystem responses, while accounting for data quality flags and potential gaps.
- Analysts should respect data quality flags, particularly CV-based exclusions, missing samplers, abnormal sampling durations, and contamination notes, when deriving conclusions or building predictive models.