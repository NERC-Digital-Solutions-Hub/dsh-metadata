# adcp_####_xs#.csv

## Overview
- Dataset of water depths and velocity components measured at cross-sections along the South Saskatchewan River, Canada.
- Filename convention encodes year (####) and cross-section number (xs#).
- Measurements include depth and depth-averaged horizontal velocity components (Easting and Northing directions).

## Data structure and variables
- Five data columns:
  - Column 1: Measurement location UTM Easting (m)
  - Column 2: Measurement location UTM Northing (m)
  - Column 3: Water depth (m)
  - Column 4: Depth-averaged velocity component in Easting direction (m/s)
  - Column 5: Depth-averaged velocity component in Northing direction (m/s)

## Data collection methodology
- Instrument: Sontek M9 acoustic Doppler current profiler (aDCP) mounted on a small zodiac boat or SonTek Hydroboard.
- Positioning: RTK differential GPS (dGPS) used to record instrument position; velocities corrected for boat speed and heading.
- Measurement mode: Pulse coherent, averaged to 1 Hz (7 pings per second).
- Velocity reporting: Two horizontal components of depth-averaged velocity; accuracy of velocity measurements ±1 cm/s.
- Configuration: Cross-sections extend from bank to bank, oriented approximately perpendicular to downstream flow.

## Data coverage and file structure
- Cross-sections are labeled xs1, xs2, ... xs24 with year-specific data subfolders/files.
- Data collection dates and cross-sections included:
  - 28/08/2015: adcp_2015_xs1.csv – adcp_2015_xs8.csv
  - 29/08/2015: adcp_2015_xs9.csv – adcp_2015_xs18.csv
  - 31/08/2015: adcp_2015_xs19.csv – adcp_2015_xs24.csv
  - 12/09/2016: adcp_2016_xs1.csv – adcp_2016_xs6.csv
  - 10/09/2016: adcp_2016_xs7.csv – adcp_2016_xs12.csv
  - 14/09/2016: adcp_2016_xs13.csv – adcp_2016_xs20.csv
  - 08/06/2017: adcp_2017_xs1.csv – adcp_2017_xs6.csv

## Data provenance and context
- Authors: Chris Unsworth, Andrew Nicholas, Phil Ashworth, Dan Parsons, Greg Sambrook Smith.
- Purpose: Provide information on the distribution of river flow across cross-sections; supports environmental monitoring and analysis of spatial flow patterns.

## Data quality, standards, and accessibility
- Spatial reference: Measurements reported in UTM Easting/Northing (meters).
- Temporal coverage: Data collected across multiple years (2015–2017) with specific cross-sections per date.
- Output format: CSV files suitable for integration into standard environmental analysis workflows; coherent with the monitoring aim of assessing riverine hydraulic conditions.