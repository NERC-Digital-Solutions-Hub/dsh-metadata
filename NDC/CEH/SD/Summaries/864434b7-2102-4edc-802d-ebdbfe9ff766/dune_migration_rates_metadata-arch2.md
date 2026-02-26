# Dune_migration_rates.csv

## Purpose and scope
- Dataset containing dune migration rates, water depths, and flow velocities measured at cross-sections on the South Saskatchewan River, Canada, in 2017.
- Six columns: cross-section number; measurement location UTM Easting (m); measurement location UTM Northing (m); dune migration rate (m per hour); depth-averaged velocity magnitude (m per second); water depth (m).
- Collected on 12 June 2017 to characterize spatial patterns of dune migration and related flow characteristics at the same locations.

## Data collection methods
- Dune migration rates:
  - Derived from repeat aerial imagery with a grid flight pattern and 80% lateral and longitudinal image overlap.
  - Orthomosaics created using SfM software Pix4D.
  - Flight lines conducted in up to five epochs within a day; image Ground Sampling Distance (GSD) typically 0.025–0.03 m.
  - Bedform crests digitised in individual images; migration rates calculated from mean migration distance between image pairs divided by the time between image captures.
- Water depth and velocity:
  - Measured with a Sontek M9 acoustic Doppler current profiler (aDcp) mounted on a Zodiac boat.
  - Position recorded with RTK differential GPS; velocities corrected for boat speed and heading.
  - Data collected in pulse coherent mode; averaged from 7 pings per second to 1 Hz.
  - The M9 uses 9 transducers across frequencies of 0.5–3.0 MHz.
  - Measurements taken along cross-sections extending between river banks and approximately perpendicular to downstream flow.

## Data structure and variables
- Column 1: Cross-section number.
- Column 2: Measurement location UTM Easting (m).
- Column 3: Measurement location UTM Northing (m).
- Column 4: Dune migration rate (m per hour).
- Column 5: Depth-averaged velocity magnitude (m per second).
- Column 6: Water depth (m).

## Data handling, quality, and accessibility
- Uses standardised, repeatable methods for data generation (aerial imagery with SfM and ADCP measurements with RTK positioning).
- Typical practice includes storing and uploading datasets to appropriate data portals to facilitate access and reuse.

## Context and provenance
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Purpose: Provide spatial patterns of dune migration rates alongside associated flow characteristics at the same cross-sectional locations.