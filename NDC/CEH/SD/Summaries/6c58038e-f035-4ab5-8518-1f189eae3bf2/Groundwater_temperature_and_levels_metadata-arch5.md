# Groundwater temperatures and levels from a field experiment in the Conwy Valley, North Wales, UK (2013 - 2015)

## Overview
- Dataset documenting groundwater temperatures (°C) and water levels (metres above Ordnance Datum Newlyn, ODN) from a field experiment conducted 2013–2015 in the Conwy Valley, North Wales, UK.
- Primary data file: Groundwater_temperature_and_levels.csv.
- Supporting location and metadata files: Plot_locations.csv and Plot_locations_metadata.rtf.
- Metadata emphasizes experimental design, collection methods, calibration, units, and data structure to enable discoverability and reuse.

## Experimental design and collection methods
- Experimental setup:
  - Three transects, each 75 metres long and 20 metres apart, across a hillslope perpendicular to the River Hiraethlyn.
  - Four boreholes drilled to bedrock along each transect; some locations include an additional borehole (labelled 'new') that does not differ from 'old'.
- Data collection:
  - Each borehole equipped with a pressure transducer with an integrated data logger.
  - Loggers periodically retrieved; data read into a laptop.
- Fieldwork and instrumentation:
  - Boreholes drilled with a Cobra percussion hammer corer (Van Walt Ltd).
  - Pressure transducers: Diver (Schlumberger Water Services) or Level Troll 500 (In-Situ).
- Calibration and processing:
  - Barometric pressure corrections applied; transducer data converted to depths to water table using standard calibrations.
- Time and units:
  - Date/time recorded as GMT.
  - Temperature in degrees Celsius; water levels expressed in metres above ODN Newlyn.
- Quality control:
  - Visual inspection of plotted time series.

## Data structure and content
- Groundwater_temperature_and_levels.csv:
  - Contains temperature and water level measurements for multiple boreholes.
  - Borehole columns are labeled with patterns such as Temp_1.1, Water_level_1.1, Temp_1.2, Water_level_1.2, etc.
  - Some borehole labels include suffixes (e.g., Temp_4.1.o, Water_level_4.1.o) indicating special cases or variants.
  - dateTime column records timestamps in GMT.
  - 26 data columns plus dateTime; empty cells indicate missing data.
- Plot_locations.csv:
  - Borehole location information corresponding to the data in Groundwater_temperature_and_levels.csv.
- Plot_locations_metadata.rtf:
  - Metadata describing borehole locations (structure and context for location data).

## Metadata and documentation
- File-level metadata includes:
  - Names and descriptions of data columns (temperature and water levels per borehole).
  - Units and measurement types.
  - Data provenance from field collection (instruments and calibration steps).
- Supporting documents are linked to facilitate data discovery and reuse.

## Data governance and stewardship implications
- Standardization and interoperability:
  - Ensure consistent naming conventions for boreholes and variables across datasets.
  - Maintain clear mappings between Groundwater_temperature_and_levels.csv and Plot_locations.csv.
- Metadata completeness and clarity:
  - Preserve calibration notes and instrument details to support reproducibility.
  - Document any bespoke or non-interoperable elements (e.g., special borehole codes like .o or .n suffixes).
- Data quality and provenance:
  - Retain notes from QC (visual checks) and calibration procedures to support traceability.
  - Clearly indicate missing data with empty cells and, if possible, provide rationale or data gaps.
- Data access, sharing, and updates:
  - Ensure datasets remain discoverable via catalogues and portals; keep supporting files up-to-date.
  - Establish process for updating measurements or adding new borehole data if the study is extended.
- Units and time standards:
  - Preserve GMT for time; maintain Celsius for temperature and metres above ODN for levels to avoid misinterpretation.

## Practical considerations for data stewards
- Address incomplete user needs by providing comprehensive metadata and clear linking between data and location metadata.
- Manage multiple data formats and naming conventions to ensure interoperability across analyses and platforms.
- Plan for updates or additions (e.g., new boreholes or reprocessed data) and versioning to maintain dataset integrity over time.