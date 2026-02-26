# Countryside Survey 2007: Description of the statistical methodology used for the analysis of Countryside Survey data

- Purpose and goal
  - Describe the statistical methodology used to analyze Countryside Survey (CS) data.
  - Compare previous CS methods with the 2007 changes, focusing on achieving consistent, efficient stock and change estimates over time.
  - Adopt modelling-based approaches to enable consistent estimation across surveys and to utilise all available data.

- Context and data structure
  - CS field data come from a stratified sample of 1 km squares on a GB grid; two sampling levels within each square (square-level and within-square plots).
  - Measurements include binary and continuous variables.
  - Land Classification stratification: GB Land Classes with country-specific classifications (45 classes in 2007: 21 England, 8 Wales, 16 Scotland), enabling country reporting and comparability.

- Old vs. new estimation approaches
  - Old method
    - Stock estimates used all data from a given survey.
    - Change estimates used only repeated measurements across survey pairs.
    - Led to inconsistencies: stock and change estimates could conflict due to using different data subsets.
  - New modelling approach (CS 2007)
    - Uses a single modelling framework to estimate both stock and change, ensuring consistency and efficiency.
    - Employs mixed effects/repeated measures models to account for data hierarchy and missing data.
    - Utilises all available information, improving precision; future surveys can refine past estimates.

- Modelling framework and data levels
  - Square-level data
    - Treated as repeated measures across surveys within Land Classes.
    - Fixed effects: land-class means by survey (stock estimates).
    - Random effects: square-level deviations; survey-to-survey deviations allowed to be correlated.
    - Core model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land-class means per survey), s_ij as square random effects, e_ijk as repeated-measures error.
  - Plot-level data
    - Within-square plots add another hierarchical layer.
    - Previously analyzed with varied approaches; current method extends the square-level model to include plot-level random effects (and a plot residual), while preserving the bootstrapping approach for standard errors.
  - Model simplifications to ensure feasibility
    - Full random-effects parameterization is large; to keep models stable and computable, assumptions are made to reduce the number of random parameters (e.g., AR1 structure, common variances across surveys).
    - AR1 (autoregressive order 1) structure reduces the covariance parameters while keeping essential temporal correlation.
    - Fixed effects remain robust to reasonable misspecifications of random-effects distributions; bootstrap is used for standard errors to preserve robustness.

- Parameter types and distributions
  - Fixed effects: stock estimates (land-class means per survey) and derived changes.
  - Random effects: square-level and plot-level deviations; variances and covariances.
  - Assumptions: normality for random effects (subject to validation); AR1 covariance reduction; bootstrap used for standard errors to mitigate distributional concerns.

- Model testing and validation
  - Broad Habitats (stock and change for habitat categories) previously showed inconsistencies when using old methods.
  - Modelling approach applied to 1984, 1990, and 1998 Broad Habitat data showed consistent estimates; changes equaled the differences between successive stock estimates in line with the model design.
  - Comparisons between old and new methods generally showed differences within the bounds of previous inconsistencies; most changes were small and not statistically significant.
  - The modelling approach was also validated for soil (plot-level) and was extended to stack across square and plot levels for consistency.

- Practical considerations and limitations
  - Computational demands: modelling with bootstrapped standard errors is time-consuming; AR1 models strike a balance between precision and practicality.
  - Robustness: fixed-effect estimates are robust to moderate misspecification of random-effects distributions; variance-covariance parameters are more sensitive.
  - Non-normal data issues: some variables (e.g., standing water) exhibited non-normality; in such cases, old methods or alternative treatments may be used if necessary.
  - Updating past results: because analyses incorporate data from all surveys, estimates for past surveys can be revised as new data arrive; this differs from the prior reporting approach where earlier results were fixed.
  - Overall benefit: the modelling approach makes full use of hierarchical data, yields more precise estimates, and provides a consistent framework applicable across square and plot data.

- Implications for Countryside Survey reporting
  - For CS 2007 and beyond, adoption of the modelling approach yields more precise, consistent stock and change estimates by utilising all information and respecting data structure.
  - While it introduces updates to prior estimates as new data arrive, this reflects improved inference rather than errors in the earlier analyses.
  - The methodology supports automated application to large numbers of variables, enabling scalable, robust environmental monitoring and policy assessment.

- References and further information
  - References include foundational works on mixed models, bootstrap methods, and prior CS methodology reports.
  - For more information on Countryside Survey, see the project office contact details and website.