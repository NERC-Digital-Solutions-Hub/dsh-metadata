# Statistical methodology for Countryside Survey data

- This technical report describes the statistical methodology used to analyse Countryside Survey (CS) data, detailing the legacy methods, the changes implemented for CS2007, and the implications of adopting a modelling-based, consistent-estimation approach.
- Key motivation for change: previous stock and change estimates were inconsistent because stock used all data from a survey while change used only repeated measurements; modelling with consistent estimation addresses these mismatches.

## Core findings of the executive summary

- Modelling to achieve consistency and efficiency is feasible and robust, with estimates typically within the range of old-method inconsistencies but more precise.
- The new modelling approach uses all available information (from all surveys) to produce stock and change estimates, improving precision and enabling outputs that benefit from information in preceding surveys.
- Implementation is technically challenging and more computationally intensive due to iterative model fitting, but results are more coherent across time.
- To guard against model-misspecification risks, results from the new modelling approach are checked against the old method; differences are generally small and within prior error bounds.
- Outputs for CS2007 emphasise timelines spanning from the first survey to the present, rather than only changes since the immediate predecessor, highlighting the consistency benefits of the modelling approach.
- The AR1 mixed-effects model, combined with bootstrap for standard errors, is recommended for large-scale automation across many variables due to its balance of robustness, simplicity, and computational practicality.

## Data structure and sampling

- Data come from a stratified sample of 1 km squares across GB, arranged within the ITE Land Classification framework.
- Each square provides measurements at two levels: square-level (covering the whole square) and plot-level (within the square) for various features.
- Land Classes vary by country (England, Wales, Scotland), with 21 English, 8 Welsh, and 16 Scottish classes in CS2007.

## Estimation methods

- Old method:
  - Estimates stock by combining means/SEs for each Land Class across all measurements.
  - Estimates change from repeated measurements only, leading to potential inconsistencies between stock and change estimates.
- New modelling method (consistent estimation):
  - Uses modelling to estimate stock and change simultaneously, applicable to both square- and plot-level data.
  - Treats missing information via advanced incomplete-data techniques (e.g., mixed models, repeated measures) rather than simply filling in missing values.
  - Requires distributional assumptions for random effects; uses bootstrap to obtain robust SEs.

## Modelling details

- Square-level data:
  - Model: y_ijk = a_ik + s_ij + e_ijk
    - a_ik: fixed effects (land-class means for each survey)
    - s_ij: square-level random effect
    - e_ijk: repeated-measures (within-square) residuals
  - Random effects (s_ij and e_ijk) have covariances and variances to be estimated; a full model is parameter-heavy.
  - To keep the model practical, random-effect parameters are reduced using structure (e.g., AR1 assumptions).
- Plot-level data:
  - Incorporates plot-level residuals in addition to square-level random effects.
  - Can be embedded in bootstrap procedures to obtain SEs.
- Model simplifications (AR1):
  - Assumes common variance across surveys within a land class and first-order autocorrelation for repeated measures.
  - Reduces the number of random-effect parameters to a manageable level (three per survey per land class).
- Model specification:
  - General form for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - Random effects (s_ij) and residuals (e_ijk) are normally distributed with land-class-specific variances and covariances.
- Estimation approach:
  - Fixed effects (stock estimates) are robust to some misspecification of random-effects distributions.
  - Variances/covariances are more sensitive; bootstrap is used to obtain robust SEs.

## Model testing and Broad Habitats

- Re-examined Broad Habitats using CS data from 1984, 1990, and 1998 to compare old vs new methods.
- Old method: stock vs. change estimates often inconsistent across time; change estimates derived from different data subsets were not aligned with stock differences.
- New modelling approach (AR1 with bootstrap) produced consistent estimates where changes matched the differences in stock, with all estimates largely within old-method error bounds.
- This analysis supported adopting the modelling approach for CS2007 and beyond, including plotting and soil data analyses.

## Limitations and implications

- Computational complexity: AR1 modelling with bootstrapping is slower than the old method, but still practical for CS-scale analyses.
- Model choice sensitivity: fixed-effect estimates (stock/change) are robust to distributional mis-specification, but variance/covariance estimates are more sensitive; bootstrap helps mitigate this.
- Non-normal data challenges: some variables (e.g., standing water) may cause convergence to local maxima, leading to reverting to older methods for those cases.
- Consistency across time: because analyses use data from all surveys, estimates for any single survey can be updated as new surveys add information; cross-time consistency across reporting occasions is not guaranteed in the same way as with the old approach.
- Practical benefit: the modelling approach better utilises all information and aligns with the data hierarchy, delivering more precise estimates and enabling more comprehensive data products and temporal analyses.

## Practical takeaways for data support and data products

- For end users and dashboards: expect more precise stock and change estimates and potential updates to historical survey estimates as new data are incorporated.
- When communicating results: explain that consistency is achieved through modelling rather than comparing stock and change across differing data subsets; include bootstrap-based standard errors to reflect non-normal data distributions.
- For automation: the AR1-based modelling with bootstrap is the recommended standard, balancing robustness and computational feasibility across many variables.
- For data quality and interpretation: ensure users understand the limitations around model assumptions, especially for variables with highly non-normal distributions.

## References and notes

- Core methodological references include CS1990, AR1 modelling approaches, Dempster et al. (1977) on EM-type methods, and bootstrap literature (Efron & Tibshirani, 1993).
- The CS2007 methodology was designed to be consistent with prior findings while providing a more efficient and robust framework for estimating stock and change.