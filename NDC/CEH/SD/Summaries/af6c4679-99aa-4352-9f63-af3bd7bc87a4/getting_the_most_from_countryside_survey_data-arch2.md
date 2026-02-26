# Notes on the downloadable data

- Purpose: Describe how Countryside Survey (CS) data are collected, processed, and analyzed to preserve representativeness and guide proper use by researchers.

## Key confidentiality and geographic precision

- Precise locations of Countryside Survey squares are kept confidential by UKCEH.
- External users cannot identify survey squares with precision greater than 100 square kilometres.
- As a result, users cannot determine whether specific survey squares fall within defined areas below this threshold.

## Sampling design and data structure

- CS field survey data come from a sample of 1-km squares across Great Britain (GB).
- Each selected square is mapped and measurements are taken at two levels:
  - Whole-square level (characteristics of the entire square).
  - Within-square level (features described inside the square, e.g., quadrats for vegetation, soils, etc.).
- Measurements include a mix of data types (binary yes/no variables and continuous measurements such as areas or lengths).

## Sampling approach and representativeness

- The CS sample squares are not a random subset of all 1-km GB squares.
- The sample is stratified, with sub-samples within designated strata defined by the ITE Land Classification.
- Land classifications have changed over time and differ by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Estimates that do not account for stratification may not be representative and can have incorrect variation estimates.

## Exclusions and implications for analyses

- Not all GB 1-km squares were surveyed; squares with area >90% sea or >75% urban (based on 1:250,000 scale OS maps) were excluded from field surveys.
- The field survey data thus represent only the included squares; GB-wide or regional estimates assume excluded vegetative land is similar to sampled land. This assumption may introduce bias mainly in regions with high sea or urban square proportions but is generally small because the excluded area is limited.

## Estimation methods and uncertainty

- Official GB estimates are produced using ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron & Tibshirani, 1993) to address skewness in some features.

## Practical implications for analysts

- When using CS data, apply stratification by Land Classification and incorporate area-based weights.
- Use ratio estimates where appropriate and account for the sampling design in variance estimation (prefer bootstrap SEs/CIs).
- Be mindful of potential biases from excluded squares, especially in regions with substantial sea or urban areas.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.