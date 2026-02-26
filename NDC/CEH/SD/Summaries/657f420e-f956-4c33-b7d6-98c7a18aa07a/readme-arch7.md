# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Describes SG and anemometer data collected for 19 trees in Danum Valley, Malaysia.
- Field centre coordinates: 4°57'53.0"N, 117°48'18.3"E.
- Trees are part of the 50 ha Smithsonian plot and the 1 ha intensive carbon monitoring plot 1.
- Data includes both raw (spectral-analysis suitable) and processed (time-series suitable) data.
- MATLAB analysis scripts and deeper discussion available at GitHub: TobyDJackson/WindAndTrees_Danum.
- Contact: tobydjackson@gmail.com.

## Datasets and data structure
- Trees.csv: tree species ID and a Smithsonian census ID for each tree.
- StrainGauges.csv: arm length, calibration coefficient, and mounting angles for SGs.
- Data organization by data logger:
  - C1: CR1000 with 3 SG pairs (heights 1.3, 25, 35 m; top pair on a 1st-order branch).
  - C2: CR1000 with 4 SG pairs on four trees.
  - C3: CR1000 with first 3 SG pairs on one tree (1.3, 19, 30 m) and 1 pair on another.
  - C4: CR23x with 6 SG pairs on separate trees (triggered).
  - C5: CR23x with 6 SG pairs on separate trees (triggered).
- Wind data:
  - C1_cup: 0.1 Hz wind speed at 25 and 35 m on tree 1 (cup anemometers).
  - C3_cup: 0.1 Hz wind speed at 19 m on tree 6 (cup anemometer).
  - C3_sonic: 1 Hz wind speed and direction at 30 m on tree 6 (2D sonic anemometer).
- Data quality notes:
  - CR1000 data quality is good.
  - CR23x data quality is poor; explained in the associated publication.

## Data collection specifics
- Strain measurements: strain gauges attached approximately perpendicularly to capture two axes of motion; sampling at 4 Hz; times in UTC.
- Wind measurements: various resolutions aligned with instrument type.
- Height references for SG placements include 1.3 m, 19 m, 25 m, 30 m, 35 m, etc., with several trees monitored.
- Data colors / formats: raw data (mV from loggers) and filtered/processed time-series data.

## Data processing and availability
- Processing pipeline:
  1) Raw data (mV from logger)
  2) Calibrated data
  3) Filtered data (Butterworth bandpass to remove long-term drift)
  4) NE data (strain on North and East facing sides)
  5) MaxStrain data (max of the two channels at each time step)
- Data versions:
  - Online versions available.
  - Other versions available on request.
- Data accessibility:
  - Raw data suitable for spectral analysis; processed data suitable for time-series analysis.
- Software and repository:
  - MATLAB scripts for analysis.
  - GitHub repository: TobyDJackson/WindAndTrees_Danum.
- Contact for questions: tobydjackson@gmail.com.

## GIS and mapping considerations
- Link trees to GIS attributes via Trees.csv (species ID and Smithsonian census ID) for spatial analyses.
- Data cover multiple plots (50 ha Smithsonian plot and 1 ha intensive plot) with varying SG heights and wind measurement locations, enabling spatial/temporal correlation analyses.
- Data quality caveat (CR23x) may affect spatial analyses in certain loggers; consult publication for details.

## References and contact
- Instrument reference: Moore et al. (2004) on dynamic response measurement of standing trees to wind loading.
- GitHub repository for data and scripts: TobyDJackson/WindAndTrees_Danum.
- Primary contact: tobydjackson@gmail.com.