# Statistical methodology for the Countryside Survey data (CS2007)

- Purpose
  - Describe the statistical methodology used to analyze Countryside Survey (CS) data and explain changes introduced for CS 2007 to achieve consistent estimation of stock and change.

- Why methodology changed
  - Previous estimates of stock used all data from a survey, while change relied on repeated measurements, causing inconsistencies between stock and change estimates.
  - Modelling approaches using all available data can produce consistent and more efficient (precise) estimates, but require additional distributional assumptions that need validation.
  - Aim to provide results that are robust, transparent, and comparable across surveys, while improving precision.

- Core methodological shifts
  - Move from separate stock and change calculations to modelling-based, consistent estimation for both.
  - Use of mixed effects/repeated measures models to handle incomplete data and the hierarchical structure of CS data (squares and plots within land classes).
  - Adoption of an autoregressive AR1 structure to model correlations across successive surveys, reducing the number of random parameters and stabilising estimation.
  - Implementation of bootstrapping to obtain standard errors and confidence intervals, accommodating non-normal data distributions.

- Data structure and levels
  - Two sampling levels:
    - Square level: information for whole 1 km squares within Land Classes; data may be missing across survey years.
    - Plot level: within-square plots provide additional measurements (e.g., vegetation, soils); previous analyses treated plots variably, now incorporated into a unified modelling framework.
  - Land Classes and area weighting: estimates are scaled by land class area to produce regional/national stock and change.

- Modelling details
  - Square level data
    - Model: y_ijk = a_ik + s_ij + e_ijk
      - a_ik: fixed effects representing land-class means for survey k
      - s_ij: square-level random effect
      - e_ijk: repeated measures random effect (within-square deviations)
    - Assumptions: s_ij ~ N(0, τ_i^2), e_ijk ~ N(0, σ_ik^2) with covariances for squares across surveys; correlations modelled (AR1) to capture within-land-class survey dependencies.
  - Plot level data
    - Extend square-level model to include plot-level residuals.
    - Allow for both square-level variation and plot-level residuals, with bootstrapping to derive SEs.
  - Parameter reduction
    - To keep models tractable, assume:
      - Variances across surveys are constant within a land class (σ_i constant across surveys).
      - AR1 structure for covariances: correlations decrease with time between surveys.
    - This yields a compact model with three random-effect parameters per land class, irrespective of the number of surveys.
  - Model specification and estimation
    - Emphasis on fixed effects (stock estimates per land class per survey) being robust to distributional mis-specifications of random effects.
    - Use of bootstrap (robust to non-normality) to obtain standard errors for fixed effects.
  - Model testing: Broad Habitats
    - Compared stock/change estimates derived from the old methods with those from the modelling approach using data from 1984, 1990, and 1998.
    - Found that modelling produced consistent estimates, with differences typically small and within previous inconsistencies, supporting adoption.

- Practical considerations and limitations
  - Computational demands: modelling, especially with many variables, can be slow; AR1 with bootstrap was chosen as a workable compromise for large CS analyses.
  - Model choice sensitivity: fixed effects robust to some mis-specification, but variance/covariance parameters can be more sensitive; bootstrap mitigates some risk.
  - Non-normal data issues: very non-normal distributions (e.g., standing water) can cause convergence to local maxima or unreliable estimates; in such cases, older methodologies may be preferred for those variables.
  - Updating and consistency across reporting
    - Because analyses use data from all surveys, estimates for earlier surveys can be updated as new surveys are added.
    - This means cross-reporting consistency across years is not maintained in the same way as with the old approach; however, updates reflect new information and are considered reasonable.

- Implementation and validation
  - The CS analysis framework produces two sets of estimates for comparison: new (consistent) method and old method; differences are checked and are generally small, within prior inconsistencies.
  - Automated, standardised modelling approach was developed to apply across many variables with checks against the old method to ensure robustness.

- Implications for practice
  - Enhanced precision and consistency in stock and change estimates by leveraging all available data and the data hierarchy.
  - More efficient use of information across time, improving the reliability of habitat and landscape-level assessments.
  - Adoption supports more integrated analyses (including soils, Broad Habitats, and other plot-level data) with coherent uncertainty estimation via bootstrapping.
  - For data leadership, highlights the value of modelling-based approaches to manage incomplete data, complex sampling designs, and cross-survey comparisons while maintaining transparency about assumptions and limitations.