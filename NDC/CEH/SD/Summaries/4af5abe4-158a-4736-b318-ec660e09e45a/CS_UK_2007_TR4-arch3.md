# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data and documents changes from previous CS methodologies introduced for CS2007.
- Old methods were robust but produced inconsistent stock and change estimates because stock used all survey data while change relied only on repeat measurements; this caused mismatches in reported trends.
- Modelling for consistent estimation was investigated and found feasible and robust, with differences from old methods generally within existing inconsistencies.
- The new modelling approach, adopted for CS2007, uses all available information to produce more precise estimates but requires additional data distribution assumptions and greater computational effort.
- The AR1 mixed-effects modelling framework with bootstrap-based standard errors was selected for square and plot level data to balance efficiency, robustness, and practicality for large-scale analyses.
- Implementing the modelling approach revealed practical challenges, but it yielded a substantially improved product and allowed consistent estimation across the full time series.
- The approach implies that estimates for any single survey can be updated as new data arrive, leading to small revisions to historical findings.

## 1. Introduction
- This technical report outlines CS sampling and analysis procedures, reviews the previous methodology, and explains the changes implemented for CS2007, including limitations and implications.

## 2. Sampling
- CS data come from a stratified sample of 1 km squares within a 15 km GB grid.
- Each square is mapped and measured at two levels: square-wide measurements and within-square plot measurements (e.g., quadrats for vegetation, soils).
- Land Classification (ITE) is used for stratification; country-specific adaptations have led to 45 classes in CS2007 (England, Wales, Scotland with related but distinct national classifications).

## 3. Estimation
- The traditional approach computed means and standard errors within Land Classes and combined them (weighted by land area) to obtain regional means or totals.
- This method makes minimal distributional assumptions and treats land classes as independent in the combination step.

## 4. Bootstrapping
- Significance testing moved from assuming normality to bootstrap methods due to skewness in some features.
- Bootstrap (typical 1000–10,000 resamples) provides distribution-based estimates for standard errors and confidence intervals, accommodating non-normal data.

## 5. Reasons for Modifications to CS Methodology
- Past reporting showed inconsistencies: stock estimates used all data, while change estimates used repeated measurements only, causing apparent discrepancies.
- Various approaches to achieve consistency were evaluated; modelling stock and change consistently was found feasible and advantageous, especially for harmonizing square and plot-level analyses.
- The modelling approach leverages incomplete data techniques (mixed effects/repeated measures) to derive consistent and more efficient estimates.

## 6. Modelling basics
- Consistent estimation requires fitting models that handle incomplete data across multiple surveys.
- Mixed effects and repeated measures models separate fixed effects (stock/change means over surveys) and random effects (variance components reflecting sampling structure).
- Implementing full models with many random effects is often unstable and computationally heavy; simplifying assumptions are used to reduce parameter counts while preserving robust fixed-effect estimates.

## 4.3 Square level data
- Square-level data are treated as repeated measures within Land Classes.
- A mixed model with fixed effects for Land Class means across surveys and random effects for squares (and their survey-to-survey correlations) is used.
- Within-class variance and covariances are allowed to differ across land classes.

## 4.4 Plot level data
- Plot-level data within squares can be analyzed by extending the square-level model to include a plot-level residual (random effect) in addition to the square-level random effect.
- This accommodates within-square plot variation and can be integrated into bootstrapping procedures.

## 4.5 Model specification
- General model for square-level data: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik are fixed effects (land-class means per survey),
  - s_ij are square random effects,
  - e_ijk are repeated measures residuals.
- Random effects (s and e) follow distributional assumptions that vary by land class and survey, with covariances modeled (often AR1).
- To keep models tractable, random-effect parameters (variances/covariances) are constrained (e.g., common AR1 structure across surveys, common variance per land class) to reduce parameter count.
- AR1 plus bootstrap is used to obtain robust standard errors, balancing model complexity and practical run-time.

## 4.6 Model testing – Broad Habitats
- The 1984, 1990, and 1998 CS Broad Habitats data were re-evaluated with the new modelling approach.
- Old method discrepancies between stock and change were not present in the new models; changes derived from stock estimates matched the sum of period-wise changes, addressing prior inconsistencies.
- Comparisons showed the new modelling approach yielded estimates within the old method’s error bounds; most changes were small relative to prior discrepancies.
- The modelling approach extended beyond square data to include plot data and supported adopting the new methodology for CS2007.

## Limitations and Implications
- The AR1 model with bootstrap is robust for fixed effects but introduces substantial computation time; full parameterized models are often impractical for large variable sets.
- Estimation of variance/covariance parameters is less robust than fixed effects; bootstrap mitigates this but decisions about model structure remain important.
- Very non-normal data can cause convergence or bias in certain variables (e.g., standing water); in such cases, older methods or cautious interpretation may be necessary.
- Results are updated as new surveys are added; historic estimates may be revised, reflecting newly available information rather than prior inconsistencies.
- The modelling approach leverages all available information and preserves data hierarchy, improving precision; however, it requires explicit distributional assumptions and careful model checking.

## Implications for Monitoring Framework Authors
- Emphasize consistent estimation across time to enable reliable trend analysis of environmental health indicators.
- Favor modelling approaches (e.g., mixed effects AR1 structures) to integrate data from multiple surveys and hierarchical plot-square structures.
- Use bootstrap methods to obtain robust confidence intervals when data are non-normal or complex.
- Plan for computational resources and automated workflows to apply standard models across many variables.
- Be transparent about assumptions, update historic results with new data, and communicate any revisions to stakeholders.
- Invest in data quality and metadata to support data sharing, reproducibility, and governance across monitoring programs.