# UK Butterfly Monitoring Scheme (UKBMS) Methodology and Data Analysis

- The UKBMS collects data from over 1,000 sites annually across the UK using standardized butterfly monitoring methods.
- All-species transects (Pollard walks) are the core method, with fixed routes (2–4 km) sampled weekly under suitable weather, plus alternative methods for certain data (single-species transects, timed counts, and egg/larval web counts).
- Transects are designed to sample habitat types and management activities, and must remain fixed to enable year-to-year comparisons.
- Sampling typically yields about 26 counts per year per site, conducted between 10:45 am and 3:45 pm under specified weather conditions (e.g., dry; wind < Beaufort 5; temperature thresholds depending on sunshine).

- Data collection is performed in the field on standard recording forms and entered into the Transect Walker software, with data either entered by the recorder or a regional transect coordinator. Transect Walker files are uploaded to an Oracle database.

- The analytical approach uses a General Additive Model (GAM) to impute missing values and calculate site indices. These site indices are combined across monitored sites to produce a national Collated Index for each species.
- Because not all sites are monitored every year, a log-linear regression is used to estimate missing values and produce indices and trends, accounting for year and site effects.
- Collated Indices are updated annually as new data are incorporated; past years may be revised as data are added.
- Species trends are derived from linear regression on the collated indices:
  - Across the full time series (from 1976 to 2011 in the provided data)
  - Over the last 20 years (1992–2011)
  - Over the last 10 years (2002–2011)
- The database contains detailed trend outputs, including the number of contributing years, slope, standard error, p-value, trend description (e.g., rapid decline, rapid increase, stable), and percent change over each period. Some species have shorter trend series due to limited data in earlier years.

- Recorded values are presented as relative measures rather than absolute population counts. Site indices relate to actual population size through a proportional detectability relationship and are transformed to a log scale (Log10 Collated Index, LCI) for analysis and interpretation.
- Trends are reported as the rate of change in the Collated Index per year (slope).

- Quality control is embedded at multiple stages:
  - Automatic checks within Transect Walker flag potential data-entry errors (e.g., anomalously high counts, records outside flight periods).
  - Regional coordinators validate data using local knowledge.
  - Additional automated and manual validation steps screen for species outside known distribution, flights outside typical periods, first-time site records, and unusually extreme values.

- Data storage and format:
  - Species trends are stored as CSV files with fields including Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change, 10-yr slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, and 10-yr % change.
  - The dataset uses standard taxonomy references (scientific and common names) and records per-species time-series statistics.
  - The Transect Walker software used for data entry is freely downloadable from the UKBMS website (www.ukbms.org).
  - The underlying data are stored in an Oracle database, with site-level data managed by regional coordinators and consolidated into national indices.

- Outputs and accessibility:
  - National annual indices and species-specific trends are produced from the collated data and updated as new data are incorporated.
  - Results are typically disseminated as reports, charts, or dashboards to inform monitoring and decision-making.