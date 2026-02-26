# Rating Curves

## Overview
- A collection of R scripts to produce rating (stage/discharge) curves using three data source families: area/velocity from pygmy current meters and stream profiles, salt dilution gauging (slug method and constant release method), and the float method.
- The float/orange data showed high repeat variability and are largely ignored; outliers are identified and removed using field notes. The process and data handling are documented within the datasets themselves.
- Outputs include processed data, figures, and shapefiles to support validation and cross-checking of discharge estimations.

## Data sources and methods
- Area/velocity measurements from pygmy current meters paired with stream profile data.
- Salt dilution gauging using:
  - Slug method
  - Constant release method
- Float or orange method data (deemed too variable; largely excluded from final use).

## Processing pipeline and workflow
- Primary script sequence:
  - site.R -> useful.functs.R -> managefiles.R -> libs.R -> ExtractStage.R -> disch_pyg_figs.R -> pyg.R -> flt.R -> AppendSDG.R -> fig.R
- TODO: integrate Slug.R (Slug.R resides in the Discharge folder) into the processing sequence.
- Outputs per step include data extraction, cross-section and velocity processing, and final plotting.

## Site setup and environment
- site.R sets up the environment for two sites: Aghnashini (agh.R) and Nilgiris (nlg.R), with optional memory cleanup.
- TODOs include renaming/subscripting cleanups and removing a “disch_” prefix to streamline naming conventions.

## Utilities and data management
- useful.functs.R provides helpers to simplify code and reduce size, including:
  - substrLeft/Right, is.even/odd
  - .ls.objects and lsos workflow for memory management
  - delfiles for cleanup
  - fixtime for time formatting fixes
  - writeshape for exporting cross-section polygons to shapefiles
- managefiles.R defines data folder structures, data type classifications (pygmy meters, float data, stream profiles, etc.), and lists files/folders for cleanup and validation.
- libs.R loads required libraries.

## Detailed processing components
- ExtractStage.R: extracts water level stage data and aligns timestamps with outputs from water level recorder scripts, saving to CSV/R objects.
- pyg.figs.R and pyg.figs.R chunks (pyg.figs.R, pyg.figs.R Chunk 1–4): assist in configuring cross-sectional regions, plotting cross-sections, identifying velocity meter locations, and preparing plots for validation.
- pyg.R (Chunk 1–5): processes velocity-area profiles, merges velocity readings with cross-section data, and prepares final outputs; includes velocity extraction, averaging by height percentage, and integration with cross-section data to derive area/velocity relationships.
- AppendSDG.R: appends salt-dilution data (SDG) to the stage-discharge data derived from pygmy results.
- fig.R: uses ggplot2 to plot the rating curves and dumps final data as CSVs and figures.
- AreaStgRln.R: a work in progress to test sources of errors in velocity-area measurements (e.g., stage vs area, time vs stage, discharge vs area, overlaying profiles). Currently plots timestamped data with color-coding to identify errors.
- PlotCleanRatingCurves.R: plots manually cleaned rating curves with justifications for discarded points, producing both figures and CSVs for use in discharge calculations.

## Outputs and validation
- Final outputs include:
  - Cleaned and raw rating curve data (CSV)
  - Plots/figures for rating curves
  - Shapefiles representing cross-sectional areas for GIS validation
- The workflow emphasizes cross-validation against field notes and manual checks to justify exclusions, ensuring data quality for environmental monitoring and policy assessment.

## Challenges and considerations
- Variability and potential unreliability of slug/constant-release salt-dilution data; ongoing integration with pygmy-derived datasets.
- Ensuring consistent naming and code structure as subroutines are migrated or renamed.
- Maintaining a robust documentation trail within datasets to track decisions about outliers and data inclusion.

## TODOs and future work
- Integrate Slug.R into the main processing sequence.
- Shift sub-routine naming to align with site.R conventions; consider removing “disch_” prefixes.
- Expand functional coverage for data binding and graph generation within a consolidated workflow.
- Complete data model details, forms, and metadata to support replication and auditing by environmental monitoring teams.