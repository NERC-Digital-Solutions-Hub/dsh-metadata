# This document describes the wind and strain data collected for 21 trees in Wytham Woods [1], a mature temperate woodland in southern England (51°46'27.2"N 1°20'20.1"W), from September 2015 to June 2016.

## Overview
- Objective: extract resonant frequencies of trees, estimate critical wind speeds for breakage, and test a finite element model of tree-wind dynamics.
- Metadata: census IDs link trees to the Wytham Woods census; metadata file available as tree_species_censusID.txt.
- Location and period: Wytham Woods, southern England; September 2015 to June 2016.

## Data collection and structure
- Strain data
  - Sampling rate: 4 Hz.
  - Sensors: two strain gauges per tree, attached at 1.3 m on the trunk and oriented approximately perpendicular.
  - Logging: six data loggers used; data availability is non-uniform due to battery/storage limits.
  - File naming: each logger file is separate and named by the trees it contains (e.g., T1, T2_3, T4_7).
  - Data format: first column is UTC datestamp; subsequent columns are strain measurements. There are two measurements per tree, resulting in two columns per tree, projected into Northward and Eastward directions; values converted from mV to strain using calibration.txt.
- Data provenance and organization
  - The dataset is partitioned by logger, with per-logger file contents reflecting the trees recorded by that logger.

## Data processing, scripts, and access
- Processing environment: MATLAB.
- Processing documentation: description of data processing, assumptions, and sensitivities available on GitHub.
- Code and data: MATLAB scripts and accompanying MATLAB-specific data files available at GitHub (WindAndTrees_Wytham).
- Reproducibility: detailed processing steps enable replication and validation.

## Wind and climate data
- Wind measurements
  - Source: canopy walkway wind measurements.
  - Instruments: cup anemometer (Vector Instruments A100LK/5M) in winter; Gill Sonic-1 in summer.
  - Time resolution: varies by instrument.
- Local climate data
  - Long-term wind data available from the Environmental Change Institute (data.ecn.ac.uk).

## Data access, governance, and contact
- Access and questions: tobydjackson@gmail.com; project repository on GitHub.
- References for context
  - [1] Savill et al. (2010), Wytham Woods: Oxford's Ecological Library.
  - [2] Butt et al. (2009), Long-term broadleaf monitoring plot at Wytham Woods.
  - [3] Moore et al. (2004), Instrument to measure dynamic response of standing trees to wind loading.