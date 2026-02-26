# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, using multiple data collection methods to sample butterfly populations.
- Primary methods include:
  - All-species transects (Pollard walks): fixed-route line transects (2–4 km) walked weekly from April to September under suitable weather; 5 m wide recording band; routes fixed to enable year-on-year comparisons; typically 26 counts per site per year.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling along two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum two in July/August, spring visits encouraged).
  - Additional methods: single-species transects (few weeks per focal species), timed counts, and egg/larval web counts.
- Transect timing and conditions are carefully specified (time windows, weather criteria, and habitat sampling considerations) to ensure comparability across years.

# Data collection and processing

- Field data are recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker software; regional transect coordinators compile data for their region.
- Data are uploaded to an Oracle database; quality control includes automatic checks in Transect Walker and validation by regional coordinators, with additional automated/manual checks for out-of-range records, unusual flight periods, new site records, extreme counts, and unusual site-year combinations.

# Analytical methods

- The UKBMS uses two analytical approaches depending on species category:
  - Wider countryside (mobile, broad habitat use) species:
    - A two-stage model uses all counts from all survey types to estimate the annual seasonal flight pattern (generalised additive model, GAM) and standardises counts by seasonality.
    - In the second stage, a model with seasonal values as an offset estimates annual abundance changes, producing an annual Collated Index for each species.
  - Habitat specialists and regular migrants (less WCBS data; more reduced-effort sampling):
    - A GAM imputes missing values and calculates a site index; site indices are combined to derive a national annual index (Collated Index).
    - A log-linear regression on collated indices yields trends, accounting for year effects and site effects; indices are updated annually as new data arrive.
- Trends and indices:
  - Collated Indices are derived for species observed at five or more sites per year.
  - National trends are computed via regression on collated indices for three periods: the entire series (1976–2013), the last 20 years, and the last 10 years.
  - For wider countryside species, a two-stage approach normalises seasonal patterns across years but allows year-to-year variation; for habitat specialists/regular migrants, missing values are imputed to create a complete site index for trend estimation.

# Data structure and measurements

- Site indices provide a relative measure of population size, proportional to true abundance, with detectability influenced by species traits.
- Collated Indices are presented as the logarithm (Log10) of the Collated Index (LCI), scaled so the average index over the series equals 2.
- Reported outputs include:
  - Series slope (per-year change) and standard error
  - P-values and textual trend descriptions (rapid decline, rapid increase, stable)
  - Percentage change over the full series and over 20-year and 10-year periods
  - 20-year and 10-year slopes, standard errors, P-values, and trend descriptions
- Data are stored as CSV files with fields such as scientific name, common name, number of years in the series, slopes, standard errors, P-values, trend details, and percentage changes.

# Quality assurance and data governance

- Ongoing data validation combines automated checks and regional oversight to maintain data integrity.
- Validation includes consistency with known distributions and flight periods, detection of anomalous records, and checks against established distribution and flight-period ranges.

# Data format and accessibility

- The primary stored output is a CSV file containing species trends and related statistics, with clearly defined columns for identifiers, metrics, and trend descriptors.
- The dataset provides multiple time-based perspectives (entire series, 20-year, 10-year) to support long-term monitoring and recent trend detection.