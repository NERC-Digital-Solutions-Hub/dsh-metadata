# This file describes the strain gauge (SG) and anemometer data collected for 19 trees in Danum Valley, Malaysia.

## Overview
- Location: Danum Valley, Malaysia; field centre coordinates: 4°57'53.0"N 117°48'18.3"E.
- Study context: Trees are part of the 50ha Smithsonian plot and the 1ha intensive carbon monitoring plot 1.
- Data types: Strain gauge (SG) and anemometer data for 19 trees.
- Data availability: Both raw data (suitable for spectral analysis) and processed data (suitable for time-series analysis) are deposited.
- Access tools: MATLAB scripts used for analysis and a more in-depth discussion are available at github.com/TobyDJackson/WindAndTrees_Danum; contact Toby Jackson at tobydjackson@gmail.com.
- Reference: Moore et al. (2004) for the strain measurement instrument.

## Data files
- Trees.csv: provides tree species ID and a census ID that identifies each tree in the Smithsonian census.
- StrainGauges.csv: provides arm length, calibration coefficient, and mounting angles required to process the raw data.

## Experimental setup and data organization
- Strain measurements: pairs of SGs mounted approximately perpendicularly to capture two axes of motion; sampling at 4 Hz; times in UTC.
- Mounting: SG pairs are attached to the trunk at various heights; typical heights include 1.3 m, 25 m, and 35 m, with the top pair attached to a 1st-order branch.
- Data loggers (organized by data logger): C1 (CR1000) with 3 SG pairs, C2 (CR1000) with 4 SG pairs on four trees, C3 (CR1000) with SGs on one tree and one on another, C4 (CR23x) with 6 SG pairs on separate trees, C5 (CR23x) with 6 SG pairs on separate trees.
- Wind data: 
  - C1_cup: 0.1 Hz wind speed data at 25 m and 35 m on tree 1 using Vector Instruments A100LK/5M cup anemometers.
  - C3_cup: 0.1 Hz wind speed data at 19 m on tree 6 with a cup anemometer.
  - C3_sonic: 1 Hz wind speed and direction data at 30 m on tree 6 with a 2D sonic anemometer (Gill Sonic 1).

## Data quality
- Overall: Data quality is good for CR1000s (C1–C3) but poor for CR23xs (C4–C5); reasons discussed in the associated publication.
- Wind data: Requires no processing.

## Data processing and formats
- Data processing pipeline (raw to analysis-ready):
  1. Raw data: measurements in millivolts from the data loggers.
  2. Calibrated data.
  3. Filtered data: long-term drift removed with a Butterworth band-pass filter.
  4. NE data: strain on the North and East facing sides of the trunk.
  5. MaxStrain data: combination of the two channels to yield maximum strain at each time step.
- Available versions: The versions described are online; additional versions are available on request.

## Notes
- The raw data are suitable for spectral analysis, while the processed data are suitable for time-series analysis.
- Most users should not need to process the data themselves.
- The publication discusses calibration and data quality considerations; contact information and GitHub repository provide additional resources.