# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: provide annual, site-based monitoring data on butterfly population status to inform policy questions related to biodiversity status and trends.
- History and scale: in operation since 1976, currently monitoring over 2,500 actively recorded sites each year.
- Data are analyzed across all sampling methods to produce an integrated dataset used to understand changes in insect populations and to support policy decisions.

## Data collection framework

- Sampling components:
  - Standard butterfly transects (Pollard walks): fixed-route transects at sites chosen by recorders, 2–4 km long, 5 m wide, weekly counts (up to 26 visits per year, April–Sept).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km square sampling, two parallel transects per square, 2–3 visits per year (minimum 2 visits in Jul/Aug), focused on common habitats like farmland; ~800 squares/year.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) for specific species.
- Objective: combine different sampling approaches to create a comprehensive, policy-relevant view of butterfly populations across the UK.

## Nature of data collected

- Phenology focus: timing of adult butterfly flight periods (imago stage) across sites and years.
- Metrics and interpretation:
  - Simple metrics: first/last recording dates, peak date, and duration of the flight period.
  - Alternative metrics to handle sampling limitations: mean flight date and the standard deviation around the mean to indicate synchrony.
  - Generational structure: most species have multiple generations; methods allow separation into first/second flight periods where possible, with species-specific limitations noted.
  - For some species (multivoltine or uni-voltine), data may cover entire flight periods or split into up to two distinct flight periods; for others, only the entire flight season is available.
- Data limitations: not all species generation splits are possible due to overlapping flight periods and sampling window constraints (April 1 – Sept 30).

## Quality control

- Data entry and validation:
  - Field data recorded on standard forms, entered online via UKBMS data entry site or Transect Walker software, then uploaded to a central database.
  - Automatic checks flag anomalies (e.g., unusually high counts, records outside known flight periods); coordinators can approve or adjust records.
  - Regional transect coordinators review data for questionable entries and perform ongoing checks during the season.
- Validation suite:
  - Automated and manual validation steps include checks against known species distributions (using Butterfly Conservation’s BNM data), flight periods, first-time site records, abnormal abundances, and site-specific patterns.
  - Corrections are made through queries and, if needed, direct edits to the UKBMS dataset after coordination with coordinators or recorders.

## Details of this data download

- Content: phenology data for all species in the UK across all sites and years with sufficient data.
- Format: comma-separated values (.csv).
- Special provisions:
  - For 13 species, data are available for the entire flight period and separately for two distinct flight periods within each year at each site (where possible).
  - For all other species, data are available for the entire flight season only.
- Column descriptions (highlights):
  - SITENO, SITENAME, GRIDREF: site identifiers, name, and grid reference.
  - SPECIES_NAME, COMMON_NAME: scientific and common names.
  - YEAR, NUMBER_OF_BROODS, BROOD: year and flight period information (entire period, first brood, second brood).
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT: timing and magnitude of observed flight activity.
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE: summarized phenology metrics and dispersion.
  
## Licence and attribution statement

- Open Government Licence (OGL): allows free use and reuse with minimal conditions.
- Provisions:
  - Include proper citation including the DOI in any reports or publications using the data.
  - Include the attribution: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS Partners offer advisory support on dataset details and interpretation of outputs.
- Collaboration: possible co-authorship and intellectual input for publications, conference presentations, or posters arising from UKBMS data.
- Contacts:
  - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation Transect Co-ordinator: transect@butterfly-conservation.org