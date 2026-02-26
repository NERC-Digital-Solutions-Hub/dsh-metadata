# STATISTICAL METHODOLOGY FOR COUNTRYSIDE SURVEY DATA

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data, with a focus on changes introduced for CS in 2007.
- Old methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, leading to mismatches between stock and change.
- Modelling approaches for consistent estimation were found feasible and robust, generally yielding estimates close to old methods but with improved consistency and precision.
- The 2007 CS adopted a modelling-based, consistent estimation framework that uses all available information and accounts for data hierarchy, improving precision.
- Implementing modelling is computationally intensive; AR1 mixed-effects models with bootstrap were selected for practicality and robustness.
- Validation involved comparing new modelling results with old methods and across small data subsets; differences were typically within the previously observed inconsistencies.
- A key implication is that estimates for any one survey can be updated as new data become available, potentially revising earlier results slightly; this dynamic updating reflects the use of all surveys in estimation.
- Limitations include reliance on distributional assumptions for variance/covariance components and potential non-normality issues; bootstrap methods help mitigate these concerns.

## 1. Introduction
- Countryside Survey data come from a stratified sample of 1 km squares over a 15 km GB grid.
- Each selected square is mapped and measured at two levels: square level (whole square) and within-square plot level.
- Measurement types range from binary to continuous, with land classification (ITE) guiding stratification; classifications have evolved (GB→country-specific: England, Wales, Scotland) to 45 classes in CS2007.
- The aim is to produce regionally and nationally representative estimates of stock and change for various features.

## 2. Overview of Previous CS Methodology
- Previous estimation combined land class means to produce national or regional estimates, weighting by land class area.
- Stock estimates used all data from a survey; change estimates used repeated measurements only, causing inconsistencies between stock and change.
- Missing data (e.g., unrepeated squares due to landowner refusals or new squares) contributed to discrepancies.
- Bootstrapping had been introduced for significance testing due to non-normalities in some features.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies between stock and change were not errors but artifacts of differing data usage.
- The goal was to achieve consistency across stock and change estimates, including between adjacent and non-adjacent survey intervals.
- Modelling approaches could provide consistent and efficient (more precise) estimates for both stock and change and be applicable to square and plot level data.
- The modelling approach requires more assumptions about data distributions, necessitating careful validation, especially for small subsets.

## 4. Modelling Approach for Consistent Estimation

### 4.1 Square Level Data
- Square-level data treated as a random sample within each land class; standard repeated-measures (mixed) models are used.
- Fixed effects represent land-class means across surveys; random effects capture square-level variation and survey-to-survey correlations.
- The simplest fixed-effects model regresses the mean within each land class on survey year; differences between successive surveys provide consistent change estimates.
- Random effects (squares and repeated measures) account for hierarchical data and correlations across surveys.

### 4.2 Plot Level Data
- Plot-level data within squares can be handled by extending the square-level model to include an additional plot-level random effect (plot residuals), or by allowing for square-level variation while respecting the sampling structure.
- Bootstrapping can be applied in conjunction with these mixed models to obtain robust standard errors.

### 4.3 Model Specification
- General form: yijk = ai_k + sij + eijk, where:
  - ai_k are fixed effects (land-class means per survey),
  - sij are square random effects,
  - eijk are repeated-measures residuals.
- Random effects are assumed normal with land-class-specific variances; residuals may have covariances that vary by land class and survey.
- The hierarchical model becomes parameter-heavy as the number of surveys grows; thus, simplifications are used.

### 4.4 Reducing Model Complexity
- To keep models tractable, random-effect parameters are often constrained:
  - Variance components may be constant across surveys (σi) or land classes.
  - Covariance structures may be simplified using an autoregressive AR1 approach, assuming constant within-land-class variance and a first-order autocorrelation for survey residuals.
- The AR1 approach reduces the number of random parameters to three per survey, regardless of the number of surveys.

### 4.5 AR1 Modelling and Bootstrap
- Although fixed effects are relatively robust, variance and covariance estimates are sensitive to distributional assumptions.
- Bootstrap estimation of standard errors is recommended and robust to mis-specification.
- The AR1 model with bootstrap SEs was tested as a practical, robust approach for CS data.

### 4.6 Model Testing – Broad Habitats
- Broad Habitat data (stock and change estimates for seven habitats across 1984, 1990, 1998) were re-evaluated.
- Old methods produced inconsistencies between stock- and change-based estimates; modelling (AR1) provided consistent estimates, with changes computed as the difference between stock estimates or via summed inter-survey changes.
- Differences between old and new methods were generally small and within prior inconsistencies; the modelling approach resolved historical discrepancies.
- Findings for plot- and soil-level data supported the feasibility and consistency of modelling across data types, leading to adoption of the new approach for CS2007.

## 5. Limitations and Implications
- Model-based analysis with bootstrapped SEs is computationally demanding, though AR1 provides a practical balance of speed and robustness.
- Fixed effects estimates (stock and change) are robust to some mis-specification of random-effects distributions; variance/covariance estimates are more sensitive.
- Very non-normal data (e.g., standing water) may cause convergence issues; in such cases, older methods may be used for presentation.
- Adoption of a consistent modelling framework means estimates for a given survey can be updated as new data are integrated, which may revise earlier results slightly.
- The approach leverages all available information, respects data hierarchy, and generally yields more precise estimates.
- Practical implications include the need for automated, scalable modelling and careful communication of updated estimates over time.

## 6. References
- Barr et al. (1993), Countryside Survey 1990 Main Report
- Dempster, Laird, and Rubin (1977)
- Efron and Tibshirani (1993)
- Haines-Young et al. (2000)
- Scott (2002)