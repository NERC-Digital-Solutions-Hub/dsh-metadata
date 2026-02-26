# Half-hourly water level and temperature measurements from seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Automated half-hourly measurements of water level and temperature spanning 2018–2020 from seven wetland sites in Peru.
- Data collected with Solinst Leveloggers installed in perforated dipwells.
- Barometric pressure corrections applied using nearby barologgers.
- Data analysed and published by Flores Llampazo et al. (2022) in Hydrological Processes.

## Data Format and Structure
- File: CSAP_2.1_Dipwell_loggers.csv (UTF-8, comma-separated).
- Columns:
  - Plot_code: site identifier
  - Date: dd/mm/yyyy
  - Time: decimal fraction of day
  - Level: water level in metres relative to an arbitrary dipwell datum
  - Temperature: degrees Celsius
- NA indicates missing data.
- Time is recorded as a fraction of the day; Date is text.

## Data Quality and Processing
- Data downloaded from field loggers and subjected to sense checks.
- Corrected for atmospheric pressure variations using Solinst Levelogger software.
- QC steps reflect field data provenance and post-processing for consistency.

## Variables and Units
- Plot_code: site identifier
- Date: day/month/year
- Time: fraction of day
- Level: water depth in metres (positive = rising water)
- Temperature: degrees Celsius
- Location bounds: latitude -4.07 to -5.88; longitude -73.27 to -74.83
- Datum note: Level is relative to an arbitrary datum (usually top of the dipwell)

## Spatial and Temporal Coverage
- Seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru
- Time span: 2018–2020

## Access, Provenance, and Publication
- Dataset used in and associated with a 2022 Hydrological Processes article (Flores Llampazo et al.), DOI: 10.1002/hyp.14690
- Project funded by UKRI-NERC (grant NE/R000751/1); Principal Investigator: Dr Ian Lawson
- Data stewardship emphasises format, quality, metadata, discoverability, and updates

## Data Governance Considerations for Data Leaders
- Clear documentation of data collection methods, corrections (barometric pressure), and QC steps enhances reliability and reusability.
- Metadata included with field identifiers, dates, times, units, and datum references supports interoperability and future integration with broader data systems.
- Supports data discovery across platforms by providing a single, well-structured CSV file with explicit variable definitions and provenance.