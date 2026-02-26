# Countryside Survey 2007 Technical Report

## Purpose and scope
- Describes the statistical methodology used for analysis of Countryside Survey (CS) data.
- Reports on changes from previous CS methodologies and explains adoption of a modelling approach for 2007 (CS2007) to achieve consistent stock and change estimates.
- Highlights that modelling uses all available information, improving precision, while bootstrap is used to derive robust standard errors and confidence intervals.

## Data and sampling context
- CS Field Survey collects data from a stratified sample of 1 km squares at the intersection of a 15 km grid covering Great Britain.
- Two levels of sampling: across squares (square level) and within squares (plot level) to capture broader and within-square features.
- Land Classification (ITE-based) is used for stratification, with country-specific adaptations resulting in distinct classes per England, Wales, and Scotland.

## Methodological changes
- Previous methods: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- New approach: modelling-based, producing consistent and more precise estimates of both stock and change by using data from all surveys in a unified model.
- Adoption driven by evidence that modelling can be robust and efficient, with care taken to validate results against the old method, especially for small subsets.

## Modelling approach
- Square level data:
  - Treated as a repeated-measures problem with a mixed effects model (fixed effects for land-class means across surveys; random effects for squares and within-square survey deviations).
  - Aims to provide consistent stock and change estimates by integrating data across all surveys.
  - Distributional assumptions govern variance components; bootstrap is used to obtain robust standard errors.
- Plot level data:
  - Recognizes hierarchical structure within squares; introduces plot-level residuals (random effects) in addition to square-level effects.
  - Both square and plot level data can be embedded in bootstrap procedures for inference.
- Model specification:
  - General form: y_ijk = a_i_k + s_i_j + e_i_jk
  - a_i_k: fixed effects (land-class means for survey k)
  - s_i_j: square-level random effect
  - e_i_jk: repeated-measures random effect
  - Variances/covariances modeled with options to reduce parameter count (e.g., AR1 assumptions across surveys).
- Parameter reduction and AR1:
  - To keep models tractable, random effects are simplified (e.g., common variance across surveys, AR1 structure for covariances).
  - AR1 model reduces random parameters to a manageable number per land class, enabling automated analysis across many variables.
- Model testing and robustness:
  - Bootstrap standard errors are used because fixed-effect estimates are robust to some mis-specifications, while variance components are sensitive.
  - Analyses include cross-checks against old methods to ensure results remain within prior uncertainty bounds.

## Implementation and validation
- Consistency testing:
  - Broad Habitat analyses (using data from 1984, 1990, 1998) show that modelling methods remove discrepancies between stock and change observed with older methods.
  - Stock and change estimates from the new model generally align with previous estimates within their prior error bounds.
- Scope and feasibility:
  - AR1 model provides a good balance of stability, speed, and robustness for large-scale application across numerous variables.
  - Full parametrised models are computationally intensive; AR1 with bootstrap was found practical for CS2007.
- Cross-validation:
  - New and old methods run in parallel to verify that differences are small and within historical inconsistency ranges.

## Limitations and implications
- Computational complexity:
  - Bootstrapping and mixed-model fitting are demanding; large-scale analyses require automation and careful model selection.
- Sensitivity to distributional assumptions:
  - Fixed effects are robust, but variance/covariance parameters can be affected; bootstrap mitigates some risks.
- Data characteristics:
  - Very non-normal data (e.g., standing water) can cause convergence issues; in such cases, older methodologies may be used for those variables.
- Consistency and updating:
  - Because analyses use data from all surveys, estimates for earlier years may be revised as new data become available, which differs from the previous approach of static past estimates.
- Practical benefits for GIS:
  - More precise, consistent estimates across time enhance map-based visualization and trend analysis.
  - Results integrate information from multiple survey periods, supporting better spatial decision-making and policy support.
  - Automated, standardized modelling enables scalable production of stock/change maps and associated uncertainty.

## Additional notes and references
- The report includes detailed methodological descriptions, comparisons with previous CS methodology, and references to foundational statistical methods (e.g., EM algorithm, bootstrap).
- The approach is designed to be implemented in automated pipelines to support large numbers of variables, with ongoing validation to ensure robustness across cases.