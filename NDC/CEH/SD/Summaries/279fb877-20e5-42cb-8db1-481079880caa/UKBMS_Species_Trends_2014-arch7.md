# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
  - Data are primarily obtained from fixed transects (Pollard walks) to estimate butterfly abundance and trends, with variations for different survey types (all-species, wider countryside surveys, timed counts, larval web counts).

- Sampling regimes and data collection
  - All-species transects:
    - Fixed-route line transects (typically 2–4 km) walked weekly from April to September.
    - Butterflies recorded within a fixed 5 m wide belt along the transect.
    - Transects are chosen to reflect habitat types and management; routes remain fixed year to year for comparability.
    - Walks occur in specific weather windows (time of day, wind, temperature, and sunshine conditions).
  - Wider Countryside Butterfly Survey (WCBS):
    - Reduced-effort survey established in 2009 to sample wider countryside habitats.
    - Based on two parallel 1-km transects, subdivided into 10 sections within randomly selected 1-km squares.
    - Typically 2–4 visits per year (minimum two visits in July/August; spring visits encouraged).
  - Data collection workflow:
    - Field data recorded on standard forms; entered online via UKBMS MyData or via Transect Walker software.
    - Data uploaded by regional transect coordinators to an Oracle database; later consolidated and managed.

- Data processing and analysis
  - Two analytical approaches by species group:
    - Wider countryside (mobile) species:
      - Two-stage model using all survey data to estimate seasonal patterns and annual indices.
      - Stage 1: Generalised additive model (GAM) to estimate the annual seasonal flight pattern for each species.
      - Stage 2: Model uses seasonal values as an offset to estimate annual abundance changes (accounting for variable seasonality).
    - Habitat specialists and regular migrants (with less WCBS data):
      - GAM to impute missing values and calculate a site index.
      - Collated Index: derived from country-wide site indices; used with log-linear regression to estimate national trends.
      - Trends computed using linear regression on collated indices over time: full series (1976–2013), last 20 years (1993–2013), and last 10 years (2003–2013).
  - Key concepts:
    - Collated Index is an annual national index for each species, updated as new data arrive.
    - Site index represents a relative, not absolute, population size; normalized to reflect comparable scales.

- Data formats and values
  - Site indices are relative measures that correlate with more intensive population size metrics.
  - Collated Indices are presented as Log10 (LCI) values, scaled so the series average equals 2.
  - Trends are reported as slopes (rate of change per year) with associated statistics.
  - Data include multiple time-horizon metrics: full-series slope, 20-year slope, 10-year slope, and corresponding p-values and trend descriptions.
  - Species are categorized as:
    - Wider countryside species (mobile, broad habitat range).
    - Habitat specialists (low mobility, semi-natural habitats).
    - Regular migrants (seasonal arrivals from continental Europe).

- Quality control and data validation
  - Automatic checks within Transect Walker flag anomalous counts or records outside known flight periods.
  - Regional transect coordinators review data for questionable entries; validation continues throughout the season.
  - Post-entry validation includes checks for records outside known distribution, out-of-season records, first-time site records, extreme values, or unusual deviations.

- Data storage and access
  - The primary data product for analyses, Species Trends, is stored as a CSV file.
  - Columns include: SCI_NAME, COMMON_NAME, NYEARS, F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL, F_FULL_R, T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R, T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R, and related descriptive fields.
  - The dataset integrates counts, indices, slopes, standard errors, p-values, trend descriptions, and percentage changes across multiple timeframes.

- Limitations and notes
  - Collated Indices may be revised as new data are incorporated, potentially altering earlier year trends.
  - Earlier recording years may lack sufficient data for robust trend calculation, resulting in shorter or incomplete series for some species.
  - Data interpretation requires consideration of year effects (weather variability) and site effects in the models.