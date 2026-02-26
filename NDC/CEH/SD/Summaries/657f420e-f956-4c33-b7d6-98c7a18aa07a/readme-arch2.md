# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Location: 19 trees in Danum Valley, Malaysia; part of the Smithsonian 50ha plot and the 1ha intensive carbon monitoring plot 1; field center coordinates provided.
- Data types: strain gauge (SG) data and anemometer wind data; strain sampled at 4 Hz; wind data at varying resolutions; times are in UTC.
- Supporting files: Trees.csv (species ID and Smithsonian census ID); StrainGauges.csv (arm length, calibration coefficient, mounting angles).
- Data accessibility: raw data (spectral analysis) and processed data (time-series) are deposited; Matlab analysis scripts and deeper discussion available on GitHub.
- Contact: tobydjackson@gmail.com.

## Data Files and Contents
- Trees.csv: tree species ID and census ID for Smithsonian census reference.
- StrainGauges.csv: arm length, calibration coefficient, mounting angles needed to process raw data.
- Data formats: both raw (suitable for spectral analysis) and processed (suitable for time-series analysis) available online.
- GitHub resources: MATLAB scripts and in-depth discussion at github.com/TobyDJackson/WindAndTrees_Danum.
- Questions: contact provided email.

## Data Collection Details
- Strain measurement: strain pairs attached approximately perpendicularly to capture two axes of motion; measured as extension/strain.
- Data logger organization:
  - C1 (CR1000): 3 SG pairs at heights 1.3, 25, 35 m (top pair on a 1st order branch).
  - C2 (CR1000): 4 SG pairs on four trees.
  - C3 (CR1000): first 3 SG pairs on one tree (1.3, 19, 30 m) and 1 pair on another tree.
  - C4 (CR23x): 6 SG pairs on separate trees.
  - C5 (CR23x): 6 SG pairs on separate trees.
- Wind data:
  - C1_cup: 0.1 Hz wind speed at 25 and 35 m on tree 1 (cup anemometers).
  - C3_cup: 0.1 Hz wind speed at 19 m on tree 6 (cup).
  - C3_sonic: 1 Hz wind speed and direction at 30 m on tree 6 (2D sonic anemometer).
- Physical setup: anemometers mounted on metal poles boomed ~1.5 m from the trunk.
- Data quality notes: overall high quality from CR1000s; CR23xs data quality is poor (discussed in the associated publication).

## Data Processing and Versions
- Processing pipeline:
  1) Raw data in millivolts (mV) from loggers.
  2) Calibrated data.
  3) Filtered data using a Butterworth band-pass filter to remove long-term drift.
  4) NE data: strain on North and East facing trunk sides.
  5) MaxStrain: maximum of the two channels at each time step.
- Availability: online versions are provided; additional versions available on request.
- Wind data: requires no processing.

## Data Quality, Limitations, and Context
- Data quality issue: CR1000s generally reliable; CR23x units show poorer data quality; rationale and details discussed in the associated publication.
- Reference framework: Moore et al. (2004) for the strain measurement concept; Instrumentation context and limitations discussed in the related publication.

## Access, Reuse, and Contact
- Datasets include both raw and processed forms facilitating different analyses (spectral or time-series).
- Analysis resources: MATLAB scripts and discussion available via GitHub.
- For questions or further data versions, contact the provided email: tobydjackson@gmail.com.

## References
- Moore, D. et al. (2004). An inexpensive instrument to measure the dynamic response of standing trees to wind loading. Agriculture and Forest Meteorology.
- Associated publication discusses reasons for CR23x data quality issues.