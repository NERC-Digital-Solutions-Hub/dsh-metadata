# Countryside Survey 2007: Statistical Methodology

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, summarize prior methods, and detail changes implemented for CS in 2007 to achieve consistent estimation of stock and change.

## Key context and motivation

- Previous CS methods estimated stock using all data from a survey and change using repeated measurements, causing inconsistencies between stock and change estimates.
- Modelling approaches for consistent estimation were investigated and found feasible and robust, offering more precise estimates by using all available information and the data hierarchy.

## Data and sampling

- Data come from a stratified sample of 1 km squares across Great Britain, with two levels of sampling:
  - Square level: broad measurements for each Land Class and survey year.
  - Plot level: detailed measurements within squares (vegetation, soils, etc.).
- Land Classification: country-specific classifications (England, Wales, Scotland) with 21, 8, and 16 classes respectively (totalling 45 classes nationally).
- Each survey adds new squares over time, causing unrepeated data to dominate earlier surveys in pairwise comparisons.

## Estimation: traditional vs modelling approaches

- Old approach: stock estimates used all data from a survey; change estimates used repeated measurements only. This yielded inconsistencies when comparing adjacent surveys or non-adjacent periods.
- Modelling approach: use consistent estimation by fitting models (mixed effects/repeated measures) to data from all surveys, yielding stock and change estimates that are compatible across time periods.

## Modelling basics and rationale

- Incomplete data techniques modeled via mixed effects, using fixed effects (stock/change as functions of survey year) and random effects (square-level and plot-level variation).
- To keep the model tractable with many land classes and surveys, random effect parameters are reduced using structure:
  - AR1 (first-order autoregressive) covariance for repeated measures.
  - Common variance parameters across surveys for each land class.
- Benefits:
  - Consistency: stock and change estimates align within the modelling framework.
  - Efficiency: more precise estimates by leveraging all data and the data hierarchy.
  - Robustness: fixed effect estimates are relatively robust to mis-specification of random effects; bootstrap standard errors provide robust uncertainty measures.

## Square level data

- Framework: repeated measures mixed model with:
  - Fixed effects: land-class means across surveys (year as factor).
  - Random effects: square-level deviations and within-square, across-survey correlations.
- Goal: derive stock estimates from fixed effects scaled by land-class area; changes derived from differences in these stock estimates, ensuring internal consistency.

## Plot level data

- Plot-level measurements within squares can be analyzed by extending the square-level model to include an additional plot-level random effect (plot residuals) and correlated survey residuals.
- Bootstrapping adapts to these extended models to obtain valid standard errors.

## Model specification (conceptual)

- General form for square level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square random effect
  - e_ijk: repeated measures residual
- Random effects assumed normal with land-class-specific variances; covariances vary by land class and survey pair.
- Parameter reduction strategies:
  - Variances may be constant across surveys within a land class (σ_i).
  - AR1 structure for covariances to reduce parameters to three per land class.
- Estimation uses bootstrap for standard errors to remain robust under distributional assumptions.

## Model testing: Broad Habitats

- Historical habitat data (1984, 1990, 1998) analyzed with both the old approach and the new modelling approach.
- Findings: modelling approach eliminates the stock/change discrepancies observed with the old method; differences between methods generally fall within previous error bounds.
- The new approach was also tested on soil and plot-level data, confirming feasibility and consistency across scales.
- Adoption: CS2007 adopted the modelling approach for Broad Habitats and extended data types.

## Limitations and implications

- Computational intensity: fully parameterised models are slow; AR1 offers a practical balance between speed and precision.
- Model choice sensitivity: fixed effects are robust, but variance/covariance estimates can be sensitive; bootstrapping mitigates some concerns.
- Non-normal data: significant non-normality (e.g., standing water) can cause convergence or bias; in some cases, the old method may be preferred for those variables.
- Updating results: because analyses incorporate all surveys, estimates for earlier years can be revised as new data are added; this is conceptually distinct from earlier inconsistencies but results may shift slightly with new information.
- Practical implication: a standardized, automated modelling approach is needed to handle many variables across surveys while delivering robust, interpretable results.

## Practical takeaway for data users

- CS2007 provides more precise, consistent stock and change estimates by modelling across surveys and incorporating the data structure.
- Outputs are updated as new survey data become available, reflecting improved estimates for earlier periods.
- The approach supports broader, self-consistent analyses across square and plot levels, with uncertainty quantified via bootstrapping.