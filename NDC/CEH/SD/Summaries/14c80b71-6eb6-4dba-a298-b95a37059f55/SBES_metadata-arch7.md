# SBES_2015.csv, SBES_2016.csv

## Overview
- Water depths along the South Saskatchewan River, Canada, for 2015 and 2016.
- Data collected along the boat’s track line to capture spatial variations in water depth and river bed morphology.
- Provided as three-column CSVs suitable for GIS mapping and analysis.

## Data Content
- Columns:
  - Measurement location UTM Easting (m)
  - Measurement location UTM Northing (m)
  - Water depth (m)
- Purpose: to characterize depth variations and bedform features (large-scale bars and dune bedforms) along the river.

## Methods and Instruments
- Bathymetry: Navisound NS 215 system and Reson TC 2024 200 kHz high-resolution SBES.
- Sampling rate: 10 Hz.
- Geolocation: Leica 1230 RTK dGPS.
- Platform: small zodiac boat.

## Temporal and Sampling Details
- 2015 data collection: September 7–9, 2015.
- 2016 data collection: September 2–14, 2016.
- Data samples represent the boat’s track line during transit.

## Data Quality and Cleaning
- Data were filtered to remove spikes and errors associated with water shallower than the instrument’s measurement range.

## Spatial Reference and Coverage
- Coordinates provided as UTM Easting/Northing (in meters).
- Datum and UTM zone not specified in the metadata; users should confirm projection details for GIS work.
- Coverage is along the river reach surveyed by the boat track line rather than a fixed grid.

## How to Use in GIS
- Suitable for creating along-track bathymetric profiles, cross-sections, or interpolated bathymetric surfaces.
- Can be combined with other bathymetric or river morphology datasets to analyze bedform features.

## Limitations and Considerations
- Data are along a single track line, not a full-area grid; spatial completeness depends on survey extent.
- Spatial reference details (UTM zone/datum) need confirmation for accurate GIS integration.
- Depth accuracy is tied to instrument range and post-processing (spike removal) steps.

## Authors and Source
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Files: SBES_2015.csv, SBES_2016.csv.