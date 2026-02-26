# Notes on the downloadable data

## Overview
- Countryside Survey (CS) field data come from a sample of 1 km squares across Great Britain, with measurements made at both the square level and within-square features (e.g., quadrats for vegetation, soils, etc.). Variables range from binary to continuous.
- To preserve representativeness, precise locations of survey squares are confidential: external users cannot identify squares with precision finer than 100 square kilometres.

## Sampling design and classification
- The sampling design is stratified by Land Classification (ITE), with country-specific adaptations.
- Land Classification history:
  - Originally 32 classes.
  - 1998: Scotland reporting required, increasing to 42 classes.
  - 2007: Wales reporting requirement increased to 45 classes.
  - Current practice effectively yields 21 classes in England, 8 in Wales, and 16 in Scotland.
- Not all GB squares are surveyed: squares with >90% sea or >75% urban area are excluded from field surveys.
- Official GB or regional estimates assume vegetative land in excluded squares is similar to sampled squares, which may introduce bias, particularly if a region contains many sea or urban squares.

## Data access and confidentiality
- The confidentiality policy restricts precise square locations; users cannot determine whether a square falls within defined areas below the 100 square km precision threshold.

## Estimation, analysis, and uncertainty
- Estimates are produced as ratio estimates by land class, weighted by the vegetative land area within each land class.
- Land-class estimates are combined using weights corresponding to the broader vegetative land area of each land class.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to skewness in some features.

## Limitations and cautions for analysis
- The CS data are not a random sample; analyses must account for stratification and weighting to avoid biased inferences.
- Extrapolations to whole GB or particular regions should be treated with caution, especially if the region includes a high proportion of excluded squares (sea/urban).

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report. DETR, London.
- Cochran, W.G. (1963). Sampling techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap. Chapman and Hall; London.

## Implications for Data Leaders
- Ensure metadata clearly documents: sampling design, stratification, land-class classification changes, square exclusions, and weighting schemes.
- Provide guidance on bootstrap-based uncertainty estimates and appropriate use of ratio estimates.
- Maintain transparency about confidentiality constraints and how they affect spatial analyses.
- Facilitate user understanding of non-random sampling and the need for appropriate weighting and stratified analysis to support robust decision-making.