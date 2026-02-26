# Countryside Survey 2007: Statistical Methodology

- This technical report describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for the 2007 CS analysis.
- It compares the old (pre-2007) methods with the new modelling approach, emphasizing the shift to consistent estimation of stock and change.

## Executive Summary

- Previous CS methods estimated stock using all data from a survey but estimated change from repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling approaches using data from all surveys can produce consistent, robust estimates for both stock and change.
- The CS 2007 move to modelling yields more precise estimates, as it utilizes all available information and the data hierarchy.
- Implementation of modelling is computationally intensive; AR1 mixed models with bootstrap were chosen for practicality and robustness.
- Validation against Broad Habitat data and prior surveys showed the new method is generally in line with old results within their prior uncertainty.

## Data and Sampling

- CS data come from a stratified sample of 1 km squares on a 15 km GB grid; two sampling levels: (1) whole squares and (2) plots within squares.
- Land Classification (LC) stratification is used, with country-specific classifications (45 LC classes for CS 2007).
- Measurements range from binary to continuous variables and are linked to both square-level and plot-level features.

## Estimation and Consistency

- Old approach: stock estimates used all data from a survey, while change estimates used only repeated measurements, creating inconsistencies when comparing stock and change.
- New modelling approach aims for consistency by jointly estimating stock and change using data from all surveys, improving precision.

## Modelling Approach

- Uses mixed effects and/or repeated measures models to handle incomplete data and the CS sampling structure.
- Fixed effects: land-class means across surveys.
- Random effects: square-level effects and within-square (plot-level) residuals, with correlations across surveys.
- AR1 covariance structure is adopted to reduce the number of random parameters and to improve stability and efficiency.
- Bootstrap is used to obtain standard errors and confidence intervals, accommodating non-normality and providing robust inference.

## Square-Level Data

- Model structure for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residuals
- Assumes normality for random components, with variances and covariances that may vary by land class and survey.
- AR1 assumptions reduce parameter count and maintain interpretability; bootstrap used to obtain robust SEs.

## Plot-Level Data

- Plot-level data (plots within squares) historically treated either as aggregated or as independent observations, which could bias SEs.
- The modelling framework can be extended to include plot-level residuals, capturing within-square variability and correlating across surveys.

## Model Specification

- Core model: y_ijk = a_ik + s_ij + e_ijk
- Distributional assumptions: normal random effects with land-class-specific variances; covariances across surveys follow AR1 structure.
- A balance is sought between model complexity and practicality for automated application across many variables.

## Model Testing – Broad Habitats

- Analyses of Broad Habitats using 1984, 1990, and 1998 data show that modelling eliminates the inconsistencies seen with older methods.
- Stock and change estimates from the new model align with the old method within their prior uncertainty; changes between methods are generally small relative to existing variability.
- The new method supports consistent reporting over time, including plotting changes over multi-survey intervals.

## Limitations and Implications

- Modelling with bootstrapped standard errors is robust but computationally intensive; fully parameterised models are slow for large variable sets.
- AR1 model offers stability and efficiency, but variance/covariance parameters are more sensitive to distributional assumptions; bootstrap mitigates some of this risk.
- Some non-normal data (e.g., very skewed variables like standing water) may challenge convergence; in such cases, older (traditional) methods may be preferred for specific variables.
- Using data from all surveys means estimates for earlier surveys can be updated as new data arrive, which contrasts with the previous static reporting and may slightly revise past findings.
- Overall, the modelling approach should produce more precise estimates by leveraging the full data hierarchy and all available information.

## References

- Barr et al. 1993; Haines-Young et al. 2000; Dempster et al. 1977; Efron and Tibshirani 1993; Scott 2002.