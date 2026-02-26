# Fluctuating Asymmetry Analysis Workflow for Bumblebee Wings

- A set of R scripts designed to process landmark data from left and right forewings of bumblebee museum specimens to compute fluctuating asymmetry (FA), assess measurement quality, and analyze temporal and climatic relationships.
- Focuses on standardizing data processing, ensuring data quality, enabling reproducibility, and producing outputs suitable for reporting and further monitoring.

## Data Inputs and Outputs

- Required inputs:
  - TPS landmark files for all specimens (left and right forewings with 13 landmarks each).
  - Orientation data CSV listing specimens with upside-down wings.
- Outputs:
  - FA metrics per specimen under multiple quality-control cut-offs (CSV).
  - Directional asymmetry and measurement error assessments (CSV).
  - Subsampled FA dataset for balanced temporal coverage (CSV: Subsampled_FA_Data_0_1_v3.csv).
  - Plots and model estimates for FA analyses (plot files and associated data).

## Processing Pipeline by Script

- 01_Filtering_specimens_generating_FA.R
  - Reads landmark data; flips left wings to align with right wings; corrects orientation for upside-down wings.
  - Performs quality control using:
    - Wing-angle variability (difference in y-axis positions between specific landmarks).
    - Procrustes distance from species mean shape after alignment.
  - Tests multiple quality-cut-off values to optimize data retention.
  - Removes low-quality specimens, Procrustes-aligns remaining wings, computes wing shape FA (Procrustes distance), exports FA CSVs per cut-off.

- 02_Testing_for_directional_asymmetry.R
  - Similar initial orientation corrections and QC (with fixed cut-offs 0 and 1).
  - After QC, performs Procrustes alignment and conducts a Procrustes ANOVA.
  - Exports results assessing directional asymmetry and measurement error by species and sex.

- 03_Repeatability_analysis.R
  - Assesses repeatability of landmarking with 20 specimens, each landmarked three times by two raters.
  - Converts data for Procrustes alignment; computes FA and centroid size asymmetry.
  - Visualizes FA by landmark and date; uses linear mixed-effects models to test for differences between landmarkers and recording dates.
  - No data outputs beyond analysis results.

- 04_Rarefying_FA_data_even_temporal_coverage
  - Balances temporal coverage by ensuring at least one specimen per species/caste/climate region/year/month.
  - Reduces years with >20 samples to maintain even sampling.
  - Exports Subsampled_FA_Data_0_1_v3.csv.

- 05_Statistical_analysis_plot_report
  - Analyzes FA using generalized additive models (GAMs).
  - Tests: (1) FA differences among four bee species; (2) FA differences between halves of the 20th century and by species; (3) FA over time as a continuous variable; (4) FA versus mean annual temperature and precipitation.
  - Model-building via maximal model and stepwise simplification; plots generated with predict.gam() alongside raw data.
  - Output includes plots of model estimates and underlying data.

## Quality Control, Transparency, and Governance

- Data quality
  - Multiple QC checks to identify and remove low-quality specimens before analysis.
  - QC methods on wing orientation, wing-angle variability, and shape deviation from species means.
- Metadata and provenance
  - Requires clear records of orientation status and cut-off choices; Procrustes alignment steps are tracked within scripts.
- Reproducibility and openness
  - Outputs are clearly derived from the input TPS and orientation data, with explicit dependency on cut-off parameters.
  - Subsampled dataset and FA results are produced for downstream reporting and potential sharing.
- Data management considerations
  - Outputs are CSVs and plots suitable for incorporation into dashboards or reports.
  - The workflow highlights the need for consistent data formatting, alignment procedures, and versioned analyses to support monitoring objectives.

## Relevance to Monitoring Frameworks

- Standardizes measurement pipelines
  - Converts raw landmark data into comparable FA metrics through consistent orientation, QC, and alignment procedures.
- Supports evidence-based decision-making
  - Provides temporal and climatic context for FA, enabling assessment of environmental health indicators over time.
- Addresses common monitoring challenges
  - Data quality and completeness: embedded QC to maximize reliable samples.
  - Metadata gaps: explicit orientation and QC parameters; requires provenance information for transparency.
  - Data sharing and governance: outputs are structured (CSV/plots) for easy sharing, with traceable processing steps.
- Enables reporting and dashboards
  - Produces interpretable metrics (FA, directional asymmetry, measurement error) and model-based estimates suitable for policy-oriented dashboards and methodological reporting.

## Key Takeaways for Monitoring Authors

- Build-in quality control at data intake to ensure reliable indicators.
- Document orientation corrections, QC cut-offs, and alignment steps to preserve data provenance.
- Use reproducible pipelines that produce both raw-derived metrics and accessible summaries/plots for stakeholders.
- Strive for balanced temporal coverage to detect trends while managing sample sizes through subsampling when necessary.
- Integrate advanced statistical analyses (e.g., GAMs, Procrustes ANOVA) to explore species differences, temporal trends, and climate associations in environmental health indicators.