# Countryside Survey 2007: Statistical Methodology

## Executive summary
- Describes the statistical methodology used to analyze Countryside Survey (CS) data, reviews previous CS methods, and details changes implemented for CS in 2007.
- Old approach: stock estimates used all data from a survey while change estimates used only repeated measurements, causing inconsistencies between stock and change.
- Modelling approach: demonstrates that consistent estimation via modelling is feasible and robust, with differences from old methods typically within the existing inconsistency range.
- Adoption: 2007 CS reports use the modelling approach for consistency and efficiency, producing more precise estimates by using all available information.
- Trade-offs: modelling requires distributional assumptions about the data; results are validated by comparison with previous methods, especially for small subsets.
- Practical aspects: the modelling approach is computationally intensive (more CPU time) but yields a significantly improved product; outputs may update previous survey estimates as new data become available.

## Overview of CS data and sampling
- Two-level sampling within GB: 1 km squares on a 15 km grid; measurements at the square level and within-square plots.
- Data types range from binary to continuous (e.g., areas, lengths).
- Stratification by Land Classification (GB classification evolved over time; separate national classifications for England, Wales, Scotland).

## Estimation and handling of uncertainty
- Old method: means and standard errors per Land Class estimated and then combined to regional/national estimates, weighting by land area.
- Assumptions: independence of Land Class estimates from each other and from total land.
- Bootstrapping (since CS2000): used to estimate standard errors and confidence intervals for square-level data due to potential non-normality, enabling robust significance testing.

## Why modifications were needed
- Point estimates of stock and change were viewed as inconsistent when produced with the old approach (stock from all data vs change from repeated data).
- Inconsistencies arise because different data subsets (unrepeated vs repeated squares) are used for stock and change.
- The shift in CS reporting (emphasizing timelines across multiple surveys) highlighted these inconsistencies, motivating the move to consistent estimation via modelling.

## Modelling basics for consistent estimation
- Incomplete data techniques (EM-like approaches) are used to integrate information from all surveys, respecting the data’s hierarchical structure.
- Mixed effects/repeated measures models are fitted to data from all surveys; fixed effects relate to stock/change values, random effects reflect sampling variation.
- Models require distributional assumptions; robustness of fixed effects is higher than for variance/covariance parameters. Bootstrap remains recommended for standard errors.

## Square-level data modelling
- Treats CS data as a random sample of squares within each Land Class; use repeated measures mixed models.
- Fixed effects: land-class means across surveys (stock estimates when scaled by land area).
- Random effects: square-level deviations and within-square survey deviations, allowing for correlation across surveys.
- Complexity grows with more surveys, so simplifications (e.g., reducing random parameters) are used to keep models tractable.

## Plot-level data modelling
- Within-square plots add another layer of data; earlier analyses varied (summarised to square level or treated plots as independent).
- Modern approach extends the square-level model to include plot-level random effects, with bootstrapping incorporated to obtain correct standard errors.

## Model specification and reduction
- General form for square-level data: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means per survey)
  - s_ij: square random effects
  - e_ijk: repeated-measures residuals
- Random effects are assumed normally distributed with land-class-specific variances; e residuals have variances that can vary by land class and survey, with covariances across squares.
- To keep models manageable, assumptions are made to reduce the number of random parameters (e.g., AR1 structure for covariances; common variance scaling across surveys).
- AR1 (autoregressive of order 1) reduces random-parameter complexity to three per survey, regardless of the number of surveys.
- Fixed effects are robust to some mis-specification of random effects distributions; bootstrap is used to obtain robust standard errors.

## Model testing: Broad Habitats
- Analyses of seven Broad Habitats using 1984, 1990, and 1998 CS data show that modelling yields consistent stock and change estimates, eliminating the previous discrepancies between stock-based and repeat-square-based change estimates.
- New modelling estimates align with the inconsistencies expected under the old approach but within their error bounds.
- Comparisons indicate that differences between old and new methods are small relative to existing inconsistencies; the modelling approach is feasible and advantageous.

## Limitations and implications
- Bootstrapped standard errors with AR1 models are computationally demanding but generally workable for large CS datasets.
- Fixed-effect estimates are robust to model variation; variance/covariance estimates are more sensitive to distributional assumptions.
- Some non-normal data (e.g., standing water) can cause convergence issues; in such cases, older methods may be preferred for that variable.
- The modelling approach uses information from all surveys, so estimates for a given survey can be updated as new data arrive; this maintains consistency over time but means cross-reporting consistency across occasions may fluctuate with new data.
- Overall, the approach provides more precise estimates and a unified, hierarchical analysis framework across square and plot levels, at the cost of higher computational effort and the need for careful model validation.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron and Tibshirani (1993); Scott (2002).