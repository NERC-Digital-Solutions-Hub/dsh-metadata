# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
- Data types include:
  - All-species transects (Pollard walks): fixed-route line transects with 26 counts per year, typically 2–4 km long, 45 minutes to 2 hours, conducted weekly from April to September under suitable weather.
  - Reduced-effort Wider Countryside Butterfly Survey (WCBS): sampling wider countryside habitats with 2–4 visits per site per year.
  - Single-species transects: follow all-species methodology but recorded only during a few weeks for focal species.
  - Timed counts and egg/larval web counts: species-specific abundance counts within set times and areas.
- Transect design principles:
  - Transect routes are fixed to enable year-to-year comparability.
  - Timing and weather thresholds are specified (e.g., activity conditions, temperature, sunshine, wind).

- Data collection methods:
  - Field data recorded on standard forms; entered online via UKBMS data entry site (mydata) or via Transect Walker software.
  - Data entry can be done by the recorder or a regional transect coordinator.
  - Each transect coordinator aggregates data for all sites in their region; online data and Transect Walker files are uploaded to an Oracle database.

- Analytical methods:
  - Two main approaches to national indices:
    - Wider countryside species: uses all counts from all survey types in a two-stage model (generalised additive model to estimate seasonal patterns, off-set in a second stage to estimate annual changes).
    - Habitat specialists and regular migrants: uses GAM to impute missing values and create a site index; a log-linear model then produces a Collated Index (CIs) across monitored sites.
  - Trends are derived by linear regression on Collated Indices:
    - Across all years (1976–2013) for overall trends.
    - Over the last 20 years (1993–2013) and last 10 years (2003–2013).
  - Group definitions:
    - Wider countryside species: mobile species across varied habitats.
    - Habitat specialists: low mobility, semi-natural habitats.
    - Regular migrants: species overwintering outside the UK but arriving annually.

- Nature and units of recorded values:
  - Site indices are relative population size measures.
  - Collated Indices are log10-transformed and scaled so the average index across the series equals 2, enabling relative comparisons over time.
  - Trends are the slope (change per year) of the Collated Index.
  - Some species' series may be shorter due to data availability.

- Quality control:
  - Automatic checks in Transect Walker flag unusual counts or out-of-season records.
  - Regional transect coordinators review data and perform ongoing checks during the season.
  - Post-entry validation includes cross-checks against known distributions, flight periods, new site entries, extreme values, and deviations from normal site-level patterns.

- Format of stored data:
  - Species Trends data stored as CSV with fields including:
    - SCI_NAME (scientific name) and COMMON_NAME.
    - NYEARS (number of years in the series).
    - F_LIN_B, F_LIN_SE, F_LIN_P (slope, standard error, p-value for the whole series).
    - F_TRENDDETAIL (text description of overall trend).
    - F_FULL_R (percent change over the full series).
    - T20_LIN_B/SE/P and T20_TRENDDETAIL/T20_20_R (20-year metrics).
    - T10_LIN_B/SE/P and T10_TRENDDETAIL/T10_10_R (10-year metrics).
  - Metadata references and notes describe the methodological context and interpretation for these values.