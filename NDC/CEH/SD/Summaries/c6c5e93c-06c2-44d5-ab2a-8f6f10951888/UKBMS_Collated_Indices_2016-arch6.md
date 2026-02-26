# The UK Butterfly Monitoring Scheme (UKBMS)

- Purpose and scope
  - The UKBMS aggregates butterfly data from over 2,000 sites annually across the UK.
  - Data come from standard methods (all-species transects and Wider Countryside Butterfly Survey) and, at times, other standardized approaches (timed counts, egg/larval web counts).

- Data collection methods
  - All-species transects
    - Fixed-route line transects sampled weekly from early April to late September.
    - Routes are chosen to reflect habitat and management; routes fixed to enable year-to-year comparisons.
    - Typical length: 2–4 km; 45 minutes to 2 hours to walk; recorded within a 5 m wide band.
    - Weather constraints: suitable butterfly activity conditions; specific times (roughly 10.5:00–15:45) and temperature/wind criteria.
  - Single-species transects
    - Follow the all-species method but focus on one focal species for selected weeks.
  - Timed counts and egg/larval web counts
    - Timed counts: fixed area and time, following weather guidelines.
    - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort survey in wider countryside habitats (farmland, etc.), modeled after the BTO Breeding Bird Survey.
    - Two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per season, with minimum July/August visits.

- Data recording and flow
  - Field data captured on standard forms.
  - Online data entry via the UKBMS data site or via Transect Walker (free download).
  - Data entered by recorders or regional transect coordinators; coordinators gather data for all sites in their region.
  - Online data and Transect Walker files uploaded to an Oracle database housing all records.

- Roles and data governance
  - Regional transect coordinators supervise data from their regions.
  - Continuous quality checks occur during data entry and via automated/manual validation post-entry.

- Analytical methods and indices
  - Two main approaches by species group:
    - Wider countryside species (mobile, across diverse habitats)
      - Two-stage model using all counts in a season to estimate a seasonal flight pattern (generalised additive model in stage 1).
      - Normalised daily values yield a seasonal pattern; stage 2 uses full annual counts with seasonal pattern as an offset to estimate annual abundance changes.
      - Described in Dennis et al. 2013.
    - Habitat specialists and regular migrants (less WCBS data; more reduced-effort data)
      - General Additive Model (GAM) to impute missing values and derive a site index.
      - Collated Index (across sites) produced by combining site indices; uses log-linear regression to account for year and site effects and to estimate missing values.
      - Collated Indices updated annually as more data are added; indices for species with data from at least five sites per year.
  - Index types
    - Site indices: relative measures of population size, representing a constant proportion of the actual population depending on species.
    - Collated Indices: presented as the base-10 logarithm (LCI); scaled so the average index over the full series equals 2, providing a relative temporal measure of population size.

- Taxa definitions and data coverage
  - Wider countryside species: mobile, found across wider habitats.
  - Habitat specialists: low mobility, constrained to semi-natural habitats.
  - Regular migrants: species that overwinter outside the UK; annually influx from continental Europe.
  - Data gaps: some early years have no Collated Indices due to insufficient data; series length is noted in datasets.

- Data quality control and validation
  - In-platform automatic checks (e.g., implausible counts, flight-period anomalies) during data entry.
  - Regional coordinators validate data; continuous checks throughout the season.
  - Additional automated/manual validation to flag out-of-range distributions, first-time site records, unusually high/low abundances, and other anomalies.
  - Validation guidance includes cross-checks against Butterfly Conservation resources and existing UKBMS data.

- Data products and storage
  - Collated Indices stored as CSV files.
  - Columns include: Species (scientific name), Common name, Year, No. Sites, Collated Index, Time period.
  - The Collated Index for each species is derived from monitoring data and may revise historical values as new data are incorporated.

- References and methodological notes
  - Key methods and validation approaches cited from Dennis et al. (2013), Rothery & Roy (2001), Moss & Pollard (1993), and Pollard & Yates (1993).
  - Collated indices and site indices are designed to enable tracking temporal trends while accounting for missing data and varying yearly conditions.