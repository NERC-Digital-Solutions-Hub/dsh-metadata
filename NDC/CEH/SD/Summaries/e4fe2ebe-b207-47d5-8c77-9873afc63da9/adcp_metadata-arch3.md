# Discovery metadata and Contextual metadata: adcp_####_xs#.csv files from the South Saskatchewan River

## Overview
- Dataset comprises water depths and two horizontal components of depth-averaged velocity across river cross-sections on the South Saskatchewan River, Canada.
- File naming convention encodes year (####) and cross-section number (xs#).

## Data structure
- Each file contains five columns:
  - Column 1: Measurement location UTM Easting (m)
  - Column 2: Measurement location UTM Northing (m)
  - Column 3: Water depth (m)
  - Column 4: Depth-averaged velocity component in Easting direction (m/s)
  - Column 5: Depth-averaged velocity component in Northing direction (m/s)

## Data collection and methods
- Instrument: Sontek M9 acoustic Doppler current profiler (aDCP) mounted on a small zodiac boat or a SonTek Hydroboard.
- Positioning: aDCP position recorded with RTK dGPS; velocities corrected for instrument head motion using boat speed and heading.
- Data acquisition: pulse coherent mode; 7 pings per second, averaged to 1 Hz to improve signal-to-noise ratio.
- Velocity reference: two horizontal components of depth-averaged velocity.
- Transducers: M9 uses 9 transducers with frequencies between 0.5 and 3.0 MHz.
- Measurement geometry: cross-sections extend between both banks, oriented approximately perpendicular to downstream flow.
- Velocity data accuracy: +/- 1 cm/s.

## Purpose and scope
- Data collected to characterize the distribution of flow across cross-sections of the South Saskatchewan River.

## File and collection details
- Data were collected on:
  - 28/08/2015: adcp_2015_xs1.csv to adcp_2015_xs8.csv
  - 29/08/2015: adcp_2015_xs9.csv to adcp_2015_xs18.csv
  - 31/08/2015: adcp_2015_xs19.csv to adcp_2015_xs24.csv
  - 12/09/2016: adcp_2016_xs1.csv to adcp_2016_xs6.csv
  - 10/09/2016: adcp_2016_xs7.csv to adcp_2016_xs12.csv
  - 14/09/2016: adcp_2016_xs13.csv to adcp_2016_xs20.csv
  - 08/06/2017: adcp_2017_xs1.csv to adcp_2017_xs6.csv

## Context and metadata
- Data are accompanied by discovery and contextual metadata that describe the dataset structure, measurement approach, and file conventions.
- Location coordinates are provided in UTM (Easting/Northing).
- Data collection aimed to provide spatially distributed flow information across river cross-sections with explicit documentation of data collection methods and processing.