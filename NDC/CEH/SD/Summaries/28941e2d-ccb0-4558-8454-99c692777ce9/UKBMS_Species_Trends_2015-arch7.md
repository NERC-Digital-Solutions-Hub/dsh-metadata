# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, using multiple sampling methods to estimate butterfly abundance and trends.
- Sampling types:
  - All-species transects: fixed-route line transects (2–4 km) with a 5 m wide counted strip, typically 26 counts per year from April to September; weekly surveys under suitable weather.
  - Single-species transects: follow all-species transect methodology but recorded only for focal species during selected weeks.
  - Timed counts and egg/larval web counts: species-specific counts within set times/areas.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling along two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year, with spring encouragement.
- Transect design aims to sample habitat types and management, with routes fixed to allow year-to-year comparisons.

- Data collection workflow:
  - Field data recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker software.
  - Transect coordinators (regionally assigned) compile data for all sites in their region; data uploaded to an Oracle database.
  - Online data and Transect Walker files are available for upload into the central database.

- Analytical methods and indices:
  - Wider countryside species: two-stage model using all data (including all survey types) to estimate seasonal flight patterns with a Generalised Additive Model (GAM); uses seasonal values as an offset to estimate annual abundance changes; implemented as described by Dennis et al. (2013).
  - Habitat specialists and regular migrants: GAM used to impute missing values and compute site indices; site indices are combined to form a Collated Index; missing years are handled with a log-linear regression to estimate indices and trends.
  - Trends: a linear regression on collated indices to produce population-change trends since 1976; computed for the full series, the last 20 years, and the last 10 years.
  - Species categories: wider countryside (mobile across wide habitats), habitat specialists (low mobility in semi-natural habitats), regular migrants (overwinter outside the UK).

- Data products and units:
  - Site indices: relative measures of population size (not absolute counts); proportional to true abundance and subject to detection differences among species.
  - Collated Indices: given as Log10(Collated Index) with species-specific scaling so the average index over the series equals 2.
  - Trends: expressed as the rate of change in the Collated Index per year; provided for the full series, 20-year period, and 10-year period.
  - Data coverage notes: some early years lack collated indices for certain species due to limited data; trends may be shorter for those species.

- Quality control and validation:
  - Automatic range and data-entry checks in Transect Walker (e.g., improbable counts, out-of-season records).
  - Regional transect coordinators verify records; ongoing validation during the season.
  - Additional automated/manual checks against known distributions, normal flight periods, first-time site recordings, and extreme values.

- Data storage and format:
  - Species Trends are stored as CSV files.
  - Columns include: Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr slope/Std.Err/P-value/Trend/% change, 10-yr slope/Std.Err/P-value/Trend/% change.
  - Scientific names follow Fauna Europaea; common names follow standard references.
  - Indices are log-transformed (Log10 Collated Index) and scaled to enable comparisons across species and time.

- GIS and mapping implications:
  - Fixed transects and WCBS squares provide explicit spatial units suitable for mapping and spatial analyses.
  - Data flows from field collection to GIS-ready outputs (CSV exports) via Transect Walker and the Oracle database.
  - Indices and trends enable map-based visualization of spatial and temporal population changes across sites, regions, and habitat types.
  - Differences in data density (wide vs. specialist species) are accounted for in modelling, which informs what is suitable for map-based storytelling and policy briefings.