# Statistical methodology for Countryside Survey data

- Purpose: Describe the statistical methodology used to analyse Countryside Survey (CS) data, summarise previous approaches, and detail changes implemented for CS in 2007 to achieve consistent estimates of stock and change over time.
- Context: CS involves a two-level sampling framework (1 km squares and plots within squares) across GB, with land classifications and varied measurement types. Prior methods grouped stock and change using different data subsets, causing inconsistencies between stock estimates and reported change.

## Key data and sampling features

- Two-level design: 1 km square sampling within a 15 km grid; within-square plots and quadrats for additional data (vegetation, soils, etc.).
- Stratification: Land Classification as the basis for weighting; country-specific classifications (England, Wales, Scotland) with related classes.
- Data types: Mix of binary and continuous measurements; both square-level and plot-level data are collected.
- Missing data: New squares added over time; some squares/plots are not measured in all surveys, creating incomplete data across survey pairs.

## Estimation: past vs. new approach

- Old approach: Stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs. This produced inconsistencies between stock and change estimates.
- New approach (CS2007): Modelling to jointly estimate stock and change, producing consistent and more efficient estimates by leveraging data from all surveys and the data hierarchy.
- Rationale: Modelling can handle missing information more coherently and utilize correlations across surveys to improve precision, though it introduces distributional assumptions.

## Modelling basics and approach

- Incomplete data:  Missing data techniques (EM-type mixed models) are used to produce consistent stock and change estimates without simply imputing values.
- Data structure: Mixed/replicated models with fixed effects (land-class means across surveys) and random effects (square and plot-level variation) to reflect the sampling design.
- Square-level data: Repeated measures/mixed models with fixed effects for land-class means by survey; random effects capture square-to-square and within-square correlations across surveys.
- Plot-level data: Extends the square-level model by adding plot-level residuals; bootstrapping can be used to obtain standard errors that reflect the data hierarchy.

## Model specification and parameter reduction

- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Distribution: Random effects (s_ij) and residuals (e_ijk) assumed normal with land-class-specific variances and covariances that may vary by survey and land class.
- Parameter reduction (to keep models tractable):
  - Assume random effect variability does not vary by survey (common σ_i).
  - Use AR1 structure for repeated-measures covariance (covariances between successive surveys constant; non-adjacent surveys conditionally independent).
  - This AR1 reduction results in three random-effect parameters per land class, regardless of number of surveys, balancing model fit with computational practicality.
- Estimation of uncertainty: Bootstrap is used to obtain standard errors and confidence intervals, providing robustness to potential mis-specification of distributional forms.

## Model testing and Broad Habitats

- Application: Broad Habitat analyses (stock and change) were re-evaluated with the modelling approach using 1984, 1990, and 1998 data.
- Findings: Modelling removed the inconsistencies found with the old method; change estimates equalled differences in sequential stock estimates, and summed changes matched overall periods.
- Comparison: Differences between old and new methods were small relative to the existing discrepancies; most changes stayed within old method error bounds.

## Limitations and implications

- Computational demands: Modelling with bootstrap is slower than old methods; AR1 model is chosen for efficiency and robustness, but full parameterization can be slow for large variable sets.
- Data integration: Analyses use information from all surveys; results for a given survey can be updated as new data become available, leading to revisions of past estimates.
- Assumptions: Results rely on distributional assumptions for fixed and random effects; robustness of fixed-effect estimates is relatively high, but variance/covariance parameters can be sensitive to mis-specification.
- Non-normal data: Some variables (e.g., standing water) exhibited non-normal distributions; in such cases, old methods were retained for those variables to avoid convergence issues, while generally the AR1/bootstrap approach was preferred.
- Scale of results: Outputs are presented on the original measurement scale; transformations would complicate interpretation due to mixed fixed and random effects.

## Practical implications for environmental analysts

- Improved precision: Leveraging all available data and the hierarchical structure yields more precise stock and change estimates.
- Consistency across time: Modelling ensures internally consistent estimates for stock and change across surveys, facilitating temporal trend analysis.
- Data accessibility and reuse: While some underlying data underpinning estimates are maintained for transparency, the approach encourages reuse of full model-based estimates and consistent methodologies across CS outputs.
- Automation and scalability: A standardized AR1-based modelling framework supports automated analyses across many variables, supporting large-scale, time-series environmental monitoring.

## References and methodological context

- Key methodological foundations and prior CS analyses cited, including:
  - Barr et al. (1993): Countryside Survey 1990 Main Report
  - Dempster, Laird, and Rubin (1977): EM algorithm for incomplete data
  - Efron and Tibshirani (1993): Bootstrap methods
  - Haines-Young et al. (2000): Accounting for nature: UK habitat assessment
  - Scott (2002): Maximum likelihood with empirical Fisher information
- The CS2007 approach integrates these foundations to deliver consistent, data-rich environmental monitoring outputs.