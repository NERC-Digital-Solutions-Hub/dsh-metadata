# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015)

## Overview
- Metadata and primary dataset for groundwater temperatures (°C) and levels (metres above Ordnance Datum Newlyn, ODN) collected in boreholes.
- Field setting: three transects across a hillslope in the Conwy Valley, near the river Hiraethlyn.
- Timeframe: 2013–2015.
- Primary file: Groundwater_temperature_and_levels.csv.
- Additional metadata references: Plot_locations.csv (borehole locations) and Plot_locations_metadata.rtf (location metadata).

## Experimental design
- Three transects, each 75 metres long and 20 metres apart, running perpendicular to the river.
- On each transect, four boreholes drilled to bedrock; some locations include a second borehole (labeled as 'new'), which do not differ from the 'old' boreholes.
- Boreholes labeled across multiple schemes (e.g., 1.1, 1.2, 1.3, 1.4; 2.2, 2.4; 4.1.o, 4.2.n, etc.).

## Data collection and instrumentation
- Sensors: pressure transducers with integrated loggers installed in each borehole.
- Data collection: periodic retrieval of borehole loggers and transfer to a laptop for processing.
- Drilling method: Cobra percussion hammer corer.
- Transducer models: Diver (Schlumberger Water Services) or Level Troll 500 (In-Situ).

## Calibration and data processing
- Barometric pressure correction applied to transducer readings.
- Depths to water table derived using standard calibrations.

## Nature and units of recorded values
- Temperature: degrees Celsius (°C).
- Water level: metres above Ordnance Datum Newlyn (ODN).

## Quality control
- Visual inspection of plotted time series used as the quality check.

## Data structure and metadata
- Groundwater_temperature_and_levels.csv contains:
  - dateTime: Date and Time (GMT).
  - Temp_*.X and Water_level_*.X: temperature and water level readings for each borehole (e.g., Temp_1.1, Water_level_1.1, Temp_1.2, Water_level_1.2, etc.).
- Borehole locations: Plot_locations.csv.
- Location metadata: Plot_locations_metadata.rtf.
- Notes:
  - Empty cells indicate missing data.
  - 26 columns in total, with various borehole identifiers (including mixed suffixes such as .o, .n, .d, etc.) to denote different boreholes or configurations.