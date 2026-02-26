# Countryside Survey 2007 Methodology

- This report describes the statistical methodology used to analyze Countryside Survey (CS) data, summarises the previous methodology, and details the changes introduced for CS 2007 to achieve consistent estimation of stock and change.

- Key motivation for methodological change:
  - Previous approaches used stock estimates from all data in a survey and change estimates from repeated measurements, causing inconsistencies between stock and change across survey pairs.
  - Modelling-based, consistent estimation is feasible and generally robust, providing more precise estimates by using all available information and the data’s hierarchical structure.

- Data and sampling design:
  - CS data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two sampling levels: whole squares and within-square plots; measurements vary from binary to continuous (areas, lengths).
  - Land Classification (ITE) has 45 classes for CS 2007 (England, Wales, Scotland have country-specific classifications).

- Estimation and inference:
  - Old approach: means/standard errors per land class then weighted combination by land area; assumes independence between land classes and total land.
  - To assess significance, bootstrap methods are used due to potential non-normality, especially for square-level data.
  - New approach emphasizes consistency between stock and change across all surveys and uses modelling to integrate incomplete data.

- Modelling and modelling basics:
  - Consistent estimation is achieved by fitting mixed-effects/repeated-measures models to data from all surveys; fixed effects represent land-class-year means; random effects capture square-level and within-square (plot-level) variability and their correlations across surveys.
  - For square-level data, a repeated-measures (mixed) model is used with:
    - Fixed effects: land-class means per survey.
    - Random effects: square-level and within-square (survey-to-survey) deviations, with correlations across surveys.
  - For plot-level data, models extend to include plot-level random effects in addition to square-level effects; bootstrapping can be applied to these models.
  - A simplified AR1 (autoregressive, order 1) structure is used to reduce the number of random parameters and improve computational feasibility, while remaining robust for fixed-effect estimates.
  - Model specification example: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed land-class effects by survey, s_ij are square random effects, and e_ijk are repeated-measures residuals.

- Handling missing data and consistency:
  - Incomplete data (e.g., unrepeated squares across surveys) is addressed via mixed-model approaches that use information from all surveys without imputing missing values.
  - Consistency means stock and change estimates derived from the modelling approach are coherent across adjacent and non-adjacent survey intervals.

- Model testing and Broad Habitats:
  - CS2000/CS2007 analyses of Broad Habitats show that consistent modelling avoids the inconsistencies seen when using the old methods (e.g., changes from stock vs. repeat-squares).
  - Modelling outputs for Broad Habitats and plot-level data were validated against older data, generally within the bounds of previous discrepancies, supporting adoption of the new approach.

- Practical considerations and limitations:
  - The AR1 model with bootstrap SEs provides robust fixed-effect estimates but requires more computation than the old method.
  - Fully parameterised models can be slow; therefore, automated, standard models (like AR1) are preferred for large-scale analyses.
  - Results from a survey can be updated when new data are added, meaning past survey estimates may shift slightly with new information; this reflects improved use of all available data.
  - Distributional assumptions for random effects impact variance/covariance estimation; bootstrap helps maintain robust standard errors.
  - Non-normal data can cause convergence issues for some variables (notably freshwater standing water); in such cases, older methods may be retained for those specific variables.

- Data products and outputs:
  - The modelling approach yields stock estimates by land class and survey, along with change estimates that are internally consistent.
  - Outputs include standard errors and confidence intervals (via bootstrap), enabling more reliable trend analysis and planning.
  - The approach supports both square-level and plot-level analyses in a unified framework, enabling potential cross-level data products and dashboards.

- Implications for data support:
  - Requires automated pipelines to implement AR1 modelling, bootstrap SEs, and data updates as new CS surveys are conducted.
  - Promotes a shift from isolated survey reports to timeline-spanning analyses that incorporate all available data.
  - Emphasizes the need for clear communication of consistency considerations to end users, including how changes in past estimates may occur with new data.

- References and sources:
  - Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002), among others.