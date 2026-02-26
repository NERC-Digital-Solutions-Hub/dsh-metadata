# Notes on the downloadable data

- CEH holds precise locations of Countryside Survey (CS) field survey squares confidential to preserve representativeness; external users cannot identify squares to better than 100 square kilometres.
- CS field survey data come from a sample of 1 km squares across Great Britain, with two sampling levels: the square level (mapped and measured features) and within-square level (quadrats and additional information on vegetation, soils, etc.). Measurements include binary and continuous variables.
- The sample squares are not a random subset; they are stratified within the ITE Land Classification framework. Over time, classifications have been updated: originally 32 classes; 1998 expanded to 42 (separate Scotland reporting); 2007 expanded to 45 (separate Wales reporting). England has 21 classes, Wales 8, Scotland 16.
- Estimates derived from CS data depend on stratification; analyses that ignore stratification may be unrepresentative. Official GB and regional estimates use ratio estimation by land class and weight by vegetative land area within each class.
- Not all GB squares were surveyed: squares with more than 90% sea or more than 75% urban area were excluded from field survey. Estimates for GB or regions assume excluded squares are similar in vegetative composition to sampled squares; this bias is generally small except in regions with high sea/urban proportions.
- Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness (Efron and Tibshirani, 1993).
- Data provenance and accessibility considerations:
  - The requirement to publicly share datasets can be a barrier to reuse of some existing data.
  - Metadata quality may be inadequate, complicating reuse or verification.
  - To support monitoring, researchers may need to apply ratio-estimation procedures and account for the complex sampling design and weighting.
- References:
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.