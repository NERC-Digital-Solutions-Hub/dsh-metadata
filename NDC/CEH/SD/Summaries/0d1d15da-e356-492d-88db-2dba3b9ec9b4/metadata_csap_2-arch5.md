# Half-hourly water level and temperature measurements from seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Automated half-hourly measurements of water level and temperature spanning parts of 2018–2020.
- Seven locations in Peru; data collected with Solinst Leveloggers installed in perforated plastic tube dipwells.
- Barometric pressure variations corrected using nearby barologgers.
- Data analyzed and published by Flores Llampazo et al. (2022) in Hydrological Processes.

## Data structure and contents
- File: CSAP_2.1_Dipwell_loggers.csv (UTF-8, comma-separated values)
- Columns (headers in first row): Plot_code, Date, Time, Level, Temperature
- NA indicates missing data
- Date format: dd/mm/yyyy
- Time: decimal fraction of day
- Level: water depth in metres, relative to an arbitrary dipwell datum (positive = rising depth)
- Temperature: degrees Celsius
- Geographic scope: approx. lat -4.07 to -5.88, lon -73.27 to -74.83
- Plot_code identifies each site

## Data quality and provenance
- Quality control: data downloaded from loggers in the field, sense-checked, corrected for atmospheric pressure variations using Solinst Levelogger software
- Provenance: data collection via Solinst Leveloggers; barometric correction applied; used in subsequent publication

## Metadata, standards, and governance considerations
- Metadata reflects data structure, units, formats, and geospatial footprint
- Governance notes:
  - Clarify datum used for Level measurements
  - Document barometric correction approach and any interpolation methods
  - Specify data licensing, access terms, and repository location
  - Include data custodian contact and dataset versioning information

## Project context and funding
- Funded by UKRI-NERC, grant NE/R000751/1
- Principal Investigator: Dr Ian Lawson

## Access and reuse considerations
- Suitable for sharing in environmental data portals and catalogues
- Publication provides validation context (Flores Llampazo et al., 2022) for interpretation and reuse