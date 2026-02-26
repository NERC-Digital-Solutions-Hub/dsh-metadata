# Statistical Methodology Used for the Countryside Survey Data

- This report describes the statistical methodology used to analyse Countryside Survey (CS) data, summarises previous methods, and details the changes implemented for CS in 2007.

Executive Summary
- Previous methods were robust but produced inconsistencies: stock used all survey data while change used only repeated measurements across survey pairs.
- Investigations with CS Broad Habitat data showed that consistent estimation via modelling was feasible and robust; results generally aligned with old methods.
- A modelling approach for consistent estimation has been adopted for CS 2007 data.
- The modelling approach makes additional distributional assumptions, so results are validated by comparing with the previous methodology, especially for small subsets.
- Modelling utilises all available information, yielding more precise estimates; new surveys can improve past estimates, though changes are typically small.
- Implementation of modelling is computationally intensive, requiring iterative model fitting and careful handling of CS sampling complexity; ultimately results in an improved product.

Introduction and Context
- The technical report provides an overview of CS sampling and analysis, reviews the previous methodology, and explains changes made for CS 2007, plus limitations and implications.
- The Countryside Survey uses stratified sampling of 1 km squares on a GB-wide 15 km grid; data are collected at two levels (square-wide and within-square plots) with varied data types.
- Land Classification (ITE) is used for stratification; classifications have expanded over time to support country-specific reporting (England, Wales, Scotland).

Estimation and Inference
- The traditional approach: compute means and standard errors by Land Class, then combine (weighted by land area) to obtain regional or national estimates; assumes independence across Land Classes.
- Significance testing shifted from normality assumptions to bootstrap methods due to potential skewness, especially for square-level data.

Rationale for Methodological Change
- Inconsistencies arose because stock estimates used all data, while change estimates used only repeated measurements; this could yield non-aligned stock-change estimates.
- Several potential approaches to achieve consistency were discussed; modelling (consistent estimation) was found to be feasible and beneficial, offering robust, efficient estimates for both stock and change and applicable to square and plot level data.

Modelling Basics
- Incomplete data techniques (e.g., EM-like approaches) enable consistent estimation by modelling data structure rather than imputing missing values; this requires distributional assumptions.
- Mixed effects/repeated measures models are used to capture fixed effects (stock/change across surveys) and random effects reflecting sampling structure.
- After fitting, fixed effects translate into stock and change estimates; random effects govern variability and correlations.

Square Level Data
- For complete 1 km squares, data are treated as a random sample within Land Classes; a repeated-measures (mixed) model is used.
- Fixed effects: land-class means across surveys (regression of the variable on year/survey as a categorical factor).
- Random effects: square-level deviations and within-square, across-survey correlations; these account for repeated measurements in the same square over time.

Plot Level Data
- Plot data within squares are more complex; earlier analyses either aggregated to square level or treated plots as independent, risking biased SEs.
- Modern approach uses a mixed model that includes both square-level and plot-level residuals (random effects), with bootstrapping used to obtain robust SEs.
- Models can be extended to include plot-level residuals, yielding correlations that pertain to plots rather than squares; both forms can be bootstrapped.

Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for each survey)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures random effects
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) with covariances for squares across surveys
- Complexity challenges:
  - Each land class and multiple surveys generate many random parameters; full models can be unstable with limited per-class data.
  - Reductions focus on common structures (e.g., AR1) to limit random-parameter count and keep models tractable.

AR1 Modelling and Bootstrap
- The AR1 approach assumes constant within-land-class variance across surveys and first-order autocorrelation between successive surveys.
- Reduces random effects to a manageable number (three per survey) regardless of the number of surveys.
- While fixed effects are robust to some misspecifications, variance/covariance estimates are sensitive; bootstrap standard errors are recommended for robustness.

Model Testing and Broad Habitats
- CS2000 Broad Habitat analyses demonstrated that models could produce consistent stock/change estimates where old methods produced discrepancies.
- Mixed-effect AR1 models fitted to 1984, 1990, and 1998 data eliminated inconsistencies between stock and change estimates observed with older methods.
- Differences between old and new methods were generally small, often within the old method’s own confidence intervals; most changes were minor.

Limitations and Practical Implications
- AR1 modelling with bootstrapped SEs enhances robustness but is computationally slower than the old method.
- For large numbers of variables, a standard automated model is preferred; AR1 with bootstrap proved practical for CS2007.
- Model choice remains important; fixed effects estimates are robust, but SEs depend on distributional assumptions for random effects; bootstrap mitigates some risks.
- Some variables with highly non-normal distributions (e.g., standing water) can cause convergence to local maxima; in such cases, older methods or alternative handling may be used.
- Adopting a model-based, data-integrative approach means past survey estimates can be updated as new data arrive, leading to small revisions to earlier findings.

References
- Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002)
- Acknowledges funding and the CS project office; CS2007 undertaken with Defra and NERC support; data reproducibility and accessibility emphasized.

Notes for Analysts
- The shift to modelling emphasizes consistent estimation across time and surveys, leveraging all available data and respecting the hierarchical sampling structure.
- Bootstrapping provides distribution-free inference for standard errors, accommodating non-normal data.
- Expect updated estimates for past surveys as new data are incorporated; this is an intended feature of the modelling approach, not a defect in prior reporting.