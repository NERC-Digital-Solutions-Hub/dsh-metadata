# Notes on the downloadable data

## Key GIS implications
- Precise locations of Countryside Survey (CS) squares are confidential; external users can only identify squares to a precision of 100 square kilometres.
- This confidentiality limits the ability to determine whether specific survey squares fall within defined, smaller areas in spatial analyses.

## Sampling design and spatial scope
- CS data come from a 1 km square sampling framework across Great Britain (GB); each square is mapped and measured at two levels: the whole square and features within the square.
- Data types range from binary (yes/no) to continuous (areas, lengths).
- Sampling is not random but stratified by the ITE Land Classification, with country-specific classifications: England (21 classes), Wales (8), Scotland (16). Historically, classifications expanded from 32 to 42 (1998 for Scotland) and 45 overall (2007 for Wales-related reporting changes).
- Estimates ignoring stratification may be unrepresentative and misrepresent variation.

## Excluded areas and representativeness
- Squares with more than 90% sea or more than 75% urban land (as measured from 1:250,000 OS maps) were excluded from survey.
- Official GB estimates are produced using ratio estimates by land class, weighted by the vegetative land area within each class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness.

## Implications for mapping and analysis
- GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares; this assumption introduces potential bias, particularly in regions with high sea/urban proportions.
- When using CS data in GIS:
  - Be mindful of stratification and country-specific land-class classifications.
  - Apply appropriate area-based weights and consider bootstrap-derived uncertainty.
  - Acknowledge confidentiality-imposed precision limits (100 km²) when spatially intersecting with finer-scale boundaries.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.