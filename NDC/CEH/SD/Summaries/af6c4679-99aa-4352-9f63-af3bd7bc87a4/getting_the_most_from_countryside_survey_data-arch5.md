# Notes on the downloadable data

## Purpose and privacy of data
- Delineates how Countryside Survey (CS) field data are collected and how to handle them responsibly.
- Precise locations of CS squares are kept confidential and are not disclosed to external users with precision finer than 100 square km.
- This privacy measure prevents identification of whether CS squares fall within defined areas, informing risk management and analytical scope.

## Sampling design and levels
- Data come from a sample of 1-km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
- Measurements cover a range of data types, from binary to continuous (areas, lengths).

## Representativeness and selection
- CS squares are not a simple random sample of all 1-km GB squares.
- The sample is stratified by the ITE Land Classification into designated strata; country-specific classifications exist (England: 21 classes, Wales: 8, Scotland: 16).
- Historic changes: Land Classification evolved from 32 classes (original) to 42 (1998) and 45 (2007) to support separate country reporting.
- Official estimates are conditioned on stratification and area of vegetative land within each land class.

## Exclusions and practical implications
- Some squares were excluded from field survey: squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps).
- GB-wide estimates assume similarity between vegetative land in excluded squares and sampled squares; this assumption minimizes bias unless a region is unusually dominated by sea or urban land.

## Estimation methods and uncertainty
- Estimates for land classes are produced using ratio estimation techniques (Cochran, 1963), weighted by vegetative land area within each class.
- Since 1998, to address skewness in some features, standard errors and confidence intervals are estimated using bootstrap methods (Efron & Tibshirani, 1993).

## Implications for data use and analysis
- Analyses must account for stratified sampling and weighting; failing to do so may yield biased estimates or incorrect variation.
- Users should be aware that estimates are representative of the sampled squares and the vegetative land within classes, not necessarily all GB squares.
- Special care when interpreting results for regions with high proportions of sea or urban land, due to potential bias from exclusions.

## References (methodology and provenance)
- Barr, C.J. et al. Countryside Survey 1990 Main Report (DETR, London).
- Cochran, W.G. Sampling Techniques (2nd ed.) (1963).
- Efron, B. & Tibshirani, R.J. An Introduction to the Bootstrap (1993).