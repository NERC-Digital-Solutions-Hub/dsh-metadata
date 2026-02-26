# Experimental design/sampling regime

- Scope and purpose
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
  - Data underpin population indices and trends for multiple butterfly species, used to understand spatial patterns and temporal changes.

- Data collection methods
  - Field data recorded on standard forms and entered online via UKBMS data entry site or Transect Walker software.
  - Data submission is managed by transect coordinators who compile regional data; online data and Transect Walker files feed into an Oracle database.

- Transect types and protocols
  - All-species transects: fixed-route line transects (2–4 km) walked weekly Apr–Sep under suitable weather; 5 m wide counts; routes fixed to enable year-to-year comparisons; time window roughly 10:45–15:45.
  - Single-species transects: same methodology as all-species but limited to periods of focal species’ flight.
  - Timed counts and egg/larval web counts: species-specific counts within set areas and times, following weather criteria.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in wider countryside habitats (farmland, etc.); two parallel 1-km transects within randomly chosen 1-km squares; 2–4 visits per year, with minimum two visits in July/August.

- Data processing and storage
  - Data are entered by recorders or regional coordinators and uploaded to an Oracle database.
  - Rigorous quality checks occur at multiple levels: automatic checks in Transect Walker, regional coordinator validation, and ongoing automated/manual validation for out-of-range records, unusual flight periods, first-time site records, and anomalous counts.

- Analytical approaches (two main pathways)
  - Wider countryside species: two-stage model using all survey data
    - Stage 1: generalized additive model estimates annual seasonal flight pattern.
    - Stage 2: full annual counts modeled with seasonal values as an offset to derive annual abundance changes.
    - References: Dennis et al. 2013.
  - Habitat specialists and regular migrants: GAM-based imputation and site indexing
    - Impute missing values to compute site index; combine into a national Collated Index.
    - Use log-linear regression to estimate missing values and derive indices/trends, accounting for year and site effects.
  - Trend calculation
    - Linear regression on Collated Indices to produce a single trend for each species across:
      - All years (1976–2016)
      - Last 20 years (1997–2016)
      - Last 10 years (2007–2016)
    - Collated Indices are log10-transformed; trends reported as slope values with associated statistics.

- Data products and formats
  - Site indices: relative measures of population size, linked to broader population estimates (e.g., MRR methods) and dependent on detectability differences by species.
  - Collated Indices: log10-transformed values with mean normalization (average index set to 2 for comparability).
  - Outputs include: series slope, standard errors, p-values, trend descriptions, and percent changes over specified periods.
  - Storage format for results: CSV file with columns including scientific name, common name, number of years, slopes, errors, p-values, trend descriptors, and percentage changes for current and recent periods (10/20 years).

- Data quality and standards
  - Automatic and manual data validation to ensure records align with known distributions and flight periods; checks for out-of-range or unusual observations.
  - Regional coordinators possess domain knowledge to verify site-level data before inclusion in national analyses.

- Relevance for GIS applications
  - Spatially explicit transect routes and site locations enable mapping of sampling effort and geographic coverage.
  - Time-series indices and trends support choropleth mapping of species abundance changes over decades and recent periods.
  - Data standardization (CSV formats, fixed fields, consistent species naming) facilitates integration with other biodiversity or environmental datasets.
  - Quality control lineage (field forms -> Transect Walker -> online input -> Oracle database -> national indices) provides traceable data provenance for GIS and analytical work.