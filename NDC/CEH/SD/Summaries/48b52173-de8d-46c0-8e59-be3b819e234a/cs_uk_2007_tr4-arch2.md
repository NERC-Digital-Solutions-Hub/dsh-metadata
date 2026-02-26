# Countryside Survey 2007: Consistent Estimation for Stock and Change

- Executive summary
  - Describes the statistical methodology for Countryside Survey (CS) data, reviewing previous methods and detailing changes introduced for CS in 2007.
  - Old methods were robust but produced inconsistencies: stock estimates used all survey data, while change estimates relied on repeated measurements, leading to mismatches between stock and change across surveys.
  - Modelling-based, consistent estimation is feasible and robust; differences from previous methods are generally small relative to existing inconsistencies.
  - The new modelling approach uses all available information to yield more precise estimates, with past survey estimates potentially updated as new data become available.
  - Implementation is technically challenging and computationally intensive, but results are a substantially improved product; checks against the old method show differences within expected bounds.
  - The CS2007 analysis adopts the modelling approach and integrates it with bootstrapping to provide robust uncertainty assessment.

- 1. Introduction
  - This technical report outlines sampling and analysis procedures for CS data, reviews the previous CS methodology, and explains the rationale and details of the 2007 methodological changes, along with limitations and implications.

- 2. Overview of previous CS methodology
  - CS data are collected from a stratified sample of 1 km squares on a GB grid, with two sampling levels: square-wide measurements and within-square plot measurements.
  - Land Classification (ITE) stratifies squares; the classification evolved to 45 classes for CS2007 to support country-specific reporting.
  - Estimation previously involved means and standard errors by Land Class, then aggregation by land area to regional figures; assumed independence between Land Classes and totals.
  - Significance testing relied on normality; earlier methods used bootstrapping for square-level data to address non-normality.

- 3. Reasons for modifications to CS methodology
  - Inconsistencies arose because stock estimates used all data from a survey while change estimates used only repeated measurements, causing differences that could be misinterpreted as errors.
  - Missing information across survey pairs (e.g., unrepeated squares) contributed to discrepancies when comparing adjacent and non-adjacent survey changes.
  - Several potential approaches to achieve consistency were considered; modelling offered consistent and efficient estimates for both stock and change across square and plot levels.

- 4. Consistent estimation via modelling
  - 4.1 Possible approaches
    - Modelling stock and change together using data from all surveys provides consistent estimates; direct differences between stock estimates can also be used but may be less efficient in some cases.
  - 4.2 Modelling basics
    - Incomplete data techniques (e.g., EM-like mixed models) are employed to handle missing information, requiring distributional assumptions.
    - Mixed-effects/repeated-measures models are fitted to data across surveys; fixed effects relate to stock/change, random effects reflect sampling structure.
  - 4.3 Square level data
    - Square-level data are treated as repeated-measures within land classes; a two-component model with fixed effects (land-class means per survey) and random effects (square-level and repeated-measures variation) is used.
    - Random effects include square-level deviations and correlations of repeated measurements within squares across surveys.
  - 4.4 Plot level data
    - Plot data within squares are more fully incorporated to leverage hierarchical structure; models can include plot-level residuals in addition to square-level effects.
    - Both square- and plot-level models can be embedded in bootstrapping for robust SEs.
  - 4.5 Model specification
    - General form: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed land-class means per survey, s_ij are square random effects, and e_ijk are repeated-measures residuals.
    - Random effects are typically assumed normal; variances/covariances can vary by land class and survey.
    - To keep models tractable with many surveys, random-parameter reduction is used (e.g., AR1 structure: constant within-land-class variance across surveys and first-order autocorrelation for repeated measures).
    - Bootstrap is recommended for standard errors due to potential mis-specification of variance-covariance structures.
  - 4.6 Model testing – Broad Habitats
    - Analyses of Broad Habitat data from 1984, 1990, 1998 demonstrated prior inconsistencies between stock and change using old methods.
    - Fitting AR1 mixed models produced consistent estimates; changes computed as differences between stock estimates matched sums of inter-survey changes.
    - Comparisons showed new estimates generally within old-method uncertainty, with improvements in internal consistency.
    - Results supported adopting the modelling approach for CS2007 data across square and plot levels.
  
- 5. Limitations and implications
  - Bootstrapped standard errors with AR1 models are robust but computationally intensive; fully parameterised models are slow for large variable sets.
  - The AR1 approach provides a practical balance between model complexity and stability; fixed effects estimates are robust to some distributional mis-specification.
  - Some non-normal data (e.g., standing water) can cause convergence issues; in such cases, older methods may be used for that variable, or results treated with caution.
  - Implementing a model-based, data-integrating approach means past survey estimates can be revised as new data become available, which is conceptually different from reporting inconsistencies in earlier practice but aligns with updating knowledge as information accumulates.
  - Adoption improves precision by using the full data hierarchy and all available information, enabling standardized, comparable outputs across time; however, it requires automated models and consistent quality checks for large-scale analyses.

- 6. References
  - Cited works include foundational CS reports and methodological developments (e.g., Barr et al., 1993; Haines-Young et al., 2000), EM algorithm references (Dempster et al., 1977), bootstrap references (Efron and Tibshirani, 1993), and methodological developments by Scott (2002).