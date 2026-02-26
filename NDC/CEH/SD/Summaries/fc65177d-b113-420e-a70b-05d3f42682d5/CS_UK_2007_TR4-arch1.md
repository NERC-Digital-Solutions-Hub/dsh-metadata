# Countryside Survey in 2007: Statistical Methodology and Consistent Estimation

- This technical report describes the statistical methodology used to analyse Countryside Survey (CS) data, reviews the previous CS methodology, and explains the changes implemented for CS in 2007 to achieve consistent estimation of stock and change.
- It documents why the previous approach produced inconsistencies between stock and change estimates and how modelling for consistent estimation addresses these issues.
- The new modelling approach uses all available information, improves precision, and yields results that are robust to missing data, though it relies on additional distributional assumptions and more computational effort.

## Executive Summary

- Previous CS methods were robust but produced inconsistencies: stock used all data from a survey, while change used only repeated measurements, causing mismatches between stock and change estimates.
- Modelling for consistent estimation is feasible and generally robust; CS2007 findings using modelling differ from old methods by less than the inherent inconsistencies of the old approach.
- CS2007 adopts modelling-based consistent estimation, which leverages all information and improves precision; estimates for earlier surveys can be updated when new data are added, though changes are typically small.
- The modelling approach requires extra assumptions about data distributions and involves substantial computer time due to iterative model fitting.
- A practical AR1 mixed-effects model reduces the number of random parameters, enabling automated application across many variables; bootstrap is used to obtain robust standard errors.
- The modelling framework is described for square-level data (and extended to plot-level data), with explicit model specifications and assumptions.
- Model testing, including Broad Habitats, shows that consistent estimates align with previous results within existing error bounds and eliminate the inconsistencies observed with the older methods; the approach was adopted for CS2007.
- Limitations include sensitivity to distributional assumptions for variance/covariance parameters, non-normal data issues (e.g., freshwater standing water), and computational intensity; results are presented on the original measurement scale.
- Implications include updated backward-looking estimates as new surveys add information; the approach better represents data hierarchy and uses all available information, though it may update earlier findings.

## 1. Introduction

- The report outlines sampling and analysis procedures for CS data, contrasting them with the previous methodology and detailing changes for CS2007.
- CS sampling uses a stratified sample of 1 km squares on a GB-wide 15 km grid; measurements occur at two levels within each square (square-level and within-square plot-level measurements) across multiple data types.
- Land Class stratification (based on ITE Land Classification) underpins country-specific reporting, with separate classifications for England, Wales, and Scotland.

## 2. Overview of Previous CS Methodology

- Regional/national estimates were formed by means and standard errors for each Land Class, weighted by Land Class area to obtain region-wide estimates.
- Stock estimates used all data from a survey; change estimates used only repeated measurements, leading to mismatches and perceived inconsistencies between stock and change.

## 3. Reasons for Modifications to CS Methodology

- Discrepancies between stock and change estimates prompted exploration of consistent estimation methods.
- Three potential consistent approaches were discussed (stock from all data with change from stock differences; change from repeated squares; modelling for stock and change). Modelling was found to be feasible, robust, and applicable to both square and plot data, producing consistent and more precise estimates.
- While the modelling approach requires stronger distributional assumptions, its performance was checked against the old method to ensure results remained within previous error bounds.

## 4. Consistent Estimation

### 4.1 Possible Approaches

- Stock from all measurements with change as the difference between stock estimates (consistent but may be inefficient if survey-to-survey covariance is large; not ideal for plot-level data; easy to implement).
- Change from repeated measurements only (robust but potentially less efficient and not directly applicable to some data types).
- Modelling to estimate both stock and change consistently (applicable to square and plot data; more efficient and conceptually coherent; chosen for CS2007).

### 4.2 Modelling Basics

- Incomplete data techniques (e.g., EM, mixed models) allow estimation with missing data, but require distributional assumptions.
- Consistent estimation for CS involves fitting mixed effects/repeated measures models with fixed effects (stock/change) and random effects (capturing sampling structure).
- Models estimate variances and covariances in addition to means; fixed effects are robust to some mis-specification of random effects.

### 4.3 Square Level Data

- Data within complete 1 km squares are treated as a random sample within each Land Class; a repeated-measures (mixed) model is used.
- Fixed effects: Land Class means across surveys (a_ik).
- Random effects: Square-level deviations (s_ij) and repeated-measures deviations (e_ijk), with correlations across surveys.
- The model provides stock estimates (via Land Class means scaled by area) and consistent change estimates (differences of fitted stock means or derived from model structure).

### 4.4 Plot Level Data

- Plot-level measurements within squares are more complex; earlier analyses either aggregated to square level or treated plots as independent, potentially biasing standard errors.
- The modelling framework extends to include plot-level residuals, allowing for square-level variation plus plot-level deviations; both types of data can be incorporated within bootstrapping.

### 4.5 Model Specification

- General square-level model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land-class means across surveys), s_ij as square-level random effects, and e_ijk as repeated-measures residuals.
- Normal distribution assumptions for random effects, with land-class-specific variances and survey- and land-class-specific measurement errors.
- A large number of random effects can make full models unstable; simplifications are used to maintain tractable estimation.

### 4.6 Model Testing – Broad Habitats

- Analyses of Broad Habitat data (1984, 1990, 1998) using modelling eliminated the inconsistencies observed with the old method; stock estimates and changes derived from the model were consistent and summed properly across periods.
- Comparisons showed most differences between old and new methods were small relative to the old method’s inherent inconsistencies; the new approach provided consistent estimates for square, soil, and plot-level data.
- The AR1 modelling approach, combined with bootstrap SEs, was identified as a practical, robust choice for CS2007.

## 5. Limitations and Implications

- Bootstrapping with square-level data is computationally demanding; the AR1 model balances robustness, speed, and a manageable number of random parameters.
- Fixed-effect estimates (stock and change) are robust to moderate distributional mis-specifications; variance/covariance parameters are more sensitive.
- Very non-normal data can cause convergence to local maxima or estimation issues (e.g., freshwater standing water); in such cases, older methods may be retained for those variables, or alternative transformations would be needed.
- Large-scale, automated analyses require a standard modelling approach; AR1 with bootstrap provides robustness and practical feasibility for CS’s breadth of analyses.
- Because analysis uses data from all surveys, estimates for any given survey may be updated as new data are added; this differs from the previous practice of fixed estimates with limited updating.
- The approach reduces inconsistencies, improves precision, and aligns results across different data levels (square, plot), but requires careful interpretation when comparing results across reporting occasions.

## 6. References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Dempster, A.P., et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm. J.R. Statist. Soc. B.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.
- Haines-Young, R.H., et al. (2000). Accounting for nature: assessing habitats in the UK countryside, DETR, London.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix. J. Statistical Computation and Simulation.
- This report is copyrighted by the Natural Environment Research Council (NERC).