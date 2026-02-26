# Countryside Survey 2007: Statistical Methodology

- Purpose and scope
  - Describes the statistical methods used to analyze Countryside Survey (CS) data.
  - Explains the shift from previous methods to modelling-based, consistent estimation of stock and change for the 2007 CS data.
  - Assesses limitations, implications, and validation against older methods.

- Data, sampling, and structure
  - Data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two sampling levels: square level (area-wide measures) and plot level (within-square measures).
  - Variables vary from binary to continuous; land classification (ITE) underpins strata, with country-specific classifications (England, Wales, Scotland).
  - Measurements include stock-like totals per land class and changes across survey intervals; missing data arise from uneven square recording across surveys.

- Estimation: consistency and efficiency
  - Old method: stock estimates used all data from a survey, while change estimates used only repeat measurements, causing inconsistencies between stock and change.
  - New modelling approach aims to provide consistent estimates of stock and change using all available data and the hierarchical structure, producing more precise results.
  - Changing emphasis from adjacent-survey changes to timelines spanning from the first survey to the present.

- Modelling framework
  - Mixed effects/repeated measures models underpin consistent estimation.
  - Models accommodate the CS hierarchical sampling (squares and plots) and the correlation of repeated measurements.
  - Fixed effects capture land-class means across surveys; random effects capture square-level and within-square/plot-level variation and correlations.

- Square-level data modelling
  - Treated as a repeated measures problem within land classes.
  - Basic form: fixed effects for land-class means across surveys; random square effects; repeated-measures residuals.
  - Variance and covariance structures model how measurements vary by land class and across surveys.

- Plot-level data modelling
  - acknowledges within-square plot variation; previously treated plots as independent or aggregated at square level.
  - Extended mixed models incorporate an additional plot-level random effect alongside the square-level effect.
  - Both square- and plot-level models can be embedded within bootstrap procedures to obtain standard errors.

- Model specification and AR1 approach
  - General square-level model: y_ijk = a_ik + s_ij + e_ijk, with a_ik fixed effects (land-class means), s_ij square random effects, e_ijk repeated-measures residuals.
  - Distributional assumptions: random effects normally distributed with land-class-specific variances; residuals normally distributed with variances varying by land class and survey; covariances between surveys captured.
  - Parameter reduction (AR1 model): assume common variance across surveys within a land class and an autoregressive (order-1) structure for covariances across successive surveys.
  - Result: a robust, stable model with a small, fixed number of random-effect parameters (three per land class, regardless of the number of surveys).
  - Bootstrap: used for standard errors to remain robust to potential misspecification of random-effect distributions.

- Model testing: Broad Habitats
  - Examines stock vs. change estimates for Broad Habitats across 1984, 1990, and 1998.
  - Demonstrates that modelling removes the inconsistencies seen with the older methods (differences between stock-derived changes versus repeated-squares changes).
  - Findings show new modelling estimates largely fall within previous error bounds, with improvements in precision.

- Limitations and implications
  - AR1 modelling is computationally intensive; fully parameterised models are slow, so a pragmatic AR1 approach with bootstrap is chosen.
  - Fixed-effect estimates are robust to some mis-specification, but variance/covariance estimates can be sensitive; bootstrap mitigates this.
  - Non-normal distributions can cause convergence issues (notably seen with standing water in freshwater data); in such cases, older methods may be preferred for those variables.
  - Using data from all surveys means earlier survey estimates can be updated as new data arrive; this yields more accurate historical estimates but alters previous reporting slightly.
  - The approach scales to large numbers of variables through automation, balancing model complexity with practical run times.

- Practical implications for GIS and data products
  - Produces stock and change estimates that are consistent across time, enhancing map-based data products and time-series analyses.
  - Leverages the full data hierarchy (square and plot levels) to deliver more precise spatial estimates that support policy, management, and public-facing visualizations.
  - Requires computational resources and automated quality checks to ensure consistent results across many variables.
  - Outputs can be updated with each new survey, providing refined baselines for past maps and future projections.

- References and further reading
  - Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron and Tibshirani (1993); Scott (2002) for underlying statistical methods and bootstrap/EM approaches.

- Summary for GIS specialists
  - The 2007 Countryside Survey adopts a consistent, model-based approach (AR1 mixed models with bootstrap) to estimate stock and change across land classes, squares, and plots.
  - This yields more precise, comparable map-based outputs over time, while explicitly handling missing data and the data’s hierarchical structure.
  - While more computationally demanding, the approach provides robust estimates and a scalable framework for producing GIS-ready statistics across numerous variables and habitats.