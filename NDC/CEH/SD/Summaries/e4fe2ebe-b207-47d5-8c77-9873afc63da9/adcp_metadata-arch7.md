# Discovery metadata: File: adcp_####_xs#.csv

- Contains water depths and velocities measured at cross-sections on the South Saskatchewan River, Canada.
- File naming convention: adcp_####_xs#.csv
  - Four # symbols indicate the year of data collection.
  - The # after 'xs' indicates the cross-section number.

## Data Content

- Five data columns:
  - Column 1: Measurement location UTM Easting (meters)
  - Column 2: Measurement location UTM Northing (meters)
  - Column 3: Water depth (meters)
  - Column 4: Depth-averaged velocity component in Easting direction (m/s)
  - Column 5: Depth-averaged velocity component in Northing direction (m/s)
- Velocities represent the two horizontal components of depth-averaged velocity.
- Data collected to map the distribution of flow across river cross-sections.

## Collection Methodology

- Instrument: Sontek M9 acoustic Doppler current profiler (ADCP) mounted on a small zodiac boat or SonTek Hydroboard.
- Positioning: ADCP position recorded with RTK dGPS; velocities corrected for boat speed and heading.
- Measurements: Pulse coherent mode; 7 pings per second, averaged to 1 Hz for improved signal-to-noise.
- Transducers: M9 with 9 transducers, operating at 0.5–3.0 MHz.
- Alignment: Cross-sections extended between river banks and oriented approximately perpendicular to downstream flow.

## Data Processing and Quality

- Velocities reported are the two horizontal components of depth-averaged velocity.
- Velocity accuracy: ±1 cm/s.
- Data are cleaned and transformed for integration into GIS-based analyses; unit consistency (meters and meters/second) maintained.

## Data Organization and Timeline

- Data files span multiple years and cross-sections:
  - 28/08/2015: adcp_2015_xs1.csv to adcp_2015_xs8.csv
  - 29/08/2015: adcp_2015_xs9.csv to adcp_2015_xs18.csv
  - 31/08/2015: adcp_2015_xs19.csv to adcp_2015_xs24.csv
  - 12/09/2016: adcp_2016_xs1.csv to adcp_2016_xs6.csv
  - 10/09/2016: adcp_2016_xs7.csv to adcp_2016_xs12.csv
  - 14/09/2016: adcp_2016_xs13.csv to adcp_2016_xs20.csv
  - 08/06/2017: adcp_2017_xs1.csv to adcp_2017_xs6.csv
- Cross-sections numbered sequentially within each year (xs1, xs2, …), with year encoded in the filename.

## GIS Relevance

- Provides georeferenced measurements (UTM coordinates) suitable for map-based visualization of spatial flow distribution.
- Facilitates creation of spatial layers for depth, eastward velocity, and northward velocity across river cross-sections.
- Data can be integrated with other hydrological or environmental datasets for policy, planning, or public-facing GIS visualizations.