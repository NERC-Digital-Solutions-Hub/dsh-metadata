# Rating Curves

- Purpose: A collection of R scripts to construct rating (stage-discharge) curves or stage/volume cross-sections from multiple data sources.
- Data sources:
  - Area/velocity measurements using a pygmy current meter and a stream profile.
  - Salt dilution gauging (Slug method and Constant release method).
  - Float or orange method (noted as yielding highly variable results and thus ignored).
- Field notes: Used to de-select outliers and document the data processing decisions.
- Sites and environment: Two-site setup (Aghnashini and Nilgiris) with site-specific environment scripts and broader workflow.

- Processing workflow (script sequence):
  - site.R -> useful.functs.R -> managefiles.R -> libs.R -> ExtractStage.R -> disch_pyg_figs.R -> pyg.R -> flt.R -> AppendSDG.R -> fig.R
  - A TODO item to add Slug.R (salt dilution) into the processing sequence.

- Key scripts and roles:
  - site.R: Sets up environment for each site (agh and nlg); can perform memory cleanup.
  - useful.functs.R: Helper functions (string utilities, memory management helpers, time formatting fixes, shape output, etc.) with attribution notes.
  - managefiles.R: Defines and manages data and output folders, data type groupings, file lists, and cleanup routines.
  - libs.R: Loads required libraries.
  - ExtractStage.R: Extracts water level stage data from water level recorders and aligns with timestamps.
  - pyg.figs.R / pyg.figs.R (chunks): Assists in determining cross-sectional region sizes and prepares figures to guide cross-section and velocity meter placements.
  - pyg.R: Processes velocity-area profiles from pygmy meters; merges with cross-section data; computes velocity, area, and discharge relationships; prepares data for plotting and GIS outputs.
  - flt.R: Handles data from the float method (inferred from workflow naming).
  - AppendSDG.R: Appends salt-dilution gauging data to the corresponding stage-discharge dataset derived from pygmy-meter results.
  - fig.R: Uses plotting to generate final figures and exports final CSV outputs.
  - PlotCleanRatingCurves.R: Plots manually cleaned rating curves after field validation; outputs both figures and cleaned CSV data.
  - AreaStgRln.R: Work-in-progress with tests to diagnose inconsistencies in velocity-area measurements (stage vs. area, time vs. stage, discharge vs. area, overlaying profiles).

- Outputs:
  - Cross-sectional and stage-discharge relationships with associated CSV data and figures.
  - GIS-ready shapefiles representing cross-sections (for area verification and spatial analysis).
  - Final rating curves and cleaned data suitable for discharge calculations.

- Data governance and standards:
  - Emphasis on data provenance by documenting processing steps and linking to field notes.
  - Clear data organization through managefiles.R to maintain folder structures and consistent naming.
  - Metadata and quality checks implied (outlier removal, verification steps, cross-checks with GIS outputs).

- Challenges and next steps:
  - Missing Slug.R integration for salt dilution processing.
  - Ongoing efforts to standardize sub-routine naming and overall script naming conventions.
  - Further development of AreaStgRln.R and enhancements to automated quality checks.
  - Potential enhancements to generate additional graphs and directly bind data files to output structures.