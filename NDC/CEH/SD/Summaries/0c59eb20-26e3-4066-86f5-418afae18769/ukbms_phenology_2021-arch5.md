# About the UK Butterfly Monitoring Scheme

- Overview and governance
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - Volunteers contribute data; the dataset supports understanding population trends and informing biodiversity policy.
  - Data are collected under a structured sampling framework and analyzed collectively to produce national trends.

- Data collection methods
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m width, weekly counts from April to September (ideally 26 counts/year), ~2000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits/year (minimum 2 visits in July/August), ~800 squares/year.
  - Targeted surveys: Single-species transects, timed counts, and egg/larval web counts or other methods focusing on specific species.
  - All data from different methods are analyzed together to assess butterfly population changes.

- Nature of data collected (phenology)
  - Focus on butterfly flight period timing (adult, imago stage) across sites and years.
  - Phenology metrics include: first/last recording dates, date of peak counts, duration of flight period, mean flight date, and the standard deviation around mean flight date to capture synchrony.
  - For multi-voltine species, data may be split into first and second flight periods; for uni-voltine species with overwintering, two distinct flight periods may be reported.
  - Limitations: incomplete weekly coverage and the April 1–September 30 recording window can affect accuracy for some species; additional metrics are provided to mitigate these limitations.

- Quality control and data validation
  - Field data collected on standard forms, entered online via the UKBMS data entry site or Transect Walker, then uploaded to a central database.
  - Automated checks flag unusual counts and records outside known flight periods; regional transect coordinators perform ongoing manual checks.
  - Further automated/manual validation includes cross-referencing distributions, flight periods, and site-specific trends; data edits are made as needed.

- Details of this data download (format and schema)
  - Contains phenology data for all species, all sites, and all years with sufficient data.
  - Provided as a CSV file; thirteen species may have separate data for two flight periods; others have data for the entire flight season.
  - Key columns include:
    - SITENO, SITENAME, GRIDREF
    - SPECIES_NAME, COMMON_NAME
    - YEAR
    - NUMBER_OF_BROODS, BROOD
    - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
    - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

- Licence and attribution
  - Open Government Licence (OGL) for use and reuse with few conditions.
  - Proper citation with the provided DOI in any publications using the data.
  - Attribution statement to include with derived information or images: Contains UKBMS data © Butterfly Conservation, UKCEH, BTO, and JNCC.

- Collaboration and contact details
  - UKBMS partners offer guidance and interpretation assistance; potential for co-authorship and intellectual input in publications resulting from UKBMS data.
  - Contacts:
    - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
    - Butterfly Conservation: Transect Co-ordinator (transect@butterfly-conservation.org)