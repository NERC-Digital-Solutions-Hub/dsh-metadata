# Rating Curves

## Overview
- A collection of scripts to create rating or stage/discharge curves using three data types: 
  - Area/velocity measurements from pygmy current meters and stream profiles
  - Salt dilution gauging (slug method and constant release method)
  - Float or orange method
- Note: float/constant release data show high variability between repeats and are ignored; outliers are de-selected based on field notes; the data processing steps are documented within the datasets.
- The workflow is designed to be reproducible and traceable, with explicit sequencing and data management.

## Data types, sources, and quality considerations
- Data sources include:
  - Pygmy current meter velocity measurements and cross-sectional profiles
  - Stream stage data tied to time stamps
  - Salt dilution gauging data (slug and constant release; slug data noted as to be integrated)
- Data quality and processing notes:
  - Outliers removed using field notes
  - There is attention to scale and local-level data availability; challenges around data access, standardization, and integration across datasets are acknowledged
  - Plans to keep datasets discoverable with metadata

## Script sequence and workflow
- Core processing chain:
  - site.R -> useful.functs.R -> managefiles.R -> libs.R -> ExtractStage.R -> disch_pyg_figs.R -> pyg.R -> flt.R -> AppendSDG.R -> fig.R
- TODO: Add Slug.R script to the processing sequence (discharge processing for salt dilution data)

## Site configuration and environment
- site.R sets up environments for two sites:
  - agh.R for Aghnashini
  - nlg.R for Nilgiris
- Includes optional memory cleanup (uncomment to enable)

## Core helpers and data management
- useful.functs.R provides common utilities to reduce code size, including:
  - String manipulation helpers (substrLeft/Right)
  - is.even/odd checks
  - Memory management helpers (ls.objects, lsos)
  - File management (delfiles)
  - Time/date corrections (fixtime)
  - shapefile output helper (writeshape)
- managefiles.R defines and organizes folders for:
  - Pygmy current meters data, float method data, stream profiles, manual profiles, and ESRI shapefiles
  - File and folder naming conventions and dataset inventories
- libs.R loads required libraries for the entire workflow

## Data extraction and stage information
- ExtractStage.R extracts the water level stage given data and timestamps, aligning with outputs from WLR scripts
- Outputs are saved to CSV and R objects for downstream processing

## Velocity-area processing and cross-section visualization
- pyg.figs.R (and pyg.figs.R: Chunk-based sections)
  - Used to assist in determining cross-sectional region sizes for velocity profiles
  - Produces figures showing stream cross-section and velocity meter locations
  - Outputs guide creation of cross-section files under cx_sec/wlr_XX for GIS validation
- pyg.R (and associated chunks)
  - Processes velocity-area profiles for each station
  - For each station folder:
    - Matches cross-section data with processed stage data
    - Merges velocity readings with cross-section areas
    - Calculates average velocities at specified heights (e.g., 60%, 20%, 80%)
    - Writes velocity data per section, with appropriate corrections, and combines with cross-section areas
  - Outputs include figures and GIS shapefiles, enabling area/velocity ratings to be visualized and validated
  - Emphasis on consistent naming conventions and data structure to facilitate merging

## Salt dilution gauging integration
- appendSDG.R
  - Attaches salt dilution gauging (SDG) values onto the file containing stage-discharge values derived from pygmy meter data
- Slug.R (not yet integrated)
  - Script to process SDG data (to be added to the main pipeline)

## Visualization and final outputs
- fig.R
  - Utilizes ggplot2 to create final rating-curve figures
  - Exports figures and a CSV data file as the final rating-curve outputs
- PlotCleanRatingCurves.R
  - Plots manually cleaned rating curves after field checks
  - Includes justifications for discarding points (e.g., poor velocity readings at low streamflow)
  - Outputs both a figure and a CSV with data used for discharge calculations
- AreaStgRln.R (work in progress)
  - Aims to identify potential errors through multiple tests, including:
    - Stage vs total profile area
    - Time vs stage overlays
    - Discharge versus area relationships
    - Overlaying profile polygons for alignment
  - Current implementation plots datasets in color to help diagnose discrepancies

## Data handling, validation, and collaboration
- Emphasis on cross-checking: combining velocity readings with cross-section data, validating against GIS shapefiles, and ensuring consistency across datasets
- Collaboration notes include plans for naming conventions improvements, adding missing data bindings, and enhancing graphing functions to reduce code duplication

## Ongoing improvements and future work
- Add Slug.R into the processing pipeline to incorporate slug-derived SDG data more comprehensively
- Rename and reorganize scripts to standardize naming conventions and reduce ambiguity
- Expand helper functions to automate graph generation and file naming
- Improve methods to harmonize data from multiple sources and scales, ensuring robust handling of local-scale data challenges
- Continue work on AreaStgRln.R for error diagnostics and improved reliability of velocity-area relationships

## Summary of outputs
- Figures and CSV files representing rating curves
- GIS shapefiles for cross-sections and area/velocity relationships
- Processed stage and velocity datasets aligned by time and station
- Documentation embedded in datasets and scripts to facilitate auditability and reuse