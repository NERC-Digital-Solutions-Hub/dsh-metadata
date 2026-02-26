# About the UK Butterfly Monitoring Scheme

- Overview
  - The UKBMS is a collaboration funded by Butterfly Conservation, the Centre for Ecology and Hydrology (CEH), British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - Relies on volunteers; monitors butterfly populations across the UK since 1976.
  - Currently >2500 actively recorded sites each year; data used to understand biodiversity status and inform policy.

- Data collection and structure
  - Components:
    - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts, 5 m width, ~26 counts/year; ~2000 sites.
    - Reduced effort surveys: single-species transects, alternative methods (timed counts, egg/larval web counts).
    - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel 1-km transects, 2–4 visits per year (July/August prioritized); ~750 squares/year.
  - Data types: counts for all species along transects; special methods focus on particular species.

- Data processing and trend analysis
  - Uses abundance indices (relative measures) rather than absolute population sizes.
  - Indices reflect a constant proportion of butterflies present; detection varies by species.
  - Collated species indices produced with Generalised Abundance Index (GAI, 2016) and weighting by survey effort/flight period.
  - Combines data from all components to model seasonal patterns and generate trends.

- Quality control
  - Field data captured on standard forms; entered online or via Transect Walker.
  - Automated checks for data errors; regional transect coordinators validate records.
  - Further validation checks for range, flight period, site history, extreme values.
  - Corrections made through queries and coordination with recorders before final dataset updates.

- Details of this data download (columns and content)
  - Provides long- and short-term trends for species with sufficient data; delivered as CSV.
  - Key columns include:
    - COMMON_NAME, SCI_NAME
    - NYEARS (years in the series)
    - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL (overall trend description)
    - F_FULL_R (percent change over the series)
    - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (last 20 years)
    - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (last 10 years)
  - Data uses vernacular names (COMMON_NAME) aligned with Emmet & Heath, and scientific names (SCI_NAME) from Fauna Europaea.

- Licence and attribution
  - Open Government Licence (OGL) for free use and reuse with few conditions.
  - Must include citation with DOI as specified in metadata; attribution required: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.”

- Collaboration and contact
  - Partners offer guidance on dataset interpretation; possible co-authorship and intellectual input for publications.
  - Contacts:
    - Tom Brereton (Butterfly Conservation): tbrereton@butterfly-conservation.org
    - Marc Botham (CEH): ukbms@ceh.ac.uk

- Practical takeaways for data leaders
  - Demonstrates multi-component data integration (transacts, WCBS, reduced surveys) for a unified trend index.
  - Highlights governance practices: standardized data collection, regional validation, automated and manual quality checks.
  - Emphasizes open data licensing and clear attribution to enable reuse across networks and collaborations.
  - Provides structured metadata and clear column definitions for long/short-term trend analyses to inform data strategy, reporting, and policy-oriented analyses.