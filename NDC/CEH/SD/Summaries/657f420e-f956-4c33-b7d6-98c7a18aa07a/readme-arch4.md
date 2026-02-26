# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Describes SG and anemometer data collected for 19 trees in Danum Valley, Malaysia.
- Field centre coordinates: 4°57'53.0"N, 117°48'18.3"E.
- Trees are part of the Smithsonian 50 ha plot and the 1 ha intensive carbon monitoring plot 1.

## Data files and contents
- Trees.csv: tree species ID and census ID ( Smithsonian census identifier).
- StrainGauges.csv: arm length, calibration coefficient, and mounting angles required to process raw data.

## Data products and access
- Raw data (suitable for spectral analysis) and processed data (suitable for time-series analysis) are deposited.
- MATLAB scripts used to analyze the data are available at github.com/TobyDJackson/WindAndTrees_Danum.
- For questions, contact: tobydjackson@gmail.com.

## Data collection details
- Strain: measured with pairs of SGs attached approximately perpendicularly to capture two axes of trunk motion; sampled at 4 Hz; times in UTC.
- Wind speed: measured at various resolutions; anemometers mounted on metal poles about 1.5 m from the trunk.

## Data organization by data logger
- C1 (CR1000): 3 SG pairs (heights 1.3, 25, 35 m); top pair on a first-order branch.
- C2 (CR1000): 4 SG pairs on four trees.
- C3 (CR1000): first 3 SG pairs on one tree (1.3, 19, 30 m) and 1 pair on another tree.
- C4 (CR23x): 6 SG pairs on separate trees using a trigger system.
- C5 (CR23x): 6 SG pairs on separate trees using a trigger system.

## Wind data specifics
- C1_cup: 0.1 Hz wind speed data at 25 m and 35 m on tree 1 (cup anemometers, Vector Instruments A100LK/5M).
- C3_cup: 0.1 Hz wind speed at 19 m on tree 6 (cup anemometer).
- C3_sonic: 1 Hz wind speed and direction at 30 m on tree 6 (2D sonic anemometer, Gill Sonic 1).

## Data quality and processing status
- Data quality: CR1000 data are good; CR23x data are poor (details discussed in the associated publication).
- Wind data requires no processing.

## Data processing pipeline
- Stages:
  - Raw data: measurements in millivolts from data loggers.
  - Calibrated data.
  - Filtered data: long-term drift removed with a Butterworth band-pass filter.
  - NE data: strain on North and East-facing sides of the trunk.
  - MaxStrain data: maximum strain from the two channels at each time step.
- Available online: specified versions; additional versions available on request.

## Reference
- Moore et al. (2004), An inexpensive instrument to measure the dynamic response of standing trees to wind loading. Agriculture and Forest Meteorology.