# Consistent Estimation for Countryside Survey 2007

## Executive summary
- The report describes a statistical methodology for Countryside Survey (CS) data analysis, detailing changes implemented for CS 2007 to achieve consistent stock and change estimates.
- Previous methods used little data for change estimates (repeat measurements only) while using all data for stock, causing inconsistencies between stock and change.
- Modelling approaches using CS Broad Habitat data showed that consistent estimation is feasible and robust; differences from old methods are generally small relative to existing inconsistencies.
- A modelling-based approach has been adopted for 2007, leveraging all available information to produce more precise estimates, with potential small updates to past results as new data are incorporated.
- Implementing modelling is technically challenging and computationally intensive but yields a substantially improved product.

## 1. Introduction
- CS data are collected from a stratified sample of 1 km squares on a 15 km GB grid, with two levels of sampling within each square (square-wide and within-square plots).
- Data types range from binary to continuous measurements; Land Classification (ITE) defines strata with country-specific classifications (England, Wales, Scotland) for reporting.
- The 2007 methodology changes focus on consistent estimation of stock and change across surveys, moving beyond the previous practice of mixing data sources across surveys.

## 2. Overview of previous CS methodology
- Stock estimates used all data from a survey; change estimates used only repeated measurements across survey pairs.
- This led to mismatches where stock changes did not equal observed changes, and inconsistencies between adjacent and non-adjacent survey changes.
- Bootstrapping was used for significance testing due to skewness in some measurements; normality assumptions were avoided for square-level data.

## 3. Reasons for modifications to CS methodology
- Point estimates (stock and change) from old methods appeared inconsistent when comparing changes across surveys, though not due to data errors.
- Differences arose because missing information (e.g., unrepeated squares) affected stock and change estimates differently.
- The shift in reporting focus (timeline from first survey to present) increased the need for truly consistent estimates across all surveys.
- Modelling approaches offer consistency and efficiency, applying to both square- and plot-level data, with bootstrap-based standard errors providing robust uncertainty measures.

## 4. Consistent estimation

### 4.1 Possible approaches
- Considered several ways to achieve consistency; using stock estimates for all measurements and deriving change from stock differences is robust and easy but inefficient for some data types and may not extend well to plot-level data.
- Modelling stock and change together offers consistency and efficiency but requires stronger distributional assumptions.

### 4.2 Modelling basics
- Incomplete data are handled via mixed-effects/repeated-measures models, requiring fixed effects (stock/change means by land class and survey) and random effects (variation between squares, within-square repeated measures).
- Estimation uses all surveys, linking past and future data; this can update past estimates as new data arrive.

### 4.3 Square level data
- For complete 1 km squares, a repeated-measures mixed model is used: fixed effects for land-class means per survey, random square effects, and correlated residuals over surveys.
- The model structure grows in complexity with more surveys; to keep models tractable, random-effect parameters are reduced.

### 4.4 Plot level data
- Plot-level data within squares can be analyzed with models that include plot-level random effects in addition to square-level effects.
- This allows proper handling of hierarchical data and correlations across plots and squares, integrated within bootstrapping.

### 4.5 Model specification
- General model: y_ijk = a_ik + s_ij + e_ijk, where:
  - a_ik: fixed effects (land class i, survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Random effects are typically normal, with variances possibly differing by land class; covariances between surveys can be modeled.
- To keep the model parsimonious, assumptions such as common variance across surveys (sigma_i) and autoregressive AR1 structure for covariances are used, reducing parameters to a manageable number.

### 4.6 Model testing – Broad Habitats
- Broad Habitat data (proportions of land within a square by habitat category) from 1984, 1990, 1998 were analyzed to test modelling approaches.
- Old methods showed clear inconsistencies between stock and change; AR1-based modelling produced consistent estimates, with changes matching sums of period changes.
- Comparisons indicated that differences between old and new methods were generally small relative to existing inconsistencies.
- CS adopted the modelling approach for 2007 and extended consistency checks to plot-level data (soil data and plotting datasets).

## 5. Limitations and implications
- Bootstrapping within square-level data with AR1 models is computationally intensive; fully parameterised models are slow and impractical for large numbers of variables.
- The AR1 model provides robustness and efficiency for fixed effects, but variance/covariance parameters are more sensitive to distributional assumptions.
- In practice, the AR1 approach with bootstrap standard errors is used to balance robustness and computational feasibility.
- Some very non-normal data (e.g., standing water) may lead to convergence issues or local maxima; in such cases, old methodologies may be preferred for reporting those variables.
- Because analyses use data from all surveys, past survey estimates may be updated as new surveys are added; this is conceptually different from older reporting inconsistencies and is considered reasonable given the new information.
- Adopting a consistent, automated model-based approach improves efficiency and precision but requires careful interpretation of trends and transparency about methodological changes.

## 6. Implications for GIS and data products
- Produces more precise, consistent stock and change estimates across square and plot levels, enhancing map-based data products for policy, clients, and public audiences.
- Enables integrated temporal analyses across surveys, improving trend visualization and spatial planning across England, Wales, and Scotland.
- Requires clear documentation of model assumptions, data handling, and potential updates to past results when new surveys are added.
- Involves greater computational resources and automated processes to maintain consistency across large datasets and numerous variables.

## References
- Barr et al. (1993); Haines-Young et al. (2000); Dempster et al. (1977); Efron and Tibshirani (1993); Scott (2002).