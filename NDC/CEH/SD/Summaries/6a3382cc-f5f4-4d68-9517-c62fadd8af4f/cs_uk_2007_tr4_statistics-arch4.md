# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, including changes introduced for CS2007 to achieve consistent estimates of stock and change.
- Previous methods used minimal assumptions and were robust but produced inconsistencies: stock used all data from a survey, while change used only repeated measurements, causing mismatches between stock and change estimates.
- Modelling-based, consistent estimation (AR1 mixed-effects/repeated-measures models with bootstrap) is feasible and generally robust; differences from old methods are typically small.
- The new approach uses all available information, increasing precision; future surveys can improve past estimates as new data reduce uncertainty.
- Implementation is technically demanding (more computer time) and required careful checks, but provides a more coherent framework across square and plot levels and across time.
- A standard AR1 modelling approach with bootstrap is adopted for CS2007 to enable automated, robust analyses across many variables, with cross-checks against the old method to ensure comparability.
- Broad Habitats testing shows modelling yields consistent stock and change estimates, resolving prior inconsistencies between methods.

## Context and Sampling Design
- CS data come from a stratified sample of 1 km squares at the intersections of a 15 km grid covering Great Britain; two sampling levels provide square-wide and within-square (plot) data.
- Land Classification (ITE) underpins stratification; the classification evolved to 45 classes for CS2007, with national classifications (England, Wales, Scotland) enabling separate reporting.
- Data types range from binary to continuous, requiring flexible modelling to reflect hierarchical structure and missing data patterns.

## Estimation and Data Handling: Old vs. New Approaches
- Old approach: calculate means and standard errors for each Land Class, then combine (weighted by land area) to get regional estimates; assumes independence across Land Classes.
- Stock vs. change inconsistencies arose because stock used all squares while change used repeated squares; this mismatch led to non-coincident stock and change estimates.
- New approach: modelling-based, consistent estimation using data from all surveys; estimates of stock and change are derived from a unified model, ensuring consistency across time.

## Modelling Basics and Rationale
- Incomplete data techniques (mixed effects/repeated measures models) enable estimating stock and change from all available data, not by imputing missing values but by using the correlation structure to inform estimates.
- Fixed effects capture land-class means across surveys; random effects capture the hierarchical structure (squares within land classes) and the repeated measurements across surveys.
- With many surveys, full models become unwieldy; reducing random-effect parameters is essential to practical fitting while preserving robust fixed-effect estimates.
- AR1 ( autoregressive) structure is adopted to model within-land-class covariances across surveys, drastically reducing parameter count and stabilising estimation.

## Square-Level Data
- Model: y_ijk = a_i_k + s_i_j + e_i_jk
  - a_i_k: fixed effects representing land-class means at each survey
  - s_i_j: square-level random effect (within land class)
  - e_i_jk: within-square, repeated-measures residual
- Assumes normal distributions for random effects with land-class-specific variances; covariances across surveys are modelled (autocorrelation).
- Benefits: stock estimates (from fixed effects scaled by land area) are automatically consistent with change estimates (differences in fitted stock across surveys).

## Plot-Level Data
- Plot-level data within squares adds hierarchical complexity; prior analyses often collapsed to square level or treated plots as independent.
- Enhanced modelling introduces a plot-level residual (random effect) in addition to the square-level effect, capturing within-square plot variation and correlations across surveys.
- Both square and plot-level models can be embedded within bootstrap procedures to obtain robust standard errors.

## Model Specification and Practicalities
- General square-level model: y_ijk = a_i_k + s_i_j + e_i_jk
- Random effects: variances and covariances are estimated; hydrocarbon of parameter count grows with number of surveys.
- To keep the model tractable, two simplifying assumptions are used:
  - Random effects variances do not vary by survey (σ_i constant across surveys).
  - Covariance structure across surveys is AR1 (first-order autocorrelation), reducing repeated-measures covariance parameters to one per land class.
- This AR1-with-constant-variance approach (AR1 model) limits random-parameter complexity to three per land class, regardless of the number of surveys.
- Parameter estimation uses bootstrap to obtain standard errors, ensuring robustness when distributional assumptions are imperfect.

## Model Testing: Broad Habitats
- Re-analysis of Broad Habitat data (1984, 1990, 1998) showed that the modelling approach eliminates stock-change discrepancies evident with earlier methods.
- Consistent stock and change estimates from the AR1 model matched differences derived from consecutive inter-survey periods when summed appropriately.
- Comparisons indicate that, for most habitats, differences between old and new methods fall within old method error bounds; gains in consistency and precision are clear.

## Limitations and Implications
- Bootstrapped, model-based estimation is computationally intensive; fully parameterised models are slow, but AR1 balances complexity and practicality.
- Fixed-effect estimates (stock/change) are robust to some mis-specification of random-effect distributions; variance/covariance parameters are more sensitive and rely on model choices.
- Very non-normal data may cause convergence issues (notably for some variables like standing water in CS freshwater data); in such cases, older methodology may be preferred for those variables.
- Adopting a model-based approach means past survey estimates can be updated as new data arrive; estimates are not fixed to prior reporting occasions because information from later surveys refines earlier estimates.
- A standardized modelling approach is needed for automation and consistency across many variables; however, model choices and checks remain important to ensure reliability.

## Practical Implications for Data Leaders
- Emphasizes the importance of a data strategy that supports consistent, cross-temporal estimation across time series and data hierarchies.
- Highlights the value of modelling approaches that utilize all available information and respect data structure (square and plot levels) for greater precision and coherence.
- Indicates the need for rigorous data governance around methodological changes, metadata, and versioning, since updates to past estimates are expected as new data are incorporated.
- Underlines computational considerations and the importance of automated, robust pipelines (AR1+bootstrap) to handle large numbers of variables without sacrificing quality.
- Encourages documenting assumptions, validating results against prior methods, and maintaining transparency about limitations and potential updates.

## References and Contact
- Key references include Barr et al. (1993); Dempster et al. (1977); Efron and Tibshirani (1993); Haines-Young et al. (2000); Scott (2002).
- Contact for Countryside Survey information: Countryside Survey Project Office, CEH Lancaster, via countrysidesurvey@ceh.ac.uk or 01524 595811.
- CS2007 was funded by Defra and NERC, with ongoing collaboration across government bodies.