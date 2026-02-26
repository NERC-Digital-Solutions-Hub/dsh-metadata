# Experimental design/sampling regime

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
  - Data are gathered using fixed linear transects (Pollard walks) and additional standardized low-effort methods.
  - Multiple data products (all-species, single-species, timed counts, egg/larval web counts, and WCBS) feed national indices and trends.

- Data collection methods
  - All-species transects
    - Fixed-route line transect; all butterflies counted weekly under specified weather.
    - Transects 2–4 km long, divided into habitat/management sections; counts across a 5 m band from April to September (ideally 26 counts/year).
    - Weather/time windows: 10:45–15:45, suitable butterfly activity (dry, wind < Beaufort 5, temp thresholds depending on sun).
  - Single-species transects
    - Follow the all-species method but recorded only during a subset of flight-period weeks.
  - Timed counts and egg/larval web counts
    - Timed counts: fixed time and area, same daily weather constraints as transects.
    - Egg/larval web counts: count eggs/larval webs in suitable habitat areas.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort sampling in wider countryside; two parallel 1-km transects within randomly selected 1-km squares.
    - 2–4 visits per year, minimum 2 visits in July/August; spring visits encouraged.

- Data recording and storage
  - Field data recorded on standard forms.
  - Data entered online via UKBMS data entry site or Transect Walker software.
  - Regional transect coordinators compile data for all sites in their region.
  - Data uploaded to an Oracle database for storage and processing.

- Analytical methods and indices
  - Wider countryside species (mobile, diverse habitats)
    - Two-stage model using all survey data: Stage 1 generalised additive model (GAM) to estimate annual seasonal flight pattern; Stage 2 model uses seasonal values as an offset to estimate annual abundance changes.
    - Method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants (less WCBS data)
    - GAM-based imputation to estimate missing values and derive a site index.
    - Collated Index created by combining site indices; then a log-linear regression across collated indices to produce national trends.
  - Trend reporting
    - Trends calculated for each species over: 1976–2016 (whole series), last 20 years (1997–2016), and last 10 years (2007–2016).
    - Indices are relative (site index) or log-transformed collated indices (LCI); provide a consistent, comparable view over time.
  - Data updating
    - Collated Indices updated annually as new monitoring data are incorporated; past years’ indices can adjust slightly.

- Nature and units of recorded values
  - Site indices: relative measures of population size (not absolute counts), proportional to actual populations.
  - Collated Indices: log10-transformed; scaled so the average equals 2 across the series.
  - Trends: reported as slope (change per year) in Collated Index; include 5% significance criteria to categorize as rapid decline, rapid increase, or stable.

- Quality control and data validation
  - Automatic validation in Transect Walker flags unusual counts and out-of-season records.
  - Regional coordinators review records; continuous validation during the season.
  - Additional automated/manual checks for:
    - species outside known distribution
    - records outside known flight periods
    - first-time records at a site
    - extreme or unexpected abundances

- Data format and metadata
  - Output: Species Trends stored as CSV files.
  - Key CSV columns include:
    - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
    - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
    - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
  - Other notes:
    - Species categories defined (Wider countryside species, habitat specialists, regular migrants)
    - Some early years may lack collated indices due to insufficient data.