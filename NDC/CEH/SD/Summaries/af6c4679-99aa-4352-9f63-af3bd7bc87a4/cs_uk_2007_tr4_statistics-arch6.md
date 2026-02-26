# Statistical methodology for Countryside Survey data

- Purpose: Describe the statistical methods used to analyze Countryside Survey (CS) data, including changes from previous methods and the rationale for adopting a modelling approach for 2007.
- Key motivation: Previous methods yielded inconsistencies between stock (current extent) and change (between surveys) estimates because stock used all data from a survey while change used repeated measurements only. Modelling offers consistent, efficient (more precise) estimates by using all available information and respecting data hierarchy.

## Executive summary
- Prior CS methods were robust but relied on minimal assumptions and produced inconsistencies between stock and change estimates.
- Modelling approaches to achieve consistency were feasible and generally aligned with previous results, with differences largely within prior inconsistency ranges.
- A formal modelling framework (AR1 mixed effects/repeated measures models) was adopted for CS 2007, requiring more computational effort but delivering more precise estimates by using all data and correctly handling data structure.
- The modelling approach uses additional assumptions about data distributions; results are validated against previous methods, with bootstrap used to obtain robust standard errors.
- The method was tested on Broad Habitats data and other datasets (e.g., soil, plot-level data) to demonstrate consistency across data types; ultimately adopted for 2007 CS.
- Implications: Estimates for any given survey may be influenced by information from all surveys, leading to updated estimates as new data arrives. This is a conscious shift from earlier reporting, reflecting the benefit of incorporating new information.

## Introduction and context
- The report outlines sampling and analysis procedures for CS data, reviewing the old methodology and detailing changes implemented for 2007.
- CS sampling: stratified sampling of 1 km squares within a GB grid; two levels of data (square-level and within-square plots) across land classes.

## Previous CS methodology (overview)
- Stock estimates: based on means and standard errors for each Land Class, then combined (weighted by land area).
- Change estimates: based on repeated measurements (paired surveys) and not directly aligned with stock estimates, causing inconsistencies.
- Bootstrapping: introduced in CS2000 to address non-normality for square-level data, improving significance estimation.

## Reasons for methodological modifications
- Inconsistencies between stock and change estimates were due to using all data for stock but only repeated data for change.
- Desire to produce consistent estimates across time and reporting horizons, including non-adjacent survey intervals.
- Modelling offers consistent, robust estimates for both stock and change, and can be applied to square and plot-level data.

## Modelling approach: basics
- Use of mixed effects/repeated measures models to handle incomplete data and to produce consistent stock and change estimates.
- Fixed effects: represent land-class means across surveys.
- Random effects: represent square-level and plot-level variation, with correlations across surveys.
- The modelling framework requires distributional assumptions for random effects and covariances; these are managed via bootstrap for robust standard errors.

## Square level data
- Data treated as a random sample of squares within land classes; a repeated-measures (mixed) model is used.
- Fixed effects: land-class means by survey.
- Random effects: square-level deviations and survey-to-survey deviations, with correlations across surveys.

## Plot level data
- Within-square plots add hierarchical complexity. Earlier analyses either summarized plots at the square level or treated plots as independent, potentially biasing standard errors.
- Extended models include plot-level residuals (random effects) alongside square-level effects; both square- and plot-level models can be embedded in bootstrap procedures.

## Model specification
- General square-level model: y_ijk = a_i_k + s_i_j + e_i_jk
  - a_i_k: fixed effects (land-class means per survey)
  - s_i_j: square-level random effect
  - e_i_jk: repeated-measures error
- Random effects are assumed normally distributed; variances and covariances vary by land class and over surveys.
- To control complexity (and instability with many random parameters), two reduction strategies are used:
  - Assume random-effect variability does not vary with land class (simplified, often unrealistic).
  - Use AR1 (autoregressive) structure: covariances between successive surveys decay with lag, reducing parameters to a manageable three per land class.
- Bootstrap is used to obtain standard errors, since fixed effects are robust but variance components can be sensitive to distributional assumptions.

## Model testing: Broad Habitats
- CS2000 Broad Habitat data (from 1984, 1990, 1998) were reanalyzed with the modelling approach.
- Result: modelling removed the inconsistencies between stock and change observed with the old method; changes derived from stock differences matched the sum of period changes.
- When comparing old vs new methods, most differences were within prior inconsistencies, and only a few estimates changed by more than a standard error.
- Additional consistency checks extended to soil data and plot-level data, supporting the adoption of the modelling approach for 2007 CS.

## Limitations and implications
- Modelling with bootstrapped standard errors is computationally intensive but feasible; AR1 offers a good balance of robustness, speed, and few random parameters.
- Fixed-effect estimates (stock/change) are robust to model mis-specification, but variance/covariance parameters are more sensitive to distributional assumptions.
- Very non-normal data (e.g., standing water) can cause convergence to local maxima or problematic estimates; in such cases, old methods may be preferred for that variable.
- Using data from all surveys means past estimates can be revised as new data arrive; this reflects improved use of information rather than reporting inconsistency.
- Overall benefits: more precise, consistent estimates by incorporating hierarchical data structure and all available information; however, models require careful checks and automated application for large-scale analyses.

## References and context
- Foundational references include Barr et al. (1993), Dempster et al. (1977), Efron and Tibshirani (1993), Haines-Young et al. (2000), and Scott (2002).
- The CS methodology report emphasizes adopting a standard AR1 modelling approach for large-scale analyses and validating results against prior methods.