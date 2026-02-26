# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, primarily using fixed-route transects (Pollard walks) to estimate butterfly abundance, with alternative standardized methods (timed counts, egg/larval web counts) for some species or sites.
- All-species transects are designed to sample habitat types and management activity, with routes fixed to enable year-to-year comparison. Typical transects are 2–4 km, divided into habitat/management sections, and cover a 5 m wide belt along the route, with about 26 counts per year from April to September.
- Weather and time constraints are specified: counts occur between 10:45 and 15:45, under suitable butterfly activity conditions (specific temperature, wind, and sunshine criteria).
- Single-species transects follow the all-species methodology but focus on a focal species for a few weeks; timed counts and egg/larval web counts occur in designated periods when conditions are appropriate.
- Data recording follows standardized forms in the field, entered into Transect Walker software, and uploaded to an Oracle database; regional transect coordinators compile data for their regions.

- Data collection and management
  - Field records are entered into Transect Walker and then consolidated by regional coordinators; data are stored in an Oracle relational database.

- Analytical methods
  - After validation, a General Additive Model (GAM) is used to impute missing values and calculate a site index.
  - Site indices are combined into a national Collated Index for each species; because not all sites are monitored every year, a log-linear regression is employed to estimate missing values and derive indices and trends.
  - The Collated Index is updated annually as new data are incorporated; some early years may have shorter trend series due to data gaps.
  - Trends are computed via linear regression on the collated indices for:
    - the entire series (since 1976),
    - the last 20 years (1993–2013),
    - the last 10 years (2003–2013).
  - Indices are expressed as the log10 of the Collated Index, scaled so the series mean equals 2 to enable relative comparisons.
  - Trends include slope, standard error, p-value, and a textual trend description (rapid decline, rapid increase, or stable).

- Nature and interpretation of data
  - Site indices are relative population size measures, correlated with more intensive methods (e.g., mark–release–recapture); Collated Indices are presented as log10-transformed values.
  - The approach emphasizes relative changes over time rather than absolute counts, with clear indicators of statistical significance.

- Quality control and validation
  - Automatic checks in Transect Walker flag potential data entry errors (e.g., unusually high counts, records outside known flight periods).
  - Regional coordinators validate data; additional automatic and manual checks query out-of-range records, out-of-range distributions, first-time site records, and anomalous abundances.

- Data formats and storage
  - Species trends are stored as CSV files with columns including species, number of years, series slope, standard error, p-value, trend, and percentage changes; equivalent 20-year and 10-year slope, standard error, p-value, trend, and percent change fields are included.
  - The dataset uses scientific names (Fauna Europaea), common names, and time-series metadata to support longitudinal analyses.

- Implications for monitoring framework design
  - Demonstrates how fixed, standardized sampling coupled with rigorous QA, robust statistical treatment of missing data, and transparent data structures enables reliable long-term trend analysis.
  - Highlights the importance of methodical data governance, metadata clarity, and clear communication of uncertainty to stakeholders.
  - Reflects common practical challenges in environmental monitoring (data gaps, site coverage changes, and evolving indices) and how to address them through modeling and documentation.