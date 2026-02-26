# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015) Water temperature (degees Celsius) and levels (metres above Ordnance Datumn Newlyn (ODN) in boreholes - Metadata for file Groundwater_temperature_and_levels.csv

## Overview
- Describes groundwater temperature and water level data collected from boreholes in the Conwy Valley, North Wales, during 2013–2015.
- Experimental design: three 75 m transects (20 m apart) across a hillslope, perpendicular to the river Hiraethlyn; along each transect, four boreholes drilled to bedrock (with some locations having a second borehole labeled 'new'; 'new' and 'old' boreholes are not functionally different).
- Measurements: water temperature (degrees Celsius) and water level (metres above Ordnance Datum Newlyn, ODN) in each borehole.
- Data collection: pressure transducers with integrated loggers; data retrieved periodically and downloaded to a laptop.
- Calibration: barometric pressure corrections applied to convert transducer readings to depths to water table.
- Data quality: visual inspection of time series as a quality check.
- Supporting files: borehole locations in Plot_locations.csv; borehole location metadata in Plot_locations_metadata.rtf.

## Data structure and variables
- Main file: Groundwater_temperature_and_levels.csv
- Contents: dateTime (GMT) plus temperature and water level readings for each borehole.
- Borehole labeling: Temp_1.1 / Water_level_1.1, Temp_1.2 / Water_level_1.2, Temp_1.3 / Water_level_1.3, Temp_1.4 / Water_level_1.4, etc.; additional boreholes labeled with indices such as Temp_4.1.o, Water_level_4.1.o, Temp_4.2.n, Water_level_4.2.n, Temp_4.4.o.d, Water_level_4.4.o.d, Temp_4.4.n, Water_level_4.4.n.
- Column details: 26 main data columns describing temperature and water level readings per borehole; dates and times are in GMT.
- Units:
  - Temperature: degrees Celsius
  - Water level: metres above ODN Newlyn (ODN)
- Data gaps: empty cells indicate no data for that timestamp/borehole combination.

## Instruments, collection, and calibration
- Borehole drilling: Cobra percussion hammer corer.
- Sensors: pressure transducers (Diver by Schlumberger Water Services or Level Troll 500 by In-Situ).
- Data collection: integrated loggers; data retrieved periodically and downloaded to a laptop.
- Calibration: barometric pressure corrections applied to convert transducer readings to depths to water table using standard calibrations.

## Location and metadata
- Plot_locations.csv: borehole locations referenced for the transects.
- Plot_locations_metadata.rtf: metadata describing borehole locations.
- Data allow spatial analyses across transects and borehole positions along the hillslope.

## Practical considerations for analysts
- Data quality and usability:
  - Visual QC performed; reliance on plotted time series for validation.
  - Some boreholes contain missing data at various times; expect incomplete time series across sites.
- Temporal alignment:
  - Times are recorded in GMT; consider time zone alignment and potential DST effects if combining with other datasets.
- Analytical opportunities:
  - Correlations between temperature and water level within and across boreholes.
  - Temporal responses to hydrological events (events like rainfall/runoff) and lag analyses.
  - Spatial patterns along the transects to infer subsurface flow characteristics or bedrock impacts.
  - Modelling radioactive or thermal responses using multi-site time-series data, with attention to data gaps.
- Data limitations:
  - Right-scale data gaps and variability in data density across boreholes.
  - Data quality assessment is primarily visual; additional QA steps may be beneficial for rigorous modelling.

## Access and related materials
- Groundwater_temperature_and_levels.csv: primary dataset containing time-stamped temperature and water level readings per borehole.
- Plot_locations.csv: borehole geographic positions.
- Plot_locations_metadata.rtf: metadata describing borehole locations.