# Dune_migration_rates.csv

## Overview
- Contains dune migration rates, water depths, and velocities measured at cross-sections on the South Saskatchewan River, Canada in 2017.
- Data collected to understand spatial patterns of dune migration and related flow characteristics.

## Data content and structure
- Six data columns:
  - Cross-section number
  - Measurement location UTM Easting (m)
  - Measurement location UTM Northing (m)
  - Dune migration rate (m per hour)
  - Depth-averaged velocity magnitude (m per second)
  - Water depth (m)

## Spatial and temporal coverage
- Measurements taken along cross-sections extending between river banks, perpendicular to downstream flow.
- Collected on 12 June 2017.
- Cross-sections defined by UTM coordinates; location data enable spatial mapping of dune movement and flow fields.

## Data collection and processing methods
- Dune migration rates:
  - Obtained via repeat aerial imagery with a grid pattern (80% lateral and longitudinal overlap).
  - Orthomosaics created from images using Structure-from-Mo tion (SfM) with Pix4D.
  - Bedform crests digitised in individual images; migration rates computed from mean migration distance between image pairs divided by time between captures.
  - Flights conducted in multiple epochs (up to five in a day) at 1-hour intervals.
  - Image Ground Sampling Distance (GSD) typically 0.025–0.03 m.
- Water depth and velocity:
  - Measured with a Sontek M9 acoustic Doppler current profiler (aDcp) mounted on a zodiac boat.
  - Position tracked with RTK differential GPS; velocities corrected for boat speed and heading.
  - Data collected along cross-sections spanning river width, aligned approximately perpendicular to flow.
  - Data processing: 7 pings per second; averaged to 1 Hz; velocities relative to instrument head.

## Data quality and provenance
- High-resolution imagery and precise positioning underpin measurements (GSD and RTK-GPS noted).
- Velocity data are corrected for instrumental motion and averaged to improve signal-to-noise.
- Clear methodological documentation provided for reproducibility (image processing, flight pattern, cross-sectioning, and instrumentation).

## Usage and potential applications
- Enables analysis of spatial patterns in dune migration and their relationship to flow characteristics.
- Useful for understanding sediment transport dynamics, bedform evolution, and river morphodynamics.
- Data can inform models of dune migration rates and associated hydraulic conditions across cross-sections.

## Metadata, governance, and access
- Discovery and contextual metadata provided (file: Dune_migration_rates.csv).
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Data format: CSV with clearly defined six columns; supports discoverability, reuse, and integration with related datasets.