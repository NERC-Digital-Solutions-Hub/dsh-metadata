# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, summarising previous methods and detailing changes implemented for CS 2007.
- Previous estimation separated stock (all data from a survey) from change (repeat measurements only), which led to inconsistencies between stock and change estimates.
- Modelling consistent estimation via mixed effects/repeated measures was found to be feasible and robust, producing estimates close to or within the range of previous methods’ discrepancies but with improved precision.
- The new modelling approach uses all available information, improving efficiency and allowing improvements to past survey estimates as new data are collected.
- Implementation was technically challenging and computationally intensive, but ultimately yielded a more refined product.
- The modelling framework was tested against Broad Habitats data and other plot/square level datasets, confirming feasibility and consistency with earlier_CS results, while offering greater precision.
- A trade-off exists: model assumptions are more demanding, and some estimates for earlier surveys may be revised as the dataset grows; however, fixed effect estimates (stock/change) are robust to reasonable model variations and bootstrap procedures provide robust standard errors.

## Introduction and Aim
- The report provides a description of the statistical methodology for CS data analysis, reviews the previous CS methodology, and explains the changes made for CS 2007.
- Emphasises consistent estimation across the full time series to avoid mismatches between stock and change estimates.

## Overview of Previous CS Methodology
- Stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs.
- This caused mismatches: stock and change could point to inconsistent conclusions across time.
- Previous reporting focused on current survey and change since the immediately preceding survey, creating potential inconsistencies when comparing non-adjacent periods.

## Reasons for Modifications to CS Methodology
- Historical inconsistencies arose because stock and change were derived from different data subsets.
- Several approaches could yield consistency; modelling approaches (consistent estimation) were chosen because they can handle both square and plot level data and provide more precise estimates.
- Modelling aligns with the goal of reporting results that span multiple surveys, not just adjacent pairs.

## Modelling Basics
- Incomplete data techniques (e.g., mixed effects/repeated measures) allow consistent estimation across all surveys, using data from all available years.
- Models require assumptions about data distributions; fixed effects reflect stock/change values, while random effects capture meta-variability due to the sampling structure.
- Two data levels considered: square level (1 km squares) and plot level (within-square plots).

## Square Level Data
- Data treated as a repeated measures model with fixed effects for land classes and surveys, plus random square effects and correlated within-square deviations across surveys.
- Aims to produce consistent stock estimates per survey; change is derived from differences in these stock estimates.

## Plot Level Data
- Plot data within squares can be summarized at the square level or modelled directly, with attention to the hierarchical data structure.
- Models can include an additional plot-level random effect to account for within-square variation.
- Both square- and plot-level models can be incorporated into bootstrapping procedures to obtain standard errors.

## Model Specification and Practical Modelling Choices
- General square-level model: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik are fixed effects (land class means by survey),
  - s_ij are square-level random effects,
  - e_ijk are repeated-measures residuals.
- Random effects are assumed to be normally distributed with land-class-specific variances; repeated effects have covariances that vary by land class and survey pair.
- The full model becomes highly parameterised as the number of surveys increases; thus, simplifications are needed.
- Two practical reductions:
  - Variances (σ_ik) are assumed constant across surveys for a given land class.
  - An autoregressive AR1 structure is used for covariances across surveys, reducing repeated-measure parameters per land class to one.
- The AR1 model combined with bootstrap for standard errors (robust to distributional mis-specification) was investigated as a practical, robust approach for CS data.

## Model Testing – Broad Habitats
- Re-analyzed Broad Habitat data (1984, 1990, 1998) with both old (non-modelled) methods and the new modelling approach.
- Old method produced inconsistencies between stock and change; the AR1 modelling approach produced consistent stock/change estimates that matched the implied changes from consecutive periods.
- Comparisons showed differences between methods largely within the previously observed inconsistencies; the modelling approach provided a more coherent framework.
- Additional consistency checks extended to soil data (1978 vs. 1998) and plot data, confirming feasibility and consistency across data types.
- Based on results, CS adopted the new modelling methodology for 2007 analyses.

## Limitations and Implications
- AR1 modelling with bootstrap is computationally intensive; full parameterised models can be slow or unstable for large numbers of variables.
- The AR1 approach offers robustness and a reduced parameter set, but variance/covariance parameters remain sensitive to distributional assumptions; bootstrap helps mitigate this.
- Model selection and checking are important; for large-scale CS analyses, a standard, automated AR1-based pipeline was favored to balance robustness and practicality.
- Results are tied to data from all surveys; adding new surveys can revise past estimates, which is conceptually different from prior static reporting but reflects increased use of all available information.
- Non-normal data can pose convergence and estimation challenges (e.g., very non-normal freshwater standing water data were better served by the old method in that specific case).

## Implications for Monitoring Frameworks
- Demonstrates the value of modelling approaches that exploit hierarchical data structures to produce consistent, efficient estimates over time.
- Highlights trade-offs between methodological complexity, computational requirements, and interpretability of results for policy monitoring.
- Emphasises the importance of robust uncertainty estimation (e.g., via bootstrapping) when distributional assumptions are uncertain or violated.
- Underlines the potential for past survey estimates to be updated as new data become available, enhancing long-term monitoring continuity while requiring careful communication of changing baselines.