# Countryside Survey 2007: Statistical Methodology

- Purpose: Describe the statistical methodology used for Countryside Survey (CS) data analysis, summarize previous methods, and detail the changes implemented for CS2007 to achieve consistent estimation of stock and change.

## Executive Summary (key takeaways)

- Previous CS methods used robust, minimal-assumption estimation for stock (all data from a survey) and change (only repeated measurements), creating inconsistencies between stock and change estimates.
- Modelling-based, consistent estimation is feasible and generally robust; results from modelling differ from old methods by less than the inherent inconsistencies already present.
- CS2007 adopts a modelling approach to achieve consistency and efficiency, using information from all surveys to improve estimates for both stock and change.
- The modelling approach requires additional distributional assumptions and more computation; results for small subsets are checked against the old methodology.
- Overall, modelling yields more precise estimates, and new survey data can slightly adjust previous estimates due to information being re-estimated in light of all available data.
- Implementation is technically challenging and slower than prior methods, but an AR1 mixed-effects modelling framework with bootstrap-derived standard errors provides a practical, robust solution.
- The new methodology was tested against Broad Habitat data and other datasets to verify consistency; results generally align within previous uncertainty bounds.
- A shift to consistent estimation changes presentation from single-survey emphasis to timeline-spanning reporting, highlighting the inter-survey consistency and updated estimates as new data accrue.

## Sampling and Data Structure

- Data come from a stratified sample of 1 km squares on a GB-wide 15 km grid; two hierarchical levels:
  - Square level: measurements describe features within each square; some data relate to the whole square.
  - Plot level: several plots within each square provide more detailed measurements (vegetation, soils, etc.).
- Land Classification Stratification: Land classes (21 England, 8 Wales, 16 Scotland in CS2007) based on ITE classification; the scheme supports country-specific reporting.
- Data types: mix of binary and continuous variables; measurements vary in scale and type.

## Estimation and Bootstrapping

- Old method (pre-2000): stock estimates used all data from a survey; change estimates used repeated measurements only; this created inconsistencies between stock and change.
- New method (CS2007): modelling-based estimation to obtain consistent stock and change estimates across surveys.
- Bootstrap: used to estimate standard errors and confidence intervals because some features are non-normally distributed, ensuring robust significance testing.

## Why Modifications to CS Methodology

- Inconsistencies: reported stock-change inconsistencies arose because stock and change used different data subsets.
- Approaches considered for consistency:
  - Use stock from all data and change from differences between stock estimates (easy to implement, robust, but less efficient for some data and not directly suitable for plot-level data).
  - Use modelling to estimate stock and change consistently (more efficient and applicable to square and plot data, but relies on additional distributional assumptions).
- Decision: adopt a modelling approach (consistent estimation) for CS2007, with checks against the old method to ensure results remain within prior uncertainty bounds.

## Modelling Basics and Data Types

- Mixed effects and/or repeated measures models are employed to handle incomplete data and hierarchical sampling.
- General idea: fit models with fixed effects (land-class- and year-specific means) and random effects (square-level, plot-level, and survey-to-survey correlations).
- Two data levels:
  - Square level data: treated as repeated measures within Land Classes; models include fixed effects for land classes and years, plus random square effects and survey residuals.
  - Plot level data: additional plot-level random effects can be included; models can embed plotting residuals within bootstrapping.

## Square Level Data: Modelling Approach

- y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land class i, survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Random effects distributions: assumed normal; variances can vary by land class and survey.
- Covariances: capture correlation of repeated measurements across surveys within the same square and land class.
- AR1 modelling: reduces the number of random parameters by assuming common within-land-class variance across surveys and an autoregressive structure for survey-to-survey covariances.

## Plot Level Data: Enhanced Modelling

- Plot-level measurements can be incorporated by adding a plot-level residual (random effect) to reflect within-square, within-land-class plot variation.
- Both square-level and plot-level models can be embedded within bootstrapping to obtain robust standard errors.

## Model Specification and Practical Considerations

- General square-level model: y_ijk = a_i_k + s_ij + e_ijk
- Fixed effects: a_i_k captures land-class means across surveys; interpreted as stock estimates when scaled by land-class area.
- Random effects: s_ij (square-level) and e_ijk (repeated measures); variability and covariances are modelled.
- Parameter reduction: AR1 framework and common variance assumptions reduce parameter counts, improving stability and computational feasibility for CS’s large number of variables.
- Robustness: fixed effects are relatively robust to mis-specification of random-effects distributions; bootstrap SEs help mitigate issues with variance-covariance estimation.

## Model Testing: Broad Habitats

- Historical data (1984, 1990, 1998) analyzed with both old and new methods.
- Findings:
  - Stock and change estimates from modelling do not exhibit the prior inconsistencies between stock-derived change and repeat-square change.
  - Differences between old and new estimates generally fall within the old method’s uncertainty bounds.
  - Using modelling yields consistent estimates for Broad Habitats, soil data (1978, 1998), and plot-level data, prompting adoption for CS2007.

## Limitations and Implications

- Computational demands: full parametric models are slow; AR1 with bootstrap strikes a balance between accuracy and practicality for large CS analyses.
- Model dependence: estimates depend on distributional assumptions; fixed effects are robust, but variance/covariance estimates can be sensitive.
- Non-normal data: highly non-normal variables (e.g., standing water) may cause convergence or local maxima issues; in some cases, old methodology results are kept for such variables.
- Updating previous results: incorporating data from all surveys means past survey estimates can be revised as new information becomes available; this is different from the prior, more static reporting structure.
- Advantages: more precise estimates, unified treatment of square and plot data, and better use of hierarchical structure across the survey timeline.

## Practical Implications for Analysts

- Automated, standard modelling approach (AR1 mixed effects with bootstrap) can be applied to a large number of variables to produce robust results.
- Analyses should present results on the original measurement scale; transformations are possible but require transformations back, which can complicate uncertainty propagation.
- When communicating results, emphasize consistent stock/change estimates across the full time series rather than single-survey snapshots.

## References and Acknowledgments

- Key methodological references include works on EM algorithm for incomplete data, bootstrap methods, and previous CS reporting (Barr et al.; Haines-Young et al.; Scott 2002).
- CS2007 analyses funded by aDefra-led government partnership; CEH/NERC as principal contributors.
- Contact: Countryside Survey Project Office for further information.