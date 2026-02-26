# Notes on the downloadable data

- The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness. External users cannot know whether squares fall within defined areas to better than 100 square km precision.

## Sampling considerations in the Countryside Survey Data

- CS field survey data are from a sample of 1 km squares across GB. For each selected square, the square is mapped and detailed measurements are taken, with some measurements at the square level and others within-square.
- Measurements vary from binary (yes/no) to continuous (areas, lengths). There are two sampling levels: the entire square and sub-sampled within-square features (e.g., quadrats for vegetation, soils).
- The squares sampled are not a random subset of all GB squares. The sample is stratified, with sub-samples taken within designated strata defined by the ITE Land Classification.
- Land Classification history:
  - Original: 32 classes
  - 1998: expanded to 42 classes for Scotland reporting
  - 2007: expanded to 45 classes for Wales reporting
  - Result: England, Wales, and Scotland currently have country-specific classifications (21, 8, and 16 classes respectively).
- Estimates not accounting for stratification may be unrepresentative and have biased variation estimates.

## Exclusions and representativeness

- Not all GB squares were surveyed; squares with:
  - more than 90% sea area, or
  - more than 75% urban area (based on 1:250,000 OS maps)
  were excluded from field surveying.
- Official GB estimates assume that vegetative land in excluded squares is similar in composition to sampled squares. This is generally reasonable given the small total land involved, but regions with high sea/urban proportions may experience bias.

## Estimation and statistical methods

- Estimates by land class are produced as ratio estimates (Cochran, 1963), weighting by the vegetative land area within each land class.
- From 1998 onward, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness in some features.

## Practical implications for analysis

- When analysing CS data, account for stratification by land class and country-specific classifications.
- Apply appropriate weights based on the vegetative land area in each land class.
- Consider bootstrap-based standard errors and confidence intervals rather than assuming simple random sampling.
- Be mindful of the exclusion criteria and potential biases in regions with substantial sea or urban coverage; interpret estimates for such regions with caution.

## References

- Barr, C.J., Bunce, R.G.H., Clarke, R.T., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.