# About the UK Butterfly Monitoring Scheme

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - Relies on volunteers; provides annual, site-based butterfly population data and wider 1km-square sampling.
  - Aims to understand population changes and inform biodiversity policy; data are integrated from multiple components to produce species-level trends. Over 2,500 active sites recorded each year.

- Data collection and structure
  - Sampling framework comprises:
    - Standard butterfly transects (Pollard walks): fixed routes, 2–4 km, 5 m wide strip, weekly counts from April to September (ideally 26 counts/year); ~2,000 sites sampled annually.
    - Reduced effort surveys: single-species transects, or alternative methods (timed counts; egg/larval web counts) focusing on specific species or life stages.
    - Wider Countryside Butterfly Survey (WCBS): stratified-random 1km squares with two parallel 1-km transects; 2–4 visits per year (minimum two in July/August).
  - Spatial coverage:
    - Site-based transects for local indices.
    - WCBS covers ~750 squares per year; combined results provide broad UK coverage.
  - Temporal coverage:
    - Monitoring since 1976; annual data published for each year.
  - Data characteristics:
    - Abundance indices are relative measures (not absolute counts).
    - Site indices are combined into species-level collated indices using the Generalised Abundance Index (GAI) with weighting by the proportion of the flight period surveyed.

- Data processing and quality control
  - Field data collection on standard forms; entered online via UKBMS MyData or Transect Walker.
  - Data validation:
    - Automatic checks for entry errors and improbable values.
    - Regional transect coordinators validate records; ongoing QA throughout the season.
    - Automated/manual checks for records outside known distributions, outside flight periods, novel site records, or extreme differences; edits made as needed.
  - Data integration uses counts from all components to model seasonal patterns and fill gaps, with observed data weighted more heavily than extrapolated data.

- Data download details (availability for GIS use)
  - Content: annual collated indices of abundance for each species with sufficient data (1976–2017; some early years excluded for some species due to insufficient data).
  - Format: CSV file.
  - Columns explained:
    - SPECIES CODE: unique species identifier
    - SPECIES: scientific name (Fauna Europaea)
    - COMMON NAME: vernacular name (Emmet & Heath)
    - YEAR: year of the collated index
    - NO. SITES: number of contributing sites
    - COLLATED INDEX: log10 of the collated index; scaled so mean equals 2 across the series
    - YEAR RANK: relative rank of CI within all years for the species (1 = best year)
    - TIME PERIOD: period used to produce the collated indices
    - COUNTRY: country data used for regional indices

- Licence and attribution
  - Data provided under Open Government Licence (OGL); allows reuse with conditions.
  - Citation/DOI requirements must be included in publications using the data.
  - Attribution statement to be included: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right Butterfly Conservation, the Centre for Ecology & Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee.”

- Collaboration and contact details
  - UKBMS Partners offer assistance with dataset interpretation and potential co-authorship.
  - Contacts:
    - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
    - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)