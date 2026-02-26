# Statistical Methodology for the Countryside Survey 2007

## Executive Summary
- Describes the statistical methodology used for Countryside Survey (CS) data analysis, summarizing previous methods and detailing changes for CS 2007.
- Previous stock estimates used all survey data, while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling to achieve consistent estimation (using all data and linked stock/change) was found feasible and robust, with differences from old methods generally within existing inconsistencies.
- CS 2007 adopts a modelling approach for consistent estimation, improving precision by utilizing all available information and the hierarchical structure of the data.
- The modelling approach is more computationally intensive, requiring iterative fitting; practical implementation faced CS sampling complexity, but yielded a significantly improved product.
- Validation against earlier methods (through Broad Habitats and plot-level data) supported the feasibility and benefits of modelling; hence CS 2007 adopts the new methodology.
- The approach uses AR1-based mixed models and bootstrap for standard errors to maintain robustness, with comparisons between new and old methods conducted to ensure compatibility.
- Limitations include reliance on distributional assumptions for some parameters and the potential updating of past survey estimates as new data arrive; nonetheless, the approach aims for greater accuracy and consistency.

## 1. Introduction
- The report provides an overview of Sampling and Analysis procedures for Countryside Survey data, outlining the reasons for and details of 2007 estimation changes.
- It contrasts the new modelling-based approach with previous CS methodology and discusses limitations and implications.

## 2. Overview of Previous CS Methodology
- CS field data come from a stratified 1 km square sample on a 15 km GB grid; measurements occur at two levels within each square (square-wide and within-square plots).
- Land Classification (ITE) stratifies squares; classifications have evolved (GB: 32 → 42 → 45 classes with country-specific splits) to accommodate reporting needs (England, Wales, Scotland).
- Estimation: prior method computed region-wide means/standard errors by combining land-class estimates weighted by land area; assumed independence across Land Classes.
- Bootstrapping: significance testing for square-level data used bootstrap rather than normality assumptions due to skewness and non-normal distributions.

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies arose because stock used all data from a survey while change used only repeated measurements, causing mismatches between stock and change estimates.
- Presenting results across long timelines (from the first survey to the present) highlighted these inconsistencies; the feasibility of producing consistent estimates was investigated, prompting new estimation methods.
- Three potential approaches to consistency were considered, with modelling identified as the most capable of providing consistent and efficient estimates for both square and plot-level data.

## 4. Consistent Estimation

### 4.1 Possible Approaches
- Stock from all measurements with change from differences of stock estimates.
- Change from repeated measurements only.
- Modelling (mixed effects/repeated measures) to jointly estimate stock and change with consistency and efficiency.

### 4.2 Modelling Basics
- Incomplete data techniques (e.g., EM-type mixed models) enable consistent estimation but introduce distributional assumptions.
- Mixed-effects/repeated-measures models include fixed effects (stock/change as functions of surveys) and random effects (accounting for sampling structure).
- Consistency requires fitting models to data from all surveys; complexity increases with the number of surveys and random-effect parameters.

### 4.3 Square Level Data
- Data at complete 1 km squares are treated as repeated measures within Land Classes.
- A mixed-effects model: y_ijk = a_iK + s_ij + e_ijk, with fixed effects a_iK (land-class means across surveys), square random effects s_ij, and repeated-measures residuals e_ijk.
- Random effects are normally distributed with land-class-specific variances; repeated-measures have covariances that vary by land class and survey.
- The parameterization grows with the number of surveys; hence simplifications are used to keep the model tractable.

### 4.4 Plot Level Data
- Plot-level data within squares add hierarchical complexity; previous analyses either reduced to square level or treated plots as independent (potential biases).
- Mixed models can incorporate a plot-level random effect in addition to the square-level effect; both forms can be bootstrapped.

### 4.5 Model Specification
- General square-level model: y_ijk = a_iK + s_ij + e_ijk.
- Random effects: s_ij (square-level) and e_ijk (repeated-measures), with distributions that can vary by land class and survey.
- To manage complexity, two simplifying assumptions (AR1 structure and common variance across surveys) reduce random parameters to a practical number, enabling robust fixed-effect estimates.
- Bootstrap-based standard errors are used to preserve robustness when variance/covariance structures are simplified.

### 4.6 Model Testing – Broad Habitats
- Broad Habitat data across 1984, 1990, and 1998 were reanalyzed with modelling to assess consistency.
- Old method inconsistencies between stock and change were eliminated under the new modelling approach; changes calculated as differences in stock or via integrated models aligned with resulting stock estimates.
- Comparisons showed differences between old and new methods were generally within the range of prior inconsistencies, supporting adoption of consistent estimation.
- Additional analyses extended to soil data and plot-level data, confirming feasibility of consistent estimation across data types.

## 5. Limitations and Implications
- Implementing model-based analysis within a bootstrap framework is computationally demanding, but fixed-effect estimates (stock/change) are robust to model variation.
- Fully parameterised models are slow; AR1 models with bootstrap provide a practical balance of speed and robustness for large-scale CS analyses.
- The fixed-effect estimates remain robust even if random-effect distributions are mis-specified; however, variance/covariance estimates are more sensitive.
- Very non-normal data can cause convergence to local maxima (as seen with freshwater standing water), in which case old methodologies may be preferred for that variable.
- Using a consistent modelling approach leverages all available information and respects data hierarchy, likely yielding more precise estimates.
- A consequence of updating with new data is that past survey estimates may be revised; this is a natural outcome of integrating information across all surveys.

## 6. References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, Laird, Rubin (1977). EM algorithm for incomplete data.
- Efron, Tibshirani (1993). Bootstrap.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation using the empirical Fisher information matrix.