# WildCrickets06F_EarlyCallingVsSurvival

- Overview
  - Dataset describes individual male lifespan classified by early calling effort.
  - EarlyCalling classification is High (H) or Low (L) relative to the population median of early calling activity.

- Data fields and definitions
  - Year: Year when the cricket was alive.
  - Lifespan: Lifespan in days.
  - EarlyCalling: Categorical field with values H (High) or L (Low) representing early calling effort.

- Classification method
  - EarlyCalling is determined by whether early calling activity exceeds (H) or falls below (L) the population median.

- Data quality and metadata needs
  - Ensure Lifespan is consistently measured in days.
  - Validate the H/L coding against the underlying early calling measurements.
  - Document the population median threshold used for the H/L classification to enable reproducibility.
  - Identify and handle any missing values in Year, Lifespan, or EarlyCalling.
  - Provide metadata including variable definitions, units, data collection context, and provenance.

- Data governance and usage considerations
  - Suitable for analyses linking lifespan with early calling category across individuals.
  - Maintain clear provenance and versioning to track how the median-based classification may change with updated data.