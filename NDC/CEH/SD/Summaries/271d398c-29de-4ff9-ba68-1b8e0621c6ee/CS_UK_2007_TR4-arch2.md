# Countryside Survey 2007: Description of Statistical Methodology

## Executive Summary
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data, summarizing previous methods and detailing changes implemented for CS in 2007.
- Previous approaches used stock estimates from all data and change estimates from repeated measurements, which could yield inconsistencies between stock and change.
- Modelling-based, consistent estimation was found feasible and robust for Broad Habitat data, and was adopted for CS2007, improving precision by utilizing all available information and the data hierarchy.
- The modelling approach provides more precise estimates but requires additional distributional assumptions and more computer time; care is taken to validate results, especially for small data subsets.
- Unlike previous methods, the new approach updates past survey estimates as new data become available, meaning estimates are not strictly fixed across reporting occasions.
- For CS2007, the AR1 modelling approach with bootstrap standard errors was chosen for square-level data due to its balance of robustness, efficiency, and practicality; it was also tested against older methods to ensure comparability.
- The methodology was extended to plot-level data, though complexities required careful handling, and adjustments were made to ensure bootstrapped standard errors remain robust.
- A specific note: for freshwater standing water, non-normal distributions caused convergence to a local maximum with the new method, so estimates for that variable remained from the old methodology.
- Overall, the new modelling approach is more efficient and consistent, though it demands greater computational resources and careful model choice; the results are intended to be more reliable and comparable across surveys.

## Introduction
- This technical report overviews CS sampling and analysis procedures, reviews the previous CS statistical methodology, and explains the changes applied to CS in 2007, including limitations and implications.

## Sampling
- CS Field Survey uses a stratified sample of 1 km squares at a 15 km GB grid intersection.
- Two levels of sampling: square level (the whole square) and within-square plots/quadrats (plot level).
- Measurements cover a range of data types from binary to continuous.
- Land Classification (ITE) stratifies sampling; England, Wales, and Scotland now have country-specific classifications (45 classes in total: 21 England, 8 Wales, 16 Scotland).

## Estimation
- The traditional approach estimated regional/national means and standard errors for each Land Class and then combined them by weighting by land-area.
- This method made minimal distributional assumptions and assumed independence between Land Classes.

## Bootstrapping
- Significance testing uses bootstrap rather than assuming normality, addressing skewness in some features and non-normal data distributions (typical for square-level data).

## Reasons for Modifications to CS Methodology
- Past reports showed inconsistencies where stock estimates (all data) did not match change estimates (repeat measurements only).
- Inconsistencies arise because different data subsets are used to estimate stock vs. change across survey pairs.
- Several approaches to achieve consistency were considered; modelling (consistent estimation) was chosen for CS2007 due to robustness and efficiency, applicable to both square and plot data.

## Modelling Basics
- Incomplete data techniques (mixed effects/repeated measures) are used to achieve consistency across surveys, requiring distributional assumptions.
- Fixed effects represent stock and change; random effects capture sampling variation (squares, plots) and their correlations across surveys.
- A major challenge is the large number of random parameters; practical reduction strategies are used to keep models tractable.

## Square Level Data
- Square-level data are treated as repeated measures within Land Classes; a mixed-effects model with fixed effects for Land Class means across surveys and random square-level effects is used.
- The random effects account for square-to-square variation and within-square survey deviations, with correlations across surveys allowed.

## Plot Level Data
- Plot-level data within squares can be analyzed by extending the square-level model to include an additional plot-level residual/random effect.
- Both square-level and plot-level analyses can be embedded within bootstrapping procedures.

## Model Specification
- General form for square-level data: y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means by survey), square random effects s_ij, and repeated-measures residuals e_ijk.
- Random effects are assumed to be normally distributed, with variances and covariances that can vary by land class and survey.
- To keep models practical, several parameter-reduction strategies are used:
  - Assume random effect variability is constant across surveys (σ_i).
  - Use an autoregressive AR1 structure for covariances, reducing repeated-measures parameters to a small number.
- Bootstrap methods are used to obtain robust standard errors, especially important when variance-covariance parameters are difficult to estimate precisely.

## Model Testing – Broad Habitats
- Broad Habitat data (stock and change across 1984, 1990, 1998, etc.) were reanalyzed with modelling to assess consistency.
- Old methods showed inconsistencies between stock-derived and repeat-square-derived change estimates; modelling produced consistent estimates without these discrepancies.
- Comparisons between old and new methods showed changes typically within the old method’s error bounds; in most cases, differences were not statistically meaningful.
- The analyses supported adopting the modelling approach for the 2007 CS data and extending consistency checks to soil and plot-level data as well.

## Limitations and Implications
- Implementing model-based analysis with bootstrap is computationally demanding, but fixed-effects estimates are robust to model variation.
- The AR1 model reduces parameter count and is practical for large numbers of analyses; results are robust to moderate distributional mis-specifications.
- Some variables with very non-normal distributions (e.g., freshwater standing water) may not suit the modelling approach, potentially requiring the old method for those variables.
- Because analyses use data from all surveys, estimates for a given survey can be revised as new data become available; cross-reporting consistency across all reporting occasions may not be maintained in the same way as before.
- Overall, the approach leverages complete data structures, improving precision and consistency, while requiring automated, standardized model application for many variables.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (Bootstrap); Scott (2002).