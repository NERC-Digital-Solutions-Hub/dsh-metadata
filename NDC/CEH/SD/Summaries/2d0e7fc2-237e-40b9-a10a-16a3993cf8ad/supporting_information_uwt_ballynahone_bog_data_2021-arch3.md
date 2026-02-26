# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Overview
- Monitoring purpose: assess ammonia (NH3) air concentrations to evaluate potential adverse effects from local poultry livestock installations on Ballynahone Bog, a peatland ecosystem.
- Site management: Ballynahone National Park area; environmental site managed locally by Ulster Wildlife Trust (UWT).
- Analysis: data collection by UWT; analysis by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.
- Instrument: UKCEH ALPHA® passive samplers deployed along a transect through the bog.
- Sampling cadence: monthly exposure cycles; samplers mounted at about 1.5 m above ground on shelters.

## Sampling and analysis methods
- Sampler design: CEH ALPHA® passive samplers with citric acid coated filters to capture NH3; PTFE membrane oriented downwards; protective caps when not exposed.
- Deployment: replicated samplers per site to improve reliability; mounted on poles.
- Sample processing: exposed samplers extracted into deionised water; NH3 concentration measured by SEAL AA3 colorimetric analyser.
- Calculation: ambient NH3 concentration derived from sampler results using a known uptake rate (0.003241315 m3 hr-1) and exposure duration.
- Quality considerations: some samples excluded due to incorrect exposure or weather-related loss; data flagged accordingly.

## Data quality and governance
- Quality assurance rules:
  - Coefficient of variation (CV) of replicates must be < 15%; otherwise replicates are evaluated or discarded.
  - Missing samplers assigned a placeholder (-9999.00) and marked invalid.
  - Sampler duration anomalies (long/short) flagged.
  - Local contamination or deviations noted; non-representative samplers discarded.
- Final dataset: UWT_Ballynahone_Bog_Data_2021.csv containing accepted data values with appropriate flags.
- Metadata and reporting: dataset includes site names, exposure periods, measured concentrations (µg NH3 m-3), and a data flag; site and measurement metadata documented for traceability.
- Data status and interoperability: includes data capture percentage, verification status, and EMEP-related flags to support reporting and international comparability.

## Data structure and metadata
- Dataset: UWT_Ballynahone_Bog_Data_2021.csv
- Key columns (examples):
  - site name, start_date, end_date
  - ammonia concentration (µg NH3 m-3)
  - data flag (validity and quality indicators)
  - verification status, data capture percentage, EMEP flags
  - month-year stamp for measurement period
- Data status codes and flags (e.g., 103 = valid, -1 = not valid) used to indicate quality and representativeness.
- Rich metadata fields describing measurement start/end dates and times, unique identifiers, network code (BE), parameter type (alpha_NH3_g), unit (µg NH3 m-3), and level of verification.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Coordinates: latitudes ~54.82–54.83, longitudes ~ -6.67 to -6.65
  - Height of air inlet above ground: 1.5 m
- The sites form a transect within Ballynahone Bog to monitor spatial variation in NH3 concentrations.