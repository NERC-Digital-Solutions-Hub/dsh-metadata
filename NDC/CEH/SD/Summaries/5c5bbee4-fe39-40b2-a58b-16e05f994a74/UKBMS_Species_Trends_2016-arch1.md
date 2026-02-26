# UK Butterfly Monitoring Scheme (UKBMS) methodology

- Overview
  - UKBMS collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
  - Data come from multiple collection methods (all-species transects, single-species transects, timed counts, larval/egg counts) and are processed into national and site-specific indices and trends.

- Experimental design and sampling regime
  - All-species transects:
    - Fixed-route line transects (2–4 km) sampled weekly from early April to late September.
    - 5 m wide band along the transect; aim for ~26 counts per year.
    - Transects are fixed to enable year-over-year comparison and are divided into habitat/management sections.
    - Walk times: typically 10:45–3:45, under suitable butterfly activity conditions (dry, Beaufort wind < 5, temperature thresholds with sunshine/overcast adjustments).
  - Wider Countryside Butterfly Survey (WCBS):
    - Reduced-effort sampling in wider countryside habitats; two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum two in July/August; spring visits encouraged).
  - Single-species transects:
    - Follow the all-species methodology but record only during select weeks for the focal species.
  - Timed counts and egg/larval web counts:
    - Targeted counts within a set area and time window; egg/larval counts in suitable habitats for certain species.

- Data collection methods
  - Field recording on standard forms.
  - Online data entry via UKBMS data portal or Transect Walker software.
  - Data entered by recorders or regional transect coordinators; uploaded to an Oracle database.

- Analytical methods
  - Two main approaches by species group:
    - Wider countryside species (mobile across habitats):
      - Use all counts in a season to estimate the annual seasonal pattern (two-stage model).
      - Stage 1: Generalised Additive Model (GAM) estimates daily seasonal flight pattern; values normalised to a common seasonal pattern per year.
      - Stage 2: Full annual counts model with seasonal pattern as an offset to estimate annual abundance changes.
      - Method described in Dennis et al. (2013).
    - Habitat specialists and regular migrants (less complete WCBS data; use reduced-effort counts):
      - GAM to impute missing values and calculate site index.
      - Collated Index (across sites) derived; missing values imputed with a log-linear regression model accounting for year and site effects.
      - Collated Indices updated annually as new data arrive; include species with data from at least five sites per year.
      - Linear regression on collated indices to produce a simple trend since 1976, plus sub-period trends (1997–2016, 2007–2016).
  - Species categories:
    - Wider countryside species: mobile, broad habitat use.
    - Habitat specialists: low mobility, semi-natural habitats.
    - Regular migrants: overwinter outside the UK; arrive annually.
  - Output metrics:
    - Collated Indices: log10 transformed; scaled so the series average equals 2.
    - Trends: computed as slope of Collated Index over time; reported with time windows (1976–2016, 1997–2016, 2007–2016).

- Nature and units of recorded values
  - Site indices are relative measures of population size and correlate with more intensive methods (e.g., MRR).
  - Collated Indices are log10-transformed; trends are slopes indicating rate of change per year.
  - Some species have shorter trend series if data are sparse or unevenly distributed.

- Quality control
  - Automatic checks in Transect Walker flag anomalous counts or records outside known flight periods.
  - Regional transect coordinators validate records; continuous review during the season.
  - Additional automated/manual validation for out-of-range distributions, first-time site records, extreme abundances, or unusual temporal patterns.

- Format of stored data
  - Stored as CSV with columns including:
    - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
    - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
    - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
  - Key interpretation notes:
    - Series slope and p-value indicate longer-term trends across the entire series.
    - 20-year and 10-year metrics provide shorter-term trend perspectives.
    - Trends are categorized (e.g., Rapid decline, Rapid increase, Stable) based on slope direction and significance.