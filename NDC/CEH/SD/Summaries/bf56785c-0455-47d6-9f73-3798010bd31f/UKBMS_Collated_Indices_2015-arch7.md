# The UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects data from over 2,000 sites annually across the UK, primarily via fixed-route Pollard walk transects for all-species counts, plus reduced-effort Wider Countryside Butterfly Survey (WCBS) transects and other standardized methods (timed counts, egg/larval web counts) for certain species.
- Data are gathered in the field on standard forms, entered online or via Transect Walker software, and uploaded to an Oracle database. Regional coordinators compile and validate data for their regions.

- All-species transects
  - Fixed-route, typically 2–4 km, walked weekly from April to September (ideally 26 counts/year) in a 5 m wide belt.
  - Transects are fixed to enable year-to-year comparisons and are divided into habitat/management sections.
  - Weather and time requirements: 10:45–15:45, dry conditions, wind < Beaufort 5, temperature thresholds (≥13°C with ~60% sun or ≥17°C if overcast).

- Other data collection methods
  - Single-species transects follow the same methodology but are recorded only on a subset of weeks.
  - Timed counts and egg/larval web counts target specific species or life stages.
  - WCBS (established 2009) uses two parallel 1-km transects in randomly selected 1-km squares, with 2–4 visits (minimum 2 in July/August), sampling wider countryside habitats.

- Data flow and storage
  - Field records are entered via the UKBMS data entry site or Transect Walker, and forwarded to regional coordinators.
  - All records are uploaded into a central Oracle database.

- Analytical methods
  - Wider countryside species: two-stage model using all survey data
    - Stage 1: generalized additive model (GAM) estimates annual seasonal flight pattern.
    - Stage 2: full annual counts model uses seasonal values as an offset to estimate annual abundance changes.
    - Based on Dennis et al. 2013.
  - Habitat specialists and regular migrants: GAM to impute missing values and derive site indices; a log-linear regression aggregates site indices into a national Collated Index.
  - Collated Indices are updated annually; indices for some species may change retrospectively as new data are incorporated. Indices are calculated for species recorded at five or more sites per year.

- Values, interpretation, and scale
  - Site indices are relative measures of population size, proportional to actual abundance.
  - Collated Indices are presented as Log10 Collated Index (LCI) with the series scaled so the average across the series equals 2, enabling relative comparisons over time.

- Species categories
  - Wider countryside species: mobile, spanning wide habitats.
  - Habitat specialists: low mobility, mostly semi-natural habitats.
  - Regular migrants: overwinter outside the UK and migrate to the UK each year (Admiral noted as increasingly resident in parts of the UK).

- Quality control and data validation
  - Automatic checks in Transect Walker flag potential data-entry errors (e.g., unusual counts, out-of-season records).
  - Regional coordinators validate records; online data undergoes ongoing checks.
  - Post-entry validation includes queries for records outside known distribution, unusual abundances, or first-time site records.

- Data structure and metadata
  - Collated Indices are stored as CSV with columns: Species (scientific name per Fauna Europaea v2.2), Common name, Year, No. Sites, Collated Index, Time period.
  - Earlier years may have incomplete indices due to insufficient data; datasets indicate the number of contributing years for each species’ trend.