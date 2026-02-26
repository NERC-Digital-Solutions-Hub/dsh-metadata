# About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology (CEH), British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
- It provides annual, site-based butterfly population status data across the UK since 1976.
- Data come from a large-scale network of over 2,500 active sites each year, spanning multiple sampling components.

## Data collection framework
- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects; 5 m wide recording band; counts from April to September; ~26 counts/year; nearly 2,000 sites sampled annually.
- Reduced effort surveys: single-species transects, timed counts, egg/larval web counts; focus on specific species or life stages.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects; 2–4 visits/year (minimum 2 visits in July/August); established 2009 to sample common habitats; ~750 squares/year.
- All components are combined to produce UKBMS results for trend analyses.

## Nature of data and trend analysis
- Data are used to create abundance indices (relative measures) rather than absolute counts.
- Site indices reflect a proportion of butterflies at a given site; some species are more detectable than others.
- Collated indices for each species are produced using the Generalised Abundance Index (GAI) with a weighting that accounts for the proportion of the flight period surveyed each year.
- Counts from all survey types are used to estimate seasonal patterns and fill gaps in observation data.

## Quality control
- Field data are captured on standard forms and entered online via the UKBMS data entry site or Transect Walker.
- Automated checks flag unusual counts or records outside known flight periods; regional coordinators review data, and ongoing validation occurs throughout the season.
- Additional automated/manual validation screens for out-of-range records, records outside known distribution, first-time site records, and anomalous abundances; corrections are made through data queries and edits.

## Details of this data download
- Content: annual collated indices of abundance for UK butterfly species with sufficient data, covering 1976–2018 (some earlier years lacked complete data for certain species).
- Format: CSV file.
- Columns include:
  - SPECIES CODE (unique species number)
  - SPECIES (scientific name per Fauna Europaea)
  - COMMON NAME (vernacular name)
  - YEAR (year of the collated index)
  - NO. SITES (number of sites contributing)
  - COLLATED INDEX (log10 of the collated index; scaled so the series average equals 2)
  - YEAR RANK (yearly rank of the CI for that species)
  - TIME PERIOD (data period used to generate the indices)
  - COUNTRY (regional data source)
- Purpose: enables historical trend analysis and cross-year comparisons.

## Licence and attribution statement
- Available under the Open Government Licence (OGL), permitting free use with minimal conditions.
- Must include the citation/DOI as specified in the metadata when used in publications.
- Attribution: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details
- UKBMS Partners offer guidance on dataset details and interpretation of outputs.
- Potential for co-authorship and intellectual input on publications and presentations.
- Contacts:
  - Tom Brereton (Butterfly Conservation): tbrereton@butterfly-conservation.org
  - Marc Botham (CEH): ukbms@ceh.ac.uk