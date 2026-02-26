# About the UK Butterfly Monitoring Scheme

- The UKBMS is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with volunteer data contributors. It provides annual population data for butterflies across the UK to inform biodiversity status and trends and policy questions.
- It uses a multi-method sampling framework to cover spatial scales from site-based transects to stratified-random 1 km squares and targeted surveys, with data from over 3000 active sites annually.

## Data collection and spatial design

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects at a site; weekly counts along a fixed-width belt (about 5 m); up to 26 counts per year; typical season April–September.
  - By 2022, there are over 2000 standard transect sites.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km square sampling using the same transect methodology; 2–3 visits/year (minimum 2 visits in July/August); ~800 squares sampled annually.
- Targeted surveys: single-species transects or alternative methods such as timed counts and egg/larval web counts.
- Spatial data identifiers: SITENO (site ID), SITENAME, GRIDREF (1:50,000 to 6-figure accuracy grid reference for transect start), with WCBS using 1 km squares for spatial coverage.

## Phenology data and metrics

- Phenology here refers to timing of adult butterfly flight periods recorded on UKBMS transects.
- Phenology metrics derived from standard transects (weekly counts) include:
  - FIRSTDAY, LASTDAY: first and last observation days after April 1 each year.
  - PEAKDAY, PEAKCOUNT: day and count of the peak observation.
  - MEAN_FLIGHT_DATE: weighted mean day of flight activity for a species at a site per year.
  - FLIGHTPERIOD_SD: variation around the mean flight date.
  - FLIGHTPERIOD_RANGE: duration in days between FIRSTDAY and LASTDAY.
- Some metrics may be affected by incomplete weekly coverage or the April 1–September 30 recording window; alternative metrics (e.g., mean flight date and SD) are used to mitigate this.

## Quality control

- Field data are collected on standard forms, then entered online via the UKBMS data entry site or Transect Walker; data uploaded to a central database.
- Automated checks flag unusual counts or records outside known flight periods; options exist to adjust records.
- Regional transect coordinators verify data; ongoing checks during the season.
- Post-entry validation includes checks against known distributions, flight periods, and unusual abundance patterns; data corrections are made via queries and coordination with coordinators or recorders.

## Data download details

- This download provides phenology data for all species across all standard transect sites and all years with sufficient data.
- File format: CSV.
- Columns include:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME (binomial name per standard checklists)
  - COMMON_NAME
  - YEAR
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

## Licence and attribution

- Data are provided under an Open Government Licence (OGL) for free use and reuse with few conditions.
- Citation/DOI must be included in any reports describing research using the data.
- Attribution statement to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- The UKBMS partners offer advisory support and interpretation assistance; opportunities for co-authorship and intellectual input in publications resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation: transect@butterfly-conservation.org