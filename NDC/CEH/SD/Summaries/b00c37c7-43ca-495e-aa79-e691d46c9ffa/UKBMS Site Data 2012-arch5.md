# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Data capture uses standardised methods to enable year-to-year comparisons and reliable aggregations.

- Data collection methods
  - All-species transects (Pollard walks): fixed-route line transects; weekly recording of all butterflies under defined weather conditions; transects are 2–4 km, 45 minutes to 2 hours, typically 26 counts per year.
  - Transect routes are fixed to sample habitat/management types and to ensure comparability over time.
  - Single-species transects follow the all-species methodology but record only for certain weeks.
  - Timed counts and egg/larval web counts: species-specific assessments over set times/areas.

- Data handling and workflows
  - Site location data are collected in the field and entered into Transect Walker (free software) by the recorder or regional transect coordinator.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Transect Walker data are uploaded into an Oracle database for storage.

- Data fields and storage
  - Site location data stored as CSV with columns including:
    - Site number, site name, grid reference, Easting (X), Northing (Y)
    - Length of transect, number of sections, country
    - Number of years surveyed and first/last year surveyed (up to 2012)
  - Grid references are typically 6-figure accuracy, representing the transect route center.

- Quality control and validation
  - Regional transect coordinators validate records and check site location data.
  - Data subsequently undergo automated and manual validation to ensure accuracy and consistency.

- Temporal and scope notes
  - The dataset described records information up to the year 2012.
  - Data are linked to fixed routes and historical site records to support longitudinal analyses.

- Governance and reuse considerations (Data Stewards perspective)
  - Standardised collection and storage methods support data discoverability, comparability, and interoperability across sites and years.
  - Clear provenance: route changes generate new site entries, preserving historical continuity.
  - Structured formats (CSV, Oracle DB, Transect Walker) facilitate integration with other datasets and metadata capture for data sharing.