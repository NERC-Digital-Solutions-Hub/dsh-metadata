# Notes on the downloadable data

## Confidentiality and data access
- To preserve representativeness, the precise locations of Countryside Survey (CS) field survey squares are confidential; external users cannot identify square locations with precision better than 100 square km.
- Consequently, users cannot determine whether any survey squares fall within defined areas below this threshold.

## Countryside Survey data overview
- CS field survey data come from a sample of 1 km squares in Great Britain (GB).
- Each selected square is mapped and measured at two levels: the square level (characterising the whole square) and within-square (describing features inside the square).
- Measurements include a mix of binary (yes/no) and continuous variables (e.g., areas, lengths).

## Sampling design and representativeness
- The CS sample squares are not a random subset; the sampling is stratified within designated strata defined by the ITE Land Classification.
- Land Classification classifications have changed by country:
  - England: 21 classes
  - Wales: 8 classes
  - Scotland: 16 classes
- Since 1998, estimates that do not account for stratification may be non-representative and have inaccurate variation estimates.
- Some GB squares were excluded from field survey:
  - Excluded if more than 90% sea or more than 75% urban (based on 1:250,000 OS maps).
- In practice, GB-wide estimates assume vegetative land in excluded squares is similar to sampled squares; the bias is generally negligible, except potentially in regions with a high proportion of sea or urban squares.

## Estimation methods and uncertainty
- Official land-class estimates are produced using ratio estimates (Cochran, 1963), weighted by the vegetative land area in each land class.
- Estimates are then combined across land classes using the area of vegetative land as weights.
- From 1998, bootstrap methods (Efron and Tibshirani, 1993) are used to estimate standard errors and confidence intervals due to skewness in some features.

## Practical considerations for analysts
- When using CS data, account for stratified sampling by ITE Land Classification to obtain valid inferences.
- Be mindful of potential biases if analyses involve regions with high proportions of sea or urban squares.
- Use ratio-estimate framing and bootstrap-derived uncertainty measures as appropriate for robust interpretation.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.