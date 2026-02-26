# 01_Filtering_specimens_generating_FA.R

- Purpose and scope
  - Generates fluctuating asymmetry (FA) values and performs quality control (QC) for bumblebee wing landmark data.
  - Handles input data with 13 landmarks on left and right forewings per specimen; orientation corrections applied to ensure wings lie in the same plane before analysis.

- Key data inputs
  - TPS (thin plate spline) files for all specimens.
  - Orientation data CSVs listing specimens with upside-down wings.

- Core processing steps
  - For each species:
    - Read landmark data.
    - Flip left wings to align with right wings; correct upside-down wings to proper orientation.
    - Quality control:
      - QC1: assess wing angle differences by comparing the y-axis positions of landmarks 1 and 10 for each wing (differential angle).
      - QC2: Procrustes alignment to mean wing shape for the species; evaluate how far each wing deviates from the mean.
      - Test multiple QC cut-offs to maximize data quality while minimizing sample loss.
    - Remove low-quality specimens based on QC criteria.
    - Procrustes align remaining wings.
    - Compute FA as Procrustes distances.
    - Export a CSV with FA values per specimen under different QC cut-offs.

- Outputs
  - CSV files containing fluctuating asymmetry values for each specimen under various QC cut-offs.

- Data governance considerations
  - Ensures consistent orientation and alignment through standardized Procrustes analysis.
  - Maintains traceable QC thresholds and sample-level filtering to support reproducibility and auditability.

---

## 02_Testing_for_directional_asymmetry.R

- Purpose and scope
  - Assesses directional asymmetry and potential measurement error in left vs. right forewings.

- Key data inputs
  - TPS files for all specimens.
  - Orientation data CSVs for upside-down wings.

- Core processing steps
  - For each species:
    - Load data; flip left wings to align with right and correct orientation.
    - Apply QC (two checks as in script 01, with fixed cut-offs: 0 for wing quality and 1 for angle).
    - Remove low-quality specimens.
    - Procrustes align the remaining wings and create a geomorph-compatible dataframe of coordinates.
    - Conduct a Procrustes ANOVA and export results.

- Outputs
  - CSV file detailing directional asymmetry and measurement error per species and sex under specified QC cut-offs.

- Data governance considerations
  - Provides a transparent assessment of asymmetry and measurement reliability, essential for data quality and cross-study comparability.

---

## 03_Repeatability_analysis.R

- Purpose and scope
  - Evaluates the repeatability of landmarking and consistency between the two main landmarkers.

- Key data inputs
  - TPS files from repeatability dataset: left and right wings of 20 specimens landmarked three times by two landmarkers.

- Core processing steps
  - Convert coordinates for Procrustes alignment.
  - Compute Procrustes distance (wing shape FA) and centroid size asymmetry.
  - Visualize FA by landmarker and by date landmarked.
  - Use a linear mixed-effects model to test for significant differences between landmarkers or between recording dates.

- Outputs
  - No explicit outputs files are described; results are produced via plots and statistical models.

- Data governance considerations
  - Establishes inter-annotator reliability and procedural consistency, informing data quality and instrumentation choices.

---

## 04_Rarefying_FA_data_even_temporal_coverage

- Purpose and scope
  - Achieves more even temporal coverage of FA data across a century.

- Key data inputs
  - 20210409_updated_dataset.csv (dataset containing FA measurements and metadata).

- Core processing steps
  - Randomly retain at least one specimen for every combination of bee species, caste, climate region, year, and month.
  - If a given year still has more than 20 samples, randomly down-sample to fewer than 20.
  - Export the subsampled dataset.

- Outputs
  - Subsampled_FA_Data_0_1_v3.csv ensuring balanced temporal representation.

- Data governance considerations
  - Improves comparability over time and reduces sampling bias; provides a reproducible subsampling approach.

---

## 05_Statistical_analysis_plot_report

- Purpose and scope
  - Performs statistical analysis and visualization of FA using generalized additive models (GAMs).

- Key data inputs
  - Subsampled_FA_Data_0_1_v3.csv (from script 04).

- Core processing steps
  - Compare FA across four bumblebee species.
  - Assess FA differences between the first and second halves of the 20th century, with species-specific effects.
  - Model FA as a continuous time trend over the 20th century.
  - Evaluate FA associations with mean annual temperature and annual precipitation.
  - Model selection via a maximal model including all variables, followed by stepwise reduction.
  - Generate plots of model estimates using predict.gam().

- Outputs
  - Plots of model estimates with raw data.
  - Includes supplementary GAM analyses related to manuscript Arce & Cantwell-Jones et al. (Journal of Animal Ecology).

- Data governance considerations
  - Provides a transparent, model-based synthesis of FA patterns over time and climate drivers; supports reproducibility via GAM-based analysis and explicit model selection workflow.

---

## Overall notes for Data Leaders

- End-to-end data pipeline
  - The collection comprises a cohesive pipeline from data preparation and quality control (QC) to statistical analysis and visualization, designed to produce robust FA metrics and enabling time-series and climate-linked analyses.

- Quality, provenance, and metadata
  - QC is explicit and adjustable (multiple cut-offs in two main QC steps); provenance is maintained via orientation corrections, Procrustes alignment, and detailed input/output specifications for each script.

- Reproducibility and collaboration
  - The workflow relies on TPS landmark data and standardized processes; repeatability analysis and transparency about landmarkers support cross-team reliability and collaboration.

- Data discoverability and gaps
  - Requires explicit input files (TPS, orientation data) and yields clear outputs (CSV and plots), aiding discoverability and reuse; highlights potential data challenges (orientation issues, measurement error, data sparsity in certain periods or species) that could inform future data collection and partnerships.