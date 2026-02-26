# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Location: near the field centre at 4°57'53.0"N 117°48'18.3"E; part of the Smithsonian 50ha plot and the 1ha intensive carbon monitoring plot 1.
- Data files:
  - Trees.csv: tree species ID and census ID (links to Smithsonian census).
  - StrainGauges.csv: arm length, calibration coefficient, mounting angles for data processing.
- Data availability: raw data (suitable for spectral analysis) and processed data (suitable for time-series analysis) deposited.
- Analysis resources: MATLAB scripts and in-depth discussion at github.com/TobyDJackson/WindAndTrees_Danum; contact tobydjackson@gmail.com for questions.
- Data format note: strain data are organized by data logger (C1–C5); wind data from various instruments/heights.

## Data collection details
- Strain data:
  - Measured as strain (extension/original length) using pairs of SGs attached approximately perpendicularly to capture two axes.
  - Sampling rate: 4 Hz; times in UTC.
  - Mounting: SGs on multiple heights (e.g., 1.3, 25, 35 m) on several trees; some top pairs attached to branches.
- Wind data:
  - Varied resolutions by instrument:
    - C1_cup: 0.1 Hz wind speed at 25 m and 35 m (cup anemometers).
    - C3_cup: 0.1 Hz wind speed at 19 m (cup anemometer).
    - C3_sonic: 1 Hz wind speed and direction at 30 m (2D sonic anemometer).
  - Instruments: Vector Instruments A100LK/5M (cup) and Gill Sonic 1 (sonic).
- Data quality context:
  - CR1000 loggers: overall good data quality.
  - CR23x loggers: poorer data quality; discussed in related publication.

## Data processing and products
- Processing pipeline (recommended for use):
  1. Raw data (in mV from loggers)
  2. Calibrated data
  3. Filtered data (Butterworth band-pass to remove long-term drift)
  4. NE data (strain on North and East facing sides)
  5. MaxStrain data (combination of the two channels at each time step)
- Available versions: online versions mentioned; other versions available on request.
- Data types:
  - Raw data suitable for spectral analysis.
  - Processed data suitable for time-series analysis.

## Metadata, quality, and governance
- Metadata considerations: calibration coefficients and mounting angles provided to enable processing; emphasizes provenance from SGs and loggers.
- Data governance: data sharing and transparency are facilitated via open access to raw/processed data and code, with clear attribution and contact for questions.

## References and contact
- Reference: Moore et al. (2004) on an inexpensive instrument to measure dynamic tree response to wind loading.
- Contact and access:
  - GitHub repository: TobyDJackson/WindAndTrees_Danum
  - Email: tobydjackson@gmail.com