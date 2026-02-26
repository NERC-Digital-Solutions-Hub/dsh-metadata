# About the UK Butterfly Monitoring Scheme

- What it is and who funds it
  - A UK-wide, long-running scheme organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - Recognizes and thanks volunteers for data contributions.
  - Purpose: monitor butterfly population status and trends to inform biodiversity policy questions.

- Data collection framework and scale
  - Site-based, annual sampling with multiple methods:
    - Standard butterfly transects (Pollard walks): fixed routes, 2–4 km, weekly counts (typical 26 visits/year) over broad habitat types.
    - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, 2–3 visits/year, focused on common habitats (e.g., farmland).
    - Targeted surveys: single-species transects and non-transect methods (e.g., timed counts, egg/larval web counts).
  - Since 1976, with over 3,000 actively recorded sites annually (as of recent years); data from all methods are analyzed together.
  - Sampling design includes both fixed-route and stratified-random approaches to cover diverse landscapes.

- Data structure and trend analysis
  - Outputs are abundance indices (relative measures) rather than absolute counts.
  - Collated indices per species use the Generalised Abundance Index (GAI) method (2016), with a site- and year-weighting scheme that emphasizes observed data proportional to the flight period coverage.
  - All counts across counts and surveys in a season are used to model seasonal patterns and fill gaps due to incomplete recording.

- Data quality control and governance
  - Field data recorded on standard forms, entered online via UKBMS data entry site or Transect Walker software, and uploaded to a central database.
  - Automatic checks flag anomalies (e.g., unusually high counts, records outside flight periods).
  - Regional transect coordinators review data; ongoing validation includes checks against species distributions, flight periods, first-time site records, and outlier abundances.
  - Corrections and edits are implemented through queries and coordinated discussions with coordinators or recorders.

- Data download specifics (scope and format)
  - Timeframe: annual collated indices for each species with sufficient data from 1976–2023 (some early years excluded for insufficient data).
  - File format: comma-separated values (.csv).
  - Key columns:
    - SPECIES_CODE: unique species code
    - SPECIES: scientific name
    - COMMON_NAME: vernacular name
    - YEAR: year of the collated index
    - N_SITES: number of contributing sites
    - COLLATED_INDEX: log10 of the Collated Index, scaled so the series average equals 2
    - YEAR_RANK: year rank in CI values for the species
    - TIME_PERIOD: data period used to build indices
    - COUNTRY: source country for regional indices
  - Data structure supports cross-year trend analysis and cross-site comparisons.

- Licence and attribution
  - Open Government Licence (OGL) for free use and reuse with few conditions.
  - Must include citation with DOI as specified in metadata when publishing research using the data.
  - Attribution statement to be included: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.

- Collaboration and contact
  - UKBMS partners offer advisory support on data use and interpretation.
  - Willing to contribute to co-authorship and intellectual input for publications, conferences, or posters.
  - Contacts:
    - Marc Botham, UKCEH: ukbms@ceh.ac.uk
    - Butterfly Conservation Transect Co-ordinator: transect@butterfly-conservation.org