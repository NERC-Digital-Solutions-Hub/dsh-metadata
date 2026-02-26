# The UK Butterfly Monitoring Scheme (UKBMS)

## Aim and scope for environmental analysts
- Monitors butterfly populations across the UK to provide a consistent, time-series view of environmental health and policy performance.
- Aggregates data from over 2,000 sites annually using standardized methods to enable cross-year comparisons and trend analysis.

## Data collection methods
- All-species transects (Pollard walks): fixed 2–4 km routes, 5 m wide band, weekly counts from April to September (ideally 26 counts/year). Routes fixed to sample habitat/management units; weather and daylight constraints apply (dry, Beaufort wind ≤5, temperature thresholds, sunshine conditions).
- Single-species transects: follow all-species methodology but recorded only on selected weeks for focal species.
- Timed counts and egg/larval web counts: counts over set periods/areas; weather constraints similar to transects.
- Wider Countryside Butterfly Survey (WCBS, established 2009): reduced-effort sampling in farmland and wider countryside; two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (plus recommended July/August spring visits).

## Data collection and management workflow
- Field data recorded on standard forms; entered online via UKBMS data entry site or via Transect Walker software.
- Data entry performed by recorders or regional transect coordinators; end-of-season consolidation by regional coordinators.
- Online data and Transect Walker outputs uploaded into an Oracle database housing all records.

## Analytical methods and outputs
- Two main analysis streams to produce national indices by species:
  - Wider countryside species
    - Two-stage model using all counts (all survey types) to estimate seasonal patterns and annual indices.
    - Stage 1: Generalised Additive Model (GAM) estimates daily seasonal flight pattern; normalised to a common seasonal pattern by year.
    - Stage 2: Full-annual-count model uses seasonal values as offsets to estimate year-to-year abundance changes.
    - Method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants
    - GAM imputes missing values and calculates site indices.
    - Collated Index (national annual index) derived by combining site indices via a log-linear regression; accounts for year and site effects.
    - Indices updated annually as new monitoring data are added; some years may have shorter series due to data availability.
- Group definitions:
  - Wider countryside species: mobile, wide habitat range.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK; transient presence each year.
  - Note: Red Admiral shows regional residency in parts of the UK but is generally considered a migrant.

## Nature and units of recorded values
- Site indices: relative measures of population size, proportional to actual abundance; allow comparability across sites and years.
- Collated Indices: expressed as the Log10 of the Collated Index (LCI); scaled so the mean index across the series is 2 for each species.
- Data completeness:
  - Collated Indices may be unavailable for some early years due to insufficient data; the dataset documents the number of contributing years per species/year.

## Quality control and data validation
- In-field automatic checks (Transect Walker) flag unusually high counts or records outside flight periods; options to adjust or confirm entries.
- Regional coordinators validate data for each region; ongoing checks during the season.
- Post-entry validation includes: records out of known distribution (cross-checked with BNMs and UKBMS data), out of flight period, first-ever site records, extreme or atypical abundances.
- Data are stored as CSV files with defined columns (Species, Common name, Year, No. Sites, Collated Index, Time period) to support traceability and reuse.

## Accessibility and reuse considerations
- Structured data outputs (site indices and Collated Indices) enable monitoring of environmental health and policy performance over time.
- The dataset emphasizes transparency and reusability, with data quality checks and clear documentation of methods, enabling other researchers and policymakers to access and interpret underlying data (subject to data governance and availability).

## Key data products and indicators
- Site indices: relative, site-level population indicators.
- Collated Indices (LCI): national trends per species on a consistent, annual basis.
- Documentation on data contributions (number of sites per year) and notes on data limitations for certain species in earlier years.

## References and methodological notes
- Methodological foundations and validation references provided (e.g., Dennis et al. 2013; Rothery & Roy 2001; Moss & Pollard 1993) for indices and modelling approaches.