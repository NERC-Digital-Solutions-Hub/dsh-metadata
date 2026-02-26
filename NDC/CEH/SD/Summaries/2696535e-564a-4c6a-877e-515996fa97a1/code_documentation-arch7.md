# Fluctuating asymmetry analysis scripts for bumblebee wing landmarks

- Purpose: Generate fluctuating asymmetry (FA) values and perform quality control on landmark data from bumblebee wings, exporting results for further analysis.
- Context: A suite of R scripts processes TPS landmark data for left and right forewings, realigns orientations, conducts quality control, and outputs FA metrics and related analyses.

## Input data and files

- TPS files for all specimens (left and right forewings with 13 landmarks each).
- Orientation data: CSVs listing which specimens have upside-down wings.
- Additional datasets referenced:
  - 20210409_updated_dataset.csv (for temporal subsampling)
  - Subsampled_FA_Data_0_1_v3.csv (output from subsampling)
  - Subsampled datasets used for model plotting (Plots of model estimates with raw data)

## Processing workflow by script

- 01_Filtering_specimens_generating_FA.R
  - Reads landmark data for each species.
  - Flips left wings to align with right wings; corrects upside-down wings.
  - Quality control (QC) using:
    - Wing angle differences (difference in y positions between landmarks 1 and 10 for each wing).
    - Procrustes-aligned mean-wing-shape differences to identify outliers.
  - Tests multiple QC cut-offs to maximize data quality while minimizing sample loss.
  - Performs Procrustes alignment after QC and computes wing shape FA (Procrustes distance).
  - Exports a CSV of Procrustes distances (FA) per specimen under different QC cut-offs.

- 02_Testing_for_directional_asymmetry.R
  - Assesses directional asymmetry and potential measurement error.
  - Applies orientation corrections (wing flipping) and QC as above (using fixed cut-offs: 0 for QC and 1 for angle).
  - Procrustes-aligns to create a geomorph dataframe and runs a Procrustes ANOVA.
  - Exports results as a CSV (directional asymmetry and measurement error by species and sex under QC cut-offs).

- 03_Repeatability_analysis.R
  - Evaluates repeatability of landmarking across two landmarkers and across dates.
  - Processes 20 specimens (left/right wings landmarked three times by two landmarkers).
  - Procrustes alignment and calculation of wing shape FA; also computes centroid size asymmetry.
  - Visualizes FA by landmarker and date; uses linear mixed effects models to test landmarkers/date effects.
  - No output files are produced by this script.

- 04_Rarefying_FA_data_even_temporal_coverage
  - Aims for even temporal coverage of FA data across century:
    - Randomly retains at least one specimen per combination of species, caste, climate region, year, and month.
    - For years with >20 samples, randomly reduces to fewer than 20.
  - Exports Subsampled_FA_Data_0_1_v3.csv.

- 05_Statistical_analysis_plot_report
  - Analyzes FA data with generalized additive models (GAMs) and creates plots.
  - Research questions:
    - Do FA levels differ among the four bumblebee species?
    - Do FA differences appear between the first and second halves of the 20th century, varying by species?
    - How does FA change across the 20th century when time is treated continuously?
    - How does FA correlate with mean annual temperature and precipitation?
  - Model selection via maximal model with all variables, then stepwise simplification.
  - Uses predict.gam() for plotting model estimates alongside raw data.
  - Outputs plots of model estimates with raw data; datasets referenced include Subsampled_FA_Data_0_1_v3.csv.

## Outputs and data products

- CSV files containing:
  - Procrustes distances (FA) per specimen under different QC cut-offs (from 01_Filtering_specimens_generating_FA.R).
  - Directional asymmetry and measurement error results by species and sex (from 02_Testing_for_directional_asymmetry.R).
  - Subsampled FA data for improved temporal coverage (Subsampled_FA_Data_0_1_v3.csv from 04_Rarefying_FA_data_even_temporal_coverage).
- Plots and model estimates:
  - GAM-based plots of FA by species, century period, and climate variables (from 05_Statistical_analysis_plot_report).

## Relevance to GIS Specialists

- Data integration: FA results are structured as tabular data (CSV) with associated metadata (species, caste, year, month, climate region), enabling GIS-style linking to spatial or environmental attributes.
- Visualization potential: FA metrics and model outputs can be mapped or overlaid with climate and regional data to explore spatial-temporal patterns.
- Data quality emphasis: The QC steps (wing orientation, angle differences, Procrustes alignment) align with GIS data quality practices (consistency, provenance, and transformation of geometric data).
- Workflow transparency: Clear input dependencies, processing steps, and outputs support reproducibility and data lineage within GIS projects.

## Metadata and provenance

- Last updated: 22/04/2022
- Author: Aoife Cantwell-Jones