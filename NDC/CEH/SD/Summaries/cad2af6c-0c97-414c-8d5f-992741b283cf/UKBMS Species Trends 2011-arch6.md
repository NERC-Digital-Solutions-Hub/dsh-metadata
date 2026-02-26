# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) aggregates data from over 1,000 sites annually across the UK to estimate butterfly population abundance using standardized methods.
- Recording methods are designed to enable year-to-year comparability and include multiple data collection approaches.

- All-species transects
  - Fixed-route line transect at a site, recording all butterflies along the route weekly.
  - Transects are typically 2–4 km, take 45 minutes to 2 hours, and subdivide into habitat/management sections.
  - Data collected in a 5 m wide band along the transect from early April to late September, ideally 26 counts per year.
  - Transect routes are fixed to allow year-to-year comparisons.
  - Observations occur 10:45–15:45 and only under suitable weather (dry, Beaufort wind ≤5, temperature ≥13°C with ≥60% sunshine or >17°C when overcast).

- Single-species transects
  - Follow the all-species methodology but record only one focal species during a subset of weeks.

- Timed counts and egg/larval web counts
  - Timed counts record abundance of a species over a set period/area, within the same daily time window as transects and under specified weather conditions.
  - Egg/larval web counts document eggs or larval webs in suitable habitat areas.

- Data collection methods
  - Field data are captured on standard forms.
  - Entries are made into Transect Walker software (free from UKBMS website), either by the recorder or a regional transect coordinator.
  - Each transect coordinator aggregates data for their region; Transect Walker files are uploaded to an Oracle database.

- Analytical methods
  - After validation, a General Additive Model (GAM) imputes missing values and computes a site index.
  - Site indices are combined to form a national annual index for each species (Collated Index) using a log10 transformation.
  - Not all sites are monitored every year, so a log-linear regression model estimates missing values and produces indices/trends that account for year and site effects.
  - Collated Indices are updated annually as more data are received; past years may be revised.
  - Trends are derived by linear regression on the collated indices for:
    - The full series (1976–2011)
    - The last 20 years (1992–2011)
    - The last 10 years (2002–2011)
  - Some species have shorter trend series due to insufficient early data.

- Nature and units of recorded values
  - Site indices are relative measures, proportional to actual population size; their detectability varies by species.
  - Collated Indices are presented as Log10 Collated Index (LCI), scaled so the average index over the series equals 2.
  - Trend outputs are slopes representing the rate of change per year.

- Quality control
  - Transect Walker performs automatic checks for data-entry errors (e.g., out-of-range counts, sightings outside flight period).
  - Regional coordinators review records for plausibility.
  - Additional automated/manual validation checks address out-of-range distributions, first-time site records, and unusual abundances.

- Format of stored data
  - Species Trends are stored as CSV with fields including:
    - Species (scientific name per Fauna Europaea)
    - Common name
    - No.years (years over which the series trend is calculated)
    - Series slope (trend over the full series)
    - Series Std.Err (standard error)
    - Series P-value (statistical significance)
    - Series trend (description: Rapid decline, Rapid increase, Stable)
    - Series % change
    - 20-yr Slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
    - 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change
  - The dataset provides both numerical statistics and qualitative trend descriptions for interpretation.