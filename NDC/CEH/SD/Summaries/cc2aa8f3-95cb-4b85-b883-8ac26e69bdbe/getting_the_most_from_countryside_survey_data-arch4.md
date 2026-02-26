# Notes on the downloadable data

- Confidentiality and access: UKCEH holds precise locations of Countryside Survey (CS) squares; external users cannot identify square locations with precision better than 100 square km. This limits ability to determine whether squares fall within specific defined areas below that threshold.
- Data structure: CS Field Survey data come from a sample of 1 km squares across Great Britain. Each selected square is mapped and measured at two levels: the whole square and features within the square (e.g., quadrats for vegetation, soils, etc.). Measurements span binary and continuous variables.
- Sampling design: The CS sample squares are not a random subset; they are stratified within Land Classification classes. Country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16; historically 32, then 42, then 45 with national reporting changes). Estimation must account for this stratification to avoid biased variation estimates.
- Exclusions and representativeness: Some squares (based on 1:250,000 OS maps) are excluded if more than 90% sea or more than 75% urban. Official GB estimates assume excluded land is similar in vegetation to sampled squares; bias is generally negligible except where a region contains many sea/urban squares.
- Estimation methodology: Estimates by land class are produced using ratio estimation (Cochran, 1963) with weights based on vegetative land area in each class. Land-class estimates are then combined using the corresponding vegetative land area as weights.
- Uncertainty and inference: Since 1998, standard errors and confidence intervals have been computed using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.
- References for methodology: Barr et al. (1993) Countryside Survey 1990 main report; Cochran (1963) Sampling Techniques; Efron & Tibshirani (1993) An Introduction to the Bootstrap.
- Practical implications for data strategy:
  - Ensure metadata clearly documents confidentiality constraints, sampling design, and estimation methods to enable appropriate reuse and interpretation.
  - When using CS data, account for stratification and the bootstrap-based uncertainty measures in analyses and reporting.
  - Be aware that GB-wide estimates rely on assumptions about excluded land; regional analyses may require caution if the region has a high proportion of sea/urban squares.
  - Maintain clear provenance and versioning of data products to reflect any updates to classifications or estimation approaches.
- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap.