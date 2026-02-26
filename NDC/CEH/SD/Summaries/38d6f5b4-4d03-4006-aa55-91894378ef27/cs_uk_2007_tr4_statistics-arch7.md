# Statistical Methodology for Countryside Survey Data (CS2007)

- The document describes the statistical methods used to analyze Countryside Survey (CS) data, focusing on changes introduced for the 2007 CS analysis.
- It contrasts previous robust but sometimes inconsistent methods with a new modelling approach that yields consistent estimation of stock and change across surveys.
- The new approach uses all available information from all surveys, leading to more precise estimates, and allows consistent estimation for both square and plot level data.
- Implementation is computationally intensive, requiring iterative model fitting and more computer time, but provides improved products for map-based data presentation and GIS analyses.
- Validation steps compare new modelling results with the old methodology to ensure results remain within prior uncertainty bounds.

## Context and Data Structure

- CS uses a stratified sample of 1 km squares on a 15 km GB grid; measurements are made at two levels: square level (covering the whole square) and within-square plot level.
- Measurements include binary and continuous variables (e.g., areas, lengths).
- Land classification (ITE) defines strata for square selection; classifications vary by country (England, Wales, Scotland), with country-specific class counts.
- The goal is to estimate stock (extent/area) and change over time for various features and habitats, and to present these through map-based outputs.

## Estimation Methods: Old vs. New

- Old method: means and standard errors calculated per Land Class; stock estimated using all data from a survey, change estimated from repeated measurements only. This caused inconsistencies where stock changes did not match changes between survey pairs.
- New method: modelling (consistent estimation) using data from all surveys to estimate stock and change simultaneously, producing coherent, robust estimates across time.
- Bootstrapping is retained for significance testing and to obtain confidence intervals, particularly for square-level data where distributions are skewed.

## Modelling Basics and Rationale

- The modelling approach relies on mixed effects and repeated measures models to handle incomplete data and the hierarchical CS sampling structure.
- Fixed effects represent Land Class means in successive surveys; random effects capture square-level and plot-level variation and their correlations across surveys.
- Model assumptions introduce distributional requirements; fixed effects are fairly robust to mis-specification, but variance/covariance components are more sensitive.
- Two modelling scales are used:
  - Square-level data: repeated measures mixed model with land-class fixed effects and square-level random effects.
  - Plot-level data: extended models accounting for within-square plot variation, with options to include plot-level residuals and correlations via bootstrapping.

## Model Specifications and Practicalities

- General square-level model: y_ijk = a_i_k + s_ij + e_ijk, where a_i_k are fixed land-class means by survey, s_ij are square random effects, and e_ijk are repeated-measures errors.
- Random effects are normally distributed with land-class-specific variances; within-square and cross-survey correlations are modelled.
- To manage complexity (many random effects with many surveys), several simplifications are used:
  - Assume random effect variances are constant across surveys for a land class.
  - Use an AR1 (first-order autoregressive) structure for repeated measures covariance, reducing the number of parameters to three per survey.
- Bootstrap standard errors are used to ensure robust inference, particularly when the variance-covariance structure is uncertain or non-normality is present.

## Model Testing: Broad Habitats

- Data from 1984, 1990, and 1998 Broad Habitats were used to test modelling versus old methods.
- Old method inconsistencies (stock vs. change) were evident when using repeated squares versus differences of stock estimates; modelling produced consistent estimates that matched the summed inter-survey changes.
- Comparisons showed that differences between old and new methods were generally small relative to prior uncertainty, with most estimates falling within old-method error bounds.
- Extending the modelling approach to plot-level data and soil datasets also supported feasibility and consistency, guiding adoption for the 2007 CS.

## Limitations and Implications

- The AR1 modelling with bootstrap is robust for fixed effects but sensitive to distributional assumptions for random effects; fully parameterised models can be slow, so practical use favours the AR1 approach.
- Some data (e.g., freshwater standing water) exhibited non-normality leading to convergence issues; in such cases, older methodology results may be retained.
- Adoption of a model-based, coherent approach means past survey estimates can be updated as new data become available, which is conceptually different from prior fixed inconsistencies and may slightly revise previous results.
- The approach better utilizes all information and the data hierarchy, improving precision and enabling consistent mapping outputs across surveys.

## Implementation and Outputs

- The modelling framework is designed for automated application to large sets of variables, balancing robustness with computational feasibility.
- Results support more precise mapping of stock and change over time, enabling GIS users to produce clearer, consistent map-based representations across multiple survey periods.
- Implementation involved extensive checks comparing old and new methods, ensuring that updated estimates remain reasonable within historical uncertainty.

## References and Documentation

- The report cites prior Countryside Survey methods and foundational statistical work (EM algorithm, bootstrap, etc.) and provides broader context for the Countryside Survey project timeline and reporting.
- For further information, the Countryside Survey project office and website are listed in the document.