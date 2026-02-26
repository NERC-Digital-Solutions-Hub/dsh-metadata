# UK Butterfly Monitoring Scheme (UKBMS)

- Overview
  - Data from over 2,000 sites annually across the UK.
  - Multiple data collection methods: all-species transects, single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).
  - Aims to monitor butterfly abundance and trends using standardized designs to enable year-to-year comparisons.

- Experimental design and sampling regime
  - All-species transects (Pollard walks): fixed 2–4 km routes, 5 m wide counts, weekly from April to September (ideally 26 counts/year); routes fixed to enable year-to-year comparisons.
  - Transect conditions: walks conducted 10:45–15:45 under suitable butterfly activity weather (dry, Beaufort wind < 5, temperature thresholds with sunshine or overcast).
  - Single-species transects: follow all-species methodology but recorded only during focal species flight periods.
  - Timed counts and egg/larval web counts: standardized time-limited observations for specific species.
  - WCBS (2009–present): reduced-effort survey sampling wider countryside habitats (farmland, etc.); two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year, with July/August as core periods.

- Data collection methods
  - Field data recorded on standard forms; entered online via the UKBMS data site or via Transect Walker software.
  - Data entry performed by recorders or regional transect coordinators; regional coordinators consolidate data end-of-season.
  - All data uploaded to an Oracle database storing the full records.

- Analytical methods
  - For wider countryside species: two-stage model using all survey data.
    - Stage 1: generalized additive model (GAM) to estimate annual seasonal flight patterns.
    - Stage 2: off-set seasonal values in a full annual counts model to estimate yearly abundance changes.
  - For habitat specialists and regular migrants (with missing data): GAM to impute missing values and compute site indices; a log-linear regression on collated indices yields national indices.
  - Collated Indices updated annually with new data; prior years’ indices may be revised as past data are incorporated.
  - Trends: linear regression on collated indices to produce species-wide trends over:
    - Whole series (1976–2015),
    - Last 20 years (1996–2015),
    - Last 10 years (2006–2015).

- Nature and units of recorded values
  - Site indices: relative measures of population size, not absolute counts; reflect a constant proportion of actual abundance and depend on detectability (varies by species).
  - Collated Indices: presented as log10 indices (Log10 Collated Index, scaled so average over the series equals 2).
  - Trends: expressed as the slope of the Collated Index over the specified time period.

- Quality control
  - Automatic checks in Transect Walker flag unusual entries (e.g., abnormally high counts, records outside flight periods).
  - Regional coordinators review data for each region; continuous-season validation.
  - Additional automated/manual validations target out-of-range records, records outside known distribution, first-time site records, and atypical abundances.

- Format of stored data
  - Stored as CSV with fields including:
    - Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change,
    - 20-yr: Slope, Std.Err, P-value, Trend, % change,
    - 10-yr: Slope, Std.Err, P-value, Trend, % change.