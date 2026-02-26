# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK.
- Data support for estimating butterfly population abundance and trends using standardized methods.
- Outputs include site-level indices and national collated indices to enable comparison and monitoring over time.
- Data are prepared for end users (e.g., policymakers, researchers) to explore and interpret trends.

## Data collection methods
- All-species transects: fixed-route lines (2–4 km) walked weekly during favorable butterfly conditions (dates, weather criteria specified), recording all species within a 5 m band; routes fixed to enable year-to-year comparisons; typically 26 counts/year.
- Transect timing: observed between 10:45 and 15:45, under defined weather conditions (sunshine/temperature constraints).
- Single-species transects: follow all-species methodology but recorded only during focal species’ flight periods.
- Timed counts: counts of a focal species over a fixed time/area, under standard conditions.
- Egg/larval web counts: counts of eggs or larval webs in suitable habitat for specific species.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling (two parallel 1 km transects per 1 km square) in farmland and wider countryside; 2–4 visits per year, summer emphasis.

## Data recording and storage
- Field data collected on standard forms; entered online via UKBMS data entry site or Transect Walker software.
- Data entry may be by the recorder or a regional transect coordinator; regional coordinators compile data for their region.
- Online data and Transect Walker files uploaded to an Oracle database storing all records.
- Primary data products (indices) are derived from the database and related files.

## Analytical methods
- Two main approaches depending on data richness and survey type:

  - Wider countryside species:
    - All season data used to estimate a seasonal flight pattern for each year.
    - Two-stage model: stage 1 uses a generalized additive model (GAM) to estimate annual seasonal patterns; stage 2 uses full annual counts with seasonal values as an offset to estimate yearly abundance changes.
    - Described in Dennis et al. 2013.

  - Habitat specialists and regular migrants:
    - GAM used to impute missing values and derive site indices where reduced-effort data are common.
    - Site indices aggregated to produce a national Collated Index via a log-linear model, accounting for year effects and site effects.
    - Collated Index updated annually as more data are added; some years may have shorter series due to limited data.
    - Collated Indices calculated for species recorded at five or more sites per year.

## Data products and interpretation
- Site indices: relative measures of population size at a site, proportional to the number of butterflies observed; not absolute counts.
- Collated Indices (LCI): log10-scaled, standardized to have an average index of 2 across the series for each species; provides a national perspective on trends.
- Data columns in Collated Indices CSV include: Species (scientific name), Common name, Year, No. Sites, Collated Index, Time period.
- Nature of indices: relative, enabling comparison of trends over time even when absolute counts differ by species or site.

## Quality control and validation
- Automatic in-field checks within Transect Walker flag anomalous counts or records outside known flight periods.
- Regional transect coordinators review records for questionable entries; ongoing validation during the season.
- Additional automated/manual validation includes checks for records outside known distribution, out-of-season records, first-time site records, and extreme or inconsistent abundances.
- Data quality processes ensure consistency with external references (e.g., distribution data) and track outliers.

## Data availability and limitations
- Early years for some species lack Collated Indices due to insufficient data; this is documented as the number of contributing years per species.
- Indices may be updated retrospectively as more data are received and incorporated.
- Site indices are relative, and the Collated Index may shift slightly as historical data are integrated.

## Dataset structure and accessibility
- Collated Indices are stored as CSV files with defined columns (Species, Common name, Year, No. Sites, Collated Index, Time period).
- Data entry and access via UKBMS platforms (http://www.ukbms.org/mydata) and Transect Walker software; underlying analyses rely on an Oracle database.

## Key references
- Dennis, Freeman, Brereton, & Roy (2013): Indexing butterfly abundance while accounting for missing counts and seasonal variability.
- Rothery & Roy (2001): Application of generalized additive models to butterfly data.
- Moss & Pollard (1993); Pollard & Yates (1993): Foundations for calculating collated indices and related methodologies.