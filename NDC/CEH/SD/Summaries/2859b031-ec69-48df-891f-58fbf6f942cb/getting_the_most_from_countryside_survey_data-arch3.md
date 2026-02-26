# Notes on the downloadable data

- Confidentiality and geographic precision
  - The precise locations of Countryside Survey (CS) square survey sites are kept confidential by UKCEH.
  - External users cannot identify exact locations to better than 100 square kilometres.
  - This limits ability to determine whether squares fall within defined areas.

- Sampling design and data structure
  - CS field survey data come from a sample of 1 km squares across Great Britain.
  - There are two sampling levels: whole squares and within-square features.
  - Measurements include a range from binary (yes/no) to continuous (areas, lengths).

- Representativeness and stratification
  - The CS sample is not a simple random subset; it is stratified within designated strata.
  - Strata are defined by the ITE Land Classification, which varies by country and over time (England: 21 classes, Wales: 8, Scotland: 16; overall classifications evolved from 32 to 45 classes).
  - Estimates must account for stratification; ignoring it can lead to non-representative results and incorrect variation estimates.

- Exclusions and regional implications
  - Squares with more than 90% sea or more than 75% urban coverage were excluded from field surveying.
  - Official GB estimates are effectively representative of the remaining squares; extrapolations to the whole GB assume similar vegetative land composition in excluded areas.
  - This assumption may be problematic for regions with high sea/urban square proportions, though bias is considered negligible in general.

- Estimation methods and uncertainty
  - GB land-class estimates are produced using ratio estimates that incorporate the area of vegetative land within each sample square.
  - Land-class estimates are combined using weights equal to the vegetative land area of each class.
  - Since features can be skewed, standard errors and confidence intervals are estimated using bootstrap methods (since 1998).

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.