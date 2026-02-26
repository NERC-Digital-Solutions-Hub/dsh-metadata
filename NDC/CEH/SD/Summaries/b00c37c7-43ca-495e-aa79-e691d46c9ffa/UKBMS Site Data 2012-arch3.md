# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 UK sites annually, primarily via fixed linear transects (Pollard walks) to enable year-to-year comparability in butterfly sightings.

- Data collection methods
  - All-species transects: fixed-route, all butterflies recorded weekly under specified weather conditions; typical transects are 2–4 km, divided into habitat/management sections; about 26 counts per year.
  - Single-species transects: follow the all-species method but record only for one or a few weeks during the focal species’ flight period.
  - Timed counts: abundance of a focal species recorded over a fixed time in a defined area.
  - Egg/larval web counts: count eggs or larval webs of species in suitable habitat areas.
  - Observations occur between 10:45 and 15:45, only under suitable butterfly-activity weather (e.g., dry, wind < Beaufort 5, 13°C+ with ≥60% sunshine or >17°C if overcast).

- Data collection workflow
  - Site location data are collected in the field and entered into Transect Walker (free software) by recorders or regional transect coordinators.
  - If a transect route changes, the new route becomes a new site with a new site number.
  - Transect Walker data are uploaded to an Oracle database.

- Nature and units of recorded values
  - Site location data include OS grid reference (central transect location), Easting/Northing coordinates, transect length, and the number of sections along the transect.

- Quality control
  - A regional transect coordinator validates records for their sites.
  - After preliminary checks, data undergo additional automated and manual validation to ensure correctness of site location data.

- Format and content of stored data
  - Site Location Data are stored as CSV files with columns including:
    - Site number, Site name
    - Gridreference (OS grid reference)
    - Easting, Northing
    - Length (metres)
    - Country
    - No. Sections
    - No. Yrs surveyed (up to 2012)
    - First year surveyed
    - Last year surveyed (up to 2012)

- Scope and metadata
  - The dataset captures spatial (grid references, coordinates) and temporal (years surveyed) metadata for sites.
  - Up-to-date site data and consistent route definitions are maintained through the fixed-route design and governance by regional coordinators.