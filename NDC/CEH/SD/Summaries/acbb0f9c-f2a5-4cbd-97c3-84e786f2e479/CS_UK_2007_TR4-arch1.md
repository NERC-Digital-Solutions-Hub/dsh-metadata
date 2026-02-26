# STATISTICAL METHODOLOGY USED FOR COUNTRYSIDE SURVEY DATA

## Executive summary
- Describes the statistical methodology for analyzing Countryside Survey (CS) data and the changes made for CS2007.
- Old methods: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling approaches using data from multiple surveys can provide consistent and efficient (more precise) estimates; Broad Habitat data indicated modelling was feasible and robust.
- CS2007 adopts modelling for consistent estimation; results are generally close to previous estimates within existing inconsistency bounds, but more precise.
- Modelling requires distributional assumptions and careful validation, especially for small subsets; bootstrap is used to assess significance and standard errors.
- Using a modelling approach utilizes all available information, improving past estimates as new data become available; past estimates may be updated slightly.
- Implementation is computationally intensive, requiring iterative model fitting; the AR1 mixed-model approach was chosen for practicality and robustness, with checks comparing old and new methods.

## Introduction
- The report overviews CS sampling and analysis procedures, reviews the previous methodology, and details the 2007 changes, including limitations and implications.

## Sampling
- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Two sampling levels: square-level measurements (some taken for whole squares) and within-square plot-level measurements.
- Land Classification (ITE) stratifies the sampling; country-specific classifications exist (England, Wales, Scotland).
- Measurements include binary and continuous variables; the sampling design supports estimation at regional/national levels.

## Estimation
- Original estimation: means and standard errors by Land Class, then weighted by land area to obtain region-wide estimates.
- This procedure makes few distributional assumptions but treats stock and change estimates from different data sets (all-squares vs. repeated-squares) as potentially inconsistent.

## Bootstrapping
- Significance testing uses bootstrap due to concerns about normality, especially for square-level data.
- Resampling provides distributions for stock and change without relying on normality assumptions.

## Reasons for modifications to CS methodology
- Inconsistencies arose because stock used all survey data while change used only repeated measurements.
- Three possible consistent approaches examined; modelling approach chosen for consistency and efficiency, applicable to both square and plot data.
- Old methods could produce inconsistent reporting across adjacent vs. non-adjacent survey intervals.
- The modelling approach uses complete data and reduces reliance on distributional assumptions due to bootstrap.

## Modelling basics
- Incomplete data techniques (EM-like approaches) enable consistent estimation by using data from all surveys.
- Mixed effects/repeated measures models separated into fixed effects (stock/change) and random effects (sampling variation).
- Models require distributional assumptions; fixed effects estimators are robust, but variance/covariance parameters are less stable.
- Bootstrapping is used to obtain robust standard errors.

## Square level data
- Data treated as a random sample of squares within each Land Class; repeated measures within squares are modelled.
- Basic model: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects for land class i and survey k, s_ij are square-level random effects, and e_ijk are repeated-measures errors.
- Random effects are typically normally distributed with land-class-specific variances; covariances across surveys are modelled.

## Plot level data
- Plot-level data within squares can be analysed by extending the square-level model with an additional plot-level residual (random effect).
- This allows for correlation of plots within a square and supports bootstrapping across the full data hierarchy.

## Model specification
- General form for square-level data: y_ijk = a_ik + s_ij + e_ijk.
- Distributions: s_ij ~ N(0, τ_i^2) and e_ijk ~ N(0, σ_ik^2) with covariances across surveys.
- For K surveys, there are K fixed effects per Land Class but many random parameters; variance-covariance estimation becomes unstable with many surveys.
- Practical reduction: assume random effects do not vary by land class; and/or assume variances are constant across surveys (AR1 structure for covariances).
- AR1 model (one-step autoregressive) reduces random parameters to a manageable number (three per survey, regardless of the number of surveys).
- Fixed effects are robust to some mis-specification; variance parameters can be bootstrap-estimated for reliability.

## Model testing – Broad Habitats
- Examined Broad Habitat data across 1984, 1990, and 1998 using old and new methods.
- Old approach showed inconsistencies between stock and change; new modelling approach produced consistent estimates.
- Differences between old and new estimates generally fell within the old method’s error bounds; some differences were small in magnitude relative to standard errors.
- Consistency achieved across square-level and plot-level data; adopted new methodology for CS2007.

## Limitations and implications
- Bootstrapped, model-based estimates are computationally demanding, especially for many variables.
- AR1 model provides a practical balance of robustness, speed, and parameter reduction; fixed-effects estimates are robust to some mis-specification.
- Fully parameterised models are slow; a standardized AR1 approach is preferred for large-scale analyses.
- Analyses involve data from all surveys; new information can update past estimates, so past results may shift slightly over time.
- Non-normal data can affect parametric SEs; bootstrap methods help but some variables (e.g., standing water) may converge to local maxima; old methods may be retained for those cases.
- On the original measurement scale, results remain interpretable; transforming data may complicate back-transformation for fixed and random effects.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (bootstrap); Scott (2002) on empirical Fisher information.
- Countryside Survey project materials and related methodological literature.