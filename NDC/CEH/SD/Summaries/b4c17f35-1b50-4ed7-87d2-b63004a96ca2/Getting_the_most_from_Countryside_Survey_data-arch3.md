# Notes on the downloadable data

- Data confidentiality and precision
  - The precise locations of Countryside Survey (CS) field survey squares are kept confidential by CEH to preserve representativeness.
  - External users cannot be provided with location precision finer than 100 square kilometres.
  - This prevents identification of whether specific survey squares fall within defined areas.

- Sampling design and levels
  - CS field survey data come from a sample of 1 km squares across Great Britain (GB).
  - Two levels of sampling: whole squares and within-square measurements.
  - Measurements include a mix of binary and continuous variables (e.g., vegetation, soils) collected via mapped squares and detailed quadrats.

- Stratification and country-specific classifications
  - The sample is not a random subset; it is stratified by the ITE Land Classification.
  - Land classifications have been revised over time and differ by country:
    - England: 21 classes
    - Wales: 8 classes
    - Scotland: 16 classes
  - Original global classification evolved from 32 to 42, then 45 classes due to country reporting requirements.
  - Estimates that do not account for stratification may be unrepresentative.

- Exclusions and representativeness
  - Squares with more than 90% sea area or more than 75% urban area are excluded from field survey.
  - Official GB estimates assume excluded squares have vegetative land composition similar to sampled squares.
  - This assumption is generally unlikely to bias results unless a region has a high proportion of sea/urban squares.

- Estimation method and uncertainty
  - Land class estimates are produced as ratio estimates weighted by the vegetative land area within each class.
  - Standard errors and confidence intervals are calculated using bootstrap methods (since 1998) to address skewness.

- Data sharing, metadata, and governance
  - Challenges include sharing underlying datasets publicly and ensuring adequate metadata.
  - Importance of data quality assurance, cleaning, transformation, analysis, and clear presentation in outputs (reports, charts, dashboards).
  - Emphasis on data governance to ensure datasets meet standards and are stored, shared, and kept up to date.