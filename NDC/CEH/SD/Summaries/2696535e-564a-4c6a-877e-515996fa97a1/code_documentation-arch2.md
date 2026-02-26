# Filtering and Analyzing Fluctuating Asymmetry Data in Bumblebee Wings

## Overview
- A workflow of five data-processing and analysis scripts to generate and assess fluctuating asymmetry (FA) in bumblebee wings from museum specimens.
- Aimed at producing standardised, quality-controlled FA outputs to support environmental health monitoring and related policy scrutiny.
- Emphasises data quality, reproducibility, and the ability to compare FA across species, time periods, and climate variables.

## Data inputs and preparation
- Input data sources:
  - TPS landmark files for left and right forewings of each specimen.
  - Orientation data specifying which specimens have upside-down wings.
- Initial preparation steps:
  - Flip left wings to align with right wings; correct orientation for upside-down wings.
  - Organise data by species for sequential processing.

## Quality control (QC) and data cleaning
- QC criteria implemented in the FA calculation script:
  - Examine wing angle differences by comparing y-axis positions between landmarks 1 and 10 for each wing.
  - Compare each specimen’s wing shape to the species mean shape after Procrustes alignment.
- Testing of QC cut-offs:
  - Multiple cut-offs evaluated to maximize data quality while minimizing sample loss.
- Output after QC:
  - Exclusion of low-quality specimens.
  - Procrustes alignment performed on remaining data.
  - Procrustes distances computed as wing shape FA and exported as CSV.

## Directional asymmetry and measurement error
- Purpose:
  - Assess directional asymmetry (DA) and potential measurement error.
- Processing steps:
  - Read landmark data, apply orientation corrections, and perform QC as in the QC-focused script.
  - Construct a geomorph data frame with Procrustes-aligned coordinates.
  - Conduct Procrustes ANOVA to evaluate DA and measurement error.
- Output:
  - CSV files detailing DA and measurement error per species and sex under defined QC cut-offs.

## Repeatability analysis
- Goal: assess landmarking repeatability between two landmarkers.
- Approach:
  - Use TPS data where 20 specimens of a single species are landmarked three times by two landmarkers.
  - Procrustes alignment and calculation of FA (wing shape) and centroid size asymmetry.
  - Visualization of FA by landmark and landmarking date.
  - Linear mixed effects model tests for significant differences by landmarker or date.
- Output:
  - No explicit output files produced; results interpreted from model outputs.

## Data balancing for temporal coverage
- Objective: achieve even temporal coverage of FA data across the century.
- Method:
  - Randomly retain at least one specimen for each combination of species, caste, climate region, year, and month.
  - For years with more than 20 samples, randomly down-sample to fewer than 20.
- Output:
  - Subsampled FA dataset exported as CSV (Subsampled_FA_Data_0_1_v3.csv).

## Statistical analysis and plotting (GAMs)
- Core analyses:
  - Compare FA across four bumblebee species.
  - Examine FA differences between the first and second halves of the 20th century, by species.
  - Model FA as a function of time (continuous) across the 20th century.
  - Assess FA correlations with mean annual temperature and annual precipitation.
- Modelling approach:
  - Generalized additive models (GAMs) with a maximal model including all candidate variables, then simplified via stepwise removal.
  - Model estimates plotted using predict.gam(), alongside raw data.
- Required input:
  - Subsampled_FA_Data_0_1_v3.csv
- Output:
  - Plots showing model estimates with corresponding raw data.

## Outputs and data stewardship
- Produced data products:
  - CSV files containing fluctuating asymmetry values per specimen across QC cut-offs.
  - CSVs for directional asymmetry and measurement error per species/sex.
  - Subsampled FA data CSV to ensure balanced temporal representation.
  - GAM-based plots and model estimate visuals linking FA to species, time, and climate variables.
- Data handling considerations:
  - Emphasis on storing and sharing standardized datasets for environmental monitoring and policy evaluation.
  - Reproducibility supported by clear input requirements and documented QC procedures.

## Relevance for environmental monitoring
- Provides a standardised pipeline to transform raw wing landmark data into comparable FA metrics.
- Enables cross-species and temporal comparisons of environmental stress indicators, with explicit QC and repeatability checks.
- Facilitates integration with climate and time-series analyses to assess how FA relates to environmental drivers and policy-relevant timelines.