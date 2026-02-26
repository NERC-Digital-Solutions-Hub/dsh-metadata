# Description of the statistical methodology used for the analysis of Countryside Survey data

## Executive summary
- The report describes the statistical methodology for Countryside Survey (CS) data analysis, detailing changes implemented for CS in 2007 to achieve consistent estimation of stock and change.
- Previous methods used all data for stock but only repeated measurements for change, causing inconsistencies between stock and change estimates.
- Modelling with consistent estimation (via mixed-effects/repeated measures) was found feasible and generally robust; differences from old methods are typically within existing inconsistencies.
- The 2007 CS adopts modelling approaches and bootstrap for uncertainty, increasing precision by using all available information and respecting data hierarchy.
- Implementing modelling is computationally intensive; AR1 mixed-effects models were chosen for practicality and robustness, with checks comparing new and old methods.
- Results can update previous estimates as new survey data are added, reflecting improved information, but not all reporting occasions will be strictly consistent across time.

## What CS methodology changes aim to achieve
- Move from inconsistently combining stock (all squares) and change (repeat squares) estimates to a consistent estimation framework.
- Use all available data across surveys to improve precision of both stock and change estimates.
- Provide estimates that are robust to missing data and the hierarchical structure of CS sampling.

## Data structure and sampling
- CS data are drawn from a stratified sample of 1 km squares on a 15 km GB grid; each square is mapped and measured at two levels: square-level and within-square plot-level data.
- Measurements vary (binary and continuous) and are organized by Land Classes defined differently for each country (England, Wales, Scotland).

## Estimation approaches
- Old approach: stock estimates used all data from a survey; change estimates used only repeated measurements, leading to potential inconsistencies.
- New approach: modelling-based consistent estimation using all surveys; estimates stock and change jointly via fixed effects (means by land class across surveys) and random effects (square and plot level variation).
- Two main estimation philosophies discussed:
  - Stock-change as difference between stock estimates (robust but potentially less efficient, especially when correlations across surveys are high).
  - Modelling approach that yields consistent, efficient estimates of both stock and change.

## Modelling basics and structure
- Mixed-effects/repeated measures framework is used to handle incomplete data across surveys.
- General square-level model: y_ijk = a_i,k + s_ij + e_ijk
  - a_i,k: fixed effects representing land-class means at survey k
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects are assumed normally distributed with land-class-specific variances; residuals can have covariances across surveys.
- The model must balance many random parameters with relatively few observations per land class; hence simplifications are needed.

## Reducing model complexity: AR1 approach
- To keep models tractable, two key simplifications are adopted (the AR1 model):
  - Random effects variances are assumed constant across surveys for a given land class.
  - Covariances between successive surveys follow a first-order autoregressive (AR1) structure, reducing the number of covariance parameters.
- This AR1 assumption reduces the total number of random effect parameters to three per survey, regardless of the number of surveys.
- Bootstrap is used to estimate standard errors, providing robustness to potential distributional misspecifications.

## Plot-level data considerations
- Plot-level data within each square can be incorporated by adding plot-level residuals; this extends the square-level model to capture within-square variation.
- Two forms are possible:
  - Include a plot-level random effect (plots nested within squares) to account for within-square correlation.
  - Treat plots within squares with their own residual structure, while still embedding the model in a bootstrap framework.

## Model specification and data handling
- The general modelling approach requires specifying distributions for random effects and residuals; however, the fixed effects (stock/change) remain robust to reasonable misspecifications.
- When necessary, data transformations to normality are avoided to keep results on original measurement scales, though this can complicate back-transformations of parameters.

## Significance testing and Broad Habitats
- Prior CS analyses used simple bootstrap-based significance without strong distributional assumptions.
- The modelling approach applied to Broad Habitat data (from 1984, 1990, and 1998) produced estimates that did not exhibit the inconsistencies of the old method.
- For each habitat, stock and change estimates are derived from the model; reported change over a period equals the sum of inter-survey changes implied by the stock estimates.

## Practical implications and limitations
- Benefits:
  - More precise estimates by leveraging all available data and respecting data hierarchy.
  - Consistent estimation of stock and change across surveys.
  - Applicability to square-level and plot-level data; supports automated application across many variables.
- Costs and challenges:
  - Modelling is technically slower than the old method; AR1 reduces but does not eliminate computation time.
  - Requires careful model selection and validation; fixed effects are robust, but variance/covariance parameters are sensitive to distributional assumptions.
  - Some variables with highly non-normal distributions (e.g., standing freshwater) can yield convergence issues; in such cases, older methods may be preferred for those variables.
  - Updates to past survey estimates occur when new data are added; estimates for earlier surveys may be revised, which is conceptually different from the old inconsistency-driven differences but expected as more information becomes available.
  - Large-scale automated implementation requires standardized checks to ensure consistency between new and old methods (CS2007 included parallel computations with both methods).

## Implications for monitoring practice
- The modelling approach enhances data utilisation and comparability over time, supporting longer-term environmental monitoring and policy assessment.
- Consistent, model-based estimates facilitate clearer interpretation of trends and policy performance across time and land classes.
- Analysts should anticipate updated past estimates as new surveys are processed, reflecting improved data integration rather than errors.

## Limitations and considerations for interpretation
- Results depend on distributional assumptions for random effects; bootstrap mitigates some risks but not all.
- Some variables may require specialized handling or remain better served by the traditional method, depending on data characteristics.
- Automated analyses require standardised model choices (e.g., AR1) and ongoing validation to ensure robustness across a wide range of variables.

## References and additional information
- Prior CS methods and reports are referenced (e.g., CS1990, Barr et al.; Haines-Young et al.; foundational EM algorithm and bootstrap literature).
- CS data and project information are available through the Countryside Survey project office and website.