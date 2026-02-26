# Description of the statistical methodology used for the analysis of Countryside Survey data

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, recap previous approaches, and detail the changes implemented for CS2007 to achieve consistent estimation and improved precision.

## Executive summary (key takeaways)

- Previous CS estimation mixed stock (all squares) with change (repeat squares only), causing inconsistencies between stock and change estimates.
- Modelling to achieve consistent estimation is feasible and robust; differences from old methods are generally small relative to existing uncertainties.
- The 2007 CS adopted a modelling approach (mixed effects/repeated measures with AR1 structure) to use all available data and produce more precise estimates for both stock and change.
- The modelling approach requires distributional assumptions and more computing time; results are validated against the old methodology.
- Consistent estimation improves precision across square and plot level data and enables unified treatment across habitats (Broad Habitats) and soil/plot data, but updates past estimates as new information becomes available.
- Limitations include sensitivity to distributional form, potential issues with highly non-normal data, and practical constraints on model complexity for large variable sets.

## 1. Introduction and data structure

- Countryside Survey data are collected from a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels: square level (entire square) and within-square plots (plot level) to capture vegetation, soils, etc.
- Land Classification (ITE) defines strata for square selection; classifications are country-specific (England, Wales, Scotland) and have evolved to accommodate reporting needs.
- Variables range from binary to continuous; data are hierarchical and incomplete due to missing squares across survey years.

## 2. Previous methodology (overview)

- Stock estimates: means and standard errors computed for each Land Class, then combined (weighted by land-area) to give region/national stocks.
- Change estimates: calculated from repeated measurements only, not from all data, leading to inconsistencies with stock.
- Bootstrap used for square-level data to account for non-normal distributions.

## 3. Why modifications to CS methodology

- Inconsistencies arose because stock used all data from a survey while change used only repeated data, so differences between stock and change were not guaranteed to align.
- Three potential consistency approaches were considered; modelling (consistent estimation) was found feasible and advantageous, addressing both stock and change simultaneously and robustly.
- New approach increases precision by leveraging all available information and accounting for data hierarchy but introduces more assumptions about data distributions.

## 4. Modelling approach for consistent estimation

### 4.1 General modelling framework

- Uses mixed effects and/or repeated measures models to handle incomplete data and hierarchical sampling.
- Fixed effects: land-class means across surveys (stock estimates).
- Random effects: square-level deviations and survey-to-survey (repeated measures) residuals.
- After fitting, fixed effects are transformed to stock and change estimates; this yields estimates that are consistent across surveys.

### 4.2 Square level data

- Model: y_ijk = a_i_k + s_i_j + e_i_jk
  - a_i_k: fixed effects representing land-class means at survey k.
  - s_i_j: square-level random effect (variation of squares within land class).
  - e_i_jk: repeated-measures residuals (within-square variation across surveys).
- Distributions:
  - s_i_j ~ N(0, τ_i^2) varying by land class.
  - e_i_jk ~ N(0, σ_ik^2) with covariances among squares across surveys.
- Complexity: full model with all variance/covariance terms is large; robust fixed-effect estimates can be obtained even with simpler specifications.

### 4.3 Plot level data

- Plot-level data within squares add further hierarchy; methods previously used either condensed to square level or treated plots as independent.
- Extended models add a plot-level random effect alongside the square-level effect; allows correlation of plots within a square and can be embedded in bootstrapping.

### 4.4 Model specification and reduction of parameters

- The full model has many random effect parameters, which can be unstable with sparse data per land class.
- Reductions include:
  - Assuming equal random effect variances across surveys (σ_i common across surveys).
  - Using AR1 (autoregressive order 1) structure for repeated measures: covariances between successive surveys are constant; non-adjacent surveys are conditionally independent given intervening surveys.
- AR1 markedly reduces parameter count to three random-effect parameters per survey, independent of the number of surveys.
- Fixed effects are robust to mis-specification of random effects; bootstrap standard errors provide robust uncertainty estimates.

### 4.5 Model testing and Broad Habitats

- Broad Habitat analyses (from 1984, 1990, 1998, and later) compared old methods (stock vs. change from different data subsets) with modelling results.
- Modelling produced estimates that avoided previous discrepancies; differences between old and new methods generally fell within old method inconsistencies.
- The modelling approach was validated for square-level data and extended to plot-level data (soil data and 1978–1998 datasets), supporting adoption for CS2007.

### 4.6 Practical implementation and checks

- Analyses involve data from all surveys; past estimates can be updated as new data become available, reflecting improved information rather than errors.
- Computation is intensive; AR1 with bootstrap is a practical balance between robustness and efficiency for large numbers of analyses.
- The analysis framework includes checks comparing new (model-based) and old methods to ensure changes are not substantial beyond existing variability.

## 5. Limitations and implications

- Distributional assumptions for random effects affect variance/covariance estimates; fixed-effect estimates are generally robust.
- For very non-normal data, transformations are tricky because results must be presented on the original measurement scale.
- Some non-normal variables (e.g., standing water) may cause convergence to local maxima with new methods; in such cases, old methodologies may be reported.
- Computational demands are higher; for large variable sets, a standard AR1 model with bootstrap is favored for practicality.
- Results for past surveys are updated with new data, which can alter estimates slightly; this is conceptually distinct from the prior inconsistencies and reflects cumulative information use.

## 6. Implications for practice

- Analysts can rely on consistent estimation to produce stock and change estimates that are directly comparable across surveys.
- The modelling approach provides improved precision by incorporating the data hierarchy and all available information.
- When communicating results, it is important to note that earlier survey estimates may be revised as new data are incorporated.
- Data reporting and metadata practices should reflect the use of all-survey information and the potential for updated past estimates.

## References (selected)

- Barr et al. (1993); CS1990 main report.
- Dempster, Laird, Rubin (1977); EM algorithm for incomplete data.
- Efron & Tibshirani (1993); Bootstrap methods.
- Haines-Young et al. (2000); Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002); Maximum likelihood estimation using the empirical Fisher information matrix.