# About the UK Butterfly Monitoring Scheme

## Overview
- Organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- Relies on volunteers; aims to provide annual data on butterfly population status across the UK.
- Data are derived from a wide-scale site-based monitoring program plus random 1km-square sampling; used to understand biodiversity trends and inform policy.
- Active since 1976, with over 2500 sites contributing each year.

## Data collection and components
- Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km), normally 26 counts per year across a 5 m width, weekly from April to September; ~2000 sites.
- Reduced effort surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on specific species or methods.
- Wider Countryside Butterfly Survey (WCBS): transect methodology with stratified-random 1 km squares; 2–4 visits per square per year (around 750 squares annually) to sample common habitats like farmland.
- Foundational references include Pollard & Yates (1993) and WCBS methodology.

## Nature of data collected and trend analysis
- Produces abundance indices (relative measures) rather than absolute counts.
- Site indices approximate a constant proportion of true population size; detectability varies by species.
- Collated indices are generated with the Generalised Abundance Index (GAI) method, with weighting to reflect the proportion of the flight period surveyed each year.
- All counts from Pollard walks, reduced surveys, and WCBS inform seasonal patterns; gaps are extrapolated, with observed data given more weight.

## Quality control
- Field data recorded on standard forms and entered online via UKBMS, or via Transect Walker software.
- Automatic checks flag anomalous entries; regional transect coordinators review data throughout the season.
- Additional automated and manual validation checks target out-of-range distributions, atypical flight periods, first site occurrences, and extreme or unusual counts.
- Any data corrections are coordinated with coordinators and recorded in the main dataset.

## Details of this data download
- Provides annual collated indices of abundance for species with sufficient data from 1976–2018; some early years may have missing indices due to data limitations.
- Delivered as a CSV file with columns:
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (Fauna Europaea)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - NO. SITES: number of contributing sites
  - COLLATED INDEX: log10 of the collated index; scaled so the average equals 2
  - YEAR RANK: ranking of CI within the species’ time series
  - TIME PERIOD: time period used for the collated index
  - COUNTRY: country used for regional indices

## Licence and attribution statement
- Open Government Licence (OGL) allowing free use/reuse with few conditions.
- Must include citation details (DOI) in reports/publications.
- Attribution to include: Contains UKBMS data © Butterfly Conservation, Centre for Ecology and Hydrology, British Trust for Ornithology, and Joint Nature Conservation Committee.

## Offer of collaboration and contact details
- UKBMS partners offer advice on dataset usage and help interpret outputs.
- Open to co-authorship and intellectual input for publications, conferences, or posters.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)