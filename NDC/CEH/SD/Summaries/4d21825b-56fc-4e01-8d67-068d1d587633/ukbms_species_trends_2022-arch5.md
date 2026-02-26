# UK Butterfly Monitoring Scheme Data Download

## Overview
- Managed by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- Relies on volunteer-led, site-based monitoring to track butterfly population status in the UK since 1976.
- Data underpin policy questions on biodiversity status and trends.
- Scope includes over 3000 actively recorded sites each year; data are collected via multiple sampling methods and analyzed together.

## Data collection and structure
- Sampling framework comprises:
  - Standard butterfly transects (Pollard walks): fixed routes, 2–4 km, 26 weekly counts April–September.
  - Wider Countryside Butterfly Survey (WCBS): stratified 1 km squares with two parallel transects, 2–3 visits per year.
  - Targeted surveys: single-species transects and other methods (e.g., timed counts, egg/larval web counts).
- Data types include abundance indices (relative measures of population size, not absolute counts).
- Indices are constructed to reflect seasonal patterns using the Generalised Abundance Index (GAI) with site- and year-weighting to balance observed vs. extrapolated data.
- Data columns in the downloadable file include:
  - COMMON_NAME, SCI_NAME, NYEARS
  - Long-term trends: F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL, F_FULL_R
  - Last 20/10 years trends: T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
  - Last 10 years trends: T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
  - Trend descriptions categorize rapid decline, rapid increase, or stability based on slope and P-values.

## Data quality control
- Field data recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker.
- Automated checks flag data-entry errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review records for questionable entries; ongoing validation throughout the season.
- Additional automated/manual validation checks ensure records are within expected distribution ranges, flight periods, and site history; discrepancies are resolved through queries and coordinator/recorders’ input.

## Details of this data download
- Provides long- and short-term trends for species with sufficient data, in CSV format.
- Long-term trends cover from 1976 to 2022 (start year may vary by species due to data availability).
- Descriptions for each column align with referenced taxonomic/name sources (COMMON_NAME per Emmet & Heath; SCI_NAME per Agassiz et al. updates).

## Licence and attribution
- Released under the Open Government Licence (OGL), enabling free use with minimal conditions.
- When used, citations must include the specified DOI in the metadata record.
- Attribution to include with outputs: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact
- UKBMS partners offer guidance and interpretation of outputs.
- Opportunities for co-authorship and intellectual input in publications, conference presentations, or posters resulting from UKBMS data use.
- Contact points:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)