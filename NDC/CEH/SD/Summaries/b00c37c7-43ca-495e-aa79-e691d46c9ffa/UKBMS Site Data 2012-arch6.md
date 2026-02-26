# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites per year in the UK.
  - Data are gathered using standardized methods: all-species transects (Pollard walks), plus single-species transects, timed counts, and egg/larval web counts for selected species.

- Data collection methods
  - All-species transects: fixed-route line transects where all butterflies are recorded weekly under defined weather conditions; transects are 2–4 km long, divided into habitat/management sections, and typically yield 26 counts per year from April to September.
  - Transect protocol: transects must be fixed to enable year-to-year comparisons; data collection occurs between 10:45 and 15:45 under weather criteria (dry conditions, wind < Beaufort 5, temperature thresholds depending on sunshine/overcast conditions).
  - Single-species transects: follow the all-species method but focus on one focal species and are conducted in fewer weeks.
  - Timed counts: record abundance of a particular species over a set period and area within the same time window and weather criteria.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat for selected species.

- Data collection tools and workflow
  - Field data are entered into Transect Walker (free software) by the recorder or regional transect coordinator.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Transect Walker data are uploaded into an Oracle database that stores all records.

- Data structure and storage
  - Site location data include OS grid reference, transect length (m), and number of sections.
  - Grid reference is decomposed into Easting (X) and Northing (Y) coordinates.
  - The core site location data are stored in a CSV file with columns:
    - Site number
    - Site name
    - Gridreference
    - Easting
    - Northing
    - Length
    - Country
    - No. Sections
    - No. Yrs surveyed
    - First year surveyed
    - Last year surveyed (up to 2012)

- Quality control
  - A regional transect coordinator validates records for their sites.
  - Data then undergo automated and manual validation procedures to ensure accuracy of site location data.

- Data implications for analysis and reuse
  - Fixed routes enable year-to-year comparability of butterfly sightings.
  - Route changes create new site entries, affecting longitudinal analyses.
  - Outputs include structured site location data that support mapping, aggregation, and cross-site analyses.

- Reference
  - Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation.