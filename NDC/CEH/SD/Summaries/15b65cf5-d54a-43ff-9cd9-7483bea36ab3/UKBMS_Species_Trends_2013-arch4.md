# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK to monitor butterfly populations.
  - Data support the development of site-level indices and national trends, enabling assessment of changes over time.

- Sampling design
  - All-species transects: fixed-route line transect (2–4 km) surveyed weekly during April–September under suitable weather; 5 m wide belt, typically 26 counts per year, with transects chosen to represent habitat and management variation and kept fixed for year-to-year comparability.
  - Single-species transects: follow the all-species methodology but record for only a few focal weeks.
  - Timed counts and egg/larval web counts: conduct species-specific counts in designated areas during flight periods or suitable habitat conditions.
  - Weather and activity constraints: surveys occur between 10:45 and 15:45 with specific conditions (e.g., temperature, wind, sunshine) to ensure butterfly activity.

- Data collection workflow
  - Field data are recorded on standard forms and entered into Transect Walker (free software).
  - Data can be entered directly by recorders or by regional transect coordinators.
  - Transect Walker data are uploaded to an Oracle database, housing all records; regional coordinators compile data for their regions.

- Data processing and analysis
  - After validation, a General Additive Model (GAM) imputes missing values and computes site indices.
  - Site indices are aggregated to produce a national Collated Index per species, represented as Log10(Collated Index) to enable relative comparisons.
  - Missing values and trends are estimated via a log-linear regression model, accounting for year and site effects.
  - Trends are calculated for:
    - The full time series (since 1976)
    - The last 20 years (1993–2013)
    - The last 10 years (2003–2013)
  - Note: Collated Indices may be revised as new data are received; not all species have complete series in earlier years due to data sparsity.

- Data quality, validation, and governance
  - Automated validation within Transect Walker flags anomalies (e.g., unusually high counts, out-of-season records).
  - Regional coordinators perform additional checks, followed by automated and manual validation steps (including cross-checks against known distributions, flight periods, and site occurrence).
  - Data are stored with metadata describing species, years, slopes, standard errors, p-values, trends, and percentage changes over different time periods.

- Data format and metadata
  - Primary data outputs are stored as CSV files with detailed columns, including:
    - Species (scientific name per Fauna Europaea)
    - Common name
    - No.years (years contributing to the series)
    - Series slope, Std.Err, P-value, Trend, % change
    - 20-year and 10-year slopes, Std.Err, P-values, Trends, % changes
  - Site indices are relative measures (not absolute population sizes) and are derived from a proportional relationship to actual counts.
  - Data are scaled so that the average index over the series equals 2 for comparability.
  - Taxonomic references and source methodologies (e.g., Pollard & Yates; Moss & Pollard) underpin the analytical approach.

- Accessibility and reuse
  - Transect Walker is freely downloadable from the UKBMS website.
  - The data flow moves from field collection to an Oracle database, with CSV-derived outputs for analyses and public dissemination of trends varying by dataset.

- Implications for data leaders
  - Emphasizes standardized, auditable data collection and processing pipelines (field forms → Transect Walker → Oracle DB → GAM/COLLATED INDEX).
  - Highlights the need for ongoing data quality assurance, clear metadata, and transparent handling of revisions as new data are incorporated.
  - Demonstrates how complex temporal analyses (full series, 20-year, 10-year trends) are derived from a hierarchical data architecture, enabling governance of long-term monitoring programs and informing cross-network data collaborations.