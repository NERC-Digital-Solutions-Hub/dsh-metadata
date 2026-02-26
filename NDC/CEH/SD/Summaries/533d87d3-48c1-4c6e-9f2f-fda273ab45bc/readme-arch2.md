# Wind and strain data collected for 21 trees in Wytham Woods

## Overview
- Describes wind and trunk strain data collected for 21 trees in Wytham Woods, a mature temperate woodland in southern England, from September 2015 to June 2016.
- Aims to: (a) extract resonant frequencies of trees, (b) estimate critical wind speeds that could cause breakage, (c) test a finite element model of tree–wind dynamics.
- Meta-data links to the Wytham Woods census (tree_species_censusID.txt available).

## Data collection and instrumentation
- Strain data collected at 4 Hz using two strain gauges per tree, mounted at 1.3 m on the trunk and oriented approximately perpendicular.
- Six data loggers used; data availability is non-uniform due to battery and storage constraints.
- Data logger files are separate and labeled by tree numbers (e.g., T1, T2_3, T4_7).
- First column in each file is UTC timestamp; subsequent columns are strain measurements (two per tree, projected to Northward and Eastward directions). Signals converted from mV to strain using calibration data in calibration.txt.

## Data structure and metadata
- Data files are organized by logger, with each file containing a subset of trees.
- Calibration and meteorological metadata enable linking strain data to tree identity and orientation.
- A census-linked metadata file supports association with tree species and census IDs.

## Processing, reproducibility, and availability
- MATLAB-based processing scripts and MATLAB-specific data files are available for data processing, with a description of processing steps, assumptions, and sensitivities.
- Processing workflow and reproducibility are documented on GitHub: github.com/TobyDJackson/WindAndTrees_Wytham.

## Wind and climate data context
- Wind data collected from the canopy walkway: winter measurements with a cup anemometer (Vector Instruments A100LK/5M) and summer measurements with a Gill Sonic-1; time resolution varies by instrument.
- Local climate data, including long-term wind data, available from the Environmental Change Institute (data.ecn.ac.uk).

## Data access and contact
- Data and associated scripts are accessible via GitHub (TobyDJackson/WindAndTrees_Wytham).
- Questions can be directed to tobydjackson@gmail.com.

## References
- Savill et al. (2010) Wytham Woods: Oxford's Ecological Library.
- Butt et al. (2009) Long-term broadleaf monitoring plot at Wytham Woods.
- Moore et al. (2004) Instrument for measuring dynamic response of standing trees to wind loading.