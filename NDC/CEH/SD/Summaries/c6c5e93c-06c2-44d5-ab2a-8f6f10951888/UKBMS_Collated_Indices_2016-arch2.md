# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- Collects data from over 2,000 sites per year across the UK.
- Uses standardized methods to monitor butterfly abundance and derive trends.
- Data include all-species transects, single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).
- Data are recorded in the field, entered online or via Transect Walker, and stored in an Oracle database.
- Outputs include site indices and national Collated Indices used to assess environmental health and policy performance over time.

## Data collection methods
- All-species transects (Pollard walk): fixed-route, 2–4 km, weekly counts (April–September), 26 counts/year; routes fixed for year-to-year comparability; weather- and time-of-day constraints.
- Single-species transects: follow all-species methodology but recorded only for focal species during selected weeks.
- Timed counts: abundance of a focal species recorded for a set period within a defined area; weather constraints apply.
- Egg/larval web counts: count eggs or larval webs for species in suitable habitat.
- Wider Countryside Butterfly Survey (WCBS): introduced in 2009 for broader habitats; two parallel 1-km transects in randomly chosen 1-km squares; 2–4 visits per year, with July/August emphasis.
- Data entry: field forms, online entry at ukbms.org/mydata, or Transect Walker software; regional transect coordinators aggregate and submit data; data uploaded to an Oracle database.

## Analytical methods
- Two national index approaches:
  - Wider countryside species: uses all counts across survey types in a two-stage model. Stage 1 uses a generalised additive model to estimate annual seasonal flight patterns; Stage 2 uses counts with seasonal values as an offset to estimate annual abundance changes. Method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants: insufficient WCBS data and reliance on reduced-effort sampling lead to GAM-based imputation to derive site indices; site indices are combined via a log-linear regression to produce a Collated Index. Collated Indices are updated annually as new data arrive; calculated for species recorded at five or more sites per year.
- Output units:
  - Site index: relative, not absolute, population size; proportional to actual population with species-dependent detectability.
  - Collated Indices: presented as Log10 Collated Index (LCI); scaled so the average index over the series equals 2 for relative comparisons over time.
- Species definitions:
  - Wider countryside species: mobile across many habitats.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK, arrive annually.

## Data quality and outputs
- Quality control:
  - Automatic checks in Transect Walker flag unusual counts or out-of-season records.
  - Regional coastal coordinators verify records; continuous validation during the season.
  - Further automated/manual validation checks for out-of-range records, out-of-distribution range, first-time site records, and extreme or unusual counts.
- Data formats:
  - Collated Indices stored as CSVs with columns: Species, Common name, Year, No. Sites, Collated Index, Time period.
  - Names standardized to Fauna Europaea (scientific names) and recognized common names.

## Data interpretation and caveats
- Collated Indices and site indices are relative measures and depend on sampling coverage and detection probabilities.
- Some early years lack Collated Indices due to insufficient data, resulting in shorter trend series for certain species.
- Indices are updated as new data are integrated, which can slightly modify past trend estimates.