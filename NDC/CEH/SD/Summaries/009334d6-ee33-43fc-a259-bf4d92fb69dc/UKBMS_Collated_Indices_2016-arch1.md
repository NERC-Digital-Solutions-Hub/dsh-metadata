# The UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects data from over 2,000 sites annually across the UK, using standardized methods to count butterflies.
- Data types include all-species transects, reduced-effort Wider Countryside Butterfly Survey (WCBS) transects, and other standardized methods (timed counts, egg/larval web counts) for certain species.

## Data collection methods

- All-species transects (Pollard walk):
  - Fixed-route line transects 2–4 km long, sampled weekly from April to September.
  - Record all butterfly species within a fixed 5 m wide belt along the transect.
  - Transects are fixed to allow year-to-year comparisons and are chosen to reflect habitat types and management.
  - Weather constraints: suitable butterfly activity (dry, wind < Beaufort 5, temperature thresholds with sunshine or overcast as specified).
- WCBS (Wider Countryside Butterfly Survey):
  - Reduced-effort sampling to cover wider countryside habitats (farmland, etc.).
  - Based on 1-km squares with two parallel 1-km transects, subdivided into 10 sections.
  - Typically 2–4 visits per year, with a minimum of 2 visits in July/August; spring visits encouraged.
- Single-species transects, timed counts, and egg/larval web counts are used for certain species during portions of the flight period.

## Data capture and management

- Field recording on standard forms; subsequent online entry via the UKBMS data portal or Transect Walker software.
- Data entry can be done by recorders or regional transect coordinators.
- Transect coordinators compile data for their region; online data and Transect Walker files are uploaded to an Oracle database holding all records.

## Analytical methods

- Two main approaches, depending on data richness:
  - Wider countryside (WCBS and similar):
    - Uses all counts in a season to estimate the annual seasonal flight pattern (two-stage model).
    - Stage 1: Generalized Additive Model (GAM) to estimate annual seasonal pattern per species.
    - Stage 2: Use seasonal pattern as an offset in a model fitted to all annual counts to estimate annual abundance changes and trends.
    - Described in Dennis et al. 2013.
  - Habitat specialists and regular migrants (with less WCBS data and more limited sampling):
    - GAM to impute missing values and to compute a site index.
    - Site indices are combined to derive a national annual Collated Index (CI) for each species.
    - A log-linear regression is used to estimate missing values due to varying year and site effects.
    - Collated Indices are updated annually as more data are incorporated; some years may have shorter trend series if data are sparse.
    - CI calculation requires a species to be recorded at five or more sites per year.

## Outputs and interpretation

- Site indices: relative measures of population size, proportional to the true population; not absolute counts.
- Collated Indices (CI): presented as the logarithm (Log10) of the Collated Index; scaled so that the average index over the full series equals 2, providing a relative time series of population size.
- The CI reflects overall national trends, with potential adjustments as more data are added over time.

## Quality control

- Automatic checks in Transect Walker flag anomalous records (e.g., unusually high counts, records outside flight periods).
- Regional transect coordinators review and validate records; validation continues throughout the season.
- Additional automated and manual validation procedures check for out-of-range records, records outside known distribution, first-time site records, and unusual abundances.

## Data availability and dataset structure

- Collated Indices are stored as CSV files.
- Each record includes:
  - Species (scientific name per Fauna Europaea)
  - Common name (per Emmet & Heath)
  - Year
  - No. Sites contributing to the CI for that year
  - Collated Index value
  - Time period used to produce the CI
- Some species have shorter trend series due to insufficient data in early years; this is documented as the number of contributing years.

## Definitions and taxonomy

- Wider countryside species: mobile species occurring across a broad range of habitats.
- Habitat specialists: low mobility species largely restricted to semi-natural habitats.
- Regular migrants: species that do not overwinter in the UK and migrate from continental Europe each year.
- Red Admiral may be resident in parts of southern England and Wales, but is generally treated as a migrant overall.

## Notes on data lineage

- The Collated Indices are updated as additional monitoring data become available, which can slightly alter previous years’ indices.
- The methodologies reference established statistical approaches (GAMs, two-stage models, and log-linear imputation) and are documented in methodological literature (e.g., Dennis et al. 2013; Rothery & Roy 2001; Moss & Pollard 1993; Pollard & Yates 1993).