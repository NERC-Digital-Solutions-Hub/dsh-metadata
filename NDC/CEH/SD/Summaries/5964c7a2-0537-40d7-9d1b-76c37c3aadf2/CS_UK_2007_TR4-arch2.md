# Countryside Survey 2007 Statistical Methodology

- Aim
  - Describe the statistical methodology used to analyse Countryside Survey (CS) data and detail changes implemented for analysis of CS data in 2007.
  - Move from method that could produce inconsistencies between stock and change estimates to a modelling approach that yields consistent, more precise estimates across surveys.
  - Use all available information, with robust handling of missing data, and present outputs in standard formats (e.g., stock/change estimates, confidence measures).

- Data and sampling design
  - Data come from a stratified sample of 1 km squares on a GB-wide 15 km grid.
  - Two sampling levels within each square: square-level measurements and plot-level measurements within squares.
  - Measurements include binary and continuous variables; Land Classification used for stratification (GB classes evolving to 45 classes by CS2007, with national classifications for England, Wales, Scotland).

- Estimation: old approach vs modelling approach
  - Old method: stock estimates used all data from a survey; change estimates used only repeated measurements between surveys, causing inconsistencies between stock and change.
  - New method: modelling-based, producing consistent and efficient stock and change estimates by using data from all surveys and accounting for missing information.
  - Bootstrapping is used to derive standard errors and confidence intervals, accommodating non-normal data distributions.

- Modelling approach and rationale
  - Modelling allows consistent estimation for both square and plot level data, improving precision by using hierarchical data structures.
  - Requires distributional assumptions about data; results are validated against the previous method to ensure plausibility.
  - Implemented with a mixed effects/repeated measures framework; fixed effects relate to stock/change across surveys, random effects capture the sampling structure.

- Square-level data modelling
  - Data treated as repeated measures within land classes; model components:
    - Fixed effects: land-class means across surveys.
    - Random effects: square-level deviations (and their correlations over surveys).
  - General form: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects, s_ij as square random effect, e_ijk as repeated-measure residuals.
  - Random effects are assumed normally distributed with land-class-specific variances; correlations across surveys are modelled.

- Plot-level data modelling
  - Plot data within squares can be modelled by extending square-level models with an additional plot-level residual.
  - Accounts for variation among plots within squares and their correlation across surveys.
  - Can be embedded within bootstrapping to obtain robust standard errors.

- Model specification and parameter reduction
  - To control complexity, several reductions are used:
    - Variance parameters may be assumed constant across surveys or land classes.
    - Autoregressive AR1 structure reduces repeated-measures covariance parameters to a small set per land class.
  - AR1 model plus bootstrap chosen for balance of robustness, efficiency, and practicality for large numbers of analyses.
  - Fixed-effects estimates are relatively robust to distributional mis-specification; variance/covariance parameters are more sensitive.

- Model testing: Broad Habitats
  - Historic CS outputs include stock and change for Broad Habitats (using square-level proportion data).
  - Comparisons show modelling eliminates prior stock/change inconsistencies; estimates across surveys become coherent.
  - For extensive habitats, differences between old and new methods generally fall within old method inconsistencies.
  - Extends to plot-level and soil data, supporting a unified, consistent approach.

- Limitations and implications
  - Computationally intensive; AR1 offers a practical, robust solution with a manageable number of random parameters.
  - Estimates for a given survey can be revised as new data from later surveys become available; updates reflect new information rather than errors.
  - Non-normal data or extreme distributions (e.g., standing water) can pose convergence or estimation issues; in some cases, older methods may be used for those variables.
  - Results are presented on the original measurement scale; transforming scales can complicate interpretation due to mixed fixed and random effects.
  - Implications for data users include better precision and consistent interpretation across time, at the cost of longer run times and the need for automated, standardized modelling workflows.

- Practical implications for analysts and data management
  - Use of complete data across surveys improves the quality and precision of estimates; outputs can inform policy monitoring and environmental health assessments.
  - Bootstrapped standard errors provide robust significance testing without heavy reliance on normality assumptions.
  - Outputs (stock, change, and their uncertainties) are produced in clear formats (e.g., maps, charts) and stored/uploaded to appropriate data portals for accessibility.
  - Adoption of consistent methods across large numbers of variables supports comparative analyses over time and across habitats.

- References and context
  - Builds on prior CS methodology and literature (e.g., CS1990, Broad Habitat work, bootstrap methods, and EM-based incomplete-data techniques).
  - Methodological choices grounded in statistical theory (mixed models, repeated measures, AR1 structure) and practical considerations for large environmental monitoring programs.