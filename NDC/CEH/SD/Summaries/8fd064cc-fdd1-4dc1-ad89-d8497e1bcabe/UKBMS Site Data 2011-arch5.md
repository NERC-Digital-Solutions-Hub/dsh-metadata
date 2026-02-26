# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, using standardized methods to monitor butterfly populations.
- Data types include all-species transects (Pollard walks), single-species transects, timed counts, and egg/larval web counts.

## Data collection methods

- All-species transects: fixed-route line transects, recording all butterflies along the route weekly under defined weather conditions; transects are 2–4 km, divided into habitat/management sections, typically yielding 26 counts per year from April to September.
- Transects are conducted between 10:45 and 15:45, with weather criteria (dry, Beaufort wind <5, temperature thresholds with sunshine or overcast conditions).
- Single-species transects follow the same methodology but are recorded only for specific weeks.
- Timed counts: abundance of a focal species recorded over a set period and area; weather criteria apply.
- Egg/larval web counts: counts of eggs or larval webs in suitable habitat areas.
- Field location data are captured in the transect setup, then entered into Transect Walker software.

## Data capture and system workflow

- Data entered by field recorders or regional transect coordinators; new transect routes treated as new sites with new site numbers.
- Transect Walker data are uploaded to an Oracle database for storage.
- Site location data include OS grid references, transect length, and number of sections; grid references are further broken into Easting and Northing coordinates.

## Data structure and storage

- Site Location Data stored as CSV with columns:
  - Site number (unique site identifier)
  - Site name
  - Gridreference (OS grid reference, typically 6-figure accuracy)
  - Easting (X) and Northing (Y)
  - Length (transect length in metres)
  - Country
  - No. Sections (number of transect sections)
  - No. Yrs surveyed (years of data up to 2011)
  - First year surveyed
  - Last year surveyed (up to 2012)

## Quality control and governance

- Each site belongs to a region overseen by a transect coordinator who validates records; this is followed by automated and manual validation procedures.
- Data quality checks ensure correctness of site location data and consistency across years, enabling reliable year-to-year comparisons.
- Fixed transect routes are essential for comparability; changes in route are recorded by treating the new route as a new site.

## Data updates, lifecycle, and accessibility

- Data are updated through ongoing collection and entry; new routes are added as new sites, preserving historical continuity for comparability.
- Some site data may be incomplete, reflecting gaps in information for a subset of sites.
- Data are stored in an Oracle database with site location data available as CSV files, supporting downstream discovery and reuse.

## Considerations for Data Stewards

- Ensure metadata captures site identifiers, route history, and any route changes (to preserve provenance and comparability).
- Manage incomplete data gracefully and document data quality flags or gaps.
- Maintain clear linkage between Transect Walker outputs and the central Oracle repository for auditability.
- Monitor weather-condition constraints and their impact on data availability and temporal coverage.
- Support interoperability by standardizing coordinates (OS grid references, Easting/Northing) and ensuring consistent reporting across years.