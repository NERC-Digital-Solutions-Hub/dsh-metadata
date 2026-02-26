# The UK Butterfly Monitoring Scheme (UKBMS)

- Collects data from over 2,000 sites annually across the UK.
- Uses standardized data collection methods to estimate butterfly abundance and trends over time.
- Data underpin national indices for various butterfly groups and individual species.

## Data collection methods

- All-species transects (Pollard walks):
  - Fixed-route, 2–4 km, 45 minutes to 2 hours, weekly counts from early April to late September.
  - 5 m wide recording band; routes chosen to reflect habitat types and management.
  - Weather- and time-of-day constraints apply (10:45–15:45; suitable butterfly activity; specific temperature and sun conditions).
- Single-species transects:
  - Follows all-species methodology but recorded only for focal species and during selected weeks.
- Timed counts and egg/larval web counts:
  - Timed counts record abundance of a species over a set period/area under suitable weather.
  - Egg/larval web counts document eggs or larval webs in suitable habitat areas.
- Wider Countryside Butterfly Survey (WCBS):
  - Reduced-effort survey since 2009 to sample farmland and other wider countryside habitats.
  - Two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits (minimum two in July/August; spring visits encouraged).

## Data collection, entry, and management

- Field data recorded on standard forms; entered online via the UKBMS data site or Transect Walker software.
- Data entered by recorders or regional transect coordinators; uploaded to a central Oracle database.
- Each transect coordinator manages data from all sites in their region.

## Analytical methods and indices

- Two distinct modeling approaches by data type:
  - Wider countryside species:
    - Two-stage model using all counts to estimate annual seasonal flight patterns (generalized additive model).
    - Daily estimates are used as an offset to model annual changes in abundance (stage two).
    - Method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants:
    - General Additive Model (GAM) to impute missing values and compute site indices.
    - Site indices aggregated to produce a national Collated Index per species (log-linear regression for missing values and trend estimation).
    - Collated Indices updated annually as new data are incorporated; calculated for species recorded at five or more sites per year.
- Definitions of species groups:
  - Wider countryside species: mobile, broad habitat range.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: do not overwinter in the UK.

## Output, units, and data presentation

- Site indices: relative measures of population size (not absolute), reflecting a constant proportion of true abundance.
- Collated Indices: presented as the logarithm (Log10) of the Collated Index (LCI); indices are scaled so the average across the series equals 2 for comparability.
- Data coverage notes:
  - Some early years lacked sufficient data for Collated Indices; the number of contributing years is indicated for each species-year.

## Quality control and data governance

- Data validation:
  - Automatic checks in Transect Walker flag unusual counts or out-of-season records; recorders can modify entries.
  - Regional coordinators validate data throughout the season.
  - Further automated/manual validation checks for out-of-range distributions, flights outside known periods, first-time site records, and outlier values.
- Data storage and structure:
  - Collated Indices stored as CSV files with defined columns (Species, Common name, Year, No. Sites, Collated Index, Time period).
- Metadata and traceability:
  - Dataset entries include site counts, years of contribution, and associated metadata to support traceability and verification.

## Terminology and notes

- Collated Indices may be revised as new data are integrated; past years’ indices can be updated.
- The scheme emphasizes consistent method application, data quality checks, and transparent reporting of data limitations and site coverage.

## Relevance for monitoring framework authors

- Demonstrates integration of standardized field methods, centralized data management, and dual analytical approaches tailored to data richness.
- Shows how relative indices (site indices and Collated Indices) are derived and scaled for temporal trend analysis.
- Highlights governance considerations: validation workflows, coordination roles, and data sharing/availability through publicly accessible formats (CSV) and central databases.
- Addresses common monitoring challenges: data gaps, missing values, habitat/-range heterogeneity, and transparency of uncertainty due to varying site coverage over time.