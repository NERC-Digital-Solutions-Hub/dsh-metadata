# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015) Water temperature (degees Celsius) and levels (metres above Ordnance Datumn Newlyn (ODN) in boreholes - Metadata for file Groundwater_temperature_and_levels.csv

## Overview
- Dataset of groundwater temperatures and water levels collected over 2013–2015 in the Conwy Valley, North Wales, UK.
- Focus is on borehole-based measurements using calibrated sensors, with data organized for time-series analysis.

## Experimental design
- Three 75-m transects, 20 m apart, across a hillslope perpendicular to the River Hiraethlyn.
- On each transect, four boreholes drilled to bedrock (locations in Plot_locations.csv); some sites include a second borehole (labeled 'new') that does not differ from 'old'.
- Aimed to capture spatial variation in groundwater temperature and level.

## Data collection and instrumentation
- Data collected with pressure transducers (integrated loggers) installed in each borehole; data periodically retrieved and read into a laptop.
- Boreholes drilled with a Cobra percussion hammer corer.
- Transducers used: Diver (Schlumberger Water Services) or Level Troll 500 (In-Situ).

## Calibration and units
- Barometric pressure corrections applied to convert transducer readings to depths to water table using standard calibrations.
- Recorded units: water temperature in degrees Celsius; water level in metres above Ordnance Datum Newlyn (ODN).

## Data structure and metadata
- Main file: Groundwater_temperature_and_levels.csv
  - Contains dateTime (GMT) and multiple pairs of Temperature and Water_level measurements for boreholes.
  - Column naming includes Temp_1.1, Water_level_1.1, Temp_1.2, Water_level_1.2, etc., with additional borehole codes (e.g., Temp_4.1.o, Water_level_4.1.o, Temp_4.4.n, etc.).
  - 26 data columns described; empty cells indicate no data.
- Borehole locations described in Plot_locations.csv.
- Metadata for borehole locations available in Plot_locations_metadata.rtf.

## Supporting documents and data access
- Plot_locations.csv provides borehole coordinates/identifiers.
- Plot_locations_metadata.rtf contains metadata for borehole locations.

## Quality control and data limitations
- Quality control performed via visual inspection of plotted time series.
- Data gaps indicated by empty cells; variability across boreholes and potential access/recording interruptions should be considered in analyses.

## Implications for data leadership and reuse
- Clear lineage: experimental design, instrumentation, calibration, and data structure documented to support governance and reproducibility.
- Discoverability: consolidated metadata and dedicated location files facilitate data discovery and reuse across projects or networks.
- Data quality considerations: known gaps and time-series QC steps inform risk assessment and data cleaning plans.
- Potential for integration: structured, multi-borehole time-series suitable for cross-borehole analyses, trend detection, and integration with broader hydrogeological datasets.