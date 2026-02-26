# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute the data.
- Purpose: annual data on butterfly population status across the UK, used to understand population changes and inform biodiversity policy.
- Run since 1976 with data from over 2500 actively recorded sites each year; data from all sampling methods are analyzed together.

## How the data are collected (sampling framework)

- Standard butterfly transects (Pollard walks): fixed-route transects (typically 2–4 km) surveyed weekly for up to 26 counts/year; record all species within a fixed-width band (about 5 m).
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (minimum 2 visits in July/August; spring visits encouraged).
- Targeted surveys: single-species transects; alternative methods for specific species (e.g., timed counts, egg/larval web counts).
- Data sources include common habitats and wide geographic coverage across the UK.

## Nature of the data and trend analysis

- Outputs are abundance indices (relative measures) rather than absolute population sizes. Site indices reflect a consistent proportion of butterflies present per site; detectability varies by species.
- Indices are aggregated to species-level collated indices using the Generalised Abundance Index (GAI) method (2016) with a weighting adjustment by the proportion of the species flight period surveyed at each site/year.
- All counts from Pollard walks, reduced surveys, and WCBS are used to model seasonal counts and extrapolate for gaps; weighting emphasizes observed data over extrapolated data.

## Quality control

- Field data are collected on standard forms and entered online via the UKBMS data entry site or Transect Walker; uploaded to a central database.
- Automated checks flag potential errors (e.g., unusually high counts, records outside flight periods); records can be adjusted.
- Regional transect coordinators validate data and monitor records throughout the season.
- Further automated/manual validation checks screen for misrecords (out of distribution ranges, out of flight period, first-time site records, unusual abundances). Corrections are made through queries and coordination with coordinators/recorders.

## Details of this data download

- Contains annual collated indices of abundance for UK butterfly species with sufficient data from 1976–2021 (some early years limited by data availability).
- Format: CSV file with columns:
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (per updated checklists)
  - COMMON NAME: vernacular name
  - YEAR: year of the collated index
  - NO. SITES: number of contributing sites
  - COLLATED INDEX: log10 of the collated index; scaled so the series average is 2
  - YEAR RANK: year-specific rank for the collated index (1 = best year)
  - TIME PERIOD: period of data used for the index
  - COUNTRY: country data source for regional indices
- Note: indices are relative measures rather than absolute population sizes.

## Licence and attribution

- Data are provided under an Open Government Licence (OGL) for free use and reuse with few conditions.
- Attribution: include the citation details and the provided DOI in any publication or report using the data.
- Attribution statement to include with derived data/images: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS Partners can advise on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conference presentations, or posters.
- Contact:
  - Marc Botham, UKBMS (ukbms@ceh.ac.uk)
  - Butterfly Conservation Transect Co-ordinator (transect@butterfly-conservation.org)

## GIS considerations for map-based use

- Data provide species-specific collated indices across multiple sites and years, suitable for temporal and spatial trend mapping.
- Useful for creating UK-wide and regional maps of abundance trends, with site-level context and country/region attribution.
- Can be joined with site polygons or 1 km square grids (WCBS) to visualize spatial distribution and changes over time.
- Be mindful of the relative nature of indices and differing flight periods when interpreting spatial patterns.