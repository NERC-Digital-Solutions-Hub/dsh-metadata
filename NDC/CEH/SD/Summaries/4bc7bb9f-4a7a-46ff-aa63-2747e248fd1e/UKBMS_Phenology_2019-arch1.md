# About the UK Butterfly Monitoring Scheme

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - It relies on volunteers and long-running, site-based monitoring to track butterfly population status across the United Kingdom since 1976.
  - The dataset supports understanding changes in insect populations and informs biodiversity status and trends policy questions.
  - Over 2,500 actively recorded sites contribute data each year.

- Data collection framework
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km) recorded weekly (up to 26 counts/year) along a fixed width (≈5 m). About 2,000 sites are sampled annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (minimum 2 visits in July/August). Approximately 750 squares sampled per year.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species or life stages.

- Nature of the data (phenology)
  - Phenology refers to timing of adult butterfly flight periods and related life-history events.
  - Phenology metrics are derived from standard transects (weekly counts during the main activity season); WCBS data are not used for phenology calculation due to reduced sampling effort.
  - Metrics include: first/last recording dates, peak date/count, and flight period length.
  - Additional metrics used in other phenology studies: mean flight date (weighted), and standard deviation around the mean date (synchronisation of flight periods).
  - Some species have multiple generations; where possible, data are split into first and second flight periods. For bivoltine/multivoltine species, two separate flight-period measures may be provided; for some uni-Voltine species (Brimstone, Peacock), two distinct flight periods are possible due to spring and summer emergence.
  - Limitations: generation separation is constrained by difficulty in distinguishing overlapping flight periods; for many species, data represent the entire flight period.

- Quality control
  - Field data are collected on standard forms, then entered online (UKBMS data entry site) or via Transect Walker, before uploading to a central database.
  - Automated checks flag unusual counts or records outside known flight periods; regional coordinators perform ongoing validation.
  - Further automated/manual validation checks assess records outside known distribution, out-of-season records, first-time site records, atypical abundances, or unusual changes relative to site norms.
  - Data corrections are made through queries and consultations with coordinators or recorders as needed.

- Details of this data download (format and content)
  - Provides phenology data for all species across all sites/years with sufficient data, in a CSV (.csv) file.
  - For 13 species, data are available for the entire flight period and separately for two distinct flight periods per year at each site; for all other species, data are available for the entire flight season only.
  - Columns include:
    - SITENO: unique site number
    - SITENAME: site name
    - GRIDREF: OS grid reference for the site
    - SPECIES_NAME: scientific name (Fauna Europaea)
    - COMMON_NAME: vernacular name (EMMET & Heath)
    - YEAR: year of metric calculation
    - NUMBER_OF_BROODS: number of distinct flight periods used
    - BROOD: 0 = entire flight period; 1 = first flight period; 2 = second flight period
    - FIRSTDAY: day number after April 1 for first recording of the brood
    - LASTDAY: day number after April 1 for last recording of the brood
    - PEAKDAY: day of maximum count for the brood
    - PEAKCOUNT: maximum count for the brood
    - MEAN_FLIGHT_DATE: weighted mean day of flight for the brood
    - FLIGHTPERIOD_SD: standard deviation around the mean flight date
    - FLIGHTPERIOD_RANGE: days between first and last record of the brood

- Licence and attribution
  - Data are provided under the Open Government Licence (OGL), enabling free use with minimal conditions.
  - Citations and DOIs must be included in references for publications using the data.
  - Attribution statement: Contains UKBMS data © copyright and database rights held by Butterfly Conservation, UKCEH, BTO, and JNCC.

- Collaboration and contact
  - UKBMS partners offer advisory support and interpretation assistance.
  - Potential for co-authorship and intellectual input in scientific outputs.
  - Contact: UKBMS via UKCEH (Marc Botham, ukbms@ceh.ac.uk) or Butterfly Conservation (Transect coordinator, transect@butterfly-conservation.org).