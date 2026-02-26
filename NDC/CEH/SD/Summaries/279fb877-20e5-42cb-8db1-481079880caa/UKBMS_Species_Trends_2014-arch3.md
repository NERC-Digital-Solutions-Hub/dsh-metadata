# UK Butterfly Monitoring Scheme (UKBMS)

- Purpose and scope
  - A national monitoring program collating butterfly observations from over 2,000 sites annually across the UK.
  - Aims to produce population indices and trends to scrutinise environmental health, inform policy, and guide future decisions.
  - Distinguishes between wider countryside species, habitat specialists, and regular migrants for tailored analysis.

- Experimental design and sampling regime
  - All-species transects (Pollard walks): fixed-route line transects (typically 2–4 km) sampled weekly from April to September; counts recorded in a 5 m wide belt; routes fixed to enable year-to-year comparability.
  - Transects are conducted under suitable butterfly activity weather (specific temperature, wind, and sunshine criteria).
  - Single-species transects follow the same methodology but focus on selected focal species for a subset of weeks.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling since 2009 to cover wider habitats (farmland, etc.); uses two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per year (minimum 2 visits in July/August).

- Data collection methods
  - Field data recorded on standard forms; entered online via the UKBMS data entry site or via Transect Walker software.
  - Regional transect coordinators gather and submit all data for their region; data subsequently uploaded to an Oracle database.
  - Quality checks occur during and after entry, supported by automatic and manual validation processes.

- Analytical methods
  - Two-stage approach for wider countryside species: use all counts across a season to estimate a yearly seasonal pattern, then fit a model to observed counts with seasonal values as an offset to derive annual indices and trends.
  - For habitat specialists and regular migrants (with more missing data): use General Additive Models (GAMs) to impute missing values and derive site indices; combine into national Collated Indices.
  - Trends are estimated by linear regression on Collated Indices:
    - Whole time series (1976–2013 in the example)
    - Last 20 years (1993–2013)
    - Last 10 years (2003–2013)
  - Collated Indices are log-transformed (Log10) and scaled so the series’ average equals 2, enabling relative comparisons over time.
  - Acknowledge that not all sites are monitored every year; models account for year and site effects and update indices as new data arrive.

- Nature and units of recorded values
  - Site indices: relative measures of population size (not absolute counts); designed to be proportional to actual abundance.
  - Collated Indices: Log10-transformed, standardized to a mean of 2 for comparative purposes.
  - Trends: expressed as slopes (change per year) with associated significance.
  - Percentage changes: reported for overall and multi-year periods (e.g., 20-year, 10-year changes).

- Quality control
  - In-field automated checks (Transect Walker) flag anomalous counts or out-of-season records; recorders may adjust or confirm entries.
  - Regional coordinators validate data for their region; ongoing checks throughout the season.
  - Additional automated and manual validation steps verify out-of-range records, unusual distributions, new site records, and extreme values.

- Format and structure of stored data
  - Data stored in CSV format with detailed fields, including:
    - SCI_NAME (scientific name) and COMMON_NAME
    - NYEARS (years over which the series is calculated)
    - F_LIN_B, F_LIN_SE, F_LIN_P (slope, standard error, p-value)
    - F_TRENDDETAIL (textual description of overall trend)
    - F_FULL_R (overall percentage change)
    - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year metrics)
    - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year metrics)
  - Indices and trends are updated annually as new monitoring data are incorporated.
  - Data sharing and transparency considerations are addressed through explicit data governance and documentation of methods.