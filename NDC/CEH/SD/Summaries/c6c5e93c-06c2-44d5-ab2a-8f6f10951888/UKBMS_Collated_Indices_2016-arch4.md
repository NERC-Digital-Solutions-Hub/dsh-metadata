# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 2,000 UK sites annually.
- Data types include all-species transects, single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).
- Data are used to derive national indices of butterfly abundance through standardized analytical methods.
- Data management emphasizes standardized collection, quality control, and transparent indexing to enable trend analysis across years and species groups.

## Data collection methods
- All-species transects (Pollard walks)
  - Fixed-route, 2–4 km, surveyed weekly from April to September.
  - Record all butterfly species within a fixed 5 m width along the transect.
  - Routes are fixed to allow year-to-year comparisons; weather windows required for activity (dry, wind < Beaufort 5, temperature thresholds with sun/cloud conditions).
- Single-species transects
  - Follow the all-species methodology but focus on a focal species, recorded only on selected weeks.
- Timed counts and egg/larval web counts
  - Timed counts: abundance of a species counted over a set period in a defined area, during suitable weather.
  - Egg/larval web counts: count eggs or larval webs within suitable habitat areas.
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey started in 2009 to sample wider countryside habitats (farmland, etc.).
  - Based on the BTO Breeding Bird Survey design: two parallel 1-km transects within randomly selected 1-km squares.
  - Typically 2–4 visits per year, minimum of 2 visits in July/August; spring visits encouraged.

## Data collection workflow and management
- Field data captured on standard forms.
- Data entered online via the UKBMS data entry site or Transect Walker software (free download).
- Data entry by the recorder or regional transect coordinators; regional coordinators compile data for their region.
- Online data and Transect Walker outputs uploaded into an Oracle database.

## Data analysis and indices
- Two analytical approaches by species group:
  - Wider countryside species
    - Use all survey data in a two-stage model to estimate seasonal patterns and annual changes.
    - Stage 1: Generalized Additive Model (GAM) to estimate annual seasonal flight pattern; daily values normalised to a consistent seasonal pattern across sites but varying by year.
    - Stage 2: Model the full annual counts with seasonal values as an offset to derive annual abundance changes.
    - Based on Dennis et al. 2013.
  - Habitat specialists and regular migrants
    - Data sparse for WCBS and reduced-effort methods; GAMs impute missing values and calculate a site index.
    - Site indices are aggregated to produce a national Collated Index via a log-linear framework that accounts for year and site effects.
- Collated Index (CI)
  - CI is calculated for species with data from five or more sites per year.
  - CI values are log10-transformed and scaled so the series’ average index equals 2, enabling relative comparisons over time.
  - Indices are updated annually as new monitoring data are incorporated; early years may have shorter trend series due to data limitations.
- Definitions and scope
  - Wider countryside species: mobile, broad habitat range.
  - Habitat specialists: low-mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK; some species (e.g., Red Admiral) may be resident in parts of the UK.
- Data coverage notes
  - Earlier years may have incomplete CI calculations due to insufficient data; the dataset notes the number of contributing years per species.

## Quality control and validation
- Automatic checks in Transect Walker flag unusual counts or records outside known flight periods.
- Regional transect coordinators review data for reasonableness and consistency.
- Continuous validation by regional coordinators; automated and manual procedures further validate entries.
- Specific checks for:
  - Records outside recognized distribution ranges (cross-checked against BNMs and UKBMS data).
  - Records outside normal flight periods.
  - First-time site records.
  - Extreme or markedly unusual abundances.

## Outputs and metadata
- Collated Indices are stored as CSV files.
- Key columns:
  - Species (scientific name as per Fauna Europaea)
  - Common name
  - Year
  - No. Sites (sites contributing to the CI that year)
  - Collated Index (CI) for the year
  - Time period (data used to compute the CI)
- The Collated Index provides a relative measure of population size over time, linked to but not equating to absolute population counts.
- The CI series can be revised as new data are incorporated, potentially altering historical values.

## Implications for data governance (data leaders)
- Emphasizes the need for standardized, repeatable data collection across sites and methods.
- Maintains clear data provenance and metadata (site counts, time periods, and data sources) to enable robust trend analysis.
- Highlights the importance of quality control, cross-dataset validation, and transparent handling of missing data via GAMs and imputation.
- Encourages coordination across data types (transects, timed counts, WCBS) to build a coherent national picture.
- Demonstrates how to handle evolving data coverage (early years with fewer sites) and communicate associated limitations.