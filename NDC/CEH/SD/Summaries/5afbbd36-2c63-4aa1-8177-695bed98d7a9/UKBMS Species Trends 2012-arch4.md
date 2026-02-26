# Experimental design/sampling regime

- Purpose and scope
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites per year in the UK to monitor butterfly abundance and trends.
  - Data support population estimates and trend analyses for multiple species across sites and years.

- Data collection methods
  - All-species transects
    - Fixed-route line transects (2–4 km) sampled weekly from April to September under suitable weather.
    - Counts recorded within a fixed 5 m wide band to enable year-to-year comparisons.
    - Transects are designed to sample habitat types and management activities; routes are kept fixed.
    - Typical session lasts 45 minutes to 2 hours; observations between 10:45 and 15:45.
  - Single-species transects
    - Follow the all-species protocol but record only for one focal species during a few weeks.
  - Timed counts and egg/larval web counts
    - Timed counts record a species’ abundance over a set period and area under suitable weather.
    - Egg/larval web counts capture eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).
  - Data capture
    - Field data recorded on standard forms and entered into Transect Walker software.
    - Data entry performed by recorders or regional transect coordinators.
    - Transect Walker outputs uploaded to an Oracle database.

- Data processing and analytics
  - Validation and quality checks
    - Automatic checks in Transect Walker flag anomalous records; regional coordinators verify data.
    - Additional automated/manual validation screens for out-of-range distributions, unusual flight periods, first sightings, extreme counts, or atypical site-year patterns.
  - Modelling and indices
    - After validation, General Additive Models (GAM) impute missing values and produce a site index.
    - Site indices are combined into species-level Collated Indices (log10 transformed; scaled so the average equals 2).
    - A log-linear regression model estimates missing values and derives trends for the Collated Indices.
    - Trends computed for the entire series (1976–2012), last 20 years (1993–2012), and last 10 years (2003–2012).
    - Some species have shorter trend series due to insufficient data in earlier years.
  - Data outputs and storage
    - Collated Indices and species trends inform annual reports and analyses.
    - Data formats include CSV storage for species trends with fields such as species, years, slopes, p-values, and trend descriptors.

- Nature and units of recorded values
  - Site index: relative population size, not absolute; relates to other abundance measures.
  - Collated Indices: log10-transformed values; scaled so the average index equals 2.
  - Trends: expressed as slopes (change in Collated Index per year); provide per-species directional trends over specified periods.
  - Outputs also include percentage changes over whole series, 20-year, and 10-year windows.

- Data quality and governance
  - Multi-layer validation (in-field automatic checks, regional coordinator reviews, and post-entry data quality checks).
  - Consistent data handling practices across sites and years to maintain comparability.
  - Documentation of data formats and transformation (CSV structure, column definitions) to support reproducibility.

- Data format and metadata
  - Stored as CSV with columns including: Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr slope/std.err/p-value/trend/% change, 10-yr slope/std.err/p-value/trend/% change.
  -Taxonomic naming follows Fauna Europaea; common names follow Emmet and Heath references.
  - Series are flagged with the number of contributing years to indicate reliability.

- Implications for Data Leaders
  - End-to-end data pipeline: standardized field collection, controlled data entry, rigorous validation, and transparent modeling to produce interpretable indices and trends.
  - Emphasis on data quality, reproducibility, and governance to ensure trusted, longitudinal insights across years and species.
  - Clear data products (site indices, Collated Indices, and trend metrics) support decision-making and monitoring at scale.
  - Well-documented data formats and metadata facilitate reuse, integration with external datasets, and cross-site collaboration.