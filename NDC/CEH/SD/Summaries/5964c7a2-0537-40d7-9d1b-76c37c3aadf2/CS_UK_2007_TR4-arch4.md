# STATISTICAL METHODOLOGY FOR COUNTRYSIDE SURVEY DATA

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines the 2007 modifications.
- Old methods used minimal assumptions for stock and change, but stock and change estimates were inconsistently derived from different data subsets, leading to apparent mismatches.
- Modelling-based consistent estimation (applied to CS Broad Habitat data and other datasets) is feasible, robust, and typically yields estimates closer to the precision achievable when using all available information.
- The 2007 approach adopts a modelling framework that uses all data across surveys, producing more precise stock and change estimates, with consistency between them.
- The new methodology requires additional distributional assumptions and more computational effort, but results are validated by comparison with the old method and by bootstrap-based uncertainty assessment.
- Where feasible, the AR1 mixed-effects modelling with bootstrap standard errors is used to provide robust, consistent estimates for square- and plot-level data.
- The transition improves precision and consistency, but also updates past estimates as new information becomes available, meaning results can change with new surveys.
- The approach was tested on Broad Habitat data and other datasets; overall differences from the old method were within the bounds of prior inconsistencies, and in many cases produced more reliable inferences.

## Introduction
- Purpose: provide an overview of CS sampling and analysis procedures and describe changes to estimation for CS2007.
- Scope: covers sampling design, estimation, bootstrapping, and the implications/limitations of the modelling shift.

## Overview of Previous CS Methodology
- Sampling: stratified sampling of 1 km squares on a GB-wide grid; measurements at square level and within-square plots; data types ranged from binary to continuous.
- Estimation: previous method computed means and standard errors for Land Class estimates and combined them to regional/national estimates, weighting by land class area.
- Bootstrapping: normality was assumed for significance testing prior to 2000; bootstrap was introduced to accommodate non-normal data distributions.

## Reasons for Modifications to CS Methodology
- Inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, leading to mismatches.
- Visualization of inconsistency: different methods yield different results for stock and change; presenting confidence intervals can reveal these inconsistencies without implying data errors.
- Goal: move toward consistent estimators that produce coherent stock and change estimates across adjacent and non-adjacent survey intervals.

## Consistent Estimation via Modelling
- Modelling approach: use mixed effects and/or repeated measures models to estimate stock and change across all surveys, providing consistent and more precise estimates.
- Trade-offs: requires stronger distributional assumptions about data and random effects; fits are more complex and computationally intensive.
- Practical solution: employ reduced-parameter AR1 (autoregressive) models to manage model complexity while preserving robustness of fixed-effect estimates.
- Bootstrap: continue to use bootstrap for standard errors, improving robustness to distributional mis-specification.

## Square Level Data
- Data structure: square-level observations with fixed effects representing Land Class means over surveys; random effects capture square-level variability and within-square, across-survey correlations.
- Modelling: repeated measures/mixed effects models account for hierarchical sampling and correlations across surveys.

## Plot Level Data
- Challenge: plot-level data within squares adds complexity due to additional hierarchical structure.
- Prior approaches: varied between summarizing to square level or treating plots as independent; risk of biased results if heterogeneity is mis-specified.
- CS2007 approach: extend models to include plot-level residuals (random effects) in addition to square-level effects; bootstrapping used to obtain valid standard errors.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Random effects: assumed normally distributed with land-class-specific variances; within-square and cross-survey covariances are modelled.
- Parameter reduction: to keep models tractable, assume equal variance parameters across surveys or across land classes where appropriate; AR1 structure reduces repeated-measures covariances to a small number of parameters per land class.
- Robustness: fixed effects are relatively robust to mis-specification of random effects; bootstrap standard errors help mitigate potential mis-specifications.
- Practical note: a fully parameterised model was too slow for large datasets; AR1 with bootstrap was adopted as the standard, automated approach.

## Model Testing — Broad Habitats
- Historical context: Broad Habitat stock and change estimates previously showed inconsistencies between stock-based and repeat-square change estimates.
- Modelling results: AR1-based models produced consistent stock and change estimates across 1984–1998 data; differences from old methods were within prior inconsistency ranges.
- Validation: comparisons show that new estimates are not substantially different from old estimates beyond established variability; in aggregate, the modelling approach yields coherent results across survey intervals.

## Limitations and Implications
- Computational demands: modelling with bootstrapping is significantly slower than the old method, though AR1 reduces complexity enough to be feasible for large-scale analyses.
- Model choice: fixed-effects are robust to some mis-specifications, but variance/covariance parameters are sensitive; bootstrap helps preserve accurate uncertainty estimates.
- Non-normal data: some variables with highly non-normal distributions (e.g., standing water in CS freshwater data) may not converge well under the new method; in such cases, older methods may be preferred for those specific estimates.
- Data updating: because analyses integrate data from all surveys, newer surveys can update past estimates; this is conceptually distinct from the previous inconsistencies and is seen as a natural consequence of incorporating more information.
- Automation need: given the scale (many variables), a standard, automated modelling approach is essential to ensure consistency and efficiency across analyses.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, and Rubin (1977); Efron and Tibshirani (1993); Scott (2002) – foundational methodological references underpinning the modelling and bootstrap approaches used.