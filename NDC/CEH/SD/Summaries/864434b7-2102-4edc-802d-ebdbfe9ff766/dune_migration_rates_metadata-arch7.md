# Dune_migration_rates.csv

## Overview
- Dataset containing dune migration rates, water depths, and flow velocities at cross-sections along the South Saskatchewan River, Canada, in 2017.
- Aimed at providing spatial patterns of dune migration and associated flow characteristics for GIS-based analysis and visualization.

## Data structure
- CSV file with six columns:
  - Cross-section number
  - Measurement location UTM Easting (meters)
  - Measurement location UTM Northing (meters)
  - Dune migration rate (meters per hour)
  - Depth-averaged velocity magnitude (meters per second)
  - Water depth (meters)

## Measurements and methods
- Dune migration rates:
  - Derived from repeat aerial imagery using grid flight lines with ~80% lateral and longitudinal overlap.
  - Orthomosaics created with Pix4D; image Ground Sampling Distance typically 0.025–0.03 m.
  - Dune crests digitised in individual images; migration rates calculated as mean migration distance between image pairs divided by the time between image collections.
  - Up to five epochs in a day to track bedform movement.
- Hydrodynamics:
  - Depth-averaged velocity and water depth measured with a Sontek M9 ADCP mounted on a zodiac.
  - Position logged with RTK dGPS; velocities corrected for boat speed and heading.
  - ADCP data collected along cross-sections spanning river width, perpendicular to downstream flow.
  - ADCP settings: pulse coherent mode, ~7 pings per second, averaged to 1 Hz; 9 transducers, 0.5–3.0 MHz.

## Spatial and temporal scope
- Location: South Saskatchewan River, Canada.
- Date of data collection: 12 June 2017.
- Cross-sections extend between river banks; oriented approximately perpendicular to downstream flow.
- UTM-based location data (Easting/Northing) for each measurement point.

## Processing and provenance
- Dune migration rates computed from image-derived distances over elapsed time between flight epochs.
- In-situ flow data (velocity and depth) integrated with dune migration data at corresponding cross-sections.

## GIS considerations and uses
- Suitable for map-based visualization of spatial patterns in dune migration alongside hydraulic characteristics.
- Can be linked with orthomosaic layers and other GIS datasets in a UTM coordinate framework.
- Useful for time-series analysis using multiple flight epochs; supports cross-section-based hydrodynamic and sediment transport studies.

## Data quality and notes
- Data combine remotely sensed imagery with in-situ ADCP measurements; coordinate accuracy relies on RTK dGPS.
- Datum for UTM coordinates not specified; users should confirm the datum for precise GIS alignment.
- Units are specified per column; consistency across analyses recommended.

## Authors / contact
- Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth

## Access and format
- File format: CSV
- Metadata provides measurement context, collection methods, and unit details to support proper interpretation and reuse in GIS workflows.