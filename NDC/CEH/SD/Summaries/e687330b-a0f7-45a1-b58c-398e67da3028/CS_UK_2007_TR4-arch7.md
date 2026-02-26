# Countryside Survey 2007 Methodology

- This report describes the statistical methodology used for analyzing Countryside Survey (CS) data, summarises previous methods, and explains changes implemented for CS in 2007 to achieve consistent estimation of stock and change.

## Executive summary

- Previous CS methods used minimal assumptions and were robust, but stock estimates used all data from a survey while change used only repeated measurements, causing inconsistencies between stock and change.
- Modelling with consistent estimation (using all data across surveys) is feasible and robust; differences from old methods are generally small.
- The 2007 CS adopted modelling for consistent estimation, which yields more precise estimates by leveraging all available information.
- The modelling approach requires additional distributional assumptions; results, especially for small subsets, are checked against the previous methodology.
- While more computationally intensive, the modelling approach produces improved products and consistency across time.
- Implementation challenges were overcome, leading to a substantially improved analysis product.

## 1. Introduction

- The report gives an overview of sampling and analysis procedures for CS data, reviews the previous methodology, and explains the reasons and details of the 2007 changes.
- Full prior details are documented in Barr et al. (1993).

## 2. Overview of previous CS methodology

- CS field data come from a stratified sample of 1 km squares on a 15 km GB grid; each square is mapped and measured, with some measurements within squares (plots) and others for the whole square.
- Data types range from binary to continuous (areas, lengths).
- Land Classification (ITE) strata are country-specific (England, Wales, Scotland) with 21, 8, and 16 classes respectively.
- Stock estimates traditionally used means/standard errors by Land Class, then combined by area weighting; change estimates used only repeated measurements.

## 3. Reasons for modifications to CS methodology

- Inconsistencies arose because stock (all data) and change (repeat data) were derived from different data sets.
- Some squares/plots are missing between surveys due to new squares, refusals, etc., causing unmatched data across surveys.
- Three potential consistency approaches exist; CS previously used stock from all data and change from repeated data, which is not fully consistent.
- Modelling approaches (treating stock and change jointly across all surveys) offer consistent and more efficient estimates, but require more assumptions.

## 4. Consistent estimation

- Modelling aims to produce stock and change estimates that are consistent across surveys and leverage all available information.

### 4.1 Possible approaches

- Approaches include using stock estimates from all data with change as the difference between stock estimates, or using modelling to produce consistent stock and change estimates for both square and plot level data.
- The modelling approach is attractive for consistency and robustness, though covariance between successive surveys can affect efficiency and applicability to plot-level data.

### 4.2 Modelling basics

- Incomplete data techniques (EM, multiple imputation concepts) underpin consistent estimation; CS uses mixed effects/repeated measures models with fixed effects (stock/change) and random effects (sampling variation).
- Models require distributional assumptions for random effects; bootstrap can provide robust standard errors.
- For CS, models must handle data from multiple surveys, land classes, and hierarchical structure.

### 4.3 Square level data

- Square-level data are treated as repeated measures within land classes; a mixed model with fixed effects for land-class means across surveys and random square effects plus repeated measures within squares.
- Random effects capture square-level deviations and correlations of repeated measurements across surveys.

### 4.4 Plot level data

- Plot-level data within squares add complexity; earlier analyses sometimes treated plots as separate or collapsed data.
- A model can include both square-level and plot-level residuals; both forms can be embedded within bootstrap procedures.
- Properly accounting for plot-level variation improves precision over square-only analyses.

### 4.5 Model specification

- A general form: y_ijk = a_ik + s_ij + e_ijk, where a_ik are fixed effects (land-class means per survey), s_ij are square random effects, and e_ijk are repeated-measures residuals.
- Distributions: random effects and residuals are assumed normal with land-class-specific variances; covariances vary by land class and survey pair.
- The model becomes complex as surveys increase; reducing random-effect parameters is necessary for practicality.

### 4.6 Model testing – Broad Habitats

- Historically, CS reported Broad Habitat stock and change; inconsistencies between stock-based and repeat-square-based change estimates were evident.
- Modelling with AR1 (first-order autocorrelation) across surveys provides consistent estimates for Broad Habitats.
- The AR1 model reduces random-parameter complexity while maintaining robust fixed-effect estimates; bootstrap is used for standard errors due to potential mis-specification of variance components.
- Broad Habitat analyses on 1984, 1990, and 1998 data showed modelling eliminated the previous discrepancies and produced consistent results.

## 5. Limitations and implications

- Bootstrapping square-level data with AR1 modelling is computationally demanding but feasible; fixed effects proved robust to model variation, though fully parameterised models are slow.
- The AR1 model is a practical balance between model complexity and computational efficiency; bootstrap SEs provide robust uncertainty estimates.
- Results are presented on original measurement scales; transforming data (to compute back-transformed estimates) can complicate interpretation due to random effects.
- Some variables with non-normal distributions (e.g., standing water) can cause convergence issues; in such cases the older methodology may be used for that variable.
- Adopting a model-based approach means past estimates may be revised as new survey data are added, unlike the previous method where older results remained fixed.
- Overall, the modelling approach uses all available information, respects data hierarchy, and yields more precise estimates.

## 6. References

- Barr et al. (1993) CS 1990 Main Report; DETR
- Dempster, Laird, Rubin (1977) EM algorithm; J R Statist Soc B
- Efron, Tibshirani (1993) Bootstrap
- Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
- Scott (2002) ML estimation using the empirical Fisher information
- Additional CS-related sources and project details

- Note: The document is © Natural Environment Research Council; CS2007 was funded collaboratively by Defra and other bodies.