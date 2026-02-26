# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly populations and derive national indices and trends.
- Data collection centers on fixed-route transects (Pollard walks) for all-species counts, with reduced-effort schemes (Wider Countryside Butterfly Survey, WCBS) and specialist methods (timed counts, egg/larval web counts) for broader or different habitat use.
- Transects are 2–4 km long, divided into habitat/management sections, walked weekly during April–September, in favorable weather, and within a fixed route to enable year-to-year comparisons.
- WCBS uses two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per year, designed to sample wider countryside habitats.
- Single-species transects, timed counts, and larval/web counts are conducted during the focal species’ flight period and under specified weather conditions.
- Field data are recorded on standard forms and entered online (UKBMS site) or via Transect Walker, then uploaded to an Oracle database; regional transect coordinators compile data for their areas.

- Analytical framework differentiates species groups:
  - Wider countryside species (mobile, broad habitat range): a two-stage model using all survey data to estimate seasonal patterns and compute annual indices, accounting for varying seasonality.
  - Habitat specialists and regular migrants (more data from reduced-effort methods): a General Additive Model (GAM) imputes missing values and derives site indices; a log-linear model estimates missing values to produce national indices.
- Indices and trends:
  - Collated Indices synthesize site data into annual national indices per species; used to compute trends across time (1976–2013, with recent 20-year and 10-year windows examined).
  - For wider countryside species, trends are based on the all-data, multi-method approach; for specialists/migrants, trends rely on imputed site indices.
  - Linear regression on collated indices yields a simple measure of abundance change over time.

- Nature and units of recorded values:
  - Site indices are relative population measures, reflecting a constant proportion of actual abundance.
  - Collated Indices are presented as Log10 Collated Index (LCI) per species; trends are slopes of the collated index over time.
  - Trend details categorize direction and significance (rapid decline/increase or stable) based on slope and P-value thresholds.
- Data products include annual, multi-decadal (e.g., 20-year, 10-year) trends and percent changes, with updates as new data are received.

- Quality control and validation:
  - Automatic checks in Transect Walker flag unusual counts or out-of-season records; regional coordinators validate and can adjust data.
  - Continuous validation throughout the season, plus follow-up queries against known distributions, flight periods, first-site records, and anomalous abundances.

- Data storage and schema:
  - Species Trends are stored in CSV format with fields such as SCI_NAME, COMMON_NAME, NYEARS, and a range of statistical metrics (slopes, standard errors, P-values, trend descriptions, percent changes) for overall series, plus 10-year and 20-year windows.
  - Columns include detailed slope metrics (F_LIN_B, F_LIN_SE, F_LIN_P), trend descriptions (F_TRENDDETAIL), and analogous 10- and 20-year equivalents (T10_LIN_B, T20_LIN_B, etc.).

- GIS and mapping implications:
  - Data are linked to precise transect locations and, for WCBS, 1-km squares, enabling spatial visualization of trends by site or square.
  - Relative indices allow comparative mapping of trends across species and regions, though units are relative rather than absolute population sizes.
  - Handling of missing data and year-to-year variability is critical for accurate spatial trend analyses; ongoing data validation improves reliability for map-based products.

- Key constraints and considerations for GIS use:
  - Data heterogeneity across methods and years; not all sites contribute every year, affecting completeness.
  - Early years have incomplete species coverage, impacting long-term trend robustness for some taxa.
  - Indices are updated as new data arrive, potentially altering previous year trends and necessitating version-aware mapping.