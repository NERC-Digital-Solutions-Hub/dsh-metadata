# Classic ASCII Output Format

- Purpose: Describes how Teledyne WinRiver II exports ADC data to ASCII files, enabling standardized, reviewable environmental monitoring data over time.

## Opening a new ASCII-out data file

- On file creation, WinRiver II writes three header lines:
  - A, Description note 1 (entered via Add Note)
  - B, Description note 2 (entered via Add Note)
  - C, Descriptions of fields for subsequent data (e.g., DEPTH CELL LENGTH, NUMBER OF DEPTH CELLS, NUMBER OF PINGS PER ENSEMBLE, TIME PER ENSEMBLE, PROFILING MODE)
- These header lines document the data structure and field meanings for users.

## Data segmentation and ensemble structure

- For every new data segment (raw or averaged data), the ASCII file begins with a set of leading information:
  - The first six rows contain leader, scaling, navigation, and discharge information.
  - Starting with row seven, data are organized by bin depth; information for all bins in the current ensemble is written, then the next ensemble starts at the top.
- Ensembles are not split across files; a single file contains one or more complete ensembles.
- If data are missing from the ADCP, they are not written (no dashes or fill values).
- Known “bad data” sentinel values:
  - Velocity: -32768
  - Discharge: 2147483647
  - Latitude/Longitude: 30000

## ASCII-Out File Format (Table 7) – key content

- Each ensemble includes:
  - Ensemble time and date (year, month/day, day, hour, minute, second, hundredths, etc.)
  - Ensemble number and segment information (including total ensembles in the segment if averaging/processing)
  - Orientation data (pitch and roll)
  - Navigation time and reference (BT vs GPS) including velocity components and heading
  - Location data (latitude/longitude) and GPS-related fields (GPS vs BT reference)
  - Discharge values (middle, top, bottom estimates) and related depth/sounder information
  - Depth readings per bin (per-depth cell data), depth units, and depth-related fields (e.g., river depth, vertical beam depths)
  - Per-bin velocity data (east, north, vertical components), error, velocity backscatter, and percent-good
  - Beam depths, bin depths, and related metadata (e.g., depth interval, scale factors)
- Units and references are specified in the field descriptions; data rows are separated by spaces.

## GGA - Global Positioning System Fix Data (Table 27)

- Purpose: Documents the GGA NMEA sentence format used to convey GPS fix data within the dataset.
- Contents of a GGA sentence include:
  - UTC time of fix
  - Latitude and longitude (with hemispheres)
  - GPS quality indicator (fix status)
  - Number of satellites, horizontal dilution of precision (HDOP)
  - Antenna altitude above mean sea level and geoidal separation
  - Age of differential GPS data and differential reference station ID (if DGPS is used)
- The first two characters of the GGA sentence must match the device and are set in the Peripheral Configuration Dialog (system interconnections with the depth sounder example).
- This format supports cross-device compatibility and integration with standard GPS data streams.

## GGA NMEA Format details

- Structure (summary): hhmmss.ss, lat, N/S, lon, E/W, fix quality, satellites, HDOP, altitude, M, geoid separation, M, DGPS age, DGPS station ID.
- Used by WinRiver II to align GPS positioning with ADCP data for accurate navigation and depth correlation.

## Device compatibility note

- The first two characters of the GGA sentence must match the device type and are configured in the Peripheral Configuration Dialog.

## Relevance for environmental monitoring analysts

- Standardization: Provides a consistent, auditable ASCII format for environmental data (ADCP bins, bathymetry, discharge, and GPS).
- Data integrity: Clearly defined handling for missing and bad data improves quality control and traceability.
- Data integration: Structured outputs facilitate combining ADCP data with GPS and other datasets, supporting longitudinal analyses and policy-performance monitoring.
- Accessibility: Documentation of field definitions, units, and references supports reuse and sharing of datasets, aiding broader environmental health assessments and monitoring programs.