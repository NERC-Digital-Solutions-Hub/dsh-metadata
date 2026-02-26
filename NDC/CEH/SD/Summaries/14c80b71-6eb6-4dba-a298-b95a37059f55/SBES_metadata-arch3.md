# SBES_2015.csv, SBES_2016.csv

## Overview
- Dataset of water depth measurements on the South Saskatchewan River, Canada, for 2015 and 2016.
- Authors: Phil Ashworth, Andrew Nicholas, Dan Parsons, Greg Sambrook Smith, Chris Unsworth.
- Files: SBES_2015.csv and SBES_2016.csv.

## Data Contents
- Columns:
  - UTM Easting (m)
  - UTM Northing (m)
  - Water depth (m)
- Purpose: to characterize spatial variations in water depth and river bed morphology along the boat track.
- Sampling extent: measurements collected along a boat track rather than a fixed grid.

## Methods and Data Collection
- Instruments: Navisound NS 215 and Reson TC 2024 200 kHz high-resolution dual-frequency SBES (single-beam echo sounder).
- Sampling rate: 10 Hz.
- Positioning: Leica 1230 Real-Time Kinematic (RTK) dGPS.
- Vessel: small zodiac boat.
- Temporal coverage: data collected in 2015 (Sept 7–9) and 2016 (Sept 2–14).
- Data processing: spikes and out-of-range data filtered; shallower-than-range data removed.

## Context and Rationale
- Collected to provide information about spatial variations in water depth and river bed morphology.
- Depth variations reflect both large-scale bar forms and smaller dune bedforms.

## Data Quality and Metadata
- Data are geolocated with explicit instrument and processing details.
- Metadata includes instrument types, sampling cadence, geolocation method, collection dates, and data processing steps (spike filtering, depth-range filtering).

## Implications for Monitoring Frameworks
- Supports understanding of river morphology and habitat—relevant for environmental health monitoring.
- Provides spatially explicit depth metrics that can inform policy evaluation, decision-making, and future monitoring design.
- Rich contextual metadata enhances data governance, transparency, and reuse.

## Data Access and Governance Considerations
- Available as two CSV files with accompanying descriptive metadata.
- The text describes collection and processing processes; explicit licensing or reuse constraints are not specified.