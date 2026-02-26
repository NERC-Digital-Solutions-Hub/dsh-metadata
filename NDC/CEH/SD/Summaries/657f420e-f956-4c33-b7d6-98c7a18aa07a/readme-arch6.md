# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Field centre located at 4°57'53.0"N 117°48'18.3"E; part of the Smithsonian 50ha plot and the 1ha intensive carbon monitoring plot 1.
- Data relate to 19 trees with species and census IDs provided in Trees.csv.
- StrainGauges.csv provides arm length, calibration coefficient, and mounting angles for processing raw data.
- Raw data (suitable for spectral analysis) and processed data (suitable for time-series analysis) are deposited.
- MATLAB analysis scripts available at github.com/TobyDJackson/WindAndTrees_Danum; contact tobydjackson@gmail.com.
- Wind data requires no processing. Data quality is good for CR1000s; CR23xs data quality is poor (discussed in the associated publication).
- Tree and wind measurements are time-stamped in UTC.

## Data files
- Trees.csv: tree species ID and census ID for Smithsonian census.
- StrainGauges.csv: SG geometry (arm length), calibration coefficients, mounting angles.

## Data collection details
- Strain measurement: SG pairs attached approximately perpendicularly to capture two axes of motion; sampling at 4 Hz.
- Anemometer setup: mounted on metal poles attached to trunks, boomed ~1.5 m.
- Data loggers (by site):
  - C1 (CR1000): 3 SG pairs at heights 1.3 m, 25 m, 35 m (top pair on 1st order branch).
  - C2 (CR1000): 4 SG pairs on four trees.
  - C3 (CR1000): first 3 SG pairs on one tree (1.3, 19, 30 m) and 1 pair on another tree.
  - C4 (CR23x): 6 SG pairs on separate trees with trigger logging.
  - C5 (CR23x): 6 SG pairs on separate trees with trigger logging.
- Wind data:
  - C1_cup: 0.1 Hz wind speed at 25 m and 35 m on tree 1 (Vector Instruments A100LK/5M).
  - C3_cup: 0.1 Hz wind speed at 19 m on tree 6.
  - C3_sonic: 1 Hz wind speed and direction at 30 m on tree 6 (2D sonic anemometer, Gill Sonic 1).
- Temporal and spatial specifics: all times UTC; wind data resolutions vary by instrument.

## Data processing and versions
- Processing pipeline:
  1) Raw data: millivolt (mV) from loggers.
  2) Calibrated data.
  3) Filtered data: long-term drift removed with Butterworth band-pass filter.
  4) NE data: strain on North and East facing sides of the trunk.
  5) MaxStrain data: maximum strain from the two channels at each time step.
- Available online: certain processing versions; additional versions available on request.

## Data quality and caveats
- Overall data quality: CR1000 data good; CR23x data poor (discussed in the related publication).
- Wind data generally requires no processing.

## Access, contact, and references
- Primary contact: tobydjackson@gmail.com
- GitHub repository for analysis scripts and discussion: github.com/TobyDJackson/WindAndTrees_Danum
- Reference: Moore et al. (2004) on an inexpensive instrument to measure the dynamic response of standing trees to wind loading.