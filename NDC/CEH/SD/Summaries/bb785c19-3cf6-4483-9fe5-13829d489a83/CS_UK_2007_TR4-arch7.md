# Countryside Survey 2007: Statistical Methodology

## Executive overview
- Describes the statistical methodology used to analyze Countryside Survey (CS) data.
- Highlights changes from previous CS methodology to achieve consistent estimates of stock and change.
- Moves to a modelling approach (mixed effects/repeated measures with AR1 structure) to utilize all data and produce more precise estimates.
- Uses bootstrap to obtain robust standard errors and confidence intervals, accommodating non-normal data distributions.
- Notes increased computational effort and the need for automated, scalable modelling across many variables.
- Emphasises that new estimates are informed by all surveys, so past estimates may be updated with new information.

## Introduction
- This technical report explains sampling and analysis procedures for CS data.
- Reviews the previous CS methodology and documents the rationale and details of changes for CS2007.
- Aims to present a consistent, efficient estimation framework applicable to square and plot level data while acknowledging limitations.

## Overview of previous CS methodology
- CS field data come from a stratified sample of 1 km squares using a two-level sampling (square-level measurements and within-square plot measurements).
- Data are distributed across Land Classes; England, Wales, and Scotland each have country-specific classifications.
- Old estimation approach: stock estimates used all data from a survey; change estimates used only repeated measurements, causing potential inconsistencies between stock and change.
- Significance testing relied on normal approximations prior to CS2000; bootstrap was introduced to handle non-normality.

## Reasons for modifications to CS methodology
- Inconsistencies arose because stock and change were derived from different data subsets.
- Missing information (e.g., unrepeated squares) inflated discrepancies between stock and change estimates.
- Several approaches could yield consistent estimates; modelling (consistent estimation) emerged as feasible and robust, applicable to both square and plot data.
- Modelling allows using all available data and provides more precise estimates, but requires stronger distributional assumptions.

## Consistent estimation (modelling approach)
- Modelling uses mixed effects and/or repeated measures to handle incomplete data and to produce consistent stock and change estimates.
- Requires specifying fixed effects (stock/change means per Land Class per survey) and random effects (variability at square/plot level and across surveys).
- Trade-off: more assumptions and parameters, but greater efficiency and consistency; bootstrap can mitigate risks in estimating standard errors.

### Square level data
- Treats each Land Class as a random sample of squares; uses repeated-measures mixed models.
- Fixed effects: stock means per Land Class across surveys.
- Random effects: square-level deviations and within-square survey deviations, with correlations across surveys.

### Plot level data
- Includes within-square plots (e.g., vegetation/soil measurements) to better exploit hierarchical data.
- Previous analyses treated plots separately or aggregated to square level; modern approach uses a hierarchical mixed model that accounts for square and plot-level variation.
- Bootstrapping can be applied to both square and plot-level models.

### Model specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class i, survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures (within-square/within-survey) residuals
- Random effects assumed normally distributed with class- and survey-specific variances; covariances across surveys modelled (often AR1 to limit parameters).
- Reducing random parameter count is essential for stability and computational feasibility; common (per Land Class) variance and AR1 covariance structures are used.
- AR1 (autoregressive) structure reduces random parameters to a manageable number while preserving essential correlations between successive surveys.
- Bootstrap is used for standard errors, since parametric SEs can be biased under complex random-effects structures.

### Model testing – Broad Habitats
- Re-analysis of Broad Habitat data (1984, 1990, 1998) shows inconsistencies in old methods when comparing stock versus change.
- Modelling with AR1 and consistent estimation yields results that align with the new method’s framework; differences from old methods are generally within existing uncertainties.
- Additional analyses extended to soil and plot data; consistent, model-based estimates were feasible beyond square-level data.

## Limitations and implications
- AR1 modelling with bootstrapped SEs is robust for fixed effects but more delicate for variance/covariance parameters.
- Fully parameterised models can be very slow; AR1 provides a good balance of speed and stability.
- Model choice is important; automated, scalable implementation is preferred for large numbers of variables.
- Results for any one survey are influenced by information from all surveys; estimates can be updated with new data, which is conceptually different from the previous, fixed reporting timeline.
- Non-normal data may affect some distributions; transformations are not preferred due to back-transformation complications on the original measurement scale.
- In some cases (e.g., very non-normal freshwater standing water data), old methods may remain preferred due to convergence or stability concerns.
- Overall, modelling approach increases efficiency and precision, enabling more informative map-based data products, but requires careful interpretation of updated past estimates in light of new data.

## References
- Barr et al. (1993), CS1990 Main Report
- Dempster, Laird, Rubin (1977), EM algorithm
- Efron, Tibshirani (1993), Bootstrap
- Haines-Young et al. (2000), Accounting for nature: assessing habitats in the UK countryside
- Scott (2002), Maximum likelihood estimation with empirical Fisher information
- Additional CS methodological references linked to AR1 and mixed models