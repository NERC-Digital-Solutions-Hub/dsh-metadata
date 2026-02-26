# Countryside Survey 2007: Statistical Methodology for the analysis of Countryside Survey data

- This technical report describes the statistical methodology used to analyze Countryside Survey (CS) data, comparing the previous methods with the modelling approach adopted for CS 2007 to achieve consistent stock and change estimates across surveys.
- It argues that modelling approaches, though requiring more assumptions and computation, yield more precise and robust estimates by using all available data and properly accounting for data hierarchy and missing information.
- The report validates the modelling approach against earlier methods and through Broad Habitat testing, and discusses limitations, implications for reporting, and practical considerations for implementation.

## Context for GIS data products

- Objective: produce map-based data visualisations that accurately reflect stock and changes in countryside features over time, suitable for policy, clients, or the public.
- Modelling approach provides consistent estimates across multiple surveys, enabling time-series mapping and comparability, with uncertainty quantified via bootstrap.

## Data sources and structure

- CS uses a stratified sample of 1 km squares across GB on a 15 km grid; measurements occur at two levels:
  - Square level: measurements that apply to the whole square (e.g., Land Class totals)
  - Plot level: measurements within each square (e.g., vegetation, soils) across multiple plots
- Land Classification: GB-wide classification adjusted for country reporting; CS 2007 uses a 45-class Land Classification split by England, Wales, Scotland.

## Estimation approaches (old vs new)

- Old approach
  - Stock estimates: use all data from a survey
  - Change estimates: use only repeated measurements across surveys
  - Result: potential inconsistencies between stock and change estimates due to different data pools
- Modelling approach (CS 2007)
  - Uses consistent estimation by fitting mixed effects/repeated measures models to data from all surveys
  - Produces stock and change estimates that are internally consistent
  - Applies to both square-level and plot-level data
  - Requires assumptions about data distributions; uses bootstrap to obtain standard errors and confidence intervals, accommodating non-normal data

## Modelling basics and data types

- Square-level data
  - Treated as a repeated-measures problem with fixed effects (survey/year) and random effects (squares within land classes)
  - Fixed effects provide mean stock per Land Class per survey; changes are differences in these fixed effects
  - Random effects capture square-level and within-square variation across surveys
- Plot-level data
  - Plots within squares are modelled with an extension to include plot-level residuals (random effects)
  - Keeps the hierarchical structure and accounts for within-square and across-square variability
  - Both square- and plot-level models can be embedded within bootstrapping

## Model specification and simplification (AR1)

- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class means per survey)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residuals
- Random effects
  - Must specify variances and covariances; too many parameters can hinder fitting
  - Simplifications:
    - Variances σ_i assumed common across surveys for a land class
    - Autoregressive AR1 structure for covariances: correlations between surveys decay with time, reducing parameters to a manageable number
- AR1 model plus bootstrap
  - Balances robustness of fixed effects with a practical, parsimonious random-effects structure
  - Bootstrap provides robust standard errors without over-reliance on distributional assumptions

## Consistency and reporting

- Consistency: the modelling approach ensures stock and change are derived from the same model framework, avoiding past inconsistencies
- Reporting emphasis: timelines spanning from the first survey to the present; updated past estimates may occur as new surveys are added
- Comparison to old methods: differences between old and new methods are generally small relative to existing uncertainties; most estimates remain within previous error bounds

## Validation and testing (Broad Habitats)

- Tested modelling approaches on Broad Habitat data (1984, 1990, 1998) and plot-level soil data
- Findings:
  - Old method inconsistencies between stock and change are resolved with the modelling approach
  - Stock and change estimates from the AR1 model align with the consistency criteria
  - Changes between periods derived from stock differences or from repeated squares converge under the modelling framework
- Conclusion: modelling provides consistent estimates without sacrificing accuracy

## Limitations and practical implications

- Computational demand: AR1 modelling with bootstrap is slower than the old method; full deployment across many variables is time-intensive
- Model selection: fixed effects robust to some mis-specification; variance/covariance estimates are more sensitive
- Non-normal data: bootstrap helps; some highly non-normal variables may still pose challenges (e.g., standing water in freshwater data) where old methods were retained for those cases
- Data updating: analyses use information from all surveys; past estimates may be revised with new data, which is a deliberate, conceptually different update from previous inconsistencies
- Applicability: method aims to be automated for large-scale use; a balance between model complexity and practicality is required

## Implications for GIS practitioners

- Improved map accuracy and reliability:
  - Stock and change mapped over time with quantified uncertainty
  - Consistent estimates enable robust time-series visualisations and trend analyses
- Data integration:
  - Handles data at multiple resolutions (square-level and plot-level) within a single coherent framework
- Transparency and uncertainty:
  - Bootstrap-based confidence intervals accompany estimates, aiding interpretation in map legends and decision-making
- Practical considerations:
  - Expect longer processing times for analyses across many variables
  - Past estimates may shift slightly as the model is updated with new data, which is a feature of leveraging all available information
  - When communicating results, emphasize the modelling assumptions and the role of uncertainty

## References and further reading

- Barr et al. (1993); Dempster et al. (1977); Efron & Tibshirani (1993); Haines-Young et al. (2000); Scott (2002)