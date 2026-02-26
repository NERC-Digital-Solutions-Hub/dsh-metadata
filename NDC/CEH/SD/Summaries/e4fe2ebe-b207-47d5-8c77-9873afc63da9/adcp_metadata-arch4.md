# Discovery metadata: adcp_####_xs#.csv

## Overview
- Dataset contains water depths and velocities measured at cross-sections on the South Saskatchewan River, Canada.
- File naming convention: the first four # characters indicate the year of data collection; the # after 'xs' indicates the cross-section number.

## Data contents and structure
- Five data columns:
  - Column 1: Measurement location UTM Easting (m)
  - Column 2: Measurement location UTM Northing (m)
  - Column 3: Water depth (m)
  - Column 4: Depth-averaged velocity component in Easting direction (m/s)
  - Column 5: Depth-averaged velocity component in Northing direction (m/s)

## Data collection and methods
- Collected with a Sontek M9 acoustic Doppler current profiler (aDcp) mounted on a small boat (zodiac) or SonTek Hydroboard.
- Position tracked with RTK dGPS; velocities corrected for boat speed and heading.
- Data collected in pulse coherent mode (7 pings/s), averaged to 1 Hz for improved signal-to-noise.
- Velocities are the two horizontal components of the depth-averaged velocity, measured along cross-sections that extend between banks and are perpendicular to downstream flow.
- M9 specifics: 9 transducers, frequencies 0.5–3.0 MHz; velocity measurement accuracy ±1 cm/s.

## Spatial and temporal coverage
- Cross-sections across the river width; data intended to characterize flow distribution across sections.
- Data collected on:
  - 28/08/2015 (adcp_2015_xs1.csv to adcp_2015_xs8.csv)
  - 29/08/2015 (adcp_2015_xs9.csv to adcp_2015_xs18.csv)
  - 31/08/2015 (adcp_2015_xs19.csv to adcp_2015_xs24.csv)
  - 12/09/2016 (adcp_2016_xs1.csv to adcp_2016_xs6.csv)
  - 10/09/2016 (adcp_2016_xs7.csv to adcp_2016_xs12.csv)
  - 14/09/2016 (adcp_2016_xs13.csv to adcp_2016_xs20.csv)
  - 08/06/2017 (adcp_2017_xs1.csv to adcp_2017_xs6.csv)

## Authors and source
- Chris Unsworth, Andrew Nicholas, Phil Ashworth, Dan Parsons, Greg Sambrook Smith

## Data quality, discoverability, and governance considerations for data leaders
- Metadata is explicit about measurement location, depth, velocities, and processing steps (instrument corrections, averaging, and frame of reference), aiding quality assessment and reuse.
- Clear naming convention supports discoverability and longitudinal tracking across years and cross-sections.
- Documentation covers instrumentation, acquisition mode, and accuracy, supporting trust and comparability with other river-flow datasets.
- Potential improvements for data governance:
  - Aggregate dataset-level metadata detailing spatial-temporal coverage, units, data quality flags, and any data gaps.
  - Centralized catalog entry to facilitate cross-network discovery and interoperability.
  - Clear licensing and usage rights to enable broader sharing and reuse across partners.