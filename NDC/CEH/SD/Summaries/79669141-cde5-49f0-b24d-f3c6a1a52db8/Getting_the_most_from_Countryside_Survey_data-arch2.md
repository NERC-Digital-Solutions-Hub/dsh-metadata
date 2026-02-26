# Notes on the downloadable data

- To preserve the representativeness of the wider countryside, the precise locations of Countryside Survey (CS) field squares are kept confidential by CEH; external users will not receive square locations with precision better than 100 square kilometers.
- As a result, users cannot determine whether particular survey squares fall within defined areas at finer spatial scales.

## Sampling design and data structure

- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and measured at two levels: 
  - Whole-square level (characterising the square)
  - Within-square level (detailed measurements from quadrats on vegetation, soils, etc.)
- Measurements include both binary (yes/no) variables and continuous metrics (areas, lengths, etc.).

## Sampling design specifics

- The sample squares are not a random subset of all GB squares; it is a stratified sample with sub-samples within designated strata defined by the ITE Land Classification.
- Land Classification evolution:
  - Originally 32 classes
  - 1998: Scotland reporting required, classification expanded to 42 classes
  - 2007: Wales reporting required, classification expanded to 45 classes
  - Effectively, England, Wales, and Scotland each have separate classifications (England: 21 classes, Wales: 8, Scotland: 16).

## Representativeness and estimation implications

- Estimates that do not account for stratification may be unrepresentative and have inaccurate measures of variation.
- Not all GB squares were surveyed; some were excluded if their area was more than 90% sea or more than 75% urban (as defined at 1:250,000 OS map scale).
- Official GB estimates (and regional estimates) assume that vegetative land in excluded squares is similar in composition to sampled squares; this assumption introduces potential bias, which is likely small unless a region contains a high proportion of sea or urban areas.

## Calculation methods and uncertainty

- Land class estimates are produced using ratio estimates (Cochran, 1963), weighting by the vegetative land area within each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) to address skewness in some features.

## Practical implications for analysts

- When using CS data, account for stratification and the weighting scheme by land class and vegetative area.
- Use ratio-estimator outputs and bootstrap-based uncertainty measures for inference.
- Be mindful of confidentiality constraints that limit spatial precision and consider the implications for spatial analyses at fine scales.
- Recognize that some GB areas (sea/urban-dominated) are underrepresented due to exclusions, and interpret regional results with this caveat.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.