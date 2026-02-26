# The UK Butterfly Monitoring Scheme

- A national program collating butterfly counts from over 2,000 sites annually across the UK to monitor population abundance and trends.

## Data collection methods and workflow

- All-species transects: fixed-route 2–4 km lines, tallied weekly (April–September) in a 5 m wide band; routes fixed to enable year-to-year comparisons; weather/conducive activity criteria applied.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort survey along two parallel 1-km transects within 1-km squares; 2–4 visits per year (more in July/August), sampling wider habitats.
- Single-species transects: follow all-species method but focused on a few weeks for a focal species.
- Timed counts and egg/larval web counts: species-focused counts within set time/area and habitat.
- Data capture: field records on standard forms; online entry via UKBMS data site or Transect Walker software; regional transect coordinators compile data per region.
- Data storage: online entries and Transect Walker files uploaded to an Oracle database containing all records.
- Roles: recorders upload data; transect coordinators oversee data for their region and perform quality checks.

## Data standards, metadata, and governance

- Standardized methods across sites to ensure comparability; transects sampled to reflect habitat types and management activities.
- Methodology relies on Pollard-style transects and standardized timing and weather conditions to ensure data quality and repeatability.
- Metadata considerations include site, transect, species, year, number of contributing sites, and data provenance (field methods, data entry path).

## Data processing and analytical methods

- Two analytical paths depending on data type:
  - Wider countryside species: uses all survey data in a two-stage model. Stage 1 fits a generalized additive model (GAM) to estimate annual seasonal flight patterns; normalizes values to a common seasonal pattern across years. Stage 2 fits a model to the full annual counts with the seasonal pattern as an offset to derive annual abundance changes.
  - Habitat specialists and regular migrants: employ GAMs to impute missing values and derive a site index; combine site indices to produce a national Collated Index, adjusting for year effects and site effects via a log-linear regression.
- Collated Indexes are updated annually as new monitoring data are incorporated; past years’ indices can shift slightly with new data.
- Distinctions among species groups:
  - Wider countryside species: mobile, broad habitat distribution.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: species overwintering abroad but arriving yearly.
- Indexing outputs are designed to enable temporal trend comparisons across species and groups.

## Data products and structure

- Collated Indices: annual, species-specific indices derived from site data; not all species have long series if data are sparse in early years.
- Site indices: relative abundance measures per site used to compute Collated Indices; reflect a constant proportion of true population size, varying by species detectability.
- Log10 Collated Index (LCI): Collated Indices transformed to log scale for analysis and presentation; indexed so the average across the series equals 2.
- Output data format (CSV): columns include Species (scientific name), Common name, Year, No. Sites (sites contributing to the index that year), Collated Index, Time period (data window used).

## Data quality control and validation

- Automated checks in Transect Walker flag unusual counts and out-of-flight-period records; options to accept or correct flagged data.
- Regional coordinators perform ongoing validation during the season; additional automated/manual checks target distribution range, first-time site records, extreme values, and year-to-year consistency.
- Data quality controls ensure national indices are built from credible, validated observations and highlight potential data gaps or anomalies.

## Practical considerations for data stewards

- Keep clear records of data sources, methods (standard transect types, sampling frequency, weather criteria), and any deviations.
- Track which species have long versus short time series (some species lack long Collated Indices due to data gaps in early years).
- Maintain documentation of modeling approaches (GAMs, two-stage seasonal adjustment, imputation techniques) to support reproducibility and governance.
- Monitor updates to indices as new data arrive, noting that historical indices may shift slightly with ongoing data incorporation.

## Key notes and definitions

- Site indices are relative population measures; Collated Indices are modeled and transformed (log scale) to enable comparisons over time.
- The scheme emphasizes consistent transect placement, standardized data capture, and rigorous quality checks to ensure data utility for trend analysis and conservation decision-making.