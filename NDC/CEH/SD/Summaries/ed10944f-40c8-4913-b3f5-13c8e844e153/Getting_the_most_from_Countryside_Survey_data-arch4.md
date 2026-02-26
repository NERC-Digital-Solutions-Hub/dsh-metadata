# Notes on the downloadable data

- Confidentiality of precise locations
  - The exact locations of Countryside Survey (CS) squares are kept confidential by CEH.
  - External users cannot identify squares with precision finer than 100 square kilometers, limiting the ability to determine if squares fall within specific areas.

- Data structure and sampling levels
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Two sampling levels: whole squares and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include both binary and continuous variables.

- Sampling design and stratification
  - The sampling is not random; it is stratified by land classification (ITE Land Classification).
  - Country-specific classifications have evolved:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Historically, classifications expanded from 32 classes (original) to 42 (1998 Scotland) to 45 (2007 Wales-related). Each country effectively has its own classification.

- Representativeness and weighting
  - Estimates from CS must account for stratification; naïve (unstratified) estimates may be biased.
  - Official estimates for GB use ratio estimates by land class, weighting by vegetative land area in each class.
  - Some squares were excluded from field surveys based on area criteria (more than 90% sea or more than 75% urban) and this affects coverage.

- Coverage caveats and assumptions
  - The field survey is representative only of squares meeting the exclusion criteria.
  - For GB or regional estimates, it is assumed that vegetative land in excluded squares resembles that in sampled squares. This assumption may introduce bias, especially in regions with high sea or urban proportions; the impact is generally small but context-dependent.

- Uncertainty and statistical methods
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

- Practical implications for data users (Data Leaders perspective)
  - Always account for stratification and weighting when analyzing CS data.
  - Use the appropriate country/class-specific classifications and be aware of changes over time.
  - Consider the confidentiality constraints when linking CS data to other geographies or precise location-based analyses.
  - Check bootstrap-based uncertainty estimates for robust inference.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron and Tibshirani (1993). An Introduction to the Bootstrap.