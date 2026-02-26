# Countryside Survey 2007: Statistical Methodology

## Overview
- Describes the statistical methods used to analyze Countryside Survey (CS) data and the changes introduced for CS2007.
- Moves from previous robust but inconsistent stock/change estimation to a modelling approach that provides consistent, efficient estimates for both stock and change across surveys.
- Uses data from all surveys (not just the latest) and incorporates the hierarchical CS sampling structure (squares and plots) to improve precision.
- Employs bootstrapping to obtain robust standard errors and significance in the presence of non-normal data distributions.

## Background: previous methodology and its limitations
- Previous approach: compute means/standard errors by Land Class and combine to regional totals; stock used all data from a survey, change used repeated measurements only.
- This created inconsistencies: stock and change estimates could differ and not align across adjacent or non-adjacent survey years.
- Reporting focus shifted in CS2007 from adjacent-survey changes to timelines spanning from the first survey to the present, highlighting inconsistencies under the old method.

## The modelling solution: consistent estimation
- Modelling approach uses mixed/EM-type models to estimate stock and change in a unified framework, producing consistent and more precise estimates.
- Requires distributional assumptions and more computing time, but offers improved use of all information and data hierarchy.
- Uses bootstrap to obtain standard errors, accommodating non-normal data and ensuring robust inference.

## Data structure and modelling at square and plot levels
- Square-level data:
  - Treated as a repeated-measures (mixed) model with fixed effects for land class and survey/year, and random effects for squares within land classes.
  - Stock estimates come from fixed effects; change estimates are derived as differences in fitted stock across surveys, ensuring consistency.
- Plot-level data:
  - Recognizes hierarchical structure: plots within squares within land classes.
  - Earlier approaches either collapsed to square level or treated plots as independent; current approach extends mixed models to include plot-level residuals and, where feasible, embeds plotting variation into bootstrapping.
- Practical modelling: to keep the model tractable, variance/covariance parameters are reduced (e.g., AR1 structure for repeated measures and common variance across surveys), balancing model complexity with stability and computing efficiency.

## Model specification and practical considerations
- Core model form (square level): y_ijk = a_ik + s_ij + e_ijk, with fixed effects a_ik (land-class means across surveys), square random effects s_ij, and repeated-measures residuals e_ijk.
- Random effects are assumed normal with land-class-specific variances; within-square correlations across surveys are modeled.
- AR1 simplification reduces random-parameter dimensionality to a manageable level (three random-effect parameters per land class, regardless of number of surveys).
- While fixed effects are robust to some mis-specification, variance/covariance estimates are more sensitive; bootstrapping is used to obtain reliable standard errors.

## Validation: Broad Habitats and other data
- Reanalyzed Broad Habitats data (1984, 1990, 1998) to compare old vs. new methods.
- Modelling approach produced consistent stock and change estimates; differences from old methods generally small and within bootstrap uncertainty.
- Found that, where differences existed, old-method discrepancies often exceeded those from modelling, especially forchange estimates based on repeated squares.
- Extended consistency checks to soil (plot-level) and other datasets, supporting the feasibility of applying consistent estimation across data types.

## Limitations and implications
- Computationally intensive; AR1-based modelling is slower than the old approach but still practical for CS-scale analyses.
- Model choice matters: AR1 is robust, stable, and efficient for large numbers of variables; more complex models may be slower and less reliable in practice.
- Distributional assumptions for random effects can affect variance estimates; bootstrap provides more robust standard errors.
- When new data are added, past survey estimates can be updated; this yields more precise past estimates but means cross-report consistency across multiple reporting times is dynamic rather than fixed.
- The approach leverages all available information and the data hierarchy, yielding more precise estimates, but requires automated, repeatable analyses for numerous variables.

## Practical implications for data use and products
- Enables self-serving data products with consistent stock and change estimates across time and geography.
- Produces more precise estimates by incorporating data from all surveys and acknowledging hierarchical data structure (squares and plots).
- Outputs are model-based estimates with bootstrap confidence intervals, suitable for policy and planning analyses where consistency and precision matter.
- Outputs may update previous findings as new surveys are incorporated, reflecting new information while maintaining methodological integrity.

## References and further reading
- References to CS1990 methods, bootstrap procedures, and AR1 modelling are provided to support the methodological choices and validation.
- Links to Countryside Survey project and key methodological papers are included for deeper technical detail.