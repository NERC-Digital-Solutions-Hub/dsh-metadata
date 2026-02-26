# Fluctuating asymmetry analysis scripts for bumblebee museum specimens

## Overview
- A suite of R scripts designed to generate, QC, and analyse fluctuating asymmetry (FA) from bumblebee forewing landmarks.
- Focuses on data preparation, directional asymmetry and measurement error assessment, repeatability of landmarking, temporal sampling balance, and advanced statistical modelling (GAMs) to interpret FA in relation to species, time, and climate.

## Required inputs
- TPS files for all specimens (both left and right forewings landmarked).
- Orientation data CSV listing specimens with upside-down wings.
- For repeatability: TPS files for 20 specimens landmarked three times by two landmarkers.
- 20210409_updated_dataset.csv for temporal subsampling.

## Processing and QC workflow by file

- 01_Filtering_specimens_generating_FA.R
  - Read landmark data per species; flip left wings to align with right.
  - Correct orientation for upside-down wings.
  - Quality control (two mechanisms):
    - Wing angular difference: compute difference in y-axis positions between landmarks 1 and 10 for each wing.
    - Procrustes-based shape distance: compare each wing to species mean after Procrustes alignment.
  - Test multiple QC cut-offs to balance quality against sample loss.
  - Remove low-quality specimens; Procrustes-align remaining wings; compute Procrustes distance as FA.
  - Export CSVs of FA per specimen under different QC cut-offs.

- 02_Testing_for_directional_asymmetry.R
  - Assess directional asymmetry and potential measurement error.
  - Read data, flip left wings, correct orientation, apply QC (cut-offs: 0 and 1).
  - Procrustes-align; assemble geomorph dataframe; perform Procrustes ANOVA.
  - Export CSVs with directional asymmetry and measurement error by species and sex, under QC cut-offs.

- 03_Repeatability_analysis.R
  - Evaluate repeatability of landmarking (two landmarkers, three trials per specimen).
  - Convert coordinates for Procrustes alignment; compute FA (Procrustes distance) and centroid size asymmetry.
  - Visualize FA by landmarker and landmark date; fit linear mixed effects models to test landmarkers’ and dates’ effects.
  - No output files produced (likely for internal diagnostics).

- 04_Rarefying_FA_data_even_temporal_coverage
  - Achieve even temporal coverage across year, month, species, caste, and climate region.
  - Randomly retain at least one specimen for each combination; if a year has >20 samples, randomly reduce to <20.
  - Export Subsampled_FA_Data_0_1_v3.csv.

- 05_Statistical_analysis_plot_report
  - Analyze FA using generalized additive models (GAMs).
  - Questions addressed:
    - Do FA levels differ among the four bumblebee species?
    - Do FA changes differ between the first and second halves of the 20th century, by species?
    - How does FA change over the 20th century when time is treated continuously?
    - How does FA relate to mean annual temperature and annual precipitation?
  - Model-building: start with a maximal model (all variables) and simplify via stepwise removal.
  - Plot model estimates using predict.gam() alongside raw data.
  - Outputs include plots of model estimates with raw data; GAM analyses appear in manuscript supplements.

## Outputs (summary)
- FA values for each specimen under multiple QC cut-offs (CSV).
- Directional asymmetry and measurement error results by species and sex (CSV).
- Procrustes distance-based FA metrics and related repeatability diagnostics (no final outputs; internal plots/calls described).
- Subsampled FA dataset ensuring even temporal coverage (CSV).
- GAM-based model plots and associated analyses (plots and supplementary analyses).

## Key considerations for analysts
- QC is central: varying cut-offs can impact sample loss vs. data quality; multiple cut-offs are tested to optimize outcomes.
- Alignment and Procrustes methods ensure shape comparisons are scale- and orientation-invariant.
- Temporal balancing (rarefying) improves comparability across century-long data.
- The workflow links data preparation directly to statistical interpretation, facilitating transparent, reproducible analysis and reporting.