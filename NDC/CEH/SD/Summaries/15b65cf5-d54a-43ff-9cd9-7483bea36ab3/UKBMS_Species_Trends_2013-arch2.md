# The UK Butterfly Monitoring Scheme (UKBMS)

- Overview
  - Collects data from over 1,000 sites per year across the UK to monitor butterfly populations.
  - Uses standardized methods to estimate abundance and trends, enabling long-term environmental health assessment and policy performance scrutiny.
  - Outputs include site-level indices, national collated indices per species, and trend measures across multiple time periods.

- Experimental design and sampling regime
  - All-species transects (Pollard walks): fixed-route line transects 2–4 km long, surveyed weekly from April to September under suitable weather; each transect is divided into habitat/management units for consistent year-to-year comparisons.
  - All-species data are collected in a fixed 5 m wide band along the transect; typical effort yields about 26 counts per year per site.
  - Time of day and weather constraints: surveys conducted 10:45–15:45; suitable butterfly activity weather: dry conditions, wind < Beaufort 5, and temperature thresholds (≥13°C with at least 60% sunshine or >17°C if overcast).
  - Single-species transects and alternative methods (timed counts, egg/larval web counts) are used for particular focal species or protocols.

- Data collection and management
  - Field data recorded on standard forms and entered into Transect Walker software; data can be entered by the recorder or a regional transect coordinator.
  - Transect data are uploaded to an Oracle database; regional coordinators consolidate data for their regions.

- Analytical methods
  - Data validation precedes analysis, with automated and manual checks for entry errors, out-of-range records, and species flown outside normal periods or distributions.
  - General Additive Models (GAM) are used to impute missing values and compute site indices. Collated indices (per species) are derived by combining data from monitored sites and adjusting for varying yearly effort.
  - Indices are presented as log10(Collated Index) and scaled so the average index over the series equals 2, providing a relative measure of population size.
  - Trends are calculated by linear regression on collated indices:
    - Full series (since 1976)
    - Last 20 years (1993–2013)
    - Last 10 years (2003–2013)
  - Some species have shorter trends due to insufficient data in earlier years; the dataset documents the number of contributing years.

- Nature and units of recorded values
  - Site indices are relative population measures, proportional to actual abundance rather than absolute counts.
  - Collated Indices are transformed to a log scale (Log10) for consistency and comparability.
  - Trends are reported as slopes (change per year) with accompanying p-values and descriptive trend labels (e.g., rapid decline, stable).

- Quality control and data validation
  - Automatic checks in Transect Walker flag potential data issues; regional coordinators review and validate records.
  - Additional automated/manual validation to ensure records align with known distributions, flight periods, and typical counts.

- Format of stored data
  - Species Trends stored as CSV with fields including:
    - Species, Common name, No.years (years in the trend)
    - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
    - 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
    - 10-yr slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change
  - Trends and statistics are presented with standard error and significance indicators to support interpretation and replication.

- Interpretation and use
  - Site indices provide localized context; collated indices provide national-scale per-species perspectives.
  - The framework enables tracking of environmental health and policy outcomes over multiple timescales, with explicit caveats when data are sparse in earlier years.
  - Methodological references underpinning the approach include Pollard & Yates (1993) and subsequent methodological refinements (e.g., Rothery & Roy, Moss & Pollard).