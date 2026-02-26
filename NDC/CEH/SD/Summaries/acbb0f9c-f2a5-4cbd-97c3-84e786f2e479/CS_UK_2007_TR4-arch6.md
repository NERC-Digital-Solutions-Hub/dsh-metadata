# Countryside Survey 2007: Consistent Estimation

- Purpose
  - Describe the statistical methodology used for Countryside Survey (CS) data analysis.
  - Explain changes made for CS in 2007 and rationale for adopting a modelling approach that yields consistent stock and change estimates.

- Why changes were needed
  - Previous methods mixed data usage: stock was estimated from all survey data, while change depended only on repeated measurements.
  - This led to inconsistencies where reported stock differences did not equal reported changes between survey pairs.
  - Modelling with consistent estimation was found to be feasible, robust, and generally in line with prior uncertainties.

- Modelling approach (consistent estimation)
  - Use data from all surveys to estimate both stock and change via mixed effects/repeated measures models.
  - Produce consistent, efficient (more precise) estimates for stock and change across time.
  - Implement with bootstrap to obtain standard errors and confidence intervals, accommodating non-normal data.

- Data structure and levels
  - Square level data: measurements from a stratified sample of 1 km squares within Land Classes; involves fixed and random effects to reflect survey structure.
  - Plot level data: within-square plots included; models extended to include plot-level residuals (and their correlation across surveys) to respect data hierarchy.

- Model specifics (square level)
  - Basic form: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land class means across surveys)
    - s_ij: square-level random effects
    - e_ijk: repeated-measures residuals
  - Distribution and covariance structures varied by land class and survey; originally many random parameters posed fitting challenges.

- Parameter reduction and AR1 approach
  - To keep models tractable, random effects are reduced using assumptions:
    - Variances of random effects do not vary across surveys (common σ_i for each land class).
    - Repeated-measures covariances follow an AR1 structure (first-order autocorrelation) across surveys.
  - This AR1 reduction yields three random-effect parameters per survey, regardless of the number of surveys.
  - AR1 with bootstrap standard errors is recommended for robust inference.

- Plot-level modelling
  - Extend square-level model to include an additional plot-level residual/random effect.
  - Allows correlations within plots across surveys and maintains proper variance structure.
  - Both square- and plot-level models can be embedded in bootstrap procedures.

- Model testing and Broad Habitats
  - Re-analyzed Broad Habitat data (1984, 1990, 1998) to compare old vs new methods.
  - Old approach: stock from all squares vs change from repeated squares produced inconsistencies.
  - New modelling approach (AR1) produced consistent stock and change estimates; differences from old methods generally fell within prior variability.
  - For several Habitat analyses, the modelling approach yielded estimates comparable in precision to previous results but with internal consistency.
  - Also validated consistency for soil data (1978 vs 1998) and plot-level data, supporting adoption for CS2007.

- Limitations and implications
  - Computationally intensive; full parameterised models can be slow, so AR1 with bootstrap is favored for large analyses.
  - Fixed-effect estimates are robust to moderate mis-specification of random effects; variance/covariance estimates are more sensitive.
  - Non-normal distributions can affect some estimates; bootstrap helps mitigate this.
  - Some variables with highly non-normal distributions (e.g., standing water in freshwater data) may require old methods or cautious interpretation.
  - Results are updated as new surveys are added; estimates for earlier surveys may shift as new information is incorporated (a natural consequence of using all-survey data).

- Practical outcomes and adoption
  - Adopts a consistent estimation framework for 2007 CS data, enabling more reliable time-spanning assessments.
  - Uses all available information and respects data hierarchy, leading to more precise stock and change estimates.
  - Provides a scalable, automated modelling approach suitable for large numbers of variables, with checks against the old methodology.
  - Output remains in the original measurement scale (without excessive transformation) for interpretability.

- References and resources
  - Key methodological references and prior CS work cited, including bootstrap methods and mixed-effects modelling literature.
  - Documentation and CS project website for further information and data access.