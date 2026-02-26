# Wind and Strain Data Collected for 21 Trees in Wytham Woods

## Overview
- Describes wind and strain measurements for 21 trees in Wytham Woods, southern England, from September 2015 to June 2016.
- Objectives: extract resonant frequencies, estimate critical wind speeds for breakage, and test a finite element model of tree-wind dynamics.
- Metadata enables linking trees to the Wytham Woods census (tree_species_censusID.txt).

## Data Collection Summary
- Strain data:
  - Collected at 4 Hz using two strain gauges per tree, mounted at ~1.3 m on the trunk and oriented approximately perpendicular.
  - Six data loggers used; data availability is non-uniform due to battery/storage limitations.
  - Data logger files are separate and named by tree coverage (e.g., T1, T2_3, T4_7).
- Wind data:
  - Collected from the canopy walkway using a cup anemometer (Vector Instruments A100LK/5M) in winter and a Gill Sonic-1 in summer.
  - Time resolution varies by instrument.
- Location and timing:
  - Wytham Woods, 51°46'27.2"N, 1°20'20.1"W.
  - Study period: September 2015 – June 2016.
- Data accessibility:
  - MATLAB processing scripts and data files available on GitHub (WindAndTrees_Wytham).

## Data Structure and Formats
- Files:
  - Each logger file corresponds to a subset of trees (e.g., T1, T2_3, etc.).
- Columns:
  - First column: UTC timestamp.
  - For each tree: two columns (one per strain gauge), projected to Northward and Eastward components.
  - Raw data in millivolts (mV) converted to strain using calibration information in calibration.txt.
- Metadata:
  - Census IDs included to enable linking with the Wytham Woods census dataset.

## Data Processing and Documentation
- Processing scripts (MATLAB) and MATLAB-friendly data files provided.
- Includes detailed descriptions of data processing steps, assumptions, and sensitivities.
- Aims to support reproducibility and integration into GIS workflows.

## Data Linkage and Accessibility
- Calibration and transformation rules documented (calibration.txt).
- Links to:
  - GitHub repository: TobyDJackson/WindAndTrees_Wytham
  - Local climate data and long-term wind context from the Environmental Change Institute (data.ecn.ac.uk).
- Contact: tobydjackson@gmail.com.

## GIS relevance and Potential Applications
- Spatially linked tree data enable map-based visualization of:
  - Tree-specific strain responses and potential resonant frequencies.
  - Spatial patterning of wind loading and variability across the stand.
  - Integration with census-linked attributes for policy or ecological analyses.
- Data can be incorporated into GIS as:
  - Tree-level feature layer with attributes (censusID, coordinates, tree height/diameter if available, calibration metadata).
  - Time-series layers or linked rasters showing strain and wind metrics.
  - Basemap layers combining wind data with climate datasets from the Environmental Change Institute.

## Limitations and Considerations
- Data coverage is uneven across trees due to battery/storage constraints; not all loggers have full time series.
- Two strain measurements per tree are oriented to approximate Northward and Eastward directions; calibration required for precise directional analyses.
- Data standardization and cleaning required to combine across multiple loggers and time periods before GIS analyses.

## References
- 1) Savill et al. (2010), Wytham Woods: Oxford's Ecological Library.
- 2) Butt et al. (2009), Long-term broadleaf monitoring plot at Wytham Woods.
- 3) Moore et al. (2004), Instrumentation for measuring dynamic response to wind.