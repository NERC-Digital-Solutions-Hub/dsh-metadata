# Countryside Survey 2007: Statistical Methodology

- Purpose and scope
  - Describes the statistical methodology for analyzing Countryside Survey (CS) data.
  - Summarises previous CS methods and details changes implemented for CS in 2007 to achieve consistent estimation of stock and change using modelling.

- Key motivation for methodological change
  - Previous approaches computed stock using all data from a survey and change from repeated measurements, causing inconsistencies between stock and change estimates.
  - Modelling-based, consistent estimation using data from all surveys was investigated and found feasible and robust, with differences from old methods generally within existing inconsistencies.

- Modelling approach and benefits
  - Adopted modelling for consistent and more efficient (more precise) estimates of stock and change.
  - Uses all available information and properly represents data hierarchy (square and plot levels) across surveys.
  - Requires additional distributional assumptions; results are checked against the old methodology, especially for small subdatasets.
  - Outputs from newer modelling can slightly revise prior survey estimates as new data become available, but these changes are typically small.

- Data structure and sampling
  - CS data come from a two-level sampling framework:
    - 1 km square level sampled within a GB-wide grid, stratified by the ITE Land Classification.
    - Within each square, plots are sampled to capture within-square variation (vegetation, soils, etc.).
  - Data types include binary and continuous variables; changes in Land Classification (country-specific reporting) have led to 45 classes (England, Wales, Scotland separately organized).

- Estimation methods
  - Old method: compute means and standard errors for land classes, then weight and combine to region totals; assumes mean estimates are independent across land classes.
  - Bootstrap: used since CS2000 to obtain standard errors and confidence intervals because some features are skewed and normality assumptions may be invalid.
  - New modelling approach: interprets stock and change jointly via mixed-effects/repeated-measures models, producing consistent and more precise estimates.

- Modelling specifics
  - Square-level data
    - Considered as repeated-measures within land classes; use a mixed-effects model with:
      - Fixed effects: land-class–survey means (stock per survey).
      - Random effects: square-level deviations and repeated-measures (survey) deviations, with correlations across surveys.
    - General form for square-level data: y_ijk = a_iK + s_ij + e_ijk, with appropriate normality assumptions for random effects and residuals.
  - Plot-level data
    - Plot data within squares can be modelled by extending the square-level model to include a plot-level random effect, capturing within-square variability.
    - Two modelling options: (1) include plot residuals alongside square residuals; (2) treat plots within a land class with correlated survey residuals.
    - Both options can be embedded in bootstrapping to obtain robust SEs.
  - Parameter reduction and AR1 approach
    - Full model with all variance/covariance parameters is often unstable due to many parameters relative to data.
    - Reductions:
      - Assume random effect variances do not vary by survey but are land-class specific (σ_i).
      - Use an autoregressive AR(1) structure for covariances across successive surveys, reducing repeated-measures covariance parameters to a single per-land-class parameter.
    - Result: a stable AR1 model with three random-effect parameters per survey, regardless of the number of surveys.
  - Estimation and validation
    - Fixed effects are robust to mis-specification of random-effects distributions.
    - Bootstrap is used to estimate standard errors, preserving robustness even with simplified random-effects structures.
    - For the CS freshwater standing-water variable, non-normality caused convergence to a local maximum with the new method; in that case, the old method was retained for that variable.

- Model testing and application to Broad Habitats
  - Re-analysis of broad-habitat data (1984, 1990, 1998) showed substantial inconsistencies between stock and change under older methods.
  - The AR1 modelling approach eliminates these discrepancies; changes over periods are consistent with the differences of stock estimates across adjacent surveys.
  - Comparisons between old and new estimates typically fall within the historical inconsistencies of the old method, with most changes being small.
  - Results from plotting and soil data (including plot-level data) supported the feasibility and benefits of consistent estimation under the new modelling framework.

- Limitations and practical implications
  - Computational demands are higher (iterative model fitting and bootstrapping).
  - Some models with full parameterization are slow; AR1 offers a practical balance between speed and accuracy.
  - Results depend on distributional assumptions; fixed-effects estimates tend to be robust, but variance/covariance estimates are more sensitive.
  - Very non-normal data may challenge the modelling approach; in rare cases, old methods may be preferred for that variable (e.g., standing water in CS freshwater data).
  - Adoption implies that estimates for any given survey may be updated as new surveys are added, reflecting the use of information across all surveys. This is conceptually different from prior inconsistencies but expected with continuous data integration.

- Overall takeaway
  - The CS2007 statistical methodology adopts a modelling-based, consistent estimation framework (AR1 mixed models with bootstrapping) to produce more precise, coherent stock and change estimates across surveys, while leveraging all available data and preserving a robust analytical approach.