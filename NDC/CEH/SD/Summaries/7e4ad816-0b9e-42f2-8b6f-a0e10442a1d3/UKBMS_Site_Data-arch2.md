# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, primarily via fixed linear transects called Pollard walks.
- Monitoring approaches include:
  - All-species transects: fixed routes, weekly counts, 2–4 km in length, 5 m wide belt, sampling April to September with about 26 counts per year; transects are fixed to enable year-to-year comparisons; typical weather windows and times (10:45–15:45) required.
  - Single-species transects: follow the all-species methodology but record only a focal species during selected weeks.
  - Timed counts and egg/larval web counts: targeted abundance for specific species under set weather conditions.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling of wider habitats (established 2009), using two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per year (minimum two visits in July/August; spring visits encouraged).

- Data collection methods:
  - Site location data collected in the field when transects or counts are set up.
  - Data entered online via UKBMS MyData portal or via Transect Walker software; new route creates a new site in the system.
  - Online data and Transect Walker files uploaded to an Oracle database.

- Nature and units of recorded values:
  - Site location includes OS grid reference, transect length, and number of sections; WCBS status noted; some data gaps exist for WCBS sites due to randomised 1-km squares.
  - Grid references are further broken into Easting (X) and Northing (Y) coordinates.

- Quality control:
  - Each site belongs to a regional transect coordinator who validates records; following initial checks, automated and manual validation procedures verify location data and data integrity.

- Format and storage of site location data:
  - Stored as CSV with columns including:
    - Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. of Sections, No. Years surveyed, First year surveyed, Last year surveyed, Survey type (WCBS or UKBMS).
  - WCBS sites are marked as WCBS; other surveys are denoted as UKBMS.

- Purpose and outputs:
  - The standardized data collection and validation framework enables monitoring of butterfly abundance over time and supports the production of outputs such as reports, maps, and charts, with datasets stored in a centralized database for analysis and policy scrutiny.