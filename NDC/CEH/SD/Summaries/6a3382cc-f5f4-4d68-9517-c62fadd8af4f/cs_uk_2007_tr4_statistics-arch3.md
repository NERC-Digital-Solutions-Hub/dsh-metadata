Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis, summarising previous methods and detailing changes implemented for CS 2007.
- Previous approach: stock estimates used all data from a survey, while change estimates used only repeated measurements; this created inconsistencies between stock and change.
- Modelling approaches for consistent estimation were investigated and found feasible and robust; differences from old methods were generally small compared with the pre-existing inconsistencies.
- CS 2007 adopts modelling methods to achieve consistent, efficient estimates of both stock and change.
- Modelling requires additional distributional assumptions; results were validated against the old method, particularly for small data subsets.
- Advantages: uses all available information, produces more precise estimates, and yields potential small revisions to past estimates as new data are incorporated.
- Implementation is technically demanding (more computer time due to iterative modelling); overcoming sampling complexities has produced a substantially improved product.

## Introduction and Context
- The report outlines sampling and analysis procedures for CS data, reviewing the previous CS methodology and describing changes for CS 2007, with implications and limitations.
- Full methodological background on CS sampling and estimation is documented in earlier publications (e.g., Barr et al., 1993).

## Sampling and Data Structure
- CS Field Survey uses a stratified sample of 1 km squares across GB on a 15 km grid; two sampling levels within each square:
  - Square-level measurements (covering the whole square, e.g., land cover categories).
  - Plot-level measurements within squares (e.g., vegetation, soils) for detailed features.
- Strata are defined by the ITE Land Classification, with country-specific classifications (England, Wales, Scotland) due to reporting requirements; classification counts vary by country.
- Data types range from binary to continuous measurements.

## Estimation and Inference
- Old method: estimate means and standard errors for Land Classes, then weight by land area to obtain regional/national estimates; assumes independence across Land Classes.
- Uncertainty assessment previously relied on standard errors; significance testing often assumed normality.

## Bootstrapping for Non-Normal Data
- Because some features are skewed, CS 2000 onwards used bootstrapping to obtain standard errors and confidence intervals, avoiding strict normality assumptions.

## Reasons for Methodological Modifications
- Inconsistencies between stock (all squares) and change (repeat squares) estimates led to misalignment; results could appear contradictory when comparing adjacent vs. non-adjacent survey periods.
- The need for estimates that are consistent across time horizons and more informative than pairwise comparisons motivated modelling approaches that use data from all surveys jointly.
- Several potential approaches were considered; modelling (mixed effects/repeated measures) was chosen for its consistency and efficiency, despite requiring more assumptions.

## Modelling Approach: Basics
- Incomplete data techniques (e.g., EM/modern mixed models) enable consistent estimation by leveraging information from all surveys, but require distributional assumptions.
- Mixed models separate fixed effects (stock/change values) from random effects (sampling/within-square variation and correlations across surveys).
- The approach aims to produce stock and change estimates that are internally consistent, leveraging correlations across time and space.

## Square Level Data Modelling
- Treats complete 1 km squares as the observational unit within each Land Class; uses repeated measures/mixed models.
- Fixed effects: land class means across surveys (year as categorical variable).
- Random effects: square-level deviations (random effects) and within-square, across-survey residuals (repeated measures effects) with correlation structures across surveys.

## Plot Level Data Modelling
- Plot-level data within squares can be modelled with an extension that includes a plot-level residual (random effect) in addition to the square-level random effect.
- Allows for hierarchical modelling that accounts for both square and plot-level variation; both square-only and plot-inclusive models can be bootstrapped.

## Model Specification and Practical Considerations
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class means per survey)
  - s_ij: square-level random effect
  - e_ijk: repeated measures residual
- Random effects assumed normal with land-class-specific variances; repeated-measures residuals have covariances that vary by land class and survey pair.
- With K surveys, many random parameters arise; to keep models tractable, two simplifications are emphasized:
  - Common variance across surveys for each land class (σ_i)
  - Autoregressive one (AR1) structure for repeated measures covariances, reducing parameters to a manageable level
- AR1 plus bootstrap is advocated to obtain robust standard errors, given potential mis-specification of variance-covariance structures.

## Model Testing: Broad Habitats
- Historical CS Broad Habitats (1984, 1990, 1998) were re-evaluated using modelling to test consistency.
- Found that stock-change inconsistencies from old methods were resolved under the new modelling approach; changes estimated from stock differences matched those from repeated squares within the model framework.
- Comparisons showed that differences between old and new estimates were generally within the previous inconsistencies, with most changes small.
- Validation extended to soil data (1978 vs. 1998) and plot-level data, confirming feasibility of consistent estimation beyond square-level data.
- Result: adoption of the modelling approach is supported for 2007 CS analyses.

## Limitations and Implications
- Implementing model-based analysis with bootstrapping is computationally intensive; large numbers of variables pose practical constraints.
- Fixed-effect estimates (stock/change) are robust to some model misspecifications, but variance/covariance parameters are more sensitive; bootstrap helps preserve robustness.
- Non-normal data can cause convergence issues (e.g., very non-normal standing water data), where old methods may be preferred for those variables; nonetheless, the AR1 bootstrap approach is favored for overall consistency.
- Despite increased complexity, modelling better utilizes data and respects data hierarchy, improving precision and enabling more coherent policy-relevant indicators.
- Adoption means past estimates may be revised as new survey data become available, which is a logical consequence of integrating information across all surveys; updating past results is considered acceptable given the improved methodology.

## References and Acknowledgments
- Communities and reports cited: Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (bootstrap); foundational works on Countryside Survey methodology and habitat accounting.
- CS2007 analyses are implemented with AR1 modelling and bootstrap for standard errors; ongoing validation and automated application across variables are emphasized.

Note: The CS2007 methodology was developed by the Countryside Survey team at the Centre for Ecology and Hydrology (NERC) with Defra support and aims to provide robust, policy-relevant environmental health indicators through consistent, data-driven estimation across surveys.