# Statistical methodology for Countryside Survey data

- This report describes the statistical methodology used to analyse Countryside Survey (CS) data, summarises previous methods, and details changes implemented for CS 2007.
- Key motivation: previous stock estimates used all data from a survey while change estimates used only repeated measurements, leading to inconsistencies between stock and change.
- A modelling-based, consistent estimation approach was found to be feasible and robust using CS Broad Habitat data; results were generally close to old estimates within existing uncertainty.
- The modelling approach utilises all available information, yielding more precise estimates; future surveys can also improve past estimates, though the changes may be small.
- The switch to modelling is computationally demanding (iterative model fitting) and required addressing CS’s complex sampling design; robust checks were made to validate results.

## Sampling and data structure

- CS data come from a stratified sample of 1 km squares on a 15 km GB-wide grid; measurements occur at two levels: square level and within-square plot level.
- Land Classification: England (21 classes), Wales (8), Scotland (16) across a 45-class system; national classifications are related to a GB origin.
- Data types include binary and continuous measures (areas, lengths, etc.).

## Estimation: old methods and bootstrapping

- Previous approach: estimate means and standard errors by Land Class, then combine by land area to regional totals; assumed independence across Land Classes.
- Stock estimates used all data from a survey; change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Bootstrapping (1000–10,000 resamples) is used to obtain significance and confidence intervals, particularly for square-level data where normality is questionable.

## Why modify CS methodology?

- To address inconsistencies where adjacent-survey changes did not align with non-adjacent changes when using old methods.
- New approach aims to produce consistent estimates of stock and change across all surveys by modelling incomplete data and leveraging data from all years.

## Modelling basics

- Incomplete data techniques (mixed effects/repeated measures) are used to combine data from all surveys.
- Modelling requires distributional assumptions; fixed effects focus on stock and change by Land Class and survey, while random effects capture sampling structure.
- The goal is to obtain robust fixed effect estimates (stock/change) while controlling for missing data and hierarchical structure.

## Square level data

- Model treats CS square data as a repeated-measures problem with:
  - Fixed effects: land-class mean values for each survey.
  - Random effects: square-level deviations from land-class means.
  - Repeated-measures correlations of survey deviations within the same square.
- This yields stock estimates by scaling land-class means by area and automatically gives consistent change estimates as differences across surveys.

## Plot level data

- Plot-level measurements within squares require careful handling of hierarchical structure.
- Earlier analyses either collapsed to square level or treated plots as independent, risking bias or inflated precision.
- The modelling framework can incorporate an additional plot-level residual, allowing correlations to vary within plots and squares; these forms can be bootstrapped.

## Model specification and simplifications

- General square-level model: y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land class i, survey k)
  - s_ij: random square effect for land class i
  - e_ijk: random repeated-measures effect for square j, survey k
- Random effects: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances between surveys.
- Parameter burden grows with the number of surveys; to keep models tractable, a reduced scheme is used (AR1):
  - Assume same variance structure across surveys within a land class and a first-order autoregressive (AR1) structure for inter-survey covariances.
  - This reduces random-effect parameters to a small, fixed number per land class regardless of survey count.
- Bootstrap standard errors are used because variance/covariance parameter estimates can be sensitive to distributional assumptions.

## Model testing: Broad Habitats

- Prior analyses of Broad Habitats (1984, 1990, 1998) showed inconsistencies between stock and change using old methods.
- Modelling with AR1 achieved consistent stock and change estimates across survey pairs; differences between old and new methods were small and generally within old discrepancies.
- Results confirmed feasibility and improved consistency across time, supporting the adoption of modelling for 2007 analyses.

## Limitations and implications

- AR1 models are robust for fixed effects but may yield misleading parametric standard errors if distributional assumptions are wrong; bootstrap mitigates this risk.
- Some very non-normal data (e.g., standing water) can lead to convergence to local maxima; in such cases, older methods may be used for those variables.
- Fully parameterised models can be extremely slow; AR1 with bootstrap is a practical, robust compromise for large numbers of analyses.
- Adopting a model-based approach means past estimates for earlier surveys can be revised as new data are incorporated; this is conceptually different from the older, inconsistent reporting.
- The approach uses all available information and respects data hierarchy, delivering more precise estimates; however, automated, standardized model fitting is essential for large-scale analyses.

## Practical takeaways for data use

- The Countryside Survey 2007 shift to consistent modelling enhances data reliability and enables more precise trend analyses across surveys.
- Outputs (stock and change) are now derived from models that integrate data over time, improving robustness and comparability.
- Users should expect small revisions to past estimates as new survey data are added, reflecting updated information rather than errors in prior analyses.
- For scalable data support, automated AR1-based modelling with bootstrap is recommended to maintain consistency and efficiency across many variables.