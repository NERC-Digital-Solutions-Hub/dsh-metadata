# Countryside Survey 2007: Statistical methodology

- Purpose and scope
  - Describes the statistical methodology used to analyse Countryside Survey (CS) data and explains changes implemented for CS 2007 to achieve consistent estimates of stock and change across surveys.
  - Moves from historical, less consistent methods to a modelling approach that uses all available data and provides more precise estimates, with careful validation against the old method.

- Data, sampling, and measurement
  - Data come from a stratified sample of 1 km squares across Great Britain, with two sampling levels: square-level measurements and within-square plot measurements.
  - Land Classification (regional adaptations for England, Wales, Scotland) defines strata for square selection; classifications have evolved to accommodate country reporting (GB → 21 England classes, 8 Wales, 16 Scotland for CS 2007).
  - Measurements span binary and continuous variables and are tied to both square-level and plot-level structures.

- Estimation: old vs new approaches
  - Previous approach: stock estimates used all data from a survey, while change estimates used only repeated measurements. This caused inconsistencies: stock vs. change could diverge and not align across adjacent surveys.
  - New approach (CS 2007): modelling techniques to produce consistent, efficient estimates of both stock and change using data from all surveys. This approach reduces discrepancies and typically yields more precise results.
  - Bootstrapping is used to derive standard errors and confidence intervals due to potential non-normality in the data.

- Modelling basics and structure
  - Concept: use mixed effects/repeated measures models to handle incomplete data and the hierarchical sampling design.
  - Square-level data model:
    - y_ijk = a_i k + s_ij + e_ijk
      - a_i k: fixed effects representing land-class means in each survey
      - s_ij: square-level random effect
      - e_ijk: repeated-measures residual
    - Random effects are assumed normally distributed with land-class–specific variances; repeated-measures covariances vary by land class and survey pair.
  - Plot-level data: extend the square-level model to include plot-level residuals, allowing for correlations within plots and squares; both square- and plot-level analyses can be embedded within bootstrap procedures.
  - Parameter reduction (AR1 model):
    - To keep the model tractable with many surveys and land classes, reduce random-effect parameter count by assuming:
      - Variances do not vary across surveys (common σ_i for a land class across surveys).
      - Covariances follow an autoregressive (AR1) structure with a single covariance parameter per land class.
    - This yields a robust, computationally efficient model with three random-effect parameters per land class, regardless of the number of surveys.
  - Model selection and estimation:
    - Fixed effects are robust to reasonable distributional mis-specification.
    - Random-effect variance/covariance parameters are more sensitive; bootstrap standard errors are preferred for these components.
    - A dual-estimation approach (AR1 bootstrap vs old method) is used to ensure results are within expected bounds.

- Model testing and validation
  - Broad Habitat analyses (using data from 1984, 1990, 1998) demonstrated that modelling yields consistent stock and change estimates and reduces discrepancies seen with the old method.
  - Comparisons show most changes between old and new methods are small relative to existing uncertainties; the new method aligns stock and change estimates on a consistent footing.
  - The modelling approach was extended to soil data and plot-level analyses, confirming feasibility and consistency across data types, supporting adoption for CS 2007.

- Limitations and implications
  - The AR1 modelling with bootstrapped SEs is computationally more demanding than the previous method; full model fitting can be slow, necessitating automated, scalable procedures for many variables.
  - Fixed-effect estimates are robust to some mis-specifications, but variance/covariance parameter estimates are more sensitive to distributional assumptions.
  - Very non-normal data (e.g., standing water) can cause convergence or estimation issues; in such cases, the project retained older methodology for those specific variables.
  - Adoption of a model-based, data-integrative approach means that estimates for any given survey can be revised upward or downward as new data from later surveys are incorporated; cross-survey consistency is prioritized over static historical comparability.

- Practical takeaways for data leaders
  - Embrace modelling approaches that utilize all available data and respect the hierarchical sampling structure to obtain more precise, consistent stock and change estimates.
  - Use bootstrapping to obtain robust standard errors in the presence of non-normal data distributions.
  - Implement parameter-reduction strategies (like AR1) to keep models tractable across many surveys and variables while preserving estimation quality.
  - Be prepared for iterative updates: new surveys can revise past estimates, a natural consequence of integrating more information over time.
  - Ensure transparent communication about the distinction between stock and change estimates, especially when moving from old to new methods, to avoid misinterpretation of apparent inconsistencies.