# Notes on the downloadable data

- Countryside Survey (CS) field survey data come from a sample of 1 km squares in Great Britain (GB), with measurements at both the square level and within-square features (e.g., quadrats for vegetation, soils).
- Measurements are varied, including binary and continuous variables, collected to characterise each square and its internal features.
- The sampling is not a simple random subset; it is stratified by the ITE Land Classification, with country-specific classifications (England: 21 classes, Wales: 8, Scotland: 16) and changes over time (1998 Scotland reporting, 2007 Wales reporting).

## Location confidentiality

- To preserve representativeness of the wider countryside, precise square locations are kept confidential by UKCEH.
- External users cannot identify whether survey squares fall within defined areas with precision finer than 100 square kilometres.

## Sampling design and representativeness

- The field survey covers only squares meeting specific criteria: island/sea and urban coverage exclusions (not more than 90% sea or 75% urban within a square).
- Consequently, CS estimates are representative only of the included squares; GB-wide estimates assume similarity in vegetative land composition between included and excluded squares, which may introduce bias if regional differences are large.
- Estimates are derived using ratio methods for each land class, weighted by the vegetative land area of each class.

## Analysis methods and uncertainty

- Standard errors and confidence intervals are estimated using bootstrap methods (since 1998) due to skewness concerns in some features.
- Analysis must account for the stratified sampling design to avoid biased estimates and incorrect variation assessment.

## Data usage and outputs

- Data are prepared and presented in clear formats such as reports, maps, and charts.
- Datasets are stored and uploaded to appropriate data portals, aligning with standardized processing and accessibility aims.

## Considerations for data users

- Understanding and incorporating the stratification, weighting, and sampling exclusions is essential for valid analyses.
- While GB-wide estimates are possible, they rely on assumptions about excluded areas and should be interpreted with awareness of potential regional biases.

## References

- Barr, C.J., et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
- Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
- Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.