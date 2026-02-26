# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers contributing data.
- Purpose: provide annual data on butterfly population status through a nationwide, site-based monitoring program to understand changes in insect populations and inform biodiversity policy.
- Scale: since 1976, with over 2500 actively recorded sites each year; data from all sampling methods are analyzed together.

## Data collection framework and components

- Standard butterfly transects (Pollard walks): fixed-route transects (typically 2–4 km) at sites chosen by recorders; weekly counts (up to 26 per year) from early April to end September; habitat-based sections; nearly 2000 sites sampled annually.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km square locations with two parallel 1 km transects; 2–3 visits per year (minimum two in July/August, spring visits encouraged); ~750 squares sampled per year.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focusing on particular species or life stages.
- Historical reference: Pollard & Yates (1993) described the standard methods.

## Nature of data collected (phenology)

- Focus: phenology data – timing of adult butterfly flight periods across sites and years.
- Suitable for phenology metrics only from standard transects with weekly counts during the main flight season.
- Metrics include:
  - First and last recorded dates per site/year per species
  - Peak date and peak count
  - Flight period length (last-first)
  - Mean flight date (weighted mean) and standard deviation around mean (measure of synchronisation)
  - For multi-voltine species, separate data for first and second flight periods where possible; for uni-voltine species (e.g., Brimstone, Peacock), two distinct flight periods may be reported (early-year and summer) in addition to the entire flight period
- Notes:
  - Some generations overlap, making separation imperfect; data include overall flight period measures and, where possible, separate first/second flight periods
  - Data limitations due to recording period (April 1 – September 30) and uneven weekly coverage across sites/years

## Quality control

- Field data recorded on standard forms, then entered online or via Transect Walker; uploaded to central database.
- Automatic checks warn about data entry errors (e.g., abnormally high counts, out-of-season records); coordinators review and may adjust records.
- Regional transect coordinators validate data throughout the season; additional automated and manual validation checks screen for:
  - Records outside known species distribution
  - Records outside normal flight period
  - First-time site records
  - Unusually high or unusual abundances
- Corrections are made through queries and coordination with recorders/coordinators where needed.

## Details of this data download

- Scope: phenology data for all species across all UK sites and years with sufficient data; available as a CSV (.csv) file.
- Data availability: for thirteen species, data can be provided for the entire flight period and separately for two distinct flight periods within each year at each site; for other species, data are available for the entire flight season only.
- Column descriptions:
  - SITENO: unique site number within UKBMS
  - SITENAME: site name
  - GRIDREF: OS grid reference for site (start of transect)
  - SPECIES_NAME: scientific name (Fauna Europaea, v2.2)
  - COMMON_NAME: vernacular name (as per standard references)
  - YEAR: year of phenology metric
  - NUMBER_OF_BROODS: number of distinct flight periods available for the species in that year/site
  - BROOD: flight period index (0 = entire flight period; 1 = first flight period; 2 = second flight period)
  - FIRSTDAY: day number after 1 April for first record of a given brood
  - LASTDAY: day number after 1 April for last record of a given brood
  - PEAKDAY: day number after 1 April of the peak count
  - PEAKCOUNT: peak count value
  - MEAN_FLIGHT_DATE: weighted mean day after 1 April for the given brood
  - FLIGHTPERIOD_SD: standard deviation around the mean flight date
  - FLIGHTPERIOD_RANGE: number of days between firstday and lastday
- BROOD values:
  - 0: entire flight period
  - 1: first flight period (first generation or post-overwintering adults)
  - 2: second flight period (subsequent generations or second generation in bi-voltine species)
- Data format: CSV for easy integration into data workflows

## Licence and attribution

- Licence: Open Government Licence (OGL) – allows free use with few conditions.
- Citation: include the dataset’s DOI/citation in any publications or reports that describe research using the data.
- Attribution statement: must be included with any information or images derived from the data:
  Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS Partners offer advisory support and interpretation of outputs; opportunities for co-authorship and input into publications, conferences, or posters.
- Contacts:
  - UK Centre for Ecology & Hydrology – Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation – Transect co-ordinator (transect@butterfly-conservation.org)