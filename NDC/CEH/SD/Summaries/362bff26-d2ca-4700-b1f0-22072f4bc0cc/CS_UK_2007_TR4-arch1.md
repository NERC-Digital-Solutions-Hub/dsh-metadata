# Countryside Survey 2007: Description of the statistical methodology used for the analysis of Countryside Survey data

- Executive Summary
  - Describes the statistical methodology used to analyse Countryside Survey (CS) data and the changes introduced for CS in 2007.
  - Old methods were robust but produced inconsistencies: stock was estimated from all survey data, while change relied on repeated measurements, leading to mismatches between stock and change.
  - Modelling for consistent estimation (using all available data and the full hierarchical structure) is feasible and generally robust; differences from old methods are small relative to existing inconsistencies.
  - The new modelling approach increases precision by leveraging all information, though it requires additional distributional assumptions and more computational effort.
  - To ensure reliability, results from the new methods were checked against the old methods, especially for small subsets of data.
  - The AR1 modelling approach with bootstrap-based standard errors was selected for its balance of robustness, efficiency, and practicality for large numbers of analyses.
  - Adoption of model-based methods implies that estimates for earlier surveys can be updated as new data become available, which may slightly revise past results.

- 1. Introduction
  - Provides an overview of CS sampling and analysis procedures, reviews the previous CS methodology, and explains the reasons for and details of changes implemented for CS2007.
  - Highlights the limitations of prior methods and the goal of achieving consistency across the full time span of CS data.

- 2. Overview of previous CS methodology
  - Sampling: CS uses a stratified sample of 1 km squares across GB on a 15 km grid; two levels of sampling within each square (square-level data and plot-level data within squares); Land Classification (LClasses) stratifies squares; classifications evolved (GB → Scotland/Wales-specific) to support separate reporting.
  - Estimation: previous approach calculated means and standard errors by Land Class and then combined them (weighted by land area) to produce regional/national stock or change estimates; assumed independence between Land Classes.
  - Bootstrapping: due to skewness, CS2000 shifted from normality-based SEs to bootstrap methods to obtain significance testing and confidence intervals.

- 3. Reasons for modifications to CS methodology
  - Inconsistencies arose because stock estimates used all data from a survey while change used only repeated measurements; this could yield non-matching stock and change estimates.
  - Several potential approaches to achieve consistency were considered (e.g., using all data for stock and all data for change, or using repeated squares only, or modelling); modelling was identified as feasible and capable of producing consistent and efficient estimates for both square and plot data.
  - The aim was to move from presenting potentially conflicting point estimates to providing a coherent, model-based framework.

- 4. Consistent estimation
  - Square-level data
    - Data are treated as a random sample of squares within each Land Class, with missing observations handled via mixed-effects/repeated-measures models.
    - Fixed effects: Land Class means across surveys (year as a categorical predictor).
    - Random effects: square-level deviations and within-square repeated-measures correlations; an AR1 structure is used to model covariances across successive surveys.
    - A simplified AR1 approach reduces the number of random-parameter estimates, enabling stable and efficient estimation across many Land Classes.
    - Bootstrap is used to obtain robust standard errors because variance/covariance parameters are less reliably estimated.
  - Plot-level data
    - Plot data within squares were previously handled in various ad hoc ways; modelling extends to include plot-level random effects, allowing for correlation within squares and across surveys.
    - Both square-level and plot-level information can be incorporated, with bootstrapping enhancing reliability of SEs.
  - Model specification
    - General square-level model: y_ijk = a_i_k + s_ij + e_ijk, with fixed effects a_i_k (Land Class i, survey k), square random effects s_ij, and repeated-measures error e_ijk.
    - Random effects are assumed to be normally distributed, with variances/covariances that may vary by Land Class; AR1 structure reduces parameter count.
    - Practical considerations: full parameterization is complex and slow; AR1 with bootstrap provides a robust, automated solution for large-scale analyses.
  - Model testing – Broad Habitats
    - Re-analysis of historical Broad Habitat data (1984, 1990, 1998) showed that modelling avoided the inconsistencies of the previous approach and that changes inferred from stock differences aligned with sums of inter-survey changes.
    - Comparisons between old and new methods found that most estimates remained within old error bounds; differences were generally small and not statistically significant.
    - Results supported adopting the new consistent estimation approach for CS2007 and beyond; consistency also extended to soil and plot-level datasets.

- 5. Limitations and implications
  - Bootstrapped SEs within the AR1 framework are robust, but fully parameterized models are slow; AR1 strikes a balance between robustness and computational practicality for large variable sets.
  - Model selection and checking are essential; fixed effects are robust to moderate mis-specification, but variance/covariance estimates can be sensitive to distributional assumptions.
  - Some non-normal data (e.g., standing water) may cause convergence or estimation issues; in such cases, older methods may be retained for those variables.
  - Adopting a model-based approach means past survey estimates can be revised as new data are added, reflecting improved information rather than identifying errors in earlier analyses.

- 6. References
  - Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002) and related CS methodology literature.
  - Acknowledges funding and distribution rights for Countryside Survey data and outputs.