# This document describes the wind and strain data collected for 21 trees in Wytham Woods [1], a mature temperate woodland in southern England (51°46'27.2"N 1°20'20.1"W), from September 2015 to June 2016.

## Purpose and scope
- Objectives: extract resonant frequencies of trees, estimate critical wind speeds at which trees would break, and test a finite element model of tree-wind dynamics.
- Metadata linkage: census IDs available to connect trees to the Wytham Woods census via tree_species_censusID.txt.

## Data collected

- Strain data
  - Sampling rate: 4 Hz.
  - Instrumentation: two strain gauges per tree, attached at 1.3 m on the trunk and oriented approximately perpendicular.
  - Deployment: six data loggers; data gaps due to battery/storage limits; each logger file contains data for a subset of trees (e.g., T1, T2_3, T4_7).
  - Data format: first column = UTC datestamp; for each tree, two columns representing the two strain channels; data projected to Northward and Eastward directions; units converted from millivolts to strain using calibration.txt.
  - File organization: separate files per logger corresponding to the trees contained within.

- Wind data
  - Source: canopy walkway measurements.
  - Instruments: cup anemometer (Vector Instruments A100LK/5M) in winter; Gill Sonic-1 in summer.
  - Temporal resolution: varies between instruments.

- Climate/wind context
  - Local climate data and long-term wind data available from the Environmental Change Institute (data.ecn.ac.uk).

## Data processing and accessibility

- Processing tools
  - MATLAB scripts and MATLAB-friendly data files are available at github.com/TobyDJackson/WindAndTrees_Wytham.
  - A description of data processing, assumptions, and sensitivities is provided in the same repository.
- Calibration and metadata
  - Calibration details used to convert from mV to strain are documented in calibration.txt.
  - Metadata links to the Wytham census are available via tree_species_censusID.txt.
- Reproducibility
  - Data processing steps, assumptions, and sensitivities are described to enable replication and evaluation of analyses.

## Limitations and considerations for analysts

- Data completeness
  - Availability of data is non-uniform due to battery/storage limitations; some loggers may have intermittent data.
- Cross-dataset integration
  - Wind measurements come from different instruments with varying resolutions; care needed when aligning with strain data.
- Data access
  - Data and processing scripts are hosted publicly (GitHub); requires referencing calibration and metadata files for full interpretation.
- Potential data gaps
  - Some trees/loggers may be missing portions of time series, affecting frequency analysis and model validation at certain periods.

## How this data can be used

- Identify resonant frequencies of trees from strain time series.
- Estimate critical wind speeds for breakage and validate finite element models of tree-wind interactions.
- Correlate wind loading data with tree responses to understand determinants of mechanical stability.
- Combine with local climate data to assess context and drive predictive considerations for forest dynamics.

## References and contact

- References for data context:
  - Savill et al. (2010) Wytham Woods: Oxford’s Ecological Library.
  - Butt et al. (2009) Establishment of a long-term broadleaf monitoring plot at Wytham Woods.
  - Moore et al. (2004) An inexpensive instrument to measure the dynamic response of standing trees to wind loading.
- Contact: tobydjackson@gmail.com; GitHub repository listed above.