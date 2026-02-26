# UK Butterfly Monitoring Scheme (UKBMS) data download

## Overview of the UKBMS

- A collaborative, funded program by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- Relies on volunteers; aims to monitor butterfly population status across the UK since 1976.
- Sampling framework includes:
  - Standard butterfly transects (Pollard walks): weekly counts across long fixed routes at ~2000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with fewer visits.
  - Targeted surveys (single-species transects, timed counts, egg/larval web counts).
- Data are analyzed together to inform biodiversity status and trends; >2500 actively recorded sites annually.

## Nature of data collected

- Focuses on phenology: timing of adult butterfly flight periods on UKBMS transects.
- Phenology metrics include:
  - First and last recording dates at a site in a year.
  - Peak date and peak count.
  - Flight period length (days between first and last observation).
  - Mean flight date (weighted) and flight period standard deviation (SD).
  - Flight period range (duration between first and last day of recording for a brood).
- Special considerations:
  - Some metrics are limited by weekly survey gaps and the April 1–Sept 30 recording window.
  - Many species have multiple generations; metrics can be presented for entire flight periods or separated by first/second broods for certain species.
  - For 11 multivoltine species, first and second flight periods can be separated; two uni-voltine species (Brimstone and Peacock) may show two distinct flight periods due to overwintering.
  - For two univoltine species, data can be presented for both early and summer flight periods as well as the full period.

## Quality control

- Field data collected on standard forms and entered online (via UKBMS mydata or Transect Walker).
- Automated checks in data entry systems flag anomalies (e.g., unusually high counts, out-of-season records).
- Regional transect coordinators validate records; ongoing checks throughout the season.
- Further automated/manual validation compares records against known distributions, typical flight periods, and site-specific baselines.
- Corrections are made via queries and communications with coordinators or recorders.

## Details of this data download

- Content: phenology data for all species in the UK, across all sites and years with sufficient data.
- Format: comma-separated values (CSV).
- Key columns and meanings:
  - SITENO: site identifier; SITENAME; GRIDREF.
  - SPECIES_NAME: binomial scientific name; COMMON_NAME: vernacular name.
  - YEAR: year of the phenology metric.
  - NUMBER_OF_BROODS: number of distinct flight periods recorded for a species in a year/site.
  - BROOD: 0 = entire flight period; 1 = first brood; 2 = second brood.
  - FIRSTDAY, LASTDAY: day numbers after 1 April of first/last recording for the brood.
  - PEAKDAY, PEAKCOUNT: day and count of the flight period peak.
  - MEAN_FLIGHT_DATE: weighted mean day number after 1 April for the brood.
  - FLIGHTPERIOD_SD: standard deviation around the mean flight date.
  - FLIGHTPERIOD_RANGE: days between first and last recording for the brood.
- Special coverage:
  - Thirteen species have data available for both the entire flight period and separate first/second broods, where possible.
  - For other species, data are available for the entire flight season only.

## Licence and attribution

- Licensed under the Open Government Licence (OGL); allows free use and reuse with few conditions.
- Must include citation details (DOI) in any reports or publications describing research using the data.
- Attribution statement required with any information or images derived from the data: Contains UKBMS data © copyright and database right for Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners can advise on dataset details and interpretation of outputs.
- Collaboration opportunities include co-authorship and intellectual input for publications, conferences, or posters resulting from UKBMS data.
- Contacts:
  - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect Co-ordinator: transect@butterfly-conservation.org