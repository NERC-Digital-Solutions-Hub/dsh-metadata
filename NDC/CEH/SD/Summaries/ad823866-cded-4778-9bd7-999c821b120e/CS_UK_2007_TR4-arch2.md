# Statistical Methodology for Countryside Survey Data (CS2007)

- Purpose and scope
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data.
  - Documents changes introduced for CS in 2007 to achieve consistent estimation of stock and change over time.
  - Highlights the shift from previous methods to modelling-based approaches that utilise all available data and the survey hierarchy.

- Why the modification was needed
  - Previous methods treated stock and change with different data sets (stock used all data from a survey; change used only repeated measurements), causing inconsistencies between stock and change estimates.
  - Inconsistencies arose when comparing adjacent surveys and across non-adjacent time spans.
  - New modelling approaches aim to produce consistent, efficient (more precise) estimates by using data from all surveys and coherently accounting for missing information.

- Key methodological changes
  - Move to modelling-based consistent estimation for both square and plot level data.
  - Transition from simple means/standard errors to mixed-effects repeated-measures models.
  - Use of bootstrap to obtain robust standard errors and significance tests due to potential non-normality.

- Modelling framework and data structure
  - Data levels
    - Square level: Information for complete 1 km squares within Land Classes; includes fixed effects by survey and square-level random effects.
    - Plot level: Within-square plots; requires respecting the hierarchical sampling while modelling plot- and square-level variation.
  - Modelling approach
    - Fixed effects represent land-class means across surveys.
    - Random effects capture square-level and plot-level variation and their correlations across surveys.
    - The goal is to produce consistent stock estimates and, by construction, consistent changes (differences between stock estimates across surveys).
  - Square-level modelling details
    - Repeated measures (mixed) model with fixed effects for land classes by survey.
    - Random effects include square-level deviations and survey-to-survey residuals with correlations.
  - Plot-level modelling details
    - Extends square-level models to include a plot-level residual/random effect.
    - Allows for correlations of plot measurements within squares and across surveys.
    - Bootstrapping can be applied to these mixed models to obtain robust standard errors.

- Model specification and practical considerations
  - General form for square-level data: y_ijk = a_i_k + s_i_j + e_i_jk
    - a_i_k: fixed effects (land-class means for survey k)
    - s_i_j: square-level random effect
    - e_i_jk: repeated-measures residuals
  - Distributional assumptions
    - Random effects assumed normal with land-class-specific variances.
    - Repeated effects and covariances allowed to differ by land class and survey.
  - Parameter reduction (AR1 approach)
    - To keep models tractable with many surveys and land classes, assumptions are made to reduce random-effect parameters.
    - Common variance across surveys (σ_i) and autoregressive (AR1) structure for covariances reduce parameters to a manageable level.
    - Bootstrap standard errors are used to maintain robustness given potential mis-specification of distributions.
  - Model testing and consistency checks
    - Comparisons between old and new methods show most estimates remain within old error bounds.
    - Tests on Broad Habitats indicate modelling yields consistent stock and change estimates that resolve previous inconsistencies.

- Broad Habitats and other data
  - Re-analysis of Broad Habitats (1984, 1990, 1998) with the new modelling approach showed no major discrepancies relative to the old method, and improvements in consistency.
  - Applications to soil data (1978 vs 1998) and plot-level data confirmed feasibility of consistent estimation across data types.
  - Result: Adoption of the modelling approach for CS2007 data.

- Limitations and implications
  - Computational demands: modelling with bootstrapping is time-consuming; full parameterised models can be slow, so AR1 offers a practical balance.
  - Model selection: fixed-effects are robust to some mis-specification, but variance/covariance parameters are more sensitive; bootstrap mitigates this.
  - Data updates and reporting
    - Estimates for any single survey may be updated as new surveys are added, since all surveys inform fixed effects through the model.
    - This implies that historical results may be revised slightly with new data; however, updates are small and conceptually consistent with the approach.
  - Practical guidance
    - Use AR1 with bootstrap for large-scale automated analyses.
    - Implement checks comparing new vs old methods to ensure consistency within expected discrepancies.
    - Balance model complexity with automated application across many variables.

- Practical outputs and data management
  - Outputs include stock and change estimates with associated bootstrap-based uncertainty.
  - The modelling framework leverages all available information and respects the hierarchical sampling structure.
  - Datasets and analyses are prepared to support standardized reporting formats (e.g., maps, tables), with results that can be stored and reused in ongoing monitoring processes.

- References and underpinning work
  - Foundational methods and prior CS analyses (e.g., Barr et al. 1993; Dempster et al. 1977; Efron & Tibshirani 1993; Haines-Young et al. 2000; Scott 2002) inform the modelling approach and bootstrap techniques.

- Bottom line for analysts monitoring the environment
  - The CS2007 methodology adopts a consistent, model-based framework to estimate stock and change, accommodating data from all surveys and the hierarchical structure of the data.
  - This approach improves precision, enables updates with new information, and provides robust uncertainty via bootstrapping, albeit with higher computational demands.
  - It resolves prior inconsistencies between stock and change estimates and supports standardized, repeatable reporting across time.