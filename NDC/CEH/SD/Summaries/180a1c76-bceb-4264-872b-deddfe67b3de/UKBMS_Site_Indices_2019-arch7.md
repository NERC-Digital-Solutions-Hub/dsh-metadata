# About the UK Butterfly Monitoring Scheme

- Purpose and audience
  - Annual data on butterfly population status derived from a large site-based monitoring program.
  - Data used to understand insect population changes and address biodiversity policy questions.
  - Coordinated by Butterfly Conservation, CEH, BTO, and JNCC; relies on a large base of volunteers.
  - In the UK, the scheme has monitored butterfly abundance since 1976 with over 2,500 active sites each year.
- GIS-relevant context
  - Data are suitable for map-based analyses of spatial patterns and trends by site, species, and year.
  - Includes both fixed-site transects and spatially sampled squares (WCBS) with different spatial resolutions (sites vs 1 km squares).

## Sampling framework and data collection methods

- Standard butterfly transects (Pollard walks)
  - Fixed-route 2–4 km transects; record all butterflies in a fixed-width band (about 5 m).
  - Weekly counts from April to September; up to 26 counts/year.
  - Approximately 2,000 sites sampled annually.
- Wider Countryside Butterfly Survey (WCBS)
  - Stratified-random 1 km square sampling; two parallel 1 km transects per square.
  - 2–3 visits/year (minimum 2 visits in July/August; spring visits encouraged).
  - ~750 squares sampled per year.
- Targeted surveys
  - Single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) targeting specific species.
  - Focused recording during main flight periods; may use non-transect methods.

## Nature of data and trend analysis

- Data products
  - Abundance indices are generated (relative measures of population size) rather than absolute counts.
  - Site indices reflect a relatively stable proportion of butterflies present; detectability varies by species.
- Aggregation and modelling
  - Collated species indices across sites and years produced using the Generalised Abundance Index (GAI) with 2016 modification.
  - Data-weighting in the final stage accounts for the proportion of the species’ flight period surveyed at each site-year.
  - All counts across a season (Pollard walks, WCBS, reduced surveys) inform the seasonal pattern and extrapolation to gaps, with weighting favoring observed data.

## Quality control

- Data capture and entry
  - Field forms; online entry via UKBMS site or Transect Walker; uploaded to a central database.
- Automated and manual checks
  - Automatic checks flag unusual counts or records outside flight periods.
  - Regional transect coordinators review data; additional validation done for species range, flight period, first-time site records, and anomalous abundances.
  - Data corrections and edits performed through queries and coordination with recorders.

## Details of this data download

- Timeframe and format
  - Annual indices of abundance for each species at each UK site with sufficient data, 1976–2019.
  - Provided as a comma-separated value (.csv) file.
- Column descriptions
  - SITE CODE: unique site identifier
  - COUNTRY: region supplying the regional collated index
  - SPECIES CODE: unique code per species
  - SPECIES: scientific name (Fauna Europaea)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - SITE INDEX: abundance index for the species at the site and year; -2 indicates insufficient data to compute an accurate site index

## Licence and attribution statement

- Licence
  - Open Government Licence (OGL) for free use and reuse with few conditions.
- Citation and attribution
  - Include the dataset citation and DOI in any publications using the data.
  - Attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.