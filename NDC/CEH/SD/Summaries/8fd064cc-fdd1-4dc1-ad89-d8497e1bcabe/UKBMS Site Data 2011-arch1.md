# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Most sites estimate butterfly numbers using fixed linear transects called Pollard walks; alternative standardized methods include timed counts and egg/larval web counts for some species.

## Experimental design

- All-species transects:
  - Fixed-route line transect at a site; all butterflies recorded along the route weekly under defined weather conditions.
  - Routes selected to sample habitat types and management on the site and must remain fixed for year-to-year comparisons.
  - Typical length: 2–4 km; duration: 45 minutes to 2 hours.
  - Transects divided into sections by habitat/management units.
  - All species counted within a fixed 5 m wide band along the transect each week from early April to end September; ideally 26 counts per year.
  - Walk times: 10:45–15:45; weather criteria: dry, wind Beaufort < 5, temperature ≥ 13°C with at least 60% sunshine, or >17°C if overcast.
- Single-species transects:
  - Follow the all-species methodology but recorded only on one or a few weeks during the focal species’ flight period.
- Timed counts:
  - Record the abundance of a particular species over a fixed period and within a fixed area, using the same time window as above.
- Egg/larval web counts:
  - Record the number of eggs or larval webs of a species in a suitable habitat area.

## Data collection methods

- Site location data are collected in the field when a transect, timed count, or larval web count is established.
- Data entered into Transect Walker (free software) and submitted to an Oracle database.
- If a transect route changes, the new route is treated as a new site with a new site number.
- Transect Walker files are uploaded to the central database.

## Nature and units of recorded values

- Site location data include:
  - OS grid reference for the site, transect length (metres), and number of transect sections.
  - For many sites, some information may be incomplete.
  - Grid reference is further broken into Easting (X) and Northing (Y) coordinates.

## Quality control

- Each site’s data belong to a regional transect coordinator’s remit.
- The regional coordinator checks records; followed by automated and manual validation procedures to verify site location data.

## Format of stored data

- Site Location Data are stored as a CSV with columns:
  - Site number (unique sequential)
  - Site name
  - Gridreference (6-figure accuracy, central transect location)
  - Easting
  - Northing
  - Length (metres)
  - Country
  - No. Sections
  - No. Yrs surveyed
  - First year surveyed
  - Last year surveyed (up to 2012)