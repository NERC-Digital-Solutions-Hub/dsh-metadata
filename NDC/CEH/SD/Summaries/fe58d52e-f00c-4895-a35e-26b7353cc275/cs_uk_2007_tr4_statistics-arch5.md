# Countryside Survey in 2007

- Purpose: Describe the statistical methodology used to analyze Countryside Survey (CS) data, summarise previous methods, and detail changes introduced for CS in 2007 to achieve consistent estimation across surveys.
- Key shift: Move from stock/change estimates derived from different data subsets to a modelling approach that provides consistent and more efficient estimates using all available information.

## Executive context for Data Stewards

- Adoption of a modelling framework (mixed effects with AR1 structure) to ensure stock and change estimates are internally consistent across survey years.
- Use of bootstrapping to obtain robust standard errors and significance, accommodating non-normal data distributions.
- Recognition that updating with new survey data can revise past estimates, reflecting a dynamic, all-information-in use approach rather than fixed past results.

## 1. Introduction

- Technical report on sampling and analysis procedures for CS data; reviews CS2000 methodology and explains modifications for 2007.
- Emphasises aims of providing robust, consistent estimates by leveraging all available data and acknowledging data hierarchy.

## 2. Sampling

- Two-level sampling: 
  - 1 km squares (stratified within a 15 km GB grid), with land classifications forming strata.
  - Within-square plots/quadrats for detailed vegetation, soils, etc.
- Data types range from binary to continuous metrics (areas, lengths).
- Land Classification classifications evolved for country-specific reporting (GB -> 42 classes in CS2000; 45 classes by CS2007 to accommodate Wales reporting), with England, Wales, Scotland each retaining related class structures.

## 3. Estimation

- Original approach: compute means/standard errors for each Land Class, then combine (weighted by land area) to obtain regional/national estimates.
- Assumptions: independence between land classes and between class estimates and total land; method robust to distributional form.
- Inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.

## 4. Bootstrapping

- Used to estimate significance and confidence intervals for square-level data due to potential non-normality.
- Resampling (typically 1,000–10,000 replicates) yields empirical distributions for stock or change, enabling robust inference without normality assumptions.

## 4. Reasons for modifications to CS Methodology

- Problem: reported stock and change could appear inconsistent because they were derived from different data subsets.
- Causes: missing information across survey pairs (new squares added, unrepeated squares dropped), leading to discrepancies when comparing adjacent vs non-adjacent surveys.
- Goal: develop methods that yield consistent estimates across time spans and improve precision by using all data.

## 4. Modelling basics

- Modelling approach relies on mixed effects/repeated measures models to handle incomplete data and data hierarchy.
- Fixed effects correspond to land-class means across surveys; random effects capture square-level and survey-to-survey variation.
- Distributions of random effects require assumptions; these influence variance/covariance estimates and standard errors.
- Practical challenge: models with many random parameters can be unstable; therefore simplifications are used to keep models tractable while preserving fixed-effect estimates.

## 4.6 Model testing – Broad Habitats

- Historical comparison of Broad Habitat estimates across 1984, 1990, 1998 showed inconsistencies between stock- and repeat-square-based change estimates.
- Modelling with AR1 mixed-effects produced estimates without the discrepancies observed in old methods.
- Differences between old and new methods generally fall within the old method’s existing error bounds, indicating compatibility with past results while providing consistent trends.
- Analyses extended to soil data (1978, 1998) and plot-level data, confirming feasibility of consistent estimation beyond square-level data.

## 4.5 Model specification (summary)

- Square-level model form: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square-level random effects (within land class)
  - e_ijk: repeated-measures residuals (survey deviations)
- Random effects: assumed normal with land-class-specific variances; covariances across surveys modeled (non-stationarity reduced by AR1 structure).
- Parameter reduction: to keep models stable, assume common variance components across surveys (σ_i) and AR1 covariance structure to reduce random parameters to a manageable number per land class.
- Bootstrap remains the method of inference for standard errors due to sensitivity of parametric SEs to distributional assumptions.

## 4.5 Model specification (continued)

- AR1 (autoregressive, order 1) structure reduces random-effect parameters to a small, consistent set across surveys.
- Fixed effects robust to some mis-specification of random effects; bootstrap estimation of SEs remains robust.

## 4.6 Plot-level data

- For plot-level measurements within squares, models extend to include plot-level residuals to capture within-square variation.
- Bootstrapping can incorporate either square-level or plot-level structure, enabling coherent SE estimation across data hierarchies.

## 5. Limitations and Implications

- Computational demands: full parameterised models are slow; AR1 with bootstrap provides a practical balance between accuracy and run-time.
- Fixed-effect estimates (stock/change) are robust to reasonable model variation; variance/covariance estimates require careful specification.
- Non-normal data (e.g., freshwater standing water) can lead to convergence issues or local maxima; in such cases, older methods may be preferred for that variable.
- Analyses across all surveys mean past estimates can update with new data, which is conceptually different from the old inconsistencies but expected as information accumulates.
- Benefit: the modelling approach uses all available information and respects the data hierarchy, producing more precise estimates; however, it requires automated, standardized modelling to handle large numbers of variables.

## 6. References

- Barr et al. (1993); Haines-Young et al. (2000); Dempster, Laird, Rubin (EM algorithm); Efron & Tibshirani (bootstrap); Scott (2002) on empirical Fisher information.

- Note: The Countryside Survey in 2007 was funded by DEFRA and NERC, with ongoing data governance and availability through the Countryside Survey project office.