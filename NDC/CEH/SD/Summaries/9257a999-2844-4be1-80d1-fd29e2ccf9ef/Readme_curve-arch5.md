# Rating Curves

## Overview
- A collection of R scripts to generate rating (stage/discharge) curves using three data types: area/velocity measurements with pygmy current meters, salt dilution gauging (Slug method and Constant release method), and float/orange method (the latter two data are largely ignored due to variability; outliers are removed based on field notes).
- Aimed at producing ready-to-use datasets and visuals for discharge relationships, with outputs including plots and CSVs for further use.

## Data and Metadata Management
- Supports two sites: Aghnashini (agh.R) and Nilgiris (nlg.R); environment setup is handled by site.R, which can optionally clean up memory.
- Data types and storage are organized via a defined folder structure, with folder and file naming controlled by managefiles.R to ensure traceability across pygmy, float method, stream profiles, manual checks, and GIS shapefiles.
- Documentation and provenance are embedded in the datasets (e.g., field notes used to de-select outliers; dataset documentation records data processing steps).

## Processing Pipeline and Script Sequence
- Core sequence:
  - site.R: initializes environment for each site; optional memory cleanup.
  - useful.functs.R: utility functions (string manipulation, memory management helpers, time fixes, shapefile output, etc.), with attribution notes.
  - managefiles.R: defines directory structures and file inventories for data types; lists folders/files and cleanup targets.
  - libs.R: loads required libraries.
  - ExtractStage.R: extracts water level stage data aligned to timestamps from data sheets and writes to CSV.
  - pyg.R: processes velocity/area profiles from pygmy meters, merges with cross-section data, and outputs temporary/final datasets.
  - pyg.figs.R: assists in sizing cross-sectional regions, generates cross-section figures and GIS-ready outputs (cx_sec/wlr_XX).
  - flt.R: (listed in pipeline; purpose for filtering data not explicitly detailed here).
  - AppendSDG.R: appends salt dilution gauging (SDG) data to stage-discharge results from pygmy processing.
  - fig.R: uses ggplot2 to generate figures and outputs final CSVs.
- Additional components:
  - Slug.R (in Discharge folder): processes salt dilution gauging data; designed to be added to the processing sequence.
  - AreaStgRln.R: work-in-progress for validating consistency between stage, area, and discharge (multiple tests/plots).
  - PlotCleanRatingCurves.R: visualizes manually cleaned rating curves with field-note justifications; outputs figures and CSVs for discharge calculations.

## Data Quality, Validation, and Documentation
- Data quality emphasis:
  - Float method data deemed highly variable and excluded from final analyses.
  - Outliers identified and de-selected using accompanying field notes; processing steps documented within datasets.
  - Cross-section areas and stage data are validated by producing GIS-ready shapefiles of cross sections for area validation.
- Provenance and traceability are maintained through documented processing steps, explicit sequencing of scripts, and directory-level organization to reflect data types and stages of processing.

## Outputs, Storage, and Accessibility
- Outputs include:
  - CSV files containing stage, velocity/area, and discharge data.
  - Figures for rating curves and cross-sectional analyses.
  - GIS shapefiles representing cross sections for area validation.
- Outputs are organized into structured folders defined by managefiles.R, enabling consistent discovery and reuse across teams and sites.

## Challenges, Governance, and Next Steps
- Current gaps and planned improvements:
  - TODO: incorporate Slug.R into the main processing sequence.
  - TODO: rename and consolidate sub-routines (site.R naming adjustments).
  - TODO: expand file naming conventions for salt dilution gauging.
  - TODO: add import/bind data functions and enhance naming conventions for inputs/outputs.
  - Ongoing work on AreaStgRln.R to identify and visualize sources of errors in velocity-area measurements.
  - Documentation of model details and data stewardship notes (e.g., model make details, data organization) is pending for some components.
- These items reflect ongoing data governance efforts to improve standardization, interoperability, and reproducibility across sites and data types.