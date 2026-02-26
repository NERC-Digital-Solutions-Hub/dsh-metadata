# Statistical methodology used for the analysis of Countryside Survey data

## Executive summary
- The report describes the statistical methodology for Countryside Survey (CS) data analysis, summarising previous methods and detailing changes implemented for CS 2007.
- Previous estimation used all data for stock and only repeated measurements for change, causing inconsistencies between stock and change estimates. Modelling-based, consistent estimation was shown to be feasible and robust, producing more precise results by utilizing all available information.
- The 2007 shift adopts a modelling approach (mixed effects/repeated measures) to obtain consistent and efficient stock and change estimates, with careful validation against the old method.
- While the modelling approach is more computationally demanding and requires distributional assumptions, it can be implemented with bootstrap-based standard errors to remain robust, especially for small samples.
- The change to modelling was also applied to Broad Habitats and confirmed feasible for plot- and square-level data, reinforcing a unified, consistent analysis framework across data types.
- Overall, the new methodology improves precision and uses data more fully, but estimates for a given survey may be revised as new data from later surveys become available.

## Context and purpose
- This technical report outlines sampling and analysis procedures for CS data, comparing the old methodology with the new modelling approach adopted for CS 2007.
- The aim is to provide consistent stock and change estimates across surveys and to utilise all available information within the hierarchical CS data structure.

## Data structure and sampling
- Data come from a stratified sample of 1 km squares on a GB-wide 15 km grid. Each square is mapped and has measurements at two levels: square-wide (whole square) and within-square plots.
- Land Classification (ITE) defines strata; CS2007 uses 45 land classes (19+ classes per country) with separate national classifications.
- Measurements include binary and continuous variables (e.g., areas, lengths).

## Estimation: old vs new approaches
- Old approach: means and standard errors by Land Class, then combine to regional/national estimates using area-based weights. Stock used all data from a survey; change used only repeat measurements, leading to inconsistencies between stock and change.
- New approach: modelling-based, aiming for consistency and efficiency by estimating stock and change jointly from all data via a hierarchical model; later surveys can revise earlier estimates as more information becomes available.

## Modelling basics and rationale
- Consistent estimation via modelling requires assumptions about data distributions; models must handle incomplete data and the CS sampling hierarchy.
- Mixed effects/repeated measures models are used, with fixed effects representing land-class means across surveys and random effects capturing square- and plot-level variability and correlations across surveys.
- The fixed-effect parameters provide stock estimates; differences between fixed effects across surveys yield change estimates.

## Square level data modelling
- For complete 1 km squares, data are treated as a random sample within each land class across surveys.
- A two-part model: fixed effects (mean values by Land Class over time) plus random effects (square-level deviations and repeated-measures errors).
- Random effects include square-level variability and covariances of repeated measures across surveys, allowing correlation between surveys within the same square.

## Plot level data modelling
- Plot-level data within squares can be incorporated by extending the model to include a plot-level residual (random effect) in addition to the square-level effect.
- This provides a more complete use of plot data and can be embedded within bootstrapping for robust standard errors.

## Model specification and parameter considerations
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means in survey k)
  - s_ij: square random effect
  - e_ijk: repeated-measures residual
- Random effects are normally distributed with land-class-specific variances; repeated-measures covariances vary by land class and survey pair.
- With K surveys, the full model has many random parameters; thus, to keep models stable and computable, reductions are made.

## Reducing model complexity: AR1 approach
- Assumptions to simplify random effects:
  - Variance parameters do not vary across surveys (common σ_i for each land class).
  - Autoregressive AR1 structure for covariances (covariances between successive surveys are constant; non-adjacent surveys are conditionally independent given intervening surveys).
- This AR1 reduction yields a manageable number of random parameters (three per land class per survey), enabling practical fitting across many surveys and variables.

## Bootstrap for standard errors
- Because random effects variances/covariances are difficult to estimate precisely, bootstrap is used to obtain standard errors and confidence intervals for fixed effects, providing robustness to distributional mis-specification.

## Model testing: Broad Habitats
- Historical CS output included Broad Habitat stocks and changes across 1984, 1990, and 1998.
- Comparisons of old and new methods showed inconsistencies in stock vs. change estimates under the old method, which the modelling approach resolved.
- The AR1 model with bootstrap produced estimates consistent with earlier results within their usual uncertainty bounds, and most changes remained well within prior error margins.

## Limitations and practical implications
- Computational demands are high; fully parameterised models are slow, so AR1 with bootstrap provides a practical balance.
- Fixed-effect estimates are robust to some distributional mis-specifications, but variance/covariance estimates are sensitive; bootstrap mitigates this.
- Some variables (e.g., very non-normal freshwater standing water) may cause convergence to local maxima with the new method; in such cases, the old method’s estimates may be retained.
- Estimates for any given survey may be updated as new data from future surveys are incorporated; this differs from the previous practice of fixed estimates per reporting occasion.
- Adoption of consistent estimation improves precision and coherence across the dataset, enabling more reliable cross-survey comparisons and better use of hierarchical data structure.

## Implementation and impact
- The AR1 modelling approach was selected for CS2007 due to stability, speed, and robustness of fixed-effect estimates, making it suitable for automated, large-scale analyses.
- The analysis framework is designed to be applied automatically to a large number of variables, with checks comparing results from the old and new methods to ensure plausibility.
- The methodological shift supports using all available information, improves precision, and aligns analyses across square and plot-level data and across habitat types.