# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2019

## Overview
- Data from a transect through Ballynahone National Park (an ASSI/SAC and Ramsar site) in Northern Ireland.
- Park managed locally by Ulster Wildlife Trust (UWT); analysis by the UK Centre for Ecology and Hydrology (CEH) Edinburgh.
- Aim: assess potential NH3 deposition from local poultry livestock installations and monitor ammonia in a sensitive peatland ecosystem.

## Sampling and study area
- Passive CEH ALPHA® samplers deployed along a transect through Ballynahone Bog.
- Each sampler exposed monthly, mounted at about 1.5 m above ground on shelters.
- Replicates used per site to improve reliability.
- Field sites (eight Ballynahone bog sites) documented with precise start dates (01/09/2014) and ongoing end dates, including latitude, longitude, and 1.5 m air-inlet height.

## Measurement and analysis workflow
- Ammonia captured on a citric acid–coated filter within a PTFE membrane and analyzed after exposure.
- Analysis by SEAL AA3 colorimetric method; results converted to average NH3 concentration in air using the known sampler uptake rate (0.003241315 m3 h-1) and exposure duration.
- Data processed into monthly exposure concentration values in micrograms of NH3 per cubic metre (µg NH3 m-3).

## Data structure and content
- Final dataset: UWT_Ballynahone_Bog_Data_2019.csv.
- Each row represents one month of data for a single site; columns include:
  - site name, unique site identifier, network_id (BE), parameter_id (alpha_NH3_g)
  - measurement start/end dates and times (exposure period)
  - ammonia concentration for the exposure period (units: µg NH3 m-3)
  - flag indicating detection status (less than detection limit), verification status, unit id (24 = µg NH3 m-3)
  - data capture percentage
  - validity_id (e.g., 1 = valid, -1 = not valid)
  - EMEP data status code and related flags
  - Month-Year of the measurement (e.g., mmm-yy)
- The dataset includes a detailed mapping of fields and codes to support interoperability and cross-agency use.

## Quality control and data flags
- Raw data screening identified samples exposed incorrectly or lost due to weather; these are flagged and excluded from deposition estimates.
- Quality rules applied:
  - Coefficient of variation (CV) of replicates < 15%: data considered valid (flagged 103); CV > 15% triggers evaluation and potential discarding of some replicates.
  - Missing samplers: assigned -9999.00 and marked invalid (-1).
  - Sampler duration anomalies: data flagged when durations were longer/shorter than normal.
  - Local contamination or unusual influences: notes on sample cards; questionable samplers are discarded if not representative.
- Final dataset contains accepted values with appropriate flags to indicate validity and data issues.
- EMEP flags provide detailed reasoning for data status, including missing measurements, detection-limit considerations, samplingPeriod adjustments, contamination, and other context.

## Data governance, provenance, and stewardship
- Data collected by UWT and analyzed by CEH Edinburgh, with a formal QA process to ensure data quality and traceability.
- Data are structured with rich metadata to enable discoverability, verification, and reuse across partner organisations and policy contexts.
- The dataset is designed to support ongoing data stewardship, user needs, and potential collaboration within the broader data community.

## Site information and geography
- Ballynahone bog sites (1–8) with specified coordinates and consistent 1.5 m air inlet height.
- Each site has an identified start date (01/09/2014) and ongoing end date, with precise latitude and longitude coordinates provided.

## Implications for data strategy and reuse
- Demonstrates comprehensive data lifecycle management: from field collection and replication to rigorous QA, metadata-rich dataset construction, and clear data flags.
- Supports co-ownership and collaboration by providing standardized fields, unit definitions, and provenance details.
- Highlights the importance of documenting sampling conditions, data capture, and anomaly handling to enable robust analysis and cross-site comparisons in data-driven decision-making.