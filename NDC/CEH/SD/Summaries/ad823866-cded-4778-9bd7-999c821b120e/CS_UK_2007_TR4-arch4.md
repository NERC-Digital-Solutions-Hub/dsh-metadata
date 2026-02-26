# Statistical Methodology for Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes implemented for CS in 2007.
- Previous methods used stock estimates from all data and change estimates from repeated measurements, causing inconsistencies between stock and change.
- Modelling methods for consistent estimation are feasible and robust, yielding estimates similar to prior methods but with improved precision.
- The new approach uses a modelling framework (mixed effects/repeated measures) and AR1 structure to obtain consistent and more efficient stock and change estimates across surveys.
- To handle non-normal data and derive reliable uncertainty measures, bootstrap methods are employed for standard errors and confidence intervals.
- The modelling approach, though computationally intensive, systematically uses all available information and the hierarchical data structure, improving precision and enabling updates to past estimates as new data arrive.
- Broad Habitat analyses confirm consistency between stock and change estimates under the new method, with differences generally within previous inconsistencies.
- Limitations include increased computational demands, sensitivity to distributional assumptions for variance components, and potential non-normality issues; results are reported on the original data scale, and cross-survey updating means past estimates may be revised slightly as new data are added.

## Introduction and Scope
- This technical report presents sampling and analysis procedures for Countryside Survey data, reviewing the previous methodology and detailing changes for CS2007.
- CS sampling uses a stratified sample of 1 km squares at a 15 km GB grid intersection; measurements occur at two levels within each square (square-wide and within-square plots).
- Land Classification (ITE) stratifies selection into country-specific classes (England, Wales, Scotland) with 45 classes in the 2007 scheme.
- Data types range from binary to continuous (e.g., areas, lengths), with the aim to produce robust regional/national estimates and associated uncertainties.

## Estimation, Bootstrapping, and Prior Methodology
- Old method: compute means and standard errors for each Land Class and combine via area-based weighting to estimate regional means or totals; stock used all data from a survey, while change used only repeated measurements, causing potential inconsistencies.
- Bootstrapping (from CS2000 onward) addresses non-normality and provides robust significance assessment for square-level data.

## Reasons for Modifications to CS Methodology
- Reported stock and change in earlier CS surveys appeared inconsistent due to differing data subsets used for stock (all squares) and change (repeated squares).
- The need to present results as timelines spanning multiple surveys highlighted the problem of non-additive inconsistencies between adjacent and non-adjacent survey changes.
- Modelling approaches (consistent estimation) were explored and found feasible and robust, offering improved efficiency by using all available data and modelling the data generation process.

## Modelling Basics and Data Structures
- Incomplete data techniques (EM-like mixed models) enable consistent stock and change estimation by leveraging information across all surveys and handling missing data coherently.
- Models are mixed effects/repeated measures, with fixed effects for stock/change across surveys and random effects capturing square-level and plot-level variability, plus correlations across surveys.
- The approach requires distributional assumptions about random effects; fixed effects are robust to some mis-specification, but variance-covariance components are more sensitive.

## Square Level Data
- For complete 1 km squares, data are modeled as repeated measures within Land Classes.
- Simple fixed effects: land-class means over surveys; square-level random effects capture square-specific deviations; repeated-measures residuals model within-square changes.
- Acknowledges the challenge of many random-effect parameters relative to data; computational efficiency drives model simplification.

## Plot Level Data
- Plot-level data within squares can be analyzed with extended models that include plot-level residuals in addition to square-level effects.
- Two modelling options exist: treating plots as independent within land classes or incorporating square-level variation; both can be embedded in bootstrap procedures.

## Model Specification
- General model for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means in survey k)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Random effects are typically assumed normal with land-class-specific variances; within-land-class covariances vary by survey and land class.
- Increasing surveys dramatically increases random-parameter counts; thus, reducing random effects is essential for stability and computability.

## Reducing Model Complexity: AR1 and Other Assumptions
- To keep models tractable, two key reductions are used:
  - Variance components are assumed constant across surveys within a land class (σ_i).
  - Covariance of repeated measurements across surveys follows an AR(1) process.
- Combining these yields an AR1 model with a small, fixed number of random-effect parameters per land class, regardless of the number of surveys.
- Bootstrap standard errors are recommended because variance-covariance estimates can be less reliable under these simplified structures.

## Model Testing – Broad Habitats
- Analyses of Broad Habitat data from 1984, 1990, and 1998 using both old and new methods showed inconsistencies with stock/change from the old method.
- AR1 modelling with bootstrap produced consistent stock and change estimates, with changes across periods aligning to sums of interval changes.
- When compared, differences between old and new methods generally fell within historical inconsistencies, supporting the adoptability of the modelling approach.
- The new approach was validated for plot-level and soil data, indicating broader applicability beyond square-level data.

## Limitations and Implications
- The AR1 bootstrap approach is computationally demanding but feasible; fixed-effect estimates are robust to some model variation, while variance components require careful consideration.
- Model selection is important; fully parameterised models are slow, so a standard AR1 model is favored for automated, large-scale analyses.
- Non-normal data can bias variance estimates; for highly non-normal variables, transformations complicate interpretation on the original scale.
- Some variables (e.g., standing water) showed convergence to local maxima with the new method; in such cases, results may reflect the old methodology.
- Because data from all surveys inform estimates, past survey estimates can be revised slightly as new data are incorporated, differing from the prior practice of static past estimates.
- Overall, the modelling approach makes fuller use of information and the data hierarchy, yielding more precise estimates and consistent interpretation over time, albeit at the cost of greater computational effort and careful distributional checking.

## References
- Barr et al. 1993; Haines-Young et al. 2000; Dempster, Laird, Rubin (EM algorithm); Efron and Tibshirani (bootstrap); Scott (2002) on maximum likelihood with empirical Fisher information.