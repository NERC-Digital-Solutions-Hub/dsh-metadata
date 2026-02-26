# UK Butterfly Monitoring Scheme (UKBMS) Methodology

- Overview
  - UKBMS collects data from over 1,000 sites annually across the UK to monitor butterfly populations.
  - Uses multiple standardized survey methods to estimate abundance across species and sites.

- Experimental design and transect types
  - All-species transects (Pollard walks): fixed-route line transects, 2–4 km long, with 5 m wide recording bands, typically 26 counts per year from early April to late September.
  - Transect schedule: counts conducted weekly under suitable butterfly activity conditions, typically 10:45 am to 3:45 pm; weather criteria include dry conditions, wind < Beaufort 5, and temperature thresholds (≥13°C with ≥60% sunshine or >17°C if overcast).
  - Transects are fixed to allow year-to-year comparability; routes sampled to reflect habitat types and management on sites.
  - Single-species transects: follow the all-species methodology but focus on one focal species for a few weeks within the flight period.
  - Timed counts and egg/larval web counts: record abundances of specific species over fixed time periods or count eggs/larval webs in suitable habitats.

- Data collection methods
  - Field data recorded on standard forms.
  - Data entered into Transect Walker software (free download on UKBMS site) by recorders or regional transect coordinators.
  - Transect Walker files uploaded to an Oracle database holding all records.
  - Each transect has a regional coordinator responsible for data validation within their region.

- Analytical methods and indices
  - After validation, missing values are imputed using a General Additive Model (GAM) to derive site indices.
  - Site indices across sites are combined to produce a national annual index for each species (the Collated Index, CI).
  - Since not all sites are monitored every year, a log-linear regression model is used to estimate missing values and produce indicators and trends.
  - Collated Index updates annually as new data are added; past years may be revised.
  - Trends are derived by linear regression on the collated indices:
    - Whole series: 1976–2012
    - 20-year period: 1993–2012
    - 10-year period: 2003–2012
  - Some species lack collated indices in early years due to insufficient data; these omissions are indicated in the dataset.

- Nature and units of recorded values
  - Site indices are relative measures of population size, proportional to actual population size.
  - Collated Indices are presented as log10(CI) to provide a relative size metric over time.
  - Trends are the slope of the CI over the specified time period.
  - For each species: number of years, series slope, standard error, p-value, trend description (rapid decline, rapid increase, stable), and percent change for both the overall series and the last 20/10 years (including 20-yr and 10-yr slopes and p-values).

- Quality control and validation
  - Automatic checks in Transect Walker flag potential data entry errors (e.g., abnormally high counts, records outside known flight periods).
  - Regional coordinators review records for plausibility and consistency within their region.
  - Additional automated and manual validation: checks for out-of-range records, records outside known distribution, first-time site records, extreme abundances, and unusual seasonal patterns.

- Format of stored data
  - Species Trends stored as a CSV file with columns including:
    - Species (scientific name) and Common name
    - No.years (years in the series)
    - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
    - 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
    - 10-yr slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change

- Data use, reporting, and accessibility
  - Collated indices enable cross-site and cross-year comparisons, informing national and species-specific trends.
  - Indices and trends are updated with new monitoring data; trends reflect the most current fits given data availability.
  - Data management emphasizes traceability of data sources and the potential for datasets to be discoverable via portals with accompanying metadata.

- Notes on scope and limitations
  - Indices and trends depend on the availability and coverage of monitoring sites; not all species have full time-series coverage.
  - Early-year trends may be shorter for certain species due to insufficient data in those periods.
  - Relative indices may vary in detectability across species due to conspicuousness and flight behavior.