# Notes on the downloadable data

- Privacy and data access: The precise locations of Countryside Survey (CS) field squares are kept confident by CEH. External users cannot identify whether squares fall within defined areas with precision finer than 100 square kilometers.

- Data structure: CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels—square level (characterising the whole square) and within-square (specific features inside the square). Variables range from binary to continuous (e.g., areas, lengths).

- Representativeness and sampling design: The sample is not random but stratified within designated strata defined by land classification (ITE). Land classification classifications have been country-specific and have evolved over time (England: 21 classes; Wales: 8; Scotland: 16). Estimates not accounting for stratification may be biased or have incorrect measures of variation.

- Excluded areas and implications: Squares with more than 90% sea or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys. Official estimates assume excluded vegetative land is similar to surveyed land; this assumption is generally reasonable because the excluded land covers a small total area, but regional biases can occur if a region has a high share of sea/urban squares.

- Estimation approach: CS estimates are produced as ratio estimates by land class, weighting by the vegetative land area within each class. From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods due to concerns about skewness of some features.

- Data provenance and references: Core methodological references include Barr et al. (1993) Countryside Survey 1990 Main Report; Cochran (1963) Sampling Techniques; Efron and Tibshirani (1993) The Bootstrap.

- Practical implications for users and data leaders:
  - Always account for stratification by land class and country-specific classifications when analysing CS data.
  - Use the provided weights (based on vegetative land area) to obtain representative estimates.
  - Be mindful of the limitations due to excluded squares and potential regional biases.
  - Rely on bootstrap-based uncertainty estimates for standard errors and confidence intervals.
  - Maintain awareness of the privacy constraints around square locations when sharing or publishing maps or analyses.

- What the data enable: Detailed, multi-level measurements of vegetation, soils, and related features across GB squares, suitable for understanding landscape-level patterns while recognizing sampling design and data limitations.

- References cited:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.