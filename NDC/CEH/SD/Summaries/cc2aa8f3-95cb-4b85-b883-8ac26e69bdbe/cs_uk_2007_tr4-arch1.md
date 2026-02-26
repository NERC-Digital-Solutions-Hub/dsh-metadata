# Statistical Methodology Used for the Analysis of Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Investigation with CS Broad Habitat data showed that consistent estimation via modelling was feasible and robust; differences from old methods were generally small.
- A modelling approach with consistent estimation was adopted for CS 2007 to utilise all available information and produce more precise estimates.
- The modelling approach introduces additional distributional assumptions; results, especially for small subsets, were checked against the old methodology to ensure validity.
- While more efficient, the new method is computationally intensive because it iteratively fits models rather than performing formulaic calculations; an AR1 mixed-effects model with bootstrap was chosen for practicality and robustness.
- Comparisons between old and new methods showed most changes were within the discrepancies already present under the old approach; the new method was adopted to provide consistent estimates across time.
- The AR1 model reduces the number of random-effect parameters, enabling automated application across many analyses; bootstrap provides robust standard errors and confidence intervals.
- Adoption of consistent estimation affects time-series reporting: estimates for past surveys may be revised as new data are incorporated; this reflects using all available information rather than strictly preserving earlier results.
- The approach was tested on Broad Habitats and soil data and extended to plot-level data, supporting a unified, consistent framework for square and plot data.

## 1. Introduction
- CS data come from a stratified sample of 1 km squares on a 15 km GB grid, with two sampling levels: whole squares and features within squares (plots).
- Measurements are varied (binary to continuous) and are allocated across Land Classes.
- Land Classification has evolved (GB 32 → 42 for CS2000; 45 for CS 2007) with country-specific classifications for England, Wales, and Scotland.

## 2. Overview of Previous CS Methodology
- Regional/national estimates were formed by means and standard errors for each Land Class, then combined by area-weighted means.
- Mean estimates were assumed independent across Land Classes, which was guaranteed by the sampling design.
- Significance used normality assumptions prior to CS2000; from CS2000, bootstrap was adopted to better handle non-normal, skewed data.
- Stock estimates used all survey data; change estimates used only repeated measurements, leading to potential inconsistencies between stock and change.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies arise when stock and change are derived from different data subsets.
- To address this, several approaches were considered to achieve consistency (e.g., discarding unrepeated squares or deriving change as the difference between stock estimates).
- Modelling approaches can yield consistent and efficient (more precise) estimates for both stock and change and apply to square and plot data, but require more assumptions about data distributions.
- The chosen path emphasized modelling to provide consistency, with careful validation against the old method, especially for small samples.

## 4. Consistent Estimation
- The modelling framework uses mixed-effects/repeated-measures models to handle incomplete data and the hierarchical CS design.
- Fixed effects represent Land Class means across surveys; random effects capture square-level and plot-level variation and their correlations over time.
### 4.1 Square Level Data
- Treats the dataset as complete squares within Land Classes; uses a repeated-measures (mixed) model.
- Fixed effects: Land Class means across surveys.
- Random effects: Square-level deviations from Land Class means; correlation of square-level deviations across surveys.
### 4.2 Plot Level Data
- Plot-level data within squares can be analyzed with full hierarchical models or summarized to square level; models can incorporate an additional plot-level residual.
- Bootstrapping can be used to obtain standard errors that respect the data structure.
### 4.3 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class means at survey k)
  - s_ij: square random effect
  - e_ijk: repeated-measures error
- Random effects are typically assumed normal with Land Class–specific variances; repeated measures covariances can be structured (e.g., autoregressive AR1) to reduce parameter count.
- Parameter reduction (AR1) limits random-effect parameters to a manageable number (three per survey for each Land Class) while preserving fixed-effect robustness.
- Bootstrap estimation of standard errors is used to maintain robustness to distributional mis-specification.
### 4.6 Model Testing – Broad Habitats
- Broad Habitat data (from 1984, 1990, 1998) were analyzed to compare old methods with modelling.
- Old approach produced inconsistencies between stock and change; modelling yielded consistent estimates where stock minus previous stock equaled the sum of changes across intervals.
- Differences between old and new estimates were generally within the historical inconsistency bounds, supporting adoption of the modelling method for CS 2007 and beyond.
- Consistent analyses were also performed for soil data and a plot-level dataset, demonstrating feasibility across data types.

## 5. Limitations and Implications
- Bootstrapped, model-based analyses are computationally demanding; fully parameterised models are often impractical for large numbers of variables.
- The AR1 model balances stability, speed, and robustness; it provides reasonable fixed-effect estimates even when random-effects distributions are non-normal.
- Distributional assumptions affect variance/covariance estimation; bootstrap is used to provide robust standard errors.
- Some non-normal data (e.g., standing water) can lead to convergence issues with the new method; in such cases, the older methodology may be retained for those variables.
- Benefits include using all available information, accounting for data hierarchy, and producing more precise estimates.
- A consequence of analyses using all surveys is that estimates for past surveys may be revised when new data are added, which is conceptually different from earlier, inconsistent reporting.
- For large-scale, automated analyses, the AR1-based modelling approach is preferred to maintain consistency and efficiency across tests, while ensuring results remain robust via bootstrap validation.

## 6. References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P., et al. (1977). Maximum likelihood from incomplete data via the EM algorithm.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H., et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.