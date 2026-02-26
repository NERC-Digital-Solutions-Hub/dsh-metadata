# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) gathers data from over 2,000 sites annually across the UK; coverage includes standard all-species transects and reduced-effort Wider Countryside Butterfly Survey (WCBS) transects.

- All-species transects: fixed-route line transect at a site; record all butterflies along a 2–4 km route in a 5 m wide band; typically 26 counts per year from early April to late September; sites chosen to sample habitat types and management activities; transects fixed to enable year-to-year comparisons.

- Transect timing and conditions: walks conducted 10:45–15:45 only under suitable butterfly activity weather (specific thresholds for dryness, wind, temperature, and sunshine).

- Data collection methods: data recorded on standard forms; entered online via UKBMS MyData or Transect Walker software; field data entered by recorders or regional transect coordinators; coordinators compile data for their region; online data eventually uploaded to an Oracle database.

- Variant methods:
  - Single-species transects: follow all-species methodology but record only during a few weeks of the focal species’ flight period.
  - Timed counts: record abundance of a focal species over a set time and area.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.
  - WCBS (established 2009): reduced-effort survey for wider countryside habitats; uses two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).

- Data processing and storage:
  - Field data entered into Transect Walker or UKBMS MyData; data uploaded to an Oracle database.
  - Each transect has a regional coordinator responsible for data quality and completeness.

- Analytical methods (national indices and trends):
  - Wider countryside species: two-stage model using data from all survey types; stage 1 uses a generalized additive model (GAM) to estimate annual seasonal flight patterns; stage 2 uses counts with seasonal values as an offset to estimate annual abundance changes; method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants: GAM to impute missing values and calculate a site index; combine site indices to derive a national annual index (Collated Index); log10 transformation applied to Collated Indices.
  - Trends: linear regression on Collated Indices to produce species trends over:
    - entire series (1976–2015),
    - last 20 years (1996–2015),
    - last 10 years (2006–2015).

- Nature and units of recorded values:
  - Site indices: relative measures of population size, proportional to actual abundance; reflect detectability differences among species.
  - Collated Indices: presented as Log10 of the Collated Index (LCI); standardized so the average index over the series equals 2.
  - Trends: reported as rate of change (slope) per year for the Collated Index; interpreted with thresholds (e.g., rapid decline/increase or stable).

- Quality control:
  - Automatic checks in Transect Walker flag unusual counts or records outside known flight periods.
  - Regional coordinators perform data validation; online data checked continuously during the season.
  - Additional validation procedures include checks for records outside known distribution, out-of-season records, first-time site records, and extreme or atypical abundances.

- Format and structure of stored data:
  - Species Trends stored as CSV with columns including:
    - Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change,
    - 20-yr Slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change,
    - 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change.
  - Columns reflect the calculation of long-term and recent trends, uncertainties, and qualitative trend descriptions.