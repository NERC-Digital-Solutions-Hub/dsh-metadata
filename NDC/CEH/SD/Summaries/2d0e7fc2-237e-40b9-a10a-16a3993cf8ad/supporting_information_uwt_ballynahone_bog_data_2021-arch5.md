# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Overview
- Dataset from a transect across Ballynahone National Park (ASSI/SAC and Ramsar site) in Northern Ireland.
- Managed by Ulster Wildlife Trust (UWT); analysis by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Purpose: monitor potential NH3 deposition effects on a sensitive peatland ecosystem due to local poultry/livestock installations.
- Data collected via UKCEH ALPHA passive samplers exposed monthly along the transect.

## Methods and Protocols
- Sampler: UKCEH ALPHA® passive sampler with citric acid coated filter and PTFE membrane, deployed at ~1.5 m height.
- Sampling design: replicate samplers per site to improve reliability; monthly exposure cycles (beginning of each month).
- Analysis: samplers extracted in deionised water; ammonia measured colorimetrically with SEAL AA3; results converted to average air concentration using uptake rate (0.003241315 m3 hr-1) and exposure duration.
- Data handling: some samples excluded due to incorrect exposure or weather-related loss; flagged in dataset.
- Data recorded per site-season: field notes on anomalies (e.g., contamination, duration deviations) influence data validity.

## Data Quality Assurance and Metadata
- Quality rules applied to raw data:
  - CV of replicates < 15% required for validity; otherwise evaluated for discard or flagging.
  - Missing samplers assigned -9999.00 and invalid flag.
  - Sampler duration deviations flagged (long/short).
  - Local contamination or anomalies flagged; affected samples may be discarded.
- Final dataset (UWT_Ballynahone_Bog_Data_2021.csv) contains accepted values with appropriate flags; raw data with issues are noted as not used for deposition estimates.
- Data flags and field codes provided, including:
  - Validity indicators (e.g., 1 = valid, -1 = not valid)
  - Data capture percentages
  - EMEP status codes and related flag explanations
  - Less-than/detection-limit indicators
- Data and metadata are documented with detailed column definitions and enumerations (e.g., site identifiers, network_id, parameter_id, dates, times, concentration values, validity flags, EMEP codes, and month-year stamps).

## Dataset Contents and Structure
- Final dataset: one row per month per site, containing:
  - Site name and unique site identifier
  - Network ID (BE)
  - Parameter type (alpha_NH3_g)
  - Exposure start and end dates and times
  - Measured ammonia concentration (µg NH3 m-3)
  - Detection-limit indicator (less than)
  - Verification status and data capture percentage
  - Data flag and EMEP code
  - Month-Year of measurement (MMM-YY)
- Units: micrograms of NH3 per cubic meter of air (µg NH3 m-3)
- Page-level context includes site list with coordinates and site-specific exposure details:
  - Ballynahone bog_1 to bog_8 with start dates 01/09/2014 and ongoing end dates
  - Latitude/Longitude coordinates and 1.5 m sampling inlet height

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Precise latitude and longitude provided per site
  - Sampling inlet height: 1.5 m

## Data Accessibility and Governance
- Data generated for environmental monitoring, suitable for researchers, managers, and policymakers interested in ammonia deposition under peatland sensitivity contexts.
- Dataset formatted for integration into data portals and catalogues; includes rich metadata and standardized field definitions to support discoverability and reuse.
- Emphasis on maintaining data quality and transparent documentation of any data limitations or anomalies to support appropriate use and interpretation.