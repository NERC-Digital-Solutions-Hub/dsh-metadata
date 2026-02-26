# Wind and strain data collected for 21 trees in Wytham Woods

## Overview
- Study location: Wytham Woods, a mature temperate woodland in southern England (coordinates 51°46'27.2"N 1°20'20.1"W).
- Time period: September 2015 to June 2016.
- Objectives: extract resonant frequencies of trees, estimate critical wind speeds at which trees would break, and test a finite element model of tree-wind dynamics.
- Metadata connectivity: census IDs available to link trees to the Wytham Woods census dataset.

## Data collection and structure
- Strain data: collected at 4 Hz using two strain gauges per tree, attached at 1.3 m on the trunk and oriented approximately perpendicular to each other.
- Instrumentation: six data loggers; data availability is uneven due to battery and storage limitations.
- File organization: each logger’s data is stored in separate files named by the tree numbers contained (e.g., T1, T2_3, T4_7).
- Data format: first column is UTC timestamp; subsequent columns are strain measurements (two columns per tree, representing Northward and Eastward components) converted from millivolts to strain using calibration information in calibration.txt.

## Metadata and linkage
- A metadata file (tree_species_censusID.txt) enables linking each tree to the Wytham Woods census data.

## Processing and documentation
- Data processing scripts (in MATLAB) and MATLAB-specific data files are publicly available.
- A description of the data processing steps, assumptions, and sensitivities is provided in the accompanying materials on GitHub.

## Data access and governance
- Processing code and smaller usable data files are available at: github.com/TobyDJackson/WindAndTrees_Wytham
- For questions, contact: tobydjackson@gmail.com
- Wind data sources: canopy walkway measurements using a cup anemometer (Vector Instruments A100LK/5M) in winter and a Gill Sonic-1 in summer; time resolution varies by instrument.
- Local climate data (including long-term wind data) available from the Environmental Change Institute (data.ecn.ac.uk).

## Data quality, limitations, and considerations
- Data completeness varies due to battery/storage constraints affecting logger availability.
- Metadata completeness and dataset provenance are emphasized (e.g., census linkage, calibration details).
- Data processing documentation and assumptions are explicitly provided to aid interpretation and reproducibility.

## References
- P. Savill et al (2010), Wytham Woods: Oxford's Ecological Library.
- N. Butt et al (2009), Initial results from the establishment of a long-term broadleaf monitoring plot at Wytham Woods, Oxford, UK.
- Moore et al (2004), An inexpensive instrument to measure the dynamic response of standing trees to wind loading.