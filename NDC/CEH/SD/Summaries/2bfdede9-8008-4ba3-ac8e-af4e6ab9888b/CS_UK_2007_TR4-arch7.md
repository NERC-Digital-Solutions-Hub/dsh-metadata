# Countryside Survey 2007: Modifications to CS Methodology

## Executive summary (key takeaways for GIS practitioners)
- The report describes the statistical methodology used to analyze Countryside Survey (CS) data and the changes implemented for CS in 2007 to achieve consistent estimation of stock and change.
- Previous methods: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling approach: adoption of a modelling framework (consistent estimation) that uses data from all surveys to produce more precise, robust estimates for both stock and change.
- Benefits: greater precision by leveraging all available information; changes to past survey estimates are typically small but possible as new data informs earlier results.
- Trade-offs: modelling requires stronger distributional assumptions and more computing time; implemented checks compare new and old methods to ensure results remain within prior uncertainty.
- Scope and data structure: method applied to square-level and plot-level data, with land-class stratification and hierarchical sampling (1 km squares, with plots within squares).
- Practical implication for GIS: enables more reliable, comparable map-based representations of habitat extent and change over time; however, past estimates may be updated as new data are incorporated.

## What CS data and sampling look like
- Two-level sampling framework:
  - 1 km squares arranged on a 15 km GB grid; each square is mapped and surveyed for features (some measurements at the square level, others within plots inside the square).
  - Measurements include binary and continuous variables (areas, lengths, etc.).
- Land Classification:
  - CS uses country-specific land classifications derived from a broader GB Land Classification; 21 classes in England, 8 in Wales, 16 in Scotland (total 45 classes across the UK).
- Relevance for GIS:
  - Data are inherently spatial with class-based stratification, enabling map-based analysis of stock and change across land classes and time.

## Estimation: from old to consistent modelling
- Old approach:
  - Stock estimates: calculated using all data from a survey.
  - Change estimates: calculated from repeated measurements only.
  - Result: potential mismatches between stock and change estimates and perceived inconsistencies.
- New approach (2007 onward):
  - Use modelling to estimate both stock and change consistently from data across all surveys.
  - Modelling is feasible and robust for Broad Habitat data and other CS data.
  - Greater efficiency (more precise estimates) but requires model-based assumptions.
- Bootstrap:
  - To obtain significance and confidence intervals, bootstrap methods are used due to non-normality concerns in some features.

## Modelling basics: how consistency is achieved
- Core idea: address missing data and differing data availability across surveys by fitting a joint model to all surveys.
- Random effects and fixed effects:
  - Fixed effects: land-class means across surveys.
  - Random effects: account for square-level variation and the correlation of repeated measurements within squares across surveys.
- Square-level data:
  - Treated as repeated-measures within land classes; a mixed-effects model is used.
- Plot-level data:
  - Data within squares can be modeled with plot-level residuals in addition to square-level effects; bootstrapping can incorporate these structures.
- Model robustness:
  - Fixed-effect estimates (stock and change) are relatively robust to distributional mis-specification; variance/covariance parameters are more sensitive to assumptions.
  - To balance complexity and tractability, simpler yet effective structures are used (AR1 model).

## Square-level data: modelling structure
- General model form:
  - y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects for land class i in survey k (mean across surveys)
  - s_ij: square-level random effect for square j in land class i
  - e_ijk: repeated-measures residual for square j in survey k
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) with covariances between surveys
- Practical note:
  - The full model with all random effects can be unstable or slow; simplifications are used to keep it tractable.

## Plot-level data: extending the model
- Plot-level data adds a plot-level residual to capture within-square variation.
- Models can be extended to include both square-level and plot-level random effects, with correlations across surveys.
- Bootstrapping can be used to obtain standard errors for these extended models.

## Model specification and practical considerations
- Parameter count challenge:
  - A fully parameterized model has many random-effects parameters, which can be unstable due to limited observations per land class.
- Reducing complexity:
  - Assumptions to reduce random effects include:
    - Variance parameters do not vary across surveys (common σ_i).
    - Autoregressive AR1 structure for covariances across successive surveys.
  - This AR1 reduction yields a manageable number of random parameters (three per survey, regardless of how many surveys).
- Bootstrap for standard errors:
  - Since variance/covariance estimates can be unstable, bootstrap is recommended and used.

## Model testing: Broad Habitats
- Application to Broad Habitat data (square-level) across 1984, 1990, 1998 (and comparisons to earlier definitions).
- Findings:
  - Models yield consistent stock and change estimates, avoiding discrepancies seen with old methods.
  - Differences between old and new estimates stay within prior uncertainty; changes across periods align with sum of interval changes.
- Implication:
  - The modelling approach is feasible and beneficial for Broad Habitats; supports adoption for 2007 CS and beyond.

## Limitations and implications for data products
- Computational demand:
  - AR1 modelling with bootstrap is more time-consuming than old methods but is manageable for CS-scale analyses.
- Model selection:
  - Fixed-effect estimates are robust to some model choices, but variance/covariance estimates are sensitive; standard errors rely on bootstrap for robustness.
- Data updating and consistency over time:
  - Including data from all surveys means past estimates can be revised as new data are added; allows updating but breaks the notion of fixed past figures.
- Non-normal data concerns:
  - Some variables (e.g., standing water) showed non-normal distributions that complicated convergence; in such cases, old methodology may be preferred for that variable.
- Practical impact for GIS:
  - Produces more precise, consistent map-based estimates of stock and change, enabling better temporal comparisons.
  - Requires automated data pipelines to run standard modelling procedures across many variables.
  - Past GIS products may be updated as new CS data are incorporated, but changes are typically small relative to prior uncertainties.

## References
- Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002) – foundational texts and prior CS methodology work.
- Countryside Survey project information and contact details.

## About the document
- Authors: W.A. Scott; Centre for Ecology and Hydrology (NERC)
- Date: November 2008
- Focus: description of the 2007 CS statistical methodology, rationale for changes, modelling details (square/plot level), testing with Broad Habitats, and implications for future CS analyses and GIS-derived data products.