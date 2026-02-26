# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to estimate butterfly abundance.
  - Data are gathered through standardized methods, primarily fixed-route transects, with additional methods for specific scenarios (timed counts, egg/larval web counts).

- Spatial structure and sampling routes
  - All-species transects
    - Fixed-route line transects (2–4 km) designed to sample relevant habitat types and management.
    - Data collected along a 5 m wide belt, typically 26 counts per year from April to September.
    - Transects are kept fixed to enable year-to-year comparisons; divided into sections by habitat/management units.
    - Counts occur weekly under suitable weather (dry, wind < Beaufort 5, temperature thresholds with sunshine or overcast conditions).
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort survey: two parallel 1-km transects within randomly selected 1-km squares.
    - 2–4 visits per transect, with a minimum of two visits in July/August; spring visits encouraged.
  - Other methods
    - Single-species transects (fewer weeks), timed counts, and egg/larval web counts during focal species’ flight periods.

- Data collection workflow and location data
  - Site location data are recorded in the field and entered online via the UKBMS data entry site or via Transect Walker software.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Data and Transect Walker files are uploaded to an Oracle database.

- Data and units (site location)
  - Key fields include:
    - OS grid reference (start location of transect)
    - Easting (X) and Northing (Y) coordinates
    - Length of the transect (in metres)
    - Number of sections on the transect
    - WCBS flag (whether the site is part of WCBS)
    - Country
    - No. of years surveyed; first and last year surveyed
    - Survey type (WCBS or UKBMS)

- Data format and storage
  - Site Location Data stored as CSV.
  - Columns include: Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type.
  - Online data entry and Transect Walker files are uploaded into an Oracle database.

- Quality control and validation
  - Regional transect coordinators validate records based on local knowledge.
  - After initial checks, data undergo automated and manual validation to ensure site location accuracy.

- GIS considerations and usage
  - Provides spatially explicit transect lines and 1-km squares for mapping habitat coverage and sampling effort.
  - OS grid references and Easting/Northing enable precise GIS integration and reprojection as needed.
  - Fixed routes and WCBS sampling patterns support comparative analyses over time and across different habitat contexts.

- Limitations and notes
  - Some WCBS site data may be incomplete (randomised 1-km squares).
  - WCBS data differ in sampling intensity from all-species transects; route changes are treated as new sites.