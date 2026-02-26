# Dune_migration_rates.csv

## Overview
- Dataset of dune migration rates, water depths, and velocity measures at cross-sections along the South Saskatchewan River, Canada, collected in 2017.

## Data content and structure
- Six columns:
  1) Cross-section number
  2) Measurement location UTM Easting (meters)
  3) Measurement location UTM Northing (meters)
  4) Dune migration rate (meters per hour)
  5) Depth-averaged velocity magnitude (meters per second)
  6) Water depth (meters)

## Measurement methods and instrumentation
- Dune migration rates:
  - Obtained from repeat aerial imagery with grid flight lines
  - 80% lateral and longitudinal overlap between images
  - Orthomosaics created using Structure-from-Motion (SfM) with Pix4D
  - Ground Sampling Distance (GSD) typically 0.025–0.03 m
  - Bedform crests digitised in individual images
  - Migration rates calculated from mean migration distance between image pairs divided by time between image collection
- Water depth and velocity:
  - Measured with a Sontek M9 acoustic Doppler current profiler (aDcp) on a zodiac
  - Position recorded with RTK differential GPS (dGPS)
  - Velocities referenced to instrument head, corrected for boat speed and heading
  - Data collected in pulse coherent mode (7 pings/s), averaged to 1 Hz
  - Instrument uses 9 transducers across frequencies 0.5–3.0 MHz
  - Measurements taken along cross-sections spanning river width, perpendicular to downstream flow

## Sampling design and temporal coverage
- Data collected on 12 June 2017
- Dune migration and flow characteristics collected along cross-sections extending between river banks

## Data processing and quality
- Dune migration rates derived from image pairs over time; processing includes constructing orthomosaics and digitising bedform crests
- Depth-averaged velocity and water depth derived from in-situ aDcp measurements with post-processing corrections for ship motion and heading
- Spatial geometry defined by cross-sections and UTM coordinates for georeferencing

## Geolocation and coordinate reference
- Measurements geolocated with UTM Easting and Northing coordinates
- Cross-sections aligned approximately perpendicular to downstream flow

## Context and usage notes
- Data are intended to reveal spatial patterns in dune migration rates and associated flow characteristics
- Combines geomorphological (dune movement) and hydrodynamic (velocity and depth) metrics for integrated analysis

## Relevance for monitoring frameworks
- Provides concrete indicators (dune migration rate, depth-averaged velocity, water depth) for environmental health monitoring related to sediment dynamics and river hydraulics
- Demonstrates end-to-end data lineage: field measurements → SfM-derived geomorphology → derived migration rates; in-situ hydrodynamics → processed velocity/depth
- Highlights data provenance, metadata richness (temporal, spatial, and methodological details), and the need for robust data governance and sharing practices to support reuse and policy evaluation
- Illustrates typical challenges for monitoring frameworks: aligning diverse data types, ensuring metadata completeness, and maintaining data quality for decision-making