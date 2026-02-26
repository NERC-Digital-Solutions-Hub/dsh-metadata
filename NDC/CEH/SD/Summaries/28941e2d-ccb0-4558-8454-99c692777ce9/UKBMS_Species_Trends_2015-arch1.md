# Experimental design/sampling regime

- Scope and purpose
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
  - Data support national indices and trends for different habitat groups and species, enabling analyses of abundance changes over time.

- Sampling regimes
  - All-species transects: fixed-route line transects at each site, recording all butterflies along a 2–4 km route in a fixed 5 m width, typically 26 counts per year from April to September.
  - Weather and timing: surveys conducted weekly only under suitable butterfly activity conditions, typically between 10:45 am and 3:45 pm.
  - Transect design: routes are fixed to enable year-to-year comparability and are divided into habitat/management sections.
  - Single-species transects: follow the all-species methodology but record only during a subset of weeks for the focal species.
  - Timed counts and egg/larval web counts: targeted counts for specific species within defined areas and time windows.
  - Wider Countryside Butterfly Survey (WCBS): introduced in 2009 as a reduced-effort survey sampling wider countryside habitats; two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per season.

- Data collection and entry
  - Field data recorded on standard forms; entered online via the UKBMS MyData site or Transect Walker software.
  - Data are uploaded to an Oracle database; regional transect coordinators compile data for their regions.

- Analytical methods
  - Wider countryside species: uses a two-stage model applying all counts in a season to estimate seasonal patterns, with daily values used as an offset to derive annual indices and trends (Dennis et al. 2013).
  - Habitat specialists and regular migrants: use General Additive Models (GAM) to impute missing values and produce a site index; data are combined to form a Collated Index, with missing values estimated via a log-linear regression model to generate national indices.
  - Trends: linear regression on collated indices to produce overall trends since 1976, plus sub-period trends (1996–2015 and 2006–2015).
  - Classification of species groups: WCBS-wide mobile species; habitat specialists (low mobility, semi-natural habitats); regular migrants (overwinter outside the UK).

- Nature and units of recorded values
  - Site indices: relative measures of population size, proportional to the actual population; conversion to comparably scaled indices across sites.
  - Collated Indices: presented as Log10 of the Collated Index (LCI), scaled so the average index over the series equals 2.
  - Trends: expressed as the slope of the Collated Index over the specified time period.

- Quality control and data validation
  - Automated checks in Transect Walker flag abnormal counts, out-of-season records, and misplacements.
  - Regional coordinators validate data, with ongoing checks throughout the season.
  - Additional automated/manual validation ensures records are within known distribution, flight periods, and consistency across sites and years.

- Format and content of stored data
  - Stored as CSV files with columns including:
    - Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change
    - 20-yr slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
    - 10-yr slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change
  - The dataset captures trend estimates across the full series and recent sub-periods, with descriptive trend labels (e.g., Rapid decline, Rapid increase, Stable) based on slope and significance.