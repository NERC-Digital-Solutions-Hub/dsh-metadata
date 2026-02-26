# Dune_migration_rates.csv

- Overview
  - A dataset of dune migration rates, depth-averaged velocity, and water depth measured at cross-sections along the South Saskatchewan River, Canada, collected in 2017.

- Data content
  - Six columns:
    - Cross-section number
    - Measurement location UTM Easting (m)
    - Measurement location UTM Northing (m)
    - Dune migration rate (m per hour)
    - Depth-averaged velocity magnitude (m per second)
    - Water depth (m)

- Measurement scope
  - Spatial: cross-sections extending between river banks, oriented approximately perpendicular to downstream flow; coordinates provided in UTM.
  - Temporal: data collected on 12 June 2017; multiple UAV flights (up to five epochs in a day) with 1-hour intervals.

- Data collection methods
  - Dune migration
    - Repeat aerial imagery with a grid pattern and 80% overlap.
    - Orthomosaics created with Pix4D.
    - Flight line spacing and image overlap enable tracking bedforms.
    - Dune migration rates computed as mean migration distance between image pairs divided by the time between image captures.
    - Ground sampling distance (GSD) typically 0.025–0.03 m.
  - Hydraulics
    - Water depth and velocity measured with a Sontek M9 ADCP mounted on a zodiac.
    - Position recorded with RTK dGPS; velocities corrected for instrument head, boat speed, and heading.
    - Data collected in pulse coherent mode; averaged from 7 pings per second to 1 Hz.
    - Instrument uses 9 transducers, 0.5–3.0 MHz.

- Data processing and alignment
  - SfM photogrammetry (Pix4D) used to construct orthomosaics from UAV imagery.
  - Bedform crests digitised in images; migration rates derived from image-pair distances.
  - ADCP data aligned along cross-sections between banks and standardized to flow direction.

- Potential analyses for analysts
  - Identify spatial patterns of dune migration and their relationship to flow characteristics (depth-averaged velocity and water depth).
  - Develop predictive models linking migration rates to hydraulic variables.
  - Compare migration across cross-sections to inform river morphodynamics and management decisions.

- Provenance and metadata
  - Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
  - File: Dune_migration_rates.csv
  - Context: measurements from the South Saskatchewan River, Canada, in 2017; data collected to characterize dune migration and flow characteristics.