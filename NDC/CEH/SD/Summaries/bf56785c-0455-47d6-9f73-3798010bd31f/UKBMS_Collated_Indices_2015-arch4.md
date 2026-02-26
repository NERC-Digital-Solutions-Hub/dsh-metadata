# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
- Data come from multiple methods: fixed-route all-species transects (Pollard walks), reduced-effort Wider Countryside Butterfly Survey (WCBS) transects, single-species transects, timed counts, and egg/larval web counts for specific species.
- Data are used to produce national and site-level indices of abundance, with methods tailored to data richness by species group.

## Data collection methods
- All-species transects: fixed routes (2–4 km) walked weekly during April–September under specified weather conditions; 5 m wide recording band; typically 26 counts/year; routes sampled to reflect habitat/management types and remain fixed year to year.
- Weather and timing constraints: observations between 10:45 and 15:45; conditions require dry weather, Beaufort wind <5, and temperature thresholds depending on sunshine.
- Single-species transects: follow all-species methods but recorded only during a few weeks for the focal species.
- Timed counts and egg/larval web counts: conducted for particular species under defined time/area conditions.
- Wider Countryside Butterfly Survey (WCBS): established 2009 to sample broader habitats with reduced effort; two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per site year vs 26 for full transects; minimum two visits in July/August; spring visits encouraged.

## Data collection and governance
- Data recorded on standard forms and entered online via UKBMS MyData or the Transect Walker software.
- Data entry can be performed by the recorder or the regional transect coordinator; each regional coordinator aggregates data for their region.
- Online data and Transect Walker files are uploaded to an Oracle database containing all records.

## Analytical methods
- Two national index approaches by species group:
  - Wider countryside species: use all survey data in a two-stage model. Stage 1 applies a generalized additive model (GAM) to estimate the annual seasonal flight pattern; values are normalised to a consistent seasonal pattern across sites but varying by year. Stage 2 fits a model to the full annual counts with seasonal values as an offset to estimate annual abundance changes.
  - Habitat specialists and regular migrants: with sparser WCBS data and more reduced-effort methods, a GAM imputes missing values and computes a site index; a log-linear regression combines site indices to derive a national Collated Index (LCI). Indices are updated annually as new data are incorporated.
- Collated Indices (LCI) are calculated for species recorded at five or more sites per year; prior years’ indices may be revised as new data are added.
- Species groups:
  - Wider countryside species: mobile, across diverse habitats.
  - Habitat specialists: low mobility, mainly in semi-natural habitats.
  - Regular migrants: do not overwinter in the UK.
- Early years may lack Collated Indices due to insufficient data, resulting in shorter series for some species.

## Data products and units
- Site indices: relative measures of population size, not absolute counts; reflect proportional abundance and vary by species.
- Collated Indices: presented as log10 of the Collated Index (LCI); scaled so the average index over the series equals 2, enabling relative comparisons over time.

## Quality control and data integrity
- Automated checks in Transect Walker flag potential data entry errors (e.g., unusually high counts or records outside flight periods).
- Regional coordinators validate data; ongoing checks occur online throughout the season.
- Further validation includes queries for records out of known distribution ranges, outside normal flight periods, first-time site records, and extreme or anomalous counts.

## Data structure and metadata
- Collated Indices stored as CSV files.
- Key columns in the dataset:
  - Species (scientific name per Fauna Europaea v2.2)
  - Common name (per Emmet & Heath)
  - Year
  - No. Sites (number of sites contributing to the Collated Index for that year)
  - Collated Index
  - Time period (data used to produce the Collated Indices)

- The dataset documents data provenance and references, with prior methodological details in cited literature (e.g., Dennis et al. 2013; Rothery & Roy 2001; Moss & Pollard 1993).