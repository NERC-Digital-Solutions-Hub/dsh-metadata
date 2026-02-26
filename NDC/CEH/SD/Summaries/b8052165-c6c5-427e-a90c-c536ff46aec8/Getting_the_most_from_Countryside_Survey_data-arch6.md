# Notes on the downloadable data

- Precise locations of Countryside Survey (CS) field survey squares are confidential to protect representativeness; external users cannot identify square locations more precisely than 100 square km.
- CS field survey data come from a sample of 1 km squares in Great Britain, with measurements at two levels: whole square and within-square features (e.g., quadrats for vegetation, soils, etc.), using varied data types from binary to continuous.
- The sample is not random; it is stratified by the ITE Land Classification, with country-specific revisions:
  - 32 land classes originally, expanded to 42 in 1998 for Scotland, and to 45 in 2007 for Wales.
  - Separate classifications by country: 21 classes in England, 8 in Wales, 16 in Scotland.
- Not all GB squares were surveyed; exclusions include squares where area >90% sea or >75% urban (as defined from 1:250,000 OS maps). Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares, which may introduce bias mainly if a region has lots of sea/urban squares.
- Official estimates are produced as ratio estimates (Cochran, 1963) for each land class, weighted by vegetative land area within each class; land-class estimates are combined using the corresponding area weights for the class as a whole.
- Since 1998, to address skewness in some features, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993).
- Key methodological references:
  - Barr et al., Countryside Survey 1990 Main Report (1993)
  - Cochran, Sampling Techniques (2nd ed.) (1963)
  - Efron & Tibshirani, An Introduction to the Bootstrap (1993)