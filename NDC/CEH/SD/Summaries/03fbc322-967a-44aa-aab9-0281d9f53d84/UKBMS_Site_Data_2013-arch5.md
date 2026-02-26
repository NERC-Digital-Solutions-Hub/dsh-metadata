# Experimental design/sampling regime

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Primary methods include all-species transects (Pollard-like), with alternative methods such as timed counts or egg/larval web counts for some species or sites.

- Data collection methods
  - Field data collection involves recording site locations and butterfly counts along fixed routes.
  - Data are entered into Transect Walker software (free download from UKBMS website) by the recorder or regional transect coordinator.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Transect Walker files are uploaded into an Oracle database that stores all records.

- Nature and units of recorded values
  - Site location data include:
    - Ordnance Survey (OS) grid reference for each site
    - Transect length (metres)
    - Number of sections on a transect
  - Grid reference is also broken down into Easting (x-coordinate) and Northing (y-coordinate)

- Data collection formats and standards
  - All-species transects:
    - Fixed-route line transects of 2–4 km
    - All butterflies recorded within a fixed 5 m wide band along the transect
    - Conducted weekly from early April to late September
    - Aims for about 26 counts per year
  - Transect timing and conditions:
    - Walks between 10:45 and 15:45
    - Weather must support butterfly activity:
      - Dry conditions
      - Beaufort windspeed < 5
      - Temperature thresholds: ≥13°C with at least 60% sunshine, or ≥17°C if overcast
  - Single-species transects follow the same methodology but are recorded only for one or a few weeks during the focal species’ flight period
  - Timed counts and egg/larval web counts involve species-specific counts over a set period/area or habitat area

- Data quality control
  - Regional transect coordinators validate the data for their sites
  - Automated and manual validation procedures follow to check site location data and overall data integrity

- Data storage and accessibility
  - Site location data stored as CSV with clearly defined columns (site number, site name, grid reference, Easting, Northing, length, country, number of sections, years surveyed, first/last year surveyed)
  - Core records stored in an Oracle database; field-level data managed through Transect Walker and the UKBMS data pipeline

- Metadata and documentation
  - Documentation describes column definitions and data capture rules; notes that some site information may be incomplete
  - Route changes generate new site numbers to preserve longitudinal comparability

- Implications for data stewardship
  - Ensure consistency in transect definitions and fixed routes to enable year-to-year comparability
  - Manage updates and route changes while preserving traceability with new site numbers
  - Maintain metadata completeness (e.g., years surveyed, first/last year) and monitor for incomplete fields
  - Support interoperability between Transect Walker outputs and the Oracle database, including data quality checks and validation workflows

- Challenges highlighted
  - Incomplete user needs and priorities
  - Timely data submission and adherence to standards
  - Working with multiple systems and formats, including legacy software and large datasets
  - Handling historical or outdated route data requiring bespoke solutions