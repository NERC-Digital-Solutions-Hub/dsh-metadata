# Ammonia measurements from passive samplers at four UK Eutrophying and Acidifying Pollutants (UKEAP) network sites, 2021

## Overview
- Initial results to determine the uptake rate for ALPHA® passive samplers used in the UK and similar climates.
- Sampling conducted at four UKEAP network sites with monthly exposure cycles starting at the beginning of each month.
- Field operations conducted by UKCEH, AFBI (Hillsborough), and Ricardo AEA; analysis performed by CEH Edinburgh.

## Measurement method
- ALPHA® sampler: passive sampler with a citric acid–coated filter and a white PTFE membrane to capture NH3; membrane faces downward during exposure.
- Samplers mounted about 1.5 m above ground on a shelter, with replicate samplers per site to improve reliability.
- Analysis: exposed samplers extracted in deionised water and analyzed by SEAL AA3 colorimetry to quantify ammonium concentration.
- Conversion to ambient NH3 concentration uses a known uptake rate of 0.003241315 m3 h-1 and the exposure duration.

## Data processing and quality control
- Data flagged to indicate concerns (details on page 4 of the source document).
- Quality assessment rules:
  - Coefficient of variation (CV) of replicates < 15% deemed valid; if CV > 15%, replication results are evaluated for discard or retention; valid data flagged as 103.
  - Values above calibration range may be valid if re-measurement isn’t possible due to instrument failure or sample loss.
  - Missing data or metadata indicated by -9999 in the relevant fields.
- Final dataset: NH3_Edinburgh_Uptake_Rate_2021.csv containing accepted values with appropriate flags.
- Data status codes and EMEP flags provide additional context on verification and contamination status (see data flags section).

## Dataset structure and contents
- Each row corresponds to one month of data for a single site.
- Core columns (example list from the dataset description):
  - Site id
  - Site name
  - network_id
  - parameter_id
  - measurement start date
  - measurement start time
  - measurement end date
  - measurement end time
  - measurement (ammonia concentration in µg NH3 m-3)
  - less than (flag for values below detection limit)
  - verification id
  - unit id
  - Data capture (percent data capture)
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code and related flags
  - Month-Year
  - Comments (data notes)
- Concentrations are reported as average NH3 concentration for the specified exposure period (units: µg NH3 m-3).

## Data flags and codes
- Data flagging follows UK-AIR/EMEP conventions:
  - 999 and related codes indicate data capture and validity statuses.
  - 103 indicates CV of replicates > 15% with data still considered valid.
  - 781, 780, 654, 653, 652, 651, 260, 460, 647, 646, 645, 599, 593, 591, 559, 558, 557, 556, 555, 553, 532 provide context on data issues, contamination, or other qualifiers.
- EMEP flags include verification status, data issue numbers, and specific contamination or representativeness notes.

## Site information
- Edinburgh uptake rate OTC
  - Start date: 01/03/2020
  - End date: ongoing
  - Latitude: 55.863150
  - Longitude: -3.209845
  - Inlet height: 1.5 m
  - Collocated with UKA00128
- Auch
  - Start date: 01/03/2020
  - End date: ongoing
  - Latitude: 55.792160
  - Longitude: -3.242900
  - Inlet height: 1.5 m
  - Collocated with UKA00451
- Hills
  - Start date: 01/03/2020
  - End date: ongoing
  - Latitude: 54.452500
  - Longitude: -6.083340
  - Inlet height: 1.5 m
  - Collocated with UKA00293
- Chilbolton
  - Start date: 01/01/2021
  - End date: ongoing
  - Latitude: 51.149617
  - Longitude: -1.438228
  - Inlet height: 1.5 m
  - Collocated with UKA00614

## Data availability
- Final dataset file: NH3_Edinburgh_Uptake_Rate_2021.csv
- Each row contains a monthly measurement per site, with site identifiers, dates, concentrations, and quality flags.
- Spatial context: site coordinates and elevations enable mapping of ammonia concentrations across the four UK sampling locations.