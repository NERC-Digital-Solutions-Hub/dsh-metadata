# About the UK Butterfly Monitoring Scheme

## Overview
- A UK-wide, volunteer-driven program organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- Since 1976, provides annual site-based population data for butterflies; currently monitors over 3,000 active sites each year.
- Data come from three sampling components:
  - Standard butterfly transects (Pollard walks) monitored weekly (up to 26 times/year).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, 2–3 visits/year.
  - Targeted surveys (single-species transects, timed counts, egg/larval web counts) for specific species.
- Data are aggregated across all methods to support biodiversity status and policy questions.

## Nature of data and spatial/temporal coverage
- Data are abundance indices (relative measures of population size) rather than absolute counts.
- Indices are derived using a Generalised Abundance Index (GAI) method (2016), with site-year weighting based on the proportion of the species flight period surveyed.
- All counts from a season (Pollard walks, WCBS, other surveys) are used to model seasonal patterns and extrapolate gaps; weighting emphasizes observed data over extrapolated data.
- Temporal coverage: 1976–2022 (site-level data up to 2022); broad spatial coverage across the UK.
- Data for sensitive sites are excluded from the download.

## Data download specifics for GIS use
- Provides location and attribute data for UK sites monitored under UKBMS.
- Format: CSV (.csv).
- Key columns:
  - Site_number: unique site identifier
  - Site_name: transect location name
  - Gridreference: central 6-figure OS grid reference for transect route
  - Easting: x-coordinate (grid reference)
  - Northing: y-coordinate (grid reference)
  - Length: transect length in metres (where available)
  - Country: UK country of the site
  - N_Sections: number of transect sections
  - N_Yrs_surveyed: years with butterfly counts at the site (up to 2022)
  - First_year_surveyed: first year of data collection at the site
  - Last_year_surveyed: most recent year of data (up to 2022)
  - Survey_type: UKBMS standard transect or WCBS
- Coverage:
  - 1976–2022 data for monitored sites
  - Excludes sensitive sites

## Quality control
- Field data collected on standard forms; entered online via UKBMS MyData or Transect Walker; uploaded to a central database.
- Automated checks in the entry system and Transect Walker flag potential errors (e.g., unusual counts, records outside flight periods).
- Regional transect coordinators perform ongoing validation; after preliminary checks, additional automated/manual validation screens out out-of-range or inconsistent records.
- Further edits may be made via queries in collaboration with coordinators or recorders.

## Licence and attribution
- Open Government Licence (OGL) for use and reuse with few conditions.
- Required: cite the dataset with the provided DOI per metadata; include the attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.
- Since 2017, submitters have agreed to OGL for data submission; historic data may have third-party IP restrictions; contact UKBMS if objections arise.

## Collaboration and contact details
- UKBMS Partners offer guidance and interpretation support; potential for co-authorships and intellectual input in publications, conferences, or posters using UKBMS data.
- Contacts:
  - Marc Botham, UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation Transect Co-ordinator: transect@butterfly-conservation.org

## GIS-specific considerations
- Data are geolocated at site level with precise grid references and transect lengths, enabling spatial mapping and spatial-temporal analyses.
- Multi-year data allow trend mapping and habitat-associated pattern analyses, with attention to varying resolutions and data coverage across methods and years.
- Data licensing and attribution requirements must be observed in any map-based products or GIS publications.