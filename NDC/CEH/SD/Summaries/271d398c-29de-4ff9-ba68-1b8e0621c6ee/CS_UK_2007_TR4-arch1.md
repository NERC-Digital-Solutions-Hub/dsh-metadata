# Statistical methodology for Countryside Survey data

- This technical report describes the statistical methodology used to analyze Countryside Survey (CS) data, summarises previous methods, and details the changes implemented for CS in 2007.
- It shows how a modelling approach based on consistent estimation was found to be feasible and robust, offering more precise estimates than previous methods.
- The report discusses the trade-offs of introducing distributional assumptions, the use of bootstrap for significance, and the need to check results, especially for small data subsets.
- A key outcome is the adoption of a modelling framework (AR1 mixed-effects/repeated-measures models) that utilizes all available information and preserves consistency between stock and change estimates across surveys.

## Introduction

- Countryside Survey data are collected from a stratified sample of 1 km squares arranged in a 15 km GB grid, with measurements at two levels: square-wide and within-square plots.
- Land Classification (ITE) underpins stratification, with country-specific classifications (England, Wales, Scotland) and 45 Land Classes in CS 2007.
- The basic estimation method previously produced means and standard errors by Land Class and combined them by area weighting; stock used all data from a survey, while change used only repeated measurements, causing inconsistencies.

## Previous methodology and issues

- Stock and change estimates could be inconsistent because they were derived from different data sets (all-square data for stock vs. repeat-square data for change).
- The old approach maximised information for stock but relied on robust but less efficient methods for change, leading to interpretive inconsistencies between adjacent and non-adjacent survey comparisons.
- There were notable discrepancies when reporting changes over longer timescales, even though local inconsistencies were understood within the context of the standard errors.

## The new modelling approach

- Modelling with consistent estimation uses data from all surveys to estimate both stock and change, improving precision and coherence between estimates across time.
- This approach is applicable to both square-level and plot-level data, providing a unified framework for analysis.
- It introduces additional assumptions about data distributions, which necessitate validation through comparisons with the old methodology.

## Data structures and modelling details

- Square-level data: treated as repeated-measures within Land Classes; a mixed-effects model is used with fixed effects for Land Class means across surveys and random effects for squares and repeated measures.
- Plot-level data: recognizes hierarchical structure within squares; models can include plot-level random effects in addition to square-level effects, both embedded in bootstrapping.
- Model specification (general form): y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (Land Class means for survey k)
  - s_ij: square-level random effects
  - e_ijk: repeated-measures residuals
- Distributional assumptions: random effects and residuals are typically assumed normal; variances/covariances vary by Land Class and survey.
- Dimensionality and practicality: full random-effects models become very parameter-heavy with many surveys; therefore, reduction strategies are used.
- AR1 simplification: common approach sets a small, fixed number of random parameters by assuming:
  - Equal random-effect variances across surveys within a land class
  - An autoregressive (AR1) structure for covariances across successive surveys
- Bootstrap: used to obtain standard errors and confidence intervals for fixed effects, helping to guard against non-normality and model misspecification.
- Model testing: Broad Habitats (e.g., seven habitat categories) were re-analyzed to compare old and new methods; results showed consistency with old estimates within their typical discrepancies, supporting adoption of the modelling approach.

## Limitations and implications

- Modelling plus bootstrap is computationally intensive; fully parameterised models are slow, so a balance (AR1 with bootstrap) is preferred for large numbers of variables.
- Fixed-effect estimates (stocks and changes) are robust to some misspecification of random effects, but variance/covariance estimates are more sensitive.
- Very non-normal data (e.g., standing water) can lead to convergence issues or local maxima; in such cases, older methodologies may be retained for those variables.
- Using data from all surveys means past survey estimates can be revised as new data are added; estimates for earlier years may be updated slightly, which is conceptually distinct from the previous inconsistencies.

## Practical considerations and adoption

- The AR1 model with bootstrap was selected for CS 2007 due to its stability, relatively fast fitting, and robust fixed-effect estimates.
- To ensure reliability, CS analyses were implemented to produce results using both the new and old methods for comparison, with differences typically within existing discrepancies.
- The approach is designed to be automated for large-scale use across many variables, though model selection and checking remain important for accuracy.
- The methodology is intended to be applicable to both square- and plot-level data, enabling consistent estimates across data types and future surveys.

## References

- Barr et al. (1993); CS 1990 Main Report
- Dempster, Laird, Rubin (1977); EM algorithm
- Efron, Tibshirani (1993); Bootstrap
- Haines-Young et al. (2000); Accounting for nature: assessing habitats in the UK countryside
- Scott (2002); Maximum likelihood estimation using the empirical Fisher information matrix