# 1. About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee. It relies on volunteers and has monitored butterfly population changes across the UK since 1976, currently with over 2,500 active sites annually.
- The dataset supports understanding changes in insect populations and informing biodiversity policy questions. Data come from multiple sampling methods that are analyzed together.

## Data collection components

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, recorded weekly (ideally 26 counts per year) in a 5 m wide band, across almost 2,000 sites.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (minimum 2 visits in July/August); about 750 squares sampled annually.
- Targeted surveys: include single-species transects, timed counts, and egg/larval web counts; focused on specific species or life stages within suitable habitats.

## Nature of data and trend analysis

- UKBMS produces abundance indices (relative measures) rather than absolute population sizes. Site indices reflect a constant proportion of butterflies present, with detectability varying by species.
- Overall species indices (collated indices) are produced using the Generalised Abundance Index (GAI) method (developed 2016) with a weighting adjustment so data from each site contribute proportionally to the flight period surveyed that year.
- All seasonal counts across Pollard walks, WCBS, and reduced surveys are used to model the seasonal pattern and extrapolate to gaps, giving more weight to observed data than to extrapolated data.

## Quality control

- Data are collected on standard field forms and entered online via the UKBMS data entry site or Transect Walker software, then uploaded to a central database.
- Automatic checks flag potential errors (e.g., unusually high counts, species outside flight period). Regional transect coordinators perform ongoing validation.
- Further validation queries check distribution range (against BNMs and UKBMS data), flight period timing, first-time site records, and unusual abundances; corrections are made through data queries and coordinator input.

## Details of this data download

- This download contains annual abundance indices for each species at each site with sufficient data from 1976–2019.
- Data are provided as a CSV file with columns:
  - SITE CODE: unique site identifier
  - COUNTRY: region used to create the regional index
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (Fauna Europaea, v2.2)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - SITE INDEX: abundance index for the species at the site in that year; -2 indicates insufficient monitoring within the flight period to calculate an accurate site index

## Licence and attribution

- Data are provided under the Open Government Licence (OGL), enabling free use with few conditions.
- Reports/publications using the data must include the citation details and DOI as specified in the metadata record.
- Attribution statement to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, the Centre for Ecology & Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee.

## Offer of collaboration and contact details

- UKBMS partners offer consultancy on dataset details and interpretation of outputs.
- Potential for co-authorship and intellectual input in publications or presentations stemming from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect co-ordinator: transect@butterfly-conservation.org