# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Overview
- Dataset from a transect through Ballynahone National Park (ASSI/SAC, Ramsar site) in Northern Ireland.
- Managed locally by Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology, Edinburgh (UKCEH).
- Purpose: monitor potential NH3 deposition affecting a sensitive peatland ecosystem due to nearby poultry livestock installations.
- Field sampling uses UKCEH ALPHA passive samplers, deployed monthly along the transect; multiple sites to improve reliability.

## Methods and Data Processing
- Sampler type: CEH ALPHA passive samplers with citric acid coated filter and PTFE membrane; mounted ~1.5 m above ground on shelters.
- Replicates used at each site to estimate ambient ammonia concentrations.
- Analysis: samplers extracted into deionised water; ammonia quantified by SEAL AA3 colorimetry; concentrations converted to average air concentration using sampler uptake rate of 0.0038422 m3 h-1 and exposure duration.
- Data handling: raw data contained some incorrectly exposed or weather-lost samples; such data are flagged and not used for deposition estimates.
- Dataset after quality control: final file named UWT_Ballynahone_Bog_Data_2022.csv containing accepted values with appropriate flags.

## Data Quality and Flags
- Quality criteria applied to raw data:
  - Coefficient of variation (replicate CV) < 15%; otherwise assess replicates and may discard some; valid when representative (flagged as 103 if valid).
  - Missing samplers assigned -9999.00 and marked invalid (-1).
  - Sampler duration deviations (long/short) flagged.
  - Local contamination or other deviations noted by site operators; affected samples may be discarded; final site data is the average of remaining results.
- Data flags:
  - Data capture percentages and validity indicators accompany each record.
  - EMEP and data status flags provide methodological and quality context (e.g., verification status, data capture, detection limits).
- Documentation notes: page references and metadata describe site identifiers, coordinates, and measurement details.

## Data Structure and Contents
- Each row represents one month of data for a single site within Ballynahone bog transect.
- Columns (examples):
  - Site name, unique site identifier, network_id (BE)
  - Parameter_id (type of measurement: alpha_NH3_g)
  - Measurement start date/time and end date/time (exposure period)
  - Ammonia concentration (µg NH3 m-3)
  - Less than detection flag, verification id, unit id (24 = µg NH3 m-3)
  - Data capture percentage, validity_id (1 = valid, -1 = not valid)
  - EMEP code and data status flags
  - Month of measurement
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv containing accepted data values, with flags indicating quality and any exclusions.

## Site Information
- Ballynahone bog_1 to bog_8 included; ongoing data collection since 01/09/2014.
- Location details:
  - Latitude/Longitude for each site (approx. 54.816–54.825 N, -6.655–-6.679 W)
  - Inlet height above ground: 1.5 m
- Data coverage: ongoing data collection across eight sites along the transect in Ballynahone bog.

## Governance, Access and Usage
- Data custodians: Ulster Wildlife Trust (site operations) and UKCEH (analysis/processing).
- Dataset intended for discovery and reuse by researchers and agencies concerned with ammonia deposition and peatland health.
- Metadata covers data provenance, instrument method, quality criteria, and flagging system to support appropriate data use and updates.
- Users should consult flags and notes on data quality, sample validity, and any local contamination indicators when interpreting concentrations.