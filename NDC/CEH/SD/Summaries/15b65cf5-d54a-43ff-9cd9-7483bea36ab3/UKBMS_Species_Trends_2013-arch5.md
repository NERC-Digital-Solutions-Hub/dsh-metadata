# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) aggregates data from over 1,000 sites annually across the UK to monitor butterfly populations.
- Data collection methods include all-species transects (Pollard walks and fixed-route line transects), single-species transects, timed counts, and egg/larval web counts.
- Transects are fixed in route and habitat type to enable year-to-year comparisons; typically 2–4 km long with counts along a 5 m wide band, aiming for 26 counts per year from April to September.
- Measurements are taken under strict weather conditions and time windows to ensure comparable observations ( transects run 10:45–15:45; weather criteria include dry conditions, wind < Beaufort 5, and temperature thresholds).

- Data collection is performed on standard forms in the field, entered into the Transect Walker software, and uploaded to an Oracle database by regional transect coordinators.

- Transect routes, data handling, and analysis are designed to support robust temporal comparisons and long-term trend detection.

- Data governance considerations:
  - The dataset is dynamic; Collated Indices are updated annually as new monitoring data are incorporated, and past estimates may be revised.
  - Documentation includes the number of years contributing to each trend, enabling assessment of reliability.

- For data stewards, key workflow points include standardized data capture, centralized storage, controlled access, and clear provenance for updates and revisions.

## Data collection methods

- All-species transects: fixed-route lines with weekly recording of all butterfly species under specified conditions; transects sampled for habitat/management units; 26 counts per year.
- Single-species transects: similar methodology, focused on a particular species for a subset of weeks.
- Timed counts and egg/larval web counts: counts over fixed periods/areas and recording eggs or larval webs in suitable habitat.

## Data capture and storage workflow

- Field data recorded on standard forms and entered into Transect Walker (free software).
- Data submitted by recorders or regional coordinators and uploaded to an Oracle database.
- Regional coordinators validate data before broader quality checks.

## Analytical methods

- After validation, generalized additive models (GAM) impute missing values and derive site indices.
- Site indices are aggregated to a national level as Collated Indices for each species; indices are log10-transformed for analysis.
- Missing values and trends are estimated with a log-linear regression, accounting for year effects and site effects.
- Trends are reported for:
  - Whole time series (since 1976)
  - Last 20 years (1993–2013)
  - Last 10 years (2003–2013)
- Not all years have Collated Indices for all species (early years may be incomplete), and some species have shorter trends accordingly.
- The dataset notes how many years contribute to each trend.

## Nature and units of recorded values

- Site indices: relative measures of population size (not absolute counts), reflecting a constant proportion of the actual population.
- Collated Indices: expressed as the log10 of the index (LCI) to enable relative comparisons over time.
- Trends: reported as the slope (change per year) with accompanying standard errors and P-values.
- Trend descriptions (Series and 20/10-year) use qualitative descriptors (rapid decline, rapid increase, stable) based on slope direction and statistical significance.
- Supplementary metrics include percentage changes over the full series, 20-year, and 10-year windows.

## Quality control

- In-field automatic checks via Transect Walker flag improbable entries (e.g., abnormally high counts, records outside known flight periods).
- Regional coordinators review data for consistency and plausibility.
- Additional automated and manual validation steps check:
  - Records outside known geographic distribution
  - Records outside known flight periods
  - First-time records at a site
  - Extreme or atypical abundances

## Format of stored data

- Species Trends are stored as CSV files with columns including:
  - Species (scientific name per Fauna Europaea v2.2)
  - Common name
  - No.years (number of years in the trend)
  - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
  - 20-yr Slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
  - 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change
- References for methods and indices are provided (e.g., Rothery & Roy, Moss & Pollard) to support reproducibility.
- Columns rely on standardized taxonomy and naming conventions (Fauna Europaea, Emmet & Heath).

## Data governance and stewardship considerations

- Indices are updated annually as new data are incorporated; historical values may change, impacting reproducibility and analyses that rely on fixed historical figures.
- Metadata should capture:
  - Data collection methods (transect type, timing, weather criteria)
  - Data processing steps (GAM imputation, index construction)
  - Versioning history and dates of index updates
  - The number of contributing years per species for each trend
- Accessibility and provenance: ensure linkage between raw field data, processed indices, and published trend results to support traceability and auditability.
- Data quality monitoring: maintain and document validation procedures, thresholds for flagging anomalies, and any data corrections or exclusions.