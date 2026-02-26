# adcp_####_xs#.csv

- Overview
  - Dataset of water depths and velocity components across cross-sections of the South Saskatchewan River, Canada.
  - Collected to inform the distribution of flow across river sections; data gathered using a Sontek M9 ADCP mounted on a zodiac or a SonTek Hydroboard.
  - Instrument position recorded with RTK dGPS; velocities corrected using boat speed and heading.

- Data content and structure
  - Five columns:
    - Column 1: Measurement location UTM Easting (m)
    - Column 2: Measurement location UTM Northing (m)
    - Column 3: Water depth (m)
    - Column 4: Depth-averaged velocity component in Easting direction (m/s)
    - Column 5: Depth-averaged velocity component in Northing direction (m/s)
  - Velocities are two horizontal components of the depth-averaged velocity; measured relative to the instrument head.

- Measurement method and data quality
  - ADCP: Sontek M9 with 9 transducers; frequencies between 0.5 and 3.0 MHz.
  - Sampling mode: pulse coherent; 7 pings per second, averaged to 1 Hz.
  - Accuracy: velocity measurements +/- 1 cm/s.
  - Data processing: corrected for boat speed and heading; cross-sections extended between both banks and aligned roughly perpendicular to downstream flow.
  - Across-section data provide information on the distribution of flow across the river.

- Temporal and spatial coverage
  - Cross-sections collected on:
    - 28/08/2015
    - 29/08/2015
    - 31/08/2015
    - 12/09/2016
    - 10/09/2016
    - 14/09/2016
    - 08/06/2017
  - Data organized into per-cross-section files named adcp_<year>_xs#.csv

- Data organization and naming
  - File naming convention uses year indicators: the first four # symbols in the file name denote the year of data collection.
  - The number after xs indicates the cross-section number (e.g., xs1, xs2, ...).
  - Examples provided include adcp_2015_xs1.csv through adcp_2015_xs24.csv, adcp_2016_xs1.csv through adcp_2016_xs20.csv, and adcp_2017_xs1.csv through adcp_2017_xs6.csv.

- Context and purpose
  - Data describe the distribution of river flow across multiple cross-sections, enabling analyses of spatial flow patterns and cross-section hydraulics.

- Access and provenance notes
  - Headings, cross-section alignment, and recording methods are documented to support traceability and reproducibility of analyses.