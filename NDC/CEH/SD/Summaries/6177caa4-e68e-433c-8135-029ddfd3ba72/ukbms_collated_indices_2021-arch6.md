# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers provide the data, enabling long-term monitoring of butterfly populations in the UK.
- Purpose: derive annual population status data to understand changes in butterflies and inform biodiversity policy questions.

## Data collection framework

- Pollard walks: standard fixed-route transects (2–4 km) across sites, recording all butterflies in a 5 m wide band weekly from April to September (up to 26 counts per year). ~2000 sites sampled annually.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects; 2–3 visits per year (minimum 2 visits in July/August; spring visits encouraged). ~800 squares sampled annually.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species or life stages.

## Data processing and trend analysis

- Data are transformed into abundance indices, which are relative measures of population size rather than absolute counts.
- Site indices are combined into species-wide collated indices using the Generalised Abundance Index (GAI) method (2016), with a weighting adjustment based on the proportion of the species’ flight period surveyed each year at each site.
- The method uses counts from all sampling methods to model the seasonal pattern and extrapolate counts to account for gaps, with observed data given greater influence than extrapolated data.

## Quality control

- Field data are collected on standard forms and entered online (UKBMS data entry site) or via Transect Walker; data are uploaded to a central database.
- Automatic checks flag anomalies (e.g., unusually high counts, records outside known flight periods); regional transect coordinators perform ongoing reviews.
- Additional automated and manual validation checks screen for records outside known distribution, atypical flight periods, first-time site records, and extreme abundances; edits are made as needed in the main dataset.

## Data download details

- This download provides annual collated indices for each species in the UK with sufficient data, covering 1976–2021 (some early years excluded due to limited data).
- Format: comma-separated values (CSV).
- Key columns:
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - NO. SITES: number of contributing sites
  - COLLATED INDEX: log10 of the Collated Index (LCI), scaled so the average over the series equals 2
  - YEAR RANK: year-based rank of the CI for the species
  - TIME PERIOD: data period used to build the CI
  - COUNTRY: country data source for regional indices
- Note: Indices are relative measures of population size.

## Licence and attribution

- Open Government Licence (OGL) – free use with minimal conditions.
- When using the data in publications, include the citation with the DOI as specified in the metadata record.
- Attribution statement to include with derived information or images: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS Partners offer advisory support on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input for publications, conferences, or posters arising from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect Co-ordinator, transect@butterfly-conservation.org