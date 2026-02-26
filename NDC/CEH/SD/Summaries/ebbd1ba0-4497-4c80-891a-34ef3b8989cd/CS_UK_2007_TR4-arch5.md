# Countryside Survey 2007 Statistical Methodology

- Purpose and scope
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data for 2007.
  - Explains why methodological changes were made from previous CS analyses and how these changes improve consistency and precision.
  - Documents the implications for data governance, reporting, and future dataset updates.

- Why changes were needed
  - Previous methods used stock estimates from all data in a survey and change estimates from repeated measurements, causing inconsistencies between stock and change.
  - Inconsistencies arose when comparing adjacent surveys and when reporting changes over longer timelines.
  - Modelling approaches using consistent estimation across stock and change were investigated and found feasible and robust, particularly when using data from multiple surveys.

- Modelling approach and key features
  - Uses consistent estimation via mixed effects and repeated measures models to analyze data from all CS surveys.
  - Aims to utilize all available information (square and plot level data) and properly reflect the data hierarchy.
  - Square level data: treated as repeated measures within land classes; fixed effects capture land class means across surveys; random effects account for square-level variation and survey-to-survey correlations.
  - Plot level data: extended models to include plot-level residuals; bootstrapping used to obtain robust standard errors.
  - Model specification (example): y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land class means across surveys), square random effects s_ij, and repeated-measures residuals e_ijk; random effects assumed normally distributed with land-class-specific variances.
  - Reduction of parameters: AR1 (auto-regressive) structure used to keep the number of random parameters manageable as the number of surveys grows; improves stability and fitting speed.
  - Bootstrapping: employed to obtain standard errors and confidence intervals robust to non-normality, particularly for square-level data.

- Practical implementation and challenges
  - Implementing a modelling approach across many analyses is technically demanding and computationally intensive.
  - AR1 model with bootstrap provides a balance between robustness and feasibility for large-scale CS analyses.
  - Analyses were run in parallel with the old methodology to validate results; differences were generally small and within previous uncertainties.

- Data consistency, reporting, and implications
  - Modelling yields consistent stock and change estimates across survey intervals, improving internal coherence of time-series data.
  - Results for any single survey are influenced by information from all surveys due to the joint modelling approach; past estimates may be updated as new data become available.
  - This updating is a natural consequence of using all-survey information and reflects improvements rather than errors in earlier reports.
  - Documentation and metadata need to capture: modelling approach, assumptions, data structure (square/plot level), land-class classifications, and bootstrap methods to ensure reproducibility and clear audit trails.

- Validation and scope of application
  - Tested with Broad Habitat data (seven habitats) across 1984, 1990, and 1998; yielded consistent estimates and resolved previous stock-change discrepancies.
  - Extended validation with soil data (1978, 1998) and plot-level data confirmed feasibility of consistent estimation at multiple data granularities.
  - Adopted as the primary analysis method for the 2007 CS, with careful checks against old methods to ensure results remain within prior uncertainty bounds.

- Limitations and considerations for data governance
  - Model-based standard errors depend on distributional assumptions; bootstrapping mitigates some risks but model selection remains important.
  - Very non-normal data can lead to convergence or estimation issues for some variables (e.g., standing water in freshwater data led to preferring the old method for that variable).
  - While more efficient and precise, the approach requires transparent reporting of model specifications, data preparation, and the updating behavior of past estimates as new surveys are added.

- Implications for data management and usability
  - Encourages comprehensive metadata documenting: sampling design (1 km squares, 15 km grid), land-class classifications, levels of data (square and plot), data transformations, and the modelling framework (AR1, random effects structure).
  - Supports improved data discoverability and reuse by providing coherent, time-consistent stock/change trajectories across surveys.
  - Highlights the need for versioning and clear documentation when updating past survey estimates as new data arrive.

- References and workflow notes
  - Builds on prior CS methodology and statistical literature on mixed models, repeated measures, and bootstrapping.
  - Emphasizes automated, scalable application of a standard modelling approach across a large number of variables to support ongoing CS analyses.