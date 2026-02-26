# Notes on the downloadable data

- Confidentiality and location privacy
  - Precise locations of Countryside Survey (CS) field squares are kept confidential by UKCEH.
  - External users cannot identify exact squares beyond 100 square km precision.
  - This preserves representativeness but limits spatial identification of survey areas.

- Data structure and sampling design
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Two levels of sampling:
    - Whole-square level: maps and characterises the square.
    - Within-square level: measurements within squares (e.g., quadrats) for vegetation, soils, etc.
  - Measurements include a mix of binary and continuous variables.

- Representativeness and sampling frame
  - The sample is stratified, not purely random, using Land Classification strata.
  - Land Classification changes over time and differs by country:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Since 1998, estimates have relied on stratification to improve accuracy; country-specific classifications reflect reporting needs.

- Exclusion and scope
  - Squares with more than 90% sea area or more than 75% urban area (based on 1:250,000 OS maps) were excluded from field surveys.
  - Official estimates for GB or regions assume excluded squares have vegetative land composition similar to sampled squares.
  - Bias from exclusion is expected to be small overall, but can be problematic in regions with high sea or urban coverage.

- Estimation and uncertainty
  - Estimates are produced as ratio estimates within each land class, weighted by the vegetative land area of each class.
  - Land-class estimates are then combined using the total vegetative land area as weights.
  - Standard errors and confidence intervals are estimated via bootstrap methods since 1998 (to address skewness in features).
  - Analyses that ignore stratification may misrepresent variation and uncertainty.

- Practical implications for data use
  - When analyzing CS data, account for stratification, class weights, and area-based weighting.
  - Use bootstrap-derived standard errors for uncertainty assessments.
  - Be mindful of the privacy constraint on precise locations, which limits fine-grained spatial mapping to 100 sq km precision.
  - Consider the potential bias from excluded squares, particularly for regional analyses with substantial sea/urban coverage.

- References
  - Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
  - Cochran, W.G. (1963). Sampling Techniques (2nd ed.).
  - Efron, B. & Tibshirani, R.J. (1993). An Introduction to the Bootstrap.