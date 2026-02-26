# Statistical Methodology for Countryside Survey Data

- This technical report outlines the statistical methodology used to analyse Countryside Survey (CS) data, summarising previous methods and detailing the changes implemented for CS in 2007 (CS2007).
- It shows that while prior methods were robust with minimal assumptions, they produced inconsistencies between stock (current abundance) and change estimates due to using different data portions. A modelling approach was adopted to produce consistent, more efficient estimates across surveys.
- The new modelling approach uses all available information, improves precision, and yields estimates that update previous results as new data arrive. It requires additional distributional assumptions and more computational effort, with extensive validation against the older method.
- To handle uncertainty and non-normal data distributions, bootstrapping is used to obtain standard errors and confidence intervals.
- The shift to modelling (AR1 mixed-effects/repeated-measures models) is applied to both square and plot level data and is designed to be automated for large-scale analyses, though model selection and checking remain important.
- Limitations include computational intensity, potential sensitivity to distributional assumptions, and the fact that incorporating data from all surveys means estimates for earlier surveys may be revised with new information.

## 1. Introduction
- The report gives an overview of sampling and analysis procedures for CS data, reviews previous CS methodology, and explains changes for CS2007, including limitations and implications.

## 2. Sampling
- CS Field Survey data come from a stratified sample of 1 km squares on a 15 km GB grid.
- Each square is mapped and measured; within-square plots are used to collect additional vegetation, soils, etc.
- Two sampling levels exist: square-level and within-square plot-level measurements (binary to continuous variables).
- Land Classification (ITE) classifications evolved: GB 32 -> CS2000 42 -> CS2007 45 classes, with separate country classifications (England, Wales, Scotland) linked to the national reporting needs.

## 2.2 Estimation
- Old approach: calculate means and standard errors for each Land Class, then combine (weighted by land area) to regional/national estimates.
- Assumes independence between Land Classes and between estimates within and across classes; minimal data distribution assumptions.

## 2.3 Bootstrapping
- Pre-CS2000: normality assumed for significance testing.
- CS2000 onward: bootstrap used to estimate standard errors and confidence intervals, addressing non-normality and providing robust significance testing.

## 3. Reasons for Modifications to CS Methodology
- Prior point estimates (stock and change) were viewed as inconsistent due to different data sets used for stock vs change (stock from all squares in a survey; change from repeated measurements).
- Inconsistencies arise from missing data across survey pairs, often due to new squares being added over time and some squares not being observed in earlier surveys.
- Three potential consistency approaches are discussed; modelling approaches using all available data provide consistent, robust estimates for both stock and change, and are extendable to plot-level data.
- The modelling approach was tested with Broad Habitat data and shown to produce consistent estimates with improved precision.

## 4. Modelling Approach

### 4.1 Square level data
- Data can be treated as a repeated measures problem with mixed models: fixed effects (land class means by survey) and random effects (square-level variation and survey-to-survey residuals).
- The simplest fixed effects model estimates land-class means per survey; stock estimates follow from scaling by land-class area; change estimates are the differences in stock estimates.
- Random effects capture variation among squares within land classes and the correlation of measurements across surveys.

### 4.2 Plot level data
- Plot-level data within squares can be analyzed via mixed models that include square-level random effects and plot-level residuals.
- Previous approaches (summarising to square level or treating plots as independent) either underutilised data or risk bias.
- Models can include an additional plot-level random effect; all analyses can be embedded within bootstrapping.

### 4.3 Model specification
- General square-level model: y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land-class means by survey)
  - s_ij: square random effects
  - e_ijk: repeated measures (survey) residuals
- Random effects are assumed normal with land-class-specific variance components; repeated-measure covariances vary by land class and survey pair.
- With K surveys, the model includes K fixed effects per land class and many random parameters; to keep models tractable, random effects are reduced using constraints (e.g., AR1 structure).
- AR1 reduction: assume constant within-land-class random effect variance over surveys and AR1 (first-order autoregressive) structure for covariances, leading to three random-effect parameters per survey per land class.
- Bootstrap estimation is emphasized because it remains robust when distributional assumptions are uncertain or violated.

### 4.5 Model testing – Broad Habitats
- Historically, Broad Habitats were used (1984, 1990, 1998 data) to test methodology.
- Old methods showed inconsistencies between stock and change estimates.
- AR1 modelling with bootstrap produced consistent estimates; differences between old and new methods generally fell within the old method’s error bounds.
- Consistent analyses were also performed for soil and plot-level data, supporting adoption of the modelling approach for 2007 CS.

## 5. Limitations and Implications
- Model-based analysis with bootstrapping is computationally demanding; large numbers of variables can be slow to fit.
- Fixed effects estimates (stock/change) are robust to some distributional mis-specifications, but variance/covariance parameters are more sensitive.
- For very non-normal data, transformation can be problematic if results must be presented on the original scale.
- Some variables (e.g., standing water) showed non-normal distributions causing convergence issues; in such cases, old methodology results were retained.
- Overall, modelling utilises more information and better represents data hierarchy, yielding more precise estimates.
- Estimates for earlier surveys may be updated when new data are added, reflecting information integration across all surveys; this represents a shift from the previous reporting inconsistencies to a dynamic updating process.

## 6. References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).