# Experimental design/sampling regime

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
  - Data support multiple monitoring outputs including population indices and trends to inform conservation decisions and policy evaluation.
  - Uses standardized, fixed protocols to enable year-to-year comparability and long-term trend analysis.

- Sampling design
  - All-species transects: fixed-route line transects (2–4 km) recorded weekly from early April to late September; weather-appropriate conditions required; transects fixed to ensure comparability across years; data collected in a 5 m width along the route.
  - Single-species transects: follow the all-species methodology but recorded only during focal species flight periods.
  - Timed counts and egg/larval web counts: species-specific efforts during defined time windows and suitable weather.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling since 2009, using two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year, with at least two visits in July/August.

- Data collection methods
  - Field recording on standard forms; online data entry via UKBMS MyData or Transect Walker software.
  - Regional transect coordinators compile site data and ensure timely data handling.
  - Data uploaded to an Oracle database for central storage and management.

- Data handling and storage
  - Centralized storage in an Oracle database; data entry and uploads coordinated regionally.
  - Regional coordinators perform ongoing checks during the season; data management entrusted to ensure data integrity and accessibility.

- Analytical methods
  - For wider countryside species: two-stage modeling using all survey data.
    - Stage 1: Generalized additive model (GAM) estimates annual seasonal flight patterns.
    - Stage 2: Seasonal values are used as an offset in a larger model to estimate annual abundance changes and trends.
  - For habitat specialists and regular migrants: GAM imputes missing values to create site indices; indices aggregated to produce a national Collated Index.
  - Trend estimation: Linear regression on collated indices to yield overall trends since 1976, and across last 20 years (1997–2016) and last 10 years (2007–2016).
  - Data updates: Collated Indices updated annually as new data are incorporated, which can slightly adjust past years’ indices.

- Data quality control
  - Automated checks within Transect Walker flag anomalous counts or records outside known flight periods.
  - Regional coordinators validate questionable records; continuous validation throughout the season.
  - Additional automated/manual validation checks for records outside known distributions, first-time site records, extreme values, and year-to-year variability.

- Data formats and units
  - Site indices are relative measures correlated with absolute population sizes; Collated Indices are presented as Log10 indices, scaled so the mean across the series equals 2.
  - Trends are reported as slopes with associated standard errors and p-values, plus descriptive trend labels (e.g., Rapid decline, Rapid increase, Stable) for different time frames (entire series, last 20 years, last 10 years).
  - Data stored in CSV format with columns including scientific name, common name, number of years, series slope, standard error, p-values, trend descriptors, and percent changes for 10- and 20-year periods.

- Relevance to monitoring framework aims
  - Demonstrates integration of standardized field protocols, robust statistical modeling to handle seasonality and missing data, and transparent reporting of trends with uncertainty.
  - Highlights data governance practices (regional data handling, central storage, validation) and the importance of metadata, data quality, and data sharing through accessible data products (e.g., CSV trend files) and updated indices.