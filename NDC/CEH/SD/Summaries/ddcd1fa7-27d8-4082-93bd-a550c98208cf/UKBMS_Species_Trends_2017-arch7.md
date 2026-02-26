# 1. About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: annual, site-based monitoring plus random 1km square sampling to track butterfly population status and trends across the UK since 1976; over 2500 actively recorded sites each year.
- Sampling framework:
  - Weekly Pollard walks (standard transects): fixed-route transects (2–4 km), 5 m wide survey band, 26 counts per year, April–September.
  - Reduced effort surveys: single-species transects or alternative methods (timed counts, egg/larval web counts).
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km square locations with two parallel 1 km transects, 2–4 visits per year to sample common habitats.
- Data structure: results from all components are analyzed together to produce abundance indices (relative measures) rather than absolute counts.
- Geographic and temporal scope: UK-wide coverage with a long-running dataset, used to inform biodiversity status and policy questions.
- Data access for GIS: provides structured data about transects, sites, and species for map-based analysis and trend assessment.

## 2. Nature of data collected and trend analysis

- Data products are abundance indices derived from counts along transects and WCBS sites; indices are relative proxies for population size.
- Trend calculation: Generalised Abundance Index (GAI) method (2016) combining counts across all survey types; site-year weighting accounts for proportion of species flight period surveyed.
- Data handling: uses all counts in a season to model seasonal patterns and extrapolate gaps; weighting emphasizes observed data over extrapolated estimates.
- Trend outputs: long-term (F_LIN_B, F_LIN_SE, F_LIN_P with descriptive F_TRENDETAIL), and short-term windows (T10_LIN_*, T10_TRENDDETAIL, T20_LIN_*, T20_TRENDDETAIL, with corresponding R percentages).
- Data coverage notes: applied to species with sufficient data for reliable trends; format described for end-user interpretation.

## 3. Quality control

- Field data collection on standard forms; online entry via UKBMS MyData or Transect Walker; data uploaded to a centralized database.
- Automated checks and validation: abnormal counts, records outside flight periods, and other common entry errors are flagged with options to edit.
- Regional oversight: each site belongs to a transect coordinator who validates records; ongoing checks by coordinators throughout the season.
- Additional validation: automated/manual queries verify records against known distributions, flight periods, site first-time records, and unusual abundances; corrections made via queries and coordination with recorders.

## 4. Details of this data download

- Contents: long- and short-term trends in collated indices for all species in the UK with sufficient data; delivered as a CSV file.
- Columns and fields include:
  - COMMON_NAME and SCI_NAME
  - NYEARS (years in the series)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL (long-term trend metrics)
  - F_FULL_R (overall percentage change)
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year window)
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year window)
- Data notes: designed for analysis of trends over time with standardized descriptive fields.

## 5. Licence and attribution statement

- Open Government Licence (OGL) applies; free use with few conditions.
- Citation: include the dataset citation and DOI in any reports/publications.
- Attribution: includes UKBMS data © Butterfly Conservation, Centre for Ecology & Hydrology, British Trust for Ornithology, and Joint Nature Conservation Committee; the attribution text must accompany information or images derived from the data.

## 6. Offer of collaboration and contact details

- UKBMS Partners offer guidance on dataset use and interpretation of outputs.
- Collaboration: potential for co-authorship and intellectual input in publications, conferences, or posters resulting from UKBMS data.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)