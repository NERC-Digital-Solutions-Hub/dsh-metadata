# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

## Overview
- Set of sampling sites forming a transect through Ballynahone National Park (AREA OF SPECIAL SCIENTIFIC INTEREST / SAC; Ramsar site) in Northern Ireland.
- Purpose: assess potential NH3 emissions impact from local poultry livestock installations on Ballynahone Bog, a peatland sensitive to ammonia.
- Operators: Ulster Wildlife Trust (site operator); Centre for Ecology and Hydrology Edinburgh (analysis).
- Measurement approach: CEH ALPHA passive samplers used along the transect, exposed monthly; data processed to estimate ambient ammonia concentrations.

## Sampling method (CEH ALPHA samplers)
- Passive sampler with a citric acid coated filter to capture NH3; protected by a white PTFE membrane (diffusion of NH3 through the membrane).
- Samplers mounted on shelters at ~1.5 m above ground; replicates used for each site to improve reliability.
- Exposure: monthly cycles, at the beginning of each month.
- Analysis: exposed samplers extracted into deionised water and analyzed with SEAL AA3 colorimetric method.
- Calculation: concentration in air derived from sampler uptake rate (0.003241315 m3 h-1) and exposure duration.

## Data quality assurance and flags
- Some samples were exposed incorrectly or lost due to weather; these are not used for deposition estimates and are flagged.
- Final dataset: UWT_Ballynahone_Bog_Data_2018.csv containing accepted data with appropriate flags.
- Quality rules:
  - Coefficient of variation (CV) of replicates < 15% -> data considered valid (flag 103 if acceptable).
  - Missing samplers: marked as -9999.00 and invalid (-1).
  - Sampler duration longer/shorter than normal: flagged accordingly.
  - Local contamination or deviations noted in site records; potentially discarded if not representative; final value is average of valid results.

## Dataset contents and structure
- Each row represents one month of data for a single site.
- Columns include:
  - Site name and unique site identifier
  - network_id (UWT)
  - parameter_id (type of measurement, e.g., alpha_NH3_g)
  - measurement start/end dates and times (exposure period)
  - ammonia concentration (units: µg NH3 m-3)
  - less than detection limit flag (1 if < detection limit 0.03 µg m-3)
  - verification id (1: Verified, 2: Preliminary verified, 3: Not verified)
  - unit id (24 = µg NH3 m-3)
  - data capture percentage
  - validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status and flags)
  - Month-Year (exposure period, e.g., mmm-yy)
- EMEP flags provide detailed context for data capture, validity, and reasons (e.g., contamination, detection limits, sampling period, CV issues).

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014
  - End date: Ongoing
  - Coordinates (latitude/longitude) and height of air inlet above ground: 1.5 m
- Data cover a transect across the bog with multiple closely spaced sampling sites.

## Data use and considerations
- Data designed to support assessment of ammonia exposure/atmospheric deposition on Ballynahone Bog.
- Monthly concentration values are the average NH3 concentration during the exposure period for each site.
- Data quality and metadata (flags, detection limits, validation status, and location information) are integrated to support rigorous interpretation and potential cross-site comparisons.
- The document notes that more detailed contents and site lists appear on referenced pages of the original report.