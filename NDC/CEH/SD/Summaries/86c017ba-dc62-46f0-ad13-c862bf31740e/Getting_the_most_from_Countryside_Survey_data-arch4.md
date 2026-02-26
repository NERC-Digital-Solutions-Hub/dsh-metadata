# Notes on the downloadable data

- Overview of Countryside Survey (CS) field data: information from a sample of 1 km squares in Great Britain, with measurements at two levels (whole square and within-square features) and a variety of variable types (binary to continuous).
- Two levels of sampling are used: characteristics of the entire square and details within each square.

- Confidentiality of locations: precise locations of CS survey squares are kept confidential by CEH. External users cannot identify squares with precision finer than 100 square kilometers to protect representativeness.

- Sampling design and representativeness:
  - Squares are not a random subset of all GB squares; the sample is stratified within designated strata.
  - Stratification is based on the ITE Land Classification; country-specific revisions have altered the classification over time (32 → 42 classes in 1998; 45 classes after 2007).
  - England, Wales, and Scotland have separate classifications (21, 8, and 16 classes respectively).
  - Estimates derived from CS data must account for stratification; failing to do so may yield unrepresentative estimates and inaccurate variation.

- Exclusions and scope:
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys.
  - Official GB estimates assume similarity in vegetative land composition between excluded squares and sampled squares; this assumption is typically reasonable given the small total excluded land, but regions with substantial sea/urban areas may be problematic.

- Estimation and uncertainty:
  - Land class estimates are produced using ratio estimates that incorporate the vegetative land area within each sample square.
  - Estimates for land classes are combined using weights equal to the vegetative land area of each class.
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods to address skewness in some features (Efron and Tibshirani).

- Practical implications for data users (Data Leaders perspective):
  - Important to apply the stratified design and weighting when analyzing CS data to obtain valid inferences.
  - Use bootstrap-based uncertainty measures rather than assuming simple standard errors.
  - Be cautious with GB-wide or region-level estimates where a region contains many excluded or non-representative squares.
  - Maintain awareness of confidentiality constraints that limit precise geolocation, which may affect certain spatial analyses or reproducibility at fine scales.
  - Ensure access to accompanying methodological documentation (sampling design, stratification, weighting, and bootstrap procedures) to support data governance, reproducibility, and effective use within the data function.

- References:
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron and Tibshirani (1993). An Introduction to the Bootstrap.