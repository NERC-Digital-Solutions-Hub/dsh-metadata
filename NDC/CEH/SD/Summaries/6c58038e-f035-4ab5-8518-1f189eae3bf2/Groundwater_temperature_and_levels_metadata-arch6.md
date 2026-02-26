# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015)

## Overview
- Dataset of groundwater temperatures (°C) and levels (metres above Ordnance Datum Newlyn, ODN) from boreholes in the Conwy Valley, collected 2013–2015.
- Measurements recorded as dateTime (GMT), Temp_x.x and Water_level_x.x for multiple boreholes.
- Borehole locations are documented in Plot_locations.csv; additional location metadata is in Plot_locations_metadata.rtf.
- Groundwater_temperature_and_levels.csv contains the primary time-series data; Empty cells indicate missing data.

## Experimental design
- Three transects, each 75 metres long and 20 metres apart, across a hillslope perpendicular to the river Hiraethlyn.
- Four boreholes installed along each transect to bedrock; some locations include a second borehole (labeled as 'new' and 'old' where applicable).

## Data collection and instrumentation
- Each borehole equipped with a pressure transducer with an integrated data logger.
- Fieldwork used Cobra percussion hammer drilling; transducers included Diver (Schlumberger Water Services) or Level Troll 500 (In-Situ).
- Data retrieved periodically by reading logger data into a laptop.

## Calibration and quality control
- Barometric pressure corrections applied to convert sensor readings to depths to water table using standard calibration procedures.
- Quality control performed via visual inspection of plotted time series.

## Data structure and fields
- Groundwater_temperature_and_levels.csv includes:
  - dateTime: Date and Time (GMT)
  - Temp_1.1, Water_level_1.1
  - Temp_1.2, Water_level_1.2
  - Temp_1.3, Water_level_1.3
  - Temp_1.4, Water_level_1.4
  - Temp_2.2, Water_level_2.2
  - Temp_2.4, Water_level_2.4
  - Temp_4.1.o, Water_level_4.1.o
  - Temp_4.2.n, Water_level_4.2.n
  - Temp_4.2.o, Water_level_4.2.o
  - Temp_4.3, Water_level_4.3
  - Temp_4.4.o.d, Water_level_4.4.o.d
  - Temp_4.4.n, Water_level_4.4.n
- Borehole naming indicates location and status (e.g., .o for old, .n for new, with additional suffixes like .o.d or .o indicating combined/source data).
- 26 columns describe temperature and water level for each borehole; missing data are represented by empty cells.

## Supporting materials and metadata
- Plot_locations.csv: borehole locations.
- Plot_locations_metadata.rtf: metadata for borehole locations.

## Usage considerations and data readiness
- Suitable for cross-borehole comparisons of groundwater temperature and level dynamics over the 2013–2015 period.
- Can be joined with Plot_locations.csv for spatial analyses and with Plot_locations_metadata.rtf for metadata details.
- Be aware of missing data (empty cells) and potential inconsistencies in borehole naming conventions (old/new designations, suffixes).
- Data supports creation of time-series visualizations, summary statistics, and self-serve analytics for end users.