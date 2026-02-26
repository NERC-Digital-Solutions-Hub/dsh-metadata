# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data, and the scheme has monitored butterfly population changes across the UK since 1976, with over 3,000 active sites annually.
- Data come from multiple sampling frameworks that are analyzed together to understand status and trends in biodiversity:
  - Standard butterfly transects (Pollard walks): fixed-route transects 2–4 km long, 5 m wide recording all butterflies weekly (up to 26 counts/year) from April to September.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits/year (minimum two in July/August), sampling common habitats like farmland.
  - Targeted surveys: single-species transects, alternative methods (e.g., timed counts, egg/larval web counts) focusing on particular species.
- The dataset supports understanding changes in insect populations and informs biodiversity policy questions.

## Nature of data collected and trend analysis

- UKBMS creates abundance indices (relative measures) for each species at each site; indices represent a constant proportion of the population, with some species more detectable than others.
- Site indices are combined into species-wide (collated) indices using the Generalised Abundance Index (GAI) method (developed 2016) with a weighting adjustment that upweights data from the portion of the flight period actually surveyed each year.
- The method uses all counts across the season to estimate the seasonal pattern and extrapolate for gaps, ensuring observed data have a greater influence on final indices than extrapolated data.

## Quality control

- Field data are collected on standard forms, entered online (UKBMS data entry site) or via Transect Walker, then uploaded to a central database.
- Automatic checks flag potential data-entry errors (e.g., abnormally high counts, records outside known flight periods).
- Regional transect coordinators review data for their sites; ongoing checks occur throughout the season.
- Additional automated/manual validation screens for records outside known distributions, outside flight periods, first-time site records, and unusually extreme abundances; corrections are made via queries and discussions with coordinators/recorders.

## Details of this data download

- The download provides annual abundance indices for each species at each site with sufficient data from 1976–2023 (CSV format).
- Columns:
  - SITE_CODE: unique site identifier
  - COUNTRY: region used to create regional collated index
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per standard checklists)
  - COMMON_NAME: common name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year; -2 indicates insufficient data within the flight period
- Taxonomic references follow Agassiz et al. checklists (2013, with updates through 2020).

## Licence and attribution statement

- Open Government Licence (OGL): free use with few conditions; citation of metadata DOI is required in any publications describing the data.
- Attribution: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset details and interpretation; possible co-authorship or intellectual input for scientific outputs.
- Contacts:
  - UKCEH: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)