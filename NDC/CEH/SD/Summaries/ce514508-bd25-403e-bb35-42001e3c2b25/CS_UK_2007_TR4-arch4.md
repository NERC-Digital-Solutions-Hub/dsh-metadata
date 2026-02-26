# Countryside Survey 2007: Consistent Estimation

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis and the changes implemented for CS2007 to achieve consistent estimation of stock and change.
- Previous CS methods used stock estimates from all data and change estimates from repeated measurements, leading to inconsistencies between stock and change.
- Modelling approaches demonstrated that consistent estimation is feasible and robust for CS Broad Habitat data; differences from old methods were generally small and within prior inconsistencies.
- The adopted modelling approach uses information from all surveys, improving precision and allowing missing data to be handled coherently; earlier data can be updated as new surveys are added.
- Implementing modelling is technically challenging and more computationally intensive, requiring iterative fitting rather than formulaic calculations; a streamlined AR1 mixed-effects model was chosen for practicality and robustness.
- Bootstrap methods are used to obtain standard errors and significance, accommodating non-normal data distributions.
- For Broad Habitats (and soil/plot level data), modelling produced results consistent with, and often more efficient than, previous methods; differences from old methods were small and generally within existing error bounds.
- Adoption of the new methodology has implications for reporting timelines and the updating of past estimates as new information becomes available.

## 1. Introduction
- CS data come from a stratified, two-level sampling framework: 1 km squares (grid-based) with measurements at the square level and within-square plots; data types range from binary to continuous.
- Land Classification (ITE) has evolved, with country-specific classifications ( England, Wales, Scotland) tailored for reporting needs; 45 land classes in CS2007.
- The report outlines the sampling and analysis procedures, reviews the previous CS methodology, and explains changes for CS2007, including limitations and implications.

## 2. Overview of Previous CS Methodology
- Estimation previously involved: means and standard errors for each Land Class, then weighted combination to regional/national estimates; relatively robust with minimal distributional assumptions.
- Stock estimates used all data from a survey; change estimates used repeated measurements across survey pairs; this caused mismatches and perceived inconsistencies between stock and change.
- Bootstrapping was introduced pre-2000 to better assess significance for square-level data due to non-normal distributions.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change estimates were common, not due to data errors but due to differing data subsets used for stock vs. change.
- Three potential approaches to achieve consistency were considered: (a) use stock from all data and change from differences of stock estimates; (b) use only repeated squares for both stock and change; (c) employ modelling to jointly estimate stock and change across all surveys.
- Modelling (approach c) was found to be feasible and more efficient, producing consistent and more precise estimates for both stock and change, applicable to square and plot-level data.

## 4. Modelling Approach

### 4.1 Modelling Basics
- Incomplete data techniques (mixed effects/repeated measures models) allow consistent estimation by leveraging data across all surveys.
- Fixed effects capture stock/change values; random effects reflect sampling variation (land class, squares, plots); modelling requires distributional assumptions but fixed effects are robust to certain mis-specifications.
- The approach uses information from all surveys, producing more precise estimates but requiring more computation.

### 4.2 Square Level Data
- Square-level data are treated as repeated-measures within land classes; the basic model is a mixed effects model with:
  - Fixed effects: land-class means across surveys (aik).
  - Random effects: square-level deviations (sij) and survey-specific residuals (eijk) with covariances.
- Within-class variance and cross-survey correlations are allowed to differ by land class.

### 4.3 Plot Level Data
- Plot-level data within squares can be analysed by extending the square-level model to include a plot-level residual, capturing within-square plot variation.
- Models may embed plot-level random effects in addition to square-level effects; both square and plot-level models can be bootstrapped to obtain standard errors.

### 4.4 Model Specification
- General model for square-level data:
  yijk = aik + sij + eijk
  - aik: fixed effects (land-class means over surveys)
  - sij: square random effects
  - eijk: repeated-measures residuals
- Random effects distributions: sij ~ N(0, τi^2) varying by land class; eijk ~ N(0, σik^2) with covariances across surveys.
- With K surveys, there are K fixed effects per land class but many random-effect parameters; to keep the model tractable, simplifications are used.
- Reducing parameter count:
  - Assume random effect variances do not vary with surveys (σi common across surveys).
  - Use an autoregressive AR1 structure for covariances between repeated measures, reducing per-land-class random parameters to three per survey.
- Bootstrap is recommended for standard errors due to potential mis-specification of variance/covariance distributions.
- Models are preferred on the original scale (no transformation), though this can complicate back-transformation if needed.

### 4.5 Model Testing – Broad Habitats
- Historical Broad Habitat data (1984, 1990, 1998) were reanalyzed with modelling to verify consistency.
- Stock and change estimates from the AR1 model matched the concept of consistency (change equals the sum of inter-survey stock differences).
- Comparisons show the modelling approach yields results not outside the old-method error bounds, with most differences well within those bounds.
- Analyses extended to soil and plot-level data confirmed feasibility and consistency, supporting adoption of the new methodology for CS2007.

## 5. Limitations and Implications
- AR1 modelling with bootstrapped standard errors provides robust fixed-effect estimates but requires substantial computation; full parameterization can be slow for large variable sets.
- The chosen AR1 approach balances stability, speed, and robustness; it is suitable for automated application across many variables.
- Distributional assumptions affect variance/covariance estimates; bootstrap helps mitigate this for standard errors.
- Extremely non-normal data can cause convergence issues (e.g., standing water variable); in such cases, older methods may be preferred for that variable.
- Adopting a model-based approach means past survey estimates may be updated as new data are incorporated; this reflects a coherent, data-integrated system rather than inconsistent standalone reports.

## 6. References
- Barr et al. (1993), Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron & Tibshirani (1993); Scott (2002).