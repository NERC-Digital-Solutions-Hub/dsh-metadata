# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Data are gathered using standardized field methods (all-species transects, single-species transects, timed counts, and egg/larval web counts) with fixed routes to enable year-to-year comparisons.
- All-species transects involve recording all butterflies along a fixed 2–4 km route in a 5 m wide band, typically 26 counts per year from early April to late September; weather and time windows are constrained to suitable butterfly activity.

- Transect design and data collection:
  - Transects are fixed routes, divided into habitat/management sections to sample habitat types evenly.
  - Single-species transects cover the same routes but only during focal species flight periods.
  - Timed counts and egg/larval web counts provide alternative abundance measures for specific species.
  - Field data are collected on standard forms, entered into Transect Walker software, and uploaded to an Oracle database.
  - Each transect has a regional coordinator responsible for compiling data.

- Analytical methods:
  - Site indices are generated per site using Generalized Additive Models (GAM) to impute missing values.
  - A Collated Index (for each species) combines site indices across all monitored sites using a log-linear regression model to account for annual variability (year effects) and site differences (site effects).
  - The Collated Index is updated annually as new data are incorporated; past indices may be revised as data are received.

- Nature and units of recorded values:
  - Site indices are relative measures of population size, not absolute counts.
  - Collated Indices are presented as the Log10 Collated Index (LCI); values are scaled so the average index across the series equals 2, facilitating relative comparison over time.
  - Collated Indices are calculated for species recorded at five or more sites per year.

- Quality control and data validation:
  - Automatic checks in Transect Walker flag unusual counts or records outside known flight periods.
  - Regional coordinators review data for questionable entries and consistency with distribution and flight periods.
  - Additional automated/manual validation includes checks against known distribution ranges, first-time site records, and outlier abundances.

- Data format and storage:
  - Collated Indices are stored as CSV files.
  - Columns include: Species (scientific name per Fauna Europaea), Common name, Year, No. Sites, Collated Index, Time period (data usage window).

- GIS-relevant considerations:
  - Fixed transect routes yield comparable spatial time-series data suitable for map-based visualisation of relative abundance trends.
  - Data integration across multiple sampling methods and years supports spatial analyses of habitat effects and distributional shifts.
  - Relative indices and annual updates require versioning and careful handling of missing data and revisions in map products.

- Practical implications and challenges for GIS work:
  - Data are distributed across multiple methods, sites, and years, with varying resolutions and coverage.
  - Cleaning and transforming data are needed to align site-level indices with GIS layers (habitat units, transect routes) and to manage updates.
  - Model-based estimations (GAM, log-linear) introduce uncertainty that should be considered in spatial visualisations and trend assessments.