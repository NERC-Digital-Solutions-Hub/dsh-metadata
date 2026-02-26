# About the UK Butterfly Monitoring Scheme

- Purpose and governance: The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). It relies on volunteers to collect annual data on butterfly population status across the UK.
- Relevance for GIS: Produces spatially distributed, site- and species-specific abundance indices that support biodiversity status and trend analyses. Data are suitable for map-based visualization and spatial trend reporting.

## Data collection and structure

- Sampling framework:
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km) with recording across a 5 m wide band, weekly from April to September (up to 26 counts/year), at ~2000 sites annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km square transects with two parallel 1 km routes; 2–3 visits per year, focusing on common habitats, ~8050 squares/year.
  - Targeted surveys: single-species transects or alternative methods (e.g., timed counts, egg/larval web counts) for specific species.
- Data scope: Annual population indices derived from counts across all sampling methods; UKBMS has operated since 1976 with over 2500 actively recorded sites yearly.
- Data standardization: Species names follow standardized checklists; methods integrate data from different survey types for overall species indices.

## Data processing and trend analysis

- Indices: Abundance indices are relative measures representing the proportion of butterflies observed, not absolute counts.
- Index calculation: Use Generalised Abundance Index (GAI) method (2016) with a site- and year-weighting approach that accounts for the proportion of the species flight period surveyed at each site/year.
- Data integration: All counts from Pollard walks, reduced surveys, and WCBS are used to model seasonal counts and extrapolate where data are incomplete; weighting prioritizes observed data over extrapolated data.
- Temporal coverage: Indices summarized for each species at each site and year, enabling regional and national trend analyses.

## Quality control

- Field data capture: Standard recording forms; data entered online via the UKBMS data entry site or Transect Walker software.
- Automated checks: Immediate validation in data entry system and Transect Walker to flag unusual counts or out-of-period records.
- Regional validation: Regional transect coordinators review data for questionable records; ongoing validation throughout the season.
- Further checks: Automated and manual validation for distributions, flight periods, first-time site records, extreme or anomalous abundances; corrections made via queries and coordination with recorders.

## Data download details

- Format and content: Annual indices of abundance for each species at each site with sufficient data, covering 1976–2021, provided as a CSV file.
- Key columns:
  - SITE CODE: unique site identifier
  - COUNTRY: region-specific data source for regional collated indices
  - SPECIES CODE: unique species code
  - SPECIES: scientific name
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - SITE INDEX: abundance index for the species at the site and year (value -2 indicates insufficient monitoring within flight period for that year)
- Data scope: Includes multiple survey methods merged into annual site-by-species indices.

## Licence and attribution

- Licence: Open Government Licence (OGL), allowing free use and reuse with few conditions.
- Citation: Include the dataset citation (DOI) as provided in metadata in any reports/publications using the data.
- Attribution: Include statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, UKCEH, BTO, JNCC” with derived information or images.

## Collaboration and contacts

- Offer: UKBMS partners offer dataset guidance, interpretation assistance, and potential co-authorship or intellectual input for publications.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org