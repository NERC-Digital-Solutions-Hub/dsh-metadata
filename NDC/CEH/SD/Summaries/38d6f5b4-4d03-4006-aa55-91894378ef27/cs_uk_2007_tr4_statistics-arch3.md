Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data, summarising previous methods and detailing changes made for CS2007 to achieve consistent stock and change estimates.
- Previous approaches used minimal assumptions and maximised data use for stock estimates but estimated change from a more limited, repeated-measures subset, causing inconsistencies between stock and change estimates.
- Investigations with Broad Habitat data showed that consistent estimation via modelling was feasible and robust, with differences from old methods generally small.
- CS2007 adopts modelling for consistent estimation of both stock and change, leveraging all available data, which yields more precise estimates.
- The modelling approach introduces additional data-distribution assumptions and requires validation, especially for small data subsets, by comparison with the old method.
- Unlike the previous methods, the modelling approach uses all information and better reflects data hierarchy, improving precision but increasing computational demand.
- Implementation of modelling is technically challenging and slower, but the resulting product is significantly improved; outputs can update previous surveys as new data are incorporated.

## 1. Introduction
- This technical report provides an overview of sampling and analysis procedures for CS data, reviews the previous CS methodology, and explains the changes implemented for CS2007, including limitations and implications.
- Detailed earlier CS sampling and estimation procedures are documented in Barr et al. (1993).

## 2. Overview of Previous CS Methodology
- 2.1 Sampling
  - CS field data come from a stratified sample of 1 km squares within a 15 km GB grid.
  - Two sampling levels: square-level measurements (covering whole squares) and within-square plot measurements.
  - Land Classification (ITE) used as strata; classifications evolved over time (GB → separate country classifications: England, Wales, Scotland).
- 2.2 Estimation
  - Regional/national estimates were formed by computing means and standard errors by Land Class and then weighting by land area to obtain totals or means.
  - Stock estimates used all data from a survey; change estimates used repeated measurements only, leading to potential inconsistencies between stock and change.
- 2.3 Bootstrapping
  - Significance testing moved from assuming normality to bootstrap-based standard errors and confidence intervals due to potential non-normality in data.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change estimates arose because stock used all survey data while change used repeated measurements only.
- The proposed shift in CS2007 emphasised generating consistent estimates across all time points, addressing the interpretive issue that adjacent-survey changes may not sum to non-adjacent changes under previous methods.
- Three potential approaches to consistency were considered; modelling (consistent stock and change via full data) was selected for its robustness and efficiency, despite needing stronger distributional assumptions.
- Modelling across all surveys (square and plot level data) was chosen to provide consistent, improved precision, with bootstrap used to obtain robust standard errors.

## 4. Modelling Approach
- 4.1 Square level data
  - Treat CS as a repeated-measures, hierarchical dataset: a mixed-effects model with fixed effects for land-class means across surveys and random effects for squares within land classes.
  - Stock estimates come from fixed effects; change estimates are differences between fitted stock estimates and are inherently consistent.
- 4.2 Plot level data
  - Plot data within squares can be modeled explicitly to reflect within-square variation.
  - Models can include a plot-level residual in addition to the square-level random effect; both forms can be embedded within bootstrapping.
- 4.3 Square level data – modelling basics
  - General model: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means across surveys), s_ij are square random effects, e_ijk are repeated-measures errors.
  - Random effects assumed normally distributed with land-class-specific variances; covariances between surveys modeled and estimated.
  - Variance/covariance parameters can explode in number; practical reduction via assumptions is necessary.
- 4.4 Model specification and reduction
  - To manage complexity, several parameter-reduction strategies are used:
    - Assume random effect variances do not vary with survey (common σ_i for all surveys).
    - Use autoregressive AR1 structure for repeated-measures covariances to limit parameters to one per land class.
  - Fixed-effects estimation is robust to some mis-specification; variance/covariance parameters require careful handling.
  - Bootstrap is used for standard errors to maintain robustness when using reduced-parameter models.
- 4.5 Model testing – Broad Habitats
  - Consistency checks using Broad Habitat data across 1984, 1990, and 1998 showed modelling eliminated discrepancies between stock and change estimates that existed with older methods.
  - Comparisons indicated new modelling results generally aligned with old results within prior error bounds.
  - Analyses of soil and plot data confirmed feasibility of consistent estimation across data types; CS2007 adopted the modelling approach for broader data consistency.
- 4.6 Model testing and practical implementation
  - AR1 with bootstrap SEs was investigated as a practical, robust solution for CS data.
  - Fully parameterised models were too slow for the full dataset; AR1 offered a balance of speed and reliability.
  - The CS software was designed to run both old and new methods for cross-checks; differences were generally small and within previous error bounds.

## 5. Limitations and Implications
- Implementation of model-based analysis with bootstrapping is computationally demanding but feasible.
- Fixed-effects estimates (stock/change) are robust to some distributional mis-specifications; variance/covariance estimates are more sensitive.
- For very non-normal data (e.g., standing water), convergence issues occurred; in such cases, older methodology results were retained.
- The modelling approach produces more precise estimates by utilizing all information and reflecting the data hierarchy; however, estimates for a given survey can be revised as new surveys add information.
- The shift implies that cross-time comparability changes: estimates are updated with new data, which can yield small revisions to previous findings, but is conceptually consistent with using all available information.

## 6. References
- Barr et al. (1993); CS1990 Main Report
- Dempster, Laird, Rubin (1977); EM algorithm
- Efron, Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for nature: assessing habitats in the UK countryside
- Scott (2002); Maximum likelihood estimation using the empirical Fisher information matrix