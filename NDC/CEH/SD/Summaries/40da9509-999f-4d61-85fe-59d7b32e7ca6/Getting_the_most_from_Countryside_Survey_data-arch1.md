# Notes on the downloadable data

- Data confidentiality
  - Precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH.
  - External users cannot identify whether squares fall within defined areas with precision better than 100 square km.
  - This limits the ability to map survey squares to very fine geographic units.

- Sampling design and structure
  - CS field data come from a sample of 1 km squares across Great Britain (GB).
  - Two sampling levels: whole squares and within-square measurements (e.g., quadrats for vegetation, soils).
  - Measurements cover varied types, from binary to continuous variables.
  - The sampling is not a simple random sample; it is stratified by Land Classification within each country.
  - Land Classification classifications differ by country and over time:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Changes over time: 1998 (Scotland reporting adjustments) and 2007 (Wales reporting adjustments) led to country-specific classifications.

- Exclusions and representativeness
  - Some squares were excluded from field survey if their area was >90% sea or >75% urban (based on 1:250,000 OS maps).
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares; bias is generally small unless a region has many sea/urban squares.

- Estimation methods and uncertainty
  - Estimates are produced as ratio estimates by land class, weighting by vegetative land area within each land class.
  - Weights are based on the vegetative land area for each land class to form GB-wide estimates.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods (Efron and Tibshirani, 1993) due to skewness concerns.

- Practical implications for analysis
  - Analyses must account for the stratified sampling design to obtain representative estimates and accurate variation.
  - Ignoring stratification can lead to biased estimates of variation.
  - When extrapolating to whole GB or regions, be aware of the underlying assumption that excluded squares resemble sampled squares in vegetative composition.
  - Data encompass multiple scales (square-level and within-square features) and variable types (binary, continuous).

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report, DETR, London.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.). Wiley & Sons; London.
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap. Chapman and Hall; London.