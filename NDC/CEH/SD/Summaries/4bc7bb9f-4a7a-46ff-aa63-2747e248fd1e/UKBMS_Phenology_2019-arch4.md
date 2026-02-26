# About the UK Butterfly Monitoring Scheme

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organised and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - It relies on volunteers and has monitored butterfly population changes across the UK since 1976, with data from over 2,500 active sites annually.
  - Data from all sampling methods are analysed together and inform policy questions related to biodiversity status and trends.

- Data collection and components
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts (up to 26 visits/year) across habitats.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits/year (minimum 2 in July/August).
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts.
  - Data are collected across multiple methods and sites, with ongoing coordination and data integration.

- Phenology data and metrics
  - Phenology = timing of adult butterfly flight periods; data come from standard transects with weekly counts during the main activity season.
  - Key metrics include:
    - First and last recording dates per site per year per brood
    - Peak date and peak count
    - Flight period length (days between first and last record)
  - Additional metrics used to accommodate incomplete sampling include:
    - Mean flight date (weighted mean date)
    - Flight period standard deviation (SD) around the mean date
  - Generation-specific data:
    - For many multivoltine species, data can be split into first and second flight periods; for uni-voltine species (e.g., Brimstone, Peacock) two distinct flight periods are documented.
  - Limitations:
    - Some species have overlapping generations or limited separation capacity; for these, phenology measures are presented for the entire flight period.

- Quality control and data validation
  - Field recording on standard forms, then online entry via UKBMS data entry site or Transect Walker.
  - Automatic checks flag unusual counts or records outside known flight periods; regional transect coordinators perform ongoing review.
  - Additional validation includes cross-checks for:
    - Records outside known distribution ranges
    - Records outside normal flight periods
    - First-time records at a site
    - Atypical abundances or large deviations from site norms
  - Data corrections are made through queries and collaboration with coordinators or recorders.

- Details of this data download (format and columns)
  - Phenology data for all species, sites, and years with sufficient data; provided as a CSV file.
  - For 13 species, data may include entire flight periods plus separate first/second flight periods; other species cover the entire flight season only.
  - Columns included:
    - SITENO, SITENAME, GRIDREF
    - SPECIES_NAME, COMMON_NAME
    - YEAR, NUMBER_OF_BROODS, BROOD
    - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
    - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

- Licence and attribution
  - Open Government Licence (OGL) for use and reuse with few conditions.
  - Proper citation including DOI must be included in publications using the data.
  - Attribution statement: Contains UKBMS data © copyright and database rights held by Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact details
  - UKBMS partners offer guidance and interpretation support; opportunities for co-authorship and intellectual input in publications or presentations.
  - Contacts:
    - Marc Botham, UKBMS, CEH: ukbms@ceh.ac.uk
    - Butterfly Conservation, Transect Co-ordinator: transect@butterfly-conservation.org