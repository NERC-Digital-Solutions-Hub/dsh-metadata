# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). It relies on volunteers and has collected butterfly population data across the UK since 1976, with over 3,000 active sites annually.
- Data are gathered through a mix of sampling methods and are used to understand biodiversity trends and inform policy.

## Data collection methods (GIS-relevant framework)

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide, weekly counts (up to 26 per year) from April to September.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1-km transects, 2–3 visits per year (minimum 2 visits in July/August).
- Targeted surveys: single-species transects, timed counts, egg/larval web counts.
- Spatial scope: UK-wide; standard transects >2,000 sites; WCBS ~800 squares per year.
- Data are harmonized across methods for analysis.

## Nature of data and trend analysis (GIS workflows)

- Data are used to create abundance indices (relative measures) rather than absolute counts.
- Site indices are combined into species-level collated indices using the Generalised Abundance Index (GAI) with weighting for the proportion of the flight period surveyed at each site/year.
- The seasonal pattern of counts is estimated from all counts in a season (Pollard walks, reduced surveys, WCBS) to account for gaps; observed data are weighted more heavily than extrapolated data.

## Quality control (data reliability for mapping)

- Field data are entered on standard forms and uploaded to the UKBMS database, with online checks via the data entry site and the Transect Walker tool.
- Regional transect coordinators review records for plausibility; automated and manual validation checks flag records outside known distribution, out-of-flight-period records, first-time site recordings, extreme values, or anomalous site-year data.
- Corrections are applied through queries and edits to the main UKBMS dataset as needed.

## Details of this data download (GIS data structure)

- Contents: annual abundance indices for each species at each site with sufficient data, covering 1976–2023.
- Format: CSV text file.
- Columns:
  - SITE_CODE: unique site identifier
  - COUNTRY: country associated with the regional collated index
  - SPECIES_CODE: unique species code
  - SPECIES: scientific name (per Agassiz et al. updates)
  - COMMON_NAME: vernacular name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year (−2 indicates insufficient monitoring to compute an index)
- Note: Taxonomic updates and standard references are provided in metadata.

## Licence and attribution (data use)

- Licence: Open Government Licence (OGL) – free use with few conditions.
- Attribution: include the citation with DOI as specified in the metadata, and the statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.

## Offer of collaboration and contact details (how GIS teams can engage)

- UKBMS Partners offer guidance on dataset interpretation and collaboration opportunities, including potential co-authorships for publications or presentations.
- Contacts:
  - UKCEH: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect coordinator, transect@butterfly-conservation.org