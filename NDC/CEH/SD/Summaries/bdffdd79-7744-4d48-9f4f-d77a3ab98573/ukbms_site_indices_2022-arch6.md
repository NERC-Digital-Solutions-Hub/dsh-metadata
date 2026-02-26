# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC), with thanks to volunteers.
- Purpose: provide annual data on butterfly population status from a large, site-based monitoring program to understand trends and inform biodiversity policy.
- Scale: since 1976, the scheme has monitored changes across the UK with over 3,000 actively recorded sites each year; data from multiple sampling methods are analyzed together.

- Sampling framework (three components):
  - Standard butterfly transects (Pollard walks): fixed-route transects, 2–4 km, 26 counts per year, weekly during suitable conditions.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km square sampling, 2–3 visits per year, focused on common habitats.
  - Targeted surveys: single-species transects and non-transect methods (e.g., timed counts, egg/larval web counts).

- Data significance: the dataset comprises abundance indices (relative measures, not absolute counts) that relate to population trends; site indices combine to form overall species indices.

- Data processing and methods:
  - Generalised Abundance Index (GAI) approach (developed 2016) with weighting by the proportion of the flight period recorded each year, to produce collated species indices.
  - All counts across a season (Pollard walks, WCBS, and reduced surveys) are used to model seasonal patterns and extrapolate to account for gaps, with observed data given greater weight.

- Data quality control (QC):
  - Field recording on standard forms; online data entry via ukbms.org/mydata or Transect Walker; uploaded to a central database.
  - Automatic checks flag anomalous counts or records outside known flight periods.
  - Regional transect coordinators review data; additional automated/manual validation checks ensure records are within known distributions, flight periods, and site expectations.
  - Data corrections are made through queries and discussions with coordinators or recorders as needed.

- Details of this data download:
  - Contains annual site- and species-specific abundance indices for years with sufficient data from 1976 to 2022.
  - Delivered as a comma-separated values (CSV) file.
  - Key columns:
    - SITE_CODE: unique site identifier
    - COUNTRY: region contributing to the regional collated index
    - SPECIES_CODE: unique species identifier
    - SPECIES: scientific name
    - COMMON_NAME: common name
    - YEAR: year of the collated index
    - SITE_INDEX: abundance index for the species at that site and year; -2 indicates insufficient data to calculate an index

- Licence and attribution:
  - Open Government Licence (OGL) enabling free use and reuse with minimal conditions.
  - You must cite the dataset (including DOI) in any reports/publications describing research using the data.
  - Attribution statement to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right by Butterfly Conservation, CEH, BTO, and JNCC.

- Offer of collaboration and contact details:
  - UKBMS partners offer guidance on dataset use and interpretation, potential co-authorship, and intellectual input for publications, presentations, or posters.
  - Contact:
    - CEH: Marc Botham, ukbms@ceh.ac.uk
    - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org