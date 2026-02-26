# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 2,000 sites annually across the UK to monitor environmental health and policy-relevant trends.
- Data are gathered via standardized methods, primarily fixed-route transects (Pollard walks) that allow year-to-year comparisons, alongside reduced-effort methods for specific contexts.
- Outputs include site-level indices and national Collated Indices that track population trends over time.
- Data and outputs are stored within a central system and uploaded to appropriate portals for wider access and use by monitoring organisations.

## Data Collection Methods
- All-species transects: fixed-route line transects (2–4 km) along which all butterflies are recorded in a 5 m wide band each week from early April to late September (ideally 26 counts/year). Transects are chosen to sample habitat/management and must remain fixed across years.
- Transect timing and conditions: surveys occur between 10:45 and 15:45 under defined weather conditions suitable for butterfly activity (e.g., dry, wind < Beaufort 5, and specific temperature/sun conditions).
- Single-species transects: identical methodology but only for weeks during the focal species’ flight period.
- Timed counts and egg/larval web counts: conduct species-specific counts in set areas or habitats during restricted periods.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in wider habitats (farmland, etc.), using two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per year.
- Data recording: field forms are used, with data entered online via UKBMS MyData or Transect Walker software; regional transect coordinators compile data and upload to an Oracle database.

## Analytical Methods
- Wider countryside species: use a two-stage model incorporating all seasonality data across survey types.
  - Stage 1: Generalized Additive Model (GAM) estimates the annual seasonal flight pattern for each species.
  - Stage 2: The seasonal values are used as an offset in a model fitted to the full annual counts to estimate yearly abundance changes, producing annual indices and trends.
  - This approach accounts for varying seasonality and uses all available counts.
- Habitat specialists and regular migrants: GAM-based imputation of missing values to create a site index, then aggregation across sites to produce a national Collated Index.
  - A log-linear regression model is used to estimate missing values and produce the Collated Index and trends.
- Collated Indices are updated annually as new data are incorporated; older years may adjust slightly as data are added.
- Site Type Definitions: Wider countryside species are mobile and occur across broad habitats; habitat specialists are less mobile and restricted to semi-natural habitats; regular migrants overwinter abroad but arrive annually in the UK.

## Nature and Units of Recorded Values
- Site indices provide a relative measure of population size (not absolute counts), proportional to the actual population and comparable across years.
- Collated Indices are presented as the logarithm (base 10) of the index (LCI) and are scaled so the average index over the full time series equals 2, enabling relative temporal comparisons.

## Quality Control
- In-field and online validation: automatic checks in Transect Walker flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional coordinators review data for questionable entries; continuous validation occurs throughout the season.
- Post-entry validation includes checks for misplacement outside known distribution, out-of-season records, first-time site records, and unusual abundances.
- Data products: Collated Indices are stored as CSV files with detailed column descriptions.

## Data Structure and Output
- Collated Indices are generated per species per year and include:
  - Species (scientific name, following Fauna Europaea)
  - Common name
  - Year
  - No. Sites (sites contributing to the Collated Index that year)
  - Collated Index (the national index for that species and year)
  - Time period (data used to produce the Collated Indices)
- Data quality and metadata are documented to reflect years with insufficient data and potential revisions as more data are received.

## Data Access and Use Considerations
- The underlying datasets are designed for broad accessibility to enable monitoring, policy assessment, and further analysis by researchers and managers.
- Acknowledges the ongoing potential to enhance data value by integrating UKBMS data with other environmental datasets and by improving access to underlying data sources.