# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across GB, with measurements at two levels: the square as a whole and features within the square.
- Data are not a random sample; they are stratified by land classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16) that have evolved over time (32 → 42 → 45 classes).
- To protect representativeness, precise square locations are confidential: external users cannot identify squares with precision better than 100 square kilometers.

## Sampling design and data structure
- Each selected square is mapped; quadrats are used to collect additional information on vegetation, soils, etc.
- Measurements include binary and continuous variables.
- Some squares are excluded from field survey: areas more than 90% sea or more than 75% urban, based on 1:250,000 scale OS maps.
- Because of the sampling design, CS data are not fully representative of all GB squares; official estimates rely on ratio estimates by land class, weighted by vegetative land area.

## Representativeness and limitations
- Estimates for GB or regional levels assume excluded squares have similar vegetative composition to sampled squares; this is unlikely to be exact but the area of excluded land is typically small, so bias is generally negligible. Regions with high sea/urban proportions could be problematic.

## Estimation and uncertainty
- Official estimates are produced using ratio estimation (Cochran, 1963) within each land class, then combined using weights equal to the vegetative land area of each land class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

## Practical implications for Data Leaders
- Data understanding: must account for stratified sampling and country-specific land classifications when planning analysis or reporting.
- Metadata and data quality: classification schemes, area measures, exclusion criteria, and bootstrap-based uncertainty estimates are essential metadata.
- Data access and privacy: location confidentiality (100 km2 precision) may affect geospatial analyses or disaggregation at fine resolutions.
- Data integration and governance: when combining CS data with other datasets, respect the stratification, weighting, and potential extrapolation caveats; consider the implications of non-random square inclusion.

## References
- Barr, C.J. et al. 1993. Countryside Survey 1990 Main Report.
- Cochran, W.G. 1963. Sampling Techniques.
- Efron, B. & Tibshirani, R.J. 1993. An Introduction to the Bootstrap.