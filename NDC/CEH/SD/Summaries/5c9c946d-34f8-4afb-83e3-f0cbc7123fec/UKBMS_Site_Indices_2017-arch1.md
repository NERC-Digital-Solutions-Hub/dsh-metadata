# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: provide annual data on butterfly population status across the UK to support understanding of biodiversity trends and policy questions.

## Nature of data collected and trend analysis

- UKBMS collects abundance indices (relative measures, not absolute population sizes) across sites and years.
- Sampling framework components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m recording strip, weekly counts from April to September; ~26 counts/year at almost 2000 sites.
  - Reduced effort surveys: single-species transects, alternative methods, timed counts, egg/larval web counts.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel transects per square, 2–4 visits/year (minimum 2 visits in July/August); ~750 squares/year.
- Data synthesis: uses all counts (Pollard, reduced surveys, WCBS) to build seasonal abundance patterns and extrapolate counts to account for gaps; weighting favors observed data over extrapolated data.
- Trend estimation method: Generalised Abundance Index (GAI) with 2016 modification to weight site data by the proportion of the species flight period surveyed that year.
- Timeframe: monitoring since 1976; current effort includes ca. 2500 active sites annually.
- Outputs are used to answer policy questions about biodiversity status and trends.

## Quality control

- Data workflow: field forms -> online entry (via UKBMS MyData or Transect Walker) -> central database.
- Automated checks and validation:
  - Immediate data-entry checks for anomalies (e.g., unusually high counts, out-of-season records).
  - Regional transect coordinators validate and monitor records throughout the season.
  - Automated/manual queries for records outside known distributions, off-flight-period timing, first-time site records, extreme or unusual abundances.
- Corrections: edits are made after data queries and coordination with recorders/coordinators where necessary.

## Details of this data download

- Contents: annual abundance indices for each species at each well-sampled UK site, 1976–2017, provided as a CSV.
- Key columns described:
  - SITE CODE: unique site identifier
  - COUNTRY: region contributing to the regional index
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (Fauna Europaea)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - SITE INDEX: abundance index for the species at the site and year; -2 indicates insufficient data to compute an index
- Note: indices are relative measures designed to facilitate cross-site and cross-year comparisons.

## Licence and attribution statement

- Open Government Licence (OGL) for free use and reuse with minimal conditions.
- Must include citation details (including DOI) as specified in metadata records.
- Attribution: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset interpretation and potential co-authorship for scientific outputs.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology and Hydrology: Marc Botham (ukbms@ceh.ac.uk)