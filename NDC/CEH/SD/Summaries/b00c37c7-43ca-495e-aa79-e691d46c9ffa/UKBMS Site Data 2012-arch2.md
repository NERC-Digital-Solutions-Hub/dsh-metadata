# UK Butterfly Monitoring Scheme (UKBMS) data collection and management

- The UKBMS gathers data from over 1,000 sites annually across the UK, using standardized methods to monitor butterfly populations and habitat management impacts.
- Key data collection approaches include:
  - All-species transects (Pollard walk): fixed-route line transects 2–4 km long, sampled weekly from April to September, typically 26 counts per year.
  - Single-species transects: follow all-species methodology but focus on one or a few weeks for a focal species.
  - Timed counts: abundance of a particular species recorded over a fixed time and area.
  - Egg/larval web counts: counts of eggs or larval webs in suitable habitats for specific species (e.g., Marsh Fritillary).
- Transect routes are fixed to enable year-to-year comparability; routes are divided into habitat/management sections.

## Experimental design and sampling regime

- Transects are conducted under defined weather conditions conducive to butterfly activity (e.g., dry, Beaufort wind < 5, temperature thresholds with sunshine or overcast conditions).
- Observations occur between 10:45 and 15:45 local time.
- Data collection aims to sample diverse habitat types and management practices on each site.

## Data collection methods

- Site location data are recorded in the field at transect setup and entered into Transect Walker, a dedicated software (free download from ukbms.org).
- Data entry can be by the recorder or a regional transect coordinator; a new transect route constitutes a new site with a new site number.
- Transect Walker files are uploaded into an Oracle database that stores all records.

## Nature and units of recorded values

- Site location data include:
  - OS grid reference for each site, plus Easting and Northing coordinates.
  - Transect length (metres) and the number of sections along the transect.
  - Country, number of years surveyed, first year surveyed, and last year surveyed (up to 2012 in the documented dataset).

## Quality control

- A regional transect coordinator oversees data for their sites, leveraging local knowledge to perform checks.
- Records undergo initial validation locally, followed by automated and manual validation to verify site location data and consistency.

## Format of stored data

- Site Location Data are stored as CSV files with columns including:
  - Site number (unique identifier)
  - Site name
  - Gridreference (OS, typically 6-figure accuracy)
  - Easting and Northing (central coordinates)
  - Length (metres)
  - Country
  - No. Sections
  - No. Yrs surveyed (up to 2012)
  - First year surveyed
  - Last year surveyed (up to 2012)
- The documentation references the Pollard, E. & Yates, T.J. (1993) methodology for butterfly monitoring, indicating established, standardized practices underpinning data collection and comparability.