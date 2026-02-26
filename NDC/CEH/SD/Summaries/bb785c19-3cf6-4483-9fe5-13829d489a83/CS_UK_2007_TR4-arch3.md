# Countryside Survey 2007: Description of the statistical methodology

- Executive summary
  - Describes the statistical methodology used to analyze Countryside Survey (CS) data and outlines changes introduced for CS in 2007.
  - Previous methods were robust but produced inconsistencies: stock was estimated using all data from a survey, while change relied on repeated measurements, causing mismatches between stock and change.
  - Modelling for consistent estimation (via data from all surveys) is feasible and generally robust; differences from old methods are small relative to inherent inconsistencies.
  - The new modelling approach yields more precise estimates by using all available information and incorporating data hierarchy; future estimates can update past surveys as new data arrive.
  - Implementation is technically challenging and more computationally intensive, but ultimately produces improved products (stock and change estimates) with appropriate uncertainty estimates.

- Introduction
  - This technical report overviews CS sampling and analysis procedures, reviewing the previous CS methodology and detailing changes for CS2007.
  - Full historical detail available in Barr et al. (1993).

- CS sampling overview
  - Data come from a stratified sample of 1 km squares on a 15 km GB grid.
  - Two levels of sampling:
    - Square level: measurements covering the whole square.
    - Plot level: measurements within the square (e.g., vegetation, soils) taken on multiple plots.
  - Land Classification (ITE) stratification has evolved:
    - CS2000: 42 classes (Scotland reporting necessitated changes).
    - CS2007: 45 Land Classes (England, Wales, Scotland have country-specific classifications).
  - Measurements vary from binary to continuous.

- Estimation methods (pre-2007 context)
  - Stock estimates used means and standard errors by Land Class, then combined across Land Classes weighted by land area to yield regional/national estimates.
  - Change estimates relied on repeated measurements (paired surveys), while stock used all data from a survey—leading to inconsistencies between stock and change.

- Bootstrapping
  - Pre-CS2000 assumed normality for significance testing; CS2000 adopted bootstrap due to potential non-normality (especially for square-level data).
  - Bootstrap provides empirical distributions for estimates, enabling robust SEs and confidence intervals without strict distributional assumptions.

- Reasons for methodological modifications (to CS2007)
  - Inconsistencies: reported stock and change between survey pairs did not align because stock used all data and change used repeated data.
  - Need for consistent estimates across time, including non-adjacent surveys, and for both square and plot-level data.
  - Modelling approach can yield consistent and efficient (more precise) estimates, though it requires stronger distributional assumptions.
  - To maintain comparability and provide robust SEs, a dual-reporting check was implemented: old methods alongside new modelling methods.

- Modelling basics
  - Incomplete data techniques (e.g., EM-type approaches) enable modelling with data gaps, using correlation structures to infer missing information.
  - Mixed effects and repeated measures models are fitted to data from all surveys; fixed effects relate to land-class means over time; random effects capture hierarchical data structure and repeated measures.
  - For square-level data, the model includes fixed land-class effects and random square effects plus correlated survey residuals.
  - For plot-level data, plot-level residuals can be added to account for within-square variation; both square- and plot-level structures can be incorporated into bootstrapping.

- Square-level data modelling
  - y_ijk = a_i_k + s_ij + e_ijk, where:
    - a_ik: fixed effects (land-class means across surveys)
    - s_ij: square-level random effect
    - e_ijk: repeated-measures residual
  - Random effects: s_ij ~ N(0, τ_i^2); e_ijk ~ N(0, σ_ik^2) with covariances between surveys.
  - With K surveys, the model has 1 + K(K+1)/2 random parameters per land class; fixed effects are K per land class.
  - To manage complexity, random effects are reduced (e.g., AR1 structure) so the number of random parameters remains small and manageable.

- Plot-level data modelling
  - Plot-level data extend the square-level model by including plot-level residuals; this integrates within bootstrapping.
  - Two main modelling approaches:
    - Treat plots within squares as independent observations within land classes.
    - Include a plot-level random effect with correlations across surveys.
  - Both can be embedded in bootstrap procedures.

- Model specification (illustrative)
  - General form: y_ijk = a_ik + s_ij + e_ijk
  - Distributional assumptions: s_ij ~ N(0, τ_i^2), e_ijk ~ N(0, σ_ik^2) with cross-survey covariances; covariances may vary by land class and survey pair.

- Reducing model complexity (AR1 approach)
  - AR1 model assumes constant within-land-class variance over surveys and first-order autocorrelation of repeated measures across surveys.
  - Reduces random parameters to a small, stable set (three per Land Class per survey), facilitating automated analysis across many variables.
  - Bootstrap SEs are preferred when random-effect distributions are uncertain or potentially non-normal.

- Model testing and Broad Habitats
  - Broad Habitat analyses (based on square-level habitat proportions) were used to test modelling consistency across 1984, 1990, and 1998 data.
  - Old methodology produced inconsistencies between stock and change; modelling with AR1 produced consistent estimates and aligned change estimates with the sum of period changes.
  - Comparisons showed that differences between old and new methods were generally small relative to existing inconsistencies, supporting adoption of the modelling approach.

- Limitations and implications
  - Bootstrapped square-level analyses with full models can be computationally intensive; AR1 with bootstrap offers a practical balance.
  - Fixed-effects estimates (stock/change) are robust to some mis-specifications, but variance/covariance estimates are more sensitive; bootstrapping mitigates this.
  - Non-normal data can lead to convergence or estimation issues for certain variables (e.g., standing water in CS freshwater data); in some cases, older methods may be retained for specific variables.
  - Adopting a consistent modelling approach means past survey estimates may be updated with new data, reflecting information from all surveys; this is conceptually different from prior inconsistencies and is expected to yield small revisions over time.
  - The approach emphasizes using all available information, properly representing data hierarchy, and providing more precise, consistent estimates, while requiring standardized model selection for large-scale automated analyses.

- References
  - Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron & Tibshirani (1993); Scott (2002).
  - Acknowledges Countryside Survey data sources and the 2007 CS funding partners.