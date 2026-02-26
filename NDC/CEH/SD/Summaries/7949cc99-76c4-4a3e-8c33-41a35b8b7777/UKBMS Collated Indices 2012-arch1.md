# Experimental design/sampling regime

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Most data come from fixed-line transects called Pollard walks; other standard methods (timed counts, egg/larval web counts) used for some species/sites.
  - All-species transects involve recording all butterflies along a fixed-route, weekly, under predefined weather conditions; transects are 2–4 km, 5 m wide, and divided into habitat/management sections; typically 26 counts per year from April to September.
  - Weather and time windows: transects conducted 10:45–15:45, when butterfly activity conditions are met (dry, Beaufort wind <5, and certain temperature/sun conditions).

- Transect types and methodology
  - All-species transects: fixed routes, weekly counts, uniform habitat sampling, maintained year-to-year for comparability.
  - Single-species transects: follow all-species methodology but target one focal species for one or more weeks.
  - Timed counts: abundance of a focal species recorded over a set period/area, within the same weather window.
  - Egg/larval web counts: count eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).

- Data collection workflow
  - Field recording on standard forms.
  - Data entered into Transect Walker software; can be entered directly by recorders or by regional transect coordinators.
  - Transect Walker files uploaded to an Oracle database; regional coordinators compile data for their region.
  - Data flow supports ongoing quality checks and central storage.

- Analytical framework
  - Validation and modeling pipeline:
    - After validation, a General Additive Model (GAM) imputes missing values and derives a site index.
    - Site indices from all sampling methods are aggregated to produce a national annual index per species, the Collated Index.
    - Since not all sites are monitored every year, a loglinear regression model estimates missing values to produce indices and trends, accounting for year effects (weather) and site effects (population size variability).
    - Collated Indices are updated annually as new data are incorporated; past values may adjust slightly.
  - Scope for indices:
    - Collated indices are calculated for species observed at five or more sites per year.
  - Data units:
    - Site index is a relative measure, proportional to actual population size; not absolute.
    - Collated Indices are presented as Log10 Collated Index (LCI), scaled so the average index over the entire series equals 2 for each species.

- Data quality control
  - In-field automatic checks within Transect Walker flag potential data issues (e.g., unusually high counts, records outside known flight periods).
  - Regional coordinators review data for questionable entries, supported by regional knowledge.
  - Additional automated/manual validation includes checks against known distribution ranges, flight periods, first-time site records, and extreme or atypical values.

- Data storage and format
  - Collated Indices stored as CSV files.
  - Columns include: Species (scientific name per Fauna Europaea), Common name (per Emmet & Heath), Year, No. Sites, Collated Index, Time period (data used to produce the index).
  - Time period provides context for the data used in index calculations.

- Practical considerations for analysts
  - Indices are relative and time-varying as new data are incorporated; sensitivity to recent data updates may slightly shift historical values.
  - Local-scale analyses may be limited by data availability (minimum five sites per species per year) and by the relative nature of site indices.
  - The approach explicitly models year and site effects and uses GAM for imputation, enhancing comparability across years with incomplete site coverage.