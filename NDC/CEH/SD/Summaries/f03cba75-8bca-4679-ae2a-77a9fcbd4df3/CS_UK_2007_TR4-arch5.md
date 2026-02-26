# Statistical Methodology for the Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes made for CS2007 to improve consistency.
- Previous methods used stock estimates from all data and change estimates from repeated measurements, leading to inconsistencies between stock and change.
- Modelling approaches (consistent estimation) using data from all surveys provide more precise and robust estimates and ensure consistency between stock and change.
- Implementation is computationally intensive and requires careful validation; AR1 mixed-effects models with bootstrap are preferred for practicality and robustness.
- Tests on Broad Habitat data and other datasets show that the new modelling approach yields estimates within the uncertainty of the old methods while improving precision.
- Results imply that estimates for past surveys may be revised as new survey data are added, reflecting improved use of information across time.

## Context and Data Structure
- CS data are collected from a stratified sample of 1 km squares across GB, with two sampling levels: square level (land-class means) and within-square plot level.
- Land Classification (ITE) is used to stratify square selection; classifications have expanded over time (GB → 42 classes in CS2000, 45 in CS2007, with country-specific subdivisions).
- Data types range from binary to continuous; stock estimates relate to land-class means, while change estimates relate to temporal differences.

## Previous Methodology and Challenges
- Stock estimates used all data from a survey; change estimates used repeated measurements across surveys.
- This led to inconsistencies: stock changes did not align with changes estimated from repeated plots/squares.
- Inconsistencies were partly due to missing data when surveys introduced new squares or dropped some squares (e.g., landowner refusals).

## The 2007 Methodology: Consistent Estimation
- Adopts a modelling approach that yields consistent estimates of stock and change across surveys, using data from all available surveys.
- Modelling also provides efficiency gains (more precise estimates) by leveraging hierarchical data and correlations across time.
- Requires additional distributional assumptions; results are checked against older methods to ensure validity, especially for small subsets.

## Modelling Approaches and Details
- Square-level data:
  - Treated as repeated-measures data within a Land Class.
  - Fixed effects: land-class means across surveys (regression on year/survey).
  - Random effects: square-level residuals; correlations of successive surveys within squares.
  - Aimed for a balance between model complexity and stability; AR1 assumptions reduce random-effect parameters.
- Plot-level data:
  - Recognizes hierarchical structure (plots within squares).
  - Early analyses treated plots as independent or summarized at the square level; modern approach uses mixed models that include plot- and square-level variation.
  - Models can incorporate a plot-level residual and square-level random effects; bootstrap can be used to obtain robust standard errors.
- Model specification:
  - General form: y_ijk = a_ik + s_ij + e_ijk, where:
    - a_ik are fixed effects (land-class means per survey),
    - s_ij are square-level random effects,
    - e_ijk are repeated-measures errors.
  - Distributions: s_ij ~ N(0, τ_i^2), e_ijk ~ N(0, σ_ik^2) with covariances between surveys.
  - Parameter reduction: assume constant within-land-class variance across surveys and AR1 structure for repeated-measures covariances to keep the model tractable as the number of surveys grows.
  - Bootstrap: used for standard errors to remain robust under non-normality and to accommodate complex variance structures.
- Model testing and Broad Habitats:
  - Used existing Broad Habitat data from multiple surveys to validate consistency; modelling removed the stock-change discrepancies present in older methods.
  - Results from modelling generally aligned with old estimates within old-method uncertainty bounds, but with improved consistency and precision.

## Implementation and Practical Considerations
- Computational intensity: full parameterization is slow; AR1 model with bootstrap provides a practical, robust solution suitable for automated, large-scale analyses.
- Verification: CS analysis programs run both old and new methods to ensure negligible differences beyond expected inconsistency bounds.
- Data updating: because analyses incorporate information from all surveys, estimates for earlier years can be revised as new data are added; this reflects improved precision rather than errors.
- Non-normal data: non-normal distributions may affect variance/covariance estimates; bootstrap mitigates some risks, but very non-normal variables may require alternative handling (as noted with freshwater standing water).

## Limitations and Implications for Reporting
- Some variables with highly non-normal distributions may converge to local maxima or be difficult to model (e.g., standing water in CS freshwater data); in such cases, older methodology may be reported for those variables.
- Fully parameterized models may be impractical for all variables; AR1 with bootstrap was chosen as a stable, scalable compromise.
- Results emphasize consistency and full data utilization, improving precision and coherence across time, at the cost of potential small revisions to past results when new data are incorporated.

## Governance and Data Stewardship Implications
- Data Provenance and Lineage:
  - Clear documentation of methods and model assumptions is essential to ensure reproducibility and trust in stock/change estimates.
  - Versioned analyses: past results may be updated as newer surveys are added; maintain a changelog of revisions and justification.
- Metadata and Documentation:
  - Capture details on sampling design, Land Class definitions, plot and square-level variables, random effects structure, and bootstrap procedures.
  - Document model selection criteria (AR1 vs. alternatives) and rationale for parameter constraints.
- Data Quality and Governance:
  - Emphasize complete, timely data collection at both square and plot levels to maximize model robustness.
  - Ensure consistent handling of missing data and survey changes (e.g., new squares, refusals) within the modelling framework.
- Operationalization:
  - Develop a standard, automated modelling pipeline to apply the AR1/bootstrap approach across many variables, ensuring consistent outputs.
  - Provide mechanisms to compare old and new methods for transparency and validation.
- Data Sharing and Reuse:
  - Share model outputs, code, and methodological documentation alongside datasets to enable reuse and auditing by data users.

## References (Key Context)
- Barr et al. (1993); Haines-Young et al. (2000) on habitat accounting and CS methodologies.
- Dempster, Laird, and Rubin (1977) on EM algorithm for incomplete data.
- Efron and Tibshirani (1993) on bootstrapping.
- Scott (2002) on maximum likelihood and empirical Fisher information.
- Countryside Survey (CS) methodological reports and 2007 CS analysis validation.