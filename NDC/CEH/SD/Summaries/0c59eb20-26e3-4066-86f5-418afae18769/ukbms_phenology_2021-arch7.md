# UK Butterfly Monitoring Scheme phenology data download

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It relies on volunteers to collect annual population status data through a large-scale, site-based monitoring program.
  - Sampling frames include: standard Pollard transects (weekly, up to 26 visits), wider countryside transects (WCBS) in 1 km squares (2–3 visits), and targeted surveys for specific species.
  - The scheme has tracked butterfly abundance changes across the UK since 1976, with over 2,500 active sites each year.
  - Data from all sampling methods are analyzed together to inform biodiversity status and trends; more details at ukbms.org.

- Data collection methods
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km) with a 5 m wide recording band, typically 26 counts per year from April to September.
  - WCBS: stratified-random 1 km square locations with two parallel 1 km transects, 2–3 visits per year, designed to sample common habitats like farmland.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focusing on specific species.

- Nature of data collected
  - Phenology data capture timing of adult butterfly flight periods (imago stage) across transects.
  - Phenology metrics include first/last observation dates, peak date, peak count, and flight period duration.
  - Because of uneven weekly sampling and a season from April 1 to September 30, some metrics are limited to standard transects; alternative metrics (mean flight date and flight period SD) help address sampling biases.
  - For species with multiple generations (multivoltine) or two uni-voltine species (e.g., Brimstone, Peacock), data can be separated into first and second flight periods where possible.
  - Thirteen species have data split into two distinct flight periods; for all other species, data cover the entire flight season.

- Quality control
  - Field data are entered online or via Transect Walker, with automatic form checks for unusual counts or mis-timed records.
  - Regional transect coordinators review records and ongoing season validations.
  - Additional automated and manual validation checks flag records outside known distributions, outside flight periods, first-time site records, or anomalous abundances, with corrections made via queries and coordination with recorders.

- Details of this data download
  - Contains phenology data for all species across all sites and years with sufficient data.
  - Provided as a CSV file.
  - For thirteen species, data are available for the entire flight period plus separate data for two distinct flight periods per year; for others, data cover the entire flight season only.
  - Key columns include: SITENO, SITENAME, GRIDREF, SPECIES_NAME, COMMON_NAME, YEAR, NUMBER_OF_BROODS, BROOD, FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT, MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE.
  - Taxonomic references and standardization notes are included (Agassiz et al. and related checklists).

- Licence and attribution
  - Open Government Licence (OGL) permitting free use and reuse with few conditions.
  - Must include the citation with DOI in any reports or publications describing research using the data.
  - Attribution statement required: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact details
  - UKBMS Partners offer guidance on dataset interpretation and possible co-authorship or intellectual input for publications and presentations.
  - Contacts:
    - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
    - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org