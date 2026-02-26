# Half-hourly water level and temperature measurements from seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru, 2018-2020

## Overview
- A time-series dataset of water level and temperature measurements collected at half-hourly intervals across seven wetland sites in the Pastaza-Marañón Basin, Amazonian Peru.
- Data collected in 2018–2020 using Solinst Leveloggers installed in perforated plastic tube dipwells.
- Data corrected for barometric pressure variations using nearby barologgers.
- Analysed and published by Flores Llampazo et al. (2022) in Hydrological Processes.

## Data structure and content
- File: CSAP_2.1_Dipwell_loggers.csv (UTF-8, comma-separated)
- Variables (header): Plot_code, Date, Time, Level, Temperature
- Plot_code: unique site identifier
- Date: format dd/mm/yyyy
- Time: decimal fraction of day
- Level: water level in metres relative to an arbitrary datum (positive = rising depth)
- Temperature: air/water temperature in degrees Celsius
- NA indicates no data recorded
- Geographic scope: lat -4.07 to -5.88, lon -73.27 to -74.83

## Spatial and temporal context
- Seven wetland sites within the Pastaza-Marañón Basin, Amazonian Peru
- Time span: 2018–2020
- Spatial coordinates align with the dataset’s site codes for GIS mapping and layer-based analysis

## Data quality and processing
- Field data downloaded from loggers, subjected to sense checks
- Barometric correction applied using Solinst Levelogger software and nearby barologgers
- Data correction and cleaning performed prior to publication
- Data quality controlled as part of the accompanying analysis

## GIS-relevant details and potential uses
- Suitable for time-enabled GIS visualisations (e.g., maps of water level changes over time, choropleth or point-based time series)
- Can be joined with other spatial layers using Plot_code
- Useful for hydrological and environmental risk assessments, wetland monitoring, and policy-relevant analyses
- Notes for GIS work:
  - Level values are relative to an arbitrary datum; interpret depths accordingly
  - Time field is split into Date (dd/mm/yyyy) and Time (decimal day) for precise temporal mapping
  - Handle NA values as missing data in spatial analyses

## Provenance and access
- Project and funding: UKRI-NERC, grant NE/R000751/1
- Principal investigator: Dr Ian Lawson (itl2@st-andrews.ac.uk)
- Data source and publication: Flores Llampazo et al. (2022), Hydrological Processes, data-derived insights from the same dataset