# About the UK Butterfly Monitoring Scheme

- A national, long-running program organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee. More than 2,500 sites are active each year, with data contributed by volunteers and coordinated to support biodiversity status and trends policy questions.

## Aim and scope
- Provides annual, site-based butterfly population status data across the UK since 1976.
- Integrates data from multiple components to generate regional and national trend indicators for policy relevant insights.
- Data are used to understand changes in insect populations and to inform biodiversity status and trend questions.

## Data collection framework
- Standard butterfly transects (Pollard walks): fixed-route surveys 2–4 km long, recorded weekly in a 5 m wide band, typically 26 counts per year, across almost 2,000 sites.
- Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts focusing on specific species or habitats.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km square sampling with two parallel 1 km transects, 2–4 visits per site per year (750 squares annually), designed to better sample common habitats like farmland.
- All components feed into a unified UKBMS dataset, with results analyzed together.

## Nature of the data and trend analysis
- Data are abundance indices (relative measures) rather than absolute population sizes.
- Site indices are assumed to reflect a constant proportion of the population; detectability varies by species.
- Regional and species indices are produced using the Generalised Abundance Index (GAI) method (2016), with site-level year weighting based on the proportion of the species flight period surveyed.
- GAI uses all counts within a season to estimate the seasonal pattern and extrapolate missing observations, weighting observed data more heavily than extrapolated data.

## Quality control
- Field data recorded on standard forms, then entered online or via Transect Walker; uploaded to a central database.
- Automated checks flag outliers or records outside known flight periods; regional coordinators validate data continually during the season.
- Further automated/manual validation screens for out-of-range distributions, atypical flight periods, new site records, extreme or unusual abundances. Data edits are discussed with coordinators or recorders before updating the main dataset.

## Details of this data download
- Contains annual abundance indices for each species at each UK site with sufficient data from 1976–2018.
- Data format: CSV with columns:
  - SITE CODE: unique site identifier
  - COUNTRY: regional origin for the index
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (Fauna Europaea)
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - SITE INDEX: abundance index for the species at the site and year (value -2 indicates insufficient data to compute an index)

## Licence and attribution
- Open Government Licence (OGL) allowing free use with minimal conditions.
- Must include citation details (DOI) as specified in metadata.
- Attribution statement: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners welcome collaboration, interpretation of outputs, and potential co-authorship.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)