# Experimental design/sampling regime

- Global aim
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 UK sites annually to monitor butterfly abundance and trends through standardized methods.

- Sampling design
  - All-species transects (Pollard walks): fixed-route 2–4 km, weekly counts Apr–Sept, in suitable weather; routes fixed to allow year-to-year comparisons.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort survey along two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits per year (minimum 2 in Jul/Aug; spring visits encouraged).
  - Single-species transects, timed counts, and egg/larval web counts follow similar protocols but with differing survey intensity and focus.

- Data collection and field procedures
  - Field data recorded on standard forms; entered online via UKBMS MyData or Transect Walker software.
  - Data uploaded from field forms to an Oracle database; regional transect coordinators compile and submit data for their regions.

- Data entry and flow
  - Recording done by field observers or coordinators; data entered online or via Transect Walker; data then centralized in an Oracle database.

- Analytical methods (two-path approach by species group)
  - Wider countryside species (mobile across habitats)
    - Two-stage model using all counts to estimate seasonal flight patterns and annual indices.
    - Stage 1: Generalized Additive Model (GAM) to estimate daily seasonal pattern.
    - Stage 2: Seasonal values used as an offset in a full-count model to estimate annual abundance changes.
  - Habitat specialists and regular migrants
    - GAM to impute missing values and derive a site index for each monitored site.
    - Collated Index: aggregate index across sites via log10 transformation; updated annually as new data are added.
    - Trend estimation: linear regression on collated indices to derive species-wide trends since 1976.
  - Time periods for trends
    - Overall trend: 1976–2013
    - Last 20 years: 1993–2013
    - Last 10 years: 2003–2013

- Data quality and validation
  - Automated checks in Transect Walker flag improbable data (e.g., abnormally high counts, out-of-flight-period records).
  - Regional coordinators review records; continuous validation during the season.
  - Further automated/manual validation includes consistency with known distributions, flight periods, first-time site records, and atypical abundances.

- Nature and units of recorded values
  - Site indices: relative measures of population size, not absolute counts; derived from counts and adjusted for detection differences.
  - Collated Indices: expressed as Log10(Collated Index); scaled so the average index across the series equals 2.
  - Trends: slopes representing annual change in the Collated Index; values accompany standard errors, P-values, and qualitative trend descriptions (rapid decline, rapid increase, or stable).

- Data storage and structure
  - Species Trends stored as CSV files.
  - Key fields include:
    - SCI_NAME (scientific name), COMMON_NAME
    - NYEARS (number of years in the series)
    - F_LIN_B, F_LIN_SE, F_LIN_P (overall linear slope, SE, P-value)
    - F_TRENDDETAIL (text description of overall trend)
    - F_FULL_R (percentage change over the full series)
    - T20_LIN_B/SE/P, T20_TRENDDETAIL, T20_20_R (20-year metrics)
    - T10_LIN_B/SE/P, T10_TRENDDETAIL, T10_10_R (10-year metrics)
  - Columns reflect the two-stage analytical outputs, recent trends, and descriptive trend narratives.

- Definitions and taxonomic/groupings
  - Wider countryside species: mobile species across many habitats.
  - Habitat specialists: low-mobility species restricted to semi-natural habitats.
  - Regular migrants: species overwintering outside the UK or arriving from continental Europe annually.
  - Red Admiral: may be resident in parts of the UK, but generally treated as migratory.

- Temporal and data coverage notes
  - Collated indices depend on the number of contributing sites each year; earlier years may have incomplete series for some species.
  - Indices can be updated as new monitoring data are integrated, potentially altering past trend values slightly.