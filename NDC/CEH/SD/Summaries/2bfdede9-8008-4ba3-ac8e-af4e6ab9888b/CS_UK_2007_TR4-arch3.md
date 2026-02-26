# Countryside Survey 2007: Statistical Methodology

- Purpose
  - Describe the statistical methods used to analyse Countryside Survey (CS) data.
  - Review previous CS methodology and detail changes implemented for CS in 2007 to improve consistency between stock and change estimates.

- Why changes were needed
  - Previous methods calculated stock using all data from a survey but change from repeated measurements only, causing inconsistencies between stock and change estimates.
  - Inconsistencies could be misinterpreted as data errors; modelling offered a pathway to fully consistent estimates across surveys.

- Key methodological shift
  - Adopted a modelling approach (mixed effects/repeated measures) to produce consistent and more precise estimates of stock and change for both square-level and plot-level data.
  - Modelling requires more assumptions about data distribution; results are validated against the old method, especially for small subsets.

- Data and sampling framework
  - CS data come from a stratified sample of 1 km squares on a GB-wide 15 km grid; two levels of sampling within each square (square-level and within-square plots).
  - Measurements are varied (binary and continuous) and are classified by the ITE Land Classification, with country-specific adaptations (England, Wales, Scotland).

- Estimation: old vs new
  - Old method: stock means estimated from all data; change from repeated measurements; robust but potentially inconsistent with change estimates.
  - New method: uses modelling to estimate both stock and change consistently across all surveys; uses all available information and holds better precision.

- Modelling approach: square-level data
  - Data treated as repeated measures within Land Classes.
  - Fixed effects: land-class means by survey (regression of the variable on survey year).
  - Random effects: square-level deviations and survey-to-square residuals, with assumed normal distributions.
  - Stock estimates derived from fixed effects; change estimates are differences of stock estimates, ensuring consistency.

- Modelling approach: plot-level data
  - Acknowledges within-square plots; previous analyses either aggregated to square level or treated plots independently, risking inefficiency or bias.
  - Extended mixed models to include plot-level residuals in addition to square-level random effects.
  - Both square- and plot-level analyses can be embedded within bootstrapping to derive standard errors.

- Model specification and practical considerations
  - General form for square-level data: y_ijk = a_ik + s_ij + e_ijk, with a_ik (fixed effects), s_ij (square random effects), e_ijk (repeated-measures errors).
  - Random effects: variances/covariances can be large in number; to keep models tractable, assumptions reduce parameters (e.g., common variance across surveys; AR1 autocorrelation for repeated measures).
  - AR1 model chosen to balance stability, speed, and robustness; bootstrap used for standard errors to maintain robustness against distributional mis-specification.
  - For non-normal data or highly non-normal variables (e.g., standing water), original methods may be retained if modelling convergence issues arise.

- Model testing: Broad Habitats
  - Historically, Broad Habitats were tracked via stock and then change; inconsistencies occurred when comparing stock-derived changes to repeat-squares changes.
  - Using AR1 mixed models, stock and change estimates become consistent; differences between old and new methods generally fall within old inconsistencies.
  - Analyses across 1984, 1990, and 1998 Broad Habitats validated the modelling approach; findings broadly align with earlier discrepancies but under a consistent framework.

- Implications and limitations
  - The modelling approach is computationally intensive, especially for large numbers of variables; AR1 with bootstrap provides a practical balance.
  - Estimates for any single survey are influenced by information from all surveys; older–new survey results may be revised as new data accrue.
  - Fixed effects (stock/change) are robust to model variation; variance/covariance parameters are sensitive to distributional assumptions, so bootstrap is preferred for SEs.
  - Non-normal data can lead to convergence issues; in such cases, results may adhere to the older method or require careful interpretation.
  - Results are presented on the original measurement scale; transformations would complicate back-transformations for fixed and random effects.

- Practical outcomes for monitoring frameworks
  - Provides a coherent, data-utilising approach that fully leverages hierarchical structure and all available information to produce more precise, consistent indicators of environmental stock and change.
  - Introduces a standard, automatable modelling framework (AR1 with bootstrap) suitable for large-scale, multi-survey monitoring programs.
  - Highlights importance of data governance aspects (data sharing, metadata, and transparent uncertainty quantification) when moving to model-based estimation across time.

- References and further reading
  - Foundational works on EM algorithms and bootstrap methods cited to support modelling choices and inference.
  - Previous CS methodologies and reports referenced for context and validation of new approaches.