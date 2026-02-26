# About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- It relies on volunteers and has monitored butterfly population changes across the UK since 1976, with over 2,500 active sites annually.
- Data are used to understand insect population trends and inform biodiversity policy questions.

## Nature of data collected
- Sampling framework includes:
  - Standard butterfly transects (Pollard walks): fixed routes, weekly counts (up to 26 visits/year) across ~2–4 km, ~5 m wide transects spanning April–September.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits/year (plus encouraged spring visits).
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts).
- Data are aggregated from these methods for analysis of butterfly abundance and distribution.

## Phenology metrics
- Phenology refers to timing of life-history events (e.g., adult flight periods).
- Based on UKBMS transects, phenology metrics include:
  - First/last recording dates per site per year
  - Peak date and peak count
  - Flight period length (days between first and last record)
  - Mean flight date and standard deviation around mean date (to reflect synchronisation)
  - Flight period range (duration)
- Generation-specific data:
  - Multivoltine species: study may report first and second flight periods where separable
  - Univoltine species (e.g., Brimstone, Peacock): two distinct flight periods possible (post-winter emergence and summer)
- Some species require combining data across generations due to overlap; metrics may be presented for entire flight period when separation is not possible.

## Quality control
- Data collection on field forms; entered online via UKBMS data entry site or Transect Walker.
- Automatic checks flag implausible entries (e.g., unusually high counts, out-of-season records).
- Regional transect coordinators review data; continuous checks during the season.
- Further automated/manual validation screens for records outside known distributions, atypical abundances, or first-time site records.
- Corrections are made through queries and coordination with coordinators or recorders.

## Details of this data download
- Provides phenology data for all species in the UK at all sites/years with sufficient data, available as a CSV.
- For 13 species, data may include both entire flight period and separate first/second flight periods; for other species, data cover the entire flight season only.
- Column descriptions include:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME, COMMON_NAME
  - YEAR, NUMBER_OF_BROODS, BROOD
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

Notes on BROOD values:
- 0 = entire flight period
- 1 = first flight period
- 2 = second flight period
- (Two distinct flight periods apply to selected species; not all species have two periods.)

## Licence and attribution
- Data are provided under the Open Government Licence (OGL), permitting free use with minimal conditions.
- Include the citation with DOI in any outputs describing research using the data.
- Attribution statement to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS partners offer advisory support and interpretation assistance.
- Opportunities for co-authorship and intellectual input in publications and presentations.
- Contact:
  - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect Coordinator: transect@butterfly-conservation.org