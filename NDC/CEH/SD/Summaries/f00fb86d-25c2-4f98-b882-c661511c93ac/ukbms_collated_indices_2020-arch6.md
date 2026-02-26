# 1. About the UK Butterfly Monitoring Scheme

## Overview
- A collaborative, long-running program to monitor butterfly populations in the UK.
- Coordinated by Butterfly Conservation, UK Centre for Ecology & Hydrology (CEH), British Trust for Ornithology (BTO), and Joint Nature Conservation Committee (JNCC); relies on volunteers.
- Data underpin understanding of butterfly population status and biodiversity trends since 1976; currently records from over 2,500 sites annually.

## Data collection methods
- Standard butterfly transects (Pollard walks): fixed routes (2–4 km) with weekly counts (typically 26 visits/year) across fixed habitat sections; about 2,000 sites sampled yearly.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects; 2–3 visits/year to sample common habitats (farmland), ~800 squares/year.
- Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) conducted during focal flight periods or specific conditions.

## Data structure and indices
- Output as abundance indices (relative measures, not absolute counts) based on counts across transect sections/sites.
- Site indices reflect a constant proportion of the population; detectability varies by species.
- Collated species indices produced using the Generalised Abundance Index (GAI) method (2016) with site-year weighting by the proportion of the species flight period surveyed; integrates data from all methods to estimate seasonal patterns and extrapolate gaps.
- Weighting emphasizes observed data over extrapolated data.

## Quality control and validation
- Field data recorded on standard forms; entered online via UKBMS Data Entry or Transect Walker; uploaded to a central database.
- Automated checks flag anomalies (e.g., unusually high counts, out-of-flight-period records).
- Regional transect coordinators review data; ongoing validation through automated/manual procedures, including checks against known distributions, flight periods, first records at a site, and unusual abundances.
- Corrections handled through queries and coordination with recorders/coordinators.

## Data download and dataset contents
- Annual collated indices (1976–2020) for species with sufficient data; earlier years may be incomplete.
- Data provided as CSV with columns:
  - SPECIES CODE, SPECIES, COMMON NAME
  - YEAR, NO. SITES
  - COLLATED INDEX (log10; scaled so the average across the series equals 2)
  - YEAR RANK (1 = best year)
  - TIME PERIOD, COUNTRY
- Indices are relative population measures rather than absolute counts.

## Licence and attribution
- Open Government Licence (OGL) for dataset use and reuse.
- Required citation details and a provided attribution statement when using information or images derived from the data.

## Collaboration and contact
- UKBMS partners offer guidance on dataset interpretation and potential co-authorship.
- Contact: UK Centre for Ecology & Hydrology (Marc Botham, ukbms@ceh.ac.uk) or Butterfly Conservation (Transect co-ordinator, transect@butterfly-conservation.org).