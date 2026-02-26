# Notes on the downloadable data

## Overview of data confidentiality and precision
- The precise locations of Countryside Survey (CS) survey squares are kept confidential by CEH to preserve representativeness of the wider countryside.
- External users cannot identify survey squares with precision better than 100 square kilometers.
- Consequently, it is not possible to determine whether any survey squares fall within defined areas below this threshold.

## Sampling structure and data types
- CS field survey data come from a sample of 1 km squares across Great Britain (GB).
- Each selected square is mapped and multiple measurements are made, including quadrats for vegetation, soils, etc.
- There are two levels of sampling:
  - Whole-square level (characterizes the square)
  - Within-square level (describes features inside the square)
- Measurements span varied types, from binary yes/no variables to continuous metrics such as areas or lengths.

## Sampling design and its implications
- The CS sample squares are not a random subset of all GB squares.
- It is a stratified sample with sub-samples within designated strata defined by the ITE Land Classification.
- Land Classification changes over time:
  - Originally 32 classes
  - 1998: expanded to 42 classes (Scotland reporting)
  - 2007: expanded to 45 classes (Wales reporting)
  - Each country effectively has its own classification (England: 21 classes, Wales: 8, Scotland: 16)
- Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

## Exclusions and representativeness
- Some GB squares were not considered for field survey:
  - Excluded if their area (per 1:250,000 OS maps) was more than 90% sea or more than 75% urban.
- Field survey data are representative only of the squares that meet these criteria.
- In practice, GB or regional estimates assume vegetative land in excluded squares is similar to that in sampled squares.
- Bias from this assumption is likely negligible overall, unless a region has a high proportion of sea or urban squares.

## Estimation and uncertainty
- Official estimates are produced as ratio estimates (Cochran, 1963) for each land class, weighted by the vegetative land area in each class.
- Since 1998, standard errors and confidence intervals have been estimated using bootstrap methods (Efron and Tibshirani, 1993) due to concerns about skewness in some features.

## References
- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. and Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.