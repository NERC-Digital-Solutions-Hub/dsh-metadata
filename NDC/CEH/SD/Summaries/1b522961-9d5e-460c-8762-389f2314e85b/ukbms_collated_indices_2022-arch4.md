# About the UK Butterfly Monitoring Scheme

- Purpose and scope
  - The UKBMS is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It provides annual, site-based data on butterfly population status to understand biodiversity trends and inform policy.
  - Since 1976, it has monitored changes across the UK with over 3,000 actively recorded sites each year.

- Data collection methods (sampling framework)
  - Standard butterfly transects (Pollard walks): fixed-route transects 2–4 km long, recording all butterflies along a 5 m band weekly from early April to late September (up to ~26 visits/year).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits/year to sample common habitats (farmland); ~800 squares sampled annually.
  - Targeted surveys: single-species transects and methods not using transects (e.g., timed counts, egg/larval web counts) focused on specific species during their flight period.

- Data processing and trend analysis
  - Use abundance indices (relative measures) derived from counts rather than absolute population sizes.
  - Site indices are combined into species-wide indices using the Generalised Abundance Index (GAI) with weighting to reflect the proportion of the flight period surveyed at each site/year.
  - All seasonal counts (Pollard walks, reduced surveys, WCBS) are used to model seasonal patterns and extrapolate for gaps; weighting emphasizes observed data over extrapolated data.

- Quality control and data stewardship
  - Field data are recorded on standard forms, then entered online or via Transect Walker before being uploaded to a central database.
  - Automated checks in the data entry system and Transect Walker flag potential errors (e.g., unusual counts, records outside flight periods).
  - Regional transect coordinators validate and review data, with ongoing checks throughout the season.
  - Additional automatic and manual validation flags are used (e.g., distributions, flight periods, new site records, anomalous abundances). Edits are made as needed after coordination with coordinators or recorders.

- Data download and metadata
  - The download provides annual collated indices of abundance for species with sufficient data from 1976–2022; available as a CSV file.
  - Columns include:
    - SPECIES_CODE: unique species code
    - SPECIES: scientific name
    - COMMON_NAME: vernacular name
    - YEAR: year of the collated index
    - N_SITES: number of contributing sites
    - COLLATED_INDEX: log10 of the collated index (scaled so the series average equals 2)
    - YEAR_RANK: rank of the year for that species
    - TIME_PERIOD, COUNTRY: regional time period and data source
  - Some early years lack collated indices due to insufficient data.

- Licence and attribution
  - Data are provided under an Open Government Licence (OGL) with few conditions.
  - Users must cite the dataset (including DOI) in publications and include the attribution: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, UKCEH, BTO, and JNCC.”

- Collaboration and contact
  - UKBMS partners offer advice on dataset details and interpretation of outputs.
  - Opportunities for co-authorship and intellectual input in publications, conferences, or posters.
  - Contacts: UKBMS team at ukbms@ceh.ac.uk and transect@butterfly-conservation.org.