# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness of the wider countryside; external users cannot identify square locations to a precision better than 100 square km.
- CS Field Survey data come from a sample of 1 km squares in Great Britain, with two sampling levels: whole squares and within-square features (e.g., quadrats for vegetation, soils).
- Measurements cover varied types, from binary to continuous (areas, lengths), with some characterising the square and others within-square features.
- The CS sample is not a random subset; it is stratified by the ITE Land Classification. The land-class classifications have evolved:
  - Original: 32 classes
  - 1998: 42 classes ( Scotland reporting requirements)
  - 2007: 45 classes ( Wales reporting requirements)
  - Current: England 21 classes, Wales 8, Scotland 16 (country-specific classifications)
- Some squares were excluded from field survey:
  - Areas more than 90% sea, or more than 75% urban (based on 1:250,000 OS maps)
  - Estimates for GB or regions assume excluded vegetative land is similar to sampled land; this generally produces negligible bias, except in regions with high sea/urban proportions.
- Official estimates use ratio estimation (Cochran, 1963) for each land class, weighting by the vegetative land area within each class; combined estimates use weights from the total vegetative land area in each class.
- Since 1998, standard errors and confidence intervals have been estimated with the bootstrap (Efron & Tibshirani, 1993) due to skewness concerns.
- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report
  - Cochran (1963). Sampling Techniques (2nd ed.)
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap