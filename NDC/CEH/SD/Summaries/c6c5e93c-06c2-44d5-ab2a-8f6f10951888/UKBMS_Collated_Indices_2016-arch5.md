# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects and integrates data from over 2,000 sites annually across the UK.
- Multiple data collection methods are used to estimate butterfly abundance, including all-species transects (Pollard walks), single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).

## Data collection methods
- All-species transects (Pollard walks):
  - Fixed-route line transect, 2–4 km, sampled weekly from April to September.
  - Belt: 5 m wide; transect remains fixed to enable year-to-year comparisons.
  - Typical session: 45 minutes to 2 hours; weather and habitat management sampled to represent diverse conditions.
  - 26 counts per year per transect; conducted between 10:45 and 15:45, under specified weather conditions (dry, wind < Beaufort 5, temperature thresholds with sun or overcast rules).
- Single-species transects:
  - Follows all-species methodology but recorded only during selected weeks for focal species.
- Timed counts and egg/larval web counts:
  - Timed counts record abundance of a focal species over a set period and area under suitable weather.
  - Egg/larval web counts record eggs or larval webs within habitat areas for selected species.
- Wider Countryside Butterfly Survey (WCBS):
  - Reduced-effort survey using two parallel 1-km transects within randomly selected 1-km squares.
  - 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).
  - Based on the BTO Breeding Bird Survey methodology.

## Data submission and storage
- Field data recorded on standard forms; entered online via UKBMS MyData or via Transect Walker software.
- Data entry performed by the recorder or the regional transect coordinator; regional coordinators compile data for their region.
- Data uploaded into an Oracle database that houses all records.

## Analytical methods and outputs
- Wider countryside species (mobile, broad habitat use):
  - Two-stage model using all data across survey types to estimate annual seasonal patterns and to compute annual population changes.
  - Stage 1: Generalized Additive Model (GAM) to estimate annual seasonal flight pattern; day values normalized to a common seasonal pattern across sites but varying by year.
  - Stage 2: Model on full annual counts with seasonal values as an offset to derive annual changes in abundance.
  - Method described in Dennis et al. 2013.
- Habitat specialists and regular migrants (less complete WCBS data; reduced-effort sampling):
  - GAM to impute missing values and calculate a site index.
  - Site indices combined to derive a national annual Collated Index.
  - Collated Index computed as a log10 index (LCI); normalization set so the average index across the series equals 2.
  - Not all sites are monitored every year; series length varies, and indices may be updated retrospectively as more data are received.
- Species classifications:
  - Wider countryside species: mobile, broad habitat range.
  - Habitat specialists: low mobility, semi-natural habitats.
  - Regular migrants: overwinter outside the UK; some species (e.g., Red Admiral) may be resident in parts of the UK.
- Data products:
  - Collated Indices for each species, updated annually as more data are incorporated.
  - Dataset includes: Species (scientific name), Common name, Year, No. Sites contributing, Collated Index, Time period of data used.

## Quality control and governance
- Automated checks in Transect Walker flag unusual counts or records outside known flight periods.
- Regional transect coordinators review data for questionable records; continuous validation throughout the season.
- Additional automated and manual validation steps:
  - Checks for records outside known distribution or flight periods.
  - Records first observed at a site.
  - Extreme abundances or atypical values for a site and time.
- Data provenance and integrity are maintained through tiered validation and updates to the Collated Indices as new data arrives.

## Data standards, interoperability, and stewardship considerations
- Data are stored in a structured format (CSV for Collated Indices) with well-defined columns and metadata, enabling reproducibility and traceability.
- Indices are scaled and indexed (log10 Collated Index) to facilitate comparison over time.
- Documentation references for the analytical methods and models (GAMs, two-stage modeling) support transparency and reuse of analyses.
- The ongoing update cycle means past indices may be revised as new data are incorporated, underscoring the need for versioning and clear metadata about data periods and contributions.

## Implications for data stewards
- Maintain clear metadata documenting data collection methods, site definitions, and temporal windows.
- Ensure robust data validation, error handling, and provenance tracking from field forms to the Oracle database and final CSV outputs.
- Manage versioning and change logs for Collated Indices as new data are integrated.
- Support interoperability by standardizing taxonomic nomenclature (scientific and common names) and time-period definitions.
- Facilitate data access and reuse through well-documented outputs and transparent methodological references.