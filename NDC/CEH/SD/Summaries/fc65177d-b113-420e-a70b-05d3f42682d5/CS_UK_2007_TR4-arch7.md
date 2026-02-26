# Countryside Survey in 2007: Statistical Methodology

- Purpose: Describe the statistical methods used for Countryside Survey (CS) data analysis, summarise previous methods, and outline the changes adopted for CS in 2007 to achieve consistent estimation of stock and change.

- Key motivation for change:
  - Previous methods used all data for stock but only repeated measurements for change, leading to inconsistencies between stock and change estimates.
  - Modelling approaches can produce consistent, more efficient estimates by using information from all surveys and data levels.

- Data and sampling context:
  - Data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two sampling levels within squares: square-level (land class totals) and plot-level (within-square features, e.g., vegetation, soils).
  - Land Class classifications (country-specific) are used to weight estimates by land area for regional/national estimates.
  - Data types range from binary to continuous.

- Estimation approaches:
  - Old method: means and standard errors per land class, then weighted combination by land area; robust to various distributions but inconsistently combines stock and change.
  - Bootstrapping: used since CS2000 to obtain distribution-based confidence intervals, accommodating non-normal data.

- Why modelling? The move to consistent estimation:
  - Modelling (mixed-effects/repeated-measures) can provide consistent stock and change estimates across surveys and data levels.
  - Benefits: uses all available information, improves precision, and yields estimates that remain coherent as more surveys are added.
  - Drawbacks: requires stronger distributional assumptions and more computing time; needs rigorous validation, especially for small subsets.

- Model framework (square-level data):
  - Core idea: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land-class means for survey k)
    - s_ij: square-level random effects
    - e_ijk: repeated-measures residuals
  - Distributions: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances between surveys.
  - Goal: fixed effects provide stock estimates per survey; stock-change consistency is automatic through model structure.
  - Practical issue: full model has many random parameters; unstable with many surveys and land classes.

- Model reduction and AR1 approach:
  - To keep models practical, reduce random-parameter complexity.
  - Assumptions:
    - Variance parameters do not vary by survey; a common σ_i for all surveys.
    - Autoregressive AR1 structure for covariances: correlations decay with time, reducing covariance parameters to one per land class.
  - Result: an AR1 model with bootstrap standard errors, offering a balance of robustness and efficiency.

- Plot-level data considerations:
  - Plot-level data can extend the square-level model by adding a plot-level random effect.
  - Models can be embedded within bootstrapping to obtain robust standard errors.
  - Different modelling approaches for plots (within-squares) can be combined or compared, ensuring coherence with square-level results.

- Model specification and practicalities:
  - Emphasis on keeping fixed-effect estimates robust; variance/covariance parameters are more sensitive to mis-specification.
  - Comprehensive model testing is used (including AR1 with bootstrap) to ensure estimates stay within reasonable bounds compared with old methods.
  - Large numbers of analyses (many variables) require automated, standardized modelling choices.

- Broad Habitats testing (CS2000 data as a case study):
  - Compared old methods (stock vs. repeat-squares change) with modelling approach.
  - Modelling eliminated the inconsistencies between stock and change across 1984–1998 while producing estimates within old-method error bounds.
  - Stock-change estimates under modelling were generally as precise or more precise than old methods; differences were small and often within existing uncertainties.

- Limitations and implications:
  - Modelling with bootstrapped SEs is computationally intensive, but AR1 offers a practical balance.
  - Fixed-effect estimates are robust to some distributional mis-specifications; variance/covariance estimates are more fragile.
  - Very non-normal data may require transformations or careful handling; some variables (e.g., standing water) may still pose convergence issues, with some legacy estimates retained from the older method.
  - All-surveys modelling implies that estimates for any single survey can shift as new surveys are added, which is conceptually different from the previous notion of reporting consistency across adjacent surveys.
  - Using a consistent modelling framework improves precision and leverages hierarchical data structure; updates with new data are expected and appropriate.

- Practical outcomes for GIS and data products:
  - Produces more precise, consistent stock and change estimates across land classes and surveys, improving map-based visualisations and trend reporting.
  - Facilitates cross-survey comparability and coherent spatial representations at square and plot levels.
  - Enables automated, scalable analysis across many spatial features and habitats with a standard modelling approach.

- References (key works guiding methodology):
  - Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm) (1977); Efron & Tibshirani (1993) bootstrap; Scott (2002).

- Implementation notes:
  - CS2007 adopted the AR1 modelling approach with bootstrap SEs as the primary method for consistent estimation.
  - Analyses include checks comparing new and old methods to ensure differences are not substantial beyond prior inconsistencies.
  - When applying the modelling approach, results may revise earlier findings slightly as new information becomes available, which is expected and aligns with improved use of data.