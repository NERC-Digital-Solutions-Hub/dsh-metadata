# Notes on the downloadable data

- Confidentiality of locations: The precise locations of Countryside Survey (CS) field squares are kept confidential by CEH; external users cannot identify square locations to better than 100 square km, limiting fine-grained geographic identification.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: the square itself and features within the square (e.g., quadrats for vegetation, soils).
- Measurements are of varied types, from binary (yes/no) to continuous (areas, lengths).
- The sampling is not a simple random subset; it is stratified by the ITE Land Classification. Country-specific versions exist:
  - England: 21 land classes
  - Wales: 8 land classes
  - Scotland: 16 land classes
- The land classification has evolved: originally 32 classes, then 42 (1998) for Scotland, and 45 (2007) with Wales reporting requirements.

## Coverage and representativeness

- Not all GB squares were considered for field survey. Squares with >90% sea or >75% urban area were excluded.
- Official GB estimates assume that vegetative land in excluded squares is similar in composition to sampled squares. This assumption is usually reasonable because the excluded area is small; risk of bias increases if a region has a high proportion of sea or urban squares.

## Estimation and inference

- Estimates by land class are produced using ratio estimation (Cochran, 1963), weighting by the vegetative land area within each land class.
- Since some features are skewed, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) from 1998 onward.

## Practical implications for analysts

- Analyses must account for stratification by land class and the use of area-based weights; naïve estimates ignoring stratification may be biased.
- Because the sample is not random and includes exclusions, extrapolations to the whole GB or large regions should be used with caution, particularly in areas with substantial sea or urban cover.
- When combining data across years or countries, ensure comparability of land classifications and note any changes in classification schemes.
- Be mindful of data provenance and metadata, and reference the provided methodologies (ratio estimates, bootstrap SEs) when reporting uncertainty.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.