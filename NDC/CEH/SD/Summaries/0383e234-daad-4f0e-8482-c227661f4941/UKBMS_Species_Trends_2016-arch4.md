# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
- Most sites use fixed-route transects (Pollard walk) to estimate butterfly counts; includes both standard all-species transects and reduced-effort Wider Countryside Butterfly Survey (WCBS).
- Some species are monitored with alternative methods (timed counts, egg/larval web counts).

- All-species transects:
  - Fixed-route line transect sampling of all butterflies along a 2–4 km route.
  - Weekly counts from early April to end September, weather-permitting.
  - Transects divided into habitat/management sections; counts collected within a fixed 5 m wide band.
  - Typical 26 counts per year; weather windows: 10:45–15:45, dry conditions, wind Beaufort ≤ 5, temperature ≥ 13°C with sun (or ≥ 17°C if overcast).

- Single-species transects:
  - Follow the same methodology as all-species transects but record only for focal species during selected weeks.

- Timed counts and egg/larval web counts:
  - Timed counts record abundance over a fixed period/area under suitable weather.
  - Egg/larval web counts record eggs or larval webs in habitats used by specific species (e.g., Marsh Fritillary).

- Wider Countryside Butterfly Survey (WCBS):
  - Reduced-effort sampling to cover wider countryside habitats (farmland, etc.).
  - Based on two parallel 1-km transects within randomly selected 1-km squares; fixed-route transect approach.
  - 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).

- Data recording and entry:
  - In-field data on standard forms; online entry via UKBMS data site or Transect Walker software.
  - Regional transect coordinators compile data for all sites in their region.
  - Data uploaded to an Oracle database; online data and Transect Walker files are the primary inputs.

- Data governance and access points:
  - Data flow involves field recorders, regional coordinators, and centralized storage to enable ongoing analysis and trend estimation.

## Data collection methods

- Field recording uses standard forms; post-field entry through UKBMS site or Transect Walker.
- Transect coordinators are responsible for data completeness and quality within their region.
- Data management includes direct entry by recorders or coordinators and subsequent uploads to the central database.

## Analytical methods

- Two national index approaches, depending on data type:

- For Wider Countryside (WCBS) and similar data:
  - Two-stage model using all survey data types to estimate seasonal patterns and annual abundance changes.
  - Stage 1: Generalised additive model (GAM) estimates annual seasonal flight pattern for each species; daily values are normalised to a common seasonal pattern per year.
  - Stage 2: Full annual counts modeled with seasonal values as an offset to estimate year-to-year abundance changes.
  - Referenced methods: Dennis et al. 2013.

- For habitat specialists and regular migrants:
  - GAM used to impute missing values due to uneven data collection and to derive site indices.
  - Collated Index created by combining site indices; years with insufficient monitoring lead to adjusted indices.
  - A log-linear regression on collated indices yields national trends for each species.
  - Trends calculated for:
    - Entire series (1976–2016)
    - Last 20 years (1997–2016)
    - Last 10 years (2007–2016)
  - Species groups defined by mobility and habitat: wide-range (WCBS), habitat specialists, regular migrants.
  - Not all species have full data across all years; prior years may have fewer contributing sites, affecting trend length.

- Data handling notes:
  - Collated Indices are relative measures (log10 scale) rather than absolute population sizes; indices are scaled so the average over the series is 2.
  - Trends are reported as slopes (change per year) with associated p-values and descriptive trend labels (Rapid decline, Rapid increase, Stable).

## Nature and units of recorded values

- Site indices: relative measures of local population size; reflect detectability variance between species.
- Collated Indices: log10-transformed, scaled so long-term average equals 2.
- Trends: slope of Collated Index over specified time windows (per year change).
- Data quality indicators include standard errors and p-values for both overall series trends and 10/20-year trends.

## Quality control

- In-field automatic checks (Transect Walker) flag unusual records (e.g., out-of-season sightings, abnormally high counts).
- Regional coordinators review and validate data continuously during the season.
- Post-entry validation includes automated and manual checks for:
  - Records outside known distribution ranges
  - Out-of-season records
  - First-time site records
  - Extreme or anomalous counts

## Format of stored data

- Data stored as CSV with the following columns:
  - Sci_Name, Common_name
  - No_years
  - Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
  - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
  - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change

- Column descriptions:
  - Sci_Name: scientific name per Fauna Europaea (version 2.2)
  - Common_name: vernacular name per Emmet & Heath
  - No_years: number of years used in the series trend
  - Series_slope/Std_Err/P_value/Trend/%_change: overall (all-time) trend metrics
  - 20_yr_Slope/Std_Err/P_value/Trend/%_change: 20-year trend metrics
  - 10_yr_Slope/Std_Err/P_value/Trend/%_change: 10-year trend metrics

- Additional context notes:
  - Collated Indices are on a log10 scale; trends describe directional changes and statistical significance.
  - Data sources include references to methodological papers (e.g., Pollard & Yates; Rothery & Roy) and species-specific documentation.

- Data provenance and standards:
  - Scientific naming follows Fauna Europaea; common names follow established butterfly references.
  - The dataset is continually updated as new monitoring data are received and incorporated.