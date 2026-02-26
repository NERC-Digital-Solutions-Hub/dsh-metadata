# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

## Overview
- Location: Ballynahone National Park, Northern Ireland; an ammonia-sensitive peatland (ASSI/SAC, Ramsar site).
- Managed by Ulster Wildlife Trust (UWT); analysis by Centre for Ecology and Hydrology Edinburgh (CEH).
- Purpose: Assess potential NH3 deposition from local poultry livestock installations along a transect through the bog.
- Timeframe: Data collected 2014–2017; samplers exposed monthly at the start of each month.

## Sampling design and method
- Transect sampling across Ballynahone Bog with multiple sites (bog_1 to bog_8).
- Passive CEH ALPHA® samplers used to measure NH3 in air.
  - Sampling medium: citric acid–coated filter with a PTFE membrane; membrane faces downward during exposure.
  - Deployment: replicate samplers mounted on shelters on poles at about 1.5 m above ground; protection container provided.
- Exposure routine: monthly cycles; replicates to improve reliability.
- Data captured: monthly ammonia concentration per site, with start and end dates for each exposure period.

## Analysis and data processing
- Analysis method: samplers extracted into deionised water and analyzed by AMFIA (Ammonia Flow Injection Analysis) using conductivity to determine NH3 concentration.
- Conversion: sampler results converted to average NH3 concentration in air using known uptake rate of ALPHA samplers (0.003241315 m3 h-1) and exposure duration.
- Data quality handling:
  - Some samples excluded due to incorrect exposure or weather; these flagged as concerns.
  - Final dataset: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv containing accepted values with appropriate flags.
- Data structure: each row represents one month of data for a single site; columns include site name, start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.

## Data quality, flags, and documentation
- Quality control rules applied to raw data:
  - Coefficient of variation (CV) of replicates < 15% required for validity; CV > 15% leads to evaluation and potential discard; valid results flagged as 103 if representative.
  - Missing samplers: value -9999.00 and invalid flag (-1).
  - Duration anomalies: samplers left longer/shorter than normal cycle flagged.
  - Local contamination or influences: site operator notes used to discard non-representative samples; remaining results averaged for the site data.
- Data flags: final dataset includes a “Data capture” percentage, validity status, and a detailed EMEP/status code row to indicate data quality and reasons (e.g., below detection limit, CV issues, contamination, sampling period anomalies).
- Verification: data contains a verification status field (1 = Verified, 2 = Preliminary verified, 3 = Not verified).

## Dataset contents and structure
- Dataset name: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv.
- Key fields per row:
  - Station name, unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g).
  - Exposure start date/time and end date/time.
  - Ammonia concentration for the exposure period (µg NH3 m-3).
  - Flags for detection limit, verification, unit, data capture, validity, EMEP code, and Month-Year.
- Site information included:
  - Ballynahone bog_1 to Ballynahone bog_8, each with start date 01/09/2014 and ongoing end date.
  - Geographic coordinates (latitude, longitude) and height of air inlet (1.5 m).

## Site context and governance
- Ballynahone Bog is part of a broader protected area network and monitored for atmospheric NH3 impact on a sensitive peatland ecosystem.
- Data collection and analysis conducted by CEH Edinburgh with local site operations by Ulster Wildlife Trust.