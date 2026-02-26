# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- The UKBMS collects data from over 2,000 sites annually across the UK.
- Data come from standardized field methods, primarily fixed-route transects (Pollard walks), for both all-species monitoring and reduced-effort surveys.
- Outputs include site-level indices and national Collated Indices to track population trends over time.
- Data are processed and presented through reports, charts, or dashboards, with ongoing quality assurance and governance.

## Data collection design
- All-species transects (Pollard walks)
  - Fixed-route line transect at each site; all butterflies recorded along a 2–4 km route.
  - Weekly counts from early April to end of September (ideally 26 counts/year).
  - Transects are fixed to allow year-to-year comparability; routes sampled to reflect habitat types and management.
  - Counts occur under specified weather conditions (dry, wind < Beaufort 5, temp thresholds depend on sun/overcast).
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey started in 2009 to sample wider countryside habitats (farmland, etc.).
  - Based on two parallel 1-km transects within randomly selected 1-km squares; fixed-route methodology similar to all-species transects.
  - 2–4 visits per year required, with a minimum of 2 visits in July/August; spring visits encouraged.
- Other methods
  - Single-species transects (fewer weeks).
  - Timed counts for particular species (with set area and time).
  - Egg/larval web counts for species in suitable habitats.
- Data recording and flow
  - Field data on standard forms; entered online via the UKBMS data entry site or Transect Walker software.
  - Data are uploaded to an Oracle database; transect coordinators compile region-wide data.

## Data types and measures
- Data types
  - All-species transect counts (across 26 counts/year per site when possible).
  - Timed counts and egg/larval web counts for focal species.
  - WCBS data for wider countryside sampling.
- Measures and outputs
  - Site indices: relative measures of population size at a site (not absolute; proportional to true abundance).
  - Collated Indices: national indices for each species, derived from site data.
  - Collated Indices are presented as log10 values (Log10 Collated Index, LCI) and scaled so the average index across the series equals 2.
- Species classification
  - Wider countryside species, habitat specialists, and regular migrants are treated with different analytical approaches due to data richness.

## Analytical methods
- For wider countryside species (WCBS and related data)
  - Two-stage model:
    - Stage 1: Generalised additive model (GAM) to estimate the annual seasonal flight pattern for each species.
    - Stage 2: Use seasonal values as an offset in a full-count model to estimate annual changes in abundance.
  - This approach uses data from all survey types to inform the seasonal pattern and trends.
  - Detailed methodology described in Dennis et al. (2013).
- For habitat specialists and regular migrants (less WCBS data)
  - GAM-based imputation to fill missing values and estimate site indices.
  - Combine site indices across sites to produce a national Collated Index.
  - Log-linear regression to account for year effects and site effects when estimating missing values.
  - Collated Indices updated annually as new data are incorporated; past years may be revised.
  - Criteria: Collated Index calculated for species recorded from five or more sites per year.
- Data handling notes
  - Some years may have no Collated Indices for certain species due to insufficient data; trends are flagged accordingly.

## Data quality and governance
- Validation and quality checks
  - Automatic checks in Transect Walker flag abnormal counts or records outside known flight periods.
  - Regional transect coordinators review data for questionable records and perform ongoing validation throughout the season.
  - Additional automated/manual validation checks for records outside distribution ranges, unusual timings, first-time site records, and extreme values.
- Data storage and format
  - Collated Indices stored as CSV files with columns: Species, Year, No. Sites, Collated Index, Time period.
  - Data are collected and validated at regional levels before national aggregation.
- Transparency and reproducibility
  - Methodologies and data processing steps are published and referenced (e.g., methods from Dennis et al. 2013; Rothery & Roy 2001; Moss & Pollard 1993), supporting reproducibility and comparability over time.

## Limitations and data coverage
- Early years for some species may have incomplete Collated Indices due to insufficient data, resulting in shorter trend series.
- The Collated Index for a species can change retrospectively as new data are incorporated, affecting historical trends.

## Data products and metadata
- Primary outputs
  - Site indices (relative abundance per site).
  - National Collated Indices (log10 scale) for species with sufficient data.
- Metadata and data structure
  - Data include columns for species, year, number of contributing sites, Collated Index, and data time period, enabling interpretation of trends and data provenance.