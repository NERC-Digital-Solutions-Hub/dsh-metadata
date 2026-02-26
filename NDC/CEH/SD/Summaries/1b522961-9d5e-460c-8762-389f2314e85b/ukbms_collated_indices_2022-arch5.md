# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data, and the scheme has monitored butterfly populations across the UK since 1976, with over 3,000 active sites annually.
- Purpose: generate annual population status data to understand trends and support biodiversity policy questions.

## Data collection and sampling framework

- Standard butterfly transects (Pollard walks): fixed-route line transects (2–4 km) at sites chosen by recorders; all butterflies counted in a 5 m band; typically 26 counts per year (weekly April–September); weather conditions are suitable for butterfly activity.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects per square; 2–3 visits per year (minimum 2 visits in July/August); ~800 squares sampled annually to cover common habitats.
- Targeted surveys: single-species transects and other methods (timed counts, egg/larval web counts) for particular species or habitats.
- Data from all methods are combined in analyses to produce species-level abundance trends.

## Nature of the data and trend analysis

- Data are abundance indices (relative measures, not absolute counts) derived from counts across sites and methods.
- Collated indices for each species are produced using the Generalised Abundance Index (GAI) method (2016), with site-year weights reflecting the proportion of the species flight period surveyed at each site.
- The GAI-based method uses counts from all survey types to model seasonal patterns and extrapolate to account for missing data, with weighting emphasizing observed data over extrapolated data.

## Quality control and data validation

- Field data are recorded on standard forms and entered online (via UKBMS data entry site or Transect Walker) before uploading to a central database.
- Automated checks flag potential data entry errors (e.g., unusually high counts, records outside flight periods).
- Regional transect coordinators validate data continuously during the season; a series of automated and manual validation steps further check for out-of-range records, distribution issues, first-time site records, and abnormal abundances.
- Corrections are made through targeted queries and discussions with coordinators or recorders where needed.

## Details of this data download

- Provides annual collated indices of abundance for UK butterfly species with sufficient data from 1976–2022 (where data exist in the latest year of the series).
- Data format: CSV (.csv) with columns including:
  - SPECIES_CODE (unique identifier)
  - SPECIES (scientific name)
  - COMMON_NAME (vernacular name)
  - YEAR (year of the collated index)
  - N_SITES (number of contributing sites)
  - COLLATED_INDEX (log10 of the collated index; scaled so the series’ average equals 2)
  - YEAR_RANK (relative ranking of the year for the species)
  - TIME_PERIOD (period used to produce indices)
  - COUNTRY (country data used for regional indices)
- Notes: Some earlier years lack collated indices due to insufficient data.

## Licence and attribution

- Data are provided under an Open Government Licence (OGL) for free use and reuse with minimal conditions.
- Citations/DOI must be included in any reports/publications describing research using the data.
- Attribution statement: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset details and interpretation of outputs.
- Collaboration opportunities include co-authorship and intellectual input for scientific outputs.
- Contacts:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation Transect Co-ordinators: transect@butterfly-conservation.org