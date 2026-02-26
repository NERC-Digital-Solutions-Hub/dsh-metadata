# Countryside Survey 2007 – Statistical Methodology

## Executive summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, including changes from previous methods.
- Previous methods were robust but produced inconsistencies: stock estimates used all data from a survey while change estimates used only repeated measurements.
- Modelling approaches demonstrated that consistent estimation of both stock and change is feasible and robust; differences from old methods are generally small.
- CS2007 adopts modelling for consistent estimation, improving precision by using all available information across surveys.
- Modelling requires additional distributional assumptions; validity checks, especially for small subsets, were performed by comparison with the old method.
- Although more computationally intensive, the modelling approach yields more precise estimates and a more coherent use of data over time.
- Implementation posed technical challenges due to CS’s complex sampling; successful adoption results in a significantly improved product, with outputs that can update past estimates as new data arrive.

## Introduction
- The report provides an overview of CS data sampling and analysis procedures, summarising previous methodology and detailing the 2007 modifications.
- Full methodological detail for CS sampling/estimation is available in prior CS reports.

## Data collection and sampling
- CS Field Survey uses a stratified sample of 1 km squares on a 15 km GB grid.
- Two levels of sampling within each square: square-wide measurements and within-square plot measurements.
- Measurements range from binary to continuous (areas, lengths).
- Land Classification strata evolved by country (England, Wales, Scotland) to reflect reporting needs; CS2007 classification comprised 45 land classes (21 England, 8 Wales, 16 Scotland).

## Estimation and data handling
- Old approach: estimate means and standard errors for each Land Class, then combine to regional/national estimates, weighting by land area; treated means as independent across land classes.
- Change estimates historically derived from repeated measurements; this could create inconsistencies with stock estimates.
- Bootstrapping introduced to quantify significance and confidence intervals for square-level data due to non-normal distributions.

## Why modifications were needed
- Reported stock and change inconsistencies arise because stock uses all survey data while change uses repeated measurements only.
- Multiple approaches considered to achieve consistency; modeling-based approaches found to be feasible, robust, and capable of delivering consistent stock and change estimates.
- The shift aimed to produce coherent timelines from the first survey to the present, though it introduces small updates to past estimates as new data are incorporated.

## Modelling basics
- Modelling treats missing information using incomplete-data techniques (EM-like approaches); relies on distributional assumptions.
- Mixed-effects/repeated-measures models are fitted to data from all surveys; fixed effects relate to stock/change, random effects reflect sampling structure and variability.
- Models can be applied to both square-level and plot-level data; attempt to balance model complexity with data sparsity to maintain stability and computational feasibility.
- Bootstrap remains essential for robust standard errors, given potential misspecification of random-effects distributions.

## Modelling details: square level data
- Data for complete 1 km squares are treated as a random sample within each land class; a repeated-measures (mixed) model is used.
- Basic fixed-effects component estimates land-class means across surveys; stock estimates scale by land-class area; change estimates are differences between consecutive stock estimates, ensuring automatic consistency.
- Random-effects component accounts for square-level deviations and correlation of successive surveys within the same square.

## Modelling details: plot level data
- Plot-level data within squares introduces hierarchical complexity; previous analyses treated plots variously (summarised to square level, treated as independent, or partially modeled).
- Modern approach extends the square-level model to include a plot-level residual (random effect) and allows for correlations at the plot level; both forms can be embedded within bootstrapping.

## Model specification and AR1 approach
- General square-level model: y_ijk = a_i_k + s_i_j + e_i_jk, with fixed effects a_i_k (land-class means across surveys), square random effects s_i_j, and repeated-measure errors e_i_jk.
- Random effects covariances and variances are typically large in number; to keep models workable, two simplifications are used:
  - Variances do not vary with surveys (common σ_i) across surveys.
  - Autoregressive AR1 structure for covariances, reducing repeated-measures parameters to one per land class.
- This AR1 model, combined with bootstrap for standard errors, provides a practical balance of robustness and computational efficiency.

## Model testing – Broad Habitats
- Analyses of Broad Habitat data from 1984, 1990, and 1998 show that modelling avoids the inconsistencies seen in older methods.
- Stock and change estimates derived from the AR1 model align with the old approach within old-level variability; differences are generally small.
- Consistency and precision improve; results support adopting the modelling approach for 2007 onward across square and plot data, including soil and other datasets.

## Limitations and implications
- While bootstrapping with AR1 is robust, fully parameterised models are slow; AR1 offers a practical compromise for large-scale analyses.
- Fixed-effects estimates are robust to some mis-specification of random-effects distributions; variance/covariance estimates are more sensitive.
- Some variables with highly non-normal distributions (e.g., standing water) may not converge under the new method; older methodology may be preferred for those cases.
- Data from all surveys influence current estimates; past survey estimates can be revised as new data arrive—this updating is expected and not considered an inconsistency.
- The shift improves precision by utilizing hierarchical structure and all available information; however, reporting must accommodate potential small revisions to earlier surveys.

## Practical implications for data management and outputs
- Adoption enables more precise, consistent stock and change estimates across surveys, improving data usability for policy and planning.
- Outputs may be more suitable for self-service analysis, given the coherent, model-based framework across time.
- Automated, standardized modelling enables scalable analysis across a large set of variables, with checks comparing old and new methods to ensure results remain within prior uncertainty bounds.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).