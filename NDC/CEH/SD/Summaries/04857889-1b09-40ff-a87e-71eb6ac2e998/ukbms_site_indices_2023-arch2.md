# About the UK Butterfly Monitoring Scheme

- Purpose and context
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It provides annual data on butterfly population status from a large-scale, site-based monitoring program, vital for understanding insect population changes and informing biodiversity policy.
  - Since 1976, the scheme has monitored changes across the United Kingdom, with over 3000 actively recorded sites each year.

- Monitoring framework and data sources
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide band, recording all species weekly (up to 26 counts/year) across habitat sections; weather conditions tailored for butterfly activity; >2000 sites monitored by 2022.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects; 2–3 visits/year (plus encouraged spring visits); ~800 squares sampled annually.
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts, focusing on specific species or alternative methods.
  - Data from all methods are analyzed together to produce unified trends.

- Data analysis and trend construction
  - Output is abundance indices (relative measures) rather than absolute population sizes.
  - Site indices reflect a stable proportion of butterflies present; detection varies by species.
  - Overall species indices (collated indices) are derived using the Generalised Abundance Index (GAI) method (2016) with a weighting adjustment based on the proportion of the flight period surveyed at each site/year.
  - The method uses counts from all sampling methods to model seasonal patterns and extrapolate to account for gaps, with observed data given greater weight.

- Quality control and data integrity
  - Field data are collected on standard forms, entered online (UKBMS data entry site) or via Transect Walker, and uploaded to a central database.
  - Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
  - Regional transect coordinators validate data; additional automated and manual validations screen for range, flight period, new site records, and aberrant abundances; corrections are made through queries and coordination with reporters.

- Data download details (scope and structure)
  - The download provides annual abundance indices for each species at each site with sufficient data, spanning 1976–2023, in CSV format.
  - Key columns:
    - SITE_CODE: unique site identifier
    - COUNTRY: country contributing to the regional index
    - SPECIES_CODE: unique species identifier
    - SPECIES: scientific name
    - COMMON_NAME: vernacular name
    - YEAR: year of the collated index
    - SITE_INDEX: abundance index for the species at the site and year (–2 indicates insufficient data for index calculation)

- Taxonomy and naming references
  - Species and common names follow established checklists and references (Agassiz et al. updates; Emmet & Heath for common names).

- Licence and attribution
  - Data are provided under the Open Government Licence (OGL), enabling free use with few conditions.
  - Attribution required: include the citation/DOI as specified in the metadata; include a statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.

- Collaboration and contact information
  - UKBMS partners welcome collaboration, interpretation support, and potential co-authorship for publications resulting from UKBMS data.
  - Contacts:
    - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
    - Butterfly Conservation, Transect Co-ordinator: transect@butterfly-conservation.org

- Key implications for environmental monitoring analysts
  - Standardized, long-running data framework enables consistent trend analysis and policy evaluation.
  - Open licensing and clear attribution facilitate data reuse and integration with other environmental datasets.
  - Robust QA/QC processes support data reliability and comparability across years, sites, and methods.
  - Detailed metadata and structured CSV output support reproducible analyses and cross-study synthesis.