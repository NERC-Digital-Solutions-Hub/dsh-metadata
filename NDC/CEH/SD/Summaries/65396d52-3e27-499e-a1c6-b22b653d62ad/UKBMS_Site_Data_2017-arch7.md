# UK Butterfly Monitoring Scheme

## Overview
- A national program organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology (CEH), British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- Involves volunteers collecting annual population data for butterflies across the UK.
- Data are used to understand insect population changes and inform biodiversity policy.
- Data collection began in 1976 and currently covers more than 2,500 sites annually.

## Data and methods
- Sampling framework comprises three components:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m observation band, weekly counts from April–September; ~26 counts/year at ~2,000 sites.
  - Reduced effort surveys: single-species transects or alternative methods (timed counts, egg/larval web counts).
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel transects per square, 2–4 visits per year (minimum 2 in July/August); ~750 squares/year.
- Data are collected across site-based monitoring and 1 km squares; some methods focus on particular species.
- Data are combined across components for species-level analyses.

## Data and trend analysis
- Uses abundance indices (relative measures) rather than absolute population sizes.
- Site indices reflect a constant proportion of butterflies present; some species are detected more readily than others.
- Trend indices for species are produced using the Generalised Abundance Index (GAI) with year/site-weighting based on the proportion of the species flight period surveyed.
- Counts from all components are used to estimate seasonal patterns and extrapolate gaps, with weighting favoring observed data.

## Quality control
- Field data recorded on standard forms; entered online via UKBMS data entry site or Transect Walker software.
- Automatic checks flag unlikely values, activities outside known flight periods, etc.
- Regional transect coordinators review data; ongoing validation includes checks against distribution ranges, flight periods, first-time site records, and abnormal abundances.
- Edits to the main UKBMS dataset are made after validation and discussion with coordinators or recorders.

## Details of this data download
- Provides location and attribute data for UK butterfly monitoring sites from 1976–2017; sensitive sites excluded.
- Data format: CSV.
- Key columns include:
  - Site number, Site name, Gridreference, Easting, Northing
  - Length (transect length), Country, No. Sections
  - No. Yrs surveyed, First year surveyed, Last year surveyed
  - Survey type (UKBMS standard transect or WCBS)

## Licence and attribution
- Open Government Licence (OGL) for reuse with few conditions.
- Requires citation with the dataset’s DOI in any publications using the data.
- Attribution statement: Contains UKBMS data © Butterfly Conservation, CEH, BTO, JNCC.
- Since 2017, data submitters have agreed to OGL; noted potential restrictions on historic data if concerns arise.

## Collaboration and contact details
- UKBMS partners offer collaboration and interpretation support; opportunities for co-authorship on publications.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - CEH: Marc Botham (ukbms@ceh.ac.uk)

## GIS considerations for use
- Spatial data are in UK coordinate frameworks (grid references, easting/northing) suitable for conversion to standard GIS projections (e.g., OS grid to WGS84).
- Useful for creating map-based products: site density, transect coverage, WCBS sampling intensity, and temporal trends by year and site.
- Data can be joined with habitat layers, land-use data, and other biodiversity datasets to analyze spatial patterns and drivers.
- Limitations to consider: sensitive-site exclusions, varying data collection methods over time, and the open-data licensing terms for attribution.