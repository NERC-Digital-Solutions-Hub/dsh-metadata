# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Purpose and Context
- Monitor ammonia (NH3) in air across Ballynahone Bog, a sensitive peatland within Ballynahone National Park (ASSI/SAC) and Ramsar site.
- Concern: NH3 emissions from local poultry/livestock installations may affect the bog.
- Local operator: Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology, Edinburgh (UKCEH).
- Aim aligns with standardized environmental monitoring to support assessment of environmental health and policy performance over time.

## Methods and Data Collection
- Transect of eight sites through Ballynahone Bog; monthly passive sampling during 2021.
- Samplers: UKCEH ALPHA® passive samplers with citric acid-coated filters and a PTFE membrane; mounted ~1.5 m above ground on shelters; replicated samplers used for each site for reliability.
- Analysis: exposed samplers extracted into deionised water; analyzed with SEAL AA3 colorimetric method to determine NH3 concentration.
- Calculation: ambient air concentration derived from sampler concentration using uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Units: NH3 concentration reported as micrograms per cubic metre (µg NH3 m-3) for the exposure period.

## Quality Assurance and Data Flags
- Some samples excluded due to incorrect exposure or weather-related loss; data flagged accordingly.
- Quality rules:
  - Coefficient of variation (CV) of replicates < 15% deemed valid; otherwise evaluated for potential discard.
  - Missing samplers flagged; value -9999.00 and marked invalid (-1).
  - Sampler duration (long/short) flagged when outside normal monthly cycle.
  - Local contamination or influences noted; non-representative results discarded as needed; final data reflect the average of remaining valid replicates.
- Final dataset: UWT_Ballynahone_Bog_Data_2021.csv containing accepted data values with appropriate flags.
- Data status and flags align with a structured schema including verification status, detection limits, and data capture metrics.

## Dataset Structure and Content
- Each row represents one month of data for a single site.
- Key columns (example):
  - Site name, unique site identifier, network_id (BE)
  - Parameter_id (NH3 measurement type: alpha_NH3_g)
  - Measurement start/end dates and times
  - Ammonia concentration for the exposure period (µg NH3 m-3)
  - Less-than flag (detection limit: 0.03 µg NH3 m-3)
  - Verification id (1 = Verified, 2 = Preliminary verified, 3 = Not verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP data status codes and flags
  - Month-Year (mmm-yy)
- EMEP flags provide detailed context on data capture, validity, and potential data issues (e.g., contamination, sampling period duration, detection limits).

## Site Information
- Ballynahone bog_1 to bog_8:
  - Start date: 01/09/2014; End date: Ongoing
  - Coordinates (latitude/longitude) provided for each site
  - Height of air inlet above ground: 1.5 m

## Data Management and Availability
- Data collected for 2021 and stored with metadata to support verification, quality assurance, and traceability.
- Dataset designed to be stored in appropriate data portals and shared for broader use, enabling follow-on analyses and integration with other environmental datasets.

## Relevance to Environmental Monitoring and Policy
- Demonstrates standardized data collection, QA/QC, and documentation suitable for long-term monitoring and policy evaluation.
- Provides transparent data lineage and flags to enable re-use and combination with other datasets (addressing the challenge of increasing dataset value and ensuring access to underlying data).