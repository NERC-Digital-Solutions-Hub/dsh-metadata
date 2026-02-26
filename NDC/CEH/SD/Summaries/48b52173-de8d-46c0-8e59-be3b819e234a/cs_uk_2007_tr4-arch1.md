# Statistical Methodology for Countryside Survey Data (CS2007)

- Purpose and scope
  - Describes statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
  - Aims to produce consistent, robust stock and change estimates by leveraging all available data and addressing previous inconsistencies between stock (level estimates) and change (between-survey differences).

- Key motivation for methodology change
  - Previous approach used all data for stock but only repeated measurements for change, causing mismatches and apparent inconsistencies.
  - Modelling with consistent estimation can use all data for both stock and change, improving precision and robustness, especially when dealing with missing data and complex sampling.

- Modelling approach and main features
  - Use of mixed effects/repeated measures models to achieve consistent estimates of stock and change across multiple surveys.
  - Two data levels addressed:
    - Square level data (1 km squares): modeled with repeated-measures/mixed models to capture fixed effects (survey year) and random effects (squares, within-square variation, and their correlations across surveys).
    - Plot level data within squares: extended models to include plot-level residuals, allowing for hierarchical data structure and within-square/within-plot variability.
  - Reduction of random-effects parameters to keep models stable and computationally feasible:
    - AR1 (autoregressive order 1) structure for covariances, plus common variance parameters across surveys, substantially reducing parameter count.
  - Model specification
    - General form: y_ijk = a_ink + s_ij + e_ijk, with fixed effects a representing land-class means by survey, square-level random effects s_ij, and repeated-measures residuals e_ijk.
    - Assumes normality for random effects and residuals within land classes; uses bootstrap to obtain robust standard errors and confidence intervals where distributional assumptions may be questionable.
  - Estimation and inference
    - Fixed effects (stock/change) estimated robustly; variance/covariance components require careful specification.
    - Bootstrap is used to obtain standard errors and confidence intervals, mitigating sensitivity to normality assumptions.

- Data structure and sampling
  - CS sampling comprises a stratified sample of 1 km squares within a 15 km GB grid, with two levels of data collection:
    - Square level: overall square measurements, linked to Land Classes.
    - Plot level: measurements within each square (e.g., vegetation, soils).
  - Land Classification System (ITE) evolved by country-specific reporting; CS2007 uses 45 classes (England, Wales, Scotland have separate classifications).

- Testing and application: Broad Habitats
  - Prior analyses showed inconsistencies when using old methods; modelling with AR1 consistently removed these discrepancies.
  - For seven Broad Habitats across 1984, 1990, and 1998 data, modelling produced stock/change estimates without the previous inconsistencies and within the old method’s error bounds.
  - Demonstrated that stock and change estimates derived from the consistent method align with historical data while providing more precise estimates.

- Limitations and implications
  - AR1 modelling, while robust and more informative, is computationally more intensive; full parameterised models can be slow, so a standard AR1 approach was adopted for automation across many variables.
  - Distributional assumptions matter for variance/covariance estimates; bootstrap helps, but complex models may still be sensitive to non-normal data.
  - Results for a given survey can be updated when new data become available, meaning estimates may slightly revise past figures; this reflects improved utilization of all information rather than errors.
  - Non-normal data (e.g., standing water) can lead to convergence issues; in such cases, older methods may be retained for those specific variables.
  - The approach is designed to be robust and scalable to large numbers of variables, automating model fitting while ensuring results remain within plausible bounds.

- Practical outcomes for analysts
  - More precise, consistent stock and change estimates by incorporating data from all surveys and properly accounting for data hierarchy (squares and plots).
  - Improved ability to track long-term trends across entire timeseries rather than only adjacent survey changes.
  - Updated estimates for earlier surveys as new data become available, with small anticipated revisions rather than large, unexplained shifts.
  - Concrete, model-based framework (AR1 mixed models with bootstrap SEs) that can be automated for large-scale analysis across many habitat types and variables.