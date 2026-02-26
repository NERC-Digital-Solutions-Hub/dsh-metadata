# About the UK Butterfly Monitoring Scheme

- Overview
  - Funded and organized by Butterfly Conservation, UK Centre for Ecology & Hydrology (CEH), British Trust for Ornithology (BTO), and Joint Nature Conservation Committee (JNCC); heavily volunteer-driven.
  - Monitors butterfly population status annually across the UK since 1976; typically >3,000 actively recorded sites each year.
  - Data from all sampling methods are analyzed together; the dataset supports understanding biodiversity trends and policy questions.

- Data collection and structure
  - Sampling frameworks:
    - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 26 counts/year, 5 m width, weekly from April to Sept.
    - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel 1 km transects, 2–3 visits/year (minimum two in July/August).
    - Targeted surveys: single-species transects, timed counts, egg/larval web counts using various methods.
  - Data are gathered from sites and 1 km squares, with region- or country-level categorization for aggregation.
  - Outputs: site-based counts and transect data are combined to form annual collated indices per species.

- Data processing and quality control
  - Abundance indices are relative (not absolute population sizes).
  - Collated indices produced with Generalised Abundance Index (GAI) methodology (2016), weighting site data by the proportion of the species’ flight period surveyed that year.
  - Seasonal counts across all methods are used to model seasonal patterns and fill gaps; observed counts have greater influence than extrapolated data.
  - Data entry and validation:
    - Field forms and online entry (UKBMS MyData) or Transect Walker software.
    - Automated checks for data entry errors; regional transect coordinators validate data.
    - Additional validation for out-of-range distributions, unusual flight periods, first-time site records, and extreme values; corrections made as needed.

- Details of this data download
  - Provides annual collated indices of abundance for species with sufficient data, covering 1976–2023 (not all years for all species due to data sufficiency).
  - Format: CSV file with columns:
    - SPECIES_CODE: unique species identifier
    - SPECIES: scientific name
    - COMMON_NAME: vernacular name
    - YEAR: year of the collated index
    - N_SITES: number of contributing sites for that year
    - COLLATED_INDEX: log10 of the Collated Index, scaled so the series’ average is 2
    - YEAR_RANK: year rank for the collated index (1 = best year)
    - TIME_PERIOD: time period used to produce the indices
    - COUNTRY: country of data origin for the regional index
  - Species checklists referenced: Agassiz et al.’s Lepidoptera checklists (2013, 2019, 2020) with updates.

- Licence and attribution statement
  - Open Government Licence (OGL) for free use and reuse with few conditions.
  - Requires citation including the DOI in reports/publications using the data.
  - Attribution: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.”

- Offer of collaboration and contact details
  - UKBMS partners offer dataset guidance and collaboration, including potential co-authorship.
  - Contacts:
    - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
    - Butterfly Conservation: transect@butterfly-conservation.org

- GIS-specific relevance and considerations
  - Data supports map-based analysis of butterfly population trends by species and year, with regional context.
  - Useful for spatial visualization at site and 1 km square scales, and for creating regional indices across the UK.
  - The indices are relative measures; spatial mapping should consider per-site contribution (N_SITES) and regional aggregation (COUNTRY) alongside the collated indices.
  - Data completeness varies by species and year due to historical data sufficiency; some years lack collated indices for certain species.