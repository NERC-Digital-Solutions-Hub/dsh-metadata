# Countryside Survey 2007: Statistical Methodology

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, review previous methods, and detail changes introduced for CS in 2007 to achieve consistent estimation of stock and change.

- Core shift in 2007: Move from estimating stock and change with separate data sets (old method) to a modelling approach that provides consistent, efficient estimates by using all available information and accounting for data hierarchy and missing information.

- Benefits of modelling approach:
  - Produces more precise estimates by leveraging information from all surveys and the data structure.
  - Ensures stock and change estimates are consistent within the modelling framework.
  - Reduces discrepancies between stock and change observed under previous methods.
  - Enables unified analysis across square and plot level data, including hierarchical structure.

- Key methodological changes:
  - Adoption of mixed effects/repeated measures models (square level) and extended approaches for plot level data.
  - Use of an AR1 (autoregressive order 1) structure to model covariances across surveys, reducing the number of random parameters and improving stability.
  - Bootstrapping to derive standard errors and confidence intervals, accommodating non-normal data distributions.
  - Implementation across multiple variables and habitats with automated procedures, aimed at robustness and practicality for large datasets.

- Data structure and sampling:
  - CS data come from a stratified sample of 1 km squares on a GB-wide 15 km grid.
  - Two sampling levels: square level (overall square metrics) and plot level (within-square plot measurements).
  - Land Classification (ITE) used for stratification; classifications updated over time for national reporting (England, Wales, Scotland).

- Estimation approaches:
  - Old method: stock estimated using all data from a survey; change estimated from repeated measurements, leading to potential inconsistencies between stock and change.
  - New modelling method: jointly estimates stock and change via a single model, ensuring consistency and improving efficiency; uses complete data across surveys and incorporates missing information via the model.

- Modelling basics:
  - Data are treated as hierarchical; models include fixed effects (land class means over surveys) and random effects (square and plot level variations, plus within-square/repeated measures correlations).
  - Square level model: y_ijk = a_iK + s_ij + e_ijk, with a_iK as fixed effects (land class means per survey), s_ij as square random effects, and e_ijk as repeated measures errors; distributions assume normality with land-class-specific variances and covariances.
  - Plot level extension: introduces a plot-level random effect in addition to square-level effects to capture within-square plot variation; both square and plot levels can be embedded in bootstrapping.

- Practical model considerations:
  - Full model with all random effects can be unstable and computationally intensive; AR1 with a smaller set of parameters balances stability and precision.
  - Assumptions about variance/covariance structures are important; mis-specification can affect standard errors, but bootstrap can mitigate this.
  - Transforming data to ensure normality is avoided to preserve results on original measurement scales; transformation complicates interpretation and back-transformation.

- Model specification (illustrative):
  - y_ijk = a_i k + s_ij + e_ijk, with fixed effects a_i k representing land-class means across survey k, square-level random effects s_ij, and repeated-measures residuals e_ijk.
  - Random effects (s_ij, e_ijk) are normally distributed with land-class specific variances; AR1 structure used to model covariances across surveys.
  - Reductions in random parameter counts achieved by assuming constant variance components across surveys and/or land classes, and using AR1 for covariances.

- Model testing and Broad Habitats:
  - Re-analysis of Broad Habitat data from 1984, 1990, and 1998 showed that modelling avoided the inconsistencies seen when using stock-change differences from old methods.
  - Consistent estimates derived from modelling matched within old method error envelopes; changes between methods typically small relative to existing uncertainties.
  - Demonstrates feasibility of applying consistent estimation to both square and plot-level data, and across different habitat datasets.

- Limitations and implications:
  - Modelling is computationally demanding, particularly when analysing many variables; AR1 offers a practical balance between speed and robustness.
  - Distributional assumptions affect variance/covariance estimates; bootstrap provides more reliable standard errors when these assumptions are imperfect.
  - Not all data are equally well-behaved (e.g., freshwater standing water showed non-normality challenges); in some cases, old methodology may be retained for specific variables.
  - Results are “updated” as new surveys are added; estimates for earlier surveys can shift slightly with new information, which is conceptually different from historical inconsistencies but reflects improved information use.
  - An automated, standard modelling approach is favored for large-scale application, ensuring robustness across many variables while acknowledging potential limitations in model fit for very non-normal data.

- Implications for data governance and practice:
  - Enhanced precision and consistency support more reliable trend analysis and reporting over time.
  - The approach encourages better metadata, data quality, and documentation to support complex hierarchical modelling.
  - Findings emphasize the importance of coherent data systems and the need to coordinate data across surveys, habitats, and plot/square levels for robust national reporting.
  - Results can influence how future CS analyses are conducted and updated as new data become available.

- References and context:
  - Builds on prior CS methodology (Barr et al., 1993; CS1990 main report) and statistical foundations (EM algorithm for incomplete data; bootstrap methods; mixed-effect modelling).
  - Aligns with broader efforts to account for missing data and hierarchical sampling in environmental surveys.
  - Publication and methodologies supported by NERC and Defra partnerships; aims for transparent, robust inference across CS2007 and beyond.