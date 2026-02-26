# Rating Curves

- A collection of R scripts to create rating or stage/discharge curves using multiple data sources:
  - Area/velocity measures from pygmy current meters with stream profiles
  - Salt dilution gauging via slug method, constant release method, and float method
- Note: float and constant release methods showed highly variable results between repeats and are largely ignored; field notes are used to de-select outliers. Documentation of these decisions is stored in the datasets.

## Data sources and treatment

- Datasets used:
  - Pygmy current meter velocity-area profiles
  - Salt dilution gauging data: slug method, constant release method, and float method (latter two with caveats)
- Data quality decisions:
  - Outliers removed using field notes
  - Time/date corrections and formatting handled (fixtime helper)
  - Some data (float method) deemed too variable and excluded from final analyses

## Processing workflow (script sequence)

- site.R: Sets up the environment for two sites (Aghnashini and Nilgiris) and calls other routines; can clean memory (optional)
- useful.functs.R: Helper functions to simplify procedures and reduce code size (examples: string manipulation, even/odd tests, memory management helpers, file deletion, time fixes, shapefile output)
- managefiles.R: Defines and tracks folder/file naming schemes for:
  - Pygmy meters data, float method data, stream profile data, manual checks, ESRI shapefiles, and pygmy output metrics
  - Lists folders/files for data types; supports post-script cleanup and gap checks between velocity measures and cross sections
- libs.R: Loads required libraries
- ExtractStage.R: Extracts stage data for water level recorders by matching time stamps to outputs from WLR scripts
- pyg.figs.R and pyg.figs.R (Chunked): Assists in determining cross-sectional region sizes, draws stream cross sections with velocity meter locations, and outputs figures to guide cross-section definitions
- pyg.R: Core processing of velocity-area profiles
  - Reads cross-section coordinates, merges with processed stage data
  - Calculates average velocities per section, applies correction factors, and handles repeats
  - Outputs CSVs and prepares GIS-compatible shapefiles; merges velocity with cross-section data to produce area/velocity tables
- flt.R: Handles processing for float method data (part of the workflow sequence)
- AppendSDG.R: Appends salt dilution gauging data to the existing salt dilution values (SDG) tied to stage-discharge from pygmy results
- fig.R: Generates figures using ggplot2 and writes final CSVs/assets for rating curves
- AreaStgRln.R (work in progress): Proposed tests to identify errors in velocity-area measurements, including stage-area consistency, time-stage relationships, discharge-area overlays, and polygon alignment
- PlotCleanRatingCurves.R: Plots manually cleaned rating curves after QA and field note justifications; outputs both figures and CSVs for discharge calculations

## Outputs and end-user products

- Data products:
  - CSV files linking stage, area, and velocity for cross-section segments
  - GIS shapefiles of cross sections for area calculations and QA in GIS software (e.g., Q-GIS)
  - Figures illustrating cross-sections, velocity measurements, and rating curves
- Self-serve and QA enablement:
  - Outputs designed to be reviewed, reused, and extended by end users
  - Clear provenance and alignment between velocity readings, cross sections, and discharge estimates

## Data quality, reproducibility, and governance

- Quality control:
  - Outlier removal guided by field notes
  - Time alignment and formatting corrections (fixtime)
  - Visual QA via rating curve plots and cross-section figures (PlotCleanRatingCurves.R)
- Reproducibility:
  - Documented script sequence and environment setup per site
  - Centralized data organization via managefiles.R and helpful utilities in useful.functs.R
- Documentation and future improvements:
  - TODOs include adding Slug.R to the processing sequence, renaming/subroutine organization, and improving data import/binding/graphing utilities
  - Plan to rename scripts and remove prefixes (e.g., disch_)

## Key takeaways for Data Support perspective

- Integrates multiple hydrological data sources into a unified workflow to produce rate curves and discharge relationships.
- Emphasizes data cleaning, standardization, and traceability from raw measurements to GIS-ready outputs.
- Provides end-user ready artifacts (CSV, shapefiles, and figures) to facilitate data exploration and decision-making.
- Recognizes data variability challenges (especially float method) and documents decisions to promote clarity and reuse.
- Includes ongoing development (AreaStgRln.R, Slug.R integration, and improved naming/graphing utilities) to enhance data quality and usability.