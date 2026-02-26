# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Aim
- Classify every 1 km square in Great Britain into land classes.
- Use automated, machine-readable data to reproduce the original ISA-based classifications.
- Provide outputs that support long-term environmental health and policy monitoring through standardized formats (maps, reports, tables).

## Data and dataset structure
- Data sources and features used (all at 1 km square level):
  - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
  - ALTITUDE: hill behind, distance to hill, gradient, valley behind, mean altitude, aspect, slope length
  - MAPDATA: roads (A, B), railways, canals, rivers, towns, water bodies, coastlines, etc. (0.1 hectare units)
  - DISTANCE: distance to south coast, distance to west coast
  - ISLAND: island indicators
  - CLIMATE: sunshine hours, snow days, January min temp
  - GEOLOGY: detailed rock classifications
  - DRIFT: drift types and lithology (e.g., glacial, alluvium, drift types)
- Data sources include MOD 100 m DTM (altitude), OS digital map data, and climate/vegetation-related datasets.
- Data preparation emphasized clean, complete, machine-readable inputs suitable for automated classification.

## Classification approaches explored
- Original ISA (Indicator Analysis) approach as baseline.
- Multivariate methods tested:
  - Discriminant Function
  - Logistic Regression (LR)
  - Logistic/Discriminant combinations
  - Various other multivariate techniques (e.g., simulation ordination)
- Key evaluation criteria across methods:
  - Geographical distribution of squares per class
  - Class dispersion (means and standard errors of variables)
  - Concordance with original ISA classifications for 1212 squares
  - Proportional representation of squares by class
  - Relationship to the principal environmental gradient
  - Sampling representation across survey dates
  - Ecological characteristics compared against vegetation data

## Key results and findings
- Repeated testing showed small individual differences between methods, but cumulative effects could be substantial for some classes.
- Discriminant Function alone failed to identify coastal classes in the south, requiring redefinition of coastal classes and misplacing some northern/southern boundaries (notably class 25).
- Logistic Regression and combinations with Discriminant Function provided better alignment with the original classification and coastal class identification.
- Overall, Logistic/Discriminant (LR) offered:
  - Better proportional sampling relative to stratum size
  - Higher retention of squares in the original classification
  - Generally lower standard errors and dispersion than the original classification
  - Improved performance on coastal factors versus the Discriminant Function alone
- Environmental gradient alignment remained very high across methods:
  - Original vs Discriminant: correlation ~0.997
  - Original vs Logistic: correlation ~0.995
- LR-based approaches produced tighter spatial clusters with fewer outliers compared with the original ISA, except for a few coastal adjustments (classes 7 and 8) which would require redefinition if strictly coastal.
- Estimates of land cover for GB using LR/Discriminant showed lower errors and coefficients of variation than the original method, indicating improved precision.

## Outputs and outputs validation
- Distribution maps produced for the LR-based classification (and comparison with original ISA).
- Tables and figures comparing:
  - Altitude means and standard errors across classification methods
  - Environmental gradient scores and their standard errors
  - Cross-tabulations and correspondences between original and LR/DF classifications
  - Proportional representation of squares per land class
- Validation against vegetation data showed strong correlations between classified environmental gradients and vegetation assemblages.
- Environmental means and coastal feature distributions outlined to support coastal/environmental planning and monitoring.

## Recommendation
- Adopt the Logistic Regression with Discriminant Function (Logistic/Discriminant) as the preferred classification approach.
- Rationale:
  - Discriminant Function alone fails to identify southern coastal classes and causes extensive redefinition needs; LR avoids this problem.
  - LR yields the closest balance to proportional sampling and retains the highest correspondence with the original classification.
  - LR and LR/DF show lower standard errors and reduced dispersion compared with the original ISA, enhancing reliability for monitoring.
  - Both LR and LR/DF demonstrate improved alignment with environmental gradients and vegetation relationships across GB.
- Implications for monitoring:
  - Provides a robust, standardized basis for ongoing environmental health assessment and policy evaluation.
  - Supports data integration and sharing across agencies by maintaining consistent, reproducible classifications and accessible outputs.

## Implications for environmental monitoring and policy
- Enables consistent, time-divisible comparisons of environmental health indicators across GB.
- Improves data quality, transparency, and accessibility for monitoring portals and downstream analyses.
- Facilitates integration with vegetation, soil, and climate datasets to track ecological changes and policy impacts.

## Additional outputs and related analyses
- Land cover estimates for GB based on 1978 data with improved methods.
- Ecological characteristics of land classes, including soil pH and vegetation composition, aligned with LR/DF classifications.
- Overlaying of attributes (e.g., coastal features) to capture interactions between land types and coastal environments.
- Distribution of coastal features and means for environmental attributes across classifications.
- Appendix-type references show broad usage of the Merlewood Land Classification in policy, conservation, remote sensing, and land-use planning studies.