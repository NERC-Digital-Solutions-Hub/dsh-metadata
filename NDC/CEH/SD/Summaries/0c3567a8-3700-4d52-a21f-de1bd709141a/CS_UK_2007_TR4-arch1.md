# Countryside Survey 2007: Statistical Methodology for Consistent Estimation

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data and outline the changes made for CS in 2007 to achieve consistent estimation of stock and change.
- Motivation: Previous CS analyses used different data subsets for stock and change, causing apparent inconsistencies between estimated stock and estimated change. Modelling approaches aim to produce consistent, efficient estimates by using all available information and handling incomplete data.
- Key outcome: Adoption of a modelling (mixed-effects) approach with an AR1-based structure and bootstrap for standard errors, improving precision and enabling consistent estimation across surveys while acknowledging increased computational demands.

## Context and Sampling

- Data come from a stratified sample of 1 km squares on a GB-wide 15 km grid; two levels of sampling within each square: square-level summaries and within-square plots.
- Land classification: CS2000 increased to 42 classes (England, Scotland, Wales each with country-specific sets); by CS2007 the classification expanded to 45 classes to reflect Wales reporting needs. Each country has its own related set of classes.
- Measurements vary from binary to continuous (areas, lengths); results are scaled by land class area to obtain region-wide stock estimates.

## Estimation and Inference

- Old method: stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- New emphasis (CS2007): aim for consistency by modelling stock and change jointly using data from all surveys; use bootstrap to estimate standard errors due to potential non-normality.
- Bootstrapping: essential for robust significance testing in the presence of non-normal distributions, especially for square-level data.

## Reasons for Methodological Modifications

- Problem identified: reported stock-change inconsistencies were not errors but artefacts of using different data sets for stock and change.
- Three potential approaches to consistency (illustrated conceptually): 
  - Use stock estimates from all measurements and derive change as the difference between stock estimates.
  - Use only repeated (unrepeated) squares for both stock and change.
  - Use modelling to jointly estimate stock and change from all data (preferred for consistency and efficiency).
- Selected approach: modelling with mixed-effects/repeated-measures to achieve consistent, efficient estimates for both square and plot-level data.

## Modelling Framework

- Incomplete data concepts: CS’s hierarchical sampling requires methods that can handle missing data without imputing values directly.
- General modelling strategy: fit mixed-effects models (fixed effects for land-class means across surveys; random effects for square/plot structure and repeated measures), then transform fixed effects to stock and change estimates.
- Practical model reductions: to keep models tractable, reduce the number of random effects by assuming, for example, constant variance across surveys and land classes, and using an autoregressive AR1 structure for covariances.
- Robustness: fixed-effect estimates are robust to plausible mis-specifications of random effects; bootstrap standard errors help address potential mis-specifications in variance-covariance structure.

## Square Level Data

- Model type: repeated-measures (mixed) model with:
  - Fixed effects: land-class means across surveys (stock parameters).
  - Random effects: square-level deviations from land-class means; within-square measurements correlated across surveys.
- Structure: correlations across surveys modeled, with variance components differing by land class.

## Plot Level Data

- Challenge: plots within squares introduce additional hierarchical structure; previous analyses treated plots in diverse ways.
- Enhanced modelling: include plot-level residuals (random effects) in addition to the square-level random effects, allowing correlations to vary between plots and squares.
- Embedding in bootstrap: both square- and plot-level models can be incorporated within bootstrapping procedures to obtain robust standard errors.

## Model Specification

- General square-level model form: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square-level random effect for square j in land class i
  - e_ijk: repeated-measures residual
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2) varying by land class
  - e_ijk ~ N(0, σ_ik^2) varying by land class and survey, with covariances between surveys
- Complexity: number of random parameters grows rapidly with the number of surveys; practical reductions (e.g., AR1) help keep models stable and estimable.
- AR1 approach: common variance for all surveys within a land class and AR1 structure for covariances across surveys, reducing parameters to manage.

## Model Testing: Broad Habitats

- Historical output: CS reports often included stock and change for Broad Habitats; prior methods produced inconsistencies between stock-based change and repeat-squares change.
- Findings:
  - Old vs. new modelling approaches yielded differences generally within prior inconsistencies and, for most habitats, not statistically significant.
  - Modelling using AR1 with bootstrapped SEs provided consistent estimates across 1984, 1990, and 1998 data, and was adopted for 2007 CS analyses.
- Implication: consistent estimation does not drastically alter most results but resolves prior inconsistencies and improves precision.

## Limitations and Implications

- Computational demands: full parameterised models are slow; AR1 model with bootstrap provides a practical balance of speed and robustness.
- Model selection: fixed-effects estimates are robust to reasonable model variations; variance-covariance estimates are more sensitive, hence bootstrap is favored.
- Data scale implications: analyses use information from all surveys; estimates for past surveys may be updated as new data become available, which is conceptually different from previous reporting inconsistencies but expected with new information.
- Scale and transformations: results are presented on the original measurement scale; transforming data could complicate interpretation due to the involvement of random effects.
- Non-normal data: very non-normal distributions (e.g., standing water) can cause convergence to local maxima; in such cases, older methods may be preferred for those variables.
- Overall benefit: the modelling approach utilises all information, respects data hierarchy, and yields more precise, consistent estimates, enabling more reliable trend assessment.

## References

- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron and Tibshirani (bootstrap); Scott (2002) on maximum likelihood from incomplete data; Countryside Survey methodological reports and related literature.