# Statistical methodology for Countryside Survey data

- Executive Summary
  - Describes the statistical methodology used for Countryside Survey (CS) analysis and changes introduced for CS 2007.
  - Old methods were robust but caused inconsistencies: stock was estimated using all data from a survey, while change used only repeated measurements, leading to mismatches between stock and change estimates.
  - Modelling-based, consistent estimation is feasible and robust; differences from old methods are generally within the existing inconsistency range.
  - The 2007 CS adopted a modelling approach that uses all available information, producing more precise estimates; results for earlier surveys can be updated as new data become available.
  - Modelling is computationally intensive, requiring iterative fitting; practical implementation required addressing CS sampling complexity.
  - Validation involved comparing new modelling results with old methods; most changes were small and within prior uncertainty.
  - The AR1 mixed-effects modelling approach, combined with bootstrapped standard errors, was selected for square-level data due to robustness, efficiency, and scalability; plotting-level data can also be handled within this framework.
  - Adoption of consistent estimation across habitats and plot-level data (e.g., Broad Habitats) was demonstrated; CS 2007 uses the new methodology across data types.
  - Implications: estimates for any given survey can be influenced by information from all surveys; updating past results is expected as new data arrive; automation and standardization are essential for large-scale analyses.

- Introduction
  - This technical report outlines sampling and analysis procedures for CS data, reviews the previous CS methodology, and explains changes implemented for CS 2007, including limitations and implications.

- Sampling
  - CS Field Survey uses a stratified sample of 1 km squares on a 15 km GB grid; two sampling levels: square-level measurements and within-square plot measurements.
  - Land Classification (ITE) stratification changes over time: 32 classes originally; 42 classes for CS2000 (Scotland reporting); 45 classes for CS 2007 (Wales reporting added). Each country has its own related classification (England 21, Wales 8, Scotland 16).

- Estimation and Inference (historical)
  - Previous method: compute means and standard errors by Land Class, then combine with area-proportional weights to obtain regional/national estimates.
  - This approach makes minimal distributional assumptions but assumes independence across Land Classes, and stock and change are derived from different data sets (stock from all squares, change from repeated squares).

- Bootstrapping
  - To address non-normal distributions, CS 2000 introduced bootstrapping for square-level data to obtain standard errors and confidence intervals without strong normality assumptions.

- Reasons for Modifications to CS Methodology
  - Inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing discrepancies when comparing stock and change.
  - The inconsistency is not an error but a consequence of using different data subsets; the 2007 shift aims to provide consistent estimates over time.

- Modelling Approach for Consistency
  - Modelling (mixed-effects/repeated-measures) can provide consistent and efficient stock and change estimates for both square and plot-level data.
  - Modelling requires additional distributional assumptions; robustness is enhanced by bootstrapping.
  - The approach uses data from all surveys, improving precision but causing past-year estimates to be revisable as new data arrive.

- Square Level Data
  - Data are treated as a random sample of squares within each Land Class; a repeated-measures (mixed-effects) model is used.
  - Fixed effects: land-class means across surveys.
  - Random effects: square-level differences; repeated-measures correlations across surveys are modelled.

- Plot Level Data
  - Plot-level measurements within squares can be analysed within the same modelling framework.
  - Previous analyses either aggregated to square level or treated plots as independent; the new approach allows for square-level variation and plot-level residuals, embedded within bootstrapping.

- Model Specification
  - General model for square-level data: y_ijk = a_iK + s_ij + e_ijk
    - a_iK: fixed effects (land-class means across surveys)
    - s_ij: square-level random effects
    - e_ijk: repeated-measures residuals
  - Random effects are assumed normally distributed with land-class-specific variances; repeated-measures residuals vary by land class and survey.
  - With multiple surveys, there are many variance/covariance parameters; to keep models tractable, simplifications are used.

- Model Reduction and AR1 Modelling
  - Reducing random-effect parameters is necessary for stability and practicality; assumptions include:
    - Random-effect variances do not vary across surveys (common σ_i per land class).
    - Autoregressive AR1 structure for repeated-measures covariance, reducing parameters per land class to one.
  - This AR1 approach balances robustness, stability, and computational feasibility.
  - Bootstrap standard errors are recommended because they are robust to mis-specification of variance-covariance structures.

- Model Testing — Broad Habitats
  - Past Broad Habitat analyses (1984, 1990, 1998) showed inconsistencies when using stock vs. change estimates under old methods.
  - Using AR1 mixed models yields consistent stock and change estimates; changes over long periods align with sums of period-by-period changes.
  - Compared old vs. new methods: most differences were small and within prior uncertainties; some changes were minor in the context of standard errors.
  - Adoption of modelling for 2007 CS extended consistency to soil data and plot-level data as well.

- Limitations and Implications
  - AR1 model with bootstrapped SEs is computationally heavier but feasible; fixed-effect estimates are robust to moderate model variation.
  - Full parameterization is slow; a standardized AR1-based approach is preferred for automation and large-scale analyses.
  - Results may revise past-year estimates as new data are incorporated; this updating is a natural consequence of using information from all surveys.
  - Transformations to achieve normality are generally avoided to preserve results on the original measurement scale.

- References
  - Barr et al. (1993), Haines-Young et al. (2000), Dempster et al. (1977), Efron & Tibshirani (1993), Scott (2002).

- Practical Implications for Data Leaders
  - Move towards consistent estimation across time to improve comparability and integrity of long-term datasets.
  - Leverage full hierarchical data (square and plot levels) to achieve tighter precision, at the cost of increased computational demands.
  - Use robust, automated modelling (e.g., AR1 mixed models with bootstrapped SEs) to enable scalable analyses across many variables.
  - Acknowledge that future results may revise past estimates as new data are integrated; maintain transparent documentation of methods and assumptions.
  - Ensure data governance supports updated past results and metadata to reflect methodological changes and model assumptions.