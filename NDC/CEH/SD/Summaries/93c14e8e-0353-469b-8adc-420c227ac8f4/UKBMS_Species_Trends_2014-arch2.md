# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, using fixed transect methods to estimate butterfly abundance. Most sites use all-species transects; some use reduced-effort methods (Wider Countryside Butterfly Survey, WCBS) or other standardised methods (timed counts, egg/larval web counts).

- All-species transects
  - Fixed-route line transect at a site; all butterflies recorded along the route on a weekly basis during good butterfly activity.
  - Transect length typically 2–4 km; divided into habitat/management sections; counts cover a 5 m wide band along the transect.
  - Operational period: beginning of April to end of September, ideally 26 counts per year.
  - Transects are kept fixed to enable year-to-year comparability.
  - Walking times: 10:45 am to 3:45 pm; weather constraints include dry conditions, Beaufort wind < 5, and temperature thresholds (≥13°C with at least 60% sunshine or ≥17°C if overcast).

- Single-species transects
  - Follow the all-species transect methodology but only recorded on a few weeks during the focal species’ flight period.

- Timed counts and egg/larval web counts
  - Timed counts: record abundance of a focal species over a fixed period and area, under suitable weather.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.

- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort sampling since 2009 to cover wider countryside habitats (farmland, etc.).
  - Based on two parallel 1-km transects within randomly selected 1-km squares, using the fixed-route all-species transect approach.
  - Typically 2–4 visits per year, with a minimum of 2 visits in July/August; spring visits encouraged.

- Data collection and input
  - Field data recorded on standard forms and entered online via the UKBMS data site or Transect Walker software.
  - Data submitted by individual recorders or by regional transect coordinators; coordinators compile data for their region at season end.
  - Online data and Transect Walker outputs uploaded into an Oracle database that stores all records.

## Analytical methods

- National indices are produced using two distinct approaches:
  - Wider countryside species (WCBS and similar): two-stage model using all data across survey types.
    - Stage 1: Generalised additive model (GAM) to estimate the annual seasonal flight pattern for each species.
    - Stage 2: Use the estimated seasonal pattern as an offset in a full-count model to estimate annual changes in abundance, accounting for varying seasonality. See Dennis et al. 2013.
  - Habitat specialists and regular migrants (less WCBS data; more reduced-effort sampling): GAM-based imputation to compute a site index (Collated Index).
    - Impute missing values and combine site indices to derive a national annual index.
    - Since not all sites are monitored every year, a log-linear regression is used to estimate missing values and to produce indices/trends.
    - Collated Indices updated annually as more data are added; trends calculated from these indices.
- Trend calculation
  - Linear regression on collated indices to produce a simple measure of change over time for each species.
  - Time periods analyzed: 1976–2013 (whole series), last 20 years (1993–2013), and last 10 years (2003–2013).
  - Classification of trend direction/significance is based on slope and P-value (e.g., rapid decline/increase vs. stable).

## Nature and units of recorded values

- Site indices are relative measures of population size (not absolute counts), proportional to actual abundance, and are influenced by detectability differences among species.
- Collated Indices are reported as the logarithm (base 10) of the Collated Index (LCI) with the series mean scaled so that the average index equals 2; this provides a relative measure of population size over time.
- Trends are expressed as the slope of the Collated Index over the chosen time period. Percentage changes are given as a series change (%) or 20- and 10-year change metrics.

- Species categorisation
  - Wider countryside species: mobile species across a wide range of habitats.
  - Habitat specialists: low-mobility species restricted to semi-natural habitats.
  - Regular migrants: species that do not overwinter in the UK but arrive from continental Europe each year.
  - Note: Red Admiral may be resident in parts of southern England and Wales, but is treated as predominantly migratory UK-wide.

## Quality control

- Data validation in Transect Walker includes automatic checks for data-entry errors (e.g., abnormally high counts, records outside flight periods).
- Regional transect coordinators review and validate records; validation continues throughout the season.
- Additional automated and manual validation steps check for records outside known distributions, outside normal flight periods, first-time site records, extreme abundances, or abnormal site-year comparisons.
- Validation ensures data consistency before inclusion in analyses.

## Format of stored data

- Species Trends are stored as CSV files with columns including:
  - SCI_NAME (scientific name), COMMON_NAME, NYEARS (number of years in the series),
  - F_LIN_B (slope of the overall series), F_LIN_SE (standard error), F_LIN_P (P-value),
  - F_TRENDDETAIL (text description of the trend; e.g., rapid decline, stable),
  - F_FULL_R (overall percentage change),
  - T20_LIN_B/SE/P and T20_TRENDDETAIL/T20_20_R (20-year metrics),
  - T10_LIN_B/SE/P and T10_TRENDDETAIL/T10_10_R (10-year metrics).

- The data structure supports interpretation of long-term trends (1976–2013 and recent periods) while accommodating missing data and site-level variation.