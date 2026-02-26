# Statistical methodology for Countryside Survey data

## Overview
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, detailing changes implemented for CS in 2007.
- Balances prior robust but inconsistent estimation methods with a modelling approach that yields consistent, more precise stock and change estimates.
- Emphasizes validation against previous methods and the broader goal of using all available information.

## Data and Sampling
- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid; measurements occur at square and within-square (plot) levels.
- Land Classification is used to define strata; the classification evolved (GB → country-specific) resulting in 45 classes for CS2007 (England, Wales, Scotland split).
- Data types range from binary to continuous (areas, lengths).

## Estimation and Inference (Pre-2007 vs. 2007+)
- Old approach: stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- New approach: modelling techniques enable consistent estimation of both stock and change across surveys, using all available data.
- Bootstrapping is used for significance testing due to potential non-normality.

## Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock and change were derived from different data subsets.
- Three potential consistent estimation paths were considered; modelling emerged as the most robust and efficient for both square and plot level data.
- The shift aims to provide results that are internally consistent over time and across reporting horizons.

## Modelling Basics
- Incomplete data techniques (mixed effects/repeated measures models) are used to integrate data from all CS surveys.
- Models include fixed effects (stock/change as functions of land class and survey) and random effects (capturing square-level and repeated-measures variability).
- Reducing random-effect parameters is essential due to many land classes; assumptions are made to keep the model tractable while preserving fixed-effect robustness.

## Square Level Data
- Treats complete 1 km squares as the primary unit; uses repeated-measures mixed models.
- Basic form: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik are fixed effects (land-class means per survey),
  - s_ij are square-level random effects,
  - e_ijk are within-square repeated-measures residuals with survey-to-survey correlations.
- Variances and covariances are allowed to differ by land class and survey; AR1-like structure is used to control parameter growth.

## Plot Level Data
- Within-square plots provide additional information but previously were analyzed inconsistently.
- Extended models incorporate plot-level random effects in addition to square-level effects; can also be analyzed by aggregating to the square level with bootstrapping.
- Both square- and plot-level analyses can be embedded within bootstrap procedures.

## Model Specification and AR1 Approach
- General square-level model structure: y_ijk = a_ik + s_ij + e_ijk with distributional assumptions for random effects.
- To keep models practical (especially with many surveys), random-effect parameters are constrained:
  - Variances may be constant across surveys (σ_i) for a land class.
  - Repeated-measures covariances follow an AR1 structure (one covariance parameter per land class, per AR1 assumption).
- This AR1 specification reduces random-effect parameters to three per survey, regardless of the number of surveys.
- Fixed effects are robust to some mis-specification of random effects; bootstrap provides robust standard errors.

## Model Testing – Broad Habitats
- Re-examined Broad Habitat stocks and changes using the modelling approach across the 1984, 1990, and 1998 datasets.
- Demonstrated that modelling removes inconsistencies between stock- and change-based estimates observed with previous methods.
- Found that modelling estimates were generally within the old-method error bounds and often more precise.

## Limitations and Implications
- The AR1 bootstrap approach is computationally demanding but feasible; fixed-effect estimates are robust to some distributional mis-specification.
- Fully parameterised models are slow; the AR1 model offers a practical balance of speed and robustness for large-scale analyses.
- Model selection is important; in large analyses, a standard, automated AR1 approach with bootstrap is recommended.
- Some non-normal data (e.g., freshwater standing water) may produce convergence issues; in such cases, older methods may be retained for those variables.
- Using data from all surveys means estimates for any single survey can be updated as new data arrive; this shifts reporting semantics from fixed historical estimates to evolving estimates as information accumulates.

## Practical Implications for Analysts
- The modelling approach leverages the full hierarchical structure and all available data, yielding more precise estimates.
- Consistency is achieved across stock and change estimates, at the cost of requiring distributional assumptions and extra computation.
- Results for earlier surveys may be revised with new data, reflecting a dynamic, information-rich analysis process.
- Automated, standardised modelling (AR1 with bootstrap) is recommended for large-scale, multi-variable CS analyses.

## References
- Key sources include prior CS methodologies (Barr et al. 1993; Haines-Young et al. 2000), and foundational works on EM algorithms, bootstrap methods, and related statistical modelling.