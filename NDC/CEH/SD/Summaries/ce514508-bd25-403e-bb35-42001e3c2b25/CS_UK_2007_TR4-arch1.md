# Statistical methodology for Countryside Survey data

- Purpose and scope
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data.
  - Summarises previous methods and outlines the changes implemented for CS in 2007 to achieve consistent estimation of stock and change.

- Key problem with previous methods
  - Stock estimates used all data from a survey, while change estimates used only repeated measurements, leading to inconsistencies between stock and change.
  - Inconsistencies arise because missing information (e.g., unrepeated squares/plots) is handled differently for stock and change.

- Modelling-based solution
  - Demonstrates that consistent, robust estimation of stock and change is feasible via modelling.
  - Modelling uses information from all surveys, providing more precise estimates (improved efficiency).
  - New approach was validated by comparing with the old method; differences generally small and within previous inconsistencies.

- Why switch to modelling
  - Addresses inconsistencies and leverages all available information.
  - Produces more precise estimates for both stock and change.
  - Enables consistent analysis across time; though past results may be updated as new data arrive.

- Data structure and sampling
  - Two-level sampling: 1 km squares on a GB-wide 15 km grid, with measurements at square level and within-square plot level.
  - Land Classification (LC) framework with country-specific adjustments (45 LC classes overall; England, Wales, Scotland have related but distinct classifications).

- Estimation and inference
  - Old method: means/standard errors by LC, then area-weighted combination to regional/national estimates; minimal distributional assumptions.
  - Bootstrap: used to obtain significance without assuming normality (especially for square-level data).

- Consistent estimation via modelling (core approach)
  - Use mixed-effects/repeated-measures models to jointly model stock and change across all surveys.
  - Fixed effects: LC means across surveys (stock-related parameters).
  - Random effects: account for square-level variation and within-square correlations across surveys; number of random parameters is managed to keep models tractable.
  - Square-level data: repeated-measures mixed models; AR1 (autoregressive order 1) structure to capture within-LC correlations over time.
  - Plot-level data: extend models to include plot-level residuals; maintain hierarchical structure; bootstrapping remains central for SEs.

- Model specification and simplification
  - General form for square-level data: y_ijk = a_i1 + a_i2 + ... + s_ij + e_ijk, where a_i_k are fixed effects for LC i in survey k, s_ij are square random effects, e_ijk are repeated-measures residuals.
  - Distributional assumptions: random effects and residuals assumed normal; AR1 structure reduces the number of random parameters, aiding stability and computation.
  - Pragmatic balance: robust fixed-effect estimates even if some random-effect distributions are misspecified; bootstrap enhances reliability of SEs.

- Model testing and Broad Habitats
  - Re-evaluated historical Broad Habitat data (1984, 1990, 1998) with the modelling approach.
  - Old method showed inconsistencies between stock and change; AR1 modelling produced consistent estimates with differences generally within the old method’s error bounds.
  - Results supported adopting the modelling method for CS2007 data.

- Limitations and practical implications
  - Computationally intensive; full parameterised models are slow for large variable sets, so AR1 modelling with bootstrap was preferred for practicality.
  - Fixed-effect estimates are robust to some mis-specifications; variance/covariance parameters are more sensitive, so bootstrap is used for SEs.
  - Results for any single survey may be updated as new data are incorporated; this is a natural consequence of using information from all surveys.
  - Some very non-normal data (e.g., standing freshwater) may require alternative handling; in such cases, old methods may be retained for those variables.

- Implications for reporting
  - Consistent estimation improves interpretability across time; however, cross-survey consistency at fixed reporting moments may be affected as new data revise past estimates.
  - The approach is designed to be automated for large-scale analyses, enabling robust, repeatable results across many variables.

- References and background
  - Foundational methods and prior CS reports (Barr et al., 1993; Haines-Young et al., 2000) cited.
  - Foundational statistical techniques: EM algorithm for incomplete data (Dempster et al., 1977), bootstrap (Efron & Tibshirani, 1993), empirical Fisher information (Scott, 2002).

- Practical takeaway for analysts
  - For CS data, modelling provides consistent stock and change estimates by integrating data across all surveys and accounting for the data hierarchy.
  - AR1 mixed-effects models, coupled with bootstrap for SEs, offer a robust and scalable solution, with careful attention to model specification and computational feasibility.
  - Users should expect some revision of past estimates as new surveys are incorporated, reflecting updated information rather than errors in prior analyses.

- Availability and contact
  - Countryside Survey in 2007 funded by NERC/Defra partnership; project outputs published by CEH and partners.