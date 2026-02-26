# Statistical Methodology for Countryside Survey Data

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data and the changes implemented for CS in 2007.
- Old methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling for consistent estimation using all available data is feasible and, in practice, yields estimates close to old methods but with improved precision.
- The new modelling approach requires distributional assumptions and more computational effort, so results are validated by comparing with the previous method.
- In CS2007, a modelling framework (AR1 mixed models with bootstrap) is adopted, improving efficiency and allowing consistent estimation for both square- and plot-level data.
- While more data and complexity improve estimates, they also mean past estimates can be updated as new surveys occur; this reflects the integrated use of information across surveys.
- The AR1 model was chosen for practicality, stability, and robustness, with bootstrap used to obtain robust standard errors.
- The approach was tested on Broad Habitat data and found to resolve prior inconsistencies, supporting adoption for CS2007.

## Data and Sampling
- CS data come from a stratified sample of 1 km squares across GB, defined by the ITE Land Classification.
- Two levels of sampling: square level (whole square) and within-square plot level (features within the square).
- Land Classification evolved: GB 32 classes originally; CS2000 used 42; CS2007 uses 45 classes, with separate national classifications (England, Wales, Scotland) for country reporting.

## Estimation and Bootstrapping
- Previous estimation involved calculating means and standard errors for each Land Class and combining them (weighting by land area) to obtain regional/national estimates.
- Bootstrapping is used for square-level data to obtain significance without assuming normality (addresses skewness in some features).

## Reasons for Methodology Modifications
- Inconsistencies arose because stock and change estimates used different data subsets; stock used all squares, change used repeated squares only.
- To address this, modelling methods were explored to achieve consistent estimates for stock and change across surveys.
- Modelling approaches (instead of traditional methods) can provide consistent and more efficient estimates, though they introduce additional assumptions about data distributions.

## Modelling Approach
- The goal is consistent estimation of stock and change by leveraging data from all surveys in a hierarchical framework.
- Mixed effects/repeated measures models are used to handle incomplete data and the hierarchical sampling design.

### Square Level Data
- Treated as repeated measures within Land Classes; a fixed-effects regression models land-class means across surveys.
- Random effects capture square-level deviations within each Land Class.
- Observations for a given square across surveys are correlated; the model accounts for this structure.

### Plot Level Data
- Plot-level data within squares can be incorporated with additional plot-level residuals, preserving the square-level structure while allowing plot-level variation.
- Models can embed plot-level random effects and square-level random effects, with bootstrapping used to obtain reliable standard errors.

### Model Specification
- General model for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means across surveys)
  - s_ij: random square effect within land class
  - e_ijk: residual (repeated measures) effect
- Random effects (s_ij, e_ijk) are assumed normally distributed with land-class-specific variances; covariances across surveys are modelled.
- To control the number of random parameters (which grows with the number of surveys), two simplifying assumptions are used:
  - Variances are constant across surveys within a land class (σ_i depending on land class, not survey).
  - Covariances follow an autoregressive AR1 structure across surveys, reducing repeated-measures parameters to a single value per land class.
- AR1 plus bootstrap is preferred for robust standard errors, given potential non-normality and model complexity.

### Model Testing - Broad Habitats
- Re-assessed Broad Habitat data (1984, 1990, 1998) with the new modelling approach.
- Old method produced stock and change inconsistencies; the AR1 modelling approach produced consistent estimates where stock minus change matched the inter-survey changes.
- Comparisons show differences between old and new methods generally fall within the prior method’s error bounds; modelling resolves prior inconsistencies.

## Limitations and Implications
- Computationally intensive; AR1 with bootstrap increases run time relative to older methods but remains feasible for CS-scale analyses.
- Fixed-effects estimates are robust to some mis-specifications of random effects distributions; however, variance/covariance parameters are more sensitive.
- For very non-normal data (e.g., standing water), the new method can converge to local maxima; in such cases, the old method may be preferred for that variable.
- Adopting a consistent modelling approach means past estimates can be revised as new survey data become available, reflecting the integrated use of accumulated information.
- A standard, automated AR1-based modelling approach is favored for large-scale CS analyses to balance robustness, efficiency, and practicality.

## Practical Takeaways for Analysts
- Use modelling with AR1 structure to obtain consistent stock and change estimates across multiple CS surveys.
- Employ bootstrap for standard errors to accommodate non-normal data distributions.
- Incorporate both square- and plot-level data within a hierarchical mixed-model framework to exploit all available information.
- Be aware that new data will refine historic estimates; communicate revisions as part of ongoing monitoring rather than treating past results as fixed.
- Validate modelling results against previous methods to understand deviations and ensure results stay within plausible bounds.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).