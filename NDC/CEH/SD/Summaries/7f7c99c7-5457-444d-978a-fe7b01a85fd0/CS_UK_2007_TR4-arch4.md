# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes introduced for the 2007 analysis.
- Old methods used stock estimates from all data and change estimates from repeated measurements, causing inconsistencies between stock and change.
- Modelling with consistent estimation (via mixed effects/repeated measures models) was found feasible, robust, and generally aligned with previous results, while using all available data to increase precision.
- The AR1 (autoregressive) modelling approach reduces the number of random parameters, improving stability and run-time, and is paired with bootstrap methods to obtain robust standard errors.
- Implementing modelling is technically challenging and computationally intensive, especially for large variable sets; automated, standardised models (like AR1 with bootstrap) were favored for CS2007.
- The new approach was tested against Broad Habitat data (and other datasets), showing consistent estimates and improvements in precision; past inconsistencies tended to fall within existing error bounds.
- Adoption of the modelling approach implies that estimates for earlier surveys can be revised as new data are added, which may lead to small updates to past findings.
- Limitations include sensitivity to distributional assumptions, potential non-normality in some variables, and computational demands; in some non-normal cases, old methods or data transformations may be preferable for specific variables (e.g., standing water in freshwater data).

## Background: CS design and data structure
- CS uses a stratified sample of 1 km squares on a 15 km GB grid, with two data levels: square-level measurements and within-square plot-level measurements.
- Land Classification (ITE) defines strata, with country-specific classifications (England, Wales, Scotland) in CS2007.
- Data types range from binary to continuous measurements; stock estimates relate to total land class means, while changes relate to differences over time.

## Why the methodology changed
- Previous reporting showed inconsistencies where stock estimates (using all data) did not align with change estimates (from repeated measurements).
- Missing data across survey pairs (new squares introduced, some squares not recorded in earlier surveys) drove inconsistencies.
- Several approaches for consistency were considered; modelling with consistent estimation offers robust, efficient estimates across both square and plot-level data, albeit with additional assumptions.

## Modelling approach and advantages
- Incomplete data techniques (mixed effects/repeated measures models) are used to achieve consistency by leveraging information across all surveys.
- Fixed effects represent land-class means across surveys; random effects capture square-level and plot-level variation and their correlations across surveys.
- AR1 (autoregressive) models reduce the number of random parameters by assuming:
  - Within-land-class variances are constant across surveys.
  - Repeated-measures covariances follow a first-order autocorrelation (adjacent surveys correlated; distant surveys less so).
- Benefits:
  - Produces consistent and more precise stock and change estimates.
  - Estimates for fixed effects are robust to mis-specification of random effects distributions; bootstrap provides robust standard errors.
- Trade-offs/limitations:
  - Full parameterised models are slow; AR1 offers a practical balance of speed and accuracy.
  - Distributional assumptions for random effects matter, and non-normal data can bias results if not carefully handled.
  - Some very non-normal variables may require alternative handling; in extreme cases, older methods might be used for those variables.

## Square-level data: modelling details
- Treat CS as a repeated-measures design within Land Classes.
- Model structure: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for each survey).
  - s_ij: square-level random effects (vary by land class).
  - e_ijk: repeated-measures residuals (vary by survey and land class, with correlation across surveys).
- Random effects are assumed normal with land-class-specific variances; covariances across surveys are modelled (AR1 reduces parameter count).

## Plot-level data: modelling details
- Plot data within squares can be analysed by extending the square-level model to include plot-level residuals.
- Two approaches:
  - Treat plots within squares as adding a plot-level random effect (with square-level variation retained).
  - Treat plots as independent within land class (less robust if within-square variation differs from between-square variation).
- Both approaches can be integrated within bootstrapping for standard errors.

## Model specification and estimation
- General square-level model equation: y_ijk = a_ik + s_ij + e_ijk
- Random effects:
  - s_ij ~ N(0, τ_i^2) (square-level)
  - e_ijk ~ N(0, σ_ik^2) with covariances across surveys
- To manage complexity, assumptions are made:
  - Variances σ_ik are constant across surveys within land class (σ_i).
  - AR1 covariance structure reduces multiple covariances to a single parameter per land class.
- Estimation uses bootstrap to obtain standard errors, ensuring robustness to distributional mis-specification.

## Model testing: Broad Habitats
- Historical CS uses Broad Habitats with data from 1984, 1990, 1998 (and 1978 data not directly comparable).
- Previous methods produced inconsistencies between stock and change estimates; modelling with AR1 produced consistent estimates with no results outside old-method error bounds.
- Changes between old and new methods were generally small relative to standard errors; in one case (neutral grassland 1990), a change was notable but still within plausible bounds.
- Results from modelling aligned with results from repeated squares and stock-change comparisons, supporting adoption for 2007 and beyond.
- Extended testing to plot-level soil data and confirmed feasibility for consistent estimates across data types.

## Limitations and implications
- Modelling with bootstrap is robust but computationally intensive; automated, standardised modelling is essential for large CS analyses.
- Fixed-effect estimates are relatively robust to random-effects mis-specification; variance/covariance estimates are more sensitive and require careful handling.
- Across many surveys, the model includes many random parameters; AR1 helps, but exact distributions remain a consideration.
- Results for past surveys are updated with new data, meaning estimates can revise historical findings; this is conceptually different from the older inconsistencies but is a natural outcome of using all available information.
- For unusual non-normal data, transform-and-back transformations are possible but can complicate interpretation due to involvement of random effects in back-transformations.

## Practical implications for Data Leaders
- For data strategy, shift toward modelling-based estimation to achieve consistency and improve precision across time.
- Ensure data governance supports hierarchical data structures (square and plot levels), complete metadata, and cross-survey linkages.
- Plan for computational resources and automation to handle AR1-based modelling across large variable sets; bootstrap-based standard errors require substantial processing.
- Maintain documentation on model assumptions, especially distributional choices and AR1 structure, to support interpretation and auditability.
- Be aware that new data can revise past survey estimates; communicate updates as part of an ongoing data lifecycle rather than static figures.
- When presenting results, emphasize the consistency between stock and change estimates, and clearly annotate any limitations due to data non-normality or model assumptions.

## References
- Barr et al., 1993; Haines-Young et al., 2000; Dempster et al., 1977; Efron & Tibshirani, 1993; Scott, 2002.