# Countryside Survey 2007: Consistent Estimation

- Purpose: Describe and justify the statistical methodology used to analyse Countryside Survey (CS) data for 2007, adopting a modelling approach that yields consistent estimates of stock and change across surveys and utilizes all available information.

## Why changes were made

- Previous methods calculated stock using all data from a survey but change from only repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling demonstrated that consistent estimation is feasible and robust for CS Broad Habitat data, with results typically close to those from the old methods but with improved precision.
- 2007 reporting shifts to timelines spanning from the first survey to the present, necessitating consistency across multiple surveys.
- Modelling offers more efficient use of data and better handling of missing information, though it requires additional distributional assumptions and greater computational effort.

## Modelling approach and key concepts

- Goal: Achieve consistent estimates of stock and change for both square-level and plot-level data by jointly modelling data from all surveys.
- Core idea: Use mixed effects and/or repeated measures models to account for the hierarchical CS sampling structure and missing data patterns.
- Fixed effects: Represent land-class means across successive surveys; provide estimated stock values when scaled by land-class area.
- Random effects: Capture square-level variation (and plot-level variation for plots within squares) and their correlations across surveys.
- Consistency: Estimates of stock and change are derived from the same model, ensuring consistency across time and data types.

## Data structure and levels

- Square-level data: Based on a stratified sample of 1 km squares; each square yields measurements across surveys, with some missing data due to non-surveyed squares or newly added squares.
- Plot-level data: Within each square, multiple plots yield additional measurements; modelling can incorporate plot-level residuals to reflect within-square variation.
- Land Classes: Sampling is stratified by Land Class, with class-specific parameters and area-based weighting when aggregating to regional or national estimates.

## Model specification and estimation

- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Distributional assumptions: Random and residual effects are typically normal, with variances and covariances that may vary by land class and survey.
- Parameter reduction (AR1 model): To keep the model tractable with many surveys and land classes, assume:
  - Constant within-land-class variance across surveys
  - Autoregressive (order 1) structure for covariances (covariances depend on adjacent surveys)
  - Results in a small, stable set of random-effect parameters (three per land class per survey)
- Bootstrap: Standard errors and significance testing are obtained via bootstrapping instead of relying on strict normality, improving robustness to non-normal data.

## Outputs, consistency, and reporting

- Consistency: Stock and change estimates are derived from the same modelling framework, so they are inherently consistent with each other.
- Updates with new data: Because the method uses information from all surveys, estimates for earlier surveys may be revised as new data become available, reflecting new information.
- Validation: Comparisons with old methods show that differences are generally small and within old inconsistencies, with significant improvements in precision.

## Testing and evidence (Broad Habitats)

- Analyses on 1984, 1990, and 1998 Broad Habitat data showed that:
  - Old method inconsistencies (stock vs. change) are eliminated under the modelling approach.
  - Differences between old and new estimates are typically small and within the previous method’s error bounds.
- Similar modelling applied to plot-level data (soil and other measurements) confirmed feasibility and consistency, supporting adoption for 2007.

## Implementation challenges and practical considerations

- Computational intensity: AR1 modelling with bootstrapping requires more computer time than the older method, but is feasible for large CS datasets.
- Model selection: A standard, automated approach (the AR1 model with bootstrap) is favored for large-scale analyses to ensure robustness and efficiency.
- Limitations: Strong distributional assumptions can affect variance estimates; non-normal data may lead to convergence issues in some cases (e.g., freshwater standing water), where older methods may be preferred for that variable.
- Reporting implications: Because estimates are updated with new data, historical results may shift slightly, which is conceptually different from the previous, inconsistent reporting.

## Implications for data use and data products

- Benefits for data support:
  - More precise, consistent stock and change estimates across long time series.
  - Full use of data hierarchy (square and plot levels) and all available information.
  - Ability to provide self-serve data products (e.g., model-based estimates, uncertainty) with transparent uncertainty via bootstrapped intervals.
- Considerations for dissemination:
  - Communicate that earlier survey estimates may be revised as new surveys are included.
  - Emphasize the modelling assumptions and their potential impact on certain non-normal variables.

## Summary takeaway

- The CS2007 analysis adopts a mixed-effects modelling approach (AR1) with bootstrapped uncertainty to produce consistent, more precise estimates of stock and change across surveys, leveraging all available data and the hierarchical CS sampling structure, while acknowledging increased computational demands and distributional assumptions.