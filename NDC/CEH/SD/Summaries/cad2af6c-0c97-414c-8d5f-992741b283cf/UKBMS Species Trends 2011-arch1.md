# Experimental design/sampling regime

- Scope and data collection
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Primary method: all-species transects (Pollard walk) with fixed routes to enable year-to-year comparisons.
  - Supplementary methods: single-species transects, timed counts, and egg/larval web counts for focal species.
  - Transects: 2–4 km long, divided into habitat/management units, typically 26 counts per year (weeklies from early April to late September).
  - Observation windows and conditions: counts conducted 10:45–15:45 under suitable butterfly activity; weather criteria include dry conditions, wind < Beaufort 5, and temperature thresholds (≥13°C with ≥60% sunshine or >17°C if overcast).

- Data collection process
  - Field data recorded on standard forms and entered into Transect Walker software (freely available).
  - Data entry by recorders or regional transect coordinators; regional coordinators compile data for all sites in their region.
  - Transect Walker files uploaded to an Oracle database.

- Analytical framework
  - Data validation follows a multi-step approach with automated checks (e.g., out-of-range counts, records outside flight periods) and regional manual reviews.
  - Site indices: computed using General Additive Models (GAM) to impute missing values and derive site indices.
  - Collated Index: national annual index for each species derived by combining site indices; uses log-linear regression to handle missing values and differential year/site effects.
  - Trends: derived from linear regression on collated indices over different periods—whole series (since 1976), last 20 years (1992–2011), and last 10 years (2002–2011).
  - Data updates: Collated Indices are updated annually as new monitoring data are received; early years may lack some species due to insufficient data.

- Data characteristics and units
  - Site indices are relative measures of population size (not absolute counts) and reflect detectability differences among species.
  - Collated Indices are presented as the log10 of the Collated Index (LCI); series trends are expressed as slopes (change per year).
  - Acknowledges that detection probability varies by species; indices are scaled so the average index over the series equals 2.

- Data quality and validation
  - Automatic quality controls alert for anomalous counts or records outside known distributions or flight periods.
  - Regional coordinators check data quality; additional validation ensures consistency with known distributions and flight timings.

- Data storage and structure
  - Recorded data formats: stored as CSV files with detailed metadata columns.
  - Key columns include: Species (scientific name), Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change, 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, and 10-yr % change.
  - The dataset captures the number of years used for trends, statistical significance, and qualitative trend descriptions (e.g., rapid decline, rapid increase, stable).