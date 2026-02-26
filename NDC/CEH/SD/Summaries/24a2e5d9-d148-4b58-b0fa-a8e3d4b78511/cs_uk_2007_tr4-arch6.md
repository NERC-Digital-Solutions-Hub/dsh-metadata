# Countryside Survey in 2007: Consistent Estimation

## Executive Summary
- The report describes the statistical methodology used for Countryside Survey (CS) data analysis and details changes implemented for CS 2007 to improve consistency between stock and change estimates.
- Previous methods used minimal assumptions and produced robust but inconsistent stock vs. change estimates (stock used all survey data; change used only repeated measurements).
- Modelling with consistent estimation (via mixed effects/repeated measures and AR1 structure) is feasible and generally robust; differences from old methods are typically within existing inconsistencies.
- The new modelling approach uses all available information, yielding more precise estimates; estimates for past surveys can be updated as new data become available, though changes are usually small.
- Implementing modelling is computationally more demanding and requires careful checks, especially for small data subsets; AR1 with bootstrap was chosen for practicality and robustness.
- The approach was tested on Broad Habitats and other data (including plot-level data) and supported adopting the new method for CS 2007.

## Why Methodology Was Modified
- Point estimates (stock) and interval estimates (stock/change) were historically inconsistent due to differing data sources for stock and change.
- Missing data (e.g., unrepeated plots/squares) contributed to discrepancies between stock and change estimates.
- The shift from emphasising adjacent-survey changes to spanning from the first survey to the present highlighted these inconsistencies and motivated a consistent estimation framework.

## Modelling Approach for Consistent Estimation
- Use modelling to estimate both stock and change consistently across surveys, applicable to square and plot-level data.
- Mixed effects/repeated measures models incorporate fixed effects (land class means per survey) and random effects (squares, plots, and their correlations over time).
- Aim to reduce the number of random parameters to keep models tractable, adopting AR1 (first-order autoregressive) structure to capture survey-to-survey correlations with a small, stable parameter set.

## Data Structure and Levels
- Square-level data: complete 1 km squares within Land Classes; repeated measures across surveys; model treats squares as random effects with within-square correlations over time.
- Plot-level data: within-square plots; hierarchical structure considered to avoid biased standard errors; models extended to include plot-level random effects when needed.
- Land Classification: evolving national classifications (GB: 32 → 42 → 45 classes) with country-specific sub-classifications (England, Wales, Scotland).

## Model Specification (Key Formulation)
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square-level random effect for square j in land class i
  - e_ijk: repeated-measures error
- Random effects assumed normally distributed with land-class-specific variances; Covariances modeled to reflect time correlations.
- AR1 reduction: assume common within-land-class variance across surveys and first-order autocorrelation of repeated measures to drastically reduce parameters.

## Model Testing and Application
- Broad Habitats: old method yielded inconsistencies between stock and change; new AR1 modelling with bootstrap produced consistent estimates where changes equaled stock differences over survey intervals.
- Comparison with old methods showed most estimates stayed within old error bounds; differences were typically small and often within existing inconsistencies.
- Additional testing on soil data (1984, 1990, 1998) and plot data supported feasibility and consistency of the approach.

## Practical Considerations and Limitations
- Computation: AR1 modelling with bootstrapping is more time-consuming; fully parameterized models are slow, so standardized automated models are preferred for large-scale use.
- Model choice: fixed effects robust to some mis-specification of random effects; variance/covariance parameters require careful handling; bootstrap standard errors enhance robustness.
- Non-normal data: some variables (e.g., standing water) exhibited non-normal distributions; in some cases, old methods were retained when new methods converged to problematic local maxima.
- Updating past surveys: incorporating all surveys means past estimates may be revised with new data; this reflects new information rather than correcting past errors.

## Implications for Data Support and Use
- More precise, consistent stock and change estimates across the CS time series.
- Improved use of all available data and proper representation of data hierarchy enhances reliability of results and supports better communication of trends.
- Automated, standardized modelling approach facilitates scalable analysis across many variables, with checks comparing new and old methods to ensure results remain within reasonable bounds.
- Outputs are dependent on model structure and distributions; robust bootstrap procedures mitigate some distributional concerns.

## Notes on Data and Accessibility
- The methodology supports both square and plot-level data, enabling consistent cross-scale reporting.
- Results for 2007 reflect adoption of the modelling approach, with historical data re-analyzed where feasible to ensure comparability.