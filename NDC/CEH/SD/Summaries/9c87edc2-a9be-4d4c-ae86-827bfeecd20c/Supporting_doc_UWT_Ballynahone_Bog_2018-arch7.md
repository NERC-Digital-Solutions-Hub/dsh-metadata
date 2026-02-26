# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

## Overview
- A transect of eight sampling sites in Ballynahone Bog, Northern Ireland, within a national park, ASSI/SAC, and Ramsar site.
- Objective: assess NH3 air concentrations to evaluate potential amonia impact from nearby poultry livestock installations.
- Analysis performed by CEH Edinburgh; operator duties by Ulster Wildlife Trust (UWT).
- Data collected using CEH ALPHA® passive samplers exposed monthly; concentration derived from colorimetric analysis.

## Sampling method and data collection
- Passive samplers mounted at about 1.5 m above ground on shelters; replicate samplers used per site for reliability.
- Samplers exposed in monthly cycles; sampling period defined by start and end dates.
- Ammonia concentration in air calculated from sampler uptake rate (0.003241315 m3 hr-1) times exposure duration, using the measured ammonia from deionised water extracted from samplers analyzed by SEAL AA3.
- Raw data include monthly measurements per site, with fields such as site name, network_id, parameter_id, exposure dates and times, concentration, and quality flags.

## Data quality and flags
- Data quality rules applied to identify valid measurements:
  - CV of replicates < 15% required for reliability; if CV > 15%, evaluation determines whether replicates are discarded.
  - Missing samplers flagged as invalid (-1) with value -9999.00 for concentration.
  - Sampler duration deviations (long/short) flagged accordingly.
  - Local contamination or influences noted by site operators; flagged results may be discarded if not representative.
- Final dataset (UWT_Ballynahone_Bog_Data_2018.csv) contains accepted measurements with appropriate flags.
- Some raw samples were excluded due to weather or incorrect exposure; flagged accordingly in the dataset.

## Dataset contents and structure
- Each row represents one month of data for a single site.
- Columns include:
  - Site name
  - Start date and end date of exposure
  - Ammonia concentration (µg NH3 m-3)
  - Data flag (quality indicator)
  - Additional fields such as verification status, data capture percentage, and EMEP status codes
- Units: micrograms of NH3 per cubic metre of air (µg NH3 m-3).

## EMEP and data flags
- EMEP-related flags provide data status and reasonings (e.g., missing data, below detection limit, contamination, sampling period anomalies, etc.).
- Examples of flag purposes:
  - Data capture percentage
  - Validity status (valid/not valid)
  - Reason for flag (e.g., contamination, sampling period issues, below detection limits)

## Site information and transect details
- Ballynahone bog_1 to Ballynahone bog_8 with consistent start date: 01/09/2014; end date: ongoing.
- Spatial identifiers:
  - Each site has latitude, longitude, and height of air inlet above ground (1.5 m).
- Location details enable GIS mapping of the transect across the bog and integration with other spatial data layers.

## Data handling and provenance
- Raw data checked and assessed for quality; status and flags documented in the final dataset.
- Analysis and data processing conducted to ensure consistency across sites and months.
- Dataset intended for use in GIS-based visualization and spatial analysis to interpret ammonia exposure patterns along the transect.