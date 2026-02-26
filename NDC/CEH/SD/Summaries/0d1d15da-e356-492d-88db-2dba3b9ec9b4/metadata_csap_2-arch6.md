# Half-hourly water level and temperature measurements from seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- Automated time series of water level and temperature at half-hourly intervals spanning 2018–2020.
- Seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru.
- Data collected with Solinst Leveloggers installed in perforated plastic tube dipwells.
- Barometric pressure corrections applied using nearby barologgers; corrections performed with Solinst software.
- Data previously analyzed and published by Flores Llampazo et al. (2022) in Hydrological Processes.

## Data structure and content
- Single UTF-8 encoded CSV file: CSAP_2.1_Dipwell_loggers.csv.
- Columns (first row headers): Plot_code, Date, Time, Level, Temperature.
- Date: text format dd/mm/yyyy.
- Time: decimal fraction of day.
- Level: water depth in metres relative to dipwell datum; positive indicates increasing depth.
- Temperature: degrees Celsius.
- NA indicates no data recorded.
- Geographical coverage: latitude -4.07 to -5.88, longitude -73.27 to -74.83.

## Data quality and processing
- Data downloaded from field loggers; checked for plausibility (sense checks).
- Corrected for atmospheric pressure variations using Solinst Levelogger software.
- Quality assurance notes indicate standard field QA processes were applied.

## Metadata and provenance
- Plot_code serves as the site identifier.
- Funded by UKRI-NERC, grant NE/R000751/1.
- Principal Investigator: Dr Ian Lawson (contact provided in the dataset notes).
- Data provenance aligns with the 2018–2020 deployment at seven wetland sites and links to published work (Flores Llampazo et al., 2022).

## Access, usage, and licensing
- Data available in a single CSV file, suitable for self-service analysis and dashboarding.
- NA values denote missing measurements; time and date require parsing for time-series analyses.
- Related publication provides methodological context and validation.

## Considerations for analysis
- Time representation: Time is a decimal fraction of the day; convert to standard HH:MM for readability.
- Level values are relative to an arbitrary dipwell datum; cross-site comparisons require consistent reference frames.
- Temperature and water level are measured at half-hourly intervals; ensure consistent resampling if aggregating.
- Barometric corrections rely on nearby barologger data; verify proximity and calibration when reusing data.
- Site-specific plotting codes needed to map measurements to locations.

## Related publications and references
- Flores Llampazo et al. (2022). Hydrological Processes. DOI: 10.1002/hyp.14690.