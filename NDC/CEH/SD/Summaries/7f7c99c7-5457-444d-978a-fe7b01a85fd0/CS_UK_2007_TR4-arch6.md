# Countryside Survey 2007: Statistical Methodology

- This technical report describes the statistical methods used to analyse Countryside Survey (CS) data, reviews the previous CS methodology, and details changes introduced for CS2007, with a focus on achieving consistent stock and change estimates.
- The move from non-model-based estimates (stock from all data vs. change from repeated measurements) to a modelling approach improves consistency and precision across surveys.
- The modelling approach is robust but requires distributional assumptions and careful validation, especially for small data subsets.
- Implementing the modelling framework uses all available information and the hierarchical structure of CS data, producing more precise estimates and enabling past estimates to be updated as new data arrive.

## Why Changes Were Needed

- Previous reporting produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, leading to mismatches between stock and change.
- Many squares/plots are unrepeated across survey intervals, causing discrepancies when computing stock and change separately.
- Modelling stock and change consistently using incomplete data improves robustness and comparability across adjacent and non-adjacent survey intervals.
- A modelling approach also extends to both square- and plot-level data, enabling a unified analysis framework.

## Modelling Approach and Key Concepts

- Incomplete data techniques (mixed effects and repeated measures models) are used to obtain consistent estimates of stock and change across surveys.
- Fixed effects capture land-class means across survey years; random effects account for square-level and plot-level variability and their correlations across surveys.
- AR1 (auto-regressive order 1) structure is proposed to reduce the number of random parameters while maintaining realistic correlation across successive surveys.
- Bootstrap methods are used to obtain standard errors and confidence intervals, providing robustness to non-normal data distributions.

## Data Structures and Modelling Details

- Square-level data:
  - Treat CS data as a random sample of squares within each land class.
  - Use repeated-measures mixed models: fixed effects for land-class means by survey; random effects for squares and survey-to-survey deviations.
  - Observations y_ijk follow a model with fixed effects a_ik, square-level random effects s_ij, and repeated-measures errors e_ijk, with distributions allowing varying variances and covariances by land class and survey.
- Plot-level data:
  - Data within squares (plots) are hierarchical; previous analyses either aggregated to square level or treated plots as independent (risking bias).
  - Extended mixed models can include plot-level residuals in addition to square-level random effects; these models can be embedded within bootstrapping.
- Model specification:
  - y_ijk = a_ik + s_ij + e_ijk, with a_ik representing land-class means at survey k, s_ij the square random effect, and e_ijk the repeated-measures residuals.
  - Variance/covariance structures vary by land class and survey; AR1 reduces random-effect parameters to manage complexity and improve stability.
  - Distributional assumptions for random effects affect standard errors; bootstrap is used to obtain robust SEs.

## Model Testing and Broad Habitats

- Historical Broad Habitat analyses (1984, 1990, 1998) showed inconsistencies with old methods.
- Modelling with AR1 provided consistent stock and change estimates, avoiding the previous discrepancies between stock-based and repeated-squares-based changes.
- Comparisons between old and new methods show most differences are small and within the previous inconsistencies, reinforcing the viability of the modelling approach.
- The approach was tested on other data (soil, plot-level) and found feasible for consistent analyses across scales, supporting adoption for the 2007 CS data.

## Limitations and Implications

- AR1 modelling with bootstrapped SEs is robust but computationally intensive; fully parameterised models are slow for large variable sets, so a simplified AR1 approach is preferred for routine analyses.
- Fixed-effect estimates (stock and change) are robust to some mis-specification, but variance/covariance parameters require careful handling; bootstrap helps mitigate sensitivity.
- Some data (e.g., freshwater standing water) exhibited non-normal distributions causing convergence issues; in such cases, older methods were retained to ensure reasonable estimates.
- Adopting a model-based approach means past survey estimates can be updated as new data arrive, reflecting improved use of information, but past results may change slightly over time.
- The new methodology improves precision and consistency, but it is important to communicate that differences across reporting occasions may reflect updated information rather than errors.

## Operational Considerations

- Implementation is technically challenging and requires substantial computing time, but the AR1 model offers a practical balance between complexity and robustness.
- Analyses across many variables necessitate automated, standardized modelling workflows with quality checks comparing new and old methods to ensure reasonable updates.

## References

- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, Laird, Rubin (1977). Maximum likelihood from incomplete data via EM algorithm.
- Efron, Tibshirani (1993). An introduction to the bootstrap.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation using the empirical Fisher information matrix.