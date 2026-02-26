# Notes on the downloadable data

- Purpose of notes: To preserve representativeness of the wider countryside and guide proper use of Countryside Survey (CS) data, including understanding sampling, estimation, and limitations.

- Location confidentiality: Precise locations of CS survey squares are kept confidential by CEH; external users cannot identify squares with precision better than 100 square km, so users cannot determine whether squares fall within defined areas below this threshold.

- Sampling design overview:
  - CS field survey data come from a sample of 1 km squares in Great Britain (GB).
  - Each selected square is mapped and measured at two levels: the square level and within-square features (e.g., quadrats for vegetation, soils, etc.).
  - Measurements include a mix of binary (yes/no) and continuous variables (areas, lengths).

- Stratified sampling and classification:
  - Squares are not a random subset; they are stratified by the ITE Land Classification.
  - Land classification counts have evolved: 32 classes originally, 42 in 1998 (due to Scotland reporting), and 45 classes after 2007 (due to Wales reporting), resulting in country-specific classifications (England 21, Wales 8, Scotland 16).
  - Estimates that do not account for stratification may be unrepresentative and have inaccurate variation estimates.

- Exclusions and representativeness:
  - Squares with more than 90% sea area or more than 75% urban area are excluded from field surveys.
  - Official GB estimates are based on the included squares; extrapolation to GB assumes vegetative land in excluded squares is similar to sampled squares, a condition that may not hold in regions with substantial sea/urban areas.

- Estimation methods:
  - Estimates are produced using ratio estimation for each land class, weighting by the vegetative land area in each class.
  - Land class estimates are combined using the total vegetative land area as weights.
  - Since 1998, standard errors and confidence intervals have been estimated using bootstrapping due to skewness concerns (Efron & Tibshirani, 1993).

- Implications for analysis:
  - Analyses should incorporate stratification and weighting to produce valid inferences.
  - Bootstrapping is recommended for assessing uncertainty, reflecting the data’s skewed nature.

- References:
  - Barr et al. (1993) Countryside Survey 1990 Main Report
  - Cochran (1963) Sampling Techniques
  - Efron & Tibshirani (1993) An Introduction to the Bootstrap