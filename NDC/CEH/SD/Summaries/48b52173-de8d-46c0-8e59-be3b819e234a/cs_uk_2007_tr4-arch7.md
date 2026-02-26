# Countryside Survey in 2007 – Statistical methodology

- Purpose and scope
  - Describes the statistical methodology used to analyse Countryside Survey (CS) data and the changes made for CS in 2007.
  - Aims to provide consistent, efficient stock and change estimates across surveys for map-based data products.

- What changed and why
  - Old methods produced stock and change estimates that could be inconsistent when compared across surveys (stock from one survey vs change from another).
  - New modelling approach using consistent estimation across all surveys addresses these inconsistencies and uses all available data, yielding more precise estimates.
  - Modelling requires more assumptions about data distributions and more computation, but validation shows estimates remain robust in practice.

- Sampling framework
  - CS data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two sampling levels: square-level measurements (some nationwide summaries) and within-square plot-level measurements (vegetation, soils, etc.).
  - Land Classification (regional classifications) partitions squares for analysis; classifications have evolved (GB 32 → 42 → 45 classes) to support country-specific reporting (England, Wales, Scotland).

- Estimation versus modelling
  - Old approach: means and standard errors per Land Class, then weighted combination to regional estimates; stock used all data from a survey, change relied on repeated measurements—leading to potential mismatches.
  - New approach: consistent estimation via modelling (mixed effects/repeated measures models) that yields stock and change estimates from the same data source and are automatically consistent.
  - Bootstrapping is used for significance testing due to possible non-normality.

- Modelling basics for square-level data
  - y_ijk = a_ik + s_ij + e_ijk, where:
    - a_ik are fixed effects (land-class survey means),
    - s_ij are square-level random effects,
    - e_ijk are repeated-measures errors with covariances across surveys.
  - Random effects account for within-square and between-survey correlations; variance and covariance parameters are estimated but can be numerous.
  - Practical reduction: adopt AR1 (autoregressive) structure to keep parameters manageable (common σ_i across surveys for repeated measures; AR1 for inter-survey covariances).

- Plot-level data and extensions
  - Plot-level measurements within squares can be incorporated by adding a plot-level residual; this improves efficiency but requires bootstrapping to derive valid standard errors.
  - Two model forms: one with square-level random effects only, and one that includes plot-level random effects.

- Model specification and practical considerations
  - Emphasises keeping parameters tractable: use AR1 with a small, fixed number of random effects per land class.
  - Fixed effects robust to moderate mis-specification of random effects; bootstrap provides robust SEs when variance-covariance structure is uncertain.
  - Transformations to handle non-normal data are generally avoided to keep results on the original measurement scale.

- Model testing: Broad Habitats
  - Reanalyzed habitat data (seven Broad Habitats) across 1984, 1990, 1998 to test modelling approach.
  - Modelling eliminated the previous stock-change inconsistencies across survey pairs; differences between old and new methods were within previous inconsistencies and often small.
  - Consistent estimates were achieved for both stock and change, and results aligned with earlier findings when considering prior variability.

- Limitations and implications
  - Computationally intensive, especially for large variable sets; AR1 model is a practical balance of speed and accuracy.
  - Estimates for a given survey are influenced by all surveys due to the joint modelling, meaning past estimates may be revised as new data come in.
  - Distributional assumptions affect variance/covariance estimates; bootstrap mitigates this for fixed effects.
  - Some variables (e.g., very non-normal data like standing water) may require special handling; in one freshwater case, the old method was retained due to convergence issues.
  - A standard, automated modelling approach is favored for large-scale CS analyses to ensure consistency and reproducibility.

- Implications for GIS data products
  - Produces more precise, consistent time-series estimates of stock and change across land classes and regions, improving map-based visualisations.
  - Results are updated as new surveys are added, offering refined past estimates; users should interpret past results as potentially revisable with new data.
  - Bootstrapped standard errors allow robust significance testing and more reliable confidence intervals for map-based reporting.
  - Enables unified treatment of square- and plot-level data, supporting richer, multi-scale GIS analyses and transparent uncertainty.

- References (selected)
  - Barr et al., Countryside Survey 1990 Main Report
  - Dempster, Laird, Rubin (EM algorithm)
  - Efron, Tibshirani (bootstrap)
  - Haines-Young et al., Accounting for nature: assessing habitats in the UK countryside
  - Scott (2002), Maximum likelihood estimation with empirical Fisher information

- Contact and funding
  - Countryside Survey project office, CEH Lancaster; CS2007 funded by Defra and partners led by NERC.