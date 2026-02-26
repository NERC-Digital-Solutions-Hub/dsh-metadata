# Countryside Survey 2007 Methodology

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, summarize previous methods, and detail the changes adopted for CS in 2007 to achieve consistent estimates of stock and change.

- Core shift in approach:
  - From creating stock estimates (using all data from a survey) and change estimates (from repeated measurements) to a modelling framework that provides consistent and efficient estimates of both stock and change across surveys.
  - Modelling uses data from all surveys jointly, improving precision but requiring distributional assumptions that must be validated.

- Key benefits:
  - More precise estimates by exploiting all available information and the hierarchical structure of CS data.
  - Consistency between stock and change estimates across survey intervals, reducing apparent discrepancies.
  - Ability to produce estimates for both square-level and plot-level data within a unified modelling framework.

- Principal challenges and considerations:
  - Modelling requires additional distributional assumptions; results especially for small subsets must be validated against the old method.
  - Modelling is computationally intensive; full models with many random effects can be unstable or slow but simplified AR1 models balance robustness and efficiency.
  - Updating past survey estimates: as new data arrive, past estimates may be revised, which is conceptually different from the previous inconsistent reporting but arguably appropriate as information accumulates.

- Data structure and sampling:
  - Based on a stratified sample of 1 km squares on a GB-wide 15 km grid.
  - Two sampling levels: square level (whole square measurements) and plot level (within-square plots for detailed vegetation/soil data).
  - Land Classification (ITE) used for stratification; classifications have expanded over time (GB -> 42 classes in CS2000, 45 classes in CS2007; separate country classifications with related classes).

- Estimation approaches (old vs new):
  - Old method: stock estimates used all squares in a survey; change estimates used only repeated squares, causing potential inconsistencies between stock and change.
  - New method: consistent estimation via modelling (mixed effects/repeated measures) that directly estimates stock and change from all data, with differences derived from fixed effects; bootstrap used for standard errors due to non-normality concerns.

- Modelling details:
  - Square-level data:
    - y_ijk = a_i_k + s_ij + e_ijk, where:
      - a_i_k: fixed effects (land class i, survey k)
      - s_ij: square-level random effect
      - e_ijk: repeated-measures random effect
    - Random effects: s ~ N(0, τ_i^2); e ~ N(0, σ_ik^2) with covariances across surveys
    - AR1 (autoregressive of order 1) style reduction to control the number of random parameters (three per survey when used with land classes)
  - Plot-level data:
    - Extends square-level model to include plot-level residuals; accounts for within-square plot variation and survey correlations.
  - Model specification and robustness:
    - Fixed effects capture land-class means per survey; changes come from differences in fixed effects between surveys.
    - Reduction of random parameters to maintain stability; AR1 model used with bootstrap SEs for robustness.
    - Non-normal distributions can affect variance/covariance estimates; bootstrap helps maintain reliable SEs.

- Model testing and Broad Habitats:
  - Re-analyzed seven Broad Habitats across 1984, 1990, 1998 using both old and new methods.
  - Findings: new modelling approach produced consistent stock and change estimates; differences from old method were generally within old error bounds; improvements in internal consistency demonstrated.
  - Additional checks extended to soil data and plot-level data, confirming feasibility of consistent estimates beyond square-level data.

- Limitations and practical implications:
  - Computationally demanding, particularly with large numbers of variables; AR1 offers a practical balance but is still slower than the old method.
  - Fixed-effect estimates are robust to some mis-specification, but variance/covariance parameters require careful handling; bootstrap is used to obtain reliable SEs.
  - Very non-normal data (e.g., freshwater standing water) may converge to local maxima with the new method; in such cases, the older method’s estimates may be preferred.
  - Analyses are conducted using data from all surveys; consequently, past survey estimates may be revised as new data are incorporated, reflecting updated information and better modelling.

- Implications for data governance, storage, and sharing (Data Steward lens):
  - Necessitates comprehensive documentation of methodology, model specifications, assumptions, and changes over time for auditability and reproducibility.
  - Requires versioning of datasets and methods to track updates to past survey estimates as new data arrive.
  - Encourages standardized metadata for sampling design (square/plot hierarchy, Land Classification), data types, and modelling choices (AR1, bootstrap procedures).
  - Highlights the importance of providing access to both old and new method results during transition to maintain comparability and transparency.
  - Emphasizes automated, scalable analysis pipelines to handle large numbers of variables across multiple surveys.
  - Underlines the value of metadata on data quality issues, such as non-normality concerns and specific variables with non-standard distributions.

- Outcome and trajectory:
  - Adoption of a consistent, model-based estimation framework for CS2007 (and beyond) to improve precision and cross-survey comparability.
  - Demonstrated feasibility of applying sophisticated statistical models to large, hierarchical environmental datasets with multiple data layers (square and plot levels).
  - Commitment to transparency in methods, validation against prior approaches, and readiness to update historical results as data accumulate.