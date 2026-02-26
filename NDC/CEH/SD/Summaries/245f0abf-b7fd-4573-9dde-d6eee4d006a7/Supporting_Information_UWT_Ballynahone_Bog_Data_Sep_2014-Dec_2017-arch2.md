# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

## Overview
- Field site transect through Ballynahone National Park (ASSI/SAC) and Ramsar site in Northern Ireland.
- Ammonia-sensitive peatland ecosystem; concern over NH3 emissions from local poultry livestock installations.
- Operated by Ulster Wildlife Trust (UWT); analysis by Centre for Ecology and Hydrology Edinburgh (CEH).
- Sampling period: 2014–2017; monthly exposure cycles starting at the beginning of each month.
- Data enable monitoring of ambient NH3 concentrations and potential deposition impacts along the transect.

## Sampling Method
- Instrument: CEH ALPHA® passive samplers with citric acid-coated filters and PTFE membranes, facing downward.
- Deployment: Replicate samplers mounted on shelters on poles at about 1.5 m above ground.
- Replication: Multiple samplers per site to improve reliability.
- Analysis workflow: Exposed samplers extracted into deionised water; analysis by AMFIA (ammonia flow injection analysis) to determine NH3 concentration via conductivity response.
- Conversion to ambient concentration: Uses known sampler uptake rate (0.003241315 m3 hr-1) and exposure duration to estimate average air concentration (µg NH3 m-3).
- Data format: Each row corresponds to one month per site; columns include site ID, exposure period, ammonia concentration, and data flags.

## Data Processing and Quality Assurance
- Raw data issues: Some samples exposed incorrectly or lost to weather; flagged, and not used for deposition estimates.
- Quality rules:
  - Coefficient of variation (CV) of replicates < 15% for validity; averages with acceptable CV are considered valid (flag 103).
  - Missing samplers: assigned -9999.00 and marked invalid (-1).
  - Sampling duration anomalies: longer/shorter than normal flagged as non-standard but may be considered representative.
  - Local contamination or influences: notes from site operator; affected samples may be discarded; final site value is the average of valid results.
- Final dataset: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv containing accepted values with appropriate flags.
- Data structure: Dataset includes monthly NH3 concentration (µg NH3 m-3), data capture percentage, validity flag, and EMEP-related status codes.
- EMEP flags and data status: Comprehensive flag system indicating data capture, detection limits, contamination sources, sampling period deviations, and verification status.

## Dataset Details
- Primary data column: Ammonia concentration for each month per site (units: µg NH3 m-3).
- Key metadata fields: 
  - Site name and unique identifier
  - Network/source (UWT)
  - Parameter type (alpha_NH3_g)
  - Exposure start/end dates and times
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - Verification status and EMEP code
  - Month-Year (mm-yy)

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8
  - Start date: 01/09/2014
  - End date: Ongoing
  - Coordinates (latitude, longitude) provided for each site
  - Height of air inlet above ground: 1.5 m
- Notes: Site locations form a transect within Ballynahone Bog with repeated monthly sampling across all eight sites.

## Context for Environmental Monitoring and Policy
- Purpose aligns with standardised environmental monitoring: consistent data format, QA/QC, and accessible datasets for evaluating environmental health and policy performance over time.
- Data are prepared for upload to appropriate portals, supporting transparency and reuse for broader analyses.

## Key Considerations for Analysts
- Datasets are designed for integration with other monitoring data; combining NH3 data with additional environmental datasets can enhance insight into deposition and ecosystem impacts.
- Underlying data and flags are documented to enable critical evaluation and reuse; ensure proper interpretation of CV, data capture, and validity indicators.
- The transect design and monthly cadence provide temporal and spatial context for trend analyses and policy assessments related to ammonia emissions and peatland sensitivity.