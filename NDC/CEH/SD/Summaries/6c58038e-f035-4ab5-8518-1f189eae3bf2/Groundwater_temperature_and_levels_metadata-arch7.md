# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015)

## Overview
- Field dataset of groundwater water temperature (°C) and water levels (metres above Ordnance Datum Newlyn, ODN) from 2013–2015 in the Conwy Valley, North Wales.
- Data collected from boreholes along three 75 m transects (20 m apart) perpendicular to the River Hiraethlyn.
- Boreholes labeled as 'old' or 'new' (second borehole at some locations) but 'new' boreholes do not differ from 'old'.

## Experimental design
- Three transects across a hillslope; each transect has four boreholes drilled to bedrock.
- Some locations feature an additional borehole (labelled 'new').
- Boreholes locations are documented in Plot_locations.csv.

## Data collection methods
- Each borehole contains a pressure transducer with an integrated data logger.
- Data are periodically retrieved and loaded into a laptop for processing.

## Fieldwork and instrumentation
- Boreholes drilled with a Cobra percussion hammer corer.
- Transducers used: Diver (Schlumberger Water Services) or Level Troll 500 (In-Situ).

## Calibration and data processing
- Barometric pressure corrections applied; transducer values converted to depths to water table using standard calibrations.

## Nature and units of recorded values
- Temperature: degrees Celsius (°C).
- Water level: metres above Ordnance Datum Newlyn (ODN).

## Quality control
- Visual inspection of plotted time series to check data integrity.

## Data structure and documentation
- Main data file: Groundwater_temperature_and_levels.csv
  - Columns include dateTime (GMT) and pairs of Temp_x.y / Water_level_x.y for multiple boreholes (e.g., Temp_1.1, Water_level_1.1, Temp_1.2, Water_level_1.2, etc.).
  - Borehole identifiers include 1.1, 1.2, 1.3, 1.4, 2.2, 2.4, 4.1.o, 4.1.n, 4.2.n, 4.2.o, 4.3, 4.4.o.d, 4.4.o, 4.4.n.
  - Empty cells indicate no data.
- Location data: Plot_locations.csv (borehole coordinates/locations).
- Metadata for locations: Plot_locations_metadata.rtf.

## How this can be used in GIS
- Join Groundwater_temperature_and_levels.csv to Plot_locations.csv using borehole identifiers to map borehole locations and align time-series data spatially.
- Visualize spatial patterns of groundwater temperature and water levels across transects.
- Create time-enabled map visualizations or generate per-borehole time-series layers for policy, client, or public-facing dashboards.

## Considerations and caveats
- Data gaps exist where cells are empty; some boreholes may have missing timestamps.
- Consistency across borehole naming conventions and metadata essential for accurate joins.
- Units: ensure consistent interpretation of water levels as metres above ODN and temperatures in °C when mapping or analyzing.