# Fluctuating asymmetry (FA) analysis pipeline for bumblebee wing landmarks

## Overview
- A multi-file workflow to compute and analyze fluctuating asymmetry (FA) from landmark coordinates on bumblebee forewings.
- Includes orientation correction, quality control, Procrustes alignment, FA calculation, directional asymmetry assessment, repeatability testing, data resampling for temporal coverage, and GAM-based statistical analysis with plotting.

## Data inputs and orientation handling
- Input data: TPS files for all specimens and CSV files listing upside-down wings (Orientation data).
- For each species:
  - Read landmark data for left and right forewings (13 landmarks each).
  - Flip left wings to align with right wings; correct any upside-down wings to proper orientation.

## 01_Filtering_specimens_generating_FA.R
- Quality control (two mechanisms):
  - Wing angle consistency: compare difference in y-axis positions between landmarks 1 and 10 for each wing.
  - Procrustes-based similarity: measure how far each wing shape is from the species mean shape after alignment.
- Test multiple QC cut-offs to maximize quality and minimize sample loss.
- After removing low-quality specimens, perform Procrustes alignment and compute wing shape FA (Procrustes distance).
- Outputs:
  - CSVs of Procrustes distances (FA) for specimens under different QC cut-offs.
- Required inputs: TPS files; Orientation data CSV.

## 02_Testing_for_directional_asymmetry.R
- Assess directional asymmetry and measurement error:
  - Read and orient data as above; apply QC (two checks but with a fixed cut-off set: 0 for quality and 1 for angle).
- After removing low-quality specimens, Procrustes-align coordinates and create a geomorph dataframe.
- Conduct a Procrustes ANOVA to evaluate directional asymmetry and measurement error.
- Outputs:
  - CSVs with assessments of directional asymmetry and measurement error for each species and sex, under different QC cut-offs.
- Required inputs: TPS files; Orientation data CSV.

## 03_Repeatability_analysis.R
- Assess repeatability of landmarking and consistency between two landmarkers.
- Process 20 specimens per species, each landmarked three times by two landmarkers.
- Steps:
  - Procrustes alignment of coordinates.
  - Compute FA (Procrustes distance) and centroid size asymmetry.
  - Visualise FA by landmaker and landmarking date.
  - Linear mixed-effects models test for differences between landmarkers or dates.
- Outputs:
  - No explicit output files produced; analysis results are generated within the workflow.
- Required inputs: Repeatability_analysis_TPS_files.

## 04_Rarefying_FA_data_even_temporal_coverage
- Goal: achieve more even temporal coverage of FA data over the century.
- Procedure:
  - Randomly keep at least one specimen for every combination of species, caste, climate region, year, and month.
  - For years with more than 20 samples, randomly reduce to fewer than 20.
- Output:
  - Subsampled_FA_Data_0_1_v3.csv
- Required input: 20210409_updated_dataset.csv

## 05_Statistical_analysis_plot_report
- Analyses FA trends using generalized additive models (GAMs).
- Analyses include:
  - Differences in FA among the four bumblebee species.
  - Differences in FA between the first and second halves of the 20th century, by species.
  - How FA changes over the 20th century when time is treated continuously.
  - Correlations between FA and mean annual temperature and annual precipitation.
- Model selection: fit a maximal model with all variables, then simplify via stepwise removal.
- Plotting: use predict.gam() to visualise model estimates alongside raw data.
- Outputs:
  - Plots of model estimates with raw data.
- Required input: Subsampled_FA_Data_0_1_v3.csv.
- Last updated: 22/04/2022; Author: Aoife Cantwell-Jones.