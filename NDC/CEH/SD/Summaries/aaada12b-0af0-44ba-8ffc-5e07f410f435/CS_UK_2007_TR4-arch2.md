# STATISTICAL METHODOLOGY FOR ANALYSIS OF COUNTRYSIDE SURVEY DATA

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, summarising previous methods and detailing the changes implemented for CS in 2007.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling approaches to achieve consistent estimation were found feasible and robust, with differences from old methods generally within existing inconsistency bounds.
- The new modelling approach uses all available information, yielding more precise estimates; estimates for earlier surveys can be revised as new data informs the model, though changes are typically small.
- Implementation is technically demanding, requiring substantial computing time due to iterative model fitting; nonetheless the approach provides a substantially improved product.
- The report demonstrates consistency checks comparing old and new methods and discusses limitations, validation, and implications for reporting.

## What Countryside Survey Data Looks Like
- Data come from a stratified sample of 1 km squares across GB, with measurements at two levels:
  - Square level: measurements that apply to the whole square (e.g., habitat areas).
  - Plot level: measurements within squares (e.g., vegetation, soils) across multiple plots per square.
- Land Classification is used to define strata; classifications have been updated over time (GB 32 -> 42 -> 45 classes) with country-specific classifications (England, Wales, Scotland).
- Measurements include binary and continuous variables, and estimates are weighted by land class area when aggregating to regional or national levels.

## Why Methods Needed to Change
- Past reports showed inconsistencies: stock estimates from all data vs. change estimates from repeated measurements did not align.
- Missing information between surveys (e.g., unrepeated or newly added squares) caused discrepancies when comparing adjacent surveys or non-adjacent periods.
- The aim shifted from describing current surveys and changes since the last survey to providing consistent estimates across the full timeline from the first survey to the present.
- Several approaches to achieve consistency were considered; modelling emerged as the most consistent and efficient method for both square and plot data.

## Modelling Approach for Consistent Estimation
- Consistent estimation uses modelling (mixed effects/repeated measures) to estimate both stock and change, incorporating data from all surveys.
- Benefits:
  - Produces consistent and more precise estimates.
  - Estimates for earlier surveys can be updated as new data informs the model.
- Drawbacks:
  - Requires stronger distributional assumptions about the data.
  - Model fitting is computationally intensive.
- Implementation uses two data levels:
  - Square level data: treated with repeated measures mixed models.
  - Plot level data: extended models to account for the hierarchical plot-to-square structure.
- Bootstrap is used to obtain standard errors and confidence intervals due to potential non-normality in the data.

## Square Level Data
- Model framework: repeated measures mixed model with two components:
  - Fixed effects: land class means for each survey (stock estimates when scaled by land class area).
  - Random effects: square-level random differences and within-square (repeated measures) residuals, with correlations across surveys.
- The base model estimates stock via fixed effects across surveys; change is derived as differences in fitted stock estimates, ensuring automatic consistency.

## Plot Level Data
- Plot data within squares are more complex due to hierarchical structure.
- Previous analyses either summarized to square level or treated plots as independent within a land class, both with limitations.
- Modern approach:
  - Include a plot-level random effect in addition to the square-level effect, with correlated survey residuals focused on the plot level.
  - Both square- and plot-level models can be embedded within bootstrap procedures to obtain robust uncertainty estimates.

## Model Specification
- General form for square level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class means across surveys)
  - s_ij: square-level random effect
  - e_ijk: within-square, repeated-measures residual
- Variance components:
  - s_ij ~ Normal(0, τ_i^2) varies by land class
  - e_ijk ~ Normal(0, σ_ik^2) varies by land class and survey, with covariances between surveys
- A major challenge is the large number of random parameters when many surveys are involved. To keep models practical, two reductions are common:
  - Assume random effect variances do not vary across surveys (σ_i common across surveys).
  - Use an autoregressive AR1 structure for covariances across successive surveys, reducing repeated-measures parameters to a small, consistent set.
- Fully parameterised models are slow; the AR1 model with bootstrap standard errors provides a robust, efficient compromise.
- Fixed effects are relatively robust to distributional mis-specification of random effects, but variance-covariance estimates are sensitive. Bootstrap helps maintain accurate SEs.

## Model Testing – Broad Habitats
- Historical data on Broad Habitats (1984, 1990, 1998) were reanalyzed to test modelling approaches.
- Old methods produced inconsistencies between stock and change; the AR1 modelling approach yielded consistent estimates with smaller, more reliable SEs.
- Changes between old and new methods were generally small relative to existing inconsistencies, and new estimates aligned within previous error bounds.
- Results supported adopting the modelling approach for CS2007 and extending consistent estimation to soil (1978–1998) and plot-level data, promoting a uniform, scalable approach.

## Limitations and Implications
- Bootstrapped SE estimation with complex models is computationally demanding but feasible; fixed-effect estimates are robust across reasonable model variations.
- Fully parameterised models are slow; AR1 offers a stable, scalable solution suitable for automated application across many variables.
- Distributional assumptions for random effects can affect variance estimates; bootstrap SEs mitigate this risk.
- Some variables with highly non-normal distributions (e.g., standing water) posed convergence issues; in such cases, older methodologies may be preferred for those variables.
- Results are updated as data accumulates; estimates for earlier surveys may shift slightly with new information, reflecting the integrated, all-surveys approach.
- Implications for reporting:
  - Consistent estimates across time, with improved precision, but with occasional revisions to earlier figures as new data are incorporated.
  - Results are presented on the original measurement scale; transformations are avoided when reporting fixed- and random-effects-derived quantities.

## Practical Implications for Analysts Monitoring the Environment
- Provides a robust, consistent framework for temporal environmental monitoring, enabling fair comparisons across surveys and habitats.
- Uses all available data and respects the hierarchical structure (square and plot levels), improving precision without sacrificing interpretability.
- Bootstrap-based uncertainty quantification supports significance testing and clearer communication of trends.
- Automated modelling approach supports scalable analysis across large numbers of variables and habitats, aligning with standardised monitoring practices.
- Emphasizes data provenance and consistency, with explicit handling of missing information and its impact on stock and change estimates.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P., et al. (1977). Maximum likelihood from incomplete data via the EM Algorithm.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H., et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.