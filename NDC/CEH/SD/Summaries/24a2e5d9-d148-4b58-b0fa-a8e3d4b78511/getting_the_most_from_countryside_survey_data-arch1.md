# Notes on the downloadable data

- Confidentiality and geographic precision
  - Exact locations of Countryside Survey (CS) squares are held confidential by UKCEH.
  - External users cannot identify whether squares fall within defined areas with precision finer than 100 square km.

- Sampling design and data structure
  - CS Field Survey data come from a sample of 1 km squares in GB.
  - Each selected square is mapped and measured at two levels: the square level and within-square features.
  - Measurements include binary variables and continuous metrics (areas, lengths).
  - The sampling is not a random subset; it is stratified by land classification (ITE Land Classification).
  - Land classifications have evolved: originally 32 classes, expanded to 42 in 1998 (SCotland reporting), and 45 classes after Wales reporting changes.
  - Each country (England, Wales, Scotland) effectively has its own classification (England ~21 classes, Wales ~8, Scotland ~16).

- Representativeness and exclusions
  - Official estimates are produced by ratio estimates per land class, weighted by the vegetative land area of each class.
  - Not all GB squares were surveyed; squares >90% sea or >75% urban were excluded.
  - Estimates for GB or regions assume excluded squares have similar vegetative land composition to sampled squares; bias is generally negligible unless a region has a high share of sea/urban squares.

- Estimation, inference, and uncertainty
  - Since 1998, standard errors and confidence intervals are estimated using bootstrap methods due to concerns about skewness in features being estimated.

- Practical implications for analysts
  - When analyzing CS data, account for the stratified sampling design and use appropriate weights.
  - Use ratio-estimation procedures at the land-class level and aggregate via vegetative land area weights.
  - Apply bootstrap-based SEs and CIs for more accurate uncertainty assessment.
  - Be mindful of the confidentiality constraint that limits precise geographic localization below 100 square km.
  - Acknowledge potential representativeness limitations due to exclusions (sea/urban squares) and country-specific land classifications.

- References
  - Barr et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran (1963). Sampling Techniques.
  - Efron & Tibshirani (1993). An Introduction to the Bootstrap.