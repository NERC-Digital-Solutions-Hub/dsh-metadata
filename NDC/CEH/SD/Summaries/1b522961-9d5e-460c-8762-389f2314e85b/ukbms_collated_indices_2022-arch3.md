# About the UK Butterfly Monitoring Scheme

- Overview
  - Organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - Aims to provide annual data on butterfly population status from a large-scale, site-based monitoring program to inform policy questions on biodiversity status and trends.
  - In operation since 1976, with over 3,000 actively recorded sites per year; data from all sampling methods are analyzed together.

- Data collection and sampling framework
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts (April–September), ~26 counts/year at each site.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel transects per square, 2–3 visits/year (minimum 2 in July/August), ~800 squares/year.
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on specific species or flight periods.
  - Data are combined across methods to produce species abundance indices rather than absolute counts; indices reflect a constant proportion of true population size, with some species detection bias.

- Data processing and trend analysis
  - Use abundance indices derived from counts along transects and sites; indices are relative measures.
  - Collated indices for each species produced with Generalised Abundance Index (GAI) method (2016) plus weighting by the proportion of the flight period surveyed each year at each site.
  - All counts in a season are used to model seasonal patterns and extrapolate to account for recording gaps; observed data are given greater influence through weighting.

- Quality control and data governance
  - Field data captured on standard forms, entered online via the UKBMS data entry site or Transect Walker.
  - Automatic checks flag potential errors (e.g., unusually high counts, records outside flight periods); regional coordinators validate records.
  - Additional automated/manual validation checks for out-of-range records, new site records, extreme abundances, and distribution consistency; edits made in the master dataset as needed.

- Data download details
  - Data cover 1976–2022 for species with sufficient data; some early years may lack collated indices for certain species.
  - Format: comma-separated values (CSV).
  - Key columns: SPECIES_CODE, SPECIES (scientific name), COMMON_NAME, YEAR, N_SITES, COLLATED_INDEX (log10, scaled so the series average equals 2), YEAR_RANK, TIME_PERIOD, COUNTRY.
  - COLLATED_INDEX is a relative index enabling comparison of population size over time.

- Licence and attribution
  - Open Government Licence (OGL) with wide use rights; attribution required.
  - Citation details (including DOI) must be included in references where the data are used.
  - Attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact
  - UKBMS Partners offer advice on dataset details and interpretation of outputs.
  - Joint authorship or intellectual input into publications resulting from UKBMS data is welcome.
  - Contacts: Marc Botham (ukbms@ceh.ac.uk) and Butterfly Conservation transect co-ordinator (transect@butterfly-conservation.org).