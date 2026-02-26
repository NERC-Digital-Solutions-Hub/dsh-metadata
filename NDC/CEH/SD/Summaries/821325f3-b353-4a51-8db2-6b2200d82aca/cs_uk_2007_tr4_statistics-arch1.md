# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes introduced for CS in 2007.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling approaches for consistent estimation were explored using Broad Habitat data; results showed modelling could be feasible and robust, with differences from old methods generally within existing inconsistencies.
- CS 2007 adopts consistent estimation via modelling, utilizing all available information to produce more precise estimates. This also means past survey estimates may be revised as new data improve prior estimates.
- Modelling is computationally intensive, requiring iterative fitting and careful handling of CS’s complex sampling. Despite challenges, a more accurate product emerges.
- The approach relies on additional distributional assumptions, so results are validated against previous methodology, especially for small data subsets.
- The new method has been tested on Broad Habitats and soil data, supporting broader adoption for square and plot-level data.

## Introduction
- Summary of sampling and analysis procedures for Countryside Survey data; review of CS2000 methods and description of CS2007 changes.
- CS sampling involves a stratified sample of 1 km squares on a GB-wide 15 km grid, with measurements at two levels: square-wide and within-square plots.
- Land Classification (ITE) used to stratify square selection; classifications expanded from 32 to 42 (CS2000) and to 45 for CS2007, with country-specific classifications (England, Wales, Scotland).

## Estimation and Bootstrapping
- Old method: compute means and standard errors for each Land Class, then combine across classes weighted by land area to obtain regional/national estimates; assumed independence between Land Classes.
- Significance testing: bootstrap (instead of normal-theory SEs) due to concerns about non-normality, particularly for square-level data.
- Bootstrapping provides distribution-free SEs and confidence intervals, accommodating skewness in the data.

## Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock estimates used all survey data while change estimates used only repeated measurements, leading to potential mismatches.
- Several consistency approaches were considered; the report highlights that estimating stock from all data and change from the difference of stock estimates has advantages (consistency, robustness, ease), but may be inefficient if inter-survey covariance is large and is not ideal for plot-level data.
- Modelling approaches were found to offer consistent and efficient estimates for both stock and change, applicable to square and plot data, but require stronger distributional assumptions. The AR1-based modelling approach was selected for practicality and robustness.

## Modelling Basics
- Incomplete data techniques (e.g., EM-like mixed models) allow combining data across surveys; models include fixed effects (stock/change values) and random effects (reflecting sampling structure and repeated measures).
- Mixed-effects models handle missing data by borrowing strength across surveys; fixed effects give stock/change estimates, while random effects describe between-square and within-square variability.
- These models require distributional assumptions; their robustness for fixed effects is generally good, but variance/covariance estimates are more sensitive to misspecification. Bootstrap standard errors help preserve robustness.

## Square Level Data
- Data treated as a random sample of squares within each Land Class; square-level repeated measures are modeled with mixed models.
- Fixed effects model: mean value per Land Class across surveys; random effects capture square-to-square variation and repeated survey correlations.
- Within-square correlations across surveys are allowed; the model accommodates the hierarchical sampling structure.

## Plot Level Data
- Within-squares plots provide additional vegetation and soil measurements; previous analyses treated plots in various ad hoc ways.
- Modelling extends to include plot-level random effects (in addition to square-level effects) to capture within-square plot variation and cross-survey correlations.
- Both square-level and plot-level models can be embedded within bootstrap procedures to obtain robust SEs.

## Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means in survey k)
  - s_ij: square-level random effect for square j in land class i
  - e_ijk: repeated measures error
- Random effects assumed normal with land-class-specific variances; repeated-measure covariances vary by land class and survey pair.
- With K surveys, the full model has many variance/covariance parameters; to maintain practicality, a reduction strategy is used.
- Two scalable reductions:
  - Variances of random effects do not vary by land class (often not realistic, but a simplification).
  - Covariances are described by an AR1 structure, implying a constant within-land-class correlation across successive surveys and diminishing correlation for non-adjacent surveys.
- The AR1 model, combined with bootstrap for standard errors, provides a robust, computable framework (referred to as AR1 with bootstrap).

## Model Testing – Broad Habitats
- Historical Broad Habitat data (1984, 1990, 1998) showed inconsistencies between stock and change under previous methods.
- Applying the AR1 modelling approach eliminated these inconsistencies; stock and change estimates derived from the model were consistent with summed inter-survey changes and with prior estimates within bootstrap uncertainty.
- Comparative analyses between old and new methods showed differences generally within prior discrepancies, with the modelling approach validating feasibility for Broad Habitats, soil, and plot-level data.
- Based on these results, CS2007 adopted the new modelling methodology.

## Limitations and Implications
- Computationally intensive; AR1 with bootstrap works well but slower than previous methods.
- Fixed-effect estimates (stock/change) are robust to model variation; variance/covariance parameters require careful specification.
- Non-normal data can affect estimation; transformations are possible but complicate back-transformation on the original measurement scale.
- Some variables with highly non-normal distributions (e.g., standing water in freshwater data) may not converge well under the new method; in such cases, the older method may be preferred for reporting.
- The modelling approach uses information from all surveys, so estimates for any given survey can be updated as new data arrive; this means past survey estimates may be revised slightly when new information becomes available.
- Overall, the modelling approach yields more efficient, consistent estimates and a unified framework across square and plot data, at the cost of greater computational demand and the need for explicit distributional assumptions.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron and Tibshirani (1993); Scott (2002).

## Notes
- The CS2007 analysis was implemented with a considerable emphasis on validation against the prior methodology to ensure results remained credible.
- The project highlights the balance between statistical rigor (consistency, precision) and practical constraints (data complexity, computation time).