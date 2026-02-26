# Teledyne WinRiver II Software User's Guide (P/N 957-6231-00 (August 2016)) Excerpt Summary

## Overview
- Describes Classic ASCII Output Format used by WinRiver II for exporting ADCP data.
- Covers the structure of new ASCII-out data files, including initial header lines, ensemble data organization, and how data are represented per bin and per ensemble.
- Also explains the GGA NMEA format used for GPS data integration and how device-specific settings influence output.

## Classic ASCII Output Format

- File initialization
  - Each time a new ASCII-out data file is opened, WinRiver II writes three header lines:
    - A, Field = 1. A, Description = NOTE 1 …
    - B, Field = 1. B, Description = NOTE 2 …
    - C, Field = 1. C, Description = DEPTH CELL LENGTH (cm) …
  - These lines can be populated by user notes and describe key metadata (e.g., depth cell length).

- Ensemble structure
  - For every new data segment (raw or averaged), the first six rows contain leader, scaling, navigation, and discharge information.
  - Starting with row seven, data are written in columns based on the current bin depth.
  - The encoder continues ensemble-by-ensemble without splitting ensembles across files.
  - Missing data (not sent by the ADCP) are not included in the file.
  - Known bad-data sentinel values:
    - Velocity: -32768
    - Discharge: 2147483647
    - Latitude/Longitude: 30000

- Row and field organization (highlights)
  - Row 1–3: Ensemble metadata, including ensemble time, date, ensemble number, number of ensembles in segment (if averaging/processing), pitch, and roll.
  - Reference logic: Row three fields one–five reference Bottom-Track if the reference is Bottom-Track; if the reference is GGA, they reference the GPS GGA string.
  - Beams and depth context: Beam depths are not corrected for Pitch and Roll.
  - The middle and bottom sections include velocity components, error terms, and discharge data, with references to Bottom-Track (BT), GPS (GGA/VTG), and depth measurements.
  - Depth and bin-specific data include per-bin depth, velocity readings (east, north, vertical components), velocity error, backscatter, percent-good, and derived discharge values.

- Practical notes
  - Fields are separated by one or more spaces.
  - The file size grows to accommodate at least one ensemble.
  - The structure supports both raw and processed data (segment-level context included when averaging/processing).

## GGA - Global Positioning System Fix Data

- Purpose
  - Provides time, position, and fix-related data from a GPS receiver for use with positioning and navigation in the monitoring workflow.

- Format overview
  - The GGA line follows the NMEA standard format:
    - Time (UTC)
    - Latitude and longitude with hemispheres
    - GPS quality indicator (fix type)
    - Number of satellites, HDOP, and altitude (with units)
    - Geoidal separation and related units
    - Age of differential GPS data and DGPS reference station ID (if applicable)
  - The first two characters of the GGA sentence must match the device and are configured in the Peripheral Configuration Dialog (e.g., with the depth sounder integration).

## Implications for Monitoring Frameworks

- Data interoperability
  - Outputs are structured as stable ASCII formats with clearly defined header notes and per-ensemble data, facilitating integration with external monitoring systems.
  - GPS information (GGA) is embedded, enabling spatial alignment and georeferencing of ADCP-derived metrics.

- Metadata and data quality
  - Clear indicators of data availability and quality (missing data handling, bad-data sentinel values) aid in data cleansing and quality assurance workflows.
  - The need to reference Bottom-Track vs GPS data within ensembles affects how velocity data are interpreted and reconciled with external datasets.

- Data transformation considerations
  - The requirement to transform and align fields (e.g., bin-based data, pitch/roll corrections not applied to beam depths) implies careful handling when integrating into broader environmental health monitoring dashboards or reports.
  - Some metadata and device-specific configuration (e.g., first-two-characters device matching) must be captured to ensure correct interpretation of the GGA and ADCP outputs.