# Countryside Survey 2007: Statistical Methodology

- This technical report describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS 2007 to achieve consistent stock and change estimates.
- It contrasts the previous, robust but potentially inconsistent methods with a modelling approach that uses all available data and yields more precise estimates.
- The shift to a modelling framework relies on incomplete-data techniques, mixed-effects/repeated-measures models, and bootstrap-based standard errors to accommodate non-normal data and complex data structure.
- The modelling approach is designed to produce estimates that are coherent over time (stock and change) and to utilize information from all surveys, potentially updating past results as new data arrive.

## 1. Introduction
- CS field data come from a stratified sample of 1 km squares across a 15 km grid over Great Britain.
- Two levels of sampling exist: square-level means (covering the whole square) and within-square plot-level measurements (e.g., vegetation, soils).
- Land Classification (ITE) stratifies the sampling; classifications have evolved for separate country reporting (England, Wales, Scotland).

## 2. Overview of previous CS methodology
- Initially, regional/national estimates were formed by combining land-class means and standard errors, weighted by land-area.
- Stock estimates used data from the entire survey; change estimates relied on repeat measurements (paired surveys), causing inconsistencies between stock and change.
- Significance testing relied on normality assumptions; bootstrap was not always used.
- Reporting emphasized changes since the last survey rather than long-term timelines, contributing to interpretational challenges when comparing across non-adjacent surveys.

## 3. Reasons for modifications to CS methodology
- Inconsistencies arose because stock used all survey data while change used only repeated measurements.
- The goal was to obtain consistent estimates of stock and change across surveys and to improve precision by leveraging all available information.
- Modelling (consistent estimation) was investigated as feasible and robust, particularly for Broad Habitat data; results differed little from old methods within existing inconsistency bounds.
- New methods were adopted for CS 2007 to provide more coherent historical timelines and improved efficiency.

## 4. Consistent estimation
- A modelling approach replaces inconsistent pairwise estimates with a framework that jointly estimates stock and change across all surveys.
- Incomplete-data techniques (mixed effects and repeated-measures models) allow information from all surveys to inform estimates, while accounting for missing data.
- The modelling framework requires distributional assumptions and careful checks, especially for small sub-samples.

### 4.1 Square level data
- For complete 1 km squares, data are treated as repeated-measures within Land Classes.
- A mixed-effects model: fixed effects for Land Class means by survey; random effects for squares and survey-specific residuals, including covariances across surveys.
- The basic square-level model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land-class means by survey), s_ij as square random effects, e_ijk as repeated-measures residuals.
- Random effects are assumed normally distributed; variances/covariances vary by land class and survey.

### 4.2 Plot level data
- Plot-level data within squares can be incorporated with extensions to the square-level model by adding a plot-level random effect.
- This yields a hierarchy that more accurately represents the data structure and improves standard error estimation.
- Bootstrapping can be used to obtain robust standard errors for these models.

### 4.3 Model specification
- General form: y_ijk = a_ik + s_ij + e_ijk, with distributions s_ij ~ N(0, τ_i^2) and e_ijk ~ N(0, σ_ik^2), including covariances between surveys.
- For multiple surveys, many random-effect parameters exist; to keep models tractable, the AR1 (autoregressive) structure is used.
- AR1 assumes common within-land-class variance across surveys and a first-order autocorrelation for survey-to-survey covariances.
- This reduces random-effect parameters to a manageable number (three per land class), while preserving essential correlation structure.
- Bootstrap is recommended for standard errors due to potential mis-specification in variance/covariance parameters.

### 4.4 Model testing – Broad Habitats
- Past CS outputs included stock and change for Broad Habitats; inconsistencies were evident under the old methods.
- With modelling (AR1) methods applied to 1984, 1990, and 1998 data, stock and change estimates became consistent within the bootstrap framework.
- Differences between old and new methods were generally small relative to existing inconsistencies; in most cases, new estimates fell within old uncertainty bounds.
- Consistent estimates were also demonstrated for soil data and plot-level data, supporting adoption of the approach for 2007.

## 5. Limitations and implications
- Bootstrapping with complex mixed models is computationally intensive, but AR1 models provide a practical balance of speed and robustness.
- Fixed-effect estimates (stock/change) are robust to some mis-specification of random-effects distributions; variance/covariance parameters are more sensitive.
- Very non-normal data can lead to convergence issues or local maxima; an example with freshwater standing water showed reliance on the old method for that variable.
- The modelling approach uses information from all surveys, so past estimates can be updated when new data arrive; results for a given survey may shift slightly as data accumulate.
- An automated, standard modelling approach is favored for large-scale analyses to produce robust results efficiently.

## 6. Implications for data governance and reporting (Data Leaders perspective)
- Emphasizes the importance of data standardization, consistent longitudinal methods, and metadata that capture model assumptions and data hierarchies.
- Highlights the value of modelling approaches that utilize incomplete data and hierarchical structure to improve precision.
- Underlines the need for scalable, automated analysis pipelines to handle large numbers of variables and repeated surveys.
- Points to potential updates to past results as new data become available, requiring clear communication of methodological changes and their implications.

## 7. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron and Tibshirani (bootstrap); Scott (2002) on empirical Fisher information.