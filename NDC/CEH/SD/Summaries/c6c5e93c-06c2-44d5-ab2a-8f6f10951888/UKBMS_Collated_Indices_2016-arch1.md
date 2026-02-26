# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK.
- Butterflies are primarily counted along fixed-line transects called Pollard walks, using standardised methods to estimate population abundance for various species.
- Data support national indices and trends for butterfly populations, with updates and quality checks to ensure reliability.

## Data collection methods
- All-species transects
  - Fixed-route line transect at a site, recording all butterflies along a 2–4 km route in a fixed-width band (typically 5 m) each week from early April to late September (ideally 26 counts/year).
  - Transects are fixed to enable year-to-year comparisons and cover habitat/management units; walks occur 10:45–15:45 under suitable butterfly activity conditions.
  - Typically 45 minutes to 2 hours per walk.
- Single-species transects
  - Follow the all-species transect methodology but record only for a focal species during a subset of weeks.
- Timed counts and egg/larval web counts
  - Timed counts: record abundance of a chosen species over a fixed period and area, within allowed weather windows.
  - Egg/larval web counts: record eggs or larval webs in suitable habitat for particular species (e.g., Marsh Fritillary).
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort sampling in wider countryside habitats (farmland, etc.), modeled on the BTO Breeding Bird Survey approach.
  - Two parallel 1-km transects per 1-km square, 2–4 visits per year (minimum two visits in July/August; spring visits encouraged).

## Data collection and handling
- Field data are collected on standard forms.
- Data entered online via UKBMS data entry site or via Transect Walker software; input by recorders or regional transect coordinators.
- Transect coordinators compile and submit regional data; online data and Transect Walker files are uploaded into an Oracle database.

## Analytical methods and indices
- Two main national indexing approaches, depending on data type:
  - Wider countryside species (mobile, various habitats)
    - Use all counts from all survey types to estimate seasonal patterns and yearly abundance changes.
    - Two-stage model:
      1) Generalised Additive Model (GAM) to estimate annual seasonal flight pattern; daily values normalized to a year-specific pattern.
      2) Full annual counts model with seasonal values as an offset to estimate annual abundance changes.
    - Described in Dennis et al. 2013; accounts for missing counts and seasonal variability.
  - Habitat specialists and regular migrants (less WCBS data)
    - Use GAM to impute missing values and derive a site index.
    - Combine site indices to produce a national Collated Index.
    - Because not all sites are monitored every year, apply a log-linear regression to estimate missing values and produce indices and trends.
    - Collated Indices are updated annually with new data; indices for species require at least five monitored sites per year.
- Index definitions and scaling
  - Site indices provide a relative measure of population size, proportional to the actual population.
  - Collated Indices are presented as the log10 of the Collated Index (LCI), scaled so the average index over the series equals 2 for each species.
  - Red Admiral example noted as increasingly resident in parts of the UK, though largely migratory elsewhere.

## Data quality, validation, and reporting
- In-built automatic checks in Transect Walker flag anomalous counts or records outside known flight periods; recorders may adjust or confirm records.
- Regional coordinators review submissions for questionable records; checks continue throughout the season.
- Additional automated and manual validation steps verify distribution ranges, flight periods, new site appearances, extreme values, and deviations from typical site counts.
- Data and indices are compiled with metadata, documenting source sites, counts, and calculations.

## Data products and metadata
- Collated Indices are stored as CSV files with columns:
  - Species (scientific name per Fauna Europaea)
  - Common name (vernacular, per Emmet & Heath)
  - Year (calendar year of the Collated Index)
  - No. Sites (number of contributing sites for that year)
  - Collated Index (value for the given species/year)
  - Time period (data range used to produce the Collated Index)

## Challenges and context for analysis
- Data gaps in earlier years for some species due to insufficient data for Collated Indices.
- Indices may be updated retrospectively as more data are incorporated, potentially altering previously reported trends.
- Data scale and heterogeneity across site types require careful modeling (GAMs, offset terms) to produce robust national trends.
- Quality assurance and data accessibility rely on coordinated fieldwork, standardised protocols, and data portals with rich metadata.