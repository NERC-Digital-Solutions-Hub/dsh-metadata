# Experimental design/sampling regime

- Purpose and scale: UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to estimate butterfly abundance and trends.

- Primary data collection methods:
  - All-species transects (Pollard walks): fixed-route line transects, 2–4 km long, 45 minutes to 2 hours, 5 m width, 26 counts per year from April to September; weekly surveys under suitable weather.
  - Weather and timing constraints: surveys conducted 10:45–15:45 under conditions favorable to butterfly activity (quiet specific thresholds for wind, temperature, sunshine).
  - Transect routes are fixed to enable year-to-year comparisons and habitat/management sampling.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling along two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits per year (primarily July/August) to sample wider habitats.
  - Additional methods: single-species transects (fewer weeks), timed counts, and egg/larval web counts for specific species.

- Data collection and entry:
  - Field data recorded on standard forms; entered online via UKBMS data entry site or Transect Walker software.
  - Data submission managed by transect coordinators for each region; online data and Transect Walker files uploaded to an Oracle database.

- Analytical methods:
  - For WCBS and wider countryside species: two-stage modeling using all-season counts to estimate seasonal flight patterns and derive annual indices; generalised additive models (GAMs) used to fit seasonal patterns, with seasonality as an offset in a subsequent model to estimate annual changes.
  - For habitat specialists and regular migrants: GAMs impute missing values and create site indices; a log-linear regression on site indices yields a Collated Index (national annual index).
  - Trend estimation: linear regression on Collated Indices to produce species-wide trends over:
    - Entire series (1976–2016)
    - Last 20 years (1997–2016)
    - Last 10 years (2007–2016)
  - Updates: Collated Indices updated annually as new monitoring data are incorporated; past years may be revised.

- Data formats and units:
  - Site indices are relative measures tied to a proportional share of the actual population.
  - Collated Indices are expressed as Log10 of the Collated Index (LCI) to standardize comparisons.
  - Trends reported as slopes (change per year); accompanied by standard errors and p-values.

- Quality control and validation:
  - Automated checks in Transect Walker for data entry anomalies (e.g., unusually high counts, records outside flight periods).
  - Regional transect coordinators validate data, with ongoing checks throughout the season.
  - Additional automated/manual validations for species outside known distributions, atypical flight periods, first-time records at sites, and extreme deviations.

- Data storage and metadata:
  - Species Trends stored in CSV format.
  - Columns include: Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change, 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change, 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change.
  - Taxonomic naming follows Fauna Europaea; common names follow Emmet and Heath.
  - Data limitations noted: some species have shorter trend series due to insufficient years or data gaps; some early years may be missing from collated indices.

- Taxonomic and interpretation notes:
  - Classifications of species: Wider countryside species (mobile across habitats), habitat specialists (restricted to semi-natural habitats), and regular migrants (overwinter outside the UK).
  - Some species (e.g., Red Admiral) may be resident in parts of the UK but are generally treated as migrants.
  - Site indices are a relative measure; Collated Indices provide a broader national perspective, both tied to trend interpretations via slope significance.