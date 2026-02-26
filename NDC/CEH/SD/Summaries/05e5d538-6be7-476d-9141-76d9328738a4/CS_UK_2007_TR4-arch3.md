Countryside Survey in 2007: Statistical Methodology for Consistent Estimation

## Executive summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data, focusing on changes implemented for CS in 2007 to achieve consistency between stock and change estimates.
- Previous methods used all data for stock and repeated measurements for change, creating inconsistencies between stock and change estimates.
- Modelling-based consistent estimation (using mixed effects/repeated measures models with an AR1 structure) was found to be feasible, robust, and more precise, though it requires more computational time and additional assumptions.
- The AR1 modelling approach, combined with bootstrapped standard errors, provides stable estimates across surveys and makes full use of hierarchical CS data (square and plot levels) and land classifications.
- Comparisons with the old methodology show that differences are generally small and fall within the previous level of inconsistency; improvements in precision are achieved by leveraging information from all surveys.
- Practical implementation notes: modelling is computationally intensive, requires automated standardised procedures, and entails updating previous survey estimates as new data become available.

## Introduction
- The document provides an overview of CS sampling and analysis procedures, reviews the previous CS methodology, and details the rationale and specifics of the 2007 methodological changes.
- Fuller descriptions of prior sampling and estimation are available in earlier CS reports.

## Sampling
- Data come from a stratified sample of 1 km squares within a 15 km GB grid; measurements occur at two levels: square-wide and within-square plots.
- Land Classification (ITE) is used for strata; classifications have evolved (32 → 42 → 45 classes) with country-specific reporting (England, Wales, Scotland).

## Estimation
- The traditional approach computed means and standard errors for each Land Class and then combined them (weighted by land area) to produce regional/national estimates.
- This method makes minimal distributional assumptions and assumes independence of land classes, but can yield inconsistencies between stock and change due to using different data subsets.

## Bootstrapping
- Because some CS data are skewed, normality assumptions for significance testing are questioned.
- Bootstrapping (typically 1000–10,000 resamples) is used to obtain standard errors and confidence intervals that accommodate non-normal data distributions.

## Reasons for Modifications to CS Methodology
- Past results revealed inconsistencies: stock estimates used all data from a survey while change estimates used only repeated measurements.
- The goal was to produce consistent estimates across adjacent and non-adjacent survey periods and to better reflect information from all surveys.
- Three potential approaches were considered; modelling (consistent estimation via a single model across surveys) was chosen for its robustness and efficiency, despite requiring stronger distributional assumptions.

## Modelling basics
- Incomplete data techniques are employed to achieve consistency; this necessitates assumptions about data distributions.
- Mixed effects/repeated measures models (with fixed effects for stock/change and random effects for hierarchical sampling) are used to handle missing data and data structure.
- The AR1 (autoregressive order 1) structure is adopted to reduce the number of random parameters while maintaining reasonable modeling of correlations between surveys.
- Bootstrap is recommended for standard errors due to potential mis-specification of random effect distributions.

## Square level data
- Square-level data are modeled as a repeated-measures (mixed) model with Land Class as fixed effects across surveys.
- Random effects capture square-level deviations and the correlation of measurements across surveys within the same square.
- This framework ensures stock estimates per survey and derived change estimates are internally consistent.

## Plot level data
- Plot-level measurements within squares are more complex; previous analyses treated plots separately or aggregated to square level.
- The modelling approach extends to plot-level data by incorporating plot-level residuals in addition to square-level random effects, all within a bootstrapped framework.

## Model specification
- General model form for square-level data: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land class means per survey), square random effects s_ij, and repeated-measures errors e_ijk.
- Random effects are assumed normal with land-class-specific variances; covariances across surveys are modeled, typically with a parsimonious structure (e.g., AR1) to keep parameter counts manageable.
- Reducing the number of random parameters is essential for stability and feasibility; common variance across surveys and AR1 covariance structures are used.
- While fixed-effects estimates are robust to some mis-specification, variance/covariance estimates are more sensitive; bootstrap helps protect inference.

## Model testing – Broad Habitats
- Historically, Broad Habitat estimates showed discrepancies between stock and change under old methods.
- Modelling with an AR1 structure eliminated these discrepancies; results across 1984–1998 were coherent and within previous inconsistency bounds.
- Analyses of soil and plot-level data corroborate the feasibility of consistent estimation beyond square-level data.
- Consequently, CS adopted the modelling approach for the 2007 data.

## Limitations and implications
- AR1 modelling with bootstrap is robust but computationally demanding; large variable sets may require automation and standardization.
- Fixed-effect estimates are generally robust to the exact distributional form, but variance/covariance estimates are more sensitive; bootstrap mitigates this.
- Some non-normal data (e.g., standing water) can cause convergence issues; in such cases, older methods may be retained for that variable.
- The modelling approach uses information from all surveys, so estimates for any given survey can be updated as new data arrive; this means results are not strictly fixed across reporting occasions but reflect updated information.
- Overall, the approach is more efficient and uses hierarchical data more fully, yielding more precise estimates, with transparent handling of missing data and data structure.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).