# The UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects butterfly data from over 2,000 sites annually across the UK, primarily via fixed linear transects called Pollard walks.
- Data collection methods include all-species transects, single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).

## Data collection methods

- All-species transects
  - Fixed-route transects 2–4 km long; recordings cover all butterfly species along a 5 m wide band.
  - Typically 26 counts per year from April to September; routes are fixed to enable year-to-year comparisons.
  - Observations conducted in suitable butterfly activity windows (specific weather conditions and times).

- Single-species transects
  - Follows the all-species methodology but focuses on specific species for only certain weeks.

- Timed counts and egg/larval web counts
  - Timed counts record abundance of a focal species over a set period and area.
  - Egg/larval web counts document eggs or larval webs in suitable habitat.

- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey in wider countryside habitats (farmland, etc.), based on a subset of the all-species methodology.
  - Uses two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per season, with at least 2 visits in July/August.

## Data recording and storage

- Field recording on standard forms; data entered online via the UKBMS data entry site or into Transect Walker software.
- Data entry is done by recorders or regional transect coordinators; coordinators compile data for their region each monitoring season.
- Online data and Transect Walker files are uploaded into an Oracle database containing all records.

## Analytical methods

- Wider countryside species
  - Use a two-stage model leveraging all counts from all survey types.
  - Stage 1: generalized additive model (GAM) estimates annual seasonal flight patterns per species.
  - Stage 2: full annual counts are modeled with seasonal values as an offset to estimate annual abundance changes and trends.
  - Method described in Dennis et al. (2013).

- Habitat specialists and regular migrants
  - With gaps in WCBS data and reliance on timed counts/larval counts, a GAM imputes missing values and computes a site index.
  - Collated Index (national annual index) is derived from all site indices; a log-linear regression accounts for year and site effects to estimate missing values and trends.
  - Collated Indices are updated annually as new monitoring data are incorporated; earlier years may be revised.

- Outputs and scale
  - Site indices are relative measures of population size, proportional to the number of butterflies present (not absolute counts).
  - Collated Indices are presented as the log10 of the Collated Index (LCI); indices are scaled so that the long-term average equals 2.

## Data quality and validation

- Automatic checks in Transect Walker flag potential data entry errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review data for questionable records and perform ongoing validation during the season.
- Further automated and manual validation procedures include cross-checks against known distributions, flight periods, first-time site records, and anomalous counts.

## Outputs and data structure

- Collated Indices: taxonomy includes species, year, number of contributing sites, Collated Index value, and the time period used for the data.
- Output format: Collated Indices are stored as CSV files.
- Data provenance and updates: Collated Indices may be revised as additional monitoring data are received and incorporated.

## Definitions and terminology

- Wider countryside species: mobile species occurring across a wide range of habitats.
- Habitat specialists: low-mobility species primarily in semi-natural habitats.
- Regular migrants: species that overwinter outside the UK but arrive annually.
- Red Admiral: example of a species with changing residency patterns in parts of the UK.

## Data governance and usage implications for Data Leaders

- Clear data flows from field collection to online entry, regional coordination, and central storage (Oracle database).
- Explicit data quality controls and continuous validation support trust in indices and trend analyses.
- Distinct analytical pipelines for different species groups ensure appropriate handling of data gaps and seasonal variability.
- Outputs (site indices and Collated Indices) provide relative measures suitable for temporal trend analysis and cross-site comparisons.
- Data are updated annually with potential revisions to past years as new data are integrated, highlighting the importance of versioning and metadata for governance.