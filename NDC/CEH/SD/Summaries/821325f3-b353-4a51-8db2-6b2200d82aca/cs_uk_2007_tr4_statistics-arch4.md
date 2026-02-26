# Statistical methodology used for the analysis of Countryside Survey data

- Purpose and context
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
  - Moves from a robust but inconsistent legacy approach to a modelling-based, consistent estimation framework that uses all available data.

- Why the methodology changed
  - Previous methods produced stock estimates from all data in a survey but changed estimates from only repeated measurements, causing mismatches between stock and change and apparent inconsistencies across surveys.
  - Modelling demonstrated that consistent estimation of stock and change is feasible and robust, with results largely aligning with old methods within their inherent variability.

- Modelling approach and key concepts
  - Consistent estimation via modelling (AR1 mixed-effects framework) to derive stock and change from data across all surveys.
  - Benefits: uses all information, increases precision, and yields estimates that are internally consistent across time.
  - Trade-offs: introduces distributional assumptions about data; requires careful validation, especially for small subsets.

- Data structure and levels
  - Two-level sampling: 1 km squares within a 15 km GB grid; measurements at square level and within-square plots.
  - Land Classification (LC) used to stratify squares; country-specific LC classifications (England, Wales, Scotland) with alignment to a GB origin.

- Square-level modelling (core approach for complete squares)
  - Model framework: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects representing land-class means for survey k (stock estimates when scaled by LC area).
    - s_ij: square-level random effect (variation between squares within LC).
    - e_ijk: repeated-measures residual (variation within square across surveys).
  - Distributional assumptions: random effects are normal with LC-specific variances; residuals have LC- and survey-specific variances and covariances.
  - Challenge: many random-effect parameters; AR1 simplification reduces complexity.

- Plot-level modelling
  - Plot data within squares can be modelled with an additional plot-level random effect, enabling full hierarchical treatment.
  - Bootstrapping can be applied to obtain robust standard errors for fixed effects, accommodating complex variance structures.

- Model specification and parameter reduction (AR1 approach)
  - To keep models tractable, assume:
    - Within LC, random effect standard deviations are constant across surveys (σ_i).
    - Covariances follow an autoregressive (AR1) structure across successive surveys.
  - This reduces random-effect parameters to a manageable number (three per LC per survey in the AR1 setup), enabling automated application across many variables.

- Estimation and inference
  - Fixed effects (stock estimates) are relatively robust to distributional mis-specification.
  - Variance-covariance parameters are more sensitive to distributional assumptions; bootstrap standard errors are used for robust inference.
  - Analyses produce results on the original measurement scale; transformations are avoided to preserve interpretability.

- Validation and comparison to old methods
  - CS2007 results were compared with old methods; differences in stock/change estimates generally fell within the historical inconsistency range.
  - For Broad Habitats, modelling produced consistent stock and change estimates across 1984, 1990, and 1998 data, resolving prior inconsistencies.
  - Where non-normal data caused issues (e.g., standing water), old methodology results were retained to avoid biased estimates.

- Limitations and implications
  - Computational intensity: full parametric models are slow; AR1 offers a practical balance between speed and stability.
  - Model selection is important; fixed-effect estimates are robust, but variance/covariance estimates rely on assumptions.
  - When new survey data are added, estimates for earlier surveys can revise, reflecting the use of all available information; cross-report comparability over time can be affected.
  - The approach provides more precise estimates by leveraging hierarchical data and all available information, but requires careful communication of assumptions and potential revision of past results as data evolve.

- Practical implications for data leadership
  - Enhances data governance through transparent, model-based, consistent estimations across time, improving decision support for policy and planning.
  - Supports automation and scalability: a standard AR1-based modelling workflow can be applied to a large number of variables.
  - Improves discoverability and usability of results by providing precise, temporally coherent stock and change estimates derived from a unified framework.
  - Highlights the importance of metadata, documentation of model assumptions, and bootstrap-based uncertainty measures to enable informed interpretation by stakeholders.

- Context and references
  - Builds on established statistical foundations (mixed-effects models, repeated measures, and bootstrap methods) and CS history (tracking habitat stocks and changes across surveys).
  - Key references include works on bootstrap methods, EM algorithms for incomplete data, and prior Countryside Survey methodology publications.