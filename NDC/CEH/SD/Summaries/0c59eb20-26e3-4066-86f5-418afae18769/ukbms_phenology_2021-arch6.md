# About the UK Butterfly Monitoring Scheme

## Overview
- Organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- Acknowledges volunteers; aims to monitor butterfly population status annually.
- Uses a wide-scale site-based sampling framework with multiple data collection methods.
- Data from all methods are analyzed together and the dataset supports biodiversity status and policy questions.
- Maintains a long-running program since 1976 with over 2500 active sites each year.

## Data components and sampling frameworks
- Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m width, weekly counts from early April to end September (up to 26 counts/year); ~2000 sites.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel 1 km transects subdivided into 10 sections; 2–3 visits per year (plus recommended July/August and some spring visits); ~800 squares/year.
- Targeted surveys: Single-species transects and alternative methods:
  - Timed counts (abundance over a set period/area for a species).
  - Egg and larval web counts (e.g., for Marsh Fritillary).
  - Focus on specific species during their flight periods.

## Nature of data collected (phenology)
- Phenology refers to timing of adult butterfly flight periods across years and sites.
- Data are derived from UKBMS transects with weekly counts during the main activity season.
- Metrics include:
  - First and last observation dates per site/year/brood.
  - Peak day and peak count.
  - Flight period length (days between first and last observation).
  - Mean flight date (weighted mean) and standard deviation (measure of synchronisation).
  - Flight period range (days between first and last day).
- For species with multiple generations (multivoltine) or two UK-univoltine groups (e.g., Brimstone, Peacock), data may be split into first and second flight periods where feasible.
- Limitations due to non-weekly sampling and a recording window from April 1 to September 30; for some species, separate-generation metrics may be constrained by data rather than biology.

## Quality control
- Field data recorded on standard forms and entered online via UKBMS MyData or Transect Walker.
- Automated checks flag improbable counts or records outside known flight periods; users may override or edit.
- Regional transect coordinators validate and review data, with ongoing checks throughout the season.
- Further automated and manual validation flags records outside known distribution, outside normal flight periods, first-time site records, and unusual abundances; corrections are made via queries and coordination with recorders as needed.

## Details of this data download
- Provides phenology data for all species in the UK at all sites and years with sufficient data.
- Delivered as a CSV (.csv) file.
- For thirteen species, data are available for the entire flight period and separately for two distinct flight periods where possible; for all other species, data cover the entire flight season only.
- Key columns:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME, COMMON_NAME
  - YEAR, NUMBER_OF_BROODS, BROOD
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

## Licence and attribution statement
- Available under the Open Government Licence (OGL).
- Requires citation with the dataset’s DOI in any reports or publications.
- Attribution to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, UKCEH, BTO, JNCC.

## Offer of collaboration and contact details
- UKBMS Partners can advise on dataset details and interpretation of outputs.
- Co-authorship and intellectual input in scientific outputs are welcome.
- Contact:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org