# Notes on the downloadable data

- The Countryside Survey (CS) Field Survey data are collected from a sample of 1 km squares across Great Britain, with measurements at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.). Measurements range from binary to continuous variables.
- The precise locations of CS survey squares are kept confidential by CEH to preserve representativeness, with a location precision no better than 100 square kilometers. This prevents external users from identifying whether squares fall within defined areas.

## Sampling design and data structure

- The CS sample squares are not a random subset; the sampling is stratified by land classification (ITE Land Classification). The classification has evolved over time and differs by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Square selection changes over time due to reporting requirements (e.g., Scotland, Wales) leading to country-specific classifications.
- Not all GB squares were considered for field survey. Squares were excluded if their area on 1:250,000 OS maps was more than 90% sea or more than 75% urban.
- Official GB estimates are produced using ratio estimates by land class, weighted by the area of vegetative land in each class. Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods to address skewness.

## Representativeness and limitations

- Estimates are representative only for the squares meeting the survey criteria; extrapolation to all GB squares assumes similarity of vegetative land in excluded squares, which may introduce bias if regions have disproportionate amounts of sea or urban land (generally small bias, but possible in regions with many excluded squares).
- Analysts must account for stratified sampling and the weighting scheme when interpreting estimates and their variation.

## Data confidentiality, access, and metadata

- The precise square locations are withheld, which has implications for data usability and spatial analyses.
- Data provenance matters: metadata quality and availability may require contacting the original data originators, and there may be barriers to sharing underlying datasets publicly.
- Data governance and data management standards apply; users may need to engage with dataset custodians to obtain metadata, understand transformations, and ensure proper use.

## Data processing, estimation, and references

- Measurements include a mix of binary and continuous variables, collected at both square and within-square scales.
- Two-stage sampling (whole square and within-square) informs how features are characterized and how estimates are produced.
- Estimation approach:
  - Ratios are used for land-class estimates.
  - Weights are based on the vegetative land area of each class.
  - Bootstrap (since 1998) provides standard errors and confidence intervals due to skewness in some features.
- References for the sampling framework and methods:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap

## Practical implications for monitoring frameworks

- When designing environmental health monitoring, account for:
  - Stratified, non-random sampling and country-specific land classifications
  - Exclusion criteria and potential biases in extrapolations beyond surveyed squares
  - The need for appropriate weighting and ratio-estimation methods
  - The use of bootstrap for robust uncertainty estimation
  - Data confidentiality constraints that limit precise geolocation and require careful handling of metadata
- Consider engaging with data originators to obtain complete metadata and ensure compliance with data governance and sharing requirements.