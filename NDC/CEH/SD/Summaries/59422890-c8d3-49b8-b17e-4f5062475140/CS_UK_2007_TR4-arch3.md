# Statistical methodology used for the analysis of Countryside Survey data

- Purpose and scope
  - Describes the statistical methodology for analyzing Countryside Survey (CS) data.
  - Documents reasons for modifying the CS methodology for CS2007 and outlines the new consistent-estimation modelling approach.
  - Compares new modelling methods with the previous, largely robust but inconsistent, methods and discusses implications and limitations.

- Why changes were made
  - Previous methods: stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
  - Inconsistencies arose because different data subsets were used for stock and change across survey pairs.
  - Modelling (consistent estimation) uses data from all surveys to estimate stock and change jointly, producing internally consistent results and improved precision.
  - Validation: new modelling results were compared with old methods; differences generally fell within old method error bounds, with substantial improvements in precision anticipated from using all available information.

- Modelling approach and data structure
  - Applicable to both square-level and plot-level data; designed to handle CS’s hierarchical sampling (1 km squares within land classes; plots within squares).
  - Square-level data: treated as a repeated-measures/mixed-effects model with fixed effects for land-class means across surveys and random effects for squares and survey-related deviations.
  - Plot-level data: extended models include an additional plot-level residual/random effect to capture within-square plot variation; both square and plot level analyses can be embedded in bootstrapping.
  - Goal: obtain consistent and efficient estimates of stock (mean extent per land class per survey) and change (differences across surveys).

- Modelling specifics and parameter reduction (AR1 framework)
  - General square-level model: y_ijk = a_ik + s_ij + e_ijk, with a_ik as fixed effects (land-class means by survey), s_ij as square random effects, and e_ijk as repeated-measures residuals.
  - Random effects: variances and covariances of square and repeated measures are allowed to differ by land class; full models would have many random parameters and be unstable with CS’s data structure.
  - To keep models practical and robust, two simplifying assumptions (AR1 model) are used:
    - Random effect variances do not vary by survey (common per land class; σ_i).
    - Repeated-measures covariances follow a first-order autoregressive process (AR1), reducing covariance parameters to one per land class.
  - Result: three random-effect parameters per survey per land class, regardless of the number of surveys.
  - Estimation and inference:
    - Fixed effects (stock estimates) are estimated robustly; standard errors and confidence intervals are obtained via bootstrap.
    - Parametric standard errors can be unreliable for complex models; bootstrapping provides robust SEs.
  - Model testing and validation:
    - The AR1 modelling approach with bootstrap SEs was tested against Broad Habitats data and historical CS data, showing consistent results with improved precision without conflicting with earlier findings.

- Practical considerations and limitations
  - Computational demands: modelling is more time-consuming than older methods; full parameterized models are slow, so AR1 is favored for routine analyses.
  - Robustness: fixed-effect estimates are generally robust to moderate distributional mis-specifications; variance/covariance estimates are more sensitive.
  - Data quality and non-normality: non-normal data can affect estimates; bootstrap helps mitigate this; some variables with highly non-normal distributions (e.g., standing water) may still pose challenges.
  - Updating previous surveys: because analyses incorporate data from all surveys, estimates for earlier years can be revised when new data are added; this is a natural consequence of using a joint, all-surveys model.
  - Data sharing and metadata: the approach relies on combining data across surveys; consistent data governance, metadata, and data-sharing practices are important to ensure transparency and reproducibility.

- Key findings from applying the modelling approach
  - Consistent estimation is feasible and robust across Broad Habitat analyses and other data (including soil and plot-level data) and provides more precise estimates than old methods.
  - Differences between old and new methods generally fall within the old method’s error bounds; notable improvements occur in precision rather than large shifts in point estimates.
  - The modelling approach is recommended for CS2007 and beyond to achieve consistency across reporting intervals and to enable the use of all available information.

- Implications for monitoring practice
  - Adoption of a standard modelling framework enables automated, scalable analysis across many variables and surveys.
  - Results are inherently updated as new CS data become available, reflecting improved information; this is a deliberate shift from static, year-by-year reporting to a dynamic, integrated estimation approach.
  - The approach aligns with data governance goals by emphasizing transparent modelling assumptions, use of bootstrap for uncertainty, and explicit handling of data hierarchy.

- References and further reading
  - Key methodological references detailing CS sampling and estimation history, EM algorithm for incomplete data, and bootstrap techniques.
  - Foundational CS reports and methodological papers cited to underpin the modelling approach and its validation.