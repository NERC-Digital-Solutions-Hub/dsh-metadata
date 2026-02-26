# Notes on the downloadable data

- Privacy of locations: The precise locations of Countryside Survey (CS) field survey squares are held confidential by CEH; external users cannot identify whether squares fall within defined areas with precision better than 100 square km.

- Data structure and measurement levels: CS field survey data come from a sample of 1 km squares in GB. Each square is mapped and measured at two levels (the square as a whole and features within the square), with varied data types from binary to continuous (e.g., areas, lengths). Measurements include quadrats and other vegetation/soil information.

- Sampling design and stratification: The CS sample squares are not a random subset; they are stratified by the ITE Land Classification. The land-class classification has evolved (32 → 42 → 45 classes) with separate country classifications (England: 21, Wales: 8, Scotland: 16) and country-specific reporting. Analyses that ignore stratification may yield non-representative estimates and incorrect variation.

- Square inclusion/exclusion and representativeness: Squares with >90% sea or >75% urban area were excluded from field survey. Official GB and regional estimates assume excluded squares have similar vegetative land composition to sampled squares; this assumption is generally reasonable because the excluded portion is small, though it could bias results in regions with high sea/urban proportions.

- Estimation and uncertainty: Official estimates are produced using ratio estimates by land class, weighted by the vegetative land area of each class. Since 1998, standard errors and confidence intervals are estimated via bootstrap methods (Efron & Tibshirani) to address skewness.

- Practical implications for analysts:
  - Incorporate stratification and area-weighting in analyses.
  - Be mindful of location privacy constraints limiting precise geographic pinpointing.
  - Use bootstrap-derived uncertainty measures for inference.
  - Recognize the sampling design implications when generalizing to GB or regional scales.

- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.