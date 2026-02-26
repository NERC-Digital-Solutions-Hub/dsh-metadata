# Countryside Survey 2007: Statistical Methodology

- This technical report describes the statistical methodology used for analyzing Countryside Survey (CS) data, focusing on changes introduced for CS in 2007 and how they improve over previous methods.
- Key motivation: previous methods yielded inconsistencies between stock (overall extent) and change estimates due to using different data subsets for each, which is problematic for map-based data products and interpretation.

## Executive overview

- Previous CS methods used minimal assumptions and were robust but produced inconsistencies because stock used all data from a survey while change used only repeated measurements.
- Modelling-based, consistent estimation is feasible and generally robust; results differ from old methods by less than the discrepancies already present due to prior approaches.
- The 2007 shift adopts consistent estimation via modelling, using all available information and producing more precise estimates.
- Modelling requires additional distributional assumptions; results are validated by comparison with old-method estimates, especially for small subsets.
- The new approach yields more precise estimates and allows past survey estimates to be updated as new data become available, though changes to past estimates are typically small.
- Implementing modelling is technically demanding and more CPU-intensive, but the AR1 modelling approach provides a practical balance of robustness and efficiency.
- Software implementations include bootstrapping to obtain robust standard errors, particularly for square-level data; models are designed to be automated for large numbers of variables.

## Introduction and context

- The report outlines sampling and analysis procedures for CS data, reviews the previous methodology, and explains the reasons and details for 2007 changes.
- Fuller details of CS sampling and estimation are provided in earlier CS reports.

## Sampling and data structure in GIS terms

- Sampling uses a stratified sample of 1 km squares at the intersection of a 15 km grid covering Great Britain.
- Two levels of data collection within each square:
  - Square level: measurements that describe the whole square (e.g., habitat extent by Land Class).
  - Plot level: measurements within squares (e.g., vegetation and soils data across multiple plots).
- Land Classification (ITE) and country-specific adaptations (England, Wales, Scotland) define the strata for square selection; class counts differ by country but are related to a GB classification.

## Estimation versus modelling

- Old approach:
  - Stock estimates per Land Class used all data from a survey.
  - Change estimates used data from repeated measurements across surveys.
  - This created potential inconsistencies between stock and change.
- Modelling approach (CS2007):
  - Use mixed effects and/or repeated-measures models to estimate stock and change in a consistent framework across surveys.
  - Applies to both square-level and plot-level data.
  - Requires distributional assumptions about random effects and repeated measures; uses bootstrapping to obtain robust SEs.
  - Benefits: leverages all available information; yields consistent and more precise estimates.

## Modelling basics and implementation

- Missing data handling: modelling uses incomplete data methods (mixed models) that rely on distributional assumptions; aims to produce consistent stock and change estimates across surveys.
- General square-level model:
  - y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means in each survey)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
  - Assumes normality for random effects and residuals, with a structure that allows for correlations across surveys.
- Plot-level data:
  - Extends the square-level model by adding a plot-level residual to capture within-square variability; both square and plot-level residuals can be embedded in bootstrapping.
- Parameter reduction (AR1 model):
  - To keep models tractable with many surveys, assume random effects do not vary across surveys and/or land classes in flexible ways.
  - AR1 (autoregressive order 1) assumption reduces random-effect parameters to three per land class, regardless of the number of surveys.
  - Bootstrap is recommended for standard errors under AR1 due to potential mis-specification of variance-covariance estimates.
- Practical note: fully parameterised models are computationally slow; AR1 with bootstrap offers a robust, automated approach suitable for large-scale CS analyses.

## Model specification (conceptual)

- Square-level observation model:
  - y_ijk = a_ik + s_ij + e_ijk
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) varies by land class and survey, with covariances across squares
- Random-effects structure and covariances are designed to be parsimonious (AR1) to maintain stability and computational feasibility.

## Model testing and Broad Habitats

- Broad Habitat analysis (1984, 1990, 1998) served as a test bed:
  - Old method: stock and change estimates from stock vs. repeated squares showed inconsistencies.
  - Modelling approach (AR1) yielded consistent stock and change estimates; discrepancies were within the old method’s error bounds.
  - The modelling approach was also applied to soil data and plot-level data, confirming feasibility for consistent estimation across data types.
- Outcome: adoption of the modelling approach for 2007 CS data.

## Limitations and implications

- Bootstrapping with square-level data is computationally intensive but feasible.
- Fixed-effect estimates (stock/change) are robust to model variation; variance/covariance parameter estimates are less robust, but bootstrap standard errors mitigate this.
- Some non-normal data can cause convergence to local maxima; in such cases the old methodology may be preferred for those specific variables (e.g., standing water in freshwater datasets).
- Consistent modelling uses data from all surveys, so past estimates can be updated as new surveys are added; past reporting occasions may see small revisions.
- For large-scale analyses, a standard AR1 model with bootstrap provides a practical balance between accuracy and computational efficiency.

## Implications for GIS data products

- More precise and consistent stock and change estimates improve map-based representations and trend analyses.
- Updating past years with new survey data yields revised past estimates; users should expect small revisions over time as new information is incorporated.
- The approach supports uniform treatment of square- and plot-level data, enabling coherent map products across data scales.

## References (key sources)

- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron and Tibshirani (1993); Scott (2002).