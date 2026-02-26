# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Data from 19 trees in Danum Valley, part of the Smithsonian 50ha plot and the 1ha intensive carbon monitoring plot 1.
- Field centre coordinates provided; trees identified in Smithsonian census.
- Includes both raw data (suitable for spectral analysis) and processed data (suitable for time-series analysis).
- MATLAB analysis scripts and deeper discussion available on GitHub; contact person provided.

## Datasets and files
- Trees.csv: tree species ID and census ID for Smithsonian identification.
- StrainGauges.csv: arm length, calibration coefficient, and mounting angles for processing raw data.
- Data versions online: raw, calibrated, filtered, NE (North/East strain), and MaxStrain data; other versions available on request.
- Processing reference: Moore et al. 2004 for the strain gauge instrument methodology.
- GitHub repository for processing scripts: TobyDJackson/WindAndTrees_Danum; contact email: tobydjackson@gmail.com.

## Instrumentation and data collection
- Strain measurement: pairs of SGs attached approximately perpendicularly to capture two axes of motion, monitored at 4 Hz, times in UTC.
- Wind measurement: different resolutions by instrument; boomed ~1.5 m from trunk.
- Anemometers and logger organization:
  - C1 CR1000: 3 SG pairs on tree heights 1.3, 25, 35 m (top pair on 1st order branch).
  - C2 CR1000: 4 SG pairs on four trees.
  - C3 CR1000: first 3 SG pairs on one tree (1.3, 19, 30 m) and 1 pair on another tree.
  - C4 CR23x: 6 SG pairs on separate trees (triggered logging).
  - C5 CR23x: 6 SG pairs on separate trees (triggered logging).
- Wind data specifics:
  - C1_cup: 0.1 Hz wind speed at 25 and 35 m on tree 1 (cup anemometers).
  - C3_cup: 0.1 Hz wind speed at 19 m on tree 6 (cup anemometer).
  - C3_sonic: 1 Hz wind speed and direction at 30 m on tree 6 (2D sonic anemometer).

## Data organization and storage
- Data organized by data logger (C1–C5) with associated SG pairs and heights.
- Includes both raw voltage data from loggers and processed data products listed above.
- Field center coordinates and tree localization provided to support dataset discoverability and reuse.

## Data processing and quality
- Processing pipeline:
  1) Raw data in mV from data loggers.
  2) Calibrated data.
  3) Filtered data (Butterworth band-pass to remove long-term drift).
  4) NE data (strain on North and East facing sides).
  5) MaxStrain data (maximum of the two channels per time step).
- Data quality notes:
  - CR1000-based data generally good.
  - CR23x-based data quality described as poor in the associated publication.
  - Wind data requires no processing beyond recording.

## Metadata and provenance
- Strain gauge mounting details (arm length, calibration coefficients, mounting angles) captured in StrainGauges.csv to support reproducibility.
- Tree identities and census linkage provided via Trees.csv.
- Publication reference and instrument background documented to contextualize measurement approach.

## Access, resources, and contact
- GitHub: TobyDJackson/WindAndTrees_Danum
- Contact: tobydjackson@gmail.com
- Availability of additional processing versions or datasets upon request.