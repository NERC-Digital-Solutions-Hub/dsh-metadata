# Notes on the downloadable data

## Overview of the Countryside Survey data
- Field data come from a sample of 1 km squares across Great Britain.
- Each selected square is mapped and detailed measurements are taken within the square (e.g., quadrats for vegetation, soils, etc.), yielding two sampling levels: whole square and within-square.
- Measurements span binary (yes/no) to continuous variables (areas, lengths).

## Confidentiality and data access
- To preserve representativeness of the wider countryside, precise locations of CS survey squares are kept confidential.
- External users are not provided with location precision finer than 100 square kilometres; you cannot determine whether a given square falls inside defined areas at finer scales.

## Sampling design and representativeness
- The CS sample squares are not a random subset; they are stratified within designated strata.
- Land Classification stratification has evolved:
  - Originally 32 classes; expanded to 42 in 1998 for Scotland reporting.
  - Further revision to 45 classes in 2007 for Wales reporting.
  - Consequently, England has 21 classes, Wales 8, Scotland 16.
- Not all GB squares were surveyed; excluded squares are those with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps).
- Official estimates assume vegetative land in excluded squares is similar to sampled squares; bias is typically small except in regions with high sea/urban proportions.

## Estimation and uncertainty
- Estimates are produced as ratio estimates by land class, weighting by the vegetative land area within each class.
- Standard errors and confidence intervals are estimated via bootstrap methods since 1998, addressing skewness in some features.

## Implications for data use and governance (Data Leaders perspective)
- When analyzing CS data, incorporate stratification by land class and the weighting scheme to obtain representative estimates.
- Acknowledge limitations due to non-random sampling and exclusions; regional estimates may be biased if the region contains many sea or urban squares.
- Use bootstrap-derived uncertainty measures to quantify precision.
- Maintain awareness of confidentiality constraints that limit ultra-fine geographic inferences.
- Consult the cited methodological references for deeper understanding of sampling and estimation procedures.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.