Countryside Survey in 2007: Consistent Estimation

## Executive Summary
- The report describes a statistical methodology shift for Countryside Survey (CS) data analysis, adopting modelling to achieve consistent stock and change estimates across surveys.
- Previous methods were robust but produced inconsistencies because stock used all data while change used only repeated measurements.
- Modelling methods for consistent estimation were feasible and generally robust, with differences from old methods within existing inconsistencies.
- The 2007 CS adopted the modelling approach, which uses all available information and improves precision, though it requires more computing time and careful validation.
- Outputs include more precise stock/change estimates and the potential for past survey estimates to be updated when new data are included.
- Validation included comparisons with Broad Habitat data and other data levels (square and plot), showing feasibility and improved consistency.
- The approach is technically challenging but is implemented with AR1 mixed models and bootstrap for robust standard errors.

## 1. Introduction
- This technical report outlines sampling and analysis procedures for CS data, reviewing the old methodology and detailing changes for CS2007.
- Emphasizes moving from describing current surveys and changes to long-term timelines, using consistent estimation.

## 2. Previous CS Methodology (Overview)
- CS field data come from a stratified sample of 1 km squares across GB, with two sampling levels: square-wide and within-square plots.
- Land Classification stratifies sampling; 45 classes in CS2007 (England, Wales, Scotland) reflecting country reporting needs.
- Estimation previously computed means/SEs for each Land Class and combined them, assuming independence across classes.

## 3. Reasons for Modifications
- Inconsistencies arose because stock estimates used all data while change estimates used repeated measures only.
- Comparing stocks across surveys could differ from changes between surveys, creating apparent but not real inconsistencies.
- A modelling approach using data from all surveys provides consistent, robust estimates for both stock and change and allows improved precision.
- Modelling is more complex and requires assumptions about data distributions; results are validated against the old method.

## 4. Consistent Estimation via Modelling
- Incomplete data handling through modelling leverages information from all surveys to estimate stock and change consistently.
- Mixed effects/repeated measures models are used, with fixed effects for stock/change and random effects for hierarchical sampling structure.
- Models are fitted to data from all surveys, transforming fixed-effect estimates into stock/change estimates.

### 4.1 Square Level Data
- Treats CS data as a random sample of squares within each Land Class; uses repeated measures mixed models.
- Fixed effects: land-class means across surveys.
- Random effects: square-level deviations and within-square survey deviations, with correlations across surveys.

### 4.2 Plot Level Data
- Plot data within squares can be handled by extending the square-level model with an additional plot-level random effect.
- Allows for proper accounting of plot-to-plot variation within squares; both square and plot levels can be bootstrapped.

### 4.3 Model Specification
- General model: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means across surveys), s_ij are square random effects, e_ijk are repeated measures residuals.
- Random effects: assumed normal, with land-class-specific variances; repeated-measures covariances vary by land class and survey.
- To keep models tractable with many surveys, random-effects parameters are reduced (e.g., AR1 structure, common variance components across surveys).
- AR1 + bootstrap is used to achieve robust standard errors and feasible computation.

### 4.4 Model Testing – Broad Habitats
- Previous outputs for Broad Habitats showed inconsistencies between stock and change when using old methods.
- Modelling (AR1 with bootstrap) yields estimates that align with differences across surveys, removing prior discrepancies.
- Reanalyses across 1984, 1990, 1998 data demonstrated improved consistency; differences between old and new methods generally fell within old uncertainty bounds.
- The approach was also validated for soil and plot-level data, supporting adoption for 2007 CS.

## 5. Limitations and Implications
- Bootstrapping with complex models is computationally intensive; AR1 model reduces random-parameter burden but remains slower than old methods.
- Fixed-effect estimates (stock/change) are robust to some distributional mis-specifications; variance/covariance parameters are more sensitive.
- Very non-normal data can cause convergence issues; in some freshwater data, old methods were retained when new methods diverged.
- Results are on the original measurement scale; transforming data for analysis complicates interpretation and back-transformation.
- Because analyses use data from all surveys, estimates for any one survey may be revised as new data become available; routine updating is expected rather than treated as errors.
- Overall, modelling should yield more precise estimates and a consistent approach across square and plot data, if distributional assumptions are reasonable.

## 6. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).