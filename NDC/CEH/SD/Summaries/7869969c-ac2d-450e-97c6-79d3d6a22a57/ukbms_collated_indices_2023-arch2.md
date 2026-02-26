# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- It relies on volunteers and a long-running, site-based monitoring program to produce annual data on butterfly population status across the UK since 1976.
- The dataset informs policy-related questions about biodiversity status and trends and encompasses a broad sampling framework across multiple methods and habitats.

## Data collection and sampling framework

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide, recording all butterflies weekly (ideally 26 counts per year) across 2000+ sites by 2022.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (minimum two in July/August), about 800 squares sampled annually.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focusing on specific species or life stages.
- Sampling spans multiple years and methods are analyzed together to provide comprehensive trend data.

## Nature of data and trend analysis

- Data are summarized as abundance indices (relative, not absolute counts) to reflect population trends.
- Site indices represent stable proportional detection across the season; detectability varies by species.
- Collated indices (per species per year) are produced using the Generalised Abundance Index (GAI) with a weighting adjustment: site data are weighted by how much of the species’ flight period was surveyed that year.
- The GAI uses counts from all methods to model seasonal patterns and extrapolate to fill gaps, prioritizing observed data in the final index.

## Quality control

- Data captured on standard forms and entered online via the UKBMS data entry system or Transect Walker.
- Automatic checks alert for anomalies (e.g., implausible counts, records outside a species’ flight period).
- Regional transect coordinators validate data, with ongoing checks throughout the season.
- Additional automated and manual validation screens test distribution ranges, flight periods, first-time site records, and unusual abundances; corrections are implemented through queries and coordinate-driven edits.

## Details of this data download

- Provides annual collated indices of abundance for UK butterfly species with sufficient data from 1976–2023 (some early years lack indices due to insufficient data).
- Delivered as a CSV file.
- Columns include:
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name
  - COMMON_NAME: common name
  - YEAR: year of the collated index
  - N_SITES: number of contributing sites
  - COLLATED_INDEX: log10 of the collated index, scaled so the series average equals 2
  - YEAR_RANK: rank of the year’s index for the species
  - TIME_PERIOD, COUNTRY: metadata about data used for regional indices
- Taxonomy and naming follow established checklists and references.

## Licence and attribution

- Data are provided under the Open Government Licence (OGL).
- Users must include the specified citation with any reports or publications describing research using the data (including DOI).
- Attribution statement to include with any derived information or images: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer advisory support on dataset details and interpretation of outputs.
- Willing to contribute as co-authors or provide intellectual input for scientific outputs.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect coordinator, transect@butterfly-conservation.org