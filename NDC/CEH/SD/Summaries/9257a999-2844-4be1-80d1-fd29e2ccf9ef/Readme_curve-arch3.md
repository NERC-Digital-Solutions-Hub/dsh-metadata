# Rating Curves

- Purpose and scope
  - Aims to create rating or stage/discharge curves using three data sources: area/velocity from pygmy current meters with stream profiles, salt dilution gauging (slug method and constant release method), and float method data.
  - Float/orange method data are largely ignored due to highly variable repeats; outliers are removed using field notes. Emphasizes documentation of data processing decisions.

- Sites and environment
  - Focuses on two sites (Aghnashini and Nilgiris) with site-specific setup and routines to prepare and run analyses.

- Data sources and methods
  - Area/velocity: pygmy current meters plus stream profile data.
  - Salt dilution gauging: slug method and constant release method (integration with rating curves via SDG data).
  - Float method: collected data are considered but not retained for final rating curves due to variability.
  - Outlier handling: field notes used to de-select questionable points; data processing steps are documented within the datasets.
  - Metadata and data provenance: scripts include notes on data sources, transformations, and cleaning steps; emphasis on reproducibility.

- Workflow and scripting sequence
  - site.R: initializes environment for each site and triggers other routines; includes optional memory cleanup.
  - useful.functs.R: utility functions (string manipulation, memory management, time fixes, shapefile creation) to simplify workflows and improve readability.
  - managefiles.R: standardizes folder/file naming for different data types (pygmy meters, float method data, stream profiles, shape files, etc.); helps manage file inventories and cleanup.
  - libs.R: loads required libraries.
  - ExtractStage.R: extracts water level (stage) corresponding to time stamps from water level recorders, aligning with WLR outputs.
  - disch_pyg_figs.R and pyg.R: process velocity-area data, align stage with velocity readings, and generate plots and temporary outputs; calculate cross-sectional areas and prepare data for integration into rating curves.
  - pyg.figs.R and related chunks: create cross-section figures, identify velocity meter locations, and generate GIS-ready outputs for area calculations.
  - flt.R: (implied handling of float method data) part of the processing chain; exact functions not detailed in the provided text.
  - AppendSDG.R: appends salt dilution gauging data onto the stage-discharge data derived from pygmy meter results, enabling combined analysis.
  - fig.R: generates final figures and outputs, including CSV data files and plots for the rating curves.
  - Additional components: AreaStgRln.R (work in progress) proposes diagnostics to compare stage against area, time versus stage, and discharge versus area; PlotCleanRatingCurves.R provides cleaned rating curves with justifications for discarded points, outputting both figures and CSVs.

- Outputs and deliverables
  - Cross-sectional area calculations and area/velocity datasets for velocity-profile segments.
  - Merged stage-velocity-geometry data for rating-curve construction.
  - CSV files and plotted figures representing raw and processed rating curves.
  - GIS-ready shapefiles of cross-sections to enable validation in GIS tools (e.g., Q-GIS).
  - Cleaned rating curves with justifications for exclusions (PlotCleanRatingCurves.R).

- Data governance, quality, and reproducibility
  - Emphasizes documenting data sources, processing steps, and justifications (e.g., excluding variable float data, de-selecting outliers with field notes).
  - Uses scripts to manage metadata, ensure data are transformed and quality-assured, and enable controlled sharing of results and underlying data.
  - Outputs are designed to be reproducible via a defined script sequence and environment setup per site.

- Ongoing work and improvements
  - AreaStgRln.R is a work-in-progress to stress-test velocity-area measurements and their relationships (stage vs area, time vs stage, discharge vs area) and to visually compare overlapping profile polygons.
  - TODOs include refining subroutine names, reorganizing site-specific code, and expanding file naming conventions and additional graphing utilities.
  - Additional TODOs in related components suggest further enhancements to data ingestion, graph generation, and governance of input/output naming.

- Relevance to monitoring framework authors
  - Demonstrates a structured, governed pipeline for developing and validating environmental health indicators (rating curves) using multiple data sources.
  - Addresses common monitoring challenges: data gaps, data access, data silos, metadata quality, data transformation requirements, and transparent documentation of data handling and exclusions.
  - Provides a reproducible framework for assembling, validating, and sharing environmental metrics and their supporting datasets and visualizations.