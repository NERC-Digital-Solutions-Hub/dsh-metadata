# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: provide annual data on butterfly population status to understand changes in biodiversity and answer policy questions related to status and trends.
- History and scope: in operation since 1976, currently involving over 3,000 actively recorded sites each year.
- Data integration: combines multiple sampling methods into a single dataset to analyse trends across the UK.

## Sampling framework
- Standard butterfly transects (Pollard walks): fixed-route 2–4 km, 5 m wide, recording all species weekly from April to September (up to 26 counts/year); routes chosen by the recorder.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects subdivided into 10 sections; 2–3 visits/year (minimum 2 visits in July/August); focuses on common habitats such as farmland; about 800 squares sampled per year.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) conducted during the focal species’ flight period or in suitable habitats.

## Data and trend analysis
- Data products: abundance indices (relative measures) derived from counts rather than absolute population sizes.
- Index construction: site indices are combined into species-level collated indices using the Generalised Abundance Index (GAI) method (2016), with a modification weighting site data by the proportion of the species flight period surveyed that year.
- Use of data: counts from all methods (Pollard walks, reduced surveys, WCBS) to estimate seasonal counts and extrapolate gaps; weighting emphasizes observed data over extrapolated data.

## Quality control
- Data collection: field-recorded on standard forms, then entered online via the UKBMS data entry site or Transect Walker software and uploaded to a central database.
- Validation: automated checks and regional transect coordinators review data continually; additional automated and manual validation checks assess records for out-of-range distribution, out-of-period observations, first-time site records, and unusually high or divergent counts.
- Corrections: data entry errors corrected through queries and discussions with coordinators or recorders, with edits applied to the main UKBMS dataset.

## Data download format
- This data download provides annual species abundance indices at each site for 1976–2023.
- File format: comma-separated values (.csv).
- Key columns:
  - SITE_CODE: unique site identifier
  - COUNTRY: region contributing to the regional collated index
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per standard checklists)
  - COMMON_NAME: vernacular name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year; -2 indicates insufficient data to compute an index

## Licence and attribution
- License: Open Government Licence (OGL), enabling free use and reuse with few conditions.
- Citation: include the dataset citation/DOI in any reports or publications using the data.
- Attribution: include the statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.”

## Collaboration and contact details
- UKBMS Partners offer advisory support on dataset details and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conferences, or posters produced from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)