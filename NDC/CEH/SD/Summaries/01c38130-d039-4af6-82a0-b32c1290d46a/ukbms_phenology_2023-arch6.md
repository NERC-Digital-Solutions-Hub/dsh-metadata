# About the UK Butterfly Monitoring Scheme

## Overview and purpose
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- It relies on volunteers and provides annual data on butterfly population status across the UK.
- The dataset supports understanding insect population changes and informs biodiversity policy questions.
- Monitoring uses multiple sampling frameworks with site-based transects and surveys across broad geographies and habitats.

## Data collection methods
- Standard butterfly transects (Pollard walks): fixed-route transects, 2–4 km, weekly counts (up to 26 per year) along habitat-specific sections; typically over 2000 sites monitored yearly.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (July/August emphasis; spring visits encouraged) across around 800 squares annually.
- Targeted surveys: single-species transects, alternative methods like timed counts, and egg/larval web counts for specific species.
- All data types are analyzed together to assess butterfly population trends.

## Nature of the data and phenology
- Phenology focuses on timing of adult butterfly flight periods recorded on UKBMS transects.
- Phenology metrics include first/last recording dates, peak date/count, mean flight date, standard deviation around mean flight date (synchronisation), and flight period duration.
- Because WCBS and incomplete weekly coverage exist, some metrics may be biased for certain species or years; alternative phenology metrics are used to reduce sensitivity to sampling gaps.
- Simple metrics (FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT) may be affected by the April–September recording window.

## Quality control
- Field data are collected on standard forms and entered online (UKBMS MyData) or via Transect Walker; data then enter a central database.
- Automated checks flag unusual counts or records outside known flight periods; regional transect coordinators review data for questionable records.
- Additional automated/manual validation checks identify records outside species’ known distributions, out-of-season records, first-time appearances at sites, and atypical abundances; corrections are made via queries and coordinator/recorder consultations.

## Details of this data download
- This download provides phenology data for all species across all standard transect sites and years with sufficient data, as a CSV file.
- Key columns and definitions:
  - SITENO: unique site number
  - SITENAME: site name
  - GRIDREF: UK Ordnance Survey grid reference
  - SPECIES_NAME: scientific name (binomial)
  - COMMON_NAME: common name
  - YEAR: year of the phenology metric
  - FIRSTDAY: day number after April 1st of first observation
  - LASTDAY: day number after April 1st of last observation
  - PEAKDAY: day number after April 1st of peak count
  - PEAKCOUNT: peak count value
  - MEAN_FLIGHT_DATE: weighted mean day of flight across the season
  - FLIGHTPERIOD_SD: SD around the mean flight date
  - FLIGHTPERIOD_RANGE: days between firstday and lastday
- Taxonomic references: Agassiz et al. (2013, 2019, 2020) with updates to British Lepidoptera checklists.

## Licence and attribution
- Data are provided under the Open Government Licence (OGL), permitting open use with few conditions.
- Must include citation (including DOI) as specified in metadata in any reports/publications using the data.
- Attribution statement required: Contains UKBMS data © Butterfly Conservation, UKCEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners offer advisory support and interpretation of outputs.
- Potential for co-authorship and intellectual input in publications, conferences, and posters using UKBMS data.
- Contact:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation: transect@butterfly-conservation.org