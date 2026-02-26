# 1. About the UK Butterfly Monitoring Scheme

- Purpose and organization: The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers. It provides annual population-status data for butterflies across the UK, used to address biodiversity status and trends for policy and decision-making. Since 1976, it has monitored changes across over 2,500 active sites each year.

- GIS-relevant data structure and sampling frameworks:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m wide, ~26 counts per year, at ~2,000 sites.
  - Reduced effort surveys: single-species transects or alternative methods (timed counts, egg/larval web counts) focusing on specific species.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1-km transects, 2–4 visits per year (minimum 2 in Jul/Aug), ~750 squares per year.
  - Data are spatially explicit at site level and across 1 km squares, enabling map-based analysis of spatial trends.

- Data types and trend analysis:
  - Abundance indices: relative measures derived from counts along transects and surveys, not absolute population sizes.
  - Collated indices per species use the Generalised Abundance Index (GAI) with weighting by the proportion of the flight period surveyed at each site/year, combining data from all components to estimate seasonal patterns and fill data gaps.

- Quality control and validation:
  - Field data captured on standard forms; online entry through UKBMS MyData or Transect Walker.
  - Automated checks flag anomalous counts or records outside known flight periods; regional coordinators review and validate.
  - Additional automated/manual validation ensures records fit known distributions and typical site/site-year patterns; corrections/improvements are incorporated into the main dataset.

- Details of this data download:
  - Provides annual site- and species-specific abundance indices for the UK for 1976–2018.
  - Delivered as a CSV with columns: SITE CODE, COUNTRY, SPECIES CODE, SPECIES (scientific name), COMMON NAME, YEAR, SITE INDEX (abundance index). If a site-year could not yield an accurate index, SITE INDEX may be -2.

- Licence and attribution:
  - Open Government Licence (OGL) for free use and reuse with minimal conditions.
  - Must include full citation with DOI where applicable.
  - Attribution statement required: Contains UKBMS data © Butterfly Conservation, CEH, BTO, JNCC.

- Collaboration and contact:
  - UKBMS partners offer guidance on dataset use and interpretation; opportunities for co-authorship on publications resulting from UKBMS data.
  - Contacts: Butterfly Conservation – Tom Brereton (tbrereton@butterfly-conservation.org); CEH – Marc Botham (ukbms@ceh.ac.uk).