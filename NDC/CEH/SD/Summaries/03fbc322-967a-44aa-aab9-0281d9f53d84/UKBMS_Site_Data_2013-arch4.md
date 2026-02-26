# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Data collection relies on fixed transect methods to enable year-to-year comparisons and track butterfly abundance.

## Data collection methods
- All-species transects
  - Fixed-route line transect (2–4 km) where all butterflies observed along the route each week.
  - Typically 26 counts per year (weekly from early April to late September).
  - Transect routes are chosen to sample habitat types and management activity; routes are kept fixed for comparability.
  - Counts occur under set weather conditions: 10:45 am to 3:45 pm; dry conditions; wind < Beaufort 5; temperature thresholds (13°C with 60%+ sunshine, or >17°C if overcast).
  - Data collected in a 5 m wide band along the transect.
  - Called a Pollard walk; Pollard & Yates (1993) referenced for methodology.
- Single-species transects
  - Same methodology as all-species transects but focused on one or a few weeks for the focal species.
- Timed counts and egg/larval web counts
  - Timed counts record abundance of a species over a set period within a defined area.
  - Egg and larval web counts document eggs or larval webs in suitable habitat areas (e.g., Marsh Fritillary).

## Data collection workflow
- Site location data collected in the field at transect setup and entered into Transect Walker software (free download from UKBMS).
- Data entry can be by the recorder or the regional transect coordinator; route changes create a new site with a new site number.
- Transect Walker files are uploaded into an Oracle database that stores all records.

## Data capture: nature and units
- Site location data include:
  - OS grid reference (start point), typically 6-figure accuracy
  - Easting and Northing coordinates (X, Y)
  - Transect length (metres)
  - Number of sections on the transect
- Additional fields:
  - Country
  - Number of years surveyed at the site
  - First year surveyed
  - Last year surveyed (up to 2012 for reporting)

## Quality control
- Each site’s data are overseen by a regional transect coordinator with knowledge of the sites.
- Records undergo preliminary validation by the regional coordinator, followed by automated and manual validation to ensure location accuracy and data consistency.

## Data storage format
- Site Location Data stored as CSV.
- Key columns include:
  - Site number, Site name
  - Gridreference, Easting, Northing
  - Length, Country
  - No. Sections, No. Yrs surveyed
  - First year surveyed, Last year surveyed

## References and notes
- Methodological framework based on Pollard, E. & Yates, T.J. (1993) for butterfly monitoring.
- Data collection and storage infrastructure (Transect Walker; Oracle database) underpins data management and accessibility.