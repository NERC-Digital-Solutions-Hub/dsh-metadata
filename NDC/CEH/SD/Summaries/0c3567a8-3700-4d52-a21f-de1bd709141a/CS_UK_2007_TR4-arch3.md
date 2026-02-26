Statistical Methodology for Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data, and changes implemented for CS2007.
- Previous methods used stock estimates from all data and change estimates from repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling-based, consistent estimation was found feasible and robust, producing estimates that differ little from old methods within existing inconsistencies, while using all available data to increase precision.
- Adoption of modelling for CS2007 required additional distributional assumptions, prompting validation against previous methods, especially for small data subsets.
- The modelling approach increases efficiency and precision; improvements to previous surveys can subtly adjust past estimates as new data inform missing values.
- Implementation was technically challenging and computationally intensive, but led to a significantly improved product.
  
## Introduction
- Technical report on sampling and analysis procedures for Countryside Survey data; justification for methodological changes for CS2007; discussion of limitations and implications; references to detailed prior CS methodology.

## Overview of Previous CS Methodology
- Sampling: hierarchical design with two levels in 1 km squares across GB; stratified by Land Classification; data collected at square level and within-square plots.
- Estimation: regional or national means and standard errors calculated by weighting Land Class estimates by land area; assumed independence between Land Classes.
- Bootstrapping: non-normality addressed by bootstrap methods for square-level data; used to estimate standard errors and confidence intervals.

## Reasons for Modifications to CS Methodology
- Prior inconsistencies: stock estimates used all data, while change estimates used repeated measurements, leading to non-aligned stock and change.
- Missing information across survey pairs (due to new squares or non-recorded squares) created discrepancies when comparing adjacent and non-adjacent surveys.
- Consideration of several consistent-estimation approaches; modelling (consistent and efficient) chosen for CS2007 to address data incompleteness and hierarchical structure.

## Modelling Basics
- Modelling aims to provide consistent estimates of stock and change by using data from all surveys and handling missing information via incomplete-data techniques (mixed effects/repeated-measures models).
- Requires distributional assumptions about random effects and repeated measures; fixed effects relate to stock/change across surveys.

## Square Level Data
- Data considered as random samples of squares within each Land Class; analysis via repeated-measures/mixed models.
- Fixed effects: land-class means across surveys treated as fixed; random effects: square-level deviations and within-square repeated-measures deviations, with correlations over surveys.
- Provides stock estimates by survey from fixed effects; change estimates derived from differences of stock estimates and are automatically consistent.

## Plot Level Data
- Within-squares plots add another data level; previous analyses either aggregated to square level or treated plots as independent, risking bias.
- Mixed models can include plot-level residuals in addition to square-level effects; both square- and plot-level models can be bootstrapped.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square random effects
  - e_ijk: repeated-measures residuals
- Random effects: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances between surveys
- With K surveys, there are K fixed effects and many random-effect parameters; the model can become unstable with many parameters, especially across numerous Land Classes.

## Random-Effects Reduction (AR1 Model)
- To keep models tractable, reduce random-effect parameters by:
  - Assuming random effects do not vary across surveys (σ_i common across surveys).
  - Using an AR1 (order-1 autoregressive) structure for repeated-measures covariances, implying constant within-land-class autocorrelation across adjacent surveys.
- This AR1 reduction yields three random-effect parameters per land class, regardless of the number of surveys.
- Bootstrap is recommended for standard errors, as parametric SEs may be biased under distributional misspecification.

## Model Testing – Broad Habitats
- Past CS outputs included stock and change for Broad Habitats; previous methods showed inconsistencies between stock- and change-derived estimates.
- Reanalysis with AR1 modelling and bootstrap produced consistent stock and change estimates, with differences from old methods generally small and within old error bounds.
- Analyses of seven Broad Habitats (1984, 1990, 1998) and additional soil/plot datasets confirmed feasibility and consistency; hence the new modelling approach was adopted for CS2007.

## Limitations and Implications
- AR1 model with bootstrap is computationally intensive but feasible; fixed-effect estimates are robust to moderate distributional mis-specification.
- Variance/covariance parameter estimates are more sensitive; non-normal data can affect convergence and standard errors.
- Some variables with highly non-normal distributions (e.g., standing water) can lead to convergence issues; in such cases, older methods may be preferred for those variables.
- Results are presented on the original scale; using models can shift past estimates as new data inform missing values.
- The modelling approach improves precision by exploiting all information and the data hierarchy; however, it reduces cross-reporting comparability over time as new surveys update past estimates.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (1977); Efron & Tibshirani (1993); Scott (2002).