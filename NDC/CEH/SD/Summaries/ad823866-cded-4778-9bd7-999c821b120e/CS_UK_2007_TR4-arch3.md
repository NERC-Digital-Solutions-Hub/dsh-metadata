Countryside Survey 2007: Statistical Methodology

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data, detailing changes for the 2007 analysis.
- Previous methods were robust but produced inconsistencies: stock was estimated from all survey data, while change relied on repeated measurements, leading to mismatches.
- Modelling-based, consistent estimation using all available data proved feasible and generally robust; differences from old methods were small.
- The AR1 (autoregressive) mixed-effects modelling approach was adopted to produce consistent and more precise stock and change estimates.
- To handle non-normal data and provide robust uncertainty, bootstrapping was used for standard errors and confidence intervals.
- The modelling framework applies to both square-level and plot-level data, though plot-level analyses required additional considerations.
- Implementation required more computing time and careful checks; estimates for past surveys can be updated as new data are added.
- The CS 2007 analysis adopts the new methodology for consistency and efficiency, with extensive validation against the previous approach.
- Limitations include sensitivity to distributional assumptions for random effects and potential issues with highly non-normal data (e.g., freshwater standing water); in some cases, old methods were retained if necessary.

## Introduction
- The document provides an overview of sampling and analysis procedures for Countryside Survey data, reviews the previous methodology, explains the motivation for changes in 2007, and discusses limitations and implications.

## Data and Sampling
- CS field data come from a stratified sample of 1 km squares within a 15 km GB grid, with two levels of sampling: square-level measurements and within-square plot-level measurements.
- Land Classification (ITE-based) stratifies squares; the classification has evolved across years and countries (England, Wales, Scotland) for reporting needs.
- Data types range from binary to continuous measurements (e.g., areas, lengths).

## Estimation and Methodology
- Old approach: compute means and standard errors by Land Class, then combine with area-weighting to obtain regional estimates; minimal distributional assumptions.
- Change estimates previously depended on repeated measurements, while stock used all data from a survey, leading to inconsistencies between stock and change.
- New approach: modelling techniques for consistent, efficient estimation of both stock and change, applicable to square and plot data; relies on incomplete-data methods and mixed-effects models.
- Bootstrapping is used to obtain standard errors and confidence intervals due to potential non-normality in the data.

## Modelling Basics
- Consistent estimation via modelling requires fitting models to data from all surveys, incorporating fixed effects (stock/change as functions of survey) and random effects (capturing sampling structure and within-square/plot variation).
- Two modelling schemes are described: square-level data (repeated-measures/mixed models) and plot-level data (more complex hierarchical structures with potential plot-level residuals).
- Modelling introduces additional assumptions about data distributions, which must be checked for validity.

## Square Level Data
- Model treats mean values within each Land Class across surveys as fixed effects; stock estimates come from land-class means scaled by land area.
- Random effects capture square-level variation and correlation of survey deviations within squares over time.
- The model is a repeated-measures/mixed-effects structure, allowing estimation of stock and change in a formally consistent way.

## Plot Level Data
- Plot data within squares can be analysed more efficiently than summarising to square level but require proper accounting for the hierarchical structure.
- Previous approaches either collapsed data to square level or treated plots as independent, risking bias or inefficiency.
- The modelling framework can incorporate an additional plot-level random effect, enabling bootstrapping to produce valid uncertainty estimates.

## Model Specification
- General form for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects are assumed to be normally distributed with land-class-specific variance components; within-square correlations across surveys are modelled.
- Parameter inflation (many random effects) can hinder fitting; simplifications are proposed, notably:
  - AR1 (autoregressive) structure: assumes constant within-land-class variance across surveys and a first-order correlation of successive surveys, reducing random-effect parameters to a manageable level.
- Bootstrap-based standard errors are used to maintain robustness where distributional assumptions may be violated.

## Model Testing – Broad Habitats
- Historically, Broad Habitats were a key output; inconsistencies between stock and change estimates were evident with old methods.
- Analyses using the AR1 modelling approach for 1984, 1990, and 1998 Broad Habitats showed that the new estimates eliminated the prior discrepancies.
- Comparisons between old and new methods generally kept estimates within the old method’s error bounds, with most differences small.
- Consistent analyses extended to plot-level soil data, confirming feasibility beyond square-level data and supporting adoption of the new methodology for 2007.

## Limitations and Implications
- The AR1 model with bootstrap provides a practical balance between model complexity and computational feasibility for large numbers of variables.
- Estimation of variance and covariance components is more sensitive to model specification; fixed-effect estimates are relatively robust.
- For very non-normal data, transforming to a different scale can complicate interpretation on the original measurement scale.
- Some variables (e.g., freshwater standing water) exhibited non-normal distributions that caused convergence issues; in such cases, the old methodology was retained for reporting.
- Using data from all surveys means past estimates may be revised as new data are incorporated; this is conceptually distinct from prior inconsistencies and reflects improved information usage.
- Overall, the modelling approach is more efficient and leverages hierarchical structure, yielding more precise stock and change estimates, provided distributional assumptions are reasonable.

## References
- Barr et al. (1993); Dempster, Laird, Rubin (1977); Efron & Tibshirani (1993); Haines-Young et al. (2000); Scott (2002) among others.
- Countryside Survey documentation and related methodological work.