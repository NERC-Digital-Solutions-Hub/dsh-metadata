# Rating Curves

## Overview
- A collection of R scripts to create rating or stage/discharge curves from multiple data sources.
- Data sources include area/velocity measurements with pygmy meters and stream profiles, salt dilution gauging (slug and constant release methods), and the float method (the latter ignored due to high variability).
- Outliers are identified and de-selected using field notes; processing steps are documented within the datasets.

## Datasets and Data Sources
- Area/velocity measurements from pygmy current meters and stream profiles.
- Salt dilution gauging data using slug method and constant release method; float/orange method data noted as highly variable and ignored.
- Field notes used to de-select outliers; processing documented in datasets.

## Processing Pipeline / Workflow
- Sequence of scripts:
  - site.R -> useful.functs.R -> managefiles.R -> libs.R -> ExtractStage.R -> disch_pyg_figs.R -> pyg.R -> flt.R -> AppendSDG.R -> fig.R
- Site-specific setup targets two sites: aghnashini (agh.R) and Nilgiris (nlg.R); optional memory cleanup.
- TODO items include shifting sub-routine naming to site.R and renaming/removing prefixes (disch_).

## Key Scripts and Roles
- site.R: Sets up environment for the two sites and orchestrates the workflow; optional cleanup.
- useful.functs.R: Utility functions to simplify procedures and reduce code size (e.g., string helpers, memory management, fixtime, writeshape). Notable functions:
  - substrLeft/Right, is.even/odd, .ls.objects, lsos, delfiles, fixtime, writeshape.
- managefiles.R: Defines and lists data folders for pygmy meters, float method data, stream profiles, manual profiles, and GIS shapefiles; supports cleanup and file naming conventions.
- libs.R: Loads required libraries.
- ExtractStage.R: Extracts stage for a water level recorder by matching data timestamps to outputs from WLR scripts.
- disch_pyg_figs.R: Generates figures related to discharge and pygmy-based analyses.
- pyg.figs.R: Assists in sizing cross-sectional regions for velocity profiles and plots cross sections with velocity meter locations; outputs to a wlr_XX folder structure.
- pyg.R: Core processing of velocity-area profiles from pygmy meters:
  - Iterates stations, binds cross-section shapes, merges with WLR stage data, and prepares data for rating curves.
  - Outputs temporary and final CSVs, prepares figures, and writes cross-sectional shapefiles.
  - Chunked processing details include merging velocity readings with cross-section data, calculating areas, and generating output shapefiles.
- flt.R: Processes float-method data; aligns velocity readings with cross-sections and outputs prepared files for integration.
- AppendSDG.R: Appends salt-dilution gauging (SDG) data to the existing stage-discharge dataset.
- fig.R: Uses ggplot2 to plot figures and export final CSV data for the rating curves.
- AreaStgRln.R: In-progress script intended to run a suite of tests to identify errors in velocity-area measurements (e.g., stage vs area, time vs stage, discharge vs area, and overlay of profiles); currently plots successive files to identify timing/scale issues.
- PlotCleanRatingCurves.R: Plots manually cleaned rating curves with field-note justifications; outputs both figures and CSVs for discharge calculations.

## Outputs and GIS Relevance
- GIS-ready outputs include cross-sectional shapefiles (via writeshape) to enable area calculations and GIS verification in platforms like QGIS.
- Final outputs include:
  - Rating-curve related figures.
  - CSV datasets suitable for discharge calculations.
  - Shapefiles representing stream cross sections for GIS analysis and validation.

## Notable Details and Quality Assurance
- Documentation emphasizes datasets and processing steps are recorded within the datasets themselves.
- Outliers are removed based on field notes; date/time corrections are handled (fixtime helper).
- Manual checks are encouraged (pyg.figs.R) to size cross sections before final processing.
- TODOs indicate planned improvements and scripting enhancements, including additional data sources (Slug.R) and naming/structuring refinements.

## Pending Improvements and Considerations for GIS Specialists
- Integrate Slug.R into the processing sequence.
- Rename and reorganize scripts to improve clarity (e.g., remove disch_ prefixes, site.R naming).
- Expand helper functions for graphing to reduce code in fig.R.
- Ensure all outputs remain GIS-friendly (consistent shapefile generation and metadata).

## End Goal
- Deliver robust rating curves and associated GIS-ready outputs (cross-section shapefiles, area calculations, figures, and CSVs) to support spatial analysis, policy discussions, and client-facing data products.