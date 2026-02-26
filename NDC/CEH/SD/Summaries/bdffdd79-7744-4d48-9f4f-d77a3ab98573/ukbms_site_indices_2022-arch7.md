# 1. About the UK Butterfly Monitoring Scheme

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- It provides annual, site-based monitoring data on butterfly population status to understand changes and support biodiversity policy questions.
- Since 1976, the scheme has tracked changes with over 3000 actively recorded sites each year, combining data from multiple sampling methods.

## Data collection framework
- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide band, record all species weekly (up to 26 counts/year) from April to September; weather conditions suitable for butterflies.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares; two parallel transects per square, 1 km long, 2–3 visits per year (minimum two in July/August; spring visits encouraged).
- Targeted surveys: single-species transects and other methods (e.g., timed counts, egg/larval web counts) focusing on specific species or life stages.
- Geographic and temporal scope: data cover site-level locations across the UK with long-running, multi-method observation streams.

## Nature of data collected and trend analysis
- Data are used to create abundance indices (relative measures of population size) rather than absolute counts.
- Site indices reflect a constant proportion of butterflies present; detectability varies by species.
- Indices for species are produced by combining site indices using the Generalised Abundance Index (GAI) with 2016 updates, including weighting by the proportion of the species flight period surveyed at each site/year.
- All counts from Pollard walks, reduced surveys, and WCBS are used to estimate seasonal patterns and extrapolate to account for recording gaps; weighting emphasizes observed data over extrapolated data.

## Quality control
- Field data are collected on standard forms and entered online via the UKBMS data entry site or Transect Walker; uploaded to a central database.
- Automated checks flag improbable entries (e.g., unusually high counts, records outside known flight periods); coordinators review and may prompt corrections.
- Regional transect coordinators validate data throughout the season; additional automated and manual validation checks include distribution-range checks, flight-period checks, first-site records, and unusual abundances.
- Corrections are made through queries and discussions with coordinators or recorders, ensuring data integrity.

## Details of this data download
- Provides annual abundance indices (site- and species-specific) for all UK sites with sufficient data from 1976–2022.
- File format: CSV.
- Key columns:
  - SITE_CODE: unique site identifier
  - COUNTRY: country/region used to derive regional collated indices
  - SPECIES_CODE: unique species identifier
  - SPECIES: scientific name (per Agassiz et al. updates)
  - COMMON_NAME: vernacular name
  - YEAR: year of the collated index
  - SITE_INDEX: abundance index for the species at the site and year; -2 indicates insufficient monitoring for that site-year
- Notes on data: indices are relative measures intended for trend analysis and comparative mapping.

## Licence and attribution
- Open Government Licence (OGL) applies, enabling free use with few conditions.
- Required: citation with DOI as listed in metadata when describing research using the data.
- Attribution statement to accompany derived information/images: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details
- UKBMS Partners offer advisory support and interpretation of outputs; opportunities for co-authorship and intellectual contribution to publications, conferences, or posters.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org