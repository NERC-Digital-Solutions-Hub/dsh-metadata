# Discovery metadata: File: adcp_####_xs#.csv

## Overview
- Dataset consisting of water depths and velocity measurements across cross-sections of the South Saskatchewan River, Canada.
- Files are organized by year and cross-section (xs#); first four # symbols in the filename indicate year, # after xs indicates cross-section number.
- Authors: Chris Unsworth, Andrew Nicholas, Phil Ashworth, Dan Parsons, Greg Sambrook Smith.

## Data content and structure
- Each file contains five columns:
  1. Measurement location UTM Easting (m)
  2. Measurement location UTM Northing (m)
  3. Water depth (m)
  4. Depth-averaged velocity component in Easting direction (m/s)
  5. Depth-averaged velocity component in Northing direction (m/s)
- Velocities are depth-averaged horizontal components; coordinates are in UTM.
- Data describe the distribution of flow across river cross-sections, extending between both banks and oriented approximately perpendicular to downstream flow.

## Collection methods
- Instrument: Sontek M9 acoustic Doppler current profiler (aDcp) mounted on a small zodiac boat or SonTek Hydroboard.
- Positioning: aDcp position recorded with RTK dGPS; velocities corrected for boat speed and heading.
- Sampling: pulse coherent mode; 7 pings per second, averaged to 1 Hz to improve signal-to-noise ratio.
- Transducers: 9 transducers; frequencies between 0.5 and 3.0 MHz.
- Velocity accuracy: +/- 1 cm/s.
  
## Temporal coverage
- 28/08/2015: adcp_2015_xs1.csv – adcp_2015_xs8.csv
- 29/08/2015: adcp_2015_xs9.csv – adcp_2015_xs18.csv
- 31/08/2015: adcp_2015_xs19.csv – adcp_2015_xs24.csv
- 12/09/2016: adcp_2016_xs1.csv – adcp_2016_xs6.csv
- 10/09/2016: adcp_2016_xs7.csv – adcp_2016_xs12.csv
- 14/09/2016: adcp_2016_xs13.csv – adcp_2016_xs20.csv
- 08/06/2017: adcp_2017_xs1.csv – adcp_2017_xs6.csv

## Purpose and use cases
- Provides data to analyze spatial flow distribution across river cross-sections.
- Supports hydrological analyses, hydraulic modeling, and related data products for exploration and public dissemination.
- Can be used to create dashboards, pivot tables, or reports to facilitate self-service data access.

## Data quality, caveats, and considerations
- Velocities are two horizontal components of depth-averaged velocity; orientation and cross-section alignment are approximate to perpendicular flow.
- Data are corrected for instrument head motion using boat speed and heading.
- Cross-sections span between banks; ensure correct interpretation of UTM coordinates and cross-section identifiers when combining files.
- Users should be aware of potential formatting and naming variations across years when aggregating datasets.