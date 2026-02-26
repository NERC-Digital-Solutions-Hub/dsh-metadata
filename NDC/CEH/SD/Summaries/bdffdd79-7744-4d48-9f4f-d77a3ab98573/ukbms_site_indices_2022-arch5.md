# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with substantial contributions from volunteers.
- It provides annual data on butterfly population status from a large-scale, site-based monitoring program, spanning since 1976 and involving over 3,000 actively recorded sites per year.
- The scheme uses multiple sampling frameworks:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m band, 26 counts per year (weekly from April to September).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, 2–3 visits per year.
  - Targeted surveys: single-species transects and other methods (timed counts, egg/larval web counts) focused on specific species.
- Data from all methods are analyzed together to produce population indices used for biodiversity policy questions.

## Data collected and trend analysis

- The dataset uses abundance indices (relative measures) rather than absolute counts, reflecting the proportion of butterflies detected at a site, which varies by species.
- Site indices are combined into species-wide collated indices using the Generalised Abundance Index (GAI) method (2016), with site-year weighting based on the proportion of the species’ flight period surveyed.
- Counts from Pollard walks, reduced surveys, and WCBS are used to model seasonal patterns and fill gaps in recording, with weighting giving observed data greater influence than extrapolated data.

## Quality control

- Field data are recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker, before upload to a central database.
- Automatic checks flag potential data errors (e.g., unusually high counts, records outside known flight periods); regional transect coordinators perform ongoing validation.
- Additional automated and manual validations assess records against known distributions, flight periods, first-time site records, and abnormal counts; data corrections are made through queries and coordinator input.

## Details of this data download

- Provides annual indices of abundance for each species at each UK site with sufficient data, for 1976–2022, in CSV format.
- Key columns:
  - SITE_CODE: unique site identifier
  - COUNTRY: regional data source for the collated index
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per updated Agassiz et al.)
  - COMMON_NAME: common name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year (a value of -2 indicates insufficient monitoring to compute an index)
- Taxonomic references are provided for species naming (Agassiz et al. updates).

## Licence and attribution

- Data are provided under the Open Government Licence (OGL), permitting free use with limited conditions.
- Users must include the citation with the DOI in any reported research using the data and provide the required attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS Partners offer assistance with dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conferences, or posters resulting from UKBMS data.
- Contact persons:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org