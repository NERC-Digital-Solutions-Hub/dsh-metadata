# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data; the scheme has monitored butterfly population changes in the UK since 1976.
- Data are collected through a combination of site-based monitoring across three sampling frameworks:
  - Standard butterfly transects (Pollard walks): fixed-route transects 2–4 km long, with weekly counts (up to 26 visits) from April to September at ~2000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (minimum 2 visits in July/August); ~800 squares sampled annually.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species.
- The UKBMS integrates data from all methods to monitor changes in butterfly populations and to inform biodiversity status and policy questions. More details are available at UKBMS website.

## Nature of data collected (phenology and metrics)

- Phenology data track timing of adult butterfly flight periods (imago stage) on UKBMS transects.
- Data-derived metrics include:
  - First and last recorded dates per site/year for a species.
  - Peak date and peak count.
  - Flight period length (days between first and last observation).
  - Mean flight date (weighted mean date) and standard deviation (SD) to assess synchrony.
  - Flight period range (duration between first and last day of flight).
- Constraints:
  - Phenology can be calculated reliably only from standard transects with weekly counts during the main flight season.
  - Some species have multiple generations (multivoltine) or overwintering life stages, requiring differentiated metrics where possible.
  - For eleven multivoltine species, separate first and second flight periods are provided; for some uni-voltine species (Brimstone, Peacock), separate first and second flight periods are also reported.
  - For species where generation separation is not reliable due to overlapping flight periods, data are reported for the entire flight period.
- The dataset supports analyses of timing, duration, and synchrony of butterfly flight periods across sites and years.

## Quality control and validation

- Data collection involves field-recording on standard forms, then online entry (via UKBMS MyData or Transect Walker) and uploading to a central database.
- Automated checks in the data entry system flag potential errors (e.g., abnormally high counts, records outside known flight periods).
- Regional transect coordinators review records for their sites and conduct ongoing validation during the season.
- Additional automated and manual validation checks screen for:
  - Records outside known distribution ranges (cross-checked with Butterflies for the Millennium data and UKBMS data).
  - Records outside normal flight periods.
  - First-time records at a site.
  - Abnormally high or atypical abundances.
- Data corrections are made via queries and coordination with transect coordinators or recorders; edits are reflected in the main UKBMS dataset.

## Details of this data download (CSV format and fields)

- The download provides phenology data for all species across all sites and years with sufficient data, in a comma-separated value (.csv) file.
- For 13 species, data may be available for the entire flight period and, where possible, for two distinct flight periods within each year at each site. For all other species, data cover the entire flight season only.
- Columns described in the dataset:
  - SITENO: unique site number within UKBMS
  - SITENAME: site name
  - GRIDREF: OS grid reference for the site (typically 6-figure)
  - SPECIES_NAME: binomial scientific name (Fauna Europaea)
  - COMMON_NAME: vernacular name (as per standard references)
  - YEAR: year of the phenology metric
  - NUMBER_OF_BROODS: number of distinct flight periods recorded for the species
  - BROOD: which flight period data represent (0 = entire flight period; 1 = first brood; 2 = second brood)
  - FIRSTDAY: day number after 1 April of first record in the brood
  - LASTDAY: day number after 1 April of last record in the brood
  - PEAKDAY: day number after 1 April of peak count
  - PEAKCOUNT: peak count value
  - MEAN_FLIGHT_DATE: weighted mean day number after 1 April for the brood
  - FLIGHTPERIOD_SD: standard deviation around the mean flight date
  - FLIGHTPERIOD_RANGE: number of days between firstday and lastday
- BROOD interpretation:
  - 0 = entire flight period (first to last record for the site/year)
  - 1 = first flight period (e.g., first generation or post-overwintering emergence)
  - 2 = second flight period (subsequent generations or post-first-generation events)

## Licence and attribution

- Data are provided under the Open Government Licence (OGL), permitting free use and reuse with minimal conditions.
- Citations, including the dataset DOI, must be included in any publications using the data.
- Attribution statement to be included with any information or images derived from the data: Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right (Butterfly Conservation, CEH, BTO, JNCC).

## Collaboration and contact details

- UKBMS Partners offer guidance on dataset use and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in scientific publications, conference presentations, or posters resulting from UKBMS data.
- Contacts:
  - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org