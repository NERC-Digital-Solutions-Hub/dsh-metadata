# 1. About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers contributing data.
- Purpose: annual site-based monitoring to track butterfly population status across the UK; data support biodiversity status and policy questions.
- Sampling framework comprises three main components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects; record all species in a 5 m band weekly from April to September (up to ~26 counts/year); over 2,000 sites monitored yearly by 2022.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects; 2–3 visits per year (plus encouraged spring visits) to sample common habitats; ~800 squares sampled annually.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focusing on specific species or life stages.
- Data span: monitoring since 1976 with over 3,000 actively recorded sites each year; data from all methods are analyzed together.

## Nature of data collected and trend analysis

- Data are used to create abundance indices (relative measures) rather than absolute population sizes.
- Site indices reflect the proportion of butterflies observed, which varies by species in detectability.
- Overall species indices (collated indices) are produced using the Generalised Abundance Index (GAI) method, with site-year weighting based on the proportion of the flight period surveyed.
- The GAI uses all counts in a season (Pollard walks, reduced surveys, WCBS) to estimate seasonal patterns and extrapolate to account for gaps; observed data are weighted more heavily than extrapolated data.
- References to methodological publications underpin the approach.

## Quality control

- Field data are recorded on standard forms, then entered online (UKBMS data entry site) or via Transect Walker, before uploading to a central database.
- Automatic checks flag potential errors (e.g., abnormally high counts, records outside flight periods); regional transect coordinators perform ongoing validation.
- Further automated/manual validation checks include verification against known distributions, flight periods, new site records, and unusual abundances; edits are made as needed in the main dataset.

## Details of this data download

- Contains annual abundance indices for each species at each UK site with sufficient data, covering 1976–2023.
- File format: comma-separated values (CSV).
- Columns and meanings:
  - SITE_CODE: unique site identifier
  - COUNTRY: country contributing to the regional collated index
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per standardized checklists)
  - COMMON_NAME: vernacular name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year (use -2 if insufficient data to calculate an index)
- Taxonomic references provided for species nomenclature.

## Licence and attribution statement

- Data download is provided under the Open Government Licence (OGL), allowing free-use with few conditions.
- Attribution requirements:
  - Include the citation with DOI in any reports/publications using the data.
  - Include the attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS Partners offer advisory support on dataset interpretation and potential co-authorship or intellectual input for publications arising from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org