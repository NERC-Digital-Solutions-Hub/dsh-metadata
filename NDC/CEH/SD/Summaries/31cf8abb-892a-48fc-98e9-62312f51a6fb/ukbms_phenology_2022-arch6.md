# About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- It relies on volunteers and site-based monitoring to produce annual data on butterfly population status across the UK since 1976.
- Sampling components include:
  - Standard butterfly transects (Pollard walks) monitored weekly (up to 26 times/year)
  - Wider Countryside Butterfly Survey (WCBS) with stratified-random 1km squares, 2–3 visits/year
  - Targeted surveys (single-species transects, timed counts, egg/larval web counts)
- Data from all sampling methods are analyzed together.
- The dataset supports understanding insect population changes and biodiversity policy questions.
- >3000 active sites recorded each year; more details at UKBMS website.

## Nature of data collected
- Focus: phenology – timing of adult butterfly flight periods per year at each site.
- Phenology metrics include:
  - Dates of first and last record per site per year
  - Date and count of peak flight activity
  - Number of days between first and last record (flight period length)
  - Mean flight date and standard deviation (SD) around the mean (seasonal synchronisation)
  - Flight period range (days between first and last record)
- Data limitations:
  - Phenology can be calculated only from standard transects with weekly counts (not WCBS).
  - Many species have multiple generations; metrics may be split into first and second flight periods for certain multivoltine species and two uni-voltine species (Brimstone and Peacock) where applicable.
  - For some species, generations may overlap, limiting accurate separation.
- Taxonomic and generation handling notes are provided for several species and generations.

## Quality control
- Data workflow: field recording forms → online entry (UKBMS data entry site or Transect Walker) → database.
- Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review records; data undergo further automated and manual validation.
- Additional queries check for out-of-range distributions, first-time site records, and atypical abundances; edits are made as needed.

## Details of this data download
- Content: phenology data for all species, at all sites and years with sufficient data.
- Format: comma-separated values (CSV).
- Special handling: thirteen species have data for the entire flight period plus separate first/second flight periods; other species have data for the entire flight season only.
- Columns included and meanings:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME, COMMON_NAME
  - YEAR, NUMBER_OF_BROODS, BROOD
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE
- BROOD values:
  - 0 = entire flight period
  - 1 = first flight period (first generation or post-overwintering adults)
  - 2 = second flight period (subsequent generations or post-first-generation adults)
- FIRSTDAY/LASTDAY/PEAKDAY are day numbers after 1 April
- MEAN_FLIGHT_DATE is a weighted mean date; SD indicates synchronisation; range is days between first and last record
- Note: 13 species have both full-year and two-flight-period data where possible; others provide entire flight season only.
- Taxonomic notes reference Agassiz et al. checklists (2013/2019/2020).

## Licence and attribution statement
- Data available under an Open Government Licence (OGL) for free use and reuse with few conditions.
- Must include citation with DOI in any reports/publications using the data.
- Required attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners offer guidance on dataset interpretation and potential collaboration.
- Co-authorship and intellectual input into publications and presentations possible.
- Contact:
  - UKCEH: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)